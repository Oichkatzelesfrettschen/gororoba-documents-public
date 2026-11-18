Source: https://doi.org/10.3390/math7010074
PDF sha256: d4ca83ccdad3674474c20503c376e94f537b069eb362faf22654d0afe81a6878
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of soykan_2019_tribonacci_and_tribonacci_lucas_sedenions.pdf

Transcription of `soykan_2019_tribonacci_and_tribonacci_lucas_sedenions.pdf` in this directory, 19 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-19 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

mathematics
Article

Tribonacci and Tribonacci-Lucas Sedenions
Yüksel Soykan
Department of Mathematics, Art and Science Faculty, Zonguldak Bülent Ecevit University,
67100 Zonguldak, Turkey; yuksel_soykan@hotmail.com
Received: 14 November 2018; Accepted: 9 January 2019; Published: 11 January 2019

Abstract: The sedenions form a 16-dimensional Cayley-Dickson algebra. In this paper, we introduce
the Tribonacci and Tribonacci-Lucas sedenions. Furthermore, we present some properties of these
sedenions and derive relationships between them.
Keywords: Tribonacci numbers; sedenions; Tribonacci sedenions; Tribonacci-Lucas sedenions
MSC: 11B39; 11B83; 17A45; 05A15

1. Introduction
The Tribonacci sequence { Tn }n≥0 and the Tribonacci-Lucas sequence {Kn }n≥0 are defined by the
third-order recurrence relations:
Tn = Tn−1 + Tn−2 + Tn−3 ,

T0 = 0, T1 = 1, T2 = 1,

(1)

K n = K n −1 + K n −2 + K n −3 ,

K0 = 3, K1 = 1, K2 = 3

(2)

and:
respectively. The Tribonacci concept was introduced by 14-year-old student M.Feinberg [1] in 1963.
The basic properties of it were given in [2–12], and Binet’s formula for the nth number was given
in [13].
The sequences { Tn }n≥0 and {Kn }n≥0 can be extended to negative subscripts by defining:
T−n = − T−(n−1) − T−(n−2) + T−(n−3)
and:
K−n = −K−(n−1) − K−(n−2) + K−(n−3)
for n = 1, 2, 3, . . ., respectively. Therefore, recurrences (1) and (2) hold for all integers n.
By writing Tn−1 = Tn−2 + Tn−3 + Tn−4 , substituting for Tn−2 in (1), and eliminating Tn−2 and
Tn−3 between this recurrence relation and the recurrence relation (1), a useful alternative recurrence
relation is obtained for n ≥ 4 :
Tn = 2Tn−1 − Tn−4 ,

T0 = 0, T1 = T2 = 1, T3 = 2.

(3)

Extension of the definition of Tn to negative subscripts can be proven by writing the recurrence
relation (3) as:
T−n = 2T−n+3 − T−n+4 .
Note that T−n = Tn2−1 − Tn−2 Tn (see [4]).

Mathematics 2019, 7, 74; doi:10.3390/math7010074

www.mdpi.com/journal/mathematics

## PDF page 2

Mathematics 2019, 7, 74

2 of 19

Next, we present the first few values of the Tribonacci and Tribonacci-Lucas numbers with positive
and negative subscripts:
n
Tn
T−n
Kn
K−n

0
0
0
3
3

1
1
0
1
−1

2
1
1
3
−1

3
2
−1
7
5

4
4
0
11
−5

5
7
2
21
−1

6
13
−3
39
11

7
8
24
44
1
4
71 131
−15 3

9
81
−8
241
23

10
149
5
443
−41

...
...
...
...
...

It is well known that for all integers n, the usual Tribonacci and Tribonacci-Lucas numbers can be
expressed using Binet’s formulas:
Tn =

α n +1
β n +1
γ n +1
+
+
(α − β)(α − γ) ( β − α)( β − γ) (γ − α)(γ − β)

(4)

and:
Kn = αn + βn + γn
respectively, where α, β, and γ are the roots of the cubic equation x3 − x2 − x − 1 = 0. Moreover,

α

=

β

=

γ

=

√
√
√
3
19 + 3 33 + 19 − 3 33
,
3
√
√
√
√
3
3
1 + ω 19 + 3 33 + ω 2 19 − 3 33
,
3
√
√
√
√
3
3
1 + ω 2 19 + 3 33 + ω 19 − 3 33
3
1+

√
3

where:

√
−1 + i 3
ω=
= exp(2πi/3),
2
is a primitive cube root of unity. Note that we have the following identities:
α+β+γ
αβ + αγ + βγ
αβγ

= 1,
= −1,
= 1.

The generating functions for the Tribonacci sequence { Tn }n≥0 and Tribonacci-Lucas sequence
{Kn }n≥0 are:
∞
∞
x
3 − 2x − x2
∑ Tn xn = 1 − x − x2 − x3 and ∑ Kn xn = 1 − x − x2 − x3 .
n =0
n =0
We now present some properties of the Tribonacci and Tribonacci-Lucas numbers.
•

We have [3]:
⎛

Tn+1
⎜
N n = ⎝ Tn + Tn−1
Tn

Tn
Tn−1 + Tn−2
Tn−1

⎞
Tn−1
⎟
Tn−2 + Tn−3 ⎠
Tn−2

and:
tr ( N n )
Cn

= Kn = Tn + 2Tn−1 + 3Tn−2 = 3Tn+1 − 2Tn − Tn−1 ,
= − Tn2 + 2Tn2−1 + 3Tn2−2 − 2Tn Tn−1 + 2Tn Tn−2 + 4Tn−1 Tn−2

## PDF page 3

Mathematics 2019, 7, 74

3 of 19

where:

⎛

1
⎜
N=⎝ 1
1

1
0
0

⎞
0
⎟
1 ⎠,
0

tr (.) is the trace operator and Cn is defined by:
Cn = αn βn + αn γn + βn γn

•

which is the sum of the determinants of the principal minors of order two of N n .
We have [4]:
Tn3−1 − 1

= 2Tn−2 Tn−1 Tn + Tn−3 Tn−1 Tn+1 − Tn2−2 Tn+1 − Tn−3 Tn2
= Tn−2 (2Tn−1 Tn − Tn+1 ) + Tn−3 ( Tn2 − Tn−1 Tn+1 ).

•

Tribonacci numbers satisfy the following equality [12]:
Tk+n = Tk Kn − Tk−n Cn + Tk−2n .

In this paper, we define Tribonacci and Tribonacci-Lucas sedenions in the next section and
give some properties of them. Before giving their definition, we present some information on
Cayley-Dickson algebras.
The algebras C (complex numbers), H (quaternions), and O (octonions) are real division algebras
obtained from the real numbers R by a doubling procedure called the Cayley-Dickson process
(construction). By doubling R (dim 20 = 1), we obtain the complex numbers C (dim 21 = 2); then,
C yields the quaternions H (dim 22 = 4); and H produces octonions O (dim 23 = 8). The next
doubling process applied to O then produces an algebra S (dim 24 = 16) called the sedenions.
This doubling process can be extended beyond the sedenions to form what are known as the 2n -ions
(see for example [14–16]).
Next, we explain this doubling process.
The Cayley-Dickson algebras are a sequence A0 , A1 , . . . of non-associative R-algebras with
involution. The term “conjugation” can be used to refer to the involution because it generalizes
the usual conjugation on the complex numbers. For a full explanation of the basic properties
of Cayley-Dickson algebras, see [14]. Cayley-Dickson algebras are defined inductively. We begin
by defining A0 to be R. Given An−1 , the algebra An is defined additively to be An−1 × An−1 .
Conjugation in An is defined by:
( a, b) = ( a, −b)
multiplication is defined by:

