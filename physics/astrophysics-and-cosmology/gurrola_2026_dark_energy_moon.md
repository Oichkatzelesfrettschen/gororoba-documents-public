Source: https://arxiv.org/abs/2603.04841v1
PDF sha256: 1d8e94aac2d2791f3dd9f45701b7e78bf0f8b9085deb637937e72057c3ac1cfa
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of gurrola_2026_dark_energy_moon.pdf

Transcription of `gurrola_2026_dark_energy_moon.pdf` in this directory, 9 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-9 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Probing Dark Energy on the Moon
Alfredo Gurrola,1 Robert J. Scherrer,1 Oem Trivedi1

arXiv:2603.04841v1 [astro-ph.CO] 5 Mar 2026

1

Department of Physics and Astronomy, Vanderbilt University, Nashville, TN, USA

The effective field theory (EFT) of cosmic acceleration provides a model-independent framework
for describing dark energy and modified gravity, yet many of its defining operators remain weakly
constrained by existing observations. We show that measurements of horizon-scale metric fluctuations with a lunar laser interferometer directly probe the kinetic sector of the EFT of dark energy,
enabling constraints on operators governing scalar perturbation dynamics rather than background
expansion. In particular, we demonstrate sensitivity to the EFT kinetic coefficient M24 and the
associated sound speed of dark energy, c2s . This establishes a qualitatively new observational handle
on the microphysical consistency conditions of late-time acceleration models, allowing broad classes
of EFT parameter space to be either discovered or excluded.

INTRODUCTION

Explaining the origin of the observed late–time cosmic acceleration remains one of the most profound open
problems in fundamental physics. Although the standard
ΛCDM paradigm provides an excellent phenomenological
description of a broad range of cosmological observations,
the physical nature of the component driving acceleration, dark energy, [1] is still unknown. This ambiguity
has motivated a vast landscape of theoretical proposals,
including dynamical scalar fields, modified gravity theories, and scenarios inspired by quantum gravity [2, 3, 5].
A particularly powerful framework for organizing and
comparing these possibilities is the effective field theory
(EFT) of cosmic acceleration [6–11]. The EFT formalism provides a unifying and model–independent language
in which all operators consistent with the symmetries
of a quasi FLRW spacetime are systematically parameterized. In this approach, different dark energy and
modified gravity models correspond to specific choices
of time–dependent EFT coefficients. Observational constraints can therefore be mapped directly onto combinations of operators that encode the underlying microphysics, without committing to a particular ultraviolet
completion.
Most current observational constraints focus on background quantities, such as the dark energy equation of
state parameter w. However, widely different theories
can yield nearly identical background expansion histories [12–16]. Within the EFT framework, this degeneracy arises because background evolution probes only
a restricted subset of operators, leaving the kinetic and
gradient structure of perturbations comparatively unconstrained. In particular, the sound speed of dark energy perturbations, c2s , which governs the propagation of
scalar fluctuations and controls the clustering properties
of dark energy, remains only weakly bounded.
The value of c2s provides a direct discriminator between
classes of models. Canonical scalar field scenarios generically predict c2s = 1, implying that dark energy perturbations propagate luminally and remain smooth on sub-

horizon scales. In contrast, more general constructions
including coupled dark energy models [17–21], k-essence
and other non-canonical theories [22–36], and broad subclasses of the EFT parameter space, naturally predict
c2s ≪ 1, enabling significant clustering on cosmological
scales. In some cases, superluminal propagation (c2s > 1)
can also arise at the level of the low–energy effective description. Consequently, measuring or constraining c2s
provides direct information about the kinetic operators
in the EFT action and about the stability and consistency of the theory.
Despite its theoretical importance, the sound speed of
dark energy has proven extremely challenging to constrain observationally. Existing bounds are derived primarily from integrated effects in the late–time Universe,
such as the Integrated Sachs–Wolfe (ISW) effect [37–
44]. These probes depend on line–of–sight integrals over
evolving gravitational potentials and are therefore sensitive only indirectly to the underlying perturbation dynamics. As a result, large regions of EFT parameter
space, particularly those governing the kinetic structure
and propagation speed of scalar perturbations, remain
effectively unconstrained.
In a recent work [45], we proposed a qualitatively new
observational route to the microphysics of cosmic acceleration by showing that a lunar interferometer setup like
the Lunar Interferometer for Laser Astronomy (LILA)
[46] can directly probe the dark energy sound speed c2s
through real time measurements of horizon-scale scalar
gravitational potentials in an ultra-low frequency band
inaccessible from Earth. Treating dark energy both as a
general fluid and within the EFT of cosmic acceleration,
we showed that the sound speed c2s governs clustering on
scales k ≲ aH/cs , inducing characteristic scale and time
dependent modifications of the gravitational potentials
(Φ, Ψ) that map directly into an interferometric strain
signal. We developed a likelihood and Fisher-forecast
framework based on mock strain spectra demonstrating
that lunar interferometry can achieve discovery level sensitivity to clustering dark energy (c2s ≪ 1) or exclude
broad classes of perturbative models.
In this work, we take that line of thought forward and

## PDF page 2

