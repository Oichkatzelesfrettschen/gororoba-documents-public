Source: see manifest row of the PDF
PDF sha256: 0fe6c371a3d739cc6771b2c87d77ed966aa08eb55e3904a3ab61cdc7dc92080f
License: public domain (PNAS vol. 7, published in the United States in 1921)
Language: eng
Fidelity: machine-gated

# Transcription of dickson_1921_article_only_quaternions_their_generalizations.pdf

Transcription of `dickson_1921_article_only_quaternions_their_generalizations.pdf` in this directory, 6 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 1-6 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories. No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Check for
updates
<b>PROCEEDINGS</b>
OF THE
NATIONAL ACADEMY OF SCIENCES
Volume 7
APRIL 15, 1921
Number 4
QUATERNIONS AND THEIR GENERALIZATIONS
By Leonard Eugene Dickson
DEPARTMENT OF MATHEMATICS, UNIVERSITY OF CHICAGO
Read before the Academy, April 26, 1921
1. The discovery of quaternions by W. R. Hamilton in 1843 has led
to an extensive theory of linear algebras (or closed systems of hyper-
26, 2026 from IP address 71.84.237.76.
complex numbers) in which the quaternion algebra plays an important
rôle. Frobenius proved that the only real linear associative algebras
in which a product is zero only when one factor is zero are the real number
system, the ordinary complex number system, and the algebra of real
quaternions. A much simpler proof has been given by the writer.<sup>2</sup> Later,
the writer<sup>3</sup> was led to quaternions very naturally by means of the four-
parameter continuous group which leaves unaltered each line of a set
of rulings on the quadric surface <math>x_1^2 + x_2^2 + x_4^2 + x_4^2 = 0</math>.
The object of the present note is to derive the algebra of quaternions
and its direct generalizations without assuming the associative or com-
mutative law. I shall obtain this interesting result by two distinct
Downloaded from https://www.pnas.org by 71.84.237.76 on March
methods.
2. The term field will be employed here to designate any set of ordinary
complex numbers which is closed under addition, subtraction, multipli-
cation, and division. Thus all complex numbers form a field, likewise
all real numbers, or all rational numbers.
Just as a couple <math>(a, b)</math> of real numbers defines an ordinary complex
number <math>a + bi</math>, where <math>i^2 = -1</math>, so also an <i>n</i>-tuple <math>(x_1, ..., x_n)</math> of numbers
of a field <math>F</math> defines a hypercomplex number
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
<math>xx' = \sum_{i=1}^{n} x_i x'_j . e_i e_j, \ x = x' = \sum_{i=1}^{n} (x_i = x'_i) e_i, \ fx = xf = \sum_{i=1}^{n} fx_i . e_i,</math>
when <math>f</math> is in <math>F</math>, so that multiplication is distributive. Under these assump-
tions, the set of all numbers (1) with coördinates in F shall be called a
linear algebra over <math>F</math>.
3. We assume that <math>e_1</math> is a principal unit (modulus), so that <math>e_1x = xe_1 = x</math>
for every number <math>x</math> of the algebra, and write 1 for <math>e_1</math>. We assume that
every number of the algebra satisfies a quadratic equation with coefficients
in F. If <math>e^2 + 2ae + b = 0</math>, <math>(e + a)^2 = a^2 - b</math>, so that we may take
the units to be 1, <math>E_2, \ldots, E_n</math>, where <math>E_i^2 = s_{ii}</math>, a number of <math>F</math>. For <math>i</math> and
j distinct and >1, <math>E_i = E_j</math> satisfies a quadratic, so that <math>(E_i = E_j)^2 =</math>
<math>s_{ii} + s_{jj} = (E_i E_j + E_j E_i)</math> is a linear function of <math>E_i = E_j</math>. Thus <math>E_i E_j + E_j</math>
26, 2026 from IP address 71.84.237.76.
<math>E_i E_i</math> is a linear function of <math>E_i + E_j</math> and of <math>E_i - E_j</math>, and hence is a number
<math display="block">2s_{ij} = 2s_{ji} \text{ of } F.</math>
Let <math>u_2, \ldots, u_n</math> be arbitrary numbers of <math>F</math> and write <math>U = \sum u_k E_k</math>.
Then
<math>U^2</math> equals
<math display="block">Q = \sum s_{kl} u_k n_l.</math>
It is a standard theorem that Q can be reduced to <math>\sum c_i v_i^2</math> by a linear trans-
formation <math>u_k = \sum a_{kl}v_l</math> with coefficients in F and of determinant <math>\pm 0</math>.
Write
Downloaded from https://www.pnas.org by 71.84.237.76 on March
<math display="block">e_l = \sum a_{kl} E_k</math>
<math display="block">(l=2,\ldots,n).</math>
<math>k.l = 2</math>
Then 1, <math>e_2</math>, ..., <math>e_n</math> are linearly independent and may be taken as the new
units of our algebra over F. Then
<math display="block">U = \sum_{k,l} a_{kl} v_l E_k = \sum_{l} v_l e_l,</math>
<math display="block">U^2 = \sum v_k v_l e_k e_l = \sum c_i v_i^2.</math>
Hence
<math>e_i^2 = c_i, e_i e_j + e_j e_i = 0</math>  <math>(i, j = 2, ..., n, i \neq j).</math>
(3)
4. Write <math>x = x_1 + \sum x_i e_i</math>. Then <math>(x - x_1)^2 = \sum c_i x_i^2</math>. This gives <math>xx' = x_1 + \sum x_i e_i</math>.
<math>x'x = \sigma</math>, where