( a, b)(c, d) = ( ac − db, da + bc)
and addition is defined by componentwise as:

( a, b) + (c, d) = ( a + c, b + d).
√
Note that An has dimension 2n as an R-vector space. If we set, as usual, ∥ x ∥ = Re( xx ) for
x ∈ An , then xx = xx = ∥ x ∥2 .
Now, suppose that B16 = {ei ∈ S : i = 0, 1, 2, . . . , 15} is the basis for S, where e0 is the identity
(or unit) and e1 , e2 , . . . , e15 are called imaginaries. Then, a sedenion S ∈ S can be written as:
15

15

i =0

i =1

S = ∑ a i ei = a0 + ∑ a i ei

## PDF page 4

Mathematics 2019, 7, 74

4 of 19

where a0 , a1 , . . . , a15 are all real numbers. Here, a0 is called the real part of S, and ∑15
i =1 ai ei is called its
imaginary part.
The addition of sedenions is defined as componentwise, and multiplication is defined as follows:
if S1 , S2 ∈ S, then we have:
(
)(
)
15

∑ a i ei

S1 S2 =

i =0

15

∑ bi e i

i =0

15

= ∑ a i b j ( ei e j ).

(5)

i,j=0

By setting i ≡ ei where i = 0, 1, 2, . . . , 15, the multiplication rule of the base elements ei ∈ B16 can
be summarized as in the following Figure 1 (see [17,18]).

0
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

0

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

0
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

1
−0
−3
2
−5
4
7
−6
−9
8
11
− 10
13
− 12
− 15
14

2
3
−0
−1
−6
−7
4
5
− 10
− 11
8
9
14
15
− 12
− 13

3
−2
1
−0
−7
6
−5
4
− 11
10
−9
8
15
− 14
13
− 12

4
5
6
7
−0
−1
−2
−3
− 12
− 13
− 14
− 15
8
9
10
11

5
−4
7
−6
1
−0
3
−2
− 13
12
− 15
14
−9
8
− 11
10

6
−7
−4
5
2
−3
−0
1
− 14
15
12
− 13
10
11
8
9

7
6
−5
−4
3
2
−1
−0
− 15
− 14
13
12
− 11
− 10
9
8

8
9
10
11
12
13
14
15
−0
−1
−2
−3
−4
−5
−6
−7

9
−8
11
− 10
13
− 12
− 15
14
1
−0
3
−2
5
−4
−7
6

10
− 11
−8
9
14
15
− 12
− 13
2
−3
−0
1
6
7
−4
−5

11
10
−9
−8
− 14
15
− 12
13
2
3
−1
−0
7
−6
5
−4

12
− 13
− 14
− 15

13
12
− 15
14
−9
−8
− 11
10
5
4
−7
6
−1
−0
−3
2

14
15
12
− 13
− 10
11
−8
−9
6
7
4
−5
−2
3
−0
−1

15
− 14
13
12
− 11
− 10
9
−8
7
−6
5
4
−3
−2
1
−0

−8
9
10
11
4
−5
−6
−7
−0
1
2
3

Figure 1. Multiplication table for sedenions’ imaginary units.

From the above table, we can see that:
e0 ei = ei e0 = ei ; ei ei = −e0 for i ̸= 0; ei e j = −e j ei for i ̸= j and i, j ̸= 0.
The operations requiring the multiplication in (5) are quite a few. The computation of a sedenion
multiplication (product) using the naive method requires 256 multiplications and 240 additions,
while an algorithm, which was given in [19], can compute the same result in only 122 multiplications
(or multipliers, in the hardware implementation case) and 298 additions (for more details, see [19]).
Using direct multiplication, the numbers of the operations requiring for the multiplication of two
n
2 -ions are presented in the following Table 1.
Table 1. Direct multiplication.
2n -Ions

Computational Method

Multiplications

Additions

Quaternions
Octonions
Sedenions

Based on expression (5)
Based on expression (5)
Based on expression (5)

16
64
256

12
56
240

Efficient algorithms for the multiplication of quaternions, octonions, and sedenions with a reduced
number of real multiplications already exist, and the results of synthesizing an efficient algorithm of
computing the two 2n -ions product are given in the following Table 2.

1

## PDF page 5

Mathematics 2019, 7, 74

5 of 19

Table 2. Efficient algorithms for the multiplication.
2n -Ions

Computational Method

Multiplications

Additions

Quaternions
Octonions
Sedenions

Algorithm in [20]
Algorithm in [21]
Algorithm in [19]

8
32
122

88
298

The problem with the Cayley-Dickson process is that each step of the doubling process results in
a progressive loss of structure. R is an ordered field, and it has all the nice properties we are so familiar
with in dealing with numbers like: the associative property, commutative property, division property,
self-conjugate property, etc. When we double R to have C, C loses the self-conjugate property (and is no
longer an ordered field); next, H loses the commutative property, and O loses the associative property.
When we double O to obtain S; S loses the division property. It means that S is non-commutative,
non-associative, and has a multiplicative identity element e0 and multiplicative inverses, but it is not a
division algebra because it has zero divisors; this means that two non-zero sedenions can be multiplied
to obtain zero: an example is (e3 + e10 )(e6 − e15 ) = 0, and the other example is (e2 − e14 )(e3 + e15 ) = 0
(see [18]).
The algebras beyond the complex numbers go by the generic name hypercomplex number.
All hypercomplex number systems after sedenions that are based on the Cayley-Dickson construction
contain zero divisors.
Note that there is another type of sedenions, which is called conic sedenions or sedenions of
Charles Muses, as they are also known; see [22–24] for more information. The term sedenion is also
used for other 16-dimensional algebraic structures, such as a tensor product of two copies of the
biquaternions, or the algebra of four by four matrices over the reals.
In the past, non-associative algebras and related structures with zero divisors have not been given
much attention because they did not appear to have any useful applications in most mathematical
subjects. Recently, theoretical physicists have centered much attention on the Cayley-Dickson algebras
O (octonions) and S (sedenions) because of their increasing usefulness in formulating many of the
new theories of elementary particles. In particular, the octonions O (which is the only non-associative
normed division algebra over the reals; see for example [25,26]) has been found to be involved in many
unexpected areas (such as topology, quantum theory, Clifford algebras, etc.), and sedenions appear in
many areas of science like linear gravity and electromagnetic theory.
Briefly, S, the algebra of sedenions, has the following properties:
•
•
•
•

S is a 16-dimensional non-associative and non-commutative (Cayley-Dickson) algebra over the
reals,
S is not a composition algebra or division algebra because of its zero divisors,
S is a non-alternative algebra, i.e., if S1 and S2 are sedenions, the rules S12 S2 = S1 (S1 S2 ) and
S1 S22 = (S1 S2 )S2 do not always hold,
S is a power-associative algebra, i.e., if S is a sedenion, then Sn Sm = Sn+m .

2. The Tribonacci and Tribonacci-Lucas Sedenions, Their Generating Functions, and
Binet’s Formulas
In this section, we define Tribonacci and Tribonacci-Lucas sedenions and give generating functions
and Binet formulas for them. First, we give some information about quaternion sequences, octonion
sequences, and sedenion sequences from the literature.
Horadam [27] introduced nth Fibonacci and nth Lucas quaternions as:
3

Qn = Fn + Fn+1 e1 + Fn+2 e2 + Fn+3 e3 = ∑ Fn+s es
s =0

