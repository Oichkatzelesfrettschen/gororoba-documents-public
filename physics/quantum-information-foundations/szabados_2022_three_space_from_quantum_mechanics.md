Source: see manifest row of the PDF
PDF sha256: 65126c7b3982b870d7a366e7d9f8e8b09e5af30c6625e02bd882060a1d009623
License: CC-BY-4.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of szabados_2022_three_space_from_quantum_mechanics.pdf

Transcription of `szabados_2022_three_space_from_quantum_mechanics.pdf` in this directory, 34 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-34 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Foundations of Physics (2022) 52:102
https://doi.org/10.1007/s10701-022-00617-2

Three‑Space from Quantum Mechanics
László B. Szabados1
Received: 13 March 2022 / Accepted: 9 August 2022 / Published online: 5 September 2022
© The Author(s) 2022

Abstract
The spin geometry theorem of Penrose is extended from SU(2) to E(3) (Euclidean)
invariant elementary quantum mechanical systems. Using the natural decomposition
of the total angular momentum into its spin and orbital parts, the distance between
the centre-of-mass lines of the elementary subsystems of a classical composite system can be recovered from their relative orbital angular momenta by E(3)-invariant
classical observables. Motivated by this observation, an expression for the ‘empirical distance’ between the elementary subsystems of a composite quantum mechanical system, given in terms of E(3)-invariant quantum observables, is suggested. It is
shown that, in the classical limit, this expression reproduces the a priori Euclidean
distance between the subsystems, though at the quantum level it has a discrete character. ‘Empirical’ angles and 3-volume elements are also considered.
Keywords Spin networks · Spin-Geometry Theorem · Quantum geometry ·
Empirical distance

1 Introduction
In 1966, Penrose suggested the so-called SU(2) spin network as a simple model for
a quantum spacetime (which was published much later only in [1], see also [2, 3,
4]). In this model, angles between elementary quantum mechanical subsystems of
the Universe were expressed in terms of SU(2) Casimir invariants, and, using combinatorial/graphical techniques, he showed that, in the classical limit, these angles
tend to angles between directions in the Euclidean 3-space. The significance of this
result is that the (conformal structure of the) ‘physical 3-space’ that we use as an
a priori given ‘arena’ in which the physical objects are thought to be arranged and

Dedicated to András A. Márton, who is able to transform geometry, physics and philosophy into
poetry: www.​marto​naand​ras.​hu.
* László B. Szabados
lbszab@rmki.kfki.hu
1

Wigner Research Centre for Physics, 114, P. O. Box 49, Budapest 1525, Hungary
Vol.:(0123456789)
1
3

## PDF page 2

102

Page 2 of 34

Foundations of Physics (2022) 52:102

the interactions between them occur is determined by the quantum physical systems
themselves in the classical limit. Later, this result was derived in [5] (and recently
in [6]) in the usual framework of quantum mechanics; and, following [5], it became
known as the Spin Geometry Theorem.
In [5], Moussouris investigated the structure of networks with other symmetry
groups, in particular with the Poincaré group, and derived relations between various
observables of such systems. However, as far as we know, recovering the distance,
i.e. the metric (rather than only the conformal structure of the Euclidean 3-space/
Minkowski vector space) from these models is still lacking.
According to the traditional view, the distance in a metric space is associated
with a pair of points. Thus, the points are usually considered to be the primary
concept. Nevertheless, from a positivistic, or rather a Machian view, the position
in physical 3-space/spacetime in itself is meaningless, and it seems reasonable to
speak only about relative positions of different elementary subsystems of the Universe. This view might suggest to consider the distance, or, in general the relations
between points, to be more fundamental than the points; and that the points themselves should be defined by these relations.
In classical general relativity the spacetime geometry, and, in particular, the distance between the spacetime points, is determined by standard clocks, light rays and
mirrors. However, at the fundamental level no such instruments exist and, also, the
light rays are formed by infinitely many photons in special configurations. Thus,
the instrumentalist approach of defining the spacetime and its properties, using e.g.
some form of ‘quantum clocks’ (see e.g. [7]) at the fundamental level, does not seem
to work.
The philosophy of the present investigations is the positivistic, Machian one of
[1, 2, 3, 4] (that we also adopted in [6]), even from two points of view: first, no a
priori notion of ‘physical 3-space’ or ‘spacetime’ is used. These notions should be
defined in an operational way using only existing (material) quantum subsystems of
the Universe. Second, we speak about angle and distance only between two (elementary) subsystems of the Universe, without introducing ‘directions’ and ‘points’ at all,
e.g. in the form of some ‘position operator’. (For a well readable summary of the
approaches based on the position operators, see [8].)
A potentially viable mathematical realization of such a program could be based
on the use of the algebra of (basic) quantum observables in the algebraic formulation of quantum theory. We consider the quantum system to be specified completely
if its algebra of (basic) quantum observables (and, if needed, its representation, too)
is given. We think that the notion of space(time) and all of its properties should be
defined in terms of the observables of elementary systems. Roughly speaking, an
elementary quantum system is a system whose observables are the self-adjoint elements of the universal enveloping algebra of some ‘small’ Lie algebra, mostly of the
symmetry group acting on the system, and the states of the system belong to the carrier space of some of its unitary, irreducible representations. From our point of view,
su(2) and the Lie algebras e(3) and e(1, 3) of the Euclidean and the Poincaré group,
E(3) and E(1, 3), respectively, are particularly interesting. (This general idea of the
‘G-invariant elementary quantum mechanical systems’ is motivated by that of the
Poincaré invariant systems of Newton and Wigner [9].) The observables belonging

13

## PDF page 3

Foundations of Physics (2022) 52:102

Page 3 of 34 102

to this ‘small’ Lie algebra will be called the basic observables. All the structures
on the algebra of observables may be used in the construction, but additional extra
structures may not. In particular, in the present investigations we use only the general kinematical framework of quantum mechanics, but e.g. no evolution equation
for the quantum states.
The above strategy yields apparently paradoxical results: we have well defined
distance between ‘points’ (or rather straight lines, as we will see) that are not defined
at all in the quantum theory, just like the angles between ‘directions’ that are not
defined either. The ‘true’ geometry of the physical 3-space/spacetime should ultimately be synthesized from the ‘empirical’ distances, angles, etc. introduced via the
quantum observables.
As a first step in this strategy, in [6] we gave a simple proof of (a version of) the
Spin Geometry Theorem by showing how the conformal structure of the Euclidean 3-space can be recovered in this algebraic framework from the basic quantum observables of SU(2)-invariant systems. The present paper provides one more
step: we extend the Spin Geometry Theorem to recover the metric of the Euclidean
3-space by extending the symmetry group from SU(2) to the quantum mechanical
Euclidean group E(3). Here, by quantum mechanical Euclidean group we mean the
semi-direct product of SU(2) and the group of translations in the Euclidean 3-space,
rather than the classical E(3), which is the semi-direct product of SO(3) and the
group of translations.
Technically, the key idea is that the spin part of the total angular momentum of
a composite system is built from the spin of the constituent subsystems and their
relative orbital angular momentum; and the latter, in the traditional formulation,
contains information on the distance between the subsystems. (In fact, already in
the last but one sentence of [1], Penrose raised this possibility in Poincaré-invariant
systems.) This idea can in fact be used to define the distance between the elementary
Poincaré-invariant quantum mechanical systems as well. However, since the latter
is technically different and considerably more complicated, results of those investigations will be published separately. This distance, expressed by E(3)-invariant
classical observables of the composite system, is our key notion, and is called the
empirical distance. The analogous notion in the quantum theory, defined exclusively
in terms of the E(3)-invariant basic quantum observables, is motivated by this classical expression.
The main result of the present paper is that although in quantum theory this
empirical distance has some discrete and highly non-Euclidean character, but in the
classical limit it reproduces the a priori Euclidean distance between the classical
centre-of-mass lines of point particles, i.e. of the straight lines in ℝ3. This can be
considered to be an extension of Penrose’s Spin Geometry Theorem from SU(2) to
E(3)-invariant systems. Therefore, the metric structure of the Euclidean 3-space can
be recovered from the quantum theory in the classical limit. Note, however, that in
the present approach it is the straight lines rather than the points that emerged as the
elementary objects in ℝ3. This feature of the present approach is analogous to that
of twistor theory [10, 11, 12], where, classically, the elementary objects are the (in
general twisting) null lines in Minkowski spacetime with given vorticity or ‘twist’.
The quantity here that is analogous to twist is the spin of the elementary systems.

13

## PDF page 4

102

Page 4 of 34

Foundations of Physics (2022) 52:102

Also, at the quantum level, E(3)-invariant ‘empirical angles’ and ‘empirical 3-volume elements’ are suggested, and it is shown that they reproduce the angles and
3-volume elements in ℝ3 in the classical limit.
In the next section we show how the distance of the centre-of-mass lines of E(3)invariant elementary classical mechanical systems can be expressed by their E(3)invariant classical observables. This expression will provide the basis of our empirical distance in the quantum theory. In Sect. 3, we define E(3)-invariant elementary
quantum mechanical systems and summarize their key properties. In particular, we
determine their centre-of-mass states, which are the closest analogs of those of the
classical systems, which turn out to be given just by the spin weighted spherical
harmonics. Section 4 is devoted to the calculation of the empirical distance, angles
and 3-volume elements. We clarify their classical limit there. Some final remarks are
given in Sect. 5. The paper is concluded with appendices, in which certain technical
details that we used in the main part of the paper are presented.
In deriving the results we use complex techniques developed in general relativity.
The related ideas, notations and conventions are mostly those of [10, 13], except that
the signature of the spatial 3-metric is positive, rather than negative definite. We do
not use abstract indices.

2 
E(3)‑Invariant Classical Systems
2.1 The Definition of the Elementary Systems
A physical system will be called an E(3)-invariant elementary classical mechanical
system if its states can be characterized completely by its linear momentum pa and
angular momentum J ab, a, b, ... = 1, 2, 3; under the action of SO(3), they transform
as a vector and anti-symmetric tensor, respectively, and, under the translation by
𝜉 a ∈ ℝ3, as (pa , J ab ) ↦ (̃pa , J̃ ab ) ∶= (pa , J ab + 𝜉 a pb − 𝜉 b pa ). Then

P2 ∶= 𝛿ab pa pb ,

W ∶=

1 ab
J 𝜀abc pc
2

(2.1)

are invariant with respect to these transformations. Here 𝜀abc is the Levi-Civita alternating symbol, and 𝛿ab is the Kronecker delta. The space of the linear and angular
momenta, endowed with the Lie products

{pa , pb } = 0,

{pa , J bc } = 𝛿 ab pc − 𝛿 ac pb ,

{J ab , J cd } = 𝛿 bc J ad − 𝛿 bd J ac + 𝛿 ad J bc − 𝛿 ac J bd

(2.2)
(2.3)

form the Lie algebra e(3) of E(3). Then P2 and W have vanishing Lie bracket both
with pa and J ab, i.e. they are Casimir invariants. Lowering and raising the Latin indices will be defined by 𝛿ab and its inverse, respectively.1
1
Strictly speaking, the abstract Lie algebra e(3) is the semi-direct sum of a 3-dimensional commutative ideal and so(3) ≈ su(2); and the linear and angular momenta belong to the dual space of these subLie algebras. Hence, the natural positive definite metric 𝛿ab on the commutative ideal (coming from the

13

## PDF page 5

Foundations of Physics (2022) 52:102

Page 5 of 34 102

If pa = 0, then P = 0 and W = 0. In this degenerate case the subsequent strategy
to recover the metric structure of ℝ3 in terms of the basic observables does not seem
to work. Thus, in the present paper, we consider only the pa ≠ 0 case.
Next we form M a ∶= J ab pb, for which it follows that Ma pa = 0, and the identity

P2 J ab = 𝜀abc pc W + M a pb − M b pa

(2.4)

holds. Since the first term on the right of (2.4) is translation invariant while
̃ a = M a + (P2 𝛿 a − pa pb )𝜉 b, this identity is usually interpreted as the
Ma ↦ M
b
decomposition of the angular momentum to its spin (or rather helicity) and orbital
parts, and M a as ( P2-times) the centre-of-mass vector of the system. Note that
𝛿ba − pa pb ∕P2 is the projection to the 2-plane orthogonal to pa. Thus one can always
find a 1-parameter family of translations, viz. 𝜉 a = −M a ∕P2 + upa, u ∈ ℝ, which
̃ a = 0. The resulting total angular momenyields vanishing centre-of-mass vector, M
ab
abc
2
tum is J̃ = 𝜀 pc W∕P , which is just the piece of the angular momentum that
the Casimir invariant W represents. Thus the straight line qa (u) ∶= M a ∕P2 + upa is
interpreted as the trajectory of the centre-of-mass point of the system, and will be
called the system’s centre-of-mass line. For the sake of brevity, we call an elementary system with given P and W a single particle.
Since Ma pa = 0, the set of the pairs (pa , Ma ) is the cotangent bundle T ∗ SP of the
2-sphere SP ∶= {pa ∈ ℝ3 | P2 ∶= pa pb 𝛿ab = const} of radius P in the momentum
space. Clearly, those and only those pairs (pa , Ma ) can be transformed to one another
by an Euclidean transformation whose Casimir invariants P and W are the same. In
particular, (pa , Ma ) can always be transformed into (pa , 0) by an appropriate translation. This single particle state space, T ∗ SP , is homeomorphic to the manifold of the
directed straight lines in ℝ3: a line L is fixed if its direction and any of its points are
specified. Now, the direction of L is fixed by the unit vector pa ∕P , while for a point
of L we choose the point where L intersects the 2-plane containing the origin of
ℝ3 and orthogonal to pa ∕P . This latter is given by M a ∕P2. The scale on these lines
is fixed by P. W is an additional structure on L: it fixes the component of the total
angular momentum vector 12 𝜀abc Jbc in the direction pa ∕P.
2.2 The Empirical Distance of Two Particles
The aim of the present subsection is to express the distance between any two straight
lines of the Euclidean 3-space, considered to be the centre-of-mass lines of elementary classical systems, by E(3)-invariant classical observables.

Footnote 1 (continued)
Killing–Cartan metric on so(3) via the SU(2) group action on it) yields the metric 𝛿ab on the classical
momentum space and the whole tensor algebra over this space. Also, the natural volume 3-form 𝜀abc on
the momentum 3-space comes from the natural volume 3-form on the ideal. The transformation properties of the linear and angular momenta follow from the E(3) multiplication laws. Although, formally,
the dual e(3)∗ of e(3) is not Lie algebra, but it has a natural (linear) Poisson manifold structure with the
bracket operation (2.2)–(2.3). With this structure e(3)∗ is isomorphic with the Lie algebra e(3). Thus, all
these algebraic/geometric structures are manifestations of those on the abstract Lie algebra e(3).

13

## PDF page 6

102

Page 6 of 34

Foundations of Physics (2022) 52:102

