Source: https://annas-archive.gl/md5/5c03dc8a5d3f840b4d7f18def1d16a05
PDF sha256: de0333ee5c62027a264337dbd6bcb351f1806bf901fc77d2f416e6b31a3fcfcf
License: public domain (L. E. Dickson, Duke Math. J. 1 (1935) 113-125, published in the United States in 1935, copyright not renewed)

# Transcription of dickson_1935_linear_algebras_with_associativity_not_assumed.pdf

Transcription of `dickson_1935_linear_algebras_with_associativity_not_assumed.pdf` in this directory, 13 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 1-13 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories. No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

LINEAR ALGEBRAS WITH ASSOCIATIVITY NOT ASSUMED
By L. E. Dickson
1. The complete structure of linear associative algebras was known to depend
upon the division algebras. When the reference field <math>F</math> is an algebraic field,
H. Hasse has recently proved that every normal division algebra is cyclic.
This perfection of the theory of associative algebras justifies attention to non-
associative algebras.
Known examples of non-associative division algebras are Cayley's algebra of
order 8, and the writer's commutative algebras of orders 3 and <math>2n</math> (§15).
Many
new division algebras of order 4 are given here by Theorems 2 and 3.
In §§7–11 we determine all types of algebras of order 3 having a principal
unit (or modulus) denoted by 1. Except for special values of the parameters,
these algebras are simple. It is known that every associative simple algebra
of order 3 is a division algebra.
Thus the structure theorems for associative algebras fail in general for non-
associative algebras. Similarly for other properties. Consider the algebra A
of order 4 with <math>e_1^2 = e_2</math>, <math>e_2e_1 = e_3</math>, and all further <math>e_ie_j = 0</math>. For <math>X = x_0 + e_1</math>
<math>\sum x_i e_i</math>, evidently <math>(X - x_0)(X - x_0)^2 = 0</math>, so that A has the left rank 3. But
its right rank is 4 since 1, <math>e_1</math>, <math>e_1^2 = e_2</math>, <math>e_1^2 e_1 = e_3</math> are linearly independent. Al-
gebra (37) with 13 parameters also has left and right ranks 3 and 4.
Part I. Rank 2
2. In case the field F has a modulus p, assume that <math>p \neq 2</math>.
<b>Lemma 1.</b> If 1, u, v are linearly independent with respect to F, and <math>u^2 = a + cu</math>,
<math>v^2 = b + dv</math>, then
<math display="block">uv + vu = du + cv + f,</math>
<math>f</math> in <math>F</math>.
Write t for <math>a + b + cu + dv</math>. Then
<math>(u + v)^2 = t + uv + vu = r + s(u + v)</math>
<math>(u-v)^2 = t - uv - vu = R + S(u-v)</math>.
Addition yields <math>s + S = 2c</math>, <math>s - S = 2d</math>. Subtraction gives Lemma 1.
Received March 25, 1935.
<sup>1</sup> If only the numbers of F are commutative with every element.
<sup>2</sup> Linear Algebras, Cambridge Tract No. 16, p. 14, p. 69 (p. 17 for the characteristic
equations); On triple algebras and ternary cubic forms, Bull. Amer. Math. Soc., vol. 14
(1907-8), pp. 160-169, p. 169; Linear algebras in which division is always uniquely possible,
Trans. Amer. Math. Soc., vol. 7 (1906), pp. 370-390; On commutative linear algebras in
which division is always uniquely possible, ibid., pp. 514-522.
113

## PDF page 2

114
L. E. DICKSON
3. After adding scalars (numbers of <math>F</math>) to the initial units, we obtain a basis
1, <math>e_1, \dots, e_n</math>, where <math>e_i^2 = a_i</math>. By Lemma 1,
<math>(i \neq j)</math>.
<math>e_i e_j + e_j e_i = b_{ij}</math>
We get <math>e_i e_i</math> from the latter and
<math display="block">e_i e_j = c_{ij} + \sum_{k=1}^n c_{ijk} e_k</math>
<math>(i < j)</math>.
Using summations for <math>i = 1, \dots, n</math>, let
<math>X = \xi + \Sigma x_i e_i,</math> <math>Y = \eta + \Sigma y_i e_i,</math> <math>XY = P_0 + \Sigma P_i e_i.</math>
Let <math>\Sigma'</math> denote summation for <math>i, j = 1, \dots, n</math> with <math>i < j</math>. Then
<math display="block">P_0 = \xi \eta + \sum x_i y_i a_i + \sum' b_{ij} x_j y_i + \sum' (x_i y_j - x_j y_i) c_{ij},</math>
<math>P_k = \xi y_k + \eta x_k + \Sigma'(x_i y_i - x_j y_i) c_{ijk}</math>  <math>(k = 1, \dots, n)</math>.
The right determinant <math>\Delta(X)</math> is defined to be the determinant of the coeffi-
cients of <math>\eta</math>, <math>y_1, \dots, y_n</math> in <math>P_0, P_1, \dots, P_n</math>. Multiply the first column by <math>-\xi</math>
and the <math>(j + 1)</math>-st column by <math>x_j</math> (for <math>j = 1, \dots, n</math>) and add. The sum is
the value of <math>P_k</math> for <math>\eta = -\xi</math>, <math>y_i = x_i</math>. For <math>k \ge 1</math>, <math>P_k</math> evidently vanishes. Since
Y becomes <math>-X'</math>, where X' is the conjugate of X, <math>P_0</math> becomes the negative of
the norm of <math>X</math>.
The right determinant <math>\Delta(X)</math> and left determinant <math>\Delta'(X)</math> of any
THEOREM 1.
algebra of rank 2 are both divisible by the norm <math>N(X)</math>.
The quotient is obtained at once from the cofactor of any element in the
first row (cf. §5).
4. Division algebras of rank 2. We assume that if any product of two
factors is zero, then one factor is zero.
LEMMA 2. If 1, u, v are linearly independent in F, then 1, u, v, uv are linearly
independent in <math>F</math>.
We can choose <math>m</math> and <math>n</math> in <math>F</math> such that
<math>U = u - m,</math> <math>V = v - m,</math> <math>U^2 = a,</math> <math>V^2 = k.</math>
By Lemma 1, <math>UV + VU = 2c</math>. Take <math>e_1 = U</math>, <math>e_2 = V - ca^{-1}U</math>. Then
<math>e_1^2 = a,</math> <math>e_2^2 = b,</math> <math>e_1e_2 + e_2e_1 = 0.</math>
If <math>a = k^2</math>, k in F, then <math>(e_1 - k)(e_1 + k) = 0</math>, <math>e_1 = \pm k</math>, whereas 1 and <math>e_1</math>
are linearly independent in <math>F</math>. Hence
<math>a \neq \text{square in } F</math>,
<math>b \neq \text{square in } F</math>.
(1)
If 1, <math>u</math>, <math>v</math>, <math>uv</math> are linearly dependent in <math>F</math>, the same is true of 1, <math>U</math>, <math>V</math>, <math>UV</math>
and of 1, <math>e_1</math>, <math>e_2</math>, <math>e_1e_2</math>. Hence <math>e_1e_2 = r + se_1 + te_2</math>, where <math>r</math>, <math>s</math>, <math>t</math> are in <math>F</math>. Then

