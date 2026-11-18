Source: see manifest row of the PDF
PDF sha256: 1175ea83d365bff9de959eb772c0c3fc52cf7c02bcf1a16ebb7cf086a713f346
License: CC-BY-4.0
Language: eng
Fidelity: machine-gated

# Transcription of panella_svesko_2023_quantum_kerr_de_sitter_black_holes_in_three_dimensions.pdf

Transcription of `panella_svesko_2023_quantum_kerr_de_sitter_black_holes_in_three_dimensions.pdf` in this directory, 52 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-52 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Published for SISSA by

Springer

Received: April 8, 2023
Accepted: June 6, 2023
Published: June 21, 2023

Emanuele Panella and Andrew Svesko
Department of Physics and Astronomy, University College London,
Gower Street, London, WC1E 6BT, U.K.

E-mail: emanuele.panella.21@ucl.ac.uk, a.svesko@ucl.ac.uk
Abstract: We use braneworld holography to construct a three-dimensional quantumcorrected Kerr-de Sitter black hole, exactly accounting for semi-classical backreaction effects
due to a holographic conformal field theory. By contrast, classically there are no de Sitter
black holes in three-dimensions, only geometries with a single cosmological horizon. The
quantum Kerr black hole shares many qualitative features with the classical four-dimensional
Kerr-de Sitter solution. Of note, backreaction induces inner and outer black hole horizons
which hide a ring singularity. Moreover, the quantum-corrected geometry has extremal,
Nariai, and ultracold limits, which appear as fibered products of a circle and two-dimensional
anti-de Sitter, de Sitter, and Minkowski space, respectively. The thermodynamics of the
classical bulk black hole, described by the rotating four-dimensional anti-de Sitter C-metric,
has an interpretation on the brane as thermodynamics of the quantum black hole, obeying
a semi-classical first law where the Bekenstein-Hawking area entropy is replaced by the
generalized entropy. For purposes of comparison, we derive the renormalized quantum
stress-tensor due to a free conformally coupled scalar field in the classical Kerr-de Sitter
conical geometry and perturbatively solve for its backreaction.
Keywords: Black Holes, AdS-CFT Correspondence
ArXiv ePrint: 2303.08845

Open Access, c
⃝ The Authors.
Article funded by SCOAP3 .

https://doi.org/10.1007/JHEP06(2023)127

JHEP06(2023)127

Quantum Kerr-de Sitter black holes in three
dimensions

## PDF page 2

Contents
1

2 Braneworlds and quantum SdS black hole: review

4

3 Geometry of quantum Kerr-dS3 black holes
3.1 Bulk and brane geometry
3.2 Black hole on the brane
3.3 Extremal, Nariai, ultracold, and lukewarm limits
3.4 Holographic conformal matter stress-tensor

8
8
11
15
19

4 Thermodynamics of quantum Kerr-dS3 black holes
4.1 Bulk thermodynamics
4.2 Semi-classical thermodynamics on the brane

23
23
25

5 Discussion

28

A Geometry of classical Kerr-dS3

31

B Perturbative backreaction in Kerr-dS3

33

C Elements of the AdS C-metric

38

D Limits of qKdS

41

1

Introduction

Developing a consistent theory of quantum gravity remains a difficult open problem in
theoretical physics. To make progress, it is standard practice to simplify the problem. One
approach is to focus on spacetimes exhibiting features quantum gravity is expected to display,
such as black holes, whose thermodynamics lay the foundation for holography. Another
approach is to study quantum gravity in spacetimes with fewer dimensions than our own,
where we often have better analytic control. Combining both views has proven successful in
the context of the anti-de Sitter/conformal field theory (AdS/CFT) correspondence, where,
for example, physics of three-dimensional AdS black holes [1, 2], including a statistical
interpretation of their thermal entropy [3, 4] and computation of the partition function [5],
has a dual description in terms of a CFT living on the two-dimensional boundary of AdS.
Classically, however, there are no black hole solutions to Einstein’s field equations
in three-dimensional de Sitter space (dS3 ). Rather, the geometry of a point mass in dS3
describes a conical defect with a single cosmological horizon and no black hole horizon [6].

–1–

JHEP06(2023)127

1 Introduction

## PDF page 3

Gµν + Λ3 gµν = 8πG3 ⟨Tµν ⟩

(1.1)

of a massless conformally coupled scalar field with stress-energy tensor Tµν in a threedimensional Schwarzschild-de Sitter background. To leading order in backreaction, the
geometry receives a correction, δgtt ∼ LP /r in static coordinates, such that a black hole
horizon appears [7]. In fact, the (t, r)-sector of the resulting geometry looks like a classical
four-dimensional Schwarzschild-dS black hole, heralding a holographic pedigree.
The purpose of this article is to analyze semi-classical backreaction of a conformal field
theory in a Kerr-dS3 (KdS3 ) background. Despite the inclusion of rotation, the KdS3 metric
also describes a conical defect with a single cosmological horizon (see, e.g., [8]). As we will
show, semi-classical backreaction leads to the development of inner and outer black hole
horizons, as is standard for the classical higher-dimensional Kerr-dS geometry. However,
as in the static case, to confirm such a quantum-corrected black hole does arise, we must
consistently solve the semi-classical Einstein equations for a large number of quantum fields
perturbatively in LP beyond leading order, another challenging open problem.
Fortunately, there is an alternative framework, dubbed ‘braneworld holography’ [9], that
may exactly account for quantum backreaction, without explicitly solving the semi-classical
Einstein equations (1.1). In this setting, one couples Einstein gravity in a holographic
asymptotically (d + 1)-dimensional AdS background to a d-dimensional Randall-Sundrum
brane [10]. Integrating out the bulk gravitational degrees of freedom up to the brane leads
to a theory of gravity induced on the brane with, schematically, the following field equations
Gµν + Λd gµν + (higher-curvature) = 8πGd ⟨Tµν ⟩ .

(1.2)

This leads to two equivalent perspectives, bulk and brane. The bulk is described by classical
general relativity in AdSd+1 , with a dual CFTd description, coupled to a codimension-1 brane,
while an observer confined to the brane experiences a d-dimensional semi-classical theory
of gravity coupled to the holographic CFTd with an ultraviolet cutoff and renormalized
1

The basic reasoning follows from dimensional analysis. The Planck length in three-dimensions is
LP = ℏG3 , where we work in units with the speed of light set to unity. A collection of c ≫ 1 quantum
fields will introduce a combined quantum effect of cℏ which may gravitate giving rise to a black hole with
horizon radii cLP ≫ LP . Crucially, even in the limit of vanishing quantum gravity effects, where c → ∞
and LP → 0 with cLP fixed, classical backreaction due to the quantum fields remain finite.

–2–

JHEP06(2023)127

This is unfortunate since de Sitter space, having a positive cosmological constant, is a
reasonable approximation of our universe during its inflationary past and current phase of
accelerated expansion. Consequently, the uncharged Kerr-de Sitter spacetime is, arguably,
the most astrophysically relevant black hole to study. However, it seems we cannot
learn about the microphysics of higher-dimensional de Sitter black holes by appealing to
lower dimensions.
Despite the lack of classical dS3 black holes, quantum effects dramatically alter the
situation: de-Sitter black holes with horizons significantly larger than the Planck length
arise due to semi-classical backreaction [7].1 Cursory evidence for this can be seen by
analyzing the semi-classical Einstein equations

## PDF page 4

SBH =

A4
A3
↔ Sgen =
+ SWald + SCFT .
4G4
4G3

(1.3)

Here A3 represents the area of the horizon of the brane black hole, SWald is the Wald
entropy [15] accounting for the higher-curvature corrections in the theory, and SCFT is the
CFT entanglement entropy due to quantum fluctuations outside of each horizon. With
this identification, we will uncover the first law of thermodynamics of quantum-corrected
Kerr-de Sitter black holes, which, again, is guaranteed to hold to all orders in backreaction.
An outline of the remainder of this article is as follows. In section 2 we briefly review
braneworld holography and the construction of the qSdS solution. Section 3 is primarily
devoted to the geometric construction of the qKdS black hole, where include an analysis of
each of its Nariai, extremal, and ultracold limits, and compute the renormalized stress-tensor
2

Historically, exact three-dimensional black hole solutions on the brane were uncovered in [13, 14] and
later interpreted as holographic quantum black holes in [11], however, the higher curvature corrections of
the induced gravity action on the brane were not explicitly accounted for until [12].

–3–

JHEP06(2023)127

stress-tensor ⟨Tµν ⟩. Consistency between these two pictures demands quantum dynamics
of the brane gravity theory be entirely encoded in the classical dynamics of the bulk.
Consequently, black holes localized on a brane in AdSd+1 — found by solving the classical
bulk Einstein equations with brane boundary conditions — are, from the brane point of
view, black holes corrected by the backreaction of the d-dimensional CFT [11]. Thus far,
this procedure has been carried out analytically in d = 3, uncovering a family of quantum
AdS3 black holes, collectively referred to as the quantum BTZ (qBTZ) solution [12], and
the quantum Schwarzschild-dS (qSdS) black hole [7].2
Following suit, here we use braneworld holography to find an exact quantum-corrected
rotating black hole in dS3 , a non-trivial extension of [7]. Our starting point, as in [12], is
the rotating AdS4 C-metric, however, coupled to an asymptotically dS3 Randall-Sundrum
brane. As an exact solution to the bulk Einstein equations, we are guaranteed the brane
geometry is an exact solution to the full semi-classical theory (1.2), in the planar limit of
the CFT, resulting in the quantum Kerr-dS (qKdS) black hole, presented in (3.17). The
essential new correction to the geometry is a term which goes like 1/r in appropriate static
coordinates. This feature, combined with the 1/r2 behavior typical in a Kerr-black hole
(including classical Kerr-dS3 ), results in a three-dimensional geometry with three horizons,
an inner and outer black hole horizon and a cosmological horizon, leading to three limiting
behaviors: (i) an extremal limit, when the inner and outer horizons coincide, (ii) the rotating
quantum Nariai black hole, when the outer and cosmological horizons coincide, and (iii) an
ultracold limit when all three horizons coincide. There is also a ‘lukewarm’ quantum black
hole, where the surface gravities of outer and cosmological horizons are equal. Further,
unlike three-dimensional KdS, the quantum-corrected geometry has a ring singularity.
Quantum backreaction also enriches the thermodynamic behavior of the black hole.
Via holography, thermodynamics of the bulk black hole is interpreted as thermodynamics
of the semi-classical brane black hole. Crucially, the Bekenstein-Hawking entropy of the
bulk black hole SBH , proportional to the area A4 of its event horizon, is identified with the
three-dimensional generalized entropy Sgen ,

## PDF page 5

of the holographic CFT. A detailed account of the horizon thermodynamics is given in
section 4. We conclude in section 5 where we describe multiple future research directions.
To keep this article complete and self-contained, we include a number of appendices.
Appendix A summarizes the basic elements of the classical Kerr-dS3 geometry. Since we
have not seen the computation performed in the literature, in appendix B we provide an
analysis of perturbative backreaction due to a massless conformally coupled scalar field
in classical Kerr-dS3 . Appendix C reviews the geometry of the AdS4 C-metric along with
additional details of the braneworld construction. Appendix D expounds on the extremal,
Nariai, ultracold, and lukewarm limits of the quantum black hole.

Braneworlds and quantum SdS black hole: review

Braneworld holography and induced gravity. Consider an asymptotically AdSd+1
spacetime M of curvature scale Ld+1 , with a dual description in terms of a CFTd on
the asymptotic boundary ∂M. The standard AdS/CFT dictionary of Gubser, Klebanov,
Polyakov and Witten (GKPW) [16, 17] relates the CFT generating functional to the on-shell
gravitational action. Even at tree level, the on-shell action will have long-distance infrared
(IR) divergences since the metric will grow to infinity as the asymptotic AdS boundary is
approached. These correspond to ultraviolet (UV) divergences due to quantum fluctuations
of the dual CFT. Holographic renormalization [18, 19] is a prescription to remove the IR
divergences by adding appropriate local counterterms [18, 20–22] in a minimal subtraction
scheme. The divergent contribution to the action may be cast in terms of the curvature
invariants with respect to the induced metric hij near ∂M
(

√
L2d+1
Ld+1
2(d − 1)
R
dR2
2
Idiv =
dd x −h
+
+
R
−
16πGd+1 ∂M
(d − 2) (d − 2)2 (d − 4) ij 4(d − 1)
L2d+1
∫

[

)

]

+ ... .

(2.1)
Technically, this action arises by introducing an IR cutoff surface at some small finite
distance away from ∂M. Integrating out the bulk degrees freedom up to the cutoff surface,
the regulated bulk gravity action (Einstein-Hilbert action plus a Gibbons-Hawking-York
boundary term) is a sum of a divergent contribution (2.1) and a finite action in the limit
the bulk cutoff surface approaches the boundary. Holographic renormalization is complete
by adding a counterterm Ict = −Idiv to the regulated action and taking the boundary limit.
In braneworld holography [9], the bulk IR regulator surface is replaced by a ddimensional end-of-the-world brane B (typically taken to be near the boundary), as in
the Randall-Sundrum braneworld construction [10], such that the limiting procedure is
not taken. Consequently, the physical space is cutoff, however, there are no longer any
divergences to remove and Idiv is finite. Additionally, the metric on the brane is dynamical,
characterized by a holographically induced higher curvature theory of gravity coupled to a
CFT with a UV cutoff. More precisely, the induced theory on the brane is found by adding
to the bulk Einstein theory the brane action
Ibrane = −τ

√
dd x −h ,

∫
B

–4–

(2.2)

JHEP06(2023)127

2

## PDF page 6

where τ is a parameter controlling the tension of the brane. Integrating out the bulk
between ∂M up to B as in holographic regularization, the induced theory on the brane is
I = IBgrav [B] + ICFT [B] .

(2.3)

The induced gravity theory on the brane is (see, e.g., [23, 24])3
[

L2d+1
+
(d − 4)(d − 2)

(

∫

2(d − 1)(d − 2)
4πGd+1 Ld+1
d x −h R +
1−
τ
2
(d − 1)
Ld+1
B
d

(

2
Rij
−

dR2
4(d − 1)

)

]

)

(2.4)

+ ··· ,

where the ellipsis corresponds to higher curvature densities, which have thus far been
efficiently computed up to quintic order in curvature for arbitrary d and sextic order for
d = 3 [24]. Here Gd represents the effective Newton’s constant endowed from the bulk
Gd =

d−2
Gd+1 .
2Ld+1

(2.5)

It is also natural to introduce another induced length scale Ld on the brane, expressed
in terms of Ld+1 , Gd+1 and τ , which would represent the induced dS radius on the brane.
We will do this explicitly momentarily. The second action ICFT corresponds to the finite
contribution to the regulated bulk action upon integrating out the bulk. This contribution
is not determined by the boundary metric and thus corresponds to the state of the CFT d .
There are two ways to interpret the theory I (2.3). From the bulk perspective, I
characterizes a theory of a finite (d + 1)-dimensional system with dynamics ruled by general
relativity and a brane. Alternatively, from the brane perspective, I represents a specific
holographically induced higher-curvature theory in d dimensions coupled to a CFT which
backreacts on the brane metric hij . Notably, the CFT has a UV cutoff corresponding to the
IR cutoff surface introduced in holographic regularization. Additionally, the induced theory
of gravity is said to be ‘massive’ since a massive graviton bound state will localize on the
brane [25], however, this mass will become negligible for a brane very near the boundary. 4
By consistency, there is an equivalence between the bulk and brane viewpoints, leading
to a powerful computational device: classical solutions to the bulk Einstein equations (with
appropriate brane boundary conditions) exactly correspond to solutions to the semi-classical
equations of motion on the brane.5 Specifically, classical black holes map to quantum3

The gravitational sector of the induced theory here is technically given by the sum IBgrav = 2Idiv + Ibrane .
The factor of two depends on the specific braneworld construction. Namely, whether or not we consider a
Z2 construction by gluing a second copy of the spacetime along the cutoff region such that one integrates
out the bulk geometry on both sides of the brane.
4
A construction with two branes would also have a remaining scalar mode, the radion [26], representing
the displacement between the branes [26, 27]. Here we consider a bulk with a single brane and thence
no radion.
5
It is worth emphasizing that exact bulk solutions lead to exact solutions to the entire gravity theory on
the brane, including the whole tower of higher-derivative terms. Importantly, while general higher derivative
theories of gravity are pathological since they are typically accompanied with ghosts, one does not expect
the brane theory to be pathological (assuming one does not truncate the series of terms) since the bulk
theory and the procedure of integrating out the bulk are not pathological.

–5–

JHEP06(2023)127

√

1
IBgrav =
16πGd

## PDF page 7

corrected black holes, accounting for all orders of backreaction [11]. To illustrate this point,
we briefly summarize a relevant construction below, the quantum SdS3 black hole [7].
The qSdS black hole. Consider the four-dimensional AdS4 C-metric, a solution to
Einstein’s equation with a negative cosmological and belongs to the general PlebanskiDemianski type-D class [28]
[

ℓ2
dr2
ds =
−H(r)dt2 +
+ r2
2
(ℓ + xr)
H(r)

(

2

dx2
+ G(x)dφ2
G(x)

)]

,

(2.6)

H(r) = 1 −

r2
µℓ
−
,
2
r
R3

G(x) = 1 − x2 − µx3 .

(2.7)

Our conventions primarily follow [12], however, with κ = +1 and set ℓ23 = −R32 such that
the brane we eventually introduce is a dS3 brane of radius R3 .6 The C-metric is known
to describe accelerating black holes, where the real, positive parameter ℓ is equal to the
(inverse) acceleration. Meanwhile, µ > 0 is interpreted to be a mass parameter of the
four-dimensional black hole. The AdS4 length scale L4 is related to the parameters R3 and
ℓ via
[
(
) ]
ℓ 2
−2
−2
L4 = ℓ
1−
.
(2.8)
R3
For L24 > 0 such that the bulk cosmological constant is negative, we require R32 > ℓ2 .
Following the construction of [13, 14], a Randall-Sundrum brane with tension τ and
action (2.2) is placed at the umbilic x = 0 surface, resulting in a tension
τ=

1
.
2πG4 ℓ

(2.9)

The tension may be read off from the Israel junction conditions which determine the location
of the brane, such that tuning the tension corresponds to changing the position of the brane.
We review this construction more carefully in appendix C. Further, recall that the brane
effectively cuts off the bulk space. For a dS braneworld, we keep only the x > 0 portion
of the bulk, eliminating all but one of the roots of G(x), which we denote as x1 . This
root corresponds to an axis for the rotational Killing symmetry ∂φ resulting in a conical
singularity at x = x1 ,7 and is removed via the identification
φ ∼ φ + ∆φ ,

∆φ =

4π
|G′ (x1 )|

=

4πx1
.
3 − x21

(2.10)

To complete the space, we perform surgery by cutting the bulk at x = 0, keeping only the
range 0 ≤ x ≤ x1 , where there are no conical singularities, and glue a second copy along B
to complete the space. See figure 1 for an illustration.
6

The cases κ = 0 or κ = −1 exclude the possibility of a dS3 brane, since the roots of H(r) do not
represent a cosmological horizon in those cases.
7
In fact, the vector ∂φ will have vanishing norm on the locus x = xi for each zero xi of G(x).

–6–

JHEP06(2023)127

with metric functions H(r) and G(x)

## PDF page 8

The geometry induced on the brane at x = 0 will result in a metric in (t, r, φ)-coordinates
which has a conical deficit angle due to the identification (2.10). To respect regularity in
the bulk, one thus rescales coordinates (t, r, φ) → (t̄, r̄, φ̄), where t = η t̄, r = η −1 r̄, and
φ = η φ̄, and 2πη ≡ ∆φ, such that φ̄ is periodic in 2π, and results in the geometry [7]
ds2qSdS = −H(r̄)dt̄2 +H −1 (r̄)dr̄2 + r̄2 dt̄2 ,

