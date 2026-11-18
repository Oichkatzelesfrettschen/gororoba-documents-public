Source: https://doi.org/10.46298/jonas.17802
PDF sha256: 3af912b1f23e33653ae954ec73c050e749424b9995a0d876342c47b1a911f1a7
License: CC-BY-4.0
Language: eng
Fidelity: machine-gated

# Transcription of chapman_levin_2026_central_products_cayley_dickson_loops.pdf

Transcription of `chapman_levin_2026_central_products_cayley_dickson_loops.pdf` in this directory, 7 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-7 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Journal of Non-Associative Structures 1 (2026), no. 1, Paper no. 7
DOI: https://doi.org/10.46298/jonas.17802
©2026 Adam Chapman and Ilan Levin
This is an open access article licensed under the CC BY 4.0 licence.

Central products of Cayley-Dickson loops
Adam Chapman and Ilan Levin
Abstract. This paper studies the triviality of commutators in central products of
Cayley-Dickson loops. Two immediate outcomes of this study are (1) the construction of a sequence of non-commutative di-associative loops in which the probability
that a random commutator is trivial approaches 1, and (2) an easy proof that if
two central products of n-fold Cayley-Dickson loops are isomorphic for n ⩾ 3, then
the loops in the ﬁrst product are term-wise isomorphic to the loops in the second
product.

Contents
1 Cayley-Dickson Algebras

2

2 Cayley-Dickson Loops

2

3 Commutants and Commutators

3

4 Associativity Degree

6

MSC 2020: 20N05 (primary); 17D99 (secondary)
Keywords: Di-Associative Loops; Cayley-Dickson Algebras; Commutativity Degree; Central Product
Contact information:
A. Chapman:
Aﬃliation: Academic College of Tel-Aviv-Yaﬀo, Israel.
Email: adam1chapman@yahoo.com
I. Levin:
Aﬃliation: Bar-Ilan University, Israel.
Email: ilan7362@gmail.com
Editorial information:
Received: March 24, 2026
Accepted: June 23, 2026
Communicated by: Leandro Vendramin
Acknowledgments: We thank the anonymous referees whose detailed reports have improved the quality
of this paper considerably.

1

## PDF page 2

Adam Chapman and Ilan Levin

1

Cayley-Dickson Algebras

Given a ﬁeld F of char(F ) ̸= 2 and γ ∈ F × , a Cayley-Dickson doubling B = A{γ}
of an algebra A over F with involution σ is deﬁned to be A ⊕ Aℓ where multiplication is
given by (q + rℓ)(s + tℓ) = qs + γσ(t)r + (tq + rσ(s))ℓ. The involution extends from A
to B by σ(q + rℓ) = σ(q) − rℓ. We deﬁne the n-fold Cayley-Dickson algebra (γ1 , . . . , γn )F
recursively to be B = A{γn } where A = (γ1 , . . . , γn−1)F , and the initial 0-fold algebra is
F with the trivial involution (see [14]). It is known (see [14] and [9, Section 33.C]) that:
• when n = 1, (α)F are quadratic étale algebras, i.e., either F × F or quadratic ﬁeld
extensions K of F , with the involution being the nontrivial automorphism of the
Galois group of K/F ;
• when n = 2, (α, β)F are quaternion algebras over F , with the involution being the
symplectic involution;
• when n = 3, (α, β, γ)F are octonion algebras;
• when n = 4, (α, β, γ, δ)F are sedenion algebras, etc.
These algebras, especially for n ⩽ 3, are important for various reasons. Tensor products of
these algebras, especially for n = 2 (see [11]), but also for higher n (for instance in [1]) are
also objects of interest in the active research of mathematics. In [12], isomorphisms between tensor products of octonion algebras were studied. The norm form of (γ1 , . . . , γn )F
given by x ↦→ xσ(x) is the n-fold Pﬁster form ⟨⟨γ1 , . . . , γn ⟩⟩ (see [13]).

2

Cayley-Dickson Loops

