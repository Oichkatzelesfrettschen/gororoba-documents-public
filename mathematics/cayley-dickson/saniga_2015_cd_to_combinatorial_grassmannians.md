Source: https://doi.org/10.3390/math3041192
PDF sha256: 808f3e5edcd4341ac0904e7b313472cf030c7c0cbd7993ec473aedaa8e59cec5
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine (failed: characters)

# Transcription of saniga_2015_cd_to_combinatorial_grassmannians.pdf

Transcription of `saniga_2015_cd_to_combinatorial_grassmannians.pdf` in this directory, 30 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 21 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories; pages 1-20, 22-30 from the PDF's own text layer (pdftotext version 26.10.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Mathematics 2015, 3, 1192-1221; doi:10.3390/math3041192

OPEN ACCESS

mathematics
ISSN 2227-7390
www.mdpi.com/journal/mathematics
Article

From Cayley-Dickson Algebras to
Combinatorial Grassmannians
Metod Saniga 1, *, Frédéric Holweck 2 and Petr Pracna 3
1

Astronomical Institute, Slovak Academy of Sciences, Tatranská Lomnica 05960, Slovak Republic
IRTES/UTBM, Université de Bourgogne Franche-Comté, Belfort Cedex 90010, France;
E-Mail:frederic.holweck@utbm.fr
3
J. Heyrovský Institute of Physical Chemistry, v. v. i., Academy of Sciences of the Czech Republic,
Dolejškova 3, Prague 18223, Czech Republic; E-Mail: ppracna@seznam.cz
2

* Author to whom correspondence should be addressed; E-Mail: msaniga@astro.sk;
Tel.: +421-52-78791-28; Fax: +421-52-4467656.
Academic Editor: Carsten Schneider
Received: 23 August 2015 / Accepted: 30 November 2015 / Published: 4 December 2015

Abstract: Given a 2N -dimensional Cayley-Dickson algebra, where 3 ≤ N ≤ 6, we first
observe that the multiplication table of its imaginary units ea , 1 ≤ a ≤ 2N − 1, is encoded
in the properties of the projective space PG(N − 1, 2) if these imaginary units are regarded
as points and distinguished triads of them {ea , eb , ec }, 1 ≤ a < b < c ≤ 2N − 1 and
ea eb = ±ec , as lines. This projective space is seen to feature two distinct kinds of lines
according as a + b = c or a + b ̸= c. Consequently, it also exhibits (at least two)
different types of points in dependence on how many lines of either kind pass through
each of them. In order to account for such partition of the PG(N − 1, 2), the concept of
Veldkamp space of a finite point-line incidence structure is employed. The corresponding
point-line incidence structure is found to be a specific binomial configuration CN ; in
particular, C3 (octonions) is isomorphic to the Pasch (62 , 43 )-configuration, C4 (sedenions) is
the famous Desargues (103 )-configuration, C5 (32-nions) coincides with the Cayley-Salmon
(154 , 203 )-configuration found in the well-known Pascal mystic hexagram and C6 (64-nions)
is identical with a particular (215 , 353 )-configuration that can be viewed as four triangles in
perspective from a line where the points of perspectivity of six pairs of them form a Pasch
configuration. Finally, a brief examination of the structure of generic CN leads to a conjecture
that CN is isomorphic to a combinatorial Grassmannian of type G2 (N + 1).

## PDF page 2

Mathematics 2015, 3

1193

Keywords: Cayley-Dickson algebras; Veldkamp spaces; finite geometries

1. Introduction
As it is well known (see, for example, [1,2]), the Cayley-Dickson algebras represent a nested sequence
A0 , A1 , A2 , . . . , AN , . . . of 2N -dimensional (in general non-associative) R-algebras with AN ⊂ AN +1 ,
where A0 = R and where for any N ≥ 0 the set AN +1 comprises all ordered pairs of elements from AN
with conjugation defined by:
(x, y)∗ = (x∗ , −y)
(1)
and multiplication by:
(x, y)(X, Y ) = (xX − Y y ∗ , x∗ Y + Xy)

(2)

Every finite-dimensional algebra (see, for example, [2]) is defined by the multiplication rule of its basis.
The basis elements (or units) e0 , e1 , e2 , . . . , e2N +1 −1 of AN +1 , e0 being the real basis element (identity),
can be chosen in various ways. Our preference is the canonical basis:
e0 = (e0 , 0),

e1 = (e1 , 0),

e2 = (e2 , 0),

...,

e2N −1

= (e2N −1 , 0)

e2N = (0, e0 ),

e2N +1 = (0, e1 ),

e2N +2 = (0, e2 ),

...,

e2N +1 −1

= (0, e2N −1 )

where, by abuse of notation (see, for example, [3]), the same symbols are also used for the basis elements
of AN . This is because the paper essentially focuses on multiplication properties of basis elements and
the canonical basis seems to display most naturally the inherent symmetry of this operation. For, in
addition to revealing the nature of the Cayley-Dickson recursive process, it also implies that for both a
and b being non-zero we have ea eb = ±ea⊕b , where the symbol “⊕” denotes “exclusive or” of the binary
representations of a and b (see, for example, [4]). From the above expressions and Equations (1) and (2)
one can readily find the product of any two distinct units of AN +1 if the multiplication properties of
those of AN are given. Such products are usually expressed/presented in a tabular form, and we shall
also follow this tradition here. All the multiplication tables we made use of were computed for us by
Jörg Arndt; the computer program is named cayley-dickson-demo.cc and is freely available from his
web-site [5].
Employing such a multiplication table of AN , N ≥ 2, it can be verified that the 2N − 1 imaginaries
(N )
ea , 1 ≤ a ≤ 2N − 1, form 2 2−1 /3 distinguished sets each of which comprises three different units
{ea , eb , ec } that satisfy the equation:
ea eb = ±ec
(3)
and where each unit is found to belong to 2N −1 −1 such sets. (Although these properties will explicitly be
illustrated only for the cases 3 ≤ N ≤ 6, due to the nested structure of the algebras they must be exhibited
by any other higher-dimensional AN .). Regarding the imaginaries as points and their distinguished
triples as lines, one gets a point-line incidence geometry where every line has three points and through
each point there pass 2N −1 − 1 lines and which is isomorphic to PG(N − 1, 2), the (N − 1)-dimensional
projective space over the smallest Galois field GF (2) (see also [6] for N = 3 and [7] for N = 4). Let
us assume, without loss of generality, that the elements in any distinguished triple {ea , eb , ec } of AN are

## PDF page 3

Mathematics 2015, 3

1194