## PDF page 3

111
MATHEMATICS: L. E. DICKSON
Vol. 7, 1921 -
<math>x' = 2x_1 - x = x_1 - \sum_{i} x_i e_i, \ \sigma = x_1^2 - \sum_{i} c_i x_i^2.</math>
We shall call <math>x'</math> the conjugate to <math>x</math> and <math>\sigma = \sigma(x)</math> the norm of <math>x</math>.
Hence-
the product of any number and its conjugate in either order equals its
We assume that the norm of a product equals the product of the
norm.
norms of the factors:
<math>\sigma(x)\sigma(\xi) = \sigma(X)</math>, if <math>x\xi = X</math>.
(4)
and shall investigate the resulting types of linear algebras. We assume
also that each <math>c_i \neq 0</math> in (3).
5. By (2) the coördinates of <math>X = x\xi</math> are <math>X_k = \sum x_i \xi_j \gamma_{ijk}</math>. Since <math>e_i^2 = c_i</math>,
we have <math>\gamma_{ii1} = c_i</math>, <math>\gamma_{iik} = 0</math> <math>(i>1, k>1)</math>. Hence
<math display="block">X_1 = x_1 \xi_1 + \sum_{i=2} x_i \xi_i c_i + \sum_{i,j=2} x_i \xi_j \gamma_{ij1},</math>
26, 2026 from IP address 71.84.237.76
<math display="block">, X_k = x_1 \xi_k + x_k \xi_1 + \sum x_i \xi_j \gamma_{ijk}.</math>
(5)
<math>i,j=2</math>
(k > 1)
Since this transformation is the identity <math>X = x</math> if <math>\xi = 1</math>, we obtain an
infinitesimal transformation by taking <math>\xi_1 = 1</math>, <math>\xi_j = \delta t</math>, <math>\xi_i = 0(i \pm 1, j)</math>:
<math display="block">\delta x_1 = X_1 - x_1 = \left\{ c_j x_j + \sum_{i=2} \gamma_{ij1} x_i \right\} \delta t, \delta x_j = \left\{ x_1 + \sum_{i=2} \gamma_{ijj} x_i \right\} \delta t,</math>
<math>i = 2</math>
<math>i \neq j</math>
Downloaded from https://www.pnas.org by 71.84.237.76 on March
<math display="block">\delta x_k = \left\{ \sum_{\substack{i=2\\i\neq j}} \gamma_{ijk} x_i \right\} \delta t</math>
<math>(k \pm 1, j).</math>
(6)
For these <math>\xi</math>'s, <math>\sigma(\xi)</math> is unity to within an infinitesimal of the second order.
Hence the increment to <math>\sigma(x)</math> must vanish identically, so that
<math>\gamma_{ij1} = \gamma_{ijj} = \gamma_{iji} = 0</math> (1, i, j distinct),
(7)
<math>c_k \gamma_{ijk} + c_i \gamma_{kji} = 0</math> (1, i, j, k distinct).
(8)
By <math>(7)</math>, <math>(5)</math> simplifies to
<math display="block">X_1 = x_1 \xi_1 + \sum_{i=2}^{n} x_i \xi_i c_i, X_k = x_1 \xi_k + x_k \xi_1 + \sum_{i=2}^{n} x_i \xi_i \gamma_{ijk} \ (k > 1),</math>
(9)
where, in the final sum, <math>i</math> and <math>j</math> range over distinct values from 2, ..., <math>n</math>,
excluding k. This final sum is, therefore, absent if <math>n=3</math>; whence <math>\sigma(X)</math>

