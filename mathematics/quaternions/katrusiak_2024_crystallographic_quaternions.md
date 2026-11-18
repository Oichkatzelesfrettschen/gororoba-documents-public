Source: https://doi.org/10.3390/sym16070818
PDF sha256: 7430cb88ba9d40999fa0f3dabbd9cd5cdb6fa83c230ce8df8b69144156838de2
License: cc-by
Language: eng
Fidelity: machine-gated

# Transcription of katrusiak_2024_crystallographic_quaternions.pdf

Transcription of `katrusiak_2024_crystallographic_quaternions.pdf` in this directory, 14 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-14 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

SS symmetry
Article

Crystallographic Quaternions
Andrzej Katrusiak *

and Stiv Llenga †
Faculty of Chemistry, Adam Mickiewicz University, Uniwersytetu Poznańskiego 8, 61-614 Poznań, Poland;
sxl1428@student.bham.ac.uk
* Correspondence: katran@amu.edu.pl; Tel.: +48-618291590
† Current address: Heidelberg Institute for Theoretical Studies, Ruprecht Karl University of Heidelberg,
69118 Heidelberg, Germany.

Abstract: Symmetry transformations in crystallography are traditionally represented as equations
and matrices, which can be suitable both for orthonormal and crystal reference systems. Quaternion
representations, easily constructed for any orientations of symmetry operations, owing to the vector
structure based on the direction of the rotation axes or of the normal vectors to the mirror plane, are
known to be advantageous for optimizing numerical computing. However, quaternions are described
in Cartesian coordinates only. Here, we present the quaternion representations of crystallographic
point-group symmetry operations for the crystallographic reference coordinates in triclinic, monoclinic, orthorhombic, tetragonal, cubic and trigonal (in rhombohedral setting) systems. For these
systems, all symmetry operations have been listed and their applications exemplified. Owing to
their concise form, quaternions can be used as the symbols of symmetry operations, which contain
information about both the orientation and the rotation angle. The shortcomings of quaternions,
including different actions for rotations and improper symmetry operations, as well as inadequate
representation of the point symmetry in the hexagonal setting, have been discussed.
Keywords: symmetry operations; quaternion representation; crystallography; non-Cartesian systems;
Cayley table

1. Introduction
Citation: Katrusiak, A.; Llenga, S.
Crystallographic Quaternions.
Symmetry 2024, 16, 818. https://
doi.org/10.3390/sym16070818
Academic Editor: Vasilis K.
Oikonomou
Received: 30 April 2024
Revised: 13 June 2024
Accepted: 19 June 2024
Published: 29 June 2024

Copyright: © 2024 by the authors.
Licensee MDPI, Basel, Switzerland.
This article is an open access article
distributed under the terms and
conditions of the Creative Commons
Attribution (CC BY) license (https://
creativecommons.org/licenses/by/

The algebra of quaternions was invented nearly two centuries ago [1–4] and it is often
used for technical and scientific applications involving various rotations, as well as in
computer graphics [5–8]. In crystallography, quaternions have been applied for positioning
diffractometer shafts [9,10], describing disorientations between crystal lattices [11,12], refining orientation matrix during diffraction measurements [13] and rotating and comparing
molecules [14–17]. However, the applications of quaternions for representing symmetry
operations are scarce and, like most of the quaternion calculations, they are limited to the
orthonormal reference systems [18,19]. Owing to the easy and appealing algebra of quaternions, their application for transforming vectors described in crystallographic reference
systems can be presented in a simple intuitive manner. A limitation is that all applications
of quaternions in crystallography presented in the literature are described for Cartesian
systems [20]. Presently, we discuss the application of quaternions for representing symmetry operations of vectors described in the reference axes of crystallographic systems.
In this project, we aimed at investigating the applicability of quaternions representing
point-symmetry operations for non-Cartesian reference systems of crystals, describing
the transformations of vectors by using quaternions as well as generating new symmetry
operations from others by combining (multiplying) their quaternion representations. While
the quaternions were originally constructed for the orthogonal space, the crystallographic
systems are, in general, non-Cartesian. For this reason, we have undertaken to derive
quaternions representing symmetry operations in traditional crystallographic systems.

4.0/).

Symmetry 2024, 16, 818. https://doi.org/10.3390/sym16070818

https://www.mdpi.com/journal/symmetry

## PDF page 2

Symmetry 2024, 16, 818

2 of 14

It will be shown that the quaternion representation of symmetry operations in crystallographic reference systems can be more concise than the equivalent matrices. Therefore,
apart from the consequent simplicity of the notation and reduced number of arithmetic
calculations, the direct connection of quaternions with the symmetric directions and the
angle of rotation in crystallographic systems can make them more appealing for illustrating
and teaching symmetry and point-group concepts. Another purpose of the present study
was to investigate the limitations of adopting classical quaternions (q = s + ui + vj + wk) for
the complete representation of all symmetry operations in non-Cartesian crystallographic
reference systems. These limitations can be considered to be the stumbling blocks hindering
the common use of quaternions in crystallography. To emphasize our intention to employ
the quaternions to crystallographic systems, both the Schönflies and Hermann–Mauguin
notations will be used for the symmetry elements and operations.
2. Discussion
2.1. Basic Definitions
Hereafter, the quaternion will be defined as q = s + ui + vj + wk, where s, u, v and w are
scalars, all s, u, v, w ⊂ R, whereas i, j and k are imaginary versors fulfilling the conditions
i2 = j2 = k2 = ijk = −1 [2–4]. The quaternion is a four-dimensional version of complex
numbers, where s is the real and u, v and w are the imaginary components. Quaternion
q can represent a rotation by angle φ about vector v = [u, v, w] in the three-dimensional
orthogonal space, when it is written in the following form:
q(φ,v) = [cos(φ/2) + n·sin(φ/2)]

(1)

