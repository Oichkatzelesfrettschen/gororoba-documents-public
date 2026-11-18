Source: see manifest row of the PDF
PDF sha256: baefbf9f2cc608978322b873a8d1fc0df3f1501ba69e546ca1f1876b0c9ddd41
License: CC-BY-4.0
Language: eng
Fidelity: machine-gated

# Transcription of kapec_2023_photon_rings_around_warped_black_holes.pdf

Transcription of `kapec_2023_photon_rings_around_warped_black_holes.pdf` in this directory, 31 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-31 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Classical and Quantum Gravity

You may also like

PAPER • OPEN ACCESS

Photon rings around warped black holes

- Analytical description of quasi-normal
mode in resonant plasmonic nano cavities
Fan Yang, Haitao Liu, Hongwei Jia et al.

To cite this article: Daniel Kapec et al 2023 Class. Quantum Grav. 40 095006

- Quasinormal mode theory and modelling
of electron energy loss spectroscopy for
plasmonic nanostructures
Rong-Chun Ge and Stephen Hughes

View the article online for updates and enhancements.

- The ringing of quantum corrected
Schwarzschild black hole with GUP
Yujia Xing, Yi Yang, Dong Liu et al.

This content was downloaded from IP address 71.84.237.76 on 29/07/2023 at 07:09

## PDF page 2

Classical and Quantum Gravity
Class. Quantum Grav. 40 (2023) 095006 (30pp)

https://doi.org/10.1088/1361-6382/acc164

Photon rings around warped black holes
Daniel Kapec1,2, Alexandru Lupsasca3,∗
and Andrew Strominger2
1

Center of Mathematical Sciences and Applications, Harvard University, Cambridge,
MA 02138, United States of America
2
Center for the Fundamental Laws of Nature, Harvard University, Cambridge, MA
02138, United States of America
3
Department of Physics and Astronomy, Vanderbilt University, Nashville, TN 37212,
United States of America
E-mail: alexandru.v.lupsasca@vanderbilt.edu
Received 4 November 2022; revised 18 January 2023
Accepted for publication 3 March 2023
Published 3 April 2023
Abstract

The black hole photon ring is a prime target for upcoming space-based VLBI
missions seeking to image the fine structure of astrophysical black holes. The
classical Lyapunov exponents of the corresponding nearly bound null geodesics
control the quasinormal ringing of a perturbed black hole as it settles back down
to equilibrium, and they admit a holographic interpretation in terms of quantum
Ruelle resonances of the microstate dual to the Kerr black hole. Recent work
has identified a number of emergent symmetries related to the intricate selfsimilar structure of the photon ring. Here, we explore this web of interrelated
phenomena in an exactly soluble example that arises as an approximation to
the near-extremal Kerr black hole. The self-dual warped AdS3 geometry has
a photon ring as well as SL(2, R) isometries and an exactly calculable quasinormal mode (QNM) spectrum. We show explicitly that the geometric optics
approximation reproduces the eikonal limit of the exact scalar QNM spectrum,
as well as the approximate ‘near-ring’ wavefunctions. The SL(2, R) isometries
are directly related to the emergent conformal symmetry of the photon ring in
black hole images but are distinct from a recently discussed conformal symmetry of the eikonal QNM spectrum. The equivalence of the classical QNM
spectrum—and thus the photon ring—to the quantum Ruelle resonances in
the context of a spacetime with a putative holographic dual suggests that the
photon ring of a warped black hole is indeed part of the black hole hologram.
∗

Author to whom any correspondence should be addressed.

Original Content from this work may be used under the terms of the Creative Commons Attribution
4.0 licence. Any further distribution of this work must maintain attribution to the author(s) and the
title of the work, journal citation and DOI.
1361-6382/23/095006+30$33.00 © 2023 The Author(s). Published by IOP Publishing Ltd Printed in the UK

1

## PDF page 3

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

Keywords: black hole, photon ring, holography
(Some figures may appear in colour only in the online journal)
1. Introduction
The photon ring around a black hole controls a surprising number of observational signatures relevant to both current and future gravitational experiments. Its intricate, nested subring structure associated to nearly bound photons predicts distinct interferometric signatures
in black hole images [1], and may become visible with near-term space-based missions. The
ring also controls quasinormal ringdowns predicted for LIGO [2]: the last tones emitted as a
perturbed black hole settles back down to equilibrium consist of nearly trapped gravitational
waves slowly leaking off of the photon ring. These two phenomena are closely related in the
geometric optics approximation, in which high-frequency solutions of the wave equation are
constructed from null geodesic congruences (see, e.g. [3]).
Given that the photon ring controls so many distinctive features of classical black hole physics, it is natural to wonder if it might similarly constrain quantum aspects of black holes. Semiclassical analysis suggests that black holes behave much like isolated quantum-mechanical
systems with eSBH approximately thermal microstates and extremely chaotic dynamics. Known
examples of the holographic principle relate the classical quasinormal ringing of the black
hole to the damped oscillations of a perturbed thermal quantum state, also known as Ruelle
resonances [4]. The photon ring therefore controls, via geometric optics, the high-frequency
sector of the Ruelle spectrum for asymptotically flat black holes. The quantum-mechanical
description of black holes is intimately tied to the emergence of spacetime, and one might
think of the photon ring as an emergent geometrization of the high-frequency Ruelle spectrum. In other words, one can ‘hear’ the shape of the photon ring in the spectrum of quantum
Ruelle resonances.
Black hole spectroscopy is quickly becoming an experimental discipline, but no proposed
holographic dual to the Kerr black hole has managed to explain its spectrum of Ruelle resonances from quantum mechanics. This remains an open challenge for theorists. The eikonal
limit of the Kerr quasinormal mode (QNM) spectrum is [5, 6]
ℓ≫1

ωℓmn ≈

(

)
(
)
1
1
Ω(µ) − i n +
γL (µ) ,
ℓ+
2
2

(1.1)

where ℓ is an integer related to the total angular momentum, −ℓ ⩽ m ⩽ ℓ is the azimuthal
angular momentum, and µ = m/ℓ ∈ (−1, 1) is kept fixed as both ℓ and |m| are taken large.
The quantity µ ≈ sin θmax (r̃) determines both the orbital inclination θmax and the photon shell
radius r̃ of the bound orbit, and Ω(µ(r̃)) is the angular velocity of the orbit at radius r̃. The
imaginary parts of the QNM frequencies are controlled by γL (µ(r̃)) = γ(r̃)/τ (r̃), which is the
ratio of the bound orbit’s Lyapunov exponent γ to the orbital period τ of its libration in θ.
In figure 1, we plot the eikonal dispersion relation and Ruelle exponents for several values
of the black hole spin. For small spins, both the dispersion relation and the Ruelle spectrum
are roughly flat, since the spin can be viewed as a small perturbation of the spherically symmetric (m-independent) case. As the spin increases, non-linearities gradually become more
pronounced, culminating in the striking graph for the near-extremal black hole. Reproducing
even the qualitative non-linear features of this curve is a sharp diagnostic for any proposed
dual to Kerr.

2

## PDF page 4

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

Figure 1. The dispersion relation for a near-extremal black hole becomes linear for

µ > µc and the Lyapunov exponent vanishes.

The rightmost plot has an interesting geometric interpretation that will be important for
this paper. As a Kerr black hole spins up and approaches the limiting extremal geometry, a
warped throat of divergent proper depth opens up outside of its event horizon [7, 8]. This
Near-Horizon Extreme Kerr (NHEK) region of spacetime exhibits a geometrically realized
emergent conformal symmetry that we will denote SL(2, R)ISO [9]. The NHEK geometry is
a warped version of the Anti-de Sitter (AdS) throats that emerge outside near-extremal nonrotating black holes. As the black hole tends to extremality, a subset of the co-rotating bound
photon orbits with µ > µc move into the NHEK region [5]. Since these geodesics co-rotate
with the horizon, Ω(µ) ≈ µΩH is linear in the NHEK regime. The infinite amount of space
in the throat allows the corresponding waves to bounce around for a long time before falling
through the horizon or escaping to infinity, so the imaginary
√ parts of the frequencies also go
to zero linearly in the deviation from extremality 0 ⩽ κ = M 2 − a2 ≪ 1, or equivalently, in
the limit of vanishing Hawking temperature TH ≈ κ/4π M (e.g. [10, 11]):
(

)
1
ω ≈ mΩH − i n +
2π TH .
2

(1.2)

In other words, the linear ramp and vanishing exponents in the right panel of figure 1 are
essentially a spectral signature of the extremal throat. The overtone structure with γL = γ/τ
independent of m signals the presence of an exact conformal symmetry geometrically realized
in the spacetime as an isometry group. In the near-extremal throat, the fundamental n = 0 mode
is highest-weight and higher overtones simply correspond to SL(2, R)ISO -descendants, with
the overtone number equal to the descendant level.
The geometric conformal symmetry of the NHEK spectrum does not extend to the nonextremal case or to the portion of the photon ring that remains outside the throat in the extremal
limit. Simply put, the imaginary parts of the frequencies depend on m, so no single set of
SL(2, R) generators L̂± could construct overtone families for all of the different values of m:
the spacings between successive overtones would simply not agree. However, in a superselection sector of fixed m (and therefore of fixed large real frequency in the geometric optics
limit), the overtone structure persists and begs for interpretation. Schematically, one anticipates an emergent SL(2, R) structure in phase space rather than in spacetime. Precisely such a
structure was identified in [6]. In an appropriately defined ‘near-ring region’ of phase space, an
emergent conformal symmetry SL(2, R)QN controls the eikonal limit of the QNM spectrum.
These symmetry generators are fibered over the photon ring, and their form depends explicitly
on the parameters γ and τ associated to each orbit. Each overtone family decomposes into two
highest-weight representations of SL(2, R)QN according to the parity of the overtone number,

3

## PDF page 5

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

and together the symmetries generate the entire eikonal QNM spectrum4 . We are used to thinking of holography in spacetime, but the most general statement of the holographic principle
might instead involve phase space. Does SL(2, R)QN have a role to play? We would love to
know the answer!
The near-ring region of Kerr exhibits yet another type of emergent conformal symmetry [6]
that we denote SL(2, R)PR and which is singled out for its direct observational relevance: it
serves as an organizing principle for the fine structure of photon rings in black hole images. The
Hamiltonian flow generated by the dilations of SL(2, R)PR drives unbound geodesics towards
the near-ring region of phase space and pushes points on the black hole image closer to the
image of the photon ring. A discrete subgroup relates successive strongly lensed images of the
same source, revealing the intricate self-similar structure of the photon ring.
Clearly, one wishes to understand the relations between these three different conformal
groups. Their relationships are obscured by the complexity of the Kerr black hole, and the
discussion would certainly benefit from a simpler exactly solvable toy model. This raises the
question: what is the simplest holographic system with a photon ring controlling its short-wave
Ruelle spectrum?
The BTZ black hole is certainly the simplest black hole with a known holographic description, but unfortunately it does not have a photon orbit at finite radius5 . Black holes in higherdimensional AdS spacetimes do admit unstably bound null orbits, but they also possess stably
trapped orbits that bounce back-and-forth off of the boundary and introduce a timescale longer
than that associated to photon rings, thereby obscuring the role of the latter. The simplest geometry known to us that admits both a photon ring and a reasonably well understood holographic
description is the self-dual warped AdS3 spacetime, which is better known as a constant-θ slice
of the near-NHEK throat.
In this paper, we accordingly study photon rings in self-dual warped AdS3 . In section 2,
we begin with a brief review of this spacetime and then show that, like NHEK, it enjoys an
SL(2, R)ISO isometry group that makes the wave equation exactly solvable in terms of hypergeometric functions. The fundamental n = 0 QNMs are highest-weight with respect to this
symmetry algebra, and the n > 0 overtones arise as SL(2, R)ISO -descendants. The geometry
has a photon orbit at finite radius. We show explicitly that the corresponding geometric optics
approximation reproduces the eikonal limit of the exact QNM spectrum, as well as the approximate near-ring wavefunctions. Interestingly, we find that in order to recover the entire eikonal
QNM spectrum from the geometric optics approximation, it is necessary to also consider a
second bound null geodesic located behind the horizon.
Next, we define the SL(2, R)QN generators that operate exclusively within the near-ring
region of phase space. Each QNM overtone family decomposes into two highest-weight representations of SL(2, R)QN , so SL(2, R)QN does not reduce to SL(2, R)ISO in the extremal
limit. These groups arise from distinct constructions, but their action on the QNM wavefunctions is related in a simple way in the near-ring region, explained below. It seems plausible
that there is a more fundamental relationship between the two symmetries, but we leave this
question to future investigation.
In section 3, we define the conformal group SL(2, R)PR that acts on the phase space of null
geodesics and contains a dilation that scales every light ray into the photon ring. Interestingly,
we find that the observationally relevant SL(2, R)PR and the geometric SL(2, R)ISO are both
4 In the extremal limit, these combine into a single highest-weight representation of the emergent SL(2, R)

