Source: https://zenodo.org/api/records/22016333
PDF sha256: 48a4b2385b3ef16872c4c4a3e5d2d3972ee752bb8dfe10f091b7b6745553ef7b
License: CC-BY-4.0
Language: eng
Fidelity: machine-gated

# Transcription of skiouris-2026-algebraic-hiddenness.pdf

Transcription of `skiouris-2026-algebraic-hiddenness.pdf` in this directory, 32 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-32 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Algebraic Hiddenness in the Sedenion Algebra:
Characterization, Spectral Structure, and Bundle Topology
Kyriakos John Skiouris
Agingo Corporation
Charlotte, NC
kyriakos@agingo.com
August 2026

Abstract
The 16-dimensional sedenion algebra S, obtained as the fourth Cayley–Dickson doubling
of the reals, is the lowest level of the CD tower at which the composition law fails and zero
divisors appear. We develop a complete algebraic and geometric theory of its zero-divisor
locus and the rank-4 vector bundle naturally associated with it.
The principal results are geometric. (i) The Bundle Nontriviality Theorem — the
rank-4 kernel bundle over G2 /SU(2) carries a nonzero Z/2 secondary characteristic class
(the aphanic twist), and parallel transport around certain geodesic loops is −id. (ii) The
Holonomy Decomposition Theorem — given the previously established holonomy U (2) =
(U (1) × SU(2))/Z2 of the canonical connection, the SU(2) factor is the restriction to the
kernel of the lifted G2 -stabilizer action, and the U (1) factor is generated, at the basepoint,
by a commutator of right-multiplications Re1 , Re2 . (iii) The Rℓ Centrality Theorem — that
U (1) generator is the restriction to the kernel of a single global ambient operator Rℓ on S,
with [Rℓ , L⊤
p Lp ] = 0 on the entire imaginary locus, of which the aphanic locus is a strict
subset. (iv) The CD-Tower Recursion Theorem — that centrality identity is level-uniform,
holding at every Cayley–Dickson level by an argument using only flexibility, inner-product
duality, and the conjugation anti-homomorphism property.
These rest on an algebraic foundation which we develop by a self-contained route, and
whose structural conclusions are in substantial part already known. (v) A Pfaffian route
to the annihilator structure of S: the identity Pf(Lp ) = −(∥p∥2 )2 T , with T = 4∥a∥2 ℜ(b)2 +
4⟨a, b⟩2 + (∥a∥2 − ∥b∥2 )2 , certified by exact finite computation, from which follow in one
derivation the zero-divisor criterion of Moreno and Khalil–Yiu, the {0, 4} nullity dichotomy
of Moreno and Biss–Dugger–Isaksen, and the determinant factorization det Lp = (∥p∥2 )4 T 2
obtained independently by Koebisu. (vi) A derivation of the 4-8-4 spectral structure of the
2
4
2 8
2
4
Gram operator Gp = L⊤
p Lp — Spec(Gp ) = {(∥p∥ − σ) , (∥p∥ ) , (∥p∥ + σ) }, σ = 2∥x ∧ y∥
— by an associator-norm argument; this is equivalent to the eigenvalue computation of
Biss–Christensen–Dugger–Isaksen for their operator Ma = (1/∥a∥2 )Lā La , and is used here
as the structural input to the bundle and holonomy results above. (vii) A unified eleven-step
proof of the Aphanic Characterization Theorem, the doubly-imaginary case of the criterion
in (v). All proofs are constructive and certified by self-contained C++17 probes.

Keywords: sedenion, Cayley–Dickson algebra, zero divisor, non-associative algebra, Berry
phase, G2 , kernel bundle, holonomy.
MSC: 17A35, 17A75, 53C29, 55R25, 17D05.
arXiv categories: math.RA (primary), math.DG, math.AT (cross-list).

1

## PDF page 2

Contents
1 Introduction
1.1 The Cayley–Dickson Tower and Its Fourth Doubling . . . . . . . . . . . . . . . .
1.2 Setting and Conventions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
1.3 Principal Results . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
1.4 Computational Reproducibility . . . . . . . . . . . . . . . . . . . . . . . . . . . .
1.5 Relationship to the Companion Paper . . . . . . . . . . . . . . . . . . . . . . . .

3
3
3
3
4
4

2 Setup and Conventions
2.1 The Cayley–Dickson Tower . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
2.2 Properties Surviving Each Doubling . . . . . . . . . . . . . . . . . . . . . . . . .
2.3 Standing Assumptions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
2.4 A Note on Empirical Certification . . . . . . . . . . . . . . . . . . . . . . . . . .
2.5 Definitions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

5
5
5
5
6
6

3 The Aphanic Characterization Theorem
7
3.1 Setup . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 7
3.2 The Proof . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 7
3.3 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 10
4 The 4-8-4 Spectral Theorem

10

5 The Sedenion Annihilator Fourfold Theorem
5.1 Elementary reductions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
5.2 The determinant and Pfaffian identity . . . . . . . . . . . . . . . . . . . . . . . .
5.3 The annihilator criterion . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
5.4 The kernel dimension is exactly four . . . . . . . . . . . . . . . . . . . . . . . . .
5.5 G2 -transport and the canonical kernel . . . . . . . . . . . . . . . . . . . . . . . .
5.6 The nullity spectrum and left–right equality . . . . . . . . . . . . . . . . . . . . .
5.7 The main theorem . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
5.8 An exact certificate for the Pfaffian identity . . . . . . . . . . . . . . . . . . . . .

11
12
12
13
14
14
16
16
17

6 Bundle Topology and the Aphanic Twist
6.1 The Aphanic Locus as a Homogeneous Space . . . . . . . . . . . . . . . . . . . .
6.2 G2 -Equivariance of the Kernel Bundle . . . . . . . . . . . . . . . . . . . . . . . .
6.3 Bundle Nontriviality . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

18
18
18
19

7 Algebraic Identification of the Holonomy Factors
7.1 Setup . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
7.2 The stabilizer inside g2 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
7.3 The decomposition theorem . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
7.4 Remarks . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

20
20
21
21
22

8 Algebraic R ℓ Centrality
8.1 Statement . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
8.2 Strict strengthening over the fiberwise statement . . . . . . . . . . . . . . . . . .
8.3 Proof . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
8.4 Numerical certification . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
8.5 Remarks . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

23
23
24
24
26
26

2

## PDF page 3

9 The Cayley–Dickson Tower Recursion
9.1 Imaginary Left–Right Symmetry . . . . . . . . . . . . . . . . . . . . . . . . . . .
9.2 Recursive Rℓ Centrality . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
9.3 Empirical Confirmation at the Chingon Level . . . . . . . . . . . . . . . . . . . .

26
27
27
28

10 Open Frontiers
10.1 The SU(2)L –Fano Identification . . . . . . . . . . . . . . . . . . . . . . . . . . . .
10.2 Universality of the Holonomy Classification at Higher Levels . . . . . . . . . . . .
10.3 Global Integrability of the Kernel Distribution . . . . . . . . . . . . . . . . . . .
10.4 Two-Layer Theorem Beyond Dim 32 . . . . . . . . . . . . . . . . . . . . . . . . .
10.5 Connection to Twistor Theory . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

28
29
29
29
29
29

3

## PDF page 4

1

Introduction

1.1

The Cayley–Dickson Tower and Its Fourth Doubling