## PDF page 4

112
<i>MATHEMATICS: L.E.DICKSON</i>
Proc. N. A. S.
has the term <math>2x_2\xi_2c_2.x_3\xi_3c_3</math> which does not occur in <math>\sigma(x)\sigma(\xi)</math>. But <math>c_2c_3 \neq 0</math>
by hypothesis. Hence <math>n > 3</math>.
Hitherto we have not examined the conditions which follow from the
final equations (3); these are
<math display="block">\gamma_{iik} = -\gamma_{iik} \quad (i, j = 2, \ldots, n; i \pm i).</math>
(10)
6. Taking <math>n = 4</math> and applying (10), we see that (9) become
<math display="block">\begin{cases} X_1 = x_1\xi_1 + c_2x_2\xi_2 + c_3x_3\xi_3 + c_4x_4\xi_4, X_2 = x_1\xi_2 + x_2\xi_1 + \gamma_{342}(x_3\xi_4 - x_4\xi_3), \\ X_3 = x_1\xi_3 + x_3\xi_1 + \gamma_{243}(x_2\xi_4 - x_4\xi_1), X_4 = x_1\xi_4 + x_4\xi_1 + \gamma_{234}(x_2\xi_3 - x_3\xi_2). \end{cases}</math>
(11)
These transformations do not in general form a group and hence are not
generated by the corresponding infinitesimal transformations employed
above. Hence it remains to require that <math>\sigma(X) = \sigma(x)\sigma(\xi)</math> under the
transformations (11). The conditions are seen to be
<math>c_3c_4 = -c_2\gamma^2_{342}, c_2c_4 = -c_3\gamma^2_{243}, c_2c_3 = -c_4\gamma^2_{234}, c_4\gamma_{234} = c_2\gamma_{342} = -c_3\gamma_{243},</math>
the first two of which reduce to the third by means of the last three equa-
To these last can be reduced all the conditions <math>(8)</math> by means of <math>(10)</math>.
tions.
26, 2026 from IP address 71.84.237.76.
Applying the transformation of variables which multiplies <math>x_4</math>, <math>\xi_4</math>, <math>X_4</math>
by <math>\gamma_{234}</math>, and leaves the remaining <math>x_i</math>, <math>\xi_i</math>, <math>X_i</math> unaltered, we get
<math display="block">\begin{cases} X_1 = x_1 \xi_1 + c_2 x_2 \xi_2 + c_3 x_3 \xi_3 - c_2 c_3 x_4 \xi_4, & X_2 = x_1 \xi_2 + x_2 \xi_1 - c_3 x_3 \xi_4 + c_3 x_4 \xi_3, \\ X_3 = x_1 \xi_3 + x_3 \xi_1 + c_2 x_2 \xi_4 - c_2 x_4 \xi_2, & X_4 = x_1 \xi_4 + x_4 \xi_1 + x_2 \xi_3 - x_3 \xi_2. </math>
<math>(11^{1})</math>
These are the values obtained by Lagrange<sup>5</sup> in his generalization <math>\sigma(x)\sigma(\xi) =</math>
<math>\sigma(X)</math> of Euler's formula for the product of two sums of four squares.
Then <math>x\xi = X</math> gives the following multiplication table for the units:
<math display="block">\begin{cases} e_2^2 = c_2, e_3^2 = c_3, e_4^2 = -c_2c_3, e_2e_3 = e_4, e_3e_2 = -e_4, \\ e_2e_4 = c_2e_3, e_4e_2 = -c_2e_3, e_3e_4 = -c_3e_2, e_4e_3 = c_3e_2. \end{cases}</math>
(12)
This algebra is associative and is the direct generalization of quaternions
Downloaded from https://www.pnas.org by 71.84.237.76 on March
to a general field F which the writer obtained elsewhere from assump-
tions including associativity. The four-rowed determinants of the general
number x of this algebra equals <math>\sigma^2(x)</math>. The case <math>c_2 = c_3 = -1</math> gives the
algebra of quaternions, for which it is customary to write <math>i, j, k</math> instead
of our units <math>e_2</math>, <math>e_3</math>, <math>e_4</math>.
7. It is not very laborious to show by the above method that the cases
<math>n = 5</math> and <math>n = 6</math> are excluded. However, Hurwitz has proved that a
relation of the form <math>\sigma(x)\sigma(\xi) = \sigma(X)</math> is impossible if <math>n \neq 1, 2, 4, 8</math>. A
slight simplification of his proof, together with an account of the history
of this problem, has been given by the writer.7 Hurwitz made no attempt
to find all solutions when <math>n = 4</math>. We proceed to treat this problem.
Consider the case <math>c_i = -1</math> to which the general case may be reduced
by an irrational transformation. Then <math>\sigma(x) = \sum x_i^2</math>. We investigate
the linear algebras having property (4), i. e.,
<math display="block">(x_1^2 + \ldots + x_n^2)(\xi_1^2 + \ldots + \xi_n^2) = X_1^2 + \ldots + X_n^2,</math>
(13)