ISO

isometry.
5 As we will describe in section 2, there is a sense in which the BTZ ‘photon shell’ resides at the conformal boundary
of the spacetime.
4

## PDF page 6

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

special cases of the more general SL(2, R) phase space construction explored in [6], and that
SL(2, R)PR can be thought of as a particular deformation of SL(2, R)ISO within this family.
Finally, in section 4, we discuss how the spectrum of resonances of self-dual warped AdS3
resembles that of a CFT2 with the corresponding left and right temperatures and a peculiar
identification of momenta. Although the interpretation of this match is still not rigorously
understood, we take this as evidence that the holographic dual to this black hole spacetime
encodes its photon ring, or in other words, that the photon ring is part of the hologram.
2. Warped AdS3 black holes
In this section, we describe a soluble example in the context of a known holographic duality
in string theory, in which photon ring Lyapunov exponents and late-time Ruelle resonances
can be shown to agree. The example is self-dual warped AdS3 , which is also the near-horizon
region of the near-extreme warped AdS3 black hole. Warped AdS3 is a spacetime in which
the SL(2, R)R × SL(2, R)L isometry of AdS3 is broken down to SL(2, R)R × U(1), e.g. by
fluxes or a gravitational Chern–Simons term. It is characterized by a continuous warp factor Λ
defined such that Λ = 1 for unwarped AdS3 . Such geometries arise in string theory, including
examples with exactly soluble string worldsheet CFTs [12–14]. On the boundary side, they
are related to warped CFTs [15, 16] that are integrable J̄T deformations of ordinary CFTs
[17–23]. Warped AdS3 black holes are also of special interest due to their many similarities
to Kerr black holes. In fact, in the near-extreme near-horizon limit, three-dimensional sections
of Kerr with fixed polar angle θ reduce to a self-dual warped AdS3 quotient with warp factor
θ
Λ(θ) = 1+sin
cos2 θ . The literature on these topics is extensive, including, e.g. [24–29]. Penrose
diagrams illustrating the causal structure of warped AdS3 appear in [30].
For our present purposes, we are interested in warped AdS3 with Λ > 1 both because it
possesses a photon shell and because this is the geometry that describes polar cross sections
of Kerr. Here, we show that the Lyapunov exponent that governs the exponential deviation of
nearly bound orbits from their orbital radius in the photon shell also controls the imaginary
part of QNM frequencies in the eikonal limit. This imaginary part can also be identified with
2π TH (with T H the Hawking temperature of the black hole) times the (real part of the) weight
of the associated operator in the dual warped CFT2 , as expected on general grounds. This
number is identified under bulk-boundary duality as the Ruelle exponent governing the return
to equilibrium of a slightly perturbed thermal quantum state.
The results of this section show, in this toy stringy example, that the photon shell of a black
hole describes properties of its quantum microstates in a thermal ensemble.
2.1. The near-ring region

The metric describing the near-horizon region of the near-extreme warped AdS3 black hole can
be obtained from the near-NHEK (near-extreme near-horizon Kerr) geometry by considering
hypersurfaces of constant polar angle [31–33]:
[
ds2 = ℓ2 −r (r + 4π TH ) dt2 +

]
dr 2
2
+ Λ2 [dϕ + (r + 2π TH ) dt] .
r (r + 4π TH )

(2.1)

In these coordinates, the horizon is at r = 0, T H denotes the dimensionless Hawking temperature, and ℓ is the (warped) AdS3 radius. The warp factor Λ is defined such that (2.1) reduces
to (unwarped) self-dual AdS3 when Λ = 1.
5

## PDF page 7

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

We are interested in affinely parameterized null geodesics xµ (s) = (t(s), r(s), ϕ(s)). These
have the conserved energy
[
]
E
2
=
r
(r
+
4π
T
)
ṫ
−
Λ
(r
+
2π
T
)
ϕ̇
+
(r
+
2π
T
)
ṫ
(2.2)
H
H
H
ℓ2
and angular momentum
[
]
L
2
=
Λ
ϕ̇
+
(r
+
2π
T
)
ṫ
,
(2.3)
H
ℓ2
where the dot denotes ∂s . The null condition can be written as
V(r)
r (r + 4π TH )
gµν ẋµ ẋν = ṙ 2 + 4 = 0 ,
ℓ2
ℓ

(2.4)

with
L2
2
r (r + 4π TH ) − [E + (r + 2π TH ) L] .
(2.5)
Λ2
Equations (2.2)–(2.5) imply the null geodesic equation for xµ (s). Bound photon orbits are
defined by the conditions
V(r) =

V(r) = V ′ (r) = 0 .

(2.6)

These depend only on the specific (energy-rescaled) angular momentum
λ=

L
.
E

(2.7)

The conditions (2.6) must be simultaneously solved for the critical impact parameter λ = λ̃
and the orbital radius r = r̃ of the bound geodesic. Demanding that V ′ (r̃) = 0 requires that
λ̃(r̃) = −

1
(
).
(r̃ + 2π TH ) 1 − Λ12

(2.8)

Substituting this into the constraint V(r̃) = 0 yields a quadratic equation with roots at the two
critical radii
⎛
⎞
1
1
√
r̃± = 2π TH ⎝± √
− 1⎠ ≷ 0
=⇒
λ̃± = ∓
≶0.
(2.9)
1 − Λ12
2π TH 1 − Λ12
This spacetime therefore admits two bound photon orbits with orbital period τ and angular
velocities Ω̃± given by
∣
ṫ ∣∣
1
2π
τ = ∓2π ∣
= √
> 0,
Ω̃± = ∓
≶0.
(2.10)
τ
1
ϕ̇ r=r̃± ,λ=λ̃± TH 1 − 2
Λ
We note that one orbit is prograde, while the other is retrograde. Since r̃− < 0 < r̃+ , the inner
orbit lies inside the horizon. We will thus restrict our attention to the outer orbit and consider
nearly bound null geodesics with small radial deviation δr ≡ r − r̃+ . More specifically, we are
interested in the near-ring region defined in phase space by
⎧
⎪
|δr| ≪ TH
(near-peak) ,
⎪
⎪
∣
⎪
⎨∣∣
1
∣
(near-critical) ,
∣λ − λ̃+ ∣ ≪
NEAR-RING REGION:
(2.11)
TH
⎪
2
⎪
ℓ
1
⎪
⎪
⎩ ≪
(high-energy) .
E
TH
6

## PDF page 8

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

The first condition zooms in on the bound orbit in spacetime, while the second condition zooms
in on the bound orbit in momentum space. Together, these conditions scale into the (outer)
photon shell, defined as the phase space locus
PHOTON SHELL:

δr = 0 = λ − λ̃+ .

(2.12)

The last condition in (2.11) is required in order to relate solutions of the wave equation to
geodesic congruences and will only become important in subsequent sections. As TH → 0,
we note that the near-ring region completely localizes on the bound orbit in physical space
(δr = 0) but also fills all of momentum space (with no restriction on E or λ).
The radial deviation of a nearly bound orbit grows exponentially as δr ∼ eγ n , where n is the
orbit number and γ is a Lyapunov exponent that can be determined by linearizing the geodesic
equation about the near-ring region:
1
δr̈ ≈ − 4 V ′ ′ (r̃)δr .
(2.13)
2ℓ
Since r̃+ is a local maximum of the radial potential,
V ′ ′ (r̃+ ) = −

E2
<0,
2π 2 TH2

(2.14)

