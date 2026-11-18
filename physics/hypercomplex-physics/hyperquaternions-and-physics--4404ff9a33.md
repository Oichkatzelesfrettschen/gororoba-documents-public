Source: https://doi.org/10.21468/SciPostPhysProc.14
PDF sha256: 4404ff9a333ea13e4c6a8af7b11f0d306f3b5bcf773cd34f852f7489a055e6d7
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine (failed: characters)

# Transcription of hyperquaternions-and-physics--4404ff9a33.pdf

Transcription of `hyperquaternions-and-physics--4404ff9a33.pdf` in this directory, 9 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-9 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

SciPost Phys. Proc. 14, 030 (2023)

Hyperquaternions and physics
Patrick R. Girard1⋆ , Romaric Pujol2 , Patrick Clarysse1 and Philippe Delachartre1
1 CREATIS, Université de Lyon, CNRS UMR5520, INSERM U1294, INSA-Lyon, France
2 Pôle de Mathématiques, INSA-Lyon, France
⋆ patrick.girard@creatis.insa-lyon.fr
34th International Colloquium on Group Theoretical Methods in Physics
Strasbourg, 18-22 July 2022
doi:10.21468/SciPostPhysProc.14

Abstract
The paper develops, within a new representation of Clifford algebras in terms of tensor
products of quaternions called hyperquaternions, several applications. The first application is a quaternion 2D representation in contradistinction to the frequently used 3D
one. The second one is a new representation of the conformal group in (1+2) space
(signature + − −) within the Dirac algebra C5 (2, 3) ≃C ⊗ H ⊗ H subalgebra of H ⊗ H ⊗ H.
A numerical example and a canonical decomposition into simple planes are given. The
third application is a classification of all hyperquaternion algebras into four types, providing the general formulas of the signatures and relating them to the symmetry groups
of physics.
Copyright P. R. Girard et al.
This work is licensed under the Creative Commons
Attribution 4.0 International License.
Published by the SciPost Foundation.

Received 18-11-2022
Accepted 11-08-2023
Check for
updates
Published 24-11-2023
doi:10.21468/SciPostPhysProc.14.030

Contents
1 Introduction

2

2 Preliminaries: Clifford algebras and hyperquaternions
2.1 Quaternions and biquaternions
2.2 Clifford algebras and hyperquaternions

2
2
2

3 Quaternion 2D representation

3

4 Hyperquaternionic conformal group in (1+2) space
4.1 Algebraic structure
4.2 Restricted conformal group
4.3 Numerical example

3
3
4
4

5 Classification of hyperquaternion algebras

5

6 Conclusion

7

A Multivector structure of C5 (2, 3)

8

References

8
030.1

## PDF page 2

SciPost Phys. Proc. 14, 030 (2023)

1

Introduction

A new hyperquaternionic representation of Clifford algebras [1, 2] has been introduced recently [3–7], hyperquaternion algebras being defined as tensor products of quaternion algebras (or subalgebra thereof). This paper develops several hyperquaternionic applications.
Throughout this paper, H⊗m will denote the tensor product of m quaternion algebras, i.e.
⊗m
H = H ⊗ H⊗ · · · ⊗H (m terms). The structure of the paper is as follows.
In the preliminaries, the historical origins and basic concepts of hyperquaternion Clifford
algebras are examined. In the third section, a quaternion 2D representation is proposed in contradistinction to a widely used 3D representation. In the fourth section, the conformal group
of the (1 + 2) space (signature +−−) is developed within the Dirac algebra C5 (2, 3) ≃ C ⊗ H⊗2
considered as a subalgebra of H⊗3 ≃ C6 (2, 4) . The choice of the (1 + 2) space is motivated by
its use in quantum gravity [8]. A numerical example together with a canonical decomposition
into simple planes is provided. Finally, the fifth section gives a classification of all hyperquaternion algebras into four types with general formulas of the signatures and associated symmetry
groups of physics.

2

Preliminaries: Clifford algebras and hyperquaternions

2.1

