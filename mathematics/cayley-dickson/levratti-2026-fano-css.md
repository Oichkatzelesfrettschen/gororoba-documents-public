Source: https://zenodo.org/api/records/20445734
PDF sha256: 05295802b74533ec8598c215a4b1898907f3c20ab21ffebc907e2388ce84ee9c
License: CC-BY-4.0
Language: eng
Fidelity: machine-gated

# Transcription of levratti-2026-fano-css.pdf

Transcription of `levratti-2026-fano-css.pdf` in this directory, 8 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-8 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

FANO DUALITY, PROJECTIVE ORTHOGONALITY,
AND THE CSS BRIDGE
GIOVANNI LEVRATTI
Abstract. The companion paper [5] constructed an explicit map ρ : ZD∗ (4) →
Cliff(0, 7) and observed, via exhaustive computation, that the triple-product identity
ρ̃(ep )ρ̃(er )ρ̃(et ) = φp,r,t · Q{p,r,t} defines a bijection from the 7 Fano lines to the 7
non-zero elements of {I, Z}⊗3 , which coincides with the projective duality of PG(2, F2 ).
The paper left open whether this duality is the X/Z duality of the Steane [[7, 1, 3]] code
studied in [4].
We close this gap, prove the analogous result for n = 5 (Theorem 5.1), and establish
that M = In−1 for all n ≥ 2 under the MSB-first generator convention (Proposition 5.2).
The main theorem (Theorem 3.1) states that the map {p, r, t} ↦→ Q{p,r,t} equals the
projective orthogonal complement in F32 , and that Q{p,r,t} is exactly the Z-stabilizer
of the Steane code associated to the dual point. The proof proceeds in three steps:
−1
⊥
(1) an explicit verification that Q{p,r,t} = Z ⊗bin ({p,r,t} ) for all seven Fano lines; (2)
identification of the dual point with the unique Z-stabilizer support in the Steane code;
(3) a GL(3, F2 )-equivariance argument showing the correspondence is canonical.
As a corollary, the sign-parity constraint πA πB πC = −1 (Theorem 7.18 of [1]) acquires
a unified interpretation: it is simultaneously the Clifford phase of a balanced ZD triple
([4], Theorem 4.2) and the projective orthogonality relation between Fano lines and their
dual points in PG(2, F2 ).

1. Introduction
The Cayley–Dickson tower A0 = R ⊂ A1 = C ⊂ A2 = H ⊂ A3 = O ⊂ A4 = S ⊂ · · · has
been the subject of a series of papers establishing a complete classification of zero-divisors.
The counting formula
(
)
n−1
(1)
|ZD(n)| = 336 ·
,
n ≥ 4,
3
2
was proved in [1], and its generating function was identified as a Weil zeta function
in [3]. The active stabiliser construction of [4] established bijections between zero-divisor
structure and stabiliser codes. The Clifford representation of [5] constructed an explicit
map ρ : ZD∗ (4) → Cliff(0, 7) and computed, for every Fano line {p, r, t}, the triple product
(2)

ρ̃(ep )ρ̃(er )ρ̃(et ) = φp,r,t · Q{p,r,t} ,

φp,r,t ∈ {+i, −i},

where Q{p,r,t} ∈ {I, Z}⊗3 is a non-identity Z-type Pauli string, the same for all eight valid
single-Pauli selections. [5] observed that {p, r, t} ↦→ Q{p,r,t} is a bijection from Fano lines
to {I, Z}⊗3 \ {I ⊗3 }, consistent with projective duality, and stated:
“The Fano duality {p, r, t} ↦→ Q{p,r,t} identified above is the duality between
X-type and Z-type stabilizers in the CSS codes of [4]. Establishing this
correspondence as a theorem . . . is the natural problem for a subsequent
paper.”
Date: May 29, 2026.
2020 Mathematics Subject Classification. 81P70, 94B05, 17A35, 51E20.
1

## PDF page 2

2

GIOVANNI LEVRATTI

The present paper establishes this as Theorem 3.1 (n = 4) and proves the analogue for
n = 5 (Theorem 5.1), along with a general result that M = In−1 for all n ≥ 2 under the
MSB-first generator convention (Proposition 5.2).
∼

