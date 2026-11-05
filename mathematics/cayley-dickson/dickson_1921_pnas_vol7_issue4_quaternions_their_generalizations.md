Source: see manifest row of the PDF
PDF sha256: 12b43ef32e16c7f274e791cda39b1b5b6a752ebd2c64370b34224978d9541804
License: public domain (PNAS vol. 7 no. 4, published in the United States in 1921)

# Transcription of dickson_1921_pnas_vol7_issue4_quaternions_their_generalizations.pdf

Transcription of `dickson_1921_pnas_vol7_issue4_quaternions_their_generalizations.pdf` in this directory, 25 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 1-25 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories. No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

<b>PROCEEDINGS</b>
OF THE
NATIONAL ACADEMY OF SCIENCES
APRIL 15, 1921
Volume 7
Number 4
QUATERNIONS AND THEIR GENERALIZATIONS
By LEONARD EUGENE DICKSON
DEPARTMENT OF MATHEMATICS, UNIVERSITY OF CHICAGO
Read before the Academy, April 26, 1921
1. The discovery of quaternions by W. R. Hamilton in 1843 has led
to an extensive theory of linear algebras (or closed systems of hyper-
complex numbers) in which the quaternion algebra plays an important
rôle. Frobenius1 proved that the only real linear associative algebras
in which a product is zero only when one factor is zero are the real number
system, the ordinary complex number system, and the algebra of real
quaternions. A much simpler proof has been given by the writer.2 Later,
the writer3 was led to quaternions very naturally by means of the four-
parameter continuous group which leaves unaltered each line of a set
of rulings on the quadric surface <math>x_1^2 + x_2^3 + x_3^4 + x_4^5 = 0</math>.
The object of the present note is to derive the algebra of quaternions
and its direct generalizations without assuming the associative or com-
mutative law. I shall obtain this interesting result by two distinct
methods.
2. The term field will be employed here to designate any set of ordinary
complex numbers which is closed under addition, subtraction, multipli-
cation, and division. Thus all complex numbers form a field, likewise
all real numbers, or all rational numbers.
Just as a couple <math>(a, b)</math> of real numbers defines an ordinary complex
number <math>a + bi</math>, where <math>i^2 = -1</math>, so also an <i>n</i>-tuple <math>(x_1, ..., x_n)</math> of numbers
of a field F defines a hypercomplex number
<math>x = x_1e_1 + x_2e_2 + \ldots + x_ne_n</math>
(1)
where the units <math>e_1, \ldots, e_n</math> are linearly independent with respect to the
field <math>F</math> and possess a multiplaction table
<math display="block">e_i e_j = \sum_{k=1} \gamma_{ijk} e_k</math>
<math display="block">(i, j = 1, \ldots, n),</math>
(2)
109

## PDF page 2

110
MATHEMATICS: L. E. DICKSON
Proc. N. A. S.
n which the <math>\gamma</math>'s are numbers of <math>F</math>. Let <math>x' = \sum x_i e_i</math> be another hypercom-
plex number whose coördinates <math>x_i</math> are numbers of <math>F</math>. Then shall
<math>xx' = \sum x_i x_j' \cdot e_i e_j, \ x = x' = \sum (x_i = x_i') e_i, \ fx = xf = \sum fx_i \cdot e_i,</math>
when <math>f</math> is in <math>F</math>, so that multiplication is distributive. Under these assump-
tions, the set of all numbers <math>(1)</math> with coördinates in <math>F</math> shall be called a
linear algebra over F.
3. We assume that <math>e_1</math> is a principal unit (modulus), so that <math>e_1x = xe_1 = x</math>
for every number <math>x</math> of the algebra, and write 1 for <math>e_1</math>. We assume that
every number of the algebra satisfies a quadratic equation with coefficients
in F. If <math>e^2 + 2ae + b = 0</math>, <math>(e + a)^2 = a^2 - b</math>, so that we may take
the units to be 1, <math>E_2, \ldots, E_n</math>, where <math>E_i^i = s_{ii}</math>, a number of <math>F</math>. For <math>i</math> and
j distinct and >1, <math>E_i = E_j</math> satisfies a quadratic, so that <math>(E_i = E_j)^2 =</math>
<math>s_{ii} + s_{jj} = (E_i E_j + E_j E_i)</math> is a linear function of <math>E_i = E_j</math>. Thus <math>E_i E_j + E_j E_i</math>
<math>E_i E_i</math> is a linear function of <math>E_i + E_j</math> and of <math>E_i - E_j</math>, and hence is a number
<math display="block">2s_{ij} = 2s_{ji} \text{ of } F.</math>
Let <math>u_2, \ldots, u_n</math> be arbitrary numbers of <math>F</math> and write <math>U = \sum u_k E_k</math>.
Then
<math>U^2</math> equals
<math display="block">Q = \sum s_{kl} u_k n_l.</math>
It is a standard theorem that Q can be reduced to <math>\Sigma c_i v_i^2</math> by a linear trans-
formation <math>u_k = \sum a_k v_l</math> with coefficients in F and of determinant <math>\pm 0</math>.
Write
<math display="block">e_l = \sum a_{kl} E_k</math>
<math display="block">(l=2,\ldots,n).</math>
Then <math>1, e_1, \ldots, e_n</math> are linearly independent and may be taken as the new
units of our algebra over <math>F</math>. Then
<math display="block">U = \sum_{k,l} a_{kl} v_l E_k = \sum_l v_l e_l,</math>
<math display="block">U^2 = \sum_{k,l} v_k v_l e_k e_l = \sum_i c_i v_i^2.</math>
Hence
<math>e_i^1 = c_i, e_i e_j + e_j e_i = 0</math>  <math>(i, j = 2, ..., n, i \neq j).</math>
(3)
4. Write <math>x = x_1 + \sum x_i e_i</math>. Then <math>(x - x_1)^2 = \sum c_i x_i^2</math>. This gives <math>xx' =</math>
<math>x'x = \sigma</math>, where

## PDF page 3

111
Vol. 7, 1921
MATHEMATICS: L. E. DICKSON
<math>x' = 2x_1 - x = x_1 - \sum_{i=1}^{n} x_i e_i, \ \sigma = x_1^2 - \sum_{i=1}^{n} c_i x_i^2.</math>
We shall call x' the conjugate to x and <math>\sigma = \sigma(x)</math> the norm of x. Hence
the product of any number and its conjugate in either order equals its
norm. We assume that the norm of a product equals the product of the
norms of the factors:
<math>\sigma(x)\sigma(\xi) = \sigma(X)</math>, if <math>x\xi = X</math>,
(4)
and shall investigate the resulting types of linear algebras. We assume
also that each <math>c_i \neq 0</math> in (3).
5. By (2) the coördinates of <math>X = x\xi</math> are <math>X_k = \sum x_i \xi_j \gamma_{ijk}</math>. Since <math>e_i^2 = c_i</math>,
we have <math>\gamma_{ii1} = c_i</math>, <math>\gamma_{iik} = 0</math> <math>(i>1, k>1)</math>. Hence
<math display="block">X_1 = x_1 \xi_1 + \sum x_i \xi_i c_i + \sum x_i \xi_j \gamma_{ij1},</math>
<math display="block">X_k = x_1 \xi_k + x_k \xi_1 + \sum x_i \xi_j \gamma_{ijk}. \quad (5)</math>
<math>i,j=2</math>
(k > 1)
Since this transformation is the identity <math>X = x</math> if <math>\xi = 1</math>, we obtain an
infinitesimal transformation by taking <math>\xi_1 = 1</math>, <math>\xi_j = \delta t</math>, <math>\xi_i = 0(i \pm 1, j)</math>:
<math display="block">\delta x_1 = X_1 - x_1 = \left\{ c_j x_j + \sum_{i=2} \gamma_{ij1} x_i \right\} \delta t, \delta x_j = \left\{ x_1 + \sum_{i=2} y_{ijj} x_i \right\} \delta t,</math>
<math>i=2</math>
<math>i \pm j</math>
<math display="block">\delta x_k = \left\{ \sum_{i=1}^n \gamma_{ijk} x_i \right\} \delta t \qquad (k \neq 1, j). \quad (6)</math>
For these <math>\xi</math>'s, <math>\sigma(\xi)</math> is unity to within an infinitesimal of the second order.
Hence the increment to <math>\sigma(x)</math> must vanish identically, so that
<math>
\gamma_{ij1} = \gamma_{ijj} = \gamma_{iji} = 0
</math>
(1, i, j distinct),
<math display="block">
c_k \gamma_{ijk} + c_i \gamma_{kji} = 0
</math>
(1, i, j, k distinct).
(8)
By (7), (5) simplifies to
<math display="block">X_1 = x_1 \xi_1 + \sum_{i} x_i \xi_i c_i, X_k = x_1 \xi_k + x_k \xi_1 + \sum_{i} x_i \xi_i \gamma_{ijk} \ (k > 1),</math>
(9)
where, in the final sum, <math>i</math> and <math>j</math> range over distinct values from <math>2, \ldots, n</math>,
excluding k. This final sum is, therefore, absent if <math>n=3</math>; whence <math>\sigma(X)</math>

