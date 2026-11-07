Source: see manifest row of the PDF
PDF sha256: 897435f9d4e45c3a161f3d0657194d4c137d22468d2d771d48e5542219542d4e
License: public domain (J. H. M. Wedderburn, Trans. AMS 15 (1914); JSTOR Early Journal Content)
Language: eng
Fidelity: machine-gated

# Transcription of wedderburn_1914_primitive_algebra_TAMS_vol15.pdf

Transcription of `wedderburn_1914_primitive_algebra_TAMS_vol15.pdf` in this directory, 6 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 2-6 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories; pages 1 from the PDF's own text layer (pdftotext version 26.10.0, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Early	
  Journal	
  Content	
  on	
  JSTOR,	
  Free	
  to	
  Anyone	
  in	
  the	
  World	
  
This	
  article	
  is	
  one	
  of	
  nearly	
  500,000	
  scholarly	
  works	
  digitized	
  and	
  made	
  freely	
  available	
  to	
  everyone	
  in	
  
the	
  world	
  by	
  JSTOR.	
  	
  
Known	
  as	
  the	
  Early	
  Journal	
  Content,	
  this	
  set	
  of	
  works	
  include	
  research	
  articles,	
  news,	
  letters,	
  and	
  other	
  
writings	
  published	
  in	
  more	
  than	
  200	
  of	
  the	
  oldest	
  leading	
  academic	
  journals.	
  The	
  works	
  date	
  from	
  the	
  
mid-­‐seventeenth	
  to	
  the	
  early	
  twentieth	
  centuries.	
  	
  
	
  We	
  encourage	
  people	
  to	
  read	
  and	
  share	
  the	
  Early	
  Journal	
  Content	
  openly	
  and	
  to	
  tell	
  others	
  that	
  this	
  
resource	
  exists.	
  	
  People	
  may	
  post	
  this	
  content	
  online	
  or	
  redistribute	
  in	
  any	
  way	
  for	
  non-­‐commercial	
  
purposes.	
  
Read	
  more	
  about	
  Early	
  Journal	
  Content	
  at	
  http://about.jstor.org/participate-­‐jstor/individuals/early-­journal-­‐content.	
  	
  
	
  
	
  
	
  
	
  
	
  
	
  
	
  
	
  
JSTOR	
  is	
  a	
  digital	
  library	
  of	
  academic	
  journals,	
  books,	
  and	
  primary	
  source	
  objects.	
  JSTOR	
  helps	
  people	
  
discover,	
  use,	
  and	
  build	
  upon	
  a	
  wide	
  range	
  of	
  content	
  through	
  a	
  powerful	
  research	
  and	
  teaching	
  
platform,	
  and	
  preserves	
  this	
  content	
  for	
  future	
  generations.	
  JSTOR	
  is	
  part	
  of	
  ITHAKA,	
  a	
  not-­‐for-­‐profit	
  
organization	
  that	
  also	
  includes	
  Ithaka	
  S+R	
  and	
  Portico.	
  For	
  more	
  information	
  about	
  JSTOR,	
  please	
  
contact	
  support@jstor.org.

## PDF page 2

