Source: https://doi.org/10.3934/math.2022483
PDF sha256: b414f9facf8ad61065f07e099c3e85c5ff2d95d161d2503532883a68df4c656f
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of some-properties-and-vajda-theorems-of-split-dual-fibonacci-and-split-dual-lucas--b414f9facf.pdf

Transcription of `some-properties-and-vajda-theorems-of-split-dual-fibonacci-and-split-dual-lucas--b414f9facf.pdf` in this directory, 9 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-9 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

AIMS Mathematics, 7(5): 8645–8653.
DOI: 10.3934/math.2022483
Received: 27 September 2021
Revised: 20 February 2022
Accepted: 22 February 2022
Published: 02 March 2022

http://www.aimspress.com/journal/Math

Research article

Some properties and Vajda theorems of split dual Fibonacci and split dual
Lucas octonions
Ümit Tokeşer1 , Tuğba Mert2,∗ and Yakup Dündar1
1

Department of Mathematics, Faculty of Arts and Sciences, Kastamonu University, Kastamonu
37100, Turkey
2
Department of Mathematics, Faculty of Sciences, Sivas Cumhuriyet University, Sivas 58100,
Turkey
* Correspondence: Email: tmert@cumhuriyet.edu.tr.
Abstract: In this paper, we introduce split dual Fibonacci and split dual Lucas octonions over the
˜ (a, b, c), where a, b and c are real numbers. We obtain Binet formulas for these octonions.
algebra Õ
Also, we give many identities and Vajda theorems for split dual Fibonacci and split dual Lucas
octonions including Catalan’s identity, Cassini’s identity and d’Ocagne’s identity.
Keywords: octonions; dual Fibonacci and dual Lucas numbers; split dual Fibonacci and split dual
Lucas octonions
Mathematics Subject Classification: 11B39, 11R52

1. Introduction
Quaternions and octonions were described by Sir William R. Hamilton in 1843 and Cayley-Dickson
in 1845, respectively. In 1873, Clifford extended real numbers to dual numbers [16]. For the real
numbers a and a∗ , the form of the dual number d is
d = a + εa∗
where ε is the dual unit and
ε2 = 0, ε , 0.
The Binet formulas for the Fibonacci and Lucas numbers are
Fn =

αn − βn
and Ln = αn + βn
α−β

## PDF page 2

8646
√

√

where α = 1+2 5 and β = 1−2 5 are the roots of the characteristics equation
x2 − x − 1 = 0.
The positive root α is known as golden ratio. The quaternions were introduced by Horadam [3]. Some
authors studied Fibonacci or split Fibonacci quaternions [1, 2, 4–6, 8, 10–12, 17, 18].
Keçilioğlu and Akkuş gave the Fibonacci and Lucas octonions and their Binet formulas [7]. Halici
also worked on dual Fibonacci octonions in [9] and obtained the Binet formula with its generator
function. Ünal et al. investigated properties of dual Fibonacci and dual Lucas octonions [14]. In
addition, Bilgici et al. obtained generalized Fibonacci and Lucas octonions, and gave a lot of identities
to them [15].
In [13], Akkuş and Keiliolu took the form
a + lb
of a pair of quaternions, shown as (a, b), with a new imaginary unit l and defined the product rule as
(
)
(a + lb) (c + ld) = ac + λdb̄ + l (ād + cb)
where λ2 = 1. When λ = −1 and λ = 1 above, octonions and split octonions are obtained, respectively.
Split octonions form an eight-dimensional algebra on real numbers. The difference from standard
octonions is that it contains elements that are different from zero. Accordingly, let us show the split
˜ In addition, Akkuş and Keiliolu have given the nth split
dual octonion algebra on real numbers with Õ.
Fibonacci and nth split Lucas octonions in the form of
Qn =

7
∑

Fn+s e s

i=1

and
Tn =

7
∑

Ln+s e s

i=1

where Fn is nth Fibonacci number, Ln is nth Lucas number [13]. If we take a = 1, b = 1 and c = −1 in
the generalized octonion multiplication table in [15], we get the split octonion table (see Table 1).
Table 1. Multiplication table of split octonion.
·
e0
e1
e2
e3
e4
e5
e6
e7

AIMS Mathematics

e0
e1
e2
e3
e0
e1
e2
e3
e1 −1 e3 −e2
e2 −e3 −1 e1
e3
e2 −e1 −1
e4 −e5 −e6 −e7
e5
e4 −e7
e6
e6
e7
e4 −e5
e7 −e6
e5
e4

