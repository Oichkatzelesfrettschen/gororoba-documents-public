Source: https://doi.org/10.46298/cm.12613
PDF sha256: 090f88a7cfca84c5afd0d07d70182d264ca7b30ba8999733302f2dd293a8e4bd
License: https://creativecommons.org/licenses/by-sa/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of chapman_vishkautsan_2025_roots_right_factors_polynomials_left_eigenvalues_matrices_cayley_dickson_algebras.pdf

Transcription of `chapman_vishkautsan_2025_roots_right_factors_polynomials_left_eigenvalues_matrices_cayley_dickson_algebras.pdf` in this directory, 11 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-11 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Communications in Mathematics 33 (2025), no. 3, Paper no. 1.
DOI: https://doi.org/10.46298/cm.12613
©2025 Adam Chapman and Solomon Vishkautsan
This is an open access article licensed under the CC BY-SA 4.0

1

Roots and right factors of polynomials and left eigenvalues
of matrices over Cayley–Dickson algebras
Adam Chapman and Solomon Vishkautsan
Abstract. Over a composition algebra A, a polynomial f (x) ∈ A[x] has a root α if
and only f (x) = g(x) · (x − α) for some g(x) ∈ A[x]. We examine whether this is true
for general Cayley–Dickson algebras. The conclusion is that it is when f (x) is linear
or monic quadratic, but it is false in general. Similar questions about the connections
between f and its companion Cf (x) = f (x) · f (x) are studied. Finally, we compute
the left eigenvalues of 2 × 2 octonion matrices.

1

Introduction

Given an algebra A (in this article an algebra is unital but is not necessarily commutative or associative) with involution τ over a ﬁeld F , and a choice of γ ∈ F × , the
Cayley–Dickson double B = A{γ} of A is deﬁned to be A ⊕ Aℓ with the product
(q + rℓ)(s + tℓ) = qs + γtr + (tq + rs)ℓ
for any q, r, s, t ∈ A, and where x = τ (x) for any x ∈ A. The involution τ extends to
B by deﬁning q + rℓ = q − rℓ. A Cayley–Dickson algebra is obtained by repeating this
process several times, starting with a quadratic separable extension K of F , with τ being
the unique non-trivial automorphism of order 2 of K acting trivially on F . We denote such
an algebra A by K{γ2 , . . . , γm } where γ2 , . . . , γm are the chosen elements of F × , in this
order. When char(F ) ̸= 2, K is actually F {γ1} for the right choice of γ1 ∈ F × , and thus
A = F {γ1 , γ2 , . . . , γm }. Such algebras (regardless of the characteristic of the base ﬁeld) are
MSC 2020: primary 17A75; secondary 17A45, 17A35, 17D05, 37P35, 37C25
Keywords: Cayley–Dickson Algebras; Polynomials; Roots; Decomposition
Contact information:
A. Chapman:
Aﬃliation: School of Computer Science, Academic College of Tel-Aviv-Yaﬀo, Israel.
Email: adam1chapman@yahoo.com
S. Vishkautsan:
Aﬃliation: Department of Computer Science, Tel-Hai Academic College, Israel.
Email: wishcow@gmail.com

## PDF page 2

2

Adam Chapman and Solomon Vishkautsan

