Source: see manifest row of the PDF
PDF sha256: 8a91c1c966342f3381bd0d54dd7f5729e55e91552c7de0ad0dad4a42d05e5420
License: CC-BY-4.0
Language: eng
Fidelity: machine (failed: second-reader)

# Transcription of pedersen_2022_stark_localization_as_a_probe_of_nanostructure_geometry.pdf

Transcription of `pedersen_2022_stark_localization_as_a_probe_of_nanostructure_geometry.pdf` in this directory, 10 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 2 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories; pages 1, 3-10 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

You may also like

PAPER • OPEN ACCESS

Stark-localization as a probe of nanostructure
geometry
To cite this article: T G Pedersen et al 2022 New J. Phys. 24 093005

- Exhaled breath condensate in acute
pulmonary embolism; a porcine study of
effect of condensing temperature and
feasibility of protein analysis by mass
spectrometry
Inger Lise Gade, Jacob Gammelgaard
Schultz, Lasse Jørgensen Cehofski et al.
- The 24th Nordic Semiconductor Meeting
Haraldur Páll Gunnlaugsson, Arne
Nylandsted Larsen and Christian
Uhrenfeldt

View the article online for updates and enhancements.

- Water Balance Simulations of a PEMFC
Using a Multifluid Model
Torsten Berning, Madeleine Odgaard and
Soren Kær

This content was downloaded from IP address 71.84.237.76 on 29/07/2023 at 07:05

## PDF page 2

https://doi.org/10.1088/1367-2630/ac8b29
New J. Phys. 24 (2022) 093005
IOP Publishing
Published in partnership
<b>New Journal of Physics</b>
Deutsche Physikalische Gesellschaft DPG
with: Deutsche Physikalische
IOP Institute of Physics
Gesellschaft and the Institute
The open access journal at the forefront of physics
of Physics
<b>PAPER</b>
CrossMark
Stark-localization as a probe of nanostructure geometry
<b>OPEN ACCESS</b>
T G Pedersen<sup>1,*</sup>, H D Cornean<sup>2</sup>, D Krejčiřik<sup>3</sup>, N Raymond<sup>4</sup> and E Stockmeyer<sup>5</sup>
RECEIVED
Department of Materials and Production, Aalborg University, DK-9220 Aalborg Øst, Denmark
3 May 2022
Department of Mathematical Sciences, Aalborg University, DK-9220 Aalborg Øst, Denmark
REVISED
Department of Mathematics, Faculty of Nuclear Sciences and Physical Engineering, Czech Technical University in Prague, Trojanova
3 August 2022
13, 12000 Prague 2, Czech Republic
ACCEPTED FOR PUBLICATION
4
Laboratoire Angevin de Recherche en Mathématiques, LAREMA, UMR6093, UNIV Angers, SFR Math-STIC, 2 boulevard Lavoisier
19 August 2022
49045 Angers Cedex 01, France
PUBLISHED
Instituto de Física, Pontificia Universidad Católica de Chile, Vicuña Mackenna 4860, Santiago 7820436, Chile
5
29 September 2022
Author to whom any correspondence should be addressed.
E-mail: tgp@mp.aau.dk
Original content from
this work may be used
Keywords: nanostructures, Stark, spectroscopy
under the terms of the
Creative Commons
Attribution 4.0 licence.
Any further distribution
<b>Abstract</b>
of this work must
It is a central tenet of quantum mechanics that spatial resolution is limited by the wave nature of
maintain attribution to
the author(s) and the
particles. Energies of stationary states reflect delocalized wave functions and cannot be ascribed to
title of the work, journal
any single point. Yet, electrons confined in nanostructures become localized against the boundary
citation and DOI.
by strong electric fields. Energies then reflect the local curvature of the nanostructure surface
n
rather than entire volume. We propose using spectroscopy of Stark-localized states to map
nanostructure surface curvature. By varying field direction, local curvatures are extracted from
absorption spectra. Moreover, the required field strength is shown to be feasible experimentally.
We use nanowires with elliptic cross section as a detailed benchmark providing quantitative error
estimates and practical guide lines.
1. Introduction
Optical spectroscopy is among the most useful techniques for characterization of nanostructures <math>[1-3]</math>.
Both energy levels and symmetry properties are revealed by various optical probes. Nanostructures
suspended in vacuum or air are characterized by tall barriers confining electrons to their interior [1–5]. In
turn, electrons and holes in the interior behave essentially as free particles except that their apparent mass is
the effective one. As a consequence, electron and hole eigenstates are solutions of the Helmholtz equation.
Their eigenvalues are, therefore, properties of the entire surface bounding the nanoparticle. Kac famously
asked 'can you hear the shape of a drum?' in relation to the equivalent problem of a vibrating membrane
[6]. The answer turned out to be 'no' since knowing all eigenvalues is not enough to uniquely determine
shape. Knowing only part of the spectrum leads to even greater shape uncertainty. The question we ask in
the present work is whether or not optical spectroscopy can determine nanostructure surface geometries. As
with the vibrating drum, the answer is clearly 'no' if only surfaces restrict eigenstates. Electrons, however,
differ from drums by being highly sensitive to strong electric fields. In the present work, we propose using
the Stark effect in strong electric fields to facilitate local probes of the nanostructure geometry. Thus, a
sufficiently strong Stark field will push electrons and holes against the barrier and, in turn, a weak infrared
field probing transitions between Stark-localized states will reveal the local surface curvature. By varying the
direction of the Stark field, a full mapping of the curvature is possible.
The envisioned experimental setup is sketched in figure 1. We focus on translationally invariant
nanowires in a transverse Stark field, cf figure 1(a). In addition, a weak optical probe field is present. The
polarization of the probe field must have a component perpendicular to both Stark field and nanowire
long-axis in order to probe transitions between confined states as shown in figure 1(b). Note that this setup
would apply equally well to two-dimensional islands and patches such as graphene nanodisks [7] subject to
in-plane fields. A strong Stark field will pull electrons and push holes against the barrier, respectively. The
stronger the field, the more tightly confined the carriers. Eventually, states cease to be delocalized over the
© 2022 The Author(s). Published by IOP Publishing Ltd on behalf of the Institute of Physics and Deutsche Physikalische Gesellschaft