e4
e4
e5
e6
e7
1
e1
e2
e3

e5
e5
−e4
e7
−e6
−e1
1
−e3
e2

e6
e6
−e7
−e4
e5
−e2
e3
1
−e1

e7
e7
e6
−e5
−e4
−e3
−e2
e1
1

Volume 7, Issue 5, 8645–8653.

## PDF page 3

8647

We define split dual Fibonacci and split dual Lucas numbers by
F̃n = Fn + εFn+1

(1.1)

L̃n = Ln + εLn+1

(1.2)

and

respectively. In this paper, following Keçilioğlu and Akkuş, and Ünal et al., we define the split dual
˜ The nth split dual
Fibonacci and split dual Lucas octonions over the split dual octonion algebra Õ.
Fibonacci octonion S DFOn is
S DFOn =

7
∑

F̃n+s e s

(1.3)

L̃n+s e s

(1.4)

s=0

and the nth split dual Lucas octonion S DLOn is
S DLOn =

7
∑
s=0

where F̃n is nth split dual Fibonacci number and L̃n is nth split dual Lucas number. By using Eq (1.1),
we obtain
S DFOn =
=

7
∑

7
∑
Fn+s e s + ε Fn+s+1 e s

s=0

s=0

7
∑

(Fn+s + εFn+s+1 ) e s

s=0

= S FOn + εS FOn+1
where S FOn =

7
∑

Fn+s e s is split Fibonacci octonion. Similarly, by using Eq (1.2), we have

s=0

S DLOn = S LOn + εS LOn+1
where S LOn =

7
∑

Ln+s e s is split Lucas octonion.

s=0

2. Binet formulas for split dual Fibonacci and Lucas octonions
In this section, we obtain Binet formulas and Vajda theorems for S DFOn and S DLOn . There are
three well-known identities for split dual Fibonacci and Lucas numbers, namely, Catalan’s, Cassini’s
and d’Ocagne’s identities. These types of identities for split dual Fibonacci and Lucas octonions can
be obtained by using the Vajda theorems. The following theorem gives the Binet formulas for these
octonions.
AIMS Mathematics

Volume 7, Issue 5, 8645–8653.

## PDF page 4

8648

Theorem 1. For n ≥ 0, the nth split dual Fibonacci octonion is
S DFOn =

α′ αn − β′ βn
α−β

and nth split dual Lucas octonion is
S DLOn = α′ αn + β′ βn
where α = (1 + εα)
′

7
∑

α e s and β = (1 + εβ)
′

s

7
∑

βses.

s=0

s=0

Proof. In [13], the Binet formulas for the split Fibonacci and split Lucas octonions are as follows:
α∗ αn − β∗ βn
α−β

(2.1)

T n = α∗ αn + β∗ βn

(2.2)

Qn =
and

where α =
∗

7
∑

α e s and β =
s

∗

s=0

7
∑

βses.

s=0

By using from the Eq (2.1), we get the Eq (1.3). We know that
S DFOn =

7
∑

F̃n+s e s =

s=0

7
∑

(Fn + εFn+1 ) e s = S FOn + εS FOn+1 .

s=0

When the Binet formula of split Fibonacci octonion is used in this last equation, we get
α∗ αn − β∗ βn
α∗ αn+1 − β∗ βn+1
+ε
α−β
α−β
∗ n
∗ n
αα
ββ
(1 + εα) −
(1 + εβ) .
=
α−β
α−β

S DFOn =

If the expressions α∗ and β∗ given in [13] are used,
7
7
∑
∑
αn
βn
α′ αn − β′ βn
s
(1 + εα) α e s −
(1 + εβ) β s e s =
S DFOn =
α−β
α−β
α−β
s=0
s=0

is obtained. By using similar method, we get Binet formula of split dual Lucas octonion.

□

Using Binet’s formulas, we can easily derive the identities between split dual Fibonacci and split
dual Lucas octonions.
Now, we give some useful identities that play very important roles throughout the paper for
calculations.
AIMS Mathematics

Volume 7, Issue 5, 8645–8653.

## PDF page 5

8649

Lemma 1. We have obtained followings
(
)
√ 545
1305
(α ) =
+ S PO0 + 5
+ S FO0 ,
2
2
(
)
√ 545
1305
∗ 2
(β ) =
+ S PO0 − 5
+ S FO0 ,
2
2
√
α∗ β∗ = S PO0 + 5λ,
√
β∗ α∗ = S PO0 − 5λ,
∗ 2