Quaternions and biquaternions

The quaternion group [9, 10] was discovered in 1843 by W. R. Hamilton and is constituted by
the elements (±1, ±i, ± j, ±k) satisfying the formula
i 2 = j 2 = k2 = i jk = −1 .

(1)

The quaternion algebra H is defined as a set of four real numbers qi , called quaternions
q = q0 + q1 i + q2 j + q3 k. The conjugate qc of q is defined by qc = q0 − q1 i − q2 j − q3 k. Hamilton
was to give a 3D (if not 4D) interpretation of quaternions which was to lead to the classical
vector calculus still in use today. He also introduced complex quaternions which he named
biquaternions.

2.2

Clifford algebras and hyperquaternions

Clifford in 1878, introduced his algebras as tensor products of quaternion algebras [11]. He
proved the following theorem
C2m ≃ H⊗m ,

C2m−1 ≃ C ⊗ H⊗m−1 .

(2)

Lipschitz in 1880, derived the rotation formula of nD Euclidean spaces [12]
x ′ = a x a−1 ,

a ∈ C+ .

(3)

He thereby rediscovered the (even) Clifford algebras. In 1922, Moore [13] was to call Lipschitz’s algebras: hyperquaternions, a term which we shall extend to all Clifford algebras. A
major success of Clifford algebras in physics was the Dirac algebra and the spinor calculus. Recent developments in Clifford algebras seem to have somewhat neglected if not totally ignored
the hyperquaternionic filiation.
In terms of generators, the Clifford algebra Cn (p, q) has n = p + q generators ei such that
ei e j + e j ei = 0 (i ̸= j), ei2 = +1 (p generators) and ei2 = −1 (q generators). The total number of
elements is 2n . The algebra contains scalars (S), vectors (V ) ei , bivectors (B) ei e j (i ̸= j), etc.
030.2

## PDF page 3

SciPost Phys. Proc. 14, 030 (2023)

C + is the (even) subalgebra constituted by products of an even number of ei . It is to be noticed
that the hyperquaternion product is independent of the choice of the generators whereas the
multivector structure depends on it.
Examples of hyperquaternion Clifford algebras are: quaternions H (e1 = i, e2 = j), biquaternions C ⊗ H (e1 = i I, e2 = jI, e3 = kI, I = 1⊗i), H ⊗ H (e0 = j, e1 = kI, e2 = kJ, e3 = kK)
with (I, J, K) = 1⊗ (i, j, k).

3

Quaternion 2D representation

In contradistinction to Hamilton who gave a 3D interpretation of quaternions which is still
widely used today, we shall provide a 2D plane representation below since quaternions constitute a Clifford algebra with only two generators

e1 = i , e2 = j , e1 e2 = k
e12 = e22 = −1 .
(4)
Interior and exterior products can be defined with x = x 1 i + x 2 j ∈ V, B = bk bivector (b ∈R)
by
x. y = − (x y + y x) /2 = x 1 y1 + x 2 y2 ∈ S ,

(5)

x ∧ y = (x y − y x) /2 = (x 1 y2 − x 2 y1 ) k ∈ B ,

(6)

x.B = − (x B − B x) /2 = b (−x 2 i + x 1 j) ∈ V ,

(7)

x ∧ B = (x B + B x) /2 = 0 .

(8)

The rotation group SO(2) is expressed by
x ′ = r x rc = (x 1 cos θ − x 2 sin θ ) i + (x 1 sin θ + x 2 cos θ ) j ,

(9)

r = e kθ /2 = (cos θ /2 + k sin θ /2) ∈ B .

(10)

with

The modeling of an Euclidean 3D space can be realized similarly with biquaternions [14].

4

Hyperquaternionic conformal group in (1+2) space

The conformal group of the (1 + 3) space has been examined within the algebra H⊗3 ≃ C6 (2, 4)
in [4]. Here, we consider the (1 + 2) subspace within the subalgebra C5 (2, 3) ≃ C ⊗ H⊗2 ≃ C(4)
isomorphic to the Dirac algebra. This space has received much attention in particular with
respect to quantum gravity [8]. We first introduce the algebraic structure, then the restricted
conformal group and a numerical example including a canonical decomposition into simple
planes.

