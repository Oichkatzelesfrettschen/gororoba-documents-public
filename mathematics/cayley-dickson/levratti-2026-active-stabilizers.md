Source: https://zenodo.org/api/records/20431754
PDF sha256: 7bd01b5fda24b2de56b10bf9404efaa968e48d467350f1b8f361ef9ed36c3a9b
License: CC-BY-4.0
Language: eng
Fidelity: machine-gated

# Transcription of levratti-2026-active-stabilizers.pdf

Transcription of `levratti-2026-active-stabilizers.pdf` in this directory, 9 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-9 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

ACTIVE STABILIZERS IN REED–MULLER
CSS CODES FROM CAYLEY–DICKSON ZERO-DIVISORS
GIOVANNI LEVRATTI
Abstract. We establish three results connecting the zero-divisor structure of the Cayley–
Dickson algebras An to the stabilizer formalism of quantum error-correcting codes.
Step 1 (Bijection, n = 4). The 7 lo-flats of ZD(4)—the weight-4 subsets F ⊂ {1, . . . , 7}
with a ⊕ b ⊕ c ⊕ d = 0—are in explicit bijection with the 7 non-identity elements of the
X-stabilizer group SX of the Steane [[7, 1, 3]] code. All 7 lo-flats carry identical sign-parity
pattern: πEE|FF = −1 (inactive), πEF1 = πEF2 = +1 (active).
Step 2 (Operator translation). For every mixed flat F = {i, j, 8+k, 8+l} in A4 , the
algebraic identity πA · πB · πC = −1 (Theorem 7.18 of [1]) translates into the Clifford-group
identity
(
)(
)(
)
Zα Zβ Xα Xγ Xβ Xγ = − Yα Yβ ,
where the global phase −1 is the precise Clifford avatar of πA πB πC = −1, partially resolving
the open question of [4] on whether the sign-parity invariant π has a stabilizer-group interpretation. The operator −Yα Yβ is a detectable error with weight-2n−2 syndrome, confirmed
for n = 4, 5.
Step 3 (Extension to n = 5, verified on QPU). The 15 Fano planes of PG(3, F2 )
are in explicit bijection with the 15 non-identity elements of the X-stabilizer group SX ∼
=
(Z/2Z)4 of the [[15, 7, 3]] code (4 generators, 24 − 1 = 15 non-identity elements). The phase
identity and syndrome formula extend to all n ≥ 4 (Universal Phase Lemma, Theorem 5.4).
Syndrome structure verified on ibm kingston (156-qubit QPU, job d8bm67ijki0s73aq6idg,
27 May 2026).

1. Introduction
The Cayley–Dickson algebra A4 (sedenions, dimension 16) is the first in the infinite tower
An to admit zero-divisors. Levratti [1] establishes a complete sign-parity classification of
zero-divisor pairs in An (n ≥ 4) and proves
(
)
n−1
(1)
|ZD(n)| = 336 ·
,
3
2
( )
where 3· 2 is the Gaussian binomial counting 3-dimensional F2 -subspaces. The main combinatorial engine is the Reed–Muller connection (Theorem 3.9 of [1]): zero-divisor pairs in An
correspond exactly to weight-4 codewords of RM(1, n)⊥ = RM(n−2, n).
Paper 2 [4] (the Informational Identity Boundary); see also [3] for the Fano bijection and
Grassmannian structure identifies an open problem:
Determine whether the sign-parity invariant π translates into a property of
the stabilizer group of the CSS code built from RM(1, n): specifically, whether
πA πB πC = −1 corresponds to a constraint on the stabilizer generators, and
Date: May 28, 2026.
2020 Mathematics Subject Classification. 81P70, 94B05, 17A35, 05E99.
1

## PDF page 2

2

GIOVANNI LEVRATTI

