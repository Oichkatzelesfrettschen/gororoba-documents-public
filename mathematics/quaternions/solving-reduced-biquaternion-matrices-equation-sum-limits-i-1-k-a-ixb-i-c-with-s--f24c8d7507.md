Source: https://doi.org/10.3934/math.2022181
PDF sha256: f24c8d75079574c623da6857de15fd4e795fc565e869b51b830089c358774179
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of solving-reduced-biquaternion-matrices-equation-sum-limits-i-1-k-a-ixb-i-c-with-s--f24c8d7507.pdf

Transcription of `solving-reduced-biquaternion-matrices-equation-sum-limits-i-1-k-a-ixb-i-c-with-s--f24c8d7507.pdf` in this directory, 19 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-19 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

AIMS Mathematics, 7(3): 3258–3276.
DOI: 10.3934/math.2022181
Received: 18 September 2021
Accepted: 22 November 2021
Published: 29 November 2021

http://www.aimspress.com/journal/Math

Research article

Solving reduced biquaternion matrices equation

k
∑
i=1

Ai XBi = C with special

structure based on semi-tensor product of matrices
Wenxv Ding1,2 , Ying Li1,2, * , Anli Wei1,2 and Zhihong Liu1,2
1

College of Mathematical Sciences, Liaocheng University, Liaocheng 252000, China

2

Research Center of Semi-tensor Product of Matrices: Theory and Applications, Liaocheng 252000,
China

* Correspondence: Email: liyingld@163.com; Tel: 8618865209166.
Abstract: In this paper, we propose a real vector representation of reduced quaternion matrix and
study its properties. By using this real vector representation, Moore-Penrose inverse, and semi-tensor
product of matrices, we study some kinds of solutions of reduced biquaternion matrix equation (1.1).
Several numerical examples show that the proposed algorithm is feasible at last.
Keywords: semi-tensor product of matrices; reduced biquaternion; matrix equation; real vector
representation
Mathematics Subject Classification: 15A06

1. Introduction
Throughout this paper, the following notations are used. R, RBQ represent the set of real number
and reduced biquaternion, respctively. Rt (Rt ) represent the set of all real column(row) vectors with
order t. Rm×n , RBm×n
represent the set of all m × n real matrices, reduced biquaternion matrices,
Q
n×n
respectively. RBHQ , RBn×n
AQ represent the set of all n × n Hermitian reduced biquaternion matrices and
Anti-Hermitian reduced biquaternion matrices, respectively. Ik represents the unit matrix with order
k, δik represents the ith column of unit matrix Ik . δk [i1 , · · · , i s ] is a abbreviation of [δik1 , · · · , δiks ].
m×n
A = A1 + A2 i + A3 j + A4 k ∈ RBm×n
, (i = 1 : 4) and define A = A1 − A2 i − A3 j − A4 k
Q , where Ai ∈ R
T
H
†
to be conjugate of A. A , A , A represent the transpose, conjugate transpose, Moore-Penrose(MP)
inverse of matrix A. ⊗ represents the Kronecker product of matrices. ⋉ represents the semi-tensor
product of matrices. ∥·∥ represents the Frobenius norm of a matrix or Euclidean norm of a vector.
The concept of quaternion was proposed by Hamilton in 1843, which is an extension of complex

## PDF page 2

3259

number. It consists of four parts, i.e.
a = ar + ai i + a j j + ak k,
where ar , ai , a j , ak are real numbers and i, j, k satisfy
i2 = j2 = k2 = −1, ij = −ji = k, jk = −kj = i, ki = −ik = j.
As can be seen from the product rule above, quaternion is not commutative with respect to
multiplication. Owing to this reason, quaternion becomes more complicated in some operations, and
it will have great trouble in application to practical problems. This also promotes the generation of
reduced biquaternion to some extent. Reduced biquaternion is similar to quaternion in form, but it has
a different product rule.
Definition of reduced biquaternion [1]
a = ar + ai i + a j j + ak k,
where ar , ai , a j , ak are real numbers and
i2 = k2 = −1, j2 = 1, ij = ji = k, jk = kj = i, ki = ik = −j.
e1 = 1+2 j , e2 = 1−2 j are two special numbers in reduced biquaternion. Obviously,
en1 = en−1
= . . . = e1 , en2 = en−1
= . . . = e2 , e1 e2 = 0.
1
2
Therefore, e1 and e2 are both idempotent elements and divisors of zero. Any reduced biquaternion with
the form k1 e1 or k2 e2 is also a divisor of zero and does not have a multiplicative inverse, where, k1 , k2 are
arbitrary complex numbers. By means of e1 and e2 , we can uniquely express the reduced biquaternion
a = ar + ai i + a j j + ak k as a = a1 e1 + a2 e2 , where a1 = (ar + a j ) + (ai + ak )i, a2 = (ar − a j ) + (ai − ak )i.
The conjugate of a reduced biquaternion a is denoted by a and a = ar − ai i − a j j − ak k. The norm
of a reduced biquaternion a is
√
∥a∥ =

a2r + a2i + a2j + a2k .

Then, the Frobenius norm of A ∈ RBm×n
is defined as follows
Q
∥A∥ =

‾
⎷ m n
∑∑

∥ai j ∥2 .

i=1 j=1

The concept of reduced biquaternion was first defined by Schütte and Wenzel in 1990 [2]. It can be
seen that the product of reduced biquaternions has commutability compared with quaternion. Thus,
many operations of reduced biquaternion are simpler than those of quaternion. Such as, the
implementations of the discrete reduced biquaternion Fourier transform, convolution, correlation.
Therefore, it is of importance to study the theoretical knowledge and numerical calculation of reduced
biquaternions. Many good results on reduced biquaternions have obtained. For example, Pei et al.
investigated digital signal and image processing using reduced biquaternion in 2004 [1] and gave the
algorithms for calculating the eigenvalues, the eigenvectors, and the singular value decomposition of a
AIMS Mathematics

Volume 7, Issue 3, 3258–3276.

## PDF page 3

3260

reduced biquaternion matrix in 2008 [3]; Isokawa et al. studied two types of multistate Hopfield
neural networks using reduced biquaternion in 2010 [4]. At the same time, scholars also focused on
the solution of specific reduced biquaternion matrix equations because matrix equations have a wide
range of applications in control theory, stability and other fields. Hidayet derived the expressions of
the minimal norm least squares solution for the reduced biquaternion matrix equation AX = B using
the e1 − e2 form in 2019 [5]; Yuan studied the Hermitian solutions of the reduced biquaternion matrix
equation (AXB, CXD) = (E, F) using complex representation [6].
In this paper, we study the least squares problems of the reduced biquaternion matrix equation
k
∑

