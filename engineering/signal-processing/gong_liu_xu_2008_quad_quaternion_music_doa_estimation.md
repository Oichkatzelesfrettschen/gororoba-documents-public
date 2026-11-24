Source: https://doi.org/10.1155/2008/213293
PDF sha256: e546b08ac03f619a757fa3ec7b16e38455efd9ffc3d31c348f17f1ac80b674d3
License: https://creativecommons.org/licenses/by/
Language: eng
Fidelity: machine-gated

# Transcription of gong_liu_xu_2008_quad_quaternion_music_doa_estimation.pdf

Transcription of `gong_liu_xu_2008_quad_quaternion_music_doa_estimation.pdf` in this directory, 14 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-14 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Hindawi Publishing Corporation
EURASIP Journal on Advances in Signal Processing
Volume 2008, Article ID 213293, 14 pages
doi:10.1155/2008/213293

Research Article
Quad-Quaternion MUSIC for DOA Estimation
Using Electromagnetic Vector Sensors
Xiaofeng Gong, Zhiwen Liu, and Yougen Xu
Department of Electronic Engineering, Beijing Institute of Technology, Beijing 100081, China
Correspondence should be addressed to Yougen Xu, yougenxu@bit.edu.cn
Received 24 April 2008; Revised 22 October 2008; Accepted 22 December 2008
Recommended by Jacques Verly
A new quad-quaternion model is herein established for an electromagnetic vector-sensor array, under which a multidimensional
algebra-based direction-of-arrival (DOA) estimation algorithm, termed as quad-quaternion MUSIC (QQ-MUSIC), is proposed.
This method provides DOA estimation (decoupled from polarization) by exploiting the orthogonality of the newly defined “quadquaternion” signal and noise subspaces. Due to the stronger constraints that quad-quaternion orthogonality imposes on quadquaternion vectors, QQ-MUSIC is shown to oﬀer high robustness to model errors, and thus is very competent in practice.
Simulation results have validated the proposed method.
Copyright © 2008 Xiaofeng Gong et al. This is an open access article distributed under the Creative Commons Attribution License,
which permits unrestricted use, distribution, and reproduction in any medium, provided the original work is properly cited.

1.

INTRODUCTION

A “complete” electromagnetic (EM) vector sensor comprises six collocated and orthogonally oriented EM sensors
(e.g., short dipole and small loop), and provides complete
electric and magnetic field measurements induced by an
EM incidence [1–3]. An “incomplete” EM vector sensor
with one or more components removed is also of high
interest in some practical applications [4, 5]. Numerous
algorithms for direction-of-arrival (DOA) estimation using
one or more EM vector sensors have been proposed.
For example, vector sensor-based maximum likelihood
strategy was addressed in [6–9], multiple signal classification (MUSIC [10]) was extended for both incomplete
and complete EM vector-sensor arrays in [11–16], subspace fitting technique was reconsidered for incomplete
EM vector sensors in [17, 18], and estimation of signal
parameters via rotational invariance techniques (ESPRIT
[19]) was revised for EM vector sensor(s) in [20–26].
The identifiability issue of EM vector sensor-based DOA
estimation has been discussed in [27–29]. Some other
related work can be found in [30–34]. In all the contributions mentioned above, complex-valued vectors are
used to represent the output of each EM vector sensor
in the array, and the collection of an EM vector-sensor
array is arranged via concatenation of these vectors into a

“long vector.” Consequently, the corresponding algorithms
somehow destroy the vector nature of incident signals
carrying multidimensional information in space, time, and
polarization.
More recently, a few eﬀorts have been made on characterizing the output of vector sensors within a hypercomplex framework, wherein hypercomplex values, such
as quaternions and biquaternions, are used to retain the
vector nature of each vector sensor [35–37]. In particular,
singular value decomposition technique was extended for
quaternion matrices in [35] using three-component vector
sensors. Quaternion-based MUSIC variant (Q-MUSIC) was
proposed in [36] by using two-component vector sensors.
Biquaternion-based MUSIC (BQ-MUSIC) was proposed in
[37] by employing three-component vector sensors. The
advantage of using quaternions and biquaternions for vector
sensors is that the local vector nature of a vector-sensor
array is preserved in multiple imaginary parts, and thus
could result in a more compact formalism and a better
estimation of signal subspace [36, 37]. More importantly,
from the algebraic point of view, the algebras of quaternions
and biquaternions are associative division algebras using
specified norms [38], and therefore are convenient to use in
the modeling and analysis of vector-sensor array processing.
However, it is important to note that quaternions and
biquaternions deal with only four-dimensional (4D) and

## PDF page 2

2

EURASIP Journal on Advances in Signal Processing

(8D) algebras, respectively, while a full characterization of
the sensor output for complete six-component EM vector
sensors requires an algebra with dimensions equal to 12 or
more.
Unfortunately, not all algebras having 12 or more
dimensions are associative division algebras. For example,
sedenions, as a well-known 16D algebra, are neither an
associative algebra nor a division algebra [39], and thus
are not suitable for the modeling and analysis of vector
sensors. In this paper, we use a specific 16D algebra—
quad-quaternions algebra [40–42] to model the output of
six-component EM vector sensor(s) [3]. This 16D quadquaternion algebra can be proved to be an associative
division algebra, and thus is well adapted to the modeling and analysis of complete EM vector sensors. More
precisely, We redefine the array manifold, signal subspace,
and noise subspace from a quad-quaternion perspective,
and propose a quad-quaternion-based MUSIC variant (QQMUSIC) for DOA estimation by recognizing and exploiting the quad-quaternion orthogonality between the quadquaternion signal and noise subspaces. QQ-MUSIC here
is shown to be more attractive in the presence of two
typical model errors, that is, sensor position error and
sensor orientation error, which are often encountered in
practice.
The rest of the paper is organized as follows. In Section 2,
we present introductions on quad-quaternions and quadquaternion matrices. In Section 3, the quad-quaternionbased MUSIC algorithm is presented. In Section 4, we compare the proposed algorithm with some existing methods by
simulations. Finally, we conclude the paper in Section 5.
Since this paper concerns several diﬀerent hypercomplex
values, we here summarize the symbols of values that will
appear in subsequent sections in Table 1.
2.

QUAD-QUATERNIONS AND QUAD-QUATERNION
MATRICES

In this section, we introduce the algebra of quad-quaternions, and represent some results related to quad-quaternion
matrices. The algebras of quaternions and biquaternions are
introduced in detail in [35–38] and thus are not addressed
here.
2.1. Quad-quaternions and quad-quaternion matrices
Quad-quaternion algebras are a class of 16D algebras [40],
which were first considered by Albert since the 1930s [41].
(The quad-quaternion algebras mentioned in this paper are
termed as the generalized biquaternion algebras in [40–42]).
The quad-quaternion algebra is defined as follows.
Definition 1 (see [42]). Denote H(an ,bn ) the quaternion
algebra over bases {1, in , jn , kn }, where i2n = an , jn2 = bn ,
in jn = − jn in = kn , and an , bn are nonzero real numbers,
n = 1, 2, then a quad-quaternion algebra over real numbers
is the tensor product [40] of H(a1 ,b1 ) and H(a2 ,b2 ) , denoted by
H(a1 ,b1 )H(a2 ,b2 ) = H(a1 ,b1 ) ⊗ H(a2 ,b2 ) .

By definition, we can see that any element p
H(a1 ,b1 )H(a2 ,b2 ) can be expressed as
(

p = p00 + I p01 + J p02 + K p03

∈

)

(

)

(

)

(

)

+ i p10 + I p11 + J p12 + K p13

+ j p20 + I p21 + J p22 + K p23

(1)

+ k p30 + I p31 + J p32 + K p33 ,
where
i2 = a1 ,

j 2 = b1 ,

k2 = −a1 b1 ,

I 2 = a2 ,

J 2 = b2 ,

K 2 = −a2 b2 ,

i j = − ji = k,
(

)

(

)

IJ = −JI = K,

(

)

(

)

ki = −ik = j · − a1 ,

KI = −IK = J · − a2 ,

jk = −k j = i · − b1 ,

JK = −KJ = I · − b2 ,

lL = Ll,
(2)
where l = i, j, k and L = I, J, K.
Denote the classical Hamilton quaternions by H [43],
and consider the following particular case a1 = b1 = a2 =
b2 = −1, so that H(a1 ,b1 ) = H(a2 ,b2 ) = H. Then, with
an appropriate choice of norm, the tensor product of H
and H, denoted by HH = H ⊗ H, can be proved to be
a division algebra according to [42, Theorem 4.3], so that
zero divisors do not exist (note that the quad-quaternions
herein mentioned are labeled as the generalized biquaternions
in [42], which are diﬀerent from the classical biquaternions).
Since the algebra of quad-quaternions is always an associative
algebra [41], then HH = H ⊗ H is an associative division
algebra.
Furthermore, from (1) we can see that p ∈ HH can be
interpreted as a quaternion with quaternionic coeﬃcients. In
addition, if pmn = 0 for all m, n = 0, 1, 2, 3, p is called a zero
quad-quaternion, denoted by p = 0. If p00 = 1, and all the
other coeﬃcients are zero, then p is called an identity quadquaternion, denoted by p = 1. In addition, p00 is called the
scalar part of p, denoted by S(p), while the vector part of p is
given by V (p) = p − S(p).
Besides the expression in (1), a quad-quaternion p ∈ HH
can as well be expressed as
p = p0 + I p1 + J p2 + K p3 = b0 + Ib1 ,