whether “active” stabilizers play a distinguished role in the error-correction
properties.
The present paper answers this question for n = 4, establishing the bijection (Step 1) and the
phase identity (Step 2), and extends both results to n = 5 (Step 3), verified computationally
and on IBM Quantum hardware.
Notation. Qubits are labeled by elements of {0, . . . , 15} (the canonical basis indices of A4 ).
(n)
(n)
We write εi,j ∈ {+1, −1} for the Cayley–Dickson sign: ei · ej = εi,j ei⊕j . The sign table is
constructed recursively by the four doubling rules of Lemma 2.1 of [2] (Paper 3).
2. Background
2.1. Sign-parity framework. A 2-flat in An is a set F = {i, j, k, l} ⊂ {1, . . . , 2n − 1} with
i ⊕ j ⊕ k ⊕ l = 0. It has three splits: A = (i, j)|(k, l), B = (i, k)|(j, l), C = (i, l)|(j, k). The
sign-parity of split (p, q)|(r, s) is
π(F, split) = εp,r εq,r εp,s εq,s ∈ {+1, −1}.
A split is active if π = +1 and inactive if π = −1. The Sign Parity Criterion (Theorem 7.3 of
[1]) asserts: a split produces a zero-divisor pair if and only if it is active. By Theorem 7.18 of
[1]:
(2)

πA · πB · πC = −1 for every 2-flat in every An (n ≥ 4).

2.2. Fano plane and lo-flats. In A4 (dimension 16, imaginary basis indices {1, . . . , 15}),
the mixed zero-divisor pairs have one ε-type index (≤ 7) and one f -type index (≥ 8) in each
component (Theorem 7.7 of [1]). The lo-flat of a mixed flat {i, j, 8+k, 8+l} is its projection
{i, j, k, l} ⊂ {1, . . . , 7}.
Definition 2.1. A lo-flat is a weight-4 subset F = {a, b, c, d} ⊂ {1, . . . , 7} with a⊕b⊕c⊕d = 0.
There are exactly 7 lo-flats; they are the weight-4 codewords of the Hamming code [7, 4, 3],
equivalently the complements of the 7 lines of the Fano plane PG(2, F2 ).
2.3. Steane code. The Steane [[7, 1, 3]] code [5] is the CSS code CSS(C, C) with C = [7, 4, 3]
(the Hamming code); see also [6] for the stabilizer formalism. Its X-stabilizer group SX ∼
= (F2 )3
is generated by gX1 , gX2 , gX3 with supports equal to the rows of the parity check matrix H7,4,3 :
gX1 = X1 X3 X5 X7 ,

gX2 = X2 X3 X6 X7 ,

gX3 = X4 X5 X6 X7 .

The Z-stabilizer group has the same three supports. Both groups have 7 non-identity elements,
each of weight-4 support.
3. Step 1: Bijection Lo-Flat – Steane Stabilizer
Theorem 3.1 (Explicit bijection). The 7 lo-flats of ZD(4) are in explicit bijection with the 7
non-identity elements of SX (and identically of SZ ). Under the natural labeling by supports:

## PDF page 3

ACTIVE STABILIZERS IN RM-CSS CODES FROM CD ZERO-DIVISORS

Fk

Support

Fano complement Steane element

F1
F2
F3
F4
F5
F6
F7

{1, 2, 4, 7}
{1, 2, 5, 6}
{1, 3, 4, 6}
{1, 3, 5, 7}
{2, 3, 4, 5}
{2, 3, 6, 7}
{4, 5, 6, 7}

{3, 5, 6}
{3, 4, 7}
{2, 5, 7}
{2, 4, 6}
{1, 6, 7}
{1, 4, 5}
{1, 2, 3}

gX1 · gX2 · gX3
gX1 · gX2
gX1 · gX3
gX1
gX2 · gX3
gX2
gX3

3

Type
product
product
product
generator
product
generator
generator

