Source: https://doi.org/10.1007/s00032-021-00325-y
PDF sha256: c4770512083fbad27a2e0da1209e54d72e82da6dd4912b542ea8ddf649ea6e5a
License: https://creativecommons.org/licenses/by/4.0
Language: eng
Fidelity: machine-gated

# Transcription of krausshar_2021_function_theories_in_cayley_dickson_algebras_and_number_theory.pdf

Transcription of `krausshar_2021_function_theories_in_cayley_dickson_algebras_and_number_theory.pdf` in this directory, 26 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-26 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Milan J. Math. Vol. 89 (2021) 19–44
https://doi.org/10.1007/s00032-021-00325-y
Published online March 8, 2021
© 2021 The Author(s)

Milan Journal of Mathematics

Function Theories in Cayley-Dickson
Algebras and Number Theory
Rolf Sören Kraußhar
Abstract. In the recent years a lot of eﬀort has been made to extend the theory
of hyperholomorphic functions from the setting of associative Cliﬀord algebras to
non-associative Cayley-Dickson algebras, starting with the octonions.
An important question is whether there appear really essentially diﬀerent
features in the treatment with Cayley-Dickson algebras that cannot be handled
in the Cliﬀord analysis setting. Here we give one concrete example: Cayley-Dickson
algebras admit the construction of direct analogues of so-called CM-lattices, in
particular, lattices that are closed under multiplication.
Canonical examples are lattices with components from the algebraic number
√
√
ﬁelds Q[ m1 , . . . mk ]. Note that the multiplication of two non-integer lattice
paravectors does not give anymore a lattice paravector in the Cliﬀord algebra. In
this paper we exploit the tools of octonionic function theory to set up an algebraic
relation between diﬀerent octonionic generalized elliptic functions which give rise
to octonionic elliptic curves. We present explicit formulas for the trace of the
octonionic CM-division values.
Mathematics Subject Classiﬁcation (2010). Primary 30G35; Secondary 11G15.
Keywords. Function theory in Cayley-Dickson algebras, generalized elliptic functions, generalized CM lattices, algebraic number ﬁelds, octonions.

1. Introduction
There are a number of diﬀerent possibilities to generalize complex function theory
to higher dimensions.
One classical and well-established option is to consider functions in several complex variables in Cn where the classical holomorphicity concept is applied separately
to each complex variable, see, for example, [8, 15]. From the viewpoint of algebraic
geometry, the theory of several complex variables provides the natural setting to
study Abelian varieties and curves.
Another possibility is oﬀered by Cliﬀord analysis which considers null-solutions
to a generalized Cauchy-Riemann operator that are deﬁned in a subset of vectors or

## PDF page 2

20

R.S. Kraußhar

paravectors and that take values in an associative Cliﬀord algebra, see, for instance,
[3, 5, 12, 21].
In the recent years one also observes a lot of progress in extending the constructions from the setting of associative Cliﬀord algebras to non-associative CayleyDickson algebras, in particular, to the framework of octonions, see, for example,
[7, 9, 11, 17, 18, 19, 25].
Although one has no associativity anymore, at least in the octonionic case it
was possible to also generalize a number of classical theorems, such as the Cauchy
integral formula or the formulas for the Taylor and Laurent series representations
by following more or less the same line of argumentation as performed in Cliﬀord
analysis. See [16, 26, 30, 31, 32, 33]. Due to the non-associativity one has to bracket
terms in a particular way together. However, apart from this, some of the results
still look very similar to the formulas derived for the Cliﬀord algebra case, at least
at a ﬁrst glance.
Therefore, an important question is whether there appear really essentially different features in the treatment with the more complicated non-associative CayleyDickson algebras. In [18] and [19] the authors present some important structural
diﬀerences. In contrast to the Cliﬀord analysis setting, octonionic regular functions
in the sense of the Riemann approach, called O-regular for short, do not form a left
or right O-module anymore. If f is a left O-regular function, then it is not guaranteed
that f λ is also left O-regular. So, there is no one-to-one correspondence between the
set of monogenic functions in R8 embedded in an associative Cliﬀord algebra Cl07
and O-regular functions.
On the one hand, the lack of this property represents an obstacle in the development of generalizations of many other theorems to the non-associative setting.
On the other hand, there is the challenge to ﬁgure out problems that really require
a treatment with non-associative Cayley-Dickson algebras that cannot be treated in
the Cliﬀord analysis setting.
One aim of this paper to describe one very concrete example.
Cayley-Dickson algebras Ck oﬀer the possibility to consider lattices Ω ⊂ Ck that
admit non-trivial left and right ideals L and R such that LΩ ⊆ Ω, resp. ΩR ⊆
Ω. These are natural generalizations of the so-called classical CM-lattices (lattices
that remain invariant under multiplication by some non-trivial non-integer complex
numbers). These lattices play an important role in the treatment of algebraic points
of elliptic curves, cf. [22]. In particular, in Cayley-Dickson algebras one can consider
lattices which, apart from their algebraic structure of a module, are additionally
closed under multiplication. See also [1] in which some basic properties of generalized
CM-lattices in some graded RF Zn -algebras with deformations have been discussed,
in particular, for RF Z3 -algebras and Cliﬀord algebras.
In fact, one can consider CM-lattices in Cliﬀord algebras. However, Cliﬀord
analysis is restricted to considering functions that are only deﬁned in the subset

## PDF page 3

.

Function Theories in Cayley-Dickson algebras

21

of paravectors and not for variables from the full Cliﬀord algebra (apart from the
particular quaternionic case). Note, however, that the multiplication of two noninteger lattice paravectors from Rn+1 does not give anymore a lattice paravector
from Rn+1 . It gives an element from the full Cliﬀord algebra that involves bivector
parts. Therefore, a monogenic function evaluating CM-values of the form f (μω)
with non-real multiplicators μ ∈ L and non-real lattice paravectors ω ∈ Ω cannot
be deﬁned. In the framework of Cliﬀord analysis, the argument in the function must
again be a paravector. In [20] we introduced a two-sided kind of CM-multiplication,
considering a simultaneous multiplication by the same multiplicator from the left
and from the right to the lattice of the form f (ηωη). In fact, whenever ω and η
are paravectors, then the special product of the form ηωη actually again gives a
paravector. But this is not the case if one applies the multiplicator η only from one
side or if one considers on both sides of ω two diﬀerent multiplicators η and μ. In
these cases one has no paravector anymore, in general.
This obstacle can successfully be overcome using Cayley-Dickson algebras instead. In contrast to the Cliﬀord algebra setting, in the octonions every non-zero
element is invertible.
More generally, in the context of Cayley-Dickson algebras, one can meaningfully
deﬁne functions where the arguments may stem from subsets of the full CayleyDickson algebra and not only from the subset of paravectors.
Now, the function theory in Cayley-Dickson algebras also admits the construction of generalized Weierstraß elliptic functions which satisfy the regularity criterion
in the sense of the Riemann approach. Taking special care of the non-associativity,
the construction of the regular analogue of the Weierstraß ℘-function can be performed in exactly the same way as in Cliﬀord analysis (cf. [21], [27]), namely by
periodizing the partial derivatives of the associated O-regular Cauchy kernel and
adding some convergence preserving terms. This possibility was already roughly
outlined in [20, 21]. Recently, a 7-fold periodic generalization of the cotangent series was explicitly written out particularly for the octonionic case in [25]. This also
underlines the current interest in this topic.
However, the treatment with Cayley-Dickson algebras provides us with a new
feature, if we consider these functions in association with a period lattice that has
a non-trivial one-sided Cayley-Dickson multiplication, since we do not have such an
algebraic structure in the Cliﬀord analysis setting where we are restricted to deﬁne
the functions on the space of paravectors.
At least in the octonionic cases we are able to deduce explicit algebraic relations
between the diﬀerent CM-division values of some prototypes of generalized elliptic
functions. The canonical examples of CM-lattices in Cayley-Dickson algebras are lat√
√
tices whose components stem from multi-quadratic number ﬁelds Q[ m1 , . . . mk ].
In the octonionic case the canonical examples are tri-quadratic number ﬁelds. This is
also in line with the classical complex
case in which we deal with imaginary quadratic
√
number ﬁelds of the form Q[ −m].

## PDF page 4

22

R.S. Kraußhar