## PDF page 4

MATHEMATICS: L. E. DICKSON
Proc. N. A. S.
112
has the term <math>2x_2\xi_2c_2.x_3\xi_3c_3</math> which does not occur in <math>\sigma(x)\sigma(\xi)</math>.
But c2c2 =0
by hypothesis. Hence <math>n > 3</math>.
Hitherto we have not examined the conditions which follow from the
final equations (3); these are
<math>\gamma_{iik} = -\gamma_{ijk} \quad (i, j = 2, ..., n; i \neq i).</math>
(10)
6. Taking <math>n = 4</math> and applying (10), we see that (9) become
<math display="block">\int X_1 = x_1 \xi_1 + c_2 x_2 \xi_2 + c_3 x_3 \xi_3 + c_4 x_4 \xi_4, X_2 = x_1 \xi_2 + x_2 \xi_1 + \gamma_{342} (x_3 \xi_4 - x_4 \xi_3),</math>
(11)
<math display="block">X_3 = x_1\xi_3 + x_3\xi_1 + \gamma_{243}(x_2\xi_4 - x_4\xi_1), X_4 = x_1\xi_4 + x_4\xi_1 + \gamma_{224}(x_2\xi_3 - x_3\xi_2).</math>
These transformations do not in general form a group and hence are not
generated by the corresponding infinitesimal transformations employed
above. Hence it remains to require that <math>\sigma(X) = \sigma(x)\sigma(\xi)</math> under the
transformations (11). The conditions are seen to be
<math>c_3c_4 = -c_2\gamma^2 s_{42}, c_2c_4 = -c_3\gamma^2 s_{43}, c_2c_3 = -c_4\gamma^2 s_{234}, c_4\gamma_{234} = c_2\gamma_{342} = -c_3\gamma_{243},</math>
the first two of which reduce to the third by means of the last three equa-
To these last can be reduced all the conditions <math>(8)</math> by means of <math>(10)</math>.
tions.
Applying the transformation of variables which multiplies <math>x_4</math>, <math>\xi_4</math>, <math>X_4</math>
by <math>\gamma_{224}</math>, and leaves the remaining <math>x_i</math>, <math>\xi_i</math>, <math>X_i</math> unaltered, we get
<math display="block">(X_1 = x_1\xi_1 + c_2x_2\xi_2 + c_3x_3\xi_3 - c_2c_3x_4\xi_4, X_2 = x_1\xi_2 + x_2\xi_1 - c_3x_3\xi_4 + c_3x_4\xi_3,</math>
<math>(11^{1})</math>
<math>X_3 = x_1\xi_3 + x_2\xi_1 + c_2x_2\xi_4 - c_2x_4\xi_2</math>, <math>X_4 = x_1\xi_4 + x_4\xi_1 + x_2\xi_2 - x_3\xi_2</math>.
These are the values obtained by Lagrange in his generalization <math>\sigma(x)\sigma(\xi) =</math>
<math>\sigma(X)</math> of Euler's formula for the product of two sums of four squares.
Then <math>x\xi = X</math> gives the following multiplication table for the units:
<math display="block">\int e_1^1 = c_2, \ e_1^2 = c_3, \ e_4^2 = -c_2c_3, \ e_2e_3 = e_4, \ e_3e_2 = -e_4,</math>
(12)
<math display="block">\begin{cases} e_2e_4 = c_2e_3, \ e_4e_2 = -c_2e_3, \ e_3e_4 = -c_3e_2, \ e_4e_3 = c_3e_2. \end{cases}</math>
This algebra is associative and is the direct generalization of quaternions
to a general field F which the writer obtained elsewhere from assump-
tions including associativity. The four-rowed determinants of the general
number x of this algebra equals <math>\sigma^2(x)</math>. The case <math>c_2 = c_3 = -1</math> gives the
algebra of quaternions, for which it is customary to write i, j, k instead
of our units e2, e2, e4.
7. It is not very laborious to show by the above method that the cases
<math>n = 5</math> and <math>n = 6</math> are excluded. However, Hurwitz has proved that a
relation of the form <math>\sigma(x)\sigma(\xi) = \sigma(X)</math> is impossible if <math>n \neq 1, 2, 4, 8</math>. A
slight simplification of his proof, together with an account of the history
of this problem, has been given by the writer.7 Hurwitz made no attempt
to find all solutions when <math>n = 4</math>. We proceed to treat this problem.
Consider the case <math>c_i = -1</math> to which the general case may be reduced
by an irrational transformation. Then <math>\sigma(x) = \sum x_i^2</math>. We investigate
the linear algebras having property (4), i. e.,
<math>(x_1^2 + \ldots + x_n^2)(\xi_1^2 + \ldots + \xi_n^2) = X_1^2 + \ldots + X_n^2</math>
(13)

## PDF page 5

113
MATHEMATICS: L. E. DICKSON
Vol. 7, 1921
if
<math display="block">X_k = \sum_{i=1}^{n} \left(\sum_{j=1}^{n} \gamma_{ijk} x_i\right) \xi_j \qquad (k = 1, ..., n). </math> (14)
The matrix M of this substitution has the element <math>\sum_{i=1}^{i=n} \gamma_{ijk} x_i</math> in the kth
row and jth column. If this substitution is applied to a quadratic form
in <math>X_1, \ldots, X_n</math> of matrix Q, it is a standard theorem that we obtain a quadratic
form in <math>\xi_1, \ldots, \xi_n</math>, whose matrix is <math>M'QM</math>, where <math>M'</math> is the transposed
of <math>M</math>, being obtained from <math>M</math> by the interchange of its rows and columns.
In our problem, <math>Q</math> is the identity matrix <math>I</math> whose elements are all zero
except the diagonal elements which are 1. Hence, by (13),
<math display="block">M'M = (x_1^2 + \ldots + x_n^2)I.</math>
(15)
When a homogeneous polynomial <math>\sigma(x_1, \ldots, x_n)</math> of any degree has the
property (4) of possessing a theorem of multiplication, the writer<sup>8</sup> has
proved that we may apply a linear transformation on <math>x_1, \ldots, x_n</math> which
leave <math>\sigma(x)</math> unaltered and one on <math>\xi_1, \ldots, \xi_n</math> which leaves <math>\sigma(\xi)</math> unaltered
such that the new algebra has the principal unit, <math>e_1</math>, so that <math>\gamma_{1jk}</math> and <math>\gamma_{j1k}</math>
are both 0 if <math>j \neq k</math>, and both unity if <math>j = k</math>.
Hence <math>M = x_1 M_1 + ... + x_n M_n</math>, where <math>\gamma_{ijk}</math> is the element in the
kth row and jth column of <math>M_i</math>, whence <math>M_i = I</math>. Thus (15) gives
<math>M'_{i} = -M_{i}, M'_{i}M_{i} = 1, M'_{i}M_{j} + M'_{j}M_{i} = 0 \quad (i > 1, j > 1, j \neq i). </math> (16)
In view of the values of <math>\gamma_{jik}</math>, and <math>M_i^1 = -M_i</math>, we have, when <math>n = 4</math>,
<math display="block">M_2 = \begin{pmatrix} 0 & -1 & 0 & 0 \\ 1 & 0 & -\gamma_{223} & -\gamma_{224} \\ 0 & \gamma_{223} & 0 & -\gamma_{234} \end{pmatrix}, \qquad M_3 = \begin{pmatrix} 0 & 0 & -1 & 0 \\ 0 & 0 & -\gamma_{322} & -\gamma_{324} \\ 1 & \gamma_{323} & 0 & -\gamma_{334} \end{pmatrix},</math>
<math display="block">M_4 = \begin{pmatrix} 0 & 0 & 0 & -1 \\ 0 & 0 - \gamma_{423} - \gamma_{424} \\ 0 & \gamma_{423} & 0 & -\gamma_{434} \\ 1 & \gamma_{424} & \gamma_{434} & 0 \end{pmatrix}.</math>
By <math>M_iM_i = I</math>, we have <math>M^{2i} = -I</math>, which gives
<math>\gamma_{223} = \gamma_{224} = \gamma_{323} = \gamma_{334} = \gamma_{424} = \gamma_{434} = 0, \ \gamma^2 = \delta^2 = \epsilon^2 = 1,</math>
where <math>\gamma = \gamma_{234}</math>, <math>\delta = \gamma_{324}</math>, <math>\epsilon = \gamma_{423}</math>. Hence
<math display="block">M_{2} = \begin{pmatrix} 0 & -1 & 0 & 0 \\ 1 & 0 & 0 & 0 \\ 0 & 0 & 0 & -\gamma \end{pmatrix}, \quad M_{3} = \begin{pmatrix} 0 & 0 & -1 & 0 \\ 0 & 0 & 0 & -\delta \\ 1 & 0 & 0 & 0 \\ 0 & \delta & 0 & 0 \end{pmatrix}, \quad M_{4} = \begin{pmatrix} 0 & 0 & -1 \\ 0 & 0 & -\epsilon & 0 \\ 0 & \epsilon & 0 & 0 \end{pmatrix}. \quad (17)</math>
The final condition (16) states that <math>M_iM_j</math> is skew-symmetric. The
products M2M2, M2M4, M2M4 of matrices (17) are seen at once to be

## PDF page 6

114
ZOOLOGY: J. F. FULTON, JR.
Proc. N. A. S.
skew-symmetric if and only if <math>\delta = -\gamma</math>, <math>\epsilon = \gamma</math>, and then <math>M_2M_3 = \gamma M_4</math>,
<math>M_2M_4 = -\gamma M_3</math>, <math>M_3M_4 = \gamma M_2</math>. Writing i, j, k for <math>M_2</math>, <math>M_3</math>, <math>\gamma M_4</math>, we have
the multiplication table of quaternions. Or we may form the matrix
M and write <math>X_k</math> for the sum of the products of the elements of its kth
row by <math>\xi_1, \ldots, \xi_4</math>, and take <math>\gamma = 1</math> (by multiplying <math>x_4, \xi_4, X_4</math> by <math>\gamma</math>); we
obtain (11') for <math>c_2 = c_3 = -1</math>. Hence we have again obtained the quatern-
ion algebra without assuming the associative law. The case <math>n = 8</math> is
being investigated in this way by one of my students.
<sup>1</sup> Frobenius, Jour. für Math., 84, 1878 (59).
Dickson, Linear Algebras, "Cambridge Tracts in Mathematics and Mathematical
Physics," No. 16, 1914 (10-12).
<sup>3</sup> Dickson, Bull. Amer. Math. Soc., 22, 1915 (53-61).
<sup>4</sup> By (7), <math>e_2e_3 = e_3e_2 = 0</math>.
Lagrange, Nouv. Mém. Acad. Roy. Sc. de Berlin, année 1770, Berlin, 1772 (123-133);
Oeuvres de Lagrange, 3, 1869 (189). Reproduced in Dickson's History of the Theory
of Numbers, II, 1920 (279-281).
6 Dickson, Trans. Amer. Math. Soc., 13, 1912 (65).
Dickson, Annals of Math., 20, 1919 (155-171, 297).
Dickson, Comptes Rendus du Congrès Internat. Math., Strasbourg, 1920 (131–146).
NOVOCAINE AS A SUBSTITUTE FOR CURARE<sup>1</sup>
By John F. Fulton, Jr.
HARVARD UNIVERSITY
Communicated by G. H. Parker, March 3, 1921
Since the recent war, the need of a substitute for the Indian arrow poison,
curare, has been keenly felt in many physiological laboratories. While
investigating the activity of certain local anesthetics, it was found that
novocaine, in its effect upon the neuro-muscular mechanism of frogs,
duplicates in many particulars the unique action of curare.
If the sciatic nerve of a sciatic-gastrocnemius preparation is bathed in
a strong solution of novocaine (2.5 per cent in water or in physiological
salt solution) for as long as twenty minutes, no decrease in its conduc-
tivity can be observed. However, if the muscle itself is bathed in such a
solution (by direct immersion or, "painting" with a camel's hair brush) the
power of reacting to nervous stimulation is destroyed within three to
five minutes, though ability to respond by contraction to direct electrical
stimulation remains unimpaired. Thus, in the action of novocaine there
is a complete duplication of the properties originally described by Claude
Bernard for curare.
Whether novocaine acts directly upon the end-plates of the motor
fibers or upon some membrane intermediate between the plates and the
Contributions from the Zoölogical Laboratory of the Museum of Comparative
Zoölogy at Harvard College. No. 330.

## PDF page 7

115
Vol. 7, 1921
PHYSICS: E. W. WASHBURN
muscle has not been determined. A dye that I have made by linking
novocaine with a benzene nucleus was found to be physiologically active,
like the 2.5% novocaine, and appears to stain the elements acted upon by
the novocaine. When the stain is diazotized directly into the living muscle,
by putting the tissue first into novocaine and then into a solution of the
staining base, only the muscle nuclei take the stain deeply, the nervous
elements of the end-plates as well as the motor fibers remaining uncolored.
It seems reasonably certain, therefore, that novocaine acts upon some
constituent of the neuro-muscular mechanism beyond the end-plates.
The significance of the affinity of the dye for the muscle nuclei is as yet
unknown. The object of this note is to direct the attention of physiologists
to a convenient substitute for curare.
NOTE ON A METHOD OF DETERMINING THE DISTRIBUTION
OF PORE SIZES IN A POROUS MATERIAL
BY EDWARD W. WASHBURN
DEPARTMENT OF CERAMIC ENGINEERING, UNIVERSITY OF ILLINOIS
Communicated by W. A. Noyes, February 12, 1921
The pressure required to force mercury into a capillary pore of radius,
r, is <math>\frac{-2\gamma\cos\theta}{\theta}</math>, where <math>\gamma</math> is the surface tension and <math>\theta</math> the angle of contact.
Upon this relation can be based a method for determining the effective
pore diameters in a porous material such as charcoal. If pores of various
diameters are present, one may determine also the fraction of the total
porosity which is due to pores having effective diameters lying between
any two stated limits. The procedure would be as follows:
The coarsely granular sample of the thoroughly outgassed material is
weighed and placed in a steel pressure bomb which is then evacuated
until all adsorbed gases are removed. Pure mercury is then admitted to
fill the bomb and a series of pressure and volume measurements are made
at various pressures up to the highest pressure it is desired to employ.
The decrease in volume, <math>\Delta V</math>, accompanying a small pressure increase
of <math>\Delta p</math>, in any part of the range must evidently be due to the filling of
pores whose effective radii lie between the limits <math>r</math> and <math>r - \Delta r</math>, or
<math display="block">\frac{\Delta r}{\Delta p} = \frac{-2\gamma \cos \theta}{p^2}.</math>
A blank experiment without the porous material should of course be
made in order to correct for the compressibility of the mercury and the
expansion of the bomb under pressure. For accurate results the com-
pressibility of the porous material, and the variation of <math>\gamma</math> and <math>\theta</math> with <math>p</math>
should also be known.
relies that a home source is the capturies

## PDF page 8

116
PHYSICS: A. F. BLAKESLEE
Proc. N. A. S.
The value of <math>\theta</math> could be determined from an X-ray photograph of a
mercury meniscus in a capillary composed of the material under exam-
ination, or by the drop-shape method.
AN APPARENT CASE OF NON-MENDELIAN INHERITANCE
IN DATURA DUE TO A DISEASE
BY ALBERT F. BLAKESLEE
STATION FOR EXPERIMENTAL EVOLUTION, COLD SPRING HARBOR, N. Y.
Communicated by C. B. Davenport, February 26, 1921
In the common Jimson Weed (Datura Stramonium), spiny or armed
capsules are dominant to smooth or inermis capsules. A cross between
two plants, each homozygous for a single member of this pair of characters
will produce spiny fruited offspring in the <math>F_1</math> and a ratio of 3 spiny to 1
smooth plant in the <math>F_2</math> generation.
In 1915, the writer found a single inermis plant in a culture where smooth
capsules could not have occurred through segregation. It was considered
a new inermis mutation and its inheritance was therefore studied in crosses
with normals.
The new form was called Quercina on account of the increased oak-like
dentation of its leaves. The most conspicuous character on the mature
plant was the partial or complete suppression of spines on the capsules.
An examination of the plants throughout the growing and flowering con-
dition indicated that other parts of the plant were also involved and
showed such changes as the slitting of the normally undivided corolla,
the absence of pollen, which caused the plant to depend upon outcrossing
in order to set seed, and certain other characters associated with less
vigorous growth.
Later investigation showed that the Ouercina character occurred spon-
taneously in the garden cultures in many ways like a vegetative mutation.
In a single year's test, about <math>1^{1}/_{4}</math> per cent of the normal plants in the field
took on the Quercina character by the last of the season. This Quercina
character generally shows itself weakly in a single branch and gradually
spreads to all the new growth. It occasionally happens on plants which
are acquiring the Quercina character that capsules will be found in a
transitional condition with their spines only partially reduced. Some-
times some of the valves may be entirely smooth and others on the same
capsule fully spined.
So far as we can judge from the literature, other investigators who have
worked on the Jimson Weed found have Quercina plants in their cultures.
They seem not to have noticed, however, any of the distinctive characters
other than those shown by the capsules.

## PDF page 9

PHYSICS: A. F. BLAKESLEE
117
Vol. 7, 1921
Naudin<sup>1</sup> reports in an F<sub>1</sub> between an inermis variety (D. laevis) of
D. Stramonium and the armed type, that while most of the plants had
spiny fruits, others had fruits with reduced spines. Many of the capsules
on three out of the forty plants in this generation were very spiny on part
of the surface while totally smooth on the rest. Naudin believed that they
united thus by distinct and separate compartments the distinctive traits
of the parental types D. laevis and D. Stramonium. He calls this "hy-
bridité disjointe" and cites in this connection the condition in the graft
chimera Cytisus Adami. In a series of <math>F_2</math> plants from the same original cross
Naudin found 6 individuals out of 38 which again showed more or less
well marked his "hybridité disjointe" and which were presumably
Quercinas.
Godron<sup>2</sup> reports finding capsules partly spiny and partly smooth. He
objects, however, to Naudin's interpretation that the separation of the
fruit into smooth and spiny portions is due to their origin from smooth and
spiny parents, since he says that he has found this condition when both
parents had spines.
Bateson and Saunders,3 after discussing the intermediate color of the
flowers in the <math>F_1</math> between white and purple flowered forms, say: "The
occurrence of intermediate forms was also occasionally noticeable in the
fruits. Among the large number of capsules examined, there were some
of the mosaic type, in which part of the capsule was prickly and the re-
mainder smooth, while others suggesting a blend, were more or less prickly
all over, but the prickles were much reduced in size, and often formed
mere tubercles. These mosaics occurred as rareties both on prickly in-
dividuals and on smooth ones still more rarely." Further evidence point-
ing to the Quercina nature of these abnormal capsules is given in their
following statement: "Such intermediate fruits were most often found
towards the end of the flowering season."
It may be stated that the writer has grown many thousand plants of
the Jimson Weed, including large numbers of individuals that were hetero-
zygous for inermis capsules, but has never observed any except Quercinas
which showed a mosaic arrangement of the spines on the fruits, with some
valves smooth and others more or less spiny. Despite their misconception
of the nature of the phenomenon which they observed, it is highly prob-
able that the investigators mentioned were describing the same type of
plant that we have considered under the term Quercina.
The Quercina character does not breed true. It is transmitted by seed
to about 79 per cent of its offspring when pollinated from normal plants.
The remaining 21 per cent normal offspring do not produce Quercina
seedlings in the next generation, and hence do not carry the character in
a recessive condition.

## PDF page 10

118
PHYSICS: A. F. BLAKESLEE
Proc. N. A. S.
Two plants which were changing over from a normal to a Quercina con-
dition were investigated with regard to the type of offspring obtained from
their individual capsules. There seems to be only a rough correspondence
between the strength of the Quercina character in the parent and the
number of Quercina plants in its offspring.
As has been stated already, Quercina flowers are characteristically de-
void of pollen. In a few plants, however, which were becoming trans-
formed into Quercinas, pollen was obtained and used in crosses onto normal
plants. Quercina offspring were obtained from such crosses showing that
the character in question can be transmitted through the male.
The non-Mendelian nature of the breeding results with Quercina plants
as well as the spontaneous occurrence of the character on branches of
normal plants and its spread to the new growth suggested the desirability
of attempting to transmit the character by grafting. This attempt was
entirely successful and Quercina cions grafted onto normal plants of the
Jimson Weed causes the new growth of the stock to take on the appear-
ance of Quercina. There is ample evidence, therefore, to indicate that the
cause of the Quercina complex, which by ourselves as well as by earlier
investigators had been supposed to be a manifestation of a genetic char-
acter, is in fact a disease transmissible by grafting.
It has not been found possible to infect plants artificially by rubbing
with diseased leaves nor by inoculation of expressed juice from Quercina
plants.
The profound morphological changes brought about in the leaves and
especially in the flowers and fruit are such that Quercina individuals would
be considered worthy of specific if not of generic separation if 100 per cent
of the seedlings instead of only 79 per cent came true to the Quercina com-
plex. As the facts stand, however, there is much in the behavior of
Ouercina plants which suggests genetic phenomena.
To one who has read the data presented in the foregoing pages, certain
similarities may be apparent between the Quercina in the Jimson Weed
and rogues in peas investigated by Bateson and Pellew.4 It will not be
desirable, however, to discuss the two forms more in detail until grafting
experiments with the rogues in peas have given definite results.
A detailed account of the Quercina disease with photographs will appear
shortly in the Journal of Genetics.
<sup>1</sup> Naudin, Ch., Nouvelles Recherches sur L'Hybridité dans les Végétaux, Nouv.
Arch. Mus., 1, 1865 (41-54).
<sup>2</sup> Godron, D. A., Des hybrides et des metis de Datura., Nancy, 1873 (1-75).
Bateson, W. and Saunders, E. R., Report to Evolution Committee of the Royal
Society, 1, 1902 (21–32).
Bateson, W. and Pellew, Caroline, "The Genetics of 'Rogues' among Culinary
Peas," Proc. Royal Soc., 91, 1920 (186-195).

## PDF page 11

119
PHYSIOLOGY: LANGWORTHY AND HOLMES
Vol. 7, 1921
THE EFFECT OF A VARIATION IN MILLING ON THE DIGESTI-
BILITY OF WHEAT FLOURS
By C. F. LANGWORTHY AND ARTHUR D. HOLMES
CONTRIBUTION FROM THE OFFICE OF HOME ECONOMICS, U. S. DEPARTMENT OF
AGRICULTURE
Communicated by W. A. Noyes, February 16, 1921
Introduction.—Cereals are almost universally the great source of carbo-
hydrate food in the human ration, and with moderate additions of fat
and protein they are capable of sustaining life and health over long periods
of time. They may be stored for years with little deterioration in quality,
are easily transported and yield the greatest amount of food for the labor
expended in producing them. Of the cereal grains, wheat, largely be-
cause of its gluten content which causes it to produce superior bread
making flour, has come to be considered as an almost indispensable article
of diet throughout Western Europe and America.
The normal, annual
per capita consumption of wheat in this country is approximately five
bushels.1 Valuable as wheat is in the human dietary in normal times, it
is even more important in times of stress, for a disturbance in the bread
supply has an immediate and often harmful effect on national morale.
The shortage in the food supply of the world in 1917 made the collec-
tion and correlation of data concerning human nutrition of utmost im-
portance and many matters were re-examined in the hope of providing
additional data of value. Extensive investigations of the chemical com-
position, digestibility, and nutritive value of wheat and wheat products
have been made by European investigators and in the United States.
Earlier investigations of this Office, undertaken with the cooperation of
the Maine and Minnesota Agricultural Experiment Stations, included
studies of the digestibility of wheat flours prepared under a variety of
milling conditions from wheat grown under uniform climatic, seasonal
and soil conditions. The results2 obtained showed that the protein of
white flour (72% extraction) was 88.1% digested, that of entire wheat
flour (85% extraction) was 81.9% digested, and that of graham flour
(100% extraction) was 76.9% digested. While the data were sufficient
to permit general conclusions regarding the effect of variation of milling
on digestibility, the unprecedented world shortage of food during the
World War made rigid economy in the use of food materials necessary
and in 1917 the U.S. Food Administration requested this Office to secure
additional data concerning the relative digestibility of flours representing
a series of extractions from the same lot of wheat. The results obtained
from the work thus undertaken were available to the Food Administration
during the war period. The findings, however, are not limited in their
application to special conditions under which the work was carried out but

## PDF page 12

120
PHYSIOLOGY: LANGWORTHY AND HOLMES PROC. N. A. S.
are of equal interest in the consideration of general problems of nutrition
and the economic utilization of the food supply under normal conditions.
The flours studied were prepared from the wheat mixture furnished to
the flour millers by the U.S. Grain Corporation late in 1917. It consisted
of the following:
20% choice hard spring (largely Marquis)
25% 58 lbs. spring
15% velvet chaff
25% slightly smutty spring
10% durum
5% Kansas and Oklahoma
At the request of the Food Administration the wheat was so milled by
commercial flour mills that a uniform series of extractions was obtained.
As required by the U.S. Food Administration regulations then in force,
the amount of wheat used was limited in the proportion of 264 lbs. of 58-lb.
wheat for 196 lbs. of flour. The milling data follow:
75% out of 72% extraction yielding 54% of the wheat
95% out of 74% extraction yielding 70% of the wheat
100% out of 85% extraction yielding 85% of the wheat
100% out of 100% extraction yielding 100% of the wheat
For the sake of convenience the above flours will be referred to accord-
ing to the percentage of the wheat extracted. Described in ordinary com-
mercial terms, the 54% flour contained only patent flour. The 70% ex-
traction, that is 95% of 74% extraction, is what is known commercially
as a 95% patent, or "standard patent" and contained patent, 1st clear,
and a small portion of the 2nd clear. The 85% flour corresponds to the
old-fashioned "whole-wheat" flour, and contained patent, 1st clear, 2nd
clear, Red Dog, and Shorts. The 100% flour corresponds to that known
formerly as graham flour and contained the entire wheat kernel.
These experiments were begun before the Food Administration had
adopted the milling of what was later known as "war flour." The latter
was sometimes known as "100% war flour," but this did not mean that
it contained 100% of the wheat. In milling the "war flour," 100 lbs.
of cleaned wheat was separated into two products: about 75 lbs. of flour
(never less than 74.3 lbs.) and about 25 lbs. of feed, giving a flour of about
75% extraction. The 95% patent or 70% extraction flour used in these
experiments was similar to the "war flour," save that 5% of low grade and
2nd clear stock had been removed to improve its bread-making quality.
Feeding experiments were conducted with healthy young men accord-
ing to the method commonly used by the Office of Home Economics in
studies of digestibility.8
In order to ascertain whether the subjects acquired during the period
of the experiments any increased tolerance for the coarser flours the squad

## PDF page 13

121
Vol. 7, 1921
PHYSIOLOGY: LANGWORTHY AND HOLMES
was divided into groups of five subjects each, and one group was served
the 54%, 70%, 85%, and 100% flours in the order given while the second
group was served the flours in the reverse order. The results of the 139
digestion experiments reported below do not indicate that the first group
of subjects acquired any tolerance for the coarser flours not possessed by
the second group which was served the coarser flours first.
The experimental diet was so chosen that its preparation should involve
a minimum of labor, that the bread should supply the larger portion of
the total protein, and that it should be representative of a simple mixed
diet. The diet consisted of bread, fruit (orange), butter, sugar, with tea
or coffee as a beverage if desired.
The fruit, butter, and sugar were served as purchased from a nearby
market. A quantity of bread sufficient to supply all the subjects for one
day was prepared daily, the ingredients being used in the following pro-
portion:
3 cups sifted flour
1 teaspoon salt
1 tablespoon sugar
1/8 to 1/2 cake yeast
1 tablespoon hydrogenated vegetable oil
1 cup water
While data relative to the digestibility of the diet as a whole are of value,
interest was primarily centered in the digestibility of the bread or rather
the flour from which the bread was made. The digestibility of the pro-
tein and carbohydrate supplied by the different breads has been estimated
by making a correction for the undigested protein and carbohydrate re-
sulting from the accessory foods by a method outlined in detail in earlier
publications.4 It has been assumed from the results of the early investi-
gations of this Office that the digestibility of the protein of butter is 97%
and protein of fruit, 85%; of the carbohydrate of fruit, 90%; and of sugar,
98%.
In planning the investigation, it was decided to make a sufficient number
of digestion experiments so that the average results obtained should be of
general application. The experimental periods were to be long enough
so that the effect of any irregularity in the rate of passage of food residues
through the alimentary tract, and any error in the separation or collec-
tion of feces would be practically negligible. The experimental periods
which were from 15 to 25 days in length were subdivided and considered
as separate three-day experiments, following one directly after the other.
The subjects for the experiments were students in local educational
institutions, and were selected with care in order that the conclusions might
be applicable to the average normal adult. An attempt was made to
include in the squad some accustomed to strenuous exercise, some ac-
customed to take light exercise, and some who took little recreation, in

## PDF page 14

122
PHYSIOLOGY: LANGWORTHY AND HOLMES PROC. N. A. S.
order to have under observation individuals whose peristaltic action was
normal and regular and others who had a tendency toward constipation.
Summary of Results.—The results obtained in the studies of 54%,
70%, 85%, and 100% flours are summarized in the table which follows:
TABLE 5
SUMMARY OF EXPERIMENTS ON THE DIGESTIBILITY OF WHEAT FLOURS
DIGESTIBILITY OF ENTIRE RATION
AVERAGE
DIGESTI-
DIGESTI-
AMOUNT
NUMBER
BILITY OF
KIND OF FLOUR
BILITY OF
OF BREAD
BREAD
USED IN PREPARA-
OF
BREAD
BATEN
CARBO-
TION OF BREAD
CARBO-
EXPTS.
PROTEIN
PROTEIN
FAT
PER MAN
HYDRATE
HYDRATE
PER DAY
PER CENT
PER CENT
PER CENT
PER CENT
PER CENT
GRAMS
87.7
99.7
54% flour
43
87.8
96.5
98.8
600
70% flour
90.1
99.0
90.1
99.9
42
564
96.1
85% flour
21
472
87.1
96.9
97.5
87.1
98.5
100% flour
33
84.2
93.9
95.0
84.2
94.4
663
In the above experiments the subjects ate on an average considerably
more than a pound of bread daily for periods of from 6 to 20 days without
producing any digestive disturbances, which indicates that wheat flours,
regardless of percentage of extraction, are well tolerated by the human body.
The coefficients of digestibility, obtained from the 139 digestion ex-
periments reported above, 87.7% for protein and 99.7% for carbohydrate
of 54% flour; 90.1% for protein and 99.9% for carbohydrate of 70% flour
(95% patent); 87.1% for protein and 98.5% for carbohydrate of 85%
("whole wheat") flour; and 84.2% for protein and 94.4% for carbohydrate
of 100% flour, show these flours to be well digested. From these results
it appears that the U.S. Food Administration in attempting to obtain
efficient utilization of the wheat supply secured did well to specify that
wheat should be milled at 75% extraction, that is an extraction similar
to the one which in these experiments showed the highest proportion of
digestible nutrients.
The digestibility of the fat content of the experimental diet was quite
uniform and was practically identical with that of butter and "shortening"6:
which comprised the major portion of the fat consumed, except in the series.
of experiments with 100% flour in which the fat was only 93.7% digested.
Attention was given to the effect of the different flours on peristaltic
The 54% and 70% flours did not tend to produce constipation
action.
during a period of 15 to 18 days, and although a somewhat freer movement
of the bowels resulted from the continued use of 85% and 100% flours:
no case of pronounced laxative effect was noted.

## PDF page 15

MATHEMATICS: E. V. HUNTINGTON
Vol. 7, 1921
123
In general the results of the digestion experiments here reported are in
accord with conclusions drawn from earlier studies of the digestibility of
wheat flours. The digestibility of the 70% (95% patent) flour was the
highest, that of the 54% flour was slightly greater than that of the 85%
("whole wheat") flour, while the digestibility of the 100% (graham) flour
was lowest of all those studied. Since the flavor of bread made with the
different flours varies, the use of different kinds for bread making is an easy
way of giving variety to the diet.
1 U. S. Dept. Agr., Bur. Crop Estimates, Monthly Crop Rept., 3, 1917, No. 10 (99).
<sup>2</sup> U. S. Dept. Agr., Office Expt. Sta. Bull. 85, 1900 (32-33); Bull. 101, 1901 (33);
Bull. 126, 1903 (29, 45); Bull. 143, 1904 (32); Bull. 156, 1905 (36).
<sup>3</sup> U. S. Dept. Agr., Bull. 310, 1915; 617, 1919; 717, 1919.
<sup>4</sup> U. S. Dept. Agr., Bull. 470, 1916 (7); 525, 1917 (4).
<sup>b</sup> Connecticut Storrs Sta. Rpt., 1899 (104).
<sup>6</sup> U. S. Dept. Agr., Bull. 310, 1915.
THE MATHEMATICAL THEORY OF THE APPORTION-
MENT OF REPRESENTATIVES
BY EDWARD V. HUNTINGTON
HARVARD UNIVERSITY, CAMBRIDGE, MASS.
Communicated by E. H. Moore, February 14, 1921
The Problem.—The exact quota to which each state is theoretically
entitled on the basis of population usually involves a fraction. The problem
is, to replace these exact quotas by whole numbers in such a way that the re-
sulting injustice (due to adjustment of the fractions) shall be as small as
possible.
This problem has been the subject of violent debate in Congress for
the past one hundred years, a new method of apportionment having been
proposed after almost every decennial census. None of these methods,
however, possesses any satisfactory mathematical justification. The
need of a strictly mathematical treatment of the problem having been
called to the writer's attention by Dr. J. A. Hill, Chief Statistician of
the Bureau of the Census, the following solution has been worked out on
the basis of two very simple postulates. The new method may be called
the Method of Equal Proportions.
Let N be the total number of representatives, <math>A, B, C, \ldots</math> the popula-
tions of the several states, and <math>a, b, c, \ldots</math> the number of representatives
assigned to each.
Fundamental Principle.—In a satisfactory apportionment between two
states (A greater than B), we shall agree that <math>A/a</math> and <math>B/b</math> should be as
nearly equal as possible; also <math>a/A</math> and <math>b/B</math>; also <math>A/B</math> and <math>a/b</math>; also <math>B/A</math>
and <math>b/a</math>.

## PDF page 16

124
MATHEMATICS: E. V. HUNTINGTON
Proc. N. A. S.
Now to say that two quantities are "nearly equal" may be interpreted
to mean: either, that the difference between the quantities is nearly zero;
or, that the ratio between them is nearly one.
(Here the difference "between" two quantities means the larger minus
the smaller. Similarly, the ratio "between" two quantities means the
larger divided by the smaller.)
If we adopt the "difference" interpretation, we have:
Postulate 1a. The difference between <math>A/a</math> and <math>B/b</math>; or
The difference between <math>a/A</math> and <math>b/B</math>; or
POSTULATE Ib.
The difference between <math>A/B</math> and <math>a/b</math>; or
POSTULATE Ic.
The difference between <math>B/A</math> and <math>b/a</math>; should be as near
POSTULATE Id.
zero as possible.
If, on the other hand, we adopt the "ratio" interpretation, we have:
POSTULATE I. The ratio between A/a and B/b (or the ratio between
<math>a/A</math> and <math>b/B</math>; or the ratio between <math>A/B</math> and <math>a/b</math>; or the ratio between <math>B/A</math>
and <math>b/a</math>; all of which have the same value) should be as near unity as possible.
Since there is no way of choosing, mathematically, between Postulates
Ia and Ib or between Postulates Ic and Id, and since these four demands
lead to four different results, we shall reject all four of them and adopt
Postulate I as the proper interpretation of our Fundamental Principle.
The case of two states is thus disposed of.
For the case of three or more states, one further principle is required,
which we state as follows:
POSTULATE II. In a satisfactory apportionment, there should be no pair
of states which is capable of being "improved" by a transfer of representa-
tives within that pair—the word "improvement" being understood in the
sense implied by the test already adopted for the case of two states, and
the rare cases of "no choice" being decided in favor of the larger state.
From these two postulates the following theorem can then be deduced:
THEOREM I. For any given values of A, B, C, ... and N, there will
always be one and only one satisfactory apportionment in the sense defined
by Postulates I and II. No further principles are required.
A working rule for computing this "best" apportionment in any given
case is found to be as follows:
Working Rule.—Multiply the population of each state by as many of
the numbers
Inf., <math>1/\sqrt{1 \times 2}</math>, <math>1/\sqrt{2 \times 3}</math>, <math>1/\sqrt{3 \times 4}</math>, ...
as may be necessary, and record each result, together with the name of
the state, on a small card. Arrange these cards according to the magni-
tude of the numbers recorded upon them, from the largest to the smallest,
thus forming a priority list for the given states (the cards marked "Inf."
being placed at the head of the list, arranged among themselves in order

## PDF page 17

MATHEMATICS: E. V. HUNTINGTON
125
Vol. 7, 1921
of magnitude of the populations of the states). Finally, assign the repre-
sentatives, from the 1st to the Nth, to the several states in the order in which
the names of the states occur in this priority list. (It should be noted that
this method satisfies automatically the constitutional requirement that
every state shall have at least one representative.)
This method may be called the "method of the geometric mean," since
the "multipliers" are the reciprocals of the geometric means of consecutive
integers.
The solution of the problem is thus complete.
Alternative Methods.—If we had adopted Postulate Ia or Ib we should
have been led, in like manner, to two other methods which may be called
the method of the harmonic mean (Ia), and the method of the arithmetic
mean (Ib), since the "multipliers" in the working rules are as follows:
(Ia) Inf., <math>\frac{1+2}{2(1\times 2)}</math>, <math>\frac{2+3}{2(2\times 3)}</math>, <math>\frac{3+4}{2(3\times 4)}</math>, ...
(Ib) 2, <math>2/3</math>, <math>2/5</math>, <math>2/7</math>, ...
It can be shown that method Ia favors the smaller states more than
method I does, while method Ib favors the larger states more than method
I does. Since there is no mathematical reason for adopting either of the
two Postulates Ia and Ib to the exclusion of the other, both should be re-
jected.
Postulates Ic and Id also determine two distinct methods, which may
be called the two methods of similarity ratios. It can be shown that Ic
favors the small states even more than Ia does, while Id favors the large
states even more than Ib does, so that both should be rejected.
Each of these four methods violates three of the four conditions ex-
pressed in our Fundamental Principle, while the method of the geometric
mean satisfies all these conditions simultaneously.
The following further methods are suggested by the Theory of Least
Squares.
In a theoretically perfect apportionment, <math>A/a</math> would be equal
to <math>P/N</math>, and <math>a/A</math> to <math>N/P</math> (where P is the total population). Hence,
in place of Postulates I and II, we might consider the following:
Postulate IIIa. The sum of the squares of the deviations of the <math>A/a</math>
from their true values; or
POSTULATE IIIb. The sum of the squares of the deviations of the a/A
from their true values; should be a minimum.
It can be shown, however, that IIIa favors the smaller states even more
than Ic does, while IIIb favors the larger states even more than Id does.
In other words, Postulates IIIa and IIIb violate, in opposite directions,
all four of the conditions expressed in our Fundamental Principle. Since
there is no mathematical reason for adopting either to the exclusion of
the other, both should be rejected.

## PDF page 18

126
MATHEMATICS: E. V. HUNTINGTON
Proc. N. A. S.
The same remark applies if in Postulates IIIa and IIIb the word "square"
is replaced by "absolute value."2
Hence it is clear that if a numerical measure of injustice is desired, both
the deviation of <math>A/a</math> and the deviation of <math>a/A</math> should be taken into ac-
count together. That is, any formula which reports <math>A/a</math>, say, as too
large by a certain amount, should also report <math>a/A</math> as too small by the same
amount. The formulas suggested by the simple application of the idea
of least squares, as shown in the preceding paragraph, do not have this
property. A combination of these formulas suggests, however, the follow-
ing postulate, in which <math>\alpha</math> denotes the theoretical value of a.
POSTULATE III. In a satisfactory apportionment, the sum T of terms
of the form Ae2 where
<math display="block">e = \frac{(a/A) - (\alpha/A)}{\sqrt{(a/A)(\alpha/A)}} = \frac{(A/a) - (A/a)}{\sqrt{(A/\alpha)(A/a)}} = \frac{a - \alpha}{\sqrt{a\alpha}}</math>
should be a minimum.3
For purposes of computation, this total error, T, may be replaced by
an average error, <math>E = \sqrt{S/N}</math>, where S is the sum of terms of the form
<math>\alpha e^2 - (a - \alpha)^2/a</math>.
The method determined by Postulate III is precisely the same as the
method of equal proportions based on Postulates I and II.
<sup>1</sup> This article contains the substance of two papers presented to the American Mathe-
matical Society, December 28, 1920, and February 26, 1921. Further details, with
proofs and examples, will be published either in the Transactions of the American
Mathematical Society, or in the Quarterly Publication of the American Statistical
Association, or in the American Mathematical Monthly.
For the history of the subject see W. F. Willcox, "The Apportionment of Repre-
sentatives" (presidential address at the annual meeting of the American Economic
Association, December 1915), published in the American Economic Review, Vol. 6,
No. 1, Supplement, pp. 1–16, March, 1916. See also 62d Congress, 1st Session, House
of Representatives, Report No. 12, pp. 1-108, April 25, 1911, and John H. Humphreys,
"Proportional Representation," London, 1911
The most important of the methods hitherto known are four:
The Vinton method of 1850, long in use in Congress, is known to lead to an "Alabama
paradox;" that is, an increase in the total size of the House may cause a decrease in the
representation of some state.
The Hill method of alternate ratios, proposed by Dr. J. A. Hill in 1910 but not adopted,
comes very near to satisfying the postulates of the present paper, and uses for the
first time (though only partially) the idea of the geometric mean. The method is in-
complete however, since it can be shown to lead to an Alabama paradox.
The Willcox method of major fractions, devised by Professor W. F. Willcox in 1900-
1910, and now in use in Congress, employs, in effect, a working rule like ours with
multipliers: Inf., <math>2/3</math>, <math>2/5</math>, <math>2/7</math>, ...; it is essentially the same as the method of the
arithmetic mean, and therefore favors the larger states unduly, just as the hitherto
unsuspected but equally justifiable method of the harmonic mean favors the smaller
states unduly. (It may be noted that the name "major fractions" is somewhat mis-
leading, since the Willcox major fraction is not a major fraction of the true quota, but

## PDF page 19

127
GENETICS: C. B. BRIDGES
Vol. 7, 1921
a major fraction of an artificial quota, scaled up or down from the true quota to meet
the requirements of the computation.)
The d'Hondt method, originated in Belgium and now widely used in European elec-
tions, employs "multipliers" 1, <math>1/2</math>, <math>1/3</math>, <math>1/4</math>... and can be shown to favor the larger
states to the extent of violating all four of the conditions expressed in our Fundamental
Principle.
<sup>2</sup> If one should try to minimize the sum of the squares (or the sum of the absolute values)
of the deviations of the a's themselves from their true values (with or without "weighting"
by the population of the state), the resulting methods would all lead to an Alabama
paradox. The same is true of the weighted sum of the absolute values of the deviations
of <math>a/A</math> (or of <math>A/a</math>). The same is also true of the absolute values of the logarithms of
the ratios between the a'S and their true values.
This Postulate III was added on April 23, after Professor F. W. Owens had shown
(at the meeting of the American Mathematical Society on February 26) that the
method of minimizing the sum of terms like <math>A[(a/A) - (\alpha/A)]^2</math> leads to the same
result as the Willcox method of major fractions. It may be noted that the method of
minimizing the sum of terms like <math>a[(A/a) - (A/a)]^2</math> leads, not as one might expect, to
the method of the harmonic mean, but to the method of the geometric mean.
CURRENT MAPS OF THE LOCATION OF THE MUTANT GENES
OF DROSOPHILA MELANOGASTER<sup>1</sup>
BY CALVIN B. BRIDGES
COLUMBIA UNIVERSITY, N. Y.
Communicated by T. H. Morgan, December 5, 1920
The maps that have been published<sup>2</sup> showing the distribution of the
mutant genes of D. melanogaster can now be much improved because
of the discovery of new mutants and the accumulation of crossover data.
Figure 1 gives in simplified form the maps that are in use in our laboratory.
The distances on the maps are based on the total amount of crossing
over between the loci, one unit of distance representing one per cent of
crossing over. The map-distances are the same as the observed crossover
values or "percentages of exchange" whenever the two loci considered
are so close together that no, or only a negligible amount of, double crossing
over occurs between them. In the first (X-) chromosome this practical
equivalence of map-distance and exchange-value holds for loci not farther
apart than about 15 units. In the middle of the second chromosome and
of the third chromosome the equivalence holds for only about 10 units.
In the end-regions of the second and third chromosomes it holds up to
nearly 20 units. For distances somewhat greater than these the map-
distances exceed the observed percentages of exchange by an amount equal
to twice the percentage of double crossing over between the given loci.
For still greater distances the difference includes also three times the per-
centage of triples. The number of quadruple crossovers is negligible
except perhaps when the whole length of the second chromosome is to

## PDF page 20

128
GENETICS: C. B. BRIDGES
PROC. N. A. S.
be considered. For each chromosome and for each region within a chromo-
some the amount of this multiple crossing over is characteristic, and may
not be the same in amount for different sections of equal map-distance.
Because of this variation, the accurate expression of the relation between
map-distance and exchange-values for the more distant loci, requires a
table of conversion corrections for each pair of loci considered. Such
tables will be published with the more detailed maps of the chromosomes.
In general, the correction is relatively slight with distances that are under
20-40, but for longer intervals the correction increases at an accelerated
rate. We have not met with percentages of exchange that exceed 50.0,
though two of the maps are about a hundred units long.
The map of the third chromosome is the most accurate, since the cal-
culation of the distances between the principal loci is made on the basis
of all data up to 1920, and an improved method of weighting and inter-
relating the data has been followed. Relatively little change in these
primary distances—the "triangulation" of the map—is expected with the
further accumulation of data. There is still some uncertainty with re-
gard to the region to the left of spineless, for the different sets of data
upon that region may not be comparable because of the possible presence
of crossover variations. The data used in the calculations for the primary
distances in the first and second chromosomes are homogeneous, and al-
though not including the last four years' work, are still fairly ample in
amount. Changes are to be expected when these two maps are recalcu-
lated with the improved method and complete data.
The most useful mutants are those that are separable from the wild-
type with completeness and ease, that are not inferior to the wild-type
in viability and productivity, and that do not interfere with the use in
the same experiment of any large class of the other mutant characters.
Dominants are more valuable than recessives. Mutants accurately
located in the chromosome are more valuable than those whose positions
are less well established, though if the other desirable features mentioned
above are present in a given new mutant the position will be found rather
quickly. A very large factor in the value of the mutant is its position
in the chromosome. The end positions are most valuable. Throughout
the remainder of the chromosome the most favorable positions are those
evenly spaced and just close enough together so that no double crossing
over occurs between them. If the interval is too small there is trouble
in getting double recessives, and the crossover classes are so small that
large totals are required to make differences significant.
The mutants that fulfill all the above requirements most nearly are
followed by an asterisk (*) in the maps. Their loci are the primary bases
with relation to which the other mutants are located. There are several
cases in which two or more excellent mutants affecting quite different

## PDF page 21

.
CONCESSION IN
CHRONOSOME_III
CHROMOSOME I
COMMISSION III.
telegraph
scute 0.02 e
yellow a<br>lethel 7
-2.0
0.6
star .
roughold .
0.0
0.0
0.0
bent .
aristaless
1.0
e #6,0 seelege
hite .
notch +
3.0
bnordel.
expanded .
4.0
5.5
echinus +
7.3
bifid .
9.0
truncate .
11.0
gull
13.0
pink-wing<br>streak +
13.7
crousveinless e
14.0
16.7
club
20.0
eut .
21.0
singed
22.5
oreem-b
sepia * bairy *
25.8
27.5
ten .
flipper
25.0
losenge .
dachs .
divergent
32.0
33.0
vermilion's
35.0
ski-II +
cream-III<br>dwarfoid<br>scarist
33.5
35.5
tiny-bristles<br>miniature<br>dusky +<br>furrowed
squat
36.0<br>36.1<br>37.5<br>38.0
禁:3
tilt<br>dichasts .
40.5
ascute<br>deformed
45.0<br>45.0<br>45.0<br>45.5
43.0
sable .
MALCOOD +
minute-6
44.0
curled<br>dwarf<br>pink
44.4
garnet +
46.7
black<br>jaunty
48.5
epterous
purploje
52.5
55.5.<br>54.5
smill-sing
53.8<br>54.0<br>55.0<br>36.0
two-bristle<br>spineless *<br>bitherax *<br>bitheraxeid
rudimentary
56.5<br>57.0<br>58.5<br>59.5
forked .
56.0
safranin
mall-eye -
39.0<br>60.0<br>60.5<br>61.0
glass • kidney giant spread
fused +
trefoil
61.0
63.5
delta .
65.0
vestigial .
65.0
cleft
65.5
hairless .
66.5
telescope<br>dash
67.5
band .
70.0<br>71.0
lobe .
70.0
CIII
minute-5II
white-ecolli *
72.0
73.5
ourved .
77.0
reef
minute-2
85.0
84.5
68.0
89.0
95.0
purploid
claret
37.7
plexus .
97.5
lethal-lia
100.8
brom, .
109.0
blistered
104.5<br>105.0<br>105.5
apeck<br>balloon
Fig. 1. Maps showing the distribution of mutant loci in the four chromosomes of
Drosophila melanogaster (Oct. 15, 1920).
[A † sign should be added to miniature (I,36.1) and gull (II,11.0), and a * sign to
black (II,46.5), speck (II,105.0), pink (III,45.5), and claret (III,95.4).]

## PDF page 22

130
GENETICS: C. B. BRIDGES
PROC. N. A. S.
regions of the body are located very close to one another (e.g., yellow and
scute, sable and garnet, forked and bar, sepia and hairy, hairless and
ebony, claret and minute). Of these neighboring mutants that one is
used which interferes least with the other characters in the particular
experiment, and the results of all such experiments are correlated by a
simple correction made possible by knowledge of the distance between the
loci. Such groups of loci, the members of which can be used as alternates,
are treated as one base in the construction of maps and in linkage work.
The mutants followed by a plus sign (+) are somewhat less valuable
in one or another respect, perhaps only in that of position.
Of the remaining mutants, not marked, some are exceedingly valuable
in special work. As an example of these may be mentioned CIII, which
prevents practically all crossing over within the right half of the third
chromosome and thus is much used in holding other mutants in their
proper relations in balanced stocks and while making up multiple stocks.
But most of the unmarked mutants are those more difficult to separate,
of poor viability, or less accurately located. Thus the mutant bithorax,
which is located very close to spineless, has second rank and would be
used as an alternate to spineless if the relation between the loci were
accurately known. But the loci of these two mutants are so close to-
gether that as yet no double recessive has been obtained, and hence no
back-cross test of the order and distance between these two loci has been
made. Dominants, and recessives close to dominants, are easily and
accurately placed, but there may be an error of five or even more units
in the indicated positions of certain (unmarked or omitted) second-
chromosome recessives whose positions are as yet known only through
reference to a distant base. These are relatively unimportant mutants,
and since they are not very useful, there is little incentive to determine
their locations more accurately. The serial order of the loci marked
with an asterisk is certain, and in only a few cases are the positions of the
second-rank mutants likely to be shifted with the accumulation of data.
Most of the unmarked mutants have their proper position with respect
to the first and even second rank mutants, but their order with respect to
each other is often uncertain in the absence of direct tests.
About 25 of the mapped loci represent more than one mutant allelo-
morph; thus, there are twelve allelomorphs at the white locus, and three
to six allelomorphs at each of several other loci. Many of the mutants
are recurrent; e. g., vermilion, notch, and rudimentary have each arisen
independently on more than ten occasions.
It will be noticed that the mutant loci are not distributed at random
along the chromosome maps, but are more closely spaced at the left end
of the first, at both ends of the second, and throughout the mid-region
of the third. This massing may correspond to a like massing of the genetic

## PDF page 23

131
Vol. 7, 1921
GENETICS: C. B. BRIDGES
materials. When orthopteran chromosomes are in the extended phase
preceding their condensation as tetrads they may be seen to consist of
granules of unequal size distributed at unequal distances along the linin
thread, both granule size and spacing being characteristic and relatively
constant for a given chromosome. Another explanation of the uneven
spacing seems more probable: The amount of crossing over between
given loci, e. g., black and purple in the second chromosome, is known to
vary in a definite manner with the age of the mother, with temperature,
and with genetic modifiers of crossing over. Since a unit of map-distance
is thus known to represent different lengths of chromosome thread, the
regions in which loci appear relatively closely spaced may be regions
in which one unit of map distance represents a longer section of chromosome
than in those regions that appear relatively unoccupied. - It may be sup-
posed that each region of chromosome has its characteristic relation be-
tween unit of map-distance and corresponding length of chromosome.
It is probably significant that in the second and third chromosomes the
distribution of mutant loci is approximately symmetrical about their mid-
points, for these chromosomes are V-shaped with median attachment
of the spindle fibre, while the first chromosome, which has the massing
at one end, has terminal attachment. The variations, from region to region,
in the proportion of double crossing over, referred to above, show a dis-
tribution that is symmetrical in the second and third chromosomes. From
this and other evidence it is probable that there is a definite relation be-
tween the region of chromosome, considered morphologically, and the
variations in the ratio of map-unit to length of chromosome thread.
When the different chromosomes are compared the average ratios are
found to be practically the same for all. Thus, the lengths of chromosomes
as measured directly in metaphase plates are in the ratio of 100: 159: 159:
12, while the known lengths of the chromosomes as mapped are in the
ratio of 100: 165: 155: 2.8 This is a surprisingly close agreement
between the observed lengths of the condensed chromosomes and their
lengths in terms of map-units.
<sup>1</sup> Contribution from the Carnegie Institution of Washington.
The maps in the frontispiece of the Mechanism of Mendelian Heredity were made
in 1914, and are both incomplete and out of proportion. A new frontispiece, practically
the same as the figure accompanying this paper, has been supplied for a revision of
the Mechanism and for a French edition. A similar figure is to appear in a book by
Dr. Sharp of Cornell. The best of the earlier maps of the first chromosome is that
given in Carnegie Institution Publication No. 237, p. 22. Partial maps of the first
chromosome that are more modern have been given in connection with special papers
(Genetics, 1, 1916 (8); Amer. Nat., 1916 (421); J. Gen. Physiol., 1919 (646). A map of
the second chromosome, complete to 1916, is given in Carnegie Institution Publication
No. 278, p. 303. No satisfactory map of the third chromosome has previously been
published, though partial maps based on special work have been given (Amer. Nat., 1916
(217); Genetics, 1919 (208).

## PDF page 24

132
GENETICS: C. B. BRIDGES
PROC. N. A. S.
<sup>8</sup> Since figure 1 was drawn (Oct. 15, 1920) a mutant (M-23) has been located at 101
in chromosome III, and there has been found to be about 1% of crossing over between
bent and eyeless in the fourth chromosome. (Scarlet is at 41.5, Chromosome III.)
the state of the state of the state of the state of the state of the state of the state of the state of the state of the state of the state of the state of the state of the state of the state of the state of the state of t


~
Control of the Control of the Control of the Control of the Control of the Control of the Control of the Control of the Control of the Control of the Control of the Control of the Control of the Control of the Control of t
Market Street Control of the Control of the Control of the Control of the Control of the Control of the Control of the Control of the Control of the Control of the Control of the Control of the Control of the Control of th

PROPERTY OF THE PROPERTY OF THE PROPERTY OF THE PROPERTY OF THE PROPERTY OF THE PROPERTY OF THE PROPERTY OF THE PROPERTY OF THE PROPERTY OF THE PROPERTY OF THE PROPERTY OF THE PROPERTY OF THE PROPERTY OF THE PROPERTY OF TH








And the second second

## PDF page 25

*



1


.
1
