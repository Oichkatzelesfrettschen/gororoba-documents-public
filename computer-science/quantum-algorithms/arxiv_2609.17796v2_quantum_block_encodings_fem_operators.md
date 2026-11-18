Source: https://arxiv.org/abs/2609.17796v2
PDF sha256: 1a367d5233c1466d23e5fbbd99374cf3376ebabe980bf2995e6b92f62a888683
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of arxiv_2609.17796v2_quantum_block_encodings_fem_operators.pdf

Transcription of `arxiv_2609.17796v2_quantum_block_encodings_fem_operators.pdf` in this directory, 22 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-22 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Quantum Block Encodings for Periodic Two-Phase Finite Element
Operators: 2D Poisson and 2D Elasticity
Krishnan Suresha,∗
a University of Wisconsin–Madison, Department of Mechanical Engineering, Madison, WI, 53706, USA

ABSTRACT

Keywords:
block encoding
linear combination of unitaries
shift decomposition
computational homogenization
plane-stress elasticity
two-phase microstructure

Quantum algorithms require embedding linear operators into unitaries using block encodings.
The costs associated with these block encodings determine whether a quantum speedup is
achieved. Efficient shift decomposition encodings have been proposed for 2D homogeneous
scalar operators. Here, we present exact block encodings for 2D homogeneous elasticity, 2D
two-phase bilinear Poisson, and 2D two-phase elasticity periodic finite-element operators.
For 2D homogeneous elasticity, the resulting linear combination of unitaries (LCU) has
𝐿 = 17 terms for every Poisson [
ratio 𝜈 and ]every mesh resolution, and the subnormalization
is the closed form 𝛼 = 𝐸(33 + 𝜈)∕ 6(1 − 𝜈 2 ) , exceeding ‖𝐊‖2 by the resolution-independent
factor (33 + 𝜈)∕24.
To address two-phase periodic microstructures, we introduce two oracles with distinct roles:
a node-to-element oracle, built from cyclic shifts, that carries a nodal index to each of the
four incident element indices, and a microstructure-specific material oracle that marks phase
membership with a sign. This yields 25 and 57 LCU terms for two-phase Poisson and elasticity,
respectively; the latter reduces to 49 at 𝜈 = 1∕3. The term counts are independent of mesh
resolution, volume fraction, and phase contrast. The subnormalizations, provided in closed form,
are independent of mesh resolution and volume fraction. In the scalar case, the tight bound
𝛼 = ‖𝐊‖∞ is achieved whenever a node lies entirely in the stiffer phase. In the elasticity case that
bound is not attained, since the shear coupling contributes entries of both signs to a row. An opensource implementation is available at https://github.com/UW-ERSL/PyBlockEncode.

arXiv:2609.17796v2 [cs.CE] 17 Sep 2026

ARTICLE INFO

1. Introduction

Quantum algorithms for linear systems, differential equations, and matrix functions promise substantial speedups
for large-scale computational problems [1, 2, 3, 4, 5]. Modern algorithmic formulations require the underlying operator
𝐀 to be embedded in a larger unitary  as a block encoding: an (𝑎 + 𝑛)-qubit unitary whose top-left 2𝑛 × 2𝑛 block is
𝐀∕𝛼 for some subnormalization 𝛼 ≥ ‖𝐀‖2 . Constructing that encoding is the first step of every modern pipeline. The
block encoding cost determines whether a quantum speedup is achieved. A general-purpose encoder working from the
entries of 𝐀 alone, such as FABLE [6], costs (4𝑛 ) gates at 𝛼 = 2𝑛 max𝑖𝑗 |𝐴𝑖𝑗 | for a 2𝑛 × 2𝑛 matrix, and the exponential
overhead is unavoidable without structure [7].
Operators in computational mechanics over regular meshes typically have structure. A finite element discretization
on a regular grid is sparse, assembled from one small element matrix, and expressible in terms of cyclic shifts. A
substantial literature, reviewed in Section 2, uses this structure for scalar 1D and 2D homogeneous operators.
In this work, we construct exact shift-decomposition-based block encodings of three operators: 2D homogeneous
elasticity, 2D two-phase bilinear Poisson, and 2D two-phase elasticity.
Section 2 provides a brief technical background and reviews the literature. Section 3 recalls the shift-decomposition
encoding of the periodic homogeneous Poisson cell, and Section 4 derives the same for elasticity. Section 5 introduces
the two-phase microstructure, the node-to-element mapping and the material oracle. Section 6 and Section 7 generalize
the two encodings to two phases. Section 8 describes the circuit and summarizes the resources, and Section 9 documents
the open-source implementation and the reproduction of every table reported here. Appendix A draws the four circuits
at 𝑚 = 2.
∗ Corresponding author

ksuresh@wisc.edu (K. Suresh)

ORCID (s): 0000-0002-9688-9697 (K. Suresh)

K. Suresh: Preprint submitted to Elsevier

Page 1 of 22

## PDF page 2

Block encodings for periodic two-phase finite element operators

2. Background
2.1. Block Encoding and LCU
A unitary  acting on 𝑎 + 𝑛 qubits is an (𝛼, 𝑎, 𝜀)-block encoding [4] of an 𝑛-qubit operator 𝐀 if
(
) (
)‖
‖
‖𝐀 − 𝛼 ⟨0|⊗𝑎 ⊗ 𝐼  |0⟩⊗𝑎 ⊗ 𝐼 ‖ ≤ 𝜀.
‖
‖2

(1)

We place the system register on the least-significant qubits, so the encoded block is the contiguous top-left corner
 [∶2𝑛 , ∶2𝑛 ]. Setting 𝜀 = 0 gives an exact encoding.
The canonical construction assembles  as a linear combination of unitaries (LCU) [8, 5]. Given
𝐀=

𝐿−1
∑

(2)

𝑐𝑘 𝑈𝑘

𝑘=0

with unitaries 𝑈𝑘 and real coefficients 𝑐𝑘 , the subnormalization is 𝛼 =
𝑈𝑘 is a generalized permutation, carrying one nonzero entry per row,
∑
∑
|𝐴𝑖𝑗 | ≤ 𝛼 =
|𝑐𝑘 |.
‖𝐀‖2 ≤ ‖𝐀‖∞ = max
𝑖

𝑗

∑

𝑘 |𝑐𝑘 |. For symmetric 𝐀, and whenever every

(3)

𝑘

Every unitary used in this paper is of that form: each 𝑈𝑘 has at most one entry in a given row, so no cancellation
between terms can push 𝛼 below the largest absolute row sum, and ‖𝐀‖∞ is a floor on what the decomposition can
attain.
2 ∕𝛼 2 at ‖𝑥‖ = 1, and
The subnormalization 𝛼 controls both the post-selection success probability 𝑝 = ‖𝐀𝑥‖√
2
the query complexity of downstream routines. The circuit then has three stages: PREP loads |𝑐𝑘 |∕𝛼 into the ancilla
register, SELECT applies 𝑈𝑘 controlled on the ancilla state |𝑘⟩, and UNPREP uncomputes the ancilla, with the sign of
𝑐𝑘 absorbed into 𝑈𝑘 or carried by a second preparation. On the |0⟩-ancilla subspace,
∑
(
) (
)
|𝑐𝑘 |.
(4)
⟨0|anc ⊗ 𝐼  |0⟩anc ⊗ 𝐼 = 𝐀∕𝛼, 𝛼 =
𝑘

Consequently, three quantities determine the cost of block-encoding:
∑
1. The subnormalization 𝛼 = 𝑘 |𝑐𝑘 |, which affects the query complexity linearly and the post-selection probability
quadratically.
2. The Toffoli count of SELECT, which, for a generic implementation, is (𝐿) [9].
3. The arbitrary-angle rotation count of PREP, which dominates the fault-tolerant cost because each rotation costs
(log 1∕𝜀syn ) 𝑇 gates at precision 𝜀syn , while everything else is Clifford and Toffoli.
The PREP register must address all 𝐿 terms, so its width satisfies 𝑛prep ≥ ⌈log2 𝐿⌉. A dense PREP on 𝑛prep qubits uses
2𝑛prep − 1 rotations, whether or not every index carries amplitude.

2.2. Pauli Encodings
The common generic approach is LCU expansion in the Pauli basis [10]. The Pauli term count, verified numerically
for 𝑚 = 2 to 6, is
⎧3 𝑚
⎪42 ,
⎪ 9 4𝑚 ,
⎪ 16
𝐿Pauli = ⎨ 9 4𝑚 − 1,
8
⎪(2𝑚+1 − 1)2 ,
⎪ 19
⎪ 4𝑚 − 11 ⋅ 2𝑚 + 1,
⎩2

1D Poisson,
2D Poisson (FE),
2D elasticity,
2D Poisson, 2-phase,
2D elasticity, 2-phase,

(5)

for 𝑚 qubits per spatial direction. The two 2-phase counts hold at every contrast, but they are specific to the
microstructure of Figure 1; other microstructures may give different counts. The subnormalization grows quadratically
K. Suresh: Preprint submitted to Elsevier

Page 2 of 22

## PDF page 3

Block encodings for periodic two-phase finite element operators

in 𝑚 for both homogeneous 2D cases. Considerable effort has gone into computing Pauli coefficients faster, through
tensorized recursion [11], tree traversal [12], symmetry-restricted enumeration [13] and the fast Walsh–Hadamard
transform [14].
Beyond standard Pauli decompositions, several alternative matrix encoding strategies have been proposed. Lu et
al. [15] benchmarked multiple encoding approaches: parallel Walsh–Hadamard expansions, standard LCU methods,
and an SVD-based singular value dilation that reduces any real square matrix to an exact two-term LCU. The SVD
dilation attains 𝛼 = ‖𝐀‖2 , but its two factors are dense rather than generalized permutations. Other general blockencoding frameworks, such as state preparation pairs or oracle-based linear combinations of unitaries [4], similarly
shift the computational complexity to deep state-preparation circuits or unmapped oracle operations unless specific
structural assumptions are made. Xu and Hu [16] remove the operator encoding entirely; instead they vectorize 𝐊 and
evaluate the variational cost functions as inner products through a swap test; the expense moves to state preparation,
which they state as an open problem.
Kuklinski et al. [7] make the premise of this paper precise: efficient block encodings require structure.

