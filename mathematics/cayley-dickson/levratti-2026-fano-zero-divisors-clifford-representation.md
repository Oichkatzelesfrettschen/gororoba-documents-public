Source: https://zenodo.org/records/20445208/files/A%20CLIFFORD%20REPRESENTATION%20OF%20THE%20FANO%20ZERO-DIVISORS_v1.pdf
PDF sha256: ad1fcadd82fcd3b3b3924d8f06a440c525e7bd8eed9a4ab4128b748546b368d5
License: https://creativecommons.org/licenses/by/4.0/

# Transcription of levratti-2026-fano-zero-divisors-clifford-representation.pdf

Transcription of `levratti-2026-fano-zero-divisors-clifford-representation.pdf` in this directory, 8 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-8 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

A CLIFFORD REPRESENTATION OF THE FANO ZERO-DIVISORS
GIOVANNI LEVRATTI
Abstract. We construct an explicit map ρ : ZD∗ (4) → Cliff(0, 7) from the 84 active
zero-divisors of the sedenion algebra A4 into the Clifford algebra Cliff(0, 7) ∼
= M8 (R);
see [7] for the general theory of Clifford algebras. The map is defined by ρ(ep +σe8+k ) :=
O
LO
ep , where Lep denotes left-multiplication by ep in the octonions O = A3 . We prove three
exact properties: (i) GL(3, F2 )-equivariance; (ii) anti-commutation {ρ(A), ρ(B)} = 0 for
every ZD pair, via the distinct ε-index theorem (proved algebraically); and (iii) the Fano
reflection identity ρ(ep )ρ(er )ρ(et ) = εp,r,t R{0,p,r,t} for every Fano line {p, r, t}. A remark
records the precise relation between these results and a naı̈ve “Cliff(8), Pauli-weight-4”
formulation originally proposed. All results are verified computationally for n = 4, 5, 6, 7.

Contents
1. Introduction
Notation
2. Structural Preliminaries
2.1. Active zero-divisors
2.2. The distinct ε-index theorem
3. The Clifford Generators
4. The Representation
5. Main Theorems
5.1. Anti-commutation
5.2. GL(3, F2 )-equivariance
5.3. Fano reflection identity
6. Comparison with the Original Desiderata
6.1. Connection to Paper 5 stabilizer codes
7. Discussion
7.1. Geometric meaning of the Fano reflection
7.2. Connection to the sign-parity framework
7.3. Verified extension to n ≤ 7
Appendix A. Numerical Verification
Acknowledgements
References

1
2
2
2
2
3
3
3
3
3
4
5
5
7
7
7
7
7
8
8

1. Introduction
The Sign-Parity Classification [1] established that every ZD pair (A, B) ∈ ZD(4) has
the form A = ep + σe8+k , B = er + τ e8+l with indices satisfying the Fano-plane incidence
structure. The present paper asks whether this combinatorial structure can be encoded
as an algebraic representation in a Clifford algebra.
Date: May 29, 2026.
2020 Mathematics Subject Classification. 17A35, 15A66, 05B25, 81P10.
Key words and phrases. Cayley–Dickson algebras, zero-divisors, octonions, Clifford algebras, Fano
plane, GL(3, F2 ).
1

## PDF page 2

2

GIOVANNI LEVRATTI