where the unit vector along the axis of rotation is n = v/|v|.
2.2. Rotations
Equation (1), directly connecting quaternions with rotations, is well known and it can
be generally applied for representing the symmetry operations in orthogonal systems [2–8].
For performing a rotation of a real-space vector r = [x y z], it should be projected onto the
three-dimensional imaginary subspace of four-dimensional quaternions; this projection
will be further represented by the same symbol, but with round brackets: r = (ix + jy + kz).
Its image r’ after the rotation by angle φ about vector v, described by quaternion q(φ,v)
(Equation (1)), is equal to
r’ = q(φ,v)·r ·q*(φ,v)
(2)
where q*(φ,v) is the conjugate of q(φ,v): q*(φ,v) = q(φ, − v). Equation (2) is generally applicable for orthonormal (Cartesian) coordinates. Several such rotations are
exemplified below.
Let us rotate vector r = [211] by 180◦ about the plane-diagonal vector [110] in a cubic
system. This rotation is represented by the quaternion (Equation (1))
(
) ( √
√ )
◦
q 180 , [110] = i/ 2 + j/ 2 .
According to Equation (2),
( √
(
√
√
√ )
′
r = i/ 2 + j/ 2)·(2i + 1j + 1k)· −i/ 2 − j/ 2 = (i + 2j − k).
Thus, the vector components after the 180◦ rotation about direction [110] are r’ = [1 2 −1].
The rotation C3 of vector r = [1, 0, 1], which in crystallographic coordinates corresponds
◦
to rc = [1, 1/2, 1], about axis [z] can be performed
√ by quaternion q(120 ,[001]), which
◦
according to Equation (1) is q(120 ,[001]) = (1/2 + k 3/2). The rotated vector according to
Equation (2) is

## PDF page 3

Symmetry 2024, 16, 818

3 of 14

(
(
)
(
√
√
√
′
r = 1/2 + k 3 /2)·(1i + 0j + 1k)· 1/2 − k 3 /2) = −1/2i + 3 /2j + k .
Thus,
the vector components after the rotation by 60◦ about the [001] axis are r’ = [−1/2,
√
3/2, 1].
2.3. Efficiency of Quaternions



1
Rx =  0
0

The quaternion representation of rotations and symmetry operations can be advantageous compared to other representations in certain applications. The most apparent and
frequently cited advantage is the easiness of constructing performing any rotation from
the rotation axis and angle, as defined in Equations (1) and (2). The matrix representation
in a general case requires that the rotation be composed of the Euler rotations about the
orthogonal axes:





0
0
cos ε 2 0 − sin ε 2
cos ε 3 − sin ε 3 0
cos ε 1 − sin ε 1 , Ry =  0
1
0 , Rz =  sin ε 3
cosε 3 0,
sin ε 1
cosε 1
sin ε 2 0
cosε 2
0
0
1
where the aligning angles εi (i = 1, 2, 3) can be calculated by using the trigonometric functions.
Several variants are possible, for example, first, the rotation axis v can be rotated by angle ε3
about axis z to bring it to the xz plane (matrix Rz multiplied by v); subsequently, this new
position of v can be rotated by angle ε2 about axis y by matrix Ry , to overlie vector v with axis
x. For the so-aligned v axis, the rotation by angle φ is performed by the rotation matrix


1
0
Rx (φ) = 0 cos φ
0 sin φ


0
− sin φ
cos φ

Subsequently, the system should be rotated back by the reverse matrices of Rz and Ry ;
hence, the matrix rotation of vector r by angle φ around vector v can be written as
r’= Rz −1 ·Rx −1 ·Rx (φ)·Rx ·Rz ·r
Only the cubic system is consistent with the Cartesian reference system, as the unit
cell parameters fulfil the orthonormal conditions a = b = c and α = β = γ = 90 ◦ . Crystallographic systems—tetragonal, hexagonal, trigonal, orthorhombic, monoclinic and
triclinic—gradually depart from the orthonormal setting, with the most ‘skew’ being
the triclinic system, where all a, b, and c are different in length and all α, β and γ divert
from 90 ◦ .
Before using the Euler matrices, any non-Cartesian system should be orthogonalized.
The most general case is for a triclinic crystal. Its unit cell parameters, a, b, c, α, β and γ,
can be used for constructing a lower-triangular orthogonalization matrix L [21]:


a·sin β·sin γ∗
L = − a·sin β·cos γ∗
a· sin β

0
b·sin α
b· cos α


0
0,
c

where cosγ* = (cosα·cosβ − cosγ)/(sinα·sinβ) and sinγ* = (1 − cos2 γ*)1/2 . The L matrix
above would not generally preserve the crystal symmetric direction; for example, in a
monoclinic system, the crystal symmetry direction [010], in the orthogonalized coordinates,
would become [0, b sinα, b cosβ]. Thus, the rotation axis vector v requires orthogonalization,
too. For returning to the crystallographic reference system, the rotation of the vector should

## PDF page 4

Symmetry 2024, 16, 818

4 of 14

be transformed back by multiplying by the reverse of the orthogonalization matrix, L−1 , so
the formula above further complicates to
r’= L−1 ·Rz −1 ·Rx −1 ·Rx (φ)·Rx ·Rz ·L·r
The quaternion representation of this rotation by angle φ about vector v, as defined
in Equations (1) and (2), is straightforward and more concise. While there is no doubt
about the concise form of the quaternion representation in Cartesian reference systems,
to our knowledge direct quaternion transformations in non-Cartesian systems have
not been explored, and the purpose of this work is to check the possibility of using
the quaternion representations of point-group symmetry operations directly in crystallographic coordinates. The strength of matrix representations, commonly used in
crystallography, is that the step transformations can be easily combined through the
multiplication of matrices, which would reduce the above formula to r’ = T(φ)·r, where
T(φ) = L−1 ·Rz −1 ·Rx −1 ·Rx (φ)·Rx ·Rz ·L. Depending on the type of rotation, the comparison of the number of arithmetic operations can be more or less advantageous for the
matrix and quaternion representations.
For example, finding a rotation about the 3-fold axis along direction [111] in a trigonal
R lattice through the Euler rotations about the axes of orthogonalized reference system
requires hundreds of arithmetic operations, including trigonometric functions, but as
indicated above, they can be reduced to the matrix equation
  
y
0
 z  = 0
x
1

1
0
0

 
0
x
1  y 
0
z

The quaternion equation can be straightforwardly written following Equations (1) and (2):
(1 + i + j + k)(xi + yj +zk)(1 − i − j − k) = yi + zj + xk.
The reduced matrix representation requires 9 multiplications and 6 additions, while the
quaternion representation requires 48 multiplications and 16 additions.
In another example, a rotation about the 2-fold axis along direction [100] is described
by the following matrix equation, corresponding to just one Euler rotation about axis [x]:


 
x
1
 − y  = 0
z
1

0
−1
0

 
0
x
0  y 
−1
z

