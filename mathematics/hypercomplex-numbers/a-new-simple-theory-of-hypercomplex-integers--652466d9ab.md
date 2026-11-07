Source: see manifest row of the PDF
PDF sha256: 652466d9ab54fb3981ab2fb89667c5996af03f8c633c424b2a4309cd77aeeefe
License: public domain (L. E. Dickson, J. Math. Pures Appl. 9e serie 2 (1923); Dickson died 1954)
Language: eng
Fidelity: machine (failed: characters)

# Transcription of a-new-simple-theory-of-hypercomplex-integers--652466d9ab.pdf

Transcription of `a-new-simple-theory-of-hypercomplex-integers--652466d9ab.pdf` in this directory, 47 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 1-47 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories. No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

JOURNAL
DE
MATHÉMATIQUES
PURES ET APPLIQUÉES
FONDÉ EN 1836 ET PUBLIE JUSQU'EN 1874
PAR JOSEPH LIOUVILLE
L.-E. DICKSON
A New Simple Theory of Hypercomplex Integers
Journal de mathématiques pures et appliquées 9<sup>e</sup> série, tome 2 (1923), p. 281-326.
<a href="http://www.numdam.org/item?id=JMPA_1923_9_2__281_0">http://www.numdam.org/item?id=JMPA_1923_9_2__281_0</a>
Numdam
gallica
Article numérisé dans le cadre du programme
Gallica de la Bibliothèque nationale de France
http://gallica.bnf.fr/
et catalogué par Mathdoc
dans le cadre du pôle associé BnF/Mathdoc
http://www.numdam.org/journals/JMPA

## PDF page 2

28 I
A NEW SIMPLE THEORY OF HYPERCOMPLEX INTEGERS.
A New Simple Theory of Hypercomplex Integers;
By L.-E. DICKSON.
1. Introduction. - Since this Memoir presents ideas of more
general interest than its title would indicate, it has been so written
that it may be read by those having no previous acquaintance with
hypercomplex numbers. It opens up a broad subject which is destined
to furnish a wide generalization of the theory of algebraic numbers.
A clear idea of the nature of our conclusions is furnished by §§ 4-6.
These and the earlier sections are strictly elementary and self-con-
tained, and make use only of facts proved here.
The immediate purpose of the Memoir is to present a new concep-
tion of hypercomplex integers which is entirely free from the fatal
objections valid against the earlier conceptions of Hurwitz and
Du Pasquier (§ 4). If their definitions are taken literally, there do not
exist hypercomplex integers in the majority of algebras of hypercom-
plex numbers. If we discard a certain one of their assumptions, we
obtain integers but are faced with the insurmountable difficulty that
factorization into primes is not only not unique, but cannot be made
unique by the introduction of ideals of any kind, a fact proved in this
Memoir. These essential difficulties all disappear under the new defi-
nition proposed here.
In his various papers cited below, Du Pasquier merely determined
the integers in each algebra in the classic lists, without investigating
the properties of the integers. This investigation is made here for the
algebras in 2 and 3 units, to obtain material for an adequate compa-
rison of the old and new definitions, and such a comparison is always

## PDF page 3

282
L.-E. DICKSON.
decidedly in favor of the new. Incidentally, the new definition tells us
automatically just what enlargement we need to make of a Du Pasquier
system of integers in order to obtain a system having unique factori-
zation into primes.
The new definition has been tested by all the classic algebras in 2,
3 and 4 units, and found in every case to give wholly satisfactory
results, as well as to explain serious difficulties arising under the ear-
lier definitions. Moreover, the new theory is far simpler to apply than
the old, and more readily lends itself to the proof of general theo-
rems, which are wholly lacking in the writings based on the old defi-
nitions.
2. Hypercomplex numbers. — The oldest example is that of ordi-
nary complex numbers <math>a + bi</math>, where a and b are real and i
denotes <math>\sqrt{-1}</math>. Next we have algebraic numbers, like
<math>x = a + b\sqrt{-3}</math>, <math>y = a + b\sqrt[3]{2} + c\sqrt[3]{4}</math>,
where now <math>a, b, c</math> are rational numbers (integers or fractions). These
are examples of hypercomplex numbers
<math>x = a + b e(c = \sqrt{-3}), \quad \gamma = a + b e_1 + c e_2(e_1 = \sqrt[3]{2}, e_2 = \sqrt[3]{3}),</math>
the first having two basals units, <math>e_0 = 1</math>, e, and the second three
basal units <math>e_0 = 1</math>, <math>e_1</math>, <math>e_2</math>. The numbers <math>a</math>, <math>b</math> or <math>a</math>, <math>b</math>, <math>c</math>, which are mul-
tiplied into the units, are called coordinates. The units satisfy the
relations
<math>e^2 = -3</math>; <math>e_1^2 = e_2</math>, <math>e_1 e_2 = e_2 e_1 = 2</math>, <math>e_2^2 = 2e_1</math>.
We may and shall ignore the values of the units as radicals, and
employ these relations to express any product (or square) of the units
as a linear function of the units. The same is therefore true as to the
product of any two numbers <math>x</math> or any two numbers <math>y</math>. We call such a
set of relations the multiplication table of the units.
We give another important example needed later. Let
<math display="block">(1) \quad e_0 = \begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix}, \qquad e_1 = \begin{pmatrix} 0 & 0 \\ 1 & 0 \end{pmatrix}, \qquad e_2 = \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix}, \qquad e_3 = \begin{pmatrix} 0 & 0 \\ 0 & 1 \end{pmatrix}.</math>

## PDF page 4

283
A NEW SIMPLE THEORY OF HYPERCOMPLEX INTEGERS.
Then any two-rowed square matrix <math>x</math> may be expressed in terms of
these four as follows
<math>x \equiv \begin{pmatrix} x_0 & x_2 \\ x_1 & x_3 \end{pmatrix} \equiv x_0 e_0 + x_1 e_1 + x_2 e_2 + x_3 e_3,</math>
(3)
since the product of matrix <math>c_0</math> by <math>x_0</math> is a similar matrix having the
element <math>x_0</math> in place of 1. The general matrix <math>x</math> is thus expressed as a
hypercomplex number with the four basal units <math>e_0</math>, <math>e_1</math>, <math>e_2</math>, <math>e_3</math>, whose
multiplication table is (1)
(3) <math>c_0^2 = c_0</math>, <math>c_3^2 = c_3</math>, <math>c_0 c_2 = c_2 c_3 = c_2</math>, <math>c_3 c_1 = c_1 c_0 = c_1</math>,
<math>e_2e_1=e_0, \qquad e_1e_2=e_3,</math>
together with the relations which state that all further squares and
products are zero.
Instead of adding or multiplying these hypercomplex numbers, we
may (more quickly) add or multiply the corresponding matrices x. To
find the element in the rth row and <math>c</math> the column of the product of <math>x</math>
by a similar matrix <math>x'</math>, we multiply the elements of the rth row of <math>x</math>
by the corresponding elements of the <math>c</math> th column of <math>x'</math> and add the
two products. For example,
<math>x' = \begin{pmatrix} x_3 & -x_2 \\ -x_1 & x_0 \end{pmatrix}, \qquad x \, x' = \begin{pmatrix} x_0 x_3 - x_1 x_2 & 0 \\ 0 & x_0 x_3 - x_1 x_2 \end{pmatrix}.</math>
Hence <math>x</math> and <math>x'</math> are roots of
<math display="block">x^2 - (x_0 + x_3) x + (x_0 x_3 - x_1 x_2) \varepsilon = 0, \qquad \varepsilon = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}.</math>
(4)
Here <math>\varepsilon = e_0 + e_3</math> plays the role of unity in multiplication. Thus every
two-rowed square matrix <math>x</math> is a root of a quadratic equation. Matrices
are known to obey the associative law of multiplication <math>xy.z = x.yz</math>.
In the same manner, we can express all n-rowed square matrices as
hypercomplex numbers in <math>n^2</math> basal units. Such a matrix <math>x</math> is the
(1) If we write <math>e_{11}</math> for <math>e_0</math>, <math>e_{21}</math> for <math>e_1</math>, <math>e_{12}</math> for <math>e_2</math>, and <math>e_{22}</math> for <math>e_3</math>, we may express
the multiplication table (of 16 products) in the compact form
<math>e_{ij}e_{jk}=e_{ik}, \quad e_{ij}e_{ik}=0 \quad (i\neq j).</math>

## PDF page 5

284
L.-E. DICKSON.
root (<math>^{1}</math>) of an equation of degree <math>n</math> whose constant term is the deter-
minant of <math>x</math> and is called the <i>norm</i> of <math>x</math>. Hence the norm of a product
is the products of the norms of the factors.
In general, we shall consider only hypercomplex numbers (2)
<math display="block">x = x_0 e_0 + x_1 e_1 + \ldots + x_n e_n</math>
(5)
with rational coordinates <math>x_0, ..., x_n</math> and a multiplication table
<math display="block">e_i e_j = \sum_{k=0} \gamma_{ijk} e_k \qquad (i, j = 0, 1, \ldots, n),</math>
(6)
where the constants <math>\gamma_{ijk}</math> are rational numbers. The product of <math>x</math> by
<math display="block">y = y_0 e_0 + \ldots + y_n e_n</math>
is defined to be the number obtained from <math>\sum x_i y_j e_i e_j</math> by replacing <math>e_i e_j</math>
by its expression (6). We agree that <math>x</math> and <math>y</math> are equal if and only
if <math>x_0 = y_0, ..., x_n = y_n</math>. We assume the associative law and the exis-
tence of a (unique) principal unit <math>\varepsilon</math> such that <math>\varepsilon x = x \varepsilon = x</math> for every
hypercomplex number <math>x</math>; we shall often write 1 for <math>\varepsilon</math>. If <math>r</math> is a rational
number, <math>rx</math> denotes <math>\Sigma(rx_i)e_i</math>. We define <math>x + y</math> to be
<math>(x_0 + y_0)e_0 + \ldots + (x_n + y_n)e_n</math>
Hence the set of all numbers (5) with rational coordinates is closed
under addition, subtraction, and multiplication. It is called a rational
(1) For a very simple proof, see the second foot-note in § 15.
(2) We may identify <math>e_i</math> with the matrix having the element <math>\gamma_{ijk}</math> in the <math>(i+1)</math>
th row and <math>(k+1)</math> th column; then relations (6) hold in matrices. For
example, if
<math>e_0^2 = e_0, \qquad e_1 e_0 = e_0 e_1 = e_1, \qquad e_1^2 = -e_0,</math>
then
<math>e_0 = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}, \qquad e_1 = \begin{pmatrix} 0 & 1 \\ -1 & 0 \end{pmatrix}.</math>
Hence ordinary complex numbers <math>x_0 + v_1 i</math> may be expressed as matrices
<math>\begin{pmatrix} x_0 & x_1 \\ -x_1 & x_0 \end{pmatrix}</math>

## PDF page 6

