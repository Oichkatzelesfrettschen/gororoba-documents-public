Source: https://zenodo.org/api/records/22082732
PDF sha256: 5e715063e9d1eeb6f4746034f14fd67e9e5c31d85e648f92812e6d161cd6c81d
License: CC-BY-4.0
Language: eng
Fidelity: machine-gated

# Transcription of skiouris-2026-aphanics-pathion.pdf

Transcription of `skiouris-2026-aphanics-pathion.pdf` in this directory, 33 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-33 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Aphanics at the Pathion Level:
Spectrum Stratification and the Universal Clifford Triad
Kyriakos John Skiouris
Agingo Corporation, Charlotte NC
research@agingo.com
August 2026
Abstract
We extend the Aphanes framework from the sedenion algebra S to its Cayley–Dickson
double, the pathion algebra P = S ⊕ S · ℓ of dimension 32. At sedenion level, prior work
establishes that for any aphanic basepoint p the closed-form Berry curvature operator Ca,b (p)
has a four-dimensional kernel structure giving F(p) ∼
= u(1) ⊕ su(2) and a G2 -equivariant
rank-4 closure. Lifting these results to pathion exposes structurally new phenomena: the
2
2
Gram operator Gp = L⊤
p Lp has spectrum {0, ∥p∥ , 2∥p∥ } at dyadic basepoints and an eightvalued spectrum at generic aphanics. We establish two theorems describing the kill set of
a ↦→ Ca,∗ (p); in each, the containment (sufficiency) direction is proved symbolically, while
the exact kill-set dimension (necessity) is certified numerically (Appendix A). The Pathion
Universal Kill Set Theorem states that at every pathion-aphanic p with dim Kp = 4, this
= spanR {p, ℓ16 , ℓ16 · p}. The Pathion
kill set is exactly the three-dimensional space quniv
p
Q-Centralizer Vanishing Theorem at Dyadic Basepoint states that under the additional
hypothesis of a three-valued Gram spectrum of canonical Stratum-II type, the kill set extends
(32)
. Both theorems follow from a structural result
⊃ quniv
to a five-dimensional space qp
p
which is the heart of this paper: the three operators Lp , Lℓ16 , Lℓ16 ·p form a pairwise anticommuting Clifford triad on P. We prove this Triad Theorem algebraically, reducing the
third pair to a sedenion identity ∆(s1 , s2 ) = 0 for orthogonal imaginary s1 , s2 ∈ Im(S),
which in turn reduces by a four-block Cayley–Dickson decomposition to a three-variable
octonion identity Ω(A, B; c) = 0. The latter falls to a two-line argument from polarization,
Artin’s theorem on two-generator subalgebras of the octonions, and the composition norm
(32)
⊕ qanti
is shown to be Z2 -graded: each summand
form. The dim-5 structure qp = quniv
p
p
is independently Clifford-internal at every aphanic basepoint, but mixed pairs across the
(32)
grading do not anti-commute. Hence the dyadic-only extension to qp uses a mechanism
distinct from the universal Clifford triad. All symbolically proved identities are additionally
certified numerically; each certification states its epistemic basis in Appendix A.

1

Introduction

The Aphanes framework studies a class of algebraically hidden generators in non-associative
Cayley–Dickson algebras above the octonions. The core equation p · A(p) = 0 with A(p) ̸= 0
captures a structurally real generator annihilated by its own system’s left-multiplication. At
sedenion level S (dimension 16), prior work established the algebraic characterization of aphanic
basepoints and the universal 4−8−4 spectrum of the Gram operator [1], and a closed-form
Berry curvature operator [2] Ca,b (p) whose four-dimensional kernel space carries a u(1) ⊕ su(2)
Lie structure with global holonomy group U (2) = (U (1) × SU (2))/Z2 , the gauge group of the
electroweak interaction, arrived at from pure sedenion algebra without physics input.
A natural question is whether these structures persist at higher levels of the Cayley–Dickson
tower. The pathion algebra P = S ⊕ S · ℓ16 of dimension 32 provides the first non-trivial test. We
establish that the framework lifts in a refined form (sufficiency directions symbolically, exact
1

## PDF page 2

kill-set dimensions by numerical certification): the rank-4 kernel persists, but the universal kill
set of the curvature operator drops from dimension 5 at sedenion to dimension 3 at pathion,
with a dimension-5 extension surviving only at basepoints of three-valued spectrum.
The structural heart of these results is a Clifford-like triad of three pairwise anti-commuting
operators canonically attached to each aphanic basepoint. We prove the triad theorem algebraically by reducing through a Cayley–Dickson tower: the pathion identity reduces to a
sedenion identity, which reduces to an octonion identity, which falls to Artin’s theorem on twogenerator subalgebras. The chain hides the non-associative complexity by trapping it in the
well-developed alternative-algebra structure of the octonions.
Organization. Section 2 fixes notation for the Cayley–Dickson recursion, the aphanic locus,
and the Berry curvature operator. Section 3 describes the pathion spectrum stratification.
Section 4 states and proves the two pathion Q-centralizer vanishing theorems. Section 5 proves
the Pathion Clifford Triad Theorem and unwinds the supporting algebraic chain (Lemma A,
(32)
Delta-reduction, Omega-theorem). Section 6 describes the Z2 -graded Clifford sublattice on qp
that separates the universal from the dyadic-only kill set. Section 7 proves the Two-Regime
Dyadic Closure Theorem underlying the dyadic extension. Section 8 discusses connections
to the sedenion U(2) holonomy and open questions. Appendix A reports machine-precision
certification of the key identities.
Main results.

The substantive contributions of this paper are:

(1) Theorem 4.1 (Pathion Universal Kill Set): for every pathion-aphanic p with dim Kp = 4,
the kill set of a ↦→ Ca,∗ (p) is the three-dimensional space quniv
= spanR {p, ℓ16 , ℓ16 · p}.
p
(2) Theorem 4.3 (Pathion Dyadic Q-Centralizer Vanishing): at pathion-aphanic p with
(32)
Spec(Gp ) = {0, ∥p∥2 , 2∥p∥2 }, the kill set extends to a five-dimensional space qp
=
ι1 (Vp ) ⊕ Rℓ16 ⊕ ι2 (Vp ).
(3) Theorem 5.1 (Pathion Clifford Triad): the three operators Lp , Lℓ16 , Lℓ16 ·p on P are skewsymmetric, mutually orthogonal, and pairwise anti-commute.
(4) Theorem 5.7 (Octonion Ω Identity): for all A, B, c ∈ O, Ā(Bc) + B̄(Ac) − (cB̄)A −
(cĀ)B = 0.
(32)

(5) Theorem 6.3 (Z2 -Graded Clifford Sublattice): the dim-5 space qp
decomposes as
anti where each summand is independently Clifford-internal but pairs across the
⊕
q
quniv
p
p
grading are not.
(6) Theorem 7.17 (Two-Regime Dyadic Closure): [La , Gp ] = 0 for a ∈ qanti
at every
p
dyadic basepoint with three-valued Gram spectrum, by distinct mechanisms at canonical Stratum-II and at CD-aligned.

2

Preliminaries

2.1

Cayley–Dickson recursion

We use the canonical recursive Cayley–Dickson product. For a normed ∗-algebra A, its double
A(2) = A ⊕ A has product
(a, b)(c, d) = (ac − d¯b, d a + b c̄)
(1)
and conjugation (a, b)∗ = (ā, −b). Iterating from R produces R → C → H → O → S → P → · · ·
with dimensions 1, 2, 4, 8, 16, 32. We write O for the octonions, S for the sedenions, and P for
the pathions.
2

## PDF page 3

The norm form ∥x∥2 = xx̄ = x̄x ∈ R holds in every Cayley–Dickson algebra. The composition law ∥xy∥ = ∥x∥∥y∥ holds in O but fails in S. Octonions are alternative; sedenions
are flexible but not alternative; this exact transition is the source of the structural phenomena
studied here.
For p = (x, y) ∈ P with x, y ∈ S, write ι1 (x) = (x, 0) and ι2 (y) = (0, y), so p = ι1 (x) + ι2 (y).
The left-multiplication operator Lp acts on P by Lp v = pv, and similarly Rp v = vp. We write
(S)
Lp when the underlying algebra is S, and Lp unambiguously when context fixes the algebra.
We use ℓ16 for the unit doubling generator of P over S, so ℓ16 = (0, 1) and ℓ216 = −1.

2.2

The aphanic locus

Definition 2.1. A point p ∈ P is aphanic if dimR ker Lp > 0. We write P aph ⊂ Im(P) for the
locus of imaginary aphanic points.
The sedenion-level characterization of [1] states that p = ι1 (x) + ι2 (y) ∈ S is aphanic if and
only if x, y ∈ Im(O), ∥x∥ = ∥y∥, and ⟨x, y⟩ = 0. At pathion the analogous characterization
holds in two strata:
Proposition 2.2 (Pathion Aphanic Stratification). For p = ei + ej with i ∈ {1, . . . , 15} and
j ∈ {17, . . . , 31} (so the pathion slot i encodes a sedenion direction s1 and slot j − 16 encodes a
sedenion direction s2 ), p is aphanic if and only if s1 ̸= s2 , and:
 if ⟨s1 , s2 ⟩S = 0 in R15 but the pair lies in a common octonion sub-copy ( Stratum I), then
dim ker Lp = 12 and Spec(Gp ) = {012 , 28 , 412 };
 otherwise ( Stratum II), dim ker Lp = 4 and Spec(Gp ) = {04 , 224 , 44 }, the sedenionrecursive analog.

In what follows, “aphanic” will refer to the generic Stratum II case dim Kp = 4. The structurally important spectral fact is that this spectrum has only three distinct values: 0, ∥p∥2 = 2,
and 2∥p∥2 = 4. At generic aphanic basepoints (random imaginary halves with the orthogonality and equal-norm constraints), the spectrum has eight distinct values {04 , λ41 , . . . , λ47 } with all
multiplicities equal to four, summing to 8 · 4 = 32 = dim P.

2.3

Berry curvature operator and kill set

The closed-form Berry curvature operator [2, Theorem 3.7] attached to an aphanic basepoint p
is
(
)
+
Ca,b (p) = πp Lb G+
(2)
p La − La Gp Lb πp
+
+
where Gp = L⊤
p Lp , Gp is the Moore–Penrose pseudoinverse, and πp = I − Gp Gp is the orthogonal projector onto ker Lp . The operator depends bilinearly on a, b ∈ Im(P).

Definition 2.3 (Kill Set). The kill set of the curvature operator at p is
{
}
K(p) := a ∈ Im(P) : Ca,b (p) = 0 for all b ∈ Im(P) .
The kill set measures the kernel of the linear map a ↦→ Ca,∗ (p) ∈ Hom(Im(P), End(Kp )).
At sedenion the kill set is the canonical qp = ι1 (Vp ) ⊕ Rℓ ⊕ ι2 (Vp ) of dimension 5, where
Vp = spanR {x, y} ⊂ S [2, R133]. The pathion lift of this statement is the central object of this
paper, and it splits into two distinct theorems with different rigor sources.

3

## PDF page 4

Status conventions. Proof vocabulary (prove, proved, proven) is reserved in this paper
for claims established symbolically. Computational witnesses carry a separate vocabulary: a
certification states its epistemic basis, either a numerical tolerance or exact (exhaustive finite
verification or exact arithmetic), and is never restated as a proof. Where a theorem’s two
directions have different rigor sources, each direction’s basis is stated in place; in particular, the
necessity directions of Theorems 4.1 and 4.3 are numerical certifications, not proofs. Citations
of the form “v47-A22” or “framework state” refer to the author’s internal research ledger of
promoted results; the sedenion-level foundations are published in the two companion papers
[1, 2], and framework-ledger material cited here should be read as announced, with proofs of
record in that ledger.

3

Pathion spectrum stratification

The defining feature distinguishing pathion from sedenion is the loss of orbit invariance of the
Gram spectrum. At sedenion, Spec(Gp ) is the universal triple {04 , 28 , 44 } for every aphanic p.
At pathion this universality fails:
Proposition 3.1 (Spectrum Non-Invariance). There exist aphanic p, p′ ∈ PPaph with dim Kp =
dim Kp′ = 4 and ∥p∥ = ∥p′ ∥ such that Spec(Gp ) ̸= Spec(Gp′ ). Specifically, dyadic basepoints
of the form p = ei + ej (in a Stratum II configuration of Proposition 2.2; canonical representative p = e1 + e26 ) have the three-valued spectrum {04 , ∥p∥2 24 , 2∥p∥2 4 }, while random aphanic
basepoints have an eight-valued spectrum {04 , λ41 , . . . , λ47 }.
The structural consequence is computational: at dyadic basepoints, the pseudoinverse G+
p
7
3
2
admits a closed-form Lagrange-3 polynomial representation G+
p = 4∥p∥4 Gp − 4∥p∥6 Gp , while at
generic aphanic basepoints the pseudoinverse must be obtained from an eigendecomposition.
This distinction is the technical reason why the kill set has different dimensions in the two
regimes (Theorems 4.1 and 4.3 below).
Orbit-level refinement of Proposition 3.1. The non-invariance recorded above has since
been resolved into a partial orbit classification in subsequent framework work, which we record
here as cross-reference rather than reprove. Let A, B ⊂ PPaph denote, respectively, the loci
of pathion-aphanic basepoints with ∥p∥2 = 2 and Gram spectrum {012 , 28 , 412 } (Class A) or
{04 , 224 , 44 } (Class B Stratum II ). Two facts are established outside the present paper:
1. Class A complement spectrum theorem (R138). On the six named dyadic Class
A subcases enumerated in the framework state, Spec(Gp ) = {012 , 28 , 412 } uniformly; this
spectrum is the defining Class A property. What R138 proves is the complement spectrum
theorem: for the complement operators Gk := Mk⊤ Mk (with Mk = A − Tk , k ∈ {2, 4, 6}
indexing the three outer cosets), Spec(Gk ) = {012 , 28 , 412 } as well, via the per-octonion-sub
identity Gk |Op = 2I8 combined with Gk |O⊥
= 4 πpgr , where πpgr is the rank-4 orthogonal
p
projector onto the graph of the isometry +Φp within each outer coset (not the kernel
projector πp of this paper). Proven and promoted in the framework state at v46-C18
close.
2. Class B Stratum II three-orbit classification (R140). Every p ∈ B lies in exactly
one of three G2 -orbits: canonical G2 · (e1 + e26 ), mirror G2 · (e11 + e20 ), or broken-mirror
balanced G2 · p3 , where p3 = √12 (e1 + e25 + e10 + e18 ) satisfies Spec(Gp3 ) = {04 , 224 , 44 }
together with cb2can (p3 ) = 12 and cb2mir (p3 ) = 4. The third orbit was discovered as a
refutation of an earlier two-layout exhaustion conjecture and is not in either of the two
named layouts of R139 (the prior two-layout sufficient-condition theorem at v47-A7). R140
strictly extends R139 without modifying it; R139’s two-layout scope remains correct as
4

## PDF page 5

a sufficient condition. Proven and promoted in the framework state at v47-A22 close via
two new lemmas: a G2 -equivariance lift of the Class B variety and a sign-correlation rule
sign(α1 )sign(β2 ) = sign(β1 )sign(α2 ) derived from the collapse of the three independent
Class B trace conditions to a single parity equation P = 1, where P := s1 s25 s10 s18 .
The eight-valued generic-aphanic class (Class C ) remains open as an orbit classification; its
separability by a natural 10-tuple of continuous G2 -invariants is, however, resolved negatively
on a local/generic neighborhood by R142, and the residual rank-3 deficiency is then closed
positively by an explicit 13-tuple of local coordinates on a dense open set (R143). Both are
recorded after the R141 paragraph below. The ρ = 3 single-component-redundancy classes (D,
E, F ) are closed by R141 below.
Structural anatomy of case (3) (v47-A24 to v47-A29). The closed-form anatomy of
the third orbit on its broken-mirror balanced two-parameter family
p(a, b) := a(e1 + e25 ) + b(e10 + e18 ) ∈ P,

(a, b) ∈ R2 ,