(3)

where pn = p0n + ip1n + j p2n + k p3n ∈ H, n = 0, 1, 2, 3; bm =
pm + J pm+2 ∈ HC(J) , m = 0, 1. In particular, p = b0 + Ib1 can
be considered as a quad-quaternion version of the CayleyDickson expression for quaternions and biquaternions in
[36, 37]. The definitions of addition and multiplication
extend naturally from the case of biquaternion matrices, and
thus are not addressed here.
From the geometric perspective, a quad-quaternion p =
p0 +ip1 + j p2 +k p3 can be considered as a point in a 4D space
spanned by 1, i, j, k, as shown in Figure 1. The diﬀerence
from the quaternion case is that the 1, i, j, k coeﬃcients of

## PDF page 3

Xiaofeng Gong et al.

3
Table 1: Symbols of algebraic values.

R
C(L)

Real numbers
Complex numbers with bases {1, L}, where L = i, j, k, I, J, K. In particular, C(i) is denoted by C.

H(a,b)

Quaternions with bases {1, i, j, k} such that i2 = a, j 2 = b and i j = − ji = k, where a and b are nonzero real numbers. In
particular, H = H(−1,−1) corresponds to the classical Hamilton quaternions

H(1) , H(2)

H(1) denotes Hamilton’s quaternions with bases {1, i, j, k }; H(2) denotes the Hamilton quaternions with bases {1, I, J, K }.
In particular, we denote H(1) by H.

HC(L)

Biquaternions with bases {1, i, j, k, L, Li, L j, Lk}, L = I, J, K, such that i2 = −1, j 2 = −1, i j = − ji = k and lL = Ll, where
l = i, j, k. In particular, we denote HC(I) by HC .

HH

Quad-quaternions with bases {1, i, j, k, I, Ii, I j, Ik, J, Ji, J j, Jk, K, Ki, K j, Kk} such that i2 = j 2 = I 2 = J 2 = −1,
i j = − ji = k, IJ = −JI = K, and lL = Ll, where l = i, j, k and L = I, J, K.

p are not real values, but four individual quaternions which
can be considered as four subpoints in a 4D hypospace
spanned by 1, I, J, K. Therefore, quite similar to quaternion
rotations [38], we can interpret quad-quaternion multiplications as a more complex 16D “quad-quaternion rotations”
which involve both 4D rotations(quaternion multiplications) and combination of 4D points (quaternion additions)
in spaces spanned by 1, i, j, k and 1, I, J, K.
Definition 2. A quad-quaternion matrix Q ∈ (HH )M ×N is a
matrix with M rows and N columns of which each element
is a quad-quaternion qm,n ∈ HH , m = 1, 2, . . . , M, n =
1, 2, . . . , N. In particular, an N dimensional quad-quaternion
column (row) vector can be considered as an N × 1 (1 ×
N) quad-quaternion matrix. In this paper, quad-quaternion
vectors are specifically referred to as column vectors. Similar
to the case of quad-quaternion scalars, a quad-quaternion
matrix Q ∈ (HH )M ×N can be expressed as follows:
(

Q = Q00 + IQ01 + JQ02 + KQ03

)

(

)

(

)

(

)

+ i Q10 + IQ11 + JQ12 + KQ13

+ j Q20 + IQ21 + JQ22 + KQ23

+ k Q30 + IQ31 + JQ32 + KQ33

(4)

= Q0 + IQ1 + JQ2 + KQ3 = B0 + IB1 ,

where Qn1 n2 ∈ RM ×N , n1 , n2 = 0, 1, 2, 3, Qn ∈ HM ×N ,
n = 0, 1, 2, 3, and B0 , B1 ∈ (HC(J) )M ×N . Similar to quadquaternion scalars, the scalar and vector parts of Q are given
by S(Q) = Q00 and V (Q) = Q − S(Q), respectively.
In the following discussion, we mainly focus on results
related to quad-quaternion matrices and vectors. The results
related to scalars can be directly obtained by considering a
quad-quaternion scalar as a 1 × 1 quad-quaternion “matrix.”
2.2. Previous relevant results
In this section, we present some results that are directly
generalized from quaternion or biquaternion results. All
the lemmas in this section can be proved similarly to their
quaternion and biquaternion counterparts in [35–37], and
thus are not included in this paper.

K
p3

1

I

J

p = p0 + ip1 + j p2 + k p3

k

K

p3

1

I

p0 J
1

p2

j
K

p1
K
i

I

1

I

1
p2 J

p1 J

Figure 1: The geometric illustration of quad-quaternions.

Definition 3 ([37, Definition 2]). There exist four diﬀerent
conjugations for quad-quaternion matrices as follows.
(i) C-conjugation QC : QC = B0 − IB1 ;
(ii) H1 -conjugation Q⋆ : Q⋆ = Q∗0 + IQ∗1 + JQ∗2 + KQ∗3 ;
(iii) H2 -conjugation Q∗ : Q∗ = Q0 − IQ1 − JQ2 − KQ3 ;
(iv) Total-conjugation Q: Q = Q∗0 − IQ∗1 − JQ∗2 − KQ∗3 ,
where Q∗n denotes the quaternion conjugation of Qn , n =
0, 1, 2, 3, as given in [36].
Definition 4 (from [37]). The transpose of Q = Q0 + IQ1 +
JQ2 + KQ3 ∈ (HH )M ×N , denoted by QT ∈ (HH )N ×M , is
defined as QT ≜ QT0 + IQT1 + JQT2 + KQT3 , where QTn denotes
the quaternion transpose of Qn , n = 0, 1, 2, 3. Then we have
the following four diﬀerent conjugated transposes.
C

T

(i) C-conjugated transpose Q◁ : Q◁ = (QC ) = (QT ) ;
⋆

(ii) H1 -conjugated transpose QH1 : QH1 = (Q⋆ )T = (QT ) ;
∗

(iii) H2 -conjugated transpose QH2 : QH2 = (Q∗ )T = (QT ) ;
T

(iv) Total-conjugated transpose QH : QH = (Q) = QT .
Definition 5 ([37, Definition 3]). The norm of a quadquaternion p = p0 + I p1 + J p2 + K p3 , denoted by | p|, is
given by
| p| =

√∣ ∣
∣ ∣
∣ ∣
∣ ∣
∣ p0 ∣2 + ∣ p1 ∣2 + ∣ p2 ∣2 + ∣ p3 ∣2 .

(5)

## PDF page 4

4

EURASIP Journal on Advances in Signal Processing

By definition, we can see that the following equation holds:
[( ∗

∗

∗

∗

S(pp) = S p0 − I p1 − J p2 − K p3

)(

[( ∗

=S

p0 +I p1 +J p2 +K p3

p0 p0 + p1∗ p1 + p2∗ p2 + p3∗ p3

)]

)

(

)

(

)

(

)]

+ I p0∗ p1 + p3∗ p2 − p1∗ p0 − p2∗ p3
+ J p0∗ p2 + p1∗ p3 − p2∗ p0 − p3∗ p1

+ K p0∗ p3 + p2∗ p1 − p3∗ p0 − p1∗ p2

Q = UDUH =

(
)
= p0∗ p0 + p1∗ p1 + p2∗ p2 + p3∗ p3 = | p|2 .

It is important to note that | pq| /= | p||q|, so that quadquaternions do not form a normed algebra. We can further
define the norm of a quad-quaternion vector q ∈ (HH )N ×1
by
(7)

Definition 6 (see (15) from [37]). Two quad-quaternion
vectors a, b ∈ (HH )N ×1 are said to be orthogonal if
aH b = 0.

(8)

Definition 7 (see (17) from [37]). The adjoint matrix (χ Q ∈
(HC(J) )2M ×2N ) of a quad-quaternion matrix Q ∈ (HH )M ×N =
B0 + IB1 (where B0 , B1 ∈ (HC(J) )M ×N ) is given by
(

)

B0 B∗1
χQ ≜
.
−B1 B∗
0
Let further ΨM ≜ [IM , −I · IM ] ∈ (C(I) )
is the identity matrix of size M × M, then
1
Q = ΨM χ Q ΨH
N,
2

(9)
M ×2M

, where IM
(10)

where
ΨM ΨH
M = 2IM ,
H
χ Q ΨH
N ΨN = ΨM ΨM χ Q .

(11)

Lemma 1 (from [35]). Consider two quad-quaternion matrices A ∈ (HH )M ×N and B ∈ (HH )N ×L , and denote the adjoint
matrices of A, B, and AB by χ A , χ B , and χ AB , respectively, then
χ AB = χ A · χ B .

4N
∑
n=1

(6)

√ (
)
∥q ∥ ≜ S q H q .

Corollary 1 (from [37]). The eigenvalues of a Hermitian
quad-quaternion matrix are real values. Consider a Hermitian
quad-quaternion matrix Q ∈ (HH )N ×N whose adjoint matrix
χ Q can be eigendecomposed as χ Q = Ub DUH
b , where Ub ∈
(HC )2N ×4N , and D ∈ R(4N ×4N) is a real diagonal matrix. The
eigendecomposition of Q is then given by

(12)

