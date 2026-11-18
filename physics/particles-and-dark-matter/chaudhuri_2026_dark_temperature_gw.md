Source: https://arxiv.org/abs/2602.20760v1
PDF sha256: 35b1420ad603136b3e7fb1dddad14d43da375cfc1a14d18c953e859f7cf2bcda
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of chaudhuri_2026_dark_temperature_gw.pdf

Transcription of `chaudhuri_2026_dark_temperature_gw.pdf` in this directory, 13 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-13 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Dark Temperature Hierarchies and Gravitational Waves from the Electroweak Phase
Transition
Arnab Chaudhuri1, ∗
1

arXiv:2602.20760v1 [hep-ph] 24 Feb 2026

Department of Physics, School of Advanced Sciences,
Vellore Institute of Technology, Vellore, Tamil Nadu 632014, India.
We investigate the impact of a semi-decoupled dark sector with a temperature hierarchy relative
to the Standard Model plasma on the electroweak phase transition and its associated gravitational
wave signal. Working within a minimal Higgs-portal extension, we allow the dark sector to possess a higher temperature at the electroweak epoch while remaining consistent with cosmological
bounds on additional relativistic degrees of freedom. The temperature hierarchy modifies the thermal structure of the effective potential and alters nucleation dynamics without requiring large portal
couplings or extreme supercooling. Within the cosmologically allowed window, we find a monotonic
enhancement of the gravitational wave amplitude by more than an order of magnitude compared
to the standard thermal case, accompanied by a shift of the peak frequency within the millihertz
regime. The resulting stochastic background moves substantially closer to the projected sensitivity
of future space-based interferometers. Our results demonstrate that hidden-sector temperature hierarchies can leave observable imprints on electroweak-scale phase transitions even in minimal and
perturbative frameworks.

I.

INTRODUCTION

Phase transitions in the early Universe provide a powerful probe of physics beyond the Standard Model. In particular, a first-order electroweak phase transition (EWPT) would generate a stochastic gravitational wave background
potentially observable by space-based interferometers operating in the millihertz frequency range [1–5]. Because the
Standard Model predicts a smooth crossover for the observed Higgs mass, additional degrees of freedom are required
to realize a first-order transition [6–9]. Among the simplest and most extensively studied possibilities is the addition
of a gauge-singlet scalar coupled to the Higgs through a portal interaction [10–20].
Singlet extensions have been widely explored in the context of electroweak baryogenesis and gravitational wave
production [21–28]. In conventional analyses, the hidden sector is assumed to share a common temperature with the
Standard Model plasma during the electroweak epoch. Under this assumption, the thermal corrections entering the
finite-temperature effective potential are entirely determined by the visible-sector bath, and the resulting gravitational
wave signal depends sensitively on the detailed scalar spectrum and portal coupling.
However, the assumption of a common temperature is not generic. If a hidden sector decouples from the visible
sector at sufficiently high temperatures, entropy conservation in each sector implies that the two temperatures evolve
independently [29–33]. In such scenarios the dark-sector temperature at the electroweak epoch is not fixed a priori, but
becomes an additional cosmological parameter constrained primarily by bounds on extra relativistic energy density.
These bounds are commonly expressed in terms of ∆Neff and are tightly constrained by cosmic microwave background
and big bang nucleosynthesis data [34–37]. Hidden sectors with temperature hierarchies have been studied in a variety
of cosmological contexts, including dark radiation, freeze-in dark matter, and non-standard thermal histories [38–41].
Despite the extensive literature on singlet-driven electroweak phase transitions and gravitational waves, the effect
of a semi-decoupled temperature hierarchy on electroweak-scale gravitational wave phenomenology has not been
systematically quantified. A hotter dark bath modifies the thermal corrections to the effective potential, altering
both the quadratic and bosonic cubic temperature-dependent terms. Because these coefficients enter differently in the
determination of the critical temperature, the nucleation action, and the inverse duration parameter, even moderate
temperature hierarchies can significantly affect the latent heat parameter α, the inverse duration β/H, and the
nucleation temperature Tn . These quantities directly control the amplitude and peak frequency of the gravitational
wave spectrum [2–5, 9, 26–28, 42–67].
Recent years have seen substantial progress in understanding gravitational wave production from cosmological phase
transitions, including improved modeling of sound-wave dynamics and numerical simulations of bubble expansion
[5, 26, 47, 68, 69]. Planned space-based interferometers such as LISA, BBO, and DECIGO provide strong motivation
to revisit electroweak-scale transitions with refined theoretical tools [70–74]. In this context, it is timely to reassess
minimal scalar extensions under non-standard thermal histories that remain cosmologically viable.
∗ arnab.chaudhuri@vit.ac.in

## PDF page 2

2
In this work we investigate how a dark temperature hierarchy modifies the electroweak phase transition and its
gravitational wave signal within a minimal Higgs-portal extension of the Standard Model. We allow the dark sector
to possess a temperature TD = ξT during the electroweak epoch and determine the cosmologically allowed range
of ξ consistent with bounds on ∆Neff . We compute the finite-temperature effective potential including one-loop
thermal corrections and daisy resummation, and evaluate bubble nucleation numerically using CosmoTransitions
[75]. Focusing on perturbative portal couplings, we analyze how the phase transition parameters vary across the
allowed hierarchy window and compute the resulting gravitational wave spectra and their signal-to-noise ratio for
LISA.
We find that increasing the dark temperature ratio within cosmological bounds leads to a systematic enhancement
of the gravitational wave amplitude by more than an order of magnitude, together with a shift of the peak frequency
within the millihertz regime. The enhancement arises from modified nucleation dynamics induced by the hotter
dark bath and occurs within a perturbative and cosmologically consistent framework. Our results demonstrate that
hidden-sector temperature hierarchies can leave observable imprints on electroweak-scale phase transitions even in
minimal scalar portal models.
The paper is organized as follows. In Sec. II we introduce the Higgs-portal framework and discuss the cosmological
consistency conditions allowing a temperature hierarchy between the dark and visible sectors. In Sec. III we analyze
the electroweak phase transition dynamics and present the numerical results for the nucleation parameters. Sec. IV
is devoted to the resulting gravitational wave spectra and their comparison with projected detector sensitivities. We
conclude in Sec. V.
II.