The Cayley–Dickson construction generates an infinite tower of real ∗-algebras
R ⊂ C ⊂ H ⊂ O ⊂ S ⊂ P ⊂ C≂ ⊂ · · ·
by recursive application of the doubling formula
¯ da + bc̄).
(a, b)(c, d) = (ac − db,

(1)

The first three doublings produce C, H, and O. By Hurwitz’s theorem (Baez, 2002; Hurwitz,
1898), no fourth normed real division algebra exists; the sedenion algebra S, the fourth doubling,
is no longer a division algebra. The composition law ∥ab∥ = ∥a∥ ∥b∥ fails in S, and zero divisors
appear: there exist p, q ∈ S \ {0} with pq = 0. The locus of left zero divisors is the focus of this
paper.
The standard view of this transition is degradative. The associative, normed, and division
properties are progressively shed at each doubling, and beyond O what remains is regarded as an
algebraic curiosity rather than a structural object of independent interest. We take a different
view. The zero-divisor locus of S is a smooth real submanifold with a G2 -symmetry, the kernel of
the multiplication operator Lp has constant dimension 4 on this locus, and the family of kernels
assembles into a topologically nontrivial vector bundle whose canonical connection has holonomy
in the unitary group U (2) (established previously; see Section 7, where that identification is taken
as given and its factors are located inside so(K)). What from one perspective is a degeneracy,
from another is a precisely defined geometric object.

1.2

Setting and Conventions

We work throughout with the canonical recursive Cayley–Dickson multiplication (1). Handwritten multiplication tables based on Fano-plane bookkeeping are not equivalent to the recursive
formula in detail (sign conventions differ in 24 of the 2 × 8 × 7 = 112 products that are nonzero),
and the choice matters: which pairs (x, y) produce a zero divisor depends on the sign convention.
The recursive product is the canonical choice in the modern non-associative algebra literature
(Baez, 2002; Schafer, 1966) and is the convention used throughout. All numerical certifications
referenced in this paper are run with this convention.
For a ∈ S, La , Ra : S → S denote the 16 × 16 real matrices of left and right multiplication by
a. We write p = (x, y) ∈ S for p = ι1 (x) + ι2 (y) where ι1 , ι2 are the canonical inclusions of O
into the two halves of S. The inner product on S is the natural one inherited from O, and the
imaginary subspace is Im(S) = Im(O) ⊕ O · ℓ.

1.3

Principal Results

1. Section 3 (Characterization). A unified algebraic proof that dim ker Lp > 0 if and only
if ∥x∥ = ∥y∥ and ⟨x, y⟩ = 0, with kernel dimension exactly 4 in that case (Theorem 3.1).
The proof passes through the keystone identity (∥x∥2 − ∥y∥2 )2 + 4⟨x, y⟩2 = 0 whose
non-negative summands force both conditions simultaneously.
2
2. Section 4 (4-8-4 Spectrum). The Gram operator Gp = L⊤
p Lp has spectrum {(∥p∥ −
4
2
8
2
4
σ) , (∥p∥ ) , (∥p∥ + σ) } with σ = 2∥x ∧ y∥ (Theorem 4.1). The aphanic locus is exactly
where the lowest block hits 0, and the iconic “4-8-4” multiplicities arise from the Cayley–
Dickson block decomposition combined with an isometry-difference structure of the offdiagonal block.

4

## PDF page 5

3. Section 5 (Annihilator Fourfold Theorem). The full left-annihilator dichotomy for an
arbitrary nonzero sedenion, dropping the standing assumption that the second component
is imaginary (Theorem 5.14): a nonzero real part forces a trivial kernel; for imaginary
p = (a, b) with b ∈ O arbitrary, ker Lp ̸= 0 if and only if ℜ(b) = 0, ⟨a, b⟩ = 0, and |a| = |b|,
with dimR ker Lp exactly 0 or 4 and dimR ker Lp = dimR ker Rp . The mechanism is the
determinant identity det Lp = (|p|2 )4 T 2 with T = 4|a|2 ℜ(b)2 + 4⟨a, b⟩2 + (|a|2 − |b|2 )2 ,
whose three non-negative summands force the criterion; the value 4 is the multiplicity
count of Theorem 3.1.
4. Section 6 (Bundle Topology). The aphanic locus V ∼
= G2 /SU(2) is an 11-dimensional
homogeneous space, and the kernel map Φ : V → Gr(4, S) realizes a rank-4 real bundle
K → V with Aut(O)-equivariance. We show that K carries a nonzero secondary Z/2
characteristic class (Theorem 6.4), and the canonical connection has holonomy −id around
certain geodesic loops (Theorem 6.6).
5. Section 7 (Holonomy Decomposition). The full holonomy algebra at the basepoint
decomposes algebraically as u(2) = u(1)R ⊕ su(2)L , where the su(2) factor is the restriction
to K of the lifted action of the SU(2) ⊂ G2 stabilizer of the basepoint, and the u(1) factor
is generated by a commutator of right-multiplications by orthogonal quaternionic units
(Theorem 7.2).
6. Section 8 (Rℓ Centrality). The u(1) generator at the basepoint is, up to scale, the
restriction to K of a single ambient operator Rℓ on S, and [Rℓ , Gp ] = 0 on the entire
imaginary locus (Theorem 8.1). The aphanic conditions ∥x∥ = ∥y∥ and ⟨x, y⟩ = 0 are not
used in the proof.
7. Section 9 (Tower Recursion). The centrality identity is the S-level instance of a towerwide recursion that propagates via the Imaginary L–R Symmetry Lemma LX̄ LX = RX̄ RX
on Im(An ), a flexibility corollary preserved at every CD level (Theorem 9.1). The pathionlevel analogue is proven algebraically (Theorem 9.3), and empirical confirmation is given
at the chingon level.
8. Section 10 (Open Frontiers). A summary of the questions left open: persistence of
the holonomy classification at higher CD levels, the algebraic identification of the SU(2)
factor with right-multiplication by Fano units, and the global integrability of the kernel
distribution.

1.4

Computational Reproducibility

Every algebraic claim in the paper is accompanied by a self-contained C++17 probe that
verifies the claim numerically at machine precision. The probes are released as a single archive
(the_aphanic_toy) with no external dependencies, building under both MSVC and GCC. Where
proofs are algebraic, the probes serve as referee-checkable witnesses; where proofs are empirical
(e.g., dim 64 chingon recursion), the probes are the primary evidence. All residuals reported in
the paper are reproducible to within IEEE double rounding.

1.5

Relationship to the Companion Paper

The framework paper (Skiouris, 2026) formalizes the Aphanics cognitive monitoring framework
at the abstract level: the kernel of an internal action operator, the curvature of its variation, and
the topological winding number of closed dialectical arcs. That paper is a framework proposal
whose structural credibility depends on the existence of at least one concrete algebraic setting in
which the abstract axioms are realized. The present paper supplies that setting — the sedenion
algebra — with full proofs of the realization. The two papers are independent in their formal
5

## PDF page 6

content but mutually reinforcing: the abstract framework explains why the specific algebraic
results matter, and the specific algebraic results demonstrate that the framework is not vacuous.

2

Setup and Conventions

2.1

The Cayley–Dickson Tower

We adopt the notation An for the nth Cayley–Dickson algebra, with A0 = R and An+1 =
An ⊕ An · ℓn+1 where ℓ2n+1 = −1 and ℓn+1 anticommutes with every imaginary element of An .
Multiplication is given by recursive application of (1). The first six levels are
A0 = R,

A1 = C,

A2 = H,

A3 = O,

A4 = S,

A5 = P,

A6 = C≂.

We write ℓ for ℓ4 = e8 , the doubling generator of S over O, which is identified with the basis
element with index 8 when S is given the standard ordered basis {1, e1 , . . . , e15 }. Similarly
ℓ5 = e16 is the doubling generator of P over S, and ℓ6 = e32 that of C≂ over P.

2.2

Properties Surviving Each Doubling

The properties enjoyed by An degrade at each doubling. The relevant landmarks are recorded in
Table 1.
Table 1: Algebraic properties surviving each Cayley–Dickson doubling.
Property

R

C

H

O

S

P

higher

Commutative
Associative
Alternative
Composition
Division algebra
Flexible
Conjugation ∗-anti-hom.

yes
yes
yes
yes
yes
yes
yes

yes
yes
yes
yes
yes
yes
yes

no
yes
yes
yes
yes
yes
yes

no
no
yes
yes
yes
yes
yes

no
no
no
no
no
yes
yes

no
no
no
no
no
yes
yes

no
no
no
no
no
yes
yes

The key observation underpinning the present work is that the two properties surviving every
doubling — flexibility a(ba) = (ab)a and the conjugation anti-homomorphism ab = b̄ā — are
sufficient to drive the Rℓ centrality identity (Section 8) and its tower-wide recursion (Section 9).
The characterization theorem of Section 3 relies on the stronger composition and alternativity
properties, which is why the dim-16 case is the lowest level at which a nontrivial kernel exists.

2.3

Standing Assumptions

Unless stated otherwise:
• p = (x, y) ∈ S with x, y ∈ Im(O) (the imaginary locus).
• Lp , Rp ∈ End(S) are the matrices of left and right multiplication, in the standard ordered
basis.
• Gp = L⊤
p Lp is the Gram operator.
• σ = 2∥x ∧ y∥ = 2 ∥x∥2 ∥y∥2 − ⟨x, y⟩2 is the wedge norm.
√

• V̂ ⊂ S is the aphanic cone, defined by ∥x∥ = ∥y∥, ⟨x, y⟩ = 0, and x, y linearly independent;
it is invariant under positive scaling.
6

## PDF page 7

• V := {p ∈ V̂ : ∥x∥ = ∥y∥ = 1} is the aphanic locus, the unit-normalized slice of the cone
(equivalently ∥p∥2 = 2). Unless stated otherwise, V denotes this unit-normalized
locus throughout. The spectral statements are homogeneous in ∥p∥ and are stated on
the cone V̂; the bundle and holonomy statements are stated on V.
• K → V is the rank-4 real bundle Kp = ker Lp .

2.4

A Note on Empirical Certification

Throughout the paper, results are classified as PROVEN (algebraic proof, no appeal to numerics),
EMPIRICAL (verified numerically at high precision but without a known algebraic proof), or
CONFIRMED (stated by other authors, verified here). Each theorem statement records its
status. Empirical residuals quoted are worst-case across the cited number of random samples.
These three words are reserved for claims. The computational witnesses carry a separate
vocabulary: code reports PASS, FAIL, or CERTIFIED, and never PROVED or PROVEN. A
certification must state its epistemic basis — either the numerical tolerance at which it was
evaluated, or exact, when the result is established by exhaustive finite verification or by exact
arithmetic. Tier vocabulary belongs to claims, witness vocabulary to computation, and the two
are never interchanged.
The separation is not a concession. Where bilinearity reduces an identity to finitely many
basis triples and every one is checked exactly, this manuscript may correctly say the identity is
proved: the program reports what it did, exact certification, and the mathematics states what
follows from it, a proof. Saying both, in their own words, is more precise than letting one word
carry both senses.

2.5

Definitions

The following three terms are used throughout, including inside formal statements. Each is fixed
here, before first such use.
Definition 2.1 (Aphanic element). Let p = (x, y) ∈ S under the Cayley–Dickson identification
S = O ⊕ O. Then p is aphanic if x, y ∈ Im(O) and
∥x∥ = ∥y∥ ̸= 0,

⟨x, y⟩ = 0,

where ⟨·, ·⟩ and ∥ · ∥ are the standard Euclidean inner product and norm on O ∼
= R8 .
Definition 2.2 (Aphanic locus). The aphanic locus is the set A := { p ∈ S : p is aphanic } of all
elements satisfying Definition 2.1.
Definition 2.3 (Aphanic twist). The aphanic twist of the kernel bundle K → V is its secondary
characteristic class
[K] ∈ H 6 (V; Z/2) ∼
= Z/2.
Remark 2.4. The name records what the definition does not: an aphanic p is a nonzero element
of S annihilated, in the sense made precise in Section 3, by the very operator its own system
uses to measure it. The two conditions of Definition 2.1 — equal norms and orthogonality —
are exactly the conditions under which that annihilation occurs, and Definition 2.2 names the
resulting set.
Definition 2.3 names an invariant, not a phenomenon. The aphanic twist exists as a class
whatever its value; whether it vanishes is the content of Theorem 6.4, and the associated −id
transport behaviour is treated separately where it is established. The definition deliberately
does not identify the class with a holonomy character.

7

## PDF page 8

3

The Aphanic Characterization Theorem

This section gives an unbroken algebraic derivation of the central theorem of the framework: for
p = (x, y) ∈ S with x, y ∈ Im(O), the left-multiplication operator Lp has a nontrivial kernel if and
only if ∥x∥ = ∥y∥ and ⟨x, y⟩ = 0; and when these conditions hold, dim ker Lp = 4. The proof is an
eleven-step chain from the Cayley–Dickson multiplication formula through composition-algebra
identities, Artin’s theorem, and the seven-dimensional associator norm formula, terminating in
the single algebraic identity (∥x∥2 − ∥y∥2 )2 + 4⟨x, y⟩2 = 0 whose non-negative summands force
both conditions simultaneously.

3.1

Setup

The sedenion algebra is constructed by Cayley–Dickson doubling of the octonions, S = O ⊕ O · ℓ,
with multiplication
(
¯ da + bc̄),
(a, b)(c, d) = ac − db,

a, b, c, d ∈ O.

(2)

Here ¯· denotes octonion conjugation: if u = u0 + uim with u0 ∈ R and uim ∈ Im(O), then
ū = u0 − uim . The inner product on O is ⟨u, v⟩ = 12 (uv̄ + vū)0 , and that on S extends as
∥(x, y)∥2 = ∥x∥2 + ∥y∥2 .
For a ∈ O, denote by La , Ra : O → O the 8 × 8 real matrices representing left and right
multiplication by a. Let C denote the 8 × 8 conjugation matrix. Three identities will be used
repeatedly:
1. Composition law: La Lā = Ra Rā = ∥a∥2 I for all a ∈ O.
2. Skew-adjointness on imaginaries: for a ∈ Im(O), LTa = −La and RaT = −Ra .
3. Alternativity: O is alternative, so the associator [u, v, w] := (uv)w − u(vw) is totally
antisymmetric in its three arguments on Im(O).
In particular, for a ∈ Im(O) we have ā = −a, so the composition law specialises to L2a =
−∥a∥2 I and Ra2 = −∥a∥2 I.
Theorem 3.1 (Aphanic Characterization). Let p = (x, y) ∈ S with x, y ∈ Im(O). Then
ker Lp ̸= {0} ⇐⇒ ∥x∥ = ∥y∥ and ⟨x, y⟩ = 0.

(3)

When these conditions hold, dim ker Lp = 4.

3.2

The Proof

The proof proceeds in eleven steps. Each step is a theorem of elementary octonion algebra; none
appeals to numerical evidence.
Step 1 (Cayley–Dickson Block Structure). Applying (2) to p = (x, y) acting on z = (u, v)
gives p · z = (xu − v̄y, vx + yū). For x, y ∈ Im(O) the operator on (u, v)T is the 16 × 16 block
matrix
(
)
Lx −Ry C
Lp =
.
(4)
Ly C
Rx
Here v̄y = Ry C(v) and yū = Ly C(u); the sign on Ry C comes from (2) directly.

8

## PDF page 9

Step 2 (Diagonal Blocks of the Gram Operator). Let G := LTp Lp . Using (4) and the
transpose identities for imaginary generators:
GT L = LTx Lx + (Ly C)T (Ly C) = (−Lx )(Lx ) + C T LTy Ly C
= −L2x + C(−Ly )(Ly )C = ∥x∥2 I + C∥y∥2 I C = ∥p∥2 I.
Here we used L2x = −∥x∥2 I and C 2 = I. The same computation for the bottom-right block gives
GBR = ∥p∥2 I.
Step 3 (Off-Diagonal Block F ). The top-right block of G is
GT R = LTx (−Ry C) + (Ly C)T Rx = (−Lx )(−Ry C) + C T (−Ly )Rx = Lx Ry C − CLy Rx =: F.
The bottom-left block is GBL = F T . Therefore
(

G = ∥p∥ I16 + W,

W =

2

0
FT

F
0

)

.

(5)

Step 4 (The Associator Identity for F ). Direct expansion: for any z ∈ O,
F (z) = Lx Ry C(z) − CLy Rx (z) = x(z̄ y) − y(zx).
The second term simplifies: y(zx) = zx · ȳ = (x̄z̄)ȳ. For imaginary x, y, x̄ = −x and ȳ = −y,
hence y(zx) = ((−x)z̄)(−y) = (xz̄)y. Therefore
F (z) = x(z̄ y) − (xz̄) y = [x, z̄, y],

(6)

the octonion associator with middle argument z̄.
Step 5 (Vanishing on Q: Artin’s Theorem). Let Q := span{1, x, y, xy}. We first address
a degeneracy. If x, y are linearly dependent (y = cx for some c ∈ R), then p = x · (1, c) lies in an
associative C-like subalgebra of S in which Lp is invertible. Both sides of (3) fail trivially.
Assume henceforth x, y linearly independent. Then dim Q = 4. By Artin’s theorem, the
subalgebra of O generated by any two elements is associative; Q is such a subalgebra. For z ∈ Q,
z̄ ∈ Q, and the associator [x, z̄, y] = 0 since Q is associative. By (6),
F ∣Q ≡ 0,
∣

dim(ker F |Q ) ≥ 4.

(7)

Step 6 (Associator Norm on Q⊥ ). Let Q⊥ ⊂ O denote the four-dimensional orthogonal
complement of Q. Since Q is closed under conjugation, so is Q⊥ ; for imaginary z ∈ Q⊥ ,
z̄ = −z ∈ Q⊥ , and z satisfies ⟨z, 1⟩ = ⟨z, x⟩ = ⟨z, y⟩ = ⟨z, xy⟩ = 0.
Lemma 3.2 (Associator Norm on Q⊥ ). For every z ∈ Q⊥ ,
∥
∥
(
)
∥[x, z, y]∥2 = 4 ∥z∥2 ∥x∥2 ∥y∥2 − ⟨x, y⟩2 .

(8)

Proof. On Im(O) ∼
= R7 define the cross product u × v := 12 (uv − vu) = Im(uv) for u, v ∈ Im(O),
so that uv = −⟨u, v⟩ + u × v. Lagrange’s identity:
∥u × v∥2 = ∥u∥2 ∥v∥2 − ⟨u, v⟩2 .

(9)

A direct calculation using alternativity (Baez, 2002; Schafer, 1966) gives the associator-tripleproduct identity
(
)
[x, z, y] = 2 z × (x × y) − ⟨z, x⟩ y + ⟨z, y⟩ x
(10)
9

## PDF page 10

for x, y, z ∈ Im(O). Since z ∈ Q⊥ implies z ⊥ x and z ⊥ y, the last two terms vanish, giving
[x, z, y] = 2 z × (x × y). Apply (9) with u = z, v = x × y:
∥z × (x × y)∥2 = ∥z∥2 ∥x × y∥2 − ⟨z, x × y⟩2 .
The second term vanishes: x × y = Im(xy) = xy + ⟨x, y⟩ · 1, so ⟨z, x × y⟩ = ⟨z, xy⟩ + ⟨x, y⟩⟨z, 1⟩,
and both summands are zero (z ⊥ xy, z ⊥ 1). Therefore ∥z ×(x×y)∥2 = ∥z∥2 (∥x∥2 ∥y∥2 −⟨x, y⟩2 )
by (9) again, and ∥[x, z, y]∥2 = 4 times this.
The middle-argument z̄ in (6) is −z for imaginary z, and Q⊥ is closed under conjugation.
Hence ∥F (z)∥2 = ∥[x, z, y]∥2 for z ∈ Q⊥ :
∥F (z)∥2 = 4 ∥z∥2 ∥x∥2 ∥y∥2 − ⟨x, y⟩2 ,
(

)

z ∈ Q⊥ .

(11)

Step 7 (Singular Values of F ). Combining (7) and (11): F vanishes on the four-dimensional
subspace Q, and acts on Q⊥ by a fixed scalar multiple of an isometry.
√ The squared singular values
⊥
2
2
2
of F on Q are all equal to 4(∥x∥ ∥y∥ −⟨x, y⟩ ). Writing σ := 2 ∥x∥2 ∥y∥2 − ⟨x, y⟩2 = 2 ∥x∧y∥:
SV(F ) = {04 , σ 4 }.

(12)

Note σ = 0 ⇐⇒ x, y linearly dependent, already handled in Step 5.
(

Step 8 (Spectrum of W ).

For an anti-diagonal block matrix W =

0
FT

)

F
, the eigenvalues
0

of W are ± SV(F ). Therefore
Spec(W ) = {−σ 4 , 08 , σ 4 }.

(13)

Step 9 (Spectrum of G). From (5): G = ∥p∥2 I + W , so
Spec(G) =

(∥p∥2 − σ)4 , (∥p∥2 )8 , (∥p∥2 + σ)4 .

{

Step 10 (The Keystone Identity).

}

(14)

Since Lp has full rank iff G = LTp Lp has trivial kernel,

ker Lp ̸= {0} ⇐⇒ 0 ∈ Spec(G) ⇐⇒ ∥p∥2 = σ.
Squaring and rearranging:
(∥x∥2 − ∥y∥2 )2 + 4⟨x, y⟩2 = 0

(15)

Both summands are non-negative; their sum is zero iff each vanishes individually: ∥x∥ = ∥y∥
and ⟨x, y⟩ = 0.
Step 11 (Multiplicity). When the aphanic conditions hold, (14) has smallest eigenvalue
0 with algebraic (hence geometric, G symmetric positive semidefinite) multiplicity exactly 4.
Therefore dim ker G = 4. Since G = LTp Lp acts on a finite-dimensional inner product space,
ker Lp = ker G, giving dim ker Lp = 4.
□

10

## PDF page 11

3.3

Summary

The chain of implications:
(4) ⇒

(5)

⏟⏞⏞⏟

⏟⏞⏞⏟

CD

composition

⇒

Artin

(6)
⏟⏞⏞⏟

=⇒ (7)

expansion

Lemma 3.2

=⇒

⏟⏞⏞⏟

(12) ⇒ (14) ⇒ (15) ⇒ Theorem 3.1.
⏟⏞⏞⏟

F |Q =0

SV(F )

⏟⏞⏞⏟

Spec(G)

⏟⏞⏞⏟

keystone

Every link is algebraic. The composition law, skew-adjointness, and alternativity are the
three pillars of O used at the dim-8 level. Artin’s theorem handles the Q-kernel. The associator
norm formula handles the Q⊥ singular values. The keystone (∥x∥2 − ∥y∥2 )2 + 4⟨x, y⟩2 = 0 forces
both aphanic conditions from a single equation.
Corollary 3.3 (Determinant Formula). det(Lp )2 = det(G) = (∥p∥2 − σ)4 (∥p∥2 )8 (∥p∥2 + σ)4 ,
with σ = 2∥x∧y∥. In particular det(Lp ) = 0 exactly on the aphanic locus, and for ∥x∥ = ∥y∥ = 1,
⟨x, y⟩ = 0 the non-singular part gives leading coefficient 24 · 42 = 256 = 44 .
Remark 3.4 (On the Higher Cayley–Dickson Levels). The proof above relies on three octonionlevel identities: the composition law La Lā = ∥a∥2 I, alternativity (Artin’s theorem in particular),
and skew-adjointness on imaginaries. Of these, the composition law fails at the next CD level
P = S ⊕ S · ℓ′ (this is precisely why S has zero divisors); alternativity fails in S already. What
survives at every level is flexibility a(ba) = (ab)a and the inner-product duality ⟨ab, c⟩ = ⟨b, āc⟩.
The recursion theorem of Section 9 extends the Rℓ -centrality result to every CD level using only
these preserved identities.

4

The 4-8-4 Spectral Theorem

The proof of Theorem 3.1 produces, as intermediate output, a complete description of the
spectrum of the Gram operator Gp = L⊤
p Lp in the imaginary locus. We promote that output to
a named theorem, since it is the structural workhorse of the holonomy and centrality results
that follow.
Theorem 4.1 (4-8-4 Spectral Theorem). Let p = (x, y) ∈ S with x, y ∈ Im(O) linearly
independent, and let σ := 2∥x ∧ y∥. Then the Gram operator Gp = L⊤
p Lp has spectrum (with
multiplicities)
{
}
Spec(Gp ) = (∥p∥2 − σ)4 , (∥p∥2 )8 , (∥p∥2 + σ)4 .
(16)
For aphanic p (∥x∥ = ∥y∥ and ⟨x, y⟩ = 0), the spectrum reduces to
Spec(Gp ) =

0 , (∥p∥2 )8 , (2∥p∥2 )4 .

{ 4

}

(17)

For unit aphanic observers (∥x∥ = ∥y∥ = 1, hence ∥p∥2 = 2), the spectrum is the iconic
{04 , 28 , 44 }.
Proof. This is equation (14) from the proof of Theorem 3.1, extracted as a stand-alone
result.√ The aphanic-locus form follows by substituting ∥x∥ = ∥y∥ and ⟨x, y⟩ = 0 into
σ = 2 ∥x∥2 ∥y∥2 − ⟨x, y⟩2 , giving σ = 2∥x∥∥y∥ = ∥p∥2 .
Remark 4.2 (Structural reading of the multiplicities). The multiplicities 4 + 8 + 4 = 16 partition
S as dim S. The 8 in the middle is the diagonal ∥p∥2 · I part of the CD-block decomposition
(Step 2 of the characterization proof). The two 4’s are the symmetric pair ±σ contributed by the
off-diagonal block W in (5); they originate from the eight singular values of W being arranged
as ± SV(F ) with SV(F ) = {04 , σ 4 }. Equivalently, the 4’s come from the four-dimensional
associative subalgebra Q = span{1, x, y, xy} and its rank-4 complement Q⊥ inside O.

11

## PDF page 12

Corollary 4.3 (Determinant and Pfaffian). det(Lp )2 = (∥p∥2 )8 (∥p∥2 − σ)4 (∥p∥2 + σ)4 =
(
)4
(∥p∥2 )8 (∥p∥2 )2 − σ 2 . In particular det(Lp ) = 0 exactly on the aphanic locus. Normalizing
∥x∥ = ∥y∥ = 1 (so that ∥p∥2 = 2 and σ → 2) and writing ε := ∥p∥2 − σ for the approach
parameter, the displayed √
identity gives det(Lp )2 = 28 ε4 44 + O(ε5 ), so the leading non-vanishing
coefficient of det(Lp ) is 28 · 44 = 24 · 42 = 44 = 256. The sign is determined, not a choice: Lp
is real skew-symmetric of even order for imaginary p, so det Lp = Pf(Lp )2 ≥ 0 (Lemma 5.3,
proved in Section 5 below), and the positive root is the only admissible one. The normalization
is needed: without it the coefficient is (∥p∥2 )4 (∥p∥2 + σ)2 .
Corollary 4.4 (Spectral projectors). For aphanic p the three eigenvalues {0, ∥p∥2 , 2∥p∥2 } are
distinct, so each spectral projector of Gp is a polynomial in Gp given by Lagrange interpolation.
In particular the kernel projector πp onto ker Lp is
πp =

(Gp − ∥p∥2 I)(Gp − 2∥p∥2 I)
1
(Gp − ∥p∥2 I)(Gp − 2∥p∥2 I).
=
2
2
(0 − ∥p∥ )(0 − 2∥p∥ )
2∥p∥4

Any operator commuting with Gp commutes with every spectral projector, hence in particular
with πp .
The spectral projector formula above is what allows Theorem 8.1 (Rℓ centrality on Gp ) to
descend to a centrality identity on πp , recovering the original fiberwise centrality statement as a
corollary.
Remark 4.5 (Status). PROVEN. Equivalent to (14) from Section 3.

5

The Sedenion Annihilator Fourfold Theorem

The Characterization Theorem 3.1 and the spectral result of Section 4 were stated for a doubly
imaginary generator p = (x, y) with x, y ∈ Im(O). Two natural questions are left open by
that hypothesis. First, what happens when the second component is permitted a real part, i.e.
p = (a, b) with a ∈ Im(O) but b ∈ O arbitrary? Second, what is the left-annihilator behaviour
of a completely general nonzero sedenion, including those with nonzero real part? This section
answers both. The outcome is a single clean dichotomy for every nonzero p ∈ S, together with
the exact left-nullity spectrum and the equality of left and right nullities. We refer to the
combined statement as the Annihilator Fourfold Theorem (Theorem 5.14).
Relation to prior work. The zero divisors of the sedenions have been studied previously from
a set-theoretic and structural standpoint. In proposing their programme, Biss et al. (2008, §1)
observed that the zero-divisor loci of the Cayley–Dickson algebras should prove geometrically
interesting objects in their own right, and set the understanding of the topological properties
of ZD(An ) as an aim. The present paper carries that programme out for the A4 stratum, by
studying not the locus alone but the rank-4 kernel bundle it carries. Moreno (1998) determined
the zero-divisor locus of the Cayley–Dickson algebras over R, showing in particular that a doubly
imaginary p = (x, y) is a zero divisor exactly when ∥x∥ = ∥y∥ and ⟨x, y⟩ = 0 (the two-condition
criterion, re-proved by elementary means as Theorem 3.1), and described the resulting variety
as stratified by the rank of Lp . Cawagas (2004) analysed the subalgebra structure of S and the
organisation of its zero divisors.
The structural facts recorded in this section are, individually, known. Moreno (1998, Cor. 1.17)
proved that dimR ker Lp is always a multiple of 4, and gave the zero-divisor criterion (Moreno,
1998, Cor. 2.14); the criterion was obtained independently by Khalil and Yiu (1997, Thm. 3.2.3).
Biss et al. (2008, Thm. 1.2) proved the bound dim Ann(x) ≤ 2n − 4n + 4, which at n = 4
equals 4, re-proved Moreno’s divisibility (Biss et al., 2008, Thm. 9.8), and stated the resulting
{0, 4} dichotomy for S explicitly (Biss et al., 2008, §12), where the criterion appears as (Biss
et al., 2008, Prop. 12.1). In particular the imaginarity of both components — and with it
12

## PDF page 13

ℜ(b) = 0 — is a consequence of the zero-divisor hypothesis in that work (Biss et al., 2008,
Lem. 9.4), not an assumption; we claim no improvement on that point. Equality of the left and
right annihilators holds in every Cayley–Dickson algebra (Biss et al., 2008, Cor. 9.3), which
subsumes dimR ker Lp = dimR ker Rp for S. The determinant factorization below was obtained
independently, in the equivalent form det Lv = D14 D22 , by Koebisu (2026, Thm. 3.7).
What this section contributes is therefore not the dichotomy but the route: a single Pfaffian
identity, Pf(Lp ) = −(∥p∥2 )2 T , certified by an exact finite computation, from which the criterion,
the determinant factorization det Lp = (∥p∥2 )4 T 2 , and the nullity value all follow in one derivation.
That route is what carries into the spectral and bundle-theoretic material of Sections 4 and 6,
which is independent of the algebraic literature cited here.
Throughout, Lp , Rp ∈ End(S) are left and right multiplication in the standard ordered basis
{1, e1 , . . . , e15 }, ℓ = e8 is the doubling generator, and p = (a, b) abbreviates p = ι1 (a) + ι2 (b)
with a, b ∈ O. We write | · | for the octonion norm, ⟨ , ⟩ for its inner product, and ℜ(b) = b0
for the real part. We use repeatedly the three octonion-level facts collected in Section 3.1: the
composition law Lu Lū = Ru Rū = |u|2 I, skew-adjointness of imaginary generators (L⊤
w = −Lw
for w ∈ Im(O)), and alternativity of O. At the sedenion level we use only the two tower-universal
properties of Table 1: flexibility and the inner-product duality ⟨uv, w⟩ = ⟨v, ūw⟩, which gives
L⊤
p = Lp̄ on S.

5.1

Elementary reductions

Lemma 5.1 (Real part forces trivial kernel). If p ∈ S has ℜ(p) ̸= 0, then Lp is invertible; in
particular ker Lp = {0}.
Proof. Write p = p0 + pim with p0 = ℜ(p) ∈ R and pim ∈ Im(S), so Lp = p0 I + Lpim . The
inner-product duality ⟨uv, w⟩ = ⟨v, ūw⟩ holds at every Cayley–Dickson level and gives L⊤
q = Lq̄
for all q ∈ S; for q = pim ∈ Im(S) we have q̄ = −q, hence L⊤
=
−L
.
Thus
L
is
a
real
skewpim
pim
pim
symmetric matrix, and its eigenvalues are purely imaginary. The eigenvalues of Lp = p0 I + Lpim
are therefore of the form p0 + iµ with µ ∈ R, none of which vanishes when p0 ̸= 0. Hence
det Lp ̸= 0.
By Lemma 5.1 the annihilator problem is nontrivial only for imaginary p, i.e. ℜ(p) = 0. In
our coordinates ℜ(p) = ℜ(a), so p imaginary means a ∈ Im(O) while b ∈ O is unconstrained.
This is the precise sense in which the present section generalizes Section 3: there b was assumed
imaginary, here it is arbitrary. We record the two genuinely degenerate cases.
Lemma 5.2 (Degenerate components). Let p = (a, b) be imaginary and nonzero.
(i) If a = 0 then ker Lp = {0}.
(ii) If b = 0 then ker Lp = {0}.
Consequently ker Lp ̸= {0} forces a ̸= 0 and b ̸= 0.
Proof. If a = 0 then p = (0, b) with b ̸= 0, and the product (0, b)(u, v) = (−v̄b, bū) vanishes only
if v̄b = 0 and bū = 0; since O is a division algebra and b ̸= 0, this forces v = u = 0. If b = 0 then
p = (a, 0) with a ∈ Im(O) \ {0}, and (a, 0)(u, v) = (au, va) vanishes only if au = va = 0, again
forcing u = v = 0 in the division algebra O. Both kernels are trivial.

5.2

The determinant and Pfaffian identity

For imaginary p the operator Lp is skew-symmetric, so its determinant is a perfect square and is
controlled by the Pfaffian.

13

## PDF page 14

Lemma 5.3 (Skew-symmetry and the Pfaffian). For imaginary p ∈ S, L⊤
p = −Lp , so Lp is a
16 × 16 real skew-symmetric matrix and
det Lp = Pf(Lp )2 ,

(18)

where Pf is the Pfaffian taken in the standard ordered basis.
Proof. L⊤
p = Lp̄ = L−p = −Lp as in Lemma 5.1. Identity (18) is the defining property of the
Pfaffian of a skew-symmetric matrix of even order.
Introduce the four real invariants of p = (a, b),
I1 = |a|2 ,

D1 = ℜ(b),

D2 = ⟨a, b⟩,

D3 = |a|2 − |b|2 ,

|p|2 = |a|2 + |b|2 ,

(19)

and the nonnegative quantity
T = 4 |a|2 ℜ(b)2 + 4 ⟨a, b⟩2 + |a|2 − |b|2
(

)2

= 4I1 D12 + 4D22 + D32 .

(20)

Proposition 5.4 (Determinant/Pfaffian factorization). For every imaginary p = (a, b) ∈ S (that
is, a ∈ Im(O), b ∈ O),
Pf(Lp ) = − (|p|2 )2 T,

det Lp = (|p|2 )4 T 2 ,

hence

(21)

with T as in (20). Both sides are polynomials in the sixteen real coordinates of p; the displayed
sign of Pf is that of the standard ordered basis, while det Lp is independent of orientation.
The proof is given in Section 5.8 as an exact finite certificate of a polynomial identity: both
sides are G2 -invariant polynomials, the Pfaffian has total degree 8, and an exact evaluation on
a complete 9-point-per-variable grid in normal-form coordinates determines the identity over
Z. The certificate is purely algebraic (exact integer and modular arithmetic, no floating-point
inference). We first record that the identity is consistent with, and extends, the spectral results
already proved.
Remark 5.5 (Consistency with the 4-8-4 spectrum). When b ∈ Im(O) one has ℜ(b) = 0, so
D1 =√0 and T = (|a|2 − |b|2 )2 + 4⟨a, b⟩2 . A short computation gives T = (|p|2 )2 − σ 2 with
σ = 2 |a|2 |b|2 − ⟨a, b⟩2 the wedge norm of Section 4:
(|p|2 )2 − σ 2 = (|a|2 + |b|2 )2 − 4(|a|2 |b|2 − ⟨a, b⟩2 ) = (|a|2 − |b|2 )2 + 4⟨a, b⟩2 .
)2

)4