Proof. The 7 lo-flats are exactly the 7 weight-4 codewords of the Hamming code [7, 4, 3], whose
parity check matrix H7,4,3 has rows generating SX . The 7 non-identity elements of SX ∼
= (F2 )3
have supports equal to the symmetric differences of non-empty subsets of {gX1 , gX2 , gX3 }.
Direct verification confirms that these 7 supports are precisely the 7 lo-flats (Table above). □
Theorem 3.2 (Uniform sign-parity). Every lo-flat Fk has the same sign-parity pattern under
the mixed-flat embedding in A4 : for any actual mixed flat {i, j, 8+k, 8+l} projecting to F ,
πEE|FF = −1

(inactive),

πEF1 = πEF2 = +1

(active).

In particular, the sign-parity invariant π does not distinguish Steane generators (F4 , F6 , F7 )
from product stabilizers (F1 , F2 , F3 , F5 ).
Proof. By Lemma 7.8 of [1]: for a mixed flat F = {i, j, 2n−1 +k, 2n−1 +l} in An ,
(
)
πAn (F, EF|EF) = − πAn−1 {i, j, k, l}, (i, k)|(j, l) .
For n = 4, the projected flat {i, j, k, l} ⊂ {1, . . . , 7} is a flat in A3 = O of type εε|εε (all indices
are ε-type in A3 ; mixed EF|EF flats do not exist in A3 ). By Lemma 7.24 of [1] (Quadrilateral
parity in O): for any i, j, k, l ∈ {1, . . . , 7} with i ⊕ j = k ⊕ l and {i, j} ∩ {k, l} = ∅,
(
)
O O O
πA3 {i, j, k, l}, (i, k)|(j, l) = εO
ik εjk εil εjl = −1.
Hence πA4 (EF|EF) = −(−1) = +1 for every mixed flat. The EE|FF sign follows from the
product identity (2): πEE · (+1) · (+1) = −1, giving πEE|FF = −1. The computation depends
only on the sign table of A3 via Lemma 7.24, and is independent of the specific lo-flat. □
Remark 3.3. The three Steane generators correspond to the three rows of H7,4,3 ; the four
product stabilizers are F2 -combinations of two or three generators. This is a property of the
Hamming code, not of the sign-parity invariant.
4. Step 2: Operator Translation of πA πB πC = −1
4.1. Balanced triples of split half-operators.
Definition 4.1 (Half-operators). Let F = {i, j, 8+k, 8+l} be a mixed flat in A4 . For each
split, the two halves are the two size-2 subsets on each side. Assign operator types by π:
inactive split (EE|FF, π = −1) −→ Z-type,

active split (EFm , π = +1) −→ X-type.

A balanced triple selects one half from each split such that each qubit index appears exactly 0
or 2 times among the three halves.
For the flat F = {i, j, 8+k, 8+l} there are exactly four balanced triples:

## PDF page 4

4

GIOVANNI LEVRATTI

Selection From EE (Z) From EF1 (X) From EF2 (X) Missing index
1
2
3
4

{i, j}
{i, j}
{8+k, 8+l}
{8+k, 8+l}

{i, 8+k}
{j, 8+l}
{i, 8+k}
{j, 8+l}

{j, 8+k}
{i, 8+l}
{i, 8+l}
{j, 8+k}

8+l
8+k
j
i