## PDF page 3

115
LINEAR ALGEBRAS
<math>(e_1-t)\left(e_2+\frac{r+st}{t^2}e_1+\frac{rt+as}{t^2}e_1\right)=0</math>,
whereas neither factor is zero. This proves Lemma 2.
Since we may take <math>e_1e_2</math> as the fourth basal element <math>e_3</math>,
<math>e_1^2 = a</math>, <math>e_2^2 = b</math>, <math>e_1e_2 = e_3</math>, <math>e_2e_1 = -e_3</math>.
(2)
Write <math>e_i^2 = c_i + 2m_i e_i</math> for <math>i \ge 3</math>. Apply Lemma 1 with <math>(u, v) = (e_i, e_i)</math>,
<math>(e_2, e_i), (e_i, e_j)</math> in turn. We get
<math>e_1e_i + e_ie_1 = g_i + 2m_ie_1,</math> <math>e_2e_i + e_ie_2 = h_i + 2m_ie_2</math> <math>(i \ge 3)</math>,
(3)
<math>e_i e_j + e_j e_i = t_{ij} + 2m_i e_j + 2m_j e_i</math> <math>(i, j \ge 3, i \ne j)</math>.
Write <math>x = \xi + \sum x_i e_i</math>. Squaring <math>x - \xi</math>, we get
<math display="block">x^2 = 2x \Big(\xi + \sum_{i=1}^n x_i m_i\Big) - N,</math>
<math display="block">N = \xi^2 + 2\xi \sum x_i m_i - ax_1^2 - bx_2^2 - \sum c_i x_i^2 - \sum g_i x_1 x_i - \sum h_i x_2 x_i - \sum t_{ij} x_i x_j,</math>
where the summations are for <math>i \geq 3, j \geq 3</math>, while <math>i < j</math> in <math>\Sigma'</math>. Thus (2) and (3)
imply that every element <math>x</math> of the algebra satisfies a quadratic equation. Evi-
dently <math>N</math> is the norm <math>xx'</math> of <math>x</math>. Also,
<math>x^2</math> is scalar if and only if <math>\xi = -\sum_{i=1}^n x_i m_i</math>.
(4)
We may choose a basis satisfying (2) and <math>e_3^2 = \text{scalar}</math>. Proof is needed only
when <math>m_3 \neq 0</math>. Use the basis
<math>e_1, 	 E_2 = x = \xi + \sum x_i e_i, 	 E_3 = e_1 E_2.</math>
1,
where (4) holds. Then
<math display="block">e_1E_2 + e_2E_1 = 2ax_1 + \sum_{i=1}^{n} g_ix_i</math>
becomes zero by choice of <math>x_1</math>. Let
<math display="block">e_1e_i = k_i + \sum_{i=1}^n c_{ij}e_j</math>
<math>(i \geq 3)</math>.
Then
<math>E_3 = s + \xi e_1 + x_2 e_3 + \sum_{i=1}^n \left(\sum_{i=2}^n x_i c_{ij}\right) e_i, \quad s = ax_1 + \sum_{i=2}^n x_i k_i.</math>
By (4), <math>E_3^2</math> is scalar if
<math>s + m_3(x_2 + \sum_{i=1}^n x_i c_{i3}) + \sum_{i=1}^n m_i \left( \sum_{i=1}^n x_i c_{ij} \right) = 0.</math>
This and the former condition hold if, for example,
<math>x_i = 0 \ (i \ge 4), \quad x_3 = 2, \quad x_1 = -g_3/a, \quad m_3 x_2 = g_3 - 2k_3 - 2 \sum_{i=0}^{\infty} m_i c_{3i}.</math>

## PDF page 4