Overview of the argument. Let bin : {1, . . . , 7} −→ F32 \ {0} be the standard bijection k ↦→ binary representation of k. For a set S ⊂ F32 we write S ⊥ for its orthogonal
complement under the standard inner product on F32 .
Definition 1.1 (Dual Pauli string). For a Fano line L = {p, r, t} ⊂ {1, . . . , 7} (i.e. bin(p)⊕
bin(r) ⊕ bin(t) = 0), the dual Z-string is
−1

ZL := Z ⊗bin

(v)

,

v := spanF2 {bin(p), bin(r), bin(t)}⊥ ∩ (F32 \ {0}),

representations.
i.e. v ∈ F32 \{0} is the unique non-zero vector orthogonal to all three
⨂3 binary
wj
⊗w
3
Here Z
for w = (w1 , w2 , w3 ) ∈ F2 denotes the Pauli string j=1 Z .
Remark 1.2. Since bin(p), bin(r), bin(t) ∈ F32 are the three non-zero vertices of a Fano
line, they span a 2-dimensional subspace W ⊂ F32 , and W ⊥ is 1-dimensional (as dim F32 =
3), so v is uniquely determined. There are exactly seven Fano lines and seven non-zero
vectors, so L ↦→ v is a bijection.
The main theorem asserts two things: that Q{p,r,t} = ZL (the computational duality
of [5] equals projective orthogonality), and that ZL is the Z-stabiliser of the Steane code
associated to the dual point.
2. Background
We recall the notation used throughout.
2.1. Fano plane and lo-flats. The Fano plane PG(2, F2 ) has seven points {1, . . . , 7} =
F32 \ {0} and seven lines. Under the bijection bin, a Fano line is a set {p, r, t} with
bin(p) + bin(r) + bin(t) = 0 ∈ F32 .
A lo-flat of ZD(4) is a weight-4 subset F = {a, b, c, d} ⊂ {1, . . . , 7} with a⊕b⊕c⊕d = 0.
There are exactly seven lo-flats; they are the complements of the seven Fano lines [3,
Theorem 3.2].
2.2. Steane code and stabilisers. The Steane [[7, 1, 3]] code is CSS(C, C) [7] with
C = [7, 4, 3] the binary Hamming code. Its X-stabiliser group SX ∼
= (Z/2Z)3 is generated
by g1X , g2X , g3X with supports equal to the rows of the parity-check matrix H7,4,3 :
g1X = X1 X3 X5 X7 ,
g2X = X2 X3 X6 X7 ,
g3X = X4 X5 X6 X7 .
The Z-stabilisers g1Z , g2Z , g3Z have the same supports. The seven non-identity elements of
SX (resp. SZ ) have supports exactly equal to the seven lo-flats [4, Theorem 3.1].
2.3. The map ρ̃ and Pauli decompositions. The map ρ of [5] is defined by
ρ : ZD∗ (4) → Cliff(0, 7) by ρ(ep + σe8+k ) := LO
ep , the left-multiplication operator of ep in
O
the octonions. The Clifford generators Lek decompose as
−i
LO
ek =

4
∑
(k) (k)
s j Pj ,

2 j=1

## PDF page 3

FANO DUALITY, PROJECTIVE ORTHOGONALITY,

AND THE CSS BRIDGE

3

with all four coefficients of equal magnitude 12 . The map ρ̃ selects one Pauli string per generator from its four-element Pauli coset; there are exactly eight valid selections satisfying
{ρ̃(ei ), ρ̃(ej )} = 0 for all i ̸= j.
For every valid selection and every Fano line {p, r, t}:
ρ̃(ep )ρ̃(er )ρ̃(et ) = φp,r,t · Q{p,r,t} ,

(3)

where Q{p,r,t} ∈ {I, Z}⊗3 is independent of the selection [5, Remark 6.2].
3. Main Theorem
Theorem 3.1 (CSS Bridge). Let {p, r, t} ⊂ {1, . . . , 7} be any Fano line and let Q{p,r,t} ∈
{I, Z}⊗3 be as in (3). Then:
(i) (Projective orthogonality) Q{p,r,t} = Z ⊗v , where v ∈ F32 \ {0} is the unique vector
orthogonal to bin(p), bin(r), bin(t), i.e. Q{p,r,t} = ZL in the notation of Definition 1.1.
(0 0 1)
(ii) (CSS identification) Let M ∈ GL(3, F2 ) be the bit-reversal matrix M = 0 1 0 .
1 0 0
The non-identity Z-stabiliser of the Steane [[7, 1, 3]] code [6] whose support equals
the lo-flat {1, . . . , 7} \ {p, r, t} corresponds, under the generator-combination labelling of SZ ∼
= (Z/2Z)3 , to the vector M vL ∈ F32 \ {0}. Equivalently, SZ (M vL ) =
{1, . . . , 7} \ {p, r, t}, where SZ (w) denotes the support of the Z-stabiliser labelled
w.
(iii) (Contragredient equivariance) For every g ∈ GL(3, F2 ) and every Fano line L =
{p, r, t}:
Qg(L) = Z ⊗g