4.1

Algebraic structure

As generators of the subalgebra C5 (2, 3) ≃ C ⊗ H⊗2 , we take
ea = kI ,

e0 = kJ ,

e1 = kK l ,

e2 = kK m ,

eb = j ,

(11)

with
H⊗3 = (i, j, k) ⊗ (I, J, K) ⊗ (l, m, n) ,

030.3

(12)

## PDF page 4

SciPost Phys. Proc. 14, 030 (2023)

and (l, m, n) = 1 ⊗ 1 ⊗ (i, j, k). A general element A of H⊗3 can be viewed as a set of 16
quaternions [qi ] = ai + bi l + ci m + di n
 
 
A = [q1 ] + I [q2 ] + J [q3 ] + K q4 + i [q5 ] + i I [q6 ] + iJ q7 + iK [q8 ]
 
 
+ j q9 + j I [q10 ] + jJ [q11 ] + jK [q12 ] + k [q13 ] + kI q14 + kJ [q15 ] + kK [q16 ] . (13)
The explicit multivector structure of C5 (2, 3) is given in Appendix [A]. The algebra has
25 = 32 elements with 10 parameters for the bivectors. The product is implemented in
http://www.notebookarchive.org/2021-08-6z1zbda/.

4.2

Restricted conformal group

The restricted conformal group in (1 + 2) space is obtained via the procedure described in [1].
First, one constructs an affine space within C5 (2, 3). Let X be a five dimensional vector


x2 − 1
x2 + 1
X=
ea + x +
e b = x 2 ϵ1 + x + ϵ2 ,
(14)
2
2
with x = x 0 e0 + x 1 e1 + x 2 e2 ∈ E3 ,
ϵ1 =

X 2 = 0 and

ea + e b
,
2

ϵ2 =

e b − ea
,
2

ϵ12 = ϵ22 = 0 .

(15)

The restricted conformal group is then expressed by the transformations
X ′ = aX ac

(aac = 1 ,

a ∈ C5+ (2, 3)) .

(16)

They are composed of
θ

• spatial rotations a = e n 2 ,
θ

• boosts a = e B 2 ,

B ∈ (I l, I m) ,

• translations a = eϵ1 u = 1 + ϵ1 u

(u ∈ E3 ) ,

• transversions a = eϵ2 v = 1 + ϵ2 v

(v ∈ E3 ) ,

ϕ

ϕ

ϕ

ϕ

• dilations a = e ea e b 2 = e−i I 2 = cosh 2 − i I sinh 2 .
The total number of parameters is
obtains the general transformations
X ′ = f X fc

(n+2)(n+1)
= 10 (n = 3) .
2

( f fc = 1 ,

Through combinations, one

f ∈ C5+ (2, 3)) .

(17)

The Lie algebra is given in [4]

4.3

Numerical example

Here, we present a numerical example consisting of a set of transformations together with a
canonical decomposition thereof.

030.4

## PDF page 5

SciPost Phys. Proc. 14, 030 (2023)

As transformation X ′ = f X f c we shall consider a dilation (e−ϕ = 1/3) followed by a unit
translation (u = e1 ) and a rotation ( θ = π/2 in the plane e12 = n). The combination of these
transforms yields the hyperquaternion f ∈ C +
ϕ

θ

f = e n 2 eϵ1 u e−i I 2

(18)

= (cos θ /2 + n sin θ /2) (1 + ϵ1 u) (cosh ϕ/2 − i I sinh ϕ/2)




(kI + j)
2
1
1
1
= p + np
kK l p − i I p
1+
2
3
3
2
2
‾
‾

⎷
⎷2
1
1 2
− p i I (1 + n) +
(J + iK) (l + m) ,
=
3
2 3
6

(19)
(20)
(21)