The paper is structured as follows.
In Section 2, we summarize the most important facts and notions about hypercomplex numbers in Cayley-Dickson algebras and recall their basic properties which
are used in the sequel of this paper.
In Section 3, we look at integral domains and introduce lattices with CayleyDickson multiplications. We describe them in terms of generalized integrality conditions involving norms and trace expressions. We show that lattices of the form
∑k
Z + 2i=1−1 Zi ωi , where the real components of the primitive periods stem from an
√
√
algebraic ﬁeld of the form Q[ m1 , . . . mk ] and where the elements m1 , . . . , mk
are all mutually distinct positive square-free integers, serve as important non-trivial
examples of lattices with Cayley-Dickson multiplication.
In Section 4, we give a short overview on which basic tools can be carried over
from Cliﬀord analysis to the non-associative setting and explain where we meet structural obstacles. While generalizations of the Weierstraß ζ-function and ℘-function
can even be introduced in general Cayley-Dickson algebras, a number of structural
and technical features require at least an alternative or a composition algebra. So
we turn to focus on octonions in the sequel.
The core piece of the paper is Section 4.3, where we establish algebraic relations between the values of the octonionic generalized Weierstraß ζ-function at a
point and their octonionic CM-division values. In particular, we present an explicit
algebraic formula to calculate the trace of the octonionic division values of the generalized octonionic regular Weierstraß ℘-function. They turn out to be elements of the
number ﬁeld generated by the algebraic elements of the lattice components and the
components of the Legendre-constants which still require an algebraic investigation
in the future.
An exciting topic of future research in this direction would be to ask whether
the octonionic functions can be used to do some class ﬁeld theory. Do these division
values play some role in the construction of Galois ﬁeld extensions of the abovementioned number ﬁelds?
The Jugendtraum of Kronecker addressing the classiﬁcation
of all abelian ﬁeld
√
extensions of imaginary quadratic number ﬁelds Q[ −m] is an extension of the
famous Kronecker-Weber theorem stating that all abelian extensions of Q are contained in cyclotomic extensions.
The solution of Kronecker’s Jugendtraum was the motivation for the development of class ﬁeld theory which took more than 70 years (starting from D. Hilbert’s
famous Zahlbericht [14] and continuing with P. Furtwängler, H. Weber, T. Tagaki,
E. Artin, K. Hey, M. Zorn, M. Matchett, and many others, among them also R.
Fueter, who was a student of D. Hilbert).
It turned out that the complex division values of the associated meromor2 g3
phic doubly periodic function g3g−27g
2 ℘(z) lie in abelian Galois ﬁeld extensions of
2
3
√
Q[ −m], cf. [28], similarly as the division values of the exponential functions lie in
abelian extensions of Q.

## PDF page 5

Function Theories in Cayley-Dickson algebras

23

The construction of algebraic ﬁeld extensions of bi-quadratic number ﬁelds was
a crucial motivation for R. Fueter to develop hypercomplex function theories. He
developed his four-fold periodic monogenic quaternionic elliptic functions exactly
for this purpose, cf. [10, 23]. The framework of Cayley-Dickson algebras now even
addresses more generally than quaternions multi-quadratic number ﬁelds containing
imaginary quadratic number ﬁelds and also biquadratic number ﬁelds considered
by R. Fueter as special subcases, among many others. However, to address multiquadratic extensions of Q one ﬁrst needs to develop a Kummer theory. Even the case
of biquadratic extensions involves additional diﬃculties arising from the splitting of
primes. The question whether one can do some class ﬁeld theory with octonions
hence deﬁnitely represents an exciting open research ﬁeld.
Explicit formulas for the division values of generalized multiperiodic functions
that we developed in this paper might have some interest in this sense, but there are
also many fundamental open problems that need to be solved in order to be able to
give some satisfactory answers to this question.

2. Some basic properties of Cayley-Dickson algebras
We start by introducing the construction principle of Cayley-Dickson algebras. For
details, we refer the reader to, for instance, [1, 2, 16, 29] and elsewhere. They contain
all normed real division algebras, i.e., the ﬁelds of real and complex numbers R and
C, the skew ﬁeld of Hamiltonian quaternions H, and the non-associative alternative
octonions O as special cases.
Following [29], one may start with a ring R that has a two-sided multiplicative neutral element 1 and a non-necessarily commutative and non-necessarily associative multiplication. Furthermore, we impose that it has a “conjugation” antiautomorphism a ↦→ a with the properties that a + b = a + b, ab = b a, and a = a
for all a, b ∈ R. Then one forms pairs of numbers of the form (a, b) and (c, d) and
deﬁnes an addition and multiplication operation by
(a, b) + (c, d) := (a + c, b + d),

(a, b) · (c, d) := (ac − db, ad + cb).

The conjugation is extended by (a, b) := (a, −b).
The simplest choice is to take for the ring R the real numbers R in which we have
a = a. The above-indicated doubling process, called Cayley-Dickson doubling, then
generates in the ﬁrst step the complex number ﬁeld C. It is the ﬁrst Cayley-Dickson
algebra generated by the doubling process starting with R. If we continue performing
this doubling procedure, then we obtain a chain of non-necessarily commutative nor
associative algebras which are the (classical) Cayley-Dickson algebras Ck where k
denotes the step of the doubling procedure. The next Cayley-Dickson algebra C2 is
the skew ﬁeld of Hamiltonian quaternions, where each element can be written in
the form z = x0 + x1 e1 + x2 e2 + x3 e3 . Here, e2i = −1 for i = 1, 2, 3, e1 e2 = e3 ,
e2 e3 = e1 , e3 e1 = e2 , and ei ej = −ej ei for all distinct i, j from {1, 2, 3}. This algebra
is not commutative anymore, but it is still associative. It is still an example of an
associative Cliﬀord algebra. This is not anymore the case after having performed

## PDF page 6

24

R.S. Kraußhar

the following doubling step where we arrive at the octonions O. Octonions have the
form
z = x 0 + x1 e 1 + x2 e 2 + x3 e 3 + x4 e 4 + x5 e 5 + x6 e 6 + x7 e 7
where e4 = e1 e2 , e5 = e1 e3 , e6 = e2 e3 , and e7 = e4 e3 = (e1 e2 )e3 . Like in the
quaternionic case, we have e2i = −1 for all i = 1, . . . , 7 and ei ej = −ej ei for all
mutually distinct i, j ∈ {1, . . . , 7}. The multiplication is visualized in the following
multiplication table:
·
e1
e2
e3
e4
e5
e6
e7
e1 −1
e4
e5 −e2 −e3 −e7
e6
e2 −e4 −1
e6
e1
e7 −e3 −e5
e3 −e5 −e6 −1 −e7
e1
e2
e4
e4
e2 −e1
e7 −1 −e6
e5 −e3
e5
e3 −e7 −e1
e6 −1 −e4
e2
e6
e7
e3 −e2 −e5
e4 −1 −e1
e7 −e6
e5 −e4
e3 −e2
e1 −1
As one can easily deduce with the help of this table, the octonions are not
associative anymore. Therefore, they are no Cliﬀord algebras anymore. However,
one still has a number of nice properties, stemming from the fact that the octonions
still form an alternative composition algebra.
In particular, one has the Moufang relations, guaranteeing that
(ab)(ca) = a((bc)a)
for all a, b, c ∈ O, which, in particular, for c = 1 gives the ﬂexibility condition
(ab)a = a(ba). Moreover, one has the important rule
(ab)b = b(ba) = a(bb) = a(bb)
for all a, b ∈ O.
All the ﬁrst Cayley-Dickson algebras Ck with k ≤ 3 are division algebras.
In the next step of the Cayley-Dickson doubling we then obtain the 16-dimensional sedenions. As mentioned in [16], one has ej ek = −δjk + εjkm em , where δij is
the usual Kronecker symbol and εjkm is the usual epsilon tensor, which is totally
antisymmetric in its indices given by the usual permutation rule for a 3-indexed
antisymmetric tensor with values from {0, 1, −1}.
Up from here we have to deal with zero divisors (which in the case of sedenions
is a measure zero subset) and one even loses the alternative multiplication structure.
Artin’s theorem only guarantees the power associativity for Ck with k ≥ 4. Therefore,
we also lose the general Moufang identities at this level.
k −1
2∑
xj ej of a
But an important property remains: that each element z = x0 +
Cayley-Dickson algebra Ck satisﬁes a quadratic equation of the form
z 2 − S(z)z + N (z) = 0,

j=1

## PDF page 7

Function Theories in Cayley-Dickson algebras

25

where S(z) = z + z = 2x0 is the trace and where
2

