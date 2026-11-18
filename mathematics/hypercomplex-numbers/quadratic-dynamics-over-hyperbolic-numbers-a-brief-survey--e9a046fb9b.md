Source: see manifest row of the PDF
PDF sha256: e9a046fb9bb28122f9fa02f9993441dfd2a31e9413b872282c4c5c457f966757
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of quadratic-dynamics-over-hyperbolic-numbers-a-brief-survey--e9a046fb9b.pdf

Transcription of `quadratic-dynamics-over-hyperbolic-numbers-a-brief-survey--e9a046fb9b.pdf` in this directory, 7 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-7 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Surveys in Mathematics and its Applications
ISSN 1842-6298 (electronic), 1843-7265 (print)
Volume 17 (2022), 269 – 275

QUADRATIC DYNAMICS OVER HYPERBOLIC
NUMBERS: A BRIEF SURVEY
Sandra Hayes

Abstract. Hyperbolic numbers, also called split complex or perplex numbers in the literature,
are a variation of complex numbers established as a theory primarily by W. Clifford in the nineteenth
century who applied them to mechanics. Today hyperbolic numbers are considered to be the basic
mathematics of Einstein’s theory of special relativity. The goal of this paper is to present concise,
direct proofs of results contained in [1, 2, 4, 5, 6, 7] on the dynamics of hyperbolic numbers which
is quite different from the dynamics of complex numbers. The hyperbolic Mandelbrot set for
quadratic functions over hyperbolic numbers is simply a filled square, and the filled Julia set for
hyperbolic parameters inside the hyperbolic Mandelbrot set is a filled rectangle. For hyperbolic
parameters outside the hyperbolic Mandelbrot set, the filled Julia set has 3 possible topological
descriptions, if it is not empty, namely it is connected, totally disconnected, or disconnected but
not totally disconnected. This is in contrast to the complex case where it is always a non-empty
totally disconnected set.

1

Introduction

A hyperbolic number is a number z with two real components x and y written as
z = x+jy with a new imaginary unit j, referred to as the hyperbolic imaginary unit,
defined by the property that it is not equal to 1 or −1 but satisfies j 2 = 1. Whereas
the complex numbers form a field, the hyperbolic numbers are only an algebra,
because there are zero divisors, i.e. non-zero hyperbolic numbers which have no
multiplicative inverse. The zero divisors are all non-zero numbers z = x + jy with
x = ±y, i.e numbers on either diagonal. The zero divisors play a fundamental role
in explaining the dynamics of quadratic functions over hyperbolic numbers as well
as in explaining the applications of hyperbolic numbers to physics. Geometrically,
the zero divisors form the light cone.
Because of the zero divisors, the algebra H of all hyperbolic numbers is not a
2020 Mathematics Subject Classification: 37-02, 37C35
Keywords: Hyperbolic (Split Complex or Perplex) Numbers; quadratic dynamics; Mandelbrot
set; filled Julia sets

******************************************************************************
http://www.utgjiu.ro/math/sma

## PDF page 2

270

S. Hayes

normed space in the
√ way, i.e. by generalizing the Euclidean norm for complex
√ natural
numbers ||z|| = zz = x2 + y 2 , where z = x − iy is the complex conjugate of
the complex number z = x + iy. However,
the √
modulus of a hyperbolic number
√
2
2
z = x + jy, which is defined to be |x − y | = |zz ∗ |, where z ∗ = x − jy is the
hyperbolic conjugate of the hyperbolic number z, does play a role in special relativity,
since it is invariant under the Lorentz transformations of special relativity.
Quadratic dynamics over hyperbolic numbers refers to the dynamics of quadratic
functions fc (z) = z 2 +c with z and c hyperbolic, i.e. describing their Mandelbrot sets
and their filled Julia sets for parameters c inside and outside those Mandelbrot sets.
The boundary of the Mandelbrot set for quadratic functions over complex numbers
is a classical fractal. However, the Mandelbrot set for quadratic functions over
hyperbolic numbers is simply a filled square, The filled Julia set for all hyperbolic
parameters c inside the hyperbolic Mandelbrot set is a filled rectangle, but the
only filled Julia set for complex numbers whose boundary is a simple curve is when
the parameter c is the origin. For hyperbolic parameters c outside the hyperbolic
Mandelbrot set, the filled Julia set has 3 possible topological descriptions if it nonempty, in contrast to the complex case where the filled Julia set for parameters
outside the Mandelbrot set is topologically always a non-empty Cantor set.
These known results, whose proofs are straightforward using the technique of
characteristic coordinates, will be discussed here. In contrast to the importance of
hyperbolic numbers in physics, where they are viewed as basic to Einstein’s theory
of special relativity [9], the quadratic dynamics over hyperbolic numbers is not very
interesting. Some open questions for further investigations of the dynamics over
hyperbolic numbers will be mentioned.