−T v
L

,

where g(L) = {g(p), g(r), g(t)} and g −T = (g −1 )T . In other words, L ↦→ QL is
equivariant for the contragredient (dual) action of GL(3, F2 ) on F32 .
Proof. We prove parts (i)–(iii) in order.
Part (i): Projective orthogonality.
The seven Fano lines and the explicit Q-values from [5, Remark 6.2] are given in Table 1.
For each line L = {p, r, t}, we compute WL := spanF2 {bin(p), bin(r), bin(t)} and its
orthogonal complement WL⊥ ⊂ F32 . Since bin(p) + bin(r) + bin(t) = 0, the three vectors
span a 2-dimensional subspace, so WL⊥ is 1-dimensional. Let vL be its unique non-zero
element.
Table 1. Fano duality: explicit verification for all seven Fano lines.
Columns: Fano line; projective orthogonal vL ; dual index q = bin−1 (vL );
Z-string ZL = Q{p,r,t} (Part i); stabiliser label M vL (Part ii); lo-flat =
SZ (M vL ).
Line {p, r, t}
{1, 2, 3}
{1, 4, 5}
{1, 6, 7}
{2, 4, 6}
{2, 5, 7}
{3, 4, 7}
{3, 5, 6}

vL

q Q{p,r,t}
T

(1, 0, 0)
(0, 1, 0)T
(1, 1, 0)T
(0, 0, 1)T
(1, 0, 1)T
(0, 1, 1)T
(1, 1, 1)T

4
2
6
1
5
3
7

ZII
IZI
ZZI
IIZ
ZIZ
IZZ
ZZZ

M vL

SZ (M vL )
T

(0, 0, 1)
(0, 1, 0)T
(0, 1, 1)T
(1, 0, 0)T
(1, 0, 1)T
(1, 1, 0)T
(1, 1, 1)T

{4, 5, 6, 7}
{2, 3, 6, 7}
{2, 3, 4, 5}
{1, 3, 5, 7}
{1, 3, 4, 6}
{1, 2, 5, 6}
{1, 2, 4, 7}

## PDF page 4

4

GIOVANNI LEVRATTI

Inspection of Table 1 shows that in every row, Q{p,r,t} = Z ⊗vL : the Z-factors appear in
exactly the bit-positions where vL is 1. This is an explicit verification for all seven Fano
lines; the bijectivity of L ↦→ vL (projective duality of PG(2, F2 )) is a standard fact.
Part (ii): CSS identification.
(0 0 1)
Let M = 0 1 0 ∈ GL(3, F2 ) be the bit-reversal matrix (M 2 = I, det M = 1).
1 0 0
The Steane Z-generators have supports supp(g1Z ) = {1, 3, 5, 7}, supp(g2Z ) = {2, 3, 6, 7},
supp(g3Z ) = {4, 5, 6, 7}. For w = (w1 , w2 , w3 ) ∈ F32 \ {0}, write SZ (w) for the support of
the corresponding non-identity element of SZ ∼
= (Z/2Z)3 :
⨁
SZ (w) :=
supp(gjZ ) (symmetric difference).
j: wj =1