285
A NEW SIMPLE THEORY OF HYPERCOMPLEX INTEGERS.
linear associative algebra with a principal unit (briefly a rational
algebra), or a rational hypercomplex number system.
Since <math>\varepsilon</math>, <math>x</math>, <math>x^2</math>, ..., <math>x^{n+1}</math> are linear homogeneous functions of <math>e_0</math>, ...,
<math>e_n</math> with rational coefficients, some linear combination of them with
rational coefficients is zero. Hence x satisfies an unique equation of
lowest degree with rational coefficients and leading coefficient unity.
This is called the rank equation when the coordinates of x are arbi-
trary rational numbers. Its constant term is called the norm of x and
designated <math>N(x)</math>.
5. Preliminary survey of hypercomplex integers. — Gauss
called <math>a + bi</math> a complex integer if a and b are rational integers; every
complex integer decomposes into complex primes uniquely apart
from unit factors, <math>\pm 1</math>, <math>\pm i</math>.
For <math>\theta = \sqrt{-3}</math>, we might call <math>a + b\theta</math> a quadratic integer if and only
if a and b are rational integers. But 4 would then have two essentially
different factorizations
<math>4 = 2 \times 2, \quad 4 = (1 + \theta)(1 - \theta)</math>
into indecomposable integers 2, <math>1 + 0</math>, <math>1 - 0</math>, no one of which is the
product of another by a unit, necessarily <math>\pm 1</math>. By a unit is meant a
(quadratic) integer <math>u = a + b\theta</math> which divides 1, so that there exists
another integer <math>v</math> such that <math>uv = 1</math>. Then <math>N(u)N(v) = 1</math>, where
<math>N(u) = a^2 + 3b^2</math> is a rational integer. Hence <math>N(u) = 1</math>, <math>a = \pm 1</math>,
<math>b=0</math>, and <math>u=\pm 1</math>.
We may avoid all such double factorizations by including among
our (algebraic) integers not only the numbers <math>a + b\theta</math> in which a
and <math>b</math> are rational integers, but also those in which <math>a</math> and <math>b</math> are both
halves of odd integers. Then
<math>u = \frac{1}{2} + \frac{1}{2}\theta, \qquad u' = \frac{1}{2} - \frac{1}{2}\theta</math>
are units since they are algebraic integers whose product is 1. The
only units are here <math>\pm 1</math>, <math>\pm u</math>, <math>\pm u'</math>. Thus the second of the above fac-
torizations of 4 may now be written in the form <math>4 = (2u)(2u')</math>, which

## PDF page 7

<b>28</b>6
L.-E. DICKSON.
is not regarded as essentially different from <math>4 = 2 \times 2</math>, just as the
latter is not distinguished from <math>4 = (-2)(-2)</math>.
A still simpler example will show the wisdom of enlarging certain
proposed systems of integers. Let the system S be composed of unity
and all positive even integers, This system is evidently closed under
multiplication. Then 60 has two (and only two) decompositions into
indecomposables of S:
<math>60 = 2 \times 30, \quad 60 = 6 \times 10,</math>
where no one of 2, 6, 10, 30 is a product of two numbers, each not
the unique unit 1, of S, so that all four are indecomposable. We evi-
dently restore unique factorization into indecomposables by annexing
to S all positive odd integers.
An algebraic number is called integral if and only if it is a root of
an equation having rational integral coefficients and having unity as
the coefficient of the highest power of the unknown. For example,
<math>x = a + b\sqrt{m}</math> is a root of
<math display="block">x^{2}-2ax+(a^{2}-mb^{2})=0,</math>
which, for <math>m = -1</math>, has rational integral coefficients only when a
and b are both rational integers, so that we have Gauss's complex
integers <math>a + bi</math>. For <math>m = -3</math>, the coefficients are rational integers
only when a and b are either both rational integers or both halves of
odd integers (see above). For <math>m = -3k^2</math>, where k is a rational
integer, a and kb have the values just mentioned, so that the coordi-
nate <math>b</math> of the algebraic integer <math>x</math> may have the denominator <math>2k</math>.
There is no point in studying factorization in the set A of all inte-
gral algebraic numbers. For, if a is any rational integer,
<math>a = a_1^2 = a_2^4 = a_3^8 = \dots</math>
where <math>a_1, a_2, a_3, ...,</math> are roots of <math>x^2 = a, x^4 = a, x^8 = a, ...,</math> and
hence belong to <math>A</math>, so that the factorization of <math>a</math> within <math>A</math> would never
terminate. Hence in the theory of algebraic numbers we confine our
attention to the rational functions with rational coefficients of a parti-
cular algebraic number. Then uniqueness of factorization into primes

## PDF page 8

287
A NEW SIMPLE THEORY OF HYPERCOMPLEX INTEGERS.
either holds true or can always be secured by the introduction of
Dedekind's ideals. The above definition of algebraic integers led to
this wholly satisfactory conclusion and is therefore a thoroughly satis-
factory definition.
However, this definition fails in general for hypercomplex numbers.
For example, let us call a two-rowed square matrix (2) integral if and
only if its four elements are rational and the coefficients of the qua-
dratic equation (4) satisfied by it are rational integers. Then, if <math>k</math> is
an arbitrary rational integer <math>\neq 0</math>,
<math display="block">\mathbf{M}_k = \begin{pmatrix} \mathbf{o} & k^{-1} \\ k & \mathbf{o} \end{pmatrix}</math>
is an integral matrix, since it is a root of <math>x^2 - 1 = 0</math> by <math>M^2 = \varepsilon</math>. But
<math display="block">P = M_2 M_1 = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & 2 \end{pmatrix}, \qquad S = M_1 + M_2 = \begin{pmatrix} 0 & \frac{3}{2} \\ 3 & 0 \end{pmatrix}</math>
are neither integral matrices, since the middle coefficient of (4)
is <math>\frac{5}{5}</math> for P, and the constant term is <math>-\frac{9}{2}</math> for S. Hence this set of inte-
gral matrices is closed neither under multiplication nor under
addition.
Historically the first definition of hypercomplex integers was that
made for the case of quaternions
<math>q = a + bi + c_I + dk</math>
by R. Lipschitz (*). The multiplication table of the basal units (2) is
(7) <math>i^2 = j^2 = k^2 = -1</math>, <math>ij = -ji = k</math>, <math>jk = -kj = i</math>, <math>ki = -ik = j</math>.
(1) Journal de Math., série 4, t. 11, 1886, p. 393-439.
(2) They may be defined in terms of the matrix units (1) as follows:
<math>\iota = e_0 + e_3, \qquad \iota = \sqrt{-1} \ (e_3 - e_0), \qquad \jmath = e_2 - e_1,</math>
<math>k = -\sqrt{-1} (e_2 + e_1),</math>
Or we may define <math>\tau</math>, <math>i</math>, <math>j</math>, <math>k</math> as 4-rowed square matrices with rational integral
elements by means of the last note in § 2.
38
Journ. de Math. tome II. - Fasc. III, 1923.

## PDF page 9

288
L.-E. DICKSON.
He called <math>q</math> an integral quaternion if and only if <math>a, b, c, d</math> are rational
integers. But we then have three essentially different factorizations of
2 into prime quaternions <math>1 + i</math>, <math>1 + j</math>, <math>1 + k</math>:
<math>2 = -i(1+i)^2</math>, <math>2 = -j(1+j)^2</math>, <math>2 = -k(1+k)^2</math>,
(8)
while <math>1+i</math> is not the product of <math>1+j</math> or <math>1+k</math> by a unit, here <math>\pm 1</math>,
<math>\pm i</math>, <math>\pm j</math>, or <math>\pm k</math>.
A. Hurwitz (1) avoided all such difficulties by including among the
integral quaternions not only those of Lipschitz, but also all quater-
nions whose coordinates are all halves of odd numbers. Now the three
factorizations (8) are no longer essentially different; for example,
<math>u + j = (1+i)u</math>, <math>u = \frac{1}{2}(1-i)(1+j) = \frac{1}{2}(1-i+j-k)</math>,
and the integral quaternion <math>u</math> is a unit since <math>u u' = 1</math>, where
<math>u' = \frac{1}{2}(1+i-j+k)</math>
is an integral quaternion. Hurwitz's system of integral quaternions is
closed under addition, subtraction, and multiplication, and they have
unique factorization into prime quaternions when the arrangement of
the norms of those primes is prescribed.
We do not obtain satisfactory results by following the definition of
integral algebraic numbers and calling a quaternion <math>q</math> integral if and
only if its coordinates are rational and the coefficients of the quadratic
equation satisfied by <math>q</math> and its conjugate
<math display="block">q' = a - bi - cj - dk</math>
are rational integers. For,
<math display="block">Q = \frac{3}{5}i + \frac{4}{5}j</math>
would be integral since <math>Q^2 = -1</math>, and <math>Q = i</math> not integral being a
(1) Göttinger Nachrichten, 1896, p. 311-340; amplified in his Vorlesungen
über die Zahlentheorie der Quaternionen (Berlin, 1919).

## PDF page 10

289
A NEW SIMPLE THEORY OF HYPERCOMPLEX INTEGERS.
root of <math>x^2 + \frac{4}{5} = 0</math>. Thus the difference of the integral quaternions Q
and <math>i</math> is not integral.
4. Hypercomplex integers as defined by Hurwitz and Du Pas-
quier. — Our aim is to select the integers from the set of all hyper-
complex numbers (5) with rational coordinates, having a multipli-
cation table (6) in which the <math>\gamma_{ijk}</math> are given rational numbers. In brief
we seek the arithmetic of a given rational algebra.
Although the definition by Hurwitz was stated only for quater-
nions, it may be expressed in general form as follows.
Within a rational hypercomplex number system <math>[cf. (5), (6)]</math> a
system of integral hypercomplex numbers shall have the following
properties:
B (basis): The system has a finite basis (i. e., it contains numbers
<math>q_1, \ldots, q_k</math> such that every number of the system is expressible in the
form <math>\sum c_i q_i</math>, where each <math>c_i</math> is a rational integer);
C (closure): The system is closed under addition, subtraction, and
multiplication;
U (units): The system contains the basal units <math>e_0, ..., e_n</math>;
M (maximal): The system is a maximal (i.e., it is not contained
in a larger system having properties B, C, U).
The only modification made by Du Pasquier (') was to replace U
by the weaker assumption U.:
<math>U_{+}</math> (unit 1): The systems contains the principal unit 1.
We proceed to show that each of these definitions fails completely
for the algebra with two basal units 1 and e, where <math>e^2 = 0</math>. Any
system has a basis 1, <math>q = r + se</math>, where r and s are fixed rational
numbers, <math>s \neq 0</math>. Since <math>q^2</math> is in the system by C, we must have
<math>q^2 = a + bq</math>, where a and b are rational integers. Hence
<math>r^2 = a + br</math>, <math>2rs = bs</math>; <math>2r = b</math>, <math>r^2 = -a</math>.
Thus <math>r</math> is a rational integer, so that any system has the basis <math>r</math>, <math>se</math>,
(1) Vierteljahrsschrift Naturf. Gesell. Zürich, t. 54, 1909, p. 116-148;
L'enseignement math., t. 17, 1915, p. 340-343; t. 18, 1916, p. 201-260.

## PDF page 11

290
L.-E. DICKSON.
where s is rational. This system is contained in that having the basis,
1, te if and only if <math>\frac{3}{t}</math> is a rational integer. Since therefore the system
<math>(1, se)</math> is contained in the larger system <math>(1, \frac{1}{3}se)</math>, and the latter is
contained in the still larger system <math>\left(1,\frac{1}{4}se\right)</math>, etc., there exists no ma-
ximal system. In other words, there exist no hypercomplex inte-
gers in this algebra.
The same conclusion holds true also for Hurwitz's definition, which
adds the requirement U that <math>e</math> shall occur in the system <math>(1, se)</math> and
hence that s be the reciprocal of a rational integer.
Suppose we omit the requirement M that the system be a maximal.
It is to be anticipated (§ 5) that the laws of divisibility in a chosen
system will not be as simple as in a larger (existing) system, nor the
laws in the latter as simple as in a still larger (existing) system, and
so on to infinity, and hence that the laws in the chosen system will be
extremely complicated. This conjecture is confirmed in § 3.
5. Insurmountable difficulties in any Hurwitz or Du Pasquier
binary arithmetic with <math>e^2 = 0</math>. — We shall examine the laws of divi-
sibility in the system having the basis 1, se, where s is a chosen
rational number <math>\neq</math> 0. Without disturbing the relation <math>e^2 = 0</math>, we may
take <math>se</math> as a new basal unit <math>e</math>. Hence we may take <math>s = r</math>.
Then the integers are <math>x + ye</math>, where <math>x</math> and <math>y</math> are rational integers.
Since <math>x + ye</math> is a root of <math>(\omega - x)^2 = 0</math>, its norm is <math>x^2</math>. Hence <math>x = \pm 1</math>
for a unit. Conversely, <math>\pm 1 + ke</math> is a unit when k is any rational
integer, since its product by <math>\pm \tau - ke</math> is <math>\tau</math>. Write
<math>c_0 = 3</math>, <math>c_1 = 3 + e</math>, <math>c_2 = 3 + 2e</math>.
Then
<math>c_1c_2 = c_0^2 u</math>, <math>c_0c_2 = c_1^2</math>, <math>c_0c_1 = c_2^2 v</math>,
(9)
where <math>u = 1 + e</math>, and <math>v = 1 - e</math> are units. No one of <math>c_0</math>, <math>c_1</math>, <math>c_2</math> can be
obtained from another one of them by multiplication by units both on
the left and right. For if <math>u_k</math> denotes <math>\pm 1 + ke</math>,
<math>u_k c_j u_l = c_n, \quad n = j \pm 3(l+k) \equiv j \pmod{3}.</math>

## PDF page 12

A NEW SIMPLE THEORY OF HYPERCOMPLEX INTEGERS.
291
Finally, since no integer has the norm 3, <math>c_j</math> is not the product of
two integers neither of which is a unit, and hence is a prime. Thus,
by (9), we have two essentially different decompositions <math>c_0 c_2</math> and <math>c_1^2</math> of
the same integer into primes.
Nor is it possible to restore unique factorization into primes by the in-
troduction of ideals, hovever defined. It is understood that in introdu-
cing ideals, each integer whose norm is not zero, and its associates (i. e.,
all products of it on both sides by arbitrary units), shall correspond
to the same unique ideal, and that the product of two integers corres-
ponds to the ideal which is the product of the two ideals corresponding
to the two integers, and finally that the ideal I corresponding to the
units plays the rôle of unity in the multiplication of ideals and has no
ideal factor other than I. Hence the totality of ideals contains a set of
ideals simply isomorphic with the set of classes of associated integers.
Then <math>c_0, c_1, c_2</math> correspond to distinct ideals <math>C_0, C_1, C_2</math>, no one the
unit ideal I, such that, by (9),
<math>C_1C_2 = C_0^2</math>, <math>C_0C_2 = C_1^2</math>, <math>C_0C_1 = C_2^2</math>.
(10)
By the last two equations, any prime ideal factor D of Co divides
both <math>C_1</math> and <math>C_2</math>. Hence <math>C_i = DQ_i</math> (<math>i = 1, 2, 3</math>), where <math>Q_0, Q_1, Q_2</math> are
distincts ideals. Thus
<math>Q_1Q_2 = Q_0^2</math>, <math>Q_0Q_2 = Q_1^2</math>, <math>Q_0Q_1 = Q_2^2</math>.
No <math>Q_i</math> is 1. For, if <math>Q_2 = I</math>, the third equation would give <math>Q_0 = Q_1 = I</math>.
Hence the <math>Q_i</math> have the same properties as the <math>C_i</math>, and it is impossible
to express the equal ideals <math>C_1 C_2</math> and <math>C_0^2</math> as the same product of prime
ideals.
Theorem 1. – For the algebra with the basal units <math>i</math> and <math>e</math>,
where <math>e^2 = \mathbf{0}</math>, the definitions of integers by both Hurwitz and Du
Pasquier fail since there is no maximal system. They fail also if
we omit their requirement that a maximal system exists, since, if
the integers are defined to be numbers of any chosen one of the infi-
nitude of non-maximal systems, factorisation into indecomposable
numbers is not unique and cannot be made unique by the introduc-
tion of ideals however defined.

## PDF page 13

L.-E. DICKSON.
292
Similar insurmountable difficulties will be shown (§§ 11, 12) to
arise for the majority of algebras in three units. This is doubtless true
also of algebras in four units, for the majority of which there is cer-
tainly no maximal system (§ 14) and hence, properly speaking, no
integers under the definition of Hurwitz or Du Pasquier.
6. New definition of hypercomplex integers. — We shall employ
the assumptions C (closure), U<sub>1</sub> (unit 1), M (maximal) and R:
R (rank equation): For every number of the system, the coefficients
of the rank equation are all rational integers.
We shall often obtain the same system of integers if we replace R
by the weaker assumption N:
N (norm): The norm of every number of the system is a rational
integer.
Consider the algebra with the units 1, <math>e</math>, where <math>e^2 = 0</math>, for which we
saw that the definitions by Hurwitz and Du Pasquier both fail. We
make the assumptions C, U, M, N. Since <math>x = a + bc</math> is a root of
<math>(\omega - a)^2 = 0</math>, we have <math>N(x) = a^2</math>. Hence if x is in a system satis-
fing our assumptions, <math>a</math> is a rational integer. The unique maximal
system (of integers) is evidently composed of all the <math>x = a + bc</math>, in
which <math>a</math> is a rational integer and <math>b</math> is rational. The product of <math>x</math> by
the unit <math>1 + ke</math> is <math>a + (b + ak)e</math>, which, for <math>a \neq 0</math>, becomes a by
taking <math>k = -\frac{b}{a}</math>. Hence every integer whose norm is not zero is asso-
ciated with a rational integer a, and hence is factorable into primes
uniquely apart from unit factors.
Our unique system of integers is the aggregate of the integers in
the infinitude of systems obtained in § 1 by the definition of either
Hurwitz or Du Pasquier. The insurmountable difficulties, which
arose when they chose as their integers the numbers of any one of
their systems, have now been shown to disappear for our properly
chosen enlargement of their too restricted system. This enlargement
was accomplished by the abandonment of their strong assumption B
of a finite basis and the replacement of it by the weaker assumption N
about the norm <math>(cf. \S 8)</math>.
Theorem II. — All of the difficulties mentioned in Theorem I

## PDF page 14

293
A NEW SIMPLE THEORY OF HYPERCOMPLEX INTEGERS.
disappear under the new definition of integers, which now decom-
pose into primes uniquely.
7. Characteristic equations, property of <math>N(x)</math>. — To define the
characteristic equations, note that, by(6),
<math display="block">x e_j = \sum_{k=0}^n y_{jk} e_k, \qquad y_{jk} = \sum_{i=0}^n x_i \gamma_{ijk}.</math>
Writing the first equation in full for <math>j = 0, 1, ..., n</math>, we get
<math>(y_{00}-x)v_0+y_{01}v_1+\ldots+y_{0n}v_n=0,</math>
<math>y_{10}e_0 + (y_{11}-v)e_1 + \ldots + y_{1n}e_n = 0.</math>
<math>y_{n_0}e_0 + y_{n_1}e_1 + \ldots + (x_{nn} - x)e_n = 0.</math>
When x is replaced by an ordinary variable <math>\omega</math>, the determinant of the
coefficients of <math>e_0, ..., e_n</math> is
<math>\delta(\omega) = \left| \sum_{i=1}^{n} \gamma_{ijk} x_i - \delta_{jk} \omega \right|,</math>
where <math>\delta_{ij} = 1</math>, <math>\delta_{ik} = 0</math> if <math>j \neq k</math>. We call <math>\delta(\omega)</math> the right-hand charac-
teristic determinant of x. Let <math>C_0(\omega)</math>, ..., <math>C_n(\omega)</math> denote the adjoint
minors of the elements of j th column. Let <math>\varepsilon = \Sigma \varepsilon_j e_j</math> be the principal
unit. Multiply the above linear equations by <math>C_0(x)\varepsilon</math>, ..., <math>C_n(x)\varepsilon</math> on
the left and add. We evidently get <math>\delta(x) c_j = 0</math>. Multiply this by <math>\varepsilon_j</math> and
sum for <math>j = 0, 1, ..., n</math>; we get <math>\delta(x) = 0</math>. Hence <math>x</math> is a root of the right-
hand characteristic equation <math>\delta(\omega) = 0</math>. It is understood that, besides
substituting <math>x^k</math> for <math>\omega^k</math>, we multiply the constant term <math>\delta(o) = \Delta(x)</math> by <math>\epsilon</math>.
Similarly, every hypercomplex number <math>x</math> is a root of its left-hand
characteristic equation <math>\delta'(\omega) = 0</math>, obtained by starting from <math>e_i x</math> ins-
tead of the above <math>xe_j</math>. Denote <math>\delta'(o)</math> by <math>\Delta'(x)</math>. These characteristic
determinants <math>\delta(\omega)</math> and <math>\delta'(\omega)</math> remain unaltered (1) under any linear
transformation on the basal units <math>e_i</math>.
If y is a fixed and w a variable hypercomplex number, the rela-
(1) Dickson, Linear Ugebras, Cambridge University Tract, no 16, 1914, p. 19.

## PDF page 15

294
L.-E. DICKSON.
tion <math>x' = xy</math> defines a linear transformation on <math>x_0, ..., x_n</math> with the
determinant <math>\Delta'(y)</math>. Similarly, to <math>y'</math> corresponds a second transfor-
mation <math>x'' = x'y'</math>. Then to <math>y'' = yy'</math> corresponds <math>x'' = xy''</math>, which is
the product of the former transformations. Hence
<math>\Delta'(\gamma)\Delta'(\gamma')=\Delta'(\gamma\gamma').</math>
Similarly, the determinant of the linear transformation defined by
<math>x' = yx</math> is <math>\Delta(y)</math>, and we get
<math>\Delta(\gamma) \Delta(\gamma') := \Delta(\gamma)'</math>.
If the coordinates of <math>x</math> are arbitrary rational integers, its <math>rank</math>
equation <math>R(\omega) = 0</math> is the unique equation of lowest degree having
the root x and coefficients which are polynomials in the coordinates
of x, the leading coefficient being unity. Evidently <math>R(\omega)</math> divides
both <math>\delta(\omega)</math> and <math>\delta'(\omega)</math>. Hence <math>N(x) \equiv R(o)</math> divides both <math>\Delta(x)</math> and <math>\Delta'(x)</math>.
By the above definitions, either characteristic equation for <math>x = \varepsilon</math>,
where <math>\varepsilon</math> is the principal unit, is <math>(1 - \omega)^{n+1} = 0</math>, and <math>R(\omega)</math> is then a
power of <math>1 - \omega</math>, whence <math>N(\varepsilon) = 1</math>. It now follows (') that
<math>N(y)N(y') = N(yy')</math>.
Theorem III. - The norm of a product of any two hypercomplex
numbers is equal to the product of their norms.
8. General remarks on the definitions of hypercomplex integers.
- In the new definition, we may replace assumption R by the
assumption that, for every number of the system, the coefficients of
the right-hand characteristic equation are rational integers, or by the
similar property for the left-hand characteristic equation. The advan-
tage in demonstrations is that we know the explicit form of the charac-
teristic equations for a general algebra, but not that of the rank equa-
tion. Furthermore, we shall prove that the assumptions B and C of
Hurwitz and Du Pasquier imply the property R of the rank equation.
Theorem IV. — If all the coefficients of the rank equation are
(1) Dickson, Comptes rendus du Congrès international des Mathématiciens,
(Strasbourg, 1920), Toulouse, 1921. § 5.

## PDF page 16

295
A NEW SIMPLE THEORY OF HYPERCOMPLEX INTEGERS.
rational integers, those of either characteristic equation are rational
integers, and conversely.
The converse follows from Gauss's lemma; if
<math>\hat{o}(\omega) = \omega^m + a_1 \omega^{m-1} + \ldots + a_m</math>
has rational integral coefficients and is divisible by
<math>R(\omega) = \omega^r + \Lambda_1 \omega^{r-1} + \ldots + \Lambda_r</math>
with rational coefficients, these coefficients <math>\Lambda_i</math> are all rational integers.
Next let <math>R(\omega)</math> have rational integral coefficients. Then the roots
of <math>R(\omega) = 0</math> are integral algebraic numbers. But (') these roots include
all the distinct roots of <math>\delta(\omega) = 0</math>. Hence the coefficients of the latter
are integral algebraic numbers and also rational (since the coordi-
nates <math>x_i</math> and <math>\gamma_{ijk}</math> are assumed to be rational), and hence are rational
integers.
Theorem V. — For every system having the closure pooperty Cand
a finite basis composed (2) of as many linearly independent num-
bers as the algebra has basal units, the characteristic equations
of each number of the system have rational integral coefficients.
Such a system has a basis <math>E_0 = 1</math>, <math>E_1</math>, ..., <math>E_n</math>. We may take the <math>E_i</math>
as new basal units of the algebra. By the closure property C, <math>E_i E_i</math>
belongs to the system. By the property B of the basis, <math>E_i E_j</math> is equal to
a linear function of <math>E_0</math>, ..., <math>E_n</math> with rational integral coefficients.
Hence the new constants of multiplication <math>\Gamma_{ijk}</math> are rational integers.
The same is true of the coordinates <math>X_i</math> of every number <math>X = \Sigma X_i E_i</math> of
the system (property B). Hence either characteristic equation of X has
rational integral coefficients. But the coefficients of that equation are
invariant under every linear transformation of the basal units (§ 7).
Hence any system according to the definition of Du Pasquier is
(1) G. Scheffens, Math. Annalen, t. 39, 1891, p. 302. — Dickson, Linear
Algebras, p. 22.
(2) Assumed by Du Pasquier (ref. in § 4) in finding his systems of 2-rowed
square matrices, the only algebra for which he has given details of the work of
finding maximal systems.
39
Journ. de Math., tome II. - Fasc. III, 1923.

## PDF page 17

296
L.-E. DICKSON.
a system according to the new definition, but not conversely, so
that the new maximal systems are usually not systems of Du Pasquier.
After the introduction of the new basal units E, the particular
. Du Pasquier system becomes the set of linear combinations of the <math>\mathbf{E}_i</math>
with rational integral coordinates and hence has property U; but this
need not be true simultaneously of the remaining Du Pasquier systems
of the same algebra (<math>cf. \S 16</math>). Hence after making a suitably chosen
transformation of the basal units with rational coefficients, we obtain
an algebra in which at least one Du Pasquier system is a Hurwitz
system.
<b>9.</b>General theory of integers of reducible algebras. — A linear
associative algebra S of hypercomplex numbers with s basal units
whose coordinates range independently over all rational numbers, and
having a principal unit s, is called rationally reducible if it contains
<math>\alpha + \beta = s</math> numbers <math>e_1, ..., e_{\alpha}, E_1, ..., E_{\beta}</math>, not satisfying a linear homo-
geneous equation with rational coefficients, such that
<math>e_i \mathbf{E}_j = \mathbf{0}, \quad \mathbf{E}_j e_i = \mathbf{0} \quad (i = 1, ..., \alpha; j = 1, ..., \beta).</math>
(11)
In the contrary case, S is called rationally irreducible.
Let S be rationally reducible. It is readily proved (') that all
squares and products of <math>e_1, ..., e_n</math> are linear functions of <math>e_1, ..., e_n</math>
with rational coefficients, so that <math>e_1, ..., e_{\alpha}</math> are the basal units of an
algebra a with rational coordinates. Likewise, <math>E_1, ..., E_{\beta}</math> are the basal
units of an algebra A. Also, <math>a</math> and A have principal units <math>e</math> and E res-
pectively, whose sum is <math>\varepsilon</math>.
Conversely, from any two linear associative algebras <math>a</math> and A with
basal units <math>e_i</math> and <math>E_j</math>, principal units <math>e</math> and <math>E</math>, and rational coordinates,
we evidently obtain a linear associative algebra S with the basal
units <math>e_1, ..., e_{\alpha}, E_1, ..., E_{\beta}</math>, principal unit <math>e + E</math>, and rational coordi-
nates, by postulating relations (11) and regarding <math>e_1, ..., E_{\beta}</math> as satis-
fyng no linear homogeneous equation with rationial coefficients.
We call S the <i>direct sum</i> of a and A and write <math>S = a + A = A + a</math>,
and call a and A the components of S.
(1) Dickson, Linear Algebras, p. 26, 27.

## PDF page 18

297
A NEW SIMPLE THEORY OF HYPERCOMPLEX INTEGERS.
Theorem VI. — Consider systems of integers having properties
C, U<sub>1</sub>, R (and M). The first (or second) components of the num-
bers of any (maximal) system of integers of a rationally reducible
algebra constitute a (maximal) system of integers of the first (or
second) component algebra. Conversely, given a (maximal) system
[X] of integers x of an algebra a and a (maximal) system [X] of
integers <math>{\bf X}</math> of another algebra <math>{\bf A},</math> if we add every number <math>x</math> to every
number X, we obtain sums forming a (maximal) system of inte-
gers of the direct sum <math>a + A</math>.
By Theorem IV, R implies that the coefficients of the right-hand
characteristic equation are rational integers, and conversely.
(i). Let [z] be any given system of integers z of a reducible
algebra <math>S = a + A</math>. We have <math>z = x + X</math>, where x is a number <math>\sum x_i e_i</math>
of the first component algebra a, and X is a number <math>\sum X_k E_k</math> of A. To
determine the right-hand characteristic determinant of <math>z</math> for <math>S(\S 7)</math>,
we employ
<math>se_j = \sum_{i=1}^n x_i e_i e_j + 0 \qquad (j = 1, ..., x),</math>
<math>zE_j = o + \sum_{k=1}^{n} X_k E_k E_j</math>  <math>(j = 1, ..., \beta).</math>
Hence the right-hand characteristic determinant of z for S is equal
to the product of that of w for a by that of X for A. Hence, by
Gauss's lemma (§ 8), the polynominals in <math>\omega</math> which are equal to the
last two determinants have rational integral coefficients when z is in
the system <math>[z]</math>. Hence the rank equations of <math>x</math> and <math>X</math> for <math>a</math> and <math>A</math>,
respectively, have rational integral coefficients. Next, if also
<math>z' = x' + X'</math> is in <math>[z]</math>, then <math>zz' = xx' + XX'</math> is in <math>[z]</math> by the closure
property C. We have now proved the first half of Theorem VI with
both words maximal omitted.
(ii) Conversely, let <math>[x]</math> by any given system of integers <math>x</math> of an
algebra <math>a</math>, and [X] any given system of integers of another algebra A.
As explained above, we may regard a and A as the components of a
rationally reducible algebra <math>S = a + A</math> for which relations (11)
hold. To every number <math>x</math> of <math>[x]</math> add every number <math>X</math> of <math>[X]</math>. By the

## PDF page 19

298
L.-E. DICKSON.
facts in (i), these sums form a system <math>[z]</math> of numbers of S having
properties C, U,, and R.
Further, let <math>[x]</math> and <math>[X]</math> be maximal systems of a and A, respecti-
vely. Then if <math>[z]</math> is not a maximal system of S, it is contained in a
larger system <math>[z']</math> of S. By (i), the first components <math>x'</math> of the
<math>z' = x' + X'</math> form a system <math>[x']</math> of numbers of a having properties C,
<math>U_i</math>, R, and likewise for the second components X'. Either <math>[x']</math> is
larger than <math>[x]</math> and contains it, or else <math>[X']</math> is larger than <math>[X]</math>, con-
trary to hypothesis. This proves the last half of Theorem VI.
(iii) Returning to part (i), let <math>[z]</math> be a maximal system of S. Then
if <math>[x]</math> is contained in a larger system <math>[x']</math> of <math>a</math>, part <math>(ii)</math> shows that <math>[x']</math>
and [X] determine a system <math>|z'|</math> of numbers <math>z' = x' + X</math> of S, which
have properties C, U, and R, such that |z'| contains the smaller
system <math>[z]</math>, whereas <math>[z]</math> was assumed to be a maximal. This completes
the proof of the first half of Theorem VI.
Theorem VII. — The second part of Theorem VI holds also for
systems of integers defined by properties C, U, N and M.
We employ the known result (1) that the rank equation of S is
equal to the product of the rank equations of the component algebras a
and A. From their constant terms, we get
<math>N_{S}(z) = N_{\alpha}(x) \cdot N_{\Lambda}(X)</math>.
(13)
where each norm is taken with respect to the algebra indicated by
the subscript.
Let there be given systems <math>[w]</math> and <math>[X]</math> of integers of a and A, res-
pectively. To every <math>x</math> of <math>[x]</math> add every <math>X</math> of <math>[X]</math>; these sums form a
set [z] of numbers <math>z = x + X</math> of the direct sum <math>S = a + A</math>. Since <math>N_a(x)</math>
and <math>N_{\lambda}(X)</math> are rational integers by assumption N, <math>N_{\kappa}(z)</math> is a rational
(1) For, if <math>r(\omega) = 0</math> is the rank equation of a and <math>R(\omega) = 0</math> that of A, <math>\omega</math>
and X are both roots of <math>r(\omega)</math>. <math>R(\omega) = 0</math>. But <math>z = x + X</math> implies <math>z^k = x^k + X^k</math>,
whence <math>f(z) = f(x) + f(X)</math> for any polynomial f. Hence, z is a root
of <math>r</math>, <math>R = 0</math>. That it is not the root of an equation of lower degree follows by use
of <math>z = x + 0</math> or <math>z = 0 + X</math>, since the coefficients of r are independent of the
coordinates of X.

## PDF page 20

A NEW SIMPLE THEORY OF HYPERCOMPLEX INTEGERS.
<b>299</b>
integer by (12). Thus [3] has property N and evidently also proper-
ties C and U.
Suppose that [z] is not a maximal, but is contained in a larger
system <math>[z']</math> of numbers of S having properties C, U, N. Since <math>e + o</math>
and <math>o + E</math> are in <math>[z]</math>, they are in <math>[z']</math>. Then if <math>z' = x' + X'</math> is any
number of <math>[z']</math>, <math>ez' = x'</math> and <math>x' + E</math> are in <math>[z']</math>. Thus <math>N_s(x' + E)</math> is a
rational integer by hypothesis, and is equal to <math>N_a(x')</math> by (12),
since <math>N_{\alpha}(E) = 1</math> by § 7 (end). Hence <math>N_{\alpha}(x')</math> is a rational integer.
Hence the <math>x'</math> form a system <math>[x']</math> of numbers of a having properties C,
<math>U_1</math>, N. Likewise for the X'. Either <math>[x']</math> is larger than <math>[x]</math> and contains
it, or <math>[X']</math> is larger than <math>[X]</math>, contrary to the assumption that <math>[x]</math>
and [X] are maximal.
From the third and fourth sentences of the preceding paragraph,
we obtain the following analogue of the first part of Theorem VI.
Theorem VIII. – In a rationally reducible algebra <math>S = a + \Lambda</math>,
consider systems of integers having properties C and N and con-
taining (1) the principal units e and E of a and A. The first compo-
nents of the numbers of any (maximal) system of integers of S
constitute a (maximal) system of integers of a, and the second
components a system of A.
Let a number <math>z = x + X</math> of a system <math>|z|</math> of integers he a unit, so
that there exists a number <math>z'=x'+X'</math> of <math>|z|</math> such that <math>zz'=\varepsilon=e+E</math>.
Then <math>xx' = c</math>, <math>XX' = E</math>, and <math>x</math> is a unit of <math>a</math>, and <math>X</math> of <math>A</math>. Conversely,
if <math>x</math> and <math>X</math> are units of <math>a</math> and <math>A</math>, then <math>x + X</math> is a unit of <math>a + A</math>.
If all integers of norm <math>\neq</math> o of the component algebras <math>a</math> and A
factor into primes uniquely apart from unit factors, the same is true
of the integers of <math>a + A</math>.
For example, consider the direct sum <math>(e_0) + (e_1) + (e_2)</math>:
<math>e_i^2 = e_i, \quad e_i e_j = o(j = i), \quad 1 = e_0 + c_1 + e_2.</math>
The rank and characteristic equations are <math>II(x_i - \omega) = 0</math>.
(1) Without assuming that the systems contain c and E, I have verified the
theorem for the three classic reducible algebras in 3 units (§ 11), the proof
being long only for <math>a = (e_0) + (e_1)</math>, <math>b = (e_2)</math>.

## PDF page 21

<b>30</b>0
L.-E. DICKSON.
Hence under the new definition by properties C, U, R, M the
integers are the numbers having rational integral coordinates. The
latter are all <math>\geq 0</math> in the product of x by a suitably chosen unit
<math>\pm e_0 \pm e_1 \pm e_2</math>. We restrict attention to integers x of norm <math>x_0 x_1 x_2 \neq 0</math>
and having positive integral coordinates. Denote <math>x</math> by <math>(x_0, x_1, x_2)</math>.
Then <math>xy = (x_0y_0, x_1y_1, x_2y_2)</math>. Since
<math>(p, q, rs) = (p, q, r)(1, 1, s), (p, q, r) = (p, q, 1)(1, 1, r),</math>
one of the coordinates of a prime is a rational prime and the remaining
two are unity, and conversely every such number is a prime. Hence if
the <math>p_i</math>, <math>q_j</math>, <math>r_k</math> are all rational primes, we have the following unique
factorization into primes:
<math>(p_1...p_a, q_1...q_b, r_1...r_c) = \prod_{i=1}^a (p_i, 1, 1). \prod_{j=1}^b (1, q_j, 1). \prod_{k=1}^c (1, 1, r_k).</math>
Given that a number <math>x</math> of an algebra <math>a</math> is an integer if and only if
specified coordinates <math>x_i</math> are rational integers and the remaining coor-
dinates <math>x_i</math> are rational, and similarly for another algebra A, then we
know from Theorem VI that in the direct sum <math>S = a + A</math> a number
<math>z = x + X</math> is an integer if and only if the coordinates <math>x_i</math> and <math>X_i</math> are
rational integers and the remaining coordinates <math>x_i</math> and <math>X_i</math> are rational.
From <math>zz' = xx' + XX'</math>, where <math>z' = x' + X'</math> is a unit, we conclude
that an integer z is associated with those and only those integers
whose first components are associated with <math>x</math> in <math>a</math> and whose second
components are associated with X in A.
If <math>\alpha</math> is one of the two rationally irreducible algebras in two basal
units (§ 10), or one of the three in three basal units (§ 12), we shall
find that an integer x of a, such that <math>N(x) \neq 0</math>, is associated with the
abridged integer having the same coordinates <math>x_i</math> (which were rational
integers in <math>x</math>), but having zeros in place of the coordinates <math>x_i</math> (which
were rational in <math>x</math>). Hence for every rationally reducible algebra
in 2, 3 or 4 basal units, each integer <math>z = x + X</math>, such that <math>X(z) \neq 0</math>,
is associated with the abridged integer having each <math>x_j</math> and <math>X_j</math> zero, but
with no further coordinates zero. Thus the laws of factorization in
<math>a + \Lambda</math> are the same as in <math>a' + \Lambda'</math>, where <math>a'</math> denotes the abridgement

## PDF page 22

301
A NEW SIMPLE THEORY OF HYPERCOMPLEX INTEGERS.
of a to the basal units <math>e_i</math>, and A' the abridgement of A to the units <math>E_i</math>.
But if <math>a</math> is the algebra of matrices (§ 13), further coordinates are
zero in the associates of x.
By the results in this section we may read off at once all the pro-
perties of the integers of a rationally reducible algebra from those of
the components.
10. Algebras in two units. — We assume properties C, U,, N, M.
The unique maximal system of integers of the reducible algebra
<math>(e_0) + (e_1) : e_0^2 = e_0, \quad e_0 e_1 = e_1 e_0 = 0, \quad e_1^2 = e_1, \quad 1 = e_0 + e_1,</math>
is composed of all the numbers <math>x_0e_0 + x_1e_1</math> in which <math>x_0</math> and <math>x_1</math> are
rational integers. Those of norm <math>x_0x_1\neq 0</math> decompose into primes
uniquely apart from unit factors <math>\pm e_0 \pm e_1</math> (§ 9). This algebra is
another form of that with the basal units 1, c, where <math>c^2 = 1</math>. That
with <math>e^2 = 0</math> was treated in §§ 4, 3. That with <math>e^2 = -1</math> has as integers
Gauss's complex integers <math>x + yi</math>, where <math>x</math> and <math>y</math> are rational integers.
For <math>c^2 = \pm \tau</math>, the same results are obtained by Du Pasquier's definition.
11. Reducible algebras in three units - Such an algebra is the
direct sum of an algebra in two units <math>e_0</math> and <math>e_1</math> (§ 10) and the
algebra <math>(e_2)</math> in a single unit such that <math>e_2^2 = e_2</math>. Hence they are
<math>(e_0)+(e_1)+(e_2);</math>
<math>\Lambda + (e_2), \quad \Lambda = (e_0, e_1), \quad e_0^2 = e_0, \quad e_0 e_1 = e_1 e_0 = e_1, \quad e_1^2 = -e_0;</math>
<math>B + (e_2), \quad B = (e_0, e_1), \quad e_0^2 = e_0, \quad e_0 e_1 = e_1 e_0 = e_1, \quad e_1^2 = 0.</math>
Under the new definition (') of integers, Theorem VI shows that the
integers of the first two algebras are the numbers all of whose coordi-
nates are rational integers, while those of B + <math>(e_2)</math> are <math>\sum x_i e_i</math>, where <math>x_i</math>
is rational and <math>x_0</math> and <math>x_2</math> are rational integers. For all three algebras,
every integer of norm <math>\neq 0</math> decomposes into primes uniquely apart
from unit factors.
Only for the first two of these algebras are the integers the same by
(1) Also with R replaced by N, the proof being longer.

## PDF page 23

302
L.-E. DICKSON.
Du Pasquier's (') definition. In B + <math>(e_2)</math> replace <math>e_0</math> by <math>1 - e_2</math>; we get
his system 3. He found that the most general system of numbers
under his definition has the basis 1, <math>\alpha e_1</math>, <math>\beta e_1 + g e_2</math>, where <math>\alpha</math> and <math>\beta</math>
are rational, <math>\frac{\beta}{\alpha} = \frac{g_1}{w}</math>, while <math>g_1</math> and <math>g</math> are rational integers, whence no
systems is maximal and integers do no exist. Note that the aggregate
of the numbers in all of his systems is the above system of integers
under the new definition.
Let us ignore the assumption of a maximal, and take as integers
the numbers of an arbitrarily chosen one of his systems. Without
altering the multiplication table of the units, we may take <math>\alpha e_i</math> as a
new unit <math>c_i</math>, which amounts to taking <math>\alpha = 1</math>. Then the integers have
the basis
<math>1 = e_0 + e_2, \qquad e_1, \qquad g^{-1}g_1e_1 + ge_2.</math>
Thus <math>g^2 e_2</math> is integral. Write h for <math>g^2 + 3</math>, and
<math>c_i = (3, j, h) = 3 + jc_1 + g^2 e_2</math>
where <math>(x_0, x_i, x_2)</math> denotes <math>\sum x_i e_i</math>. Since
<math>(x_0, x_1, x_2)(y_0, y_1, y_2) = (x_0y_0, x_0y_1 + x_1y_0, x_2y_2),</math>
we have
<math>c_i c_k = c_i^2 (if j + k = 2t), c_i u_i = c_{i+3i}</math>
<math>u_l = (1, l, 1), \quad u_l u_{-l} = 1,</math>
whence <math>u_i</math> is a unit. Thus
<math>c_1^2 = c_0 c_2,</math> <math>c_2^2 = c_1 c_3 = c_1 c_0 u_1,</math> <math>c_0^2 = c_2 c_{-2} = c_2 c_1 u_{-1},</math>
which may be written as
<math>c_1 c_2 = c_0^2 u_1, \qquad c_0 c_2 = c_1^2, \qquad c_0 c_1 = c_2^2 u_{-1},</math>
which are exactly of the type (9). The only possible units are
<math>(1, l, \pm 1)</math> and their negatives; but <math>(1, l, -1)</math> is not one of our inte-
gers, and hence is not a unit, if <math>|g| > 2</math>. We find that no two of
<math>c_0, c_1, c_2</math> are associated numbers and that each is a prime. Hence <math>(\S 5)</math>
(1) Bull. Soc. Math. de France, t. XLVIII, 1920, p. 109-132.

## PDF page 24

<b>3o3</b>
A NEW SIMPLE THEORY OF HYPERCOMPLEX INTEGERS.
factorization into primes is not unique and cannot be made unique by
the introduction of ideals of any kind. This conclusion applies to each
of the triply infinite number of systems of integers, one system for
each set of values of <math>\alpha</math>, <math>\beta</math>, <math>g</math>. We saw above how these difficulties
disappear under the new definition.
12. Irreducible Algebras in Three Units. — We employ assump-
tions C, U, N, M, and find that the resulting integers have also pro-
perties U and R. For the algebra
<math>T_1: e_0 = 1, e_1^2 = e_2, e_1 e_2 = e_2 e_1 = e_2^2 = 0,</math>
the rank and characteristic equations are all <math>(x_0 - \omega)^3 = 0</math>. The
maximal system of integers is composed of all numbers <math>x</math> for which <math>x_0</math>
is a rational integer and <math>x_1</math>, <math>x_2</math> are rational. If
<math>x_0 \neq 0</math>, <math>x = x_0</math>, for <math>x = 1 - \frac{x_1}{x_0} e_1 + \frac{x_1^2 - x_0 x_2}{x_0^2} e_2</math>.
Hence x is a unit if <math>x_0 = 1</math>. Thus u is a unit, and any integer x of
norm <math>x_0^3 \neq 0</math> is associated with <math>x_0</math>, and hence decomposes into primes
uniquely.
If we replace <math>u</math> by <math>1 - \frac{x_1}{x_0}e_1 - \frac{x_2}{x_0}e_2</math>, we see that all the preceding
statements hold also for the algebra
<math>T_2</math>: <math>e_0 = 1</math>, <math>e_1^2 = e_1 e_2 = e_2 e_1 = e_2^2 = 0</math>.
Finally, consider the algebra
<math>T_3: e_0^2 = e_0, e_1^2 = e_1, e_1e_2 = e_2e_0 = e_2,</math>
<math>e_0 e_1 = e_1 e_0 = e_0 e_2 = e_2 e_1 = e_2^2 = 0</math>
<math>e_0 + e_1 = 1</math>, <math>R(\omega) = (x_0 - \omega)(x_1 - \omega)</math>, <math>\hat{o}(\omega) = (x_0 - \omega)(x_1 - \omega)^2</math>.
Thus
<math>N(x) = x_0 x_1, \quad N(x+1) = (x_0+1)(x_1+1).</math>
Hence if x is an integer, <math>x_0x_1</math> and <math>x_0 + x_4</math> are rational integers. Thus
the maximal system is composed of all numbers x for which <math>x_0</math> and <math>x_1</math>
are rational integers, while <math>x_2</math> is rational.
40
Journ. de Math., tome II. - Fasc. III, 1923.

## PDF page 25

304
L.-E. DICKSON.
Denote <math>x</math> by <math>(x_0, x_1, x_2)</math>. Then
(13)
<math>(x_0, x_1, x_2)(y_0, y_1, y_2) = (x_0, y_0, x_1, y_1, x_1, y_2 + x_2, y_0).</math>
For <math>u_z \equiv (1, 1, z)</math>, <math>u_z u_z = 1</math>, so that <math>u_z</math> is a unit. Now
<math>u_{w}xu_{z}=(x_{0}, x_{1}, r), \qquad r=x_{2}+x_{0}w+x_{1}z.</math>
(14)
Hence, unless <math>x_0 = x_1 = 0</math>, we can find rational numbers <math>w</math>, <math>z</math> such
that <math>r = 0</math>. Thus any integer of norm <math>x_0 x_1 \neq 0</math> is associated with
<math>x_0 e_0 + x_1 e_1</math>. By § 10, the latter integers decompose into primes
uniquely.
These satisfactory results regarding the integers of any of these
three algebras <math>T_i</math> are in marked contrast to the results obtained by the
definitions of either Hurwitz or Du Pasquier. Then there is no
maximal system of integers, while if we select any system we meet
essential difficulties.
First, for T<sub>4</sub>, which is Du Pasquier's system 4, the most general
system of integers was stated by him to have the basis 1, <math>g^{-1}\alpha^2 e_2</math>,
<math>\alpha e_1 + \beta e_2</math>, where <math>\alpha</math> and <math>\beta</math> are rational and <math>g</math> is a rational integer, so
that no system is maximal. Taking
<math>E_1 = \alpha e_1 + \beta e_2, \qquad E_2 = E_1^2 = \alpha^2 e_2,</math>
we obtain <math>T_i</math> written in capital letters <math>E_i</math>. Hence the new basis is 1,
<math>E_1</math>, <math>tE_2</math>, where <math>t = \frac{I_1}{x}</math>. Write <math>c_j</math> for <math>3 + jtE_2</math>. We obtain (9), where
now
<math>u=1+t\mathbf{E}_2, \quad v=1-t\mathbf{E}_2</math>
are units. No two of the primes <math>c_0</math>, <math>c_4</math>, <math>c_2</math> are associates. Hence (§ 5),
decomposition into primes is not unique, and cannot be made unique
by the introduction of ideals of any kind.
For T<sub>2</sub>, which is Du Pasquier's system 6, the most general system
of integers was stated by him to have the basis, 1, <math>\alpha e_1</math>, <math>\beta e_4 + \gamma e_2</math>,
where <math>\alpha</math>, <math>\beta</math>, <math>\gamma</math> are rational, so that no system is maximal. The last two
numbers of the basis may be taken as new units E<sub>1</sub>, E<sub>2</sub> without dis-
turbing T2. The further discussion for T, applies also here,
where <math>t = 1</math>.

## PDF page 26

305
A NEW SIMPLE THEORY OF HYPERCOMPLEX INTEGERS.
Du Pasquier's system 5 is
<math>e_0 = 1</math>, <math>e_1^2 = 1</math>, <math>e_1 e_2 = e_2</math>, <math>e_2 e_1 = -e_2</math>, <math>e_2^2 = 0</math>,
and his most general system of integers has the basis <math>\tau</math>, <math>\alpha e_2</math>,
<math>gE + \beta r_2</math>, where <math>\alpha</math> and <math>\beta</math> are rational, <math>g</math> is a rational integer,
and <math>E = \frac{1}{2}(1 + e_1)</math>. Taking the latter as a new unit in place of <math>e_1</math>, and
then <math>\varepsilon = E + g^{-1}\beta e_2</math> in place of E, we get
<math>\varepsilon^2 = \varepsilon</math>, <math>\varepsilon e_2 = e_2</math>, <math>e_2 \varepsilon = 0</math>, <math>e_2^2 = 0</math>,
and the basis 1, <math>\alpha e_2</math>, <math>\alpha \varepsilon_2</math>. The effect of taking <math>\alpha e_2</math> as a new <math>e_2</math> is to
take <math>\alpha = 1</math>. Finally, we write <math>e_i</math> for <math>\epsilon</math>, and <math>e_0</math> for <math>i - \epsilon</math>; and get
algebra <math>T_3</math> and the basis <math>r</math>, <math>ge_1</math>, <math>e_2</math>. Hence <math>(p, q, r)</math> is an integer if
and only if <math>p, q, r</math> are rational integers such that <math>p = q \pmod{g}</math>.
By (13),
<math>(p, q, r) = (p, 1, z)(1, q, w), \quad \text{if} \quad z + w = r.</math>
All three numbers are integers if
<math>p \equiv q \equiv 1 \pmod{g}</math>.
As special cases, or by (14),
<math>(p, 1, 0) u_z = (p, 1, z), \qquad u_w(1, q, 0) = (1, q, w).</math>
Hence <math>(p, q, r)</math> is the product of units and <math>(p, 1, 0)</math>, <math>(1, q, 0)</math>. Also,
<math>(p, q, o)</math> is the product of the last two. By (14) for <math>x = (p, p, o)</math>,
x is associated with <math>(p, p, r)</math> if and only if <math>r = p(w + z)</math>. Hence if
<math>p \equiv 1 \pmod{g}</math> and if r is not divisible by p, <math>(p, p, r)</math> and <math>(p, p, o)</math>
are not associated, but have the same factorization apart from units.
This property of <math>(p, p, r)</math> holds also for the product of <math>(r, s, l)</math>
by <math>(a, b, n)</math>, where
<math display="block">l = rw + sz, \qquad n = aw_1 + bz_1,</math>
if <math>sn + al</math> is not divisible by the greatest common divisor of <math>ra</math>
and <math>sb</math>; for example, if <math>r</math> and <math>b</math> have a common factor not a divisor
of <math>as(z + w_1)</math>.

## PDF page 27

306
L.-E. DICKSON.
Theorems IX. - For the six classic algebras in three units, the
integers of the unique system obtained by the new definition have
unique factorization into primes and the system is either identical
(in the case of two reducible algebras) with the system of integers
obtained by Du Pasquier's definition or else is the aggregate of
the numbers in his infinitely many systems, no one of which is a
maximal nor has satisfactory laws of factorization into primes.
Thus the new definition succeeds when that of Du Pasquier fails,
by causing the proper enlargement of every one of his systems which
present serious difficulties to a system having no difficulties.
15. The Associated Arithmetic. — In § 12, we proved that the
integers of norm <math>\neq</math> o of the algebra <math>T_3</math> in three basal units are asso-
ciated (by multiplication by units) with the integers <math>x_0 e_0 + x_1 e_1</math> of
the algebra <math>S = (e_0) + (e_1)</math>. We shall say that the latter integers
form the arithmetic associated with the arithmetic of the integers
of <math>T_a</math>. And similarly in general.
14. Algebras in Four Units. — We make use of Study's (*) list
of the algebras into which any algebra in four units can be transformed
by a real linear transformation on the units. Ten of them are ratio-
nally reducible, and the properties of their integers are obtained by
inspection from the results in § 9. Thirteen of them are rationally irre-
ducible (although III<sub>b</sub> is algebraically reducible). We shall discuss
in §§ 16, 17 the algebra of real quaternions and the algebra XII<sub>b</sub>
obtained from it by an imaginary transformation of the units.
There remain eleven algebras. For each of them, there is no
maximal system under the definition of Du Pasquier (2), so that inte-
gers do not exist. Under the new definition by properties C, U, R, M,
the integers are found by a mere inspection of the left-hand characte-
ristic equation <math>\delta'(\omega) = 0</math>, while their essential properties are readily
(1) Monatshefte Math. Physik, t. 1, 1890, p. 305-309.
(2) Comptes rendus du Congrès international des Mathématiciens (Stras-
bourg, 1920); Toulouse, 1921, p. 164-175.

## PDF page 28

307
A NEW SIMPLE THEORY OF HYPERCOMPLEX INTEGERS.
found. The notation V (13) means that the algebra is numbered V in
٠
Study's list and is system 13 in Du Pasquier's list. The notation
<math>[x_0, x_i]</math> means that <math>\Sigma x_i e_i</math> is an integer (under the new definition) if
and only if <math>x_0</math> and <math>x_1</math> are rational integers and the remaining coordi-
nates <math>x_2</math> and <math>x_3</math> are rational.
For algebras V (13), IX (17), X (18), XI (19), XIV (22), and
XVI (29), we have
<math>\hat{o}'(\omega) = (x_0 - \omega)^{\gamma}</math> and <math>[x_0]</math>.
The associated arithmetic is that of rational integers <math>x_{v}</math>.
For <math>III_b(11)</math> and <math>XIII(20)</math>,
<math>\delta'(\omega) = \frac{1}{2}(x_0 - \omega)^2 + x_1^2 = \text{and} [x_0, x_1].</math>
The associated arithmetic is that of ordinary complex inte-
gers <math>x_0 + x_1 i</math>.
For VII'(15), we employ new units:
<math>E_0 = \frac{1}{2}(1 - e_1), \qquad E_1 = \frac{1}{2}(1 + e_1), e_2, e_3,</math>
and get
<math>E_0^2 = E_0, 	 E_1^2 = E_1, 	 E_1 e_2 = e_2, 	 E_1 e_3 = e_3, 	 e_2 E_0 = e_2, 	 e_3 E_1 = e_3,</math>
all further products being zero. Then
<math>\partial'(\omega) = (x_0 - \omega)^2 (x_1 - \omega)^2, [x_0, x_1].</math>
For XIII<sub>b</sub> (21), we employ as units the proceding <math>E_0</math>, <math>E_1</math>, and
<math>E_2 = \frac{1}{2}(e_2 - e_3), \qquad E_3 = \frac{1}{2}(e_2 + e_3),</math>
and get
•
<math>E_0^2 = E_0</math>, <math>E_1^2 = E_1</math>, <math>E_0 E_2 = E_2</math>, <math>E_1 E_3 = E_3</math>, <math>E_2 E_1 = E_2</math>, <math>E_3 E_0 = E_3</math>,
all further products being zero. Then
<math display="block">\delta'(\omega) = (x_0 - \omega)^2 (x_1 - \omega)^2, \quad [x_0, x_1].</math>
•
V

## PDF page 29

<b>3</b>08
L.-E. DICKSON.
For XV (23), we employ new units <math>E_0</math>, <math>E_1</math>, <math>e_2</math>, <math>e_3</math>, and get
<math>E_0^2 = E_0</math>, <math>E_1^2 = E_1</math>, <math>E_1 e_2 = e_2</math>, <math>E_1 e_3 = e_3</math>, <math>e_2 E_0 = e_2</math>, <math>e_3 E_0 = e_3</math>.
all further products being zero. Then
<math>\hat{\mathbf{c}}'(\omega) = (x_0 - \omega)^3 (x_1 - \omega), \quad [x_0, x_1].</math>
For the last three algebras the associated arithmetic is that of
<math>(E_0) + (E_1)</math>, and hence is that of pairs of rational integers.
13. Algebra and Arithmetic of Square Matrices. — It was
shown in <math>\S 2</math>, that all n-rowed square matrices with rational elements
form a linear associative algebra in <math>n^2</math> basal units. We shall now inves-
tigate maximal systems of such-matrices having properties <math>C, U_1, R</math>.
The system S composed of all matrices whose elements are all
rational integers has the properties C, U,, R by § 2. We shall now
prove that it is a maximal. Suppose that S is contained in a larger
system L having those properties. Thus L contains a matrix m whose
elements are fractions having a least common denominator <math>d</math>,
where <math>d > \tau</math>. By a theorem due to H. J. S. Smith ('), we can find
square matrices p and q having rational integral elements of deter-
minant unity such that <math>pmq = \delta</math>, where <math>\delta</math> is a diagonal matrix all of
whose elements outside the main diagonal are zero, while those in the
diagonal are <math>\frac{d_1}{d}</math>, ..., <math>\frac{d_r}{d}</math>, o, ..., o where r is the rank of m, the <math>d_i</math> are
rational integers which are positive with the exception (when <math>r = n</math>)
of <math>d_n</math>, whose sign is that of <math>|m|</math>, and <math>d_i</math> is a divisor of <math>d_{i+1}</math>. Any
common divisor of <math>d_i</math> and <math>d</math> would divide every <math>d_i</math> and hence divide
the numerator of every element of <math>m</math>, contrary to the definition of <math>d</math>.
Hence <math>d_1</math> and <math>d</math> are relatively prime.
Since matrices p and q belong to S and hence to L, the product
<math>pmq = \delta</math> belongs to L by property C. We shall prove that <math>\delta</math> does not
(1) Phil. Trans. London, t. 151, 1861, p. 293; Coll. Math. Papers, t. I,
p. 367; Cf. Bachmann, Arith. Quadr. Formen, t. IV, 1898, p. 294; Böcher,
Introduction to Higher Algebra, 1907, p. 264-267. We first remove the
rational factor <math>\frac{1}{d}</math> from m and place it in front of p.
4

## PDF page 30

309
A NEW SIMPLE THEORY OF HYPERCOMPLEX INTEGERS.
have property R. If <math>R(\omega) = 0</math> denotes the rank equation of the general
<i>n</i>-rowed square matrix <math>x</math>, we obtain <math>R(\omega)</math> by subtracting <math>\omega</math> from
each diagonal term of <math>x</math>. This classic theorem (') was verified in § 2
for <math>n=2</math>.
For 8 the rank equation becomes
<math display="block">\prod \left(\frac{d_i}{d} - \omega\right) = 0.</math>
Its coefficients are rational integers by the assumption R. Hence its
roots are rational integers, whereas <math>\frac{d_1}{d}</math> is not integral. In view of this
contradiction, our system S is a maximal.
But this systems S is not the only maximal system. If <math>\Sigma</math> is any
system of matrices with rational elements having properties C, U,
R. M, and if t is any matrix such that both t and <math>t^{-1}</math> transform every
matrix with rational elements into one with rational elements, we
readily prove that t transforms \(\Sigma\) into a system of matrices having the
same four properties. The conditions on t are evidently satisfied if <math>\binom{2}{t}</math>
the elements of t are all products of rational numbers by the same
number. This common factor may be omitted since it cancels
from <math>t^{-1}mt</math>. Hence if we transform our maximal system S by any
matrix having rational elements of determinant not zero, we obtain a
maximal system of matrices with rational elements having properties
C. U<sub>1</sub>, R. We obtain in this way an infinitude of distinct maximal
systems. For, if we employ as t the diagonal matrix whose diagonal
(1) Let <math>e_{ij}</math> denote the matrix whose elements are all zero except that in
the ith row and jth column, which is unity. Let <math>x_{ij}</math> be the element in the ith
row and <math>j</math> th column of <math>x</math>. Then
<math>x e_{ij} = x_{1i} e_{1j} + x_{2i} e_{2j} + \ldots + x_{ni} e_{nj}.</math>
Transposing and keeping j fixed, but taking <math>i = 1, ..., n</math>, we have n equations
the matrix of whose coefficients is derived from <math>(x_{ij})</math> by subtracting <math>\omega = x</math>
from each diagonal term. The determinant D of this matrix is known to be an
irreducible polynomial, when the <math>x_{ij}</math> are arbitrary. Thus the rank equation
is <math>D = 0</math>.
(2) And only then for 2-rowed square matrices.

## PDF page 31

310
L.-E. DICKSON.
elements are <math>k_1, ..., k_n</math>, we see that <math>t</math> transforms <math>(c_{ij})</math> into a matrix
having <math>c_{ij}\frac{k_{j}}{k_{i}}</math> as the element in the <i>i</i>th row and <i>j</i>th column. Since the
<math>k's</math> are arbitrary rational numbers <math>\neq 0</math>, we may take <math>k_1 = 1</math> without
loss of generality. For example, if <math>n = 2</math>,
<math display="block">t = \begin{pmatrix} 1 & 0 \\ 0 & k \end{pmatrix}, \qquad t^{-1} \begin{pmatrix} x_0 & x_2 \\ r_1 & r_2 \end{pmatrix} t = \begin{pmatrix} x_0 & k \cdot x_2 \\ k^{-1} \cdot r_1 & x_2 \end{pmatrix}.</math>
If in the final matrix we let <math>x_0, x_1, x_2, x_3</math> range independently over
all rational integers, we obtain a system <math>S_k</math> which is identical with <math>S_l</math>
if and only if <math>k = \pm l</math>.
Theorem X. - There exist infinitely many maximal systems
of n-rowed square matrices with rational elements having proper-
ties C, U<sub>1</sub>, R. One such maximal system is composed of all the
matrices with rational integral elements.
Whether or not there exist maximal systems, not derivable from S
by transformation, is not decided here and a decision is immaterial for
our theory. In any case we would make an arbitrary selection of one
maximal system and call its matrices integral. Fortunately the selec-
tion of S itself is wholly satisfactory, since the matrices of S have
unique factorization into primes, as we proceed to prove.
Nothing is simpler (') than the arithmetic of all matrices <math>m</math> with
rational integral elements. Any such matrix u is a unit if and only if
its determinant is <math>\pm 1</math>; for, its adjoint matrix <math>u'</math> has rational integral
elements, and <math>uu' = u'u = r</math>. By the above discussion (with now
<math>d=1</math>), there exist units p and q such that <math>pmq \equiv \delta</math>, where <math>\delta</math> is a dia-
gonal matrix whose diagonal terms <math>d_i</math> are all positive integers or zero.
Thus matrix <math>m</math> is associated with such a diagonal matrix <math>\delta</math>. Hence
unique factorization of matrices of non-vanishing determinants into
prime matrices will follow if proved for diagonal matrices all of whose
diagonal elements are positive rational integers. But this was proved
for diagonal matrices near the end of <math>\S 9</math> (for the typical case <math>n=3</math>),
(1) In spite of the very long discussion by ideals, etc., by Du Pasquier in
his Zürich thesis (Vierteljahrsschrift Naturf. Gesell. Zürich, t. 31, 1906,
p. 55-129; t. 52, 1907, p. 243-248).

## PDF page 32

311
A NEW SIMPLE THEORY OF HYPERCOMPLEX INTEGERS.
since the product of two diagonal matrices <math>(d_1, ..., d_n)</math> and <math>(\delta_1, ..., \delta_n)</math>
is <math>(d_1 \delta_1, ..., d_n \delta_n)</math>.
Or, if we prefer, we may write <math>\delta = d_1 e_1 + d_2 e_2 + d_3 e_3</math>, where
<math display="block">e_1 = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{pmatrix}, \qquad e_2 = \begin{pmatrix} 0 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0 \end{pmatrix}, \qquad e_3 = \begin{pmatrix} 0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 1 \end{pmatrix}.</math>
<math>e_i^2 = e_i</math>, <math>e_i e_j = 0</math> <math>(j \neq i)</math>, <math>e_1 + e_2 + e_3 = 1</math>,
which are the basal units of the algebra employed in § 9. But there
are now infinitely many units, while there were only eight.
Theorem XI. - The arithmetic of all n-rowed square matrices
with rational integral elements is associated with the arithmetic of
the direct sum <math>(e_1) + (e_2) + ... + (e_n)</math>, and has unique factori-
zation into primes.
16. The Property U. - An equivalent statement of the first
theorem in § 13 is that the system S of n-rowed square matrices with
rational integral elements is the unique maximal system of all matrices
with rational elements having properties C, R, and U, where U states
that all the basal units <math>e_{ij}</math> occur in the system.
The initial result in § 13 shows also that S is the unique maximal
system of matrices with rational elements having properties B, C, U,
so that the matrices (of S) having rational integral elements are the
integral matrices according to Hurwitz's definition (<math>\S 4</math>). For, if S is
not a maximal system, we proved that it contains the diagonal
matrix &, and hence by property C also every power of &. There is no
linite basis (i. e., property B fails), since <math>\delta^n</math> is not a linear function of
the lower powers of <math>\delta</math> with rational integral coefficients <math>c_i</math>. For, <math>\left(\frac{d_1}{d}\right)^n</math>
would then be equal to <math>\sum c_i \left(\frac{d_1}{d}\right)^i</math> which is the quotient of a rational
integer by <math>d^{n-1}</math>, whereas <math>\frac{d_1^n}{d}</math> is not a rational integer.
Under Du Pasquier's (') definition by properties B, C, U,, M, a
(1) Vierteljahrsschrift Naturf. Gesell. Zürich, t. 31, 1906, p. 116-148;
quoted in l'Enseignement math., t. 18, 1916, p. 201-260.
41
Journ. de Math., tome II. - Fasc. III, 1923.

## PDF page 33

312
L.-E. DICKSON.
long computation led him to all of the x6 maximal systems of 2-rowed
square matrices with rational elements, since the four basal matrices
involve six arbitrary rational integers.
Hence, if we assume C and either B or R, we find a unique maximal
system of matrices or an infinitude of maximal systems, according as
we assume also U or U<sub>1</sub>. However, we have an excellent reason for
deciding not to assume U, in spite of its having led us to a simpler
conclusion than does U<sub>1</sub>. In fact, property U is not always invariant
under a linear tsansformation of the basal units with rational (')
coefficients, while the properties U., B, R, N, C, M are always all
invariant. Expressed otherwise, a maximal system of integers contai-
ning all the basal units may transform into a system not containing
all the new basal units.
Light is thrown on this question by the algebra derived from the
algebra (7) of real quaternions by taking
<math>E_3 = i\sqrt{-1}, \quad E_2 = j\sqrt{-1}, \quad E_1 = -k.</math>
Thus
<math>E_1^2 = -1</math>, <math>E_2^2 = E_3^2 = +1</math>, <math>E_1 E_2 = -E_2 E_1 = E_3</math>,
(15)
<math>E_1 E_3 = -E_3 E_1 = -E_2</math>, <math>E_2 E_3 = -E_3 E_2 = -E_1</math>.
Call <math>x</math> and <math>x'</math> conjugates if
<math>x = x_0 + \sum x_i E_i, \quad x' = x_0 + \sum x_i E_i.</math>
Then
<math display="block">N(x) \equiv xx' = x'x = x_0^2 + x_1^2 - x_2^2 - x_3^2.</math>
(16)
Consider maximal systems of integers x with rational coordinates
having properties C, U, N. Let x be an integer, so that <math>N(x)</math> and
<math>N(x+1)</math> are rational integers. By their difference, the double of the
(1) If the coefficients are rational integers of determinant ±1 (the case of
arithmetical equivalence), property U is invariant. When that property is pos-
tulated, we should not confine our investigation of all possible arithmetics to a
study of a complete list of algebras no two of which are equivalent under trans-
formations of the units with rational coefficients, but study the much larger
list of algebras no two of which are equivalent under transformations with
rational integral coefficients.

## PDF page 34

313
A NEW SIMPLE THEORY OF HYPERCOMPLEX INTEGERS.
a absolute term » <math>x_0</math> of x is a rational integer. By property C, <math>E_1x</math>,
<math>E_2x</math>, <math>E_3x</math> are integers; their absolute terms are <math>-x_1, x_2, x_3</math>. Hence
each <math>2x_i</math> is a rational integer. Evidently <math>x_i = X_i + a_i</math>, where <math>X_i</math> is a
rational integer and <math>a_i = 0</math> or <math>\frac{1}{2}</math>. Then <math>x = X + a</math>, where X is an
integer by property U. By C. <math>a = x - X</math> is an integer. Write
<math>a = \frac{1}{2}(\Lambda_0 + \Sigma \Lambda_i E_i), \quad \Lambda_j = 0 \text{ or } 1.</math>
By <math>N(a)</math>, <math>A_0^2 + A_1^2</math> and <math>A_2^2 + A_3^2</math> differ by a multiple of 4, while each
sum is 0, 1, or 2; hence they are equal. Thus the only sets of values
are
<math>(A_0, A_1, A_2, A_3) = (o, o, o, o), (o, 1, 1, o),</math>
(17)
<math>(0, 1, 0, 1)</math>. <math>(1, 0, 1, 0)</math>,
(1, 0, 0, 1), (1, 1, 1, 1).
An evident system I of integers satisfying our assumptions is
composed of all the numbers X whose four coordinates are all rational
integers. We shall examine the systems obtained by annexing to I
one or more of the five numbers <math>u \neq 0</math> corresponding to the sets (17)
other than the first set.
First, annex the a corresponding to either the second or lifth
٠
set (17), viz.,
<math>e_1 = \frac{1}{2}(E_1 + E_2), \qquad e_3 = \frac{1}{2}(1 + E_3).</math>
(18)
Since <math>e_1 E_2 = e_3</math>, <math>e_3 E_2 = e_4</math>, the enlarged system contains both <math>e_4</math>
and <math>e_a</math> by property C. If we annex also the <math>a</math> corresponding to either
the third or fourth set (17), viz.,
<math>e'_1 = \frac{1}{2}(E_1 + E_3), \qquad e'_3 = \frac{1}{2}(t + E_2),</math>
(19)
we annex both, since <math>E_3 e'_1 = e'_3</math>, <math>E_3 e'_3 = e'_1</math>.
But
<math>e'_3 + e_1 - E_2 = \frac{1}{3}(1 + E_1)</math>
٠

## PDF page 35

314
L.-E. DICKSON.
has the norm <math>\frac{1}{2}</math>, and we do not obtain a system satisfying our
assumptions. Hence the only possible maximal systems are I, the
system S, obtained by annexing the pair (18) to I, and the system S2
obtained by annexing the pair (19) to I. For, the a corresponding to
the sixth set (17) is equal to <math>e_1 + e_3</math> and to <math>e'_1 + e'_3</math> and hence is in
both <math>S_1</math> and <math>S_2</math>.
The system <math>S_i</math> contains (18) and all the <math>E_i</math>, and hence also
(20) <math>e_0 = \frac{1}{2}(1 - E_3) = e_3 - E_3, \quad e_2 = \frac{1}{2}(E_2 - E_1) = e_1 - E_1.</math>
Conversely, from (18) and (20) we obtain by additions and subtrac-
tions the three <math>E_i</math> and 1. The multiplication table of the <math>e_i</math> is given
by (3). Hence the system S, is composed of the linear combinations
of the <math>e_i</math> with rational integral coefficients, and has properties C,
U, M. While we may deduce the new norm from (16) by expressing
the old coordinates <math>x_i</math> in terms of the new, we obtain it directly
from the next remark. The relations (3) are all satisfied by the ma-
trices (1) (1). Then <math>x = \sum x_i e_i</math> becomes the matrix (2), whose deter-
minant <math>x_0 x_3 - x_1 x_2</math> is <math>N(x)</math> by (4), and is a rational integer when <math>x</math>
is in <math>S_1</math>. Thus <math>S_1</math> has the properties <math>C_1</math>, <math>C_2</math>, <math>N_3</math>, <math>M_4</math>.
Also S<sub>2</sub> has the same properties since it is derived from S<sub>4</sub> by
interchanging <math>e_2</math> and <math>e_3</math> and changing the sign of <math>e_4</math>, and this trans-
formation of units leaves unaltered the multiplication table (3).
Theorem XII. - Algebra (15) contains exactly two maximal
sets S<sub>1</sub> and S<sub>2</sub> of integers having properties C, U, N, and each is
equivalent (under rational transformation of the units) to the
arithmetic of 2-rowed square matrices with rational integral
elements.
We proved above that the algebra of matrices with rational ele-
ments has a single maximal set S of integers having properties C,
U, R (and hence N). When we transform the algebra (15) into the
(1) But by no other 2-rowed square matrices apart from the interchange of
those corresponding to <math>c_0</math> and <math>c_3</math> as well as those corresponding to <math>e_1</math> and <math>c_2</math>,
such interchanges leaving unaltered the set of equations (3).

## PDF page 36

315
A NEW SIMPLE THEORY OF HYPERCOMPLEX INTEGERS.
matric algebra by the rational transformation (18) and (20), we
thereby transform S, into S, and S<sub>2</sub> into the system of matrices
(21) <math display="block"> \begin{pmatrix} x_0 + x_1 + \frac{1}{2}x_2 + 2x_3, & x_1 + \frac{1}{2}x_2 \\ \frac{1}{2}x_2, & x_1 + \frac{1}{2}x_2 \end{pmatrix}, </math>
in which <math>x_0</math>, <math>x_1</math>, <math>x_2</math>, <math>x_3</math> range independently over all rational
integers. This system of matrices (21) does not contain <math>e_0</math>. It has
properties C, N, M, U, but not U.
In view of Theorem X and our transformation of units, algebra (15)
has an infinitude of maximal systems having properties C, U,, R, and
hence composed of integers according to the definition adopted in this
memoir. By the formula above Theorem X, such systems include
that formed of the linear combinations of <math>1, k^{-1}e_1, kE_2, e_3</math> with
rational integral coefficients, where k is any fixed rational number <math>\neq 0</math>.
The value of the provisional assumption U lies in its help in
detecting at least one maximal system according to our definition
(with U<sub>i</sub> and not U), and moreover one having the pleasing pro-
perty U, as well as uniqueness of factorization into primes, which
recommend its selection in preference to all other maximal systems
as the system of integers of the algebra in its initial units.
17. Integral Quaternions. — If <math>x</math> is in a maximal system of qua-
ternions with rational coordinates having properties C, U, N, we find
at once that only the first and last cases (17) exist, so that the four
coordinates of x are either all rational integers or all halves of odd
integers. Hence <math>x</math> is a linear combination of
<math display="block">\rho = \frac{1}{2}(1 + i + j + k), \quad i, j, k,</math>
(53)
with rational integral coefficients. The squares and products of the
numbers (22) are equal to such linear combinations of (22).
Theorem XIII. - The unique maximal system of quaternions
with rational coordinates having properties C, U, N is composed of
all quaternions whose four coordinates are either all rational
integers or all halves of odd integers.

## PDF page 37

316
L.-E. DICKSON.
A like conclusion was reached by Hurwitz for quaternions having
properties C, U, B, as required by his definition of integers. His proof
is much longer and more difficult then the above proof.
According to the definition of integer in this memoir, there is at
least one maximal system of integral quaternions, viz., the system of
Hurwitz, and its numbers would naturally be chosen as our integral
quaternions in view of their admirable properties as to factorization
into prime quaternions.
<b>18.</b> General Theory. — We shall now give a complete theory of
integers in any linear associative algebra, the coordinates of whose
numbers range over all complex numbers. There are two categories
of such algebras. For any algebra of the first category we may intro-
duce new units <math>\varepsilon_1, ..., \varepsilon_h, \gamma_1, ..., \gamma_k</math>, such that (1)
<math>\varepsilon_i^2 = \varepsilon_i, \quad \varepsilon_i \eta_{\rho} = \eta_{\rho}, \quad \eta_{\rho} \varepsilon_j = \eta_{\rho}, \quad \eta_{\rho} \eta_{\sigma} = \sum \gamma_{\rho \sigma \tau} \eta_{\tau},</math>
while all further products are zero. Here <math>\eta_{\sigma}</math>, <math>\eta_{\sigma}</math> and <math>\eta_{\tau}</math> are of charac-
ters <math>(i, j)</math>, <math>(j, l)</math> and <math>(i, l)</math>; while in the summation, <math>\tau > \rho</math>, <math>\tau > \sigma</math>.
For the general number
<math>z = x_1 z_1 + \ldots + x_h z_h + y_1 \eta_1 + \ldots + y_k \eta_k</math>
we have <math>\delta(\omega) = \Pi(x_i - \omega)^{m_i}</math>. Since <math>R(\omega)</math> is a divisor of the latter,
the maximal system of integers is composed of all the numbers z
in which the <math>x_i</math> are rational integers and the <math>y_j</math> are rational. We rea-
dily prove that <math>u = 1 + \sum a_j r_{ij}</math> is a unit if the <math>a_j</math> are any rational
numbers. For,
<math>u(1-a_1\eta_1)=1-a_1^2\eta_1^2+l_2=1+a_{12}\eta_2+l_3</math>
where <math>\ell_i</math> is a linear function of <math>\eta_i</math>, <math>\eta_{i+1}</math>, ..., with rational coefficients.
Similarly,
<math>(1 + a_{12}\eta_2 + l_3)(1 - a_{12}\eta_2) = 1 - a_{13}^2 \eta_3^2 + l_3' = 1 + a_{13}\eta_3 + l_4,</math>
<math>(1 + a_{13}\eta_3 + l_3)(1 - a_{13}\eta_3) = 1 + a_{14}\eta_4 + l_5.</math>
(1) E. Cartan, Annales de la Fac. Sc. de Toulouse, t. 12, 1898, B. 33; Dickson,
Linear Algebras, p. 44.

## PDF page 38

317
A NEW SIMPLE THEORY OF HYPERCOMPLEX INTEGERS.
We finally reach a product equal to 1. Hence
<math>uv = 1,</math> <math>v = (1 - a_1 \eta_1) (1 - a_{12} \eta_2) (1 - a_{13} \eta_3) \dots = 1 + \sum_{i=1}^{n} b_i \eta_i,</math>
where each <math>b_j</math> is rational. Thus c is an integer, and u and v are units.
If <math>x_1, ..., x_k</math> are given rational integers each <math>\neq</math> 0 and <math>y_1, ..., y_k</math> are
any rational numbers, <math>z = \sum x_i \varepsilon_i + \sum y_\rho \eta_\rho</math> is associated with <math>\sum x_i \varepsilon_i</math>, <math>i \in \mathbb{N}</math>,
there exists a unit c such that <math>z_i = \sum x_i z_i</math>. For, if u is the unit
<math>u = 1 + \sum x_i^{-1} y_0 \eta_0</math>
<math>\sum x_i \varepsilon_i u = z</math>. As shown above, there exists a unit <math>v</math> such that <math>uv = 1</math>.
Hence the arithmetic of any algebra of the first category is asso-
ciated (§ 15) with the arithmetic of the algebra which is the direct
<math>sum(\varepsilon_1)+\ldots+(\varepsilon_h).</math>
The units of an algebra of the second category (') fall into sets,
each corresponding to a unit of an algebra of the first category, and
having the multiplication table
<math display="block">e'_{\alpha\beta}e'_{\beta\gamma}=e'_{\alpha\gamma}, \qquad e'_{\alpha\beta}\eta^{\rho}_{\beta\gamma}=\eta^{\rho}_{\alpha\gamma}, \qquad \eta^{\rho}_{\beta\gamma}e'_{\gamma\delta}=\eta^{\rho}_{\beta\delta}, \qquad \eta^{\rho}_{\alpha\beta}\eta^{\sigma}_{\beta\gamma}=\sum_{i}\gamma_{\rho\sigma\tau}\eta^{\tau}_{\alpha\gamma}</math>
<math>(\tau > \rho, \tau > \sigma)</math>,
where the superscripts do not denote powers, the <math>\gamma</math>'s are constants,
and all further products of the <math>e</math> and <math>\eta</math> are zero.
Consider any number z of the algebra. Then
<math>z = x + y,</math> <math>x = \sum_{k,\lambda,\alpha} x_{\lambda\alpha}^k e_{\lambda\alpha}^k,</math> <math>y = \sum_{\rho,\lambda,\beta} y_{\lambda\beta}^\rho w_{\lambda\beta}^\rho.</math>
The right-hand characteristic determinant <math>\delta(\omega)</math> of z is known to be a
product of powers of the determinants
<math>\mathbf{D}_i(\boldsymbol{\omega}) = \left[ \begin{array}{ccccc} x_{11}^i & \cdots & x_{12}^i & \cdots & x_{1p_i}^i \\ \cdots & \cdots & \cdots & \cdots \\ x_{p_{i1}}^i & x_{p_{i2}}^i & \cdots & x_{p_{imi}}^i - \boldsymbol{\omega} \end{array} \right],</math>
which involve no coordinate of <math>y</math>. Hence <math>z</math> is an integer if and only
(1) CARTAN, loc. cit., B. 51; Dickson, loc. cit., p. 54.

## PDF page 39

318
1..-E. DICKSON.
if w is an integer, the coordinates of y being arbitrary rational num-
bers. Consider
<math display="block">u = 1 + \sum_{\beta, \alpha, \beta} a^{\beta}_{\alpha\beta} \, \eta^{\beta}_{\alpha\beta}.</math>
Then
<math display="block">x u = x + \sum_{\lambda, \rho, \alpha, \beta} \alpha_{\lambda \alpha}^{\rho} \alpha_{\alpha \beta}^{\rho} \eta_{\lambda \beta}^{\rho}</math>
will reduce to <math>x + y</math> if and only if
<math display="block">\sum_{\alpha} x_{\lambda\alpha}^{i} \alpha_{\alpha\beta}^{\flat} = y_{\lambda\beta}^{\flat} \qquad \text{(for all $\varrho$, $\lambda$, $\beta$).}</math>
Here <math>\alpha</math> and <math>\lambda</math> each take the same values 1, ..., <math>p_i</math>. The determinant of
the coefficients of <math>a_{i\beta}^{\rho}</math>, ..., <math>a_{p_i\beta}^{\rho}</math> is <math>D_i(\alpha)</math>, which is not zero if <math>N(x) \neq \alpha</math>.
Then the equations uniquely determine the <math>a</math>.
The proof that <math>u</math> is a unit is similar to that above :
<math display="block">u\left(1-\sum a_{\alpha\beta}^{1}\eta_{\alpha\beta}^{1}\right)=1+\sum_{\alpha\beta}b_{\alpha\beta}^{2}\eta_{\alpha\beta}^{2}.</math>
<b>3.</b> [3
α. p
whose product by
<math>1 - \sum b_{\alpha\beta}^2 \eta_{\alpha\beta}^2</math>
is
2 = 3
<math>1 + \sum_{\alpha,\beta} c^{\rho}_{\alpha\beta} \, \eta^{\rho}_{\alpha\beta},</math>
٠
We finally reach a product equal to 1. Hence <math>uv = 1</math> for
<math display="block">v = \left(1 - \sum_{\alpha,\beta} a_{\alpha\beta}^{\dagger} \eta_{\alpha\beta}^{\dagger}\right) \left(1 - \sum_{\alpha,\beta} b_{\alpha\beta}^{\dagger} \eta_{\alpha\beta}^{\dagger}\right) \left(1 - \sum_{\alpha,\beta} c_{\alpha\beta}^{\dagger} \rho_{\alpha\beta}^{\dagger}\right) \dots = 1 + \sum_{\rho,\alpha,\beta} c_{\alpha\beta}^{\rho} \eta_{\alpha\beta}^{\rho},</math>
where the g are rational. Thus c is an integer, and u and <math>v</math> are units.
Then <math>xu = z</math> gives <math>zv = x</math>. Thus every number z whose norm is not
zero is associated with its x component.
These & components are known to be the numbers of the algebra
which is the direct sum of several general matric algebras (§ 13).

## PDF page 40

•
319
A NEW SIMPLE THEORY OF HYPERCOMPLEX INTEGERS.
Applying Theorems VI and XI, and noting that our conclusion applies
also to algebras of the first category, we obtain
Theorem XIV. - The arithmetic of any linear associative algebra
the coordinates of whose numbers range over all complex numbers
is associated with the arithmetic of a direct sum of algebras each
with a single unit. Any number whose norm is not zero decomposes
into primes uniquely.
We therefore obtain only trivial arithmetics from algebras the
coordinates of whose numbers range over the field of all complex
numbers. If we restrict the coordinates and the coefficients of the
transformations of the units to the field of real numbers, we obtain
algebras in addition to those just investigated (for example, real qua-
ternions) and now obtain arithmetics which are not trivial. If we
employ the field of rational numbers, we obtain still further algebras
and a rich variety of arithmetics, which will form the subject of
the book cited in <math>\S 20</math>.
19. The Integers of Cayley's Algebra. — We employ the four
quaternion units <math>i, i, j, k</math> as well as the new units
<math>e=e_4</math>, <math>ie=e_5</math>, <math>je=e_6</math>, <math>ke=e_7</math>.
Any linear combination of these 8 basal units may be designated
by <math>x = q + Qe</math>, where
<math>q = x_0 + x_1 i + x_2 j + x_3 k</math>, <math>Q = x_4 + x_5 i + x_6 j + x_7 k</math>
(23)
are quaternions. Instead of employing Cayley's multiplication table
for these 8 units, it is far simpler to use the condensed law of multi-
plication
(21) <math>(q+Qe)(r+Re)=t+Te</math>, <math>t\equiv qr-R'Q</math>, <math>T\equiv Rq+Qr'</math>,
found by the writer ('), who also discovered that both right-hand
and left-hand division, except by zero, is always uniquely possible.
(1) Diekson, Linear Algebras, p. 15.
42
Journ. de Math., tome II. - Fasc. III, 1923.

## PDF page 41

320
L.-E. DICKSON.
Here r' denotes the quaternion conjugate to <math>r(\S 5)</math>. Unlike all the
earlier algebras in this memoir, the present algebras is not asso-
ciative.
As a special case of (24), the product of <math>x</math> by <math>q'-Qe</math> in either
order is
<math>qq' + QQ' = x_0^2 + \ldots + x_0^2</math>
which is the norm <math>N(x)</math> of x, since it is the constant term of the qua-
dratic equation satisfied by x. We have
<math>N(xy) = N(x)N(y)</math>.
We shall determine all maximal sets of integers <math>x</math> with rational
coordinates having properties C, U, N.
With <math>x</math>, also <math>x + i</math>, <math>x + i</math>, ..., <math>x + e_i</math>, are integers. From their
norms we subtract N(x) and conclude that <math>2x_0 + 1, ..., 2x_7 + 1</math>, are
all rational integers. Hence
<math>x_t = \frac{1}{2}X_t</math>  <math>(t = 0, ..., 7),</math>
where each <math>X_t</math> is a rational integer. Since <math>N(x)</math> is a rational integer,
<math>\Sigma X_t^2</math> is divisible by 4. According as <math>X_t</math> is even or odd, <math>X_t^2</math> has the
remainder o or i when divided by 4. Hence the number of odd X,
is 0, 4 or 8. In the first and third cases, q and Q are Hurwitz's integral
quaternions. By annexing e to all such quaternions, we obtain a
system H containing our <math>x</math>, and forming a part of the larger system
(30) obtained below.
Hence let exactly four of the eight coordinates of <math>x = q + Qe</math> be
halves of odd integers, the four not being those of <math>q</math>, nor those of <math>Q</math>
(otherwise <math>x</math> is in H). If three of those four are in one of <math>q</math>, Q, and
hence the fourth in the other, then, by employing <math>xe</math> instead of <math>x</math> if
necessary, we may assume that three are in <math>Q</math> and one in <math>q</math>. After
multiplying x on the left by 1, i, j, or k, we may assume that <math>x_0</math> is
half an odd integer, while <math>x_1, x_2, x_3</math> are rational integers. Subtracting
from x a quaternion with rational integral coordinates, we get
<math>\frac{1}{2} + Q_1 e</math>. Its product by <math>1 + i</math> is <math>\frac{1}{2}(1 + i) + Q_1 e</math>, which falls under the
next case.

## PDF page 42

321
A NEW SIMPLE THEORY OF HYPERCOMPLEX INTEGERS.
Next, let exactly two of the coordinates of <math>q</math> and two of those of <math>Q</math>
be halves of odd integers. After multiplying <math>w</math> on the left by <math>i, i, j</math>,
or k, we may take <math>x_0</math> as half an odd integer. Since the multiplication
table (7) of quaternions is unaltered by a cyclic permutation of <math>i, j, k</math>,
we may treat only one of three analogous cases (and at the end of our
discussion draw similar conclusions for the two omitted cases), and
hence assume here that <math>w_i</math> is half an odd integer, while <math>w_a</math> and <math>w_a</math> are
rational integers. Then by subtracting a quaternion with rational
integral coordinates, we get <math>q = \frac{1}{2}(1+i)</math>. Since
<math>i \cdot v + 1 = iq + 1 + (Qi)e, \quad iq + 1 = q,</math>
we may replace Q by Qi without disturbing q. Hence if either <math>x_4</math>
or <math>x_5</math> of Q is half an odd integer, we may take <math>x_5</math> to be that one. After
subtracting Re, where R is a quaternion with rational integral coor-
dinates, we have the cases
(25) <math>Q = \frac{1}{2}(1+i), \frac{1}{2}(1+j), \frac{1}{2}(1+k), \frac{1}{2}(j+k).</math>
We shall reduce these cases to the second, for which x is
<math display="block">Z = \frac{1}{2}(1+i) + \frac{1}{2}(1+j)e,</math>
(36)
whence
<math>(i+j)Z = \frac{1}{2}(i+i+j-k) + je,</math>
so that the set contains
<math display="block">\rho = \frac{1}{2}(1+i+j+k),</math>
(27)
and hence all of Hurwitz's integral quaternions. We shall assume that
the latter occur in our set in all cases.
For the first case <math>(25)</math>, <math>x</math> is
<math display="block">L = \frac{1}{2}(1+i) + \frac{1}{2}(1+i)e.</math>

## PDF page 43

322
L.-E. DICKSON.
Then
<math>(\rho e)L = \frac{1}{2}(-1-j) + \frac{1}{2}(1+k)e.</math>
Apply the cyclic permutation <math>(ikj)</math> and to the result add <math>i+i</math>; we
get Z. In the third case (25), replace <math>j</math> by <math>-k</math>, and <math>k</math> by <math>j</math> (so that
the multiplication table of quaternion units is unaltered); we get the
second case (25). In the fourth case (25), we add
<math display="block">\frac{1}{2}(1+i-j-k)e.</math>
which belongs to our set by hypothesis, and get the first case (25).
Hence all cases have now been reduced to (26).
Since the set contains Z, it contains
<math>eZ = w \equiv \frac{1}{2}(-1+j) + \frac{1}{2}(1-i)e,</math> <math>(\rho e)Z = v \equiv \frac{1}{2}(-1-k) + \frac{1}{2}(1+k)e.</math>
Adding <math>1 + ie</math> to w, and <math>1 + k</math> to v, we get
(28) <math>W = \frac{1}{2}(1+j) + \frac{1}{2}(1+i)e</math>, <math>V = \frac{1}{2}(1+k) + \frac{1}{2}(1+k)e</math>.
The followings 8 numbers
i. j, k, <math>\rho</math>, e, W, Z, V
(29)
are evidently linearly independent. In view of 2W, 2Z, 2V, 2p, we
may express ie, je, ke, 1 as linear functions of the numbers (29) with
rational integral coefficients. Note also that
<math>\rho e = Z - W + V + ie - i - i - k</math>
Hence all of the numbers previously mentioned as belonging to our
system of integers are linear functions of the eight in (29) with
rational integral coefficients. It can be verified that this is true also of
the product of any two of the numbers (29). Hence the system of
numbers
<math display="block">\int x = x_0 \rho + x_1 i + x_2 j + x_3 k + x_4 e + x_5 W + x_6 Z + x_7 V</math>
<math display="block">(x_0, \dots, x_7 \text{ rational integers})</math>
(30)

## PDF page 44

323
A NEW SIMPLE THEORY OF HYPERCOMPLEX INTEGERS.
has the properties U and C. It has the property N, since
(31) <math>x = \frac{1}{2}(x_0 + x_3 + x_6 + x_7) + \left(x_1 + \frac{1}{2}x_0 + \frac{1}{2}x_6\right)i + \left(x_2 + \frac{1}{3}x_0 + \frac{1}{2}x_3\right)J</math>
<math>+\left(x_{3}+\frac{1}{2}x_{0}+\frac{1}{2}x_{7}\right)k+\left[x_{3}+\frac{1}{2}(x_{5}+x_{6}+x_{7})\right]e^{-\frac{1}{2}}</math>
<math>+\frac{1}{2}x_3ie+\frac{1}{2}x_6je+\frac{1}{2}x_7ke</math>
the sum of the squares of whose eight components is the rational
integer
<math>N(x) = x_0^2 + ... + x_2^2 + x_0(x_1 + x_2 + x_3 + x_5 + x_6 + x_7)</math>
<math>+ x_1(x_3 + x_6 + x_7) + x_1x_6 + x_2x_3 + x_3x_7 + x_5x_6 + x_5x_7 + x_6x_7</math>
If we make any enlargement of this system (30), we obtain a system
not having properties U, C, N. For, let us annex <math>u = q + Qe</math>, four
of whose coordinates are rational integers, while four are the halves
of odd integers. First, let two of the latter be coordinates of q and
two of Q. This will be true also of <math>u</math>, <math>iu</math>, <math>ju</math>, <math>ku</math>, in one of which <math>x_*</math>
is half an odd integer. After subtracting Re, where R has rational
coordinates, we may take
<math>Q = \frac{1}{2}(i+i), \quad \frac{1}{2}(i+j), \quad \text{or} \quad \frac{1}{2}(i+k).</math>
In the respective cases, we subtract W, Z, or V from u and get a
number lacking <math>e</math> and hence a quaternion <math>r</math>. If <math>r</math> is in Hurwitz's
arithmetic, r is in our system (30), and we have caused no enlargement
by annexing u. Hence r is not in Hurwitz's arithmetic and therefore
enlarges it to a system of quaternions not having properties U, C, N
<math>(\S 17).</math>
Finally, let exactly three of the coordinates of <math>Q</math> and one of <math>q</math> be
halves of odd integers (the reverse case reducing to this after multi-
plication by e). As above we may assume that <math>q = \frac{1}{2}</math>, while three of
the coordinates of Q are <math>\frac{1}{2}</math> and the fourth is zero. Subtracting <math>\rho e</math>, we
get <math>\frac{1}{2} - \frac{1}{2}le</math>, where <math>l = 1</math>, <math>i</math>, <math>j</math>, or <math>k</math>. But the norm is now <math>\frac{1}{2}</math> and not
a rational integer. Hence our system is a maximal.

## PDF page 45

324
L.-E. DICKSON.
Theorem XV. - The only maximal systems of integers of Cayley's
algebra having properties C, U, N are (30) and the two systems
obtained from it by cyclic permutations of <math>i, j, k</math>.
For the system (30) there are exactly 240 units:
<math>\pm i</math>, <math>\pm i</math>, <math>\pm j</math>, <math>\pm k</math>, <math>\pm e</math>, <math>\pm ie</math>, <math>\pm je</math>, <math>\pm ke</math>,
<math>u = \frac{1}{2}(\pm i \pm i \pm j \pm k), ue,</math>
<math display="block">\frac{1}{2}(\pm i \pm j) + \frac{1}{2}(\pm i \pm i)e, \qquad \frac{1}{2}(\pm i \pm j) + \frac{1}{2}(\pm j \pm k)e,</math>
<math>\frac{1}{2}(\pm i \pm i) + \frac{1}{2}(\pm i \pm j)e, \qquad \frac{1}{2}(\pm i \pm i) + \frac{1}{2}(\pm i \pm k)e,</math>
<math>\frac{1}{2}(\pm 1 \pm k) + \frac{1}{2}(\pm 1 \pm k)e</math>, <math>\frac{1}{2}(\pm 1 \pm k) + \frac{1}{2}(\pm i \pm j)e</math>,
<math>\frac{1}{2}(\pm i \pm k) + \frac{1}{2}(\pm i \pm i)e, \qquad \frac{1}{2}(\pm i \pm k) + \frac{1}{2}(\pm j \pm k)e,</math>
<math>\frac{1}{2}(\pm j \pm k) + \frac{1}{2}(\pm i \pm j)e, \qquad \frac{1}{2}(\pm j \pm k) + \frac{1}{2}(\pm i \pm k)e,</math>
<math>\frac{1}{2}(\pm i \pm j) + \frac{1}{2}(\pm i \pm k)e, \qquad \frac{1}{2}(\pm i \pm j) + \frac{1}{2}(\pm i \pm j)e.</math>
There are many ways to express 2 as the product of an integer f
by its conjugate : <math>f = i + i</math>, or a number with any two coordinates
<math>\pm 1</math> and the others zero; <math>f = \rho + e</math>, for <math>\rho</math> in (27), or a number with
any four coordinates <math>\pm \frac{1}{2}</math>, one <math>\pm 1</math>, and three zero; <math>f = q + Qe</math>,
where q and Q are both of the form
<math>\frac{1}{2}(\pm 1 \pm i \pm j \pm k).</math>
Note that
<math>(1+i)\sigma = \rho + \rho e, \qquad \sigma = \frac{1}{2}(1+j) + \frac{1}{2}(1+k)e,</math>
<math>\tau(1+i) = \rho + \rho e, \qquad \tau = \frac{1}{2}(1+k) + \frac{1}{2}(i+j)e,</math>
where <math>\tau</math> is a unit, but <math>\sigma</math> is not an integer (30). Thus <math>\rho + \rho c</math> is the pro-
duct of <math>i + i</math> on the left by a unit, but not on the right. Again
<math>\lambda = (1+i)\lambda = \rho + c, \qquad \lambda = \frac{1}{2}(1+j) + \frac{1}{2}(1-i)e = \text{unit.}</math>

## PDF page 46

325
A NEW SIMPLE THEORY OF HYPERCOMPLEX INTEGERS.
But it would be very laborious to prove that two integers of the same
norm are not associates if we permit unit factors both on the right
and left simultaneously.
If <math>g</math> is a given integer (30), we can find an integer <math>q</math> of the same
form (30) such that
<math display="block">N(g-mq) \subseteq \frac{5}{4}m^2,</math>
where <math>m</math> is any given positive rational integer. When <math>a</math> and <math>b</math> are any
given integers, we can find integers <math>q</math> and <math>c</math> such that
<math>a = qb + c</math>, <math>N(c) \in \frac{5}{4}N(b)</math>.
Take (') <math>g = a\bar{b}</math>, <math>m = b\bar{b}</math>, and write c for <math>a - qb</math>. We readily verify
by (24) that <math>(qb)\bar{b} = qm</math>, although the associative law usually fails
here. Thus
<math>g-qm = (a-qb)\overline{b} = c\overline{b}, \quad N(c)N(\overline{b}) = \frac{5}{4}m^2.</math>
For integral quaternions, Hurwitz proved similarly that
<math>N(g-mq) < m^2</math>, <math>a = bq + c</math>, <math>N(c) < N(b)</math>,
and hence established the existence of a right-hand greatest common
divisor of a and b. Since we are unable to prove its existence for our
integers (30), we have no valid reason to prefer the system (30), or
one of its two equivalents, to other maximal systems (if such exist)
having properties C, U,, N, M.
20. Outlook. — We investigated above the integers of the classic
canonical algebras to which any algebra in 2, 3, or 4 basal units can
be reduced by a linear transformation with real coefficients. If we
restrict attention to transformations with rational coefficients, we'
obtain a much larger list of canonical algebras. The arithmetic of the
(1) If <math>b = r + Re</math>, we write <math>\vec{b}</math> for <math>r' - Re</math>, where <math>r'</math> is the conjugate of the
quaternion <math>r</math>.

## PDF page 47

326
L.-E. DICKSON. - THEORY OF HYPERCOMPLEX INTEGERS.
· new algebras not in the former list will have new types of properties.
In particular, we may now secure unique factorization into primes,
only after the introduction of ideals. This becomes evident if we recall
that an algebraic number field of degree <math>n</math> is a special type of linear
algebra in <math>n</math> basal units. This more general theory of hypercomplex
integers will be presented in the author's book, Algebras and Their
Arithmetics, in course of publication by the University of Chicago
Press.
三号
£ 8 "
•
1


·
.
⊾
