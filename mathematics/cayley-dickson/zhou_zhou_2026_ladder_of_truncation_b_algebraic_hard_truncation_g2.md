Source: https://zenodo.org/records/23151835/files/The%20Ladder%20of%20Truncation%20B;%20The%20Paradigm%20of%20Algebraic%20Hard%20Truncation---From%20Hurwitz's%20Theorem%20to%20texorpdfstring%7B$G_2$%7D%7BG2%7D%20Rigid%20Anchoring.pdf
PDF sha256: ebb98f5bbb92314c4ff63d9d28a2ec3a9e17c1c0ae0c8134cea671caa04251a0
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of zhou_zhou_2026_ladder_of_truncation_b_algebraic_hard_truncation_g2.pdf

Transcription of `zhou_zhou_2026_ladder_of_truncation_b_algebraic_hard_truncation_g2.pdf` in this directory, 44 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-44 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

The Ladder of Truncation B: The Paradigm of
Algebraic Hard Truncation—From Hurwitz’s Theorem
to G2 Rigid Anchoring
Zhou Changzheng, Zhou Ziqing
Email: ziqing-zhou@outlook.com
October 5, 2026
Abstract
This paper starts from the termination condition of the Cayley–Dickson ladder
and elevates algebraic hard truncation from a classification fact to a diagnosable
structural event. Under norm-weighted constraint-network encoding, the injection
gap is defined as the square of the minimum singular value of all left-multiplication
operators on the unit sphere, and it is proved that on the four division levels of
the real numbers, complex numbers, quaternions, and octonions the injection gap
is identically equal to the theoretical maximum, while upon entering the sedenion
level it jumps to zero. The Hurwitz classification excludes finite-dimensional real
normed division algebras between dimension eight and any successor; hence this
jump is not the endpoint of an asymptotic process but a discontinuous transition in
the sense of value range. It is further proved that the complete residual of symmetry at the truncation point is the fourteen-dimensional exceptional Lie group G2 .
The geometry of the debris is recorded by two spaces that must be distinguished:
the zero-divisor carrier space (the totality of failing elements) is diffeomorphic to
the Stiefel manifold V2 (R7 ), of dimension eleven; the normalized annihilating-pair
space (the totality of annihilation events) is diffeomorphic to G2 , of dimension
fourteen. The debris of failure, as the totality of annihilation events, is the same
geometric object as the surviving symmetry; its principal-bundle structure gives
the dimension count fourteen equals eleven plus three. The zero divisors at the
sedenion level cause the left-multiplication kernel to have dimension four; a single multiplication can annihilate four linearly independent input directions, and
the information-conservation inequality fails for every finite efficiency parameter.
Internal operations do not raise dimension; the two-sided quotient necessarily destroys divisibility; the endpoint of repair can only be a division level after dimension
reduction. This paper registers three boundaries: the specific numerical value of
the injection gap depends on encoding weights, and the cross-encoding invariant
is the instability mode rather than the numerical value; the dimension-retraction
formula is given only as a conditional corollary; and no isomorphism is claimed
between the present truncation residual and truncation residuals in other domains.

Keywords: truncation; normed division algebras; Hurwitz theorem; zero divisors; G2 ;
spectral gap; information conservation

1

## PDF page 2

1

Introduction

The Cayley–Dickson construction starts from the real numbers and, through the doubling
procedure, successively generates the complex numbers, the quaternions, the octonions,
and the sedenions. Each step is completely legitimate at the symbolic level, and the
construction appears to have no reason to stop. The Hurwitz classification, however,
gives an exact blockade: over the real field, the finite-dimensional unital normed division
algebras are, up to isomorphism, only four in number: the real numbers, the complex
numbers, the quaternions, and the octonions. The sedenions, which the symbolic machine
continues to write after the eighth dimension, are no longer a division algebra; among
them there exist nonzero elements whose product is zero.
This paper adopts a perspective different from the standard reading of the classification theorem: Hurwitz’s theorem is not merely an enumeration of object classes, but also
a coordinate record of a phase-transition event. It marks the exact position on the ladder
where legal extension fails. To support this reading, three questions must be answered.
First, what is the observable signature of truncation at the network level? Second, why
does this signature appear as a jump rather than asymptotically? Third, what remains
after truncation, and why is what remains precisely that?
The answers of this paper are as follows. The signature is the injection gap under
norm-weighted encoding: the four division-algebra levels take the constant value one, and
the sedenion level jumps to zero. The necessity of the jump comes from the discreteness
of the control parameter and from the Hurwitz blockade: between dimension eight and
any successor there exists no normed division algebra, and within the ladder there exists
no intermediate-dimensional object available for continuous interpolation. The complete
answer to the third question requires distinguishing two geometries of the debris: the
geometry of the totality of failing elements is the eleven-dimensional Stiefel manifold
V2 (R7 ), and the geometry of the totality of annihilation events is the fourteen-dimensional
exceptional Lie group G2 ; the two are connected by an SU (2) principal bundle, and the
dimension count fourteen equals eleven plus three closes. The debris of failure, as the
totality of annihilation events, is geometrically exactly the surviving symmetry.
The phase-transition coordinates consist of four elements: the category is the category
of finite-dimensional real normed algebras on the Cayley–Dickson ladder; the control
parameter is the level, whose discreteness is an essential feature of this case rather than
a technical defect; the encoding is norm-weighted constraint-network encoding; the order
parameter is the instability mode of the injection gap along the control parameter, namely
the five-valued structure of four plateaus plus one jump. In these coordinates, the value
range of the injection gap has two elements, and there is no object in the category that
takes an intermediate value. “Not passing through an intermediate state” thus acquires
a precise meaning: it is not that the decay curve is steep, but that there is simply no
intermediate value in the value range.
The honest boundaries of this paper are declared already in the introduction. The
specific numerical value of the injection gap depends on the weight scheme; what is invariant across encodings is the instability mode rather than the numerical value. The
dimension-retraction formula appears only in the status of a conditional corollary; its
constant calibration depends on framework-level information-coupling bookkeeping, and
before that calibration is established it does not constitute a theorem and does not participate in other arguments. This paper does not claim any isomorphism between the
residual of this truncation and truncation residuals in other domains. All numerical as2

## PDF page 3

sertions in this paper are accompanied by explicit machine-checking protocols and can
be verified step by step in exact integer arithmetic.

2

Preliminaries: The Cayley–Dickson Ladder and
the Record of Axiom Loss

2.1

Construction and Norm