4.2. The phase identity.
Theorem 4.2 (Step 2 — Clifford avatar of πA πB πC = −1). For every mixed flat F =
{i, j, 8+k, 8+l} in A4 , and for every balanced triple of half-operators with the π-type assignment,
the product of the three half-operators in the Pauli group satisfies
(
)(
)(
)
Zα Zβ Xα Xγ Xβ Xγ = − Yα Yβ ,
where α, β are the two indices that each appear once in the Z-half and once in a distinct X-half
(the repeated pair), and γ is the index shared by both X-halves (absent from the Z-half ). The
fourth index of F is the missing index: it appears in none of the three half-operators. The
global phase is −1 = πEE · πEF1 · πEF2 .
Proof. Collect the product by qubit:
• Qubit α: contributes Zα (from Z-half) and Xα (from first X-half). Product: Zα Xα = iYα
(phase i).
• Qubit β: contributes Zβ and Xβ . Product: Zβ Xβ = iYβ (phase i).
• Qubit γ: contributes Xγ · Xγ = I (phase 1).
Total phase: i · i = i2 = −1. Operator: Yα Yβ ⊗ Iγ .
The four balanced selections differ only in the labeling of (α, β, γ); in each case the two
qubits appearing in both a Z-half and an X-half contribute phase i each, giving −1 overall. □
Remark 4.3 (Why exactly −1). The phase −1 arises from exactly two ZX anticommutations.
This count is forced by the structure of a balanced triple: the inactive EE|FF split contributes
both its qubits to the Z-type half, and each of the two active EF splits contributes one of
those same qubits to its X-type half. Varying the type assignment (e.g., making the EE-half
also X-type) eliminates all anticommutations and gives phase +1; such a product cannot
detect the π = −1 of the inactive split.
Corollary 4.4 (Partial resolution of the stabilizer sign-parity problem). The identity
πA πB πC = −1 has the following Clifford-group interpretation: for each 2-flat of A4 , the
product of three half-stabilizer operators (one Z-type from the inactive EE|FF split, two
X-types from the active EF|EF splits) carries a global phase of −1 and produces a weight-2
Y -type operator −Yα Yβ . This operator is a detectable error of the associated CSS code with
two-level syndrome structure:
• Generator-level: the number of X-generators whose support overlaps {α, β} in exactly
one qubit; this count depends on the specific pair {α, β} and ranges over {1, 2, 3} for
[[15, 7, 3]].
• Full-group level: among all 2n−1 − 1 non-trivial elements of the X-stabilizer group,
exactly 2n−2 have odd overlap with {α, β}, independently of the pair (Theorem 5.5).
The phase −1 = πEE · πEF1 · πEF2 is the Clifford avatar of the algebraic sign-parity product
identity.

## PDF page 5

ACTIVE STABILIZERS IN RM-CSS CODES FROM CD ZERO-DIVISORS

5

Remark 4.5 (What the −1 is not). The −1 does not appear as a product of weight-4
stabilizers. Indeed, in any CSS code, the X-stabilizer group and Z-stabilizer group are both
isomorphic to (F2 )r (abelian, all elements squaring to +I), so no product of stabilizer elements
can give −I. The −1 lives in the weight-2 sector of the full Pauli group, where Z and X
factors on the same qubit anticommute.
4.3. Computational verification for n = 4.
Proposition 4.6 (Step 2 verified for n = 4). For all 42 active mixed flats of ZD(4) and all 4
balanced triples per flat: the product (Zα Zβ )(Xα Xγ )(Xβ Xγ ) has phase −1 and operator Yα Yβ .
Verified by exhaustive computation using the fixed Cayley–Dickson sign table.
The verification uses the following universal argument (not dependent on the sign table at
all):
Lemma 4.7 (Universal phase lemma). For any two distinct qubits α, β and any qubit γ
(possibly equal to α or β, but not appearing twice in the product):
(Zα Zβ )(Xα Xγ )(Xβ Xγ ) = (Zα Xα ) · (Zβ Xβ ) · (Xγ )2 = (iYα )(iYβ )(I) = −Yα Yβ .
Proof. All operators on different qubits commute in the Pauli group. Use ZX = iY and
X 2 = I.
□
5. Step 3: Extension to n = 5 and General Syndrome Formula
5.1. Lo-flat structure for n = 5.
Theorem 5.1 (Step 3 — Bijection for n = 5). For n = 5, the following hold.
(i) There are exactly 15 Fano planes in PG(3, F2 ) (3-dimensional subspaces of F42 ), each
containing exactly 7 weight-4 lo-flat sets. The 105 lo-flat sets are partitioned by the
15 Fano planes: each lo-flat belongs to exactly one plane, so 15 × 7 = 105 with no
multiplicity.
(ii) The 15 Fano planes are in explicit bijection with the 15 non-identity elements of
the X-stabilizer group SX of the code [[15, 7, 3]] = CSS(Ham(4), Ham(4)), where
Ham(4) = [15, 11, 3] is the binary Hamming code. The bijection is
(
)
W ↦−→ gX {1, . . . , 15} \ W ,
i.e. each Fano plane W (7 points) maps to the X-stabilizer whose weight-8 support is
the complement of W in {1, . . . , 15} = PG(3, F2 ).
(iii) The product identity πA · πB · πC = −1 (Theorem 7.18 of [1]) holds for all 315 triples
arising from the 105 weight-4 lo-flat sets of A5 .
Proof. All three parts verified by exhaustive computation over A5 using the corrected Cayley–
Dickson sign table. (i): Uniqueness of the containing plane: given {a, b, c, d} ⊂ {1, . . . , 15}
with a⊕b⊕c⊕d = 0 and all elements nonzero, any three of {a, b, c, d} are linearly independent
over F2 (if dim span{a, b, c} = 2, the three non-zero elements of the 2-dimensional subspace are
exhausted by {a, b, c}, forcing d = a⊕b⊕c = 0, a contradiction). Hence W := span{a, b, c, d} is
the unique 3-dimensional subspace containing {a, b, c, d}. Direct enumeration gives 15×7 = 105
total, confirmed by computation (each of the 105 lo-flat sets belongs to exactly one plane).
(ii): complement map verified for all 15 Fano planes against all 15 non-trivial elements of SX .
(iii): 0 violations over 105 × 3 = 315 triples.
□