Hence (21) reduces to det Lp = (|p|2 )4 (|p|2 )2 −σ 2 , equivalently det(Lp )2 = (|p|2 )8 (|p|2 )2 −σ 2 ,
which is exactly the Determinant Corollary 3.3 obtained from the singular values SV(F ) =
{04 , σ 4 } in Step 7 of the proof of Theorem 3.1. The new content of Proposition 5.4 is the
additional term 4|a|2 ℜ(b)2 , which records the effect of a nonzero real part of b and is invisible to
the imaginary-locus analysis.
(

5.3

(

The annihilator criterion

Theorem 5.6 (Annihilator criterion). Let p = (a, b) ∈ S be imaginary and nonzero. Then
ker Lp ̸= {0} ⇐⇒ ℜ(b) = 0,

⟨a, b⟩ = 0,

|a| = |b|.

(22)

Proof. ker Lp ̸= {0} iff det Lp = 0. By Proposition 5.4, det Lp = (|p|2 )4 T 2 , so det Lp = 0 iff
|p|2 = 0 or T = 0. As p ̸= 0 we have |p|2 > 0, whence det Lp = 0 ⇐⇒ T = 0.
The expression T = 4|a|2 ℜ(b)2 + 4⟨a, b⟩2 + (|a|2 − |b|2 )2 is a sum of three nonnegative real
numbers, so T = 0 holds iff each summand vanishes:
|a|2 ℜ(b)2 = 0,

⟨a, b⟩ = 0,

|a|2 = |b|2 .

By Lemma 5.2, ker Lp ̸= {0} forces a ̸= 0, hence |a|2 > 0; the first equation then gives ℜ(b) = 0.
This proves the forward implication. Conversely, if ℜ(b) = 0, ⟨a, b⟩ = 0 and |a| = |b|, then every
summand of T vanishes, so T = 0, det Lp = 0, and ker Lp ̸= {0}.
14

## PDF page 15

Theorem 5.6 recovers the equivalence (3) of Theorem 3.1 without assuming b imaginary,
deriving ℜ(b) = 0 from the vanishing of T ; the same implication is established by a direct
argument in (Biss et al., 2008, Lem. 9.4). What is particular to the present derivation is its
source: the non-negativity of the three summands of the single invariant T , which is the analogue,
for the full invariant, of the keystone identity (15).

5.4

The kernel dimension is exactly four

When the criterion of Theorem 5.6 holds, the second component b is imaginary, ⟨a, b⟩ = 0,
|a| = |b|, and (by Lemma 5.2) a, b are nonzero, hence linearly independent. Thus (a, b) is an
aphanic pair in the sense of Section 3, and the dimension follows immediately from the algebraic
characterization.
Theorem 5.7 (Exact kernel dimension). If p = (a, b) is imaginary with ker Lp ̸= {0}, then
dimR ker Lp = 4.
Proof. By Theorem 5.6, ℜ(b) = 0, so b ∈ Im(O), and |a| = |b|, ⟨a, b⟩ = 0 with a, b linearly
independent. These are exactly the hypotheses of Theorem 3.1 (aphanic case), which gives
dimR ker Lp = 4.
The dimension claim therefore needs nothing beyond the octonion-level algebra of Section 3.
For completeness, and because it exposes the G2 -symmetry on which Section 6 rests, we record an
independent route to the same value: a quaternionic action on the kernel forces 4 | dimR ker Lp ,
and a single exact rank computation pins the value to 4.
Lemma 5.8 (Quaternionic operators on the kernel). Let p = (a, b) be imaginary with |a| = |b|
and ⟨a, b⟩ = 0, and define J1 = R(a,0) and J2 = R(b,0) on S, i.e. right multiplication by the
lower-embedded halves. Explicitly J1 (u, v) = (ua, vā) and J2 (u, v) = (ub, v b̄). Then, as operators
on S,
J12 = J22 = − |a|2 I,
J1 J2 + J2 J1 = 0.
(23)
Proof. Both identities are computed entirely within O, where multiplication is alternative, so
every step below is a legitimate octonion identity. For the squares, the right-alternative law
(wc)c = wc2 gives J12 (u, v) = ((ua)a, (vā)ā) = (ua2 , vā2 ); since a ∈ Im(O), a2 = −|a|2 and
ā2 = (−a)2 = −|a|2 , so J12 = −|a|2 I. The same computation for b gives J22 = −|b|2 I, and
|b| = |a| yields J22 = −|a|2 I.
For the anticommutator, consider the first component of (J1 J2 + J2 J1 )(u, v):
(ub)a + (ua)b = u(ba + ab) + [u, b, a] + [u, a, b] ,
(

)

where [u, c, c′ ] = (uc)c′ − u(cc′ ) is the octonion associator. In the alternative algebra O the
associator is alternating in all three arguments over the whole of O (not only on Im O), so
[u, b, a] + [u, a, b] = 0; and ab + ba = −2⟨a, b⟩ = 0 for orthogonal imaginary a, b. Hence the first
component vanishes. The second component, (v b̄)ā+(vā)b̄, vanishes by the identical computation
with ā = −a, b̄ = −b. Thus J1 J2 + J2 J1 = 0.
The relations (23) hold globally on S. To make ker Lp an H-module it remains to show J1 , J2
preserve the kernel; this is established in Proposition 5.11 below, by an explicit check at the
canonical element followed by G2 -transport.

5.5

G2 -transport and the canonical kernel

The automorphism group G2 = Aut(O) acts on S diagonally (Lemma 6.2): for φ ∈ G2 , the map
φ̃ = diag(φ, φ) is an algebra automorphism of S, whence
Lφ̃p = φ̃ Lp φ̃−1 ,

ker Lφ̃p = φ̃(ker Lp ),
15

φ̃(a, 0) = (φa, 0).

(24)

## PDF page 16

In particular dimR ker Lp is constant on G2 -orbits, and J1 , J2 are carried to the corresponding
operators at φ̃p.
Proposition 5.9 (Reduction to the canonical pair). Every imaginary p = (a, b) with |a| = |b| ̸= 0,
⟨a, b⟩ = 0, and b ∈ Im(O) is carried by a scaling and a diagonal G2 -automorphism to the canonical
element p0 = e1 + e10 = (e1 , e2 ). Consequently J1 , J2 preserve ker Lp for all such p if and only if
they preserve ker Lp0 .
Proof. Scaling p ↦→ p/|a| multiplies Lp by the positive scalar |a|, hence fixes ker Lp and rescales
J1 , J2 ; it reduces to the case |a| = |b| = 1, i.e. (a, b) an ordered pair of orthonormal imaginary
octonions. By Baez (2002, §4.1), G2 acts simply transitively on basic triples: for any two
ordered triples (f1 , f2 , f3 ) of imaginary octonions with fi2 = −1, ⟨f1 ⟩ ∼
= C, ⟨f1 , f2 ⟩ ∼
= H, and
f1 , f2 , f3 generating O, there is a unique φ ∈ G2 carrying the first to the second. An ordered
orthonormal imaginary pair (a, b) satisfies a2 = b2 = −1 and a ⊥ b, so ⟨a, b⟩ ∼
= H; choosing any
unit c orthogonal to the four-dimensional subalgebra ⟨1, a, b, ab⟩ (its orthogonal complement in
Im(O) has dimension 4, hence is nonempty) makes (a, b, c) a basic triple. Simple transitivity on
basic triples therefore specializes to transitivity on ordered orthonormal imaginary 2-frames, so
(a, b) = (φe1 , φe2 ) for some φ ∈ G2 , and φ̃p0 = p after scaling. The equivalence of the invariance
statements is then immediate from (24).
Lemma 5.10 (Exact canonical rank). At the canonical element p0 = e1 + e10 one has rank Lp0 =
12 and dimR ker Lp0 = 4. An explicit orthogonal basis of ker Lp0 is
e7 + e12 ,

−e6 + e13 ,

e5 + e14 ,

−e4 + e15 ,

(25)

equivalently, in half-coordinates, (e7 , e4 ), (−e6 , e5 ), (e5 , e6 ), (−e4 , e7 ). Writing v1 , v2 , v3 , v4 for
this basis, the operators J1 = R(e1 ,0) and J2 = R(e2 ,0) of Lemma 5.8 preserve ker Lp0 , acting by
J1 : v1 ↦→ v2 ↦→ −v1 , v3 ↦→ −v4 ↦→ v3 ;

J2 : v1 ↦→ v3 ↦→ −v1 , v2 ↦→ v4 ↦→ −v2 ,

(26)

so that J12 = J22 = −I and J1 J2 + J2 J1 = 0 on ker Lp0 .
Proof. The four vectors in (25) have pairwise disjoint support, hence are linearly independent,
and a direct application of the multiplication (2) verifies p0 ·v = 0 for each; thus dimR ker Lp0 ≥ 4.
For the reverse bound, the 12 × 12 leading minor of Lp0 on rows and columns {0, 1, . . . , 11}
has determinant 16 ̸= 0 (an exact integer computation), so rank Lp0 ≥ 12, i.e. dimR ker Lp0 ≤ 4.
The two bounds give equality. The action (26) is the direct evaluation of v ↦→ v · (e1 , 0) and
v ↦→ v · (e2 , 0) via (2): each image is again one of ±vi , so ker Lp0 is preserved, and (26) gives
J12 = J22 = −I and {J1 , J2 } = 0 on the kernel by inspection. Every entry of Lp0 is an integer
in {−1, 0, 1}, so the determinant, the kernel relations, and the action (26) are verified by exact
integer arithmetic with no rounding.
Combining the base-point value dimR ker Lp0 = 4 (Lemma 5.10) with the reduction to p0
(Proposition 5.9) and the orbit-invariance of dimR ker Lp from (24) gives a second proof that
dimR ker Lp = 4 for every imaginary p with nontrivial kernel, in agreement with Theorem 5.7.
This route is independent of the octonion-level multiplicity count of Section 3 on which Theorem 5.7 rests, although – unlike that primary argument – it does invoke the G2 -transitivity
fact of Proposition 5.9. Its value lies less in re-proving the dimension than in exposing the
quaternionic structure of the kernel, recorded next, which underlies the bundle of Section 6.
Proposition 5.11 (Quaternionic module structure). For imaginary p = (a, b) with ker Lp ̸= {0},
the operators J1 = R(a,0) and J2 = R(b,0) preserve ker Lp , which is thereby a left module over
the quaternion algebra generated by the identity and the normalized operators J1 /|a|, J2 /|a|.
Consequently 4 | dimR ker Lp .
16

## PDF page 17

Proof. Invariance holds at the canonical element p0 = e1 + e10 by the explicit action (26) of
Lemma 5.10: J1 , J2 map the kernel basis into itself. By Theorem 5.6 and Proposition 5.9,
any p with ker Lp ̸= {0} equals, after scaling, φ̃p0 for some φ ∈ G2 . Since φ̃(a, 0) = (φa, 0),
the canonical operators intertwine, φ̃ R(e1 ,0) φ̃−1 = R(φe1 ,0) and likewise for e2 ; together with
ker Lp = φ̃(ker Lp0 ) from (24), this carries the invariance at p0 to invariance at p. With the
global relations (23) (Lemma 5.8), the normalized J1 /|a|, J2 /|a| make ker Lp a finite-dimensional
real H-module; such a module is free over the division ring H, so 4 | dimR ker Lp .

5.6

The nullity spectrum and left–right equality

Theorem 5.12 (Nullity spectrum). For nonzero p ∈ S the possible values of dimR ker Lp are
exactly 0 and 4. Both occur: dimR ker Lp = 0 whenever ℜ(p) ̸= 0 (Lemma 5.1) and, for imaginary
p, whenever the criterion of Theorem 5.6 fails; dimR ker Lp = 4 precisely on the imaginary
aphanic locus. In particular 4 | dimR ker Lp for every nonzero p.
Proof. If ℜ(p) ̸= 0 then ker Lp = {0} by Lemma 5.1. If p is imaginary, then either the criterion
of Theorem 5.6 fails and ker Lp = {0}, or it holds and dimR ker Lp = 4 by Theorem 5.7. No
other value occurs. The value 0 is realized by, e.g., any p with ℜ(p) ̸= 0, and the value 4 by the
canonical p0 = e1 + e10 (Lemma 5.10).
Theorem 5.13 (Left–right equality). For every p ∈ S, dimR ker Lp = dimR ker Rp .
Proof. Conjugation x ↦→ x̄ is a real-linear isometric involution of S and an algebra antihomomorphism, xy = ȳ x̄ at every Cayley–Dickson level. Hence px = 0 ⇐⇒ px = x̄ p̄ = 0,
i.e. x ∈ ker Lp ⇐⇒ x̄ ∈ ker Rp̄ . The map x ↦→ x̄ is a real-linear bijection ker Lp → ker Rp̄ , so
dimR ker Lp = dimR ker Rp̄ . For imaginary p, p̄ = −p and Rp̄ = −Rp , which has the same kernel
as Rp ; for p with ℜ(p) ̸= 0 both kernels are trivial by the analogue of Lemma 5.1 for Rp (right multiplication by an imaginary element is also skew). In either case dimR ker Lp = dimR ker Rp .

5.7

The main theorem

Theorem 5.14 (Sedenion Annihilator Fourfold Theorem). Let S = O ⊕ O be the sedenion
algebra under the Cayley–Dickson product (2), and for p = (a, b) ∈ S let Lp (x) = px. For every
nonzero p:
(1) if ℜ(p) ̸= 0, then ker Lp = {0};
(2) if p is imaginary (so a ∈ Im(O), b ∈ O), then
ker Lp ̸= {0} ⇐⇒ ℜ(b) = 0, ⟨a, b⟩ = 0, |a| = |b|;
(3) the real dimension of ker Lp is either 0 or 4; in particular 4 | dimR ker Lp ;
(4) dimR ker Lp = dimR ker Rp .
Proof. Part (1) is Lemma 5.1; part (2) is Theorem 5.6; part (3) combines Theorem 5.12 with
Theorem 5.7; part (4) is Theorem 5.13.
Remark 5.15 (Status and scope). PROVEN. The dimension value 4 (and hence the spectrum {0, 4}) rests on the octonion-level Characterization Theorem 3.1 and is algebraic throughout. The determinant identity Proposition 5.4 is established by the exact finite certificate
of Section 5.8; its imaginary-component restriction coincides with the spectral Corollary 3.3
(Remark 5.5). The independent G2 -transport route of Section 5.5 invokes one standard external
fact, the simple transitivity of G2 on basic triples (Baez, 2002, §4.1); the primary dimension
argument does not use it. The theorem is a statement about the sedenion algebra S alone:
no claim is made about the pathion algebra or any higher Cayley–Dickson level, where the
determining octonion identities (composition, alternativity) no longer hold.
17

## PDF page 18

5.8

An exact certificate for the Pfaffian identity

This subsection proves Proposition 5.4. The argument is a finite exact certificate: it reduces the
identity to a finite list of exact integer evaluations, with a proven degree bound guaranteeing
that the list is complete. No floating-point arithmetic and no random sampling enter the proof.
Both sides are G2 -invariant. For φ ∈ G2 the diagonal automorphism φ̃ lies in SO(16)
(it is orthogonal and fixes the real axis), and by (24) Lφ̃p = φ̃Lp φ̃⊤ . For a skew matrix M
and S ∈ SO(16) one has Pf(SM S ⊤ ) = det(S) Pf(M ) = Pf(M ), so Pf(Lp ) is G2 -invariant;
the invariants I1 , D1 , D2 , D3 , |p|2 in (19) are manifestly G2 -invariant, so the right-hand side
−(|p|2 )2 T is as well.
Reduction to a normal form. Every imaginary p = (a, b) with a ̸= 0 lies in the G2 -orbit of
a normal form
p = (αe1 , β + γe1 + δe2 ),
α, β, γ, δ ∈ R,
(27)
obtained by rotating a to the e1 -axis (transitivity of G2 on imaginary directions) and then
rotating the part of b orthogonal to the ⟨1, e1 ⟩ plane into the e2 -direction (the stabilizer SU(3) of
e1 acts transitively on spheres in the orthogonal 6-space). The achievable invariants are I1 = α2 ,
D1 = β, D2 = αγ, D3 = α2 − (β 2 + γ 2 + δ 2 ); the constraint δ 2 = |b|2 − ℜ(b)2 − ⟨a, b⟩2 /|a|2 ≥ 0
is the Cauchy–Schwarz inequality, so (27) realizes every orbit (the case a = 0 occurs at α = 0).
Since both sides of (21) are G2 -invariant, it suffices to prove the identity on the normal forms
(27), i.e. as a polynomial identity in the four variables (α, β, γ, δ).
Degree bound. Each entry of Lp is linear in the coordinates of p, so on the normal form (27)
each entry is linear in (α, β, γ, δ). The Pfaffian of a 16 × 16 matrix is a homogeneous polynomial
of degree 8 in the matrix entries; hence Pf(Lp ) is a polynomial of total degree 8, and therefore
of degree at most 8 in each of α, β, γ, δ. The right-hand side −(|p|2 )2 T is likewise of degree 8.
Two polynomials of degree at most 8 in each variable that agree at 9 distinct values of each
variable – that is, on the full product grid {−4, −3, . . . , 4}4 of 94 = 6561 points – are identical
(multivariate Lagrange interpolation / the Combinatorial Nullstellensatz). It therefore suffices
to verify (21) at these 6561 points by exact arithmetic.
Exact evaluation of the Pfaffian. At an integer grid point the entries of Lp are integers,
and on the normal form each entry is a single signed coordinate, so |(Lp )ij | ≤ 4. The Pfaffian is
a signed sum of the 15!! = 2,027,025 perfect-matching products of eight entries, whence
| Pf(Lp )| ≤ 15!! · 48 = 132,843,110,400 < 12 P1 P2 ,

(28)

where P1 = 2,000,000,011 and P2 = 1,000,000,007 are two primes with P1 P2 ≈ 2 × 1018 .
Computing Pf(Lp ) mod P1 and modP2 by exact skew-symmetric Gaussian elimination over the
respective prime fields and reconstructing by the Chinese Remainder Theorem yields a unique
integer in (− 12 P1 P2 , 12 P1 P2 ); by the bound (28) this integer is Pf(Lp ). The right-hand side
−(|p|2 )2 T is a small integer evaluated directly. Carrying this out at all 6561 grid points, the
two integers coincide at every point. By the degree bound this proves Pf(Lp ) = −(|p|2 )2 T as a
polynomial identity over Z, and squaring gives det Lp = (|p|2 )4 T 2 .
□
Remark 5.16 (On the certificate). The computation is a finite, exact, and independently reproducible verification of an algebraic identity, not numerical evidence: the arithmetic is over Z and
finite fields, the degree bound is proved, the evaluation grid is complete for that degree, and the
integer Pfaffian is recovered exactly under the bound (28). The same value of Pf(Lp ) is obtained
from either prime alone within (28), and Pf(Lp )2 = det Lp provides a further consistency check
against an independent determinant routine. A self-contained program performing the certificate
is included in the supplementary archive.
18

## PDF page 19

6

Bundle Topology and the Aphanic Twist

By Theorem 3.1, ker Lp is a four-dimensional subspace of S for every aphanic p. As p varies
over the aphanic locus V, the kernels assemble into a continuous family — a rank-4 real vector
bundle K → V. This section establishes two structural facts: (1) the bundle is G2 -equivariant
with quaternionic fibers (the structure group reduces to SU(2) acting via the fundamental
representation), and (2) the bundle is topologically nontrivial, carrying a nonzero Z/2 secondary
characteristic class. The non-flatness of the canonical connection follows as a corollary.

6.1

The Aphanic Locus as a Homogeneous Space

Proposition 6.1 (Aphanic locus is a G2 -orbit). The aphanic locus V ⊂ S (unit-normalized,
per Section 2.3) is a single G2 -orbit, diffeomorphic to the homogeneous space G2 /SU(2). The
dimension is dim G2 − dim SU(2) = 14 − 3 = 11. The identification of the unit zero-divisor
locus of S with the Stiefel manifold V2 (R7 ) is due to Moreno (1998) and is recorded again in
(Biss et al., 2008, §12); the homogeneous-space presentation G2 /SU(2) used here, and everything
bundle-theoretic built on it in Sections 6–9, is what the present treatment adds.
Sketch. G2 = Aut(O) acts on O preserving the inner product and the real subspace, so it acts on
Im(O). As established in Proposition 5.9, G2 acts transitively on ordered orthonormal pairs in
Im(O) — the simple transitivity of G2 on basic triples (Baez, 2002, §4.1), restricted to the first
two frame vectors (cf. Harvey 1990 for the Stiefel-manifold formulation). The aphanic conditions
∥x∥ = ∥y∥, ⟨x, y⟩ = 0 say exactly that (x, y) is an unordered orthonormal pair (after rescaling),
so G2 acts transitively on the projectivized aphanic locus. The stabilizer of the basepoint (e1 , e2 )
in G2 is the subgroup fixing both e1 and e2 ; this is the SU(2) ⊂ G2 acting on the quaternionic
complement O ⊖ H(e1 , e2 ) in the standard way. Therefore V ∼
= G2 /SU(2).
The image of the kernel map Φ : V → Gr(4, S) is diffeomorphic to G2 /U (2), the twistor space
of S 6 (Bryant, 1982). The fibration G2 /SU(2) → G2 /U (2) has fiber S 1 , captured geometrically
by the rotation of the (e1 , e2 ) frame.

6.2

G2 -Equivariance of the Kernel Bundle

Lemma 6.2 (G2 -Invariance of K). The doubled G2 -action on S, D̃ := diag(D, D) for D ∈ G2 ⊂
SO(O), satisfies D̃ ∈ Aut(S). Consequently the kernel bundle K is G2 -equivariant: for every
g ∈ G2 and p ∈ V,
g̃ · ker Lp = ker Lg̃·p .
Proof. For g ∈ G2 , g(uv) = g(u)g(v) in O, g(ū) = g(u), and ∥g(u)∥ = ∥u∥. Applying the
recursive product (1) and using these, g̃((a, b)(c, d)) = (g̃(a, b))(g̃(c, d)). Hence g̃ ∈ Aut(S). For
any aphanic p and z ∈ ker Lp , Lp (z) = pz = 0, so g̃(p) · g̃(z) = g̃(pz) = 0, i.e., g̃(z) ∈ ker Lg̃(p) .
The reverse inclusion follows from g̃ −1 , completing the proof.
Theorem 6.3 (Fiber Representation Theorem). The stabilizer SU(2) ⊂ G2 of the basepoint
p0 = e1 + e2 · ℓ acts on ker Lp0 by the fundamental (spin- 12 ) representation. Under this action,
∼ Sp(1)-module.
ker Lp0 ∼
= H as an SU(2) =
Sketch. The Lie subalgebra s = {D ∈ g2 : De1 = De2 = 0} has dimension 3 (rank-11 constraint
in 14-dimensional g2 ). After an exact rational normalization (certified in op_six_anchors_A;
the earlier numerical Gram–Schmidt is superseded), three generators S0 , S1 , S2 ∈ s satisfy
[Si , Sj ] = 6 εijk Sk . Lifting to S via S̃i = diag(Si , Si ) and restricting to K0 := ker Lp0 gives
operators on H which, after rescaling Ta = Sa /6, satisfy Ta2 = − 14 idK0 , {Ta , Tb } = 0 for a ̸= b,
[Ta , Tb ] = Tc cyclically. This is the spin- 12 representation of su(2). The quadratic Casimir
∑
C2 = a Ta2 = − 43 idK0 yields j(j + 1) = 3/4, j = 1/2, confirming irreducibility.
19

## PDF page 20

The lemma and the fiber representation theorem together identify K → V with the associated
bundle G2 ×SU(2) H, where SU(2) acts on H by left multiplication (its fundamental two-dimensional
complex representation, equivalently the four-dimensional real representation Sp(1) ↷ H).

6.3

Bundle Nontriviality

Theorem 6.4 (Bundle Nontriviality / Aphanic Twist). The kernel bundle K = G2 ×SU(2) H over
V = G2 /SU(2) is topologically nontrivial. The characteristic class [K] ∈ H ∗ (V; Z/2) is nonzero.
Proof. The cohomology of V = G2 /SU(2) is computed from the Serre spectral sequence of the
fibration S 5 → V2 (R7 ) → S 6 (where V2 (R7 ) ∼
= V is the Stiefel manifold of orthonormal 2-frames
in R7 ):


k = 0, 11,

Z
k
H (V; Z) = Z/2 k = 6,


0
otherwise.
All primary characteristic classes (w1 , . . . , w4 , p1 , Euler) vanish for dimensional reasons: they
live in H k for k ≤ 4, all of which are zero. Hence K is stably trivial, and the only possible
nonzero invariant is a secondary class in H 6 (V; Z/2) = Z/2.
To detect this class, restrict K to the fiber S 5 of the Serre fibration. The classifying map of
5
S as the principal SU(2)-bundle SU(2) ,→ SU(3) → S 5 gives, via the long exact sequence of
homotopy groups,
∂

π5 (SU(3)) → π5 (S 5 ) −
→ π4 (SU(2)) → π4 (SU(3)) = 0.
Since π5 (S 5 ) = Z, π4 (SU(2)) = Z/2, and the target π4 (SU(3)) = 0, the connecting homomorphism ∂ is surjective. The generator of π5 (S 5 ) maps to the nontrivial element of π4 (SU(2)),
so the principal SU(2)-bundle SU(3) → S 5 is the unique nontrivial SU(2)-bundle on S 5 . Its
associated bundle SU(3) ×SU(2) H is the unique nontrivial quaternionic line bundle on S 5 , and
this is exactly the restriction of K to the fiber. Therefore K is nontrivial.
Remark 6.5 (Scope of the topological statement). Theorem 6.4 asserts nontriviality, detected
through the SU(2)-structure of the fiber restriction, and nothing more. It does not classify
rank-4 real bundles over V: a full classification involves the obstructions in H 6 (V; π4 (SO(4))) =
Z/2 ⊕ Z/2 together with the top cell of V, and is left open here.
Theorem 6.6 (Berry Phase Theorem (Berry, 1984; Simon, 1983)). The canonical (Nomizu)
connection (Kobayashi and Nomizu, 1963; Nomizu, 1954) on K → V is non-flat. There exist
closed loops Γ ⊂ V around which the parallel transport on K is the operator −idH .
Sketch. Consider the loop ΓA : θ ↦→ (cos θ)e1 + (sin θ)e3 + e2 · ℓ, θ ∈ [0, 2π]. This is a closed
geodesic in V. Direct integration of the Nomizu connection 1-form along ΓA , using the explicit
form of the connection in the orthonormal frame, gives holonomy −id. This is now certified
in closed form, with no integration: writing ΓA (θ) = exp(θX) · p0 for the unique X ∈ g2
with Xe1 = e3 , Xe3 = −e1 , Xe2 = 0 lying in the reductive complement m of s, the curve
θ ↦→ exp(θX) is the horizontal lift of ΓA for the canonical connection (Kobayashi and Nomizu,
1963), so the holonomy is the action of h := exp(2πX) on the fibre. Exactly, X splits Im(O) as
⟨e2 ⟩ ⊕ ⟨e1 , e3 ⟩ ⊕ ⟨e4 , . . . , e7 ⟩ with X 2 = 0, −Id and − 14 Id respectively; the half-integer frequency
on the last block gives h = diag(+1 on {1, e1 , e2 , e3 }, −1 on {e4 , . . . , e7 }) in closed form. One
checks exactly that h ∈ Aut(O), that h fixes p0 (so the loop closes), and that h̃ = diag(h, h)
preserves K with h̃|K = −id.
Because V is simply connected, every loop bounds a disc and the holonomy group coincides
with the restricted holonomy group; by the Ambrose–Singer theorem (Kobayashi and Nomizu,
1963) it is generated by curvature transported over a filling disc. Non-flatness is therefore
(

)

20

## PDF page 21

a consequence of the computation rather than a separate hypothesis: a flat connection on a
simply connected base has trivial holonomy, whereas ΓA transports by −id ̸= id. Other geodesic
loops may still have trivial holonomy (e.g., loops in the S 5 fiber not crossing the antipode);
the holonomy of each is fixed by the curvature over its own filling disc, and — V being simply
connected — no homotopy-class bookkeeping enters.
The class of Theorem 6.4 is not what ΓA measures. That class lives in H 6 (V; Z/2) and is
registered by the clutching function of K over the equatorial S 4 ⊂ S 5 through π4 (SU(2)) = Z/2; a
1-cycle cannot detect it. The −id holonomy of ΓA and the nonvanishing Z/2 class are independent
facts about K — the first metric-geometric, the second topological.
Remark 6.7 (Status). Theorem 6.3 is PROVEN, with no residual floating-point dependence:
dim g2 = 14 and dim s = 3 are certified by exact rational row reduction paired with exhibited nonzero minors (bounding each rank above and below), the normalization of the Ta is
exact-rational, and the Casimir is the exact scalar − 34 id. Irreducibility is certified over R, of
quaternionic type — the complexification is two copies of the spin- 12 representation. Theorem 6.4
is PROVEN (Serre spectral sequence, long exact sequence of homotopy groups). Theorem 6.6
is PROVEN: the numerical integration that formerly carried it is superseded by the exact
closed-form evaluation of exp(2πX) given above. Exactly the following are certified in exact
arithmetic: that X exists in g2 , is unique, and is Frobenius-orthogonal to s; that Xe1 = e3 ,
Xe2 = 0, Xe3 = −e1 ; that Im(O) splits X-invariantly as ⟨e2 ⟩ ⊕ ⟨e1 , e3 ⟩ ⊕ ⟨e4 , . . . , e7 ⟩ with X 2
equal to 0, −Id and − 14 Id on the three blocks; that the resulting h = exp(2πX) lies in Aut(O)
(checked on all 64 basis pairs) and satisfies h2 = Id; that h fixes p0 , so ΓA closes; that h̃ preserves
K by exact containment; and that h̃|K = −id. Exactly one ingredient is non-computational, and
it is a standard fact rather than a new claim: on a reductive homogeneous space, exp(tX) is
horizontal for the canonical connection precisely when X ∈ m (Kobayashi and Nomizu, 1963).
No floating-point quantity enters the theorem or its proof.

7

Algebraic Identification of the Holonomy Factors

It is established in prior work that the natural connection on the kernel sub-bundle K → Paph
has holonomy algebra u(2) = u(1) ⊕ su(2) and holonomy group U (2) = (U (1) × SU (2))/Z2 . That
statement is intrinsic: it identifies the Lie algebra up to isomorphism but does not locate its
factors inside the ambient algebra so(K) of skew-symmetric endomorphisms of a single fiber.
The present section closes that gap. Fixing the base point p0 = e1 + e2 · ℓ, we give both factors
explicit generators inside the sedenion multiplication structure.

7.1

Setup

Throughout this section, all sedenion multiplications are the canonical recursive Cayley–Dickson
product
¯ da + bc̄).
(a, b)(c, d) = (ac − db,
Let K := ker Lp0 , a 4-dimensional real subspace of S; the standard computation yields the
orthonormal basis
k0 = √12 (e7 + e12 ),

k1 = √12 (−e6 + e13 ),

k2 = √12 (e5 + e14 ),

k3 = √12 (−e4 + e15 ).

(29)

Identify K ∼
= H by (a0 , a1 , a2 , a3 ) ↦→ a0 + a1 i + a2 j + a3 k. Under this identification, the ambient
Lie algebra decomposes as
so(K) = su(2)L ⊕ su(2)R ,
where su(2)L (resp. su(2)R ) consists of left (resp. right) multiplication by imaginary quaternions
on H. These two subalgebras centralize each other; their direct sum exhausts so(4).
21

## PDF page 22

Let G2 = Aut(O) act on S by the doubled representation D̃ = diag(D, D) with D ∈ SO(O),
and let g2 ⊂ so(O) denote its Lie algebra, realized concretely as the span of the octonion
derivations Da,b = [La , Lb ] + [La , Rb ] + [Ra , Rb ], a, b ∈ Im(O), with dim g2 = 14.

7.2

The stabilizer inside g2

Proposition 7.1. The subalgebra
s := { D ∈ g2 : De1 = 0, De2 = 0 }
is three-dimensional, and it generates the copy of su(2) whose quotient produces Paph ∼
=
G2 /SU (2).
Proof. Express each D ∈ g2 in an orthonormal basis of g2 (obtained by Gram–Schmidt on
the 49-dimensional ambient space Mat7 (R) applied to a spanning set of derivations). The two
conditions De1 = 0 and De2 = 0 give 14 linear equations in 14 unknowns. Exact rational row
reduction gives rank 11, hence dim s = 3. The rank is certified in exact arithmetic in both
directions: fraction-free elimination over Q bounds it above, and an exhibited nonzero 11 × 11
minor bounds it below. The prerequisite dim g2 = 14 is certified the same way, by solving
the Leibniz system over all 64 basis pairs rather than assuming that a chosen spanning set
of derivations exhausts g2 . The identification s ∼
= su(2) follows from item (i) of Theorem 7.2
below.
Fix generators S0 , S1 , S2 ∈ s (any basis will do). Define their lifts and fiber restrictions
Ja := diag(Sa , Sa ) ∣K ,
∣

a ∈ {0, 1, 2}.

(30)

Each Ja ∈ so(K) by construction: the lift preserves K exactly (certified as exact containment
over Q, with no leakage tolerance), since K is G2 -invariant; cf. Lemma 6.2.

7.3

The decomposition theorem

Let G1 , G2 , G3 , G4 ∈ so(K) denote the four curvature generators of that prior work (the central
generator G1 = J∆ and the Gram–Schmidt basis {G2 , G3 , G4 } of the non-abelian factor). For
v ∈ Im(S), write Rv |K for the restriction to K of right-multiplication by v on S (when K is
Rv -invariant).
∼ H induced by (29),
Theorem 7.2 (Holonomy Decomposition). Under the identification K =
the holonomy algebra of the natural connection on K → Paph at p0 decomposes as
hol = u(2) = u(1)R ⊕ su(2)L ,

(31)

where:
(i) Setting Ia := Ja /3 from (30), one has Ia2 = −Id, {Ia , Ib } = 0 for a ̸= b, and [I0 , I1 ] = 2 I2
(with cyclic permutations). Consequently spanR {J0 , J1 , J2 } = su(2)L .
(ii) spanR {G2 , G3 , G4 } = su(2)L , with explicit change of basis
G2 = 61 J1 ,

G3 = 16 J0 ,

G4 = − 16 J2 .

(iii) [G1 , Ja ] = 0 for a ∈ {0, 1, 2}; hence G1 lies in the centralizer of su(2)L in so(K), which is
su(2)R .

22

## PDF page 23

(iv) The right-multiplications Re1 |K and Re2 |K are well-defined elements of so(K) ∩ su(2)R ,
and
G1 = − 14 [ Re1 |K , Re2 |K ].
In particular, u(1)R = R·G1 is the Lie closure of the right-multiplication pair {Re1 |K , Re2 |K }
in so(K).
Proof. All identities below are verified in exact rational arithmetic by the op_six_anchors_A
certification probe — every residual is the identically zero matrix over Q, and every dimension
count is a fraction-free row reduction paired with an exhibited nonzero minor. No floating-point
computation is load-bearing in any statement of this theorem. Here we give the structural
argument.
(i) A direct matrix computation from (30) yields Ja2 = −9 Id, {Ja , Jb } = 0 (a ̸= b), and
[J0 , J1 ] = 6 J2 with cyclic permutations. Rescaling Ia := Ja /3 gives the standard imaginaryquaternion relations Ia2 = −Id, {Ia , Ib } = 0, [I0 , I1 ] = 2 I2 . Three elements of so(4) satisfying these relations necessarily generate su(2)L under the identification K ∼
= H; indeed,
H
H
H
left-multiplication Li , Lj , Lk on H satisfy exactly these relations and span su(2)L by definition.
(ii) Project each Gm (m = 2, 3, 4) onto span{J0 , J1 , J2 } in the Frobenius inner product;
the residuals are zero, giving the stated change of basis. Equality of the two three-dimensional
subspaces follows.
(iii) Direct commutator computation: [G1 , Ja ] = 0 for a = 0, 1, 2, exactly over Q. The
centralizer of span{Ja } in so(K) is moreover certified to have dimension exactly 3 by exact row
reduction. Since so(K) = su(2)L ⊕ su(2)R with each factor equal to the other’s centralizer (a
standard fact about so(4)), the conclusion is immediate.
(iv) That Re1 and Re2 preserve K at p0 is a direct verification, certified as exact containment
(zero leakage, not a bounded one); this uses only that e1 , e2 lie in the quaternionic subalgebra
H spanned by {1, e1 , e2 , e3 } that appears in the Cayley–Dickson construction of p0 . A direct
commutator computation gives
− 14 [Re1 |K , Re2 |K ] = G1 ,
as an exact identity over Q, with G21 = − 14 Id pinning the normalization exactly. The Lie-closure
statement follows: the pair {Re1 |K , Re2 |K } spans only a two-dimensional subspace of su(2)R , but
their bracket supplies the third dimension, and the line R · [Re1 |K , Re2 |K ] is precisely u(1)R .

7.4

Remarks

Remark 7.3 (Origin of each factor). Theorem 7.2 supplies each summand of u(2) with a distinct
algebraic origin inside S:
• The non-abelian factor su(2)L is the restriction to K of the lifted action of the SU (2) ⊂ G2
stabilizer of p0 . The symmetry quotiented out to form the aphanic locus G2 /SU (2)
reappears inside the fiber as the non-abelian rotation.
• The abelian factor u(1)R is not generated by a single elementary right-multiplication on
K; it is generated by the Lie bracket of two such right-multiplications by orthogonal units
of the distinguished quaternion subalgebra ⟨1, e1 , e2 , e3 ⟩. The Berry phase generator is,
algebraically, a commutator of right-actions.
Remark 7.4 (Reshaping of an earlier conjecture). Earlier working versions of this framework
conjectured that the non-abelian factor would identify with right-multiplication by imaginary
quaternions on K (i.e., with su(2)R ). Theorem 7.2 shows the opposite: the non-abelian factor is
left-multiplication, while the abelian factor is a distinguished line inside the right-multiplication
algebra. The geometric content of the two factors is therefore reversed relative to that conjecture.
23

## PDF page 24

Remark 7.5 (Reproducibility). Every claim in the proof is certified in exact rational arithmetic by
a single self-contained C++17 probe (op_six_anchors_A.cpp) with no external dependencies,
superseding the earlier floating-point verification (holonomy_u2_identification.cpp). Integer
arithmetic throughout, with 128-bit internals and hard overflow checks; every residual is the
identically zero matrix and every dimension count is a fraction-free row reduction paired with an
exhibited nonzero minor, so each rank is bounded above and below in exact arithmetic. There is
no leakage tolerance anywhere: subspace invariance is certified as exact containment. Nothing
in this section rests on floating point.
Remark 7.6 (No physics claim). The Lie group U (2) = (U (1) × SU (2))/Z2 is, up to isomorphism,
the electroweak gauge group of the Standard Model. The results here make no physical claim;
they are strictly mathematical statements about the holonomy of a natural connection on the
sedenion kernel sub-bundle. What the sedenion algebra has produced, without physical input,
is the Lie group U (2). What it has not done is supply a metric, a bundle of Dirac spinors, a
Yukawa sector, or any of the structure required to interpret this as a physical gauge theory.
That interpretation, if it is warranted at all, is a separate question.

8

Algebraic R ℓ Centrality

Section 7 identified the abelian factor u(1)R ⊂ u(2) inside the ambient sedenion multiplication
algebra at the basepoint p0 = e1 + e2 · ℓ. The identification was local: it placed the generator
G1 = − 14 [Re1 |K , Re2 |K ] inside su(2)R at the single fiber over p0 . The Three-Way Identity
√
strengthened this to the Three-Way Identity, 2 G1 = Rℓ |Kp0 = 2 B3 , which showed that three
independent constructions of the U(1) center—Berry, CD algebra, frame-free Hodge—collapse
to a single line at p0 .
This section answers the question carried from that identity and only partly addressed by
the earlier orbit-uniform numerical statement (which certified [Rℓ , πp ] = 0 on Paph,1 at machine
precision across N = 64 random samples but offered no algebraic derivation): is the U(1)
generator a fiberwise restriction of a single p-independent operator on S, and is the centrality
identity algebraic rather than numerical?
The answer is yes, with a sharper statement than the kernel-projector version: the centrality
identity holds for the full Gram operator Gp = L⊤p Lp across the entire imaginary locus, of which
Paph is the kernel-bearing sublocus, and the proof is a five-stage reduction in the Cayley–Dickson
block algebra.

8.1

Statement

Theorem 8.1 (Algebraic Rℓ Centrality). Let S = O ⊕ O · ℓ be the sedenion algebra under
¯ da + bc̄), with ℓ = e8 . Let
canonical recursive Cayley–Dickson doubling (a, b)(c, d) = (ac − db,
p = (x, y) with x, y ∈ Im(O), Lp left-multiplication by p, Gp := L⊤p Lp the Gram operator, and
Rℓ right-multi plication by ℓ. Then
[Rℓ , Gp ] = 0

on R16 .

(32)

Corollary 8.2 (Fiberwise centrality). For every p ∈ Paph,1 the orthogonal projector πp onto
ker(Lp ) satisfies [Rℓ , πp ] = 0.
Proof of Corollary 8.2. On the aphanic locus the Gram operator Gp has spectrum {04 , 28 , 44 }
(the 4-8-4 Spectral Theorem); the three eigenvalues are distinct, so each eigenprojector is a
polynomial in Gp given by Lagrange interpolation:
πp =

Gp − µI
= 18 (Gp − 2I)(Gp − 4I).
0
−
µ
µ∈{2,4}
∏

24

## PDF page 25

Any operator commuting with Gp commutes with every polynomial in Gp , hence with πp .
Theorem 8.1 gives [Rℓ , Gp ] = 0, so [Rℓ , πp ] = 0.

8.2

Strict strengthening over the fiberwise statement

Theorem 8.1 is strictly stronger than the numerical that statement in two independent senses.
Remark 8.3 (Locus). The fiberwise statement holds on the aphanic locus Paph,1 (the unit-norm
aphanic observers, an 11-dimensional homogeneous space G2 /SU (2)). Theorem 8.1 holds on
the imaginary locus {p = (x, y) ∈ S : x, y ∈ Im(O)}, a 14-dimensional real submanifold of S of
which the aphanic locus is a strict, codimension-3 subset. The aphanic conditions ∥x∥ = ∥y∥
and ⟨x, y⟩ = 0 play no role in the proof.
Remark 8.4 (Operator). It is an identity on πp , the rank-4 spectral projector of Gp . Theorem 8.1
is an identity on the full operator Gp , of which πp is one of three spectral projectors (for the
eigenvalues 0, 2, 4). The full identity contains the kernel-restricted version as a corollary.

8.3

Proof

Throughout this subsection let
K : O → O,

K(u) := ū

denote octonion conjugation, with matrix K = diag(1, −1, −1, . . . , −1) ∈ R8×8 in the standard
basis {1, e1 , . . . , e7 } of O. Define the associator-action operator
Ax,y : O → O,

Ax,y (u) := [x, u, y] := (xu)y − x(uy).

The proof proceeds in five stages, each a self-contained algebraic identity verified at machine
precision in the C++17 probe op_rell_centrality_proof.cpp on 1 + 64 + 64 = 129 samples
spanning p0 , the aphanic orbit, and the imaginary-non-aphanic regime (Section 8.4).
Stage 1: block decomposition of Lp and Gp
Identify S with O ⊕ O via (u, v) ↔ u + v · ℓ. Direct application of the Cayley–Dickson product
gives
(
)
(
)
Lx −Ry K
0 −I8
Lp =
,
Rℓ =
.
(33)
Ly K
Rx
I8
0
The composition-algebra identities Lā La = Rā Ra = ∥a∥2 I in O, together with K 2 = I, K⊤ = K,
L⊤a = Lā , R⊤a = Rā , give
(

Gp =

L⊤p Lp

=

)

∥p∥2 I8
B
,
B⊤
∥p∥2 I8

B = −Lx̄ Ry K + KLȳ Rx .

(34)

For x, y ∈ Im(O) (x̄ = −x, ȳ = −y) this specializes to
B = Lx Ry K − KLy Rx .

(35)

Stage 2: reduction to skewness
Direct block multiplication of the matrices in (33) and (34) yields
(

[Rℓ , Gp ] =

)

−(B + B⊤ )
0
.
0
B + B⊤

Hence [Rℓ , Gp ] = 0 ⇐⇒ B is skew-symmetric.
25

(36)

## PDF page 26

Stage 3: associator identity for the cross-block
Apply B in (35) to u ∈ O:

B(u) = x · (ū y) − y(ux).

The Cayley–Dickson conjugation is an anti-homomorphism, ab = b̄ā, so y(ux) = ux · ȳ = (x̄ū)ȳ.
For x, y ∈ Im(O) this is (−xū)(−y) = (xū) y, giving
B(u) = x(ū y) − (xū) y = − (xū)y − x(ūy) = −[x, ū, y] = −Ax,y (Ku).
]

(37)

B = −Ax,y ◦ K.

(38)

[

Thus, as 8 × 8 real matrices,

The minus sign is essential and traces to the parity of ȳ = −y in y(ux).
Stage 4: Ax,y is skew on O for x, y ∈ Im(O)
Stages 4 and 5 are written at the octonion level, since that is the level at which the sedenion crossblock lives. The ingredients they use — flexibility, the inner-product duality ⟨uv, w⟩ = ⟨v, ūw⟩,
and the conjugation anti-homomorphism property — hold at every Cayley–Dickson level (Table 1),
so the arguments transpose verbatim one level up; this is what Section 9 makes explicit.
In a normed composition algebra, ⟨ab, c⟩ = ⟨b, āc⟩ = ⟨a, cb̄⟩. Applying both forms,
⟨[x, u, y], v⟩ = ⟨(xu)y, v⟩ − ⟨x(uy), v⟩
= ⟨u, x̄(v ȳ)⟩ − ⟨u, (x̄v)ȳ⟩
= − u, [x̄, v, ȳ] .
⟨

⟩

For x, y ∈ Im(O), [x̄, v, ȳ] = [−x, v, −y] = [x, v, y], hence
A⊤x,y = −Ax,y .

(39)

Stage 5: K commutes with Ax,y for x, y ∈ Im(O)
By the anti-homomorphism property,
[x, u, y] = (xu)y − x(uy) = ȳ(ūx̄) − (ȳū)x̄ = −[ȳ, ū, x̄].
For x, y ∈ Im(O), −[ȳ, ū, x̄] = −[−y, ū, −x] = −[y, ū, x] = [x, ū, y] by the alternation of the
associator under transposition of outer arguments. Therefore
K Ax,y (u) = [x, u, y] = [x, ū, y] = Ax,y (Ku),

(40)

i.e., [K, Ax,y ] = 0.
Closure
Combining (38), (39), (40):
B⊤ = −(Ax,y K)⊤ = −K⊤ A⊤x,y = −K(−Ax,y ) = KAx,y = Ax,y K = −B.
So B is skew, and (36) yields [Rℓ , Gp ] = 0.

□

26

## PDF page 27

8.4

Numerical certification

Each of Stages 1–5 is a matrix identity over R. The probe op_rell_centrality_proof.cpp
certifies all five at machine precision on three sample sets:
• the basepoint p0 = e1 + e2 · ℓ (every residual identically zero, 0 · 100 );
• N = 64 random aphanic observers p ∈ Paph,1 (worst residual 2.34 · 10−15 , Stage 2
commutator at the 16 × 16 level);
• N = 64 random imaginary-non-aphanic observers (x, y ∈ Im(O) with generic norms and
inner product; worst residual 2.33 · 10−14 ).
All residuals are ≤ 10−12 , the declared tolerance. The third sample set is the operative test for
the strict strengthening claimed in Section 8.2: it lies outside Paph but inside the proof’s scope.

8.5

Remarks

Remark 8.5 (Why the imaginary locus is the natural domain). The proof uses x̄ = −x and
ȳ = −y in two essential places: in the simplification of y(ux) to (xū)y (Stage 3, equation (37))
and in collapsing [x̄, v, ȳ] = [x, v, y] (Stage 4, justifying A⊤ = −A). Real components of x or y
would propagate through both reductions and break the skew-symmetry of B. The proof tells
us, in passing, that the imaginary locus is the maximal subset of S on which Rℓ is algebraically
central with respect to the Gram operator.
Remark 8.6 (Reframing of the Section 6 U(1) generator). Theorem 7.2 gave the U(1) center at p0
as the commutator − 41 [Re1 |Kp0 , Re2 |Kp0 ] = G1 . That construction is basepoint-bound: Re1 and
Re2 stop preserving Kp as p moves off the quaternionic distinguished subalgebra. Theorem 8.1
replaces the commutator construction with a single ambient operator Rℓ = Re8 that is central
with respect to Gp at every imaginary p. Combined with the Three-Way Identity (2G1 = Rℓ |Kp0
at p0 ), the upgrade is: the U(1) generator is a single global matrix on S, not a fiberwise
commutator.
Remark 8.7 (Reproducibility). The five-stage decomposition is realized in a single self-contained
C++17 probe (op_rell_centrality_proof.cpp) with no external dependencies, building under
both MSVC and GCC; runtime is sub-second. The probe emits per-stage worst-case residuals
on the basepoint and both random sample sets.
Remark 8.8 (Level-uniformity and the tower). The five-stage proof structure relies only on (i) the
Cayley–Dickson block decomposition, (ii) the composition-algebra norm identity at the preceding
doubling level, and (iii) the anti-homomorphism property of conjugation. Each ingredient
survives every doubling step provided x, y are taken in the imaginary part of the previous-level
algebra. The identity is therefore not specific to S: it is proved for every level in Theorem 9.3 of
Section 9, which supplies the general argument. At the first higher level — the dim-32 pathion
algebra P = S ⊕ S · ℓ16 with ℓ16 = e16 , and p = (x, y) ∈ P with x, y ∈ Im(S) — the identity reads
[Re16 , Gp ] = 0, and the aphanic sublocus of P correspondingly carries an algebraic U (1) center
generated by the restriction of Re16 to the fiberwise kernel. The numerical values quoted at
higher levels are certification witnesses for the implementation, not evidence for the identity.

9

The Cayley–Dickson Tower Recursion

The Rℓ centrality identity of Section 8 was proven for the dim-16 case, with two ingredients used
at the diagonal-block stage that depend on the composition-algebra structure of O:
(i) LX̄ LX = ∥X∥2 I on O for every X ∈ O (composition law);
27

## PDF page 28

(ii) A = D = ∥p∥2 I in the diagonal blocks of Gp = L⊤
p Lp .
The composition law fails at the next CD level: S is not a composition algebra. Naively, this
should obstruct the centrality proof at dim 32. In fact the obstruction is illusory: a strictly
weaker identity, the Imaginary L–R Symmetry Lemma, suffices to drive the diagonal-block
argument, and that identity is preserved at every CD level via flexibility alone. This section
establishes the tower-wide recursion.

9.1

Imaginary Left–Right Symmetry

Theorem 9.1 (Imaginary L–R Symmetry). Let An be the 2n -dimensional Cayley–Dickson
algebra obtained by canonical recursive doubling. For every n ≥ 1, every X ∈ Im(An ), and every
q ∈ An ,
X̄(Xq) = (qX)X̄.
(41)
Equivalently, LX̄ LX = RX̄ RX as operators on An .
Proof. Cayley–Dickson algebras are flexible at every level An : a(ba) = (ab)a for all a, b ∈ An .
Linearizing in a,
[a, b, c] = [c, b, a]
∀ a, b, c ∈ An ,
the outer-pair symmetry of the associator. Apply this with a = X, b = X, c = q:
[X, X, q] = [q, X, X].
For X ∈ Im(An ), X 2 = −∥X∥2 ∈ R commutes with everything in An , so
X(Xq) − X 2 q = (qX)X − qX 2 ⇐⇒ X(Xq) = (qX)X.
Negating both sides (X̄ = −X for X ∈ Im) gives X̄(Xq) = (qX)X̄, which is LX̄ LX =
RX̄ RX .
Remark 9.2 (The flexibility shadow of composition). At composition levels (An for n ≤ 3, i.e.,
C, H, O), both sides of (41) reduce independently to ∥X∥2 q, so each operator equals ∥X∥2 I. At
n ≥ 4 the operators each individually deviate from ∥X∥2 I (reflecting the loss of composition),
but they continue to agree with each other — their common value is some non-scalar operator
that nonetheless inherits centrality with respect to the structures we construct.

9.2

Recursive Rℓ Centrality

Theorem 9.3 (Recursive Rℓn+1 Centrality). Let An+1 = An ⊕ An · ℓn+1 , n ≥ 3, and let
(n+1)

p = (X, Y ) ∈ An+1 with X, Y ∈ Im(An ). Let Gp

:= L⊤
p Lp on An+1 . Then

[Rℓn+1 , G(n+1)
] = 0.
p
Proof. The block form of Lp on An+1 ∼
= An ⊕ A n ,
(

Lp =

)

LX
−RY Kn
,
LY Kn
RX

(

Rℓn+1 =

)

0 −I
,
I 0

where Kn is conjugation in An , gives by direct 2 × 2 block multiplication
(

[Rℓn+1 , G(n+1)
]
p
where

=

)

−(B + B ⊤ ) A − D
,
A−D
B + B⊤

A = LX̄ LX + Kn LȲ LY Kn ,

D = RX̄ RX + Kn RȲ RY Kn ,
28

## PDF page 29

and B is a cross-block built from associator-action operators on An .
Diagonal vanishing A = D. By Theorem 9.1 applied to X and to Y , LX̄ LX = RX̄ RX and
LȲ LY = RȲ RY . Substituting term-by-term, A = D.
Off-diagonal vanishing B + B ⊤ = 0. The argument is identical to that in Section 8 (Stages 3–
5), using only the inner-product duality ⟨ab, c⟩ = ⟨b, āc⟩ (which holds at every CD level) and the
conjugation anti-homomorphism property (also tower-universal). Both ingredients survive every
doubling, so the cross-block argument ports verbatim to level n + 1 for X, Y ∈ Im(An ).
(n+1)
Both diagonal and off-diagonal blocks vanish, so [Rℓn+1 , Gp
] = 0.
Corollary 9.4 (Kernel-projector centrality at every level). At any level n + 1 ≥ 4 where An+1
contains aphanic observers p (i.e., ker Lp ̸= 0) with halves in Im(An ), the orthogonal projector
(n+1)
πp
onto ker Lp commutes with Rℓn+1 :
[Rℓn+1 , πp(n+1) ] = 0.
(n+1)

Proof. Spectral projectors are polynomials in Gp
via Lagrange interpolation across distinct
(n+1)
eigenvalues; commutation with Gp
descends to commutation with each spectral projector.

9.3

Empirical Confirmation at the Chingon Level

The proof of Theorem 9.3 relies on three identities that survive every Cayley–Dickson doubling:
flexibility, inner-product duality, and the conjugation anti-homomorphism. None of these is
special to the dim-32 case. The natural conjecture is that the recursion continues indefinitely.
Proposition 9.5 (Chingon-level certification probe, EMPIRICAL). At dim 64 (the chingon
algebra C≂), the centrality identity
[Re32 , G(64)
p ] = 0,

p = (X, Y ), X, Y ∈ Im(P),

is verified at machine precision across N = 8 random samples, with worst residual 3.05 · 10−13 .
The structural argument of Theorem 9.3 ports verbatim to this level, so an algebraic proof is
implied; the empirical verification serves as a sanity check.
The probe op_chingon_centrality_sanity.cpp computes the 64 × 64 Gram and right(64)
multiplication matrices via the recursive CD product and certifies ∥[Re32 , Gp ]∥F ≤ 10−12 .
Build target included in the supplementary archive.
Remark 9.6 (Status of the tower recursion). Theorem 9.1 is PROVEN (algebraic). Theorem 9.3
is PROVEN for all n ≥ 3: its proof uses only the inner-product duality and the conjugation
anti-homomorphism property, both of which hold at every Cayley–Dickson level, so the argument
is level-uniform and no doubling step is distinguished. Proposition 9.5 accordingly reports a
corroborating certification probe at n + 1 = 6 (dim 64); it witnesses the implementation rather
than carrying the claim, which the theorem already establishes at that level and above.

10

Open Frontiers

The framework as developed here closes the algebraic-foundations chapter of the Aphanes
program. Several questions remain open as research directions; we list the principal ones, in
order of proximity to the present results.

29

## PDF page 30

10.1

The SU(2)L –Fano Identification

Theorem 7.2 identifies the u(1) factor of the holonomy algebraically as the restriction to Kp0
of the ambient operator Rℓ . The corresponding identification of the su(2)L factor remains less
direct: it is the restriction of the lifted SU(2)-stabilizer action, which is defined geometrically
via the orbit structure rather than as a direct product of ambient operators. Numerical evidence
indicates that the three generators G2 , G3 , G4 of su(2)L correspond to right-multiplication by
the imaginary quaternions i, j, k ∈ H acting on the rank-4 complement Im(Q)⊥ ∼
= H, where
Q = span{1, e1 , e2 , e1 e2 } is the distinguished quaternionic subalgebra at the basepoint. An
algebraic proof of this identification would parallel Theorem 8.1 for the abelian sister, closing
the loop on the U(2) decomposition.

10.2

Universality of the Holonomy Classification at Higher Levels

Theorem 9.3 establishes the algebraic recursion of the U(1) center; the analogous question for
the holonomy decomposition is open. At the pathion level (dim 32), aphanic observers exist
(Two-Layer Theorem; (Cawagas, 2004) and probes), but the kernel structure is known to be
richer: there is a rank-jumping kernel sheaf with strata of dimension 4 and dimension 0. Whether
the canonical connection on the dim-4 stratum has U (2) holonomy, deforms to a larger group,
or ruptures at the next CD doubling is undetermined. The natural template, given Theorem 9.1,
is to test whether the analogous stabilizer action on the dim-4 stratum produces a copy of su(2)
centralized by an ambient Rℓ5 -restriction.

10.3

Global Integrability of the Kernel Distribution

Axiom 3 of the abstract framework (Skiouris, 2026) asserts non-integrability of the rank-4 kernel
distribution p ↦→ ker Lp over the aphanic locus. This is supported empirically (no smoothlydefined four-form ω satisfying dω ∈ I(ω) has been found) but lacks a formal Frobenius test. A
direct computation of the Frobenius bracket on the Gram–Schmidt-orthonormal kernel basis at
a generic p would settle the matter. This is a finite computation in O-arithmetic that has not
yet been carried out.

10.4

Two-Layer Theorem Beyond Dim 32

Cawagas (Cawagas, 2004) conjectured, and we have empirically confirmed through dim 64, that
fresh aphanic kernels (i.e., non-trivial ker Lp at points p that are not pulled back from lower
levels) arise only at dim 16 and dim 32, vanishing thereafter. An algebraic proof of the Two-Layer
Theorem at all higher levels remains open. The Schur complement argument at dim 32 indicates
that the next obstruction to fresh kernels is a determinant condition that, empirically, becomes
generic at dim 64+; a proof would generalize the keystone identity (15) to higher CD doublings.

10.5

Connection to Twistor Theory

The image of the kernel map Φ : V → Gr(4, S) is G2 /U (2), the twistor space of S 6 (Bryant,
1982). The algebraic structure of the kernel bundle pulled back from this twistor space, and
its relationship to standard twistor constructions on S 6 (Bryant’s nearly-Kähler structure, the
canonical G2 -frame bundle), is a natural further line of inquiry — particularly given the U(2)
holonomy and the fact that twistor spaces of nearly-Kähler 6-manifolds carry canonical Kähler
structures with U(2) holonomy in their own right.

30

## PDF page 31

Acknowledgments
Christopher J. Vizas has been this project’s Socrates: the most productive irritant a solitary
line of work could have, and the person most responsible for its turn toward formalization. He
put the American Mathematical Society’s 1962 Manual for Authors of Mathematical Papers into
the author’s hands, where it has remained a distillation engine for the author’s thinking ever
since. His range, from the sea and the space programme to law and public service, is why he
could see where this work needed to go before the author could, and he supplied the bridge to
the academy that an unaffiliated researcher does not otherwise have.
The author thanks Dr. Elias G. Carayannis, Professor Emeritus of Information Systems and
Technology Management at the George Washington University, with whom he has previously
co-authored, for sustained discussions on institutional creativity, structural blind spots, and the
framework’s broader implications, and for something a family cannot supply. In a tradition
where one’s own are obliged to encourage, he was the first Greek outside the author’s family,
and the first with credentials and no obligation, to say the work was worth doing. That is the
only kind of saying that carries.
The author’s deepest debt is to Paul Jacob Hall, co-founder of Agingo Corporation, who for
nine years has held open the space in which this work could be done, space that no institution
and no investor was prepared to offer. The first letter the author wrote him cast the undertaking
as an odyssey, with Agingo as its Ithaca; he has kept faith with that description every year since.
This work is as much his as the author’s. The author thanks the team at Agingo Corporation
alongside him, and the many long lunches at the Open Kitchen where these ideas were first
argued into shape.
Finally, the author thanks his family: his parents, his brother and sister, his wife and his
children. A child who takes apart the fire screen, then the walkie-talkie, then the household’s
first computer is a difficult thing to encourage. He was encouraged anyway, given room, an
unblocked shelf, and a patient hearing for more than one monologue about processor architecture.
That no condition was ever attached is the part he understood last and values most. Whatever
in this paper comes from taking a structure apart to find what holds it together was learned at
home, long before it had a name.
Preparation note. The author used an AI assistant in preparing this manuscript: for prior-art
search, for checking citations and internal consistency, and for editorial work on the exposition.
The mathematics, the proofs, and the certification probes are the author’s own.

References
J. C. Baez, The Octonions, Bull. Amer. Math. Soc. 39 (2002), 145–205.
M. V. Berry, Quantal phase factors accompanying adiabatic changes, Proc. R. Soc. A 392 (1984),
45–57.
R. L. Bryant, Submanifolds and special structures on the octonions, J. Diff. Geom. 17 (1982),
185–232.
R. E. Cawagas, On the structure and zero divisors of the Cayley–Dickson sedenion algebra,
Discuss. Math. Gen. Algebra 24 (2004), 251–265.
J. H. Conway and D. A. Smith, On Quaternions and Octonions, A. K. Peters, 2003.
F. R. Harvey, Spinors and Calibrations, Academic Press, 1990.
A. Hurwitz, Über die Composition der quadratischen Formen, Nachr. Ges. Wiss. Göttingen
(1898), 309–316.
31

## PDF page 32

K. Imaeda and M. Imaeda, Sedenions: algebra and analysis, Appl. Math. Comput. 115 (2000),
77–88.
S. Kobayashi and K. Nomizu, Foundations of Differential Geometry, Vol. I, Wiley, 1963.
D. K. Biss, D. Dugger, and D. C. Isaksen, Large annihilators in Cayley–Dickson algebras, Comm.
Algebra 36 (2008), no. 2, 632–664. arXiv:math/0511691.
D. K. Biss, J. D. Christensen, D. Dugger, and D. C. Isaksen, Large annihilators in Cayley–Dickson
algebras II, Bol. Soc. Mat. Mexicana (3) 13 (2007), no. 2, 269–292. arXiv:math/0702075.
D. K. Biss, J. D. Christensen, D. Dugger, and D. C. Isaksen, Eigentheory of Cayley–Dickson
algebras, Forum Math. 21 (2009), no. 5, 833–851. arXiv:0905.2987.
S. Khalil and P. Yiu, The Cayley–Dickson algebras, a theorem of A. Hurwitz, and quaternions,
Bull. Soc. Sci. Lett. Łódź Sér. Rech. Déform. 24 (1997), 117–169.
S. Koebisu, Determinant factorization for left multiplication in the sedenions, arXiv:2512.13002
(2026).
G. Moreno, Constructing zero divisors in the higher dimensional Cayley–Dickson algebras,
arXiv:math/0512517 (2005).
G. Moreno, The zero divisors of the Cayley–Dickson algebras over the real numbers, Bol. Soc.
Mat. Mexicana (3) 4 (1998), no. 1, 13–28. MR1625585. arXiv:q-alg/9710013.
K. Nomizu, Invariant affine connections on homogeneous spaces, Amer. J. Math. 76 (1954),
33–65.
R. D. Schafer, An Introduction to Nonassociative Algebras, Academic Press, 1966.
B. Simon, Holonomy, the quantum adiabatic theorem, and Berry’s phase, Phys. Rev. Lett. 51
(1983), 2167–2170.
K. J. Skiouris, Aphanics and Creative Curvature: A Geometric Theory of Hidden Generation in
Dialectical Cognitive Systems, arXiv preprint, in preparation, 2026.
F. Wilczek and A. Zee, Appearance of gauge structure in simple dynamical systems, Phys. Rev.
Lett. 52 (1984), 2111–2114.
P. Zvengrowski, A 3-fold vector product in R8 , Comment. Math. Helv. 40 (1966), 149–152.

32
