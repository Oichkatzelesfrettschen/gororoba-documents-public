Source: see manifest row of the PDF
PDF sha256: 4f8311c70a752cbb1f244c1b7deab52f49fe8bbad207d206391a532254cafa53
License: public domain (L. E. Dickson, Linear Algebras, Cambridge Tracts 16 (1914); Dickson died 1954)
Language: eng
Fidelity: machine (failed: characters)

# Transcription of dickson_1914_linear_algebras.pdf

Transcription of `dickson_1914_linear_algebras.pdf` in this directory, 92 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 1-92 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories. No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

w
761
NIVERSITY OF

00470005

TORONTO

并

0




460000000

廽

, ($)
79<br>7487

## PDF page 2

.
×
.
*
.
-

-
.
.
4
.
.
-
.
.
1

## PDF page 3

×
×

## PDF page 4

Digitized by the Internet Archive
in 2007 with funding from
Microsoft Corporation
. .
1
.
.
.
http://www.archive.org/details/linearalgebras00dickuoft
1

## PDF page 5

1214
8
Cambridge Tracts in Mathematics
and Mathematical Physics
GENERAL EDITORS
G. H. HARDY, M.A., F.R.S.
J. G. LEATHEM, M.A.
DAMERSON TO STREET BRIDES
A. A. CELLEY PRODUCES
A THE LANGE CONTRACTOR
CHARLES AND ACTION OF THE PERSON OF
No. 16
LINEAR ALGEBRAS
REDE LESS STEEL AND SERVICE
AND THE RESIDENCE STREET, THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF T
all the second second
AND DESCRIPTION OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PART
CONTRACTOR OF THE PARTY.

## PDF page 6

CAMBRIDGE UNIVERSITY PRESS
C. F. CLAY, MANAGER,
London: FETTER LANE, E.C.
Edinburgh: 100 PRINCES STREET
Berlin: A. ASHER AND CO.
Leipzig: F. A. BROCKHAUS
New York: G. P. PUTNAM'S SONS
Bomban and Calcutta: MACMILLAN AND CO., LID.
Toronto: J. M. DENT AND SONS, LTD.
Tokyo: THE MARUZEN-KABUSHIKI-KAISHA
.
All rights reserved

## PDF page 7

111
LINEAR ALGEBRAS
by
L. E. DICKSON, Ph.D.
Professor of Mathematics in the University of Chicago
Cambridge:
143249
at the University Press
1914

## PDF page 8

-
1 200
Cambridge:
PRINTED BY JOHN CLAY, M.A.
AT THE UNIVERSITY PRESS
QA<br>251<br>D5
.


4
5 0.7 4
.

## PDF page 9

V
PREFACE
THE theory of linear associative algebras (or closed systems of
hypercomplex numbers) is essentially the theory of pairs of
reciprocal linear groups (§ 52) or the theory of certain sets of matrices
or bilinear forms (§ 53). Beginning with Hamilton's discovery of
quaternions seventy years ago, there has been a rapidly increasing
number of papers on these various theories. The French Encyclopedia
of Mathematics devotes more than a hundred pages to references and
statements of results on this subject (with an additional part on
ordinary complex numbers). However, the subject is rich not merely
in extent, but also in depth, reaching to the very heart of modern
algebra.
The purpose of this tract is to afford an elementary introduction
to the general theory of linear algebras, including also non-associative
algebras. It retains the character of a set of lectures delivered at the
University of Chicago in the Spring Quarter of 1913. The subject is
presented from the standpoint of linear algebras and makes no use
either of the terminology or of theorems peculiar to the theory of
bilinear forms, matrices or groups (aside of course from § 52-54, which
treat in ample detail of the relations of linear algebras to those
topics).
Part I relates to definitions, concrete illustrations, and important
theorems capable of brief and elementary proof. A very elementary
proof is given of Frobenius's theorem which shows the unique place of
quaternions among algebras. The remarkable properties of Cayley's
algebra of eight units are here obtained for the first time in a simple
manner, without computations. Other new results and new points of
view will be found in this introductory part.
In presenting in Parts II and IV the main theorems of the general
theory, it was necessary to choose between the expositions by Molien,
Cartan and Wedderburn (that by Frobenius being based upon bilinear
forms and hence outside our plan of treatment). We have not pre-
sented the theory of Molien partly because his later proofs depend

## PDF page 10

vi
PREFACE
upon the theory of groups and partly because certain of his earlier
proofs have not yet been made correctly by his methods. The more
general paper by Wedderburn is based upon a rather abstract calculus
of complexes, comparable with the theory of abstract groups (§ 61). In
compensation, he obtains in relatively brief space the main theorems
not only for the usual cases of complex and real algebras, but also for
algebras the coordinates of whose numbers range over any field (stated
in § 56).
In order that our treatment of the general theory shall be ele-
mentary and concrete and shall use but a very few concepts easily kept
in mind, we have confined our exposition (in Part II) to the classical
case of algebras whose numbers have ordinary complex coordinates
and given a careful revision of the theory as presented in Cartan's
fundamental paper. Running parallel with the general theory is an
illustrative example treated independently but in the spirit of the
theory. While we thereby lose the generalization to a general field,
we gain the important normalized sets of units, first given by Scheffers
under certain restrictions, and so obtain the analogues of important
theorems on the canonical forms of groups of linear transformations or
of sets of matrices or bilinear forms.
I am much indebted to Professor Wedderburn of Princeton and
Miss Hazlett of Chicago for suggestions made after careful readings of
the proofs. My thanks are due to the editors for the opportunity to
participate in this useful series of tracts. Finally, I am under obliga-
tions to the officials of the University Press for complying with all of
my requests as regards the form of this tract, and for expeditious
publication in spite of the distance travelled by the proofs. The
quality of the printing speaks for itself.
L. E. D.
CHICAGO,
May, 1914.

## PDF page 11

1
CONTENTS
PAGE
PREFACE .
V
PART I.
DEFINITIONS, ILLUSTRATIONS AND ELEMENTARY THEOREMS
SECT.
Ordinary complex numbers, number fields
1, 2.
1
Matrices; matric algebra as a linear algebra
3, 4.
<math>^{3}</math>
.
Definition of linear algebras, coordinates, units
5.
5
Division; principal unit; transformation of units
<math>6-8.</math>
7
Equations and polynomials in a single number
<math>9-10.</math>
9
11.
Unique place of quaternions among algebras
10
.
12, 13.
Properties of quaternions, relation to matrices.
12
14.
Cayley's generalization of real quaternions
14
<math>15-17.</math>
Characteristic determinants; invariance.
16
18.
Binary algebras.
21
. . .
.
19.
Rank and rank equation of an algebra
21
.
20.
Ternary algebras with a modulus
23
.
.
.
Reducibility, direct sum, direct product .
26
21, 22.
.
Units normalized relative to a number; example
29
23, 24.
REVISION OF CARTAN'S GENERAL THEORY OF COMPLEX
PART II.
LINEAR ASSOCIATIVE ALGEBRAS WITH A MODULUS
33
<math>25-27.</math>
Units having a character; example.
36
Nilpotent numbers, normalized units; examples
28-34.
38
35.
Separation of algebras into two categories.
38
<math>36 - 38.</math>
Algebras <math>A_1</math> of first category, nilpotent algebras
44
39.
Normalized units for <math>A_1</math>
.
46
Algebras <math>A_2</math> of the second category
<math>40-45.</math>
ě.
50
46.
Any <math>A_2</math> has a quaternion sub-algebra
51
Normalized units for <math>A_2</math>; determinant
47, 48.
55
Invariant sub-algebra, simple algebras
49.
56
50-51.
Main theorem; commutative case

## PDF page 12

viii
CONTENTS
PART III. RELATIONS OF LINEAR ALGEBRAS TO OTHER SUBJECTS
PAGE
SECT.
Linear associative algebras and linear groups .
58
52.
Linear associative algebras and bilinear forms.
53.
62
Relations of linear algebras and finite groups .
63
54.
.
Dedekind's view for commutative associative algebras
55.
64
Part IV. Linear Algebras over a Field <math>F</math>
56.
Statement of main theorem; real simple algebras
66
Algebras of Weierstrass
57.
68
.
.
Division algebras
<math>58-60.</math>
69
.
- 1
.
.
.
Statement of further results
61.
72
. .
.
Analytic functions of hypercomplex numbers .
62.
73
N

## PDF page 13

20
PART I
DEFINITIONS, ILLUSTRATIONS AND ELEMENTARY
THEOREMS
1.
Arithmetical definition of ordinary complex numbers.
The following purely arithmetical theory of couples (a, b) of real
numbers differs only in unessential points from the initial theory of
W. R. Hamilton*. Two couples (a, b) and (c, d) are called equal if
and only if <math>a = c</math>, <math>b = d</math>. Addition, subtraction and multiplication of
two couples are defined by the formulast
<math>(a, b) + (c, d) = (a + c, b + d)</math>
<math>(a, b) - (c, d) = (a - c, b - d)</math>
(1).
<math>(a, b) (c, d) = (ac - bd, ad + bc)</math>
Addition is seen to be commutative and associative:
<math>x + x' = x' + x</math>, <math>(x + x') + x'' = x + (x' + x'')</math>
(2),
where x, x', x" are any couples. Multiplication is commutative,
associative and distributive:
<math>xx' = x'x</math>, <math>(xx') x'' = x(x'x'')</math>
(3),
<math>x(x' + x'') = xx' + xx'', (x' + x'') x = x'x + x''x</math>
(4).
* Trans. Irish Acad., vol. 17 (1837), p. 293; Lectures on Quaternions, 1853,
Preface.
+ Each couple (a, b) uniquely determines a vector from the origin O to the
point A with the rectangular coordinates a, b. The sum of two vectors from 0 to
A and the point <math>C=(c, d)</math> is defined to be the vector from O to the fourth vertex S
of the parallelogram having the lines OA and OC as two sides. The coordinates
of S are <math>a+c</math>, <math>b+d</math>.
Subtraction of vectors is the operation inverse to addition;
thus <math>OS - OA = OC</math>.
To define the product of the vectors from O to A and C, we
employ initially the polar coordinates <math>r</math>, <math>\theta</math> and <math>r'</math>, <math>\theta'</math> of <math>A</math> and <math>C</math>. Then <math>OA</math>. <math>OC</math> is
defined to be the vector from O to the point P with the polar coordinates rr,
<math>\theta + \theta'</math>. Since A has the rectangular coordinates <math>a = r \cos \theta</math>, <math>b = r \sin \theta</math>, and similarly
for C and P, the expansions of <math>\cos (\theta + \theta')</math> and <math>\sin (\theta + \theta')</math> lead to the third relation
(1) between the rectangular coordinates of A, C, P.
D.
1

## PDF page 14

[(5)]
ORDINARY COMPLEX NUMBERS
2
Division is defined as the operation inverse to multiplication.
Division except by (0, 0) is possible and unique:
<math display="block">\frac{(c,d)}{(a,b)} = \left(\frac{ac+bd}{a^2+b^2}, \frac{ad-bc}{a^2+b^2}\right)</math>
(5).
In particular, we have
<math>(a, 0) \pm (c, 0) = (a \pm c, 0), \quad (a, 0) (c, 0) = (ac, 0),</math>
<math>\frac{(c, 0)}{(a, 0)} = \left(\frac{c}{a}, 0\right)</math> if <math>a \neq 0</math>.
Hence the couples (a, 0) combine under the above defined addition,
multiplication, etc., exactly as the real numbers a combine under
ordinary addition, multiplication, etc. Without introducing any con-
tradiction, we may and shall impose upon our system of couples <math>(a, b)</math>,
subject to the above definitions of addition, etc., the further assumption *
that the couple <math>(a, 0)</math> shall be the real number <math>a</math>. For brevity write <math>i</math>
Then
for <math>(0, 1)</math>.
<math>i^2 = (0, 1)(0, 1) = (-1, 0) = -1,</math>
<math>(a, b) = (a, 0) + (0, b) = a + (b, 0) (0, 1) = a + bi.</math>
Relations
The resulting symbol <math>a + bi</math> is called a complex number.
(1) and (5) now take the familiar forms
<math display="block">(a+bi)\pm(c+di) = (a\pm c) + (b\pm d)i</math>
<math display="block">(a+bi) \pm (c+di) = (a \pm c) + (b \pm a) i</math><br>
<math display="block">(a+bi) (c+di) = (ac-bd) + (ad+bc) i</math>
(6),
<math>\frac{c+di}{a+hi} = \frac{ac+bd}{a^2+b^2} + \frac{ad-bc}{a^2+b^2}i</math>
where, for the last, <math>a + bi \neq 0</math>, i.e. <math>a</math> and <math>b</math> are not both zero.
Number fields. A set of complex numbers is called a
2.
number field (domain of rationality or Körper) if the rational
operations can always be performed unambiguously within the set.
In other words, the sum, difference, product and quotient (the divisor
not being zero) of any two equal or distinct numbers of the set must
be numbers belonging to the set.
In view of (6), all complex numbers <math>a + bi</math> form a field. Again,
all real numbers form a field. The set of all rational numbers is a
field, but the set of all integers is not.
* Just as the natural numbers are included among the signed integers, the
integers among the rational numbers, and the latter among the real numbers
defined by means of them. In the same train of ideas, 1 is often used to denote
the principal unit (§ 7, § 11), and the number <math>e</math> for the scalar matrix <math>S_e</math> (§ 4, second
foot-note).

## PDF page 15

§ 37
MATRICES
3
3.
Matrices. The concept matrix* affords an excellent in-
troduction to the subject of this tract and, moreover, is of special
importance in the general theory. We shall consider only square
matrices of n rows each containing n elements. For example, if
<math>n=2,</math>
<math>m = \begin{pmatrix} a & b \\ c & d \end{pmatrix}, \quad \mu = \begin{pmatrix} a & \beta \\ \gamma & \delta \end{pmatrix}</math>
(7)
are matrices, the elements of the first matrix m being a, b, c, d.
Each element may be any number of a given number field F.
We shall say that <math>m</math> and <math>\mu</math> are equal if and only if their corre-
sponding elements are equal, <math>a = a</math>, etc. Addition and multiplication
are defined by
<math>m + \mu = \begin{pmatrix} a + a & b + \beta \\ c + \gamma & d + \delta \end{pmatrix}, \quad m\mu = \begin{pmatrix} aa + b\gamma & a\beta + b\delta \\ ca + d\gamma & c\beta + d\delta \end{pmatrix}</math>
(8).
The element in the ith row and jth column of the product is the sum
of the products of each element of the ith row of the first matrix by
the corresponding element of the jth column of the second matrix,
i.e. first by first, second by second, etc. This rule holds also for
matrices of <math>n^2</math> elements. Of the four possible rules for expressing
the product of two determinants of order n as a determinant of
order n, the above is the only rule which holds also for matrices.
With the exception of (31), the laws (2)-(4) for addition and
multiplication hold for matrices. Since the product (82) is in general
altered when the Roman and Greek letters are interchanged, matric
multiplication is usually not commutative. Accordingly we shall see
that we must distinguish between two distinct kinds of division of
matrices.
To this end, note that
<math display="block">\begin{pmatrix} e & 0 \\ 0 & e \end{pmatrix} m = m \begin{pmatrix} e & 0 \\ 0 & e \end{pmatrix} = \begin{pmatrix} ea & eb \\ ec & ed \end{pmatrix}</math>
(9).
In particular, the unit matrix
<math>I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}</math>
(10)
has the property that <math>Im = mI = m</math>, for every matrix m. By the
inverse of a matrix m whose determinant <math>\Delta = |m|</math> is not zero is
Fleant
* Cayley, Phil. Trans. London, vol. 148 (1858), pp. 17-37 (=Coll. Math.
Papers, II, pp. 475, 604).
1-2

## PDF page 16

[(11)]
4
MATRICES
<math display="block">m^{-1} = \begin{pmatrix} \frac{d}{\Delta} & \frac{-b}{\Delta} \\ \frac{-c}{\Delta} & \frac{a}{\Delta} \end{pmatrix}</math>
(11),
if <math>n=2</math>, while if <math>n \equiv 2</math>, we employ as the element in the <i>i</i>th row and
jth column the quotient of the co-factor of the element in the jth
row and ith column of <math>\Delta</math> by <math>\Delta</math>. Then
<math>mm^{-1} = m^{-1}m = I</math>
(12).
Given two matrices m and p such that <math>|m| \neq 0</math>, we can find one
and only one matrix <math>\mu = m^{-1}p</math> such that <math>m\mu = p</math>, also one and only
one matrix <math>\nu = pm^{-1}</math> such that <math>\nu m = p</math>. These respective kinds of
division by <math>p</math> by <math>m</math> shall be called right-hand and left-hand division.
On the contrary, if <math>|m| = 0</math>, there is no matrix <math>\mu</math> for which <math>m\mu = I</math>,
since this would imply <math>0 |\mu| = |I| = 1</math>. Likewise, there is no matrix <math>\nu</math>
for which <math>\nu m = I</math>.
Thus right- and left-hand division by m are each always possible
and unique if and only if the determinant of m is not zero.
Addition, subtraction, multiplication and division of matrices with
elements in a field F lead to matrices with elements in F. Accordingly
we shall speak of the matric algebra over the field F. When F is the
field of all complex numbers, the field of all real numbers, or that of
all rational numbers, we have the complex, real or rational matric
algebra of square matrices of <math>n^2</math> elements.
A matric algebra viewed as a linear algebra*.
4.
Taking <math>n=2</math>, we shall make use of the particular matrices
<math>e_{11} = \begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix}, \quad e_{12} = \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix}, \quad e_{21} = \begin{pmatrix} 0 & 0 \\ 1 & 0 \end{pmatrix}, \quad e_{22} = \begin{pmatrix} 0 & 0 \\ 0 & 1 \end{pmatrix}</math>
(13).
Their sixteen products by twos are
<math>e_{ij}e_{jk}=e_{ik},\quad e_{ij}e_{tk}=0\quad (t\neq j)</math>
(14).
If m is a matrix and e is a number, we shall define the product t em
* For references, see § 13.
+ In the product (9) we may therefore replace the "scalar matrix" <math>\begin{pmatrix} e & 0 \\ 0 & e \end{pmatrix} = S_e</math>
by the number e. This becomes intuitive if we note that <math>S_e = eI</math>.
Since
<math>S_e + S_f = S_{e+f}</math>, <math>S_e S_f = S_{ef}</math>, etc., the algebra of all scalar matrices over a field F
is abstractly identical with F. This replacement of Se by e is similar to that of
<math>(a, 0)</math> by <math>a</math> in § 1.

## PDF page 17

<math>\S 4</math>
MATRIC ALGEBRA AS LINEAR ALGEBRA
5
or me to be the matrix each of whose elements is the product of e by
the corresponding element of <math>m</math>:
<math>e\begin{pmatrix} a & b \\ c & d \end{pmatrix} = \begin{pmatrix} a & b \\ c & d \end{pmatrix} e = \begin{pmatrix} ea & eb \\ ec & ed \end{pmatrix}</math>
(15).
In view of (13), matrices (7) and (8) may be expressed in the
form
<math>m = ae_{11} + be_{12} + ce_{21} + de_{22}</math>
(16),
<math>\mu = ae_{11} + \beta e_{12} + \gamma e_{21} + \delta e_{22}</math>
<math>m + \mu = (a + \alpha) e_{11} + (b + \beta) e_{12} + (c + \gamma) e_{21} + (d + \delta) e_{22}</math>
(17).
<math display="block">m\mu = (aa + b\gamma)e_{11} + (a\beta + b\delta)e_{12} + (ca + d\gamma)e_{21} + (c\beta + d\delta)e_{22}</math>
The last may also be found from (16) by use of relations (14).
The set of hyper-complex numbers <math>ae_{11} + ... + de_{22}</math>, in which <math>a, ..., d</math>
range independently over a field F, and for which addition and multi-
plication are defined by (17), is called a linear associative algebra
over <math>F</math> with the four units <math>e_{11}, ..., e_{22}</math> subject to the multiplication
table (14).
For any n, let <math>e_{ij}</math> be the square matrix of <math>n^2</math> elements all zero except
that in the ith row and jth column which is unity. Then relations (14)
hold. We obtain a linear associative algebra with <math>n^2</math> units <math>e_{ij}</math>.
General definition of hyper-complex numbers and
5.
linear algebras*. We shall generalize the notion of couples in § 1
and, with a change of notation, the notion of quadruples (7). Consider
the set of all n-tuples <math>(x_1, ..., x_n)</math>, whose coordinates <math>x_1, ..., x_n</math> range
independently over a given number field F.
Two n-tuples are called equal if and only if their corresponding
coordinates are equal.
Addition and subtraction of n-tuples are defined by
<math>(x_1, \ldots, x_n) + (x_1', \ldots, x_n') = (x_1 \pm x_1', \ldots, x_n \pm x_n')</math>
(18).
The product of any number <math>\rho</math> of the field <math>F</math> and any <math>n</math>-tuple
<math>x = (x_1, ..., x_n)</math>
is defined to be
(19).
<math display="block">\rho x = x \rho = (\rho x_1, \ldots, \rho x_n)</math>
* Hamilton's Lectures on Quaternions, 1858, Introduction. For definitions by
independent postulates, see Dickson, Trans. Amer. Math. Soc., vol. 4 (1903), p. 21;
vol. 6 (1905), p. 344.

## PDF page 18

6
GENERAL LINEAR ALGEBRA
[(20)]
The <i>n</i> units are defined to be
<math>e_1 = (1, 0, ..., 0), e_2 = (0, 1, 0, ..., 0), ..., e_n = (0, ..., 0, 1).</math>
Hence any <math>n</math>-tuple <math>x</math> can be expressed in the form
<math>x = x_1 e_1 + x_2 e_2 + \dots + x_n e_n</math>
We shall call x a hyper-complex number, or briefly a number.
In view
of the definition of equality of n-tuples, x and
<math>x' = x_1'e_1 + \ldots + x_n'e_n</math>
are equal if and only if <math>x_1 = x_1', ..., x_n = x_n'</math>. In particular, <math>x = 0</math>
implies that each <math>x_i = 0</math>. Hence the units <math>e_1, ..., e_n</math> are linearly in-
dependent with respect to the field <math>F</math>.
It is assumed that any two such numbers <math>x</math> and <math>x'</math> can be
combined by an operation called multiplication subject to the dis-
tributive laws (4):
<math display="block">xx' = \sum_{i=1}^{n} x_i x_i' e_i e_j,</math>
and such that the product <math>xx'</math> is a number <math>\Sigma z_i e_i</math> with coordinates in <math>F</math>.
Necessary conditions for the latter property are
<math>e_i e_j = \sum_{k=1}^{n} \gamma_{ijk} e_k</math>  <math>(i, j = 1, ..., n; \gamma' s \text{ in } F)</math>
(20).
These are sufficient conditions, since they imply
<math>xx' = y \equiv \sum y_k e_k, \quad y_k = \sum_{i=1}^n x_i x_i' \gamma_{ijk} \qquad (k = 1, ..., n)</math>
(21).
Properties (18) and (19) of n-tuples give
<math>x \pm x' = \sum_{i=1}^{n} (x_i \pm x_i') e_i, \quad \rho x = x \rho = \sum_{i=1}^{n} (\rho x_i) e_i</math>
(22),
if <math>\rho</math> is in <math>F</math>. The set of all numbers <math>\sum x_i e_i</math>, with coordinates in <math>F</math>,
combined under multiplication as in (21), under addition and sub-
traction as in <math>(22_1)</math>, and under multiplication by a number <math>\rho</math> of <math>F</math>
as in (222), shall be said to form a linear algebra (or system of
hyper-complex numbers) over the field <math>F</math>, with the units <math>e_1, \ldots, e_n</math>
(linearly independent with respect to <math>F</math>) and the multiplication table
(20). The <math>n^3</math> numbers <math>\gamma_{ijk}</math> are called the constants of multiplication.
Neither the commutative nor the associative law of multiplication is
assumed.

## PDF page 19