## PDF page 5

113
MATHEMATICS: L. E. DICKSON
Vol. 7, 1921
if
<math display="block">X_k = \sum_{i=1}^n \left(\sum_{i=1}^n \gamma_{ijk} x_i\right) \xi_j \qquad (k = 1, \ldots, n). </math> (14)
The matrix M of this substitution has the element <math>\sum_{i=1}^{i=n} \gamma_{ijk} x_i</math> in the kth
row and jth column. If this substitution is applied to a quadratic form
in <math>X_1, \ldots, X_n</math> of matrix Q, it is a standard theorem that we obtain a quadratic
form in <math>\xi_1, \ldots, \xi_n</math>, whose matrix is <math>M'QM</math>, where <math>M'</math> is the transposed
of <math>M</math>, being obtained from <math>M</math> by the interchange of its rows and columns.
In our problem, <math>Q</math> is the identity matrix <math>I</math> whose elements are all zero
except the diagonal elements which are 1. Hence, by (13),
<math>M'M = (x_1^2 + \ldots + x_n^2)I.</math>
(15)
When a homogeneous polynomial <math>\sigma(x_1, \ldots, x_n)</math> of any degree has the
property (4) of possessing a theorem of multiplication, the writer8 has
proved that we may apply a linear transformation on <math>x_1, \ldots, x_n</math> which
leave <math>\sigma(x)</math> unaltered and one on <math>\xi_1, \ldots, \xi_n</math> which leaves <math>\sigma(\xi)</math> unaltered
26, 2026 from IP address 71.84.237.76.
such that the new algebra has the principal unit <math>e_1</math>, so that <math>\gamma_{1jk}</math> and <math>\gamma_{j1k}</math>
are both 0 if <math>j \neq k</math>, and both unity if <math>j = k</math>.
Hence <math>M = x_1 M_1 + \ldots + x_n M_n</math>, where <math>\gamma_{ijk}</math> is the element in the
kth row and jth column of <math>M_i</math>, whence <math>M_i = I</math>. Thus (15) gives
<math>M'_{i} = -M_{i}, M'_{i}M_{i} = 1, M'_{i}M_{j} + M'_{j}M_{i} = 0 \quad (i > 1, j > 1, j \neq i).</math> (16)
In view of the values of <math>\gamma_{jik}</math>, and <math>M_i^1 = -M_i</math>, we have, when <math>n = 4</math>,
<math display="block">M_{2} = \begin{pmatrix} 0 & -1 & 0 & 0 \\ 1 & 0 - \gamma_{223} - \gamma_{224} \\ 0 & \gamma_{223} & 0 & -\gamma_{234} \end{pmatrix}, \qquad M_{3} = \begin{pmatrix} 0 & 0 & -1 & 0 \\ 0 & 0 - \gamma_{323} - \gamma_{324} \\ 1 & \gamma_{323} & 0 - \gamma_{334} \end{pmatrix},</math>
Downloaded from https://www.pnas.org by 71.84.237.76 on March
0
<math>\gamma_{224} \quad \gamma_{234} \quad 0</math>
0
7324 7334
0
<math display="block">M_4 = \begin{pmatrix} 0 & 0 & 0 & -1 \\ 0 & 0 - \gamma_{423} - \gamma_{424} \\ 0 & \gamma_{423} & 0 & -\gamma_{434} \end{pmatrix}.</math>
By <math>M_i M_i = I</math>, we have <math>M^{2i} = -I</math>, which gives
<math>\gamma_{223} = \gamma_{224} = \gamma_{323} = \gamma_{334} = \gamma_{424} = \gamma_{434} = 0, \ \gamma^2 = \delta^2 = \epsilon^2 = 1,</math>
where <math>\gamma = \gamma_{234}</math>, <math>\delta = \gamma_{324}</math>, <math>\epsilon = \gamma_{423}</math>. Hence
<math display="block">M_{2} = \begin{pmatrix} 1 & 0 & 0 & 0 \\ 1 & 0 & 0 & 0 \\ 0 & 0 & 0 - \gamma \end{pmatrix}, \quad M_{3} = \begin{pmatrix} 0 & 0 & -1 & 0 \\ 0 & 0 & 0 - \delta \\ 1 & 0 & 0 & 0 \end{pmatrix}, \quad M_{4} = \begin{pmatrix} 0 & 0 & -\epsilon & 0 \\ 0 & \epsilon & 0 & 0 \\ 1 & 0 & 0 & 0 \end{pmatrix}. \quad (17)</math>
The final condition (16) states that <math>M_iM_j</math> is skew-symmetric.
The
products <math>M_2M_3</math>, <math>M_2M_4</math>, <math>M_3M_4</math> of matrices (17) are seen at once to be

