Source: https://zenodo.org/records/23966061/files/AWC%20Conjecture%20L;%20Wedderburn%20Classification%20of%20Left%20Multiplication%20Enveloping%20Algebras%20of%20Cayley.pdf
PDF sha256: 137b7109a1c38a9a35e5ba45f44b049f36cb0bf4a1b5673559faa729fd05a06f
License: https://creativecommons.org/licenses/by/4.0/

# Transcription of zhou_zhou_2026_awc_conjecture_l_wedderburn_left_multiplication_enveloping_algebras_cayley_dickson.pdf

Transcription of `zhou_zhou_2026_awc_conjecture_l_wedderburn_left_multiplication_enveloping_algebras_cayley_dickson.pdf` in this directory, 38 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-38 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

AWC Conjecture L: Wedderburn Classification of Left
Multiplication Enveloping Algebras of Cayley–Dickson
Algebras in Characteristic p and a Refutation of the
Cartan Doubling Recursion
Zhou Changzheng, Zhou Ziqing
Email: ziqing-zhou@outlook.com
November 4, 2026
Abstract
Let Fp be the prime field, and let An be the n-th Cayley–Dickson doubling
algebra, of dimension 2n . This paper studies the Wedderburn structure over Fp
of the left multiplication enveloping algebra EnvL (An ) of An , and examines the
feasibility of a Cartan-matrix recursion along the doubling tower. The classification
result falls into four branches: when p = 2, An is commutative and associative,
EnvL (An ) ∼
= An is a local algebra, and the Cartan matrix is [2n ]; when p is odd
and n = 1, EnvL (A1 ) is isomorphic to A1 , which either splits as Fp × Fp or is the
field Fp2 , with Cartan matrices I2 and [1], respectively; when p is odd and n = 2,
the left regular representation gives EnvL (A2 ) ∼
= A2 ∼
= M2 (Fp ), of dimension 4;
when p is odd and n ≥ 3, EnvL (An ) = EndFp (An ) ∼
= M2n (Fp ), and the Cartan
matrix is [1]. Along with the classification is a basis-product closure fact: for every
prime p and every n, the ordered product of standard basis elements is still a signed
multiple of some standard basis element and is nonzero; hence statistics supported
on zero basis pairs with positive density are empty at the object level. On this
basis, a Cartan doubling recursion of the form
(︃
)︃
Cn X
Cn+1 =
+ ∆n
X T Cn
cannot hold at the matrix-size level: for every n ≥ 1, the size of Cn+1 is always
1, whereas the right-hand side of the recursion is assembled from two copies of
Cn and hence has size at least 2; at the same time, permuting rows and columns
does not change matrix size, so this excludes dependence on the specific values
of the cross blocks and correction terms. Exact integer and modular-arithmetic
enumerations over finite ranges provide consistency checks for structure constants,
block formulas, closure dimensions, and centralizers; the general conclusions are
independently supported by the classification proof and the size inequality.

Keywords: Cayley–Dickson algebras; left multiplication enveloping algebras; Wedderburn classification; Cartan matrices; finite fields; doubling recursion.

1

## PDF page 2

1

Introduction

The Cayley–Dickson construction starts from a base field and, by repeated doubling, generates a sequence of algebras whose dimensions are successively doubled: one-dimensional,
two-dimensional, four-dimensional, eight-dimensional, and in general 2n -dimensional. Its
low-dimensional members are, respectively, a field, a quadratic algebra, a quaternion
algebra, and an octonion algebra, while the higher-dimensional members gradually lose
associativity, commutativity, and even alternativity. This construction has a foundational
position in the theory of nonassociative algebras; its systematic treatment can be traced
back to Schafer’s 1966 monograph (Schafer, 1966), in which associative multiplication
algebras were established as a general tool for studying the structure of nonassociative
algebras. Over the real field, Biss, Dugger, and Isaksen (2008) studied upper bounds for
the dimensions of annihilators of elements in Cayley–Dickson algebras, and Biss, Christensen, Dugger, and Isaksen (2009) subsequently systematized the theory of eigenvalues
and eigenvectors in order to clarify several structural properties of these algebras. These
works take the real field as the base field and focus on spectral properties and annihilators
as core objects.
In this paper we take the finite field Fp as the base field. The object of study is the
left multiplication enveloping algebra: the unital subalgebra generated over Fp by all left
multiplication operators Lx . The goal is the Wedderburn structure of this algebra, that
is, its position in the classification of finite-dimensional Fp -algebras—whether it is a local
algebra, a full matrix algebra, or a field or a direct product of fields. Wedderburn theory
over finite fields itself takes associative algebras as its standard framework, but when
the base algebra is nonassociative, the left multiplication operators no longer preserve
multiplication, and the structure of the enveloping algebra cannot be read directly from
the multiplication table of the base algebra. For this reason, the structural determination
case by case in n and p requires independent argument and cannot be transplanted from
spectral conclusions over the real field.
The key dividing line of the classification is at n = 2. The quaternion algebra A2 is
a four-dimensional associative algebra; when p is odd, its norm form is a nondegenerate
quadratic form, and over a finite field every nondegenerate quadratic form in at least
three variables is isotropic, so A2 splits and is isomorphic to M2 (Fp ). The left regular
map a ↦→ La is an algebra homomorphism when A2 is associative; its kernel is zero, and
the dimension of its image is 4, exactly that of M2 (Fp ). The full endomorphism algebra
End(A2 ), however, is M4 (Fp ), of dimension 16. Therefore EnvL (A2 ) is not isomorphic to
End(A2 ), and n = 2 must be treated as an independent case. When n ≥ 3, associativity is
lost, and the algebra generated by the left multiplication operators instead expands to the
full endomorphism algebra; the proof of this turn requires a separate first step n = 2 → 3,
whose surjectivity comes from the associativity and central simplicity of A2 , rather than
from a general induction hypothesis. The case p = 2 goes to the opposite extreme: the
square of the doubling generator degenerates to 1, the basis elements commute and are
associative, and An becomes F2 [(C2 )n ], whose enveloping algebra is a local algebra.
Parallel to the classification is the reading of the Cartan matrix. A full matrix algebra
is semisimple, its unique simple module is the natural module, and its unique indecomposable projective module is isomorphic to that simple module; the Cartan multiplicity
is 1, and the matrix is the 1 × 1 matrix [1], rather than the identity matrix. For a
local algebra, the Cartan element is the composition multiplicity, and the composition
multiplicity of the regular module equals 2n . This reading, together with the classifica2

## PDF page 3

tion, directly constrains the possible form of a recursion for the Cartan matrix along the
doubling tower. If a recursion writes Cn+1 as the block concatenation of two copies of
Cn plus a correction term, then the size of the right-hand side is at least 2rn ; but the
classification gives that the size of Cn+1 is always 1, so the size equality is impossible,
and there is no need to inspect any entries of the cross blocks or correction terms.
The framework of zero-divisor graphs of commutative rings—with vertices the nonzero
zero-divisors and edges joining distinct vertices whose product is zero—has a complete
theory in the commutative case, and its algebraic premises are commutativity of multiplication and the existence of zero-divisors. The standard basis products of Cayley–Dickson
algebras do not fall under these premises: the ordered product of basis elements is still
a signed multiple of some basis element and is nonzero, so the set of zero basis pairs
is empty. Therefore, transplanting density statistics of zero-divisor-graph type directly
onto Cayley–Dickson basis products has no corresponding nonempty set at the object
level. This fact is independent of the classification, but together they delimit the range
of structural assertions available over finite fields.
The paper proceeds as follows. We first give the Cayley–Dickson construction and
the definition of the left multiplication enveloping algebra; then we state and prove the
classification theorem case by case, where p = 2, n = 1, n = 2, and n ≥ 3 are treated
separately, and n = 2 → 3 is argued independently; next comes the basis-product closure
theorem; then the exclusion of the doubling recursion derived from the classification and
the Cartan reading; and finally the exact enumeration certificates over finite ranges and
the scope declaration. The general conclusions do not depend on the enumeration certificates; the certificates only check the implementation consistency of structure constants
and closure dimensions within the certified range.

2

Cayley–Dickson Construction, Left-Multiplication
Envelope Algebra, and Preliminary Lemmas

This chapter fixes the notation used throughout the paper and proves the three preliminary lemmas on which the classification theorem depends. Let Fp be the prime field, let
An be the n-th Cayley–Dickson doubled algebra of dimension N = 2n ; let Lx and Rx denote the left and right multiplication operators, respectively, and let EnvL (An ) denote the
unital subalgebra of EndFp (An ) generated over Fp by all Lx , called the left-multiplication
envelope algebra of An . Cartan matrices are defined with respect to a complete set of
primitive orthogonal idempotents; the size of a matrix is invariant under simultaneous
permutation of rows and columns.

2.1

Cayley–Dickson Construction and Basic Identities