Ai XBi = C.

(1.1)

i=1

Since Hermitian and Anti-Hermitian matrices are very useful in engineering problems and linear
system theory. So many researchers turn on the problems of (Anti)-Hermitian matrix equations, for
example, [7, 8] derived explicit determinantal representation formulas of the general, Hermitian, and
Anti-Hermitian solutions to the system of two-sided quaternion matrix equations A1 XA∗1 = C1 and
A2 XA∗2 = C2 in 2018 and the Sylvester type matrix equation AXA∗ + BY B∗ = C in 2019 using
determinantal representations of Moore-Penrose inverse, respectively. [9] proposed a recursive
algorithm for calculating the inversion of the confluent Vandermonde matrix that with consecutive
powers devoted just to the Hermite type interpolation and derived an explicit analytic formula for the
calculation of the inverse of the confluent Vandermonde matrix in 2013. [10] considered the
quaternion matrix equation X − AX̂B = C and studied its minimal norm least squares solution,
j-self-conjugate least squares solution and anti- j-self-conjugate least squares solution by means of
real representation matrices of quaternion matrix in 2020.
We determine our research objective as the least squares Hermitian solution and the least squares
Anti-Hermitian solution as follows:
p×q
m×q
Problem 1. Let Ai ∈ RBm×n
Q , Bi ∈ RBQ , C ∈ RBQ , and


k


∑




n×p
SQ = 
X|X
∈
RB
,
A
XB
=
C
.

i
i
Q




i=1

Find out XQ ∈ S Q such that
∥∥ ∥∥
∥XQ ∥ = min ∥X∥ .
X∈S Q

n×q
m×q
Problem 2. Let Ai ∈ RBm×n
Q , Bi ∈ RBQ , C ∈ RBQ , and


k


∑




n×n
S HQ = 
X|X
∈
RB
,
A
XB
=
C
.

i
i
HQ




i=1

Find out XHQ ∈ S HQ such that
∥∥
∥
∥XHQ ∥∥ = min ∥X∥ .
X∈S HQ

Problem 3.

n×q
m×q
Let Ai ∈ RBm×n
Q , Bi ∈ RBQ , C ∈ RBQ , and



k


∑




n×n
S AQ = 
X|X
∈
RB
,
A
XB
=
C
.

i
i
AQ




i=1

AIMS Mathematics

Volume 7, Issue 3, 3258–3276.

## PDF page 4

3261

Find out XAQ ∈ S AQ such that
∥∥
∥
∥XAQ ∥∥ = min ∥X∥ .
X∈S AQ

The semi-tensor product(STP) of matrices was proposed initially by Cheng to solve linearization
problem of nonlinear systems, which is a generalization of traditional matrix product for the case when
the two factor matrices do not meet the dimension matching condition. It has been proved to be a
power tool in many fields such as game theory [11], graph coloring [12], logic systems [13] and so on.
In this paper, we will convert the least squares problem of reduced biquaternion matrix equation to the
corresponding real problems by using the semi-tensor product of matrices.
This paper is organized as follows. In Section 2, some basic knowledge of semi-tensor product of
matrices is introduced. In Section 3, a new kind of real vector representation of a reduced biquaternion
matrix and the main properties are proposed. In Section 4, the solutions of Problems 1–3 are studied by
using the real vector representation of reduced biquaternion matrix, the special structure of solutions
and semi-tensor product of matrices. In Section 5, two examples are illustrated to demonstrate the
Algorithms. Finally the present thesis is summarized.
2. Semi-tensor product of matrices(STP)
In this section, we will recall some basic knowledge of semi-tensor product of matrices. Please
refer to [14, 15] for more details.
Definition 2.1. Let A ∈ Rm×n , B ∈ R p×q , the semi-tensor product of A and B, denoted by
A ⋉ B = (A ⊗ It/n )(B ⊗ It/p ),
where t = lcm(n, p) is the least common multiple of n and p. If n = p, the semi-tensor product reduces
to the traditional matrix product.
Next, a simple numerical example is used to explain the semi-tensor product of matrices.


[
]
 2 −2 −1 1 
1 2


Example 2.1. Suppose A =  1 0 3 −3, B =
, then


−2 −1
−2 −3 2 1



  1 0 2 0 

 2 −2 −1 1  

  0 1 0 2 
A ⋉ B = A (B ⊗ I2 ) =  1 0 3 −3 


 −2 0 −1 0 


−2 −3 2 1
0 −2 0 −1


 4 −4 5 −5


= −5 6 −1 3  .


−6 −5 −6 −7
Lemma 2.1. Assume that A, B, C are real matrices with appropriate sizes, a, b ∈ R.
(1) (Distributive law) A ⋉ (aB ± bC) = aA ⋉ B ± bA ⋉ C, (aA ± bB) ⋉ C = aA ⋉ C ± bB ⋉ C.
(2) (Associative law)(A ⋉ B) ⋉ C = A ⋉ (B ⋉ C).
(3) (Transpose)(A ⋉ B)T = BT ⋉ AT .
(4) (Inverse)(A ⋉ B)−1 = B−1 ⋉ A−1 , where A and B are invertible square matrices.
(5) Assume that x ∈ Rm , y ∈ Rn , then x ⋉ y = x ⊗ y.
AIMS Mathematics

Volume 7, Issue 3, 3258–3276.

## PDF page 5

3262