N (z) = zz = |z| =

k −1
2∑

x2i

i=0

is the norm of z, cf. [29]. Note that, in general, dimR Ck = 2k .
The only real normed division algebras, where one has the multiplicative property N (zw) = N (z)N (w), are R, C, H, and O. Up from the sedenions it can happen
that N (zw) − N (z) · N (w) ̸= 0, see [16].
To conclude this section, we want to mention that we can get a diﬀerent chain
of algebras if we construct the doubling diﬀerently, as proposed, for instance, in [29].
In the framework of a diﬀerent doubling it is possible to maintain some of the nicer
properties, such as the multiplicativity of the norm.

3. Integrality conditions and lattices with Cayley-Dickson
multiplication
In this section we introduce some number-theoretical concepts. We start with
Deﬁnition 3.1. An element z from a Cayley-Dickson algebra Ck is called rational
(resp. integral) if its trace S(z) and its norm N (z) are a rational number from Q
(or an integer from Z, respectively).
Now suppose that we deal with a set of rational or integral Cayley-Dickson
numbers, respectively. If these numbers satisfy additionally
N (a + b), N (a · b), S(a + b), S(a · b) ∈ Q ( resp. ∈ Z)
for all a, b, then this set of Cayley-Dickson numbers forms a ring and even an algebra which, however, is not necessarily commutative nor associative. In the quaternionic setting, an algebra of rational (integral) quaternions that satisfy the abovementioned conditions is sometimes called a quaternionic rational (integral) Brandt
algebra, cf. [1, 10]. In exactly the same way one can deﬁne octonionic rational and
integral Brandt algebras.
As in the quaternionic setting, also in the octonionic setting one can easily
characterize multiplicatively invariant rational and integral Brandt algebras in the
following way:
Proposition 3.2. Two rational (resp. integral) octonions a, b ∈ O belong to a rational
(integral) non-associative Brandt algebra if and only if 2⟨a, b⟩ and 2⟨a, b⟩ are elements from Q (resp. from Z), where ⟨·, ·⟩ is the usual Euclidean scalar product in
R8 .
Proof. In the octonions one still has
N (ab) = (ab) · (ab) = ab(ba) = a(bb)a = N (a)N (b).

## PDF page 8

26

R.S. Kraußhar

Furthermore,
N (a + b) = (a + b)(a + b) = aa + bb + ab + ba = N (a) + N (b) + 2⟨a, b⟩.
Next, we have
S(ab) = ab + ab = 2⟨a, b⟩,
and trivially S(a + b) = S(a) + S(b).

□

Remark 3.3. If the ring is additionally stable under conjugation, then the second
condition 2⟨a, b⟩ ∈ Q (resp. ∈ Z) can be dropped.
Next we introduce the concept of generalized complex multiplication of lattices
in Cayley-Dickson algebras.
Deﬁnition 3.4 (Lattices with Cayley-Dickson multiplication).
Let Ω2k = Zω0 + Zω1 + · · · + Zω2k −1 be a 2k -dimensional lattice, where all elements
ωh (h = 0, . . . 2k − 1) are R-linearly independent elements from Ck . Then we say that
Ω2k has a left (right) Ck -multiplication if there exists an η ∈ Ck \Z such that
η · Ω2k ⊆ Ω 2k ,

resp.

Ω 2k · η ⊆ Ω2 k .

In the case where we have ηω ∈ Ω2k for all η, ω ∈ Ω2k we say that the lattice is
closed under multiplication. In this case, the lattice forms a non-associative ring.
In the more general case, the (non-associative) ring of left multiplicators form
a left (resp. right) ideal. Lattices with Cayley-Dickson multiplication can be constructed by choosing the primitive generators from a rational or integral Brandt
algebra. The most important examples are lattices whose components stem from
multiquadratic number ﬁelds. The canonical examples can be constructed as follows.
Take k mutually distinct square-free positive integers m1 , . . . , mk .
Then take a lattice of the form
Z + Zω1 + · · · + Zωk + Zω1 ω2 + · · · + Zωk−1 ωk + · · · + Z((ω1 · · · ωk−2 )ωk−1 ) · ωk ,
where
ω0 := 1,

√
ω1 := α1 m1 e1 ,
.. .. ..
. . .
√
ωk := αk mk ek ,
√
ω1 · ω2 := α1 α2 m1 m2 e1 e2 ,
.. .. ..
. . .
√
((ω1 · · · )ωk−1 ) · ωk := α1 · · · αk m1 · · · mk ((e1 · · · )ek−1 ) · ek ,

## PDF page 9

Function Theories in Cayley-Dickson algebras

27

and where one chooses all the appearing components αj1 ···jr to be rational numbers.
An arbitrary Z linear combination of these lattice elements then has the form
γ0 + γ1 ω1 + · · · + γk ωk + · · · + γ1···k (ω1 (· · · ))ωk
√
√
= γ0 + γ1 α1 m1 e1 + · · · + γk αk mk ek + · · ·
√
+ γ1···k α1···k m1 · · · mk ((e1 · · · )ek−1 )ek ,
where all γj1 ···jr are integers. As one easily may verify, the product of such two
elements again gives an element of the same form, for instance,
√
ω1 · ω2 = α1 α2 m1 m2 e1 e2 .
Note that in Ck one has that (ej ek )em = ±(em ej )ek which, however, means that the
second structure constants are not anti-symmetric, in general. In the case where all
elements αj1 ···jr are integers, then one easily gets lattices being even closed under
multiplication. One can directly observe that these lattices all form rational (resp.
integral) Brandt algebras in the Cayley-Dickson algebra and that they are stable
under conjugation. The components of the primitive lattice generators are elements
√
√
from the multiquadratic number ﬁeld Q[ m1 , . . . , mk ]. In the particular complex
case we are dealing with the classical CM-lattices of the form Z + Zτ where τ ∈
√
Q[e1 m1 ]. In the octonionic case we deal with tri-quadratic number ﬁelds. Slightly
more generally, consider eight R linearly independent octonionic lattice generators
ωh (h = 0, . . . , 7) where
√
√
√
ωh = αh0 + αh1 m1 e1 + αh2 m2 e2 + αh3 m3 e3
√
√
√
+ αh4 m1 m2 e4 + αh5 m1 m3 e5 + αh6 m2 m3 e6
√
+ αh7 m1 m2 m3 e7 ,
αhj ∈ Q.
It is easy to check that any product ωh ωl turns out to be of the same form.
For the sake of completeness, we introduce the notation W = (ωhl )hl (h, l ∈
{0, . . . , 2k − 1}) for the matrix of the components of the lattice generators ωh represented in the basis ωh = ωh,0 + ωh,1 e1 + ωh,2 e2 + · · · + ωh,2k −1 (e1 (· · · )ek−1 )ek .
Furthermore, det(W ) stands for its determinant and θh,j represents the adjoint determinant, also called co-factor, associated with the element ωh,j .

4. Algebraic relations between the CM-division values of
octonionic regular elliptic functions
4.1. Cayley-Dickson regular functions and their basic properties
To make the paper self-contained, we brieﬂy summarize the basic facts on CayleyDickson regular functions in the sense of the Riemann approach and, in particular, on
octonionic regular (monogenic) functions that are needed to prove the main results
of this paper. Apart from this regularity concept there is also the concept of sliceregularity in these algebras. See, for instance, [11] and the very recent paper [17]
which is based on a diﬀerent geometric splitting. However, in this paper we restrict
ourselves to focus entirely on the following deﬁnition.

## PDF page 10

28

R.S. Kraußhar

Deﬁnition 4.1 (Cayley-Dickson regularity (cf. [7, 16])). Let U be an open subset in
the Cayley-Dickson algebra Ck . A function f : U → Ck is called left (right) CayleyDickson regular if Df (z) = 0 (resp. f (z)D = 0) for all z ∈ U , where
2k −1

∑ ∂
∂
+
ej
D :=
∂x0
∂xj
j=1

is the generalized Cauchy-Riemann operator in the Cayley-Dickson algebra Ck .
In the case k = 3 we get the class of octonionic monogenic functions, discussed
in [6, 13, 25, 26, 30, 31, 32, 33], which will be called O-regular functions for short in
all that follows. If k = 4, then we deal with the sedenionic monogenic functions, see
also [16]. The general case has been addressed in [7].
All left and right Cayley-Dickson regular functions are also harmonic. They
k −1
2∑
∂2f
= 0.
satisfy
∂x2
j=0

i