MODEL AND COSMOLOGICAL CONSISTENCY

We consider the Standard Model (SM) extended by a real scalar singlet S interacting through a Higgs portal
coupling. Such extensions constitute one of the minimal frameworks for modifying electroweak phase transition
dynamics while preserving the SM gauge structure [15, 76, 77].
We impose a discrete Z2 symmetry under which
S → −S,

(1)

while all Standard Model fields remain even. This symmetry forbids linear and cubic singlet operators and ensures
that S = 0 is an extremum of the tree-level potential.
The scalar-sector Lagrangian is
1
1
λS 4 κ †
L = LSM + (∂µ S)2 − m2S0 S 2 −
S − H H S2,
2
2
4
2

(2)

where mS0 is the singlet mass parameter, λS the singlet quartic coupling, and κ the portal interaction strength.
Electroweak symmetry breaking proceeds along the Higgs direction provided
m2S0 +

κ 2
v > 0,
2

(3)

so that the singlet does not acquire a vacuum expectation value in the broken phase.
In unitary gauge,
( )
1 0
H=√
,
2 h
where h denotes the neutral Higgs field. The tree-level Higgs potential is
1
1
V0 (h) = − µ2 h2 + λh4 ,
2
4

(4)

with λ ≃ 0.13 fixed by mh = 125 GeV and v = 246 GeV. Along the Higgs background, the singlet field-dependent
mass is
κ
m2S (h) = m2S0 + h2 .
(5)
2
The electroweak phase transition is analyzed using the full one-loop finite-temperature effective potential including
Coleman–Weinberg corrections, thermal contributions, daisy resummation, and counterterms. Explicit expressions
and renormalization conditions are summarized in Appendix A.

## PDF page 3

3
For analytic intuition, the high-temperature expansion admits the approximate cubic form
Veff (h, T ) = Dξ (T 2 − T02 )h2 − Eξ T h3 +

λT 4
h .
4

(6)

The cubic term arises from the bosonic zero Matsubara modes in the high-temperature expansion of the thermal
integrals and generates the barrier between phases. It originates from gauge bosons and the singlet scalar and does
not violate the Z2 symmetry, since it is induced radiatively at finite temperature in the Higgs direction.
We allow the singlet sector to possess a temperature TD different from the SM temperature T , defining
ξ≡

TD
.
T

In the high-temperature limit,
κ 2
ξ ,
24
1 ( κ )3/2
Eξ = ESM +
ξ.
12π 2

Dξ = DSM +

(7)
(8)

2
The ξ 2 scaling originates from quadratic thermal corrections proportional to TD
, while the linear ξ dependence arises
from the bosonic zero-mode contribution to the cubic term [6]. Numerically, DSM ≃ 0.4 and ESM ≃ 0.01.
The singlet thermal mass entering ring resummation is

ΠS (TD ) =

κ 2 2
ξ T ,
12

(9)

which regulates infrared divergences from the zero mode [78]. All numerical results below are obtained from the full
one-loop resummed potential.
A temperature hierarchy requires that the singlet sector is not in thermal equilibrium with the SM plasma at the
electroweak epoch. The dominant portal-induced process is HH ↔ SS. At T ≫ mi ,
σ∼

κ2
,
T2

Γ ∼ κ2 T.

Comparing with the Hubble rate during radiation domination,
√
π 2 g∗ T 2
H(T ) =
,
90 MPl
decoupling occurs when Γ ≲ H, giving parametrically
κ2
Tdec ∼ √ MPl .
g∗

(10)

For κ ∼ O(1), this scale is far above the electroweak temperature, ensuring thermal decoupling during the phase transition. In deriving Eq. (10) we have assumed relativistic scattering in the symmetric phase, valid for temperatures well
above the electroweak scale. For portal couplings in the perturbative regime, κ ≲ O(1), the decoupling temperature
obtained from Γ ∼ H lies parametrically far above the electroweak scale, ensuring that the singlet sector is thermally
separated prior to the phase transition. Once decoupled, entropy conservation in each sector independently preserves
the temperature ratio ξ, up to the standard dilution from changes in the effective number of relativistic degrees of
freedom.
At temperatures near and below the electroweak scale, the Higgs field acquires a vacuum expectation value and
both Higgs and singlet states become massive. The number densities entering the portal-induced interaction rate
Γ ∼ n⟨σv⟩ are then Boltzmann suppressed, causing Γ to decrease more rapidly than the Hubble rate. Consequently,
thermal re-equilibration does not occur during or after the electroweak phase transition. The temperature hierarchy
therefore remains stable throughout the transition in the perturbative parameter region considered in this work.
Entropy conservation implies
(
ξBBN = ξEW

g∗,s (TBBN )
g∗,s (Tdec )

)1/3
.

(11)

## PDF page 4

4
Using g∗,s (Tdec ) ≃ 106.75 and g∗,s (TBBN ) ≃ 10.75, the dilution factor is approximately 0.46.
A relativistic real scalar contributes
( )4/3
4 11
4
ξBBN
,
∆Neff =
7 4