3. Structured Block Encoding
On a regular grid, a finite difference (FD) or finite element (FE) discretization of the Poisson or elasticity operator
produces a matrix that is sparse and translation invariant: every node carries the same stencil, built from a small set
of repeated entries. Structured block encoding is the collection of techniques that use this structure so that the gate and
ancilla counts scale as (poly(𝑚)) rather than (2𝑚 ), and the subnormalization stays constant, for an 𝑚-qubit operator.
Several families of structured block encoding have been proposed. These include shift decomposition, where we
write the operator in closed form as a short sum of shift operators and use that sum in an LCU [8, 17, 18, 19, 20].
A closely related recursion expands the Dirichlet stencil in (𝑚) terms built from the ladder operators 𝝈± = (𝑿 ±
𝑖𝒀 )∕2 [21]; Gnanasekaran and Surana [22] generalize this to a basis of such operators and recover the decomposition
by unitary completion, at (𝑚) terms for the one-dimensional Poisson operator and a SELECT cost that grows with the
term count. The sparse-access approach places the nonzero values of a structured operator by addressing them directly,
through a pair of oracles [23, 24, 25]. Finally, the element-decomposition method, which is specific to FE, assembles
the global stiffness matrix from small element matrices [26, 27].
This paper focuses on the shift decomposition approach and addresses two limitations in the literature. The first
is the scalar restriction. Shift decomposition has been developed for scalar operators, and the two constructions that
address linear elasticity take a different approach: Hölscher et al. [27] take an LCU over elements, so the term count
equals the element count and the subnormalization grows with the mesh, and Danz et al. [25] build the stiffness and
mass matrices of an elastic structure from general fixed-point arithmetic oracles. Neither yields a decomposition whose
length is independent of resolution.
The second limitation is the homogeneity restriction. Block encodings of variable-coefficient operators do exist:
Deiml and Peterseim [28] admit an arbitrary spatially varying coefficient but leave its oracle abstract and the
subnormalization grows with the ellipticity contrast; Pechan et al. [29] construct a heterogeneous three-dimensional
Poisson encoding from the sparse local structure of the discretized operator, at a subnormalization bounded by the
largest conductivity in the cell; Yano and Sato [30] represent a piecewise coefficient profile by a controlled Fourier
series, which is approximate at a material interface. What none of them provides is a linear combination of fixed length
in closed form, over a material oracle realized exactly.
Table 1 compares the scope of the proposed work against the existing literature.

3.1. 1D Homogeneous Periodic Poisson
Shift decomposition is easiest to see on a 1D operator. For the 1D Poisson problem on 𝑁 = 2𝑚 periodic nodes,
discretized using linear finite elements of unit element length, leads to the stiffness matrix
⎡ 2 −1
⎢−1 2
𝐊1𝐷 = ⎢
⋮
⎢
⎣−1 0

0 ⋯
−1 ⋯
⋱
⋯ −1

−1⎤
0⎥
,
⋮⎥
⎥
2⎦

(6)

where the corner entries carry the periodic wrap. This can be expressed compactly as
𝐊1𝐷 = circ(−1, 2, −1),
K. Suresh: Preprint submitted to Elsevier

(7)
Page 3 of 22

## PDF page 4

Block encodings for periodic two-phase finite element operators
Table 1
Prior block encodings and the present construction. S scalar, V vector; FD finite difference, FE finite element; Dim spatial
dimension, 𝑑 any dimension; U uniform, H heterogeneous, 2 two-phase; Y/N whether the work names a public repository.
(1) means constant in 𝑁; the term count of a shift construction grows linearly with 𝑑 for finite differences and as 3𝑑
for tensor-product finite elements. † also treats non-periodic boundary conditions; ‡ holds for constant coefficients; § the
framework is stated for any 𝑑, but the stiffness analysis is carried out in one dimension; ⋆ the two SVD factors are dense
and unstructured, and no efficient circuit for them is given. n/a marks a quantity that does not apply, a dash one the cited
work does not report. Every 𝛼 is quoted at unit element length.
work

Op

FE/FD

Dim

Mat

Approach

𝐿

𝛼

Kharazi (2025) [17]

S

FD

𝑑

Sturm (2025) [18]

S

FD

𝑑

Hogancamp (2026) [20]

S

FD

𝑑

U

Mahmud (2026) [31]

S

FD

𝑑

U

Gnanasekaran (2026) [22]

S

FD

1§

U

Alkadri (2025) [19]

S

FE

𝑑

U, H

element LCU

code

U

shift†

(1)

(1)

Y

U

shift

(1)

(1)

N

shift†

(1)

(1)

N

shift + optimality

(1)

(1)

N

ladder + completion

(𝑚)

—

N

(1)‡

(1)‡

N
Y

Deiml (2025) [28]

S

FE

𝑑

H

FE + BPX, oracle

n/a

∝ contrast

Pechan (2026) [29]

S

FD

3

H

sparse access

n/a

12𝑘max

Y

Yano (2026) [30]

S

FD

𝑑

H

diagonal, Fourier

n/a

assumed

N

Danz (2026) [25]

V

FE

1§

U, H

arithmetic oracle

n/a

—

N

Arora (2025) [26]

S

FE

1

H

VQLS; element

𝑁 +2

n/a

N

Lu (2026) [15]

S

any

2

n/a

coh. VQLS; SVD

2⋆

1⋆

N

Hölscher (2026) [27]

V

FE

2

2

element + Grover

(𝑛el )

𝑛el 𝛿

Y

This work

S, V

FE

2

2

shift + reflections

(1)

(1)

Y

where circ(𝑎, 𝑏, 𝑐) carries 𝑎 on the sub-diagonal, 𝑏 on the diagonal and 𝑐 on the super-diagonal, each off-diagonal band
wrapping into the opposite corner.
Let 𝑆𝑐 be the cyclic shift
⎡0
⎢1
𝑆𝑐 = ⎢ 0
⎢
⎢⋮
⎣0

0
0
1
0

0 ⋯
0 ⋯
0 ⋯
⋱
⋯ 1

1⎤
0⎥
0⎥ ,
⎥
⋮⎥
0⎦

(8)

so that 𝑆𝑐 ∶ |𝑗⟩ ↦ |(𝑗+1) mod 𝑁⟩. It is a permutation matrix, hence unitary, and its adjoint 𝑆𝑐† is the backward shift.
Thus Equation (6) can be expressed as
𝐊1𝐷 = 2𝐼 − 𝑆𝑐 − 𝑆𝑐† .

(9)

This is an exact LCU, and hence a block encoding: three unitaries, coefficients known in closed form, and a
subnormalization 𝛼 = 4 that does not grow with 𝑁. The cost is one increment modulo 𝑁 of depth (𝑚) [32, 23];
the controlled ripple-carry increment used here costs 2𝑚 − 2 Toffoli, 𝑚 CNOT and 𝑚 − 1 clean ancillas that are
returned to |0⟩ and reused by every shift in the circuit [33, 34].
Table 2 compares the cost of encoding 𝐊1𝐷 using shift decomposition against an exact Pauli expansion of the same
operator at 𝑚 = 12. The gap widens in 2D and for heterogeneous cells. For the 1D cell, the chain ‖𝐊‖2 ≤ ‖𝐊‖∞ ≤ 𝛼
collapses to equality, so the shift decomposition is optimal.

3.2. 2D Homogeneous Periodic Poisson
For a 2D periodic Poisson problem consisting of a 𝑁 × 𝑁 grid of bilinear 𝑄4 elements, the finite element operator
separates into 1D factors [35, 36, 19],
𝐊2𝐷,sc = 𝐊1𝐷 ⊗ 𝐌1𝐷 + 𝐌1𝐷 ⊗ 𝐊1𝐷 ,
K. Suresh: Preprint submitted to Elsevier

(10)
Page 4 of 22

## PDF page 5

Block encodings for periodic two-phase finite element operators
Table 2
Periodic 1D finite element Poisson cell at 𝑚 = 12 qubits, 4,096 degrees of freedom. The shift column is measured; the
Pauli column is exact in closed form, 𝐿 = 34 2𝑚 , 𝛼 = 𝑚 + 2 and 𝑝succ = 16∕(𝑚 + 2)2 , since ‖𝐊1𝐷 ‖2 = 4 at every even 𝑁. This
is the one cell in which the comparison is tabulated; the four 2D cells follow the same pattern more sharply, at the term
counts of Equation (5).
quantity

Pauli

shift

terms 𝐿
prep qubits
prep slots
select Toffoli
𝛼
𝑝succ

3,072
12
4,096
3,072
14.0
0.082

3
2
4
48
4.000
1.00

where 𝐌1𝐷 = 16 circ(1, 4, 1) is the consistent mass matrix. Throughout this paper, the left factor of a Kronecker product
acts on the 𝑥 register, the next on the 𝑦 register; ⊗ thus lists registers from least to most significant, the reverse of the
matrix Kronecker product. Both factors are three-band circulants, so both admit the shift decomposition of Section 3.1,
𝐌1𝐷 = 64 𝐼 + 16 𝑆𝑐 + 61 𝑆𝑐† ,

(11)

and Equation (10) expands over the nine unitaries {𝐼, 𝑆𝑐 , 𝑆𝑐† }⊗2 . This approach to the periodic scalar cell is due to
Sturm and Schillo [18] and, for tensor-product finite elements, to Qu-FEM [19].
Merging the coefficients that land on the same pair of shifts,
∑
𝑈𝑝 ⊗ 𝑈 𝑞 ,
(12)
𝐊2𝐷,sc = 38 𝐼 ⊗ 𝐼 − 13
(𝑈𝑝 ,𝑈𝑞 )≠(𝐼,𝐼)

nine terms with
𝛼2𝐷,sc = 83 + 8 ⋅ 13 = 16
.
3

(13)

As a nodal stencil, Equation (12) is the bilinear nine-point Laplacian, and 𝛼2𝐷,sc = ‖𝐊2𝐷,sc ‖∞ exactly.
9 𝑚
The shift decomposition is independent of mesh resolution, against 16
4 terms at 𝛼 = (𝑚2 +2𝑚+8)∕3 for a generic
Pauli expansion of the same operator.