As important example of a function that is left and right Cayley-Dickson regular
serves the generalized Cauchy kernel function q0 (z) := z2k . Precisely speaking, it is
|z|

left and right regular at any point z ̸= 0. In the octonionic case one has q0 (z) = |z|z 8 .
As a direct consequence, also all partial derivatives
qn (z) :=

∂ |n|
n k

−1
∂xn1 1 · · · ∂x2k2−1

q0 (z),

n := (n1 , . . . , n2k −1 ), |n| =

k −1
2∑

nj ,

j=1

are left and right Ck -regular at all points with z ̸= 0.
Following K. Imaeda, in the algebras Ck up from k > 3 one cannot set up a general Cauchy integral formula with this kernel function anymore, because the second
structure constants are not anti-symmetric in these cases, cf. [16]. This represents a
serious obstacle. This might be a reason why so far there has not been spent that
much eﬀort to develop a comprehensive generalized function theory in the algebras
Ck with k > 3.
However, in the octonionic case, one still gets a Cauchy integral formula. Nevertheless, notice that in contrast to the Cliﬀord analysis setting, one has to be careful
with how to bracket the expressions together. From [32] and elsewhere we may recall:
Theorem 4.2 (Octonionic Cauchy-integral formula). Let U ⊆ O be open and K ⊂ U
be the closure of an open domain in O with an orientable strongly Lipschitz boundary
∂K. Let f : U → O be a left (right) O-regular function. Then, under the condition
that z ∈ int(K) we have
(
)
∫
1
q0 (w − z) · dσ(w)f (w) ,
f (z) =
ω8
∂K

## PDF page 11

.

Function Theories in Cayley-Dickson algebras

respectively,
1
f (z) =
ω8

∫ (

29

)
f (w)dσ(w)

· q0 (w − z),

∂K

π4

where ω8 = 3 is the surface measure of the unit hypersphere in O. Here dσ(w) =
7
∧
∧
∑
(−1)i ei dwi is the oriented octonionic surface diﬀerential form where dwi = dw0 ∧

i=0

dw1 ∧ · · · dwi−1 ∧ dwi+1 · · · ∧ dw7 .
Following [16], even in the non-alternative cases, every function f : U → Ck
that is left (right) Ck -regular in an open neighborhood around a point a ∈ U can
locally be expanded in a Taylor series of the form
f (z) =

+∞
∑

Vn (z − a)an ,

|n|=0

resp.

f (z) =

+∞
∑

an Vn (z − a),

|n|=0

|n|

∂
where an := ∂x
n f (a) are hypercomplex numbers from Ck and the polynomials Vn (z)
are the generalized Fueter polynomials. This is a consequence of the power associativity that remains valid in all Cayley-Dickson algebras.
In the Cayley-Dickson algebra setting, the Fueter polynomials have the form
∑
1
Vn (z) =
(Zπ(n1 ) (Zπ(n2 ) (· · · (Zπ(n2k −2 ) Zπ(n2k −1 ) ) · · · ))).
|n|!
π∈perm(n)

Here, perm(n) denotes the set of all distinguishable permutations of the sequence
(n1 , n2 , . . . , n2k −1 ) and Zi := Vτ (i) (z) := xi − x0 ei for all i = 1, . . . , 2k − 1, see [31,
Theorem C, p. 208], where the octonionic case has been treated speciﬁcally.
As in the complex and Cliﬀord analysis setting, Cauchy’s integral formula allows
us easily to show the particular octonionic case the following.
Theorem 4.3 (Octonionic Liouville theorem). If f : O → O is left or right O-regular
and bounded over the whole algebra O, then f must be a constant.
Proof. We describe the left O-regular case. By performing partial diﬀerentiation on
the octonionic Cauchy integral formula, one directly obtains that
∫
(
)
1
∂
f (z) =
qτ (i) (w − z) · dσ(w) · f (w) .
∂xi
ω8
|z−w|=r

Thus, in view of |qτ (i) (z − w)| ≤ M |z − w|−8 (with a real constant M ) and since the
4 7
measure of the surface of a 8-dimensional ball of radius r is π 3r , we have
∣ ∂
∣ M
∣
∣
f (z)∣ ≤
sup{|f (z)|},
∣
∂xi
r z∈O
which tends to zero, because supz∈O {|f (z)|} is bounded. Hence, f must be constant.
□

## PDF page 12

30

R.S. Kraußhar

Note that we have used the Cauchy integral formula which is not available for
higher-dimensional Cayley-Dickson algebras. Therefore, this simple proof cannot be
extended directly to the more general algebras Ck for k > 3.
More generally, on can also establish that even every function f : O → O that
is harmonic and bounded over the whole algebra O is a constant. This actually can
be done by classical harmonic analysis.
In particular, for the octonionic case one may also introduce in view of the
property of being a composition algebra:
Deﬁnition 4.4 (Octonionic meromorphicity). Let U ⊆ O be an open set. Suppose
that a ∈ U and that f : U \{a} → O is left (right) O-regular. Then the point a is
called a non-essential isolated singularity of f if there exists a non-negative integer
n such that |z − a|n |f (z)| remains bounded in a neighborhood around a. Left (right)
O-regular functions that have at most unessential singular points in a discrete subset
S ⊂ O are called left (right) O-meromorphic.
More generally, one can also extend the notion of octonionic meromorphicity to
functions which have non-essential singularities on manifolds with boundary, namely,
by deﬁning non-essential singular sets S in the same way as W. Nef did for the
quaternionic case in [24, 10]. This is technically more complicated. For simplicity
we therefore restrict ourselves to only address octonionic functions with isolated
singularities in this paper, although a more general treatment is possible.
4.2. Basic properties of octonionic regular elliptic functions
In this subsection we brieﬂy summarize the most basic properties of octonionic
regular elliptic functions. We start by giving its deﬁnition which is similar to that
addressing the quaternionic case in [10] and to that addressing paravector-valued
functions with values in associative Cliﬀord algebras in [21].
Deﬁnition 4.5. Let Ω8 = Zω0 +. . .+Zω7 be an arbitrary eight-dimensional octonionic
lattice; that means that ω0 , . . . , ω7 are supposed to be eight R-linearly independent
octonions. Further, let S ⊂ O be a discrete subset. A left (right) O-regular function
f : O\S → O that has atmost unessential singularities at the points of S is called a
left (right) O-regular elliptic function if it satisﬁes at each z ∈ O\S that f (z + ω) =
f (z) for all ω ∈ Ω8 and S + ω = S for all ω ∈ Ω8 .
Remark 4.6. A crucial diﬀerence to the Cliﬀord analysis setting consists in the fact
that the set of left (right) O-regular elliptic functions is not a right (left) nonassociative O-module, see [19] Remark 4.4. But one still has the property that left
(right) O-regularity is inherited by partial derivation of such a function.
Like in complex and Cliﬀord analysis (cf. [21, 27]) it is not possible to ﬁnd any
non-constant Ω8 -periodic function that is left or right O-regular on the whole algebra
O. This is due to the fact that the topological quotient O/Ω8 is a compact 8-torus.
However, any function that is O-regular on the whole algebra O is, in paticular,
continuous. Hence, it is bounded on the topological quotient torus, which means

## PDF page 13

Function Theories in Cayley-Dickson algebras

31