H(r̄) = 1−8G3 M −

ℓF (M ) r̄2
− 2.
r̄
R3

(2.11)

This is the three-dimensional quantum Schwarzschild-de Sitter black hole. Depending on
the size of ℓF (M ), there exist two positive roots to H(r̄) = 0, denoted r̄+ and r̄c , the black
hole and cosmological horizon, respectively. From the bulk perspective, the cosmological
horizon on the brane arises due to the brane intersecting the acceleration horizon of the
bulk black hole. Moreover, here the mass M of the brane black hole and the form factor
F (M ) are
8G3 M ≡ 1 −

4x21
,
(3 − x21 )2

F (M ) ≡

8(1 − x21 )
,
(3 − x21 )3

(2.12)

with renormalized Newton’s constant G3 ≡ L4 G3 /ℓ. To arrive at the expression for F (M ),
the parameter µ is treated as being “derived” from G(x1 ) = 0, such that x1 ∈ (0, 1], where
x1 = 1 coincides with µ = 0 [12].
We can think of the metric (2.11) as a semi-classical black hole because it is an exact
solution to the holographically induced theory of gravity
1
I=
16πG3

∫

√

2
3
2
d x −h R − 2 − L24 Rij
− R2 + . . . + ICFT ,
8
L
B
3
3

[

(

–7–

)

]

(2.13)

JHEP06(2023)127

Figure 1. Left: bulk AdS4 with a de Sitter3 brane. The brane is represented as a (magenta)
hyperboloid. The bulk region up to the brane (x < 0, dashed magenta region) is excluded. To
complete the construction, we glue a second copy along the two-sided brane. Cosmological horizons
on the dS brane corresponds to the bulk acceleration horizons intersecting the brane (red dashed
line). Right: constant t-time slice of a single AdS4 cylinder with a de Sitter brane (thick red circle)
containing black holes. The coordinates cover only half of the disk, containing only a single black hole
and cosmological horizon, where the other half is obtained via an appropriate analytic continuation.

## PDF page 9

with semi-classical equations of motion
8πG3 ⟨TijCFT ⟩ = Gij +
+ℓ

2

[

hij
L23

(2.14)

9
1
1
4Rik R̃jk − RRij −□Rij + ∇i ∇j R+ hij
4

4

2

(

13 2
1
2
R −3Rkl
+ □R
8
2

)]

+. . . .

3

Geometry of quantum Kerr-dS3 black holes

As reviewed above, braneworld holography grants us the ability to study the problem of
semi-classical backreaction without having to explicitly solve semi-classical equations of
motion. By a judicious choice of a bulk spacetime, the bulk black hole localizes on the
brane and leads to the qSdS on the brane — the first known example of an exact quantum
de Sitter black hole in the sense that the solution encodes all orders of semi-classical
backreaction. Here we use braneworld holography to uncover the quantum Kerr-de Sitter
black hole, focusing primarily on the geometry, leaving the thermodynamic analysis for the
subsequent section.
3.1

Bulk and brane geometry

Analogous to the rotating quantum BTZ black hole [12], our starting point is the rotating
AdS4 C-metric, describing accelerating Kerr-AdS4 black holes and has the line element
[

) ])

2
H(r)
Σ
Σ
G(x)
a
ds2 = ω 2 −
(dt−ax2 dφ)2 +
dr2 +r2
dx2 +
dφ+ 2 dt
Σ
H(r)
G(x)
Σ
r