4. 2D Homogeneous Elasticity
In this section, we extend the above results to 2D homogeneous periodic elasticity. Ordering rows and columns by
displacement component gives the familiar 2 × 2 block
[
]
𝐊𝑥𝑥 𝐊𝑥𝑦
𝐊2𝐷,el =
.
(14)
𝐊𝑦𝑥 𝐊𝑦𝑦
The blocks separate [35, 37] as
)
(
𝐌
⊗
𝐊
𝐊𝑥𝑥 = 𝐶 𝐊1𝐷 ⊗ 𝐌1𝐷 + 1−𝜈
1𝐷
1𝐷 ,
2
)
(
𝐊
⊗
𝐌
+
𝐌
⊗
𝐊
,
𝐊𝑦𝑦 = 𝐶 1−𝜈
1𝐷
1𝐷
1𝐷
1𝐷
2
(
)
1+𝜈
𝐊𝑥𝑦 = 𝐊⊤
𝐆1𝐷 ⊗ 𝐆1𝐷 ,
𝑦𝑥 = −𝐶 2

(15)
(16)
(17)

where 𝐶 = 𝐸∕(1 − 𝜈 2 ) and 𝐆1𝐷 = 12 circ(−1, 0, 1) is the antisymmetric gradient coupling, whose shift decomposition
is
𝐆1𝐷 = 12 𝑆𝑐† − 12 𝑆𝑐 .
K. Suresh: Preprint submitted to Elsevier

(18)
Page 5 of 22

## PDF page 6

Block encodings for periodic two-phase finite element operators

The 𝐆1𝐷 ⊗ 𝐆1𝐷 coupling is the new cross-derivative term. Since 𝐆1𝐷 is antisymmetric, 𝐆1𝐷 ⊗ 𝐆1𝐷 is symmetric, so
𝐊𝑥𝑦 = 𝐊𝑦𝑥 on a periodic homogeneous grid.
Elasticity carries 𝑛𝑑 = 2 degrees of freedom per node, so 𝐊2𝐷,el is 2𝑁 2 × 2𝑁 2 and the 2 log2 𝑁 spatial qubits no
longer address it. One further qubit is required, the dof qubit |𝑑⟩, with 𝑑 = 0 selecting the 𝑥 displacement and 𝑑 = 1
the 𝑦 displacement. It is now the most significant qubit of the system register, following the 𝑥 and 𝑦 registers.
Equation (14) is the sum of three matrices, a block-diagonal average, a block-diagonal difference, and a purely
off-diagonal part. With 𝐊𝑥𝑦 = 𝐊𝑦𝑥 each is a single Kronecker product,
[
]
𝐊𝑥𝑥 +𝐊𝑦𝑦
𝟎
𝐊2D,el = 21
𝟎
𝐊𝑥𝑥 +𝐊𝑦𝑦
[
]
𝟎
1 𝐊𝑥𝑥 −𝐊𝑦𝑦
+2
(19)
𝟎
𝐊𝑦𝑦 −𝐊𝑥𝑥
[
]
𝟎
𝐊𝑥𝑦
+
,
𝐊𝑥𝑦
𝟎
each term a single Kronecker product of an 𝑁 2 × 𝑁 2 spatial block with 𝐼, 𝑍 and 𝑋 respectively, so that
𝐊2𝐷,el =

𝐊𝑥𝑥 +𝐊𝑦𝑦
2

⊗𝐼 +

𝐊𝑥𝑥 −𝐊𝑦𝑦
2

⊗ 𝑍 + 𝐊𝑥𝑦 ⊗ 𝑋.

(20)

This splits 𝐊2𝐷,el into three Pauli components, each an 𝑁 2 × 𝑁 2 spatial block tensored with one single-qubit matrix.
We can now substitute the shift decompositions of 𝐊1𝐷 , 𝐌1𝐷 and 𝐆1𝐷 into Equation (20) to arrive at the following
proposition.
Proposition 1. For the periodic plane-stress 𝑄4 elasticity operator with Young’s modulus 𝐸 and Poisson ratio 𝜈, the
global stiffness matrix 𝐊2𝐷,el admits the exact LCU
∑
(21)
𝑐𝑝𝑞𝑟 𝑈𝑝(𝑥) ⊗ 𝑈𝑞(𝑦) ⊗ 𝜎𝑟(𝑑) ,
𝐊2𝐷,el =
(𝑝,𝑞,𝑟)∈

with 𝑈𝑝 , 𝑈𝑞 ∈ {𝐼, 𝑆𝑐 , 𝑆𝑐† }, 𝜎𝑟 ∈ {𝐼, 𝑍, 𝑋}, and  the set of triples carrying a nonzero coefficient, of size | | = 17
for every 𝜈 ∈ (−1, 21 ) and every 𝑁 = 2𝑚 with 𝑚 ≥ 2. The subnormalization is
𝛼2𝐷,el (𝜈) =

𝐸 (33 + 𝜈)
,
6 (1 − 𝜈 2 )

(22)

constant in 𝑁.
Proof. Substitute the shift decompositions of 𝐊1𝐷 , 𝐌1𝐷 and 𝐆1𝐷 into the three Pauli components of Equation (20) and
merge coefficients landing on the same shift pair. The 𝐼 and 𝑍 components expand over the nine pairs {𝐼, 𝑆𝑐 , 𝑆𝑐† }⊗2 ,
the 𝑋 component over the four pairs carrying a shift in both directions, since 𝐆1𝐷 has no identity term. Of the nine 𝑍
entries only the four axis pairs survive the antisymmetric combination 𝐊1𝐷 ⊗𝐌1𝐷 −𝐌1𝐷 ⊗𝐊1𝐷 , giving 9+4+4 = 17.
The nine pairs are distinct as operators for 𝑚 ≥ 2, where 𝑆𝑐 ≠ 𝑆𝑐† , so no further merging occurs, and no coefficient
vanishes: the 𝐼 prefactor carries (3−𝜈) and the 𝑍 and 𝑋 prefactors carry (1+𝜈), vanishing only at 𝜈 = 3 and 𝜈 = −1
respectively, neither of which the plane-stress operator admits. For 𝛼, the merged coefficients of the spatial factors sum
in magnitude to 16∕3, 4 and 1 for the 𝐼, 𝑍 and 𝑋 components respectively, and weighting them by the component
prefactors 𝐶(3−𝜈)∕4, 𝐶(1+𝜈)∕4 and 𝐶(1+𝜈)∕2 gives Equation (22).
Table 3 groups the 17 terms. There are at most four distinct magnitudes. The eight non-identity shift pairs are the
eight stencil neighbors: four axis pairs such as (𝑆, 𝐼) and (𝐼, 𝑆 † ), and four diagonal pairs such as (𝑆, 𝑆) and (𝑆 † , 𝑆).
The spectral norm is ‖𝐊2𝐷,el ‖2 = 4𝐶 for every 𝜈 and every 𝑁, so the ratio 𝛼2𝐷,el ∕‖𝐊2𝐷,el ‖2 is a closed form,
𝛼2𝐷,el
33 + 𝜈
=
,
(23)
‖𝐊2𝐷,el ‖2
24
which is 1.3875 at 𝜈 = 0.3.
The term count 𝐿 = 17 and the closed form 𝛼2𝐷,el (𝜈) hold at every 𝑚 ≥ 2, against 89 4𝑚 − 1 terms for an exact Pauli
expansion of the same operator (Equation (5)).
K. Suresh: Preprint submitted to Elsevier

Page 6 of 22

## PDF page 7

Block encodings for periodic two-phase finite element operators
Table 3
The 17 LCU terms of the periodic plane-stress 𝑄4 elasticity operator at 𝐸 = 1, grouped by coefficient. 𝑆 ≡ 𝑆𝑐 , 𝑆 † ≡ 𝑆𝑐† ,
and the pair (𝑈𝑝(𝑥) , 𝑈𝑞(𝑦) ) names the stencil offset. Summing the distinct magnitudes with their multiplicities gives 𝛼2𝐷,el (𝜈)
of Equation (22).
𝜎𝑟

stencil offsets (𝑈𝑝(𝑥) , 𝑈𝑞(𝑦) )

#

𝐼

(𝐼, 𝐼), the centre

1

𝐼

all eight neighbours

8

𝑍

(𝐼, 𝑆), (𝐼, 𝑆 † )

2

𝑍

(𝑆, 𝐼), (𝑆 † , 𝐼)

2

𝑋

(𝑆, 𝑆 † ), (𝑆 † , 𝑆)

2

𝑋

(𝑆, 𝑆), (𝑆 † , 𝑆 † )

2

𝛼2𝐷,el =

∑

𝑘 |𝑐𝑘 |

17

coefficient
2(3 − 𝜈)
3(1 − 𝜈 2 )
3−𝜈
−
12(1 − 𝜈 2 )
1
+
4(1 − 𝜈)
1
−
4(1 − 𝜈)
1
+
8(1 − 𝜈)
1
−
8(1 − 𝜈)
𝐸(33 + 𝜈)
6(1 − 𝜈 2 )

𝜈 = 0.3
+1.9780
−0.2473
+0.3571
−0.3571
+0.1786
−0.1786
6.0989

5. Two-Phase Microstructure
We now turn our attention to finite element meshes that carry two materials. We refer to the spatial distribution
of the two phases as the microstructure. The periodic two-phase cell is the natural target, because it is the unit cell of
computational homogenization [38, 39, 40, 41].
With a second phase, the operator is no longer translation invariant. This leads to two challenges. First, the material
is defined element by element, whereas the shift operators act on nodal registers, so the encoding must relate the two
indices; Section 5.1 constructs this node-to-element mapping from cyclic shifts. Second, the element moduli must enter
the linear combination as unitaries. A diagonal modulus matrix is not unitary, and expanding it in a generic basis would
tie 𝐿 to the microstructure; Section 5.2 writes it instead as a combination of the identity and a material reflection, with
coefficients determined by 𝐸1 and 𝐸2 . Sections 6 and 7 then assemble the two-phase operators from these pieces.
Figure 1 shows the primary example used throughout: a square inclusion of side 𝑁∕2 at the center of the cell. Each
phase carries its own material property. For the Poisson problem, 𝐸1 and 𝐸2 are the conductivities of the two phases;
for elasticity, they are the two Young’s moduli, with a common Poisson ratio 𝜈. Each element 𝑒 carries a modulus
implied from these two phases,
𝐸𝑒 = 𝐸2 + (𝐸1 − 𝐸2 ) 𝜒𝑒 ,

𝜒𝑒 ∈ {0, 1},

(24)

where 𝜒𝑒 is the microstructure-specific binary field discussed in Section 5.2.
The assumed periodicity of the microstructure links opposite boundaries of the domain. Under this assumption, an
𝑁 × 𝑁 mesh carries 𝑁 2 elements and 𝑁 2 distinct nodes. We index both nodes and elements using 2𝑚 qubits, where
𝑁 = 2𝑚 . We write |𝑒⟩, with 𝑒 = (𝑒𝑥 , 𝑒𝑦 ), when the register is read as an element index, and |𝑖⟩, with 𝑖 = (𝑖𝑥 , 𝑖𝑦 ), when
read as a nodal index.

5.1. Node-to-Element Mapping
The material field is defined element by element, whereas the shift operators of Section 3 act on nodal registers.
We therefore define a mapping from one to the other.
Each grid node is touched by four adjacent elements, located at the relative spatial offsets
(𝑎, 𝑏) ∈  ∶= {(0, 0), (−1, 0), (0, −1), (−1, −1)}.

(25)

Figure 2 illustrates this for the node 𝑖 = (8, 3).
(
)
The node-to-element mapping 𝑆(𝑎,𝑏) carries the nodal register |𝑖⟩ to the element index 𝑒 = 𝑖 + (𝑎, 𝑏) mod 𝑁,
componentwise:
𝑆(𝑎,𝑏) = 𝑆𝑐𝑎 ⊗ 𝑆𝑐𝑏 ,
K. Suresh: Preprint submitted to Elsevier

(26)
Page 7 of 22

## PDF page 8

Block encodings for periodic two-phase finite element operators

where 𝑆𝑐 is the 1D cyclic forward shift of Equation (8) and 𝑆𝑐−1 = 𝑆𝑐† its backward counterpart. Thus, for example,
𝑆(1,0) = 𝑆𝑐1 ⊗ 𝑆𝑐0 = 𝑆𝑐 ⊗ 𝐼.

(27)

Since  = {0, −1}2 , the mapping factorizes over the two spatial registers, and the four offsets of Equation (25) are
generated by one conditional shift per register. The offsets are taken modulo 𝑁, so a node on the last row or column
reaches elements in the first, and  is the same four offsets at every node with no exception at the mesh ends. Periodicity
is also what makes 𝑆(𝑎,𝑏) a permutation, and hence unitary. 𝑆(𝑎,𝑏) acts purely as a spatial coordinate translation, without
referencing the material property or the microstructure geometry.

5.2. The Material Oracle and Reflection
The microstructure itself is defined as a binary field on the elements,
𝜒 ∶ {0, … , 𝑁−1}2 → {0, 1},

(28)

where
𝑣𝑓 =

1 ∑
𝜒𝑒 ,
𝑁2 𝑒

(29)

is the volume fraction of phase 1. We write 𝑟 = 𝐸1 ∕𝐸2 for the phase contrast ratio.
Two-phase encoding requires a quantum circuit that evaluates the membership field 𝜒. For the square inclusion in
Figure 1 the membership test factorizes into independent conditions on 𝑒𝑥 and 𝑒𝑦 . An element lies inside the inclusion
when 𝑒𝑥 ∈ [𝑁∕4, 3𝑁∕4) and 𝑒𝑦 ∈ [𝑁∕4, 3𝑁∕4). The two leading bits of 𝑒𝑥 , with 𝑒𝑥,𝑚−1 the most significant, place
it in one of four quarters, and 𝑒𝑥 lies in range precisely when 𝑒𝑥,𝑚−1 ⊕ 𝑒𝑥,𝑚−2 = 1. Applying the identical condition to
𝑒𝑦 yields the Boolean predicate
)
)
(
(
(30)
𝜒𝑒 = 𝑒𝑥,𝑚−1 ⊕ 𝑒𝑥,𝑚−2 ∧ 𝑒𝑦,𝑚−1 ⊕ 𝑒𝑦,𝑚−2 ,
for every 𝑚 ≥ 2. Note that Equation (30) applies only to the microstructure of Figure 1; other microstructures require
their own predicates.
Given the Boolean indicator 𝜒𝑒 , the material phase enters the block encoding through the material reflection oracle
𝑅𝜒 :
𝑅𝜒 = 𝐼 − 2 diag(𝜒),

(31)

which acts on the element state |𝑒⟩ by applying a phase flip conditional on phase membership,
𝑅𝜒 |𝑒⟩ = (−1)𝜒𝑒 |𝑒⟩.

(32)

The operator 𝑅𝜒 is diagonal, Hermitian, and unitary (𝑅2𝜒 = 𝐼). Because it marks states with a phase rather than a flag
register, it requires no additional ancilla qubits and enters linear combinations of unitaries directly. Under Equation (30),
𝑅𝜒 acts on exactly four qubits at every 𝑚, the two leading bits of each coordinate: two CNOT gates compute the two
parities in place, one controlled 𝑍 applies the phase, and two CNOT gates restore the register. No ancilla is needed,
because the parities are computed in place on the coordinate registers rather than onto shift-control qubits. For this
microstructure the cost is four CNOT and one controlled 𝑍 at every 𝑚 ≥ 2.
Combining the mapping 𝑆(𝑎,𝑏) with the base oracle 𝑅𝜒 yields the four element-wise material reflection operators
𝑅(𝑎,𝑏) as seen from node 𝑖. Reading right to left, the nodal index is carried to the element index, the oracle is queried
there, and the index is carried back:
(
)
†
𝑅(𝑎,𝑏) = 𝑆(𝑎,𝑏)
𝑅𝜒 𝑆(𝑎,𝑏) = 𝐼 − 2 diag 𝜒 𝑖+(𝑎,𝑏) 𝑖 .
(33)
(
)
Writing 𝐷(𝑎,𝑏) ∶= diag 𝐸 𝑖+(𝑎,𝑏) 𝑖 for the modulus of the element at offset (𝑎, 𝑏) as seen from node 𝑖, the two-phase
field of Equation (24) gives
𝐷(𝑎,𝑏) =

𝐸1 + 𝐸2
𝐸 − 𝐸2
𝐼 − 1
𝑅(𝑎,𝑏) .
2
2

K. Suresh: Preprint submitted to Elsevier

(34)

Page 8 of 22

## PDF page 9

Block encodings for periodic two-phase finite element operators

Figure 1: The two-phase cell at 𝑚 = 5: a square inclusion of side 𝑁∕2, centered, at volume fraction 𝑣𝑓 = 1∕4. The inclusion
carries 𝜒𝑒 = 1 and is left unshaded; the matrix carries 𝜒𝑒 = 0.

(7, 4)

(8, 4)

(9, 4)

e = (7, 3) e = (8, 3)

(7, 3)

(8, 3)

(9, 3)

e = (7, 2) e = (8, 2)

(7, 2)

(8, 2)

(9, 2)

Figure 2: The four elements incident on node 𝑖 = (8, 3), on the 2 × 2 patch surrounding it. Each element carries the index
of its own lower-left node, marked by a square, so the element at offset (𝑎, 𝑏) has index 𝑖 + (𝑎, 𝑏) and the four indices are
(8, 3), (7, 3), (8, 2) and (7, 2) as (𝑎, 𝑏) runs over Equation (25).

K. Suresh: Preprint submitted to Elsevier

Page 9 of 22

## PDF page 10

Block encodings for periodic two-phase finite element operators

6. Two-Phase Poisson
Section 3.2 decomposed the homogeneous cell into 1D factors. A variable modulus destroys that separation, so
we work instead at the level of the element matrix, where the modulus is a scalar multiplier and the shift structure
survives. At unit conductivity the bilinear 𝑄4 element matrix is
⎡ 4 −1 −2 −1⎤
1 ⎢−1 4 −1 −2⎥
𝐤 = ⎢
,
6 ⎢−2 −1 4 −1⎥⎥
⎣−1 −2 −1 4 ⎦

(35)

𝑒

its rows and columns running counterclockwise from the lower-left corner. We index them by the corners, writing
𝑘𝑒 [𝑐, 𝑐 ′ ] with 𝑐, 𝑐 ′ ∈ {0, 1}2 .
For node (𝑖𝑥 , 𝑖𝑦 ), Figure 2 shows the four incident elements and their offsets (𝑎, 𝑏) ∈ . Each of those elements
couples that node to all four of its own nodes, so a second index is needed to enumerate them. The element at offset
(𝑎, 𝑏) has lower-left node (𝑖𝑥 , 𝑖𝑦 )+(𝑎, 𝑏), so node (𝑖𝑥 , 𝑖𝑦 ) is its corner 𝑐 = −(𝑎, 𝑏) and its four nodes are (𝑖𝑥 , 𝑖𝑦 )+(𝑎, 𝑏)+𝑐 ′
as 𝑐 ′ runs over {0, 1}2 . That node couples to node (𝑖𝑥 , 𝑖𝑦 ) + 𝛿, with 𝛿 = (𝑎, 𝑏) + 𝑐 ′ , through the entry 𝑘𝑒 [𝑐, 𝑐 ′ ].
−𝛿

−𝛿

An entry in the row at (𝑖𝑥 , 𝑖𝑦 ) and the column at (𝑖𝑥 , 𝑖𝑦 ) + 𝛿 is the operator 𝑆𝑐 𝑥 ⊗ 𝑆𝑐 𝑦 , so the element at (𝑎, 𝑏)
contributes the four-term operator
∑
] −𝛿
[
−𝛿
(36)
𝐓(𝑎,𝑏) ∶=
𝑘𝑒 𝑐, 𝑐 ′ 𝑆𝑐 𝑥 ⊗ 𝑆𝑐 𝑦 ,
𝑐 ′ ∈{0,1}2

with 𝛿 = (𝑎, 𝑏) + 𝑐 ′ running with the sum. Scaling each element by its modulus gives the assembled operator
∑
𝜒
𝐊2𝐷,sc =
𝐷(𝑎,𝑏) 𝐓(𝑎,𝑏) ,

(37)

(𝑎,𝑏)∈

with 𝐷(𝑎,𝑏) defined in Equation (34).
The four 𝐓(𝑎,𝑏) merge into the nine-term homogeneous operator of Equation (12),
∑
𝐓(𝑎,𝑏) = 𝐊2𝐷,sc ,

(38)

(𝑎,𝑏)∈

and each carries the same four coefficients up to order, hence the same coefficient sum 34 , so the four together sum to
16
, which is 𝛼2𝐷,sc of Equation (13).
3

Substituting Equation (34) into Equation (37) splits the operator into a mean part, which merges by Equation (38),
and a contrast part, which does not:
𝐸 −𝐸 ∑
𝐸 +𝐸
𝜒
𝑅(𝑎,𝑏) 𝐓(𝑎,𝑏) .
(39)
𝐊2𝐷,sc = 1 2 𝐊2𝐷,sc − 1 2
2
2
(𝑎,𝑏)∈
The microstructure appears only inside the reflections.
Proposition 2. Equation (39) is an exact LCU of the two-phase periodic 𝑄4 Poisson operator in which every unitary
is a cyclic shift pair, optionally preceded by one material reflection. For every 𝐸1 ≠ 𝐸2 , every 𝜒 and every 𝑁 = 2𝑚
with 𝑚 ≥ 2 it has
𝐿 = 9 + 16 = 25,

𝜒

𝛼2𝐷,sc = 16
max(𝐸1 , 𝐸2 ).
3

(40)

At 𝐸1 = 𝐸2 the second family vanishes and 𝐿 collapses to the 9 of Equation (12).
Proof. The first family of Equation (39) is 𝐊2𝐷,sc , nine terms. The second is four reflections carrying four shifts each,
and the sixteen combinations occupy sixteen index slots distinct from each other and from the first family, so nothing
∑
𝜒
merges: 𝐿 = 25. For 𝛼2𝐷,sc , the first family contributes 12 (𝐸1 +𝐸2 ) 𝛼2𝐷,sc and the second 12 |𝐸1 −𝐸2 | (𝑎,𝑏) ‖𝐓(𝑎,𝑏) ‖,

where ‖𝐓(𝑎,𝑏) ‖ denotes the sum of the coefficient magnitudes of 𝐓(𝑎,𝑏) . Each ‖𝐓(𝑎,𝑏) ‖ is 34 , so the second sum is 16
,
3
]
𝜒
16 [
16
as is 𝛼2𝐷,sc , giving 𝛼2𝐷,sc = 3 (𝐸1 +𝐸2 ) + |𝐸1 −𝐸2 | ∕2, which is 3 max(𝐸1 , 𝐸2 ). The factor 𝐸1 − 𝐸2 gives the
collapse.
K. Suresh: Preprint submitted to Elsevier

Page 10 of 22

## PDF page 11

Block encodings for periodic two-phase finite element operators

Material contrast introduces no extra subnormalization penalty beyond scaling with the stiffer phase’s modulus.
Switching the soft and stiff phases gives the same subnormalization.
𝜒
𝜒
This subnormalization reaches the smallest value a shift-based LCU can attain, 𝛼2𝐷,sc = ‖𝐊2𝐷,sc ‖∞ , whenever
the mesh contains at least one node completely surrounded by the stiffer material. Because the matrix infinity norm
𝜒
‖𝐊2𝐷,sc ‖∞ is the maximum absolute row sum across all nodes, a single fully stiffened node raises the matrix norm to
𝜒

max(𝐸1 , 𝐸2 ), which equals 𝛼2𝐷,sc .
its upper limit of 16
3
If no such node exists, as in a fine checkerboard pattern where every node touches a mix of soft and stiff elements,
𝜒
max(𝐸1 , 𝐸2 ), making the bound less tight. For example, an 8 × 8
the maximum row sum ‖𝐊2𝐷,sc ‖∞ is smaller than 16
3
𝜒
𝜒
checkerboard with a 3 ∶ 1 material contrast yields ‖𝐊2𝐷,sc ‖∞ = 10.667 against 𝛼2𝐷,sc = 16. The encoding remains
𝜒
exact in all cases, but 𝛼2𝐷,sc reflects a worst-case material bound.
𝜒
Neither 𝐿 = 25 nor the circuit varies with the contrast; only the PREP angles and 𝛼2𝐷,sc do. An exact Pauli expansion

of the same operator leads to (2𝑚+1 − 1)2 terms at every contrast for the microstructure of Figure 1 (Equation (5)).

7. Two-Phase Elasticity
For two-phase elasticity, the construction of Section 6 applies unchanged once 𝑘𝑒 [𝑐, 𝑐 ′ ] becomes a 2 × 2 block.
Two things differ, and both belong to elasticity rather than to the method: a fourth dof component, 𝑖𝑌 , appears, and the
four element contributions at a node no longer share a sign.
The plane-stress 𝑄4 element matrix is 8 × 8, two degrees of freedom per node. Indexing rows and columns by
corners as before, 𝑘𝑒 [𝑐, 𝑐 ′ ] is now the 2 × 2 block coupling the two displacement components at the corner-𝑐 node to
those at the corner-𝑐 ′ node. Each block resolves
( 0 over
) the real orthogonal basis {𝐼, 𝑍, 𝑋, 𝑖𝑌 } of the dof register, the
1 , which is real and orthogonal and carries the antisymmetric part
first three as in Section 4 and the fourth 𝑖𝑌 = −1
0
of each block. Writing [ ⋅ ]𝑟 for the component along 𝜎𝑟 , the element at offset (𝑎, 𝑏) contributes
𝐓(𝑎,𝑏) ∶=

∑

∑[
] −𝛿
−𝛿
𝑘𝑒 [𝑐, 𝑐 ′ ] 𝑟 𝑆𝑐 𝑥 ⊗ 𝑆𝑐 𝑦 ⊗ 𝜎𝑟 ,

(41)

𝑐 ′ ∈{0,1}2 𝑟

with 𝑐 = −(𝑎, 𝑏) and 𝛿 = (𝑎, 𝑏) + 𝑐 ′ as in Equation (36). The assembly and the split are then Equations (37) and (39)
verbatim, with 𝐷(𝑎,𝑏) acting on the spatial registers alone:
𝜒

𝐊2𝐷,el =

𝐸1 +𝐸2
𝐸 −𝐸 ∑
𝑅(𝑎,𝑏) 𝐓(𝑎,𝑏) .
𝐊2𝐷,el − 1 2
2
2
(𝑎,𝑏)∈

(42)

∑
The two properties that carried Section 6 now read differently. The merge still holds, (𝑎,𝑏) 𝐓(𝑎,𝑏) = 𝐊2𝐷,el , the
17 terms of Proposition 1. But each 𝐓(𝑎,𝑏) now carries ten terms rather than four, distributed 2, 3, 3, 2 over its four
offsets: the offset at the node itself and the diagonal offset carry {𝐼, 𝑋}, while the two axis offsets carry {𝐼, 𝑍, 𝑖𝑌 }.
The reflection family therefore holds 40 terms.
The 𝑖𝑌 component is absent from the merged family and present in the reflection family, and the reason is structural.
Merging restores the symmetry 𝐊𝑥𝑦 = 𝐊𝑦𝑥 on which the three-component rewriting of Equation (20) depends; with
a variable modulus each element is weighted separately, the shear block loses that symmetry, and 𝑖𝑌 carries the
antisymmetric remainder. Its total weight is
∑ ∑|
| |1 − 3𝜈|
,
|[𝐓(𝑎,𝑏) ]𝑖𝑌 | =
|
|
1 − 𝜈2

(43)

(𝑎,𝑏) 𝛿

so the eight 𝑖𝑌 terms vanish at 𝜈 = 1∕3 and nowhere else.
Proposition 3. Equation (42) is an exact LCU of the two-phase periodic plane-stress 𝑄4 operator in which every
unitary is a cyclic shift pair tensored with a single-qubit 𝜎𝑟 ∈ {𝐼, 𝑍, 𝑋, 𝑖𝑌 }, optionally preceded by one material
reflection. For every 𝐸1 ≠ 𝐸2 , every 𝜒, every 𝜈 ∈ (−1, 12 ) and every 𝑁 = 2𝑚 with 𝑚 ≥ 2,
𝐿 = 17 + 40 = 57,

𝐿 = 49 at 𝜈 = 1∕3,

K. Suresh: Preprint submitted to Elsevier

(44)
Page 11 of 22

## PDF page 12

Block encodings for periodic two-phase finite element operators

and the subnormalization is
𝜒

𝛼2D,el = min(𝐸1 , 𝐸2 ) 𝐴(𝜈) + |𝐸1 − 𝐸2 | 𝐵(𝜈),

(45)

with 𝐴(𝜈) = 𝛼2𝐷,el of Equation (22) at 𝐸 = 1 and
𝐵(𝜈) =

69 + 5𝜈 + 6 |1 − 3𝜈|
.
12 (1 − 𝜈 2 )

(46)

At 𝐸1 = 𝐸2 the second family vanishes and 𝐿 collapses to 17.
Proof. The counting is that of Proposition 2 with ten terms per element in place of four, and the eight 𝑖𝑌 terms carry
total weight |1 − 3𝜈|∕(1 − 𝜈 2 ) by Equation (43), vanishing at 𝜈 = 1∕3 and nowhere else, which is the drop to 49.
∑
For the subnormalization, summing magnitudes in Equation (42) gives 21 (𝐸1 +𝐸2 )𝐴 + 12 |𝐸1 −𝐸2 | (𝑎,𝑏) ‖𝐓(𝑎,𝑏) ‖, and
(
)
∑
writing 12 (𝐸1 +𝐸2 ) = min(𝐸1 , 𝐸2 ) + 21 |𝐸1 −𝐸2 | collects the two into Equation (45) with 𝐵 = 𝐴 + (𝑎,𝑏) ‖𝐓(𝑎,𝑏) ‖ ∕2.
Evaluating that sum on the plane-stress element gives Equation (46), whose absolute-value term is half the 𝑖𝑌 weight
of Equation (43).
Written out, Equation (45) reads
[
1
𝜒
1
𝛼2D,el =
(𝐸1 +𝐸2 )(33+𝜈)
2
6 (1 − 𝜈 ) 2
(
)]
+ |𝐸1 −𝐸2 | 18 + 2𝜈 + 3|1−3𝜈| .

(47)

As in the scalar cell, the reflections are present at every contrast, so 𝐿 = 57 and the circuit are fixed and only the
moduli move, against an exact Pauli expansion of 159,338,497 terms at 𝑚 = 12 for the microstructure of Figure 1
(Section 2.2).

8. The Block-Encoding Circuit
8.1. Registers
The system register carries 2𝑚 + ⌈log2 𝑛𝑑 ⌉ qubits (𝑛𝑑 = 1 for Poisson and 𝑛𝑑 = 2 for elasticity), ordered as 𝑥, 𝑦,
then the dof qubit. The ancilla carries one shift-control qubit 𝑠, the 𝑚 − 1 clean carry ancillas 𝑎 of the incrementer and
finally, the PREP register of 𝑛prep qubits. Table 4 collects the resulting cost in closed form.
Only two entries depend on the mesh: the system register, at 2𝑚 + ⌈log2 𝑛𝑑 ⌉ qubits, and the 𝑚 − 1 carry ancillas,
which are returned to |0⟩ and reused by every shift. Everything the decomposition controls is constant in 𝑚: the term
count, the PREP width, and the coefficients themselves. The Toffoli count is affine in 𝑚 at a slope of 8 per shifted
register, which is the four controlled shifts of a homogeneous cell and the eight of a two-phase cell at 2𝑚 − 2 Toffoli
each.

8.2. The Cyclic Shift
The shift is the controlled ripple-carry cyclic increment of Section 3.1, drawn in Figure 3: 2𝑚 − 2 Toffoli, 𝑚 CNOT
and 𝑚 − 1 clean ancillas, transpiling to 11𝑚 − 10 two-qubit gates.

8.3. PREP
Two different preparations are used,
∑√
𝖯𝐿 |0⟩ =
|𝑐𝑘 |∕𝛼 |𝑘⟩,
𝑘

𝖯𝑅 |0⟩ =

∑

√
sgn(𝑐𝑘 ) |𝑐𝑘 |∕𝛼 |𝑘⟩,

(48)

𝑘

so that
(
)
(
)
 = 𝖯†𝑅 ⊗ 𝐼 ⋅ SEL ⋅ 𝖯𝐿 ⊗ 𝐼

(49)

K. Suresh: Preprint submitted to Elsevier

Page 12 of 22

## PDF page 13

Block encodings for periodic two-phase finite element operators
Table 4
Cost of the five encodings as a function of 𝑚, exact at every 𝑚 ≥ 2 and verified against measurement at every 𝑚 from 2 to
12. A superscript 𝜒 marks a two-phase cell. 𝐿 is the number of LCU terms, the four middle columns are qubit counts, and
the last is a gate count. Every cell also carries one shift control qubit, included in the total; it and the 𝑚 − 1 carry ancillas
are clean and shared by every shift in the circuit, so both are counted once. 𝑛prep can exceed ⌈log2 𝐿⌉ because the index is
factored; see Section 8.3. The Toffoli count is taken before transpilation; for the transpiled two-qubit count see Figure 4.
qubits

Toffoli

cell

𝐿 system

carry prep

1D Poisson
2D Poisson
2D Poisson𝜒
2D elasticity
2D elasticity𝜒

3
9
25
17
57

𝑚−1
𝑚−1
𝑚−1
𝑚−1
𝑚−1

𝑚
2𝑚
2𝑚
2𝑚 + 1
2𝑚 + 1

total

gates

2 2𝑚 + 2
4𝑚
4 3𝑚 + 4
8𝑚
7 3𝑚 + 7 16𝑚 − 7
6 3𝑚 + 7 8𝑚 + 4
9 3𝑚 + 10 16𝑚 − 1

∑
has top-left block 𝑘 𝑐𝑘 𝑈𝑘 ∕𝛼 = 𝐊∕𝛼 and no signs appear inside SELECT.
A standard dense PREP uses ⌈log2 𝐿⌉ qubits. SELECT must then apply each 𝑈𝑘 controlled on all 𝑛prep qubits, which
requires 𝐿 controlled blocks and (𝐿) Toffoli gates [9]. Every unitary in Equations (21), (39) and (42) is, however,
a tensor product with one factor per register: a shift on 𝑥, a shift on 𝑦, a Pauli 𝜎𝑟 on the dof register, and at most one
reflection 𝑅(𝑎,𝑏) . Each factor is drawn from a small fixed set, three shifts per spatial register and four Pauli operators, so
the terms are the combinations of those sets while the operations the circuit has to realize are their union. We therefore
use a factored encoding of the index [23], in which SELECT applies one multiplexer per register and the choice made
on one register is independent of the choice made on the others; for a Pauli LCU, factored encoding over qubits is
standard. Consequently, SELECT cost is independent of 𝐿; the Poisson operators at 𝐿 = 5 (FD) and 𝐿 = 9 (FE)
compile to identical SELECT circuits. The small price to pay is a wider PREP register. The index 𝑘 is the concatenation
of one field per factor: two bits for each shift exponent, two bits for 𝜎𝑟 , and, for a two-phase operator, three one-bit
fields for the reflection: a flag 𝑔 that applies 𝑅𝜒 , and bits 𝑎 and 𝑏 that select the offset in Equation (33). Unused codes
receive zero amplitude. The register grows from ⌈log2 𝐿⌉ = 4, 5, 5, 6 to 𝑛prep = 4, 7, 6, 9 for the four cells (Table 4).

8.4. SELECT
SELECT applies one controlled operation for each value of each PREP field. The stages, in circuit order, are (see
Appendix A):

1. Spatial: on each of 𝑥 and 𝑦, a controlled increment 𝑆𝑐 and a controlled decrement 𝑆𝑐† , four controlled shifts in
all.
2. Dof: a controlled 𝑍 and 𝑋, and in the two-phase elasticity cell a controlled 𝑖𝑌 , implemented as 𝑅𝑦 (−𝜋). This
stage is absent in the scalar cells.
3. Reflection: in the two-phase cells, decrements on 𝑥 and 𝑦 controlled on 𝑎 and 𝑏, 𝑅𝜒 controlled on 𝑔, and the
matching increments. This is 𝑅(𝑎,𝑏) of Equation (33), and adds four controlled shifts and one oracle query.
SELECT therefore contains four controlled shifts in a homogeneous cell and eight in a two-phase cell, at most three
controlled single-qubit gates, and at most one oracle query, for every 𝐿. Each controlled shift costs 2𝑚 − 2 Toffoli
and each two-bit stage adds two, which gives the Toffoli counts of Table 4. Since SELECT does not depend on 𝐿, each
elasticity circuit exceeds its scalar counterpart by a constant number of gates.
Finally, every field is at most two bits wide, so each control line is computed by one Toffoli, and no gate in the four
circuits has more than two controls. This matters for the following reason.
In Qiskit 2.4.2 [42], the transpiler synthesizes a multi-controlled 𝑋 with four or more controls using idle circuit
qubits as clean ancillas, since a Qiskit circuit assumes every qubit starts in |0⟩. A block encoding must act correctly
on an arbitrary system state, so the transpiled circuit applies a different operator. The circuits here avoid this: the
factored index of Section 8.3 limits every gate to two controls, and we synthesize every multi-controlled gate explicitly.
Appendix A draws all four encodings as built.

K. Suresh: Preprint submitted to Elsevier

Page 13 of 22

## PDF page 14

Block encodings for periodic two-phase finite element operators
Table 5
Cost of the two preparations at 𝑚 = 12, against the whole circuit. Slots is 2𝑛prep , the addressable indices; 𝐿 of them carry
amplitude and the rest are prepared at zero.
cell
2D scalar, homog.
2D scalar, 2-phase
2D elast., homog.
2D elast., 2-phase

𝑛prep
4
7
6
9

slots

rot.

prep CX

share

16
9
29
128 25
253
64 17
125
512 57 1021

22
240
114
1004

4%
18%
16%
46%

𝐿

Table 6
The two factors of Equation (50) at 𝑚 = 5, 𝜈 = 0.3, 𝐸1 ∕𝐸2 = 3. The LCU slack is independent of 𝑚 in all four cells;
the norm gap is independent of 𝑚 only in the homogeneous cells. 𝑝succ is the post-selection probability on the maximizing
singular vector.
cell
2D scalar, homog.
2D scalar, 2-phase
2D elast., homog.
2D elast., 2-phase

LCU slack norm gap 𝛼∕‖𝐊‖2
1.0000
1.0000
1.1935
1.2473

1.3333
1.3485
1.1625
1.1778

1.3333
1.3485
1.3875
1.4691

𝑝succ
0.563
0.550
0.519
0.463

8.5. Circuit Cost
Section 2.1 noted that the arbitrary-angle rotations of PREP dominate the fault-tolerant cost, each costing
(log 1∕𝜀syn ) 𝑇 gates while everything else is Clifford and Toffoli. Table 5 splits the two-qubit count accordingly:
PREP is constant in 𝑚 and SELECT grows.
Figure 4 gives the transpiled two-qubit count from 𝑚 = 2 to 12; the slopes are 48 gates per qubit of resolution in the
homogeneous cells and 96 in the two-phase cells. The homogeneous elasticity circuit costs a constant more than the
homogeneous scalar one. The intercepts are 25 and 143 in the homogeneous cells and 209 and 1012 in the two-phase
cells.

8.6. Tightness
The ratio 𝛼∕‖𝐊‖2 factors as
‖𝐊‖∞
𝛼
𝛼
×
.
=
‖𝐊‖2
‖𝐊‖∞
‖𝐊‖2
⏟⏟⏟ ⏟⏟⏟
LCU slack

(50)

norm gap

Table 6 evaluates both factors. Both scalar cells have an LCU slack of 1 here: the four element contributions at a
node share a sign, so 𝛼 = ‖𝐊‖∞ whenever some node lies entirely in the stiffer phase, as shown in Section 6; for a
microstructure with no such node, the checkerboard of that section for instance, the slack exceeds 1. The elasticity
cells have a slack above 1 at every microstructure because contributions of opposite sign cancel (Section 7). For
homogeneous elasticity, 𝛼∕‖𝐊‖2 = 1.1935 × 1.1625 = 1.3875 at every 𝑚; in the two-phase cells the norm gap,
and with it the product, decreases as 𝑚 increases.

K. Suresh: Preprint submitted to Elsevier

Page 14 of 22

## PDF page 15

Block encodings for periodic two-phase finite element operators

x0
x1
x2
x3
s
a0
a1
a2
Figure 3: The controlled cyclic increment at 𝑚 = 4, the only primitive whose cost grows with the mesh.

2250

2D scalar, homogeneous
2D elasticity, homogeneous
2D scalar, two-phase
2D elasticity, two-phase

2000
two-qubit gates

1750
1500
1250
1000
750
500
250
2

4

6
8
m, qubits per direction

10

12

Figure 4: Two-qubit gate count against 𝑚 for the four 2D cells, measured rather than fitted, for the circuit transpiled to
{CX, 𝑈 } at optimization level 2 (Qiskit 2.4.2).

K. Suresh: Preprint submitted to Elsevier

Page 15 of 22

## PDF page 16

Block encodings for periodic two-phase finite element operators

9. Implementation
This work is implemented in PyBlockEncode, an open-source Python library built on Qiskit 2.4.2 [42] and available
at https://github.com/UW-ERSL/PyBlockEncode; the importable module is pyblockencode. The supported
operators are
• POISSON1D()
• POISSON2D(’fd’)
• POISSON2D(’fe’)
• ELASTICITY2D(nu, E)
• POISSON2D_2PHASE(vf, E1, E2)
• ELASTICITY2D_2PHASE(nu, vf, E1, E2)
The size is given either as 𝑁, the grid points per direction, or as 𝑚 = log2 𝑁 qubits per direction; the encoded
operator carries 𝑁, 𝑁 2 or 2𝑁 2 rows according to the cell. Listing 1 encodes the homogeneous elasticity cell at 𝑚 = 12.
Listing 1: The homogeneous elasticity cell at 𝑚 = 12.
from pyblockencode import blockencode, ELASTICITY2D
cell = ELASTICITY2D(nu=0.3)
qc, info = blockencode(cell, N=4096)
print(f"operator = {info.kind}")
print(f"dofs = {info.dofs:,} L = {info.L}")
print(f"alpha = {info.alpha:.4f}")
print(f"qubits = {info.qubits}")
print(f"Toffoli = {info.toffoli} CX = {info.cx}")
----- output -------------------------------operator = elasticity2d
dofs = 33,554,432 L = 17
alpha = 6.0989
qubits = 43
Toffoli = 100 CX = 719

The two-phase operators place a centered square inclusion of volume fraction vf; every result reported here uses
𝑣𝑓 = 1∕4, for which the oracle is Equation (30). Listing 2 encodes the two-phase elasticity cell at 𝑚 = 12.
Listing 2: The two-phase elasticity cell at 𝑚 = 12.
from pyblockencode import blockencode, ELASTICITY2D_2PHASE
cell = ELASTICITY2D_2PHASE(nu=0.3, vf=0.25, E1=3, E2=1)
qc, info = blockencode(cell, N=4096)
print(f"operator = {info.kind}")
print(f"dofs = {info.dofs:,} L = {info.L}")
print(f"alpha = {info.alpha:.4f}")
print(f"qubits = {info.qubits}")
print(f"Toffoli = {info.toffoli} CX = {info.cx}")
----- output -------------------------------operator = elasticity2d_2phase
dofs = 33,554,432 L = 57
alpha = 19.1209
qubits = 46
Toffoli = 191 CX = 2164

10. Conclusions
In this paper, we presented exact block encodings for 2D homogeneous elasticity, two-phase 2D Poisson, and twophase 2D elasticity operators on periodic finite element grids, built on shift decomposition and a material reflection
oracle. For homogeneous 2D elasticity at 𝑚 = 12 qubits per direction (33.6 million degrees of freedom), the LCU has
17 terms, against 18.9 million for the Pauli expansion.
K. Suresh: Preprint submitted to Elsevier

Page 16 of 22

## PDF page 17

Block encodings for periodic two-phase finite element operators

Two-phase microstructures enter through one material reflection oracle conjugated by the four node-to-element
shifts. The resulting LCUs have 𝐿 = 25 terms for scalar Poisson and 𝐿 = 57 for elasticity (49 at 𝜈 = 1∕3), independent
of the grid resolution 𝑁, the volume fraction 𝑣𝑓 , and the contrast 𝑟 = 𝐸1 ∕𝐸2 ; the subnormalizations are closed forms in
the two moduli, independent of 𝑁 and 𝑣𝑓 . The formulation is restricted to regular grids, periodic boundary conditions,
and isotropic phases.
The periodic cell is the setting of computational homogenization that this paper targets. Non-periodic boundaries
and unstructured meshes require additional de-periodization and mapping [17], which are not treated here.
Several extensions follow the same construction: (1) Arbitrary microstructures require only a different 𝑅𝜒 , since
neither 𝐿 nor 𝛼 𝜒 depends on 𝜒, so the open cost is the oracle itself: four CNOT and one controlled 𝑍 for a predicate
with a closed form, and a table lookup for one without. (2) A functionally graded phase replaces the binary indicator
with a discretized modulus, which the same split encodes as one reflection per bit plane, so 𝐿 grows with the bit depth
rather than with the number of distinct moduli. (3) The decomposition applies unchanged to any translation-invariant
finite element operator on a regular periodic grid, including the mass, convection-diffusion and Helmholtz operators,
for which only the element matrix and hence the coefficients change. (4) Extending the work from 2D to 3D leave the
node-to-element map and the reflection unchanged, with eight incident elements in place of four, and the scalar cell
follows with new constants and no new argument, while the vector cell requires padding the 3 × 3 nodal blocks into a
two-qubit dof register, which is where the additional terms and subnormalization arise [29]. (5) A more efficient PREP
[43] may be desirable, especially in 3D.
Two directions lie outside the present formulation. Nonlinear elasticity re-encodes, at every Newton step, a tangent
operator whose element moduli vary with the current state; whether the oracle can be updated rather than rebuilt
at each iteration is open. Finally, the end-to-end cost of a QSVT-based solve [4] remains to be quantified, and the
subnormalizations reported here need to be quantified.

Acknowledgments
The author acknowledges the Vilas Associate Grant from the University of Wisconsin Graduate School.

Declarations
The author declares no conflict of interest.

Code availability
The code developed in this work is available at https://github.com/UW-ERSL/PyBlockEncode.

Use of AI Tools
The author used generative AI assistants, specifically, Claude (Anthropic) and Gemini (Google) during the
preparation of this manuscript. The tools were used for code development and drafting of text. All content was reviewed,
verified, and edited by the author, who takes full responsibility for the accuracy and integrity of the work.

A. The Four Circuits
Figures A.1 to A.4 give the four encodings at 𝑚 = 2, with only the two preparations boxed and every other gate
drawn as built. The gaps marked reindex are where the shift-control qubit 𝑠 is cleared, the PREP index is recoded for
the next term, and 𝑠 is set again.

K. Suresh: Preprint submitted to Elsevier

Page 17 of 22

## PDF page 18

Block encodings for periodic two-phase finite element operators

x0
x1
y0
y1
s
a
p0 0
p1 1P
p2 2
p3 3

Sx

Sx

reindex

Sy

reindex

X
X

Sy

reindex

reindex

X

0

X

1

L

X
X

X

X

2

PR

3

Figure A.1: Scalar homogeneous cell at 𝑚 = 2, 𝐿 = 9, 𝛼 = 16∕3, on 3𝑚 + 4 = 10 qubits. The four bracketed stages 𝑆𝑥 , 𝑆𝑥† ,
𝑆𝑦 , 𝑆𝑦† are the two multiplexers of Section 8.4, one per spatial register. Within each, the Toffoli before and after computes
and uncomputes the select control from a two-bit field, and the 𝑋 gates around it choose which value of that field the
shift controls.

x0
x1
y0
y1
s
a
p0 0
p1 1P
p2 2
p3 3

Sx

Sx

reindex

Sy

reindex

X
X

Sy

reindex

reindex

X

0

X

1

L

X
X

X

X

2

PR

3

Figure A.2: Scalar two-phase cell at 𝑚 = 2, 𝐿 = 25, 𝛼 = 16 at 𝐸1 ∕𝐸2 = 3, on 3𝑚+7 = 13 qubits. The first half is Figure A.1;
†
the three brackets 𝑆𝑎𝑏 , 𝑅𝜒 , 𝑆𝑎𝑏
at the right are the conjugation of Equation (33) read right to left, a conditional shift on
each spatial register, the oracle controlled on 𝑔, and the shifts undone.

K. Suresh: Preprint submitted to Elsevier

Page 18 of 22

## PDF page 19

Block encodings for periodic two-phase finite element operators

x0
x1
y0
y1
d
s
a
p0 0
p1 1
p2 2P
p3 3
p4 4
p5 5

Sx

Sx

reindex

X
X

X

X

L

x0
x1
y0
y1
d
s
a
p0
p1
p2
p3
p4
p5

Sy

reindex

X

Sy

reindex

reindex

Z

reindex

X

reindex

0
1
X

X

2

X

3
X
X

X

X

PR

4
5

Figure A.3: Elasticity homogeneous cell at 𝑚 = 2, 𝐿 = 17, 𝛼 = 6.099 at 𝜈 = 0.3, on 3𝑚 + 7 = 13 qubits.

K. Suresh: Preprint submitted to Elsevier

Page 19 of 22

## PDF page 20

Block encodings for periodic two-phase finite element operators

x0
x1
y0
y1
d
s
a
p0 0
p1 1
p2 2
p3 3
p4 4P
p5 5
p6 6
p7 7
p8 8

Sx

Sx

reindex

Sy

reindex

X
X

Sy

reindex

reindex

Z

X

X
X
X

X

X

L

x0
x1
y0
y1
d
s
a
p0
p1
p2
p3
p4
p5
p6
p7
p8

X

reindex

X

reindex

reindex

iY

Sab

Sab

R

H

H

RY

0
1
2
3
X

X

X

4PR
5
6
7
8

Figure A.4: Elasticity two-phase cell at 𝑚 = 2, 𝐿 = 57, 𝛼 = 19.121 at 𝜈 = 0.3 and 𝐸1 ∕𝐸2 = 3, on 3𝑚 + 10 = 16 qubits.
Every stage of the construction appears: the four spatial multiplexers, the dof multiplexer 𝑍, 𝑋, 𝑖𝑌 , and the reflection
†
stage, whose three brackets 𝑆𝑎𝑏 , 𝑅𝜒 , 𝑆𝑎𝑏
are the conjugation of Equation (33) read right to left.

K. Suresh: Preprint submitted to Elsevier

Page 20 of 22

## PDF page 21

Block encodings for periodic two-phase finite element operators

CRediT authorship contribution statement
Krishnan Suresh: Conceptualization, Methodology, Software, Validation, Writing – original draft.

References
[1] Aram W Harrow, Avinatan Hassidim, and Seth Lloyd. Quantum algorithm for linear systems of equations. Physical review letters,
103(15):150502, 2009.
[2] Andrew M Childs, Robin Kothari, and Rolando D Somma. Quantum algorithm for systems of linear equations with exponentially improved
dependence on precision. SIAM Journal on Computing, 46(6):1920–1950, 2017.
[3] Pedro CS Costa, Dong An, Yuval R Sanders, Yuan Su, Ryan Babbush, and Dominic W Berry. Optimal scaling quantum linear-systems solver
via discrete adiabatic theorem. PRX Quantum, 3(4):040303, 2022.
[4] András Gilyén, Yuan Su, Guang Hao Low, and Isaac L Chuang. Quantum singular value transformation and beyond: exponential improvements
for quantum matrix arithmetics. In Proceedings of the 51st Annual ACM SIGACT Symposium on Theory of Computing (STOC), pages 193–204,
2019. arXiv:1806.01838.
[5] Dominic W Berry, Andrew M Childs, Richard Cleve, Robin Kothari, and Rolando D Somma. Simulating Hamiltonian dynamics with a
truncated taylor series. Physical review letters, 114(9):090502, 2015.
[6] Daan Camps and Roel Van Beeumen. FABLE: Fast approximate quantum circuits for block-encodings. 2022 IEEE International Conference
on Quantum Computing and Engineering (QCE), pages 104–113, 2022. arXiv:2205.00081.
[7] Parker Kuklinski, Benjamin Rempfer, Justin Elenewski, and Kevin Obenland.
Efficient block-encodings require structure, 2025.
arXiv:2509.19667.
[8] Andrew M Childs and Nathan Wiebe. Hamiltonian simulation using linear combinations of unitary operations. Quantum Information &
Computation, 12(11-12):901–924, 2012.
[9] Ryan Babbush, Craig Gidney, Dominic W Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, and Hartmut Neven.
Encoding electronic spectra in quantum circuits with linear T complexity. Physical Review X, 8(4):041015, 2018.
[10] Krishnan Suresh. Applied Quantum Computing for Engineers: Linear Solvers and Optimization. Independently published, first edition, 2026.
ISBN-13: 979-8244366846.
[11] Lukas Hantzko, Lennart Binkowski, and Sabhyata Gupta. Tensorized Pauli decomposition algorithm. Physica Scripta, 99(8):085128, 2024.
[12] Océane Koska, Marc Baboulin, and Arnaud Gazda. A tree-approach Pauli decomposition algorithm with application to quantum computing.
In ISC High Performance 2024 Research Paper Proceedings (39th International Conference), pages 1–11. Prometeus GmbH, 2024.
[13] Rocco Monteiro Nunes Pesce and Paul D Stevenson. H2ZIXY: Pauli spin matrix decomposition of real symmetric matrices. arXiv preprint
arXiv:2111.00627, 2021.
[14] Timothy N. Georges, Bjorn K. Berntson, Christoph Sünderhauf, and Aleksei V. Ivanov. Pauli decomposition via the fast Walsh–Hadamard
transform. New Journal of Physics, 27(3):033004, 2025.
[15] Chao Lu, Muralikrishnan Gopalakrishnan Meena, Eduardo Antonio Coello Perez, Kalyana Chakravarthi Gottiparthi, and Seongmin Kim.
Memory-, circuit-, and ansatz-efficient vqls for cfd on hybrid quantum-hpc systems. arXiv preprint arXiv:2608.09661, 2026.
[16] Yongchun Xu and Heng Hu. Decomposition-free variational quantum linear solver: Application in computational mechanics. Computer
Methods in Applied Mechanics and Engineering, 447:118396, 2025.
[17] Tyler Kharazi, Ahmad M Alkadri, Jin-Peng Liu, Kranthi K Mandadapu, and K Birgitta Whaley. Explicit block encodings of boundary value
problems for many-body elliptic operators. Quantum, 9:1764, 2025.
[18] Andreas Sturm and Niclas Schillo. Efficient and explicit block encoding of finite difference discretizations of the Laplacian. ACM Transactions
on Quantum Computing, 2025.
[19] Ahmad M Alkadri, Tyler D Kharazi, K Birgitta Whaley, and Kranthi K Mandadapu. A quantum algorithm for the finite element method.
arXiv preprint arXiv:2510.18150, 2025.
[20] Thomas Hogancamp, Reuben Demirdjian, and Daniel Gunlycke. Linear-combination-of-unitaries decomposition for the Laplace operator.
Physical Review A, 114(1):012455, 2026.
[21] Hai-Ling Liu, Yu-Sen Wu, Lin-Chun Wan, Shi-Jie Pan, Su-Juan Qin, Fei Gao, and Qiao-Yan Wen. Variational quantum algorithm for the
Poisson equation. Physical Review A, 104(2):022418, 2021.
[22] Abeynaya Gnanasekaran and Amit Surana. Efficient quantum access model for sparse structured matrices using linear combination of “things”.
Physical Review A, 113(2):022437, 2026.
[23] Daan Camps, Lin Lin, Roel Van Beeumen, and Chao Yang. Explicit quantum circuits for block encodings of certain sparse matrices. SIAM
Journal on Matrix Analysis and Applications, 45(1):801–827, 2024. arXiv:2203.10236.
[24] Christoph Sünderhauf, Earl Campbell, and Joan Camps. Block-encoding structured matrices for data input in quantum computing. Quantum,
8:1226, 2024. arXiv:2302.10949.
[25] Sven Danz, Tobias Stollenwerk, and Alessandro Ciani. An implementation of quantum oracles for the finite element method. SIAM Journal
on Scientific Computing, 48(3):B386–B419, June 2026.
[26] Abhishek Arora, Benjamin M Ward, and Caglar Oskay. An implementation of the finite element method in hybrid classical/quantum computers.
Finite Elements in Analysis and Design, 248:104354, 2025.
[27] Leonhard Hölscher, Oliver Ahrend, Lukas Karch, Carlotta L’Estocq, Marc Marfany Andreu, Tobias Stollenwerk, Frank K Wilhelm, and Julia
Kowalski. End-to-end quantum algorithm for topology optimization in structural mechanics. Quantum Science and Technology, 11(2):025029,
2026.
[28] Matthias Deiml and Daniel Peterseim. Quantum realization of the finite element method. arXiv preprint arXiv:2403.19512, 2024.

K. Suresh: Preprint submitted to Elsevier

Page 21 of 22

## PDF page 22

Block encodings for periodic two-phase finite element operators
[29] Austin Pechan, John Golden, and Daniel O’Malley. Block encoding of the three-dimensional heterogeneous Poisson equation with application
to fracture flow. Physical Review Applied, 25(4):044038, 2026.
[30] Hiroshi Yano and Yuki Sato. Quantum framework for parameterizing partial differential equations via diagonal block-encoding. arXiv preprint
arXiv:2603.01358, 2026.
[31] Jishnu Mahmud and Rebekah Herrman. Moment-structured block encodings of periodic finite-difference operators. arXiv preprint
arXiv:2607.11596, 2026.
[32] Thomas G Draper. Addition on a quantum computer. arXiv preprint quant-ph/0008033, 2000.
[33] Craig Gidney. Halving the cost of quantum addition. Quantum, 2:74, 2018.
[34] Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, and David Petrie Moulton. A new quantum ripple-carry addition circuit. arXiv
preprint quant-ph/0410184, 2004.
[35] Michel O Deville, Paul F Fischer, and Ernest H Mund. High-order methods for incompressible fluid flow, volume 1. Cambridge university
press Cambridge, 2002.
[36] Charles F Van Loan. The ubiquitous Kronecker product. Journal of computational and applied mathematics, 123(1-2):85–100, 2000.
[37] Olgierd Cecil Zienkiewicz, Robert Leroy Taylor, and Jian Z Zhu. The finite element method: its basis and fundamentals. Elsevier, 2013.
[38] Felix Givois, Matthias Kabel, and Nicolas Gauger. QFT-based homogenization. arXiv preprint arXiv:2207.12949, 2022.
[39] Burigede Liu, Michael Ortiz, and Fehmi Cirak. Towards quantum computational mechanics. Computer Methods in Applied Mechanics and
Engineering, 432:117403, 2024.
[40] Yiren Wang, Michael Ortiz, and Fehmi Cirak. QAFE2: Quantum accelerated multiscale finite element analysis. Computer Methods in Applied
Mechanics and Engineering, 461:119204, 2026.
[41] Loïc Balazi, Matthias Deiml, and Daniel Peterseim. Quantum enhanced numerical homogenization. arXiv preprint arXiv:2603.28521, 2026.
[42] Ali Javadi-Abhari, Matthew Treinish, Kevin Krsulich, Christopher J Wood, Jake Lishman, Julien Gacon, Simon Martiel, Paul D Nation, Lev S
Bishop, Andrew W Cross, et al. Quantum computing with qiskit. arXiv preprint arXiv:2405.08810, 2024.
[43] Krishnan Suresh and Sanjay Suresh. Pyencode: an open-source library for structured quantum state preparation. Quantum Science and
Technology, 2026.

K. Suresh: Preprint submitted to Elsevier

Page 22 of 22