that it is bounded on the closure of each period cell. Therefore, as a consequence of
the generalized octonionic Liouville theorem, such a function must be a constant.
The same holds under the weaker condition of being harmonic.
Therefore, a non-constant O-regular or harmonic Ω8 -periodic function must
have singularities.
Examples. The simplest non-trivial examples of O-regular functions are given in
terms of the Ω8 -periodization of the partial derivatives of the octonionic Cauchy
kernel function q0 (z). Applying the classical Eisenstein series convergence argument,
the series
]
∑ [( ∂ |n| )
℘n (z) :=
q
(z
+
ω)
0
∂xn
ω∈Ω8

converges normally whenever |n| :=

∑7

j=1 nj ≥ 2, since

∑
ω∈Ω8 \{0}

|ω|−(7+α) is conver-

gent if and only if α > 1. In the limit case where n = τ (i) is ∑
a multi-index of length 1
(where nj = δij for one particular i ∈ {1, . . . , 7}) the series ω∈Ω8 qτ (i) (z + ω) where
∂
q0 (z) is not convergent anymore. However, as usual, convergence can
qτ (i) (z) = ∂x
i
be achieved by adding a convergence-preserving term in the way
)
∑ (
qτ (i) (z + ω) − qτ (i) (ω) ,
℘τ (i) (z) = qτ (i) (z) +
ω∈Ω8 \{0}

similar to the Cliﬀord algebra case, cf. [10, 21, 27].
In fact, in complete analogy to the Cliﬀord analysis setting one can prove:
Proposition 4.7. The series ℘τ (i) (z) are Ω8 -periodic.
Proof. To prove the periodicity, one can apply the same chain of arguments as in
the complex case. From a direct rearrangement argument it is clear that for |n| ≥ 2
the series ℘n satisfy ℘n (z + ω) = ℘n (z) for all z ∈ O\Ω8 and all ω ∈ Ω8 . So, for
any i, the diﬀerence of ℘τ (i) (z + ω) − ℘τ (i) (z) must be a constant, say C. Let ωh
be a primitive period of Ω8 and consider z = − ω2h . Furthermore, note that ℘τ (i)
is an even function, because each term in the series representation is even. qτ (i) is
even, because it is the partial derivative of q0 , which obviously is odd. Therefore,
the diﬀerence ℘τ (i) (z + ω) − ℘τ (i) (z) becomes ℘τ (i) (− ω2h + ω) − ℘τ (i) (−(− ω2h )) =
℘τ (i) ( ω2h ) − ℘τ (i) ( ω2h ) = 0, thus C = 0 and the Ω8 periodicity is established, since ωh
was an arbitrarily chosen primitive period.
□
Remark 4.8. If we consider the subseries that arises by summing only over the
lattice points of a seven-dimensional sublattice Ω7 whose elements ω ∈ Ω7 satisfy all
S(ω) = 0, where S(ω) = ω + ω means the trace as deﬁned in Deﬁnition 3.1, then we
deal with a partial derivative of the octonionic generalized cotangent function from
[25].

## PDF page 14

32

R.S. Kraußhar

The left O-regular primitive of the fully Ω8 -periodic function ℘τ (i) given by
ζ(z) := q0 (z) +

(

∑

q0 (z + ω) − q0 (ω) +

ω∈Ω8 \{0}

7
∑

)
Vτ (j) (z)qτ (j) (ω)

j=1

provides us with the direct analogue of the Weierstraß ζ-function, satisfying, like
∂ζ
= ℘τ (i) . ζ(z) is not Ω8 -periodic anymore. However, ζ(z) is
in the Cliﬀord case, ∂x
i
quasi Ω8 -periodic, which means that
ζ(z + ωh ) − ζ(z) = ηh ,
where ηh are octonionic constants, the so-called octononic Legendre constants. In
the latter equation ωh (h = 0, . . . , 7) represent the primitive periods of Ω8 . The
Legendre constants are given by
ηh = ζ(−

ωh
ωh
ωh
+ ωh ) − ζ(− ) = 2ζ( ),
2
2
2

because ζ is an odd function which can readily be seen by a rearrangement of the
series.
Remark 4.9. The left O-regularity of ζ(z) follows from the application of the Weierstraß convergence theorem from [32, Theorem 11] to each particular term of the
series. Note that
)
∂ (
xj − x0 ej qτ (j) (ω)
D[Vτ (j)(z)qτ (j) (ω) ] =
∂x0
]
[ ∂ (
)
+ ej
xj − x0 ej qτ (j) (ω)
∂xj
]
)
∑ [ ∂ (
+
ej
xj − x0 ej qτ (j) (ω)
∂xi
i̸=0,j

= −ej qτ (j) (ω) + ej qτ (j) (ω) = 0.
The left and right O-regularity of the functions ℘τ (i) and ℘n with |n| ≥ 2 is evident.
The detailed proof of convergence follows along the same lines as in the Cliﬀord
case. Hence, we omit it. See [21] and see also [25] for the particular octonionic
cotangent series constructions treated there.
Remark 4.10. The same series constructions can also be made in the general 2k dimensional Cayley-Dickson algebras by inserting the functions q0 (z) := z2k or
|z|

their partial derivatives, respectively, in the series constructions. The convergence
conditions remain the same. However, notice that we do not have an analogue of
Liouville’s theorem in the more general setting due to the lack of a direct analogue
of Cauchy’s integral formula. Anyway, the Taylor expansion representation of the
Cauchy kernel function and its partial derivatives which are required in the convergence proof remain valid.

## PDF page 15

Function Theories in Cayley-Dickson algebras

33

4.3. Octonionic regular elliptic functions for generalized CM-lattices and their
division values
The results presented in this subsection only address the octonionic setting, because
the proofs explicitly use the alternative property of the octonions which is lost in
the higher-dimensional Cayley-Dickson algebras Ck with k > 3.
Before we start, we need to establish some important preparatory statements.
First we note that
(λz) · μ
μ · (λz)
=
8
|(λz) · μ|
|μ|8 |λz|8
(
)
μ · (zλ)
=
=
q
(μ)
·
q
(z)q
(λ)
.
0
0
0
|μ|8 |z|8 |λ|8

q0 ((λz) · μ) =

Analogously, one obtains
λ · (zμ)
zμ · λ
=
8
|λ · (zμ)|
|λ|8 |zμ|8
(
)
(μ z) · λ
=
=
q
(μ)q
(z)
· q0 (λ).
0
0
|μ|8 |z|8 |λ|8

q0 (λ · (zμ)) =

Here we used the conjugation property ab = ba.
Now we want to show the following formula.
Proposition 4.11. For each λ, μ, z ∈ O\{0} we have
(

)
μ · q0 ((λz) · μ) · λ =

1
q0 (z).
(N (μ)N (λ))3

(1)

Proof. Here, we have to argue very carefully, since we do not have associativity. So,
we do it step by step. First we note that
)
μ · q0 (zμ) = μ ·
(

(

zμ
|zμ|8

)

(
=μ·

μz
|μ|8 |z|8

)
=

1
(μ μ)z
=
q0 (z),
8
8
|μ| |z|
|μ|6

where we exploited the alternating property μ(μ z) = (μμ)(z). Here, we exploited
a special property of the octonions that cannot be extended to sedenions or the
following Cayley-Dickson algebras.

## PDF page 16

34

R.S. Kraußhar

(
)
Next we put f (z) := μ · q0 (zμ) = |μ|1 6 q0 (z). And now we can conclude that
(
)
(
)
μ · q0 (λz) · μ)
· λ = f (λz) · λ
1
q0 (λz) · λ
|μ|6
(
)
λz
1
·λ
=
|μ|6 |λz|8

=

(z λ) · λ
z · (λ · λ)
=
6
8
8
|μ| |z| |λ|
|μ|6 |z|8 |λ|8
1 1
1
=
q0 (z) =
q0 (z).
|μ|6 |λ|6
(N (μ)N (λ))3

=

□

Remark 4.12. We wish to emphasize clearly that this formula holds for octonions.
Our argumentation cannot be extended beyond octonions in the next steps of the
usual Cayley-Dickson doubling, at least not by using this chain of arguments, because
we explicitly used the alternative property.
1
As a direct consequence of the fact that (N (μ)N
is real-valued we obtain the
(λ))3
following important statement.
)
(
(
)
· λ and, in
Proposition 4.13. For all λ, μ ∈ O\{0} the functions μ · q0 (λz) · μ)