endowed with a linear trace form Tr(q) = q + q and a quadratic norm form Norm(q) = q · q
satisfying q 2 − Tr(q)q + Norm(q) = 0 for any q ∈ A.
When dim A = 4, A is called a quaternion F -algebra, and when dim A = 8 an octonion
algebra, and when dim A = 16 a sedenion algebra. Special attention is given in the
literature to the Cayley–Dickson algebras constructed over the real numbers by repeatedly
choosing γ = −1, i.e., R{−1, −1, . . . , −1}. The ﬁrst four of those are C, H, O and S (resp.
the complex ﬁeld, Hamilton’s quaternions, the real octonion division algebra and the real
sedenion algebra). These algebras can be described as real Cayley–Dickson algebras with
anisotropic norm form, or as locally-complex Cayley–Dickson algebras (a real unital algebra
is called locally-complex if any nonscalar element generates a subalgebra isomorphic to C;
c.f. [1]).
The norm form of a Cayley–Dickson algebra A is multiplicative as long as dim A ≤
8. When dim A ≥ 16, it stops being multiplicative. For example, when A = S with
its standard basis e0 , e1 , . . . , e15 (for the deﬁnition of the standard basis in terms of the
generators of S and its multiplication table, see for example [5, Section 2.2] and [2, Section
2]), the elements α = e1 + e10 and β = e7 + e12 are of norm 2, so having a multiplicative
norm form would mean Norm(αβ) = 4, but in fact αβ = 0.
In this article we address several questions that came up in the writing of the articles
[5, 7]. In Section 2 we discuss the decomposition of the form f (x) = g(x) · (x − λ) for roots
λ of polynomials with coeﬃcients in a Cayley–Dickson algebra. We show that such a decomposition exists for linear and monic quadratic polynomials but does not exist in general
for Cayley–Dickson algebras of dimension ≥ 16. We also show that in the latter algebras
there exist polynomials which have no roots. Finally, we give some counterexamples to
questions regarding roots and critical points of Cayley–Dickson polynomials.
In Section 3 we prove that every octonion matrix has a left eigenvalue, and provide a
method for their computation. This provides a direct generalization of Huang and So’s
results for quaternion matrices in [12].

2

Polynomials over Cayley–Dickson Algebras

Given a Cayley–Dickson algebra A over F , we deﬁne the polynomial algebra A[x] to be
A ⊗F F [x]; i.e., the indeterminate x behaves like a central element, and in particular, every
commutator or associator involving x is trivial. Every polynomial f (x) ∈ A[x] can thus
be written as f (x) = cn xn + · · · + c1 x + c0 for some c0 , c1 , . . . , cn ∈ A. The substitution of
λ ∈ A in f (x) is deﬁned by f (λ) = cn (λn ) + · · · + c1 λ + c0 . This expression is well-deﬁned
as Cayley–Dickson algebras are always power-associative, see [15]. We say that λ ∈ A is a
root of f (x) ∈ A[x] if f (λ) = 0.
For f (x) ∈ A[x], the companion polynomial of f (x) is deﬁned by
Cf (x) = Norm(f (x)) = f (x) · f (x) ∈ F [x],
where f (x) = cn xn + · · · + c1 x + c0 . It is known that when dim A ≤ 8, every root of f (x)
is a root of Cf (x), and every root of Cf (x) has an element quadratically equivalent to it,
i.e., an element with the same trace and norm, which is a root of f (x); see [3].

## PDF page 3

Roots and right factors of polynomials and left eigenvalues of matrices over Cayley–Dickson algebras 3

2.1

Roots and linear factors of Cayley–Dickson Polynomials

It is known that when A is a Cayley–Dickson algebra of dim A ≤ 8, then λ ∈ A is a
root of f (x) ∈ A[x] if and only if x − λ is a right factor of f (x), i.e., f (x) = g(x) · (x − λ)
for some g(x) ∈ A[x], see [3].
Question 2.1. Given a polynomial f (x) over a Cayley–Dickson algebra A and λ ∈ A, is it
true that λ is a root of f (x) if and only if there exists g(x) ∈ A[x] such that
f (x) = g(x) · (x − λ)?
We begin by settling Question 2.1 for linear and monic quadratic polynomials:
Proposition 2.2. When f (x) ∈ A[x] is either linear or monic quadratic, an element λ ∈ A
is a root of f (x) if and only if f (x) = g(x) · (x − λ) for some g(x) ∈ A[x].
Proof. When f (x) is linear, f (x) = ax + b for some a, b ∈ A. If λ is a root, then
f (λ) = aλ + b = 0,
and so b = −aλ, which means f (x) = ax − aλ = a(x − λ). In the opposite direction, when
(x − λ) is a right factor of f (x), there exists a ∈ A such that f (x) = a(x − λ) = ax − aλ,
and then clearly f (λ) = 0.
When f (x) is monic quadratic, f (x) = x2 + ax + b. If λ is a root, then f (λ) =
λ2 + aλ + b = 0, and so b = −λ2 − aλ, which means
f (x) = x2 + ax − λ2 − aλ = (x + λ)(x − λ) + a(x − λ) = (x + λ + a)(x − λ).
In the opposite direction, if x − λ is a right factor, then f (x) = (x + c)(x − λ) for some
c ∈ A, and so f (x) = x2 + cx − λx − cλ, which means f (λ) = λ2 + cλ − λ2 − cλ = 0.
We now provide negative answers to Question 2.1 in general, both for the implication
that having a root λ means having a right factor x − λ, and its converse statement.
Example 2.3. Consider A = S with its standard basis e0 , . . . , e15 , and denote α = e1 + e10
and β = e7 + e12 . The elements α and β are zero divisors, and we have αβ = βα = 0.
We remark that anisotropic Cayley–Dickson algebras over ﬁelds of characteristic diﬀerent
from 2 are reversible, i.e. αβ = 0 implies βα = 0; see [8, Theorem 2.3].
Now let f (x) = 21 βx2 + β. Since
1
1
f (α) = β · (α2 ) + β = β · (−2) + β = 0,
2
2
α is a root of f (x). However, if x − α were a right factor of f (x), there would exist c ∈ A
for which
1
1
f (x) = ( βx + c)(x − α) = βx2 + cx − cα,
2
2
implying both c = 0 and cα = −β, a contradiction.