## PDF page 3

New J. Phys. 24 (2022) 093005

T G Pedersen et al

Figure 1. (a) Schematic setup showing a nanowire in a strong Stark ﬁeld and weak infrared probe ﬁeld. (b) The Stark ﬁeld
pushes carriers against the boundary, such that resonant absorption of a perpendicular probe ﬁeld becomes sensitive to local
radius of curvature R. Electrons (blue) and holes (red) Stark-localize on opposite sides.

entire cross section but, instead, ﬁnd themselves conﬁned by the ﬁeld and the barrier at the point of
maximal Stark effect on the nanowire boundary, as sketched in ﬁgure 1(b). Electrons and holes are, thus,
Stark-localized near points on the boundary with maximum displacement in the negative and positive ﬁeld
direction, respectively. Importantly, conﬁnement in the in-plane direction perpendicular to the Stark ﬁeld is
governed by the local curvature. Thus, a small radius of curvature translates into tight conﬁnement in the
perpendicular dimension, see ﬁgure 1(b). The ﬁnal ingredient in our proposal is the probe ﬁeld inducing
transitions between Stark-localized states. As is intuitively clear, such transitions will be highly sensitive to
the local curvature. In fact, as recently demonstrated [8], the system behaves mathematically as a harmonic
oscillator with characteristic frequency determined by the curvature radius R. By scanning the Stark ﬁeld
direction (or rotating the nanowire), the local curvature along the boundary may ﬁnally be mapped.
Our proposal is quite generic but, still, has obvious limitations. Primarily, only convex boundaries can
be mapped in entirety. Any locally concave points, i.e. points intersected by lines joining other boundary
points, cannot be probed because such points never support Stark-localized states. More subtly, our
proposal rests on the assumption that barriers between nanowire and surroundings are sufﬁciently tall that
carriers remain conﬁned even in large Stark ﬁelds, that is, barriers effectively acting as hard walls. Hence,
our proposal applies to free-standing nanowires with a substantial barrier between interior and exterior, as
opposed to heterostructures with barriers formed by varying atomic composition. High quality
free-standing nanowires have been demonstrated in a wide range of materials, see e.g. [9–11]. Below, the
inﬁnite-barrier approximation will be critically examined. As a realistic benchmark, we consider nanowires
with an elliptic cross section. From simulated probe absorption spectra in strong Stark ﬁelds in this
geometry, we demonstrate that our proposal is, indeed, feasible. We consequently expect that spectroscopic
studies of Stark-localized electronic states will pave the way for a novel toolbox of signiﬁcance for
nanostructure characterization.

