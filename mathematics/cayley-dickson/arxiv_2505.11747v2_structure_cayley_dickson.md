Source: https://arxiv.org/abs/2505.11747v2
PDF sha256: 815b797e690def4bd889ea30b17ecd715f3009ed60526a76ea9fd92f45aab7e2
License: http://creativecommons.org/licenses/by-nc-sa/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of arxiv_2505.11747v2_structure_cayley_dickson.pdf

Transcription of `arxiv_2505.11747v2_structure_cayley_dickson.pdf` in this directory, 25 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-25 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Structure of the Cayley-Dickson algebras
G. P. Wilmot
University of Adelaide, Australia

arXiv:2505.11747v2 [math.RA] 13 Oct 2025

Abstract
Viewing the Cayley-Dickson process as a graded construction provides a rigorous deﬁnition of associativity consisting of three types and the non-associative parts dividing into four
types. These simplify the Moufang loop identities and Mal’cev’s identity, which identiﬁes
the non-associative Lie algebra structure. Many authors have assumed the Moufang loop
identities are identical but this is not the case for sedenions. Analysing the non-associativity
structure uncovers 3-cycles that distinguish between the Moufang identities and are used to
identify three power-associative subalgebras of sedenions and higher level Cayley-Dickson
algebras.
Power-associativity introduces zero divisors into Cayley-Dickson algebras in a systematic
way and it is convenient to replace the terminology hypercomplex numbers with ultracomplex
numbers for the power-associative algebras. The non-associative types simplify the Moufang
identities and show that zero divisors in these algebras occur in multiples of 84. Modes are
uncovered that reduce these down to factors of seven base zero divisor pairs. It is shown
that this is due to the the power-associative subalgebras being embedded into ultracomplex
numbers in multiples of seven. The graded notation allows the eight octonion and seven
power-associative subalgebras of sedenions to be uniquely derived, up to representation.
Split Cayley-Dickson algebras are proved to be isomorphic to each other for any ultracomplex algebra and these share the same non-associative structure as the non-split case
but with diﬀerent zero divisors. These are provided for the split sedenions.
Keywords. Octonions, sedenions, Cayley-Dickson algebras, split sedenions, zero divisors,
graded algebras, Moufang loops, Malcev algebra, ultracomplex numbers.

1

Introduction

The standard approach to the Cayley-Dickson construction [5] at step n is to deﬁne a multiplication operation for An ∼
= An−1 ⊕ An−1 by
(a, b)(c, d) = (ac + ǫd∗ b, da + bc∗ ),
where the conjugate is (a, b)∗ = (a∗ , −b) and ǫ = 1 for the normed composition algebras analysed
by Hurwitz [6]. The products ac, d∗ b, da and bc∗ are deﬁned according to the construction for
An−1 ∼
= An−2 ⊕ An−2 , which in turn is eventually determined by elements in A0 = R.
Traditionally, the multiplication operator is introduced using anticommuting imaginaries i, j, l
for the complex numbers, quaternions and octonions, respectively, as
A1 = R ⊕ iR = C,
A2 = C ⊕ Cj = H and
A3 = H ⊕ lH = O.

(1)

This paper introduces a graded decomposition of anticommuting elements, on , at each level, n,
as
An = An−1 ⊕ An−1 on
so that o1 = i, o2 = j and o3 = −l. The ungraded notation of using k = ij is then represented
in graded form as ij = o12 . All elements of An are generated using the binomial expansion,
which provides an ordering of these elements. This is not important for the normed division
algebras and, for example, the exception Lie algebra G2, which are the automorphisms for
octonions. Swapping any pair of the seven elements of octonions generates another representation
of octonions. The ordering enables power-associativity but only comes into play for An with n ≥ 4
where A4 = S, the sedenions.
1

## PDF page 2

Deriving an ordering using the graded notation ﬁnds that power-associative algebras have
three types of associativity, which leads to four types of non-associativity. Octonions only have
one symmetric type of non-associativity that makes the three Moufang loop identities identical.
Sedenions introduce two more non-associative types, which separates two of the Moufang identities and allows for zero divisors. The trigintaduonions, A5 , include the ﬁnal non-associative
type, identiﬁed by the remaining Moufang identity giving unique results, which adds more complicated zero divisors. Using the new non-associative types provides a simpler categorisation
than the Moufang identities. Analysis of the new non-associative types uncovers cyclic forms
and modes that categorise zero divisors and applied to the 84 known sedenion zero divisors [7],
reduces them to seven distinct triples of basis elements with three cycles and four modes each.
The trigintaduonions have 1,260 zero-divisors, which are derived from 147 distinct triples. The
cyclic forms identify the octonion and three power-associative sub-algebras of A5 , called pseudooctonion algebras in [10]. Each of these algebras contain 12 zero divisors and since they are
embedded in An , n ≥ 4, in multiples of seven, then it is found that zero divisors in An , n > 3
occur in multiples of 84. The cardinality formula for zero divisors for all An is derived.
Using loop analysis, Cawagas [7] has previously identiﬁed the ﬁrst power-associative subalgebra by identifying that it did not satisfy one of the three Moufang identities, unlike octonions.
He called this quasi-octonions and provided an enumeration in [9]. This paper takes a diﬀerent
approach to loop analysis to prove that most of the sedenion triple products satisfy the three
Moufang identities in diﬀerent ways. Previous work [10] has shown that the quasi-octonions
are part of a series of six algebras, called pseudo-octonions to allow for the designation Pk ,
k ∈ {4, 8, 10, 12, 14, 16} where k is the number of distinct non-associative triple products. These
algebras where shown to break the symmetry of octonions in a way consistent with exceptional
Lie algebra G2. Cawagas found seven copies of P4 embedded in sedenions as well as eighth copies
of octonions. Another two of these power-associative algebras are introduced in the next two
levels of Cayley-Dickson algebras, A5 and A6 .
The octonions have been found to apply to areas in particle physics [11, 12] and extended
to sedenions more recently [13, 14, 15, 16]. It may not be necessary to go to higher dimensions
to achieve new representations in particle physics. All Cayley-Dickson algebras of dimension
higher than octonions consist of multiple copies of octonions and various pseudo-octonions so it
is possible that just octonions and the pseudo-octonion algebras are all that is necessary.
Section 2 starts by building the Cayley-Dickson construction as two equivalent pyramids
using graded and binary notations. Swapping between the two allows the usual composition
properties to be proved for all Cayley-Dickson algebras showing that the graded notation is indeed
equivalent to the usual doubling of algebras [8]. Section 3 derives the four non-associativity types
that simplify the Moufang identities and Malcev algebras and derives the eight non-associative
3-cycles and 3-cycle structure in the Cycle theorem that identiﬁes the subalgebras of An for
n ≥ 3. The 15 octonion and P4 representations embedded in sedenions are identiﬁed using the
graded notation.
Section 4 deﬁnes zero divisors and modes in the Mode theorem and shows the relationship to
the eight 3-cycles. It proceeds to document the seven and 147 prime zero divisors of A4 and A5 ,
respectively, and applies the Cycles and Modes theorems to uncover the rest. Section 5 shows
each Cayley-Dickson algebra has a single split version with the same non-associative structure
but diﬀerent zero divisors. These are provided for the split sedenions.

2

Graded Cayley-Dickson Construction

Deﬁnition. The basis of the Cayley-Dickson algebra (at)level n, called the ungraded dimension,
has 2n graded elements consisting of grades of size nk called a k-grade. Basis elements are
represented as oα where α is a set of digits from A(n) = {∅, (1), (12), . . . , (12 · · · n)}, generated
by the recurrence relation A(n) = A(n − 1) + A(n − 1)(n), where set multiplication by (n)
extends each member of the set by n, A(n − 1)(n) = {(n), (1n), (12n), . . . , (12 · · · (n − 1)n)}.
This operation is called expansion but multiplying by an existing member will contract some
members. Using the notation of Porteous [17] whereby Nn1 is the set of natural numbers from 1
up to and including n, then {(12 · · · n)}(k) = {(12 · · · (k − 1)(k + 1) · · · n)} for k ∈ N3n−1 . Note
that A(n) includes the empty set, ∅, or no digit case, to denote the unit graded element, 1, which
is the only graded element at level zero and the unit notation is preferred to the use of the empty
set, o = 1. The set brackets are dropped in the graded element, (α) → oα .

2

## PDF page 3

The graded recurrence relation is an example of the binomial theorem, which has the property
n ( )
∑
n
k=0

k

= 2n ,

(2)

and the basis has a binary expansion described by Pascal’s triangle. This provides a natural
ordering of the graded elements shown in the following graded element pyramid to level 3,
1
{1, o1 }
{1, o1 , o2 , o12 }
{1, o1 , o2 , o12 , o3 , o13 , o23 , o123 }.
Lemma 1. Any list of distinct graded elements multiplied together via set expansion and contraction generates another distinct graded element if the unit, 1, is excluded.
Proof. Set expansion and contraction of two distinct members of A(n) is the symmetric diﬀerence
or the union minus the intersection of the two groups of indices. This is diﬀerent to the initial
two members and this process can continue for any number of distinct graded elements as long
as the no digit case is not encountered. Each row of Pascal’s triangle of graded elements contains
an even number of each index, excluding level 1, because each index is doubled for the next level
of the recurrence relation and there are an even number of existing elements to double with the
new index. Hence, excluding the ﬁrst row, the multiplication of all elements of any row contracts
to α being the no digit case. Excluding such cases produces a distinct new graded element.
Deﬁnition. A k-grade contains graded elements oα where α has k indices called the length of
α. The k = 1 case is called a generator because all graded elements can be generated from these
by expansion and contraction. At level n these are o1 , o2 , · · · , on .
Deﬁnition. A pure element excludes the unit basis element, 1. A blade is a pure, non-zero,
scaled basis element and a k-blade is a member of the k-grade. Note that blades may have
positive or negative squares and for the remainder this assumed to be ±1, for blades. A blade is
positive or negative for scale +1 or -1, respectively.
The Cayley-Dickson construction uses pairs of scalars to represent the graded pyramid.
Deﬁnition. The pyramid element a, at level n, speciﬁes the nth row of a binary pyramid with
coeﬃcients aβ , β ∈ B(n), where B(n) = B(n − 1)(0) + B(n − 1)(1) so that B(n) is all binary
numbers with n digits from N10 and set multiplication extends the binary numbers in B(n − 1).
Hence B(n) covers all 2n combinations of n digits in A(n) and this is an equivalence relationship
to graded elements with coeﬃcients aβ = 0 or ±1 because appending a 1 to β at the nth position
is the same as appending n to the graded recurrence relation. Hence, at level 1, a0 = (±1, 0) = ±1
and a1 = (0, ±1) = ±o1 . To level three this is
a = (a0 , a1 )
= ((a00 , a10 ), (a01 , a11 ))

(3)

