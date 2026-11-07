Source: see manifest row of the PDF
PDF sha256: 6a4fa6fa366ff88268f004bbf41012687c6f5f74a6107d488156720e7504a3ce
License: Project Gutenberg License (US public domain text)
Language: eng
Fidelity: machine-gated

# Transcription of schafer_1961_nonassociative_algebras_FULL.pdf

Transcription of `schafer_1961_nonassociative_algebras_FULL.pdf` in this directory, 81 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 2-3, 6, 74 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories; pages 1, 4-5, 7-73, 75-81 from the PDF's own text layer (pdftotext version 26.10.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

The Project Gutenberg EBook of An Introduction to Nonassociative Algebras,
by
R. D. Schafer
This eBook is for the use of anyone anywhere at no cost and with
almost no restrictions whatsoever. You may copy it, give it away or
re-use it under the terms of the Project Gutenberg License included
with this eBook or online at www.gutenberg.org

Title: An Introduction to Nonassociative Algebras
Author: R. D. Schafer
Release Date: April 24, 2008 [EBook #25156]
Language: English
Character set encoding: ASCII
*** START OF THIS PROJECT GUTENBERG EBOOK NONASSOCIATIVE ALGEBRAS ***

## PDF page 2



## PDF page 3

AN INTRODUCTION TO
NONASSOCIATIVE ALGEBRAS
R. D. Schafer
MASSACHUSETTS INSTITUTE OF TECHNOLOGY
An Advanced Subject-Matter Institute in Algebra
Sponsored by
The National Science Foundation
<math>Stillwater,\ Oklahoma,\ 1961</math>

## PDF page 4

Produced by David Starner, David Wilson, Suzanne Lybarger and the
Online Distributed Proofreading Team at http://www.pgdp.net

Transcriber’s notes
This e-text was created from scans of the multilithed book
published by the Department of Mathematics at Oklahoma
State University in 1961. The book was prepared for
multilithing by Ann Caskey.
The original was typed rather than typeset, which somewhat
limited the symbols available; to assist the reader we have
here adopted the convention of denoting algebras etc by
fraktur symbols, as followed by the author in his substantially
expanded version of the work published under the same title
by Academic Press in 1966.
Minor corrections to punctuation and spelling and minor
modiﬁcations to layout are documented in the LATEX source.

## PDF page 5

iii

These are notes for my lectures in July, 1961, at the Advanced
Subject Matter Institute in Algebra which was held at Oklahoma State
University in the summer of 1961.
Students at the Institute were provided with reprints of my paper,
Structure and representation of nonassociative algebras (Bulletin of the
American Mathematical Society, vol. 61 (1955), pp. 469–484), together
with copies of a selective bibliography of more recent papers on nonassociative algebras. These notes supplement §§3–5 of the 1955 Bulletin
article, bringing the statements there up to date and providing detailed
proofs of a selected group of theorems. The proofs illustrate a number
of important techniques used in the study of nonassociative algebras.
R. D. Schafer

Stillwater, Oklahoma
July 26, 1961

## PDF page 6



## PDF page 7

I.

Introduction

By common consent a ring R is understood to be an additive
abelian group in which a multiplication is deﬁned, satisfying
(1)

(xy)z = x(yz)

(2)

(x + y)z = xz + yz,

for all x, y, z in R

and
z(x + y) = zx + zy
for all x, y, z in R,

while an algebra A over a ﬁeld F is a ring which is a vector space over
F with
(3)

α(xy) = (αx)y = x(αy)

for all α in F , x, y in A,

so that the multiplication in A is bilinear. Throughout these notes,
however, the associative law (1) will fail to hold in many of the algebraic
systems encountered. For this reason we shall use the terms “ring” and
“algebra” for more general systems than customary.
We deﬁne a ring R to be an additive abelian group with a second
law of composition, multiplication, which satisﬁes the distributive laws
(2). We deﬁne an algebra A over a ﬁeld F to be a vector space over
F with a bilinear multiplication (that is, a multiplication satisfying
(2) and (3)). We shall use the name associative ring (or associative
algebra) for a ring (or algebra) in which the associative law (1) holds.
In the general literature an algebra (in our sense) is commonly
referred to as a nonassociative algebra in order to emphasize that (1)
is not being assumed. Use of this term does not carry the connotation
that (1) fails to hold, but only that (1) is not assumed to hold. If (1)
is actually not satisﬁed in an algebra (or ring), we say that the algebra
(or ring) is not associative, rather than nonassociative.
As we shall see in II, a number of basic concepts which are familiar
from the study of associative algebras do not involve associativity in any
way, and so may fruitfully be employed in the study of nonassociative
algebras. For example, we say that two algebras A and A′ over F are
isomorphic in case there is a vector space isomorphism x ↔ x′ between
them with
(4)

(xy)′ = x′ y ′

for all x, y in A.
1

## PDF page 8

2

INTRODUCTION

Although we shall prove some theorems concerning rings and
inﬁnite-dimensional algebras, we shall for the most part be concerned
with ﬁnite-dimensional algebras. If A is an algebra of dimension n over
F , let u1 , . . . , un be a basis for A over F . Then the bilinear multiplication in A is completely determined by the n3 multiplication constants
γijk which appear in the products
(5)

ui uj =

n
∑

γijk uk ,

γijk in F .

k=1

We shall call the n2 equations (5) a multiplication table, and shall sometimes have occasion to arrange them in the familiar form of such a table:

u1
..
.
ui
..
.
un

u1 . . . uj . . . un
..
.
..
.

...
γijk uk . . .
..
.
..
.

The multiplication table for a one-dimensional algebra A over F is
given by u21 = γu1 (γ = γ111 ). There are two cases: γ = 0 (from which
it follows that every product xy in A is 0, so that A is called a zero
algebra), and γ = 0. In the latter case the element e = γ −1 u1 serves as a
basis for A over F , and in the new multiplication table we have e2 = e.
Then α ↔ αe is an isomorphism between F and this one-dimensional
algebra A. We have seen incidentally that any one-dimensional algebra
is associative. There is considerably more variety, however, among the
algebras which can be encountered even for such a low dimension as
two.
Other than associative algebras the best-known examples of algebras are the Lie algebras which arise in the study of Lie groups. A Lie
algebra L over F is an algebra over F in which the multiplication is
anticommutative, that is,
(6)

x2 = 0

(implying xy = −yx),

and the Jacobi identity
(7)

(xy)z + (yz)x + (zx)y = 0

for all x, y, z in L

## PDF page 9

INTRODUCTION

3

is satisﬁed. If A is any associative algebra over F , then the commutator
(8)
satisﬁes
(6′ )
and
(7′ )

[x, y] = xy − yx
[x, x] = 0
[

]

[

]

[

]

[x, y], z + [y, z], x + [z, x], y = 0.

Thus the algebra A− obtained by deﬁning a new multiplication (8) in
the same vector space as A is a Lie algebra over F . Also any subspace
of A which is closed under commutation (8) gives a subalgebra of A− ,
hence a Lie algebra over F . For example, if A is the associative algebra
of all n × n matrices, then the set L of all skew-symmetric matrices
in A is a Lie algebra of dimension 12 n(n − 1). The Birkhoﬀ-Witt theorem states that any Lie algebra L is isomorphic to a subalgebra of an
(inﬁnite-dimensional) algebra A− where A is associative. In the general
literature the notation [x, y] (without regard to (8)) is frequently used,
instead of xy, to denote the product in an arbitrary Lie algebra.
In these notes we shall not make any systematic study of Lie algebras. A number of such accounts exist (principally for characteristic
0, where most of the known results lie). Instead we shall be concerned
upon occasion with relationships between Lie algebras and other nonassociative algebras which arise through such mechanisms as the derivation algebra. Let A be any algebra over F . By a derivation of A is meant
a linear operator D on A satisfying
(9)

(xy)D = (xD)y + x(yD)

for all x, y in A.

The set D(A) of all derivations of A is a subspace of the associative
algebra E of all linear operators on A. Since the commutator [D, D′ ]
of two derivations D, D′ is a derivation of A, D(A) is a subalgebra of
E− ; that is, D(A) is a Lie algebra, called the derivation algebra of A.
Just as one can introduce the commutator (8) as a new product
to obtain a Lie algebra A− from an associative algebra A, so one can
introduce a symmetrized product
(10)

x ∗ y = xy + yx

in an associative algebra A to obtain a new algebra over F where the
vector space operations coincide with those in A but where multiplication is deﬁned by the commutative product x ∗ y in (10). If one is

## PDF page 10

4

INTRODUCTION

content to restrict attention to ﬁelds F of characteristic not two (as we
shall be in many places in these notes) there is a certain advantage in
writing
(10′ )

x · y = 12 (xy + yx)

to obtain an algebra A+ from an associative algebra A by deﬁning
products by (10′ ) in the same vector space as A. For A+ is isomorphic
under the mapping a → 12 a to the algebra in which products are deﬁned
by (10). At the same time powers of any element x in A+ coincide with
those in A: clearly x · x = x2 , whence it is easy to see by induction on
n that x · x · · · · · x (n factors) = (x · · · · · x) · (x · · · · · x) = xi · xn−i =
1
(xi xn−i + xn−i xi ) = xn .
2
If A is associative, then the multiplication in A+ is not only commutative but also satisﬁes the identity
(11)

(x · y) · (x · x) = x · [y · (x · x)]

for all x, y in A+ .

A (commutative) Jordan algebra J is an algebra over a ﬁeld F in which
products are commutative:
(12)

xy = yx

for all x, y in J,

and satisfy the Jordan identity
(11′ )

(xy)x2 = x(yx2 )

for all x, y in J.

Thus, if A is associative, then A+ is a Jordan algebra. So is any subalgebra of A+ , that is, any subspace of A which is closed under the
symmetrized product (10′ ) and in which (10′ ) is used as a new multiplication (for example, the set of all n × n symmetric matrices). An
algebra J over F is called a special Jordan algebra in case J is isomorphic to a subalgebra of A+ for some associative A. We shall see that
not all Jordan algebras are special.
Jordan algebras were introduced in the early 1930’s by a physicist, P. Jordan, in an attempt to generalize the formalism of quantum
mechanics. Little appears to have resulted in this direction, but unanticipated relationships between these algebras and Lie groups and the
foundations of geometry have been discovered.

## PDF page 11

INTRODUCTION

5

The study of Jordan algebras which are not special depends upon
knowledge of a class of algebras which are more general, but in a certain
sense only slightly more general, than associative algebras. These are
the alternative algebras A deﬁned by the identities
(13)
and
(14)

x2 y = x(xy)

for all x, y in A

yx2 = (yx)x

for all x, y in A,

known respectively as the left and right alternative laws. Clearly any
associative algebra is alternative. The class of 8-dimensional Cayley
algebras (or Cayley-Dickson algebras, the prototype having been discovered in 1845 by Cayley and later generalized by Dickson) is, as we
shall see, an important class of alternative algebras which are not associative.
To date these are the algebras (Lie, Jordan and alternative) about
which most is known. Numerous generalizations have recently been
made, usually by studying classes of algebras deﬁned by weaker identities. We shall see in II some things which can be proved about completely arbitrary algebras.

## PDF page 12

II.

Arbitrary Nonassociative Algebras

Let A be an algebra over a ﬁeld F . (The reader may make the
appropriate modiﬁcations for a ring R.) The deﬁnitions of the terms
subalgebra, left ideal, right ideal, (two-sided) ideal I, homomorphism,
kernel of a homomorphism, residue class algebra A/I (diﬀerence algebra
A − I), anti-isomorphism, which are familiar from a study of associative
algebras, do not involve associativity of multiplication and are thus
immediately applicable to algebras in general. So is the notation BC
for the subspace of A spanned by all products bc with b in B, c in C
(B, C being arbitrary nonempty subsets of A); here we must of course
distinguish between (AB)C and A(BC), etc.
We have the fundamental theorem of homomorphism for algebras:
If I is an ideal of A, then A/I is a homomorphic image of A under the
natural homomorphism
(1)

a → a = a + I,

a in A, a + I in A/I.

Conversely, if A′ is a homomorphic image of A (under the homomorphism
(2)

a → a′ ,

a in A, a′ in A′ ),

then A′ is isomorphic to A/I where I is the kernel of the homomorphism.
If S′ is a subalgebra (or ideal) of a homomorphic image A′ of A,
then the complete inverse image of S′ under the homomorphism (2)—
that is, the set S = {s ∈ A | s′ ∈ S′ }—is a subalgebra (or ideal) of A
which contains the kernel I of (2). If a class of algebras is deﬁned by
identities (as, for example, Lie, Jordan or alternative algebras), then
any subalgebra or any homomorphic image belongs to the same class.
We have the customary isomorphism theorems:
(i) If I1 and I2 are ideals of A such that I1 contains I2 , then
(A/I2 )/(I1 /I2 ) and A/I1 are isomorphic.
(ii) If I is an ideal of A and S is a subalgebra of A, then I ∩ S
is an ideal of S, and (I + S)/I and S/(I ∩ S) are isomorphic.
6

## PDF page 13

ARBITRARY NONASSOCIATIVE ALGEBRAS

7

Suppose that B and C are ideals of an algebra A, and that as a
vector space A is the direct sum of B and C (A = B + C, B ∩ C = 0).
Then A is called the direct sum A = B ⊕ C of B and C as algebras.
The vector space properties insure that in a direct sum A = B ⊕ C the
components b, c of a = b + c (b in B, c in C) are uniquely determined,
and that addition and multiplication by scalars are performed componentwise. It is the assumption that B and C are ideals in A = B ⊕ C
that gives componentwise multiplication as well:
(3) (b1 + c1 )(b2 + c2 ) = b1 b2 + c1 c2 ,

bi in B, ci in C.

For b1 c2 is in both B and C, hence in B ∩ C = 0. Similarly c1 b2 = 0, so
(3) holds, (Although ⊕ is commonly used to denote vector space direct
sum, it has been reserved in these notes for direct sum of ideals; where
appropriate the notation ⊥ has been used for orthogonal direct sum
relative to a symmetric bilinear form.)
Given any two algebras B, C over a ﬁeld F , one can construct an
algebra A over F such that A is the direct sum A = B′ ⊕ C′ of ideals
B′ , C′ which are isomorphic respectively to B, C. The construction of
A is familiar: the elements of A are the ordered pairs (b, c) with b in
B, c in C; addition, multiplication by scalars, and multiplication are
deﬁned componentwise:

(4)

(b1 , c1 ) + (b2 , c2 ) = (b1 + b2 , c1 + c2 ),
α(b, c) = (αb, αc),
(b1 , c1 )(b2 , c2 ) = (b1 c1 , b2 c2 ).

Then A is an algebra over F , the sets B′ of all pairs (b, 0) with b in B
and C′ of all pairs (0, c) with c in C are ideals of A isomorphic respectively to B and C, and A = B′ ⊕ C′ . By the customary identiﬁcation
of B with B′ , C with C′ , we can then write A = B ⊕ C, the direct sum
of B and C as algebras.
As in the case of vector spaces, the notion of direct sum extends to
an arbitrary (indexed) set of summands. In these notes we shall have
occasion to use only ﬁnite direct sums A = B1 ⊕ B2 ⊕ · · · ⊕ Bt . Here
A is the direct sum of the vector spaces Bi , and multiplication in A is
given by
(5) (b1 + b2 + · · · + bt )(c1 + c2 + · · · + ct ) = b1 c1 + b2 c2 + · · · + bt ct

## PDF page 14

8

ARBITRARY NONASSOCIATIVE ALGEBRAS

for bi , ci in Bi . The Bi are ideals of A. Note that (in the case of a
vector space direct sum) the latter statement is equivalent to the fact
that the Bi are subalgebras of A such that
(6)

Bi Bj = 0

for i = j.

An element e (or f ) in an algebra A over F is called a left (or
right) identity (sometimes unity element) in case ea = a (or af = a)
for all a in A. If A contains both a left identity e and a right identity
f , then e = f (= ef ) is a (two-sided) identity 1. If A does not contain
an identity element 1, there is a standard construction for obtaining an
algebra A1 which does contain 1, such that A1 contains (an isomorphic
copy of) A as an ideal, and such that A1 /A has dimension 1 over F .
We take A1 to be the set of all ordered pairs (α, a) with α in F , a in
A; addition and multiplication by scalars are deﬁned componentwise;
multiplication is deﬁned by
(7)

(α, a)(β, b) = (αβ, βa + αb + ab),

α, β in F , a, b in A.

Then A1 is an algebra over F with identity element 1 = (1, 0). The
set A′ of all pairs (0, a) in A1 with a in A is an ideal of A1 which is
isomorphic to A. As a vector space A1 is the direct sum of A′ and
the 1-dimensional space F 1 = {α1 | α in F }. Identifying A′ with its
isomorphic image A, we can write every element of A1 uniquely in the
form α1 + a with α in F , a in A, in which case the multiplication (7)
becomes
(7′ )

(α1 + a)(β1 + b) = (αβ)1 + (βa + αb + ab).

We say that we have adjoined a unity element to A to obtain A1 . (If
A is associative, this familiar construction yields an associative algebra
A1 with 1. A similar statement is readily veriﬁable for (commutative)
Jordan algebras and for alternative algebras. It is of course not true
for Lie algebras, since 12 = 1 = 0.)
Let B and A be algebras over a ﬁeld F . The Kronecker product
B ⊗F A (written B ⊗ A if there is no ambiguity) is the tensor product

B ⊗F A of the vector spaces B, A (so that all elements are sums b ⊗ a,
b in B, a in A, multiplication being deﬁned by distributivity and
(8)

(b1 ⊗ a1 )(b2 ⊗ a2 ) = (b1 b2 ) ⊗ (a1 a2 ),

bi in B, ai in A.

## PDF page 15

ARBITRARY NONASSOCIATIVE ALGEBRAS

9

If B contains 1, then the set of all 1 ⊗ a in B ⊗ A is a subalgebra of
B ⊗ A which is isomorphic to A, and which we can identify with A (similarly, if A contains 1, then B ⊗ A contains B as a subalgebra). If B and
A are ﬁnite-dimensional over F , then dim(B ⊗ A) = (dim B)(dim A).
We shall on numerous occasions be concerned with the case where
B is taken to be a ﬁeld (an arbitrary extension K of F ). Then K does
contain 1, so AK = K ⊗F A contains A (in the sense of isomorphism)
as a subalgebra over F . Moreover, AK is readily seen to be an algebra
over K, which is called the scalar extension of A to an algebra over
K. The properties of a tensor product insure that any basis for A over
F is a basis for AK over K. In case A is ﬁnite-dimensional over F ,
this gives an easy representation for the elements of AK . Let u1 , . . . , un
be any basis for A over F . Then the elements of AK are the linear
combinations
(9)

∑

α i ui

(=

∑

αi ⊗ ui ),

αi in K,

where the coeﬃcients αi in (9) are uniquely determined. Addition and
multiplication by scalars are performed componentwise. For multiplication in AK we use bilinearity and the multiplication table
(10)

ui uj =

∑

γijk uk ,

γijk in F .

The elements of A are obtained by restricting the αi in (9) to elements
of F .
For ﬁnite-dimensional A, the scalar extension AK (K an arbitrary
extension of F ) may be deﬁned in a non-invariant way (without recourse
to tensor products) by use of a basis as above. Let u1 , . . . , un be any
basis for A over F ; multiplication in A is given by the multiplication
table (10). Let AK be an n-dimensional algebra over K with the same
multiplication table (this is valid since the γijk , being in F , are in
K). What remains to be veriﬁed is that a diﬀerent choice of basis for A
over F would yield an algebra isomorphic (over K) to this one. (A noninvariant deﬁnition of the Kronecker product of two ﬁnite-dimensional
algebras A, B may similarly be given.)
For the classes of algebras mentioned in the Introduction (Jordan
algebras of characteristic = 2, and Lie and alternative algebras of arbitrary characteristic), one may verify that algebras remain in the same
class under scalar extension—a property which is not shared by classes
of algebras deﬁned by more general identities (as, for example, in V).

## PDF page 16

10

ARBITRARY NONASSOCIATIVE ALGEBRAS

Just as the commutator [x, y] = xy − yx measures commutativity
(and lack of it) in an algebra A, the associator
(11)

(x, y, z) = (xy)z − x(yz)

of any three elements may be introduced as a measure of associativity
(and lack of it) in A. Thus the deﬁnitions of alternative and Jordan
algebras may be written as
(x, x, y) = (y, x, x) = 0

for all x, y in A

[x, y] = (x, y, x2 ) = 0

for all x, y in A.

and

Note that the associator (x, y, z) is linear in each argument. One identity which is sometimes useful and which holds in any algebra A is
(12)

a(x, y, z) + (a, x, y)z = (ax, y, z) − (a, xy, z) + (a, x, yz)
for all a, x, y, z in A.

The nucleus G of an algebra A is the set of elements g in A which
associate with every pair of elements x, y in A in the sense that
(13)

(g, x, y) = (x, g, y) = (x, y, g) = 0

for all x, y in A.

It is easy to verify that G is an associative subalgebra of A. G is
a subspace by the linearity of the associator in each argument, and
(g1 g2 , x, y) = g1 (g2 , x, y) + (g1 , g2 , x)y + (g1 , g2 x, y) − (g1 , g2 , xy) = 0 by
(13), etc.
The center C of A is the set of all c in A which commute and
associate with all elements; that is, the set of all c in the nucleus G
with the additional property that
(14)

xc = cx

for all x in A.

This clearly generalizes the familiar notion of the center of an associative algebra. Note that C is a commutative associative subalgebra of
A.
Let a be any element of an algebra A over F . The right multiplication Ra of A which is determined by a is deﬁned by
(15)

Ra : x → xa

for all x in A.

## PDF page 17

ARBITRARY NONASSOCIATIVE ALGEBRAS

11

Clearly Ra is a linear operator on A. Also the set R(A) of all right
multiplications of A is a subspace of the associative algebra E of all
linear operators on A, since a → Ra is a linear mapping of A into E.
(In the familiar case of an associative algebra, R(A) is a subalgebra of
E, but this is not true in general.) Similarly the left multiplication La
deﬁned by
(16)

La : x → ax

for all x in A

is a linear operator on A, the mapping a → La is linear, and the set
L(A) of all left multiplications of A is a subspace of E.
We denote by M(A), or simply M, the enveloping algebra of
R(A) ∪ L(A); that is, the (associative) subalgebra of E generated by
right and left multiplications of A. M(A) is the intersection of all
subalgebras of E which contain both R(A) and L(A). The elements

of M(A) are of the form S1 · · · Sn where Si is either a right or left
multiplication of A. We call the associative algebra M = M(A) the
multiplication algebra of A.
It is sometimes useful to have a notation for the enveloping algebra
of the right and left multiplications (of A) which correspond to the
elements of any subset B of A; we shall write B∗ for this subalgebra of

M(A). That is, B∗ is the set of all S1 · · · Sn , where Si is either Rbi ,
the right multiplication of A determined by bi in B, or Lbi . Clearly
A∗ = M(A), but note the diﬀerence between B∗ and M(B) in case B
is a proper subalgebra of A—they are associative algebras of operators
on diﬀerent spaces (A and B respectively).
An algebra A over F is called simple in case 0 and A itself are
the only ideals of A, and A is not a zero algebra (equivalently, in the
presence of the ﬁrst assumption, A is not the zero algebra of dimension
1). Since an ideal of A is an invariant subspace under M = M(A),
and conversely, it follows that A is simple if and only if M = 0 is an
irreducible set of linear operators on A. Since A2 (= AA) is an ideal of
A, we have A2 = A in case A is simple.
An algebra A over F is a division algebra in case A = 0 and the
equations
(17)

ax = b,

ya = b

(a = 0, b in A)

have unique solutions x, y in A; this is equivalent to saying that, for
−1
any a = 0 in A, La and Ra have inverses L−1
a and Ra . Any division

## PDF page 18

12

ARBITRARY NONASSOCIATIVE ALGEBRAS

algebra is simple. For, if I = 0 is merely a left ideal of A, there is an
element a = 0 in I and A ⊆ Aa ⊆ I by (17), or I = A; also clearly
A2 = 0. (Any associative division algebra A has an identity 1, since
(17) implies that the non-zero elements form a multiplicative group. In
general, a division algebra need not contain an identity 1.) If A has
ﬁnite dimension n ≥ 1 over F , then A is a division algebra if and only
if A is without zero divisors (x = 0 and y = 0 in A imply xy = 0),
inasmuch as the ﬁnite-dimensionality insures that La (and similarly
Ra ), being (1–1) for a = 0, has an inverse.
In order to make the observation that any simple ring is actually an
algebra, so the study of simple rings reduces to that of (possibly inﬁnitedimensional) simple algebras, we take for granted that the appropriate
deﬁnitions for rings are apparent and we digress to consider any simple ring R. The (associative) multiplication ring M = M(R) = 0 is
irreducible as a ring of endomorphisms of R. Thus by Schur’s Lemma
the centralizer C′ of M in the ring E of all endomorphisms of R is an
associative division ring. Since M is generated by left and right multiplications of R, C′ consists of those endomorphisms T in E satisfying
Ry T = T Ry , Lx T = T Lx , or
(18)

(xy)T = (xT )y = x(yT )

for all x, y in R.

Hence S, T in C′ imply (xy)ST = ((xS)y) T = (xS)(yT ) = (x(yS)) T =
(xT )(yS). Interchanging S and T , we have (xy)ST = (xy)T S, so that
zST = zT S for all z in R2 = R. That is, ST = T S for all S, T in C′ ;
C′ is a ﬁeld which we call the multiplication centralizer of R. Now the
simple ring R may be regarded in a natural way as an algebra over the
ﬁeld C′ . Denote T in C′ by α, and write αx = xT for any x in R. Then
R is a (left) vector space over C′ . Also (18) gives the deﬁning relations
α(xy) = (αx)y = x(αy) for an algebra over C′ . As an algebra over C′
(or any subﬁeld F of C′ ), R is simple since any ideal of R as an algebra
is a priori an ideal of R as a ring.
Moreover, M is a dense ring of linear transformations on R over
C′ (Jacobson, Lectures in Abstract Algebra, vol. II, p. 274), so we have
proved
Theorem 1. Let R be a simple ring, and M be its multiplication
ring. Then the multiplication centralizer C′ of M is a ﬁeld, and R may
be regarded as a simple algebra over any subﬁeld F of C′ . M is a dense
ring of linear transformations on R over C′ .

## PDF page 19

ARBITRARY NONASSOCIATIVE ALGEBRAS

13

Returning now to any simple algebra A over F , we recall that the
multiplication algebra M(A) is irreducible as a set of linear operators
on the vector space A over F . But (Jacobson, ibid) this means that
M(A) is irreducible as a set of endomorphisms of the additive group of
A, so that A is a simple ring. That is, the notions of simple algebra and
simple ring coincide, and Theorem 1 may be paraphrased for algebras
as
Theorem 1′ . Let A be a simple algebra over F , and M be its
multiplication algebra. Then the multiplication centralizer C′ of M is
a ﬁeld (containing F ), and A may be regarded as a simple algebra over
C′ . M is a dense ring of linear transformations on A over C′ .
Suppose that A has ﬁnite dimension n over F . Then E has dimension n2 over F , and its subalgebra C′ has ﬁnite dimension over F . That
is, the ﬁeld C′ is a ﬁnite extension of F of degree r = (C′ : F ) over F .
Then n = mr, and A has dimension m over C′ . Since M is a dense
ring of linear transformations on (the ﬁnite-dimensional vector space)
A over C′ , M is the set of all linear operators on A over C′ . Hence C′ is
contained in M in the ﬁnite-dimensional case. That is, C′ is the center
of M and is called the multiplication center of A.
Corollary. Let A be a simple algebra of ﬁnite dimension over F ,
and M be its multiplication algebra. Then the center C′ of M is a ﬁeld,
a ﬁnite extension of F . A may be regarded as a simple algebra over C′ .
M is the algebra of all linear operators on A over C′ .
An algebra A over F is called central simple in case AK is simple
for every extension K of F . Every central simple algebra is simple (take
K = F ).
We omit the proof of the fact that any simple algebra A (of arbitrary dimension), regarded as an algebra over its multiplication centralizer C′ (so that C′ = F ) is central simple. The idea of the proof
is to show that, for any extension K of F , the multiplication algebra
M(AK ) is a dense ring of linear transformations on AK over K, and
hence is an irreducible set of linear operators.
Theorem 2. The center C of any simple algebra A over F is either
0 or a ﬁeld. In the latter case A contains 1, the multiplication centralizer
C′ = C∗ = {Rc | c ∈ C}, and A is a central simple algebra over C.

## PDF page 20

14

ARBITRARY NONASSOCIATIVE ALGEBRAS

Proof: Note that c is in the center of any algebra A if and only if
Rc = Lc and [Lc , Ry ] = Rc Ry − Rcy = Ry Rc − Ryc = 0 for all y in A
or, more compactly,
(19)

R c = Lc ,

Rc Ry = Ry Rc = Rcy for all y in A.

Hence (18) implies that
(20)

cT is in C

for all c in C, T in C′ .

For (18) may be written as
(18′ )

Ry T = T Ry = RyT

for all y in A

or, equivalently, as
(18′′ )

Lx T = LxT = T Lx

for all x in A.

Then (18′ ) and (18′′ ) imply RcT = T Rc = T Lc = LcT , together with
RcT Ry = Rc T Ry = Rc RyT = Rc(yT ) = R(cT )y and Ry RcT = Ry Rc T =
Rc Ry T = Rc T Ry (= R(cT )y ), That is, (20) holds. Note also that (19)
implies
(21)

Lx Rc = Rc Lx

for all c in C, x in A.

Since Rc1 Rc2 = Rc1 c2 (ci in C) by (19), the subalgebra C∗ of M(A)
is just C∗ = {Rc | c ∈ C}, and the mapping c → Rc is a homomorphism
of C onto C∗ . Also (19) and (21) imply that Rc commutes with every
element of M so that C∗ ⊆ C′ . Moreover, C∗ is an ideal of the (commutative) ﬁeld C′ since (18′ ) and (20) imply that T Rc = RcT is in C∗ for
all T in C′ , c in C. Hence either C∗ = 0 or C∗ = C ′ .
Now C∗ = 0 implies Rc = 0 for all c in C; hence C = 0. For, if there
is c = 0 in C, then I = F c = 0 is an ideal of A since IA = AI = 0.
Then I = A, A2 = 0, a contradiction.
In the remaining case C∗ = C′ , the identity operator 1A on A is in
′
C = C∗ . Hence there is an element e in C such that Re = Le = 1A , or
ae = ea = a for all a in A; A has a unity element 1 = e. Then c → Rc
is an isomorphism between C and the ﬁeld C′ . A is an algebra over the
ﬁeld C, and as such is central simple.

## PDF page 21

ARBITRARY NONASSOCIATIVE ALGEBRAS

15

For any algebra A over F , one obtains a derived series of subalgebras A(1) ⊇ A(2) ⊇ A(3) ⊇ · · · by deﬁning A(1) = A, A(i+1) = (A(i) )2 . A
is called solvable in case A(r) = 0 for some integer r.
Proposition 1. If an algebra A contains a solvable ideal I, and if
A = A/I is solvable, then A is solvable.
Proof: Since (1) is a homomorphism, it follows that A2 = A2 and
that A(i) = A(i) . Then A(r) = 0 implies A(r) = 0, or A(r) ⊆ I. But
I(s) = 0 for some s, so A(r+s) = (A(r) )(s) ⊆ I(s) = 0. Hence A is
solvable.
Proposition 2. If B and C are solvable ideals of an algebra A,
then B + C is a solvable ideal of A. Hence, if A is ﬁnite-dimensional,
A has a unique maximal solvable ideal N. Moreover, the only solvable
ideal of A/N is 0.
Proof: B + C is an ideal because B and C are ideals. By the second
isomorphism theorem (B + C)/C ∼
= B/(B ∩ C). But B/(B ∩ C) is a
homomorphic image of the solvable algebra B, and is therefore clearly
solvable. Then B + C is solvable by Proposition 1. It follows that,
if A is ﬁnite-dimensional, the solvable ideal of maximum dimension is
unique (and contains every solvable ideal of A). Let N be this maximal
solvable ideal, and G be any solvable ideal of A = A/N. The complete
inverse image G of G under the natural homomorphism of A onto A is
an ideal of A such that G/N = G. Then G is solvable by Proposition 1,
so G ⊆ N. Hence G/N = G = 0.
An algebra A is called nilpotent in case there exists an integer t
such that any product z1 z2 · · · zt of t elements in A, no matter how
associated, is 0. This clearly generalizes the concept of nilpotence as
deﬁned for associative algebras. Also any nilpotent algebra is solvable.
Theorem 3. An ideal B of an algebra A is nilpotent if and only
if the (associative) subalgebra B∗ of M(A) is nilpotent.
Proof: Suppose that every product of t elements of B, no matter
how associated, is 0. Then the same is true for any product of more
than t elements of B. Let T = T1 · · · Tt be any product of t elements
of B∗ . Then T is a sum of terms each of which is a product of at
least t linear operators Si , each Si being either Lbi or Rbi (bi in B).

## PDF page 22

16

ARBITRARY NONASSOCIATIVE ALGEBRAS

Since B is an ideal of A, xS1 is in B for every x in A. Hence xT
is a sum of terms, each of which is a product of at least t elements
in B. Hence xT = 0 for all x in A, or T = 0, B∗ is nilpotent. For
the converse we need only that B is a subalgebra of A. We show by
induction on n that any product of at least 2n elements in B, no matter
how associated, is of the form bS1 · · · Sn with b in B, Si in B∗ . For
n = 1, we take any product of at least 2 elements in B. There is
a ﬁnal multiplication which is performed. Since B is a subalgebra,
each of the two factors is in B: bb1 = bRb1 = bS1 . Similarly in any
product of at least 2n+1 elements of B, no matter how associated,
there is a ﬁnal multiplication which is performed. At least one of the
two factors is a product of at least 2n elements of B, while the other
factor b′ is in B. Hence by the assumption of the induction we have
either b′ (bS1 · · · Sn ) = bS1 · · · Sn Lb′ = bS1 · · · Sn+1 or (bS1 · · · Sn )b′ =
bS1 · · · Sn Rb′ = bS1 · · · Sn+1 , as desired. Hence, if any product S1 · · · St
of t elements in B∗ is 0, any product of 2t elements of B, no matter
how associated, is 0. That is, B is nilpotent.

## PDF page 23

III.

Alternative Algebras

As indicated in the Introduction, an alternative algebra A over F
is an algebra in which
(1)

x2 y = x(xy)

for all x, y in A

(2)

yx2 = (yx)x

for all x, y in A.

and

In terms of associators, (1) and (2) are equivalent to
(1′ )
and
(2′ )

(x, x, y) = 0

for all x, y in A

(y, x, x) = 0

for all x, y in A.

In terms of left and right multiplications, (1) and (2) are equivalent to
(1′′ )
and

L x2 = L x 2

for all x in A

(2′′ )

R x2 = R x 2

for all x in A.

The associator (x1 , x2 , x3 ) “alternates” in the sense that, for any
permutation σ of 1, 2, 3, we have (x1σ , x2σ , x3σ ) = (sgn σ)(x1 , x2 , x3 ).
To establish this, it is suﬃcient to prove
(3)

(x, y, z) = −(y, x, z)

for all x, y, z in A

(4)

(x, y, z) = (z, x, y)

for all x, y, z in A.

and

Now (1′ ) implies that (x + y, x + y, z) = (x, x, z) + (x, y, z) + (y, x, z) +
(y, y, z) = (x, y, z) + (y, x, z) = 0, implying (3). Similarly (2′ ) implies
(x, y, z) = −(x, z, y) which gives (x, z, y) = (y, x, z). Interchanging y
and z, we have (4). The fact that the associator alternates is equivalent
to
(5)

Rx Ry − Rxy = Lxy − Ly Lx = Ly Rx − Rx Ly =
Lx Ly − Lyx = Ry Lx − Lx Ry = Ryx − Ry Rx
17

## PDF page 24

18

ALTERNATIVE ALGEBRAS

for all x, y in A. It follows from (1′′ ), (2′′ ) and (5) that any scalar
extension AK of an alternative algebra A is alternative.
Now (3) and (2′ ) imply
(6)
that is,
(6′ )
or
(6′′ )

(x, y, x) = 0

for all x, y in A;

(xy)x = x(yx)

for all x, y in A,

Lx R x = Rx Lx

for all x in A.

Identity (6′ ) is called the ﬂexible law. All of the algebras mentioned
in the Introduction (Lie, Jordan and alternative) are ﬂexible. The
linearized form of the ﬂexible law is
(6′′′ )

(x, y, z) + (z, y, x) = 0

for all x, y, z in A.

We shall have occasion to use the Moufang identities
(7)
(8)
(9)

(xax)y = x [a(xy)] ,
y(xax) = [(yx)a] x,
(xy)(ax) = x(ya)x

for all x, y, a in an alternative algebra A (where we may write xax unambiguously by (6′ )). Now (xax)y − x [a(xy)] = (xa, x, y) + (x, a, xy) =
(−x, xa, y) − (x, xy, a) = − [x(xa)] y + x [(xa)y] − [x(xy)] a + x [(xy)a] =
−(x2 a)y − (x2 y)a + x [(xa)y + (xy)a] = −(x2 , a, y) − (x2 , y, a) −
x2 (ay) − x2 (ya) + x [(xa)y + (xy)a] = x [−x(ay) − x(ya) + (xa)y +
(xy)a] = x [(x, a, y) + (x, y, a)] = 0, establishing (7). Identity (8) is the
reciprocal relationship (obtained by passing to the anti-isomorphic algebra, which is alternative since the deﬁning identities are reciprocal).
Finally (7) implies (xy)(ax) − x(ya)x = (x, y, ax) + x [y(ax) − (ya)x] =
−(x, ax, y) − x(y, a, x) = −(xax)y + x [(ax)y − (y, a, x)] = −x [a(xy) −
(ax)y + (y, a, x)] = −x [−(a, x, y) + (y, a, x)] = 0, or (9) holds.
Theorem of Artin. The subalgebra generated by any two elements x, y of an alternative algebra A is associative.
Proof: Deﬁne powers of a single element x recursively by x1 = x,
xi+1 = xxi . Show ﬁrst that the subalgebra F [x] generated by a single
element x is associative by proving
(10)

xi xj = xi+j

for all x in A (i, j = 1, 2, 3, . . . ).

## PDF page 25

ALTERNATIVE ALGEBRAS

19

We prove this by induction on i, but shall require the case j = 1:
(11)

xi x = xxi

for all x in A (i = 1, 2, . . . ).

Proving (11) by induction, we have xi+1 x = (xxi )x = x(xi x) =
x(xxi ) = xxi+1 by ﬂexibility and the assumption of the induction. We
have (10) for i = 1, 2 by deﬁnition and (1). Assuming (10) for i ≥ 2, we
have xi+1 xj = (xxi )xj = [x(xxi−1 )] xj = [x(xi−1 x)] xj = x [xi−1 (xxj )] =
x(xi−1 xj+1 ) = xxi+j = xi+j+1 by (11), (7) and the assumption of the
induction. Hence F [x] is associative.
Next we prove that
(12)

xi (xj y) = xi+j y

for all x, y in A (i, j = 1, 2, 3, . . . ).

First we prove the case j = 1:
(13)

xi (xy) = xi+1 y

for all x, y in A (i = 1, 2, 3, . . . ).

The case i = 1 of (13) is given by (1); the case i = 2 is
x (xy) = x [x(xy)] = (xxx)y = x3 y by (1) and (7). Then for i ≥ 2,
write the assumption (13) of the induction with xy for y and i for
i + 1: xi−1 [x(xy)] = xi (xy). Then xi+1 (xy) = (xxi−1 x)(xy) =
x [xi−1 {x(xy)}] = x [xi (xy)] = (xxi x)y = xi+2 y by (7). We have
proved the case j = 1 of (12). Then with xy written for y in (12), the
assumption of the induction is xi+j (xy) = xi [xj (xy)]. It follows that
xi (xj+1 y) = xi [xj (xy)] = xi+j (xy) = xi+j+1 y by (13). Now (12) holds
identically in y. Hence
2

(14)

xi (xj y k ) = (xi xj )y k .

Reciprocally
(15)

(y k xj )xi = y k (xj xi ).

Since the distributive law holds in A, it is suﬃcient now to show that
(16)

(xi y k )xj = xi (y k xj )

in order to show that the subalgebra generated by x, y is associative.
But (14) implies (xi , y k , xj ) = −(xi , xj , y k ) = 0.

## PDF page 26

20

ALTERNATIVE ALGEBRAS

An algebra A over F is called power-associative in case the subalgebra F [x] of A generated by any element x in A is associative. Any
alternative algebra is power-associative; the Theorem of Artin also implies
(17)

R x j = R xj ,

L x j = L xj

for all x in A.

An element x in a power-associative algebra A is called nilpotent in
case there is an integer r such that xr = 0. An algebra (ideal) consisting
only of nilpotent elements is called a nilalgebra (nilideal ).
Theorem 4. Any alternative nilalgebra A of ﬁnite dimension over
F is nilpotent.
Proof: Any subalgebra B of A is generated by a ﬁnite number of
elements (for example, the elements in a basis for B over F ). We prove
by induction on the number of generators of B that B∗ is nilpotent for
all subalgebras B; hence, in particular, for B = A. If B is generated by
one element x, then by (6′′ ) and (17) any T in B∗ is a linear combination
of operators of the form
(18)

R x j1 , L x j2 , R x j3 L x j4

for ji ≥ 1.

Then, if xj = 0, we have T 2j−1 = 0, B∗ is nilpotent. Hence, by the
assumption of the induction, we may take a maximal proper subalgebra
B of A and know that B∗ is nilpotent. But then there exists an element
x not in B such that
(19)

xB∗ ⊆ B.

For B∗r = 0 implies that AB∗r = 0 ⊆ B, and there exists a smallest
integer m ≥ 1 such that AB∗m ⊆ B. If m = 1, take x in A but not in
B; if m > 1, take x in AB∗m−1 but not in B. Then (19) is satisﬁed.
Since B is maximal, the subalgebra generated by B and x is A itself.
It follows from (19) that A = B + F [x] so that M = A∗ = (B + F x)∗ .
Put y = b in (5) for any b in B. Then (19) implies that
(20)

R x R b = R b1 − R b R x , R x L b = L b R x + R b R x − R b2 ,
L x R b = R b L x + L b L x − L b3 , L x L b = L b1 − L b L x

for bi in B. Equations (20) show that, in each product of right and
left multiplications in B∗ and (F x)∗ , the multiplication Rx or Lx may

## PDF page 27

ALTERNATIVE ALGEBRAS

21

be systematically passed from the left to the right of Rb or Lb in a
fashion which, although it may change signs and introduce new terms,
preserves the number of factors from B∗ and does not increase the
number of factors from (F x)∗ . Hence any T in A∗ = (B + F x)∗ may
be written as a linear combination of terms of the form (18) and others
of the form
B1 ,

B 2 Rx m1 ,

B 3 Lx m2 ,

B 4 Rx m3 Lx m4

for Bi in B∗ , mi ≥ 1. Then if B∗r = 0 and xj = 0, we have T r(2j−1) = 0;
for every term in the expansion of T r(2j−1) contains either an uninterrupted sequence of at least 2j − 1 factors from (F x)∗ or at least r factors
Bi . In the latter case the Rx or Lx may be systematically passed from
the left to the right of Bi (as above) preserving the number of factors from B∗ , resulting in a sum of terms each containing a product
B1 B2 · · · Br = 0. Hence every element T of the ﬁnite-dimensional associative algebra A∗ is nilpotent. Hence A∗ is nilpotent (Albert, Structure
of Algebras, p. 23). Hence A is nilpotent by Theorem 3.
Any nilpotent algebra is solvable, and any solvable (power-associative) algebra is a nilalgebra. By Theorem 4 the concepts of nilpotent
algebra, solvable algebra, and nilalgebra coincide for ﬁnite-dimensional
alternative algebras. Hence there is a unique maximal nilpotent ideal
N (= solvable ideal = nilideal) in any ﬁnite-dimensional alternative
algebra A; we call N the radical of A. We have seen that the radical of
A/N is 0.
We say that A is semisimple in case the radical of A is 0, and omit
the proof that any ﬁnite-dimensional semisimple alternative algebra A
is the direct sum A = S1 ⊕ · · · ⊕ St of simple algebras Si . The proof
is dependent upon the properties of the Peirce decomposition relative
to an idempotent e.
An element e of an (arbitrary) algebra A is called an idempotent
in case e2 = e = 0.
Proposition 3. Any ﬁnite-dimensional power-associative algebra,
which is not a nilalgebra, contains an idempotent e (= 0).
Proof: A contains an element x which is not nilpotent. The subalgebra F [x] of A generated by x is a ﬁnite-dimensional associative
algebra which is not a nilalgebra. Then F [x] contains an idempotent e
(= 0) (Albert, ibid), and therefore A does.

## PDF page 28

22

ALTERNATIVE ALGEBRAS

By (1′′ ) and (2′′ ) Le and Re are idempotent operators on A which
commute by (6′′ ) (“commuting projections”). It follows that A is the
vector space direct sum
(21)

A = A11 + A10 + A01 + A00

where Aij (i, j = 0, 1) is the subspace of A deﬁned by
(22)

Aij = {xij | exij = ixij , xij e = jxij }

i, j = 0, 1.

Just as in the case of associative algebras, the decomposition of any
element x in A according to the Peirce decomposition (21) is
(23) x = exe + (ex − exe) + (xe − exe) + (x − ex − xe + exe).
We derive a few of the properties of the Peirce decomposition as follows:
(xij yji )e = (xij , yji , e) + xij (yji e)
= −(xij , e, yji ) + xij (yji e)
= −jxij yji + jxij yji + ixij yji
= ixij yji
and similarly e(xij yji ) = ixij yji , so
(24)

Aij Aji ⊆ Aii ,

i, j = 0, 1.

That is, A11 and A00 are subalgebras of A, while A10 A01 ⊆ A11 ,
A01 A10 ⊆ A00 . Also x11 y00 = (ex11 e)y00 = e [x11 (ey00 )] = 0 by (7), and
similarly y00 x11 = 0. Hence A11 and A00 are orthogonal subalgebras of
A. Similarly Aii Aij ⊆ Aij , Aij Ajj ⊆ Aij , etc.
We wish to deﬁne the class of Cayley algebras mentioned in the
Introduction. We construct these algebras in the following manner.
The procedure works slightly more smoothly if we assume that F has
characteristic = 2, so we make this restriction here although it is not
necessary.
An algebra A with 1 over F is called a quadratic algebra in case
A = F 1 and for each x in A we have
(25)

x2 − t(x)x + n(x)1 = 0,

t(x), n(x) in F .

## PDF page 29

ALTERNATIVE ALGEBRAS

23

If x is not in F 1, the scalars t(x), n(x) in (25) are uniquely determined;
set t(α1) = 2α, n(α1) = α2 to make the trace t(x) linear and the norm
n(x) a quadratic form.
An involution (involutorial anti-isomorphism) of an algebra A is a
linear operator x → x on A satisfying
(26)

xy = y x,

x=x

for all x, y in A.

Here we are concerned with an involution satisfying
(27)

x + x ∈ F 1,

xx(= xx) ∈ F 1

for all x in A.

Clearly (27) implies (25) with
(27′ )

x + x = t(x)1,

xx(= xx) = n(x)1

for all x in A

(since 1 = 1, we have t(α1) = 2α, n(α1) = α2 from (27)).
Let B be an algebra with 1 having dimension n over F and such
that B has an involution x → x satisfying (27). We construct an
algebra A of dimension 2n over F with the same properties and having
B as subalgebra (with 1 ∈ B) as follows: A consists of all ordered pairs
x = (b1 , b2 ), bi in B, addition and multiplication by scalars deﬁned
componentwise, and multiplication deﬁned by
(28)

(b1 , b2 )(b3 , b4 ) = (b1 b3 + µb4 b2 , b1 b4 + b3 b2 )

for all bi in B and some µ = 0 in F . Then 1 = (1, 0) is a unity element
for A, B′ = {(b, 0) | b ∈ B} is a subalgebra of A isomorphic to B,
v = (0, 1) is an element of A such that v 2 = µ1 and A is the vector
space direct sum A = B′ + vB′ of the n-dimensional vector spaces B′ ,
vB′ . Identifying B′ with B, the elements of A are of the form
(29)

x = b1 + vb2

(b1 in B uniquely determined by x),

and (28) becomes
(28′ )

(b1 + vb2 )(b3 + vb4 ) = (b1 b3 + µb4 b2 ) + v(b1 b4 + b3 b2 )

for all bi in B and some µ = 0 in F . Deﬁning
(30)

x = b1 − vb2 ,

## PDF page 30

24

ALTERNATIVE ALGEBRAS

we have xy = y x by (28′ ) since b → b is an involution of B; hence
x → x is an involution of A. Also
x + x = t(x)1,

xx(= xx) = n(x)1

where, for x in (29), we have
n(x) = n(b1 ) − µn(b2 ).

t(x) = t(b1 ),

(31)

Assume that the norm on B is a nondegenerate quadratic form;
that is, the associated symmetric bilinear form
(a, b) = 12 [n(a + b) − n(a) − n(b)]

(32)

(= 21 t(ab))

is nondegenerate (if (a, b) = 0 for all b in B, then a = 0). Then the norm
n(x) on A deﬁned by (31) is nondegenerate. For y = b3 + vb4 implies
that (x, y) = 12 [n(x + y) − n(x) − n(y)] = 12 [n(b1 + b3 ) − µn(b2 + b4 ) −
n(b1 ) + µn(b2 ) − n(b3 ) + µn(b4 )] = (b1 , b3 ) − µ(b2 , b4 ). Hence (x, y) = 0
for all y = b3 + vb4 implies (b1 , b3 ) = µ(b2 , b4 ) for all b3 , b4 in B. Then
b4 = 0 implies (b1 , b3 ) = 0 for all b3 in B, or b1 = 0 since n(b) is
nondegenerate on B; similarly b3 = 0 implies (b2 , b4 ) = 0 (since µ = 0)
for all b4 in B, or b2 = 0. That is, x = 0; n(x) is nondegenerate on A.
When is A alternative? Since A is its own reciprocal algebra, it
is suﬃcient to verify the left alternative law (1′ ), which is equivalent to (x, x, y) = 0 since (x, x, y)[ = (x, t(x)1 − x, y) = −(x, x,]y).
Now (x, x, y) = n(x)y − (b1 + vb2 ) (b1 b3 − µb4 b2 ) + v(b1 b4 − b3 b2 ) =
[

]

[

n(x)y − b1 (b1 b3 ) − µb1 (b4 b2 ) + µ(b1 b4 )b2 − µ(b3 b2 )b2 − v b1 (b1 b4 ) −
]

[

]

b1 (b3 b2 ) + (b1 b3 )b2 − µ(b4 b2 )b2 = n(x)y − n(b1 ) − µn(b2 ) (b3 + vb4 ) −
µ(b1 , b4 , b2 ) − v(b1 , b3 , b2 ) = −µ(b1 , b4 , b2 ) − v(b1 , b3 , b2 ) by a trivial extension of the Theorem of Artin. Hence A is alternative if and only if
B is associative.
The algebra F 1 is not a quadratic algebra, but the identity operator
on F 1 is an involution satisfying (27); also n(α1) is nondegenerate on
F 1. Hence we can use an iterative process (beginning with B = F 1)
to obtain by the above construction algebras of dimension 2t over F ;
these depend completely upon the t nonzero scalars µ1 , µ2 , . . . , µt used
in the successive steps. The norm on each algebra is a nondegenerate
quadratic form. The 2-dimensional algebras Z = F 1 + v1 (F 1) are
either quadratic ﬁelds over F (µ1 a nonsquare in F ) or isomorphic to

## PDF page 31

ALTERNATIVE ALGEBRAS

25

F ⊕ F (µ1 a square in F ). The 4-dimensional algebras Q = Z + v2 Z
are associative central simple algebras (called quaternion algebras) over
F ; any Q which is not a division algebra is (by Wedderburn’s theorem
on simple associative algebras) isomorphic to the algebra of all 2 × 2
matrices with elements in F .
We are concerned with the 8-dimensional algebras C = Q + v3 Q
which are called Cayley algebras over F . Since any Q is associative,
Cayley algebras are alternative. However, no Cayley algebra is associative. For Q is not commutative and there exist q1 , q2 in Q such that
[q1 , q2 ] = 0; hence (v3 , q2 , q1 ) = (v3 q2 )q1 − v3 (q2 q1 ) = v3 [q1 , q2 ] = 0 by
(28′ ). Thus this iterative process of constructing alternative algebras
stops after three steps. The quadratic form n(x) is nondegenerate; also
it permits composition in the sense that
(33)

n(xy) = n(x)n(y)

for all x, y in C.

For n(xy)1 = (xy)(xy) = xyy x = n(y)xx = n(x)n(y)1. Also
(34)

t ((xy)z) = t (x(yz))

for all x, y, z in A.

For (x, y, z) = −(z, y, x) = (z, y, x) implies (xy)z + z(y x) = x(yz) +
(z y)x, so that (34) holds.
Theorem 5. Two Cayley algebras C and C′ are isomorphic if and
only if their corresponding norm forms n(x) and n′ (x′ ) are equivalent
(that is, there is a linear mapping x → xH of C into C′ such that
(35)

n′ (xH) = n(x)

for all x in C;

H is necessarily (1–1) since n(x) is nondegenerate).
Proof: Suppose C and C′ are isomorphic, the isomorphism being
H. Then (25) implies (xH)2 − t(x)(xH) + n(x)1′ = 0 where 1′ = 1H is
the unity element of C′ . But also (xH)2 − t′ (xH)(xH) + n′ (xH)1′ = 0.
Hence [t′ (xH) − t(x)] (xH) + [n(x) − n′ (xH)] 1′ = 0. If x ∈
/ F 1, then
′
′
xH ∈
/ F 1 and n(x) = n (xH). On the other hand n(α1) = α2 =
′
n (α1′ ), and we have (35) for all x in C.
For the converse we need to establish the fact that, if B is a proper
subalgebra of a Cayley algebra C, if B contains the unity element 1
of C, and if (relative to the nondegenerate symmetric bilinear form

## PDF page 32

26

ALTERNATIVE ALGEBRAS

(x, y) deﬁned on C by (32)) B is a non-isotropic subspace of C (that
is, B ∩ B⊥ = 0), then there is a subalgebra A = B + vB (constructed
as above). For the involution x → x on C induces an involution on
B, since b = t(b)1 − b is in B for all b in B. Also B non-isotropic
implies C = B ⊥ B⊥ with B⊥ non-isotropic (Jacobson, Lectures in
Abstract Algebra, vol. II, p. 151; Artin, Geometric Algebra, p. 117).
Hence there is a non-isotropic vector v in B⊥ , n(v) = −µ = 0. Since
t(v) = t(v1) = 2(v, 1) = 0, we have
(36)

v 2 = µ1,

µ = 0 in F .









Now vB ⊆ B⊥ since (34) implies (va, b) = 12 t (va)b = 12 t v(ab) =
(v, ba) = 0 for all a, b in B. Hence B ⊥ vB. Also vB has the same
dimension as B since b → vb is (1–1). Suppose vb = 0; then v(vb) =
v 2 b = µb = 0, implying b = 0. In order to show that A = B ⊥ vB is
the algebra constructed above, it remains to show that
(37)
(38)
(39)

a(vb) = v(ab),
(va)b = b(va),
(va)(vb) = µba

for all a, b in B. Now t(v) = 0 implies v = −v; hence v in B⊥ implies
0 = 2(v, b) = t(vb) = vb + bv = vb − bv, or
(40)

bv = vb

for all b in B.

Hence (v, a, b) + (a, v, b) = 0 = (va)b − v(ab) + (av)b = (va)b − v(ab) +
(va)b − a(vb) = [t(a)1 − a] vb − v(ab), establishing (37). Applying the
involution to b(va) = v(ba), and using (40), we have (38). Finally
(va)(vb) = (va)(bv) = v(ab)v = v 2 (ba) = µba by the Moufang identity
(9). Hence A = B ⊥ B⊥ is the subalgebra speciﬁed. Since B and B⊥
are non-isotropic, so is A. [Remark: we have shown incidentally that
if Q is any quaternion subalgebra containing 1 in a Cayley algebra C,
then Q may be used in the construction of C as C = Q + vQ.]
Now let C and C′ have equivalent norm forms n(x) and n′ (x′ ). Let
B (and B′ ) be as above. If B and B′ are isomorphic under H0 , then
the restrictions of n(x) and n′ (x′ ) to B and B′ are equivalent. Then by
Witt’s theorem (Jacobson, ibid, p. 162; Artin, ibid, p. 121), since n(x)
and n′ (x′ ) are equivalent, the restrictions of n(x) and n′ (x′ ) to B⊥ and

## PDF page 33

ALTERNATIVE ALGEBRAS

27

B′⊥ are equivalent. Choose v in B⊥ with n(v) = 0; correspondingly we
have v ′ in B′⊥ such that n′ (v ′ ) = n(v). Then a + vb → aH0 + v ′ (bH0 ) is
an isomorphism of B ⊥ vB onto B′ ⊥ v ′ B′ by the construction above.
Hence if we begin with B = F 1, B′ = F 1′ , repetition of the process
gives successively isomorphisms between Z and Z′ , Q and Q′ , C and C′ .
A Cayley algebra C is a division algebra if and only if n(x) = 0 for
every x = 0 in C. For x = 0, n(x) = 0 imply xx = n(x)1 = 0, C has
zero divisors. Conversely, if n(x) = 0, then x(xy) = (xx)y = n(x)y for
1
1
1
−1
Lx Lx = 1C , L−1
all y implies n(x)
x = n(x) Lx and similarly Rx = n(x) Rx ;
hence if n(x) = 0 for all x = 0, then C is a division algebra.
[Remark: If F is the ﬁeld of all real numbers, the norm form n(x) =
 2

αi for x = αi ui clearly has the property above. Also there are
alternative algebras F 1, Z, Q, C with this norm form (take µi = −1
at each step). Hence there are real alternative division algebras of
dimensions 1, 2, 4, 8. It has recently been proved (see reference [12]
of the appended bibliography of recent papers) that ﬁnite-dimensional
real division algebras can have only these dimensions. It is not true,
however, that the only ﬁnite-dimensional real division algebras are the
four listed above; they are the only alternative ones. For other examples
of ﬁnite-dimensional real division algebras (necessarily of these speciﬁed
dimensions of course) see reference [23] in the bibliography of the 1955
Bulletin article.]
Corollary. Any two Cayley algebras C and C′ with divisors of zero
are isomorphic.
Proof: Show ﬁrst that C has divisors of zero if and only if there
is w ∈
/ F 1 such that w 2 = 1. For 1 − w = 0, 1 + w = 0 imply
(1 − w)(1 + w) = 1 − w 2 = 0 (note t(w) = 0 implies 1 ± w = 1 ∓ w so
that n(1 ± w) = 0). Conversely, if C has divisors of zero, there exists
x = 0 in C with n(x) = 0. Then x = α1 + u, u ∈ (F 1)⊥ = {u | t(u) = 0}
implies 0 = n(x)1 = xx = (α1 + u)(α1 − u) = α2 1 − u2 . If α = 0, then
w = α−1 u satisﬁes w 2 = 1 (w ∈
/ F 1). If α = 0, then n(u) = 0 so that
u is an isotropic vector in the non-isotropic space (F 1)⊥ . Hence there
exists w in (F 1)⊥ with n(w) = −1 (Jacobson, ibid, p. 154, ex. 3), or
w 2 = t(w)w − n(w)1 = 1 (w ∈
/ F 1).
1
Now let e1 = 2 (1 − w), e2 = 1 − e1 = 12 (1 + w). Then e1 2 = e1 ,
2
e2 = e2 , e1 e2 = e2 e1 = 0 (e1 and e2 are orthogonal idempotents). Also
n(ei ) = 0 for i = 1, 2. Hence every vector in ei C is isotropic since

## PDF page 34

28

ALTERNATIVE ALGEBRAS

n(ei x) = n(ei )n(x) = 0. This means that ei C is a totally isotropic
subspace (ei C ⊆ (ei C)⊥ ). Hence dim(ei C) ≤ 12 dim C = 4 (Jacobson,
p. 170; Artin, p. 122). But x = 1x = e1 x + e2 x for all x in C, so
C = e1 C + e2 C. Hence dim(ei C) = 4, and n(x) has maximal Witt index
= 4 = 12 dim C. Similarly n′ (x′ ) has maximal Witt index = 4. Hence
n(x) and n′ (x′ ) are equivalent (Artin, ibid). By Theorem 5, C and C′
are isomorphic.
Over any ﬁeld F there is a Cayley algebra without divisors of zero
(take µ = 1 so v 2 = 1). This unique Cayley algebra over F is called
the split Cayley algebra over F .
F 1 is both the nucleus and center of any Cayley algebra. Also
any Cayley algebra is simple (hence central simple over F ). (This is
obvious for all but the split Cayley algebra.) For, if I is any nonzero
ideal of C, there is x = 0 in I. But x is contained is some quaternion
subalgebra Q of C. Then Q × Q is an ideal of the simple algebra Q.
Hence 1 ∈ Q = Q × Q ⊆ I, and I = C.
We omit the proof of the fact that the only alternative central simple algebras of ﬁnite dimension which are not associative are Cayley
algebras. (Actually the following stronger result is known: any simple
alternative ring, which is not a nilring and which is not associative, is
a Cayley algebra over its center; in the ﬁnite-dimensional case the restriction eliminating nilalgebras is not required since Theorem 4 implies
that A2 = A for a ﬁnite-dimensional alternative nilalgebra). Hence the
simple components Si in a ﬁnite-dimensional semisimple alternative
algebra are either associative or Cayley algebras over their centers.
The derivation algebra D(C) of any Cayley algebra of characteristic
= 3 is a central simple Lie algebra of dimension 14, called an exceptional
Lie algebra of type G (corresponding to the 14-parameter complex exceptional simple Lie group G2 ). The related subject of automorphisms
of Cayley algebras is studied in [33].

## PDF page 35

IV.

Jordan Algebras

In the Introduction we deﬁned a (commutative) Jordan algebra J
over F to be a commutative algebra in which the Jordan identity
(1)

(xy)x2 = x(yx2 )

for all x, y in J

is satisﬁed. Linearization of (1) requires that we assume F has characteristic = 2; we make this assumption throughout IV. It follows from
(1) and the identities (2), (3) below that any scalar extension JK of a
Jordan algebra J is a Jordan algebra.
Replacing x in
(1′ )

(x, y, x2 ) = 0

for all x, y in J

by x + λz (λ ∈ F ), the coeﬃcient of λ is 0 since F contains at least
three distinct elements, and we have
(2)

2(x, y, zx) + (z, y, x2 ) = 0

for all x, y, z in J.

Replacing x in (2) by x + λw (λ ∈ F ), we have similarly (after dividing
by 2) the multilinear identity
(3) (x, y, wz) + (w, y, zx) + (z, y, xw) = 0

for all w, x, y, z in J.

Recalling that La = Ra since J is commutative, we see that (3) is
equivalent to
(3′ ) [Rx , Rwz ] + [Rw , Rzx ] + [Rz , Rxw ] = 0
for all w, x, z in J
and to
(3′′ ) Rz Rxy − Rz Ry Rx + Ry Rzx − Ry(zx) + Rx Rzy − Rx Ry Rz = 0
for all x, y, z in J.
Interchange x and y in (3′′ ) and subtract to obtain
(4)

[Rz , [Rx , Ry ]] = R(x,z,y) = Rz[Rx ,Ry ]
29

for all x, y, z in J.

## PDF page 36

30

JORDAN ALGEBRAS

Now (4) says that, for all x, y in J, the operator [Rx , Ry ] is a derivation
of J, since the deﬁning condition for a derivation D of an arbitrary
algebra A may be written as
[Rz , D] = RzD

for all z in A.

Our ﬁrst objective is to prove that any Jordan algebra J is powerassociative. As in III we deﬁne powers of x by x1 = x, xi+1 = xxi , and
prove
(5)

xi xj = xi+j

for all x in J.

For any x in J, write Gx = Rx ∪ Rx2 . Then the enveloping algebra
G∗x is commutative, since the generators Rx , Rx2 commute by (1). For
i ≥ 2, we put y = x, z = xi−1 in (3′′ ) to obtain
(6)

Rxi+1 = Rxi−1 Rx2 − Rxi−1 Rx2 − Rx2 Rxi−1 + 2Rx Rxi .

By induction on i we see from (6) that Rxi is in G∗ for i = 3, 4, . . . .
Hence
(7)

R xi R xj = R xj R xi

for i, j = 1, 2, 3, . . .

Then, in a proof of (5) by induction on i, we can assume that xi xj+1 =
xi+j+1 ; then xi+1 xj = (xxi )xj = xRxi Rxj = xRxj Rxi = xj+1 xi = xi+j+1
as desired.
One can prove, by a method similar to the proof of Theorem 4 in
III (only considerably more complicated since the identities involved
are more complicated), that any ﬁnite-dimensional Jordan nilalgebra
is nilpotent. We omit the proof, which involves also a proof of the fact
that
(8)

Rx is nilpotent for any nilpotent x
in a ﬁnite-dimensional Jordan algebra.

As in III, this means that there is a unique maximal nilpotent (= solvable = nil) ideal N which is called the radical of J. Deﬁning J to
be semisimple in case N = 0, we have seen that J/N is semisimple. The proof that any semisimple Jordan algebra S is a direct sum
S = S1 ⊕ · · · ⊕ St of simple Si is quite complicated for arbitrary F ;
we shall use a trace argument to give a proof for F of characteristic 0.

## PDF page 37

JORDAN ALGEBRAS

31

Let e be an idempotent in a Jordan algebra J. Put i = 2 and x = e
in (6) to obtain
(9)

2Re3 − 3Re2 + Re = 0;

that is, f (Re ) = 0 where f (λ) = (λ − 1)(2λ − 1)λ. Hence the minimal
polynomial for Re divides f (λ), and the only possibilities for characteristic roots of Re are 1, 12 , 0 (1 must occur since e is a characteristic
vector belonging to the characteristic root 1: eRe = e2 = e = 0). Also
the minimal polynomial for Re has simple roots. Hence J is the vector
space direct sum
(10)
where
(11)

J = J1 + J1/2 + J0
Ji = {xi | xi e = ixi } ,

i = 1, 1/2, 0.

Taking a basis for J adapted to the Peirce decomposition (10), we see
that Re has for its matrix relative to this basis the diagonal matrix
diag{1, 1, . . . , 1, 1/2, 1/2, . . . , 1/2, 0, 0, . . . , 0} where the number of 1’s
is dim J1 > 0 and the number of 1/2’s is dim J1/2 . Hence
(12)

trace Re = dim J1 + 21 dim J1/2 .

If F has characteristic 0, then trace Re = 0.
A symmetric bilinear form (x, y) deﬁned on an arbitrary algebra
A is called a trace form (associative or invariant symmetric bilinear
form) on A in case
(13)

(xy, z) = (x, yz)

for all x, y, z in A.

If I is any ideal of an algebra A on which such a bilinear form is deﬁned,
then I⊥ is also an ideal of A: for x in I, y in I⊥ , a in A imply that xa
and ax are in I so that (x, ay) = (xa, y) = 0 and (x, ya) = (ya, x) =
(y, ax) = 0 by (13). In particular, the radical A⊥ = {x | (x, y) =
0 for all y ∈ A} of the trace form is an ideal of A.
We also remark that it follows from (13) that (xRy , z) = (x, zLy )
and (xLy , z) = (z, yx) = (zy, x) = (x, zRy ) so that, for right (or left)
multiplications Si determined by bi ,
(14)

(xS1 S2 · · · Sh , y) = (x, ySh′ · · · S2′ S1′ )

## PDF page 38

32

JORDAN ALGEBRAS

where Si′ is the left (or right) multiplication determined by bi ; then, if
B is any subset of A,
(15)

(xT, y) = (x, yT ′ )

for all x, y in A, T in B∗ ,

where T ′ is in B∗ .
Theorem 6. The radical N of any ﬁnite-dimensional Jordan algebra J over F of characteristic 0 is the radical J⊥ of the trace form
(16)

(x, y) = trace Rxy

for all x, y in J.

Proof: Without any assumption on the characteristic of F it follows from (4) that (x, y) in (16) is a trace form: (xy, z) − (x, yz) =
trace R(x,y,z) = 0 since the trace of any commutator is 0. Hence J⊥
is an ideal of J. If J were not a nilideal, then (by Proposition 3) J⊥
would contain an idempotent e (= 0) and, assuming characteristic 0,
(e, e) = trace Re = 0 by (12), a contradiction. Hence J⊥ is a nilideal
and J⊥ ⊆ N. Conversely, if x is in N, then xy is in N for every y in A,
and Rxy is nilpotent by (8). Hence (x, y) = trace Rxy = 0 for all y in
A; that is, x is in J⊥ . Hence N ⊆ J⊥ , N = J⊥ .
Theorem 7. Let A be a ﬁnite-dimensional algebra over F (of arbitrary characteristic) satisfying
(i) there is a nondegenerate (associative) trace form (x, y) deﬁned
on A, and
(ii) I2 = 0 for every ideal I = 0 of A.
Then A is (uniquely) expressible as a direct sum A = S1 ⊕ · · · ⊕ St of
simple ideals Si .
Proof: Let S (= 0) be a minimal ideal of A. Since (x, y) is a trace
form, S⊥ is an ideal of A. Hence the intersection S ∩ S⊥ is either 0
or S, since S is minimal. We show that S totally isotropic (S ⊆ S⊥ )
leads to a contradiction.
For, since S2 = 0 by (ii), we know that the ideal of A generated
by S2 must be the minimal ideal S. Thus S = S2 + S2 M where
M is the multiplication algebra of A. Any element s in S may be

written in the form s = (ai bi )Ti for ai , bi in S, where Ti = Ti′ is
the identity operator 1A or Ti is in M. For every y in A we have by

## PDF page 39

JORDAN ALGEBRAS



33





(15) that (s, y) = ((ai bi )Ti , y) = (ai bi , yTi′ ) = (ai , bi (yTi′ )) = 0
since bi (yTi′ ) ∈ S ⊆ S⊥ . Then s = 0 since (x, y) is nondegenerate;
S = 0, a contradiction. Hence S ∩ S⊥ = 0; that is, S is non-isotropic.
Hence A = S ⊥ S⊥ and S⊥ is non-isotropic. That is, A = S ⊕ S⊥ ,
the direct sum of ideals S, S⊥ , and the restriction of (x, y) to S⊥ is
a nondegenerate (associative) trace form deﬁned on S⊥ . That is, (i)
holds for S⊥ as well as A. Moreover, any ideal of the direct summand
S or S⊥ is an ideal of A; hence S is simple and (ii) holds for S⊥ .
Induction on the dimension of A completes the proof.
Corollary. Any (ﬁnite-dimensional) semisimple Jordan algebra J
over F of characteristic 0 is (uniquely) expressible as a direct sum
J = S1 ⊕ · · · ⊕ St of simple ideals Si .
Proof: By Theorem 6 the (associative) trace form (16) is nondegenerate; hence (i) is satisﬁed. Also any ideal I such that I2 = 0 is
nilpotent; hence I = 0, establishing (ii).
As mentioned above, the corollary is actually true for F of characteristic = 2. What remains then, as far as the structure of semisimple
Jordan algebras is concerned, is a determination of the central simple
algebras. The ﬁrst step in this is to show that every semisimple J
(hence every simple J) has a unity element 1. Again the argument we
use here is valid only for characteristic 0, whereas the theorem is true
in general.
We begin by returning to the Peirce decomposition (10) of any
Jordan algebra J relative to an idempotent e. The subspaces J1 and J0
are orthogonal subalgebras of J which are related to the subspace J1/2
as follows:
(17)

J1/2 J1/2 ⊆ J1 + J0 ,

J1 J1/2 ⊆ J1/2 ,

J0 J1/2 ⊆ J1/2 .

For we may put x = e, z = xi ∈ Ji , y = yj ∈ Jj in (2) to obtain
2i(e, yj , xi ) + (xi , yj , e) = 0, or (1 − 2i) [(xi yj )e − j(xi yj )] = 0, so that
(18)

Ji Jj ⊆ Jj

if i = 1/2.

Hence J1 2 ⊆ J1 , J0 2 ⊆ J0 , J1 J0 = J0 J1 ⊆ J0 ∩ J1 = 0, so J1 and J0 are
orthogonal subalgebras by (18), and also the last two inclusions in (17)
hold. Put x = x1/2 , z = y1/2 , y = w = e in (3) and write x1/2 y1/2 =
a = a1 + a1/2 + a0 to obtain 21 (x1/2 , e, y1/2 ) + (e, e, a) + 12 (y1/2 , e, x1/2 ) =

## PDF page 40

34

JORDAN ALGEBRAS

(e, e, a) = 0. Hence ea − e(ea) = a1 + 12 a1/2 − e(a1 + 12 a1/2 ) =
a1 + 12 a1/2 − a1 − 14 a1/2 = 14 a1/2 = 0. Hence x1/2 y1/2 = a1 + a0 ∈ J1 + J0 ,
establishing (17).
Now
(19)

trace Rb = 0

for all b ∈ J1/2 .

For b in J1/2 implies trace Rb = 2 trace Reb = 2(e, b) = 2(e2 , b) =
2(e, eb) = (e, b) by (16) and (13), so trace Rb = (e, b) = 0. Writing
x = x1 + x1/2 + x0 , y = y1 + y1/2 + y0 in accordance with (10), we have
xy = (x1 y1 + x1/2 y1/2 + x0 y0 ) + (x1 y1/2 + x1/2 y1 + x1/2 y0 + x0 y1/2 ) with
the last term in parentheses in J1/2 by (17). Hence (19) implies that
(20)

(x, y) = trace Rx1 y1 +x1/2 y1/2 +x0 y0 .

Now x1/2 y1/2 = c = c1 + c0 (ci in Ji ) implies trace Rc1 + trace Rc0 =
trace Rc = (x1/2 , y1/2 ) = 2(ex1/2 , y1/2 ) = 2(e, x1/2 y1/2 ) = 2 trace Re(c1 +c0 )
= 2 trace Rc1 , so that trace Rc1 = trace Rc0 . Then (20) may be written
as
(20′ )

(x, y) = trace Rx1 y1 +z0 ,

z0 = 2c0 + x0 y0 in J0 .

In any algebra A over F an idempotent e is called principal in case
there is no idempotent u in A which is orthogonal to e (u2 = u =
0, ue = eu = 0); that is, there is no idempotent u in the subspace
A0 = {x0 | x0 ∈ A, ex0 = x0 e = 0}. In a ﬁnite-dimensional Jordan
algebra J, this means that e is a principal idempotent of J if and only
if the subalgebra J0 (in the Peirce decomposition (10) relative to e) is
a nilalgebra.
Now any ﬁnite-dimensional Jordan algebra J which is not a nilalgebra contains a principal idempotent. For J contains an idempotent e
by Proposition 3. If e is not principal, there is an idempotent u in J0 ,
e′ = e + u is idempotent, and J1,e′ (the J1 relative to e′ ) contains properly J1,e = J1 . For x1 in J1,e implies x1 e′ = x1 (e + u) = x1 e + x1 u = x1 ,
or x1 is in J1,e′ . That is, J1,e ⊆ J1,e′ . But u ∈ J1,e′ , u ∈
/ J1,e . Then
dim J1,e < dim J1,e′ , and this process of increasing dimensions must
terminate, yielding a principal idempotent.
Theorem 8. Any semisimple (hence any simple) Jordan algebra
J of ﬁnite dimension over F of characteristic 0 has a unity element 1.

## PDF page 41

JORDAN ALGEBRAS

35

Proof: J has a principal idempotent e. Then J0 is a nilalgebra, so
that (x, y) = trace Rx1 y1 by (20′ ) since trace Rz0 = 0 by (8). Hence x
in J1/2 + J0 implies x1 = 0, (x, y) = 0 for all y in J, so x is in J⊥ . That
is, J1/2 + J0 ⊆ J⊥ = N = 0, or J = J1 , e = 1.
If J contains 1 and e1 = 1, then e2 = 1 − e1 , is an idempotent,
and the Peirce decompositions relative to e1 and e2 coincide (with differing subscripts). We introduce a new notation: J11 = J1,e1 (= J0,e2 ),
J12 = J1/2,e1 (= J1/2,e2 ), J22 = J0,e1 (= J1,e2 ). More generally, if
1 = e1 + e2 + · · · + et for pairwise orthogonal idempotents ei , we have
the reﬁned Peirce decomposition
(21)

J=

∑

Jij

i≤j

of J as the vector space direct sum of subspaces Jii = J1,ei (1 ≤ i ≤ t),
Jij = J1/2,ei ∩ J1/2,ej (1 ≤ i < j ≤ t); that is,
(22)

Jii = {x | x ∈ J, xei = x},
Jij = Jji = {x | x ∈ J, xei = 21 x = xej },

i = j.

Multiplicative relationships among the Jij are consequences of (17) and
the statement preceding it.
An idempotent e in J is called primitive in case e is the only idempotent in J1 (that is, e cannot be written as the sum e = u + v of
orthogonal idempotents), and absolutely primitive in case it is primitive in any scalar extension JK of J. A central simple Jordan algebra J
is called reduced in case 1 = e1 + · · · + et for pairwise orthogonal absolutely primitive idempotents ei in J. In this case it can be shown that
the subalgebras Jii in the Peirce decomposition (22) are 1-dimensional
(Jii = F ei ) and that the subspaces Jij (i = j) all have the same dimension. If J is a central simple algebra over F , there is a scalar extension
JK which is reduced (for example, take K to be the algebraic closure
of F ), and it can be shown that the number t of pairwise orthogonal
absolutely primitive idempotents ei in JK such that 1 = e1 + · · · + et is
unique; t is called the degree of J.
We list without proof all (ﬁnite-dimensional) central simple Jordan
algebras J of degree t over F of characteristic = 2. Recall from the
Introduction that J is a special Jordan algebra in case J is isomorphic to

## PDF page 42

36

JORDAN ALGEBRAS

a subalgebra of an algebra A+ where A is associative and multiplication
in A+ is deﬁned by
(23)

x · y = 12 (xy + yx).

We say that each algebra is of type A, B, C, D, or E listed below.
AI . J ∼
= A+ with A any central simple associative algebra (necessarily of dimension t2 over F ).
AII . Let A be any involutorial simple associative algebra over F ,
the involution being of the second kind (so that the center Z of A is
a quadratic extension of F and the involution induces a non-trivial
automorphism on Z (Albert, Structure of Algebras, p. 153)). Then
J∼
= H(A), the t2 -dimensional subalgebra of self-adjoint elements in the
2t2 -dimensional algebra A+ . If J is of type AI or AII , and if K is the
algebraic closure of F , then JK ∼
= Kt+ where Kt is the algebra of all
t × t matrices with elements in K.
B, C. Let A be any involutorial central simple associative algebra
over F (so the involution is of the ﬁrst kind). Then J ∼
= H(A), the
+
subalgebra of self-adjoint elements in A . There are two types (B and
C) which may be distinguished by passing to the algebraic closure K
of F , so that AK is a total matrix algebra. In case B the (extended)
involution on AK is transposition (a → a′ ) so that A has dimension
t2 and J has dimension 21 t(t + 1) over F . In
case C)the (extended)
(
0 1t
so that A has
involution on AK is a → g −1 a′ g where g =
−1t 0
dimension 4t2 and J has dimension 2t2 − t over F .
D.
Let (x, y) be any nondegenerate symmetric bilinear form on
a vector space M of dimension n ≥ 2. Then J is the vector space direct
sum J = F 1 + M, multiplication in the (n + 1)-dimensional algebra J
being deﬁned by xy = (x, y)1 for all x, y in M. Here t = 2 (dim J ≥ 3).
E.
The algebra C3 of all 3 × 3 matrices with elements in a Cayley
algebra C over F has the standard involution x → x′ (conjugate transpose). The 27-dimensional subspace H(C3 ) of self-adjoint elements
(24)





ξ1 c b


 c ξ2 a  ,
b a ξ3

ξi in F , a, b, c in C,

## PDF page 43

JORDAN ALGEBRAS

37

is a (central simple) Jordan algebra of degree t = 3 under the multiplication (23) where xy is the multiplication in C3 (which is not associative).
Then J is any algebra such that some scalar extension JK ∼
= H(C3 )K
(= H((CK )3 )).
The possibility of additional algebras of degree 1, mentioned in the
1955 Bulletin article, has been eliminated in reference [32] of the bibliography of more recent papers. The proof involves use of a two-variable
identity which is easily seen to be true for special Jordan algebras. But
any such identity is then true for arbitrary Jordan algebras since it has
been proved that the free Jordan algebra with two generators is special
[71; 38], a result which is false for three generators [9]. The identity in
question is
(25)

{

{aba}2 = a{ba2 b}a

}

for all a, b in J,

where {abc} is deﬁned in a Jordan algebra J by {abc} = (ab)c + (bc)a −
(ac)b, so that {aba} = b(2Ra 2 − Ra2 ). Hence in A+ (A associative) we
have {aba} = 2(b · a) · a − b · a2 = aba, so that {aba}2 = aba2 ba =
{a{ba2 b}a}. Then (25) is satisﬁed in any special Jordan algebra (in
particular, the free Jordan algebra with two generators) and thus in
any Jordan algebra.
Therefore all (ﬁnite-dimensional) separable Jordan algebras are
known, and the Wedderburn decomposition theorem stated in the 1955
Bulletin article is valid without restriction. Some of the computations
employed in the original proof may be eliminated [79].
A central simple Jordan algebra of degree 2 (that is, of type D) is a
commutative quadratic algebra with 1 (a2 − t(a)a + n(a)1 = 0) having
nondegenerate norm form n(a), and conversely. For a = α1 + x, x ∈ M,
implies a2 − t(a)a + n(a)1 = 0 where t(a) = 2α, n(a) = α2 − (x, x),
and n(a) is nondegenerate if and only if (x, y) is.
The algebras of types A, B, C are special Jordan algebras by deﬁnition. An algebra of type D is a subalgebra of A+ , where A is the (associative) Cliﬀord algebra of (x, y) (Artin, Geometric Algebra, p. 186).
But algebras of type E are not special (as we show below), and are
therefore called exceptional central simple Jordan algebras. Exceptional Jordan division algebras exist (over suitable ﬁelds F ; but not,
for example, over a ﬁnite ﬁeld or the ﬁeld of all real numbers) [2]. If an
exceptional central simple Jordan algebra J is not a division algebra,

## PDF page 44

38

JORDAN ALGEBRAS

then it is reduced, and J is isomorphic to an algebra H(C3 , Γ) of selfadjoint elements in C3 under a canonical involution x → Γ−1 x′ Γ where
Γ = diag{γ1 , γ2 , γ3 }, γi = 0 in F . Isomorphism of reduced exceptional
simple Jordan algebras is studied in [8].
The unifying feature in the list of central simple Jordan algebras
above is that, for t > 2, a reduced central simple Jordan algebra is isomorphic to the algebra H(Dt , Γ) deﬁned as follows: D is an alternative
algebra (of dimension 1, 2, 4, or 8) with unity element u and involution
d → d satisfying d + d ∈ F u, dd = n(d)u, n(d) nondegenerate on D; Dt
is the algebra of all t × t matrices with elements in D; Γ = diag{γ1 , γ2 ,
. . . , γt }, γi = 0 in F . Then x → Γ−1 x′ Γ is a canonical involution in Dt ,
and the set H(Dt , Γ) of all self-adjoint elements in Dt is a subalgebra of
+
D+
t (that is, we do not need A associative to deﬁne A by (23)). If D
is associative, then Dt = D ⊗F Ft is associative, and J ∼
= H(Dt , Γ) is a
special Jordan algebra. If D is not associative, then J ∼
= H(Dt , Γ) is not
a Jordan algebra unless t = 3. Hence we have J of type B if D = F 1; J
of type A if D = Z (type AI if Z = F ⊕ F ; type AII if Z is a quadratic
ﬁeld over F ); J of type C if D = Q; J of type E if t = 3 and D = C.
The corresponding dimensions for J are clearly t + 12 t(t − 1)(dim D);
that is, 12 t(t + 1) for type B, t2 for type A, 2t2 − t for type C, and 27
for type E.
Theorem 9. Any central simple Jordan algebra J of type E is
exceptional (that is, is not a special Jordan algebra).
Proof: It is suﬃcient to prove that H(C3 ) is not special. For, if
J were special, then J ∼
= J′ ⊆ A+ with A associative implies JK =
K ⊗J ∼
= K ⊗ J′ ⊆ K ⊗ A+ = (K ⊗ A)+ = AK + so that H((CK )3 ) ∼
= JK
is special, a contradiction.
Suppose that H(C3 ) is special. There is an associative algebra A (of
possibly inﬁnite dimension over F ) such that U is an isomorphism of
H(C3 ) into A+ . For i = 1, 2, 3 deﬁne elements ei in A and 8-dimensional
subspaces
Si = {di | d ∈ C}
of A by
(26)

xU = ξ1 e1 + ξ2 e2 + ξ3 e3 + a1 + b2 + c3

## PDF page 45

JORDAN ALGEBRAS

39

for x in (24); that is, for ξi in F and a, b, c in C. (Note that our notation
is such that we will never use e for an element of C). Then
(27)

S = F e1 + F e2 + F e3 + S1 + S2 + S3 = H(C3 )U

is a 27-dimensional subspace of A. S is a subalgebra of A+ . The
mapping V = U −1 deﬁned on S (not on all of A) is an isomorphism of
S onto H(C3 ):
(28)

(xU · yU )V = x · y

for all x, y in H(C3 ).

For our proof we do not need all of the products in A+ of elements of
S. However, performing the multiplications in H(C3 ), we see that (28)
yields
(29)
(30)
(31)
(32)
(33)

ei 2 = ei (= 0),
ei · ej = 0,
ei · ai = 0,
ei · aj = 12 aj ,
ui 2 = ej + ek ,

i = 1, 2, 3;
i = j;
a in C, i = 1, 2, 3;
a in C, i = j;
i, j, k distinct,

where u is the unity element in C; and
(34)

2ai · bj = (b a)k ,
a, b in C, i, j, k a cyclic permutation of 1, 2, 3.

Now (29) and (30) imply that ei (i = 1, 2, 3) are pairwise orthogonal
idempotents. For A is associative, so ei ej + ej ei = 0 for i = j implies
ei 2 ej + ei ej ei = 0 = ei ej ei + ej ei 2 , or ei ej = ej ei ; hence ei ej = 0 for
i = j. By an identical proof it follows from (31) that
(31′ )

ei ai = ai ei = 0,

i = 1, 2, 3.

For i, j, k distinct, (32) implies ei aj + aj ei = aj = ek aj + aj ek ; then
f aj + aj f = 2aj for the idempotent f = ei + ek . Hence f 2 aj + f aj f =
2f aj , so f aj f = f aj and similarly f aj f = aj f ; that is, f aj = aj f = aj :
(35)

(ei + ek )aj = aj = aj (ei + ek ),

i, j, k distinct.

## PDF page 46

40

JORDAN ALGEBRAS

Also (32) implies ei aj = aj − aj ei , so ei aj ei = aj ei − aj ei 2 = 0:
(36)

i = j.

ei aj ei = 0,

For any a in C, deﬁne
(37)

a′ = e1 a3 u 3

in A.

Then (ab)′ = e1 (ab)3 u3 = e1 (b1 a2 + a2 b1 )u3 = e1 a2 b1 u3 by (34) and
(31′ ). Also (34) implies a3 u1 + u1 a3 = (u a)2 = a2 and
(38)

u2 b3 + b3 u 2 = b1 .

Hence (ab)′ = e1 (a3 u1 + u1 a3 )(u2 b3 + b3 u2 )u3 = e1 a3 u1 (u2 b3 + b3 u2 )u3
by (31′ ). Now b3 u2 u3 = b3 u2 (e1 + e3 )u3 = b3 u2 e1 u3 = (b1 − u2 b3 )e1 u3 =
−u2 b3 e1 u3 = −u2 (e1 + e3 )b3 e1 u3 = −u2 e1 b3 e1 u3 = 0 by (35), (31′ ),
(38), and (36). Also u1 u2 b3 = u1 u2 (e1 + e2 )b3 = u1 u2 e1 b3 = (u3 −
u2 u1 )e1 b3 = u3 e1 b3 by (35), (31′ ), (34). Hence (ab)′ = e1 a3 u1 u2 b3 u3 =
e 1 a 3 u 3 e 1 b 3 u 3 = a′ b ′ .
Clearly the mapping a → a′ is linear; hence it is a homomorphism
of C onto the subalgebra C′ of A consisting of all a′ . Since C is simple,
the kernel of this homomorphism is either 0 or C; in the latter case 0 =
u′ = e1 u3 2 = e1 (e1 + e2 ) = e1 = 0 by (33), and we have a contradiction.
Hence a → a′ is an isomorphism. But C′ is associative, whereas C is
not. Hence H(C3 ) is an exceptional Jordan algebra.
Any central simple exceptional Jordan algebra J over F is a cubic
algebra: for any x in J,
(39)

x3 − T (x)x2 + Q(x)x − N (x)1 = 0,
T (x), Q(x), N (x) in F .

Here x2 x = xx2 (= x3 ) since J is commutative. It is suﬃcient to show
(39) for H(C3 ). But x in (24) implies (39) where
(40)
(41)
(42)

T (x) = ξ1 + ξ2 + ξ3 ,
Q(x) = ξ1 ξ2 + ξ2 ξ3 + ξ3 ξ1 − n(a) − n(b) − n(c)
[

]

= 12 (T (x))2 − T (x2 ) ,

N (x) = ξ1 ξ2 ξ3 − ξ1 n(a) − ξ2 n(b) − ξ3 n(c) + t(abc);

## PDF page 47

JORDAN ALGEBRAS

41

if F has characteristic = 3 (as well as = 2), formula (42) may be written
as
(42′ )

[

]

N (x) = 16 (T (x))3 − 3T (x)T (x2 ) + 2T (x3 ) .

The cubic norm form (42) satisﬁes N ({xyx}) = [N (x)]2 N (y); that is,
N (x) permits a new type of composition [35; 69].
In the 1955 Bulletin article, only passing mention is made in §7
of the relationships between exceptional central simple Jordan algebras J and exceptional simple Lie algebras and groups; relationships
which stem from the fact that the derivation algebra D(J) is a central
simple Lie algebra of dimension 52, called an exceptional Lie algebra
of type F (corresponding to the 52-parameter complex exceptional Lie
group F4 )—a proof of this for F of characteristic = 2 appears in [36]
(characteristic = 2, 3 in [70]). Since 1955 the relationships, including
a characterization of Cayley planes by means of H(C3 , Γ), have been
vigorously exploited [18; 19; 20; 35; 36; 37; 39; 70; 76; 78; 81; 82].

## PDF page 48

V.

Power-associative Algebras

We recall that an algebra A over F is called power-associative in
case the subalgebra F [x] generated by any element x of A is associative.
We have seen that this is equivalent to deﬁning, for any x in A,
x1 = x,

xi+1 = xxi

for i = 1, 2, 3, . . .,

and requiring
(1)

xi xj = xi+j

for i, j = 1, 2, 3, . . .

All algebras mentioned in the Introduction are power-associative (Lie
algebras trivially, since x2 = 0 implies xi = 0 for i = 2, 3, . . . ). We shall
encounter in V new examples of power-associative algebras.
The most important tool in the study of noncommutative powerassociative algebras A is the passage to the commutative algebra A+ .
Let F have characteristic = 2 throughout V; we shall also require that
F contains at least four distinct elements. The algebra A+ is the same
vector space as A over F , but multiplication in A+ is deﬁned by
(2)

x · y = 12 (xy + yx)

for x, y in A,

where xy is the (nonassociative) product in A. If A is power-associative,
then (as in the Introduction) powers in A and A+ coincide, and it follows
that A+ is a commutative power-associative algebra.
Let A be power-associative. Then (2) implies
(3)

x2 x = xx2

for all x in A

(4)

x2 x2 = x(xx2 )

for all x in A.

and

In terms of associators, we have
(3′ )
and
(4′ )

(x, x, x) = 0

for all x in A

(x, x, x2 ) = 0

for all x in A.
42

## PDF page 49

POWER-ASSOCIATIVE ALGEBRAS

43

Also (3) may be written in terms of a commutator as
(3′′ )

[x2 , x] = 0

for all x in A.

Using the linearization process employed in IV, we obtain from (3′′ ),
by way of the intermediate identity
(3′′′ )

2[x · y, x] + [x2 , y] = 0

for all x, y in A,

the multilinear identity
(3m)

[x · y, z] + [y · z, x] + [z · x, y] = 0

for all x, y, z in A.

Similarly, assuming four distinct elements in F , (4) is equivalent to
(4′′ )
to

2(x, x, x · y) + (x, y, x2 ) + (y, x, x2 ) = 0 for all x, y in A,

2(x, y, x · z) + 2(x, z, x · y) + 2(y, x, x · z) + 2(x, x, y · z)
+ 2(z, x, x · y) + (y, z, x2 ) + (z, y, x2 ) = 0
for all x, y, z in A,
and ﬁnally to the multilinear identity
(4′′′ )

(4m)

(x, y, z · w) + (z, y, w · x) + (w, y, x · z)
+(y, x, z · w) + (z, x, w · y) + (w, x, y · z)
+(z, w, x · y) + (x, w, y · z) + (y, w, z · x)
+(w, z, x · y) + (x, z, y · w) + (y, z, w · x) = 0
for all x, y, z, w in A,

where in each row of the formula (4m) we have left one of the four
elements x, y, z, w ﬁxed in the middle position of the associator and
permuted the remaining three cyclically.
We omit the proof of the fact that, if F has characteristic 0, then
identities (3) and (4) are suﬃcient to insure that an algebra is powerassociative; the proof involves inductions employing the multilinear
identities (3m) and (4m). We omit similarly a proof of the fact that,
if F has characteristic = 2, 3, 5, the single identity (4) in a commutative algebra implies power-associativity. One consequence of this latter
fact is that in a number of proofs concerning power-associative algebras

## PDF page 50

44

POWER-ASSOCIATIVE ALGEBRAS

separate consideration has to be given to the characteristic 3 or 5 case
by bringing in associativity of ﬁfth or sixth powers and an assumption
that F contains at least 6 distinct elements. We shall omit these details,
simply by assuming characteristic = 3, 5 upon occasion.
An algebra A over F is called strictly power-associative in case
every scalar extension AK is power-associative. If A is a commutative
power-associative algebra over F of characteristic = 2, 3, 5, then A is
strictly power-associative. The assumption of strict power-associativity
is employed in the noncommutative case, and in the commutative case
of characteristic 3 or 5, when one wishes to use the method of extension
of the base ﬁeld.
Let A be a ﬁnite-dimensional power-associative algebra over F .
Just as in the proofs of Propositions 1 and 2, one may argue that A
has a unique maximal nilideal N, and that A/N has maximal nilideal
0. For if A is a power-associative algebra which contains a nilideal I
such that A/I is a nilalgebra, then A is a nilalgebra. [If x is in A, then
xs = xs = 0 for some s, so that xs = y ∈ I and xrs = (xs )r = y r = 0 for
some r.] Since any homomorphic image of a nilalgebra is a nilalgebra,
it follows from the second isomorphism theorem that, if B and C are
nilideals, then so is B + C. For (B + C)/C ∼
= B/(B ∩ C) is a nilalgebra,
so B + C is. This establishes the uniqueness of N. It follows as in the
proof of Proposition 2 that 0 is the only nilideal of A/N. N is called the
nilradical of A, and A is called semisimple in case N = 0. Of course any
anticommutative algebra (for example, any Lie algebra) is a nilalgebra,
and hence is its own nilradical. Hence this concept of semisimplicity is
trivial for anticommutative algebras.
For the moment let A be a commutative power-associative algebra,
and let e be an idempotent in A. Putting x = e in (4′′ ) and using
commutativity, we have y(2Re 3 − 3Re 2 + Re ) = 0 for all y in A, or
(5)

2Re 3 − 3Re 2 + Re = 0

for any idempotent e in a commutative power-associative algebra A. As
we have seen in the case of Jordan algebras in IV, this gives a Peirce
decomposition
(6)

A = A1 + A1/2 + A0

of A as a vector space direct sum of subspaces Ai deﬁned by
(7)

Ai = {xi | xi e = ixi },

i = 1, 1/2, 0; A commutative.

## PDF page 51

POWER-ASSOCIATIVE ALGEBRAS

45

Now if A is any power-associative algebra, the algebra A+ is a commutative power-associative algebra. Hence we have the Peirce decomposition
(6) where
(7′ )

Ai = {xi | exi + xi e = 2ixi },

i = 1, 1/2, 0.

Put y = z = e in (3m) and let x = xi ∈ Ai as in (7′ ) to obtain
(2i − 1)[xi , e] = 0; that is, xi e = exi if i = 1/2. Hence (7′ ) becomes
(7′′ )

i = 1, 0;
Ai = {xi | exi = xi e = ixi },
A1/2 = {x1/2 | ex1/2 + x1/2 e = x1/2 }

in the Peirce decomposition (6) of any power-associative algebra A.
As we have just seen, the properties of commutative power-associative
algebras may be used (via A+ ) to obtain properties of arbitrary powerassociative algebras.
Let A be a commutative power-associative algebra with Peirce decomposition (6), (7) relative to an idempotent e. Then A1 and A0 are
orthogonal subalgebras of A which are related to A1/2 as follows:

(8)

A1/2 A1/2 ⊆ A1 + A0 ,
A1 A1/2 ⊆ A1/2 + A0 ,
A0 A1/2 ⊆ A1 + A1/2 .

Note that the last two inclusion relations of (8) are weaker than for
Jordan algebras in IV. The proofs are similar to those in IV, and are
given by putting x = e, y = yj ∈ Aj , z = xi ∈ Ai in (4′′′ ). We omit
the details except to note that the characteristic 3 case of orthogonality
requires associativity of ﬁfth powers.
For x ∈ A1 , w ∈ A1/2 , we have wx = (wx)1/2 + (wx)0 ∈ A1/2 + A0
by (8). Then w → (wx)1/2 is a linear operator on A1/2 which we denote
by Sx :
(9)

wSx = (wx)1/2

for x ∈ A1 , w ∈ A1/2 .

If H is the (associative) algebra of all linear operators on A1/2 , then
x → 2Sx is a homomorphism of A1 into the special Jordan algebra H+ ,
for x → Sx is clearly linear and we verify
(10)

Sxy = Sx Sy + Sy Sx

for all x, y in A1

## PDF page 52

46

POWER-ASSOCIATIVE ALGEBRAS

as follows: put x ∈ A1 , y ∈ A1 , z = e, w ∈ A1/2 in (4m) to obtain
(11) e [y(wx) + x(wy) + w(xy)] + w(xy) − 2x(yw) − 2y(xw) = 0,
since e(yw) = 12 (yw)1/2 implies x [e(yw)] = 12 x(yw)1/2 = 12 x(yw) and
y [e(xw)] = 12 y(xw) by interchange of x and y. By taking the A1/2
component in (11), we have (10) after dividing by 3. Similarly, deﬁning
the linear operator Tz on A1/2 for any z in A0 by
(12)
we have
(13)
and
(14)

wTz = (wz)1/2

for z ∈ A0 , w ∈ A1/2 ,

Tzy = Tz Ty + Ty Tz

for all z, y in A0 ,

Sx T z = Tz Sx

for all x in A1 , z in A0 .

This is part of the basic machinery used in developing the structure
theory for commutative power-associative algebras as reported in the
1955 Bulletin article. The result that simple algebras (actually rings)
of degree greater than 2 are Jordan has been extended by the same
technique to ﬂexible power-associative rings (the conclusion being that
A+ is Jordan) [58]. All semisimple commutative power-associative algebras of characteristic 0 are Jordan algebras [51]. The determination
of all simple commutative power-associative algebras of degree 2 and
characteristic p > 0 is still not complete [1; 24].
Here we shall develop only as much of the technique as will be
required in the proof of the following generalization of Wedderburn’s
theorem that every ﬁnite associative division ring is a ﬁeld (Artin, Geometric Algebra, p. 37). In IV it was mentioned that exceptional Jordan
division algebras do exist over suitable ﬁelds F ; however, F cannot be
ﬁnite in that event and we assume this particular case of the following
theorem (as well as Wedderburn’s theorem) in the proof of
Theorem 10. Let D be a ﬁnite power-associative division ring of
characteristic = 2, 3, 5. Then D is a ﬁeld.
For the proof we require an exercise and a lemma.
Exercise. If u and v are orthogonal idempotents in a commutative
power-associative algebra A, then
(15)

Ru Rv = Rv Ru .

## PDF page 53

POWER-ASSOCIATIVE ALGEBRAS

47

(Hint: put x = u, y = v in (4′′′ ) and use (5). After considerable
manipulation, and use of characteristic = 3, 5, this (together with what
one obtains by interchanging u and v) will yield (15).)
Lemma. Let e be a principal idempotent in a commutative powerassociative algebra A (that is, A0 in (7) is a nilalgebra). Then every
element in A1/2 is nilpotent.
Proof: To obtain (18′ ) below, one does not need to assume that e
is principal. For any w ∈ A1/2 put x = w, y = e in (4′′ ) to obtain
(16)

w3 − w(ew2 ) − ew 3 = 0

for w in A1/2

Let x = (w 2 )1 ∈ A1 , z = (w 2 )0 ∈ A0 , so that w 2 = x + z, ew 2 = x,
w(ew2 ) = wx = (wx)1/2 + (wx)0 . Also w 3 = wx + wz = (wx)1/2 +
(wx)0 + (wz)1/2 + (wz)1 so that ew 3 = 12 (wx)1/2 + 12 (wz)1/2 + (wz)1 .
Then (16) implies (wx)1/2 = (wz)1/2 , or
(17)

wSx = wTz

for any w in A1/2

where w2 = x + z, x = (w 2 )1 , z = (w 2 )0 . Now
(18)

wSx k = wTz k

for k = 1, 2, 3, . . .

For (17) is the case k = 1 of (18) and, assuming (18), we have wSx k+1 =
wSx k Sx = wTz k Sx = wSx Tz k = wTz k+1 by (14). But (10) and (13)
imply Sxk = 2k−1 Sx k , Tzk = 2k−1 Tz k , so (18) yields
(18′ )

wSxk = wTzk

for k = 1, 2, 3, . . .

where w is any element of A1/2 and w2 = x + z, x ∈ A1 , z ∈ A0 .
Now let e be a principal idempotent in A. Then every element w
in A1/2 is nilpotent. For z = (w2 )0 is nilpotent, and z k = 0 for some k.
By (18′ ) we have w 2k+1 = w(w 2 )k = w(x + z)k = w(xk + z k ) = wxk =
(wxk )1/2 + (wxk )0 = wSxk + (wxk )0 = (wxk )0 in A0 is nilpotent; hence
w is nilpotent.
We use the Lemma to prove that any ﬁnite-dimensional powerassociative division algebra D over a ﬁeld F has a unity element 1.
For D+ is a (ﬁnite-dimensional) commutative power-associative algebra without nilpotent elements = 0, so D+ contains a principal idempotent e (as in IV, D+ contains an idempotent e; if e is not principal,

## PDF page 54

48

POWER-ASSOCIATIVE ALGEBRAS

+
′
there is an idempotent u ∈ D+
0 = D0,e , e = e + u is idempotent,
+
dim D+
1,e < dim D1,e′ , and the increasing dimensions must terminate).
By the Lemma, since 0 is the only nilpotent element in D+ , we have
+
+
+
+
′′
D+
1/2 = D0 = 0, D = D1 , e is a unity element for D . By (7 ) e is a
unity element for D.

Proof of Theorem 10: We are assuming that D is a ﬁnite powerassociative division ring. We have seen in II that this means that D
is a (ﬁnite-dimensional) division algebra over a (ﬁnite) ﬁeld. Hence we
have just seen that D has a unity element 1, so that D is an algebra over
its center. Thus we may as well take D to be an algebra over its center
F , a ﬁnite ﬁeld. Hence F is perfect (Zariski-Samuel, Commutative
Algebra, vol. I, p. 65).
Now D+ is a Jordan algebra over F . For let x, y be any elements
of D+ . If x ∈ F 1, the Jordan identity
(19)

(x · y) · x2 = x · (y · x2 )

for all x, y in D+

holds trivially. Otherwise the (commutative associative) subalgebra
F [x] of D+ is a ﬁnite (necessarily separable) extension of F , so there
is an extension K of F such that F [x]K = K ⊕ K ⊕ · · · ⊕ K, x is a
linear combination x = ξ1 e1 + ξ2 e2 + · · · + ξn en of pairwise orthogonal
idempotents ei in F [x]K ⊆ (D+ )K with coeﬃcients in K. In order to
establish (19), it is suﬃcient to establish
(19′ )

(ei · y) · (ej · ek ) = ei · [y · (ej · ek )] ,

i, j, k = 1, . . . , n.

For j = k, (19′ ) is obvious; for j = k, (19′ ) reduces to (15).
Now the radical of D+ (consisting of nilpotent elements) is 0. Although our proof of the Corollary to Theorem 7 is valid only for characteristic 0, we remarked in IV that the conclusion is valid for characteristic = 0. Hence D+ is a direct sum S1 ⊕ · · · ⊕ Sr of r simple
ideals Si , each with unity element ei . The existence of an idempotent
e = 1 in D+ is suﬃcient to give zero divisors in D, a contradiction,
since the product e(1 − e) = 0 in D. Hence r = 1 and D+ is a simple Jordan algebra over F . Let C be the center of D+ . Then C is a
ﬁnite separable extension of F , C = F [z], z ∈ C (Zariski-Samuel, ibid,
p. 84). If D+ = C = F [z], then D = F [z] is a ﬁeld, and the theorem
is established. Hence we may assume that D+ = C, so D+ is a central
simple Jordan algebra of degree t ≥ 2 over the ﬁnite ﬁeld C and is

## PDF page 55

POWER-ASSOCIATIVE ALGEBRAS

49

of one of the types A–E listed in IV. We are assuming that type E is
known not to occur. The other types are eliminated as follows.
Wedderburn’s theorem implies that, over any ﬁnite ﬁeld, there are
no associative central division algebras of dimension > 1. Hence, by
Wedderburn’s theorem on simple associative algebras, every associative
central simple algebra over a ﬁnite ﬁeld is a total matric algebra. Thus
we have the following possibilities:
AI . D + ∼
= Ct + , t ≥ 2. Then Ct + contains an idempotent e11 = 1,
a contradiction.
AII . D+ is the set H(Zt ) of self-adjoint elements in Zt , Z a
quadratic extension of C, where the involution may be taken to be
a → g −1 a′ g with g a diagonal matrix. Hence H(Zt ) contains e11 = 1, a
contradiction.
B.
D+ ∼
= H(Ct ), the involution being a → g −1 a′ g with g diagonal; hence H(Ct ) contains e11 = 1, a contradiction.
(

C.

)D

+

∼
= H(C2t ), the involution being a → g −1 a′ g, g =

0 1t
; H(C2t ) contains the idempotent e11 + et+1,t+1 = 1, a
−1t 0
contradiction.

There remains the possibility that D+ might be of type D (where
the dimension is necessarily ≥ 3). The basis u1 , . . . , un for M may
be normalized so that (ui , uj ) = 0 for i = j, (ui , ui ) = αi = 0 in C;
that is, ui 2 = αi 1, ui · uj = 0 for i = j. Each of the ﬁelds C[ui ] is
a quadratic extension of C. But in the sense of isomorphism there is
only one quadratic extension of the ﬁnite ﬁeld C (Zariski-Samuel, ibid,
pp. 73, 83); hence all αi may be taken to be the same nonsquare α in
C. Let β be any element of C. Then w = βu1 + u2 ∈
/ F 1 implies F [w]
is isomorphic to F [u1 ], so w2 = (β 2 + 1)α1 = γ 2 α1, γ in C; that is, for
any β ∈ C, there is γ ∈ C satisfying
(20)

γ 2 = β 2 + 1.

Now let P be the prime ﬁeld of characteristic p contained in C. It
follows from (20) that all elements in P are squares of elements in C.
For 1 (also 0) satisﬁes this condition, and it follows by induction from
(20) that all elements in P do. In particular, −1 = β 2 for some β ∈ C.
Then w2 = (βu1 + u2 )2 = 0, a contradiction.

## PDF page 56

50

POWER-ASSOCIATIVE ALGEBRAS

Theorem 11. Let A be a ﬁnite-dimensional power-associative algebra over F satisfying the following conditions:
(i)
(ii)
(iii)

there is an (associative) trace form (x, y) deﬁned on A;
(e, e) = 0
for any idempotent e in A;
(x, y) = 0
if x · y is nilpotent, x, y in A.

Then the nilradical N of A coincides with the nilradical of A+ , and is the
radical A⊥ of the trace form (x, y). The semisimple power-associative
algebra S = A/N satisﬁes (i)–(iii) with (x, y) nondegenerate. For any
such S we have
(a)
(b)

S = S1 ⊕ · · · ⊕ St for simple Si ;
S is ﬂexible.

If F has characteristic = 5, then
(c)
(d)

S+ is a semisimple Jordan algebra;
S+
i is a simple (Jordan) algebra, i = 1, . . . , t.

Proof: By (i) we know from IV that A⊥ is an ideal of A. If there
were an idempotent e in A⊥ , then (ii) would imply (e, e) = 0, a contradiction. Hence A⊥ is a nilideal: A⊥ ⊆ N. Conversely, x in N implies
x · y is in N for all y in A, so that (x, y) = 0 for all y in N by (iii), or
x is in A⊥ . Hence N ⊆ A⊥ , N = A⊥ . Any ideal of A is clearly an ideal
of A+ ; hence any nilideal of A is a nilideal of A+ , and N is contained
in the nilradical N1 of A+ . But x in N1 implies x · y is in N1 for all y
in A+ , or (x, y) = 0 by (iii) and we have N1 ⊆ A⊥ = N.
Now (x, y) induces a nondegenerate symmetric bilinear form (x, y)
on A/A⊥ = A/N where x = x + N, etc.; that is, (x, y) = (x, y).
Then (x y, z) = (xy, z) = (xy, z) = (x, yz) = (x, y z), so (x, y) is a
trace form. To show (ii) we take any idempotent e in A/N and use
the power-associativity of A to “lift” the idempotent to A: F [e] is a
subalgebra of A which is not a nilalgebra, so there is an idempotent
u ∈ F [e] ⊆ F e + N, and u = e. Then (e, e) = (u, u) = (u, u) = 0.
Suppose x · y = x · y is nilpotent. Then some power of x · y is in N,
x · y is nilpotent, and (x, y) = (x, y) = 0, establishing (iii).
Now let S satisfy (i)–(iii) with (x, y) nondegenerate. Then the
nilradical of S is 0, and the hypotheses of Theorem 7 apply. For if

## PDF page 57

POWER-ASSOCIATIVE ALGEBRAS

51

I2 = 0 for an ideal I of S, then I is a nilideal, I = 0. We have
S = S1 ⊕ · · · ⊕ St for simple Si ; also we know that the Si are not
nilalgebras (for then they would be nilideals of S), but this will follow
from (d).
Now (3′′′ ) implies that a · z = 0 where a = 2[x · y, x] + [x2 , y].
Since a · z is nilpotent, (iii) implies (a, z) = ((xy)x, z) + ((yx)x, z) −
(x(xy), z) − (x(yx), z) + (x2 y, z) − (yx2 , z) = 0 for all x, y, z in S. The
properties of a trace form imply that
(21)

(xy + yx, xz − zx) = (x2 , zy − yz).

Interchange z and y to obtain (xz + zx, xy − yx) = (x2 , yz − zy) =
(xy + yx, zx − xz) by (21). Add (xy + yx, xz + zx) to both sides of
this to obtain (xy, xz + zx) = (xy + yx, zx). Then (xy, xz) = (yx, zx),
so that
(22)

((xy)x, z) = (x(yx), z)

for all x, y, z in S.

Since (x, y) is nondegenerate on S, (22) implies (xy)x = x(yx); that
is, S is ﬂexible.
To prove (c) we note ﬁrst that (x, y) is a trace form on S+ :
(23)

(x · y, z) = (x, y · z)

for all x, y, z in S.

Also it follows from (23), just as in formula (14) of IV, that
(24)

(yS1 S2 · · · Sh , z) = (y, zSh · · · S2 S1 )

where Si are right multiplications of the commutative algebra S+ . In
the commutative power-associative algebra S+ formula (4′′ ) becomes
(25)

4x2 · (x · y) − 2x · [x · (x · y)] − x · (y · x2 ) − y · x3 = 0.

Applying the same procedure as above, we write a for the left side of
(25), have a · z = 0 for all z in S+ , so (iii) implies 4 (x2 · (x · y), z) −
2 (x · [x · (x · y)] , z) − (x · (y · x2 ), z) − (y · x3 , z) = 0 or
(26) (y · z, x3 ) + 2 (x · [x · (x · y)], z) = 4(x · y, x2 · z) − (y · x2 , x · z).
By (24) the left-hand side of (26) is unaltered by interchange of y and
z. Hence 4(x · y, x2 · z) − (y · x2 , x · z) = 4(x · z, x2 · y) − (z · x2 , x · y) so

## PDF page 58

52

POWER-ASSOCIATIVE ALGEBRAS

that (after dividing by 5) we have (x · y, x2 · z) = (y · x2 , x · z). Hence
((x · y) · x2 , z) = (x · (y · x2 ), z) for all z in S, or (x · y) · x2 = x · (y · x2 ),
S+ is a Jordan algebra. We know from IV that, since the nilradical of
S+ is 0, S+ is a direct sum of simple ideals, but it is conceivable that
these are not the Si + given by (a). To see that the simple components
of S+ are the Si + given by (a), we need to establish (d).
Let T be an ideal of Si + ; we need to show that T is an ideal of Si .
It follows from (a) that T is an ideal of S+ , and is therefore by (c) a
direct sum of simple ideals of S+ each of which has a unity element.
The sum of these pairwise orthogonal idempotents in S+ is the unity
element e of T. Now e is an idempotent in S+ (and S), and the Peirce
decomposition (7′′ ) characterizes T as
(27)

T = S1,e = {t ∈ S | et = te = t}.

Let s be any element of S. Then ﬂexibility implies (s, t, e) + (e, t, s) = 0,
or
(28)

(st)e − st + ts = e(ts)

for all t ∈ T, s ∈ S.

But T an ideal of S+ implies that s · t ∈ T, so that st + ts = e(st + ts) =
e(st) + (st)e − st + ts by (27) and (28); that is, e(st) + (st)e = 2st, and
st is in T = S1,e by (7′ ). But then s · t in T implies ts is in T also; T is
an ideal of S. Then T ⊆ Si is an ideal of Si . Hence the only ideals of
Si + are 0 and Si + . Since Si + cannot be a zero algebra, Si + is simple.
We list without proof the central simple ﬂexible algebras A over
F which are such that A+ is a (central) simple Jordan algebra. These
are the algebras which (over their centers) can appear as the simple
components Si in (a) above:
1.

A is a central simple (commutative) Jordan algebra.

2. A is a quasiassociative central simple algebra. That is, there
is a scalar extension AK , K a quadratic extension of F , such that AK is
isomorphic to an algebra B(λ) deﬁned as follows: B is a central simple
associative algebra over K, λ = 12 is a ﬁxed element of K, and B(λ)
is the same vector space over K as B but multiplication in B(λ) is
deﬁned by
(29)

x ∗ y = λxy + (1 − λ)yx

where xy is the (associative) product in B.

for all x, y in B

## PDF page 59

POWER-ASSOCIATIVE ALGEBRAS

53

3. A is a ﬂexible quadratic algebra over F with nondegenerate
norm form.
Note that, except for Lie algebras, all of the central simple algebras
which we have mentioned in these notes are listed here (associative
algebras are the case λ = 1 (also λ = 0) in 2; Cayley algebras are
included in 3).
We should remark that, if an algebra A contains 1, any trace form
(x, y) on A may be expressed in terms of a linear form T (x). That is,
we write
(30)
and have
(31)

T (x) = (1, x)

for all x in A,

(x, y) = T (xy)

for all x, y in A

since (x1, y) = (1, xy). The symmetry and the associativity of the trace
form (x, y) are equivalent to the vanishing of T (x) on commutators and
associators:
(32)

T (xy) = T (yx),
T ((xy)z) = T (x(yz))

for all x, y, z in A.

If A is power-associative, hypotheses (ii) and (iii) of Theorem 11 become
(33)
and
(34)

T (e) = 0

for any idempotent e in A,

T (z) = 0

for any nilpotent z in A,

the latter being evident as follows: (34) implies that, if x · y is nilpotent,
then 0 = T (x · y) = (1, x · y) = 12 (1, xy) + 12 (1, yx) = 12 (x, y) + 12 (y, x) =
(x, y) and, conversely, if z = 1 · z is nilpotent, then (iii) implies T (z) =
(1, z) = 0.
A natural generalization to noncommutative algebras of the class
of (commutative) Jordan algebras is the class of algebras J satisfying
the Jordan identity
(35)

(xy)x2 = x(yx2 )

for all x, y in J.

## PDF page 60

54

POWER-ASSOCIATIVE ALGEBRAS

As in IV, we can linearize (35) to obtain
(35′ )

(x, y, w · z) + (w, y, z · x) + (z, y, x · w) = 0
for all w, x, y, z in J.

If J contains 1, then w = 1 in (35′ ) implies
(36)

(x, y, z) + (z, y, x) = 0

for all x, y, z in J;

that is, J is ﬂexible:
(37)

(xy)x = x(yx)

for all x, y in J.

If a unity element 1 is adjoined to J as in II, then a necessary and sufﬁcient condition that (35′ ) be satisﬁed in the algebra with 1 adjoined
is that both (35′ ) and (36) be satisﬁed in J. Hence we deﬁne a noncommutative Jordan algebra to be an algebra satisfying both (35) and
(37).
Exercise. Prove: A ﬂexible algebra J is a noncommutative Jordan
algebra if and only if any one of the following is satisﬁed:
(38)
(39)
(40)
(41)

(x2 y)x = x2 (yx)
for all x, y in J;
2
2
x (xy) = x(x y)
for all x, y in J;
2
2
(yx)x = (yx )x
for all x, y in J;
+
J is a (commutative) Jordan algebra.

We see from (41) that any semisimple algebra (of characteristic
= 5) satisfying the hypotheses of Theorem 11 is a noncommutative
Jordan algebra.
Since (35′ ) and (36) are multilinear, any scalar extension AK of a
noncommutative Jordan algebra is a noncommutative Jordan algebra.
It may be veriﬁed directly that any noncommutative Jordan algebra is
power-associative (hence strictly power-associative).
Let J be any noncommutative Jordan algebra. By (41) J+ is a
(commutative) Jordan algebra, and we have seen in IV that a trace
form on J+ may be given in terms of right multiplications of J+ . Our
application of this to the situation here works more smoothly if there is
a unity element 1 in J, so (if necessary) we adjoin one to J to obtain a

## PDF page 61

POWER-ASSOCIATIVE ALGEBRAS

55

noncommutative Jordan algebra J1 with 1 and having J as a subalgebra
(actually ideal). Then by the proof of Theorem 6 we know that
(42)

+
(x, y) = trace Rx·y
= 12 trace(Rx·y + Lx·y )
for all x, y in J1

is a trace form on J1 + where R+ indicates the right multiplication in
J1 + ; hence (23) holds for all x, y, z in J1 , where (x, y) is the symmetric
bilinear form (42). In terms of T (x) deﬁned by (30), we see that (23)
is equivalent to
(43)

T ((x · y) · z) = T (x · (y · z))

for all x, y, z in J1 .

Now (36) implies
(44)

Lxy − Ly Lx + Ry Rx − Ryx = 0

for all x, y in J1 .

Interchanging x and y in (44), and subtracting, we have
(45)

R[x,y] + L[x,y] = [Ry , Rx ] + [Lx , Ly ]

for all x, y in J1 .

Hence T ([x, y]) = (1, [x, y]) = 21 trace(R[x,y] + L[x,y] ) = 0 by (42)
and (45). Then xy = x · y + 12 [x, y] implies T (xy) = T (x · y) =
1
T (xy) + 12 T (yx), or
2
(46)

T (xy) = T (yx) = (x, y)

for all x, y in J1

since T (x · y) = (1, x · y) = (x, y) by (23). Now (43) and (46) imply
that (x, y) is a trace form on J1 . For 0 = 4T [(x · y) · z − x · (y · z)] =
T [(xy)z + (yx)z + z(xy) + z(yx) − x(yz) − x(zy) − (yz)x − (zy)x] =
2T [(xy)z − x(yz) − (zy)x + z(yx)] = 4T [(xy)z − x(yz)] by (36), so
T ((xy)z) = T (x(yz)), or (xy, z) = (x, yz) as desired. Then (42)
induces a trace form on the subalgebra J of J1 .
Corollary to Theorem 11. Modulo its nilradical, any ﬁnitedimensional noncommutative Jordan algebra of characteristic 0 is
(uniquely) expressible as a direct sum S1 ⊕ · · · ⊕ St of simple ideals
Si . Over their centers these Si are central simple algebras of the
following types: (commutative) Jordan, quasiassociative, or ﬂexible
quadratic.

## PDF page 62

56

POWER-ASSOCIATIVE ALGEBRAS

Proof: Only the veriﬁcation for (x, y) in (42) of hypotheses (ii) and
(iii) remains. But these are (12) and (8) of IV.
It was remarked in IV that, although proof was given only for commutative Jordan algebras of characteristic 0, the results were valid for
arbitrary characteristic (= 2). The same statement cannot be made
here. The trace argument in Theorem 11 can be modiﬁed to give the
direct sum decomposition for semisimple algebras [58]. But new central simple algebras occur for characteristic p [52; 55]; central simple
algebras which are not listed in the Corollary above are necessarily of
degree one [58] and are ramiﬁed in the sense of [35].
A ﬁnite-dimensional power-associative algebra A with 1 over F
is called a nodal algebra in case every element of A is of the form
α1 + z where α ∈ F and z is nilpotent, and A is not of the form
A = F 1 + N for N a nil subalgebra of A. There are no such algebras
which are alternative (of arbitrary characteristic), commutative Jordan
(of characteristic = 2) [32], or noncommutative Jordan of characteristic
0. But nodal noncommutative Jordan algebras of characteristic p > 0
do exist. Any nodal algebra has a homomorphic image which is a simple
nodal algebra.
Let J be a nodal noncommutative Jordan algebra over F . Since the
commutative Jordan algebra J+ is not a nodal algebra, J+ = F 1 + N+
where N+ is a nil subalgebra of J+ ; that is, J = F 1 + N, where N is
a subspace of J consisting of all nilpotent elements of J, and x · y ∈ N
for all x, y ∈ N. For any elements x, y ∈ N we have
(47)

xy = λ1 + z,

λ ∈ F , z ∈ N.

There must exist x, y in N with λ = 0 in (47). Since N+ is a nilpotent
commutative Jordan algebra, the powers of N+ lead to 0; equivalently,
the subalgebra (N+ )∗ of M(J+ ) is nilpotent. Now (47) implies yx =
−λ1 + (2x · y − z) and (xy)x = λx + zx = x(yx) = −λx + 2x(x · y) − xz,
or
(48)

x(x · y) = λx + x · z.

Now 0 = (x, x, y) + (y, x, x) = x2 y − x(λ1 + z) + (−λ1 + 2x · y − z)x −
yx2 = 2x2 y − 2λx − 2x · z + 4(x · y) · x − 2x(x · y) − 2x2 · y implies
(49)

x2 y = 2λx + 2x · z − 2(x · y) · x + x2 · y

## PDF page 63

POWER-ASSOCIATIVE ALGEBRAS

57

by (48). Deﬁning
(47′ )

λi ∈ F , zi ∈ N,

xi y = λi 1 + zi ,

linearization of (49) gives
(49′ )

(x1 · x2 )y = λ1 x2 + λ2 x1 + x1 · z2 + x2 · z1
− (x1 · y) · x2 − (x2 · y) · x1 + (x1 · x2 ) · y.

Theorem 12. Let J be a simple nodal noncommutative Jordan
algebra over F . Then F has characteristic p, J+ is the pn -dimensional
(commutative) associative algebra J+ = F [1, x1 , . . . , xn ], xpi = 0, n ≥ 2,
and multiplication in J is given by
(50)

fg = f · g +

n
∑

∂f ∂g
·
· cij ,
i,j=1 ∂xi ∂xj

cij = −cji ,

where at least one of the cij (= −cji ) has an inverse.
Proof: Since J = F 1 + N, every element a in J is of the form
(51)

a = α1 + x,

α ∈ F , x ∈ N.

By (51) every associator relative to the multiplication in J+ is an associator
(52)

[x1 , x2 , x3 ] = (x1 · x2 ) · x3 − x1 · (x2 · x3 ),

xi ∈ N.

We shall ﬁrst show that J+ is associative by showing that the subspace
B spanned by all of the associators (52) is 0. For any y in N, (49′ )
implies that (x1 · x2 )y is in N, so [(x1 · x2 ) · x3 ] y = λ3 x1 · x2 + (x1 · x2 ) ·
z3 + x3 · [λ1 x2 + λ2 x1 + x1 · z2 + x2 · z1 − (x1 · y) · x2 − (x2 · y) · x1 +
(x1 · x2 ) · y] − [(x1 · x2 ) · y] · x3 − (x3 · y) · (x1 · x2 ) + [(x1 · x2 ) · x3 ] · y by
(47′ ) and (49′ ). Interchange subscripts 1 and 3, and subtract, to obtain
[x1 , x2 , x3 ]y = [x1 , x2 , x3 ] + [x1 , z2 , x3 ] + [z1 , x2 , x3 ] − [x1 · y, x2 , x3 ] −
[x1 , x2 · y, x3 ] + [x3 · y, x2 , x1 ] + [x1 , x2 , x3 ] · y, so that we have the ﬁrst
inclusion in
(53)

BN ⊆ B + B · N,

NB ⊆ B + B · N.

The second part of (53) follows from nb = −bn + 2b · n for b in B, n in
N.

## PDF page 64

58

POWER-ASSOCIATIVE ALGEBRAS

by

Deﬁne an ascending series C0 ⊆ C1 ⊆ C2 · · · of subspaces Ci of J
(54)

C0 = B,

Ci+1 = Ci + Ci · N.

Note that all the Ci are contained in N (actually in N · N · N, since
B is). Since (N+ )∗ is nilpotent, there is a positive integer k such that
Ck+1 = Ck . We prove by induction on i that
(55)

Ci N ⊆ Ci+1 ,

NCi ⊆ Ci+1 .

The case i = 0 of (55) is (53). We assume (55) and prove that Ci+1 N ⊆
Ci+2 as follows: by the assumption of the induction it is suﬃcient to
show
(56)

(Ci · N)N ⊆ Ci+1 + Ci+1 · N.

Now the ﬂexible law (36) is equivalent to
(57)

(x · y)z = (yz) · x + (yx) · z − (y · z)x for all x, y, z in J.

Put x in Ci , y and z in N into (57), and use yz = µ1 + w, µ ∈ F , w ∈ N,
to see that each term of the right-hand side of (57) is in Ci+1 + Ci+1 · N
by the assumption (55) of the induction. We have established (56), and
therefore Ci+1 N ⊆ Ci+2 . Then, as above, NCi+1 ⊆ Ci+1 N + Ci+1 · N ⊆
Ci+2 , and we have established (55). For the positive integer k such that
Ck+1 = Ck , we have Ck an ideal of J. For Ck J = Ck (F 1 + N) ⊆ Ck by
(55), and similarly JCk ⊆ Ck . The ideal Ck , being contained in N, is
not J. Hence Ck = 0, since J is simple. But B ⊆ Ck , so B = 0, J+ is
associative.
An ideal I of an algebra A is called a characteristic ideal (or Dideal) in case I is mapped into itself by every derivation of A. A is
called D-simple if 0 and A are the only characteristic ideals of A.
We show next that the commutative associative algebra J+ is Dsimple. Interchange x and y in (36) to obtain
(36′ )

(y, x, z) + (z, x, y) = 0

for all x, y, z in J;

interchange y and z in (36) to obtain
(36′′ )

(x, z, y) + (y, z, x) = 0

for all x, y, z in J;

## PDF page 65

POWER-ASSOCIATIVE ALGEBRAS

59

adding (36) and (36′ ), and subtracting (36′′ ), we obtain the identity
(58)

[x · y, z] = [x, z] · y + x · [y, z]

for all x, y, z in J,

which is valid in any ﬂexible algebra. Identity (58) is equivalent to the
statement that
(59)

D = Rz − Lz

for any z in J

is a derivation of J+ . If I is an ideal of J+ , then x · z is in I for all x
in I, z in J. If, furthermore, I is characteristic, then [x, z] = xD is in
I, since D in (59) is a derivation of J+ . Hence xz = x · z + 12 [x, z] and
zx = x · z − 12 [x, z] are in I for all x in I, z in J; that is, I is an ideal
of J. Hence J simple implies that the commutative associative algebra
J+ is D-simple.
It is a recently proved result in the theory of commutative associative algebras (see [24]) that, if A is a ﬁnite-dimensional D-simple
commutative associative algebra of the form A = F 1 + R where R is
the radical of A, then (except for the trivial case A = F 1 which may
occur at characteristic 0, and which does not give a nodal algebra) F
has characteristic p and A is the pn -dimensional algebra A = F [1, x1 ,
. . . , xn ], xi p = 0.
Now any derivation D of such an algebra has the form
(60)

f → fD =

n
∑
∂f

i=1 ∂xi

· ai ,

ai ∈ A,

where the ai of course depend on the derivation D. Then (59) implies
that f → [f, g] is a derivation of J+ for any g in J. By (60) we have
(61)

[f, g] =

n
∑
∂f

i=1 ∂xi

· ai (g),

ai (g) ∈ J.

To evaluate the ai (g), note that xi D = [xi , g] = ai (g) and
(62)

[g, xi ] =

n
∑
∂g

j=1 ∂xj

· aj (xi ).

Then aj (xi ) = [xj , xi ] implies ai (g) = −[g, xi ] = −
(63)

[f, g] =

n
∑

∂f ∂g
·
· [xi , xj ]
i,j=1 ∂xi ∂xj

n
∑
∂g

j=1 ∂xj

· [xj , xi ], or

## PDF page 66

60

POWER-ASSOCIATIVE ALGEBRAS

by (61), so that f g = f · g + 12 [f, g] implies (50) where cij = 12 [xi , xj ]. If
every cij were in N, then N would be a subalgebra of A, a contradiction.
Hence at least one of the cij is of the form (51) with α = 0, so it has
an inverse, and n ≥ 2.
Not every algebra described in the conclusion of Theorem 12 is
simple (see [55]). However, all such algebras of dimension p2 are, and
for every even n there are simple algebras of dimension pn . There are
relationships between the derivation algebras of nodal noncommutative
Jordan algebras and recently discovered (non-classical) simple Lie algebras of characteristic p [7; 11; 17; 68]. For a general discussion of Lie
algebras of characteristic p, see [61].

## PDF page 67

BIBLIOGRAPHY

61

The following list of papers on nonassociative algebras is intended
to bring up to date (May 1961) the selective bibliography which appears
at the end of the expository article [64].

1.

A. A. Albert, On partially stable algebras, Trans. Amer. Math. Soc.
vol. 84 (1957), pp. 430–443; Addendum to the paper on partially
stable algebras, ibid, vol. 87 (1958), pp. 57–62.

2.

, A construction of exceptional Jordan division algebras, Ann. of
Math. (2) vol. 67 (1958), pp. 1–28.

3.

, On the orthogonal equivalence of sets of real symmetric matrices, J. Math. Mech. vol. 7 (1958), pp. 219–236.

4.

, Finite noncommutative division algebras, Proc. Amer. Math.
Soc. vol. 9 (1958), pp. 928–932.

5.

, Finite division algebras and ﬁnite planes, Proc. Symposia Applied Math., vol. X, Combinatorial Analysis, Amer. Math. Soc.
1960, pp. 53–70.

6.

, A solvable exceptional Jordan algebra, J. Math. Mech. vol. 8
(1959), pp. 331–337.

7.

A. A. Albert and M. S. Frank, Simple Lie algebras of characteristic p,
Univ. e Politec. Torino. Rend. Sem. Mat. vol. 14 (1954–5), pp. 117–
139.

8.

A. A. Albert and N. Jacobson, On reduced exceptional simple Jordan
algebras, Ann. of Math. (2) vol. 66 (1957), pp. 400–417.

9.

A. A. Albert and L. J. Paige, On a homomorphism property of certain
Jordan algebras, Trans. Amer. Math. Soc. vol. 93 (1959), pp. 20–29.

10. S. A. Amitsur, A general theory of radicals. II. Radicals in rings and
bicategories, Amer. J. Math. vol. 76 (1954), pp. 100–125; III. Applications, ibid, pp. 126–136.
11. Richard Block, New simple Lie algebras of prime characteristic, Trans.
Amer. Math. Soc. vol. 89 (1958), pp. 421–449.
12. R. Bott and J. Milnor, On the parallelizability of the spheres, Bull. Amer.
Math. Soc. vol. 64 (1958), pp. 87–89.

## PDF page 68

62

BIBLIOGRAPHY

13. Bailey Brown and N. H. McCoy, Prime ideals in nonassociative rings,
Trans. Amer. Math. Soc. vol. 89 (1958), pp. 245–255.
14. R. H. Bruck, Recent advances in the foundations of euclidean plane geometry, Amer. Math. Monthly vol. 62 (1955), No. 7, part II, pp. 2–
17.
15. P. M. Cohn, Two embedding theorems for Jordan algebras, Proc. London
Math. Soc. (3) vol. 9 (1959), pp. 503–524.
16. J. Dieudonné, On semi-simple Lie algebras, Proc. Amer. Math. Soc.
vol. 4 (1953), pp. 931–932.
17. M. S. Frank, A new class of simple Lie algebras, Proc. Nat. Acad. Sci.
U.S.A. vol. 40 (1954), pp. 713–719.
18. Hans Freudenthal, Sur le groupe exceptionnel E7 , Nederl. Akad. Wetensch. Proc. Ser. A. vol. 56 (1953), pp. 81–89; Sur des invariants
caractéristiques des groupes semi-simples, ibid, pp. 90–94; Sur le
groupe exceptionnel E8 , ibid, pp. 95-98; Zur ebenen Oktavengeometrie, ibid, pp. 195–200.
19.

, Beziehungen der E7 und E8 zur Oktavenebene I. Nederl. Akad.
Wetensch. Proc. Ser. A. vol. 57 (1954), pp. 218–230; II. ibid,
pp. 363–368; III. ibid, vol. 58 (1955), pp. 151–157; IV. ibid, pp. 277–
285; V. ibid, vol. 62 (1959), pp. 165–179; VI. ibid, pp. 180–191; VII.
ibid, pp. 192–201; VIII. ibid, pp. 447–465; IX. ibid, pp. 466–474.

20.

, Lie groups and foundations of geometry, Canadian Mathematical Congress Seminar, 1959 (mimeographed).

21. Marshall Hall, Jr., Projective planes and related topics, Calif. Inst. of
Tech, 1954, vi + 77pp.
22.

, An identity in Jordan rings, Proc. Amer. Math. Soc. vol. 7
(1956), pp. 990–998.

23. L. R. Harper, Jr., Proof of an Identity on Jordan algebras, Proc. Nat.
Acad. Sci. U.S.A. vol. 42 (1956), pp. 137–139.
24.

, On diﬀerentiably simple algebras, Trans. Amer. Math. Soc.
vol. 100 (1961), pp. 63–72.

25. Bruno Harris, Centralizers in Jordan algebras, Paciﬁc J. Math, vol. 8
(1958), pp. 757–790.

## PDF page 69

BIBLIOGRAPHY

26.

63

, Derivations of Jordan algebras, Paciﬁc J. Math. vol. 9 (1959),
pp. 495–512.

27. I. N. Herstein, On the Lie and Jordan rings of a simple associative ring,
Amer. J. Math., vol. 77 (1955), pp. 279–285.
28.

, The Lie ring of a simple associative ring, Duke Math. J. vol. 22
(1955), pp. 471–476.

29.

, Jordan homomorphisms, Trans. Amer. Math. Soc. vol 81 (1956),
pp. 331–341.

30.

, Lie and Jordan systems in simple rings with involution, Amer.
J. Math. vol. 78 (1956), pp. 629–649.

31. N. Jacobson, Some aspects of the theory of representations of Jordan
algebras, Proc. Internat. Congress of Math., 1954, Amsterdam,
vol. III, pp. 28–33.
32.

, A theorem on the structure of Jordan algebras, Proc. Nat. Acad.
Sci. U.S.A. vol. 42 (1956), pp. 140–147.

33.

, Composition algebras and their automorphisms, Rend. Circ.
Mat. Palermo (2) vol. 7 (1958), pp. 55–80.

34.

, Nilpotent elements in semi-simple Jordan algebras, Math. Ann.
vol. 136 (1958), pp. 375–386.

35.

, Some groups of transformations deﬁned by Jordan algebras.
I., J. Reine Angew. Math. vol. 201 (1959), pp. 178–195; II., ibid,
vol. 204 (1960), pp. 74–98; III., ibid, vol. 207 (1961), pp. 61–85.

36.

, Exceptional Lie algebras, dittoed, 57 pp.

37.

, Cayley planes, dittoed, 28 pp.

38. N. Jacobson and L. J. Paige, On Jordan algebras with two generators, J.
Math. Mech. vol. 6 (1957), pp. 895–906.
39. P. Jordan, Über eine nicht-desarguessche ebene projecktive Geometrie,
Abh. Math. Sem. Hamb. Univ. vol. 16 (1949), pp. 74–76.
40. Irving Kaplansky, Lie algebras of characteristic p, Trans. Amer. Math.
Soc. vol. 89 (1958), pp. 149–183.

## PDF page 70

64

BIBLIOGRAPHY

41. Erwin Kleinfeld, Primitive alternative rings and semisimplicity, Amer.
J. Math. vol. 77 (1955), pp. 725–730.
42.

, Generalization of a theorem on simple alternative rings, Portugal. Math. vol. 14 (1956), pp. 91–94.

43.

, Standard and accessible rings, Canad. J. Math. vol. 8 (1956),
pp. 335–340.

44.

, Alternative nil rings, Ann. of Math. (2) vol. 66 (1957), pp. 395–
399.

45.

, Assosymmetric rings, Proc. Amer. Math. Soc. vol 8 (1957),
pp. 983–986.

46.

, A note on Moufang-Lie rings, Proc. Amer. Math. Soc. vol. 9
(1958), pp. 72–74.

47.

, Quasi-nil rings, Proc. Amer. Math. Soc. vol. 10 (1959), pp. 477–
479.

48.

, Simple algebras of type (1, 1) are associative, Canadian J. Math.
vol. 13 (1961), pp. 129–148.

49. Max Koecher, Analysis in reelen Jordan-Algebren, Nachr. Acad. Wiss.
Göttingen Math.-Phys. Kl. IIa 1958, pp. 67–74.
50. L. A. Kokoris, Power-associative rings of characteristic two, Proc. Amer.
Math. Soc. vol. 6 (1955), pp. 705–710.
51.

, Simple power-associative algebras of degree two, Ann. of Math.
(2) vol. 64 (1956), pp. 544–550.

52.

, Simple nodal noncommutative Jordan algebras, Proc. Amer.
Math. Soc. vol. 9 (1958), pp. 652–654.

53.

, On nilstable algebras, Proc. Amer. Math. Soc. vol. 9 (1958),
pp. 697–701.

54.

, On rings of (γ, δ)-type, Proc. Amer. Math. Soc. vol. 9 (1958),
pp. 897–904.

55.

, Nodal noncommutative Jordan algebras, Canadian J. Math.
vol. 12 (1960), pp. 488–492.

## PDF page 71

BIBLIOGRAPHY

65

56. I. G. Macdonald, Jordan algebras with three generators, Proc. London
Math. Soc. (3), vol. 10 (1960), pp. 395–408.
57. R. H. Oehmke, A class of noncommutative power-associative algebras,
Trans. Amer. Math. Soc. vol. 87 (1958), pp. 226–236.
58.

, On ﬂexible algebras, Ann. of Math. (2) vol. 68 (1958), pp. 221–
230.

59.

, On ﬂexible power-associative algebras of degree two, Proc.
Amer. Math. Soc. vol. 12 (1961), pp. 151–158.

60. Gunter Pickert, Projektive Ebenen, Berlin, 1955.
61. Report of a Conference on Linear Algebras, Nat. Acad. of Sci. – Nat.
Res. Council, Publ. 502, v + 60 pp. (1957) (N. Jacobson, Jordan
algebras, pp. 12–19; Erwin Kleinfeld, On alternative and right alternative rings, pp. 20–23; G. B. Seligman, A survey of Lie algebras
of characteristic p, pp. 24–32.)
62. R. L. San Soucie, Right alternative rings of characteristic two, Proc.
Amer. Math. Soc. vol. 6 (1955), pp. 716–719.
63.

, Weakly standard rings, Amer. J. Math. vol. 79 (1957), pp. 80–
86.

64. R. D. Schafer, Structure and representation of nonassociative algebras,
Bull. Amer. Math. Soc. vol. 61 (1955), pp. 469–484.
65.

, On noncommutative Jordan algebras, Proc. Amer. Math. Soc.
vol. 9 (1958), pp. 110–117.

66.

, Restricted noncommutative Jordan algebras of characteristic p,
Proc. Amer. Math. Soc. vol. 9 (1958), pp. 141–144.

67.

, On cubic forms permitting composition, Proc. Amer. Math. Soc.
vol. 10 (1959), pp. 917–925.

68.

, Nodal noncommutative Jordan algebras and simple Lie algebras
of characteristic p, Trans. Amer. Math. Soc. vol. 94 (1960), pp. 310–
326.

69.

, Cubic forms permitting a new type of composition, J. Math.
Mech. vol. 10 (1961), pp. 159–174.

## PDF page 72

66

BIBLIOGRAPHY

70. G. B. Seligman, On automorphisms of Lie algebras of classical type,
Trans. Amer. Math. Soc. vol. 92 (1959), pp. 430–448; II, ibid, vol. 94
(1960), pp. 452–482; III, ibid, vol. 97 (1960), pp. 286–316.
71. A. I. Shirshov, On special J-rings, Mat. Sbornik N. S. vol. 38 (80) (1956),
pp. 149–166 (Russian).
72.

, Some questions in the theory of rings close to associative, Uspehi Mat. Nauk, vol. 13 (1958), no. 6 (84), pp. 3–20 (Russian).

73. M. F. Smiley, Jordan homomorphisms onto prime rings, Trans. Amer.
Math. Soc. vol. 84 (1957), pp. 426–429.
74.

, Jordan homomorphisms and right alternative rings, Proc.
Amer. Math. Soc. vol. 8 (1957), pp. 668–671.

75. T. A. Springer, On a class of Jordan algebras, Nederl. Akad. Wetensch.
Proc. Ser. A. vol. 62 (1959), pp. 254–264.
76.

, The projective octave plane, Nederl. Akad. Wetensch. Proc.
Ser. A. vol. 63 (1960), pp. 74–101.

77.

, The classiﬁcation of reduced exceptional simple Jordan algebras,
Nederl. Akad. Wetensch. Proc. Ser. A. vol. 63 (1960), pp. 414–422.

78. Taeil Suh, On isomorphisms of little projective groups of Cayley planes,
Yale dissertation, 1960.
79. E. J. Taft, Invariant Wedderburn factors, Illinois J. Math. vol. 1 (1957),
pp. 565–573.
80.

, The Whitehead ﬁrst lemma for alternative algebras, Proc. Amer.
Math. Soc. vol. 8 (1957), pp. 950–956.

81. J. Tits, Le plan projectif des octaves et les groupes de Lie exceptionnels,
Acad. Roy. Belgique Bull. Cl. Sci. (5) vol. 39 (1953), pp. 309–329;
Le plan projectif des octaves et les groupes exceptionnels E6 et E7 ,
ibid, vol. 40 (1954), pp. 29–40.
82.

, Sur la trialité et les algèbres d’octaves, Acad. Roy. Belg. Bull.
Cl. Sci. (5) vol. 44 (1958), pp. 332–350.

83. M. L. Tomber, Lie algebras of types A, B, C, D, and F , Trans. Amer.
Math. Soc. vol. 88 (1958), pp. 99–106.

## PDF page 73

BIBLIOGRAPHY

67

84. F. van der Blij and T. A. Springer, The arithmetics of octaves and of
the group G2 , Nederl. Akad. Wetensch. Proc. Ser. A. vol. 62 (1959),
pp. 406–418.
85. L. M. Weiner, Lie admissible algebras, Univ. Nac. Tucumán. Rev. Ser. A.
vol. II (1957), pp. 10–24.

## PDF page 74



## PDF page 75

LICENSING.

End of the Project Gutenberg EBook of An Introduction to Nonassociative
Algebras, by R. D. Schafer
*** END OF THIS PROJECT GUTENBERG EBOOK NONASSOCIATIVE ALGEBRAS ***
***** This file should be named 25156-pdf.pdf or 25156-pdf.zip *****
This and all associated files of various formats will be found in:
http://www.gutenberg.org/2/5/1/5/25156/
Produced by David Starner, David Wilson, Suzanne Lybarger
and the Online Distributed Proofreading Team at
http://www.pgdp.net

Updated editions will replace the previous one-the old editions
will be renamed.
Creating the works from public domain print editions means that no
one owns a United States copyright in these works, so the Foundation
(and you!) can copy and distribute it in the United States without
permission and without paying copyright royalties. Special rules,
set forth in the General Terms of Use part of this license, apply to
copying and distributing Project Gutenberg-tm electronic works to
protect the PROJECT GUTENBERG-tm concept and trademark. Project
Gutenberg is a registered trademark, and may not be used if you
charge for the eBooks, unless you receive specific permission. If you
do not charge anything for copies of this eBook, complying with the
rules is very easy. You may use this eBook for nearly any purpose
such as creation of derivative works, reports, performances and
research. They may be modified and printed and given away-you may do
practically ANYTHING with public domain eBooks. Redistribution is
subject to the trademark license, especially commercial
redistribution.

*** START: FULL LICENSE ***
THE FULL PROJECT GUTENBERG LICENSE
PLEASE READ THIS BEFORE YOU DISTRIBUTE OR USE THIS WORK
To protect the Project Gutenberg-tm mission of promoting the free
distribution of electronic works, by using or distributing this work
(or any other work associated in any way with the phrase "Project
Gutenberg"), you agree to comply with all the terms of the Full Project
Gutenberg-tm License (available with this file or online at
http://gutenberg.org/license).

Section 1. General Terms of Use and Redistributing Project Gutenberg-tm
electronic works
1.A. By reading or using any part of this Project Gutenberg-tm
electronic work, you indicate that you have read, understand, agree to
and accept all the terms of this license and intellectual property
(trademark/copyright) agreement. If you do not agree to abide by all

69

## PDF page 76

70

LICENSING.

the terms of this agreement, you must cease using and return or destroy
all copies of Project Gutenberg-tm electronic works in your possession.
If you paid a fee for obtaining a copy of or access to a Project
Gutenberg-tm electronic work and you do not agree to be bound by the
terms of this agreement, you may obtain a refund from the person or
entity to whom you paid the fee as set forth in paragraph 1.E.8.
1.B. "Project Gutenberg" is a registered trademark. It may only be
used on or associated in any way with an electronic work by people who
agree to be bound by the terms of this agreement. There are a few
things that you can do with most Project Gutenberg-tm electronic works
even without complying with the full terms of this agreement. See
paragraph 1.C below. There are a lot of things you can do with Project
Gutenberg-tm electronic works if you follow the terms of this agreement
and help preserve free future access to Project Gutenberg-tm electronic
works. See paragraph 1.E below.
1.C. The Project Gutenberg Literary Archive Foundation ("the Foundation"
or PGLAF), owns a compilation copyright in the collection of Project
Gutenberg-tm electronic works. Nearly all the individual works in the
collection are in the public domain in the United States. If an
individual work is in the public domain in the United States and you are
located in the United States, we do not claim a right to prevent you from
copying, distributing, performing, displaying or creating derivative
works based on the work as long as all references to Project Gutenberg
are removed. Of course, we hope that you will support the Project
Gutenberg-tm mission of promoting free access to electronic works by
freely sharing Project Gutenberg-tm works in compliance with the terms of
this agreement for keeping the Project Gutenberg-tm name associated with
the work. You can easily comply with the terms of this agreement by
keeping this work in the same format with its attached full Project
Gutenberg-tm License when you share it without charge with others.
1.D. The copyright laws of the place where you are located also govern
what you can do with this work. Copyright laws in most countries are in
a constant state of change. If you are outside the United States, check
the laws of your country in addition to the terms of this agreement
before downloading, copying, displaying, performing, distributing or
creating derivative works based on this work or any other Project
Gutenberg-tm work. The Foundation makes no representations concerning
the copyright status of any work in any country outside the United
States.
1.E.

Unless you have removed all references to Project Gutenberg:

1.E.1. The following sentence, with active links to, or other immediate
access to, the full Project Gutenberg-tm License must appear prominently
whenever any copy of a Project Gutenberg-tm work (any work on which the
phrase "Project Gutenberg" appears, or with which the phrase "Project
Gutenberg" is associated) is accessed, displayed, performed, viewed,
copied or distributed:
This eBook is for the use of anyone anywhere at no cost and with
almost no restrictions whatsoever. You may copy it, give it away or
re-use it under the terms of the Project Gutenberg License included
with this eBook or online at www.gutenberg.org
1.E.2.

If an individual Project Gutenberg-tm electronic work is derived

## PDF page 77

LICENSING.

from the public domain (does not contain a notice indicating that it is
posted with permission of the copyright holder), the work can be copied
and distributed to anyone in the United States without paying any fees
or charges. If you are redistributing or providing access to a work
with the phrase "Project Gutenberg" associated with or appearing on the
work, you must comply either with the requirements of paragraphs 1.E.1
through 1.E.7 or obtain permission for the use of the work and the
Project Gutenberg-tm trademark as set forth in paragraphs 1.E.8 or
1.E.9.
1.E.3. If an individual Project Gutenberg-tm electronic work is posted
with the permission of the copyright holder, your use and distribution
must comply with both paragraphs 1.E.1 through 1.E.7 and any additional
terms imposed by the copyright holder. Additional terms will be linked
to the Project Gutenberg-tm License for all works posted with the
permission of the copyright holder found at the beginning of this work.
1.E.4. Do not unlink or detach or remove the full Project Gutenberg-tm
License terms from this work, or any files containing a part of this
work or any other work associated with Project Gutenberg-tm.
1.E.5. Do not copy, display, perform, distribute or redistribute this
electronic work, or any part of this electronic work, without
prominently displaying the sentence set forth in paragraph 1.E.1 with
active links or immediate access to the full terms of the Project
Gutenberg-tm License.
1.E.6. You may convert to and distribute this work in any binary,
compressed, marked up, nonproprietary or proprietary form, including any
word processing or hypertext form. However, if you provide access to or
distribute copies of a Project Gutenberg-tm work in a format other than
"Plain Vanilla ASCII" or other format used in the official version
posted on the official Project Gutenberg-tm web site (www.gutenberg.org),
you must, at no additional cost, fee or expense to the user, provide a
copy, a means of exporting a copy, or a means of obtaining a copy upon
request, of the work in its original "Plain Vanilla ASCII" or other
form. Any alternate format must include the full Project Gutenberg-tm
License as specified in paragraph 1.E.1.
1.E.7. Do not charge a fee for access to, viewing, displaying,
performing, copying or distributing any Project Gutenberg-tm works
unless you comply with paragraph 1.E.8 or 1.E.9.
1.E.8. You may charge a reasonable fee for copies of or providing
access to or distributing Project Gutenberg-tm electronic works provided
that
- You pay a royalty fee of 20% of the gross profits you derive from
the use of Project Gutenberg-tm works calculated using the method
you already use to calculate your applicable taxes. The fee is
owed to the owner of the Project Gutenberg-tm trademark, but he
has agreed to donate royalties under this paragraph to the
Project Gutenberg Literary Archive Foundation. Royalty payments
must be paid within 60 days following each date on which you
prepare (or are legally required to prepare) your periodic tax
returns. Royalty payments should be clearly marked as such and
sent to the Project Gutenberg Literary Archive Foundation at the
address specified in Section 4, "Information about donations to

71

## PDF page 78

72

LICENSING.

the Project Gutenberg Literary Archive Foundation."
- You provide a full refund of any money paid by a user who notifies
you in writing (or by e-mail) within 30 days of receipt that s/he
does not agree to the terms of the full Project Gutenberg-tm
License. You must require such a user to return or
destroy all copies of the works possessed in a physical medium
and discontinue all use of and all access to other copies of
Project Gutenberg-tm works.
- You provide, in accordance with paragraph 1.F.3, a full refund of any
money paid for a work or a replacement copy, if a defect in the
electronic work is discovered and reported to you within 90 days
of receipt of the work.
- You comply with all other terms of this agreement for free
distribution of Project Gutenberg-tm works.
1.E.9. If you wish to charge a fee or distribute a Project Gutenberg-tm
electronic work or group of works on different terms than are set
forth in this agreement, you must obtain permission in writing from
both the Project Gutenberg Literary Archive Foundation and Michael
Hart, the owner of the Project Gutenberg-tm trademark. Contact the
Foundation as set forth in Section 3 below.
1.F.
1.F.1. Project Gutenberg volunteers and employees expend considerable
effort to identify, do copyright research on, transcribe and proofread
public domain works in creating the Project Gutenberg-tm
collection. Despite these efforts, Project Gutenberg-tm electronic
works, and the medium on which they may be stored, may contain
"Defects," such as, but not limited to, incomplete, inaccurate or
corrupt data, transcription errors, a copyright or other intellectual
property infringement, a defective or damaged disk or other medium, a
computer virus, or computer codes that damage or cannot be read by
your equipment.
1.F.2. LIMITED WARRANTY, DISCLAIMER OF DAMAGES - Except for the "Right
of Replacement or Refund" described in paragraph 1.F.3, the Project
Gutenberg Literary Archive Foundation, the owner of the Project
Gutenberg-tm trademark, and any other party distributing a Project
Gutenberg-tm electronic work under this agreement, disclaim all
liability to you for damages, costs and expenses, including legal
fees. YOU AGREE THAT YOU HAVE NO REMEDIES FOR NEGLIGENCE, STRICT
LIABILITY, BREACH OF WARRANTY OR BREACH OF CONTRACT EXCEPT THOSE
PROVIDED IN PARAGRAPH F3. YOU AGREE THAT THE FOUNDATION, THE
TRADEMARK OWNER, AND ANY DISTRIBUTOR UNDER THIS AGREEMENT WILL NOT BE
LIABLE TO YOU FOR ACTUAL, DIRECT, INDIRECT, CONSEQUENTIAL, PUNITIVE OR
INCIDENTAL DAMAGES EVEN IF YOU GIVE NOTICE OF THE POSSIBILITY OF SUCH
DAMAGE.
1.F.3. LIMITED RIGHT OF REPLACEMENT OR REFUND - If you discover a
defect in this electronic work within 90 days of receiving it, you can
receive a refund of the money (if any) you paid for it by sending a
written explanation to the person you received the work from. If you
received the work on a physical medium, you must return the medium with
your written explanation. The person or entity that provided you with

## PDF page 79

LICENSING.

the defective work may elect to provide a replacement copy in lieu of a
refund. If you received the work electronically, the person or entity
providing it to you may choose to give you a second opportunity to
receive the work electronically in lieu of a refund. If the second copy
is also defective, you may demand a refund in writing without further
opportunities to fix the problem.
1.F.4. Except for the limited right of replacement or refund set forth
in paragraph 1.F.3, this work is provided to you ’AS-IS’ WITH NO OTHER
WARRANTIES OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO
WARRANTIES OF MERCHANTIBILITY OR FITNESS FOR ANY PURPOSE.
1.F.5. Some states do not allow disclaimers of certain implied
warranties or the exclusion or limitation of certain types of damages.
If any disclaimer or limitation set forth in this agreement violates the
law of the state applicable to this agreement, the agreement shall be
interpreted to make the maximum disclaimer or limitation permitted by
the applicable state law. The invalidity or unenforceability of any
provision of this agreement shall not void the remaining provisions.
1.F.6. INDEMNITY - You agree to indemnify and hold the Foundation, the
trademark owner, any agent or employee of the Foundation, anyone
providing copies of Project Gutenberg-tm electronic works in accordance
with this agreement, and any volunteers associated with the production,
promotion and distribution of Project Gutenberg-tm electronic works,
harmless from all liability, costs and expenses, including legal fees,
that arise directly or indirectly from any of the following which you do
or cause to occur: (a) distribution of this or any Project Gutenberg-tm
work, (b) alteration, modification, or additions or deletions to any
Project Gutenberg-tm work, and (c) any Defect you cause.

Section

2.

Information about the Mission of Project Gutenberg-tm

Project Gutenberg-tm is synonymous with the free distribution of
electronic works in formats readable by the widest variety of computers
including obsolete, old, middle-aged and new computers. It exists
because of the efforts of hundreds of volunteers and donations from
people in all walks of life.
Volunteers and financial support to provide volunteers with the
assistance they need, is critical to reaching Project Gutenberg-tm’s
goals and ensuring that the Project Gutenberg-tm collection will
remain freely available for generations to come. In 2001, the Project
Gutenberg Literary Archive Foundation was created to provide a secure
and permanent future for Project Gutenberg-tm and future generations.
To learn more about the Project Gutenberg Literary Archive Foundation
and how your efforts and donations can help, see Sections 3 and 4
and the Foundation web page at http://www.pglaf.org.

Section 3.
Foundation

Information about the Project Gutenberg Literary Archive

The Project Gutenberg Literary Archive Foundation is a non profit
501(c)(3) educational corporation organized under the laws of the
state of Mississippi and granted tax exempt status by the Internal
Revenue Service. The Foundation’s EIN or federal tax identification

73

## PDF page 80

74

LICENSING.

number is 64-6221541. Its 501(c)(3) letter is posted at
http://pglaf.org/fundraising. Contributions to the Project Gutenberg
Literary Archive Foundation are tax deductible to the full extent
permitted by U.S. federal laws and your state’s laws.
The Foundation’s principal office is located at 4557 Melan Dr. S.
Fairbanks, AK, 99712., but its volunteers and employees are scattered
throughout numerous locations. Its business office is located at
809 North 1500 West, Salt Lake City, UT 84116, (801) 596-1887, email
business@pglaf.org. Email contact links and up to date contact
information can be found at the Foundation’s web site and official
page at http://pglaf.org
For additional contact information:
Dr. Gregory B. Newby
Chief Executive and Director
gbnewby@pglaf.org

Section 4. Information about Donations to the Project Gutenberg
Literary Archive Foundation
Project Gutenberg-tm depends upon and cannot survive without wide
spread public support and donations to carry out its mission of
increasing the number of public domain and licensed works that can be
freely distributed in machine readable form accessible by the widest
array of equipment including outdated equipment. Many small donations
($1 to $5,000) are particularly important to maintaining tax exempt
status with the IRS.
The Foundation is committed to complying with the laws regulating
charities and charitable donations in all 50 states of the United
States. Compliance requirements are not uniform and it takes a
considerable effort, much paperwork and many fees to meet and keep up
with these requirements. We do not solicit donations in locations
where we have not received written confirmation of compliance. To
SEND DONATIONS or determine the status of compliance for any
particular state visit http://pglaf.org
While we cannot and do not solicit contributions from states where we
have not met the solicitation requirements, we know of no prohibition
against accepting unsolicited donations from donors in such states who
approach us with offers to donate.
International donations are gratefully accepted, but we cannot make
any statements concerning tax treatment of donations received from
outside the United States. U.S. laws alone swamp our small staff.
Please check the Project Gutenberg Web pages for current donation
methods and addresses. Donations are accepted in a number of other
ways including checks, online payments and credit card donations.
To donate, please visit: http://pglaf.org/donate

Section 5.
works.

General Information About Project Gutenberg-tm electronic

Professor Michael S. Hart is the originator of the Project Gutenberg-tm

## PDF page 81

LICENSING.

concept of a library of electronic works that could be freely shared
with anyone. For thirty years, he produced and distributed Project
Gutenberg-tm eBooks with only a loose network of volunteer support.

Project Gutenberg-tm eBooks are often created from several printed
editions, all of which are confirmed as Public Domain in the U.S.
unless a copyright notice is included. Thus, we do not necessarily
keep eBooks in compliance with any particular paper edition.

Most people start at our Web site which has the main PG search facility:
http://www.gutenberg.org
This Web site includes information about Project Gutenberg-tm,
including how to make donations to the Project Gutenberg Literary
Archive Foundation, how to help produce our new eBooks, and how to
subscribe to our email newsletter to hear about new eBooks.

75