## PDF page 6

6

GIOVANNI LEVRATTI

Remark 5.2 (Bijection differs from n = 4). For n = 4: lo-flat sets Fk ⊂ {1, . . . , 7} (weight 4)
are directly the X-stabilizer supports (also weight 4). For n = 5: lo-flat sets (weight 4) are
contained within Fano planes, and the stabilizer supports are complements (weight 8). The
objects in bijection are the Fano planes (not individual lo-flat sets).
5.2. Sign-parity structure for n = 5.
Proposition 5.3 (Two π-types for n = 5). The 105 weight-4 lo-flat sets of A5 split into two
types by their canonical π-pattern:
• Type B (63 sets, 8 Fano planes with all 7 sets of type B): same uniform pattern as
n = 4: πEE|FF = −1, πEF1 = πEF2 = +1.
• Type A (42 sets, 7 Fano planes with 6 type-A and 1 type-B): pattern πEE|FF = −1,
πEF1 = −1, πEF2 = −1 for one split (fully inactive); and πEE|FF = +1, πEF1 = +1,
πEF2 = −1 for each of the other two splits.
Both types satisfy πA πB πC = −1. The type-B Fano planes correspond to the 8 planes in
PG(3, F2 ) whose ZD-projected structure is uniformly inherited from A3 ; the type-A planes
reflect the non-trivial ZD structure of A4 ⊂ A5 (sedenion sub-algebra).
5.3. Theorem B: Stability of the phase identity for all n.
Theorem 5.4 (Stability of πA πB πC = −1 and the phase identity). For all n ≥ 4 and every
mixed flat F = {i, j, 2n−1 +k, 2n−1 +l} in An :
(i) πA · πB · πC = −1 (Theorem 7.18 of [1]).
(ii) The balanced-triple product identity (Zα Zβ )(Xα Xγ )(Xβ Xγ ) = −Yα Yβ holds for any
three half-operators drawn from the three splits of F , with Z-type from the inactive
split and X-type from the active splits.
(iii) The global phase −1 equals πA πB πC for every n ≥ 4.
Proof. (i) is Theorem 7.18 of [1], valid for all n ≥ 4. (ii)–(iii): Lemma 4.7 (Universal Phase
Lemma) is a statement of pure Pauli algebra — it uses only ZX = iY , X 2 = I, and
commutativity of operators on distinct qubits — with no reference to the sign table or to
n. Therefore it holds for all n ≥ 4. The phase −1 = i2 from two ZX-anticommutations
corresponds to exactly πA πB πC = (−1)(+1)(+1) = −1.
□
5.4. General syndrome formula.
Theorem 5.5 (Syndrome weight formula). For the CSS code associated to ZD(n) based on
Ham(n − 1), and for any pair {α, β} ⊂ {1, . . . , 2n−1 − 1}, the number of non-trivial elements
of the full X-stabilizer group SX whose support has odd overlap with {α, β} is exactly 2n−2 ,
independently of the pair.
Note. This is the full-group syndrome weight, counting all 2n−1 − 1 non-trivial elements of
SX . The generator-level syndrome weight (number of generating syndrome bits equal to 1)
varies by pair.
Proof. Let k := n − 1 be the number of independent X-generators. For any pair {α, β}, let
s = (s1 , . . . , sk ) ∈ Fk2 be the generator-level syndrome: si = |{α, β} ∩ supp(gi )| mod 2. Since
α ̸= β are distinct nonzero elements of Fn−1
, their binary representations differ in at least one
2
bit position k, i.e. bitk (α) ̸= bitk (β). Since sk = |{α, β} ∩ supp(gk )| mod 2 = bitk (α) ⊕ bitk (β)
(the support of gk is exactly {j : bitk (j) = 1}; see Open Problem (2) below for the full
∏ Paulialgebra derivation), we have sk = 1, hence s ̸= 0. A non-trivial group element gM = i∈M gi

