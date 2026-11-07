Source: see manifest row of the PDF
PDF sha256: 6949cedf4a2baace787c63991958e7cfba7d0ffe892f7e45c8575e3183a74743
License: https://creativecommons.org/licenses/by-sa/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of geometric-algebra-for-physicists--6949cedf4a.pdf

Transcription of `geometric-algebra-for-physicists--6949cedf4a.pdf` in this directory, 131 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 1-2, 10, 100, 122, 130 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories; pages 3-9, 11-99, 101-121, 123-129, 131 from the PDF's own text layer (pdftotext version 26.10.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Geometric Algebra for Physicists
Lecture notes
Preliminary version!
For the most up-to-date version, visit
https://physi.uni-heidelberg.de/~vhollmeier/ga4p

## PDF page 2

CC O O O O O O O O O O O O O O O O O O 
This work is licensed under a Creative Commons
"Attribution-ShareAlike 4.0 International" license.
1

## PDF page 3

Contents
0 Introduction
0.1 Overview . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
0.2 History of geometric algebra . . . . . . . . . . . . . . . . . . . . . . . . . .
0.2.1 “Unified language for physics” claims . . . . . . . . . . . . . . . . .
0.3 This lecture . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
0.3.1 Literature . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

3
3
4
5
5
6

1 Basics of geometric algebra
1.1 k-vectors and the exterior product . . . . . . . . . . . . . . . . . . . . . . .
1.1.1 Scalars and vectors . . . . . . . . . . . . . . . . . . . . . . . . . . .
1.1.2 Bivectors . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
1.1.3 Trivectors and more . . . . . . . . . . . . . . . . . . . . . . . . . .
1.1.4 Invertibility? . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
1.2 The interior product . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
1.2.1 Interior product between k-vectors and vectors . . . . . . . . . . . .
1.2.2 Properties of the interior product . . . . . . . . . . . . . . . . . . .
1.3 Multivectors and the geometric product . . . . . . . . . . . . . . . . . . . .
1.3.1 Grade projection . . . . . . . . . . . . . . . . . . . . . . . . . . . .
1.3.2 Anticommutation relations . . . . . . . . . . . . . . . . . . . . . . .
1.3.3 Higher grades . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
1.3.4 Invertibility . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
1.3.5 Interior and exterior product revisited . . . . . . . . . . . . . . . .
1.4 The two-dimensional geometric algebra Cl(2) . . . . . . . . . . . . . . . . .
1.4.1 The even subalgebra Cl+ (2) and complex numbers . . . . . . . . . .
1.4.2 Two-dimensional rotations . . . . . . . . . . . . . . . . . . . . . . .

8
8
9
9
11
13
13
14
16
16
18
19
20
22
23
24
24
26

2 Geometric algebra of space
29
2.1 Overview . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 29
2.1.1 3D pseudoscalars . . . . . . . . . . . . . . . . . . . . . . . . . . . . 30
2.1.2 Eliminating the cross product . . . . . . . . . . . . . . . . . . . . . 33
2.2 Transformations . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 35
2.2.1 Projection and rejection . . . . . . . . . . . . . . . . . . . . . . . . 36
2.2.2 Reflections . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 36
2.2.3 Rotations . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 37
2

## PDF page 4

2.3

2.4

2.2.4 Some facts about rotors . . . . . . . . . . . . . . . . . . . . . . . .
2.2.5 A short note on quaternions . . . . . . . . . . . . . . . . . . . . . .
2.2.6 Infinitesimal rotations . . . . . . . . . . . . . . . . . . . . . . . . .
2.2.7 Angular velocity . . . . . . . . . . . . . . . . . . . . . . . . . . . .
Differential operators . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
2.3.1 The geometric derivative . . . . . . . . . . . . . . . . . . . . . . . .
2.3.2 Identities involving the geometric derivative . . . . . . . . . . . . .
2.3.3 Product rule . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
Pauli matrices . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

40
41
42
44
45
46
48
49
50

3 Tensor notation
52
3.1 Overview . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 52
3.1.1 Tensor notation is not the same as matrix representation . . . . . . 53
3.1.2 Fully antisymmetric rank k tensors . . . . . . . . . . . . . . . . . . 53
3.1.3 Vectors, bivectors and trivectors . . . . . . . . . . . . . . . . . . . . 54
3.1.4 Extracting components . . . . . . . . . . . . . . . . . . . . . . . . . 55
3.1.5 Some examples . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 56
3.2 Operations in tensor notation . . . . . . . . . . . . . . . . . . . . . . . . . 56
3.2.1 Linear operations . . . . . . . . . . . . . . . . . . . . . . . . . . . . 57
3.2.2 Symmetric and antisymmetric parts . . . . . . . . . . . . . . . . . . 57
3.2.3 Interior product . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 58
3.2.4 Exterior product . . . . . . . . . . . . . . . . . . . . . . . . . . . . 60
3.3 Differential forms . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 61
3.4 Transformation matrices . . . . . . . . . . . . . . . . . . . . . . . . . . . . 62
4 Geometric algebra of spacetime
65
4.1 Basics . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 66
4.1.1 Foundations of special relativity . . . . . . . . . . . . . . . . . . . . 66
4.1.2 Four-vectors . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 66
4.1.3 Natural units . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 67
4.1.4 Examples of four-vectors . . . . . . . . . . . . . . . . . . . . . . . . 68
4.1.5 Brief recap on time in special relativity . . . . . . . . . . . . . . . . 72
4.1.6 STA multivectors . . . . . . . . . . . . . . . . . . . . . . . . . . . . 73
4.1.7 A note on the Dirac gamma matrices . . . . . . . . . . . . . . . . . 76
4.2 Spacetime rotations . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 77
4.2.1 Circular rotations . . . . . . . . . . . . . . . . . . . . . . . . . . . . 77
4.2.2 Hyperbolic rotations . . . . . . . . . . . . . . . . . . . . . . . . . . 78
4.2.3 Rotations bivectors revisited . . . . . . . . . . . . . . . . . . . . . . 80
4.3 Relativistic dynamics . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 82
4.3.1 Relative velocities . . . . . . . . . . . . . . . . . . . . . . . . . . . . 82
4.3.2 Relativistic acceleration . . . . . . . . . . . . . . . . . . . . . . . . 83
4.3.3 Relativistic kinematics . . . . . . . . . . . . . . . . . . . . . . . . . 86
4.4 Space-time split . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 89
4.4.1 The even subalgebra of Cl(1, 3) . . . . . . . . . . . . . . . . . . . . 89
3

## PDF page 5

4.5

4.4.2 Splitting bivectors . . . . . . . . . . . . . . . . . . . . . . . . . . .
4.4.3 Splitting vectors . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
4.4.4 Relativistic acceleration revisited . . . . . . . . . . . . . . . . . . .
STA geometric derivatives . . . . . . . . . . . . . . . . . . . . . . . . . . .

90
90
93
94

5 Electrodynamics
96
5.1 Overview . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 98
5.1.1 Traditional formalism for electromagnetism . . . . . . . . . . . . . . 98
5.1.2 Geometric formalism for electromagnetism . . . . . . . . . . . . . . 99
5.1.3 The electrodynamic equation . . . . . . . . . . . . . . . . . . . . . 101
5.1.4 A note on differential forms . . . . . . . . . . . . . . . . . . . . . . 102
5.1.5 Gauge fields . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 103
5.2 Solutions to the electromagnetic equation . . . . . . . . . . . . . . . . . . . 106
5.2.1 Plane-wave solutions . . . . . . . . . . . . . . . . . . . . . . . . . . 106
5.2.2 Electrostatics . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 110
5.3 The electromagnetic force . . . . . . . . . . . . . . . . . . . . . . . . . . . 115
5.3.1 Reformulation of the electric and magnetic force in STA . . . . . . 115
5.3.2 Geometric interpretation . . . . . . . . . . . . . . . . . . . . . . . . 117
6 Geometric calculus

119

7 Spinors
120
7.1 Matrix representations . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 120
7.1.1 Pauli representation . . . . . . . . . . . . . . . . . . . . . . . . . . 121
7.1.2 STA representation . . . . . . . . . . . . . . . . . . . . . . . . . . . 123
7.2 Fundamenentals of spinors . . . . . . . . . . . . . . . . . . . . . . . . . . . 125
7.2.1 What is a vector? . . . . . . . . . . . . . . . . . . . . . . . . . . . . 125
7.2.2 Going beyond vector matrices and vector tensors . . . . . . . . . . 126
Acknowledgements

128

4

## PDF page 6

Chapter 0
Introduction
If a man, holding a belief which he
was taught in childhood or persuaded
of afterwards, keeps down and pushes
away any doubts which arise about it
in his mind, purposely avoids the
reading of books and the company of
men that call in question or discuss
it, and regards as impious those
questions which cannot easily be
asked without disturbing it - the life
of that man is one long sin against
mankind.
William Clifford, The Ethics of Belief
(1879)

0.1

Overview

Physics is the science of trying to describe reality with mathematics. Over time, specific
mathematical constructs like vectors, matrices, tensors or differential forms have been
established as the standard mathematical language for physics. However, these concepts
are not unique. Physicists do not do mathematics for the sake of mathematics, but to
model reality - and the most important part of this is to find the best mathematical tools
for the specific phenomenon we are trying to describe.
Sadly, it is not commonplace in physics to try to improve upon the existing mathematical tooling. Once some mathematical concept like the cross product is introduced,
physicists generally don’t try to improve it, but uncritically use it for all eternity - even
if it is already long obsolete for mathematicians. This has led us into a difficult situation
- the mathematical tooling we are being taught in our university classes is a messy, incoherent patchwork that grew over multiple centuries. The various inconsistencies that

5

## PDF page 7

have crept into it over time have a very real effect on the everyday work of physicists they inhibit intuitive understanding of physical concepts, slow down our calculations and
lead to misunderstandings.
Geometric algebra (GA) is an attempt at clearing up some parts of this chaos. In
particular, geometric algebra replaces, improves and unifies
• vector algebra,
• large parts of matrix algebra,
• antisymmetric tensor algebra,
• exterior algebra and differential forms,
• multivariate, vector and exterior calculus,
• the tetrad formalism in differential geometry, and
• spinor algebra
into a simple, elegant and natural framework. Many concepts from physics become a lot
clearer once they are reformulated in GA. In particular, GA puts a focus on geometric
intuition for what is going on behind the maths.
The core concept of geometric algebra is the so-called geometric product. It is
both associative and invertible. These properties make practical calculations with it very
simple. To make it work out, we need to define so-called k-vectors and multivectors a generalization of the concept of a vector.

0.2

History of geometric algebra

The inventors of geometric algebra in the modern sense are Hermann Grassmann (1809 1877) and William Clifford (1845 - 1879).
Grassmann introduced the wedge product and the exterior algebra in 1844. At
that time, however, the general concept of a vector still was in its infancy, and Grassmann’s exterior algebra was regarded as incomprehensible by contemporary physicists
and mathematicians. Also, it had several important issues - the wedge product was not
invertible, which hindered practical computations. Grassmann’s work was largely ignored
during his lifetime.
The situation changed, however, when Clifford combined the wedge product with
the inner product to form the so-called geometric product. Based on Grassman’s
exterior algebra, he introduced geometric algebra in his 1878 work “Applications of
Grassmann’s Extensive Algebra”. The algebra he described was very elegant and much
easier to work with than exterior algebra. Unfortunately, he died from tuberculosis several
months later, so his ideas had little chance to spread. His work was only remembered by
some mathematicians under the name “Clifford algebra”.

6

## PDF page 8

Meanwhile, physicists were investigating electromagnetism. This is when the concept
of vectors and vector fields became mainstream in physics. However, Josiah Gibbs and
Oliver Heaviside, two chief investigators of electromagnetism at that time, did not know
of the work of Clifford and instead invented the makeshift ad-hoc construct of the “cross
product” in the 1880s. For physicists, it certainly represented an advance at that time,
but it should never have become a permanent solution. Unfortunately, it did - Heaviside’s
formulation of the Maxwell equations is identical to the modern-day one being taught to
undergraduate physics students.
The cross product quickly took its roots in physics in the early 20th century, and
Clifford’s geometric algebra was largely forgotten until the advent of quantum mechanics.
While investigating electron spin, Wolfgang Pauli introduced the Pauli matrices in 1927,
and Paul Dirac the Dirac matrices in 1928. However, they were regarded as something
purely quantum-mechanical at that time - what Pauli and Dirac did not realize is that
the algebra formed by their matrices is nothing but the geometric algebra, and that their
matrices have a geometric interpretation.
Later, in the 1960s, theoretical physicist David Hestenes (1933 - ) rediscovered Clifford’s work and made the connection to the work of Pauli and Dirac. He realized that
geometric algebra was a much more convenient, elegant and natural tool for performing
spatial computations than the matrix-vector and tensor algebra prevailing at his time,
and went on a crusade to convince other physicists to use it. He extended geometric
algebra to the theory of special relativity, devising spacetime algebra (STA).
However, geometric algebra did not gain traction until the 2000s and 2010s, when Chris
Doran and Anthony Lasenby published the comprehensive work Geometric Algebra for
Physicists (2002)1 . In the following years, geometric algebra began to spread among
physicists and computer scientists due to its many advantages in practical calculations.

0.2.1

“Unified language for physics” claims

Some proponents have claimed that geometric algebra is so versatile that it can be used
as a unified mathematical language for the entirety of physics. For instance, there are
GA reformulations of the entirety of Lie group theory - even of the groups that are not
directly elements of a (real) geometric algebra. Perhaps the most vocal proponents of this
claim are Doran and Lasenby - in their book, they try to use as few non-GA mathematical
constructs as possible. Critics of this claim have argued that the usefulness of geometric
algebra is limited to specific branches of mathematics, and that it should not be used
everywhere regardless of its specific benefits.

0.3

This lecture

In this lecture, we put a focus on practical computations and geometric intuition instead
of mathematical formalism. It is explicitly not a mathematics lecture, but a physics
1

This book is a great resource on how to apply geometric algebra to various parts of physics. Among
us GA connaisseurs, it is jokingly called the “GA bible” or the “Gabel”.

7

## PDF page 9

lecture. We roughly follow the path of Doran, Lasenby: Geometric Algebra for physicists
- we first introduct the concept of multivectors and the geometric product, and then
successively treat the 2D, 3D, and 1+3D geometric algebras and their applications to
everyday physics. In contrast to Doran and Lasenby, we put an emphasis on showing how
to directly translate between GA and conventional maths.
We are not going to concern ourselves with whether geometric algebra is a unified
language for physics. Instead, we are just going to switch between conventional math and
geometric algebra depending on whichever is most convenient for the problem at hand.
The conventions we use mostly come from either Doran and Lasenby or sudgylacmoe’s
videos on geometric algebra, or have been devised by ourselves to achieve maximum
clarity. Most notably, we use
τ = 2π.
(1)
Using Tau has become somewhat commonplace in geometric algebra, for instance in
sudgylacmoe’s videos. This convention makes rotations much clearer to think about - one
full turn is equal to τ radians, one half of a turn is equal to τ /2, a quarter-turn is equal
to τ /4, and so on.
We are going to use colored boxes for various purposes:
Warning 0.1

Example warning

This is a warning.
!
Tangent 0.1

Tangents

This is a box for information that is only tangentially related to the topic at hand
- hints at more advanced topics, trivia, fun facts, etc.
ç

Equation 0.1

Important equation
∂F = j

0.3.1

(2)
π

Literature

For further study, we recommend:
• Doran, Lasenby: Geometric Algebra for Physicists (2002). Very comprehensive work on geometric algebra. Most notably, its treatment of rotors and spinors
differs from ours.
• sudgylacmoe’s video series on geometric algebra (available on YouTube).
3blue1brown-styled introduction to various fields of geometric algebra. Very good
primer.

8

## PDF page 10

• Hestenes: Spacetime Algebra (1966). The original book that reintroduced
geometric algebra to physics. It covers the material of the second half of this
lecture, although it uses some conventions that have become antiquated.
9

## PDF page 11

Chapter 1
Basics of geometric algebra
Chapter summary
• k-vectors are a generalization of the concept of scalars and vectors.
• The exterior product can be used to construct k-vectors from vectors.
• The interior product “tears down” k-vectors.
• The geometric product is the combination between the interior and the exterior
product.
• Multivectors are sums of k-vectors of different grades.
• The geometric product is associative and invertible, but not commutative.
• The geometric algebra of the 2D plane Cl(2) is the simplest example of a geometric
algebra.
• We can use the 2D geometric algebra to reformulate complex numbers and 2D
rotations.

1.1

k-vectors and the exterior product

Much of geometric algebra revolves around finding a vector product that is both associative and invertible. In this chapter, we start by examining the exterior product
(also known as the outer product or wedge product), and the interior product (also
known as the dot product or inner product). We are going to show why neither of
them fulfills these requirements.
Then, we are going to combine the interior and exterior product into the geometric
product and show that it does exactly what we want - the geometric product will be
both associative and invertible.

10

## PDF page 12

1.1.1

Scalars and vectors

We start by introducing k-vectors, a core concept in GA. You already know two types
of k-vectors:
• scalars (or 0-vectors): A quantity without dimension or orientation.
• vectors (or 1-vectors): A length with an orientation.
First of all, let’s talk about scalars. Scalars represent simple quantities like mass
or temperature which have no concept of direction or orientation. There’s something
important to note about scalars: If two scalars are “located” at two different positions
in space - for instance the masses two distinct objects or two temperature measurements
at different locations - we consider them equal iff their numerical values are equal, even
though they are not at the same location. For instance, these two masses are considered
equal:

m = 1kg
m = 1 kg
Vectors, on the other hand, are a length with an orientation, like velocity, acceleration,
or momentum. We consider two vectors equal to each other iff they have the same length
and orientation. All of these vectors are considered equal to each other:

Mathematically, we describe vectors by first choosing a set of basis vectors, for
instance in three dimensions:
e1 , e 2 , e 3 .
(1.1)
A specific vector is formed by taking a linear combination of them. For instance, the
vectors in the above figure are given by
v = 2e1 + e2 .

1.1.2

Bivectors

The next grade of k-vectors we are going to examine is 2:
11

(1.2)

## PDF page 13

• bivectors (or 2-vectors): An area with an orientation.
To illustrate what that means, we are going to introduce the wedge product - also
called outer product or exterior product: Let a, b be two distinct vectors. They
define a parallelogram:
a∧b
b

a

This parallelogram has an area and an orientation. Thus, we call it a bivector B.
Its area can be calculated with the standard formula for parallelogram areas, while the
orientation is given by the combined orientations of a and b. Note that the order matters
- we drew a “swirl” inside the bivector that marks the rotation from the first vector a to
the second vector b.
Mathematically, this bivector is given by the wedge product ∧ between the two vectors:
B =a∧b

(1.3)

The wedge product is anticommutative for vectors, a ∧ b = −b ∧ a. The bivector
given by going from a to b is exactly −1 times the bivector given by going from b to a:
a∧b

b∧a

b

b

= (−1)·
a

a

Note that the direction of the swirl in the second bivector was reversed. As a consequence, this means that for any vector,
a ∧ a = 0.

(1.4)

This makes intuitive sense - two times the same vector span no area between them.
Two bivectors are equal iff they have the same orientation and area, regardless of
shape or position. This means that, for instance, the following bivectors are all equal to
each other:
12

## PDF page 14

So how do we mathematically determine if two bivectors B = a ∧ b and C = c ∧ d
are equal to each other? We make use of the associativity and distributivity of the wedge
product. For instance, for:
a = 2e1
b = e1 + 2e2
(1.5)
c = 3e1 − 4e2
d = e1 + e3 ,
we insert the respective basis decompositions of the vectors into the wedge product:

and

B =a∧b
= 2e1 ∧ (e1 + 2e2 )
= 2e1 ∧ e1 + 4e1 ∧ e2
= 4e1 ∧ e2 ,

(1.6)

C =c∧d
= (3e1 + 4e2 ) ∧ (e1 + e3 )
= 3e1 ∧ e1 + 3e1 ∧ e3 + 4e2 ∧ e1 + 4e2 ∧ e3
= −4e1 ∧ e2 + 4e2 ∧ e3 − 3e3 ∧ e1 .

(1.7)

We see that B and C clearly are not equal to each other. The form we brought them
into right now is somewhat analogous to the basis decomposition for a vector - similarly
to how we decomposed a vector a into a linear combination of e1 , e2 , ..., we decomposed
the bivectors B and C into linear combinations of e1 ∧ e2 , e2 ∧ e3 , ... to compare them.
Conventionally, we order the indices of our basis k-vectors in a cyclic way (1 → 2 →
3 → 1 · · · ).

1.1.3

Trivectors and more

The next type of k-vector on the line are:
• trivectors (or 3-vectors): A volume with an orientation.

13

## PDF page 15

We can form trivectors by taking the wedge product between three trivectors. For
instance, the trivector
T = e1 ∧ e2 ∧ e3
(1.8)
is the parallelepiped spanned by the vectors e1 , e2 and e3 .

Figure 1.1: The trivector e1 ∧ e2 ∧ e3 .
As before, trivectors with the same volume and orientation but with different shapes
are considered equal. In three dimensions, it is somewhat hard to see how different
trivectors could have different orientations - after all, there is only one possible orientation
for volumes in three dimensions. Consider, however, for a second, a four-dimensional
Euclidean space with the basis vectors e1 , e2 , e3 , e4 . Then, e.g. the trivectors
e1 ∧ e2 ∧ e3

(1.9)

e2 ∧ e3 ∧ e4

(1.10)

and
would have the same volume, but differing orientations.
Again, these vectors need to be linearly independent. If they aren’t, they don’t span
a volume, so the resulting trivector is zero. For instance, if we tried to take the wedge
product between e1 , e2 and e2 :
e1 ∧ e2 ∧ e2 = 0.
(1.11)
We can also form trivectors by taking an already existing bivector and wedging another
vector on top of it:
U = B ∧ e3 = (4e1 ∧ e2 ) ∧ e3
(1.12)
The wedge product is associative, so we can drop the parentheses:
U = 4 e1 ∧ e2 ∧ e3

(1.13)

In four-dimensional space, we will also get to know tetravectors, which represent
four-dimensional hypervolumes. We can construct tetravectors either by wedging four
vectors,
H = e1 ∧ e2 ∧ e3 ∧ e4 ,
(1.14)
a vector and a trivector,
H = (e1 ∧ e2 ∧ e3 ) ∧ e4

14

(1.15)

## PDF page 16

or two bivectors:
H = (e1 ∧ e2 ) ∧ (e3 ∧ e4 ).

(1.16)

There is something important to take note of here: When we go to higher grades, the
wedge product is not always anticommutative.
We could go to higher and higher grades of k-vectors, but in practice, tetravectors are
going to be the highest grade of k-vectors we need.

1.1.4

Invertibility?

We have seen how we can build up bivectors, trivectors and tetravectors using the wedge
product. But does it fulfill the conditions we set for a vector product? It is obviously
associative.
The exterior product between a scalar λ and some other k-vector X is just the scalar
multiplication:
λ ∧ X = λX
(1.17)
In this special case, the exterior product is invertible. However, in general, it is not
invertible at all for a simple reason:
We saw that the exterior product can be used to “span up” k-vectors from other kvectors of lower grade. For instance, the wedge product between a vector and a bivector
resulted in a trivector. For this to work out, the vector should not lie inside the bivector if it does, the parallelipiped will be completely flat, and the trivector equal to zero. Only
vectors with an orthogonal part w.r.t. the bivector produce non-zero trivectors.
This means that if we have a bivector B and a vector v with a part orthogonal and a
part parallel to B,
v = v⊥ + v∥
(1.18)
the wedge product B ∧ v will only contain information about the orthogonal part:
B ∧ v = B ∧ v⊥ + B ∧ v∥
= B ∧ v⊥

(1.19)

This means that the information about the parallel part v∥ is lost. In other words, given
the final trivector T = B ∧ v and the bivector B, there is no way we could reconstruct
the original vector v. Hence, the wedge product is not invertible.

1.2

The interior product

Next, we are going to talk about the interior product - also known as the inner
product or the dot product. We already know the simplest case of the interior product
- namely, the interior product between two vectors:
v·w

15

(1.20)

## PDF page 17

The interior product is commutative for vectors. It measures the amount of overlap
between v and w. If v and w are parallel, we have v · w = |v||w|. If v and w are
orthogonal, however, the interior product between them is zero.
Let’s compare this with the exterior product between two vectors, v ∧ w. If the two
vectors are orthogonal, the bivector has the area |v||w|, and if the vectors are parallel, the
exterior product between them is zero. This is roughly the opposite of what the exterior
product does.

1.2.1

Interior product between k-vectors and vectors