2
propose a qualitatively new observational avenue wherein
direct measurements of the real–time evolution of horizon–scale metric perturbations using LILA provide direct sensitivity to the operators in the EFT action that
control the kinetic term and gradient energy of dark energy fluctuations, and by probing the time dependence
of large scale gravitational potentials, a lunar–based interferometer can access precisely those sectors of parameter space that are invisible to traditional background
and integrated probes. We show that this approach enables direct tests of the stability conditions, clustering
behavior and propagation speed of dark energy perturbations, independent of assumptions about ultraviolet completions. In particular, constraints on the strain induced
by evolving horizon–scale potentials can be translated
into bounds on c2s within the EFT framework. Our results therefore illustrate how next–generation precision
measurements of metric fluctuations in the Solar System
can open a new window onto the microphysics of cosmic
acceleration.
EFFECTIVE FIELD THEORY OF DARK
ENERGY

A systematic and model–independent description of
dark energy and modified gravity is provided by the
effective field theory (EFT) of cosmic acceleration [6].
In unitary gauge, where fluctuations of the dark energy scalar are absorbed into the metric, the action can
be written as an expansion in operators consistent with
time–dependent spatial diffeomorphism invariance. At
lowest order in fluctuations, the action takes the form
[
∫
M∗2
4 √
R − Λ(t) − c(t)g 00 +
S = d x −g
2
]
M24 (t)
00 2
(δg ) + · · · ,
2

speed of dark energy perturbations is
c2s =

c(t)
.
c(t) + 2M24 (t)

(2)

This expression makes the physical interpretation transparent. When M24 = 0, one recovers c2s = 1, corresponding to a canonical scalar field with luminal propagation and negligible clustering on sub-horizon scales.
For M24 > 0, the sound speed is reduced, c2s < 1, allowing dark energy perturbations to cluster more efficiently
on large scales. In the regime M24 ≫ c(t), the scalar sector becomes strongly kinetically screened: fluctuations
acquire large inertia, their propagation speed becomes
small, and the field can cluster significantly on horizon
scales.
Crucially, because M24 enters only at quadratic order in
perturbations, it leaves the background expansion history
essentially unchanged. As a result, it is largely invisible
to distance–based probes such as supernova luminosity
distances or baryon acoustic oscillations. Existing constraints on M24 , and therefore on c2s , arise mainly from
integrated effects in the evolution of gravitational potentials, most notably the late–time Integrated Sachs–Wolfe
(ISW) effect. These constraints are indirect and remain
comparatively weak, leaving broad regions of parameter
space unconstrained.
The EFT framework can be extended beyond this minimal truncation. In full generality, additional operators
consistent with the residual symmetries may be included,
such as couplings between the lapse perturbation and the
extrinsic curvature, or quadratic combinations of curvature fluctuations:
[
∫
M∗2 (t)
M 4 (t)
4 √
R−Λ(t)−c(t)g 00 + 2 (δg 00 )2
S = d x −g
2
2
]
( 2
)
m33 (t) 00
2
ij
−
δg δK + µ2 (t) δK − δKij δK + · · · , (3)
2

(1)

where M∗2 is the (possibly time–dependent) Planck mass,
Λ(t) and c(t) determine the background evolution, and
M24 (t) multiplies the leading quadratic operator in lapse
perturbations.
Among these coefficients, M24 (t) plays a particularly
important physical role. While Λ(t) and c(t) are fixed by
the requirement of reproducing the desired background
expansion history, the operator (δg 00 )2 does not contribute to the homogeneous dynamics at leading order.
Instead, it controls the kinetic structure of scalar perturbations. In this sense, M24 governs the inertia of dark
energy fluctuations and directly determines their propagation and clustering properties.
In the minimal truncation where (δg 00 )2 provides the
dominant modification to the scalar sector, the sound

where δKij denotes perturbations of the extrinsic
curvature and the ellipsis represents higher–order or
higher–derivative operators. Although these terms do
not modify the background evolution at leading order,
they can significantly alter the dynamics of scalar perturbations through kinetic mixing (“braiding”) with the
metric and through modified gradient structures.
Restoring time diffeomorphism invariance via the
Stückelberg field π, defined by the transformation t →
t + π(xµ ), and expanding to quadratic order in perturbations, one obtains an effective action for the single propagating scalar degree of freedom after integrating out the
non-dynamical lapse and shift. The quadratic action can
always be written in the form
[
]
∫
Beff (t)
2
(2)
3
3
2
S = dt d x a Aeff (t) ζ̇ −
(∇ζ) , (4)
a2

## PDF page 3

3
where ζ is the gauge–invariant curvature perturbation.
The coefficients Aeff and Beff depend on the full set of
EFT functions, the Hubble rate, and the matter content.
In this general setting, the physical sound speed is defined invariantly as
c2s =

Beff (t)
.
Aeff (t)

(5)