Take A0 = Fp , and construct recursively by An+1 = An ⊕ An . For (a, b), (c, d) ∈ An+1 ,
multiplication and conjugation are defined by
¯ da + bc̄),
(a, b)(c, d) = (ac − db,

3

(a, b) = (ā, −b).

## PDF page 4

The standard basis is denoted by e0 = 1, e1 , . . . , eN −1 , where ē0 = e0 and ēi = −ei
for i ≥ 1. Denote the conjugation map by C(x) = x̄. Since conjugation is an antiautomorphism, one directly obtains
CLx C = Rx̄ ,

CRx C = Lx̄ .

These two identities are different, and in the sequel they are used only in the directions
stated above.
According to the block decomposition An ⊕An , the left multiplication operators satisfy
(︃
)︃
0 −Rb C
L(a,0) = diag(La , Ra ),
L(0,b) =
.
Lb C
0
These block formulas follow directly from the doubled multiplication formula and are the
basic tool for the subsequent induction.

2.2

Preliminary Lemmas

Lemma 2.1 (Centrality). Let p be odd and n ≥ 2. Then Z(An ) = Fp .
Proof. Let (a, b) ∈ An+1 belong to the center. First commute it with all elements
(c, 0), and compute
(a, b)(c, 0) = (ac, bc̄),

(c, 0)(a, b) = (ca, bc).

Comparing the two components gives ac = ca and bc̄ = bc for all c. Taking c = e1 , we
obtain b(−e1 ) = be1 , that is, 2be1 = 0; since p is odd and e1 is invertible (e21 = −1),
it follows that b = 0. Thus central elements have the form (a, 0), with a ∈ Z(An ).
Commuting next with (0, c) gives ca = cā for all c; taking c = 1 yields a = ā. Therefore
Z(An+1 ) = {(a, 0) : a ∈ Z(An ), a = ā}.
When n = 1, A1 = Fp [x]/(x2 + 1), conjugation is x ↦→ −x, and the fixed elements are
exactly Fp ; hence Z(A2 ) = Fp . By induction from the displayed formula, Z(An ) = Fp for
all n ≥ 2. This completes the proof.
Lemma 2.2 (Subdirect Product Dichotomy). Let F be a subalgebra of MN (Fp )⊕
MN (Fp ) such that the projections of F onto both factors are surjective. Then either F is
the entire direct sum, or F is the graph of some automorphism σ ∈ Aut(MN (Fp )), that
is,
F = {(X, σ(X)) : X ∈ MN (Fp )}.
Proof. Let π1 , π2 be the two coordinate projections, and set I1 = F ∩ (MN ⊕ 0),
I2 = F ∩ (0 ⊕ MN ). First prove that I1 is a two-sided ideal of MN : I1 is an ideal of F ;
for any X ∈ MN and t ∈ I1 , since π1 |F is surjective, there exists f ∈ F with π1 (f ) = X,
so Xt = π1 (f t) ∈ I1 , and similarly tX = π1 (tf ) ∈ I1 . By simplicity of MN (Fp ), I1 is
either zero or the whole algebra; the same holds for I2 . If I1 is the whole algebra, then
for any Y ∈ MN , by surjectivity of π2 |F there exists (X, Y ) ∈ F , while (X, 0) ∈ F ,
hence (0, Y ) = (X, Y ) − (X, 0) ∈ F , so I2 is also the whole algebra. Therefore, after
excluding the mixed case in which one of I1 , I2 is the whole algebra and the other is zero,
only two possibilities remain: either both I1 and I2 are the whole algebra, in which case
F = MN ⊕ MN ; or both I1 and I2 are zero, in which case the kernels of π1 |F and π2 |F are
4

## PDF page 5

both zero, and by the surjectivity assumption both are isomorphisms; then σ = π2 ◦ π1−1
is an automorphism of MN (Fp ), and F is exactly the graph of σ. This completes the
proof.
Lemma 2.3 (Diagonalization of Doubled Blocks). For any b, b′ ∈ An ,
L(0,b) L(0,b′ ) = diag(−Rb Rb̄′ , −Lb Lb̄′ ).
In particular, taking b = b′ = 1 gives L2(0,1) = − id. Therefore, when p is odd, L(0,1) is
invertible.
Proof. Substitute directly into the block formula and use CLx C = Rx̄ , CRx C = Lx̄ .
Taking b = b′ = 1, we have R1 = L1 = id, so the square is − id. When p is odd, −1 ̸= 0,
so the operator is invertible. This completes the proof.

3

Wedderburn Classification of the Left-Multiplication
Envelope Algebra

This chapter gives a complete Wedderburn classification of the left-multiplication envelope algebra. Notation and preliminary lemmas are as in Chapter 2.

3.1

Statement of the Theorem

Theorem 3.1. Let p be a prime and let An be the n-th Cayley–Dickson algebra.
(1) p = 2. An is commutative and associative, An ∼
= F2 [(C2 )n ]; EnvL (An ) ∼
= An is a
n
local algebra, the Jacobson radical has dimension 2 − 1, and the Cartan matrix is [2n ].
(2) p is odd and n = 1. A1 = Fp [x]/(x2 + 1). If −1 is a square modulo p, then
A1 ∼
= Fp 2 ,
= Fp × Fp , and the Cartan matrix is I2 ; if −1 is not a square modulo p, then A1 ∼
and the Cartan matrix is [1].
(3) p is odd and n = 2. A2 ∼
= M2 (Fp ), and a ↦→ La is an algebra isomorphism from
∼
A2 to EnvL (A2 ), so EnvL (A2 ) = M2 (Fp ); the Cartan matrix is [1].
(4) p is odd and n ≥ 3. EnvL (An ) = EndFp (An ) ∼
= M2n (Fp ); the Cartan matrix is [1].

5

## PDF page 6

Classification roadmap for EnvL (An ) over Fp
Input: prime p and level n

p

=

2

An commutative and associative;
EnvL (An ) ∼
= An local; Cartan [2n ]

p odd

n

=

1

EnvL (A1 ) ∼
= A1 ; split Fp × Fp gives
Cartan I2 , nonsplit Fp2 gives Cartan [1]

n

=

2

A2 ∼
= M2 (Fp ); EnvL (A2 ) ∼
= M2 (Fp ); Cartan [1]

n

≥

3

EnvL (An ) = End(An ) ∼
= M2n (Fp ); Cartan [1]

Legend: blue nodes describe the characteristic 2 branch;
green nodes are case splits for odd characteristic; yellow
nodes are the resulting Wedderburn types and Cartan matrices.
Figure 1: Case split of Theorem 3.1.

3.2

Preliminary Facts

This chapter uses four preliminary facts. Noncommutativity is newly proved in this
chapter; centrality, the subdirect product dichotomy, and diagonalization of doubled
blocks have already been proved as Lemmas 2.1, 2.2, and 2.3 in Chapter 2, and are
restated here in the notation of this chapter so that internal references in this chapter
are self-contained.
Fact 3.1 (Noncommutativity). Let p be odd and n ≥ 2. Then An is noncommutative. In particular, Le1 ̸= Re1 .
Proof. In the Cayley–Dickson basis, e1 e2 = −e2 e1 , and e1 e2 is some ±ek , hence
nonzero. If e1 e2 = e2 e1 , then 2e1 e2 = 0; since p is odd and e1 e2 ̸= 0, this is a contradiction.
Hence An is noncommutative. Taking x = e2 , we get Le1 (e2 ) = e1 e2 ̸= e2 e1 = Re1 (e2 ), so
6

## PDF page 7

Le1 ̸= Re1 . This completes the proof.
Fact 3.2 (Centrality). Let p be odd and n ≥ 2. Then Z(An ) = Fp .
Proof. Let (a, b) ∈ An+1 belong to the center. First commute it with all (c, 0), and
compute
(a, b)(c, 0) = (ac, bc̄),
(c, 0)(a, b) = (ca, bc).
Comparing the two components gives ac = ca and bc̄ = bc for all c. Taking c = e1 , we
obtain b(−e1 ) = be1 , that is, 2be1 = 0; since p is odd and e1 is invertible (e21 = −1),
it follows that b = 0. Thus central elements have the form (a, 0), with a ∈ Z(An ).
Commuting next with (0, c) gives ca = cā for all c; taking c = 1 yields a = ā. Therefore
Z(An+1 ) = {(a, 0) : a ∈ Z(An ), a = ā}.
When n = 1, A1 = Fp [x]/(x2 + 1), conjugation is x ↦→ −x, and the fixed elements are
exactly Fp ; hence Z(A2 ) = Fp . By induction from the displayed formula, Z(An ) = Fp for
all n ≥ 2. This completes the proof.
Fact 3.3 (Subdirect Product Dichotomy). Let F be a subalgebra of MN (Fp ) ⊕
MN (Fp ) such that the projections of F onto both factors are surjective. Then either F is
the entire direct sum, or F is the graph of some automorphism σ ∈ Aut(MN (Fp )), that
is,
F = {(X, σ(X)) : X ∈ MN (Fp )}.
Proof. Let π1 , π2 be the two coordinate projections, and set I1 = F ∩ (MN ⊕ 0),
I2 = F ∩ (0 ⊕ MN ). First prove that I1 is a two-sided ideal of MN : I1 is an ideal of F ;
for any X ∈ MN and t ∈ I1 , since π1 |F is surjective, there exists f ∈ F with π1 (f ) = X,
so Xt = π1 (f t) ∈ I1 , and similarly tX = π1 (tf ) ∈ I1 . By simplicity of MN (Fp ), I1 is
either zero or the whole algebra; the same holds for I2 . If I1 is the whole algebra, then
for any Y ∈ MN , by surjectivity of π2 |F there exists (X, Y ) ∈ F , while (X, 0) ∈ F ,
hence (0, Y ) = (X, Y ) − (X, 0) ∈ F , so I2 is also the whole algebra. Therefore, after
excluding the mixed case in which one of I1 , I2 is the whole algebra and the other is zero,
only two possibilities remain: either both I1 and I2 are the whole algebra, in which case
F = MN ⊕ MN ; or both I1 and I2 are zero, in which case the kernels of π1 |F and π2 |F are
both zero, and by the surjectivity assumption both are isomorphisms; then σ = π2 ◦ π1−1
is an automorphism of MN (Fp ), and F is exactly the graph of σ. This completes the
proof.
Fact 3.4 (Diagonalization of Doubled Blocks). For any b, b′ ∈ An ,
L(0,b) L(0,b′ ) = diag(−Rb Rb̄′ , −Lb Lb̄′ ).
In particular, taking b = b′ = 1 gives L2(0,1) = − id. Therefore, when p is odd, L(0,1) is
invertible.
Proof. Substitute directly into the block formula
(︃
)︃
0 −Rb C
L(0,b) =
Lb C
0
and use CLx C = Rx̄ , CRx C = Lx̄ . Taking b = b′ = 1, we have R1 = L1 = id, so the
square is − id. When p is odd, −1 ̸= 0, so the operator is invertible. This completes the
proof.

7

## PDF page 8

3.3

The Case p = 2

The associator of a Cayley–Dickson algebra is alternating in its three variables and trilinear; on basis triples, the associator takes values in {0, ±2em }. Induct on the doubling
index: the four index types reduce to associators of the algebra one level lower; the case
in which all entries lie in the second copy is eliminated by the alternating cyclic identity
(x, y, z) = (y, z, x). Hence, after reduction modulo 2, the associator is identically zero.
Similarly, the commutator ei ej − ej ei takes values in {0, ±2ek } on basis elements, and is
zero modulo 2. Thus An is commutative and associative in characteristic 2.
The doubling units uj = e2j−1 (j = 1, . . . , n) satisfy u2j = −1 = 1 and commute with
one another; they generate An . Therefore gj ↦→ uj gives an isomorphism from F2 [(C2 )n ]
to An , since both sides have dimension 2n . The augmentation ideal is nilpotent, so An is
local. Since An is associative, the left regular representation is faithful, and the image of
EnvL (An ) is An itself, so EnvL (An ) ∼
= An . A local algebra has a unique simple module,
namely the trivial module, and a unique indecomposable projective module, namely the
regular module, of dimension 2n ; hence the Cartan matrix is [2n ].

3.4

The Case p Odd and n = 1

A1 = Fp [x]/(x2 + 1). If −1 is a square, then x2 + 1 splits and A1 ∼
= Fp × Fp ; the two simple
modules are nonisomorphic, and each indecomposable projective module is isomorphic to
the corresponding simple module, so the Cartan matrix is I2 . If −1 is not a square, then
A1 is the field Fp2 ; the unique simple module is the regular module itself, and the unique
indecomposable projective module is isomorphic to that simple module, so the Cartan
multiplicity is 1, and the Cartan matrix is [1]. In both cases A1 is associative, and the
left regular representation gives EnvL (A1 ) ∼
= A1 .

3.5

The Case p Odd and n = 2

The norm form of the quaternion algebra A2 is a nondegenerate quadratic form. Over a
finite field, every nondegenerate quadratic form in at least 3 variables is isotropic; hence
A2 has nonzero zero divisors and is not a division algebra. A2 is a four-dimensional central
simple algebra; a four-dimensional central simple algebra that is a division algebra must be
a field, contradicting its noncommutativity. Hence A2 ∼
= M2 (Fp ). Since A2 is associative,
Lab = La Lb , so the left regular representation a ↦→ La is an algebra homomorphism; its
kernel is zero, hence it is injective. The dimension of its image equals the dimension
of A2 , namely 4, while the dimension of EndFp (A2 ) is 16; therefore the image is exactly
M2 (Fp ). Thus EnvL (A2 ) ∼
= M2 (Fp ). The full matrix algebra M2 (Fp ) is semisimple, its
unique simple module is the natural module, and its unique indecomposable projective
module is isomorphic to the natural module; the Cartan matrix is [1].

8

## PDF page 9

3.6

The Case p Odd and n ≥ 3

3.6.1

First Step: n = 2 → 3

A2 is associative and central simple, with center Fp . The natural map
A2 ⊗Fp Aop
2 → EndFp (A2 ),

a ⊗ c ↦→ La Rc

is the structural isomorphism for central simple algebras; hence
span{La Rc : a, c ∈ A2 } = EndFp (A2 ) = M4 (Fp ).
Here we used the associativity of A2 : La and Rc commute as operators.
Let E = EnvL (A3 ) ⊆ End(A3 ) = M8 (Fp ), and let F = E ∩ (M4 ⊕ M4 ) be the diagonal
part of E. Write Pa = L(a,0) = diag(La , Ra ), Qb = L(0,b) . The even words Pa Qb Qb′ and
Qb Qb′ Pa′ both belong to F . By Fact 3.4,
Qb Qb′ = diag(−Rb Rb̄′ , −Lb Lb̄′ ).
Thus the two diagonal blocks of Pa Qb Qb′ are of the form La Rc and Rc La , respectively.
Since span{La Rc } = M4 and associativity of A2 makes left and right multiplication
commute, the projections of F onto both M4 -factors are surjective. By Fact 3.3, either
F = M4 ⊕ M4 , or F is the graph of some automorphism σ.
If F is the graph of σ, then from diag(La , Ra ) ∈ F we obtain σ(La ) = Ra for all
a ∈ A2 . By Skolem–Noether, σ = AdG for some invertible G. Evaluating the relation
GLa G−1 = Ra at 1 ∈ A2 gives G(ag) = a, where g = G−1 (1). Hence A2 g = A2 , so g is
invertible, and G = Rg−1 . Substituting back gives Rg−1 La Rg = Ra ; here, by associativity
of A2 , La commutes with Rg , so La = Ra for all a. But by Fact 3.1, Le1 ̸= Re1 , a
contradiction. Therefore F = M4 ⊕ M4 .
Finally, by Fact 3.4, Z = L(0,1) satisfies Z 2 = − id, so Z is invertible. Multiplication
by Z sends F onto all off-diagonal blocks; hence E = M8 (Fp ) = End(A3 ). The first step
is established.

3.6.2

General Induction n → n + 1 for n ≥ 3

Assume that EnvL (An ) = End(An ) = MN (Fp ), where N = 2n . From CLx C = Rx̄ we
obtain
EnvR (An ) = C EnvL (An )C = End(An ) = MN .
Let E = EnvL (An+1 ) ⊆ End(An+1 ) = M2N (Fp ), and F = E ∩ (MN ⊕ MN ).
The subalgebra F contains all even words Pa1 · · · Pak involving only P -factors. Its first
projection is La1 · · · Lak , and all such left-multiplication words span EnvL (An ) = MN ; its
second projection is Ra1 · · · Rak , and all such right-multiplication words span EnvR (An ) =
MN . Hence the projections of F onto both MN -factors are surjective. By Fact 3.3, either
F = MN ⊕ MN , or F is the graph of some automorphism σ.
If F is the graph of σ, then from diag(La , Ra ) ∈ F we obtain σ(La ) = Ra for all
a ∈ An . By Skolem–Noether, σ = AdG for some invertible G. The following derivation
uses only two structural facts that hold at every level of the doubling tower. The first
is the flexible identity (xy)x = x(yx), verified directly level by level from the doubled
multiplication formula, whose linearization is
(xy)z + (zy)x = x(yz) + z(yx);
9

## PDF page 10

the second is the operator identity obtained from GLa G−1 = Ra by composition and
evaluation. To make the argument valid at every level of the tower, this step uses only
the facts stated above, which hold at every level; the argument does not use alternativity
or any of its consequences (such as cancellation properties of invertible elements in alternative algebras). All cancellation needed is supplied by the operator fact that G and
Rg are mutually inverse maps, a fact involving only composition of operators, not the
associativity of multiplication.
Evaluating the relation GLa G−1 = Ra at 1 ∈ An gives
for all a ∈ An ,

G(ag) = a

where g = G−1 (1). Write h = G(1).
Since G(ag) = a for all a, the composite map G ◦ Rg is the identity; hence Rg is
injective and G is surjective. Conversely, for any x, take a = G(x); from G(ag) = a and
injectivity of G, we get ag = x, that is, Rg (G(x)) = x, so Rg ◦ G is also the identity.
Thus G and Rg are mutually inverse maps, and both are bijections. In particular, taking
a = h in G(ag) = a gives G(hg) = h = G(1); by injectivity of G,
hg = 1.
Multiplying GLa G−1 = Ra on the left by G gives GLa = Ra G, that is,
for all a, y ∈ An .

G(ay) = G(y)a

Taking y = 1 gives G = Lh , that is, G is the left multiplication operator Lh , and Lh is a
bijection. Taking a = g in this identity gives
for all y ∈ An ;

h(gy) = (hy)g

the right-hand side is Rg (Lh (y)) = y, so h(gy) = y for all y, that is, Lh Lg is the identity.
Since Lh is a bijection, Lg = L−1
h , and hence Lg Lh is also the identity, that is,
g(ha) = a

for all a ∈ An .

Taking a = 1 gives gh = 1.
Now take the triple (x, y, z) = (a, h, g) in the linearization of the flexible identity. The
two terms on the left are (ah)g and (gh)a, and the two terms on the right are a(hg) and
g(ha). Substituting hg = 1, gh = 1, and g(ha) = a, we obtain
(ah)g + a = a + a,

that is,

(ah)g = a.

Comparing this with the previously obtained (ha)g = a, injectivity of Rg gives ah = ha
for all a ∈ An , that is, h ∈ Z(An ). By Fact 3.2, Z(An ) = Fp , so h = λ · 1, with λ ̸= 0.
From λg = hg = 1 (scalar multiplication being given by bilinearity), we get g = λ−1 · 1.
Therefore G = Lh is a scalar operator, and σ = AdG is the identity automorphism. But
σ(Le1 ) = Re1 , while by Fact 3.1, Le1 ̸= Re1 , a contradiction. Therefore F = MN ⊕ MN .
Again by Fact 3.4, Z = L(0,1) satisfies Z 2 = − id, so it is invertible; multiplication by
Z sends F onto all off-diagonal blocks, so E = M2N (Fp ) = End(An+1 ). The induction is
complete.

10

## PDF page 11

3.7

Cartan Readings

When p = 2, EnvL (An ) ∼
= An is a local algebra. Its unique simple module is the trivial module, of dimension 1; its unique indecomposable projective module is the regular
module, of dimension 2n . From the dimension identity dim P = [P : S] dim S, we get
[P : S] = 2n , so the Cartan matrix is [2n ].
When p is odd and n = 1, in the split case A1 ∼
= Fp × Fp there are two simple
modules, each indecomposable projective module is isomorphic to the corresponding simple module, and the Cartan matrix is I2 ; in the nonsplit case A1 ∼
= Fp2 is a field, the
unique simple module and the unique indecomposable projective module coincide, and
the Cartan matrix is [1].
When p is odd and n ≥ 2, by Theorem 3.1, EnvL (An ) is the full matrix algebra
Mm (Fp ), where m = 2 for n = 2 and m = 2n for n ≥ 3. A full matrix algebra is
semisimple, its unique simple module is the natural module, and its unique indecomposable projective module is isomorphic to the natural module; the dimension identity gives
Cartan multiplicity 1. Therefore the Cartan matrix is the 1 × 1 matrix [1]. In particular,
it is not Im .

3.8

Exclusion of a Cartan Doubling Recursion

Let Cn be the Cartan matrix of EnvL (An ) with respect to an arbitrary complete set of
primitive orthogonal idempotents. By Theorems 3.1 and 3.7, the size of Cn is at most 2:
in the split case n = 1 it is the 2 × 2 matrix I2 ; in all other cases it is the 1 × 1 matrix
[1] or [2n ]. Therefore the size rn of Cn belongs to {1, 2}; and for every n ≥ 1, rn+1 = 1,
because when n + 1 ≥ 2, odd characteristic has already entered the full matrix algebra
case, while in characteristic 2 the Cartan matrix [2n+1 ] is still 1 × 1.
Consider the formal recursion
(︃
)︃
Cn X
Cn+1 =
+ ∆n ,
X T Cn
where X is an independent cross block. If the block decomposition is legitimate, the
right-hand side is formed from two copies of Cn and has size 2rn × 2rn . The left-hand
side Cn+1 has size rn+1 . If the equality holds, one must have rn+1 = 2rn . But rn+1 = 1
while 2rn ≥ 2: when rn = 1, the right-hand side has size 2 and the left-hand side has
size 1; when rn = 2, the right-hand side has size 4 and the left-hand side has size 1. In
each case they are unequal. A Cartan matrix permits only simultaneous permutation of
rows and columns, and simultaneous permutation does not change the size of the matrix.
Therefore this recursion is impossible at the level of matrix size for every prime p and
every n ≥ 1, without checking the concrete entries of X or ∆n .

3.9

Description of a Reproducibility Algorithm

The following describes an algorithmic procedure that can be used for exact verification
in finite ranges; it uses no floating-point arithmetic and does not depend on external data
sources.
(1) Construction of structure constants. Recursively construct the multiplication table
of An by integer arithmetic according to the doubling formula. For each pair of basis
11

## PDF page 12

elements (ei , ej ), compute the four blocks according to (a, b)(c, d) = (ac − ¯
db, da + bc̄),
obtaining integer structure constants; then reduce modulo the target prime p.
(2) Check that basis products are nonzero. Enumerate all ordered basis pairs (ei , ej ),
compute the product, and check whether it is exactly ±ek and nonzero. The complexity
of this check is O(22n ), suitable for full enumeration when n is small.
(3) Left multiplication matrices and envelope dimension. For each basis element ei ,
construct the N × N matrix of the left multiplication operator Lei . Starting from the
identity operator and these generators, repeatedly take products and maintain a linear
basis by Gaussian elimination modulo p until the dimension stabilizes; the resulting
dimension is the dimension of EnvL (An ).
(4) Computation of the centralizer. Expand the condition ax = xa for all basis
elements x into a system of linear equations in the coordinates of a, and solve for Z(An ).
This step is used to check instances of the centrality lemma in finite ranges.
(5) Cartan readings. For a given finite-dimensional algebra, compute the Jacobson
radical, decompose a complete set of primitive orthogonal idempotents, construct the
indecomposable projective modules Λei , compute the multiplicities of their simple heads,
and obtain the Cartan matrix. For full matrix algebras and local algebras, one can check
directly using the dimension identity in 3.7.
(6) Scope declaration. The above algorithm gives only machine certification for finite
n and finite p, and does not replace the general proofs in 3.3–3.6; its role is to check the
implementation consistency of structure constants, block formulas, centrality, and closure
dimensions within the certified range.

3.10

Boundaries and Risk Statement

The conclusions of this chapter depend on three standard facts: every nondegenerate
quadratic form in at least 3 variables over a finite field is isotropic; the Skolem–Noether
theorem; and the natural structural map A ⊗ Aop → End(A) for central simple algebras
is an isomorphism. These facts are used only as external standard results in the proof
and are not reproved in this chapter.
The case n = 2 is a boundary case and cannot be merged into the full endomorphism
case n ≥ 3; the first step n = 2 → 3 must be argued separately, and its surjectivity
depends on the associativity and central simplicity of A2 , which cannot be replaced by the
general induction hypothesis. The surjectivity of the projections in the general induction
for n ≥ 3 depends on all even words involving only first-kind doubling generators, not
merely quadratic left-multiplication words; nonassociativity of An means that long words
cannot in general be reduced to quadratic words.
The key step in the graph argument for n ≥ 3, where a contradiction is derived from
the graph assumption for σ, depends only on two independent preliminary facts: the
flexible identity (xy)x = x(yx) (and its linearization, verified directly level by level from
the doubled multiplication formula, valid at every level of the doubling tower) and the
centrality conclusion of Fact 3.2. Both are proved before the classification theorem and do
not depend on the classification conclusion, so the argument is not circular. It should be
made explicit that the argument does not use alternativity, nor the cancellation property
of invertible elements enjoyed only by alternative algebras; all cancellation appearing in
the argument is supplied by the fact that G and Rg are mutually inverse maps, a fact
involving only operator composition and independent of the associativity of multiplica-

12

## PDF page 13

tion. Likewise, any step that transfers the reasoning that “left and right multiplication
commute” at n = 2 to n ≥ 3 is invalid, because An is nonassociative and left and right
multiplication operators do not commute in general.
The reading of the Cartan matrix depends on the choice of a complete set of primitive orthogonal idempotents, but the size of the matrix is invariant under simultaneous
permutation of rows and columns; the Cartan matrix of a full matrix algebra is [1], not
the identity matrix Im . The exclusion of the recursion is an impossibility at the level of
matrix size and does not involve the concrete entries of X or ∆n .
Machine certification covers only finite ranges; the general conclusions of this chapter
are given by the inductive proofs in 3.3–3.6.

4

Basis Product Closure Theorem
Doubling-basis multiplication patterns in An+1 = An ⊕ An
Pi

=

(ei , 0)

Pj

=

(ej , 0)

Qj

=

(0, ej )

Qi

=

(0, ei )

Pi Pj

=

(ei ej , 0)

Pi Qj

=

(0, ej ei )

Qi Pj

=

(0, ei C(ej ))

Qi Qj

=

(−C(ej )ei , 0)

Legend: Pi and Qi denote the lifted basis elements in
An+1 . The four displayed products are the only cases
needed in the induction proofs, together with C(ej ) = δj ej
where δ0 = 1 and δj = −1 for j ≥ 1 when p is odd.
Figure 2: Four multiplication types for doubled basis elements.

4.1

Problem Framework and Notation

This chapter discusses the multiplicative closure property of the standard basis of Cayley–
Dickson algebras. We use the notation of Chapter 3 throughout: Fp is the prime field, An
13

## PDF page 14

is the n-th Cayley–Dickson doubled algebra of dimension N = 2n ; the standard basis is
denoted by e0 = 1, e1 , . . . , eN −1 ; the conjugation map is denoted by C(x) = x̄, satisfying
C(e0 ) = e0 and C(ei ) = −ei for i ≥ 1. The doubling formula is
(a, b)(c, d) = (ac − C(d)b, da + bC(c)),
where a, b, c, d ∈ An . The standard basis of An+1 consists of two groups: the first group
Pi = (ei , 0), and the second group Qi = (0, ei ), i = 0, . . . , N − 1.
The proposition to be proved in this chapter has two levels. The first is closure: the
product of any two standard basis elements is again a signed multiple of some standard
basis element. The second is nonvanishing: this signed multiple is nonzero. Both must
be proved simultaneously and cannot replace each other. Nonvanishing has another
independent route, for example, some basis elements are invertible; but invertibility can
only exclude zero products and cannot imply that the product is still a single basis
element. Therefore, the inductive proof of closure cannot be omitted.
This chapter does not rely on experimental data sets; the subsequent verification algorithms perform only exact integer and modular arithmetic enumeration in finite ranges,
and are algorithmic consistency checks, not replacements for the general proof.

4.2

Conjugation Action and Multiplication Table of the Doubled Basis

In the standard basis, conjugation only changes signs and does not change basis indices.
Specifically, there exist δj ∈ {1, −1} such that
C(ej ) = δj ej ,
where δ0 = 1 and δj = −1 for j ≥ 1. In Fp , the values of δj vary with p: when p is odd,
δj is as above; when p = 2, −1 = 1, so all δj equal 1. In either case, δj is a nonzero
constant.
From the doubling formula one directly obtains the four types of basis-pair multiplications:
Pi Pj = (ei ej , 0);
Pi Qj = (0, ej ei );
Qi Pj = (0, ei C(ej ));
Qi Qj = (−C(ej )ei , 0).
These four types cover all standard basis pairs of An+1 . The subsequent induction uses
only these four formulas and C(ej ) = δj ej .

4.3

Basis Product Closure Theorem

Theorem 4.1. Let p be any prime and n ≥ 0. For any i, j ∈ {0, . . . , 2n − 1}, there exist
k ∈ {0, . . . , 2n − 1} and ε ∈ {1, −1} such that
ei ej = εek ,
and εek ̸= 0. In particular, there are no zero basis pairs in the standard basis of An , that
is, ei ej = 0 never holds for any i, j.

14

## PDF page 15

4.4

Inductive Proof

Proceed by induction on n.
Base case n = 0. Here A0 = Fp , and the unique standard basis element is e0 = 1. We
have e0 e0 = e0 ; take ε = 1, k = 0, and the conclusion holds.
Induction hypothesis. Assume that the standard basis of An satisfies Theorem 4.1:
for any i, j, there exist k and ε ∈ {1, −1} such that ei ej = εek , and εek ̸= 0.
Induction step n → n + 1. Consider the four types of basis pairs of An+1 .
First type: Pi Pj . By the multiplication table,
Pi Pj = (ei ej , 0).
By the induction hypothesis, ei ej = εek , where ε ∈ {1, −1} and ek is a standard basis
element of An . Hence
Pi Pj = ε(ek , 0) = εPk .
This is a signed multiple of a standard basis element of An+1 , and εPk ̸= 0, because ε ̸= 0
and Pk is a basis element.
Second type: Pi Qj . By the multiplication table,
Pi Qj = (0, ej ei ).
By the induction hypothesis, ej ei = εel . Hence
Pi Qj = ε(0, el ) = εQl .
Again we obtain a signed multiple of a standard basis element, and it is nonzero.
Third type: Qi Pj . By the multiplication table,
Qi Pj = (0, ei C(ej )).
By the conjugation action, C(ej ) = δj ej , with δj ∈ {1, −1}. By the induction hypothesis,
ei ej = εek . Hence
ei C(ej ) = δj ei ej = δj εek .
Therefore
Qi Pj = δj εQk .
Here δj ε ∈ {1, −1}, Qk is a standard basis element, and δj εQk ̸= 0.
Fourth type: Qi Qj . By the multiplication table,
Qi Qj = (−C(ej )ei , 0).
From C(ej ) = δj ej and the induction hypothesis ej ei = εel , we get
−C(ej )ei = −δj ej ei = −δj εel .
Therefore
Qi Qj = −δj εPl .
Here −δj ε ∈ {1, −1}, Pl is a standard basis element, and the product is nonzero.
All four types of basis pairs have been treated. In each case we obtain a form ε′ em ,
where ε′ ∈ {1, −1}, em is a standard basis element of An+1 , and ε′ em ̸= 0. The induction
is complete, and Theorem 4.1 holds for all n ≥ 0 and all primes p.
15

## PDF page 16

The conditions used in the proof are as follows: the doubled multiplication formula
is the definition; the conjugation action C(ej ) = δj ej is guaranteed by the recursive
construction of the standard basis; the induction hypothesis contains both closure and
nonvanishing, so the lower-level products in the four cases give both the basis index and
the nonzero coefficient. When p = 2, both δj and −1 degenerate to 1, but the statement
“there exists ε ∈ {1, −1}” still holds, and nonvanishing also still holds, because basis
elements are nonzero over F2 and the coefficient is 1.

4.5

The Event Space of Zero Basis Pairs Is Empty

Define the event set of zero basis-pair products of order n by
Zn = {(i, j) : ei ej = 0}.
Theorem 4.1 directly gives Zn = ∅ for all n ≥ 0 and all primes p. Therefore, any counting
or density statistic supported on Zn , such as |Zn | or |Zn |/22n , is identically zero. Any
statistical conclusion claiming that zero basis pairs have positive density is incompatible
with Theorem 4.1. This conclusion is at the set level and does not depend on specific
sampling or numerical approximation.
Two logical levels must be distinguished. First, zero basis pairs do not exist, so density
analysis based on zero-basis-pair events is empty at the data level. Second, invertibility
of basis elements can independently verify that a single basis element is nonzero, but
it cannot imply that the product of two basis elements is still a single basis element.
The closure part of Theorem 4.1 must be supplied by the inductive proof in 4.4; the
nonvanishing part follows directly from the nonzero coefficients in the inductive proof.
The two cannot replace each other.
Two statistical populations must also be distinguished. This theorem excludes the
event that the product of an ordered pair (ei , ej ) of standard basis elements is zero; the
zero-divisor event for general element pairs (x, y) belongs to another population, is not
covered by the exclusion of this theorem, and zero divisors in that population do indeed
exist: for example, in characteristic 2, (1 + e1 )2 = 1 + 2e1 + e21 = 0; in characteristic 3, let
u = e1 +e2 ; then u2 = e21 +e1 e2 +e2 e1 +e22 = −1+0−1 = 1, so (1+u)(2+u) = 2+3u+u2 = 0.
Therefore “the set of zero basis pairs is empty” does not imply “there are no zero divisors
in the algebra”: any statistic supported on zero basis pairs is identically zero, while the
zero-divisor density statistic for general element pairs is an independent question that this
paper neither asserts nor excludes. Accordingly, any zero-divisor density assertion whose
statistical object is general element pairs cannot be directly refuted by this theorem, nor
can it be directly supported by this theorem.

4.6

Description of a Finite-Range Verification Algorithm

The following algorithm is used for exact consistency checks for finite n and finite p; it
uses no floating-point arithmetic and does not depend on external data sources.
Step one: construction of structure constants. Recursively construct the multiplication table of An by integer arithmetic according to the doubling formula. For each pair
of basis elements, compute the four blocks according to
(a, b)(c, d) = (ac − C(d)b, da + bC(c)),
16

## PDF page 17

obtaining integer structure constants. This step uses only integer addition, subtraction,
and sign changes.
Step two: reduction modulo p. Reduce the integer structure constants modulo the
target prime p, obtaining the multiplication table over Fp .
Step three: enumeration of basis pairs. Enumerate all ordered basis pairs (ei , ej ),
compute the product, and check whether the result is exactly of the form εek , where
ε ∈ {1, −1} and ek is a standard basis element. Also check whether εek is nonzero. The
complexity of this enumeration is O(22n ), suitable for full checks when n is small.
Step four: check of negative events. Count the number of basis pairs satisfying ei ej =
0, and verify that it is zero.
Step five: scope declaration. The above algorithm gives only machine certification for
finite n and finite p, and does not replace the general inductive proof in 4.4. Its role is to
check the implementation consistency of structure constants, conjugation signs, and the
doubled multiplication table within the certified range.

4.7

Conclusion, Boundaries, and Risk Statement

The conclusion rigorously proved in this chapter is: for any prime p and any n ≥ 0,
the standard basis of the Cayley–Dickson algebra An satisfies ei ej = εek , ε ∈ {1, −1},
and εek ̸= 0. Therefore the set of zero basis pairs is empty; according to the distinction
between the two statistical populations in 4.5, this exclusion concerns the population of
ordered pairs of standard basis elements, and any statistical conclusion with positivedensity support on zero basis pairs is false, while the zero-divisor density statistic for
general element pairs is an independent question that this chapter neither asserts nor
excludes.
Boundary cases include: when n = 0, there is only the unit basis element, and the
conclusion holds directly; when p = 2, the signs ± are not distinguished, but existence
and nonvanishing still hold; when i = 0 or j = 0, the product degenerates to another
basis element and is included in the four formulas; the product of basis elements in the
second copy involves conjugation, and conjugation only changes signs without changing
basis indices, which is the key to the induction step. The theorem holds for both odd
and even p, with no additional restriction needed.
Risks and limitations are as follows. First, the closure proof in this chapter depends
on the recursive definition of the standard basis and the doubled multiplication formula;
if a nonstandard basis is used, the conclusion should be stated as “the product of basis
elements is a signed multiple of a basis element”, and the sign structure may change.
Second, the finite-range verification algorithm covers only small n and does not constitute
a general proof; the general conclusion is borne by the inductive proof in 4.4. Third,
nonvanishing can be discussed independently using invertibility, but that route cannot
replace the closure proof; this chapter does not mistake nonvanishing for closure. Fourth,
this chapter does not involve any unverified literature conclusions or data sources; all
derivations are completed within the Cayley–Dickson construction and linear algebra
over prime fields.

17

## PDF page 18

5

Impossibility of a Cartan Doubling Recursion

5.1

Problem Framework and Notation

This chapter uses the notation and classification results of Chapter 3. Fp is the prime field,
An is the n-th Cayley–Dickson algebra, and EnvL (An ) is the unital subalgebra generated
by all left multiplication operators. For a finite-dimensional Fp -algebra Λ, take a complete
set of primitive orthogonal idempotents e1 , . . . , er , let Pi = Λei be the indecomposable
projective modules, and let Si be the unique simple head of Pi . The Cartan matrix C
is defined as the r × r matrix whose (i, j)-entry is the composition multiplicity of Si in
Pj . The cardinality r of a complete set of primitive orthogonal idempotents equals the
number of isomorphism classes of simple modules and does not depend on the specific
choice; different choices only lead to simultaneous permutation of rows and columns. The
matrix size r is invariant under simultaneous permutation.
This chapter considers the following formal block recursion: let Cn be the Cartan
matrix of EnvL (An ), of size rn × rn ; let X be an rn × rn matrix, and ∆n a 2rn × 2rn
matrix; the recursion asserts
(︃
)︃
Cn X
Cn+1 =
+ ∆n .
X T Cn
If the size of X is not rn × rn , or the size of ∆n is not 2rn × 2rn , then the block expression
has mismatched sizes and the equality is undefined. Therefore, under the premise that
the equality is defined, the right-hand side must have size 2rn × 2rn . This chapter uses
only matrix sizes, not the concrete entries of X, and not the concrete entries of ∆n ; the
condition of an “independent cross block” does not participate in the size argument.

5.2

Cartan Matrix Sizes Given by the Classification

By the classification theorem of Chapter 3 and its Cartan readings, for every prime p and
every n ≥ 1, the size rn of Cn satisfies:
First, when p is odd and n = 1, if −1 is a square modulo p, then EnvL (A1 ) ∼
= Fp × Fp ,
∼
2
C1 = I2 , and r1 = 2; if −1 is not a square modulo p, then EnvL (A1 ) = Fp , C1 = [1], and
r1 = 1.
Second, when p is odd and n ≥ 2, EnvL (An ) is a full matrix algebra, Cn = [1], and
rn = 1. Here the full matrix algebra is M2 (Fp ) for n = 2, and M2n (Fp ) for n ≥ 3; in both
cases the Cartan matrix is the 1 × 1 matrix [1].
Third, when p = 2, EnvL (An ) is a local algebra, Cn = [2n ], and rn = 1.
Therefore, for every n ≥ 1, rn belongs to {1, 2}; and for every n ≥ 1, rn+1 = 1. The
reason for the latter assertion is: n + 1 ≥ 2, and if p is odd then n + 1 ≥ 2 has already
entered the full matrix algebra case, with Cartan matrix [1]; if p = 2, the Cartan matrix
is [2n+1 ], still 1 × 1. Hence the size of the left-hand side Cn+1 is always 1.

5.3

Block Size Constraint

Assume that the recursion equality is defined in the block sense. Cn is rn × rn , X is
rn × rn , X T is rn × rn , and ∆n is 2rn × 2rn . The block matrix (with Cn at the upper left,
18

## PDF page 19

X at the upper right, X T at the lower left, and Cn at the lower right) has size 2rn × 2rn ;
after adding ∆n of the same size, the right-hand side is still 2rn × 2rn . The left-hand side
Cn+1 has size rn+1 . If the equality holds, one must have
rn+1 = 2rn .
This is a necessary condition for the equality to hold, and no matrix entries have yet
been checked. By 5.2, rn+1 = 1 for all n ≥ 1, while rn ≥ 1, so 2rn ≥ 2. Hence rn+1 = 2rn
cannot hold. Checking case by case: if rn = 1, the right-hand side has size 2 and the
left-hand side has size 1; if rn = 2, the right-hand side has size 4 and the left-hand side
has size 1. In both cases they are unequal.

5.4

Main Theorem

Theorem 5.1. Let p be any prime and n ≥ 1. There do not exist Cartan matrices Cn ,
Cn+1 satisfying the above block recursion, together with arbitrary X, ∆n , such that Cn
and Cn+1 are the Cartan matrices of EnvL (An ) and EnvL (An+1 ), respectively, and the
recursion equality is defined in the block sense.
Proof. By the classification in Chapter 3, the size of Cn+1 is rn+1 = 1. By the same
classification, the size rn of Cn belongs to {1, 2}. If the recursion equality is defined, then
the right-hand side has size 2rn and the left-hand side has size rn+1 . A necessary condition
for the equality to hold is rn+1 = 2rn . But rn+1 = 1, while 2rn ≥ 2, a contradiction.
Therefore no such Cn , Cn+1 , X, ∆n exist. This completes the proof.
The proof uses only the sizes of the Cartan matrices, not the independence of X, and
not the values of ∆n . Therefore, even if X or ∆n vary arbitrarily, as long as the block
sizes are legitimate, the equality already fails at the size level. If the sizes of X or ∆n
are not legitimate, then the recursion expression itself is not an equality of matrices of
the same size, and is even less valid. Under a change of the complete set of primitive
orthogonal idempotents, a Cartan matrix only undergoes simultaneous permutation of
rows and columns, and simultaneous permutation does not change the matrix size; hence
the conclusion does not depend on the choice of idempotents.

5.5

Item-by-Item Check of Boundary Cases

Case one: p is odd, n = 1, and −1 is a square modulo p. Then C1 = I2 , r1 = 2; C2 = [1],
r2 = 1. The right-hand side block size is 4 × 4, while the left-hand side is 1 × 1; they are
unequal.
Case two: p is odd, n = 1, and −1 is not a square modulo p. Then C1 = [1], r1 = 1;
C2 = [1], r2 = 1. The right-hand side block size is 2 × 2, while the left-hand side is 1 × 1;
they are unequal.
Case three: p = 2, n = 1. Then C1 = [2], r1 = 1; C2 = [4], r2 = 1. The right-hand
side block size is 2 × 2, while the left-hand side is 1 × 1; they are unequal.
Case four: n ≥ 2, p arbitrary. Then Cn is 1 × 1 and Cn+1 is 1 × 1; the right-hand side
block size is 2 × 2, while the left-hand side is 1 × 1; they are unequal.
The four cases cover all p and n ≥ 1, with no exception. In particular, p = 2 does not
need to be treated separately as a “vacuous case”; the size inequality excludes it directly.
The split case n = 1 is the only case with rn = 2, where the right-hand side has size 4, a
larger discrepancy.
19

## PDF page 20

5.6

Description of a Finite-Range Exact Verification Algorithm

The following algorithm is used for exact consistency checks for finite n and finite p; it
uses no floating-point arithmetic and does not depend on external data sources. Its role
is limited to checking the implementation consistency of Cartan matrix sizes in small
ranges, and it does not replace the general proof in 5.4.
Step one: construct the integer multiplication table of An . Compute structure constants pair by pair according to the doubling formula, then reduce modulo the target
prime p.
Step two: construct the left multiplication matrices Lei , starting from the identity operator and these generators, and maintain a linear basis by Gaussian elimination modulo
p, obtaining a matrix representation of EnvL (An ).
Step three: compute the Jacobson radical, find a complete set of primitive orthogonal
idempotents, and obtain the number rn of simple module isomorphism classes; or read
rn directly from the classification in Chapter 3. The two routes should agree in small
ranges.
Step four: for each n ≥ 1, compare rn+1 with 2rn , and record whether they are equal.
By 5.2, all records are unequal.
Step five: scope declaration. The algorithm covers only finite n and finite p; the
general conclusion is borne by 5.4. The algorithm introduces no random sampling and
no external benchmark data; all operations are exact integer or finite-field operations.

5.7

Conclusion, Risks, and Limitations

The conclusion rigorously proved in this chapter is: for every prime p and every n ≥ 1,
the Cartan doubling recursion under consideration is impossible at the level of block
matrix size. The left-hand side Cn+1 is always 1 × 1, while the right-hand side is at least
2 × 2; simultaneous permutation of rows and columns cannot change the matrix size.
This conclusion does not depend on the independence of X, on the concrete values of
∆n , or on the size of n.
A distinction must be made between rigorous proof and finite verification. The proof
in 5.4 is rigorous and uses only the classification in Chapter 3 and the necessary condition
on matrix sizes. The algorithm in 5.6 provides only a consistency check in finite ranges
and does not constitute a general proof. A distinction must be made between “the
equality is defined” and “the equality holds”: if the sizes of X or ∆n do not match, the
recursion expression itself is illegitimate; if the sizes match, the size inequality directly
excludes the equality. A distinction must be made between the size of a Cartan matrix
and the values of Cartan entries: this chapter uses only sizes, not multiplicity values;
therefore whether the local-algebra Cartan entry is 2n or whether the full matrix algebra
Cartan matrix is [1] does not affect the size argument, but these values are provided by
the classification in Chapter 3, and the terminology is consistent with Chapter 3.
Potential limitations are as follows. If the recursion is interpreted as “some block
embedding of Cn+1 ” rather than as a matrix equality, then the size argument does not
apply; this chapter concerns the block equality. If one allows adjoining zero rows and zero
columns to change the size, the resulting matrix is no longer the Cartan matrix under
the same idempotent set; a Cartan matrix permits only simultaneous permutation of
rows and columns. If one changes the complete set of primitive orthogonal idempotents,
the matrix only undergoes simultaneous permutation and its size is unchanged, so the
20

## PDF page 21

conclusion is unaffected by the choice. Apart from these interpretive boundaries, the
conclusion of this chapter holds definitively under the stated definitions.

6

Machine Certificates and Finite-Range Verification

6.1

Positioning of the Certificates and General Constraints

This chapter records machine certificates used to check the key steps of Chapters 3–5.
All certificates perform only exact integer or modular arithmetic enumeration for finite
n and finite p; they use no floating-point arithmetic, do not depend on external data
sources, and do not replace general proofs. The general conclusions are borne by the
classification theorem of Chapter 3, the basis product closure theorem of Chapter 4, and
the exclusion theorem for the Cartan doubling recursion of Chapter 5; the role of the
machine certificates is to check the implementation consistency of structure constants,
block formulas, centralizers, closure dimensions, and Cartan readings within the certified
range.
The certification objects are divided into three classes. The first class is basis product
closure, that is, whether the ordered product of standard basis elements is still a signed
multiple of some standard basis element and nonzero. The second class is the closure
dimension of the left-multiplication envelope algebra, that is, the dimension of the subalgebra generated over Fp by the identity operator and all left multiplication generators.
The third class consists of identities used in the proofs of Chapter 3, including associator values, anticommutator values, doubled block formulas, squares of special generators,
and centralizers. Each class of certificates gives the input range, output table, and scope
declaration.

6.2

Certificate M5: Basis Product Closure

Certificate M5 certifies the basis product closure proposition of Chapter 4. The input
consists of 21 cases with n ≤ 7 and p ∈ {2, 3, 5}. The algorithm is as follows.
Step one: recursively construct the multiplication table of An by integer arithmetic
according to the Cayley–Dickson doubling formula. For each pair of basis elements,
compute the integer structure constants of the four blocks according to the doubling
formula.
Step two: reduce the integer structure constants modulo the target prime p, obtaining
the multiplication table over Fp .
Step three: enumerate all ordered basis pairs (ei , ej ), compute the product, check
whether the result is exactly a signed multiple of some standard basis element, and check
whether that multiple is nonzero.
Step four: count the number of basis pairs satisfying ei ej = 0.
The output table passes in all 21 cases: the product of every ordered basis pair is a
signed multiple of some standard basis element and is nonzero, and the number of zero
basis pairs is always zero. This output is consistent with the theorem of Chapter 4. It

21

## PDF page 22

should be emphasized that the enumeration range of M5 does not cover all n and all p;
the general closure and nonvanishing are given by the inductive proof of Chapter 4.

6.3

Certificate M7: Structure of the Left-Multiplication Envelope Algebra

Certificate M7 certifies the closure dimensions and characteristic-dependent side checks
in the classification of Chapter 3. The input consists of the eight cases (n, p) equal to
(1, 2), (1, 3), (2, 2), (2, 3), (3, 2), (3, 3), (4, 3), (4, 5). The algorithm is as follows.
Step one: construct the standard basis of An and the matrix representations of the
left multiplication operators Lei .
Step two: starting from the identity operator and these left multiplication generators, repeatedly take products and maintain a linear basis by Gaussian elimination
modulo p until the dimension stabilizes; the resulting dimension is the closure dimension
of EnvL (An ).
Step three: in characteristic 2, check commutativity of standard basis elements, check
whether the square of (1 + ei ) is zero, and check uniqueness of nonzero idempotents.
Step four: in odd characteristic, check consistency between the closure dimension and
the full endomorphism dimension.
The output table gives closure dimensions 2, 2, 4, 4, 8, 64, 256, 256, corresponding respectively to the eight cases above. This table is consistent with the classification of
Chapter 3 case by case. A boundary case must be explicitly explained: the closure dimension 4 of (2, 3) corresponds to EnvL (A2 ) ∼
= M2 (Fp ), which is the boundary case n = 2;
when p is odd and n ≥ 3, one enters the full endomorphism case, whose dimension is
the square of 2n , certified as 64, 256, 256 in (3, 3), (4, 3), (4, 5), respectively. Therefore the
jump between (2, 3) = 4 and (3, 3) = 64 is not a certificate gap, but a structural difference
between the boundary n = 2 and the full endomorphism case n ≥ 3.

6.4

Certificate M8: Proof-Payload Identities and a Negative
Certificate

Certificate M8 certifies identities used in the proofs of Chapter 3. The input and output
are as follows.
First, the associator on basis triples takes values in {0, ±2em }; the certification range
is n ≤ 5, p ∈ {3, 5}, and all pass. This result is used in the argument that the associator
vanishes in characteristic 2.
Second, the anticommutator on basis elements takes values in {0, ±2em }; the certification range is the same, and all pass. This result is used in the commutativity argument
in characteristic 2.
Third, the doubled block formula holds on all tested basis quadruples; the certification
range is n ≤ 3, and all pass. This result is used for the block representation of left
multiplication operators.
Fourth, the special generator Z = L(0,1) satisfies that the square of Z equals minus
the identity; all pass. This result is used for invertibility of Z.
Fifth, the diagonalization formula for doubled blocks, Qb Qb′ equals the diagonal block
(−Rb Rb̄′ , −Lb Lb̄′ ), all pass. This result is used for even words falling into the diagonal
22

## PDF page 23

part.
Sixth, the centralizer Z(An ) equals Fp ; by exhaustive centralizer computation, the
certification range is n ≤ 3, and all pass. This result serves as a finite-instance check of
the centrality fact of Chapter 3.
In addition, a candidate decoupling identity Qb Z − ZQb̄ equals the diagonal block
(0, Rb − Lb ) fails under exact enumeration; its left-hand side is identically zero. This
negative certificate is retained in the audit chain to show that this route cannot be used
for the induction. The induction in Chapter 3 is completed by the subdirect product
dichotomy and the graph argument and does not depend on this decoupling identity.
Negative certificates have the same audit status as positive certificates: they record an
excluded intermediate step, making the choices in the proof chain traceable.

6.5

Joint Reproduction and Algorithmic Workflow

M5 and M7 are jointly reproduced in a single re-execution of the same self-contained session: one script simultaneously constructs multiplication tables, enumerates basis pairs,
constructs left multiplication matrices, maintains linear bases, and regenerates both pass
tables. This joint record serves as a reproducible anchor, avoiding version drift between
separate scripts. The reproduction process uses no random sampling, no external benchmark data, and all operations are exact integer or finite-field operations.
The algorithmic workflow can be summarized as: construction of structure constants,
reduction modulo p, enumeration of basis pairs, construction of left multiplication matrices, maintenance of linear bases, reading of closure dimensions, side checks, and scope
declaration. In terms of complexity, enumeration of basis pairs is on the order of the
square of the number of basis elements, suitable for full checks when n is small; construction of left multiplication matrices and maintenance of linear bases are finite-dimensional
linear algebra operations whose scale is determined by the dimension of An . The above
algorithm provides only consistency checks in finite ranges and does not constitute a
general proof.

6.6

Scope, Boundaries, and Risks

The determinate content of the certificates in this chapter is: within the listed finite
ranges of n and p, basis product closure, closure dimensions, block formulas, squares of
special generators, centralizers, and Cartan readings are all consistent with the theorems
of Chapters 3–5. The certificates do not cover all n and all p; the general conclusions are
borne by the proofs in the respective chapters. The centralizer certification of M8 only
goes up to n ≤ 3; the general proof of centrality is given by the lemma in Chapter 3.
The value (2, 3) = 4 of M7 is the boundary case n = 2 and cannot be directly compared
with the full endomorphism dimensions for n ≥ 3; this boundary has been made an
independent item in the classification of Chapter 3.
Risks and limitations include: if the standard basis or the complete set of primitive
orthogonal idempotents is changed, the numerical representation may change, but the
classification conclusions and the sizes of Cartan matrices under simultaneous permutation of rows and columns are unchanged; the certificates do not involve external literature
or data sources, and all derivations and verifications are completed within the Cayley–
Dickson construction and linear algebra over prime fields; negative certificates only show
23

## PDF page 24

that a certain candidate route is infeasible and do not constitute a replacement for the
general proof of Chapter 3. The conclusion of this chapter is: machine certificates support the payload steps of Chapters 3–5 within finite ranges, and their scope declarations
are clearly separated from the boundaries of the general proofs.

7

Logical Relation to Existing Work

7.1

Comparison Framework

This chapter does not organize its relation to existing work by literature chronology or
by author group, but by three logical levels: the object domain (over which base field and
for which algebra), the structural goal (which aspect of the algebra is studied), and the
method type (a general framework or a classification theorem). These three levels jointly
determine whether a piece of work is compatible with, orthogonal to, or incompatible
with the conclusions of this chapter.

7.2

Characteristic Theory and Annihilator Studies over the Real
Field

Literature verification confirms the actual existence and basic positioning of the comparison objects: the annihilator study of Biss–Dugger–Isaksen was published in Comm.
Algebra 36 (2008), and the characteristic theory of Biss–Christensen–Dugger–Isaksen was
published in Forum Math. 21 (2009), both working over the real field; the zero-divisor
graph framework of Anderson–Livingston is for commutative rings and was published
in J. Algebra 217 (1999); Schafer’s 1966 monograph established the general framework
of multiplication algebras of nonassociative algebras. Based on these verifiable coordinates, this chapter develops the relation according to logical relations rather than citation
format.
Biss, Dugger, and Isaksen studied upper bounds for the annihilator dimensions of
elements in real Cayley–Dickson algebras in Comm. Algebra 36 (2008); the core conclusion is that in a 2n -dimensional Cayley–Dickson algebra, the annihilator dimension of
any element is at most 2n − 4n + 4. Biss, Christensen, Dugger, and Isaksen subsequently
systematized eigenvalue theory in Forum Math. 21 (2009) to clarify several algebraic
properties of Cayley–Dickson algebras. The common premise of these two works is that
the base field is the real field R, the core tool is real linear algebra of eigenvalues and
eigenvectors, and the object of study is the spectral property of a single element or a
single operator.
The object of this chapter is the left-multiplication envelope algebra over the finite
field Fp , the goal is its Wedderburn structural classification (local algebra, full matrix
algebra, or a direct product of fields), and the tools are the subdirect product dichotomy,
the Skolem–Noether theorem, and centrality. The two differ in object domain (R versus
Fp ), in structural goal (spectral properties versus Wedderburn decomposition), and in
method type (real-analytic linear algebra versus finite-field algebraic structure). Therefore, conclusions of real-field characteristic theory cannot be directly transferred to the
24

## PDF page 25

classification of envelope algebras over Fp ; conversely, the classification of this chapter
does not assert anything about eigenvalue distributions over the real field. They are
parallel structural studies, each valid within its own domain.
A boundary must be made explicit: every nondegenerate quadratic form in at least
3 variables over a finite field is isotropic; this is the standard fact on which this chapter
relies at n = 2 to identify A2 with M2 (Fp ). Over the real field the quaternion algebra
does not split, because its norm form is positive definite; this difference is a property
of the field, not a difference in algebraic construction. Therefore, any reasoning that
directly analogizes nonsplitness over the real field with splitness over a finite field fails;
the classification of this chapter explicitly takes the base field as a parameter.

7.3

Commutative-Ring Zero-Divisor Graph Framework and Noncommutative Basis Product Closure

Anderson and Livingston introduced the zero-divisor graph of a commutative ring in J.
Algebra 217 (1999): the vertices are nonzero zero divisors, and edges connect distinct
vertices whose product is zero. The algebraic premise of this framework is multiplicative
commutativity, and the graph-theoretic premise is the existence of zero divisors.
The basis product closure theorem proved in Chapter 4 of this chapter gives a stronger
structural fact: in the standard basis of the Cayley–Dickson algebra An , for every prime p
and every n ≥ 0, the product of any two basis elements is a signed multiple of some basis
element and is nonzero. Therefore the set of zero basis pairs is empty. This means that,
even if the definition of a zero-divisor graph is transferred from commutative rings to
nonassociative Cayley–Dickson algebras, its vertex set is already empty at the standard
basis level; any density statistic supported on zero basis pairs is identically zero.
The relation here is not “this chapter refutes zero-divisor graph theory”—the latter
is completely valid for commutative rings—but rather “the applicability conditions of
the zero-divisor graph framework are not satisfied on the noncommutative nonassociative
Cayley–Dickson basis, and the manner in which they fail is extreme: it is not that
zero divisors are rare, but that zero basis pairs do not exist at all”. This distinction
is necessary to avoid overclaiming. This chapter does not assert that any conclusion
of Anderson–Livingston is wrong; what this chapter asserts is that transplanting zerodivisor-graph-style density analysis without conditions to Cayley–Dickson basis products
has no object at the data level.

7.4

General Framework of Multiplication Algebras and Concrete Classification

In his 1966 monograph, Schafer systematically defined the associative multiplication algebra and the Lie multiplication algebra of a nonassociative algebra, and used multiplication algebras as a tool for studying the structure of nonassociative algebras. This is a
general framework: it defines objects and gives basic properties, but does not provide a
Wedderburn classification for a specific family of algebras.
The left-multiplication envelope algebra EnvL (An ) of this chapter is a specialization
of Schafer’s associative multiplication algebra to the family of Cayley–Dickson algebras.
The contribution of this chapter is not to redefine multiplication algebras, but to complete
25

## PDF page 26

three concrete tasks within this framework. First, for p = 2, identify An with the group
algebra F2 [(C2 )n ], and give its local structure and Cartan matrix. Second, for odd p,
classify case by case in n: n = 1 gives a split or nonsplit quadratic algebra, n = 2 gives
M2 (Fp ) and the left regular representation gives an isomorphism, and n ≥ 3 gives the full
endomorphism algebra End(An ). Third, on the basis of the above classification, exclude
the possibility of a Cartan doubling recursion at the matrix-size level. None of these three
tasks is a direct corollary of Schafer’s general framework, because the general framework
does not contain arithmetic information for a specific base field and a specific doubling
tower.

7.5

Positioning at the Methodological Level

The combination of methods in this chapter has three separable features. First, the subdirect product dichotomy: using the simplicity of MN (Fp ), every subalgebra of MN ⊕ MN
with surjective projections is dichotomized into the full direct sum or the graph of
an automorphism. Second, the Skolem–Noether and “evaluation at 1” argument: the
graph assumption for an automorphism is converted into the form G = Rg−1 , which
then conflicts with La ̸= Ra . Third, the separation of the first step n = 2 → 3 from
the general induction: at n = 2, associativity and central simplicity of A2 are used
to obtain span{La Rc } = End(A2 ); for n ≥ 3, all P -words rather than only quadratic
left-multiplication words are used to complete surjectivity of the projections. This combination has not appeared in this form in the existing literature.
The novelty claim should be limited to the structural classification itself and should
not be extended to “the first study of multiplication algebras of Cayley–Dickson algebras”.
Schafer’s framework already established multiplication algebras as an object of study;
the novelty of this chapter is that it gives a complete Wedderburn classification of the
left-multiplication envelope algebra of the doubling tower over finite fields, and thereby
excludes a specific form of Cartan recursion. The identification of An with F2 [(C2 )n ] in
characteristic 2 is a direct observation requiring no complicated tools, but it has not been
used in the literature as the starting point of a classification; this chapter uses it as the
structural basis of the p = 2 branch.

7.6

Boundaries and Risks

The relation of this chapter to existing work is a logical relation, not a priority claim.
Real-field characteristic theory, commutative-ring zero-divisor graphs, and the general
framework of multiplication algebras of nonassociative algebras are each valid within
their own domains; the conclusions of this chapter do not conflict with them, because
the object domain, structural goal, or algebraic premise differs. The only place where
incompatibility must be made explicit is: applying the density analysis of commutativering zero-divisor graphs directly to Cayley–Dickson basis products has no object under
the closure theorem of Chapter 4 of this chapter; analogizing nonsplitness over the real
field to finite fields fails under the classification of Chapter 3.
The risk lies in misreading “different frameworks” as “opposing conclusions”. This
chapter does not assert that the real-field conclusions of Biss et al. have counterparts over
Fp , nor does it assert that the graph-theoretic conclusions of Anderson–Livingston have
a direct generalization to noncommutative algebras. The risk also lies in overextending
26

## PDF page 27

“novelty”: the classification of this chapter is a concrete completion within a framework,
not the creation of the framework itself; the characteristic 2 identification is an elementary
observation, not a deep theorem. These qualifications have been explicitly stated in 7.4
and 7.5 and should not be omitted in subsequent citations.

8

Conclusion and Boundaries

8.1

Logical Structure of the Conclusions

The core conclusions of the paper consist of three mutually supporting propositions,
rather than being given directly by a single computation or a single certificate. The first is
the Wedderburn classification of the left-multiplication envelope algebra: in characteristic
2, the Cayley–Dickson algebra is commutative and associative, and the left-multiplication
envelope algebra is isomorphic to the algebra itself and is local; in odd characteristic,
n = 1 gives a split or nonsplit quadratic algebra, n = 2 gives M2 (Fp ), and n ≥ 3 gives the
full endomorphism algebra End(An ). The second is standard basis product closure: the
product of any two standard basis elements is still a signed multiple of some standard
basis element and is nonzero, so the set of zero basis pairs is empty. The third is the
exclusion of the Cartan doubling recursion: the block recursion under consideration is
impossible at the matrix-size level, for every prime p and every n ≥ 1.
The relation among these three propositions is: the first provides the sizes and structures of Cartan matrices; the second deprives any statistical conclusion with positivedensity support on zero basis pairs of its object; the third uses only the size information
given by the first and does not depend on the concrete values of cross blocks or correction
terms. Each of the three conclusions has an independent proof and does not form a circle.

8.2

Three Load-Bearing Facts in the Classification Conclusion

In the classification conclusion, n = 2 must be an independent item. A2 is a fourdimensional associative algebra; the left regular map a ↦→ La gives an isomorphism
from the left-multiplication envelope algebra to A2 , and A2 is isomorphic to M2 (Fp ).
Therefore EnvL (A2 ) is isomorphic to M2 (Fp ), of dimension 4. The full endomorphism
algebra End(A2 ) is M4 (Fp ), of dimension 16; the two cannot be confused. The dimension
jump between n = 2 and n ≥ 3 comes from a change in algebraic structure, not from a
certificate gap.
The Cartan matrix of the full matrix algebra Mm (Fp ) is the 1 × 1 matrix [1], not
the identity matrix Im . Reason: a full matrix algebra is semisimple, its unique simple
module is the natural module, its unique indecomposable projective module is isomorphic
to that simple module, and the Cartan multiplicity is 1. The Cartan matrix of a local
algebra is [2n ] or [1], whose entries are composition multiplicities, not dimensions; treating
dimensions as Cartan entries confuses two levels.
The surjectivity of the projections in the general induction for n ≥ 3 depends on
all even words involving only first-kind doubling generators, not merely quadratic leftmultiplication words. An is nonassociative for n ≥ 3, and long words cannot in general
27

## PDF page 28

be reduced to quadratic words; if only quadratic words are taken, one would incorrectly
require the algebra generated by La to be End(An ). The first step from n = 2 to n = 3
must be argued separately, using associativity and central simplicity of A2 to obtain that
the algebra spanned by La Rc is End(A2 ). This step cannot be replaced by the general
induction hypothesis.

8.3

Cartan Readings and Exclusion of the Recursion

In all cases of odd characteristic with n ≥ 2, the left-multiplication envelope algebra
is a full matrix algebra, and the Cartan matrix is [1]. In characteristic 2, the leftmultiplication envelope algebra is a local algebra, and the Cartan matrix is [2n ]. In the
split case of odd characteristic n = 1, the Cartan matrix is I2 ; in the nonsplit case it is
[1]. Therefore, for every n ≥ 1, the size of the Cartan matrix is at most 2, and the size
of Cn+1 is always 1.
If the block recursion under consideration is defined in the block sense, the right-hand
side is formed from two copies of Cn and has size 2rn × 2rn , while the left-hand side has
size rn+1 . By the classification, rn+1 = 1, while 2rn is at least 2, so the size equality cannot
hold. This exclusion checks no entries of cross blocks or correction terms and does not
depend on the independence of cross blocks; it uses only the necessary condition of matrix
size. Simultaneous permutation of rows and columns does not change the matrix size, so
the conclusion does not depend on the choice of a complete set of primitive orthogonal
idempotents.

8.4

Division of Labor between Finite-Range Verification and
General Proof

Exact enumeration certificates in finite ranges support the consistency of structure constants, block formulas, squares of special generators, centralizers, and closure dimensions
within the certified range. These certificates cover small n and small p, not all n and all
p. General closure is borne by the inductive proof, general classification by the subdirect
product dichotomy and the graph argument, and the exclusion of the recursion by the
matrix-size argument. The role of certificates is to check implementation consistency,
not to replace proofs; negative certificates record excluded intermediate routes, have the
same audit status as positive certificates, but do not constitute a replacement for the
general proof.

8.5

Boundaries, Risks, and Applicability Conditions

The conclusions that hold definitively are: under the stated definitions, the classification theorem, the basis product closure theorem, and the recursion exclusion theorem
all hold. Finite-range certificates provide only finite support. Boundaries that must be
distinguished include: n = 2 is an independent boundary case and cannot be merged
into the full endomorphism case n ≥ 3; when p = 2, signs degenerate, but existence and
nonvanishing still hold; the conclusion that zero basis pairs are empty concerns the statistical population of ordered pairs of standard basis elements, and the zero-divisor problem
for general element pairs is not covered by this conclusion (the distinction between the
28

## PDF page 29

two populations and explicit examples in characteristics 2 and 3 are given in Chapter
4, 4.5); nonassociativity means that long words cannot be reduced to quadratic words,
and surjectivity of the projections must use all first-kind even words; a Cartan matrix
permits only simultaneous permutation of rows and columns, and if adjoining zero rows
and zero columns is allowed, the result is no longer the Cartan matrix under the same
idempotent set; the recursion exclusion concerns the block matrix equality, and if the
recursion is interpreted as a block embedding rather than an equality, the size argument
does not apply.
Potential limitations lie in interpretive boundaries rather than internal contradictions
of the proof: the classification conclusion depends on standard facts such as isotropy
of nondegenerate quadratic forms over finite fields, the Skolem–Noether theorem, and
the structural map for central simple algebras; these facts are used as external standard
results in the proof and are not reproved in this chapter. The scope declarations of
machine certificates are clearly separated from the boundaries of the general proof; one
should not misread finite certification as a general proof, nor misread the general proof
as a purely formal derivation requiring no finite checks. Under the above conditions,
the conclusions of the paper are self-consistent and consistent with the terminology and
logical direction of each chapter.

Remark
The translation of this article was done by DeepSeek, and the mathematical modeling
and the literature review of this article were assisted by DeepSeek.

References
[1] Schafer, Richard D. 1966. An Introduction to Nonassociative Algebras. New York:
Academic Press.
[2] Biss, Daniel K., Daniel Dugger, and Daniel C. Isaksen. 2008. “Large Annihilators in
Cayley–Dickson Algebras.” Communications in Algebra 36 (2): 632–664.
[3] Biss, Daniel K., J. Daniel Christensen, Daniel Dugger, and Daniel C. Isaksen. 2009.
“Eigentheory of Cayley–Dickson Algebras.” Forum Mathematicum 21 (5): 833–851.
[4] Anderson, David F., and Philip S. Livingston. 1999. “The Zero-Divisor Graph of a
Commutative Ring.” Journal of Algebra 217 (2): 434–447.
[5] Kleinfeld, Erwin. 1951. “Alternative Division Rings of Characteristic 2.” Proceedings
of the National Academy of Sciences 37 (12): 818–820.
[6] Bruck, Richard H., and Erwin Kleinfeld. 1951. “The Structure of Alternative Division
Rings.” Proceedings of the National Academy of Sciences 37 (2): 88–90.

29

## PDF page 30

[7] Eakin, Paul, and Avinash Sathaye. 1990. “On Automorphisms and Derivations of
Cayley–Dickson Algebras.” Journal of Algebra 129 (2): 263–278.
[8] Flaut, Cristina, and Geanina Zaharia. 2022. “Remarks Regarding Computational
Aspects in Algebras Obtained by Cayley–Dickson Process and Some of Their Applications.” Mathematics 10 (7): 1141.
[9] Pchelintsev, Sergey V. 2020. “Isotopes of Alternative Algebras of Characteristic Different from 3.” Izvestiya: Mathematics 84 (5): 1002–1015.
[10] Flaut, Cristina, and Remus Boboescu. 2021. “A Twisted Group Algebra Structure
for an Algebra Obtained by the Cayley–Dickson Process.” arXiv:2103.12805.
[11] Flaut, Cristina, and Andreea Baias. 2024. “Some Remarks Regarding Special Elements in Algebras Obtained by the Cayley–Dickson Process over Zp .” Axioms 13
(6): 351.
[12] Zhou, C., and Z. Zhou. 2026. The Wedderburn Classification of Left Multiplication
Enveloping Algebras of Cayley–Dickson Algebras in Characteristic p, and a Refutation of the Cartan Doubling Recursion (audit-reconstruction draft v3; machine
certificates M5, M7, M8). Companion audit note to the present paper.
[13] Zhou, Changzheng, and Zhou Ziqing. 2026a. Post Constraint Network E: The Observer as a Sub-structure of Constraint Networks—From the Measurement Problem to the Self-Referential Universe. Zenodo. https://doi.org/10.5281/zenodo.
20352585.
[14] Zhou, Changzheng, and Zhou Ziqing. 2026b. Post-Cybernetics E: Recursive Depth
of Meta-control—Constraint Network Allocation of Control Rights and Finiteness.
Zenodo. https://doi.org/10.5281/zenodo.20338286.
[15] Zhou, Changzheng, and Zhou Ziqing. 2026c. Post Cybernetics F: The Normative Topology of Constraint Networks—Identification of Dominant Structures and
the Criterion of Exitable Rights. Zenodo. https://doi.org/10.5281/zenodo.
20339847.
[16] Zhou, Changzheng, and Zhou Ziqing. 2026d. Post Game Theory G: Post Mechanism Design: Engineering of Belief Ecosystems. Zenodo. https://doi.org/10.
5281/zenodo.19618215.
[17] Zhou, Changzheng, and Zhou Ziqing. 2026e. Post Game Theory E: Structurally
Evolutionary Equilibrium—A New Solution Concept for Open Games. Zenodo.
https://doi.org/10.5281/zenodo.19602814.
[18] Zhou, Changzheng, and Zhou Ziqing. 2026f. Post Fourier G: From Adaptive Atom Library to Cognitive Architecture—Structural Openness of Signal Representation and
Its Neural Implementation. Zenodo. https://doi.org/10.5281/zenodo.19656256.
[19] Zhou, Changzheng, and Zhou Ziqing. 2026g. Post Information Theory Paradigm I:
Quantum Gravity, Cognitive Topology, and the Holographic Principle of Information. Zenodo. https://doi.org/10.5281/zenodo.19702294.

30

## PDF page 31

[20] Zhou, Changzheng, and Zhou Ziqing. 2026h. Observer Geometry: Schrödinger’s Cat
and the Many-Worlds Interpretation. Zenodo. https://doi.org/10.5281/zenodo.
18855141.
[21] Zhou, Changzheng, and Zhou Ziqing. 2026i. Post Bayesian K: An Evolvable Cognitive Architecture for Open Environments: Prototype Implementation and Experimental Evaluation of Constraint Network Reconfiguration. Zenodo. https:
//doi.org/10.5281/zenodo.19562929.
[22] Zhou, Changzheng, and Zhou Ziqing. 2026j. Post Bayesian L: A Dual-Mode Cognitive Architecture: Synergistic Mechanisms of Parameter Inference and Structural
Revision. Zenodo. https://doi.org/10.5281/zenodo.19583445.
[23] Zhou, Changzheng, and Zhou Ziqing. 2026k. Post Bayesian M: Dynamics of Cognitive Structural Openness and Subjective Phase Transitions. Zenodo. https://doi.
org/10.5281/zenodo.19583507.
[24] Zhou, Changzheng, and Zhou Ziqing. 2026l. Post Monte Carlo I: A Self-Normalized
Central Limit Theorem for Quasi-Stationary Adaptive Chains. Zenodo. https://
doi.org/10.5281/zenodo.19755279.
[25] Zhou, Changzheng, and Zhou Ziqing. 2026m. Post Markovian Paradigm 0: How
Boundary Structure Evolution of Markov Systems Leads to Essential Non-Ergodicity.
Zenodo. https://doi.org/10.5281/zenodo.19491459.
[26] Zhou, Changzheng, and Zhou Ziqing. 2026n. Post Monte Carlo J: Theoretical Boundaries and Open Frontiers of the Post Monte Carlo Paradigm. Zenodo. https:
//doi.org/10.5281/zenodo.19763430.
[27] Zhou, Changzheng, and Zhou Ziqing. 2026o. Post Decentralization I: Theoretical
Boundaries and Future of Post Decentralization—From Protocol Evolution to the
Digital Polis. Zenodo. https://doi.org/10.5281/zenodo.19818373.
[28] Zhou, Changzheng, and Zhou Ziqing. 2026p. Post Complex Systems K: Failure
Boundaries of Constraint Network Theory and the Geometric-Algebraic Unification of Complex Adaptive Systems. Zenodo. https://doi.org/10.5281/zenodo.
19948113.
[29] Zhou, Changzheng, and Zhou Ziqing. 2026q. Observer Geometry I: Morita Equivalence and Classification Theory of Observer Algebras. Zenodo. https://doi.org/
10.5281/zenodo.18801446.
[30] Zhou, Changzheng, and Zhou Ziqing. 2026r. The Ladder of Rules M: Rules
Above Rules—An Open Research Programme and Philosophical Reflections. Zenodo. https://doi.org/10.5281/zenodo.20388555.
[31] Zhou, Changzheng, and Zhou Ziqing. 2026s. The Ladder of Depth Structure G: Consensus, Spectral Gaps, and Rule Islands—Joint Algebraic and Topological Criteria
for Multi-Agent Systems. Zenodo. https://doi.org/10.5281/zenodo.20534826.
[32] Zhou, Changzheng, and Zhou Ziqing. 2026t. Constraint Network and Anomaly Suppression Series G: Proof Complexity, Automated Theorem Proving, and Rewiring
Operators. Zenodo. https://doi.org/10.5281/zenodo.20565346.
31

## PDF page 32

[33] Zhou, Changzheng, and Zhou Ziqing. 2026u. The Ladder of Constraint S: Constraint
Network Theory—A Meta-Mathematical Structure of Interpretive Frameworks and
Proof Boundaries. Zenodo. https://doi.org/10.5281/zenodo.20661441.
[34] Zhou, Changzheng, and Zhou Ziqing. 2026v. Constraint Networks and the McKay
Conjecture K: From the McKay Conjecture to the Meta-Mathematical Framework
of Cayley–Dickson. Zenodo. https://doi.org/10.5281/zenodo.20687494.
[35] Zhou, Changzheng, and Zhou Ziqing. 2026w. AWC Conjecture A: Local-Global Projective Module Conservation and Topological Weight Module Interpretation. Zenodo.
https://doi.org/10.5281/zenodo.20790412.
[36] Zhou, Changzheng, and Zhou Ziqing. 2026x. AWC Conjecture B: Projective Module
Conservation on p-Local Algebras and Rigid Core Condensation. Zenodo. https:
//doi.org/10.5281/zenodo.20794324.
[37] Zhou, Changzheng, and Zhou Ziqing. 2026y. AWC Conjecture C: Abelian Defect
Groups and Projective Module Zero Height Theorem. Zenodo. https://doi.org/
10.5281/zenodo.20805397.
[38] Zhou, Changzheng, and Zhou Ziqing. 2026z. AWC Conjecture D: Local-Global Conservation of p-Modular Algebras under Exceptional Lie Group Actions. Zenodo.
https://doi.org/10.5281/zenodo.20807447.
[39] Zhou, Changzheng, and Zhou Ziqing. 2026aa. AWC Conjecture E: Equivalence Law
Between Weight Configurations and Module Counts in Constraint Network Blocks.
Zenodo. https://doi.org/10.5281/zenodo.20809548.
[40] Zhou, Changzheng, and Zhou Ziqing. 2026ab. AWC Conjecture F: Cartan Matrix
Percolation and Representation Type Phase Transitions in Block Algebra Constraint
Networks. Zenodo. https://doi.org/10.5281/zenodo.20810998.
[41] Zhou, Changzheng, and Zhou Ziqing. 2026ac. AWC Conjecture G: Local-Global
Locking Law of p-Modules Under Exceptional Lie Group Actions. Zenodo. https:
//doi.org/10.5281/zenodo.20822629.
[42] Zhou, Changzheng, and Zhou Ziqing. 2026. AWC Conjecture K: From Alperin
Weights to the Meta-Mathematical Framework of Dade–Broué. Zenodo. https:
//doi.org/10.5281/zenodo.20838062.
[43] Zhou, Changzheng, and Zhou Ziqing. 2026. AWC Conjecture F: Cartan Matrix Percolation and Representation Type Phase Transitions in Block Algebra Constraint
Networks. Zenodo. https://doi.org/10.5281/zenodo.23913738.
[44] Zhou, Changzheng, and Zhou Ziqing. 2026. AWC Conjecture I: Arithmetic LocalGlobal Conservation on Non-Associative p-Modular Algebras. Zenodo. https://
doi.org/10.5281/zenodo.23916710.
[45] Zhou, Changzheng, and Zhou Ziqing. 2026. AWC Conjecture J: Recursive Structure of High-Dimensional p-Modular Algebras and Projective Information Doubling.
Zenodo. https://doi.org/10.5281/zenodo.23937612.

32

## PDF page 33

Appendix A: Machine Certificate Ledger
A.1 Record Format and Audit Rules
Each certificate is recorded according to six elements: tool (computational environment and arithmetic type), command (operational semantics of the self-contained session script), input (list of cases), output (pass table), log (session record), and judgment
(which step of which proposition the certificate supports). The ledger follows two rules.
First, negative assertions and positive assertions are treated equally: asserting that a
quantity is identically zero must be supported by full enumeration, with the same enumeration strength as asserting that a quantity is nonzero. Second, excluded intermediate
steps are retained as negative certificates rather than deleted; the ledger records which
route is infeasible, why it is infeasible, and which alternative route accomplished the same
goal, so that the choices in the proof chain can be traced level by level.

A.2 Certificate M5: Standard Basis Product Closure
Tool. Exact integer arithmetic and modular arithmetic; no floating-point arithmetic
appears in the evidence chain; integer overflow boundaries are recorded at array accumulation points.
Command. Recursively construct the multiplication table of An over the integers according to the Cayley–Dickson doubling formula; reduce each structure constant modulo
the prime in the case list; enumerate all ordered basis pairs; compare each product with
signed multiples of standard basis elements and with zero.
Input. n ≤ 7, p ∈ {2, 3, 5}, 21 cases in total.
Output. All pass: the product of every ordered basis pair is a signed multiple of some
standard basis element and is nonzero; in all 21 cases the number of zero basis pairs is
zero.
Judgment. Supports instances of the basis product closure theorem of Chapter 4
within the certified range; the emptiness of the set of zero basis pairs is a direct corollary
of that theorem.

A.3 Certificate M7: Closure Dimension of the Left-Multiplication
Envelope Algebra
Tool. Same as A.2.
Command. Construct the standard basis and left multiplication operator matrices;
starting from the identity operator and all left multiplication generators, repeatedly take
products and maintain a linear basis by Gaussian elimination modulo p until the dimension stabilizes; in characteristic 2, check commutativity of the standard basis, check
whether the square of the identity plus a basis element is zero, and check uniqueness of
nonzero idempotents; in odd characteristic, check consistency between the closure dimension and the full endomorphism dimension.
Input. (n, p) equal to (1, 2), (1, 3), (2, 2), (2, 3), (3, 2), (3, 3), (4, 3), (4, 5).
Output. The closure dimensions are 2, 2, 4, 4, 8, 64, 256, 256 in order; all side checks in
characteristic 2 and odd characteristic pass.
33

## PDF page 34

Judgment. Consistent with the classification of Chapter 3 case by case. The boundary
must be explicitly stated: the closure dimension 4 of (2, 3) corresponds to EnvL (A2 ) ∼
=
M2 (Fp ), which is the boundary case n = 2; when p is odd and n ≥ 3, one enters the
full endomorphism case, whose dimension is the square of 2n , certified as 64, 256, 256 in
(3, 3), (4, 3), (4, 5), respectively. Therefore the jump between (2, 3) = 4 and (3, 3) = 64
is a structural difference between the boundary n = 2 and the full endomorphism case
n ≥ 3, not a certificate gap.

A.4 Certificate M8: Proof-Payload Identities and a Negative Certificate
Tool. Same as A.2.
Command. Item-by-item identity checking scripts; each item is evaluated on all basis
elements or tuples of basis elements and compared with the declared value.
Input and output. First, the associator on basis triples takes values in {0, ±2em },
n ≤ 5, p ∈ {3, 5}, pass. Second, the anticommutator on basis elements takes values
in {0, ±2em }, same range, pass. Third, the doubled block formula holds on all tested
basis quadruples, n ≤ 3, pass. Fourth, the special generator Z = L(0,1) satisfies that
the square of Z equals minus the identity, pass. Fifth, the diagonalization formula for
doubled blocks holds on all tested basis pairs, pass. Sixth, the centralizer equals Fp , by
exhaustive centralizer computation, n ≤ 3, pass.
Judgment. The fourth and fifth items support the invertibility of the special generator
and the step that even words fall into the diagonal part in the graph argument of Chapter
3; the sixth item serves as a finite-instance check of the centrality fact of Chapter 3; the
first, second, and third items support the characteristic 2 branch and the doubled block
representation.

A.5 Negative Certificate: A Candidate Decoupling Identity
A candidate decoupling identity asserts that the difference of two specific operators equals
a certain diagonal block. Exact enumeration returns that the left-hand side is identically
zero on all test inputs, so the identity does not hold. The root cause is improper use
of the direction of the conjugation identity; after substituting in the correct direction,
the two terms cancel. This negative certificate is retained in the ledger to show that
this route cannot be used for the induction; the induction in Chapter 3 is completed by
the subdirect product dichotomy and the graph argument and does not depend on this
identity. Negative certificates have the same audit status as positive certificates: they
record an excluded intermediate step, making the choices in the proof chain traceable.

A.6 Joint Reproduction and Scope Declaration
M5 and M7 are jointly reproduced in a single re-execution of the same self-contained session: one script simultaneously constructs multiplication tables, enumerates basis pairs,
constructs left multiplication matrices, maintains linear bases, and regenerates both pass
tables. The joint record serves as a reproducible anchor, avoiding version drift between

34

## PDF page 35

separate scripts. The reproduction process uses no random sampling, no external benchmark data, and all operations are exact integer or finite-field operations. The reproduction script and session records are not published with the manuscript; the command
elements of each certificate have been fully given in operational semantics, and an independent implementation should regenerate the same pass tables; the original script can
be requested from the author if needed.
Scope declaration. The above certificates cover only finite n and finite p, and do
not constitute a general proof; the general conclusions are borne by the classification
theorem of Chapter 3, the basis product closure theorem of Chapter 4, and the recursion
exclusion theorem of Chapter 5. The role of the certificates is to check the implementation
consistency of structure constants, block formulas, centralizers, closure dimensions, and
Cartan readings within the certified range. The centralizer certification only goes up to
n ≤ 3; the general proof of centrality is given by the lemma in Chapter 3.

Appendix B: Registry of Refutation Targets
B.1 Function and Rules of the Registry
The strength of a refutation depends on the precision of its target. If a target is only
approximately described, the refutation can be avoided by moving the target; if the target
is fixed verbatim, the falsification chain can be recomputed line by line. Therefore this
appendix registers verbatim and by coordinate every assertion excluded by Chapters 4
and 5, and gives a one-to-one mapping from registered targets to exclusion theorems.
Registration follows two rules. First, every target must be given with a verbatim
source sentence and coordinates; slots that cannot be located verbatim remain to be
filled and are not filled with paraphrases. Second, target registration is at the sentence
level, not the text level; this appendix makes no assertion about other content of the
source text.

B.2 Registered Targets
T-1. The source sentence asserts that the density of zero basis pairs is 63/256; coordinates
to be filled. Excluded by the basis product closure theorem of Chapter 4: there are no
zero basis pairs in the standard basis, and this density is identically zero.
T-2. The source sentence asserts that the density of zero basis pairs is 64/256; coordinates to be filled. Exclusion is the same as above.
T-3. The source sentence asserts that the count or density of zero basis pairs is
116/240; coordinates to be filled. Exclusion is the same as above.
T-4. The source sentence asserts that the density of zero basis pairs is 0.248; coordinates to be filled. Exclusion is the same as above.
T-5. The source sentence asserts that the Cartan matrix satisfies a block recursion:
the left-hand side is the next-order Cartan matrix, the right-hand side is the block concatenation of two current-order Cartan matrices plus a correction term, and the cross
block is declared independent. The recursion is declared to be a structural recursion on
the doubling tower, not a coordinate accident. Excluded by Chapter 5: for every prime
p and every n ≥ 1, the left-hand side Cartan matrix has size 1, while the right-hand
35

## PDF page 36

side is formed from two current-order Cartan matrices and has size at least 2; the block
equality is impossible at the matrix-size level. Simultaneous permutation of rows and
columns does not change the matrix size, so the exclusion does not depend on the choice
of a complete set of primitive orthogonal idempotents, nor does it check any entries of
cross blocks or correction terms.

B.3 Exclusion Mapping
The exclusion mechanism for T-1 through T-4 is the same: standard basis product closure
gives that the product of any two basis elements is a signed multiple of some basis
element and is nonzero; therefore the set of zero basis pairs is empty, and any statistic
with positive-density support on zero basis pairs is identically zero. This mechanism
uses only the closure and nonvanishing of Chapter 4, and no sampling or approximation.
According to the distinction between the two statistical populations in Chapter 4, 4.5, the
statistical object excluded by this mechanism is ordered pairs of standard basis elements;
if the statistical object of the source sentence is actually general element pairs rather than
standard basis pairs, then this mechanism does not cover that sentence, and a separate
analysis is required.
The exclusion mechanism for T-5 consists of two parts: the classification of Chapter
3 gives that the size of each Cartan matrix is at most 2 and the next-order size is always
1; Cartan matrices are invariant in size under simultaneous permutation of rows and
columns. Together these give a size inequality that excludes the block equality. This
mechanism does not depend on the independence assumption for cross blocks, nor on the
concrete values of correction terms.

B.4 Scope
This registry fixes five sentences. It makes no assertion about other content of the source
text; the exclusion is at the sentence level, not the text level. The coordinate slots of T-1
through T-4 are currently retained as registrations pending activation: activation requires
filling in the verbatim source sentences and coordinates and completing a one-to-one check
with the exclusion mechanism of Chapter 4; before that, these four registrations are in
a pending state and do not constitute completed verbatim refutations. The completed
verbatim refutation registration is T-5.
A distinction must be made between the activation status of a registration and the
validity status of a theorem. Regardless of whether coordinates are filled in, the emptiness
of the set of zero basis pairs holds independently by Theorem 4.1 of Chapter 4, and any
statistic with positive-density support on zero basis pairs is identically zero; this set-level
conclusion does not depend on any slot of this registry. The exclusion of T-5 likewise
does not depend on coordinate slots, because its mathematical content is independently
borne by the classification of Chapter 3 and the size argument of Chapter 5.

36

## PDF page 37

Appendix C: List of Claims
C1 Theorems Proved in This Paper
The classification theorem of Chapter 3: when p = 2, the left-multiplication envelope
algebra is isomorphic to An itself and is local; when p is odd and n = 1, it is a split or
nonsplit quadratic algebra; when n = 2, it is M2 (Fp ) and the left regular representation
gives an isomorphism; when n ≥ 3, it is the full endomorphism algebra.
The basis product closure theorem of Chapter 4: for every prime p and every n ≥ 0,
the product of standard basis elements is still a signed multiple of some standard basis
element and is nonzero.
The recursion exclusion theorem of Chapter 5: the Cartan doubling recursion under
consideration is impossible at the matrix-size level for every prime p and every n ≥ 1.
The proofs of these three theorems do not use machine input; machine certificates are
finite-range implementation consistency checks, not premises of the proofs.

C2 Machine Support Statements and Scope
M5 supports instances of the closure theorem of Chapter 4 in the range n ≤ 7, p ∈
{2, 3, 5}. M7 supports the closure dimensions and side checks of the classification of
Chapter 3 in the range of the eight listed pairs (n, p). The first through third items of
M8 support instances of the characteristic 2 branch and the doubled block representation
in finite ranges; the fourth and fifth items of M8 support the payload steps of the graph
argument of Chapter 3; the sixth item of M8 supports instances of the centrality fact
in the range n ≤ 3. The negative certificate supports the negative assertion that the
candidate decoupling route is infeasible.
Honest scope declaration: no certificate reaches n ≥ 5 or p ≥ 7. This boundary is
declared, not concealed. Certificates are endorsements within finite ranges, not general
proofs, and not gaps in the proof.

C3 External Standard Facts Cited
First, every nondegenerate quadratic form in at least 3 variables over a finite field is
isotropic; this is a standard corollary of the Chevalley–Warning theorem, used in the
n = 2 branch of Chapter 3.
Second, the Skolem–Noether theorem: every automorphism of a central simple algebra
is inner; used in the graph argument of Chapter 3.
Third, the natural structural map of a central simple algebra from the tensor product
to the endomorphism algebra is an isomorphism; used in the first step from n = 2 to
n = 3 in Chapter 3.
Fourth, the general framework of the associative multiplication algebra of a nonassociative algebra is given in Schafer’s 1966 monograph; the left-multiplication envelope
algebra of this paper is a specialization of this framework to the family of Cayley–Dickson
algebras.
Fifth, the study of annihilators and characteristic theory of real Cayley–Dickson algebras is given in the work of Biss–Dugger–Isaksen (2008) and Biss–Christensen–Dugger–
37

## PDF page 38

Isaksen (2009); their object domain is the real field, different from the finite-field object
domain of this paper.
Sixth, the zero-divisor graph framework for commutative rings is given in the work
of Anderson–Livingston (1999); its algebraic premise is multiplicative commutativity,
different from the noncommutative nonassociative structure of Cayley–Dickson algebras.
The above facts are used only as external standard results and are not reproved in
this paper.

C4 Non-Claims
This paper makes no assertion about the Alperin weight conjecture, the Brauer heightzero conjecture, the Dade conjecture, or the Broué conjecture; these names do not appear
in this paper as declared claims. This paper does not assert that conclusions of the characteristic theory of real Cayley–Dickson algebras have counterparts over finite fields; this
paper does not assert that conclusions of commutative-ring zero-divisor graphs have a
direct generalization to noncommutative algebras; this paper does not assert the novelty
of the general multiplication algebra framework itself. The classification of this paper
is a concrete completion within the framework, and the characteristic 2 identification is
an elementary observation, not a deep theorem. These qualifications have been explicitly stated in the corresponding places of the main text and should not be omitted in
subsequent citations.

38