## PDF page 4

4

Adam Chapman and Solomon Vishkautsan

Example 2.4. Using the notations from the previous example, consider f (x) = βx2 + βx.
This polynomial decomposes as f (x) = (βx + β)(x − α), but f (α) = −2β, so α is not a
root of f (x).
The question of real Cayley–Dickson algebras being “algebraically closed” is classic.
In this context, “algebraically closed” means that every polynomial of degree at least 1
has a root in the algebra. This was proved in the wider setting of general real quaternion
polynomials for polynomials with one leading monomial by Eilenberg and Niven (See [10]).
This result was subsequently generalized to the real octonions by Jou [13], and to more
complicated polynomials over any ﬁnite-dimensional real composition division algebra in
[16]. For the special case of left or one-sided polynomials over O as discussed in this article,
we propose the following short proof.
Proposition 2.5. Every polynomial f (x) ∈ O[x] of degree at least 1 has a root in O.
Proof. The companion polynomial of f (x) is deﬁned by Cf (x) = Norm(f (x)) = f (x)·f (x).
It is a polynomial with real coeﬃcients of degree at least 2, and thus it admits a complex
root α. Since the complex numbers embed into O, we can assume that α ∈ O. By [4,
Theorem 3.4], the root α of Cf (x) is quadratically equivalent to some root of f (x) in O
(i.e., there exists a root of f (x) with the same trace and norm as α).
Corollary 2.6. Every polynomial f (x) ∈ O[x] decomposes as a product of linear factors of
the form
f (x) = ((...(c(x − λn )) . . . (x − λ3 ))(x − λ2 ))(x − λ1 ).
Proof. This follows from the former proposition and the correspondence between linear
right factors and roots of octonion polynomials described at the beginning of the section
and proven in [3].
We remark that the λi for 2 ≤ i ≤ n in Corollary 2.6 are not necessarily roots of
f (x). A natural question to ask is whether this type of decomposition extends to higher
dimensional Cayley–Dickson algebras.
Question 2.7. Are all real Cayley–Dickson algebras with anisotropic norm form algebraically closed?
The answer to Question 2.7 is evidently negative, as real anisotropic Cayley–Dickson
algebras of dimension ≥ 16 contain zero divisors. Each such zero divisor α deﬁnes a linear
map q ↦→ αq on A which is not surjective, implying that there exists some β ∈ A such that
there is no solution in A to the equation αx = β. This proves that the linear polynomial
f (x) = αx − β has no roots in A. We now provide a concrete counterexample in S:
Example 2.8. Let α and β be the elements of A = S from Example 2.3, and let f (x) =
αx − β. We show that this linear polynomial has no roots in S.
Consider the real-valued symmetric bilinear form ⟨a, b⟩ associated with the quadratic
form Norm(a) on an arbitrary Cayley–Dickson algebra A over R, with ⟨a, a⟩ = Norm(a)

## PDF page 5

Roots and right factors of polynomials and left eigenvalues of matrices over Cayley–Dickson algebras 5