By [4, Theorem 3.1], {SZ (w) : w ̸= 0} is exactly the set of seven lo-flats.
Claim: SZ (M vL ) = {1, . . . , 7} \ {p, r, t} for every Fano line {p, r, t}.
Proof of claim: exhaustive verification over all seven Fano lines, recorded in Table 1.
SZ
⊥
M
Abstractly, this is a finite check that the composition L ↦−
→ vL ↦−→ M vL ↦−→
SZ (M vL )
equals {1, . . . , 7} \ L for all seven lines L.
The matrix M is the unique element of GL(3, F2 ) that reconciles the bit-ordering convention of bin (MSB first) with the generator-index ordering of the parity-check matrix
H7,4,3 .
Part (iii): Contragredient equivariance.
The orthogonal complement map W ↦→ W ⊥ in F32 satisfies (gW )⊥ = g −T (W ⊥ ) for
all g ∈ GL(3, F2 ) and all subspaces W . Indeed: v ∈ (gW )⊥ ⇔ ⟨v, gw⟩ = 0 for all
w ∈ W ⇔ ⟨g T v, w⟩ = 0 for all w ∈ W ⇔ g T v ∈ W ⊥ ⇔ v ∈ g −T (W ⊥ ).
For a Fano line L = {p, r, t}, this gives vg(L) = g −T vL and hence Qg(L) = Z ⊗vg(L) =
−T
Z ⊗g vL .
Verified exhaustively for the three generators {swap(0, 1), swap(1, 2), add(0 ← 1)} of
GL(3, F2 ), over all seven Fano lines by direct computation.
Remark 3.2 (Contragredient vs. covariant action). The contragredient action is intrinsic
to projective duality: under GL(3, F2 ), points transform covariantly and hyperplanes (lines
in PG(2, F2 )) transform contravariantly. That QL transforms via g −T confirms it encodes
the Z-type (dual) information to the X-type line L.
□
4. Corollaries
Corollary 4.1 (Unified interpretation of πA πB πC = −1). For every 2-flat of A4 , the
sign-parity constraint πA πB πC = −1 (Theorem 7.18 of [1]) admits three equivalent interpretations:
(a) (Sign-parity, algebraic): Exactly one of the three splits of every 2-flat is inactive
(π = −1) and two are active (π = +1).
(b) (Clifford, [4]): The product of three balanced half-operators from the three splits
carries global phase −1 and produces −Yα Yβ .
(c) (Projective, Theorem 3.1): The product ρ̃(ep )ρ̃(er )ρ̃(et ) equals φ · ZL , where ZL is
the projective dual of the Fano line {p, r, t}; the phase φ ∈ {+i, −i} records the
residual sign, and ZL records the geometric obstruction to associativity.
Proof. Part (a) is [1, Theorem 7.3 and 7.18]. Part (b) is [4, Theorem 4.2]. Part (c)
follows from Theorem 3.1(i) and (3): the triple product ρ̃(ep )ρ̃(er )ρ̃(et ) is φ · Q{p,r,t} with
Q{p,r,t} = ZL by part (i).
□

## PDF page 5

FANO DUALITY, PROJECTIVE ORTHOGONALITY,

AND THE CSS BRIDGE

5