2

The Hyperbolic Mandelbrot Set

The hyperbolic Mandelbrot set as well as the hyperbolic filled Julia set for quadratic
functions fc (z) = z 2 + c over hyperbolic numbers, i.e. z and c are hyperbolic, rely
on the notion of boundedness for a sequence (zn )n∈N of hyperbolic numbers zn .
Definition 1. (zn )n∈N is bounded if each of the real sequences (xn )n∈N and (yn )n∈N
is bounded where zn = xn + jyn .
This is one way of generalizing the notion of boundedness for a sequence (zn )n∈N
of complex numbers zn = xn + iyn to that for a sequence of hyperbolic numbers,
but is not the only way as will be mentioned later.
Recall that the complex Mandelbrot set M comprises all complex numbers c for
which the orbit (fcn (0))n∈N is bounded when fc (z) = z 2 + c with z complex. Analogously, the hyperbolic M andelbrot set, denoted by MH , is the set of all hyperbolic
numbers c such that the forward orbit of the origin (fcn (0))n∈N is bounded when
fc (z) = z 2 + c and z is hyperbolic.
******************************************************************************
Surveys in Mathematics and its Applications 17 (2022), 269 – 275
http://www.utgjiu.ro/math/sma

## PDF page 3

Quadratic dynamics over hyperbolic numbers

271