particular, q0 (λz) · λ and μ · q0 (zμ) are left and right O-regular at each z ∈ O\{0}.
Remark 4.14. Note again that in contrast to the Cliﬀord analysis setting the property
of the latter proposition is not immediate, because left (right) O-regular functions
do not form a right (left) O-module as mentioned before. The property is true for
the particular function q0 but at least as far as we know it is not evident for any
arbitrary left (right) O-regular function f .
Now let particularly Ω8 = Z + Zω1 + · · · + Zω7 (ω0 = 1) be a lattice with
octonionic multiplication as deﬁned in Section 3. Suppose that λ ∈ O\R is a nontrivial multiplicator from a left ideal L with LΩ8 ⊆ Ω8 and assume that μ ∈ O\R is
a non-trivial multiplicator from a right ideal R with Ω8 R ⊆ Ω8 .
We look at the associated octonionic left O-regular Weierstraß ζ-function
7
(
)]
∑
∑ [
ζ(z) = ζ(z, Ω) = q0 (z) +
q0 (z + ω) − q0 (ω) +
Vτ (j) (z) qτ (j) (ω) .
ω∈Ω8 \{0}

j=1

If Ω8 is such a lattice and L is such a left ideal, then we can ﬁnd a λ ∈ L\R
such that λω ∈ Ω8 for all ω ∈ Ω8 .
So, the function ζ(λz) · λ is a well-deﬁned quasi-elliptic function on the same
lattice Ω8 , since λω ∈ Ω8 for all ω ∈ Ω8 . Note that quasi-ellipticity means that the
function is Ω8 -periodic up to a constant.

## PDF page 17

Function Theories in Cayley-Dickson algebras

35

It is easy to see that it is at least harmonic when applying the Weierstraß convergence theorem to each term of the series. According to Proposition 4.13( the term
)
q0 (λz)λ is left and right O-regular and hence harmonic. The terms Vτ (j) (z) qτ (j) (ω)
are all linear and therefore in the kernel of the Laplacian. Since the Laplacian is a
scalar operator, one has
Δ[q0 (λz + ω)λ] = Δ[q0 (λz + ω)]λ.
So, since 0 = Δ[q0 (λz)λ] and since O is a division algebra, one also has Δ[q0 (λz)] =
0. Since ω ̸= 0, one can ﬁnd a t ∈ O such that ω = λt. Applying a linear shift in the
argument also leads to the fact that
Δ[q0 (λz + ω)] = Δ[q0 (λz + λt)] = Δ[q0 (λ(z + t))]
[(
) λ ]
)] λ
[(
(z
+
t)
= 0,
= Δ q0 (z + t)
=
Δ
q
0
|λ|8
|λ|8
since the diﬀerential remains invariant under the shift z + t.
Analogously, there are elements μ ∈ R\R such that ωμ ∈ Ω8 for all ω ∈ Ω8 , so
that the function μ · ζ(zμ) is also a well-deﬁned quasi-elliptic function again on the
same lattice, since also ωμ ∈ Ω8 for all ω ∈ Ω8 . Here again, we can establish that
this function is at least harmonic.
More generally, and bearing in mind the non-associativity, the two functions
(
)
1
(z) := μ · ζ((λz) · μ) · λ
ζλ,μ
and

(
)
2
ζλ,μ
(z) := μ · ζ(λ · (zμ)) · λ

are well-deﬁned at least harmonic quasi-elliptic functions for all λ ∈ L, μ ∈ R, since
(λΩ8 ) · μ ⊆ Ω8 μ ⊆ Ω8
and
λ · (Ω8 μ) ⊆ λΩ8 ⊆ Ω8 .
These inclusions are true, because Ω8 is a lattice with Cayley-Dickson multiplication
(CM-property).
For the sake of clarity, the quasi-periodicity (periodicity up to a constant) follows explicitly by the calculations
(
)
1
(z + ω) = μ · ζ((λ[z + ω]) · μ) · λ
ζλ,μ
(
)
= μ · ζ((λz) · μ + (λω) · μ) · λ
(
)
= μ · ζ((λz) · μ + ω ∗ ) · λ
(
)
= μ · ζ((λz) · μ) + C(w∗ ) · λ
(
)
(
)
= μ · ζ((λz) · μ) · λ + μ · C(ω ∗ ) · λ
1
(z + ω) + C̃(ω ∗ ),
= ζλ,μ

## PDF page 18

36

R.S. Kraußhar

where C(ω ∗ ) and C̃(ω ∗ ) are two constants depending on ω ∗ , which is deﬁned by
ω ∗ := (λω) · μ, which is an element from Ω8 , because of the CM-property.
1 (z) and ζ 2 (z), in general, diﬀer from each other
Note that both functions ζλ,μ
λ,μ
as a consequence of the lack of associativity. For the sake of convenience we focus
1 (z), since the other version can be treated
from now on the function ζλ,μ (z) := ζλ,μ
analogously.
(
)
The function μ · ζ((λz) · μ) · λ is singular if and only if (λz) · μ = ω for a lattice

point ω ∈ Ω8 . This is equivalent to (λz) = ωμ−1 ⇐⇒ z = λ−1 · (ωμ−1 ). Thus, the
1 (z) has isolated point singularities at exactly the points z = λ−1 ·(ωμ−1 )
function ζλ,μ
where ω runs through Ω8 .
By a counting argument, we obtain that ζλ,μ has exactly N (λμ)4 -many isolated
point singularities in the fundamental periodic cell
F := {x = α0 + α1 ω1 + · · · + α7 ω7 | 0 ≤ αj < 1, j ∈ {0, . . . , 7}},
which, in particular, contains 0.
The set of all these singularities that lie in the fundamental set will be denoted
by Vλ,μ;Ω8 in all that follows.
Remark 4.15. In the simple case where λ = 2 and μ = 1, this set consists exactly of those points where the coordinates either have the value zero or 1/2, whose
cardinality evidently equals 28 = N (2)4 .
Now we have all pre-requisites to formulate and prove our main theorem.
Theorem 4.16. Let Ω8 = Z + Zω1 + · · · + Zω7 , (ω0 := 1) be an octonionic lattice with
octonionic multiplication with the properties and notations as described previuously.
The trace of the octonionic division values of the O-regular elliptic functions ℘τ (i)
(i = 1, . . . , 7) can be expressed by
∑
℘τ (i) (v)
v∈Vλ,μ;Ω8 \{0}

[ 7
]
7
7
)
(
∑
∑
(N (λ)N (μ))3 ∑
=−
Θ hi μ · (
nhj ηj ) · λ − N (λ)N (μ)
Θ hi η h ,
det(W )
h=0

j=0

h=0

where Θhi denotes the adjoint determinant (co-factor) associated with the lattice
component ωhi and where
Vλ,μ;Ω8 := {v ∈ F | v = λ−1 · (ωμ−1 ), ω ∈ Ω8 }.
Proof. As a consequence of formula (1), we may infer that the Laurent expansion of
the function ζλ,μ centered at zero has the form
(
)
1
ζλ,μ (z) = μζ((λz) · μ) · λ =
q0 (z) + A(z),
(N (μ)N (λ))3
where A is a function that is at least harmonic in some neighborhood of 0.

## PDF page 19

.

Function Theories in Cayley-Dickson algebras

Conversely, the function

∑

37

ζ(z + v)

v∈Vλ,μ;Ω8

can be written in the form q0 (z) + B(z), where B(z) is also a function that is
deﬁnetely left O-regular around 0. Therefore, the diﬀerence function
∑
1
·
ζ(z + v)
(2)
f (z) := ζλ,μ (z) −
3
(N (μ)N (λ))
v∈Vλ,μ;Ω8

is at least harmonic around 0, too. Similarly, one gets the same result if one considers
the Laurent expansion around another singular point v ∈ Vλ,μ;Ω8 .
The same is true for all the partial derivatives (i ∈ {0, . . . , 7})
∂
∂
1
f (z) =
ζλ,μ (z) −
∂xi
∂xi
(N (μ)N (λ))3
=

∂
1
ζλ,μ (z) −
∂xi
(N (μ)N (λ))3

∑
v∈Vλ,μ;Ω8

∑

∂
ζ(z + v)
∂xi
℘τ (i) (z + v).

(3)

v∈Vλ,μ;Ω8

The functions ℘τ (i) (z + v) are all Ω8 -periodic, because we proved that ℘i (z) is Ω8
periodic.
∂
The functions ∂x
ζλ,μ (z) are Ω8 -periodic, too, because ζλ,μ (z + ω) − ζλ,μ (z)
i
turned out to be constant, so the partial derivatives of this expression must be
Ω8 -periodic.
∂f
Consequently, each function fi := ∂x
is Ω8 -periodic and must be at least hari
monic on the entire algebra O, since it has no singularity inside of Vλ,μ;Ω8 . So, in view
of Liouville’s theorem there are octonionic constants Ci ∈ O such that fi (z) = Ci
for all z. Now we make the ansatz
∑
∑
1
ζλ,μ (z) =
ζ(z
+
v)
+
Vτ (j) (z)Cj + C,
(4)
(N (μ)N (λ))3
j=1

v∈Vλ,μ;Ω8

where C is a further octonionic constant.
Now let ωh be a primitive period of Ω8 (h = 0, 1, . . . , 7). Then we have
(
)
(
)
·λ
ζλ,μ (z + ωh ) = μ · ζ λ(z + ω) · μ)
=

1
(N (μ)N (λ))3
+

7
∑
j=1

for all h ∈ {0, 1, . . . , 7}.

∑

ζ(z + ωh + v)

v∈Vλ,μ;Ω8

Vτ (j) (z + ωh )Cj + C

## PDF page 20

38

R.S. Kraußhar

Now the crucial aspect is that the lattice Ω8 has octonionic multiplication of
the form (λΩ8 )μ ⊆ Ω8 and λ(Ω8 μ) ⊆ Ω. Therefore, there exist integers nhj ∈ Z such
that
7
∑
nhj ω j .
(5)
(λωh ) · μ =
j=0

In view of the Legendre relation that we stated in the previous subsection, we have
the additive relation
7
∑
nhj η j
(6)
ζ((λz) · μ + (λωh ) · μ) = ζ((λz) · μ) +
j=0

with the octonionic Legendre constants η0 , . . . , η7 .
Applying formula (4) we get
)
(
(
)
·λ
μ · ζ (λ(z + ωh )) · μ
=

1
(N (μ)N (λ))3

∑

ζ(z + ωh + v) +

7
∑

Vτ (j) (z + ωh )Cj + C.

j=1

v∈Vλ,μ;Ω8

Using the Legendre relation, the latter equation is equivalent to
)
(
(
)
·λ
μ · ζ (λz) · μ + (λωh ) · μ
=

1
(N (μ)N (λ))3
+

7
∑

[

∑

]
ζ(z + v) + ηh

v∈Vλ,μ;Ω8

Vτ (j) (z + ωh )Cj + C.

j=1

Applying (6) to the previous equation leads to
(
)
7
(
)
( ∑
)
μ · ζ (λz) · μ
· λ + μ(
n hj η j ) · λ
j=0

=

1
(N (μ)N (λ))3
+

7
∑

∑

[

7
] ∑
Vτ (j) (z)Cj + C
ζ(z + v) + ηh +
j=1

v∈Vλ,μ;Ω8

Vτ (j) (ωh )Cj .

j=1

Since the ﬁrst term of the left-hand side equals the expression of the sum of the ﬁrst
two terms of the right-hand side in view of (4), we obtain the relation
(

μ·(

7
∑
j=0

)
n hj η j ) · λ =

1
(N (μ)N (λ))3

∑
v∈Vλ,μ;Ω8

ηh +

7
∑
j=1

Vτ (j) (ωh )Cj .

## PDF page 21

Function Theories in Cayley-Dickson algebras

39

Next, since the cardinality of Vλ,μ;Ω8 equals N (λμ)4 , we have
∑
ηh = N (λμ)4 · ηh .
v∈Vλ,μ;Ω8

Thus, we arrive at
7
7
)
(
∑
∑
nhj ηj ) · λ = N (λμ)ηh +
(ωhj − ej ωh0 )Cj ,
μ·(
j=0

where we put ωh =

7
∑
j=0

(7)

j=1

ωhj ej for the representation of the primitive periods ωh in

the coordinates of the canonical basis elements e0 , e1 , . . . , e7 .
Next, let us write Θhj for the adjoint determinant (co-factor) associated with
the element ωhj . Then, classical linear algebra tells us that
7
∑

ωhi Θhl = δil det(W ).

(8)

h=0

Note that the elements Θhl are all real numbers. Combining the formula (8) with (7),
we obtain that
7 [
7
7
) ]
(
∑
∑
∑
nhj ηj ) · λ − N (λ)N (μ)
Θ hi η h
Θ hi μ · (
j=0

h=0
7 ∑
7 (
∑

=

h=0 j=1

h=0

)

Θ hi ω hj − e j Θ hi ω h0 C j .
⏟ ⏞⏞ ⏟
=0

The underbraced expression Θhi ωh0 vanishes, because we always have δi0 = 0, since
i ̸= 0.
In view of (8) the latter equation simpliﬁes to
7 [
∑

7
7
) ]
∑
∑
nhj ηj ) · λ − N (λ)N (μ)
Θhi ηh = Ci det(W ).
Θ hi μ · (

(

j=0

h=0

h=0

Thus, for i = 1, . . . , 7 we obtain
) ]
(
7 [
7
7
∑
∑
∑
nhj ηj ) · λ − N (λ)N (μ)
Θ hi η h
Θ hi μ · (
Ci =

h=0

j=0

h=0

det(W )

.

Now we are in position to calculate the traces of the octonionic Weierstraß’ functions.
First of all we recall that
1
ζ(z)
ζλ,μ (z) −
(N (λ)N (μ))3
1
=
(N (λ)N (μ))3

∑
v∈Vλ,μ;Ω8 \{0}

ζ(z + v) +

7
∑
j=1

Vτ (j) (z)Cj + C.

## PDF page 22

40

R.S. Kraußhar

Since ζ is an odd function, ζλ,μ is an odd function, too. Consequently,
ζλ,μ (z) −

1
ζ(z) = O(z)
(N (λ)N (μ))3

around zero, because the singular parts cancel out, following from Proposition 4.11.
In view of lim ℘τ (i) (z) − qτ (i) (z) = 0 for all i = 1, . . . , 7, which is clear from the
z→0

series representation, because lim qτ (i) (z + ω) − qτ (i) (ω) = 0, one even has that the
z→0

expression on the right-hand side is of order O(z 3 ).
So, in particular,
)
(
1
ζ(z)
= 0,
lim ζλ,μ (z) −
z→0
(N (λ)N (μ))3
and since lim Vτ (j) (z) = 0, one has
z→0

1
(N (λ)N (μ))3

∑

ζ(v) = −C.

v∈Vλ,μ;Ω8 \{0}

Next,
∂ζλ,μ
1
−
℘
∂xi
(N (λ)N (μ))3 τ (i)
is an even expression and of the form O(z 2 ) around the origin. So,
)
( ∂ζ (z)
1
λ,μ
−
℘ (z) = 0.
lim
z→0
∂xi
(N (λ)N (μ))3 τ (i)
On the other hand,
∂ζλ,μ (z)
1
−
℘ (z)
∂xi
(N (λ)N (μ))3 τ (i)
=

1
(N (λ)N (μ))3

∑

℘τ (i) (z + v) +

v∈Vλ,μ;Ω8 \{0}

7
∑
∂
V (z)Cj .
∂xi τ (j)
j=1

Thus, with the same limit argument we obtain that
∑
1
℘τ (i) (v) = −Ci .
(N (λ)N (μ))3
v∈Vλ,μ;Ω8 \{0}

If we apply the formula for the expression of the constants Ci derived above,
then we ﬁnally arrive at the desired trace formula for the octonionic CM-division
values of the associated ℘τ (i) -function,
∑
℘τ (i) (v)
v∈Vλ,μ;Ω8 \{0}

[ 7
]
7
7
)
(
∑
∑
(N (λ)N (μ))3 ∑
=−
Θ hi μ · (
nhj ηj ) · λ − N (λ)N (μ)
Θ hi η h
det(W )
h=0

j=0

for each i = 1, . . . , 7, and the theorem is proved.

h=0

□

## PDF page 23

Function Theories in Cayley-Dickson algebras

41

Remark 4.17. For the sake of completeness we want to re-emphasize that the constant C gives up to a minus sign multiplied with the third power of the quadratic
norm expressions exactly the value of the trace of the CM-division values of the
O-regular Weierstraß ζ-function:
∑
ζ(v) = −(N (λ)N (μ))3 · C.
v∈Vλ,μ;Ω8 \{0}

Unfortunately, unlike for the constants Ci , we so far have no further information on
the algebraic nature of the constant C.
4.4. Final remark and outlook
The trace of the octonionic division values of the functions ℘τ (i) is an octonion
whose real components are elements from the ﬁeld that is generated by the algebraic
number ﬁeld of the real components of the primitive periods ωh (canonically from a
triquadratic number ﬁeld) and by the real components of the octonionic Legendre
constants ηh . It would be a great goal to ﬁgure out under which conditions these are
algebraic and if one can do some class ﬁeld theory with these octonionic functions.
Furthermore, it would be an essential question whether similar constructions
could be carried over to the more general framework of Cayley-Dickson algebras or
even more generally to graded deformed RF Zn -algebras that we discussed in [1]. As
explained in Section 3, the theory of CM-lattices is available for this much more
general setting. However, in the proofs and in the constructions of Section 4.3 we
applied at several places the alternative property, which is true in the octonionic
case but not anymore beyond this when proceeding with the usual Cayley-Dickson
doubling. Perhaps some of these results can be carried over to the context of the
algebra of the 2n -ons considered by D. Warren in [29], indicating another possibility
for further future research in this kind of direction.
A possible ﬁeld of application consists also in understanding whether these
generalizations of elliptic functions may play a similar role in G2 -gauge theories,
analogous to the role of quaternionic regular elliptic functions playing for SU (2)instantons, cf. [13].
Another open problem, suggested by one of the referee’s, would be the following. We have constructed a family of octonionic Weierstraß ℘ functions ℘τ (i)
(i = 1, . . . , 7) from partial derivation of one octonionic Weierstraß ζ-function. Actually, in complex analysis the Weierstraß ζ-function, in turn, can be derived from
d2
one of the four Jacobi theta functions, namely, by ℘(u) = − du
2 log θ(u). So, the
Weierstraß ζ-function can be constructed from that theta function as derivative and
the Weierstraß ℘-function as its second derivative. It is an open question (even in
the quaternionic case) whether one can deﬁne a monogenic theta function for a general lattice and if one can derive all the generalized Weierstraß ℘-functions from
partial derivation of such a monogenic theta function (or perhaps of several ones).
Note that partial derivation of a Weierstraß ζ-function in the octonionic case gives
seven linearly independent diﬀerent Weierstraß ℘τ (i) functions. Furthermore, if one
introduces one primitive of the Weierstraß ζ-function, then this function will also

## PDF page 24

42

R.S. Kraußhar

induce seven linearly independent Weierstraß ζ-functions. One among them might
be the particular one described in this paper. Each of these Weierstraß ζ-functions,
in turn, induces seven Weierstraß ℘-functions by partial derivation.
Acknowledgement
The author is very thankful to the referees of this paper. Their suggestions and comments were extremely valuable and contributed a lot to the successful development
of this paper.
Funding. Open Access funding enabled and organized by Projekt DEAL.
Open Access. This article is licensed under a Creative Commons Attribution 4.0
International License, which permits use, sharing, adaptation, distribution and reproduction in any medium or format, as long as you give appropriate credit to
the original author(s) and the source, provide a link to the Creative Commons licence, and indicate if changes were made. The images or other third party material
in this article are included in the article’s Creative Commons licence, unless indicated otherwise in a credit line to the material. If material is not included in
the article’s Creative Commons licence and your intended use is not permitted by
statutory regulation or exceeds the permitted use, you will need to obtain permission directly from the copyright holder. To view a copy of this licence, visit
http://creativecommons.org/licenses/by/4.0/.
Publisher’s Note. Springer Nature remains neutral with regard to jurisdictional
claims in published maps and institutional aﬃliations.

References
[1] H. Albuquerque, R.S. Kraußhar. Multiplicative invariant lattices in Rn obtained by twisting of group algebra and some explicit characterizations. Journal of Algebra 319 No. 3
(2008), 1116–1131.
[2] J. Baez. The octonions. Bull. Amer. Math. Soc. 39 (2002), 145–205.
[3] F. Brackx, R. Delanghe, F. Sommen. Cliﬀord Analysis, Pitman Res. Notes in Math.,
76, 1982.
[4] F. Colombo, I. Sabadini, D. C. Struppa. Entire slice regular functions. Springer Briefs
in Mathematics. Springer, Cham, 2016. v+118 pp.
[5] R. Delanghe, F. Sommen, V. Souček. Cliﬀord Algebra and Spinor-valued Functions.
Mathematics and Its Applications 53, Kluwer Academic Publishers, 1992.
[6] P. Dentoni, M. Sce. Funzioni regolari nell’algebra di Cayley. Rend. Sem. Mat. Univ.
Padova 50 (1973), 251-–267.
[7] C. Flaut, V. Shpakivski. Holomorphic functions in generalized Cayley-Dickson algebras.
Adv. Appl. Cliﬀord Algebras 25 (2015), 95-–112.
[8] E. Freitag. Complex Analysis 2. Springer, Heidelberg, 2011.
[9] E. Frenod, S. V. Ludkowski. Integral operator approach over octonions to solution of
nonlinear PDE. Far East Journal of Mathematical Sciences (FJMS) (2017).

## PDF page 25

Function Theories in Cayley-Dickson algebras

43

[10] R. Fueter. Functions of a Hypercomplex Variable. Lecture Notes written and supplemented by E. Bareiss, ETH Zürich, Wintersemester 1948/49.
[11] R. Ghiloni, A. Perotti. Slice regular functions on real alternative algebras. Adv. Math.
226 (2011), 1662–1691.
[12] K. Gürlebeck, K. Habetha, W. Sprößig. Holomorphic Functions in the Plane and ndimensional space. Birkhäuser, Basel, 2008.
[13] F. Gürsey, H. Tze. On the role of division and Jordan algebras in particle physics. World
Scientiﬁc, Singapore, 1996.
[14] D. Hilbert. The Theory of Algebraic Number Fields (Zahlbericht 1896). Springer, Berlin,
1998.
[15] L. Hörmander. An Introduction to Complex Analysis in Several Variables. NorthHolland Mathematical Library, Vol. 7. North-Holland, Amsterdam, 1990.
[16] K. Imaeda. Sedenions: algebra and analysis. Appl. Math. Comp. 115 (2000), 77–88.
[17] M. Jin, G. Ren, I. Sabadini. Slice Dirac operator over octonions. Isr. J. Math. (2020).
https://doi.org/10.1007/s11856-020-2067-z
[18] J. Kauhanen, H. Orelma. Cauchy-Riemann Operators in Octonionic Analysis. Advances
in Applied Cliﬀord Algebras 28 No. 1 (2018), 14pp.
[19] J. Kauhanen, H. Orelma. On the structure of Octonion regular functions. Advances in
Applied Cliﬀord Algebra 29 No. 4 (2019), 17pp.
[20] R.S. Kraußhar. The multiplication of the Cliﬀord-analytic Eisenstein series. Journal of
Number Theory 102 No. 2 (2003), 353–382.
[21] R.S. Kraußhar. Generalized automorphic Forms in hypercomplex spaces. Birkhäuser,
Basel, 2004.
[22] S. Lang. Complex multiplication. Grundlehren der Mathematischen Wissenschaften
(Fundamental Principles of Mathematical Sciences) 255 Springer, New York, 1983.
[23] H.R. Malonek. Rudolf Fueter and his motivation for hypercomplex function theory. Advances in Applied Cliﬀord Algebras 11 (2001), 219–229.
[24] W. Nef. Die unwesentlichen Singulariäten der regulären Funktionen einer Quaternionenvariablen. Comm. Math. Helv. 16 (1943-44), 284–304.
[25] C. Nolder. Much to do about octonions. AIP Proceedings, ICNAAM 2018, 2116, 160007
(2019); https://doi.org/10.1063/1.5114151
[26] K. Nono. On the octonionic linearization of Laplacian and octonionic function theory.
Bull. Fukuoka Univ. Ed. Part III 37 (1988), 1–15.
[27] J. Ryan. Cliﬀord Analysis with generalized elliptic and quasi-elliptic functions. Applicable Analysis, 13 (1982), 151–171.
[28] B. Schoeneberg. Elliptic Modular Functions. Die Grundlagen der mathematischen Wissenschaften 201, Springer, Berlin-Heidelberg-New York, 1974.
[29] W. D. Smith. Quaternions, octonions, 16-ons and 2n -ons; New kinds of numbers. Pensylvania State University (2004), 1–68. DOI: 10.1.1.672.2288
[30] Xing-min Li and Li-Zhong Peng. On Stein-Weiss conjugate harmonic function and octonion analytic function. Approx. Theory and its Appl. 16 (2000), 28–36.
[31] Xing-min Li, K. Zhao, Li-Zhong Peng. The Laurent series on the octonions. Advances
in Applied Cliﬀord Algebras 11 (S2) (2001), 205–217.

## PDF page 26

44

R.S. Kraußhar

[32] Xing-min Li and Li-Zhong Peng. The Cauchy integral formulas on the octonions. Bull.
Belg. Math. Soc. 9 (2002), 47–62.
[33] Xing-min Li , Zhao Kai, Li-Zhong Peng. Characterization of octonionic analytic functions. Complex Variables 50 No. 13 (2005), 1031–1040.
Rolf Sören Kraußhar
Fachbereich Fachwissenschaft Mathematik
Erziehungswissenschaftliche Fakultät
Universität Erfurt
Nordhäuser Str. 63
D 99089 Erfurt
Germany
e-mail: soeren.krausshar@uni-erfurt.de
Submitted: December 10, 2019.
Revised: October 14, 2020.
Accepted: October 28, 2020.