Let A be a real algebra with an involution x ↦→ x̄ and a positive definite quadratic norm
N (x) = xx̄. Its double A2 = A × A is equipped with the multiplication
¯ da + bc̄),
(a, b)(c, d) = (ac − db,
the involution
(a, b) = (ā, −b),
and the norm
N ((a, b)) = N (a) + N (b).
Starting from A0 = R, define recursively Ak+1 = A2k . The algebra at level k has dimension
2k and is denoted by Ak . The first five levels are
A0 = R,

A1 = C,

A2 = H,

A3 = O,

A4 = S.

Here S is the sedenion algebra. Write e0 = 1 and let e1 , . . . , en−1 be the imaginary
basis elements; an imaginary element means an element with zero real part. Under the
standard sign convention, e2i = −1 for i ≥ 1, and ei ej = −ej ei for i, j ≥ 1, i ̸= j. In the
doubling process, the basis elements of the second copy are denoted by en+i = ei en , where
n = 2k . The entire multiplication table is determined level by level by integer addition,
subtraction, and multiplication, without floating-point approximation.
Proposition 1 (Recursive well-definedness and norm hierarchy). The above doubling
construction gives a real algebra at each level; the involution is an anti-automorphism;
N (x) = xx̄ is a positive definite quadratic form; and the norm recursion N ((a, b)) =
N (a) + N (b) holds. For k = 1, 2, 3, the norm multiplicativity
N (xy) = N (x)N (y)
holds; for k = 4, norm multiplicativity fails.
Proof sketch. All four terms on the right-hand side of the doubling formula belong to the
lower-level algebra Ak ; hence, after pushing down level by level to A0 = R, the multiplication table is completely determined by integer operations. The involution recursion
(a, b) = (ā, −b) is compatible with the multiplication formula, and a direct computation
gives (xy) = ȳx̄. The norm recursion is given by N ((a, b)) = N (a)+N (b) and is consistent
with N (x) = xx̄ at all levels. Norm multiplicativity for k = 1, 2, 3 belongs to the classical
Hurwitz range; the failure for k = 4 follows directly from the existence of sedenion zero
divisors. If there exist nonzero a, b with ab = 0, then N (ab) = 0 while N (a)N (b) > 0, so
norm multiplicativity cannot hold.
3

## PDF page 4

Boundaries of applicability. First, Proposition 2.1 only records the failure of norm
multiplicativity at k = 4; it does not attribute the failure to errors in the integer implementation. All subsequent algebraic arguments use only the exact multiplication table;
numerical checks are used only to verify structural facts, not to replace proofs. Second,
the division algebras referred to in this paper are by default unital; the Hurwitz classification cited later presupposes the existence of a unit. Outside this category there
exist absolute-valued algebras without a unit (such as twisted complex numbers), which
are outside the scope of this paper, and the “complete residual” conclusion of the third
question does not speak about them.

2.2

Level-by-Level Axiom Profile and Zero-Divisor Structure

The retention and loss of properties at the five levels are shown in the following table.
Core Properties
Retained

Level

Algebra

Dimension

k=0

R

1

Commutativity, associativity, divisibility, norm
multiplicativity, alternativity

k=1

C

2

k=2

H

4

k=3

O

8

Commutativity, associativity, divisibility, norm
multiplicativity, alternativity
Associativity, divisibility, norm multiplicativity,
alternativity
Divisibility, norm multiplicativity, alternativity

k=4

S

16

Power associativity

Core Properties
Lost
None
Natural order (not an
algebraic axiom)
Commutativity
Associativity
Divisibility, norm
multiplicativity,
alternativity; zero
divisors appear

Table 1: Level-by-level axiom profile.

The reading of Table 2.1 requires three qualifications.
doubling
A0 (R)

doubling
A1 (C)

doubling
A2 (H)

doubling
A3 (O)

A4 (S)

Injection gap ∆(WK ) on the unit sphere: division levels ∆ = 1 (plateau), sedenion level ∆ = 0 (catastrophic drop).

Legend: blue boxes = normed division levels (k ≤ 3), red box = first non-division level (k = 4). The
control parameter is the discrete level k, so there is no intermediate object inside the ladder between O
and S.

Figure 1: Cayley–Dickson ladder and the plateau–jump signature of the injection gap.

First, S is still power associative. The subalgebra generated by each element is associative; this is a classical conclusion for quadratic algebras. Therefore this paper does
not list “loss of power associativity” as a fact at the sedenion level. Power associativity
is weaker than associativity and does not restore divisibility.
Second, the subsequent arguments of this paper use only three losses: divisibility,
norm multiplicativity, and alternativity. Divisibility makes the left-multiplication operator invertible for nonzero elements; norm multiplicativity makes the left-multiplication
operator at the division levels an isometry; alternativity guarantees that in the octonion
4

## PDF page 5

level the subalgebra generated by any two elements is still associative, so that the associator does not destroy the structure of the relevant linear equations. The appearance of
zero divisors at the sedenion level makes the left-multiplication operator singular.
Third, the structure of zero divisors is not unconstrained. The following criterion
gives an exact characterization of sedenion left zero divisors.
Proposition 2 (Moreno criterion for sedenion left zero divisors). In A4 = S, a nonzero
element (a, b) is a left zero divisor if and only if a, b are nonzero, equal-norm, orthogonal
imaginary octonions, i.e.
a, b ∈ Im(O) \ {0},

N (a) = N (b),

Re(ab̄) = 0.

Proof sketch. Let x = (a, b) and y = (u, v), where a, b, u, v ∈ O. By the doubling
multiplication,
xy = (au − v̄b, va + bū).
The condition xy = 0 is equivalent to
au = v̄b,

(1)

va = −bū.

(2)

If a = 0 or b = 0, then by the divisibility of O, equations (1) and (2) force u = v = 0, so
a nonzero left zero divisor must have both a, b nonzero.
Taking norms in (1) and using the norm multiplicativity of O gives
N (a)N (u) = N (v)N (b).
Taking norms in (2) gives
N (v)N (a) = N (b)N (u).
Combining the two equations and eliminating the positive quantities N (u), N (v) yields
N (a)2 = N (b)2 , hence N (a) = N (b) > 0.
Substituting (1) into (2) and eliminating v gives an octonion linear equation for u.
Expanding the cross terms using the Moufang identities for octonions shows that this
equation has a nonzero solution if and only if the cross term Re(ab̄) vanishes, i.e. a and
b are orthogonal. Conversely, the equal-norm orthogonality condition directly gives a
nonzero solution. This completes the proof.
Boundaries of applicability. Proposition 2.2 characterizes left zero divisors, i.e. elements x = (a, b) for which there exists a nonzero y with xy = 0. Right zero divisors are
obtained by symmetry under the involution, and their structure is the same as that of
left zero divisors. The zero element is not counted as a zero divisor.
Proposition 3 (Canonical count of standard two-term zero divisors). A standard twoterm zero divisor means that a, b are each a two-term combination of imaginary octonion
basis elements and satisfy the equal-norm orthogonality condition of Proposition 2.2. The
canonical representative family has count 84.
The count proceeds in two steps. The first step is the structural count. The imaginary
part of the octonions has seven basis elements e1 , . . . , e7 . Choose an unordered pair {i, j},
giving
(︃ )︃
7
= 21
2
5

## PDF page 6

choices. For each such pair, the line structure through {i, j} in the Fano plane determines
the constraint on the partner pair; in the sense of canonical representatives, the partner
has 4 support types. Hence the structural count is
21 × 4 = 84.
The second step is the enumeration merge, which takes exhaustive enumeration as authoritative and makes 84 a step-by-step verifiable identity. The complete enumeration is
performed on the fifteen imaginary basis elements of A4 . A two-term imaginary element
has the form ±ei ± ej with 1 ≤ i < j ≤ 15. The number of single elements is
(︃ )︃
15
× 4 = 105 × 4 = 420.
2
The number of ordered pairs is
420 × 420 = 176,400.
On this ordered-pair search space, testing whether the product is zero according to the
exact integer multiplication table gives 1,344 annihilating ordered pairs. The merge
protocol is as follows. A canonical representative of a standard two-term zero divisor is
taken as (x0 , y0 ): x0 = ep +eq+8 , where 1 ≤ p < q ≤ 7; y0 is one of the four partners of this
carrier under the fixed sign convention (the lowest-index component is taken positive),
and its support type is determined by the line structure through {p, q} in the Fano
plane. There are 21 × 4 = 84 canonical representatives. Each canonical representative
generates 16 annihilating ordered pairs: the two components of the carrier change sign
independently (4 ways), the two components of the carrier are interchanged (2 ways, the
partner support-type set unchanged), and the partner changes sign as a whole (2 ways).
The fibers are defined by pairing the unordered support type of the carrier with the
partner support type; they are pairwise disjoint, so
84 × 16 = 1,344
holds exactly, and the fibers exhaust all annihilating ordered pairs. This count agrees
with the structural count of the Moreno criterion and with the enumeration output of
the later machine-check protocol in exact integer arithmetic.
Two counting levels must be distinguished: 176,400 is the unmerged ordered-pair
search space; 1,344 is the total number of annihilating ordered pairs; 84 is the canonical
representative family of the annihilation relation. 84 is not the total number of sedenion
zero divisors. All zero divisors are parametrized by V2 (R7 ) and form√a continuum. The
norm square of a standard two-term zero divisor is 2, so its norm is 2.
Remark 1 (Interface with the later operator encoding). The algebraic properties recorded
in this section enter directly into the later constraint-network encoding. Divisibility is
equivalent to the invertibility of the left-multiplication family La (x) = ax for nonzero a;
norm multiplicativity makes La at the division levels an isometry, so that its minimum
singular value equals ∥a∥; alternativity at the octonion level guarantees that the subalgebra
generated by any two elements is still associative, so that the relevant kernel equations
remain linear; the appearance of zero divisors at the sedenion level makes La singular.
The later definition of the injection gap ∆ depends only on the singular-value structure
of the left-multiplication family, so the three loss records in Table 2.1 constitute all its
algebraic premises.
6

## PDF page 7

3

Constraint Network Encoding and Multiplication
Information Operators

3.1

Encoding Objects, Graph Spectral Quantities, and Operator Spectral Quantities

Let K be the real algebra Ak at level k of the Cayley–Dickson ladder, with dimension
n = 2k and basis elements e0 , e1 , . . . , en−1 , where e0 = 1. The constraint-network encoding
WK is defined as follows: the node set is the set of all basis elements; for every pair of
basis elements ei , ej , if the multiplication table gives a relation ei ej = ±em , then a signed,
target-labeled constraint edge is created recording this multiplication relation; the edge
weight is the norm of the relevant basis elements. In the norm-weighted scheme adopted
in this paper, all basis elements have norm 1, so the edge weight is 1.
The carrying operator of this encoding is the left-multiplication family
La : K → K,

La (x) = ax,

a ∈ K.

The left-multiplication family is a family of real linear operators on K. The constraint
graph itself induces a graph Laplacian matrix LG (WK ), whose second smallest eigenvalue
is called the algebraic connectivity of the graph and is denoted by λ2 (WK ). Algebraic
connectivity is a spectral quantity of the graph’s combinatorial structure: it depends on
nodes, edges, edge weights, edge directions, sign labels, and whether multiple relations
are merged, among other encoding choices.
The subsequent arguments of this paper do not use λ2 (WK ) as a criterion. The
spectral quantity used in this paper is the operator invariant of the left-multiplication
representation family, namely the injection gap ∆(WK ). The two belong to different
levels: λ2 is a spectral quantity of the graph Laplacian, while ∆ is the infimum of the
singular values of the continuous operator family {La } on the unit sphere. In general
the two are not equal. The role of the graph spectral quantity is motivational: it shows
that in constraint-graph encoding, the idea of detecting connectivity, degeneration, or
instability through spectral readings has independent precedent. The proof chain of this
paper depends only on ∆, not on λ2 , and does not claim any equality or equivalence
between the two.

3.2

Definition and Well-Definedness of the Injection Gap

Definition 1 (Injection gap). Let K be a finite-dimensional real algebra equipped with
the positive definite quadratic norm
∥x∥2 = N (x) = xx̄.
For each a ∈ K, define the left-multiplication operator La (x) = ax. Let σmin (La ) denote
the minimum singular value of La with respect to the inner product induced by the above
norm. Define the injection gap as
∆(WK ) = min{σmin (La )2 : a ∈ K, ∥a∥ = 1}.
If the unit sphere of K is compact and σmin (La ) is continuous in a, then the infimum is
attained, so one may write min rather than inf. At every level of the ladder in this paper,
7

## PDF page 8

K is a finite-dimensional real algebra, the unit sphere is compact, La is continuous in a,
and σmin is continuous; hence Definition 3.1 is well-defined.
Equivalently, σmin (La )2 is the smallest eigenvalue of L∗a La , where L∗a is the adjoint of
La with respect to the norm inner product. Hence
∆(WK ) = min{λmin (L∗a La ) : a ∈ K, ∥a∥ = 1}.
If there exists a nonzero a such that La is singular, then taking the normalization a/∥a∥,
the left-multiplication operator remains singular, so ∆(WK ) = 0. If La is invertible for
every nonzero a, then σmin (La ) > 0 for every unit a, so ∆(WK ) > 0.
Definition 3.1 depends only on the singular-value structure of the left-multiplication
operator family. It does not depend on how the edge directions, edge multiplicities, or
sign labels of the constraint graph are organized into an adjacency matrix, nor on the
eigenvalues of the graph Laplacian matrix. The way the norm-weighted scheme enters
the definition is: the unit sphere is given by the norm ∥ · ∥, and the singular values are
given by the inner product induced by the same norm.

3.3

Spectral Reading of Divisibility

Lemma 1 (Divisibility and invertibility of left multiplication). At each level Ak of the
ladder in this paper, the following conditions are equivalent:
(i) Ak is a division algebra;
(ii) for every nonzero a ∈ Ak , the left-multiplication operator La is invertible;
(iii) for every nonzero a ∈ Ak , σmin (La ) > 0.
Moreover, if Ak satisfies norm multiplicativity
N (xy) = N (x)N (y),
then for each a ∈ Ak , La is the composite of the scalar ∥a∥ with an orthogonal operator,
and hence
σmin (La ) = ∥a∥.
In particular, on the unit sphere ∥a∥ = 1, one has σmin (La ) = 1.
Proof. First prove the equivalence of (i) and (ii) at every level of the ladder in this paper.
For A0 through A3 , divisibility holds. Let a ̸= 0. By divisibility, a has a multiplicative
inverse a−1 . These levels are all alternative algebras; in an alternative algebra the inverse
satisfies
a−1 (ax) = x
for all x. Hence La−1 is a left inverse of La . A finite-dimensional linear operator has a left
inverse if and only if it is invertible, so La is invertible. Conversely, if La is invertible for
every nonzero a, then the equation ax = 0 has only the zero solution, so a is not a left
zero divisor. At every level of the ladder in this paper, the absence of left zero divisors
is consistent with divisibility: A0 through A3 are division algebras; A4 = S has nonzero
left zero divisors, hence is not a division algebra. Therefore (i) and (ii) are equivalent.
8

## PDF page 9

The equivalence of (ii) and (iii) is a standard fact for finite-dimensional linear operators: La is invertible if and only if L∗a La is positive definite, if and only if σmin (La ) > 0.
Now prove the singular-value structure under norm multiplicativity. If N (xy) =
N (x)N (y), then for any x,
∥La x∥2 = N (ax) = N (a)N (x) = ∥a∥2 ∥x∥2 .
Hence
∥La x∥ = ∥a∥∥x∥.
When a ̸= 0, the operator La /∥a∥ preserves the norm, hence is orthogonal. Thus La =
∥a∥Ua , where Ua is an orthogonal operator. All singular values of an orthogonal operator
are equal to 1, so all singular values of La are equal to ∥a∥. In particular, σmin (La ) = ∥a∥.
Taking ∥a∥ = 1 gives σmin (La ) = 1. This completes the proof.
Proposition 4 (Injection-gap readings for the two types of levels). Under the normweighted encoding:
(1) if K is one of A0 , A1 , A2 , A3 , then ∆(WK ) = 1;
(2) if K = A4 = S, then ∆(WS ) = 0.
Proof. For A0 through A3 , norm multiplicativity holds. By Lemma 3.1, for every unit
a one has σmin (La ) = 1, so σmin (La )2 = 1. Taking the infimum over all unit a gives
∆(WK ) = 1.
For S, there exists a nonzero zero divisor a, i.e. there exists a nonzero b with ab = 0.
Then La (b) = 0, so La has a nontrivial kernel and is singular, hence σmin (La ) = 0. Taking
the normalization a/∥a∥, La/∥a∥ is still singular, so σmin = 0 occurs on the unit sphere.
Hence ∆(WS ) = 0. This completes the proof.
Proposition 3.2 uses only the singularity of the left-multiplication operator, not the
graph Laplacian matrix. It gives the plateau–jump structure of the injection gap at the
division levels and the sedenion level: the injection gap is identically 1 at the four division
levels, and jumps to 0 upon entering S. The subsequent argument for the necessity of the
jump depends on the Hurwitz blockade and the classification of absolute-valued algebras,
not on algebraic connectivity.

3.4

Distinction Between Algebraic Connectivity and Injection
Gap

Remark 2 (Graph spectral quantities and operator invariants must not be conflated).
The algebraic connectivity λ2 (WK ) of the constraint graph and the injection gap ∆(WK )
are invariants of different types.
First, the objects defined are different. λ2 (WK ) is the second smallest eigenvalue of the
graph Laplacian matrix LG (WK ), belonging to the combinatorial spectrum of the graph.
∆(WK ) is the square of the minimum singular value of the left-multiplication operator
family {La } on the unit sphere, belonging to the operator spectrum of the algebraic multiplication table.
Second, the parameters depended on are different. λ2 (WK ) depends on the specific
encoding of the constraint graph, including whether edges distinguish signs, whether directions are retained, how multiple edges are merged, how edge weights are calibrated, and
9

## PDF page 10

whether zero-divisor relations are included as edges. ∆(WK ) depends only on the linear
structure of the left-multiplication operators La and the norm inner product. Changing the
organization of the graph can change λ2 , but it does not change the singularity structure
of La , hence does not change the zero/nonzero determination of ∆.
Third, in general the two are not equal. Even if the norm-weighted scheme and the
numbering of basis elements are fixed, there is no a priori equality between λ2 and ∆. If
a relation between them appears under some special encoding, that requires an additional
theorem to establish and cannot be used as a premise of this paper.
Therefore the position of algebraic connectivity in this paper is motivational: it shows
that spectral readings in graph encoding can carry structural information. The arguments
of this paper use only the injection gap ∆. Whenever truncation, jumps, or instability
caused by zero divisors are involved, the criterion is ∆, not λ2 .

3.5

Boundaries of Applicability and Risks

First, the numerical value of the injection gap depends on the weight scheme. This
paper adopts norm weighting with basis elements of norm 1. If edge weights are changed
or the left-multiplication operators are globally rescaled, the specific value of ∆ can
change. What is invariant across weight schemes is the instability mode: the division
levels remain on the same positive constant plateau, and the sedenion level jumps to 0.
If an intermediate value appears, it comes from the weight calibration itself, not from
continuous degeneration of the algebraic structure within the ladder.
Second, the norm-multiplicativity condition of Lemma 3.1 is indispensable. If norm
multiplicativity fails, then even if La is invertible, σmin (La ) need not equal ∥a∥. At the S
level, norm multiplicativity and divisibility fail simultaneously, and the existence of zero
divisors directly gives ∆ = 0.
Third, alternativity is used in the analysis of kernel structure, but is not required by
the definition of the injection gap itself. Definition 3.1 requires only that K be a finitedimensional real algebra equipped with a positive definite quadratic norm. Alternativity
is used in the later analysis of the zero-divisor kernel space to guarantee that the structure
of the relevant linear equations is not destroyed by the associator.
Fourth, this paper does not claim any equality, proportionality, or equivalence between
algebraic connectivity and the injection gap. If in the future a relation between them is
established under a specific graph encoding, that relation should be stated as an additional
theorem with its encoding premises made explicit. The proof chain of this paper depends
only on ∆, and therefore does not bear the proof debt of that additional relation.

4

Spectral Gap Catastrophe Theorem

4.1

Statement of the Theorem

Under the norm-weighted encoding of the Cayley–Dickson ladder, the definition of the
injection gap ∆(WK ) has been given in the previous chapter: for the real algebra Ak
10

## PDF page 11

at level k, let n = 2k , let the basis elements be e0 = 1, e1 , . . . , en−1 , and let the leftmultiplication operator family be La (x) = ax. For each a ∈ Ak , let σmin (La ) be the
minimum singular value of La with respect to the norm inner product. Then
∆(WK ) = min{σmin (La )2 : a ∈ Ak , ∥a∥ = 1}.
The core conclusion of this chapter is as follows.
Theorem 1 (Spectral gap catastrophe). Under the norm-weighted encoding of the Cayley–
Dickson ladder:
(i) for K ∈ {R, C, H, O}, the injection gap is identically the theoretical maximum:
∆(WK ) = 1;
(ii) for K = S, the injection gap jumps to zero: ∆(WS ) = 0;
(iii) within the category of this paper, ∆ takes no intermediate value: its value range is
{0, 1}.
Items (i) and (ii) give the plateau–jump structure; (iii) gives the closedness of the value
range. It must be emphasized that (iii) is a statement about the value range, not a
continuity statement. It does not depend on any continuous family in a moduli space, nor
does it claim that no other numerical values exist outside the category.

4.2

Readings at the Division Levels and the Sedenion Level

First handle (i) and (ii) of Theorem 4.1.
Let K be one of A0 = R, A1 = C, A2 = H, A3 = O. These levels are all division
algebras, and their recursive norms satisfy multiplicativity:
N (xy) = N (x)N (y).
For any nonzero a ∈ K, the left-multiplication operator La satisfies
∥La x∥2 = N (ax) = N (a)N (x) = ∥a∥2 ∥x∥2 .
Hence
∥La x∥ = ∥a∥∥x∥.
When a ̸= 0, the operator La /∥a∥ preserves the norm, hence is orthogonal. Thus La =
∥a∥Ua , where Ua is an orthogonal operator. All singular values of an orthogonal operator
are equal to 1, so all singular values of La are equal to ∥a∥. In particular,
σmin (La ) = ∥a∥.
Taking a on the unit sphere, i.e. ∥a∥ = 1, gives σmin (La ) = 1. Hence
∆(WK ) = min{12 : ∥a∥ = 1} = 1.
This gives (i) of Theorem 4.1.
Now handle K = S. The sedenion algebra is not a division algebra; there exist nonzero
a, b ∈ S with ab = 0. Then La (b) = 0, so La has a nontrivial kernel and is singular. The
11

## PDF page 12

minimum singular value of a singular operator is zero, i.e. σmin (La ) = 0. Normalize a by
setting a′ = a/∥a∥. Since a ̸= 0, one still has La′ (b) = 0, so La′ is singular. Hence a point
with σmin = 0 occurs on the unit sphere. Therefore
∆(WS ) = min{σmin (La )2 : ∥a∥ = 1} = 0.
This gives (ii) of Theorem 4.1.

4.3

No Intermediate Value in the Range

Now handle (iii) of Theorem 4.1. First clarify the category of this paper.
The category of this paper refers to the category of finite-dimensional real normed
algebras formed by the Cayley–Dickson ladder and its isomorphism classes. The objects
of this category are equipped with a positive definite quadratic norm induced by an
inner product, and at the division levels the norm satisfies multiplicativity N (xy) =
N (x)N (y). The sedenions S are equipped with the Cayley–Dickson recursive norm, but
norm multiplicativity fails at this level.
Take any object K in this category. There are two cases.
Case one: K is a division algebra. By the Hurwitz classification, the finite-dimensional
real normed division algebras are, up to isomorphism, only R, C, H, O. Hence K is isomorphic to one of these four levels. The equipped norm satisfies multiplicativity. By the
argument of 4.2, for every unit a one has σmin (La ) = 1, so ∆(WK ) = 1.
Case two: K is not a division algebra. A finite-dimensional real algebra is not a
division algebra if and only if there exist nonzero a, b with ab = 0. Then La has a
nontrivial kernel, La is singular, and σmin (La ) = 0. After normalizing a, one still has
σmin (La/∥a∥ ) = 0. Hence ∆(WK ) = 0.
The two cases exhaust all objects in the category of this paper. Therefore ∆ can only
be 0 or 1, and no intermediate value exists. The value range is {0, 1}.
There is a boundary to make explicit here: if one leaves the category of this paper and
allows division algebras to be equipped with non-multiplicative norms, then σmin (La ) need
not equal ∥a∥, and ∆ may take other values. All arguments of this paper are confined
to the recursive norms of the Cayley–Dickson ladder and norm-weighted encoding, and
therefore do not bear the burden of cases outside the category. Another boundary is:
the closedness of the value range of ∆ comes from the Hurwitz classification and finitedimensional linear algebra, not from any limiting process along a continuous parameter
curve. Hence it does not require a pre-defined continuous family in a moduli space.

4.4

Discriminant Polynomial

The singularity of the left-multiplication operator family can also be recorded uniformly
by a discriminant polynomial.
Definition 2 (Discriminant polynomial). For K = Ak , let n = 2k . Define
DK (a) = det La .
Since La is an n-dimensional real linear operator and the coordinates of a enter the
matrix elements of La linearly, DK is a homogeneous polynomial of degree n in a. For
the sedenion level K = S, n = 16, and DS is a homogeneous polynomial of degree 16.
12

## PDF page 13

Corollary 1 (Zero set of the discriminant polynomial). On S,
DS (a) = 0
if and only if a = 0 or a is a left zero divisor. Hence the zero set of DS is exactly
{0} ∪ ZL (S),
where ZL (S) denotes the left zero-divisor cone of S.
Proof. det La = 0 is equivalent to La being singular, which is equivalent to the existence
of a nonzero x ∈ S with ax = 0. When a = 0 this is obvious; when a ̸= 0, this is precisely
the definition of a being a left zero divisor. Conversely, if a is a left zero divisor, then
there exists a nonzero x with ax = 0, so La is singular and det La = 0. This completes
the proof.
This chapter only registers this discriminant-polynomial statement. Its structural details and the further geometric description of the zero-divisor cone belong to the later
chapter on phase-transition coordinates. It should be pointed out here that DS characterizes left-multiplication singularity, i.e. left zero divisors; right zero divisors require
the discriminant polynomial of the right-multiplication operator Ra (x) = xa. In S the
left and right zero-divisor structures are the same, but the specific sets of elements need
not be pointwise identical. The subsequent arguments of this paper use only the leftmultiplication discriminant polynomial.

4.5

Discussion and Boundaries

The information-theoretic reading of Theorem 4.1 is as follows. At the four divisionalgebra levels, the injection gap is identically at its theoretical maximum 1, and there is
no channel of information loss. Upon entering the sedenion level, the appearance of zero
divisors makes the left-multiplication operator singular, and the injection gap jumps to
0. The total amount of constraints grows exponentially along the ladder: level k has 4k
multiplication relations. Yet the injection gap does not move at all before the collapse.
Hence truncation is not the cumulative endpoint of a decay process, but a jump from
perfect conservation to complete collapse without passing through an intermediate state.
The asymptotic-decay narrative has no mathematical counterpart here: within the
category of this paper, the value range of the injection gap contains only 0 and 1, and
intermediate values are not in the value range. Any continuous parameter curve whose
semantics is “approaching truncation”, if its values always lie within the category of this
paper, can only have injection gap 0 or 1, and cannot vary continuously from 1 to 0. If
the curve leaves the category of this paper, then its spectral values no longer describe the
algebraic structure within the ladder, but only reflect the choice of external encoding or
weight scheme.
There are three boundaries to the conclusions of this chapter.
First, the value range {0, 1} depends on the norm-weighted encoding and the multiplicativenorm premise. If the edge-weight scheme is changed or non-multiplicative norms are
allowed, the specific value of ∆ can change. What is invariant across weight schemes is
the instability mode: the division levels remain on the same positive constant plateau,
and the sedenion level jumps to zero. If an intermediate value appears, it comes from
13

## PDF page 14

the weight calibration itself, not from continuous degeneration of the algebraic structure
within the ladder.
Second, the discriminant polynomial DS characterizes only left-multiplication singularity. If both left and right zero divisors need to be recorded, one should use the leftmultiplication and right-multiplication discriminant polynomials separately. The subsequent arguments of this paper depend only on the left-multiplication family, so no
right-multiplication discriminant polynomial is introduced.
Third, item (iii) of Theorem 4.1 is a statement about the value range, not a statement
of topological continuity. It does not depend on a continuous family in a moduli space, nor
does it claim that no other numerical values exist outside the category of this paper. The
proof chain of this paper uses only the Hurwitz classification, finite-dimensional linear
algebra, and the singularity structure of left-multiplication operators, and introduces no
undefined intermediate space or unconstructed continuous interpolation family.

5

Phase Transition Coordinates: Discrete Control
Parameter, Order Parameter, and Instability Mode

5.1

Phase, Control Parameter, and Order Parameter

The task of phase-transition coordinates is to convert the statement “truncation as a
phase transition” into a testable mathematical object. Four elements are needed: category, control parameter, phase, and order parameter. The category of this paper is
the category of finite-dimensional real normed algebras generated by the Cayley–Dickson
ladder. The control parameter is the ladder level
k ∈ N,

dim Ak = 2k .

Within the scope of this paper, k = 0, 1, 2, 3, 4, corresponding to
A0 = R,

A1 = C,

A2 = H,

A3 = O,

A4 = S.

The control parameter k is discrete. This is not a technical defect, but an essential feature
of this case: the ladder is indexed by integer levels, and the Hurwitz classification excludes
finite-dimensional real normed division algebras between dimension 8 and any successor,
so there is no object in the category of dimensions 9 to 15 available for interpolation. The
discreteness of the control parameter directly determines the form of the phase-transition
event.
For each level K = Ak , the constraint-network encoding WK is given in the previous
chapter: nodes are basis elements, edges record multiplication relations, and edge weights
are the norms. The left-multiplication operator family is
La (x) = ax,

a ∈ K.

The injection gap is
∆(WK ) = min{σmin (La )2 : a ∈ K, ∥a∥ = 1},
14

## PDF page 15

where σmin (La ) is the minimum singular value of La with respect to the norm inner
product.
Definition 3 (Phase and phase-transition coordinates). A phase-transition coordinate
consists of the quadruple
(category, control parameter, encoding, order parameter).
In this paper:
• the category is the category of finite-dimensional real normed algebras of the Cayley–
Dickson ladder;
• the control parameter is the level k ∈ N;
• the encoding is the norm-weighted constraint-network encoding WK ;
• the order parameter is the instability mode M (WK ).
A phase is defined as an encoding equivalence class with the same instability mode under
a given encoding equivalence relation. The encoding equivalence relation requires that
two encodings agree on the zero/nonzero determination of the singular values of the leftmultiplication operator family, and that their plateau values agree up to an allowed global
positive scaling. This equivalence relation does not require the eigenvalues of the graph
Laplacian matrices to be equal, nor the adjacency matrices of the constraint graphs to be
entrywise equal.
The order parameter is not a single numerical value of ∆. A single numerical value
would be globally rescaled with the weight scheme. The order parameter is the instability
mode of ∆ along the control parameter, i.e. the structure of the plateaus, the jump
location, and whether the values before and after the jump are zero. Under the normweighted encoding, the order parameter is
M = (1, 1, 1, 1, 0).
Its reading is: the four levels k = 0, 1, 2, 3 lie on the same positive constant plateau, and
at k = 4 there is a jump to zero. Under other weight schemes that respect the isometry
of the left-multiplication family, the plateau value may become a positive constant cw ,
and the order parameter is
M = (cw , cw , cw , cw , 0).
What is invariant across encodings is the pattern “four plateaus plus one jump”, not
the specific numerical value of the plateau. If an intermediate value appears under some
weight scheme, that intermediate value comes from the weight calibration itself, not from
continuous degeneration of the algebraic structure within the ladder. In that case ∆
measures the weight scheme, not the algebraic structure.
A phase-transition event is defined as: when the control parameter k changes, the
order parameter M changes discontinuously. In the ladder of this paper, this event
occurs between k = 3 and k = 4. Since the control parameter is discrete, there is no
object in the category at k = 3.5. The phase-transition event is not a limit point on a
continuous curve, but a mode jump between discrete levels.

15

## PDF page 16

Boundary statement. The discreteness of the control parameter is an essential feature
of this case. If one leaves the Cayley–Dickson ladder and allows an artificially constructed
continuous parameter family, then the category, encoding, and order parameter must be
redefined, and the phase-transition coordinates of this paper cannot be directly transferred. The cross-encoding invariance of the order parameter is limited to weight schemes
that respect the isometry of the left-multiplication family. If a weight scheme destroys
this isometry, the numerical change of ∆ no longer reflects the instability mode of the
algebraic structure.

5.2

Discreteness Theorem: Value Range and No Interpolation

This section incorporates the latter half of the spectral gap catastrophe theorem into
the phase-transition coordinates and gives a statement about the value range. The core
conclusion is: within the category of this paper, the injection gap takes no intermediate
value.
Theorem 2 (Value range theorem). Let K be an object in the category of finite-dimensional
real normed algebras of the Cayley–Dickson ladder, equipped with the recursive norm, and
adopt the norm-weighted constraint-network encoding. Then
∆(WK ) ∈ {0, 1}.
Moreover, each object takes only one of the two values: if K is a division algebra, then
∆(WK ) = 1; if K is not a division algebra, then ∆(WK ) = 0. There is no object in the
category that takes an intermediate value.
Proof. There are two cases.
Case one: K is a division algebra. By the Hurwitz classification, the finite-dimensional
real normed division algebras are, up to isomorphism, only
R, C, H, O.
Hence K is isomorphic to one of A0 , A1 , A2 , A3 . These levels all satisfy norm multiplicativity:
N (xy) = N (x)N (y).
For any nonzero a ∈ K,
∥La x∥2 = N (ax) = N (a)N (x) = ∥a∥2 ∥x∥2 .
Hence
∥La x∥ = ∥a∥∥x∥.
When a ̸= 0, La /∥a∥ preserves the norm, hence is orthogonal. Thus La = ∥a∥Ua , where
Ua is an orthogonal operator. All singular values of an orthogonal operator are equal to
1, so all singular values of La are equal to ∥a∥. In particular,
σmin (La ) = ∥a∥.
Taking a on the unit sphere, i.e. ∥a∥ = 1, gives σmin (La ) = 1. Hence
∆(WK ) = min{12 : ∥a∥ = 1} = 1.
16

## PDF page 17

Case two: K is not a division algebra. A finite-dimensional real algebra is not a
division algebra if and only if there exist nonzero a, b ∈ K with ab = 0. Then La (b) = 0,
so La has a nontrivial kernel and is singular. The minimum singular value of a singular
operator is zero, i.e. σmin (La ) = 0. Normalize a by setting a′ = a/∥a∥. Since a ̸= 0, one
still has La′ (b) = 0, so La′ is singular. Hence a point with σmin = 0 occurs on the unit
sphere. Therefore
∆(WK ) = min{σmin (La )2 : ∥a∥ = 1} = 0.
The two cases exhaust all objects in the category of this paper. Therefore ∆ can only
be 0 or 1. The value range is {0, 1}. This completes the proof.
Corollary 2 (No interpolation). Within the category of this paper, there is no object K
such that ∆(WK ) takes an intermediate value between 0 and 1. Hence the transition from
∆ = 1 to ∆ = 0 cannot be realized by a continuous change of objects within the category.
This transition is a jump in the sense of the value range: it is not that the decay curve
is steep, but that there is simply no intermediate value in the value range.
Boundaries of applicability. The value range theorem depends on three premises.
First, the category is limited to the Cayley–Dickson ladder and its isomorphism classes.
Second, the norms equipped at the division levels satisfy multiplicativity. Third, the
existence of zero divisors at the non-division level directly gives a nontrivial kernel of
the left-multiplication operator. If division algebras are allowed to be equipped with
non-multiplicative norms, then σmin (La ) need not equal ∥a∥, and ∆ may take other
values. If artificial objects outside the category are allowed, intermediate values may
appear. All arguments of this paper are confined to norm-weighted encoding and recursive
norms, and therefore do not bear the burden of cases outside the category. Albert’s
classification of absolute-valued algebras further supports the point: norm multiplicativity
fails irreversibly beyond dimensions {1, 2, 4, 8}. This paper uses only its conclusion to
support the irreversibility of the loss of norm multiplicativity, and does not use it to
replace the proof of the value range theorem.

5.3

Discriminant Polynomial and Zero-Divisor Cone

The value range theorem gives the discrete values of the order parameter. In order to
localize the phase-transition event as an algebraic object, a discriminant polynomial is
needed.
Definition 4 (Discriminant polynomial). Let K = Ak , with dimension n = 2k . Define
DK (a) = det La .
Since La is an n-dimensional real linear operator and the coordinates of a enter the
matrix elements of La linearly, DK is a homogeneous polynomial of degree n in a. For
the sedenion level K = S, n = 16, and DS is a homogeneous polynomial of degree 16.
Proposition 5 (Zero set of the discriminant polynomial). On S,
DS (a) = 0
if and only if a = 0 or a is a left zero divisor. Hence the zero set of DS is exactly
{0} ∪ ZL (S),
where ZL (S) denotes the left zero-divisor cone of S.
17

## PDF page 18

Proof. det La = 0 is equivalent to La being singular, which is equivalent to the existence
of a nonzero x ∈ S with ax = 0. When a = 0 this is obvious; when a ̸= 0, this is precisely
the definition of a being a left zero divisor. Conversely, if a is a left zero divisor, then
there exists a nonzero x with ax = 0, so La is singular and det La = 0. This completes
the proof.
The discriminant polynomial is homogeneous. For any real number λ,
DK (λa) = det Lλa = λn det La = λn DK (a).
Hence the zero set is a cone: if a is in the zero set, then λa is also in the zero set. For S,
the zero set is exactly the union of the left zero-divisor cone and the zero point.
In the phase-transition coordinates, the discriminant polynomial plays the role of a
local order parameter. At the division levels, DK is nonzero away from zero; at the S
level, DS acquires a nontrivial zero cone. The existence of the left zero-divisor cone is
precisely the algebraic root of the jump of ∆ to zero.
Boundaries of applicability. DS characterizes only left-multiplication singularity, i.e.
left zero divisors. Right zero divisors require the discriminant polynomial of the rightmultiplication operator Ra (x) = xa,
DSR (a) = det Ra .
The left and right zero sets need not be pointwise identical in general. The subsequent
arguments of this paper use only the left-multiplication family, so no right-multiplication
discriminant polynomial is introduced. If both left and right zero divisors need to be
recorded, the two discriminant polynomials should be used separately and must not be
conflated.

5.4

Three-Channel Reading Theorem

The phase-transition coordinates give a unified framework. Within this framework, the
structural change at the truncation point can be observed through three reading channels:
the spectral channel, the information channel, and the symmetry channel. The three
channels are not three independent events, but three invariant readings of the same
algebraic structural change.
Spectral channel. By the value range theorem, the injection gap jumps from ∆ = 1
to ∆ = 0, with the control-parameter location from k = 3 to k = 4.
Information channel. There exist nonzero left zero divisors in S. Take a standard zero
divisor a, whose norm square is 2. The left-multiplication operator La has a nontrivial
kernel, and the kernel dimension is 4. A single left multiplication compresses 4 linearly
independent input directions to the same output 0. Under the counting-cell model at
resolution scale δ, the number of indistinguishable microstates compressed into the same
output grows as δ diverges, while the number of arithmetic steps of a single multiplication
is bounded. Hence the information-conservation inequality S(G′ ) ≥ S(G) − ηC(G) fails
on the right-hand loss term without bound for every finite efficiency parameter η. The
failure is dimensional: unbounded loss versus bounded cost.
Symmetry channel. The automorphism group of the octonions is the fourteen-dimensional
exceptional Lie group G2 : Aut(O) ∼
= G2 . G2 is the complete residual of the surviving
symmetry at the truncation point. The geometry of the truncation debris is recorded by
18

## PDF page 19

two spaces that must be distinguished; their definitions, theorem citations, and bundle
structure are developed in Chapter 9. The first layer is the zero-divisor carrier space
ZD(S), the set of all norm-one left zero divisors; the Moreno criterion parametrizes its
elements as a pair of equal-norm orthogonal unit imaginary octonions, so ZD(S) is diffeomorphic to the Stiefel manifold V2 (R7 ), of dimension 11. The second layer is the
normalized annihilation-pair
√ space Z(S), the set of ordered pairs (x, y) with xy = 0 and
∥x∥ = ∥y∥ = 1 (the norm- 2 section differs only by a positive scaling; see Chapter 9);
Moreno proved that it is homeomorphic to G2 , and Reggiani proved that it is isometric
to G2 under the natural reduced left-invariant metric, of dimension 14. G2 is the automorphism group of O, not the automorphism group of S; its connection with S is realized
geometrically through the annihilation-pair space, not by automorphism identity.
Theorem 3 (Consistency of the three-channel readings). In the phase-transition coordinates, the spectral channel, the information channel, and the symmetry channel occur
simultaneously at the control parameter k = 4. The three channels record the same algebraic structural change: the spectral channel records the loss of divisibility, manifested as
the jump of ∆ from 1 to 0; the information channel records the left-multiplication kernel
caused by zero divisors, manifested as the kernel dimension of a standard zero divisor
being 4, so that a single multiplication can annihilate 4 input directions; the symmetry
channel records the surviving geometric structure at the truncation point, manifested as
Aut(O) ∼
= G2 , with the normalized annihilation-pair space Z(S) diffeomorphic to G2 and
the zero-divisor carrier space ZD(S) diffeomorphic to V2 (R7 ).
The only proven unity within the scope of this paper is: the debris of failure, as the
totality of annihilation events, and the surviving symmetry are the same geometric object.
This paper explicitly does not claim the following: it does not claim any isomorphism
between the residual of this truncation and truncation residuals in other domains; it does
not claim a quantitative equality between the information channel and the symmetry
channel; it does not claim that G2 is the automorphism group of S.
Boundaries of applicability. First, the kernel dimension 4 is the dimension of the leftmultiplication kernel; the fiber dimension of the principal bundle SU (2) → Z(S) → ZD(S)
is 3. The two numerical values are different, and their precise relation is established in
Chapter 9. Second, the diffeomorphism and isometry between Z(S) and G2 are citations
of literature theorems and are not reproved in this paper; this paper uses only this
geometric conclusion and does not use any additional metric structure. Third, the threechannel consistency is a qualitative synchronization, not a unified field theory. It does
not extrapolate to the second law of thermodynamics, nor does it claim that macroscopic
irreversibility is uniquely determined by this algebraic truncation.
Risks and limitations. The value range theorem depends on the Hurwitz classification
and norm multiplicativity; outside the category of this paper, intermediate values may
appear. The cross-encoding invariance of the order parameter is the instability mode,
not the numerical value. The discriminant polynomial records only left-multiplication
singularity; right multiplication requires a separate definition. The three-channel readings
share the same control-parameter location, but the quantitative relations among the three
channels are beyond the scope of this paper. This paper registers the proven structural
unity: the identity of the debris as event space with the surviving symmetry.

19

## PDF page 20

6

Annihilation of Information Traceability

This chapter gives the reading of the same phase-transition coordinates in the information
channel.

6.1

Algebraic Conditions for Traceability

In the norm-weighted constraint-network encoding WK , the evolution of states along
multiplication chains is described by the left-multiplication operator family
La (x) = ax,

a ∈ K.

If the state history is required to be uniquely reconstructible from the output, then every
left multiplication must not lose difference information. This is formalized as follows.
Definition 5 (Left-multiplication traceability). The encoding WK is called traceable in
the left-multiplication sense if for every nonzero a ∈ K, the left-multiplication map La is
injective, i.e.
La (x1 ) = La (x2 ) =⇒ x1 = x2 .
Proposition 6 (Divisibility is equivalent to left-multiplication traceability). At each level
Ak of the Cayley–Dickson ladder, the following conditions are equivalent:
(i) Ak is a division algebra;
(ii) for every nonzero a ∈ Ak , La is injective;
(iii) for every nonzero a ∈ Ak , La is invertible.
Proof. First prove (i) implies (iii). If Ak is a division algebra, then every nonzero a has a
multiplicative inverse a−1 . At every level of the ladder in this paper, the left-multiplication
operator satisfies
La−1 La = id.
Hence La has a left inverse. A finite-dimensional linear operator has a left inverse if and
only if it is invertible, so La is invertible.
Next prove (iii) implies (ii). An invertible operator is necessarily injective.
Finally prove (ii) implies (i). If La is injective for every nonzero a, then the equation
ax = 0 has only the zero solution. Hence there are no nonzero left zero divisors. At
every level of the ladder in this paper, the absence of left zero divisors is consistent with
divisibility: A0 through A3 are division algebras; A4 has nonzero left zero divisors, hence
is not a division algebra. Therefore (ii) implies (i). This completes the proof.
The boundaries of applicability of Proposition 6.2 are as follows. First, it discusses
only traceability in the left-multiplication sense. Traceability in the right-multiplication
sense requires the right-multiplication operator Ra (x) = xa. Second, traceability guarantees only that a single left multiplication is invertible. If every factor in a multi-step
composite is nonzero and invertible, then the composite is invertible and the history
can be reconstructed step by step. Third, at the sedenion level, there exist nonzero but
non-invertible factors, namely zero divisors. Then a single left multiplication can be
non-invertible, and information annihilation occurs.

20

## PDF page 21

6.2

Annihilation Arithmetic at the Sedenion Level

Upon entering the sedenion level K = S, divisibility fails. By the Moreno criterion, there
exist nonzero left zero divisors in S. Take a standard zero divisor a, whose norm square
is 2. The left-multiplication operator La is singular, and the kernel
ker La = {x ∈ S : ax = 0}
is a nontrivial subspace. Under the exact integer multiplication table, a linear-algebra
computation gives
dim ker La = 4.
This kernel dimension is consistent with the general results on large annihilators in
Cayley–Dickson algebras. Two quantities must be distinguished here: the kernel dimension 4 is the dimension of the kernel space of the left-multiplication operator La ; it
is not equal to the dimension of any principal-bundle fiber. The fiber dimension is determined by the bundle structure; for example, some principal bundles have fiber dimension
3, which is not the same quantity as the kernel dimension 4, and no correspondence between the two is established; Chapter 9 gives the precise relation: the fiber is the unit
sphere of the left-multiplication kernel for a fixed carrier, dim ker Lx = dim π −1 (x)+1 = 4.
The arithmetic meaning of the kernel dimension 4 is: there exist 4 linearly independent
input directions x1 , x2 , x3 , x4 such that
La (x1 ) = La (x2 ) = La (x3 ) = La (x4 ) = 0.
Hence a single left multiplication can compress these 4 independent directions into the
same output. The output no longer distinguishes these input directions, and difference
information is annihilated.
To quantify this annihilation, consider the counting-cell model at resolution scale
δ > 0. Suppose the state space is partitioned into cells of volume approximately δ d ,
where d is the dimension of the state space. The macroscopic entropy Sδ (G) is defined
as the logarithm of the number of cells covered by the current macroscopic state. The
dynamics is a single left multiplication T = La , whose arithmetic cost is bounded, denoted
by C(G) = 1. The efficiency parameter η > 0 is finite and represents the upper bound on
information loss allowed per unit cost. The information-conservation inequality states:
there exists a constant η depending only on the encoding scheme such that for all δ,
Sδ (G′ ) ≥ Sδ (G) − ηC(G),
where G′ = T (G).
Now take a to be a standard zero divisor. The kernel ker La is a 4-dimensional linear
subspace. Take a 4-dimensional ball of radius R in it. Under the δ-partition, this ball
contains approximately
cR4 δ −4
cells, where c is a positive constant depending only on the dimension. All these cells are
mapped by La to near the same output point 0. Even if the output side allows a finite
number of cells, the indistinguishability in the kernel directions still gives a lower bound
on the macroscopic entropy loss:
Sδ (G) − Sδ (G′ ) ≥ ln(cR4 δ −4 ) − O(1) = 4 ln(1/δ) + O(1).
21

## PDF page 22

The right-hand side diverges logarithmically as δ → 0, while ηC(G) = η is a fixed
constant. Hence for any finite η, taking δ sufficiently small, for example
)︃
(︃
η + O(1)
,
δ < exp −
4
makes the information-conservation inequality fail. The failure is not an accidental result
of a constructive counterexample sequence, but a direct dimensional corollary: unbounded
loss versus bounded cost.
Boundaries of applicability. This argument depends on three model-internal premises.
First, the state space is partitioned into counting cells at resolution scale δ, and macroscopic entropy is defined by cell counting. Second, the arithmetic cost of a single multiplication is bounded, taken as 1 in this paper. Third, the efficiency parameter η is a
finite constant independent of δ. If η is allowed to diverge with δ, or the cost is allowed to
diverge with δ, the inequality might hold in another form. This paper is confined to algebraic encoding and the above counting model. Misalignment between the kernel space
and the partition grid changes only the constant term, not the logarithmic divergence
term 4 ln(1/δ). If the output side has a finite number of cells, this also does not affect
the lower bound.

6.3

Correspondence with the Phase-Transition Coordinates

In the phase-transition coordinates, the control parameter is the level k, and the order
parameter is the instability mode. At k = 4, the order parameter jumps from the fourplateau structure to zero. The information-channel reading is as follows.
First, loss of divisibility. At the sedenion level there exist nonzero left zero divisors,
and the left-multiplication operator is no longer injective.
Second, locking of the kernel dimension. The left-multiplication kernel of a standard
zero divisor has dimension 4.
Third, a single multiplication can annihilate 4 input directions. Difference information
is irreversibly lost in one step.
Fourth, the information-conservation inequality fails for every finite efficiency parameter. The loss lower bound diverges logarithmically as the resolution scale δ → 0, while
the cost is bounded.
These readings are synchronized with the injection-gap jump in the spectral channel and with the G2 residual in the symmetry channel. The only proven structural unity
within the scope of this paper is: the debris of failure and the surviving symmetry are the
same geometric object, namely the normalized annihilation-pair space Z(S) is diffeomorphic to G2 . This paper does not claim a quantitative equality between the information
channel and the symmetry channel, nor does it claim that the kernel dimension 4 equals
the fiber dimension of any principal bundle; Chapter 9 gives the precise relation: the
fiber is the unit sphere of the kernel space.

6.4

Boundaries and Risks

First, the definition of traceability is limited to left-multiplication injectivity. More complex history-reconstruction protocols may introduce additional constraints, but the non22

## PDF page 23

invertibility of a single left multiplication is already sufficient to block the unique reconstruction of difference information.
Second, the kernel dimension 4 is the dimension of the left-multiplication kernel.
The right-multiplication kernel must be computed separately; the left and right kernel
dimensions in S have the same structure, but the specific sets of elements need not be
pointwise identical.
Third, the information-conservation inequality is a model-internal statement, not the
second law of thermodynamics. This paper does not extrapolate to physical thermodynamics.
Fourth, δ → 0 is an idealized limit. At finite resolution, the failure threshold can be
explicitly computed by comparing 4 ln(1/δ) with η.
Fifth, the specific coordinates of a standard zero divisor depend on the sign convention,
but structural conclusions such as the kernel dimension 4, the existence of zero divisors,
and the failure of the information-conservation inequality are convention-independent.
This paper uses only structural conclusions and does not depend on specific coordinate
assignments.
In summary, the information-channel reading is: at the control parameter k = 4 of
the phase-transition coordinates, traceability is annihilated by a single left multiplication,
and the kernel dimension 4 together with the bounded multiplication cost causes the
information-conservation inequality to fail for every finite efficiency parameter. This is
the quantitative manifestation of algebraic hard truncation in the information channel.

7

G2 Rigid Anchoring

This chapter gives the reading of the same phase-transition coordinates in the symmetry
channel.

7.1

Location of the Symmetry Channel

In the phase-transition coordinates, the control parameter is the level k, and the order
parameter is the instability mode. The spectral channel records the plateau and jump of
the injection gap ∆, and the information channel records the annihilation of difference
information caused by the left-multiplication kernel. The symmetry channel records the
residual of the same algebraic structural change in geometric symmetry. The reading
location of this channel is still at the control parameter k = 4: zero divisors appear at
the sedenion level, divisibility is lost, and the symmetry surviving at the truncation point
is characterized by the octonion automorphism group G2 .
The object of the symmetry channel must first be clarified. The set of all R-algebra
automorphisms of the octonion algebra O forms the group Aut(O). The classical fact
is Aut(O) ∼
= G2 , where G2 is the fourteen-dimensional compact connected simple Lie
group. G2 is not merely some connected subgroup, nor merely the identity component; it
is the full automorphism group of O. In the sequel, whenever this paper says that “G2 is
the symmetry surviving at the truncation point”, it uses this precise meaning. The two

23

## PDF page 24

spaces of the debris geometry—the zero-divisor carrier space ZD(S) and the normalized
annihilation-pair space Z(S)—are made precise in Chapter 9.

7.2

The Symmetry Surviving at the Truncation Point

Theorem 4 (Rigid anchoring). (i) G2 is the complete residual of the symmetry at the
O truncation point: Aut(O) ∼
= G2 is the full automorphism group. There is no larger
algebraic automorphism group that simultaneously preserves the octonion multiplication structure and the norm.
(ii) The debris of failure is governed by the same symmetry: the normalized annihilationpair space Z(S) is diffeomorphic to G2 ; the zero-divisor carrier space ZD(S) is
diffeomorphic to the Stiefel manifold V2 (R7 ).
(iii) The blockade is at the category level: any attempt to extend O within the category
of normed bilinear algebras must destroy norm multiplicativity or divisibility.
Proof sketch. (i) Let φ be an R-algebra automorphism of O. An automorphism preserves
the unit, so φ fixes the real axis and acts on the imaginary part Im(O) ∼
= R7 . The octonion multiplication structure implies the norm structure, so the action of φ on Im(O)
belongs to O(7); since Aut(O) is connected, Aut(O) ⊆ SO(7). The classical theorem
gives Aut(O) ∼
= G2 . The qualification “no larger” is: within the scope of algebraic automorphisms that simultaneously preserve the multiplication structure and the norm, there
is no larger group; if one requires only norm preservation without preserving the multiplication structure, then O(7) is larger, but such a group is not an algebraic automorphism
group and is outside the scope of this theorem.
(ii) The Moreno criterion gives the parametrization of zero divisors and the manifold
structure of the zero-divisor space. The zero-divisor carrier space ZD(S) is diffeomorphic
to V2 (R7 ); the normalized annihilation-pair space Z(S) is diffeomorphic to G2 , and Reggiani further proved that this diffeomorphism is an isometry under the natural reduced
left-invariant metric. The definitions, dimension counts, and principal-bundle structures
of the two spaces are given in Chapter 9. It must be noted here: G2 is the automorphism
group of O, not the automorphism group of S; the connection between G2 and S is the
geometric realization of the annihilation-pair space, not an automorphism identity.
(iii) If there existed a 16-dimensional object extending O within the category of
normed bilinear algebras and simultaneously preserving norm multiplicativity and divisibility, then one would obtain a 16-dimensional real normed division algebra. The
Hurwitz classification excludes unital real normed division algebras of dimension 16, so
such an extension is impossible. This completes the proof.
The correspondence of Theorem 7.1 with the phase-transition coordinates is as follows. At the control parameter k = 4, the order parameter jumps from the four-plateau
structure to zero. What the symmetry channel records is: the full automorphism group
surviving at the octonion level is G2 ; the annihilation-event space at the sedenion level
geometrically reproduces G2 . The only proven unity within the scope of this paper is:
the debris of failure, as the totality of annihilation events, and the surviving symmetry
are the same geometric object. This paper does not claim any isomorphism between the
G2 residual and truncation residuals in other domains.

24

## PDF page 25

7.3

Conditional Corollary: Dimension Retraction

Suppose the information carrier penetrates through a G2 filter, and the coupling constant
is calibrated according to the information-carrier compression ratio as ε0 = (14/8)(ln 2)/6 ≈
0.202. Then the effective dimension of the carrier retracts according to Deff = 2DH /(1 +
ε0 DH ). This function is strictly increasing in DH , with supremum 2/ε0 ≈ 9.89. The
exact range in which Deff < 8 holds is DH < D∗ , where the critical value is D∗ =
8/(2 − 8ε0 ) ≈ 20.9. Hence the effective statement of retraction below eight dimensions
is: when 16 ≤ DH ≤ 20, Deff < 8 (endpoint readings: Deff (16) ≈ 7.56, Deff (20) ≈ 7.93);
when DH ≥ 21, the inequality no longer holds (Deff (21) ≈ 8.01).
Conditional-depth declaration: the constant calibration of this corollary depends on
framework-level information-coupling bookkeeping, whose derivation is beyond the scope
of this paper. This paper registers it as a conditional statement, whose validity presupposes the independent establishment of that calibration. Before the calibration is
established, this corollary does not constitute a theorem and does not participate in any
other argument of this paper. The debt scope of this corollary is limited to this section
and is not assigned to any other proposition of this paper.

7.4

Boundaries and Risks

First, G2 is Aut(O), not Aut(S). The connection between G2 and S is the geometric
realization of the annihilation-pair space, not an automorphism identity. Conflating the
two leads to a category error.
Second, the diffeomorphism between the normalized annihilation-pair space Z(S) and
G2 , as well as Reggiani’s isometric strengthening, are citations of literature theorems.
This paper uses only this geometric conclusion, does not use any additional metric structure, and does not claim any isomorphism between this structure and truncation residuals
in other domains.
Third, the kernel dimension 4 is the dimension of the left-multiplication kernel, while
the principal-bundle fiber dimension is 3. The two numerical values are different. Chapter
9 gives the precise relation: the fiber is the unit sphere of the left-multiplication kernel
for a fixed carrier, dim ker Lx = dim π −1 (x) + 1 = 4.
Fourth, the debt scope of the conditional corollary is limited to Section 7.3, and its
validity or invalidity does not affect the proven algebraic structural conclusions of this
paper.
Fifth, this paper does not extrapolate to the second law of thermodynamics. The
symmetry channel records the geometric residual at the algebraic truncation point, not
a physical law of macroscopic irreversibility.
Sixth, the structural conclusions are convention-independent: the existence of zero
divisors, Aut(O) ∼
= G2 , the diffeomorphism of the normalized annihilation-pair space with
G2 , the diffeomorphism of the zero-divisor carrier space with V2 (R7 ), the kernel dimension
4, and other facts are convention-independent. Specific coordinate assignments depend
on the sign convention, but this paper uses only structural conclusions.

25

## PDF page 26

8

Irreversibility and the Arrow of Time

8.1

Internal Operations and Dimension Monotonicity

Let the starting point be the sedenion algebra S, of dimension 16. By algebraic internal
operations, this paper means the following three types:
First, taking subalgebras. If B is a subalgebra of A, then dim B ≤ dim A.
Second, taking two-sided quotients. Let I be a two-sided ideal of A, i.e. for all a ∈ A
and x ∈ I, one has ax ∈ I and xa ∈ I. The dimension of the quotient algebra A/I is
dim(A/I) = dim A − dim I ≤ dim A.
Third, taking isomorphic images. An isomorphism preserves dimension, so the isomorphic image has the same dimension as the original algebra.
Therefore, starting from S, for any finite sequence in which every step is one of the
above three types of internal operations, the dimension is monotonically nonincreasing
along the sequence. The dimension of the endpoint of the sequence does not exceed 16.
Now consider the case where the endpoint dimension equals 16. Since the dimension
starts at 16 and is monotonically nonincreasing, if the endpoint is still 16, then the
dimension must remain 16 at every step of the sequence.
If some step takes a subalgebra and the dimension remains 16, then the subalgebra
equals the original algebra itself.
If some step takes a two-sided quotient and the dimension remains 16, then the dimension of the ideal I is
dim I = dim S − dim(S/I) = 16 − 16 = 0,
so I is the zero ideal and the quotient algebra is isomorphic to S itself.
If some step takes an isomorphic image, then the image is isomorphic to the original
algebra.
Therefore, any sequence of internal operations whose endpoint dimension is 16 must
have an endpoint isomorphic to S. But S is not a division algebra, because it contains
nonzero left zero divisors. Hence the endpoint cannot be a sixteen-dimensional normed
division algebra.
Further clarify the case of a proper two-sided quotient. Let I be a proper two-sided
ideal of S, i.e. I ̸= S. If I contains an invertible element u, then the multiplicative
inverse u−1 of u belongs to S. Since I is a two-sided ideal, uu−1 = 1 belongs to I. Then
I contains the unit, so I = S, contradicting that I is proper. Hence any nonzero element
of a proper two-sided ideal I is non-invertible. In S, non-invertible elements are exactly
zero divisors or zero. Therefore any proper two-sided ideal contains a zero divisor. Hence
any proper two-sided quotient cannot preserve full divisibility. If the quotient is still a
division algebra, then by the Hurwitz classification below, its dimension can only belong
to {1, 2, 4, 8}, which is strictly less than 16. This closes the question “does there exist
a nontrivial sixteen-dimensional quotient?”: a sixteen-dimensional quotient requires the
zero ideal, and a nontrivial quotient must have lower dimension.

26

## PDF page 27

8.2

Impossibility of Internal Repair

Theorem 5 (Impossibility of internal repair). There is no sequence starting from S and
consisting only of algebraic internal operations whose endpoint is a sixteen-dimensional
normed division algebra. Any division-algebra endpoint obtained by internal operations
must belong to
{R, C, H, O}.
In other words, the endpoint of so-called “repair” can only be a division level after dimension reduction, and it is impossible to restore divisibility at the sixteen-dimensional
level.
Proof. Let the endpoint of the sequence be A.
Case one: dim A = 16. By the dimension monotonicity of 8.1, the dimension at every
step of the sequence is 16. The endpoint is isomorphic to S. S contains nonzero zero
divisors, hence is not a division algebra. Therefore A is not a sixteen-dimensional normed
division algebra.
Case two: dim A < 16 and A is a division algebra. By the Hurwitz classification, the
finite-dimensional real normed division algebras are, up to isomorphism, only
R, C, H, O,
of dimensions 1, 2, 4, 8. Hence A must belong to {R, C, H, O}.
The two cases exhaust all possibilities. Therefore internal operations cannot advance
from S to a new sixteen-dimensional division algebra; the division-algebra endpoint can
only be a lower-dimensional level. This completes the proof.

8.3

Arithmetic Root of Irreversibility

The Cayley–Dickson doubling procedure
¯ da + bc̄)
(a, b)(c, d) = (ac − db,
compresses two lower-dimensional structures into a higher-dimensional structure. Every
step is completely legitimate at the symbolic level, but the loss of structural axioms is
irreversible. Upon entering the sedenion level, norm multiplicativity fails, alternativity
fails, and zero divisors appear. The left-multiplication operator
La (x) = ax
is no longer invertible for every nonzero a. The left-multiplication kernel of a standard
zero divisor has dimension 4. This means that there exist 4 linearly independent input
directions that are all compressed into the same output after one left multiplication.
The output no longer distinguishes these input directions, and difference information is
annihilated inside the map.
Internal operations cannot raise dimension. Subalgebras do not raise dimension, twosided quotients do not raise dimension, and isomorphic images preserve dimension. Therefore, once one enters S, one cannot decompress back to O by internal operations, nor can
one regain divisibility at the sixteen-dimensional level. The information required for inversion is not masked by external noise, but has already been destroyed in the structure of
the multiplication map. This is the arithmetic root of irreversibility within the algebraic
category.

27

## PDF page 28

8.4

Correspondence with the Phase-Transition Coordinates

In the phase-transition coordinates, the control parameter is the level k, and the order
parameter is the instability mode. At k = 4, the order parameter jumps from the fourplateau structure to zero. The spectral channel records the jump of the injection gap ∆
from 1 to 0; the information channel records the left-multiplication kernel dimension 4;
the symmetry channel records the surviving symmetry at the truncation point as G2 .
Irreversibility is the consequence of the same phase-transition coordinates at the operational level. Once one enters k = 4, the dimension monotonicity of internal operations
prevents any subsequent operation from raising the dimension; if a two-sided quotient
preserves dimension 16, then the ideal is zero and the quotient is S itself; if the ideal
is nonzero, then the quotient dimension decreases, and divisibility can only fall into
{R, C, H, O}. Therefore, starting from S, one cannot return to a higher division level by
internal operations, nor construct a new sixteen-dimensional division algebra.
The “arrow of time” here is a name for algebraic one-directionality, not a physical arrow of time. It describes that after the loss of structural axioms, the difference information
required for inversion has been annihilated inside the map. It is not frictional dissipation,
not statistical coarse-graining, and not a corollary of the second law of thermodynamics.

8.5

Boundaries and Risks

First, internal operations are limited to taking subalgebras, taking two-sided quotients,
and taking isomorphic images. If external objects are introduced, the category is changed,
or dimension-raising constructions are artificially allowed, then this theorem does not
apply.
Second, the Hurwitz classification applies to finite-dimensional real normed division
algebras. Outside this category, the classification conclusion does not apply, and the
dimension restriction on division-algebra endpoints no longer holds.
Third, the argument that a proper two-sided ideal contains a zero divisor depends on
S containing a unit and on invertible elements generating the whole algebra. This paper
uses this argument under the definition of two-sided ideals in nonassociative algebras, i.e.
requiring both AI ⊆ I and IA ⊆ I.
Fourth, the kernel dimension 4 is related to the left-multiplication operator. The rightmultiplication operator must be computed separately. The irreversibility conclusion of
this paper depends only on the nontriviality of the kernel of the left-multiplication family
and the dimension monotonicity of internal operations, not on the specific coordinates of
zero divisors.
Fifth, this paper does not extrapolate to the second law of thermodynamics. Irreversibility is strictly confined to the algebraic category; its content is the loss of structural
axioms and the annihilation of difference information, not a macroscopic physical process.
Sixth, the specific coordinates of zero divisors depend on the sign convention, but
structural conclusions such as dimension monotonicity, the Hurwitz classification, the
kernel dimension 4, and the impossibility of internal repair are convention-independent.

28

## PDF page 29

9

The Two Geometries of the Debris: Carrier Space
and Annihilation Event Space

9.1

Layering of Objects

When Chapters 5 and 7 state that “the debris of failure and the surviving symmetry
are the same geometric object”, the word debris simultaneously carries two geometric
objects. One is the failing element itself: a nonzero, left-noninvertible sedenion; the
other is the annihilation event: an ordered pair of equal norm whose product is zero. The
two have different dimensions and must be registered separately; otherwise the identity
proposition cannot be judged true or false. This chapter completes this distinction and
gives the closed form of the dimension count.
Definition 6 (Zero-divisor carrier space). ZD(S) = {x ∈ S : x is a left zero divisor, ∥x∥ =
1}, equipped with the subspace topology.
Definition 7 (Normalized annihilation-pair space). Z(S) = {(x, y) ∈ S × S : xy =
0, ∥x∥ = ∥y∥ = 1}, equipped with the subspace topology.
Convention
note. Other chapters of this paper use the standard two-term zero divisor
√
of norm 2 as a model (its norm square is 2); Definitions 9.1 and 9.2 take the norm-1
section. The two conventions differ only by a global positive scaling, and the diffeomorphism type and group-action structure are unchanged; the conclusions of this chapter are
true under both conventions.

9.2

The Two Spaces and Their Identification

Theorem 6 (Debris geometry, precise form).
manifold V2 (R7 ), of dimension 11.

(i) ZD(S) is diffeomorphic to the Stiefel

(ii) Z(S) is diffeomorphic to G2 , of dimension 14; moreover, under its natural reduced
left-invariant metric, it is isometric to G2 .
projection π(x, y) = x
Carrier layer: ZD(S) ∼
= V2 (R7 ) (dimension 11).
Objects are norm-1 left zero divisors x.

Event layer: Z(S) ∼
= G2 (dimension 14). Objects
are normalized pairs (x, y) with xy = 0.

Fiber over a fixed carrier x0 : π −1 (x0 ) = {y ∈ ker Lx0 : ∥y∥ = 1} ∼
= S3 ∼
= SU (2). Kernel relation:
dim ker Lx0 = 4 = dim(π −1 (x0 )) + 1.

Legend: the carrier space counts failing elements; the event space counts annihilation events. The two spaces
are linked by the classical principal bundle SU (2) → G2 → V2 (R7 ), so 14 = 11 + 3.

Figure 2: Carrier space vs. annihilation-event space and the principal-bundle linkage.

Structural source of (i). By the Moreno criterion of Proposition 2.2, x = (a, b) ∈ S =
O2 is a left zero divisor if and only if a, b are nonzero equal-norm orthogonal imaginary
octonions. Under the norm-1 convention, x ↦→ (a/∥a∥, b/∥b∥) gives a bijection between
29

## PDF page 30

ZD(S) and the set of all orthogonal unit pairs in Im(O) ∼
= R7 —that is, V2 (R7 ); this
bijection and its inverse are expressed by smooth algebraic operations, hence it is a
diffeomorphism. The dimension is dim V2 (R7 ) = 2 · 7 − 3 = 11.
(ii) is the theorem of Moreno (homeomorphism) and Reggiani (diffeomorphism and
isometry), cited here without proof. Reggiani also confirms that the identification ZD(S) ∼
=
7
V2 (R ) agrees with (i).

9.3

Precise Relation Between the Principal Bundle and the
Kernel Space

Define the projection π : Z(S) → ZD(S), (x, y) ↦→ x.
Proposition 7 (Kernel realization of the fiber). For any x0 ∈ ZD(S), π −1 (x0 ) = {y ∈
ker Lx0 : ∥y∥ = 1}, i.e. the unit sphere of the left-multiplication kernel ker Lx0 . In
particular, every fiber is diffeomorphic to S 3 .
Proof. By definition, (x0 , y) ∈ Z(S) if and only if x0 y = 0 and ∥y∥ = 1; the former
is y ∈ ker Lx0 . The kernel ker Lx0 is an R-linear subspace of S (Appendix C.3). It
remains to show that the kernel dimension is independent of x0 ; this is the real point
of the proposition. G2 acts diagonally on S = O2 : g(a, b) = (ga, gb); since g preserves
multiplication, involution, and norm, for any p, q ∈ S one has g(pq) = (gp)(gq), so the
left-multiplication operator satisfies Lgx0 ◦g = g ◦Lx0 , hence ker Lgx0 = g ·ker Lx0 , and the
kernel dimension is an orbit invariant. Through the equivariant identification of Theorem
9.1(i), all points of ZD(S) form a single orbit of G2 on V2 (R7 ): G2 acts transitively on
S 6 with isotropy subgroup SU (3), and SU (3) acts transitively on the unit sphere of the
orthogonal complement. Hence all fibers are pairwise diffeomorphic and have the same
dimension. Appendix A(6) machine-checks dim ker Lx0 = 4 at a standard two-term zero
divisor, so every fiber is diffeomorphic to S 3 . This completes the proof.
Theorem 7 (Identification of the Borel principal bundle). Under the identification of
Theorem 9.1, the projection π agrees with the classical principal bundle SU (2) → G2 →
V2 (R7 ): G2 acts transitively on V2 (R7 ), the isotropy subgroup is SU (2), and the fiber is
diffeomorphic to SU (2) ∼
= S 3 . The dimension count closes: dim Z(S) = dim ZD(S) +
dim SU (2), i.e. 14 = 11 + 3.
Corollary 3 (Precise kernel count). For any x0 ∈ ZD(S), dim ker Lx0 = dim π −1 (x0 ) +
1 = 4. The statement registered in earlier chapters that “the kernel dimension 4 and the
fiber dimension 3 are not the same quantity” is thereby made precise: their difference is
identically one, and each fiber is geometrically realized as the unit sphere of the corresponding left-multiplication kernel. The two numbers count different objects—4 counts the
input directions annihilated by the fixed operator, and 3 counts the annihilation-partner
directions over a fixed carrier—and conflating the two is the other side of the same coin
as establishing a precise relation between them.
Boundaries of applicability. The bundle identification of Theorem 9.3 is a citation
combining a classical theorem with Reggiani’s identification; this paper does not reprove
its equivariance. All conclusions of this chapter concern only left zero divisors; the corresponding structure for right zero divisors is obtained by symmetry under the involution,
and there is a natural diffeomorphism between the left and right spaces, but this paper
does not develop it.

30

## PDF page 31

9.4

Precise Form of the Identity Proposition

Now we can give the only legitimate reading of the slogan of Chapters 5 and 7.
Surviving symmetry (Aut(O) ∼
= G2 , dimension 14) = the totality of annihilation
events Z(S) (the debris as event set).
Carrier space ZD(S) ∼
= V2 (R7 ) = G2 /SU (2) (the debris as the set of failing elements,
the quotient space of the surviving symmetry action).
Reading discipline: the fourteen-dimensional identity holds only at the event level; the
element level is an eleven-dimensional accompanying geometry, not G2 . Both readings
are legitimate, but they must be stated layer by layer; if the two layers are compressed
into the same notation, the identity proposition becomes undecidable.

9.5

Open Problems

Problem one (universality). Is the carrier–event dichotomy a universal structure of algebraic hard truncation? That is, for any truncation with an order-parameter jump in
phase-transition coordinates, does there always exist an “event space” that is the same
object as the surviving symmetry at the truncation point, while the “carrier space” is
the quotient of that symmetry action?
Problem two (metric–counting correspondence). Reggiani’s isometric structure induces a natural left-invariant metric on Z(S). Is there a quantitative correspondence
between the geometric quantities of this metric (diameter, cut locus, geodesic completeness) and the divergence rate 4 ln(1/δ) in the δ-partition counting model of Chapter 6?
Problem three (left–right symmetry). What is the precise statement connecting the
right annihilation-pair space and the left annihilation-pair space by the involution? Is
their union closed under some composition operation?

9.6

Boundaries of Applicability of This Chapter

First, Theorems 9.1 and 9.3 are citations and assemblies of literature theorems; the
contribution of this paper √
is to register the two spaces in layers and close the dimension
count. Second, the norm- 2 and norm-1 conventions differ only by a positive scaling,
and the conclusions are unchanged. Third, this chapter does not claim any isomorphism
between the carrier–event structure of this truncation and truncation residuals in other
domains; Problem one is only a question, not a claim.

10

Open Boundaries and Honest Declarations

This chapter registers the boundaries of applicability and the non-claims of the arguments
of this paper. These boundaries are not additional disclaimers, but constituent parts of
the argument structure. They limit the effective range of the conclusions and prevent
over-extrapolation.
(1) Encoding dependence of numerical values. The specific numerical value of the
injection gap depends on the weight scheme. Under norm-weighted encoding, the spectral
31

## PDF page 32

gap catastrophe theorem gives the plateau–jump structure ∆ equals 1 and ∆ equals 0.
Under other weight schemes that respect the isometry of the left-multiplication family,
the plateau value may become a positive constant, but the jump location and the zerovalue structure remain unchanged. If an intermediate value appears, it comes from the
weight calibration itself, not from continuous degeneration of the algebraic structure
within the ladder. What is invariant across encodings is the instability mode, i.e. the
order-parameter structure of “four plateaus plus one jump”, not the specific numerical
value of the plateau.
(2) Debt scope of the conditional corollary. The dimension-retraction formula of Section 7.3 presupposes the calibration of framework-level information-coupling bookkeeping,
and its effective range is limited to 16 ≤ DH ≤ 20. The independent establishment of
that calibration is beyond the scope of this paper. Before the calibration is established,
this corollary does not constitute a theorem and does not participate in the proof of
any other proposition of this paper. Its debt scope is limited to that section and is not
assigned to other conclusions of this paper.
(3) Closure of the isomorphism boundary. This paper does not claim an isomorphism
between the G2 residual and truncation residuals in any other domain. The only proven
unity within the scope of this paper is: the debris of failure, as the totality of annihilation
events, and the surviving symmetry are the same geometric object, namely the normalized annihilation-pair space Z(S) is diffeomorphic to G2 (Reggiani strengthened it to an
isometry); the zero-divisor carrier space ZD(S) is diffeomorphic to V2 (R7 ), the quotient
space of the G2 action. This isometry is a geometric fact, not an automorphism identity.
G2 is the automorphism group of the octonions O, not the automorphism group of the
sedenions S. The distinction between the two spaces and their principal-bundle structure
are given in Chapter 9.
(4) Corroborative status of the cases. Hurwitz termination, zero-divisor geometry,
and absolute-valued algebra blockade are all facts already established in the literature.
Their use in this paper is limited to corroboration and assembly, and does not depend on
any of them in a form beyond its original statement. The proof chain of this paper uses
only the proven parts of these facts and introduces no additional assumptions.
(5) Distinction between sign conventions and structural conclusions. The encoding
conventions of this paper are explicitly locked in Appendix B: the authoritative convention
is the doubling recursion of Section 2.1; the Fano hand-calculation table of B.2 is a derived
table of that recursion, and the orientation is governed by the recursive output; the pseudocode of B.3 is an executable implementation of that recursion and has been checked
cell by cell over the full table. All Fano-dependent assertions of this paper have been
recomputed under this locked convention. Specific assignments under different sign conventions may differ, for example the specific coordinates of zero divisors and the specific
values of alternativity failure. But the structural conclusions are convention-independent:
the existence of zero divisors, the kernel dimension 4, the failure of alternativity at the
sedenion level, the canonical count 84 of standard two-term zero divisors, the value range
{0, 1} of the injection gap, the G2 rigid anchoring, the carrier–event dichotomy, etc. This
paper uses only structural conclusions and does not depend on specific sign assignments.
The validity of any assertion depending on specific coordinates is limited to the locked
encoding convention. This convention is consistent with the Cayley–Dickson recursive
implementation, and all numerical assertions are verifiable in exact integer arithmetic.
The above five boundaries jointly limit the scope of the conclusions of this paper.
The mathematical backbone of this paper—from the Hurwitz classification to the G2
32

## PDF page 33

rigid anchoring—does not depend on additional assumptions outside these boundaries.
The role of the boundary declarations is to institutionalize the honesty and verifiability
of the argument.

11

Conclusion

The termination of the Cayley–Dickson ladder is, in the framework of this paper, not
a taxonomic footnote, but a first-order phase transition (phase-transition coordinates
in Chapter 5). The phase-transition coordinates consist of the quadruple of category,
control parameter, encoding, and order parameter: the category is the category of finitedimensional real normed algebras of the Cayley–Dickson ladder; the control parameter is
the level k, corresponding to dimension 2k ; the encoding is the norm-weighted constraintnetwork encoding; the order parameter is the instability mode of the injection gap along
the control parameter. In these coordinates, the division levels form the same positive
constant plateau, and upon entering the sedenion level the order parameter jumps to zero.
The discreteness of the control parameter is not a technical defect, but an essential feature
of this case: the Hurwitz classification excludes finite-dimensional unital real normed
division algebras between dimension 8 and any successor, so there is no intermediatedimensional object within the ladder available for continuous interpolation.
The reading of the spectral channel is: under norm-weighted encoding, for the four division levels of real numbers, complex numbers, quaternions, and octonions, the injection
gap is identically the theoretical maximum 1; for the sedenion level, the appearance of
zero divisors makes the left-multiplication operator singular, and the injection gap jumps
to 0. The value range theorem further gives that, within the category of this paper, the
value range of the injection gap is {0, 1}, each object taking only one of the two, and there
is no object in the category taking an intermediate value. Hence “not passing through
an intermediate state” acquires a precise meaning: it is not that the decay curve is steep,
but that there is simply no intermediate value in the value range. The necessity of the
jump comes from the Hurwitz blockade and the classification of absolute-valued algebras:
there is no normed division algebra between dimension 8 and any successor, and the loss
of norm multiplicativity occurs irreversibly beyond dimensions 1, 2, 4, 8. Any continuous
parameter curve whose semantics is “approaching truncation”, if its values always lie
within the category of this paper, can only have injection gap 0 or 1, and cannot vary
continuously from 1 to 0; if it leaves the category of this paper, then its spectral values
no longer describe the algebraic structure within the ladder, but only reflect the choice
of external encoding or weight scheme.
The reading of the information channel is: at every level of the Cayley–Dickson ladder,
divisibility is equivalent to the invertibility of the left-multiplication operator for nonzero
elements, and also equivalent to traceability in the left-multiplication sense. Upon entering the sedenion level, there exist nonzero left zero divisors. Take a standard zero divisor;
its left-multiplication kernel has dimension 4. This means that there exist 4 linearly independent input directions that are all compressed into the same output after one left
multiplication. The output no longer distinguishes these input directions, and difference
information is annihilated inside the map. Under the counting-cell model at resolution
scale δ, the indistinguishability in the kernel directions gives a lower bound on the macro33

## PDF page 34

scopic entropy loss, which diverges logarithmically as δ tends to zero; while the arithmetic
cost of a single multiplication is bounded. Therefore the information-conservation inequality fails for every finite efficiency parameter. The failure is dimensional: unbounded
loss versus bounded cost.
The reading of the symmetry channel is: the full R-algebra automorphism group of
the octonions is the fourteen-dimensional exceptional Lie group G2 , and this is the full
automorphism group; there is no larger algebraic automorphism group that simultaneously preserves the octonion multiplication structure and the norm. The geometry of
the debris is recorded by two spaces that must be distinguished (Chapter 9): the normalized annihilation-pair space Z(S) is diffeomorphic to G2 , and the zero-divisor carrier
space ZD(S) is diffeomorphic to the Stiefel manifold V2 (R7 ). The debris of failure, as
the totality of annihilation events, and the surviving symmetry are the same geometric
object; projecting this identity to the carrier layer gives the classical Borel principal bundle SU (2) → Z(S) → ZD(S), with the dimension count 14 = 11 + 3 closing, and each
fiber geometrically realized as the unit sphere of the corresponding left-multiplication
kernel. This paper does not claim any isomorphism between the G2 residual and truncation residuals in other domains, nor does it conflate G2 with the sedenion automorphism
group.
The reading of irreversibility is: starting from the sedenions, a sequence consisting
only of algebraic internal operations cannot have as its endpoint a sixteen-dimensional
normed division algebra. Internal operations include taking subalgebras, taking two-sided
quotients, and taking isomorphic images, none of which raises dimension. If the endpoint
dimension is still 16, then the dimension must remain 16 at every step; if some step takes
a two-sided quotient and the dimension remains 16, then the ideal is the zero ideal and
the quotient is isomorphic to the sedenions themselves; but the sedenions contain nonzero
zero divisors and are not a division algebra. If a proper two-sided ideal is nonzero, then
any nonzero element in it is non-invertible. Therefore a proper two-sided quotient must
destroy divisibility. If the endpoint dimension is less than 16 and the endpoint is a division
algebra, then by the Hurwitz classification the endpoint must belong to the real numbers,
complex numbers, quaternions, or octonions. The endpoint of internal repair can only
be a division level after dimension reduction; it is impossible to restore divisibility at
the sixteen-dimensional level. The arithmetic root of irreversibility is that after the loss
of structural axioms, the difference information required for inversion has already been
annihilated inside the multiplication map; this paper does not extrapolate to the second
law of thermodynamics.
Boundaries and risks are as follows. First, the specific numerical value of the injection
gap depends on the weight scheme; what is invariant across encodings is the instability
mode, not the specific numerical value of the plateau. Second, the dimension-retraction
formula is a conditional corollary, whose effective range is limited to 16 ≤ DH ≤ 20, and
whose constant calibration depends on framework-level information-coupling bookkeeping; before the calibration is established it does not constitute a theorem. Third, the
isomorphism boundary is closed: this paper does not claim an isomorphism between the
residual of this truncation and truncation residuals in other domains. Fourth, specific
zero-divisor coordinates and specific values of alternativity failure depend on the sign
convention; but structural conclusions such as the existence of zero divisors, the kernel
dimension 4, the failure of alternativity at the sedenion level, the canonical count of standard two-term zero divisors, the value range of the injection gap, the G2 rigid anchoring,
and the carrier–event dichotomy are convention-independent. Fifth, the kernel dimension
34

## PDF page 35

4 and the principal-bundle fiber dimension 3 are numerically different, and their precise
relation is dim ker Lx = dim π −1 (x) + 1, the fiber being the unit sphere of the kernel space
(Chapter 9); this paper does not regard 4 and 3 as the same quantity.
Within the above boundaries, the conclusions of this paper can be graded as follows.
What is definitely established includes: the enumeration of division levels by the Hurwitz classification; the failure of norm multiplicativity at the sedenion level; the existence
of zero divisors and the canonical count of standard two-term zero divisors; the leftmultiplication kernel dimension 4; Aut(O) ∼
= G2 ; the diffeomorphism of the normalized
annihilation-pair space with G2 and of the zero-divisor carrier space with V2 (R7 ); the
principal-bundle structure SU (2) → Z(S) → ZD(S); the impossibility of internal repair.
What is conditionally established includes: the failure of the information-conservation
inequality under the counting-cell model and finite efficiency parameters; its validity depends on the resolution-scale partition and the bounded-cost assumption. What remains
to be independently established includes: the framework-level calibration on which the
dimension-retraction formula depends. What is not claimed includes: residual isomorphism, thermodynamic extrapolation, conflation of kernel dimension with fiber dimension, and conflation of left and right zero divisors.
Within the scope of this paper, algebraic hard truncation thereby becomes the prototype of all truncation types: discrete, irreversible, and carrying a rigid residual. Discreteness comes from the level indexing of the control parameter and the Hurwitz blockade;
irreversibility comes from internal operations not raising dimension and from the annihilation of difference information; the rigid residual is the fourteen-dimensional exceptional
Lie group G2 , whose geometric incarnation is the manifold formed by the totality of
annihilation events—the normalized annihilation-pair space—connected to the elevendimensional failing-element space by an SU (2) principal bundle. The termination of the
Cayley–Dickson ladder is not an accidental halt of a symbolic machine, but an honest
phase transition.

Remark
The translation of this article was done by DeepSeek, and the mathematical modeling
and the literature review of this article were assisted by DeepSeek.

References
[1] Hurwitz, Adolf. “Über die Komposition der quadratischen Formen von beliebig vielen Variabeln.” Nachrichten von der Gesellschaft der Wissenschaften zu Göttingen,
Mathematisch-Physikalische Klasse (1898): 309–316.
[2] Baez, John C. “The Octonions.” Bulletin of the American Mathematical Society 39,
no. 2 (2002): 145–205.
[3] Conway, John H., and Derek A. Smith. On Quaternions and Octonions: Their Geometry, Arithmetic, and Symmetry. Natick, MA: A K Peters, 2003.
35

## PDF page 36

[4] Albert, A. A. “Quadratic Forms Permitting Composition.” Annals of Mathematics
(2) 43, no. 1 (1942): 161–177.
[5] Albert, A. A. “Absolute-Valued Algebraic Algebras.” Bulletin of the American Mathematical Society 55, no. 8 (1949): 763–768.
[6] Schafer, Richard D. An Introduction to Nonassociative Algebras. New York: Academic Press, 1966.
[7] Moreno, Guillermo. “The Zero Divisors of the Cayley-Dickson Algebras over the
Real Numbers.” Boletı́n de la Sociedad Matemática Mexicana (3) 4, no. 1 (1998):
13–28.
[8] Biss, Daniel K., Daniel Dugger, and Daniel C. Isaksen. “Large Annihilators in
Cayley-Dickson Algebras.” Communications in Algebra 36, no. 2 (2008): 632–664.
[9] Reggiani, Silvio. “The Geometry of Sedenion Zero Divisors.” arXiv:2411.18881, 2024.
[10] Fiedler, Miroslav. “Algebraic Connectivity of Graphs.” Czechoslovak Mathematical
Journal 23, no. 98 (1973): 298–305.
[11] Shannon, Claude E. “A Mathematical Theory of Communication.” Bell System Technical Journal 27 (1948): 379–423, 623–656.
[12] Moufang, Ruth. “Alternativkörper und der Satz vom vollständigen Vierseit (D9 ).”
Abhandlungen aus dem Mathematischen Seminar der Universität Hamburg 9 (1933):
207–222.
[13] Jacobson, Nathan. “Composition Algebras and Their Automorphisms.” Rendiconti
del Circolo Matematico di Palermo (2) 7 (1958): 55–80.
[14] Zorn, Max. “Alternativkörper und quadratische Systeme.” Abhandlungen aus dem
Mathematischen Seminar der Universität Hamburg 9 (1933): 395–402.
[15] Kleinfeld, Erwin. “Simple Alternative Rings.” Annals of Mathematics (2) 58 (1953):
544–547.

Appendix A: Machine-Check Protocol and Results
Protocol. The algebras are generated by an exact integer implementation of the Cayley–
Dickson doubling procedure, with formulas as in Chapter 2. The initial value is A0 = R,
iterated to k = 4. All computations are performed in exact integer arithmetic, without
floating-point approximation, with the sole exception of the singular value decomposition,
which uses double precision and reports 15 significant digits. The verification steps are
as follows.
(1) For k = 1, 2, 3, take 200 random integer vectors with coefficients in [−2, 2] and
verify that N (xy) = N (x)N (y) holds exactly.

36

## PDF page 37

(2) For k = 4, take 3000 vectors of the same type (pseudorandom sampling, seed
20261005) and count the number of multiplicativity failures: 2969 failures, 31 exact
successes. Failure is the rule rather than the exception: exact equality of norm multiplicativity at k = 4 occurs only in low-measure special cases (for example, one factor is
a real scalar, or both factors lie in some octonion subalgebra), and the sampling hit rate
tends to one hundred percent as the coefficient range is enlarged.
(3) Exhaustively enumerate all ordered pairs in the range of two-term imaginary
elements ±ei ± ej (1 ≤ i < j ≤ 15), 176,400 pairs in total, and test whether the product
is zero, obtaining 1,344 annihilating ordered pairs. The merge protocol is the same
as the enumeration-merge step of Proposition 2.3: the canonical representative takes
the carrier x0 = ep + eq+8 (1 ≤ p < q ≤ 7) and the partner takes the four support
types under the fixed sign convention (the lowest-index component is taken positive),
giving 21 × 4 = 84 representatives; each representative generates 16 ordered pairs via
independent sign changes of the two carrier components (4 ways), interchange of the
two carrier components (2 ways), and overall sign change of the partner (2 ways). The
machine-check output satisfies 1,344 = 84 × 16, the fibers are pairwise disjoint, and they
exhaust all annihilating ordered pairs. The parametrization takes exhaustive merging as
authoritative; the structural count is explained by the Fano line constraints as 21×4 = 84,
where {i, j} ⊂ {1, . . . , 7} has 21 choices, the partner support type is determined by
the Fano line through {i, j}, and the second index satisfies the +8 copy relation: er+8
corresponds to the second copy of er .
(4) On all triples of imaginary basis elements, verify whether the alternativity identity
[x, y, z] = −[y, x, z] holds for k = 3, and locate the minimal counterexample for k = 4.
For k = 3 it holds on 3000 random trials and on all basis-element triples; for k = 4 it
fails on the basis triple (e1 , e10 , e4 ): [e1 , e10 , e4 ] = 2e15 ̸= 0, while [e10 , e1 , e4 ] = 0. All
672 (ordered) failing instances on basis-element triples have the form of one side being
zero; there is no case in which the two associators are negatives of each other and both
nonzero. The specific sign assignments are governed by the machine-check output of the
recursive convention of B.3.
(5) For k = 4, verify the power-associativity identity on 500 random elements; it
holds.
(6) For a sample unit element a ∈ O, compute all singular values of La ; for the standard zero divisor a = e1 +e10 , compute the dimension of ker La . For sample unit elements
a ∈ O, all singular values of La equal 1; for the standard zero divisor, dim ker La = 4,
and the kernel space is spanned by the four two-term elements e4 − e15 , e5 + e14 , e6 − e13 ,
e7 + e12 , consistent with the general result of Biss–Dugger–Isaksen. The precise relation between this kernel dimension and the principal-bundle fiber dimension is given in
Chapter 9: the fiber is the unit sphere of the kernel space.
All steps of this protocol are executed under the recursive convention locked in Appendix B; the consistency of B.2 and B.3 is the consistency of the locked convention
itself.
Verification guide. Each step of the protocol involves only the construction of the
integer multiplication table, exhaustive search, and one double-precision singular value
decomposition; executing the above steps in any standard numerical environment should
yield structurally identical results (the per-group values of the random sampling step vary
with the seed, and the failure count is stable at normal sampling sizes; the numbers 84,
16, and 1,344 in step (3) are deterministic outputs independent of sampling).

37

## PDF page 38

Appendix B: Explicit Gauge and Integer Implementation of the Cayley–Dickson Construction
B1 Sign Convention and Convention Locking
The basis elements of the algebras Ak at each level are denoted by e0 , . . . , en−1 , n = 2k ,
e0 = 1. The basis elements of the second copy in the doubling Ak+1 = Ak × Ak are
numbered en+i = ei en (0 ≤ i ≤ n − 1), i.e. the new imaginary unit en multiplies the old
basis elements on the right. The involution is defined recursively by x̄ = (ā, −b) when
x = (a, b), which gives: for i ≥ 1, ei is imaginary, e2i = −1, and for i, j ≥ 1, i ̸= j,
ei ej = −ej ei . The norm is defined recursively by N ((a, b)) = N (a) + N (b), and the
relation N (x) = xx̄ is preserved at all levels.
Convention locking. The sole authority for the encoding convention of this paper is
the doubling recursion formula of Section 2.1; the Fano hand-calculation table of B.2 is
a derived table of that recursion, and the orientation is always governed by the recursive
output; the pseudocode of B.3 is an executable implementation of that recursion. If
any specific coordinate assertion conflicts with the hand-calculation table, the recursive
output prevails.

B2 Exact Recursion of Multiplication and Fano Hand-Calculation
Table
¯ da + bc̄).
(a, b)(c, d) = (ac − db,
All four terms on the right-hand side are operations within the lower-level algebra Ak ;
hence, after pushing down level by level to A0 = R, the entire multiplication table is
determined by integer addition, subtraction, and multiplication, without any floatingpoint operation.
The multiplication at the octonion level (k = 3) can be quickly hand-computed using
the Fano plane. The seven imaginary basis elements e1 , . . . , e7 correspond to the seven
points of the Fano plane. The seven Fano lines (triples) and their orientations are as
follows; the orientation is governed by the output of the recursion locked in B.1. A
positive sign means cyclic order as listed: ei ej = ek , ej ek = ei , ek ei = ej ; a negative sign
means the reverse direction.
Line 1 (1, 2, 3) positive
Line 2 (1, 4, 5) positive
Line 3 (1, 6, 7) negative
Line 4 (2, 4, 6) positive
Line 5 (2, 5, 7) positive
Line 6 (3, 4, 7) positive
Line 7 (3, 5, 6) negative
This table has been machine-checked to satisfy norm multiplicativity on all octonion
basis-element pairs, and it agrees item by item with the recursion of B.3. Unlisted basiselement pairs are given by anticommutativity ei ej = −ej ei and e2i = −1.

38

## PDF page 39

B3 Description of the Integer Implementation Algorithm
Construct A0 : basis [e0 ], multiplication table T0 = [[+e0 ]] (stored as signed basis elements).
For k = 0, 1, 2, 3: n = 2k . The new table T ′ has size 2n × 2n. Let the involution sign
factor be s(j) = +1 (j = 0) or −1 (j ≥ 1), and let off(±em ) = ±em+n (the basis index is
shifted by n as a whole, with the sign preserved). The four blocks are assigned as follows:
T ′ [i][j] = T [i][j] corresponds to (a, 0)(c, 0) = (ac, 0)
T ′ [i][n + j] = off(T [j][i]) corresponds to (a, 0)(0, d) = (0, da)
T ′ [n + i][j] = off(s(j) · T [i][j]) corresponds to (0, b)(c, 0) = (0, bc̄)
¯ 0)
T ′ [n + i][n + j] = −s(j) · T [j][i] corresponds to (0, b)(0, d) = (−db,
Here s(j) · (±em ) only flips the sign and does not touch the index. The four blocks
cover all four quadrants of the doubling formula; the involution sign is uniformly carried
by s(j), and the second-copy shift is uniformly carried by off.
Verification statement: the above four-block assignment agrees cell by cell with the
doubling formula of Section 2.1 over the full table range for k = 1, 2, 3, 4 (machinechecked); the Fano table of B.2 is the derived table of this recursion at k = 3, agreeing
item by item.

B4 Determinism of the Zero-Divisor Enumeration
On the multiplication table generated by B.3, exhaustively enumerate all ordered pairs
of two-term imaginary elements ±ei ± ej (︁(1 )︁≤ i < j ≤ 15) and test whether the product
is zero. The number of single elements is 15
× 4 = 420, and the number of ordered pairs
2
is 176,400. The product test is an integer table lookup, with no rounding. The output
of this exhaustive enumeration is the source of the result of step (3) of Appendix A.

Appendix C: Combinatorial Counting of the Moreno
Criterion and the Structure of the Kernel
C1 Derivation Sketch of the Moreno Criterion
Write a sedenion as (x, y) according to the doubling at k = 3, with x, y ∈ O. The product
is (x, y)(u, v) = (xu − v̄y, vx + yū). Let (x, y) be nonzero. If one of x, y is zero, then
by the divisibility of O, the product being zero forces (u, v) = 0, so no zero divisor is
produced. Hence a zero divisor must have both x, y nonzero. The norm computation
gives N ((x, y)(u, v)) = N (xu − v̄y) + N (vx + yū); using the norm multiplicativity of the
octonions and the Moufang identities to expand term by term, one can prove that the
cross terms are exactly inner products of the form Re(xūv · · · ), and that they vanish
if and only if x, y have equal norm and are orthogonal (in the imaginary sense). The
criterion is necessary and sufficient, and for two-term elements (ei + ej , ek ± el ) it can be
directly verified by hand.

39

## PDF page 40

C2 Structure of the 84 Count
A standard two-term zero divisor requires x = ei and y = ej to
(︁7)︁be two distinct imaginary
basis elements; the unordered pair {i, j} ⊂ {1, . . . , 7} has 2 = 21 choices. For each
√
such unordered pair, there are exactly 4 annihilating partners b = (ek ± el )/ 2, whose
indices (k, l) are determined by the line structure of the Fano plane: the quaternion triple
containing a (the Fano line through {i, j}) gives the real-part constraint on b, and the
remaining structure gives the two signs ±. The structural count is 21 × 4 = 84.
The correspondence with the parametrization of step (3) of Appendix A is as follows.
The canonical representative chooses {i, j} on the imaginary part {1, . . . , 7} of the octonions and {k, l} determined by the Fano line. The actual sedenion standard zero divisors
are obtained by the second-copy correspondence: er+8 corresponds to the second copy of
er , i.e. adding 8 to the index means taking the corresponding basis element in the second
copy. For example, in (e1 + e10 )(e4 − e15 ) = 0, e10 is the second copy of e2 , and e15 is the
second copy of e7 . After exhaustive enumeration of 176,400 ordered pairs and merging
by canonical equivalence, the resulting 84 annihilation relations agree with the 21 × 4
structure. 84 is the canonical representative count of this two-term subfamily, not the
total number of zero divisors; all zero divisors are parametrized by the Moreno criterion
by V2 (R7 ) and form a continuum.

C3 Structural Derivation of the Kernel Dimension
Take a standard zero divisor a = (x, y), where x, y are equal-norm orthogonal imaginary octonions, ∥a∥2 = 2. The kernel ker La is the right annihilator ann(a). By the
multiplication formula of B.1, (u, v) ∈ ker La is equivalent to the octonion system
vx = −yū.

xu = v̄y,

Using y −1 = −y (since ∥y∥ = 1), the first equation gives v̄ = −(xu)y, i.e. v is uniquely
determined by u; substituting into the second equation gives a single octonion equation for
u. The left-hand side of this equation is linear in u (the Moufang identities guarantee that
linearity is not destroyed by the associator), so the solution set is an R-linear subspace.
For a = e1 +e10 , the machine check directly gives four two-term annihilating elements:
(e1 +e10 )(e4 −e15 ) = 0, (e1 +e10 )(e5 +e14 ) = 0, (e1 +e10 )(e6 −e13 ) = 0, (e1 +e10 )(e7 +e12 ) = 0.
These four are linearly independent and directly form a basis of ker La , so the kernel
dimension is 4, consistent with the general result of Biss–Dugger–Isaksen. All annihilation
partners are exactly the two-term elements among the ± combinations of this basis; there
is no fourth basis vector that needs to be registered as a non-two-term combination.
Chapter 9 further gives the geometric reading: the unit sphere of annihilation partners for
a fixed carrier a is exactly the fiber at a of the principal bundle SU (2) → Z(S) → ZD(S).

40

## PDF page 41

Appendix D: Formal Declaration of the Information
Conservation Inequality
D1 Objects and Notation
Let G be a finite-state network: the node set is a discretization of the state space X,
and the resolution scale δ > 0 partitions X into Nδ counting cells, with cell volume ∼ δ d
(d the dimension of the state space). A macroscopic state is a union of cells, and the
macroscopic entropy is defined as Sδ (G) = ln Nδ (macroscopic state). The dynamics is
a map T : X → X (in this paper: a single left multiplication La , one arithmetic step,
bounded cost). The total constraint amount C(G) is defined as the number of basic
arithmetic steps required to execute the dynamics (a single multiplication has C = 1; the
multiplication cost expanded along the k-level doubling recursion is a bounded function
of k). The efficiency parameter η > 0 is the upper bound on information loss allowed
per unit cost. The information-conservation inequality states: there exists a constant η
(depending only on the encoding scheme, not on δ) such that for all δ,
Sδ (G′ ) ≥ Sδ (G) − ηC(G),

G′ = T (G).

D2 Verification at the Division Levels
When K is a division algebra, La is injective, and T maps cells bijectively to cells (norm
multiplicativity guarantees that the cell volume of the image is not distorted), so Nδ is
unchanged and the loss is 0 ≤ ηC. The inequality holds with margin, and η need only
be any finite positive value. La is an isometry, and the difference between the image of a
cell and a cell is only in the boundary layer, with entropy difference o(1), which does not
affect the bijective count.

D3 Failure at the Sedenion Level
Take a to be a standard zero divisor, with dim ker La = 4 (Appendix C.3). A 4dimensional ball of radius R in ker La contains ∼ cR4 δ −4 cells under the δ-partition
(c a constant depending only on the dimension), all compressed into a single output cell.
Hence
Sδ (G) − Sδ (G′ ) ≥ 4 ln(1/δ) + ln(cR4 ) − o(1) = 4 ln(1/δ) + O(1).
The right-hand side diverges logarithmically as δ → 0, while ηC(G) = η · 1 is a fixed
constant. Therefore for any finite η, taking δ < exp(−(η + O(1))/4) makes the inequality
fail. The failure does not require a constructive counterexample sequence; it is a direct
corollary of dimension (unbounded loss versus bounded cost). The phrase “fails for every
finite efficiency parameter” in the information channel of Chapter 6 of the main text is
the condensed statement of this paragraph.

41

## PDF page 42

D4 Boundaries of Use
This appendix declares only the above instantiation of the inequality under algebraic
encoding; the form of the inequality under other encodings (geometric, informationtheoretic) may differ, and this paper does not use it beyond these boundaries.

Appendix E: Comparative Computation of Encoding
Weight Dependence
E1 Control Group Settings
The numerical value of the injection gap ∆ depends on the weight scheme. Let there be
three schemes: (α) norm weighting (the scheme of the main text), with basis edge weight
= 1; (β) uniform down-weighting, with the operator globally rescaled La ↦→ (1/n)La , n
the dimension; (γ) geometric down-weighting, with the operator rescaled La ↦→ 2−k La
(at level k).

E2 Comparison Results
Scheme (α): ∆(R) = ∆(C) = ∆(H) = ∆(O) = 1, ∆(S) = 0 (Chapter 4, spectral gap
catastrophe theorem).
Scheme (β): the singular values are globally rescaled by 1/n, so ∆β (WK ) = ∆(WK )/n2 .
Values: 1, 1/4, 1/16, 1/64, 0. The ladder then presents the appearance of “level-by-level
asymptotic decay to 0”, but this is a pure weight artifact: the operators at each level
have not been changed in any structural information, only the scale has been recalibrated
by the square of the dimension.
Scheme (γ): rescaling by 2−k , so ∆γ (WK ) = 4−k ∆(WK ). Values: 1, 1/4, 1/16, 1/64,
0. It coincides completely with (β) at every level k ≤ 3, and still jumps to 0 at S. The
coincidence is not accidental: when n = 2k , 1/n2 = 4−k , and the two down-weightings
are two bodies of the same calibration function.

E3 Conclusion
Under every weight scheme that respects the internal symmetry of each level (the isometry of the left-multiplication family), the division levels always take the same positive
constant cw (cw varies with the scheme), and the S level always takes 0; intermediate
values appear only in schemes where the symmetry is artificially broken, in which case ∆
measures the weight itself rather than the algebraic structure. The cross-scheme invariant
is the instability mode: the five-valued structure “four plateaus + one jump”. The value
sequences of schemes (β) and (γ) are pointwise identical, showing that the “asymptotic
decay appearance” can be produced entirely by the calibration function, independently
of structural degeneration; this constitutes the quantitative support for item (1) of Chap-

42

## PDF page 43

ter 10 and serves as the defining content of the order parameter in the phase-transition
coordinates of Chapter 5.

Appendix F: Compilation of Background Facts and
Lemmas on G2
F1. Aut(O) preserves the norm, so Aut(O) ⊆ O(8); connectedness gives Aut(O) ⊆
SO(8). Aut(O) is a fourteen-dimensional simple Lie group, isomorphic to the exceptional
group G2 , of rank 2.
F2. The seven-dimensional fundamental representation of G2 is realized as the natural
action on the imaginary part Im(O) of O; G2 acts transitively on S 6 ⊂ Im(O), and transitively on the set of unit tangent vectors, which is diffeomorphic to the Stiefel manifold
V2 (R7 ). dim V2 (R7 ) = 2 · 7 − 3 = 11.
F3. Principal bundle SU (2) → G2 → V2 (R7 ): fiber dimension dim SU (2) = 3, base
dimension 11, total 3 + 11 = 14 = dim G2 , and the dimension count closes. This bundle
gives the dimension decomposition of G2 ; the kernel dimension 4 and the fiber dimension
3 are numerically different, and their precise relation is given in Chapter 9: the fiber is
the unit sphere of the left-multiplication kernel for a fixed carrier, dim ker = dim fiber+1.
F4. The normalized annihilation-pair
space of the sedenions Z(S) = {(x, y) ∈ S × S :
√
xy = 0, ∥x∥ = ∥y∥ = 2} (the norm-1 convention differs only by a global positive
scaling) is diffeomorphic to G2 ; Reggiani further proved that it is isometric to G2 under
the natural reduced left-invariant metric. The zero-divisor carrier space ZD(S) (the normnormalized space of left zero-divisor elements) is diffeomorphic to V2 (R7 ). Under the
identification of Theorem 9.1, the projection (x, y) ↦→ x is the classical Borel principal
bundle SU (2) → G2 → V2 (R7 ), and each fiber is realized as the unit sphere of ker Lx .
F5. The number fourteen is not a tuning parameter: it is the dimension of the symmetry group preserving all structures of O (multiplication, norm, involution), uniquely
determined by the Hurwitz blockade; any larger norm-preserving symmetry must destroy
the multiplication structure.

43

## PDF page 44

Appendix G: Literature Verification Registration Table
Number

Literature

[1]

Hurwitz 1898, Nachrichten von der Gesellschaft der
Wissenschaften zu Göttingen, Math.-Phys. Klasse, 309–316

[2]
[3]
[4]
[5]
[6]
[7]

[8]
[9]

[10]
[11]
[12]
[13]
[14]
[15]

Verification Status

Baez 2002, Bull. Amer. Math. Soc. 39(2), 145–205
Conway & Smith 2003, On Quaternions and Octonions, A K
Peters
Albert 1942, Annals of Mathematics (2) 43(1), 161–177
Albert 1949, Bull. Amer. Math. Soc. 55(8), 763–768
Schafer 1966, An Introduction to Nonassociative Algebras,
Academic Press
Moreno 1998, Bol. Soc. Mat. Mexicana (3) 4(1), 13–28

Biss, Dugger & Isaksen 2008, Communications in Algebra
36(2), 632–664
Reggiani 2024, arXiv:2411.18881

Fiedler 1973, Czechoslovak Mathematical Journal 23(98),
298–305
Shannon 1948, Bell System Technical Journal 27, 379–423,
623–656
Moufang 1933, Abhandlungen aus dem Mathematischen
Seminar der Universität Hamburg 9, 207–222
Jacobson 1958, Rendiconti del Circolo Matematico di Palermo
(2) 7, 55–80
Zorn 1933, Abhandlungen aus dem Mathematischen Seminar
der Universität Hamburg 9, 395–402
Kleinfeld 1953, Annals of Mathematics (2) 58, 544–547

Volume, issue, pages consistent with
the original
Volume, issue, pages consistent
Publisher and edition consistent
Volume, issue, pages consistent
Volume, issue, pages consistent
Edition consistent
Journal name, volume, issue, pages
consistent (pages per journal version
13–28)
Volume, issue, pages consistent
arXiv number, author (Silvio Reggiani),
and v1 submission date (2024-11-28)
verified at terminal; abstract
conclusions (Z(S) isometric to G2 ,
ZD(S) isometric to V2 (R7 )) agree with
the citation in Chapter 9 of this paper
Dual numbering of old volume 23 and
new volume 98 consistent
Volume and pages consistent
Volume, issue, pages consistent
Volume, issue, pages consistent
Volume, issue, pages consistent
Volume, issue, pages consistent

Table 2: Literature verification registration table.

44