Corollary 4.2 (Non-Fano obstruction). The fundamental obstruction identified in [5]
(that no single Pauli selection can satisfy the octonion algebra relations) has a codetheoretic interpretation: the 28 non-collinear triples of PG(2, F2 ) are exactly the triples
{p, r, t} for which bin(p) + bin(r) + bin(t) ̸= 0 in F32 , i.e. the triples that do not define a
Z-type stabiliser dual. The cocycle condition for coct fails on precisely these triples.
Proof.
(7) A triple {p, r, t} is collinear in PG(2, F2 ) iff bin(p) + bin(r) + bin(t) = 0. There
are 3 = 35 unordered triples total, 7 collinear (Fano lines) and 28 non-collinear. By [5,
Remark 6.2], the cocycle identity for coct holds iff the triple is collinear. For non-collinear
triples, no Z-type dual exists, so Q{p,r,t} is not a pure Z-string; the cocycle failure is the
algebraic shadow of the absence of a projective dual.
□
Remark 4.3 (Dependence of M on the generator basis). The bit-reversal matrix M
is not an intrinsic feature of the projective duality; it is an artefact of two independent conventions. The map bin encodes k ∈ {1, . . . , 7} with the most significant bit
first, while the standard parity-check matrix H7,4,3 orders the generators so that gjZ detects the j-th bit least-significant-first. If one instead labels the Z-generators so that
supp(gjZ ) = {k : bitj−1 (k) = 1} with bit-positions indexed MSB-first (i.e., matching the
bin convention), then SZ (vL ) = {1, . . . , 7} \ {p, r, t} directly and Part (ii) holds with
M = I3 . The appearance of M in the theorem is a convention artefact, not a geometric
obstruction.
5. Extension to n = 5: the [[15, 7, 3]] CSS Bridge
We establish the analogue of Theorem 3.1 for n = 5. The ambient geometry is now
PG(3, F2 ) (with 15 points), the role of Fano lines is played by Fano planes (2-dimensional
projective subspaces, 7-element sets), and the code is [[15, 7, 3]].
Theorem 5.1 (n = 5 CSS Bridge). Let W ⊂ {1, . . . , 15} be a Fano plane in PG(3, F2 ),
i.e. a 7-element set closed under bitwise XOR. Let vW ∈ F42 \ {0} be the unique nonzero
vector orthogonal to every element of W :
W = {k ∈ {1, . . . , 15} : bin4 (k) · vW = 0}.
Let the Z-generators of the [[15, 7, 3]] code have supports supp(gjZ ) = {k : bin4 (k)j−1 = 1}
for j = 1, 2, 3, 4 (MSB-first convention), and write SZ (w) for the support of the Z-stabiliser
labelled w ∈ F42 \ {0}. Then:
(i) (Projective duality) The assignment W ↦→ vW is the projective duality of PG(3, F2 ):
it is a bijection from the 15 Fano planes to F42 \ {0}, sending each hyperplane to
its unique orthogonal point.
(ii) (CSS identification, M = I4 ) SZ (vW ) = {1, . . . , 15} \ W for every Fano plane W .
Equivalently, the Z-stabiliser labelled vW has support equal to the complement of
W , which by [4, Theorem 5.1] is also the support of the X-stabiliser corresponding
to W .
(iii) (Contragredient equivariance) For every g ∈ GL(4, F2 ): vg(W ) = g −T vW .
Proof. Parts (i) and (iii) are standard facts of projective geometry over F2 ; part (i) is the
definition of projective duality and (iii) follows from the contravariance of the orthogonal
complement map (gW )⊥ = g −T (W ⊥ ) (same argument as in the proof of Theorem 3.1(iii)).
Part (ii) is verified exhaustively for all 15 Fano planes by direct computation (the sign
table of A4 , which determines the lo-flat structure of ZD(5) via [1]). The explicit data are
in Table 2.
□

## PDF page 6

6

GIOVANNI LEVRATTI

Proposition 5.2 (M = In−1 for the MSB-first PCM convention). For all n ≥ 2, let the
[[2n−1 − 1, 2n−1 − n, 3]] Hamming CSS code have Z-generators giZ with support
supp(giZ ) = {k ∈ {1, . . . , 2n−1 − 1} : biti−1 (k) = 1},

i = 1, . . . , n − 1,

where biti−1 (k) is the (i − 1)-th bit of binn−1 (k) counted MSB-first. Then for every hyperplane W of PG(n − 2, F2 ) with normal vW ,
SZ (vW ) = {1, . . . , 2n−1 − 1} \ W.
Equivalently, M = In−1 for all n ≥ 2 with the MSB-first PCM convention.
Proof. By the structure of the Hamming parity-check matrix:
SZ (w) = {k : ⟨binn−1 (k), w⟩ = 1

(mod 2)}.

By the definition of the hyperplane WvW :
{1, . . . , 2n−1 − 1} \ WvW = {k : ⟨binn−1 (k), binn−1 (vW )⟩ = 1
n−1

Setting w = binn−1 (vW ) gives SZ (vW ) = {1, . . . , 2

(mod 2)}.

− 1} \ WvW .

□