A TYPE OF PRIMITIVE ALGEBRA*
BY
J. H. M. WEDDERBURN
In a recent paper, † L. E. Dickson has discussed the linear associative
algebra, <math>A</math>, defined by the relations
<math>xy = y\theta(x), \quad y^n = g,</math>
where <math>\theta(x)</math> is a polynomial in x which is rational in the field F in which A is
defined. In this paper Dickson shows for <math>n=2</math> and <math>n=3</math> that, when <math>\theta</math>
and g are properly chosen, A is primitive, i. e., every element in it with the
exception of zero has an inverse: A is in fact in the case <math>n=2</math> a direct general-
ization of quaternions.
So far as I am aware no algebra other than these two and fields has been
proved to be primitive; hence it is of considerable interest to find that for any
value of <math>n</math>, <math>\theta</math> and <math>g</math> can be so chosen as to make Dickson's algebra primitive.
In discussing primitive algebras we may without any real loss of generality
assume that any element commutative with every other element of the algebra
is a scalar, i. e., an element of the field <math>F</math>. For, all such elements generate a
commutative subalgebra B and, as in the theory of groups, we can find a
complex <math>C</math> for which
<math>A = BC = CB</math>.
We can therefore regard <math>A</math> as an algebra whose coefficients lie in the field <math>F</math>
extended by the elements of the commutative primitive algebra <math>B</math> and, in this
algebra, scalars are the only elements commutative with every other element.
A primitive algebra will be called <i>normal</i> when reduced in this manner.
It follows from the general theory of linear associative algebras; that a
normal primitive algebra is of order <math>n^2</math> and that, when the field is sufficiently
extended, it is equivalent to the simple matric algebra <math>e_{pq}</math> (<math>p, q=1, 2, \dots, n</math>),
so that its identical equation is of degree <math>n</math>. We shall now investigate the
consequences that result from the assumption that the normal primitive
* Presented to the Society, December 31, 1913.
† These Transactions, vol. 15 (1914), pp. 31-46.
‡ See, for instance, my paper in the Proceedings of the London Mathe-
matical Society, ser. 2, vol. 6 (1907), pp. 77-118, where references are given.
162

## PDF page 3

163
1914]
A TYPE OF PRIMITIVE ALGEBRA
algebra A contains an element for which the group of the corresponding
identical equation is the cyclic group of order <math>n</math>.
1. Let A be a normal primitive algebra of order <math>n^2</math> and let x be an element
of it for which the group of the identical equation <math>f(x) = 0</math> is cyclic.
If <math>\xi_1, \xi_2, \dots, \xi_n</math> are the roots of x, the corresponding primitive idempotent
elements are
<math display="block">e_r \equiv e_{rr} = \frac{(x - \xi_1) \cdots (x - \xi_{r-1}) (x - \xi_{r+1}) \cdots (x - \xi_n)}{(\xi_r - \xi_1) \cdots (\xi_r - \xi_{r-1}) (\xi_r - \xi_{r+1}) \cdots (\xi_r - \xi_n)}</math>
<math>(r=1,2,\cdots,n)</math>
and* when F is extended by the roots of <math>x</math>, A contains a matric† algebra
<math>(e_{pq})</math> which does not reduce to <math>e_1, e_2, \dots, e_n</math>, since then x would be commuta-
tive with every element of A. We may therefore suppose <math>e_{12} \neq 0</math>, so that
there is an element <math>y_1</math>, rational in <math>F</math>, for which <math>e_1 y_1 e_2</math> is not zero. The con-
jugates of <math>e_1 y_1 e_2</math> in <math>F</math> are <math>e_r y_1 e_{r+1}</math> <math>(r = 1, 2, \dots, n)</math>, none of which can
therefore be zero.
If we set
<math>e_r y_1 e_{r+1} = \eta_r, r+1 e_r, r+1,</math>
the element
<math>y = \sum_{i=1}^{n} \eta_{r, r+1} e_{r, r+1}</math>
is rational since it is the sum of the conjugates of <math>e_1 y_1 e_2</math>; its nth power is evi-
dently the scalar <math>\eta_{12} \eta_{23} \cdots \eta_{n1} = g</math>, say, which is therefore rational.
Since
<math display="block">x=\sum_{r=1}^n \xi_r e_r,</math>
<math>xy = \sum_{r=1}^{n} \xi_r \eta_{r, r+1} e_{r, r+1} = yx_1,</math>
where
<math display="block">x_1 = \sum_{r=1}^n \xi_{r-1} e_r.</math>
The element <math>x_1</math> is commutative with x and is therefore a rational polynomial
in x, say <math>\theta(x)</math>, since the identical equation, <math>f(x) = 0</math>, has no repeated roots.
Evidently <math>x</math> and <math>y</math> generate <math>A</math> when expressed in its matric form and therefore
also in its rational form.
We have therefore the following
THEOREM. A normal primitive algebra which contains an element x whose
group is cyclic is generated by x and an element y which satisfies the relations
*See Proceedings of the London Mathematical Society, l. c., p. 97.
† A matric algebra is one for which a basis <math>(e_{pq})</math> can be chosen for which <math>e_{pq}e_{rs}=0</math>, <math>q\neq r</math>,
<math>e_{pq} e_{qr} = e_{pr}</math>, <math>\Sigma e_{rr} = 1</math>. Some of the elements <math>e_{pq}</math> may be zero, but if so the algebra is reducible.