for all a ∈ A. The bilinear form satisﬁes the identities ⟨a, bc⟩ = ⟨ac̄, b⟩ = ⟨b̄a, c⟩ for all
a, b, c ∈ A (see [15, Lemma 6]). Consequently, if αx = β, it follows that
2 = ⟨β, β⟩ = ⟨αx, β⟩ = −⟨x, αβ⟩ = −⟨x, 0⟩ = 0,
a contradiction.
2.2

The Companion Polynomial

Let A be a Cayley–Dickson algebra over F , and f (x) ∈ A[x]. Recall that when dim A ≤
8, every root of f (x) is a root of Cf (x), and every root of Cf (x) has an element quadratically
equivalent to it. In [5] it was pointed out that f (x) = αx ∈ S[x] has β as a root even
though β is not a root of Cf (x) = 2x2 (where α and β are as in Example 2.3). The second
part of the property stated in the ﬁrst line of this paragraph has not been dealt with
though, which brings up the following question.
Question 2.9. Is every root of Cf (x) quadratically equivalent to some root of f (x), even
when dim A ≥ 16?
The answer is in general no:
Example 2.10. In example 2.8 we showed that the polynomial f (x) = αx − β ∈ S[x] has
no roots, but its companion Cf (x) = 2x2 + 2 certainly does (all the elements of trace 0
and norm 1).
2.3

Isolated and Spherical Roots

Another property of f (x) ∈ A[x] when dim A ≤ 8 and its norm form is anisotropic
is that every root of f (x) is either isolated (i.e., it is the only element in the quadratic
equivalence class that is a root of f (x)), or spherical (i.e., every element in the quadratic
equivalence class of the root is also a root of f (x)).
Question 2.11. When the norm form of A is anisotropic, is every root of a polynomial
f (x) in A[x] either spherical or isolated?
This is not true when dim A ≥ 16:
Example 2.12. The polynomial f (x) = αx ∈ S[x] has both β and −β as quadratically
equivalent roots, but α is not a root, even though α is quadratically equivalent to β.
2.4

Critical Points

The Gauss–Lucas theorem states that the critical points of f (x) ∈ C[x] (i.e. the roots
of the derivative f ′ (x)) are contained in the convex hull of the roots of f (x). In [11] it
was shown that this does not extend to f (x) ∈ H[x] (here the derivative f ′ (x) is deﬁned
formally). In [5, Theorem 4.2] it was proven that the spherical critical points of f (x)
(again, f ′ (x) is deﬁned formally) are contained in the convex hull of the roots of Cf (x) for
any f (x) ∈ A[x] where A is any real anisotropic Cayley–Dickson algebra.

## PDF page 6

6

Adam Chapman and Solomon Vishkautsan

Question 2.13. Are the spherical roots of f ′ (x) contained in the convex hull of the roots
of f (x)?
We hereby show that this does not hold:
Example 2.14. The polynomial f (x) = 31 x3 + x + i ∈ H[x] has three isolated roots,
none of which are spherical. Indeed, the polynomial has three complex roots, but no real
quadratic factors, i.e., no two roots are complex-conjugate. If f (x) had a spherical root λ,
it would have had exactly two distinct roots quadratically equivalent to λ in C (see e.g. [18,
Theorem 2.2]; or [5, Corollary 3.8] for general locally-complex Cayley–Dickson algebras),
and these must be complex-conjugate, leading to a contradiction. Note however, that
f ′ (x) = x2 + 1 does have spherical roots, most of which are not contained in the convex
hull of the roots of f (x), which are all complex.

3

Roots and Left Eigenvalues