It can be seen from the Definition 2.1 that semi-tensor product of matrices is a generalization of
traditional matrix product. A large part of the properties of traditional matrix product are preserved by
semi-tensor product of matrices. Here, only (3) of Lemma 2.1 is simply proved and the other properties
of Lemma 2.1 are similarly proved.
Proof. Suppose A ∈ Rm×n , B ∈ R p×q , t = lcm(n, p), we can obtain
))T
)(
A ⊗ It/n B ⊗ It/p
(
)T (
)
= B ⊗ It/p A ⊗ It/n T
(
)(
)
= BT ⊗ It/p AT × It/n

(A ⋉ B)T =

((

= BT ⋉ AT .
□
The semi-tensor product of a matrix and a vector has the following property of quasi-commutativity.
Definition 2.2. A swap matrix W[m,n] is a mn × mn matrix, which is defined as
W[m,n] = δmn [1, · · · , (n − 1)m + 1, · · · , m, · · · , nm] ∈ Rmn×mn .
We use the following example to briefly illustrate the construction of swap matrix.
Example 2.2. Suppose m = 2, n = 3, then
[
]
W[m,n] = δ6 [1, 3, 5, 2, 4, 6] = δ16 , δ36 , δ56 , δ26 , δ46 , δ66


1 0 0 0 0 0
0 0 0 1 0 0


0 1 0 0 0 0

= 
0 0 0 0 1 0


0 0 1 0 0 0
0 0 0 0 0 1
Remark 2.1. When m = n, we denote W[m,n] = W[n] .
The function of a swap matrix is to exchange the order of two vectors in vector multiplication.
Lemma 2.2. Let x ∈ Rm and y ∈ Rn be two column vectors. Then W[m,n] ⋉ x ⋉ y = y ⋉ x.
 
[ ]
y1 
x1
 
Example 2.3. Suppose x =
, y = y2 . Using the swap matrix constructed in Example 2.2, we can
 
x2
y3
obtain

AIMS Mathematics

Volume 7, Issue 3, 3258–3276.

## PDF page 6

3263




1
1 0 0 0 0 0
0 0 0 1 0 0
0

 [ ] y 

1
0 1 0 0 0 0 x
 

1
 (
y2 ) = 0
W[m,n] ⋉ x ⋉ y = 
⊗
0
0 0 0 0 1 0 x2  

y3


0
0 0 1 0 0 0

0 0 0 0 0 1
0


y1 x1 
y x   
 1 2  y  [ ]
y x   1  x 
=  2 1  = y2  ⊗ 1  = y ⋉ x
y2 x2    x2 
y3


y3 x1 
y3 x2

0
0
1
0
0
0

0
0
0
0
1
0

0
1
0
0
0
0

0
0
0
1
0
0



0  x1 y1 
 

0  x1 y2 


0  x1 y3 


0  x2 y1 


0  x2 y2 


1 x2 y3

Lemma 2.3. Assume A ∈ Rm×n is given, x ∈ Rt , ω ∈ Rt . Then
x ⋉ A = (It ⊗ A) ⋉ x,
A ⋉ ω = ω ⋉ (It ⊗ A).


 a11 . . . a1n 
[
]T

..  ∈ Rm×n , thus
Proof. Suppose x = x1 , x2 , . . . , xt ∈ Rt , A =  ...
. 


am1 . . . amn



 x1 ⊗ Im   a11 . . . a1n 

 
.. 
x ⋉ A = (x ⊗ Im ) A =  ...   ...
. 

 

xt ⊗ Im am1 . . . amn

T

 x1 0 . . . 0 . . . xt 0 . . . 0  

  a11 . . . a1n 
 0 x1 . . . 0 . . . 0 xt . . . 0   .
.. 
=  .. .. . .
..
.. .. . . ..   ..
. 
 . .
. . ... . .
. .  

 am1 . . . amn

0 0 0 x1 . . . 0 0 0 xt


 x1 A


 x2 A
=  ..  = (It ⊗ A) ⋉ x.
 . 


xt A
When ω is a row vector, we use the transpose property of the semi-tensor product of matrices to derive
the transformation.
□
Definition 2.3. Let Wi (i = 0, 1, · · · , n) be vector spaces. The mapping F : Πni=1 Wi → W0 is called a
multilinear mapping, if for any 1 ≤ i ≤ n, α, β ∈ R,
F(x1 , · · · , xi−1 , αxi + βyi , · · · , xn ) = αF(x1 , · · · , xi , · · · , xn ) + βF(x1 , · · · , yi , · · · , xn ),
AIMS Mathematics

Volume 7, Issue 3, 3258–3276.

## PDF page 7

3264

in which xi ∈ Wi , 1 ≤ i ≤ n, yi ∈ Wi . If dim(Wi ) = ki , (i = 0, 1, · · · , n), and (δ1ki , δ2ki , · · · , δkkii ) is the
basis of Wi . Denote
k0
∑
j1
j2
jn
F(δk1 , δk2 , · · · , δkn ) =
c sj1 , j2 , ··· , jn δks0 ,
s=1

in which jt = 1, · · · , kt , t = 1, · · · , n. Then
{
}
c sj1 , j2 , ··· , jn | jt = 1, · · · , kt , t = 1, · · · , n, s = 1, · · · , k0
are called structure constants of F. Arranging these structure constants in the following form
 11···1

n
c1
· · · c11···k
· · · ck11 k2 ···kn 
1
 11···1

n
· · · c11···k
· · · ck21 k2 ···kn 
c2
2
MF =  ..
..
..  ,
 .
.
. 
 11···1
k1 k2 ···kn 
n
ck0
· · · c11···k
·
·
·
c
k0
k0
MF is called the structure matrix of F.
3. A new kind of real vector representation of a reduced biquaternion matrix and its properties
In this section, we will propose the concept of real vector representation of a reduced biquaternion
matrix and study its properties.
Definition 3.1. Let x = x1 + x2 i + x3 j + x4 k ∈ RBQ , denote vR (x) = [x1 , x2 , x3 , x4 ]T , vR (x) is called as
the real vector representation of x.
Theorem 3.1. Let x, y ∈ RBQ , then
vR (xy) = MQ ⋉ vR (x) ⋉ vR (y),

(3.1)

where

 1
 0
MQ = 
 0
0

0
1
0
0

0
0
1
0

0
0
0
1

0 −1 0 0 0
1 0 0 0 0
0 0 0 −1 1
0 0 1 0 0

0
0
0
1

1
0
0
0

0
1
0
0


0 0 0 −1 

0 0 1 0 
,
0 −1 0 0 

1 0 0 0

MQ is the structure matrix of multiplication of reduced biquaternions.
Proof. Suppose x = x1 + x2 i + x3 j + x4 k, y = y1 + y2 i + y3 j + y4 k, we can obtain
xy = (x1 + x2 i + x3 j + x4 k) (y1 + y2 i + y3 j + y4 k)
= (x1 y1 − x2 y2 + x3 y3 − x4 y4 ) + (x1 y2 + x2 y1 + x3 y4 + x4 y3 ) i
+ (x1 y3 + x3 y1 − x2 y4 − x4 y2 ) j + (x1 y4 + x4 y1 + x2 y3 + x3 y2 ) k,
thus the left hand side of (3.1) is


 x1 y1 − x2 y2 + x3 y3 − x4 y4 
 x y + x y + x y + x y 
2 1
3 4
4 3
 1 2
 x y + x y − x y − x y  .
1
3
3
1
2
4
4
2


x1 y4 + x4 y1 + x2 y3 + x3 y2
AIMS Mathematics

Volume 7, Issue 3, 3258–3276.

## PDF page 8

3265

Since the right hand side of (3.1) is
   
   
 x1  y1 
 x1  y1 
 x  y 
 x  y 
MQ ⋉ vR (x) ⋉ vR (y) = MQ ⋉  2  ⋉  2  = MQ ⋉  2  ⊗  2 
 x3  y3 
 x3  y3 
x4
y4
x4
y4


 x1 y1 − x2 y2 + x3 y3 − x4 y4 
 x y + x y + x y + x y 
2 1
3 4
4 3
 .
=  1 2
 x1 y3 + x3 y1 − x2 y4 − x4 y2 
x1 y4 + x4 y1 + x2 y3 + x3 y2
□

(3.1) can be obtained.

Combined the real vector representation of a reduced biquaternion with vec operator of a real matrix,
we propose a new kind of real vector representation of a reduced biquaternion matrix. For this purpose,
we first propose the real vector representation of a reduced biquaternion vector as follows.
[
]
[
]T
Definition 3.2. Let x = x1 , · · · , xn , y = y1 , · · · , yn be reduced biquaternion vectors. Denote
 R 1 
 R 1 
 v (x ) 
 v (y ) 




.
R
R
..
 , v (y) =  ...  ,
v (x) = 
 R n 
 R n 
v (x )
v (y )
vR (x) and vR (y) are called as the real vector representation of reduced biquaternion vectors x and y.
Now we define the concepts of the real vector representation of a reduced biquaternion matrix A.
Definition 3.3. For A = (Aed ) ∈ RBm×n
Q , e = 1, · · · , m, d = 1, · · · , n, denote
 R 11 
 R 11 
 v (A ) 
 v (A ) 
 . 
 . 
 ..  
 ..  

 R m1  vR (Col1 (A))
 R 1n   vR (Row1 (A)) 

 v (A )   R

v (A )  R








v
(Col
(A))
v
(Row
(A))
2
2







 , vR (A) =  ..  = 
 ,
vRc (A) =  ...  = 
..
.
r

 .  
.

 R 1n  
.
.

vR (Am1 ) 

 v (A )   R


R
v (Coln (A))
v
(Row
(A))
 . 
m
 .. 
 .. 
 . 


 R mn 
vR (Amn )
v (A )
vRc (A) and vRr (A) are called the real column stacking form and the real row stacking form of A,
respectively. Real column stacking form and real row stacking form of A are collectively called real
vector representation of A.
We can prove that this real vector representation has the following properties with respect to vector
or matrix operations.

AIMS Mathematics

Volume 7, Issue 3, 3258–3276.

## PDF page 9

3266

[
]
[
]
[
]T
Theorem 3.2. Let x = x1 , x2 , · · · , xn , x̌ = x̌1 , x̌2 , · · · , x̌n , y = y1 , y2 , · · · , yn , a ∈ R, xi , x̌i , yi ∈
RBQ , then
(1) vR (x + x̌) = vR (x) + vR ( x̌),
(2) vR (ax) = avR (x),
n
∑
(
)
R
(δin )T ⋉ I4n ⊗ (δin )T ⋉ vR (x) ⋉ vR (y).
(3) v (xy) = MQ ⋉
i=1

Proof. By simply computing, we know (1), (2) hold. We only give a detailed proof of (3). Using
Theorem 3.1, we have
vR (xy) = vR (x1 y1 + x2 y2 + · · · + xn yn )
= MQ ⋉ vR (x1 ) ⋉ vR (y1 ) + · · · + MQ ⋉ vR (xn ) ⋉ vR (yn )
= MQ ⋉ (δ1n )T ⋉ vR (x) ⋉ (δ1n )T ⋉ vR (y) + · · · + MQ ⋉ (δnn )T ⋉ vR (x) ⋉ (δnn )T ⋉ vR (y)
(
)
(
)
= MQ ⋉ (δ1n )T ⋉ I4n ⊗ (δ1n )T ⋉ vR (x) ⋉ vR (y) + · · · + MQ ⋉ (δnn )T ⋉ I4n ⊗ (δnn )T ⋉ vR (x) ⋉ vR (y)
n
∑
(
)
= MQ ⋉
(δin )T ⋉ I4n ⊗ (δin )T ⋉ vR (x) ⋉ vR (y).
i=1

□
By using Theorem 3.2, we can drive the following results on the real vector representation of
multiplication of two reduced biquaternion matrices.
n×p
Theorem 3.3. Let A, Ǎ ∈ RBm×n
Q , B ∈ RBQ , α ∈ R, then

(1) vRr (A + Ǎ) = vRr (A) + vRr (Ǎ), vRc (A + Ǎ) = vRc (A) + vRc (Ǎ),
(2) vRr (αA) = αvRr (A), vRc (αA) = αvRc (A),
(3) vRr (AB) = G ⋉ vRr (A) ⋉ vRc (B), vRc (AB) = G′ ⋉ vRr (A) ⋉ vRc (B),
in which




F ⋉ (δ1m )T ⋉ [I4mn ⊗ (δ1p )T ]
F ⋉ (δ1m )T ⋉ [I4mn ⊗ (δ1p )T ]




..
..




.
.




p T 
1
T
m
T
1
T

F ⋉ (δm ) ⋉ [I4mn ⊗ (δ p ) ]
F ⋉ (δm ) ⋉ [I4mn ⊗ (δ p ) ]




..
..
 , G′ = 
 ,
G = 
.
.




p
F ⋉ (δ1 )T ⋉ [I4mn ⊗ (δ p )T ]
F ⋉ (δmm )T ⋉ [I4mn ⊗ (δ1p )T ]
m




..
..







.
.




F ⋉ (δmm )T ⋉ [I4mn ⊗ (δ pp )T ]
F ⋉ (δmm )T ⋉ [I4mn ⊗ (δ pp )T ]
(
)
n
∑
and F = MQ ⋉ (δin )T ⋉ I4n ⊗ (δin )T .
i=1

Proof. We still only prove the first equality in (3). We block A and B with its rows or columns as
follows
AIMS Mathematics

Volume 7, Issue 3, 3258–3276.

## PDF page 10

3267



 Row1 (A) 


[
]
 Row2 (A) 
A = 
 , B = Col1 (B) Col2 (B) · · · Col p (B) .
..


.


Rowm (A)
Then we have
 R
 

 v (Row1 (A)Col1 (B))   F ⋉ vR (Row1 (A)) ⋉ vR (Col1 (B)) 

 

..
..

 

.
.
 R
 

R
R
 v (Row1 (A)Col p (B))   F ⋉ v (Row1 (A)) ⋉ v (Col p (B)) 

 

..
..
 = 

vRr (AB) = 
.
.
 

 R
v (Rowm (A)Col1 (B))  F ⋉ vR (Rowm (A)) ⋉ vR (Col1 (B))

 

..
..

 

.
.

 

R
R
R
v (Rowm (A)Col p (B))
F ⋉ v (Rowm (A)) ⋉ v (Col p (B))

 

F ⋉ [(δ1m )T ⋉ vRr (A)] ⋉ [(δ1p )T ⋉ vRc (B)] F ⋉ (δ1m )T ⋉ [I4mn ⊗ (δ1p )T ]

 

..
..

 

.
.






p
p
F ⋉ [(δ1m )T ⋉ vRr (A)] ⋉ [(δ p )T ⋉ vRc (B)] F ⋉ (δ1m )T ⋉ [I4mn ⊗ (δ p )T ]
 
 R

..
..
 = 
 ⋉ vr (A) ⋉ vRc (B).
= 
.
.
 


F ⋉ [(δmm )T ⋉ vRr (A)] ⋉ [(δ1p )T ⋉ vRc (B)] F ⋉ (δmm )T ⋉ [I4mn ⊗ (δ1p )T ]

 

..
..

 

.
.

 

p T 
p T
m T
R
R
m T
F ⋉ [(δm ) ⋉ vr (A)] ⋉ [(δ p ) ⋉ vc (B)]
F ⋉ (δm ) ⋉ [I4mn ⊗ (δ p ) ]
□

The second equality can be proved similarly.
4. Algebraic solutions of Problems 1–3

In this section, we study Problems 1–3. By means of the real vector representation of reduced
biquaternion matrix and STP, we first convert Problems 1–3 into the corresponding real least squares
problems. And then we obtain their solutions.
Lemma 4.1. [16] The matrix equation Ax = b, with A ∈ Rm×n and b ∈ Rm , has a solution x ∈ Rn if
and only if
AA† b = b.
In that case it has the general solution
x = A† b + (In − A† A)y,
where y ∈ Rn is an arbitrary vector. The minimal norm solution of the linear system of equations
Ax = b is A† b
p×q
m×q
Theorem 4.2. Let Ai ∈ RBm×n
Q , Bi ∈ RBQ , C ∈ RBQ , denote

 k

∑ R

M = G1 ⋉ G ⋉ I4mn ⊗ W[4pq,4np] ⋉  vr (Ai ) ⋉ vRc (Bi ) ,
(

)

i=1

AIMS Mathematics

Volume 7, Issue 3, 3258–3276.

## PDF page 11

3268

where G1 has the same structure as G in Theorem 3.3 excepting the dimension. Hence the set S Q of
Problem 1 is represented as
{
}
S Q = X | vRc (X) = M † vRr (C) + (I4np − M † M)y, ∀y ∈ R4np .
(4.1)
And then, the minimal norm solution XQ of Problem 1 satisfies
vRc (XQ ) = M † vRr (C).

(4.2)

Proof.
k
∑

Ai XBi = C

i=1

 k
∑


⇐⇒ vRr 

i=1



Ai XBi  = vRr (C)

 k

∑ R

R
⇐⇒ G1 ⋉ G ⋉ I4mn ⊗ W[4pq,4np] ⋉  vr (Ai ) ⋉ vc (Bi ) ⋉ vRc (X) = vRr (C)
(

)

i=1

⇐⇒ MvRc (X) = vRr (C).
For the real matrix equation
MvRc (X) = vRr (C),
by Lemma 4.1, its solutions can be represented as
vRc (X) = M † vRr (C) + (I4np − M † M)y, ∀y ∈ R4np .
Thus we get the formula in (4.1).
Notice
∥
∥
minn×p ∥X∥ ⇐⇒ R min ∥∥vRc (X)∥∥

X∈RBQ

vc (X)∈R4np

According to the previous proof of this theorem, we have that the minimal norm solution XQ ∈ S Q of
Problem 1 satisfies
vRc (XQ ) = M † vRr (C).
□

Therefore, (4.2) holds.

By Theorem 4.2, we can get the sufficient and necessary condition of compatibility of the reduced
n
n
∑
∑
biquaternion matrix equation Ai XBi = C and the expression of the solution when Ai XBi = C is
i=1

i=1

compatible.
p×q
m×q
Corollary 4.3. Let Ai ∈ RBm×n
Q , Bi ∈ RBQ , C ∈ RBQ , M is given in Theorem 4.2. Then the following
statements are equivalent:
(a) Problem 1 has a solution X ∈ S Q ;
(b) (MM † − I4mq )vRr (C) = 0.
Moreover, if (b) holds, the solution set of (1.1) over RBn×p
Q can be represented as
{
}
S Q = X | vRc (X) = M † vRr (C) + (I4np − M † M)y, ∀y ∈ R4np .

AIMS Mathematics

Volume 7, Issue 3, 3258–3276.

## PDF page 12

3269

Proof.
k
∑

Ai XBi = C ⇐⇒MvRc (X) = vRr (C) ⇐⇒ MM † MvRc (X) = vRr (C)

i=1

(
)
⇐⇒MM † vRr (C) = vRr (C) ⇐⇒ MM † − I4mq vRr (C) = 0.
□
In order to study Problem 2, we define vRs (X) and give the relation of vRs (X) and vRc (X) for an
Hermitian matrix.


 x11 · · · x1n 

..
..  ∈ RBn×n , x = x1 + x2 i + x3 j + x4 k ∈ RB , denote
Theorem 4.4. Let X =  ...
Q
ij
.
. 
HQ
ij
ij
ij
ij


xn1 · · · xnn
 
 
 J1 
 J1r 




 . 
 . 
 xii 
LX1 
 .. 
 .. 
 R



 
 
LX2 
v (xi(i+1)) 
R
LXi = 
 , v s (X) =  ..  , J =  Jr  , Jr =  Jmr  ,
..
 . 
 . 


 . 
.
 .. 
 .. 
 R



 
 
v (xin )
LXn
Jn
Jnr
)T
 ( γ+η+2 )T
 (
 (
λ+θ+2
)T




δ
δ



2
2
λ+1



−n )
δ2n2 −n



( 2nγ+η+3
( 2n −n )T



T



λ+θ+3






 −δ2n2 −n
 01×2n2 −n
 δ2n2 −n
(
)
(
)T ,
Jmr = 
,
J
=
,
J
=


mr
mr
T



γ+η+4
λ+θ+4



m<r
m=r
m>r
2 −n



0
−δ
δ
1×2n



2
2






( 2n −n )
( 2n −n )

 0 2



 −δγ+η+5 T
 δλ+θ+5 T
1×2n −n
2n2 −n
2n2 −n
, η = 4(r − m − 1), λ = (r−1)(8n+2−4r)
, θ = 4(m − r − 1). Then
where, γ = (m−1)(8n+2−4m)
2
2
vRc (X) = J ⋉ vRs (X).
Remark 4.1. It can be seen from the structural characteristics of matrix X that only part of the elements
in matrix X can be used to represent the whole matrix X. So we need to find all the non-zero and nonrepeating elements in X, which reduces the number of elements in vRc (X). J is a correspondence between
the real vector representation of the matrix X and the real vector representation of the independent
elements of the matrix X.
n×q
m×q
Theorem 4.5. Let Ai ∈ RBm×n
Q , Bi ∈ RBQ , C ∈ RBQ , denote

 k
(
) ∑

M̃ = G3 ⋉ G4 ⋉ I4mn ⊗ W[4nq,4n2 ] ⋉  vRr (Ai ) ⋉ vRc (Bi ) ⋉ J,
i=1

where G3 , G4 have the same structure as G in Theorem 3.3 excepting the dimension. Hence the set
S HQ of Problem 2 is represented as
}
{
)
(
2
S HQ = X|vRs (X) = M̃ † vRr (C) + I2n2 −n − M̃ † M̃ y, ∀y ∈ R2n −n .
(4.3)
And then, the minimal norm solution XHQ of Problem 2 satisfies
vRs (XHQ ) = M̃ † vRr (C).
AIMS Mathematics

(4.4)
Volume 7, Issue 3, 3258–3276.

## PDF page 13

3270

Proof.
k
∑
i=1

 k
∑


Ai XBi = C ⇐⇒ vRr 

i=1



Ai XBi  = vRr (C).

Using Theorem 4.4, we can obtain
 k
∑


vRr 

i=1



Ai XBi  = vRr (C)

 k

∑ R

R
⇐⇒ G3 ⋉ G4 ⋉ I4mn ⊗ W[4nq,4n2 ] ⋉  vr (Ai ) ⋉ vc (Bi ) ⋉ vRc (X) = vRr (C)
(

)

i=1



∑
(
)  k


R
R
⇐⇒ G3 ⋉ G4 ⋉ I4mn ⊗ W[4nq,4n2 ] ⋉  vr (Ai ) ⋉ vc (Bi ) ⋉ J ⋉ vRs (X) = vRr (C)
i=1

⇐⇒ M̃vRs (X) = vRr (C).
For the real matrix equation
M̃vRs (X) = vRr (C),
(
)
we can obatin vRs (X) = M̃ † vRr (C)+ I2n2 −n − M̃ † M̃ y by using Lemma 4.1. Thus we get the formula (4.3).
Notice
∥
∥
minn×n ∥X∥ ⇐⇒ min ∥∥vRs (X)∥∥ ,
X∈RBHQ

2

vRs (X)∈R2n −n

we obtain that the minimal norm reduced biquaternion Hermitian solution XHQ ∈ S HQ of Problem 2
satisfies
vRs (XHQ ) = M̃ † vRr (C).
□

Therefore, (4.4) holds.

n×q
m×q
Corollary 4.6. Let Ai ∈ RBm×n
Q , Bi ∈ RBQ , C ∈ RBQ , M̃ is given in Theorem 4.5. Then the following
statements are equivalent:
(c) Problem 2 has a solution X ∈ S HQ ;
(d) ( M̃ M̃ † − I4mq )vRr (C) = 0.
Moreover, if (c) holds, the solution set of (1.1) over RBn×n
HQ can be represented as

{
}
(
)
2
S HQ = X | vRs (X) = M̃ † vRr (C) + I2n2 −n − M̃ † M y, ∀y ∈ R2n −n .
Remark 4.2. When X is a Hermitian matrix, Theorem 4.4 can be used to transform the reduced
n
∑
biquaternion matrix equation Ai XBi = C into real matrix equation M̃vRs (X) = vRr (C). Corollary 4.6
i=1

can be obtained by a proof method similar to Corollary 4.3.
Similar to Theorem 4.4, we can give the relationship between vRs (X) and vRc (X) in the reduced
biquaternion Anti-Hermitian matrix for studying Problem 3.
AIMS Mathematics

Volume 7, Issue 3, 3258–3276.

## PDF page 14

3271


 x11 · · ·

..
Theorem 4.7. Let X =  ...
.

xn1 · · ·


x1n 

3
4
2
1
 ∈ RBn×n
AQ , xi j = xi j + xi j i + xi j j + xi j k ∈ RBQ , denote

xnn



 ′
 ′ 
 xii2 
J




 J1r 




1
3
 . 
L̃X1 
 . 
 xii 
 .. 


 .. 
 x4 
 
L̃X


 ′ 
2




ii
,
L̃Xi = vR (x
, vRs (X) =  .  , J ′ =  Jr′  , Jr′ =  Jmr


.
i(i+1)) 

 . 
 . 
 . 






 .. 
 .. 
..


 
 
.
L̃Xn
′
′
 R

J
Jnr
n
v (xin )
 ( σ+ξ )T

 ( τ−ξ )T



2 +n
0



−
δ
δ2n2 +n
1×2n




2n2 +n)


(
)



(
(
)
T



T
τ+1



σ+ξ+1
τ−ξ+1 T



δ



δ
δ
2
 2n2 +n
 ( 2n +n )

2
′
′
′
( σ+ξ+2 )T , Jmr
T , Jmr =  ( 2n +n )T ,
=
Jmr
=



τ+2
τ−ξ+2



δ



m<r
m=r
m>r
δ 2 +n
δ 2 +n
2






( 2n +n )T



( 2n
)T
( 2n
)






τ+3
σ+ξ+3
 δ
 δ 2
 δτ−ξ+3 T
2n +n

2n2 +n

2n2 +n

, τ = (r−1)(8n+6−4r)
, ξ = 4(r − m). Then
where, σ = (m−1)(8n+6−4m)
2
2
vRc (X) = J ′ ⋉ vRs (X).
n×q
m×q
Theorem 4.8. Let Ai ∈ RBm×n
Q , Bi ∈ RBQ , C ∈ RBQ , denote

 k

∑ R

M̂ = G3 ⋉ G4 ⋉ I4mn ⊗ W[4nq,4n2 ] ⋉  vr (Ai ) ⋉ vRc (Bi ) ⋉ J ′ ,
(

)

i=1

where, G3 ,G4 are defined in Theorem 4.5. Hence the set S AQ of Problem 3 is represented as
{
}
(
)
2
S AQ = X|vRs (X) = M̂ † vRr (C) + I2n2 +n − M̂ † M̂ y, ∀y ∈ R2n +n .

(4.5)

And the minimal norm reduced biquaternion Anti-Hermitian solution XAQ ∈ S AQ of Problem 3 satisfies
vRs (XAQ ) = M̂ † vRr (C).

(4.6)

n×q
m×q
Corollary 4.9. Let Ai ∈ RBm×n
Q , Bi ∈ RBQ , C ∈ RBQ , M̂ is given in Theorem 4.8. Then the following
statements are equivalent:
(e) Problem 3 has a solution X ∈ S AQ ;
(f) ( M̂ M̂ † − I4mq )vRr (C) = 0.
Moreover, if (f) holds, the solution set of (1.1) over RBn×n
AQ can be represented as
}
{
(
)
2
S AQ = X|vRs (X) = M̂ † vRr (C) + I2n2 +n − M̂ † M̂ y, ∀y ∈ R2n +n .

5. Algorithm and numerical experiments
Based on the algebraic solutions in Section 4, we now present the numerical algorithms and
numerical examples for finding solutions of Problems 1–3 in this section.
AIMS Mathematics

Volume 7, Issue 3, 3258–3276.

## PDF page 15

3272

Algorithm 5.1. For Problem 1
Step1: Input: Ai , Bi , C, W[4pq,4np] Ai ∈ RBm×n
Bi ∈ RBQp×q
Q
m×q
and C ∈ RBQ (i = 1 : k)
Step2: Compute vRr (Ai ), vRc (Bi ), vRr (C), G1 , G, M
Step3: if b in Corollary 4.3 holds, then calculate the
solution X ∈ S Q according to (4.1).
Step4: if b in Corollary 4.3 and rank(M) = 4np hold, then
calculate the unique solution XQ according to (4.2).
Step5: Output: the solution X ∈ S Q
Algorithm 5.2. For Problem 2
Step1: Input: Ai , Bi , C, W[4nq,4n2 ] Ai ∈ RBm×n
Bi ∈ RBn×q
Q
Q
and C ∈ RBm×q
(i
=
1
:
k)
Q
Step2: Compute vRr (Ai ), vRc (Bi ), vRr (C), G3 , G4 , M̃
Step3: if d in Corollary 4.6 holds, then calculate the
solution X ∈ S HQ according to (4.3).
Step4: if b in Corollary 4.6 and rank( M̃) = 2n2 − n hold, then
calculate the unique solution XHQ according to (4.4).
Step5: Output: the solution X ∈ S HQ
Algorithm 5.3. For Problem 3
Step1: Input: Ai , Bi , C, W[4nq,4n2 ] Ai ∈ RBm×n
Bi ∈ RBn×q
Q
Q
and C ∈ RBm×q
(i
=
1
:
k)
Q
Step2: Compute vRr (Ai ), vRc (Bi ), vRr (C), G3 , G4 , M̂
Step3: if f in Corollary 4.9 holds, then calculate the
solution X ∈ S AQ according to (4.5).
Step4: if f in Corollary 4.9 and rank(M) = 2n2 + n hold, then
calculate the unique solution XAQ according to (4.6).
Step5: Output: the solution X ∈ S AQ
To simplify the process of checking the algorithms, in the following numerical examples, we use
the reduced biquaternion matrix equation A1 XB1 + A2 XB2 = C. To ensure that Problem 1 under testing
has a solution, we suppose Ai , Bi , C, X are known reduced biquaternion matrices.
Example 5.1. Let m = n = p = q = 3, and Ai = Ai1 + Ai2 i + Ai3 j + Ai4 k ∈ RBm×n
Q , Bi = Bi1 + Bi2 i +
p×q
n×p
Bi3 j + Bi4 k ∈ RBQ (i=1,2), X = X1 + X2 i + X3 j + X4 k ∈ RBQ . We take








8 4 4
6 2 2
5 2 4
1 5 3








A11 = 3 7 6 , A12 = 9 4 5 , A13 = 8 8 9 , A14 = 6 3 8 ,








6 5 2
7 2 8
8 4 5
6 5 9








0 5 5 
10 3 3
2 3 1
2 4 4








A21 = 2 3 2 , A22 =  4 4 6 , A23 = 1 4 3 , A24 = 9 6 10 ,








7 2 5
3 5 8
2 9 9
1 6 7








2 5 6
5 6 4 
9 1 7
1 8 9








B11 = 2 7 10 , B12 = 9 3 1 , B13 = 7 7 3 , B14 = 0 5 6 ,








8 3 7
5 9 7
7 9 9
5 4 0
AIMS Mathematics

Volume 7, Issue 3, 3258–3276.

## PDF page 16

3273









8 2 5 
7 1 1
8 1 10
5 1 4








B21 = 6 9 2  , B22 = 5 7 5 , B23 = 8 7 6  , B24 = 4 1 8








2 0 10
5 0 1
7 5 8
8 2 8








1 4 3
10 4 3 
1 4 4 
7 7 1 








X1 = 4 7 4 , X2 =  2 2 10 , X3 = 7 5 10 , X4 = 7 7 10 .








5 6 0
1 5 9
3 9 3
5 2 2
Compute
C = A1 XB1 + A2 XB2 .

(5.1)

Denote ε1 = log10 ∥MM † − I4mq ∥, we obtain
rank(M) = 36, ε1 = −12.6916.
According to Algorithm 5.1, the reduced biquaternion matrix equation (5.1) has a unique solution
XQ ∈ S Q , we can get ε2 = log10 ∥XQ − X∥ = −11.3929.
Example 5.2. Ai and Bi (i = 1, 2) are defined in Example 5.1. Suppose








2 
−2 2.5
1.5 0
1 2
 0
 0 −2 −1.5
 0








0 −3  , X̃3 =  2
0
0  , X̃4 = −1.5 0 1 ,
X̃1 = 2 0 5.5 , X̃2 =  2








2 5.5 7
−2.5 3
0
1.5 0
0
0
−1 0
X̃ = X̃1 + X̃2 i + X̃3 j + X̃4 k


1
2 − 2i − 2j + 1.5k 2 + 2.5i − 1.5j



0
5.5 − 3i + k  ∈ RB3×3
= 2 + 2i + 2j − 1.5k
HQ


2 − 2.5i + 1.5j
5.5 + 3i − k
7
Compute (5.1). we can get ε3 = log10 ∥ M̃ M̃ † − I4mq ∥ = −10.7394 and rank( M̃) = 15. The reduced
biquaternion matrix equation (5.1) has a unique solution XHQ by using Algorithm (5.2). So we can get
ε4 = log10 ∥XHQ − X̃∥ = −13.5758.
Example 5.3. Ai and Bi (i = 1, 2) are defined in Example 5.1. Suppose








7 5.5
4 
 0 −0.5 −1.5
 1
8 6 5
6 4








0
2  , X 2 =  7
4 4.5 , X 3 = 6 8 7 , X 4 = 4 3 6.5 ,
X 1 = 0.5








1.5 −2
0
5.5 4.5 5
5 7 9
4 6.5 2
X = X1 + X2i + X3j + X4k


i + 8j + 6k
−0.5 + 7i + 6j + 4k −1.5 + 5.5i + 5j + 4k



4i + 8j + 3k
2 + 4.5i + 7j + 6.5k  ∈ RB3×3
=  0.5 + 7i + 6j + 4k
AQ


1.5 + 5.5i + 5j + 4k −2 + 4.5i + 7j + 6.5k
5i + 9j + 2k

AIMS Mathematics

Volume 7, Issue 3, 3258–3276.

## PDF page 17

3274

Similarly, Compute (5.1). we can get ε5 = log10 ∥ M̂ M̂ † − I4mq ∥ = −9.6723 and rank( M̃) = 21. The
reduced biquaternion matrix equation (5.1) has a unique solution XAQ by using Algorithm 5.3. So we
can get ε6 = log10 ∥XAQ − X∥ = −12.6248.
Example 5.4. For m = n = p = q = 2K, Ai and Bi generated randomly for K = 2 : 6. Consider the
reduced biquaternion matrix equation (1.1), we record the errors in the three Problems in Figure 1.

Figure 1. Errors in different dimensions.
Examples 5.1–5.4 are used to show the feasibility of Algorithms 5.1–5.3.
6. Conclusions
In this paper, we proposed a real vector representation of reduced biquaternion matrix, which
preserves the relative positions of the elements in the original reduced biquaternion matrix. For every
element in reduced biquaternion, the real and three imaginary parts are remained as a whole.
Combined this real vector representation with semi-tensor product of matrices, we solved the
Problems 1–3.
Acknowledgments
This work was supported by National Natural Science Foundation of China 62176112; Science
and Technology Project of Department of Education, Shandong Province ZR2020MA053; the science
foundation of Liaocheng University under grants 318011921.
Conflict of interest
The authors declare that they have no competing interests.
AIMS Mathematics

Volume 7, Issue 3, 3258–3276.

## PDF page 18

3275

References
1. S. C. Pei, J. H. Chang, J. J. Ding, Commutative reduced biquaternions and their Fourier transform
for signal and image processing applications, IEEE T. Signal. Proces., 52 (2004), 2012–2031. doi:
10.1109/TSP.2004.828901.
2. H. D. Schütte, J. Wenzel, Hypercomplex numbers in digital signal processing, IEEE Int. Symp.
Circuits Syst., 2 (1990), 1557–1560. doi: 10.1109/ISCAS.1990.112431.
3. S. C. Pei, J. H. Chang, J. J. Ding, M. Y. Chen, Eigenvalues and singular value decompositions
of reduced biquaternion matrices, IEEE T. Circuits Syst. I, 55 (2008), 2673–2685. doi:
10.1109/TCSI.2008.920068.
4. T. Isokawa, H. Nishimura, N. Matsui, Commutative quaternion and multistate hopfield neural
networks, In: The 2010 international joint conference on neural networks, 2010. doi:
10.1109/IJCNN.2010.5596736.
5. H. H. Kösal, Least-squares solutions of the reduced biquaternion matrix equation AX = B
and their applications in colour image restoration, J. Mod. Optic., 66 (2019), 1802–1810. doi:
10.1080/09500340.2019.1676474.
6. S. F. Yuan, Y. Tian, M. Z. Li, On Hermitian solutions of the reduced biquaternion matrix
equation (AXB, CXD) = (E, G), Linear Multlinear Algebra, 68 (2020), 1355–1373. doi:
10.1080/03081087.2018.1543383.
7. I. I. Kyrchei, Determinantal representation of general and (skew-) Hermitian solutions to the
generalized sylvester-type quaternion matrix equation, Abst. Appl. Anal., 2019 (2019), 5926832.
doi: 10.1155/2019/5926832.
8. I. I. Kyrchei, Determinantal representations of solutions and Hermitian solutions to some
system of two-sided quaternion matrix equations, J. Math., 2018 (2018), 6294672. doi:
10.1155/2018/6294672.
9. J. S. Respondek, Recursive numerical recipes for the high efficient inversion of the
confluent Vandermonde matrices, Appl. Math. Comput., 225 (2013), 718–730. doi:
10.1016/j.amc.2013.10.018.
10. F. X. Zhang, M. S. Wei, Y. Li, J. L. Zhao, An efficient method for least squares problem of
the quaternion matrix equation X − AX̂B = C, Linear Multlinear Algebra, 2020, 1–13. doi:
10.1080/03081087.2020.1806197.
11. D. Z. Cheng, Q. H. Qi, Z. Q. Liu, From STP to game-based control, Sci. China Inform. Sci., 61
(2018), 010201. doi: 10.1007/s11432-017-9265-2.
12. Y. Z. Wang, C. H. Zhang, Z. B. Liu, A matrix approach to graph maximum stable set and
coloring problems with application to multi-agent systems, Automatica, 48 (2012), 1227–1236.
doi: 10.1016/j.automatica.2012.03.024.
13. J. Q. Lu, H. T. Li, Y. Liu, F. F. Li, Survey on semi-tensor product method with its applications in
logical networks and other finite-valued systems, IET Control Theory Appl., 11 (2017), 2040–2047.
doi: 10.1049/iet-cta.2016.1659.
AIMS Mathematics

Volume 7, Issue 3, 3258–3276.

## PDF page 19

3276

14. D. Z. Cheng, H. S. Qi, Z. Q. Li, Analysis and control of Boolean networks: A semi-tensor product
approach, London: Springer, 2011. doi: 10.1007/978-0-85729-097-7.
15. D. Z. Cheng, Z. Q. Liu, Z. H. Xu, T. L. Shen, Generalised semi-tensor product of matrices, IET
Control Theory Appl., 14 (2020), 85–95. doi: 10.1049/iet-cta.2019.0337.
16. G. H. Golub, C. F. VanLoan, Matrix computations, 4 Eds., Baltimore MD: The Johns Hopkins
University Press, 2013.
© 2022 the Author(s), licensee AIMS Press.
This
is an open access article distributed under the
terms of the Creative Commons Attribution License
(http://creativecommons.org/licenses/by/4.0)

AIMS Mathematics

Volume 7, Issue 3, 3258–3276.