Lemma 2 ([37, Lemma 1]). If PH = P, then P ∈ (HH )N ×N
is Hermitian. Then we note that the adjoint matrix of a
Hermitian quad-quaternion matrix is also Hermitian.
Definition 8 (from [37]). If Qu = uλ, where u ∈ (HH )N ×1 ,
λ ∈ C, and Q ∈ (HH )N ×N , then λ and u are, respectively, the
right eigenvalue and the associated right eigenvector of Q.
Lemma 3 ([37, Lemma 2]). Denote the adjoint matrix of Q ∈
(HH )N ×N by χ Q , if λ ∈ C and ub ∈ (HC(J) )2N ×1 are the right
eigenvalue and the associated right eigenvector of χ Q , then λ
and u = ΨN ub are the right eigenvalue and the associated right
eigenvector of Q.

λn un uH
n,

(13)

√

where U = (1/ 2)ΨN Ub ∈ (HH )N ×4N , λn is the nth element
of the diagonal of D, un is the nth column vector of U.
Lemma 4. The eigenvectors corresponding to diﬀerent eigenvalues of a Hermitian quad-quaternion matrix are orthogonal.
2.3.

New definitions and lemmas for
quad-quaternioins

In this section, we introduce some new results related to
quad-quaternions. For an easier reading of this section, all
the results are given directly, while some of their proofs are
summarized in the appendix for the reference of interested
readers.
Definition 9. Let Λ = {1, i, j, k, I, Ii, I j, Ik, J, Ji, J j, Jk, K, Ki,
K j, Kk} and Γ ⊆ Λ, then the Γ-match of a quad-quaternion
matrix Q ∈ (HH )M ×N , denoted by S(Q | Γ), is obtained
by keeping the coeﬃcients of the units in Γ unchanged, and
setting all the other coeﬃcients to zero. The Γ-complement
of Q is defined as V (Q | Γ) ≜ Q − S(Q | Γ).
By definition, we know that the match and complement
operations are used to select some desired parts of quadquaternions. For example, if Γ = {1, i, K }, then S(Q | Γ) =
Q00 +iQ10 +KQ03 , where Q00 , Q10 , Q03 are given in (4). Also it
can be proved that V (Q | Γ⊥ ) = S(Q | Γ), where Γ⊥ denotes
the complement of Γ. Particularly, if Γ = {1}, S(Q | Γ) and
V (Q | Γ) are equal to the scalar part and the vector part of
Q, respectively.
Definition 10. Let Λ = {1, i, j, k, I, Ii, I j, Ik, J, Ji, J j, Jk, K, Ki,
K j, Kk}, and Γ ⊆ Λ, then the Γ-conjugation of a quadquaternion matrix Q = S(Q | Γ) + V (Q | Γ) ∈ (HH )M ×N
is denoted by conj(Q | Γ), and defined as
conj(Q | Γ) ≜ S(Q | Γ) − V (Q | Γ).

(14)

It should be noted that the four conjugations given in
Definition 3 are actually four special examples of the Γconjugation corresponding to diﬀerent selections of Γ.
For example, the H1 -conjugation corresponds to Γ =
{1, I, J, K }, whereas the total-conjugation corresponds to Γ =
⊥
{i, j, k, I, J, K } .
Lemma 5. Given two sets Γ1 , Γ2 ⊆ Λ, we have
((

(

conj conj Q | Γ1

))

| Γ2

)

(
) (
)⊥ )
(
,
= conj Q | Γ1 ∩ Γ2 ∪ Γ1 ∪ Γ2

(15)

## PDF page 5

Xiaofeng Gong et al.

5

where Γ1 ∩ Γ2 and Γ1 ∪ Γ2 denote the intersection and union of
Γ1 and Γ2 , respectively.
Definition 11. Let Λ = {1, i, j, k, I, Ii, I j, Ik, J, Ji, J j, Jk, K, Ki,
K j, Kk} and Γ ⊆ Λ, the Γ-conjugated transpose of Q is
given by conj(Q | Γ)T . It is easy to prove that conj(Q | Γ)T =
conj(QT | Γ). Also, when Γ = Λ, QT = conj(Q | Γ)T .
Similar to the Γ -conjugation, the four diﬀerent conjugated
transposes given in Definition 4 are four diﬀerent examples
corresponding to four diﬀerent selections of Γ.
Definition 12. Quad-quaternion vectors v1 , v2 , . . . , vN ∈
(HH )M ×1 are said to be right (left) linear dependent if there
are scalars μ1 , μ2 , . . . , μN ∈ HH not all zero, such that v1 μ1 +
v2 μ2 + · · · + vN μN = oM ×1 (μ1 v1 + μ2 v2 + · · · + μN vN =
oM ×1 ). Moreover, if v1 μ1 + v2 μ2 + · · · + vN μN = oM ×1
(μ1 v1 + μ2 v2 + · · · + μN vN = oM ×1 ) is true if and only
if μ1 , μ2 , . . . , μN are all zero, vectors v1 , v2 , . . . , vN are said
to be right (left) linearly independent. Here, oN ×1 is an
N × 1 zero vector. Obviously, since v1 μ1 /= μ1 v1 in most
cases, the concept of right linear dependent (independent)
is diﬀerent from that of left linear dependent (independent).

{

spanned by v1 , v2 , . . }. , vN as R ≜ v | v = v1 μ1 +
v2 μ2 + · · · + vN μN , where μ1 , μ2 , . . . , μN are arbitrary
quad-quaternion scalars. R can also be denoted as R =
span(v1 , v2 , . . . , vN ).
Lemma 8. If v1 , v2 , . . . , vN are N eigenvectors of a Hermitian
quad-quaternion matrix, then v1 μ1 , v2 μ2 , . . . , vN μN are also
a set of eigenvectors of this Hermitian quad-quaternion
matrix, where μ1 , μ2 , . . . , μN are nonzero quad-quaternions.
Then, we have span(v1 , v2 , . . . , vN ) = span(v1 μ1 , v2 μ2 , . . . ,
vN μN ).
This lemma indicates that the indetermination of eigenvectors of a Hermitian quad-quaternion matrix does not
impact their span. From the geometric perspective, when
the eigenvector multiplies a nonzero scalar from the right
side, all the elements of this eigenvector are rotated in the
16D quad-quaternion space (as shown in Figure 1) with
the same quad-quaternion manner, and the proportional
relationship between diﬀerent elements does not change.
Therefore, the intrinsic “structure” of this eigenvector is
independent of the above-mentioned eigenvector indetermination.

Definition 13. Given a set of quad-quaternion vectors
v1 , v2 , . . . , vN ∈ (HH )M ×1 , if v1 , v2 , . . . , vR (R < N),
are right (left) linearly independent and there exists an
arbitrary vector vR+1 ∈ (HH )M ×1 such that v1 , v2 , . . . , vR+1
are right (left) linearly dependent, then v1 , v2 , . . . , vR form
a maximal right (left) linearly independent set. Furthermore, we define the right (left) rank of {v1 , v2 , . . . , vN }
as rankR ({v1 , v2 , . . . , vR }) ≜ R (rankL ({v1 , v2 , . . . , vR }) ≜
R).

3.

Definition 14. Given a quad-quaternion matrix P = [p1 ,
p2 , . . . , pN ], where pn is the nth column of P, n =
1, 2, . . . , N. Then the right (left) rank of P is defined
as rankR (P) ≜ rankR ({p1 , p2 , . . . , pN }) (rankL (P) ≜
rankL ({p1 , p2 , . . . , pN })). In addition, we have the following
lemma.

p(θ,ϕ,γ,η) = i Ex

Lemma 6. Denote the adjoint matrix of P ∈ (HH )
then
(

N ×N

by χ P ,

)

( )
( )
1
1
rankR (P) = rankR χ P rankL (P) = rankL χ P .
2
2

(16)
In the following discussion, we only consider the right rank, and
we denote rank(P) = rankR (P).
Lemma 7. Denote the eigenvalue decomposition of a Hermitian quad-quaternion matrix Q by Q = UDUH , then we have
1
rank(Q) = rank(D).
4

(17)

Definition 15. Given a set of orthogonal quad-quaternion
vectors v1 , v2 , . . . , vN , we can define the vector space R

QUAD-QUATERNION MUSIC

3.1.

Quad-quaternion model for EM vector sensors

Let (θ, ϕ) and (γ, η) be the azimuth-elevation 2D DOA (see
Figure 2) and polarization of an EM signal, respectively,
where 0 < θ ≤ 2π, 0 ≤ ϕ ≤ π, and 0 ≤ γ ≤ π/2, −π ≤ η ≤ π.
The output of an EM vector sensor then can be capsulated
into the following quad-quaternion scalar:
[ (θ,ϕ,γ,η)

[ (θ,ϕ,γ,η)

+ k Ez

(θ,ϕ,γ,η) ]

+ IHx

(θ,ϕ,γ,η) ]

+ IHz

[ (θ,ϕ,γ,η)

+ j Ey

(θ,ϕ,γ,η) ]

+ IH y

,
(18)

(θ,ϕ,γ,η)

(θ,ϕ,γ,η)

(θ,ϕ,γ,η)

(θ,ϕ,γ,η)

where Ex
, Ey
, Ez
∈ C(J) , and Hx
,
(θ,ϕ,γ,η)
(θ,ϕ,γ,η)
(J)
Hy
, Hz
∈ C are the three components of the
electric vector and the magnetic vector, respectively, which
are defined as [2]
⎛

(θ,ϕ,γ,η) ⎞
Ex
⎞
⎜
⎟ ⎛
cos ϕ cos θ
− sin θ
⎜ (θ,ϕ,γ,η) ⎟
⎜ Ey
⎟ ⎜
⎟
⎜
⎟ ⎜
cos θ
cos ϕ sin θ ⎟
⎜
⎟ ⎜
⎟ (
⎜ (θ,ϕ,γ,η) ⎟ ⎜
)
⎟
⎜ Ez
⎟ ⎜
− sin ϕ ⎟
cos γ
0
⎜
⎟ ⎜
⎟
⎜
⎟≜
·
.
⎜ (θ,ϕ,γ,η) ⎟ ⎜
− cos ϕ cos θ − sin θ ⎟
sin γeJη
⎟
⎜Hx
⎟ ⎜
⎟ ⏟
⏞⏞
⏟
⎜
⎟ ⎜
⎜ (θ,ϕ,γ,η) ⎟ ⎜
( )2×1
cos θ ⎟
⎠
⎜H
⎟ ⎝ − cos ϕ sin θ
hγ,η ∈ C(J)
⎜ y
⎟
sin
ϕ
0
⎝
⎠
(θ,ϕ,γ,η)

Hz

(19)
Thus, (18) can be rewritten as

## PDF page 6

6

EURASIP Journal on Advances in Signal Processing

pθ,ϕ,γ,η =

⎧
⎪
⎪
⎪
⎪
⏞
⎪
⎪
⎪
(
⎪
⎨

(1)

(

Θθ,ϕ ∈ C(I)

)1×2

(2)

⏟⏟
⏞
)T
− sin θ − I · cos ϕ cos θ

⎪
cos ϕ cos θ − I · sin θ
⎪
⎪
⎪
⏟
⎪
⎪
⎪
⎪
⎩

⏞
(

dθ,ϕ = e

1 θ,ϕ /λ)

,...,e

]