When A is a non-commutative algebra, the notion of eigenvalues of a matrix B with
coeﬃcients in A divides into two categories: left eigenvalues λ which satisfy B⃗v = λ⃗v for
some nonzero vector ⃗v , and right eigenvalues which satisfy B⃗v = ⃗v λ (in either case we say
that ⃗v is the eigenvector associated to the eigenvalue λ). We focus here on left eigenvalues.
The motivating observation is that λ is a left eigenvalue of B ∈ Mn (A) if and only if there
exists a nonzero column vector ⃗v in An (the direct product of n copies of A) for which
(B − λI)⃗v = 0, which means B − λI deﬁnes (by multiplication from the left) a singular
linear endomorphism of An as an F -vector space.
In the associative case, right eigenvalues are well-understood. In [14] it was shown that
over H they can be easily found through the embedding of Mn (H) into M2n (C), and this
method was generalized in [6] to any associative central division algebra. When A is a
quaternion algebra, it was shown in [12] that the left eigenvalues of 2 × 2 matrices over
A can be found by solving a quadratic equation. The goal of this section is to do the
analogous thing for octonion division algebras. Note that the special case of 2 × 2 and
3 × 3 Hermitian matrices over O was studied in [9].
Let A be an octonion division algebra over a ﬁeld F . Consider a matrix B ∈ Mn (A).
Let σL (B) denote the set of left eigenvalues of B, and let
ΣL (B) = {(λ, ⃗v) : λ ∈ A, ⃗0 ̸= ⃗v ∈ An , B⃗v = λ⃗v }.
Lemma 3.1. Let λ be a left eigenvalue of a matrix B ∈ Mn (A) and ⃗v ∈ An an associated
eigenvector, where A is an octonion division algebra over a ﬁeld F . Then for any 0 ̸= e ∈
A, the element eλ is an eigenvalue of the matrix eB with an associated eigenvector ⃗v e.
Proof. The algebra A satisﬁes the Moufang identity (xy)(zx) = x(yz)x. Therefore for any
e ∈ A we have (eB)(⃗v e) = e(B⃗v )e = e(λ⃗v )e = (eλ)(⃗v e).
Lemma 3.2. Let B ∈ Mn (A) be a lower (upper) triangular matrix with diagonal (a1 , . . . , an ),
where A is any (not necessarily associative) division algebra over a ﬁeld F . Then σL (B) =
{a1 , . . . , an }.

## PDF page 7

Roots and right factors of polynomials and left eigenvalues of matrices over Cayley–Dickson algebras 7