= (((a000 , a100 ), (a010 , a110 )), ((a001 , a101 ), (a011 , a111 ))).
The Cayley-Dickson process in pyramid form provides the same ordering as the graded elements with the last index corresponding to on , if it is 1. Some pyramid coeﬃcients at level 2
are β = ij, i, j ∈ N10 which corresponds to signed oβ = o1 , o2 , o12 for aij = a10 , a01 , a11 in (3),
respectively. The four extreme blades at level 3 are
±o1 = (((0, ±1), (0, 0)), ((0, 0), (0, 0))) and
±o123 = (((0, 0), (0, 0)), ((0, 0), (0, ±1))).
Deﬁnition. The Cayley-Dickson product at level i for two pure pyramid elements, aα bβ , with
α, β ∈ B(n), with αi being all indices to the left of position i and αi being all indices to the right
of position i, is
(aαi 0 αi , aαi 1 αi )(bβi 0βi , bβi 1βi ) =
)
(
aαi 0 αi bβi 0βi − ǫi b∗βi 1βi aαi 1 αi , bβi 1βi aαi 0 αi + aαi 1 αi b∗βi 0βi ,
3

(4)

## PDF page 4

where ǫi = ±1 for i ∈ Nn1 and the conjugate operator at level i is a∗α 0 = (a∗αi 0 αi , −aαi 1 αi ) and
the conjugate operator on the right hand side acts at level i − 1 and has no eﬀect at level 0.
Equation (4) corresponds to a section of the pyramid one pair deep at level i. The terms on the
right hand side of (4) are called the parallel and cross terms, respectively. The αi indices are not
shown if empty.
The construction uses Pascal’s recurrence relation to create a pyramid, n pairs deep, whereby
the ﬁrst division repeats the structure on of the left half on the right but multiplied by on . For
n = 1, so that α, β ∈ B(0), the no index case, then
(a0 , a1 )(b0 , b1 ) = (a0 b0 − ǫ1 b1 a1 , b1 a0 + a1 b0 )

(5)

since a0 , a1 , b0 , b1 ∈ R and the conjugate has no eﬀect at level zero.
For n ≥ 2, showing just the ﬁrst pair in each half, with α ∈ B(n) and β = 00 · · · 0 of length
n − 2, then
n−1 pairs

n−1 pairs

⏟⏟
⏟⏟
( ⏞(
)⏞ ⏞(
)⏞ )
aα = (· · · ((aβ00 , aβ10 ), . . .) , (· · · ((aβ01 , aβ11 ), . . .) .
⏟ ⏞⏞ ⏟
⏟ ⏞⏞ ⏟
n−2

(6)

n−2

For n = 2, again with α, β ∈ B(1) of lengths 1,

(a0 , a1 )(b0 , b1 )
(
)
= (a00 , a10 ), (a01 , a11 ))((b00 , b10 ), (b01 , b11 )
(
= (a00 , a10 )(b00 , b10 ) − ǫ2 (b01 , b11 )∗ (a01 , a11 ),
)
(b01 , b11 )(a00 , a10 ) + (a01 , a11 )(b00 , b10 )∗
(
= (a00 b00 − ǫ1 b10 a10 , b10 a00 + a10 b10 ) − ǫ2 (b01 a01 + ǫ1 a11 b11 , b01 a11 − b11 a01 ),
(
)
b01 a00 − ǫ1 a10 b11 , a10 b01 + b11 a00 ) + (a01 b00 + ǫ1 b10 a11 , −b10 a01 + a11 b00 )
(
= (a00 b00 − ǫ1 b10 a10 − ǫ2 b01 a01 − ǫ1 ǫ2 a11 b11 , b10 a00 + a10 b00 − ǫ2 b01 a11 + ǫ2 b11 a01 ),
(
)
b01 a00 − ǫ1 a10 b11 + a01 b00 + ǫ1 b10 a11 , a10 b01 + b11 a00 − b10 a01 + a11 b00 ) .

(7)

Lemma 2. For blade oi1 i2 ...ik then o2i1 i2 ...ik = −ǫi1 ǫi2 . . . ǫk , for i1 i2 . . . ik , k ∈ Nn1 .

Proof. From (7) or (4) with α = β and β ∈ B(1) then only parallel terms exist at level two,
∑
(aβ0 , aβ1 )(bβ0 , bβ1 ) = ((a00 b00 − ǫ1 b10 a10 − ǫ2 b01 a01 − ǫ1 ǫ2 a11 b11 , 0),
β
(b01 a00 − ǫ1 a10 b11 + a01 b00 + ǫ1 b10 a11 , 0)).
Hence, by symmetry and embedding in (6), the following apply to levels of the pyramid after
one,
o1 o1 = ((−ǫ1 b10 a10 , 0), (0, 0)) = −ǫ1 ,
o2 o2 = ((−ǫ2 b01 a01 , 0), (0, 0)) = −ǫ2 and
o12 o12 = ((−ǫ1 ǫ2 a11 b11 , 0), (0, 0)) = −ǫ1 ǫ2 .
This is generalised to a k-blade, aα , α ∈ B(n), with α containing ones at positions i1 , i2 , . . . , ik ∈
Nn1 , k ∈ Nn1 , and zeros elsewhere. From (4), if ik ̸= n then the zeros at the end of α will act as
a2α = aα bα until the rightmost index, ik = i, is reached. Then
aα bα = aαi 1 αi bαi 1 αi = (−ǫi b∗αi 1 αi aαi 1 αi , 0)
where
b∗αi 1 αi aαi 1 αi =

{

(ǫi−1 b∗αi−1 1 αi−1 aαi−1 1 αi−1 , 0) if i − 1 ∈ i1 , i2 , . . . , ik ,
otherwise.
(b∗αi−1 0 αi−1 aαi−1 0 αi−1 , 0)

The ﬁrst case is positive because the original conjugation negated the oi element and a new
conjugate for the i−1 level was introduced whereas for b∗αi−1 0 αi−1 the conjugation is passed to the
next level without eﬀect. Continuing to the following levels has no eﬀect on the original sign and
together will introduce ǫj from a2αj 1 αj ∀j ∈ i1 , i2 , . . . , ik−1 . This means o2i1 i2 ...ik = −ǫi1 ǫi2 · · · ǫik
which is assumed true and by induction a2α1 is considered for α having ones in positions i1 i2 . . . ik
and zeros elsewhere. Then
aα1 bα1 = (−ǫn+1 b∗α1 aα1 , 0),
hence o2i1 i2 ...ik (n+1) = −ǫi1 ǫi2 . . . ǫik ǫn+1 .
4

## PDF page 5

Lemma 3. For δ ∈ A(n − 1) not all zeros then oδ on = oδn and on oδ = −oδn .
Proof. At level n = 1, 1o1 = (1, 0)(0, 1) = (0, b1 a0 ) = o1 . At n = 2,
o1 o2 = ((0, 1), (0, 0))((0, 0), (1, 0)) = ((0, 0), (0, a10 b01 )) = o12 .
For the reverse product, at level n = 1, o1 1 = (0, 1)(1, 0) = (0, b1 a0 ) = o1 . At n = 2,
o2 o1 = ((0, 0), (1, 0))((0, 1), (0, 0)) = ((0, 0), (0, a01 b∗10 )) = −o12 .
The symmetry of the on pyramid used here for any oδ ≡ aα0 is that the ﬁrst term on the
right hand side of the pyramid is a cross term and all the rest are parallel terms,
{(
)
(0, 0), (0, aαn−1 10 b∗βn−1 01 ) if oδ contains on−1 and
)
aα0 bβ1 = (0, aα0 bβ1 ) = (
(0, 0), (aαn−1 00 bβn−1 01 , 0) otherwise.

Since conjugation has no eﬀect on bβn−1 0 then extrapolating to level 0 gives a positive sign,
oδ on = oδn . The second case, on oδ , has the same symmetry, with the conjugate having no eﬀect
other than the minus sign introduced at level n,
{(
)
(0, 0), (0, −bαn−1 10 a∗βn−1 01 ) if oδ contains on−1 and
∗
)
aβ1 bα0 = (0, aβ1 bα0 ) = (
(0, 0), (aβn−1 01 bαn−1 00 , 0)
otherwise

hence on oδ = −oδn .

Theorem 1 (Cayley-Dickson algebras). The Cayley-Dickson construction to any level, n, generates an algebra with pure elements, x, y satisfying xy = −yx if x ̸= y and, if ǫi = 1, ∀i ∈ Nn1
and x = y, then xy = −1. The unit, 1, has no eﬀect under multiplication.
Proof. From Lemma 1, product expansion and contraction of blades shows that the generators of
the algebra under multiplication are an injection and repeated multiplication becomes a surjection
thus generating the scaled basis of the algebra. Lemma 2 shows that for ǫi = 1, ∀i ∈ Nn1 then
o2α = −1, ∀α ∈ A(n). For the unit, 1 = bβ where β ∈ B(n) is all zeros, the product from (4) at
level i > 1 is seen to be an identity for itself and pure elements,
(
)
(aαi 0 αi , aαi 1 αi )(bβ , 0) = aαi 0 αi bβ , aαi 1 αi b∗β
(
)
= (aαi−1 0 αi−1 , 0)(bβ , 0), (aαi−1 1 αi−1 , 0)(bβ , 0) .

The expansion terminates at level 0 with aα bβ = aα and is symmetric so aβ bα = bα also.
Anticommutation is proved by induction starting with Lemma 3 for o1 o2 = −o2 o1 . This is the
n = 2 level but is provided as the basis of induction in the proof of the lemma. By the symmetry
of the construction, this result applies at all levels n > 2 for these pure elements. Assuming
the n − 1 product is true, aα0 bβ0 = −bβ0 aα0 , for α, β ∈ B(n − 1), not all zeros, and α ̸= β,
then multiplying by on produces a pyramid whereby the left-hand half does not contain on and
the right-hand half reﬂects this structure but includes on for all elements. Proving xy = −yx
for the on case is divided into three equations which need to be proved; on aα0 = −aα0 on ,
aα1 bβ0 = −bβ0 aα1 and aα1 bβ1 = −bβ1 aα1 , for α, β not all zeros. Lemma 3 has already shown
the ﬁrst case and found that a∗α = −aα since α is not all zeros. Hence, the second case with β
not all zeros, is
aα1 bβ0 = (0, aα1 )(bβ0 , 0) = (0, aα1 b∗β0 ) and
bβ0 aα1 = (bβ0 , 0)(0, aα1 ) = (0, aα1 bβ0 ) = −aα1 bβ0 .
Finally, induction and symmetry of the pyramid is used on aα1 bβ1 + bβ1 aα1 = 0,
aα1 bβ1 = (0, aα1 )(0, bβ1 ) = (−b∗β1 aα1 , 0) and
bβ1 aα1 = (0, bβ1 )(0, aα1 ) = (−a∗α1 bβ1 , 0).

(8)

These anticommutator terms occur in the same position on the right-hand half as the terms
without on on the left-hand half of the pyramid. After the ﬁrst pyramid multiplication they
have identical paths through the each side of the pyramid apart from the minus signs and the
conjugate. The conjugate descends the path until the ﬁrst 1 in α from the right and changes
5

## PDF page 6

the sign and disappears for the rest of the path, a∗α1 = −aα1 and similarly, a∗β1 = −aβ1 . Hence
the minus signs are cancelled in (8) and so using symmetry and arguing by induction with
aα0 bβ0 − bβ0 aα0 = 0 true at level 2 and assumed true at level n − 1, then
−b∗β1 aα1 − a∗α1 bβ1 = aα0 bβ0 + bβ0 aα0 = 0.

Corollary. The ﬁrst four levels of blades with ǫi = 1 ∀i ∈ N41 are isomorphic to complex numbers,
C, quaternions, H, octonions, O, and sedenions, S, respectively.
Proof. Theorem 1 showed that blades generate Cayley-Dickson algebras under the product rules
(4). It is obvious that the ﬁrst generator, o1 , at level 1 is isomorphic to the imaginary of complex
numbers. At level two, the usual representation of quaternions also have the cyclic product rules,
ij = k, jk = i and ki = j. Starting by calculating the cyclic rules in full
o1 o2 = ((0, 1), (0, 0))((0, 0), (1, 0)) = ((0, 0), (0, 1)(1, 0))
= ((0, 0), (0, 1∗ )) = o12 ,
o2 o12 = ((0, 0), (1, 0))((0, 0), (0, 1)) = (−(0, 1)∗ (1, 0), (0, 0))
= ((0, 1), (0, 0)) = o1 and

(9)

o12 o1 = ((0, 0), (0, 1))((0, 1), (0, 0)) = ((0, 0), (0, 1)(0, 1)∗)
= ((0, 0), −(−1, 0)) = o2 .
Thus level 2 is isomorphic to H. At level 3 there are seven blades, {o1 , o2 , o12 , o3 , o23 , o13 , o123 },
which matches the number of octonion basis elements and it is obvious that the quaternions
are embedded in the ﬁrst three pure terms, which is a feature of O. This suﬃces to provide
the isomorphism. At level 4 there are 15 blades matching the sedenions and the octonions are
embedded in the ﬁrst seven blades. This is a requirement of sedenions and will suﬃce to prove
the isomorphism, given Theorem 1.
The alternative ring properties of Cayley-Dickson algebras that are essential to simplify nonassociative expressions are now proved [18].
Lemma 4. For x and y distinct blades with ǫi = 1, i ∈ Nn1 , then yxx = −y and x(xy) = −y.
Proof. The later statement is true if the former is true, x(xy) = −(xy)x = yxx, if y ̸= x and
obviously x(xx) = −x otherwise. The proof of the former proceeds via induction. It works for H
which needs to be checked for the six combinations of two from three elements using the cyclic
product rules (9),
o1 o2 o2 = o12 o2 = −o2 o12 = −o1 ,
o1 o12 o12 = −o2 o12 = o12 o2 = −o1 ,
o2 o1 o1 = −o1 o2 o1 = −o12 o1 = −o2 ,
o2 o12 o12 = −o12 o2 o12 = o1 o12 = −o2 ,
o12 o1 o1 = −o1 o12 o1 = o2 o1 = −o12 and
o12 o2 o2 = −o1 o2 = −o12 .
Assuming aα0 bβ0 bβ0 = bβ0 (bβ0 aα0 ) = −aα0 , α, β ∈ B(n − 1) not all zeros, then by induction only
the following conditions need to be proved, which for the second two equations again use the
symmetry argument that after the ﬁrst step in the pyramid expansion the left-right symmetry
means the same path is followed on both sides,
aα1 bβ0 bβ0 = (0, aα1 )(bβ0 , 0)(bβ0 , 0)
= (0, aα1 b∗β0 )(bβ0 , 0)
= (0, aα1 b∗β0 bβ0 )
= −aα1 ,

6

## PDF page 7

aα0 bβ1 bβ1 = (aα0 , 0)(0, bβ1 )(0, bβ1 )
= (0, bβ1 aα0 )(0, bβ1 )
= (−b∗β1 (bβ1 aα0 ), 0)
= (bβ0 (bβ0 aα0 ), 0)
= −aα0

and

aα1 bβ1 bβ1 = (0, aα1 )(0, bβ1 )(0, bβ1 )
= (−b∗β1 aα1 , 0)(0, bβ1 )
= (0, −bβ1 (b∗β1 aα1 ), 0)
= (0, bβ0 (bβ0 aα1 ), 0)
= (0, −aα1 )
= −aα1 .
This leaves xon on where β is all zeros in the last two equations. In that case the conjugate has
no eﬀect after the ﬁrst step and −b∗β1 (bβ1 x) = −bβ1 (b∗β1 x) = −x. Hence aα bβ bβ = −aα for all
α, β ∈ B(n). Note that while xyzz = −xy, it is not necessarily true that x(xyz) = −yz for
distinct blades x, y, z. For example, o1 (o1 o2 o3 ) = o23 .
Deﬁnition. The associator is deﬁned, using left-expansion, as
[a, b, c] = (ab)c − a(bc) = abc − a(bc),
which is zero for H because quaternions are associative
[5] and have one ordered pure triple. This
()
is not the case for octonions, O, which have 73 = 35 ordered pure triples. Of these 28 have a
non-zero associator and seven are associative. The latter triples are
(o1 , o2 , o12 ), (o2 , o3 , o23 ), (o1 , o3 , o13 ), (o1 , o23 , o123 ),
(o2 , o13 , o123 ), (o12 , o3 , o123 ), (o12 , o13 , o23 ).

(10)

All of the triples in (10) are quaternion-like, either isomorphic or anti-isomorphic with quaternions with cyclic product rules, and the ﬁrst one is the quaternion subset from level 2. The next
two have the same structure and would be called quaternions if the basis where reordered. The
last triple provides rotations between the three generators, which is a feature of quaternions if
the generators represent three dimensional vector space, R3 . The three remaining triples can
not be interpreted in this way but the graded product of the three blades in all seven triples is
seen to be a scalar, either ±1. The remaining triples will be shown to be non-associative. For
example, Lemma 2 has o1 o2 o3 = o123 whereas expanding the pyramid for o1 (o2 o3 ) gives the term
−a100 b011 in the o123 position so that o1 (o2 o3 ) = −o123 , hence the associator is non-zero and this
triple is non-associative, [o1 , o2 , o3 ] = 2o123 .
The names quaternion and octonion seem to be derived from book binding techniques involving a quire of four or eight folios of paper, respectively. Traditionally, an ancient book or
codex would use separate sheets or bifolio with a single fold stacked and bound to the binding
or stub. This was superseded with folding a single large sheet several times to make the quire.
The type of fold starts with a bifolio, which is double the number of folios. Two bifolia have
quarto fold type, four has Octavo and eight has extodecimo type, which covers more than eight
folios [19]. Accordingly, the preﬁx ultra is introduced herein to designate all power-associative
Cayley-Dickson algebras. Then, the complex numbers are followed by the hypercomplex numbers, O and H, and the following power-associative algebras would be known as the ultracomplex
numbers.
Deﬁnition. The Cayley-Dickson series for power-associative algebras after A3 , with ǫi = 1
for i ∈ Nn1 , are designated Um , m = n − 3, which refers to the ultronion algebras. Thus the
normed algebras, R, C, H and O, are not included in the Um series and the series starts with the
sedenions, S ≡ U1 . The split algebras are denoted Ũm and later it is shown they are isomorphic
to each other, for any dimension, for any positive number of ǫi = −1, i ∈ Nn1 . The proof of
uniqueness of Ũn also applies to split versions of C (Lorentz numbers), H and O.

7

## PDF page 8

3

Structure Theorems

To concentrate on non-associative triple products the term triad is used to provide distinct triples
that avoid scalars and repeated elements with trivial associativity.
( )
Deﬁnition. There are N 3 scaled triple products bcd and N3 naturally ordered triples with
blades b < c < d where N = 2n − 1 and n is the number of generators. The ordered triples are
the same as removing all pairs and triples of the same element from the N 3 set and dividing by
the number of permutations, 6. A triad is deﬁned as ordered triples containing distinct blades
whereby b < c < d so that bcd is non-zero. Hence basis element a = bcd can be deﬁned for triads
and a is distinct from b, c, d, which follows from Lemma 1. Of course, there are 5 unordered
triples for each triad.
Theorem 2 (Associativity theorem). The 24 permutations of triad products generate three types
of associativity, called Types 1, 2 and 3. These are shown in Table 1 where equivalence of
associators means both are zero or both are non-zero, noting that only 12 permutations for ordered
b, c, d and a = bcd are required because [a, b, c] = −[c, b, a].
Table 1: Triad Associativity Types
Associativity Equivalence
Associativity
[b, a, c] ≈ [b, d, c] ≈ [a, b, d] ≈ [a, c, d]
Type 1
[a, b, c] ≈ [b, c, d] ≈ [b, a, d] ≈ [a, d, c]
Type 2
[a, c, b] ≈ [c, b, d] ≈ [a, d, b] ≈ [c, a, d]
Type 3
Proof. Excluding complete associativity for triads where all associativity types are zero means
that a(bc) = −(bc)a = cba if a is not a scaling of bc and similarly for abc = (ab)c = c(ba). Hence
[a, b, c] = abc − a(bc) = c(ba) − (cb)a = −[c, b, a]. This is also true for associative triple products,
where a is a scalar, because both sides are zero. Now, if b, c, d are not associative, the relation
a = bcd means ad−1 = bc or d = −a(bc)−1 = −bca/b2 /c2 , noting that (bc)2 = −b2 c2 . First,
Type 2 and Type 3 associativity are analysed.
Assuming Type 2 associativity, [a, b, c] = abc − a(bc) = 0 or [c, b, a] = cba − c(ba) = 0, then
substituting d into the other three associators in the second row in Table 1, scaled by (bc)2 , gives
[b, c, d](bc)2 = bc(bca) − b(c(bca)) = −(bca)(bc) − (bca)cb = −(bc)a(bc) + c(ba)cb
= a(bc)(bc) − baccb = a(bc)2 + abbc2 = −ab2 c2 + ab2 c2 = 0,
[b, a, d](bc)2 = ba(bca) − b(a(bca)) = −ba(c(ba)) + b(bc)a2 = c(ba)(ba) + cbba2 = 0 and
[a, d, c](bc)2 = a(bca)c − a(bcac) = −(bca)ac + a(c(ba)c) = −bcca2 + (bacc)a = 0.
Assuming Type 3 associativity, [a, c, b] = acb − a(cb) = 0 or [b, c, a] = bca − b(ca) = 0, then
substituting d into the other three associators in the third row of Table 1, scaled by (bc)2 , gives
[c, b, d](bc)2 = cb(bca) − c(b(bca)) = −b(ca)(cb) − bcabc = cab(cb) − b(ca)bc
= −a(cb)(cb) + (ca)bbc = a − cac = 0
2

[a, d, b](bc) = a(bca)b − a(bcab) = −bcaab + bcaba = bcb + b(ca)ba = 0 and
[c, a, d](bc)2 = ca(bca) − c(a(bca)) = −bca(ca) − bcaac = −b(ca)(ca) + bcc = 0.
Assuming Type 1 associativity, [b, a, c] = bac − b(ac) = 0 or [c, a, b] = cab − c(ab) = 0, then
substituting d into the other three associators in the ﬁrst row of Table 1, scaled by (bc)2 , gives
[b, d, c](bc)2 = b(bca)c − b(bcac) = −bcabc + bcacb,
[a, b, d](bc)2 = ab(bca) − a(b(bca)) = (bca)(ba) − bcaba = −cba(ba) + cbaba and
[a, c, d](bc)2 = ac(bca) − a(c(bca)) = −bca(ac) − bcaca.
If Type 2 associativity is also assumed then cba = c(ba) and, also again using [c, a, b] = 0, the
three equations become
−bcabc + bcacb = c(ba)bc − c(ba)cb = −b(ac)bc + baccb = acbbc + abb = 0,
−cba(ba) + cbaba = c(ba)(ba) − c(ba)ba = −c + bac(ab) = −c + b(ac)ba = −c + cabba = 0 and
−bca(ac) − bcaca = c(ba)(ac) + c(ba)ca = −bac(ac) − bacca = −b(ac)(ac) − b = 0.
8

## PDF page 9

If Type 3 associativity is also assumed with Type 1 then bca = b(ca) or cba = −b(ca) and, also
again using [c, a, b] = 0, the three equations become
−bcabc + bcacb = −b(ca)bc + b(ca)cb = −acbbc − cabcb = −a − c(ab)cb = −a + abccb = 0,
−cba(ba) + cbaba = b(ca)(ba) − b(ca)ba = −cab(ba) + cabba = c(ab)(ab) + c = 0 and
−bca(ac) − bcaca = b(ca)(ca) − b(ca)ca = −b + cabca = −b + c(ab)ca = −b + bacca = 0.
Hence Types 2 and 3 associativity are non-associatively equivalent in there own right but Type 1
needs either Type 2 or Type 3 for equivalence.
Deﬁnition. The triple associator, T (b, c, d), is introduced to cover associativity Types 1, 2 and
3 to allow for an unambiguous deﬁnition of associativity,
T (b, c, d) = [b, d, c] − [d, c, b] + [c, b, d].
Deﬁnition. A triad, b, c, d, is associative if T (b, c, d) = 0 and non-associative if T (b, c, d) ̸= 0.
This may seem like over-kill but will soon be seen to be a necessary condition.
Artin’s theorem [5] is stated only for associative subalgebras of octonions but can be generalised and then extended to ﬁnd all subalgebras of any Cayley-Dickson algebra.
Theorem 3 (Generalised Artin theorem). Any two distinct blades of H, O or Um , m > 0,
generate an algebra isomorphic or anti-isomorphic to quaternions which is thus associative.
Proof. From Lemma 1, multiplying any two distinct blades generates a third distinct blade. Since
the generated blade is the symmetric diﬀerence then multiplying this third element by one of the
ﬁrst two will recover the other of the ﬁrst two. All such products are closed under multiplication
and forms a Cayley-Dickson algebra, by Theorem 1, because distinct blades anti-commute and
have negative square in this case. For any two blades, b and c then bc = d, cd = c(bc) = −bcc = b
and db = −cbb = c, by Lemma 4. These are the cyclic, quaternion-like product rules and thus
the triad b, c and bc is isomorphic to H. The triple associator shows associativity for the triad,
T (b, c, bc) = b(bc)c − b(bcc) − bc(cb) + bc(cb) + cb(bc) − c(b(bc))
= −bcbc + bb − bc(bc) + c(bcb)
= +1 − 1 + 1 − 1
= 0.
Theorem 4 (Ultronion generation). Any ultacomplex algebra, Um , m > 0, as well as O, can be
generated by n = m + 3 distinct blades, oαk , ∀ k ∈ Nn1 , with indices αk that include all n indices
an odd number of times over all k. For convenience, allow m = 0 as U0 = O.
Proof. Triad b, c, d (ie three distinct blades), with a = bcd non-scalar, is non-associative,
T (b, c, d) = bdc − b(dc) − dcb + d(cb) + cbd − c(bd)
= bdc + dcb − dcb + bcd − bcd + bdc
= 2bdc

(11)

= ±2a.
Combinations of b, c, d give seven distinct blades by Lemma 1, bc, bd, cd, bcd, which are isomorphic
to octonions because they satisfy the rules of Un and these are the same as O by Theorem 1. Any
n such terms similarly generate 2n − 1 distinct terms if, by Lemma 1, the symmetric diﬀerence
of their grades do not become the empty set, which is guaranteed by the condition that each
generator is represented an odd number of times in the indices. Hence they are isomorphic to
Un−3 , by Theorem 1.
The generation theorem disguises the complexity of the algebras since it avoids generating
algebras from arbitrary triads at higher levels. This will take some eﬀort and starts by analysing
the asymmetry of non-associativity.
Theorem 5 (Non-associativity theorem). If a triad is not associative then either all associativity
types are non-zero or only one is non-zero, the other two being zero.

9

## PDF page 10

Proof. From Table 1, for triad b, c, d, Type 1 associativity has bdc = b(dc), Type 2 associativity
has bcd = b(cd) and Type 3 associativity has cbd = c(bd). Starting with Type 1 and substituting
Type 3 then Type 2 associativity, is
bdc = −c(db) = −cbd = bcd = −b(dc),
which contradicts Type 1 associativity if Types 2 and 3 are assumed. Similarly, substituting the
reverse of Type 3 then Type 1 into Type 2,
bcd = −d(bc) = −dbc = bdc = b(dc) = −b(cd),
which contradicts Type 2 associativity. Finally substituting the reverse of both Type 2 and
Type 1 into Type 3,
cbd = −d(cb) = −dcb = cdb = c(db) = −c(bd),
which contradicts Type 3 associativity. This proves existence of associativity pairs for nonassociativity. For necessity, if any associator is non-zero then since a = bcd then the associator
must be ±2a. If only one associator type is zero and the other two are non-zero then from (11),
the triple associator becomes
T = ±2a ± 2a + 0 = ±2a,
which is again a contradiction and proves the conjecture. This theorem says nothing about all
three associator types being non-zero and the triple associator is satisﬁed in this case, as well as
satisfying the paired type associativity.
Deﬁnition. Non-associativity types are deﬁned, using ⋆ to mean non-zero, as
Associativity
Type 1 Type 2 Type 3
⋆
0
0
0
⋆
0
0
0
⋆
⋆
⋆
⋆

Non-Associativity
Type A
Type B
Type C
Type X

Deﬁnition. Triad (b, c, d) generates a Malcev algebra if it satisﬁes Mal’cev’s identity [20], which
is immediately simpliﬁed for ultracomplex numbers,
bc(bd) − bcdb − cdbb − dbbc = 0,
−bc(db) − bcdb + cd + dc = 0 or
bcdb + bc(db) = 0.

(12)

The simpliﬁed identity means [bc, d, b] ̸= 0 which implies A or X non-associativity if bc is
interpreted as a new c. Malcev algebras deﬁne non-associative Lie algebras and this is analysed
later where B and C non-associativity types are also encountered. For quaternion-like triads,
d = bc can be substituted into (12),
bcdb + bc(db) = bc(bc)b + bc(bcb) = −b + bcc = −2b
and similarly, cycles d = b or d = c are also non-zero. So associative algebras are not Malcev
algebras.
Theorem 6 (Moufang associativity theorem). A Moufang loop [21] is a non-associative algebraic
structure that satisﬁes three identities for non-associative triad (b, c, d). Calling these types 1 to
3, then each type exhibits the non-associativity shown in the following table.
Type
1
2

Moufang non-associativity
d(b(dc)) − dbdc = 0
b(d(cd)) − bdcd = 0

3

db(cd) − d(bc)d = 0

10

Equivalence
B or X
C or X
B or X if Malcev,
A or C otherwise

## PDF page 11

Proof. Type 1 and 2 equations, multiplied by d and assuming d2 = −1, become respectively
d(b(dc))d − dbdcd = −b(dc)dd + bddcd = dcbdd − bcd = −dcb − bcd = −bcd − b(cd) = 0 and
b(d(cd))d − bdcdd = −d(cd)bd + dbcdd = −cddbd + dbcdd = cbd − dbc = cdb + c(db) = 0.
Substituting the ﬁrst equation into Type 2 associativity is [b, c, d] = bcd − b(cd) = 2bcd, which
is non-zero. Substituting the second into Type 3 associativity is [c, b, d] = cbd − c(bd) = 2cbd,
which is also non-zero. Hence Moufang loop non-associativity of Type 1 and 2 corresponds to
B-non-associativity and C-non-associativity, respectively, or X-non-associativity in both cases.
Multiplying Moufang type 3 by db gives,
db(cd)(db) − d(bc)d(db) = −cd(db)(db) − bc(db) = 0,
so cd = bc(db). Applying (12) so that cd = −bcdb and substituting into Type 2 associativity
gives,
[b, c, d] = bcd − b(cd) = bcd + b(bcdb) = bcd − bcdbb = bcd + bcd = 2bcd ̸= 0.
This implies type B or X non-associativity. If Mal’cev’s identity is not satisﬁed then (12) takes the
opposite sign, [bc, d, b] = 0, and Type 2 associativity is then zero so that A or C non-associativity
holds. This completes the proof and it is noted that it is possible to use combinations of the
Moufang types along with Mal’cev’s identity to distinguish all four types of non-associativity A,
B, C and X.
Note that some authors[22, 23] include a fourth Moufang type, db(cd) = d(bcd). But this is
the same as the third type since d(bcd) = −bcdd = d(bc)d.
The associative triads have pairs (b, c), (b, bc) and (c, bc), which form a 3-cycle of pairs. This
applies to all pairs and can be extended to triads to provide another level of structure to the
ultronions.
Label
C
H
O
U1
U2
U3
U4
U5
U6
U7

Associative
0
1
7
35
155
651
2,667
10,795
43,435
174,251

Table 2: Triad Structure
Non-Cycles 3-Triad Cycles
0
0
0
0
4
24
60
360
620
3,720
5,580
33,480
47,244
283,464
388,620
2,331,720
3,152,140
18,912,840
25,390,860
152,345,160

Total
0
1
35
455
4,495
39,711
333,375
2,731,135
22,108,415
177,910,271

Deﬁnition. Naturally ordered basis pairs form 3-cycles, (b, c), (b, bc) and (c, bc), which cover
all ordered pairs. This is because there are (2n − 1)(2n − 2)/2 combinations of pairs which have
factors one and two numbers less than a power of 2 so one must have a factor of 3. These pairs
can be ordered as b < c < bc and the pairs of the ordered 3-cycles are called the ﬁrst, second
and third cycle, respectively. A 3-triad cycle extends this to the triads (b, c, d), (b, bc, d), (c, bc, d)
where b < c < bc < d. These are not distinct since triads with d < bc have second and third
cycles already included elsewhere. Such cases are called non-cycles and associative triads, d = bc,
are also degenerate.
Table 2 enumerates all triads for Cayley-Dickson algebras for up to 10 generators. Nonassociative triads are split into non-cycles and cycles where the non-cycle ones have d < bc. The
summation
of these triad enumerations is provided in the last column of Table 2 that matches
(N )
,
where
N
= 2n − 1.
3
For quaternions, H, the associative triad in Table 2 is (o1 , o2 , o12 ). For octonions, O, the 7
associative triads have been provided by (10). The 24 3-triad cycles are derived from eight triads
starting with the following ﬁrst cycles,
(o1 , o2 , o3 ),
(o1 , o3 , o23 ),

(o1 , o2 , o13 ),
(o1 , o3 , o123 ),

(o1 , o2 , o23 ),
(o2 , o3 , o123 ),
11

(o1 , o2 , o123 ),
(o12 , o13 , o123 ).

(13)

## PDF page 12

All these octonion triads have X-non-associativity and it will soon be proved that the cycles
must also be of type X. Remember [o1 , o2 , o3 ] = 2o123 and multiplying terms by distinct basis
elements does not change the non-associativity type. To achieve this we need another generator,
o4 , for example, so that for b = o1 , c = o2 and d = o34 then Type 2 is associative, [o2 , o3 , o34 ] =
−o1234 + o1234 = 0 and Type 1 is non-associative, [o1 , o34 , o2 ] = −o1234 − o1234 ̸= 0.
Table 3 provides the ﬁrst A and C triads from U1 and the ﬁrst B triad from U2 as examples.
For X non-associativity, the ﬁrst U1 X case not included in O is selected but note that any
octonion non-associative triad could have been selected with generator o3 replaced with o4 .
Type
A
B
C
X

Table 3: Non-associativity to Associativity Examples
Type 1
Type 2
Type 3
[o1 , o34 , o2 ] = −2o1234 [o1 , o2 , o34 ] = 0
[o2 , o1 , o34 ] = 0
[o1 , o345 , o24 ] = 0
[o1 , o24 , o345 ] = −2o1235 [o24 , o1 , o345 ] = 0
[o1 , o34 , o24 ] = 0
[o1 , o24 , o34 ] = 0
[o24 , o1 , o34 ] = −2o123
[o1 , o4 , o2 ] = −2o124
[o1 , o2 , o4 ] = 2o124
[o2 , o1 , o4 ] = −2o124

The enumeration of 3-triad cycles in Table 2 can be divided by three and categorised as
belonging to one of eight 3-triad cycles and the enumeration of non-cycles is separated into the
four single triads rows shown in Table 4. This table provides the 3-triad cycles structure for
Cayley-Dickson algebras up to 10 generators and will be used to categorise zero divisors in the
next section. As can be seen the structures up to U4 are distinct and after this the structure
is the same so only U1 , U2 , U3 and U4 provide algebras with unique structure for ultracomplex
numbers. The following theorem validates this table.
Theorem 7 (Cycles theorem). Of the 64 possible non-associativity 3-triad cycles only silos AAA,
ACC, XBB, BBA, BXC, CAB, CCX and XXX exist.

Structure
AAA
BBA
ACC
XBB
BXC
CAB
CCX
XXX
A
B
C
X

O
0
0
0
0
0
0
0
8
0
0
0
4

U1
28
0
0
0
0
0
28
64
0
0
28
32

Table 4: Non-associative Structure
U2
U3
U4
U5
U6
252 1,988 14,868 111,300 849,492
168 1,848 15,120 115,080 872,928
84 1,344 12,852 105,672 834,876
0
672
9,072
87,360 752,976
0
168
4,536
60,648 621,432
0
0
3,024
31,744 577,584
336 2,660 18,648 129,612 931,392
400 2,480 16,368 115,824 863,600
84 1,008 9,828
87,864 747,180
0
504
7,560
78,456 709,128
252 1,988 14,868 111,300 849,492
284 2,080 14,988 111,000 856,340

U7
6,605,284
6,721,848
6,569,136
6,219,360
5,628,168
5,431,104
6,955,060
6,651,760
6,175,008
6,022,296
6,605,284
6,588,272

Proof. Starting with A-non-associativity for the ﬁrst cycle then showing that the second and
third cycles have Type 2 associativity shows that these are either A or C-non-associative. Here
we use Type 2 associativity [b, c, d] = 0 and Type 3 associativity [c, b, d] = 0 and apply to the
second cycle equivalent,
[b, bc, d] = b(bc)d − b(bcd) = −bcbd + bcdb = cbbd + b(cd)b = −cd + cd = 0 and
[c, bc, d] = c(bc)d − c(bcd) = −bccd + bcdc = bd − c(bd)c = bd − bd = 0.

(14)

Hence the result is either A or C and AA means third cycle A and AC means third cycle C needs
to be shown. Using Type 3 associativity, [c, b, d] = 0, then third cycle Type 2 associativity is
[c, bc, d] = c(bc)d − c(bcd) = −bccd − cbdc = bd − c(bd)c = 0,
meaning either AAA or AAC. Now assume third cycle Type 3 associativity, then
[bc, c, d] = bccd − bc(cd) = 0 =⇒ db = −bc(cd)
Substitute this into second Type 3 associativity,
[bc, b, d] = bcbd − bc(db) = −cbbd + bc(bc(cd)) = cd + cd(bc)(bc) = 0,
12

## PDF page 13

which means the third cycle for AA is also A. To the contrary, if the second cycle is not Type 3
associative then neither is the third so it must be ACC.
For the BBA and BXC silos we need to show that the second cycle has non-zero Type 2
associator and third cycle Type 2 associativity. Starting with the Type 2 associator for the
second and third cycles and using Type 3 associativity, [c, b, d] = 0, and Type 1 associativity,
[b, d, c] = 0, then
[b, bc, d] = b(bc)d − b(bcd) = −bcbd + bcdb = cbbd − c(bd)b = dc + b(dc)b = 2dc ̸= 0 and
[c, bc, d] = c(bc)d − c(bcd) = −bccd + bcdc = bd − c(bd)c = bd − bd = 0.
So the second cycle is either B or X-non-associative and the third A or C. If the second cycle
is B then the third can be expanded using Type 3 and Type 1 associativity. Considering third
cycle Type 1 associativity and using Type 3 associativity and assuming the third cycle Type 3
associativity from (14), then
[c, d, bc] = cd(bc) − c(d(bc)) = cd(bc) − bcdc = cd(bc) + c(bd)c = cd(bd) + bc(cd) = cd(bd − bc) ̸= 0.
Hence BB has A as the third cycle and therefore BXC is the other 3-cycle.
For CAB and CCX silos, consider the second and third Type 2 associativity. Using Type 2
associativity, [b, c, d] = 0, and Type 1 associativity, [b, d, c] = 0, then
[b, bc, d] = b(bc)d − b(bcd) = −bcbd + bcdb = cbbd + b(cd)b = −cd + cd = 0 and
[c, bc, d] = c(bc)d − c(bcd) = −bccd + bcdc = bd + b(cd)c = bd − bdcc = 2bd ̸= 0.
Hence the second cycle is either A or C and the third either B or X. This is separated by showing
that the second and third associator are either both associative or both non-zero. Substituting
second Type 3 associativity, [bc, b, d] = 0 as cd = bc(db) into the third gives,
[bc, c, d] = bccd − bc(cd) = −bd − bc(bc(db)) = −bd − db(bc)(bc) = 0.
Hence C in the ﬁrst cycle leads to CAB or CCX silos.
The silos that start with X non-associativity are proved using Moufang’s non-associativity.
From Theorem 6, for X-non-associativity the Moufang types are 1 and 2,
d(b(dc)) − dbdc = dcbd + bddc = 0
b(d(cd)) − bdcd = cddb − bdcd = 0

⇒
⇒

bc = dcbd and
bc = bdcd.

(15)
(16)

So the second cycle is either B or X. Type 3 and 1 for the second cycle using (16) for Type 3 is
[bc, b, d] = bcbd − bc(bd) = cd − bc(bd),

(17)

[b, d, bc] = bd(bc) − b(d(bc)) = bd(bc) − bcdb = bd(bc) − dcbddb = bd(bc) − dc = [bc, b, d].
Type 2 and 3 for the third cycle with (15) applied to Type 2 is
[c, bc, d] = c(bc)d − c(bcd) = bd + bcdc = bd + bdcddc = 2bd ̸= 0,
[bc, c, d] = bccd − bc(cd) = −bd − bc(cd).

(18)

Hence, the third cycle is B or X, since Type 2 is non-zero, assuming the ﬁrst cycle is X or B,
from (15). If Type 3 second cycle is zero, such that cd = bc(bd) from (17), then (18) becomes
−bd − bc(cd) = −bd + bc(bd)(bc) = −bd − bd(bc)(bc) = 0.
So again, the third cycle is B if the second is B, alternatively, both are X. Since the ﬁrst cycle
was assumed to be X we have 3-triads cycles XXX or XBB.
Half of the 3-triad cycle silos satisfy the identity for Malcev algebra, (12), which can now
be recognised as second and third cycles from the Cycle theorem. Due to the cyclic rules the
AAA and XXX silos satisfy (12) for all cycles so each 3-triads cycle provides a Malcev algebra
of 3 triads. This is applicable to the eight XXX cycles of O indicated in Table 4 and shown in
(13). The four non-cycle X triads are (o2 , o3 , o13 ), (o2 , o13 , o23 ), (o12 , o3 , o13 ) and (o12 , o3 , o23 )
and these also satisfy Mal’cev’s identity since their second and third cycle parts overlap with
other X triads. This completes the 28 Malcev triads in O that provide the tangent space of
13

## PDF page 14

the 7-sphere since the 7 associative O triads do not satisfy the Malcev identity. There are four
remaining silos with partial Malcev properties. The ACC and XBB satisfy (12) for the second
and third cycles but not the ﬁrst. The other two cases are BAC and CAB where the ﬁrst cycle
are Malcev algebra triads but the second and third are not. All these cases are derived from (12)
which implies that only cycles that include A and X cases will satisfy this identity.
The X non-associative triad is the only completely symmetric non-associative type and this
is the characteristic of octonions. This identiﬁes the non-associative triads of O(in) the XXX silo
and the O parts of U1 in Table 4. Each triad generates 7 distinct blades giving 73 = 28 distinct
triads and the members of 3-triad cycles are already included in this set so only the ﬁrst cycle
needs to be considered. O have 8 × 3 = 24 triads in the XXX silo and 4 in the non-cycles. U1 has
eight times these numbers and these can be identiﬁed with 8 triads that generate the composed
O then seven copies of O,
(o1 , o2 , o3 ), (o1 , o2 , o4 ), (o1 , o3 , o4 ), (o1 , o23 , o4 ),
(o2 , o3 , o4 ), (o2 , o13 , o4 ), (o12 , o3 , o4 ), (o12 , o13 , o4 ).
The remaining AAA and CCX silos have 56 3-triad cycles giving seven copies of another
algebra with triads
(o1 , o2 , o34 ), (o1 , o3 , o24 ), (o1 , o23 , o24 ), (o2 , o3 , o14 ), (o2 , o13 , o14 ), (o12 , o3 , o14 ), (o12 , o13 , o14 ).
Each of these are isomorphic to an algebra documented in [10] which is part of a series of six algebras that break the symmetry of octonions whereby subalgebras of exceptional Lie algebra G2
provide automorphisms for these algebras. These have properties similar to the split octonions
seen later, so were called the pseudo-octonions, designated Pk where k is the number of nonassociative triads k = 4, 8, 10, 12, 14, 16. The ﬁrst case, P4 , was discovered[7] and enumerated[9]
by Cawagas. Only this algebra and two other pseudo-octonion algebras, P12 and P14 , are subalgebras of ultracomplex numbers, the other three are not included. The number of occurrences of
each subalgebra for the same algebras as shown in Table 4 is provided in Table 5. Octonions have
seven quaternion subalgebras, seen in 10 for (o1 , o2 , o3 ), and the pseudo-octionions have seven
octonion-like algebras, split or not. Each quaternion-like algebra overlaps three times with other
octonion-like rings. For example, (o1 , o2 , o12 ) occurs in (o1 , o2 , o3 ), (o1 , o2 , o4 ) and (o1 , o2 , o34 ).
Hence the number of associative sub-algebras in sedonions is (7 + 8) × 7/3 = 35 and from the table is can be seen that the number of overlapping quaternion-like algebras for each octonion-like
subalgebra in Uk is 2k+1 − 1.
Structure
H
O
P4
P12
P14
Total Pk

O
7
1
0
0
0
0

Table 5: Ultracomplex Subalgebras
U1 U2
U3
U4
U5
U6
35 155 651 2,667 10,795 43,435
8
50
310 2,046 14,478 107,950
7
63
413 2,583 16,905 118,251
0
42
504 4,158 30,996 229,194
0
0
168 3,024 34,776 332,640
7
105 1085 9,765 82,677 680,085

U7
174,251
831,470
873,901
1,729,728
2,912,616
5,516,245

Deﬁnition. Deﬁne the number of blades or pure basis elements in Um as Nm = 2m+3 − 1. Also
deﬁne Hm , Sm and Om as the number of total H, Pk and O copies in Um , respectively. Each Pk
and O consists of 28 unique non-associative triads, unique due to Theorem 4 for O. Hence the
total number of triads in Um , which is the number of faces in the (m + 2)-simplex, is
)
(
Nm
= Hm + 28 × (Om + Sm )
3
.

Theorem 8 (Ultronion subalgebras). The number of Pk subalgebras in Um is Sm+1 = 7 × (Om +
Sm ). For convenience, m = 0 case is taken to be U0 = O, so m ≥ 0.
Proof. Table 5 shows these numbers for cases m ∈ N70 . It is also observed that the count for
each Pk is divisible by 7, hence Sm is divisible by 7, and that Sm = (Sm−1 + Om−1 ) × 7,

14

## PDF page 15

7
m
(for
) ∈ N0 . By induction, assume this is true in general and prove the Sm+1 case. Since
Nm
− Hm = 28 × (Om + Sm ) then
3

Sm+1
=
Sm

(Nm+1 )

(3Nm )
3

− Hm+1
− Hm

.

so the ratio of increase of the pseudo-octonion algebras equates to the rate of increase of the nonassociate triads. By induction the series proceeds past U7 with the same ratio and the octonions
− Sm+1 .
ﬁll in the diﬀerence, Om+1 = Sm+2
7
The silo sources for each subalgebra are provided in Table 6 along with the non-associative
type counts. Each algebra has 8 3-triad cycles from the silos totalling 24 triads and the remaining
4 triads are always found in the non-cycles, so these are not identiﬁed but can be discovered by
subtracting the identiﬁcation column from the silos. It is interesting to note that all subalgebras
have four X non-associativity types so a selection of a triad of type X does not guarantee an
algebra isomorphic to O will be generated.
Table 6: Subalgebra Identiﬁcation
Identiﬁcation
Silo counts
28X
8XXX
12A, 12C, 4X
4AAA and 4CCX
8A, 8B, 8C, 4X
4BBA, 2ACC, 2CCX or
2AAA, 2BBA, 2BXC, 2CCX
7A, 10B, 7C, 4X AAA, 3ACC, 4XBB or
AAA, XBB, 3BXC, 3CAB or
BBA, 2ACC, 2XBB, BXC, 2CAB or
BBA, ACC, XBB, 2BXC, 3CAB

Subalgebra
O
P4
P12
P14

Theorem 9 (Projection Theorem). Any triad from an ultracomplex algebra will generate an
algebra isomorphic or anti-isomorphic to H, O, P4 , P12 or P14 . Furthermore, triads from U1 can
project (or anti-project) to H, O or P4 , from U2 to a U1 subalgebra or P12 and all higher levels
can project to U2 subalgebras or P14 . This leads to the diagram of injections shown in Figure 1.

3

⤣

⤣
2

⤣

⤣
1

⤣

⤣

ℍ

⤣

ℂ

⤣

⤣

0

ℙ12 ℙ14

⤣

ℙ4

4

…

Figure 1: Injections of Cayley Dickson algebras
Proof. The injections of the normed composition algebras, C, H, O, are well deﬁned by doubling,
up to O, which has 7 copies of H and a new non-associative part given by 28 triads. These
correspond to the faces of the 6-simplex and the non-face triads, respectively, as discussed in
[10]. The associative and non-associative parts can be isolated, with associative triads being
quaternion-like by Theorem 3, and the non-associative injection into the ultronions analysed
separately. The number of distinct O + Pk subalgebra copies for each of the listed ultronions
matches the number of total non-associative triads divided by 28, as shown in Table 14, hence
these subalgebra copies provide complete coverage of each ultracomplex algreba. A member
of the XXX silo, (o1 , o2 , o3 ), generates O and the ﬁrst ordered member of CCX, (o1 , o24 , o34 ),
generates P4 . Table 4 shows that these are the only silos available for U1 . Then U2 contains
these silos and BBA with the ﬁrst ordered member, (o1 , o24 , o345 ), generating P12 . After this U3
contains silo XBB with ﬁrst ordered member (o14 , o25 , o36 ), which generates P14 . Higher level
ultracomplex algebras contain CAB, which can only generate P14 , for example the ﬁrst member
that ﬁrst appears in U7 , (o14 , o256 , o347 ).
As shown later, each of the pseudo-octonion algebras have 12 zero divisors making them
power-associative so this property ﬂows through to the ultracomplex algebras. Since there are
always seven copies of any of the pseudo-octonion algebras then zero divisors appear in multiples
of 84.
15

## PDF page 16

4

Zero Divisors

Deﬁnition. A Zero divisor is a term whereby another term exists such that both are non-zero
and the product is zero. Zero divisors can not be single blades so a zero divisor pair is deﬁned,
(a + b)(c + d) = 0, for a, b, c, d all distinct pure scaled basis elements and a2 = b2 and c2 = d2 .
Theorem 10 (Zero divisors theorem). The parallel terms and cross terms of the zero divisors
equation separate into
ac + bd = 0 and ad + bc = 0,
(19)
with the second equation being an identity thus reducing the deﬁnition to just ac = −bd. Further,
this is equivalent to Type 3 associativity and means the number of zero divisors for Un , Zm , is
Zm =

1
(Nm − 1)(Nm − 3)(Nm − 7).
16

Proof. Uniqueness of a, b, c and d ensures ac does not have the same blade as either ad or bc,
from the symmetric diﬀerence of Lemma 1, so the two equations (19) have distinct scaled blades
and are separable. Since b, c, d are distinct blades, they anticommute, and since a is pure then
a ≈ bcd then a is non-scalar so that b, c, d are non-associative, d ̸= bc. Hence triple products also
anticommute and the equations can be re-arranged as
a = −(bd)c−1 = c(bd)/c2 and a = −(bc)d−1 = cbd/d2 and
d = acb

−1

2

= b(ca)/b and d = (bc)a

−1

2

= bca/a ,

(20)
(21)

which implies c2 = d2 and a2 = b2 . Substituting (20) and (21) shows Type 3 associativity
[b, c, a] = bca − b(ca) = da2 − db2 = 0 and
[c, b, d] = cbd − c(bd) = ad2 − ac2 = 0.
Note that the reversed product (c + d)(a + b) generates −ac − bd = 0 so provide the same zero
divisor pair. Finally, substituting for a, ad = cbdd/d2 = −bc so that ad + bc = 0 is an identity.
Hence zero divisor pairs are separated into two types for A and B non-associative triads that
are both Type 3 associative. Octonions can not have zero divisors because the non-associative
triads are X non-associative. Swapping the last two elements of the associator in Table 1 swaps
Type 1 associativity and Type 2 associativity and has no correspondence with Type 3 associativity other than changing the sign. Hence A and B zero divisors may overlap because swapping the
terms within brackets produces the same zero divisor pair. Table 5 shows 12 A non associative
types for P4 , which corresponds to 12 zero divisor pairs. The other pseudo-octonion algebras
have mixures of A and B types adding up to more than 12 but since all ordered triples are included in the list of 28 triads then some A and B types overlap as zero divisors to give 12 distinct
of pseudo-octonion algebras at each level as
zero divisor pairs. Theorem 8(deﬁnes the number
)
(Nm )
7
− Hm with Hm quaternion-like or non-trivial associative
Sm+1 = 7 × (Om + Sm ) = 28
3
algebras in Um . The sequence for Hn shown in Table 5 is provided by M4415 (A006095) in [24]
as the Guassian binomial with coeﬃcients [n, 2] for q = 2. This is a(n) = (2n − 1)(2n−1 − 1)/3,
n > 2. Substituting 2n = Nm + 1 and n = m + 3 gives, for m ≥ 0,
Hm =

1 2
(N − Nm ).
6 m

Hence
)
)
((
7
Nm−1
− Hm−1
3
28
)
7 (
2
Nm−1 (Nm−1 − 1)(Nm−1 − 2) − Nm−1
+ Nm−1
=
168
1
2
=
(N 3
− 4Nm−1
+ 3Nm−1 )
24 m−1
1
=
Nm−1 (Nm−1 − 1)(Nm−1 − 3).
24

Sm =

1
(Nm − 1)(Nm − 3)(Nm − 7). Since each Pk
Substituting Nm−1 = (Nm − 1)/2, gives Sm = 192
algebra has 12 zero-divisors [10] then Zm = 12Sm .

16

## PDF page 17

Deﬁnition (Modes). Calling (19) the prime zero divisor pair then (−d + b)(c + a), is called the
dual of the prime. The terminology dual is appropriate for zero divisors. Also (a′ +b)(c+abs(db)),
with a′ = bc abs(db), is called the extended zero divisor pair, and (− abs(db) + b)(c + a′ ), is called
both extended and dual. These four cases are called modes and whether they are zero divisors
determines another level of structure for the ultronions.
Theorem 11 (Modes theorem). All dual mode transformations swap non-associativity types
between pairs of A, pairs of X and between B and C. All non-cycle extended and extended dual
transformations may act like the dual transformation or as shown in Figure 2. Transformations
of 3-triad cycles are as described in the following table.
Type
AAA
BBA
ACC
XBB
BXC
CAB
CCX
XXX

Related Types
All modes transform like the dual mode to other A types
All modes transform as shown in Figures (a) and (b)
All modes transform as shown in Figures (a) and (c)
All modes transform as shown in Figures (a) and (c)
All modes transform as shown in Figures (a) and (c)
All modes transform as shown in Figures (a) and (c)
All modes transform as shown in Figures (a) and (b)
All modes transform like the dual mode to other X types

X

e

A

C

d

B

C

d

B

d

b b

d

e

b b

e

b

e e

b

X

e

A

C

d

B

C

d

B

(a)

(b)

(c)

Figure 2: Special mode transformations
Proof. The dual mode replaces d with a in the triad (b, c, d) so substituting this into Table 1 we
ﬁnd,
Type 1 associativity [b, d, c] → [b, a, c] which is Type 1 associativity,
Type 2 associativity [b, c, d] → [b, c, a] which is Type 3 associativity (reversed), and
Type 3 associativity [c, b, d] → [c, b, a] which is Type 2 associativity (reversed).
Together these mean under the dual transformation A → A, X → X and B ↔ C and this applies
to all the triad cycles and to dual extended mode as well. Hence, only the extended mode, where
d → abs(db), for all cycles needs to be considered.
For easier traceability, the terminology Ppq is introduced to identify a prime Type p associativity equation for the q th cycle, where p, q ∈ N31 and Epq for the equivalent types and cycles
for the extended modes. Then the Type 1 and Type 3 associativity equations for the ﬁrst and
second cycles are
[b, d, c] = bdc − b(dc) = bdc + dcb,
[c, b, d] = cbd − c(bd) = cbd + bdc, = −bcd − dbc

(P11 )
(P31 )

[b, d, bc] = bd(bc) − b(d(bc)) = bd(bc) − bcdb,
[bc, b, d] = bcbd − bc(bd) = cd − bc(bd).

(P12 )
(P32 )

The extended mode associativity equations that are required are Types 1 and 3 for the ﬁrst and
second cycles and Types 2 and 3 for the third cycle,
[b, abs(db), c] = ±(b(db)c − b(dbc)) = ±(dc − bdcb),
[c, b, abs(db)] = ±(cb(db) − c(b(db))) = ±(bc(bd) − cd),

(E11 )
(E31 )

[b, abs(db), bc] = ±(b(db)(bc) − b(db(bc))) = ±(−bcd − bd(bc)b),
[bc, b, abs(db)] = ±(bcb(db) − bc(b(db))) = ±(−dbc − bcd),

(E12 )
(E32 )

[c, bc, abs(db)] = ±(c(bc)(db) − c(bc(db))) = ±(d − bc(bd)c),
[bc, c, abs(db)] = ±(bcc(db) − bc(c(db))) = ±(−d + bc(dbc)).

(E23 )
(E33 )

17

## PDF page 18

The following equivalences can be identiﬁed. E11 ≡ P11 b, E31 ≡ P32 , E12 ≡ P12 b, E32 ≡ P31 ,
E23 ≡ P32 c and E33 ≡ P31 . The later one is because if (P31 ) is zero then bc(dbc) = (bcd)(bc) =
−d(bc)(bc) = d so that (E33 ) is zero or both are non-zero. This is used in Table 7 to transform
all silos to the extended mode equivalents and to show that this behaves as shown in Figures 2
where ⋆ means non-zero.

Silo
AAA
BBA
ACC
XBB
BXC
CAB
CCX
XXX

Table 7: Extended Mode Transformations
Prime Mode
Extended Mode
P11 P31 P12 P32 E11 E31 E12 E32 E23 E33
⋆
0
⋆
0
⋆
0
⋆
0
0
0
0
0
0
0
0
0
0
0
0
0
⋆
0
0
⋆
⋆
⋆
0
0
⋆
0
⋆
⋆
0
0
⋆
0
0
⋆
0
⋆
0
0
⋆
⋆
0
⋆
⋆
0
⋆
0
0
⋆
⋆
0
0
0
⋆
⋆
0
⋆
0
⋆
0
⋆
0
⋆
0
⋆
⋆
⋆
⋆
⋆
⋆
⋆
⋆
⋆
⋆
⋆
⋆
⋆

Silo
AAA
BBA
XBB
ACC
CAB
BXC
CCX
XXX

It is observed that the non-cycle transformations occur in blocks according to the cycle (b, c)
with d < bc. The A and X transformations for non-cycles act like the dual whereas overlapping
cycle cases may swap types but keep the same number of each type for each cycle.
The deﬁnition of zero divisor pairs required that a2 = b2 and c2 = d2 . For the extended
equation to hold these become a′2 = b2 and c2 = (db)2 , which implies b2 = c2 = −1. Hence for
all subsequent work we assume a2 = b2 = c2 = d2 = ±1 and take b, c and d to be positive blades.
All zero divisor pairs in Table 4 are derived only from the silos that contain A and B nonassociative types. The mode transformations for the AAA silo all act as dual transformation,
which by Figure 2(a) provides other A types. Hence the AAA silo can be reduced by factors of
3 cycles and 4 modes in all ultracomplex algebras. The BBA silo can also be reduced by 3 cycles
but the modes are more complicated. Only the A dual mode and B extended mode generate zero
divisors so modes provide a reduction by two only. It is observed that for the ultronions shown
in Table 4, that for U1 only the AAA silo can provide distinct zero divisor pairs, numbering
28 × 3 = 84.
Cawagas [7] labels the pure sedenions as ei , for i ∈ N16
1 . The graded single, pure elements,
called the basis of S ≡ U1 , have a natural order generated by the Cayley-Dickson process, which
match these in order as
(e1 , e2 , . . . e15 ) = (o1 , o2 , o12 , o3 , o13 , o23 , o123 , o4 , o14 , o24 , o124 , o34 , o134 , o234 , o1234 ).

(22)

The ﬁrst three elements are recognised as the pure quaternions and the ﬁrst seven match the
octonions [4]. Cawagas derives the 84 zero divisor pairs shown in [7] and these are provided in
graded form in Table 8 as b and c columns followed by prime, dual, extended and its dual triads
as d, a, db and ab columns, respectively.
Sedenions are power-associative which means the associator with repeated terms is always
zero, [a, a, a] = 0. This is obvious for an algebra where the single terms square to a scalar and
other than the zero divisor pairs all terms have inverses. Octonions are alternate associative
which means swapping terms of the associator changes the sign or [a, a, b] = [a, b, a] = 0 for all
a, b ∈ O. But sedenions are not alternate associative and demonstrate asymmetric associativity.
For example, the A type from Table 3 is
[o1 , o2 , o34 ] = −o12 o34 − o1 o234 = 0 and
[o1 , o34 , o2 ] = o134 o2 + o1 o234 = −2o1234 .
This example produces the zero divisor pair (o1 − o1234 )(o2 + o34 ) that provides an example of
non-alternate associativity, [a, a, b] ̸= 0 even though [a, b, a] = 0,
[(o1 − o1234 ), (o1 − o1234 ), (o2 + o34 )] = −2o2 − 2o34 and
[(o1 − o1234 ), (o2 + o34 ), (o1 − o1234 )] = 0.
This is because each term is invertible so that (o1 − o1234 )2 = −2 but multiplying the zero divisor
terms ﬁrst gives zero. For U1 , we found above that zero divisors need d = oi4 or d = oij4 or
18

## PDF page 19

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21

b
o1
o1
o1
o1
o1
o1
o2
o2
o2
o2
o2
o12
o12
o12
o12
o3
o3
o3
o13
o13
o23

Table 8: U1 Zero Divisors
c
d
a
db
o2
o34 −o1234
o134
o12
o34
o234
o134
o3
o24
o1234
o124
o13
o24 −o234
o124
o23
o24
o134
o124
o123 o24
−o34
o124
o12
o34 −o134
o234
o3
o14 −o1234 −o124
o13
o14
o234
−o124
o23
o14 −o134 −o124
o123 o14
o34
−o124
o3
o14
o234
o24
o13
o14
o1234
o24
o23
o14
−o34
o24
o123 o14 −o134
o24
o13
o24 −o124 −o234
o23
o14
o124
−o134
o123 o14
−o24
−o134
o23
o14
o24
o34
o123 o14
o124
o34
o123 o24
o124
o34

ab
o234
o1234
−o234
−o1234
o34
o134
o1234
−o134
o34
o1234
−o234
−o134
o34
o1234
−o234
−o1234
o1234
−o234
o1234
−o234
o134

Table 9: AAA Primary Zero Divisors in U1
bc
d
o1 o2
o34
o1 o3
o24
o1 o23 o24
o2 o3
o14
o2 o13 o14
o12 o3 o14
o12 o13 o14
d = o1234 , for i, j ∈ N31 , but b and c do not contain o4 in order to satisfy [c, b, d] = 0. This means
a also contains the o4 generator, satisfying the symmetry required for the dual and other modes.
Sedenions contain 455 ordered triples split into 35 associative and, from Table 4, 84 A nonassociative, 112 C non-associative and 224 X or completely non-associative. Cawagas’s 84 zero
divisor pairs are summarised in AAA 3-triad cycle form in Table 9 which shows the primes only.
Applying the Mode and Cycles Theorems gives twelve zero divisor pairs, applicable for the AAA
silo, over the seven 3-triad cycles generating all 84 zero divisor pairs in Table 8.
Table 10: AAA Primary Zero Divisors in U2 based on O
bc cycle
d
d1
d2
o1 o2
o1 o12
o2 o12
o34 o35 o45
o1 o3
o1 o13
o3 o13
o24 o25 o45
o1 o23
o1 o123
o23 o123 o24 o25 o45
o2 o3
o2 o23
o3 o23
o14 o15 o45
o2 o13
o2 o123
o13 o123 o14 o15 o45
o12 o3
o12 o123
o3 o123 o14 o15 o45
o12 o13
o12 o23
o13 o23 o14 o15 o45
The Cayley-Dickson algebra with ﬁve generators, U2 , has 4495 ordered triples split into 155
associative, 1092 B, 336 A, 1092 C and 1820 X non-associative triads. Now U2 has 1260 zero
divisor pairs because unlike U1 with only AAA 3-triad cycles, Table 4 shows that BBA and ACC
cases are involved. The AAA and BBA silos provide all the zero divisors so that the 84 A types
from the ﬁrst cycle of the ACC silo and the 84 non-cycle A types must overlap with the ﬁrst two
silos. So only the ﬁrst two silos are analysed. What is not documented is that some of the BBA
and AAA cases overlap, in that the same b, c 3-cycle can be included in both silos for diﬀerent d
elements. All these cases will be shown in diﬀerent tables starting with ones based on octonion
19

## PDF page 20

3-cycles. Table 10 shows solutions derived from U1 which used the 4th generator in the d term. It
Table 11: AAA Primary Zero Divisors in U2 independent of O
bc cycle
d1
d2
d3
o1 o4
o1 o14
o4 o14
o25 o35 o235
o2 o4
o2 o24
o4 o24
o15 o35 o135
o12 o4
o12 o124
o4 o124 o15 o35 o135
o3 o4
o3 o34
o4 o34
o15 o25 o125
o13 o4
o13 o134
o4 o134 o15 o25 o125
o23 o4
o23 o234
o4 o234 o15 o25 o125
o123 o4 o123 o1234 o4 o1234 o15 o25 o125
uses the Cycle and Mode Theorems to simplify the 84 zero divisor pairs of U1 to just 7 primaries
and since they are AAA non-associative then all four modes can be derived from column d. The
bc 3-cycles cover all octonion pairs and as mentioned above only the d term contains o4 . This
is extended by U2 to include the 5th generator then both together, o45 , as shown in the d1 and
d2 columns of the table. All of these triads are AAA non-associative with 3-cycle solutions thus
giving three lots of 84 or 252 zero divisor pairs. The remaining AAA cases not based on octonion
3-cycles are provided in Table 11.
Table 12: Overlapping AAA and BBA Primary Zero Divisors in U2
bc cycle
d
d1
d2
o1 o24
o1 o124
o24 o124
o25
o345 o2345
o1 o34
o1 o134
o34 o134
o35
o245 o2345
o1 o234
o1 o1234
o234 o1234 o235 o245
o345
o2 o14
o2 o124
o14 o124
o15
o345 o1345
o2 o34
o2 o234
o34 o234
o35
o145 o1345
o2 o134
o2 o1234
o134 o1234 o135 o145
o345
o12 o14
o12 o24
o14 o24
o15
o345 o1345
o12 o34
o12 o1234
o34 o1234
o35
o145 o1345
o12 o134
o12 o234
o134 o234 o135 o1245 o345
o3 o14
o3 o134
o14 o134
o15
o245 o2345
o3 o24
o3 o234
o24 o234
o25
o145 o1245
o3 o124
o3 o1234
o124 o1234 o125 o145
o245
o13 o14
o13 o34
o14 o34
o15
o245 o1245
o13 o24
o13 o1234
o24 o1234
o25
o145 o1245
o13 o124
o13 o234
o124 o234 o125 o145
o245
o23 o14
o23 o1234
o14 o1234
o15
o245 o1245
o23 o24
o23 o34
o24 o34
o25
o145 o1345
o23 o124
o23 o134
o124 o134 o125 o145
o245
o123 o14
o123 o234
o14 o234
o15
o245 o1245
o123 o24
o123 o134
o24 o134
o25
o145 o1245
o123 o124
o123 o34
o124 o34
o125 o145
o245
Five of the rows can be derived by rotating the bc indices positively and one negatively,
wrapping 1 → 4. The other two rows, o2 o13 → o13 o4 and o12 o13 → o123 o4 , do not follow a
pattern nor do the d columns when compared with Table 10, so such pattern recognition is
ignored. Since Table 11 contains AAA non-associative cycles this gives another 21 × 4 × 3 = 252
zero divisor pairs.
Now all other bc pairs that don’t include o5 can be covered. This involves triads with overlapping AAA and BBA cycles but the AAA cases still have four modes and the BBA have prime
and extended modes only. Table 6 shows that for P12 and P14 the type B triads provide half
of the 12 zero divisors for the algebra. In Table 12 the d column provides the AAA structure
and the d1 and d2 columns the BBA structure. The 21 sets of 3-cycles in Table 12 thus represent 21 × 3 × 4 = 252 zero divisor pairs in the d column and the d1 and d2 columns provide
21 × 3 × 2 = 126 solutions each which means the table provides 252 + 126 × 2 = 504 zero divisor
pairs.
Table 12 can be replicated, apart from the d column, with o4 replaced with o5 in the bc
cycles, as shown in Table 13. The d1 and d2 columns have the same BBA structure and modes

20

## PDF page 21

as Table 12 which represents 21 × 3 × 4 = 252 solutions. Tables 12 and 13 provide the only B
non-associative triads in d1 and d2 columns giving 21 × 3 × 2 × 2 = 252 triads, as expected.
Adding all solutions from Tables 10 through 13 gives 252 + 252 + 504 + 252 = 1260 which is
enumerated in Table 14 under the U2 zero divisors.
Table 13: BBA only Primary Zero Divisors in U2
bc
d1
d2
bc
d1
d2
o1 o25
o345 o2345
o3 o125
o145 o245
o1 o35
o245 o2345
o13 o15
o245 o1245
o1 o235 o245 o345
o13 o25
o145 o245
o2 o15
o345 o1345
o13 o125 o145 o245
o2 o35
o145 o1345
o23 o15
o245 o1245
o2 o135 o145 o345
o23 o25
o145 o1245
o12 o15 o345 o1345
o23 o125 o145 o245
o12 o35 o145 o1345
o123 o15 o245 o1245
o12 o135 o145 o345
o123 o25 o145 o1245
o3 o15
o245 o2345 o123 o125 o145 o245
o3 o25
o145 o1245
Table 14 provides the number of non-associative elements and zero divisors for the ultronions
up to level 10. These are labelled Um where n = m + 3 is the number (of )generators. Each
generator level deﬁnes an algebra with N = 2n − 1 pure basis elements and N3 ordered product
triples. Removing the associative triads and dividing by 28 provides the number of octonion and
pseudo-octonion algebra copies which corresponds with the multiples of 84 zero divisors in the
next level ultracomplex algebra. The zero divisors for U1 correspond to the AAA silo and those
in U2 to all of the triads in the AAA and BBA silos. At higher levels, the silos after the ﬁrst two
have overlapping zero divisors. U3 has new zero divisors from the ACC and XBB silos that need
to be ﬁltered but does not require the BXC silo. U4 , U5 , U6 and U7 add new zero divisors from
the BXC silo and non-cycle triads but not the CAB silo. At these higher levels the overlapping
cycles that can show 2 or even just 1 mode.

Label
O
Õ
U1 ≡ S
Ũ1
U2
U3
U4
U5
U6
U7

5

Table 14: Ultronion Algebras Cardinality
Pure Basis
Non-Associative
Zero Divisors
Size
Triads
28 Factor
Count
84 Factor
7
28
1
0
0
7
28
–
24
–
15
420
15
84
1
15
420
–
180
–
31
4,340
155
1,260
15
63
39,060
1,395
13,020
155
127
330,708
11,811
117,180
1,395
255
2,720,340
97,155
992,124
11,811
511
22,064,980
788,035
8,161,020
97,155
1023
177,736,020 6,347,715 66,194,940
788,035

Split Cayley-Dickson Algebras

Equation (5) can also be deﬁned with a positive number of ǫi = 1 for i ∈ Nn1 . Such unitary
generators are represented as ui with u2i = 1 for i ∈ Nn1 . This provides a mixed sign basis with
elements oα uβ with α, β ∈ B(n) such that α∩β = ∅. Lemma 3 shows that squaring such elements
is −1 for even length of β and is +1 for an odd length. This is now applied to each level of the
graded algebras.
By the binomial theorem, the number of basis elements is the sum over all grades including
the number one, as shown in (2). An enumeration of the binomial theorem is expressed in
Pascal’s triangle that starts as

21

## PDF page 22

1
1
1
1
1

1
2

3
4

1
3

6

1
4

1

and is described by the recurrence relation that each position after the ﬁrst is the sum of the two
elements above. For graded algebras the triangle enumerates Cayley-Dickson algebras starting
with the reals, R. Each row after this is the statement that the number of terms of any k-grade is
given by the number of terms at grade k without the generator on or un plus those that include
this generator from grade k − 1. Pascal’s triangle is horizontally symmetric because for each term
of grade k, the complimentary term with grade n − k contains the same k indices removed from
the n generator case. For n odd there are an equal number of terms with on or un as without
in the( complimentary
terms. For n even the same applies apart from the middle grade k = n/2.
)
n
But n/2
is always even for n even and by the deﬁnition of combinations it distributes the n
generators equally into an even set, half of which contain on or un and the others exclude it. Of
course, the left-hand side has grade k = 0 that speciﬁes the basis number 1 while the right-hand
side, the compliment of 1, has k = n and always contains on or un .
Deﬁnition. The pure trace of the multiplication table for the algebra with n generators is the
sum of the squares of the 2n − 1 pure basis terms, which is −(2n − 1) for Cayley-Dickson algebra
at level n. Thus for octonions this is −7.
Theorem 12 (Trace theorem). The pure trace for all of the split ultracomplex algebras is one,
as it is for split octonions, Õ, split quaternions, H̃, and Lorentz numbers, C̃.
Proof. For any blade oα uβ , α and β from disjoint sets of B(n) then Lemma 3 shows that
(oα uβ )2 = ±1, −1 if β has even length and +1 if β has odd length. Starting at n = 1 the
Lorentz numbers, C̃, have one blade, u1 , so has pure trace one. Split quaternions, H̃, can have
pure basis, {o1 , u2 , o1 u2 } or {u1 , u2 , u12 }, both of which satisfy the theorem. By induction, the
basis at level n − 1 is assumed to have pure trace one and either on or un will multiplying all
basis elements. By the binomial theorem recurrence relation the existing pure basis is doubled by
multiplying all existing basis elements by on and adding the on (multiplication by 1). Extending
each α in this way does not change the parity of β so this doubles the pure trace count and adds
the -1 trace part for on , keeping the pure trace to one.
Now applying the same recurrence relation with un swaps even and odd parities of each β
in the new multiplied terms when excluding the unit, 1. Hence a trace of one at level n − 1 has
terms added with opposite trace parity giving a total parity of zero. But the extra term, un ,
from multiplication by 1, regains the pure trace of one.
Theorem 13 (Split Cayley-Dickson algebras). All Cayley-Dickson algebras with any positive
number of ǫi = −1 for i ∈ Nn1 are isomorphic to each other so may be represented as the
algebra of unitary generators, u1 , u2 , · · · , un , called the split algebra, either C̃, H̃, Õ or Ũm ,
m = n − 3 > 0.
Proof. From Theorem 1, all blades x, y anti-commute, xy = −yx, if x ̸= y, and by Lemma 3
have squares x2 = ±1, positive for an odd number of unitary generators and negative otherwise.
A basis of the algebra is x = oα uβ , such that α ∩ β = ∅, ∀α, β ∈ B(n). By Theorem 12, any
positive number of unitary generators produce a basis with pure trace one. Selecting a set of n
of α + β so that (oα uβ )2 = 1 but the set elements are not all from the split algebra at level n − 1
then from Lemma 1 this set generates the whole of B(n) and the corresponding basis elements
can be relabelled as new generators u′1 , u′2 , . . . , u′n .
The unitary Type 1, Type 2 and Type 3 associativity scheme for triads does not change
from the non-split case because the same sign changes apply to each associativity term. This
means the non-associativity types A, B, C and X are also appropriate but the zero divisors do
change. These start appearing for the split octonions, Õ, which have 12 zero divisor pairs which,
of course, have X-non-associativity. They have dual partners so only six need to be shown with
a partial cyclic structure,
(u1 , u2 , u13 ), (u1 , u12 , u3 ), (u2 , u12 , u3 ),
(u1 , u12 , u123 ), (u2 , u12 , u123 ), (u3 , u13 , u123 ).
22

## PDF page 23

Split octonions have idempotents of the form (1 + uα ) with nilpotents (1 + uα )(1 − uα ) for
α ∈ N31 ∪ {123}. These are derived from the four positive square blades of Õ, u2α = 1 with
u2123 = 1. Each idempotent can be multiplied on the left by the three blades that do not contain
uα , which form a left ideal and gives 16 nilponents. Multiplying by diﬀerent terms of the nilpotent
gives another zero divisor. For example, (1 + u1 ) has (−u2 + u12 )(u3 + u13 ) = 0, which satisﬁes
the deﬁnition for a zero divisor since u12 u3 u13 = −u2 . Hence ideals overlap with zero divisors
for split algebras.
b
u1
u1
u1
u1
u1
u1
u2
u2
u2
u2
u2

Table 15: Split Sedenion Zero Divisors
c
d blades
b
c
d blades
u2 u13 , u14 , −u134 u12 u3 u34 , −u134
u3
u23 , u14 , u124
u12 u13
−u4 , u14
u23
u4 , u24
u12 u4
u34
u4
u24 , u34 , u1234
u12 u14
−u134
u24
−u134 , −u234
u3
u4
u14 , u24
u34
−u234
u3 u14
−u124
u3 u13 , u24 , −u124
u3 u24
−u124
u13
u4 , u14
u13 u4
u24
u4
u14 , u34 , u1234
u13 u14
−u124
u14
−u134 , −u234
u23 u4
u14
u34
u134
u23 u24
−u124

Split sedenions, Ũ1 , have 180 zero divisor pairs derived from 108 X, 48 A and 24 C-nonassociative triads which includes extending the zero divisor to allow for unitary products. Unlike
the split octonions, Ũ1 has a full cyclic structure with correspondence of the d terms for all cycle
triads. The X types have only two modes and not necessarily the dual. The A and C types
either have only the primary mode or all four modes with A type having three such cases and
C have just two. This reduces to the 39 primaries shown in Table 15 and with 21 modes then
the 3 triad cycles for each triad gives the 180 zero divisor pairs for Ũ1 . The d blades shown as
negative in the table require (−a + b)(c + d) for all ﬁrst cycles but some second and third cycles
need the extended dual mode as well. The two exceptions are (u1 , u2 , −u134 ) and (u2 , u3 , −u124 )
which need the extended dual mode with the standard positive zero divisor.
An overlap between split and non-split zero divisors does not occur. The triad (u12 , u13 , u14 )
and its product, u12 u13 u14 = −u1234 , contains terms that are all imaginary, which should be
analogous to the non-split triad (o12 , o13 , o14 ) but this has product +o1234 providing a zero
divisor with opposite parity.

6

Summary

The Cayley-Dickson algebras have been assumed to be symmetric in the permutation of basis elements but this is only valid for hypercomplex numbers. The octonions introduce non-associativity
but in a symmetric form. Using the graded notation provides a rigorous deﬁnition to the order
of basis elements and exposes the asymmetry of the power-associative Cayley-Dickson algebras.
The octonion non-associative triads are alternate, which means swapping basis elements in the
associator changes its sign. The term ultracomplex numbers has been introduced to cover the
case of the associator toggling between zero and non-zero when swapping elements of the associator. This extends the symmetric non-associativity to another three types that exhibit asymmetric
properties in cycles that lead to multiples of 84 zero divisor pairs and modes that, along with
cycles, can reduce these down to 7, if overlap is taken into account. The total number of zero
divisors for each algebra is also derived.
The graded approach also applies to split ultracomplex numbers by showing that, like the hypercomplex case, there is only one split algebra at each level of the Cayley-Dickson construction.
In this case it is convenient to use ǫ = −1 for all generators, which then have positive square
generators, u2i = 1. The convenient symmetry thereafter is that all odd length grades are unitary
and all even grades are imaginary. The non-associativity from the non-split case carries over for
identical indices with identical zero divisors for the imaginary terms whereas the unitary zero
divisors can be related to ideals of the algebra or imaginary zero divisors. Open questions for future work are to establish connections of split zero divisors to ideals, gain further understanding
of how zero divisors aﬀect Malcev algebras, investigate the relationships between the pseudo23

## PDF page 24

octonion algebras and establish why only three of the six are contained in power-associative
algebras.
The author gratefully acknowledges the invaluable assistance and encouragement of James
Chapell, Jacqui Ramagge and Derek Abbott for improving terminology, mathematical understanding and ongoing assistance with the publishing of this article. Acknowledgement is also due
to Maher ben abdessalem, Espirit, Tunisia for communicating a correction to Zm . The author
also acknowledges the support of an Australian Government Research Training Program Scholarship. All of this work was veriﬁed with the use of an octonion/ultronion calculator written in
Python. The github URL for the calculator is
https://github.com/GPWilmot/geoalg.

References
[1] Morton L. Curtis, Abstract Linear Algebra with revisions by P. Place. Springer Science
+Business Media, New York, 1990, ISBN 978-0-387-97263-3.
[2] L. Sorgsepp and J. Lohmus, Binary and Ternary Sedenions, Hadronic J. 4 (1981) pp. 327353.
[3] K. Imaeda and M. Imaeda, Sedenions: Algebra and Analysis, Applied Mathematics and
Computation, 115 Issue 2-3, (2000) pp. 77–88.
[4] J. C. Baez, The Octonions. Bull. Amer. Math. Soc. (N.S.) 39, No.2, 2002, pp. 145–205.
[5] F. R. Harvey, Spinors and Calibrations. Academic Press, San Diego, 1990, ISBN 0-12329650-1.
[6] T. Dray and C. A. Manogue, The geometry of the octonions. World Scientiﬁc Publishing
Co. Pte. Ltd, Singapore, 2015, ISBN 978-9814401814.
[7] R. E. Cawagas, On the structure and zero divisors of the Cayley-Dickson sedenion algebra,
Discussiones Mathematicae, General Algebra and Applications 24, 2004, pp. 251–265.
[8] J. H. Conway and D. A. Smith, On quaternions and octonions : their geometry, arithmetic,
and symmetry. CRC Press LLC, Florida, 2003, ISBN 978-1-56881-134-5.
[9] R. E. Cawagas and S.A.G.Gutierez, The Subloop Structure of the Cayley-Dickson Sedenion
Loop, Journal of the Mathematical Society of the Philippines, 28, Nos 1-3 (2005), pp. 10–20.
[10] G. P. Wilmot, Construction of exception Lie algebra G2 and non-associative algebras using
Cliﬀord algebra, arXiv:2505.06011 [math.RA].
[11] C. Furey, Three generations, two unbroken gauge symmetries, and one eight-dimensional
algebra. Physics Letters B, 2018. 785 pp. 84–89.
[12] C. Furey. SU(3)C ×SU(2)L ×U(1)Y (×U(1)X ) as a symmetry of division algebraic ladder operators, The European Physical Journal C, 78(5):1-–12, 2018.
[13] N. G. Gresnigt, L. Gourlay and A. Varma, Toward a description of three generations of
fermions from the Cayley-Dickson sedenions, Physics of Particles and Nuclei, 2023, 54,
No. 6, pp. 1006-–1010.
[14] N. Gresnigt, A sedenion algebraic representation of three colored fermion generations, Journal of Physics: Conference Series, 2667 (2023) 012061, doi:10.1088/17426596/2667/1/012061.
[15] Q. Tang and J. Tang, Sedenion algebra for three lepton/quark generations and its relations
to SU(5), arxiv:2308.14768.
[16] Q. Tang and J. Tang, Sedenion algebra model as an extension of the standard model and its
link to SU(5), Symmetry in Geometric Mechanics and Mathematical Physics, MDPI Special
Issue, doi:10.3390/sym16050626.
[17] I. R. Porteous, Topological Geometry, Cambridge U. Press, 1981.

24

## PDF page 25

[18] R. H. Bruck, E. Kleinfeld, The structure of alternative division rings, Proc. of the Amer.
Math. Soc., 1951, 2 (6), 1951, p.878-890.
[19] F. Déroche, Islamic Codicology: An Introduction to the Study of Manuscripts in Arabic
Script, London: Al-Furqan Islamic Heritage Foundation, 2006), pp. 65–102.
[20] A. A. Sagle, Malcev algebras, Trans. Amer. Math. Soc. 1961, 101 (3), pp. 426–458.
[21] R. H. Bruck, A survey of binary systems, Reihe: Gruppentheorie, Spinger-Verlag, Berlin
Göttingen-Heidelberg. 1958. DOI 10.1007/978-3-662-35338-7, pp. 65–102.
[22] K. Kunen, Moufang Quasigroups, Journal of Algebra, 183, (1996) pp. 231–234.
[23] P. Vojtěchovský, Toward the classiﬁcation of Moufang loops of order 64, European J. Combin. 27, Issue 3 (2006), pp. 444-460
[24] N. J. A. Sloane and S. Plouﬀe, The Encyclopedia of Integer Sequences, Academic Press, San
Diego, 1995, ISBN 0-12-558630-2.

25