## PDF page 4

164
[April
J. H. M. WEDDERSBURN
<math>xy = y \theta(x), \quad y^n = g,</math>
where <math>\theta(x)</math> and g are rational* in the field of the coefficients and <math>y^n</math> is the first
power of y which is commutative with <math>x</math>.
Conversely if <math>x</math> and <math>y</math> satisfy these conditions, the group of <math>x</math> is the cyclic
group of order <math>n</math>. This may be shown as follows.
Since
<math>xy = y \theta(x)</math>,
therefore
<math>xy^r = y^r \theta^r(x)</math>,
where <math>\theta^{r}(x)</math> denotes the function <math>\theta</math> iterated <math>r</math> times. If <math>\theta^{r}(x) = x</math>, then
<math>y^r</math> is commutative with <math>x</math>, which is contrary to the given conditions unless
<math>r = n</math>.
The matric form of <math>y</math> can be considerably simplified by choosing the units
<math>e_{pq}</math> in such a way that <math>\eta_{r, r+1} e_{r, r+1}</math> is replaced by <math>e_{r, r+1}</math> for <math>r=1, 2, \cdots, n-1</math>,
<math>e_{n1}</math> being chosen so that
<math>e_{12} e_{23} \cdots e_{n-1, n} e_{n1} = e_{11}</math>.
This change in the basis of <math>(e_{pq})</math> leaves <math>e_{rr}</math> <math>(e = 1, 2, \dots n)</math> unaltered so
that <math>x</math> has the same form as before while <math>y</math> becomes
<math>y = e_{12} + e_{23} + \cdots + e_{n-1, n} + ge_{n1}</math>.
It is easily shown from the forms given above for x and y that any element,
z, of A can be expressed uniquely in the form
<math>y^{n-1}h_0 + y^{n-2}h_1 + \cdots + yh_{n-2} + h_{n-1}</math>
where <math>h_r</math> <math>(r = 0, 1, \dots, n-1)</math> are rational polynomials in <math>x</math>.
Now
<math>y^r = e_{1, r+1} + e_{2, r+2} + \cdots + e_{n-r, n} + g (e_{n-r+1, 1} + \cdots + e_{nr})</math>
and
<math>y^r x^s = \xi_{r+1}^s e_{1,r+1} + \xi_{r+2}^s e_{1,r+2} + \cdots,</math>
so that in the matric form of any element of <math>A</math> all the coefficients to the left of
the principal diagonal are multiplied by <math>g</math>, and if any particular coefficient
is zero all the coefficients in the same diagonal are zero.
2. We shall now determine the conditions which g must satisfy in order that
an algebra of Dickson's type shall be primitive.
Let us consider an element of the form
<math>z = y^r + y^{r-1} h_1 + \cdots + y h_{r-1} + h_r</math>
<math>(h_r \neq 0)</math>
* We may evidently modify <math>y</math> so that <math>g</math> is an algebraic integer of the field.

## PDF page 5

165
19147
A TYPE OF PRIMITIVE ALGEBRA
and let <math>k_1</math>, <math>k_2</math>, <math>\cdots</math>, <math>k_{n-r}</math> be polynomials in <math>x</math> to be determined later, then
<math>(y^{n-r} + y^{n-r-1}k_1 + \cdots + k_{n-r})z = g + y^{n-1}k_1 + y^{n-2}k_2 + \cdots + y^{n-r}k_r</math>
<math>+y^{n-1}y^{-r}k_1y^r+y^{n-2}y^{-r+1}k_1y^{r-1}h_1+\cdots+y^{n-2}y^{-r}k_2y^r+\cdots+\cdots</math>
If we put <math>k_1 = -y^r h_1 y^{-r}</math>, which is a known rational polynomial in <math>x</math>,
the coefficient of <math>y^{n-1}</math> is zero. Similarly the coefficient of <math>y^{n-2}</math> vanishes if
<math>k_2 = -yk_1 y^{r-1} h_1 y^{-r} - y^r h_2 y^{-r}</math>
which is also a known polynomial in <math>x</math>, and so on till the coefficient of <math>y^r</math> is
reached, after which the process terminates. We can therefore in general
determine the k's so that the product commences with a term <math>y^{r-s} h(x)</math>
<math>(s < r)</math> and, after multiplying on the right by <math>1/h(x)</math>, which exists if <math>h \neq 0</math>,
we have a number which begins with the term <math>y^{r-s}</math>. If this number has an
inverse, z will also have one, since, by a well-known theorem on matrices, if a
product has an inverse, the same is true of each factor. We have therefore
only two types of elements to consider: first, those which may be reduced to
the form <math>y + \varphi(x)</math> by repeated applications of the process given above;
and second elements for which at some stage the product is independent of y.
If <math>y + \varphi(x)</math> is expressed in its matric form, its determinant is easily seen
to be
<math>\varphi(\xi_1)\varphi(\xi_2)\cdots\varphi(\xi_n)-q</math>
so that, if g is not the norm of any rational function of <math>\xi</math>, any element of this
type has an inverse.
Suppose now that <math>z</math> is an element of the second of the two types mentioned
above, so that there exists an element
<math>z_1 = y^{n-r} + y^{n-r-1} k_1 + \cdots + k_{n-r}</math>
such that <math>z_1 z</math> is independent of y. The determination of the coefficients
<math>k_1, \dots, k_{n-r}</math> is wholly independent of g, as the transform of any polynomial
in x by a power of y depends solely on <math>\theta(x)</math>. We may therefore set
<math display="block">z_1 z = g + k,</math>
where <math>k</math> is independent of <math>g</math>, which may be regarded as a variable scalar.
If k is not itself a scalar, <math>g + k</math> certainly has an inverse and therefore z has
also. We may assume therefore that <math>k</math> is a scalar, so that the matrix cor-
responding to <math>z_1</math> differs from the adjoint of the matrix corresponding to z
merely by a scalar factor which must be an integral function of <math>g</math> since <math>z_1</math>, <math>z</math>
and <math>g + k</math> are all integral in g. Since the determinant of the adjoint of a
matrix is a power of the determinant of that matrix, the determinant of <math>z</math>,

## PDF page 6

166
WEDDERBURN: A TYPE OF PRIMITIVE ALGEBRA
say <math>|z|</math>, must be a power of <math>g + k</math>, and as <math>|z|</math> is obviously of the rth degree
in <math>g</math>, beginning with the term <math>(-1)^{n-r} g^r</math>, we have
<math>|z| = (-1)^{n-r} (g+k)^r</math>.
But, when <math>g = 0</math>, <math>|z|</math> becomes the norm of <math>h_r</math> so that
<math>(-1)^{n-r} k^r = N(h_r).</math>
Unless the scalar <math>g + k</math> is zero, z has an inverse. In the contrary case,
<math>g^r = N(-h_r)</math>. Hence, if no power of g less than the nth is the norm of a
rational polynomial in x, every element of the algebra, except zero, has an inverse.*
*The existence of such rational numbers g follows from Satz 33 of Hilbert's Bericht,
Jahresbericht der Deutschen Mathematiker-Vereinigung, vol. 4 (1897),
p. 198.