where
λ = −e1 − e2 + 4e3 − 3e4 + 9e5 + 6e6 − 6e7 .
Proof. The proof is completed when a = b = 1 and c = −1 in Lemma 2 in [15].

□

Now we give Vajda theorems for split dual Fibonacci and split dual Lucas octonions that could be
reduced to some special cases.
Theorem 2. For any integers n, r and s, we get
S DFOn+r S DFOn+s − S DFOn S DFOn+r+s = (−1)n Fr (S PO0 F s − λL s ) (1 + ε)
and
S DLOn+r S DLOn+s − S DLOn S DLOn+r+s = 5 (−1)n+1 Fr (S PO0 F s − λL s ) (1 + ε) .
Proof. We make proof for split dual Fibonacci octnions. We can write
S DFOn+r S DFOn+s − S DFOn S DFOn+r+s = Q̃n+r Q̃n+s − Q̃n Q̃n+r+s
(
)
+ε Q̃n+r Q̃n+s+1 + Q̃n+r+1 Q̃n+s − Q̃n Q̃n+r+s+1 − Q̃n+1 Q̃n+r+s .
We calculate the following expression
Q̃n+r Q̃n+s − Q̃n Q̃n+r+s

(2.3)

and we get
Q̃n+r Q̃n+s − Q̃n Q̃n+r+s
[
]
1
(α∗ αn+r − β∗ βn+r ) (α∗ αn+s − β∗ βn+s )
=
∗ n
∗ n
∗ n+r+s
− β∗ βn+r+s )
(α − β)2 − (α α − β β ) (α α
[ ∗ ∗
]
1
α β (−αn+r βn+s + αn βn+r+s )
=
∗ ∗
n+s n+r
n+r+s n
β)
(α − β)2 +β α (−α β + α
]
√
(−1)n [
=
Fr P0 (α s − β s ) − 5λ (α s + β s )
α−β
√
⎡ ( s
⎤
)
⎥⎥
⎢⎢⎢
α − βs
5
n
s
s
= (−1) Fr ⎢⎣P0
−
λ (α + β )⎥⎥⎦
α−β
α−β
= (−1)n Fr (P0 F s − λL s ) .
AIMS Mathematics

Volume 7, Issue 5, 8645–8653.

## PDF page 6

8650

If s + 1 is written instead of s in Eq (2.3), then
Q̃n+r Q̃n+s+1 − Q̃n Q̃n+r+s+1 = (−1)n Fr (P0 F s+1 − λL s+1 )
is obtained. If n + 1 is written instead of n and s − 1 is written instead of s in equation given above,
then we get
Q̃n+r+1 Q̃n+s − Q̃n+1 Q̃n+r+s = (−1)n+1 Fr (P0 F s−1 − λL s−1 ) .
In this case,
Q̃n+r Q̃n+s+1 − Q̃n Q̃n+r+s+1 + Q̃n+r+1 Q̃n+s − Q̃n+1 Q̃n+r+s = (−1)n Fr (P0 F s − λL s )
and so,
S DFOn+r S DFOn+s − S DFOn S DFOn+r+s = (−1)n Fr (S PO0 F s − λL s ) (1 + ε) .
□

Similarly, we can prove the Vajda theorem for split dual Lucas octonions.
From Vajda theorems, we also have the following special identities for these octonions:

Corollary 1. If −r is taken instead of s in the Vajda theorem, Catalan’s identities are obtained for split
dual Fibonacci and split dual Lucas octonions, respectively:
(
)
S DFOn+r S DFOn−r − S DFO2n = (−1)n−r+1 S PO0 Fr2 + λF2r (1 + ε)
and
(
)
S DLOn+r S DLOn−r − S DLO2n = 5 (−1)n−r S PO0 Fr2 + λF2r (1 + ε) .
Corollary 2. If −r is taken instead of s and then 1 is taken instead of r in the Vajda theorem, Cassini’s
identities are obtained for split dual Fibonacci and split dual Lucas octonions, respectively :
S DFOn+1 S DFOn−1 − S DFO2n = (−1)n (S PO0 + λ) (1 + ε)
and
S DLOn+1 S DLOn−1 − S DLO2n = 5 (−1)n−1 (S PO0 + λ) (1 + ε)
where F0 = 0, F1 = 1 and F2 = 1.
Corollary 3. If m is taken instead of n, n − m is taken instead of s and then 1 is taken instead of r
in the Vajda theorem, d’Ocagne’s identities are obtained for split dual Fibonacci and split dual Lucas
octonions, respectively:
S DFOm+1 S DFOn − S DFOm S DFOn+1 = (−1)m (S PO0 Fn−m − λLn−m ) (1 + ε)
and
S DLOm+1 S DLOn − S DLOm S DLOn+1 = 5 (−1)m+1 (S PO0 Fn−m − λLn−m ) (1 + ε) .
AIMS Mathematics

Volume 7, Issue 5, 8645–8653.

## PDF page 7

8651

3. Some results for split dual Fibonacci and split dual Lucas octonions
In this section, after deriving famous three identities Catalan’s, Cassini’s and d’Ocagne’s by using
the Vajda theorems, we present some other identities for the split dual Fibonacci and split dual Lucas
octonions.
Theorem 3. Split dual Fibonacci octonions satisfy the following identities;
i) S DFOm+n + (−1)n S DFOm−n = S DFOm Ln ,
ii) S DFOn+r Fn+r − S DFOn−r Fn−r = F2r S DFO2n ,
iii) S DFOn S DFOm − S DFOm S DFOn = 2 (−1)m+1 λFn−m (1 + ε) .
Proof. We prove only the first identity of this theorem. We need the Binet formulas for the split dual
Fibonacci octonions.
i) S( DFOm+n + (−1))n S DFOm−n
(
)
= Q̃m+n + εQ̃m+n+1 + (αβ)n Q̃m−n + εQ̃m−n+1
(
)
= (αn + βn ) Q̃m + εQ̃m+1 = (αn + βn ) S DFOm = S DFOm Ln .
□