§ 5]
GENERAL LINEAR ALGEBRA
7
For example, the set of all ordinary complex numbers <math>a+bi</math> form a binary
linear algebra over the field F of all real numbers, with the units 1 and i
subject to the multiplication table
<math>1^2 = 1</math>, <math>1 \cdot i = i \cdot 1 = i</math>, <math>i^2 = -1</math>.
In this algebra (§ 1), multiplication is commutative and associative.
The
algebra is a field <math>F(i)</math> and may be viewed as a unary algebra over this
complex field with the single unit 1.
In § 4 we considered a linear associative algebra with four units.
Given two numbers <math>x</math> and <math>y</math> of a linear algebra,
Division.
6.
we can determine uniquely a number x' of the algebra such that
<math>xx' = y</math> provided the <i>n</i> linear equations at the end of (21) are solvable
uniquely for <math>x_1', ..., x_n'</math> in the field <math>F</math>. This will be the case if and
only if the determinant
<math display="block">\Delta(x) = \left| \sum_{i=1}^{n} x_i \gamma_{ijk} \right| \quad (j, k = 1, ..., n) \quad (23)</math>
is not zero. In that case, right-hand division by x is always possible
and unique.
Similarly, there is a unique solution <math>x'</math> in the algebra of the
equation <math>x'x = y</math> if and only if
<math display="block">\Delta'(x) = \begin{vmatrix} \sum_{i=1}^{n} x_i \gamma_{jik} \\ \sum_{i=1}^{n} x_i \gamma_{jik} \end{vmatrix} \quad (j, k = 1, ..., n) \quad (24)</math>
In that case, left-hand division by x is always possible
is not zero.
and unique.
We shall call <math>\Delta(x)</math> the right-hand determinant of x, and <math>\Delta'(x)</math> the
left-hand determinant of x.
Principal unit (modulus). An algebra may contain a
7.
number
<math>\epsilon = \epsilon_1 e_1 + \dots + \epsilon_n e_n</math>.
called a principal unit or modulus, such that
(for every number <math>x</math> of the algebra) (25).
<math>x \epsilon = \epsilon x = x</math>
For example, <math>\epsilon = 1</math> in the binary algebra of all complex numbers
Again, <math>\epsilon = e_{11} + e_{22}</math> in the matric algebra of § 4.
<math>a + bi</math>.
There cannot be a second principal unit . More generally, there
is no new number <math>\epsilon'</math> for which <math>x\epsilon' = x</math> for every <math>x</math>. For, if so, <math>\epsilon\epsilon' = \epsilon</math>,
while by <math>(25_2)</math> for <math>x = \epsilon'</math>, <math>\epsilon \epsilon' = \epsilon'</math>, whence <math>\epsilon' = \epsilon</math>.
Conditions (25) hold if and only if
<math>e_j\epsilon = \epsilon e_j = e_j</math>  <math>(j = 1, ..., n)</math> (25').

## PDF page 20

8
[(26)]
MODULUS
With Kronecker, set <math>\delta_{ij} = 1</math>, <math>\delta_{jk} = 0</math> if <math>j \neq k</math>. By use of (20) and the
linear independence of <math>e_1, \ldots, e_n</math>, we see that (25') are equivalent to
<math display="block">\sum_{i=1}^{n} \epsilon_{i} \gamma_{jik} = \delta_{jk}, \quad \sum_{i=1}^{n} \epsilon_{i} \gamma_{ijk} = \delta_{jk} \qquad (j, \ k=1, \ ..., \ n)</math>
(26).
<math>\Delta'\left(\epsilon\right) = \Delta\left(\epsilon\right) = |\delta_{ik}| = 1</math>
Hence
(27).
Hence if there exists a principal unit, neither <math>\Delta(x)</math> nor <math>\Delta'(x)</math> is
identically zero in <math>x_1, ..., x_n</math>.
For the case of a linear associative algebra it is easily proved that,
conversely*, when neither <math>\Delta(x)</math> nor <math>\Delta'(x)</math> is identically zero, the
algebra has a principal unit. Indeed, there is then a number <math>u</math> for
which neither <math>\Delta(u)</math> nor <math>\Delta'(u)</math> is zero. By § 6, there is a unique
number <math>\epsilon</math> of the algebra such that <math>u\epsilon = u</math>, and a uniquely determined z
for which <math>zu = x</math>, where x is an arbitrary number of the algebra.
Then, by the associative law,
<math>x\epsilon = (zu) \epsilon = z (u\epsilon) = zu = x</math>
<math>u(\epsilon x) = (u\epsilon) x = ux, \quad \epsilon x = x.</math>
Hence <math>\epsilon</math> is a principal unit. In such an algebra any number <math>x</math> for
which <math>\Delta(x) \neq 0</math> has a unique inverse. For, if <math>x^{-1}</math> is the unique
number determined by <math>xx^{-1} = \epsilon</math>, then <math>x^{-1}x = \epsilon</math>, since
<math>x(x^{-1}x - \epsilon) = \epsilon x - x\epsilon = 0.</math>
Hence <math>x'x = \epsilon</math> implies <math>x' = x^{-1}</math>, as shown by multiplying by <math>x^{-1}</math> on the
right, so that <math>\Delta'(x) \neq 0</math> (§ 6).
Thus <math>\Delta(x) \neq 0</math> implies <math>\Delta'(x) \neq 0</math> and conversely.
8.
<b>Transformation of units.</b> Consider <math>n</math> numbers
<math display="block">E_i = \sum_{j=1}^n c_{ij}e_j \qquad (i=1,\ldots,n)</math>
(28)
in which the c's are numbers of a field F such that
<math>|c_{ij}| \neq 0</math> <math>(i, j = 1, ..., n).</math>
We may solve the n equations and obtain
<math>e_i = \sum_{j=1}^{n} t_{ij} E_j, \quad |t_{ij}| \neq 0 \quad (i = 1, ..., n)</math> (29),
where the t's are numbers of F. By means of (28) and (20) we can
* G. Scheffers, Leipzig Berichte, vol. 41 (1889), p. 293. Stated for com-
mutative algebras by Weierstrass, Göttingen Nach., 1884, p. 412.

## PDF page 21

§ 87
TRANSFORMATION OF UNITS
9
express <math>E_i E_j</math> as a linear function of the e's, and hence by (29) as a
linear function of the <math>E</math>'s:
<math>E_i E_j = \sum_{k=1}^n \Gamma_{ijk} E_k \quad (i, j = 1, ..., n)</math>
(30).
For any number x of the algebra,
<math>x \equiv \sum_{i=1}^{n} x_i e_i = \sum_{j=1}^{n} X_j E_j, \quad X_j = \sum_{i=1}^{n} t_{ij} x_i</math>
(31).
Hence x can be expressed in one way and, in view of the linear
independence of <math>E_1, ..., E_n</math> with respect to <math>F</math>, but one way as <math>\sum X_i E_i</math>,
where the <math>X</math>'s are numbers of <math>F</math>. Taking <math>E_1, ..., E_n</math> as new units,
we obtain a linear algebra over F with the constants of multiplication
<math>\Gamma_{ijk}</math>, which is called the transform of the initial algebra by the trans-
formation of units (28) or (29). The two algebras are called equivalent
under linear transformation of units in <math>F</math>.
Any number of a linear algebra is a root of an
9.
Any <math>n+1</math> numbers of a linear algebra with <math>n</math> units
equation.
over a field F are linearly dependent with respect to F. For, if the
first n of the <math>n+1</math> numbers are linearly independent with respect to <math>F</math>,
the <math>(n+1)</math>th number can be expressed as a linear function of them
with coefficients in <math>F</math> (§ 8).
Assuming here that multiplication is associative, we may denote
the product of i factors A by Ai, where A is any number of the
Since <math>A, A^2, ..., A^{n+1}</math> are linearly dependent, <math>A</math> is a root of
algebra.
an equation of degree <math>\leq n+1</math> with coefficients in <math>F</math>.
If also the algebra has a modulus <math>\epsilon</math>, then <math>\epsilon</math>, <math>A</math>, ..., <math>A</math><sup>*</sup> are linearly
dependent and A is a root of an equation of degree <math>\leq n</math> with coefficients
in <math>F</math>.
For example, in the case of the linear associative algebra of four units in
§ 4, <math>\epsilon = e_{11} + e_{22}</math> is a principal unit, and the general number m, given by (16<sub>1</sub>), is
a root of
<math>m^2 - (a+d) m + (ad-bc) \epsilon = 0.</math>
Polynomials in a single number. An algebraic
10.
identity
<math>f(x) g(x) \equiv p(x),</math>
where the functions <math>f(x)</math>, etc., are polynomials in an ordinary complex
variable with ordinary complex coefficients, without terms free of x,
implies that the same relation holds when x is any number of a linear
associative algebra. Indeed, the term involving <math>x^k</math> in <math>f(x)g(x)</math> is

## PDF page 22

10
[(32)]
POLYNOMIALS IN A NUMBER
obtained by multiplying the term in <math>x^i</math> of <math>f(x)</math> by the term in <math>x^{k-i}</math> of
<math>g(x)</math> and summing the products for <math>i = 1, ..., k - 1</math>. But the associative
law gives <math>x^i x^{k-i} = x^k</math>.
The argument holds also for functions with terms free of the
variable x provided the algebra has a principal unit <math>\epsilon</math> and this is
multiplied into those terms of the corresponding relation in the
hyper-complex number <math>x</math>.
Since the associative law implies <math>x^r x^s = x^s x^r</math>, two polynomials in a
hyper-complex number <math>x</math> are commutative.
Algebra of real quaternions; its unique place
11.
among algebras. We shall determine all linear associative
algebras over the field of real numbers such that a product is zero
only when one factor is zero. This determination is of decided
intrinsic interest and yields an important result on real simple
algebras (end of § 56).
If x is a given number <math>\neq 0</math>, <math>xx' = 0</math> implies <math>x' = 0</math>; similarly,
<math>x'x = 0</math> implies <math>x' = 0</math>. Hence (§ 6) neither <math>\Delta(x)</math> nor <math>\Delta'(x)</math> is zero
when <math>x \neq 0</math>. Thus (end of § 7) the algebra contains a principal unit,
which we shall denote by 1. If every number is a real multiple of 1,
the algebra is the field of all real numbers. Excluding this case, we
may take the units to be 1, <math>e_1, ..., e_{n-1}</math>, where <math>n > 1</math>. Then (§ 9) any
number A of the algebra is a root of an equation <math>p(x) = 0</math> of degree
<math>\leq n</math> with real coefficients. By the fundamental theorem of algebra,
<math>p(x)</math> equals a product <math>f_1(x)f_2(x)</math> ... of linear or quadratic factors with
real coefficients. Then (§ 10), <math>f_1(A)f_2(A)...=0</math>. Thus one factor is
zero. Hence any number of the algebra is a root of a quadratic
equation with real coefficients.
If <math>e^2 + 2re + s = 0</math>, then <math>(e+r)^2 = r^2 - s</math>. Hence after adding a real
constant to each <math>e_i</math>, we may assume that the square of each new
unit <math>e_i</math> is a real number. If <math>e_1^2</math> is a real number <math>\geq 0</math>,
<math>0 = e_1^2 - r^2 = (e_1 - r)(e_1 + r), \quad e_1 = \pm r,</math>
whereas <math>e_1</math> and 1 are linearly independent. Thus <math>e_1^2 = -t^2</math>, where t is
a real number <math>\neq 0</math>. Set <math>E_1 = e_1/t</math>. Then <math>E_1^2 = -1</math>. If <math>n = 2</math>, the new
units are 1, <math>E_1 = i</math>, and the algebra is the system of ordinary complex
Next, let <math>n > 2</math>. Then we may take the units to be
numbers.
1, <math>I</math>, <math>J</math>, ..., where *
<math>I^2 = -1, \quad J^2 = -1, \dots</math>
(32).
* Although <math>I^2 = J^2</math>, it does not follow that <math>(I - J)(I + J) = 0</math>, <math>I = \pm J</math>.

## PDF page 23

§ 11]
QUATERNIONS
11
Since <math>I \pm J</math> is a root of a quadratic equation,
<math>(I+J)^2 \equiv -2 + IJ + JI = r(I+J) + r_1</math>
<math>(I-J)^2 \equiv -2 - IJ - JI = s(I-J) + s_1</math>
where <math>r</math>, <math>r_1</math>, <math>s</math>, <math>s_1</math> are real. Adding, we get
<math>(r+s) I + (r-s) J + r_1 + s_1 + 4 = 0.</math>
But 1, I, J are linearly independent with respect to the field of reals.
Thus
Hence <math>r = s = 0</math>.
<math>IJ+JI=2c</math>
(c real)
(33).
The product IJ is linearly independent of 1, I, J with respect to
the field of reals. For, if
<math>IJ = r + sI + tJ</math>.
where <math>r</math>, <math>s</math>, <math>t</math> are real, then
<math>(I-t)\left(J+\frac{r+st}{t^2+1}I+\frac{rt-s}{t^2+1}\right)=0,</math>
whereas neither factor is zerd. Hence we may take
<math>IJ = K</math>
(34)
as the fourth unit. In view of this choice of K, we do not know that
<math>K^2 = -1</math>, as in (32). But, by (32)—(34),
<math>K^2 = I(JI)J = I(2c - IJ)J = 2cK - 1,</math>
<math>(K-c)^2 = c^2 - 1 < 0</math>
(35).
For, if <math>c^2 \equiv 1</math>, <math>K-c</math>, and hence <math>K</math>, would be real.
We make the real transformation of units
<math>i = I, \quad j = \frac{J + cI}{\sqrt{1 - c^2}}, \quad k = \frac{K - c}{\sqrt{1 - c^2}}.</math>
Then <math>ij = k</math>, <math>ji = -k</math>. By (35), <math>k^2 = -1</math>. By (32) and (33), <math>i^2 = -1</math>,
<math>j^2 = -1</math>. Then the associative law gives
<math>ik = i(ij) = -j, \quad ki = (ij) \ i = -ik = j,</math>
<math>kj = (ij) j = -i, \quad jk = j (ij) = -kj = i.</math>
The resulting algebra, over the field of reals, with the four units
<math>1, i, j, k</math> and the multiplication table
<math>i^2 = j^2 = k^2 = -1, \quad ij = k, \qquad ji = -k, \\ jk = i, \quad kj = -i, \quad ki = j, \quad ik = -j </math>
(36),
is called the algebra Q of real quaternions*.
* W. R. Hamilton, Trans. Irish Acad., vol. 21 (1848), p. 199 [1843]; Lectures

## PDF page 24

12
QUATERNIONS
Finally, suppose that our algebra contains a number <math>\lambda</math> not in this
sub-algebra Q.
Since <math>\lambda</math> satisfies a quadratic equation with real
coefficients, we may derive as at the outset a number l, not in Q,
such that <math>l^2 = -1</math>. By the proof leading to (33),
<math>il + li = c_1, \quad jl + lj = c_2, \quad kl + lk = c_3,</math>
where the c's are real constants. Then
.
<math>lk = (li) j = (c_1 - il) j = c_1 j - i (c_2 - jl) = c_1 j - c_2 i + kl,</math>
<math>2kl = c_3 + c_2i - c_1j</math>.
Multiply each term of the latter by <math>k</math> on the left.
Thus
<math>-2l = c_3k + c_2j + c_1i</math>.
But <math>l</math> was not in <math>Q</math>. We therefore have the
Theorem*. The only linear associative algebras over the field of
reals, in which a product is zero only when one factor is zero, are the
field of reals, the field of ordinary complex numbers, and the algebra of
real quaternions.
Simplest algebraic properties of real quaternions.
12.
To show that multiplication is associative, it suffices to verify (3<sub>2</sub>)
when each <math>x</math> is chosen from <math>i, j, k</math>. Instead of treating all 27 cases,
it suffices, in view of the symmetry of (36), to treat the sets iii, iij, iji,
<math>jii, ijk.</math> Now <math>(ij) k = -1 = i(jk)</math>, etc.
The <i>conjugate</i> <math>q'</math> of a quaternion <math>q</math> is defined by
<math>q = x + yi + zj + wk</math>, <math>q' = x - yi - zj - wk</math>.
Their product is called the norm of <math>q</math>:
<math>N(q) = qq' = q'q = x^2 + y^2 + z^2 + w^2</math>.
If <math>q \neq 0</math>, then <math>N(q) \neq 0</math> and the inverse of q is
<math>q^{-1} = \frac{1}{N(q)} q'</math>.
Thus, if <math>q \neq 0</math>, <math>qQ = q_1</math> has the unique solution <math>Q = q^{-1}q_1</math>, and <math>Qq = q_1</math>
on Quaternions, 1853; Elements of Quaternions, 1866, etc. To assist the memory,
note that if <math>i, j, k</math> be read in cyclic order (so that k is followed by i), the product of
any one by the next is the next following one.
* Frobenius, Crelle, vol. 84 (1878), p. 59; C. S. Peirce, Amer. Jour. Math.,
vol. 4 (1881), p. 225; E. Cartan, Ann. Fac. sc. Toulouse, vol. 12 (1898), B, p. 82
(see last foot-note in § 56); F. X. Grissemann, Monatshefte Math. Phys., vol. 11
(1900), pp. 132—147 (the last a slight modification of the proof by Frobenius).
The remarkably simple proof in the text is due to the writer and was outlined
by him in Trans. Amer. Math. Soc., vol. 15 (1914), p. 39.

## PDF page 25

§ 12]
QUATERNIONS
13
has the unique solution <math>Q = q_1 q^{-1}</math>. In particular, a product of two
quaternions is zero only when one factor is zero.
Since each kind of division by q is always possible and unique
if and only if <math>N(q) \neq 0</math>, it is not surprising that a computation
gives
<math display="block">\Delta(q) = \Delta'(q) = \{N(q)\}^2.</math>
The conjugate of <math>q'</math> is <math>q</math>. The conjugate of <math>qq_1</math> is <math>q'_1q'</math>. In
their product we may move the real number <math>q_1q_1'</math> to the front of <math>q</math>.
Hence the norm of a product of any two quaternions equals the pro-
duct of their norms. This proves Euler's theorem that the product
of two sums of four squares can be expressed as a sum of four
squares. For applications, see end of § 52.
The general quaternion <math>q</math> is a root of
<math display="block">a^2 - 2xa + x^2 + y^2 + z^2 + w^2 = 0.</math>
A quaternion integer* is a quaternion
<math>x(1+i+j+k)/2 + yi + zj + wk</math>
in which x, ..., w are ordinary integers. For them there is a greatest
common divisor process, unique factorization into primes (apart from
factors <math>\pm 1</math>, <math>\pm i</math>, ..., which divide unity), etc., as in the arithmetic of
ordinary integers.
Equivalence of the complex quaternion and matric
13.
algebras. We consider quaternions whose coordinates are ordinary
complex numbers <math>a + b \sqrt{-1}</math> and the complex matric algebra with four
units (§ 4). From the units <math>e_{11}</math>, ... of the matric algebra, we derive
the quaternion units as follows:
<math>1 = e_{11} + e_{22}, \quad i = \sqrt{-1} (e_{22} - e_{11}), \quad j = e_{12} - e_{21}, \quad k = -\sqrt{-1} (e_{12} + e_{21}).</math>
These satisfy the quaternion relations (36). Conversely,
<math>e_{11} = \frac{1 + \sqrt{-1}i}{2}, \quad e_{22} = \frac{1 - \sqrt{-1}i}{2},</math>
<math>e_{12} = \frac{j + \sqrt{-1} k}{2}</math>, <math>e_{21} = \frac{-j + \sqrt{-1} k}{2}</math>.
The two complex algebras are therefore t equivalent under linear
* A. Hurwitz, Göttingen Nachrichten, 1896, p. 313.
† In § 45 of Cayley's paper (cited in § 3 above), he noted that relations (36)
between the quaternion units can be satisfied by four matrices of order 2. B. Peirce,
Amer. Jour. Math., vol. 4 (1881), p. 132 (read before the Nat. Acad. Sc., 1870),

## PDF page 26

CAYLEY'S ALGEBRA
[(37)]
14
transformation of units, but the real quaternion and real matric
sub-algebras are not.
Cayley's eight unit generalization of real qua-
14.
<b>ternions.</b> Cayley* gave the real algebra with the units 1, <math>e_1, ..., e_7</math>:
<math>\left. egin{aligned} e_i^{\ 2} = -1, & e_i e_j = -e_j e_i & (i,j=1,\,...,\,7\,;\,\,i 
eq j) \\ e_1 e_2 = e_3, & e_1 e_4 = e_5, & e_1 e_6 = e_7, & e_2 e_5 = e_7 \end{aligned} 
ight.</math>
(37),
<math>e_2e_4 = -e_6</math>, <math>e_3e_4 = e_7</math>, <math>e_3e_5 = e_6</math>
together with 14 equations obtained from the last 7 by permuting
each set of three subscripts cyclically, as <math>e_2e_3=e_1</math>, <math>e_3e_1=e_2</math>.
The norm <math>N(x)</math> of a general number x is defined by
<math>x = x_0 + x_1 e_1 + \dots + x_7 e_7</math>, <math>N(x) = x_0^2 + x_1^2 + \dots + x_7^2</math>.
While the associative law holds for three units chosen from one
of the triples in (37), we have <math>e_a e_b \cdot e_c = -e_a \cdot e_b e_c</math> when the three e's
are not in one of those triples. Since the associative law fails we may
knew that the complex quaternion algebra was equivalent to the linear algebra
e<sub>11</sub>, e<sub>12</sub>, e<sub>21</sub>, e<sub>22</sub> satisfying relations (14); he and C. S. Peirce knew the corresponding
linear algebra (14) with <math>n^2</math> units (pp. 217—18).
Sylvester, Johns Hopkins Univ. Circulars, vol. I (1882), p. 241; vol. III (1884),
p. 7 (=Math. Papers, vol. III, p. 647; vol. IV, p. 122), noted that the matrices
<math>\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}, \begin{pmatrix} 0 & 1 \\ -1 & 0 \end{pmatrix}, \begin{pmatrix} 0 & \theta \\ \theta & 0 \end{pmatrix}, \begin{pmatrix} -\theta & 0 \\ 0 & \theta \end{pmatrix} [\theta = \sqrt{-1}]</math>
"construed as complex numbers are a linear transformation of the ordinary
quaternion system" [they satisfy (36) if taken as 1, i, k, j respectively, thus
verifying Cayley's above remark], and gave the transformation in § 13. If <math>\rho</math> is a
cube root of unity, the matrices
<math>I = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0 \end{pmatrix}, \quad u = \begin{pmatrix} 0 & 0 & 1 \\ \rho & 0 & 0 \\ 0 & 0 & 0 \end{pmatrix}, \quad v = \begin{pmatrix} 0 & 0 & 1 \\ \rho^2 & 0 & 0 \\ 0 & 0 & 0 \end{pmatrix}</math>
satisfy the relations <math>u^3 = v^3 = I</math>, <math>vu = \rho uv</math>. He called the linear algebra with the
nine units <math>u^i v^j</math> <math>(i, j=0, 1, 2)</math> nonions. Sylvester gave another set of matrices <math>u, v</math>
in Compt. Rend. Paris, vol. 97 (1883), p. 1336; vol. 98 (1884), pp. 273, 471 (= Math.
Papers, vol. 1v, pp. 118, 154). In Amer. Jour. Math., vol. 6 (1884), p. 286
(= Math. Papers, vol. IV, p. 224), he called the matric algebra of order p, p2-ions.
Clifford had earlier given the name quadrate algebra.
* Phil. Mag. London, ser. 3, vol. 26 (1845), p. 210 (= Coll. Math. Papers, vol. 1,
p. 127). In his <math>A_4</math>, 87 should read 47. I have changed the sign of his last unit
to obtain one (given by <math>\epsilon_7 = -1</math>) of the two algebras later considered in more detail
by Cayley, Amer. Jour. Math., vol. 4 (1881), pp. 293-6 (= Coll. Math. Papers,
vol. x<sub>1</sub>, pp. 368-371). His algebra with <math>\epsilon_7 = +1</math> may be obtained from that with
<math>\epsilon_7 = -1</math> by changing the signs of <math>e_2, \ldots, e_7</math>. Hence the various Cayley algebras
are equivalent to (37). An equivalent algebra was discovered independently by
J. J. Graves before 1844, Trans. Irish Acad., vol. 21 (1848), p. 338.

## PDF page 27

CAYLEY'S ALGEBRA
§ 14]
15
not prove by the method used for quaternions (end of § 12) that the
norm of a product equals the product of the norms of the factors.
To secure this property, Cayley made a long analysis which led finally
to the choice of signs given in the relations (37). I have given a simple
proof of this property and at the same time proved the remarkable
theorem that right- and left-hand division, except by zero, are always
possible and unique in this algebra, a fact overlooked by Cayley and
first stated in a recent paper of mine*. I shall here give more elegant
proofs based upon a representation of the 8 unit algebra as a quasi-
binary algebra with real quaternion coordinates. Set <math>e = e_4</math>. Then
the general number is <math>q + Qe</math>, where <math>q</math>, <math>Q</math> and <math>r</math>, <math>R</math> below are real
quaternions in the units 1, <math>e_1</math>, <math>e_2</math>, <math>e_3</math>. It can be verified that
relations (37) imply
<math>(q+Qe)(r+Re)=qr-R'Q+(Rq+Qr')e</math>
(38),
where <math>r'</math> is the quaternion conjugate to <math>r</math>.
Taking <math>r = q'</math>, <math>R = -Q</math>, we have
<math>(q + Qe)(q' - Qe) = qq' + QQ' = N(q + Qe).</math>
The norm of the product (38) is <math>tt' + TT'</math>, where
<math>t = qr - R'Q, \quad T = Rq + Qr'</math>
(39),
and hence equals
<math>(qq'+QQ')(rr'+RR')=N(q+Qe).N(r+Re),</math>
increased by <math>a - \beta</math>, where
<math>\alpha = RqrQ' + Qr'q'R', \quad \beta = qrQ'R + R'Qr'q'.</math>
But the conjugate of the first term of a is the second term. Hence
<math>\alpha</math> is a real number. Thus <math>\alpha = R'\alpha R + RR'</math>, and this is at once seen
to equal B. Hence the norm of a product is the product of the
norms.
Left-hand division except by zero is always possible and unique.
For, if <math>r</math>, <math>R</math>, <math>t</math>, <math>T</math> be given, we can solve (39) for <math>q</math>, <math>Q</math>. To this end
* Trans. Amer. Math. Soc., vol. 13 (1912), p. 72. Every number can be ex-
pressed as a linear function of <math>e_2</math>, <math>e_4</math>, <math>e_6</math>, with coefficients linear in <math>e_1</math>. If <math>B=r+\epsilon e_1</math>,
where r and s are real, set <math>\overline{B} = r - se_1</math>. Let also C be linear in <math>e_1</math>. Then
<math>e_j B = B e_j</math>, <math>(B e_j) (C e_j) = (B \overline{C}) e_j^2</math>, <math>(B e_j) (C e_k) = (B C) (e_j e_k)</math>,
for <math>j, k=2, 4, 6</math>; <math>j \neq k</math>. Hence the 8 unit algebra can be exhibited as a quasi-
quaternion algebra with the units 1, <math>e_2</math>, <math>e_4</math>, <math>e_6</math> and coordinates linear in <math>e_1</math>.
† The reader may take (38) as the definition of the algebra.

## PDF page 28

16
CAYLEY'S ALGEBRA
multiply the second equation (39) by <math>r</math> on the right and replace <math>qr</math> by
its value from the first; we get
<math>(rr' + RR') Q = Tr - Rt.</math>
Multiply the first by <math>r'</math> on the right and eliminate <math>Qr'</math>.
Thus
<math display="block">(rr' + RR') q = tr' + R'T.</math>
Similarly, right-hand division except by zero is always possible and
unique. By the relations in the first line of <math>(37)</math>, the general number <math>x</math>
is a root of
<math>x^2 - 2x_0x + N(x) = 0.</math>
The above theorem on the norm of a product and the corresponding
one for norms of quaternions (end of § 12) and for norms of ordinary
complex numbers lead to identities
<math>(x_1^2 + \ldots + x_n^2)(y_1^2 + \ldots + y_n^2) = z_1^2 + \ldots + z_n^2</math>
in the x's and y's, where <math>z_1, ..., z_n</math> are bilinear functions of the x's and
the y's, for the cases <math>n = 2, 4, 8</math>. That there is such an identity only
in these three cases was proved by A. Hurwitz*, using the theory of
Many earlier writers had published unsatisfactory proofs †.
matrices.
All writers have overlooked the initial paper by C. F. Degen t, who
gave the identity for <math>n = 8</math>, and a method which he supposed would
succeed for <math>n = 16</math>.
Characteristic determinants and equations.
15.
Let
<math>e_1, \ldots, e_n</math> be the units of a linear associative algebra over a field <math>F</math>
and having a principal unit <math>\epsilon</math>. Let <math>x = \sum x_i e_i</math> be the general number of
the algebra. By (20),
<math>xe_j = \sum_{k=1}^n y_{jk}e_k, \quad y_{jk} = \sum_{i=1}^n x_i \gamma_{ijk} \qquad (j=1, ..., n).</math>
For <math>j = 1, ..., n</math> in turn, the first equation gives
<math>(y_{11}-x)e_1+y_{12}e_2+\ldots+y_{1n}e_n=0,</math>
<math>y_{n1}e_1 + y_{n2}e_2 + \dots + (y_{nn} - x)e_n = 0.</math>
Let <math>\omega</math> be an arbitrary number of F. When x is replaced by <math>\omega</math>, the
determinant of the coefficients of the e's becomes <math>\delta(\omega)</math> in (40). Let
<math>C_1(\omega), \ldots, C_n(\omega)</math> be the cofactors of the elements of the jth column.
* Göttingen Nachrichten, 1898, p. 309.
† A partial list is in Encyclopédie Sc. Math., vol. 1, 1, pp. 368, 467.
‡ Mém. Acad. Sc. St. Pétersbourg, vol. 8, années 1817—18 (1822), p. 207.
There
is a misprint in the sign of <math>Rt</math>.

## PDF page 29

§ 15]
CHARACTERISTIC DETERMINANT
17
Multiply the linear equations by <math>C_1(x) \epsilon</math>, ..., <math>C_n(x) \epsilon</math> on the left.
Then (§ 10)
<math>\delta(x)e_i=0</math>
<math>(j=1,...,n).</math>
Multiply by <math>\epsilon_j</math> and sum, where <math>\sum \epsilon_j e_j = \epsilon</math>. Thus <math>\delta(x) \epsilon = 0</math>. Starting
with <math>e_j x</math>, we obtain the second part of
Theorem 1. In a linear associative algebra with a principal unit,
the general number x is a root of the right-hand and left-hand charac-
teristic equations <math>\delta(\omega) = 0</math>, <math>\delta'(\omega) = 0</math>, respectively, where
<math display="block">\delta\left(\omega\right) = \left| \begin{array}{c} n \\ \sum \\ i=1 \end{array} \gamma_{ijk} x_i - \delta_{jk} \omega \right|, \quad \delta'\left(\omega\right) = \left| \begin{array}{c} n \\ \sum \\ i=1 \end{array} \gamma_{jik} x_i - \delta_{jk} \omega \right|</math>
<math>(j, k = 1, ..., n)</math> (40).
Here <math>\delta_{jk}</math> is Kronecker's symbol (§ 7). These determinants are
called the right- and left-hand characteristic determinants, respectively.
The same definitions are made for any linear algebra. Thus the
characteristic determinants are derived from the determinants <math>\Delta(x)</math>
and <math>\Delta'(x)</math> of § 6 by subtracting <math>\omega</math> from each element of the main
diagonals.
For any linear algebra with a principal unit <math>\epsilon = \sum \epsilon_i e_i</math>, there is a
deeper relation between these pairs of determinants.
Then
<math display="block">\sum_{i=1}^{n} (x_i - \omega \epsilon_i) \gamma_{ijk} = \sum_{i=1}^{n} x_i \gamma_{ijk} - \omega \delta_{jk},</math>
<math display="block">\sum_{i=1}^{n} (x_i - \omega \epsilon_i) \gamma_{jik} = \sum_{i=1}^{n} x_i \gamma_{jik} - \omega \delta_{jk},</math>
by (26).
Hence
<math>\Delta(x-\omega\epsilon)\equiv\delta(\omega), \quad \Delta'(x-\omega\epsilon)\equiv\delta'(\omega)</math>
(41).
As multiplication may not be associative, we shall write
<math>x^{1} = x</math>, <math>x^{i+1} = x^{i}x</math>, <math>x^{1} = x^{i}x</math>, <math>x^{i+1} = x^{i}x</math>, <math>x^{i+1} = x^{i}x</math>, <math>x^{i+1} = x^{i}x</math>, <math>x^{i+1} = x^{i}x</math>, <math>x^{i+1} = x^{i}x</math>, <math>x^{i+1} = x^{i}x</math>, <math>x^{i+1} = x^{i}x</math>, <math>x^{i+1} = x^{i}x</math>, <math>x^{i+1} =</math>
and, in case there is a modulus <math>\epsilon</math>, <math>x^0 = {}^0x = \epsilon</math>. If <math>\sum t_i x^i = 0</math>, <math>x</math> is called
a right-hand root of <math>\Sigma t_i \omega^i = 0</math>. If <math>\Sigma t_i(^i x) = 0</math>, x is called a left-hand
root of <math>\sum t_i \omega^i = 0</math>. We shall prove
THEOREM 2. In any linear algebra with a principal unit, the
general number is a left-hand root of the right-hand characteristic
equation and a right-hand root of the left-hand characteristic equation.
Without loss of generality (§ 16), we may assume that the principal
unit is <math>e_1 = 1</math>. By (41), <math>\delta(\omega)</math> and <math>\delta'(\omega)</math> are derived from <math>\Delta(x)</math> and
<math>\Delta'(x)</math> by replacing <math>x_1</math> by <math>x_1 - \omega</math>. Set
<math display="block">\delta(\omega) = \Delta(x - \omega) = \sum_{i=0}^{n} r_i \omega^i.</math>
2
D.

## PDF page 30

18
[(42)]
CHARACTERISTIC DETERMINANT
Denote by <math>x_1', ..., x_n'</math> the cofactors of the elements of the first row in
<math display="block">\Delta(x) = \begin{vmatrix} \sum x_i \gamma_{i11} \dots \sum x_i \gamma_{in1} \\ \dots \\ \sum x_i \gamma_{in1} & \sum x_i \gamma_{in1} \end{vmatrix}</math>
(42).
Multiply <math>x_j'</math> by the jth element <math>\sum x_i \gamma_{ijk}</math> of the kth row and sum for
<math>j=1, \ldots, n</math>. We obtain the coefficient <math>y_k</math> of <math>e_k</math> in <math>y=xx'</math>, where
<math>x' = \sum x_j' e_j</math>. But <math>y_1 = \Delta(x)</math>, <math>y_k = 0</math> <math>(k > 1)</math>. Hence <math>xx' = \Delta(x)</math>. When
<math>x_1</math> is replaced by <math>x_1 - \omega</math>, let <math>x'</math> become
<math display="block">f = \sum_{i=0}^{n-1} f_i \omega^i,</math>
where the <math>f_i</math> are numbers of the algebra.
Thus
<math>(x-\omega)f = \Delta(x-\omega) = \sum_{i=0}^{n} r_i \omega^i.</math>
Expanding the first product and equating the coefficients of like powers
of <math>\omega</math>, we get
<math>xf_0 = r_0</math>, <math>xf_1 - f_0 = r_1</math>, ..., <math>xf_{n-1} - f_{n-2} = r_{n-1}</math>, <math>-f_{n-1} = r_n</math>.
Multiply the second equation by x on the left, the third by x twice
on the left, the fourth by x three times, etc. Adding, we get
<math>\sum r_i(^ix)=0.</math>
The proof of the second part of the theorem † is similar.
A final generalization, not hitherto published, is
Theorem 3. In an arbitrary linear algebra, the general number is
a left-hand root of <math>\omega\delta(\omega) = 0</math> and a right-hand root of <math>\omega\delta'(\omega) = 0</math>.
Let <math>e_1, ..., e_n</math> be the units of the given algebra <math>A</math>, which is not
assumed to have a principal unit, nor to be associative.
Consider the
algebra <math>A^*</math> with the units <math>e_0, e_1, ..., e_n</math>, where
<math>(i = 1, ..., n)</math>.
<math>e_0^2 = e_0, \quad e_0 e_i = e_i e_0 = e_i</math>
† This theorem was stated and proved by Dickson, Trans. Amer. Math. Soc.,
vol. 13 (1912), p. 60. For the case in which multiplication is associative, the proof
becomes essentially the simpler one of the two proofs by Frobenius, Sitzungsber.
Akad. Berlin, 1896, p. 601, when that proof is suitably translated from the
terminology of bilinear forms into that of hyper-complex numbers. In this asso-
ciative case, the theorem can be expressed as one on matrices and was first stated
in this form by Cayley and verified for <math>n=2</math> and <math>n=3</math>, Phil. Trans. London,
vol. 148 (1858), p. 24 (= Coll. Math. Papers, vol. II, p. 475). For matrix m in (7),
the theorem is <math>m^2 - (a+d)m + (ad-bc)\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \equiv 0</math>. For references to many other
proofs, see Encyc. Sc. Math., vol. 1, 1, p. 418. The earliest occurrence of the
theorem was, for <math>n=3</math>, in Hamilton's Lectures on Quaternions, 1853, pp. 566—7.

## PDF page 31