## PDF page 6

Mathematics 2019, 7, 74

6 of 19

and:

3

R n = L n + L n +1 e1 + L n +2 e2 + L n +3 e3 = ∑ L n + s e s
s =0

respectively, where Fn and Ln are the nth Fibonacci and Lucas numbers, respectively. He also defined
the generalized Fibonacci quaternion as:
3

Pn = Hn + Hn+1 e1 + Hn+2 e2 + Hn+3 e3 = ∑ Hn+s es
s =0

where Hn is the nth generalized Fibonacci number (which is now called the Horadam number) by the
recursive relation H1 = p, H2 = p + q, Hn = Hn−1 + Hn−2 (p and q are arbitrary integers). Many other
generalizations of Fibonacci quaternions have been given; see for example Halici and Karataş [28]
and Polatlı [29].
Cerda-Morales [30] defined and studied the generalized Tribonacci quaternion sequence that
includes the previously-introduced Tribonacci, Padovan, Narayana, and third-order Jacobsthal
quaternion sequences. She defined the generalized Tribonacci quaternion as:
3

Qv,n = Vn + Vn+1 e1 + Vn+2 e2 + Vn+3 e3 = ∑ Vn+s es
s =0

where Vn is the nth generalized Tribonacci number defined by the third-order recurrence relations:
Vn = rVn−1 + sVn−2 + tVn−3 .
Here, V0 = a, V1 = b, V2 = c are arbitrary integers and r, s, t are real numbers.
Various families of octonion number sequences (such as Fibonacci octonion, Pell octonion,
Jacobsthal octonion, and third-order Jacobsthal octonion) have been defined and studied by a number
of authors in many different ways. For example, Keçilioglu and Akkuş [31] introduced the Fibonacci
and Lucas octonions as:
7

Qn = ∑ Fn+s es
s =0

and:

7

Rn = ∑ Ln+s es
s =0

respectively, where Fn and Ln are the nth Fibonacci and Lucas numbers, respectively. In ref. [32],
Çimen and İpek introduced Jacobsthal octonions and Jacobsthal-Lucas octonions. In ref. [33],
Cerda-Morales introduced third-order Jacobsthal octonions, and also in ref. [34], she defined and
studied Tribonacci-type octonions.
A number of authors have defined and studied sedenion number sequences (such as second-order
sedenions: Fibonacci sedenion, k-Pell and k-Pell-Lucas sedenions, Jacobsthal and Jacobsthal-Lucas
sedenions). For example, Bilgici, Tokeşer, and Ünal [17] introduced the Fibonacci and Lucas
sedenions as:
15

F̂n = ∑ Fn+s es
s =0

and:

15

L̂n = ∑ Ln+s es
s =0

respectively, where Fn and Ln are the nth Fibonacci and Lucas numbers, respectively. In ref. [35],
Catarino introduced k-Pell and k-Pell-Lucas sedenions. In ref. [36], Çimen and İpek introduced
Jacobsthal and Jacobsthal-Lucas sedenions.

## PDF page 7

Mathematics 2019, 7, 74

7 of 19

Gül [37] introduced the k-Fibonacci and k-Lucas trigintaduonions as:
31

TFk,n = ∑ Fk,n+s es
s =0

and:

31

TLk,n = ∑ Lk,n+s es
s =0

respectively, where Fk,n and Lk,n are the nth k-Fibonacci and k-Lucas numbers, respectively.
We now define Tribonacci and Tribonacci-Lucas sedenions over the sedenion algebra S. The nth
Tribonacci sedenion is:
15

15

s =0

s =1

T̂n = ∑ Tn+s es = Tn + ∑ Tn+s es

(6)

and the nth Tribonacci-Lucas sedenion is:
15

15

s =0

s =1

K̂n = ∑ Kn+s es = Kn + ∑ Kn+s es .

(7)

T̂n = T̂n−1 + T̂n−2 + T̂n−3

(8)

K̂n = K̂n−1 + K̂n−2 + K̂n−3 .

(9)

It can be easily shown that:
and:
Note that:
T̂−n = − T̂−(n−1) − T̂−(n−2) + T̂−(n−3)
and:
K̂−n = −K̂−(n−1) − K̂−(n−2) + K̂−(n−3) .
The conjugate of T̂n and K̂n are defined by:
15

T̂n = Tn − ∑ Tn+s es = Tn − Tn+1 e1 − Tn+2 e2 − . . . − Tn+15 e15
s =1

and:

15

K̂n = Kn − ∑ Kn+s es = Kn − Kn+1 e1 − Kn+2 e2 − . . . − Kn+15 e15
s =1

respectively. The norms of nth Tribonacci and Tribonacci-Lucas sedenions are:
∥ ∥2
∥ ∥
∥ T̂n ∥ = N 2 ( T̂n ) = T̂n T̂n = T̂n T̂n = Tn2 + Tn2+1 + . . . + Tn2+15
and:

∥ ∥2
∥ ∥
∥K̂n ∥ = N 2 (K̂n ) = K̂n K̂n = K̂n K̂n = Kn2 + Kn2 +1 + . . . + Kn2 +15

respectively.
To calculate the norms of T̂n and K̂n , we need the following Lemma.

## PDF page 8

Mathematics 2019, 7, 74

8 of 19

Lemma 1 ([38]). The following formulas are valid:
n

∑ Ti2

=

1 + 4Tn Tn+1 − ( Tn+1 − Tn−1 )2
,
4

(10)

∑ Ki2

=

−Kn2 +1 − Kn2 −1 + K2n+3 + K2n−2
− 2.
2

(11)

i =1
n
i =1

We can now calculate the norms of T̂n and K̂n .
Theorem 1. The norms of nth Tribonacci and Tribonacci-Lucas sedenions are given as:
∥ ∥2
∥ ∥
∥ T̂n ∥

=

∥ ∥2
∥ ∥
∥K̂n ∥

=

4( Tn+15 Tn+16 − Tn−1 Tn ) + ( Tn − Tn−2 )2 − ( Tn+16 − Tn+14 )2
,
4
−Kn2 +16 − Kn2 +14 + Kn2 + Kn2 −2 + K2n+33 + K2n+28 − K2n+1 − K2n−4
.
2

Proof. We obtain the results from the following calculations:
∥ ∥2
∥ ∥
∥ T̂n ∥

=
=
=

n+15

n+15

n −1

i =n

i =1

i =1

∑ Ti2 = ∑ Ti2 − ∑ Ti2

1 + 4Tn−1 Tn − ( Tn − Tn−2 )2
1 + 4Tn+15 Tn+16 − ( Tn+16 − Tn+14 )2
−
4
4
4( Tn+15 Tn+16 − Tn−1 Tn ) + ( Tn − Tn−2 )2 − ( Tn+16 − Tn+14 )2
4

and:
∥ ∥2
∥ ∥
∥K̂n ∥

n+15

=

n+15

n −1

∑ Ki2 = ∑ Ki2 − ∑ Ki2

i =n