J ·2π(kNT eθ,ϕ /λ) T

⏟⏟

⏞
)T

⏞⏞

,

)

⏟

⏟

⏞⏞

(1)

(

(22)

⏟

(3)

aθ,ϕ,γ,η

where “⊗” denotes the Kronecker product.
In the presence of M narrowband, far-field, and completely polarized signals, the quad-quaternion model of an
N-element EM vector-sensor array has the following form:
M
∑

am sm (t) + n(t)

m=1

=

M
∑

[(

)

(23)

]

[ ( )

( )]

M
∑

(26)

H
σm2 am am
+ Rn ,

3.2. Algorithm details
We first define the quad-quaternion array manifold Φ as the
continuum of steering vector aθ,ϕ,γ,η in the angular parameter
space of interest I1 and the polarization parameter space of
interest I2 . That is,
}

aθ,ϕ,γ,η , (θ, ϕ) ∈ I1 , (γ, η) ∈ I2 .

(24)

(27)

}

{

∥

∥}

θm , ϕm = arg min ∥ Pn aθ,ϕ,γ,η ∥ .
θ,ϕ,γ,η

where sm (t) ∈ C(J) is the complex envelop of the mth signal,
and n(t) is the additive noise term, and dm = dθm ,ϕm , pm =
pθm ,ϕm ,γm ,ηm , Θm = Θθm ,ϕm , hm = hγm ,ηm . It is assumed here
that (1) all the incident signals are uncorrelated; (2) the
noise is spatially white and uncorrelated with the signals;
(3) steering vectors corresponding to diﬀerent selections of
(θ, ϕ, γ, η) are right linearly independent.