Recall that a set L with a binary operation is called a quasi-group if the maps
ℓa : x ↦→ ax, ra : x ↦→ xa, are bijections, for all a ∈ L. A quasi-group with an identity
element 1 is called a loop. A loop can be thought of as a non-associative group. A subloop
is a subset which forms a loop under the restricted binary operation. In particular,
Z(L) = {z ∈ L : xz = zx, (xy)z = x(yz), (xz)y = x(zy), (zx)y = z(xy)}
is a subloop. A subloop N ⩽ L is called normal if it is a kernel of some homomorphism
of loops f : L → M. Equivalently, N is normal if and only if ϕ(N) = N for any inner
automorphism ϕ ∈ Inn(L). Inner automorphisms are the subgroup of Aut(L) generated
−1
−1
by Inn(L) := ⟨ℓ−1
x rx , rxy ry rx , ℓyx ℓx ℓy : x, y ∈ L⟩. It is easy to see that ϕ(z) = z for
any z ∈ Z(L), hence any subgroup of Z(L) is a normal subloop of L. See [2] for further
background on loops in general.
For the construction of the loops of concern in this paper, ﬁrst note that the recursive
construction of (γ1 , . . . , γn )F deﬁnes a set ℓ1 , . . . , ℓn of generators of this algebra over F .
Fixing a subgroup Z of F × including γ1 , . . . , γn , we deﬁne the n-fold Cayley-Dickson loop
2

## PDF page 3

Central products of Cayley-Dickson loops