Let (pa𝐢 , J𝐢ab ), 𝐢 = 1, 2 , characterize two elementary classical mechanical systems, and let us form their formal union with the linear and angular momenta
pa ∶= pa1 + pa2 and J ab ∶= J1ab + J2ab , respectively. Then P2 and W for the composite
system are defined in terms of pa and J ab according to the general rules (2.1).
Since the Lie algebra of the basic observables of the composite system is the
direct sum of the Lie algebras of those of the constituent subsystems, it is easy to
check that pa and J ab satisfy the commutation relations (2.2)–(2.3), i.e. generate
the Lie algebra e(3); and that P2 , P21 , P22 and also W, W1, W2 are all commuting with
pa and J ab . Hence, P212 ∶= 𝛿ab pa1 pb2 = 12 (P2 − P21 − P22 ) and W12 ∶= W − W1 − W2
are also commuting with pa and J ab . It is P212 and W12 (and their quantum mechanical version) that play fundamental role in the subsequent analysis.
Since P1 P2 ≠ 0 , by (2.1) and (2.4) we obtain

P212 ( M1a M2a )
P2
1
1 ab
+
W
− 2 𝜀abc pb1 pc2 .
J1 𝜀abc pc2 + J2ab 𝜀abc pc1 = W1 12
2 2 +
2
2
P21
P2
P21
P2
(2.5)
Since our aim is to express M1a ∕P21 − M2a ∕P22 from (2.5), for a moment we
assume that the linear momenta of the constituent systems are linearly independent. This requirement is equivalent to the condition P21 P22 > P412. In this case, the
last term on the right in (2.5) is not zero, and then this equation can be solved for
M1a ∕P21 − M2a ∕P22. This solution is
W12 =

(
M2a
P212 ) a b c
P212
1
−
=
−
W
W
−
W
𝜀 bc p1 p2 + u1 pa1 + u2 pa2
2
12
1
P21
P22
P21 P22 − P412
P21
P22
(2.6)
a
for arbitrary u1 , u2 ∈ ℝ. Although its components in the 2-plane spanned by p1 and
pa2 are ambiguous, its component in the direction orthogonal to both pa1 and pa2,
M1a

d12 ∶=

(
P212 )
P212
M2a ) 𝜀abc pb1 pc2
1
−
−
W
W
−
W
=
,
√
√
2
12
1
P21
P22
P21
P22
P2 P2 − P4
P2 P2 − P4