The sound speed therefore emerges as the ratio of gradient energy to kinetic energy in the scalar sector. The operator M24 (δg 00 )2 primarily enhances Aeff , increasing the
kinetic weight of fluctuations and reducing c2s . Braiding
operators proportional to δg 00 δK and curvature combinations can modify both Aeff and Beff through mixing
with metric perturbations.
The simple expression in Eq. (2) is recovered when
(δg 00 )2 dominates the scalar dynamics and mixing effects are subleading, as occurs in the decoupling limit or
in scenarios where braiding operators are independently
constrained by gravitational wave and large–scale structure data. In this regime, M24 provides a transparent and
physically intuitive parameterization of deviations from
canonical dark energy.
From an observational standpoint, probes sensitive to
the real–time evolution of gravitational potentials on
horizon scales are directly sensitive to the effective sound
speed and therefore to M24 . In contrast, background measurements constrain only Λ(t) and c(t). Direct measurements of time–dependent scalar metric perturbations are
therefore essential to access this otherwise hidden sector
of the EFT parameter space. This motivates the use of
precision interferometric measurements of horizon–scale
strain, which can probe the kinetic operator governing
dark energy perturbations and significantly improve constraints on their propagation and clustering properties.
HORIZON-SCALE METRIC FLUCTUATIONS AS
AN EFT PROBE