− 2)
2
−Kn2 − Kn2 −2 + K2n+1 + K2n−4
− 2)
−(
2
−Kn2 +16 − Kn2 +14 − K2n+1 − K2n−4 + K2n+33 + Kn2 + Kn2 −2 + K2n+28
.
2

= (

=

i =1
i =1
2
2
−Kn+16 − Kn+14 + K2n+33 + K2n+28

Now, we will state Binet’s formula for the Tribonacci and Tribonacci-Lucas sedenions, and in the
rest of the paper, we fixed the following notations.
15

α̂

=

∑ αs es ,

s =0
15

β̂

=

∑ βs es ,

s =0
15

γ̂

=

∑ γs es .

s =0

Theorem 2. For any integer n, the nth Tribonacci sedenion is:
T̂n =

α̂αn+1
β̂βn+1
γ̂γn+1
+
+
(α − β)(α − γ) ( β − α)( β − γ) (γ − α)(γ − β)

(12)

## PDF page 9

Mathematics 2019, 7, 74

9 of 19

and the nth Tribonacci-Lucas sedenion is:
K̂n = α̂αn + β̂βn + γ̂γn .

(13)

15
s
s
Proof. Repeated use of (4) in (6) enables us to write for α̂ = ∑15
s=0 α es , β̂ = ∑s=0 β es and
15
s
γ̂ = ∑s=0 γ es :

T̂n

=
=

15

15 (

s =0

s =0

∑ Tn+s es = ∑

α n +1+ s e s
β n +1+ s e s
γ n +1+ s e s
+
+
(α − β)(α − γ) ( β − α)( β − γ) (γ − α)(γ − β)

)

α̂αn+1
γ̂γn+1
β̂βn+1
+
+
.
(α − β)(α − γ) ( β − α)( β − γ) (γ − α)(γ − β)

Similarly, we can obtain (13).
The next theorem gives us an alternative proof of Binet’s formula for the Tribonacci and
Tribonacci-Lucas sedenions. For this, we need the quadratic approximation of { Tn }n≥0 and {Kn }n≥0 :
Lemma 2. For all integers n, we have:
(a)
ααn+2

= Tn+2 α2 + ( Tn+1 + Tn )α + Tn+1 ,

ββn+2

= Tn+2 β2 + ( Tn+1 + Tn ) β + Tn+1 ,

γγn+2

= Tn+2 γ2 + ( Tn+1 + Tn )γ + Tn+1 .

Pαn+2

= K n +2 α 2 + ( K n +1 + K n ) α + K n +1 ,

Qβn+2

= K n +2 β 2 + ( K n +1 + K n ) β + K n +1 ,

Rγn+2

= K n +2 γ 2 + ( K n +1 + K n ) γ + K n +1 ,

(b)

where
P

= 3 − ( β + γ) + 3βγ,

Q

= 3 − (α + γ) + 3αγ,

R

= 3 − (α + βγ) + 3αβ.

Proof. See [39] or [34].
Alternative proof of Theorem 2:
Note that:
α2 T̂n+2 + α( T̂n+1 + T̂n ) + T̂n+1

= α2 ( Tn+2 + Tn+3 e1 + . . . + Tn+17 e15 )
+α(( Tn+1 + Tn ) + ( Tn+2 + Tn+1 )e1 + . . . + ( Tn+16 + Tn+15 )e15 )
+( Tn+1 + Tn+2 e1 + . . . + Tn+16 e15 )
= α2 Tn+2 + α( Tn+1 + Tn ) + Tn+1 + (α2 Tn+3 + ( Tn+2 + Tn+1 ) + Tn+2 )e1
+(α2 Tn+4 + ( Tn+3 + Tn+2 ) + Tn+3 )e2
..
.
+(α2 Tn+17 + ( Tn+16 + Tn+15 ) + Tn+16 )e15 .

## PDF page 10

Mathematics 2019, 7, 74

10 of 19

From the identity αn+3 = Tn+2 α2 + ( Tn+1 + Tn )α + Tn+1 for the nth Tribonacci number Tn ,
we have:
α2 T̂n+2 + α( T̂n+1 + T̂n ) + T̂n+1 = α̂αn+3 .
(14)
Similarly, we obtain:
β2 T̂n+2 + β( T̂n+1 + T̂n ) + T̂n+1 = β̂βn+3

(15)

γ2 T̂n+2 + γ( T̂n+1 + T̂n ) + T̂n+1 = γ̂γn+3 .

(16)

and:
Subtracting (15) from (14), we have:

(α + β) T̂n+2 + ( T̂n+1 + T̂n ) =

α̂αn+3 − β̂βn+3
.
α−β

(17)

α̂αn+3 − γ̂γn+3
.
α−γ

(18)

Similarly, subtracting (16) from (14), we obtain:

(α + γ) T̂n+2 + ( T̂n+1 + T̂n ) =
Finally, subtracting (18) from (17), we get:
T̂n+2

(

α̂αn+3 − β̂βn+3
α̂αn+3 − γ̂γn+3
−
α−β
α−γ

)

=

1
α−β

=

α̂αn+3
β̂βn+3
γ̂γn+3
−
+
(α − β)(α − γ) (α − β)( β − γ) (γ − α)(γ − β)

=

β̂βn+3
γ̂γn+3
α̂αn+3
+
+
.
(α − β)(α − γ) ( β − α)( β − γ) (γ − α)(γ − β)

Therefore, this proves (12). Similarly, we obtain (13).
Next, we present generating functions.
Theorem 3. The generating functions for the Tribonacci and Tribonacci-Lucas sedenions are:
∞

g( x ) = ∑ T̂n x n =
n =0

and:

∞

g( x ) = ∑ K̂n x n =
n =0

T̂0 + ( T̂1 − T̂0 ) x + T̂−1 x2
1 − x − x2 − x3

(19)

K̂0 + (K̂1 − K̂0 ) x + K̂−1 x2
1 − x − x2 − x3

(20)

respectively.
n
Proof. Define g( x ) = ∑∞
n=0 T̂n x . Note that:

g( x )
xg( x )
x2 g( x )
x3 g( x )

= T̂0 + T̂1 x + T̂2 x2 + T̂3 x3 +
=
T̂0 x + T̂1 x2 + T̂2 x3 +
=
T̂0 x2 + T̂1 x3 +
=
T̂0 x3 +

T̂4 x4 +
T̂3 x4 +
T̂2 x4 +
T̂1 x4 +

T̂5 x5 + . . . +
T̂4 x5 + . . . +
T̂3 x5 + . . . +
T̂2 x5 + . . . +

T̂n x n + . . .
T̂n−1 x n + . . .
T̂n−2 x n + . . .
T̂n−3 x n + . . .

## PDF page 11

Mathematics 2019, 7, 74

11 of 19

Using the above table and the recurrence relation T̂n = T̂n−1 + T̂n−2 + T̂n−3 , we have:
g( x ) − xg( x ) − x2 g( x ) − x3 g( x )

= T̂0 + ( T̂1 − T̂0 ) x + ( T̂2 − T̂1 − T̂0 ) x2 + ( T̂3 − T̂2 − T̂1 − T̂0 ) x3 +
( T̂4 − T̂3 − T̂2 − T̂1 ) x4 + . . . + ( T̂n − T̂n−1 − T̂n−2 − T̂n−3 +) x n + . . .
= T̂0 + ( T̂1 − T̂0 ) x + ( T̂2 − T̂1 − T̂0 ) x2 .
It follows that:
g( x ) =

T̂0 + ( T̂1 − T̂0 ) x + ( T̂2 − T̂1 − T̂0 ) x2
.
1 − x − x2 − x3

Since T̂2 − T̂1 − T̂0 = T̂−1 , the generating function for the Tribonacci sedenion is:
g( x ) =

T̂0 + ( T̂1 − T̂0 ) x + T̂−1 x2
.
1 − x − x2 − x3

Similarly, we can obtain (20).
In the following theorem, we present another forms of Binet’s formulas for the Tribonacci and
Tribonacci-Lucas sedenions using generating functions.
Theorem 4. For any integer n, the nth Tribonacci sedenion is:
T̂n

=

((α2 − α) T̂0 + α T̂1 + T̂−1 )αn (( β2 − β) T̂0 + β T̂1 + T̂−1 ) βn
+
(α − γ) (α − β)
( β − γ) ( β − α)
+

((γ2 − γ) T̂0 + γ T̂1 + T̂−1 )γn
(γ − β) (γ − α)

and the nth Tribonacci-Lucas sedenion is:
K̂n

=

((α2 − α)K̂0 + αK̂1 + K̂−1 )αn (( β2 − β)K̂0 + βK̂1 + K̂−1 ) βn
+
(α − γ) (α − β)
( β − γ) ( β − α)
+

((γ2 − γ)K̂0 + γK̂1 + K̂−1 )γn
.
(γ − β) (γ − α)

Proof. We can use generating functions. Since the roots of the equation 1 − x − x2 − x3 = 0 are
αβ, βγ, αγ and:
1 − x − x2 − x3 = (1 − αx )(1 − βx )(1 − γx )
we can write the generating function of T̂n as:
T̂0 + ( T̂1 − T̂0 ) x + T̂−1 x2
T̂0 + ( T̂1 − T̂0 ) x + T̂−1 x2
=
(1 − αx )(1 − βx )(1 − γx )
1 − x − x2 − x3
A
B
C
+
+
(1 − αx ) (1 − βx ) (1 − γx )
A(1 − βx )(1 − γx ) + B(1 − αx )(1 − γx ) + C (1 − αx )(1 − βx )
(1 − αx )(1 − βx )(1 − γx )

g( x ) =

=
=
=

( A + B + C ) + (− Aβ − Aγ − Bα − Bγ − Cα − Cβ) x + ( Aβγ + Bαγ + Cαβ) x2
.
(1 − αx )(1 − βx )(1 − γx )

## PDF page 12

Mathematics 2019, 7, 74

12 of 19

We need to find A, B, and C, so the following system of equations should be solved:
A+B+C

= T̂0

− Aβ − Aγ − Bα − Bγ − Cα − Cβ = T̂1 − T̂0
Aβγ + Bαγ + Cαβ

= T̂−1

We find that:
A

=

((α2 − α) T̂0 + α T̂1 + T̂−1 )
−α T̂0 + α T̂1 + T̂−1 + α2 T̂0
=
,
(α − γ) (α − β)
α2 − αβ − αγ + βγ

B

=

(( β2 − β) T̂0 + β T̂1 + T̂−1 )
− β T̂0 + β T̂1 + T̂−1 + β2 T̂0
=
,
2
( β − γ) ( β − α)
β − αβ + αγ − βγ

C

=

−γ T̂0 + γ T̂1 + T̂−1 + γ2 T̂0
((γ2 − γ) T̂0 + γ T̂1 + T̂−1 )
=
.
(γ − β) (γ − α)
γ2 + αβ − αγ − βγ

and:
g( x )

=

((α2 − α) T̂0 + α T̂1 + T̂−1 ) ∞ n n (( β2 − β) T̂0 + β T̂1 + T̂−1 ) ∞ n n
∑α x +
∑β x
(α − γ) (α − β)
( β − γ) ( β − α)
n =0
n =0

(−γ T̂0 + γ T̂1 + T̂−1 + γ2 T̂0 ) ∞ n n
∑γ x
(γ − β) (γ − α)
n =0
⎛
⎞
(( β2 − β) T̂0 + β T̂1 + T̂−1 ) βn
((α2 −α) T̂0 +α T̂1 + T̂−1 )αn
∞
+
(α−γ)(α− β)
( β−γ)( β−α)
⎠ xn .
= ∑⎝
((γ2 −γ) T̂0 +γ T̂1 + T̂−1 )γn
+
n =0
(γ− β)(γ−α)
+

Thus, Binet’s formula of the Tribonacci sedenion is:
T̂n

=

((α2 − α) T̂0 + α T̂1 + T̂−1 )αn (( β2 − β) T̂0 + β T̂1 + T̂−1 ) βn
+
(α − γ) (α − β)
( β − γ) ( β − α)
+

((γ2 − γ) T̂0 + γ T̂1 + T̂−1 )γn
.
(γ − β) (γ − α)

Similarly, we can obtain Binet’s formula of the Tribonacci-Lucas sedenion.
If we compare Theorem 2 and Theorem 4 and use the definition of T̂n , K̂n , we have the following
remark showing relations between T̂−1 , T̂0 , T̂1 ; K̂−1 , K̂0 , K̂1 and α̂, β̂, γ̂. We obtain (b) and (d) after
solving the system of equations in (a) and (c), respectively.
Remark 1. We have the following identities:
(a)

(α2 − α) T̂0 + α T̂1 + T̂−1
α
( β2 − β) T̂0 + β T̂1 + T̂−1
β
(γ2 − γ) T̂0 + γ T̂1 + T̂−1
γ

= α̂
=

β̂

= γ̂

## PDF page 13

Mathematics 2019, 7, 74

13 of 19

(b)
15

∑ T−1+s es

= T̂−1 =

s =0

15

α̂
γ̂
β̂
+
+
(α − β)(α − γ) ( β − α)( β − γ) (γ − α)(γ − β)

∑ Ts es

= T̂0 =

β̂β
γ̂γ
α̂α
+
+
(α − β)(α − γ) ( β − α)( β − γ) (γ − α)(γ − β)

∑ T1+s es

= T̂1 =

γ̂γ2
β̂β2
α̂α2
+
+
(α − β)(α − γ) ( β − α)( β − γ) (γ − α)(γ − β)

s =0
15

s =0

(c)

((α2 − α)K̂0 + αK̂1 + K̂−1 )
(α − γ) (α − β)

= α̂

(( β2 − β)K̂0 + βK̂1 + K̂−1 )
( β − γ) ( β − α)

=

((γ2 − γ)K̂0 + γK̂1 + K̂−1 )
(γ − β) (γ − α)

= γ̂

β̂

(d)
15

∑ K −1+ s e s

= K̂−1 = α̂α−1 + β̂β−1 + γ̂γ−1

s =0

15

∑ Ks es

= K̂0 = α̂ + β̂ + γ̂

s =0
15

∑ K1+ s e s

= K̂1 = α̂α + β̂β + γ̂γ.

s =0

Using the above remark, we can find T̂2 , K̂2 as follows:
15

β̂β3

α̂α3

γ̂γ3

∑ T2+s es = T̂2 = T̂1 + T̂0 + T̂−1 = (α − β)(α − γ) + ( β − α)( β − γ) + (γ − α)(γ − β)

(21)

s =0

and:

15

∑ K2+s es = K̂2 = K̂1 + K̂0 + K̂−1 = α̂α2 + β̂β2 + γ̂γ2 .

(22)

s =0

Of course, (21) and (22) can be found directly from (12) and (13).
Now, we present the formulas, which give the summation of the first n Tribonacci and
Tribonacci-Lucas numbers.
Lemma 3. For every integer n ≥ 0, we have:
n

1

1

∑ Ti = T0 + 2 (Tn+2 + Tn − 1) = 2 (Tn+2 + Tn − 1)

(23)

i =0

and:

n

∑ Ki =

i =0

K n +2 + K n
.
2

(24)

Proof. (23) and (24) can be easily proven by mathematical induction. For a proof of (23) with a
telescopic sum method, see [40], or with a matrix diagonalization proof, see [41], or see also [30].

## PDF page 14

Mathematics 2019, 7, 74

14 of 19

n

For a proof of (24), see [42]. Since K0 = 3 and ∑ Ki =
i =1

n

K n +2 + K n
.
∑ Ki =
2
i =0

K n +2 + K n − 6
, it follows that
2

There is also a formula of the summation of the first n negative Tribonacci numbers:
n

1

∑ T−i = 2 (1 − T−n−1 − T−n+1 ).

i =1

For a proof of the above formula, see Kuhapatanakul and Sukruan [43].
Next, we present the formulas that give the summation of the first n Tribonacci and
Tribonacci-Lucas sedenions.
Theorem 5. The summation formulas for Tribonacci and Tribonacci-Lucas sedenions are
n

1

∑ T̂i = 2 (T̂n+2 + T̂n + c1 )

(25)

i =0

and:

n

1

∑ K̂i = 2 (K̂n+2 + K̂n + c2 )

(26)

i =0

respectively, where:
c1

= −1 − e1 − 3e2 − 5e3 − 9e4 − 17e5 − 31e6 − 57e7 − 105e8 − 193e9
−355e10 − 653e11 − 1201e12 − 2209e13 − 4063e14 − 7473e15

and:
c2

= −6e1 − 8e2 − 14e3 − 28e4 − 50e5 − 92e6 − 170e7 − 312e8 − 574e9
−1056e10 − 1842e11 − 3572e12 − 6570e13 − 12084e14 − 22226e15 .

Proof. Using (6) and (23), we obtain:
n

∑ T̂i

i =0

=

n

n

n

n

i =0

i =0

i =0

i =0

∑ Ti + e1 ∑ Ti+1 + e2 ∑ Ti+2 + . . . + e15 ∑ Ti+15

= ( T0 + . . . + Tn ) + e1 ( T1 + . . . + Tn+1 )
+e2 ( T2 + . . . + Tn+2 ) + . . . + e15 ( T15 + . . . + Tn+15 ).
and:
n

2 ∑ T̂i

= ( Tn+2 + Tn − 1) + e1 ( Tn+3 + Tn+1 − 1 − 2T0 )

i =0

+e2 ( Tn+4 + Tn+3 − 1 − 2( T0 + T1 ))
..
.
+e15 ( Tn+17 + Tn+15 − 1 − 2( T0 + T1 + . . . + T14 ))
= T̂n+2 + T̂n + c1
where c1 = −1 + e1 (−1 − 2T0 ) + e2 (−1 − 2( T0 + T1 )) + . . . + e15 (−1 − 2( T0 + . . . + T14 )). Hence:
n

1

∑ T̂i = 2 (T̂n+2 + T̂n + c1 ).

i =0

## PDF page 15

Mathematics 2019, 7, 74

15 of 19

We can compute c1 as:
c1

= −1 − e1 − 3e2 − 5e3 − 9e4 − 17e5 − 31e6 − 57e7 − 105e8 − 193e9
−355e10 − 653e11 − 1201e12 − 2209e13 − 4063e14 − 7473e15 .

This proves (25). Similarly, we can obtain (26).
3. Some Identities for the Tribonacci and Tribonacci-Lucas Sedenions
In this section, we give identities about Tribonacci and Tribonacci-Lucas sedenions.
Theorem 6. For n ≥ 1, the following identities hold:
(a) K̂n = 3T̂n+1 − 2T̂n − T̂n−1 ,
(b) T̂n + T̂n = 2Tn , K̂n + K̂n = 2Kn ,
γ̂ (γ + 1) γn+1
α̂ (α + 1) αn+1
β̂ ( β + 1) βn+1
+
+
,
(c) T̂n+1 + T̂n =
(α − β)(α − γ) ( β − α)( β − γ) (γ − α)(γ − β)
n
n
n
(d) K̂n+1 + K̂n = α̂ (α + 1) α + β̂ ( β + 1) β + γ̂ (γ + 1) γ ,
n
α̂α(1 + α)n
γ̂γ(1 + γ)n
β̂β(1 + β)n
(e) ∑ (ni) F̂i =
+
+
,
(α − β)(α − γ) ( β − α)( β − γ) (γ − α)(γ − β)
i =0
n

(f) ∑ (ni)K̂i = α̂(1 + α)n + β̂(1 + β)n + γ̂(1 + γ)n .
i =0

Proof. (a) follows from the recurrence relation Kn = 3Tn+1 − 2Tn − Tn−1 (see for example [39]).
The others can be easily established.
Theorem 7. For n ≥ 0, m ≥ 3, we have:
(a) T̂m+n = Tm−1 T̂n+2 + ( Tm−2 + Tm−3 ) T̂n+1 + Tm−2 T̂n ,
(b) T̂m+n = Tm+2 T̂n−1 + ( Tm+1 + Tm ) T̂n−2 + Tm+1 T̂n−3 ,
(c) K̂m+n = Kn−1 T̂m+2 + ( T̂m+1 + T̂m )Kn−2 + Kn−3 T̂m+1 ,
(d) K̂m+n = Km+2 T̂n−1 + (Km+1 + Km ) T̂n−2 + Km+1 T̂n−3 .
Proof. (a) and (d) can be proven by strong induction on m, and (c) can be proven by strong induction
on n. For (b), replace n by n − 3 and m by m + 3 in (a).
Note that in fact, the results of the above theorem are true for all integers n and m, and taking
n = 2 in (c), we obtain:
K̂m+2 = T̂m+2 + 2T̂m+1 + 3T̂m
and taking m = −4 in (d):
K̂n−4 = − T̂n−1 + 5T̂n−3 .
Note also that since, for all integers n, T−n = 2T−n+3 − T−n+4 , it follows that:
T̂−n = 2T̂−n+3 − T̂−n+4 .
Theorem 8. For all integers n, the following identities hold:
(a) T̂n+6 = 7T̂n+3 − 5T̂n + T̂n−3
(b) T̂n+8 = 11T̂n+4 + 5T̂n + T̂n−4
(c) T̂n+10 = 21T̂n+5 + T̂n + T̂n−5
(d) K̂n+6 = 2K̂n+3 + K̂n + K̂n−3
(e) K̂n+8 = 4K̂n+4 + K̂n−4
(f) K̂n+10 = 7K̂n+5 − 2K̂n + K̂n−5 .
Proof. For all integers n and m, we have Tn+2m = Km Tn+m − K−m Tn + Tn−m and Kn+2m = Tm Kn+m −
T−m Kn + Kn−m (see [44]). Giving some value for m, we obtain the results.

## PDF page 16

Mathematics 2019, 7, 74

16 of 19

4. Matrices and Determinants Related to Tribonacci and Tribonacci-Lucas Sedenions
Define the 4 × 4 determinants Dn and En , for all integers n, by:
∣
∣ Tn
∣
∣ T
∣
Dn = ∣ 2
∣ T1
∣
∣ T0

Kn
K2
K1
K0

K n +1
K3
K2
K1

∣
∣
∣ Kn
Kn+2 ∣∣
∣
∣ K
∣
K4 ∣
∣ 2
∣ , En = ∣
∣ K1
K3 ∣
∣
∣
∣ K0
K2 ∣

Tn
T2
T1
T0

Tn+1
T3
T2
T1

∣
Tn+2 ∣∣
T4 ∣∣
∣
T3 ∣
∣
T2 ∣

Theorem 9. The following statements are true.
(a) Dn = 0 and En = 0 for all integers n.
(b) 44T̂n = 10K̂n+2 − 6K̂n+1 − 8K̂n .
(c) K̂n = − T̂n+2 + 4T̂n+1 − T̂n .
Proof. (a) is a special case of a result in [45]. Expanding Dn along the top row gives 44Tn = 10Kn+2 −
6Kn+1 − 8Kn , and now, (b) follows. Expanding En along the top row gives Kn = − Tn+2 + 4Tn+1 − Tn ,
and now, (c) follows.
Consider the sequence {Un }, which is defined by the third-order recurrence relation:
Un = Un−1 + Un−2 + Un−3 ,

U0 = U1 = 0, U2 = 1.

Note that some authors call {Un } a Tribonacci sequence instead of { Tn }. The numbers Un can be
expressed using Binet’s formula:
Un =

αn
βn
γn
+
+
(α − β)(α − γ) ( β − α)( β − γ) (γ − α)(γ − β)

and the negative numbers U−n (n = 1, 2, 3, . . .) satisfy the recurrence relation:
∣
∣ U
∣
U−n = ∣ n+1
∣ Un

∣
Un+2 ∣∣
∣ = Un2+1 − Un+2 Un .
Un+1 ∣

The matrix method is a very useful method in order to obtain some identities for special sequences.
We define the square matrix M of order three as:
⎛

1
⎜
M=⎝ 1
0

1
0
1

⎞
1
⎟
0 ⎠
0

such that det M = 1. Note that:
⎛

Un+2
⎜
n
M = ⎝ Un+1
Un

Un+1 + Un
Un + Un−1
Un−1 + Un−2

⎞
Un+1
⎟
Un ⎠ .
Un−1

For a proof of (27), see [46]. Matrix formulation of Tn and Kn can be given as:
⎛
⎞ ⎛
⎞n ⎛
⎞
Tn+2
1 1 1
T2
⎜
⎟ ⎜
⎟ ⎜
⎟
⎝ Tn+1 ⎠ = ⎝ 1 0 0 ⎠ ⎝ T1 ⎠
Tn
0 1 0
T0

(27)

(28)

## PDF page 17

Mathematics 2019, 7, 74

17 of 19

and:

⎞ ⎛
1
K n +2
⎟ ⎜
⎜
⎝ K n +1 ⎠ = ⎝ 1
Kn
0
⎛

1
0
1

⎞
⎞n ⎛
1
K2
⎟
⎟ ⎜
0 ⎠ ⎝ K1 ⎠ .
K0
0

(29)

The matrix M was defined and used in [47]. For the matrix formulations (28) and (29), see [48,49].
Now, we define the matrices MT and MK as:
⎛
⎞
⎛
⎞
T̂4 T̂3 + T̂2 T̂3
K̂4 K̂3 + K̂2 K̂3
⎟
⎜
⎟
⎜
MT = ⎝ T̂3 T̂2 + T̂1 T̂2 ⎠ and MK = ⎝ K̂3 K̂2 + K̂1 K̂2 ⎠ .
T̂2 T̂1 + T̂0 T̂1
K̂2 K̂1 + K̂0 K̂1
These matrices MT and MK can be called the Tribonacci sedenion matrix and Tribonacci-Lucas
sedenion matrix, respectively.
Theorem 10. For n ≥ 0, the following are valid:
(a)
1
⎜
MT ⎝ 1
0

1
0
1

⎞n ⎛
1
T̂n+4
⎟
⎜
0 ⎠ = ⎝ T̂n+3
0
T̂n+2

T̂n+3 + T̂n+2
T̂n+2 + T̂n+1
T̂n+1 + T̂n

⎞
T̂n+3
⎟
T̂n+2 ⎠
T̂n+1

(30)

⎛

1
0
1

⎞n ⎛
1
K̂n+4
⎟
⎜
0 ⎠ = ⎝ K̂n+3
0
K̂n+2

K̂n+3 + K̂n+2
K̂n+2 + K̂n+1
K̂n+1 + K̂n

⎞
K̂n+3
⎟
K̂n+2 ⎠
K̂n+1

(31)

⎛

(b)
1
⎜
MK ⎝ 1
0

Proof. We prove (a) by mathematical induction on n. If n = 0, then the result is clear. Now, we assume
it is true for n = k, that is:
⎛
⎞
T̂k+4 T̂k+3 + T̂k+2 T̂k+3
⎜
⎟
MT Mk = ⎝ T̂k+3 T̂k+2 + T̂k+1 T̂k+2 ⎠ .
T̂k+2
T̂k+1 + T̂k
T̂k+1
If we use (8), then for k ≥ 3, we have T̂k+3 = T̂k+2 + T̂k+1 + T̂k . Then, by induction hypothesis,
we obtain:
M T M k +1

= ( MT M k ) M
⎛
T̂k+4 T̂k+3 + T̂k+2
⎜
= ⎝ T̂k+3 T̂k+2 + T̂k+1
T̂k+2
T̂k+1 + T̂k
⎛
T̂k+2 + T̂k+3 + T̂k+4
⎜
= ⎝ T̂k+1 + T̂k+2 + T̂k+3
T̂k+1 + T̂k+2 + T̂k
⎛
T̂k+5 T̂k+4 + T̂k+3
⎜
= ⎝ T̂k+4 T̂k+3 + T̂k+2
T̂k+3 T̂k+2 + T̂k+1

Thus, (30) holds for all non-negative integers n.
(31) can be similarly proven.
Corollary 1. For n ≥ 0, the following hold:

⎞⎛
T̂k+3
1
⎟⎜
T̂k+2 ⎠ ⎝ 1
T̂k+1
0

1
0
1

⎞
1
⎟
0 ⎠
0
⎞

T̂k+4 + T̂k+3
T̂k+3 + T̂k+2
T̂k+2 + T̂k+1
⎞
T̂k+4
⎟
T̂k+3 ⎠ .
T̂k+2

T̂k+4
⎟
T̂k+3 ⎠
T̂k+2

## PDF page 18

Mathematics 2019, 7, 74

18 of 19

(a) T̂n+2 = T̂2 Un+2 + ( T̂1 + T̂0 )Un+1 + T̂1 Un
(b) K̂n+2 = K̂2 Un+2 + (K̂1 + K̂0 )Un+1 + K̂1 Un
Proof. The proof of (a) can be seen by the coefficient (28) of the matrix MT and (27). The proof of (b)
can be seen by the coefficient (29) of the matrix MK and (27).
Note that we have similar results if we replace the matrix M with the matrices N and O defined by:
⎛

1
⎜
N=⎝ 1
1

1
0
0

⎞
⎛
0
0
⎟
⎜
1 ⎠ and O = ⎝ 0
0
1

1
0
1

⎞
0
⎟
1 ⎠.
1

Funding: This research received no external funding.
Acknowledgments: We are thankful to the referees for their careful reading of the manuscript and for valuable
comments and suggestions that greatly improved the presentation of this work.
Conflicts of Interest: The author declares no conflict of interest.

References
1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.

Feinberg, M. Fibonacci–Tribonacci. Fibonacci Q. 1963, 1, 71–74.
Bruce, I. A modified Tribonacci sequence. Fibonacci Q. 1984, 22, 244–246.
Catalani, M. Identities for Tribonacci-related sequences. arXiv 2002, arXiv:math/0209179.
Choi, E. Modular tribonacci Numbers by Matrix Method. J. Korean Soc. Math. Educ. Ser. B Pure Appl. Math.
2013, 20, 207–221. [CrossRef]
Elia, M. Derived Sequences, The Tribonacci Recurrence and Cubic Forms. Fibonacci Q. 2001, 39, 107–115.
Lin, P.Y. De Moivre-Type Identities For The Tribonacci Numbers. Fibonacci Q. 1988, 26, 131–134.
Pethe, S. Some Identities for Tribonacci sequences. Fibonacci Q. 1988, 26, 144–151.
Scott, A.; Delaney, T.; Hoggatt, V., Jr. The Tribonacci sequence. Fibonacci Q. 1977, 15, 193–200.
Shannon, A. Tribonacci numbers and Pascal’s pyramid. Fibonacci Q. 1977, 15, 268–275.
Spickerman, W.; Joyner, R.N. Binets’s formula for the Recursive sequence of Order K. Fibonacci Q. 1984, 22,
327–331.
Yalavigi, C.C. Properties of Tribonacci numbers. Fibonacci Q. 1972, 10, 231–246.
Yilmaz, N.; Taskara, N. Tribonacci and Tribonacci-Lucas Numbers via the Determinants of Special Matrices.
Appl. Math. Sci. 2014, 8, 1947–1955. [CrossRef]
Spickerman, W. Binet’s formula for the Tribonacci sequence. Fibonacci Q. 1982, 20, 118–120.
Biss, D.K.; Dugger, D.; Isaksen, D.C. Large annihilators in Cayley-Dickson algebras. Commun. Algebra 2008,
36, 632–664. [CrossRef]
Imaeda, K.; Imaeda, M. Sedenions: Algebra and analysis. Appl. Math. Comput. 2000, 115, 77–88. [CrossRef]
Moreno, G. The zero divisors of the Cayley-Dickson algebras over the real numbers. Bol. Soc. Mat. Mexicana
1998, 4, 13–28.
Bilgici, G.; Tokeşer, Ü.; Ünal, Z. Fibonacci and Lucas Sedenions. J. Integer Seq. 2017, 20, 17.1.8, 11p.
Cawagas, E.R. On the Structure and Zero Divisors of the Cayley-Dickson Sedenion Algebra, Discussiones
Mathematicae. Gen. Algebra Appl. 2004, 24, 251–265.
Cariow, A.; Cariowa, G. An Algorithm for Fast Multiplication of Sedenios. Inf. Proccess. Lett. 2013, 113,
324–331. [CrossRef]
Makarov, O.M. An algorithm for the multiplication of two quaternions. USSR Comput. Math. Math. Phys.
1978, 17, 221–222. [CrossRef]
Cariow, A.; Cariowa, G. Algorithm for Multiplying Two Octonions, Radioelectronics and Communications Systems;
Allerton Press, Inc.: New York, NY, USA, 2012; Volume 55, pp. 464–473.
Köplinger, J. Signature of gravity in conic sedenions. Appl. Math. Comput. 2007, 188, 942–947. [CrossRef]
Köplinger, J. Gravity and eletromagnetism an conic sedenions. Appl. Math. Comput. 2007, 188, 948–953.

## PDF page 19

Mathematics 2019, 7, 74

24.
25.
26.
27.
28.
29.
30.
31.
32.
33.
34.
35.
36.
37.
38.
39.
40.
41.
42.
43.
44.
45.
46.
47.
48.
49.

19 of 19

Muses, C.A. Hypernumber and quantum field theory with a summary of physically applicable hypernumber
arithmetics and their geometrics. Appl. Math. Comput. 1980, 6, 63–94.
Baez, J. The octonions. Bull. Am. Math. Soc. 2002, 39, 145–205. [CrossRef]
Okubo, S. Introduction to Octonions and Other Non-Associative Algebras in Physics; Cambridge University Press:
Cambridge, UK, 1995.
Horadam, A.F. Complex Fibonacci Numbers and Fibonacci quaternions. Am. Math. Mon. 1963, 70, 289–291.
[CrossRef]
Halici, S.; Karataş, A. On a Generalization for Fibonacci Quaternions. Chaos Solitons Fractals 2017, 98, 178–182.
[CrossRef]
Polatlı, E. A Generalization of Fibonacci and Lucas Quaternions. Adv. Appl. Clifford Algebras 2016, 26,
719–730. [CrossRef]
Cerda-Morales, G. On a Generalization for Tribonacci Quaternions. Mediterr. J. Math. 2017, 14, 1–12.
[CrossRef]
Keçilioglu, O.; Akkuş, I. The Fibonacci Octonions. Adv. Appl. Clifford Algebr 2015, 25, 151–158. [CrossRef]
Çimen, C.; İpek, A. On Jacobsthal and Jacobsthal-Lucas Octonions. Mediterr. J. Math. 2017, 14, 1–13.
[CrossRef]
Cerda-Morales, G. The Third Order Jacobsthal Octonions: Some Combinatorial Properties. arXiv 2017,
arXiv:1710.00602v1.
Cerda-Morales, G. The Unifying Formula for All Tribonacci-Type Octonions Sequences and Their Properties.
arXiv 2018, arXiv:1807.04140v1.
Catarino, P. k-Pell, k-Pell-Lucas and modified k-Pell sedenions. Asian-Eur. J. Math. 2018. S1793557119500189.
[CrossRef]
Çimen, C.; İpek, A. On Jacobsthal and Jacobsthal-Lucas Sedenios and Several Identities Involving These
Numbers. Math. Aeterna 2017, 7, 447–454.
Gül, K. On k-Fibonacci and k-Lucas Trigintaduonions. Int. J. Contemp. Math. Sci. 2018, 13, 1–10. [CrossRef]
Li, J.; Jiang, Z.; Lu, F. Determinants, Norms and Spread of Circulant Matrices with Tribonacci and Generalized
Lucas Numbers. Abstr. Appl. Anal. 2014, 2014, 381829. [CrossRef]
Cerda-Morales, G. A Three-By-Three Matrix Representation of a Generalized Tribonacci sequence. arXiv 2018,
arXiv:1807.03340v1.
Devbhadra, S.V. Some Tribonacci Identities. Math. Today 2011, 27, 1–9.
Kılıç, E. Tribonacci Sequences with Certain Indices and Their Sums. Ars. Comb. 2008, 86, 13–22.
Frontczak, R. Sums of Tribonacci and Tribonacci-Lucas Numbers. Int. J. Math. Anal. 2018, 12, 19–24. [CrossRef]
Kuhapatanakul, K.; Sukruan, L. The Generalized Tribonacci Numbers With Negative Subscripts. Integer
2014, 14, 1–6.
Howard, F.T. A Tribonacci Identity. Fibonacci Q. 2001, 39, 352–357.
Melham, R.S.; Shannon, A.G. A Generalization of a Result of D’Ocagne. Fibonacci Q. 1995, 33, 135–138.
Basu, M.; Das, M. Tribonacci Matrices and a New Coding Theory, Discrete Mathematics. Algorithms Appl.
2014, 6, 1450008.
Shannon, A.G.; Horadam, A.F. Some Properties of Third-Order Recurrence Relations. Fibonacci Q. 1972, 10,
135–146.
Yalavigi, C.C. A Note on ‘Another Generalized Fibonacci Sequence’. Math. Stud. 1971, 39, 407–408.
Waddill, M.E. Using Matrix Techniques to Establish Properties of a Generalized Tribonacci Sequence.
In Applications of Fibonacci Numbers; Bergum, G.E., Philippou, A.N., Horadam, A.F., Eds.; Kluwer Academic
Publishers: Dordrecht, The Netherlands, 1991; Volume 4, pp. 299–308.
c 2019 by the author. Licensee MDPI, Basel, Switzerland. This article is an open access
⃝
article distributed under the terms and conditions of the Creative Commons Attribution
(CC BY) license (http://creativecommons.org/licenses/by/4.0/).