The second and third identities can be proved similarly.
Theorem 4. Split dual Lucas octonions satisfy the following identities;
i) S DLOn+r Ln+r − S DLOn−r Ln−r = 5F2r S DFO2n ,
ii) S DLOn+r Ln+r + S DLOn−r Ln−r = L2r S DLO2n + 2 (−1)n+r S DLO0 ,
iii) S DLOn S DLOm − S DLOm S DLOn = 10 (−1)m λFn−m (1 + ε).

Proof. We prove only the first identity of this theorem. We need the Binet formulas for the split dual
Lucas octonions
(
)
(
)
i) S DLOn+r Ln+r − S DLOn−r Ln−r = P̃n+r + εP̃n+r+1 Ln+r − P̃n−r + εP̃n−r+1 Ln−r
(
)(
)
(
)(
)
= α2r − β2r α∗ α2n − β∗ β2n + ε α2r − β2r α∗ α2n+1 − β∗ β2n+1
( 2r
) [ ( ∗ 2n
)
( ∗ 2n+1
) ]
2r
α α − β∗ β2n
αα
− β∗ β2n+1
2 α −β
= (α − β)
+ε
α−β )
α−β
α−β
(
= 5F2r Q̃2n + εQ̃2n+1 = 5F2r S DFO2n .
The other two identities can be proved similar to the theorem proved by using split dual Fibonacci
octonion.
□
Theorem 5. Split dual Fibonacci and split dual Lucas octonions satisfy the following identities;
i) S DFOm S DLOn − S DFOn S DLOm = 2 (−1)m+1 S PO0 Fn−m (1 + ε) ,
AIMS Mathematics

Volume 7, Issue 5, 8645–8653.

## PDF page 8

8652