The answer is yes, and the construction is unexpectedly clean: it uses nothing beyond the octonion left-multiplication operators LO
ek , which are the standard generators of
Cliff(0, 7).
Notation. We write An for the Cayley–Dickson algebra of dimension 2n over R, with
A3 = O (octonions) and A4 = S (sedenions). Basis elements are e0 = 1, e1 , . . . , e2n −1 ,
with
ei · ej = εij ei⊕j , εij ∈ {+1, −1},
where ⊕ denotes bitwise XOR; see [6] for the general theory of non-associative algebras.
The Fano plane PG(2, F2 ) is identified with F32 \ {0} = {1, . . . , 7}; its seven lines are
{p, r, t} with p ⊕ r ⊕ t = 0.
The ε-index of an active element A = ep + σe8+k is p ∈ {1, . . . , 7}, i.e. the index of its
octonion component.
2. Structural Preliminaries
2.1. Active zero-divisors.
Definition 2.1. An element A ∈ A4 is active if A = ep + σe8+k for some p ∈ {1, . . . , 7},
k ∈ {1, . . . , 7}, σ ∈ {+1, −1}, and there exists B ̸= 0 with AB = 0. Write ZD∗ (4) for the
set of active elements.
From [1]: |ZD∗ (4)| = 84 and |ZD(4)| = 336 ordered ZD pairs.
2.2. The distinct ε-index theorem. The following theorem is the structural core of
the construction.
Theorem 2.2 (Distinct ε-indices). Let (A, B) ∈ ZD(n) with A = ep + σA eN +k and
B = er + σB eN +l , where N = 2n−1 . Then p ̸= r. Moreover, every ordered pair (p, r) with
p ̸= r and p, r ∈ {1, . . . , N − 1} arises as the ε-indices of some ZD pair.
Proof. We prove both assertions algebraically.
Distinct ε-indices. Suppose for contradiction that p = r.
Step 1 (XOR forces k = l). By the {0, 4, 8} Trichotomy ([1], Theorem 3.6, Case B),
A · B = 0 requires
p ⊕ (N + k) ⊕ r ⊕ (N + l) = 0.
Since (N + k) ⊕ (N + l) = k ⊕ l (the leading bits 2n−1 cancel), this gives p ⊕ r = k ⊕ l.
With p = r: k ⊕ l = 0, hence k = l.
Step 2 (Direct product). With p = r and k = l, using e2p = e2N +k = −e0 and anticommutativity εN +k, p = −εp, N +k :
A · B = e2p + σB εp,N +k ep⊕(N +k) + σA εN +k,p ep⊕(N +k) + σA σB e2N +k
= −(1 + σA σB ) e0 + (σB − σA ) εp,N +k ep⊕(N +k) .
Step 3 (Contradiction). For A · B = 0 both coefficients must vanish:
• e0 coefficient: 1 + σA σB = 0 ⇒ σA σB = −1 ⇒ σA ̸= σB .
• ep⊕(N +k) coefficient: (σB − σA ) εp,N +k = 0. Since εp,N +k ̸= 0: σB = σA .
These two conditions contradict each other, so A · B ̸= 0 whenever p = r.
All 42 pairs appear. Given any ordered pair (p, r) with p ̸= r and p, r ∈ {1, . . . , 7},
set t := p ⊕ r ∈ {1, . . . , 7} (nonzero since p ̸= r). By the {0, 4, 8} Trichotomy, any ZD
pair with ε-indices (p, r) satisfies k ⊕ l = t; pick any k ∈ {1, . . . , 7} with k ̸= t and
set l := k ⊕ t ∈ {1, . . . , 7}. By the Sign-Parity Criterion ([1], Theorem 7.16), among
the four (σA , σB ) ∈ {+1, −1}2 choices for the flat {p, N + k, r, N + l}, at least one

## PDF page 3

A CLIFFORD REPRESENTATION OF THE FANO ZERO-DIVISORS

3

has sign-parity +1, yielding a ZD pair (ep + σA eN +k , er + σB eN +l ) with ε-indices exactly
(p, r).
□
Remark 2.3. The map A ↦→ ε(A) = p separates every ZD pair: ZD adjacency implies
ε(A) ̸= ε(B).
3. The Clifford Generators
The octonion left-multiplication operators are defined by
LO
ek : O → O,

x ↦→ ek · x.

O
As 8 × 8 real matrices they satisfy {LO
ei , Lej } = −2δij I8 for all i, j ∈ {1, . . . , 7}, making
them the seven generators of Cliff(0, 7) ∼
= M8 (R); see [7] for the general theory of Clifford
algebras.
O
O O
Lemma 3.1. For every i, j ∈ {1, . . . , 7} with i ̸= j: LO
ei Lej + Lej Lei = 0.

Proof. Immediate from {Lei , Lej } = −2δij I8 .

□

Remark 3.2 (Non-associativity warning). Because the octonions are not associative, LO
ei ◦
O
O
Lej ̸= Lei ·ej in general as matrix composition. The product Li Lj is a Clifford bivector of
grade 2, not a grade-1 generator.
4. The Representation
Definition 4.1. Define ρ : ZD∗ (4) → Cliff(0, 7) = M8 (R) by
(
)
ρ ep + σe8+k := LO
ep .
Remark 4.2. The map depends only on the ε-index p: it is constant on each of the 7 fibers
{A ∈ ZD∗ (4) : ε(A) = p}.
5. Main Theorems
5.1. Anti-commutation.
Theorem 5.1 (Anti-commutation). For every ZD pair (A, B) ∈ ZD(4):
{ρ(A), ρ(B)} = 0.
Proof. Let A = ep + σe8+k and B = er + τ e8+l . By Theorem 2.2, p ̸= r. Therefore
O
{ρ(A), ρ(B)} = {LO
ep , Ler } = −2δpr I8 = 0.