Remark 5.3 (M = I4 vs M ̸= I3 at n = 4). In contrast to n = 4 (where the bit-reversal
M ̸= I3 was needed), Theorem 5.1(ii) holds with M = I4 . This confirms the prediction
of Remark 4.3: the bit-reversal at n = 4 is a convention artefact that vanishes when
the stabiliser-generator ordering matches the MSB-first convention of bin. For n = 5, the
standard parity-check matrix H15,11,3 already uses MSB-first bit-ordering, so no correction
is needed.
Remark 5.4 (Computational diagnosis of the Clifford obstruction at n = 5). The precise
reason why the Clifford triple-product formula of Theorem 3.1(i) does not extend to n ≥ 5
O
O
is the loss of alternativity. For n = 4, A3 = O is alternative, giving LO
p Lq = ε(p, q) Lp⊕q ;
O
antisymmetry of ε then forces {LO
p , Lq } = 0 for p ̸= q, making the seven operators Clifford
generators.
( )
For n = 5, A4 = S is not alternative. Exhaustive computation over all 15
= 105 pairs
2
(p, q) with 1 ≤ p < q ≤ 15 gives:
A4
4
• 63 pairs (ZD-index pairs): {LA
p , Lq } = 0, consistent with πA πB πC = −1.
A4
4
• 42 pairs (non-ZD, alternativity-breaking pairs): {LA
p , Lq } ̸= 0 and ̸= −2I.
A4
4 A4
For the 42 non-ZD pairs, LA
p Lq is a linear combination of multiple operators Lr , because
the associator [ep , eq , ej ] ̸= 0 for some j. This is intrinsic to A4 : no change of basis removes
it.
6. Discussion
6.1. Summary of the bridge. The following table summarises the chain of equivalences
established across [1, 4, 5] and the present paper.
ZD algebra

←→ Projective geometry ←→

Stabiliser codes

πA πB πC = −1
([1, Thm. 7.18])

Fano line ↔ dual point
(Thm. 3.1(i))

X-stab ↔ Z-stab
([4, Thm. 3.1])

−Yα Yβ phase
([4, Thm. 4.2])

Q{p,r,t} = ZL
(Table 1)

Z-stabiliser support
= lo-flat complement

6.2. Relation to the Weil zeta function. The residue at the pole x = 21 of the ZD
zeta function [2] equals −7 = −|PG(2, F2 )| [3, Theorem 8.2] and now acquires a structural
interpretation: 7 counts the Fano lines, each of which corresponds (via Theorem 3.1) to
a Z-stabiliser of the Steane code. The sign −1 reflects the residue of Z(x) at the pole
x = 1/2, which equals −|PG(2, F2 )| = −7 by the Weil identity ([3, Theorem 8.2]).

## PDF page 7

FANO DUALITY, PROJECTIVE ORTHOGONALITY,

AND THE CSS BRIDGE

7

Table 2. n = 5 CSS bridge: all 15 Fano planes W with M = I4 . Columns:
normal vW ; first four elements of W (full W has 7 elements); SZ (vW ) =
{1, . . . , 15} \ W (8-element complement). All 15 verified by direct computation.
vW
(0, 0, 0, 1)T
(0, 0, 1, 0)T
(0, 0, 1, 1)T
(0, 1, 0, 0)T
(0, 1, 0, 1)T
(0, 1, 1, 0)T
(0, 1, 1, 1)T
(1, 0, 0, 0)T
(1, 0, 0, 1)T
(1, 0, 1, 0)T
(1, 0, 1, 1)T
(1, 1, 0, 0)T
(1, 1, 0, 1)T
(1, 1, 1, 0)T
(1, 1, 1, 1)T

W (Fano plane, 7 elements) SZ (vW ) = {1, . . . , 15} \ W
{2, 4, 6, 8, 10, 12, 14}
{1, 4, 5, 8, 9, 12, 13}
{3, 4, 7, 8, 11, 12, 15}
{1, 2, 3, 8, 9, 10, 11}
{2, 5, 7, 8, 10, 13, 15}
{1, 6, 7, 8, 9, 14, 15}
{3, 5, 6, 8, 11, 13, 14}
{1, 2, 3, 4, 5, 6, 7}
{2, 4, 6, 9, 11, 13, 15}
{1, 4, 5, 10, 11, 14, 15}
{3, 4, 7, 9, 10, 13, 14}
{1, 2, 3, 12, 13, 14, 15}
{2, 5, 7, 9, 11, 12, 14}
{1, 6, 7, 10, 11, 12, 13}
{3, 5, 6, 9, 10, 12, 15}

{1, 3, 5, 7, 9, 11, 13, 15}
{2, 3, 6, 7, 10, 11, 14, 15}
{1, 2, 5, 6, 9, 10, 13, 14}
{4, 5, 6, 7, 12, 13, 14, 15}
{1, 3, 4, 6, 9, 11, 12, 14}
{2, 3, 4, 5, 10, 11, 12, 13}
{1, 2, 4, 7, 9, 10, 12, 15}
{8, 9, 10, 11, 12, 13, 14, 15}
{1, 3, 5, 7, 8, 10, 12, 14}
{2, 3, 6, 7, 8, 9, 12, 13}
{1, 2, 5, 6, 8, 11, 12, 15}
{4, 5, 6, 7, 8, 9, 10, 11}
{1, 3, 4, 6, 8, 10, 13, 15}
{2, 3, 4, 5, 8, 9, 14, 15}
{1, 2, 4, 7, 8, 11, 13, 14}