In conventional mathematics, the interior product is only defined for two vectors. It
measures the amount of overlap between them. This concept extends neatly to k-vectors,
though! For instance, we can take the interior product between a bivector B = e1 ∧ e2
and a vector e1 :
B · e1 = (e1 ∧ e2 ) · e1 .
(1.21)
To evaluate this product, we first reorder the geometric product such that the vector
standing next to the dot product is equal to the vector on the other side of the dot
product:
(e1 ∧ e2 ) · e1 = −(e2 ∧ e1 ) · e1 .
(1.22)
If the two vectors next to this an interior product are equal, we can rewrite the parentheses to:
−(e2 ∧ e1 ) · e1 = −e2 (e1 · e1 ) = −e2
(1.23)
Warning 1.1
This scheme only works if all of the vectors in the wedge product are orthogonal
to each other. This is autmoatically the case if the k-vectors are in basis form, i.e.
ei ∧ ·el . If they aren’t, we need to write out the wedge product into multiple terms
like in (1.7).
!
The result of the interior product between a bivector and a vector is another vector.
Intuitively, we can say that by dotting a vector onto the bivector, we “took away one
grade” from the bivector and thus made it a vector. The resulting vector is what “remains”
after “taking away” one grade from the bivector:
e2

·

e1

=

−e2

e1
If the bivector and the vector are orthogonal to each other, for instance
(e1 ∧ e2 ) · e3
16

(1.24)

## PDF page 18

the interior product between them is zero.
The same goes for trivectors and vectors. For instance, let T = e1 ∧ e2 ∧ e3 . If we
want to take the interior product between T and e.g. e2 ,
T · e2 = (e1 ∧ e2 ∧ e3 ) · e2

(1.25)

we first reorder the trivector such that the two e2 stand next to each other:
(e1 ∧ e2 ∧ e3 ) · e2 = −(e1 ∧ e3 ∧ e2 ) · e2 ,

(1.26)

Now that the vectors left and right of the interior product are equal, we can rewrite the
parentheses to:
−(e1 ∧ e3 ∧ e2 ) · e2 = −(e1 ∧ e3 )(e2 · e2 )
= −e1 ∧ e3
(1.27)
= e3 ∧ e1 .
The geometric picture is the same as previously - the grade of the trivector is lowered by
one:

·

=

Again, the remaining bivector is the bivector orthogonal to e2 .
The general formula for the interior product between a vector v and a k-vector w1 ∧
w2 ∧ · · · ∧ wk is:
Equation 1.1

General interior product between a k-vector and a vector

(w1 ∧ w2 ∧ · · · ∧ wk ) · v =
v · (w1 ∧ w2 ∧ · · · ∧ wk ) =

k
∑
i=1
k
∑

wi+1 ∧ wi+2 ∧ · · · ∧ wi−1 (wi · v)
(1.28)
(v · wi )wi+1 ∧ wi+2 ∧ · · · ∧ wi−1

i=1

π
In differential geometry, this operation is also called a contraction. The reason for
that will become clear when we treat tensor notation.
Tangent 1.1
There is also a more elegant way to define the interior product between k-vectors
- the Hodge adjoint of the exterior product. However, this definition requires too
continues in the next page
17

## PDF page 19

continues from the previous page
much abstract mathematics, so we won’t treat it in this lecture.
ç

1.2.2

Properties of the interior product

The interior product is not commutative in general. For instance, for a bivector and a
vector, it is anticommutative:
(e1 ∧ e2 ) · e1 = −(e2 ∧ e1 ) · e1 = −e2 (e1 · e1 ) = −e2
e1 · (e1 ∧ e2 ) = (e1 · e1 )e2 = e2

(1.29)

In general, the interior product between a k-vector and a vector is commutative if k is
odd, and anticommutative if k is even.
Just like the exterior product, the interior product is not invertible - but for a different
reason: The exterior product throws the parallel part of the vector away, while the interior
product throws the orthogonal part away. For instance, given a bivector B = e1 ∧ e2 and
an interior product B · v = e1 , we can tell that the component of v parallel to B is e2 ,
but there is no way to tell if it also had an e3 component - remember that
(e1 ∧ e2 ) · e3 = 0

(1.30)

In the general case v = v∥ + v⊥ , we can write that
B · v = B · v∥ .

(1.31)

Therefore, there is an inherent information loss in the interior product. It is not invertible.
Warning 1.2
In fact, the interior product is not even associative - consider for instance the two
expressions
T · (B · w)
(1.32)
(T · B) · w
The first expression evaluates to a bivector, while the second expression evaluates
to a a scalar. Therefore, it is important to always write down parentheses if we are
handling multiple interior products.
!

1.3

Multivectors and the geometric product

In our quest for an invertible product, we have examined the interior and exterior product.
We found that:
• The exterior product is used to construct k-vectors.
– The exterior product between a k-vector and a vector is a k + 1-vector.
18

## PDF page 20

– The exterior product throws away the parallel parts.
• The interior product is used to tear down k-vectors.
– The interior product between a k-vector and a vector is a k − 1-vector.
– The interior product throws away the orthogonal parts.
None of them are invertible. What if we combined them, though? Then we ought to have
both pieces of information (the orthogonal and parallel part) we need for invertibility.
For two vectors a and b, we define the geometric product:
Equation 1.2

Geometric product between vectors
ab = a · b + a ∧ b

(1.33)
π

Warning 1.3
This definition is only valid for the product between two vectors - or more generally,
for products between a vector and a k-vector, k ≥ 1.
The geometric product between a scalar and a k-vector is just the normal scalar
multiplication.
!
This definition is the sum of a scalar and a bivector. You are probably wondering
how that is possible - how can we sum together two completely different things? The
answer is that we just do it without evaluating the sum. Think of complex numbers
- real and imaginary numbers are two completely different things, and yet we just sum
them together. In geometric algebra, we will be constantly summing k-vectors of different
grades together. A sum of k-vectors of different grades is called a multivector1 .
As we shall soon see, this geometric product is both associative and invertible. For
now, let us calculate a few examples. For instance, let a = e1 and b = e1 + e2 . Then the
geometric product between them is
ab = e1 · (e1 + e2 ) + e1 ∧ (e1 + e2 )
= 1 + e1 ∧ e2 ,

(1.34)

a sum of a scalar and a bivector. We can use grade diagrams like this one to depict the
geometric product:
1

The mathematician’s way of saying this is that the space of multivectors is the direct sum of all the
spaces of k-vectors from k = 0 to k = ∞.

19

## PDF page 21

3
2

∧b

bivector a ∧ b

·b

scalar a · b

1 vector a
0
a

ab

We can apply the geometric product to more than two vectors. For instance,
abc

(1.35)

is a perfectly valid expression - the geometric product is associative, so we can drop the
parentheses. It decomposes into four terms:
abc = (a · b)c + (a ∧ b)c
= (a · b)c + (a ∧ b) · c + (a ∧ b) ∧ c.

(1.36)

The first term is just a scalar multiplied with a vector, as we know it from standard vector
algebra. The second term is the interior product between a bivector and a vector - this
lowers the grade of the bivector by 1, resulting in a vector. The last term is the exterior
product between a bivector and a vector, resulting in a trivector.

3
2
1
0
a

ab

abc

Therefore, the expression abc results in the sum of a vector and a trivector.

1.3.1

Grade projection

We can extract the real and imaginary parts of a complex numbers with the functions
Re(z) and Im(z). Similarly, given some arbitrary multivector M , we can extract the k-th
grade component by using the so-called grade projection
⟨M ⟩k .
20

(1.37)

## PDF page 22

For instance, the bivector part of M would be written ⟨M ⟩2 . Applied to the previous
example, it yields
⟨ab⟩2 = ⟨1 + e1 ∧ e2 ⟩2 = e1 ∧ e2 .
(1.38)
Its scalar part is:
⟨ab⟩0 = ⟨1 + e1 ∧ e2 ⟩2 = 1.

(1.39)

We will also often drop the subscript to denote the scalar part, i.e.
⟨M ⟩ := ⟨M ⟩0 .

1.3.2

(1.40)

Anticommutation relations

When the two vectors are orthogonal to each other, the interior product between them is
zero. In such cases, the geometric product reduces to the scalar product:
ei ej = ei ∧ ej

for all i ̸= j.

(1.41)

Therefore, in such cases, the geometric product is anticommutative:
ei ej = −ej ei

for all i ̸= j.

(1.42)

Therefore, basis k-vectors like e1 ∧ e2 ∧ e3 can be equally written with the geometric
product, e1 e2 e3 . We can abbreviate this even further - to avoid having to write e’s all the
time in products like e1 e2 e3 , we just write e123 .
If the two vector operands of the geometric product are equal to each other, the exterior
product is zero and only the interior product remains. In such a case, the geometric
product is equal to the magnitude squared of the vector:
vv = v2 = v · v + v ∧ v
=v·v
= |v|2

(1.43)

Using the anticommutator brackets
{A, B} = AB + BA,

(1.44)

We can also denote these relations more succinctly as
{ei , ej } = 2δ ij

(1.45)

where δ ij is the metric of our space - in the Euclidean case, just the Kronecker delta.
Tangent 1.2
In fact, this relation is where mathematicians start when investigating Clifford
algebras - they postulate this anticommutation relation and then derive all the
continues in the next page
21

## PDF page 23

continues from the previous page
other properties of geometric algebras from it. Obviously, we are not going to do
that - we don’t want mathematical rigour, but physical intuition.
ç

3
2
1
0
ei

ei ej , i ̸= j

ei

ei ei

3
2
1
0

Figure 1.2: The grade diagram for the anticommutation relation {ei , ej } = 2δ ij .

1.3.3

Higher grades

The most prominent advantage of the geometric product is that it is associative. So far,
we’ve just been taking geometric products between vectors. However, we can just as
well take the geometric product between arbitrary k-vectors. For instance, let B be the
bivector
B = e1 ∧ e2 = e1 e2 = e12 .
(1.46)
Then, for another vector v = e1 + e3 , we can write down the geometric product
Bv.
Let’s draw a grade diagram:

22

(1.47)

## PDF page 24

3
2
1
0
Before even evaluating it, we can tell that this product will consist of a vector and
trivector part. Let’s test this:
Bv = e12 (e1 + e3 )
= e12 e1 + e12 e3
= e121 + e123
(1.48)
= −e112 + e123
= −e2 + e123 ,
a vector and a trivector. In general, we can calculate every geometric product between
arbitrary multivectors by resolving the multivectors into products of vectors and then
writing them out.
Let’s try another example: Let C = e12 + e23 and D = e34 + e13 be two bivectors.
Multiplying by a bivector is the same as consecutively multiplying by its constituent
vectors. The grade diagram for the geometric product CD is:

4
3
2
1
0
C

D

We see that the result will be the sum of a scalar, a bivector and a tetravector. In
fact,
CD = (e12 + e23 )(e34 + e12 )
= e12 e34 + e23 e34 + e12 e12 + e23 e12
= e1234 + e24 − e1221 − e2321
(1.49)
= e1234 + e24 − e11 + e2231
= e1234 + e24 − 1 + e31
= −1 + e24 + e31 + e1234 .
23

## PDF page 25

We see that this is the sum of a scalar
⟨CD⟩ = −1,

(1.50)

⟨CD⟩2 = e24 + e31 ,

(1.51)

⟨CD⟩4 = e1234 .

(1.52)

a bivector
and a tetravector

1.3.4

Invertibility

We call a vector n a unit vector if it squares to 1 with the geometric product:
n2 = nn = n · n = 1.

(1.53)

We are all used to reading this with respect to the scalar product - but the geometric
product is more powerful than that. Most importantly, it is associative. If we multiply n
onto an arbitrary multivector M ,
M n,
(1.54)
we can reverse this operation by multiplying n on top of it again:
(M n)n = M nn = M (nn) = M.

(1.55)

Therefore, we can define the vector inverse for unit vectors:
n−1 = n,

(1.56)

or for arbitrary vectors a:

a
.
a2
We can see that this is an inverse of a by calculating:
a−1 =

a
a2
aa−1 = a 2 = 2 = 1
a
a

(1.57)

(1.58)

This is the true power of the geometric product - we can form the inverse and hence
divide by vectors.
We can even form inverses for higher-grade k-vectors. For instance, the bivector e12
squares to:
(e12 )2 = e12 e12 = e1212 = −e1221 = −e11 = −1.
(1.59)
Therefore, its inverse is (e12 )−1 = −e12 .

24

## PDF page 26

1.3.5

Interior and exterior product revisited

Previously, we defined the interior and exterior product for k-vectors of arbitrary grade
and then combined them to form the geometric product. However, we can also do this
the other way around. For a k-vector X and an l-vector Y with k ≥ l, we define:
• The interior product X · Y is the lowest possible grade achievable by the geometric
product XY :
X · Y = ⟨XY ⟩k−l
(1.60)
• The exterior product X ∧Y is the highest possible grade achievable by the geometric
product XY :
X ∧ Y = ⟨XY ⟩k+l
(1.61)
For instance, for two vectors a, b, we’d define:
a · b = ⟨ab⟩
a ∧ b = ⟨ab⟩2 .

(1.62)

For a bivector B and a vector a, we’d define:
B · a = ⟨Ba⟩1
B ∧ a = ⟨Ba⟩3 .

(1.63)

These definitions provide us with a much easier way to evaluate the interior product:
Instead of shuffling around the order of the basis k-vectors and then rearranging the
parentheses, we can just calculate the geometric product between them and then pick out
the k − l grade.
There is also another way: We look at whether the grade operations are commutative
or anticommutative. We already know that for two vectors a and b, the inner product
commutes:
a · b = b · a,
(1.64)
and the wedge product anticommutes:
a ∧ b = −b ∧ a.

(1.65)

Therefore, we can tell that for two vectors:
1
a · b = (ab + ba)
2
1
a ∧ b = (ab − ba).
2
Relations of this type are going to be very useful in the future.

25

(1.66)

## PDF page 27

1.4

The two-dimensional geometric algebra Cl(2)

A geometric algebra is the algebra of multivectors with the geometric product as its
operation. We can build a geometric algebra by specifying its basis vectors and their
squares. For instance, the three-dimensional euclidean geometric algebra is built from
the basis vectors e1 , e2 , e3 that all square to 1,
(e1 )2 = (e2 )2 = (e3 )2 = 1.

(1.67)

We denote a geometric algebra with p + q basis vectors of which p square to 1 and q
square to -1 as Cl(p, q). If all the basis vectors square to 1, the space is euclidean and
we denote its geometric algebra as Cl(p). If there are also vectors that square to −1, the
space is hyperbolic. A prominent example of such a space is spacetime from special
relativity, with one vector that squares to 1 and three others that square to −1. The
spacetime algebra is denoted as Cl(1, 3).
But for now, we are going to treat a much easier example: The two-dimensional
geometric algebra Cl(2). It has two basis vectors:
e1 , e2 .

(1.68)

The only higher-grade k-vector we can construct from these vectors is the bivector
e1 2. Therefore, we only have four basis k-vectors:
• one scalar 1
• two vectors e1 , e2
• one bivector e12 .
This makes the 2D geometric algebra Cl(2) particularly simple. In mathematical language, we can write this as:
Cl(2) = span{1, e1 , e2 , e12 }

(1.69)

In the following, we are going to examine its properties.

1.4.1

The even subalgebra Cl+ (2) and complex numbers

The even subalgebra Cl+ (p, q) of some geometric algebra Cl(p, q) is defined as the subalgebra that only contains k-vectors of even grade. For instance, the even subalgebra
Cl+ (2) is composed only of the scalar and the bivector. Thus, any element z ∈ Cl+ (2)
can be written as
z = a + be12 .
(1.70)
The unit bivector e12 squares to −1:
(e12 )2 = e1212 = −e1221 = −e11 = −1.
26

(1.71)

## PDF page 28

This is familiar to us - these elements z look just like complex numbers! Complex
numbers are composed of scalars and “imaginary units”,
z = a + bi

(1.72)

i2 = −1.

(1.73)

where i squares to −1:
All complex numbers commute with each other. At first glance, it looks like this nice
analogy between C and Cl+ (2) could fall apart because of that - after all, we have seen
that the geometric product is not necessarily commutative. But in fact, we realize that:
• Scalars commute with themselves and with bivectors.
• The bivectors e12 commutes with itself and scalar multiples of itself.
In other words: All elements of Cl+ (2) commute with each other. This means that we can
in fact translate any complex number z = a+bi to an even multivector z = a+be12 and do
the exact same calculations with them. And we finally get a geometric interpretation for
imaginary numbers - the imaginary unit i can be interpreted as the bivector e12 . Complex
numbers can be interpreted as a sum of a scalar and a bivector.
We can do anything with even multivectors z. The analogue of complex conjugation
is the multivector reverse M̃ . It reverses the order of all geometric products in the
expression, but leaves it untouched otherwise:
Equation 1.3

Multivector reverse
1̃ = 1
e˜i = ei
e˜
ij = eji = −eij
e˜
ijk = ekji = −eijk
e˜
ijkl = elkji = −eijkl
···

(1.74)

π
If we apply the reverse operation on the even multivector z = a + be12 , we get:
z̃ = a + be21 = a − be12 .

(1.75)

This is exactly what we’d expect from the complex conjugate.
We can take the exponential of an imaginary number:
exp(iα) = cos(α) + i sin(α).

(1.76)

This works out because the series expansion of the exponential,
exp(iα) =

∞
∑
(iα)k
k=0

27

k!

(1.77)

## PDF page 29