ii) S DFOm S DLOn − S DLOm S DFOn = 2 (−1)m+1 (S PO0 Fn−m − λLn−m ) (1 + ε) ,
iii) S DLOn+r S DFOn+s − S DLOn+s S DFOn+r = 2 (−1)n+r S PO0 F s−r (1 + ε) ,
iv) S DLOn+r Fn+t + S DLOn+t Fn+r = 2S DFO2n+r+t − (−1)n+1 Lr−t S DFO0 ,
v) S DFOn+r Ln+r + S DFOn−r Ln−r = L2r S DFO2n + 2 (−1)n+r S DFO0 .
Proof. The proof of the theorem can be done similarly by the Binet formulas for the nth split dual
Fibonacci and nth split dual Lucas octonions proved above.
□
4. Conclusions
In the articles about Quaternions and Octonions in the literature, Catalan’s, Cassini’s and
d’Ocagne’s identities have been obtained by using their Binet formulas. In this paper, the Vajda
theorems are obtained for split dual Fibonacci and split dual Lucas octonions. We aimed to introduce
Vajda theorem, which is not included in the literature and will contribute to finding Catalan’s,
Cassini’s and d’Ocagne’s identities. In the Vajda theorem, when we write the criteria in Corollaries
1–3 in our study, Catalan’s, Cassini’s and d’Ocagne’s identities are obtained, respectively. Thus, when
we obtain the Vajda theorem by using the Binet formula, we get these three identities, which are well
known in the literature, without the need for any other calculations.
Acknowledgments
The authors are grateful to the reviewers’ valuable comments that improved the manuscript.
Conflict of interest
The authors declare that they have no conflicts of interest.
References
1. M. Akyiğit, H. H. Köksal, M. Tosun, Split Fibonacci quaternions, Adv. Appl. Clifford Algebras, 25
(2013), 535–545. https://doi.org/10.1007/s00006-013-0401-9
2. M. Akyiğit, H. H. Köksal, M. Tosun, Fibonacci generalized quaternions, Adv. Appl. Clifford
Algebras, 24 (2014), 631–641. https://doi.org/10.1007/s00006-014-0458-0
3. A. F. Horadam, Complex Fibonacci numbers and Fibonacci quaternions, Am. Math. Mon., 70
(1963), 289–291. https://doi.org/10.2307/2313129
4. C. Flaut, V. Shpakivskyi, On generalized Fibonacci quaternions and Fibonacci-Narayan
quaternions, Adv. Appl. Clifford Algebras, 23 (2013), 673–688. https://doi.org/10.1007/s00006013-0388-2
AIMS Mathematics

Volume 7, Issue 5, 8645–8653.

## PDF page 9

8653

5. S. Halici, On Fibonacci quaternions, Adv. Appl. Clifford Algebras, 22 (2012), 321–327.
https://doi.org/10.1007/s00006-011-0317-1
6. S. Halici, On complex Fibonacci quaternions, Adv. Appl. Cilifford Algebras, 23 (2013), 105–112.
https://doi.org/10.1007/s00006-012-0337-5
7. O. Keçilioğlu, I. Akkuş, The Fibonacci octonions, Adv. Appl. Clifford Algebras, 25 (2015), 151–
158. https://doi.org/10.1007/s00006-014-0468-y
8. A. F. Horadam, Quaternion recurrence relations, Ulam Q., 2 (1993), 22–33.
9. S. Halici, On dual Fibonacci octonions, Adv. Appl. Clifford Algebras, 25 (2015), 905–914.
https://doi.org/10.1007/s00006-015-0550-0
10. T. Koshy, Fibonacci and Lucas numbers with applications, Wiley-Interscience Publications, John
Wiley & Sons, Inc., 2001.
11. I. L. Iakin, Generalized quaternions of higher order, Fibonacci Quart., 15 (1977), 343–346.
12. M. R. Iyer, A note on Fibonacci quaternions, Fibonacci Quart., 7 (1969), 225–229.
13. I. Akkuş, O. Keçilioğlu, Split Fibonacci and Lucas octonions, Adv. Appl. Clifford Algebras, 25
(2015), 517–525. https://doi.org/10.1007/s00006-014-0515-8
14. Z. Ünal, Ü. Tokeşer, G. Bilgici, Some properties of dual Fibonacci and dual Lucas octonions, Adv.
Appl. Clifford Algebras, 27 (2017), 1907–1916. https://doi.org/10.1007/s00006-016-0724-4
15. G. Bilgici, Z. Ünal, Ü. Tokeşer, T. Mert, On Fibonacci and Lucas generalized octonions, Ars
Combinatoria, 138 (2018), 35–44.
16. W. K. Clifford, Preliminary sketch of bi-quaternions, Proc. Lond. Math. Soc., 4 (1871), 381–395.
17. M. N. S. Swamy, On generalized Fibonacci quaternions, Fibonacci Quart., 11 (1973), 547–549.
18. Y. Dündar, Split dual Fibonacci and split dual Lucas octonions, M.Sc. Thesis, Kastamonu
University, Graduate School of Natural and Applied Sciences, Kastamonu, 2018.
c 2022 the Author(s), licensee AIMS Press.
⃝
This
is an open access article distributed under the
terms of the Creative Commons Attribution License
(http://creativecommons.org/licenses/by/4.0)

AIMS Mathematics

Volume 7, Issue 5, 8645–8653.