As already mentioned, the technique of characteristic coordinates is used to prove
that MH is a square. This is a tool using the existence of zero divisors and therefore
not available in studying complex numbers.
The characteristic coordinates for the hyperbolic number z = x + jy are the real
numbers X = x − y, Y = x + y. These are the coordinates for z with respect to the
idempotent basis {α, α∗ } of zero divisors with α = 21 (1 − j) and α∗ = 21 (1 + j) of
zero divisors. In this basis, z = (x − y)α + (x + y)α∗ = Xα + Y α∗ , and the quadratic
form zz ∗ = x2 − y 2 becomes simply XY .
Let fc (z) = z 2 + c with hyperbolic numbers z = x + jy and c = a + jb. Then
fc (z) = x2 + y 2 + a + j(2xy + b) and its characteristic coordinates are X 2 + c1 and
Y 2 + c2 , where c1 = a − b and c2 = a + b are the characteristic coordinates of c.
Consider the isomorphic linear transformation T of the vector space H given by
the matrix
(
)
1 −1
T =
1 1
which maps a point onto its characteristic coordinates i.e. T (z) = X +
) , when
( jY
x
of real
hyperbolic numbers z = x + jy are identified with ordered pairs z =
y
numbers. Then
T (fc (z)) = X 2 + c1 + j(Y 2 + c2 ) = fc1 (X) + j(fc2 (Y ))
for the real quadratic functions fc1 (X) = X 2 + c1 , fc2 (Y ) = Y 2 + c2 . By induction,
for all n
T (fcn (z)) = fcn1 (X) + j(fcn2 (Y )).
Therefore, orbits fcn (0) of the origin for quadratic functions of hyperbolic numbers c
are reverted back to orbits fcn1 (0) and fcn2 (0) of the origin for real quadratic functions
which have been extensively studied. Obviously, a hyperbolic sequence zn = xn +jyn
is bounded if and only if its image T (zn ) is bounded.
The hyperbolic Mandelbrot set is a square as was shown in [1, 2, 4, 5, 6]:
Theorem 2. For the quadratic hyperbolic function fc (z) = z 2 + c with c = a + jb,
let S = {(a, b) ∈ R2 : −2 ≤ a − b ≤ 14 , −2 ≤ a + b ≤ 14 }. Then
MH = S.
Proof. By definition, c ∈ MH if and only if the sequence of hyperbolic numbers
(fcn (0))n∈N is bounded, i.e. if and only if both of the real sequences (fcn1 (0))n∈N
and (fcn2 (0))n∈N are bounded when c1 = a − b, c2 = a + b are the characteristic
******************************************************************************
Surveys in Mathematics and its Applications 17 (2022), 269 – 275
http://www.utgjiu.ro/math/sma

## PDF page 4

272

S. Hayes

coordinates of c. That means that c1 and c2 are in the real part of the complex
Mandelbrot set:
1
M ∩ R = [−2, ].
4
Thus, c1 , c2 ∈ [−2, 14 ] which defines S.
Visually, in the ab-plane, one diagonal of the square S is [−2, 41 ] on the a-axis,
and S intersects the b-axis at ± 41 .
Another definition of boundedness was used in [2], namely a sequence (zn )n∈N
of hyperbolic numbers zn = xn + jyn is bounded if (|zn zn∗ |)n∈N = (|x2n − yn2 |)n∈N is
bounded. That implies that every sequence of zero divisors is bounded. In [2], the
hyperbolic Mandelbrot set is, therefore, larger, namely
MH = S ∪ D,
where D represents the two diagonals.

3

The Hyperbolic Filled Julia Sets

The complex filled Julia set K(fc ) for the complex quadratic function fc (z) = z 2 + c
is the set of all complex numbers z for which (fcn (z))n∈N is bounded. This set is
either connected or a Cantor set and thus totally disconnected, but it is never empty
since it contains all periodic points.
Similarly, the hyperbolic filled Julia set KH (fc ) for the hyperbolic quadratic function fc (z) = z 2 +c is the set of all hyperbolic numbers z = x+jy whose forward orbit
(fcn (z))n∈N is bounded or equivalently such that its image (T (fcn (z))n∈N is bounded,
i.e such that the sequences (fcn1 (X))n∈N and (fcn2 (Y ))n∈N of real quadratic functions
are bounded where X = x − y, Y = x + y are the characteristic coordinates of z
and c1 = a − b, c2 = a + b are the characteristic coordinates of c = a + jb. This set
can be connected, totally disconnected, disconnected but not totally disconnected
or empty. The following two lemmas are used in the proof.
If c is real, let
KR (fc ) = K(fc ) ∩ R
be the set of all real numbers x whose orbit (fcn (x))n∈N is bounded. The hyperbolic filled Julia set can be written in terms of these real filled Julia sets [2, 6]:
Lemma 3. Let c = a + jb with its characteristic coordinates c1 = a − b, c2 = a + b.
If fc (z) = z 2 + c is a hyperbolic quadratic function, let fc1 (X) = X 2 + c1 and
fc2 (Y ) = Y 2 + c2 be the corresponding real quadratic functions in the characteristic
coordinates X = x − y, Y = x + y for z = x + jy. Then
T (KH (fc )) = KR (fc1 ) + j(KR (fc2 )).
******************************************************************************
Surveys in Mathematics and its Applications 17 (2022), 269 – 275
http://www.utgjiu.ro/math/sma

## PDF page 5

Quadratic dynamics over hyperbolic numbers

273

Proof. z ∈ KH (fc ) if and only if the sequence (fcn (z))n∈N is bounded which is true if
and only if the real sequences (fcn1 (X))n∈N and (fcn2 (Y ))n∈N are bounded. It follows
that z ∈ KH (fc ) if and only if X ∈ KR (fc1 ) and Y ∈ KR (fc2 ).
To describe the hyperbolic filled Julia sets topologically, the following well known
facts [3] about the real filled Julia set of the real quadratic function fc (x) = x2 + c
for x, c ∈ R are used, namely it is empty or it is an interval or it is a Cantor set and
therefore a totally
√ disconnected subset of that interval.
1± 1−4c
Let p± =
denote the two fixed points of the complex function fc which
2
are real if and only if c ≤ 14 . If c = 14 there is just one fixed point at p± = 12 .
Lemma 4. Let fc (x) = x2 + c for x, c ∈ R.
If c < −2, then KR (fc ) is a Cantor set contained in [−p+ , p+ ].
If c ∈ [−2, 41 ], then KR (fc ) = [−p+ , p+ ].
If c > 14 , then KR (fc ) = ∅.
After Lemma 3, the hyperbolic filled Julia set is given by an ordered pair of two
real filled Julia sets, each of which can be connected or a Cantor set, and thus totally
disconnected, if it isn’t empty. Then there are only three ways of combining them
if neither is empty: both connected, both totally disconnected or one connected
and the other totally disconnected. The following topological description of the
hyperbolic filled Julia set was proved in [2, 4, 7]. Computer generated images are
given in [2].
Theorem 5. If fc (z) = z 2 + c with hyperbolic numbers z = x + jy, c = a + jb,
then KH (fc ) has one the following four possibilities depending on the characteristic
coordinates c1 = a − b, c2 = a + b of c:
(i) KH (fc ) is connected if c ∈ S, i.e. if c1 , c2 ∈ [−2, 41 ], namely it is a rectangle.
If c ∈
/ S:
(ii) KH (fc ) is a Cantor set, thus totally disconnected, if c1 , c2 < −2
(iii) KH (fc ) is disconnected but not totally disconnected if either c1 or c2 is in
[−2, 41 ] and the other is < −2
(iv) KH (fc ) is empty otherwise, i.e. if either c1 or c2 > 14
Proof. (i) Using Lemma 3 and Lemma 4, if c ∈ S, then KH (fc ) is an ordered pair of
the two intervals [−pk+ , pk+ ] where pk+ is the positive fixed point of the real quadratic
function x2 + ck , k = 1, 2 .
(ii) An ordered pair of two Cantor sets is a Cantor set.
******************************************************************************
Surveys in Mathematics and its Applications 17 (2022), 269 – 275
http://www.utgjiu.ro/math/sma

## PDF page 6

274

S. Hayes

(iii) An ordered pair of a connected set and a totally disconnected set is a disconnected set.
(iv) At least one of the real filled Julia sets KR (fck ) is empty for k = 1, 2, and thus
the pair.
Open questions
(1) What are the properties of other maps, which are important in complex analysis,
if they are considered as maps over hyperbolic numbers? One such map has
been treated in ∑
[8], namely the generalization of the complex Riemann zeta
1
function ζ(s) = ∞
n=1 ns , s a complex number, to hyperbolic numbers s ∈ H.
In [8] it is shown that every zero of the hyperbolic Riemann zeta function
is trivial, so there is no analogy to the Riemann hypothesis for hyperbolic
numbers.
(2) What maps over the hyperbolic numbers have interesting dynamics, if any?

References
[1] R. Artzy, Dynamics of quadratic functions in cycle planes, J. Geom., 44 (1992),
26-32. MR1169405. Zbl 0802.58034.
[2] V. Blankers, T.Rendfrey, A. Shukert and P.D. Shipman,Julia and Mandelbrot
Sets for Dynamics over the Hyperbolic Numbers, Fractal and Fractional 3,6
(2019) 1-9.
[3] R. Devaney, A First Course in Chaotic Dynamical Systems: Theory and Experiment, 2nd edition, CRC Press, 2020. MR1202237. Zbl 1435.37001
[4] P.E. Fishback, Quadratic dynamics in binary number systems, J. Difference Equ.
Appl 11, 7 (2005) 597-603. MR2173246. Zbl 1074.37028
[5] W. Metzler, The ”Mystery” of the quadratic Mandelbrot set, Amer.J. Phys 62,
9 (1994) 813-814. MR1295291. Zbl 1219.37036.
[6] D. Rochon, A generalized Mandelbrot set for bicomplex numbers, Fractals, 8,
(2000) 355-368. MR1810879. Zbl 0969.37021.
[7] D. Rochon, textitOn A Generalized Fatou-Julia Theorem, Fractals 11, 3, (2003)
213-219. MR2009645. Zbl 11041.37023.
[8] D. Rochon, 2004, A Bicomplex Riemann Zeta Function, Tokyo J. Math 27, 2
(2004) 357-369. MR2107508. Zbl 1075.30025.
******************************************************************************
Surveys in Mathematics and its Applications 17 (2022), 269 – 275
http://www.utgjiu.ro/math/sma

## PDF page 7

Quadratic dynamics over hyperbolic numbers

275

[9] F. Cantoni, D. Boccaletti, R. Cannata, V. Catoni, E. Nichelatti, P. Zampetti,
The Mathematics of Minkowski Space-Time. With an introduction to commutative hypercomplex numbers., Frontiers in Mathematics, Birkhaeuser Verlag, 2008.
MR2411620. Zbl 1151.53001.
Sandra Hayes
Department of Mathematics,
The Graduate Center of the City University of New York, USA.
email: shayes@gc.cuny.edu

License
This work is licensed under a Creative Commons Attribution 4.0 International License.

******************************************************************************
Surveys in Mathematics and its Applications 17 (2022), 269 – 275
http://www.utgjiu.ro/math/sma