ϕ
1+thϕ/2
3/2
with tan θ2 = 1, tanh 2 = 21 eϕ = 1−thϕ/2 = 1/2 = 3 .
The bivector part B of f generating the transformation, divided by the scalar
B = n−

iJ 3
+ (J + iK) (l + m) .
2
4

q

2
3 is

(22)

The canonical decomposition [4] of B and f into simple, orthogonal and commuting planes
Φ
Φ
(B1 , B2 ) with b1 = tan 21 = 1, b2 = tanh 22 = 12 leads to
B = b1 B1 + b2 B2 ,

Φ1

Φ2

f = e 2 B1 e 2 B2 ,

(23)

with
3
(J + iK) (3l + m) ,
10

B12 = −1 ,

(24)

3
(J + iK) (−l + 3m) − I K ,
10

B22 = 1 .

(25)

S2 = [(B ∧ B) .B] .B = −1 .

(26)

B1 = n +
B2 =

The two invariants of the transformation are
3
S1 = B.B = − ,
4

The conformal transformation with X = ea + e1 + e b (x 0 = 0, x 1 = 1, x 2 = 0) is obtained either
directly
D

T

R

e1 → e1 /3 → (1/3 + 1) e1 = (4/3) e1 → (4/3) e2 ,

(27)

X ′ = f X f c = x a′ ea + x ′ + x ′b e b
7
25
= − ea + 4e2 − e b ,
6
6

(28)

or by computation:

yielding the final transform
x → y(x) =

5

x′
4
= e2 .
3
x ′b − x a′

(29)

(30)

Classification of hyperquaternion algebras

Table 1 lists a few hyperquaternion algebras and their signature (p, q) obtained via the generators given in [7]. The table shows the importance of the parameter s = p − q [2, 15]. It
030.5

## PDF page 6

SciPost Phys. Proc. 14, 030 (2023)

reveals four classes of hyperquaternions: the algebras H⊗r (r even or odd) and the subalgebras
C + . From (n, s) one deduces p = (n + s) /2, q = (n − s) /2 yielding the general formulas for m
integer (m ⩾ 1)
H⊗2m ≃ C4m (2m + 1, 2m − 1) ,

(s = 2) ,

C ⊗ H⊗(2m−1) ≃ C4m−1 (2m + 1, 2m − 2) ,
H

⊗(2m−1)

≃ C4m−2 (2m − 2, 2m) ,

(s = 3) ,

(s = −2) ,

C ⊗ H⊗(2m−2) ≃ C4m−3 (2m − 2, 2m − 1) ,

(s = −1) .

All signatures of hyperquaternion algebras can be derived from the first four ones via the
formula
Cn+4 (p + 2, q + 2) = Cn (p, q) ⊗H⊗2 ,
resulting from the double application of the general formula
Cn+2 (p + 1, q + 1) = Cn (p, q) ⊗C2 (1, 1) ,
together with C2 (1, 1) ≃ R (2) , R (2) ⊗R (2) ≃ R (4) ≃ H⊗2 . Furthermore, since
H⊗2 ≃ R (4) ,

C ⊗ H⊗2 ≃ C (4) ,

H⊗3 ≃ H (4) ,

one obtains all square real, complex and quaternionic matrices. Concerning the matrix representation of hyperquaternion algebras, which is beyond the scope of this paper, the above
isomorphisms show that H⊗2 can be represented either by a reducible real matrix R (16) (real
16 × 16 matrix) or by an irreducible R (4) matrix (H being represented by an irreducible
R (4) matrix). Similarly, H⊗3 and its subalgebra C ⊗ H⊗2 can be represented either by a reducible matrix R (64) or by an irreducible matrix R (16) . A classification of real irreducible
representations of quaternionic Clifford algebras can be found in [16, 17].
A hyperconjugation defined as
AH = (ic , jc , kc ) ⊗ (I c , Jc , Kc ) ⊗ (l c , mc , nc ) ,
yields the matrix transposition, adjunction and transpose quaternion conjugate. Finally, writing ω = e1 · · · en , one obtains for all hyperquaternion algebras with the above values of s and
Table 1: Hyperquaternion algebras (SR: special relativity, RQM: relativistic quantum
mechanics, usp: unitary symplectic physics, sm: standard model).
Cn (p, q)
C
H
C⊗H
H⊗2 ≃ R (4)
C ⊗ H⊗2 ≃ C (4)
H⊗3 ≃ H (4)
C ⊗ H⊗3
H⊗4
C ⊗ H⊗4
H⊗5
C ⊗ H⊗5
H⊗6