( M1a

1 2

12

1 2

12

(2.7)

is well defined. Similarly, although under a translation M1a ∕P21 − M2a ∕P22 changes as
(M1a ∕P21 − M2a ∕P22 ) ↦ (M1a ∕P21 − M2a ∕P22 ) − (pa1 pb1 ∕P21 − pa2 pb2 ∕P22 )𝜉b, its component
a
in the direction orthogonal both to pa1 and pa2 is invariant. Therefore, the vector d12

defined by the right hand side of (2.6) with u1 = u2 = 0 is uniquely determined, it
is orthogonal both to pa1 and pa2 and points from a uniquely determined point 𝜈21
of the straight line qa2 (u) ∶= qa2 + upa2, u ∈ ℝ, to a uniquely determined point 𝜈12 of
the straight line qa1 (u) ∶= qa1 + upa1, u ∈ ℝ. Its physical dimension is length, and it is
invariant with respect to the P1 ↦ 𝛼P1, P2 ↦ 𝛽P2 rescalings for any 𝛼, 𝛽 > 0. Thus
a
d12
is the relative position vector of the first subsystem with respect to the second;
and d12 is the (signed) distance between the centre-of-mass lines of the two constituent, elementary subsystems. In particular, d12 = 0 holds precisely when the two centre-of-mass lines intersect each other. This can always be achieved by an appropriate

13

## PDF page 7

Page 7 of 34 102

Foundations of Physics (2022) 52:102

a
translation of one of the two subsystems, and hence d12
can always be characterized
by such a translation.
If pa1 and pa2 are parallel, then, as we are going to show, the distance of the two corresponding centre-of-mass lines that do not coincide can be recovered as the limit of the
distances between centre-of-mass lines with non-parallel tangents, i.e. as a limit of classical observables above. Since both the numerator and the denominator in (2.7) are vanishing if pa1 and pa2 are parallel, we should check that these tend to zero in the same order
and that their quotient is finite and well defined. Since the two centre-of-mass lines are
parallel but do not coincide, they lay in a 2-plane, and the vector M1a ∕P21 − M2a ∕P22 is
non-zero, tangent to this 2-plane and is orthogonal to pa1 (and hence to pa2, too). Thus,
there is a unit vector wa which is orthogonal both to pa1 and M1a ∕P21 − M2a ∕P22. Then
let us consider the 1-parameter family of momenta pa2 (𝛼) ∶= P2 (cos 𝛼 va + sin 𝛼 wa ),
where va ∶= pa1 ∕P1 = pa2 ∕P2. In the 𝛼 → 0 limit, pa2 (𝛼) → pa2. A straightforward calculation gives that P21 P22 (𝛼) − P412 (𝛼) = P21 P22 sin2 𝛼, 𝜀a bc pb1 pc2 (𝛼) = P1 P2 𝜀a bc vb wc sin 𝛼
and

W12 (𝛼) − W1
=

P212 (𝛼)
P21

− W2 (𝛼)

P212 (𝛼)
P22

=

)
(
1 ab
J1 𝜀abc wc P2 − J2ab 𝜀abc wc P1 cos 𝛼 + J2ab 𝜀abc pc1 sin 𝛼 sin 𝛼.
2

a
(𝛼) for the centre-of-mass lines with the tangents pa1
Hence, the 𝛼 → 0 limit of d12
a
and p2 (𝛼) is, indeed, the well defined finite value
)
)
( d
( de
de
M1 M2d
1 J1 P2 − J2 P1
f
a
b c
− 2 𝜀def ve wf 𝜀a bc vb wc .
𝜀def w 𝜀 bc v w =
2
P1 P2
P21
P2

Hence, the distance d12 is also well defined and finite. In this case, however, the
points analogous to 𝜈12 and 𝜈21 above are undetermined.
To summarize: we found an alternative expression |d𝐢𝐣 | for the Euclidean distance,
{√
}
D𝐢𝐣 ∶= inf
𝛿ab (qa𝐢 (u𝐢 ) − qa𝐣 (u𝐣 ))(qb𝐢 (u𝐢 ) − qb𝐣 (u𝐣 )) | u𝐢 , u𝐣 ∈ ℝ ,
(2.8)
between the centre-of-mass straight lines of any two elementary classical systems in
terms of E(3)-invariant basic observables of the composite system. Since the latter
is given by the observables of the composite system, we call d𝐢𝐣 the ‘empirical distance’ between the two subsystems. However, if we know the distance between any
two straight lines in ℝ3, then we can determine the Euclidean distance function, too.
Hence, our empirical distance determines the metric structure of ℝ3. We will see
that the analogous empirical distance in quantum theory deviates from the a priori
Euclidean distance D𝐢𝐣, but in the classical limit the former reproduces the latter.

13

## PDF page 8

102

Page 8 of 34

Foundations of Physics (2022) 52:102

2.3 Empirical Angles and Volume Elements
In [6], we considered SO(3)-invariant elementary classical systems in which the
only basic observable was the angular momentum vector J a; and we introduced an
empirical angle between the angular momenta of two subsystems in a well defined
and SO(3)-invariant way. However, in the present case the symmetry group is the
Euclidean group E(3), and although the analogously defined empirical angles would
still be SO(3)-invariant, but they would not be invariant under translations. Thus,
in E(3)-invariant classical systems, the empirical angles between the subsystems
should be defined in terms of quantities that are invariant under translations and
covariant under rotations.
The primary candidate for such quantities is the linear momentum. Thus we
define the ‘empirical angle’ 𝜔12 between pa1 and pa2 according to

cos 𝜔12 ∶=

𝛿ab pa1 pb2
P1 P2

(2.9)

with range 𝜔12 ∈ [0, 𝜋]. This angle is clearly E(3)-invariant, and if e.g. pa1 ∕P1 can be
obtained from pa2 ∕P2 by a rotation with angle 𝛽12 in the 2-plane spanned by pa1 and
pa2, then 𝜔12 = 𝛽12. Thus 𝜔12 reproduces the angles of the a priori Euclidean geometry of ℝ3 (see also [6]). However, as we will see, they split in the quantum theory,
and they coincide only in the classical limit.
The natural volume 3-form 𝜀abc on the space of the translation generators in e(3)
makes it possible to introduce the ‘empirical 3-volume element’ by the 3-volume of
the tetrahedron spanned by three linear momenta, pa1, pa2 and pa3, of a three-particle
system by

v123 ∶=

pa pb pc
1
𝜀abc 1 2 3 .
3!
P1 P2 P2

(2.10)

Just in the case of empirical angles, in quantum theory the corresponding empirical
3-volume element and the 3-volume element of the a priori Euclidean geometry of
ℝ3 do not coincide. They do only in the classical limit (see also [6]). In Sect. 5 we
raise the possibility of another notion of empirical angles and 3-volume elements,
based on the relative position vectors d𝐢𝐣a of three-particle systems, rather than the
linear momenta.

3 
E(3)‑Invariant Elementary Quantum Mechanical Systems
3.1 The Definition and the Basic Properties of the Elementary systems
Adapting the idea of Poincaré-invariant elementary quantum mechanical systems
of Newton and Wigner [9] to the present case, a Euclidean-invariant elementary
quantum mechanical system will be defined to be a system whose states belong

13

## PDF page 9

Page 9 of 34 102

Foundations of Physics (2022) 52:102

to the carrier space of some unitary, irreducible representation of the (quantum
mechanical) Euclidean group E(3); and, in this representation, the momentum and
angular momentum tensor operators, 𝐩a and 𝐉ab , are the self-adjoint generators of
the translations and rotations, respectively. These representations are labelled by
a fixed value P2 ≥ 0 and w, respectively, of the two Casimir operators

𝐏2 ∶= 𝛿ab 𝐩a 𝐩b ,

𝐖 ∶=

1
𝜀 𝐉ab 𝐩c .
2 abc

(3.1)

Thus, the quantum mechanical operators will be denoted by boldface letters.
Clearly, in the states belonging to such representations, the energy 𝐄2 = 𝐏2 + m2
or 𝐄 = 𝐏2 ∕2m of the relativistic or non-relativistic systems of rest mass m, respectively, has a definite value. The commutators of 𝐩a and 𝐉cd are
(
)
[𝐩a , 𝐩b ] = 0, [𝐩a , 𝐉cd ] = −iℏ 𝛿 ac 𝐩d − 𝛿 ad 𝐩c ,
(3.2)

(
)
[𝐉ab , 𝐉cd ] = −iℏ 𝛿 bc 𝐉ad − 𝛿 bd 𝐉ac + 𝛿 ad 𝐉bc − 𝛿 ac 𝐉bd ;

(3.3)

which are just the Lie brackets (2.2)–(2.3) with the pa ↦ 𝐩a and J ab ↦ (i∕ℏ)𝐉ab
substitution.
Nevertheless,

𝐌a ∶= 𝐉ab 𝐩b
is not self-adjoint, because

𝐌†a = 𝐩b 𝐉ab = 𝐌a + [𝐩b , 𝐉ab ] = 𝐌a + 2iℏ𝐩a .
Thus we form 𝐂a ∶= 12 (𝐌a + 𝐌†a ) = 𝐌a + iℏ𝐩a, which is, by definition, the selfadjoint part of 𝐌a, and we consider this to be the centre-of-mass operator. The commutators of these operators can be derived from those for 𝐩a and 𝐉ab above:

[𝐩a , 𝐂b ] = −iℏ(𝛿ab 𝐏2 − 𝐩a 𝐩b ),

[𝐂a , 𝐂b ] = −iℏ𝐏2 𝐉ab .

(3.4)

As a consequence of the definitions,

𝐏2 𝐉ab = 𝐂a 𝐩b − 𝐂b 𝐩a + 𝜀abc 𝐩c 𝐖,

(3.5)

i.e. the analog of (2.4) holds for the operators, too.
The unitary, irreducible representations of the quantum mechanical Euclidean
group has been determined in various different forms (see e.g. [14–17]). The form
that we use in the present paper is given in the appendices of [18, 19], and is based
on the use of the complex line bundles O(−2s) over the 2-sphere SP of radius P in
the classical momentum 3-space, where 2s ∈ ℤ. Here O(−2s) is the bundle of spin
weighted scalars on SP with spin weight s (see e.g. [10]). The wave functions of the
quantum system are square integrable cross sections 𝜙 of O(−2s), and the Hilbert
space of these cross sections will be denoted by HP,s , or simply by H. Thus, SP is
analogous to the mass shell of the Poincaré invariant systems (see e.g. [20]). The

13

## PDF page 10

102

Page 10 of 34

Foundations of Physics (2022) 52:102

radius P is fixed by the Casimir operator 𝐏2 . The spin weight s of 𝜙 is linked to the
value of the other Casimir operator, 𝐖 , in the irreducible representation: w = ℏPs.
The SU(2) part of E(3) acts on SP as pa ↦ Ra b pb , where Ra b is the rotation
a
BB�
AA′
A ̄ A�
matrix determined by U A B ∈ SU(2) via Ra b ∶= −𝜎AA
. Here
� U B U B� 𝜎b
√ 𝜎a are
the three non-trivial SL(2, ℂ) Pauli matrices (including the factor 1∕ 2 ), according to the conventions of [13]. Raising/lowering of the unprimed and primed
spinor name indices, A, B and A′ , B′, are defined by the spinor metric 𝜀AB and its
complex conjugate, respectively. Then the action of SU(2) on the spin weighted
function 𝜙 is 𝜙(pe ) ↦ exp(−2is𝜆)𝜙((R−1 )e c pc ); while that of the translation by 𝜉 a is
simply2 𝜙(pe ) ↦ exp(−ipa 𝜉 a ∕ℏ)𝜙(pe ). Here, exp(i𝜆) is just the phase that appears
in the action, 𝜋 A ↦ exp(i𝜆)𝜋 A, of SU(2) on the spinor constituent 𝜋 A of pa (see [18,
19]). This representation of E(3) is analogous to that of the (quantum mechanical)
Poincaré group on the L2-space of spinor fields on the mass shell [20].
The spin weighted spherical harmonics s Yjm with spin weight s and indices
j = |s|, |s| + 1, ..., m = −j, −j + 1, ..., j are known to form an orthonormal basis in
the space of the square integrable cross sections of O(−2s) on the unit 2-sphere (see
[13, 21]). Hence, the space that the functions s Yjm on SR span is precisely the carrier
space of the unitary, irreducible representation of E(3) labelled by the Casimir invariants P > 0 and w = ℏPs, in which s Yjm ∕P form an orthonormal basis with respect
to the natural L2 scalar product.
In this representation, the action of 𝐩a and 𝐉a ∶= 12 𝜀abc 𝐉bc on 𝜙 is

𝐩a 𝜙 = pa 𝜙,

(3.6)

(
)
p
𝐉a 𝜙 = P� ma ð� 𝜙 − m
̄ a ð𝜙 + s� a 𝜙,
P

(3.7)

ma are the complex null tangents of SP and normalized by ma m
̄ a = 1,
where ma and ̄
′
and ð and ð are the edth operators of Newman and Penrose [21]. The explicit form
ma as well as the operators ð and ð′ in the complex steof the vectors pa, ma and ̄
reographic coordinates (𝜁, 𝜁̄ ) on SP is given in Appendix A.1. The first two terms
together on the right of (3.7) give the orbital part of the angular momentum operator, denoted by 𝐋a, while the third its spin part. Since the spin weighted harmonics
form a basis in HP,s, the basic observables 𝐩a and 𝐉a can also be given by their action
on these harmonics, too. Their matrix elements are calculated in Appendix A.2.
𝐩a and 𝐉a are known to be SO(3) vector operators. Thus, if the unitary operator 𝐔
represents U A B ∈ SU(2) on HP,s, then
𝐔† 𝐩a 𝐔 = Ra b 𝐩b ,

𝐔† 𝐉a 𝐔 = Ra b 𝐉b .

(3.8)

If 𝜙 = exp(−ipa 𝜉 a ∕ℏ)𝜒 , then by (3.6) and (3.7)

)
( i
𝐩a 𝜙 = exp − pe 𝜉 e 𝐩a 𝜒,
ℏ

)
( i
)(
𝐉a 𝜙 = exp − pe 𝜉 e 𝐉a 𝜒 + 𝜀a bc 𝜉 b 𝐩c 𝜒 . (3.9)
ℏ

2
In [19] we defined the translation by multiplication by the phase factor exp(ipa 𝜉 a ∕ℏ). Here, to be compatible with the standard sign convention, we changed the sign in the exponent to its opposite.

13

## PDF page 11

Foundations of Physics (2022) 52:102

Page 11 of 34 102

Hence, for 𝜙 = exp(−ipa 𝜉 a ∕ℏ)𝐔𝜓 ,

⟨𝜙�𝐩a �𝜙⟩ = Ra b ⟨𝜓�𝐩b �𝜓⟩,

⟨𝜙�𝐉a �𝜙⟩ = Ra b ⟨𝜓�𝐉b �𝜓⟩ + 𝜀a bc 𝜉 b Rc d ⟨𝜓�𝐩d �𝜓⟩.
(3.10)
These are just the transformation laws of the classical basic observables under the
action of the classical E(3).
Finally, it is straightforward to derive the explicit form of the centre-of-mass
operator:
(
)
𝐂a 𝜙 = i� P2 ma ð� 𝜙 + P2 m
̄ a ð𝜙 − pa 𝜙 .
(3.11)
This is also an SO(3) vector operator. A detailed discussion of the line bundle
O(−2s) and the derivation of these equations are also given in the appendices of [18,
19].
3.2 The Centre‑of‑Mass States
In this subsection we show that the spin weighted spherical harmonics form a distinguished basis among the orthonormal bases in HP,s in the sense that they are adapted
in a natural way to the basis in the abstract Lie algebra e(3) of the basic quantum
observables (but not to a Cartesian frame in the ‘physical 3-space’). In particular, they
are just the eigenfunctions of the square of the centre-of-mass vector operator, 𝐂a 𝐂a,
they are the critical points of the functional 𝜙 ↦ ⟨𝜙�𝐂a 𝐂a �𝜙⟩, and the expectation
value of the centre-of-mass vector operator in these states is zero. We will calculate
the expectation value of our empirical distance and angle in the states that are obtained
from these special ones by some E(3) transformation.
Using (3.11) and ðpa = ma (see Appendix A.1), by integration by parts it is straightforward to form the centre-of-mass-square operator 𝐂a 𝐂a. It is
(
)
)
(
𝐂a 𝐂a 𝜙 = ℏ2 P2 −P2 ðð� + ð� ð 𝜙 + 𝜙 .
(3.12)
Since the operators 𝐂a are self-adjoint, 𝐂a 𝐂a is a positive self-adjoint operator.
Similar calculations yield the square of the total and the orbital angular momentum
operators:
(
)
)
)
(
(
𝐉a 𝐉a 𝜙 = ℏ2 −P2 ðð� + ð� ð 𝜙 + s2 𝜙 , 𝐋a 𝐋a 𝜙 = −P2 ℏ2 ðð� + ð� ð 𝜙.
Thus 𝐂a 𝐂a, 𝐉a 𝐉a and 𝐋a 𝐋a deviate from one another only by a constant times the
identity operator, and hence, in particular, their spectral properties are the same.
Note also that (ðð� + ð� ð) is just the metric Laplace operator on SP.
First we show that the critical points of the functional 𝜙 ↦ ⟨𝜙�𝐂a 𝐂a �𝜙⟩ on HP,s are
∑
just the combinations of the form 𝜙 = m cm s Yjm of spin weighted spherical harmonics
s Yjm with given j. Using ⟨𝜙�𝜙⟩ = 1, by integration by parts (3.12) gives

13

## PDF page 12

102

Page 12 of 34

Foundations of Physics (2022) 52:102

�
⟨𝜙�𝐂a 𝐂a �𝜙⟩ = �2 P2 P2

�SP

�

�
�
̄ � 𝜙) + (ð� 𝜙)(ð𝜙)
̄
(ð𝜙)(ð
dSP + 1 .

The critical points of this functional with respect to the variations 𝛿𝜙 constrained
by ⟨𝜙�𝜙⟩ = 1 are just the critical points of the functional ⟨𝜙�𝐂a 𝐂a �𝜙⟩ + 𝜆ℏ2 P4 ⟨𝜙�𝜙⟩
with respect to unconstrained variations, where 𝜆 is some real Lagrange multiplier.
The vanishing of the variation of the latter functional yields
)
( �
ðð + ð� ð 𝜙 = 𝜆𝜙.
(3.13)

Thus 𝜆 must be an eigenvalue of the Laplace operator ðð� + ð� ð acting on spin weight
s functions on SP , and then the critical configurations are given by the corresponding
∑
eigenfunctions. These can be determined by expanding 𝜙 as 𝜙 = j,m cjm s Yjm with
complex constants cjm, where j = |s|, |s| + 1, |s| + 2, ... and m = −j, −j + 1, ..., j ; and
using the general formulae (A.7) how the operators ð and ð′ act on s Yjm. Substituting all these into (3.13), we find that 𝜆 = −P−2 (j2 + j − s2 ). Hence, 𝜆 is linked to j,
∑
and the corresponding eigenfunctions have the form 𝜙 = m cm s Yjm. These eigenfunctions are the critical points of the functional ⟨𝜙�𝐂a 𝐂a �𝜙⟩, and the corresponding
critical values are
�
�
�
�
⟨𝜙�𝐂a 𝐂a �𝜙⟩ = ℏ2 P2 1 + j2 + j − s2 ≥ ℏ2 P2 1 + �s� .
(3.14)

The smallest of these corresponds to j = |s|, and the corresponding eigen∑
function is 𝜙 = m cm s Y�s�m, which is holomorphic if s = −|s|, and it is antiholomorphic if s = |s| (see Appendix A.1). Forming the second variation of
⟨𝜙�𝐂a 𝐂a �𝜙⟩ + 𝜆ℏ2 P4 ⟨𝜙�𝜙⟩ at the critical points, one can see that the only minimum
does, in fact, correspond to j = |s|, and all the other critical points are only inflection. Thus the right hand side of (3.14) is the sharp strictly positive lower bound for
the expectation values of 𝐂a 𝐂a.
This analysis shows also that the spectrum of all the operators 𝐂a 𝐂a, 𝐉a 𝐉a and
𝐋a 𝐋a is discrete (as it must be since ðð� + ð� ð is an elliptic differential operator acting on cross sections of a vector bundle over a compact manifold), their eigenvalues,
respectively, are

P2 ℏ2 (1 + j2 + j − s2 ),

ℏ2 (j2 + j − s2 );
∑
and the corresponding common eigenfunctions are of the form m cm s Yjm. These
imply, in particular, that the expectation value of any of these operators is not zero
for s ≠ 0.
ma, we
By integration by parts and using how the edth operators act on pa, ma and ̄
can write
⟨𝜙�𝐂a �𝜙⟩ =i� P2

�SP

=i� P2

�Sp

13

ℏ2 j(j + 1),

�
�
ma ð𝜙 + 𝜙 ðm
̄ a dSP =
𝜙̄ ma ð� 𝜙 + ̄
�
�
̄ a ð𝜙̄ dSP = i� P2
𝜙̄ ma ð� 𝜙 − 𝜙 m

�SP

�
�
pa 𝜙 ð� ð𝜙̄ − 𝜙̄ ðð� 𝜙 dSP .

## PDF page 13

Page 13 of 34 102

Foundations of Physics (2022) 52:102

∑
Since 𝜙 = m cm s Yjm for some given j, by (A.7) we have that
2
̄
̄ � 𝜙) = −(j + s)(j − s + 1)𝜙𝜙∕2P
. Using this and its complex conjugate, finally
𝜙(ðð
we obtain
⟨𝜙�𝐂a �𝜙⟩ = 0.

(3.15)

Thus, the 2j + 1 dimensional subspaces in HP,s spanned by the harmonics s Yjm with
given j are specified e.g. by 𝐂a 𝐂a (or, equivalently by 𝐉a 𝐉a or by 𝐋a 𝐋a) in a natural
way, while the basis in these subspaces, the index m is referring to, is linked to our
choice for the basis in the sub-Lie algebra su(2) ⊂ e(3).
To summarize, {s Yjm ∕P} is not only one of the many L2-orthonormal bases in
HP,s, but it is adapted in a natural way to the centre-of-mass operator, too. Although
the expectation value of 𝐂a is zero in any eigenstate of 𝐂a 𝐂a, the expectation value
of 𝐂a 𝐂a can never be zero, even if s = 0. Its smallest expectation value, which is its
smallest eigenvalue, cannot be made zero e.g. by any translation (in contrast to the
classical case). It corresponds to j = |s|, and the corresponding eigenfunctions,
∑
𝜙 = m cm s Y�s�m, are holomorphic if s = −|s|, and anti-holomorphic if s = |s|. We call
these states the centre-of-mass states. These form a 2|s| + 1 dimensional subspace in
HP,s, and these are the states of the E(3)-invariant elementary quantum mechanical systems that are the closest analogs of the states of the classical systems with vanishing
centre-of-mass vector.

4 The Two‑Particle System
4.1 The Quantum Observables of Two‑Particle Systems
Let us consider two E(3)-invariant elementary quantum mechanical systems, whose
basic quantum observables are 𝐩a𝐢 and 𝐉ab
, 𝐢 = 1, 2. These observables are self𝐢
adjoint operators on H𝐢. The corresponding Casimir operators are denoted by 𝐏2𝐢
and 𝐖𝐢. The Hilbert space of the joint system is H1 ⊗ H2, and we can form the
operators 𝐎1 ⊗ 𝐈2, 𝐈1 ⊗ 𝐎2 ∶ H1 ⊗ H2 → H1 ⊗ H2 for any 𝐎𝐢 ∶ H𝐢 → H𝐢, where 𝐈𝐢
are the identity operators on the respective Hilbert spaces H𝐢. Clearly, 𝐎1 ⊗ 𝐈2 and
𝐈1 ⊗ 𝐎2 are commuting. In particular, 𝐏21 ⊗ 𝐈2, 𝐖1 ⊗ 𝐈2, 𝐈1 ⊗ 𝐏22 and 𝐈1 ⊗ 𝐖2 are
Casimir operators of the composite system.
Analogously to (3.1), we form
(
)(
)
𝐏2 ∶= 𝛿ab 𝐩a1 ⊗ 𝐈2 + 𝐈1 ⊗ 𝐩a2 𝐩b1 ⊗ 𝐈2 + 𝐈1 ⊗ 𝐩b2 =
(4.1)
= 𝐏21 ⊗ 𝐈2 + 𝐈1 ⊗ 𝐏22 + 2𝛿ab 𝐩a1 ⊗ 𝐩b2 ,

( ab
)( c
)
1
𝐉 ⊗ 𝐈2 + 𝐈1 ⊗ 𝐉ab
𝐩1 ⊗ 𝐈2 + 𝐈1 ⊗ 𝐩c2 =
𝜀
2
2 abc 1
(
)
1
ab
c
= 𝐖1 ⊗ 𝐈2 + 𝐈1 ⊗ 𝐖2 + 𝜀abc 𝐩c1 ⊗ 𝐉ab
2 + 𝐉1 ⊗ 𝐩 2 .
2

𝐖 ∶=

(4.2)

13

## PDF page 14

102

Page 14 of 34

Foundations of Physics (2022) 52:102

⊗ 𝐈2 and 𝐈1 ⊗ 𝐉ab
Although 𝐖 does not commute with any of 𝐩a1 ⊗ 𝐈2, 𝐈1 ⊗ 𝐩a2, 𝐉ab
,
1
2
the observables of the subsystems in the algebra of observables of the composite
⊗ 𝐈2 and 𝐈1 ⊗ 𝐉ab
system, and 𝐏2 does not commute with 𝐉ab
, but both 𝐖 and 𝐏2
1
2
a
a
ab
ab
do commute with 𝐩1 ⊗ 𝐈2 + 𝐈1 ⊗ 𝐩2 and 𝐉1 ⊗ 𝐈2 + 𝐈1 ⊗ 𝐉2 , i.e. with the linear and
angular momentum operators of the composite system. Therefore, though 𝐏2 and
𝐖 are not Casimir operators of the composite system, they are commuting with
the generators of the symmetry group E(3), i.e. they are E(3)-invariant. Moreover,
[𝐏2 , 𝐖] = 0 also holds. Hence,
(
)
1 2
𝐏 − 𝐏21 ⊗ 𝐈2 − 𝐈1 ⊗ 𝐏22 = 𝛿ab 𝐩a1 ⊗ 𝐩b2 ,
𝐏212 ∶=
(4.3)
2
𝐖12 ∶= 𝐖 − 𝐖1 ⊗ 𝐈2 − 𝐈1 ⊗ 𝐖2 =

)
(
1
+ 𝐉ab
⊗ 𝐩c2
𝜀abc 𝐩c1 ⊗ 𝐉ab
2
1
2

(4.4)

are also E(3)-invariant and [𝐏212 , 𝐖12 ] = 0 holds. These operators characterize the
relationship between the two subsystems in the composite system, and hence they
will have particular significance for us.
Using the definitions above and the first of (3.4), the identity (3.5) yields
( 2
)
(
)(
)
(
)
𝐏1 ⊗ 𝐏22 𝐖12 = 𝜀abc 𝐩b1 ⊗ 𝐩c2 𝐂a1 ⊗ 𝐏22 − 𝐏21 ⊗ 𝐂a2 + 𝐏212 𝐏21 ⊗ 𝐖2 + 𝐖1 ⊗ 𝐏22 .

(4.5)
Let the two subsystems be elementary, characterized by the Casimir invariants
(P1 , s1 ) and (P2 , s2 ), respectively. Then by (3.6) 𝐏212 is a multiplication operator on
H1 ⊗ H2, and hence, for any 𝜙1 ⊗ 𝜙2 ∈ H1 ⊗ H2, (4.5) gives

𝜀abc pb1 pc2

( 𝐂a

(
𝐂a2 )
( s1
s2 ) 2 )
1
⊗
𝐈
−
𝐈
⊗
𝜙
⊗
𝜙
=
𝐖
−
�
𝐏 𝜙 ⊗ 𝜙2 .
+
2
1
1
2
12
P1 P2 12 1
P21
P22

(4.6)
This is analogous to the classical equation (2.5), and the operators on both sides are
E(3)-invariant. Nevertheless, their physical dimension is momentum times angular
momentum, rather than length. Thus, just as in the classical case (and motivated by
(2.7)), we should consider the component of 𝐂a1 ⊗ 𝐈2 ∕P21 − 𝐈1 ⊗ 𝐂a2 ∕P22 in the direction 𝜀a bc pb1 pc2.
√
This is just (4.6) divided by P21 P22 − (𝛿ab pa1 pb2 )2 , the length of 𝜀abc pb1 pc2, and we
could consider the operator

√

𝜀abc pb1 pc2
P21 P22 − (𝛿de pd1 pe2 )2

(

)
1
1 a
a
𝐂
⊗
𝐈
−
𝐈
⊗
𝐂
2
1
2 .
P21 1
P22

(4.7)

This is a well defined, self-adjoint and E(3)-invariant operator, which is analogous
to the classical expression (2.7). However, in contrast to the classical case, the coefficient under the square root sign in the denominator is not constant. Hence it could
be difficult to use this expression e.g. in the calculation of the expectation values. To
cure this difficulty, using

13

## PDF page 15

Page 15 of 34 102

Foundations of Physics (2022) 52:102

�

�
1
dk
1 3 5 2k − 1
1 1 ⋅ 2 ⋅ 3 ⋅ 4 ⋯ (2k − 1) ⋅ (2k)
1 (2k)!
(0) =
,
⋯
= k
= 2k
√
2 2 2
2
2 ⋅ 4 ⋯ (2k)
k!
dxk 1 − x
2
2

√
for the Taylor expansion of 1∕ P21 P22 − (𝛿ab pa1 pb2 )2 we obtain
√

1
P21 P22 − (𝛿ab pa1 pb2 )2

=

∞
a b
1 ∑ 1 (2k)! ( p1 p2 )2k
𝛿
.
P1 P2 k=0 22k (k!)2 ab P1 P2

(4.8)

Using this and recalling that 𝐏212 is a multiplication operator, the above candidate
for the ‘distance operator’ becomes an expression of the positive powers of 𝐖12
and 𝐏212. Nevertheless, now the infinite series makes the application of the resulting
expression difficult in practice. Thus, although in principle this might yield a well
defined operator for the distance of the two subsystems, and certainly it would be
worth studying this, in the present paper we choose a different strategy and look for
only the ‘empirical distance’. This is the one that we followed in [6] in defining the
angle between the angular momentum vectors of SU(2)-invariant elementary quantum mechanical systems.

4.2 The Empirical Distance
Based on equation (4.6) and the discussion above, we define the empirical distance
of the two E(3)-invariant elementary quantum mechanical systems (characterized by
their Casimir invariants (P1 , s1 ) and (P2 , s2 )) in their states 𝜙1 and 𝜙2, respectively, by
�
�
⟨𝜙1 ⊗ 𝜙2 �𝐖12 − � s1 ∕P1 + s2 ∕P2 𝐏212 �𝜙1 ⊗ 𝜙2 ⟩
.
d12 ∶=
�
(4.9)
P21 P22 − ⟨𝜙1 ⊗ 𝜙2 �𝐏412 �𝜙1 ⊗ 𝜙2 ⟩

d𝐢𝐣 can, in fact, be defined in any state of the composite system consisting of any
number of elementary systems, 𝐢, 𝐣 = 1, ⋯ , N , represented by a general density
operator 𝜌 ∶ HP1 ,s1 ⊗ ⋯ ⊗ HPN ,sN → HP1 ,s1 ⊗ ⋯ ⊗ HPN ,sN , not only in pure tensor
product states of a bipartite system. However, if the density operator represents a
pure vector state which is an entangled state of the constituent systems, or if it is a
genuine mixed state of the composite system, then the state of the constituent systems would necessarily be mixed; moreover the empirical distance d𝐢𝐣 would depend
on the state of the subsystems other than the 𝐢 ’s and the 𝐣’s. Hence, in these cases
the interpretation of d𝐢𝐣 would not be obvious. Therefore, in the present paper, we
assume that the states of the composite system are tensor products of pure vector
states of the constituent systems; and hence, without loss of generality, the composite system could be assumed to consist only of two subsystems.
In this subsection, we calculate d12 using (4.9) and discuss its properties at the
genuine quantum level. The classical limit will be considered in subsection 4.4.
Let us write 𝜙1 = exp(−ip1e 𝜉1e ∕ℏ)𝐔1 𝜓1, where 𝐔1 is the unitary operator on
HP1 ,s1 representing an SU(2) matrix U1A B and 𝜉1e is a translation. Or, in other words,

13

## PDF page 16

102

Page 16 of 34

Foundations of Physics (2022) 52:102

𝜙1 is considered to be obtained from the state 𝜓1 by some E(3) transformation.
The state 𝜙2 is assumed to have the analogous form. Then by (4.4), (3.8) and
(3.10) the first term in the numerator in (4.9) is
�
�
⟨𝜙1 ⊗ 𝜙2 �𝐖12 �𝜙1 ⊗ 𝜙2 ⟩ = 𝜉1a − 𝜉2a 𝜀abc (R1 )b d ⟨𝜓1 �𝐩d1 �𝜓1 ⟩(R2 )c e ⟨𝜓2 �𝐩e2 �𝜓2 ⟩+
�
�
b
a
b
a
⟨𝜓
�𝜓
⟩
.
�𝜓
⟩⟨𝜓
�𝐩
�𝜓
⟩
+
⟨𝜓
�𝐉
�𝜓
⟩⟨𝜓
�𝐉
R
)
�𝐩
+ (R−1
2 2 2
1 1 1
2 2 2
2 ab
1 1 1
1
(4.10)
In a similar way, the relevant factor in the second term of the numerator and the nontrivial term in the denominator, respectively, are

⟨𝜙1 ⊗ 𝜙2 �𝐏212 �𝜙1 ⊗ 𝜙2 ⟩ = (R−1
R2 )ab ⟨𝜓1 �𝐩a1 �𝜓1 ⟩⟨𝜓2 �𝐩b2 �𝜓2 ⟩;
1

(4.11)

⟨𝜙1 ⊗ 𝜙2 �𝐏412 �𝜙1 ⊗ 𝜙2 ⟩ = (R−1
R2 )ab (R−1
R2 )cd ⟨𝜓1 �𝐩a1 𝐩c1 �𝜓1 ⟩⟨𝜓2 �𝐩b2 𝐩d2 �𝜓2 ⟩.
1
1
(4.12)
Thus, it is only 𝜉1a − 𝜉2a, i.e. only the relative ‘position’ of the two systems, that matters in the empirical distance. We will see that, in a similar way, it is only the relative ‘orientation’ of the two subsystems that matters. Next we specify the states 𝜓1
and 𝜓2.
If 𝜓 = s Yjm ∕P , then by (A.19), (A.22), (A.25) and (A.28)–(A.30)
⟨𝜓�𝐩a �𝜓⟩ = 𝛿3a P

ms
,
j(j + 1)

⟨𝜓�𝐉a �𝜓⟩ = 𝛿3a ℏm.

(4.13)

Thus, roughly speaking, in the state s Yjm ∕P both the linear and angular momenta
point in the ‘z-direction’ (with respect to the basis in the momentum space). Using
(A.18)–(A.26), a direct calculation gives that
�
P4
−3s2 m2 +
⟨s Yjm �𝐩1 𝐩1 �s Yjm ⟩ = ⟨s Yjm �𝐩2 𝐩2 �s Yjm ⟩ =
j(j + 1)(2j − 1)(2j + 3)
�
�
�
��
+ j(j + 1) s2 + m2 + j(j + 1) j2 + j − 1 ,

�

P4
6s2 m2 −
j(j + 1)(2j − 1)(2j + 3)
�
�
�
��
− 2j(j + 1) s2 + m2 + j(j + 1) 2j2 + 2j − 1 ;

⟨s Yjm �𝐩3 𝐩3 �s Yjm ⟩ =

(4.14)
(4.15)

and that all the other components of ⟨s Yjm �𝐩a 𝐩b �s Yjm ⟩ are vanishing. (4.14) and
(4.15) imply that 𝛿ab ⟨s Yjm �𝐩a 𝐩b �s Yjm ⟩ = P4, as it should be. These expectation values
may appear to be singular when j = 0 or 1/2, but these are not. In fact, in these cases
s = 0 and |s| = 1∕2, and hence j = n and j = 1∕2 + n, n = 0, 1, 2, ..., respectively.
Writing these into (4.14) and (4.15) and then substituting n = 0, we obtain that these
are P4 ∕3 in both cases.
Choosing both 𝜓1 and 𝜓2 in the above way, and substituting (4.13) into (4.10)
and (4.11), we find, respectively, that

13

## PDF page 17

Page 17 of 34 102

Foundations of Physics (2022) 52:102

�
�
⟨𝜙1 ⊗ 𝜙2 �𝐖12 �𝜙1 ⊗ 𝜙2 ⟩ = 𝜉1a − 𝜉2a 𝜀abc (R1 )b 3 (R2 )c 3 P1 P2
�

s1 s2 m1 m2
+
j1 (j1 + 1)j2 (j2 + 1)

P1 s1
P2 s2 �
+
,
j1 (j1 + 1) j2 (j2 + 1)
s1 s2 m1 m2
.
⟨𝜙1 ⊗ 𝜙2 �𝐏212 �𝜙1 ⊗ 𝜙2 ⟩ = (R−1
R2 )33 P1 P2
1
j1 (j1 + 1)j2 (j2 + 1)
+ (R−1
R2 )33 �m1 m2
1

Hence, the numerator of (4.9) is

�s
s �
⟨𝜙1 ⊗ 𝜙2 �𝐖12 − � 1 + 2 𝐏212 �𝜙1 ⊗ 𝜙2 ⟩ =
P1 P2
��
�
= P1 P2 𝜉1a − 𝜉2a 𝜀abc (R1 )b 3 (R2 )c 3 +
� j (j + 1) − s2

j1 (j1 + 1) − s21 ��

s1 s2 m1 m2
.
j1 (j1 + 1)j2 (j2 + 1)
(4.16)
If s1 s2 m1 m2 = 0, then this is zero. In this case at least one of the expectation values
⟨𝜙1 �𝐩a1 �𝜙1 ⟩ and ⟨𝜙2 �𝐩a2 �𝜙2 ⟩ is vanishing (see the first of (4.13)). This case is analogous to the classical situation when pa1 = 0 or pa2 = 0, and that we excluded from our
investigations (see the second paragraph in subsection 2.1). It might be worth noting
that (4.16) is just ( P1 P2 times) the expectation value of the distance operator (4.7) in
the zeroth approximation according to the expansion (4.8).
Using ⟨s Yjm �𝐩1 𝐩1 �s Yjm ⟩ = ⟨s Yjm �𝐩2 𝐩2 �s Yjm ⟩, we obtain that, in the states above,
(4.12) takes the form
��
�2 �
�2 �
�2
⟨𝜙1 ⊗ 𝜙2 �𝐏412 �𝜙1 ⊗ 𝜙2 ⟩ = (R−1
R2 )11 + (R−1
R2 )12 + (R−1
R2 )21 +
1
1
1
�2 �
�
R2 )22
+ (R−1
⟨𝜓1 �𝐩11 𝐩11 �𝜓1 ⟩⟨𝜓2 �𝐩12 𝐩12 �𝜓2 ⟩+
1
��
�2 � −1
�2 �
R
)
+
(R
R
)
⟨𝜓1 �𝐩11 𝐩11 �𝜓1 ⟩⟨𝜓2 �𝐩32 𝐩32 �𝜓2 ⟩+
+ (R−1
2 13
2 23
1
1
��
�2 � −1
�2 �
R
)
+
(R
R
)
⟨𝜓1 �𝐩31 𝐩31 �𝜓1 ⟩⟨𝜓2 �𝐩12 𝐩12 �𝜓2 ⟩+
+ (R−1
2
31
2
32
1
1
�
�2
R2 )33 ⟨𝜓1 �𝐩31 𝐩31 �𝜓1 ⟩⟨𝜓2 �𝐩32 𝐩32 �𝜓2 ⟩.
+ (R−1
1
(4.17)
A
If the SU(2) matrix U B is parameterized by the familiar Euler angles (𝛼, 𝛽, 𝛾)
according to
)
(
(
)
(
)
exp 2i (𝛼 + 𝛾) cos(𝛽∕2) i exp − 2i (𝛼 − 𝛾) sin(𝛽∕2)
A
)
(
)
(
, (4.18)
U B=
i exp 2i (𝛼 − 𝛾) sin(𝛽∕2) exp − 2i (𝛼 + 𝛾) cos(𝛽∕2)
+ (R−1
R2 )33 �
1

2 2

2

s2 P2

+

s1 P1

then the corresponding rotation matrix is

13

## PDF page 18

102

Page 18 of 34

Foundations of Physics (2022) 52:102

⎛ cos 𝛼 cos 𝛾 − sin 𝛼 cos 𝛽 sin 𝛾 − sin 𝛼 cos 𝛾 − cos 𝛼 cos 𝛽 sin 𝛾 sin 𝛽 sin 𝛾 ⎞
Ra b = ⎜ cos 𝛼 sin 𝛾 + sin 𝛼 cos 𝛽 cos 𝛾 − sin 𝛼 sin 𝛾 + cos 𝛼 cos 𝛽 cos 𝛾 − sin 𝛽 cos 𝛾 ⎟.
⎜
⎟
sin 𝛼 sin 𝛽
cos 𝛼 sin 𝛽
cos 𝛽
⎝
⎠

This yields, in particular, that

cos 𝛽12 ∶= (R−1
R2 )33 = cos 𝛽1 cos 𝛽2 + cos(𝛾1 − 𝛾2 ) sin 𝛽1 sin 𝛽2 ;
1

(4.19)
(4.20)

and that 𝛽12 is just the angle between the unit vectors (R1 )a 3 and (R2 )a 3, too:
R)ab )2
cos 𝛽12 = 𝛿ab (R1 )a 3 (R2 )b 3. Also, the combinations of the matrix elements ((R−1
1
2
in (4.17) are all expressions of cos 𝛽12 alone:
�
�
⟨𝜙1 ⊗ 𝜙2 �𝐏412 �𝜙1 ⊗ 𝜙2 ⟩ = 1 + cos2 𝛽12 ⟨𝜓1 �𝐩11 𝐩11 �𝜓1 ⟩⟨𝜓2 �𝐩12 𝐩12 �𝜓2 ⟩+
�
�
+ 1 − cos2 𝛽12 ⟨𝜓1 �𝐩11 𝐩11 �𝜓1 ⟩⟨𝜓2 �𝐩32 𝐩32 �𝜓2 ⟩+
�
�
+ 1 − cos2 𝛽12 ⟨𝜓1 �𝐩31 𝐩31 �𝜓1 ⟩⟨𝜓2 �𝐩12 𝐩12 �𝜓2 ⟩+

+ cos2 𝛽12 ⟨𝜓1 �𝐩31 𝐩31 �𝜓1 ⟩⟨𝜓2 �𝐩32 𝐩32 �𝜓2 ⟩.

(4.21)
Since the length of the vector 𝜀a bc (R1 )b 3 (R2 )c 3 in (4.16) is sin 𝛽12, (4.21) shows that
d12 depends only on the 𝛽12, i.e. on the relative ‘orientation’ of the two constituent
systems, rather than the individual Euler angles (𝛼1 , 𝛽1 , 𝛾1 ) and (𝛼2 , 𝛽2 , 𝛾2 ).
Denoting the denominator in (4.9) by P1 P2 D and substituting (4.14) and (4.15) into
(4.21), a lengthy but straightforward calculation gives that
(
1
5j (j + 1)j2 (j2 + 1)+
(2j1 − 1)(2j1 + 3)(2j2 − 1)(2j2 + 3) 1 1
)
+ (s21 − 4)j2 (j2 + 1) + (s22 − 4)j1 (j1 + 1) − 3s21 s22 + 3
)(
)
(
)
m22
3m21 m22
j1 (j1 + 1) − 3s21 j2 (j2 + 1) − 3s22 ( m21
+
−
−
(2j − 1)(2j1 + 3)(2j2 − 1)(2j2 + 3) j1 (j1 + 1) j2 (j2 + 1) j1 (j1 + 1)j2 (j2 + 1)
( 1
)(
)(
)(
)
j1 (j1 + 1) − 3s21 j1 (j1 + 1) − 3m21 j2 (j2 + 1) − 3s22 j2 (j2 + 1) − 3m22
−
cos2 𝛽12 .
j1 (j1 + 1)(2j1 − 1)(2j1 + 3)j2 (j2 + 1)(2j2 − 1)(2j2 + 3)

D2 = 1 −

(4.22)
If j1 and j2 take their smallest value, viz. j1 = |s1 | and j2 = |s2 |, i.e. when 𝜓1 and 𝜓2
are centre-of-mass states (see subsection 3.2), then this expression reduces to
( 2
)(
)
3m1 − j1 (j1 + 1) 3m22 − j2 (j2 + 1)
2
2
(4.23)
(1 − 3 cos2 𝛽12 ).
D = +
3
3(j1 + 1)(2j1 + 3)(j2 + 1)(2j2 + 3)
If at least one of j1 = |s1 | and j2 = |s2 | is 0 or 1/2, then D2 = 2∕3, and hence, in
particular, it is not zero and it does not depend on 𝛽12. For small spins the dependence of D2 on 𝛽12 is weak. The higher the spins s1 and s2, the closer the D2 to zero for
|m1 | = j1, |m2 | = j2 and cos2 𝛽12 = 1. Nevertheless, we show that D2 is strictly positive for any finite |m1 | ≤ j1 = |s1 | and |m2 | ≤ j2 = |s2 | and any angle 𝛽12.
Suppose, on the contrary, that D2 = 0, i.e. that for some m1, m2 and 𝛽12

13

## PDF page 19

Foundations of Physics (2022) 52:102

Page 19 of 34 102

(
)(
)
2(j1 + 1)(j2 + 1)(2j1 + 3)(2j2 + 3) = 3m21 − j1 (j1 + 1) 3m22 − j2 (j2 + 1) (3 cos2 𝛽12 − 1)

(4.24)
holds. Since the left hand side is positive, 3 cos2 𝛽12 ≠ 1, 3m21 ≠ j1 (j1 + 1),
3m22 ≠ j2 (j2 + 1) and j1 ≠ 0 ≠ j2 must hold. First, let us suppose that
−1 ≤ 3 cos2 𝛽12 − 1 < 0. Then by (4.24) 3m21 > j1 (j1 + 1) and 3m22 < j2 (j2 + 1) or
3m21 < j1 (j1 + 1) and 3m22 > j2 (j2 + 1) follow. Let us consider the first case. Then,
also by (4.24),
(
)
(
)(
)
2(j1 + 1)(j2 + 1) 4j1 j2 + 6(j1 + j2 ) + 9 ≤ − 3m21 − j1 (j1 + 1) 3m22 − j2 (j2 + 1)
(
)
< 3m21 j2 (j2 + 1) − 3m22 3m21 − j1 (j1 + 1) − j1 j2 (j1 + 1)(j2 + 1) < 3m21 j2 (j2 + 1)
≤ 3j12 j2 (j2 + 1).

This implies 8j12 j2 < 2(j1 + 1)(4j1 j2 + 6j1 + 6j2 + 9) ≤ 3j12 j2, which is a contradiction. The proof is similar if 3m21 < j1 (j1 + 1) and 3m22 > j2 (j2 + 1). Next suppose that
0 < 3 cos2 𝛽12 − 1 ≤ 2. Then (4.24) implies that
(
) (
)(
)
(j1 + 1)(j2 + 1) 4j1 j2 + 6j1 + 6j2 + 9 ≤ 3m21 − j1 (j1 + 1) 3m22 − j2 (j2 + 1) ,
and that either 3m21 > j1 (j1 + 1) and 3m22 > j2 (j2 + 1) or 3m21 < j1 (j1 + 1) and
3m22 < j2 (j2 + 1). In the first case this yields
(
)
(j1 + 1)(j2 + 1) 3j1 j2 + 6j1 + 6j2 + 9 ≤ 9m21 m22 − 3m21 j2 (j2 + 1) − 3m22 j1 (j1 + 1)

≤ 9m21 m22 − 3m21 j22 − 3m22 j12 ≤ 3m21 m22 − 3m21 (j22 − m22 ) − 3m22 (j12 − m21 )
≤ 3m21 m22 ≤ 3j12 j22 ,

which is a contradiction. In the second case,
(
)
(j1 + 1)(j2 + 1) 3j1 j2 + 6j1 + 6j2 + 9 ≤ 9m21 m22 − 3m21 j2 (j2 + 1) − 3m22 j1 (j1 + 1)

< 9m21 m22 − 9m21 m22 − 9m21 m22 = −9m21 m22 ,
which is also a contradiction. We expect that the denominator D, given by (4.22), is
not zero even in the general case when j1 > |s1 | and j2 > |s2 |.
The other extreme case is when both j1 and j2 tend to infinity. Now there are
three sub-cases: when m1 and m2 remain bounded, and when one of them, say m1,
or both tend to infinity with j1 and j2 . As equations (4.13) show, in all these cases
the expectation value of the linear momenta tends to zero, but in the first case the
expectation value of the angular momenta remain finite; in the second the expectation value of 𝐉a1 diverges but that of 𝐉a2 remains finite; while in the third the
expectation value of 𝐉a1 and 𝐉a2 diverges. By (4.22) these limits of D2 are

11
1
5 1
3 1
−
cos2 𝛽12 , + cos2 𝛽12 , − cos2 𝛽12 ,
16 16
8 8
4 4

(4.25)

respectively. These are independent of the spins, and none of them is zero.
Therefore, the empirical distance d12 between the elementary systems is well
defined, finite or zero, at least in the states obtained from centre-of-mass states

13

## PDF page 20

102

Page 20 of 34

Foundations of Physics (2022) 52:102

by E(3) transformations, and also in the j1 , j2 → ∞ limit, and depends only on the
relative ‘position’ and ‘orientation’ of the subsystems. Next we discuss the resulting expression of d12 in these two extreme cases.
In the first case, i.e. when j1 = |s1 | and j2 = |s2 |,
d12 =

(
) ss
( s1
m1 m2
s2 )
1
cos 𝛽12 1 2
(𝜉1a − 𝜉2a )𝜀abc (R1 )b 3 (R2 )c 3 + ℏ
+
,
D
|s1 |P1 |s2 |P2
|s1 s2 | (|s1 | + 1)(|s2 | + 1)

(4.26)
where now D is given by (4.23), and the components of the unit vectors (R1 ) 3 and
(R2 )a 3 can be read off from (4.19). The first term in the brackets can be zero when
these unit vectors are parallel, (R1 )a 3 = ±(R2 )a 3, i.e. when 𝛽12 = 0 or 𝜋 , or when
𝜉1a − 𝜉2a is zero or at least it lays in the 2-plane spanned by (R1 )a 3 and (R2 )a 3. This
term can be arbitrarily large, depending on 𝜉1a − 𝜉2a. This does not contain Planck’s
constant and the Casimir invariants P1 and P2, and gives the ‘classical part’ of the
distance, being analogous to the last term on the right of equation (2.5).
The second term in the brackets, being proportional to ℏ, is a genuine quantum
correction to the classical part. d12 depends on P1 and P2 only through this term.
This can be zero only if 𝛽12 = 𝜋∕2; and, for 𝛽12 ≠ 𝜋∕2, only in the very exceptional
case when P1 = P2 and sign(s1 ) = −sign(s2 ), i.e. if one of 𝜓1 and 𝜓2 is holomorphic
and the other is anti-holomorphic.
Even if 𝜉1a − 𝜉2a, (R1 )a 3 and (R2 )a 3 are given, d12 is not fixed: it depends on the
discrete ‘quantum numbers’ m1 and m2 of the actual states in an essential way. In
particular, for s1 = s2 = 1∕2 (4.26) gives
�
�
�
P + P2
1 � a
𝜉1 − 𝜉2a 𝜀abc (R1 )a 3 (R2 )c 3 + ℏ 1
cos 𝛽12 .
d12 = ± √
P1 P2
3 6
a

Its ‘classical part’ is less than one-sixth of the distance between the two classical
point particles with the same ((R1 )a b , 𝜉1a ) and ((R2 )a b , 𝜉2a ).
If cos 𝛽12 = ±1, then the first term between the brackets in (4.26) vanishes, and
d12 becomes an expression of the Casimir invariants (P1 , s1 ), (P2 , s2 ) of the elementary systems and the discrete quantum numbers m1 and m2 alone. So the distance in
this case is ‘universal’, it is of purely quantum mechanical origin, and, apart from
the very exceptional case above, non-zero. Thus, at the quantum level, the expression for d12 is well defined, in contrast to the classical case when, by the discussion
of subsection 2.2, the distance between two centre-of-mass lines with parallel linear
momenta could be recovered only as a limit.
As we concluded above, d12 is well defined also in the other extreme case when s1
and s2 are fixed but j1 , j2 → ∞. Now we determine the distance in this case explicitly. As (4.16) shows, in the first two cases considered in (4.25) the empirical distance d12 tends to zero, while in the third (i.e. when |m1 | = j1, |m2 | = j2 → ∞) it
tends to

�s
cos 𝛽12
s �
2ℏ 1 + 2 √
.
P2 P1
3 − cos2 𝛽
12

13

## PDF page 21

Page 21 of 34 102

Foundations of Physics (2022) 52:102

In particular, this limit is independent of 𝜉1a − 𝜉2a, and d12 reduces to the quantum
correction. Nevertheless, this extreme case corresponds to a rather exotic situation,
since by (4.13) the expectation value of the angular momenta tend to infinity while
that of the linear momenta to zero.
As we noted, in the states with the choice for 𝜓1, 𝜓2 above all the expectation
values are vanishing for s1 = 0, s2 = 0. To get non-zero results in this case, more
∑
general states with 𝜓 = j,m cjm s Yjm should be considered, because the matrix elements ⟨s Yj±1,n �𝐩a �s Yj,m ⟩ are not all zero even for s = 0 (see Appendix A.2). However,
the explicit form of the resulting expectation values are much more complicated.
4.3 The Empirical Angles and Volume Elements
Dictated by the classical formula (2.9), we define the ‘empirical angle’ between the
linear momenta of two elementary subsystems (characterized by (P1 , s1 ) and (P2 , s2 ),
respectively) in their pure tensor product state 𝜙 = 𝜙1 ⊗ 𝜙2 by

cos 𝜔12 ∶= �

⟨𝜙�𝛿ab 𝐩a1 ⊗ 𝐩b2 �𝜙⟩
⟨𝜙1 �𝐩a1 �𝜙1 ⟩𝛿ab ⟨𝜙2 �𝐩b2 �𝜙2 ⟩
=
�
P1 P2
⟨𝜙�𝐏21 �𝜙⟩ ⟨𝜙�𝐏22 �𝜙⟩

(4.27)

with range 𝜔12 ∈ [0, 𝜋]. Also, motivated by the classical expression (2.10), we
define the ‘empirical 3-volume element’ for three elementary systems in the pure
tensor product state 𝜙 = 𝜙1 ⊗ 𝜙2 ⊗ 𝜙3 by

v123 ∶=

1
𝜀 �
3! abc

⟨𝜙�𝐩a1 ⊗ 𝐩b2 ⊗ 𝐩c3 �𝜙⟩
.
�
�
2
2
2
⟨𝜙�𝐏1 �𝜙⟩ ⟨𝜙�𝐏2 �𝜙⟩ ⟨𝜙�𝐏3 �𝜙⟩

(4.28)

Since these quantities are built only from the momentum operators, and the momentum operators are invariant with respect to translations, it is enough to evaluate these
expressions only in the states of the form 𝜙 = 𝐔𝜓 .
Thus, if 𝜙1 = 𝐔1 𝜓1 and 𝜙2 = 𝐔2 𝜓2, then

1
⟨𝜓 �𝐔† 𝐩a 𝐔 �𝜓 ⟩𝛿 ⟨𝜓 �𝐔† 𝐩b 𝐔 �𝜓 ⟩ =
P1 P2 1 1 1 1 1 ab 2 2 2 2 2
1
=
(R−1 R ) ⟨𝜓 �𝐩a �𝜓 ⟩⟨𝜓2 �𝐩b2 �𝜓2 ⟩.
P1 P2 1 2 ab 1 1 1

cos 𝜔12 =

(4.29)

In particular, if 𝜓1 = s1 Yj1 ,m1 ∕P1 and 𝜓2 = s2 Yj2 ,m2 ∕P2, then

cos 𝜔12 = s1 s2

m1 m2
cos 𝛽12 .
j1 (j1 + 1)j2 (j2 + 1)

(4.30)

The angle 𝜔12 has the same qualitative properties that the empirical angle 𝜃12 has in
the SU(2)-invariant systems [6]. In particular, for given s1 and s2 and angle 𝛽12, the
empirical angle 𝜔12 is still not fixed, that may take different discrete values. Moreover, 𝜔12 is never zero even if 𝛽12 = 0, and is never 𝜋 even if 𝛽12 = 𝜋 . With given s1
and s2 the empirical angle 𝜔12 takes its minimal value in the special centre-of-mass

13

## PDF page 22

102

Page 22 of 34

Foundations of Physics (2022) 52:102

states when m1 = j1 = |s1 | and m2 = j2 = |s2 |, and 𝛽12 = 0. In particular, for
≈ 83.62◦, while for |s1 | = |s2 | = 1 it is ≈ 75.52◦.
|s1 | = |s2 | = 1∕2 this angle is 𝜔min
12
max
The maximal value of 𝜔12 is 𝜔12 = 𝜋 − 𝜔min
. This minimal/maximal value tends to
12
zero/𝜋 only in the |s1 |, |s2 | → ∞ limit. For a classical model of the ‘geometry of the
quantum directions’, see Section 4 of [6].
The evaluation of the empirical 3-volume element in the analogous states is similar. By the first of (4.13) we obtain

v123 =

s1 s2 s3 m1 m2 m3
1
𝜀 (R )a (R )b (R )c .
j1 (j1 + 1)j2 (j2 + 1)j3 (j3 + 1) 3! abc 1 3 2 3 3 3

(4.31)

The second factor in (4.31) is just the Euclidean 3-volume of the tetrahedron
spanned by the unit vectors (R1 )a 3, (R2 )a 3 and (R3 )a 3. Hence, even for given (R1 )a 3,
(R2 )a 3 and (R3 )a 3, the empirical 3-volume element takes different discrete values,
depending on the ‘quantum numbers’ of the states of the constituent subsystems. By
(4.31) v123 is always smaller than the Euclidean 3-volume element, even if all the j’s
take their minimal, and all the m’s take their maximal value, viz. m = j = |s|.
4.4 The Classical Limit of the Empirical Geometrical Quantities
Traditionally, the classical limit of an SU(2)-invariant system is defined to be the
limit in which m = j → ∞ (see e.g. [22]). However, by |m| ≤ j and (4.13), in the
present E(3)-invariant case, the expectation value of the linear momentum tends to
zero unless the spin s also tends to infinity; and this expectation value can tend to a
large macroscopic value if P is also growing appropriately. Thus, formally, the classical limit of the E(3)-invariant systems should be defined to be the limit in which
|s| = m = j → ∞ and P → ∞. Moreover, if we expect that the expectation value of
the linear and angular momenta tend to the corresponding large classical value in the
same order, then by (4.13) we should require that asymptotically P = pj + O(1∕j)
holds for some positive p. We use this latter condition in the calculation of the classical limit of the uncertainty of the empirical distance. Note that by j = |s| the states
in such a sequence are obtained from centre-of-mass states by some E(3) transformations. In the present subsection, we determine this limit of the empirical distances
and their uncertainty, and also that of the angles and 3-volume elements. We find
that these are just those in the Euclidean 3-space.
The s1 = m1 = j1, ±s2 = m2 = j2 → ∞ limit of the numerator in the expression
(4.26) of the empirical distance is

±(𝜉1a − 𝜉2a )𝜀abc (R1 )b 3 (R2 )c 3 ± ℏ

P1 ± P2
cos 𝛽12 ;
P1 P2

while, by (4.23), the same limit of its denominator is sin 𝛽12. But the latter is just the
magnitude of 𝜀a bc (R1 )b 3 (R2 )c 3, and hence, apart from the quantum correction, for
𝛽12 ≠ 0, 𝜋 this gives just the classical (signed) distance between the centre-of-mass
lines of the two classical point particles characterized by ((R1 )a b , 𝜉1a ) and ((R2 )a b , 𝜉2a ),
respectively. If, in addition, P1 , P2 → ∞, then the quantum correction goes away,
and the whole expression reduces to the classical empirical distance.

13

## PDF page 23

Page 23 of 34 102

Foundations of Physics (2022) 52:102

Since d12 is not the expectation value of some quantum observable, its standard
deviation/variance cannot be defined in the standard manner. Nevertheless, its uncertainty can be introduced by importing the idea from experimental physics how the error
of a quantity, built from experimental data, is defined. Namely, if Q = Q(q1 , ..., qn ) is a
differentiable function of its variables and, in a series of measurements, we obtain the
mean values ̄q𝛼 and errors 𝛿q𝛼 of the quantities q𝛼, 𝛼 = 1, ..., n, then the mean value and
̄ ∶= Q(̄q1 , ..., ̄qn ) and
error of Q are defined to be Q

𝛿Q ∶= |

𝜕Q
𝜕Q 𝛼
(̄q )|𝛿q1 + ⋯ + | n (̄q𝛼 )|𝛿qn ,
𝜕q
𝜕q1

respectively. Hence, since the empirical distance has the structure

⟨𝜙�𝐀12 �𝜙⟩
d12 = √
⟨𝜙�𝐁12 �𝜙⟩
with 𝐀12 ∶= 𝐖12 − ℏ(s1 ∕P1 + s2 ∕P2 )𝐏212 and 𝐁12 ∶= P21 P22 − 𝐏412, it seems natural
to define the uncertainty of d12 in the state 𝜙 = 𝜙1 ⊗ 𝜙2 to be

�
𝛿𝜙 d12 ∶=

Δ𝜙 𝐀12
�⟨𝜙�𝐀12 �𝜙⟩�

+

�
1 Δ𝜙 𝐁12
�d12 �.
2 ⟨𝜙�𝐁12 �𝜙⟩

(4.32)

Here

(Δ𝜙 𝐀12 )2 = ⟨𝜙�(𝐀12 )2 �𝜙⟩ − (⟨𝜙�𝐀12 �𝜙⟩)2
and

(Δ𝜙 𝐁12 )2 = ⟨𝜙�(𝐁12 )2 �𝜙⟩ − (⟨𝜙�𝐁12 �𝜙⟩)2 ,
the two familiar variances. We are going to show that, in the classical limit defined
above, both terms between the brackets tend to zero. Since |d12 | in this limit is
bounded, this means that the uncertainty 𝛿𝜙 d12 also tends to zero.
Since the subsequent calculations are quite lengthy but elementary, we do
not provide all the details. We indicate only the key steps. First, let us consider
⟨𝜙�(𝐀12 )2 �𝜙⟩ = ⟨𝜙�(𝐖212 − 2ℏ(j1 ∕P1 ± j2 ∕P2 )𝐏212 𝐖12 + ℏ2 (j1 ∕P1 ± j2 ∕P2 )2 𝐏412 )�𝜙⟩ .
The expectation values in
⟨𝜙1 ⊗ 𝜙2 �𝐖212 �𝜙1 ⊗ 𝜙2 ⟩ =⟨𝜙1 �𝐩a1 𝐩b1 �𝜙1 ⟩𝛿ac 𝛿bd ⟨𝜙2 �𝐉c2 𝐉d2 �𝜙2 ⟩ + ⟨𝜙1 �𝐩a1 𝐉b1 �𝜙1 ⟩𝛿ac 𝛿bd ⟨𝜙2 �𝐉c2 𝐩d2 �𝜙2 ⟩
+⟨𝜙1 �𝐉a1 𝐩b1 �𝜙1 ⟩𝛿ac 𝛿bd ⟨𝜙2 �𝐩c2 𝐉d2 �𝜙2 ⟩ + ⟨𝜙1 �𝐉a1 𝐉b1 �𝜙1 ⟩𝛿ac 𝛿bd ⟨𝜙2 �𝐩c2 𝐩d2 �𝜙2 ⟩

can be calculated by using (3.9). These are

13

## PDF page 24

102

Page 24 of 34

Foundations of Physics (2022) 52:102

⟨𝜙�𝐩a 𝐩b �𝜙⟩ =Ra c Rb d ⟨𝜓�𝐩c 𝐩d �𝜓⟩,
⟨𝜙�𝐩a 𝐉b �𝜙⟩ =Ra c Rb d ⟨𝜓�𝐩c 𝐉d �𝜓⟩ + Ra c 𝜀b ef 𝜉 e Rf d ⟨𝜓�𝐩c 𝐩d �𝜓⟩,
⟨𝜙�𝐉a 𝐉b �𝜙⟩ =Ra c Rb d ⟨𝜓�𝐉c 𝐉d �𝜓⟩ + Ra c 𝜀b ef 𝜉 e Rf d ⟨𝜓�𝐩d 𝐉c �𝜓⟩+
+𝜀a ef 𝜉 e Rf c Rb d ⟨𝜓𝐩c 𝐉d �𝜓⟩ + 𝜀a ef 𝜉 e Rf c 𝜀b gh 𝜉 g Rh d ⟨𝜓�𝐩c 𝐩d �𝜓⟩,
where some of the expectation values with 𝜓 = ±j Yjj ∕P have already been given
by (4.14) and (4.15), while the others can be calculated by (A.18)–(A.26) and
(A.28)–(A.30). These are
�
��
ℏPj � a b
𝛿1 𝛿1 + 𝛿2a 𝛿2b + 2j𝛿3a 𝛿3b + i 𝛿1a 𝛿2a − 𝛿2a 𝛿1a ,
⟨𝜓�𝐩a 𝐉b �𝜓⟩ = ±
2(j + 1)
�
��
�
1
⟨𝜓�𝐉a 𝐉b �𝜓⟩ = ℏ2 j 𝛿1a 𝛿1b + 𝛿2a 𝛿2b + 2j𝛿3a 𝛿3b + i 𝛿1a 𝛿2a − 𝛿2a 𝛿1a .
2
Using (4.20) and that, for large j, asymptotically P = pj + O(1∕j), we obtain
��
�2
�
1
a
b
c
a
2
−
𝜉
𝜀
(R
)
(R
)
�𝜙
⊗
𝜙
⟩
=
𝜉
+
⟨𝜙
⊗
𝜙
�𝐖
3
3
abc
1
2
1
2
1
2
2
1
12
P21 P22
�1
�
1 �� a
+2�
±
𝜉1 − 𝜉2a 𝜀abc (R1 )b 3 (R2 )c 3 cos 𝛽12 +
p1 p2
�
1
1 �2
1
1
±
cos2 𝛽12 + O( ) + O( ).
+�2
p1 p2
j1
j2
(4.33)
The calculation of the expectation value of the other terms is similar, and for them
we obtain

�j
j �
⟨𝜙1 ⊗ 𝜙2 � − 2� 1 ± 2 𝐏212 𝐖212
P1 P2
�j
j �2
+ �2 1 ± 2 𝐏412 �𝜙1 ⊗ 𝜙2 ⟩ =
P1 P2
�
� j1
j ��
± 2 𝜉1a − 𝜉2a 𝜀abc (R1 )b 3 (R2 )c 3 cos 𝛽12
− 2�
P1 P2
�
j �2
j
1
1
− �2 1 ± 2 cos2 𝛽12 + O( ) + O( ).
P1 P2
j1
j2
1

P21 P22

(4.34)

Comparing this with (4.33) and recalling that the first term on the right of (4.33) is
just the classical limit of the square of ⟨𝜙1 ⊗ 𝜙2 �𝐖12 − �(j1 ∕P1 ± j2 ∕P2 )𝐏212 �𝜙1 ⊗ 𝜙2 ⟩∕P1 P2,
we find that the first term in the brackets in (4.32) is of order O(1∕j1 ) + O(1∕j2 ).
Using (4.21), (4.14) and (4.15), we immediately obtain the asymptotic form of the
expectation value of the first two terms in 𝐁212 ∕P41 P42 = 1 − 2𝐏412 ∕P21 P22 + 𝐏812 ∕P41 P42.
It is

13

## PDF page 25

Page 25 of 34 102

Foundations of Physics (2022) 52:102

1
P41 P42

1
1
⟨𝜙1 ⊗ 𝜙2 �P41 P42 − 2P21 P22 𝐏412 �𝜙1 ⊗ 𝜙2 ⟩ = 1 − 2 cos2 𝛽12 + O( ) + O( ).
j1
j2

Thus, we should calculate only the asymptotic form of
f

g

⟨𝜙1 ⊗ 𝜙2 �𝐏812 �𝜙1 ⊗ 𝜙2 ⟩ = ⟨𝜙1 �𝐩a1 𝐩b1 𝐩c1 𝐩d1 �𝜙1 ⟩𝛿ae 𝛿bf 𝛿cg 𝛿dh ⟨𝜙2 �𝐩e2 𝐩2 𝐩2 𝐩h2 �𝜙2 ⟩ =
f

g

= ⟨𝜓1 �𝐩a1 𝐩b1 𝐩c1 𝐩d1 �𝜓1 ⟩(R−1
R2 )ae (R−1
R2 )bf (R−1
R2 )cg (R−1
R2 )dh ⟨𝜓2 �𝐩e2 𝐩2 𝐩2 𝐩h2 �𝜓2 ⟩
1
1
1
1

with 𝜓1 = j1 Yj1 ,j1 ∕P1 and 𝜓2 = ±j2 Yj2 ,j2 ∕P2 when j1 , j2 → ∞. Since by (A.18)–(A.26)

⟨±j Yjj �𝐩3 �±j Yjj ⟩ = ±P3

j
1
+ O( )
j+1
j

√
and all the other matrix elements of the form ⟨±j Yjj �𝐩a �±j Ylm ⟩ fall off as 1∕ j for
large j, we have that
⟨±j Yjj �𝐩a 𝐩b 𝐩c 𝐩d �±j Yjj ⟩ = P6

j4
1
𝛿 a 𝛿 b 𝛿 c 𝛿 d + O( √ ).
(j + 1)4 3 3 3 3
j

Thus, by (4.20)

1
1
1
⟨𝜙1 ⊗ 𝜙2 �𝐏812 �𝜙1 ⊗ 𝜙2 ⟩ = cos4 𝛽12 + O( √ ) + O( √ ).
P41 P42
j1
j2
Hence
1
1
1
⟨𝜙1 ⊗ 𝜙2 �𝐁212 �𝜙1 ⊗ 𝜙2 ⟩ = sin4 𝛽12 + O( √ ) + O( √ ) =
P41 P42
j1
j2
�
�2
1
1
1
= 4 4 ⟨𝜙1 ⊗ 𝜙2 �𝐁12 �𝜙1 ⊗ 𝜙2 ⟩ + O( √ ) + O( √ ),
P1 P2
j1
j2

which yields that the second term in the brackets in (4.32) is also vanishing in the
j1 , j2 → ∞ limit.
Therefore, as a summary of the results of the above calculations, we have proven
the following statement:
Theorem Let L1 , ⋯ , LN be straight lines in ℝ3 such that no two of them are parallel.
Then there are E(3)-invariant elementary quantum mechanical systems S1 , ..., SN
and a sequence of their pure quantum states 𝜙1k,...,𝜙Nk , k ∈ ℕ, indexed by pairs
(s1k , P1k ),...,(sNk , PNk ) of their Casimir invariants, respectively, such that, in the
(|s1 |, P1 ), ..., (|sN |, PN ) → ∞ limit, the magnitude |d𝐢𝐣 | of the empirical distances tend
with asymptotically vanishing uncertainty to the Euclidean distances D𝐢𝐣 between the
straight lines L𝐢 and L𝐣, given by (2.8), for any 𝐢, 𝐣 = 1, ..., N .
Thus, the metric structure of the Euclidean 3-space could be recovered in the
classical limit from appropriate quantum observables of Euclidean invariant elementary quantum mechanical systems.

13

## PDF page 26

102

Page 26 of 34

Foundations of Physics (2022) 52:102

Following the same strategy, the calculation of the classical limit of the empirical angles and 3-volume elements is quite straightforward: the m1 = j1 = s1,
m2 = j2 = s2 → ∞ limit of the empirical angles 𝜔12, given by (4.30), is 𝛽12; and the
analogous limit of the 3-volume element given by (4.31) is just the Euclidean 3-volume element. These results, together with the Theorem above, provide an extension of the Spin Geometry Theorem of Penrose [1–4] from SU(2) to E(3)-invariant
systems.

5 Final Remarks
The relative position vectors d𝐢𝐣a , 𝐢, 𝐣 = 1, 2, 3, of a three-particle system also make it
possible to define a notion of angle that is different from that we considered in subsections 2.3 and 4.3:
cos 𝜛12,32 ∶=

a b
d32
𝛿ab d12

|d12 | |d32 |

f

=

𝛿ab (𝜀a cd pc1 pd2 )(𝜀b ef pe3 p2 )
|𝜀a bc pb1 pc2 | |𝜀a bc pb3 pc2 |

=√

P22 P213 − P212 P223
√
P21 P22 − P412 P22 P23 − P423

with range 𝜛12,32 ∈ [0, 𝜋] defines the angle between the relative position vectors
pointing from the second subsystem’s centre-of-mass line to that of the first and the
third subsystems, respectively. The angles 𝜛23,13 and 𝜛21,31 are defined analogously.
Although at the classical level this angle coincides with the Euclidean one, the analogous empirical angle in the quantum theory deviates from 𝜔𝐢𝐣. Another concept of
the empirical 3-volume element could also be introduced, as the volume of the tetrahedron spanned by the three vectors 𝜀a bc pb𝐢 pc𝐣 . Thus, at the fundamental, quantum
level there might not exist unique, a priori obvious analog of the classical geometrical notions, like angle, distance or 3-volume element. In addition to the requirement
of their correct behaviour in the classical limit (and their ‘naturalness’ and ‘usefulness’), can we have some selection rule to choose one from the various
possibilities?
The states of the composite system by means of which the correct classical limit
of the various empirical geometrical quantities could be derived are pure tensor
product states, built from the pure vector states of the elementary subsystems. Thus,
in deriving these, we did not need to use entangled states of the composite system.
But then, if the subsystems are independent, how can one obtain the distance, angle,
etc. between them? The answer is that the entanglement of the subsystems can be
considered to be already built into the structure of the observables of the composite system. In fact, the operators by means of which the empirical distances, angles
and 3-volume elements are defined have the structure 𝐖12 = 12 𝛿ab (𝐩a1 𝐉b2 + 𝐉a1 𝐩b2 ),
𝐏212 = 𝛿ab 𝐩a1 𝐩b2 and 𝜀abc 𝐩a1 𝐩b2 𝐩c3, respectively. These observables of the composite system are ‘entanglements’ of the observables of the subsystems. The states of the subsystems do not need to be entangled.
As we already noted in subsection 4.2, if the state of the composite system is
mixed or entangled, then the interpretation of the empirical distance (and of the
angles and 3-volume elements, too) is not obvious, and e.g. the distance between

13

## PDF page 27

Page 27 of 34 102

Foundations of Physics (2022) 52:102

two subsystems may depend on the state of other subsystems. In this case, the resulting distances cannot be expected to be compatible with the structure of any metric space. Thus, by assuming that the state of the composite system is a pure tensor product state we implicitly assumed that the subsystems are independent, and
hence interact with one another weakly. If, however, the subsystems are inextricably
entangled (e.g. since they are very strongly interacting with one another), then the
‘quantum geometry’ defined by such systems may not be expected even to resemble
to the Euclidean geometry at all. The Euclidean structure of the classical ‘physical
3-space’ that we see appears to be defined only by the independent, very weakly
interacting subsystems of the Universe.

A. Appendix
A.1 Complex Coordinates and the Line Bundles O(−2s) over SP
In the complex stereographic coordinates (𝜁, 𝜁̄ ) on SP, defined by 𝜁 ∶= exp(i𝜑) cot(𝜃∕2)
in terms of the familiar spherical polar coordinates (𝜃, 𝜑), the Cartesian components of
the ‘position vector’ pa in the classical momentum space and the complex null tangent
ma, respectively, are

� 𝜁̄ + 𝜁
𝜁̄ − 𝜁 𝜁 𝜁̄ − 1 �
pa = P
,
,i
,
1 + 𝜁 𝜁̄ 1 + 𝜁 𝜁̄ 1 + 𝜁 𝜁̄

�
2𝜁 �
1 1 − 𝜁2 1 + 𝜁2
.
ma = √
,i
,
2 1 + 𝜁 𝜁̄ 1 + 𝜁 𝜁̄ 1 + 𝜁 𝜁̄
(A.1)
̄c − ̄
mb mc ), where ̄
ma is the complex conjugate
These imply that pa 𝜀abc = −iP(mb m
of ma. Also in these coordinates, the line element of the metric and the corresponding area element on SP , respectively, are
dh2 =

4P2
̄
d𝜁d𝜁,
(1 + 𝜁 𝜁̄ )2

dSP = −

2iP2
̄
d𝜁 ∧ d𝜁.
̄2
(1 + 𝜁 𝜁)

(A.2)

These are just the metric and area element inherited from the metric and volume
ma
element of momentum 3-space, respectively. The complex null vectors ma and ̄
are unique up to a phase as they are (1, 0) and (0, 1) type vectors, respectively, in the
natural complex structure of SP ≈ S2 (see e.g. [10]). As a differential operator, ma is
given by

ma

� 𝜕 �
�� 𝜕 �
1 �
=√
1 + 𝜁 𝜁̄
.
a
𝜕p
𝜕 𝜁̄
2P

(A.3)

ma, as well as of the ‘posiThe contraction of the complex null vectors, ma and ̄
a
tion vector’ p in the momentum space with the Pauli matrices can also be
expressed by the vectors {oA , 𝜄A } of the (normalized) Newman–Penrose
√ spinor
�
�
�
�
�
�
�
ma 𝜎aAA = −𝜄A ̄oA and pa 𝜎aAA = P(𝜄A 𝜄̄A − oA ̄oA )∕ 2 . The
basis: ma 𝜎aAA = −oA 𝜄̄A , ̄

13

## PDF page 28

102

Page 28 of 34

Foundations of Physics (2022) 52:102

components of the vectors of the Newman–Penrose basis in the spinor basis {OA , I A }
associated with the Cartesian vector basis are
� �
�
�
𝜁
1
−i
−i
oA = √
, 𝜄A = √
̄ .
1 + 𝜁 𝜁̄ 1
1 + 𝜁 𝜁̄ −𝜁
Note that this basis is well defined only on SP minus its ‘north pole’, which is the
domain of the coordinate system (𝜁, 𝜁̄ ), as well as of the complex null vectors ma and
ma.
̄
A scalar 𝜙 is said to have spin weight s = 21 (p − q) if under the rescaling
A A
{o , 𝜄 } ↦ {𝜆oA , 𝜆−1 𝜄A }, 𝜆 ∈ ℂ − {0}, the scalar 𝜙 transforms as 𝜙 ↦ 𝜆p 𝜆̄ q 𝜙 (see
[10, 13]). The bundle of such scalars is denoted by O(−2s). The complex line
bundle O(−2s) is globally trivializable precisely when s = 0 ; otherwise it has a
twist. The domain of the coordinate system (𝜁, 𝜁̄ ) is a local trivialization domain
for O(−2s) for any s. For a detailed discussion of the line bundles O(−2s), see e.g.
[10, 13].
The edth and edth-prime operators of Newman and Penrose [21] acting on spin
weighted functions, e.g. on the cross section 𝜙 of O(−2s), can be defined by
�
�
�
�
� 𝜕𝜙
� 𝜕𝜙
1 �
1 �
ð𝜙 = √
1 + 𝜁 𝜁̄
1 + 𝜁 𝜁̄
+ s𝜁𝜙 , ð� 𝜙 = √
− s ̄𝜁𝜙 ;
𝜕𝜁
𝜕 𝜁̄
2P
2P
(A.4)
�
�
2
and hence for their commutator we obtain that (ðð − ð ð)𝜙 = −(1∕P )s𝜙. It is not
difficult to check that ðpa = ma, ðma = 0 and ð� ma = −pa ∕P2.
A purely algebraic introduction of the spin weighted spherical harmonics,
given in [13], is based on the comparison of the appropriate symmetrized products of the vectors of the Cartesian spinor basis {OA , IA } and those of the Newman–Penrose spinor basis {oA , 𝜄A } adapted to the unit sphere (and given explicitly
by equation (4.15.98) of [13]):

⋯ oAj+s 𝜄Aj+s+1 ⋯ 𝜄A2j ,

(A.5)

(2j)!
2j + 1
,
√
4𝜋
(j − m)!(j + m)!(j − s)!(j + s)!

(A.6)

s Yjm ∶= Ns,j,m O(A1 ⋯ OAj−m IAj−m+1 ⋯ IA2j ) o

where the coefficient Ns,j,m is
j+m

Ns,j,m ∶= (−)

�

A1

and 2s ∈ ℤ, j = |s|, |s| + 1, |s| + 2, ... and m = −j, −j + 1, ..., j . This choice of the
normalization factor yields that the spherical harmonics 0 Yjm coincide with the
standard expressions for the ordinary spherical harmonics Yjm. The action of the edth
operators on the harmonics s Yjm is
1 √
ðs Yjm = − √
(j + s + 1)(j − s) s+1 Yjm ,
2P

13

1 √
ð� s Yjm = √
(j − s + 1)(j + s) s−1 Yjm .
2P

(A.7)

## PDF page 29

Page 29 of 34 102

Foundations of Physics (2022) 52:102

The harmonics s Yj m form an orthonormal basis in the space of the spin weighted
functions with spin weight s with respect to the L2 scalar product on the unit
2-sphere (see e.g. [13]).
A spin weighted scalar 𝜙 is called holomorphic if ð� 𝜙 = 0, and anti-holomorphic
if ð𝜙 = 0. It is known (see e.g. [10, 13]) that dim ker ð = dim ker ð� = 0 for s < 0
and s > 0, respectively; and dim ker ð = dim ker ð� = 2|s| + 1 for s ≥ 0 and s ≤ 0,
respectively. By (A.7) these kernels are spanned by the special spherical harmonics s Y|s| m. Hence the spin weight of the holomorphic cross sections is non-positive,
s = −|s|, while that of the anti-holomorphic ones is non-negative, s = |s|. They form
2|s| + 1 dimensional subspaces in HP,s.

A.2 The Evaluation of ⟨s Ykn �𝐩a � s Yjm ⟩ and ⟨s Ykn �𝐉a � s Yjm ⟩
(A.5) implies that in the product of two spherical harmonics, s1 Yj1 m1 s2 Yj2 m2 , the
difference of the total number of the IA and of the OA spinors is 2(m1 + m2 ), and
the difference of the total number of the oA and of the 𝜄A spinors is 2(s1 + s2 ).
Hence, the spin weight of s1 Yj1 m1 s2 Yj2 m2 is s1 + s2 , and in its expansion in terms of
spin weighted spherical harmonics only the harmonics of the form s1 +s2 Yj(m1 +m2 )
appear. Thus, there are constants C(s1 , j1 , m1 ;s2 , j2 , m2 |j) such that
∑ (
)
C s1 , j1 , m1 ;s2 , j2 , m2 |j s1 +s2 Yj(m1 +m2 ) ,
s1 Yj1 m1 s2 Yj2 m2 =
(A.8)
j

where, as one can show, max{|j1 − j2 |, |s1 + s2 |} ≤ j ≤ j1 + j2. These constants are
analogous to the (inverse) of the usual Clebsch–Gordan coefficients, and hence these
may also be called the (inverse) C-G coefficients.
By (A.1) and the explicit expression of the ordinary spherical harmonics in the coor̄ , the components of the linear momentum are
dinates (𝜁, 𝜁)
� �
�
√
2𝜋
(A.9)
Y
−
Y
,
i(
Y
+
Y
),
pa = P
Y
2
0 10 .
3 0 1−1 0 11 0 1−1 0 11
Hence, to determine the matrix elements ⟨s Ykn �𝐩a �s Yjm ⟩, we need to calculate the
expansion (A.8) only for 0 Y1n s Yjm.
This calculation is based on (A.5), in which, following [13], we introduce the notations Z(j, m)A1 ...A2j ∶= O(A1 ⋯ OAj−m IAj−m+1 ⋯ IA2j ) and s Z(j, m) ∶= (Ns,j,m )−1 s Yjm. Then
for any MA and any totally symmetric spinor ZA1 ...A2j the complete algebraically irreducible decomposition of their product is
ZA1 ...A2j MA = Z(A1 ...A2j MA) +

1
1
𝜀 M B ZBA2 ...A2j + ⋯ +
𝜀 M B ZA1 ...A2j−1 B .
2j + 1 A1 A
2j + 1 A2j A

Applying this formula to IA and Z(j, m)A1 ...A2j , we obtain

13

## PDF page 30

102

Page 30 of 34

Foundations of Physics (2022) 52:102

1
1
Z(j, m)A1 ...A2j IA =Z(j + , m + )AA1 ...A2j +
2
2
1
+
𝜀 I B O(B OA2 ⋯ OAj−m IAj−m+1 ⋯ IA2j ) + ⋯ +
2j + 1 A1 A
1
I B O(A1 ⋯ OAj−m−1 OB IAj−m+1 ⋯ IA2j ) =
𝜀
+
2j + 1 Aj−m A
1
1
=Z(j + , m + )AA1 ...A2j +
2
2
{
1
(j − m)𝜀A1 A O(A2 ⋯ OAj−m IAj−m+1 ⋯ IA2j ) + ⋯ +
+
(2j + 1)2j
}
+ (j − m)𝜀A2j A O(A1 ⋯ OAj−m−1 IAj−m ⋯ IA2j−1 ) =

In a similar way

j−m
1
1
1
1
𝜀 Z(j − , m + )A2 ...A2j ) .
=Z(j + , m + )AA1 ...A2j −
2
2
2j + 1 A(A1
2
2
(A.10)

j+m
1
1
1
1
𝜀 Z(j − , m − )A2 ...A2j ) .
Z(j, m)A1 ...A2j OA = Z(j + , m − )AA1 ...A2j +
2
2
2j + 1 A(A1
2
2
(A.11)
These two are the key formulae on which the present calculation of the (inverse)
C-G coefficients is based. In particular, using the technique of complete algebraic
irreducible decomposition of the various spinors, the repeated application of these
formulae yields
Z(j, m)A1 ...A2j IA IB = Z(j + 1, m + 1)ABA1 ...A2j −
)
j−m (
𝜀A(A1 Z(j, m + 1)A2 ...A2j )B + 𝜀B(A1 Z(j, m + 1)A2 ...A2j )A −
−
(A.12)
2(j + 1)
(j − m)(j − m − 1)
𝜀A(A1 Z(j − 1, m + 1)A2 ...A2j−1 𝜀A2j )B ,
−
2j(2j + 1)
1
Z(j, m)A1 ...A2j IA OB = Z(j + 1, m)ABA1 ...A2j − 𝜀AB Z(j, m)A1 ...A2j +
2
)
(
m
+
𝜀A(A1 Z(j, m)A2 ...A2j )B + 𝜀B(A1 Z(j, m)A2 ...A2j )A +
2(j + 1)
(j − m)(j + m)
+
𝜀 Z(j − 1, m)A2 ...A2j−1 𝜀A2j )B ,
2j(2j + 1) A(A1

(A.13)

Z(j, m)A1 ...A2j OA OB = Z(j + 1, m − 1)ABA1 ...A2j +
)
j+m (
𝜀A(A1 Z(j, m − 1)A2 ...A2j )B + 𝜀B(A1 Z(j, m − 1)A2 ...A2j )A −
+
(A.14)
2(j + 1)
(j + m)(j + m − 1)
𝜀A(A1 Z(j − 1, m − 1)A2 ...A2j−1 𝜀A2j )B .
−
2j(2j + 1)

13

## PDF page 31

Foundations of Physics (2022) 52:102

Page 31 of 34 102

Since Z( 21 , 21 )A = IA, Z( 21 , − 12 )A = OA, Z(1, 1)AB = IA IB, Z(1, 0)AB = I(A OB) and
Z(1, −1)AB = OA OB, equations (A.10)–(A.14), together with (A.5) and (A.6), already
give
�
0 Y1,1 s Yj,m =

�
(j − s + 1)(j + s + 1)(j + m + 1)(j + m + 2)
3 1
s Yj+1,m+1 −
8𝜋 j + 1
(2j + 1)(2j + 3)
�
s √
3
−
(j + m + 1)(j − m)s Yj,m+1 −
(A.15)
8𝜋 j(j + 1)
�
�
3 1 (j − s)(j + s)(j − m − 1)(j − m)
−
s Yj−1,m+1 ;
8𝜋 j
(2j − 1)(2j + 1)

√
0 Y1,0 s Yj,m =

�
0 Y1,−1 s Yj,m =

√
(j + 1 + s)(j + 1 − s)(j + 1 + m)(j + 1 − m)
3 1
s Yj+1,m +
4𝜋 j + 1
(2j + 1)(2j + 3)
√
3 sm
+
Y +
4𝜋 j(j + 1) s j,m
√
√
3 1 (j − s)(j + s)(j + m)(j − m)
+
s Yj−1,m ;
4𝜋 j
(2j − 1)(2j + 1)

(A.16)

�
(j + 1 + s)(j + 1 − s)(j − m + 1)(j − m + 2)
3 1
s Yj+1,m−1 +
8𝜋 j + 1
(2j + 1)(2j + 3)
�
s √
3
+
(j + m)(j − m + 1)s Yj,m−1 −
8𝜋 j(j + 1)
(A.17)
�
�
3 1 (j + s)(j − s)(j + m)(j + m − 1)
−
s Yj−1,m−1 ;
8𝜋 j
(2j − 1)(2j + 1)

where recall that, on the right hand sides, the spherical harmonics s Yj,m are vanishing
if j < |s| or j < |m|. (In these formulae, to avoid confusion, we inserted a comma
between the indices j and m of s Yjm.)
Then, using (A.9) and (A.15)–(A.17), we find that the only non-zero matrix elements of 𝐩a are
�
(j + s + 1)(j − s + 1)
P3
⟨s Yj+1,n �𝐩1 �s Yj,m ⟩ =
2(j + 1)
(2j + 1)(2j + 3)
�√
�
√
×
(j − m + 1)(j − m + 2)𝛿n,m−1 − (j + m + 1)(j + m + 2)𝛿n,m+1 ,

(A.18)

P3 s
⟨s Yj,n �𝐩1 �s Yj,m ⟩ =
2j(j + 1)
�
�√
√
(j + m)(j − m + 1)𝛿n,m−1 + (j − m)(j + m + 1)𝛿n,m+1 ,
×
(A.19)

13

## PDF page 32

102

Page 32 of 34

Foundations of Physics (2022) 52:102

�
(j + s)(j − s)
P3
⟨s Yj−1,n �𝐩1 �s Yj,m ⟩ =
2j (2j − 1)(2j + 1)
�√
�
√
×
(j − m)(j − m − 1)𝛿n,m+1 − (j + m)(j + m − 1)𝛿n,m−1 ;
(A.20)

�

(j + s + 1)(j − s + 1)
P3
2(j + 1)
(2j + 1)(2j + 3)
�√
�
√
×
(j + m + 1)(j + m + 2)𝛿n,m+1 + (j − m + 1)(j − m + 2)𝛿n,m−1 ,

⟨s Yj+1,n �𝐩2 �s Yj,m ⟩ = i

(A.21)
3

Ps
⟨s Yj,n �𝐩2 �s Yj,m ⟩ = i
2j(j + 1)
�
�√
√
(j + m)(j − m + 1)𝛿n,m−1 − (j − m)(j + m + 1)𝛿n,m+1 ,
×
(A.22)

�
⟨s Yj−1,n �𝐩2 �s Yj,m ⟩ = −i
×

P3
2j

(j + s)(j − s)
(2j − 1)(2j + 1)

�√
�
√
(j + m)(j + m − 1)𝛿n,m−1 + (j − m)(j − m − 1)𝛿n,m+1 ,
(A.23)

�
⟨s Yj+1,n �𝐩3 �s Yj,m ⟩ =

P3
j+1

(j + s + 1)(j − s + 1)(j + m + 1)(j − m + 1)
𝛿n,m ,
(2j + 1)(2j + 3)
(A.24)

⟨s Yj,n �𝐩3 �s Yj,m ⟩ =

P3 ms
𝛿 ,
j(j + 1) n,m

(A.25)

�
⟨s Yj−1,n �𝐩3 �s Yj,m ⟩ =

3

P
j

(j + s)(j − s)(j + m)(j − m)
𝛿n,m .
(2j − 1)(2j + 1)

(A.26)

Thus, the subspaces spanned by s Yj,m with given s and j are not invariant under
the action of the momentum operators; and while 𝐩3 does not change the index m,
𝐩1 ± i𝐩2 increases/decreases the value of m.
Next, we calculate the matrix elements of the angular momentum operator using
ma = ðpa, ̄
ma = ð� pa, equations (A.7) and the expression (3.7) for the angular
momentum vector operator. By integration by parts we obtain

13

## PDF page 33

Page 33 of 34 102

Foundations of Physics (2022) 52:102

⟨s Yk,n �𝐉a �s Yj,m ⟩ =ℏP
=ℏP

�SP
�SP

�
s Yk,n

�
p
(ðpa )(ð� s Yj,m ) − (ð� pa )(ðs Yj,m ) + s a2 s Yj,m dSP =
P

�
−(ð� s Yk,n )pa (ð� s Yj,m ) + (ðs Yk,n )pa (ðs Yj,m )+

�
�
�
p
+ s Yk,n pa ð� ðs Yj,m − ðð� s Yj,m + s a2 s Yk,n s Yj,m dSP =
P
�
√
ℏ √
=
(k + s + 1)(k − s) (j + s + 1)(j − s)⟨s+1 Yk,n �𝐩a �s+1 Yj,m ⟩−
2P
√
√
− (k − s + 1)(k + s) (j − s + 1)(j + s)⟨s−1 Yk,n �𝐩a �s−1 Yj,m ⟩+
�
+ 4s⟨s Yk,n �𝐩a �s Yj,m ⟩ .

(A.27)
Hence, the matrix elements of the angular momentum vector operator are simple
expressions of those of the linear momentum. Using (A.18)–(A.26) and (A.27), we
find that the only non-zero matrix elements of 𝐉a are
�√
1
⟨s Yj,n �𝐉1 �s Yj,m ⟩ = ℏP2
(j + m)(j − m + 1)𝛿n,m−1 +
2
�
(A.28)
√
+ (j − m)(j + m + 1)𝛿n,m+1 ,

⟨s Yj,n �𝐉2 �s Yj,m ⟩ =

�
i 2 √
ℏP
(j + m)(j − m + 1)𝛿n,m−1 −
2
�
√
− (j − m)(j + m + 1)𝛿n,m+1 ,

⟨s Yj,n �𝐉3 �s Yj,m ⟩ = ℏP2 m𝛿n,m .

(A.29)

(A.30)

These are precisely the well known matrix elements of the angular momentum operator in quantum mechanics. In particular, these are independent of the spin weight of
the spherical harmonics.
Acknowledgements Thanks are due to Jörg Frauendiener and Paul Tod for their useful remarks on the
determination of the inverse Clebsch–Gordan coefficients; to László Fehér for the clarification of the
algebraic structures on the dual of e(3); to Péter Vecsernyés for the numerous discussions on the algebraic
formulation of quantum theory; and to Ted Jacobson for the discussion on the role of entanglement in the
emergence of the geometry of the 3-space/spacetime from quantum mechanics.
Funding Open access funding provided by ELKH Wigner Research Centre for Physics.

Declarations
Conflict of interest There is no conflict of interest that could be relevant to the content of this article. No
funds, grants or support was received.
Open Access This article is licensed under a Creative Commons Attribution 4.0 International License,
which permits use, sharing, adaptation, distribution and reproduction in any medium or format, as long as
you give appropriate credit to the original author(s) and the source, provide a link to the Creative Commons

13

## PDF page 34

102

Page 34 of 34

Foundations of Physics (2022) 52:102

licence, and indicate if changes were made. The images or other third party material in this article are
included in the article’s Creative Commons licence, unless indicated otherwise in a credit line to the material. If material is not included in the article’s Creative Commons licence and your intended use is not permitted by statutory regulation or exceeds the permitted use, you will need to obtain permission directly from
the copyright holder. To view a copy of this licence, visit http://​creat​iveco​mmons.​org/​licen​ses/​by/4.​0/.

References
1. Penrose, R.: Combinatorial quantum theory and quantized directions. In: Houghston, L.P., Ward,
R.S. (eds.) Advances in Twistor Theory. Pitman Publishing Ltd, London (1979)
2. Penrose, R.: Angular momentum: an approach to combinatorial spacetime. In: Bastin, T. (ed.)
Quantum Theory and Beyond. Cambridge University Press, Cambridge (1971)
3. Penrose, R.: On the nature of quantum geometry. In: Klauder, J. (ed.) Magic Without Magic. Freeman, San
Francisco (1972)
4. Penrose, R.: Theory of quantized directions. In: Collected Works. vol 1, pp. 769–800. Oxford University
Press, Oxford (2010)
5. Moussouris J.P.: Quantum Models of Spacetime Based on Recoupling Theory, PhD dissertation, Oxford
University.
https://​ora.​ox.​ac.​uk/​objec​ts/​uuid:​6ad25​485-​c6cb-​4957-​b129-​5124b​b2adc​67
(1984).
Accessed Jan 2022
6. Szabados L.B.: A note on Penrose’s Spin-Geometry Theorem and the geometry of ‘empirical quantum
angles’. Found. Phys. 52, 96 (2022). https://​doi.​org/​10.​1007/​s10701-​022-​00616-3
7. Salecker, H., Wigner, E.P.: Quantum limitations of the measurement of space-time distances. Phys. Rev.
109, 571–577 (1958). https://​doi.​org/​10.​1103/​PhysR​ev.​109.​571
8. Bacry, H.: Localizability and space in quantum mechanics. In: Lecture Notes in Physics, vol. 308. Springer,
Berlin (1988)
9. Newton, T.D., Wigner, E.P.: Localized states for elementary systems. Rev. Mod. Phys. 21, 400–406 (1949).
https://​doi.​org/​10.​1103/​RevMo​dPhys.​21.​400
10. Hugget, S.A., Tod, K.P.: An Introduction to Twistor Theory, London Mathematical Society Student
Texts 4, 2nd edn. Cambridge University Press, Cambridge (1994)
11. Penrose, R., MacCallum, M.A.H.: Twistor theory: an approach to the quantisation of fields and spacetime. Phys. Rep. 6, 241–316 (1972). https://​doi.​org/​10.​1016/​0370-​1573(73)​90008-2
12. Penrose, R., Rindler, W.: Spinors and Spacetime, vol. 2. Cambridge University Press, Cambridge (1986)
13. Penrose, R., Rindler, W.: Spinors and Spacetime, vol. 1. Cambridge University Press, Cambridge (1984)
14. Rno, J.S.: Clebsch-Gordan coefficients and special functions related to the Euclidean group in threespace. J. Math. Phys. 15, 2042–2047 (1974). https://​doi.​org/​10.​1063/1.​16665​79
15. Tung, W.-K.: Group Theory in Physics. World Scientific, Singapore (1985)
16. Kowalski, K., Rembieliński, J.: Quantum mechanics on a sphere and coherent states. J. Phys. A: Math.
Gen. 33, 6035–6048 (2000). https://​doi.​org/​10.​1088/​0305-​4470/​33/​34/​309
17. Silva, R.A., Jacobson, T.: Particle on the sphere: group-theoretic quantization in the presence of a magnetic monopole. J. Phys. A: Math. Theor. 54, 235303 (2021). https://​doi.​org/​10.​1088/​1751-​8121/​abf961
18. Szabados, L.B.: An odd feature of the ‘most classical’ states of SU(2) invariant quantum mechanical
systems, arXiv:​ 2106.​08695 [gr-qc]
19. Szabados, L.B.: The ‘most classical’ states of Euclidean invariant elementary quantum mechanical systems, arXiv:​ 2111.​11876 [quant-ph]
20. Streater, R.F., Wightman, A.S.: PCT, Spin and Statistics, and All That. W. A. Benjami, INC, New York
(1964)
21. Newman, E.T., Penrose, R.: Note on the Bondi-Metzner-Sachs group. J. Math. Phys. 7, 863–879 (1966).
https://​doi.​org/​10.​1063/1.​19312​21
22. Wigner, E.P.: Group Theory and Its Application to the Quantum Mechanics of Atomic Spectra. Academic Press, New York (1959)
Publisher’s Note Springer Nature remains neutral with regard to jurisdictional claims in published maps and
institutional affiliations.

13