was developed in subsequent framework work (v47-A24 through v47-A29). For each of the three
non-trivial 16 + 16 partitions U+∗ ⊕ U−∗ of P, namely the canonical (Q00 ⊕ Q11 , Q01 ⊕ Q10 ), the
mirror (Q00 ⊕ Q10 , Q01 ⊕ Q11 ), and the sed-half (Q00 ⊕ Q01 , Q10 ⊕ Q11 ), the squared off-block
commutator-balance functional cb2∗ (p) := ∥Gp [U+∗ , U−∗ ]∥2F admits a closed form on the family:
cb2can (a, b) = 48 a2 b2 ,
cb2mir (a, b) = 16 (3a4 − 5a2 b2 + 3b4 ),
cb2sed (a, b) = 16 (3a4 − 2a2 b2 + 3b4 ).
√
At the balanced point p3 (i.e. a = b = 1/ 2) these specialize to 12, 4, and 16 respectively,
recovering the numerical values cited above. The canonical formula is derived from path–
Cayley–Dickson multiplication identities via a structural ab-purity argument on the column-pair
signature of Lp and an octonion associator-into-conjugation cancellation (I + KO ) ◦ [Le1 , Re2 ] on
the within-sed-half edges (framework state at v47-A25 close). The double-swap diagonal-block
edges
xQ00 ,Q11 (a, b) = xQ01 ,Q10 (a, b) = 8(3a4 − 5a2 b2 + 3b4 )
underlying cb2mir and cb2sed admit the operator-polynomial form
Gp [Q00 , Q11 ] = a2 · A + b2 · B,

A := I + Le1 Re1 ,

B := KO (I + Le2 Re2 ),

where A = 2P{1,e1 }⊥ and B = −2P{1,e2 }⊥ on O (twice and negative-twice the orthogonal
projectors onto the 6-dimensional subspaces orthogonal to the indicated pairs), with ∥A∥2F =
∥B∥2F = 24 and ⟨A, B⟩F = −20, the inner product traced to the 5 shared oct-basis directions
{e3 , e4 , e5 , e6 , e7 } in {e1 }⊥ ∩ {e2 }⊥ ∩ Im(O) (framework state at v47-A28 close). The mirror
and sed-half quartics follow as partition assemblies of the six edge weights with each unordered
quad pair appearing in exactly two of the three partitions (framework state at v47-A29 close).
At p3 specifically, the canonical 16 × 16 off-block Gp3 [U+can , U−can ] has rank 6, singular spectrum σ = (2, 2, 1, 1, 1, 1), and Frobenius norm squared ∥ · ∥2F = 12, with the closed operatorskeleton identity on the family
Gp [U+can , U−can ](reord) = ab · (M ⊕ N ⊤ )
after a natural column reorder Pcol ∈ O(16) of U−can from (Q01 , Q10 ) to (Q10 , Q01 ). Here
M := Le1 Re2 KO + KO Le2 Le1 KO − KO Le2 Re1 − Le1 Le2
N := KO Re2 Le1 + Re1 Re2 − KO Re1 Le2 − Re2 Re1
5

## PDF page 6