n
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

p
0
0
3
3
2
2
5
5
4
4
7
7

q
1
2
0
1
3
4
2
3
5
6
4
5

s = p−q
−1
−2
3
2
−1
−2
3
2
−1
−2
3
2

030.6

G r oup
U(1)
US p(1)
SU(2)
SO(3, 1)
SU(4)
US p(4)
SU(8)
SO(5, 3)
SU(16)
US p(16)
SU(32)
SO(7, 5)

Ph ysics
1D
2D
3D
SR
RQM
usp
sm

## PDF page 7

SciPost Phys. Proc. 14, 030 (2023)

the classical derivation (developing n = p + q and using (−1) pq = (−1)−pq )
ω2 = (−1)

n(n−1)
2

e12 ...en2 = (−1)

n(n−1)
+q
2

= (−1)

s(s−1)
2

= −1 .

Though hyperquaternion algebras have been neglected in the past, recent algebraic software
like Mathematica and numerical computing have opened perspectives for the hyperquaternion calculus. An advantage of the hyperquaternion representation of Clifford algebras, is
that the product is defined independently of the choice of the generators. Furthermore, hyperquaternion algebras single out specific Clifford algebras which seem to be closely related
to symmetry group of physics as indicated in the table above. Thus they might constitute a
step towards a greater unification as proposed in [18].

6

Conclusion

The paper has developed applications of a new hyperquaternionic representation of Clifford
algebras in terms of tensor products of quaternion algebras. One advantage of hyperquaternion algebras is a uniquely defined product, independent of the choice of generators. Though,
hyperquaternions have been somewhat neglected so far, they have become more accessible
due to the introduction of algebraic and numerical computing. As applications, the paper has
examined the quaternion 2D representation, the conformal group in (1 + 2) space together
with a numerical example and implementation. Finally, a classification of all hyperquaternion
algebras into four types has been given, with general formulas of the signatures and the associated symmetry groups. We hope to have shown that the hyperquaternion algebras might
constitute a useful unifying tool for physics.

Acknowledgements
The paper is dedicated to the memory of our colleague and friend Prof. Dr. Robert Goutte
(1932-2022) who greatly furthered and collaborated on research on quaternions and hyperquaternions.
The authors acknowledge and thank an anonymous referee for comments clarifying the
matrix quaternionic Clifford algebra representation issue.
Funding information This work was supported by the LABEX PRIMES (ANR-11-LABX-0063)
of Université de Lyon, within the program “Investissements d’Avenir” (ANR-11-IDEX-0007)
operated by the French National Research Agency (ANR).

030.7

## PDF page 8

SciPost Phys. Proc. 14, 030 (2023)

A

Multivector structure of C5 (2, 3)

(e012 = e0 e1 e2 , etc..)

1
 0

 0

 K = e0a

 0

 i I = e ba

 iJ = e b0

 0

 j = eb

 0

 0

 jK = e0a b

 0

 kI = ea
 kJ = e
0
0

0
I l = e10
J l = ea1
0
il = e0a1b
0
0
iK l = e b1
0
j I l = e10b
jJ l = ea1b
0
kl = ea01
0
0
kK l = e1

0
I m = e20
J m = ea2
0
im = e0a2b
0
0
iK m = e b2
0
j I m = e b20
jJ m = ea2b
0
km = ea02
0
0
kK m = e2


n = e12

0


0


K n = e0a12

0


i I n = e1a2b 

iJ n = e102b 

0


jn = e12b


0


0


jK n = e0a12b 

