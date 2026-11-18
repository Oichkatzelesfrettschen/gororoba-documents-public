Source: ChatGPT data export, attachment file_000000003b6071f58874973c2b24d135
PDF sha256: 5d9bf1a25f537745bf505841f43d5b60736602c8a08268d6015c5758887f4161
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine (failed: characters)

# Transcription of white_vera_sylvester_dudzinski_2026_emergent_quantization_from_a_dynamic_vacuum.pdf

Transcription of `white_vera_sylvester_dudzinski_2026_emergent_quantization_from_a_dynamic_vacuum.pdf` in this directory, 7 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-7 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

PHYSICAL REVIEW RESEARCH 8, 013264 (2026)

Emergent quantization from a dynamic vacuum
Harold White ,* Jerry Vera , Andre Sylvester, and Leonard Dudzinski
Casimir, Inc., 16441 Space Center Boulevard, Bldg. D-200, Houston, Texas 77058, USA
(Received 24 October 2025; accepted 18 February 2026; published 9 March 2026)
We show that adding quadratic temporal dispersion to a dynamic-vacuum acoustic model yields a fully
analytic, exactly isospectral mapping to the hydrogenic Coulomb problem. In the regime ω = Dq2 with D =
h̄/(2meff ), a proton-imprinted constitutive profile produces an inverse sound speed 1/cs2 (r) = A(ω) + C(ω)/r
2
) that is Coulombic at each bound eigenfrequency. Separation
and hence a time-harmonic operator (∇ 2 + keff
of variables yields the exact hydrogenic eigenfunctions Rnℓ (r)Yℓm (θ, φ); the angular labels (ℓ, m) emerge
naturally from the Laplace-Beltrami spectrum on S2 via rotational symmetry and boundary conditions (as in
standard quantum mechanics), while localization follows from A(ωn ) < 0 in a reactive stop band consistent with
causal, passive dispersion. While angular-momentum quantization follows directly from rotational symmetry
and boundary conditions in standard quantum mechanics (consistent with Noether’s theorem), here it emerges
within a classical-like dispersive acoustic framework without introducing additional wave-mechanical postulates
beyond symmetry and self-adjointness. This highlights dispersion’s role in bridging a hydrodynamic description
to quantumlike spectral structure. Identifying qn ≡ κn maps spatial scale to frequency, giving ωn = Dκn2 ∝ 1/n2
and reproducing the Rydberg ladder. Calibration to the reduced-mass Rydberg frequency (ω∗ = 2π cRH ) fixes
D = h̄/(2μ) and meff = μ, with no free parameters. We determine the frequency dependence of A(ωn ) and C(ωn )
consistent with the underlying dispersive physics and demonstrate agreement with hydrogenic mode shapes and
transition lines. The framework also predicts isotope shifts [μ → μ(M )] and symmetry-respecting Stark/Zeeman
analogues. Dispersion thus renders quantization an emergent consequence of symmetry, boundary conditions,
and causal response in a dynamic vacuum.
DOI: 10.1103/l8y7-r3rm

I. INTRODUCTION

In our prior work [1], we derived an acoustic wave
equation from the Schrödinger equation via Madelung hydrodynamics and demonstrated numerically that hydrogenic
orbital morphologies arise as acoustic resonances of a dynamic vacuum. The present work supplies the missing
temporal-dispersion closure needed to make the mapping fully
analytic and exactly isospectral to the hydrogenic Coulomb
problem. The physical basis for this dispersion, rooted
in linearized Madelung hydrodynamics, is derived in the
Appendix.
(1) Temporal dispersion of the medium: Small longitudinal
disturbances obey a quadratic dispersion in the regime of
interest:
h̄
ω = D q2 , D =
.
(1)
2 meff
The dispersive closure is a quadratic law in the regime of
interest (derived from Madelung hydrodynamics with quantum potential Q in the Appendix), which converts a spatial
*

Contact author: sonny@casimirspace.com

Published by the American Physical Society under the terms of the
Creative Commons Attribution 4.0 International license. Further
distribution of this work must maintain attribution to the author(s)
and the published article’s title, journal citation, and DOI.
2643-1564/2026/8(1)/013264(7)

inverse length into an oscillation frequency. By itself, Eq. (1)
does not quantize anything; it only maps scale to rate. This
quadratic regime is the long-wavelength/quantum-pressure
limit of the Madelung/Bogoliubov linearization [2] and also
arises in gradient-elastic continua [3–6].
(2) Spatial constitutive profile of the dynamic vacuum: A
proton-imprinted, radially varying medium [ρ(r) = γ /r 4 ]
and a finite far-field background make the local inverse sound
speed
1
cs2 (r)

= A(ω) +

C(ω)
,
r

(2)

2
which makes the time-harmonic acoustic operator (∇ 2 + keff
)
Coulombic:
(
)
C
β(ω)
ω2
2
= ω2 A +
≡ α(ω) +
. (3)
(r; ω) = 2
keff
cs (r)
r
r

Note. We distinguish (a) the plane-wave (spectral) wave
number q appearing in the dispersion (1); (b) the spatial operator coefficient keff
√(r; ω) in Eq. (3); and (c) the bound-state
inverse length κ ≡ −α that characterizes the evanescent tail
of a normalizable solution. In a uniform medium, keff would
coincide with the spectral wave number, but here the inhomogeneity (the 1/r term) is what generates hydrogenic structure,
so we keep these symbols distinct. We only identify qn ≡ κn
when using the dispersion to map spatial scale to frequency.
The next steps complete the development of the full hydrogenic eigenfunctions and observed spectrum. With Eqs. (2)

013264-1

Published by the American Physical Society

## PDF page 2

WHITE, VERA, SYLVESTER, AND DUDZINSKI

PHYSICAL REVIEW RESEARCH 8, 013264 (2026)

and (3), separation of variables p = Rℓ (r)Yℓm (θ , φ) yields the
radial ordinary differential equation (ODE)
]
[
β(ω) ℓ(ℓ + 1)
′′
u(r) = 0, u = rRℓ .
u (r) + α(ω) +
−
r
r2
Choosing the (causal, dispersive) coefficients at the eigenfrequencies ωn , one has α(ωn ) = −κn2 and β(ωn ) = β (independent of n or a constant for all eigenfrequencies) makes
this ODE identical to the hydrogenic Coulomb equation [7].
Regularity at r = 0 and decay as r → ∞ (which requires
A(ωn ) < 0, i.e., a reactive stop band) then quantize the spatial
scale and angular momentum:
κn =

β
,
2n

ℓ = 0, 1, 2, . . . ,

m = −ℓ, . . . , ℓ.

Thus, the full hydrogenic eigenfunctions Rnℓ (r)Yℓm (θ , φ) and
the (n, ℓ, m) labels emerge from the spatial eigenproblem—
they are not postulated.
Once the spatial quantization is established, the temporal
dispersion (1) maps κn to eigenfrequencies by the identification qn ≡ κn :
ωn = D κn2 = D

β 1
4 n2
2

⇒

1
En = −h̄ ωn ∝ − 2 .
n

Calibrating D = h̄/(2μ) (electron-proton reduced mass μ)
aligns the dispersion constant with the kinetic-energy operator
of the Schrödinger equation, while choosing β = 2/a0 sets
the effective coupling scale so that the resulting eigenvalues reproduce the Rydberg series. Here, a0 = 4π ε0 h̄2 /(μe2 )
is the Bohr radius, which thus enters only as a calibration
scale rather than an assumed quantum postulate. Item (2) (the
Coulombic operator) creates the quantized hydrogenic spatial
spectrum and angular momentum; item (1) (the quadratic
dispersion) converts each quantized spatial scale into the correct 1/n2 energy/frequency ladder. Together, they render the
acoustic problem isospectral to hydrogen in both eigenfunctions and spectrum, with a single reduced-mass calibration
(which simultaneously fixes the Bohr radius and energy scale)
to observation. In short, once the dynamic vacuum is endowed
with the quadratic dispersion of Eq. (1) and the Coulombic
constitutive profile of Eq. (3), the acoustic Helmholtz problem becomes Coulombic, angular-momentum quantization
emerges from symmetry, bound states follow from A < 0 [8],
and the spectrum matches observation with a single reducedmass calibration. The remainder of the paper develops this
construction, details the frequency dependence of A(ω) and
C(ω), and compares predicted levels and lines to hydrogen
data.
II. MINIMAL ASSUMPTIONS AND DISPERSION

We make a compact set of explicit assumptions that together fix the governing operator, the spectrum, and the
mapping to observation. No postulate of angular-momentum
quantization is required.
(1) Medium and governing equation: The vacuum is
modeled as a longitudinal, compressible continuum with spatially varying fields ρ(r) (effective density) and B(r) (bulk
modulus). Small-signal dynamics (to leading order, lossless)

obey
∇ · [ρ(r)−1 ∇ p] − B(r)−1 ∂t2 p = 0,
(∇

2

2
+ keff
) p = 0,
2
keff (r) = ω2 /cs2 (r),
cs2 = B/ρ.

(4a)
(4b)
(4c)
(4d)

(2) Near-field density law (proton imprint): Guided by the
electrostatic energy density around a proton, the near-field
density scales as
γ
ρ(r) = 4 , γ > 0 constant.
(5)
r
(An ambient ρ∞ is included without changing the conclusions
below.)
(3) Bulk modulus ansatz (Coulombic map): The effective
inverse sound speed has a constant background plus a 1/r
term,
ρ(r)
C(ω)
1
=
= A(ω) +
,
cs2 (r)
B(r)
r

(6)

realized, for example, by B(r) = B∞ + βB /r 3 together with
Eq. (5) [9], giving A = ρ∞ /B∞ (if ρ∞ ̸= 0) and C = γ /βB .
Consequently,
)
(
β
C
ω2
2
≡α+ .
keff
(r) = 2
= ω2 A +
(7)
cs (r)
r
r
This is the Coulombic (1/r) structure required for hydrogenic
isospectrality.
(4) Dispersion (linchpin): The longitudinal mode is dispersive with a quadratic (Schrödinger-like) law,
ω = D q2 ,

D=

h̄
.
2 meff

(8)

The full linearized Madelung dispersion has the form ω2 =
cL2 k 2 + D2 k 4 ; a concise derivation is given in the Appendix,
which connects the spatial inverse length q to temporal
frequency. This form is the short-wavelength limit of the
2
)q4 [5],
standard Bogoliubov relation ω2 = cs2 q2 + ( h̄2 /4meff
and also arises in gradient-elastic continua. It uniquely yields
the observed 1/n2 spectrum once the spatial operator is
Coulombic.
Notation: The plane-wave wave number q, the spatial operator√coefficient keff (r; ω), and the bound-state inverse length
κ = −α are kept distinct; only at discrete eigenfrequencies
ωn do we identify qn ≡ κn when mapping spatial scale to
frequency.
(5) Symmetry and boundary conditions: Spherical symmetry applies for the single-proton problem. Solutions are regular
at r = 0 and square integrable (evanescent) as r → ∞. The
latter requires
lim k 2 (r) = α = ω2 A(ω) = −κ 2 < 0

r→∞

⇒

A(ω) < 0,

(9)

i.e., a reactive (stop-band) far field that produces the familiar
exponential tails.
(6) Observation mapping and calibration: The dispersion
maps each spatial eigenvalue κn to a temporal frequency by

013264-2

## PDF page 3

EMERGENT QUANTIZATION FROM A DYNAMIC VACUUM

PHYSICAL REVIEW RESEARCH 8, 013264 (2026)

qn ≡ κn , giving
ωn = D κn2 = D

β 1
,
4 n2

III. EMERGENT ANGULAR MOMENTUM FROM
SPHERICAL SYMMETRY

2

(10)

so that En = −h̄ ωn ∝ −1/n2 . Calibration to hydrogen data
uses the reduced-mass Rydberg constant RH with ω∗ =
2π cRH and β = 2/a0 , yielding
D = ω∗ a02 =

h̄
,
2μ

(11)

so the effective mass of the longitudinal mode equals the
electron-proton reduced mass μ.
Results of assumptions. With Eq. (7), separation of p =
Rℓ (r)Yℓm (θ , φ) and u = rRℓ gives
]
[
ℓ(ℓ + 1)
β
′′
u(r) = 0,
(12)
u (r) + α + −
r
r2
the hydrogenic Coulomb radial equation.√Hence, the acoustic
problem is isospectral to hydrogen: κ = −α, n = β/(2κ ) =
nr + ℓ + 1, and
ℓ −κr

Rnℓ (r) ∝ (2κr) e

(2ℓ+1)
Ln−ℓ−1
(2κr),

pnℓm ∝ Rnℓ (r) Yℓm (θ , φ).

(13a)
(13b)

Quantization of ℓ and m emerges naturally from spherical symmetry; it is not an added axiom. Once the medium
is endowed with the quadratic dispersion of Eq. (8) and
the Coulombic constitutive profile of Eq. (7), the dynamicvacuum acoustic problem reproduces the hydrogenic spectrum and eigenfunctions, with a single reduced-mass calibration to observation.
Operator matching and self-adjointness. The time2
2
harmonic equation (∇ 2 + keff
)p = 0 with keff
(r) = ω2 (A +
C/r) separates in spherical coordinates. Writing p(r, θ , φ) =
Rℓ (r)Yℓm (θ , φ) and u = rRℓ gives [10]
]
[
β(ω) ℓ(ℓ + 1)
′′
u(r) = 0,
−
u (r) + α(ω) +
r
r2
u(0) = u(∞) = 0.
Comparing with the Coulomb Schrödinger equation u′′ +
[ 2μE /h̄2 + (2μe2 /4π ε0 h̄2 )(1/r) − ℓ(ℓ + 1)/r 2 ]u = 0
identifies
α(ω) =

2μE
,
h̄2

β(ω) =

2μe2
≡ β,
4π ε0 h̄2

showing that the acoustic operator is mathematically identical
to the hydrogenic Coulomb operator. For bound states E < 0,
α(ωn ) = −κn2 with κn = β/(2n). The normalized radial functions are
(2ℓ+1)
Rnℓ (r) = Nnℓ (2κn r)ℓ e−κn r Ln−ℓ−1
(2κn r),
√
(n − ℓ − 1)!
.
Nnℓ = (2κn )3/2
2n(n + ℓ)!

In this construction, the angular quantum numbers are not
postulated. They emerge from the spherical symmetry of the
single-proton problem, the scalar character of the acoustic
pressure p, and the requirement of regularity and singlevaluedness on the compact angular manifold S2 . For any
2
central constitutive profile keff
(r; ω), the Laplacian separates
as
L̂ 2
1
2
∂
(r
∂
)
−
,
r
r
r2
r2
]
[
1
1
2
2
∂θ (sin θ ∂θ ) +
∂ .
L̂ = −
sin θ
sin2 θ φ

∇2 =

(14)

2
Substituting p(r, θ , φ) = R(r)Y (θ , φ) into (∇ 2 + keff
)p = 0
gives the separated equations
]
[
1
λ
2
2
R = 0. (15)
L̂ 2Y = λY,
∂
(r
∂
R)
+
k
(r;
ω)
−
r
r
eff
r2
r2

On the compact sphere S2 , the conditions of single-valuedness
in φ (2π -periodicity) and regularity at the poles θ = 0, π
enforce the discrete Laplace-Beltrami spectrum
λ = ℓ(ℓ + 1),
ℓ = 0, 1, 2, . . . ,
m = −ℓ, . . . , ℓ,

(16)

with orthonormal eigenfunctions Yℓm (θ , φ) [11,13]. Thus, the

integer labels ℓ, m are an emergent spectral property of the
angular eigenproblem on S2 , not an additional quantization
axiom.
Defining u(r) ≡ r R(r) removes the first derivative from
the radial equation:
]
[
ℓ(ℓ + 1)
′′
2
u(r) = 0, u(0) = 0,
u (r) + keff (r; ω) −
r2
u(∞) = 0.

(17)

2
For the Coulombic constitutive map keff
(r; ω) = α(ω) +
β(ω)/r (Sec. II), Eq. (17) becomes the hydrogenic radial
ODE. Normalizability enforces the usual Laguerre solutions
Rnℓ (r) with n = nr + ℓ + 1 and the familiar degeneracies: For
each n, the allowed ℓ are 0, 1, . . . , n − 1, and each ℓ supports
a (2ℓ + 1)-fold magnetic degeneracy in m (total n2 ).
Takeaway. Discrete angular momentum arises automatically from the symmetry of the problem—The LaplaceBeltrami spectrum on S2 and the scalar nature of p are
sufficient. The centrifugal term ℓ(ℓ + 1)/r 2 and the hydrogenic degeneracies follow without any extra quantization
postulate.

IV. MAPPING TO OBSERVATION, DISPERSIVE
PARAMETERS, AND VALIDATION

These eigenfunctions form a complete orthonormal basis
for each ℓ and confirm the exact isospectrality between the
dynamic-vacuum acoustic operator and hydrogenic quantum
mechanics.

The spatial eigenproblem fixes the bound-state scale and
eigenfunctions,

013264-3

κn =

1
,
n a0

pnℓm (r, θ , φ) = Anℓm Rnℓ (r) Yℓm (θ , φ),

(18)

## PDF page 4

WHITE, VERA, SYLVESTER, AND DUDZINSKI

PHYSICAL REVIEW RESEARCH 8, 013264 (2026)

TABLE I. Energylike level values using reduced mass consistently (RH ). Both analytic and observation columns use RH . Frequencies in
PHz. Constants from CODATA 2018 [14].
n

|En | analytic (eV)

fn analytic (PHz)

|En | obs (eV)

fn obs (PHz)

1
2
3
4
5
6
7

13.598 434 006
3.399 608 501
1.510 937 112
0.849 902 125
0.543 937 360
0.377 734 278
0.277 518 041

3.288 051
0.822 013
0.365 339
0.205 503
0.131 522
0.091 335
0.067 103

13.598 434 006
3.399 608 501
1.510 937 112
0.849 902 125
0.543 937 360
0.377 734 278
0.277 518 041

3.288 051
0.822 013
0.365 339
0.205 503
0.131 522
0.091 335
0.067 103

so the quantized inverse length directly determines each
level’s frequency via the quadratic dispersion relation,
ωn = D κn2 =

ω∗
,
n2

1
En = −h̄ ωn ∝ − 2 .
n

The level differences reproduce the Rydberg ladder,
)
(
ω∗ 1
E
1
=
fn2 →n1 =
−
h
2π n12
n22
(
)
1
1
= c RH 2 − 2 ,
n1
n2

(19)

Both scale inversely with powers of n, consistent with the
frequency-dependent elasticity needed to maintain Coulombic
isospectrality.
Validation. Once the dispersion and reduced-mass calibration are fixed, the framework has no free parameters. The
eigenfunctions are hydrogenic and the levels follow the 1/n2
law. Tables I and II compare analytic and observed hydrogen
data (identical within precision), and Fig. 1 visualizes selected
isosurfaces of |ψnℓm |2 . The spatial morphology and transition

(20)

with calibration ω∗ = 2π cRH using the reduced-mass Rydberg constant RH [14].
Reduced-mass calibration. The electron-proton system
uses μ = me m p /(me + m p ) ≈ 0.999 46 me , which rescales the
Bohr radius and Rydberg constant as
a0(H ) =

4π ε0 h̄2
me (∞)
a ,
=
μe2
μ 0

RH = R∞

μ
.
me

With D = ω∗ (a0(H ) )2 , one obtains
D=

h̄
,
2μ

meff = μ ,

(21)

so the effective inertial parameter of the longitudinal mode
equals the reduced mass. No further tuning is required: all
absolute numbers follow from RH and a0(H ) .
2
Frequency-dependent parameters. From keff
= ω2
(A + C/r) = α + β/r, αn = −1/(n2 a02 ), and β = 2/a0 ,
the dispersion-linked coefficients are
n2
A(ωn ) = − 2 2 ,
a0 ω∗

C(ωn ) =

2n4
.
a0 ω∗2

(22)

Hence, A < 0 identifies a reactive (stop-band) far field where
modes are evanescent and localized, while C > 0 represents
the proton-induced increase of 1/cs2 near the core. Their
monotonic scalings |A| ∝ n2 , C ∝ n4 reflect how different
eigenfrequencies probe different points of the same dispersive
response function.
Material interpretation. Using ρ(r) = γ /r 4 and B(r) =
B∞ + βB /r 3 , one has 1/cs2 = ρ/B ≃ A + C/r with A =
ρ∞ /B∞ and C = γ /βB , so
B∞ (ωn ) = − ρ∞

a02 ω∗2
,
n2

βB (ωn ) = γ

a0 ω∗2
.
2n4

FIG. 1. Hydrogenic orbital density isosurfaces: Each panel
shows the isosurface of the analytic probability density
|ψnℓm (x, y, z)|2 at a fixed physical threshold (nm−3 ), computed
from Rnℓ (r) and real Yℓm (θ, φ). Isosurfaces were extracted via a
marching-cubes method; a narrow angular “pie-wedge” was masked
in volume prior to extraction to reveal interior structure, and gray
shading is illustrative only. These visualizations match the familiar
textbook morphology of hydrogenic orbitals [11].

013264-4

## PDF page 5

EMERGENT QUANTIZATION FROM A DYNAMIC VACUUM

PHYSICAL REVIEW RESEARCH 8, 013264 (2026)

TABLE II. Selected hydrogen vacuum lines using reduced mass consistently (RH ). Both analytic and observation columns use RH .
Frequencies in PHz and wavelengths in nm. Constants from CODATA 2018 [14]; observed values cross-checked with NIST ASD [15].
Transition
Lyman-α (2 → 1)
Lyman-β (3 → 1)
Lyman-γ (4 → 1)
Hα (3 → 2)
Hβ (4 → 2)
Balmer-γ (5 → 2)
Paschen-α (4 → 3)
Paschen-β (5 → 3)

f analytic (PHz)

λ analytic (nm)

f obs (PHz)

λ obs (nm)

2.466 038
2.922 712
3.082 576
0.456 674
0.609 285
0.654 573
0.159 836
0.233 817

121.568 446
102.573 376
97.087 384
656.281 106
492.162 878
456.867 793
1 875.627 447
1 282.167 200

2.466 038
2.922 712
3.082 576
0.456 674
0.609 285
0.654 573
0.159 836
0.233 817

121.568 446
102.573 376
97.087 384
656.281 106
492.162 878
456.867 793
1 875.627 447
1 282.167 200

frequencies match hydrogen exactly, demonstrating that the
dynamic-vacuum construction reproduces the observed Rydberg spectrum with a single reduced-mass calibration.

R. Efraim and D. Narea for helpful comments on manuscript
readability. AI tools were used to assist with enhancing readability and communicating ideas.

V. DISCUSSION AND CONCLUSION

DATA AVAILABILITY

Quadratic dispersion, ω = Dq2 with D = h̄/(2meff ), is
the essential ingredient that renders the dynamic-vacuum
acoustic problem analytically isospectral with hydrogen.
With the minimal constitutive map 1/cs2 (r) = A(ω) + C(ω)/r
and near-field density ρ(r) = γ /r 4 , the time-harmonic op2
erator (∇ 2 + keff
) becomes exactly Coulombic. Separation
then produces the standard hydrogenic basis Rnℓ (r)Yℓm (θ , φ);
angular-momentum quantization arises naturally from the S2
eigenproblem, and localization follows from A(ωn ) < 0.
Calibration to observation through the reduced-mass Rydberg frequency ω∗ = 2π c RH fixes all constants and implies
D = h̄/(2μ), with meff = μ (the electron-proton reduced
mass). Without additional parameters, the model reproduces
the hydrogenic shapes (Fig. 1), the 1/n2 level spacing and
Rydberg ladder (Tables I and II), and isotope shifts via
μ → μ(M ). Weak, slowly varying perturbations of 1/cs2 (r)
introduce Stark- or Zeeman-type splittings on the same analytic basis, confirming the robustness of the mapping.
This framework parallels the hydrodynamic or Madelung
formulation, where dispersion enters as a quantumlike correction. Here, however, the quadratic regime alone suffices
to produce full isospectrality, revealing quantization as an
emergent property of a dispersive, dynamic vacuum rather
than an imposed axiom. Subleading corrections (O(1/r 2 )) or
small loss terms would shift line centers or set linewidths
perturbatively but do not alter the analytic core. Extensions
to multicenter or externally forced problems follow from the
same separation principles.
In summary, a single physically motivated assumption—
quadratic dispersion—yields a closed, analytic, and observationally calibrated construction of the hydrogen spectrum. Angular momentum emerges from geometry, bound states from
A < 0, and the spectral ladder from one reduced-mass calibration. The result is a self-consistent, dispersion-anchored
dynamic-vacuum model in which quantization arises naturally
from the symmetry of the medium itself.
ACKNOWLEDGMENTS

The authors thank Casimir for institutional support during
the development of the analytic model. Special thanks to

No data were created or analyzed in this study.
APPENDIX: DISPERSION RELATION FROM MADELUNG
HYDRODYNAMICS WITH QUANTUM POTENTIAL
1. Starting point: Schrödinger equation

Consider a nonrelativistic scalar field of effective mass μ
governed by the Schrödinger equation
i h̄

h̄2
∂ψ
= − ∇ 2 ψ + V (x)ψ,
∂t
2μ

(A1)

where V (x) is an external or mean-field potential. We perform
the Madelung transformation
√
(A2)
ψ (x, t ) = ρ(x, t ) eiS(x,t )/h̄
and define the hydrodynamic velocity field
v=

∇S
.
μ

(A3)

2. Madelung hydrodynamic equations

Substituting into Eq. (A1) and separating real and imaginary parts yields the continuity equation
∂ρ
+ ∇ · (ρv) = 0,
∂t
and an Euler-like momentum equation,
)
(
∂v
+ (v · ∇ )v = −∇(V + Q),
μ
∂t

(A4)

(A5)

where the quantum potential Q is
√
h̄2 ∇ 2 ρ
Q(x, t ) = −
√ .
2μ
ρ

(A6)

Consider the force/momentum equation (A5) in the case
of static equilibrium (i.e., no acoustic excitation). In this
scenario, the classical potential term ∇V represents the equilibrium pressure gradient 1/ρ0 ∇P0 of the vacuum. Under this

013264-5

## PDF page 6

WHITE, VERA, SYLVESTER, AND DUDZINSKI

PHYSICAL REVIEW RESEARCH 8, 013264 (2026)

equilibrium identification, the momentum equation (A5) may
be expressed as
(
)
∂v
1
μ
+ (v · ∇ )v = − ∇P(ρ) − ∇Q.
(A7)
∂t
ρ
In the presence of acoustic excitation, the classical potential contributes only through the background pressure profile,
while the quantum potential governs the dynamical restoring
force associated with density fluctuations.

b. Linearized momentum equation

For small-amplitude perturbations, the convective term
(v · ∇ )v is second order in small quantities and can be neglected compared to the time derivative ∂v1 /∂t, i.e., |(v ·
∇ )v| ≪ |∂v/∂t|. The linearized form of Eq. (A7) is therefore
μ

Taking the divergence of Eq. (A15) gives

We now consider small longitudinal perturbations about
this equilibrium configuration:
v(x, t ) = v1 (x, t ),

μ

ρ1 ≪ ρ0 .
(A8)

We linearize about a static equilibrium state (ρ0 , v0 = 0)
with a time-independent background potential. The following
equations describe the dynamics of small perturbations about
this state; any purely background force balance is absorbed
into the equilibrium configuration.
From Eq. (A4), one obtains
∂ρ1
+ ρ0 ∇ · v1 = 0.
(A9)
∂t
Assuming a barotropic equation of state P = P(ρ), we
expand about ρ0 :
∣
dP ∣∣
P(ρ) ≈ P(ρ0 ) +
ρ1 .
(A10)
dρ ∣ρ0
Defining the longitudinal sound speed
∣
1 dP ∣∣
2
cL ≡
,
μ dρ ∣ρ0

μc2
h̄2
∂
∇ 4 ρ1 .
(∇ · v1 ) = − L ∇ 2 ρ1 +
∂t
ρ0
4μρ0

(A16)

Using Eq. (A9) to eliminate ∇ · v1 , one obtains
h̄2 4
∂ 2 ρ1
2 2
=
c
∇
ρ
−
∇ ρ1 .
1
L
∂t 2
4μ2

(A17)

Equation (A17) is the linearized wave equation governing
density perturbations in the Madelung fluid, including the
contribution of the quantum potential.
5. Dispersion relation

Assuming a plane-wave solution
ρ1 (x, t ) = ρ̂ ei(k·x−ωt ) ,

(A18)

substitution into Eq. (A17) yields
(A11)

the linearized pressure gradient becomes
1
μc2
− ∇P(ρ) ≈ − L ∇ρ1 .
ρ
ρ0

(A15)

4. Wave equation for density perturbations

3. Linearized equations for perturbations

ρ(x, t ) = ρ0 + ρ1 (x, t ),

h̄2
∂v1
μc2
∇(∇ 2 ρ1 ).
= − L ∇ρ1 +
∂t
ρ0
4μρ0

ω2 = cL2 k 2 +

h̄2 4
k .
4μ2

(A19)

Defining
(A12)

D≡

h̄
,
2μ

(A20)

a. Linearized quantum potential

Expanding the quantum potential (A6) to linear order in ρ1
yields
h̄2
Q≈−
∇ 2 ρ1 ,
4μρ0

the dispersion relation may be written compactly as
ω2 = cL2 k 2 + D2 k 4 .

(A21)

(A13)

(A14)

This dispersion relation contains both the acoustic (k 2 ) and
quantum-pressure (k 4 ) contributions and follows directly from
the Madelung hydrodynamic formulation when perturbations
about a force-balanced vacuum background are considered.

[1] H. White, J. Vera, P. Bailey, P. March, T. Lawrence, A.
Sylvester, and D. Brady, Acoustic derivation from Schrödinger
and numerical evidence for orbital resonances in a dynamic
vacuum, Phys. Open 1, 100009 (2019).
[2] The Madelung/Bogoliubov linearization refers to expressing
the Schrödinger or Gross-Pitaevskii equation in hydrodynamic
form (via Madelung’s transformation) and then linearizing

about a uniform background density to obtain small-amplitude
wave equations. This procedure yields the Bogoliubov dispersion relation ω2 = cs2 k 2 + h̄2 k 4 /4m2 , where the first term corresponds to acoustic (phononlike) behavior and the second term
arises from quantum-pressure effects. At low k (long wavelengths), the first term dominates and gives acoustic behavior
(ω ∝ k); at high k (short wavelengths or quantum-pressure-

so that
−∇Q ≈

h̄2
∇(∇ 2 ρ1 ).
4μρ0

013264-6

## PDF page 7

EMERGENT QUANTIZATION FROM A DYNAMIC VACUUM
dominated regime), the second term dominates, yielding a
quadratic dependence ω ∝ k 2 .
[3] E. Madelung, Quantentheorie in hydrodynamischer form, Z.
Phys. 40, 322 (1927).
[4] N. N. Bogoliubov, On the theory of superfluidity, J. Phys.
(USSR) 11, 23 (1947).
[5] L. Pitaevskii and S. Stringari, Bose-Einstein Condensation and
Superfluidity (Oxford University Press, Oxford, 2016), Chaps. 2
and 3.
[6] R. D. Mindlin, Micro-structure in linear elasticity, Arch.
Rational Mech. Anal. 16, 51 (1964).
[7] In this construction, the coefficients α(ω) and β(ω) represent
the effective response of the dispersive medium, analogous
to the energy and Coulomb coupling terms in the hydrogenic Schrödinger equation. Because the medium is causal
and frequency dependent, these coefficients vary with ω;
however, the physically relevant solutions occur only at discrete eigenfrequencies ωn . Evaluating the coefficients at these
eigenfrequencies and imposing α(ωn ) = −κn2 ensures that the
effective propagation constant is imaginary, corresponding to
a bound (evanescent) spatial mode. Setting β(ωn ) = β, independent of n, keeps the 1/r coupling strength constant across
all eigenstates. With these assignments, the radial equation reduces to the hydrogenic Coulomb equation. Thus, the quantized
hydrogenic structure emerges naturally from the dispersive
acoustic formulation without introducing it as an external
assumption.
[8] The condition A(ω) < 0 designates a reactive regime of the
dispersive medium in which the effective squared wave number

PHYSICAL REVIEW RESEARCH 8, 013264 (2026)
becomes negative, producing evanescent (spatially decaying)
solutions rather than propagating waves. Physically, this corresponds to a stop band in which the stored reactive energy
exceeds the kinetic component, confining the mode and creating
a discrete bound state. In this sense, A < 0 plays the same role
as negative total energy E < 0 in the Schrödinger formulation
of hydrogen, marking the transition from continuum to bound
eigenmodes.
[9] With ρ(r) = γ /r 4 and B(r) = βB /r 3 , one has ρ/B =
(γ /βB ) r −1 exactly; including a background B∞ preserves
the Coulombic 1/r core for r ≪ (βB /B∞ )1/3 while allowing a
tunable constant term A(ω) = ρ∞ (ω)/B∞ (ω).
[10] With domain u ∈ L 2 ((0, ∞), dr), the radial operator is selfadjoint, ensuring a real, discrete spectrum (Sturm-Liouville
theory [12]).
[11] D. J. Griffiths and D. F. Schroeter, Introduction to Quantum
Mechanics, 3rd ed. (Cambridge University Press, Cambridge,
2018).
[12] A. Zettl, Sturm-Liouville Theory (American Mathematical Society, Providence, 2005).
[13] G. B. Arfken, H. J. Weber, and F. E. Harris, Mathematical
Methods for Physicists, 7th ed. (Academic Press, Oxford, 2013).
[14] E. Tiesinga, P. J. Mohr, D. B. Newell, and B. N.
Taylor, CODATA recommended values of the fundamental physical constants: 2018, Rev. Mod. Phys. 93, 025010
(2021).
[15] A. Kramida, Y. Ralchenko, J. Reader, and NIST ASD team,
NIST atomic spectra database, version 5.x, https://physics.nist.
gov/asd.

013264-7