have rank 2 and rank 4 on the quaternion subalgebra H = span(1, e1 , e2 , e3 ) ⊂ O, with M acting
as a single ϵ-tensor on the pair (e1 , e2 ) and N acting as a direct sum of two ϵ-tensors on the
pairs (1, e3 ) and (e1 , e2 ). Both M and N vanish on H⊥ ⊂ O (framework state at v47-A26 close).
The canonical and mirror partitions are not
by any) rank-preserving(σ-bridge: at every
( related
)
can
basepoint p ∈ G2 · p3 in the third orbit, rank Gp [U+ , U−can ] = 6 while rank Gp [U+mir , U−mir ] =
4; since rank is invariant under orthogonal R, C ∈ O(16), signed row/column permutations,
scalar rescaling, and pathion automorphisms ϕ ∈ Aut(P), no identity of the form Gp [U+mir , U−mir ] =
ε · R · Gp [U+can , U−can ] · C exists. The four magnitude-1 singular values are nevertheless common
to the canonical and mirror off-blocks at p3 ; the canonical off-block carries two additional
magnitude-2 singular values originating from N ’s (1, e3 ) ϵ-tensor block (the unique-to-β realto-e3 coupling), which has no mirror-partition counterpart (framework state at v47-A27 close).
The Class A complement spectrum theorem R138 and the Class B Stratum II threeorbit classification theorem R140 recorded above are unchanged by this anatomy. No new
R-promotion is claimed at v47-A24 through v47-A29; the closed forms and operator identities
above supply structural derivations of the third-orbit anatomy that had previously been available in framework state via symbolic computation. The eight-valued class C remains open as
a classification (its 10-tuple local/generic non-separation is recorded as R142, after the R141
paragraph); classes D, E, F are resolved by R141 in the following paragraph.
Class D/E/F cross-quad trace fingerprint (R141). The preceding three-valued spectrum classes (A, B) do not exhaust the pathion-aphanic locus. Let the oct-rank ρ(p) :=
rankO (α1 , β1 , α2 , β2 ) denote the number of linearly independent octonion-imaginary components
in the four-quad decomposition of p. Classes A (ρ = 1) and B (ρ = 2) have been treated above.
The remaining cases with ρ = 3 (i.e., exactly one single-component redundancy pdep = ± ptgt
among
quad directions) produce quadratic-irrational Gram spectra (eigenvalues involv√ the
√ four √
ing 2, 3, or 5) and split into three classes according to the position of the redundancy:
 Class D (ABcross = 1, SedCross = 1): redundancy crosses both the (α, β) pair index
and the sedenion-half index, e.g. β2 = α1 .
 Class E (ABcross = 1, SedCross = 0): redundancy crosses the pair index within one
sedenion half, e.g. β1 = α1 .
 Class F (ABcross = 0, SedCross = 1): redundancy is a proportionality within one pair
across sedenion halves, e.g. α2 ∥ α1 after aphanic projection.

We record the following cross-referenced theorem, established outside the present paper at
framework state v47-B10 close.
3. Class D/E/F cross-quad trace fingerprint, canonical golden-ratio block, and
full-versus-local eigenspace split (R141). Let p ∈ PPaph at ∥p∥2 = 2 with ρ(p) = 3
and class label determined by the (ABcross, SedCross) predicate above. Recall the octquad partition Q00 , Q01 , Q10 , Q11 of P and the canonical partition U+can = Q00 ⊕ Q11 ,
U−can = Q01 ⊕ Q10 already used above.
(i) Universal block form. For any ρ = 3 class,
[
]
∣
2I
M
8
p
Gp ∣U can =
,
Mp := Gp [Q00 , Q11 ],
+
Mp⊤ 2I8
where the diagonal 2I8 blocks follow from the Per-Quad-Diagonal-Block Lemma (A12-2.1)
at aphanic + ∥p∥2 = 2.
(ii) Trace fingerprint (G2 -orbit invariant). tr(Mp ) = 6 for Class D and tr(Mp ) = 0 for
Classes E and F. The Frobenius norm satisfies ∥Mp ∥2F = 8 at the canonical basepoints of
6

## PDF page 7

all three classes (hence on their G2 -orbits, by the equivariance below). Both invariants are
preserved under the lifted G2 -action gP = diag(gO × 4) ∈ Aut(P) for gO ∈ G2 = Aut(O),
⊤ (Lemma R141.1).
via the orthogonal similarity MgP ·p = gO Mp gO
(iii) Class D two-orbit ς-stratification. Across the 210 oct-permutation Class D variants {(a, b, c) : a, b, c ∈ {1, . . . , 7}, distinct}, the singular-value tuple ς(M ) takes exactly
two values, each a single G2 -orbit:
5
 Fano-triple
√ orbit (42 = 7 Fano lines × 3! members): ς(M ) = (0, 1/φ, 1 , φ) with
φ = (1 + 5)/2.
√
 Non-Fano orbit (168 = 210 − 42 members): ς(M ) = (02 , 1/φ, 13 , 2, φ).

The Fano orbit is characterized by the condition that the redundancy triple (β1 , α2 , α1 )
lies on a Fano line of the octonion multiplication table.
(iv) Canonical
golden-ratio block. At the canonical Class D Fano-orbit representative
√
pcan
=
(1/
2)(e
1 + e11 + e18 + e25 ), the 8 × 8 block M decomposes as
D
(
)
1 0
(2)
M = E10 ⊕
⊕ I4 ,
1 1
[ ]
(2)
where E10 = 01 00 , and the golden-ratio singular values originate from the 2×2 sub-block
√
[ ]
M2 := 11 01 with M2⊤ M2 having eigenvalues (3 ± 5)/2 = φ2 , 1/φ2 .
(v) Full-versus-local V1 split. At canonical Class D, the full Gp eigenvalue-1 eigenspace
V1 ⊂ P (dimension 8) splits perfectly: dim(V1 ∩ U+can ) = dim(V1 ∩ U−can ) = 4. The Hlocalized eigenvalue-1 multiplicity of 5 on U+can decomposes as 4 genuine (from V1 ∩ U+can )
+ 1 spurious (restriction artifact not an eigenvector of the full Gp ).
(vi) Class E/F trace-zero invariance. For canonical Class E: tr(Mp ) = 0 by a cyclictrace cancellation in the per-K-sum expansion, where opposing K-positions generate
±Le1 Re1 K terms with inverted sign. For canonical Class F: tr(Mp ) = 0 by three independent cancellation mechanisms (identity, cyclic K-flip, and non-fixing
residual
√
√ trace-zero
permutations) applied to the per-K-sum with composite β2 = 2/3 e3 − (1/ 6) e1 . Both
invariances lift to the full G2 -orbit by Lemma R141.1 (Lemma R141.3).
The proof stack consolidates v47-B6 (cross-quad identification), v47-B7a (Fano-line signedpermutation trace algebra), v47-B7b (bit-exact block form and golden-ratio discovery),
v47-B7c (V1 split and Class F per-K closure), and v47-B9 (formal G2 -equivariance, finiteexhaustive ς-stratification, and E/F corollary). Promoted and recorded in the framework
state at v47-B10 close. Class D partitions into exactly two G2 -orbits; a continuous ςclassification of the full ρ = 3 locus is not claimed. A representation-theoretic explanation
of why Fano-triple =⇒ golden-ratio singular values is an open question.
Class C 10-tuple local/generic incompleteness (R142). The generic eight-valued class
C (ρ = 4: the four quad directions α1 , β1 , α2 , β2 are octonion-linearly independent, dim Kp = 4,
and Spec(Gp ) takes eight distinct values) is, unlike the ρ ≤ 3 classes above, not resolved into
a finite orbit list here. What is established (and recorded as a cross-reference to framework
state v47-C8) is a sharp obstruction to separating its G2 -orbits by a natural tuple of continuous
invariants. Let
(
)
F = I2 , I4 , tr G2p , tr G3p , tr G4p , tr G5p , tr G6p , J3 , J4 , J5 : M → R10
be the 10-tuple of continuous G2 -invariant functions on the open Class C locus M , with I2 =
∥α1 ∥2 + ∥β2 ∥2 , I4 = ⟨α1 , β2 ⟩ + ⟨β1 , α2 ⟩, J3 = ⟨[α1 , β1 ], [α2 , β2 ]⟩, J4 = ⟨[α1 , β1 , α2 ], β2 ⟩, J5 =
⟨α1 , α2 ⟩⟨β1 , β2 ⟩ − ⟨α1 , β1 ⟩⟨α2 , β2 ⟩, and G2 = Aut(O) acting by gP = diag(gO × 4).
7

## PDF page 8

4. Class C 10-tuple local/generic incompleteness (R142). On a nonempty open
neighborhood of an exhibited regular Class C point, the local manifold M has dimension
27, the G2 -orbit has dimension dO = 14, and rank dF |T M = 10. Consequently the local
G2 -quotient has dimension 27 − 14 = 13 > 10, and F does not separate the G2 -orbits of
M : there exist distinct G2 -orbits with equal F -value, and the local/generic separation
deficiency is exactly 13 − 10 = 3.
Proof sketch (exact single-point witnesses; framework v47-C7/C7b/C8). The three dimension counts are certified at one exact rational Class C witness q (an integer aphanic pathion
with ⟨s1 , s2 ⟩ = 0, ∥s1 ∥2 = ∥s2 ∥2 , oct-rank 4, dim ker Lq = 4, and eight distinct Gq -eigenvalues),
each rank established by a nonzero exact minor rather than a floating-point threshold: (L1)
the 3 × 3 constraint-gradient minor has determinant 80 ̸= 0, so dim M = 27; (L2) the 21 × 30
matrix of the g2 derivations Da,b = [La , Lb ] + [La , Rb ] + [Ra , Rb ] applied block-diagonally has
a nonzero 14 × 14 minor, and since dO ≤ dim g2 = 14 this forces dO = 14 (so q is regular,
with finite isotropy); (L3) the tangent-projected Jacobian dF |T M has a nonzero 10 × 10 minor,
so rank dF |T M = 10 (the Jacobian was independently re-derived along a truncated-polynomial
path, 300/300 entries agreeing, with an integer 13 × 13 cross-check of [ C; dF ]). Two further
exact certificates close the descent: (K1) dF · Orb⊤ = 0, the single-point confirmation of the
(independently established) global G2 -invariance of F , so the 14-dimensional orbit lies in ker dF ;
and (K2) C · Orb⊤ = 0, so the orbit is tangent to M . Each construction is homogeneous in p,
√
so the ranks at the integer point q equal those at the unit-norm point p0 = q/ c ∈ M (scaling
multiplies each matrix row by a nonzero constant and fixes T = ker C). By the constant-rank
theorem the fiber of F is locally a 27 − 10 = 17-manifold containing the 14-dimensional orbit, hence a 3-parameter family of distinct orbits sharing F ; equivalently, the 13-dimensional
slice (slice theorem, G2 compact) cannot inject continuously into R10 (invariance of domain).
No floating-point quantity is load-bearing. Promoted and recorded in the framework state at
v47-C8 close. □
Scope. The statement is local/generic (the dimension counts are certified on the maximalrank neighborhood of one regular witness, not as a density claim) while the non-separation
conclusion itself is unconditional. It is confined to pathion Class C. It does not classify the
Class C G2 -orbits, and does not assert that F is uninformative: the 10-tuple is functionally
independent (its Jacobian has full rank 10) and accounts for 10 of the 13 local orbit coordinates.
(An explicit finite-distance pair of distinct orbits with equal F is exhibited in the constructive
remark below; a continuous, non-inversion such family is left open.) The global “deficiency 3
at all basepoints” is, separately, an empirical framework observation, not part of R142.
Constructive collision witness (exact). The local/generic obstruction of R142 is complemented by an exact, finite-distance collision. Let q be the exact rational Class C witness used
in the R142 certification. Its central inverse −q is again Class C, and F (q) = F (−q) exactly,
because every component of the 10-tuple is an even function of p: I2 , I4 are quadratic, tr Gkp
⊤
is even since G−p = L⊤
−p L−p = Lp Lp = Gp , and J3 , J4 , J5 have degree 4. (This evenness
holds for every pathion; Class C membership of both points is an additional satisfied constraint.) The two representatives are nevertheless not G2 -equivalent: the associative three-form
φ1 (p) = ⟨[α1 , β1 ], α2 ⟩ is G2 -invariant (as Aut(O) preserves the octonion commutator and the
inner product) and odd, and at the witness φ1 (q) = −14 while φ1 (−q) = +14; were −q = g ·q for
some g ∈ G2 we would have φ1 (−q) = φ1 (q), a contradiction. Hence equality of the full 10-tuple
does not imply G2 -orbit equivalence. The remaining invariants agree, e.g. tr G2q = 234145504,
J3 = 98560, J4 = 48128, J5 = −70217 (all equal for q and −q), and the pair is at finite distance ∥q − (−q)∥2 = 8120 = 4∥q∥2 . All values are exact integers; no floating point enters.
This realizes the non-separation by an exact parity / orientation blindness (F is even while
the orbit-separating associative three-forms are odd) and is confined to the central-inversion

8

## PDF page 9

collision; a continuous, non-inversion finite-distance family and a global orbit classification both
remain open.
Class C 13-tuple local full-rank (R143). The local separation deficiency of exactly 3
counted by R142 is closed, generically, by the three associative G2 -orientation three-forms.
Adjoin to the 10-tuple F the forms φ1 (p) = ⟨[α1 , β1 ], α2 ⟩ (the odd invariant of the collision witness above), φ2 (p) = ⟨[α1 , β1 ], β2 ⟩, and φ3 (p) = ⟨[α1 , α2 ], β2 ⟩ (all G2 -invariant because Aut(O)
preserves the octonion commutator and the inner product) and set
(
)
F13 = I2 , I4 , tr G2p , . . . , tr G6p , J3 , J4 , J5 , φ1 , φ2 , φ3 : M → R13 .
5. Class C 13-tuple local full-rank (R143). On a dense Zariski-open subset of the
Class C stratum, rank dF13 |T M = 13; equivalently F13 is a full-rank local coordinate
system for the 13-dimensional local Class C quotient there, with fibers the G2 -orbits. The
three forms φ1 , φ2 , φ3 supply exactly the 3 orbit directions invisible to the R142 10-tuple.
Proof sketch (exact; no symbolic determinant; framework v47-C12 / C13). The augmented
Jacobian A = [ C; dF13 ] ∈ (Z[p])16×30 has integer-polynomial entries (constraint gradients
⊤
⊤
linear; spectral rows k tr(Gk−1
p (Bm Lp + Lp Bm )); the octonionic and φ rows gradients of degree≤ 4 integer-coefficient invariants). A distinguished 16 × 16 minor MJ ∈ Z[p] evaluates to
−1.9042 . . . × 1043 ̸= 0 at the exact rational Class C witness q, so MJ ̸≡ 0; hence U = {p :
MJ (p) ̸= 0} is a nonempty Zariski-open subset on which rank A = 16 (corroborated by nonzero
16 × 16 minors at the witness, ∥p∥2 = 70, and at two further independent Class C points,
∥p∥2 = 78, 106). By rank(D|ker C ) = rank[ C; D ] − rank C, the full row rank forces rank C = 3
and rank dF13 |T M = 13 on U . All 13 components are G2 -invariant, so the 14-dimensional orbit
(the generic value dO = 14 from R142) lies in ker dF13 |T M ; with rank 13 the kernel is exactly
the orbit, so F13 is a local submersion onto R13 with orbit fibers: local coordinates / local orbit
separation by the implicit function theorem.
Density (Lemma L-C13.1, framework v47-C13). The Class C stratum is cut out by ⟨s1 , s2 ⟩ =
0, ∥s1 ∥2 = ∥s2 ∥2 , ∥p∥2 = 2, that is, it is the Stiefel manifold V2 (R15 ) of orthonormal 2-frames
in R15 . By Witt’s extension theorem SO(15) acts transitively on such frames, so V2 (R15 ) is
a single orbit of the connected group SO(15, R) and its complexification V2 (C15 ) is a single
SO(15, C)-orbit, an irreducible affine variety of dimension 2 · 15 − 3 = 27, in which V2 (R15 )
is Zariski-dense. A nonzero polynomial on an irreducible variety has nowhere-dense zero set,
so U is in fact a dense Zariski-open subset, and the full-rank locus is dense in the Class C
stratum. No floating-point quantity is load-bearing. Promoted at v47-C12; scope sharpened
from “nonempty” to “dense” Zariski-open at v47-C13. □
Scope. R143 is the positive companion to R142: where R142 counts the local separation
deficiency (13−10 = 3), R143 exhibits the three explicit invariants φi that remove it and furnish
local coordinates on a dense open set. The statement is local (separation of nearby orbits via
the implicit function theorem) and does not assert global orbit separation: the central inversion
q ↦→ −q shows the odd φi separate that particular pair, but global injectivity on V2 (R15 )/G2
and a continuous, non-inversion collision both remain open. Confined to pathion Class C; the
rank may drop on the nowhere-dense closed set {MJ = 0}.

4

Two pathion Q-centralizer vanishing theorems

4.1

The universal kill set

Theorem 4.1 (Pathion Universal Kill Set). Let p ∈ PPaph with dim Kp = 4. Then
K(p) = quniv
:= spanR {p, ℓ16 , ℓ16 · p},
p

dimR quniv
= 3.
p

(Sufficiency is proved symbolically; necessity is a numerical certification, Appendix A.)
9

## PDF page 10

The proof proceeds via a centralization chain. Define
Gp = L⊤
p Lp ,

πp = I − Gp G+
p.

Lemma 4.2 (Centralization Chain). For any a ∈ Im(P), the following implications hold:
{La , Lp } = 0 =⇒ [La , L2p ] = 0 ⇐⇒ [La , Gp ] = 0 =⇒ [La , πp ] = 0 =⇒ Ca,b (p) = 0 ∀b.
Proof. The first implication is two lines: {La , Lp } = 0 gives La Lp = −Lp La , hence La L2p =
(La Lp )Lp = −(Lp La )Lp = −Lp (La Lp ) = L2p La .
The second equivalence uses Gp = −L2p , which follows from L⊤
p = −Lp for p ∈ Im(P) (since
p̄ = −p implies L⊤
=
L
=
−L
).
p̄
p
p
The third implication uses the spectral theorem: πp is the orthogonal projector onto ker Gp
and is therefore a polynomial in Gp over the spectrum of Gp . Hence anything commuting with
Gp commutes with πp .
The final implication is the formal collapse of (2): using [La , πp ] = 0 to move πp across La ,
+
+
and G+
p πp = πp Gp = 0 (since Gp ∈ R[Gp ] vanishes on ker Gp ),
+
Ca,b (p) = πp (Lb G+
p La − La Gp Lb )πp
+
= πp Lb G+
p (La πp ) − (πp La )Gp Lb πp
+
= πp Lb (G+
p πp )La − La (πp Gp )Lb πp

= 0.
Proof of Theorem 4.1. Sufficiency (quniv
⊆ K(p)): By Lemma 4.2 it suffices to show {La , Lp } =
p
2
0 for a ∈ {p, ℓ16 , ℓ16 · p}. For a = p, {Lp , Lp } = 2L2p = −2L⊤
p Lp = −2Gp , so [Lp , Lp ] = 0 trivially
and the conclusion follows directly from the rest of Lemma 4.2. For a = ℓ16 and a = ℓ16 · p, the
anti-commutation is the content of the Pathion Clifford Triad Theorem (Theorem 5.1), proven
in Section 5.
31×31 with entries
univ
Necessity
∑ (K(p) ⊆ qp ): Construct the symmetric matrix ΓC ∈ R
(ΓC )a,a′ = b ⟨Ca,b (p), Ca′ ,b (p)⟩F where the sum runs over a basis of Im(P) and the inner product
is the Frobenius product on End(Kp ). The kill set is exactly ker ΓC . Computational certification
across N = 16 random aphanic basepoints (Appendix A) shows dim ker ΓC = 3 and that quniv
⊆
p
ker ΓC at machine precision. The nullity is an integer conclusion read from a floating-point
computation: this direction is a certification, not a proof. Granting the certified nullity, equality
follows by dimension count.

4.2

The dyadic extension

Theorem 4.3 (Pathion Q-Centralizer Vanishing at Dyadic Basepoint). Let p ∈ PPaph with
Spec(Gp ) = {04 , ∥p∥2 24 , 2∥p∥2 4 }. Then
K(p) = q(32)
:= ι1 (Vp ) ⊕ Rℓ16 ⊕ ι2 (Vp ),
p

dimR q(32)
= 5,
p

where Vp = spanR {s1 , s2 } for p = ι1 (s1 ) + ι2 (s2 ). (Sufficiency is proved symbolically; necessity
is a numerical certification at canonical Stratum-II, Appendix A.)
(32)

Proof. Sufficiency (qp ⊆ K(p)): For a ∈ quniv
, [La , Gp ] = 0 follows from the Pathion Clifford
p
Triad Theorem 5.1 via the centralization chain Lemma 4.2. For a ∈ qanti
p , [La , Gp ] = 0 holds at
every dyadic basepoint by the Two-Regime Dyadic Closure Theorem 7.17 (proven in §7). By
(32)
(32)
linearity in a and the decomposition qp = quniv
⊕ qanti
p
p , [La , Gp ] = 0 holds for every a ∈ qp ,
(32)

hence by Lemma 4.2, [La , πp ] = 0 and Ca,b (p) = 0 for all b ∈ Im(P). Equivalently, qp
See also Corollary 7.18.
10

⊆ K(p).

## PDF page 11

(32)

Necessity (K(p) ⊆ qp ): By the same nullity argument as in Theorem 4.1, using a ΓC spectrum analysis whose details are recorded in the certification appendix. Computational
certification across canonical Stratum-II dyadic basepoints (Appendix A) shows dim ker ΓC = 5
(32)
and qp ⊆ ker ΓC at machine precision. As in Theorem 4.1, this direction is a certification, not
a proof; granting the certified nullity, equality follows by dimension count.
Remark 4.4. The dim-5 extension at dyadic basepoints does not arise from additional Clifford
anti-commutation with the universal triad: as we show in Section 6, the anti-symmetric extensions form a Clifford pair internally (Theorem 6.3 (2)) but do not anti-commute with the universal triad. The mechanism for their centralization with Gp at dyadic basepoints is the two-regime
closure of §7: at canonical Stratum-II, Lw is block-diagonal in the Gp -eigenspace decomposition
(Theorem 7.13); at the CD-aligned subfamily, {Lw , Lp } = 0 holds directly (Lemma 7.14); the
u-side closure {Lu , Lp } = 0 holds across the entire dyadic family (Lemma 7.6). The closed7
3
2
form Lagrange-3 pseudoinverse G+
p = 4∥p∥4 Gp − 4∥p∥6 Gp is consistent with the closure but not
load-bearing: every step of the two-regime derivation works directly from the half-localization,
block-diagonality, or octonion-flexibility identities without invoking the polynomial form of G+
p.
At generic aphanic, all three regime mechanisms fail (Remarks 7.7, 7.12, 7.16) and K(p) collapses
to quniv
.
p

5

The pathion Clifford triad

The structural heart of the universal-kill-set theorem is the following result, which we prove
algebraically.
Theorem 5.1 (Pathion Clifford Triad). Let p ∈ PPaph with dim Kp = 4. The three operators
Lp , Lℓ16 , Lℓ16 ·p acting on P satisfy:
1. L⊤
a = −La for each a ∈ {p, ℓ16 , ℓ16 · p} (skew-symmetry).
2. {La , Lb } = 0 for distinct a, b in the triad (pairwise anti-commutation).
3. ⟨a, b⟩ = 0 for distinct a, b in the triad (mutual orthogonality).
Properties (1) and (3) are formal facts at any Cayley–Dickson level; property (2) is the substantive content. Note that the three operators do not satisfy the alternative-algebra normalization L2a = −∥a∥2 I, since pathion is non-alternative. They form a Clifford-like triad without
scalar squares: generators of an anti-commuting set without a Clifford module structure on P.
The proof of property (2) decomposes into three pairs, of which the first two follow from a
single lemma and the third reduces stepwise through sedenion and octonion identities.

5.1

The first two pairs: Lemma A

Lemma 5.2 (Lemma A). For any p̃ = (a, b) ∈ Im(P) with a, b ∈ Im(S), and any v ∈ P:
[p̃, ℓ16 , v] + [ℓ16 , p̃, v] = 0.
Proof. Direct expansion using the Cayley–Dickson product (1). Compute p̃ · ℓ16 = (−b, a) and
ℓ16 · p̃ = (b, −a). For v = (v1 , v2 ), expand the four products (p̃ · ℓ16 ) · v, p̃ · (ℓ16 · v), (ℓ16 · p̃) · v,
and ℓ16 · (p̃ · v), using ā = −a, b̄ = −b, and (xy)∗ = ȳx̄. Both halves of [p̃, ℓ16 , v] + [ℓ16 , p̃, v]
reduce to sums of sedenion commutators that cancel termwise:
(
)
(
) (
)
[p̃, ℓ16 , v] + [ℓ16 , p̃, v] 1 = − [b, v1 ] + [a, v̄2 ] + [b, v1 ] − [a, v̄2 ] = 0,
(
)
(
) (
)
[p̃, ℓ16 , v] + [ℓ16 , p̃, v] 2 = [b, v2 ] + [a, v̄1 ] + − [b, v2 ] − [a, v̄1 ] = 0.
11

## PDF page 12

The standard non-associative-algebra identity {La , Lb }v = (ab + ba)v − ([a, b, v] + [b, a, v])
combined with p̃ℓ16 + ℓ16 p̃ = 0 (direct CD computation) and Lemma 5.2 immediately gives
{Lp̃ , Lℓ16 } = 0 as operators on P.
Setting p̃ = p closes the pair (p, ℓ16 ). Setting p̃ = ℓ16 ·p = (s2 , −s1 ) closes the pair (ℓ16 ·p, ℓ16 ).

5.2

The third pair: reduction to a sedenion identity

The remaining pair is (p, ℓ16 · p). Set q = ℓ16 · p. Algebra-level: pq + qp = ∥p∥2 ℓ16 − ∥p∥2 ℓ16 = 0
by direct CD. The associator content is the substantive part.
Proposition 5.3 (∆-Reduction). Let p = (s1 , s2 ) ∈ Im(P) with s1 , s2 ∈ Im(S), and let q =
ℓ16 · p = (s2 , −s1 ). Then for every v = (v1 , v2 ) ∈ P,
(
)
[p, q, v] + [q, p, v] = − ∆(s1 , s2 ) v1 , +∆(s1 , s2 ) v2 ,
(S)

(S)

(S)

(S)

where ∆(a, b) := {La , Lb } − {Ra , Rb } is a sedenion-level operator on S.
Proof. Direct CD expansion of [p, q, v] + [q, p, v] produces four groups of terms. The mixed
cross-half terms involving products of the form si (v̄2 si ) and (si v̄2 )si cancel in pairs by sedenion
flexibility [s, w, s](S) = 0, since S is flexible. The same-half terms reduce, after using s̄i = −si ,
to L(S) and R(S) anti-commutators acting on v1 and v2 respectively, with the structure asserted
in the proposition. The detailed computation, while tedious, uses no identity beyond flexibility,
the imaginarity of s1 , s2 , and CD recursion.
Theorem 5.4 (Sedenion ∆ Identity). For all a, b ∈ Im(S):
(S)

(S)

(S)
∆(a, b) := {L(S)
a , Lb } − {Ra , Rb } = 0

as operators on S.

Remark 5.5 (Orthogonality not required). The orthogonality assumption ⟨a, b⟩ = 0 is unnecessary. The inner-product term (ab + ba) = −2⟨a, b⟩ contributes identically to {La , Lb } and
{Ra , Rb }, so it cancels in ∆ regardless of ⟨a, b⟩. Numerical certification (Appendix A) confirms
∆ = 0 across both orthogonal and non-orthogonal random imaginary pairs at machine precision.
The proof of Theorem 5.4 uses a four-block CD decomposition that reduces the sedenion
identity to a pure octonion identity.

5.3

Four-block decomposition and the Ω identity

For a = (α, A), b = (β, B) with α, β ∈ Im(O) and A, B ∈ O (real parts allowed in A, B, since
the imaginarity of a in S requires only α ∈ Im(O); the second half A may have a real part
as long as the full a = (α, A) ∈ Im(S), which here means α imaginary and A unrestricted),
bilinearity in (a, b) gives
∆(a, b) = ∆(i) + ∆(ii) + ∆(iii) + ∆(iv)
(
) (
)
where
the four) blocks(correspond to) the four CD-decomposition pairs (α, 0), (β, 0) , (α, 0), (0, B) ,
(
(0, A), (β, 0) , and (0, A), (0, B) respectively. By the ∆(x, y) = ∆(y, x) symmetry, ∆(iii) =
∆(ii) .
Lemma 5.6 (Four-block analysis).
(i ) ∆(i) = 0 by octonion alternativity: {Lα , Lβ }O = {Rα , Rβ }O = −2⟨α, β⟩I.
(ii ) ∆(ii) = 0 by octonion associator alternation (consequence of alternativity) combined with
the real-vanishing property of [α, B, c]O for α ∈ Im(O).
(iii ) ∆(iv) has trivially vanishing second half; its first half reduces to the octonion identity Ω
below.
12

## PDF page 13

Theorem 5.7 (Octonion Ω Identity). For all A, B, c ∈ O:
Ω(A, B; c) := Ā(Bc) + B̄(Ac) − (cB̄)A − (cĀ)B = 0.
Proof. Ω is bilinear in (A, B) and symmetric under A ↔ B. By polarization, it suffices to prove
the diagonal Ω(A, A; c) = 0.
The diagonal is
[
]
Ω(A, A; c) = 2 Ā(Ac) − (cĀ)A .
Since O is alternative, by Artin’s theorem the subalgebra ⟨A, c⟩ generated by A and c is
associative. In particular Ā = 2 Re(A) − A ∈ ⟨A⟩ ⊂ ⟨A, c⟩, so:
 Ā(Ac) = (ĀA)c = ∥A∥2 c by associativity in ⟨A, c⟩ and the composition norm form ĀA =
∥A∥2 ∈ R.
 (cĀ)A = c(ĀA) = ∥A∥2 c by the same.

Hence Ω(A, A; c) = 2∥A∥2 c − 2∥A∥2 c = 0. By polarization 2Ω(A, B; c) = Ω(A + B, A +
B; c) − Ω(A, A; c) − Ω(B, B; c) = 0, and over R this gives Ω(A, B; c) = 0.
Proof of Theorem 5.4. By the four-block decomposition and Lemma 5.6, ∆(a, b) = 0 for all
imaginary a, b ∈ Im(S) if and only if the Ω identity holds in O. Theorem 5.7 provides this.
Proof of Theorem 5.1, completion. Property (2) for the pair (p, ℓ16 · p) follows by combining
pq + qp = 0 (direct CD) with Proposition 5.3 and Theorem 5.4. The other two pairs are closed
by Lemma 5.2. Properties (1) and (3) are formal.

5.4

The full symbolic chain

The proof chain is summarized as a sequence of implications, each line implying the one above
it:
(1) R137 step 6: [La , πp ] = 0 for a ∈ quniv
.
p
(2) Centralization with Gram: [La , Gp ] = 0, since Gp = −L2p (formal: L⊤
p = −Lp ) and
πp ∈ R[Gp ].
(3) Anti-commutation: {La , Lp } = 0 (Pathion Clifford Triad, Theorem 5.1).
(4) Two routes to anti-commutation:
 Lemma A closes the pairs (p, ℓ16 ) and (ℓ16 · p, ℓ16 ) by direct CD computation.
 The pair (p, ℓ16 · p) reduces to the sedenion identity ∆(s1 , s2 ) = 0 for imaginary
s1 , s2 ∈ Im(S).

(5) Four-block CD decomposition: ∆ = 0 holds iff each of the four blocks vanishes:
 Case (i): octonion alternativity.
 Case (ii): associator alternation in O.
 Case (iv): the octonion identity Ω(A, B; c) = 0.

(6) Octonion Ω theorem: Ω = 0 follows from polarization, Artin’s theorem on two-generator
subalgebras of O, and the composition norm form ĀA = ∥A∥2 .
Every node is either a formal Cayley–Dickson identity, a classical alternative-algebra fact
(Artin’s theorem, octonion alternativity, the composition norm form), or a generic linear-algebra
fact (polarization, spectral theorem). No empirical content remains.
13

## PDF page 14

6

The Z2 -graded Clifford sublattice
(32)

The dim-5 kill set qp
at dyadic basepoints decomposes naturally relative to the two-half
structure of p = (s1 , s2 ).
Definition 6.1. The symmetric sublattice is quniv
= span{p, ℓ16 , ℓ16 · p}, dimension 3. The
p
(32)

antisymmetric sublattice is qanti
= span{(s1 , −s2 ), (s2 , s1 )}, dimension 2. Together qp
p
univ
anti
qp ⊕ qp , dimension 5.

=

Define the involution σ : P → P by
σ(x, y) = (x, −y)

for (x, y) ∈ P = S ⊕ S · ℓ16 .

This is the second-half-negation map; it satisfies σ 2 = id. The involution acts on the kill set as
follows: σ(p) = (s1 , −s2 ), σ(ℓ16 · p) = (s2 , s1 ), σ(ℓ16 ) = −ℓ16 . Thus σ exchanges the universal
(32)
triad with the set {(s1 , −s2 ), −ℓ16 , (s2 , s1 )}, which spans the same five-dimensional space qp
as quniv
∪ qanti
— the antisymmetric sublattice qanti
is precisely the σ-image of quniv
\ Rℓ16 .
p
p
p
p
Lemma 6.2 (σ is an algebra automorphism). The map σ : P → P, σ(x, y) = (x, −y), is an
algebra automorphism: σ(z · z ′ ) = σ(z) · σ(z ′ ) for all z, z ′ ∈ P.
Proof. Direct Cayley–Dickson computation. With z = (x, y) and z ′ = (c, d):
σ(z · z ′ ) = σ(xc − d¯y, dx + yc̄) = (xc − d¯y, −dx − yc̄),
σ(z) · σ(z ′ ) = (x, −y)(c, −d) = (xc − (−d) (−y), (−d)x + (−y)c̄)
= (xc − d¯y, −dx − yc̄).
The two are identical.
Theorem 6.3 (Z2 -Graded Clifford Sublattice). At every pathion-aphanic basepoint p with
dim Kp = 4:
(1 ) Distinct elements of quniv
pairwise anti-commute as left-multiplication operators.
p
(2 ) Distinct elements of qanti
pairwise anti-commute as left-multiplication operators.
p
(3 ) Mixed pairs (one from each summand) do not in general anti-commute.
Proof. (1) is the Pathion Clifford Triad Theorem 5.1, already proven algebraically.
(2) follows from (1) by σ-transport. Since σ is an algebra automorphism (Lemma 6.2),
left-multiplication operators transport by conjugation:
Lσ(a) = σ ◦ La ◦ σ −1

for all a ∈ P.

(3)

Indeed, Lσ(a) (v) = σ(a)v = σ(a)σ(σ −1 (v)) = σ(a · σ −1 (v)) = (σ ◦ La ◦ σ −1 )(v) by the automorphism property. Anti-commutators therefore transport as well:
{Lσ(a) , Lσ(b) } = σ ◦ {La , Lb } ◦ σ −1 .
In particular {La , Lb } = 0 if and only if {Lσ(a) , Lσ(b) } = 0.
Apply this to the three pairs of the universal triad. Setting u := σ(p) = (s1 , −s2 ) and
w := σ(ℓ16 · p) = (s2 , s1 ):
 {Lp , Lℓ16 } = 0 =⇒ {Lu , L−ℓ16 } = 0 =⇒ {Lu , Lℓ16 } = 0.
 {Lp , Lℓ16 ·p } = 0 =⇒ {Lu , Lw } = 0.

14

## PDF page 15

 {Lℓ16 , Lℓ16 ·p } = 0 =⇒ {Lℓ16 , Lw } = 0.

The second of these is exactly the q antisym pairwise anti-commutation {Lu , Lw } = 0. Together
with the orthogonality and skew-symmetry of u and w (formal at any CD level), this proves (2).
(3) is an empirical observation, certified at machine zero by direct computation across N = 8
random aphanic basepoints (Appendix A); it is not a proved claim. Specifically, {Lp , Lw } and
{Lℓ16 ·p , Lu } have Frobenius norm bounded below by Θ(1) — a 15-order separation from the
within-summand zeros. A symbolic explanation of this asymmetry, in terms of the σ-action on
operator pairs, is sketched in Section 8: the failed mixed pairs (p, w) and (ℓ16 · p, u) are precisely
the pairs in which σ swaps elements within the pair (rather than mapping one element to the
other globally), so the transport argument does not apply.
Remark 6.4 (Two Clifford triads share ℓ16 ). The universal triad {p, ℓ16 , ℓ16 · p} and its σ-image
{u, ℓ16 , w} are both Clifford triads on P, sharing the generator ℓ16 . Together they exhaust the
(32)
dim-5 space qp as span{p, u} ⊕ Rℓ16 ⊕ span{ℓ16 · p, w}. The failed mixed pairs (p, w) and
(ℓ16 · p, u) are precisely the “cross-triad” pairs that involve elements from one Clifford triad and
the σ-conjugate non-corresponding element of the other.
Remark 6.5. The Z2 -grading explains why R136’s dim-5 extension does not require the
Clifford-triad mechanism with the universal triad. The antisymmetric sublattice qanti
is indep
pendently Clifford-internal (this theorem) but does not anti-commute with the universal triad.
The centralization of Gp by elements of qanti
at dyadic basepoints follows instead from the
p
two-regime closure formalized in §7: a half-localization argument (Lemma 7.6) closes the u-side
across all of dyadic; at canonical Stratum-II the w-side closes by block-diagonality of Lw in the
Gp -eigenspace decomposition (Theorem 7.13); at the CD-aligned subfamily the w-side closes
by direct Clifford-anti-commutation {Lw , Lp } = 0 (Lemma 7.14). The Lagrange-3 polynomial
7
3
2
form G+
p = 4∥p∥4 Gp − 4∥p∥6 Gp remains consistent with the closure but is not the load-bearing
element. At generic aphanic the dyadic-only mechanisms fail and K(p) collapses to quniv
.
p

7

The two-regime dyadic closure

The dyadic extension Theorem 4.3 carries, in its v1 proof-sketch form, a residual reliance on the
Lagrange-3 polynomial representation of G+
p as the load-bearing element. The Z2 -grading of §6
pairwise anti-commute (Theorem 6.3 (2), proved
sharpens the question: distinct elements of qanti
p
by σ-transport from the Pathion Clifford Triad Theorem), but the centralization [La , Gp ] = 0 for
a ∈ qanti
does not follow from the centralization chain (Lemma 4.2) alone: {La , Lp } is generically
p
nonzero across the aphanic locus. At dyadic basepoints with three-valued Spec(Gp ), however,
the centralization holds at machine precision. The question raised in §8 (Q1) was whether
the dyadic centralization admits a purely algebraic derivation, and what algebraic mechanism
replaces the failing global anti-commutation.
This section answers both questions. We prove that [La , Gp ] = 0 for every a ∈ qanti
at evp
ery dyadic pathion-aphanic basepoint, by a two-regime mechanism that splits along the dyadic
family. The u-side closes universally across the dyadic family by a half-localization argument
(§7.3). The w-side closes at canonical Stratum-II by a block-decomposition argument identifying Lw as block-diagonal in the Gp -eigenspace decomposition (§7.5–§7.7), and at the Cayley–
Dickson-aligned subfamily by a direct anti-commutation argument (§7.8). The combined result
(Theorem 7.17 in §7.9) upgrades Theorem 4.3’s sufficiency from ”machine-precision sketch” to
”algebraic via two-regime closure”, and resolves the open question (Q1) of §8: the load-bearing
element is not the Lagrange-3 polynomial but the half-localization / block-diagonality / flex
collapse structure catalogued below. The Lagrange-3 form remains consistent with the closure
but is not used in the derivation.

15

## PDF page 16

7.1

Subfamilies and notation

We work throughout with dyadic pathion-aphanic basepoints p = ι1 (s1 ) + ι2 (s2 ) ∈ PPaph whose
Gram spectrum is three-valued. The canonical subfamily is the Stratum II configuration of
Proposition 2.2 with dim Kp = 4; the CD-aligned subfamily carries the Class A signature with
dim Kp = 12. We refine the dyadic family into the following dyadic subfamilies; the entire
closure of this section concerns these subfamilies and does not extend to the eight-valuedspectrum random-aphanic locus.
Definition 7.1 (Dyadic basepoint). A pathion-aphanic p is dyadic when each sedenion half
sk (k = 1, 2) resides entirely in one octonion half of S, i.e., sk ∈ ιS1 (Im(O)) ∪ ιS2 (Im(O)), where
ιS1 , ιS2 : O → S denote the sedenion embeddings of the two octonion halves at the previous
Cayley–Dickson level. Equivalently, in the engine’s basis convention, p = ei + e16+k for some
i ∈ {1, . . . , 15} and k ∈ {2, . . . , 15}; the subfamily k ̸= i+8 is canonical Stratum II (dim Kp = 4),
while the CD-aligned ray k = i + 8 has the Class A spectral signature (dim Kp = 12).
Definition 7.2 (Canonical Stratum-II and CD-aligned subfamilies). Within the dyadic family:
 the canonical Stratum-II subfamily is the set of dyadic basepoints with s1 ∈ ιS1 (Im(O))
and s2 ∈ ιS2 (Im(O)), parameterized as s1 = (r, 0) and s2 = (0, x′ ) in the sedenion CD pair,
with r, x′ ∈ Im(O) unit and ⟨r, x′ ⟩O = 0;
 the CD-aligned subfamily is the set of dyadic basepoints satisfying s2 = s1 ·ℓ8 , equivalently
s1 = (r, 0) and s2 = (0, r) for the same r ∈ Im(O) unit.

The two subfamilies are disjoint by the orthogonality / equality split: canonical Stratum-II
requires r ̸= x′ (and orthogonal), CD-aligned requires r = x′ (i.e., s2 = s1 · ℓ8 ).
The canonical Stratum-II subfamily is the generic one in the ei + e16+k parameterization
with k ̸= i + 8; the CD-aligned subfamily is the single ray of values k = i + 8. The Gram
spectrum multiplicities are (dim E0 , dim E∥p∥2 , dim E2∥p∥2 ) = (4, 24, 4) at canonical Stratum-II
and (12, 8, 12) at CD-aligned, both three-valued in ∥p∥2 · {0, 1, 2}. We write
∑ Eλ for the λeigenspace of Gp and Pλ : R32 → Eλ for the orthogonal projector, so Gp = λ λPλ on the full
pathion module.
Definition 7.3 (Antisymmetric kill-set basis). Following §6 we write
u := σ(p) = (s1 , −s2 ),

w := σ(ℓ16 · p) = (s2 , s1 ),

so qanti
= span{u, w} and u, w ∈ Im(P) as expected. The verification ℓ16 · p = (s2 , −s1 ) (one-line
p
CD-1 calculation) gives σ(ℓ16 · p) = (s2 , s1 ) at once.
Definition 7.4 (Half-embedded operators). For k ∈ {1, 2} set
Ak := Lι1 (sk ) ,

Bk := Lι2 (sk ) .

Linearity of L(·) in its argument gives, for any dyadic basepoint:
Lp = A1 + B2 ,

Lu = A1 − B2 ,

Lw = A2 + B1 ,

Lℓ16 ·p = B1 − A2 .

The first and third decompositions are the load-bearing tools for §7.3 and §7.8, respectively;
the second pair are useful in cross-checks.

7.2

Primitive identities

The closure of the section uses only the following primitive identities, each formal at a fixed
Cayley–Dickson level. We label them for back-reference. All three top-level identities (CD1, CD-2, N-1) hold at every CD level; the next four (O-LA, O-RA, O-AC, oct-flex) live in the
octonions; and the last (sed-flex) lives at sedenion. The four sedenion lemmas L1–L4 are derived
from these primitives by a one-line direct sed-CD walk and are used as compact substitutions
in the worked sub-cases below.
16

## PDF page 17

(CD-1) Cayley–Dickson product. At any level,
(a, b)(c, d) = (ac − d¯b, da + bc̄).
(CD-2) Cayley–Dickson conjugation.

(4)

At any level,

(a, b) = (ā, −b),

(5)

hence y = −y for any imaginary y at any CD level.
(N-1) Composition norm form on imaginaries.
for imaginary y, y 2 = −∥y∥2 .
(O-LA) Octonion left-alternativity.

At any CD level, y ȳ = ȳy = ∥y∥2 ∈ R≥0 ;

For y, z ∈ O, y (yz) = y 2 z.

(O-RA) Octonion right-alternativity.

For y, z ∈ O, (zy) y = z y 2 .

(O-AC) Octonion polarization (anti-commutator on imaginaries).
yz + zy = −2⟨y, z⟩O · 1.

For y, z ∈ Im(O),
(6)

In particular yz + zy = 0 when ⟨y, z⟩ = 0.
(oct-flex) Octonion flexibility. For y, z ∈ O, y (zy) = (yz) y. Equivalently, by Artin’s
theorem on two-generator subalgebras of O, the subalgebra ⟨y, z⟩ is associative, so any associator
with two equal arguments vanishes. This subsumes O-LA and O-RA but we cite the latter where
the proof needs only the alternative form.
(sed-flex) Sedenion flexibility. For a, b ∈ S, a (ba) = (ab) a. Sedenions are flexible but
not alternative; two-generator subalgebras are not in general associative, but the flex identity
(which is the symmetrized weakening of associativity) survives the Cayley–Dickson doubling
from O.
The next four sedenion lemmas package the half-step CD contractions used repeatedly in B1
and B2. We work at canonical Stratum-II with s1 = (r, 0), x = (x′ , 0), s2 = x · ℓ8 = (0, x′ ),
r, x′ ∈ Im(O) unit, ⟨r, x′ ⟩O = 0. (At CD-aligned, the same lemmas hold with x′ = r, but the
orthogonality hypothesis is replaced by the equality.)
Lemma 7.5 (Sedenion lemmas L1–L4). At canonical Stratum-II,
(L1)

s2 · x = +ℓ8 ,

(L2)

s2 · ℓ8 = −x,

(L3)

ℓ8 · s1 = − s1 · ℓ8 ,

(L4)

(s1 · ℓ8 ) · s1 = +ℓ8 ,

s1 · (s1 · ℓ8 ) = −ℓ8 .

Proof. Each follows from a one-line direct sed-CD walk via (4), (5), and N-1 on the unit imaginary r, x′ ∈ Im(O). For (L1), s2 · x = (0, x′ )(x′ , 0) = (0 · x′ − 0̄ · x′ , 0 · 0 + x′ x̄′ ) = (0, ∥x′ ∥2 ) =
(0, 1) = ℓ8 . For (L2), s2 · ℓ8 = (0, x′ )(0, 1) = (0 − 1̄ · x′ , 1 · 0 + x′ 0̄) = (−x′ , 0) = −x. For (L3),
ℓ8 ·s1 = (0, 1)(r, 0) = (−0̄·1, 0+1· r̄) = (0, −r) and s1 ·ℓ8 = (r, 0)(0, 1) = (−1̄·0, 1·r +0) = (0, r),
so ℓ8 s1 = −(s1 ℓ8 ). For (L4), (s1 ℓ8 )s1 = (0, r)(r, 0) = (0 − 0̄ · r, 0 · 0 + rr̄) = (0, 1) = ℓ8 , and
s1 (s1 ℓ8 ) = (r, 0)(0, r) = (−r̄ · 0, r · r + 0) = (0, −∥r∥2 ) = −ℓ8 .
The pair (L4) is the explicit witness that s1 does not commute with s1 ℓ8 in S even though
both lie in commuting subalgebras (s1 ) ⊂ ιS1 (O) and (s1 ℓ8 ) ⊂ ιS2 (O); this asymmetry is exactly
what powers the Lw -action signs ±2 in B1 below.
17

## PDF page 18

7.3

The u-Closure Lemma

Lemma 7.6 (u-Closure Lemma). At every dyadic pathion-aphanic basepoint p = ι1 (s1 ) +
ι2 (s2 ) (in the sense of Definition 7.1), the operators Lu and Lp on P satisfy {Lu , Lp } = 0.
Consequently, by the centralization chain (Lemma 4.2),
[Lu , Gp ] = 0
at every dyadic basepoint, and (the same chain) Lu centralizes the spectral projector πp as well.
The proof has three steps. Step 1 is the linearity reduction {Lu , Lp } = 2(A21 − B22 ), formal at
any CD level. Step 2 is the half-localization lemma computing L2ιk (s) = −∥s∥2 I when s resides
in one octonion half of S; we work all four sub-cases (oct-half × embedding) by direct CD walk
on a generic v = (a, b) ∈ P. Step 3 substitutes the half-localization into the linearity reduction
and uses the aphanic equal-norm condition ∥s1 ∥ = ∥s2 ∥ to collapse the residual to zero.
Proof of Lemma 7.6. Step 1: linearity reduction. By Definition 7.4, Lp = A1 + B2 and
Lu = A1 − B2 . The anti-commutator-of-sum-and- difference identity (formal at any CD level,
no associativity hypothesis on the operators) gives
{Lu , Lp } = (A1 − B2 )(A1 + B2 ) + (A1 + B2 )(A1 − B2 )
= (A21 + A1 B2 − B2 A1 − B22 ) + (A21 − A1 B2 + B2 A1 − B22 )
= 2A21 − 2B22 .
The cross terms A1 B2 and B2 A1 cancel formally; the surviving two terms are scalars (in the
sense established below) by the half-localization lemma in Step 2.
Step 2: half-localization lemma. We claim that for any s ∈ Im(S) residing entirely in
one octonion half of S (i.e., s = (s′ , 0) or s = (0, s′ ) at sed-CD pair, with s′ ∈ Im(O)):
L2ι1 (s) = −∥s∥2 IP ,

L2ι2 (s) = −∥s∥2 IP ,

(7)

as endomorphisms of P. The proof is a direct two-step pathion-CD walk on a generic v =
(a, b) ∈ P, with a, b ∈ S split at sed-CD pair as a = (a1 , a2 ), b = (b1 , b2 ), ak , bk ∈ O. Note ak , bk
are not required to be imaginary; the CD walk handles general octonion components. We work
all four sub-cases.
Sub-case (i): ι1 -embedding, s = (s′ , 0). By (4) at pathion CD:
ι1 (s) · v = (s, 0)(a, b) = (sa − b̄ · 0, bs + 0 · ā) = (sa, bs).
Iterating once more,
ι1 (s)2 · v = (s, 0)(sa, bs) = (s(sa), (bs)s).
We expand each sed-component via (4) at sed-CD on s = (s′ , 0) and a = (a1 , a2 ):
sa = (s′ , 0)(a1 , a2 ) = (s′ a1 , a2 s′ ),
and on b = (b1 , b2 ):

bs = (b1 , b2 )(s′ , 0) = (b1 s′ , −b2 s′ ),

where the second-half sign uses (5): 0̄ = 0, but the sed-CD form has the s̄′ contribution to the
second slot, and s̄′ = −s′ (s’ imaginary in O, by N-1). Iterating:
s(sa) = (s′ , 0)(s′ a1 , a2 s′ )
(
)
= s′ (s′ a1 ) − a2 s′ · 0, (a2 s′ )s′ + 0 · s′ a1
(
)
= s′ (s′ a1 ), (a2 s′ )s′ ,
18

## PDF page 19

(bs)s = (b1 s′ , −b2 s′ )(s′ , 0)
(
)
= (b1 s′ )s′ − 0̄ · (−b2 s′ ), 0 · (b1 s′ ) + (−b2 s′ ) · s′
(
)
(
)
= (b1 s′ )s′ , (−b2 s′ )(−s′ ) = (b1 s′ )s′ , (b2 s′ )s′ .
The four octonion-slot products collapse by O-LA / O-RA / N-1:
O-LA

N-1

(a2 s′ )s′ = a2 (s′ )2 = −∥s′ ∥2 a2 ,

O-RA

N-1

(b2 s′ )s′ = b2 (s′ )2 = −∥s′ ∥2 b2 .

s′ (s′ a1 ) = (s′ )2 a1 = −∥s′ ∥2 a1 ,
(b1 s′ )s′ = b1 (s′ )2 = −∥s′ ∥2 b1 ,

O-RA

N-1

O-RA

N-1

Reassembling:
ι1 (s)2 · v =

(

)
(−∥s′ ∥2 a1 , −∥s′ ∥2 a2 ), (−∥s′ ∥2 b1 , −∥s′ ∥2 b2 ) = −∥s′ ∥2 v = −∥s∥2 v,

using ∥s∥ = ∥s′ ∥ when s = (s′ , 0) ∈ S. ✓
Sub-case (ii): ι1 -embedding, s = (0, s′ ). The pathion expansion is the same, ι1 (s)2 v =
(s(sa), (bs)s), but the sed-CD products differ. With s = (0, s′ ), a = (a1 , a2 ):
sa = (0, s′ )(a1 , a2 ) = (−a¯2 s′ , s′ a¯1 ),

bs = (b1 , b2 )(0, s′ ) = (−s̄′ b2 , s′ b1 ) = (s′ b2 , s′ b1 ),

where the last equality uses s̄′ = −s′ . Iterating:
s(sa) = (0, s′ )(−a¯2 s′ , s′ a¯1 )
(
)
= − s′ a¯1 · s′ , s′ · −a¯2 s′ ,
where the first slot uses 0 · (−a¯2 s′ ) = 0 and the −d¯· b = −s′ a¯1 · s′ term, and the second slot uses
(s′ a¯1 ) · 0 = 0 and the bc̄ = s′ · −a¯2 s′ term. The conjugates simplify:
s′ a¯1 = (a¯1 )∗ (s′ )∗ = a1 · (−s′ ) = −a1 s′ ,

−a¯2 s′ = −((s′ )∗ (a¯2 )∗ ) = −(s̄′ a2 ) = s′ a2 .

Substituting:
s(sa) =

(

− (−a1 s′ )s′ , s′ · s′ a2

)

=

(

(a1 s′ )s′ , (s′ )2 a2

)

= (−∥s′ ∥2 a1 , −∥s′ ∥2 a2 ),

the last equality by O-RA on (a1 s′ )s′ = a1 (s′ )2 and the scalar (s′ )2 a2 via N-1 (no O-LA needed
since the scalar (s′ )2 ∈ R ⊂ O centralizes a2 ). Similarly,
(bs)s = (s′ b2 , s′ b1 )(0, s′ )
(
)
= − s̄′ · s′ b1 , (s′ )2 b2
(
)
= s′ (s′ b1 ), (s′ )2 b2 = (−∥s′ ∥2 b1 , −∥s′ ∥2 b2 ),
by O-LA on the first slot (s′ (s′ b1 ) = (s′ )2 b1 ) and N-1 on the second. Reassembling: ι1 (s)2 v =
(−∥s′ ∥2 a, −∥s′ ∥2 b) = −∥s∥2 v. ✓
Sub-case (iii): ι2 -embedding, s = (s′ , 0). By (4):
ι2 (s) · v = (0, s)(a, b) = (−b̄s, sā).
Iterating once,
ι2 (s)2 · v = (0, s)(−b̄s, sā)
)
(
= − sā · s, s · −b̄s
(
)
(
)
= − (as̄)s, s(s̄b) = (as)s, s(sb) ,
the last equality using s̄ = −s for imaginary s ∈ Im(S), hence −(as̄)s = −(a(−s))s = (as)s and
¯ sign in (4)
s(s̄b) = s(−sb) = −s(sb), which corrects to +s(sb) after matching against the −db
19

## PDF page 20

(both signs land on the same final form when carefully tracked through the conjugations). A
direct re-derivation: at sed level with s = (s′ , 0), a = (a1 , a2 ),
as = (a1 , a2 )(s′ , 0) = (a1 s′ , −a2 s′ ),
(
)
(
)
(as)s = (a1 s′ , −a2 s′ )(s′ , 0) = (a1 s′ )s′ , (−a2 s′ )(−s′ ) = (a1 s′ )s′ , (a2 s′ )s′ ,
and by O-RA on each slot, (as)s = (−∥s′ ∥2 a1 , −∥s′ ∥2 a2 ) = −∥s′ ∥2 a. Similarly sb = (s′ , 0)(b1 , b2 ) =
(s′ b1 , b2 s′ ) at sed-CD, and
(
)
s(sb) = (s′ , 0)(s′ b1 , b2 s′ ) = s′ (s′ b1 ), (b2 s′ )s′ = (−∥s′ ∥2 b1 , −∥s′ ∥2 b2 )
by O-LA on the first slot and O-RA on the second. Reassembling: ι2 (s)2 v = ((as)s, s(sb)) =
(−∥s∥2 a, −∥s∥2 b) = −∥s∥2 v. ✓
Sub-case (iv): ι2 -embedding, s = (0, s′ ). The same template with s = (0, s′ ). At sed-CD,
as = (a1 , a2 )(0, s′ ) = (−s̄′ a2 , s′ a1 ) = (s′ a2 , s′ a1 ),
(
)
(
)
(as)s = (s′ a2 , s′ a1 )(0, s′ ) = − s̄′ · s′ a1 , (s′ )2 a2 = s′ (s′ a1 ), (s′ )2 a2 ,
using −s̄′ = s′ and the second-slot bc̄ term reducing directly. By O-LA on the first slot and N-1
on the second, (as)s = (−∥s′ ∥2 a1 , −∥s′ ∥2 a2 ) = −∥s′ ∥2 a. Similarly,
sb = (0, s′ )(b1 , b2 ) = (−b¯2 s′ , s′ b¯1 ),
s(sb) = (0, s′ )(−b¯2 s′ , s′ b¯1 ) =

(

− s′ b¯1 · s′ , s′ · −b¯2 s′

)

=

(

)
(b1 s′ )s′ , (s′ )2 b2 ,

using the same conjugation-collapse as in sub-case (ii). By O-RA on the first slot and N-1 on
the second, s(sb) = (−∥s′ ∥2 b1 , −∥s′ ∥2 b2 ) = −∥s′ ∥2 b. Reassembling: ι2 (s)2 v = −∥s∥2 v. ✓
In all four sub-cases (7) holds, completing the half-localization lemma.
Step 3: aphanic norm cancellation. Substituting (7) into Step 1’s reduction (with
s1 = (s′1 , 0) or (0, s′1 ) in one octonion half by the dyadic hypothesis, and similarly s2 ):
(
)
(
)
(
)
{Lu , Lp } = 2A21 − 2B22 = 2 − ∥s1 ∥2 IP − 2 − ∥s2 ∥2 IP = 2 ∥s2 ∥2 − ∥s1 ∥2 IP .
The aphanic characterization Proposition 2.2 gives ∥s1 ∥ = ∥s2 ∥, hence {Lu , Lp } = 0.
Centralization chain. By Lemma 4.2, {Lu , Lp } = 0 =⇒ [Lu , L2p ] = 0 ⇐⇒ [Lu , Gp ] =
0 =⇒ [Lu , πp ] = 0, which is the second assertion.
Remark 7.7 (Sharpness of the dyadic restriction). The half-localization lemma (7) fails at
random aphanic. If s1 = (α, β) has nonzero components in both octonion halves of S (i.e.,
α, β ∈ O with α, β not both zero in Im(O) part), then the second iteration of ι1 (s1 )· on a
generic v = (a, b) ∈ P produces, in the first sed-half slot of the result, a residual three-octonion
associator
[
]
− ᾱ, a¯2 , β O ,
arising from a sed-CD walk in which the cross-product β̄a2 appears alongside αa1 . The associator is nonzero for generic α, β, a2 ∈ O (octonions are alternative but not associative; three
independent imaginary octonions span a non-associative subalgebra). Consequently L2ι1 (s1 ) ̸=
−∥s1 ∥2 IP at random aphanic, the linearity reduction’s two squared terms no longer cancel, and
{Lu , Lp } is generically nonzero, in agreement with diagnostic v2’s empirical observation of a
Frobenius residual of order Θ(1) for {Lu , Lp } at random aphanic. The dyadic restriction is
therefore sharp: each sk residing in one octonion half is exactly the condition under which the
cross-half octonion associator vanishes.

20

## PDF page 21

7.4

The recovered kernel basis at canonical Stratum-II

For the w-side closure at canonical Stratum-II we work with an explicit basis of ker Lp . The
basis was recovered numerically at canonical Stratum-II by a brute-force enumeration over twocoordinate pathion vectors at p0 = e1 + e26 and a four-point family check; it then admits a
closed-form structural description in terms of the canonical Stratum-II parameters (s1 , x).
Lemma 7.8 (Recovered Kernel Basis). Let p = ι1 (s1 ) + ι2 (s2 ) be a canonical Stratum-II basepoint with s1 = (r, 0), x = (x′ , 0), s2 = x · ℓ8 = (0, x′ ), r, x′ ∈ Im(O) unit, and ⟨r, x′ ⟩O = 0.
Define
v0 = (x, s1 · ℓ8 ),

v1 = (s1 · x, ℓ8 ),

v2 = ℓ16 · v1 ,

v3 = ℓ16 · v0 ,

(8)

all elements of P. Then
(i ) {v0 , v1 , v2 , v3 } ⊂ ker Lp , and
(ii ) spanR {v0 , v1 , v2 , v3 } = ker Lp .
The closed-form expressions for v2 , v3 unfold via (4). Using ℓ16 = (0, 1) ∈ P and the
imaginarity of the second component:
v2 = (0, 1)(s1 x, ℓ8 ) = (−ℓ¯8 · 1, ℓ8 · 0 + 1 · s1 x) = (ℓ8 , −s1 x),
since ℓ¯8 = −ℓ8 at sed (CD-2, ℓ8 imaginary in S) and s1 x = −(s1 x) at sed since s1 x = (rx′ , 0) has
rx′ ∈ Im(O) (orthogonal imaginary octonions multiply to an imaginary by O-AC: rx′ + x′ r =
−2⟨r, x′ ⟩ = 0, so Re(rx′ ) = 12 (rx′ + rx′ ) = 12 (rx′ + x′ r) = 0). Likewise
v3 = ℓ16 · v0 = (0, 1)(x, s1 ℓ8 ) = (−s1 ℓ8 , x̄) = (s1 ℓ8 , −x),
using s1 ℓ8 = −(s1 ℓ8 ) (sed-imaginary, by direct computation (s1 ℓ8 )∗ = (0, r)∗ = (0, −r) = −s1 ℓ8
via (5)) and x̄ = −x (sed-imaginary).
Proof of (i), partial. For k = 0, 1 the kernel inclusions p · vk = 0 are direct CD walks worked
in Lemma 7.9 below. For k = 2, 3 the kernel inclusions follow from the Pathion Clifford
Triad (Theorem 5.1): the anti-commutation {Lp , Lℓ16 } = 0 gives Lp Lℓ16 = −Lℓ16 Lp , hence
p · v2 = Lp Lℓ16 v1 = −Lℓ16 Lp v1 = −Lℓ16 · 0 = 0, and similarly p · v3 = 0 from p · v0 = 0.
The spanning property (ii) is, in this artifact, taken as the basis definition: numerical
certification at the engine level (Section A, post-v8 family check, span residual ≤ 1.57 × 10−16 )
verifies that the four explicit vectors in (8) span the same four-dimensional subspace of P as
the eigenvalue-decomposition basis returned by the engine’s E0 (Gp ) routine. A purely algebraic
proof of (ii) would require showing that the four vectors are linearly independent and exhaust
ker Lp ; the linear-independence half follows from inspecting the explicit pathion-coordinate
forms (no two of v0 , v1 , v2 , v3 have overlapping support in the engine basis at p0 , hence span
dim 4), while the dim-count is supplied by the four-dimensional kernel guaranteed at every
Stratum II basepoint (Proposition 2.2).

7.5

B1: Kernel preservation

Lemma 7.9 (B1 – Kernel Preservation). At every canonical Stratum-II basepoint, Lw preserves
ker Lp : Lw · ker Lp ⊆ ker Lp .
By Lemma 7.8 (ii) and linearity of Lw , it suffices to verify the four identities w · vk ∈ ker Lp
for k = 0, 1, 2, 3, or equivalently that each w · vk is a scalar multiple of one of v0 , v1 , v2 , v3 . We
supply explicit Lw -action identities of this form: w · v0 = +2v2 , w · v1 = −2v3 , w · v2 = −2v0 ,
w · v3 = +2v1 . Together they give Lw as a ±2 skew signed permutation on the recovered basis
with Mw2 = −4I, matching the diagnostic v7/v8 numerical output.
21

## PDF page 22

Proof of Lemma 7.9. We work with p = (s1 , s2 ), w = (s2 , s1 ), s1 = (r, 0), x = (x′ , 0), s2 =
(0, x′ ), and the recovered basis from Lemma 7.8. Computations are organized as four kernel
checks (p · vk = 0) followed by four Lw -action checks (w · vk = ck vπ(k) ); the second pair of each
four follows from the first by anti-commutation with Lℓ16 .
Kernel check k = 0: p · v0 = 0. By (4):
p · v0 = (s1 , s2 )(x, s1 ℓ8 ) = (s1 x − s1 ℓ8 s2 , (s1 ℓ8 )s1 + s2 x̄).
First half: s1 ℓ8 = −(s1 ℓ8 ) (CD-2 + sed-imag of s1 ℓ8 = (0, r), which has zero first component and
imaginary r in the second). So −s1 ℓ8 s2 = (s1 ℓ8 )s2 . By direct sed-CD: (s1 ℓ8 )s2 = (0, r)(0, x′ ) =
(−x̄′ r, 0) = (x′ r, 0) = xs1 (at sed-pair, where xs1 = (x′ , 0)(r, 0) = (x′ r, 0)). Combined with
s1 x = (r, 0)(x′ , 0) = (rx′ , 0):
first half = (rx′ , 0) + (x′ r, 0) = (rx′ + x′ r, 0)

O-AC + Hyp

=

(0, 0) = 0.

Second half: x̄ = −x (sed-imag), so s2 x̄ = −s2 x. By L1, s2 x = ℓ8 . By L4, (s1 ℓ8 )s1 = ℓ8 . So
second half = ℓ8 − ℓ8 = 0. Combining, p · v0 = 0. ✓
Kernel check k = 1: p · v1 = 0. By (4):
p · v1 = (s1 , s2 )(s1 x, ℓ8 ) = (s1 (s1 x) − ℓ¯8 s2 , ℓ8 s1 + s2 s1 x).
First half: ℓ¯8 = −ℓ8 , so −ℓ¯8 s2 = ℓ8 s2 . By direct sed-CD, ℓ8 s2 = (0, 1)(0, x′ ) = (−x̄′ , 0) =
(x′ , 0) = x. For s1 (s1 x): at sed, s1 = (r, 0) and s1 x = (rx′ , 0), both in the first oct half. SedCD gives s1 (s1 x) = (r, 0)(rx′ , 0) = (r(rx′ ), 0). By O-LA on ⟨r⟩ (automatic, single generator):
r(rx′ ) = r2 x′ = −∥r∥2 x′ = −x′ . So s1 (s1 x) = (−x′ , 0) = −x. Hence first half = −x + x = 0.
Second half: s1 x = −(s1 x) (sed-imag), so s2 s1 x = −s2 (s1 x). By L3, ℓ8 s1 = −(s1 ℓ8 ), so the
second-half sum is −(s1 ℓ8 ) − s2 (s1 x). We compute s2 (s1 x) at sed: s2 = (0, x′ ), s1 x = (rx′ , 0),
so
s2 (s1 x) = (0, x′ )(rx′ , 0) = (−0̄ · x′ , 0 · 0 + x′ · rx′ ) = (0, x′ rx′ ).
With rx′ imaginary in O, rx′ = −(rx′ ), so x′ rx′ = −x′ (rx′ ). Apply oct-flex on ⟨r, x′ ⟩: x′ (rx′ ) =
O-AC + Hyp

O-RA

(x′ r)x′
=
(−rx′ )x′ = −r(x′ )2 = r (using ⟨r, x′ ⟩ = 0 ⇒ x′ r = −rx′ , then O-RA on
′
′
2
⟨x , r⟩, then (x ) = −1). Therefore x′ (rx′ ) = r, and x′ rx′ = −r, giving s2 (s1 x) = (0, −r) =
−(s1 ℓ8 ). So second half = −(s1 ℓ8 ) − (−(s1 ℓ8 )) = 0. Combining, p · v1 = 0. ✓
Kernel checks k = 2, 3: p · v2 = p · v3 = 0. By the Pathion Clifford Triad (Theorem 5.1),
{Lp , Lℓ16 } = 0, hence Lp Lℓ16 = −Lℓ16 Lp . Applied to v1 and v0 :
p · v2 = Lp Lℓ16 v1 = −Lℓ16 Lp v1 = −Lℓ16 · 0 = 0,
and similarly p · v3 = −Lℓ16 Lp v0 = 0.

✓

Lw -action k = 0: w · v0 = +2v2 . By (4):
w · v0 = (s2 , s1 )(x, s1 ℓ8 ) = (s2 x − s1 ℓ8 s1 , (s1 ℓ8 )s2 + s1 x̄).
First half: −s1 ℓ8 s1 = (s1 ℓ8 )s1 = ℓ8 by L4. By L1, s2 x = ℓ8 . So first half = ℓ8 +ℓ8 = 2ℓ8 . Second
half: x̄ = −x, so s1 x̄ = −s1 x = −(rx′ , 0). By the sed-CD walk above, (s1 ℓ8 )s2 = (x′ r, 0) = xs1 .
So second half = (x′ r, 0) − (rx′ , 0) = (x′ r − rx′ , 0). By O-AC + Hyp, x′ r + rx′ = 0, hence
x′ r − rx′ = −2(rx′ ). At the sed-pair level: second half = −2(rx′ , 0) = −2(s1 x). Combining,
w · v0 = (2ℓ8 , −2(s1 x)) = 2(ℓ8 , −(s1 x)) = 2v2 (recalling v2 = (ℓ8 , −s1 x) by the unfold above).
✓
Lw -action k = 1: w · v1 = −2v3 . By (4):
w · v1 = (s2 , s1 )(s1 x, ℓ8 ) = (s2 (s1 x) − ℓ¯8 s1 , ℓ8 s2 + s1 s1 x).
22

## PDF page 23

First half: −ℓ¯8 s1 = ℓ8 s1 = −(s1 ℓ8 ) by L3. s2 (s1 x) = −(s1 ℓ8 ) by the sed-CD walk in the
k = 1 kernel check. So first half = −(s1 ℓ8 ) − (s1 ℓ8 ) = −2(s1 ℓ8 ). Second half: s1 x = −(s1 x),
so s1 s1 x = −s1 (s1 x) = −(−x) = x by the same O-LA derivation as in p · v1 . By the ℓ8 s2 = x
identity (sed-CD as in p · v1 ): second half = x + x = 2x. Combining, w · v1 = (−2(s1 ℓ8 ), 2x) =
−2(s1 ℓ8 , −x) = −2v3 (since v3 = (s1 ℓ8 , −x) by the unfold of ℓ16 · v0 above). ✓
Lw -actions k = 2, 3: w · v2 = −2v0 , w · v3 = +2v1 . By Theorem 6.3 (2)’s pair {Lℓ16 , Lw } = 0
(which follows from {Lℓ16 , Lℓ16 ·p } = 0 by σ-transport in §6), Lw Lℓ16 = −Lℓ16 Lw . Applied to v1 :
w · v2 = Lw Lℓ16 v1 = −Lℓ16 Lw v1 = −Lℓ16 (−2v3 ) = 2ℓ16 v3 = 2ℓ16 (ℓ16 v0 ) = −2v0 ,
using ℓ216 = −1 in P (CD-2 norm form: ℓ216 = −∥ℓ16 ∥2 = −1). Similarly, w · v3 = Lw Lℓ16 v0 =
−Lℓ16 Lw v0 = −Lℓ16 (2v2 ) = −2ℓ16 v2 = −2ℓ16 (ℓ16 v1 ) = 2v1 . ✓
In all four cases w · vk is a scalar multiple of an element of {v0 , v1 , v2 , v3 } ⊂ ker Lp , hence
w · vk ∈ ker Lp . By Lemma 7.8 (ii) and linearity, Lw · ker Lp ⊆ ker Lp .
Corollary 7.10 (Kernel associator identity). For v ∈ ker Lp ,
[w, p, v] + [p, w, v] = 0.
Proof. By the canonical Stratum-II orthogonality ⟨p, w⟩P = 0 and the polarization identity
ab + ba = −2⟨a, b⟩ · 1 for a, b ∈ Im(P) (which holds at any CD level), we have pw + wp = 0 in
P. Together with the associator definitions [a, b, v] = (ab)v − a(bv):
(
) (
)
[w, p, v] + [p, w, v] = (wp)v − w(pv) + (pw)v − p(wv)
(
)
= (wp) + (pw) v − w(pv) − p(wv)
= 0 − w · 0 − p · (wv)
= −p · (w · v),
using pw + wp = 0 and pv = 0. By Lemma 7.9, w · v ∈ ker Lp , so p · (w · v) = 0, giving
[w, p, v] + [p, w, v] = 0.
The orthogonality ⟨p, w⟩ = 0 used above is formal at any CD level: p = (s1 , s2 ) and
w = (s2 , s1 ) give ⟨p, w⟩P = ⟨s1 , s2 ⟩S + ⟨s2 , s1 ⟩S = 2⟨s1 , s2 ⟩S = 0 by the Stratum II hypothesis
⟨s1 , s2 ⟩S = 0.

7.6

B2: Top-eigenspace annihilation

Lemma 7.11 (B2 – Top-Eigenspace Annihilation). At every canonical Stratum-II basepoint,
Lw annihilates the top Gp -eigenspace:
Lw · E2∥p∥2 (Gp ) = 0.
The proof has three structural steps. Step 1 identifies the top Gp -eigenspace with the σ-image
of ker Lp : E2∥p∥2 (Gp ) = σ(ker Lp ). Step 2 transports the operator Lw across the σ-conjugation
to obtain Lw ◦ σ = σ ◦ Lℓ16 ·p . Step 3 establishes the q universal annihilation Lℓ16 ·p · ker Lp = 0
on the recovered basis. Combining these gives, for every v ∈ ker Lp ,
(
)
Lw · σ(v) = σ Lℓ16 ·p · v = σ(0) = 0,
which by Step 1 + linearity is exactly the lemma.

23

## PDF page 24

Proof of Lemma 7.11. Step 1: E2∥p∥2 (Gp ) = σ(ker Lp ). The pathion automorphism σ(x, y) =
(x, −y) from Lemma 6.2 satisfies σ 2 = id and is an isometry. Operator transport (3) gives
Lσ(a) = σ ◦ La ◦ σ −1 for every a ∈ P, hence
σ ◦ Lp = Lσ(p) ◦ σ = Lu ◦ σ,
which on kernels gives σ(ker Lp ) = ker Lu (a 4-dimensional subspace of P, since u is also a
pathion-aphanic basepoint inheriting dim ker Lu = 4 via σ-symmetry of the aphanic locus).
We now show ker Lu ⊆ E2∥p∥2 (Gp ). From the half-localization lemma (7) applied to both
ι1 (s1 ) and ι2 (s2 ) at the dyadic basepoint, A21 = −∥s1 ∥2 IP and B22 = −∥s2 ∥2 IP . Using Lp =
A1 + B2 and Lu = A1 − B2 (Definition 7.4):
L2p + L2u = (A1 + B2 )2 + (A1 − B2 )2
= 2A21 + 2B22
= −2∥s1 ∥2 IP − 2∥s2 ∥2 IP
= −2∥p∥2 IP ,
where the last equality uses ∥p∥2 = ∥s1 ∥2 + ∥s2 ∥2 (formal at any CD level by the norm form
on the pair (s1 , s2 )). For any v ∈ ker Lu , L2u v = 0, hence L2p v = −2∥p∥2 v, which by Gp = −L2p
on imaginary p (Lemma 4.2) gives Gp v = 2∥p∥2 v. Therefore v ∈ E2∥p∥2 (Gp ), and ker Lu ⊆
E2∥p∥2 (Gp ).
The opposite inclusion follows by dimension count: at canonical Stratum-II, E2∥p∥2 (Gp ) has
dimension 4 (Definition 7.2), matching dim ker Lu = 4. Hence
σ(ker Lp ) = ker Lu = E2∥p∥2 (Gp ).
Step 2: σ-transport of Lw . By Lemma 6.2 the involution σ is an algebra automorphism,
so operator transport (3) gives
Lw ◦ σ = Lσ(σ(w)) ◦ σ = σ ◦ Lσ(w) .
We compute σ(w) via (4): w = (s2 , s1 ), hence σ(w) = (s2 , −s1 ). By a one-line CD-1 computation, ℓ16 · p = (0, 1)(s1 , s2 ) = (−s¯2 , s¯1 ) = (s2 , −s1 ) (using s¯k = −sk on imaginaries), so
σ(w) = ℓ16 · p. Therefore
Lw ◦ σ = σ ◦ Lℓ16 ·p .
(9)
Step 3: q universal annihilation Lℓ16 ·p · ker Lp = 0. By Lemma 7.8 (ii) and linearity of
Lℓ16 ·p , it suffices to verify Lℓ16 ·p · vk = 0 for k = 0, 1, 2, 3. We work the four cases.
k = 0: Lℓ16 ·p · v0 = 0. By (4):
Lℓ16 ·p · v0 = (s2 , −s1 )(x, s1 ℓ8 ) = (s2 x − s1 ℓ8 (−s1 ), (s1 ℓ8 )s2 + (−s1 )x̄).
First half: −s1 ℓ8 (−s1 ) = s1 ℓ8 s1 = −(s1 ℓ8 )s1 = −ℓ8 by L4. By L1, s2 x = ℓ8 . Hence first half =
ℓ8 − ℓ8 = 0. Second half: x̄ = −x, so (−s1 )x̄ = s1 x = (rx′ , 0). By the sed-CD walk in
p · v0 , (s1 ℓ8 )s2 = (x′ r, 0). Hence second half = (x′ r, 0) + (rx′ , 0) = (x′ r + rx′ , 0)
Combining, Lℓ16 ·p · v0 = 0. ✓
k = 1: Lℓ16 ·p · v1 = 0. By (4):

O-AC + Hyp

=

0.

Lℓ16 ·p · v1 = (s2 , −s1 )(s1 x, ℓ8 ) = (s2 (s1 x) − ℓ¯8 (−s1 ), ℓ8 s2 + (−s1 )s1 x).
First half: −ℓ¯8 (−s1 ) = ℓ¯8 s1 = −ℓ8 s1 = s1 ℓ8 by L3. s2 (s1 x) = −(s1 ℓ8 ) by the sed-CD
walk in p · v1 . Hence first half = −(s1 ℓ8 ) + (s1 ℓ8 ) = 0. Second half: s1 x = −(s1 x), so
(−s1 )s1 x = s1 (s1 x) = −x by O-LA + N-1 (as in p · v1 ). ℓ8 s2 = x by sed-CD (as in p · v1 ). Hence
second half = x − x = 0. Combining, Lℓ16 ·p · v1 = 0. ✓
24

## PDF page 25

k = 2, 3: Lℓ16 ·p · v2 = Lℓ16 ·p · v3 = 0. By the Pathion Clifford Triad (Theorem 5.1),
{Lℓ16 ·p , Lℓ16 } = 0 (the third pair of the universal triad), hence Lℓ16 ·p Lℓ16 = −Lℓ16 Lℓ16 ·p . Applied
to v1 and v0 :
Lℓ16 ·p · v2 = Lℓ16 ·p Lℓ16 v1 = −Lℓ16 Lℓ16 ·p v1 = −Lℓ16 · 0 = 0,
and similarly Lℓ16 ·p · v3 = 0. ✓
In all four cases Lℓ16 ·p · vk = 0, hence by linearity Lℓ16 ·p · ker Lp = 0.
Combining. For v ∈ ker Lp , by Step 1 σ(v) ∈ E2∥p∥2 (Gp ), and by Steps 2 + 3:
(
)
Lw · σ(v) = σ Lℓ16 ·p · v = σ(0) = 0.
Since σ : ker Lp → E2∥p∥2 (Gp ) is a bijection (by Step 1 + σ 2 = id), this gives Lw · E2∥p∥2 (Gp ) =
0.
Remark 7.12 (Range of validity). Step 1 of Lemma 7.11 requires the half-localization (7)
for both ι1 (s1 ) and ι2 (s2 ), hence the dyadic hypothesis. At random aphanic, the identity
L2p + L2u = −2∥p∥2 I fails (as catalogued in Remark 7.7), and ker Lu is no longer contained in
any single Gp -eigenspace. Step 3 in the q universal annihilation Lℓ16 ·p · ker Lp = 0 is itself a
canonical-Stratum-II identity: at CD-aligned, the recovered basis (8) does not span ker Lp (the
kernel is 12-dimensional there), and the Step 3 walks need a different basis.

7.7

Block decomposition theorem at canonical Stratum-II

Theorem 7.13 (Block decomposition of Lw at canonical Stratum-II). At every canonical
Stratum-II basepoint, Lw is block-diagonal in the orthogonal Gp -eigenspace decomposition R32 =
E0 (Gp ) ⊕ E∥p∥2 (Gp ) ⊕ E2∥p∥2 (Gp ):
Lw · E0 (Gp ) ⊆ E0 (Gp ),

Lw · E∥p∥2 (Gp ) ⊆ E∥p∥2 (Gp ),

Lw · E2∥p∥2 (Gp ) = 0.

Consequently [Lw , Pλ ] = 0 for each spectral projector Pλ , and
∑
[Lw , Gp ] =
λ [Lw , Pλ ] = 0.
λ

Proof. The kernel inclusion Lw · E0 (Gp ) ⊆ E0 (Gp ) is Lemma 7.9 (kernel of Lp equals E0 (Gp )
formally: Gp v = 0 ⇐⇒ −L2p v = 0 ⇐⇒ Lp v = 0 for the skew-symmetric Lp , since Lp has the
same kernel as L⊤
p Lp = Gp ). The top-eigenspace annihilation Lw ·E2∥p∥2 (Gp ) = 0 is Lemma 7.11.
The middle eigenspace E∥p∥2 (Gp ) is the orthogonal complement of E0 (Gp ) ⊕ E2∥p∥2 (Gp ) in the
standard inner product on P ∼
= R32 ; since Lw is real and skew-symmetric (as w ∈ Im(P),
⊤
by the formal identity Lw = Lw̄ = −Lw ), Lw preserves orthogonal complements. Therefore
Lw · E∥p∥2 (Gp ) ⊆ E∥p∥2 (Gp ).
Block-diagonality in the orthogonal eigenspace decomposition
∑ is equivalent to commuting
with each spectral projector. The spectral identity [Lw , Gp ] = λ λ [Lw , Pλ ] = 0 is then immediate.

7.8

The CD-Aligned Closure Lemma

Lemma 7.14 (CD-Aligned Closure Lemma). At every dyadic CD-aligned pathion-aphanic basepoint p = ι1 (s1 ) + ι2 (s2 ) with s2 = s1 · ℓ8 and s1 = (r, 0) for some r ∈ Im(O) unit, the operators
Lw and Lp on P satisfy {Lw , Lp } = 0. Consequently, by the centralization chain (Lemma 4.2),
[Lw , Gp ] = 0
at every CD-aligned basepoint.
25

## PDF page 26

The proof has five steps. Step 1 is a half-embedded decomposition that splits {Lw , Lp } into
four pathion-level anti-commutators of the operators Ak , Bk . Step 2 establishes the universal
mixed-pair flex vanishing {Ak , Bk } = 0 for any imaginary s ∈ Im(S), eliminating two of the four
terms via sedenion flexibility. Step 3 reduces the remaining two terms, {A1 , A2 } + {B1 , B2 },
to a pair of sedenion anti-commutators with an L ↔ R swap. Step 4 collapses both sedenion
anti-commutators to zero at CD-aligned via octonion flexibility on two-element subalgebras.
Step 5 combines.
Proof of Lemma 7.14. Step 1: half-embedded decomposition. By Definition 7.4, Lp =
A1 + B2 and Lw = A2 + B1 . Expanding:
{Lw , Lp } = {A2 + B1 , A1 + B2 }
= {A2 , A1 } + {A2 , B2 } + {B1 , A1 } + {B1 , B2 }
= {A1 , A2 } + {A2 , B2 } + {A1 , B1 } + {B1 , B2 },
using the symmetry {X, Y } = {Y, X}. The four terms are {A1 , A2 }, {B1 , B2 } (the ”diagonal”
terms in the (ι1 , ι2 )-grading, where each anti-commutator stays within a single embedding) and
{A1 , B1 }, {A2 , B2 } (the ”mixed” terms, which cross between embeddings of the same sk ).
Step 2: mixed-pair flex vanishing. We claim that for any imaginary s ∈ Im(S),
{Lι1 (s) , Lι2 (s) } = 0

on P.

(10)

This identity holds at every CD level above sedenion and requires no dyadic, aphanic, or CDaligned hypothesis.
Proof of (10). For v = (a, b) ∈ P with a, b ∈ S:
Lι1 (s) v = (sa, bs),

Lι2 (s) v = (−b̄s, sā).

By (4), iterating each composition:
Lι1 (s) Lι2 (s) v = Lι1 (s) (−b̄s, sā) = (s(−b̄s), (sā)s) = (−s(b̄s), (sā)s),
Lι2 (s) Lι1 (s) v = Lι2 (s) (sa, bs) = (−bs s, s sa).
The conjugates simplify via CD-2 + imaginarity of s: bs = s̄ b̄ = −sb̄, so −bs s = (sb̄)s; and
sa = ās̄ = −ās, so ssa = −s(ās). Substituting:
Lι2 (s) Lι1 (s) v = ((sb̄)s, −s(ās)).
Adding:
{Lι1 (s) , Lι2 (s) }v = (−s(b̄s) + (sb̄)s, (sā)s − s(ās)).
Each slot is a sedenion expression of the form (sξ)s − s(ξs) or −s(ξs) + (sξ)s, with ξ = b̄ or
ā. By sed-flex a(ba) = (ab)a on S (taking a = s, b = ξ): s(ξs) = (sξ)s in S. Hence both slots
vanish. {Lι1 (s) , Lι2 (s) }v = 0 for every v ∈ P, which is (10).
Applying (10) with s = s1 gives {A1 , B1 } = 0; with s = s2 gives {A2 , B2 } = 0. Step 1’s
expansion collapses to
{Lw , Lp } = {A1 , A2 } + {B1 , B2 }.
Step 3: pathion-to-sedenion reduction. We compute {A1 , A2 } and {B1 , B2 } explicitly
on v = (a, b) ∈ P. By (4):
A1 A2 v = Lι1 (s1 ) (s2 a, bs2 ) = (s1 (s2 a), (bs2 )s1 ),
A2 A1 v = Lι1 (s2 ) (s1 a, bs1 ) = (s2 (s1 a), (bs1 )s2 ),

26

## PDF page 27

hence
{A1 , A2 }v =

(

)
{Ls1 , Ls2 }S a, {Rs1 , Rs2 }S b ,

(11)

where {Ls1 , Ls2 }S a = s1 (s2 a) + s2 (s1 a) and {Rs1 , Rs2 }S b = (bs2 )s1 + (bs1 )s2 are sedenion
anti-commutators of left-/right-multiplication operators on S. Similarly:
B1 B2 v = Lι2 (s1 ) (−b̄s2 , s2 ā) = (−s2 ā s1 , s1 −b̄s2 )
= ((as2 )s1 , s1 (s2 b)),
using s2 ā = as¯2 = −as2 (so −s2 ā s1 = (as2 )s1 ) and −b̄s2 = −(s¯2 b) = s2 b (so s1 −b̄s2 = s1 (s2 b)).
The same computation with s1 ↔ s2 gives B2 B1 v = ((as1 )s2 , s2 (s1 b)). Therefore
)
(
(12)
{B1 , B2 }v = {Rs1 , Rs2 }S a, {Ls1 , Ls2 }S b .
Note the L ↔ R swap between (11) and (12): in {A1 , A2 } the first slot uses {L}S and the
second uses {R}S , while in {B1 , B2 } the first slot uses {R}S and the second uses {L}S .
Combining (11) and (12):
)
(
(13)
{Lw , Lp } v = ({Ls1 , Ls2 }S + {Rs1 , Rs2 }S ) a, ({Ls1 , Ls2 }S + {Rs1 , Rs2 }S ) b .
Hence
{Lw , Lp } = 0 on P

⇐⇒

{Ls1 , Ls2 }S + {Rs1 , Rs2 }S = 0 on S,

reducing the pathion-level anti-commutation to a single sedenion-level identity in the sum of
left and right anti-commutators of s1 and s2 .
Step 4: CD-aligned sedenion vanishing. We work at CD-aligned with s1 = (r, 0) and
s2 = s1 · ℓ8 = (0, r) (same r ∈ Im(O) unit, by L1 / L2 / L4 of Lemma 7.5 specialized to x′ = r).
For a generic c = (c1 , c2 ) ∈ S with c1 , c2 ∈ O (not necessarily imaginary), we compute the four
sed-CD products via (4):
(
)
s1 (s2 c) = (r, 0)(−c¯2 r, rc¯1 ) = − r(c¯2 r), (rc¯1 )r ,
(
)
s2 (s1 c) = (0, r)(rc1 , c2 r) = (rc¯2 )r, −r(c¯1 r) ,
using sed-CD-1 with the relevant first/second slots and the conjugation identity r̄ = −r. Adding:
(
)
{Ls1 , Ls2 }S c = − r(c¯2 r) + (rc¯2 )r, (rc¯1 )r − r(c¯1 r) .
Each slot is an octonion expression of the form r(ξr)−(rξ)r or its negative, with ξ ∈ {c¯1 , c¯2 } ⊂ O.
By Artin’s theorem on the two-generator subalgebra ⟨r, ξ⟩ ⊂ O (which is associative), oct-flex
r(ξr) = (rξ)r holds. Hence both slots vanish, and {Ls1 , Ls2 }S c = 0 for every c ∈ S, i.e.,
{Ls1 , Ls2 }S = 0

at CD-aligned.

(14)

The symmetric right-multiplication anti-commutator {Rs1 , Rs2 }S c = (cs1 )s2 + (cs2 )s1 admits the parallel computation. By sed-CD-1:
cs1 = (c1 , c2 )(r, 0) = (c1 r, −c2 r),
cs2 = (c1 , c2 )(0, r) = (rc2 , rc1 ),
using 0̄ = 0 on the conjugation factors and −r̄ = r. Iterating:
(
)
(cs1 )s2 = (c1 r, −c2 r)(0, r) = − r(c2 r), r(c1 r) ,
(
)
(cs2 )s1 = (rc2 , rc1 )(r, 0) = (rc2 )r, −(rc1 )r .
Adding:
{Rs1 , Rs2 }S c =

(

)
− r(c2 r) + (rc2 )r, r(c1 r) − (rc1 )r .
27

## PDF page 28

By oct-flex on ⟨r, ck ⟩ ⊂ O, both slots vanish. Hence
{Rs1 , Rs2 }S = 0

at CD-aligned.

(15)

Step 5: combine. Substituting (14) and (15) into (13):
(
)
{Lw , Lp } v = 0 · a, 0 · b = 0 ∈ P,
for every v ∈ P. Hence {Lw , Lp } = 0.
By the centralization chain (Lemma 4.2), {Lw , Lp } = 0 =⇒ [Lw , L2p ] = 0 ⇐⇒ [Lw , Gp ] =
0.
Remark 7.15 (Shortcut via the ∆ identity). The Sedenion ∆ Identity (Theorem 5.4) states
∆(s1 , s2 ) := {Ls1 , Ls2 }S −{Rs1 , Rs2 }S = 0 for all imaginary s1 , s2 ∈ Im(S), with no orthogonality
or CD-alignment hypothesis. Hence {Ls1 , Ls2 }S = {Rs1 , Rs2 }S universally, and either of (14) /
(15) implies the other. The direct sed-CD walks above are self-contained and avoid invoking ∆,
but the shortcut is a cleaner statement when integrating into v2.
Remark 7.16 (Sharpness of CD-aligned). The flex argument of Step 4 fails at canonical
Stratum-II. With s1 = (r, 0) and s2 = (0, x′ ), x′ ̸= r in Im(O) orthogonal, the sed-CD walks of
Step 4 produce cross-products r(c¯k x′ ) and (rc¯k )x′ rather than the symmetric form r(ξr) = (rξ)r
used at CD-aligned. The associator [r, c¯k , x′ ]O is generally nonzero in O — the three-element
subalgebra ⟨r, x′ , c¯k ⟩ is non-associative for generic c¯k — and the flex collapse fails. Diagnostic
v5 records ∥{Lw , Lp }∥F = 16 across the sampled canonical Stratum-II family, consistent with
this sharpness.

7.9

Master theorem and consequences

The three lemmas combine into a single master statement governing the dyadic q antisym
centralization.
Theorem 7.17 (Two-Regime Dyadic Closure). Let p ∈ PPaph be a dyadic basepoint (Definition 7.1) at which Spec(Gp ) is three-valued. Then for every a ∈ qanti
= spanR {u, w},
p
[La , Gp ] = 0.
The closure mechanism splits along the dyadic family:
(1 ) (u-side, all dyadic) For every dyadic basepoint, {Lu , Lp } = 0, hence [Lu , Gp ] = 0 via the
centralization chain (Lemma 4.2). [Lemma 7.6]
(2 ) (w-side, canonical Stratum-II ) At every canonical Stratum-II basepoint, Lw is blockdiagonal in the Gp -eigenspace decomposition E0 ⊕ E∥p∥2 ⊕ E2∥p∥2 (with kernel preservation
and top-eigenspace annihilation), hence [Lw , Gp ] = 0. [Theorem 7.13]
(3 ) (w-side, CD-aligned ) At every CD-aligned basepoint, {Lw , Lp } = 0, hence [Lw , Gp ] = 0
via the centralization chain. [Lemma 7.14]
By linearity of [·, Gp ] in the first argument, every a ∈ qanti
satisfies [La , Gp ] = 0 at every dyadic
p
basepoint (canonical Stratum-II via (1) + (2); CD-aligned via (1) + (3)).
Proof. Direct combination of the three cited lemmas. The dyadic family partitions into the
canonical Stratum-II subfamily and the CD-aligned subfamily (Definition 7.2). At canonical
Stratum-II, items (1) and (2) supply the u- and w-side closures respectively; at CD-aligned,
items (1) and (3) supply them. Linearity in a ∈ qanti
extends the basis closures [Lu , Gp ] =
p
anti
[Lw , Gp ] = 0 to all of qp = spanR {u, w}.
28

## PDF page 29

Corollary 7.18 (Algebraic upgrade of Theorem 4.3 sufficiency). The sufficiency direction
(32)
qp ⊆ K(p) in Theorem 4.3 (Pathion Q-Centralizer Vanishing at Dyadic Basepoint) admits
an algebraic proof at every dyadic basepoint with three-valued Spec(Gp ), via the centralization
chain Lemma 4.2 and:
 [La , Gp ] = 0 for a ∈ quniv
, by the Pathion Clifford Triad Theorem (5.1) and the centralp
ization chain;
 [La , Gp ] = 0 for a ∈ qanti
p , by Theorem 7.17 above.
(32)

Together these give [La , Gp ] = 0 for every a ∈ qp
Ca,b (p) = 0 for all b.

= quniv
⊕ qanti
p
p , hence [La , πp ] = 0 and

Proof. Both bullet points are established algebraically: the first via Theorem 5.1 (proved fully
algebraically in §5 via the chain Lemma A + ∆-reduction + Ω-theorem), the second via Theorem 7.17 above. The centralization chain Lemma 4.2 then propagates [La , Gp ] = 0 to [La , πp ] = 0
to Ca,b (p) = 0 for every b.
Remark 7.19 (Resolution of the Q1 mechanism question). Question (Q1) of §8 notes that
[La , Gp ] = 0 for a ∈ qanti
holds only at three-valued spectrum (not universally), and conjectured
p
7
3
2
that the responsible mechanism is the Lagrange-3 polynomial form G+
p = 4∥p∥4 Gp − 4∥p∥6 Gp ,
valid only at three-valued spectrum.
Theorem 7.17 above shows that the load-bearing algebraic mechanism is not the Lagrange-3
polynomial form, but the half-localization identity (7) (powering the u-side closure across all of
dyadic), together with one of two regime-specific arguments on the w-side: σ-image identification
of E2∥p∥2 (Gp ) with σ(ker Lp ) at canonical Stratum-II (Lemma 7.11), or octonion flexibility on
two-element subalgebras at CD-aligned (Lemma 7.14). The Lagrange-3 identity is consistent
with the closure (the G+
p -form as a polynomial in Gp commutes with anything that commutes
with Gp ), but is not used in any step of the derivation.
The dyadic restriction of the closure is sharp: Remark 7.7 catalogues the u-side failure at
random aphanic via cross-half octonion associators; Remark 7.12 catalogues the w-side failure at
random aphanic via the breakdown of L2p +L2u = −2∥p∥2 I; Remark 7.16 catalogues the canonicalStratum-II failure of the CD-aligned argument via three-element octonion subalgebras. Each of
the three lemmas has its own sharpness witness in the diagnostics.

7.10

Cross-reference to the v45-A proof note

For readers tracking the v45-A diagnostic / proof-note sequence (state/v45a l w spectral closure.md),
the lemma names used in this section map back as follows:
 Lemma 7.6 (”u-Closure Lemma”) ≡ proof-note Lemma A.
 Lemma 7.8 (Recovered Kernel Basis) + Lemma 7.9 (B1 Kernel Preservation) + Lemma 7.11
(B2 Top-Eigenspace Annihilation) + Theorem 7.13 (Block decomposition of Lw ) ≡ proofnote Lemma B (with B1 / B2 broken out as separate sub-lemmas).
 Lemma 7.14 (”CD-Aligned Closure Lemma”) ≡ proof-note Lemma C.

Lemma A (5.2) is the associator-symmetry identity used in the proof of the Pathion Clifford
Triad Theorem; it is unchanged and unrelated to the present Lemma 7.6.

29

## PDF page 30

8

Discussion

8.1

Connection to sedenion U(2) holonomy

At sedenion the holonomy group of the kernel bundle has been shown to be U (2) [2]: as a group,
(U (1) × SU (2))/Z2 , incidentally the gauge group of the electroweak interaction, though neither
cited paper claims a physical identification. The Pathion Clifford Triad Theorem provides a
structural lift of this picture: the three operators Lp , Lℓ16 , Lℓ16 ·p form an anti-commuting triad
whose squares are not scalar but whose anti-commutation pattern mirrors the generators of
an su(2) Lie algebra under the operator commutator. Whether the kernel bundle at pathion
carries an analogous U (n) structure for some n, and whether the antisymmetric Clifford pair
qanti
contributes a second Stiefel–Whitney class, are natural questions pointed at by the present
p
results but not resolved here.

8.2

Why the dimension drops

The most striking phenomenon at pathion is the dimensional drop of the universal kill set
(16)
from 5 at sedenion to 3 at pathion. We can now explain why: the sedenion kill set qp
contains five generators because all of them centralize Gp at sedenion, where the spectrum is
universally {04 , 28 , 44 } and the Lagrange-3 identity holds globally. At pathion the universal
spectrum fails (Proposition 3.1), and only the three universal-Clifford generators retain their
Gp -centralization. The two extra generators revert to dyadic-only behavior, producing the
R136 vs R137 distinction.
In other words, sedenion’s dim-5 kill set is over-determined in two distinct ways: (a) its three
universal-Clifford generators centralize Gp via the Clifford triad mechanism, valid at every CD
level; and (b) its two antisymmetric generators centralize Gp via the Lagrange-3 identity, which
is contingent on three-valued spectrum and fails to lift to pathion. Sedenion happens to satisfy
both conditions simultaneously; pathion does not.

8.3

Closed in this paper

(Q1, closed) Algebraic centralization [La , Gp ] = 0 for a ∈ qanti
at dyadic basepoints.
p
A prior version of this discussion left as an open question whether [La , Gp ] = 0 for a ∈ qanti
at
p
three-valued spectrum admits a purely algebraic derivation (the centralization is not universal,
since {La , Lp } fails for mixed pairs across the σ-grading at random aphanic). The Two-Regime
Dyadic Closure (Theorem 7.17, Section 7) supplies the derivation. The closure mechanism
is two-regime within the dyadic family rather than a single global identity: the u-side closes
universally across the dyadic family by half-localization (Lemma 7.6); the w-side closes by blockdiagonality of Lw in the Gp -eigenspace decomposition at canonical Stratum-II (Theorem 7.13),
or by direct Clifford anti-commutation {Lw , Lp } = 0 at the CD-aligned subfamily (Lemma 7.14).
7
3
2
The Lagrange-3 polynomial form G+
p = 4∥p∥4 Gp − 4∥p∥6 Gp is consistent with the closure but is
not the load-bearing element; see Remark 7.19. The dyadic restriction is sharp at three points
(Remarks 7.7, 7.12, 7.16).

8.4

Open questions

Two concrete questions remain.
(Q2) Spectrum non-invariance and orbits: substantially closed. The non-invariance
of Spec(Gp ) recorded in Proposition 3.1 is now resolved on two of the 3-valued classes:
 Class A, Spec(Gp ) = {012 , 28 , 412 }, is closed by R138 across the six named dyadic subcases
(framework state at v46-C18 close).

30

## PDF page 31

 Class B Stratum II, Spec(Gp ) = {04 , 224 , 44 }, is closed by R140 (framework state at v47A22 close) into the three G2 -orbits described in Section 3. An earlier conjecture that the
orbit classes were parameterized by an integer counting non-trivial cross-half projections
of (s1 , s2 ) is not the correct invariant; the corrected invariant is the pair (component norm
tuple, cb2can ), with three admissible values (1, 0, 0, 1, 0), (0, 1, 1, 0, 0), and ((1/2)4 , 12).

The reduction was not a single argument. R139 (v47-A7) closed the two two-quad layouts
(canonical and mirror) as a sufficient-condition theorem. A subsequent layout-exhaustion
conjecture (“Reading 3”) was refuted by an explicit third G2 -orbit at p3 = √12 (e1 + e25 +
√
e10 + e18 ), characterized by all four pathion-quad slots having equal magnitude 1/ 2 together with the co-alignment relations α1 ∥ β2 and β1 ∥ α2 in Im(O) and the sign-correlation
parity sign(α1 )sign(β2 ) = sign(β1 )sign(α2 ). R140 replaces the refuted two-layout exhaustion with the corrected three-orbit classification and, in particular, formally classifies p3 as
the third orbit. The third-orbit closed-form anatomy on the two-parameter family p(a, b) =
a(e1 + e25 ) + b(e10 + e18 ) (commutator-balance quartics cb2can , cb2mir , cb2sed ; the canonical p3
rank-6 operator skeleton ab · (M ⊕ N ⊤ ); and a rank obstruction to any rank-preserving σbridge between the canonical and mirror partitions) is recorded in Section 3 and was derived
in framework state at v47-A24 through v47-A29. The generic eight-valued class C (ρ = 4,
eight-valued Gram spectrum) remains open as an orbit classification, but its natural 10-tuple
of continuous G2 -invariants is locally/generically non-separating (R142, Section 3): on a regular Class C neighborhood the orbit space has dimension 13 = 27 − 14 while the tuple maps
into R10 , a separation deficiency of exactly 3. The central-inversion collision witness and the
local 13-tuple completion (R143) are recorded in Section 3; what remains open is a continuous, non-inversion finite-distance collision family and a global orbit classification. The ρ = 3
single-component-redundancy classes D, E, F are closed by R141 (Section 3): the cross-quad
trace fingerprint tr(M ) ∈ {6, 0} separates D from E/F, and within Class D the singular-value
tuple ς(M ) further stratifies into Fano-triple (42 members, golden-ratio singular values) and
non-Fano (168 members) G2 -orbits. Neither a continuous ς-classification of the full ρ = 3 locus
nor a representation-theoretic explanation of the Fano-triple golden-ratio phenomenon is yet
available.
(Q3) Higher levels of the tower. The chingon algebra (n = 64) is the next Cayley–
Dickson level. The techniques of this paper extend in principle to chingon, but the spectrum
non-invariance phenomenon may sharpen further. Whether the universal Clifford triad survives,
whether the R140 three-orbit structure persists, whether the R141 cross-quad trace fingerprint
and ς-stratification extend, and whether a new structural break appears at n = 64, are open.

A

Computational certification

All numerical claims in this paper are verified at machine precision (IEEE 754 double, residual
≤ 10−12 unless noted) by self-contained C++ probes. The ΓC nullity certifications cited in
the necessity directions of Theorems 4.1 and 4.3 are reported in those proofs with their sample
descriptions; their run logs are part of the framework record. The probes use a recursive Cayley–
Dickson multiplication engine with no external dependencies; full source code is available from
the author. For each result we report the maximum residual observed across the indicated
sample.

31

## PDF page 32

Identity

Sample

Pathion Clifford Triad: {La , Lb } = 0 for
a, b ∈ quniv
p
Sedenion ∆ identity, orthogonal imaginary
Sedenion ∆ identity, non-orthogonal imaginary
∆((e1 , 0), (0, e2 )) at canonical dyadic case
4-block decomposition cases (i), (ii), (iv)
Ω(A, B; c) = 0, generic A, B, c ∈ O
Ω(A, B; c) = 0, A, B ∈ Im(O)
Ω diagonal: Ā(Ac) − (cĀ)A via Artin
Z2 split: {La , Lb } within quniv
p
Z2 split: {La , Lb } within qanti
p
Z2 split: {La , Lb } mixed (separation)
σ algebra automorphism:
σ(xy) =
σ(x)σ(y)
Operator transport: Lσ(a) − σLa σ −1
Transport
residual:
{Lu , Lw } −
σ{Lp , Lℓ16 ·p }σ −1

N = 4 random aphanic
N = 32 samples
N = 32 samples
exact
N = 32 each
N = 32 samples
N = 32 samples
N = 64 samples
N = 8 random aphanic
N = 8 random aphanic
N = 8 random aphanic
N = 32 random pathions
N = 16 random pathions
N = 8 random aphanic

R141: Class D/E/F cross-quad fingerprint (v47-B7a through B9)
R141 block form [2I8 , M ; M ⊤ , 2I8 ] at
canonical D
R141 tr(M ) = 6 at canonical D
R141 tr(M ) = 0 at canonical E and F
R141 ς(M ) Fano orbit: (0, 1/φ, 15 , φ)
R141
ς(M
non-Fano
orbit:
√ )
(02 , 1/φ, 13 , 2, φ)
R141 G2 -equivariance: tr(M ), ∥M ∥2F ,
ς(M ) preserved
R141 V1 split: dim(V1 ∩ U±can ) = 4

long-double reconstruction
bit-exact
bit-exact
42 D-variants
168 D-variants
18 G2 elements
canonical D

R142: Class C 10-tuple incompleteness, exact single-point witnesses (v47-C7b/C8, exact rational arithmetic
R142 (L1) constraint minor 3 × 3, det =
80 ̸= 0 (dim M = 27)
R142 (L2) orbit minor 14 × 14 ̸= 0 (dO =
14)
R142 (L3) projected-Jacobian minor 10 ×
10 ̸= 0 (rank dF |T M = 10)
R142
(L3)
Jacobian
cross-check
(truncated-poly), 13 × 13 integer minor
R142 (K1) dF · Orb⊤ = 0 (orbit ⊆ ker dF )
R142 (K2) C · Orb⊤ = 0 (orbit tangent to
M)

exact, one witness
exact, one witness
exact, one witness
300/300 entries

exact, one witness
exact, one witness

Build environment. GCC 13.3.0 / Clang 17 / MSVC 2022, all targets C++17 with no
external dependencies. Hardware: AMD Ryzen 9 7950X3D. All probes compile and run in
under one second on a single core; wall-clock times reported in the source-level CI output
bundled with the project repository.
32

## PDF page 33

References
[1] K. Skiouris. Algebraic Hiddenness in the Sedenion Algebra: Characterization, Spectral
Structure, and Bundle Topology. Zenodo, doi:10.5281/zenodo.22016333, 2026.
[2] K. Skiouris. Aphanics and Creative Curvature: A Geometric Theory of Hidden Generation
in Dialectical Cognitive Systems. Zenodo, doi:10.5281/zenodo.22032281, 2026.

33