0


kI n = ea12 
kJ n = e012 
0

References
[1] P. Anglès, Conformal groups in geometry and spin structures, Birkhäuser, Boston, USA,
ISBN 9780817635121 (2008), doi:10.1007/978-0-8176-4643-1.
[2] M. Rausch de Traubenberg, Clifford algebras in physics, Adv. Appl. Clifford Algebras 19,
869 (2009), doi:10.1007/s00006-009-0191-2.
[3] G. L. Panga, Hyperquaternionic representations of conic sections, J. Appl. Math. Phys. 10,
2989 (2022), doi:10.4236/jamp.2022.1010200.
[4] P. R. Girard, P. Clarysse, R. Pujol, R. Goutte and P. Delachartre, Hyperquaternion conformal
groups, Adv. Appl. Clifford Algebras 31, 56 (2021), doi:10.1007/s00006-021-01159-y.
[5] P. R. Girard, P. Clarysse, R. Pujol, R. Goutte and P. Delachartre, Dual hyperquaternion
Poincaré groups, Adv. Appl. Clifford Algebras 31, 15 (2021), doi:10.1007/s00006-02101120-z.
[6] P. R. Girard, P. Clarysse, R. Pujol, R. Goutte and P. Delachartre, Hyperquaternions:
An efficient mathematical formalism for geometry, in Geometric science of information,
Springer, Cham, Switzerland, ISBN 9783030269791 (2019), doi:10.1007/978-3-03026980-7_13.
[7] P. R. Girard, P. Clarysse, R. Pujol, R. Goutte and P. Delachartre, Hyperquaternions: A new
tool for physics, Adv. Appl. Clifford Algebras 28, 68 (2018), doi:10.1007/s00006-0180881-8.
[8] S. Carlip, Quantum gravity in 2 + 1 dimensions, Cambridge University Press, Cambridge,
UK, ISBN 9780521564083 (1998), doi:10.1017/CBO9780511564192.
[9] P. R. Girard, Quaternions, Clifford algebras and relativistic physics, Birkhäuser, Basel,
Switzerland, ISBN 9783764377908 (2007), doi:10.1007/978-3-7643-7791-5.
030.8

## PDF page 9

SciPost Phys. Proc. 14, 030 (2023)

[10] P. R. Girard, Quaternions, algèbre de Clifford et physique relativiste, Presses Polytechniques
et Universitaires Romandes, Lausanne, Switzerland, ISBN 9782880746063 (2004).
[11] W. K. Clifford, Applications of Grassmann’s extensive algebra, Am. J. Math. 1, 350 (1878),
doi:10.2307/2369379.
[12] R. Lipschitz, Principes d’un calcul algébrique qui contient comme espèces particulières le
calcul des quantitiés imaginaires et des quaternions, C. R. Acad. Sci. Paris 91, 619 (1880).
[13] C. L. E. Moore, Hyperquaternions, J. Math. Phys. 1, 63 (1922).
[14] P. R. Girard, P. Clarysse, R. Pujol, L. Wang and P. Delachartre, Differential geometry revisited
by biquaternion Clifford algebra, in Curves and surfaces, Springer, Cham, Switzerland,
ISBN 9783319228037 (2015), doi:10.1007/978-3-319-22804-4_17.
[15] D. W. Marks, Binary encoded recursive generation of quantum space-times, Adv. Appl. Clifford Algebras 32, 51 (2022), doi:10.1007/s00006-022-01235-x.
[16] S. Okubo, Real representations of finite Clifford algebras. I. Classification, J. Math. Phys.
32, 1657 (1991), doi:10.1063/1.529277.
[17] H. L. Carrion, M. Rojas and F. Toppan, Quaternionic and octonionic spinors. A classification,
J. High Energy Phys. 04, 040 (2003), doi:10.1088/1126-6708/2003/04/040.
[18] M. Tegmark, Our mathematical Universe: My quest for the ultimate nature of reality, Penguin Books, London, UK, ISBN 9780241954638 (2015)

030.9