Proof. A direct elementary proof when A is a ﬁeld does not use associativity or commutativity, so transfers to our case. To summarize, it is clear that σL (B) ⊇ {a1 , . . . , an },
since it is easy to see that for each ai for 1 ≤ i ≤ n, an associated eigenvector is
e⃗i = (0, . . . , 1, . . . 0)T with 1 in the i-th position (Here and in the rest of the article
⃗v T denotes the transpose of the vector ⃗v). In the other direction, let λ ∈ σL (B), and
⃗v = (v1 , . . . , vn )T ∈ An be an associated eigenvector. The ﬁrst row of B produces the
equation a1 v1 = λv1 so either λ = a1 or v1 = 0. If v1 = 0 we continue to the second row
to obtain a2 v2 = λv2 implying either λ = a2 or v2 = 0. Continuing by induction we prove
that either λ ∈ {a1 , . . . , an } or ⃗v = 0, where the latter is a contradiction.
For a given f (x) ∈ A[x], let R(f (x)) be the set of roots of f (x) in A. We denote by
LMR(f (x)) the union of R(c · f (x)) where c ranges over all nonzero elements of A.
)
(
a b
be a matrix deﬁned over an alternative algebra A. A
Lemma 3.3. Let B =
( )c d
1
∈ A2 is an eigenvector associated to an eigenvalue λ ∈ σL (B)
vector of the form ⃗v =
s
if and only if s is a root of the quadratic polynomial f (x) = bx2 + (a − d)x − c ∈ A[x] and
λ = a + bs.
Proof. The equation B⃗v = λ⃗v induces the following system of equations:
{
a + bs = λ
c + ds = λs

(1)

Substituting λ = a + bs in the second equation, and using alternative identity (bs)s =
bs2 we obtain f (s) = bs2 + (a − d)s − c = 0, as required. The other direction follows readily
by taking a root s of f (x), setting λ = a + bs and comparing B⃗v and λ⃗v.
Lemma 3.4. Let M be a Moufang loop, and x, y, z ∈ M. Then x((x−1 y)z) = (y(zx))x−1 .
Proof. Let t = x−1 y. Then y = xt and
(y(zx))x−1 = ((xt)(zx))x−1 = (x(tz)x)x−1 = x((tz)(xx−1 )) = x(tz) = x((x−1 y)z).
The second equality follows from the Moufang identity (xt)(zx) = x(tz)x, and the third
by the Moufang identity (zxz)y = z(x(zy)) (or the fact that x and tz form a subgroup of
M).
(
)
a b
Theorem 3.5. Given a matrix B =
over a division octonion algebra A, if b = 0
c d
then σL (B) = {a, d}, and if b ̸= 0 then
}
{( ( ) )
1
×
−1
−1
· t : t ∈ A , s ∈ R(t f (x)), λ = a + t((t b)s) ,
ΣL (B) =
λ,
s

## PDF page 8

8

Adam Chapman and Solomon Vishkautsan

where f (x) = bx2 + (a − d)x − c. In particular, when b ∈ F × , we have
σL (B) = {λ : b−1 (λ − a) ∈ LMR(f (x))}.
Proof. When b = 0, (
the )
result follows from Lemma 3.2, so we assume that b ̸= 0. Now let
v
λ ∈ σL (B), and ⃗v = 1 ∈ A2 be an associated eigenvector. If v1 = 0 then from B⃗v = λ⃗v
v2
( )
v
we get bv2 = 0, so v2 = 0, a contradiction. Therefore, if ⃗v = 1 is an eigenvector, then
v2
−1
−1
v1 ̸= 0. By Lemma 3.1, we get
( that)v1 λ is a left eigenvalue of the matrix v1 B with
1
.
associated eigenvector ⃗v v1−1 =
v2 v1−1
By Lemma 3.3 we get that v2 v1−1 is a root of v1−1 f (x), where f (x) = bx2 + (a − d)x − c,
with v1−1 λ = v1−1 a + (v1−1 b)(v2 v1−1 ). Using the Moufang identity (xy)(zx) = x(yz)x on the
last equality, we get v1−1 λ = v1−1 a + v1−1 (bv2 )v1−1 . Multiplying by v1 on the left, we get
λ = a + (bv2 )v1−1 (Here we used the inverse identity x−1 (xy) = y for x ̸= 0). Summing up,
we know that v2 v1−1 ∈ LMR(f (x)), and so
{(
(
))
}
v1
−1
−1
−1
: v1 ̸= 0, v2 v1 ∈ R(v1 f (x)) .
(2)
ΣL (B) ⊆
a + (bv2 )v1 ,
v2
(
(
))
v1
−1
Now let a + (bv2 )v1 ,
be a pair in the set on the right hand side of (2). By
v2
(
)
1
−1
−1
is an eigenvector of the matrix
v2 v1 ∈ R(v1 f (x)) and Lemma 3.3 we get that
v2 v1−1
v1−1 B )
associated to the eigenvalue v1−1 a + (v1−1 b)(v2 v1−1 ). Thus by Lemma 3.1 we know
(
v1
is an eigenvector of the matrix B associated to the eigenvalue a + (bv2 )v1−1 (we
v2
used the Moufang
)) (xy)(zx) = x(yz)x to simplify the eigenvalue to this form), so
(
( identity
v1
∈ ΣL (B). We have thus proved that
a + (bv2 )v1−1 ,
v2
))
}
{(
(
v1
−1
−1
−1
: v1 ̸= 0, v2 v1 ∈ R(v1 f (x)) .
ΣL (B) =
a + (bv2 )v1 ,
v2
Setting t = v1 and s = v2 v1−1 , we obtain (here we used the identity x((x−1 y)z) =
(y(zx))x−1 from Lemma 3.4)
}
{( ( ) )
1
×
−1
−1
· t : t ∈ A , s ∈ R(t f (x)), λ = a + t((t b)s) .
ΣL (B) =
λ,
s
When b ∈ F × , λ depends only on the value of s and not of t, and thus σL (B) = {λ :
b−1 (λ − a) ∈ LMR(f (x))}.
It is known that any matrix with quaternion coeﬃcients has a left eigenvalue, see [17].
At least for 2 × 2 matrices we can say the same for octonion matrices.

## PDF page 9

Roots and right factors of polynomials and left eigenvalues of matrices over Cayley–Dickson algebras 9

Corollary 3.6. Let B ∈ M2 (O). Then σL (B) ̸= ∅, i.e. the 2 × 2 matrix B always has a left
eigenvalue.
Proof. Setting t = 1 in the theorem, and using the fact that O is “algebraically
closed”
( )
1
for some s ∈ O
(see Proposition 2.5), there always exists an eigenvector of the form
s
associated to the eigenvalue a + bs.
Corollary 3.7. Suppose b ̸= 0. When d = 0, we have 0 ∈ σL (B) if and only if c = 0.
When d ̸= 0, we have 0 ∈ σL (B) if and only if there exists a nonzero t ∈ A satisfying
d−1 (ct) − b−1 (at) = 0.
( ( ) )
1
Proof. Let λ,
· t ∈ ΣL (B). By Theorem 3.5 we get the two conditions s ∈
s
R(t−1 f (x)) and λ = a + t((t−1 b)s).
Setting a′ = t−1 a, b′ = t−1 b, c′ = t−1 c, d′ = t−1 d, λ′ = t−1 λ, the conditions become
′ 2
b s + (a′ −d′ )s −c′ = 0 and s = b′−1 (λ′ −a′ ). Plugging in s = b′−1 (λ′ −a′ ) into the equation
b′ s2 + (a′ − d′ )s − c′ = 0 we obtain a two-sided (non-standard) polynomial equation in λ′
whose constant term (i.e., the coeﬃcient obtained by setting λ′ = 0) is d′ (b′−1 a′ ) − c′ .
Assume d = 0. Then the constant term described above is equal to −c′ , which is zero
if and only if c = 0. Therefore 0 ∈ σL (B) if and only if c = 0.
When d ̸= 0, the constant term is 0 if and only if b′−1 a′ − d′−1 c′ = 0. Therefore,
0 ∈ σL (B) if and only if (b−1 t)(t−1 a) − (d−1t)(t−1 c) = 0. By multiplying from the right
by t and applying the Moufang identity ((xy)z)y = x(yzy), the last equation becomes
d−1 (ct) − b−1 (at) = 0, as required.
)
(
i 1
over the real octonion division algebra
Example 3.8. Consider the matrix B =
ij j
O with standard generators i, j, ℓ. This matrix is deﬁned over the quaternion
subalgebra
(
)
i
ij
1
−1
(as
H, and it is invertible as a quaternion matrix, with inverse B = − 2
−1 j
in the complex case, if a quaternion matrix has a one sided inverse, then it has a twosided inverse; see [18, Proposition 4.1]), and therefore 0 is not in its spectrum. However,
for t = ℓ we have d−1 (ct) − b−1 (at) = j −1 ((ij)ℓ) (
− 1−1 (iℓ)
) = 0, so by Corollary 3.7 we
−ℓ
. Note that its right multiple
get 0 ∈ σL (B). A suitable eigenvector is w
⃗ =
iℓ
)
(
−1
is not an eigenvector of B anymore, unlike the quaternionic case (where
w
⃗ · ℓ−1 =
i
the set of eigenvectors associated to a left eigenvalue is closed under multiplication by a
scalar to the right). Therefore, this matrix, as a matrix in M(2 (O) is both
) and a
) ( invertible
1 −i
i 0
where
·
zero divisor. Moreover, it is a product of two matrices B =
1
i
0 ij
neither is a zero divisor. In fact, the left matrix only has i, ij in its spectrum by Lemma 3.2
and the right one does not have 0 in its spectrum by Corollary 3.7.

## PDF page 10

10

Adam Chapman and Solomon Vishkautsan

In order to compute the left eigenvalues of B, we shall consider the polynomial f (x) =
x + (i − j)x − ij, and then σL (B) = LMR(f (x)) + i. By [7, Remark 3.5],
2

LMR(f (x)) = {ξ · (i − j)−1 (ij + 1) + (1 − ξ)(ij + 1)(i − j)−1 + zℓ : 0 ≤ ξ ≤ 1,
Norm(z) = ξ · (1 − ξ) · Norm([ij − 1, (i − j)−1 ]}
= {ξj + (1 − ξ) · (−i) + zℓ : 0 ≤ ξ ≤ 1, Norm(z) = 2ξ(1 − ξ)}.
In particular, for ξ = 0, we get −i ∈ LMR(f (x)). Thus 0 ∈ LMR(f (x)) + i = σL (B).
The arguments presented in the proof of Theorem 3.5 can also be applied to an associative division algebra D to describe the left eigenvalues of any 2 × 2 matrix over D.
Indeed, since the nonzero elements of an associative division algebra form a Moufang loop
with respect to its product, Theorem 3.5 and the preceding lemmas are applicable. Since
the algebra is associative, the expression a + t(t−1 b)s appearing in Theorem 3.5 becomes
a + s, and thus:
)
(
a b
over
Corollary 3.9. Given an associative division algebra D and a matrix B =
c d
D, if b = 0 then σL (B) = {a, d} and if b ̸= 0, then
σL (B) = {λ ∈ D : b−1 (λ − a) ∈ R(bx2 + (a − d)x − c)}.
We should mention here that Theorem 2.3 in [12] for quaternion matrices is of the form
of the corollary, and the proof there works for associative division algebras as well.

Acknowledgements
The authors wish to express their sincere gratitude to the three anonymous referees
who read the manuscript carefully and provided many helpful comments and suggestions.

References
[1] M. Brešar, P. Šemrl, and Š. Špenko. On locally complex algebras and low-dimensional
Cayley-Dickson algebras. J. Algebra, 327:107–125, 2011.
[2] R. E. Cawagas. On the structure and zero divisors of the Cayley-Dickson sedenion
algebra. Discuss. Math. Gen. Algebra Appl., 24(2):251–265, 2004.
[3] A. Chapman. Factoring octonion polynomials.
30(7):1457–1463, 2020.

Internat. J. Algebra Comput.,

[4] A. Chapman. Polynomial equations over octonion algebras. J. Algebra Appl., 19(6):10,
2020.

## PDF page 11

Roots and right factors of polynomials and left eigenvalues of matrices over Cayley–Dickson algebras11

[5] A. Chapman, A. Guterman, S. Vishkautsan, and S. Zhilina. Roots and critical points
of polynomials over Cayley-Dickson algebras. Comm. Algebra, 51(4):1355–1369, 2023.
[6] A. Chapman and C. Machen. Standard polynomial equations over division algebras.
Adv. Appl. Cliﬀord Algebr., 27(2):1065–1072, 2017.
[7] A. Chapman and S. Vishkautsan. Roots and dynamics of octonion polynomials.
Commun. Math., 30(2):25–36, 2022.
[8] E. Darpö and P. Nystedt. Von-Neumann ﬁniteness and reversibility in some classes
of non-associative algebras. Algebr. Represent. Theory, 24(5):1245–1258, 2021.
[9] T. Dray and C. A. Manogue. The geometry of the octonions. World Scientiﬁc Publishing Co. Pte. Ltd., Hackensack, NJ, 2015.
[10] S. Eilenberg and I. Niven. The “fundamental theorem of algebra” for quaternions.
Bull. Amer. Math. Soc., 50:246–248, 1944.
[11] R. Ghiloni and A. Perotti. The quaternionic Gauss–Lucas theorem. Ann. Mat. Pura
Appl. (4), 197(6):1679–1686, 2018.
[12] L. Huang and W. So. On left eigenvalues of a quaternionic matrix. Linear Algebra
Appl., 323(1-3):105–116, 2001.
[13] Y.-L. Jou. The “fundamental theorem of algebra” for Cayley numbers. Acad. Sinica
Science Record, 3:29–33, 1950.
[14] H. C. Lee. Eigenvalues and canonical forms of matrices with quaternion coeﬃcients.
Proc. Roy. Irish Acad. Sect. A., 52:253–260, 1949.
[15] R. D. Schafer. On the algebras formed by the Cayley-Dickson process. Amer. J.
Math., 76:435–446, 1954.
[16] D. M. Wilczyński. On the fundamental theorem of algebra for polynomial equations
over real composition algebras. J. Pure Appl. Algebra, 218(7):1195–1205, 2014.
[17] R. M. W. Wood. Quaternionic eigenvalues. Bull. London Math. Soc., 17(2):137–138,
1985.
[18] F. Zhang. Quaternions and matrices of quaternions. Linear Algebra Appl., 251:21–57,
1997.
Received: November 29, 2023
Accepted for publication: February 9, 2024
Communicated by: Ivan Kaygorodov and David Towers