(12)

which must satisfy ∆Neff ≲ 0.3 [34, 36]. This implies
ξEW ≲ 1.8.

(13)

We therefore consider
1.0 ≤ ξ ≲ 1.8,
with perturbative portal couplings.
A.

Benchmark parameter choice and theoretical consistency

The Standard Model parameters are fixed by
mh = 125 GeV,

v = 246 GeV,

which determine λ ≃ 0.13 at the renormalization scale µR = v.
We fix
κ = 1,

λS = 0.5,

both within the perturbative regime.
We define the physical singlet mass in the broken phase as
m2S = m2S0 +

κ 2
v .
2

(14)

Throughout this work we adopt
mS = 250 GeV,
which avoids Higgs decay constraints and is consistent with current collider limits for a Z2 -odd singlet. This benchmark
value is chosen for several phenomenological and dynamical reasons. First, mS > mh /2 ensures that the decay
h → SS is kinematically forbidden, avoiding constraints from the Higgs invisible width for portal couplings of order
unity. Second, for an exact Z2 symmetry the singlet does not mix with the Higgs, and current collider searches place
only weak direct limits on a Z2 -odd scalar with mass in the few-hundred-GeV range and perturbative portal coupling.
Third, taking mS to be of the same order as the electroweak scale ensures that the singlet contributes appreciably
to thermal corrections in the effective potential without decoupling from the plasma dynamics or inducing extreme
supercooling.
We have verified that moderate variations of mS within the range 200–400 GeV do not qualitatively modify
the hierarchy-induced enhancement mechanism discussed below. The choice mS = 250 GeV should therefore be
understood as a representative benchmark within a broader perturbative parameter region rather than a finely tuned
point.
For κ = 1, this gives
1
m2S0 = m2S − v 2 ≃ (180 GeV)2 .
2
Vacuum stability requires
λ > 0,

λS > 0,

√
κ > −2 λλS ,

which are satisfied. Perturbativity is maintained since κ, λS ≪ 4π.
With the scalar sector specified, the only remaining continuous parameter controlling the thermal dynamics is the
temperature ratio ξ = TD /T . All phase transition and gravitational wave results presented below follow from this
fully specified and internally consistent benchmark realization.

## PDF page 5

5
ξ Tc (GeV) Tn (GeV)
α
β/H
1.0 96.55
89.23
0.046 308
1.2 93.20
86.19 0.0658 256
1.4 90.04
83.01
0.079 202
1.6 88.01
78.54
0.085 176
1.8 85.48
75.01
0.109 105

TABLE I: Phase transition parameters for κ = 1 and varying dark temperature ratio ξ = TD /T .

III.

ELECTROWEAK PHASE TRANSITION DYNAMICS

We now analyze the electroweak phase transition in the presence of a dark temperature hierarchy. The quantities
characterizing the transition are the critical temperature Tc , the nucleation temperature Tn , the latent heat parameter
α, and the inverse duration parameter β/H [4, 6].
The critical temperature is defined by the degeneracy condition between the symmetric minimum at h = 0 and the
broken minimum at h ̸= 0. Using the cubic parametrization of Eq. (6), this condition yields
Tc2 =

µ2
,
2Dξ − 2Eξ2 /λT

(15)

valid within the high-temperature approximation. This expression illustrates how the thermal coefficients Dξ and
Eξ control the onset of symmetry breaking. Since Dξ grows as ξ 2 while Eξ grows linearly in ξ, increasing the dark
temperature ratio modifies the balance between the quadratic and cubic terms, leading to a systematic shift in Tc .
For the benchmark choice κ = 1, a numerical determination based on the full one-loop resummed potential yields Tc
decreases from 96.5 GeV at ξ = 1 to 85.5 GeV at ξ = 1.8.
The phase transition completes when thermal tunnelling becomes efficient. The nucleation temperature Tn is defined
by the condition
S3 (Tn )
≃ 140,
Tn

(16)