6.3. Obstruction to a full group-algebra lifting. Corollary 4.2 makes precise why no
Clifford algebra representation can lift the full octonion multiplication table to a group
algebra: the 28 non-Fano triples do not satisfy the cocycle condition, and there is no Ztype dual to assign to them. The projective geometry of PG(2, F2 ) thus encodes exactly
the boundary of what the CSS framework can see.
7. Open Problems
(1) Extension to n ≥ 6: Clifford structure. The CSS identification (Parts (i)–(ii)
of Theorems 3.1 and 5.1) now extends to all n ≥ 2 by Proposition 5.2: the bridge
SZ (vW ) = {1, . . . , 2n−1 − 1} \ W is proved analytically, with M = In−1 for n ≥ 5
and M = bit-reversal for n = 4. The remaining open problem is the Clifford part:
for n ≥ 5, there is no ρ̃-triple-product formula for QW (Remark 5.4). The open
question is whether there exists a natural map σ : ZD∗ (n) → Cliff(0, 2n−1 − 1)
extending ρ from n = 4 to all n, and whether triple products under σ recover
Z ⊗vW for the appropriate geometric objects.
(2) Twisted cocycle interpretation. The map coct is not a 2-cocycle, but it satisfies
the cocycle condition on Fano triples. Does it define a twisted 2-cocycle in the
sense of group cohomology of (Z/2Z)3 , with twisting data determined by the
projective duality of PG(2, F2 )? Relate this to the semidirect product structure
Aut(A4 ) ∼
= (Z/2Z)4 ⋊ GL(3, F2 ) of [3, §7].
(3) Physical interpretation. The map {p, r, t} ↦→ Q{p,r,t} sends each Fano line to a
Z-type logical operator in the Steane code. Does the CSS bridge of Theorem 3.1
have a physical interpretation in terms of fault-tolerant gates or transversal operations on the Steane code?
Acknowledgements
The author thanks the mathematical physics community, and in particular the body
of work on octonions and Cayley–Dickson algebras by C. Furey, G. M. Dixon, and

## PDF page 8

8

GIOVANNI LEVRATTI

J. C. Baez [8]. Computational assistance was provided by Claude (Anthropic) for algebraic verification, structural analysis, and proof scaffolding. All mathematical results
have been independently verified numerically; the author takes full responsibility for any
errors.
References
[1] G. Levratti, Sign-Parity Classification of Zero Divisors in Cayley–Dickson Algebras, Zenodo preprint
(2026), doi:10.5281/zenodo.20315751. Under review at Communications in Algebra.
[2] G. Levratti, Sign Structure, Automorphism Groups, and the ZD Zeta Function of Cayley–Dickson
Algebras, Zenodo preprint (2026), doi:10.5281/zenodo.20397587.
[3] G. Levratti, Zero-Divisors in Cayley–Dickson Algebras: Fano Geometry, Automorphisms, and the
Weil Zeta Function, Zenodo preprint (2026), doi:10.5281/zenodo.20417859.
[4] G. Levratti, Active Stabilizers in Reed–Muller CSS Codes from Cayley–Dickson Zero-Divisors, Zenodo preprint (2026), doi:10.5281/zenodo.20431754.
[5] G. Levratti, A Clifford Representation of the Fano Zero-Divisors, Zenodo preprint (2026),
doi:10.5281/zenodo.20445208.
[6] A. M. Steane, Multiple-particle interference and quantum error correction, Proc. R. Soc. Lond. A
452 (1996), 2551–2577.
[7] D. Gottesman, Stabilizer Codes and Quantum Error Correction, Ph.D. thesis, California Institute of
Technology, 1997.
[8] J. C. Baez, The octonions, Bull. Amer. Math. Soc. 39 (2002), no. 2, 145–205.
Independent Researcher, Modena, Italy
Email address: giovanni.levratti.research@gmail.com