116
L. E. DICKSON
LEMMA 3. There exists a basis satisfying (2) and (3) with <math>m_3 = 0</math>.
5. Case <math>n = 3</math>. Employ (2) and
<math>e_1e_3 = c_0 + c_1e_1 + c_2e_2 + c_3e_3,</math> <math>e_2e_3 = d_0 + d_1e_2 + d_2e_2 + d_3e_3,</math> <math>e_3^2 = f,</math> <math>e_3e_1 = g - e_1e_3,</math> <math>e_3e_2 = h - e_2e_3,</math>
(5)
which follow from (3). As in Section 3, <math>\Delta(x)</math> is
<math display="block">\begin{vmatrix} \xi & ax_1 + (g - c_0)x_3 & bx_2 + (h - d_0)x_3 & c_0x_1 + d_0x_2 + fx_3 \\ x_1 & \xi - c_1x_3 & -d_1x_3 & c_1x_1 + d_1x_2 \\ x_2 & -c_2x_3 & \xi - d_2x_3 & c_2x_1 + d_2x_2 \\ x_3 & -x_2 - c_3x_3 & x_1 - d_3x_3 & c_3x_1 + d_3x_</math>
which is the product of
<math display="block">-N(x) = -\xi^2 + ax_1^2 + bx_2^2 + fx_3^2 + gx_1x_3 + hx_2x_3</math>
<b>(6)</b>
and the quotient by <math>-x_3</math> of the minor obtained by deleting the first row and
last column. This quotient is
<math>-\xi^2-c_3\xi x_1-d_3\xi x_2+(c_1+d_2)\xi x_3+c_2x_1^2+(d_2-c_1)x_1x_2</math>
<b>(</b>7)
<math>-d_1x_2^2 + (c_3d_2 - c_2d_3)x_1x_3 + (c_1d_3 - c_3d_1)x_2x_3 + (c_2d_1 - d_1d_2)x_3^2</math>
Similarly, the left determinant <math>\Delta'(x)</math> is the product of (6) by the function
derived from (7) by changing the sign of <math>\xi</math>.
Theorem 2. The algebra R over F defined by (2) and (5) is a division algebra
if and only if neither (6) nor (7) is zero for values of <math>\xi</math>, <math>x_1</math>, <math>x_2</math>, <math>x_3</math> in the field not
all zero. The forms (6) and (7) are identical if and only if R is the algebra S
defined by <math>(2)</math> and
<math>e_3^2 = -ab,</math> <math>e_1e_3 = c_0 + ae_2,</math> <math>e_3e_1 = -e_1e_3,</math>
(8)
<math>e_2e_3=d_0-be_1, \qquad e_3e_2=-e_2e_3.</math>
In R the product of the norms of any two elements is the norm of their product if
and only if R is the algebra Q defined by (2) and (8) with <math>c_0 = d_0 = 0</math>, whence Q
is the generalized quaternion algebra and obeys the associative law.
In the products of (6) and (7) by <math>-1</math> and <math>-4</math>, respectively, we complete
the square on <math>\xi</math>, then on <math>x_1</math>, and finally on <math>x_2</math>. We obtain forms having only
square terms with the coefficients
(6')
<math>1, -a, -b, -f + g^2/(4a) + h^2/(4b)</math>;
<math>1, -A, -B, D + C^2/B,</math>
(7')
<sup>3</sup> Or the quotient by <math>x_2</math> of the minor obtained by deleting the first row and third col-
umn, etc.

## PDF page 5

117
LINEAR ALGEBRAS
where
<math>A = c_3^2 + 4c_2</math>, <math>B = d_3^2 - 4d_1 - U^2/A</math>, <math>U = 2(c_1 - d_2) - c_3d_3</math>
<math>W = c_1c_3 + 2c_2d_3 - c_3d_2, \qquad C = 2c_3d_1 - c_1d_3 + d_2d_3 + UW/A,</math>
<math display="block">D = 4(c_1d_2 - c_2d_1) - (c_1 + d_2)^2 + W^2/A.</math>
When <math>F</math> is the field of all real numbers, the condition for a division algebra
is that the numbers <math>(6')</math> and <math>(7')</math> be all positive.
When F is any field, <math>x^2 - ay^2 - bz^2 + mw^2</math> is not zero for values of <math>x, \dots, w</math>
in F not all zero if and only if a is not a square in F, b is not represented by
<math>x^2 - ay^2</math>, nor <math>-m</math> by <math>x^2 - ay^2 - bz^2</math>, for values in F of the variables. The
final condition is redundant<sup>4</sup> if <math>m = ab</math>.
The case <math>c_3 = d_3 = c_1 = d_2 = g = h = 0, f = -ab</math>, yields the
Corollary. The algebra defined by (2) and
<math>e_1e_3=c_0+ce_2</math>, <math>e_2e_3=d_0-de_1</math>, <math>e_3^2=-ab</math>, <math>e_3e_1=-e_1e_3</math>, <math>e_3e_2=-e_2e_3</math>
is a division algebra if and only if a and c are not squares in F, b is not repre-
sented by <math>x^2 - ay^2</math>, and d is not represented by <math>x^2 - cy^2</math>. When <math>c = a</math>, <math>d = b</math>,
this algebra is <math>S</math> of Theorem 2.
6. Normalization. Employ a new basis of <math>R</math>:
1, <math>E_1</math>, <math>E_2</math>, <math>E_3 = E_1 E_2</math>, <math>E_1^2</math> and <math>E_2^2</math> scalar.
(9)
By (4)
<math>E_2 = \sum y_i e_i</math>
<math>E_1 = \sum x_i e_i</math>
<math>(i = 1, 2, 3)</math>.
(10)
By Lemma 2, (9) is a basis if and only if the <math>x_i</math> are not proportional to the <math>y_i</math>.
The condition for <math>E_1E_2 + E_2E_1 = 0</math> is <math>C(x_i, y_i) = 0</math>, viz.,
<math display="block">(11) \quad 2t + g(x_1y_3 + x_3y_1) + h(x_2y_3 + x_3y_2) = 0, \quad t = ax_1y_1 + bx_2y_2 + fx_3y_3.</math>
We get <math>E_3 = f_0 + \sum f_i e_i</math>, where
<math display="block">f_0 = t + c_0 x_1 y_3 + (y - c_0) x_3 y_1 + d_0 x_2 y_3 + (h - d_0) x_3 y_2,</math>
<math>f_i = c_i L + d_i M</math> <math>(i = 1, 2),</math> <math>f_3 = c_3 L + d_3 M + N,</math>
(12)
<math>L = x_1y_3 - x_3y_1,</math> <math>M = x_2y_3 - x_3y_2,</math> <math>N = x_1y_2 - x_2y_1.</math>
We require that <math>E_3^2</math> be scalar, viz., <math>f_0 = 0</math>. Next <math>C(x_i, f_i) = 0</math> is the condition
for <math>E_1E_3 + E_3E_1 = 0</math>. We now have three linear homogeneous equations in
<math>y_1, y_2, y_3</math>. The determinant D of their coefficients is a quartic form in the <math>x_i</math>.
Assume that <math>D = 0</math> has solutions not all zero in <math>F</math>. Then our three equations
hold if the <math>y_i</math> are the cofactors of the elements of the third row of <math>D</math>. For these
values (quadratic functions of the <math>x_i</math>) of the <math>y_i</math>, the condition <math>C(y_i, f_i) = 0</math>
<sup>4</sup> L. E. Dickson, Algebren und ihre Zahlentheorie, Zürich, 1927, p. 47.

## PDF page 6

118
L. E. DICKSON
for <math>E_2E_3 + E_3E_2 = 0</math> becomes an equation in the <math>x_i</math> of degree 5. This has
solutions in common with <math>D=0</math>, but not necessarily in <math>F</math>. Hence in general
we may normalize algebra <math>R</math> so that <math>g = h = 0</math>.
Consider the normalization of algebra <math>S</math> defined by (2) and (8). Here (11)
and <math>f_0 = 0</math> become
<math>ax_1y_1 + bx_2y_2 - abx_3y_3 = 0,</math> <math>c_0L + d_0M = 0.</math>
(13)
When (13) hold, the new basis (9) satisfies equations (2) and (8) written in capital
letters if and only if
<math display="block">A = ax_1^2 + bx_2^2 - abx_3^2, 	 B = ay_1^2 + by_2^2 - aby_3^2,</math>
(14)
<math>AB + ab(aL^2 + bM^2 - N^2) = 0</math>
(15)
<math>C_0 = ab(x_2L - x_1M - x_2N) + c_0(x_1N + bx_3M) + d_0(x_2N - ax_3L),</math>
(16)
while <math>D_0</math> is derived from (16) by replacing <math>x_i</math> by <math>y_i</math>. Using the definitions (12)
and (14), we find that the left member of (15) reduces to the square of the
first sum in (13). Hence we may discard (15).
To make <math>C_0 = 0</math> for solutions of (13), we have three linear homogeneous
equations in the <math>y_i</math>; the determinant of their coefficients is a quartic form in
the <math>x_i</math>, which must vanish.
For the special case <math>c_0 = d_0 = 0</math>, <math>C_0</math> and <math>D_0</math> are identically zero by (12). Hence
every normalization of a generalized quaternion algebra is made by the new units
(10) and <math>E_3 = E_1 E_2</math>, where the <math>x_i</math> are not proportional to the <math>y_i</math> and satisfy the
single equation <math>(13_1)</math>; the new parameters are <math>(14)</math>.
7. Triple algebras of rank 2. By the first two sentences of §3,
<math>e_1^2 = a</math>, <math>e_2^2 = b</math>, <math>e_1e_2 = c + de_1 + fe_2</math>, <math>e_2e_1 = g - de_1 - fe_2</math>.
If <math>d = f = 0</math>, we have (17) with <math>k = 0</math>. If d and f are not both zero, we
may interchange the e's, if necessary, and take <math>d \neq 0</math>. Write
<math>E_2 = d^{-1}e_2,</math>
<math display="block">E_1 = de_1 + fe_2,</math>
<math>E_1E_2 = c + bf/d + E_1,</math> <math>E_2E_1 = g + bf/d - E_1.</math>
Hence every triple algebra of rank 2 is equivalent to<sup>5</sup>
(17) <math>e_1^2 = a</math>, <math>e_2^2 = b</math>, <math>e_1e_2 = c + ke_1</math>, <math>e_2e_1 = g - ke_1</math> <math>(k = 0 \text{ or } 1)</math>.
Every transformation of units for which the <math>E_i^2</math> are scalar is
<math>E_1 = re_1 + se_2,</math> <math>E_2 = te_1 + we_2,</math> <math>D = rw - st \neq 0.</math>
(18)
Then <math>E_1E_2 = kDe_1 + \text{scalar}</math>. Let (17) hold in capital letters. Then <math>kDe_1 =</math>
<math>KE_1</math>, whence <math>kD = Kr</math>, <math>Ks = 0</math>. Hence an algebra (17) with <math>K = 0</math> is not
equivalent to one with <math>k \neq 0</math>.
<sup>5</sup> If <math>k = 0</math>, we may take <math>c = 0</math> unless <math>a = b = c + g = 0</math>.

## PDF page 7

119
LINEAR ALGEBRAS
I. <math>k = 1</math>. Then <math>K = 1</math>, <math>s = 0</math>, <math>w = 1</math>, <math>r \neq 0</math>. Then <math>E_2E_1 = G - E_1</math>,
<math>G = r(g + ta), E_1E_2 = C + E_1, C = r(c + ta).</math>
I<sub>1</sub>. <math>a \neq 0</math>. We make <math>G = 0</math> by choice of <math>t</math>. Hence we may take <math>g = 0</math>.
Then <math>G = 0</math> requires <math>t = 0</math>, <math>E_1 = re_1</math>, <math>E_2 = e_2</math>. Then
<math>E_1^2 = r^2 a</math>, <math>E_2^2 = b</math>, <math>E_1 E_2 = rc + E_1</math>, <math>E_2 E_1 = -E_1</math>.
If <math>c \neq 0</math>, take <math>rc = 1</math>. Thus
(19) <math>e_1^2 = a</math>, <math>e_2^2 = b</math>, <math>e_1e_2 = c + e_1</math>, <math>e_2e_1 = -e_1</math> <math>(c = 0 \text{ or } 1)</math>
with no further normalization if <math>c = 1</math>. But if <math>c = 0</math>, we may remove any
square factor from <math>a</math>.
I<sub>2</sub>. <math>a = 0</math>. Then <math>G = rg</math>, <math>C = rc</math>, <math>A = r^2a</math>, <math>B = b + t(c + g)</math>. If <math>c + g \neq 0</math>,
we may take <math>b = 0</math> and a non-vanishing one of c and g equal to 1. If <math>c + g = 0</math>,
<math>c \neq 0</math>, we may take <math>c = 1</math>. If <math>c = g = 0</math>, we can remove a square factor from <math>a</math>.
No further normalization is possible.
For any e in algebra (19), (1, e) is a sub-algebra which is not invariant.
Every sub-algebra of order 2 lacking 1 has a basis in which the pairs of coeffi-
cients of <math>e_1</math> and <math>e_2</math> are not proportional and hence a basis <math>r + e_1</math>, <math>s + e_2</math>, with
<math>c = 2r</math>, <math>r(s - 1) = 0</math>, <math>r^2 = a</math>, <math>s^2 = b</math>.
Either <math>c = a = r = 0</math>, <math>b = s^2</math>, or <math>c = b = s = 1</math>, <math>r = 1/2</math>, <math>a = 1/4</math>. It is in-
variant by
<b>Lemma 4.</b> If S is a sub-algebra of order n of an algebra A of order <math>n+1</math>
and if A has a modulus 1, but 1 is not in S, then S is invariant in A.
For, <math>A = (1, S)</math>, <math>S^2 \leq S</math>. Hence <math>AS \leq S</math>, <math>SA \leq S</math>.
If <math>c = a = 0</math>, (19) has the single invariant sub-algebra <math>[e_1]</math> of order 1, other-
wise none.
A simple algebra is one having no proper invariant sub-algebra. <i>Hence</i> (19)
is simple unless <math>c = a = 0</math> or <math>c = b = 1</math>, <math>a = 1/4</math>. Algebra (19) is associa-
tive if and only if <math>a = c = 0</math>, <math>b = 1</math>.
Part II. Triple algebras of rank 3
8. Employ the new basis
1, <math>E_1 = a + be_1 + ce_2</math>, <math>E_2 = e + fe_1 + ge_2</math>, <math>D = bg - cf \neq 0</math>.
(20)
The commutative case shows the existence of a relation
<math>E_2E_1 - E_1E_2 = D(e_2e_1 - e_1e_2).</math>
(21)
We may choose <math>e_1</math> so that 1, <math>e_1</math>, <math>e_1^2</math> are linearly independent in <math>F</math>. Hence we
may take
<math>e_1^2 = e_2, \qquad e_1e_2 = h + je_1 + ke_2,</math>
(22)
<math>e_2^2 = m + ne_1 + pe_2, \qquad e_2e_1 = r + se_1 + te_2.</math>

## PDF page 8

120
L. E. DICKSON
For any new basis (20) we will have <math>E_1^2 = E_2</math> if
<math>e = a^2 + bc(h + r) + c^2m</math>
<math display="block">f = 2ab + bc(i + s) + c^2n,</math>
(23)
<math>q = 2ac + b^2 + bc(k + t) + c^2p</math>
Let <math>(22')</math> denote the multiplication table for <math>E_1</math>, <math>E_2</math>; it is of the form <math>(22)</math> with
each letter replaced by the corresponding capital letter. Using also (21), we get
(24) <math>R - H + (S - J)E_1 + (T - K)E_2 = D[r - h + (s - j)e_1 + (t - k)e_2].</math>
Solving (20), we get
<math>De_1 = ce - ag + gE_1 - cE_2,</math> <math>De_2 = af - be - fE_1 + bE_2.</math>
(25)
Elimination of <math>e_1</math> and <math>e_2</math> between (24) and (25) gives
<math>S-J=g(s-j)-f(t-k), \qquad T-K=-c(s-j)+b(t-k).</math>
(26)
We can always make <math>S = J</math>. Proof is needed only when <math>s \neq j</math>. By (26),
<math>S = J</math> if
<math display="block">u = (t - k)/(s - j).</math>
<math>q = fu</math>
By (23), this holds if <math>2a(c - bu)</math> equals a known quadratic form in b, c.
This
condition is satisfied by choice of a in terms of b and c if <math>c - bu \neq 0</math>.
Then
<math>D = -f(c - bu) \neq 0</math> if <math>f \neq 0</math>; we must therefore avoid the values for which
<math>f</math> and <math>g</math> in (23) are both zero.
Hence we may take <math>s = j</math>. This is not altered if we replace <math>e_1</math> by <math>e_1 - k/3</math>,
which yields <math>K = 0</math>. Hence we may take
<math>k=0.</math>
(27)
<math>s=j</math>
Apply transformation (20) subject to (23). By (24), <math>S = J</math> if <math>ft = 0</math>. There
are two cases.
9. Let <math>t \neq 0</math>. Then <math>f = 0</math>, <math>D = bg \neq 0</math>. By <math>(23_2)</math>,
<math display="block">-2a = 2cj + c^2n/b.</math>
(28)
Then
<math>S = J = e + gj + gcn/b,</math> <math>K = a + c(p - j) - c^2n/b.</math>
Eliminating a by (28), we see that <math>K = 0</math> only when
<math display="block">2p - 4j - 3cn/b = 0.</math>
<math>c = 0</math>
(29)
or
<sup>6</sup> But we can make <math>T = K</math> only when a certain invariant is not zero, C. C. MacDuffee,
Invariantive characterizations of linear algebras with the associative law not assumed, Trans.
Amer. Math. Soc., vol. 23 (1922), pp. 135-150, p. 147. In his equation below (27), the final
product should be <math>(b_2 - c_1 - d_1)(c_1 - d_1)(c_2 - d_2)^2 - b_1(c_2 - d_2)^3</math>, while <math>\alpha_1^3</math> should be <math>\alpha_2^3</math>.

## PDF page 9

121
LINEAR ALGEBRAS
Now
<math display="block">bT = ab + bc(p - j) + b^2t - c^2n</math>
reduces by (28) and (29) to
<math>T = bt</math>
(30)
By choice of b, we may take <math>T = 1</math>. To preserve this normalization <math>t = 1</math>,
we must take <math>b = 1</math>. Since
<math display="block">N = g^2 n/b,</math>
<math display="block">P-2J=-g(p-2j),</math>
(31)
no algebra of one of the following four types is equivalent to one of a differ-
ent type.
I or II. <math>n \neq 0</math>, <math>p = 2j</math>, or <math>n = 0</math>, <math>p \neq 2j</math>. Then <math>c = 0</math> by (29), whence
<math>\alpha = 0</math> by (28) and our transformation (20) is the identity.
III. <math>n \neq 0, p \neq 2j</math>. Then (29) and (28) uniquely determine <math>c \neq 0</math> and a,
whence our transformation yields a unique new algebra.
IV. <math>n = 0, p = 2j</math>. Our transformation involves a single parameter c which
is available for further normalization.
10. Let <math>t = 0</math>. Then <math>S = J</math>, <math>T = K</math> by (26) and (27). After divisions by <math>D</math>,
we find that
<math>K = 3a + (p + j)c,</math> <math>J = -3a^2 - 2ac(p + j) + b^2j + bc(n + h + r)</math>
<math>+ c^2(m - pj),</math>
<math display="block">P = 6a^2 + 4ac(p+j) + b^2p + bc(2h+2r-n) + c^2(p^2+2pj+2m).</math>
To preserve the normalization <math>k = 0</math>, take <math>K = 0</math> and eliminate <math>a</math>.
Then <math>J</math>
and <math>P</math> become quadratic forms in <math>b</math>, <math>c</math>, while
<math display="block">27N = 27nb^3 + 18w^2b^2c - 27wnbc^2 + (2w^3 + 27n^2)c^3,</math>
where <math>w = p - 2j</math>. The expressions for <math>H</math>, <math>M</math>, <math>R</math> are more complicated,
although <math>R - H = D(r - h)</math> by (24). If F is the field of all real numbers,
we may take <math>N = 0</math>. For a different <math>F</math>, normalization depends on representa-
tion by binary forms.
11. Let <math>A</math> be the algebra defined by (22) and (27). Any sub-algebra of
order 2 without the modulus 1 is <math>(u + e_1, v + e_2)</math>, where
<math>v = -u^2</math>, <math>h = u(v + j)</math>, <math>r - h = tv</math>, <math>m = nu + v^2 + pv</math>.
It is invariant in A by Lemma 4. Elimination of <math>u</math> and <math>v</math> yields two conditions
on the constants of <math>A</math>.
Let <math>W = x + ye_1 + ze_2</math> generate an invariant sub-algebra of order 1 of A.
We may take <math>y = 1</math> or <math>y = 0</math> and <math>z = 1</math>. In the latter case, elimination of
<math>x = -j</math> shows that the conditions on A are
<math display="block">h = n = 0, 	 m = -jt, 	 m = j(j - p).</math>

## PDF page 10

122
L. E. DICKSON
If <math>y = 1</math>, the conditions on A are <math>r = h</math>, <math>t = 0</math> and the results of eliminating
<math>x</math> and <math>z</math> between
<math>x = z^2h</math>, <math>z(x + zj) = 1</math>, <math>x(j + zn) = h + zm</math>, <math>z(j + zn) = x + zp</math>
If none of these special sets of conditions holds, A is simple.
Part III. Algebras of order 4 and left rank 3
12. Let <math>xx^2</math> be a linear combination of 1, <math>x</math>, <math>x^2</math> for every element <math>x</math>. Let 1,
<math>e</math>, <math>e^2</math> be linearly independent. By choice of <math>r</math> in the field <math>F</math>, <math>e_1 = e + r</math> satisfies
the first two equations in (33). Let <math>e_1e_3 = a_0 + \sum a_ie_i</math>. For
<math display="block">E = -a_1 - a_2 a_3 - a_2 e_1 + e_3,</math>
(32)
<math>e_1E</math> is linear in <math>E</math>. Take <math>E</math> as a new <math>e_3</math>. Hence
<math>e_1^2 = e_2,</math> <math>e_1e_2 = a + be_1,</math> <math>e_1e_3 = a_0 + a_3e_3,</math> <math>e_2e_1 = \sum b_ie_i,</math>
(33) <math>e_2^2 = \sum c_i e_i</math>, <math>e_2 e_3 = \sum d_i e_i</math>, <math>e_3 e_1 = \sum f_i e_i</math>,
<math display="block">e_3e_2 = \sum g_ie_i, \qquad e_3^2 = \sum h_ie_i,</math>
where <math>e_0 = 1</math>. Write
<math>X = se_1 + te_2 + we_3,</math> <math>X^2 = K + Le_1 + Me_2 + Pe_3,</math>
(34)
<math display="block">XX^2 = \operatorname{scalar} + Re_1 + Te_2 + Ve_3.</math>
The algebra will have left rank 3 if 1 and these three elements are linearly
dependent. This is true if and only if
<math display="block">\left|\begin{array}{ccc} s & L & \kappa \\ t & M & T \end{array}\right| = 0.</math>
(35)
| w P V |
Since M has the term <math>s^2</math>, while L and P are linear in s, the minors of V and R
are not zero identically. We here assume that the minor of T is zero, whence
<math>L \equiv sq, P \equiv wq</math>. Then (35) is the product of <math>M - tq \neq 0</math> by <math>sV - wR \equiv 0</math>.
By using the conditions which follow readily from <math>L \equiv sq</math>, <math>P \equiv wq</math>, and from
the terms free of t in <math>sV - wR</math>, we find that the latter is the product of q by a
determinant which is evidently zero. Hence the left rank is 3 for the algebra
<math>e_1^2 = e_2</math>, <math>e_1e_2 = a + be_1</math>, <math>e_2e_1 = b_0 + b_1e_1 + b_2e_2</math>, <math>e_2^2 = c_0 + c_2e_2</math>
(36) <math>e_2e_3 = d_0 + d_2e_2 + b_1e_3</math>, <math>e_1e_3 = a_0 + a_3e_3</math>, <math>e_3e_2 = g_0 + g_2e_2 + be_3</math>,
<math>e_3e_1 = f_0 + f_1e_1 + f_2e_2 - a_3e_3, \quad e_3^2 = h_0 + h_2e_2 + f_1e_3.</math>
Then <math>X^2</math>, <math>e_2X</math> and <math>Xe_2</math> are linear functions of 1, <math>e_2</math>, <math>X</math>. Hence if <math>Y</math> is any
element, 1, <math>e_2</math>, <math>Y</math> give a basis of a sub-algebra. Hence algebra (36) has left
rank 3 and right rank 3. For, from the linear function of 1, <math>e_2</math>, Y giving <math>Y^2Y</math>
(or <math>YY^2</math>) we may eliminate <math>e_2</math> by means of <math>Y^2 = g + he_2 + jY</math>, <math>h \neq 0</math>.

## PDF page 11

123
LINEAR ALGEBRAS
13. Conversely, for every element Y of an algebra A of order 4 over a field <math>F</math>,
let 1, <math>E</math>, <math>Y</math> give a basis of a sub-algebra, where <math>E</math> is fixed and is not a multiple
of 1. The right and left ranks of A are <math>\leq 3</math>. Exclude A's of rank 2. We
choose an element e not satisfying a quadratic equation in A. The case <math>Y = E</math>
shows that <math>E</math> satisfies a quadratic equation in <math>A</math>. Hence 1, <math>e</math>, <math>E</math> are linearly
independent in F. The case <math>Y = e</math> gives <math>e^2 = r + se + tE</math>, <math>t \neq 0</math>. Write
<math>e_1 = e - s/2,</math> <math>e_2 = e_1^2 = r + s^2/4 + tE.</math>
Then 1, <math>e_2</math>, Y give a basis of our sub-algebra. Take (32) as a new <math>e_3</math>.
We
find that 1, <math>e_2</math>, Y form an algebra for every Y in A if and only if A is identical
with algebra (36) with the second equation replaced by <math>e_1e_2 = a + be_1 + ce_2</math>.
14. Modify §12 by taking <math>L \equiv sQ</math>, <math>P \equiv st + wQ</math>. Then (35) holds (whence
the left rank is 3) if and only if algebra (33) becomes
<math>e_1^2 = e_2</math>, <math>e_1e_2 = a + be_1</math>, <math>e_1e_3 = a_0</math>, <math>e_2e_1 = b_0 + b_1e_1 + b_2e_2 + e_3</math>,
<math display="block">(37) 	 e_2^2 = c_0 + (b+b_1)e_2, 	 e_2e_3 = d_0 + b_1e_3, 	 e_3^2 = h_0 + f_1e_3,</math>
<math>e_3e_2 = g_0 + f_1e_2 + be_3</math>, <math>e_3e_1 = f_0 + f_1e_1 + f_2e_2</math>.
The right rank is 4, as shown by the right minimum equation for <math>e_1</math>. Note the
sub-algebra <math>(1, e_2, e_3)</math>.
Part IV. Division algebras
15. Let <math>J</math> be a root of a cyclic equation
<math>x^n - c_1 x^{n-1} + \cdots + (-1)^n c_n = 0</math>
i.e., an equation irreducible in a field <math>F</math> having the roots
<math>J, J' = \theta(J), J'' = \theta(J') = \theta^2(J), \dots, J^{(n-1)} = \theta^{n-1}(J), [\theta^n(J) = J],</math>
where superscripts on <math>\theta</math> denote iteratives (and not powers), while <math>\theta</math> is a poly-
nomial with coefficients in F. Write <math>B' = B(J)</math>, <math>B'' = B(J')</math>, etc. Define an
algebra with the elements <math>A + BI</math>, where A and B are polynomials in J with
coefficients in <math>F</math>, with the law of multiplication
(38) <math>(A + BI)(X + YI) = R + SI</math>, <math>R = AX + gBY'J</math>, <math>S = BX' + AY</math>,
where g is a number <math>\neq 0</math> of F. Both distributive laws hold.
Given <math>R</math>, <math>S</math> and <math>X</math>, <math>Y</math> not both zero, we can find <math>A</math>, <math>B</math> uniquely if
<math display="block">\left| \begin{array}{cc} X & gY'J \\ Y & X' \end{array} \right| \neq 0.</math>
(39)
This holds if <math>Y = 0</math>. Next, let <math>Y \neq 0</math>, <math>XX' = gYY'J</math>. This fails if <math>n = 2</math>

## PDF page 12

124
L. E. DICKSON
since J is not in F. If <math>n \geq 3</math>, we take the product of its conjugates, write
<math>N(X)</math> for the norm <math>XX' \cdots X^{(n-1)}</math> of X, and get
<math display="block">N^2(X) = g^n c_n N^2(Y),</math>
which fails if <math>g^n c_n</math> is not the square of the norm of a number of <math>F(J)</math>.
Given <math>R</math>, <math>S</math> and <math>A</math>, <math>B</math> not both zero, we seek <math>X</math>, <math>Y</math>. But
<math>C \equiv qBS'J - A'R = qBB'JX'' - AA'X</math>
(40)
If <math>n=2</math>, then <math>X''=X</math> and we obtain X uniquely and then Y. If <math>n\geq 3</math>,
let D denote the determinant of the coefficients of X, <math>X'</math>, <math>\cdots</math>, <math>X^{(n-1)}</math> in C, C',
<math>\cdots</math>, <math>C^{(n-1)}</math>.
If <math>n</math> is odd, we find that
<math display="block">D = -N^2(A) + g^n c_n N^2(B).</math>
(41)
But if n is even, <math>n \ge 4</math>, we find that <math>D = UU'</math>, where
<math>U = -N(A) + g^{n/2}N(B)JJ'' \cdots J^{(n-2)}.</math>
(42)
Transpose and multiply by the conjugate equation.
Theorem 3. Let <math>(-1)^n c_n</math> be the constant term of a cyclic equation of degree n
over a field F. The algebra in which multiplication is defined by (38) is a division
algebra if <math>n=2</math>, and when <math>n\geq 3</math> if <math>g^nc_n</math> is not the square of the norm of a num-
ber of the field <math>F(J)</math>.
For <math>n = 2</math>, the algebra over F has the basis 1, J, I, K, where
<math>J^2 = cJ - d</math>, <math>I^2 = gJ</math>, <math>JI = K</math>, <math>K^2 = dgJ</math>, <math>IK = gd</math>, <math>KJ = dI</math>,
(43)
<math>IJ = cI - K</math>, <math>JK = cK - dI</math>, <math>KI = gcJ - gd</math>.
This is a division algebra if <math>x^2 - cx + d = 0</math> is irreducible in F; it is remarkable
that there is no further condition.
A generalization of (38) is
<math display="block">R = AX + (aBY + bBY' + cB'Y + dB'Y')J,</math>
(44)
<math display="block">S = AY + mBX + nBX', \qquad m + n = 1.</math>
If <math>a = b = c = n = 0</math>, <math>d = m = 1</math>, we have the commutative algebra cited
in §1, which is a division algebra if <math>c_n</math> is not the square of the norm of a num-
ber of <math>F(J)</math>.
16. Algebras of order 2 without a modulus.
I. Let <math>e^2</math> be a scalar multiple of e for every element e. As in the proof of
Lemma 1,
<math>e_1^2 = ae_1,</math> <math>e_2^2 = be_2,</math> <math>e_1e_2 + e_2e_1 = be_1 + ae_2.</math>
Hence if <math>e = xe_1 + ye_2</math>, <math>e^2 = (ax + by)e</math>.

## PDF page 13

125
LINEAR ALGEBRAS
Let a and b be not both zero. By symmetry, take <math>a \neq 0</math>. Taking <math>e_1/a</math> as
a new <math>e_1</math>, we have <math>a = 1</math>. The idempotent elements
<math>e = (1 - by)e_1 + ye_2,</math> <math>E = (1 - bY)e_1 + Ye_2</math>
are independent if <math>Y \neq y</math>. Let <math>e_1e_2 = je_1 + ke_2</math>. The conditions for <math>eE = 0</math> are
<math>1 - bY + Yj - yj = 0,</math> <math>Yk + y - yk = 0.</math>
These have unique solutions <math>y</math>, <math>Y</math> with <math>Y \neq y</math> if <math>j + bk - b \neq 0</math>. Then
<math>e^2 = e,</math> <math>E^2 = E,</math> <math>eE = 0,</math> <math>Ee = e + E.</math>
(45)
II. In the contrary case, we have (20)-(26) after suppressing scalars and the
first equation (23). The condition for <math>S = J</math> is now a homogeneous quadratic
in b, c. Instead, we attempt to make <math>T = K</math>, given <math>t \neq k</math>; the condition is
<math>b = mc</math>, <math>m = (s - j)/(t - k)</math>. Then <math>D \neq 0</math> if <math>c \neq 0</math> and
<math>m^3 + m^2(k+t) + m(p-j-s) - n \neq 0</math>.
(46)
In this case we may therefore take <math>t = k</math>.
University of Chicago.