ordered in such a way that a < b < c. Then, for N ≥ 3, we can naturally speak about two different kinds
of triples and, hence, two distinct kinds of lines of the associated 2N -nionic PG(N − 1, 2), according as
a + b = c or a + b ̸= c; in what follows a line of the former kind will be called ordinary and that of the
latter kind defective. This stratification of the line-set of the PG(N − 1, 2) induces a similar partition of
the point-set of the latter space into several types, where a point of a given type is characterized by the
same number of lines of either kind that pass through it.
Obviously, if our projective space PG(N − 1, 2) is regarded as an abstract geometry per se, every
point and/or every line in it has the same footing. So, to account for the above-described “refinement”
of the structure of our 2N -nionic PG(N − 1, 2), it turns out to be necessary to find a representation of
this space where each point/line is ascribed a certain “internal” structure, which at first sight may seem
to be quite a challenging task. To tackle this task successfully, we need to introduce a few ideas from the
realm of finite geometry.
We start with a finite point-line incidence structure C = (P, L, I) where P and L are finite sets of
points and lines and where incidence I ⊆ P × L is a binary relation indicating which point-line pairs
are incident (see, for example, [8]). Here, we shall only be concerned with specific point-line incidence
structures called configurations [9]. A (vr , bk )-configuration is a C where: (1) v = |P| and b = |L|;
(2) every line has k points and every point is on r lines; and (3) two distinct lines intersect in at most one
point and every two distinct points are joined by at most one line; a configuration where v = b and r = k
is called symmetric (or balanced), and usually denoted as a (vr )-configuration. A (vr , bk )-configuration
)
)
(
(
is called a binomial configuration. Next, we define a geometric
and b = r+k−1
with v = r+k−1
k
r
hyperplane of C = (P, L, I), which is a proper subset of P such that a line from C either lies fully in
the subset, or shares with it only one point. If C possesses geometric hyperplanes, then one can define
the Veldkamp space of C, V(C), as follows [10]: (i) a point of V(C) is a geometric hyperplane of C and
(ii) a line of V(C) is the collection H ′ H ′′ of all geometric hyperplanes H of C such that H ′ ∩ H ′′ =
H ′ ∩H = H ′′ ∩H or H = H ′ , H ′′ , where H ′ and H ′′ are distinct geometric hyperplanes. If each line of C
has three points and C “behaves well”, a line of V(C) is also of size three and can equivalently be defined
as {H ′ , H ′′ , H ′ ∆H ′′ }, where the symbol ∆ stands for the symmetric difference of the two geometric
hyperplanes and an overbar denotes the complement of the object indicated. From its definition it is
obvious that V(C) is well suited for our needs because its points, being themselves sets of points, have
different “internal” structure and so, in general, they can no longer be on the same par; clearly, the
same applies to the lines V(C). Our task thus basically boils down to finding such CN whose V(CN ) is
isomorphic to PG(N − 1, 2) and completely reproduces its 2N -nionic fine structure. This will be carried
out in great detail for the first four non-trivial cases, 3 ≤ N ≤ 6, which, when combined with the two
trivial cases (N = 1, 2), will provide us with sufficient amount of information to guess a general pattern.
The paper is organized as follows. In Section 2 it is shown that C3 (octonions) is isomorphic
to the Pasch (62 , 43 )-configuration, which plays a key role in classifying Steiner triple systems.
In Section 3 one demonstrates that C4 (sedenions) is nothing but the famous Desargues
(103 )-configuration. In Section 4 our C5 (32-nions) is shown to be identical with the Cayley-Salmon
(154 , 203 )-configuration found in the well-known Pascal mystic hexagram. In Section 5 we find
that C6 corresponds to a particular (215 , 353 )-configuration encompassing seven distinct copies of the
Cayley-Salmon (154 , 203 )-configuration as geometric hyperplanes. In Section 6 some rudimentary

## PDF page 4

Mathematics 2015, 3

1195

((
)
(N +1) )
N +1
properties of the generic CN ∼
-configuration are outlined and its isomorphism
,
=
2
3
N −1
3
to a combinatorial Grassmannian of type G2 (N + 1) is conjectured. Finally, Section 7 is reserved for
concluding remarks.
2. Octonions and the Pasch (62 , 43 )-Configuration
From the nesting property of the Cayley-Dickson construction of AN it is obvious that the smallest
non-trivial case to be addressed is A3 , the algebra of octonions, whose multiplication table is presented
in Table 1.
Table 1. The multiplication table of the imaginary unit octonions ea , 1 ≤ a ≤ 7. For the
sake of simplicity, in what follows we shall employ a short-hand notation ea ≡ a; likewise
for the real unit e0 ≡ 0. There are also delineated multiplication tables corresponding to the
distinguished nested sequence of sub-algebras of complex numbers (a = 1, the upper left
corner) and quaternions (1 ≤ a ≤ 3, the upper left 3 × 3 square).
*

1

2

3

4

5

6

7

1
2
3
4
5
6
7

−0
+3
−2
+5
−4
−7
+6

−3
−0
+1
+6
+7
−4
−5

+2
−1
−0
+7
−6
+5
−4

−5
−6
−7
−0
+1
+2
+3

+4
−7
+6
−1
−0
−3
+2

+7
+4
−5
−2
+3
−0
−1

−6
+5
+4
−3
−2
+1
−0

The above-given multiplication table implies the existence of the following seven distinguished trios
of imaginary units:
{1, 2, 3}, {1, 4, 5}, {1, 6, 7},
{2, 4, 6}, {2, 5, 7},
{3, 4, 7}, {3, 5, 6}
Regarding the seven imaginary units as points and the seven distinguished triples of them as lines, we
obtain a point-line incidence structure where each line has three points and, dually, each point is on three
lines, and which is isomorphic to the smallest projective plane PG(2, 2), often called the Fano plane,
depicted in Figure 1.
It is then readily seen that we have six ordinary lines, namely:
{1, 2, 3}, {1, 4, 5}, {1, 6, 7},
{2, 4, 6}, {2, 5, 7},
{3, 4, 7}

## PDF page 5

Mathematics 2015, 3

1196

and only single defective one, that is:
{3, 5, 6}
Similarly, our octonionic PG(2, 2) features two distinct types of points. A type-one point is such that
two lines passing through it are ordinary, the remaining one being defective; such a point lies in the set:
{3, 5, 6} ≡ α
A type-two point is such that every line passing through it is ordinary; such a point belongs to the set:
{1, 2, 4, 7} ≡ β
which is highlighted by gray color in Figure 1.

e1

e2

e7
e4

e3

e5

e6

Figure 1. An illustration of the structure of PG(2, 2), the Fano plane, that provides the
multiplication law for octonions (see, e.g., [6]). The points of the plane are seven small
circles. The lines are represented by triples of circles located on the sides of the triangle, on
its altitudes, and by the triple lying on the big circle. The three imaginaries lying on the same
line satisfy Equation (3).
A configuration C3 whose Veldkamp space reproduces the above-described partitions of points and
lines of PG(2, 2) is, as we will soon see, nothing but the well-known Pasch (62 , 43 )-configuration, P.
This configuration, which plays a very important role in classifying Steiner triple systems (see, for
example, [11]), is depicted in Figure 2 in a form showing an automorphism of order three; it also lives in
the Fano plane and, as it is readily seen by comparing Figures 1 and 2, it can be obtained from the latter
by removal of any of its seven points and all the three lines passing through it.
In order to see that V(P) ∼
= PG(2, 2) we shall first show, using our diagrammatical representation
of P, all seven geometric hyperplanes of P—Figure 3. We see that they are indeed of two different
forms, of cardinality three and four. A member of the former set comprises two points at maximum
distance from each other. Such geometric hyperplane corresponds to a type-one (or α-) point of PG(2, 2).
A member of the latter set features three points on a common line; such a geometric hyperplane of P
corresponds to a type-two (or β-) point of our PG(2, 2). The seven lines of V(P) are illustrated in

## PDF page 6

Mathematics 2015, 3

1197

a compact diagrammatic form in Figure 4; as it is easily discernible, each of the six ordinary lines is of
the form {α, β, β}, whilst the remaining defective one has the {α, α, α} shape.

Figure 2. An illustrative portrayal of the Pasch configuration: circles stand for its points,
whereas its lines are represented by triples of points on common straight segments (three)
and the triple lying on a big circle.

3

5

6

7

4

2

1
Figure 3. The seven geometric hyperplanes of the Pasch configuration. The hyperplanes are
labelled by imaginary units of octonions in such a way that the seven lines of the Veldkamp
space of the Pasch configuration are identical with the seven distinguished triples of units,
that is with the seven lines of the PG(2, 2) shown in Figure 1.

## PDF page 7

Mathematics 2015, 3

1198

1

2

7

4

3

5

6

Figure 4. A unified view of the seven Veldkamp lines of the Pasch configuration. The reader
can readily verify that for any three geometric hyperplanes lying on a given line of the Fano
plane, one is the complement of the symmetric difference of the other two.
3. Sedenions and the Desargues (103 )-Configuration
Our next focus is on A4 , the sedenions, whose basic multiplication properties are summarized in
Table 2.
An inspection of this table yields as many as 35 distinguished triples, namely:
{1, 2, 3}, {1, 4, 5}, {1, 6, 7}, {1, 8, 9}, {1, 10, 11}, {1, 12, 13}, {1, 14, 15},
{2, 4, 6}, {2, 5, 7}, {2, 8, 10}, {2, 9, 11}, {2, 12, 14}, {2, 13, 15},
{3, 4, 7}, {3, 5, 6}, {3, 8, 11}, {3, 9, 10}, {3, 12, 15}, {3, 13, 14},
{4, 8, 12}, {4, 9, 13}, {4, 10, 14}, {4, 11, 15},
{5, 8, 13}, {5, 9, 12}, {5, 10, 15}, {5, 11, 14},
{6, 8, 14}, {6, 9, 15}, {6, 10, 12}, {6, 11, 13},
{7, 8, 15}, {7, 9, 14}, {7, 10, 13}, {7, 11, 12}
Regarding the 15 imaginary units as points and the 35 distinguished trios of them as lines, we obtain
a point-line incidence structure where each line has three points and each point is on seven lines, and
which is isomorphic to PG(3, 2), the smallest projective space—as depicted in Figure 5. The latter figure
employs a diagrammatical model of PG(3, 2) built, after Polster [12], around the pentagonal model of
the generalized quadrangle of type GQ(2, 2) whose 15 lines are illustrated by triples of points lying on
black line-segments (10 of them) and/or black arcs of circles (5). The remaining 20 lines of PG(3, 2)
comprise four distinct orbits: the yellow, red, blue and green one consisting, respectively, of the yellow
({1, 10, 11}), red ({1, 8, 9}), blue ({3, 13, 14}) and green ({3, 12, 15}) line and other four lines we get
from each by rotation through 72 degrees around the center of the pentagon.

## PDF page 8

Mathematics 2015, 3

1199

Table 2. The multiplication table of the imaginary unit sedenions ea , 1 ≤ a ≤ 15. As in the
previous section, we shall employ a short-hand notation ea ≡ a; likewise for the real unit
e0 ≡ 0. There are also shown multiplication tables corresponding to the distinguished nested
sequence of sub-algebras starting with complex numbers (a = 1), quaternions (1 ≤ a ≤ 3)
and octonions (1 ≤ a ≤ 7).
*

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

13

14

15

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
13
14
15

−0
+3
−2
+5
−4
−7
+6
+9
−8
−11
+10
−13
+12
+15
−14

−3
−0
+1
+6
+7
−4
−5
+10
+11
−8
−9
−14
−15
+12
+13

+2
−1
−0
+7
−6
+5
−4
+11
−10
+9
−8
−15
+14
−13
+12

−5
+4
−6
−7
−7
+6
−0
−1
+1
−0
+2
−3
+3
+2
+12 +13
+13 −12
+14 +15
+15 −14
−8
+9
−9
−8
−10 +11
−11 −10

+7
+4
−5
−2
+3
−0
−1
+14
−15
−12
+13
+10
−11
−8
+9

−6
+5
+4
−3
−2
+1
−0
+15
+14
−13
−12
+11
+10
−9
−8

−9
−10
−11
−12
−13
−14
−15
−0
+1
+2
+3
+4
+5
+6
+7

+8
−11
+10
−13
+12
+15
−14
−1
−0
−3
+2
−5
+4
+7
−6

+11
+8
−9
−14
−15
+12
+13
−2
+3
−0
−1
−6
−7
+4
+5

−10
+9
+8
−15
+14
−13
+12
−3
−2
+1
−0
−7
+6
−5
+4

+13 −12
+14 +15
+15 −14
+8
+9
−9
+8
−10 +11
−11 −10
−4 −5
+5
−4
+6
+7
+7
−6
−0
+1
−1 −0
−2
+3
−3 −2

−15
−12
+13
+10
−11
+8
+9
−6
−7
−4
+5
+2
−3
−0
+1

+14
−13
−12
+11
+10
−9
+8
−7
+6
−5
−4
+3
+2
−1
−0

e1
e14

e13
e11

e12

e10

e5

e7

e8

e15
15

e9

e3
e4

e2

e6

Figure 5. An illustration of the structure of PG(3, 2) that provides the multiplication law for
sedenions. As in the previous case, the three imaginaries lying on the same line are such that
the product of two of them yields the third one, sign disregarded.

## PDF page 9

Mathematics 2015, 3

1200

It is not difficult to verify that we have 25 ordinary lines, namely:
{1, 2, 3}, {1, 4, 5}, {1, 6, 7}, {1, 8, 9}, {1, 10, 11}, {1, 12, 13}, {1, 14, 15},
{2, 4, 6}, {2, 5, 7}, {2, 8, 10}, {2, 9, 11}, {2, 12, 14}, {2, 13, 15},
{3, 4, 7}, {4, 8, 12}, {4, 9, 13}, {4, 10, 14}, {4, 11, 15},
{3, 8, 11}, {5, 8, 13}, {6, 8, 14}, {7, 8, 15},
{3, 12, 15}, {5, 10, 15}, {6, 9, 15}
and 10 defective ones, namely:
{3, 5, 6}, {3, 9, 10}, {3, 13, 14},
{5, 9, 12}, {5, 11, 14},
{6, 10, 12}, {6, 11, 13},
{7, 9, 14}, {7, 10, 13}, {7, 11, 12}
Similarly, our sedenionic PG(3, 2) features two distinct types of points. A type-one point is such
that four lines passing through it are ordinary, the remaining three being defective; such a point lies
in the set :
{3, 5, 6, 7, 9, 10, 11, 12, 13, 14} ≡ α
A type-two point is such that every line passing through it is ordinary; such a point belongs to the set:
{1, 2, 4, 8, 15} ≡ β
being illustrated by gray shading in Figure 5. We see that all defective lines are of the same form,
namely {α, α, α}. The 25 ordinary lines split into two distinct families. Ten of them are of the form
{α, β, β}, namely:
{1, 2, 3}, {1, 4, 5}, {1, 8, 9}, {1, 14, 15},
{2, 4, 6}, {2, 8, 10}, {2, 13, 15},
{4, 8, 12}, {4, 11, 15},
{7, 8, 15}
and the remaining 15 are of the form {α, α, β}, namely:
{1, 6, 7}, {1, 10, 11}, {1, 12, 13},
{2, 5, 7}, {2, 9, 11}, {2, 12, 14},
{3, 4, 7}, {4, 9, 13}, {4, 10, 14},
{3, 8, 11}, {5, 8, 13}, {6, 8, 14},
{3, 12, 15}, {5, 10, 15}, {6, 9, 15}
A configuration C4 whose Veldkamp space reproduces the above-described partitions of points and
lines of PG(3, 2) is, as demonstrated below, the famous Desargues (103 )-configuration, D, which is one

## PDF page 10

Mathematics 2015, 3

1201

of the most prominent point-line incidence structures (see, for example, [13]). Up to isomorphism, there
exist altogether 10 (103 )-configurations. The Desargues configuration is, unlike the others, flag-transitive
and the only one where for each of its points the three points that are not collinear with it lie on a line.
This configuration, depicted in Figure 6 in a form showing its automorphism of order three, also lives
in our sedenionic PG(3, 2); here, its points are the 10 α-points and its lines are all the defective lines.
In order to see that V(D) ∼
= PG(3, 2) we shall first introduce, using our diagrammatical representation
of D, all 15 geometric hyperplanes of D—Figure 7. We see that they are indeed of two different forms,
and of required cardinality ten and five. A member of the former set comprises a point and three points
not collinear with it. Such geometric hyperplane corresponds to a type-one (or α-) point of PG(3, 2).
A member of the latter set features six points located on four lines, with two lines per each point; this is
nothing but the Pasch configuration we introduced in the previous section. Such a geometric hyperplane
of D corresponds to a type-two (or β-) point of our PG(3, 2). It is also a straightforward task to verify
that V(D) is endowed with 35 lines splitting into the required three families; those that correspond to
defective lines of our sedenionic PG(3, 2) are shown in Figure 8, while those that correspond to ordinary
lines are depicted in Figure 9 (of type {α, β, β}) and Figure 10 (of type {α, α, β}). Figure 11 offers a
“condensed” view of the isomorphism V(D) ∼
= PG(3, 2).

Figure 6. An illustrative portrayal of the Desargues configuration, built around the model
of the Pasch configuration shown in Figure 2: circles stand for its points, whereas its lines
are represented by triples of points on common straight segments (six), arcs of circles (three)
and a big circle.
We shall finalize this section by pointing out that the existence of two different kinds of geometric
hyperplanes of the Desargues configuration is closely connected with two well-known views of this
configuration. The first one is as a pair of triangles that are in perspective from both a point and
a line (Desargues’ theorem), the point and the line forming a geometric hyperplane. The other
view is as the incidence sum of a complete quadrangle (i.e., a (43 , 62 )-configuration) and a Pasch
(62 , 43 )-configuration [18].

## PDF page 11

Mathematics 2015, 3

1202

14

13

11

9

10

12

6

5

3

1

2

4

8

7

15

Figure 7. The 15 geometric hyperplanes of the Desargues configuration. The hyperplanes
are labelled by imaginary units of sedenions in such a way that—as we shall verify in the
next three figures—the 35 lines of the Veldkamp space of the Desargues configuration are
identical with the 35 distinguished triples of units, that is with the 35 lines of the PG(3, 2)
shown in Figure 5.

## PDF page 12

Mathematics 2015, 3

1203

7-9-14

7-10-13

7-11-12

3-13-14

5-11-14

6-11-13

3-9-10

5-9-12

6-10-12

3-5-6

Figure 8.
The 10 Veldkamp lines of the Desargues configuration that represent
the 10 defective lines of the sedenionic PG(3, 2). Here, as well as in the next two figures, the
three geometric hyperplanes comprising a given Veldkamp line are distinguished by different
colors, with their common elements (here just a single point) being colored black. For each
Veldkamp line we also explicitly indicate its composition.

## PDF page 13

Mathematics 2015, 3

1204

2-4-6

1-4-5

1-2-3

4-8-12

2-8-10

1-8-9

4-11-15

2-13-15

1-14-15

7-8-15

Figure 9.
The 10 Veldkamp lines of the Desargues configuration that represent
the 10 ordinary lines of the sedenionic PG(3, 2) of type {α, β, β}.

## PDF page 14

Mathematics 2015, 3

1205

6-9-15

5-10-15

3-12-15

6-8-14

5-8-13

3-8-11

1-6-7

2-5-7

3-4-7

2-12-14

4-9-13

1-10-11

2-9-11

1-12-13

4-10-14

Figure 10. The 15 Veldkamp lines of the Desargues configuration that represent the 15
ordinary lines of the sedenionic PG(3, 2) of type {α, α, β}.

## PDF page 15

Mathematics 2015, 3

1206

1

13

14

12

11

15

10

7

5

8

9
3

4

2

6

Figure 11. A compact graphical view of illustrating the bijection between 15 imaginary unit
sedenions and 15 geometric hyperplanes of the Desargues configuration, as well as between
35 distinguished triples of units and 35 Veldkamp lines of the Desargues configuration.
4. 32-Nions and the Cayley-Salmon (154 , 203 )-Configuration
Our next case is A5 , or the 32-nions, whose multiplication properties are encoded in Table 3.
From this table we infer the existence of 155 distinguished triples of imaginary units. Regarding
the 31 imaginary units of A5 as points and the 155 distinguished triples of them as lines, we obtain a
point-line incidence structure where each line has three points and each point is on 15 lines, and which is
isomorphic to PG(4, 2). We next find that 65 lines of this space are defective and 90 ordinary. However,
unlike the preceding two cases, there are three different types of points in our 32-nionic PG(4, 2):
10 α-points,
α ≡ {7, 11, 13, 14, 19, 21, 22, 25, 26, 28},
each of which is on nine defective and six ordinary lines; 15 β-points,
β ≡ {3, 5, 6, 9, 10, 12, 15, 17, 18, 20, 23, 24, 27, 29, 30},
each of which is on seven defective and eight ordinary lines; and six γ-points,
γ ≡ {1, 2, 4, 8, 16, 31},

## PDF page 16

Mathematics 2015, 3

1207

each of them being on 15 ordinary (and, hence, on zero defective) lines. This stratification of the point-set
of PG(4, 2) leads, in turn, to two different kinds of defective lines and three distinct kinds of ordinary
lines. Concerning the former, there are 45 of them of type {α, α, β}, namely:
{3, 13, 14}, {3, 21, 22}, {3, 25, 26},
{5, 11, 14}, {5, 19, 22}, {5, 25, 28},
{6, 11, 13}, {6, 19, 21}, {6, 26, 28},
{7, 9, 14}, {7, 10, 13}, {7, 11, 12}, {7, 17, 22}, {7, 18, 21}, {7, 19, 20},
{7, 25, 30}, {7, 26, 29}, {7, 27, 28},
{9, 19, 26}, {9, 21, 28},
{10, 19, 25}, {10, 22, 28},
{11, 17, 26}, {11, 18, 25}, {11, 19, 24}, {11, 21, 30}, {11, 22, 29}, {11, 23, 28},
{12, 21, 25}, {12, 22, 26},
{13, 17, 28}, {13, 19, 30}, {13, 20, 25}, {13, 21, 24}, {13, 22, 27}, {13, 23, 26},
{14, 18, 28}, {14, 19, 29}, {14, 20, 26}, {14, 21, 27}, {14, 22, 24}, {14, 23, 25},
{15, 19, 28}, {15, 21, 26}, {15, 22, 25}
and 20 of type {β, β, β}, namely:
{3, 5, 6}, {3, 9, 10}, {3, 17, 18}, {3, 29, 30},
{5, 9, 12}, {5, 17, 20}, {5, 27, 30},
{6, 10, 12}, {6, 18, 20}, {6, 27, 29},
{9, 17, 24}, {9, 23, 30},
{10, 18, 24}, {10, 23, 29},
{12, 20, 24}, {12, 23, 27},
{15, 17, 30}, {15, 18, 29}, {15, 20, 27}, {15, 23, 24}
As per the latter, one finds 15 of them of type {β, β, β}, namely:
{3, 12, 15}, {3, 20, 23}, {3, 24, 27},
{5, 10, 15}, {5, 18, 23}, {5, 24, 29},
{6, 9, 15}, {6, 17, 23}, {6, 24, 30},
{9, 18, 27}, {9, 20, 29},
{10, 17, 27}, {10, 20, 30},
{12, 17, 29}, {12, 18, 30}

## PDF page 17

Mathematics 2015, 3

1208

60 of type {α, β, γ}, namely:
{1, 6, 7}, {1, 10, 11}, {1, 12, 13}, {1, 14, 15}, {1, 18, 19}, {1, 20, 21},
{1, 22, 23}, {1, 24, 25}, {1, 26, 27}, {1, 28, 29},
{2, 5, 7}, {2, 9, 11}, {2, 12, 14}, {2, 13, 15}, {2, 17, 19}, {2, 20, 22},
{2, 21, 23}, {2, 24, 26}, {2, 25, 27}, {2, 28, 30},
{3, 4, 7}, {3, 8, 11}, {3, 16, 19}, {3, 28, 31},
{4, 9, 13}, {4, 10, 14}, {4, 11, 15}, {4, 17, 21}, {4, 18, 22},
{4, 19, 23}, {4, 24, 28}, {4, 25, 29}, {4, 26, 30},
{5, 8, 13}, {5, 16, 21}, {5, 26, 31},
{6, 8, 14}, {6, 16, 22}, {6, 25, 31},
{7, 8, 15}, {7, 16, 23}, {7, 24, 31},
{8, 17, 25}, {8, 18, 26}, {8, 19, 27}, {8, 20, 28}, {8, 21, 29}, {8, 22, 30},
{9, 16, 25}, {9, 22, 31},
{10, 16, 26}, {10, 21, 31},
{11, 16, 27}, {11, 20, 31},
{12, 16, 28}, {12, 19, 31},
{13, 16, 29}, {13, 18, 31},
{14, 16, 30}, {14, 17, 31}
and, finally, 15 of type {β, γ, γ}, namely:
{1, 2, 3}, {1, 4, 5}, {1, 8, 9}, {1, 16, 17}, {1, 30, 31},
{2, 4, 6}, {2, 8, 10}, {2, 16, 18}, {2, 29, 31},
{4, 8, 12}, {4, 16, 20}, {4, 27, 31},
{8, 16, 24}, {8, 23, 31},
{5, 16, 31}

## PDF page 18

Mathematics 2015, 3

1209

Table 3. The multiplication table—for better readability split into two parts—of the
imaginary unit 32-nions ea , 1 ≤ a ≤ 31, in short-hand notation ea ≡ a (and e0 ≡ 0).
*

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

13

14

15

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
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31

−0
+3
−2
+5
−4
−7
+6
+9
−8
−11
+10
−13
+12
+15
−14
+17
−16
−19
+18
−21
+20
+23
−22
−25
+24
+27
−26
+29
−28
−31
+30

−3
−0
+1
+6
+7
−4
−5
+10
+11
−8
−9
−14
−15
+12
+13
+18
+19
−16
−17
−22
−23
+20
+21
−26
−27
+24
+25
+30
+31
−28
−29

+2
−1
−0
+7
−6
+5
−4
+11
−10
+9
−8
−15
+14
−13
+12
+19
−18
+17
−16
−23
+22
−21
+20
−27
+26
−25
+24
+31
−30
+29
−28

−5
−6
−7
−0
+1
+2
+3
+12
+13
+14
+15
−8
−9
−10
−11
+20
+21
+22
+23
−16
−17
−18
−19
−28
−29
−30
−31
+24
+25
+26
+27

+4
−7
+6
−1
−0
−3
+2
+13
−12
+15
−14
+9
−8
+11
−10
+21
−20
+23
−22
+17
−16
+19
−18
−29
+28
−31
+30
−25
+24
−27
+26

+7
+4
−5
−2
+3
−0
−1
+14
−15
−12
+13
+10
−11
−8
+9
+22
−23
−20
+21
+18
−19
−16
+17
−30
+31
+28
−29
−26
+27
+24
−25

−6
+5
+4
−3
−2
+1
−0
+15
+14
−13
−12
+11
+10
−9
−8
+23
+22
−21
−20
+19
+18
−17
−16
−31
−30
+29
+28
−27
−26
+25
+24

−9
−10
−11
−12
−13
−14
−15
−0
+1
+2
+3
+4
+5
+6
+7
+24
+25
+26
+27
+28
+29
+30
+31
−16
−17
−18
−19
−20
−21
−22
−23

+8
−11
+10
−13
+12
+15
−14
−1
−0
−3
+2
−5
+4
+7
−6
+25
−24
+27
−26
+29
−28
−31
+30
+17
−16
+19
−18
+21
−20
−23
+22

+11
+8
−9
−14
−15
+12
+13
−2
+3
−0
−1
−6
−7
+4
+5
+26
−27
−24
+25
+30
+31
−28
−29
+18
−19
−16
+17
+22
+23
−20
−21

−10
+9
+8
−15
+14
−13
+12
−3
−2
+1
−0
−7
+6
−5
+4
+27
+26
−25
−24
+31
−30
+29
−28
+19
+18
−17
−16
+23
−22
+21
−20

+13
+14
+15
+8
−9
−10
−11
−4
+5
+6
+7
−0
−1
−2
−3
+28
−29
−30
−31
−24
+25
+26
+27
+20
−21
−22
−23
−16
+17
+18
+19

−12
+15
−14
+9
+8
+11
−10
−5
−4
+7
−6
+1
−0
+3
−2
+29
+28
−31
+30
−25
−24
−27
+26
+21
+20
−23
+22
−17
−16
−19
+18

−15
−12
+13
+10
−11
+8
+9
−6
−7
−4
+5
+2
−3
−0
+1
+30
+31
+28
−29
−26
+27
−24
−25
+22
+23
+20
−21
−18
+19
−16
−17

+14
−13
−12
+11
+10
−9
+8
−7
+6
−5
−4
+3
+2
−1
−0
+31
−30
+29
+28
−27
−26
+25
−24
+23
−22
+21
+20
−19
−18
+17
−16

## PDF page 19

Mathematics 2015, 3

1210
Table 3. Cont.

*

16

17

18

19

20

21

22

23

24

25

26

27

28

29

30

31

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
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31

−17
−18
−19
−20
−21
−22
−23
−24
−25
−26
−27
−28
−29
−30
−31
−0
+1
+2
+3
+4
+5
+6
+7
+8
+9
+10
+11
+12
+13
+14
+15

+16
−19
+18
−21
+20
+23
−22
−25
+24
+27
−26
+29
−28
−31
+30
−1
−0
−3
+2
−5
+4
+7
−6
−9
+8
+11
−10
+13
−12
−15
+14

+19
+16
−17
−22
−23
+20
+21
−26
−27
+24
+25
+30
+31
−28
−29
−2
+3
−0
−1
−6
−7
+4
+5
−10
−11
+8
+9
+14
+15
−12
−13

−18
+17
+16
−23
+22
−21
+20
−27
+26
−25
+24
+31
−30
+29
−28
−3
−2
+1
−0
−7
+6
−5
+4
−11
+10
−9
+8
+15
−14
+13
−12

+21
+22
+23
+16
−17
−18
−19
−28
−29
−30
−31
+24
+25
+26
+27
−4
+5
+6
+7
−0
−1
−2
−3
−12
−13
−14
−15
+8
+9
+10
+11

−20
+23
−22
+17
+16
+19
−18
−29
+28
−31
+30
−25
+24
−27
+26
−5
−4
+7
−6
+1
−0
+3
−2
−13
+12
−15
+14
−9
+8
−11
+10

−23
−20
+21
+18
−19
+16
+17
−30
+31
+28
−29
−26
+27
+24
−25
−6
−7
−4
+5
+2
−3
−0
+1
−14
+15
+12
−13
−10
+11
+8
−9

+22
−21
−20
+19
+18
−17
+16
−31
−30
+29
+28
−27
−26
+25
+24
−7
+6
−5
−4
+3
+2
−1
−0
−15
−14
+13
+12
−11
−10
+9
+8

+25
+26
+27
+28
+29
+30
+31
+16
−17
−18
−19
−20
−21
−22
−23
−8
+9
+10
+11
+12
+13
+14
+15
−0
−1
−2
−3
−4
−5
−6
−7

−24
+27
−26
+29
−28
−31
+30
+17
+16
+19
−18
+21
−20
−23
+22
−9
−8
+11
−10
+13
−12
−15
+14
+1
−0
+3
−2
+5
−4
−7
+6

−27
−24
+25
+30
+31
−28
−29
+18
−19
+16
+17
+22
+23
−20
−21
−10
−11
−8
+9
+14
+15
−12
−13
+2
−3
−0
+1
+6
+7
−4
−5

+26
−25
−24
+31
−30
+29
−28
+19
+18
−17
+16
+23
−22
+21
−20
−11
+10
−9
−8
+15
−14
+13
−12
+3
+2
−1
−0
+7
−6
+5
−4

−29
−30
−31
−24
+25
+26
+27
+20
−21
−22
−23
+16
+17
+18
+19
−12
−13
−14
−15
−8
+9
+10
+11
+4
−5
−6
−7
−0
+1
+2
+3

+28
−31
+30
−25
−24
−27
+26
+21
+20
−23
+22
−17
+16
−19
+18
−13
+12
−15
+14
−9
−8
−11
+10
+5
+4
−7
+6
−1
−0
−3
+2

+31
+28
−29
−26
+27
−24
−25
+22
+23
+20
−21
−18
+19
+16
−17
−14
+15
+12
−13
−10
+11
−8
−9
+6
+7
+4
−5
−2
+3
−0
−1

−30
+29
+28
−27
−26
+25
−24
+23
− 22
+21
+20
−19
−18
+17
+16
−15
−14
+13
+12
−11
−10
+9
−8
+7
−6
+5
+4
−3
−2
+1
−0

A point-line configuration C5 whose Veldkamp space accounts for these stratifications of both
the point- and line-set of our 32-nionic PG(4, 2) is of type (154 , 203 ). (It is worth mentioning
here that there exists another remarkable configuration whose Veldkamp space does the same job
for us, namely the generalized quadrangle of order two, also known as the Cremona-Richmond
(153 )-configuration (see, for example, [14]). However, this configuration is triangle-free and so it
cannot contain the Desargues configuration as dictated by the nesting property of the Cayley-Dickson
algebras.) This configuration is formed within our PG(4, 2) by 15 β-points and 20 defective
lines of {β, β, β} type and its structure is sketched in Figure 12. It is a rather easy task
to verify that this particular (154 , 203 )-configuration possesses 31 distinct geometric hyperplanes
that fall into three different types. A type-one hyperplane consists of a pair of skew lines at

## PDF page 20

Mathematics 2015, 3

1211

maximum distance from each other; there are, as depicted in Figure 13, 10 hyperplanes of this
type and they correspond to α-points of PG(4, 2). A type-two hyperplane features a point and
all the points not collinear with it, the latter forming the Pasch configuration; there are, as shown
in Figure 14, 15 hyperplanes of this type and their counterparts are β-points of PG(4, 2). A type-three
hyperplane is identical with the Desargues configuration; we find, as portrayed in Figure 15, altogether
six hyperplanes of this type, each standing for a γ-point of PG(4, 2).

Figure 12. An illustration of the structure of the (154 , 203 )-configuration, built around the
model of the Desargues configuration shown in Figure 6. The five points added to the
Desargues configuration are the three peripheral points and the red and blue point in the
center. The 10 lines added are three lines denoted by red color, three blue lines, three lines
joining pairwise the three peripheral points and the line that comprises the three points in the
center of the figure, that is the ones represented by a bigger red circle, a smaller blue circle
and a medium-sized black one.

3

3

3

1
Figure 13. The 10 geometric hyperplanes of the (154 , 203 )-configuration of type one; the
number below a subfigure indicates how many copies of the particular hyperplane we get by
rotating the corresponding subfigure through 120 degrees around its center.

## PDF page 21

Mathematics 2015, 3
1212
3
3
<b>Figure 14.</b> The 15 geometric hyperplanes of the <math>(15_4, 20_3)</math>-configuration of type two.
5
<b>Figure 15.</b> The six geometric hyperplanes of the <math>(15_4, 20_3)</math>-configuration of type three.

## PDF page 22

Mathematics 2015, 3

1213

a

b

c

d

e

Figure 16. The five types of Veldkamp lines of the (154 , 203 )-configuration. Here, unlike
Figures 8–10, each representative of a geometric hyperplane is drawn separately and different
colors are used to distinguish between different hyperplane types: red is reserved for type
one, yellow for type two and blue for type three hyperplanes. As before, the black color
denotes the core of a Veldkamp line, that is the elements common to all the three hyperplanes
comprising it.
We also find that our (154 , 203 )-configuration yields 155 Veldkamp lines that are, as expected, of five
different types. A type-I Veldkamp line, shown in Figure 16a, features two hyperplanes of type one and

## PDF page 23

Mathematics 2015, 3

1214

a type-two hyperplane and its core consists of two points that are at maximum distance from each other;
( )
= 15 × 6/2 = 45 Veldkamp lines of this type and they correspond to defective lines
there are 10
2
of PG(4, 2) of type {α, α, β}. A type-II Veldkamp line, featured in Figure 16b, is composed of three
hyperplanes of type two that share three points on a common line; there are, obviously, 20 Veldkamp
lines of this type, having for their counterparts defective lines of PG(4, 2) of type {β, β, β}. A type-III
Veldkamp line, portrayed in Figure 16c, also consists of three hyperplanes of type two, but in this case
the three common points are pairwise at maximum distance from each other; a quick count leads to
15 Veldkamp lines of this type, these being in a bijection with 15 ordinary lines of PG(4, 2) of type
{β, β, β}. Next, we have a type-IV Veldkamp line, depicted in Figure 16d, which exhibits a hyperplane
of each type and whose core is composed of a line and a point at the maximum distance from it; since
for each line of our (154 , 203 )-configuration there are three points at maximum distance from it, there
are 20 × 3 = 60 Veldkamp lines of this type, having their twins in ordinary lines of PG(4, 2) of type
{α, β, γ}. Finally, we meet a type-V Veldkamp line, sketched in Figure 16e, which is endowed with
two hyperplanes of type three and a single one of type two, and whose core is isomorphic to the Pasch
()
configuration; hence, we have 62 = 15 Veldkamp lines of this type, being all representatives of ordinary
lines of PG(4, 2) of type {β, γ, γ}.
Before embarking on the final case to be dealt with in detail, it is worth having a closer look at
our (154 , 203 )-configuration and pointing out its intimate relation with the famous Pascal’s Mystic
Hexagram. If six arbitrary points are chosen on a conic section and joined by line segments in any
order to form a hexagon, then the three pairs of opposite sides of the hexagon meet in three points
that lie on a straight line, the latter being called the Pascal line. Taking the permutations of the six
points, one obtains 60 different hexagons. Thus, the so-called complete Pascal hexagon determines
altogether 60 Pascal lines, which generate a remarkable configuration of 146 points and 110 lines called
the hexagrammum mysticum, or the complete Pascal figure (for the most comprehensive, applet-based
representation of this remarkable geometrical object, see [15]). Both the points and lines of the complete
Pascal figure split into several distinct families, usually named after their discoverers in the first half of
the 19-th century. We are concerned here with the 15 Salmon points and the 20 Cayley lines (see, for
example, [16,17]) which form a (154 , 203 )-configuration. This configuration is discussed in some detail
in [18], where it is also depicted (Figure 6) and called the Cayley-Salmon (154 , 203 )-configuration. It
is precisely this Cayley-Salmon (154 , 203 )-configuration which our 32-nionic (154 , 203 )-configuration
is isomorphic to. The same configuration is also portrayed in Figure 8 of [15]. In the latter work, two
different views/interpretations of the configuration are also mentioned. One is as three pairwise-disjoint
triangles that are in perspective from a line, in which case the centers of perspectivity are guaranteed
by Desargues’ theorem to also lie on a line; we just stress here that these two lines form a geometric
hyperplane (of type one, see Figure 13). The other view of the figure takes any point of the configuration
to be the center of perspectivity of two quadrangles whose six pairs of corresponding sides meet
necessarily in the points of a Pasch configuration; again, the point and the associated Pasch configuration
form a geometric hyperplane (of type two, see Figure 14). We can offer one more view of the
configuration, stemming from the existence of type-three hyperplanes, namely as the incidence sum
of a Desargues configuration and three triangles on a commmon side (see Figure 15).

## PDF page 24

Mathematics 2015, 3

1215

5. 64-Nions and a (215 , 353 )-Configuration
The final algebra we shall treat in sufficient detail is A6 , or the 64-nions. From the corresponding
multiplication table, which due to its size we do not show here but which is freely available at [19], we
infer the existence of 651 distinguished triples of imaginary units. Regarding the 63 imaginary units of
64-nions as points and the 651 distinguished triples of them as lines, we obtain a point-line incidence
structure where each line has three points and each point is on 31 lines, and which is isomorphic to
PG(5, 2). Following the usual procedure, we find that 350 lines of this space are defective and 301
ordinary. Likewise the preceding case, we encounter three different types of points in our 64-nionic
PG(5, 2): 35 α-points, each of which is on 21 defective and 10 ordinary lines; 21 β-points, each of
which is on 15 defective and 16 ordinary lines; and seven γ-points, each of them being on 31 ordinary
(and, hence, on zero defective) lines. This stratification of the point-set of PG(5, 2) leads, in turn, to
three different kinds of defective lines and four distinct kinds of ordinary lines. Out of 350 defective
lines, we find 105 of type {α, α, α}, 210 of type {α, α, β} and 35 of type {β, β, β}. On the other hand,
301 ordinary lines are partitioned into 105 lines of type {α, β, β}, 70 of type {α, α, γ}, 105 of type
{α, β, γ} and 21 of type {β, γ, γ}.
The Veldkamp space mimicking such a fine structure of PG(5, 2) is that of a particular
(215 , 353 )-configuration, C6 , that also lives in our PG(5, 2) and whose points are the 21 β-points and
whose lines are the 35 defective lines of {β, β, β} type. To visualise this configuration, we build
it around the model of the Cayley-Salmon (154 , 203 )-configuration of 32-nions shown in Figure 12.
Given the Cayley-Salmon configuration, there are six points and 15 lines to be added to yield our
(215 , 353 )-configuration, and this is to be done in such a way that the configuration we started with forms
a geometric hyperplane in it. As putting all the lines into a single figure would make the latter look rather
messy, in Figure 17 we briefly illustrate this construction by drawing six different figures, each featuring
all six additional points (gray) but only five out of 15 additional lines (these lines being also drawn in
gray color), namely those passing through a selected additional point (represented by a doubled circle).
Employing this handy diagrammatical representation, one can verify that our (215 , 353 )-configuration
exhibits 63 geometric hyperplanes that fall into three distinct types. A type-one hyperplane consists
of a line and its complement, which is the Pasch configuration; there are 35 distinct hyperplanes of
this form, each corresponding to an α-point of our PG(5, 2). A type-two hyperplane comprises a point
and its complement, which is the Desargues configuration; there are 21 hyperplanes of this form, each
having a β-point for its PG(5, 2) counterpart. Finally, a type-three hyperplane is isomorphic to the
Cayley-Salmon configuration; there are seven distinct hyperplanes of this type, each answering to a
γ-point of the PG(5, 2). We leave it with the interested reader to verify by themselves that the Veldkamp
space of our (215 , 353 )-configuration indeed features 651 lines that do fall into the above-mentioned
seven distinct kinds.
As in the previous two cases, we shall briefly describe a couple of interesting views of our
(215 , 353 )-configuration, both related to type-one hyperplanes. The first one is as four triangles in
perspective from a line where the points of perspectivity of six pairs of them form a Pasch configuration,
the line and the Pasch configuration comprising a geometric hyperplane (compare with the first view of
both the Desargues and the Cayley-Salmon configuration). This is sketched in Figure 18, where the four

## PDF page 25

Mathematics 2015, 3

1216

triangles are denoted, in boldfacing, by green, red, yellow and blue color, the line of perspectivity by
boldfaced gray color, and the points of perspectivity of pairs of triangles (together with the corresponding
lines they lie on and that are also boldfaced) by black color. The other view is as three complete
quadrangles that are pairwise in perspective in such a way that the three points of perspectivity lie
on a line and where the six triples of their corresponding sides meet at points located on a Pasch
configuration, again the line and the Pasch configuration forming a geometric hyperplane (compare with
the second view of both the Desargues and the Cayley-Salmon configuration).
a

d

b

c

e

f

Figure 17. An illustration of the structure of the (215 , 353 )-configuration, built around the
model of the Cayley-Salmon (154 , 203 )-configuration shown in Figure 12.

Figure 18. A “generalized Desargues” view of the (215 , 353 )-configuration.

## PDF page 26

Mathematics 2015, 3
6. 2N -Nions and a

1217

((
)
N +1
2

(N +1) )
-Configuration
,
3
N −1
3

At this point it is quite easy to spot the general pattern. If one also includes the trivial cases
of complex numbers (N = 1), where the relevant geometry is just a single point, that is, the
(10 , 03 )-configuration, and quaternions (N = 2), whose geometry is a single line, that is, the
(31 , 13 )-configuration, we obtain the following nested sequence of configurations whose Veldkamp
spaces capture the stratification/partition of the point- and line-sets of the 2N -nionic PG(N − 1, 2),
N being a positive integer,
(10 , 03 ),
(31 , 13 ),
(62 , 43 ),
(103 , 103 ),
(154 , 203 ),
(215 , 353 ),
...,
((
)
(
))
N +1
N +1
,
,
2
3
N −1
3
....
It is curious to notice that the first entry represents a triangular number, while the second one is
a tetrahedral number, or triangular pyramidal number. In other words, we get a nested sequence of
) (r+k−1)
(
)-configurations with r = N − 1 and k = 3, whose properties have very
,
binomial ( r+k−1
k
r
k
r
recently been discussed in a couple of interesting papers [20,21]. The first few configurations are shown,
in a form where the configurations are nested inside each other, in Figure 19.

C

S

H

O

32

64 ...

(N +1) )
-configurations of 2N -nions for
,
Figure 19. A nested hierarchy of finite
3
2
3
N −1
1 ≤ N ≤ 5 when embedded in the Cayley-Salmon configuration (N = 5).
((
)
N +1

## PDF page 27

Mathematics 2015, 3

1218

A particular character
this nesting
is reflected in the structure of geometric hyperplanes.
(( of
)
(N +1) )
N +1
, 3 3 -configuration by CN , we can express the types of geometric
Denoting our generic
2
N −1
hyperplanes of the above-discussed cases in a compact form as follows:
C1 :
C2 :
C3 :
C4 :
C5 :
C6 :

∅,
C1 ,
C2 ,
C3 ,
C4 ,
C5 ,

C1 ⊔ C1 ,
C2 ⊔ C1 ,
C3 ⊔ C1 , C2 ⊔ C2 ,
C4 ⊔ C1 , C3 ⊔ C2

which implies the following generic hyperplane compositions:
CN : CN −1 , CN −2 ⊔ C1 ,

CN −3 ⊔ C2 ,

...,

C N ⊔ C N −1

CN : CN −1 , CN −2 ⊔ C1 ,

CN −3 ⊔ C2 ,

...,

C⌊ N ⌋ ⊔ C⌊ N ⌋

2

2

or
2

2

according as N is even or odd, respectively; here, the symbol “⊔” stands for a disjoint union of two sets.
In the spirit of previous sections, let us also have a closer look at the nature of our generic CN . To
this end, we first recall the following observations. C4 , the Desargues configuration, can be viewed as
(4 − 2 =) two triangles in perspective from a line which are also perspective from a point, that is C1 ; the
line and the point form a geometric hyperplane of C4 . Next, C5 , the Cayley-Salmon configuration, admits
a view as (5 − 2 =) three triangles in perspective from a line where the points of perspectivity of three
pairs of them are on a line, aka C2 ; the two lines form a geometric hyperplane of C5 . Finally, C6 , our
(215 , 353 )-configuration, can be treated as (6 − 2 =) four triangles in perspective from a line where the
points of perspectivity of six pairs of them lie on a Pasch configuration, alias C3 ; the line and the Pasch
configuration form a geometric hyperplane of C6 . Generalizing these observations, we conjecture that
for any N ≥ 4, CN can be regarded as N − 2 triangles that are in perspective from a line in such a way
)
(
that the points of perspectivity of N 2−2 pairs of them form the configuration isomorphic to CN −3 , where
the latter and the axis of perspectivity form a geometric hyperplane of CN .
Next, we invoke the concept of combinatorial Grassmannian (see, for example, [22,23]). Briefly,
a combinatorial Grassmannian Gk (|X|), where k is a positive integer and X is a finite set, is a point-line
incidence structure whose points are k-element subsets of X and whose lines are (k + 1)-element subsets
of X, incidence
inclusion.
It is known [22] that if |X| = N + 1 and k = 2, G2 (N + 1) is
(( being
(N +1) )
)
N +1
, 3 3 -configuration; in particular, G2 (4) is the Pasch configuration, G2 (5)
a binomial
2
N −1
is the Desargues configuration and G2 (N + 1)’s with N ≥ 5 are called generalized Desargues
configurations. Now, from our detailed examination of the four cases it follows that C3 , C4 , C5 , C6 , . . . , CN
)
)
(
(
are endowed with 1, 5, 15, 35, . . . , N4+1 Pasch configurations. And as N 4+1 is also the number of Pasch
configurations in G2 (N + 1), N ≥ 3, we are also naturally led to conjecture that CN ∼
= G2 (N + 1). From
what we have found in the previous sections it follows that this property indeed holds for 1 ≤ N ≤ 6,
being illustrated for N = 5 and N = 6 in Figure 20.

## PDF page 28

Mathematics 2015, 3

1219

16

57

27
37

47
12
15
13 26

35
23
36

14
25
56
34

17

45
24
46

67

Figure 20. Left: A diagrammatical proof of the isomorphism between C5 and G2 (6). The
points of C5 are labeled by pairs of elements from the set {1, 2, . . . , 6} in such a way that each
line of the configuration is indeed of the form {{a, b}, {a, c}, {b, c}}, a ̸= b ̸= c ̸= a. Right:
A pictorial illustration of C6 ∼
= G2 (7). Here, the labels of six additional points are only
depicted, the rest of the labeling being identical to that shown in the left-hand side figure.
7. Conclusions
An intriguing finite-geometrical underpinning of the multiplication tables of Cayley-Dickson algebras
AN , 3 ≤ N ≤ 6, has been found that admits generalization to any higher-dimensional AN . This
started with an observation that the multiplication properties of imaginary units of the algebra AN are
encoded in the structure of the projective space PG(N − 1, 2). Next, this space was shown to possess
a refined structure stemming from particular properties of triples of imaginary units forming its lines.
To account for this refinement, we employed the (concept of Veldkamp
space of point-line incidence
(N +1)
(N +1) )
structure and found out the latter to be a binomial
, 3 3 -configuration CN ; in particular,
2
N −1
C3 (octonions) was found to be isomorphic to the Pasch (62 , 43 )-configuration, C4 (sedenions) to the
famous Desargues (103 )-configuration, C5 (32-nions) to the Cayley-Salmon (154 , 203 )-configuration
found in the well-known Pascal mystic hexagram and C6 (64-nions) was shown to be identical with a
particular (215 , 353 )-configuration that can be viewed as four triangles in perspective from a line where
the points of perspectivity of six pairs of them form a Pasch configuration. These configurations are seen
to form a remarkable nested pattern, where CN −1 is embedded in CN as its geometric hyperplane, that
naturally reflects the spirit of the Cayley-Dickson recursive construction of corresponding algebras.
It is a well-known fact that the only first four algebras AN , 0 ≤ N ≤ 3, are “well-behaved” in the
sense of being normed, alternative and devoid of zero-divisors—the facts that are frequently offered as an
explanation why a relatively little attention has been paid so far to their higher-dimensional cousins, these
latter being even regarded by some scholars as “pathological”. It may well be that our finite-geometric,

## PDF page 29

Mathematics 2015, 3

1220

Veldkamp-space-based approach will be able to shed a novel, unexpected light at this issue as it is only
starting with N = 4 when CN is found to feature a “generalized Desargues property” in the sense that
it can be interpreted as N − 2 triangles that are in perspective from a line in such a way that the points
)
(
of perspectivity of N 2−2 pairs of them form the configuration isomorphic to CN −3 . Or, in a slightly
different form, it is only for N ≥ 4 when CN contains Desargues configurations, these occurring as
components of its geometric hyperplanes at that.
Acknowledgments
This work was partially supported by the VEGA Grant Agency, Project 2/0003/13, as well as by
the Austrian Science Fund (Fonds zur Förderung der Wissenschaftlichen Forschung (FWF)), Research
Project M1564-N27. We would like to express our sincere gratitude to Hans Havlicek (Vienna University
of Technology) for a number of critical remarks on the first draft of the paper. Our special thanks go to
Jörg Arndt who computed for us multiplication tables of octonions, sedenions, 32-nions and 64-nions.
We are also very grateful to Boris Odehnal (University of Applied Arts, Vienna) for creating nice
computer versions of several figures.
Author Contributions
Metod Saniga and Frédéric Holweck conducted research, Metod Saniga wrote the paper and
Petr Pracna computerized a diagrammatical presentation of the main results.
Conflicts of Interest
The authors declare no conflict of interest.
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

Jacobson, N. Basic Algebra I; W. H. Freeman: San Francisco, CA, USA, 1974.
Schafer, R.D. Introduction to Non-Associative Algebras; Dover: New York, NY, USA, 1995.
Moreno, G. Hopf construction map in higher dimensions. Bol. Soc. Mat. Mex. 2004, 10, 383–397.
Arndt, J. Matters Computational: Ideas, Algorithms, Source Code; Springer: Heidelberg,
Germany, 2011.
Arndt, J. The FXT Demos: Arithmetical Algorithms. Available online: http://jjj.de/fxt/
demo/arith/index.html (accessed on 30 January 2014).
Baez, J.C. The octonions. Bull. Am. Math. Soc. 2002, 39, 145–205.
Culbert, C. Cayley-Dickson algebras and loops. J. Gen. Lie Theory Appl. 2007, 1, 1–17.
Shult, E.E. Points and Lines: Characterizing the Classical Geometries; Springer: Berlin,
Germany, 2011.
Grünbaum, B. Configurations of Points and Lines; Graduate Studies in Mathematics 103; American
Mathematical Society: Providence, RI, USA, 2009.
Buekenhout, F.; Cohen, A.M. Diagram Geometry: Related to Classical Groups and Buildings;
Springer: Berlin, Germany, 2013.

## PDF page 30

Mathematics 2015, 3

1221

11. Grannell, M.J.; Griggs, T.S. The Pasch Configuration.
Encyclopaedia of Mathematics.
Available online: http://www.encyclopediaofmath.org/index.php/Pasch configuration (accessed
on 14 May 2014).
12. Polster, B. A Geometrical Picture Book; Springer Verlag; New York, NY, USA, 1998.
13. Pisanski, T.; Servatius, B. Configurations from a Graphical Viewpoint; Birkhäuser: Basel,
Switzerland, 2013.
14. Saniga, M.; Planat, M.; Pracna, P.; Havlicek, H. The Veldkamp space of two-qubits. SIGMA 2007,
3, doi:10.3842/SIGMA.2007.075.
15. Fisher, J.C.; Fuller, N. The Complete Pascal Figure Graphically Presented. Available online:
http://www.math.uregina.ca/˜fisher/Norma/paper.html (accessed on 14 May 2014).
16. Lord, E. Symmetry and Pattern in Projective Geometry; Springer: Heidelberg, Germany, 2013.
17. Conway, J.; Ryba, A. The Pascal mysticum demystified. Math. Intell. 2012, 34, 4–8.
18. Boben, M.; Gévay, G.; Pisanski, T. Danzer’s configuration revisited. Adv. Geom. 2015, 15,
393–408.
19. Arndt, J. TMP-Zero-Divisors, Available online: http://jjj.de/tmp-zero-divisors/mult-table-64-ions.txt
(accessed on 30 January 2014).
20. Prażmowska, M.; Pra
K. Binomial Configurations Which Contain Complete Graphs:
((żmowski,
) (n+1) )
n+1
-Configuration. 2014, arXiv:1404.4064. Available online:
Kn -Subgraphs of a
2 n−1 3 3
http://arxiv.org/abs/1404.4064 (accessed on 17 May 2014).
21. Petelczyc, K.; Prażmowska, M.; Prażmowski, K.; A complete classification of the
(154 203 )-configurations with at least three K5 -graphs. Discret. Math. 2015, 338, 1243–1251.
22. Prażmowska, M. Multiple perspectives and generalizations of the Desargues configuration.
Demonstr. Math. 2006, 39, 887–906.
23. Prażmowska, M.; Prażmowski, K. A generalization of Desargues and Veronese configurations.
Serdica Math. J. 2006, 32, 185–208.
c
⃝ 2015 by the authors; licensee MDPI, Basel, Switzerland. This article is an open access article
distributed under the terms and conditions of the Creative Commons Attribution license
(http://creativecommons.org/licenses/by/4.0/).