and the quaternion equation i(xi + yj + zk)(−i) = −i + yj + zk requires 9 multiplications
and 6 additions, compared to 6 multiplications and no additions, respectively. It can
be concluded that the advantages of the matrix and quaternion representations depend
on the particular problem, its complication and possible optimization procedures for
computations. In many crystallographic considerations, the symmetry operations or other
calculations can be performed directly in the reference system of crystal axes, which is
preferential, require less computer power, is more precise and easier than the procedures
resorting to the orthogonalization. Undoubtedly, for the purpose of efficiently comparing
the performance of matrix and quaternion representations in crystal reference systems, both
these representations in non-Cartesian systems are required. Therefore, it is the purpose of
this article to investigate the suitability of quaternions for symmetry operations directly in
crystallographic reference systems.
2.4. Quaternion Identity and Inversion
Equation (1) can be used for deriving the identity quaternion, corresponding to the
360◦ rotation:

## PDF page 5

Symmetry 2024, 16, 818

5 of 14

q(360◦ ,v) = [cos(180◦ ) + n·sin(180◦ )] = −1

(3)

In this case, the q(360◦ ,v) quaternion has only the scalar component different from zero,
and the pre- and post-multiplications can be reduced to the multiplication by 1. It can be
noted that Equation (3) can be extended by including an integer n of multiple full rotations:
q(n·360◦ , v) = cos(n·180◦ ) + n sin(n·180◦ ) =