□
5.2. GL(3, F2 )-equivariance.
Theorem 5.2 (GL(3, F2 )-equivariance). For every g ∈ GL(3, F2 ) acting on {1, . . . , 7} =
F32 \ {0}:
ρ(g · A) = g · ρ(A),
where the right-hand action permutes the generators {Le1 , . . . , Le7 } by index.
Proof. The ε-index satisfies ε(g · A) = g(ε(A)) since g acts on the octonion component. Since GL(3, F2 ) ∼
= PSL(2, 7) is a subgroup of G2 = Aut(O) (see [5], §4.1), every g ∈ GL(3, F2 ) acts on {e1 , . . . , e7 } as an octonion automorphism. The induced map
φ(g) : Lei ↦→ Leg(i) satisfies {Leg(i) , Leg(j) } = −2δg(i),g(j) I8 = −2δij I8 , hence is an automorphism of Cliff(0, 7). The automorphism group GL(3, F2 ) ∼
= PSL(2, 7) and its action on
the Fano geometry are studied in detail in [2].
□

## PDF page 4

4

GIOVANNI LEVRATTI

5.3. Fano reflection identity.
Definition 5.3. For a Fano line {p, r, t} (with p ⊕ r ⊕ t = 0), the Fano 4-flat is F =
{0, p, r, t} ⊂ {0, . . . , 7}. The Fano reflection is
{
(
)7
+1 j ∈ F,
RF := 2PF − I8 = diag χF (j) j=0 , χF (j) =
−1 j ∈
/ F.
Note RF2 = I8 (involution).
We need two preparatory lemmas.
Lemma 5.4 (ε-identity). For every Fano line {p, r, t}: εp,r,t := sign(ep · (er · et )) = −εrt .
Proof. Since r⊕t = p: er ·et = εrt ep . Hence ep ·(er ·et ) = εrt (ep ·ep ) = εrt ·(−1) = −εrt . □
Lemma 5.5 (Line sign consistency). For every Fano line {p, r, t}, let α := εrt . Then
εpr = εtp = α.
Proof. Wrap(p, r) with p ⊕ r = t: εpr · εt,r = −1. Since εt,r = −εrt = −α: εpr (−α) = −1,
so εpr = α. Wrap(r, p) with r ⊕ p = t: εrp · εt,p = −1. Since εrp = −εpr = −α:
(−α)εtp = −1, so εtp = α.
□
Theorem 5.6 (Fano Reflection Identity). For every Fano line {p, r, t}:
O O
LO
ep Ler Let = εp,r,t RF = −εrt RF ,

where F = {0, p, r, t}.
Proof. Set α := εrt , so εp,r,t = −α (Lemma 5.4).
Step 1 (Diagonal form). Since p ⊕ r ⊕ t = 0, the operator G := Lep Ler Let acts on each
basis vector ej as ep · (er · (et · ej )) = λj ej , where
λj = εtj εr, t⊕j εp, r⊕t⊕j .
Hence G is diagonal.
Step 2 (j ∈ F , four sub-cases). Write α = εpr = εtp = εrt (Lemma 5.5). We show
λj = −α for each j ∈ {0, p, r, t}.
• j = 0: λ0 = εt,0 · εr,t · εp,p = 1 · α · (−1) = −α.✓
• j = p: t ⊕ p = r and r ⊕ t ⊕ p = 0 (Fano), so λp = εtp · εr,r · εp,0 = α · (−1) · 1 = −α.✓
• j = r: t ⊕ r = p and r ⊕ t ⊕ r = t (Fano), so λr = εtr · εr,p · εp,t . Now εtr = −α,
εrp = −α (anti-commutativity), and Wrap(p, t) with p ⊕ t = r gives εpt · εrt = −1,
so εpt = −α. Hence λr = (−α)(−α)(−α) = −α3 = −α.✓
• j = t: t ⊕ t = 0 and r ⊕ t ⊕ t = r, so λt = εtt · εr,0 · εp,r = (−1) · 1 · α = −α.✓
Thus λj = −α = εp,r,t for all j ∈ F .
Step 3 (Lo-flat: j ∈
/ F ). For j ∈ {1, . . . , 7} \ {p, r, t}, the indices j, p, r, t are all distinct
and all lie in {1, . . . , 7}, so Lj anti-commutes with each of Lp , Lr , Lt :
Lj G = Lj Lp Lr Lt = (−Lp Lj )Lr Lt = Lp Lr Lj Lt = −Lp Lr Lt Lj = −G Lj .
Hence {Lj , G} = 0. Since G = diag(λ0 , . . . , λ7 ), this gives λj⊕l = −λl for every l. Setting
l = 0: λj = −λ0 = −(−α) = α = −εp,r,t .✓
Conclusion. G has eigenvalue −α = εp,r,t on span(F ) and eigenvalue +α = −εp,r,t on
the lo-flat, so G = εp,r,t RF .
□
Corollary 5.7. Γprt := Lep Ler Let is an involution: Γ2prt = I8 .
Proof. Γ2prt = ε2p,r,t RF2 = I8 .

□

## PDF page 5

A CLIFFORD REPRESENTATION OF THE FANO ZERO-DIVISORS

5

6. Comparison with the Original Desiderata
Remark 6.1 (Comparison with the Cliff(8) formulation). The construction was
originally framed as a map ρ : ZD∗ (4) → Cliff(8) = M16 (R) satisfying four properties:
(a) GL(3, F2 )-equivariance, (b) “Pauli weight = 4”, (c) {ρ(A), ρ(B)} = 0 for ZD pairs,
and (d) ρ(eA )ρ(eB )ρ(eC ) = −I16 for covering triples. The construction above differs in
the following exact ways.
Target algebra. Our ρ maps into Cliff(0, 7) = M8 (R) (7 generators). The proposed
Cliff(8) = M16 (R) (8 generators) admits a natural embedding M8 ,→ M16 via M ↦→ M ⊗I2 ,
but this adds no structure relevant to the zero-divisor problem. Cliff(0, 7) is the correct
and minimal target.
Pauli weight. In Cliff(0, 7) acting on (R2 )⊗3 (3 qubits), the generators Lek have Paulidecomposition weight at most 3. The condition “weight = 4” was predicated on a 4-qubit
target and is not a natural invariant of the zero-divisor structure.
Triple product identity. The property ρ(eA )ρ(eB )ρ(eC ) = −I16 was overly strong. The
correct identity (Theorem 5.6) gives Γprt = εp,r,t RF , a Fano reflection, not a scalar multiple of the identity. Since πA πB πC = −1 for every 2-flat ([1], Theorem 7.18), this encodes
exactly the sign constraint of the Sign-Parity framework.
The exact properties of ρ are summarised in Table 1.

Property

Original formulation

Exact result

(1) Equivariance

GL(3, F2 )-equivariant

proved (same)

(2) Triple product

= −I16

= εprt RF (Fano reflection)

(3) Anti-commutation {ρ(A), ρ(B)} = 0 for ZD pairs proved (same)
(4) Pauli weight

= 4 in Cliff(8)
dropped (wrong target)
Table 1. Original desiderata vs. exact results.

6.1. Connection to Paper 5 stabilizer codes.
Remark 6.2 (Pauli decomposition and Fano duality). Pauli decomposition. Each LO
ek ∈
3
M8 (R), viewed as an operator on 3 qubits (dim = 2 = 8), decomposes as
4
∑
(k) (k)
s j Pj ,

−i
LO
ek = 2

(k)

sj ∈ {+1, −1},

j=1

with all four coefficients of equal magnitude 12 . This is forced by the Frobenius identity
2
O
⊤ O
∥LO
isometry of R8 , hence orthogonal: (LO
ek ∥F = 8 (since Lek is an
ek ) Lek = I8 , giving
∑
Tr(I8 ) = 8), which requires P |ck,P |2 = 1 = 4 · 14 .

## PDF page 6

6

GIOVANNI LEVRATTI

The explicit decompositions are
−i
LO
e1 = 2 (IIY + IZY + ZIY − ZZY),
−i
LO
e2 = 2 (IYI + IYZ − ZYI + ZYZ),
−i
LO
e3 = 2 (IXY + IYX − ZXY + ZYX),
−i
LO
e4 = 2 (−YII + YIZ + YZI + YZZ),
−i
LO
e5 = 2 (−XIY + XZY + YIX + YZX),
−i
LO
e6 = 2 (XYI − XYZ + YXI + YXZ),
−i
LO
e7 = 2 (XXY − XYX + YXX − YYY).

The X-part encodes the Fano points. For every k ∈ {1, . . . , 7}, all four Pauli strings
in the decomposition of LO
ek share the same X-part (positions where X or Y appears), and
this X-part equals the binary representation of k in F32 :
( )
= bin(k) ∈ F32 \ {0}.
x-part LO
ek
This gives a canonical bijection ek ↔ bin(k) between the 7 octonion generators and the
7 points of PG(2, F2 ).
The 8 anti-commuting single-Pauli selections. An exhaustive search over all 47 =
16 384 ways of selecting one Pauli string per generator from its four components shows
that exactly 8 selections satisfy {ρ̃(ei ), ρ̃(ej )} = 0 for all 21 pairs i ̸= j. These 8 selections
share the same fixed X-parts and differ only in which Z-correction is chosen from the
4-element coset {I, Z}⊗3 .
Triple products and Fano duality. For every one of the 8 valid selections, and for
every Fano line {p, r, t}, the triple product equals
ρ̃(ep ) ρ̃(er ) ρ̃(et ) = ϕp,r,t · Q{p,r,t} ,

ϕp,r,t ∈ {+i, −i},

where Q{p,r,t} ∈ {I, Z}⊗3 is a specific non-identity Z-type Pauli string, the same for all
8 selections. The assignment {p, r, t} ↦→ Q{p,r,t} is a bijection from the 7 Fano lines to the
7 nonzero elements of {I, Z}⊗3 ∼
= F32 \ {0}, and coincides with the projective duality of
PG(2, F2 ): the dual (in the combinatorial sense) of each Fano line.
The twisted group algebra is the octonions. Define the cocycle coct (bin(i), bin(j)) :=
εij (the octonion sign table of [1]). The twisted group algebra C[(Z/2)3 ]coct with multiplication uα · uβ = coct (α, β) uα⊕β is non-associative and its left-regular representation sends
ubin(k) ↦→ LO
ek . This algebra is therefore isomorphic to the octonions O themselves: the
twisted group algebra construction recovers the original representation, not a new one.
The cocycle condition fails on non-Fano triples. The map coct is not a group 2cocycle: the cocycle identity c(α, β) c(α ⊕ β, γ) = c(α, β ⊕ γ) c(β, γ) fails for exactly the
28 non-collinear triples in PG(2, F2 ). The 7 Fano lines satisfy it — these are precisely
the triples for which both parenthesisations of the triple product agree: (up · ur ) · ut =
up · (ur · ut ) = εp,r,t · u0 . The failure on non-Fano triples is the octonion associator.
The fundamental obstruction. Every Pauli string squares to +I, while L2ek = −I
in Cliff(0, 7). This group-theoretic mismatch is the precise obstruction: no assignment
of single Pauli strings to the generators of O can reproduce the octonion multiplication,
even projectively.
Open problem (Paper 8). The Fano duality {p, r, t} ↦→ Q{p,r,t} identified above is
the duality between X-type and Z-type stabilizers in the CSS codes of [4]. Establishing
this correspondence as a theorem — and determining whether the non-Fano failure of

## PDF page 7

A CLIFFORD REPRESENTATION OF THE FANO ZERO-DIVISORS

7

the cocycle condition has a code-theoretic interpretation — is the natural problem for a
subsequent paper.
7. Discussion
7.1. Geometric meaning of the Fano reflection. The operator RF = 2PF − I8 acting on O = R8 is the reflection fixing the Fano 4-flat F = {0, p, r, t} and negating its
orthogonal complement (the lo-flat). The sub-algebra Hprt := span{e0 , ep , er , et } ∼
= H
(quaternions) is a Cayley–Dickson subalgebra of O, and RF is its grading involution:
the Z/2Z-grading of O with even part Hprt and odd part its orthocomplement. Thus
Γprt = Lep Ler Let is the chirality element of the quaternionic subalgebra associated to the
Fano line {p, r, t}.
7.2. Connection to the sign-parity framework. The Fano reflection identity provides
a Clifford-algebraic realisation of the sign-parity discriminant. The octonion triple sign
εp,r,t coincides with π(F, split) for the corresponding 2-flat in A4 ([1], Definition 7.2),
bridging the sign-parity classification of Paper 1 with the present Clifford representation.
The ZD zeta function of [3], whose poles encode the four division-algebra thresholds,
acquires a Clifford-algebraic interpretation through this bridge: the residue at each pole
corresponds to the count of Fano triples acting via Γprt .
7.3. Verified extension to n ≤ 7. The construction ρ(A) = LO
ε(A) and all three main
theorems extend to all n ≥ 4, with ρ defined on the EF-type active elements of ZD∗ (n).
Theorem 7.1 (Extension to n ≤ 7). For every n ∈ {4, 5, 6, 7}:
(1) All EF-type ZD pairs of An have distinct ε-indices (Theorem 2.2).
(2) {ρ(A), ρ(B)} = 0 for all EF-type ZD pairs (Theorem 5.1).
(3) Lep Ler Let = εp,r,t RF for all 7 Fano lines (Theorem 5.6).
Proof. Items (2) and (3) concern only the A3 structure and are independent of n. Item (1)
is verified computationally for n ≤ 7 (Appendix A). The algebraic proof for all n follows
by induction on the hereditary decomposition ([1], Theorem 8.1): every EF-type ZD pair
in An+1 arises from an EF-type ZD pair in An under the Cayley–Dickson embedding,
which preserves the ε-index structure.
□
Appendix A. Numerical Verification
All theorems were verified computationally for n = 4, 5, 6, 7 using Python/NumPy on
an AMD Ryzen Threadripper 2950X (16 physical cores). gl(3,F2 )-equivariance (Theorem 5.2) was additionally verified in GAP 4.15.
ZD counts by block type. Active elements of An are classified as EF (one component
in the E-block {1, . . . , 2n−1 − 1}, one in the F-block {2n−1 , . . . , 2n − 1}), EE (both in E),
or FF (both in F). EE and FF pairs are zero-divisors inherited from the embedded copy
of An−1 ([1], Theorem 8.1); the map ρ is defined on EF-type elements.
Theorem 2.2 (distinct ε-indices): 0 failures among EF-type ZD pairs at every n.
Theorem 5.6 (Fano Reflection Identity): ∥Lep Ler Let − εp,r,t RF ∥max = 0 for all 7 Fano
lines, verified independently of n.
Theorem 5.2 (GL(3, F2 )-equivariance): verified in GAP 4.15 by constructing the permutation group
G = ⟨ σ1 , σ2 ⟩ ⊂ Sym({1, . . . , 7})
with σ1 = (2 6)(3 7) and σ2 = (1 4 2)(3 5 6). GAP confirms |G| = 168, G ∼
= PSL(2, 7), G
is 2-transitive on {1, . . . , 7}, and all 7 Fano lines are preserved by all 168 elements of G.

## PDF page 8

8

GIOVANNI LEVRATTI

n dim

EF

EE

FF

Cross

Total Expected

Time

4 16
336
—
—
—
336
336 <0.1 s
5 32
3,696
336
336
672
5,040
5,040
<1 s
6 64 31,920 5,040 5,040 10,080 52,080
52,080
1s
7 128 260,400 52,080 52,080 104,160 468,720
468,720
58 s
Table 2. ZD pair counts by block type for An , n = 4, . . . , 7. EF: one index
in each block (new pairs); EE/FF: both indices in the same block (inherited
from An−1 ); Cross: pairs involving one inherited
( ) and one new EF element
(= EE+FF). Expected total: |ZD(n)| = 336 n−1
.
3 2
Acknowledgements
The author thanks Claude (Anthropic) for extensive assistance with algebraic verification, proof development, and LATEX editing throughout this work and the companion
papers.
References
[1] G. Levratti, Sign-Parity Classification of Zero Divisors in Cayley–Dickson Algebras, Zenodo preprint
(2026), doi:10.5281/zenodo.20315751.
[2] G. Levratti, Zero-Divisors in Cayley–Dickson Algebras: Fano Geometry, Automorphisms, and the
Weil Zeta Function, Zenodo preprint (2026), doi:10.5281/zenodo.20417859.
[3] G. Levratti, Sign Structure, Automorphism Groups, and the ZD Zeta Function of Cayley–Dickson
Algebras, Zenodo preprint (2026), doi:10.5281/zenodo.20397587.
[4] G. Levratti, Active Stabilizers in Reed–Muller CSS Codes from Cayley–Dickson Zero-Divisors, Zenodo preprint (2026), doi:10.5281/zenodo.20431754.
[5] J. C. Baez, The octonions, Bull. Amer. Math. Soc. 39 (2002), 145–205.
[6] R. D. Schafer, An Introduction to Nonassociative Algebras, Academic Press, New York, 1966.
[7] I. R. Porteous, Clifford Algebras and the Classical Groups, Cambridge University Press, 1995.
Independent Researcher, Modena, Italy
Email address: giovanni.levratti.research@gmail.com