{

(25)

where σm2 = E[sm (t)s∗m (t)] and Rn = E[n(t)nH (t)] = σn2 IN .
It can be easily proven according to Definition 14 that
the rank of A = [a1 , a2 , . . . , aM ] is M, then in the absence
2
])AAH is M,
of noise, the rank of Rx = diag([σ12 , σ22 , . . . , σM
and the column vectors of Rx span the signal subspace Rs . In
the presence of noise, we apply an M-rank approximation
of Rx to estimate the bases of signal subspace. According
to Lemma 7, we know that the best M-rank approximation
of Rx has 4M eigenvalues, thus we can use the eigenvectors
v1 , . . . , v4M associated with the largest 4M eigenvalues as the
bases of signal subspaces. Denote Es = [v1 , . . . , v4M ] and En =
[v4M , . . . , v4N ], then Rs = span(Es ) and Rn = span(En ).
N ×N
, we have ∥Pn am ∥ = 0,
Further, define Pn = En EH
n ∈ HH
then
{

Θm ⊗ dm · hm · sm (t) + n(t),

m=1

Φ ≜

(20)

)

R x = E x tl x H tl ,

m=1

+ Θ(3)
θ,ϕ ⊗ dθ,ϕ hγ,η · k,

x(t) =

· hγ,η .

Define the covariance matrix with quad-quaternion entries
as

⏟

aθ,ϕ,γ,η

⏞⏞

⎪
⎪
⎪
⏟⎪
⎪
⎪
⎪
⎪
⎭

Rn = R⊥s .

Rx =

)

⏟

·k

where “E” denotes expectation. From (23),

(2)

aθ,ϕ,γ,η

⏞

T

(

)
( (2)
)
Θ(1)
θ,ϕ ⊗ dθ,ϕ hγ,η · i + Θθ,ϕ ⊗ dθ,ϕ hγ,η · j
⏞⏞

⏟⏟

I · sin ϕ
· j+
− sin ϕ

⎫
⎪
⎪
⎪
⎪
⎪
⎪
⎪
⎪
⎬

Rs = span a1 , . . . , aM ,

(
⏟

⏞

)1×2

Moreover, the signal subspace and noise subspace in quadquaternion case are defined as follows:

(21)

aθ,ϕ,γ,η = pθ,ϕ,γ,η dθ,ϕ = Θθ,ϕ ⊗ dθ,ϕ hγ,η
=

(

(3)

Θθ,ϕ ∈ C(I)

Θθ,ϕ ∈H1C×2

where kn is the position vector of the nth EM vector sensor,
eθ,ϕ is the propagation vector corresponding to (θ, ϕ), λ is the
wavelength of incident signals. The steering vector of such an
N-element EM vector-sensor array then can be expressed as
(

)1×2

cos θ − I · cos ϕ sin θ
·i+
cos ϕ sin ϕ + I · cos ϕ

For an array of N EM vector sensors, the spatial steering
vector dθ,ϕ is given by
[ J ·2π(kT e

(

Θθ,ϕ ∈ C(I)

(28)

In the presence of finite data length, Rx can be estimated
as follows:
1∑
x(tl )xH (tl ).
L l=1
L

R̃x =

(29)

Accordingly, En and Pn can be estimated by eigendecomposing R̃x .
A question of fundamental interests is whether the
indetermination of quad-quaternion eigenvectors impacts
the results of MUSIC. According to Lemma 8, the indetermination of eigenvectors does not impact the vector space
spanned by them, and thus does not impact the estimation
of noise subspace. Since the performance of MUSIC-like
algorithms is mainly dependent on the accuracy of subspace
estimation, the indetermination of eigenvectors does not
impact the results of quad-quaternion MUSIC.

## PDF page 7

Xiaofeng Gong et al.

7
z

3.3. Decoupling of angular and polarization
parameters

ϕ

According to (28), a 4D search is required for DOA
estimation, which might be computationally prohibitive.
We next discuss how to decouple polarization from DOA
estimation for the purpose of reducing the computational
burden. Firstly, we prove the following lemma.

y
x
θ

M ×1

, L ∈ {i, j, k, I, J, K } and a
Lemma 9. Given h ∈ (C(L) )
Hermitian matrix F ∈ (HH )M ×M , then S(hH Fh) = hH S(F |
{1, L})h. Here, S(hH Fh) and S(F | {1, L}) denote the scalar
part of hH Fh and the {1, L}-match of F, respectively.
Proof. Without loss of generality, we assume L = J. Hence,
M ×1
. Let further F = (F00 + IF01 ) + i(F10 + IF11 ) +
h ∈ (C(J) )
j(F20 + F21 ) + k(F30 + F31 ), then S(F | {1, J }) = F00 . Since
FH = F, we have FH
00 = F00 . Then it is further obtained that
( H

)

[ H(

)

(

)

(

)

(

) ]

S h Fh = S h

F00 + IF01 + i F10 + IF11

)
(
)
= S h F00 h = hH F00 h = hH S F | {1, J } h.

(30)
We use the above-mentioned lemma to discuss the
decoupling of angular and polarization parameters. Let u =
×1)
Pn aθ,ϕ,γ,η ∈ H(N
, then
H
√ (

∥
∥
)
∥Pn aθ,ϕ,γ,η ∥ = S uH u .

(31)

According to (23), and denote Ξθ,ϕ = Pn · Θθ,ϕ ⊗ dθ,ϕ , then
we have the following equation from Lemma 9:
(

)

(

)

H
H
H
S uH u = S hH
γ,η Ξθ,ϕ Ξθ,ϕ hγ,η = hγ,η S Ξθ,ϕ Ξθ,ϕ | {1, J } hγ,η .
(32)
H
Note further that hH
γ,η hγ,η = 1 and S(Ξθ,ϕ Ξθ,ϕ | {1, J }) is
a complex-valued Hermitian matrix, then according to the
Rayleigh-Ritz theorem [11], we obtain

( hH S(ΞH Ξ | {1, J })h )
∥
∥
γ,η
γ,η
θ,ϕ θ,ϕ
min ∥Pn aθ,ϕ,γ,η ∥ = min

θ,ϕ,γ,η

θ,ϕ,γ,η

Step 4. then the DOA estimates are obtained by
{

(

)}

(θ,ϕ)∈I1

+ j F20 + F21 + k F30 + F31 h

)

Step 3. given an arbitrary (θ, ϕ) ∈ I1 , calculate Ξθ,ϕ = Pn ·
Θθ,ϕ ⊗ dθ,ϕ and S(ΞH
θ,ϕ Ξθ,ϕ | {1, J }).

arg min λmin Fθ,ϕ

( H

(

Figure 2: Coordinate system and angle definition.

hH
γ,η hγ,η

( (
))
= λmin S ΞH
θ,ϕ Ξθ,ϕ | {1, J } ,

(33)
where λmin (S(ΞH
θ,ϕ Ξθ,ϕ | {1, J })) denotes the smallest eigenH
value of S(Ξθ,ϕ Ξθ,ϕ | {1, J }). Thus, the 4D search problem is
reduced to a 2D search.
For clarity, we finally summarize the above split method
(termed as QQ-MUSIC) as follows:
Step 1. calculate the sampled covariance matrix R̃x according
to (29);
Step 2. apply the quad-quaternion EVD to R̃x , select the
4(N − M) eigenvectors associated to the smallest 4(N − M)
eigenvalues, and calculate the noise subspace projector Pn ;

.

(34)

It is important to note that QQ-MUSIC cannot fulfill simultaneous estimation of DOA and polarization.
The problem of polarization estimation or joint DOApolarization estimation remains unresolved and is currently
under investigation by the authors.
3.4.

Computation complexity

In this section, the computational complexity of QQMUSIC, BQ-MUSIC, and long-vector MUSIC is addressed.
As addressed in [36, 37], the covariance matrix estimation
best illustrates the complexity diﬀerence of the three algorithms, therefore we only consider the computational complexity involved in this part. The evaluation of computational
complexity includes two aspects: memory requirement and
number of real number additions (A), multiplications (M),
and divisions (D).
Assume that the array comprises N complete EM vector
sensors, and T snapshot vectors are available. The quadquaternion array output X ∈ (HH )N ×T then is given by
)

(

(

)

X = X0 +IX1 = iX01 + jX02 +kX03 +I iX11 + jX12 +kX13 ,
(35)
N ×T

,
where X0 , X1 ∈ (HC(J) )N ×T , and X0n , X1n ∈ (C(J) )
n = 1, 2, 3. Then the biquaternion data model (Xb ∈
(HC(J) )2N ×T ) and the long-vector data model (Xlv ∈
6N ×T
(C(J) )
) for the same array output are, respectively,
written as
[

Xb = X0T , X1T

]T

,

[

]T

T
T
T
T
T
T
Xlv = X01
, X02
, X03
, X11
, X12
, X13
.
(36)

Moreover, the sampled covariance matrices in the three
models can be calculated as follows:
1
1
1
R̃Q = XXH ,
R̃B = Xb XbH ,
R̃LV = Xlv XlvH ,
T
T
T
(37)

## PDF page 8

8

EURASIP Journal on Advances in Signal Processing
Table 2: Computational eﬀort for covariance estimation.

QQ-MUSIC
BQ-MUSIC
LV-MUSIC

Memory requirements (complex values)
8N 2
16N 2
36N 2

where R̃Q , R̃B , R̃LV are sampled covariance matrices used in
QQ-MUSIC, BQ-MUSIC, and LV-MUSIC, respectively.
From (37), R̃Q has N 2 entries, each of which is quadquaternion valued and can be represented by eight complex
numbers. Therefore, a memory of at least 8N 2 complex
numbers is required in the quad-quaternion case. Similarly,
for biquaternion and long-vector models, 16N 2 and 36N 2
complex numbers are required, respectively.
Let us now evaluate the total number of basic arithmetic
operations needed for estimation of the covariance matrix.
As revealed by (37), every entry of R̃Q is obtained by T
quad-quaternion multiplications, T − 1 quad-quaternion
additions, and a division by a real value. Note that one quadquaternion multiplication implies 162 real multiplications
plus 16 × 15 real additions, one quad-quaternion addition
implies 16 real additions, and the division by a real value
equals 16 real divisions.
The number
[
] of operations needed
for one entry is 162(M) + 16 × 15(A) T + 16(T − 1)(A) + 16(D) ,
where subscripts “(M),” “(A),” “(D)” denote real multiplication, real addition, and real division, respectively. Thus, the
total number is {[162(M) +16 × 15(A) ]T +16(T − 1)(A) +16(D) }·
2
2
N 2 = 256N 2 T(M) + (256T − 16)N(A)
+ 16N(D)
. Similarly,
the total numbers of arithmetic operations in biquaternion
and long-vector models are given by 256N 2 T(M) + (256T −
2
2
2
32)N(A)
+ 32N(D)
and 144N 2 T(M) + (144T − 72)N(A)
+
2
72N(D) , respectively. Table 2 summarizes the covariance
matrix computational eﬀorts for all the three algorithms.
We can see that QQ-MUSIC largely reduces the memory
requirements, mainly due to the more economical formulism
of quad-quaternion model. In addition, with regard to
basic arithmetic operation number, we can see that QQMUSIC requires 16N 2 less real divisions and 16N 2 more
real additions than BQ-MUSIC. Since the computational
complexity of divisions is much more than that of additions,
QQ-MUSIC slightly outperforms BQ-MUSIC in this aspect.
We may also note that LV-MUSIC requires least operations
for estimating the covariance matrix, which conflicts our
intuition that a more concise model should lead to less
computational complexity. This fact can be explained as
follows. In QQ-MUSIC, we are using a 16D algebra to model
six-component vector sensors, and only twelve imaginary
units of quad-quaternions are used in this formulation.
Therefore, this insuﬃcient use of quad-quaternions results
in more arithmetic operations.

Real multiplications
256N 2 T
256N 2 T
144N 2 T

Real additions
(256T − 16)N 2
(256T − 32)N 2
(144T − 72)N 2

Real divisions
16N 2 (D)
32N 2 (D)
72N 2 (D)

Consider two quad-quaternion vectors x, y ∈ (HH )Nx ×1
given by
(

)

(

)

(

)

(

)

(

)

(

)

x = x01 + Ix11 i + x02 + Ix12 j + x03 + Ix13 k,

(38)

y = y01 + Iy11 i + y02 + Iy12 j + y03 + Iy13 k.

The corresponding biquaternion representation and complex representation then can be written as
[

T
T
, x11
xbq = x01

]T

[

T
T
, x12
i + x02

]T

[

T
T
, x13
j + x03

]T

,

( )2N ×1
k ∈ HC x ,
[

T
T
, y11
ybq = y01

]T

[

T
T
, y12
i + y02

]T

[

T
T
, y13
j + y03

]T

,

( )2N ×1
k ∈ HC x ,
[

]T

(
)6Nx ×1
∈ C(J)
,

[

]T

)6Nx ×1
(
∈ C(J)
.

T
T
T
T
T
T
, x11
, x02
, x12
, x03
, x13
xc = x01
T
T
T
T
T
T
, y11
, y02
, y12
, y03
, y13
yc = y01

(39)
Imposing the orthogonal constraint on quad-quaternion
vectors (xH y = 0) yields
H
H
H
H
H
H
x01
y01 + x11
y11 + x02
y02 + x12
y12 + x03
y03 + x13
y13 = 0,
T
T
T
T
T
T
x01
y11 − x11
y01 + x02
y12 − x12
y02 + x03
y13 − x13
y03 = 0,
H
H
H
H
x02
y03 + x12
y13 − x03
y02 − x13
y12 = 0,
T
T
T
T
x02
y13 − x12
y03 − x03
y12 + x13
y02 = 0,
H
H
H
H
x03
y01 + x13
y11 − x01
y03 − x11
y13 = 0,
T
T
T
T
x03
y11 − x13
y01 − x01
y13 + x11
y03 = 0,
H
H
H
H
x01
y02 + x11
y12 − x02
y01 − x12
y11 = 0,
T
T
T
T
x01
y12 − x11
y02 − x02
y11 + x12
y01 = 0.

(40)
In contrast, orthogonal constraint on biquaternion vectors
H
(xbq
ybq = 0) results in
H
H
H
H
H
H
y01 + x11
y11 + x02
y02 + x12
y12 + x03
y03 + x13
y13 = 0,
x01
H
H
H
H
x02
y03 + x12
y13 − x03
y02 − x13
y12 = 0,
H
H
H
H
x03
y01 + x13
y11 − x01
y03 − x11
y13 = 0,
H
H
H
H
x01
y02 + x11
y12 − x02
y01 − x12
y11 = 0.

(41)

3.5. Orthogonality-measure comparison
As addressed in [37], vector orthogonality in higher dimensional algebra imposes stronger constraints on vector components. In this part, we take a further look into the quadquaternion-related orthogonality.

Moreover, the orthogonal constraint on complex vectors
(xcH yc = 0) leads to
H
H
H
H
H
H
y01 + x11
y11 + x02
y02 + x12
y12 + x03
y03 + x13
y13 = 0.
x01

(42)

## PDF page 9

Xiaofeng Gong et al.

9

y
z

√

d × Pe

b

d
y

x

a

d
(a)
√

d × Pe

x
z

b

Norm of the loop
Actual sensor position
Ideal sensor position

y

Figure 3: An array with sensor position errors.

x

a

By comparing (40), (41) and (42), it is obtained that:
(b)
H
ybq = 0 =⇒ xcH yc = 0.
xH y = 0 =⇒ xbq

(43)

Consequently, the quad-quaternion orthogonality can
impose stronger constraints than both biquaternion and
complex algebra do. This property of quad-quaternions
results in a better robustness of QQ-MUSIC to model errors,
as to be demonstrated in Section 4.

Figure 4: A short dipole or loop with arbitrary orientation.

Sensor-position error
the positions of EM vector sensors are not precisely known.
In the simulations, we model such sensor position error by
additive uniformly distributed noise, that is,
√

[

]T

k n = kn + Pe · d · εx , ε y , 0 ,
4.

SIMULATION RESULTS

In this section, simulation results are provided to compare
the proposed QQ-MUSIC with both biquaternion-based
(such as BQ-MUSIC) and complex-based methods (such
as LV-MUSIC) for six-component EM vector-sensor arrays.
It should be noted that BQ-MUSIC was actually proposed
for three-component vector-sensor arrays [37]. Therefore,
we here use a 2 × 1 biquaternion vector to represent a
six-component vector sensor, and further we concatenate
these vectors into a biquaternion long-vector to enable BQMUSIC.
We compare the proposed QQ-MUSIC with BQ-MUSIC,
LV-MUSIC, and polarimetric smoothing algorithm (PSAMUSIC [30]), in terms of robustness to model errors
and DOA estimation performance under diﬀerent levels of
signal-to-noise ratio (SNR). All the statistics shown here are
computed by averaging the results of 200 independent trials.
The array used here is an L-shaped array that comprises
four and five EM vector sensors along the x-axis and y -axis,
respectively (see Figure 3). The spacing between two adjacent
EM vector sensors is d = λ/2. Before representing the results,
we introduce the following two model errors.

(44)

where k n and kn are the actual and ideal position coordinates
of the nth EM vector sensor, respectively, εx and ε y are
uniformly distributed noise terms, and Pe is the power of
sensor position error.
Sensor-orientation error
the orientation angles of a dipole and a loop are illustrated
in Figure 4. With an orientation angle (α, β), where α ∈
[0, 2π), β ∈ [0, π/2], the outputs of a dipole and a loop are,
respectively, given by
(θ,ϕ,γ,η)

Eα,β

= [cos α sin β, sin α sin β, cos β]
[ (θ,ϕ,γ,η) (θ,ϕ,γ,η) (θ,ϕ,γ,η) ]
· Ex
, Ey
, Ez
T,

(θ,ϕ,γ,η)

Hα,β

(45)

= [cos α sin β, sin α sin β, cos β]
[ (θ,ϕ,γ,η) (θ,ϕ,γ,η) (θ,ϕ,γ,η) ]
· Hx
, Hy
, Hz
T,

(θ,ϕ,γ,η)

(θ,ϕ,γ,η)

(θ,ϕ,γ,η)

(θ,ϕ,γ,η)

(θ,ϕ,γ,η)

where Ex
, Ey
, Ez
, and Hx
, Hy
,
(θ,ϕ,γ,η)
Hz
are given in (23). Let the orientation angles of

## PDF page 10

10

EURASIP Journal on Advances in Signal Processing

the three dipoles of the nth EM vector sensor be (α1,n , β1,n ),
(α2,n , β2,n ), and (α3,n , β3,n ), while the orientation angles of the
three loops be (α4,n , β4,n ), (α5,n , β5,n ), and (α6,n , β6,n ), then we
have
[

]

[

]

√ [

]

αl,n , βl,n = αl , βl + Pe εα,l,n , εβ,l,n ,

(46)

l = 1, . . . , 6; n = 1, . . . , N,

p(n)
θ,ϕ,γ,η =

where Pe is the power of the sensor orientation error,
εα,l,n , εβ,l,n are uniformly distributed noise terms, (α1 , β1 ) =
(α4 , β4 ) = (0, π/2), (α2 , β2 ) = (α5 , β5 ) = (π/2, π/2),
(α3 , β3 ) = (α6 , β6 ) = (0, 0) are the corresponding nominal
orientation angles in the absence of sensor orientation error.
Combining (22), (23), (45), and (46), the output of the nth
EM vector sensor equals

(
(
)
(
)
)⎞T
{ ⎛cos ε
β,1,n sin εα,1,n − ϕ − I · sin εβ,4,n sin θ − cos εα,4,n − ϕ cos εβ,4,n cos θ
⎝
⎠ ·i
(
)
(
)
cos εβ,1,n cos θ cos εα,1,n − ϕ + sin εβ,1,n sin θ + I · cos εβ,4,n sin εα,4,n − ϕ
⎛

+⎝
⎛

+⎝

(

)

(

(

(

)

(

(

)

(

(

(

)

T

x(t) =

T

)⎞T

aθm ,ϕm ,γm ,ηm sm (t) + n(t).

In the first experiment, we assume that only the sensor
position error exists. Three uncorrelated signals are from
(θ1 , ϕ1 ) = (8◦ , 90◦ ), (θ2 , ϕ2 ) = (35◦ , 90◦ ), and (θ3 , ϕ3 ) =
(60◦ , 90◦ ) (to exclude the eﬀect of DOA ambiguity on the
comparison, we here only consider azimuth angle estimation), respectively, with polarizations (γ1 , η1 ) = (45◦ , 0◦ ),
(γ2 , η2 ) = (45◦ , 90◦ ), and (γ3 , η3 ) = (45◦ , 180◦ ), respectively.
The sensor noise is assumed to be Gaussian white and
uncorrelated with the incident signals. The overall root mean
square error (RMSE) performance measure used here is
defined as follows:
‾
│ N
)2 ]
│ 1 ∑s [(
⎷
θm − θ̃n,m ,

1
M m=1 N n=1

(47)

}
· hγ,η .

1.4
1.2

]

(48)

ε=

⎠ ·j

⎠ ·k
)

(

m=1

M │
∑

)⎞T

sin εβ,3,n cos θ cos εα,3,n − ϕ − cos εβ,3,n sin θ + I · sin εβ,6,n sin εα,6,n − ϕ

J ·2π(kN eθ,ϕ /λ) T,
pθ,ϕ,γ,η eJ ·2π(k1 eθ,ϕ /λ) , . . . , p(N)
θ,ϕ,γ,η e
M
∑

)

sin εβ,3,n sin εα,3,n − ϕ + I · cos εβ,6,n sin θ − cos εα,6,n − ϕ sin εβ,6,n cos θ

Overall RMSE (degree)

[ (1)

)

cos εβ,2,n cos θ sin ϕ − ε1,2,n + sin εβ,2,n sin θ + I · cos εβ,5,n cos εα,5,n − ϕ

Accordingly, the quad-quaternion expressions of the steering
vector and the array output can be, respectively, modified as
aθ,ϕ,γ,η =

)

cos εβ,2,n cos εα,2,n − ϕ − I · sin εβ,5,n sin θ − sin εα,5,n − ϕ cos εβ,5,n cos θ

1
0.8
0.6
0.4
0.2
0

0

0.01

0.02

0.03

0.04

0.05

0.06

0.07

Power of sensor-position error
QQ-MUSIC
BQ-MUSIC

LV-MUSIC
PSA-MUSIC

Figure 5: RMS estimation errors versus sensor position error
power.

(49)

where θ̃n,m is the estimate of true azimuth angle θm in the
nth trial. It is plotted in Figure 5 that the curves of overall
RMSE against sensor position error power for QQ-MUSIC,
BQ-MUSIC, LV-MUSIC, and PSA-MUSIC wherein the SNR
and the number of snapshots are fixed as 30 dB and 1000,
respectively. It can be seen that QQ-MUSIC provides the best
estimation accuracy in the presence of sensor position error.
In the second experiment, we assume that only the sensor
orientation error exists. The DOAs and polarizations of the
incident signals are the same as the first example. The overall
RMSE curves of QQ-MUSIC, BQ-MUSIC, LV-MUSIC, and

PSA-MUSIC against the power of sensor orientation error
are plotted in Figure 6, wherein the SNR is constantly 30 dB.
We can see that QQ-MUSIC shows better robustness to
sensor orientation error than BQ-MUSIC and LV-MUSIC.
In particular, when the power of sensor orientation error is
high, QQ-MUSIC can still provide reliable DOA estimates. It
can also be observed that the performance of PSA-MUSIC
is independent of the senor orientation error. This can be
explained by noting that PSA-MUSIC does not preserve the
polarization information, and thus is independent of the
model error in the polarization dimension.

## PDF page 11

Xiaofeng Gong et al.

11
5

7

4.5

6
Overall RMSE (degree)

Overall RMSE (degree)

4
5
4
3
2

3.5
3
2.5
2
1.5

1
0

1
0

1

2

3
4
5
6
7
8
Power of sensor-orientation error

QQ-MUSIC
BQ-MUSIC

9

−10

LV-MUSIC
PSA-MUSIC

1

12
Overall RMSE (degree)

14

0.8
0.6
0.4
0.2
0

−6

−4

−2

0
2
SNR (dB)

4

6

8

10

LV-MUSIC
PSA-MUSIC

Figure 8: RMS estimation errors versus SNR in the presence of
sensor position errors.

1.2

−10

−8

QQ-MUSIC
BQ-MUSIC

Figure 6: RMS estimation errors versus the power of sensor
orientation error.

Overall RMSE (degree)

0.5

10

10
8
6
4
2

−8

−6

−4

QQ-MUSIC
BQ-MUSIC

−2

0
2
SNR (dB)

4

6

8

10

LV-MUSIC
PSA-MUSIC

0

−10

−8

−6

−4

QQ-MUSIC
BQ-MUSIC

−2

0
2
SNR (dB)

4

6

8

10

LV-MUSIC
PSA-MUSIC

Figure 7: RMS estimation errors versus SNR for an ideal EM
vector-sensor array.

Figure 9: RMS estimation errors versus SNR in the presence of
sensor orientation errors.

We next compare the performance of QQ-MUSIC with
BQ-MUSIC, LV-MUSIC, and PSA-MUSIC with respect to
SNR. The DOAs and polarizations are the same as the first
two examples. The SNR is varied between −10 dB and 10 dB.
Three cases are considered (1) in the absence of model error;
(2) in the presence of sensor position error only, and the
error power is Pe = 0.05; (3) in the presence of sensor
orientation error only, with model error power Pe = 5.
The results are given in Figures 7–9. From Figure 7, in a
model error-free case, QQ-MUSIC and BQ-MUSIC are a
bit inferior to LV-MUSIC and PSA-MUSIC. From Figure 8,
we can see that QQ-MUSIC outperforms BQ-MUSIC, LV-

MUSIC, and PSA-MUSIC at all levels of SNR, in the
presence of sensor position errors; from Figure 9, we see that
QQ-MUSIC outperforms LV-MUSIC and PSA-MUSIC in
sensor orientation errors, while slightly underperforms PSAMUSIC because the performance of the latter is independent
of sensor orientation errors.
Then, we consider the case of several incident signals with
close DOAs and polarizations. An “L”-shaped array with 20
complete EM vector sensors is used, and six incident signals
are assumed to be impinging, among which the first and
the second signals, the third and the fourth signals, and the
fifth and the sixth signals are close to each other in both

## PDF page 12

12

EURASIP Journal on Advances in Signal Processing
100

QQ-MUSIC (dB)

10−1

10−2

10−3

10−4
10

20

30
40
50
Azimuth angle (degree)

60

70

Figure 10: QQ-MUSIC spectrum in the presence of several close
signals; SNR=30 dB, the number of snapshots is 100.

100

BQ-MUSIC (dB)

10−1

10−2

10−3

10−4
10

angular and polarization domains: (θ1 , ϕ1 ) = (18◦ , 90◦ ),
(θ2 , ϕ2 ) = (20◦ , 90◦ ), (θ3 , ϕ3 ) = (40◦ , 90◦ ), (θ4 , ϕ4 ) =
(41◦ , 90◦ ), (θ5 , ϕ5 ) = (65◦ , 90◦ ), and (θ6 , ϕ6 ) = (67◦ , 90◦ );
(γ1 , η1 ) = (γ2 , η2 ) = (γ3 , η3 ) = (γ4 , η4 ) = (γ5 , η5 ) =
(γ6 , η6 ) = (0◦ , 0◦ ) (to exclude the eﬀect of DOA ambiguity
on the comparison, we here only consider azimuth angle
estimation). In addition, we assume that no model error
exists for the above-mentioned array, the SNR is 30 dB,
and the number of snapshots is 100. The spectra of QQMUSIC, BQ-MUSIC, and LV-MUSIC are given in Figures
11-12, in which the dotted lines indicate the true azimuth
angles. We note that both BQ-MUSIC and LV-MUSIC fail
to distinguish the third and the fourth signals, while QQMUSIC can successfully distinguish all the six sources with
considerable accuracy.
5.

CONCLUSIONS

In this paper, we have proposed a new DOA estimator,
termed as quad-quaternion MUSIC (QQ-MUSIC), for sixcomponent EM vector-sensor arrays. This new MUSIC variant has employed a newly developed quad-quaternion model
that provides a less memory-consuming way to deal with
six-component EM vector-sensor outputs. Moreover, with
sensor position error or sensor orientation error present,
QQ-MUSIC has been shown to be able to oﬀer better DOA
estimation accuracy than both biquaternion-MUSIC (BQMUSIC) and long-vector MUSIC (LV-MUSIC). Thus, QQMUSIC may be more attractive than the examined methods
in many practical situations, where model errors cannot be
ignored.
APPENDIX

20

30
40
50
Azimuth angle (degree)

60

70

Figure 11: BQ-MUSIC spectrum in the presence of several close
signals; SNR=30 dB, the number of snapshots is 100.

100

PROOFS OF LEMMAS 5–8 IN SECTION 2
Proof of Lemma 5. If we denote conj(Q | Γ3 ) = conj((conj(Q
| Γ1 )) | Γ2 ), then by definition, Γ3 is a set consisting of
the bases whose coeﬃcients are not inversed. Obviously, the
coeﬃcients of bases in Γ1 ∩ Γ2 are not inversed, and the
coeﬃcients of bases in (Γ1 ∪ Γ2 )⊥ are inversed twice so that
they are also not inversed. Therefore, Γ3 = (Γ1 ∩ Γ2 ) ∪
(Γ1 ∪ Γ2 )⊥ .

LV-MUSIC (dB)

10−1

Proof of Lemma 6. Without loss of generality, here we only
consider the case of right rank. Assume the right rank of
P ∈ (HH )M ×N is R, then by definition there exists a set of
R column vectors q1 , q2 , . . . , qR of P and R quad-quaternion
scalars λ1 , λ2 , . . . , λR , such that

10−2

10−3

q1 λ1 +q2 λ2 + · · · +qR λR = oM ×1 ⇐⇒ λ1 = λ2 = · · · = λR = 0.
(A.1)

10−4
10

20

30
40
50
Azimuth angle (degree)

60

70

Figure 12: LV-MUSIC spectrum in the presence of several close
signals; SNR = 30 dB, the number of snapshots is 100.

Moreover, for an arbitrary nonzero column vector qR+1 of P,
there exist R + 1 quad-quaternion scalars μ1 , μ2 , . . . , μR , μR+1
not all zero, such that
q1 μ1 + q2 μ2 + · · · + qR μR + qR+1 μR+1 = oM ×1 .

(A.2)

## PDF page 13

Xiaofeng Gong et al.

13

According to Lemma 1 and (A.1) and (A.2), we have

REFERENCES

χ q1 χ λ1 + χ q2 χ λ2 + · · · + χ qR χ λR
= O2M ×2 ⇐⇒ λ1 = λ2 = · · · = λR = 0,

χ q1 χ μ1 + χ q2 χ μ2 + · · · + χ qR χ μR + χ qR+1 χ μR+1 = O2M ×2 ,
(A.3)
where χ qn ∈ (HC(J) )2M ×2 and χ λn , χ μn ∈ (HC(J) )2×2 are
the adjoint matrices of qn , λn and μn , respectively, n =
1, 2, . . . , R, R + 1. We further denote χ qn = [χ n,0 , χ n,1 ], λn =
λn,0 + Iλn,1 , and μn = μn,0 + Iμn,1 , then χ 1,0 , χ 1,1 , . . . , χ R,0 , χ R,1
are column vectors of χ P . According to the definition of
adjoint matrices and (A.3), we have
R
∑
(
n=1

χ n,0 λn,0 − χ n,1 λn,1

)

= o2M ×1 ⇐⇒ λ1,0 = λ1,1 = · · · = λR,0 = λR,1 = 0,

(A.4)
R+1
∑

(

n=1
R+1
∑
n=1

)

χ n,0 μn,0 − χ n,1 μn,1 = o2M ×1 ,

(

∗

∗

(A.5)

)

χ n,0 μn,1 + χ n,1 μn,0 = o2M ×1 .

Since μ1 , μ2 , . . . , μR , μR+1 are not all zero, without loss of
generality, we assume μR+1 = μR+1,0 + iμR+1,1 =
/ 0, and further
0.
Then,
we
have
from
(A.5)
that
assume μR+1,1 =
/
(

−1
μ∗R+1,0 + μ∗R+1,1
χ R+1,0 μR+1,1

+

R
∑
[
n=1

(

)

−1
χ n,0 μn,0 μR+1,1
μ∗R+1,0 + μ∗n,1

)

(
)]
−1
μ∗R+1,0 − μ∗n,0 = o2M ×1 .
− χ n,1 μn,1 μR+1,1

(A.6)
From (A.4) and (A.6), we see that χ 1,0 , χ 1,1 , . . . , χ R,0 , χ R,1
consist a maximal right linearly independent set, therefore
the right rank of χ P is 2R.
Proof of Lemma 7. According to Lemma 6, rank(Q) =
1/2 rank(χ Q ), where Q is a Hermitian quad-quaternion
matrix that can be eigenvalue decomposed as Q = UDUH .
χ Q is the adjoint biquaternion matrix of Q. According to
Lemma 2, χ Q is also Hermitian. Then according to [37,
Definition 6], we have
( ) 1
1
rank(Q) = rank χ Q = rank(D).
2
4

(A.7)

Proof of Lemma 8. is directly obtained from Definition 15.

ACKNOWLEDGMENT
This work was supported in part by the National Natural
Science Foundation of China under Contracts no. 60672084,
no. 60602037, and no. 60736006.

[1] R. T. Compton Jr., “The tripole antenna: an adaptive array
with full polarization flexibility,” IEEE Transactions on Antennas and Propagation, vol. 29, no. 6, pp. 944–952, 1981.
[2] J. Li, “Direction and polarization estimation using arrays with
small loops and short dipoles,” IEEE Transactions on Antennas
and Propagation, vol. 41, no. 3, pp. 379–387, 1993.
[3] A. Nehorai and E. Paldi, “Vector-sensor array processing for
electromagnetic source localization,” IEEE Transactions on
Signal Processing, vol. 42, no. 2, pp. 376–398, 1994.
[4] K. T. Wong, “Direction finding/polarization estimation-dipole
and/or loop triad(s),” IEEE Transactions on Aerospace and
Electronic Systems, vol. 37, no. 2, pp. 679–684, 2001.
[5] J. Tabrikian, R. Shavit, and D. Rahamim, “An eﬃcient vector
sensor configuration for source localization,” IEEE Signal
Processing Letters, vol. 11, no. 8, pp. 690–693, 2004.
[6] I. Ziskind and M. Wax, “Maximum likelihood localization
of diversely polarized sources by simulated annealing,” IEEE
Transactions on Antennas and Propagation, vol. 38, no. 7, pp.
1111–1114, 1990.
[7] A. J. Weiss and B. Friedlander, “Maximum likelihood signal
estimation for polarization sensitive arrays,” IEEE Transactions
on Antennas and Propagation, vol. 41, no. 7, pp. 918–925, 1993.
[8] J. Li and P. Stoica, “Eﬃcient parameter estimation of partially
polarized electromagnetic waves,” IEEE Transactions on Signal
Processing, vol. 42, no. 11, pp. 3114–3125, 1994.
[9] H. Lee and R. Stovall, “Maximum likelihood methods for
determining the direction of arrival for a single electromagnetic source with unknown polarization,” IEEE Transactions
on Signal Processing, vol. 42, no. 2, pp. 474–479, 1994.
[10] R. O. Schmidt, A signal subspace approach to emitter location
and spectral estimation, Ph.D. dissertation, Stanford University, Stanford, Calif, USA, 1981.
[11] E. R. Ferrara Jr. and T. M. Parks, “Direction finding with
an array of antennas having diverse polarizations,” IEEE
Transactions on Antennas and Propagation, vol. 31, no. 2, pp.
231–236, 1983.
[12] Y. Hua, “A pencil-MUSIC algorithm for finding twodimensional angles and polarizations using crossed dipoles,”
IEEE Transactions on Antennas and Propagation, vol. 41, no. 3,
pp. 370–376, 1993.
[13] A. J. Weiss and B. Friedlander, “Direction finding for diversely
polarized signals using polynomial rooting,” IEEE Transactions
on Signal Processing, vol. 41, no. 5, pp. 1893–1905, 1993.
[14] K. T. Wong and M. D. Zoltowski, “Self-initiating MUSICbased direction finding and polarization estimation in spatiopolarizational beamspace,” IEEE Transactions on Antennas and
Propagation, vol. 48, no. 8, pp. 1235–1245, 2000.
[15] K. T. Wong, L. Li, and M. D. Zoltowski, “Root-MUSIC-based
direction-finding and polarization estimation using diversely
polarized possibly collocated antennas,” IEEE Antennas and
Wireless Propagation Letters, vol. 3, no. 1, pp. 129–132, 2004.
[16] M. D. Zoltowski and K. T. Wong, “Closed-form
eigenstructure-based direction finding using arbitrary
but identical subarrays on a sparse uniform Cartesian array
grid,” IEEE Transactions on Signal Processing, vol. 48, no. 8, pp.
2205–2210, 2000.
[17] A. Swindlehurst and M. Viberg, “Subspace fitting with
diversely polarized antenna arrays,” IEEE Transactions on
Antennas and Propagation, vol. 41, no. 12, pp. 1687–1694,
1993.

## PDF page 14

14
[18] J. Li, P. Stoica, and D. Zheng, “Eﬃcient direction and polarization estimation with a COLD array,” IEEE Transactions on
Antennas and Propagation, vol. 44, no. 4, pp. 539–547, 1996.
[19] R. Roy and T. Kailath, “ESPRIT-estimation of signal parameters via rotational invariance techniques,” IEEE Transactions
on Acoustics, Speech and Signal Processing, vol. 37, no. 7, pp.
984–995, 1989.
[20] J. Li and R. T. Compton Jr., “Angle and polarization estimation
using ESPRIT with a polarization sensitive array,” IEEE
Transactions on Antennas and Propagation, vol. 39, no. 9, pp.
1376–1383, 1991.
[21] J. Li and R. T. Compton Jr., “Angle estimation using a
polarization sensitive array,” IEEE Transactions on Antennas
and Propagation, vol. 39, no. 10, pp. 1539–1543, 1991.
[22] J. Li and R. T. Compton Jr., “Two-dimensional angle and
polarization estimation using the ESPRIT algorithm,” IEEE
Transactions on Antennas and Propagation, vol. 40, no. 5, pp.
550–555, 1992.
[23] J. Li, “On polarization estimation using a crossed-dipole
array,” IEEE Transactions on Signal Processing, vol. 42, no. 4,
pp. 977–980, 1994.
[24] K. T. Wong and M. D. Zoltowski, “Uni-vector-sensor ESPRIT
for multisource azimuth, elevation, and polarization estimation,” IEEE Transactions on Antennas and Propagation, vol. 45,
no. 10, pp. 1467–1474, 1997.
[25] K. T. Wong and M. D. Zoltowski, “Closed-form direction
finding and polarization estimation with arbitrarily spaced
electromagnetic vector-sensors at unknown locations,” IEEE
Transactions on Antennas and Propagation, vol. 48, no. 5, pp.
671–681, 2000.
[26] M. D. Zoltowski and K. T. Wong, “ESPRIT-based 2-D direction finding with a sparse uniform array of electromagnetic
vector sensors,” IEEE Transactions on Signal Processing, vol. 48,
no. 8, pp. 2195–2204, 2000.
[27] K.-C. Tan, K.-C. Ho, and A. Nehorai, “Uniqueness study
of measurements obtainable with arrays of electromagnetic
vector sensors,” IEEE Transactions on Signal Processing, vol. 44,
no. 4, pp. 1036–1039, 1996.
[28] K.-C. Tan, K.-C. Ho, and A. Nehorai, “Linear independence
of steering vectors of an electromagnetic vector sensor,” IEEE
Transactions on Signal Processing, vol. 44, no. 12, pp. 3099–
3107, 1996.
[29] B. Hochwald and A. Nehorai, “Identifiability in array processing models with vector-sensor applications,” IEEE Transactions on Signal Processing, vol. 44, no. 1, pp. 83–95, 1996.
[30] D. Rahamim, J. Tabrikian, and R. Shavit, “Source localization
using vector sensor array in a multipath environment,” IEEE
Transactions on Signal Processing, vol. 52, no. 11, pp. 3096–
3103, 2004.
[31] Y. Zhang, B. A. Obeidat, and M. G. Amin, “Spatial polarimetric time-frequency distributions for direction-of-arrival
estimations,” IEEE Transactions on Signal Processing, vol. 54,
no. 4, pp. 1327–1340, 2006.
[32] Y. Xu and Z. Liu, “Polarimetric angular smoothing algorithm
for an electromagnetic vector-sensor array,” IET Radar, Sonar
& Navigation, vol. 1, no. 3, pp. 230–240, 2007.
[33] P. Chevalier, A. Ferréol, L. Albera, and G. Birot, “Higher
order direction finding from arrays with diversely polarized
antennas: the PD-2q-MUSIC algorithms,” IEEE Transactions
on Signal Processing, vol. 55, no. 11, pp. 5337–5350, 2007.
[34] Y. Wu, H. C. So, C. Hou, and J. Li, “Passive localization of
near-field sources with a polarization sensitive array,” IEEE
Transactions on Antennas and Propagation, vol. 55, no. 8, pp.
2402–2408, 2007.

EURASIP Journal on Advances in Signal Processing
[35] N. Le Bihan and J. I. Mars, “Singular value decomposition
of quaternion matrices: a new tool for vector-sensor signal
processing,” Signal Processing, vol. 84, no. 7, pp. 1177–1199,
2004.
[36] S. Miron, N. Le Bihan, and J. I. Mars, “Quaternion-MUSIC for
vector-sensor array processing,” IEEE Transactions on Signal
Processing, vol. 54, no. 4, pp. 1218–1229, 2006.
[37] N. Le Bihan, S. Miron, and J. I. Mars, “MUSIC algorithm for
vector-sensors array using biquaternions,” IEEE Transactions
on Signal Processing, vol. 55, no. 9, pp. 4523–4533, 2007.
[38] J. Ward, Quaternions and Cayley Numbers: Algebra and
Applications, Kluwer Academic Publishers, New York, NY,
USA, 1997.
[39] K. Imaeda and M. Imaeda, “Sedenions: algebra and analysis,”
Applied Mathematics and Computation, vol. 115, no. 2-3, pp.
77–88, 2000.
[40] T. Y. Lam, D. B. Leep, and J.-P. Tignol, “Biquaternion
algebras and quartic extensions,” Publications Mathématiques
de l’Institut des Hautes Études Scientifiques, vol. 77, no. 1, pp.
63–102, 1993.
[41] A. A. Albert, “A construction of non-cyclic normal division
algebras,” Bulletin of the American Mathematical Society, vol.
38, no. 6, pp. 449–456, 1932.
[42] T. Unger and N. Markin, “Quadratic forms and space-time
block codes from generalized quaternion and biquaternion
algebras,” http://arxiv.org/abs/0807.0199.
[43] W. R. Hamilton, “On a new species of imaginary quantities
connected with a theory of quaternions,” Proceedings of the
Royal Irish Academy, vol. 2, pp. 424–434, 1843.