(γ1 , . . . , γn )Z over Z to be the multiplicative subloop of (γ1 , . . . , γn )F generated by Z and
ℓ1 , . . . , ℓn (see [8]). Note that it always contains −1. For example, if Z = {±1} and F
is any ﬁeld of characteristic 0, then (−1, −1)Z is the famous quaternion group Q8 , and
(−1, −1, −1)Z is the octonion loop O16 (see [7]). We deﬁne the central product L1 ∗ L2 of
two loops L1 and L2 with center Z in the same manner as in groups, i.e., L1 × L2 modulo
{(x, x−1 )|x ∈ Z}. The notation is taken from [5], see also [6, Chapter 2, Section 5]. As
with groups, the center Z can be identiﬁed with {(z, 1) : z ∈ Z} in L1 ∗L2 , and this is then
the center of L1 ∗ L2 . As with groups (see for example in [5], this notion extends without
any problem to central products of any ﬁnite number of loops sharing the same center Z.
Note that the central product L1 ∗ · · · ∗ Lm of Cayley-Dickson loops Li = (γi,1 , . . . , γi,n )Z ,
i ∈ {1, . . . , m}, is also the multiplicative subloop of the corresponding tensor product
A1 ⊗F · · · ⊗F Am over F of the Cayley-Dickson algebras Ai = (γi,1, . . . , γi,n )F generated by
the generators of these algebras and Z. All the loops mentioned above are di-associative
(that is, every two elements generate an associative subgroup, see [4, Theorem 5.4]), so
they are “close” to being groups in some sense.
The goal of this paper is to examine how diﬀerently central products of loops behave
from groups. We focus on Cayley-Dickson loops, but this calls for a deeper study of larger
families of such loops. For the group of quaternions Q8 = (−1, −1)Z with Z = {±1},
we have Q8 ∗ Q8 = (1, −1)Z ∗ (1, −1)Z , even though Q8 ∼
̸= (1, −1)Z . We show that this
does not extend to higher-fold Cayley-Dickson loops. Another important diﬀerence is the
commutativity degree: For non-abelian groups, it cannot exceed 58 . We show here that
for central products of Cayley-Dickson loops, the commutativity degree can approach 1.
More precisely, we prove the following statements:
1. The probability that a random commutator in L1 ∗ L2 is trivial approaches 1 as n
approaches ∞ when L1 and L2 are n-fold Cayley-Dickson loops over Z of |Z| < ∞.
2. If D1 , . . . , Dm , E1 , . . . , Em are n-fold Cayley-Dickson loops over Z such that n ⩾ 3
and D1 ∗ · · · ∗ Dm ∼
= E1 ∗ · · · ∗ Em , then there exists σ ∈ Sm such that Dk ∼
= Eσ(k)
for all k ∈ {1, . . . , m}.
See [10] for a similar discussion on the associativity degree of Moufang loops. Item (2) is
related to questions about automorphisms of Cayley-Dickson loops, as were studied in [7]
and [3], and serves as a loop analogue (at least for n = 3) of [12]. We also study the
associativity degree of ﬁnite n-fold Cayley-Dickson Loops (−1, . . . , −1)Z .

3

Commutants and Commutators

Given a loop L and x ∈ L, deﬁne the commutant of x as CL (x) := {y ∈ L|xy = yx}.
The commutator [x, y] of x, y ∈ L is the unique element such that (xy) = [x, y](yx), whose
existence and uniqueness follow from the deﬁnition of a loop. Note that in our case, where
all the loops are central products of Cayley-Dickson loops, all the commutators are in
{±1}.
3

## PDF page 4

Adam Chapman and Ilan Levin

Let D1 , . . . , Dm be n-fold Cayley-Dickson loops over Z. Note that each Di possesses
a surjective homomorphism from Di to (Z/2Z)n sending the k-th generator of Di to ek for
all k = 1, . . . , n, and the elements of Z to ⃗0. The kernel is thus Z. Hence, Di /Z ∼
= (Z/2Z)n .
For A = D1 ∗ · · · ∗ Dm , we obtain in a similar way an isomorphism A/Z ∼
= (Z/2Z)mn . The
ﬁniteness of A/Z as a set enables us to carry out the following calculations.
Note that for any positive integer d, G = (Z/2Z)d is both an additive group and an
F2 -vector space, and every subgroup of G is thus an F2 -vector space as well which has
a well-deﬁned dimension. We apply this notion in the proofs below.
Proposition 1. Let D1 , . . . , Dm be n-fold Cayley-Dickson loops over Z and let x ∈ Dk \ Z
for some k ∈ {1, . . . , m}. Set A = D1 ∗ · · · ∗ Dm . Then, CA (x)/Z is of cardinality
1
1
2(m−1)n+1 = 2n−1
2mn = 2n−1
· |A/Z|.
Proof. This readily follows from the fact that CDk (x)/Z is of dimension 1, Dk /Z is of
dimension n and the deﬁnition of the central product.
We say that an element y ∈ A is of rank k if:
1. y = xi1 · · · xik ;
2. xij ∈ Dij \ Z for all j = 1, . . . , k and;
3. i1 < i2 < · · · < ik .
We denote it by rankA (y) = k. If y ∈ Z, then rankA (y) := 0. Note that this is welldeﬁned, as we can omit brackets and change the order of the xi ’s as we wish, because all
their associators and commutators vanish.
Theorem 2. Let D1 , . . . , Dm be n-fold Cayley-Dickson loops over Z, let y ∈ A, and let
1
= 12 + 21 (2p − 1)k , where p = 2n−1
.
rankA (y) = k. Then |CA2(y)/Z|
mn
1
|CA (y)/Z| for any y ∈ A of rankA (y) = k
Proof. Set bk = 2mn
Let us prove by induction on k that bk = 12 + 21 (2p − 1)k . The base case is covered
by Proposition 1. Assume it is true for k − 1. Write y = xi1 · · · xik . By the deﬁnition of
the central product, for any ã ∈ A, the commutator [y, ã] is the product of the diﬀerent
commutators [xi1 , ã], . . . , [xik−1 , ã], [xik , ã]. As a result, we obtain the identity

[y, ã] = [xi1 · · · xik−1 , ã] · [xik , ã].
Therefore, ã ∈ CA (y) if and only if
[xi1 · · · xik−1 , ã] = [xik , ã] = 1 or [xi1 · · · xik−1 , ã] = [xik , ã] = −1.
The probability of the former is pbk−1 and the probability of the latter is (1 − p)(1 − bk−1 ).
So bk = pbk−1 + (1 − p)(1 − bk−1 ) = (1 − p) + (2p − 1)bk−1 , and by plugging the induction
assumption bk−1 = 12 + 12 (2p − 1)k−1 we are done.
4

## PDF page 5

Central products of Cayley-Dickson loops

When |Z| < ∞, one can see that
( )
m
(2n − 1)k .
| {x ∈ A : rankA (x) = k} | = |Z| ·
k

(♣)

Corollary 3. Let (x, y) be an element chosen from L × L with uniform distribution, where
L = D1 ∗D2 is the central product of two n-fold Cayley-Dickson loops over Z with |Z| < ∞.
Then Pc (L) = P(xy = yx) = 1 − 6 · 21n + 22 · 41n − 24 · 81n + 8 · 161n .
Proof. Note that |L| = |Z| · 22n . By the law of total probability with respect to rankA (x),
we have
2
∑
P(xy = yx) =
P(xy = yx| rankA (x) = i) · P(rankA (x) = i).
i=0

Moreover, using (♣) for m = 2, the distribution of rankA (x) is given by
( )
|Z| 2
(2n − 1)i .
P(rankA (x) = i) =
|A| i
Substituting these values yields
P(xy = yx) =

1 1
|Z|
(1 + p · 2 · (2n − 1) + ( + (2p − 1)2 ) · (2n − 1)2 ) =
|A|
2 2
1
1
1
1
= 1 − 6 · n + 22 · n − 24 · n + 8 · n
2
4
8
16

Corollary 4. There exists a sequence of di-associative loops {Kn }∞
n=1 such that the commutativity degree approaches 1, i.e., limn→∞ Pc (Kn ) = 1.
Proof. Take Kn to be as in the previous corollary and n → ∞.
This demonstrates how versatile di-associative loops are, even rather natural ones,
compared to groups in terms of their commutativity degree.
Remark 5. If we consider D1 , . . . , Dm to be n-fold Cayley-Dickson loops over Z and
Am = D1 ∗ · · · ∗ Dm , ﬁx n ⩾ 2, and then we get limm→∞ Pc (Am ) = 21 . This was known for
n = 2, in which case these loops are quaternionic groups.
We now turn our concern to understanding automorphisms of these objects, when
n ⩾ 3.
Theorem 6. If D1 , . . . , Dm , E1 , . . . , Em are n-fold Cayley-Dickson loops over Z with n ⩾ 3
and D1 ∗ · · · ∗ Dm ∼
= E1 ∗ · · · ∗ Em , then there exists σ ∈ Sm for which Dj ∼
= Eσ(j) .
Proof. Let ϕ : D1 ∗ · · ·∗ Dm → E1 ∗ · · ·∗ Em be an isomorphism. Given bk as in Theorem 2,
1
|bk − 21 | = 12 |2p − 1|k is strictly decreasing, since p = 2n−1
and n ⩾ 3. Hence, {bk }∞
k=0
has no repetitions. Thus, ϕ preserves the rank. Let x ∈ Dj , rankD (x) = 1, for some
5

## PDF page 6

Adam Chapman and Ilan Levin

j ∈ {1, . . . , m}. Then ϕ(x) ∈ Eℓ , for some ℓ, because its rank is 1. The only elements
anti-commuting with x are Dj \ Z⟨x⟩, and the only elements anti-commuting with ϕ(x)
are Eℓ \ Z⟨ϕ(x)⟩, so ϕ(Dj \ Z⟨x⟩) = Eℓ \ Z⟨ϕ(x)⟩, and altogether we get that ϕ(Dj ) = Eℓ .
So there exists σ ∈ Sm for which Dj ∼
= Eσ(j) .

4

Associativity Degree

In [10] it was shown that the associativity degree of a ﬁnite non-associative Moufang
loop is bounded from above by 43
. Here we study the associativity degree of the n-fold
64
Cayley Dickson loops Ln = (−1, . . . , −1)Z , for |Z| < ∞. It is important to note that the
order of an n-fold Cayley-Dickson loop is 2n |Z|. In this context, we deﬁne the associativity
degree of Ln , denoted by PA (Ln ), to be the probability that for a random triple of elements
(x, y, z) chosen from Ln × Ln × Ln with uniform distribution, ⟨x, y, z⟩ is a group. This
coincides with the deﬁnition in [10] for Moufang loops, where this is equivalent to saying
that (xy)z = x(yz) because of Moufang’s theorem.
n

n

+8
.
Theorem 7. The associativity degree of Ln is PA (Ln ) = 7·4 −14·2
8n

Proof. Let (a, b, c) be an arbitrary element in Ln × Ln × Ln . It amounts to counting the
number of triples generating a subgroup. If a ∈ Z, then b and c can be any elements. We
have 22n ·|Z|3 such triples. If a ̸∈ Z (and there are 2n ·|Z|−|Z| such elements), we consider
two cases: b ∈ ⟨a, Z⟩ and b ̸∈ ⟨a, Z⟩. Note that |⟨a, Z⟩| = 2|Z|. If b ∈ ⟨a, Z⟩, then c can
be any element, and there are |Z|(2n − 1) · 2|Z| · 2n |Z| such triples. If b ̸∈ ⟨a, Z⟩, then c
has to belong to ⟨a, b, Z⟩ by [8, Lemma 7], and there are |Z|(2n − 1) · |Z|(2n − 2) · 4|Z|
such triples. After summing everything and dividing by |Ln |3 , we ﬁnally get that
PA (Ln ) =
2

7 · 4n − 14 · 2n + 8
.
8n
2

64
+8
For example, when n = 2, 7·4 −14·2
= 64
= 1, as expected, and when n = 3,
82
7·43 −14·23 +8
344
43
= 512 = 64 , as was already found in [10].
83

References
[1] G. Blachar, L. H. Rowen, and U. Vishne. Identities of the algebra O ⊗ O. In Algebra and Coding
Theory, volume 785 of Contemp. Math., pages 35–45. Amer. Math. Soc., [Providence], RI, [2023]
©2023.
[2] R. H. Bruck. A survey of binary systems. Reihe: Gruppentheorie. Springer-Verlag, Berlin-GöttingenHeidelberg, 1958. Ergebnisse der Mathematik und ihrer Grenzgebiete, (N.F.), Heft 20.
[3] A. Chapman, I. Levin, U. Vishne, and M. Zaninelli. Loops with involution and the Cayley-Dickson
doubling process. arXiv preprint arXiv:2501.00123, 2024.
[4] C. Culbert. Cayley-Dickson algebras and loops. Journal of Generalized Lie Theory and Applications,
1(1):1–17, 2007.

6

## PDF page 7

Central products of Cayley-Dickson loops

[5] D. Gorenstein. The classiﬁcation of ﬁnite simple groups. I. Simple groups and local analysis. American Mathematical Society. Bulletin. New Series, 1(1):43–199, 1979.
[6] D. Gorenstein. Finite groups. Chelsea Publishing Co., New York, second edition, 1980.
[7] J. Kirshtein. Automorphism groups of Cayley-Dickson loops. Journal of Generalized Lie Theory
and Applications, 6:Art. ID G110901, 10, 2012.
[8] J. Kirshtein. Multiplication groups and inner mapping groups of Cayley-Dickson loops. Journal of
Algebra and its Applications, 13(1):1350078, 26, 2014.
[9] M.-A. Knus, A. Merkurjev, M. Rost, and J.-P. Tignol. The book of involutions, volume 44 of American Mathematical Society Colloquium Publications. American Mathematical Society, Providence,
RI, 1998. With a preface in French by J. Tits.
[10] I. Levin. How associative can a non-associative Moufang loop be? Communications in Algebra,
54(4):1723–1727, 2026.
[11] A. S. Merkurjev. On the norm residue symbol of degree 2. Doklady Akademii Nauk SSSR, 261(3):542–
547, 1981.
[12] P. J. Morandi, J. M. Pérez-Izquierdo, and S. Pumplün. On the tensor product of composition
algebras. Journal of Algebra, 243(1):41–68, 2001.
[13] S. M. Musgrave. Representations of alternative Cliﬀord algebras of quadratic forms. Glasgow
Mathematical Journal, 57(3):579–590, 2015.
[14] R. D. Schafer. On the algebras formed by the Cayley-Dickson process. American Journal of Mathematics, 76:435–446, 1954.

7