<math>\S 15]</math>
CHARACTERISTIC DETERMINANT
19
Thus <math>e_0</math> is a principal unit of <math>A^*</math>. Set
<math>x = \sum_{i=1}^{n} x_i e_i, \quad x^* = x_0 e_0 + x, \quad x' = \sum_{i=1}^{n} x_i' e_i.</math>
Then <math>x</math> and <math>x^*</math> are the general numbers of <math>A</math> and <math>A^*</math>. Since
<math>(x_0'e_0+x') x^* = x_0'x_0e_0 + \sum_{i=1}^n (x_0'x_i+x_i'x_0) e_i + x'x,</math>
the left-hand determinant of <math>x^*</math> is
<math display="block">\Delta'_{n+1}(x^*) = \begin{vmatrix} x_0 & \cdots & 0 \\ x_1 & x_0 + \sum x_j \gamma_{1j1} & \cdots & \sum x_j \gamma_{nj1} \\ \cdots & \cdots & \cdots \\ x_n & \sum x_j \gamma_{1jn} & \cdots & x_0 + \sum x_j \gamma_{njn} \end{vmatrix},</math>
with <math>x_0</math> occurring only in the main diagonal. By (41), the left-hand
characteristic determinant <math>D(\omega)</math> of <math>x^*</math> is therefore
<math>\Delta'_{n+1}(x^* - \omega e_0) = (x_0 - \omega) \sum_{i=1}^{n} l_i (\omega - x_0)^i,</math>
where <math>\Sigma l_i \omega^i</math> is the expansion of the left-hand characteristic determinant
<math>\delta'(\omega)</math> of x. By the second theorem above, <math>x^*</math> is a right-hand root of
<math>D(\omega) = 0</math>. Set <math>x_0 = 0</math>. Hence <math>x</math> is a right-hand root of <math>\sum l_1 \omega^{i+1} = 0</math>.
The first part of the theorem is proved similarly.
16.
Determinants of x unaltered by linear transforma-
tion of units. Introduce new units <math>E_1, ..., E_n</math> as in §8; let <math>x</math>
become <math>X = \sum X_j E_j</math>. We are to prove that <math>\Delta(x)</math>, given by (23),
equals
<math display="block">D(X) = \left| \sum_{i=1}^{n} X_i \Gamma_{ijk} \right| \qquad (j, k = 1, ..., n).</math>
If <math>x</math> and <math>y</math> are given numbers of the initial algebra, <math>xx' = y</math> has a
unique solution x' if and only if <math>\Delta(x) \neq 0</math> (§ 6). Similarly, <math>XX' = Y</math>
has a unique solution X' if and only if <math>D(X) \neq 0</math>. But <math>x = X</math>, etc.
Hence <math>\Delta(x) = 0</math> implies <math>D(X) = 0</math>. If <math>\Delta(x)</math> is identically zero, then
<math>D(X)</math> is, and the theorem <math>\Delta(x) = D(X)</math> is true. Henceforth,
let <math>\Delta(x)</math> be not identically zero, so that there exists a modulus <math>\epsilon \leq 7</math>.
Since every set of values of the <math>x_i</math>, <math>\gamma_{ijk}</math> for which <math>\Delta(x) = 0</math> is a set of
solutions of <math>D(X)=0</math>, it will follow from a well-known theorem on
polynomials that <math>\Delta(x)</math> is a factor of <math>D(X)</math> as soon as <math>\Delta(x)</math> is proved
to be an irreducible function of its arguments <math>x_i</math>, <math>\gamma_{ijk}</math>. Since each
element of the determinant <math>D(X)</math> equals a function linear and
homogeneous in <math>x_1, ..., x_n</math>, and linear and homogeneous in the <math>\gamma</math>'s,
2-3

## PDF page 32

20
CHARACTERISTIC DETERMINANT
the quotient of <math>D(X)</math> by <math>\Delta(x)</math> depends only upon the coefficients <math>t_{ij}</math>
of the transformation of units. The quotient is unity, since the latter
is its value for <math>x = \epsilon</math> by (27).
It remains only to prove that <math>\Delta(x)</math> is irreducible. If the function
<math>\Delta(x)</math>, homogeneous in the <math>\gamma</math>'s and homogeneous in <math>x_1, \ldots, x_n</math>, is the
product of two factors, each factor is homogeneous in the <math>\gamma</math>'s and in
the x's. But the coefficient of <math>x_1^n</math> is <math>|\gamma_{1jk}|</math>, a determinant whose <math>n^2</math>
elements are arbitrary and hence an irreducible function of these
<math>n^2</math> elements <math>\gamma_{1jk}</math>. Hence one factor of <math>\Delta</math> is free of the <math>\gamma</math>'s. Taking
<math>\gamma_{ijk} = 0 \ (i \neq j)</math>, we have
<math display="block">\Delta(x) = |x_j \gamma_{ijk}| = x_1 \dots x_n |\gamma_{ijk}| \qquad (j, k = 1, \dots, n).</math>
Hence for general values of the <math>\gamma</math>'s, the factor free of the <math>\gamma</math>'s is <math>x_1 \dots x_n</math>.
But the coefficient of <math>x_1^n</math> in <math>\Delta</math> was seen to be not identically zero.
A like argument holds for <math>\Delta'(x)</math>. Hence <math>\Delta(x)</math> and <math>\Delta'(x)</math> are unaltered
under linear transformation of the units. Since the modulus <math>\epsilon</math> is
unaltered, we have*, by (41), the
The determinants and characteristic determinants of
THEOREM.
the general number of any linear algebra remain unaltered under any
linear transformation of the units.
17.
Invariants and covariants of linear algebras.
Consider the linear algebra with n units whose constants of multi-
plication <math>\dagger \gamma_{ijk}</math> are undetermined numbers of a field F. Let C be a
polynomial in these <math>\gamma</math>'s and the coordinates <math>x_i</math> of the general number <math>x</math>
of the algebra over <math>F</math>. If, under every linear transformation of units (§ 8),
<math>C(X_i; \Gamma_{ijk}) = f \cdot C(x_i; \gamma_{ijk}),</math>
where f is a function only of the coefficients <math>t_{ij}</math> of the transformation,
C is called a covariant of the algebra. In particular, C is an absolute
covariant if <math>f = 1</math>, and an invariant if C involves only the <math>\gamma</math>'s.
The characteristic determinants <math>\delta(\omega)</math> and <math>\delta'(\omega)</math> are absolute co-
variants of the general linear algebra with <math>n</math> units (§ 16).
For example, consider the algebra with the units <math>\epsilon</math>, <math>e</math>, where <math>\epsilon</math> is a principal
unit, and <math>e^2 = \gamma e + c\epsilon</math>. For <math>x = x_1 \epsilon + x_2 e</math>,
<math display="block">\Delta(x) = \Delta'(x) = \begin{vmatrix} x_1 & cx_2 \\ x_2 & x_1 + \gamma x_2 \end{vmatrix},</math>
<math>\delta(\omega) = \delta'(\omega) = \omega^2 - l\omega + \Delta(x), \quad l \equiv 2x_1 + \gamma x_2.</math>
* The invariance of <math>\delta(\omega)</math> when <math>\Delta(x) \equiv 0</math> follows by continuity.
<math>\dagger</math> If there be a modulus, we take it as the unit <math>e_1</math>. Then
<math>\gamma_{1jj} = \gamma_{j1j} = 1, \quad \gamma_{1jk} = \gamma_{j1k} = 0 \quad (j \neq k).</math>
The remaining <math>\gamma</math>'s are to be left arbitrary. See the example.

## PDF page 33

§ 17]
COVARIANTS OF ALGEBRAS.
BINARY ALGEBRAS
21
Then <math>l</math> and <math>\Delta(x)</math> are absolute covariants. To give a direct proof, introduce
the new units <math>\epsilon</math>, <math>E=re+s\epsilon</math>, where <math>r\neq 0</math>. Then
<math>x = X_1 \epsilon + X_2 E</math>, <math>X_1 = x_1 - \frac{8x_2}{r}</math>, <math>X_2 = \frac{x_2}{r}</math>
<math>E^2 = \Gamma E + C\epsilon</math>, <math>\Gamma = 2s + r\gamma</math>, <math>C = r^2c - rs\gamma - s^2</math>,
<math display="block">\begin{vmatrix} \dot{X}_{1} & C\dot{X}_{2} \\ \dot{X}_{2} & \dot{X}_{1} + \Gamma\dot{X}_{2} \end{vmatrix} = \Delta(x), \ 2X_{1} + \Gamma\dot{X}_{2} = l.</math>
The discriminant of <math>\Delta(x)</math> gives an invariant of the algebra:
<math>\Gamma^2 + 4C = r^2 (\gamma^2 + 4c)</math>.
18.
Binary linear algebras with a principal unit. In
the last example, take <math>r=1, s=-\gamma/2</math>. Then <math>\Gamma=0</math>. Let therefore
<math>\gamma = 0</math> in the initial algebra. In order that the transformed algebra
shall have <math>\Gamma = 0</math>, the transformation must be <math>E = re</math> (i.e. have <math>s = 0</math>).
Then <math>C = r^2c</math>. Hence the binary algebra
<math>\epsilon^2 = \epsilon</math>, <math>\epsilon e = e \epsilon = e</math>, <math>e^2 = c \epsilon</math>
(43),
and the similar one with the parameter C, are equivalent if and only
if c and C are both zero, or both are not zero and their ratio is the
square of a number of the field <math>F</math>.
If F is the field of all complex numbers, the two types of non-
equivalent binary algebras are (43) with <math>c = 0</math>, <math>c = 1</math>.
If F is the field of reals, the three types are (43) with <math>c = 0</math>, <math>c = 1</math>,
<math>c=-1</math>, the last being the field <math>F(i)</math> of complex numbers.
Cayley* gave the seven types of non-equivalent binary associative
algebras over the field of complex numbers, the presence of a principal
unit not being assumed. Miss O. C. Hazlett recently obtained these
seven types from the triple algebras having a modulus (§ 20) and
characterized them by covariants.
Rank and rank equation of a linear algebra. Let
19.
<math>e_1, \ldots, e_n</math> be the units of an algebra over a field <math>F</math> and let the
coordinates <math>x_1, ..., x_n</math> of <math>x = \sum x_i e_i</math> be undetermined numbers of <math>F</math>.
First, let the algebra be associative. By § 15, x is a root of
<math>\delta(\omega) = 0</math> or <math>\omega \delta(\omega) = 0</math>, according as the algebra has or has not a
principal unit. Thus <math>x^n</math> or <math>x^{n+1}</math> is a linear combination of lower
powers of <math>x</math> (also by § 9). The rank <math>r</math> of the algebra is the least
positive integer such that <math>x^r</math> is a linear combination of lower powers
* Proc. London Math. Soc., vol. 15 (1883-4), p. 185 (= Coll. Math. Papers,
vol. xII, pp. 60, 105).
+ Annals of Mathematics, vol. 16 (1914), p. 1.

## PDF page 34

22
RANK OF AN ALGEBRA
of x whose coefficients are rational functions of <math>x_1, ..., x_n</math> with
coefficients in F. The equation <math>R(x) = 0</math> itself is called the rank
equation of the algebra*. If there were two such equations, the
difference would give an equation of lower degree.
Now <math>R(\omega)</math> is a divisor of <math>\delta(\omega)</math> or <math>\omega\delta(\omega)</math>. For, if not, the division
by <math>R(\omega)</math> would lead to a remainder <math>\rho(\omega)</math>, of degree <math>< r</math>, which
vanishes for <math>\omega = x</math>, contrary to the definition of <math>r</math> (cf. § 10).
Similarly, <math>R(\omega)</math> divides <math>\delta'(\omega)</math> or <math>\omega\delta'(\omega)</math>.
It follows that the coefficients of <math>R(\omega)</math> are integral rational
functions of <math>x_1, ..., x_n</math>. For, if not, some set of finite values of the
x's would give an infinite root of a characteristic equation.
Let <math>\omega_1, \ldots, \omega_r</math> be the ordinary complex roots of <math>R(\omega) = 0</math>. Then, if
the algebra has a modulus <math>\epsilon</math>,
<math>R(x) \equiv (x - \omega_1 \epsilon) \dots (x - \omega_r \epsilon) = 0.</math>
The factors are commutative (§ 10). Thus <math>f = x - \omega_i \epsilon</math> is a number <math>\neq 0</math>
such that <math>fg = 0</math> for some <math>g \neq 0</math>. Such a number f is called a nil factor <math>\dagger</math>.
Then <math>\Delta(f) = 0</math>, and since <math>gf = 0</math>, <math>\Delta'(f) = 0</math> (§ 6). Hence, by (41),
<math>\omega_1, \ldots, \omega_r</math> are roots of the two characteristic equations. Conversely,
any root <math>\omega</math> of one of the latter, say <math>\delta(\omega) = 0</math>, is one of the set <math>\omega_1, \ldots, \omega_r</math>.
For, if <math>w = x - \omega \epsilon</math>, then <math>\Delta(w) = 0</math> by (41) and we can find a number
<math>y \neq 0</math> such that <math>wy = 0</math>. Now
<math>v_i \equiv x - \omega_i \epsilon = w + \mu_i \epsilon, \quad \mu_i \equiv \omega - \omega_i,</math>
<math display="block">0 = v_1 v_2 \dots v_r = (\quad) w + \mu_1 \mu_2 \dots \mu_r \epsilon.</math>
Multiply this by y on the right. Thus <math>0 = \mu_1 \dots \mu_r y</math>. Hence one of
the <math>\mu</math>'s is zero. We thus have (Scheffers, <math>l.c.</math>)
Theorem 1. For a linear associative algebra having a principal
unit, the distinct roots of the rank equation <math>R(\omega) = 0</math> are identical with
the distinct roots of either characteristic equation.
For example, the results in § 12 show that each characteristic
determinant of the quaternion <math>x + yi + zj + wk</math> is
<math>\{(x-\omega)^2+y^2+z^2+w^2\}^2=\{R(\omega)\}^2.</math>
* Th. Molien, Math. Annalen, vol. 41 (1893), p. 113. G. Scheffers, ibid., vol. 39
(1891), p. 293, called it the characteristic equation of the system, and r the "Grad."
It is often called the identical equation of the algebra.
+ B. Peirce, Amer. Jour. Math., vol. 4 (1881), p. 104; Weierstrass, Gött. Nach.,
1884, p. 395.

## PDF page 35

§ 19]
RANK OF AN ALGEBRA
23
Under a transformation of units, let the rank equation
<math>R\left(\omega\;;\;x_{i},\;\gamma_{ijk}\right)=0</math>
satisfied by <math>\omega = x</math>, be transformed into <math>\rho(\omega; X_i, \Gamma_{ijk}) = 0</math>, so that <math>\rho = 0</math>
for <math>\omega = X</math>. But <math>R(\omega; X_i, \Gamma_{ijk}) = 0</math> for <math>\omega = X</math>. Unless the last equation
is identical with <math>\rho = 0</math>, we obtain by subtraction an equation of degree
<math>< r</math> satisfied by <math>\omega = X</math>. This equation is the transform of an equation
of degree <math>< r</math> satisfied by <math>\omega = x</math>, contrary to the definition of r. Hence
(Miss Hazlett, l.c.):
Theorem 2. The rank equation of a linear associative algebra is
unaltered by every linear transformation of units.
In the sense of <math>\S</math> 17, the rank <math>r</math> is an invariant of the general
associative algebra with n units, whereas the rank function <math>R(\omega)</math> is
not a covariant.
For non-associative linear algebras, there is an equation <math>\rho(\omega) = 0</math>
of lowest degree having x as a right-hand root (§ 15), called the
right-hand rank equation. Then* <math>\rho(\omega)</math> divides <math>\delta'(\omega)</math> or <math>\omega\delta'(\omega)</math>,
according as there is or is not a modulus. A similar definition and
property hold for the left-hand rank equation. These equations are
unaltered by every linear transformation of units.
For example, in the commutative, but not associative, linear algebra with
the units <math>\epsilon</math>, <math>e_1</math>, ..., <math>e_5</math>, of which <math>\epsilon</math> is a principal unit, and
<math>e_1^2 = e_2</math>, <math>e_1 e_2 = e_3</math>, <math>e_1 e_3 = -e_2</math>, <math>e_1 e_4 = e_5</math>, <math>e_1 e_5 = e_3^2 = -e_4</math>,
<math>e_2^2 = e_4</math>, <math>e_2e_3 = -e_5</math>, <math>e_2e_4 = e_2e_5 = e_3e_4 = e_3e_5 = e_4^2 = e_4e_5 = e_5^2 = 0</math>,
<math>w = x_1 e_1 + ... + x_5 e_5</math> is a root of
<math>w \cdot w^3 + x_1^2 w^2 = 0</math>
but not of a cubic or quadratic equation. The general number <math>x = x_{n\ell} + w</math> is
therefore a root of
<math>x \cdot x^3 - 4x_0x^3 + (x_1^2 + 6x_0^2)x^2 - 2(x_0x_1^2 + 2x_0^3)x + (x_0^2x_1^2 + x_0^4)\epsilon = 0.</math>
20. Complex ternary linear associative algebras with
a modulus †. Consider a linear associative algebra, over the field of
all complex numbers, with three units and the modulus c. Its rank r
is 3 or 2.
First, let <math>r = 3</math>. There exists a number a such that
(I)
<math>R(a) \equiv (a - \lambda_1 \epsilon)(a - \lambda_2 \epsilon)(a - \lambda_3 \epsilon) = 0</math>
and such that a is not a root of a quadratic equation.
* Trans. Amer. Math. Soc., vol. 13 (1912), p. 62, Cor. II.
+ E. Study, Göttingen Nach., 1889, pp. 243-7. Many computations there
made or left to the reader are avoided in the exposition in this tract. Study gave
no argument leading to (A), (B) in case II.

## PDF page 36

24
<math>\lceil (44) \rceil</math>
TERNARY ALGEBRAS
(I<sub>1</sub>) If the roots <math>\lambda_1</math>, <math>\lambda_2</math>, <math>\lambda_3</math> are distinct, set
<math display="block">e_1 = \frac{\left(\alpha - \lambda_2 \epsilon\right) \left(\alpha - \lambda_3 \epsilon\right)}{\left(\lambda_1 - \lambda_2\right) \left(\lambda_1 - \lambda_2\right)}, \quad e_2 = \frac{\left(\alpha - \lambda_1 \epsilon\right) \left(\alpha - \lambda_3 \epsilon\right)}{\left(\lambda_2 - \lambda_1\right) \left(\lambda_2 - \lambda_2\right)}, \quad e_3 = \frac{\left(\alpha - \lambda_1 \epsilon\right) \left(\alpha - \lambda_2 \epsilon\right)}{\left(\lambda_2 - \lambda_1\right) \left(\lambda_2 - \lambda_2\right)}.</math>
For a an arbitrary number, the sum of these e's will be proved to
equal <math>\epsilon</math>. If we replace a by <math>\lambda_i \epsilon</math> <math>(i = 1, 2, 3)</math>, we see that
(44)
<math>e_1 + e_2 + e_3 = \epsilon</math>
But an algebraic quadratic equation is an identity if it is
is satisfied.
satisfied by three values. Thus (44) holds. By the associative law,
powers of a and hence the <math>a - \lambda_i \epsilon</math> are commutative. Thus, if <math>i \neq j</math>,
<math>e_i e_j</math> has the factor R and is zero. Multiplying (44) on the right by <math>e_i</math>,
we get <math>e_i^2 = e_i</math>. Hence
<math>e_i e_i = 0</math>, <math>e_i^2 = e_i</math> <math>(i = 1, 2, 3; i \neq j)</math>
(45).
Finally, the e's are linearly independent. For, by multiplying <math>\sum a_i e_i = 0</math>
by <math>e_j</math> on the right, we get <math>a_j e_j = 0</math>, <math>a_j = 0</math>, since <math>e_j \neq 0</math>. The resulting
algebra (45) is evidently associative, and has
<math>R = \delta = \delta' = (x_1 - \omega)(x_2 - \omega)(x_3 - \omega).</math>
(I<sub>2</sub>) If <math>\lambda_1 = \lambda_2 + \lambda_3</math>, set <math>l = \lambda_1 - \lambda_3</math> and
<math>e_1 = -(\alpha - \lambda_3 \epsilon) (\alpha - 2\lambda_1 \epsilon + \lambda_3 \epsilon)/l^2</math>
<math>e_2 = c (\alpha - \lambda_1 \epsilon) (\alpha - \lambda_3 \epsilon), \quad e_3 = (\alpha - \lambda_1 \epsilon)^2 / l^2,</math>
where <math>c</math> is any constant <math>\neq 0</math>. Each product in the first line of
<math display="block">e_1e_3 = e_3e_1 = e_2e_3 = e_3e_2 = e_2^2 = 0</math>
<math display="block">e_1^2 = e_1, \quad e_1e_2 = e_2e_1 = e_2, \quad e_3^2 = e_3</math>
(46)
has the factor <math>R</math> and is zero. By addition, <math>e_1 + e_3 = \epsilon</math>. Multiplying
this on the left by <math>e_1</math>, <math>e_2</math>, <math>e_3</math> in turn and on the right by <math>e_2</math>, we get the
relations in the second line of (46). The units are linearly independent
since the products of <math>\sum a_i e_i = 0</math> on the left by <math>e_2</math> and <math>e_3</math> in turn give
<math>a_1 = a_3 = 0</math>. The relations (46) for this associative algebra are un-
altered if <math>e_2</math> is replaced by <math>te_2</math>. Here
<math display="block">R = \delta = \delta' = (x_1 - \omega)^2 (x_3 - \omega).</math>
If <math>\lambda_1 = \lambda_2 = \lambda_3</math>, set <math>e_1 = \epsilon</math>, <math>e_2 = \alpha - \lambda_1 \epsilon</math>, <math>e_3 = (\alpha - \lambda_1 \epsilon)^2</math>.
Then
<math>(I_3)</math>
<math>e_1e_1 = e_1e_1 = e_1</math>, <math>e_2e_3 = e_3e_2 = e_3^2 = 0</math>, <math>e_2^2 = e_3</math>
(47),
<math display="block">R = \delta = \delta' = (x_1 - \omega)^3.</math>
Next, let <math>r=2</math>. Take <math>e_1=\epsilon</math>, <math>e_2</math>, <math>e_3</math> as the units. Since <math>r=2</math>,
(11)
<math>\xi = ye_2 + ze_3</math> is a root of a quadratic <math>\xi^2 + 2L\xi + Q_1\epsilon = 0</math>, where L is a

## PDF page 37

§ 20]
TERNARY ALGEBRAS
25
linear and <math>Q_1</math> a quadratic function of y and z with fixed coefficients
depending upon the <math>\gamma_{ijk}</math>. Thus <math>(\xi - L\epsilon)^2 = Q\epsilon</math>, where <math>Q</math> is a quadratic
function of <math>y, z</math>. If <math>Q</math> is not identically zero it can be transformed
linearly into <math>yz</math> or <math>z^2</math>, neither of which is zero for <math>(y, z) = (1, 1)</math> or <math>(1, 2)</math>.
Hence we can find two linearly independent sets <math>(y, z)</math> for which <math>Q = 0</math>,
and therefore three linearly independent units <math>\epsilon</math>, <math>\xi_2 - L_2 \epsilon</math>, <math>\xi_3 - L_3 \epsilon</math>, such
that the squares of the last two are <math>Q_2\epsilon</math>, <math>Q_3\epsilon</math>, respectively, where
<math>Q_2Q_3 \neq 0</math>. Take <math>E_i = (\xi_i - L_i \epsilon)/Q_i^{\frac{1}{2}}</math>. Then
<math>E_2^2 = \epsilon</math>, <math>E_3^2 = \epsilon</math>
(A).
But if Q, and hence the square of <math>ye_2 + ze_3 - L\epsilon</math>, is identically zero,
where <math>L</math> is a certain linear function of <math>y</math>, <math>z</math>, we have only to subtract
constant multiples of <math>\epsilon</math> from <math>e_2</math>, <math>e_3</math> to obtain new units for which
.
<math>e_2^2 = 0</math>, <math>e_3^2 = 0</math>
(B).
Consider case (A). Set
<math>(\Pi_1)</math>
<math>E_2E_3 = \alpha\epsilon + \beta E_2 + \gamma E_3</math>.
<math>E_2(E_2E_3) = (\beta + \alpha\gamma)\epsilon + (\alpha + \beta\gamma)E_2 + \gamma^2E_3 = E_2^2E_3 = E_3</math>
Then
<math>(E_2 E_3) E_3 = (\gamma + \alpha \beta) \epsilon + \beta^2 E_2 + (\alpha + \beta \gamma) E_3 = E_2 E_3^2 = E_2,</math>
<math>\beta^2 = \gamma^2 = 1</math>, <math>\alpha + \beta \gamma = \beta + \alpha \gamma = \gamma + \alpha \beta = 0</math>.
When the sign of <math>E_2</math> is changed, that of <math>\gamma</math> is changed. Hence we may
set <math>\gamma = \pm 1</math>. Changing if necessary the sign of <math>E_3</math>, we may also set
<math>\beta = +1</math>. Hence
<math>E_2E_2=-\epsilon+E_2+E_3</math>.
Set <math>e_2 = E_2</math>, <math>e_3 = E_2 + E_3</math>. Then
<math>e_2^2 = \epsilon</math>, <math>e_2 e_3 = e_3</math>, <math>e_3^2 - e_3 e_2 = e_3</math>,
<math>e_3e_2=r\epsilon+se_2+te_3</math>.
Equating the two values of <math>e_2e_3e_2</math> and the two values of <math>e_3e_2e_2</math>, we get
<math>r = s</math>, <math>t^2 = 1</math>, <math>s(1 + t) = 0</math>, respectively. For <math>t = 1</math>, <math>e_3 e_2 = e_3</math>, <math>e_3^2 = 2e_3</math>, and
<math>\epsilon, f \equiv e_2 + e_3, f^2 = \epsilon + 4e_3</math> are linearly independent, whereas the rank is 2.
Hence <math>t=-1</math>,
<math>e_3 e_2 = s \epsilon + s e_2 - e_3, \quad e_3^2 = s \epsilon + s e_2,</math>
<math>(e_3e_2)e_3 = 2se_3 - e_3^2 = e_3(e_2e_3) = e_3^2, \quad e_3^2 = se_3,</math>
so that <math>s = 0</math>. We have therefore the algebra
<math>e_1e_i = e_ie_1 = e_i</math>, <math>e_2^2 = e_1</math>, <math>e_2e_3 = e_3</math>, <math>e_3e_2 = -e_3</math>, <math>e_3^2 = 0</math> (48),
<math>\delta = lR</math>, <math>\delta' = l'R</math>, <math>R = ll'</math>, <math>l \equiv x_1 + x_2 - \omega</math>, <math>l' = x_1 - x_2 - \omega</math>.
Here, and in (49), <math>R</math> may be derived from <math>\delta</math> and <math>\delta'</math> as in § 19.

## PDF page 38

26
[(49)]
TERNARY ALGEBRAS
(II<sub>2</sub>) Finally, consider case (B). Let <math>e</math>, <math>f</math> denote <math>e_2</math>, <math>e_3</math> or <math>e_3</math>, <math>e_2</math>.
Set <math>ef = a\epsilon + be + cf</math>. Then
<math>0 = e^2 f = e(ef) = ac\epsilon + (a + bc)e + c^2 f, \quad c = a = 0,</math>
<math>0 = ef^2 = (ef)f = (be)f = b^2e, b = 0,</math>
<math>e_1e_1 = e_1e_1 = e_1</math>, <math>e_2^2 = e_2e_3 = e_3e_2 = e_3^2 = 0</math>
(49),
<math>\delta = \delta' = (x_1 - \omega)^3</math>, <math>R = (x_1 - \omega)^2</math>.
No two of the five resulting linear associative algebras (45)—(49)
with a principal unit are equivalent. They are characterized by the
invariant r and the covariant <math>\delta(\omega)</math>.
The corresponding problem for 4, 5, 6 units has been treated*.
21.
Reducible linear associative algebras with a
A linear associative algebra <math>A</math> with <math>n</math> units over a
modulus.
field <math>F</math> and with a modulus <math>\epsilon</math> is called reducible <math>\dagger</math> with respect
to F if it contains <math>p + q = n</math> numbers <math>e_1, ..., e_p</math>; <math>E_1, ..., E_q</math>, linearly
independent with respect to <math>F</math>, such that
<math>e_i E_i = 0, \quad E_i e_i = 0 \qquad (i = 1, ..., p; j = 1, ..., q)</math> (50).
Any number of <math>A</math> is a linear combination of the <math>e</math>'s and <math>E</math>'s. Let
the modulus be <math>\epsilon = e + E</math>, where e is a linear function of <math>e_1, ..., e_p</math>, and
<math>E</math> of <math>E_1, ..., E_q</math>. If x is any linear function of <math>e_1, ..., e_p</math> with coefficients
in F, then <math>x = x\epsilon = xe</math>, since <math>xE = 0</math>, and <math>x = \epsilon x = ex</math>. Similarly, if X
is any linear function of <math>E_1, ..., E_q</math>, then <math>EX = XE = X</math>. Next,
<math>x_1x_2 = x + X</math>, where <math>x_1</math> and <math>x_2</math> are any linear functions of <math>e_1, ..., e_p</math>.
Multiply by <math>E</math> on the right. We get <math>0 = X</math>. Hence <math>\ddagger</math> the product
of any two x's is an x. Similarly, the product of any two X's is an X.
Hence the numbers x form a sub-algebra <math>s = (e_1, ..., e_p)</math> with a modulus <math>e_n</math>
and the numbers X form a sub-algebra <math>S = (E_1, ..., E_q)</math> with a
modulus E. The algebra A is said to be decomposable into s and S,
and is called their direct <math>\S</math> sum, <math>A = s + S = S + s</math>.
* Encyc. Sc. Math., vol. 1, 1, pp. 401-3. For the irreducible algebras with
six units, see G. Voghera, Denkschr. Ak. Wiss., Wien, vol. 84 (1908).
+ G. Scheffers, Math. Annalen, vol. 39 (1891), p. 317; vol. 41 (1893), p. 601.
In Amer. Jour. Math., vol. 4 (1881), p. 100, B. Peirce defined a mixed (impure)
algebra A to be one each of whose numbers is the sum of a number of a sub-
algebra s and a number of a sub-algebra S such that the products <math>eE</math> and <math>Ee</math> of
any numbers e of s and E of S are numbers common to s and S. In case zero is
the only common number, the mixed algebra is reducible in the sense of the text.
‡ Proved less simply by S. Epsteen, Trans. Amer. Math. Soc., vol. 5 (1904),
p. 105.
§ A mixed algebra is not always the direct sum of s and S.

## PDF page 39

§ 21]
REDUCIBILITY.
DIRECT SUM
27
Conversely, from any two linear (associative) algebras <math>(e_1, ..., e_p)</math>
and <math>(E_1, ..., E_q)</math> over <math>F</math> with moduli <math>e</math> and <math>E</math>, we obtain a linear
(associative) algebra <math>(e_1, ..., E_q)</math> over <math>F</math> with the modulus <math>e + E</math> by
postulating relations (50) and regarding e1, ..., E to be linearly in-
dependent with respect to <math>F</math>.
Scheffers gave the following criterion for reducibility:
A linear associative algebra <math>A</math> with a modulus <math>\epsilon</math> is reducible if and
only if it contains a number <math>e \neq \epsilon</math> such that <math>e^2 = e</math>, <math>ex = xe</math>, for every
number x of A.
That these conditions are necessary was proved above. That they
are sufficient is proved by setting <math>E = \epsilon - e</math> and showing that <math>A = s + S</math>,
where s is composed of all products <math>xe</math>, and S of all products <math>xE</math>, <math>x</math>
ranging over all numbers of A. We have
<math>eE = e(\epsilon - e) = e - e = 0</math>, <math>Ee = (\epsilon - e)e = 0</math>,
<math>xe \cdot yE = xy \cdot eE = 0</math>, <math>yE \cdot xe = y(Ee)x = 0</math>,
since <math>ey = ye</math> for any y in A. Also <math>A = s + S</math> since
<math>x = x\epsilon = x(e + E) = xe + xE</math>.
Finally, if the xe are expressible linearly in terms of linearly in-
dependent numbers <math>e_1, ..., e_p</math> of the form <math>xe</math>, and the <math>xE</math> in terms of
<math>E_1, ..., E_q</math>, then <math>e_1, ..., E_q</math> are linearly independent. For, if <math>xe + yE = 0</math>,
the product by <math>e</math> on the right gives <math>xe = 0</math>.
A component s of a reducible algebra A may be reducible or
Hence a reducible algebra may be decomposed into
irreducible.
irreducible algebras. For example, algebra (45) is the sum of three
irreducible algebras <math>(e_1)</math>, <math>(e_2)</math>, <math>(e_3)</math>, and, by <math>(44)</math>, its modulus is the sum
of the moduli <math>e_1</math>, <math>e_2</math>, <math>e_3</math> of the sub-algebras.
Concerning the uniqueness of decomposition, see end of § 61.
Direct product of two algebras. Let <math>s = (e_1, \ldots, e_p)</math>,
22.
<math>S = (E_1, \ldots, E_q)</math> be two linear algebras over a field <math>F</math>, so that
<math>e_i e_j = \sum_{k=1}^p \gamma_{ijk} e_k, \quad E_i E_j = \sum_{k=1}^q \Gamma_{ijk} E_k.</math>
Proceeding* in a formal manner, regard <math>\epsilon_{ik} = e_i E_k = E_k e_i</math>, for <math>i = 1, ..., p</math>;
<math>k=1, \ldots, q</math>, as pq linearly independent units of an algebra P with
* W. K. Clifford, Amer. Journ. Math., vol. 1 (1878), p. 350 (= Coll. Math. Papers,
1882, p. 266). If <math>\omega^2 = 1</math> and <math>\omega</math> is commutative with every real quaternion q and <math>Q</math>,
he called <math>q + \omega Q</math> a biquaternion (not Hamilton's biquaternion, a quaternion with
ordinary complex coefficients).