## PDF page 7

ACTIVE STABILIZERS IN RM-CSS CODES FROM CD ZERO-DIVISORS

7

⨁

(for non-empty
⨁ M ⊆ {1, . . . , k}) has odd overlap with {α, β} iffk i∈M si = 1. The evaluation
map M ↦→
i∈M si is a surjective F2 -linear functional on F2 (surjective since s ̸= 0), so
k−1
exactly 2
of the 2k subsets satisfy it. The empty set gives 0, so among the 2k − 1 non-empty
subsets: exactly 2k−1 = 2n−2 give value 1. Verified computationally for n = 4 (full-group
weight 4 = 22 , all 21 pairs) and n = 5 (full-group weight 8 = 23 , all 105 pairs). QPU results
(Theorem 5.6) confirm the generator-level syndromes, which are consistent with full-group
weight 8 as required.
□
5.5. QPU verification on IBM Quantum hardware.
Theorem 5.6 (QPU verification). The syndrome weight formula of Theorem 5.5 for n = 5
was verified experimentally on the ibm kingston quantum processor (156 qubits, 27 May
2026, job ID d8bm67ijki0s73aq6idg). Eight circuits (19 physical qubits each: 15 data + 4
ancilla) were executed at 8192 shots per circuit. The two experiment types are:
• Exp. A: prepare |+⟩⊗15 (eigenstate of all X-generators), apply Zα Zβ , measure Xsyndrome.
• Exp. B: prepare |0⟩⊗15 (eigenstate of all Z-generators), apply Xα Xβ , measure Zsyndrome.
Together they verify both components of the Yα Yβ syndrome. The bitstrings record the generatorlevel syndrome (4 bits for the 4 independent generators of [[15, 7, 3]]); the full-group syndrome
weight is 2n−2 = 8 for every nonzero generator syndrome, by Theorem 5.5. Results:
Circuit

Error

noerr expA
noerr expB
Z0Z1 expA
X0X1 expB
Z2Z3 expA
X2X3 expB
Z0Z14 expA
X0X14 expB

none
none
Z0 Z1
X0 X1
Z2 Z3
X2 X3
Z0 Z14
X0 X14

Expected Top result Fidelity
0000
0000
0011
0011
0111
0111
1110
1110

0000
0000
0011
0011
0111
0111
1110
1110

28.7%
51.4%
30.6%
49.9%
32.7%
44.5%
38.2%
53.8%