{

−1 for n odd
1 for n even

(3a)

Because r’ = q rq* for all n, Equation (3a) is reduced to r’ = 1r, i.e., the identity operation.
Further, we shall assume as the definition of the inversion centre that for any vector r its
inversion image is −r. Consequently, the quaternion representation of the inversion centre
can be defined as
r’ = −q(360◦ ,v)·r ·q*(360◦ ,v)
(4)
which can be simplified to the operation equivalent to the centre of inversion, Ci :
r’ = −1·r

(5)

2.5. Quaternion Mirror Plane
Quaternions are ideally suited for representing mirror-plane (Cs , m) symmetry operations. The mirror plane perpendicular to a given direction can be considered as a
combination of a 2-fold rotation (by 180◦ ) about the normal to a plane and the inversion
centre at the intersection of the plane and the 2-fold axis. Following the above discussion,
the mirror plane can be represented as the product
r’ = −q(180◦ ,n)·r ·q*(180◦ ,n)

(6)

where vector n is perpendicular to the mirror plane and fulfils the normalization condition
as defined in Equation (1). It can be noted that for all quaternions with real part s = 0,
Equation (6) can be reduced to a simpler form:
r’ = q·r ·q

(7)

This includes any quaternion q(180◦ ,n), because cos(90◦ ) = 0, which applies to all mirror
planes, represented as their normal-direction vector n projected into the imaginary space.
For example, the reflection of vector r = [211] in the mirror plane perpendicular to
vector v = [110] can be performed by Equation (6) for quaternion
q(180◦ ,[110]) defined
√
◦
in Equation
(1).
√
√ In this example,
√ q(180√,[110]) = (i + j)/ 2. According to Equation (6),
r’ = (i/ 2 + j/ 2)·(2i + j + k)·(i/ 2+ j/ 2) = (−i − 2j + k), corresponding to the real-space
vector r’ = [−1 −2 1].
2.6. Inverse Rotations
We shall further consider inverse rotations, which are the same as the symmetry
operations of inverse axes (also termed improper axes) in crystallography. Originally,
Schoenflies distinguished only one inverse rotation, which he termed Spiegelachse and
denoted as S4 ; according to Schönflies, axis S4 was derived as a combination of a 4-fold
rotation (C4 ) with a perpendicular mirror plane (Cs ). Symbol S in S4 and subscript
s − in Cs − are derived from the German word Spiegel, meaning mirror in English.
Schönflies described combinations of the mirror plane with other rotation axes, denoted
with symbols C1 , C2 , C3 , C6 , as Ci , Cs , C3i , and C3h , respectively. Since then, symbols
S1 (Hermann–Mauguin symbol m), S2 (1), S3 (6), S4 (4) and S6 (3) have been used, too
(Hermann–Mauguin symbols are given in brackets). Hermann and Mauguin, in turn,
combined natural 1-, 2-, 3-, 4- and 6-fold rotations with the centre of inversion, and the
derived products were inversion axes denoted as 1, m, 3, 4 and 6.

## PDF page 6

Symmetry 2024, 16, 818

6 of 14

Thus, the improper rotations 1, m, 3, 4 and 6 can be generated either (i) by combining
the mirror plane with natural axes 2, 1, 6, 4 and 3, respectively, or (ii) by combining the
inversion centre with natural axes 1, 2, 3, 4 and 6, respectively. For the first approach
(i) of generating the inverse rotations by combining the rotations with the mirror plane,
Equations (2) and (7) give
r’ = q(φ,n)·q(180◦ ,n)·r ·q(180◦ ,n)·q*(φ,n),
which can be reduced to
r’ = −q(φ,n)*·r ·q(φ,n)

(8)

The second approach (ii), i.e., the combination of a natural rotation axis with the inversion
centre, gives
r’ = −q(φ,n)·r ·q*(φ,n)
(9)
The combinations with the mirror plane (Equation (8)) and with the inverse centre
(Equation (9)) result in the opposite sense of the improper rotations.
For example, the symmetry operations for improper axis 4 around axis [z] can be
based on the quaternion
( ◦ ) [ ( ◦)
( ◦ )]
√
q 90 , n = cos 45 + n· sin 45
= (1 + k)/ 2.
Let us transform vector r = [1 1 1], so r = (i + j + k), according to Equation (8) (plane m plus
the natural rotation 4)
r’ = −i + j − k,
which corresponds to the axis 4 (S4 ) rotation rightward (when looking from the origin in
the positive direction of axis [z]), while according to Equation (9) (inversion centre plus the
natural rotation), we obtain
r’ = i − j − k,
corresponding to the operation of the improper rotation axis 4 performed leftward. Further
in this paper, we will use the second approach (Equation (9)) for the improper rotations.
2.7. Crystal Reference Systems
Quaternions are generally described in Cartesian reference systems, i.e., orthogonal
axes with versors equal in length. For certain non-Cartesian reference systems, it can be
shown that quaternions can genuinely represent symmetry operations of crystallographic
point groups. The quaternion representations of symmetry operations, as specified in
Equations (1)–(9), can be directly applied to vectors described in the crystal reference sets
of axes for the crystallographic systems, as specified in Tables 1–5. Thus, the symmetry
operations of identity C1 and inversion Ci have simple quaternion representations that
are valid in the triclinic system (Table 1). These quaternion representations of C1 and
Ci can be applied in all crystallographic systems. Table 2 lists the symmetry operations
C1 , Ci , C2 and Cs valid in the monoclinic system. In this case, we have applied the IUCr
convention to the monoclinic symmetry direction along [y]. The symmetry operations
characteristic of orthorhombic (Table 3) and tetragonal (Table 4) systems are valid in
these non-Cartesian systems, too. The crystallographic reference axes of the cubic system
are Cartesian; hence, the quaternion representations of all cubic symmetry operations,
specified in Table 5, are valid.
It can be noted that the proper and improper rotations involving the same quaternion
q can be achieved either through transformation type r’ = q·r ·q* (Equation (2)) or through
transformation type r’ = −q·r ·q* (Equation (9)), respectively. For the identity and inversion centre, these transformation types simplify to r’ = 1·r (Equation (3a)) and r’ = −1·r
(Equation (5)), respectively; for mirror planes, the simplification r’ = q·r ·q (Equation (7)) is
obtained. These main types of transformations as well as their simplifications have been
indicated in Tables 1–5.

## PDF page 7

Symmetry 2024, 16, 818

7 of 14

Table 1. Symmetry elements described in the Hermann–Mauguin notation for the triclinic system,
the symmetry operations represented as quaternions and the transformation type for vector r.
Symmetry Element

Quaternion (q)

Quaternion Action

1
1

1
−1

qr
qr

Table 2. Symmetry elements for the monoclinic system and quaternion representations of their
symmetry operations.
Symmetry Element

Quaternion (q)

Quaternion Action

1
1

1
−1
k
k

qr
qr
qrq*
qrq

2[010]
m[010]

Table 3. Symmetry elements for the orthorhombic system and the corresponding quaternion representations.
Symmetry Element

Quaternion (q)

Quaternion Action

1
1

1
−1
i
j
k
i
j
k

qr
qr
qrq*
qrq*
qrq*
qrq
qrq
qrq

2[100]
2[010]
2[001]
m[100]
m[010]
m[001]

Table 4. Symmetry operations for the tetragonal system, their quaternion representations and actions.
Symmetry Operation

Quaternion (q)

Quaternion Action

1
1

1
−1
i
j
k
√
(i + j)/ √2
(−i + j)/ 2
√
(1 + k ) / 2
k √
(−1 + k)/√ 2
(1 + k ) / 2
k √
(−1 + k)/ 2
i
j
k
√
(i + j)/ √2
(−i + j)/ 2

qr
qr
qrq*
qrq*
qrq*
qrq*
qrq*
qrq*
qrq*
qrq*
−qrq*
−qrq*
−qrq*
qrq
qrq
qrq
qrq
qrq

2[100]
2[010]
2[001]
2[110]
2[110]
4[001]
42 [001]
43 [001]
4[001]
42 [001]
43 [001]
m[100]
m[010]
m[001]
m[110]
m[110]

For non-Cartesian trigonal and hexagonal crystallographic systems (the hexagonal
family), the quaternion representations of symmetry operations are not generally valid
for the crystallographic reference axes. The quaternion representations of the symmetry
operations can be applied for the Cartesian system. For example, the inverse rotation 3

## PDF page 8

Symmetry 2024, 16, 818

8 of 14

◦
of vector
√ r = [1,0,1] about axis [z] can be performed for quaternion q(120 ,[001]) equal to
(1 + k 3)/2. According to Equation (9),
(
(
)
(
√
√
√
′
r = − 1 + k 3 )·(i + k)· 1 − k 3 )/4 = i/2 − j 3 /2 − k .

Thus, the r’ vector components
after the symmetry operation of improper rotation 3 about
√
direction [001] is [1/2 − 3/2 − 1], which is the 3 rotation performed for the orthogonal
Cartesian system. However, for the crystallographic reference axes of the hexagonal unit
cell, this cannot be performed. Only the symmetry operations for the trigonal point groups
described in the R lattice can be represented as quaternions, as listed in Table 6.
Table 5. Symmetry operations for the cubic system, their quaternion representations and actions. For
the sake of brevity, of all 40 proper and improper 3- and 4-fold axes, only the full set of operations
has been listed for axes 3[111] ; for the remaining ones, the power indices α = 1, 2 and β = 1, 2, 3 have
been introduced (cf. Table 4).
Symmetry Operation

Quaternion (q)

Quaternion Action

1
1

1
−1
i
j
k √
(i + j)/ √2
(−i + j)/ 2
√
(i + k)/ √2
(−i + k)/ 2
√
( j + k)/ √2
(− j + k)/ 2
(1 + i + j + k)/2
(−1 + i + j + k)/2
[(1 − i + j + k)/2]α
[(1 + i − j + k)/2]α
[(1 + i + j − k)/2]α
[(1 + i + j + k)/2]α
[(1 − i + j + k)/2]α
[(1 + i − j + k)/2]α
[(1 + i + j − k)/2]α
√
[(1 + i )/ √2]β
[(1 + j)/ √2]β
[(1 + k)/√ 2]β
[(1 + i )/ √2]β
[(1 + j)/ √2]β
[(1 + k)/ 2]β
i
j
k
√
(i + j)/ √2
(−i + j)/ 2
√
(i + k)/ √2
(−i + k)/ 2
√
( j + k)/ √2
(− j + k)/ 2

qr
qr
qrq*
qrq*
qrq*
qrq*
qrq*
qrq*
qrq*
qrq*
qrq*
qrq*
qrq*
qrq*
qrq*
qrq*
−qrq*
−qrq*
−qrq*
−qrq*
qrq*
qrq*
qrq*
−qrq*
−qrq*
−qrq*
qrq
qrq
qrq
qrq
qrq
qrq
qrq
qrq
qrq

2[100]
2[010]
2[001]
2[110]
2[110]
2[101]
2[101]
2[011]
2[011]
31 [111]
32 [111]
(3[111] )α
(3[111] )α
(3[111] )α
(3[111] )α
(3[111] )α
(3[111] )α
(3[111] )α
(4[100] )β
(4[010] )β
(4[001] )β
(4[100] )β
(4[010] )β
(4[001] )β
m[100]
m[010]
m[001]
m[110]
m[110]
m[101]
m[101]
m[011]
m[011]

## PDF page 9

Symmetry 2024, 16, 818

9 of 14

Table 6. Symmetry operations in trigonal point groups described in the rhombohedral Bravais lattice
R, their quaternion representations and actions.
Symmetry Operation

Quaternion (q)

Quaternion Action

1
1

1
−1 √
(i − j ) / 2
√
( j − k)/ 2
√
(−i + k)/ 2
(1 + i + j + k)/2
(−1 + i + j + k)/2
(1 + i + j + k)/2
+ k)/2
(−1 + i + j √
(i − j ) / 2
√
( j − k)/ 2
√
(−i + k)/ 2
i
j
k
√
(i + j)/ √2
(−i + j)/ 2

qr
qr
qrq*
qrq*
qrq*
qrq*
qrq*
−qrq*
−qrq*
qrq
qrq
qrq
qrq
qrq
qrq
qrq
qrq

2[110]
2[011]
2[101]
3[111]
32 [111]
3[111]
32 [111]
m[110]
m[011]
m[101]
m[100]
m[010]
m[001]
m[110]
m[110]

2.8. Quaternion Symbols of Symmetry Operations
Quaternions representing the operations in certain symmetry classes are concise and
therefore they can be considered as a convenient method for writing symbols of symmetry
operations and elements. The two main multiplication types for obtaining point-group
symmetry operations of (i) natural axes 1, 2, 3, 4 and 6 are executed through multiplication
qrq* (Equation (2)) and (ii) improper rotation axes 1, m, 3, 4 and 6 are performed through
multiplication −qrq* (Equation (9)). We propose that the quaternion symbol q be used for
coding the natural rotations and the negative sign before quaternion, −q, for the improper
rotations. As pointed before, other multiplication types are also possible, but they are
simplifications of Equations (2) and (9); for example, the simplification qrq applies to the
quaternion operations consisting of imaginary components only (Equation (7)).
It should be noted that the multiplications of quaternions representing natural rotations yield either 1 or −1 (cf. Equation (3a). For example, the double rotation of the
multiplication q(180◦ ,[z])·q(180◦ ,[z]) equals −1. However, this negative sign of the combined quaternion would compensate in the transformation (Equation (2)); hence, it can be
ignored in the multiplication table. It illustrates that the quaternions cannot be considered
separately from their transformation types.
Figure 1 and Table 7 illustrate the informative concise quaternions applied as operation
symbols used in the multiplication table for symmetry class mmm (Schönflies symbol D2h ).
Below, by using various symmetry operations in the quaternion representation, the Miller
indices of orthorhombic bipyramid faces have been indexed. Instead of general Miller
indices (hkl), in order to avoid their confusion with the quaternion symbols, we transformed
unit face (1 1 1) to complete its family of planes {1 1 1}:
i(i + j + k)(−i) = (−1 + k – j)(−i) = i – j – k, corresponding to face (1 1 1);
i(i + j + k)(i) = (−1 + k – j)(i) = −i + j + k, corresponding to face (1 1 1);
j(i + j + k)(−j) = (−k – 1 + i)(−j) = −i + j – k, corresponding to face (1 1 1);
j(i + j + k)(j) = (−k – 1 + i)(j) = i – j + k, corresponding to face (1 1 1);
k(i + j + k)(−k) = (j – i – 1)(−k) = −i – j + k, corresponding to face (1 1 1);
−1(i + j + k) = −i – j – k, corresponding to face (1 1 1);
−1(−i – j + k)= i – j− k, corresponding to face (1 1 1).

## PDF page 10

0 0 1
0
0 −1 1
1
−1
−1
0 0
1
0 0 1
−1
1
0 −1 0
−1 = 0 −1 0 1 , −1 =
0
0 1
0
0 1 1
1
1
−1
0
0 −1
1
0 −1
0 −1 .
1 =
0
0 −1
1
−1

Symmetry 2024, 16, 818

1
1
1 ,
1

0 0 −1 1
−1
−1
0
0 1
−1
0 1 ,
−1 = 0 −1
0
0 −1 1
−1
10 of 14

Figure1.1.An
Anorthorhombic
orthorhombicbipyramid
bipyramidwith
withits
itssymmetry
symmetryelements
elementsindicated
indicatedas
asquaternions:
quaternions:2-fold
2-fold
Figure
axes arrows and quaternions (indicated in blue); the mirror-plane quaternions (perpendicular to [x],
axes arrows and quaternions (indicated in blue); the mirror-plane quaternions (perpendicular to [x],
[y] and [z]) running along the edges of the bipyramid are indicated in red (cf. Table 7).
[y] and [z]) running along the edges of the bipyramid are indicated in red (cf. Table 7).
Table 7. Multiplication table for the symmetry operations of point group mmm. Hermann–Mauguin
Table
7. Multiplication
for thewith
symmetry
operationsinofthe
point
group
mmm.
symbols
of symmetry table
operations
their directions
indices
are
listedHermann–Mauguin
in the top row and
symbols
of and
symmetry
operations
with their
directions
indices
the top
row
and
left
column,
their
products are
represented
as in the
quaternions
inare
thelisted
tableinbody.
The
proper
left
column,
their (Equation
products (2)
are should
represented
as while
quaternions
the table
Theimproper
proper
rotations
areand
positive
be used),
the in
negative
sign body.
indicates
rotations are
(Equation
(9)).
rotations
positive
(Equation (2) should be used), while the negative sign indicates improper
rotations (Equation (9)).
Symmetry Operation
1
1
2[100]
2[010]
2[001]
m[100]
m[010]
m[001]

Symm. operation
1 1
1
1 −1
1
2[ ] 1
−1
i
2[ ]−i
j
2[ ]− j
k
k
𝑚[ −
]
−i
i
𝑚[ ]
−j
j
𝑚[ ]
−k

k

1
1
12[100] −1
−1i
1
𝑖 −i −𝑖
𝑗 1 −𝑗
𝑘 k −𝑘
−𝑖 j
𝑖
−1
𝑗
−𝑗
−k
−𝑘− j 𝑘

2[

]

2[010𝑖 ]
j−𝑖
− j1
k𝑘
1𝑗
i
−1
−k
−𝑘
−1
−𝑗
i

2[

]

𝑗2[001]
−𝑗k
𝑘−k
1j
𝑖 i
−𝑘1
−j
−1
−i
𝑖 −1

2[

𝑚[ ]
𝑚[ ]
]
𝑘 m[100] −𝑖 m[010]−𝑗
−𝑘 −i
𝑖
−j 𝑗
i
j −𝑘
𝑗
−1
−k −1
𝑖 −1 −𝑘
−1 −𝑖
1 −k −𝑗
−
j
−i 𝑘
1
−𝑗
1
k
−𝑖
𝑘
1
k
1
−1 j
𝑗
𝑖
i

𝑚[

]

−𝑘]
m[001
−k𝑘
k−𝑗
− j−𝑖
−−1
i
−1𝑗
j
𝑖
i
1
1

Each of the quaternion operations requires either six or three quaternion
The
corresponding
matrix
are
multiplications,
whereas all
theoperations
vector-by-matrix
multiplications above require nine scalar
  
    
    
 
multiplications
and
six
additions.
1
1
0
0
1
−1
−1 0 0
1
−1
−1 0
0
1
= 0
 1,
 1  = for0the1 4-fold
,
−1The
 1,  1
quaternion
become
somewhat
complicated
rotations
= 0 −
1
0symbols
1 0more
0  1
−1 the 0
0 −1
1
0 0 1
1
0 0for−1
and
symmetry
elements
of 1the diagonal
directions,
as−1exemplified
point 1group
  
    
    
 
1 in 1
−1 of0 its0
1
−1 in Table
−1 8. 0
0
42𝑚
Figure0 2 0and 1the −1
multiplication
quaternions
However,1 the
 −1 = 0
1
0
 
1
−1
 1 =  0
−1
0


−1
0

0 1,  −1 =  0
1
1
1
0
 
0
0
−1
−1
0   −1.
0 −1
1

−1
0

0 1,  −1 =  0
1
1
−1
0

−1
0

0  1,
−1
1

Each of the quaternion operations requires either six or three quaternion multiplications,
whereas all the vector-by-matrix multiplications above require nine scalar multiplications and
six additions.

## PDF page 11

Symmetry 2024, 16, 818
Symmetry 2024, 16, x FOR PEER REVIEW

11 of 14
11 of 14

The quaternion symbols become somewhat more complicated for the 4-fold rotations and the
symmetry
elements
of the diagonal
directions,
exemplified
for is
point group
42m or
in Figure
information
explicitly
contained in
the as
quaternion
symbol
comparable
higher2 and
than
the
multiplication
of its
quaternions
Table
8. However,
the information
explicitly
contained
the
quaternion
(i +inj)/√2
in other
notations.
For
example,inthe
symbols
of 2-fold
axis 2[110] and
quaternion symbol is comparable or higher
than
in
other
notations.
For
example,
the
symbols
of
√
contain a similar number of alphanumerical
symbols, but the quaternion symbols could
2-fold axis 2[110] and quaternion (i + j)/ 2 contain a similar number of alphanumerical symbols,
√
be further simplified by applying abbreviations, such as p = 1/ √2 for
normalizing
but the quaternion symbols could be further simplified by applying abbreviations,
such as√
p = 1/ 2
be
diagonal
planes
or s planes
= 1/2 (see
quaternion
symbol
(i (i+ +j)/√2
for
normalizing
diagonal
or s =Tables
1/2 (see4–6).
TablesSo,
4–6).
So, quaternion
symbol
j)/ 2can
can be
shortened
to
(i
+
j)p.
shortened to (i + j)p.

Figure2.2.Cyclographic
Cyclographicprojection
projectionofofpoint
pointgroup
group42m
42𝑚
with
indicated
quaternion
representations
Figure
with
indicated
quaternion
representations
of
of
the
symmetry
elements:
proper
rotations
are
blue
and
improper
rotations
are
red
(cf. Table
8).
the symmetry elements: proper rotations are blue and improper rotations are red (cf. Table
8). The
The conventional orientation of the reference system (axis [y] across the page and [x] down) is is
conventional orientation of the reference system (axis [y] across the page and [x] down) is is apparent
apparent from the quaternion symbols.
from the quaternion symbols.
Table 8. Multiplication table of symmetry operations in point group 42𝑚, with the Hermann–
Table
8. Multiplication
of symmetry
operations
in point
group
the Hermann–
[100]·41[001] is −(i + j)/√2
Mauguin
symbols in thetable
left column
multiplied
by this from
the top
row,42m,
e.g., 2with
1
Mauguin
symbols
in
the
left
column
multiplied
by
this
from
the
top
row,
e.g.,
2[100] · 4of
1
[001]
[100] is −(i − j)/√2 in this non-Abelian
point group. Quaternion representations
the
and 4 [001]·2√
√
isymmetry
− (i + j)/operations
2 and 41 are
· 2 the
is − (ibody;
− j)/the 2quaternions
in this non-Abelian
point
group.operations
Quaternion
representing
improper
are
[001]in
[100] table
representations
thesign.
symmetry operations are in the table body; the quaternions representing
marked
by the of
minus
improper operations are marked by the minus sign.
Symmetry Operation

Symm.
1
operat.

41 [001]

1

− 1 √+ k

1
41 [001]

1

1

1

− 1 √+ k

2

− √

2[100]

i

422[001]

2[010]

1

𝑘i + j

− √

2

𝑘 i−√−1j

4j 3[001] − − 2
√2
i+j
√
j

m[110]

−

m[110]

− √[

−

2
i2− j ]
2

𝑖i

2[

𝑗

]

42[001] 3
𝑘

√2
− k √− 1
𝑘

2

1

43[001]

4 [001]

1 + 𝑘k

1+𝑘

4k 1[001] − − k √− 1
√2 2
k−1

43 [001]

4 [001]

k

2

42 [001]

41[001]2

−

2[

− k√−1 𝑘 − 1 i
2−

𝑘−1

1

− 1 √+ k

√2

2

]

2[100]

𝑖

2[

]

2[010]
j

j −

√2

i−

𝑗

√2

i−j
− √𝑖
2

i+j
i−j
k
− √
𝑘 − 11√+2 k
1 + 𝑘− √2
2 𝑖
−
𝑗
1 i − j−
1
k
− √
√2 j
√2
2
𝑖−𝑗
𝑖+𝑗
1 + 𝑘 i √+ j
k −
1−
−
1 i −
𝑘
2
√2 − j
i−j
1√
− k √2 − 1 √
+ k √2
− 𝑗√
𝑖 − 𝑗− 2
𝑖+
2
2
− − i √+ j
𝑗
1√
+k 1
j −
− 1 √− k 𝑘
√2 2
√2 − 2
2

−

𝑖−𝑗

𝑖

−

𝑖+𝑗

𝑘

]

i+j
− −√𝑖 + 𝑗
2

i+j
√2 − i √− j
− √
2 𝑖−𝑗
2𝑖 +𝑗

1

𝑚[

m[110]

1

i √2

𝑚[

m[110]

]

i𝑖−−
√j 𝑗
−
− 2

j √2

i+j
− √𝑗
2

j 𝑖−𝑗
−
k
− 1 √+ √2
2

i𝑖 + 𝑗
−1 − k
− √√2
2

− 1 √− 𝑗k

− 1 √+𝑖 k

1

k

2

−k
−

1+𝑘
√2
1−𝑘

2

1−𝑘

−1
−

√2
1+𝑘

√2 and matrix representations
√2
√2
Below, the quaternion
of the symmetry operations
are √2
com𝑖+𝑗
𝑖−𝑗
1molecule.
−𝑘
1We
+𝑘
pared
for
generating
equivalent
atomic
positions
in
a
chose
the
S
-symmetric
𝑚[ ] −
−
−
−
−𝑗
𝑗
1 4
𝑘
√22 OH)4 , located on √2
√2 the four-fold inversion
molecule of √2
pentaerythritol, C(CH
the centre of
𝑗 structure, of 𝑖 +
𝑗
−k
axis in the 𝑖 −
crystal
tetragonal
space-group1 + k
symmetry1I4
[22]. Atom C1 at special
𝑚[ ] −
−
−
−
𝑖
𝑗
𝑘
1
position [000]√2
transforms into itself
(hence
its
site
occupation
factor
√2
√2
√2is ¼, cf. Figure 3), while
the methanol group is located in the general position [xyz] and it transforms to the equivalent
positions
[xyz] A
and [xyz]
operation
4 1 [001]
according to
Equation
C through
Below,
the, [xyz]B
quaternion
and
matrix quaternion
representations
of the
symmetry
operations
are
2
(6):
[xyz]
=
−
(1
+
k)
·
[xi
+
yj
+
zk]
·
(1
–
k)/2
=
j
–
i
–
k
(cf.
Table
8);
operation
4
according
A
[001]
compared for generating equivalent atomic positions in a molecule. We chose the Sto4symmetric molecule of pentaerythritol, C(CH2OH)4, located on the centre of the four-fold

## PDF page 12

Symmetry 2024, 16, 818

inversion axis in the crystal structure, of tetragonal space-group symmetry I4 [22]. Atom
C1 at special position [000] transforms into itself (hence its site occupation factor is ¼, cf.
Figure 3), while the methanol group is located in the general position [xyz] and it
transforms to the equivalent positions [xyz]A, [xyz]B and [xyz]C through quaternion
12 of 14
operation 41[001] according to Equation (6): [xyz]A = −(1 + k)·[xi + yj + zk]·(1 − k)/2 = j − i − k
(cf. Table 8); operation 42[001] according to Equation (2): [xyz]B = k·[xi + yj + zk]·(−k) = −i − j +
3
as (1
k)·[xi
+ k)
yj =+ −
zk]·(1
j + i − k or43simpler
k·[xi + yj + zk]A·(−k).
k;Equation
and operation
(2): [xyz]4B [001]
= k · [xi
+ yj− +
zk] · ( −
i – j ++k;k)/2
and−operation
[001] as (1 – k) · [xi + yj +
zk] · (1 +
k)/2 – j + i –
k or simpler
k · [xi + yj +of
zk] A ·
( − k).4 The
equivalent
matrix representations
The
equivalent
matrix
representations
these
operations
are
of these 4 operations are

0 1 0
−1 0 0
0 −1 0



2
3
,
4
and
4
4 =0 −11 0
=
=
0
0
−1
0
0 .
0
−1
0 0
0 −11 00
1
2
3
0 ,−1
00 .−1
and 4 = 1 00
4 = −1 00 0
4 =  0 0−1 0
0 1
1

0

0

−1

0

0

1

0

0

−1

(a)

(b)
Figure
Space-filling
model
thethe
pentaerythritol
its SS44 axis,
Figure3.3.(a) (a)
Space-filling
modelofof
pentaerythritolmolecule
molecule viewed
viewed along
along its
axis, as
aspresent
in the
crystal
structure at
1.15at GPa
[23];[23];
code
of of
colours:
H,light
lightgrey,
grey,
present in
the crystal
structure
1.15 GPa
code
colours:C,C,dark
dark grey,
grey, H,
O, O,
red;red; (b)
autostereographic
projection
the crystal
crystalstructure,
structure,
space
group
I4, with
represented
as
(b)
autostereographic
projection[24]
[24] of
of the
space
group
I4, with
atomsatoms
represented
as
capped
colouredasas
indicated
above,
hydrogen
bonds
OH···O
are
cyan;labels
atomic
labels
cappedsticks
sticks coloured
indicated
above,
hydrogen
bonds OH
···O are
cyan;
atomic
C1 (C2
H1 C1 (C2
H1
O1 with
H3) no
with
with additional
letters
A, B equivalent
and C indicate
H2H2
O1 H3)
and no
withand
additional
letters A, B and
C indicate
methanolequivalent
substituents.methanol
substituents.
3. Conclusions
The quaternion representations of symmetry operations in crystallographic reference systems
3. Conclusions

are attractive for several reasons, such as their easy intuitive construction, direct connections with
The quaternion
representations
of symmetry
reference
the rotation
axis orientation
and rotation angles
as well as operations
the simplicityin
ofcrystallographic
performing arithmetic
systems
are
attractive
several
reasons,
as their
intuitivereference
construction,
operations
required
for for
transforming
vectors
in bothsuch
Cartesian
and easy
crystallographic
systems. direct
Most
importantly,
quaternions
are an
alternative
to the and
matrixrotation
representation
of as
symmetry
operations,
connections
with the
rotation
axis
orientation
angles
well as the
simplicity
except the hexagonal reference system. The two different, matrix and quaternion, representations give
of performing arithmetic operations required for transforming vectors in both Cartesian
the opportunity to choose the one more appropriate for performing crystallographic, diffractometric
and
crystallographic
reference
systems.
Most
importantly,
quaternions
are an alternative
or any
numerical calculations
involving
symmetry
operations
in triclinic,
monoclinic, orthorhombic
to the
matrix
representation
symmetry
operations,
except
hexagonal
reference
tetragonal,
cubic and
rhombohedral of
lattices. In
these systems,
owing to
the the
simplicity of
quaternions’
notation, it
can
be used
instead of
symmetry
symbols, for
example, give
inmultiplication
table
system.
The
two
different,
matrix
and operation
quaternion,
representations
the
opportunity to
of quaternions,
to Cayley tables
multiplied symmetry
operations diffractometric
or for the symbols or any
choose
the oneanalogous
more appropriate
for of
performing
crystallographic,
of cyclic crystallographic classes. Therefore, the direct application of quaternions for symmetry
numerical
calculations involving symmetry operations in triclinic, monoclinic,
transformations of vectors in crystal reference systems appears very attractive.

## PDF page 13

Symmetry 2024, 16, 818

13 of 14

However, there are important limitations of the quaternion representation of symmetry
operations. In particular, the point-symmetry operations in the quaternion representation do
not fulfil all requirements of the algebraic group, because two types of the multiplication actions
are required for distinguishing proper and improper rotations. Moreover, the quaternion representations for the crystallographic hexagonal reference system have still not been resolved, and
further studies aimed at the complete quaternion representations of all symmetry operations in
crystallographic reference systems are required. The inadequacy of quaternions for generally
representing the symmetry operations in all crystallographic reference systems is likely the main
handicap for the common use of quaternions in crystallography [18,20], while they are thriving in
other applications not requiring non-Cartesian reference systems [3–8]. Nonetheless, as presented
in our study, even in the present incomplete compilation, the elegant form of quaternion rotations
is appealing for their crystallographic applications.
Author Contributions: Conceptualization, methodology, validation: A.K. Writing—original draft
preparation, writing—review and editing, visualization: A.K. and S.L. All authors have read and
agreed to the published version of the manuscript.
Funding: This research was funded by the Polish Ministry of Higher Education, through the statutory
fund of the Adam Mickiewicz University in Poznań.
Data Availability Statement: Data are contained with the article.
Acknowledgments: The authors are grateful to Quy Hien Le for reading the manuscript and for the fruitful
discussions. S.L. participated in the Erasmus Mundus SERP+ program, http://www.master-serp.eu.
Conflicts of Interest: The authors declare no conflicts of interest. The funder had no role in the design
of the study; in the collection, analyses, or interpretation of data; in the writing of the manuscript; or
in the decision to publish the results.

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

Rodrigues, O. Des lois géometriques qui regissent les déplacements d‘un systéme solide dans l‘espace, et de la variation des
coordonnées provenant de ces déplacement considérées indépendant des causes qui peuvent les produire. J. Math. Pures Appl.
1840, 5, 380–440.
Hamilton, W.R. Lectures on Quaternions; Hodges and Smith: Dublin, Ireland, 1853.
Altmann, S.L. Rotations, Quaternions, and Double Groups; Clarendon Press: Oxford, UK, 1986.
Altmann, S.L. Hamilton, Rodrigues and the quaternion scandal. Math. Mag. 1986, 62, 291–308. [CrossRef]
Shaw, J.B. Vector Calculus with Applications to Physics; D. van Nostrand Company: New York, NY, USA, 1922.
Hanson, A. Visualizing Quaternions; Morgan-Kaufmann/Elsevier: New York, NY, USA, 2006; ISBN 9780080474779.
Girard, P.R. Quaternions, Clifford Algebras and Relativistic Physics; Birkhäuser Verlag AG, Basel-Boston-Berlin: Basel, Switzerland,
2007; ISBN 978-3-7643-7790-8.
Bród, D. On some combinatory properties of balancing split quaternions. Symmetry 2024, 16, 373. [CrossRef]
Thomas, D.J. Modern equations of diffractometry. Goniometry. Acta Cryst. A 1990, A46, 321–343. [CrossRef]
White, K.I.; Bugris, V.; McCarthy, A.A.; Ravelli, R.B.G.; Csankó, K.; Cassetta, A.; Brockhauser, S. Calibration of rotation axes for
multi-axis goniometers in macromolecular crystallography. J. Appl. Cryst. 2018, 51, 1421–1427. [CrossRef] [PubMed]
Grimmer, H. Disorientations and coincidence rotations for cubic lattices. Acta Cryst. A. 1974, A30, 685–688. [CrossRef]
Bonnet, R. Disorientation between any two lattices. Acta Cryst. A 1980, A36, 116–122. [CrossRef]
Clegg, W. Orientation matrix refinement during four-circle diffractometer data collection. Acta Cryst. A 1984, A40, 703–704. [CrossRef]
Mackay, A.L. Quaternion transformation of molecular orientation. Acta Cryst. A 1984, A40, 165–166. [CrossRef]
Diamond, R. A note on the rotational superposition problem. Acta Cryst. A 1988, A44, 211–216. [CrossRef]
Theobald, D.L. Rapid calculation of RMSDs using a quaternion-based characteristic polynomial. Acta Cryst. A 2005, A61,
478–480. [CrossRef] [PubMed]
Hanson, A.J. The quaternion-based spatial-coordinate and orientation-frame alignment problems. Acta Cryst. A 2020, A76,
432–457. [CrossRef] [PubMed]
Bernal, J.D. The Analytic Theory of Point Systems. 1923. Unpublished. Available online: https://www.iucr.org/__data/assets/
pdf_file/0008/25559/Bernal_monograph.pdf (accessed on 30 May 2024).
Fritzer, H.P. Molecular symmetry with quaternions. Spectrochim. Acta A 2001, 57, 1919–1930. [CrossRef] [PubMed]
West, R.H. Quaternion Representation of Crystal Point Groups. Ph.D. Thesis, North Texas State College, Denton, TX, USA, 1959.
Available online: https://digital.library.unt.edu/ark:/67531/metadc108066/ (accessed on 30 May 2024).
Rollett, J.S. Computing Methods in Crystallography; Pergamon Press: London, UK, 1965; pp. 22–23.
Llewellyn, F.J.; Cox, E.G.; Goodwin, T.H. 183. The crystalline structure of the sugars. Part IV. Pentaerythritol and the hydroxyl
bond. J. Chem. Soc. 1937, 883–894. [CrossRef]

## PDF page 14

Symmetry 2024, 16, 818

23.
24.

14 of 14

Katrusiak, A. High-pressure X-ray diffraction study of pentaerythritol. Acta Crystallogr. B 1995, B51, 873–879. [CrossRef]
Katrusiak, A. Crystallographic autostereograms. J. Mol. Graphics Modell. 2001, 19, 363–367. [CrossRef] [PubMed]

Disclaimer/Publisher’s Note: The statements, opinions and data contained in all publications are solely those of the individual
author(s) and contributor(s) and not of MDPI and/or the editor(s). MDPI and/or the editor(s) disclaim responsibility for any injury to
people or property resulting from any ideas, methods, instructions or products referred to in the content.