the motion is indeed unstable and one finds the exponential deviation
)
(
E
s
δr(0) .
δr(s) ≈ exp
2π TH ℓ2
The increase in the affine parameter s per orbit is
∣
ˆ 2π
dϕ
2π ∣∣
(2πℓ)2 TH
√
∆s =
.
=
=
ϕ̇
ϕ̇ ∣r=r̃+ ,λ=λ̃+ E 1 − 12
0
Λ

(2.15)

(2.16)

It follows that, as a function of the orbit number n = ∆ϕ
2π , the radial deviation δr(n) increases
as
2π
γ=√
δr(n) ≈ eγ n δr(0) ,
(2.17)
.
1 − Λ12
Together with ϕ ≈ Ω̃+ t, this completes the solution of the null geodesic equation in the nearring region (2.11) of the warped AdS3 metric (2.1), where much of the interesting motion in
the black hole exterior occurs. A similar analysis applies near the inner photon shell r − r̃− =
0 = λ − λ̃− in the black hole interior, resulting in the same Lyapunov exponent γ. The solution
everywhere else in the spacetime can be written in terms of the integrals evaluated in [8], but
this full solution will not be of interest to us here.
To later connect with the QNM spectrum, we note here the simple relations
√
1
1
γ
Ω̃± =
γL ≡ = 2π TH .
(2.18)
= ∓2π TH 1 − 2 ,
Λ
τ
λ̃±
In the limit Λ → 1, the quantities r̃± , γ, and τ diverge, but the ratio γL = γτ remains finite. In
this sense, the unwarped AdS3 photon shell (2.12) resides at the conformal boundary.
2.2. QNM spectrum

In this section, we compute the QNM frequencies of the (self-dual) warped AdS3 spacetime (2.1), whose imaginary parts become the Ruelle exponents. We are primarily interested
7

## PDF page 9

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

in photons, but since the effects of spin are subleading in the geometric optics regime, it is
sufficient for our purposes to solve the wave equation for a massless scalar field Φ(xµ ) in the
background (2.1)6 :
∇2 Φ = 0 .

(2.19)

Inserting the ansatz Φ(t, r, ϕ) = e−iωt+imϕ ψ(r), this reduces to a second-order ODE for the
radial function ψ(r),
r (r + 4π TH ) ψ ′ ′ (r) + (2r + 4π TH ) ψ ′ (r)
[
]
2
[ω + m (r + 2π TH )]
1
+
− m2 − β 2 +
ψ(r) = 0 ,
r (r + 4π TH )
4
where we have defined
√(
1−

β = im

1
Λ2

)
−

1
.
4m2

(2.20)

(2.21)

This is a form of the hypergeometric equation and the solutions are given in terms of ω̂ = 2πωTH
as
ψ in (r) = r− 2 (ω̂+m)
i

(

r
+1
4π TH

) 2i (ω̂−m)

[

2 F1

1
1
r
+ β − im, − β − im; 1 − i (ω̂ + m) ; −
2
2
4π TH

]

,

(2.22)
(

i

ψ out (r) = r+ 2 (ω̂+m)

r
+1
4π TH

) 2i (ω̂−m)

[
2 F1

1
r
1
+ β + iω̂, − β + iω̂; 1 + i (ω̂ + m) ; −
2
2
4π TH

]
.

(2.23)
The first solution ψ in (r) is ‘ingoing’ in the sense that a local observer at the horizon will see
infalling particles going into the black hole. The second solution ψ out (r) has particles coming
out of the past horizon and therefore does not correspond to QNMs, but rather to ‘anti-QNMs’
(appendix A). Near the horizon,
r→0

ψ in (r) ≈ r− 2 (ω̂+m) ,
i

r→0

i

ψ out (r) ≈ r+ 2 (ω̂+m) ,

(2.24)

while for r ≫ 4π TH ,
1
i
r→∞
1
Γ(2β)Γ [1 − i (ω̂ + m)]
(1
) (1
) (4π TH ) 2 −β− 2 (ω̂+m) r− 2 +β + (β → −β) ,
ψ in (r) ≈
Γ 2 + β − im Γ 2 + β − iω̂
(2.25)
r→∞

ψ out (r) ≈

1
i
1
Γ(2β)Γ [1 + i (ω̂ + m)]
(1
) (1
) (4π TH ) 2 −β+ 2 (ω̂+m) r− 2 +β + (β → −β) .
Γ 2 + β + im Γ 2 + β + iω̂
(2.26)

Resonances occur when one of these terms vanishes. For the ‘in’ modes, the resonant frequencies are of the form
1
∓ β − iω̂ = −n
(2.27)
2

6 Due to the large isometry group of this spacetime, we expect separation of variables and the method of highest-

weight representations to also apply to vector and tensor QNMs (see, e.g. [34]).
8

## PDF page 10

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

for some integer n ∈ N = {0, 1, 2, . . .}. Inserting (2.21) and recalling that ω̂ = 2πωTH , (2.27)
takes the explicit form
√(
)
1
1
1
iω
∓ im
1− 2 −
−
= −n .
(2.28)
2
Λ
4m2 2π TH
Solving for ω then yields the spectrum of resonant frequencies
√(
)
(
)
1
1
1
−
i
n
+
2π TH ,
m∈Z,
ωmn± = ∓2π TH m
1− 2 −
Λ
4m2
2

n∈N.

(2.29)

Since Imωmn± < 0, the associated modes decay exponentially in the future, so we recognize
ωmn± to be the spectrum of QNM frequencies. Likewise, the anti-QNM frequencies are resonances of the ‘out’ modes (appendix A).
In the eikonal regime |m| ≫ 1, the QNM spectrum (2.29) becomes
√
(
)
|m|≫1
1
1
2π TH
ωmn± ≈ ∓2π TH m 1 − 2 − i n +
(2.30)
Λ
2
(
)
1
= mΩ̃± − i n +
γL ,
(2.31)
2
which shows that the photon shell controls the QNM spectrum ωmn± in the eikonal limit. More
precisely, the outer photon shell governs the branch with m/Reωmn+ = λ̃+ < 0, while the inner
photon shell governs the branch with m/Reωmn− = λ̃− > 0. As expected, the full photon shell
is needed to recover the complete QNM spectrum.
A closely related calculation in the near-horizon region of (near-)extreme Kerr [33] shows
that h = 12 + β is the conformal weight of a massless scalar under the SL(2, R) isometry of
warped AdS3 , and hence also of the associated boundary operator in the dual field theory.
Equation (2.27) simply reflects the fact that the thermal two-point function of such a primary
field with Re(h) = 12 has the leading long-time behavior e−2π TH t in the Gibbs state.
In the context of AdS3 holography, BTZ black holes are dual to thermal states in CFT2 ,
and the thermal two-point function takes a universal form that can be recovered by summing
over the spectrum of QNMs [35, 36]. Likewise, in the context of warped AdS3 holography,
summing over QNMs with frequencies (2.31) produces a hyperbolic sine, which matches the
form of the thermal two-point correlator in the putative dual warped CFT2 [37].
2.3. Conformal symmetry of the QNM spectrum

For the remainder of our discussion, it is convenient to work in the coordinates
√
4π TH
4π TH
T = 2π TH t ,
x = log 1 +
,
r = 2x
.
r
e −1

(2.32)

The horizon is now located at x → ∞ while the boundary resides at x = 0, and the metric takes
the simple form
[
(
)2 ]
2
2
−dT
+
dx
dT
ds2 = ℓ2
+ Λ2 dϕ +
(2.33)
.
tanh x
sinh2 x
The isometry group is SL(2, R) × U(1) with generators
L̂µ0 ∂µ = −∂T ,

L̂µ± ∂µ = e±T (− cosh x∂T ∓ sinh x∂x + sinh x∂ϕ ) ,
9

Wµ0 ∂µ = ∂ϕ ,

(2.34)

## PDF page 11

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

which obey the SL(2, R) × U(1) commutation relations
[
]
[
]
L̂0 , L̂± = ∓L̂± ,
L̂+ , L̂− = 2L̂0 ,

[

]
W0 , L̂m = 0 .

(2.35)

The Killing vectors define quantities L̂m = L̂µm pµ that are conserved along geodesics and for
our purposes best thought of as Hamiltonian functions in the six-dimensional phase space
(T, x, ϕ, pT , px , pϕ ) with canonical symplectic form:
L̂± = e±T [−pT cosh x + (pϕ ∓ px ) sinh x] ,

L̂0 = −pT ,

W0 = pϕ . (2.36)

The action of the spacetime vectors (2.34) then lifts in the obvious way to a phase space action,
with the Hamiltonian functions (2.36) acting via the Poisson bracket (with {xµ , pµ } = −1) and
satisfying the SL(2, R) × U(1) algebra (2.35).
The inverse metric is reducible in terms of the Killing vectors
(
)
L̂µ L̂ν + L̂ν+ L̂µ−
1
ℓ2 gµν = L̂µ0 L̂ν0 − + −
− 1 − 2 Wµ0 Wν0 ,
(2.37)
2
Λ
so the Laplacian may be expressed as the Casimir of SL(2, R) × U(1):
[
(
)
]
LL̂+ LL̂− + LL̂− LL̂+
1
1
2
2
2
∇ Φ = − 2 −LL̂0 +
+ 1 − 2 LW 0 Φ .
ℓ
2
Λ

(2.38)

The mode ansatz Φ(T, x, ϕ) = e−iω̂T+imϕ ψ(x) reduces the massless wave equation ∇2 Φ = 0
to the radial ODE
1
− β2
V(x) = ω̂ 2 + m2 + 2ω̂m coth x + 4 2 ,
sinh x

ψ ′ ′ (x) + V(x)ψ(x) = 0 ,

(2.39)

with β as in (2.21). We note that ω̂T = ωt. The potential satisfies V(x̃± ) = V ′ (x̃± ) = 0 when
m = λ̃± ω = λ̂± ω̂ with
√
1
1
1
λ̂± = 2π TH λ̃± = ∓ √
Ω̂± =
.
(2.40)
,
x̃± = ±arctanh 1 − 2 ,
Λ
λ̂±
1− 1
Λ2

In particular, one has cothx̃± = −λ̂± . The two independent solutions of the radial ODE (2.39)
are
[
]
1
1
1
im
in
iω̂ x
ψ (x) = e (sinh x) 2 F1
+ β − im, − β − im; 1 − i (ω̂ + m) ;
,
(2.41)
2
2
1 − e2x
]
[
1
1
1
−iω̂
out
−imx
ψ (x) = e
(sinh x)
+ β + iω̂, − β + iω̂; 1 + i (ω̂ + m) ;
,
(2.42)
2 F1
2
2
1 − e2x
with asymptotics at the boundary x = 0 given by
x→0 2

ψ in (x) ≈

−im

x→0 2

ψ out (x) ≈

(2x) 2 −β Γ(2β)Γ [1 − i (ω̂ + m)]
(1
) (
) + (β → −β) ,
Γ 2 + β − im Γ 12 + β − iω̂

(2.43)

(2x) 2 −β Γ(2β)Γ [1 + i (ω̂ + m)]
(
) (
) + (β → −β) .
Γ 12 + β + im Γ 12 + β + iω̂

(2.44)

iω̂

1

1

We have already analyzed the resonances of these modes in section 2.1. For the ‘in’ modes,
resonances arise when 21 ∓ β − iω̂ = −n, resulting in the spectrum (2.29) of QNM frequencies.
The QNMs are thus
10

## PDF page 12

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

Φmn± (T, x, ϕ) = e−iω̂T+imϕ+iω̂x (sinh x)im 2 F1

(
ω̂ = ω̂mn± = ±iβ − i n +

[

1
2

1
1
1
+ β − im, − β − im; 1 − i (ω̂ + m) ;
2
2
1 − e2x

]
,

(2.45)

)
,

(2.46)

where the two branches ± of the spectrum are associated with the outer and inner photon
shell, respectively. The anti-QNMs are similarly obtained as resonances of the ‘out’ modes in
appendix A. In the eikonal regime |m| ≫ 1,
√
|m|≫1
|m|≫1
1
β ≈ im 1 − 2 = ∓imΩ̂±
=⇒
±iβ ≈ mΩ̂± ,
(2.47)
Λ
(
)
|m|≫1
so ω̂mn± ≈ mΩ̂± − i n + 12 as expected from (2.31), and the fundamental n = 0 mode
behaves as
|m|≫1

1

Φm0± (T, x, ϕ) ≈ 2 2 +imΩ̂± −im e−( 2 +imΩ̂± )T+imϕ+imx (sinh x) 2
1

1

+imΩ̂±

.

(2.48)

From now on, we focus on the outer bound orbit at x̃ = x̃+ with angular velocity Ω̂ = Ω̂+ ,
which controls the + branch ωmn = ωmn+ of the QNM spectrum. Suppressing the + subscript
and dropping constant factors, we obtain>
|m|≫1

1

Φm0 (T, x, ϕ) ∼ e−( 2 +imΩ̂)T+imϕ+imx (sinh x) 2
1

+imΩ̂

.

(2.49)

Independent of the eikonal approximation, one can verify that the n = 0 fundamental QNMs
are highest-weight and that their n > 0 overtones are SL(2, R)-descendants. Indeed, the modes
−ĥT+imϕ+imx
ΦHW
(sinh x) ,
m0 (T, x, ϕ) = e

ĥ

ĥ =

|m|≫1 1
1
−β ≈
+ imΩ̂ ,
2
2

(2.50)

satisfy
LL̂+ ΦHW
m0 = 0 ,

HW
LL̂0 ΦHW
m0 = ĥΦm0 ,

and their SL(2, R) descendants obey
n
HW
ΦHW
mn = LL̂− Φm0 ,

HW
LHW
W0 Φm0 = imΦm0 ,

(
)
LL̂0 ΦHW
=
ĥ
+
n
ΦHW
mn
mn .

(2.51)

(2.52)

These SL(2, R) towers of modes reproduce the exponentially decaying QNM overtones up to
normalization:
[n−1
]
∏
HW
−ĥ+im
Φmn = 2
ĥ + k + im Φmn .
(2.53)
k =0

The exact value of the relative amplitude of successive QNM overtones is
(
)
ΦHW (T, x, ϕ)
= 2e−T ĥ cosh x + im sinh x .
um = m1
HW
Φm0 (T, x, ϕ)

(2.54)

In the eikonal limit |m| ≫ 1, we can approximate ĥ ≈ imΩ̂ = im
, with λ̂ = λ̂+ , simplifying this
λ̂
ratio to
(
)
(
)
um ≈ 2imΩ̂e−T cosh x + λ̂ sinh x ∼ e−T cosh x + λ̂ sinh x .
(2.55)
In the next sections, we will want to compare the exact modes (2.50) to their near-ring and
geometric optics approximations near the (outer) bound orbit x ≈ x̃. Letting δx = x − x̃ and
|m|≫1

using ĥ ≈ imΩ̂, we find that
11

## PDF page 13

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al
|m|≫1

ĥ

eimx (sinh x) = eimx eĥ log sinh x ≈ eimx+imΩ̂ log sinh x

|δ x|≪1

≈ c0 e

− 2i

mΩ̂
δ x2
Λ2 −1

,

(2.56)

so that very near the bound orbit, the exact QNM wave functions (2.50) with large m behave
(up to a constant) as
1
− 12 T−imΩ̂(T+ 21 kδ x2 )+imϕ
,
k≡ 2
.
ΦHW
(2.57)
m0 (T, δx, ϕ) ∼ e
Λ −1
A similar analysis shows that the anti-QNM overtones are SL(2, R)-descendants of the lowestweight n = 0 mode.
2.4. QNMs in the near-ring region

In this section, we study the QNMs in the near-ring region of the warped AdS3 metric (2.1)
and show that they form a shadow pair of highest-weight representations of an emergent nearring SL(2, R)QN symmetry, which differs from the geometrically realized conformal symmetry
generated by the vector fields L̂m given in (2.34).
The near-ring region for waves on warped AdS3 is defined in analogy with (2.11) as
⎧
|δr| ≪ TH
|δx| ≪ 1
(near-peak) ,
⎪
⎪
⎪
∣
∣
∣
∣
⎪
⎨∣ m
∣
∣m
∣
1
∣
∣
∣
∣
(near-critical) ,
NEAR-RING REGION:
∣ ωR − λ̃∣ ≪ TH
∣ ω̂R − λ̂∣ ≪ 1
⎪
⎪
⎪
⎪
⎩ 1 ≪ 1
1 ≪ ω̂R
(high-frequency) .
ωR
TH
(2.58)
This defines a region of the phase space of waves on warped AdS3 , rather than simply a region
of spacetime. Still focusing on the outer photon shell, the wave potential (2.39) in this near-ring
region takes the simple form
V(x̃ + δx) ≈

ω̂R2
2
(Λ2 − 1)

δx2 −

2iω̂R ω̂I
,
Λ2 − 1

(2.59)

and the radial ODE for ψ(x) reduces to
[
]
1
ω̂R2
iω̂I
2
2
∂ +
δx ψ(δx) = 2
ψ(δx) .
(2.60)
2ω̂R δx (Λ2 − 1)2
Λ −1
(
)−1
> 0 as
We may rewrite this in terms of k = Λ2 − 1
[
]
1
Hψ = iω̂I ψ ,
H=
∂δ2x + k2 ω̂R2 δx2 .
(2.61)
2kω̂R
This is precisely the time-independent Schrödinger equation for eigenstates ψ of the upsidedown harmonic oscillator with associated eigenvalues iω̂I , which are allowed to be imaginary
because the boundary conditions are non-Hermitian. Interestingly, in this example, the nearring approximation for the imaginary part of the QNM spectrum is exact.
Following [6], we now define the operators (recall that T = γL t)
e±T
a± = √
(∓∂δx − ikω̂R δ x) ,
2kω̂R

i
i
L 0 = − ( a+ a− + a− a+ ) = H ,
4
2

a2
L± = ± ± .
2

(2.62)

The a± generate the Heisenberg algebra [a+ , a− ] = iI, while the Lm obey the exact SL(2, R)QN
commutation relations:
[L0 , L± ] = ∓L± ,

[L+ , L− ] = 2L0 .
12

(2.63)

## PDF page 14

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

Although these operators are defined everywhere, they are only useful in the near-ring region
where L0 is proportional to the Hamiltonian H. The eigenstates of L0 satisfy L0 ψh = hψh ,
so we may identify ω̂I = −2h, or equivalently, ωI = −2γL h. The mode ansatz Φ(T, x, ϕ) =
e−iω̂T+imϕ ψ(x) reduces in the near-ring region (2.58) to
Φ(T, δx, ϕ) ≈ e−iω̂R T+imϕ Φh (T, δx) ,

Φh (T, δx) = eω̂I T ψh (δx) = e−2hT ψh (δx) . (2.64)

Though the operator L0 does not admit a normalizable ground state, it can still produce a
discrete spectrum provided that boundary conditions are chosen appropriately. The QNM
boundary condition for the fundamental mode is equivalent to the highest-weight condition
L+ Φh = 0, which admits two solutions with h = 14 and h = 43 :
Φ 1 (T, δx) = e− 2 T ψ 1 (δx) ,

ψ 1 (δx) = e− 2 kω̂R δx ,

Φ 3 (T, δx) = e− 2 T ψ 3 (δx) ,

ψ 3 (δx) = δx e− 2 kω̂R δx .

1

4

(2.65)

4

3

4

2

i

4

2

i

4

4

(2.66)

The action of SL(2, R)QN then produces a tower of descendants that are precisely the higher
overtones:
(√
)
Φh,N (T, δx) = LN− Φh (T, δx) = e−2(h+N)T ψh+N (δx) ∝ e−2(h+N)T D2(h+N)− 1
2ikω̂R δx ,
2

(2.67)
where Dn (t) denotes the nth parabolic cylinder function. Since at the edges δx → ±∞ of the
near-peak region,
(√
) δx→±∞
2
i
Dn
2ikω̂R δx
≈ δxn e− 2 kω̂R δx ,
(2.68)
and recalling that ω̂R = mΩ̂, it follows that the nth overtone behaves near the edges as
Φmn (T, δx, ϕ)

δ x→±∞ −(n+ 1 )T
2

∼

e

δxn e−iω̂R (T+ 2 kδx )+imϕ ,
1

2

(2.69)

which agrees with the highest-weight QNMs (2.57) in the near-ring region (2.58). Likewise,
imposing a lowest-weight condition would reproduce the n = 0 anti-QNM (A.13), whose L+
descendants are the near-ring anti-QNM overtones
Φ̃mn (T, δx, ϕ)

δ x→±∞ +(n+ 1 )T
2

∼

e

δxn e−iω̂R (T− 2 kδx )+imϕ .
1

2

(2.70)

Now we would like to compare the emergent SL(2, R)QN symmetry of the near-ring region
with the exact spacetime isometry SL(2, R)ISO . We will only compare their actions on the
QNMs within the near-ring region in which the SL(2, R)QN symmetry actually emerges. In that
region, SL(2, R)QN acts on functions via the differential operators L± defined in (2.62), while
SL(2, R)ISO acts on them via the Lie derivative taken along its vector field generators (2.34).
From (2.52), we see that SL(2, R)ISO acts on the QNM overtone number as n → n + 1,
while from the preceding discussion we see that SL(2, R)QN acts on it as n → n + 2. It thus
follows that within the near-ring region,
L± Φmn ∝ L2L̂± Φmn .
Similarly,

L0 Φmn = 2i HΦmn = − 12 ω̂I Φmn ,

(2.71)

)
1(
LL̂0 − Ω̂LW0 Φmn .
2
13

using

Φmn ∼ e−(iω̂T+imϕ ,

we) have
LL̂0 Φmn = −∂T Φmn = iω̂Φmn and LW0 Φmn = ∂ϕ Φmn = imΦmn , so that LL̂0 − Ω̂LW0 Φmn =
(
)
i ω̂R + iω̂I − mΩ̂ Φmn = −ω̂I Φmn . Hence,
L0 Φmn =

while

(2.72)

## PDF page 15

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

2.5. QNMs from geometric optics

In this section, we reproduce some results from sections 2.2 and 2.3 using the geometric optics
approximation. Waves with large frequencies compared to the local curvature scale take the
approximate form
Φ ≈ AeiS ,

(2.73)

with a rapidly varying phase S(xµ ) and a slowly varying amplitude A(xµ ). In terms of the
gradient
pµ = ∂µ S ,

(2.74)
µ

which is normal to the wavefronts of constant S(x ), the wave equation takes the form
−pµ pµ A + i (2pµ ∇µ A + A∇µ pµ ) + ∇2 A = 0 .

(2.75)

In the geometric optics approximation, this equation is solved order-by-order in inverse powers
of p. At leading order,
pµ pµ = 0 ,

pµ ∇ µ pν = 0 ,

(2.76)

so that p is required to be tangent to a null geodesic. At subleading order, the parallel transport
of the amplitude along the congruence is related to the expansion θ = ∇µ pµ as
1
pµ ∂µ log A = − θ .
(2.77)
2
This implies that the expansion controls the exponential behavior of the amplitude with respect
to affine parameter:
1
1
∂s log A = − θ
(2.78)
=⇒
A ∼ A 0 e− 2 θ s .
2
According to (2.77), any quantity that does not vary along the null congruence can be used to
build towers of approximate solutions to the wave equation given some seed solution. More
precisely, if a function u(xµ ) satisfies

pµ ∂µ u = 0

(2.79)

along the congruence, and moreover if
Φ0 ≈ A0 eiS

(2.80)

is an approximate (to leading and subleading order) solution to (2.75), then it follows
from (2.77) that
Φn ≈ un A0 eiS

(2.81)

is also an approximate solution to the wave equation. In other words, if A0 is an amplitude
solving (2.77) along a congruence with tangent p, then so is An = un A0 . As we will show,
the ‘minimal’ solution to (2.77) for ‘critical’
(i.e. asymptotically bound) rays in the near-ring
1 √
region (2.58) takes the form A0 = e− 2 T sinh x, and according to (2.17) and (2.18), the quantity
u = e−T δx

(2.82)

is constant on the unstable critical orbit and obeys (2.79) in the near-ring region. Geometric
optics therefore produces a family of solutions associated to the same bound photon orbit but
differing in the amplitude:
Φmn (T, δx, ϕ) ≈ e−(n+ 2 )T (δx) eiS(T,δx,ϕ) .
1

n

14

(2.83)

## PDF page 16

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

As we will now show, this expression precisely reproduces the near-ring expression (2.69) for
the QNMs.
Null geodesics in (2.33) have a conserved energy ω̂ = −pT and angular momentum m = pϕ .
Their momentum is
ˆ x√
pµ = ∂µ S ,
S = −ω̂T + mϕ ±x
V(x ′ )dx ′ ,
(2.84)
where V(x) is the radial potential (2.39), ±x = signpx , and S is a Hamilton–Jacobi principal
function. Here, we focus on unstable critical rays with impact parameter m/ω̂ = λ̂ = Ω̂−1
given in (2.40). Their momentum and phase are
p̂µ = ∂µ Ŝ ,

[
ˆ x(
Ŝ = ω̂ −T + λ̂ϕ +
x̃

) ]
[
]
1
′
+
λ̂
dx
=
ω̂
−
T
+
λ̂ϕ
+
λ̂
x
+
log
(
sinh
x
)
+
C
,
tanh x ′

(2.85)
where the integration constant C is an irrelevant phase shift. Because these geodesics asymptote to the peak of their radial potential V(x) (located at a double root x = x̃, which they cannot
cross), they form congruences with precisely the right behavior to approximate wave solutions obeying QNM boundary conditions (namely, purely ingoing at the horizon and purely
outgoing at the boundary). The expansion of these congruences is
ω̂
θ = ∇2 Ŝ = − 2 .
(2.86)
ℓ
The subleading equation (2.77) for the wave amplitude A(T, x) takes the explicit form
[(
(
)
]
)
1
λ̂
1
+ λ̂ ∂x + 1 +
∂T −
A(T, x) = 0 .
(2.87)
tanh x
tanh x
2 sinh2 x
It admits a minimal solution (with the simplest radial dependence after separation of variables)
1 √
A0 (T, x) = e− 2 T sinh x ,

(2.88)

which generates an infinite family of solutions of the form

(
)
u(T, x) = e−T cosh x + λ̂ sinh x .

An (T, x) = un (T, x)A0 (T, x) ,

(2.89)

Recalling that ω̂ = mΩ̂ for critical rays, the eikonal approximation to the QNMs is

(
)n
1
1
Φmn (T, x, ϕ) ≈ An (T, x)eiŜ(T,x,ϕ) = e−nT cosh x + λ̂ sinh x e−( 2 +imΩ̂)T+imϕ+imx (sinh x) 2 +imΩ̂ . (2.90)

In particular, setting n = 0 in this formula results in
1

Φm0 (T, x, ϕ) ≈ A0 (T, x)eiŜ(T,x,ϕ) = e−( 2 +imΩ̂)T+imϕ+imx (sinh x) 2
1

+imΩ̂

, (2.91)

which precisely reproduces the eikonal limit (2.49) of the fundamental QNM. Likewise, the
geodesic approximation (2.90) predicts that successive overtones differ by the ratio u(T, x)
given in (2.89), which also matches the eikonal limit of the exact ratio given in (2.55) for
QNMs. We note that to first order in the near-ring region,
e−T δx
u(T,x̃ + δx) ≈ − √
,
Λ2 − 1

(2.92)

so that in this region of phase space, these quantities take the simple form u ∼ e−T δx, in accord
with (2.82).
15

## PDF page 17

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

When the spacetime admits an SL(2, R) isometry (as is the case here), the geometric optics
construction of the overtone wavefunctions has a clear explanation in terms of this symmetry.
On a critical trajectory with critical momentum p̂, the Hamiltonian functions (2.36) take the
approximate form in the near-ring region x = x̃ + δx
(
)
(2.93)
L̂+ (p̂) = 0 ,
L̂− (p̂) = 2ω̂e−T cosh x + λ̂ sinh x ∝ u(T, x) .
This is equivalent to the statement that the phase function Ψ0 = eiŜ is highest-weight with
respect to SL(2, R)ISO , and we could equivalently express (2.89) as
An (T, x) ∝ L̂n− (T, x, p̂)A0 (T) .

(2.94)

This equation states that to generate higher overtone amplitudes based on a critical congruence, one simply multiplies the seed amplitude by the Hamiltonian function L̂− (x, p̂). This is
of course the geometric optics analogue of the exact statement that the higher-overtone wavefunctions are conformal descendants,
Φmn ∝ LnL̂− Φm0 .

(2.95)

This follows because, to leading order in the geometric optics approximation,
(
)
(
)
L̂µ∓ ∂µ A0 eiŜ = iA0 L̂µ∓ p̂µ eiŜ + subleading .

(2.96)

The constructions (2.90) and (2.94) are equivalent because they both rely on solutions to the
equation pµ ∂µ L(x, p) = 0. The quantity L̂− (x, p) = L̂µ− pµ solves this equation for any geodesic
congruence by virtue of the Killing equation, while u(T, x) satisfies it specifically for the critical trajectory p̂ to which the QNMs are associated.
3. Observable conformal symmetry of the ‘photon ring’
In this section, we define the observable conformal symmetry SL(2, R)PR of the ‘photon ring’
and explore its relationship with the spacetime isometry group SL(2, R)ISO of the warped AdS3
metric (2.1).
3.1. Successive images are related by a dilation

Black hole images in three dimensions are somewhat trivial, since the observer’s screen is just
a line, rather than a plane, and the image of the (outer) bound orbit is a single critical point,
rather than a (closed) critical curve. However, this simple case is still rich enough to illustrate
the SL(2, R)PR construction recently applied to Schwarzschild and Kerr black holes [6]. Since
the WAdS3 metric (2.1) is not of direct astrophysical interest, we treat it telegraphically and
refer the reader to [6] for a more detailed analysis.
The phase space Γ of null geodesics in the geometry (2.33) is four-dimensional, with
coordinates (x, ϕ, px , pϕ ), canonical symplectic form Ω = dpx ∧ dx + dpϕ ∧ dϕ, and Hamiltonian (obtained by solving gµν pµ pν = 0 for H = −pt )
√
p2ϕ
pϕ
− p2x +
H=−
.
(3.1)
tanh x
Λ2 sinh2 x
The (outer) bound orbit has (x, px ) = (x̃, 0), and critical energy
√
pϕ
1
H̃ =
= −pϕ 1 − 2 > 0 ,
Λ
λ̂
16

(3.2)

## PDF page 18

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

which is positive since pϕ < 0 because the orbit is counter-rotating. This dynamical system is integrable and therefore admits a canonical transformation to action-angle variables
(x, ϕ, px , pϕ ) → (T, Φ, H, L) given by
[
]
H + L coth x
L
dx
√
dT = √
dx , dΦ = dϕ + coth x (H + L coth x) −
, L = pϕ ,
Λ2 sinh2 x
V(x)
V(x)
(3.3)
where the radial geodesic potential is
L2
.
(3.4)
Λ2 sinh2 x
As expected, this canonical transformation preserves the symplectic form: Ω = dH ∧ dT +
dL ∧ dΦ.
The action-angle variables trivialize the dynamics:
2

V(x) = (H + L coth x) −

Ḣ = {H, H} = 0 ,

L̇ = {L, H} = 0 ,

Φ̇ = {Φ, H} = 0 ,

Ṫ = {T, H} = 1 .

(3.5)

The first two equations indicate that the phase space Γ foliates into superselection sectors of
fixed (H, L), which are conserved momenta. The third equation implies that a photon with
initial coordinates (xs , ϕs , H, L) evolves to final coordinates (xo , ϕo , H, L) such that
]
ˆ ϕo
ˆ xo [
dx
L
√
∆ϕ = ϕo − ϕs = − dϕ = − − coth x (H + L coth x) −
,
(3.6)
2
2
Λ sinh x
V(x)
ϕs
xs
where the slash indicates that the integral is to be evaluated along the photon trajectory. The
last equation identifies T as the variable conjugate to energy, i.e. time. Hence, the time elapsed
along a geodesic as it evolves from (xs , ϕs , H, L) to (xo , ϕo , H, L) is
ˆ xo
H + L coth x
√
T= −
dx .
(3.7)
V(x)
xs
Equations (3.6) and (3.7) represent the solution to the null geodesic equation in the warped
AdS3 metric (2.33), reduced to a problem of quadratures. These integrals can be evaluated in
terms of elliptic integrals [8].
Since we are interested in optical images of sources far from the black hole, here we focus
on geodesics that begin and end at the boundary x = 0 and therefore always remain outside
the bound orbit at x = x̃. A distant observer at large radius xo → 0 near the boundary receives
these geodesics with impact parameter
λ=

L
1
> λ̂ = − √
.
H
1− 1

(3.8)

Λ2

√
The radius of closest approach is reached when the radial momentum px = ± V(x) vanishes.
This occurs at the smallest root of the radial potential V(x), namely
[ √
]
√
λ Λ2 + λ2 (1 − Λ2 ) − λΛ2
1
xmin = arctanh
⩽ x̃ = arctanh 1 − 2 .
(3.9)
2
2
Λ +λ
Λ
Geodesics with Ĥ = 0 are critical and asymptote to the closed photon orbit at x = x̃ in the far
past and/or future. Their impact parameter λ = λ̂ defines the ‘critical point’ on the image line.
Points to the right of this critical point can be illuminated, while the observer screen to the left
is dark.
17

## PDF page 19

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

It is possible to define on the phase space Γ an action of a conformal group SL(2, R)PR with
generators
H+ = Ĥ ,

H0 = −TH+ ,

H− = T2 H+ ,

(3.10)

which obey the correct algebra since (T, H) are canonically conjugate. These transformations
correspond to the finite SL(2, R) ∼
= Sp(2, R) symplectomorphisms (appendix B.1)
(
)
(
)
aT + b
2
T, Ĥ −→
(3.11)
ad − bc = 1 ,
, (cT + d) Ĥ ,
cT + d
which leave the photon shell Ĥ = 0 invariant—it is, in fact, the only SL(2, R)PR -invariant submanifold of phase space.
SL(2, R)PR also has an interesting action on the image line. Since it commutes with the U(1)
generated by L, it acts within superselection sectors ΓL of fixed angular momentum. However,
it does modify the energy (or photon color) H = H+ + H̃. It therefore also modifies the impact
parameter and the radius of closest approach for each geodesic. Indeed, the ‘photon ring’ is an
attractive fixed point for the phase space flow generated by e−sH 0 , under which
Ĥ(0) → Ĥ(s) = e−s Ĥ(0) .

(3.12)

For large s, Ĥ becomes small while T → ∞.
For a critical orbit with H+ = 0, expanding the first relation in (3.3) for small δx = x − x̃ < 0
yields
dT ≈ d log δx

=⇒

δx ≈ δx0 eT .

(3.13)

Since the point of closest approach to the photon shell is given by
δx2min =

2Λ2 Ĥ
+ ...
λ̂ L

(3.14)

to leading order as Ĥ → 0, log δxmin decreases linearly under the SL(2, R)PR dilations (3.12)
and
1
∂s log δxmin = − .
(3.15)
2
Expanding (3.6) for small δxmin shows that near the photon shell,
∆ϕ =

1

(3.16)
log δxmin ,
λ̂
so that the number of orbits around the black hole w = ∆ϕ/2π diverges linearly under
dilations:
1
1
.
∂s w = −
=
(3.17)
2γ
4π λ̂
We would now like to understand the effect of the dilations (3.12) on images of a source in
the geometry (2.33). We assume there is a source star located at (xs , ϕs ) emitting light of all
colors isotropically, as well as a telescope at (xo , ϕo ). There are an infinite number of (colored)
geodesics connecting the source to the observer, each distinguished by the winding number
around the black hole. Since these geodesics share the same endpoints, they also share the same
net angular shift ∆ϕ modulo 2π. Geodesics with |w| > 12 contribute to the observed photon
ring.
Consider null geodesics of fixed pϕ = L. Demanding that the geodesics connect a source
point (xs , ϕs ) with an observer point (xo , ϕo ) cuts ΓL down to a discrete set of geodesics Γobs
18

## PDF page 20

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

labeled by the (integer part of their) winding number ⌊w⌋. In the limit w → ∞, the finite
dilation
D0 = e−2γ H0

(3.18)

relates geodesics with successive winding numbers w → w + 1. The products Dk0 for k ∈ Z

constitute a (w-independent) discrete subgroup of SL(2, R)PR mapping Γobs onto itself. This
emergent discrete scaling symmetry generates successive subring images in the ‘photon ring’
that asymptotically approach the critical point.
3.2. SL(2, R)PR and SL(2, R)ISO

When the black hole reaches zero temperature, TH = 0, the metric (2.1) reduces to
[
]
dr 2
2
2
2
2 2
2
ds = ℓ −r dt + 2 + Λ (dϕ + rdt) .
r
This spacetime admits an isometry group SL(2, R)0ISO generated by Killing vectors
)
(
1
2
Ĥ+ = ∂t ,
Ĥ0 = t∂r − r∂r ,
Ĥ− = t2 + 2 ∂t − 2tr∂r − ∂ϕ ,
r
r

(3.19)

(3.20)

which act on the six-dimensional phase space (t, r, ϕ, pt , pr , pϕ ) via SL(2, R)0ISO -generating
functions Ĥn = −Ĥµn pµ . Like their finite-temperature analogues L̂n , these functions all commute with the constrained Hamiltonian
[
]
2
p2ϕ
1 µν
1
(pt − rpϕ )
2 2
H = g pµ pν = 2 r pr −
+ 2 ≡0,
(3.21)
2
2ℓ
r2
Λ
so they are conserved charges along geodesics, and they have the same Casimir
(
)
Ĥ+ Ĥ− + Ĥ− Ĥ+
L̂+ Ĥ− + L̂− L̂+
1
2
2
C = −Ĥ0 +
= −L̂0 +
= − 1 − 2 p2ϕ . (3.22)
2
2
Λ
In the four-dimensional phase space (r, ϕ, pr , pϕ ), null geodesic motion is generated by the
Hamiltonian H = −pt , which is obtained by solving the dynamical constraint H = 0 to find
√
⎛
⎞
p2ϕ
H = −r ⎝pϕ + r 2 pr2 + 2 ⎠ .
(3.23)
Λ
As reviewed in appendix B, the coordinate time T(r, ϕ, pr , pϕ ) elapsed along geodesic flow
is the function that obeys {T, H} = 1, which for this Hamiltonian gives (up to an integration
constant T0 )
rpr
− T0 .
T=−
(3.24)
H
Under phase space reduction at time t = t0 , the functions Ĥn = −Ĥµn pµ defined from (3.20)
reduce to
(
)
1
2
2
ĥ+ = H ,
ĥ0 = t0 H + rpr ,
ĥ− = t0 + 2 H + 2t0 rpr + pϕ ,
(3.25)
r
r
where t0 is now just a constant. We note that the functions ĥ± are no longer conserved in fourdimensional phase space, since they do not commute with the Hamiltonian H and therefore
change the energy (or photon color) of a null geodesic. We now fix T0 = t0 and set
19

## PDF page 21

Class. Quantum Grav. 40 (2023) 095006

rpr
T=−
− t0 ,
H

D Kapec et al

ĥ+ ĥ− + ĥ− ĥ+
C ≡ −ĥ20 +
=−
2

(

1
1− 2
Λ

)
p2ϕ .

(3.26)

Inverting these relations allows us to rewrite (3.25) as
ĥ+ = H ,

ĥ0 = −TH ,

ĥ− = T2 H +

C
,
H

(3.27)

which shows that the phase space reduction of SL(2, R)0ISO reproduces the general form of
SL(2, R)PR given in (B.11).
As discussed in appendix B, the SL(2, R)PR construction actually leads to a two-parameter
family of phase space SL(2, R)’s labeled by a choice of critical energy H̃ and Casimir C in the
definition of H− . The choice of H̃ determines the energy hypersurface that SL(2, R)PR drives
geodesics onto, whereas the ambiguity in the choice of C included in the generator H− does
not affect the scaling into the photon shell, which only(depends )on the dilations H 0 . Here, we
see that this Casimir takes the particular form C = − 1 − Λ−2 p2ϕ for SL(2, R)0ISO . In other
words, the phase space reduction of SL(2, R)0ISO recovers the SL(2, R)PR in (3.10) up to a
shift H → Ĥ = H − H̃ and the inclusion of a specific Casimir. We conclude that SL(2, R)PR is
a simple deformation of SL(2, R)0ISO within the more general family defined by (B.11).
It is well-known that the zero-temperature metric (3.19), with Killing vectors Ĥi given
in (3.20), can be mapped into the finite-temperature metric (2.1), with Killing vectors L̂i given
in (C.1), via the coordinate transformation
e2π TH t (r + 2π TH )

t→ √
,
(r + 2π TH )2 − (2π TH )2

r→

√
(r + 2π TH )2 − (2π TH )2
2π TH e2π TH t

,

ϕ → ϕ+

1
log
2

(

r
r + 4π TH

)
.

(3.28)
This transformation maps Ĥ± → −L̂∓ and Ĥ0 → −L̂0 . This demonstrates that the finitetemperature isometry group SL(2, R)ISO and the observationally relevant SL(2, R)PR given
in (3.10) are both members of the two-parameter family of phase space SL(2, R)’s defined
by (B.11). The observational SL(2, R)PR can be thought of as a particularly useful deformation of SL(2, R)ISO within this family, since it provides an organizing principle for black hole
images.
4. Quantum Ruelle resonances = classical Lyapunov exponents
We saw in section 2 that the short-wave spectrum of QNMs in the geometry (2.1),
[
]
dr 2
2
ds2 = ℓ2 −r (r + 4π TH ) dt2 +
+ Λ2 [dϕ + (r + 2π TH ) dt] ,
r (r + 4π TH )

(4.1)

is controlled by its photon shell. It is well-known that this metric has left and right temperatures
[33, 38]
TL =

1
,
2π

TR = TH .

(4.2)

An ingoing scalar mode Φ(t, r, ϕ) = e−iωt+imϕ ψ in (r) in the background (4.1) has the leading
boundary behavior (2.25)
r→∞

ψ in (r) ≈

1
i
1
Γ(2β)Γ [1 − i (ω̂ + m)]
) (1
) (4π TH ) 2 −β− 2 (ω̂+m) r− 2 +β + (β → −β) .
(1
Γ 2 + β − im Γ 2 + β − iω̂

20

(4.3)

## PDF page 22

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

Resonances occur when one of these two terms vanishes. Recalling that ω̂ = ω/(2π TH ), this
happens when
1
iω
±β −
= −n ,
2
2π TH

1
± β − im = −n .
2

or

(4.4)

The two different signs correspond to the two different bound photon orbits: the + sign is for
the inner photon shell at r = r̃− and the − sign is for the outer photon shell at r = r̃+ . The
resonances are thus
{
{
(
)
(
)
ω = −2π TH i n + 12 + β ,
ω = −2π TH i n + 21 − β ,
(
)
(
)
Inner shell:
Outer shell:
m = −i n + 12 + β ,
m = −i n + 21 − β .
(4.5)
As pointed out by [27, 33, 39], this spectrum of resonances resembles that of a CFT2 with the
same left and right temperatures (4.2) and a peculiar identification of momenta. In a finitetemperature CFT2 , a primary operator with conformal weights hL and hR has a thermal twopoint function ⟨[O(t, x), O(t ′ , x ′ )]⟩β with Fourier transform [35, 36]
) (
) (
) (
)
(
ipL
ipR
ipR
ipL
Γ hL +
Γ hR −
Γ hR +
, (4.6)
G(pL , pR ) ∼ Γ hL −
2π TL
2π TL
2π TR
2π TR
and the poles of the retarded correlator GR (pL , pR ) correspond to the poles in the lower
half-plane:
{
pL = −2π iTL (n + hL ) ,
(4.7)
pR = −2π iTR (n + hR ) .
Consider a scalar field with conformal weights hL = hR = 21 − β. If the CFT2 has the temperatures (4.2) arising from the warped metric (4.1), then its spectrum of Ruelle resonances (4.7)
becomes
{
(
)
pL = −i n + 21 − β ,
(
)
(4.8)
pR = −2π iTH n + 12 − β ,
which exactly matches the QNM spectrum associated with the outer photon shell in (4.5),
provided that we identify
(pL , pR ) = (m, ω) .

(4.9)

This is precisely the identification previously made in equation (48) of [27] and equation (2.13)
of [39].
Likewise, a scalar field with dual conformal weights hL = hR = 12 + β reproduces the QNM
spectrum associated with the inner photon shell in (4.5). The outer and inner photon shells are
therefore shadow pairs, with conformal weights related by the shadow transform. Finally, the
resonances of ψ out (r) have the opposite sign for the imaginary part and grow rather than decay.
They are associated with the poles of the advanced Green’s function, which are the poles in
the upper half plane of the Feynman propagator (4.6).
This shows that the quantum Ruelle resonances of a CFT2 can be matched to the spectrum of resonances of the warped AdS3 spacetime (4.1), including its (anti-)QNMs. Since this
spacetime’s eikonal QNM spectrum is governed by its photon shell, this strongly suggests that
its dual CFT2 encodes the photon ring and its Lyapunov exponents.
21

## PDF page 23

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

Data availability statement
No new data were created or analysed in this study.
Acknowledgments
We thank Shahar Hadar for fruitful discussions. DK gratefully acknowledges support from
the Center of Mathematical Sciences and Applications at Harvard University. The work
of AS is supported by DOE Grant de-sc/0007870. AL gratefully acknowledges Will and
Kacie Snellings for their generous support and also thanks Stéphane Detournay for useful
conversations.

Appendix A. Anti-quasinormal mode spectrum
In this appendix, we collect formulas for anti-quasinormal modes that decay exponentially in
the past. In section 2.2, we considered the resonances of the warped AdS3 metric (2.1), which
occur when the leading boundary terms of the ingoing modes (2.25) or outgoing modes (2.26)
vanish. We found that the resonant frequencies of the ‘in’ modes correspond to the QNM
spectrum (2.29). The resonant frequencies of the ‘out’ modes are of the form 12 ± β + iω̂ = −n
for some integer n ∈ N, which results in the spectrum
√(
(
)
)
1
1
1
ωmn± = ∓2π TH m
1− 2 −
+i n+
2π TH ,
m ∈ Z , n ∈ N . (A.1)
Λ
4m2
2
Since Imωmn± > 0, the associated modes decay exponentially in the past so ωmn± is the spectrum of ‘anti-QNMs.’
Section 2.3 reworked this calculation in the conformal coordinate system (2.32). The resonances of the ‘in’ modes, which make (2.43) vanish, correspond to the QNMs (2.45) with
frequencies (2.46). The ‘out’ mode resonances occur when 12 ± β + iω̂ = −n, resulting in the
spectrum (A.1) of anti-QNM frequencies. The anti-QNMs are thus
Φ̃mn± (T, x, ϕ) = e−iω̂T+imϕ−imx (sinh x)−iω̂ 2 F1

[

1
1
1
+ β + iω̂, − β + iω̂; 1 + i (ω̂ + m) ;
2
2
1 − e2x

]

,

(A.2)
(
ω̂ = ω̂mn± = ±iβ + i n +

1
2

)
.

(A.3)

In the eikonal regime |m| ≫ 1, it follows from (2.47) that the fundamental n = 0 mode takes
the approximate form
|m|≫1

1

Φ̃m0± (T, x, ϕ) ≈ e+( 2 −imΩ̂± )T+imϕ−imx (sinh x) 2
1

−imΩ̂±

.

(A.4)

From now on, we focus on the outer bound orbit at x̃ = x̃+ with angular velocity Ω̂ = Ω̂+ ,
which controls the + branch ωmn = ωmn+ of the anti-QNM spectrum. Suppressing the + subscript, we obtain
|m|≫1

1

Φ̃m0 (T, x, ϕ) ≈ e+( 2 −imΩ̂)T+imϕ−imx (sinh x) 2
1

which is the analogue of (2.49) for anti-QNMs.
22

−imΩ̂

,

(A.5)

## PDF page 24

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

Independent of the eikonal approximation, one can verify that the n = 0 fundamental antiQNM is lowest-weight and that its n > 0 overtones are SL(2, R) descendants. Indeed, the
modes
ĥ

+ĥT+imϕ−imx
ΦLW
(sinh x) ,
m0 (T, x, ϕ) = e

ĥ =

|m|≫1 1
1
+β ≈
− imΩ̂ ,
2
2

(A.6)

LW
LW0 ΦLW
m0 = imΦm0 ,

(A.7)

satisfy
LL̂− ΦLW
m0 = 0 ,

LW
LL̂0 ΦLW
m0 = −ĥΦm0 ,

and their SL(2, R) descendants obey
n
LW
ΦLW
mn = LL̂+ Φm0 ,

(
)
LW
LL̂0 ΦLW
mn = − ĥ + n Φmn .

(A.8)

These SL(2, R) towers of modes reproduce the exponentially growing anti-QNM overtones
up to normalization:
[n−1
]
∏
LW
n
Φmn = (−2)
ĥ + k − im Φ̃mn .
(A.9)
k=0

The exact value of the relative amplitude of successive overtones is
(
)
ΦLW (T, x, ϕ)
+T
ũm = m1
=
−2e
ĥ
cosh
x
−
im
sinh
x
.
ΦLW
m0 (T, x, ϕ)

(A.10)

In the eikonal limit |m| ≫ 1, we can approximate ĥ ≈ −imΩ̂ = − im
, with λ̂ = λ̂+ , simplifying
λ̂
this ratio to
(
)
(
)
(A.11)
ũm ≈ 2imΩ̂e+T cosh x + λ̂ sinh x ∼ e+T cosh x + λ̂ sinh x .
In section 2.4, we compared the exact QNMs to their near-ring approximations near the
(outer) bound orbit x ≈ x̃. We now do the same for the exact anti-QNMs. Letting δx = x − x̃
|m|≫1

and using ĥ ≈ −imΩ̂,
|m|≫1

e−imx (sinh x) = e−imx eĥ log sinh x ≈ e−imx−imΩ̂ log sinh x
ĥ

|δ x|≪1

≈ c̃0 e

+ 2i

mΩ̂
δ x2
Λ2 −1

.

(A.12)

Near the bound orbit, the exact anti-QNM wavefunctions (A.6) with large m therefore behave
(up to a constant) as
+ 2 T−imΩ̂(T− 2 kδ x )+imϕ
ΦLW
,
m0 (T, δx, ϕ) ∼ e
1

1

2

k≡

1
Λ2 − 1

.

(A.13)

In section 2.5, we used the geometric optics approximation to construct the eikonal QNMs
using null congruences of unstable critical rays. Similarly, in this approximation, the eikonal
anti-QNMs correspond to null congruences of stable critical rays, with momentum and phase
(up to an irrelevant phase shift by an integration constant C)
[
) ]
ˆ x(
1
p̂µ = ∂µ Ŝ , Ŝ = ω̂ −T + λ̂ϕ −
+ λ̂ dx ′
tanh x ′
x̃
[
]
= ω̂ −T + λ̂ϕ − λ̂x − log (sinh x) + C .
(A.14)
These geodesics asymptote to the peak of their radial potential V(x) and form congruences
with precisely the right behavior to approximate wave solutions obeying anti-QNM boundary
23

## PDF page 25

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

conditions (namely, purely outgoing at the horizon and purely ingoing at the boundary). The
expansion of these congruences is
θ = ∇2 Ŝ =

ω̂
.
ℓ2

(A.15)

The subleading equation (2.77) for the wave amplitude Ã(T, x) takes the explicit form
[(
(
)
]
)
1
λ̂
1
Ã(T, x) = 0 ,
(A.16)
+ λ̂ ∂x − 1 +
∂T −
tanh x
tanh x
2 sinh2 x
1 √
which admits a minimal solution Ã0 (T, x) = e+ 2 T sinh x that generates an infinite family of
solutions of the form
(
)
Ãn (T, x) = ũn (T, x)Ã0 (T, x) ,
ũ(T, x) = e+T cosh x + λ̂ sinh x .
(A.17)
Recalling that ω̂ = mΩ̂, the eikonal approximation to the anti-QNMs is
Φ̃mn (T, x, ϕ) ≈ Ãn (T, x)eiŜ(T,x,ϕ)
(
)n
1
1
−imΩ̂
= e+nT cosh x + λ̂ sinh x e+( 2 −imΩ̂)T+imϕ−imx (sinh x) 2
.

(A.18)

In particular, setting n = 0 in this formula results in
1

Φ̃m0 (T, x, ϕ) ≈ Ã0 (T, x)eiŜ(T,x,ϕ) = e+( 2 −imΩ̂)T+imϕ−imx (sinh x) 2
1

−imΩ̂

, (A.19)

which precisely reproduces the eikonal limit (A.5) of the fundamental anti-QNM. Likewise,
the geodesic approximation (A.18) predicts that successive overtones differ by the ratio ũ(T, x)
given in (A.17), which also matches the eikonal limit of the exact ratio given in (A.11) for antiQNMs. Note that to first order in the near-ring region
e+T δx
ũ(T,x̃ + δx) ≈ − √
,
(A.20)
Λ2 − 1
which is indeed a constant along the stable critical orbits according to (2.17)–(2.18).
On a stable critical trajectory with critical momentum p̂, the Hamiltonian functions (2.36)
in the near-ring region x = x̃ + δx take the approximate form
(
)
(A.21)
L̂− (p̂) = 0 ,
L̂+ (p̂) = 2ω̂e+T cosh x + λ̂ sinh x ∝ ũ(T, x) .
This is equivalent to the statement that the phase function Ψ0 = eiŜ is lowest-weight with
respect to SL(2, R)ISO , and we could equivalently express (A.17) as
Ãn (T, x) ∝ L̂n+ (T, x, p̂)Ã0 (T) .

(A.22)

This equation states that to generate higher-overtone amplitudes based on a critical congruence, one simply multiplies the seed amplitude by the Hamiltonian function L̂+ (x, p̂). This
is the geometric optics analogue of the exact statement that the higher-overtone anti-QNM
wavefunctions are conformal descendants
Φ̃mn ∝ LnL̂+ Φ̃m0 .

(A.23)

Appendix B. Geodesic phase space reduction and symmetries
Geodesic motion is usually defined in the extended phase space (EPS) (t, xi , pt , pi ) corresponding to spacetime rather than the reduced phase space (RPS) (xi , pi ) corresponding to space. The
24

## PDF page 26

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

RPS formulation is not covariant: it requires a splitting of spacetime into spatial slices, and
the reduced Hamiltonian H then generates time evolution with respect to the chosen coordinate time. By contrast, the EPS formulation is covariant, and the extended Hamiltonian H can
produce geodesics with any parameterization; typically, one studies the affinely parameterized
geodesics generated by
1
H(t, xi , pt , pi ) = gµν pµ pν ,
(B.1)
2
with the canonical symplectic form Ω = dpµ ∧ dxµ . A downside of this EPS system is that it
is subject to a constraint
1
H = − µ2 ,
2

(B.2)

where µ2 = −pµ pµ is the invariant mass of the particle on the geodesic. Solving this dynamical
constraint for
H(xi , pi ) = −pt

(B.3)

reproduces the Hamiltonian of the RPS formulation, with canonical symplectic form Ω̃ =
dpi ∧ dxi . This procedure—whereby a dynamical constraint is eliminated in favor of a lowerdimensional formulation—is known as phase space reduction. The reduction from EPS to RPS
at time t0 is achieved by sending (t, pt ) → (t0 , −H), such that Ω → Ω̃.
B.1. Global and local conformal symmetry of phase space

In section 3, we defined an action of the global conformal group SL(2, R)PR on the (reduced)
phase space of null geodesics in the geometry (2.33). The same construction was also carried
out for Schwarzschild and Kerr in [6]. In all these cases, the SL(2, R)PR dilations map successive subring images to one another. This construction is general and only requires the existence
of canonical coordinates (T, H, . . .) in terms of which SL(2, R)PR generators are defined as
Hn = (−T)1−n H ,

n ∈ {−1, 0, 1} .

(B.4)

Extending this definition to arbitrary n ∈ Z yields generators of a full, infinite-dimensional
Witt algebra
{Hm , Hn } = (m − n)Hm+n ,

∀m, n ∈ Z .

(B.5)

Since {T, Hn } = (−T)1−n and {H, Hn } = (1 − n)H(−T)−n , the function H n (with n ̸= 0) generates the RPS flow
c2 (c1 − s)
1/n
T(s) = − [n(c1 − s)] ,
H(s) =
,
(B.6)
T(s)
for some constants c1 and c2 . For |n| ⩾ 2, this flow becomes manifestly complex and multivalued past s = c1 due to the branch cut in the nth root. Hence, the extension to an infinitedimensional conformal symmetry is only locally (but not globally) defined, as in CFT2 . However, the SL(2, R)PR subalgebra generates globally well-defined flows:
esH+ :

T(s) = s + T(0) ,

H(s) = H(0) ,

(B.7)

esH0 :

T(s) = e−s T(0) ,

H(s) = es H(0) ,

(B.8)

esH− :

T(s) =

T(0)
,
1 − sT(0)
25

2

H(s) = H(0) [1 − sT(0)] .

(B.9)

## PDF page 27

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

A general finite SL(2, R)PR transformation acts as
T→

aT + b
,
cT + d

2

H → (cT + d) H ,

ad − bc = 1 .

(B.10)

This is a symplectomorphism since dH ∧ dT is left invariant. This is because SL(2, R)PR ∼
=
Sp(2, R): the symplectic group of canonical transformations on a two-dimensional phase
space is the global conformal group.
B.2. Ambiguity in special conformal transformations and Casimir of SL(2, R)PR

The SL(2, R)PR group generated by the functions in (B.4) has two possible ambiguities. The
first is trivial and consists of shifts in H by functions that commute with both T and H, thus
leaving the SL(2, R)PR algebra invariant. In fact, such a shift is present in the SL(2, R)PR generators (3.10) for the warped spacetime (2.33), as well as for their analogues in Schwarzschild
and Kerr [6]. These constructions involve Ĥ = H − H̃ rather than the geodesic Hamiltonian H
by itself: a shift by the critical Hamiltonian H̃ is crucial to ensure that SL(2, R)PR transformations scale arbitrary geodesics into the critical bound orbit, leaving the photon shell as the
only SL(2, R)PR -invariant phase space submanifold.
The second ambiguity is more interesting: we note that one can also shift the special conformal generator H− by a term of the form C/H+ without affecting the SL(2, R)PR commutation relations,
C
H+ = Ĥ ,
H0 = −TH+ ,
H− = T2 H+ +
,
(B.11)
H+
provided that C is a conserved quantity along geodesics that commutes with both T and H,
and therefore with all of SL(2, R)PR . In fact, we recognize this quantity C as the Casimir of
SL(2, R)PR ,
H+ H− + H− H+
.
(B.12)
2
Since we only used the dilation generator H 0 to relate successive photon subrings, the particular form of the special conformal transformation generator H− was not important to us, and
we set it to zero in (3.10), as we did in Schwarzschild and Kerr [6]. However, these spacetimes are all axisymmetric, and hence C could be any function of the angular momentum
pϕ that is conserved along null geodesics (as well as of the Carter constant in Kerr). As
we showed
in section
3, in self-dual warped AdS3 , this Casimir must take the specific form
(
)
C = − 1 − Λ−2 p2ϕ in order for this construction to recover the spacetime isometry group.
C = −H20 +

B.3. Constructing the time coordinate T

In order to define SL(2, R)PR as in (B.4), it is necessary to first construct the time coordinate T(xi , pi ) on RPS that is canonically conjugate to the Hamiltonian H, i.e. that satisfies
{T, H}RPS = 1.
In section 3, we used the canonical transformation (3.3) to reduce the geodesic equation
in the geometry (2.33) to a problem of quadratures, resulting in the integral expression (3.7)
for T(x, H, L). A more direct approach takes advantage of the EPS formulation, where the time
coordinate obeys ṫ = {t, H}EPS . Thus, one may construct a function T (xi , pt , pi ) that also keeps
track of the time elapsed along a geodesic by demanding that ṫ = {T , H}EPS , or
{T , H}EPS = ∂pt H .

(B.13)

One can then directly recover the time function T on RPS as T(x , pi ) = T (x , pt , pi )|pt =−H(xi ,pi ) .
i

26

i

## PDF page 28

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

For example, null geodesic motion in the warped AdS3 spacetime (2.1) is generated by the
EPS Hamiltonian
[
]
2
p2ϕ
1 µν
1
[pt − (r + 2π TH ) pϕ ]
2
H = g pµ pν = 2 r (r + 4π TH ) pr −
+ 2 ≡0,
(B.14)
2
2ℓ
r (r + 4π TH )
Λ
while the RPS Hamiltonian H = −pt is obtained by solving H = 0, which results in
√
p2ϕ
.
H = − (r + 2π TH ) pϕ − r (r + 4π TH ) pr2 + 2
Λ r (r + 4π TH )

(B.15)

The time function T (r, ϕ, pt , pr , pϕ ) is defined by the EPS condition (B.13), which yields
[
]
(r + 2π TH ) pt − 2π TH [2π TH pϕ − r (r + 4π TH ) pr ]
1
T =
log
− T0 ,
(B.16)
4π TH
(r + 2π TH ) pt − 2π TH [2π TH pϕ + r (r + 4π TH ) pr ]
where T0 is an arbitrary integration constant. Plugging in pt = −H(r, pr , pϕ ) yields a function
T(r, pr , pϕ ) such that {T, H}RPS = 1, as desired. It is written explicitly in (C.5) below.
In the zero-temperature limit TH → 0, the EPS and RPS Hamiltonians (B.14) and (B.15)
reduce to (3.21) and (3.23), respectively, while the EPS and RPS times (B.16) and (C.5)
become singular, with (3.24) replacing the latter.
Appendix C. SL(2, R)QN and SL(2, R)2ISO
Here, we focus on the warped AdS3 metric (2.1) written in the coordinates (t, r, ϕ) that make
the dependence on the black hole temperature T H explicit. This geometry admits an isometry
group SL(2, R)ISO generated by vectors
[
√
1
r + 2π TH
±2π TH t
√
L̂0 = −
∂t , L̂± = e
−
∂t ± r (r + 4π TH )∂r
2π TH
2π TH r (r + 4π TH )
]
2π TH
+√
∂ϕ ,
(C.1)
r (r + 4π TH )
which are of course equivalent to (2.34) under the coordinate transformation (2.32). These
Killing vector fields define functions L̂n = −L̂µn pµ that generate the action of SL(2, R)ISO
on the six-dimensional phase space (t, r, ϕ, pt , pr , pϕ ) with canonical symplectic form. Null
geodesic motion in that phase space is generated by the constrained Hamiltonian (B.14), and
the fact that the vector fields L̂µn ∂µ are Killing ensures that the functions L̂n are conserved along
geodesics:
{
}
L̂n , H = 0 ,
∀n ∈ {−1, 0, 1} .
(C.2)
We note however that these conserved charges do not commute with each other, as they obey
the SL(2, R)ISO algebra. The Casimir of this SL(2, R)ISO is
(
)
1
L̂+ L̂− + L̂− L̂+
2
= − 1 − 2 p2ϕ .
C = −L̂0 +
(C.3)
2
Λ
In the four-dimensional phase space (r, ϕ, pr , pϕ ), null geodesic motion is generated by the
Hamiltonian H = −pt given in (B.15). Its canonically conjugate variable with respect to the
27

## PDF page 29

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

(four-dimensional) canonical symplectic form is the coordinate time T(r, ϕ, pr , pϕ ) elapsed
along geodesic flow,
{T, H} = 1 ,

(C.4)

and, as explained below (B.16), it is given (up to an integration constant T0 ) by
[
]
(r + 2π TH ) H + 2π TH [2π TH pϕ − r (r + 4π TH ) pr ]
1
log
− T0 .
T=
4π TH
(r + 2π TH ) H + 2π TH [2π TH pϕ + r (r + 4π TH ) pr ]

(C.5)

Under phase space reduction at time t = t0 , the functions L̂n = −L̂µn pµ defined from (C.1)
reduce to
√
r (r + 4π TH )
H
±2π TH t0
ℓ̂0 = −
,
ℓ̂± = e
2π TH
2π TH
⎤
⎡
√
p2ϕ
∓ 2π TH pr ⎦ , (C.6)
× ⎣pϕ + (r + 2π TH ) pr2 + 2
Λ r (r + 4π TH )
where t0 is just a constant and the factors of e±2π TH t0 could be removed by a dilation ℓ̂± →
λ±1 ℓ̂± with λ = e−2π TH t0 , which leaves the SL(2, R) algebra invariant (as SL(2, R) is its
own automorphism group). We note that the functions ℓ̂± are no longer conserved in fourdimensional phase space, since they do not commute with the Hamiltonian H and therefore
change the energy (or photon color) of a null geodesic. We also note that after setting T0 = t0 ,
( )
(
)
ℓ̂−
ℓ̂+ ℓ̂− + ℓ̂− ℓ̂+
1
1
2
log
,
C ≡ −ℓ̂0 +
= − 1 − 2 p2ϕ .
T=
(C.7)
4π TH
2
Λ
ℓ̂+
Inverting these relations allows us to rewrite (C.6) as
√
H
ℓ̂0 = −
,
ℓ̂± = e∓2π TH T ℓ̂20 + C ,
2π TH

(

1
C = − 1− 2
Λ

)
p2ϕ , (C.8)

which makes it clear that the ℓ̂± vanish when and only when they are evaluated on the critical
bound orbit pϕ = λ̃H, with λ̃ given in (2.9). In this form, the fact that these functions obey the
SL(2, R)ISO commutation relations follows immediately from the commutation relation (C.4).
To compare this SL(2, R)ISO with the SL(2, R)QN introduced in (2.62), we must return to
coordinates (2.32), which results in7
√
p2ϕ
pϕ
ℓ̂0 = −H =
+ p2x +
,
tanh x
Λ2 sinh2 x
√
ℓ̂± = e∓T H 2 + C = −H cosh x − (pϕ ∓ px ) sinh x .
(C.9)
The phase space coordinates are now (x, ϕ, px , pϕ ). To scale into the near-ring region, we
change coordinates to
x = x̃ + ϵδx ,

px = ϵP ,

(C.10)

which is a canonical transformation provided that we set the dummy parameter ε to unity after
expanding near the ring in small ε. We thus find that to leading order near the ring,

7 If not for the presence of a nonzero Casimir C, we would have ℓ̂ = e±T H and these functions would be Susskind±
Glogower operators.

28

## PDF page 30

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

√
ℓ̂± ≈ Λ2 − 1 (±P + kHδx) ,
(C.11)
( 2
)−1
where k = Λ − 1
as defined in (2.57). To make contact with the radial wave equation
from section 2.4, we quantize these operators by letting P = −i∂δx , in which case they act as
√
ℓ̂± ≈ i Λ2 − 1 (∓∂δx − ikHδx) ∝ a± ,
(C.12)
provided that we identify the energy as H = ω̂R . Since the generators L± of SL(2, R)QN are
obtained by squaring the near-ring generators a± , we conclude that SL(2, R)QN is related to the
square of the near-ring isometry group SL(2, R)ISO . This conclusion is consistent with (2.71).
ORCID iDs
Daniel Kapec  https://orcid.org/0000-0001-5615-4541
Alexandru Lupsasca  https://orcid.org/0000-0002-1559-6965
Andrew Strominger  https://orcid.org/0000-0002-1332-4122
References
[1] Johnson M D et al 2020 Universal interferometric signatures of a black hole’s photon ring Sci. Adv.
6 eaaz1310
[2] LIGO Scientific Collaboration and Virgo Collaboration 2016 Observation of gravitational waves
from a binary black hole merger Phys. Rev. Lett. 116 061102
[3] Berti E, Cardoso V and Starinets A O 2009 TOPICAL REVIEW: Quasinormal modes of black
holes and black branes Class. Quantum Grav. 26 163001
[4] Polchinski J 2015 Chaos in the black hole S-matrix (arXiv:1505.08108 [hep-th])
[5] Yang H, Nichols D A, Zhang F, Zimmerman A, Zhang Z and Chen Y 2012 Quasinormal-mode
spectrum of Kerr black holes and its geometric interpretation Phys. Rev. D 86 104006
[6] Hadar S, Kapec D, Lupsasca A and Strominger A 2022 Holography of the photon ring Class.
Quantum Grav. 39 215001
[7] Bardeen J M, Press W H and Teukolsky S A 1972 Rotating black holes: locally nonrotating frames,
energy extraction and scalar synchrotron radiation Astrophys. J. 178 347–70
[8] Kapec D and Lupsasca A 2020 Particle motion near high-spin black holes Class. Quantum Grav.
37 015006
[9] Bardeen J and Horowitz G T 1999 Extreme Kerr throat geometry: a vacuum analog of AdS2 × S2
Phys. Rev. D 60 104030
[10] Hod S 2008 Slow relaxation of rapidly rotating black holes Phys. Rev. D 78 084035
[11] Casals M and Longo Micchi L F 2019 Spectroscopy of extremal and near-extremal Kerr black holes
Phys. Rev. D 99 084047
[12] Israël D, Kounnas C, Orlando D and Marios Petropoulos P 2005 Electric/magnetic deformations
of S3 and AdS3 and geometric cosets Fortschr. Phys. 53 73–104
[13] Detournay S, Israël D, Lapan J M and Romo M 2011 String theory on warped AdS3 and Virasoro
resonances J. High Energy Phys. JHEP01(2011)030
[14] Azeyanagi T, Hofman D M, Song W and Strominger A 2013 The spectrum of strings on warped
AdS3 × S3 J. High Energy Phys. JHEP04(2013)078
[15] Hofman D M and Strominger A 2011 Chiral scale and conformal invariance in 2D quantum field
theory Phys. Rev. Lett. 107 161601
[16] Detournay S, Hartman T and Hofman D M 2012 Warped conformal field theory Phys. Rev. D
86 124018
[17] Bzowski A and Guica M 2019 The holographic interpretation of JT̄-deformed CFTs J. High Energy
Phys. JHEP01(2019)198
[18] Guica M 2018 An integrable Lorentz-breaking deformation of two-dimensional CFTs SciPost Phys.
5 048
[19] Chakraborty S, Giveon A and Kutasov D 2018 JT̄ deformed CFT2 and string theory J. High Energy
Phys. JHEP10(2018)057
29

## PDF page 31

Class. Quantum Grav. 40 (2023) 095006

D Kapec et al

[20] Apolo L and Song W 2018 Strings on warped AdS3 via TJ̄ deformations J. High Energy Phys.
JHEP10(2018)165
[21] Chakraborty S, Giveon A and Kutasov D 2019 TT̄, JT̄, TJ̄ and string theory J. Phys. A: Math. Theor.
52 384003
[22] Apolo L and Song W 2020 Heating up holography for single-trace JT̄ deformations J. High Energy
Phys. JHEP01(2020)141
[23] Guica M 2022 A definition of primary operators in JT̄-deformed CFTs SciPost Phys. 13 045
[24] Song W, Anninos D, Li W, Padi M and Strominger A 2009 Warped AdS3 black holes J. High Energy
Phys. JHEP03(2009)130
[25] Chen B and Xu Z-b 2009 Quasi-normal modes of warped black holes and warped AdS/CFT correspondence J. High Energy Phys. JHEP11(2009)091
[26] Chen B, Ning B and Xu Z-B 2010 Real-time correlators in warped AdS/CFT correspondence J.
High Energy Phys. JHEP02(2010)031
[27] Chen B and Ning B 2010 Self-dual warped AdS3 black holes Phys. Rev. D 82 124027
[28] Chen B and Long J 2010 Hidden conformal symmetry and quasinormal modes Phys. Rev. D
82 126013
[29] Song W and Strominger A 2012 Warped AdS3 /dipole-CFT duality J. High Energy Phys.
JHEP05(2012)120
[30] Auzzi R, Baiguera S, Grassi M, Nardelli G and Zenoni N 2018 Complexity and action for warped
AdS black holes J. High Energy Phys. JHEP09(2018)013
[31] Moussa K A, Clément G and Leygnac C 2003 The black holes of topologically massive gravity
Class. Quantum Grav. 20 L277–83
[32] Bouchareb A and Clément G 2007 Black hole mass and angular momentum in topologically
massive gravity Class. Quantum Grav. 24 5581–94
[33] Bredberg I, Hartman T, Song W and Strominger A 2010 Black hole superradiance from Kerr/CFT
J. High Energy Phys. JHEP04(2010)019
[34] Chen B and Stein L C 2017 Separating metric perturbations in near-horizon extremal Kerr spacetimes Phys. Rev. D 96 064017
[35] Birmingham D, Sachs I and Solodukhin S N 2002 Conformal field theory interpretation of black
hole quasinormal modes Phys. Rev. Lett. 88 151301
[36] Birmingham D, Sachs I and Solodukhin S N 2003 Relaxation in conformal field theory, HawkingPage transition and quasinormal or normal modes Phys. Rev. D 67 104026
[37] Song W and Xu J 2018 Correlation functions of warped CFT J. High Energy Phys.
JHEP04(2018)067
[38] Guica M, Hartman T, Song W and Strominger A 2009 The Kerr/CFT correspondence Phys. Rev. D
80 124008
[39] Li R and Ren J-R 2011 Quasinormal modes of self-dual warped AdS3 black hole in topological
massive gravity Phys. Rev. D 83 064024

30