At the perturbative level, dark energy can be described
by an equation of state w and a rest-frame sound speed
c2s , which controls the response of pressure perturbations
to density fluctuations. Combining energy–momentum
conservation with the Einstein equations, the linear evolution of the dark energy density contrast δDE in Fourier
space obeys schematically
)
( 2 2
cs k
− 4πGρ δDE = S(k, t),
δ̈DE + (1 − 3w)H δ̇DE +
a2
(6)
where S(k, t) encodes metric and matter source terms.
The term proportional to c2s k 2 /a2 represents pressure
support, while gravity drives clustering. The competition between these effects defines a Jeans scale,
kJ ∼

aH
,
cs

(7)

which separates regimes of smooth and clustering behavior. For k ≫ kJ , pressure gradients suppress perturbations and dark energy remains effectively homogeneous.
For k ≲ kJ , pressure support is inefficient and dark
energy can cluster gravitationally. When c2s ≪ 1, the
Jeans scale approaches the Hubble scale, allowing dark
energy perturbations to survive and evolve on horizonsized modes at late times.
The observational consequences are most transparent
in Newtonian gauge,
]
[
ds2 = a2 (τ ) −(1 + 2Φ)dτ 2 + (1 − 2Ψ)d⃗x2 , (8)
where Φ and Ψ denote scalar metric potentials. On large
scales, their evolution is governed by the generalized Poisson equation,
k 2 Φ + 3a2 H(Φ̇ + HΦ) ∝ a2 (δρm + δρDE ) .

(9)

If c2s ≃ 1, dark energy perturbations are suppressed and
Φ decays in the standard manner during cosmic acceleration. In contrast, for c2s ≪ 1, dark energy clusters on
horizon scales, contributing dynamically to the source
term and modifying both the amplitude and time dependence of Φ. This constitutes a genuine real-time alteration of metric evolution, rather than a purely line-ofsight integrated effect.
Within the EFT framework, this behavior is controlled
primarily by the kinetic operator M24 (δg 00 )2 , which sets
the effective sound speed. Small c2s (large M24 ) enhances
the persistence of horizon-scale potential fluctuations.
Since M24 does not affect the background expansion at
leading order, accessing it observationally requires direct
sensitivity to the time evolution of scalar metric perturbations.
A lunar laser interferometer provides precisely such access. Scalar metric fluctuations induce differential redshifts across a macroscopic baseline, generating an effective strain
heff (t) ≃

∆Φ(t)
,
c2

(10)

where ∆Φ(t) is the potential difference sampled by the
interferometer arms. In the ultra low frequency band
f ∼ 10−7 − 10−3 Hz,

(11)

these measurements correspond to horizon-scale modes,
largely inaccessible to terrestrial interferometers and only
indirectly probed by large-scale structure or CMB observations. In the frequency domain, the strain power spectrum traces the potential power spectrum at k ≃ 2πf /c,
Ph (f ) ∝ PΦ (k).

(12)

Because PΦ (k) at horizon scales is directly influenced by
the clustering properties of dark energy, measurements

## PDF page 4

4
of ultra–low–frequency strain provide sensitivity to the
EFT kinetic sector. In this way, a lunar interferometer
probes M24 not through background expansion or integrated signatures, but through the real-time evolution of
scalar gravitational potentials. This makes it orthogonal
and complementary to traditional cosmological probes,
offering a direct observational handle on the perturbative microphysics of dark energy.
MOCK STRAIN POWER SPECTRA

To forecast the sensitivity of a lunar laser interferometer to EFT parameters, we construct mock strain
power spectra sourced by cosmological scalar perturbations. Throughout, we assume a fiducial ΛCDM background with Ωm = 0.3, ΩDE = 0.7, and w = −1, and
evolve linear perturbations in the presence of a dark energy component with sound speed c2s . The evolution
of the Newtonian potential Φ(k, τ ) follows from the linearized Einstein equations and energy–momentum conservation. The qualitative behavior is controlled by the
sound horizon (Jeans scale kJ ). For modes with k ≪ kJ ,
pressure gradients are negligible and Φ remains approximately constant at late times. For k ≫ kJ , pressure
support suppresses dark energy perturbations, leading to
oscillatory and decaying solutions for Φ.
Because the evolution equation is linear, the full solution can be written as
Φ(k, τ ) = Φprim (k) TΦ (k, c2s ),

(13)

where Φprim (k) is the primordial potential generated during inflation and TΦ is a transfer function encoding latetime scale dependence. A simple analytic form that reproduces the correct asymptotic limits is
TΦ (k, c2s ) ≃

1
(
)2 .
cs k
1+
aH

(14)

For c2s ∼ 1, clustering is suppressed on horizon scales,
while for c2s ≪ 1 the suppression scale shifts to large k,
enhancing power at low frequencies.
The potential power spectrum then follows from
PΦ (k, τ ) = TΦ2 (k, c2s ) PΦprim (k),

(15)

where PΦprim (k) is the primordial spectrum. Scalar metric
fluctuations induce differential redshifts across an interferometer baseline, producing an effective strain h ∝ Φ.
In the long-wavelength limit relevant for a lunar detector, the response is coherent across the arms and can be
absorbed into an overall normalization. The strain power
spectrum is therefore Ph (f ) = |R(f )|2 PΦ (k), where R(f )
denotes the (orientation-averaged) detector response.
In a recent work [45], we derived representative mock
spectra for c2s = 1 and c2s = 10−2 over the frequency range

10−7 –10−3 Hz, wherein it was shown how the spectra
can exhibit approximate power-law behavior set by the
primordial spectrum and the large-scale transfer function while at high frequencies (k ≫ kJ ), all curves converge because dark energy perturbations are pressure
supported and the potential is dominated by matter fluctuations. At low frequencies near the horizon scale, however, small c2s enhances clustering, producing significant
excess power in Ph (f ).
This scale dependent transition is the key observable signature in our current investigation as well as
ultra–low–frequency strain directly traces the soundhorizon imprint in TΦ , and therefore provides sensitivity
to the EFT kinetic parameter M24 that controls c2s . A lunar laser interferometer operates precisely in this regime,
making it uniquely suited to constrain dark energy microphysics through horizon-scale metric fluctuations.
FORECAST METHODOLOGY

We now describe the statistical framework used to
quantify the sensitivity of a lunar laser interferometer to
the sound speed of dark energy and the underlying EFT
parameters. The primary observable is the strain power
spectrum, Ph (f ), which is determined by the scalar potential power spectrum and therefore by the EFT kinetic
sector. For a parameter vector θ = {c2s , w, ΩDE , . . .}, the
theory predicts a strain spectrum Phth (f ; θ). The mapping from interferometric observables to EFT parameters
proceeds as follows: EFT coefficients (such as M24 ) determine the effective sound speed c2s as described in previous
sections; c2s fixes the transfer function TΦ (k, c2s ) governing
horizon-scale metric fluctuations; and TΦ sets the frequency dependence of Ph (f ) through k = 2πf /c. The
likelihood therefore directly connects measured strain
power to the EFT kinetic operator.
Assuming Gaussian, stationary fluctuations, the likelihood for an estimated spectrum P̂h (f ) is approximated
as Gaussian in power-spectrum space,
[
]2
th
1 ∑ P̂h (f ) − Ph (f ; θ)
,
(16)
ln L(θ) = −
2
σh2 (f )
f

where σh (f ) denotes the variance in each frequency bin,
determined by instrumental noise and observation time.
To forecast parameter sensitivity prior to data acquisition, we use the Fisher information matrix,
Fij =

∑

1

f

σh2 (f )

∂Phth (f ) ∂Phth (f )
,
∂θi
∂θj

(17)

evaluated at a fiducial cosmology.
The inverse
Fisher matrix approximates the parameter covariance,
Cov(θi , θj ) ≃ (F −1
√)ij , so that the marginalized uncertainty is σ(θi ) = (F −1 )ii . The Fisher matrix serves

## PDF page 5

5

FIG. 1. Fisher contour ellipses in the (M̃24 , c2s ) plane for
a lunar laser interferometer, centered on the fiducial clustering dark energy model (w, c2s ) = (−1, 10−2 ). Shown are
the joint 1σ and 2σ confidence regions obtained using the
cosmology-calibrated mock strain power spectrum mapped
onto the EFT phase space. Λ(t) was chosen to reproduce the
desired ΛCDM-like evolution, and the braiding and extrinsiccurvature coefficients were held fixed, consistent with existing gravitational-wave propagation and large-scale structure
bounds.

FIG. 2. Fisher contour ellipses in the (M̃24 , c2s ) plane for a
lunar laser interferometer, centered on the fiducial clustering
dark energy model (w, c2s ) = (−1, 10−2 ). Shown are the joint
1σ and 2σ confidence regions obtained using the cosmologycalibrated mock strain power spectrum mapped onto the EFT
phase space. A Gaussian prior is assumed for the equationof-state parameter, restricting it to within 3% of w = −1,
the braiding parameter is allowed to vary freely, and no additional constraints are imposed on the parameters governing
the background expansion history.

three purposes: (i) forecasting the precision with which
c2s can be measured; (ii) quantifying the statistical significance of deviations from the canonical value c2s = 1; and
(iii) identifying regions of EFT parameter space that can
be excluded at a given confidence level.
Given the absence of a finalized detector design,
we adopt a design-agnostic treatment of uncertainties.
In the ultra–low–frequency regime of interest, scalarinduced strain is coherent across the baseline, and we
approximate the variance using the standard Gaussian expression with an effective number of independent modes per bin. This signal-focused approach isolates the intrinsic cosmological information content of
horizon-scale strain measurements and yields conservative, implementation-independent forecasts. More detailed noise modeling can be incorporated straightforwardly once a specific lunar interferometer configuration
is defined, without altering the conceptual mapping between interferometric observables and EFT parameters
established here.

flects a partial degeneracy between the kinetic normalization of the scalar degree of freedom and its effective propagation speed. In the unitary-gauge EFT, the
operator M24 (δg 00 )2 modifies the kinetic coefficient of
the Goldstone mode associated with broken time diffeomorphisms, while c2s is determined by the ratio of
gradient to kinetic terms in the quadratic action for
scalar perturbations. When the braiding and extrinsiccurvature operators are fixed to values independently
constrained by gravitational-wave and large-scale structure data, varying M̃24 primarily rescales the kinetic normalization, whereas c2s controls the location of the spectral turnover associated with dark energy clustering. Because the observable strain spectrum is most sensitive
to this turnover scale, a change in M̃24 can partially compensate a shift in c2s by adjusting the overall amplitude of
the scalar response without substantially altering the frequency at which the spectrum departs from the smoothΛCDM limit. This compensation produces the characteristic elongated contour, indicating that the experiment
constrains a particular linear combination of EFT parameters more tightly than each parameter individually. The
Fisher contours shown in Figure 1 were generated assuming the background expansion was fixed to w ≃ −1, while
Λ(t) was chosen to reproduce the desired ΛCDM-like evolution. The braiding and extrinsic-curvature coefficients
were held fixed, consistent with existing gravitationalwave propagation and large-scale structure bounds. The
orientation of the degeneracy direction is directly influenced by braiding. In the general EFT, the scalar sound
eff (t)
speed can schematically be written as c2s = B
Aeff (t) where

EFT CONSTRAINTS AND PARAMETER SPACE

Figure 1 shows the illustrative Fisher contour ellipses
in the (M̃24 , c2s ) plane centered on the fiducial model with
c2s = 10−2 , including the 1σ and 2σ joint confidence regions. The parameter M̃24 is the standard dimensionM4
less EFT normalization M̃24 = M 2 2H 2 . The elongated
Pl

0

shape of the Fisher contours in the (M̃24 , c2s ) plane re-

## PDF page 6

6
Beff and Aeff denote effective gradient and kinetic coefficients. Nonzero braiding mixes metric and scalar fluctuations, modifying both numerator and denominator and
thereby rotating the principal degeneracy direction in parameter space. By fixing braiding parameters, the contours shown here isolate the degeneracy associated purely
with the kinetic normalization versus propagation speed.
The Fisher contour analysis shown in Fig. 2 has been
updated to include a Gaussian prior on the dark energy
equation-of-state parameter, restricting it to within 3% of
w = −1. This prior reflects one of the tightest commonly
cited constraints from a single, coherent global analysis
in the final Planck 2018 cosmological-parameter release,
when combined with baryon acoustic oscillations and
Type Ia supernovae data [47]. Additionally, the braiding
parameter is allowed to vary freely, and no constraints are
imposed on the parameters governing the background expansion history. Consequently, all EFT parameters are
treated as free, which generically broadens the sensitivity
contours and increases their tilt, reflecting enhanced degeneracies and compensatory effects between mixing and
sound-speed contributions.
The finite width of the contours along the c2s direction directly encodes the interferometer’s sensitivity to
the clustering properties of dark energy. The fact that
the 1σ and 2σ regions occupy only a restricted range in c2s
demonstrates that the measurement is not merely sensitive to an overall amplitude rescaling, but to the dynamical propagation of the scalar perturbations themselves.
In particular, models with c2s ≪ 1 generate a distinct
low-frequency enhancement in the strain spectrum that
cannot be fully mimicked by varying M̃24 alone. Consequently, a clustering fiducial model (e.g., c2s = 10−2 ) lies
well separated from the canonical smooth dark energy
limit c2s = 1 under the assumed signal dominated conditions, indicating that strongly clustering dark energy
would be statistically distinguishable from the smooth
ΛCDM case.
Most importantly, the contour geometry demonstrates
that the lunar interferometer forecast is genuinely probing the kinetic sector of the EFT rather than simply its
background expansion parameters. The constraints on
M̃24 imply a direct bound on the coefficient of the (δg 00 )2
operator, thereby placing limits on the kinetic normalization of the Goldstone mode associated with broken
time translations. The comparatively tighter constraint
along the c2s direction shows that the experiment is especially sensitive to the propagation speed of dark energy
fluctuations, establishing that interferometric strain measurements provide a direct observational handle on the
microphysical structure of the dark energy EFT. In this
sense, the contours represent not merely a phenomenological constraint, but a quantitative bound on the underlying kinetic operators governing scalar perturbations
in the effective theory.
Figure 3 presents a corresponding Fisher contour plot

FIG. 3. Fisher contour ellipses in the (M̃24 , c2s ) plane for a
lunar laser interferometer, centered on the fiducial clustering dark energy model (w, c2s ) = (−1, 10−2 ), with all EFT
parameters allowed to vary freely in the likelihood analysis.
Shown are the joint 1σ and 2σ confidence regions obtained
using the cosmology-calibrated mock strain power spectrum
mapped onto the EFT phase space.

in the (M̃24 , c̃) plane, where c̃ ≡

c(t)
2 H2 ,
MPl
0

centered on

the fiducial clustering dark energy model (w, c2s ) =
(−1, 10−2 ), with all EFT parameters allowed to vary
freely in the likelihood analysis. The elongated shape
of the Fisher contours in the (M̃24 , c̃) plane reflects the
intrinsic relation between the background EFT function
c̃ and the kinetic operator M̃24 that together determine
the scalar sound speed. In the unitary-gauge EFT, c̃ sets
the normalization of ρDE + pDE and therefore controls
the background departure from exact de Sitter expansion, while M̃24 modifies the kinetic coefficient of scalar
perturbations. Because the observable strain spectrum
is primarily sensitive to the combination that fixes the
clustering scale, variations in c̃ can be partially compensated by correlated shifts in M̃24 that preserve c2s , leading
to a positively correlated and elongated contour.
The finite width of the contours along the c̃ direction
demonstrates that the interferometric measurement does
not merely constrain the sound speed, but also places
a direct bound on the background EFT coefficient that
controls the normalization of scalar fluctuations. In particular, the restricted extent of the 1σ and 2σ regions
implies that large deviations in c̃—and hence large departures from the canonical ΛCDM kinetic structure—would
produce spectrally distinguishable signatures in the lowfrequency strain power. The contour geometry therefore
indicates that a lunar interferometer can probe both the
kinetic normalization and the background coupling encoded in c̃, providing a quantitative constraint on the
operator multiplying g 00 in the dark energy effective field
theory. This establishes sensitivity not only to the propagation speed of fluctuations, but also to the underlying
background EFT parameter governing the scalar sector.

## PDF page 7

7
DISCUSSION AND CONCLUSIONS

We have demonstrated that horizon-scale metric fluctuations provide a direct and model-independent observational probe of the kinetic sector of the effective field
theory (EFT) of dark energy. By constraining the operator M24 and its associated scalar sound speed c2s , interferometric measurements access a sector of dark energy
physics that is effectively invisible to traditional cosmological probes based solely on background expansion or
sub-horizon structure growth. In the unitary-gauge EFT
description, M24 controls the normalization of the kinetic
operator (δg 00 )2 , while the function c(t) governs the departure from exact de Sitter evolution. The combination
of these coefficients determines the propagation and clustering properties of the scalar degree of freedom associated with broken time translations.
Our results establish that ultra-low frequency strain
measurements can constrain these EFT operators directly, without invoking a specific ultraviolet (UV) completion or committing to a particular microphysical dark
energy model. This is a crucial conceptual advance:
rather than testing individual scalar-field Lagrangians or
phenomenological parameterizations, interferometric observations probe the symmetry structure and operator
content of the most general low-energy theory consistent
with covariance and broken time diffeomorphisms. The
measurement constrains the coefficients of the EFT itself,
not merely derived phenomenological quantities.
Importantly, the forecasted contours show that
strongly clustering dark energy models (c2s ≪ 1) are spectrally distinguishable from the canonical smooth limit
c2s = 1. The ability to bound M24 simultaneously demonstrates sensitivity to the kinetic normalization of scalar
perturbations, establishing that the observable is not
reducible to a background equation-of-state constraint.
The degeneracy structure in the (M̃24 , c2s ) and (M̃24 , c̃)
planes further shows that interferometric measurements
probe specific operator combinations predicted by the
EFT, enabling quantitative tests of the scalar sector’s
internal consistency.
More broadly, this work identifies a qualitatively new
avenue for testing the microphysical structure of cosmic
acceleration. While cosmic microwave background and
large-scale structure surveys constrain the background
expansion history and gravitational coupling, horizonscale interferometric observations probe the dynamical
response of spacetime itself to dark energy fluctuations.
This complementarity elevates interferometric cosmology
from a phenomenological probe to a fundamental test of
the EFT describing the late-time Universe.
In summary, we have shown that future lunar-scale
interferometers can place decisive constraints on the kinetic operators of dark energy, independently of any specific UV-complete construction. By directly bounding

M24 , c(t), and the associated sound speed, such experiments open an observational window onto the symmetrybreaking structure underlying cosmic acceleration, transforming dark energy from a purely background phenomenon into a testable sector of low-energy effective
field theory.
It is also important to discuss in passing what would be
the theoretical implications from such constraints. The
2
such
kinetic operator M24 (t)(δg 00
( ) and its companions
)
as m33 (t) δg 00 δK and µ22 (t) δK 2 − δKij δK ij are crucial
because they determine the perturbation sector microphysics of cosmic acceleration while remaining largely
invisible to background probes [7–11]. In the minimal
truncation, M(24 directly controls
the scalar sound speed
)
via c2s = c(t)/ c(t) + 2M24 (t) , so a measurement favoring
large M24 implies c2s ≪ 1 would mean that dark energy
is kinetically ”heavy” and clusters on near-horizon scales
while its EFT sits in a strongly non-canonical regime
whose UV completion must accommodate large higher
order operator weights (and potentially a lower strong
coupling scale) while still satisfying stability/consistency
conditions. Conversely, if the data drive these coefficients
small (like M24 ≈ 0 with weak braiding/curvature operators), then c2s ≈ 1 and the EFT reduces toward the canonical, weakly coupled quintessence-like limit, meaning the
derivative expansion is efficiently suppressed and additional δg operators are genuinely subleading. This would
be a strong hint that the UV completion flows to a simple
low energy scalar sector with minimal mixing and little
room for hidden perturbative structure [48, 49].
From the EFT viewpoint, the theoretical default expectation is that these operator coefficients are not fixed
by the background (since Λ(t) and c(t) set that), so without symmetry protection they are naturally allowed to
2
H 2 ) in dimensionful units, making direct conbe O(MPl
straints on their magnitude a decisive discriminator of
whether late time acceleration is a near-canonical, UV
kind sector or a strongly non-canonical EFT requiring
nontrivial UV structure.
Acknowledgements: We gratefully acknowledge support from Vanderbilt University and the U.S. National
Science Foundation. This work is supported in part by
NSF Award PHY-2411502 and by the Vanderbilt Discovery Doctoral Fellowship.

[1] A. G. Riess et al. (Supernova Search Team), Observational evidence from supernovae for an accelerating universe and a cosmological constant, Astron. J. 116, 1009
(1998), arXiv:astro-ph/9805201.
[2] M. Li, X.-D. Li, S. Wang, and Y. Wang, Dark Energy:
A Brief Review, Front. Phys. (Beijing) 8, 828 (2013),
arXiv:1209.0922 [astro-ph.CO].
[3] M. Li, X.-D. Li, S. Wang, and Y. Wang, Dark Energy,
Commun. Theor. Phys. 56, 525 (2011), arXiv:1103.5870

## PDF page 8

8
[astro-ph.CO].
[4] M. J. Mortonson, D. H. Weinberg, and M. White, Dark
Energy: A Short Review, (2013), arXiv:1401.0046 [astroph.CO].
[5] D. Huterer and D. L. Shafer, Dark energy two decades
after: Observables, probes, consistency tests, Rept.
Prog. Phys. 81, 016901 (2018), arXiv:1709.01091 [astroph.CO].
[6] N. Frusciante and L. Perenon, Effective field theory of
dark energy: A review, Phys. Rept. 857, 1 (2020),
arXiv:1907.03150 [astro-ph.CO].
[7] G. Gubitosi, F. Piazza, and F. Vernizzi, The effective
field theory of dark energy, Journal of Cosmology and
Astroparticle Physics 2013 (02), 032.
[8] E. V. Linder, G. Sengör, and S. Watson, Is the effective
field theory of dark energy effective?, Journal of Cosmology and Astroparticle Physics 2016 (05), 053.
[9] J. Bloomfield, É. É. Flanagan, M. Park, and S. Watson,
Dark energy or modified gravity? an effective field theory approach, Journal of Cosmology and Astroparticle
Physics 2013 (08), 010.
[10] J.-H. Liang, Y. Liao, X.-D. Ma, and H.-L. Wang, Dark
sector effective field theory, Journal of High Energy
Physics 2023, 1 (2023).
[11] N. Frusciante, M. Raveri, and A. Silvestri, Effective field
theory of dark energy: a dynamical analysis, Journal of
Cosmology and Astroparticle Physics 2014 (02), 026.
[12] S. Vagnozzi, L. Visinelli, P. Brax, A.-C. Davis, and
J. Sakstein, Direct detection of dark energy: The
XENON1T excess and future prospects, Phys. Rev. D
104, 063023 (2021), arXiv:2103.15834 [hep-ph].
[13] S. A. Adil, U. Mukhopadhyay, A. A. Sen, and
S. Vagnozzi, Dark energy in light of the early JWST observations: case for a negative cosmological constant?,
JCAP 10, 072, arXiv:2307.12763 [astro-ph.CO].
[14] E. Di Valentino, S. Gariazzo, O. Mena, and S. Vagnozzi,
Soundness of Dark Energy properties, JCAP 07 (07),
045, arXiv:2005.02062 [astro-ph.CO].
[15] S. Nojiri and S. D. Odintsov, Unified cosmic history
in modified gravity: from F(R) theory to Lorentz
non-invariant models, Phys. Rept. 505, 59 (2011),
arXiv:1011.0544 [gr-qc].
[16] S. Nojiri and S. D. Odintsov, Introduction to modified
gravity and gravitational alternative for dark energy,
eConf C0602061, 06 (2006), arXiv:hep-th/0601213.
[17] B. Gumjudpai, T. Naskar, M. Sami, and S. Tsujikawa,
Coupled dark energy: towards a general description of
the dynamics, Journal of Cosmology and Astroparticle
Physics 2005 (06), 007.
[18] A. Gómez-Valent, V. Pettorino, and L. Amendola, Update on coupled dark energy and the h 0 tension, Physical
Review D 101, 123513 (2020).
[19] B. J. Barros, Kinetically coupled dark energy, Physical
Review D 99, 064051 (2019).
[20] J.-Q. Xia, Constraint on coupled dark energy models
from observations, Physical Review D—Particles, Fields,
Gravitation, and Cosmology 80, 103514 (2009).
[21] A. V. Macciò, C. Quercellini, R. Mainini, L. Amendola,
and S. A. Bonometto, Coupled dark energy: Parameter
constraints from n-body simulations, Physical Review D
69, 123516 (2004).
[22] C. Armendariz-Picon, V. Mukhanov, and P. J. Steinhardt, Essentials of k-essence, Physical Review D 63,

103510 (2001).
[23] M. Malquarti, E. J. Copeland, A. R. Liddle, and M. Trodden, A new view of k-essence, Physical Review D 67,
123503 (2003).
[24] C. Armendariz-Picon and E. A. Lim, Haloes of k-essence,
Journal of Cosmology and Astroparticle Physics 2005
(08), 007.
[25] C. Ahn, C. Kim, and E. V. Linder, Dark energy properties in dbi theory, Physical Review D—Particles, Fields,
Gravitation, and Cosmology 80, 123016 (2009).
[26] L. P. Chimento, R. Lazkoz, and I. Sendra, Dbi models for
the unification of dark matter and dark energy, General
Relativity and Gravitation 42, 1189 (2010).
[27] R.-G. Cai and S.-J. Wang, Dark matter superfluid and
dbi dark energy, Physical Review D 93, 023515 (2016).
[28] S. Chattopadhyay and U. Debnath, Interaction between
dbi-essence and other dark energies, International Journal of Theoretical Physics 49, 1465 (2010).
[29] G. Calcagni and A. R. Liddle, Tachyon dark energy
models: Dynamics and constraints, Physical Review
D—Particles, Fields, Gravitation, and Cosmology 74,
043528 (2006).
[30] J. Bagla, H. K. Jassal, and T. Padmanabhan, Cosmology
with tachyon field as dark energy, Physical Review D 67,
063504 (2003).
[31] E. J. Copeland, M. R. Garousi, M. Sami, and S. Tsujikawa, What is needed of a tachyon if it is to be the dark
energy?, Physical Review D—Particles, Fields, Gravitation, and Cosmology 71, 043003 (2005).
[32] S. M. Micheletti, Observational constraints on holographic tachyonic dark energy in interaction with dark
matter, Journal of Cosmology and Astroparticle Physics
2010 (05), 009.
[33] A. Sheykhi, M. Sadegh Movahed, and E. Ebrahimi,
Tachyon reconstruction of ghost dark energy, Astrophysics and Space Science 339, 93 (2012).
[34] J. Kehayias and R. J. Scherrer, New generic evolution for
k -essence dark energy with w ≈ −1, Phys. Rev. D 100,
023525 (2019), arXiv:1905.05628 [gr-qc].
[35] T. Chiba, S. Dutta, and R. J. Scherrer, Slow-roll kessence, Phys. Rev. D 80, 043517 (2009), arXiv:0906.0628
[astro-ph.CO].
[36] R. Das, T. W. Kephart, and R. J. Scherrer, Tracking quintessence and k-essence in a general cosmological
background, Phys. Rev. D 74, 103515 (2006), arXiv:grqc/0609014.
[37] S. Hannestad, Constraints on the sound speed of dark
energy, Phys. Rev. D 71, 103519 (2005), arXiv:astroph/0504017.
[38] R. de Putter, D. Huterer, and E. V. Linder, Measuring
the speed of dark: Detecting dark energy perturbations,
Physical Review D—Particles, Fields, Gravitation, and
Cosmology 81, 103513 (2010).
[39] G. Ballesteros and J. Lesgourgues, Dark energy with nonadiabatic sound speed: initial conditions and detectability, Journal of Cosmology and Astroparticle Physics
2010 (10), 014.
[40] M. S. Linton, A. Pourtsidou, R. Crittenden, and
R. Maartens, Variable sound speed in interacting dark
energy models, Journal of Cosmology and Astroparticle
Physics 2018 (04), 043.
[41] R. Bean and O. Dore, Probing dark energy perturbations:
the dark energy equation of state and speed of sound
as measured by wmap, Physical Review D 69, 083503

## PDF page 9

9
(2004).
[42] D. J. Eisenstein, Dark energy and cosmic sound, New
Astronomy Reviews 49, 360 (2005).
[43] O. Sergijenko and B. Novosyadlyj, Sound speed of scalar
field dark energy: weak effects and large uncertainties,
Physical Review D 91, 083007 (2015).
[44] Y. Yang, Q. Wang, X. Ren, E. N. Saridakis, and Y.F. Cai, Clustering in dynamical dark energy: observational constraints from desi, cmb, and supernovae, arXiv
preprint arXiv:2511.22478 (2025).
[45] A. Gurrola, R. J. Scherrer, and O. Trivedi, Probing the
Sound Speed of Dark Energy with a Lunar Laser Interferometer, (2026), arXiv:2601.22084 [astro-ph.CO].
[46] K. Jani, M. Abernathy, E. Berti, V. Boschi,
S. Chakrabarti, A. Cocoros, J. W. Conklin, T. Creighton,

S. Dell’Agnello, J.-C. Diels, et al., Laser interferometer lunar antenna (lila): Advancing the us priorities
in gravitational-wave and lunar science, arXiv preprint
arXiv:2508.11631 (2025).
[47] N. Aghanim, T. Ghosh, J. J. Bock, B. P. Crill, O. Doré,
S. R. Hildebrandt, G. Rocha, K. M. Górski, C. R.
Lawrence, S. Mitra, G. Roudier, and P. Collaboration,
Planck 2018 results. vi. cosmological parameters, Astronomy and Astrophysics 641, Art. No. A6 (2020).
[48] S. Melville and J. Noller, Positivity in the sky: Constraining dark energy and modified gravity from the uv,
Physical Review D 101, 021502 (2020).
[49] G. Narain and T. Li, Ultraviolet complete dark energy
model, Physical Review D 97, 083523 (2018).