which corresponds to approximately one bubble nucleated per Hubble volume in a radiation-dominated Universe [6].
Here S3 denotes the three-dimensional Euclidean action of the bounce solution computed along the Higgs direction.
We compute S3 (T ) numerically using CosmoTransitions, solving the overshoot/undershoot boundary value problem
for the full one-loop finite-temperature effective potential including ring resummation. In particular, the tunnelling
calculation does not rely on the cubic approximation of Eq. (6).
The strength and duration of the transition are characterized by the parameters
α=

]
[
d∆V
,
∆V − T
ρrad
dT T =Tn
1

β
d
=T
H
dT

(

)∣
S3 ∣∣
,
T ∣T =Tn

(17)

where ∆V ≡ Veff (hfalse , T ) − Veff (htrue , T ) is the difference in free energy density between the false and true vacua at
2
temperature T , and ρrad = π30 g∗ Tn4 is the radiation energy density with g∗ = 106.75. The parameter α measures the
fraction of vacuum energy released relative to the radiation background, while β/H quantifies the inverse duration of
the transition in units of the Hubble rate [4, 5].
We fix κ = 1 and vary ξ within the cosmologically allowed window 1 ≤ ξ ≤ 1.8. The numerical results obtained
from the full one-loop potential are summarized in Table I.
Several systematic trends emerge from the numerical analysis. The nucleation temperature decreases monotonically
as ξ increases, reflecting the modified thermal contributions to the effective potential. Simultaneously, the latent heat
parameter α increases across the allowed hierarchy window, while the inverse duration parameter β/H decreases
substantially. Between ξ = 1 and ξ = 1.8, α increases by more than a factor of two and β/H decreases by nearly a
factor of three.
The ratio Tn /Tc correspondingly decreases with increasing ξ, indicating progressively stronger supercooling within
the cosmologically allowed window, although the transition remains within a perturbative regime.
These correlated shifts in α and β/H play a central role in determining the amplitude and peak structure of the
stochastic gravitational wave background generated by the transition, which we analyze in the following section.

## PDF page 6

6

(a)

Inverse duration parameter /H

0.11

Latent heat parameter

0.10
0.09
0.08
0.07
0.06
0.05
0.04
1.0

1.1

1.2

1.3

1.4

1.5

1.6

Dark temperature ratio

1.7

1.8

300 (b)
275
250
225
200
175
150
125
100
1.0 1.1

1.2

1.3

1.4

1.5

1.6

Dark temperature ratio

1.7

1.8

FIG. 1: Dependence of (a) the latent heat parameter α and (b) the inverse duration parameter β/H on the dark
temperature ratio ξ = TD /T for κ = 1. Points denote numerical evaluations using the full one-loop effective
potential with ring resummation.

IV.

GRAVITATIONAL WAVE SIGNAL

A first-order electroweak phase transition generates a stochastic gravitational wave background through three
distinct mechanisms: scalar field gradients from bubble wall collisions, long-lasting acoustic waves in the plasma, and
magnetohydrodynamic turbulence [1, 4, 5, 52]. The total energy density may be schematically decomposed as
ΩGW (f ) = Ωcol (f ) + Ωsw (f ) + Ωturb (f ),

(18)

where Ωcol denotes the envelope (collision) contribution, Ωsw the acoustic component, and Ωturb the turbulent contribution.
For transitions in which bubble walls do not run away, numerical simulations indicate that the sound-wave contribution dominates the total signal, while the collision term is suppressed and turbulence provides a subleading correction
[5, 43, 44]. In the parameter region considered here, characterized by moderate α and β/H ≳ 100, runaway behavior
is not expected. We therefore focus on the acoustic contribution as the leading and most robust source of gravitational
radiation and neglect Ωcol and Ωturb in the quantitative predictions below.
Before presenting the predicted spectra, it is useful to summarize how the temperature hierarchy modifies the
macroscopic transition parameters entering the signal calculation. Figure 1 displays the dependence of the latent heat
parameter α and the inverse duration parameter β/H on the dark temperature ratio ξ for κ = 1. As ξ increases
within the cosmologically allowed window, α increases monotonically while β/H decreases substantially. Since the
gravitational wave amplitude scales with H∗ /β and with the released vacuum energy fraction, these correlated shifts
directly control both the normalization and the peak frequency of the signal.
The present-day gravitational wave energy density from long-lasting acoustic waves can be expressed as [4, 5]
Ωsw (f )h2 = 2.65 × 10−6

(

H∗
β

)(

κv α
1+α

)2 (

100
g∗

)1/3
vw Ssw (f ),

(19)

where H∗ is the Hubble rate at Tn , α is the ratio of released vacuum energy to radiation energy density, β/H∗
characterizes the inverse duration of the transition, g∗ is the number of relativistic degrees of freedom, vw is the
bubble wall velocity, and κv denotes the fraction of vacuum energy converted into bulk fluid motion.
We adopt the standard hydrodynamic fit appropriate for non-runaway walls,
κv ≃

α
√
.
0.73 + 0.083 α + α

Throughout this work we assume a representative subsonic wall velocity
vw = 0.6,

(20)

## PDF page 7

7

10 10

= 1.0
= 1.2
= 1.4
= 1.6
= 1.8

10 11
10 12

GWh 2

10 13
LISA

10 14
10 15
10 16

DECIGO

10 17
10 18 4
10

10 3

BBO

10 1

10 2
Frequency (Hz)

100

FIG. 2: Gravitational wave spectra for κ = 1 and varying dark temperature ratio ξ = TD /T . Increasing ξ enhances
the amplitude and shifts the peak toward lower frequencies.

consistent with deflagration solutions in moderately strong transitions and commonly adopted in phenomenological
studies.
The spectral shape function is given by
(
Ssw (f ) =

)3 [

f
fpeak

7
4 + 3(f /fpeak )2

]7/2
,

which reproduces the characteristic f 3 infrared rise and power-law decay at higher frequencies.
The peak frequency today is approximately
(
)(
)(
1
β
Tn
g∗ )1/6
−5
fpeak ≃ 1.9 × 10 Hz
.
v w H∗
100 GeV
100

(21)

(22)

Parametrically, the peak amplitude scales as
(
Ωpeak ∼

H∗
β

)(

α
1+α

)2
,

up to order-one factors associated with vw and the spectral shape. Increasing α while decreasing β/H∗ therefore
coherently enhances the signal.
Figure 2 displays the resulting spectra for the benchmark points listed in Table I. Across the allowed hierarchy
window, Tn decreases from 89 GeV to 75 GeV, α increases from 0.046 to 0.109, and β/H decreases from 308 to
105. These combined effects yield approximately a factor of ∼ 10 enhancement of the peak amplitude between
ξ = 1 and ξ = 1.8. The peak frequency remains in the millihertz regime, fpeak ∼ 10−3 –10−2 Hz, characteristic of
electroweak-scale transitions.

## PDF page 8

max = 1.8

8

SNR (LISA, 4 yr)

20

15
SNR = 10

10

SNR = 5

5

0

SNR = 1
1.0

1.1

1.2

1.3
1.4
1.5
Dark temperature ratio

1.6

1.7

1.8

FIG. 3: Signal-to-noise ratio for LISA (four-year mission) as a function of the dark temperature ratio ξ for κ = 1.
The shaded region indicates SNR ≥ 10. The vertical dashed line marks the cosmological bound ξmax = 1.8.
The enhancement mechanism arises from modified thermal coefficients induced by a hotter dark sector, which alter
the nucleation dynamics within a controlled perturbative regime.
Finally, Eq. (19) assumes that acoustic modes persist for approximately a Hubble time. Recent numerical simulations indicate that finite sound-wave lifetimes may introduce an O(1) suppression in the absolute normalization
[5, 44]. Such uncertainties affect the overall amplitude uniformly and do not modify the relative enhancement induced
by the temperature hierarchy. The monotonic amplification with increasing ξ therefore remains a robust qualitative
prediction of the framework.
A.

Signal-to-noise ratio and detectability

The gravitational wave spectra shown in Fig. 2 illustrate the hierarchy-induced enhancement. Experimental observability is quantified through the signal-to-noise ratio (SNR). For a stochastic background observed over time Tobs ,
the SNR is given by [5, 79]
[
]2
∫ fmax
ΩGW (f )
2
SNR = Tobs
df
,
(23)
Ωsens (f )
fmin
where Ωsens (f ) denotes the detector sensitivity curve expressed in energy-density units.
For LISA we adopt Tobs = 4 yr and use the publicly available sensitivity including instrumental and confusion
noise. Electroweak-scale transitions produce millihertz peaks (cf. Eq. (22)), placing the signal squarely within the
LISA band.
The resulting SNR as a function of ξ for κ = 1 is shown in Fig. 3. The shaded region corresponds to SNR ≥ 10, a
conservative criterion for robust detection.
The SNR increases steeply with ξ, reflecting the correlated evolution of α and β/H. The maximal benchmark yields
SNR ≃ 22, demonstrating that within cosmologically allowed bounds a moderate temperature hierarchy can elevate
an otherwise marginal electroweak signal into a robustly detectable regime.
Uncertainties in the sound-wave lifetime may introduce order-one normalization shifts [44], but do not alter the
monotonic growth with ξ. The qualitative conclusion remains stable.

## PDF page 9

9
V.

DISCUSSION AND CONCLUSIONS

We have investigated the impact of a semi-decoupled dark sector with temperature hierarchy TD /T ≡ ξ on the
electroweak phase transition and its associated gravitational wave signal. The framework is deliberately minimal: the
Standard Model is extended by a single real scalar singlet coupled through a Higgs portal interaction with perturbative
strength κ = 1. The dark sector is allowed to possess a higher temperature than the visible plasma at the electroweak
epoch while remaining consistent with cosmological bounds on ∆Neff .
The central result is that a temperature hierarchy modifies the thermal coefficients of the finite-temperature effective
potential in a controlled manner, thereby altering nucleation dynamics without requiring large portal couplings or
extreme supercooling. As the ratio ξ increases within the cosmologically allowed window 1 ≤ ξ ≲ 1.8, we find a
monotonic decrease in β/H, a systematic increase in the latent heat parameter α, and a corresponding reduction in
the nucleation temperature. These correlated effects enhance the peak gravitational wave amplitude by O(10) and
shift the signal toward lower frequencies at a few ×10−3 Hz.
To quantify experimental prospects, we compute the signal-to-noise ratio for LISA assuming a four-year mission.
While the thermally equilibrated case ξ = 1 yields SNR < 1, increasing the temperature hierarchy rapidly enhances
detectability. The SNR exceeds SNR = 5 for ξ ≳ 1.6 and reaches SNR ≃ 22 near the cosmological upper bound
ξ ≃ 1.8, corresponding to robust detection under conservative criteria. Within cosmologically allowed limits, a
moderate temperature hierarchy is therefore sufficient to move an otherwise marginal electroweak signal into the
observable regime of LISA.
The enhancement mechanism arises from modified thermal contributions to the quadratic and cubic terms of the
effective potential induced by the hotter dark bath. The analysis remains within a perturbative portal regime and
satisfies conservative bounds from ∆Neff after entropy dilution. Importantly, the improvement in detectability does not
rely on runaway bubble walls or extreme supercooling, but instead follows from controlled modifications of nucleation
dynamics.
The absolute normalization of the sound-wave contribution carries theoretical uncertainties associated with the
finite lifetime of acoustic modes in the plasma. Numerical simulations indicate potential O(1) corrections to the
amplitude [5, 44]. Such uncertainties rescale the overall SNR but do not alter its monotonic growth with ξ, and
therefore do not affect the qualitative conclusion regarding enhanced detectability.
More broadly, this study demonstrates that semi-decoupled dark sectors can materially influence electroweakscale gravitational wave phenomenology even in minimal scalar portal extensions. Cosmological temperature hierarchies—often neglected in phase transition analyses—can play a nontrivial role in determining nucleation dynamics
and observable signatures.
Several directions merit further investigation. A broader parameter scan including variation of the portal coupling
and singlet self-interaction would clarify the maximal achievable enhancement within perturbative limits. Embedding
the scenario in ultraviolet-complete dark sector models could connect the temperature hierarchy to specific reheating or
decoupling mechanisms. Finally, improved simulations of acoustic dynamics would reduce the theoretical uncertainty
in the predicted gravitational wave amplitude and sharpen forecasts for LISA.
In summary, a hotter dark bath consistent with cosmological bounds can enhance the electroweak gravitational
wave signal by O(10) relative to the thermally equilibrated case. For temperature hierarchies near the cosmological
upper limit, the resulting signal achieves robust detectability at LISA, illustrating that hidden-sector thermal histories
can leave observable imprints on cosmological phase transitions.

Appendix A: One-loop finite-temperature effective potential

In this appendix we summarize the explicit form of the effective potential used in the numerical analysis. All phase
transition quantities are computed from the full one-loop finite-temperature effective potential with ring (daisy)
resummation in Landau gauge within the MS renormalization scheme.
The effective potential is written as
Veff (h, T ) = V0 (h) + VCW (h) + VT (h, T ) + Vdaisy (h, T ) + Vct (h),
where the individual contributions are described below.

(A1)

## PDF page 10

10
1.

Tree-level scalar potential and field-dependent masses

The tree-level scalar potential in the background fields (h, S) is
1
1
λS 4 κ 2 2
1
S + h S ,
V0 (h, S) = − µ2 h2 + λh4 + m2S0 S 2 +
2
4
2
4
4
√ T
where h denotes the neutral Higgs field in unitary gauge, H = (0, h/ 2) .
Along the Higgs direction S = 0, the potential reduces to

(A2)

1
1
V0 (h) = − µ2 h2 + λh4 .
(A3)
2
4
The field-dependent masses entering the one-loop effective potential are obtained by expanding around the background Higgs field [6, 77]. They are given by
m2h (h) = −µ2 + 3λh2 ,

(A4)

m2G (h) = −µ2 + λh2 ,
g2
m2W (h) = h2 ,

(A5)

4
2
g
+ g ′2 2
h ,
m2Z (h) =
4
2
y
m2t (h) = t h2 ,
2
κ
m2S (h) = m2S0 + h2 .
2

(A6)
(A7)
(A8)
(A9)

Here mG denotes the Goldstone modes, g and g ′ are the electroweak gauge couplings, and yt is the top Yukawa
coupling.
The corresponding numbers of degrees of freedom contributing to the effective potential are
nh = 1,
nG = 3,
nW = 6,
nZ = 3,
nt = −12,
nS = 1,

(A10)
(A11)
(A12)
(A13)
(A14)
(A15)

where the negative sign for fermions accounts for Fermi–Dirac statistics. For gauge bosons, these multiplicities
correspond to transverse plus longitudinal polarizations at zero temperature.
These masses and multiplicities are used in the Coleman–Weinberg potential and in the finite-temperature corrections discussed below.
2.

Coleman–Weinberg potential

The one-loop zero-temperature correction is given by the Coleman–Weinberg potential,
[ ( 2
)
]
∑ ni
mi (h)
4
VCW (h) =
m (h) ln
− ci ,
64π 2 i
µ2R
i
where µR is the renormalization scale. In the MS scheme,
{
3
(scalars and fermions),
ci = 25
(gauge bosons).
6

(A16)

(A17)

All couplings entering Eq. (A16) are evaluated at the renormalization scale µR = v = 246 GeV, corresponding to the
physical electroweak vacuum expectation value.

## PDF page 11

11
3.

Finite-temperature corrections

The finite-temperature contribution is
VT (h, T ) =

)
( 2
mi (h)
T4 ∑
,
n
J
i ±
2π 2 i
T2

where J+ and J− correspond to bosons and fermions respectively,
∫ ∞
)]
[
( √
J± (y 2 ) =
dx x2 ln 1 ∓ exp − x2 + y 2 .

(A18)

(A19)

0

In the high-temperature limit, the bosonic integral contains a cubic term proportional to m3i T , which is responsible
for the barrier between phases through the contribution of bosonic zero Matsubara modes.
4.

Daisy (ring) resummation

Infrared divergences from bosonic zero modes are regulated by ring resummation [78, 80]. In practice, this amounts
to replacing
m2i (h) → m2i (h) + Πi (T )

(A20)

in the bosonic thermal functions for the longitudinal degrees of freedom.
The leading thermal masses are
)
3g 2 + g ′2
yt2
λ
κ 2
Πh (T ) = T
+
+ + ξ ,
16
4
2
12
κ 2
κ 2 2
T =
ξ T ,
ΠS (TD ) =
12 D
12
11 2 2
ΠW (T ) =
g T ,
6
11 2
ΠZ (T ) =
(g + g ′2 )T 2 .
6
2

(

(A21)
(A22)
(A23)
(A24)

Only bosonic longitudinal modes receive thermal mass corrections; transverse gauge modes do not acquire Debye
masses at leading order.
5.

Counterterm potential and renormalization

To preserve the physical Higgs vacuum expectation value and mass at zero temperature, we include a counterterm
potential. In the most general form consistent with the scalar sector,
1
δλS 4 δκ 2 2
Vct (h, S) = δµ2 h2 + δλh4 + δm2S S 2 +
S +
h S .
2
4
2

(A25)

In principle, all scalar parameters receive one-loop corrections. However, in the present analysis we restrict to the
background direction S = 0 and do not impose on-shell renormalization conditions for the singlet sector. The singlet
parameters m2S0 , λS , and κ are therefore defined in the MS scheme at the renormalization scale µR , and no physical
pole mass condition is imposed for S.
Accordingly, only the Higgs-sector counterterms δµ2 and δλ are required explicitly in the numerical implementation.
They are fixed by imposing the renormalization conditions
∣
dVeff ∣∣
= 0,
(A26)
dh ∣h=v, S=0, T =0
∣
d2 Veff ∣∣
= m2h ,
(A27)
dh2 ∣
h=v, S=0, T =0

## PDF page 12

12
ensuring that the electroweak vacuum expectation value v = 246 GeV and the Higgs mass mh = 125 GeV remain
unchanged at one loop.
Since the singlet does not acquire a vacuum expectation value and no singlet on-shell condition is imposed, the
counterterms δm2S , δλS , and δκ do not enter explicitly in the background-field calculation along S = 0.
With these conditions imposed, the zero-temperature effective potential reproduces the physical Higgs mass and
vacuum structure, while the singlet parameters retain their perturbative MS definitions at the scale µR = v.

[1] A. Kosowsky and M. S. Turner, Phys. Rev. D 47, 4372 (1993), astro-ph/9211004.
[2] M. Kamionkowski, A. Kosowsky, and M. S. Turner, Phys. Rev. D 49, 2837 (1994), astro-ph/9310044.
[3] C. J. Hogan, Mon. Not. Roy. Astron. Soc. 218, 629 (1986).
[4] C. Caprini et al., JCAP 04, 001 (2016), 1512.06239.
[5] C. Caprini et al., JCAP 03, 024 (2020), 1910.13125.
[6] M. Quiros, in ICTP Summer School in High-Energy Physics and Cosmology (1999), pp. 187–259, hep-ph/9901312.
[7] M. Trodden, Rev. Mod. Phys. 71, 1463 (1999), hep-ph/9803479.
[8] D. E. Morrissey and M. J. Ramsey-Musolf, New J. Phys. 14, 125003 (2012), 1206.2942.
[9] A. Mazumdar and G. White, Rept. Prog. Phys. 82, 076901 (2019), 1811.01948.
[10] J. R. Espinosa and M. Quiros, Phys. Lett. B 305, 98 (1993), hep-ph/9301285.
[11] A. Noble and M. Perelstein, Phys. Rev. D 78, 063518 (2008), 0711.3018.
[12] S. Profumo, M. J. Ramsey-Musolf, and G. Shaughnessy, JHEP 08, 010 (2007), 0705.2425.
[13] J. R. Espinosa, T. Konstandin, J. M. No, and M. Quiros, Phys. Rev. D 78, 123528 (2008), 0809.3215.
[14] V. Barger, P. Langacker, M. McCaskey, M. Ramsey-Musolf, and G. Shaughnessy, Phys. Rev. D 79, 015018 (2009),
0811.0393.
[15] D. Curtin, P. Meade, and C.-T. Yu, JHEP 11, 127 (2014), 1409.0005.
[16] C.-Y. Chen, S. Dawson, and I. M. Lewis, Phys. Rev. D 91, 035015 (2015), 1410.5488.
[17] A. Chaudhuri and M. Y. Khlopov, MDPI Physics 3, 275 (2021), 2103.03477.
[18] A. Chaudhuri, M. Y. Khlopov, and S. Porey, Galaxies 9, 45 (2021), 2105.10728.
[19] A. Chaudhuri and M. Y. Khlopov, Universe 7, 275 (2021), 2106.11646.
[20] A. Chaudhuri, M. Y. Khlopov, and S. Porey, Symmetry 14, 271 (2022), 2110.14161.
[21] J. Kozaczuk, JHEP 10, 135 (2015), 1506.04741.
[22] T. Huang, J. M. No, L. Pernié, M. Ramsey-Musolf, A. Safonov, M. Spannowsky, and P. Winslow, Phys. Rev. D 96, 035007
(2017), 1701.04442.
[23] A. Beniwal, M. Lewicki, M. White, and A. G. Williams, JHEP 02, 183 (2019), 1810.02380.
[24] P. Basler and M. Mühlleitner, Comput. Phys. Commun. 237, 62 (2019), 1803.02846.
[25] T. Alanne, T. Hugle, M. Platscher, and K. Schmitz, JHEP 03, 004 (2020), 1909.11356.
[26] D. Croon, O. Gould, P. Schicho, T. V. I. Tenkanen, and G. White, JHEP 04, 055 (2021), 2009.10080.
[27] A. Chaudhuri, Nucl. Phys. B 1024, 117357 (2026), 2507.13135.
[28] A. Chaudhuri and J. Das, Phys. Rev. D 106, 095016 (2022), 2206.08699.
[29] E. W. Kolb and M. S. Turner, The Early Universe, vol. 69 (Taylor and Francis, 2019), ISBN 978-0-429-49286-0, 978-0201-62674-2.
[30] L. J. Hall, K. Jedamzik, J. March-Russell, and S. M. West, JHEP 03, 080 (2010), 0911.1120.
[31] J. L. Feng, H. Tu, and H.-B. Yu, JCAP 10, 043 (2008), 0808.2318.
[32] X. Chu, T. Hambye, and M. H. G. Tytgat, JCAP 05, 034 (2012), 1112.0493.
[33] M. Blennow, E. Fernandez-Martinez, O. Mena, J. Redondo, and P. Serra, JCAP 07, 022 (2012), 1203.5803.
[34] Y. Akrami et al. (Planck), Astron. Astrophys. 641, A10 (2020), 1807.06211.
[35] N. Aghanim et al. (Planck), Astron. Astrophys. 641, A6 (2020), [Erratum: Astron.Astrophys. 652, C4 (2021)], 1807.06209.
[36] R. H. Cyburt, B. D. Fields, K. A. Olive, and T.-H. Yeh, Rev. Mod. Phys. 88, 015004 (2016), 1505.01076.
[37] B. D. Fields, K. A. Olive, T.-H. Yeh, and C. Young, JCAP 03, 010 (2020), [Erratum: JCAP 11, E02 (2020)], 1912.01132.
[38] A. Berlin, D. Hooper, and G. Krnjaic, Phys. Rev. D 94, 095019 (2016), 1609.02555.
[39] Y. Cui, M. Lewicki, D. E. Morrissey, and J. D. Wells, Phys. Rev. D 97, 123505 (2018), 1711.03104.
[40] J. A. Dror, K. Harigaya, and V. Narayan, Phys. Rev. D 99, 035036 (2019), 1810.07195.
[41] R. T. Co, F. D’Eramo, L. J. Hall, and D. Pappadopulo, JCAP 12, 024 (2015), 1506.07532.
[42] S. J. Huber and T. Konstandin, JCAP 09, 022 (2008), 0806.1828.
[43] M. Hindmarsh, S. J. Huber, K. Rummukainen, and D. J. Weir, Phys. Rev. D 92, 123009 (2015), 1504.03291.
[44] M. Hindmarsh, S. J. Huber, K. Rummukainen, and D. J. Weir, Phys. Rev. D 96, 103520 (2017), [Erratum: Phys.Rev.D
101, 089902 (2020)], 1704.05871.
[45] D. J. Weir, Phil. Trans. Roy. Soc. Lond. A 376, 20170126 (2018), [Erratum: Phil.Trans.Roy.Soc.Lond.A 381, 20230212
(2023)], 1705.01783.
[46] A. Chaudhuri and K. Kohri, Nucl. Phys. B 1018, 117098 (2025), 2404.10288.
[47] T. Srivastava, J. Das, A. Ghosh, and A. Chaudhuri, JCAP 02, 032 (2026), 2507.05917.
[48] A. Chaudhuri, P. Mishra, and R. Mohanta (2025), 2508.09835.

## PDF page 13

13
[49] A. Chaudhuri (2025), 2509.22293.
[50] E. Witten, Phys. Rev. D 30, 272 (1984).
[51] A. Kosowsky, M. S. Turner, and R. Watkins, Phys. Rev. D 45, 4514 (1992).
[52] A. Kosowsky, M. S. Turner, and R. Watkins, Phys. Rev. Lett. 69, 2026 (1992).
[53] C. Caprini, R. Durrer, T. Konstandin, and G. Servant, Phys. Rev. D 79, 083519 (2009), 0901.1661.
[54] P. Athron, C. Balázs, A. Fowlie, L. Morris, and L. Wu, Prog. Part. Nucl. Phys. 135, 104094 (2024), 2305.02357.
[55] P. Ghosh, T. Ghosh, and S. Roy, JHEP 10, 057 (2023), 2211.15640.
[56] P. Bittar, S. Roy, and C. E. M. Wagner, JHEP 12, 021 (2025), 2504.02024.
[57] C. Grojean and G. Servant, Phys. Rev. D 75, 043507 (2007), hep-ph/0607107.
[58] J. R. Espinosa, T. Konstandin, J. M. No, and G. Servant, JCAP 06, 028 (2010), 1004.4187.
[59] H. H. Patel and M. J. Ramsey-Musolf, JHEP 07, 029 (2011), 1101.4665.
[60] M. Kakizaki, S. Kanemura, and T. Matsui, Phys. Rev. D 92, 115007 (2015), 1509.08394.
[61] F. P. Huang and J.-H. Yu, Phys. Rev. D 98, 095022 (2018), 1704.04201.
[62] P. Athron, C. Balazs, A. Fowlie, G. Pozzo, G. White, and Y. Zhang, JHEP 11, 151 (2019), 1908.11847.
[63] K. Hashino, R. Jinno, M. Kakizaki, S. Kanemura, T. Takahashi, and M. Takimoto, Phys. Rev. D 99, 075011 (2019),
1809.04994.
[64] M. Chala, G. Nardini, and I. Sobolev, Phys. Rev. D 94, 055006 (2016), 1605.08663.
[65] M. J. Ramsey-Musolf, JHEP 09, 179 (2020), 1912.07189.
[66] M. Fairbairn, E. Hardy, and A. Wickens, JHEP 07, 044 (2019), 1901.11038.
[67] J. Ellis, M. Lewicki, J. M. No, and V. Vaskonen, JCAP 06, 024 (2019), 1903.09642.
[68] D. Cutting, M. Hindmarsh, and D. J. Weir, Phys. Rev. D 97, 123513 (2018), 1802.05712.
[69] J. Das, S. Niyogi, and T. Srivastava (2026), 2601.13147.
[70] P. Amaro-Seoane et al. (LISA) (2017), 1702.00786.
[71] P. A. Seoane et al. (LISA), Living Rev. Rel. 26, 2 (2023), 2203.06016.
[72] S. Kawamura et al., Class. Quant. Grav. 28, 094011 (2011).
[73] V. Corbin and N. J. Cornish, Class. Quant. Grav. 23, 2435 (2006), gr-qc/0512039.
[74] K. Yagi and N. Seto, Phys. Rev. D 83, 044011 (2011), [Erratum: Phys.Rev.D 95, 109901 (2017)], 1101.3940.
[75] C. L. Wainwright, Comput. Phys. Commun. 183, 2006 (2012), 1109.4189.
[76] B. Patt and F. Wilczek (2006), hep-ph/0605188.
[77] J. R. Espinosa, T. Konstandin, and F. Riva, Nucl. Phys. B 854, 592 (2012), 1107.5441.
[78] P. B. Arnold and O. Espinosa, Phys. Rev. D 47, 3546 (1993), [Erratum: Phys.Rev.D 50, 6662 (1994)], hep-ph/9212235.
[79] E. Thrane and J. D. Romano, Phys. Rev. D 88, 124032 (2013), 1310.5300.
[80] R. R. Parwani, Phys. Rev. D 45, 4695 (1992), [Erratum: Phys.Rev.D 48, 5965 (1993)], hep-ph/9204216.