All 8 circuits match analytical predictions. Fidelities of 29–54% reflect circuit depth ≈ 150–180
native gates after transpilation on the 156-qubit device; the correct syndrome is the plurality
outcome in every case, confirming the syndrome structure above hardware noise.
[ VERIFIED on QPU — ibm kingston, 27 May 2026 ]
6. Open Problems
(1) Complete resolution of the stabilizer sign-parity problem. Theorem 4.2 and
Corollary 4.4 give the Clifford-group translation of πA πB πC = −1: the phase −1
manifests as a full-group syndrome weight of 2n−2 (confirmed analytically and on QPU,
Theorem 5.6; generator-level weight varies by pair). Whether the active/inactive split
plays a role in decoding capacity beyond the syndrome pattern remains open.
(2) Syndrome formula for all n [Resolved]. The full-group syndrome weight = 2n−2
holds for all n ≥ 4 and all pairs {α, β} with α ̸= β.

## PDF page 8

8

GIOVANNI LEVRATTI

Proof. It suffices to prove that the generator-level syndrome vector s(α, β) ∈ Fn−1
is
2
nonzero. The generator gXk of Ham(n−1) is the X-stabilizer with support supp(gXk ) =
{j ∈ {1, . . . , 2n−1 − 1} : bitk (j) = 1} (the k-th column of the Hamming parity-check
matrix).
Step 1. SW = X ⊗W anticommutes with Yα if and only if α ∈ W . This is Pauli
algebra: X and Y anticommute on the same qubit (XY = −Y X) and commute on
distinct qubits (XI = IX), so SW · Yα = (−1)[α∈W ] Yα · SW .
Step 2. For the two-qubit error E = Yα Yβ :
∣
∣
sk = 1 ⇐⇒ gXk anticommutes with E ⇐⇒ ∣{α, β} ∩ supp(gXk )∣ ≡ 1 (mod 2).
Since |{α, β} ∩ supp(gXk )| = [α ∈ supp(gXk )] + [β ∈ supp(gXk )], we obtain sk =
bitk (α) ⊕ bitk (β), and therefore
s(α, β) = α ⊕ β ∈ Fn−1
.
2
Step 3. Since α, β ∈ {1, . . . , 2n−1 − 1} are distinct, α ⊕ β ̸= 0, so s ̸= 0. The
algebraic proof of Theorem 5.5 then applies and gives full-group syndrome weight
= 2n−2 for all n ≥ 4 and all pairs.
□
(3) Type-A vs. Type-B Fano planes [Resolved]. Let W be a Fano plane in
{1, . . . , 15} = PG(3, F2 ). Recall that {1, . . . , 7} are the ε-type and {8, . . . , 15} the
3
f -type elements of A4 (the first layer of A3 → A4 doubling, with 8 = f eA
0 ). The
criterion is:
W is Type-B ⇐⇒ 8 ∈ W or W = {1, 2, 3, 4, 5, 6, 7}.
Proof. From the Cayley–Dickson construction A5 = CD(A4 ), three sign rules hold for
all i ∈ {1, . . . , 15}, k, l ∈ {1, . . . , 15}, k ̸= l (verified from the recursion):
(3)
εA5 (i, 16+k) = +εA4 (k, i),

εA5 (16+c, j) = −εA4 (c, j),

εA5 (16+c, 16+d) = −εA4 (c, d).

For a mixed flat {i, j, 16+k, 16+l} in A5 the π-value of the EF1 |EF2 split (with first
pair {i, 16+k}) reduces via (3) to
(4)