## PDF page 40

28
[(51)]
DIRECT PRODUCT OF TWO ALGEBRAS
coordinates ranging over <math>F</math>, and set
<math>\epsilon_{ik}\,\epsilon_{jl} = e_ie_j</math>. <math>E_kE_l \equiv \sum_{q=1}^p \sum_{h=1}^q \gamma_{ijq}\Gamma_{klh}\,\epsilon_{gh}</math>.
Call P the direct* product of s and S, and write <math>P = sS = Ss</math>.
We may also obtain P by interpreting the coordinates <math>x_1, \ldots, x_p</math> in
<math>x = x_1 e_1 + \dots + x_p e_p</math> to be general numbers
(X's in F)
<math>x_i = X_{i1}E_1 + \ldots + X_{in}E_n</math>
of S. Thus <math>x = \sum X_{ik}e_i E_k</math> <math>(i = 1, ..., p; k = 1, ..., q)</math>. Or we may
regard <math>P</math> to be an algebra of <math>q</math> units over the algebra <math>s</math>.
For example, from the real quaternion algebra <math>(1, i, j, k)</math> and the
real algebra <math>(1, \sqrt{-1})</math>, we obtain the complex quaternion algebra.
If s and S are associative algebras, <math>P = sS</math> is associative. If s and
S have moduli <math>e</math> and <math>E</math>, <math>P</math> has the modulus <math>eE</math>.
For this definition of multiplication of algebras and that of addition
in § 21, the commutative, associative and distributive laws hold.
Theorem 1†. If A is a linear associative algebra having the
quaternion algebra Q as a sub-algebra and having the same modulus 1
as Q, then <math>A = QC</math>, where C is a sub-algebra, with the modulus 1, of
A such that every number of C is commutative with every number of Q.
It is just as easy to prove Wedderburn's generalization:
Theorem 2. If A is a linear associative algebra with the modulus <math>\epsilon</math>
and the sub-algebra <math>Q</math> with <math>n^2</math> units <math>e^a f^b</math> <math>(a, b = 1, ..., n)</math>:
<math>e^n = f^n = \epsilon</math>, <math>fe = \rho ef</math>
(51),
where <math>\rho</math> is a primitive nth root of unity, then <math>A = QC</math>, where <math>C</math> is a
sub-algebra, with the same modulus <math>\epsilon</math>, of A such that every number of C
is commutative with every number of Q.
The inverse of <math>E_{a,b} \equiv e^a f^b</math> is <math>\rho^{ab} E_{-a,-b}</math> since (by induction)
<math>f^b e^a = \rho^{ab} e^a f^b</math>
(51').
If X is any number of A, the <math>n^2</math> numbers
<math>N_{c,d} = \sum_{a,b=1}^{n} E^{-1}_{a,b} E_{c,d} X E_{a,b}</math> <math>(c, d=1, ..., n)</math>
* To distinguish it from the non-commutative "product" <math>\sum z_{ij}e_{i}E_{i}</math> of any two
sets <math>\sum x_i e_i</math> and <math>\sum y_j E_j</math> of numbers of an algebra.
† G. Scheffers, Math. Ann., vol. 39 (1891), pp. 364-374. In place of this
proof occupying ten pages, we shall give the short proof due to J. H. M. Wedderburn,
Proc. Roy. Soc. Edinb., vol. 26, 1 (1905-6), p. 48, of a more general theorem.

## PDF page 41

§ 22]
DIRECT PRODUCT OF TWO ALGEBRAS
29
are commutative with every number of Q. Indeed,
<math display="block">E_{r,s} \, N_{c,d} = \sum_{a,b=1}^{n} \rho^{ab} e^{r} f^{s} \, e^{-a} f^{-b} \, E_{c,d} \, X E_{a,b} = \sum_{a,b} \rho^{ab-as} e^{r-a} f^{s-b} \, E_{c,d} \, X E_{a,b}</math>
<math display="block">=\sum_{\alpha,\beta=1}^{n}\rho^{r\beta+\alpha\beta}e^{-\alpha}f^{-\beta}E_{c,\alpha}XE_{r+\alpha,\beta+\beta}=N_{c,\alpha}E_{r,s},</math>
in which we have replaced the summation indices <math>a</math>, <math>b</math> by <math>r + a</math>, <math>s + \beta</math>,
respectively. We find at once that
<math>E^{-1}_{c,d} E^{-1}_{a,b} E_{c,d} = \rho^{ad-bc} E^{-1}_{a,b}</math>
Summing for <math>c, d = 1, ..., n</math>, we get zero unless <math>a</math> and <math>b</math> are multiples
of <math>n</math>, i.e. unless <math>E_{a,b} = \epsilon</math>, and then we get <math>n^2 \epsilon</math>. Hence
<math display="block">\sum_{c,d} E^{-1}_{c,d} N_{c,d} = n^2 X.</math>
The set C of all numbers <math>\lambda, \mu, \ldots</math> of A which are commutative with
every X of A contains <math>\epsilon</math>, <math>\lambda + \mu</math>, <math>\lambda \mu</math>, and hence is a sub-algebra with
the modulus <math>\epsilon</math>. We saw that C contains every <math>N_{\epsilon,d}</math> and that X is
expressible as a sum of products of numbers <math>E^{-1}_{c,d}</math> of Q by numbers
<math>N_{c,d}</math> of C. Hence every X of A is in the direct product QC. The
product is direct since
<math display="block">\sum_{a,b=1}^{\infty} E^{-1}{}_{a,b} \gamma_{a,b} = 0</math>
<math>(\gamma's \text{ in } C)</math>
implies that each <math>\gamma = 0</math>. Since <math>\gamma</math> is commutative with the E's,
<math display="block">0 = \sum_{a,b,c,d} \sum_{d} E^{-1}_{c,d} E^{-1}_{a,b} E_{c,d} \gamma_{a,b} = n^2 \gamma_{nn}.</math>
To prove that <math>\gamma_{\alpha\beta} = 0</math>, we multiply the given relation by <math>E_{\alpha,\beta}</math> and use
the resulting relation in which <math>\gamma_{\alpha\beta}</math> is the coefficient of <math>\epsilon = E^{-1}</math>, ...
The complex algebra defined by (51) is equivalent to the complex
matric algebra of § 4. Indeed, (51) are satisfied if
<math>e = e_{12} + e_{23} + \ldots + e_{n1}, \quad f = e_{11} + \rho^{-1}e_{22} + \ldots + \rho^{-(n-1)}e_{nn}.</math>
The algebra (51) is Sylvester's algebra of nonions if <math>n = 3</math> (§ 13).
23. Units normalized relatively to a fixed number.
Given a number <math>a = \sum a_i e_i</math> of any algebra whose coordinates are
scalars, i.e. ordinary complex numbers, we can find a number
<math display="block">y = \sum y_i e_i \neq 0</math>
and a scalar w such that
(52).
<math>\alpha y = \omega y</math>

## PDF page 42

30
[(53)]
NORMALIZED UNITS
By (20) and the linear independence of the e's, necessary and sufficient
conditions for (52) are
<math display="block">\sum_{i, j=1}^{n} \gamma_{ijk} a_i y_j - \omega y_k = 0 \qquad (k=1, \ldots, n).</math>
The determinant of the coefficients of <math>y_1, ..., y_n</math> is <math>\delta(\omega)</math>, given by (40)
with <math>x = a</math>. Hence <math>\delta(\omega) = 0</math> is a necessary and sufficient condition for
the existence of a number <math>y \neq 0</math> satisfying (52).
For the general number x let <math>\delta(\omega) = 0</math> define <math>\omega</math> as an h-valued
function of <math>x_1, ..., x_n</math>, as in the theory of algebraic functions. Let
<math>\alpha</math> be a particular number <math>x</math> for which there are <math>h</math> distinct roots
<math>\omega_1, ..., \omega_h</math> of multiplicities <math>m_1, ..., m_h</math>.
If <math>y_1</math> is a second solution of (52), then <math>cy + c_1y_1</math> is a solution, where
<math>c</math> and <math>c_1</math> are any scalars. Hence all solutions <math>y</math> are linear functions of
certain t linearly independent solutions, which we take as the first t of
our new units <math>e_1, \ldots</math> Then <math>ae_j = \omega_1 e_j \ (j \leq t)</math> give
<math display="block">\sum_{i=1}^{n} \alpha_{i} \gamma_{ijk} = \omega_{1} \delta_{jk} \qquad (k=1, ..., n \; ; \; j=1, ..., t) </math> (53),
where, as usual, <math>\delta_{jj} = 1</math>, <math>\delta_{jk} = 0</math> <math>(k \neq j)</math>. Then (§ 16)
<math display="block">\delta\left(\omega\right) = \begin{vmatrix} \sum_{i=1}^{n} a_i \gamma_{ijk} - \omega \delta_{jk} \end{vmatrix} = \begin{vmatrix} \omega_1 - \omega & 0 & \dots & 0 \\ 0 & \omega_1 - \omega & \dots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \dots & \omega_1 - \omega \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \dots & 0 & M \end{vmatrix},</math>
in the first t columns of which all elements are zero except the
diagonal elements <math>\omega_1 - \omega</math>, while M denotes the matrix of the elements
in the last <math>n-t</math> rows and last <math>n-t</math> columns. Hence
<math display="block">\delta(\omega) = (\omega_1 - \omega)^t |M| = 0</math>
has <math>\omega_1</math> as a root of multiplicity <math>m_1</math>, where <math>m_1 \geq t</math>.
If <math>m_1 = t</math>, we proceed no further with <math>\omega_1</math> (see the example in § 24).
Next, let <math>m_1 > t</math>. Then there exist numbers <math>z = \sum z_j e_j + 0</math> such that
<math display="block">az = \omega_1 z + \sum_{k=1}^t c_k e_k</math>
(54):
<math display="block">\sum_{i,j,k=1}^{n} a_i z_j \gamma_{ijk} e_k = \omega_1 \sum_{k=1}^{n} z_k e_k + \sum_{k=1}^{t} c_k e_k.</math>
The coefficients of <math>e_k(k=1,...,t)</math> give equations which serve to
determine the <math>c_k</math>. Consider the coefficient of <math>e_k(k>t)</math>; in it the

## PDF page 43

§ 23]
NORMALIZED UNITS
31
coefficient of <math>z_j (j \le t)</math> is zero by (53), since <math>k > j</math>. We thus have
the conditions
<math display="block">\sum_{i=t+1}^{n}\sum_{i=1}^{n}\alpha_{i}\gamma_{ijk}z_{j}-\omega_{1}z_{k}=0 \qquad (k=t+1,\ldots,n).</math>
The matrix of the coefficients of the z's is the above M if <math>\omega = \omega_1</math>. But
<math>|M| = 0</math>. Hence there exist <math>t + t'</math> (<math>t' \ge 1</math>) linearly independent solutions
z of (54), including the solutions <math>e_1, ..., e_t</math> of (52). Taking these as
the first <math>t+t'</math> new e's, we find as before that <math>\delta(\omega)</math> has the factor
<math>(\omega_1 - \omega)^{t+t'}</math>. If <math>m_1 = t + t'</math>, we proceed no further with <math>\omega_1</math>. But if
<math>m_1 > t + t'</math>, there exist solutions <math>w \neq 0</math> of
<math>aw = \omega_1 w + \sum_{k=1}^{t+t'} d_k e_k</math>.
Ultimately we reach <math>m_1</math> linearly independent numbers
<math>a_1, a_1', \ldots, a_1^{(m_1-1)}</math>
such that
<math>aa_1^{(i)} = \omega_1 a_1^{(i)} + \text{lin. func. of } a_1, \dots, a_n^{(i-1)}</math>
(55).
Similarly, if <math>\omega_i</math> is a root of multiplicity <math>m_i</math>, there exist <math>m_i</math> linearly
independent numbers <math>a_j, a_j', ...,</math> such that*
<math>\alpha a_j^{(i)} = \omega_j a_j^{(i)} + \text{lin. func. of } a_j, \ldots, a_j^{(i-1)}</math>
(55').
These <math>n = m_1 + ... + m_h</math> numbers <math>a_j^{(l)}</math> are linearly independent.
First, if <math>a_2 = l</math>, where <math>l = c_0 a_1 + ... + c_k a_1^{(k)}</math>, <math>c_k \neq 0</math>, then
<math>\omega_2 \alpha_2 = a \alpha_2 = \omega_1 l + l', \quad 0 = (\omega_1 - \omega_2) l + l'.</math>
where <math>l'</math> is a linear function of <math>a_1, ..., a_1^{(k-1)}</math>. But <math>a_1^{(k)}</math> is not a linear
function of those a's. Next, if <math>a_2' = ca_2 + l</math>, multiplication by a on the
left gives
<math display="block">\omega_0 \alpha_0' + q \alpha_0 = c \omega_0 \alpha_0 + \omega_1 l + l'.</math>
Eliminating <math>a_2</math>, we get
<math>q\alpha_0 = (\omega_1 - \omega_0) l + l'</math>
which was proved impossible if <math>g \neq 0</math> or <math>g = 0</math>. The general step of the
proof follows similarly by induction. Hence the agin may be introduced
as n units normalized relatively to a.
By the proof leading to (55), if ax differs from ω<sub>1</sub>x by a linear
function of <math>a_1, a_1', ...,</math> then <math>x</math> itself is such a linear function.
* For the case of associative algebras having a modulus, this was stated without
proof by E. Cartan, Ann. Fac. Sc. Toulouse, vol. 12 (1898), memoir B, p. 17.

## PDF page 44

32
[(56)]
NORMALIZED UNITS
Occasionally we shall use the result similar to our first one: there
is a number <math>y \neq 0</math> and a scalar <math>\omega</math> such that
(56)
<math>yx = \omega y</math>
if and only if <math>\delta'(\omega) = 0</math>.
24.
<b>Example.</b> The algebra with the units <math>e_1, ..., e_5</math>, such that
<math>e_1e_5=e_1</math>, <math>e_2e_3=e_1</math>, <math>e_2e_5=e_2</math>, <math>e_3e_5=e_3</math>,
<math>e_4e_1=e_1</math>, <math>e_4e_2=e_2</math>, <math>e_4^2=e_4</math>, <math>e_5e_3=e_3</math>, <math>e_5^2=e_5</math>,
while the remaining <math>e_i e_j</math> are zero, is associative and has the modulus <math>\epsilon = e_4 + e_5</math>.
The conditions for <math>xy = \omega y</math> are
<math>(x_4 - \omega)y_1 + x_2y_3 + x_1y_5 = 0</math>, <math>(x_4 - \omega)y_2 + x_2y_5 = 0</math>,
<math>(x_5 - \omega) y_3 + x_3 y_5 = 0</math>, <math>(x_4 - \omega) y_4 = 0</math>, <math>(x_5 - \omega) y_5 = 0</math>.
The determinant of the coefficients of <math>y_1, ..., y_5</math> is evidently
<math>\delta(\omega) \equiv (x_4 - \omega)^3 (x_5 - \omega)^2</math>.
For <math>x = a = e_5</math>, <math>x_5 = 1</math>, <math>x_i = 0</math> (<math>i < 5</math>), and <math>\delta(\omega) = 0</math> has the roots 0, 1.
If <math>\omega=0</math>, the five conditions reduce to <math>y_3=y_5=0</math>. Since <math>y_1, y_2, y_4</math> are
arbitrary, we may take <math>e_1</math>, <math>e_2</math>, <math>e_4</math> as the linearly independent solutions y of
<math>ay=0</math>. Next, if <math>\omega=1</math>, the conditions reduce to <math>y_1=y_2=y_4=0</math>, and we may
take <math>e_3</math>, <math>e_5</math> as the linearly independent solutions y of <math>ay = y</math>. Hence <math>e_1</math>, <math>e_2</math>, <math>e_4</math>,
<math>e_3</math>, <math>e_5</math> are units normalized relatively to <math>a=e</math>.

## PDF page 45

PART II
REVISION
OF CARTAN'S
GENERAL
THEORY OF
COMPLEX
LINEAR
ASSOCIATIVE
ALGEBRAS
WITH A MODULUS
25.
Units having a character. If <math>x</math> is any number, <math>\S 23</math>
gives
<math display="block">a(a_1x) = (aa_1) x = (\omega_1a_1) x = \omega_1(a_1x).</math>
Hence (end of § 23), <math>a_1x</math> is a linear function of <math>a_1</math>, <math>a_1'</math>, .... Next,
<math>a(a_1'x) = (\omega_1 a_1' + \lambda a_1) x = \omega_1(a_1'x) + \text{lin. func. of } a_1, a_1', \ldots</math>
Hence <math>a_1'x</math> is a linear function of <math>a_1, a_1', \ldots</math> By induction, we see
similarly that any <math>a_j^{(i)}x</math> is a linear function of <math>a_j</math>, <math>a_j'</math>, ....
If <math>\epsilon</math> is the modulus, <math>\epsilon = \epsilon_1 + \ldots + \epsilon_h</math>, where <math>\epsilon_j</math> is a linear function of
the units <math>a_j, a_j', \ldots</math> By the preceding result, <math>\epsilon_j a_1^{(i)}</math> is a linear function
of <math>a_j, a_j', \ldots</math> Hence
<math display="block">\alpha_1^{(i)} = \epsilon \alpha_1^{(i)} = \sum_{i=1}^h \epsilon_i \alpha_1^{(i)}</math>
<math>\epsilon_1 a_1^{(i)} = a_1^{(i)}, \quad \epsilon_j a_1^{(i)} = 0 \quad (j \neq 1)</math>
(57).
gives
Similarly, we have
<math>\epsilon_2 \alpha_2^{(i)} = \alpha_2^{(i)}, \quad \epsilon_j \alpha_2^{(i)} = 0 \qquad (j \neq 2), \dots </math> (58).
It follows at once that
<math>\epsilon_j^2 = \epsilon_j, \quad \epsilon_j \epsilon_k = 0 \qquad (j \neq k)</math>
(59).
We shall call <math>\epsilon_1, \ldots, \epsilon_h</math> partial moduli of the algebra.
Since <math>\epsilon_1 \epsilon_1 = \epsilon_1</math>, not every <math>a_1^{(i)} \epsilon_1</math> is zero. After a suitable rearrange-
ment of <math>a_1, a_1', ...,</math> we may assume that
<math>a_1 \epsilon_1, \ a_1' \epsilon_1, \ldots, a_1^{(p-1)} \epsilon_1 \qquad (p \ge 1)</math>
(60)
are linearly independent, while each <math>a_1^{(k)}\epsilon_1</math> <math>(k \geq p)</math> is linearly dependent
on the numbers (60):
<math>a_1^{(k)} \epsilon_1 = c_0^{(k)} a_1 \epsilon_1 + \ldots + c_{p-1}^{(k)} a_1^{(p-1)} \epsilon_1 \qquad (k = p, \ldots, m_1 - 1).</math>
D.

## PDF page 46

34
[(61)]
UNITS HAVING A CHARACTER
In place of these units <math>a_1^{(k)}</math> we introduce
<math display="block">\overline{\mathbf{a}}_1^{(k)} = a_1^{(k)} - c_0^{(k)} \mathbf{a}_1 - \dots - c_{n-1}^{(k)} a_1^{(p-1)} \qquad (k = p, \dots, m_1 - 1).</math>
Now <math>\bar{a}_1^{(k)} \epsilon_1 = 0</math>. Dropping the bars from these a's, we have <math>m_1</math> linearly
independent units <math>a_1^{(i)}</math> <math>(i = 0, 1, ..., m_1 - 1)</math> such that
<math>a_1^{(k)} \epsilon_1 = 0</math>  <math>(k = p, ..., m_1 - 1)</math>
(61),
while the numbers (60) are linearly independent.
The property that any <math>a_1^{(i)}x</math> is a linear function of <math>a_1, a_1', \ldots</math>
evidently holds true also for the present <math>a_1^{(i)}</math>. Set
<math>a_1 \epsilon_1 = k_0 a_1 + \ldots + k_{m_1-1} a_1^{(m_1-1)}</math>.
Since <math>(a_1 \epsilon_1) \epsilon_1 = a_1 \epsilon_1</math>, we have, by (61),
<math display="block">\alpha_1 \epsilon_1 = k_0 \alpha_1 \epsilon_1 + \ldots + k_{p-1} \alpha_1^{(p-1)} \epsilon_1.</math>
By the linear independence of the numbers (60),
<math>k_0 = 1</math>, <math>k_1 = 0</math>, ..., <math>k_{p-1} = 0</math>,
<math>a_1 \epsilon_1 = a_1 + k_n a_1^{(p)} + \ldots + k_{m_1-1} a_1^{(m_1-1)}</math>
Similarly,
<math>a_1' \epsilon_1 = a_1' + k_p' a_1^{(p)} + \dots, \quad a_1^{(p-1)} \epsilon_1 = a_1^{(p-1)} + k_p^{(p-1)} a_1^{(p)} + \dots</math>
The right members <math>\bar{a}_1, \bar{a}_1', ..., \bar{a}_1^{(p-1)}</math> of these equations, together with
<math>a_1^{(p)}, \ldots, a_1^{(m_1-1)}</math>, evidently give <math>m_1</math> linearly independent functions of
the <math>a_1^{(i)}</math>, and hence may be taken as new units. But, by (61),
<math>\overline{a}_1\epsilon_1=a_1\epsilon_1=\overline{a}_1, \quad \overline{a}_1'\epsilon_1=\overline{a}_1', \ldots, \quad \overline{a}_1^{(p-1)}\epsilon_1=\overline{a}_1^{(p-1)}.</math>
Dropping the bars from these <math>\alpha</math>'s, we have (61) and
<math>a_1 \epsilon_1 = a_1, \quad a_1' \epsilon_1 = a_1', \dots, \quad a_1^{(p-1)} \epsilon_1 = a_1^{(p-1)}.</math>
Since <math>\epsilon_1 \epsilon_i = 0</math> by (59), if <math>i \neq 1</math>,
<math>\alpha_1 \epsilon_i = (\alpha_1 \epsilon_1) \epsilon_i = \alpha_1 (\epsilon_1 \epsilon_i) = 0, \quad \alpha_1' \epsilon_i = 0, \dots, \quad \alpha_1^{(p-1)} \epsilon_i = 0 \quad (i \neq 1).</math>
Hence if <math>\eta</math> is any one of the numbers <math>a_1, a_1', ..., a_1^{(p-1)}</math>,
<math>\eta \epsilon_1 = \eta, \quad \eta \epsilon_i = 0, \quad \epsilon_1 \eta = \eta, \quad \epsilon_i \eta = 0 \qquad (i \neq 1)</math>
(62),
the last pair from (57). These hold also for <math>\eta = \epsilon_1</math> by (59).
If <math>p = m_1</math>, the <math>\eta</math>'s include all the <math>a_1^{(j)}</math>. But if <math>p < m_1, a_1^{(k)} \epsilon_2, ...,</math>
<math>a_1^{(k)} \epsilon_h</math> are not all zero, where k is any fixed integer <math>\geq p</math>. For, if so,
<math>a_1^{(k)} = a_1^{(k)} \epsilon = a_1^{(k)} \epsilon_1</math>, contrary to (61). Suppose first that not all of the
<math>a_1^{(k)}\epsilon_2</math> are zero. Then the argument beginning with (60) is repeated
for <math>a_1^{(p)}, \ldots, a_1^{(m_1-1)}</math> in their relation to <math>\epsilon_2</math>. Thus if <math>\eta</math> is any one of
certain <math>q > 0</math> numbers <math>a_1^{(p)}, \ldots, a_1^{(p+q-1)},</math>
<math>
\eta \epsilon_2 = \eta, \quad \eta \epsilon_i = 0 \quad (i \neq 2), \quad \epsilon_1 \eta = \eta, \quad \epsilon_i \eta = 0 \quad (i \neq 1)
</math>
(63),

## PDF page 47

§ 25]
UNITS HAVING A CHARACTER
35
the last pair from (57). We proceed similarly until the set
<math>a_1, a_1', \ldots, a_1^{(m_1-1)}</math>
is exhausted.
An analogous distribution of the <math>a_2^{(i)}</math> into sets of <math>\eta</math>'s may be made,
and likewise for the <math>a_h^{(i)}</math>. We may assume that <math>\epsilon_2</math> is one of the <math>\eta</math>'s
coming from the <math>a_2^{(i)}</math>, etc.
Any <math>\eta</math> in (62) is said to have the character (1, 1); any <math>\eta</math> in (63)
the character <math>(1, 2)</math>. In general, <math>\eta</math> is of character * <math>(a, \beta)</math> if
<math>\epsilon_i \eta = 0 \ (i \neq \alpha), \quad \epsilon_\alpha \eta = \eta, \quad \eta \epsilon_i = 0 \ (j \neq \beta), \quad \eta \epsilon_\beta = \eta </math> (64).
In particular, <math>\epsilon_i</math> is of character <math>(i, i)</math>.
THEOREM.
We can find n linearly independent units <math>\epsilon_1, \ldots, \epsilon_h</math>,
<math>\eta_1, \ldots, \eta_{n-h}</math> each having a definite character.
For example, in the matric algebra of <math>n^2</math> units <math>e_0</math> in § 4, the
<math>\epsilon_i = e_{ii} (i = 1, ..., n)</math> are the partial moduli, and <math>e_{ij}</math> is of character <math>(i, j)</math>
in view of (14).
Any number <math>\eta</math> is said to be of character <math>(\alpha, \beta)</math> if and only if it
satisfies relations (64). The sum of two numbers of like character has
that character; the sum of two numbers of unlike character has no
character. For, if <math>\eta</math> has the character <math>(a, \beta)</math> and <math>\eta'</math> the character <math>(\gamma, \delta)</math>,
<math>(\eta + \eta') \epsilon_{\beta} = \eta + \eta' \text{ or } \eta, \text{ according as } \beta = \delta \text{ or } \beta \neq \delta; \text{ while}</math>
<math>\epsilon_{\alpha}(\eta + \eta') = \eta + \eta'</math> or <math>\eta</math>,
according as <math>\gamma = \alpha</math> or <math>\gamma \neq \alpha</math>.
Example. We shall find the character of each of the normalized
26.
units in the example of § 24. Here <math>h=2</math>, <math>\epsilon_1=e_4</math>, <math>\epsilon_2=e_6</math>. Then
<math>\epsilon_1^2 = \epsilon_1, \quad \epsilon_2^2 = \epsilon_2, \quad \epsilon_1 \epsilon_2 = \epsilon_2 \epsilon_1 = 0,</math>
<math>\epsilon_1 e_1 = e_1, \quad \epsilon_2 e_1 = 0, \quad e_1 \epsilon_1 = 0, \quad e_1 \epsilon_2 = e_1,</math>
<math>\epsilon_1 e_2 = e_2, \quad \epsilon_2 e_2 = 0, \quad e_2 \epsilon_1 = 0, \quad e_2 \epsilon_2 = e_2,</math>
<math>\epsilon_1 e_3 = 0</math>, <math>\epsilon_2 e_3 = e_3</math>, <math>e_3 \epsilon_4 = 0</math>, <math>e_3 \epsilon_2 = e_3</math>.
Hence <math>\epsilon_1</math> is of character (1, 1), <math>\epsilon_2</math> and <math>\epsilon_3</math> are of character (2, 2), <math>\epsilon_1</math> and <math>\epsilon_3</math> of
character (1, 2).
The product of a number <math>\eta</math> of character <math>(a, \beta)</math>
Theorem.
27.
by a number <math>\eta'</math> of character <math>(\gamma, \delta)</math> is zero if <math>\beta \neq \gamma</math>, and is either zero or
is a number of character <math>(a, \delta)</math> if <math>\beta = \gamma</math>.
* Introduced by G. Scheffers, Math. Ann., vol. 39 (1891), p. 313, in connection
with algebras without a quaternion sub-algebra. The present proof of the general
theorem is an amplification of that by Cartan, l. c., p. 19.
3-2

## PDF page 48

36
THE SUB-ALGEBRAS <math>\Sigma_i</math>
<math>\epsilon_{lpha}\eta=\eta\,\epsilon_{eta}=\eta,\quad \epsilon_{\gamma}\eta'=\eta'\,\epsilon_{eta}=\eta',</math>
We have
<math>\epsilon_{\alpha}\eta\eta' = \eta\eta' = \eta\eta'\epsilon_{\delta}, \quad \eta\eta' = (\eta\epsilon_{\delta})(\epsilon_{\gamma}\eta') = \eta(\epsilon_{\delta}\epsilon_{\gamma})\eta'.</math>
Hence, if <math>\beta \neq \gamma</math>, <math>\eta \eta' = 0</math> since <math>\epsilon_{\beta} \epsilon_{\gamma} = 0</math>. If <math>\beta = \gamma</math> and <math>\eta \eta' \neq 0</math>, then <math>\eta \eta'</math> is
of character <math>(a, \delta)</math>.
28. The sub-algebras <math>\Sigma_i</math>. The product of two numbers of
character (i, i) is of character (i, i). In view also of the remark at
the end of § 25, all of the numbers of character (i, i) of the initial
algebra <math>\Sigma</math> form a linear associative sub-algebra <math>\Sigma_i</math> with the modulus <math>\epsilon_i</math>.
The characteristic equation* for <math>\Sigma_1</math> has a single root and its
multiplicity is the number m of units of <math>\Sigma_1</math>.
For, if it had two or more distinct roots, <math>\Sigma_1</math> would have at least
two partial moduli <math>\epsilon_1'</math>, <math>\epsilon_1''</math> (§ 25). Set
<math display="block">\alpha = x_1' \epsilon_1' + x_1'' \epsilon_1'' + x_2 \epsilon_2 + \ldots + x_h \epsilon_h,</math>
where the x's are arbitrary scalars.
Then
<math>a\epsilon_1' = x_1'\epsilon_1', \quad a\epsilon_1'' = x_1''\epsilon_1'', \quad a\epsilon_2 = x_2\epsilon_2, \dots, a\epsilon_h = x_h\epsilon_h.</math>
Hence (§ 23) the characteristic equation of <math>a</math> for <math>\Sigma</math> has the distinct
roots <math>x_1', x_1'', x_2, ..., x_h</math>, whereas the number is <math>\leq h</math>.
<b>29.</b> Choose the units <math>e_i</math> of <math>\Sigma_1</math> so that <math>e_1</math> is the modulus <math>\epsilon_1</math>. As
just proved, the characteristic equation of <math>x = \sum x_i e_i</math> is <math>(\omega - l)^m = 0</math>,
where <math>l = \sum c_i x_i</math>. Taking <math>x = \epsilon_1</math>, we have <math>\omega = 1</math>, <math>l = c_1</math>, whence <math>c_1 = 1</math>.
Take as new units <math>\epsilon_1</math>, <math>\eta_i = e_i - c_i \epsilon_1</math> <math>(i = 2, ..., m)</math>. Then
<math>x = x_1' \epsilon_1 + \sum x_i \eta_i</math>
where <math>x_1' = l</math>. For the algebra in the new units, the characteristic
equation of x is <math>(\omega - x_1)^m = 0</math>. Hence the characteristic equation of
any linear combination of <math>\eta_2, ..., \eta_m</math> has no root other than zero.
Nilpotent numbers. A number is called nilpotent if
30.
some power of it is zero. Let <math>\eta^k = 0</math>, <math>\eta \neq 0</math>, and call <math>\omega</math> any root of the
characteristic equation of <math>\eta</math>. There exists (§ 23) a number <math>y \neq 0</math> such
that <math>\eta y = \omega y</math>. Multiply by <math>\eta^{k-1}</math> on the left. Thus
<math display="block">0 = \omega \eta^{k-1} y = \omega \eta^{k-2} (\omega y) = \omega^2 \eta^{k-3} (\omega y) = \dots = \omega^k y.</math>
Hence <math>\omega = 0</math>. Conversely, if the characteristic equation of <math>\eta</math> has all
its roots zero, a power of <math>\eta</math> vanishes by Theorem 1, § 15. Hence
* The prefix "right hand" will often be omitted.
† B. Peirce, Amer. Journ. Math., vol. 4 (1881), p. 97. The name Wurzel der
Null was used by Frobenius, Sitzungsb. Ak. Berlin, 1903, p. 635; pseudo-nul by
Cartan, l.c., p. 21.

## PDF page 49

§ 30]
NILPOTENT NUMBERS
37
a number is nilpotent if and only if every root of its characteristic
equation is zero. Similarly, or by Theorem 1 of § 19, every root of
the left-hand characteristic equation of a nilpotent number is zero.
31.
<b>Theorem.</b> As the units of <math>\Sigma_1</math> we may take its modulus <math>\epsilon_1</math>
and <math>m-1</math> nilpotent numbers <math>\eta</math> such that any linear function of the <math>\eta</math>'s
is nilpotent.
This follows from the result in § 29.
32.
Normalized units. In view of the last theorem and that
in <math>\S 25</math>, we may take the <math>n</math> units of any algebra to be the partial
moduli <math>\epsilon_1, \ldots, \epsilon_h</math> and <math>n-h</math> nilpotent numbers each of a definite
Note that any number of character <math>(\alpha, \beta)</math>, <math>\alpha \neq \beta</math>, is
character.
nilpotent, since its square is zero.
33. Examples. In the algebra considered in §§ 24, 26, the sub-algebra
<math>\Sigma_2</math> of numbers of character <math>(2, 2)</math> has the two units <math>\epsilon_2</math> and <math>\epsilon_3</math>, of which <math>\epsilon_2</math> is the
partial modulus. For <math>x=e_3</math>, the formula in § 24 gives <math>\delta(\omega)=\omega^5</math>. Thus <math>e_3</math> is
nilpotent in the main algebra <math>\Sigma</math>. We have <math>e_3^2=0</math>. Similarly, <math>e_1</math> and <math>e_2</math> are
nilpotent. Hence the normalized units of <math>\Sigma</math> are <math>\epsilon_1</math>, <math>\epsilon_2</math> and the nilpotent
numbers <math>e_1</math>, <math>e_2</math>, <math>e_3</math>.
As an instructive example, the reader may show by means of the general
theory that the algebra of complex quaternions is equivalent to the matric
algebra of four units [take <math>a=i</math> in § 23].
He may treat also the algebra <math>(e_1, \ldots, e_4)</math> where
<math>e_1e_4=e_1</math>, <math>e_2e_3=e_2</math>, <math>e_3e_1=e_1</math>, <math>e_3^2=e_3</math>, <math>e_4^2=e_4</math>, <math>e_4e_2=e_2</math>,
while all further products of two units are zero; the modulus is <math>e_3 + e_4</math>.
34. Theorem. The product of any nilpotent number n of
character (i, i) by any number u of the same character is nilpotent.
For concreteness, take <math>i=1</math>. Then the product <math>\eta u</math> is of character
<math>(1, 1)</math> and hence is in algebra <math>\Sigma_1</math>. By § 31,
<math>\eta u = a\epsilon_1 + \eta'</math> (a scalar, <math>\eta'</math> nilpotent).
Since <math>\eta \epsilon_1 = \eta</math>, we have
<math>\eta^2 u = \alpha \eta + \eta \eta'</math>.
Let m be the least positive integer for which <math>\eta^m u = 0</math>. If <math>m = 1</math>, the
theorem is true. If <math>m \ge 2</math>, multiply the preceding equation by <math>\eta^{m-2}</math>
on the left. Thus
<math>\eta^{m-1}\eta' = (-\alpha)\eta^{m-1}, \quad \eta^{m-1} \neq 0.</math>
Hence <math>\alpha = 0</math> since <math>\eta'</math> is nilpotent (end of § 30). Thus <math>\eta u = \eta'</math>.
In the example in § 26, § 33, e3 is nilpotent, e3 and c4 are of
character <math>(2, 2)</math>, and <math>e_3\epsilon_2 = e_3</math> is nilpotent.

## PDF page 50

[(65)]
38
ALGEBRAS <math>A_1</math> OF FIRST CATEGORY
35. Separation of algebras into two categories. An
algebra is of the first category if the determinant <math>\Delta(x)</math> of its general
number <math>\sum x_i e_i</math> is the product of n linear homogeneous functions* of
<math>x_1, \ldots, x_n</math>.
An algebra is of the second category if <math>\Delta(x)</math> has a non-linear
irreducible factor <math>f(x_1, ..., x_n)</math>.
A binary algebra is of the first category since a homogeneous function of <math>x_1</math>
and <math>x_2</math> is a product of linear functions. The five types of ternary algebras
(45)—(49) are of the first category, since for each <math>\Delta(x) \equiv \delta(0)</math> is a product of
linear factors.
The algebra of complex quaternions is of the second category, since (§ 12)
<math>\Delta(q)</math> is the square of the irreducible function <math>x^2+y^2+z^2+w^2</math>. We may also
employ the equivalent matric algebra of § 4. By (16), (17),
<math display="block">\Delta(m) = \begin{vmatrix} a & 0 & b & 0 \\ 0 & a & 0 & b \\ c & 0 & d & 0 \\ 0 & c & 0 & d \end{vmatrix} = \begin{vmatrix} c & d & 0 & 0 \\ 0 & 0 & a & b \\ 0 & 0 & c & d \end{vmatrix}</math>
(65),
while a general determinant of order two is irreducible.
We shall later (§ 46) prove that an algebra is of the second category
if and only if it has a quaternion sub-algebra. It will then follow that
the above classification into algebras of the first and second categories
(Cartan, l. c., p. 24) coincides with that tof algebras into those without
and with quaternion sub-algebras.
Algebras <math>A_1</math> of the first category.
36.
<b>Theorem.</b> The sum of two nilpotent numbers of <math>A_1</math> is
nilpotent.
The distinct roots of the characteristic equation of <math>x = \sum x_i \rho_i</math> are by
hypothesis of the form
<math>(i = 1, ..., h),</math>
<math display="block">\omega_i = a_{i1}x_1 + \ldots + a_{in}x_n</math>
where the a's depend only upon the constants of multiplication <math>\gamma_{ijk}</math>.
Hence the roots of the characteristic equation of <math>x + x'</math> are
<math>a_{i1}(x_1 + x_1') + \ldots = \omega_i + \omega_i'.</math>
* With coefficients in F, in case we are treating algebras over a field F. Since
the ω's are now in F and since the work in §§ 36-39 is purely rational, we obtain
normalized units (§ 39) with coordinates in <math>F</math>; cf. ex. in §§ 26, 33.
† G. Scheffers, Math. Ann., vol. 39 (1891), p. 305: Quaternionsysteme, Nicht-
quaternionsysteme. Th. Molien, ibid., vol. 41 (1893), p. 83.

## PDF page 51

§ 36]
ALGEBRAS A, OF FIRST CATEGORY
39
If x and x' are nilpotent, each <math>\omega_i = \omega_i' = 0</math>, and <math>x + x'</math> is nilpotent.
By § 32, any number of <math>A_1</math> is of the form
<math>x_1\epsilon_1 + \ldots + x_h\epsilon_h + y_1\eta_1 + \ldots + y_k\eta_k</math>
(66),
where the <math>\epsilon</math>'s are the partial moduli and the <math>\eta</math>'s are nilpotent numbers,
each with a definite character.
Since
<math>(x_1\epsilon_1 + \ldots + x_h\epsilon_h)\epsilon_i = x_i\epsilon_i</math>
the characteristic equation of (66) has the roots <math>x_1, \ldots, x_n</math> and hence
(66) is nilpotent if and only if <math>x_1, \ldots, x_h</math> are all zero.
<b>Theorem.</b> The product of any nilpotent number of <math>A_1</math> by
37.
any number <math>u</math> of <math>A_1</math> is nilpotent.
It suffices to prove that <math>\eta_1 u, \ldots, \eta_k u</math> are nilpotent.
Consider an <math>\eta</math> of character <math>(1, 1)</math>, and express <math>u</math> as a sum of
components each of a definite character. The product of <math>\eta</math> by a com-
ponent will be zero or of character <math>(1, j), j > 1</math>, and hence a nilpotent
number (§ 32), unless the component be of character (1, 1). In the
latter case also, the product is nilpotent (§ 34).
Consider an <math>\eta</math> of character <math>\neq</math> <math>(i, i)</math>, say <math>(1, 2)</math>. As before it suffices
to take <math>u</math> of character <math>(2, 1)</math>. Then <math>\eta u</math> is of character <math>(1, 1)</math> and
<math>
\eta u = \alpha \epsilon_1 + \zeta_1
</math>
If
where <math>a</math> is a scalar and <math>\zeta</math> a nilpotent number of character <math>(1, 1)</math>.
<math>a = 0</math>, the theorem is proved. Henceforth, let <math>a \neq 0</math>. Then (§ 34)
<math>(\eta u)^2 = a^2 \epsilon_1 + \zeta_1, \quad \zeta_1 = 2a\zeta + \zeta^2,</math>
where <math>\zeta_1</math> is a nilpotent number of <math>\Sigma_1</math> in § 28. By induction,
<math display="block">(\eta u)^m = \alpha^m \epsilon_1 + \zeta_m,</math>
where <math>\zeta_m</math> is nilpotent. If <math>u\eta</math> is nilpotent, its mth power is zero,
Then
where <math>m</math> is a certain integer.
<math display="block">0 = \eta (u\eta)^m = (\eta u)^m \eta = \alpha^m \eta + \zeta_m \eta,</math>
since <math>\epsilon_1 \eta = \eta</math>, <math>\eta</math> being of character <math>(1, 2)</math>. Thus <math>-\alpha^m</math> is a root of the
characteristic equation of <math>\zeta_m</math>. This is impossible since <math>a \neq 0</math> and <math>\zeta_m</math> is
nilpotent. Hence <math>u\eta</math> is not nilpotent:
<math>u\eta = \alpha' \epsilon_2 + \zeta',</math>
where <math>a' \neq 0</math> and <math>\zeta'</math> is nilpotent of character <math>(2, 2)</math>.
If <math>v \neq 0</math> is of character <math>(2, 1)</math>, then <math>\eta v \neq 0</math>. For, if <math>\eta v = 0</math>,
<math display="block">0 = u(\eta v) = (u\eta) v = a'v + \zeta'v,</math>
whereas <math>-a'</math> is not a root of the characteristic equation of the

## PDF page 52

ALGEBRAS <math>A_1</math> OF FIRST CATEGORY
40
nilpotent number <math>\zeta'</math> since <math>\alpha'</math> is not zero. If <math>v_1, \ldots, v_t</math> form a complete*
set of linearly independent numbers of character <math>(2, 1)</math>, then <math>\eta v_1, ..., \eta v_t</math>
are linearly independent and of character (1, 1). Indeed, <math>\Sigma c_i \eta v_i = 0</math>
implies <math>\eta v = 0</math>, where <math>v = \sum c_i v_i</math>.
If <math>w \neq 0</math> is of character <math>(1, 1)</math>, then <math>uw \neq 0</math>. For, if <math>uw = 0</math>,
<math display="block">0 = (\eta u) w = aw + \zeta w,</math>
whereas <math>-\alpha</math> is not a root of the characteristic equation of the nilpotent
number <math>\zeta</math>. If <math>w_1, ..., w_\tau</math> form a complete set of linearly independent
numbers of character <math>(1, 1)</math>, then <math>uw_1, \ldots, uw_\tau</math> are linearly independent
and of character <math>(2, 1)</math>. Indeed, <math>\Sigma c_i u w_i = 0</math> implies <math>u w = 0</math>, <math>w = \Sigma c_i w_i</math>.
By the first result, <math>t \le \tau</math>; by the second, <math>\tau \le t</math>. Hence <math>\tau = t</math> and
<math>\eta v_1, \ldots, \eta v_t</math> form a complete set of linearly independent numbers of
character (1, 1). Hence there exist scalars <math>d_i</math> such that <math>\sum d_i \eta v_i = \epsilon_1</math>.
Thus <math>\eta v = \epsilon_1</math> for <math>v = \sum d_i v_i</math>. Here <math>\eta</math> is of character <math>(1, 2)</math> and <math>v</math> of
character (2, 1). Hence
<math>(\eta + v)(\epsilon_1 + v) = \epsilon_1 + v.</math>
The characteristic equation of <math>\eta + v</math> has therefore the root unity,
whereas it is the sum of two nilpotent numbers of <math>A_1</math> and hence is
The assumption that <math>\alpha \neq 0</math> has therefore led to a contra-
nilpotent.
diction.
By reversing the order of the factors in our products, we see that
the product of any number of <math>A_1</math> by any nilpotent number is nilpotent.
Corollary. The nilpotent numbers of <math>A_1</math> form a linear associative
algebra N without a modulus.
If it had a modulus <math>\eta</math>, then would <math>\eta u = u</math>, whereas unity is not
a root of the characteristic equation of the nilpotent number <math>\eta</math>.
An algebra is called <i>nilpotent</i> if all of its numbers are nilpotent.
Normalized units of a nilpotent algebra.
38.
Theorem. In a nilpotent algebra N, linearly independent units
<math>\eta_1, \ldots, \eta_k</math>, each of a definite character <math>\dagger</math>, can be chosen so that the product
of any two units <math>\eta_i</math> and <math>\eta_j</math> is a linear function of the units <math>\eta</math> whose
subscripts exceed both i and j.
If <math>k=1</math>, <math>\eta_1^2=a\eta_1</math>, where a is scalar. Since a is a root of the
* Any number of character (2, 1) is to be a linear function of <math>v_1, \ldots, v_t</math> with
scalar coefficients. The basis of the definition is the result at the end of § 25.
† This supplement concerning character applies to algebras N contained in an
algebra with partial moduli.

## PDF page 53

§ 38]
NORMALIZED UNITS OF A NILPOTENT ALGEBRA
41
characteristic equation of the nilpotent number <math>\eta_1</math>, we have <math>a=0</math>.
The theorem is thus true for <math>k=1</math>, since it states that <math>\eta_1^2</math> is a linear
function of the (non-existing) <math>\eta</math>'s whose subscripts exceed 1, and hence
that <math>\eta_1^2 = 0</math>.
Assuming that the theorem holds for nilpotent algebras with fewer
than k units, we shall prove it for an algebra N with k units <math>e_1, \ldots, e_k</math>.
LEMMA.
There exists a number u of N for which
<math>e_1 u = 0, \quad e_2 u = 0, \dots, \quad e_k u = 0</math>
(67).
Among all of the numbers <math>u</math> (including certainly a power of <math>e_1</math>) for
which <math>e_1u=0</math>, there may be some making <math>e_2u=0</math>, some making also
<math>e_3u=0</math>, etc. Suppose that the Lemma is false. Then none of these
u's satisfy (67). Hence there is an integer <math>m < k</math> for which
<math>e_1 u = 0, \quad e_2 u = 0, \dots, \quad e_m u = 0</math>
(68)
have a common solution <math>u \neq 0</math> and such that no common solution <math>u</math>
makes <math>eu = 0</math>, where e is any number of N, linearly independent of
<math>e_1, \ldots, e_m</math>. Any linear combination of solutions of (68) is a solution.
Hence we may assume that <math>u_1, \ldots, u_n</math> form a complete set of
linearly independent solutions of (68). For <math>j \leq m</math>, <math>(e_i e_j)</math> u is zero for
every solution <math>u</math>. Hence <math>e_i e_j</math> is a linear function of <math>e_1, \ldots, e_m</math>. Thus
<math>e_1, \ldots, e_m</math> are units of a nilpotent sub-algebra <math>N_1</math>. Since <math>m < k</math>, the
hypothesis for our induction shows that our theorem holds for <math>N_1</math>.
Hence, if <math>i \leq m, j \leq m, e_i e_j</math> is a linear function of the e's whose sub-
scripts exceed <math>i</math> and <math>j</math>, but not <math>m</math>.
Let <math>\nu</math> be any number <math>\neq 0</math> of <math>N</math>. Either <math>\nu</math> is a linear combination
of <math>u_1, \ldots, u_n</math>, or there exists a number <math>\eta</math> of <math>N_1</math> such that <math>\eta v</math> is a
linear combination <math>\neq 0</math> of <math>u_1, \ldots, u_n</math>. For, if <math>i \leq m</math>, <math>e_i e_m = 0</math>, as just
proved, so that <math>e_i(e_m \nu) = 0</math> and <math>e_m \nu</math> is a linear combination of the
independent solutions <math>u_1, \ldots, u_n</math> of (68). If <math>e_m v \neq 0</math>, our italicized
statement is proved. If <math>e_m \nu = 0</math>, every <math>e_i e_{m-1} \nu = 0</math> <math>(i \le m)</math>, since <math>e_i e_{m-1}</math>
is a multiple of <math>e_m</math>, as just proved. Thus <math>e_{m-1}\nu</math> is a linear combination
of <math>u_1, \ldots, u_n</math>. Hence our italicized statement follows unless possibly
each <math>e_i v = 0</math>; but then <math>v</math> itself is a linear combination of <math>u_1, \ldots, u_n</math>.
Taking <math>e_{m+1}u_1</math> as <math>\nu</math>, our italicized result shows that either <math>e_{m+1}u_1</math> or
some <math>\eta</math> times it is a linear function <math>\neq 0</math> of <math>u_1, \ldots, u_n</math>. In the respective
cases take <math>\zeta_1 = e_{m+1}</math> or <math>\eta e_{m+1}</math>. Thus <math>\zeta_1 u_1 \neq 0</math>. Since <math>\zeta_1</math> is nilpotent,
<math>\zeta_1 u_1 + s u_1</math>, where s is scalar. Hence, by a change of notation of the <math>u</math>'s,
we may take <math>\zeta_1 u_1 = u_2</math>.
Thus
For this new <math>u_2</math>, take <math>e_{m+1}u_2</math> as <math>\nu</math> in our italicized result.

## PDF page 54

42
[(69)]
NILPOTENT ALGEBRAS
<math>\zeta_2 = e_{m+1}</math> or <math>\eta' e_{m+1}</math> has the property that <math>\zeta_2 u_2</math> is a linear combination <math>\neq 0</math>
of <math>u_1, ..., u_n</math>. If <math>\zeta_2 u_2</math> be a linear function of <math>u_1, u_2</math>, we have
<math>\zeta_1 u_1 = u_2, \ \zeta_2 u_2 = u_3, \ldots, \ \zeta_{p-1} u_{p-1} = u_p, \ \zeta_p u_p = \lambda_1 u_1 + \ldots + \lambda_p u_p \ (69),</math>
for <math>p=2</math>, where the scalars <math>\lambda_1, \ldots, \lambda_p</math> are not all zero. In the contrary
case, we may take <math>\zeta_2 u_2 = u_3</math>. Proceeding with <math>u_3</math>, we obtain a number
<math>\zeta_3</math> such that <math>\zeta_3 u_3</math> is a linear function <math>\neq 0</math> of <math>u_1, \ldots, u_n</math>. If it involves
only <math>u_1</math>, <math>u_2</math>, <math>u_3</math>, we have (69) for <math>p=3</math>. If not, we take <math>\zeta_3 u_3 = u_4</math>, etc.
We may set <math>\lambda_1 = 0, ..., \lambda_{s-1} = 0, \lambda_s \neq 0</math>, where s is a certain integer
<math>\geq 1</math>. Set
<math display="block">l = \zeta_p \zeta_{p-1} \dots \zeta_{s+1} \zeta_s - \lambda_p \zeta_{p-1} \dots \zeta_s - \dots - \lambda_{s+2} \zeta_{s+1} \zeta_s - \lambda_{s+1} \zeta_s.</math>
Multiply by <math>u_s</math> on the right. By (69) the product is
<math display="block">\zeta_p u_p - \lambda_p u_p - \dots - \lambda_{s+2} u_{s+2} - \lambda_{s+1} u_{s+1} = \lambda_s u_s.</math>
Thus <math>lu_s = \lambda_s u_s</math>. But <math>l</math> is nilpotent and <math>\lambda_s \neq 0</math>. Hence the supposition
that the lemma is false has led to a contradiction.
Let therefore <math>u_1, ..., u_n (n \ge 1)</math> form a complete set of linearly
independent solutions <math>u</math> of the system of equations (67). Let <math>\eta</math> be
any number of N. Then <math>(e_j u_i) \eta = 0</math>, so that <math>u_i \eta</math> is a linear function of
<math>u_1, \ldots, u_n</math>:
<math display="block">u_i\eta = a_{i1}u_1 + \ldots + a_{in}u_n.</math>
If <math>u = \sum c_i u_i</math>, the conditions for <math>u\eta = \rho u</math> are
<math display="block">\sum_{i=1}^{n} c_i a_{i1} - c_1 \rho = 0, \dots, \qquad \sum_{i=1}^{n} c_i a_{in} - c_n \rho = 0.</math>
Let <math>\rho</math> be a root of
<math display="block">\begin{vmatrix} a_{11} - \rho & a_{21} & \dots & a_{n1} \\ \dots & \dots & \dots \\ a_{1n} & a_{2n} & \dots & a_{nn} - \rho \end{vmatrix} = 0.</math>
Then the determinant of the coefficients of <math>c_1, ..., c_n</math> in our n equations
is zero, which therefore have a set of solutions <math>c_1, \ldots, c_n</math> not all zero.
By <math>u\eta = \rho u</math>, <math>\rho</math> is a root of the second characteristic equation of the
nilpotent number <math>\eta</math>. Hence <math>\rho = 0</math>. Given any <math>\eta</math> in <math>N</math>, we can therefore
find a linear combination <math>u \neq 0</math> of <math>u_1, ..., u_n</math> such that <math>u\eta = 0</math>.
Apply this result to <math>\eta = e_1</math>. Hence there is a linear function <math>u \neq 0</math>
of <math>u_1, ..., u_n</math> for which <math>ue_1 = 0</math>. Some of the solutions <math>u</math> of the latter
may make <math>ue_2 = 0</math>, some also <math>ue_3 = 0</math>, etc. Hence there exists an integer
<math>m \leq k</math> such that
<math>ue_1 = 0, \quad ue_2 = 0, \dots, \quad ue_m = 0</math>
(70)
have a common solution <math>u</math> which is a linear function <math>\neq 0</math> of <math>u_1, ..., u_n</math>,

## PDF page 55

§ 38]
NILPOTENT ALGEBRAS
43
but no such solution making also <math>ue = 0</math>, where <math>e</math> is a number of <math>N</math>,
linearly independent of <math>e_1, ..., e_m</math>. By a change of notation of <math>u_1, ..., u_m</math>,
we may assume that <math>u_1, ..., u_{n'}</math> form a complete set of linearly inde-
pendent solutions of (70).
We shall assume that <math>m < k</math> and prove that a contradiction results.
For <math>i \leq m</math>, <math>u(e_i e_j) = 0</math> for every solution <math>u</math> of (70). Hence <math>e_i e_j</math> is a
linear function of <math>e_1, ..., e_m</math>, which are therefore the units of a sub-
algebra <math>N_1</math>, to which our theorem applies. If <math>\nu</math> is any number <math>\neq 0</math> of <math>N_1</math>
either v is a linear combination of <math>u_1, ..., u_{n'}</math> or there exists a number <math>\eta</math>
of <math>N_1</math> such that <math>v\eta</math> is a linear function <math>\neq 0</math> of <math>u_1, ..., u_{n'}</math>. For, if <math>i \leq m</math>,
<math>e_m e_i = 0</math>, <math>(\nu e_m) e_i = 0</math> and <math>\nu e_m</math> is a linear combination of <math>u_1, \ldots, u_n</math>. If
<math>ve_m \neq 0</math>, the italicized statement holds. If zero, <math>ve_{m-1}e_i = 0</math> <math>(i \leq m)</math>,
since <math>e_{m-1}e_i</math> is a multiple of <math>e_m</math>. Thus <math>ve_{m-1}</math> is a linear function of
<math>u_1, ..., u_{n'}</math>. Taking <math>u_1 e_{m+1}</math> as <math>\nu</math>, we obtain, as in the proof of the lemma,
a <math>\zeta_1</math> for which <math>u_1\zeta_1 = su_1</math>, thence <math>u_1\zeta_1 = u_2</math>, etc. We obtain (69) with
<math>u_i \zeta_i</math> in place of <math>\zeta_i u_i</math>, and then the contradiction <math>u_s l = \lambda_s u_s</math>. Hence
<math>m=k</math>, so that there exists a solution <math>u \neq 0</math> of (67) and (70), whence
<math>ut = tu = 0</math> for every number t in the algebra N.
This <math>u</math> is a sum of numbers <math>u'</math> of definite characters. If <math>\eta</math> is of
character <math>(a, \beta)</math>, <math>u\eta</math> is a sum of products <math>u'\eta</math> each zero or of a definite
character. Since <math>u\eta = 0</math>, each <math>u'\eta = 0</math>. Similarly, each <math>\eta u' = 0</math>.
We introduce as new linearly independent units <math>\eta_1, \eta_2, ..., \eta_k</math>, where
<math>\eta_k</math> is one of the <math>u'</math>, such that each <math>\eta</math> has a definite character. Then
<math>
\eta_i \eta_k = \eta_k \eta_i = 0 \qquad (i = 1, ..., k)
</math>
(71),
<math>
\eta_i \eta_j = \sum_{s=1}^k \gamma_{ijs} \eta_s
</math> <math>(i, j = 1, ..., k).</math>
Consider an algebra with the units <math>\zeta_1, \ldots, \zeta_{k-1}</math> such that
<math display="block">\zeta_i \zeta_j = \sum_{i=1}^{k-1} \gamma_{ijs} \zeta_s \qquad (i, j=1, ..., k-1).</math>
For <math>\lambda</math>, <math>\mu</math>, <math>\nu</math> all less than <math>k</math>, <math>(\zeta_{\lambda}\zeta_{\mu})\zeta_{\nu} = \zeta_{\lambda}(\zeta_{\mu}\zeta_{\nu})</math>. Indeed, <math>\eta_{\lambda}\eta_{\mu} = \eta' + c\eta_{k}</math>,
where <math>\eta'</math> is the same linear function of <math>\eta_1, ..., \eta_{k-1}</math> that <math>\zeta_{\lambda}\zeta_{\mu}</math> is of
<math>\zeta_1, \ldots, \zeta_{k-1}</math>. But <math>(\eta_{\lambda}\eta_{\mu}) \eta_{\nu} = \eta' \eta_{\nu}</math>, so that its part free of <math>\eta_k</math> is the same
function of <math>\eta_1, ..., \eta_{k-1}</math> that <math>(\zeta_{\lambda}\zeta_{\mu})\zeta_{\nu}</math> is of <math>\zeta_1, ..., \zeta_{k-1}</math>. Similarly, the
part of <math>\eta_{\lambda}(\eta_{\mu}\eta_{\nu})</math> free of <math>\eta_{k}</math> is the same function of <math>\eta_{1},...,\eta_{k-1}</math> that
<math>\zeta_{\lambda}(\zeta_{\mu}\zeta_{\nu})</math> is of <math>\zeta_1, ..., \zeta_{k-1}</math>. Since the products of the <math>\eta</math>'s are equal,
those of the &'s are. Hence the &'s are the units of a linear associative
algebra.
Since <math>\gamma_{iks} = 0</math> <math>(i, s = 1, ..., k)</math> by <math>(71_1)</math>, the elements of the kth row

## PDF page 56

44
[(72)]
ALGEBRAS OF FIRST CATEGORY
of the characteristic determinant (40) of the <math>\eta</math>-algebra are <math>0, ..., 0, -\omega</math>.
Since <math>\gamma_{kjs} = 0</math> <math>(j, s = 1, ..., k)</math> by <math>(71_2)</math>, the minor of <math>-\omega</math> is the
characteristic determinant of the \zeta-algebra. Hence every number of
the latter is nilpotent. Since the theorem applies to this \(\xi\)-algebra,
we may suppose that new <math>\zeta</math>'s have been introduced such that, if <math>i, j, s</math>
are less than <math>k</math>, <math>\gamma_{ijs} = 0</math> unless <math>s > i</math>, <math>s > j</math>. As just noted, this result
holds also if <math>i = k</math> or <math>j = k</math>. Hence <math>\eta_1, \ldots, \eta_k</math> satisfy the requirements of
our theorem.
39. Normalized units of an algebra <math>A_1</math> of the first
category. In view of the last theorem, the result at the end of
§ 25, and the remark in § 36 on the units, we have the
Theorem*. If in the characteristic equation <math>\delta(\omega) = 0</math> for <math>A_1</math>, <math>\omega</math> is
an h-valued function of <math>x_1, ..., x_n</math>, we may choose as normalized units
<math>\epsilon_1, \ldots, \epsilon_h, \eta_1, \ldots, \eta_k, \text{ where each } \eta \text{ has a definite character}, \epsilon_i^2 = \epsilon_i,</math>
<math>\epsilon_i \epsilon_j = 0 \ (i \neq j), \ while \ \eta_a \ \eta_b \ is \ a \ linear function \ of \ those \ \eta's \ whose \ subscripts</math>
exceed a and b and have the same character as <math>\eta_a \eta_b</math>.
Conversely, any such algebra is of the first category.
To prove the converse, arrange the <math>n</math> units in the following order:
first <math>\epsilon_1</math>; then the units <math>\eta_i</math> of character <math>(1, 1), (2, 1), ..., (h, 1)</math> in
ascending order of their subscripts i; then <math>\epsilon_2</math> and the units <math>\eta_i</math> of
character <math>(1, 2), (2, 2), ..., (h, 2)</math> in the order of their subscripts <math>i</math>; etc.
Let <math>\zeta_1, ..., \zeta_n</math> be the units thus arranged. Let <math>n_{\alpha\beta}</math> be the number of
units <math>\eta</math> of character <math>(\alpha, \beta)</math> and set
<math display="block">n_{\beta}=1+n_{1\beta}+n_{2\beta}+\ldots+n_{h\beta}.</math>
The characteristic determinant of <math>z = z_1 \zeta_1 + ... + z_n \zeta_n</math> is (40):
<math>\delta\left(\omega
ight) \equiv egin{array}{cccc} \Sigma z_{i} \gamma_{i11} - \omega & \Sigma z_{i} \gamma_{i21} \dots \Sigma z_{i} \gamma_{in1} & & & & \\ & \dots & \dots & & & & \\ \Sigma z_{i} \gamma_{i1n} & \Sigma z_{i} \gamma_{i2n} \dots \Sigma z_{i} \gamma_{inn} - \omega & & & \\ \end{array}</math>
(72).
The elements which lie simultaneously in one of the first <math>n_1</math> rows and
last <math>n - n_1</math> columns are zero, since
<math>\gamma_{i\lambda\mu} = 0</math>  <math>(i = 1, ..., n; \lambda > n_1; \mu \leq n_1).</math>
Indeed, for such a set of subscripts, <math>\zeta_{\mu}</math> is of character (•1), <math>\zeta_{\lambda}</math> of
character <math>(\bullet\delta)</math>, <math>\delta > 1</math>, <math>\zeta_i \zeta_{\lambda}</math> is zero or of character <math>(\bullet\delta)</math>.
Hence in
<math display="block">\zeta_i \zeta_{\lambda} = \sum_{\mu=1}^{n} \gamma_{i\lambda\mu} \zeta_{\mu}</math>
(73),
* G. Scheffers, Math. Ann., vol. 39 (1891), p. 293. He took a definition of
algebras <math>A_1</math> different from the definition we have used following Cartan.

## PDF page 57

§ 39]
ALGEBRAS OF FIRST CATEGORY
45
<math>\zeta_{\mu}</math> (<math>\mu \leq n_1 < \lambda</math>) does not occur. Hence its coefficient is zero.
Thus
<math>\delta(\omega)</math> has as a factor the minor whose elements lie in the first <math>n_1</math> rows
and first <math>n_1</math> columns. Similarly, it has <math>n_2</math>-rowed, ..., <math>n_k</math>-rowed minors
as factors.
In the <math>n_1</math>-rowed minor all of the elements above the main diagonal
are zero, while the element in the <math>\lambda</math>th row and main diagonal is <math>x_t - \omega</math>,
where <math>(t, 1)</math> is the character of <math>\zeta_{\lambda}</math>. First, let <math>1 < \lambda \le n_1, 1 < \mu \le n_1</math>,
so that <math>\zeta_{\lambda}</math>, <math>\zeta_{\mu}</math> are <math>\gamma</math>'s. Then if <math>\zeta_{i}</math> is an <math>\eta</math>, <math>\gamma_{i\lambda\mu} = 0</math> if <math>\mu \leq \lambda</math>, by the
above theorem*. But if <math>\zeta_i = \epsilon_t</math> and <math>\zeta_\lambda</math> is of character <math>(a, 1)</math>, <math>\zeta_i \zeta_\lambda = 0</math> or
<math>\zeta_{\lambda}</math>, according as <math>\alpha \neq t</math>, <math>\alpha = t</math>, so that <math>\gamma_{i\lambda\mu} = 0</math> if <math>\mu \neq \lambda</math>, and <math>\gamma_{i\lambda\lambda} = 0</math> or 1,
according as <math>\alpha \neq t</math> or <math>\alpha = t</math>. Second, let <math>\mu = 1</math>, so that <math>\zeta_{\mu} = \epsilon_1</math>. There
is no <math>\epsilon_1</math> in the sum (73) if <math>\zeta_i</math> and <math>\zeta_{\lambda}</math> are both <math>\eta</math>'s. Next, let <math>\zeta_i = \epsilon_i</math>, so
that <math>\zeta_i \zeta_{\lambda} = 0</math> or <math>\zeta_{\lambda}</math>, according as <math>\zeta_{\lambda}</math> is not or is of character <math>(t \cdot)</math>; thus
<math>\epsilon_1</math> occurs in the sum (73) only when <math>\lambda = t = 1</math>. Since <math>\epsilon_1 \epsilon_1 = \epsilon_1</math>, <math>\gamma_{(1)} = 0</math>
<math>(i > 1), \gamma_{111} = 1</math>. Finally, if <math>\zeta_{\lambda} (\lambda \le n_1)</math> is an <math>\epsilon</math>, it is <math>\epsilon_1</math>, and the sum
(73) contains <math>\epsilon_1</math> only when it reduces to the preceding case <math>\epsilon_1 \epsilon_1 = \epsilon_1</math>.
Third, if <math>\lambda = 1</math>, <math>\gamma_{i\lambda\mu}</math> is below the main diagonal unless <math>\mu = 1</math>. Hence in
our minor, all elements above the main diagonal are zero and all in
the diagonal are zero except the <math>\gamma_{i\lambda\lambda}</math> for which <math>\zeta_i = \epsilon_i</math> and <math>\zeta_{\lambda}</math> is of
character <math>(t, 1)</math>, and these <math>\gamma</math>'s are unity. Hence if z be given the
former notation (66) we have the result at the beginning of this
paragraph. Thus the <math>n_1</math>-rowed minor equals
<math>(x_1-\omega) \prod_{i=1}^{h} (x_i-\omega)^{n_{i1}},</math>
the first factor coming from <math>\epsilon_1</math>. Similarly,
<math>(x_2 - \omega) \prod_{t=1}^{h} (x_t - \omega)^{n_{t/2}}</math>
is the value of the n2-rowed minor, etc. Set
<math>n_{t}' = 1 + n_{t1} + n_{t2} + \ldots + n_{th}</math>
Hence †
(74).
<math display="block">\delta\left(\omega\right) = (x_1 - \omega)^{n_1'} (x_2 - \omega)^{n_2'} \dots (x_h - \omega)^{n_{h'}}</math>
For example, if the units are <math>\epsilon_1</math>, <math>\eta_1</math>, <math>\epsilon_2</math>, <math>\eta_2</math>, where <math>\eta_1</math> is of character [1, 1],
<math>\eta_2</math> of character (1, 2), we have an associative algebra for which the character-
istic determinant of <math>x_1 \epsilon_1 + y_1 \eta_1 + x_2 \epsilon_2 + y_2 \eta_2</math> is
* The <math>\zeta_{\lambda}</math> and hence all of the units of the sum (73) are <math>\eta</math>'s of character (•1),
the relative order of which was not changed by our rearrangement of the units.
† The conclusions of Cartan (l. c., §§ 39, 40) are erroneous.

## PDF page 58

46
ALGEBRAS OF SECOND CATEGORY
<math display="block">\delta\left(\omega\right) = \left| \begin{array}{ccccc} x_1 - \omega & 0 & 0 & 0 \\ y_1 & x_1 - \omega & 0 & 0 \\ 0 & 0 & x_2 - \omega & 0 \\ 0 & 0 & y_2 & x_1 - \omega \end{array} \right| = (x_1 - \omega)^3 (x_2 - \omega).</math>
As a check, note that <math>n_1'=3</math>, <math>n_2'=1</math>, by inspection of the units.
Since the roots are linear functions of the x's, the algebra is of the
first category. Since <math>x_1, ..., x_h</math> are independent variables and since
<math>\delta(\omega)</math> is a covariant (§§ 16, 17), we conclude that <math>n_1', ..., n_h'</math> are unaltered
by a linear transformation of units which replaces algebra <math>A_1</math> by one
with normalized units*. By using the order <math>(1, 1), (1, 2), ..., (1, h)</math>;
<math>(2,1), \ldots, (2,h), \ldots</math>, we see that the exponents <math>n_1, \ldots, n_h</math> in <math>\delta'(\omega)</math> are
unaltered by transformation.
Moreover, each <math>n_{\alpha\beta}</math> has the last property (see Cartan, l.c., p. 36).
There is an extensive list of papers relating to the determination
and classification of algebras of the first category (Encyc. Sc. Math.,
vol. I, 1, p. 425).
ALGEBRAS A2 OF THE SECOND CATEGORY.
Properties of the characteristic determinant for A2.
40.
We shall employ the normalized units <math>\epsilon_i</math>, <math>\eta_g</math> of § 32. A linear com-
bination of the nilpotent units <math>\eta_1, ..., \eta_k</math> need not be nilpotent.
Arrange the units in the order <math>\zeta_1, ..., \zeta_n</math> as in § 39. The first
property of determinant (72) holds also here: <math>\delta = \delta_1 \delta_2 \dots \delta_h</math>, where <math>\delta_1</math>
is the minor composed of the elements in the first <math>n_1</math> rows and columns
of <math>\delta</math>, etc.
In (73) set <math>i = 1</math>, <math>\lambda \leq n_1</math>. Then <math>\zeta_{\lambda}</math> is of character (•1). Since <math>\zeta_1</math> is
the partial modulus <math>\epsilon_1</math>, we have <math>\zeta_1 \zeta_{\lambda} = 0</math> or <math>\zeta_{\lambda}</math> according as the character
of <math>\zeta_{\lambda}</math> is <math>(\alpha, 1)</math>, <math>\alpha > 1</math> or <math>(1, 1)</math>. Hence <math>\gamma_{1\lambda\mu} = 0</math> unless <math>\mu = \lambda</math> and <math>\zeta_{\lambda}</math> is
of character <math>(1, 1)</math>. Thus <math>z_1</math> occurs only in the main diagonal of <math>\delta_1</math>
and there only in the first <math>n_{11} + 1</math> terms (with coefficient unity). Simi-
larly, <math>z_{n_1+1}</math>, the coefficient of <math>\epsilon_2</math>, occurs only in the main diagonal and
* But under the transformation each <math>\epsilon_i</math> may be increased by a properly chosen
nilpotent number. For example, if <math>h=2</math>, <math>k=1</math>, and <math>\eta_1=\eta</math> is of character <math>(1,2)</math>,
the multiplication table is
<math>\epsilon_1^2 = \epsilon_1, \quad \epsilon_2^2 = \epsilon_2, \quad \epsilon_1 \epsilon_2 = \epsilon_2 \epsilon_1 = \epsilon_2 \eta = \eta \epsilon_1 = 0, \quad \eta \epsilon_2 = \eta, \quad \epsilon_1 \eta = \eta, \quad \eta^2 = 0.</math>
This is unaltered if we replace <math>\epsilon_1</math> by <math>\epsilon_1' = \epsilon_1 + \eta</math>, <math>\epsilon_2</math> by <math>\epsilon_2' = \epsilon_2 - \eta</math>.
Various writers have overlooked this possibility (see end of § 61).

## PDF page 59

§ 40]
ALGEBRAS OF SECOND CATEGORY
47
there only in <math>n_{21}</math> terms (with coefficient unity), etc. Using the second
notation (66) for z, we see that <math>x_1, x_2, ..., x_h</math> occur only in the main
diagonal of δ1 and that each element of the diagonal contains one and
but one of these x's (with coefficient unity). Thus every element of
<math>\delta_1</math> is linear and homogeneous in
<math>x_1' = x_1 - \omega, \ldots, x_h' = x_h - \omega, y_1, \ldots, y_k</math>
(75).
Hence <math>\delta_1</math> is homogeneous in <math>x_1', ..., y_k</math>.
For brevity we shall say that <math>y_i</math> is of the same character as <math>\eta_i</math> and
<math>x_i'</math> of character <math>(i, i)</math>. If, in (73), <math>\zeta_i</math> is of character <math>(a \cdot)</math> then <math>\gamma = 0</math>
unless <math>\zeta_{\mu}</math> is of character (a•). Conversely, if <math>\zeta_{\mu}</math> is of character (a•)
then <math>\gamma = 0</math> unless <math>\zeta_i</math> is of character (a.). Hence the variables <math>z_i</math> of
character <math>(a \cdot)</math> enter the same rows of the determinant <math>\delta_1</math>. Hence <math>\delta_1</math> is
homogeneous and of degree <math>n_{a1}</math> or <math>n_{a1} + 1</math> in the <math>z_i</math> of character (a•),
according as <math>\alpha > 1</math> or <math>\alpha = 1</math>.
Similarly <math>\delta_1</math> is homogeneous and of degree <math>n_{a1}</math> or <math>n_{a1} + 1</math> in the
variables of character (<math>\bullet a</math>), according as <math>a > 1</math> or <math>a = 1</math>.
Let <math>\delta(\omega) = P_1^{a_1} \dots P_l^{a_l}</math>, where <math>P_1, \dots, P_l</math> are distinct irreducible
functions of their arguments (75), the degree of <math>P_i</math> in <math>\omega</math> being <math>d_i</math>.
Then <math>d_1 + \ldots + d_l = h</math>, if <math>\delta(\omega) = 0</math> defines <math>\omega</math> as an h-valued function of
the x's and y's. For <math>y_1 = 0, ..., y_k = 0</math>, we saw that <math>\delta(\omega)</math> reduces to the
product (74) of its diagonal elements. Thus <math>P_i</math> reduces to a product
of <math>d_i</math> factors <math>x_i - \omega</math>. The resulting <math>\Sigma d_i</math> linear factors are <math>x_i - \omega</math>, ...,
<math>x_h - \omega</math> in some order. Hence no one appears twice in the same <math>P_i</math> or
appears in different <math>P</math>'s. We may thus set
<math>(P_1)_{y=0} = (x_1 - \omega) \dots (x_p - \omega) \equiv x_1' \dots x_p'</math>
(76).
The factor <math>\delta_1</math> of <math>\delta</math> is homogeneous in the variables of character (a•).
Hence each irreducible factor <math>P_1</math> of <math>\delta_1</math> is homogeneous in these variables.
To find its degree in them, it suffices to examine one term (76), which
is linear and homogeneous in the variables of character (a.). We have
therefore the
The irreducible factor <math>P_1</math> of the determinant <math>\delta_1</math> is linear
THEOREM.
and homogeneous in those of its arguments (75) whose characters are (1.),
linear and homogeneous in those of characters (2.), ..., and in those of
characters <math>(p \bullet)</math>; likewise for the variables of characters <math>(\bullet 1)</math>, ..., and for
No further variables occur in P1.
<math>(\bullet p).</math>
<b>Example.</b> In the matric algebra of four units <math>e_{ij}</math> of § 4, <math>e_{ij}</math> is of
41.
character (i, j). The characteristic determinant of
<math>x_{11}e_{11} + x_{12}e_{12} + x_{21}e_{21} + x_{22}e_{22}</math>

## PDF page 60

48
[(77)]
ALGEBRAS OF SECOND CATEGORY
is, by § 35, the square of
<math>\delta_1 = \begin{vmatrix} x_{11}' & x_{12} \\ x_{21} & x_{22}' \end{vmatrix}, \quad x_{11}' = x_{11} - \omega, \quad x_{22}' = x_{22} - \omega.</math>
Hence <math>P_1 = \delta_1</math> is linear and homogeneous in <math>x_{11}</math> and <math>x_{12}</math> of characters (1•), also
in <math>x_{21}</math> and <math>x_{22}</math> of characters <math>(2\bullet)</math>; also in <math>x_{11}</math> and <math>x_{21}</math> of characters <math>(\bullet 1)</math>; and
in <math>x_{12}</math>, <math>x_{22}</math> of characters (•2).
<b>42.</b> Sub-algebras <math>S_i</math> of <math>A_2</math>. To obtain <math>P_1</math> we need consider
only numbers involving the units of characters <math>(a, \beta)</math>, <math>a, \beta = 1, ..., p</math>.
These are the units of a sub-algebra <math>S_1</math>.
By the argument leading to (76), we may set
<math>(P_2)_{y=0} = x'_{p+1} x'_{p+2} \dots x'_q.</math>
To obtain <math>P_2</math> we need consider only numbers involving the units of
characters <math>(a, \beta)</math>, <math>a, \beta = p+1, ..., q</math>; these are the units of a sub-algebra
<math>S_2</math>, etc. The product of a number of <math>S_1</math> by one of <math>S_2</math> is zero, and vice
versa. In the characteristic determinant of the reducible (§ 21) algebra
<math>S_1 + S_2</math>, the elements in the first and third "quadrants" are all zero,
so that it equals the product of the characteristic determinants of <math>S_1</math>
and <math>S_2</math>. Similarly, for <math>S_1 + S_2 + ... + S_l</math>. Thus <math>\delta(\omega)</math> is unaltered when
we replace by zero each variable not corresponding to a unit of <math>S_1</math>,
<math>S_2, ...,</math> or <math>S_l</math>. Hence the characteristic determinant of <math>S_i</math> is <math>P_i^{a_i}</math>.
For the moment, let <math>[\alpha, \beta]</math> denote a variable (75) of character
<math>(\alpha, \beta)</math>. Let <math>P_1</math> be the irreducible factor of degree <math>p > 1</math> of <math>\delta(\omega)</math>, with
the properties given in the theorem of § 40. It involves a variable
of character <math>(\alpha, \beta)</math>, <math>\alpha \neq \beta</math>. Otherwise, a power of <math>P_1</math> would be the
characteristic determinant of a number of algebra <math>S_1</math> having each
<math>[\alpha, \beta] = 0, \ \alpha \neq \beta, \ \text{and hence of the direct sum of the algebras } \Sigma_1, \ldots, \Sigma_p</math>
of numbers of characters <math>(1, 1), ..., (p, p)</math>, respectively. But (§ 42),
<math>P_1</math> would then be a product of a function of the variables [1, 1], by a
function of the [2, 2], etc., and hence a product of linear functions,
whereas it is irreducible and of degree > 1.
By choice of the notation, we may assume that <math>P_1</math> has a term with
the factor [1, 2] and hence a factor [2, j], <math>j \neq 2</math>, which we may take to
be [2, 1] or [2, 3]; in the latter case, a factor [3, 1] or [3, 4], etc.
Thus <math>P_1</math> has a term
<math>[1, 2][2, 3] \dots [a-1, a][a, 1] \bullet [a+1, a+2] \dots [\beta, a+1] \dots \prod_{i=\gamma+1}^{p} [i, i]</math>
(77),
in which <math>[i, i]</math> for <math>i = \lambda + 1, ..., p</math> are variables <math>x_i' = x_i - \omega</math>, while the
remaining <math>[i, i]</math> are variables <math>y_i</math>. Set <math>x_1 = 0, ..., x_p = 0</math>. Then (77)

## PDF page 61

§ 42]
ALGEBRAS OF SECOND CATEGORY
49
becomes a multiple of <math>\omega^{p-\lambda}</math>, while the term (76) of <math>P_1</math> reduces to <math>\pm \omega^p</math>.
Hence algebra S<sub>1</sub> contains a number whose characteristic equation has
a root <math>\neq 0</math>, the number being a sum of numbers of characters
<math>(1, 2), (2, 3), \ldots, (a, 1), (a + 1, a + 2), \ldots, (\beta, a + 1), (i, i)</math>
<math display="block">(i = \gamma + 1, \ldots, \lambda) \tag{78},</math>
those of character (i, i) being nilpotent.
43.
Preliminary criterion for an algebra A, of the
second category. A necessary and sufficient condition that an
algebra be of the second category is that it contain a number
<math display="block">u = (e_{12} + e_{23} + \ldots + e_{\alpha-1\alpha} + e_{\alpha1}) + (e_{\alpha+1\alpha+2} + \ldots + e_{\beta\alpha+1}) + \ldots + \sum_{i=\alpha+1}^{n} \eta_{ii},</math>
whose characteristic equation has a root not zero, where the <math>e_0</math> and <math>\eta_0</math>
are linear functions of nilpotent units <math>\eta_1, ..., \eta_k</math> of characters <math>(i, j)</math> and
<math>(i, i)</math>, respectively, and where one of the integers <math>a, \beta - a, ..., \lambda - \gamma</math> is
positive.
The condition is necessary by § 42, and sufficient by § 36 [see § 47].
Since <math>u</math> is not nilpotent, there is a number <math>v \neq 0</math> such that
44.
<math>uv = \omega v</math>, <math>\omega</math> a scalar <math>\neq 0</math>. Take <math>u/\omega</math> as a new <math>u</math>. Then <math>uv = v</math>. Hence
if <math>v</math> be expressed as a sum of numbers each of a definite character
<math>(r, s)</math>, then <math>r \leq \lambda</math>. Let <math>v_{\gamma+1}</math> be the sum of the parts of <math>v</math> of character
<math>(\gamma + 1 \bullet)</math>. Then
<math>uv_{y+1} = \eta_{y+1,y+1}v_{y+1} = v_{y+1} = 0</math>
since the <math>\eta</math> is nilpotent. Hence each term <math>\neq 0</math> of <math>v</math> is of character
<math>(r, s), r \leq \gamma</math>. After a change of notation of the cycles of u, we may
assume that <math>v</math> has a term <math>\neq 0</math> of character <math>(1 \cdot)</math>. Call <math>v'</math> the number
<math>\pm 0</math> which is the sum of the terms of v of characters <math>(1 \bullet) \dots, (a \bullet)</math>.
Set <math>u' = e_{12} + e_{23} + \ldots + e_{a_1}</math>. Then <math>u'v' = v'</math>. Drop the accents. We may
therefore assume that initially
<math>u = e_{12} + e_{23} + \ldots + e_{a1}, \quad uv = v,</math>
<math>v = \sum_{i=1}^{n} (v_{1i} + v_{2i} + \ldots + v_{ai}) \neq 0,</math>
where <math>v_{ai}</math> is zero or of character <math>(a, i)</math>. By <math>uv = v</math>,
<math>e_{12}v_{2i}=v_{1i}, \quad e_{23}v_{3i}=v_{2i}, \ldots, \quad e_{a1}v_{1i}=v_{ai}.</math>
4
D.

## PDF page 62

50
[(79)]
ALGEBRAS OF SECOND CATEGORY
Let i have a fixed value for which one of the <math>v_{1i}, ..., v_{\alpha i}</math> is <math>\neq 0</math> and
hence all are <math>\neq 0</math>. It follows at once that
<math>e_{12} e_{23} \dots e_{a-1a} e_{a1} v_{1i} = v_{1i},</math>
<math>e_{23} e_{34} \dots e_{a1} \qquad e_{12} \qquad v_{2i} = v_{2i},</math>
. . . . . . . . . . . . . . . . . . . . 
<math>e_{a_1}e_{12}\ldots e_{a-2a-1}e_{a-1a}v_{ai}=v_{ai}</math>.
The product of the e's in the first of these equations has unity as a
root of its characteristic equation and is of character (1, 1); hence
(§ 31) it equals <math>a\epsilon_1 + \zeta_1</math>, where a is a scalar and <math>\zeta_1</math> is nilpotent, the
characteristic determinant of <math>a\epsilon_1 + \zeta_1</math> being a power of <math>a - \omega</math>. Thus
<math>a=1</math>,
<math>e_{12} e_{23} \dots e_{a-1a} e_{a1} = \epsilon_1 + \zeta_1,</math>
<math>e_{\mathbf{a}_1}e_{12}\dots e_{\mathbf{a}-2\mathbf{a}-1}e_{\mathbf{a}-1\mathbf{a}}=\epsilon_{\mathbf{a}}+\zeta_{\mathbf{a}},</math>
<math>\zeta_i</math> being nilpotent and of character <math>(i, i)</math>.
<b>Notation.</b> Set <math>e_{13} = e_{12}e_{23}</math>, <math>e_{\alpha 2} = e_{\alpha 1}e_{12}</math>, and, in general,
45.
<math>e_{ij} = e_{i\,i+1}e_{i+1\,i+2}\dots e_{i-2\,j-1}e_{i-1\,i} \qquad (i \neq j)</math> (79),
where <math>e_{aa+1}</math> is to be replaced by <math>e_{a1}</math>. The last equations in § 44 become
<math>e_{ji}e_{ij}=\epsilon_j+\zeta_j</math> <math>(i,j=1,\ldots,\alpha;\ i\neq j)</math> (80).
If <math>\eta</math> is a number <math>\neq 0</math> of character <math>(j, \lambda)</math>, then <math>e_{ij}\eta \neq 0</math>. For, if zero,
<math display="block">0 = e_{ii}e_{ij}\eta = \eta + \zeta_i\eta,</math>
whereas <math>-1</math> is not a root of the characteristic equation of the nilpotent
number <math>\zeta_j</math>. Let <math>n_1, ..., n_t</math> be a complete set of linearly independent
numbers of character <math>(j, \lambda)</math>. Then <math>e_{ij}n_1, ..., e_{ij}n_t</math> are linearly inde-
pendent numbers of character <math>(i, \lambda)</math>. For, if <math>\Sigma c_s e_{ij} n_s = 0</math>, then <math>e_{ij} \eta = 0</math>
when <math>\eta = \sum c_s n_s</math>. If the resulting <math>e_{ij} n_s</math> did not form a complete set, the
<math>n_s</math> would not. Hence a complete set of linearly independent numbers
of character <math>(i, \lambda)</math> is obtained from a complete set of character <math>(j, \lambda)</math> by
multiplying ei by the latter.
It may be proved in the same manner that there are as many
linearly independent numbers of character <math>(\lambda, i)</math> as of character <math>(\lambda, j)</math>,
and the latter are given by the products of the former by <math>e_{ij}</math>.
In these theorems, <math>i, j = 1, ..., \alpha</math>; <math>\lambda = 1, ..., h</math>.
<b>46.</b> In particular, if <math>n_1, ..., n_t</math> form a complete set of linearly in-
dependent numbers of character <math>(a, 1)</math>, where <math>a > 1</math>, then <math>e_{1a}n_1, \ldots,</math>
<math>e_{1a}n_t</math> form a complete set of character (1, 1). Hence for suitably

## PDF page 63

§ 46]
ALGEBRAS OF SECOND CATEGORY
51
chosen scalars <math>c_s</math>, <math>\Sigma c_s n_s</math> is a number <math>e_{a1}</math> of character <math>(a, 1)</math> such that
<math>e_{1a}e_{a1}'=\epsilon_1</math>, a number of character (1, 1). Expressed otherwise, by
means of (79),
<math>e_{1i}\beta = \epsilon_1, \ e_{1i} = e_{12}e_{23} \dots e_{i-1i}, \ \beta = e_{ii+1} \dots e_{a-1a}e_{ai}'</math>
Since <math>e_{ii}</math> and <math>\beta</math> are of characters <math>(1, i)</math> and <math>(i, 1)</math>, respectively,
<math>\beta e_{1i} = \alpha \epsilon_i + \zeta_i'</math>
where a is scalar and <math>\zeta_i</math> is nilpotent of character <math>(i, i)</math>. Multiplying
this on the left by <math>e_{1i}</math> and applying (79), we get
<math>e_{1a}e_{a1}'e_{1i} \equiv e_{1i} = \alpha e_{1i} + e_{1i}\zeta_{i}'</math>
Thus, by (56), <math>1-a</math> is a root of the left-hand characteristic equation
of the nilpotent number <math>\zeta_i</math>. Hence <math>a=1</math>, <math>e_{1i}\zeta_i'=0</math>. This contradicts
the statement after (80), unless <math>\xi_i' = 0</math>. In <math>\beta e_{ii} = \epsilon_i</math>, we drop the accent
on <math>e_{a_i}</math> and write <math>e_{ii}</math> for <math>\epsilon_i</math>. Thus
<math>e_{ii+1}e_{i+1\,i+2}\ldots e_{\alpha-1\alpha}e_{\alpha 1}e_{12}\ldots e_{i-1i}=e_{ii} \quad (i=1,\ldots,\alpha).</math>
Define <math>e_{ij}</math> by (79). Then we get
(80').
<math>e_{ji}e_{ij}=e_{jj},\ e_{ji}e_{il}=e_{jl}</math>
Hence we have <math>a^2</math> linearly independent numbers <math>e_{ij}(i, j = 1, ..., a)</math> of
character <math>(i, j)</math>, which have the same multiplication table <math>(14)</math> as the
matric algebra of <math>\alpha^2</math> units.
THEOREM. Any algebra of the second category contains a sub-
algebra equivalent to the matric algebra of <math>a^2</math> units, <math>a > 1</math>.
The matric algebra of <math>\alpha^2</math> units <math>e_{ij}</math> has as a sub-algebra the matric
algebra of the <math>\beta^2</math> units <math>e_{ij}(i, j = 1, ..., \beta)</math>, if <math>\beta < a</math>. By § 13, we have
the
COROLLARY. Any algebra of the second category contains an algebra
equivalent to the algebra of complex quaternions.
Normalized units of an algebra A, of the second
47.
category.
For brevity we shall say that there is a path joining <math>a</math> and <math>\beta</math>, where
<math>\alpha</math> and <math>\beta</math> are distinct positive integers <math>\leq h</math>, if there is a number <math>\eta_{\alpha\beta}</math> of
character <math>(\alpha, \beta)</math> and a number <math>\eta_{\beta\alpha}</math> of character <math>(\beta, \alpha)</math> such that
<math>\eta_{\alpha\beta} + \eta_{\beta\alpha}</math> is not nilpotent. The existence of a path is a necessary and
sufficient condition that an algebra be of the second category. It is
sufficient by § 36 and necessary since there is a path joining 1 and 2 in
view of
<math>(e_{12} + e_{21})(e_{11} + e_{21}) = e_{11} + e_{21}.</math>
4-2

## PDF page 64

52
[(81)]
ALGEBRAS OF SECOND CATEGORY
After rearranging the subscripts <math>1, ..., h</math>, we may assume that they
fall into sets <math>(1, 2, ..., p)</math>, <math>(p + 1, ..., q)</math>, ..., such that there is no path
joining a number of one set with a number of another set, but that
any two given numbers, as 1 and 2, of the same set may be joined by
a path; or else other numbers, as 3 and 4, of that set may be found
such that there exist paths as 13, 34, 42, securing passage from the
first to the second given numbers 1, 2. To secure such passage between
any two points, 1, 2, ..., p, evidently <math>p-1</math> paths are necessary and
They need not form a single broken line, as was assumed
sufficient.
by Cartan (l.c., p. 48), who did not employ the suggestive terminology
For <math>p = 5</math>, the possible figures (trees of Cayley) are as
of paths.
follows:
In any case we may assume that there are paths joining 1 with 2
and 2 with 3, and hence numbers <math>\eta_{12} + \eta_{21}</math> and <math>\eta_{23} + \eta_{32}</math> neither nilpotent.
Calling the first u, we can find a number <math>v \neq 0</math> such that <math>uv = v \neq 0</math>,
where <math>v</math> is necessarily a sum of numbers of characters <math>(1 \cdot)</math>, <math>(2 \cdot)</math>. Pro-
ceeding as in <math>\S</math> 44-46, with <math>\alpha = 2</math>, and making a transformation of
units (§ 46) which alters at most those of characters (1, 2) and (2, 1),
we obtain units <math>e_{12}</math> and <math>e_{21}</math> of those characters such that
<math>e_{12}e_{21} = e_{11}, \ e_{21}e_{12} = e_{22} \ (e_{ii} \text{ partial moduli})</math>
(81).
Hence this normalization is not disturbed in treating <math>\eta_{23} + \eta_{32}</math> similarly.
Hence we may set also
(82).
<math>e_{23}e_{32}=e_{22},\ e_{32}e_{23}=e_{33}</math>
If the paths form a single broken line, we get similarly
(83).
<math>e_{34}e_{43}=e_{33}, e_{43}e_{34}=e_{44}, \ldots, e_{pp-1}e_{p-1p}=e_{pp}</math>
To secure passage from 1 to 3 we must use the paths 1, 2 and 2, 3 and
accordingly we set <math>e_{13} = e_{12}e_{23}</math>, <math>e_{31} = e_{32}e_{21}</math>. In general, we set
<math>e_{i\,i+j} = e_{i\,i+1}\,e_{i+1\,i+2}\dots e_{i+j-1\,i+j}, \ e_{i+j\,i} = e_{i+j\,i+j-1}\dots e_{i+1\,i}.</math>
It is easily seen that the <math>p^2</math> numbers <math>e_{ij}</math> are the units of a matric
algebra (14).
The same result follows if the paths are distributed in any other
manner; we have only to define <math>e_{ij}</math> to be the product of the e's whose
pairs of subscripts give the uniquely determined series of paths

## PDF page 65

§ 47]
ALGEBRAS OF SECOND CATEGORY
53
securing passage from <math>i</math> to <math>j</math>. For example, if <math>p = 4</math>, and if the paths
radiate from 2 to 1, 3, 4, respectively, we have (81), (82), and
<math>e_{24}e_{42} = e_{22}, \ e_{42}e_{24} = e_{44}</math>
(84),
and define the remaining e's by
<math>e_{13} = e_{12}e_{23}, \ e_{31} = e_{32}e_{21}, \ e_{14} = e_{12}e_{24},</math>
<math>e_{41} = e_{42} e_{21}, \ e_{34} = e_{82} e_{24}, \ e_{43} = e_{42} e_{23},</math>
so that <math>e_{ij}</math> is of character <math>(i, j)</math> and relations <math>(14)</math> follow.
The theorems of § 45 still hold, with now <math>i, j = 1, ..., p</math>.
Let <math>\eta_{11}^{(\rho)}(\rho=0, 1, 2, ...)</math> denote the units of character <math>(1, 1)</math>, where
<math>\eta_{11}^{(0)} = e_{11}</math>. Then all the units of character <math>(i, j)</math>, <math>i \leq p, j \leq p</math>, are given
by
<math>\eta_{ij}^{(\rho)} \equiv e_{i1} \eta_{11}^{(\rho)} e_{11}</math>
Similarly, if <math>\lambda</math> is a fixed integer <math>> p</math>, and <math>\eta_{1\lambda}^{(\sigma)}(\sigma = 1, 2, ...)</math> are the
units of character <math>(1, \lambda)</math>, those of character <math>(i, \lambda)</math> are
<math>\eta_{i\lambda}^{(\sigma)} \equiv e_{i1} \eta_{1\lambda}^{(\sigma)} \quad (\sigma = 1, 2, \ldots).</math>
We may set
<math display="block">\eta_{11}^{(\rho)}\eta_{11}^{(\sigma)} = \sum_{\sigma} \alpha_{\rho\sigma\tau} \eta_{11}^{(\tau)}, \ \eta_{11}^{(\rho)}\eta_{1\lambda}^{(\sigma)} = \sum_{\sigma} \beta_{\rho\sigma\tau} \eta_{1\lambda}^{(\tau)}</math>
(85).
Then
<math display="block">\eta_{ij}^{(\rho)}\eta_{ji}^{(\sigma)} = \sum_{\sigma\rho\sigma\tau}\eta_{ii}^{(\tau)}, \quad \eta_{ij}^{(\rho)}\eta_{j\lambda}^{(\sigma)} = \sum_{\sigma}\beta_{\rho\sigma\tau}\eta_{i\lambda}^{(\tau)}.</math>
For example, the second product equals
<math display="block">e_{i1}\,\eta_{11}^{(\rho)}e_{1j}\,.\,e_{j1}\,\eta_{1\lambda}^{(\sigma)}=e_{i1}\,\eta_{11}^{(\rho)}\,\eta_{1\lambda}^{(\sigma)}=\Sigma\,\beta_{\rho\sigma\tau}\,e_{i1}\,\eta_{1\lambda}^{(\tau)}.</math>
Similarly, <math>\eta_{\lambda i}^{(\rho)} \eta_{ij}^{(\sigma)}</math> is a linear function of the <math>\eta_{\lambda j}^{(\tau)}</math> whose coefficients
are independent of i, j. Hence, if we are given the multiplication
table (85), etc., of the sub-algebra <math>A_1</math> composed of the units of
characters
<math>(1, 1), (1, p+1), (1, q+1), ..., (p+1, 1), (p+1, p+1), ...</math>
we can deduce the multiplication table of the main algebra A<sub>2</sub>.
In view of the definition of the sets <math>(1, 2, ..., p), ...,</math>
<math>\eta_{1p+1} + \eta_{p+11}, \ldots</math>
are nilpotent, so that the sub-algebra <math>A_1</math> is of the first category.
We therefore have a simple process to derive all algebras of the
second category from those of the first.
Let <math>E_1, ..., E_H, H_1, ..., H_K</math> be normalized units (§ 39) of <math>A_1</math>:
<math>E_i^2 = E_i, E_i H_\rho = H_\rho E_j = H_\rho, H_\rho H_\sigma = \Sigma_{\gamma\rho\sigma\tau} H_\tau</math>
(86),

## PDF page 66

54
[(87)]
ALGEBRAS OF SECOND CATEGORY
where <math>H_{\rho}</math> is of character <math>(i, j), H_{\sigma}</math> of character <math>(j, l)</math>, and each <math>H_{\tau}</math> of
character <math>(i, l)</math>, and <math>\tau > \rho</math>, <math>\tau > \sigma</math>. As normalized units* of the algebra
<math>A_2</math> of the second category we take sets of <math>p_i^2</math> units <math>e_{\alpha\beta}^{(i)}(\alpha, \beta = 1, ..., p_i)</math>
corresponding to the partial moduli <math>E_i</math>, and sets of <math>p_i p_j</math> units <math>\eta_{\alpha\beta}^{(\rho)}</math>
<math>(a = 1, ..., p_i; \beta = 1, ..., p_j)</math> corresponding to <math>H_{\rho}</math> of character <math>(i, j)</math>. If
<math>N_{ij}</math> is the number of <math>H_{\rho}</math> of character <math>(i, j)</math>, these
<math display="block">n = \sum_{i=1}^{H} p_i^2 + \sum_{i=1}^{I} N_{ij} p_i p_j</math>
normalized units of A2 have the multiplication table
<math>(a, \beta, \gamma = 1, ..., p_i)</math> (87),
<math>e_{\alpha\beta}^{(i)}e_{\beta\gamma}^{(i)}=e_{\alpha\gamma}^{(i)}</math>
<math display="block">e_{\alpha\beta}{}^{(i)}\eta_{\beta\gamma}{}^{(\rho)} = \eta_{\alpha\gamma}{}^{(\rho)}, \ \eta_{\beta\gamma}{}^{(\rho)}e_{\gamma\delta}{}^{(j)} = \eta_{\beta\delta}{}^{(\rho)} \qquad (a, \ \beta \leq p_i \ ; \ \gamma, \ \delta \leq p_j) \quad (88),</math>
<math>
\eta_{\alpha\beta}^{(\rho)}\eta_{\beta\gamma}^{(\sigma)} = \sum_{\tau} \gamma_{\rho\sigma\tau}\eta_{\alpha\gamma}^{(\tau)} \qquad (\alpha \leq p_i, \ \beta \leq p_j, \ \gamma \leq p_l, \ \tau > \rho, \ \tau > \sigma) \quad (89),
</math>
corresponding to the three types (86). All products not written are
zero †.
For a simplified statement of part of the content of this theorem,
see § 50.
48.
Characteristic determinant <math>\delta</math> of an algebra <math>A_2</math>.
Let the units <math>E</math>, <math>H</math> of the sub-algebra (86) be arranged as in § 39 so
that in its characteristic determinant <math>\delta_1</math> every element above the main
diagonal is zero. The corresponding sets of units of <math>A_2</math> are arranged
in this order, while the units in the set corresponding to <math>H_{\rho}</math> of
character <math>(i, j)</math> are arranged in the order
<math>\eta_{11}^{\rho}</math>, <math>\eta_{21}^{\rho}</math>, ..., <math>\eta_{p_{i}1}^{\rho}</math>, <math>\eta_{12}^{\rho}</math>, ..., <math>\eta_{p_{i}2}^{\rho}</math>, <math>\eta_{13}^{\rho}</math>, ..., <math>\eta_{p_{i}p_{i}}^{\rho}</math>,
and the subscripts of the <math>e_{\alpha\beta}^{(i)}</math> corresponding to <math>E_i</math> are arranged
similarly.
Consider the element in the rth row and cth column of <math>\delta_1</math>. Let
<math>(i, j)</math> be the character of the rth unit of the sub-algebra, and <math>(l, t)</math> that
of the cth unit. Then the matrix of <math>\delta</math> is obtained from that of <math>\delta_1</math> by
replacing the element in the rth row and cth column by a rectangular
array of <math>p_i p_j</math> lines and <math>p_i p_t</math> columns. Since <math>\delta_i</math> is the product of its
* As in § 22, we may express the theorem as follows: Any A2 can be deduced
from an <math>A_1</math>, given by (86), by regarding the coefficient of <math>E_i</math> to be a square matrix
of <math>p_i^2</math> elements and that of <math>H_\rho</math>, of character <math>(i, j)</math>, to be a rectangular matrix of
p<sub>i</sub> rows and p<sub>j</sub> columns, these matrices to be regarded as commutative with each
<math>E</math> and <math>H</math>.
+ Molien, Math. Ann., vol. 41 (1893), p. 83, by use of group theory; Cartan,
<math>l. c.</math>, as in the text.

## PDF page 67

§ 48]
SIMPLE AND SEMI-SIMPLE ALGEBRAS
55
diagonal elements, δ equals the product of the determinants of the
diagonal arrays, obtained by setting <math>c = r</math>, the rth being a <math>p_i p_r</math> rowed
determinant. The latter is schematically
<math display="block"> \begin{vmatrix} M_{i} & O \dots & O \\ O & M_{i} \dots & O \\ \dots & \dots & \dots \\ O & O & \dots M_{i} \end{vmatrix}, M_{i} \equiv \begin{pmatrix} x_{11}^{(i)} - \omega & x_{12}^{(i)} & \dots & x_{1p_{i}}^{(i)} \\ x_{21}^{(i)} & x_{22}^{(i)} - \omega & \dots & x_{2p_{i}}^{(i)} \\ \dots & \dots & \dots & \dots \\ x_{p,1}^{(</math>
where <math>O</math> is a <math>p_{\bar{i}}</math>-rowed square matrix all of whose elements are zero.
The schematic determinant is <math>p_j</math>-rowed, and hence equals <math>|M_i|^{p_j}</math>. Thus,
since there is a single unit <math>E_i</math> of character <math>(i, i)</math>,
<math display="block">\delta = \prod_{i=1}^{n} | M_i | p_i + N_{i1}p_1 + N_{i2}p_2 + \dots + N_{iH}p_H</math>
(91).
In particular, the characteristic determinant of the matric sub-
algebra of <math>p_i^2</math> units satisfying (87) equals <math>|M_i|^{p_i}</math>. Its rank equation
is <math>|M_i| = 0</math>, as follows from Cayley's theorem on matrices (§ 15).
A determinant like <math>|M_i|</math> whose elements are independent variables
is an irreducible function of its elements.
The characteristic determinant for an algebra A2 of the second
category is a product of powers of <math>H</math> irreducible functions <math>P_i</math> of degrees
<math>p_i</math> expressible as <math>p_i</math>-rowed determinants; and the <math>\sum p_i^2</math> elements of these H
determinants are linearly independent linear functions of the coordinates.
Here H is the number of partial moduli of the sub-algebra <math>A_1</math>.
If we equate to zero each element of these determinants, we obtain
a system of linear equations which is independent of the choice of
the units (§ 16). Hence the set of nilpotent numbers whose coordinates
satisfy these equations is independent of the choice of units. When
the normalized units of § 47 are used, these nilpotent numbers are the
linear combinations of the <math>\eta</math>'s.
Invariant sub-algebra; simple and semi-simple
49.
algebras.
An invariant sub-algebra I of any algebra A is one such that the
product of any number of I by any number of A is in I and the
product of any number of A by any number of I is in I.
For example, the algebra (e1, e2, e3) in (46) has the invariant sub-
algebras <math>(e_1, e_2)</math>, <math>(e_2)</math> and <math>(e_3)</math>. Algebra (45) has the invariant sub-
algebras <math>(e_i)</math> and <math>(e_i, e_j)</math>, <math>i, j = 1, 2, 3</math>.

## PDF page 68

56
SIMPLE AND SEMI-SIMPLE ALGEBRAS
A simple algebra is one having no invariant sub-algebra.
A semi-simple* algebra is one having no nilpotent invariant sub-
Algebra (45) is semi-simple since it has no nilpotent number,
algebra.
as shown by its characteristic equation, given after (45).
50.
Main theorem. By § 37, the nilpotent numbers of an
algebra <math>A_1</math> of the first category form an invariant nilpotent sub-algebra.
Hence <math>A_1</math> is semi-simple if and only if its units are the partial moduli
<math>\epsilon_1, \ldots, \epsilon_h</math>, and is then the direct sum of the unary algebras <math>(\epsilon_1), \ldots, (\epsilon_h)</math>.
In particular, the only simple <math>A_1</math> is that with a single unit <math>\epsilon_1</math>.
In an algebra <math>A_2</math> of the second category, the <math>\eta</math>'s are, by (89), the
units of an algebra which is nilpotent (end of § 48), and an invariant
sub-algebra of <math>A_2</math>, by (88). Hence in a semi-simple <math>A_2</math> the units <math>\eta</math> are
absent, so that its units are those contained in the matric sub-algebras
of <math>p_i^2</math> units. As each of the latter is an invariant sub-algebra, a simple
<math>A_2</math> must be matric.
Conversely, any matric algebra <math>M</math> of <math>p^2</math> units <math>e_{ij}</math> is simple.
For, if
<math>x = \sum x_{ij}e_{ij} \neq 0</math> occurs in an invariant sub-algebra I, then
<math>e_{\alpha i} x e_{j\beta} = x_{ij} e_{\alpha\beta}</math>
occurs in I. Hence every <math>e_{\alpha\beta}</math> is in I and <math>M \equiv I</math>.
Similarly, the direct sum <math>m+M</math> of two matric algebras has no
invariant sub-algebra I other than m and M. For, if <math>x + X</math> be one of
its numbers and <math>x \neq 0</math>, and if the units of m are <math>e_{ij}</math>, then
<math>e_{\alpha i}(x+X)e_{i\beta}=x_{ij}e_{\alpha\beta}</math>
is in I, so that m is a sub-algebra of I. Thus <math>I=m</math> or <math>m+M</math>.
If
there be three or more summands, the argument is similar.
Since
a matric algebra or a direct sum of matric algebras is not nilpotent,
a direct sum of matric algebras is semi-simple.
An algebra <math>(a_1, \ldots, a_r, b_1, \ldots, b_s)</math> for which <math>A = (a_1, \ldots, a_r)</math> and
<math>B = (b_1, ..., b_s)</math> are sub-algebras is called the sum of the algebras A and
B. It need not be their direct sum (§ 21).
Theorem †. Any linear associative algebra with a modulus and
* In place of Cartan's definition (l.c., p. 57) of a semi-simple algebra as a
reducible algebra each of whose irreducible components is simple, I have employed
that by J. H. M. Wedderburn, Proc. London Math. Soc., ser. 2, vol. 6 (1907), p. 94,
and deduced the former property.
+ Cartan, l.c., p. 58. For simple algebras the theorem was first proved (but
not altogether satisfactorily) by Th. Molien, Math. Ann., vol. 41 (1893), p. 125;
then by Frobenius, Berlin Sitzungsber., 1903, p. 527; cf. J. B. Shaw, Trans. Amer.

## PDF page 69

§ 50]
COMMUTATIVE ALGEBRAS
57
with complex coordinates is the sum of a semi-simple algebra and
a nilpotent invariant sub-algebra. A semi-simple algebra is either
simple or a direct sum of simple algebras, and conversely. A simple
algebra is of matric type and conversely.
Commutative algebras. A commutative complex algebra
51.
with a modulus must be of the first category (§ 46, Corollary). Em-
ploying the normalized units of § 39, we see that there cannot occur
a unit <math>\eta</math> of character <math>(\alpha, \beta)</math>, <math>\beta \neq \alpha</math>. For, if so, <math>\epsilon_{\alpha} \eta = \eta</math>, <math>\eta \epsilon_{\alpha} = 0</math>, and
multiplication would not be commutative. Then the algebra is the
direct sum of <math>\Sigma_1, ..., \Sigma_h</math>, where <math>\Sigma_j</math> is formed of the numbers of character
<math>(j, j)</math>, and has <math>r</math> units <math>e = \epsilon_1, \eta_1, \eta_2, ..., \eta_{r-1}</math> such that
<math>e^2 = e</math>, <math>e\eta_i = \eta_i e = \eta_i</math>, <math>\eta_i \eta_j = \sum_{\gamma_{ijk}} \eta_k</math>
(92),
where <math>k > i</math>, <math>k > j</math>, and <math>\gamma_{ijk} = \gamma_{jik}</math>. The <math>\gamma</math>'s are of course subject to the
further conditions implied by the associative law of multiplication.
In particular, if the algebra has no nilpotent number, no units
<math>\eta</math> occur (for, <math>\eta^2_{r-1} = 0</math>), and the algebra is <math>(\epsilon_1, ..., \epsilon_h)</math>:
<math>\epsilon_i^2 = \epsilon_i, \quad \epsilon_i \epsilon_i = 0 \quad (i, j = 1, ..., h; i \neq j)</math>
(93).
Math. Soc., vol. 4 (1903), pp. 275-283. It is implied in Frobenius's theory
(see § 54) of group characters and group determinants, Berlin Sitz., 1896, pp. 985,
1343; 1897, p. 994; 1898, p. 501; 1899, pp. 330, 482; 1904, p. 558, an elementary
exposition of which was given by Dickson, Annals of Math., ser. 2, vol. 4 (1902),
pp. 25-49. For an attractive method of treating the latter theory, see I. Schur,
Berlin Sitz., 1905, p. 406 [cf. Dickson, Trans. Amer. Math. Soc., vol. 8 (1907).
p. 389]. Cf. W. Burnside, Proc. London Math. Soc., vol. 35 (1903), p. 206. For
the work of Wedderburn, see § 56. Another proof of the main theorem and the
theorems in §§ 47, 48 has been given by Frobenius, Berlin Sitz., 1903, p. 641.

## PDF page 70

PART III
RELATIONS OF LINEAR ALGEBRAS TO OTHER
SUBJECTS
52. Correspondence between linear associative algebras
and linear groups.
Consider a linear associative algebra with the multiplication table
<math>e_ie_j = \sum_{s=1}^{n} \gamma_{ijs}e_s \qquad (i, j = 1, ..., n)</math>
(94).
For <math>y</math> a fixed number and <math>x</math> a variable number of the algebra, the
equation <math>x' = xy</math> is equivalent to the <i>n</i> equations
<math>(y)</math> <math>x_s' = \sum_{i=1}^n \gamma_{ijs} x_i y_j</math> <math>(s=1, ..., n),</math>
which define a linear homogeneous transformation of the variables
<math>x_1, ..., x_n</math> into the variables <math>x_1', ..., x_n'</math>, which corresponds to the given
number y.
Similarly, to <math>y'</math> corresponds the transformation <math>x'' = x'y'</math>:
<math>(y')</math> <math>x''_t = \sum_{s=1}^{n} \gamma_{skt} x'_s y'_k</math> <math>(t = 1, ..., n)</math>
of the variables <math>x_1', ..., x_n'</math> into <math>x_1'', ..., x_n''</math>. But
<math display="block">x'' = (xy) y' = xy'', \quad y'' \equiv yy'.</math>
To <math>y''</math> corresponds the transformation
<math>(y'')</math> <math>x_t'' = \sum_{i, s=1}^n \gamma_{ist} x_i y_s'', \ y_s'' \equiv \sum_{j, k=1}^n \gamma_{jks} y_j y_k'</math> <math>(t, s=1, ..., n),</math>
the values of the <math>y_s''</math> being found from <math>y'' = yy'</math> by use of (94).
The
transformation <math>(y'')</math> is therefore identical with the so-called <i>product</i>
<math>(y)(y')</math> <math>x''_{t} = \sum_{s, k, i, j=1}^{n} \gamma_{ijs} \gamma_{skt} x_{i} y_{j} y_{k'}</math> <math>(t=1, ..., n),</math>
obtained by eliminating the variables <math>x_s'</math> between the sets of equations

## PDF page 71

§ 52]
RELATION OF ALGEBRAS TO LINEAR GROUPS
59
(y), (y'). To give a formal verification, note that the coefficients of
<math>x_i y_j y_{k'}</math> in the last two expressions for <math>x_i''</math> are equal if
<math display="block">\sum_{s=1}^{n} \gamma_{ist} \gamma_{jks} = \sum_{s=1}^{n} \gamma_{ijs} \gamma_{skt} \qquad (i, j, k, t = 1, ..., n).</math>
These are satisfied since, by (94),
<math>e_i(e_je_k) = e_i \sum_{s=1}^n \gamma_{jks}e_s = \sum_{t,s=1}^n \gamma_{ist}\gamma_{jks}e_t,</math>
<math display="block">(e_i e_j) e_k = \left(\sum_{s=1}^n \gamma_{ijs} e_s\right) e_k = \sum_{s=1}^n \gamma_{ijs} \gamma_{skt} e_t.</math>
Hence the correspondence between numbers y and transformations
<math>(y)</math> is such that to the product <math>yy'</math> of two numbers corresponds the
product <math>(y)(y')</math> of the corresponding transformations. The resulting
set of transformations is closed under multiplication since the algebra is.
For example, if the algebra is that of four units in § 4, to the
number <math>\mu</math> in (16), with the coordinates <math>\alpha</math>, <math>\beta</math>, <math>\gamma</math>, <math>\delta</math>, corresponds the
transformation <math>m' = m\mu</math> in <math>(17_2)</math>:
<math>a' = aa + b\gamma</math>, <math>b' = a\beta + b\delta</math>, <math>c' = ca + d\gamma</math>, <math>d' = c\beta + d\delta</math>
(95).
The product* of this transformation by that with the coefficients
<math>a', \ldots, \delta'</math> is the transformation with the coefficients
<math display="block">\alpha'' = \alpha'\alpha + \gamma'\beta, \quad \gamma'' = \alpha'\gamma + \gamma'\delta, \quad \beta'' = \beta'\alpha + \delta'\beta, \quad \delta'' = \beta'\gamma + \delta'\delta \quad (96).</math>
Let the algebra have a modulus <math>\epsilon</math>. The corresponding transforma-
tion <math>x' = x\epsilon = x</math> is the identity transformation <math>x_i' = x_i (i = 1, ..., n)</math>.
Then <math>\Delta(y)</math> is not identically zero. For a number y such that <math>\Delta(y) = 0</math>,
there exists a unique number <math>y^{-1}</math> such that <math>yy^{-1} = y^{-1}y = \epsilon</math> (end of § 7).
Then <math>x' = xy</math> implies <math>x = x'y^{-1}</math>, so that the transformation <math>(y^{-1})</math> is the
inverse to <math>(y)</math> and conversely. If <math>\Delta(y) \neq 0</math> and <math>\Delta(y') \neq 0</math>, then <math>\Delta(yy') \neq 0</math>,
since <math>yy'</math> has the inverse <math>y'^{-1}y^{-1}</math>.
A set of linear transformations forms a group if the product of
* Since c, d are transformed cogrediently with a, b, the work need not be
duplicated. If the matrix of the coefficients of a and b in (95) be called \u03c4, we
have <math>\mu'' = \mu'\mu</math>. The matrix of the coefficients of the product TT of two linear
transformations in n variables equals the product of the matrices of T and T
(i.e., taken in reverse order). But if we denote by T1 the transformation
<math>a = a'a + b'\gamma</math>, <math>b = a'\beta + b'\delta</math>
of matrix <math>\mu</math>, and by <math>T_1</math> the transformation of matrix <math>\mu</math> expressing <math>a'</math>, <math>b'</math> in terms of
a", b", then by eliminating a', b', we obtain as the transformation expressing a, b
in terms of a", b" one with the matrix <math>\mu\mu'</math>. Thus transformations, expressing the
old variables in terms of the new, compound as their matrices taken in the same
See also the second foot-note in § 53.
order.

## PDF page 72

60
RELATION OF ALGEBRAS TO LINEAR GROUPS
any two of the set is a transformation of the set, if the set contains
the identity transformation, and if each transformation has an inverse
in the set. Thus we have
Theorem 1*. The set of all numbers not nilfactors of a linear
associative algebra with n units and having a modulus corresponds to
a group G of linear transformations on n variables whose coefficients
are linear functions of n arbitrary parameters.
The determinant <math>\Delta'(y)</math> of each transformation <math>(y)</math> of <math>G</math> is not zero.
The group is called <i>simply transitive</i> since it contains a unique trans-
formation <math>(y)</math> which replaces a given general set of values <math>x_1, ..., x_n</math>,
viz., one for which <math>\Delta(x) \neq 0</math>, by any given set <math>x_1', ..., x_n'</math> for which
<math>\Delta(x') \neq 0</math>. Indeed, <math>xy = x'</math> then has a unique solution y for which
<math>\Delta(y) \neq 0</math> and hence <math>\Delta'(y) \neq 0</math>.
To any number y corresponds also a transformation <math>x' = yx</math>:
<math>[y]</math> <math>x_s' = \sum_{i=1}^n \gamma_{jis} x_i y_j</math> <math>(s = 1, ..., n).</math>
Similarly, to <math>y'</math> corresponds <math>[y']</math>: <math>x'' = y'x'</math>. Then
<math>x'' = y'(yx) = y''x</math>, <math>y'' = y'y</math>, <math>[y''] = [y'][y]</math>.
Hence we obtain a second simply transitive group <math>G'</math>.
If we apply a transformation <math>(y): x' = xy</math> and then a transformation
<math>[z]: x'' = zx'</math>, we obtain <math>(y)[z]: x'' = zxy</math>. The same result is obtained
by applying first <math>[z]: x' = zx</math> and afterwards <math>(y): x'' = x'y</math>. Hence
every transformation of G is commutative with every transformation of
G'. Two such simply transitive mutually commutative groups are
called reciprocal.
The coefficients of the transformation, written at the end of formula
<math>(y'')</math>, replacing the variables <math>y_1, ..., y_n</math> by the variables <math>y_1'', ..., y_n''</math>, are
the same functions of the parameters <math>y_1, ..., y_n</math> as the coefficients of
the <math>x_i</math> in <math>(y)</math> are of the parameters <math>y_1, ..., y_n</math>, as is also clear from the
formulas <math>y'' = yy'</math>, <math>x' = xy</math>. For this reason, the group G is said to be
its own parameter group. Similarly, <math>y'' = y'y</math>, <math>x' = yx</math> show that <math>G'</math> is
its own parameter group.
Theorem 2†. Every linear associative algebra with a modulus
* Stated by Poincaré, Paris Comptes Rendus, vol. 99 (1884), p. 740.
+ E. Study, Leipzig Berichte, vol. 41 (1889), math., p. 202; reprinted in
Monatshefte Math. u. Phys., vol. 1 (1890), pp. 283-355. While Study used the
theory of bilinear forms, Scheffers gave a purely group-theoretic proof, using infini-
tesimal transformations (Lie-Scheffers, Continuierliche Gruppen, 1893, p. 627).
Cf. Scheffers, Leip. Ber., vol. 41 (1889), math., pp. 290-307.

## PDF page 73

§ 52]
RELATION OF ALGEBRAS TO LINEAR GROUPS
61
defines a definite pair of reciprocal groups, each its own parameter
group. Conversely, given any pair of simply transitive groups, reciprocal
to each other, of linear homogeneous transformations on n variables, we
can find new variables <math>x_1, ..., x_n</math> such that the groups are reduced simul-
taneously to groups of transformations (y) and [y] in which the n
parameters <math>y_1, ..., y_n</math> enter linearly and homogeneously and such that
each new group is its own parameter group; hence (y) defines a rule of
multiplication <math>x' = xy</math> of two numbers of a linear associative algebra
with the units <math>e_1, ..., e_n</math> and multiplication table (94).
Consider the linear transformation <math>Q = q_1 q q_2</math>, where
<math>q = x + yi + zj + wk</math>, <math>Q = X + Yi + Zj + Wk</math>
are quaternions with variable coordinates and q1, q2 are given quater-
nions. Then, by § 12,
<math>N(Q) = X^2 + Y^2 + Z^2 + W^2 = c(x^2 + y^2 + z^2 + w^2), \quad c = N(q_1 q_2).</math>
For <math>c \neq 0</math>, we have a transformation, involving seven arbitrary
constants, expressing X, Y, Z, W as linear functions of determinant
<math>\pm 0</math> of <math>x, y, z, w</math>, which multiplies <math>x^2 + y^2 + z^2 + w^2</math> by <math>c</math>. If we start
with the general quaternary linear transformation having 16 coefficients
and impose the last condition, viz., that the coefficients of the six
terms <math>XY</math>, ... shall vanish, and those of <math>X^2</math>, ... shall be equal, we
have nine relations and hence seven free constants. Supplementing
this "counting of constants" by the definitive formula* for the
resulting transformations, we see that all are given by the quaternion
transformation <math>Q = q_1 q q_2</math>. We therefore have a very convenient
expression for the group † generated by rotations around the origin and
stretchings from it. To obtain the corresponding group; in three
dimensions, we have only to take <math>x = X = 0</math>, <math>q_2 = q_1</math>, the quaternion
conjugate to <math>q_1</math>.
For further relations between linear algebras and groups of trans-
formations not necessarily linear, and for various geometric aspects of
our subject, the reader is referred to the Encyc. Sc. Math., vol. 1, 1,
* Cayley, 1854, Coll. Math. Papers, 11, pp. 133, 214; Klein, Math. Ann.,
vol. 37 (1890), p. 544, and Elementarmath. vom höheren Standpunkte aus, 1,
p. 161.
+ Since if also <math>Q_1 = q_3 Q q_4</math>, then <math>Q_1 = (q_8 q_1) q (q_2 q_4)</math>.
# By retaining only transformations of positive determinants, we exclude
<math>y' = -y, \quad z' = -z, \quad w' = -w</math>
and its products by the former.

## PDF page 74

62
RELATION OF ALGEBRAS TO BILINEAR FORMS
pp. 448-465. Also to p. 468 for the connection between the con-
tinuous groups of Sophus Lie and non-associative linear algebras in
which <math>ab = -ba</math>, <math>(ab) c + (bc) a + (ca) b = 0</math>, for any three numbers
<math>a, b, c</math> of the algebra.
53. Correspondence between linear associative algebras
and systems of bilinear forms.
If <math>x_i</math>, <math>u_i</math> (<math>i = 1, ..., n</math>) are <math>2n</math> independent variables,
<math display="block">A = \sum_{i=1}^{n} a_{ij} x_i u_j</math>
is called a bilinear form. Let B denote a similar form with the co-
efficients <math>b_{ij}</math>. Then <math>A+B</math> denotes the form with the coefficients
<math>a_{ij} + b_{ij}</math>. The product * AB is the bilinear form C with the coefficients
<math>c_{ij} = \sum_{k=1}^{n} a_{ik} b_{kj}</math>  <math>(i, j = 1, ..., n).</math>
Thus the matrix of the coefficients of the sum or product of two
bilinear forms is the sum or product of their matrices, taken in the
same order. The subject of bilinear forms is therefore essentially
identical with that of matrices and, if we agree to use also singular
transformations (of determinant zero), with that of linear homogeneous
transformations.
If at the beginning of § 52 we take <math>y = e_j</math>, the equation <math>x' = xe_j</math>
gives
<math>x_{s}' = \sum_{i=1}^{n} \gamma_{ijs} x_{i}</math>  <math>(s = 1, ..., n),</math>
the matrix of which has the element <math>\gamma_{ijs}</math> in the sth row and ith column.
Taking <math>\dagger</math> it as the <math>a_{is}</math> in <math>A</math>, we obtain the bilinear form
<math display="block">A_j = \sum_{i,s=1}^n \gamma_{ijs} x_i u_s.</math>
Then the number <math>\sum c_j e_j</math> corresponds to the bilinear form <math>\sum c_j A_j</math>, while
* Hence <math>AB = \sum_{k} \frac{\partial A}{\partial u_k} \frac{\partial B}{\partial x_k}</math>. This is the definition by Frobenius, <i>Jour. der Math.</i>,
vol. 84 (1877), pp. 1-63, the most important paper on the subject.
† If <math>TT' = T''</math> for linear transformations then <math>\overline{\mu} \overline{\mu}' = \overline{\mu}''</math>, where <math>\overline{\mu}</math> denotes the
matrix <math>\mu</math> of T with the rows and columns interchanged. Thus in (95), (96),
<math display="block">\begin{pmatrix} a & \beta \\ \gamma & \delta \end{pmatrix} \begin{pmatrix} a' & \beta' \\ \gamma' & \delta' \end{pmatrix} = \begin{pmatrix} a'' & \beta'' \\ \gamma'' & \delta'' \end{pmatrix}.</math>

## PDF page 75

§ 53]
RELATION OF ALGEBRAS TO FINITE GROUPS
63
the sum or product of two numbers corresponds to the sum or product
of the corresponding bilinear forms*.
For example, the units 1, i of the binary algebra of complex numbers
correspond to <math>x_1u_1 + x_2u_2</math> and <math>x_1u_2 - x_2u_1</math>.
An excellent example is furnished by the matric algebra of four units.
Since the corresponding group (95) affects the two pairs of variables cogredi-
ently, the bilinear forms are each the sum of two similar parts on separate
variables, <math>x_i u_j</math>, <math>i, j=1, 2</math> in one part and <math>i, j=3, 4</math> in the other part. Re-
taining only the first parts, we obtain
<math>ax_1u_1 + \beta x_1u_2 + \gamma x_2u_1 + \delta x_2u_2</math>
as the part corresponding to the transposed matrix of coefficients of a and b
in (95). Thus each unit <math>e_{ij}</math> of the algebra [see (162)] corresponds to the
bilinear form <math>B_{ij} \equiv x_i u_j</math> with the same subscripts. The <math>\dagger B_{ij}</math> satisfy relations
(14).
Conversely, given n bilinear forms <math>A_1, ..., A_n</math> in <math>x_i, u_i (i = 1, ..., n)</math>
such that each <math>A_r A_s</math> is a linear function of <math>A_1, ..., A_n</math> with constant co-
efficients, we may take them as the units of a linear associative algebra.
The subject of bilinear forms; is therefore at bottom identical with
that of linear associative algebras.
54. Relations of linear algebras to finite groups. Con-
sider for example the rotations I, A, B in a plane about a point
through angles 0°, 120°, 240°, respectively. They form a group with
the multiplication table
<math display="block">
\begin{array}{c|ccccccccccccccccccccccccccccccccccc</math>
This is read <math>AB = I</math>, etc. Taking <math>I</math>, <math>A</math>, <math>B</math> as units whose products are
given by the table, we have a linear associative algebra §. Similarly, if
we start with any finite group, which is associative by definition.
* C. S. Peirce proved this theorem expressed in a different notation; see list of
his papers in Encyc. Sc. Math., vol. 1, 1, p. 416. Cf. Study, Leip. Ber., vol. 41
(1889), p. 192.
† The easiest verification is by differentiation (see first foot-note of this section).
‡ References are given in Encyc. Sc. Math., vol. 1, 1, pp. 415-421, 444-446.
For an account of the theory of bilinear forms and their applications, see Muth,
Elementartheiler, Leipzig, 1899.
§ Cayley, Phil. Mag., vol. 7 (1854), p. 46 (= Coll. Math. Papers, vol. 11, 1889,
p. 129).

## PDF page 76

64
DEDEKIND'S VIEW FOR ALGEBRAS
[(94)]
If we take I, A, B as ordinary variables, and consider the three-
rowed matrix forming the body of the multiplication table of the above
group (the multipliers having been arranged so that every element of
the main diagonal is <math>I</math>), we have an example of what Frobenius* calls
the group matrix of a given finite group. The product of two such
group matrices is another of the same kind:
<math display="block">\begin{pmatrix} I & A & B \\ B & I & A \\ A & B & I \end{pmatrix} \begin{pmatrix} i & a & b \\ b & i & a \\ a & b & i \end{pmatrix} = \begin{pmatrix} \iota & a & \beta \\ \beta & \iota & a \\ a & \beta & \iota \end{pmatrix}, \quad \begin{matrix} \iota = Ii + Ab + Ba, \\ a = Ia + Ai + Bb, \\ \beta = Ib + Aa + Bi. \end{matrix}</math>
Call <math>e_1</math> the matrix obtained from the first by setting <math>I = 1</math>, <math>A = B = 0</math>;
<math>e_2</math> that by setting <math>A=1</math>, <math>I=B=0</math>; <math>e_3</math> by <math>B=1</math>, <math>I=A=0</math>. Then
<math>(Ie_1 + Ae_2 + Be_3)(ie_1 + ae_2 + be_3) = \iota e_1 + ae_2 + \beta e_3</math>
is the equivalent of the above relation between matrices, and is the
multiplication formula for the algebra with modulus <math>e_1</math> and
<math>e_2^2 = e_3</math>, <math>e_2 e_3 = e_3 e_2 = e_1</math>, <math>e_3^2 = e_2</math>.
We have in effect returned to our group of three operators. For an
elegant exposition of this direct relation between the theory of group
matrices and linear algebras, and applications to Abelian integrals, see
a memoir by Poincaré †.
Dedekind's point of view for linear associative com-
55.
mutative algebras ‡. Consider the example of the commutative
triple algebra:
<math>e_1^2 = e_1 + e_2 + e_3</math>, <math>e_2 e_3 = e_2</math>, <math>e_2^2 = e_3^2 = e_3</math>, <math>e_1 e_2 = e_1 e_3 = e_2 + e_3</math>.
Regarding these as ordinary algebraic equations for the unknowns <math>e_i</math>,
we find at once that they have only four sets of solutions:
<math>(e_1, e_2, e_3) = (0, 0, 0), (1, 0, 0), (2, 1, 1), (0, -1, 1).</math>
Excluding of course the first set, Dedekind regarded the e's as multi-
valued (but correlated) numbers, so that any linear function of them is
three-valued. The correlation is here such that, when <math>e_2 = r</math>, then
<math>e_1 = r + 1</math>, <math>e_3 = r^2</math>, where r is a three-value function for which <math>r^3 = r</math>.
In
general, the multiplication equations
<math>e_i e_j - \sum_{k=1}^n \gamma_{ijk} e_k = 0</math>  <math>(i, j = 1, ..., n)</math>
(94)
* References at the end of § 50.
† Journ. de Math., ser. 5, vol. 9 (1903), p. 180.
# Göttingen Nachr., 1885, p. 141; 1887, p. 1; reproduced by B. Berloty, Thèse,
Paris, 1886.

## PDF page 77

§ 55]
DEDEKIND'S VIEW FOR ALGEBRAS
65
of a commutative associative algebra have n sets of real or complex
solutions of determinant* not zero if and only if
<math display="block">\left|\sum_{i, j=1}^{n} \gamma_{rsi} \gamma_{ijj}\right| \neq 0 \qquad (r, s=1, ..., n).</math>
Not far removed from this view is that of Kroneckert, who obtained
all commutative linear associative algebras by use of modular systems,
the moduli being the left members of (94).
* Cf. J. Petersen, Gött. Nachr., 1887, p. 489; G. Frobenius, Berlin Sitzungsber.,
1896, p. 601; D. Hilbert, Gött. Nachr., 1896, p. 179 (by the theory of invariants).
+ Berlin Sitzungsber., 1888, pp. 429, 447, 557, 595, 983. See the clear abstract
in Encycl. Sc. Math., vol. 1, 1, pp. 409-411.
5
D.

## PDF page 78

PART IV
LINEAR ALGEBRAS OVER A FIELD F
By a division algebra shall be meant one in which both right-
56.
hand and left-hand division, except by zero, are possible and unique.
The fundamental theorem of § 50 on complex algebras has been
generalized by Wedderburn* as follows:
Theorem 1. Any linear associative algebra over a field <math>F</math> is the sum
of a semi-simple algebra and a nilpotent invariant sub-algebra, each
over F. A semi-simple algebra over F is either simple or the direct sum
of simple algebras over F. Any simple algebra over F is the direct
product of a division algebra and a simple matric algebra each over F,
including the possibility that the modulus is the only unit of one factor.
As the part relating to simple algebras is quite different from our
former result for the case of the complex field, it will clarify the
subject to have a proof of the converse:
Theorem 2. The direct product P of a division algebra D and
a matric algebra M, each over F, is simple; any number of P com-
mutative with every number of <math>P</math> is in <math>D</math>.
Denote the units of M by <math>e_{pq}(p, q = 1, ..., n)</math>, so that the <math>e_{pp}</math> are the
partial moduli and <math>\epsilon = e_{11} + ... + e_{nn}</math> is the modulus of <math>M</math> and hence of
P. Let I be any invariant sub-algebra of P, and <math>i = \sum \delta_{rs} e_{rs}</math> be any
number of I, where <math>\delta_{rs}</math> is in D. Since I is invariant, <math>e_{pp}ie_{qq}</math> is in I.
Allowing p and q to vary, we get a product <math>\neq 0</math> if <math>i \neq 0</math>, since
<math display="block">\sum_{p, q=1}^{n} e_{pp} i e_{qq} = \sum_{p=1}^{n} e_{pp} i \epsilon = \epsilon i \epsilon = i.</math>
Thus, for a certain pair of integers <math>p</math> and <math>q</math>,
<math display="block">\delta_{pq} e_{pq} = e_{pp} i e_{qq} \neq 0.</math>
* Proc. London Math. Soc., ser. 2, vol. 6 (1907), p. 109.

## PDF page 79

§ 56]
ALGEBRAS OVER ANY FIELD
67
Thus I contains a number <math>\delta_1 e_{pq}</math>, where <math>\delta_1</math> is a number <math>\neq 0</math> of D. If <math>\delta</math>
is any element of <math>D</math>, we can find a number <math>\delta_2</math> of <math>D</math> such that <math>\delta_2 \delta_1 = \delta</math>.
Hence <math>I</math> contains <math>\delta e_{pq}</math> and therefore also
<math>\delta e_{pq} e_{qr} = \delta e_{pr}, \quad e_{sp} \delta e_{pr} = \delta e_{sp} e_{pr} = \delta e_{rr}</math>
where <math>r</math>, <math>s</math> are any positive integers <math>\leq n</math>. Hence <math>I \equiv P</math>.
Next, if x is any number of P commutative with every number of
<math>P</math>, set <math>x = \sum \delta_{rs} e_{rs}</math>, where <math>\delta_{rs}</math> is in <math>D</math>. Then
<math display="block">\sum_{r=1}^{n} \delta_{rp} e_{rq} = x e_{pq} = e_{pq} x = \sum_{s=1}^{n} \delta_{qs} e_{ps},</math>
where <math>p</math> and <math>q</math> are arbitrary. Hence
<math>\delta_{rp} = 0 \ (r \neq p), \quad \delta_{pp} = \delta_{qq}, \quad x = \delta_{11} \sum e_{qq} = \delta_{11} \epsilon = \delta_{11},</math>
so that <math>x</math> is in <math>D</math>. The case in which <math>D</math> has a single unit gives the
Corollary. In a matric algebra <math>M</math> with the modulus <math>\epsilon</math>, the numbers
<math>a_{\epsilon}</math> (a scalar) are the only ones commutative with every number of M.
Hence (§ 52) the only linear transformations commutative with everyone
are those multiplying each variable by the same constant.
When <math>F</math> is the field of all complex numbers, any number of
a division algebra satisfies a linear equation (§ 11), so that the algebra
is the field itself. Hence (in agreement with § 50), any simple algebra
is matric.
When F is the field of all real numbers, the only division algebras
are the three found in § 11. We have therefore
Theorem 3*. Every real simple algebra is either a real matric
algebra M with p2 units eik, or the direct product of M and the algebra
(1, i) of ordinary complex numbers, or the direct product of M and the
algebra of real quaternions.
For the second type, the units are <math>e_{jk}</math>, <math>e'_{jk} = ie_{jk} = e_{jk}i</math>, where
<math>e_{jk}e'_{lm} = e'_{jk}e_{lm} = 0 	 (k \neq l),</math><br><math>e'_{jk}e'_{lm} = 0 	 (k \neq l),</math><br><math>e'_{jk}e'_{lm} = -e_{jm} 	 (k = l).</math>
By the above corollary, a commutative matric algebra has a single
unit e. Using the first parts of Theorem 1 and Theorem 3, we get
* Expressed and proved otherwise by Cartan (l.c., pp. 61-72). He also
proved the first part of Theorem 1 for real algebras. The method was to study
the corresponding complex algebra with the same units. We conclude that a
real division algebra is simple and hence by Theorem 3 of one of the three types
in § 11.

## PDF page 80

68
ALGEBRAS OVER ANY FIELD
Theorem 4. Any real commutative algebra without nilpotent
numbers is the direct sum of certain algebras <math>(\epsilon_i)</math>, each equivalent to the
algebra of real numbers, and certain algebras <math>(e_i, e'_i)</math>,
<math>e_i^2 = e_i</math>, <math>e_i'^2 = -e_i</math>, <math>e_i e_i' = e_i' e_i = e_i'</math>,
each equivalent to the algebra of ordinary complex numbers.
We obtain a sub-algebra of the complex algebra (93) by setting
<math>E_i, E'_i = \frac{1}{2} (e_i \pm \sqrt{-1} e'_i), \quad E^2 = E, \quad E'^2 = E', \quad EE' = E' E = 0.</math>
57. The algebras of Weierstrass. If <math>k</math> is a nilfactor (i.e.,
a number for which <math>ky = 0</math> has a solution <math>y \neq 0</math>, and <math>\sigma</math> is not, there is
an infinitude of numbers x satisfying the equation <math>k\rho + k\sigma x = 0</math>. For,
if y is one of the infinitude of y's satisfying <math>ky = 0</math>, it has the solution
x where x is determined from <math>\rho + \sigma x = y</math>. Similarly, there are equations
of any degree <math>m</math>, having each coefficient <math>c_i</math> a multiple of <math>k</math>, with an
infinitude of roots, viz., <math>x = x_0 + yz</math>, where <math>\sum c_i x_0^i = 0</math>. Weierstrass*
investigated real linear algebras in which multiplication is commutative
and associative, with <math>\Delta(x)</math> not identically zero (§ 6), and such that the
only algebraic equations having an infinitude of roots are those in
which all of the coefficients are multiples of one and the same nilfactor.
By a rather long, but elegant analysis, he proved that such an algebra
is equivalent under a real linear transformation of units to a direct
sum of real unary and binary algebras (as given in the above Theorem
4), and conversely that the resulting algebra has the specified
properties.
This result follows at once from Theorem 4; for, if the algebra had
a nilpotent number <math>\eta</math>, so that <math>\eta^k = 0</math>, the equation <math>x^k = 0</math> would have an
infinity of roots <math>r\eta</math> (r real) and yet its coefficients are not nilfactors.
But Theorem 4 was based upon results not proved in this tract. We
shall therefore give a direct proof (the second of Study's two proofs†)
of the theorem of Weierstrass, in the equivalent form (known to the
latter) that the corresponding complex algebra is of type (93). It
suffices to prove that the only complex irreducible algebras of Weier-
strass are those with a single unit <math>\epsilon</math>. By the criterion of Scheffers
(§ 21) an irreducible commutative algebra with a modulus <math>\epsilon</math> has no
further number e such that <math>e^2 = e</math>. Thus (§ 20) the rank equation is
<math>(\alpha - \lambda \epsilon)^r = 0</math>. If <math>r > 1</math>, <math>(\alpha - \lambda \epsilon)^{r-1}</math> is a root <math>\neq 0</math> of <math>x^2 = 0</math>. Hence <math>r = 1</math>
and the only unit is <math>\epsilon</math>.
* Göttingen Nachr., 1884, pp. 395-419.
† Göttingen Nachr., 1898, p. 1 [1889, pp. 262-5]. All except the last papers
cited in § 55 deal with this subject.

## PDF page 81

§ 58]
DIVISION ALGEBRAS
69
58.
Commutative non-associative division algebras.
Let F be any field (except one with the modulus 2 in which therefore
2x counts as zero) for which there is an irreducible function
<math>x^3 - Bx^2 - \beta x - b</math> (B, <math>\beta</math>, b in F).
Then division except by zero is always possible and unique in the
algebra * with the units 1, i, j over F for which
<math>i^2 = j</math>, <math>ij = ji = b + \beta i + Bj</math>, <math>j^2 = 4bB - \beta^2 - 8bi - 2\beta j</math> (97).
If the final equation be replaced by
<math>j^2 = i(ij) = bB + (b + \beta B)i + (\beta + B^2)j</math>
we obtain the field <math>F(i)</math>, the determinant <math>\Delta(x)</math> of whose general
number <math>x = r + si + tj</math> vanishes if and only if <math>r</math>, <math>s</math>, <math>t</math> are all zero. Hence
the latter property holds also for the function <math>\delta</math> derived from <math>\Delta(x)</math> by
replacing r, s, t by <math>r + \beta t</math>, <math>s + 2Bt</math>, <math>-2t</math> respectively. But <math>\delta</math> is the
determinant of <math>x</math> for algebra (97).
Of quite another character is the commutative division algebra t
with <math>2n</math> units <math>J^r</math>, <math>IJ^r</math> <math>(r = 0, 1, ..., n - 1)</math> over <math>F</math>, where <math>J</math> is a root of
a uniserial Abelian equation
<math>x^{n}-c_{1}x^{n-1}+c_{2}x^{n-2}-\ldots\pm c_{n}=0,</math>
i.e., an equation irreducible in F and having the roots
<math>J, J' = \Theta(J), J'' = \Theta(J') = \Theta^2(J), ..., J^{(n-1)} = \Theta^{n-1}(J) [\Theta^n(J) = J],</math>
where <math>\Theta</math> is a polynomial with coefficients in <math>F</math>, with the further con-
dition that <math>c_n</math> is not the square of a number of <math>F</math>. The general
number of the algebra is <math>A + BI</math>, where <math>A</math>, <math>B</math> are polynomials in <math>J</math>
with coefficients in F. Write <math>B' = B(J')</math>, <math>B'' = B(J'')</math>, etc. for the
conjugates to <math>B(J)</math>. The multiplication table of the algebra is
defined by
<math display="block">(A+BI)(X+YI)=R+SI, R=AX+B'Y'J, S=BX+AY </math> (98).
The last two equations can be solved for <math>X</math> and <math>Y</math> in the field <math>F(J)</math>
provided <math>A</math> and <math>B</math> are not both zero. Eliminating <math>X</math>, we get
<math>BB'Y'J-A^2Y=C</math>, <math>C=BR-AS</math>.
* Dickson, "On finite algebras," Göttingen Nachrichten, 1905, pp. 358-393;
Bull. Amer. Math. Soc., vol. 14 (1907-8), p. 169, where these algebras are proved
to be the only ones with three units and division unique if F is a finite field, by
use of a remarkable theorem on non-vanishing ternary cubic forms; Trans. Amer.
Math. Soc., vol. 7 (1906), pp. 370-390, where (97) is found by invariantive pro-
perties.
† Dickson, Trans. Amer. Math. Soc., vol. 7 (1906), p. 514.
5-3

## PDF page 82

[(99)]
70
DIVISION ALGEBRAS
In <math>C, C', ..., C^{(n-1)}</math> the determinant of the coefficients of <math>Y, Y', ...</math>
equals
<math>c_n B^2 B'^2 \dots [B^{(n-1)}]^2 - A^2 A'^2 \dots [A^{(n-1)}]^2 \neq 0,</math>
and the resulting Y satisfies the preceding equation. Hence division
except by zero is always possible and unique.
Linear associative division algebras. Let <math>\phi(x) = 0</math> be
59.
any uniserial Abelian equation of degree r in a field F. Call its roots
<math>i, \quad \Theta(i), \quad \Theta^2(i) = \Theta[\Theta(i)], \dots, \quad \Theta^{r-1}(i) \qquad [\Theta^r(i) = i].</math>
Then <math>i^s j^t(s, t=0, 1, ..., r-1)</math> are the <math>r^2</math> units of a linear associative
algebra <math>*</math> over <math>F</math> having
<math>\phi(i) = 0</math>, <math>ji = \Theta(i)j</math>, <math>j^r = g</math>
(99),
where g and the coefficients of the polynomials <math>\Theta</math> and <math>\phi</math> are in F. If
<math>r=2</math>, we may, without loss of generality, take <math>i^2=c</math>, where c is in F
but is not the square of a number of F. The linear functions of i
form a field <math>F(i)</math>. The general number of the algebra is <math>N = a + \beta j</math>,
<math>\alpha</math> and <math>\beta</math> in <math>F(i)</math>. If <math>\beta = 0</math>, N has the inverse <math>\alpha^{-1}</math>, in <math>F(i)</math>. If <math>\beta \neq 0</math>,
<math>N = \beta \nu</math>, where <math>\nu</math> is of the form <math>\gamma + j</math>, and <math>\gamma = e + fi</math>. Write <math>\gamma' = e - fi</math>.
Since <math>\Theta(i) = -i</math>, we have
<math>ji = -ij</math>, <math>j\gamma = \gamma'j</math>, <math>(j - \gamma')(j + \gamma) = g - \gamma\gamma'</math>.
Hence <math>\dagger</math> every number <math>N \neq 0</math> has an inverse if g is not the norm
<math>\gamma \gamma' \equiv e^2 - cf^2</math> of a number <math>\gamma</math> of <math>F(i)</math>. The conditions on <math>c</math> and <math>g</math> are
satisfied when F is the field of reals by taking <math>c = g = -1</math>, and the
algebra is then that of real quaternions.
A like result holds <math>\ddagger</math> for any r. By (99<sub>2</sub>),
<math>jf(i) = f(\Theta)j</math>, <math>j^2f(i) = f[\Theta^2(i)]j^2</math>
(100),
where <math>f</math> is a polynomial with coefficients in <math>F</math>. We shall treat the
typical case <math>r=3</math>. We have at once
<math display="block">[j^2 + k(\Theta^2)j + k(\Theta)k(\Theta^2)][j - k(i)] = g - k(i)k(\Theta)k(\Theta^2),</math>
where <math>k(\Theta^2)</math> denotes <math>k[\Theta^2(i)]</math>. Assume that g is not the norm of
a number of <math>F(i)</math>.
Then every <math>j - k(i)</math> has an inverse.
It remains
only to show that
<math display="block">z = j^2 + \alpha j + \beta</math>
has an inverse, <math>\alpha</math> and <math>\beta</math> being in <math>F(i)</math>. But
<math display="block">z [j-a(\Theta)] = [\beta - a(i) a(\Theta^2)] j + g - \beta(i) a(\Theta)</math>
* Dickson, Trans. Amer. Math. Soc., vol. 15 (1914), p. 31.
+ Dickson, l.c., and Trans. Amer. Math. Soc., vol. 13 (1912), pp. 65, 66.
‡ Wedderburn, Trans. Amer. Math. Soc., vol. 15 (1914), p. 162.

## PDF page 83

§ 59]
DIVISION ALGEBRAS
71
is not zero since g is not the norm of <math>a(i)</math>; and each number of <math>F(i)</math>
and each linear function of <math>j</math> has an inverse.
The existence of these linear associative algebras in r2 units in
which both right- and left-hand division except by zero is always possible
and unique is of decided interest and importance in view of the rôle of
division algebras in the general theory of § 56.
On the contrary, if the field F has only a finite number of elements
multiplication must be commutative in a linear associative division
algebra, which is therefore a field *.
Finite associative division algebras †. Consider p<sup>3</sup>
60.
couples <math>(x, y)</math>, where <math>x, y</math> are integers taken modulo <math>p, p</math> a prime > 2,
such that
<math>(a, c) + (x, y) = (a + x, c + y)</math>
(101),
<math>(a, c) \cdot (x, y) = (ax + \epsilon vcy, cx + \epsilon ay)</math>
(102).
Here <math>\nu</math> is a fixed quadratic non-residue of <math>p</math>, while
<math>\epsilon \equiv (a^2 - \nu c^2)^{\frac{p-1}{2}} \pmod{p}.</math>
Right-hand and left-hand division except by (0, 0) are each possible
Multiplication is associative. The first distributive law
and unique.
<math>(4_1)</math> holds, but not <math>(4_2)</math>.
For p a prime of the form <math>3l+1</math>, define the sum of <math>(a, b, c)</math> and
<math>(x, y, z)</math> as in (101), and their product to be
<math>(ax + \epsilon vcy + \epsilon^2 vbz, bx + \epsilon ay + \epsilon^2 vcz, cx + \epsilon by + \epsilon^2 az),</math>
where <math>\nu</math> is a fixed cubic non-residue of <math>p</math>, and
<math>\epsilon \equiv D^{-\frac{1}{3}} \pmod{p}, \quad D = a^3 + vb^3 + v^2c^3 - 3vabc.</math>
Now <math>D</math> is divisible by <math>p</math> only when <math>a</math>, <math>b</math>, <math>c</math> are. Indeed, <math>D</math> is the
determinant <math>\Delta(x)</math> for the field algebra of the numbers
<math>x = a + b\rho + c\rho^2</math>, <math>\rho^3 \equiv v \pmod{p}</math>.
Hence each kind of division except by (0, 0, 0) is possible and unique.
Multiplication is associative, and the first distributive law (41) holds.
The generalization to n-tuples is immediate.
* Wedderburn, Trans. Amer. Math. Soc., vol. 6 (1905), p. 349; Dickson,
Göttingen Nachr., 1905, p. 381.
† Dickson, Göttingen Nachr., 1905, p. 358.

## PDF page 84

72
STATEMENT OF FURTHER RESULTS
Each of the algebras (97) and (101)—(102) has been used to
construct non-Desarguesian and non-Pascalian geometries*.
61.
Statement of further results on general linear
algebras.
Let A be a linear algebra, not necessarily associative, over a field
F. Let I be any invariant sub-algebra of A. Let <math>i_1, ..., i_p</math> be a com-
plete set of linearly independent numbers of I with respect to the field
F. Choose numbers <math>a_1, ..., a_q</math> of A such that <math>i_1, ..., i_p, a_1, ..., a_q</math> form
a complete set of linearly independent numbers of A with respect to
F. Let <math>i, i', ...</math> denote linear functions of <math>i_1, ..., i_p</math> with coefficients in
F; and <math>a, a', ...</math> linear functions of <math>a_1, ..., a_q</math>. Then <math>ai'</math> and <math>ia'</math> are
numbers i" and i" of the invariant sub-algebra I. Hence
<math>(a+i)(a'+i') = aa' + i'''', \quad i'''' = ii' + i'' + i'''.</math>
Hence if we suppress the components <math>x_1i_1, ..., x_pi_p</math> in all numbers and
products of numbers of A, we obtain a linear algebra which is said to
accompany <math>\dagger</math> A and to be complementary to I. It is conveniently
denoted by <math>A-I</math> and called a difference algebra. The number of its
units is the excess of the number of units of A over the number of
units of I. By regarding as identical those numbers of A which differ
only by numbers of I, we obtain <math>A-I</math>. It is an associative algebra if
A is.
If each <math>A_r</math> is a maximal invariant sub-algebra of <math>A_{r-1}</math>, then <math>A_1</math>,
<math>A_2, A_3, \dots</math> is called a <i>composition series</i> of <math>A_1</math>. The difference algebras
<math>A_1 - A_2</math>, <math>A_2 - A_3</math>, ... are said to form a difference series of <math>A_1</math>. Any
two difference series of A<sub>1</sub> differ only in the arrangement of the terms of
the series. Each algebra of the difference series is simple. A like
theorem holds when each <math>A_r</math> is the largest sub-algebra of <math>A_{r-1}</math> in-
variant in <math>A_1</math>, the resulting series being called a principal or chief
difference series. These theorems are analogous to those relating to
a composition series of a finite group.
Let <math>A_1</math> be a reducible algebra and <math>A_2</math> its largest sub-algebra such
that <math>A_1</math> is the direct sum (§ 21) of <math>A_2</math> and another sub-algebra <math>A_2</math>. If
<math>A_2</math> is reducible, let <math>A_3</math> be its largest sub-algebra such that <math>A_2</math> is the
direct sum of <math>A_3</math> and another sub-algebra of <math>A_2</math>, etc. Then the series
* Veblen and Wedderburn, Trans. Amer. Math. Soc., vol. 8 (1907), p. 379.
† Th. Molien, Math. Ann., vol. 41 (1893), p. 93, begleitendes System; G.
Frobenius, Berlin Sitzungsb., 1903, p. 523, homomorphe Gruppe.
‡ Wedderburn, Proc. London Math. Soc., ser. 2, vol. 6 (1907), pp. 84, 110;
Epsteen and Wedderburn, Trans. Amer. Math. Soc., vol. 6 (1905), p. 176.

## PDF page 85

§ 61]
STATEMENT OF FURTHER RESULTS
73
<math>A_1-A_2</math>, <math>A_2-A_3</math>, ... is called * a reduction series of <math>A_1</math>. Any two
reduction series of A1 differ only in the arrangement of their terms.
By use of the latter theorem, Wedderburn proved that a linear
associative algebra over a field can be expressed in one and but one way
as the direct sum of irreducible algebras each having a modulus and an
algebra without a modulus. In particular t, an algebra with a modulus
can be expressed as the direct sum of irreducible algebras each having
a modulus. The rank equation of <math>s + S</math> is the product <math>\sharp</math> of the rank
equations of <math>s</math> and <math>S</math>.
Analytic functions of hypercomplex numbers. B.
62.
Berloty in his thesis (Paris, 1886) extended the elements of the theory
of functions of a complex variable to that of a number in an algebra of
Weierstrass. The conditions for such an extension to a general algebra
with a modulus have been treated by G. Scheffers <math>\S</math>; let <math>f_1, ..., f_n</math> be
continuous functions of <math>x_1, ..., x_n</math>; in order that <math>f = \sum f_i e_i</math> shall have
a unique derivative independent of <math>dx_1, ..., dx_n</math>, multiplication must be
commutative; in order that the derivatives and integrals of analytic
functions as defined shall be analytic, multiplication must also be asso-
ciative. A different extension was based by F. Hausdorff upon the
number of linearly independent expressions <math>\sum a_i x b_i</math>, where the a's and
b's are fixed numbers of the algebra.
* Wedderburn, l.c., pp. 86, 112; Epsteen, Trans. Amer. Math. Soc., vol. 4
(1903), p. 444.
+ G. Scheffers, Math. Ann., vol. 41 (1893), p. 601, for the case of the field of
complex numbers. His proof rests upon an incorrect inference (top of p. 603),
mentioned in the second foot-note to § 39 in this tract.
# Study, Monatshefte Math. u. Phys., vol. 2 (1891), p. 44; Scheffers, Math.
Ann., vol. 39 (1891), p. 319.
§ Paris Comp. Rend., 116 (1893), pp. 1114, 1242; Leipzig Berichte, vol. 45
(1893), math., p. 828; vol. 46 (1894), p. 120.
| Leipzig Ber., vol. 52 (1900), math., p. 45. Cf. L. Autonne, Paris Comptes
Rendus, 142 (1906), p. 1183; Journ. de Math., ser. 6, vol. 3 (1907), p. 53.

## PDF page 86

Cambridge:
PRINTED BY JOHN CLAY, M.A.
AT THE UNIVERSITY PRESS
.
٠

## PDF page 87

.

## PDF page 88



## PDF page 89

3
1

1

ACCESSED AND DESCRIPTION OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF THE PARTY OF
1

.
19
1
1
5

## PDF page 90

.
1
.
-
٠
.
.
.
.
.
.

## PDF page 91

QA
Dickson, Leonard Eugene
251
Linear algebras
D5
Physical &
Applied Sci.
PLEASE DO NOT REMOVE
CARDS OR SLIPS FROM THIS POCKET
UNIVERSITY OF TORONTO LIBRARY

## PDF page 92

,d.,
100








2 15

11.5
......