## PDF page 6

114
ZOÒLOGY: J. F. FULTON, JR.
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
<sup>2</sup> Dickson, Linear Algebras, "Cambridge Tracts in Mathematics and Mathematical
Physics," No. 16, 1914 (10–12).
<sup>3</sup> Dickson, Bull. Amer. Math. Soc., 22, 1915 (53-61).
<sup>4</sup> By (7), <math>e_2e_3 = e_3e_2 = 0</math>.
<sup>5</sup> Lagrange, Nouv. Mém. Acad. Roy. Sc. de Berlin, année 1770, Berlin, 1772 (123-133);
Oeuvres de Lagrange, 3, 1869 (189). Reproduced in Dickson's History of the Theory
of Numbers, II, 1920 (279-281).
<sup>6</sup> Dickson, Trans. Amer. Math. Soc., 13, 1912 (65).
<sup>7</sup> Dickson, Annals of Math., 20, 1919 (155-171, 297).
26, 2026 from IP address 71.84.237.76.
Dickson, Comptes Rendus du Congrès Internat. Math., Strasbourg, 1920 (131-146).
NOVOCAINE AS A SUBSTITUTE FOR CURARE<sup>1</sup>
By John F. Fulton, Jr.
HARVARD UNIVERSITY
Communicated by G. H. Parker, March 3, 1921
Since the recent war, the need of a substitute for the Indian arrow poison,
curare, has been keenly felt in many physiological laboratories.
While
investigating the activity of certain local anesthetics, it was found that
Downloaded from https://www.pnas.org by 71.84.237.76 on March
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
<sup>1</sup> Contributions from the Zoölogical Laboratory of the Museum of Comparative
Zoölogy at Harvard College. No. 330.