splits into two parts: The even ones that are real-valued because i2n = (−1)n , and the
odd ones that are imaginary-values because i2n+1 = (−1)n i:
)
(∞
)
(∞
∑ (−1)l α2l+1
∑ (−1)l α2l
+i
(1.78)
exp(iα) =
(2l)!
(2l
+
1)!
l=0
l=0
These are the respecive series expansions for cos(α) and sin(α). And we can do exactly
the same for the bivector exponential
Equation 1.4

Bivector exponential
exp(e12 α) = cos(α) + e12 sin(α).

(1.79)
π

This bivector exponetial follows the exact same rules as the normal complex exponential:
˜
exp(e
12 α) = exp(−e12 α)
(1.80)
exp(e12 α) + exp(e12 β) = exp(e12 (α + β))

1.4.2

Two-dimensional rotations

One of the primary uses of complex numbers in physics is to encode rotations through
the complex plane. For instance, we might write down the formula
x(t) = x0 eiωt
with

(
x0 =

)
1
−i

(1.81)

(1.82)

to encode two-dimensional rotational motion with the angular frequency ω. The resulting
expression would then be
(
)
cos(ωt) + i sin(ωt)
x(t) =
.
(1.83)
sin(ωt) − i cos(ωt)
This way of writing down oscillations is pretty ubiquitous in theoretical physics. When
we do this, there is an implicit convention to only interpret the real part as something
physical and to throw the imaginary part away. Therefore, we actually ought to write
(
)
cos(ωt)
x(t) =
.
(1.84)
sin(ωt)
But what is the imaginary part, then? It is a mathematical artifact to make our calculations somewhat easier. We’ve all gotten used to it by now, but wouldn’t it be better if
we found a way to encode rotations without having to resort to unphysical mathematical
parts at all?
28

## PDF page 30

Luckily, the C ≃ Cl+ (2) isomorphism provides us with the right tool we need to
eliminate these unphysical imaginary parts. Let v = xe1 + ye2 be a 2D vector. We can
rotate it by a quarter-turn by writing
v′ = ve12 .

(1.85)

We can show this by rotating the basis vectors
e1 e12 = e2
e2 e12 = −e1 .

(1.86)

Note that in contrast to complex numbers, this multiplication is not commutative!
As you can check for yourself,
ve12 = −e12 v.
(1.87)
for all v.
If we rotate by e12 two times, we get the original vector times −1.
ve12 e12 = −v

(1.88)

u⊥
u

u⊥
e12

e12

u

u

e12

−u
Figure 1.3: Applying the unit bivector e12 flips the vector u by a quarter-turn, τ4 radians.
Two quarter-turns are equal to a sign flip u → −u. This means that we can interpret
the bivector e12 as a square root of −1.
We can also use the bivector exponential for this - if we want to rotate the 2D vector
v by α degrees in the positive sense, we write:
Equation 1.5

2D rotations of vectors
v′ = v exp(e12 α).

(1.89)
π

Again, keep in mind that we have to pay attention to the order - if we were to apply
the bivector exponential from the other side, the vector would be rotated in the negative
sense.
29

## PDF page 31

This approach has the advantage that contrary to complex numbers, it distinguishes
between vectors and the objects rotating the vectors. This confusion ultimately is what
led to the aforementioned problem with unphysical imaginary parts.
Also, the bivector e12 α is our first example of a so-called rotation bivector - a
bivector whose orientation defines the plane we are rotating along, and whose magnitude
defines the angle of the rotation. In two dimensions, there is only one possible plane we
can rotate along, so all 2D rotation bivectors can be written e12 α. In three dimensions,
however, this will be more interesting, as we will see in the following chapter.
Warning 1.4
This rotation formula works only for vectors, and only in two dimensions. In the
next chapter, we are going to learn about rotors and the rotor transformation law
- they work for arbitrary multivectors and arbitrary dimensions.
!

30

## PDF page 32

Chapter 2
Geometric algebra of space
Chapter summary
• The geometric algebra of space Cl(3) describes objects in three-dimensional space.
• There is only one trivector in 3D: e123 . We call it the pseudoscalar.
• Every axial vector corresponds to a bivector. We call bivectors pseudovectors.
• The cross product has several undesirable properties. We can fully replace it with
the wedge product and bivectors.
• We can perform 3D rotations by sandwiching two reflections. The resulting objects
performing the rotation are called rotors.
• Rotation bivectors describe the plane and angle of a rotation. Rotors are formed
by exponentiating rotation bivectors.
• Quaternions are left-handed 3D bivectors.
• We can perform infinitesimal rotations with the commutator brackets.

2.1

Overview

The geometric algebra of space Cl(3) is the geometric algebra describing threedimensional space. Its vector basis consists of the three unit vectors
e1 , e 2 , e 3 .
This gives us the following possible basis k-vectors:
• 1 scalar
• 3 vectors e1 , e2 , e3
31

(2.1)

## PDF page 33

• 3 bivectors e12 , e23 , e31 ,
• 1 trivector e123 .

1
e1

e2

e3

e23

e31

e12

e123
Figure 2.1: The multivector pyramid of the space algebra.

2.1.1

3D pseudoscalars

Now that we have three dimensions instead of two, the maximum grade of our algebra is
3 - we get trivectors like e123 . They represent volume elements. There is only one possible
orientation for trivectors, so every trivector we can write down will be proportional to
e123 . For this reason, 3D trivectors are called pseudoscalars. We define the 3D unit
pseudoscalar
I = e123 .
(2.2)
The exact order 123 is a matter of convention - we could’ve also defined I ′ = e132 − I to
be the unit pseudoscalar. By choosing either I or −I, we choose an orientation for our
space - conventionally, we use right-handed coordinates, so we choose I. A left-handed
space would have −I as its unit pseudoscalar.
Just like in two dimensions, the unit pseudoscalar I squares to −1:
I 2 = e2123
= e123123
= e112323
= e2323
= −e2233
= −e33
= −1.

32

(2.3)

## PDF page 34

·

=

Figure 2.2: The equation Ie3 = e12 visualized.
The 3D pseudoscalar trivially commutes with scalars and with itself, but also with vectors
and bivectors:
ei I = Iei
(2.4)
eij I = Ieij
We have seen how to replace complex numbers with the even subalgebra of Cl(2).
This works just as well with the scalar-pseudoscalar subalgebra Cl1,I (3) of the geometric
algebra of space - that is, the subalgebra composed only of elements of the form
z = a + be123 = a + bI.

(2.5)

It largely depends on the context which one of these replacements is better suited. If we
want to replace complex numbers with no geometric meaning, for instance in the context
of complex analysis, we often choose the Cl(2) scalar-pseudoscalar method. However,
in other fields, complex numbers do carry geometric significance - for instance, in electromagnetism, we will replace the imaginary unit with the four-dimensional spacetime
pseudoscalar.
The next thing we notice when taking a look at the multivector pyramid (Figure 2.1)
is that there are just as many bivectors as vectors now. In two dimensions, there was
only one possible orientation for an area element, but now, there are three - we can write
an arbitrary bivector B as the linear combination
B = ae12 + be23 + ce31 .

(2.6)

This means that there is a one-to-one correspondence between vectors v and bivectors
B - for every vector v = v i ei , there is a corresponding bivector B = Iv. For instance, the
bivector corresponding to the vector e3 would be
Ie3 = e123 e3 = e12 .

(2.7)

The bivector Iv describes the area orthogonal to the vector e3 (see Figure 2.2). If we
want to obtain the original vector from the bivector, we simply premultiply by I −1 = −I:
I −1 e12 = −Ie12 = −e123 e12 = −e11232 = −e232 = e223 = e3 ,

(2.8)

or, more generally:
−IB = −I(Iv) = v.

(2.9)

One might therefore ask why we need 3D bivectors at all, if the information of a
bivector can also be encoded in a vector. In fact, this is the stance that most physicists
33

## PDF page 35

e3
e2

e′3

reflection
e′1

e1

e′2

L=x×p

IL = x ∧ p

Figure 2.3: The behaviour of angular momentum under reflections. Evidently, it makes
much more sense to use bivectors instead of axial vectors to describe rotational motion.
implicitly take - in traditional vector algebra, areas are always described by their normal
vectors. However, there is one important caveat here: Strictly speaking, 3D bivectors
do not correspond to vectors - they correspond to axial vectors1 . Axial vectors normally
behave like normal vectors, but once reflections and parity flips are involved, things get
messy.
For instance, the angular momentum axial vector L = x × p describes the circular
motion of a rotating object. In order to find out which direction of rotation a given
L describes, we use the right-hand rule: We point the thumb of our right hand in the
direction of L and form a fist with the four other fingers.
Now, imagine that the whole scene is being reflected in a mirror parallel to the axis
of rotation. While the plane of rotation described by the bivector IL = x ∧ p behaves as
we’d expect under this reflection, but the axial vector L = x × p includes an extra sign
flip. Figure 2.3 shows this for the example IL = Le12 .
1

In traditional math, the terms “axial vector” and “pseudovector” are used synonymously. We call
vectors that perform an extra sign flip under a reflection or parity flip “axial vectors”, and bivectors
“pseudovectors”.

34

## PDF page 36

In mathematical terms, axial vectors are defined via their behaviour under parity flips.
A parity flip P is the operation that flips the sign of all vectors:
Equation 2.1

Parity flip
P (x) = −x

(2.10)
π

If we combine this parity flip with a rotation by 180◦ , we get a reflection as shown
in Figure 2.3. Axial vectors c, however, do not flip their sign under parity transforms.
They just stay the same - which makes no sense at all, if you ask me. Hence, in geometric
algebra, we generally banish all axial vectors like L in favour of bivectors like IL = IL. For
this reason, we also refer to 3D bivectors as pseudovectors. The reason why bivectors
do not flip their sign under P is very intuitive P (a ∧ b) = P (a) ∧ P (b)
= (−a) ∧ (−b)
= a ∧ b.

(2.11)

On the other hand, the pseudoscalar I will flip its sign:
P (I) = P (e1 ∧ e2 ∧ e3 )
= P (e1 ) ∧ P (e2 ) ∧ P (e3 )
= (−e1 ) ∧ (−e2 ) ∧ (−e3 )
= −e1 ∧ e2 ∧ e3
= −I.

(2.12)

In other words - after a parity flip, our space goes from right-handed (I) to left-handed
(−I).

2.1.2

Eliminating the cross product

Now that we have vowed to drive out all axial vectors of physics, the next logical step
is to banish the cross product - the appearance of axial vectors in the cross product is
unavoidable. In Figure 2.3, we have seen that
vector × vector = axial vector.

(2.13)

axial vector × vector = vector
vector × axial vector = vector
axial vector × axial vector = axial vector.

(2.14)

We can deduce that

35

## PDF page 37

The cross product between two regular vectors a × b gives us the axial vector normal
to the plane spanned by a and b. In geometric algebra language, this means that we
want to find the vector orthogonal to the bivector a ∧ b:
a × b = −I(a ∧ b).

(2.15)

But since we have decided that we want to replace all axial vectors v with their
bivector counterparts, we are going to write:
Equation 2.2

Cross product between two vectors
a ∧ b = I(a × b).

(2.16)
π

But what if one operand of the cross product is an axial vector c = IC? In that case,
we have to rewrite the cross product in terms of the bivector C, such that it becomes::
b=a×c
= −I(a ∧ c)
= −I(a ∧ (IC))
1
= − I(aIC − ICa)
2
1
= − I(IaC − ICa)
2
1
= (aC − Ca)
2
= a · C.

(2.17)

The cross product between a vector and an axial vector translates to the interior product
between a vector and the bivector corresponding to the cross product.
Equation 2.3

Cross product between a vector and an axial vector
a×c=a·C

(2.18)
π

Similarly,
c × a = C · a = −a · C

36

(2.19)

## PDF page 38

When we cross-multiply two axial vectors c = IC, d = ID, we get the axial vector:
c × d = −I(c ∧ d)
1
= − I((IC) ∧ (ID))
2
1
= − I(ICID − IDIC)
2
1
= − I(I 2 CD − I 2 DC)
2
1
= I(CD − DC),
2

(2.20)

which corresponds to the bivector
Equation 2.4

Cross product between two axial vectors
1
I(c × d) = (DC − CD) = ⟨DC⟩2
2

(2.21)
π

One can geometrically imagine this product as follows: In 3D space, two bivectors will
always intersect along a line. The line can be defined by a unit vector n. This means that
C and D can be described as the wedge between n and some other vectors x, y orthogonal
to n:
C = xn
(2.22)
D = yn
The product ⟨DC⟩2 can be described as:
⟨DC⟩2 = ⟨ynxn⟩2
= − ⟨ynnx⟩2
= − ⟨yx⟩2
= x ∧ y.

(2.23)

These substitution rules allow us to fully eliminate the cross product from physics - and
we will do so in GA. The widespread adoption of the concepts of axial vectors and the
cross product was a grave mistake we intend to correct. This becomes particularly obvious
in the field of electromagnetism.

2.2

Transformations

One of the main applications of the cross product is the mathematical description of
rotational movement. Therefore, we are now going to investiage how to describe rotations.
The outline of this section is as follows: First, we will define the projection and
rejection operations. Then, we will use them to define the reflection operation, which
we will in turn use to define rotations and rotors.
37

## PDF page 39

Rejn (a)
a

n
Projn (a)

Figure 2.4: The projection and rejection of a vector a with respect to n

2.2.1

Projection and rejection

Let a be some vector and n a normal vector, n2 = 1. We can decompose a into a parallel
and orthogonal part with respect to n by writing:
a = an2
= ann
= (a · n + a ∧ n)n
= (a · n)n + (a ∧ n)n

(2.24)

The interior product a · n measures how much a and n coincide, such that (a · n)n is the
projection of a onto the line defined by n. Similarly, a ∧ n measures the “orthogonality”
of a with respect to n, such that (a ∧ n)n is the part of a that is orthogonal to n. This is
depicted in Figure 2.4. We call the former the projection and the latter the rejection
and denote them as
Equation 2.5

Projection and rejection
Projn (a) = (a · n)n
Rejn (a) = (a ∧ n)n.

(2.25)
π

2.2.2

Reflections

We now turn to the description of reflections by a mirror plane, like the one we have
performed in Figure 2.3. We know this type of reflection from everyday life - it’s what we
see when we look in the mirror. This is why we are used to think about it as a reflection
“by a mirror plane”. But let’s take a look at what actually happens with the vector
coordinates when we perform this reflection, for instance by the y-z plane:
x = (x1 , x2 , x3 ) → (−x1 , x2 , x3 ).

(2.26)

Only the sign of the component of e1 is flipped, while the two components associated with
the plane we were reflecting by are unchanged. That seems a bit odd. In fact, it turns out
that describing these reflections gets a lot easier if we do not think of them as reflections
by a plane, but as reflections along the normal vector of the plane. For instance, we will
now think about (2.26) as a reflection along the x-axis.
38

## PDF page 40

n

m
a
θ
2

a′′

θ

a′
Figure 2.5: A rotation along an angle of θ can be performed by performing a double
reflection along n and m. The angle between these two vectors has to be θ/2.
Let n be the normal vector of the plane of reflection, and a the vector we want to
reflect along n. Using the language of the previous section, we can split up a as follows:
a = Projn (a) + Rejn (a)

(2.27)

If we now want to reflect a along n, we simply flip the sign of the projection:
a′ = −Projn (a) + Rejn (a)

(2.28)

Inserting the respective definitions, we get
a′ = −(a · n)n + (a ∧ n)n
= (−a · n + a ∧ n)n
= (−n · a − n ∧ a)n
= −nan.

(2.29)

This is the formula for reflections along a vector.
Equation 2.6

Reflection of a vector along a vector
a′ = −nan

(2.30)
π

In fact, it works very similarly for higher grades, and not just for vectors. For instance,
a bivector B = ab would reflect like
B ′ = a′ b′ = (−nan)(−nbn) = nannbn = nabn = nBn.

2.2.3

(2.31)

Rotations

Now, we want to describe rotations. The first thing to realize is that every rotation can
be decomposed into two successive reflections.
39

## PDF page 41

Two successive reflection along the same axis n do nothing to a vector a:
a′′ = −na′ n = −n(−nan)n
= n2 an2
= a.

(2.32)

However, if we first reflect along n, and then along another unit vector m, we get:
a′ = −nan
a′′ = −ma′ m
= mnanm.

(2.33)

A single reflection is an orthonormal transformation i.e. an element of the group O(3). It
has determinant −1. Two successive reflections, however, have determinant (−1)2 = 1 they are special orthogonal transformations in SO(3). Special orthogonal transformations
in 3D are always rotations.
Taking a look at Figure 2.5, we can see that this double reflection is indeed a rotation.
To be specific, it is a rotation along the plane defined by the bivector n ∧ m. The angle
a is rotated by twice the angle between n and m. To make our life easier, we are going
to define the so-called rotor
Equation 2.7

Constructing rotors from vectors
R = nm,

(2.34)
π

that describes this rotation. Then, the formula for a rotation is:
Equation 2.8

Rotor law
a′′ = R̃aR.

(2.35)
π

The tilde R̃ denotes the multivector reverse.
Analogously to the 2D case, we know that the interior and exterior products nm are
equal to:
n · m = cos(θ/2)
(2.36)
n ∧ m = sin(θ/2)B
where

n∧m
B=√
−(n ∧ m)2

(2.37)

is the unit bivector along which the rotation is performed. We can therefore say that
R = cos(θ/2) + B sin(θ/2).
40

(2.38)

## PDF page 42

This should look vaguely familiar - it looks a bit like the formula for complex exponentials,
exp(iθ/2) = cos(θ/2) + i sin(θ/2).

(2.39)

This formula arises because the polynomial expansion for the exponential splits up into
a real and an imaginary part:
exp(iθ/2) =

∞ k
∑
i (θ/2)k
k=0
∞ 2l
∑

k!

∞
i (θ/2)2l ∑ i2l+1 (θ/2)2l+1
+
=
(2l!)
(2l + 1)!
l=0
l=0

=

∞
∑
(−1)l (θ/2)2l
l=0

(2l!)

+i

(2.40)

∞
∑
(−1)l (θ/2)2l
l=0

(2l + 1)!

= cos(θ/2) + i sin(θ/2).
This derivation relied on the fact that i2 = −1. And we will in fact see that all 3D unit
bivectors square to -1 too! For instance, B = e31 describes the rotation along the zx
plane:
(e31 )2 = e3131 = −e3311 = −1
(2.41)
So we can write:
R = exp(Bθ/2) = cos(θ/2) + B sin(θ/2),

(2.42)

the rotor that performs a rotation along the zx plane by an angle of θ.
This is an extremely useful fact. Given a rotation bivector Θ (capital theta) whose
orientation describes the plane of rotation and whose magnitude describes the angle of
rotation, we can simply find the corresponding rotor by calculating:
Equation 2.9

Constructing rotors from bivector exponentials
R = exp(Θ/2).

(2.43)
π

Both conceptually and practically, this is a lot simpler than the Euler angle approach
we had to take for rotation matrices. For instance, it doesn’t suffer from gimbal locking.
There is also an added benefit from using bivectors to describe rotations: In classical
vector algebra, we use so-called “Euler” or “rotation vectors” to describe the axis and
angle of the rotation we want to perform. For instance, a counterclockwise rotation
around the z axis by a quarter-turn would correspond to the rotation “vector”
τ
θ = e3 .
(2.44)
4
It suffers from the same problems as other axial vectors. We will thus instead use rotation
bivectors Θ = Iθ. The above rotation would be represented by the bivector
τ
Θ = e12 .
(2.45)
4
41

## PDF page 43

Thus, in geometric algebra, we do not talk about rotations “around an axis”, but rather
about “rotations along a plane” - for instance, a rotation along the xy plane.

2.2.4

Some facts about rotors

Given a rotor R = exp(Θ/2), the reverse operation evaluates to
R̃ = exp(−Θ/2).

(2.46)

We can thus directly see that for any rotor,
RR̃ = R̃R = 1.

(2.47)

The rotor law M → RM R̃ is valid for any multivector grade. For instance, a bivector
D = ab would rotate like
D′ = a′ b′ = R̃aRR̃bR = R̃abR = R̃DR.

(2.48)

If we want to perform two successive rotations R1 , R2 , we just multiply the two rotors
together:
Rtotal = R1 R2 .
(2.49)
There is something important to note: Given a specific rotation R, the rotor R′ = −R
has the exact same effect on vectors:
(−R̃)x(−R) = R̃xR.

(2.50)

To understand this better, we take a look at the simplest pair of rotors where this peculiarity arises - R = +1 and R′ = −1. Obviously, R = 1 corresponds to a rotation by an
angle of zero, exp(0) = 1. The second rotor, R′ = −1 however, corresponds to a rotation
by τ = 360◦ :
)
(
B
′
τ = cos(τ /2) + B sin(τ /2)
R = exp
2
(2.51)
= −1.
If we were to rotate by 2τ = 720◦ , we would obtain the original rotor again:
(
)
B
exp
2τ = cos(2τ /2) + B sin(2τ /2)
2
= 1.

(2.52)

This is a very interesting fact - in the rotor formalism, a rotation by 0◦ is not the same as
a rotation by 360◦ . They correspond to two different rotors, but because of the geometric
two-sided transformation law, they have the same effect on vectors. This is not some weird
mathematical artifact of geometric algebra. It corresponds to an elementary geometric
fact about rotations: The 3D group of rotations SO(3) is not simply connected. This
means that if we trace out a path starting and ending at the same rotational state, it’s
not guaranteed that we will be able to smoothly deform this path into a point.

42

## PDF page 44

Tangent 2.1
To elaborate on this, imagine a three-dimensional sphere S 2 . If we draw a loop on
its surface, we can always continuously shrink it into a point. On a 3D torus T 3 ,
however, this is not always possible - if the loop makes one turn around the torus,
we cannot deform it into a point without tearing it apart. We say that S 2 is simply
connected, but T 3 isn’t.
Doing the same thought experiment for elements of SO(3) - 9-dimensional matrices
with some constraints - can be pretty difficult. Luckily, there is a trick devised
by Paul Dirac to visualize this very intuitively - the so-called Dirac belt trick. In
this trick, we use a belt to visualize a path we might take through SO(3). The
two ends of the belt represent the start and end of our path through SO(3). The
cross-section of the belt at any point can be pictured as a vector that represents
the current state of rotation. If the orientation of both ends is the same, the belt
describes a loop through SO(3). If the belt is just a straight line without twists,
it describes a point in SO(3). Continuous deformations amount to shifting and
twisting the belt around, while keeping the orientation of both ends fixed. You can
check for yourself that if there is one τ twist in the belt, it is not possible to deform
it back into a straight line with these costraints - but if there are two τ twists in
the belts, it is possible.
ç

2.2.5

A short note on quaternions

Quaternions are the go-to solution of many physicists and engineers to describe rotations
without gimbal locking. They are an associative algebra of three complex numbers i, j, k
satisfying
i2 = j 2 = k 2 = ijk = −1.
(2.53)
They are something rather abstract normally, but with geometric algebra, they just translate to the unit bivectors:
i = e12
j = e23
(2.54)
k = −e31 .
Therefore, rotors can be formulated in quaternion algebra too. (In quaternion lingo,
rotors are called “versors”).
The even subalgebra Cl+ (3) only contains scalars and bivectors. Therefore, the even
subalgebra of Cl(3) is isomorphic to the space of quaternions H - we can translate any
quaternion
z = a + bi + cj + dk
(2.55)
to an element of the even subalgebra:
z = a + be12 + ce23 − de31 .

(2.56)

This is starting to look a lot like the isomorphism between complex numbers and the even
subalgebra Cl+ (2). In two dimensions, we had one possible rotation and one bivector (e12 )
43

## PDF page 45

that generated it. This bivector could be translated to the imaginary unit i. Now, in three
dimensions, we have three rotations and three bivectors generating them (e12 , e23 , e31 ).
They can be translated to the unit quaternions i, j, −k 2 .
However, both the complex numbers and the quaternions share the same issues: Neither has a concept of “vectors” in the proper sense. The object performing the rotation
(the rotor, or “versor” in quaternion lingo) consists of the same basis elements as the
object being rotated. This is very confusing, and it doesn’t help that the quaternions
themselves do not have any geometric interpretations. Instead, authors often resort to
projective geometry black magic to explain them, and as a result, no one really understands quaternions. Luckily, we can now see that they are just bivectors, and get a
geometric intuition for them!
Also, you might have asked yourself why k translates to −e31 instead of e31 . This
is because the definition ijk = −1 is wrong - it should have been ijk = 1. The former
definition results in a left-handed space. These peculiarities smash all hopes of doing any
halfway sensible geometry with quaternions. So let’s turn our back on them and just use
vectors and bivectors instead.

2.2.6

Infinitesimal rotations

We now investigate infinitesimal rotations - rotations whose angle very small, such that
we can neglect second-order terms.
Let Θ be a rotation bivector. Its angle should be much smaller than one - |Θ| ≪ 1.
We can then approximate the bivector exponential as
R = exp(Θ/2) ≈ 1 + Θ/2.

(2.57)

This means that the infinitesimal rotor transformation law is
M ′ = R̃M R = (1 − Θ/2)M (1 + Θ/2)
Θ Θ
≈M +M − M
[ 2 ]2
Θ
= M + M,
2

(2.58)

This is the infinitesimal rotor transformation law for a multivector,
Equation 2.10

Infinitesimal rotor transformation law
[
]
Θ
R̃M R ≈ M + M,
2

(2.59)
π

2

In fact, this is how Quaternions originally arose - Hamilton was asking himself how the rotation math
of complex numbers could be generalized to three dimensions.

44

## PDF page 46

If M is a vector, M = x, this commutator can also be expressed as:
]
[
1
Θ
= (xΘ − Θx) = x · Θ.
x,
2
2

(2.60)

We are going to use the commutator notation [x, B/2] when we want to emphasize that
we are dealing with an infinitesimal rotation - it is independent of the grade of the object
being rotated. For instance, if we wanted to rotate a bivector C, we can equivalently
write
[
]
Θ
′
C = C + C,
.
(2.61)
2
The translation of this commutator would be:
[
]
Θ
C,
= ⟨CΘ⟩2 ,
2

(2.62)

the bivector grade of the geometric product CΘ. Draw a grade diagram - you will see
that the geometric product between two bivectors will result in a scalar, bivector and
tetravector grade. We use the interior product C · Θ to get the scalar grade and the
exterior product C ∧ Θ to get the tetravector grade. We don’t have any shorthand
notation for the bivector grade though, so we have to write ⟨CΘ⟩2 .
The dot notation x · Θ for rotating vectors is primarily useful when we want to think
about the geometric details - from our geometric intuition, we can directly tell that:
• The value of x · Θ is maximal if x fully lies in the plane of Θ. This makes intuitive
sense - a vector will change fastest if it lies in the plane of rotation.
• The value of x · Θ is zero if x is orthogonal to the plane of Θ. This also makes
intuitive sense - x will not change at all under the rotation if if is orthogonal to the
plane of rotation.
In the language of commutation relations, we say that:
• If x lies in the plane of Θ, then x and Θ anticommute:
xΘ = −Θx

(2.63)

• If x is orthogonal to the plane of Θ, then x and Θ commute:
xΘ = Θx

(2.64)

This means that the bivector exponential R = exp(Θ/2) will behave as follows: If x
lies in Θ, we have
xR = x exp(Θ/2) = exp(−Θ/2)x = R̃x,
(2.65)
while if x is orthogonal to Θ, we have
xR = Rx.
45

(2.66)

## PDF page 47

In the second case, the rotor transformation law simply reduces to
R̃xR = R̃Rx = x.

(2.67)

The vector is unchanged by a rotation along the plane orthogonal to it. In the first case,
however, we get:
R̃xR = xRR = xR2 = x exp(Θ).
(2.68)
We know this - this is the rotation law from the two-dimensional geometric algebra! This
makes intuitive sense - in 2D, all vectors lie inside the plane of all bivectors, so we can
always simplify the full two-sided rotor law into a one-sided one.

2.2.7

Angular velocity

The rotor R = exp(Θ/2) describes a rotation along the direction and with the magnitude
of Θ. Now, we can ask ourselves how we can describe a rotational motion, i.e. a motion
where the angle depends on the time t. With geometric algebra, this is as simple as
R(t) = exp(Θ(t)/2).

(2.69)

The change in time of this rotor is:
˙
Θ̇(t)
Θ(t)
exp(Θ(t)/2) = exp(Θ(t)/2)
.
(2.70)
Ṙ(t) =
2
2
This is just the standard formula for taking the derivative of exponentials. Note that
Θ and R commute. Commonly, the derivative of the angle bivector Θ(t) is called the
“angular velocity bivector”:
Ω(t) = Θ̇(t)
(2.71)
If the angular velocity is constant, the above equations simplify to
R(t) = exp(Ωt/2)
(2.72)
Ω
Ω
= exp(Ωt/2).
2
2
Now suppose we start with a vector x0 and use the rotor R(t) to rotate it around. We
obtain the vector
x(t) = R̃(t)x0 R(t).
(2.73)
Ṙ(t) = exp(Ωt/2)

If we take the time derivative, we get:
ẋ = (R̃x0 R)·
˙ R + R̃x Ṙ
= R̃x
0

0

Θ̇
Θ̇
= − R̃x0 R + R̃x0 R
2
[ 2
]
Θ̇
= R̃x0 R,
,
2
[
]
Ω
= x,
2
46

(2.74)

## PDF page 48

We can therefore say that the velocity of an object at coordinate x being rotated with
angular velocity Ω around the origin is
Equation 2.11

Rotation velocity
[
]
Ω
ẋ = x,
2

(2.75)
π

This formula should make perfect intuitive sense - the angular velocity bivector represents an infinitesimal rotation after an infinitesimal time (think dΘ = Ω dt), so it can
be viewed as a generator acting on x.
We can even go one step further and find the centripetal acceleration by taking
another time derivative:
]
[
Ω
ẍ = ẋ,
2
[[
]
]
Ω Ω
(2.76)
= x,
,
2
2
)
1( 2
=
xΩ − ΩxΩ − ΩxΩ + Ω2 x
4
The quantity Ω2 is a negative scalar. Therefore, it commutes with everything, and we
can write:
Equation 2.12

Centripetal acceleration
)
1( 2
ẍ =
Ω x − ΩxΩ
2

(2.77)
π

If x lies inside the plane of the angular velocity Ω, they anticommute. In this case,
we can write ΩxΩ = −Ω2 x, and the above formula becomes particularly simple:
ẍ = Ω2 x

(2.78)

In 3D, bivectors square to negative values, i.e. Ω2 = −ω 2 . This automatically tells us
that the centripetal force has to pull the object into the center. If we multiply with m,
we thus get the well-known formula for the centripetal force:
F = mẍ = −mω 2 x.

2.3

(2.79)

Differential operators

The operator ∂i is defined as the partial derivative of some value by the coordinate i:
∂i a :=
47

∂a
.
∂xi

(2.80)

## PDF page 49

In traditional vector calculus, we use it to define the gradient operator
 
∂1
∇ = ∂2  .
∂3

(2.81)

When we apply this operator to a scalar field a, it gives us the direction of the steepest
increase of the field ∇a.
If we want to apply ∇ to a vector field v, we could take the dot product between
them to obtain the divergence:
∇ · v = ∂1 v 1 + ∂2 v 2 + ∂3 v 3 ,

(2.82)

or the cross product to obtain the curl:

 3
∂2 v − ∂3 v 2
∇ × v = ∂3 v 1 − ∂1 v 3  .
∂1 v 2 − ∂2 v 1

(2.83)

Needless to say, these expressions do not generalize to higher dimensions like 4D spacetime
or behave sensibly under parity flips.

2.3.1

The geometric derivative

Instead, we define the so-called geometric derivative or vector derivative3
Equation 2.13

Geometric derivative
∂ = ei ∂i .

(2.84)
π

This derivative is an element of the geometric algebra Cl(3) - it is a differential
operator-valued vector. It is very versatile: When we apply it to a scalar field a, it
acts like the gradient operator:
∂a = ei ∂i a.
(2.85)
Things start to get interesting once we apply it to a vector field v = v i ei :
∂v = ei ∂i v j ej
= ei ej ∂ i v j

(2.86)

Note that the order of the vectors ei , ej needs to stay fixed. The objects ∂i , v j are scalars,
so we can commute them around as we like.
3

Also denoted as ∇ instead of ∂.

48

## PDF page 50

∇×v

v

∂∧v
Figure 2.6: A sample vector field with its curl and exterior derivative.
The product between ∂ and v is the normal geometric product. It consists of the
interior product and the exterior product. We call ∂ · v the interior derivative and
∂ ∧ v the exterior derivative:
∂ · v = (ei · ej )∂i vj = ∂i v i
1
∂ ∧ v = (ei ∧ ej )∂i vj = (∂ i v j − ∂ j v i )ei ∧ ej
2

(2.87)

These derivatives can be applied to any multivector field. The grade of the exterior
derivative is one higher than the original field, and the grade of the interior derivative
one lower.
When applied to a vector, the interior derivative does what the classical divergence
does, and the exterior derivative does what the curl does. However, the curl was an axial
vector - and the exterior derivative of a vector field is the bivector corresponding to that
axial vector. Figure 2.6 illustrates this.
There is something important to note when taking the exterior and interior derivative
of vector fields. Suppose we have an axial “vector” field b, which corresponds to a bivector
field B = Ib. Then, the curl ∇ × b would translate to the interior derivative ∂ · B, and
the divergence ∇ · b would correspond to the exterior derivative ∂ ∧ B.
Two successive applications of the interior derivative or the exterior derivative on any
multivector are always zero:
Equation 2.14

Double interior and exterior derivatives
∂ · (∂ · M ) = 0
∂∧∂∧M =0

(2.88)
π

The second identity is quite easy to prove:
∂ ∧ ∂ ∧ M = e i ∂i ∧ e j ∂j M
= ∂i ∂j (ei ∧ ej )M
49

(2.89)

## PDF page 51

The wedge product ei ∧ ej is antisymmetric. However, partial derivatives commute ∂i ∂j = ∂j ∂i . This means that the term is identically zero.
We can’t quite prove the first identity yet without having to resort to a plethora of
confusing (−1)n(n−k)k factors of the sort differential form advocates like to use to feel
superior over us muggles. The good news is that we are going to develop the right tools
for this proof in the next chapter, so stay tuned.

2.3.2

Identities involving the geometric derivative

The geometric derivative ∂ consists of the sum of the interior and exterior derivative:
∂ = ∂ · + ∂∧

(2.90)

It might seem like an unnecessary complication to sum them together. After all, don’t
we need the inner and outer derivative for two completely different purposes?
It turns out that this does indeed make sense - the geometric derivative ∂ϕ “inherits”
its associativity from the geometric product. Associativity gives us a lot more flexibility.
For instance, suppose we have found a physical law saying that the geometric derivative
of some multivector field M is always zero:
∂M = 0.

(2.91)

When we premultiply both sides with another ∂, we can directly deduce:
∂ 2M = 0

(2.92)

The operator ∂ 2 is a scalar. It is commonly known as the Laplacian ∆ = ∇2 . In
traditional vector calculus, it would’ve been very difficult to deduce this identity at this
level of generalization. This associative way of handling geometric derivatives will prove
to be very useful in electrodynamics and quantum field theory.
The associativity is also very useful for some other purposes. For instance, let’s try
to decompose ∂ 2 into its constituents:
∂ 2 M = (∂ · + ∂ ∧)(∂ · + ∂ ∧)M
= ∂ · ∂ · M + ∂ · (∂ ∧ M ) + ∂ ∧ (∂ · M ) + ∂ ∧ ∂ ∧ M

(2.93)

The double-interior and double-exterior derivatives are zero:
∂ 2 M = ∂ · (∂ ∧ M ) + ∂ ∧ (∂ · M )

(2.94)

This is simple enough - a double geometric product decomposes into four parts, of which
two are zero. Now let’s assume that M is a vector field, i.e. M = v. Then:
∂ 2 v = ∂ · (∂ ∧ v) + ∂ ∧ (∂ · v).

(2.95)

The rightmost term is the exterior derivative of the scalar ∂ · v. Scalars have grade 0, so
the interior derivative of a scalar is always zero. Therefore, the exterior derivative of ∂ · v
50

## PDF page 52

is equal to its geometric derivative - aka its gradient, in conventional vector calculus. The
exterior derivative ∂ ∧ v is a bivector, which would normally be an axial vector resulting
from the curl. The subsequent interior derivative would also be translated as the curl,
as it is being applied on a bivector field. Therefore, in conventional vector calculus, this
identity reads:
∇2 v = −∇ × (∇ × v) + ∇(∇ · v).
(2.96)
This identity is well-known from conventional vector calculus. However, our formulation
(2.94) is both easier to derive and valid for all multivector grades instead of just vectors.

2.3.3

Product rule

The product rule is valid for the derivative. However, we have to be careful - the geometric
derivative ∂ is not commutative, so we cannot just write
∂(AB) = (∂A)B + A(∂B)

(INCORRECT!)

(2.97)

Instead, we have do introduce overdot notation: In the second term in the above
formula, ∂ should still stand before A, but only act on B. We will denote this with an
overdot over ∂ and the part of the expression ∂ is acting on:
Equation 2.15

Product rule for the geometric derivative
˙ Ḃ.
∂(AB) = ∂˙ ȦB + ∂A

(2.98)
π

The dots mark which part of the multivector expression the operator is acting on.
Written out, this would look like
ei ∂i (AB) = ei (∂i A)B + ei A∂i B.

(2.99)

The reason for this confusing change is simple: Previously, when we read an expression
like a∂i b, we were used to the order indicating which part the differential acts on. But in
multivector expressions, the order indicates the geometric product order - therefore, we
need a new way to indicate the order of differentials, i.e. the overdots.
This might seem like a complication, but in fact, it gives us far greater liberty - for
instance, we could also write down a “backwards derivative”
Ȧ∂˙ = (∂i A)ei .

(2.100)

This newfound freedom will prove especially useful in the area of geometric calculus. For
instance, we have seen how we can write the interior and exterior product between vectors
as the symmetric and antisymmetric part of the geometric product:
1
(ab + ba)
2
1
a ∧ b = (ab − ba)
2
a·b=

51

(2.101)

## PDF page 53

If we want to write the interior and exterior derivative this way, we need to use the overdot
notation:
)
1(
∂a + ȧ∂˙
∂·a=
2
(2.102)
)
1(
∂a − ȧ∂˙ .
∂∧a=
2

2.4

Pauli matrices

In quantum mechanics, we define the Pauli matrices,
(
)
(
)
(
)
0 1
0 −i
1 0
σ1 =
σ2 =
σ3 =
.
1 0
i 0
0 −1

(2.103)

In practically all quantum mechanics courses, they just fall out of the sky. However,
with geometric algebra, we’re able to understand the understand the reasoning behind
them. We first note that they all square to 1:
σ12 = 1
σ22 = 1
σ32 = 1

(2.104)

They anticommute with each other:
σi σj = −σj σi

for all i ̸= j.

(2.105)

This looks familiar - the basis vectors ei of the geometric algebra of space behave exactly
the same way. The matrix product between Pauli matrices takes the role of the geometric
product. Mathematically, we say that the Pauli matrices σi are a representation of the
geometric algebra of space Cl(3) - any calculation we can perform in Cl(3) can also be
done with Pauli matrices if we make the substitutions
(
)
1 0
1→
0 1
ei → σi
eij → σi σj

(2.106)
(

e123 → σ123 =

)
i 0
.
0 i

Adding and multiplying these matrices yields the same result as adding and multiplying the underlying multivectors. We can even form matrix exponentials - for instance, a
rotor generated by the rotation bivector
Θ = Θ12 e12 + Θ23 e23 + Θ31 e31

52

(2.107)

## PDF page 54

would have the Pauli matrix representation
(
)
R = exp Θ12 σ1 σ2 + Θ23 σ2 σ3 + Θ31 σ3 σ1
(
)
iΘ12
iΘ23 + Θ31
= exp
iΘ23 − Θ31
−iΘ12

(2.108)

The representation of the reverse M̃ of a multivector M is just the hermitean conjugate
of its representation M † . It leaves the scalar and the basis vectors invariant, but it flips
around the order of the matrix product. This is exactly what we want.
The matrix representation of a vector v would be:
(
)
v3
v 1 − iv 2
i
v = v σi =
(2.109)
v 1 + iv 2
−v 3
You can check for yourself that the matrix representation of the rotor law,
v′ = R† vR

(2.110)

(reading all the symbols as matrices representing multivectors) yields the same result as
the proper multivector equation
v′ = R̃vR.
(2.111)
All of this might come as a bit of an epiphany - we have been doing three-dimensional
geometric algebra with the Pauli matrices all the time! However, at the same time, we
have left some important questions unanswered: The main application of Pauli matrices
are spinors (aka spin states). How do they fit into all of this? What does it mean to write
si = ⟨ψ| σ i |ψ⟩ ,

(2.112)

for instance? Stay tuned - we are going to answer these questions in the chapter about
spinors.

53

## PDF page 55

Chapter 3
Tensor notation
A tensor is something that
transforms like a tensor
Ancient theoretical physics proverb

Chapter summary
• Tensor notation is not the same as matrix representation.
• We can denote k-vectors as fully antisymmetric rank k tensors. Every fully antisymmetric rank k tensor is a bivector.
• Multivectors can’t be denoted that way because the rank of a tensor is fixed.
• We can write the wedge product by using the antisymmetrization brackets [· · · ] on
tensors.
• We can write the interior product by forming sandwich contractions between tensors.
• The antisymmetric rank-2 tensors representing bivectors can be written as matrices.
If we exponentiate such a matrix, we get the rotation matrix corresponding to the
rotor generated by the bivector.

3.1

Overview

Geometric algebra is a very nice tool, but it has its limits. Sometimes, it can be preferable to use conventional tools like matrices or tensors to do a calculation. In addition,
practically all physics literature right now is written in conventional maths. Therefore, it
would be nice to have the tools to fluently switch between tensor notation and geometric
algebra notation.

54

## PDF page 56

3.1.1

Tensor notation is not the same as matrix representation

First of all, a warning: Previously, we have introduced the Pauli matrix representation
for Cl(3).
Warning 3.1
However, matrix representation and tensor notation are two completely different
things.
!
In particular:
• A matrix representation maps every multivector onto a matrix. However, tensor
notation can only depict pure k-vectors.
• In matrix representation, we always work with matrices. In tensor notation, we work
with tensors of arbitrary rank - and the rank-2 ones just happen to be matrices,
too.
• In matrix representation, we can multiply two matrices to get the geometric product
between the two multivectors. In tensor notation, we cannot denote the geometric
product.
• In tensor notation, the indices of our tensors are vector indices - they run over basis
vectors. In matrix notation, the indices of our tensors are spinor indices - they run
over basis spinors. You will find out what that means in the spinor chapter.

3.1.2

Fully antisymmetric rank k tensors

The fundamental principle of converting geometric algebra expression to tensors is the
basis notation of k-vectors. We already know that we can write an arbitrary k-vector as
a linear combination of basis k-vectors:
Equation 3.1

Tensor notation for a k-vector
X=

1 i1 i2 ···ik
X
ei1 ∧ ei2 ∧ · · · ∧ eik
k!

(3.1)
π

The collection of components X i1 i2 ···ik is a rank-k tensor. It is fully antisymmetric.
This means that it flips sign if we exchange any two indices:
X i1 i2 ···ik = −X i2 i1 ···ik .

(3.2)

This is because the basis bivectors also flip sign when we exchange two indices because of
the wedge product antisymmetry. This antisymmetry implies that all indices i1 , i2 , · · · , ik

55

## PDF page 57

need to be distinct from each other - if there is a duplicate index, the component is zero:
X i1 i1 ···ik = −X i1 i1 ···ik = 0

(3.3)

This equivalence always holds: Fully antisymmetric rank-k tensors correspond to kvectors, and vice versa.
Fully antisymmetric rank-k tensors

3.1.3

↔

k-vectors.

(3.4)

Vectors, bivectors and trivectors

The easiest example is the vector - we can write any arbitrary vector v as:
v = v i ei .

(3.5)

Remember that vectors v i are rank-1 tensors. Similarly, a bivector B can be written as
B=

(
)
1 ij
B ei ∧ ej = B 12 e12 + B 23 e23 + B 31 e31 .
2!

For bivectors only, we can also denote their components in matrix form:

 11
B
B 12 B 13
B ij = B 21 B 22 B 23 
B 31 B 32 B 33


0
B 12 −B 31
0
B 23 
= −B 12
B 31 −B 23
0

(3.6)

(3.7)

You are probably wondering why we used a factor of 1/k! to define the basis decomposition. The reason is simple - take the above bivector decomposition with its 1/2! factor
as an example. The Einstein summation convention in this formula will sweep across
both cyclic and anticyclic indices - for instance, somewhere in the sum, ij would assume
the value 23, and then 32 a bit later. Because ei ∧ ej = −ej ∧ ei , we needed to define
B ij = −B ji .

(3.8)

Then, the 23 and 32 parts of the sum would resolve to:
B 23 e23 + B 32 e32 = 2B 23 e23

(3.9)

We see that by summing over all possible combinations of ij, we “overcount” the basis
bivectors twice, because there are two possible permutations for every ij index pair.
Similarly, there are 6 = 3! permutations for every index triple ijk, so in order to write
down a trivector in terms of its components, we’d need to write
T =

1 ijk
T ei ∧ ej ∧ ek
3!
56

(3.10)

## PDF page 58

in order to get the normalization right. The expression T ijk might raise some eyebrows
- after all, we are working in three dimensions, so all possible index triples ijk without
duplicates are permutations of 123. The even permutations of 123 will all be equal to
some t ∈ R, and the odd permutations will be −1 times the even permutations:


if ijk is an even permutation of 123
t
ijk
T = −t if ijk is an odd permutation of 123 .
(3.11)


0
if ijk has duplicate indices.
This should look somewhat familiar - the Levi-Civita symbol in three dimensions, ϵijk
is defined as:


if ijk is an even permutation of 123
1
ijk
(3.12)
ϵ = −1 if ijk is an odd permutation of 123 .


0
if ijk is not a permutation of 123.
We can conclude that the tensor T ijk denoting a trivector T in three dimensions must
always be a multiple of ϵijk :
T ijk = tϵijk
(3.13)
The Levi-Civita symbol itself denotes the unit pseudoscalar:
1
1 ijk
ϵ ei ∧ ej ∧ ek = 3! e123 = e123 .
3!
3!

(3.14)

Therefore, it is absolutely valid to refer to the Levi-Civita symbol as the pseudoscalar
symbol.
In geometric algebra, we always work with an orthonormal metric. In the threedimensional case, our metric is just δij , so we can pull indices up and down however we
please. We could therefore also write B as
B = Bij ei ∧ ej .

(3.15)

This will change though as soon as we treat the spacetime algebra, where the metric ηµν
is nontrivial.

3.1.4

Extracting components

Now, we should investigate how to extract the tensor components of a given k-vector
algebraically. For vectors v, this is simple: We just take the interior product between the
vector and the basis vector in question:
v i = v · ei = ⟨vei ⟩ .

(3.16)

Intuitively, we might expect that this extends to arbitrary k-vectors. For instance, for
bivectors, we might try to write
⟨
⟩
B ij = B · (ei ∧ ej ) = B(ei ∧ ej )
(INCORRECT!).
(3.17)
57

## PDF page 59

But if we do this, we run into a problem: The bivectors eij square to −1, so for instance,
for a bivector B = e12 , we’d obtain the components B 12 = −B 21 = e12 · e12 = −1, the
opposite of what we want.
The solution is to dot the bivector with the inverse of the basis bivectors:
(eij )−1 = −eij .

(3.18)

Note that the inverse operation (· · · )−1 implicitly swaps upstairs and downstairs indices.
Hence, we obtain the correct tensor components by writing
⟨
⟩
B ij = B · (eij )−1 = B(ei ∧ ej )−1
(3.19)
The generalized formula for the components of a k-vector X of arbitrary grade is:
Equation 3.2

Tensor components of a k-vector
⟨
⟩
X i1 i2 ·ik = X (ei1 ∧ ei2 ∧ · · · ∧ eik )−1 .

(3.20)
π

For 3D vectors (3.16), the fact that we had to use the inverse · · ·−1 does not matter for every i, we have e2i = 1 and thus (ei )−1 = ei . However, it will matter as soon as we
treat special relativity and spacetime algebra.

3.1.5

Some examples

Whenever we see a fully antisymmetric tensor in conventional math, it is safe to translate
it to a k-vector. Common examples include:
• T1 , T2 , T3 , the generator matrices of SO(3): Matrices are rank-2 tensors, so these
are actually the bivectors e23 , e31 and e12 .
• As explained above, the Levi-Civita symbol ϵ actually is the unit pseudoscalar.
• The electromagnetic field tensor F µν actually is a bivector in the geometric algebra
of spacetime - more on that in the Electrodynamics chapter.
• The Riemann tensor Rµνρσ from general relativity is antisymmetric in its first two
and in its last two indices. Thus, it is a linear map from bivectors to bivectors.

3.2

Operations in tensor notation

Now that we have seen how we can write k-vectors as tensors, the next logical step is to
ask ourselves how to perform operations like the addition on them.

58

## PDF page 60

3.2.1

Linear operations

Linear operations on k-vectors in tensor notation are pretty simple and work as we’d
intuitively expect. For instance, if we want to add two k-vectors, we just need to add
their tensor notations together componentwise:
(B + C)ij = B ij + C ij .

(3.21)

Scalar multiplication works similarly easy:
(λB)ij = λB ij .

(3.22)

However, you may have already noticed the important caveat here: In tensor notation,
we can only add k-vectors of equal grade. It is not possible to denote mixed-grade
multivectors in tensor notation. Hence, it is not possible to denote the geometric product
- it inherently produces mixed-grade multivectors. It is possible though to denote the
interior and exterior product in tensor notation. But first, we will have to introduce some
new notation.

3.2.2

Symmetric and antisymmetric parts

Let Z i1 i2 ···ik be a rank-k tensor that is not necessarily symmetric or antisymmetric. First
of all, we define the symmetrization of Z as:
Equation 3.3

Symmetrization of a tensor
)
1 ( i1 i2 ···ik
Z (i1 i2 ···ik ) =
Z
+ all permutations of i1 i2 · · · ik .
k!

(3.23)
π

We are averaging over all possible permutations. The resulting tensor is completely
symmetric, as all antisymmetries have been “leveled out” by the sum over all permutations. If we were two swap two indices, the result would be exactly the same. For
instance, the symmetrization of a rank-3 tensor Z ijk would read
Z (ijk) =

)
1 ( ijk
Z + Z kij + Z jki + Z kji + Z jik + Z ikj .
3!

(3.24)

In contrast, the antisymmetrization of a tensor Z i1 i2 ···ik is defined as:
Equation 3.4
Z [i1 i2 ···ik ] =

Antisymmetrization of a tensor

)
1 ( i1 i2 ···ik
Z
+ all other even permutations − all odd permutations
k!
(3.25)
π

59

## PDF page 61

Now, we are not simply taking the average over all possible permutations - we are
adding the even ones and subtracting the odd ones. This means that Z [i1 i2 ···ik ] is fully
antisymmetric - whenever we exchange two indices, the perviously even permutations will
become odd, and the previously odd permutations will become even. We can say that we
have “averaged out” all symmetric parts of the tensor. For instance, the antisymmetrization of a rank-3 tensor would read
Z [ijk] =

)
1 ( ijk
Z + Z kij + Z jki − Z kji − Z ikj − Z jik
3!

(3.26)

If the tensor denotes a k-vector (i.e. if the tensor already is fully antisymmetric),
the antisymmetrization operation will have no effect on the tensor. For instance, for a
trivector T ijk :
T [ijk] = T ijk .
(3.27)

3.2.3

Interior product

Now, we are equipped to understand the expressions for the interior and exterior product.
We start by investigating the interior product. We already know the simplest case - the
interior product between two vectors v, w:
v · w = v i wi .

(3.28)

We simply form the contraction of their indices. Similarly, for bivectors and trivectors,
(B · v)i = B ij vj
(T · v)ij = T ijk vk ,
or from the other side:

(v · B)i = vj B ji
(v · T )ij = vk B kij

(3.29)

(3.30)

The general formula involving a k-vector X and a vector v is:
Equation 3.5

Interior product between a k-vector and a vector
(X · v)i1 i2 ···ik−1 = X i1 i2 ···ik−1 j vj
(v · X)i1 i2 ···ik−1 = vj X ji1 i2 ···ik−1 .

(3.31)
π

Now, we can ask ourselves how we can dot together k-vectors of arbitrary rank. We
already know that if the k-vectors are in basis form, we can rewrite the inner product
between them as a series of inner products of k-vectors with vectors. For instance, the
inner product e123 · e23 :
e123 · e23 = (e123 · e2 ) · e3
(3.32)

60

## PDF page 62

We are free to reorder the k-vector we are splitting up. For instance:
e123 · e23 = e123 · (−e32 ) = −(e123 · e3 ) · e2 .

(3.33)

Thus, to calculate such an interior product, we could naı̈vely try writing down a sandwich
contraction like
(T · B)i = T ijk Bkj .
(INCORRECT!)
(3.34)
We run into an issue here. When we work in geometric algebra notation like in (3.32)
and (3.33), we choose a specific ordering for the vectors we are dotting onto the trivector.
However, in (3.34), we sum over all index pairs jk, so we include all possible orderings
of the bivector. Hence, the correct formula has to divide by l!, where l is the number of
dummy indices. The previous example therefore correctly translates to
(T · B)i =

1 ijk
T Bkj .
2!

(3.35)

Let’s consider the general interior product between a k-vector X and an l-vector Y ,
where k > l. The resulting grade is k − l. The general sandwich contraction formula is:
Equation 3.6

Interior product between a k-vector and an l-vector
(X · Y )i1 ···ik−l =

1 i1 ···ik−l j1 j2 j3 j4 ···jl
X
Yjl ···j4 j3 j2 j1 .
l!

(3.36)
π

Proof of double interior derivative identity
Now, we are ready to prove the identity
∂ · (∂ · M ) = 0.

(3.37)

First of all, because the double interior derivative is linear, we can assume that M is a
pure k-vector without loss of generality. We can thus denote M as a tensor M i1 i2 ···ik . The
geometric derivative ∂ is denoted by the rank-1 tensor ∂ i . The first inner product is a
k − 1 vector:
(∂ · M )i2 i3 ···ik = ∂i1 M i1 i2 ···ik .
(3.38)
The second one can be sandwiched on top of the first one:
(∂ · (∂ · M ))i3 ···ik = ∂i2 ∂i1 M i1 i2 i3 ···ik .

(3.39)

M is antisymmetric over all indices. However, the two partial derivatives commute with
each other. Thus, the index contraction is equal to zero:
(
)
1
∂i2 ∂i1 M i1 i2 ··· = ∂i2 ∂i1 M i1 i2 − M i2 i1
2
)
1(
=
∂i2 ∂i1 M i1 i2 − ∂i1 ∂i2 M i2 i1
2
61

(3.40)

## PDF page 63

We now rename the indices in the second term - we can do that because they are dummy
indices:
)
1(
∂i2 ∂i1 M i1 i2 − ∂i2 ∂i1 M i1 i2
=
2
(3.41)
= 0.
Thus, we have proven the identity ∂ · (∂ · M ) = 0. Also, in general, we can remember
that if we contract something symmetric with something antisymmetric, the result will
always be zero.

3.2.4

Exterior product

Let’s say we want to take the exterior product between the vectors v = e1 and w = e2 ,
resulting in the bivector v ∧ w = e12 . The only nonzero components of the tensors v i and
wi are v 1 = 1 and w2 = 1, respectively, and the only two nonzero components of (v ∧ w)ij
are (v ∧ w)12 = −(v ∧ w)21 = 1. Therefore, our first impulse might be to write something
like
(v ∧ w)ij = v i wj
(INCORRECT!)
(3.42)
This tensor would have the component v 1 w2 = 1, but the other one is missing, v 2 w1 = 0.
It is not antisymmetric. We could therefore try to antisymmetrize the tensor:
(v ∧ w)ij = v [i wj]

(INCORRECT!)

(3.43)

However, the antisymmetrization brackets [· · · ] average over the components, so the above
tensor has the components
1
(3.44)
v [1 w2] = v [2 w1] =
2
half of what we want. This is because the component v 1 w2 has been “smeared out” over
the 2! = 2 index pairs 12 and 21. We therefore need to premultiply this expression with
2!. We obtain the correct result,
(v ∧ w)ij = 2! v [i wj] .

(3.45)

This generalizes to arbitrarily long exterior products of k-vectors. For instance:
(a ∧ b ∧ c)ijk = 3! a[i bj ck] .

(3.46)

The general formula for the exterior product of l vectors a(1) , · · · , a(l) is:
[i

i]

l
2
(a(1) ∧ · · · ∧ a(l) )i1 i2 ···il = l! a(1)1 ai(2)
· · · a(l)
.

(3.47)

The next thing to ask ourselves is how to calculate the exterior product between a
k-vector X and an l-vector Y . Looking at (3.47), we could naively try to write
(X ∧ Y )i1 ···ik+l = (k + l)! X [i1 ···ik Y ik+1 ···ik+l ]

(INCORRECT!)

(3.48)

But then, we run into a similar problem as we did in (3.34). The formula (3.47) refers
to the exterior product of a specific ordering of vectors. However, a k-vector like X i1 ···ik
contains all k! possible orderings of the cross product. The formula (3.48) would therefore
overcount the product by k! times l! times. We can thus see that the correct formula is:

62

## PDF page 64

Equation 3.7

Exterior product betweeen a k-vector and an l-vector
(X ∧ Y )i1 ···ik+l =

(k + l)! [i1 ···ik ik+1 ···ik+l ]
Y
X
k! l!

(3.49)
π

An important special case is the exterior product between a vector and a k-vector:
Equation 3.8

Exterior product between a vector and a k-vector
(a ∧ X)i1 i2 ···ik+1 = (k + 1) a[i1 X i2 ···ik+1 ]
(X ∧ a)i1 i2 ···ik+1 = (k + 1) X [i1 ···ik aik+1 ]

(3.50)
π

3.3

Differential forms

Almost every one of us will already have encountered differential forms and exterior algebra. Geometric algebra and exterior algebra are very similar in principle, but
there are some important differences. Broadly speaking, differential forms put a focus
on mathematical naturalness and abstract beauty, while geometric algebra puts a focus
on practicability and geometric intuition. In other words, exterior algebra is for physics
gods, and geometric algebra is for mortals like us.
The most important difference is that there is no metric or interior product in exterior
algebra - it is not possible to pull indices up and down as we please. Because we have a
metric in GA, it does not matter whether our vectors are covariant or contravariant. In
exterior algebra, however, we always work with covariant vectors. The basis covariant
vectors, also called one-forms, are denoted
dx1 , dx2 , · · · , dxn .

(3.51)

In our notation, they are just the basis vectors with raised indices:
e1 , e2 , · · · , en .

(3.52)

In exterior algebra, k-vectors are called k-forms. For instance, the bivector
B = e1 ∧ e2

(3.53)

B = dx1 ∧ dx2 .

(3.54)

is equivalent to the 2-form
In differential geometry, pseudoscalars are called top-forms. The exterior derivative
∂ ∧ X is denoted
dX
(3.55)
in exterior algebra. The commonly given definition for dX,
dX i1 i2 ···ik+1 = (k + 1) ∂ [i1 X i2 ···ik+1 ] ,
63

(3.56)

## PDF page 65

is just the tensor notation for the expression ∂ ∧ X.
The greatest problem with differential forms is their lack of an interior product,
and, as a consequence, a lack of an interior derivative. To remedy this, exterior algebra
defines the so-called Hodge dual ∗X. It turns a k-vector X into an n − k-vector ∗X,
where n is the number of dimensions. Its definiton is:
1
i
i
···i
(3.57)
(∗X)i1 i2 ·in−k = ϵi1 i2 ···in−k n−k+1 n−k+2 n Xin−k+1 in−k+2 ···in .
k!
This definition seems pretty intimidating, and the standard way of teaching it is completely devoid of any geometric intuition. This is part of the problem - there are good
abstract mathematical reasons to define the Hodge dual the way we do, but they are only
accessible to the initiates of expert differential geometry. Everyone else mostly just learns
this definition by heart and hopes to never have to use it again.
Luckily, we have geometric algebra now. Let us take a step back and think about
which parts of this definition we know already. The pseudoscalar symbol ϵ is the tensor
notation for the pseudoscalar I, so it looks a bit like we’re taking the interior product
between the pseudoscalar I and the k-vector X. But that’s not quite it yet - the index
contractions in (3.57) are not in sandwich order like in (3.49).
But luckily, X is totally antisymmetric, so we can rearrange them into sandwich order.
The first index of X we are pulling to the left will take (k − 1) permutations. The next
one will take (k − 2) permutations. This goes on until we have performed
k(k − 1)
(3.58)
2
permutations, and the expression for the Hodge dual reads:
k(k−1) 1
i
i
···i
(3.59)
ϵi1 i2 ···in−k n−k+1 n−k+2 n Xin ···in−k+2 in−k+1 .
(∗X)i1 i2 ·in−k = (−1) 2
k!
This looks exactly like the interior product in tensor notation (with lowered indices). We
can now translate the definition of the Hodge dual of a k-vector into GA:
(k − 1) + (k − 2) + · · · + 2 + 1 =

Equation 3.9

Hodge dual in GA
∗X = (−1)

k(k−1)
2

IX.

(3.60)
π

If we are careful with the signs, we can construct a kind of “interior product surrogate”
with the Hodge dual, as we will see in the electrodynamics chapter when translating the
differential form electrodynamic equations. However, in general, we have no reason to use
the Hodge dual - everything gets a lot easier with a metric.

3.4

Transformation matrices

In the last chapter, we have seen how we can describe rotations with rotation bivectors
Θ, rotors
R = exp(Θ/2),
(3.61)
64

## PDF page 66

and the rotor law
v′ = R̃vR.

(3.62)

The normal formalism is somewhat different. Instead of rotors, we use rotations
matrices M = M ij . They are linear maps mapping vectors to other vectors:
v ′i = M ij v j .
Those matrices can also be written as matrix exponentials:
(
)
M = exp Ti θi ,
where



0 0 0
T1 = 0 0 1
0 −1 0


0 0 −1
T2 = 0 0 0 
1 0 0


0 1 0
T3 = −1 0 0
0 0 0

(3.63)

(3.64)

(3.65)

are the generators of SO(3) and θi are the components of the rotation “vector”. For a
specific θi , this results in the generator matrix


0
θ3 −θ2
θ1 
(3.66)
Ti θi = −θ3 0
2
1
θ
−θ
0
Now, let’s try to make sense of this with geometric algebra. The first thing we note
is that the rotation axial vector is actually a bivector Θ = Iθ:
Θ = θ3 e12 + θ1 e23 + θ2 e31

(3.67)

Θ12 = −Θ21 = θ3
Θ23 = −Θ32 = θ1
Θ31 = −Θ13 = θ2

(3.68)

Its tensor components are:

So we would rewrite the above matrix as


0
Θ12 −Θ31
0
Θ23  = Θij .
Ti θi = −Θ12
Θ31 −Θ23
0

(3.69)

This is just the tensor notation for the rotation bivector Θ! We can see that the SO(3)
generator matrices Ti and the contraction Ti θi are just a really roundabout way to denote a
65

## PDF page 67

bivector without calling it a bivector. Then, the rotation matrix is the matrix exponential
of the tensor notation of the rotation bivector.
We can also do this the other way around: We can obtain the rotation matrix M ij
from a rotor by calculating
Equation 3.10

Rotation matrix corresponding to a rotor
M ij = ei · (R̃ej R).

(3.70)
π

We will rarely need this formula in practice - after all, we want to stop using rotation
matrices. It is still useful though to learn about how rotation matrices interlink with
geometric algebra.
When we apply a rotation matrix M to a vector v, it transforms like
v′ = M v,

(3.71)

v ′i = M ij v j .

(3.72)

or in index notation:
Vectors are rank-1 tensors. The above transformation law is a special case of the
tensor transformation law. In general, rank (k, l) tensors transform like
Equation 3.11

Tensor transformation law

(
)
T ′ i1 i2 ···ik ik+1 ···ik+l = M i1j1 M i2j2 · · · M ikjk M −1 i

jk+1
k+1

(
)
· · · M −1 i

jk+l
k+l

T ′ j1 j2 ···jk jk+1 ···jk+l ,
(3.73)
π

one rotation matrix for every index. Upstairs (contravariant) indices transform with
the normal rotation matrix, and downstairs (contravariant) indices transform with the
inverse rotation matrix. For instance, if we were to rotate a trivector T ,
T ′ = R̃T R

(3.74)

T ′ijk = M il M jm M kn T lmn ,

(3.75)

would transform like
the tensor transformation law for a rank (3, 0) tensor. However, if we pulled down one
of the indices (T ijk ), we’d have use the inverse for it:
(
)n
T ′ ij k = M il M jm M −1 k T lmn .
(3.76)

66

## PDF page 68

Chapter 4
Geometric algebra of spacetime
There is quite a large number of
quotes falsely attributed to me.
Sadly, people misattribute quotes to
me almost as often as they
misattribute quotes to Albert
Einstein.
Confucius

Chapter summary
• Special relativity unifies 1D time and 3D space into 4D spacetime.
• Four-vectors are constructed by combining one timelike quantity and one spacelike
quantity.
• The geometric algebra of spacetime, or spacetime algebra (STA) consists of four
basis vectors γµ . The timelike basis vector γ0 squares to (γ0 )2 = +1, and the
spacelike basis vectors γi to (γi )2 = −1.
• Lorentz boosts are just a special kind of rotation - hyperbolic rotations. In this
context, we call normal rotations “circular rotations”.
• The Dirac gamma matrices are a matrix representation of the spacetime algebra.
• The acceleration four-vector is always orthogonal to the velocity four-vector. We
can use the bivector a = AU to handle the resulting mathematical difficulties.
• Relativistic angular momentum decomposes into circular momentum (what we’re
used to), and hyperbolic momentum (a new kind of angular momentum).
• The space-time split links together non-relativistic and relativistic physics.
67

## PDF page 69

4.1

Basics

4.1.1

Foundations of special relativity

Special relativity is often perceived as an arcane science only accessible to geniuses - and it
doesn’t exactly help that many physics curriculae prioritize other topics over relativity, for
instance electromagnetism or quantum mechanics. We, however, want to show the reader
that relativity doesn’t need to be feared at all. Even though the historical development
of relativity can be very complex and confusing, it becomes very simple to grasp its
axiomatic foundations if one uses geometric algebra.
The basic axioms of special relativity can be summarized as follows:
• In addition to the three usual spatial dimensions x, y and z, we add in time t as
the fourth (or zeroth) dimension. Vectors now do not consist of three, but of four
elements.
• Normally, the three spatial unit vectors square to +1. We redefine them to square
to −1. The unit vector pointing in the time direction squares to +1.
Based on these axioms, we are going to build the so-called spacetime algebra (STA).
It is okay if you do not understand them yet - we are going to explain them in the next
few subsections.

4.1.2

Four-vectors

Previously, the basis vectors of our geometric algebra space were
e1 , e2 , e3 .
Now, to construct the geometric algebra of spacetime, we add in a zeroth basis vector
to represent time:
γ0 , γ1 , γ2 , γ3 .
An arbitrary four-vector xµ can be written as
x = xµ γµ

(4.1)

in this formalism, analogously to the three-dimensional space algebra.
However, this comes with a catch. In the space algebra, all the basis vectors square
to one (e2i = 1), but in spacetime algebra, we define
Equation 4.1

STA basis vector squares
(γ0 )2 = 1
(γ1 )2 = (γ2 )2 = (γ3 )2 = −1.

(4.2)
π

68

## PDF page 70

This means that an arbitrary vector a = aµ γµ will square to:
a2 = (a0 )2 (γ 0 )2 + (a1 )2 (γ1 )2 + (a2 )2 (γ2 )2 + (a3 )2 (γ3 )2
∑
= (a0 )2 −
(ai )2 .

(4.3)

i

In space algebra, non-zero vectors always square to positive values (a2 > 0). In STA,
however, we have to distinguish between three cases:
√
• a2 > 0: In this case, a is called a timelike vector. In this case, T = a2 is called
the proper time of a1
√
• a2 < 0: In this case, a is called a spacelike vector. In this case, s = −a2 is called
spacelike separation.
• a2 = 0: In this case, a is called a lightlike or null vector.

4.1.3

Natural units

The most important example of a four-vector is the time-position vector x. It describes
the time and location of an event - its time component specifies at what time an even
takes place, and its three space component specifies the location of the event:
x = tγ0 + xi γi
= xµ γµ .

(4.4)

We will also write four-vectors as a combination of a time component and a spatial vector:
Equation 4.2

Time-position vector
x = (t, x)

(4.5)
π

For instance, to describe the first nuclear explosion in history, we would write:
x = (July 16, 1945; Trinity Site, New Mexico, Earth).

(4.6)

However, please don’t picture this as a combination of two quantities, but rather as a
single point in a four-dimensional space. The way we humans have evolved has led us to
perceive time and space fundamentally differently, but the core point of special relativity
is that there is not that much of a difference - they are both dimensions of spacetime.
This should raise some eyebrows. The time component has the unit “second”, while
the space component has the unit “meters”. How are we supposed to add meters onto
seconds? The answer is simple: In special relativity, meters and seconds are just two
1

Proper time is normally called τ in the literature, but since we use τ = 2π, we call it to T to avoid
confusion.

69

## PDF page 71

different units for the same quantity - “time-length”, which measures distances in spacetime. The difference between seconds and meters really just is like the difference between
meter and feet. Just like there is a conversion factor to convert feet into meters,
1 foot
= 0.3048
1 meter

(4.7)

there is a conversion factor to convert seconds and meters into each other:
Equation 4.3

Natural units
1 second
= 299 792 458
1 meter

(4.8)
π

This number is better known as the speed of light. The reason for this is simple:
In special relativity, the speed of light is 1 by definition. When we measure it with our
backwards units of seconds and meters, we obtain:
c := 1 = 299 792 458 m/s

(4.9)

In order for this to work out, the conversion ratio s/m needs to be 299 792 458.
It is somewhat inconvenient to have two separate units for the same thing. Just
like the civilized world got rid of feet, special relativity got rid of seconds. Instead, we
measure time in meters. For instance, instead of saying “The bus is going to arrive in
three minutes”, we would calculate c · 180s = 54Gm and say “The bus is going to arrive
in 54 gigameters”.

4.1.4

Examples of four-vectors

We are now going to take a look at various four-vectors to get a feeling for them. We
start with the time-position four-vector.
Events
We have already given an example of a so-called absolute event four-vector:
x = (July 16, 1945; Trinity Site, New Mexico, Earth).

(4.10)

We call this vector “absolute” because it describes a specific point in spacetime. In
contrast, relative event four-vectors describe space-time separations between two events.
From everyday life, we are already familiar with some types of them:
Purely temporal relative four-vectors describe time separation. For instance, suppose
we were standing at the bus stop with the bus arriving in three minutes. There are two
relevant absolute four-vectors here: The current event
x0 = (now, here),
70

(4.11)

## PDF page 72

and the event of the bus arriving
x1 = (now + 3 minutes, here).

(4.12)

The relative2 four-vector describing the separation between these two events is
x = x1 − x0 = (3 minutes, 0) = (54 · 109 , 0, 0, 0) m.

(4.13)

If we square this vector, we find that we get a positive result:
x2 = (54 · 109 )(γ0 )2 = (54e9)2 > 0.

(4.14)

2
This is the reason for why we call
√ vectors x with x > 0 “timelike” - they describe
separations in time. The quantity x2 has a nice physical meaning: If an observer √
were
to move along this vector through space-time,
it
would
take
a
subjective
time
of
x2 .
√
This quantity is called the proper time T = x2 . It is called “proper” because its value
is the same, no matter the coordinate system. This is also valid for two events that are
separated spatially - in that case, the observer has to move through space.
In contrast, let’s suppose that we are late to the bus stop, and the bus is still departing
while we still are 100m away from the bus stop along the x-axis. This separation fourvector would look like
x = (0, 100m, 0, 0).
(4.15)

This vector would square to something negative:
x2 = (100m)2 (γ1 )2 = −(100m)2 < 0

(4.16)

This is why we√call vectors x with x2 < 0 “spacelike” - they describe separations in space.
The quantity −x2 describes the normal, spatial distance between two points we are
used to from classical physics. This√is also valid for points that do not happen at the
same time coordinate - in this case, −x2 describes how far the two points are spatially
separated from each other for an observer for which the two events take place at the same
time.
The physical difference between timelike, lightlike and null vectors is perhaps best understood by looking at a spacetime diagram where the time axis is depicted geometrically
alongside one or two3 space axes - see Figure 4.1.
If a four-vector U = U µ γµ describes the velocity of an object, the three cases respectively have the following physical meanings:
• timelike U : U describes a massive object moving slower than the speed of light.
2

It should be noted that the vectors we call “absolute” are actually relative too - the time component
is defined relative to an arbitrary moment in time, and the space component is defined relative to Earth.
However, in curved spaces like in general relativity, this does not work out anymore - then, absolute
points in spacetime and relative vectors are two distinct mathematical concepts.
3
We’d have a hard time drawing full 1+3D spacetime diagrams, so we usually ignore one or two space
axes.

71

## PDF page 73

γ0
Future

Past

timelike
spacelike
lightlike

γi

Past
Figure 4.1: A simple spacetime diagram showing the difference between timelike, spacelike, and lightlike vectors. The dashed lines represent the path of a light pulse emitted or
absorbed at the origin. The wavy line represents the path a moving object might take.
• lightlike U : U describes a massless object moving at the speed of light.
• spacelike U : U describes an object moving faster than the speed of light. Currently,
no such objects (“tachyons”) are known.
Spacelike vectors are mostly used to describe spacelike separations between two events
- i.e. the separation between two events occuring at the same time.
Four-velocity
The next type of four-vector we are going to examine is the velocity four-vector U = U µ γµ .
Its components tell us how much the time-position of an object changes per unit of proper
time. This is related, but not identical to the concept of classical velocity v:
The time component U 0 of the 4-vector U describes how fast the time coordinate of
the object changes per proper time of the object. For instance, if we watch a spaceship
flying past Earth with near the speed of light, its passengers would experience time a
lot more slowly than we do. The factor γ by which the astronauts experience time more
72

## PDF page 74

slowly than we is given by
1
(4.17)
γ=√
1 − v2
where v is the classical velocity of the spaceship. Remember that since meters and seconds
are just different units for the same thing, v is dimensionless4 . We can thus write that
U 0 = γ.

(4.18)

The classical velocity v measures how fast the space coordinates change per unit of time
coordinate. Therefore, to obtain the spatial parts of the four-velocity U , we need to write:
U i = γv i .

(4.19)

The full four-velocity is:
Equation 4.4

Four-velocity
U = (γ, γv).

(4.20)
π

A still-standing object with v = 0 only moves through time:
U = (1, 0).

(4.21)

U 2 = 1.

(4.22)

In general, U always squares to 1:

For this reason, we call these U timelike. This relation has
√ a physical interpretation: U
describes spacetime separation per unit of proper time. U 2 describes the proper time
an observer moving
along U experiences. But since U precisely describes separation per
√
2
proper time, U = 1. Therefore, U 2 = 1.
However, the story looks different for objects moving at the speed of light. Objects
moving at the speed of light do not experience time (for v → 1, γ → ∞). Therefore, we
cannot define a four-velocity of light.
Four-momentum
The four-momentum unites the classical concepts of energy and momentum. For massive
objects, it is given by:
Equation 4.5

Four-momentum
p = mU

4

(4.23)
π

We can obtain the dimensionless v by dividing the dimensionful v by c = 299 792 458m/s.

73

## PDF page 75

where m is the mass of the object. Its time component describe the energy of the
object, while its space components describe the momentum:
p = (E, p).

(4.24)

For a still-standing object, the four-momentum is given by:
p = (m, 0).

(4.25)

Classically, energy and momentum are two separate quantities, but in GR, they are
two sides of the same coin. Similarly, they have the same unit:
[p] = kg

m
m2
∼ kg.[E] = J = kg 2 ∼ kg.
s
s

(4.26)

We just need to insert the appropriate conversion factors. The famous equation E = mc2
actually is just a mundane conversion formula from units of kilograms to units of joule.
(And only valid for objects at rest.)
p squares to m2 :
p2 = m2 U 2 = m2 .
(4.27)
In fact, this is how mass is defined
in special relativity - mass is the time-length of the
√
momentum four-vector m = p2 .
Warning 4.1
Unfortunately, there is a bad habit among physicists to refer to the energy p0 as
the “mass”, which is supposedly increasing
while the object speeds up. This is not
√
the case - the actual mass is m = p2 . It does not change when we accelerate the
object.
!
A photon with wavelength λ and wavenumber k = τ /λ has energy E = ℏk and 3momentum p = ℏkn, where n is some normal vector. The four-momentum of the photon
then is
p = ℏ(k, nk).
(4.28)
It squares to p2 = 0, just as we’d expect - photons are massless.

4.1.5

Brief recap on time in special relativity

The word “time” has two meanings in special relativity: Coordinate time and proper
time.
Coordinate time describes time as measured by one specific observer. In other words,
coordinate time is the zeroth component x0 of a four-vector x. Evidently, this quantity
is not invariant under spacetime transformations - as we all know, observers moving at
very high velocities measure time differently. Therefore, when we want to specify the
74

## PDF page 76

trajectory a particle takes, we can’t just write the position as a function of coordinate
time, x(t) - this would cause serious trouble if we were to change coordinate systems.
What we do will do instead is parametrize paths by proper time. Proper time T is
defined as the time that has passed from the point of view of the object whose trajectory
we are trying to describe. If we parametrize the trajectory by some other parameter x(λ),
the proper time passing for the object between the points λ1 , λ2 is:
(
)2
∫ λ2
dx(λ)
dλ
.
(4.29)
T =
dλ
λ1
If we however parametrize the trajectory by T straightaway, i.e. x(T ), we get
(

dx(T )
dT

)2
=1

(4.30)

we can define the four-velocity U as the tangent vector of the trajectory:
U=

dx(T )
.
dT

(4.31)

This way, we guarantee that U is a unit vector, i.e. U 2 = 1. We also see that the time
component of the 4-velocity vector represents the amount of coordinate time that passes
per unit proper time of the object, and the spatial components the spatial distance the
object transverses per unit proper time.

4.1.6

STA multivectors

In space algebra, there were four grades: one scalars, three vectors, three bivectors/pseudovectors and one trivector/pseudoscalar. Now, in STA, we have:
• 1 scalar
• 4 vectors
• 6 bivectors
• 4 trivectors/pseudovectors
• 1 tetravector/pseudoscalar.
Note that we have started calling trivectors and tetravectors pseudovectors and pseudoscalars respectively. This is because there are three trivectors and one tetravector in
four dimensions, so the tetravector takes the role of the pseudoscalar and the trivector
takes the role of the pseudovector. Elements of the individual grades can be represented
by fully antisymmetric tensors as follows:
• scalar a = a
75

## PDF page 77

1

γ10

γ0

γ1

γ2

γ3

γ20

γ30

γ23

γ31

γ12

γ012 γ023 γ031 γ123
γ0123
Figure 4.2: The multivector pyramid of the spacetime algebra.
• vector v = v µ γµ
• bivector B = 1/2! B µν γµν
• trivector/pseudovector T = 1/3! T µνρ γµνρ
• tetravector/pseudoscalar P = 1/4! P µνρσ γµνρσ .
In general, tensor notation of multivectors works completely analogously to the Cl(3)
case - we just have to exchange Latin space indices (i, j, k, ...) for Greek spacetime indices
(µ, ν, ρ, ...) and remember to use the spacetime metric ηµν whenever we need to raise or
lower an index. For instance, the bivector B formed from the vectors a, b with the GA
expression
B =a∧b
(4.32)
would have the tensor analogue
B µν = 2! a[µ bν] = aµ bν − bµ aν .

(4.33)

If we wanted to interior-multiply a four-vector U = U µ γµ onto this bivector, the expression
C =B·U

(4.34)

C µ = B µν Uν = B µν ηνλ U λ .

(4.35)

would be translated to
In STA, there are six basis bivectors. They can be divided into the so-called hyperbolic
bivectors
γ01 ,
γ02 ,
γ03 ,
and the circular bivectors
γ12 ,

γ23 ,
76

γ31 .

## PDF page 78

γ2

γ0

γ1

γ1

Figure 4.3: A circular bivector γ1 ∧ γ2 and a hyperbolic bivector γ0 ∧ γ1 . Note that the
bivectors on the respective sides are all equal to each other. The inscribed shapes describe
what sort of transformation the bivectors generate (more on that in the next section).
The circular bivectors represent purely spatial two-dimensional areas just like in ordinary
space algebra. The hyperbolic bivectors, however, have no classical equivalent. They represent oriented areas with one axis in the timelike light cone. The “circular”/“hyperbolic”
terminology will become clear soon.
Trivectors represent oriented three-dimensional volumes, but now, there is more than
one possible orientation. For instance, the trivector could be purely spatial (γ1 ∧ γ2 ∧ γ3 )
- this would represent a conventional spatial volume that exists for an instant only. We
will call such a trivector a spheroid trivector. A trivector including a timelike axis, e.g.
γ0 ∧ γ2 ∧ γ3 , would represent a spatial area existing for a finite amount of time. We will
call such a trivector a hyperboloid trivector. In total, there are four basis trivectors in
STA, so every possible trivector can be interpreted as the volume orthogonal to a vector
in four dimensions. For this reason, we also call the STA trivectors pseudovectors.
Specifically:
• spheroid trivectors ⇒ timelike pseudovectors (for instance T = Iγ0 )
77

## PDF page 79

• hyperboloid trivectors ⇒ spacelike pseudovectors (for instance T = Iγ1 )
Finally, there is only one tetravector in STA - for this reason, we call STA tetravectors
pseudoscalarars. We conventionally define the unit pseudoscalar as
I = γ0 ∧ γ1 ∧ γ2 ∧ γ3 .

(4.36)

Note that we could in principle also have choosen a different order - for instance γ0132 =
−I. Choosing either +I or −I as the unit pseudoscalar amounts to choosing an orientation
of the space we are working with (either right-handed or left-handed).
The STA pseudoscalar anticommutes with vectors, commutes with bivectors and anticommutes with trivectors:
Iγµ = −γµ I
Iγµν = γµν I
(4.37)
Iγµνρ = −γµνρ I

4.1.7

A note on the Dirac gamma matrices

Those who have already studied the Dirac equation will have probably recognized the
notation we have introduced in this section. The Dirac gamma matrices are conventionally defined in terms of the Pauli matrices σi as
(
)
0 12×2
γ0 =
12×2
0
)
(
(4.38)
0 −σi
.
γi =
σi 0
They are just a matrix representation of the spacetime algebra, similar to how the Pauli
matrices are a representation of the space algebra5 . Any expression composed of sums
and products of Dirac matrices can be interpreted as an STA multivector. Similarly to
Wolfgang Pauli, Paul Dirac himself did not realize the geometric significance of these
matrices - this connection was made by David Hestenes.

5

To be precise, they represent the complexified spacetime algebra, in which the coefficients of k-vectors
are complex number-valued. The reason for that is that Dirac fermions are naturally charged, i.e. exhibit
U (1) gauge invariance - and complex numbers are precisely what is needed to represent the U (1) group.

78

## PDF page 80

4.2

Spacetime rotations

In this section, we are going to learn how to describe Lorentz transformations in geometric
algebra. To emphasize the geometric nature of them, we are going to use a slightly different terminology. Conventionally, Lorentz transformations are divided into “rotations”
and “Lorentz boosts”. However, we are going to see that in spacetime algebra, Lorentz
boosts are just a special type of rotation and can be described by rotors. Hence, we will
call the “normal” rotations circular rotations, and Lorentz boosts hyperbolic rotations. Lorentz transformations in general will be referred to as spacetime rotations.

4.2.1

Circular rotations

The circular bivectors γij generate rotations just like their Cl(3) analogues eij . There is
just one small caveat: The spacelike basis vectors square to −1, so the basis bivectors
in STA do not generate positive (counterclockwise), but negative (clockwise) rotations.
Consider the following example: The Cl(3) rotor
1
R = √ (1 + e12 )
2

(4.39)

describes a positive 90◦ rotation along the xy plane:
R̃e1 R = e2 .

(4.40)

To translate this rotor to STA, we need to use the circular bivector γ12 . A first guess for
the translation of R into STA might be
1
R = √ (1 + γ12 ) ,
2

(INCORRECT!)

(4.41)

1
(γ1 + γ211 + γ112 + γ21112 ) = −γ2
2

(4.42)

but checking it reveals that
R̃γ1 R =

i.e. the rotor R performs a negative rotation along the xy plane. This is because γ1 and
γ2 square to -1.6 The correct translation of R into STA thus is:
1
R = √ (1 − γ12 ) .
2

(4.43)

This is an important point, so let us emphasize it:
6

This is the reason for why we drew the swirls inside the circular bivector in Figure 4.3 in the clockwise
sense.

79

## PDF page 81

cosh(η)

sinh(η)

η

tanh(η)

η

η

Figure 4.4: The hyperbolic trigonometric functions.
Warning 4.2
The STA circular bivectors γij generate negative rotations. The equivalent of the
spatial bivector eij is the STA bivector −γij = γji , which generates positive rotations.
!
Generally speaking, the STA equivalent of a Cl(3) rotation around some bivector eij
by an angle of θ
(e )
ij
R = exp
θ = cos(θ/2) + eji sin(θ/2)
(4.44)
2
is
( γ )
ij
(4.45)
R = exp − θ = cos(θ/2) − γij sin(θ/2).
2
The bivector exponential works exactly like in the Cl(3) case, because the STA circular
bivectors square to −1 as well. For instance,
(γ12 )2 = γ1212 = −γ1221 = γ11 = −1

(4.46)

Apart from this subtlety, spatial rotations in STA work just as we’d expect based on
our three-dimensional intuition. We will call the rotors and rotations generated by the
circular bivectors γij circular rotations.

4.2.2

Hyperbolic rotations

We have seen that the circular bivectors γij generate circular rotations. In contrast, the
hyperbolic bivectors γ0i generate hyperbolic rotations - conventionally called Lorentz
boosts. We call them hyperbolic rotations to emphasize that boosts really are nothing
but rotations of the time and space dimensions into each other. However, there are
some important differences - for instance, we cannot expect a large enough boost in one
direction to return the system to its original state. In the following, we are going to
examine the differences between the circular rotations and hyperbolic rotations.
Contrary to the circular bivectors, the hyperbolic bivectors square to +1. For instance,
(γ01 )2 = γ0101 = −γ0110 = γ00 = +1
80

(4.47)

## PDF page 82

This means that the power expansion of a bivector exponential now resolves to
∞
(γ ) ∑
(γ0i η/2)n
0i
η =
R = exp
2
n!
n=0
∞
∑

(η/2)n
n!
n=0
(
)
(∞
)
∞
∑
∑ (η/2)2n+1
(η/2)2n
=
+ γ0i
(2n)!
(2n + 1)!
n=0
n=0
=

(γ0i )n

(4.48)

= cosh(η/2) + γ0i sinh(η/2),
where cosh and sinh are the hyperbolic trigonometric functions (see Figure 4.4). They
describe hyperbolic rotations - Figure 4.5 shows how hyperbolic rotations describe bectors
being moved along hyperbolae.
The parameter η is the hyperbolic analogue to the regular, circular angle. We call it
the hyperbolic angle. It is also called the hyperbola parameter, boost parameter,
or rapidity.
Let’s consider the timelike unit vector U = γ0 (i.e. a still-standing object) being
boosted by the hyperbolic rotor
Equation 4.6

Hyperbolic rotation
(γ )
03
η = cosh(η/2) + γ03 sinh η/2.
R = exp
2

(4.49)
π

This is a boost along the z axis, i.e. a hyperbolic rotation in the tz plane. We obtain:
R̃γ0 R = cosh(η)γ0 + sinh(η)γi

(4.50)

Its time component cosh(η)γ0 represents the amount of coordinate time passing per unit
subjective time of the object. The space component sinh(η)γ3 represents the amount of
coordinate distance the object moves along the z axis per unit subjective time. Therefore,
the classical 3-velocity magnitude of the boosted object is
v=

γ3 · (Rγ0 R̃)
sinh η
=
= tanh η.
cosh η
γ0 · (Rγ0 R̃)

(4.51)

This relation describes how the hyperbolic angle relates to the velocity we boost our
reference frame by.
Equation 4.7

Velocity and hyperbolic angle
v = tanh(η)

81

(4.52)
π

## PDF page 83

γj

γ0

v

R̃vR

v
R̃vR
γi

γi

Figure 4.5: The difference between circular rotations and hyperbolic rotations. The vector
v might for instance represent the 4-velocity of an object moving through spacetime. In
the top diagram, the 4-velocity is being rotated along a purely spatial plane, and in the
top diagram, it is being rotated from the time axis to the space axis. In both cases, the 4magnitude v 2 = vµ v µ stays invariant - rotations are magnitude-preserving per definition.
The mathematical way to state this is that both circular and hyperbolic rotations are
elements of the special orthogonal group SO(1, 3).
For small velocities, v ≈ η, but once η becomes very large, v asymptotically approaches
the speed of light c = 1. In other words: The components U 0 , U 3 of the four-velocity can
get arbitrarily large, but the classical speed v = U 3 /U 0 a bystander would measure can’t
exceed c = 1.

4.2.3

Rotations bivectors revisited

In three dimensions, rotations bivectors consisted of three components,
Θ=

1 ij
Θ ei ∧ ej = Θ12 e12 + Θ23 e23 + Θ31 e31 .
2!

(4.53)

Now, in 3+1 dimensions, there are six possible bivectors - three hyperbolic and three
circular - so our new spacetime rotation bivector Ξ (uppercase xi) has six components:
Ξ=

1 µν
Ξ γµ ∧ γν
2!

(4.54)

We can relate this STA bivector to the hyperbolic angles and classical circular rotational
angles:
1
Ξ = η i γ0i − Θij γi ∧ γj
(4.55)
2!
Mind the minus in front of the circular part. This is because the STA circular bivectors
generate negative rotations, as discussed previously.
Our treatment of rotation matrices from the last chapter carries over 1:1 to relativistic bivectors. Previously, we saw how the three generators Ti of SO(3) are just the
82

## PDF page 84

matrix/tensor notations of the bivectors. Now, we have six generators and six matrices
representing them (conventionally denoted Mµν ). However, things get somewhat messy
because we constantly need to raise and lower indices with the spacetime metric ηµν .
Spacetime algebra clearly is the superior formalism here.

83

## PDF page 85

4.3

Relativistic dynamics

Now that we have seen how spacetime transformations work, we will learn how to do
relativistic mechanics in geometric algebra. First, we are going to examine relativistic
acceleration and velocity addition. Then, we are going to learn about the basics of relativistic kinematics and rotor mechanics. As a particularly good example of how spacetime
algebra simplifies calculations, we are going to learn about relativistic orbital angular momentum.

4.3.1

Relative velocities

Classically, the relative velocity between two moving objects is calculated by subtracting
their velocities, but this does not work in special relativity for a simple reason: The
relative velocity between two objects is defined as the velocity of one of the objects as
seen from the reference frame of the second one. Classically, “boosting” an object to
another reference frame just involves subtracting velocities, but as we have seen, we need
to perform a full hyperbolic rotation in special relativity for that.
Let U1 , U2 be the 4-velocities of two observers. Now, we want to calculate the relative
velocity between them. Previously, we have seen that the circular angle θ between two
unit 3-vectors a, b is given by
a · b = cos(θ)
(4.56)
a ∧ b = sin(θ)B,
where B is the unit bivector describing the plane of rotation in which A and B lie:
B=√

a∧b

.

(4.57)

a∧b
.
a·b

(4.58)

−(a ∧ b)2

The angle θ can be reconstructed by calculating:
tan(θ)B =

Hyperbolic angles between two vectors work exactly like this. Given two four-velocity
vectors U1 , U2 with a hyperbolic angle η between them, we can write:
Equation 4.8

Hyperbolic parallelogram equations
U1 · U2 = cosh(η)
U1 ∧ U2 = sinh(η)C,

(4.59)
π

where

U1 ∧ U2
C=√
(U1 ∧ U2 )2

84

(4.60)

## PDF page 86

is the hyperbolic bivector generating the boost that rotates U1 towards U2 (remember
that U1 ∧ U2 squares to a positive number, so we had to flip the sign under the root).
Therefore:
sinh(η)
U1 ∧ U2
=
C = tanh(η)C = |v|C.
(4.61)
U1 · U2
cosh(η)
is a hyperbolic bivector whose magnitude is equal to the classical velocity. We can also
write the bivector |v|C as:
|v|C = vγ0 ,
(4.62)
where v is the spatial classical velocity vector v = v i γi . For simplicity, we are going to
denote this hyperbolic bivector as
v := vγ0 = |v|C.

(4.63)

The formula for the relative velocity bivector now reads
Equation 4.9

Relative velocity bivector
v=

U1 ∧ U2
U1 · U2

(4.64)
π

such that v = |v|. Note that this v can never become larger than c = 1 - just like we’d
expect. Don’t be confused by the boldface v - it is indeed a hyperbolic bivector. We will
explain why we chose this notation soon.

4.3.2

Relativistic acceleration

If we were to deal with non-accelerated objects only, the systems we are studying would
look pretty dull. Therefore, the first problem we need to tackle to do relativistic dynamics
is relativistic acceleration.
The four-acceleration A is defined as the derivation of U by the proper time of the
object.
Equation 4.10

Relativistic acceleration
A = U̇ .

(4.65)
π

A direct consequence of this is that A and U have to be orthogonal to each other:
U2 = 1
d 2
U =0
dT
= U̇ U + U U̇ = 0
= AU + U A = 0
= U · A = 0.
⇒

85

(4.66)

## PDF page 87

γ0
A′′ dT
U ′′
U A dT
γ1

Figure 4.6: Infinitesimal relativistic acceleration. The red hyperbola depicts all possible
values the 4-velocity vector of an object with mass can take (i.e. all vectors U with U 2 = 1.
If we want U to remain on this hyperbola, we need to choose a vector A orthogonal to
U . Note that in hyperbolic geometry, our Euclidean intuition of “orthogonal” does not
work anymore - in this diagram, U ′′ is orthogonal to A′′ just like U is orthogonal to A.
This can be pictured as the requirement that A should only move U along the U 2 = 1
hyperboloid - see Figure 4.6 for a depiction.
We now accelerate a non-moving object U = γ0 with an acceleration A = Ai γi orthogonal to U . After a short proper time dT , this results in:
U ′ = γ0 + AdT.

(4.67)

After this infinitesimal step, U still approximately squares to one and thus is a valid
4-velocity vector:
U ′2 = (U + AdT )2
2
(dT )2
= U 2 + 2U
⏟ ·⏞⏞AdT⏟ + A
⏟ ⏞⏞ ⏟
(4.68)
0
O(dT 2 )

= (γ0 )2 = 1.
However, this scheme does not work out for faster U ′′ ̸= γ0 anymore - then, the new
U and the original A are not orthogonal anymore, so we would need to boost A into the
reference frame of U ′′ = γ0 first (see Figure 4.6). Luckily, there is an easier way to achieve
this.
Consider the acceleration bivector
′′

Equation 4.11

Acceleration bivector
a := A ∧ U = AU.

86

(4.69)
π

## PDF page 88

Again, don’t be irritated yet by the boldface notation - a is indeed a hyperbolic
bivector. If we take the interior product between this bivector and a velocity 4-vector,
we always get the acceleration 4-vector we need to perform an infinitesimal acceleration.
For instance, for U = γ0 and A = aγ3 , we have a = aγ30 and:
a · U = aγ30 · γ0 = aγ3

(4.70)

If we instead want to accelerate an already moving object, for instance
1
U ′′ = √ (2γ0 + γ3 ) ,
3

(4.71)

we would need to use the updated acceleration four-vector
1
A′′ = a · U ′′ = √ (γ0 + 2γ3 ) .
3

(4.72)

It is easy to check that they are orthogonal to each other. The prescription A = a · U
works for all U .
We now remind ourselves that an expression like a · U is basically just an infinitesimal
hyperbolic rotation along the hyperbolic bivector a = aγ30 :
[ a]
,
(4.73)
a · U = − U,
2
Therefore, a 4-vector U infinitesimally accelerated in the direction of a for a time dT
reads
[ a]
′
.
(4.74)
U = U − dT U,
2
This is exactly the infinitesimal rotor transformation law with a hyperbolic bivector.
Therefore, if we accelerate U for a non-infinitesimal time T with a constant acceleration
a, the resulting velocity is given by the full rotor transformation law:
U (T ) = R̃(T )U R(T )

(4.75)

with
( a )
R(T ) = exp − T
( a2 )
(a )
= cosh T + γ03 sinh T .
2
2

(4.76)
(4.77)

The infinitesimal version of this rotor is
a
R(dT ) = 1 − dT + O(dT 2 ).
2
adT
=1+
γ03 .
2

(4.78)
(4.79)

When we apply the full rotor R(T ) to the vector γ0 , we get:
U (T ) = R̃γ0 R = cosh(aT )γ0 + sinh(aT )γ3 .
87

(4.80)

## PDF page 89

We can therefore conclude that the constant acceleration of an object by an acceleration
A for a proper time T is the same as boosting the object with boost parameter η = aT .
We see how the speed of light barrier plays out - both a and T can be arbitrarily large,
such that the hyperbolic angle η can grow arbitrarily large too. However, v = tanh(η) is
bounded to 1 from above and −1 from below.

4.3.3

Relativistic kinematics

The relativistic 4-momentum of an object is given by its 4-velocity multiplied by its mass:
p = mU

(4.81)

The time component of p represents the energy of the object, while the space components
represent the classical 3-momentum. The derivation of 4-momentum by proper time is
called the 4-force, denoted by f :
Equation 4.12

4-force
f = ṗ.

(4.82)
π

Therefore, thinking about 4-forces as “currents” of 4-momentum flowing from one
object to another is perfectly valid. The timelike component of F represents the kinetic
energy flow between them, while the spacelike components are the classical Newtonian
force (and therefore the flow of classical 3-momentum).
With these definitions, it is easy to see that the relativistic version of Newton’s third
law holds:
Equation 4.13

Relativistic Newton’s third law
f = mA.

(4.83)
π

Relativistic angular momentum
In three dimensions, the expression for the angular momentum bivector of a system is
∑
IL =
x(a) ∧ p(a) .
(4.84)
a

where x and p are the position and momentum 3-vectors, respectively. With STA, we
can effortlessly generalize this expression to four dimensions:
Equation 4.14

Relativistic angular momentum
∑
∑
L=
p(a) ∧ x(a) = −
x(a) ∧ p(a)

(4.85)

a

π
88

## PDF page 90

where x and p are the position and momentum 4-vectors. We can split up this L into
a purely hyperbolic bivector N = N i γi0 and a purely circular bivector IL:
L = N + IL

(4.86)

Here, the circular components IL are the conventional 3D angular momentum bivector we
are used to from classical physics. We will call this type of relativistic angular momentum
circular momentum. We had to flip the sign of x ∧ p because the circular bivectors of
the STA describe clockwise and not counterclockwise rotations.
The hyperbolic components N have no direct analogue in classical physics. We will
call them hyperbolic momentum7 . They represent the position of the center of mass
of the system at the time t = 0. To see why, we remind ourselves that the hyperbolic
components of L are formed from the wedge of the time components of x and the space
components of p, and vice versa:
∑
xi(a) p0(a) − x0(a) pi(a)
(4.87)
N i = Li0 =
a

For a slow (non-relativistic) object, x0 = t and p0 = m. We therefore obtain
∑
N i = Li0 =
m(a) xi(a) − tpi(a)

(4.88)

a

We see that at t = 0, this is just the expression for the center of mass of the system
multiplied by the total mass8 :
∑
1 ∑
m(a) xi(a)
(4.89)
m(a) xi(a) =
N i = M (xCoM )i = M
M a
a
∑
where M = a m(a) is the total mass of the system.
However, when the total momentum of the system is not equal to zero, the center
of mass will move over time. In fact, the time derivative of M xCoM is just the total
momentum of the system:
∑
∑
∑
i
m(a) ẋi(a) =
m(a) v(a)
=
p(a) .
(4.90)
Ṅ i = M ẋiCoM =
a

a

a

So in order to calculate the “original” (t = 0) center of mass, we subtract the total
momentum times the time from the current center of mass:
∑
N i = M xiCoM,t=0 = M xiCoM − t
pi(a)
(4.91)
a

=

∑

m(a) xi(a) − tpi(a) ,

(4.92)

a
7

Sometimes, they are also referred to as the “dynamic mass moment”
The unit of the hyperbolic momentum therefore is position times mass. In natural units, mass
is energy, and energy E = p0 is momentum in the direction of time. Thus, hyperbolic and circular
momentum have the same units.
8

89

## PDF page 91

which is just the expression for the hyperbolic momentum components N i = L[i0] . Note
that this is a conserved quantity - it doesn’t change over time. In fact, this makes perfect
sense in light of Noether’s theorem too - just like the regular circular momentum conservation is linked to the symmetry of circular rotations, hyperbolic momentum conservation
is linked to the symmetry of hyperbolic rotations.
It is important to note that when we only apply circular rotations, the hyperbolic and
circular components of L (and any other STA bivector) stay separate. However, once we
apply a hyperbolic rotation, they get mixed. For instance, consider a system of two point
masses orbiting each other in the xy plane with zero net 3-momentum and their center
of mass at x = 0. The angular momentum of such a system would be
L = |L|γ21 .

(4.93)

Once we apply a boost in the y direction with the hyperbolic angle η, this becomes
L = |L|(cosh(η)γ21 − sinh(η)γ01 ).

(4.94)

We see that a part of the circular momentum has been hyperbolically rotated into the
time axis. The resulting hyperbolic momentum describes the original location of the
center of mass. You are encouraged to draw a diagram with the γ0 , γ1 and γ2 axes to
depict this hyperbolic rotation geometrically.9

9

In traditional math, the subject of relativistic angular momentum is notorious for being extremely
complicated. It is often not taught until advanced general relativity.

90

## PDF page 92

4.4

Space-time split

The conventional four-vector formalism for SR and the classical matrix-vector formalism
are two wholly separate algebras. This means that if we want to find the classical equivalent of some given physical law, we need to manually convert the vector expressions
between these two formalisms in addition to taking the low-energy limit.
This is not the case for geometric algebra - there is a very elegant device called the
space-time split, which links the geometric algebras of space and spacetime together
seamlessly. We will derive it based on a couple of observations.

4.4.1

The even subalgebra of Cl(1, 3)

The STA even subalgebra Cl+ (1, 3) is defined as the subset of Cl(1, 3) that only contains multivectors of even grade. This means that while the full STA contains scalars,
vectors, bivectors, pseudovectors and pseudoscalars, the even subalgebra of the STA only
contains scalars, bivectors and pseudoscalars. We call this subset a “subalgebra” because
it is closed - adding or multiplying even multivectors with each other will always result
in even multivectors.
As a “basis” for the even subalgebra, we define the STA bivectors10
Equation 4.15

Even subalgebra basis
σi = γi γ0 .

(4.95)
π

such that:
σi = γi0
σij := σi σj = −γij
σ123 := σ1 σ2 σ3 = γ0123 = I.

(4.96)

We see that by multiplying the σµ bivectors with each other, we can span the whole even
subalgebra Cl+ (1, 3). In total, we get:
• 1 scalar
• 3 hyperbolic bivectors σi
• 3 circular bivectors σij
• 1 pseudoscalar σ123
Furthermore, the following anticommutation relation holds:
σi σj + σj σi = 2δij
10

(4.97)

They have nothing to do with the Pauli matrices - the notation just happens to be the same because
of a series of historic accidents.

91

## PDF page 93

This looks familiar to us - it is exactly the structure of Cl(3). We can reinterpret the σi
as the vectors of Cl(3) and the σij as the bivectors of Cl(3), and calculate with them as
if they were ei and eij . In mathematical language, we say that Cl+ (1, 3) and Cl(3) are
isomorphic.
Geometrically, we can imagine this as follows: We first single out the spacelike hyperplane of spacetime that is orthogonal to our current γ0 . Hyperbolic bivectors will
intersect with that hyperplane along a line - the vector in question. Circular bivectors, on
the other hand, will completely lie inside the hyperplane. See Figure 4.7 for an intuitive
visualization. This way of reinterpreting the 4D hyperbolic bivectors as the 3D vectors
and the 4D circular bivectors as the 3D bivectors is the core of the space-time split.

4.4.2

Splitting bivectors

In fact, interpreting hyperbolic bivectors of the form B = bi γi0 as classical 3-vectors is
not new to us at all:
• When we treated relativistic accelerations, we found that the boosts were generated
by the acceleration bivector a = aU , where a is a purely spatial 4-vector a = ai γi .
This means that we can interpret a = aγ0 = ai σi as a classical 3-vector with the
space-time split. This makes perfect sense - the classical acceleration is a 3-vector.
• When we calculated the relative velocity between two objects, we derived the relative
velocity hyperbolic bivector
U1 ∧ U1
.
v=
U1 · U2
Now, we can see that we have actually derived the formula for the classical velocity
three-vector.
• In our treatment of the relativistic angular momentum, we saw that while the
circular components of L behave like the “normal” 3D angular momentum bivector,
the hyperbolic components L[i0] behave like a classical vector indicating the center
of mass at t = 0. Using the space-time split, we can decompose L into a 3-vector
and a 3-bivector:
1
L = N i σi + ILij σij
2!
Note again that the hyperbolic and circular components of an STA bivector mix as
soon as we perform a hyperbolic rotation. Hence, the space-time split is only useful if we
commit ourselves to our current inertial frame - otherwise, we are forced to treat STA
bivectors as STA bivectors instead of as the sum of a classical 3D vector and bivector.

4.4.3

Splitting vectors

Now that we have seen how we can easily reinterpret STA bivectors as classical vectors,
it is somewhat tempting to try to do that for STA vectors too. For instance, a relativistic
92

## PDF page 94

t

γ20
y

−γ12
x
space-time split
y

σ2
σ12

x
Figure 4.7: The space-time split visualized. We can see how the 4D hyperbolic bivectors
are reinterpreted as 3D vectors, and how the 4D circular bivectors are reinterpreted as
3D bivectors. Note that the equivalent of σ12 is not γ12 , but −γ12 . Intuitively speaking,
this is because σ12 generates positive rotations (equivalently to e12 ), but γ12 generates
negative rotations.

93

## PDF page 95

4-momentum vector p = pµ γµ decomposes two parts when we go back to classical physics:
the energy E = p0 , and the 3-momentum vector p. To obtain them, we calculate:
Equation 4.16

Splitting a four-vector p
pU = E + p

(4.98)
π

where U is the 4-velocity of the observer observing the 4-vector p. Here, the interior
part of the geometric product pU represents the energy of the object in question, while
the exterior part represents the classical 3-momentum. Conventionally, we choose U to
be equal to γ0 (i.e. the current observer). Then, the split is just
pγ0 = p0 + pi σi .

(4.99)

This is a combination of a scalar and a hyperbolic STA bivector, with the latter being
reinterpreted as a classical 3-vector. In general, such quantities are called split vectors.
This vector space-time split perfectly showcases the connection between relativistic
and classical physics: In special relativity, we use 4-vectors, which unify one timelike and
one spacelike quantity. Examples of such pairs include:
• 4-position x = (t, xi ): Time and position
• 4-velocity U = (γ, U i ): Time velocity/time dilation and spatial velocity, where γ is
the Lorentz factor
• 4-momentum p = (E, pi ): Energy and momentum
• 4-force f = (P, F i ): Power and force (energy current and momentum current)
• electromagnetic 4-potential A = (ϕ, Ai ): Electric potential and magnetic vector
potential
• 4-current j = (ρ, j i ): Charge density and current density
• etc.
The core of special relativity is to treat those quantities as components of unified 4-vectors.
Classical physics, on the other hand, splits them up into two separate quantities. The
space-time split for vectors does exactly that: It splits up a single 4-vector, for instance
the 4-momentum vector p, into a sum of a scalar and a classical 3-vector pγ0 = E + p.
To convert back from the classical E + p to a 4-vector, we calculate:
Equation 4.17

Converting the split vector back into a 4-vector
p = (E + p) · U

94

(4.100)
π

## PDF page 96

where again, U is the 4-velocity of the coordinate system in which the classical quantities E and p were measured. For instance, if we performed the measurement in the
reference frame U = γ0 , we convert the split vector E + p to a four-vector p like this:
(E + p) · γ0 = Eγ0 + p · γ0
= Eγ0 + pi σi · γ0
1
= Eγ0 + pi (σi γ0 − γ0 σi )
2
i1
= Eγ0 + p (γi00 − γ0i0 )
2
= Eγ0 + pi γi00 = Eγ0 + pi γi = pµ γµ = p

(4.101)

This procedure allows us to seamlessly link relativistic and nonrelativistic physics
in general - in practice, we can convert a relativistic law into a nonrelativistic one by
inserting γ0 ’s in the right places.

4.4.4

Relativistic acceleration revisited

Now, it is easy to see why we previously defined relativistic 4-acceleration the way we did.
By “constant acceleration”, we meant to say that the classical 3-acceleration a = ai σi as
measured by the accelerated object should be constant thorough the whole process. If the
current 4-velocity is U , this classical 3-acceleration a is equivalent to the 4-acceleration
A = a · γ0 = ai γi .

(4.102)

Hence, the rotor describing an acceleration a which lasts for a proper time T is just
Equation 4.18

Relativistic acceleration rotor
(
)
aT
R(T ) = exp −
.
2

(4.103)
π

In other words: The classical change in 3-velocity ∆v = aT is a 3-vector, but with the
space-time split, we can reinterpret it as an STA hyperbolic bivector. This bivector gives
us the plane of hyperbolic rotation that describes the relativistic acceleration process,
and its magnitude is the hyperbolic angle of this hyperbolic rotation.

95

## PDF page 97

4.5

STA geometric derivatives

In STA, we define the geometric derivative analogously to the 3D case:
Equation 4.19

STA geometric derivative
∂ = γ µ ∂µ

(4.104)
π

Is is sometimes also known as the Dirac operator in quantum field theory. It behaves exactly like the 3D geometric derivative, except for some specialities related to the
hyperbolic structure of spacetime: Most importantly, we had to pull up the index of the
γ µ in (4.5) to contract it with ∂µ . This means that the spacelike basis vectors changed
sign:
γ 0 = γ0
(4.105)
γ i = −γi .
Therefore, our geoemtric derivative is written:
µ

∂ = γ ∂µ = γ0 ∂0 −

3
∑

γi ∂i .

(4.106)

i=1

This might seem like a bug at first, but it is a feature - the STA geometric derivative
perfectly captures the hyperbolic structure of spacetime. For instance, if we square the
geometric derivative:
∂ 2 = ∂ µ ∂µ
(4.107)
This operator is known as the d’Alembertian = ∂ 2 in conventional maths.
The interior derivative of a vector field A = Aµ γµ is:
∂ · A = ∂µ Aµ

(4.108)

It is somewhat comparable to the divergence in 3D, except that it also contains changes
in time. Its main use are conservation equations. To understand this better, we first
consider the space-time split version of the geometric derivative:
Equation 4.20

Geometric derivative with spacetime split applied
∂γ0 = ∂0 − ∂

(4.109)
π

Now, in classical physics, the statement that a charge density ρ together with a current
density j = j i σi is conserved is written as
∂0 ρ = −∂ · j
96

(4.110)

## PDF page 98

The change of the charge density in time should be equal to the influx (negative divergence) of current density. We can rearrange this and substitute ρ = j 0 :
0 = ∂0 ρ + ∂ · j
1
˙
= ∂0 j 0 + (∂j + j̇∂)
2
1
= ∂0 j 0 + ∂i j k (σ i σk + σk σ i )
2
= ∂0 j 0 + ∂i j k δki

(4.111)

= ∂0 j 0 + ∂i j i
= ∂µ j µ
= ∂ · j.
Therefore, in STA, the law of current conservation states that the interior derivative of
the current field is zero:
Equation 4.21

Current conservation law
∂·j =0

(4.112)
π

Any divergence in the spatial directions must be cancelled out by a divergence in the
time direction.
The exterior derivative ∂ ∧ exists too in STA. We shall see how it works in the next
chapter.

97

## PDF page 99

Chapter 5
Electrodynamics
Now, to make a mistake is easy and
natural to man. But that is not
enough. The next thing is to correct
it: When a mistake has once been
started, it is not necessary to go on
repeating it for ever and ever with
cumulative inconvenience.
Oliver Heaviside on natural units,
Electromagnetic Theory (1893)

Chapter summary
• The electromagnetic field bivector F is the bivector denoted by the antisymmetric
rank 2 electromagnetic tensor F µν .
• Electric fields are the hyperbolic components of F . Magnetic fields are the circular
components of F .
• With the space-time split, we can reinterpret the E-fields as 3D vectors. However,
regardless of the space-time split, B-fields are bivectors.
• In GA, the electromagnetic equation reads ∂F = j.
• We can formulate right-chiral and left-chiral plane-wave solutions with the pseudoscalar exponential exp(∓Ik · x), respectively.
• In electrostatics, we can find solutions by using the Green’s function approach.
• Magnetic fields generated by currents and electric fields generated by charges are
two very similar phenomena - but this is obscured by traditional maths.

98

## PDF page 100

• The electromagnetic force <math>f = qF \cdot U</math> is the force exerted on a charged particle by
an electromagnetic field. Hyperbolic EM fields hyperbolically rotate the particle’s
velocity, while circular EM fields circularly rotate the it.
99

## PDF page 101

5.1

Overview

Electromagnetism is one of the most beautiful theories ever discovered - that is, in geometric algebra. In this chapter, we will show how the jumble of vectors, pseudovectors,
tensors, minus signs and Lorentz transformations neatly falls into place once we translate
the maths to geometric algebra.

5.1.1

Traditional formalism for electromagnetism

Traditionally, all physics students start their studies of electrodynamics by learning about
the electric and magnetic “vector” fields E, B and the famous Maxwell equations. The
Maxwell equations can be divided into the homogenous Maxwell equations, in which no
charges or currents appear:
∇·B=0
(5.1)
∇ × E = −∂t B
and the inhomogenous Maxwell equations, which contain the charge density ρ and the
current density j:
ρ
∇·E=
ϵ0
(5.2)
∇ × B = µ0 (j + ϵ0 ∂t E).
Later, when studying relativistic electrodynamics, we conventionally introduce natural
units (c = ϵ0 = µ0 = 0). Furthermore, we learn that E and B are not vectors anymore,
but components of the antisymmetric rank-2 electromagnetic field tensor


0 −E x −E y −E z
E x
0
−B z B y 

(5.3)
F µν = 
y
z
E
B
0
−B x 
E z −B y B x
0
which then obeys the two relativistic electrodynamic equations
∂µ F µν = j ν

(5.4)

[µ

(5.5)

3∂ F

νρ]

=0

Here, (5.4) is equivalent to the two inhomogenous Maxwell equations (5.2). It is called
the inhomogenous electrodynamic equation. Similarly, (5.5) is equivalent to (5.1),
and hence called the homogenous electrodynamic equation. Normally, the factor of
3 is left out - we are using it to foreshadow an important conclusion.
In the conventional approach, there is justification for the form of F µν whatsoever.
Instead, the expression for F µν is just postulated, with the post-hoc justification that
(5.4, 5.5) agree with the four Maxwell equations when all components are written out.
The final tensor formalism is completely devoid of any geometric intuition.

100

## PDF page 102

5.1.2

Geometric formalism for electromagnetism

In the classical EM formalism, the magnetic field B is an axial 3-vector. This means
that the magnetic field normally looks like a vector, but does an additional sign flip
under a parity flip, similar to the angular momentum axial vector. We can easily see this
when considering how a current loop generating a B-field would behave under a reflection
(Figure 5.1). However, in geometric algebra, we have sworn a sacred oath to replace the
concept of axial vectors with the concept of bivectors. Hence, we will stop talking about
“magnetic field vectors B” and instead describe magnetic fields with the bivector
Equation 5.1

Magnetic field bivector
IB = IB

(5.6)
π

i.e. the bivector orthogonal to the original B-field vector.
In contrast, E-fields still are vectors. It is somewhat tempting to add E and IB to
obtain the mixed multivector
F = E + IB
= E i ei +

1 ij
IB eij .
2!

(5.7)

Here, the vector grade of F is the E-field, and the bivector grade is the B-field. IB ij are
the components of the bivector IB.
It might puzzle the reader why we can simply add together the electric and magnetic
field into a single quantity, even though they have two different units. It turns out that
when we use natural units in which m and s are two units for the same quantity such
that c = 1, their units (V /m and T ) are the same. If we weren’t using natural units, we’d
have to write:
F = E + cIB.
(5.8)
Previously, we have learned that we can use the space-time split to reinterpret STA
hyperbolic bivectors as classical vectors, and STA circular bivectors as classical bivectors.
We can also do this the other way around - we reinterpret our newly defined F as an STA
bivector:
Equation 5.2

Electromagnetic field bivector
F = E + IB
1 ij
B σij
2!
1
= E i γi0 − B ij γij
2!
= E i σi +

(5.9)

π
Now, electric fields are hyperbolic STA bivectors, and magnetic fields are circular STA
101

## PDF page 103

e3
e2

e′3

reflection

e′2

e′1

e1

B = Be3

j

j
B = −Be3

IB = Be12

IB = Be12

j

j

Figure 5.1: The behaviour of B-fields under reflections. We see that it makes much more
sense to describe B-fields as bivectors orthogonal to the traditional magnetic “vector” B.
To avoid confusion, we will denote the B-field bivector as IB := IB.

102

## PDF page 104

bivectors. We can see that the components F µν of this bivector are:
F i0 = −F 0i = E i
F ij = −IB ij ,
or, more succinctly in matrix notation,


0 −E 1 −E 2 −E 3
E 1
0
−IB 12 IB 31 

F µν = 
2
12
E
IB
0
−IB 23 
E 3 −IB 31 IB 23
0


0 −E 1 −E 2 −E 3
E 1
0
−B 3 B 2 
.
=
E 2 B 3
0
−B 1 
E 3 −B 2 B 1
0

(5.10)

(5.11)

This is where the electromagnetic field “tensor” F µν comes from. It is just the components
of the STA electromagnetic field bivector F . Its hyperbolic components are the
electric fields, and its circular components are the magnetic fields. With the space-time
split, we can interpret the hyperbolic part as a classical vector, and the circular part as
a classical bivector/pseudovector.

5.1.3

The electrodynamic equation

Next, we are going to translate the electrodynamic equations into geometric algebra.
The index contraction in the inhomogenous electrodynamic equation
∂µ F µν = j ν

(5.12)

is the component representation of the interior product between the vector derivative ∂
and F , or in other words, the interior derivative of F :
∂·F =j

(5.13)

with j = j µ γµ . On the other hand, the index diatraction in 3 ∂ [µ F νρ] = 0 is the exterior
derivative of F :
∂ ∧ F = 0.
(5.14)
The interior derivative ∂ · F yields a vector, while the exterior derivative ∂ ∧ F yields
a trivector. We can therefore simply combine them into a single multivector equation
without losing any information:
Equation 5.3

Electrodynamic equation
∂F = j,

103

(5.15)
π

## PDF page 105

the GA electrodynamic equation. This simplification of all four Maxwell equations
into such a short and beautiful statement perhaps is the main triumph of geometric
algebra. And it’s not shorthand notation - this is the form we are actually going to use
for practical computations in electromagnetism.

5.1.4

A note on differential forms

In exterior calculus, the homogenous and inhomogenous electrodynamic equations read
dF = 0
∗d ∗ F = −j.

(5.16)

The first equation is just the exterior derivative, ∂ ∧ F = 0. The second one is a bit more
difficult to translate, though: We remember the GA translation of the Hodge dual of a
k-vector,
k(k−1)
(5.17)
(∗X) = (−1) 2 IX
Specifically, in geometric algebra, this means that for a vector V , a bivector B, and a
trivector T :
∗V = IV
∗B = −IB
(5.18)
∗T = −IT
Thus, (??) and (5.16) translate to
∂∧F =0
I∂ ∧ (−IF ) = −j

(5.19)

Rewriting the latter equation reveals that:
1 ˙
˙
Ḟ + I Ḟ ∂)
−I∂ ∧ IF = −I (∂I
2
1 ˙
˙
= − (I ∂I
Ḟ + I 2 Ḟ ∂)
2
1 ˙ 2
˙
= (∂I
Ḟ + I 2 Ḟ ∂)
2
1
˙
= − (∂˙ Ḟ − Ḟ ∂)
2
= −∂ · F.

(5.20)

Therefore, (5.16) translates to
∂ · F = j,

(5.21)

in GA, such that the two equations are equivalent to ∂F = j. However, we can directly
see the problem with them - exterior algebra does not have the concept of an interior
derivative, so we have to use two successive Hodge duals to emulate it. Also, in practical
terms, the Hodge dual is very difficult to evaluate by hand because of the abundance of
minus signs in its derivation.
104

## PDF page 106

∇ · E = ϵρ0

∂µ F µν = j ν

∗d ∗ F = −j

∂·F =j

∇ × B = µ0 (j + ϵ0 ∂t E)

∂F = j

∇·B=0
3 ∂ [µ F νρ] = 0

dF = 0

∂∧F =0

∇ × E = −∂t B
Figure 5.2: The electromagnetic equation in its various formulations.

5.1.5

Gauge fields

Electromagnetism is also commonly formulated in terms of a gauge field A = Aµ γµ . In
literature, this is also called the “electromagnetic four-potential” or “gauge potential”. It
is the four-vector made up of the electric potential ϕ and the magnetic vector potential
A = Ai σi :
A = (ϕ + A)γ0
= ϕγ0 + Ai γi
= Aµ γµ .

(5.22)

The electromagnetic field bivector F is derived from A by taking the exterior derivative:
Equation 5.4

Electromagnetic field bivector in terms of the gauge field
F = ∂ ∧ A.

(5.23)
π

In traditional maths, this relation is commonly known in its component form
F µν = 2! ∂ [µ Aν] = ∂ µ Aν − ∂ ν Aµ .

(5.24)

The field strenght F is an unambiguous physical parameter we can measure in a lab
- for instance, we can measure is hyperbolic components with F i0 = E i with voltmeters
and its circular components F ij = −IB ij with Hall sensors. The situation is a bit more
complicated for A, though. We cannot measure e.g. the electric potential A0 = ϕ - we
can just measure differences of ϕ from place to place (these differences are called electric
fields). For instance, the two electric fields ϕ(x) and ϕ′ (x) = ϕ(x) + ϕ0 are physically
identical.
This principle is called gauge symmetry. In its most general form, it states that if
α is some scalar field, the two gauge fields A and A′ = A + ∂α are physically identical.

105

## PDF page 107

This can be seen by calculating the corresponding field strengths:
F =∂∧A
F ′ = ∂ ∧ A′
= ∂ ∧ (A + ∂α)
=∂∧A+∂∧∂∧α
=∂∧A=F

(5.25)

because the double exterior derivative ∂ ∧ ∂∧ is always zero (remember that for a scalar,
∂α = ∂ ∧ α).
Because of the huge variety of gauge fields A representing the same physical field F ,
we commonly use a procedure called gauge fixing to simplify the resulting equations.
The most commoly used gauge fixing is the so-called covariant gauge (sometimes also
called Loren(t)z gauge). It requires that our gauge field A fulfills the condition
∂ · A = 0,

(5.26)

or ∂µ Aµ = 0 in component notation. It turns out that for every gauge field A, we can
find an α such that A′ = A + ∂α fulfills the gauge condition. Such a field A′ is referred
to as gauge-fixed.
In terms of a gauge field A, the electrodynamic equation ∂F = j reads
Equation 5.5

Electrodynamic equation in terms of the gauge field
∂(∂ ∧ A) = j

(5.27)
π

Using ∂ = ∂ · +∂∧, we can rewrite this slightly as
∂(∂ − ∂·)A = j
= ∂ A − ∂(∂ · A) = j
2

(5.28)

In tensor notation, the first term reads
(∂ 2 A)µ = ∂λ ∂ λ Aµ
= ∂λ ∂ λ η µν Aν .

(5.29)

The second term is the gradient of the scalar field ∂ · A:
(∂(∂ · A))µ = (∂(∂ ν Aν ))µ
= ∂ µ (∂ ν Aν ).

(5.30)

Now, we are ready to write (5.27) in tensor form:
(∂λ ∂ λ η µν − ∂ µ ∂ ν )Aν = j µ .

(5.31)

The reason for why this equation looks so complicated is that there is no easy way to
express the geometric derivative in (5.27) in tensor notation.
If we gauge-fix A to the covariant gauge ∂ · A = 0, we know that ∂ ∧ A = ∂A and
hence

106

## PDF page 108

Equation 5.6

Gauge-fixed electrodynamic equation in terms of the gauge field
∂ 2 A = j.

(5.32)
π

Note that ∂ 2 is a fully scalar operator. It is also called the d’Alembertian operator traditionally denoted □ = ∂λ ∂ λ .
This is a very important result - it means that we can treat the different index components of A and j as fully separate:
∂ 2 Aµ = j µ .

(5.33)

This is very useful in the Green’s function approach to solving the differential equations.
We shall soon see why.
Tangent 5.1
It should also be noted that the homogenous electrodynamic equation ∂ ∧ F = 0 is
automatically fulfilled if we define F = ∂ ∧A, because two successive exterior derivatives always yield zero. Viewed slightly differently, the homogenous electrodynamic
equation ∂ ∧ F = 0 is the statement that there is a gauge field A corresponding to
F.
ç

107

## PDF page 109

5.2

Solutions to the electromagnetic equation

Now, we are going to find solutions to the electrodynamic equation. We are first going to
take a look at wave solutions in a vacuum, and then present the Green’s function method
for solving the electrodynamic equation for an arbitrary current density.

5.2.1

Plane-wave solutions

The simplest case of the electrodynamic equation ∂F = j is the vacuum case - the case
where j = 0 everywhere. The resulting equation ∂F = 0 is very easy to solve with a
plane-wave approach. Normally, imaginary numbers are used for this purpose. We are
going to show that the introduction of imaginary numbers is not necessary with GA.
But first, we have to introduce the pseudoscalar exponential exp(Iθ). Because I 2 =
−1, this evaluates to:
exp(Iθ) = cos(θ) + I sin(θ).
(5.34)
We are going to use this exponential to write our plane-wave solutions. We make the
approach
Equation 5.7

Left-chiral plane-wave
F (x) = F0 exp(Ik · x),

(5.35)
π

where F0 is some STA bivector to be determined and k is the 4-wavevector specifying
the direction of propagation of the light:
k = ωγ0 + k i γi .

(5.36)

To check whether this is a solution, we take the geometric derivative:
∂F (x) = ∂F0 exp(Ik · x)
= γ µ ∂µ F0 exp(Ik · x)

(5.37)

The basis bivector F0 is constant. The derivative of the pseudoscalar exponential is
∂µ exp(Ik · x) =

d(k · x) d exp(Iθ)
|θ=k·x = kµ I exp(Ik · x).
dxµ
dθ

(5.38)

Therefore, the geometric derivative of F (x) evaluates to:
∂F (x) = γ µ F0 ∂µ exp(Ik · x)
= γ µ F0 kµ I exp(Ik · x)
= kF0 I exp(Ik · x)

(5.39)

Note that we could shift around the ∂µ just like we’re used to - however, the γ µ had to
stay in place, as vectors do not commute with bivectors.
108

## PDF page 110

We now demand that the vacuum electrodynamic equation holds:
!

0 = ∂F (x) = kF0 I exp(Ik · x)

(5.40)

We now postmultiply both sides with −I exp(−Ik · x) to obtain:
0 = kF0

(5.41)

This already is a very tangible requirement for the basis bivector F0 . But first of all, a
brief detour: If we premultiply this equation with k, we find out that:
0 = k 2 F0 .

(5.42)

k 2 is a scalar quantity multiplied to F0 . If we want the vacuum electrodynamic equation
to be fulfilled, either k 2 or F0 should be zero. We want to describe nonzero waves, so
F0 shouldn’t be zero. Therefore, we know that k 2 = 0, i.e. the wave vector has to be
lightlike.
Now, we are ready to solve kF0 = 0. This equation implies that somehow both
k · F0 = 0 and k ∧ F0 = 0. Doesn’t that mean that k has to be both orthogonal and
parallel to F ?
Not quite! Normally, if we want to check whether two vectors a, b are orthogonal, we’d
take the dot product between them. If it is zero, a · b = 0, we’d normally say that the
two vectors are orthogonal to each other.
Warning 5.1
This scheme to determine orthogonality does not work out anymore for lightlike
vectors. For instance, if k is a nonzero lightlike vector, then k 2 = k · k = 0 - even
though k most certainly is parallel to k.
!
Therefore, the only way we can resolve the apparent contradiction k · F0 = 0 and
k ∧ F0 = 0 is that F0 needs to be of the form
F0 = kA0

(5.43)

where A0 is a vector orthogonal to k, such that F0 is a pure bivector. Then, we know
that:
kF0 = k 2 A0 = 0.
(5.44)
Equation 5.8

General plane-wave solutions

We conclude that our plane-wave approach
F (x) = F0 exp(Ik · x)
is a solution to the vacuum electrodynamic equation ∂F = 0 if
• k is lightlike: k 2 = 0
continues in the next page
109

(5.45)

## PDF page 111

continues from the previous page
• F0 contains k: F0 = k ∧ A0 , with A0 another spacetime vector.
π
All of this might be a little bit too abstract, so let’s derive an explicit example: We
want to derive the solution of an electromagnetic wave propagating in the z direction.
The corresponding wavevector is given by:
k = ω(γ0 + γ3 ),

(5.46)

where ω is the frequency of the wave. An example vector A0 orthogonal to this k is
V =
We obtain the basis bivector

1
γ1 .
ω

F0 = k ∧ A0
= γ10 + γ13
= σ1 + σ31 .

(5.47)

(5.48)

As we can see from the space-time split, this F0 represents an electric field in the x
direction, plus a magnetic bivector field in the zx direction (i.e. a magnetic vector field in
the y direction). We now take a look at what happens if we proceed by one quarter-wave
◦
(90 ), such that k · x = τ /4:
F (x′ ) = F0 exp(Ik · x)
= F0 exp(Iτ /4)
(5.49)
= F0 I.
In our case, this just means that
F (x′ ) = (σ1 + σ31 )I
= σ1 I + σ31 I
= σ23 − σ2 .

(5.50)

We see that the multiplication by the pseudoscalar turns the E-field in the x direction
into a B-field in the yz direction, and the zx B-field into a −y E-field1 . In other words,
◦
after one quarter-wave turn, F0 has been rotated by −90 in the xy plane. The rotation
continues as we’d expect - see Figure 5.3 for a depiction. The electric and magnetic field
follow an upwards spiral in the direction of the propagation. If we stick out the thumb of
our left hand into the direction of the wavevector and form a fist with the remaining four
fingers, they will point along the direction of the spiral which leads us into the direction
of propagation. It is for this reason that we refer to this type of electromagnetic radiation
as left-hand circularly polarized or left-chiral light.
In contrast, the right-chiral wave solutions are given by
1

This multiplication of F by I is the same as the electric-magnetic duality transform F → ∗F in
differential forms language.

110

## PDF page 112

y
x
z

Figure 5.3: The structure of the derived plane-wave solution. We can see how the field
starts out as σ1 + σ13 , and then starts to rotate negatively in the xy plane.
Equation 5.9

Right-chiral plane wave
F (x) = F0 exp(−Ik · x).

(5.51)
π

If we want to describe linear instead of circular polarization, we use a superposition
of the two chiral solutions. Namely,
F (x) = F0

exp(Ik · x) + exp(−Ik · x)
2

(5.52)

describes linear polarization along the axis of the initial electric field, and
F (x) = F0

exp(Ik · x) − exp(−Ik · x)
2

(5.53)

describes linear polarization perpendicular to the initial electric field.
Tangent 5.2
It is important to note that we did not have to introduce complex numbers at
all. Normally, they are ubiquitous, with several disadvantages - for instance, when
calculating the energy density and current of the electromagnetic field, we need to
explicitly remove the imaginary part.
There is a compelling reason for why we were able to remove complex numbers with
such ease: The SO(2) duality symmetry of vacuum electromagnetism. In simple
terms, SO(2) duality symmetry states that if F is a vacuum solution,
∂F = 0,

(5.54)

then F ′ = F eIα is a vacuum solution too,
∂(F eIα ) = 0.

(5.55)

In our derivation, we repurposed this symmetry to rotate around the initial EM
field bivector of our plane wave. In traditional maths, this symmetry is expressed
via the Hodge dual - we’d say that if the 2-form F is a solution, then ∗F is a solution
too. But since ∗F = IF = F I = F eIτ /4 , we can see that this way only allows us to
make quarter-turns in the SO(2) circle. Thus, this way of using SO(2) duality to
describe plane waves is unique to geometric algebra.
ç

111

## PDF page 113

5.2.2

Electrostatics

Electrostatics is the study of electromagnetic fields and currents that are constant in time.
We are first going to solve the electrodynamic equation for constant fields in gauge field
form using Green’s functions, and then derive the corresponding electromagnetic fields.
The electrodynamic equation in gauge field form reads
∂ 2 A = j,

(5.56)

assuming the covariant gauge condition ∂ · A = 0. In the static case, the operator
∂ 2 = ∂02 − ∂ 2

(5.57)

reduces to ∂ 2 = −∂ 2 , such that the electrodynamic equation becomes the electrostatic
equation:
Equation 5.10

Gauge-fixed electrostatic equation
−∂ 2 A = j.

(5.58)
π

As we have assumed that all fields are time-invariant, we can write
A(x) → A(x)
j(x) → j(x)

(5.59)

such that we are dealing with a purely spatial PDE
−∂ 2 A(x) = j(x).

(5.60)

To solve this equation, we are going to take the Green’s function approach. First of
all, we note that this equation is linear - if A1 is a solution for a current j1 and A2 a
solution for j2 , then A1 + A2 will be a solution for j1 + j2 . Therefore, in order to solve
the electrostatic equation for an arbitrary current density j, we are first going to find
solutions Gy (x) to the equation
−∂ 2 Gy (x) = δ (3) (x − y).

(5.61)

Then, the solution to j will be given by:
∫
A(x) = d3 y j(y)Gy (x)

(5.62)

We can show that this is a solution by inserting it into the electrostatic equation:
∫
2
−∂ A(x) = d3 y j(y)(−∂ 2 Gy (x))
∫
(5.63)
= d3 y j(y)δ (3) (x − y)
= j(x)
112

## PDF page 114

Intuitively speaking: It would be somewhat tedious to find the solutions for the electrostatic equation for some arbitrary j. Hence, we decompose j into lots of infinitesimal
and similar-looking fragments. It is very easy to find the solution Gy (x) for these fragments and then join them together with an integral to find the total solution for j.
Now, we just need the expression for Gy (x). We already know that the Green’s
function for a Laplacian equation is given by:
Equation 5.11

Electrostatic Greens’s function
Gy (x) =

1
1
.
2τ |x − y|

(5.64)
π

Therefore, the explicit expression for the solution of the electrostatic equation is given
by
Equation 5.12

Solution of the electrostatic equation
∫
1
j(y)
A(x) =
d3 y
2τ
|x − y|

(5.65)
π

If we want to find the corresponding electromagnetic field, we take the exterior derivative:
∫
1
j(y)
F (x) =
d3 y ∂ ∧
.
(5.66)
2τ
|x − y|
We now simplify the integrand. First, we evaluate:
( )
( )
1
1
d |r|
d |r|
d|r|
=
i
dr
d|r| dri
( )
√
1
d |r|
d r2 dr2
=
(5.67)
d|r| dr2 dri
1 1
= − 2 √ 2ri
r 2 r2
ri
=− 3
|r|
Therefore, defining r = x − y and r = rγ0 such that r0 = 0:
∂∧

j(y)
j(y)
= γ µ ∧ ∂µ
|r|
|r|
j(y)
= −γ µ ∧ rµ 3
|r|
r ∧ j(y)
=−
.
|r|3
113

(5.68)

## PDF page 115

We therefore obtain the law
Equation 5.13

Solution of the electrostatic equation in EM bivector form
∫
1
r ∧ j(y)
F (x) = −
d3 x
.
(5.69)
2τ
|r|3
π

This formula unites both the Biot-Savart law for magnetic fields generated by spacelike currents and the corresponding law for electric fields generated by timelike currents
(charges). This completely unified description of electric and magnetic fields allows us to
easily see that they are the same phenomenon. If you’re confused by this, you may wish
to ponder Figure 5.4 and 5.5.

114

## PDF page 116

γ0

γ0

j

F = ∂ ∧ A = − r∧j
|r|3

j
γ2

j
A = |r|

γ2

γ1

γ1

γ2

γ1

Figure 5.4: The electric field generated by a timelike current (aka charge). The gauge
field vectors point in the same spacetime direction as the current and falls off with 1/r.
The electromagnetic field bivectors point in the direction of the current with one axis,
and away from the current with the other axis. They fall off with 1/r2 . Classically, this
hyperbolic F -field is interpreted as a vector field (see lower diagram).

115

## PDF page 117

γ3

γ3

j

F = ∂ ∧ A = − r∧j
|r|3

j
γ2

j
A = |r|

γ2

γ1

γ1

γ3
j
γ3

B
γ1

Figure 5.5: The magnetic field generated by a spacelike current. We can see that magnetic
fields and electric fields are two sides of the same coin - namely, circular and hyperbolic
electromagnetic field vectors, respectively. This relationship gets obscured by the fact
that B-fields are conventionally mistakenly interpreted as vectors instead of bivectors,
and that the time axis is projected out in the E-field case.

116

## PDF page 118

5.3

The electromagnetic force

Electromagnetic fields exert forces on charged particles. Conventionally, this force is
divided in two parts:
• The electric or Coulomb force, exerted by electric fields on charged particles: F = qE
• The magnetic or Lorentz force, exerted by magnetic fields on moving particles:
F = qv × B.
In traditional math, these two expressions look like they have little in common. However, in this section, we are going to see that the electric and magnetic forces are just two
sides of the same coin.

5.3.1

Reformulation of the electric and magnetic force in STA

Conventionally, the electric force is given by
Fe = qE.

(5.70)

This is a classical 3-vector expression. To build a relativistically covariant expression, we
apply a reverse space-time split and post-interiormultiply with γ0 :
Fe · γ0 = qE · γ0

(5.71)

We leave the right-hand side untouched, because the electric field is supposed to be the
hyperbolic bivector
E = E i σi = E i γi0 .
(5.72)
When we resolve the product on the left-hand side, we obtain the 4-force fe = Fe · γ0 =
(Fe )i γi . We therefore obtain the following STA expression for the electric force:
fe = qE · γ0

(5.73)

Now, to the magnetic force. In traditional vector algebra, it is given by
Fm = qv × B.

(5.74)

First of all, we need to untangle the cross product. We know that
v × B = −I(v ∧ B)

(5.75)

The magnetic field “vector” B is given by B = −IIB. Therefore,
v × B = −I(v ∧ (−IIB))
= I(vIIB − IIBv)
= IvIIB − I 2 IBv
= −vIB + IBv
= IB · v
117

(5.76)

## PDF page 119

We therefore arrive at the nonrelativistic magnetic force law
Fm = qIB · v.

(5.77)

This already allows for a nice geometric interpretation: The magnetic field bivector IB
rotates the velocity along its own plane.
To make this law relativistic, we again post-interiormultiply with γ0 . Note that because Fm ∧ γ0 = 0, we can just postmultiply with the geometric product:
fm = Fm γ0 = q(IB · v)γ0
= q(IBv − vIB)γ0
= q(IBvγ0 − vIBγ0 )

(5.78)

IB does not have any time components, so it commutes with γ0 :
fm = q(IBvγ0 − vγ0 IB)
= q(IBv − vIB)
= qIB · v

(5.79)

where v = v i γi is the spacelike part of the non-relativistic 4-velocity. Remember that for
small v = v i σi , the corresponding 4-velocity is given by:
U = γ0 + v = γ0 + v i γi + O(v 2 )

(5.80)

We can therefore conclude that we’d need to add an extra γ0 into (5.79) to obtain the
four-velocity. Luckily, we can just get this if we combine it with the electric force law to
a single electromagnetic force law:
fem = fe + fm
= qE · γ0
= q(E · γ0 + IB · v)

(5.81)

Now, we can use that E · v is on the order of 1/c2 and IB · γ0 = 0 to rewrite this as:
fem = q(E + IB) · (γ0 + v)

(5.82)

Inserting the relations F = E + IB and U ≈ γ0 + v yields:
Equation 5.14

Electromagnetic force law
fem = qF · U

(5.83)
π

This is the electromagnetic force law. Some of you might recognize it from special
relativity - the conventional tensor notation is
µ
fem
= qF µν Uν .

(5.84)

Again, we see how geometric algebra gives this abstract tensor equation a geometric
meaning.
118

## PDF page 120

5.3.2

Geometric interpretation

We can reformulate the electromagnetic force law to look like the infinitesimal rotor
transformation law:
q
f
= F ·U
U̇ =
m [m
]
q
(5.85)
=
F, U
2m
[
q ]
F .
= − U,
2m
Viewed like this, electric fields (hyperbolic EM fields) generate hyperbolic rotations
of U , and magnetic fields (circular EM fields) generate circular rotations of U . This is
exactly what we are used to:
• electric fields accelerate, i.e. hyperbolically rotate particles,
• magnetic fields force them on circular cyclotron motion trajectories, i.e. circularly
rotate them.
Warning 5.2
There’s just one small caveat: the electromagnetic force law (5.83) acts on U from
the left side, while the rotor transformation law acts on U from the right side.
This is the reason for the minus sign in (). We have to pay attention to it: If the
particle is positively charged, the rotation generated by the electromagnetic force
is opposite to the rotation the bivectors F consists of generate. See Figure 5.6 for
an illustration.
!
Integrating (5.3.2) yields the rotor
( q
)
L(T ) = exp −
FT
2m
such that the velocity of the particle after the proper time T is
U (T ) = L̃(T )U0 L(T ).

(5.86)

(5.87)

If F only has a hyperbolic part (F = E = E i σi = E i γi0 ), this will lead to uniform
acceleration:
)
( q
FT
L(T ) = exp −
( 2m
)
q
= exp −
ET
(5.88)
2m
( q
)
(
)
E
q
= cosh
|E|T −
sinh
|E|T ,
2m
|E|
2m
such that, if we apply this rotor to an initially still-standing (U = γ0 ) object:
U (T ) = L̃(T )U L(T )
( q
)
( q
) Ei
= cosh
|E|T γ0 + sinh
|E|T
γi .
2m
2m
|E|
119

(5.89)

## PDF page 121

t

F = E = Eσ2

y
F = IB = Bσ12

x
Figure 5.6: The effects of electric and magnetic fields on a positively charged particle.
Electric fields are hyperbolic bivectors and hyperbolically rotate the four-velocity of the
particle. Magnetic fields are circular bivectors and thus circularly rotate the four-velocity
of the particle.
On the other hand, if F is purely circular (F = IB ij σij ), the particle will be forced
onto a cyclotron motion trajectory:
)
( q
FT
L(T ) = exp −
)
( 2m
q
IBT
= exp −
(5.90)
2m
)
( q
) IB
( q
|IB|T − sin
|IB|T
.
= cos
2m
2m
|IB|
For instance, if IB = Bσ12 and the initial object is moving along the z axis:
1
(5γ0 + 4γ3 )
3(
( (
)
(
) ))
1
q|IB|T
q|IB|T
⇒ U (T ) =
5γ0 + 4 cos
γ1 − sin
γ2
,
3
m
m
U=

a spiral trajectory through spacetime. Mind the minus sign in front of the sine.

120

(5.91)

## PDF page 122

Chapter 6
Geometric calculus
121

## PDF page 123

Chapter 7
Spinors
No one fully understands spinors.
Their algebra is formally understood
but their general significance is
mysterious. In some sense they
describe the “square root” of
geometry and, just as understanding
the square root of 1 took centuries,
the same might be true of spinors.
Michael Atiyah (1929-2019), expert
on spinors

7.1

Matrix representations

In the last couple of chapters, we have encountered two examples of matrix representations: The Pauli matrix representation, which represents the geometric algebra of space
Cl(3), and the Dirac matrix representation, which represents the geometric algebra of
spacetime Cl(1, 3).
At first, it looks like the concept of matrix representation is just a neat trick to
“emulate” geometric algebra with matrix algebra. However, as we will see in this chapter,
the concept of matrix representations is central to describing quantum-mechanical spin
and spinors.
First of all, we should become a little more concrete about what we mean by “matrix
representation”. Representation theory is a rather complicated branch of mathematics
that deserves a lecture of its own. Luckily, we don’t have to do all of it - we only need
complex matrix representations.

122

## PDF page 124

Equation 7.1

Definition of a complex matrix representation

Mathematically, an n-dimensional complex matrix representation is defined as a
bijection that assigns a complex n × n matrix to every multivector:
ρ : Cl(p, q) ↦→ Mat(n × n, C)

(7.1)

This bijection should be an isomorphism - this means that adding and multiplying
these matrices should be equivalent to adding and multiplying their underlying
multivectors:
ρ(A + B) = ρ(A) + ρ(B)
(7.2)
ρ(AB) = ρ(A)ρ(B)
π
The unit scalar 1 in the geometric algebra is always mapped to the identity matrix:
ρ(1) = In×n .

(7.3)

Generally, we can specify the rest of the representation by specifying what matrices
the basis vectors of the geometric algebra map to.

7.1.1

Pauli representation

For instance, the Pauli representation is an isomorphism ρ between Cl(3) and Mat(2 ×
2, C). The basis vectors e1 , e2 , e3 are mapped to the Pauli matrices:
Equation 7.2

Pauli matrix representation
ρ : Cl(3) → Mat(2 × 2, C)
(
)
0 1
ρ(e1 ) =
1 0
(
)
0 −i
ρ(e2 ) =
i 0
(
)
1 0
ρ(e3 ) =
0 −1

(7.4)

π
Using the isomorphism property, we can determine the matrices belonging to the other

123

## PDF page 125

basis k-vectors:

(

)
i 0
ρ(e12 ) = ρ(e1 )ρ(e2 ) =
0 −i
(
)
0 i
ρ(e23 ) = ρ(e2 )ρ(e3 ) =
i 0
(
)
0 1
ρ(e31 ) = ρ(e3 )ρ(e1 ) =
−1 0
(
)
i 0
ρ(I) = ρ(e1 )ρ(e2 )ρ(e3 ) =
0 i

(7.5)

The multivector reverse M̃ can be performed by taking the hermitean conjugate of the
corresponding matrix:
ρ(M̃ ) = ρ(M )† .
(7.6)
This makes perfect sense - the hermitean conjugate of a matrix product reverses its
order, and the matrices ρ(ei ) representing the basis vectors are all hermitean. Therefore,
for instance:
(ρ(e1 )ρ(e2 ))† = ρ(e2 )† ρ(e1 )†
(7.7)
= ρ(e2 )ρ(e1 )
There is another important operation to derive: The scalar grade projection ⟨· · ·⟩.
First, we notice that the trace of the matrices representing multivectors is almost always
zero:
tr(ρ(1)) = 2
tr(ρ(ei )) = 0
(7.8)
tr(ρ(eij )) = 0
tr(ρ(I)) = 2i
This means that we can extract the scalar grade of a multivector by:
Equation 7.3

Scalar grade projection
⟨M ⟩ =

1
Re tr(ρ(M ))
2

(7.9)
π

We can now do calculations with the complex 2x2 matrices as if they were(3D mul)
i 0
tivectors. In fact, you shouldn’t think of e.g. the bivector e12 and the matrix
0 −i
as two separate things - the matrix is simply a different way to write the multivector
e12 . Therefore, once we have chosen a specific matrix representation, we will treat a
multivector M and its matrix representation ρ(M ) as the same thing and write e.g.
(
)
1 0
e3 =
0 −i
(
)
(7.10)
i 0
e12 =
.
0 −i
124

## PDF page 126

We see that the Pauli matrices are just a way of doing calculations with 3D multivectors using matrices. There is, however, an open question: In quantum mechanics, Pauli
matrices are mainly used to operate on spin states - also called spinors - like
( )
a
|ψ⟩ =
,
a, b ∈ C.
(7.11)
b
How do these spin states fit in the picture? They can’t be multivectors, because they’re
not 2 × 2 matrices. We shall find out soon - but first, we will take a brief look at the STA
equivalent of the Pauli representation.

7.1.2

STA representation

The geometric algebra of spacetime Cl(1, 3) has much more elements than the geometric
algebra of space. Thus, we need larger matrices to represent it. This is what the Dirac
gamma matrices are for. They don’t just represent the normal STA, but the complexified STA - the spacetime algebra where multivectors can have complex instead of real
coefficients.
Equation 7.4

Gamma matrix representation of the STA

ρ : Cl(1, 3, C) → Mat(4 × 4, C)




1 0
0 −1


0 1
−1 0 


ρ(γ0 ) = 
ρ(γ1 ) = 
1 0

0 1

0 1
1 0




0 i
−1 0


−i 0
0 1



ρ(γ2 ) = 
ρ(γ
)
=
3
0 −i

1 0

i 0
0 −1

(7.12)

π
Warning 7.1
Some authors also use a slightly different representation in which γ0 is represented
by the matrix
(
)
I2×2
0
(7.13)
0 −I2×2
Our representation is called the Weyl or chiral representation, while the representation using the above matrix for γ0 is called the Dirac representation for historical
reasons. (Yes, the terminology is confusing and messy. It’s because most physicists
can’t be bothered to do their jobs and find good names for the stuff they invent.)
!

125

## PDF page 127

Again, the other basis k-vectors can be constructed by e.g.


−i 0
0 i


γ12 = ρ(γ1 )ρ(γ2 ) = 

i 0
0 −i

(7.14)

Just as in the 3D case, we will say that the multivectors like γ12 and matrices like
ρ(γ1 )ρ(γ2 ) are just two ways to depict the same object and use the notation γ12 for
both. We will thus drop the ρ’s from our notation again.
In the Pauli matrix representation, we could form the multivector reverse by taking
the hermitean conjugate M † of the matrix representing the multivector. This does not
work as easily anymore for the Dirac matrices. If we conjugate them, we find that:
(γ0 )† = γ0
(γi )† = −γi .

(7.15)

This should ring a bell. It is a parity flip with respect to the time axis γ0 . The formula
for conducting such a parity flip on a multivector M is:
Pγ0 (M ) = γ0 M γ0 .

(7.16)

Warning 7.2
Note that in four dimensions, there is more than one possible parity flip. The
statement “We leave the time coordinate invariant and flip the sign of all spatial
coordinates” is dependent on how exactly we define the time coordinate. Observers
with different velocities would therefore define parity flips differently. This is why
we added the γ0 index to P here - it indicates that the parity flip is done w.r.t γ0 .
In other words, the parity flip Pγ0 is the parity flip an observer moving with the
four-velocity U = γ0 would naturally do.
!
We have gotten ourselves into quite some trouble right now! We just wanted to
reverse the order of multiplication and ended up introducing an extra parity flip with
the hermitean conjugate M † . Even worse, this parity flip is not covariant! If we conduct
the hermitean conjugate M † in two different coordinate systems, we will get two different
results, because the parity flip is .
The solution is surprisingly simple: M † reverses the order multiplication M̃ and does
an additional parity flip w.r.t. the current time axis:
M † = γ0 M̃ γ0

(7.17)

We only want the former, so we just conduct another parity flip:
M̃ = γ0 M † γ0 = γ0 (γ0 M̃ γ0 )γ0 .
126

(7.18)

## PDF page 128

This is how we evaluate the multivector reverse when we are working with a matrix
representation. But remember - the actual definition of M̃ does not involve γ0 . What we
are actually doing here is cleaning up the mess of the hermitean conjugate.
Because the hermitean conjugate behaves so weirdly for STA representations, we will
avoid it from now on as best as we can. Just remember - when you are given a matrix
representing an STA multivector and want to take its reverse, first take the hermitean
conjugate, and then do another parity flip with the current γ0 to cancel it out.
The spinors associated with the Dirac gamma matrices have four complex components:
 
a
b

|ψ⟩ = 
a, b, c, d ∈ C
(7.19)
c ,
d
They are not STA multivectors, because they aren’t 4 × 4 matrices. Again, the same
question arises - what are they? How do they fit into the picture of the Dirac matrices
representing multivectors? We can interpret multivectors geometrically, but what about
spinors? How can we picture spinors, geometrically?

7.2

Fundamenentals of spinors

To answer the central question of this chapter “what is a spinor?” - we will first have to
clear up some confusion about matrices and vectors.

7.2.1

What is a vector?

In physics, there are two types of objects that are commonly called “vectors”.
• “Vectors” in the mathematical sense: An element of a vector space, i.e. a space
that has an addition and a distributive scalar multiplication. This type of “vector”
can be anything that behaves linearly in some way - quantum-mechanical states,
functions, spinors, tensors, etc. These “vectors” can be represented by a column of
numbers - for instance, spinors
 
a
b

(7.20)
|ψ⟩ = 
c .
d
• Vectors in the physical sense: Grade-1 elements of a geometric algebra, aka a length
with an orientation. Roughly speaking, arrows pointing through space (spacetime
in STA).

127

## PDF page 129

The second definition is a lot more specific than the first one. So far, we have only used
the second definition in this lecture. To avoid confusion, we are going to rename “vectors”
in the mathematical sense to lineals and vector spaces to linear spaces. It is important
to strictly distinguish between these concepts.
If we make a change in basis U (aka a transformation), our lineals l and matrices M
transform like
l → U −1 l
(7.21)
M → U −1 lU
The sandwich transformation law for matrices ensures that the product of a lineal and a
matrix M l transforms like a lineal:
M l → U −1 M U U −1 l = U −1 (M l).

7.2.2

(7.22)

Going beyond vector matrices and vector tensors

Matrices are linear maps acting on lineals. The first lineals we physicists encounter in our
studies are vectors, and the first matrices we encounter are vector matrices - matrices
that map vectors onto vectors. Such vector matrices describe geometric transformations
like rotations, reflections, scalings, stretchings, or projections. Similarly, all tensors we
have handled so far are vector tensors - tensors over the space of vectors. They transform
under the action of vector matrices, like in (3.73).
But of course, we can easily imagine matrices acting on different kinds of lineals! We
could imagine bivector matrices acting on bivectors. Bivectors are lineals too, and the
inertia tensor actually is such a bivector matrix - it maps the angular velocity bivector
onto the angular momentum bivector.
But most importantly, the spinors are lineals, too. We act on Pauli spinors with
the matrices representing Cl(3) multivectors, and we act on Dirac spinors with the matrices representing Cl(1, 3) multivectors. Thus, we can say that multivectors are spinor
matrices.
The rotor transformation law for a multivector M is:
M → R̃M R.

(7.23)

Now, we remember that RR̃ = 1 for all rotors. This means that
R̃ = R−1 .

(7.24)

We can thus reformulate the rotor law as
M → R−1 M R.

(7.25)

This looks just like the matrix transformation law (7.21). On the one hand, this shouldn’t
surprise us - we’ve seen that multivectors are (can be represented as) spinor matrices, so
it’s natural that they should follow the sandwich matrix transformation law. On the
other hand, this is deeply surprising - we derived the rotor law from purely geometric
considerations! Clearly, we’re onto something big here. So let’s extend this analogy - by
extension, spinors |ψ⟩ transform like

128

## PDF page 130

Equation 7.5 Spinor transformation law
<math>|\psi\rangle \to R^{-1} |\psi\rangle</math>.
(7.26)
<math>\pi</math>
129

## PDF page 131

Acknowledgements
The following people have contributed to the Heidelberg Geometric Algebra lecture so
far:
• Vanessa Alexandra Hollmeier <vhollmeier@physi.uni-heidelberg.de>: Chapters “Introduction”, “Basics of geometric algebra”, “Geometric algebra of space”,
“Tensor notation”, “Electrodynamics”, “Spinors”, technical infrastructure for the
project
• Amir Leidel <amir.leidel@stud.uni-heidelberg.de>: First draft of section on
Cl(2), chapter “Geometric calculus”
• Peleg Bar Sapir <pelegs@gmail.com>: Various improvements

130