(

8

(

(3.1)

The limit of vanishing backreaction looks singular from the bulk perspective, since keeping R3 finite
would then require L4 → 0. Instead take the limit L4 → 0 while rescaling the bulk metric by a factor L24 ,
then the brane is pushed to the boundary and gravitational dynamics on the brane is turned off, while still
keeping a non-trivial state of the non-backreacting CFT3 [7].

–8–

JHEP06(2023)127

The CFT stress-energy tensor sources the effective three-dimensional gravity theory such
that backreaction is accounted for by ⟨TijCFT ⟩. Here we work in the limit where the effective
three-dimensional theory obeys L4 ≪ L3 , or, equivalently, ℓ ∼ L4 such that ℓ/R3 is taken
to be a small expansion parameter. Thus, the higher curvature terms in the action are
multiplied by higher powers of ℓ, where, from the brane perspective, ℓ captures the strength
of backreaction. Hence, the higher-derivative corrections can be understood as a series of
corrections due to semi-classical backreaction. In the limit of small backreaction, moreover,
L23 ≈ R32 while the central charge c ≡ L24 /G4 of the CFT3 satisfies 2cG3 = L4 ≈ ℓ. Therefore,
for fixed c, gravity becomes weak on the brane as ℓ → 0 such that there is no backreaction
due to the CFT.8 Lastly, ℓ ≈ 2cLP , where LP = G3 is the Planck length (since we set ℏ = 1).
Returning to the qSdS geometry (2.11), we see that the ℓF (M )/r̄ contribution characterizes quantum-corrections to the classical SdS3 solution. Since ℓ ≈ 2cLP and c ≫ 1, as
required by holography, the qSdS is not a Planck-sized black hole, but rather has a horizon
much larger than the Planck length. Further, the renormalized Newton’s constant G3 (2.12)
takes into account the modification of the definition of mass due to the higher curvature
corrections [12]. Finally, we emphasize that analyzing the semi-classical Einstein’s equations
for a free conformally coupled scalar results in the metric (2.11) to leading order in LP [7].

## PDF page 10

with metric functions
r2
µℓ a2
−
+ 2,
r
r
R32
2
ℓ
ω2 =
,
(ℓ + xr)2

G(x) = 1 − x2 − µx3 −

H(r) = 1 −

Σ=1+

a2 4
x ,
R32

a2 x2
.
r2

(3.2)
(3.3)

2

2

ds |x=0 = −H(r)dt + H

−1

2

(r)dr + r

2

(

2
a
dφ + 2 dt .
r

)

(3.4)

Since the rotating C-metric (3.1) is a solution to the bulk Einstein equations, we are
guaranteed the brane geometry is a solution to the induced theory of gravity (2.13).
However, at this stage it would be naive to interpret this solution as the quantum Kerr-dS3
black hole. This is because we have not yet accounted for bulk regularity conditions, which
will affect more than just the periodicity of the angular variable φ. In fact, we know the
‘naive metric’ (3.4) does not capture all of the correct features because the ring singularity
lives on the brane, yet the above metric does not have a ring singularity at r = 0 but rather
a standard curvature singularity. We will see momentarily how the ring singularity makes
an appearance.
Bulk regularity. Notice that the Killing vector ∂φ no longer has vanishing norm at a
zero xi of G(x). Rather, the Killing vector
ξ b = ∂φb + ax2i ∂tb ,

(3.5)

obeys ξ 2 |xi = 0. Avoiding conical defects at x = xi requires us to identify points along
the integral curves of the vector (3.5) with an appropriate period. To determine the
correct periodicity, consider the rotating C-metric (3.1) near a zero x = xi such that
G(x) ∼ G′ (xi )(x − xi ) (see appendix C). Removal of a conical singularity at x = xi requires
one simultaneously perform the coordinate transformation t̃ = t − ax2i φ together with the
9

This is clarified when one moves to coordinates where x = cos θ, such that the singularity lies at the
θ = π/2 edge of the r = 0 disk.
10
These coordinates are Boyer-Lindquist-like. To see this, perform the successive coordinate transformations
t → t̂ + aφ and φ → −φ̂/(1 + a2 /R32 ) on (3.4). The resulting geometry is the (t̂, φ̂, r) submanifold of the
four-dimensional Kerr-dS metric in Boyer-Lindquist coordinates; e.g., eq. (2.2) of [29] with θ = π/2, µℓ = 2M ,
and where our blackening factor H(r) is different by a shift in a2 /R32 .

–9–

JHEP06(2023)127

Our conventions largely follow [12], apart from the substitutions R32 = −ℓ23 (or ℓ3 = iR3 )
and a → −a. Here a is a parameter encoding the rotation of the bulk black hole (the angular
momentum per unit mass), and in the limit a = 0 we recover the static C-metric (2.6).
Evaluating the bulk Kretschmann scalar invariant R̂abcd R̂abcd , there is a curvature singularity
when r2 Σ = r2 + a2 x2 = 0, i.e., when both r = 0 and x = 0. This is the familiar ring
singularity in Kerr black holes.9
Despite rotation, the x = 0 hypersurface remains umbilic, obeying Kij = −ℓ−1 hij , and
is thus a natural location to place the de Sitter brane. The geometry on the brane is 10

## PDF page 11

same periodicity condition on φ (2.10). Specifically, singling out the smallest positive root
x = x1 , then
4π
4πx1
φ ∼ φ + ∆φ ,
∆φ = ′
=
,
(3.6)
|G (x1 )|
3 − x21 + ã2
where to arrive to the second equality we recast the parameter µ in terms of x1
µ=

1 − x21 − ã2
,
x31

ã ≡

ax21
.
R3

(3.7)

Thus, identifying points along the orbits of ξ b are made on surfaces of constant
(3.8)

The remaining zeros xi ̸= x1 are dealt with by cutting off the bulk spacetime at x = 0, and
gluing to a second region such that the complete space is comprised of a bulk region with
x ∈ [0, x1 ], leaving a space which is free of conical singularities at x = xi .
Returning to the naive geometry at x = 0 (3.4), consider the asymptotic limit r → ∞.
The metric is asymptotic to ‘rotating dS3 ’, where the dtdφ component grows like a constant.
Unfortunately, the coordinates are not canonically normalized due to the periodicity
in φ (3.6). In fact, since points along orbits of (3.5) are identified, the periodicity in
φ (3.6) returns one to a different point in time t: from (3.8), we see that with t̃ ∼ t̃
then t ∼ t + 2πηax21 , where η ≡ ∆φ/2π. This means we cannot just rescale coordinates
(t, r, φ) → (t̄, r̄, φ̄) as done in the static case (2.11). Additionally, the periodicity alters the
asymptotic form of the metric such that the dtdφ grows as r2 , which would seem to imply
a diverging angular momentum.11
We can remedy the situation by changing coordinates (t, φ) to (t̃, φ̃) where t = t̃ + ax21 φ̃
and φ = φ̃ + C t̃ for some constant C. In the asymptotic limit, the t̃ − φ̃ component of the
naive brane metric (3.4) will have go as
(

ht̃φ̃ =

ax2
C + 21
R3

)

r2 + (a − ax21 + Ca2 x21 ) + O(1/r) .

(3.9)

Judiciously, we choose C ≡ −ax21 /R32 = −ã/R3 to eliminate the r2 divergence. Making
this choice deals with the undesired asymptotic growth, however, φ̃ is still not periodic
in 2π. This is now easily resolved by a simple rescaling, t̃ = η t̄ and φ̃ = η φ̄, such that
the transformation
(
)
ã
t = η(t̄ + ãR3 φ̄) ,
φ = η φ̄ −
t̄ ,
(3.10)
R3
puts the brane geometry in a more canonical form.12 Inverting the transformation (3.10),
1
t̄ =
(t − ãR3 φ) ,
η(1 + ã2 )

1
ã
φ̄ =
φ+
t
2
η(1 + ã )
R3
(

11

)

,

(3.11)

To see this, perform the following coordinate transformation in the brane geometry (3.4) t → t̃ + ax21 φ̃
and φ → φ̃. Then, it is straightforward to show for large r the ht̃φ̃ component of the geometry diverges as r2 .
12
We can recover the canonically normalized coordinates to describe rotating AdS3 black holes [12] upon
the double replacement ℓ3 → iR3 and aAdS3 → −adS3 , such that ãAdS3 → iãdS3 .

– 10 –

JHEP06(2023)127

t̃ ≡ t − ax21 φ .

## PDF page 12

we see the Killing vectors ∂t and ∂φ transform as
1
ã
∂t =
∂t̄ +
∂
2
η(1 + ã )
R3 φ̄
(

)

,

∂φ =

(
)
1
∂
−
ãR
∂
3
t̄ .
η(1 + ã2 ) φ̄

(3.12)

Consequently, now the rotational Killing vector (3.5) is ξ b = η −1 ∂φ̄ .
With the coordinate change (3.10), the brane metric does not quite have the canonical
asymptotic form of a rotating de Sitter black hole. We still need to redefine the radial
coordinate r. Following [12], let
rs = −

R3 ãη
x1

√

2 − x21 = −

2ãR3 2 − x21
3 − x21 + ã2

.

(3.13)

Altogether, the geometry on the brane in the canonically normalized coordinates (t̄, r̄, φ̄) is
(

(

ds2 |x=0 = − η 2
(

(

+ η2

)

)

4ã2
r̄2 µℓη 2
1−ã2 + 2 − 2 −
dt̄2
r
x1
R3
)

4ã2
r̄2 µℓ(1+ã2 )2 η 4 r R32 ã2 µ2 x21 η 4
1−ã2 + 2 − 2 −
+
r̄2
r̄2
x1
R3

(

)

)−1

dr̄2

(3.14)

µℓã2 R32 η 2
ℓ
+ r̄ +
dφ̄2 +R3 ãµx1 η 2 1+
(dφ̄dt̄+dt̄dφ̄) ,
r
x1 r
(

2

)

where we have kept both r and r̄ when convenient.
3.2

Black hole on the brane

Let us now scrutinize the brane geometry (3.14). First, we identify the mass M as
(

8G3 M ≡ 1 − η

2

4ã2
1 − ã + 2
x1

)

2

=1−

4[x21 − ã2 (x21 − 4)]
,
(3 − x21 + ã2 )2

(3.15)

where G3 ≡ L4 G3 /ℓ is the ‘renormalized’ three-dimensional Newton’s constant13 [12]. Since
the brane theory is generally three-dimensional Einstein-de Sitter gravity plus higherderivative corrections, we do not have a generic Komar-like mass integral in which we
compute M . Rather, here we have identified the mass as the subleading constant term
in ht̄t̄ , as done in Einstein-de Sitter gravity, and used G3 to encompass all of the higherderivative corrections entering at order ℓ2 in the brane action (2.13) [30]. Similarly, we have
identified the three-dimensional angular momentum J to be
4G3 J ≡ −R3 ãµx1 η 2 =

4R3 ã(x21 + ã2 − 1)
,
(3 − x21 + ã2 )2

(3.16)

where again the renormalized Newton’s constant plays the role of accounting for higherderivative corrections to the angular momentum. Importantly, notice M and J depend on
ã2 and x21 , and the parameter ℓ does not make an explicit appearance.
13

Here we operate under the assumption that G3 ≡ L4 G3 /ℓ holds to all orders in ℓ.

– 11 –

JHEP06(2023)127

√

r̄2 − rs2
r2 ≡
,
(1 + ã2 )η 2

## PDF page 13

(

ds2qKdS = −

r̄2
µℓη 2
1 − 8G3 M − 2 −
r
R3

)

dt̄2

(

r̄2
(4G3 J)2 µℓ(1 + ã2 )2 η 4 r
+ 1 − 8G3 M − 2 +
−
r̄2
r̄2
R3
(

µℓã2 R32 η 2
+ r̄2 +
r

)

)−1

dr̄2

(3.17)

ℓ
dφ̄ − 4G3 J 1 +
(dφ̄dt̄ + dt̄dφ̄) .
x1 r
(

2

)

Since the metric (3.17) is an exact solution to the full semi-classical theory of gravity on the
brane (2.14), we refer to the three-dimensional spacetime as the quantum Kerr-dS3 black
hole (qKdS). We say ‘black hole’ because, as we describe below, this geometry possesses
both an inner and outer black hole horizon, shrouding a ring singularity, and a cosmological
horizon. We say ‘quantum’ because it includes all orders of semi-classical backreaction due
to the CFT, where terms in the metric proportional to µℓ are understood to be quantum
corrections to the classical Kerr-dS3 conical defect. Justification of this terminology will be
given when we compute the renormalized CFT stress-tensor ⟨TijCFT ⟩.
Before we analyze the brane geometry (3.17) in more detail, there are a few special
limits to consider. First, clearly, when the rotation a → 0, then J = 0 and the geometry
reduces to the static metric (2.11), the quantum Schwarzschild-de Sitter black hole [7].
Next, in the limit of vanishing backreaction ℓ → 0, in which the gravitational effects of
14

An additional argument from thermodynamics, independent of the first law, is that one can directly
compute the thermodynamics of the bulk black hole + braneworld system (with either dS or AdS slicing
of the brane) via an on-shell Euclidean action approach. This was done in the case of non-rotating AdS
C-metric with a brane of AdS or dS slicing [31] where one finds precisely the same formulae for the mass,
given by a temperature derivative of the on-shell action.

– 12 –

JHEP06(2023)127

We emphasize, at this stage, the mass M (3.15) and angular momentum J (3.16) are
identifications. Justification for this, in part, comes from the fact that these quantities
satisfy a first law of thermodynamics, as we demonstrate in the next section. 14 Essentially,
as argued in [11] the mass of the black hole on the brane is identified as the mass of the
bulk black hole intersecting the brane. A feature distinguishing AdS and dS braneworld
constructions is how the mass (3.15) coincides with a conserved charge. This is because
asymptotically dS spacetimes do not have a boundary which makes providing an invariant
notion of conserved charges more difficult. From the brane perspective, one could compute
conserved charges, for example, by calculating the Brown-York quasi-local stress tensor on
slices at past and future infinity [32]. The mass found should then coincide with the mass
of the bulk black hole intersecting the brane at I ± . In practice this is difficult, however,
because the theory on the brane is a complicated higher-order theory of gravity, a context in
which defining conserved charges is also a subtle matter (AdS braneworld models encounter
the same subtlety in this regard). Alternatively, one can use the method developed in [33],
which does not require entering an asymptotic region. It would be worthwhile to explore
this question and verify the mass identified in the first law coincides with an invariant
conserved charge.
With the substitutions (3.15) and J (3.16)s, the brane geometry (3.14) takes the form

## PDF page 14

the cutoff CFT are suppressed (where G3 → G3 ), the metric (3.17) takes the form of the
classical Kerr-dS3 conical defect spacetime (see appendix A). Thirdly, when the parameter
√
µ (3.7) vanishes, i.e., x1 = 1 − ã2 , then both M = J = 0, resulting in the empty dS3
√
geometry. The mass M will also be zero when x1 = 9 − ã2 . When this is the case, J ̸= 0
and µ ̸= 0,
32ãR3
512ãR3
4G3 J =
,
µ= 2
,
(3.18)
2
2
(6 − 2ã )
(ã − 9)3 (ã2 − 3)2
and we can think of the brane geometry as quantum rotating dS3 .

ζ b = ∂t −

a
∂φ
ri2

(3.19)

becomes null at roots ri of H(r). Define the function Q(r) ≡ r2 H(r). Since Q(r) is a
quartic polynomial in r, it will have generally have either four, two, or zero real roots.
Here we focus on the case when there are four real roots, which we will see later enforces
conditions on the physical parameters a and µ. The three positive roots to Q(r) are the
cosmological horizon rc , the outer black hole horizon r+ and inner black hole horizon r− ,
obeying r− ≤ r+ ≤ rc . The fourth root, rn , is negative and resides behind the singularity
at r = 0. Using H(rc ) = 0, and H(r± ) = 0, we can express
2
R32 = rc2 + r+
+ rc r+ + r− (rc + r+ + r− ) ,

µℓ =

(rc + r+ )(rc + r− )(r+ + r− )
2 + r r + r (r + r + r ) ,
2
r c + r+
c +
− c
+
−

a2 =

rc r+ r− (rc + r+ + r− )
2 + r r + r (r + r + r ) .
rc2 + r+
c +
− c
+
−

(3.20)

The blackening factor H(r) factorizes as
H(r) =

1

(rc − r)(r − r+ )(r − r− )(r + rc + r+ + r− ) .
R32 r2

(3.21)

The limit r− → 0 coincides with a = 0, while r+ = r− = 0 corresponds to µ → 0, resulting
in the Kerr-dS3 geometry with a single cosmological horizon.
Since the black hole is stationary, the positive roots ri to H(r) correspond to rotating
horizons with rotation Ωi ,
a (x2 r2 − R2 )
Ωi ≡ 2 12 i 2 23 ,
(3.22)
R3 (ri + a x1 )

– 13 –

JHEP06(2023)127

Horizons and closed timelike curves. While the metric (3.17) is in the correct canonically normalized coordinates (t̄, r̄, φ̄), in what follows we will perform calculations in the
naive background (t, r, φ) (3.4), and perform the appropriate coordinate transformation.
This is largely done for convenience, but also because both metrics share nearly all of the
same qualitative features.
In the static case, roots of H(r) correspond to the Killing horizons of the Killing vector
∂t . With rotation, the Killing vector

## PDF page 15

where we used the transformations (3.12), to express ζ b and define ζ̄ b
η(1 + ã2 ) b
) ζ = ∂t̄b + Ωi ∂ b .
ζ̄ b ≡ (
φ̄
a2 x21
1 + r2

(3.23)

i

Further, relative to ζ̄ b , the surface gravity κi associated with each horizon ri is given by
η(1 + ã2 ) ri2 ′
η(1 + ã2 )
1
)
(
)
κi = ( 2
|H
(r
)|
=
|R2 µℓri − 2ri4 − 2a2 R32 | ,
i
2
2
2
2
2
ri + a x 1 2
ri + a x1 2R32 ri 3

(3.24)

κc = −
κ+ =

η(1 + ã2 )
(
) (rc − r+ )(rc − r− )(r+ + r− + 2rc ) ,
2R32 rc2 + a2 x21

η(1 + ã2 )
( 2
) (rc − r+ )(r+ − r− )(rc + r− + 2r+ ) ,
2R32 r+
+ a2 x21

κ− = −

(3.25)

η(1 + ã2 )
( 2
) (rc − r− )(r+ − r− )(rc + r+ + 2r− ) .
2R32 r−
+ a2 x21

Notice the cosmological horizon surface gravity κc vanishes when rc = r+ or rc = r− , and
similarly for the other surface gravities. We explore these extremal limits momentarily.
When r− → 0, i.e., vanishing rotation, we recover the surface gravities of the cosmological
horizon and black hole horizon of the qSdS black hole [7]. Additionally, in the limit of
vanishing backreaction, then r± → 0 such that κ± → 0.
As mentioned previously, in the naive coordinates (3.4), a computation of the
Kretschmann scalar reveals a curvature singularity at r = 0. In the canonically normalized coordinates (3.17), r = 0 corresponds r̄ = rs , corresponding to a ring singularity,
and is endowed from the bulk black hole solution. Moreover, near the ring singularity
there exists the possibility of closed timelike curves. Relative to the canonically normalized
metric (3.17), the norm of the axial Killing vector ∂φ̄ is
∂φ̄2 = hφ̄φ = r̄2 +

µℓã2 R32 η 2
.
r

(3.26)

Thus, for sufficiently small and negative r, the vector ∂φ̄ becomes timelike, the orbits of
which are closed curves around the rotation axis. However, unlike the rotating qBTZ black
hole, these closed timelike curves do not become naked.
When all of the roots to Q(r) are distinct, then standard methods [34] lead to a
maximal extension of the quantum Kerr-dS3 black hole. Generally, the resulting conformal
diagram is infinite in extent and is nearly identical to the Kruskal extension of the classical
four-dimensional Kerr-dS black hole. The aforementioned closed timelike curves may be
eliminated by an appropriate periodic identification [35], such that constant t̄ hypersurfaces
are closed and span two black hole regions with opposite spin, cutting through intersections
of r = rc and r = r+ (see figure 2 for a diagram).

– 14 –

JHEP06(2023)127

where we used the definition ζ̄ b ∇b ζ̄ c = κζ̄ c . Explicitly,

## PDF page 16

rn

=
r

r

r

r+

r+

r

rc

=

=

rc

r

=
r+

=

rc

=

=

=

r

r=∞

Figure 2. Penrose diagram of a neutral quantum Kerr black hole in dS3 . Shown here is the global
structure with periodic identifications made along constant t̄ hypersurfaces. The diagram has infinite
extent in the vertical directions while the dashed edges are identified.

Ergoregions. As with classical Kerr-de Sitter spacetimes, the qKdS black hole has a
stationary limit surface and two ergoregions associated with the outer black hole and
cosmological horizons. Explicitly, the time-translation Killing vector ∂t in the naive metric
has the norm N
a2
N = −H(r) + 2 .
(3.27)
r
Clearly, at the outer and cosmological horizons, where H = 0, then ∂t is spacelike. The
locus of points where N = 0 yields a stationary limit surface, satisfying r(R32 − r2 ) = R32 µℓ.
Since there exist regions in between the outer and cosmological horizons where ∂t is timelike,
there are two ergoregions, where an observer is forced to move in the direction of rotation
of the outer black hole horizon or cosmological horizon (the black hole and cosmological
ergoregions, respectively). With the appearance of ergoregions, one can in principle examine
the Penrose process of energy extraction in the qKdS solution in morally the same way
as a classical four-dimensional Kerr-de Sitter black hole (see, e.g., [36]). At least for
small backreaction, it is expected the Penrose process in the cosmological ergoregion is
not possible.
3.3

Extremal, Nariai, ultracold, and lukewarm limits

As with the four-dimensional Kerr-de Sitter black hole, the quantum Kerr-dS3 has a number
of limiting geometries. Specifically, (i) extremal or ‘cold’ limit, where r+ = r− ; (ii) rotating
Nariai limit, where rc = r+ ; (iii) the ‘ultacold’ limit where rc = r+ = r− , and (iv) the
‘lukewarm’ limit, where the surface gravities κc = κ+ . Below we summarize each of these

– 15 –

JHEP06(2023)127

r

r

r−

=

r−

rn

r

r

rn
=

=
r+

r=0

=

rc

r−
=
r

r−

rn

r

r=∞

=

=

=

r=0

r

r = −∞

r

r

r

r = −∞

## PDF page 17

limiting geometries and briefly explore their features, leaving the details to appendix D. Our
analysis primarily follows [35], and for simplicity, we work with the naive metric (t, r, φ) (3.4)
except when stated otherwise.
Extremal black hole: r+ = r− . The extremal black hole corresponds to when the outer
and inner black hole horizons coincide. In this limit the surface gravity of the outer horizon
κ+ = 0, and, correspondingly the Hawking temperature T+ of the black hole vanishes, i.e.,
the black hole is ‘cold’. Moreover, parameters a2 and µℓ may be cast as
4
3r+
,
R32

µℓ = 2r+ −

3
4r+
.
R32

(3.28)

In the extremal limit the global structure of the spacetime changes because now the (double)
black hole horizon moves to an infinite proper distance away from all other portions of the
geometry, such that the black hole interior is inaccessible from the rest of the spacetime.
In the near horizon limit of extremal qKdS, we can no longer express the metric in
coordinates (t, r, φ) as they become singular. Rather, we perform a coordinate transformation
analogous to [37, 38]
r = r+ + λρ ,

t=

τ
,
λ

φ=ϕ−

aτ
2λ,
r+

(3.29)

where upon taking λ → 0 we find
(

dρ̂2
ds2ex = Γ −ρ̂2 dτ̂ 2 + 2
ρ̂
with
Γ=

2
r+
2 /R2 ,
1 − 6r+
3

)
2
+ r+
(dϕ + k ρ̂dτ̂ )2 ,

(3.30)

2aR32
2).
r+ (R32 − 6r+

(3.31)

k=−

This is the near horizon extremal Kerr (NHEK) geometry for the quantum-corrected
Kerr-dS3 . Formally it has the same structure as the NHEK region of four-dimensional
Kerr-(A)dS spacetimes, and has the form of a fibered product of AdS2 and the circle.15 As
such, following [38], the isometry group is SL(2, R) × U(1).
√
Notice from (3.28) that a = 0 when r+ = 0 or r+ = R3 / 3, which, respectively,
√
corresponds to µℓ = 0 or µℓ = 2R3 /3 3. The latter is simply the Nariai limit of the
quantum Schwarzschild-de Sitter black hole [7], which we explore in more detail below.
Rotating Nariai black hole: rc = r+ . The Nariai solution occurs when the cosmological and outer black hole horizons coincide rc = r+ ≡ rN . Then
a2 =

2
rN
2
(R2 − 3rN
),
R32 3

(µℓ)N =

15

2rN 2
2
(R − 2rN
).
R32 3

(3.32)

Upon direct comparison, the functions Γ and k do not match those presented in [38] in the θ = π/2 limit.
This is because our form of the metric (3.4) is not exactly of Boyer-Lindquist form. Putting the naive metric
in such a form would lead to the same form functions. Likewise, had we started with the metric in (t̄, r̄, φ̄)
coordinates (3.17), the near horizon extremal geometry would have the same structure with appropriately
modified form functions.

– 16 –

JHEP06(2023)127

2
a 2 = r+
−

## PDF page 18

1
ρ

1

=

=

−

ρ

1

ρ

−

=

=

1

ρ

√
√
Notice when a = 0 we recover rN = R3 / 3 and (µℓ)N = 2R3 /3 3, the Nariai limit of the
static Schwarzschild-de Sitter black hole. Physically, the Nariai black hole is the largest
black hole which may fit inside the cosmological horizon, saturating at µN . Moreover, the
rotating Nariai black hole is generally larger than the static Nariai solution, analogous to
how the charged Nariai black hole is larger than the neutral geometry.
The blackening factor H(r) vanishes when r = rN making the (t, r, φ) coordinate system
incompatible in describing the Nariai geometry. Thus, introduce coordinates [35]
r = rN + ϵρ ,

t=

Γτ̂
,
ϵ

φ=ϕ−

a
2ϵ
rN

τ,

(3.33)

and send ϵ → 0 such that the naive geometry (3.4) becomes
(

dρ2
ds2N = Γ −(1 − ρ2 )dτ̂ 2 +
(1 − ρ2 )

)
2
+ rN
(dϕ + kρdτ̂ )2 ,

(3.34)

where
Γ=

2
R32 rN
2 − R2 ,
6rN
3

k=−

2aR32
2 − R2 ) .
rN (6rN
3

(3.35)

Hence, the Nariai limit of the qKdS black hole has the product structure of dS2 fibered over
a circle, written here in static patch coordinates, and has the isometry group U(1) × SL(2, R).
When a = 0, then Γ = R32 /3, leading to the non-rotating Nariai metric [39–41] with product
geometry dS2 × S2 . A static patch observer is restricted to the region ρ ∈ (−1, 1), where
ρ = −1 corresponds to the black hole horizon and ρ = +1 the cosmological horizon, at
a finite proper distance apart. To draw the Penrose diagram (see figure 3) it is useful to
switch to global coordinates [29]

– 17 –

JHEP06(2023)127

Figure 3. Penrose diagram of the Nariai qKdS black hole. The black hole and cosmological
horizons are located at ρ = −1 and ρ = 1, respectively, and are in thermal equilibrium at a non-zero
temperature. Clearly there is a finite proper distance between the two horizons. Future and past
infinity I ± are located at ρ = ∞, while the past and future black hole singularities correspond to
ρ = −∞. The left and right sides of the diagram are identified.

## PDF page 19

√
1
tan(η/2) = tanh
sinh−1 ( 1 − ρ2 sinh τ̂ )
2
(

)

cos ψ = ρ(cosh2 τ̂ − ρ2 sinh2 τ̂ )−1/2
k
sin(η + ψ)
log
2
sin(η − ψ)
(

χ=ϕ+
such that

(

ds2N = Γ

,

)
2
+ rN
(dχ + k tan ηdψ)2 ,

(3.37)

where ψ ∼ ψ + 2π and η ∈ (−π/2, π/2) cover the all of the dS2 portion.
Naively, when rc = r+ the surface gravities (3.24) of the cosmological and black hole
horizons vanish, κc = κ+ = 0. However, in the Nariai geometry (3.34), the two horizons are
in thermal equilibrium at a non-zero temperature TN . We will return to this in section 4.
Ultracold black hole: rc = r+ = r− . The ultracold black hole is the limit when all of
the horizons coincide, namely, rc = r+ = r− ≡ ruc . The form of the metric can be found
directly from the Nariai geometry (3.34). Since the Nariai geometry becomes singular when
rN = r− , the coordinates (ρ, τ̂ ) require an appropriate rescaling
√

ρ=

2ruc − δ
X,
R3

√

τ=

R3 R3 ruc
T,
2ruc − δ 4

(3.38)

where τ = Γτ̂ , and subsequently take the limit δ → 2ruc . The resulting geometry is
ds2uc =

R3 ruc
2aX
2
(−dT 2 + dX 2 ) + ruc
dϕ − 3 dT
4
ruc
(

)2

.

(3.39)

This geometry is of the form of a fibered product of two-dimensional Minkowski space over
a circle. Via an appropriate coordinate transformation (see [35]), the ultracold solution
can also be expressed as a fibered product of two-dimensional Rindler space and a circle.
In the limit of vanishing rotation there is no ultracold solution, but rather a static Nariai
black hole.
Lukewarm black hole: κc = κ+ . As with all Kerr-de Sitter black holes, the quantum
Kerr-dS3 has a lukewarm limit. This occurs when the surface gravities of the cosmological
and outer black hole horizons coincide at a value different from the surface gravity of the
Nariai black hole. Notably, the geometry is non-singular in (t, r, φ) coordinates. Thermodynamically speaking, this spacetime is another example of where the black hole and
cosmological horizon are in thermal equilibrium. We will return to this limit in section 4,
however, in appendix D we find its limiting form in the naive brane geometry.
Before moving on, we point out that the special limits of the quantum Kerr-dS3 black
hole has qualitatively similar features to dS3 black hole solutions to topologically massive
gravity, cf. [42–44]. Indeed, the asymptotically warped dS3 black hole (obtained from
discrete global identifications of warped dS3 ) has a Nariai limit whose U(1) × U(1) isometry
is enhanced to a SL(2, R) × U(1) isometry group. It would be interesting to understand the
relation between quantum dS3 black holes and warped dS3 black holes in more detail.

– 18 –

JHEP06(2023)127

−dη 2 + dψ 2
cos2 η

(3.36)

)

## PDF page 20

3.4

Holographic conformal matter stress-tensor

We have been referring to the geometry on the brane (3.17) as a quantum black hole since,
via the holographic dictionary, it is a solution to the semi-classical equations of motion (2.14)
to all orders in backreaction. Let us now justify this claim and solve for the expectation
value of the CFT stress-energy tensor ⟨Tij ⟩ sourcing the black hole.
Following [12], we decompose ⟨T ij ⟩ = ⟨T ij ⟩0 + ℓ2 ⟨T ij ⟩2 + . . . in increasing powers of ℓ2 .
Specifically, the leading order contribution is
1
8πG3 ⟨T ij ⟩0 = Rij − δ ij

2
R− 2
R3

)

,

(3.40)

while the O(ℓ2 ) contribution is
9
1
8πG3 ⟨T ij ⟩2 = 4Rik Rjk − □Rij − RRij + ∇i ∇j R
4
4
(
)
1 i 13 2
1
1
2
+ δj
R − 3Rkl + □R −
.
2
8
2
2R34

(3.41)

It proves is more computationally convenient to determine ⟨Tij ⟩ in the naive metric (3.4)
and then transform into the (t̄, r̄, φ̄) than working directly with the metric (3.17). Thus, in
the naive background we find the only non-vanishing components of the stress-tensor are
1
1 µℓ
⟨T tt ⟩0 = ⟨T rr ⟩0 = − ⟨T φφ ⟩0 =
,
2
16πG3 r3
1 3µℓa
⟨T φt ⟩0 = −
,
16πG3 r5

(3.42)

[
]
µℓ
2 2
4
2
90a
R
−
11r
+
R
r(18r
−
19µℓ)
,
3
3
32πG3 R32 r7
[
]
µℓ
4
2 2
2
⟨T rr ⟩2 = −
r
+
30a
R
+
R
r(6r
−
7µℓ)
,
3
3
32πG3 R32 r7
[
]
µℓ
4
2 2
2
⟨T φφ ⟩2 = −
10r
−
120a
R
−
R
r(24r
−
29µℓ)
,
3
3
2
32πG3 R3 r7
3aµℓ
⟨T tφ ⟩2 = −
,
2πG3 r5
[
]
3aµℓ
4
2 2
2
⟨T φt ⟩2 = −
23r
−
70a
R
−
R
r(30r
−
32µℓ)
3
3
32πG3 R32 r9

(3.43)

and, for completeness,
⟨T tt ⟩2 = −

Notice that while ⟨T ii ⟩0 = 0, as one would expect for a CFT stress-tensor, we see ⟨Tii ⟩2 =
−3(µℓ)2 /32πG3 r6 . A non-termminating trace at higher order powers is a consequence of
the fact that the CFT on the brane has an ultraviolet cutoff.
Transforming to the (t̄, r̄, φ̄) coordinates
⎛

⟨T īj̄ ⟩ = Λīi Λjj̄ ⟨T ij ⟩ ,

Λīj ≡

1

⎜
∂ x̄i
1
⎜ 0 r
=
j
2
∂x
η(1 + ã ) ⎝ ã
− R3

– 19 –

0
√

−ãR3

0

1

1+ã2
r 2 −rs2

⎞
⎟

0 ⎟
⎠,

(3.44)

JHEP06(2023)127

2

(

## PDF page 21

we find the leading order contribution to the stress-tensor is
(

)

µℓ
3ã2 R32
2
1
−
2ã
+
,
16πG3 (1 + ã2 )r3
x21 r2
µℓ
⟨T r̄r̄ ⟩0 =
,
16πG3 r3
(
)
µℓ
3ã2 R32
φ̄
2
⟨T φ̄ ⟩0 = −
2 − ã + 2 2
,
16πG3 (1 + ã2 )r3
x1 r
⟨T t̄t̄ ⟩0 =

3µℓãR3
16πG3 (1 + ã2 )r3

1+

3µℓã
⟨T φ̄t̄ ⟩0 =
16πG3 (1 + ã2 )R3 r3

(

ã2 R32
x21 r2

(3.45)

)

R2
1 − 2 32
x1 r

,
)

,

where recall r is given in (3.13). In what follows it suffices to only study the stress-tensor
to this order and therefore we do not include the cumbersome expressions of ⟨T īj̄ ⟩ at higher
orders in ℓ. Notice these components are equivalent to the stress-tensor of the CFT in
the rotating quantum BTZ black hole upon the simultaneous Wick rotations ℓ3 → iR3
and ã → iã.
For practical purposes, we can view the black hole as being characterized by R3 , x21 , ã
and ℓ. Notably, the mass M (3.15) and angular momentum J (3.16) do not explicitly depend
on ℓ, they only depend on ℓ through the renormalized Newton’s constant G3 . Moreover, at
least with respect to the leading order components of the stress-tensor (3.45), the parameter
ℓ only appears in the overall prefactor. Combining these two observations indicates ⟨T ij ⟩0
depends on backreaction only through G3 . This is no longer the case at higher orders,
however, as can be gleaned from the O(ℓ2 ) contributions (3.43).
In the static case, the quantum SdS black hole (2.11), the dependence of the stress-tensor
on the mass was entirely captured by a single function F (M ) (2.12) [7],
⟨T īj̄ ⟩qSdS
=
0

1 ℓF (M )
diag(1, 1, −2) .
16πG3 r̄3

(3.46)

Unfortunately this is not possible when rotation is included: the dependence of the stresstensor on M and J cannot be characterized solely by a single function F (M, J). However,
as in [12], we instead identify F (M, J) with the leading contribution at large r̄. Precisely,
consider ⟨T t̄t̄ ⟩0 at large r,
⟨Tt̄t̄ ⟩0 =

µℓ √
1 + ã2 η 3 (1 − 2ã2 ) + O(r̄−5 ) ,
16πG3 r̄3

√
where we used r ≈ r̄/ 1 + ã2 η. We thus define
√
√
8 1 + ã2 (1 − 2ã2 )
3
2
2
F (M, J) ≡ µη 1 + ã (1 − 2ã ) =
(1 − x21 − ã2 ) ,
(3 − x21 + ã2 )3

(3.47)

(3.48)

such that for large r̄
⟨T t̄t̄ ⟩0 ≈

1 ℓF (M, J)
,
16πG3
r̄3

– 20 –

(3.49)

JHEP06(2023)127

⟨T t̄φ̄ ⟩0 =

(

## PDF page 22

Comparison to perturbative backreaction. It is illustrative to compare the holographic stress-tensor (3.45) to the renormalized quantum stress-tensor due to perturbative
backreaction of a free conformally coupled scalar field in conical Kerr-dS3 . We present the
detailed computation in appendix B, summarizing the final result below:
⟨T tt ⟩ =

∞
LP ∑
1
8πG3 n=1 rn3

⟨T rr ⟩ =

∞
LP ∑
cn
,
16πG3 n=1 rn3

⟨T φφ ⟩ = −

(

Ãn
An + 2
rn

∞
LP ∑
1
8πG3 n=1 rn3

(

∞
3R3 LP ∑
1
⟨T tφ ⟩ = −
8πG3 n=1 rn3

⟨T φt ⟩ = −
Here the denominator rn ≡

√

)

,

Ãn
Bn + 2
rn

)

(

)

Ẽn
En + 2
rn

,

∞
3LP ∑
1
Fn
En + 2
3
8πG3 R3 n=1 rn
rn

(

(1)

(3.50)
,

)

.

(2)

r2 dn + R32 dn with

16
πnβ+
2 nπβ−
+ sin2
,
2 + β 2 ) sinh
2
2
(β+
−
[
(
)
(
)]
4
2
2 nπβ+
2
2 πnβ−
d(2)
=
β
sin
−
β
sinh
.
n
−
+
2 + β2 )
2
2
(β+
−
d(1)
n =

[

(

)

(

)]

(3.51)

The remaining coefficients An , Ãn , cn , etc., are cumbersome to write here, but explicitly
given in appendix B and satisfy An + c2n − Bn = 0. Moreover, the parameters β+ ≡ 2rc /R3
and β− = −8G3 J/rc are related to the periodicity of coordinates in t and φ, respectively,
where rc is the cosmological horizon radius. The infinite sum arises from using the method
of images to determine the appropriate Green function solving the scalar equation of motion,
where, unlike the Schwarzschild-dS3 case [7], there are a countably infinite number of
distinct images.

– 21 –

JHEP06(2023)127

and similarly for the other components of the stress-tensor (3.45). Notice F (M, J) will
vanish when µ = 0 (i.e., a2 = 1 − x21 ), the empty dS3 solution, or when ã2 = 1/2, and it
reduces to F (M ) (2.12) for the static solution when ã = 0.
It is worth repeating there are two perspectives to interpret the solution on the brane
and the parameters defining the background. From the bulk viewpoint, the solution is
naturally characterized by L4 , ℓ, µ and a. Meanwhile, from the point of view of the brane,
the natural quantities parameterizing the solution include the radius R3 fixing the scale of
the brane geometry, cG3 , G3 M , and G3 J. The cutoff length of the three-dimensional effective
theory is L4 = cLP , such that for large c, this cutoff is much larger than the Planck length,
where quantum gravity effects dominate. Thus, the ‘quantum’ black holes constructed
here, as described in the introduction, are much larger than the Planck length. Hence, our
solution can be viewed as a valid solution to the problem of semi-classical backreaction.

## PDF page 23

Gµν +

1
gµν = 8πG3 ⟨Tµν ⟩
R32

(3.52)

perturbatively in LP . Leaving the details to appendix B, we expand the metric ansatz
ds2 = N (r)2 f (r)dt2 +

dr2
+ r2 (dθ + k(r)dt)2
f (r)

(3.53)

to linear order in LP such that
N (r) = N0 (r)+LP N1 (r) ,

f (r) = f0 (r)++LP f1 (r) ,

k(r) = k0 (r)+LP k1 (r) .
(3.54)

At O(L0P ) we recover the classical Kerr-dS3 geometry, while perturbatively solving the
semi-classical Einstein equations yields
N1 (r) =
f1 (r) =

∞
∑
R32
an cn − 2β+ β− en
,
2
2
bn rn3
2(β+ + β− ) n=1
∞
2 + β 2 )3
∑
4hn (r)(an cn − 2β+ β− en ) − cn rn4 (β+
−
n=1

k1 (r) = −

2 + β 2 )b2 r 3
64r2 (β+
− n n

∞
2 − β 2 )e + β β c (c − 4)
(β+
R3 ∑
+ − n n
− n
,
8r2 n=1
b2n rn

(3.55)

,

(3.56)

(3.57)

with coefficients an , bn etc. are presented in appendix B. Clearly, the terms to linear order in
LP are more cumbersome than the quantum corrected geometry due to the holographic stresstensor. Since f1 ∼ 1/r as r → ∞, the correction to the blackening factor does resemble
the 4D Schwarzschild-like contribution that emerges from the holographic calculations.
However, as this derivation can only be accomplished to linear order in LP , a limit of the
perturbative approach, we cannot justify these quantum corrections induce a black hole

– 22 –

JHEP06(2023)127

Comparing to the holographic stress-tensor (3.45), we notice the tensor components
share a similar structure. In particular, coefficients aside, the two sets of tensors have a
comparable radial dependence, comparing the r̄ dependence in (3.45) and rn above. Of
course, once the infinite sums are performed, the radial dependence in (3.50) is sufficiently
more complicated than its holographic counterpart. Likewise, substituting in the explicit
expressions of β± results in expressions with cumbersome dependence on M and J. This
is in contrast to the static case explored in [7], where the radial dependence in either the
holographic or perturbative methods was the same, going as 1/r̄3 (3.46). In summary, due
to the complicated radial dependence, with non-zero rotation the result of a holographic
CFT backreacting on the geometry is far simpler than that of a single conformally coupled
scalar field. Indeed, the holographic stress-tensor (3.45) is clearly non-singular everywhere
outside of the ring singularity at r = 0. This is far less obvious looking at the perturbative
stress-tensor.
Moreover, the complicated radial dependence in the perturbative backreaction (3.50)
lead to far more complicated quantum corrections to the Kerr-dS3 geometry, a result from
solving the three-dimensional semi-classical Einstein equations

## PDF page 24

horizon; one must consider higher order corrections. It is also worth emphasizing that the
backreacted geometry due to a single free field would have lead to a black hole horizon on
the scale of the Planck length, while the holographic quantum black hole horizon is of size
ℓ ∼ cLP ≫ LP .

4

Thermodynamics of quantum Kerr-dS3 black holes

4.1

Bulk thermodynamics

The C-metric (3.1) is known to describe a uniformly accelerating black hole or a pair of such
black holes, whose accelerating is mediated by a cosmic string. Since the bulk black hole is
accelerating it is natural to wonder whether it is sensible to study the thermodynamics of
accelerating black holes. It is worth emphasizing that while the black hole is accelerating,
it is nonetheless stationary, having a time-translation Killing symmetry ∂t .16 Moreover,
the black hole(s) are held fixed at a proper distance away from the acceleration horizon.
Consequently, the black hole has a sensible thermodynamic interpretation (see, e.g., [45]),
having a well-defined temperature and entropy.
When analyzing the thermodynamics, it is useful to introduce the parameters [12]
z≡

R3
,
ri x 1

ν≡

ℓ
,
R3

α≡

ax1
ã
=
,
R3
x1

(4.1)

where ri is a positive real root of the bulk blackening factor H(r), representing each horizon
of braneworld black hole. We can express x1 , µ and ri solely in terms of these parameters,
x21 =

1 + νz 3
,
z 2 [1 + νz + α2 z(z + ν)]

ri2 = R32
µx1 =

1 + νz + α2 z(z + ν)
,
1 + νz 3

(4.2)

(z 2 − 1)(1 + α2 (1 + z 2 ))
.
1 + νz 3

The first expression is found by solving H(ri ) = 0 for x21 , from which the other two relations
readily follow.17 Moreover, the bare and renormalized Newton’s constants are
2G3 ℓ
G4 = 2L4 G3 = √
,
1 − ν2

G3 =

16

L4
G3
G3 = √
.
ℓ
1 − ν2

(4.3)

We point out that ∂t is not globally timelike. Rather, it is timelike in the region between the acceleration
horizon and the outer black hole horizon. The bulk thermodynamics we describe correspond to this region.
Alternatively, ∂t becomes spacelike in the regions between the inner and outer black hole horizons and
acceleration horizon and null infinity. In those regions the roles of coordinates (t, r) are switched.
17
Via the reassignments ℓ23 → −R32 and a → −a, we recover the relevant parameters of the quantum BTZ
via z 2 → −z 2 , ν 2 → −ν 2 and νz → νz.

– 23 –

JHEP06(2023)127

Here we analyze the thermodynamics of the quantum Kerr-dS black hole. As with the
geometry, there are two perspectives to view the thermodynamics of the system: the
thermodynamics of the classical bulk black hole, and the thermodynamics of the quantum
black hole on the brane. Due to the holographic construction, the formulae we derive in
either perspective appear the same, however, with conceptually different interpretations.
Since the parent solution is well understood, we begin with the thermodynamics of the bulk.

## PDF page 25

The limit of vanishing backreaction now coincides with small ν, and we take ν 2 < 1, which
guarantees the bulk is asymptotically AdS4 . Using the parameters (4.2), we can recast the
mass M (3.15) and angular momentum J (3.16)
M=

1 √
(z 2 − 1)[1 + α2 (1 + z 2 )][9z 2 − 1 + 8νz 3 + α2 (9z 4 − 1 + 8νz 3 )]
1 − ν2
, (4.4)
8G3
(3z 2 − 1 + 2νz 3 + α2 (1 + 4νz 3 + 3z 4 ))2

αR3 √
z(z 2 − 1)[1 + α2 (1 + z 2 )] (1 + νz 3 )(1 + νz + α2 z(z + ν))
J=
1 − ν2
.
G3
(3z 2 − 1 + 2νz 3 + α2 (1 + 4νz 3 + 3z 4 ))2
√

(4.5)

α (z 2 − 1) (1 + νz 3 )(1 + νz + α2 z(z + ν))
Ωi =
.
R3
z(1 + νz)(1 + α2 (1 + z 2 ))
√

(4.6)

Additionally, the surface gravity κi (3.24) relative to ζ̄ b yields a temperature Ti = κi /2π,
Ti =

1 (z 2 (1 + νz) + α2 (1 + 2νz 3 + z 4 ))|(2 + 3νz − νz 3 + α2 (4z 2 + νz(z 4 + 3)))|
.
2πR3
z(1 + νz)(1 + α2 (1 + z 2 ))(3z 2 − 1 + 2νz 3 + α2 (1 + 3z 4 + 4νz 3 ))
(4.7)

We will deal with absolute value more carefully in the next section.
Lastly, the bulk horizon entropy is given by the Bekenstein-Hawking area formula
Area(ri )
2
(4)
SBH =
=
4G4
4G4
=

π
G4

∫ x1

∫ 2π

dφ̄
0

0

(

ri2 ℓ2
a2 x21
dx
η
1
+
(ℓ + ri x)2
ri2

)

ηℓx1 (ri2 + a2 x21 )

(ℓ + ri x1 )
√
πR3
1 − ν 2 z(1 + α2 (1 + z 2 ))
=
.
G3 (3z 2 − 1 + 2νz 3 + α2 (1 + 3z 4 + 4νz 3 ))

(4.8)

Altogether, the mass (4.4), angular momentum (4.5), angular velocity (4.6), temperature (4.7) and entropy (4.8) constitute the thermodynamics of the rotating AdS4 bulk black
hole. In the α = 0 limit, one recovers the thermodynamics of the static AdS4 bulk [7]. One
may derive the bulk thermodynamics using a canonical partition function by evaluating
the on-shell bulk gravity action via an appropriate modification of the presentation given
in [31]. Additionally, by explicit computation it is straightforward to verify 18
(4)

(4)

∂z M − Ti ∂z SBH − Ωi ∂z J = 0 ,

∂α M − Ti ∂α SBH − Ωi ∂α J = 0 ,

(4.9)

such that the bulk system obeys the first law
(4)

dM = Ti dSBH + Ωi dJ ,

(4.10)

for all values of the parameters, including any value of the brane tension, as controlled by ν.
18

Here we replace the absolute value in Ti by an overall minus sign for reasons we explain momentarily.

– 24 –

JHEP06(2023)127

As described in the previous section, the canonically normalized Killing vector ζ̄ b =
∂t̄b + Ωi ∂φ̄ (3.23) generates rotating horizons at the positive roots ri with rotation Ωi (3.22),
now expressed as

## PDF page 26

4.2

Semi-classical thermodynamics on the brane

Thermodynamics with multiple horizons. The quantum de Sitter black hole comes
with three horizons which are generally at different temperatures. Consequently, each
horizon generally has its own thermodynamics, satisfying its own first laws, as we now
show. The mass (4.4), angular momentum (4.5), and angular velocity (4.6) of the quantum
black hole all take the same form in terms of parameters (4.1). The temperature (4.7)
encodes the temperature of each horizon of the quantum black hole, where we remind the
reader the outer and inner black hole horizons correspond to the outer and inner bulk
black hole horizons localized on the brane, while the cosmological horizon arises from the
bulk acceleration horizon intersecting the brane. To distinguish each horizon, it is useful
to slightly modify the notation for z via zc = R3 /rc x1 and z± = R3 /r± x1 to denote the
cosmological and black hole horizons, respectively. Then, from the surface gravities (3.25)
T+ = −Ti (z+ ) ,

Tc = Ti (zc ) ,

T− = Ti (z− ) ,

(4.11)

where we used r− < r+ < rc such that z− > z+ > zc . Consequently, the black hole horizon
is generally hotter than the cosmological horizon, Tc < T+ , such that the system is not in
thermal equilibrium; an observer located between the cosmological and (outer) black hole
horizon is in a system characterized by two temperatures. There are three special cases,
where the horizons degenerate, when the outer black hole and cosmological horizons are in
thermal equilibrium, as we explore below.
The most notable difference between the bulk and brane black hole thermodynamics is
(4)
the interpretation of the entropy (4.8). On the brane, this entropy SBH is equal to the sum
of gravitational entropy and the entanglement entropy of the holographic CFT [12]. Thus,
(3)
the bulk entropy is identified with the generalized entropy on the brane Sgen ,
(4)

(3)

(3)
(3)
SBH = Sgen
= Sgrav
+ SCFT .

(4.12)

This relation is exact to all orders in semi-classical backreaction codified by ν. The
gravitational entropy is computed using Wald’s entropy functional [15],
SWald = −2π

∫

dA
H

∂L
ϵab ϵcd ,
∂Rabcd

(4.13)

√
where dA = dd−2 x q is the codimension-2 area element of the bifurcate horizon H, with
qab = hab + na nb − ua ub being the induced metric, for spacelike and timelike unit normals

– 25 –

JHEP06(2023)127

From the brane perspective, the thermodynamics of the classical bulk system doubles as
the thermodynamics of the quantum de Sitter black hole. It is worth mentioning that, even
without accounting for backreaction, de Sitter thermodynamics is more subtle than their
flat or AdS space counterparts. Firstly, this is because de Sitter space lacks an asymptotic
region to introduce boundary conditions which fix thermoodynamic data to define a thermal
ensemble. Moreover, the first law of cosmological horizons [34] comes with a minus sign
which begs how the thermodynamics of the dS static patch should be understood. In what
follows, we ignore these subtleties, though it would be interesting to return to them in the
future, adapting the quasi-local approach developed in [46, 47] (see also [48, 49]).

## PDF page 27

na and ua , respectively. The binormal ϵab = (na ub − nb ua ) satisfies ϵ2 = −1, and we define
(d − 1)-dimensional metric in directions orthogonal to the horizon. Moreover, L refers to
the Lagrangian density defining the theory. With respect to the induced theory of gravity
on the brane (2.13), the gravitational entropy is
(3)
Sgrav
=

1
4G3

√

∫

[

dx q 1 + ℓ

2

(

H

3
ab
R − g⊥
Rab + O(ℓ4 /R36 ) .
4
)

]

(4.14)

(3)
SBH =

1
4G3

∫

(

√

2πri η
dx q =
4G3
H

a2 x2
1 + 21
ri

)

1 + νz (3)
=√
Sgen .
1 − ν2

(4.15)

Therefore, the Bekenstein-Hawking entropy includes semi-classical backreaction effects.
(3)
Formally, the matter entropy SCFT is given by the difference
(3)

(3)
(3)
SCFT = Sgen
− Sgrav
.

(4.16)

Notably, the matter entropy enters at linear order in ν,
(3)

(3)

(3)

(3)
SCFT ≈ Sgen
− SBH = −νzSBH ,

(4.17)

in contrast with the higher-curvature contributions to the gravitational entropy which enter
(3)
at order ν 2 . Recall that the central charge c = L24 /G4 ≈ νR3 /2G3 , such that SCFT is
proportional to c. As in the quantum BTZ case [12], generally the matter entropy will be
dominated by entanglement across the horizon(s) in CFT states with large Casimir effects.
(4)
Interpreting SBH as the generalized entropy of the quantum black hole, the bulk first
law (4.10) leads to a semi-classical first law for each horizon19
dM = T+ dSgen,+ + Ω+ dJ ,

(3)

(4.18)

(3)
dM = −Tc dSgen,c
+ Ωc dJ ,

(4.19)

(3)

dM = −T− dSgen,− + Ω− dJ ,

(4.20)

where Ωc = Ωi (zc ) and Ω± = Ωi (z± ) are the angular speeds of the cosmological and black
hole horizons. Combining the first two first laws yields
(3)
(3)
0 = T+ dSgen
+ Tc dSgen
+ (Ω+ − Ω− )dJ .

(4.21)

Our first law is consistent with the semi-classical first laws for static two-dimensional (A)dS
black holes in [48, 53]. Notice the minus sign in the first law of the cosmological horizon
remains even in the quantum-backreacted geometry. Consequently, adding positive energy
into the static patch reduces the total entropy of the system, with the entropy of pure dS
19
It is possible to assign a dynamical thermodynamic pressure P3 ∝ −Λ3 to the quantum black hole,
whose variations are induced by variations in the tension of the brane [50]. The first law then acquires a
V dP3 term, where V is the ‘thermodynamic volume’ conjugate to P3 [51, 52].

– 26 –

JHEP06(2023)127

We see higher-curvature corrections to entropy enter at order ℓ2 , such that the dominant
contribution to the entropy at leading order in backreaction is the three-dimensional
Bekenstein-Hawking entropy

## PDF page 28

being maximal, such that de Sitter black holes behave as instantons constraining the states
of the original de Sitter degrees of freedom (cf. [54–56]).
At this stage, there are two limits of interest. The first is the quantum de Sitter limit,
at z = 1 or µ = 0, and, consequently,
M = J = Ωi = 0 ,
√
2πR3 1 − ν 2
1
(3)
Sgen =
,
Tc =
,
4G3 1 + ν
2πR3

(4.22)
(4.23)

1 (z 2 − 1)(1 + α2 (1 + z 2 ))(9z 2 − 1 + α2 (9z 4 − 1))
,
8G3
(3z 2 − 1 + α2 (1 + 3z 4 ))2
√
αR3 z(z 2 − 1)(1 + α2 (1 + z 2 )) 1 + α2 z 2
J=
,
G3
(3z 2 − 1 + α2 (1 + 3z 4 ))2
√
α(z 2 − 1) 1 + α2 z 2
Ωc =
,
R3 z(1 + α2 (1 + z 2 ))
1
2(1 + 2α2 z 2 )(z 2 + α2 (1 + z 4 ))
Tc =
,
2πR3 z(3z 2 − 1 + α2 (1 + 3z 4 ))(1 + α2 (1 + z 2 ))
M=

Sc =

(4.24)

πR3
z(1 + α2 (1 + z 2 ))
,
G3 (3z 2 − 1 + α2 (1 + 3z 4 ))

where it is understood that here z = zc . It is straightforward to show the resulting
thermodynamics reproduces that of the classical Kerr-dS3 (see appendix A), namely,
πR3
(3)
Sgen
|ν=0 =
4G3

(√

√

8G3 J
8G3 J
(1−8G3 M )+i
+ (1−8G3 M )−i
R3
R3

where we used the relation

√

x + iy +

√

√

x − iy = 2 x +

)

= SKdS3 ,

(4.25)

√
x2 + y 2 / 2.

√

Thermodynamics of degenerate horizons. As described in section 3, the quantum
Kerr black hole has special limits where the two or more horizons become degenerate.
Of interest are the extremal (r+ = r− ), Nariai (rc = r+ ), and lukewarm (Tc = T+ )
geometries. The extremal black hole is one with a vanishing temperature, Text = 0. Naively,
the Nariai black hole will have a vanishing temperature, however, in its near horizon
geometry, the temperature of the black hole and cosmological horizon will be in thermal
equilibrium at a non-zero temperature TN . The precise form of the temperature can be
found, for example, by removing the conical singularity in the Euclideanized section of
the (naive) Nariai geometry (3.34), given via the Wick rotation τ̂ → iτ̂E and a → iaE ,
√
resulting in TN = (2π Γ)−1 . To connect to the canonical geometry, we relate the Nariai
radii rN and r̄N via (3.13). Lastly, the lukewarm limit occurs when the outer black hole
and cosmological horizons are in thermal equilibrium at a temperature different from
the Nariai temperature. Though the resulting expression is cumbersome and not very

– 27 –

JHEP06(2023)127

where we see the temperature of the quantum dS3 cosmological horizon is the same as
classical dS3 . Second, when backreaction vanishes ν → 0, then z± → ∞ since r± → 0 and
we have

## PDF page 29

illustrative, the precise temperature can be solved for explicitly by setting T+ = Tc (using
the surface gravities (3.25)) and following the method described in appendix D. The
lukewarm temperature is proportional to (rc − r+ )/2πR32 , with rc ̸= r+ .

5

Discussion

Other three-dimensional quantum black holes: here we focused on neutral rotating
quantum de Sitter black holes. It is natural to ask whether other types of three-dimensional
quantum black holes are possible using a similar braneworld construction. Firstly, one may
consider charged quantum black holes simply by starting from the charged AdS4 C-metric.
Although there is no need for counterterms for the Maxwell field in AdS4 [21, 57], a Maxwell
action is nevertheless generated on a brane at finite distance in the bulk, further modifying
the geometry of the quantum black hole [58]. Similarly, starting from the accelerating
Taub-NUT AdS4 black hole, one would conceivably find a quantum Taub-NUT black hole on
the brane. Altogether, via suitable modifications to the AdS4 C-metric, one could develop
a catalog of charged, rotating, Taub-NUT quantum (A)dS black holes in three-dimensions.
A further generalization would be to consider quantum black holes with scalar hair.
One way to do this is to consider bulk Einstein gravity in addition to a conformally
coupled scalar field. Black hole solutions to this theory have a rich history, dating back
to Bekenstein [59, 60], including exact generalizations of the charged C-metric [61] and
Plebanski-Demianski family of metrics [62]. In holographic renormalization, adding scalar

– 28 –

JHEP06(2023)127

In this article we used braneworld holography to construct a three-dimensional quantumcorrected Kerr-de Sitter black hole exactly accounting for backreaction effects due to a
conformal field theory. By stark contrast, there are no de Sitter black holes in threedimensions, only conical defect geometries with a single cosmological horizon. Thus,
semi-classical backreaction alters the defect geometry so as to induce inner and outer black
hole horizons, which hide a ring singularity, sharing many qualitative features with the
classical four-dimensional Kerr-de Sitter solution. With three horizons, we uncovered the
extremal, Nariai, and ‘ultracold’ limits of the semi-classical black hole, which appear as
fibered products of a circle and AdS2 , dS2 , or two-dimensional Minkowski space, respectively.
Moreover, the thermodynamics of the classical bulk black hole, described by the rotating
AdS4 C-metric, has a dual interpretation on the brane as thermodynamics of the semiclassical Kerr-dS3 black hole. Specifically, the standard first law of thermodynamics in the
bulk becomes a semi-classical first law, where the four-dimensional Bekenstein-Hawking
area-entropy is identified with the three-dimensional generalized entropy, given by the sum
of the Wald entropy due to higher curvature corrections, and the matter entropy of the CFT.
In essence, we have derived the semi-classical generalization of the first law of cosmological
horizons of Gibbons and Hawking [34]. As in the classical four-dimensional Kerr-dS solution,
the limiting geometries of the quantum Kerr-dS black hole give rise to scenarios of thermal
equilibrium, including the Nariai and lukewarm limits where the temperatures of the
cosmological and outer black hole horizons coincide. Therefore, quantum-corrections greatly
enrich the thermodynamic structure of three-dimensional de Sitter solutions.
There are multiple future directions to take this work, some of which we list below.

## PDF page 30

fields in the bulk requires additional counterterms thereby modifying the induced theory on
the brane, resulting in, presumably, an exact quantum black hole with scalar hair.

Dimensional reduction and deviations away from extremality: spherical reduction of a d ≥ 4 dimensional classical de Sitter black hole near its extremal, Nariai, or
ultracold limits results in different two-dimensional effective theories of dilaton-gravity (see,
e.g., [67, 68]). Alternatively, the low-energy dynamics of spherical reduced three-dimensional
empty dS is characterized by de Sitter Jackiw-Teitelboim gravity, where the dilaton only
ranges over positive values. Spherical reduction of three-dimensional quantum de Sitter
black holes in their nearly extremal limits will be described by modified dilaton theories of
gravity, including R2 corrections owed to reduction of the induced theory on the brane. It
would be interesting to study these effective two-dimensional theories to better understand
deviations away from extremal quantum dS black holes, along the lines of [68].
Double holography and quantum Kerr-dS/CFT: black holes localized on KarchRandall braneworlds enjoy a ‘doubly-holographic’ perspective, where the d-dimensional
induced gravity theory on the brane has a dual description in terms of a defect CFTd−1 ,
which interacts with the CFTd on the AdSd+1 boundary [25, 69–71]. As recognized in [7],
the de Sitter braneworld provides a means to explore dS/CFT holography, where gravity on
the brane may be characterized by defect Euclidean CFTs at I ± of the dS hyperboloid. The
hope would be to use this type of double holography to study dS/CFT in a controlled way.
The quantum Kerr-black hole presents an opportunity to study another kind of holographic duality, namely, the Kerr-CFT correspondence [72] (see also [38, 73]). In particular, a

– 29 –

JHEP06(2023)127

Higher dimensional quantum black holes: the quantum Kerr-dS3 black hole is another example of an exact description of a localized three-dimensional black hole in a
Randall-Sundrum braneworld, belonging to the class of the solutions uncovered in [13, 14]
(see also [63], where the brane tension was detuned from the bulk acceleration). It is
natural to wonder whether one can construct higher-dimensional quantum black holes
in a similar fashion. Extrapolating from the four-dimensional bulk models, holographic
considerations predict backreaction due to conformal fields is expected to similarly induce
quantum corrections to the geometry. For example, a semi-classical four-dimensional brane
black hole would include a ℓµ/r2 correction to the standard 1/r gravitational potential, a
behavior inherited from its parent AdS5 black hole.
Thus far, however, there are no known exact quantum black holes in higher dimensions.
This is because finding static brane localized black holes in higher dimensions has proven
challenging, both analytically and numerically (for a review, see [64]). The essential feature
of the four-dimensional C-metric which is exploited is that there is a natural location
to place the brane, at x = 0, where the Israel-junction conditions are automatically
satisfied. A higher-dimensional analog of the C-metric exuding this feature is not known
to exist [65], making the construction of exact quantum black holes difficult. Perhaps
numerical techniques together with the large-D approximation of bulk Einstein gravity, as
was recently accomplished to describe evaporating brane black holes [66], can be adapted
to construct exact quantum black holes in higher-dimensions.

## PDF page 31

Holographic information of quantum de Sitter black holes: exact semi-classical
black holes allow one to explore proposals of information theoretic descriptions of gravity
including backreaction effects. For example, in the context of the (static) quantum BTZ black
hole, both ‘complexity=volume’ and ‘complexity=action’ conjectures were analyzed [74],
where complexity=volume was found to a have a consistent semi-classical expansion, while
complexity=action was unable to produce the classical limit. Likewise, quantum de Sitter
black holes offer the chance to study holographic complexity in de Sitter space, which thus
far has largely been unexplored (see, however, [75–77]). There are at least two ways forward
with the de Sitter braneworld set-ups. One could attempt to exploit the aforementioned
doubly holographic interpretation to understand the complexity of bulk quantum fields,
however, this would require deeper insight into the relation between the CFT3 and the
Euclidean defect CFT2 . Alternately, complexity in terms of holographic state preparation,
as in [78–80], can be adapted into models of de Sitter braneworlds, where the de Sitter
hyperboloid represents time evolution of the dual boundary CFT state prepared by a
Euclidean path integral.
Specific to rotating qBTZ and quantum Kerr-dS black holes, it would be worthwhile
to see how complexity of formation — the volume-complexity of a black hole minus the
analogous volume of the relevant vacuum spacetime — is modified due to backreaction. In
fact, complexity of formation for classical rotating black holes was found to be controlled
by the thermodynamic volume familiar to the framework of extended black hole thermodynamics [81]. Likewise, it would be interesting to see whether the thermodynamic volume of
rotating quantum black holes yields a similar description of their complexity of formation.
Lastly, doubly holography of AdS braneworlds have provided a means to study the
black hole information paradox by computing the fine grained entropy of Hawking radiation
using the ‘island rule’ [23, 82, 83]. It would be worth exploring the formation of islands in
quantum de Sitter black hole backgrounds which incorporate all orders of semi-classical
backreaction. Progress in this regard has already been made in the static case [84].

Acknowledgments
We are grateful to Roberto Emparan, Juan Pedraza, and Manus Visser for discussions
and useful correspondence. EP is supported by the Cosmoparticle Initiative at University
College London. AS is supported by the Simons Foundation via It from Qubit: Simons
Collaboration on quantum fields, gravity, and information, and EPSRC.

– 30 –

JHEP06(2023)127

four-dimensional extremal Kerr-(A)dS black hole is dual to (half of a chiral) two-dimensional
CFT, a consequence that there exist boundary conditions of the near horizon extremal Kerr
solution which enhance the U(1) isometry of SL(2, R) × U(1) to a Virasoro algebra with
non-trivial central charge. Moreover, in the case of Kerr-dS, the rotating-Nariai black hole
has a dual description in terms of a two-dimensional (Euclidean) CFT [29], akin to the
dS/CFT correspondence. Since the limiting geometries of the quantum Kerr-dS3 have the
same isometry subgroup as their four-dimensional classical counterparts, it is plausible these
quantum black holes have an additional dual description in terms of a two-dimensional
chiral CFT, however, with a different central charge. It would be interesting to pursue this
duality further and better understand the dual CFT using the classical bulk.

## PDF page 32

A

Geometry of classical Kerr-dS3

In this appendix we review the geometry of the classical Kerr-dS3 black hole. To appreciate
its properties, we first briefly recall facts about conical geometries.

ds2 = dr2 + r2 dϕ2 ,

(A.1)

where, due to conical geometry, the angular variable is not 2π-periodic but rather, 0 ≤
ϕ < 2π − δ. To make the difference between the cone and the flat space metric (where ϕ
is 2π-periodic) explicit, rescale the angular coordinates to have standard 2π-periodicity.
Namely, define φ such that ϕ = γφ, where φ is 2π-periodic.21
Of interest are (2 + 1)-dimensional spacetimes with conical singularities. Generally the
spacetime is singular at the tip of the cone due to geodesic incompleteness and because there
is a curvature singularity at the tip. The stress-energy tensor sourcing such geometries is
that of a point particle of mass M (and spin J if the spacetime is stationary), whose angular
deficit δ is generally a function of the mass and spin. This also means that, classically, there
are no three-dimensional flat or de Sitter black holes as we now briefly review.
(2+1)-dimensional Kerr-de Sitter. The general solution for (2+1)-dimensional Einstein’s equations of a point particle of mass m and spin J in a background with positive
cosmological constant Λ = R12 is
3

ds2 = −N (r)dt2 + N −1 (r)dr2 + r2 (dφ + Nφ dt)2 ,

(A.2)

with lapse and shift metric functions
N (r) = m −

r2
16G23 J 2
+
,
2
r2
R3

Nφ =

4G3 J
.
r2

(A.3)

The mass and spin are respectively related to the conserved charges associated with the
time-translation and rotational Killing symmetries [8]. The lapse N has roots r±
⎛

R2
2
r±
= 3 ⎝m ±
2

√

m2 −

20

(

8G3 J
R3

)2

⎞
⎠,

(A.4)

When 0 < γ < 1, δ is referred to as an angular deficit, while δ is an angular excess when γ < 0.
More generally, near a conical singularity in spaces of constant (Gaussian) curvature K,
√ the two2
dimensional geometry has line element ds√
= dr2 + γ 2 FK (r)2 dφ2 , with F0 = r, FK = K −1/2 sin( Kr) when
K > 0 (elliptic), or FK = |K|−1/2 sinh( |K|r) when K < 0 (hyperbolic). Moreover, the range of the r
coordinate changes with K; being 0 < r < ∞ for K ≤ 0 and 0 < r < 2√πK for K > 0.
21

– 31 –

JHEP06(2023)127

Conical singularities. In Riemannian geometry, a conical singularity is a singular point
of the n-dimensional manifold in the proximity of which the metric locally looks like the
spherical quotient Sn−1 /G by a finite subgroup G. For example, for the cyclic group G = Zk ,
the resulting geometry is isomorphic to Rn with an angular deficit δ, i.e., a wedge of δ-radians
cut out from the n-dimensional plane with the edges identified, where δ = 2π(1 − γ), with
γ ≡ 1/k.20 Unsurprisingly, the geometry of cone is an example of a manifold with a conical
singularity. Explicitly, the metric on the (flat) 2-cone in polar coordinates (r, ϕ) is

## PDF page 33

with only a single positive root r+
R3
r+ =
2

(√

8G3 J
m+i
+
R3

√

8G3 J
m−i
R3

)

.

(A.5)

√

φ̃ = γφ − αt/R3 ,

t̃ = γt + αR3 φ ,

r̃/R3 =

(r/R3 )2 + α2
.
γ 2 + α2

(A.6)

This brings the Kerr-dS3 geometry (A.2) into an empty dS3 form
(

r̃2
ds = − 1 − 2
R3
2

)

(

r̃2
dt̃ + 1 − 2
R3

)−1

2

dr̃2 + r̃2 dφ̃2 ,

(A.7)

however, the coordinates t̃ and φ̃ do not have the same periodicity as genuine dS3 , where
(t, r, φ) ∼ (t, r, φ + 2π). Now
(t̃, φ̃) ∼ (t̃ + 2πR3 α, φ̃ + 2πγ) .

(A.8)

This reveals Kerr−dS3 is a conical defect geometry with angular deficit δ = 2πγ, and is a
quotient of dS3 . Moreover, the Schwarzschild-dS3 geometry (where J = 0 = α) is also a
√
conical defect with deficit δ = 1 − 8G3 M , or a particle of mass m whose stress-energy
tensor Tab = mδ(r)δa0 δb0 sources the geometry.
The thermodynamics of the cosmological horizon is straightforward to work out (cf. [86])
m = γ 2 − α2 ,
Tc =

αγR3
α
,
Ωc = −
,
4G3
γR3
2πrc
2πR3 γ
SBH =
=
,
4G3
4G3
J =−

γ 2 + α2
,
2πγR3

(A.9)

satisfying the first law
dM = −Tc dSBH + Ωc dJ ,

(A.10)

where m = 1 − 8G3 M . Moreover, the system obeys the following Smarr relation
0 = −Tc SBH + Ωc J − 2P Vc ,

(A.11)

Λ
where P = − 8πG
= − 8πG1 R2 is a thermodynamic pressure and Vc = πrc2 the conjugate
3
3 3
thermodynamic volume. If we allow for variations to the dynamical pressure, the above
first law is extended to include a +Vc dP term.

– 32 –

JHEP06(2023)127

2 + r 2 while J = −ir r /4G R .
In the main text we set m = 1 − 8G3 M . Notice R32 m = r+
+ −
3 3
−
When J = 0, we recover Schwarzschild-dS3 , where r− = 0.
The spacetime (A.2) is simply Kerr-dS3 , however, it is not a black hole. Here r+ is
identified as the cosmological horizon rc , there being no black hole horizon for reasons
given in the introduction. Rather, Kerr-dS3 is a conical defect geometry. To see this,
introduce dimensionless parameters γ ≡ rc /R3 and α ≡ −4G3 J/γR3 = ir− /R3 , satisfying
m = γ 2 − α2 , and consider the following coordinate transformation [6, 85]

## PDF page 34

B

Perturbative backreaction in Kerr-dS3

Here we study perturbative backreaction in the Kerr-dS3 conical defect geometry due to a
free conformally coupled scalar field Φ. The complete theory is characterized by
1
I=
16πG3

∫

√

1
d x −g(R − 2Λ) −
2
3

∫

√

1
d x −g
RΦ2 + (∇Φ)2
8
3

(

)

.

(B.1)

The energy-momentum tensor for Φ is found by varying the matter action

(B.2)
We will be interested in the case when Gµν = −gµν Λ, where Λ = R12 and R = 6/R32 . Upon
3
invoking the scalar equation of motion,
(

1
□ − R Φ = 0,
8
)

(B.3)

it follows that the stress-energy tensor is both traceless and conserved.
Below we compute the renormalized quantum stress-energy tensor ⟨Tµν ⟩ of the free
scalar field. We do this in two steps, primarily following the techniques developed for the
BTZ black hole and conical AdS3 [87–89], extending the analysis in [7]. First we determine
the Green function of the conical dS3 defect geometry (A.7) related to Kerr-dS3 using the
method of images. We then use point-splitting to compute the renormalized ⟨Tµν ⟩.
Green function in conical dS3 . We begin with the Green function G(x, x′ ) of pure
dS3 which solves the scalar field equations of motion (B.3). Imposing transparent boundary
conditions,22 the Green function is [90, 91]
G(x, x′ ) =

1
1
,
4π |x − x′ |

(B.4)

where |x − x′ | ≡ (x − x′ )a (x − x′ )a is the chordal or geodesic distance between x and
x′ in the four-dimensional embedding space R1,3 . The embedding coordinates xa =
(X1 , X2 , T1 , T2 )T for empty dS3 are
√

T1 =

√

r̃2 −R32 cosh(t̃/R3 ) ,

T2 =

√

r̃2 −R32 sinh(t̃/R3 ) ,

X2 = r̃ sin φ̃ ,
(B.5)
obeying −T12 + T22 + X12 + X22 = R32 , and where the metric ds2 = −dT12 + dT22 + dX12 + dX22
yields empty dS3 in static patch coordinates. Moreover, it is easy to verify
(
)
3
□−
GdS3 (x, x′ ) = 0
(B.6)
4R32
22

X1 = r̃ cos φ̃ ,

We choose transparent boundary conditions because the holographic computation naturally selects
these boundary conditions. More generically, the Green function solving the scalar field equation of motion
is 4πG(x, x′ ) = |x − x′ |−1 + λ|x + x′ |−1 , where λ is a parameter related to the boundary conditions one
imposes; transparent (λ = 0), Dirichlet (λ = −1) and Neumann (λ = 1).

– 33 –

JHEP06(2023)127

2 δIΦ
3
1
1
1
1
Tµν ≡ − √
= ∇µ Φ∇ν φ− gµν (∇Φ)2 − Φ∇µ ∇ν Φ+ gµν Φ□Φ+ Gµν Φ2 .
µν
−g δg
4
4
4
4
8

## PDF page 35

for x ̸= x′ , with the chordal distance being
|x − x′ | = [−(T1 − T1′ )2 + (T2 − T2′ )2 + (X1 − X1′ )2 + (X2 − X2′ )2 ]1/2
[

=

2R32 + 2

√

r̃2 − R32

√

(

r̃′2 − R32 cosh

t̃ − t̃′
R3

]1/2

)
′

′

− 2r̃r̃ cos(φ̃ − φ̃ )

(B.7)
.

⎛

⎞

cos(2πγ) sin(2πγ)
0
0
⎜
⎟
⎜
⎟
− sin(2πγ) cos(2πγ)
0
0
′
⎜
⎟.
H(γ, α ) = ⎜
0
0
cosh(2πα′ ) − sinh(2πα′ )⎟
⎝
⎠
0
0
− sinh(2πα′ ) cosh(2πα′ )

(B.8)

For integer n we observe H n (γ, α′ ) = H(nγ, nα′ ). When α = 0, we recover the identification
matrix for static dS3 related to the Schwarzschild-dS3 solution [7].
The Green function GCdS3 (x, x′ ) for the conical defect spacetime (A.7) then follows
using the method of images, where one sums over all distinct images of a point obtained by
the embedding space identification:
GCdS3 (x, x′ ) =

1 ∑
1 ∑
1
GdS3 (x, H n x′ ) =
,
4π n∈I
4π n∈I |x − H n x′ |

(B.9)

with
n ′

[ √

(

√

|x − H x | = 2 r̃2 − R32 r̃′2 − R32 cosh
′

(

′

− 2r̃r̃ cos φ̃ − φ̃ + 2πnγ

)

t̃ − t̃′ + 2πnα
R3

+ 2R32

)

]1/2

(B.10)

.

The summation range I ⊂ Z depends on the number of distinct images, and is related
to the nature of the identification matrix H. For the case of the Kerr-dS geometry, the
identification matrix (B.8) will act transitively on R1,3 such that there are a countably
infinite number of distinct images, i.e., I = Z. By contrast, in the limit of vanishing rotation
α = 0, the identification matrix H becomes cyclic, such that there are a finite number of
distinct images, N − 1, where N is the smallest positive integer such that H N = 1. This
implies γ is a rational number, which without loss of generality can be set to γ = 1/N .
The cyclic property is broken for the Kerr-dS3 identification matrix due to the lower block
matrix. An analogous story carries over for rotating BTZ and (static or rotating) conical
AdS3 [88, 89]. Notably, at this stage, upon the Wick rotation ℓ3 = iR3 , and J → −J,23 one
23

BTZ
BTZ
Moreover, r± → −ir±
such that γ → γBTZ and α → αBTZ = ir−
/ℓ3 = −i4G3 J/γBTZ ℓ3 .

– 34 –

JHEP06(2023)127

To construct the Green function GCdS3 (x, x′ ) for the conical defect spacetime (A.7) we
use the method of images, exploiting the fact the conical defect geometry is an orbifold
due to discrete identifications of dS3 . Namely, the Green function is given by summing
over the distinct images under the action respecting the periodicity conditions (A.8). In
particular, identified points are related by an element H ∈ SO(1, 3) on the embedding space
coordinates (B.5), except where now φ̃ ∼ φ̃ + 2πγ and t̃ ∼ t̃ + 2πα′ , where we defined
α′ = R3 α in (A.8) for notational convenience. Explicitly,

## PDF page 36

recovers the scalar field Green function in conical AdS3 [88], however, Wick rotating the
identification matrix (B.8) does not yield the appropriate identification matrix for conical
AdS3 or the rotating BTZ.
Renormalized quantum stress-tensor. The renormalized quantum stress tensor ⟨Tµν ⟩
is obtain from G(x, x′ ) using the point-splitting method [87, 88, 92, 93]. Specifically,
(

⟨Tµν (x)⟩ = lim
′

x →x

3 x x′
1
1
1
′
∇ ∇ G− gµν g αβ ∇xα ∇xβ G− ∇xµ ∇xν G+
gµν G .
4 µ ν
4
4
16R32
)

(B.11)

To evaluate each component of the renormalized stress tensor in the conical defect
background, we use the fact G(x, x′ ) is a symmetric biscalar, while its covariant derivatives
are bitensors. Thus, we invoke a generalization of Synge’s theorem for bitensors [92] (see
also eq. (54) of [94]):
′

lim
(∇xµ Aα1 ) = ∇xµ lim
(Aα1 ) − lim
(∇xµ Aα1 ) ,
′
′
′

x →x

x →x

(B.12)

x →x

where Aα1 is a bivector with equal weight at both x and x′ , whose coincidence limit exists.
Consequently, applying Synge’s rule (B.12) to the quantum stress tensor (B.11) we have:
3
1
⟨Tµν (x)⟩ = ∇xν lim
(∇xµ G)− lim
(∇xν ∇xµ G) − gµν g αβ ∇xβ lim
(∇xα G)− lim
(∇xβ ∇xα G)
′
′
x →x
x →x
x′ →x
x′ →x
4
4
(
)
1 x x
1
+ lim
− ∇µ ∇ν G+
gµν G .
(B.13)
x′ →x
4
16R32
[

]

[

]

To clarify,
∇xν lim
(∇xµ G) = ∂νx
′
x →x

(

)

lim
∂µx G − Γρνµ
′

x →x

(

lim
∂ρx G
′

x →x

)

,

(B.14)

where the coincident limit is taken before evaluating the ∂νx derivative. Meanwhile,
lim (∇xν ∇xµ G) = lim
(∂µx ∂νx G − Γρµν ∂ρ G) ,
′

x′ →x

x →x

(B.15)

where the limit x → x′ is taken at the end.
Evaluating the quantum stress-tensor (B.13) in the defect geometry (A.7) and performing the inverse coordinate transformation of (A.6) to return to (t, r, φ) coordinates

– 35 –

JHEP06(2023)127

Here G(x, x′ ) = GCdS3 (x, x′ ) is the Green function (B.9), the metric gµν is a function of the
′
spacetime point x, ∇xµ denotes a covariant derivative with respect to x, and ∇xµ denotes a
derivative with respect to the point x′ . Moreover, the coincident limit x → x′ amounts to
evaluating the resulting expression at x′ = x. Note that while normally the renormalization
of the stress tensor is difficult, here we simply subtract off the divergent n = 0 contribution
in the image sum in the coincident limit.

## PDF page 37

yields,
⟨T tt ⟩ =

∞
2 + β 2 )b − 3a ] + 2R2 g )c − 3β β e [8r 2 + (β 2 − β 2 )R2 ]
(4r2 [(β+
1 ∑
+ − n
n
− n
−
+
3 n n
3
,
2 + β 2 )2 d (r)5/2
8π n=1
(β+
n
−

⟨T rr ⟩ =

∞
1 ∑
cn
,
16π n=1 dn (r)3/2
∞
2 + β 2 )b ] + 2R2 ḡ )c − 3β β e [8r 2 + (β 2 − β 2 )R2 ]
(4r2 [3ān − (β+
1 ∑
+ − n
− n
−
+
3 n n
3
,
2 + β 2 )2 d (r)5/2
8π n=1
(β+
n
−

⟨T tφ ⟩ = −

∞
2 − β 2 ) + 2β 2 β 2 R2 ]
β+ β− cn [4r2 (cn − 4) − R32 an ] + en [4r2 (β+
3R3 ∑
−
− + 3
,
2 + β 2 )2 d (r)5/2
8π n=1
(β+
n
−

⟨T φt ⟩ = −

∞
2 − β 2 ) − R2 (β 4 + β 4 )]
β+ β− cn [4r2 (cn − 4) − R32 an ] + en [4r2 (β+
3 ∑
−
−
3 +
.
2 + β 2 )2 d (r)5/2
8πR3 n=1
(β+
n
−

(B.16)
Here we introduced parameters β+ ≡ 2γ and β− ≡ 2α′ /R3 and defined
nπβ+
nπβ−
2
+ β+
sinh2
,
2
2
[
(
)
(
)]
nπβ+
nπβ−
2
2
ān = 2 β+
sin2
+ β−
sinh2
,
2
2
[
(
)
(
)]
2 nπβ−
2 πnβ+
bn ≡ 2 sinh
+ sin
.
2
2
[

2
an = 2 β−
sin2

(

)

(

)]

(B.17)
(B.18)
(B.19)

cn ≡ 2 + cos(πnβ+ ) + cosh(πnβ− ) ,

(B.20)

en ≡ 2 sin(nπβ+ ) sinh(nπβ− ) ,
(
)
(
)
nπβ+
nπβ−
2
2
2
2
2
2
gn ≡ β−
(β+
− 2β−
) sin2
− β+
(β−
− 2β+
) sinh2
,
2
2
(
)
(
)
2
2
2
2 nπβ−
2
2
2
2 nπβ+
ḡn ≡ β+ (β+ − 2β− ) sinh
− β− (β− − 2β+ ) sin
,
2
2

(B.21)
(B.22)
(B.23)

and with denominator
4R2
nπβ+
2
dn (r) ≡ 2 3 2 β−
sin2
2
β+ + β−
[

(

)

2
− β+
sinh2

(

πnβ−
2

)

+ 2R3−2 r2 bn

]

.

(B.24)

We have already removed the divergent n = 0 contribution. Note that we recover components
of the renormalized stress-tensor for a free conformally coupled scalar field in conical
AdS3 [89] upon the Wick rotations R3 → −iL and β− → iβ− . To arrive at these expressions
we used the summation symmetry over negative and positive integers n ∈ Z such that
∑
1 ∑∞
n=1 (fn + f−n ), where f−n = ±fn depending on each summand fn . For
n∈Z/{0} fn = 2
r̃
example, ⟨T t̃ ⟩ has a numerator sin2 (nπγ) sinh(2πnα′ /R3 ) which is eliminated under the
sum symmetry between positive and negative integers.24 This symmetry eliminates all
mixed components with r̃.
24

In the non-rotating case a similar symmetry argument is made using H N = 1 (see eq. (3.42) in [89]).

– 36 –

JHEP06(2023)127

⟨T φφ ⟩ = −

## PDF page 38

To compare to the holographic stress-tensor it is useful to define
rn ≡ d1/2
n ,

2 (2)
dn = r2 d(1)
n + R3 d n ,

(B.25)

with
d(1)
n =

8bn
2
2) ,
(β+ + β−

d(2)
n =

4
nπβ+
2
β−
sin2
2
2
2
β+ + β−
[

(

)

2
− β+
sinh2

(

πnβ−
2

)]

,

(B.26)

so as to suggestively write the stress-tensor components as in (3.50) with coeffcients
A′n
,
rn2

A′n =

2 + β 2 )b − 3a ] + 2R2 g )c
(4r2 [(β+
n
− n
3 n n
,
2 + β 2 )2
(β+
−

Bn ≡

Bn′
,
rn2

Bn′ =

2 + β 2 )b ] + 2R2 ḡ )c
(4r2 [3ān − (β+
− n
3 n n
,
2
2
2
(β+ + β− )

En ≡

En′
,
rn2

En′ =

β+ β− cn [4r2 (cn − 4) − R32 an ]
,
2 + β 2 )2
(β+
−

Ãn = −
Ẽn =

2 − β 2 )R2 ]
3β+ β− en [8r2 + (β−
+
3
,
2 + β 2 )2
(β+
−

2 − β 2 ) + 2β 2 β 2 R2 ]
en [4r2 (β+
−
− + 3
,
2 + β 2 )2
(β+
−

Fn =

2 − β 2 ) − R2 (β 4 + β 4 )]
en [4r2 (β+
−
−
3 +
.
2 + β 2 )2
(β+
−
(B.27)

Quantum-corrected geometry. With the renormalized quantum stress-tensor at hand,
let us proceed and compute the quantum corrections to Kerr-dS3 by solving the threedimensional semi-classical Einstein equations
Gµν +

1
gµν = 8πG3 ⟨Tµν ⟩
R32

(B.28)

perturbatively in LP . Our strategy closely follows the AdS3 analysis presented in [89]. Our
starting point is the general form of the stationary (rotating) balck hole:
ds2 = N (r)2 f (r)dt2 +

dr2
+ r2 (dθ + k(r)dt)2 ,
f (r)

(B.29)

where k, f and N are the functions to be determined. Expanding to linear order in Lp
N (r) = N0 (r) + LP N1 (r) + O(L2P ) ,
f (r) = f0 (r) + +LP f1 (r) + O(L2P ) ,

(B.30)

k(r) = k0 (r) + LP k1 (r) + O(L2P ) .
We substitute these expressions back into the left hand side of (B.28) and match order by
order in LP with the expectation value for the stress energy tensor. At O(L0P ) we obtain
N0 = 1 ,

f0 = m −

r2
J2
+ 2,
2
R3 4r

– 37 –

k0 =

J
,
2r2

(B.31)

JHEP06(2023)127

An ≡

## PDF page 39

recovering the Kerr-dS3 metric (A.2), to a minor redefinition of the constants of integration
J. Note that we have also made the choice of a vanishing shift vector at infinity, which sets
a third integration constant to zero.
At linear order in LP , we solve the differential equations for the linear corrections to
the Kerr metric using that we have computed the stress-tensor to linear order in LP . It is
helpful to use the traceless property of the perturbative stress energy tensor,
⟨Ttt ⟩ = f02 ⟨Trr ⟩ −

(

1
m
J
− 2 ⟨Tφφ ⟩ + 2 ⟨Ttφ ⟩ .
2
r
R3 r
)

(B.32)

8πG3
N1 (r) =
LP
∫

f1 (r) =

∫

⟨Tφφ ⟩
dr 2r⟨Trr ⟩ +
,
rf0
(

)

[

(

dr −2f0 N1′ +
∫

Jk1 = f1 + 2f0 N1 + 2

2m J 2
+ 3
r
r

)

2
N1 + 3
r

∫

8πG3 3
dr −2mrN1 +
r f0 ⟨Trr ⟩
LP
(

)]

,

2N1 (r)
8πG3
rdr
− f0
⟨Trr ⟩ .
2
LP
R3
(

)

(B.33)
Substituting in (B.16) and integrating, we recover the expressions for f1 , N1 and k1 presented
in the main text (3.55)–(3.57), with
(

hn ≡ (4r

C

2

2
2
2
2
− R3 β +
)(4r2 + R32 β−
)bn + (β+
+ β−
)

2 )R2
(β 2 − β−
3
4r − −
2

)

2

dn .

(B.34)

Elements of the AdS C-metric

The AdS4 C-metric is a solution to Einstein’s equation with negative cosmological constant,
arising from a particular rescaling of the Plebanski-Demianski solution [28]:25
[

]

1
dy 2
dx2
2
ds = 2
H(y)dt
−
+
+ G(x)dφ2 ,
A (x − y)2
H(y) G(x)

(C.1)

H(y) = −λ + ky 2 − 2mAy 3 ,

(C.2)

2

with
G(x) = 1 + kx2 − 2mAx3 ,

and k = +1, 0, −1 which will determine the topology of the horizon of the black hole
solutions when they exist. The parameters A and m can be thought of as acceleration and
mass, respectively, while λ is related to the cosmological constant. Indeed, the bulk Ricci
25

Here we follow the conventions of [14]. To recover the form of the C-metric used in [12] one identifies
λ=

ℓ2
,
ℓ23

A=

1
,
ℓ

k = −κ ,

2mA = µ ,

y=

−ℓ
r

and further rescale t → t/ℓ. To connect to the conventions of [7], we make the same replacement except
restrict to κ = +1 and replace ℓ23 = −R32 , which amounts to a Wick rotation of ℓ3 .

– 38 –

JHEP06(2023)127

Going through the algebra and requiring the corrections to go to zero for vanishing stress
energy tensor, we eventually find

## PDF page 40

φ ∼ φ + ∆φ ,

∆φ =

4π
|G′ (xi )|

,

(C.3)

where xi is one of the zeros. Once the period of φ has been fixed in this way, say at x = x1 ,
then φ cannot be readjusted to eliminate the remaining conical singularities at x = x0 , x2 .
Thus, in general there will be a conical singularity along the axis x = xi with deficit angle
δ=

4π
G′ (xi )

− ∆φ ,

(C.4)

which can be interpreted as a cosmic string with tension τcs = δ/8π. Note that it is this
feature which leads one to interpret the C-metric as a single or pair of accelerating black
holes. For example, for a single black hole, a cosmic string attaches at one pole in the
background and the black hole, suspending it away from the center of the spacetime, thereby
inducing its acceleration (for a detailed analysis on the interpretation of the C-metric,
see [95]). This acceleration leads to an additional acceleration horizon, analogous to a
Rindler horizon, and an equilibrium thermodynamic description [14] (see also [45]).
We are interested in introducing a brane into the AdS4 spacetime. Generally there
will be a discontinuity in the extrinsic curvature Kij [h] across the brane which, via the
Israel junction conditions (equations of motion for the brane), is related to the stress-tensor
introduced by the brane. In the four-dimensional case at hand, where the brane action is
purely tensional, the junction conditions are
∆Kij − hij ∆K kk = 8πG4 τ hij ,
26

(C.5)

Explicitly, the cubic G(x) = −2mAx3 + kx2 + 1 = 0 can be solved by introducing x = z − k3 and express
2

3

2

[2k +27(4mA) ]
k
in depressed form, z 3 + pz + q = 0, with p = − 12(mA)
, such that the discriminant
2 and q = −
27(2mA)3
3

2

is ∆ ≡ −(4p3 + 27q 2 ) = − k +27(mA)
. When ∆ > 0, then G(x) will have three distinct real roots, while if
4(mA)4
∆ < 0 then G(x) will have one real root and two complex roots. In the flat space case [13], where k = −1,
√ .
then G(x) will have three distinct roots x0 < x2 < 0 < x1 provided 0 < mA < 3 1
3
27
2
′
To see this, introduce a coordinate x̃ = 4(x − xi )/G (xi ). Then expand the (x, φ) sector of the line
element (C.1) about a zero of G(x), where G−1 (x)dx2 +G(x)dφ2 ≈ [G′ (xi )(x−xi )]−1 dx2 +G′ (xi )(x−xi )dφ2 =
x̃2 (G′ (xi )/2)2 dφ2 + dx̃2 . Periodicity (C.3) follows from imposing regularity at x̃ = 0.

– 39 –

JHEP06(2023)127

√
tensor satisfies R̂AB = −(3/L24 )ĝAB where L4 ≡ (A λ + 1)−1 sets the scale for the bulk
cosmological constant. Maintaining a negative cosmological constant in the bulk requires
λ > −1, however, as summarized below, various ranges of λ describe different asymptotic
brane geometries.
The overall factor (x − y)−2 in (C.1) implies the point y = x is infinitely far away from
points y ̸= x (the point y = x corresponds to the asymptotic AdS4 geometry). A curvature
singularity is located at y = −∞, which is hidden behind one of the horizons. To maintain
a ‘mostly plus’ Lorentzian signature requires G(x) ≥ 0, restricting the range of x.
Each zero of H(y) corresponds to a Killing horizon associated with the time translation
Killing vector ∂t . Meanwhile, the zeros of G(x) corresponds to an axis for the rotation
symmetry ∂φ , i.e., for ξ a = ∂φa , then ξ 2 ∼ G(x), vanishing at a zero of G(x). For a range
of values of mA and k, there will be three distinct real zeros26 to G(x), {x0 , x1 , x2 }, with
each zero leading to a distinct conical singularity. One singularity can be removed via 27

## PDF page 41

Adding rotation. For completion, let us briefly review the rotating AdS4 C-metric,
following the conventions of [14].28 The line element is
ds2 =

1
H(y)
Σ(x, y) 2 Σ(x, y) 2 G(x)
(dt+ax2 dφ)2 −
dy +
dx +
(dφ−ay 2 dt)2 ,
2
2
A (x−y) Σ(x, y)
H(y)
G(x)
Σ(x, y)
(C.6)
[

]

with metric functions
H(y) = −λ + ky 2 − 2mAy 3 − a2 y 4 ,
G(x) = 1 + kx2 − 2mAx3 + a2 λx4 .

Σ(x, y) = 1 + a2 x2 y 2
(C.7)

As in the static case, this spacetime is obeys R̂AB = −3/L24 ĝAB with the same scale L4 .
When m ̸= 0, there is a curvature singularity when 1/y 2 Σ(x, y) = 0, i.e., when both
y → −∞ and x = 0, which may be recognized as the standard ring singularity familiar to
Kerr black holes.
The zeros xi of G(x) now correspond to fixed orbits of the rotational Killing vector
ξ = ∂φ − ax2i ∂t .

(C.8)

Indeed, the vector ∂φµ no longer has vanishing norm at x = xi , while ξ does. Avoiding
a conical defect at, say, x = x1 requires one identify points along the integral curves of
28

To
25, together
√
√ recover the form of the metric used in [12] one makes the identifications in Footnote
with λa → a/ℓ3 , while to recover the metric used in the main text (2.6), one identifies λa → −a/iR3 .

– 40 –

JHEP06(2023)127

−
+
where ∆Kij = Kij
− Kij
= 2Kij and Sij = −τ hij . Therefore, the tension can be seen as a
parameter which fixes the location of the brane B. In the case of the C-metric, a natural
choice for the location of B is the surface x = 0 since it is umbilic. To see this, note that the
√
unit normal to the brane at x = 0 is nix = Aϵ(x − y) G(x)∂xi , where ϵ = ±1 corresponds
to the orientation of the normal; here we take ϵ = +1 since x = 0 is a timelike hypersurface.
(x)
(x)
The non-vanishing components of Kij = ∇i nj obey Kij = −Ahij , with hij being the
induced metric along the x = 0 brane. Comparing to the Israel junction conditions we
identify the brane tension (2.9). Similarly, the y = 0 hypersurface is umbilic. Indeed, with
√
√
(y)
(y)
unit normal niy = Aϵ(x − y) H(y)∂yi , then Kij = −Aϵ −λhij , where hij is the induced
metric at y = 0.
To gain some intuition for the brane construction, it is helpful to consider the simplifying
case when mA = 0. One can then move to a coordinate frame showing the geometry is locally
AdS4 where the brane itself has a three-dimensional cosmological constant Λ3 = −λ [14].
Thus, the sign of λ denotes different constant curvature slicings of AdS4 . There are three
distinct cases: (1) λ = 0, a flat slicing. In this case one must choose k = ±1, where for
k = −1 the coordinate t is timelike everywhere; (2) −1 < λ < 0, leads to a three-dimensional
de Sitter slicing. One must select k = −1 to have dS3 in static patch coordinates and
cosmological horizons, and (3) λ > 0, an AdS3 slicing where the three different values of k
distinguish three distinct slicings of AdS3 : global coordinates (k = −1), the massive BTZ
black hole (k = +1), and the massless BTZ black hole (k = 0). The flat (λ = 0) solution
was studied in [13] while the AdS3 slicings were analyzed in [14].

## PDF page 42

this Killing vector with an appropriate period, amounting to coordinate transformation
t̃ = t + ax21 φ, where angular variable φ has the same period (C.3). To see this, expand
the relevant portion of the metric (C.6) near a zero of G(x). Without loss of generality,
consider the slice y = 0, where, up to the conformal factor
ds2 ≈ −λ(dt + ax2i dφ)2 +

dx2
+ G′ (xi )(x − xi )dφ2 .
G′ (xi )(x − xi )

(C.9)

D

Limits of qKdS

Here we provide details leading to the various limiting geometries of the qKdS black hole
described in the main text. Our analysis primarily follows [35]. First let us explore the
horizon structure of the naive metric (3.4), corresponding to the roots of the blackening
factor H(r). Introduce a function Q(r) ≡ r2 H(r) such that the roots of Q coincide with the
roots of H. Since Q is a quartic, it will have either four, two, or zero real roots. Requiring
Q to have four real roots, three of which are positive and correspond to the horizons
rc ≥ r+ ≥ r− , imposes restrictions on the physical parameters of the black hole solution,
namely, a and µ. As described in the main text, we can express the parameters a2 , R32 and
µℓ in terms of the three horizons r± and rc .30 The negative root of Q, denoted rn and
sometimes called the ‘negative horizon’, lies behind the singularity at r = 0.
29
Specifically, take the brane geometry in coordinates (t̃, ρ, φ) and then perform the shift φ = φ̃ + C t̃. In
the large ρ limit, one finds that the dt̃dφ̃ component will grow as ρ2 unless C ≡ −λax21 /(1 − λa2 x41 ). Note
this choice of constant C differs from the one in the main text because here we called t = t̃ − ax21 φ and then
redefined φ, whereas in the main text we defined t = t̃ − ax21 φ̃.
30
For example, to reexpress R32 , first subtract r+ H(r+ ) = 0 from rc H(rc ) = 0, and similarly subtract
r− H(r− ) = 0 from r+ H(r+ ) = 0. Subtracting the first of the resultant expressions from the other and
rearranging one recovers (3.20).

– 41 –

JHEP06(2023)127

Aside from the first term, the (x, φ) sector takes the same form as in the non-rotating case,
from which the periodicity of φ is (C.3) (see Footnote 27). Including rotation, however, this
would not be the correct periodicity for φ. The situation is remedied with the coordinate
transformation t̃ = t + ax2i φ, such that, at x = xi , then dt̃ = (dt + ax2i dφ). Similarly, at the
roots yi of H(y), the Killing vector ζ = ∂t + ayi2 ∂φ becomes null, defining horizons with
angular velocity Ω = ayi2 .
The brane is again placed at x = 0 since this surface remains umbilic. Indeed,
√
for spacelike unit normal nix = A(x − y) G(x)/Σ(x, y)∂xi , the extrinsic curvature again
(x)
satisfies Kij = −Ahij at x = 0. Similarly, the y = 0 hypersurface, with unit normal
√
√
(y)
niy = Aϵ(x − y) H(y)/Σ(x, y)∂yi , obeys Kij = (−Aϵ −λ)hij .
Due to the periodicity in φ, notice that along the orbit ξ the coordinate t is shifted:
via t = t̃ − ax21 φ and t̃ ∼ t̃, then t ∼ t − ax21 ∆φ. Consequently, this introduces a rotation
of frames in the asymptotic limit; namely, introducing radial coordinate ρ = −y −1 and
performing the coordinate transformation (t, y, φ) → (t̃, ρ, φ), the ht̃φ component of the
brane metric at x = 0 will grow as ρ2 and not as a constant [14]. To remove this undesired
asymptotic growth, one further shifts φ = φ̃ + C t̃ for a judiciously chosen constant29 to
remove the ρ2 growth in the coordinate frame (t̃, ρ, φ̃). To place the brane metric in more
canonically normalized coordinates, one further rescales coordinates t̃ and φ̃ and redefines
the radial coordinate ρ.

## PDF page 43

With these roots, we factorize Q as
Q(r) = −

1
(r − rc )(r − r+ )(r − r− )(r − rn ) .
R32

(D.1)

It proves convenient to introduce parameters d, δ, e and ϵ to parameterize the roots of Q,
rc = e + ϵ ,

r+ = e − ϵ ,

r− = d + δ ,

rn = d − δ .

(D.2)

0 ≤ ϵ < e,

e ≤ δ < 2e − ϵ ,

(D.3)

allowing us to write
Q=−

1
((r − e)2 − ϵ2 )((r + e)2 − δ 2 ) .
2
R3

(D.4)

Moreover, the parameters R32 , a2 and µℓ (3.20) become
R32 = 2e2 + ϵ2 + δ 2 ,
(e − δ)(e + δ)(e − ϵ)(e + ϵ)
,
2e2 + ϵ2 + δ 2
2e(δ − e)(δ + e)
µℓ =
.
2e2 + ϵ2 + δ 2
a2 = −

(D.5)

Notice from the root ordering (D.3) that a2 ≥ 0 and µ ≥ 0.
There are multiple cases when Q has degenerate roots, or degenerate horizons. These
include: (i) the extremal or ‘cold’ limit, where r+ = r− ; (ii) the (rotating) Nariai limit,
where rc = r+ , and (iii) the ‘ultracold’ limit, when rc = r+ = r− coincide. Each are
explored below.
Extremal limit. The extremal limit corresponds to when the inner and outer black hole
horizons coincide, r+ = r− . In this limit, the temperature of the outer black hole horizon
vanishes, T+ = 0, and is thus sometimes called the ‘cold’ black hole. Given the parameterization (D.2), r+ = r− imposes δ = 2e − ϵ. Consequently, the parameters (D.5) become
a2 =

1
(e − ϵ)2 (3e − ϵ)(e + ϵ) ,
2
R3

µℓ =

8e2 (e − ϵ)
,
R32

(D.6)

with R32 = 2(3e2 − 2eϵ + ϵ2 ), and
Q(r) = −

1
(r − (e + ϵ))(r − e + ϵ)2 (r + 3e − ϵ) .
R32

– 42 –

(D.7)

JHEP06(2023)127

Since rc and r± are all non-negative, we immediately learn e and d are real while δ and
ϵ must be non-negative real numbers. Expressing Q(r) in terms of these parameters, one
fixes d = −e to eliminate the r3 contribution. Additionally, the root ordering condition,
rc ≥ r+ ≥ r− and rn = −(r+ + r− + rc ) < 0 further imposes

## PDF page 44

It is interesting to consider the near horizon limit of the extremal black hole, where
r ≈ r+ = e − ϵ. The coordinates (t, r, φ) become singular in this limit and we therefore
perform the coordinate transformation
r = e − ϵ + λρ ,

t=

τ
,
λ

φ=ϕ−

aτ
,
(e − ϵ)2 λ

(D.8)

where λ is a dimensionless parameter which for the time being is non-zero. Then,
Q(ρ) = −

λ 2 ρ2
(λρ − 2ϵ)(λρ + 4e − 2ϵ) .
R32

(D.9)

(
ρ2 2
dρ2
2
2
dsex = − dτ + Γ 2 + (e − ϵ) dϕ −

ρ

Γ

2ρa
dτ
(e − ϵ)3

)2

,

(D.10)

with31

2
2
R32 r+
r+
R32 (e − ϵ)2
=
=
(D.11)
2 /R2 .
4ϵ(2e − ϵ)
(rc − r+ )(rc + 3r+ )
1 − 6r+
3
√
√
Introducing dimensionless coordinates (τ̂ , ρ̂) such that τ = Γτ̂ and ρ = Γρ̂, we find

Γ≡

(

ds2ex = Γ

dρ̂2
−ρ̂ dτ̂ + 2
ρ̂
2

)

2

2
+ r+
(dϕ + k ρ̂dτ̂ )2 ,

(D.12)

3 = −2aR2 /r (R2 − 6r 2 ).
where k ≡ −2aΓ/r+
+
3 +
3
For completeness, the leading order contribution to the holographic CFT stress-energy
tensor in the extremal background is

1
1 µℓ
⟨T τ̂τ̂ ⟩0 = ⟨T ρ̂ρ̂ ⟩0 = − ⟨T ϕτ̂ ⟩0 =
3 ,
2
16πG3 r+

(D.13)

3µℓaR32
ρ̂
2 ) r4 ,
8πG3 (R32 − 6r+
+

⟨T ϕϕ ⟩0 =

which has vanishing trace to this order.
Nariai limit. The Nariai black hole is when the outer black hole horizon and cosmological
horizon coincide, rc = r+ = rN . In this limit, naively, the temperature of the cosmological
and black hole horizons vanish, however, we will see the Nariai black hole has a non-zero
temperature. From the parameterization (D.2), rc = r+ is equivalent to ϵ = 0, such that
a2 =

e2 (δ 2 − e2 )
,
R32

2eδ 2
,
R32

(D.14)

1
(r − rN )2 ((r + rN )2 − δ 2 ) ,
R32

(D.15)

µℓ =

with R32 = 2e2 + δ 2 , and
Q=−
31

2
Here we use that in the extremal limit R32 = rc2 + 3r+
+ 2r+ rc , such that rc =

– 43 –

√

2
R32 − 2r+
− r+ .

JHEP06(2023)127

Substituting this, performing the coordinate transformation and then taking the limit
λ → 0, the naive brane geometry (3.4) becomes

## PDF page 45

which vanishes in the limit r = rN . Therefore, the (t, r, φ) coordinate system is insufficient
to describe the Nariai geometry.
To this end, consider the following coordinate transformation
r = e + ϵρ ,

t=

τ
,
ϵ

φ=ϕ−

a
τ.
e2 ϵ

(D.16)

The function Q becomes
Q(ρ) =

ϵ2
(1 − ρ2 )((ϵρ + 2e)2 − δ 2 ) .
R32

(D.17)

(

ds2N = Γ

dρ2
−(1 − ρ )dτ̂ +
(1 − ρ2 )
2

where τ = Γτ̂ and
Γ≡

)

2

+ e2 (dϕ + kρdτ̂ )2 ,

(D.18)

2aΓ
3 ,
rN

(D.19)

2
R32 e2
R32 rN
=
2 − R2 ,
4e2 − δ 2
6rN
3

k≡−

√

2.
where we used δ = R32 − 2rN
The temperature TN of the Nariai black hole can be found by Wick rotating the near
horizon metric into an appropriate Euclidean section. To see this, rescale coordinates
√
√
ρ̂ = ρ Γ and τ = τ̂ Γ, such that the Nariai metric (D.18) becomes
2
ds2N = −f (ρ̂)dτ 2 + f −1 (ρ̂)dρ̂2 + rN
(dφ + (k/Γ)ρ̂dτ )2 ,

(D.20)

2 and f (ρ̂) = 1 − ρ̂2 /Γ. Next, Wick rotate τ → iτ and a → ia , such
with k/Γ = −2a/rN
E
E
that the Euclideanized geometry is

(
2
ds2N = f (ρ̂)dτE2 + f −1 (ρ̂)dρ̂2 + rN

2aE ρ̂
dφ + 2 dτE
rN

)

.

(D.21)

√
We now zoom in to the near horizon region where ρ̂i = Γ and express the metric in flat
polar coordinates and impose regularity to remove the conical singularity. Thus, introduce
the radial coordinate
ρ′2 =

4(ρ̂ − ρ̂i )
f ′ (ρ̂i )

⇒

dρ̂2 = (f ′ (ρ̂i )ρ′ /2)2 dρ′2 .

(D.22)

Moreover, to eliminate the dτE dφ cross term in the line element, introduce coordinates
1
1
α ′
τE = 2
(γτE′ − rN αφ′ ) ,
φ= 2
τ + γφ′ ,
(D.23)
2
2
(γ + α )
(γ + α ) rN E
√
√
2 . Then, expand the metric (D.21) about ρ̂ =
with γ = Γ/rN and α = −2aE Γ/rN
Γ,
(

ds2N ≈ ρ′2 d(β −1 τE′ )2 + dρ′2 +

– 44 –

2
rN
dφ′2 ,
Γ

)

(D.24)

JHEP06(2023)127

Taking the ϵ → 0 limit, the brane metric (3.4) takes the form

## PDF page 46

where we used f (ρ̂) ≈ f ′ (ρ̂i )(ρ̂ − ρ̂i ) and
β=

Γ2
2
2
2 2
3 R2 (6rN − R3 + 4aE R3 ) .
rN
3

(D.25)

The (τE′ , ρ′ )-sector is that of a cone where we remove the singularity at ρ′ = 0 by demanding
τE′ have period ∆τE′ = 2πβ. Additionally, we impose φ′ to have period ∆φ′ = 0, such that
the geometry (D.24) represents flat polar coordinates. We now solve for the periodicity of
∆τE in the Euclidean geometry (D.21) via32

leading to
∆τE =

∆φ′ = 0 = γ∆φ −

α
∆τE ,
rN

√
2πβγ
= 2π Γ .
2
2
(γ + α )

(D.26)

(D.27)

√
Hence, the temperature of the Nariai black hole is TN = (2π Γ)−1 .
Lastly, the holographic CFT stress-energy tensor in the rotating Nariai geometry is
1
1 µℓ
⟨T τ̂τ̂ ⟩0 = ⟨T ρρ ⟩0 = − ⟨T ϕτ̂ ⟩0 =
3 ,
2
16πG3 rN
⟨T ϕϕ ⟩0 =

(D.28)

3µℓaR32
ρ
2 − R2 ) r 4 .
8πG3 (6rN
3
N

When a = 0, we recover the stress-tensor for the static quantum Nariai black hole [7].
Ultracold limit. The ultracold limit occurs when all three horizons coincide, rc = r+ =
r− ≡ ruc . Thus, this is a combination of the Nariai and extremal limits, i.e., simultaneously
sending δ → 2e − ϵ and ϵ → 0. Here we will arrive at the ultracold limit directly from the
Nariai limit, where we make the following change of variables:
√

ρ=

2e − δ
X,
R3

√

τ=

R3 R3 e
T,
2e − δ 4

(D.29)

and subsequently take the limit δ → 2e such that the Nariai geometry (D.18) becomes that
of the ultracold black hole,
ds2uc =

R3 ruc
2aX
2
(−dT 2 + dX 2 ) + ruc
dϕ − 3 dT
4
ruc
(

)2

.

(D.30)

The physical parameters meanwhile are a2 = 3e4 /R32 and µℓ = 8e3 /R32 .
Lukewarm black hole. Lastly, as with all Kerr-de Sitter black holes, the qKdS has a
lukewarm limit, where the surface gravities of the cosmological and outer black hole horizons
coincide κc = κ+ , apart from the surface gravity of the Nariai black hole. For completeness
we carry out the analysis of this limiting geometry with respect to the surface gravities of
32

Where it is useful to know the inverse coordinate transformation τE′ = γτE + rN αφ and φ′ = γφ − rβN τE .

– 45 –

JHEP06(2023)127

∆τE′ = 2πβ = γ∆τE + rN α∆φ ,

## PDF page 47

the naive black hole spacetime, leaving the analysis of the lukewarm limit of the regular
black hole for the main text.
To this end, the surface gravities with respect to the naive metric (3.4) are simply
κi = 12 |H ′ (ri )|, following the definition ζ b ∇b ζ c = κζ c , where there is a surface gravity
associated with each root of the blackening factor H(r). The temperature of each horizon
is then33
κi
|H ′ (ri )|
Ti =
=
.
(D.31)
2π
4π

Ti =

|Q′ (ri )|
1
=
|[(ri − e)((ri + e)2 − δ 2 ) + (ri + e)((ri − e)2 − ϵ2 )]| .
4πri2
2πri2 R32

(D.32)

Then, the temperature of the outer horizon r+ = e − ϵ is
T+ =

1 2ϵ((2e − ϵ)2 − δ 2 )
.
(e − ϵ)2
4πR32

(D.33)

Via root ordering, this temperature is positive, and vanishes in the extremal limit. Meanwhile,
the temperature of the cosmological horizon rc = e + ϵ is
Tc =

1 2ϵ((2e + ϵ)2 − δ 2 )
.
(e + ϵ)2
4πR32

(D.34)

Taking their difference,
Tc − T+ = 0

eϵ2 (ϵ2 − 2e2 + δ 2 ) = 0 .

⇐⇒

(D.35)

Here e = 0 is forbidden via the root ordering while ϵ = 0 corresponds to the Nariai limit.
ϵ
Hence, the lukewarm limit corresponds to when δ 2 = 2e2 −ϵ2 , with temperature Tluke = 2πR
2.
3
Moreover, since H(r) is non-zero in this limit, the lukewarm geometry is safely covered by
the coordinates (t, r, φ) with blackening factor
H(r) = −

1

((r − e)
R32 r2

2

− ϵ2 )((r + e)2 − 2e2 + ϵ2 ) ,

(D.36)

and where (D.5) become R32 a2 = (e2 − ϵ2 )2 and R32 µℓ = 4e(e2 − ϵ2 ), with R32 = 4e2 .
Open Access. This article is distributed under the terms of the Creative Commons
Attribution License (CC-BY 4.0), which permits any use, distribution and reproduction in
any medium, provided the original author(s) and source are credited. SCOAP 3 supports
the goals of the International Year of Basic Sciences for Sustainable Development.
33

One way to derive this expression of the temperature is to move to the Euclidean section of the rotating
geometry (3.4), via the double Wick rotation t → iτE and a → iaE and then impose regularity to remove
the conical singularity along the Euclidean time direction.

– 46 –

JHEP06(2023)127

Then, using H ′ (ri ) = ri−2 Q′ (ri ), since H(ri ) = 0, we have

## PDF page 48

References
[1] M. Banados, C. Teitelboim and J. Zanelli, The Black hole in three-dimensional space-time,
Phys. Rev. Lett. 69 (1992) 1849 [hep-th/9204099] [INSPIRE].
[2] M. Banados, M. Henneaux, C. Teitelboim and J. Zanelli, Geometry of the (2 + 1) black hole,
Phys. Rev. D 48 (1993) 1506 [Erratum ibid. 88 (2013) 069902] [gr-qc/9302012] [INSPIRE].
[3] A. Strominger, Black hole entropy from near horizon microstates, JHEP 02 (1998) 009
[hep-th/9712251] [INSPIRE].

[5] R. Dijkgraaf, J.M. Maldacena, G.W. Moore and E.P. Verlinde, A Black hole Farey tail,
hep-th/0005003 [INSPIRE].
[6] S. Deser and R. Jackiw, Three-Dimensional Cosmological Gravity: Dynamics of Constant
Curvature, Annals Phys. 153 (1984) 405 [INSPIRE].
[7] R. Emparan et al., Black holes in dS3 , JHEP 11 (2022) 073 [arXiv:2207.03302] [INSPIRE].
[8] D. Klemm and L. Vanzo, De Sitter gravity and Liouville theory, JHEP 04 (2002) 030
[hep-th/0203268] [INSPIRE].
[9] S. de Haro, K. Skenderis and S.N. Solodukhin, Gravity in warped compactifications and the
holographic stress tensor, Class. Quant. Grav. 18 (2001) 3171 [hep-th/0011230] [INSPIRE].
[10] L. Randall and R. Sundrum, An Alternative to compactification, Phys. Rev. Lett. 83 (1999)
4690 [hep-th/9906064] [INSPIRE].
[11] R. Emparan, A. Fabbri and N. Kaloper, Quantum black holes as holograms in AdS brane
worlds, JHEP 08 (2002) 043 [hep-th/0206155] [INSPIRE].
[12] R. Emparan, A.M. Frassino and B. Way, Quantum BTZ black hole, JHEP 11 (2020) 137
[arXiv:2007.15999] [INSPIRE].
[13] R. Emparan, G.T. Horowitz and R.C. Myers, Exact description of black holes on branes,
JHEP 01 (2000) 007 [hep-th/9911043] [INSPIRE].
[14] R. Emparan, G.T. Horowitz and R.C. Myers, Exact description of black holes on branes. II:
Comparison with BTZ black holes and black strings, JHEP 01 (2000) 021 [hep-th/9912135]
[INSPIRE].
[15] R.M. Wald, Black hole entropy is the Noether charge, Phys. Rev. D 48 (1993) R3427
[gr-qc/9307038] [INSPIRE].
[16] S.S. Gubser, I.R. Klebanov and A.M. Polyakov, Gauge theory correlators from noncritical
string theory, Phys. Lett. B 428 (1998) 105 [hep-th/9802109] [INSPIRE].
[17] E. Witten, Anti-de Sitter space and holography, Adv. Theor. Math. Phys. 2 (1998) 253
[hep-th/9802150] [INSPIRE].
[18] S. de Haro, S.N. Solodukhin and K. Skenderis, Holographic reconstruction of space-time and
renormalization in the AdS/CFT correspondence, Commun. Math. Phys. 217 (2001) 595
[hep-th/0002230] [INSPIRE].
[19] K. Skenderis, Lecture notes on holographic renormalization, Class. Quant. Grav. 19 (2002)
5849 [hep-th/0209067] [INSPIRE].

– 47 –

JHEP06(2023)127

[4] D. Birmingham, I. Sachs and S. Sen, Entropy of three-dimensional black holes in string theory,
Phys. Lett. B 424 (1998) 275 [hep-th/9801019] [INSPIRE].

## PDF page 49

[20] P. Kraus, F. Larsen and R. Siebelink, The gravitational action in asymptotically AdS and flat
space-times, Nucl. Phys. B 563 (1999) 259 [hep-th/9906127] [INSPIRE].
[21] R. Emparan, C.V. Johnson and R.C. Myers, Surface terms as counterterms in the AdS/CFT
correspondence, Phys. Rev. D 60 (1999) 104001 [hep-th/9903238] [INSPIRE].
[22] I. Papadimitriou and K. Skenderis, AdS/CFT correspondence and geometry, IRMA Lect. Math.
Theor. Phys. 8 (2005) 73 [hep-th/0404176] [INSPIRE].
[23] H.Z. Chen et al., Quantum Extremal Islands Made Easy, Part I: Entanglement on the Brane,
JHEP 10 (2020) 166 [arXiv:2006.04851] [INSPIRE].

[25] A. Karch and L. Randall, Locally localized gravity, JHEP 05 (2001) 008 [hep-th/0011156]
[INSPIRE].
[26] J. Garriga and T. Tanaka, Gravity in the brane world, Phys. Rev. Lett. 84 (2000) 2778
[hep-th/9911055] [INSPIRE].
[27] C. Charmousis, R. Gregory and V.A. Rubakov, Wave function of the radion in a brane world,
Phys. Rev. D 62 (2000) 067505 [hep-th/9912160] [INSPIRE].
[28] J.F. Plebanski and M. Demianski, Rotating, charged, and uniformly accelerating mass in
general relativity, Annals Phys. 98 (1976) 98 [INSPIRE].
[29] D. Anninos and T. Hartman, Holography at an Extremal De Sitter Horizon, JHEP 03 (2010)
096 [arXiv:0910.4587] [INSPIRE].
[30] S. Cremonini, J.T. Liu and P. Szepietowski, Higher Derivative Corrections to R-charged Black
Holes: Boundary Counterterms and the Mass-Charge Relation, JHEP 03 (2010) 042
[arXiv:0910.5159] [INSPIRE].
[31] H. Kudoh and Y. Kurita, Thermodynamics of four-dimensional black objects in the warped
compactification, Phys. Rev. D 70 (2004) 084029 [gr-qc/0406107] [INSPIRE].
[32] V. Balasubramanian, J. de Boer and D. Minic, Mass, entropy and holography in asymptotically
de Sitter spaces, Phys. Rev. D 65 (2002) 123508 [hep-th/0110108] [INSPIRE].
[33] B.P. Dolan, The definition of mass in asymptotically de Sitter space-times, Class. Quant. Grav.
36 (2019) 077001 [arXiv:1808.09081] [INSPIRE].
[34] G.W. Gibbons and S.W. Hawking, Cosmological Event Horizons, Thermodynamics, and
Particle Creation, Phys. Rev. D 15 (1977) 2738 [INSPIRE].
[35] I.S. Booth and R.B. Mann, Cosmological pair production of charged and rotating black holes,
Nucl. Phys. B 539 (1999) 267 [gr-qc/9806056] [INSPIRE].
[36] S. Bhattacharya, Kerr-de Sitter spacetime, Penrose process and the generalized area theorem,
Phys. Rev. D 97 (2018) 084049 [arXiv:1710.00997] [INSPIRE].
[37] J.M. Bardeen and G.T. Horowitz, The Extreme Kerr throat geometry: A Vacuum analog of
AdS2 × S 2 , Phys. Rev. D 60 (1999) 104030 [hep-th/9905099] [INSPIRE].
[38] T. Hartman, K. Murata, T. Nishioka and A. Strominger, CFT Duals for Extreme Black Holes,
JHEP 04 (2009) 019 [arXiv:0811.4393] [INSPIRE].
[39] H. Nariai, On a New Cosmological Solution of Einstein’s Field Equations of Gravitation, Gen.
Rel. Grav. 31 (1999) 963.

– 48 –

JHEP06(2023)127

[24] P. Bueno, R. Emparan and Q. Llorens, Higher-curvature gravities from braneworlds and the
holographic c-theorem, Phys. Rev. D 106 (2022) 044012 [arXiv:2204.13421] [INSPIRE].

## PDF page 50

[40] P.H. Ginsparg and M.J. Perry, Semiclassical Perdurance of de Sitter Space, Nucl. Phys. B 222
(1983) 245 [INSPIRE].
[41] V. Cardoso, O.J.C. Dias and J.P.S. Lemos, Nariai, Bertotti-Robinson and anti-Nariai
solutions in higher dimensions, Phys. Rev. D 70 (2004) 024002 [hep-th/0401192] [INSPIRE].
[42] Y. Nutku, Exact solutions of topologically massive gravity with a cosmological constant, Class.
Quant. Grav. 10 (1993) 2657 [INSPIRE].
[43] D. Anninos, Sailing from Warped AdS3 to Warped dS3 in Topologically Massive Gravity, JHEP
02 (2010) 046 [arXiv:0906.1819] [INSPIRE].

[45] M. Appels, R. Gregory and D. Kubiznak, Thermodynamics of Accelerating Black Holes, Phys.
Rev. Lett. 117 (2016) 131303 [arXiv:1604.08812] [INSPIRE].
[46] B. Banihashemi and T. Jacobson, Thermodynamic ensembles with cosmological horizons,
JHEP 07 (2022) 042 [arXiv:2204.05324] [INSPIRE].
[47] B. Banihashemi, T. Jacobson, A. Svesko and M. Visser, The minus sign in the first law of de
Sitter horizons, JHEP 01 (2023) 054 [arXiv:2208.11706] [INSPIRE].
[48] A. Svesko, E. Verheijden, E.P. Verlinde and M.R. Visser, Quasi-local energy and
microcanonical entropy in two-dimensional nearly de Sitter gravity, JHEP 08 (2022) 075
[arXiv:2203.00700] [INSPIRE].
[49] D. Anninos and E. Harris, Interpolating geometries and the stretched dS2 horizon, JHEP 11
(2022) 166 [arXiv:2209.06144] [INSPIRE].
[50] A.M. Frassino, J.F. Pedraza, A. Svesko and M.R. Visser, Higher-Dimensional Origin of
Extended Black Hole Thermodynamics, Phys. Rev. Lett. 130 (2023) 161501
[arXiv:2212.14055] [INSPIRE].
[51] D. Kastor, S. Ray and J. Traschen, Enthalpy and the Mechanics of AdS Black Holes, Class.
Quant. Grav. 26 (2009) 195011 [arXiv:0904.2765] [INSPIRE].
[52] B.P. Dolan, The cosmological constant and the black hole equation of state, Class. Quant. Grav.
28 (2011) 125020 [arXiv:1008.5023] [INSPIRE].
[53] J.F. Pedraza, A. Svesko, W. Sybesma and M.R. Visser, Semi-classical thermodynamics of
quantum extremal surfaces in Jackiw-Teitelboim gravity, JHEP 12 (2021) 134
[arXiv:2107.10358] [INSPIRE].
[54] E.K. Morvan, J.P. van der Schaar and M.R. Visser, On the Euclidean action of de Sitter black
holes and constrained instantons, SciPost Phys. 14 (2023) 022 [arXiv:2203.06155] [INSPIRE].
[55] P. Draper and S. Farkas, de Sitter black holes as constrained states in the Euclidean path
integral, Phys. Rev. D 105 (2022) 126022 [arXiv:2203.02426] [INSPIRE].
[56] E.K. Morvan, J.P. van der Schaar and M.R. Visser, Action, entropy and pair creation rate of
charged black holes in de Sitter space, arXiv:2212.12713 [INSPIRE].
[57] A. Chamblin, R. Emparan, C.V. Johnson and R.C. Myers, Charged AdS black holes and
catastrophic holography, Phys. Rev. D 60 (1999) 064018 [hep-th/9902170] [INSPIRE].
[58] A. Climent, R. Emparan and R. Hennigar, in preparation.

– 49 –

JHEP06(2023)127

[44] D. Anninos, S. de Buyl and S. Detournay, Holography For a De Sitter-Esque Geometry, JHEP
05 (2011) 003 [arXiv:1102.3178] [INSPIRE].

## PDF page 51

[59] J.D. Bekenstein, Exact solutions of Einstein conformal scalar equations, Annals Phys. 82
(1974) 535 [INSPIRE].
[60] J.D. Bekenstein, Black Holes with Scalar Charge, Annals Phys. 91 (1975) 75 [INSPIRE].
[61] C. Charmousis, T. Kolyvaris and E. Papantonopoulos, Charged C-metric with conformally
coupled scalar field, Class. Quant. Grav. 26 (2009) 175012 [arXiv:0906.5568] [INSPIRE].
[62] A. Anabalon and H. Maeda, New Charged Black Holes with Conformal Scalar Hair, Phys. Rev.
D 81 (2010) 041501 [arXiv:0907.0219] [INSPIRE].

[64] N. Tanahashi and T. Tanaka, Black holes in braneworld models, Prog. Theor. Phys. Suppl. 189
(2011) 227 [arXiv:1105.2997] [INSPIRE].
[65] J. Podolsky and M. Ortaggio, Robinson-Trautman spacetimes in higher dimensions, Class.
Quant. Grav. 23 (2006) 5785 [gr-qc/0605136] [INSPIRE].
[66] R. Emparan et al., Holographic duals of evaporating black holes, JHEP 05 (2023) 182
[arXiv:2301.02587] [INSPIRE].
[67] J. Maldacena, G.J. Turiaci and Z. Yang, Two dimensional Nearly de Sitter gravity, JHEP 01
(2021) 139 [arXiv:1904.01911] [INSPIRE].
[68] A. Castro, F. Mariani and C. Toldo, Near-Extremal Limits of de Sitter Black Holes,
arXiv:2212.14356 [INSPIRE].
[69] A. Karch and L. Randall, Open and closed string interpretation of SUSY CFT’s on branes
with boundaries, JHEP 06 (2001) 063 [hep-th/0105132] [INSPIRE].
[70] T. Takayanagi, Holographic Dual of BCFT, Phys. Rev. Lett. 107 (2011) 101602
[arXiv:1105.5165] [INSPIRE].
[71] M. Fujita, T. Takayanagi and E. Tonni, Aspects of AdS/BCFT, JHEP 11 (2011) 043
[arXiv:1108.5152] [INSPIRE].
[72] M. Guica, T. Hartman, W. Song and A. Strominger, The Kerr/CFT Correspondence, Phys.
Rev. D 80 (2009) 124008 [arXiv:0809.4266] [INSPIRE].
[73] H. Lu, J. Mei and C.N. Pope, Kerr/CFT Correspondence in Diverse Dimensions, JHEP 04
(2009) 054 [arXiv:0811.2225] [INSPIRE].
[74] R. Emparan, A.M. Frassino, M. Sasieta and M. Tomašević, Holographic complexity of quantum
black holes, JHEP 02 (2022) 204 [arXiv:2112.04860] [INSPIRE].
[75] A. Reynolds and S.F. Ross, Complexity in de Sitter Space, Class. Quant. Grav. 34 (2017)
175013 [arXiv:1706.03788] [INSPIRE].
[76] S. Chapman, D.A. Galante and E.D. Kramer, Holographic complexity and de Sitter space,
JHEP 02 (2022) 198 [arXiv:2110.05522] [INSPIRE].
[77] E. Jørstad, R.C. Myers and S.-M. Ruan, Holographic complexity in dSd+1 , JHEP 05 (2022)
119 [arXiv:2202.10684] [INSPIRE].
[78] J.F. Pedraza, A. Russo, A. Svesko and Z. Weller-Davies, Lorentzian Threads as Gatelines and
Holographic Complexity, Phys. Rev. Lett. 127 (2021) 271602 [arXiv:2105.12735] [INSPIRE].

– 50 –

JHEP06(2023)127

[63] M. Anber and L. Sorbo, New exact solutions on the Randall-Sundrum 2-brane: lumps of dark
radiation and accelerated black holes, JHEP 07 (2008) 098 [arXiv:0803.2242] [INSPIRE].

## PDF page 52

[79] J.F. Pedraza, A. Russo, A. Svesko and Z. Weller-Davies, Sewing spacetime with Lorentzian
threads: complexity and the emergence of time in quantum gravity, JHEP 02 (2022) 093
[arXiv:2106.12585] [INSPIRE].
[80] J.F. Pedraza, A. Russo, A. Svesko and Z. Weller-Davies, Computing spacetime, Int. J. Mod.
Phys. D 31 (2022) 2242010 [arXiv:2205.05705] [INSPIRE].
[81] A. Al Balushi, R.A. Hennigar, H.K. Kunduri and R.B. Mann, Holographic Complexity and
Thermodynamic Volume, Phys. Rev. Lett. 126 (2021) 101601 [arXiv:2008.09138] [INSPIRE].
[82] H.Z. Chen et al., Quantum Extremal Islands Made Easy, Part II: Black Holes on the Brane,
JHEP 12 (2020) 025 [arXiv:2010.00018] [INSPIRE].

[84] S.E. Aguilar-Gutierrez, A.K. Patra, J. Pedraza and M. Sasieta, in preparation.
[85] R. Bousso, A. Maloney and A. Strominger, Conformal vacua and entropy in de Sitter space,
Phys. Rev. D 65 (2002) 104039 [hep-th/0112218] [INSPIRE].
[86] M.-I. Park, Statistical entropy of three-dimensional Kerr-de Sitter space, Phys. Lett. B 440
(1998) 275 [hep-th/9806119] [INSPIRE].
[87] A.R. Steif, The Quantum stress tensor in the three-dimensional black hole, Phys. Rev. D 49
(1994) 585 [gr-qc/9308032] [INSPIRE].
[88] M. Casals, A. Fabbri, C. Martínez and J. Zanelli, Quantum dress for a naked singularity, Phys.
Lett. B 760 (2016) 244 [arXiv:1605.06078] [INSPIRE].
[89] M. Casals, A. Fabbri, C. Martínez and J. Zanelli, Quantum-corrected rotating black holes and
naked singularities in (2 + 1) dimensions, Phys. Rev. D 99 (2019) 104023 [arXiv:1902.01583]
[INSPIRE].
[90] S.J. Avis, C.J. Isham and D. Storey, Quantum Field Theory in anti-De Sitter Space-Time,
Phys. Rev. D 18 (1978) 3565 [INSPIRE].
[91] G. Lifschytz and M. Ortiz, Scalar field quantization on the (2 + 1)-dimensional black hole
background, Phys. Rev. D 49 (1994) 1929 [gr-qc/9310008] [INSPIRE].
[92] S.M. Christensen, Vacuum Expectation Value of the Stress Tensor in an Arbitrary Curved
Background: The Covariant Point Separation Method, Phys. Rev. D 14 (1976) 2490 [INSPIRE].
[93] T. Souradeep and V. Sahni, Quantum effects near a point mass in (2 + 1)-Dimensional gravity,
Phys. Rev. D 46 (1992) 1616 [hep-ph/9208219] [INSPIRE].
[94] R. Herman and W.A. Hiscock, Renormalization of the charged scalar field in curved space,
Phys. Rev. D 53 (1996) 3285 [gr-qc/9509015] [INSPIRE].
[95] J.B. Griffiths, P. Krtous and J. Podolsky, Interpreting the C-metric, Class. Quant. Grav. 23
(2006) 6745 [gr-qc/0609056] [INSPIRE].

– 51 –

JHEP06(2023)127

[83] A. Almheiri, R. Mahajan and J.E. Santos, Entanglement islands in higher dimensions, SciPost
Phys. 9 (2020) 001 [arXiv:1911.09666] [INSPIRE].