2. Stark-localization
We now introduce the model applied to describe Stark-localization on the boundary of a two-dimensional
domain. The Stark ﬁeld ⃗F can take arbitrary orientations within the plane of the domain. For deﬁniteness,
we consider electrons but all considerations apply equally to holes. We assume carriers are introduced via
doping in contrast to interband photo-excitation, which produces electron–hole pairs. Consequently,
electron–hole interactions are not considered. Moreover, we assume that the semiconductor is characterized
by an isotropic effective mass m∗ in the cross-sectional plane (x, y). In a translationally invariant nanowire,
states are of the form ϕ(x, y)eikz with an in-plane part ϕ(x, y) determined by
}
{
ℏ2 2
⃗
(1)
− ∗ ∇ + eF ·⃗r ϕ(⃗r ) = Eϕ(⃗r ).
2m
This equation is supplemented by Dirichlet boundary conditions ϕ(⃗r ) = 0 on the boundary ∂Ω of the
domain, i.e. nanowire cross section. Formally, Dirichlet boundary conditions correspond to an inﬁnite
barrier between interior and exterior. Physically, this barrier is the electron afﬁnity of the semiconductor
material surrounded by vacuum. As an example, this barrier V is about 4 eV in GaAs and similar inorganic
semiconductors [12]. If the characteristic dimension (‘diameter’) of the cross section is L, it follows that
2

## PDF page 4

New J. Phys. 24 (2022) 093005

T G Pedersen et al

Dirichlet boundary conditions apply approximately if eFL ≪ V. This places an upper limit on the
acceptable ﬁeld strength. A second concern is the dielectric breakdown limit reached by sufﬁciently high
ﬁelds. Both of these restrictions are analyzed in more detail below.
In any inversion-symmetric geometry, the lowest ﬁeld-dependent correction to the energy is quadratic.
→
In terms of the nanostructure polarizability tensor ←
α , see references [13–20], we have
←
→
1
4
E(⃗F ) = E(0) − 2 ⃗F · α · ⃗F + O(F ). The in-plane nanowire polarizability takes a diagonal form
←
→
α = diag(αxx , αyy ) in the principal-axis system, with axes coinciding with mirror lines in symmetric cases
→
such as ellipses. In general, some geometric information is contained in ←
α . Thus, a tightly conﬁned
principal direction implies a reduced polarizability element. Similarly, highly symmetric cross sections such
as circles [21], hexagons and squares [22] lead to isotropic polarizability tensors. It follows that
angle-resolved low-ﬁeld Stark spectroscopy provides useful geometric information about symmetries and
nanowire aspect ratio. However, it is clear that only limited detail may be extracted from a single pair of
numbers (αxx , αyy ). If more elaborate geometry mapping is desired in Stark spectroscopy, strong ﬁelds
beyond the quadratic regime are inevitable. Such intense ﬁelds drive electrons into regions, where the dipole
energy e⃗F ·⃗r is minimum. We denote the location on the boundary corresponding to the minimum by ⃗r min .
In the extreme high-ﬁeld limit, we have previously shown [8] that the low lying energies satisfy
( 2 2 2 )1/3 ( 2
)1/2
ℏ eFκ
ℏeF
1
+
(ν − ) + O(F 1/3 ),
E(⃗F ) = e⃗F ·⃗r min − z1
2m∗
m∗
2

(2)

where z1 = 2.338 107 410 46 . . . is the ﬁrst zero of the Airy function Ai(−z) and ν is a positive integer.
Crucially, κ = R−1 in this expression is the local curvature at ⃗r min . Physically, the curvature term follows
from a harmonic oscillator describing motion along the boundary in the vicinity of ⃗r min . The potential
energy cost associated with displacement from ⃗r = ⃗r min increases with both ﬁeld strength and curvature. It
follows that a convex boundary forces electrons to move against the electric force as they oscillate about
⃗rmin . As seen from equation (2), the harmonic oscillator frequency ω0 = (eFκ/m∗ )1/2 increases as the
square-root (Fκ)1/2 of the product of ﬁeld and curvature. A weak optical probe with a frequency ω will be
resonantly absorbed if ω ≈ ω 0 such that an absorption spectrum provides direct access to the curvature κ.
We stress the crucial point that ω 0 depends only on curvature implying that geometry can be determined in
a model-independent way in the high-ﬁeld regime.

3. Elliptical nanowires
As already mentioned, we will use nanowires with elliptical cross section, such as the one in the inset of
ﬁgure 2, as a detailed benchmark and proof of concept. Elliptic boundaries are convenient because they are
convex, smooth and easily adjustable through their major and minor axes a and b corresponding to an
aspect ratio η = a/b. The electric ﬁeld ⃗F is at an angle θ to the major axis. We simulate the strong-ﬁeld
Stark response numerically by transforming to a circular domain through the scaling x → x/a and y → y/b.
In this manner, the conﬁnement is circular at the expense of an anisotropic Laplacian, and we have
}
{
ℏ2 d2
ℏ2 d2
+ eaFx x + ebFy y ϕ(⃗r ) = Eϕ(⃗r ),
− ∗ 2 2 −
2m a dx
2m∗ b2 dy2

∂Ω : x2 + y2 = 1.

(3)

A convenient dimensionless form is found if we introduce E0 ≡ ℏ2 /(m∗ b2 ) as well as ε = E/E0 and
⃗E = eb⃗F/E0 . Hence, as a result,
}
{
1 d2
1 d2
+ ηEx x + Ey y ϕ(⃗r ) = εϕ(⃗r ).
− 2 2−
2η dx
2 dy2

(4)

Furthermore, in terms of the normalized energy ε = ε(η, Ex , Ey ), an exact scaling relation
ε(η −1 , η 3 Ey , η 3 Ex ) = η 2 ε(η, Ex , Ey ) is readily established. This relation can be viewed as the result of a
rotation by 90 degrees. The exact ﬁeld-free solutions of equations (3) and (4) are known in terms of
Mathieu functions and their characteristics [23, 24]. Since these cannot be expressed in terms of standard
functions, such exact solutions are of limited use for the present purposes. As an alternative, one may
consider ellipses that only deviate slightly from circles. Thus, for the normalized ground state energy ε(0) (η),
in the limit of low ellipticity [25, 26],
ε(0) (η) =

λ2
λ2 (6 + λ2 )
λ2
− (η − 1) +
(η − 1)2 + O[(η − 1)3 ].
2
2
16

3

(5)

## PDF page 5

New J. Phys. 24 (2022) 093005

T G Pedersen et al

Figure 2. Comparison of numerical (solid lines) and perturbative (dashed lines) Cartesian polarizabilities for an ellipse. Inset:
cross section of an ellipse with major and minor axes a and b in an electric ﬁeld.

Here, λ ≡ λ01 ≈ 2.404 83 is the ﬁrst zero of the 0th Bessel function. Such expansions are useful in the
low-ﬁeld Stark regime, as we demonstrate below. In strong ﬁelds, however, eigenstates deviate substantially
from unperturbed ones, even for nearly circular domains. Accordingly, an accurate numerical approach
based on expansion of Stark-localized eigenstates in a large basis is used throughout. In the appendix, we
describe the basis and matrix elements applied to ﬁnd eigenstates for arbitrary ﬁelds. Brieﬂy, eigenstates of
an isotropic circular cylinder are selected as a numerical basis. These states are labeled by angular
momentum l and radial quantum number n. In all simulations, l and n are restricted to the ranges
−30 ⩽ l ⩽ 30 and 1 ⩽ n ⩽ 30, respectively. Hence, the ground state energy λ2 /2 of a circular nanowire
with η = 1 is reproduced exactly in this basis. The ground state is a special case of the general eigenvalue
2
ε(0)
nl = λln /2, where λln is the nth zero the lth Bessel function, contained in this basis.
Before investigating the strong-ﬁeld Stark regime, we brieﬂy discuss the more common weak-ﬁeld case.
This is the regime, in which the electric ﬁeld may be seen as a weak perturbation, shifting each energy level
by a small amount compared to the characteristic spacing between unperturbed levels. In an
inversion-symmetric geometry, the shift is quadratic in the ﬁeld and we ﬁnd for the ground state
1
1
ε(η, Ex , Ey ) = ε(0) (η) − αxx (η)Ex2 − αyy (η)Ey2 + O(E 4 ).
2
2

(6)

The exact scaling relation implies that αxx (η) = η 4 αyy (η −1 ) and αyy (η) = η 4 αxx (η−1 ). In the case of a
perfect circle, it is known [21] that αxx (1) = αyy (1) = (4 + λ2 )/(6λ4 ) ≡ α0 . A tedious perturbation
expansion leads to the results
αxx (η) = α0 + (η − 1)α1 + (η − 1)2 α2 + O[(η − 1)3 ],
αyy (η) = α0 + (η − 1)(4α0 − α1 ) + (η − 1)2 (6α0 − 3α1 + α2 ) + O[(η − 1)3 ].

(7)

Here,
α1 =

1 16 + λ2
+
≈ 3.6772α0 ,
8
12λ4

α2 =

5
7
1
1
−
≈ 4.7004α0 .
+ 4+
24 24λ2
λ
8(λ2 − 8)

(8)

The numerical magnitude of these corrections shows that, in fact, the polarizabilities are sensitive probes
of the global geometry. The comparison in ﬁgure 2 demonstrates that the perturbative results equation (7)
hold to good accuracy in the range 0.75 < η < 1.25. Even in this restricted range, a signiﬁcant variation in
polarizability is observed. In particular, the results show that the major-axis component αxx (η) is doubled
compared to the case of a circle αxx (1) if the aspect ratio is increased to η ≈ 1.21. Hence, slight geometric
deformations lead to substantial changes in the Stark shift. Also, it is apparent that the ratio αxx (η)/αyy (η) is
a sensitive measure of aspect ratio, obviating absolute measurement of dimensions.
Next, we turn to the strong-ﬁeld regime in order to validate the expansion equation (2). Speciﬁcally, we
wish to determine the ﬁeld strength required for the harmonic oscillator term to describe the ground state
and lowest excitations with acceptable accuracy. Similarly to the normalization applied above, we introduce
4

## PDF page 6

New J. Phys. 24 (2022) 093005

T G Pedersen et al

Figure 3. Energy shift Δε for the four lowest levels in horizontal (top) and vertical (bottom) Stark ﬁelds. Solid curves are
numerical diagonalization results while circles are analytical harmonic oscillator predictions. The ellipse aspect ratio is η = 1.5.

a normalized curvature κ̃ = bκ. Thus, in terms of normalized quantities, the strong-ﬁeld expansion takes
on a particularly simple form
(
)1/3
(
)
1 2
1
ε(⃗E ) = ⃗E ·⃗r min /b − z1
E
+ (κ̃E)1/2 n −
+ O(E 1/3 ).
2
2

(9)

The curvature κ = R−1 of an ellipse is (a2 cos2 θ + b2 sin2 θ)3/2 /(ab)2 so that, conveniently,
κ̃ = (η 2 cos2 θ + sin2 θ)3/2 /η 2 . We ﬁrst compare the numerical solutions to equation (4) with the expansion
equation (9). To this end, we apply the Bessel basis as described above and consider the Stark shift
Δε ≡ ε(⃗E ) − ε(0) − ⃗E ·⃗r min /b + z1 ( 12 E 2 )1/3 . Here, the two universal terms in equation (9) were subtracted
so that the dominant part of Δε is the harmonic oscillator term varying as the square-root of the ﬁeld
strength. The prefactor κ̃ means, however, that the magnitude of this term depends on orientation of the
ﬁeld. Generally, low-curvature directions require larger ﬁelds in order to fully dominate subleading terms.
For the ellipse, a ratio of η 3 is found between horizontal and vertical prefactors κ̃.
For numerical benchmarking, we select an ellipse with an aspect ratio of η = 1.5. Accordingly, a simple
expectation for the critical ﬁelds required to enter the strong-ﬁeld regime would be that vertical ﬁelds
exceed horizontal ones by a factor 1.53 ≈ 3.4. In ﬁgure 3, we compare the analytical harmonic oscillator
expression (κ̃E)1/2 (ν − 12 ) to numerical values of Δε in strong ﬁelds. It is immediately clear that the
numerical high-ﬁeld behavior follows a square-root dependence to good accuracy. However, examining the
curves more carefully, we ﬁnd discrepancies that depend on ﬁeld strength and orientation. In relatively weak
ﬁelds, the harmonic oscillator result overestimates the actual eigenvalues. In the case of a horizontal ﬁeld
shown in the top panel of ﬁgure 3, a normalized ﬁeld of about E = 1000 is required to limit deviations to
approximately 3% for the energy difference between the two lowest states. In the vertical case, shown in the
bottom panel, the ﬁeld must be signiﬁcantly larger in agreement with the curvature-based arguments above.
It must be noted, however, that our proposal rests on the accuracy of energy differences probed by
absorption spectroscopy. Thus, systematic errors common to all levels are of no consequence. Below, the
error associated with transition energies is estimated.
As mentioned in the introduction, the assumption of Dirichlet boundary conditions corresponding to
inﬁnite barriers is only valid if F ≪ V/(eL), where V is the actual surface barrier. In terms of the
normalized ﬁeld and taking L = b, this requirement is conveniently expressed as
E≪
5

b2
m∗
V
× 2×
,
Ha a0
m0

(10)

## PDF page 7

New J. Phys. 24 (2022) 093005

T G Pedersen et al

where Ha ≈ 27.21 eV is the Hartree energy, a0 is the Bohr radius, and m0 is the free electron mass. The
conduction band in GaAs can be seen as an extreme case due to the exceedingly small effective mass [1–3]
m∗ ≈ 0.067m0 . Thus, with V = 4 eV, a ﬁeld of E = 1000 translates into a requirement b ≫ 17 nm. Hence,
for nanowires in the 10 nm range, such ﬁelds will lead to inaccuracies since the ﬁnite conﬁnement barrier
can no longer be ignored. In most materials, however, the effective mass is larger leading to relaxed
restrictions. For a 40 nm radius GaAs nanowire, the characteristic conﬁnement energy is
E0 = ℏ2 /(m∗ b2 ) ≈ 0.7 meV. This means that the GaAs dielectric breakdown limit [27] around 30 MV m−1
is reached with a normalized ﬁeld of approximately E = 1700, placing a strict upper limit on the applicable
ﬁeld. We stress that the Stark ﬁeld is static in our setup, thereby suppressing photoemission across the
surface barrier, which is known to occur in intense time-dependent (pulsed) ﬁelds [28].
Throughout, we have ignored Coulomb interactions between the conduction electrons. At a sufﬁciently
high density, this simpliﬁcation will be invalid. To quantify this restriction, we consider a nanowire with a
ﬁnite electron density ρ per unit length and require ρaHO ≪ 1, where aHO = ℏ1/2 /(m∗ eFκ)1/4 is the
characteristic conﬁnement length of the harmonic oscillator, as derived from equation (2), and ρ−1 is a
measure of the average electron–electron separation. This requirement ensures that many-body effects are
negligible compared to differences between Stark shifts and translates into a lower bound for the Stark ﬁeld
FL = ℏ2 ρ4 /(m∗ eκ). Similarly to the analysis above, we again consider a GaAs nanowire with radius
b = 40 nm. Thus, taking κ = b−1 as well as ρ = b−1 , corresponding to electrons separated approximately by
the nanowire radius, we ﬁnd a rather small lower bound of FL ≈ 18 kV m−1 . We note that GaAs is an
extreme case due to its diminutive effective mass. However, the ρ4 scaling means that, eventually, Coulomb
corrections will be of importance for more highly doped materials, even if the bound is reduced by a larger
effective mass.

4. Stark spectroscopy
A weak probe ﬁeld of the form Fω cos ωt will induce transitions between Stark-localized states. This will
manifest itself as scattering or absorption of the probe beam. From an analysis of scattering or absorption
resonances, transition energies Eνμ = Eν − Eμ may be inferred. For the ideal harmonic oscillator, only
ν = μ ± 1 transitions are allowed and ω = ω0 the only resonance observed. We expect this simple picture
to emerge in strong ﬁelds, while a much more intricate spectral response is expected in weak ﬁelds.
Absorption of the probe ﬁeld is described by the imaginary part of the frequency-dependent polarizability
α(ω), while scattering is governed by the absolute value. If the probe ﬁeld is polarized at 45 degrees to a
principal axis, transitions along both axes are probed. In this case, the polarizability of an electron in the
ground state |1⟩ is [19]
∑ |⟨1|x|ν⟩|2 + |⟨1|y|ν⟩|2
α(ω) = e2 Eν1
.
(11)
2 − ℏ2 ω 2
Eν1
ν
The dipole matrix elements ⟨1|⃗r |ν⟩ are readily expanded in the Bessel basis using equation (A4). The
response equation (11) only captures absorption by dopant electrons. Realistically, a bulk contribution,
both electronic and vibrational, should be added. Hence, transitions between Stark-localized states will
appear on top of a background signal.
We envision rotating the nanowire in the Stark ﬁeld while recording the probe absorption spectrum.
The lowest resonance E21 should ideally be a direct measure of the curvature following the harmonic
oscillator relation E21 = ℏ(eFκ/m∗ )1/2 . In order to assess the accuracy of this relation, we have simulated
absorption spectra using ﬁnite ﬁelds oriented at various angles to the nanowire major axis. For simplicity,
we work in normalized units such that ideally ε21 = (κ̃E)1/2 or, equivalently, κ̃ = ε221 /E for the harmonic
oscillator. Also, the dynamic polarizability is expressed in units of e2 b2 /E0 = e2 b4 m∗ /ℏ2 . The fourth-power
scaling with dimensions is characteristic of polarizabilities in effective-mass theories [16–20]. We must
distinguish between the actual geometric curvature κ̃ and the inferred curvature ε221 /E derived from
absorption resonances. Only in the limit of extremely large ﬁelds will the two agree. From a comparison at
various ﬁnite ﬁeld strengths we may then quantify the inherent error associated with the inferred curvature.
In ﬁgure 4, we present simulated absorption spectra for normalized Stark ﬁelds E of magnitude 100 and
1000, oriented at various angles to the ellipse major axis a taking, again, η = 1.5. The photon frequency ω is
normalized by E0 , i.e. we substitute ℏω/E0 → ω and, moreover, a ﬁnite line width is included by adding an
imaginary term i/2 to ω. The top and bottom panels in ﬁgure 4 illustrate cases of moderate and strong
Stark ﬁelds, respectively. If E = 100, the Stark shift is not quite in the harmonic oscillator limit. As a
consequence, the absorption spectra contain several resonances that shift with orientation of the Stark ﬁeld.
In contrast, if E = 1000, each spectrum essentially consists of a single peak. An example of the transition
responsible for this peak is shown in the ﬁgure inset in ﬁgure 4, bottom panel. Here, the ground and ﬁrst
6

## PDF page 8

New J. Phys. 24 (2022) 093005

T G Pedersen et al

Figure 4. Simulated probe absorption in cases of moderate (E = 100, top panel) and strong (E = 1000, bottom panel) Stark
ﬁelds. Different orientations of the Stark ﬁeld between 0◦ and 90◦ are indicated by color. The graph insets compare the inferred
and actual curvatures vs angle. Also, the bottom ﬁgure inset illustrates ground and ﬁrst excited Stark-localized states.

excited Stark-localized states are shown. It is clear that the transition dipole is perpendicular to the Stark
ﬁeld such that a perpendicular component in the probe ﬁeld is required.
We now turn to the curvatures inferred from the resonances ε221 /E in the absorption spectra. These are
shown in red as insets for both moderate and strong Stark ﬁelds in ﬁgure 4. For comparison, the actual
geometric curvature κ̃ is shown as blue symbols. As is apparent from the insets, the inferred curvature tends
to overestimate the actual one. This is especially pronounced is the moderate ﬁeld case, while the error
decreases in the strong ﬁeld. Numerically, the maximum error for E = 1000 is approximately 18% with a
decreasing tendency towards larger angles, reaching 7% at 90◦ orientation. Overall, the inferred curvature
manages to capture the exact angular dependence rather accurately, but quantitative agreement clearly
requires large Stark ﬁelds, as expected.

5. Summary
We have suggested probing transitions between Stark-localized states in nanostructures as a tool for
mapping surface curvature. Physically, a strong Stark ﬁeld pushes carriers against the surface barrier such
that any motion perpendicular to the ﬁeld is sensitive to the local curvature. In turn, a weak
time-dependent probe induces transitions between Stark-localized states. Finally, an analysis of probe
absorption spectra provides the inferred curvature. Using nanowires with elliptic cross sections as
benchmarks, we have examined the feasibility of our proposal. While weak ﬁelds allow for probes of global
properties such as nanowire aspect ratio, a strong ﬁeld is found to provide much more detailed geometric
information. We establish criteria for the required ﬁeld strength demonstrating that our proposal is, indeed,
realistic. Finally, an assessment of curvature inferred from probe absorption spectra shows that local
geometric information can be obtained with reasonable accuracy.

Acknowledgments
DK has been supported by the EXPRO Grant No. 20-17749X of the Czech Science Foundation (GAČR). ES
has been partially funded by Fondecyt (Chile) project #118–0355.

7

## PDF page 9

New J. Phys. 24 (2022) 093005

T G Pedersen et al

Data availability statement
All data that support the ﬁndings of this study are included within the article (and any supplementary ﬁles).

Appendix. Cylindrical Bessel basis
As described in the main text, we transform to a circular domain at the expense of introducing an
anisotropic Laplacian. Moreover, coordinates are scaled such that the radius of the circular domain is unity.
As a convenient normalized basis, we choose the Bessel eigenstates of a circle with isotropic Laplacian
eilθ Jl (λln r)
,
ϕ(0)
r) = √
nl (⃗
πJl+1 (λln )

ε(0)
nl =

λ2ln
.
2

(A1)

Here, J l the lth Bessel function, for which λln is the nth zero, i.e. J l (λln ) = 0 with eigenstate index
n = 1, 2, 3, . . . . Moreover, ε(0)
nl is the normalized energy eigenvalue. We require matrix elements for both
kinetic energies and Stark terms. Thus, between states with identical angular momentum l
⟨

∣ d2 ∣
∣ 2∣
⟩ ⟨
⟩
1
∣
∣ (0)
(0) ∣ d ∣ (0)
ϕ(0)
∣ϕml = ϕnl ∣ 2 ∣ϕml = − λ2ln δnm ,
nl ∣
2
dx
dy
2

(A2)

while the corresponding off-diagonal block l′ ̸= l is
⟨

∣ d2 ∣
∣ 2∣
⟩
⟨
⟩
λln λl′ m
∣
∣ (0)
(0) ∣ d ∣ (0)
=
−
ϕ
= sgn(l′ − l)(l + l′ )
.
ϕ(0)
∣ϕ
∣
∣ϕ
′
′
nl ∣
nl
ml
ml
dx2
dy2
2(λ2l′ m − λ2ln )

(A3)

Similarly, the dipole matrix elements are [20]
∣ ∣
∣ ∣
⟨
⟩
⟨
⟩
λln λl′ m
λln λl′ m
∣ ∣ (0)
∣ ∣ (0)
(0)
′
ϕ(0)
(⃗
r
)
(⃗
r
)
=
δ
,
ϕ
(⃗
r
)
(⃗
r
)
= i sgn(l − l′ )δl′ ,l±1 2
.
∣ϕ
∣ϕ
∣x
∣y
′
′
l ,l±1
nl
nl
ml
ml
2
2
2
(λln − λl′ m )
(λln − λ2l′ m )2
(A4)
Based on these matrix elements, the eigenstates in an electric ﬁeld are found from numerical
diagonalization.

ORCID iDs
T G Pedersen
H D Cornean

https://orcid.org/0000-0002-9466-6190
https://orcid.org/0000-0003-2700-8785

References
[1] Haug H and Koch S W 1993 Quantum Theory of the Optical and Electronic Properties of Semiconductors
(Singapore: World Scientiﬁc)
[2] Basu P K 1997 Theory of Optical Processes in Semiconductors (Oxford: Oxford University Press)
[3] Yu P Y and Cardona M 2003 Fundamentals of Semiconductors (Berlin: Springer)
[4] Zhu J-L, Xiong J-J and Gu B-L 1990 Phys. Rev. B 41 6001
[5] Kan S, Mokari T, Rothenberg E and Banin U 2003 Nat. Mater. 2 155
[6] Kac M 1966 Am. Math. Mon. 73 1
[7] Gutiérrez C, Brown L, Kim C-J, Park J and Pasupathy A N 2016 Nat. Phys. 12 1069
[8] Cornean H, Krejčiřı́k D, Pedersen T G, Raymond N and Stockmeyer E 2022 SIAM J. Math. Anal. 54 2114
[9] Banerjee D, Lao J Y, Wang D Z, Huang J Y, Ren Z F, Steeves D, Kimball B and Sennett M 2003 Appl. Phys. Lett. 83 2061
[10] Koblmuller G and Abstreiter G 2014 Phys. Status Solidi RRL 8 11
[11] Kargar F, Debnath B, Kakko J-P, Säynätjoki A, Lipsanen H, Nika D L, Lake R K and Balandin A A 2016 Nat. Commun. 7 13400
[12] Sze S M 1981 Physics of Semiconductor Devices (New York: Wiley)
[13] Empedocles S A and Bawendi M G 1997 Science 278 214
[14] Li D, Zhang J, Zhang Q and Xiong Q 2012 Nano Lett. 12 2993
[15] Klein J, Wierzbowski J, Regler A, Becker J, Heimbach F, Müller K, Kaniber M and Finley J J 2016 Nano Lett. 16 1554
[16] Pedersen T G, Latini S, Thygesen K S, Mera H and Nikolić B K 2016 New J. Phys. 18 073043
[17] Pedersen T G 2017 Phys. Rev. B 96 115432
[18] Pedersen T G 2019 Phys. Rev. A 99 063410
[19] Pedersen T G 2021 Phys. Rev. B 104 155414
[20] Szabó P, Góger S, Charry J, Karimpour M R, Fedorov D V and Tkatchenko A 2022 Phys. Rev. Lett. 128 070602
[21] Pedersen T G 2017 New J. Phys. 19 043011

8

## PDF page 10

New J. Phys. 24 (2022) 093005

[22]
[23]
[24]
[25]
[26]
[27]
[28]

T G Pedersen et al

Yi G, Wei G and Wu H 2007 Phys. Status Solidi b 244 4651
Troesch B A and Troesch H R 1973 Math. Comput. 27 755
Magner A G, Fedotkin S N, Arita K, Misu T, Matsuyanagi K, Schachner T and Brack M 1999 Prog. Theor. Phys. 102 551
Joseph D D 1967 Arch. Ration. Mech. Anal. 24 325
Fiore A and Grinfeld P 2010 Numer. Funct. Anal. Optim. 31 679
Luo J K, Thomas H, Morgan D V, Westwood D and Williams R H 1994 Semicond. Sci. Technol. 9 2199
Dombi P et al 2020 Rev. Mod. Phys. 92 025003

9