πEF1 = εA4 (i, j) · εA4 (k, j) · εA4 (l, i) · εA4 (k, l).
(Two sign flips from rules (2) and (3) cancel.)
Every lo-flat set F ⊂ W with 8 ∈ W belongs to one of two cases according to the
number of f -type elements of A4 in F :
• Case 1: two f -type elements in F (|F ∩ {8, . . . , 15}| = 2). Say F = {i, j, c, d}
with i, j ∈ {1, . . . , 7} and c, d ∈ {8, . . . , 15}.
Sub-case (1a): 8 ∈
/ F , i.e. c, d ∈ {9, . . . , 15}. Write c = 8 ⊕ c′ , d = 8 ⊕ d′
with c′ , d′ ∈ {1, . . . , 7}. Then {i, j, c′ , d′ } ⊂ {1, . . . , 7} is a lo-flat set of A4 and
A5
Theorem 3.2 gives π A4 ({i, j, c, d}, EF) = +1. Formula (4) then gives πEF
= +1.
Sub-case (1b): 8 ∈ F , i.e. c = 8 (wlog), d = 8 ⊕ d′ with d′ ∈ {1, . . . , 7}.
Theorem 3.2 does not apply directly since 8 has base-index 0 (the identity of A3 ).
Instead, formula (4) is evaluated using the special properties of e8 in A4 : for all
3
x ∈ {1, . . . , 15}, εA4 (x, 8) = +1 and εA4 (8, x) = −1 (consequence of e8 = (0, eA
0 )
in CD(A3 )). Each of the six EF-split values of (4) contains exactly one factor
εA4 (8, ·) = −1 and one factor εA4 (·, 8) = +1; combined with the remaining A3
signs (via εA4 (i, 8 ⊕ d′ ) = εA3 (d′ , i)), the product evaluates to +1. Verified for all
21 such lo-flat sets across the 7 planes with 8 ∈ W .

## PDF page 9

ACTIVE STABILIZERS IN RM-CSS CODES FROM CD ZERO-DIVISORS

9

• Case 2: four f -type elements in F (i.e. F = {c1 , c2 , c3 , c4 } ⊂ {8, . . . , 15}). Write
cs = 8 ⊕ us with us ∈ {0, 1, . . . , 7}. Formula (4) with all four indices in {8, . . . , 15}
reduces, via the f −f rule εA4 (8 ⊕ c, 8 ⊕ d) = −εA3 (c, d), to a product of four A3
signs. The resulting expression equals +1 by Lemma 7.24 of [1] (Quadrilateral
parity in O).
A5
In both cases πEF
= +1 for every EF split of every lo-flat set F ⊂ W . The product
A5
identity then forces πEE
= −1, giving the uniform Type-B pattern. The case W =
{1, . . . , 7} follows directly from Lemma 7.24 applied to A3 (all elements are ε-type in
A4 , no f -type involved). Verified computationally for all 7 × 7 = 49 lo-flat sets across
the 7 planes with 8 ∈ W .
□
Acknowledgements
Computational verifications were performed using the corrected Cayley–Dickson sign table
(build ten fixed) implemented in Python. Algebraic assistance and proof scaffolding provided
by Claude (Anthropic).
References
[1] G. Levratti, Sign-Parity Classification of Zero Divisors in Cayley–Dickson Algebras, Zenodo preprint
(2026), doi:10.5281/zenodo.20315751. Under review at Communications in Algebra.
[2] G. Levratti, Sign Structure, Automorphism Groups, and the ZD Zeta Function of Cayley–Dickson Algebras,
Zenodo preprint v4 (2026), doi:10.5281/zenodo.20397587.
[3] G. Levratti, Zero-Divisors in Cayley–Dickson Algebras: Fano Geometry, Automorphisms, and the Weil
Zeta Function, Zenodo preprint v10 (2026), doi:10.5281/zenodo.20417859.
[4] G. Levratti, The Informational Identity Boundary: Algebraic Foundations and Physical Conjectures,
Zenodo preprint v4 (2026), doi:10.5281/zenodo.20411845. Submitted to Foundations of Physics.
[5] A. M. Steane, Multiple-particle interference and quantum error correction, Proc. R. Soc. Lond. A 452
(1996), 2551–2577.
[6] D. Gottesman, Stabilizer Codes and Quantum Error Correction, Ph.D. thesis, California Institute of
Technology, 1997.
Independent Researcher, Modena, Italy
Email address: giovanni.levratti.research@gmail.com
