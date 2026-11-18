Source: https://arxiv.org/abs/2601.13147v3
PDF sha256: 1eb72d755f7fb441526aa1ce7600c851b1337e752d32e616689237e1e00f2f12
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of das_2026_singlet_fermion_dm.pdf

Transcription of `das_2026_singlet_fermion_dm.pdf` in this directory, 40 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-40 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Revisiting Singlet Fermion Dark Matter with a Scalar
Portal: Connecting Higgs Phenomenology and Strong
Electroweak Phase Transition

Jaydeb Das,

a Saurabh Niyogi,

b Tripurari Srivastava

c,d

arXiv:2601.13147v3 [hep-ph] 31 Jan 2026

a

Department of Physics, Indian Institute of Technology Guwahati, North Guwahati, Assam-781039,
India.
b
Department of Physics, Gokhale Memorial Girls’ College, Kolkata, West Bengal-700020, India.
c
Department of Physics and Astrophysics, University of Delhi, Delhi-110007, Delhi, India.
d
Institute of Particle Physics and Key Laboratory of Quark and Lepton Physics (MOE), Central
China Normal University, Wuhan, Hubei 430079, China.

E-mail: jaydebphys@rnd.iitg.ac.in, saurabhphys@gmail.com,
tripurarisri022@gmail.com
Abstract: We investigate a minimal extension of the Standard Model with a real singlet
scalar and a singlet Dirac fermion acting as dark matter. Unlike a conventional singlet
scalar setup, we assume that the singlet scalar does not acquire a vacuum expectation value
at zero temperature. This decouples the scalar mixing angle from the Higgs–portal quartic
coupling responsible for the strong first-order electroweak phase transition, allowing it to
coexist with current collider and direct-detection constraints. The Higgs–singlet mixing
is generated independently through a trilinear portal interaction. We check theoretical
consistency conditions, various LHC limits on heavy scalar resonances, dark matter relic
abundance, and direct detection bounds to delineate the viable parameter space. We
perform a detailed analysis of the electroweak phase transition and show that a strong firstorder transition is realized for a selected set of benchmark points. We further compute the
resulting stochastic gravitational wave spectra and find that several scenarios yield signals
potentially observable at future space-based interferometers. Our results establish a unified
and testable framework that connects collider phenomenology, first-order electroweak phase
transition, and the resulting production of gravitational waves, along with the dark matter
phenomenology, all within a simple renormalizable extension of the Standard Model.
Keywords: Dark matter, Electroweak phase transition, Gravitational wave, Collider phenomenology

## PDF page 2

Contents
1 Introduction

1

2 The framework

3

3 Constraints
3.1 Theoretical constraints
3.2 Electroweak precision observables
3.3 LHC constraints on the heavy scalar h2
3.4 Higgs signal strength constraint
3.5 Future HL-LHC sensitivity

5
5
6
6
8
9

4 Dark matter study
4.1 Relic density
4.2 Direct detection
4.3 Future collider prospects

9
9
14
17

5 Electroweak phase transition and GW detection
5.1 One-loop effective potential
5.2 Electroweak phase transition
5.3 Stochastic gravitational waves

18
18
22
23

6 Summary and conclusions

29

A Coefficients of Vct (h, s)

31

1

Introduction

The Standard Model (SM) of particle physics, despite its remarkable success in describing
the known fundamental particles and their interactions, remains incomplete. In particular,
it fails to account for the observed baryon asymmetry of the Universe, namely the excess
of matter over antimatter. Electroweak baryogenesis offers an attractive explanation for
this asymmetry, provided that the electroweak phase transition (EWPT) is strongly first
order. However, for the experimentally measured Higgs boson mass of 125 GeV, the electroweak phase transition in the SM proceeds as a smooth crossover [1–3], precluding the
strong out of equilibrium dynamics required to satisfy the Sakharov conditions [4]. Consequently, electroweak baryogenesis is not viable within the SM framework [5, 6], motivating
the exploration of physics beyond the SM (BSM). Among the many possible extensions,

–1–

## PDF page 3

minimal and economical scenarios that can address these shortcomings without introducing
unnecessary complexity are particularly appealing.
Another major missing piece in our understanding of fundamental physics is the nature
of dark matter (DM), whose existence is firmly established by astrophysical and cosmological observations but remains unexplained within the SM. A simple and widely studied
possibility is to extend the SM by a real gauge singlet scalar, which can itself serve as
a dark matter candidate when stabilized by a discrete symmetry [7, 8]. In such scalar
dark matter models, however, the stabilizing symmetry forbids interactions involving odd
powers of the singlet field. As a result, the observed relic abundance is typically achieved
only in the Higgs funnel region, requiring a very small Higgs portal coupling. While this
suppresses direct detection rates, it also renders the scalar sector ineffective in inducing
a strong first-order electroweak phase transition [9, 10]. Increasing the portal coupling to
strengthen the phase transition is, on the other hand, tightly constrained by direct detection experiments [11, 12]. Consequently, scalar dark matter extensions often face a tension
between obtaining the correct relic density and realizing a strong first-order electroweak
phase transition simultaneously.
A minimal way to alleviate this tension is to separate the roles of dark matter and the
electroweak phase transition. In this work, we consider an extension of the SM containing
a real singlet scalar and a singlet Dirac fermion. The fermion constitutes the dark matter
candidate, while the scalar field modifies the Higgs potential and plays a central role in the
dynamics of the electroweak phase transition. The Yukawa interaction between the scalar
and the fermion governs the thermal freeze out of dark matter, whereas both the scalar self
interactions and the scalar fermion coupling contribute to the finite temperature effective
potential. This minimal field content therefore provides a unified framework in which dark
matter phenomenology and electroweak phase transition dynamics are intrinsically linked,
while leaving distinct imprints in direct detection experiments, collider observables, and
cosmology.
In many singlet extended models, the scalar field acquires a vacuum expectation value
(VEV) at zero temperature, and achieving a strong first-order EWPT requires a large
Higgs portal coupling [13, 14]. This simultaneously induces a large Higgs singlet mixing
angle, which is strongly constrained by LHC measurements and direct detection bounds. In
contrast, we adopt a different strategy by requiring that the singlet scalar does not acquire a
vacuum expectation value at zero temperature [15, 16]. The Higgs singlet mixing is instead
controlled by an independent trilinear portal interaction. This construction decouples the
mixing angle from the quartic portal coupling, allowing the latter to be large enough to
generate a strong first-order electroweak phase transition (SFOEWPT) while keeping the
mixing angle small and consistent with existing experimental constraints.
Though SFOEWPT can be realized in a variety of new-physics scenarios, including
models with extended scalar sectors such as two Higgs doublet models (2HDMs) [17, 18],
various singlet or multi-scalar extensions [7, 10, 19–40], or higher-dimensional operators [5,
41–45]; we stick to a minimal extension of the SM. Thus, such minimal particle content
beyond the SM within the renormalizable and gauge-invariant framework is not only able
to explain the observed dark matter relic abundance, but also modifies the structure of

–2–

## PDF page 4

the scalar potential in such a way that opens the possibility of a strong first-order phase
transition, which is one of the required conditions for baryogenesis in the present universe.
In addition, the generation of detectable stochastic gravitational waves from the expansion
and subsequent collision of bubbles of the broken phase offers another experimental channel
to test such a scenario [46–56]. The breakthrough discovery by LIGO [57] has opened a new
window into early universe dynamics, motivating the study of electroweak-scale GWs as a
complementary probe of new physics in collider. The amplitude and peak frequency of the
resulting GW spectrum encode information about the underlying scalar potential, making
future space-based interferometers—such as LISA [58], DECIGO [59], BBO [60], TAIJI [61],
and TianQin [62]—promising tools for testing SFOEWPT scenarios. Therefore, the mixing
angle between the SM doublet and real singlet that appears in the Higgs couplings controls
the phenomenology of the heavier scalar state. On top of that, the new scalar interactions
allow for non-resonant and resonant collider signatures - thus offering a well-defined and
testable link between cosmological considerations and collider experiments.
The structure of the paper is as follows. In Section 2, we introduce the theoretical
setup of the model. Section 3 is devoted to theoretical, collider, and electroweak precision
constraints. The dark matter phenomenology, including relic density and direct detection,
is discussed in Section 4. In Section 5, we analyze the electroweak phase transition and
the associated gravitational wave signals. Finally, we summarize our results and conclude
in Section 6.

2

The framework

We extend the SM by introducing a real gauge-singlet scalar field s and a Dirac fermion
χ which is also a singlet under the SM gauge group. In this framework, the fermion χ
plays the role of a WIMP-like (weakly interacting massive particle) DM. To guarantee its
stability, we impose a discrete Z2 symmetry under which χ is odd, while the scalar field s
and all SM fields remain even. This symmetry forbids any interaction of χ directly with
the SM particles. Consequently, χ can not decay directly into any SM pair. Therefore, the
most general renormalizable Lagrangian consistent with the SM gauge symmetries and the
imposed Z2 parity for this scenario can be written as:
1
L ⊃ (∂µ s)2 + χ̄(i ̸ ∂ − mχ )χ + Lχs − V (H, s),
2

(2.1)

where mχ is the bare mass term of χ and Lχs is the Lagrangian containing the scalar-DM
Yukawa interaction. The most general renormalizable scalar potential V (H, s) is [9, 63]
1
1
1
V (H, s) = µ2h |H|2 + λh |H|4 + µ2s s2 + λs s4 + λhs |H|2 s2
2
4
2
1
+ µhs |H|2 s + µ3 s3 + a1 s,
3
where the Higgs doublet at zero temperature is
(
)
1
χ1 − iχ2
H=√
,
2 h + v + iχ3

–3–

(2.2)

(2.3)

## PDF page 5

where v ≈ 246 GeV denotes the VEV of the Higgs field at zero temperature. Since the DM
candidate χ is stabilized by a Z2 symmetry under which χ → −χ, the only renormalizable
Yukawa interaction between the singlet scalar field and the fermion field is [64, 65]
Lχs = gχ s χ̄χ,

(2.4)

where gχ is a dimensionless coupling constant. Throughout this work, we assume that the
singlet scalar does not have VEV at zero temperature [66–68]. Under this assumption, the
bare mass parameter mχ of the singlet fermion χ (see Eq. (2.1)) coincides with its physical
mass.
Scalar potential at tree level
Expanding the scalar potential V (H, s) in terms of the background fields (h, s) gives the
tree-level potential
1
1
1
1
1
1
1
V0 (h, s) = µ2h h2 + µ2s s2 + λh h4 + λs s4 + λhs h2 s2 + µhs h2 s + µ3 s3 + a1 s. (2.5)
2
2
4
4
4
2
3
At zero temperature, the electroweak vacuum is located at (h, s) = (v, 0), and the stationary
conditions of the tree-level potential require
∣
∂V0 ∣∣
(2.6)
= 0 ⇒ µ2h = −λh v 2 ,
∂h ∣(v,0)
∣
∂V0 ∣∣
µhs v 2
=
0
⇒
a
=
−
.
(2.7)
1
∂s ∣(v,0)
2
Hence, the s–tadpole condition removes a1 as a free parameter, making it fixed in terms
of the mixing parameter µhs and the VEV of the Higgs field.
Scalar mixing matrix
Although the singlet scalar field s does not acquire a VEV at zero temperature, the term
µhs s|H|2 induces mixing between the Higgs and the singlet scalar after the spontaneous
breaking of the electroweak symmetry. The CP-even scalar mass matrix at (v, 0) is
)
(
) (
2
2 M2
2λ
v
µ
v
M
h
hs
hh
hs .
(2.8)
M 2 (v, 0) =
≡
2 M2
µhs v µ2s + 12 λhs v 2
Mhs
ss
To obtain the physical scalar masses, the mass matrix is diagonalized by an orthogonal
transformation, yielding the mass eigenstates h1 and h2 defined as
( ) (
)( )
h1
cos θ − sin θ
h
=
,
(2.9)
h2
sin θ cos θ
s
Here h1 is identified with the observed 125 GeV Higgs boson, and θ denotes the Higgs–
singlet mixing angle. The gauge eigenstates can therefore be expressed in terms of the
mass eigenstates as
h = cos θ h1 + sin θ h2 ,

s = cos θ h2 − sin θ h1 ,

–4–

(2.10)

## PDF page 6

and the corresponding mass eigenvalues are
2
2
2
m2h1 = Mhh
cos2 θ + Mss
sin2 θ − 2Mhs
sin θ cos θ,

(2.11)

2
2
2
m2h2 = Mhh
sin2 θ + Mss
cos2 θ + 2Mhs
sin θ cos θ.

(2.12)

Conversely, the parameters of the scalar potential may be expressed in terms of the physical
inputs:
λh =

m2h1 cos2 θ + m2h2 sin2 θ
,
2v 2

µhs =

(m2h2 − m2h1 )
sin θ cos θ,
v

(2.13)

λhs v 2
.
(2.14)
2
These relations allow one to trade the potential parameters for the physical masses and the
mixing angle. In summary, the independent input parameters of the scalars–DM sector for
the model are:
{ v, mh1 , mh2 , sin θ, gχ , mχ , λhs , µ3 , λs }.
µ2s = m2h1 sin2 θ + m2h2 cos2 θ −

Here, we assume that the real singlet scalar does not acquire a VEV at zero temperature.
Consequently, the Higgs–singlet mixing arises solely from the dimensionful interaction term
µhs rather than from the Higgs-portal coupling λhs . As a result, the direct-detection cross
section is independent of λhs . This allows us to choose a relatively large portal coupling
to achieve a SFOEWPT, while remaining fully consistent with current direct-detection
constraints, as discussed later.

3

Constraints

In this section, we summarize the theoretical and experimental constraints relevant to
the singlet–fermion plus singlet real–scalar extension of the SM. We begin with the requirements of theoretical consistency, followed by a discussion on constraints coming from
electroweak precision observables (EWPOs). Finally, we present collider bounds on the
heavier scalar state h2 along with the Higgs signal strength measurements.
3.1

Theoretical constraints

A consistent scalar potential must be bounded from below, perturbative, and admit the
electroweak vacuum as a stable minimum.
(i) Vacuum stability.

The quartic couplings must satisfy the positivity conditions
√
λh ≥ 0,
λs ≥ 0,
λhs ≥ −2 λh λs ,
(3.1)

ensuring that the potential is bounded from below. For λhs ≥ 0 these conditions are
automatically satisfied.
(ii) Perturbative unitarity.
amplitudes requires [69–71]

Tree-level perturbative unitarity of scalar 2 → 2 scattering

|λh | ≤ 4π,
|λs | ≤ 4π,
|λhs | ≤ 8π,
√
∣
∣
∣
2 ∣ ≤ 8π.
2
3λ
+
2λ
±
(3λ
−
2λ
)
+
2λ
∣ h
s
s
h
hs ∣

–5–

(3.2)

## PDF page 7

3.2

Electroweak precision observables

Mixing between the singlet scalar and the SM Higgs modifies electroweak precision observables, particularly the oblique parameters S and T and the W -boson mass. These effects
grow with both the mixing angle θ and the heavy-scalar mass mh2 . For mh2 ≳ 800 GeV
the loop-induced corrections typically impose the bound
| sin θ| ≲ 0.2.

(3.3)

This constraint is complementary to Higgs signal-strength limits and becomes dominant
at large mh2 .
3.3

LHC constraints on the heavy scalar h2

In the real scalar singlet extension considered here, electroweak symmetry breaking leads
to two physical CP-even scalars: the observed Higgs boson h1 with mass mh1 = 125 GeV
and a heavier scalar h2 with mass mh2 . The mixing in the scalar sector suppresses all
couplings of h1 to SM quarks and gauge bosons by factor of cos θ. Similarly, the couplings
to heavier scalar to SM quarks and gauge bosons also get scaled by sin θ.
Production rate.

The production cross section of h2 at the LHC is therefore given by
σ(pp → h2 ) ≃ sin2 θ σSM (mh2 ),

(3.4)

where σSM (mh2 ) denotes the Standard Model Higgs production cross section evaluated at
mass mh2 .
Decay pattern. The branching ratios of h2 follow those of an SM Higgs boson with
mass mh2 , up to kinematic differences such as the opening of the decay h2 → h1 h1 for
mh2 > 2mh1 . We compute the signal rate
σ(pp → h2 ) × BR(h2 → XX)

(3.5)

across the (mh2 , sin θ) parameter space using MadGraph5 aMC@NLO [72]. These predictions
from the model are then compared to the 95% C.L. upper limits reported by ATLAS and
CMS in Run 2 searches for heavy scalar. The experimental limits are taken from the official
HEPData tables and interpolated across the mass range shown in the figures. The three
most relevant final states for heavy-scalar searches are:
• h2 → h1 h1 ,
• h2 → ZZ → 4ℓ,
• h2 → W W → ℓνℓν.

–6–

## PDF page 8

Figure 1: Predicted cross section σ(pp → h2 ) × BR(h2 → h1 h1 ) in the (mh2 , sin θ) plane.
The solid curve shows the ATLAS 95% CL upper limit; the region above the curve is
excluded.
Di-Higgs final state. For scalar masses around mh2 ≃ 460–600 GeV, the decay h2 →
h1 h1 becomes increasingly important. In this mass window, the ATLAS resonant di-Higgs
searches [73] provide their strongest constraint, excluding mixing angles above
sin θ ≳ 0.36.
For mh2 ≳ 600 GeV, the exclusion gradually weakens as the production cross section and
the h2 → h1 h1 branching ratio decrease.
At the High-Luminosity LHC, the di-Higgs sensitivity is expected to improve substantially [74]. The projected limits strengthen the constraint on the mixing angle to roughly
sin θ ≲ 0.20–0.25,
depending mildly on mh2 , thereby probing a significantly wider region of parameter space.
Figure 1 displays the predicted di-Higgs yield, with the black curve showing the present
95% CL exclusion from LHC searches and the blue curve indicating the expected reach of
the HL-LHC.
ZZ → 4ℓ channel. Due to the excellent invariant-mass resolution and the very small
background in the ZZ → 4ℓ channel, the strongest constraint on the mixing angle is
obtained in this mode. Using the observed limits reported in Ref. [75], we find
sin θ ≳ 0.13 − 0.20

for

250 GeV ≲ mh2 ≲ 700 GeV.

(3.6)

The bound becomes less strong as a result of the reduced production rate at higher masses.

–7–

## PDF page 9

(a)

(b)

Figure 2: Exclusion in the ZZ final state. The ZZ → 4ℓ channel provides the strongest
constraint across most of the mass range. Constraints from the W W final state. The sensitivity is weaker than ZZ due to larger backgrounds, but remains important for intermediate
masses.
WW channel. Although the branching ratio of the 125 GeV Higgs boson to W W is
larger than that to ZZ, the corresponding experimental analysis is affected by substantially
higher backgrounds, resulting in a much weaker exclusion power. As reported in Ref. [76],
the W W final state therefore provides only a modest constraint on the Higgs–singlet mixing
angle, with values as large as sin θ ≃ 0.5 remaining allowed across the full mass range
considered. Consequently, this channel is far less sensitive than the ZZ → 4ℓ mode or the
resonant di–Higgs searches. The exclusion further degrades at higher masses due to the
usual decrease in the production cross section.
Combined collider limit.

Collectively, heavy-scalar searches exclude

sin θ ≳ O(0.1)
3.4

for

mh2 ≲ 600 GeV.

(3.7)

Higgs signal strength constraint

Since h1 couples as cos θ, the global signal strength scales as
µsig = cos2 θ.

(3.8)

µATLAS = 1.04 ± 0.06,

(3.9)

sin θ ≲ 0.24.

(3.10)

ATLAS Run-II measurements yield

which implies, at the 95% C.L.,

This constraint is independent of mh2 and can be stronger than direct heavy-scalar searches.

–8–

## PDF page 10

3.5

Future HL-LHC sensitivity

The High-Luminosity LHC (HL-LHC) is expected to achieve substantially improved precision in Higgs coupling measurements, leading to a projected bound
| sin θ| ≲ 0.17.

(3.11)

Direct searches for a heavy scalar will probe mixings down to
| sin θ| ∼ 0.05–0.10

for

200 GeV ≲ mh2 ≲ 600 GeV.

(3.12)

These improvements will cover a large portion of the parameter space still allowed by
present data.

4

Dark matter study

In this section, we study the phenomenology of a WIMP-like singlet fermionic dark matter.
We compute the dark-matter relic abundance and the spin-independent DM–nucleon scattering cross section using micrOMEGAs [77, 78]. In the following subsections, we present a
detailed analysis of the relic-density constraints and direct-detection bounds, and identify
the corresponding allowed regions of the parameter space.
4.1

Relic density

In this model, the singlet Dirac fermion χ serves as the DM candidate as mentioned earlier.
It couples only with the real singlet scalar field s via the Yukawa interaction given in
Eq. (2.4). After electroweak symmetry breaking (EWSB) through the VEV of the Higgs
field, its annihilation proceeds through the two scalar mediators h1 and h2 . In addition
to DM annihilation to SM particles, some other important channels like hi hj (i, j = 1, 2)
become crucial. Hence, the abundance after thermal freeze-out is determined primarily by
two parameters (with the dominant one depending on the DM mass range): the scalar–
Higgs mixing angle sin θ, which controls the mediator–SM interactions, and the Yukawa
coupling gχ , which sets the strength of the vertices χ̄χh1,2 . Additionally, Higgs portal
coupling λhs and trilinear coupling µ3 play a crucial role in achieving the correct relic
density. Throughout the entire parameter space, the relic density is independent of the
scalar quartic coupling λs .
Depending on the relative sizes of sin θ, gχ and λhs , the correct thermal relic density can
be achieved in different (and sometimes mutually disjoint) regions of the parameter space.
The viable regions can be grouped into three characteristic classes: (i) the Higgs funnel
mχ ≃ mh1 /2, (ii) the singlet-scalar resonance mχ ≃ mh2 /2, and (iii) the degenerate region
where annihilation is enhanced by near-kinematic alignment lies beyond the mχ ≈ mh2
region.
The interplay between sin θ and gχ yields the following behavior, which has been
displayed in Fig. 3. This can be summarized as follows:

–9–

## PDF page 11

• Both sin θ and gχ large: The annihilation cross section receives substantial enhancement from both scalar mediators. In this case, the observed relic density can
be reproduced in all the characteristic regions: the Higgs funnel, the h2 -resonance,
and the degenerate region. The blue curve in Fig. 3 shows this region.
• Large sin θ, small gχ : A sizeable mixing angle ensures efficient annihilation through
the SM channels mediated by h1 and h2 . The correct relic density is typically obtained
in the Higgs funnel and the h2 -resonance regions. However, the degenerate region
becomes ineffective because a small gχ cannot generate sufficient annihilation away
from the resonance peaks. The green line in Fig. 3 corresponds to this case.
• Small sin θ, large gχ : In this regime, the SM-mediated channels are suppressed, but
the direct coupling to the singlet mediator is strong. The observed relic abundance
can then be obtained in the h2 -resonance region and in the degenerate domain, where
processes such as χχ → h∗2 → SM SM or χχ → h2 h2 may dominate. In Fig. 3, the
red curve highlights this region.
• Both sin θ and gχ small: Here, the annihilation cross section remains insufficient
throughout most of the parameter space. The correct relic density can be achieved
only near a very narrow region of the h2 -resonance, shown in magenta contour in
Fig. 3, where the s-channel enhancement boosts the annihilation efficiency.
gχ = 1.0, sinθ = 0.3

107

gχ = 1.0, sinθ = 0.3

107

gχ = 1.0, sinθ = 0.001

gχ = 1.0, sinθ = 0.001

105

gχ = 0.1, sinθ = 0.3
gχ = 0.1, sinθ = 0.001

1000
10

0.100

0.001

0.001
50

100

200

gχ = 0.1, sinθ = 0.001

10

0.100

20

gχ = 0.1, sinθ = 0.3

1000

ΩDMh2

ΩDMh2

105

500

mχ [GeV]

20

50

100

200

500

mχ [GeV]

Figure 3: Variation of relic abundance with dark matter mass mχ with two different chosen
values of sin θ and gχ mentioned in the inset. Left panel for mh2 = 200 GeV and right for
mh2 = 350 GeV. For both cases, we have taken λhs = 0.8 and µ3 = −50 GeV. The black
dashed line indicates the observed dark matter relic abundance, ΩDM h2 = 0.12±0.001 [79].
Overall, these patterns clearly indicate that achieving the observed thermal relic density requires the DM to be annihilated either through a sufficiently large mixing angle in
the scalar sector or through a sizeable DM Yukawa interaction. We have displayed the
relic abundance against the DM mass in Fig. 3 for some representative fixed values of the
mixing angle sin θ and coupling constant gχ . The purpose is to highlight the dependency of
the relic abundance on the mass of the DM. One may take, in principle, any mixing angle
and coupling constant in between the representative points, but the observed relic density
can be obtained only in the three regions of the DM mass as mentioned above.

– 10 –

## PDF page 12

1.0

0.8

0.2

0.6

g

0.1

0.4
0.2

0.0
60

100

200

m [GeV]

400 600

0.3

1.0

sin

g

0.8

0.0

1.2

0.3

0.2

0.6

sin

1.2

0.1

0.4
0.2
0.0

0.0
60

100

200

m [GeV]

400 600

Figure 4: Variation of the Yukawa coupling gχ with DM mass mχ maintaining relic
abundance in the range 0.1 ≤ ΩDM h2 ≤ 0.121. The color gradient represents the mixing
angle sin θ. Left panel for mh2 = 200 GeV and right for mh2 = 350 GeV. For both cases,
we have taken λhs = 0.8 and µ3 = −50 GeV.
The thermal relic abundance in this scalar-portal framework is governed by the interplay between the scalar mixing angle sin θ and the dark-sector Yukawa coupling gχ . The
left panel of Fig. 4 shows the allowed parameter space in the (mχ , gχ ) plane, where the
color gradient encodes the value of the mixing angle sin θ, for a fixed heavy-scalar mass
mh2 = 200 GeV, portal coupling λhs = 0.8, and trilinear parameter µ3 = −50 GeV. The
displayed region corresponds to parameter values that yield a relic density within the range,
0.1 ≤ ΩDM h2 ≤ 0.121 [79].
As seen from this figure, the observed relic abundance can be reproduced across a broad
interval of gχ values in both the Higgs-funnel region and in the vicinity of the heavy-scalar
(h2 ) resonance. In the Higgs-funnel regime (mχ ≃ mh1 /2), the annihilation cross section is
primarily controlled by the Higgs–portal interaction, which scales with the mixing angle.
Consequently, obtaining the correct relic density in this region requires a relatively large
sin θ, while the precise value of gχ plays only a subdominant role.
In contrast, when the dark-matter mass approaches the heavy-scalar resonance, mχ ≃
mh2 /2, the Breit-Wigner enhancement substantially increases the annihilation rate. This
resonant behavior permits a wide range of mixing angles to satisfy the relic density constraint, and largely independent of the magnitude of gχ (depending on how close the DM
mass is to mh2 /2). However, away from this near-degenerate region, the annihilation cross
section becomes insufficient for small gχ , and even large values of sin θ fail to reproduce
the observed relic abundance. The right panel of Fig. 4, corresponding to a heavier scalar
mass (mh2 = 350 GeV), is shown for the same trilinear and Higgs portal couplings as in
the left panel. The qualitative behavior remains similar to that observed in the left panel;
however, the viable parameter space is shifted toward larger dark-matter masses, reflecting
the dependence of the annihilation dynamics on the heavy scalar mass scale.
The requirement of a strong first-order electroweak phase transition, discussed in a
later section, favors relatively large values of the portal coupling λhs for a larger singlet
scalar mass. Fig. 5 shows that the observed relic density can be accommodated even for
such enhanced values of λhs . In particular, a larger portal coupling allows for a broader

– 11 –

## PDF page 13

region of viable parameter space in the regime mχ ≲ mh2 . Moreover, as discussed earlier,
variations in λhs do not significantly impact the determination of the direct detection cross
section.
1.2

0.3

1.0

0.2

0.6

sin

g

0.8

0.1

0.4
0.2
0.0

0.0
60

100

200

m [GeV]

400 600

Figure 5: Variation of the relic density for a sizable Higgs portal coupling λhs = 2.0, while
all other parameters are fixed to the same values as in the left panel of Fig. 4.
Complementary insight is provided by Fig. 6, which shows the allowed parameter space
in the (mχ , sin θ) plane, with the color gradient indicating the corresponding values of the
Yukawa coupling gχ . All other model parameters are fixed to the same values used in Fig. 4.
The scatter points represent parameter sets that reproduce the observed thermal relic abundance, 0.1 ≤ ΩDM h2 ≤ 0.121 [79]. As the heavy scalar mass increases, the annihilation
cross section becomes progressively more sensitive to the dark-sector Yukawa interaction
and less dependent on the scalar mixing angle. In this large-mh2 regime, the relic density
constraint is therefore only weakly correlated with sin θ, and satisfying the required annihilation rate necessitates a sufficiently large gχ . This behaviour clearly demonstrates the
transition from mixing-driven annihilation in the Higgs-funnel region to Yukawa-dominated
annihilation as the heavy scalar mass scale is increased.
We have selected nine benchmark points (BPs) shown in Tab. 1 from various parts of
the parameter space. The specified BPs remain viable under current experimental scrutiny,
adhering to both cosmological relic density measurements and direct detection constraints.
We perform our analysis primarily for two representative BSM scalar masses, mh2 = 200
GeV and 350 GeV. These mass choices ensure that the additional scalar remains within
the LHC kinematic reach, allowing for potential production and providing an immediate
experimental test of the model. For one of our benchmark scenarios (BP9), we consider
mh2 to be less than the mass of the SM Higgs boson. This choice makes the selected set
of benchmark points1 exhaustive, thereby rendering our systematic investigation complete,
as it covers a wide region of parameter space that satisfies various collider bounds while
simultaneously reproducing the correct DM and EWPT observables.
1

To achieve a SFOEWPT, several benchmarks require large quartic couplings (λhs and λs ). These values
may trigger Landau poles at an intermediate scale, rendering the model as an effective field theory valid
only up to a cutoff Λ. However, because this study targets electroweak-scale phenomena—such as relic
density, direct detection, collider observables, and gravitational wave signals—this feature does not impact
our conclusions.

– 12 –

## PDF page 14

0.3

0.8

0.1

0.4

0.2

0.8

0.1

0.4

g

sin

0.2

1.2

sin

1.2

0.0

0.0
60

100

200

m [GeV]

400 600

g

0.3

0.0

0.0
60

100

200

m [GeV]

400 600

Figure 6: Variation of mixing angle sin θ with DM mass mχ maintaining relic abundance
in the range 0.1 ≤ ΩDM h2 ≤ 0.121. The color gradient represents the Yukawa coupling gχ .
Left panel for mh2 = 200 GeV and right for mh2 = 350 GeV. For both cases, we have taken
λhs = 0.8 and µ3 = −50 GeV.

We do not explore values of mh2 significantly above 350 GeV, since heavier singlet-like
state tend to decouple from the Higgs sector. This decoupling makes it increasingly difficult
to achieve a SFOEWPT which will be discussed in the next section. Compensating for
this behavior would require taking the portal coupling λhs to very large values, which is
theoretically disfavored due to perturbativity constraints. For these reasons, our analysis
is restricted to the region mh2 ≲ 350 GeV.
Achieving a SFOEWPT usually requires an large Higgs portal coupling, which, in turn,
inevitably opens the h1 → h2 h2 decay mode in this mass range, adding a sizable partial
width to the Higgs boson total width. Latest searches for invisible decays and measurement
of total width of the Higgs boson at the LHC put stringent constraints for such mass range
mh2 < mh1 /2 [80]. Therefore, we decide to leave aside the region mh2 < mh1 /2 in our
analysis.
BPs
BP1
BP2
BP3
BP4
BP5
BP6
BP7
BP8
BP9

mh2 [GeV]

sin θ

200.0

0.001

350.0

0.001

350.0
200.0
70.0

0.07
0.13
0.002

λhs
2.2
2.4
1.9
4.3
4.45
4.0
3.8
2.02
0.8

λs
3.38
3.1
2.95
4.5
4.0
4.1
4.8
3.0
0.73

µ3 [GeV]
-20.0
100.0
-100.0
20.0
100.0
-100.0
20.0
20.0
20.0

mχ [GeV]
222.0
242.0
180.0
310.0
380.0
300.0
167.4
94.75
78.0

gχ
0.57
0.56
0.76
0.87
0.73
0.87
0.03
0.02
0.34

Table 1: Benchmark points for singlet scalar extension of the SM along with singlet
fermion dark matter. All the BPs satisfy the observed relic density and bound from the
upper limit of spin-independent DM-nucleon scattering cross section.

– 13 –

## PDF page 15

Tab. 2 presents the corresponding dark matter observables for the same benchmark
points, including the relic abundance (ΩDM h2 ) and the thermally averaged annihilation
cross sections. An interesting observation is that the DM predominantly annihilate into
h1 h1 , h2 h2 , h1 h2 final states in most of the BPs. The dearth of SM fermionic channels in
the DM annihilation is due to the presence of small sin θ and mq in both the vertices of
the Feynman diagram. Moreover, all the annihilation to SM processes are kinematically
s-channel suppressed except at the Higgs resonance. In BP7 and BP8 with relatively larger
sin θ, DM annihilates to SM gauge bosons channels. In most of the BPs the dominant
annihilation channels are the di-scalar boson final states. Though there may appear sin θ
in the triple scalar couplings, but those couplings, at the same time, are proportional to
λhs v. Here, large λhs in the BPs would play a significant role. In particular, there is no
sin θ factor in the h1 − h2 − h2 coupling. Therefore, a large fraction of the annihilation
process χχ → h∗2 → h1 h2 (in BP4,6) can be observed where both vertices are driven by
cos θ. Similarly, in BP1 and BP2, DM mostly annihilates into h2 h2 via predominantly
cos2 θ enhanced t-channel process. In addition to this, the dimensionful parameter µhs will
appear in h2 − h1 − h1 coupling, which fuels χχ → h2 → h1 h1 channel (in BP3).
4.2

Direct detection

In this model, the singlet fermion DM χ interacts with the nuclei through t-channel exchange of the two CP-even mass eigenstates h1 and h2 . Before EWSB, only the SM Higgs
doublet H couples to quarks, while the singlet real scalar field s couples to the dark matter
fermion χ through Yukawa interaction. EWSB enables mixing between the scalars, which
introduces the interaction between the DM and light quarks inside the nuclei. After EWSB,
the couplings of the two scalars with the mass eigenstates to quarks and to dark matter
become:
mq
gχχh1 = −gχ sin θ,
gqqh1 =
cos θ,
(4.1)
v
mq
gχχh2 = gχ cos θ,
gqqh2 =
sin θ.
(4.2)
v
At the momentum transfers relevant for direct detection, both scalars can be integrated
out, which yields the effective scalar interaction
[
(
)]
∑
mq
1
1
Leff =
gχ
sin θ cos θ
(χ̄χ) (q̄q).
(4.3)
2 − m2
v
m
h
h
2
1
q
This form exhibits the characteristic destructive interference between h1 and h2 exchange:
the opposite signs of the effective coefficients arise directly from the single mixing angle.
Matching Eq. (4.3) to the nucleon scalar matrix element,
∑
⟨N |
mq q̄q|N ⟩ = fN mN N̄ N,
fN ≃ 0.30,
(4.4)
q

leads to the familiar spin-independent (SI) DM–nucleon scattering cross section,
[
(
)]2
2 m4
fN
g
sin
θ
cos
θ
1
1
χ
N
σSI =
− 2
.
π(mχ + mN )2
v
m2h2
mh1

– 14 –

(4.5)

## PDF page 16

Fig. 7 shows the predicted SI cross section against DM mass for various (sin θ compared with
the latest limits from the LZ (2024) experiment [81]. For this figure, we consider only the
spin-independent cross section for the neutron, which exceeds that for the proton and thus
provides a conservative estimate. The spin-independent DM-proton/neutron scattering
cross sections (σSI ) for all the BPs are also shown in table 2. Several qualitative features
follow directly from Eq. (4.5):

0.3
SI [cm2]

SI [cm2]

10 45

0.2

10 47

0.1

10 49
10 51

0.0
60

100

200

m [GeV]

0.2

10 47

0.1

10 49
10 51

400 600

0.3

10 45

0.0
60

100

200

m [GeV]

400 600

Figure 7: Variation of nucleon-dark matter spin independent scattering cross-section σSI
with DM mass mχ maintaining relic abundance in the range 0.1 ≤ ΩDM h2 ≤ 0.121. The
color gradient represents the mixing angle sin θ. Left panel for mh2 = 200 GeV and right
for mh2 = 350 GeV. For both cases, we have taken λhs = 0.8 and µ3 = −50 GeV. The solid
green line represents the latest 2σ bound from the LZ (2024) experiment [81].

• Large scalar mixing angle yields a large DM-nucleon scattering cross section, making
large sin θ untenable against the latest LZ (2024) results [81].
• Only for small sin θ, the mediator–nucleon coupling becomes suppressed, pushing
the predicted cross section below the strongest upper limit of spin-independent DMnucleon scattering cross section given by the LZ experiment. In this regime, sizeable
gχ can still yield detectable rates through h2 exchange, provided that mh2 is not too
large.
• The expression inside bracket in Eq. (4.5) can become very small when the two
propagators nearly cancel. This “destructive interference” or “blind-spot” behaviour
produces the dip visible in Fig. 6 for certain combinations of (mh2 , sin θ) and allows
otherwise large-coupling scenarios to evade present bounds.
Overall, direct detection searches significantly restrict regions of parameter space that also
produce the correct thermal relic density. In particular, the relic-favored regions with either
large sin θ or large gχ are often in tension with the XENON1T and LZ bounds, whereas the
h2 -resonance region remains largely viable due to suppressed couplings and the interference
effect described above.
Therefore, the key points extracted from the analysis of relic density and direct detection over the BPs could be summarized as:

– 15 –

## PDF page 17

(p)

(n)

Annihilation
channels
h2 h2 (64%)
h1 h1 (36%)
h2 h2 (71%)
h1 h1 (29%)
h1 h1 (99%)
h2 h2 (1%)

BPs

ΩDM h2

σSI (cm2 )

σSI (cm2 )

BP1

0.119

6.96 × 10−50

7.10 × 10−50

BP2

0.119

6.72 × 10−50

6.86 × 10−50

BP3

0.119

1.24 × 10−49

1.26 × 10−49

BP4

0.120

3.26 × 10−49

3.32 × 10−49

BP5

0.120

2.35 × 10−49

2.40 × 10−49

BP6

0.120

3.33 × 10−49

3.40 × 10−49

BP7

0.119

1.92 × 10−48

1.96 × 10−48

BP8

0.120

1.40 × 10−48

1.44 × 10−48

h1 h2 (100%)
h1 h1 (67%)
W + W − (23%)
ZZ (7%)
+
W W − (74%)
ZZ (26%)

BP9

0.119

1.26 × 10−48

1.28 × 10−48

h2 h2 (100%)

h1 h2 (100%)
h2 h2 (69%)
h1 h1 (31%)

Table 2: Dark matter observables for the benchmark points, including relic abundance,
spin-independent scattering cross sections off protons and neutrons, and dominant annihilation channels.
• At the resonance of h2 (i.e., when mχ ≃ mh2 /2), the dark-matter relic density
becomes essentially independent of all parameters except the dark-matter mass mχ ,
which determines the proximity to the h2 resonance, and the Yukawa coupling gχ ,
which controls the annihilation rate. Since the relic density is insensitive to sin θ in
this regime, the mixing angle may be taken up to the maximum value allowed by
direct-detection bounds as considered in BP7 and BP8 in Tab. 1.
• Throughout the entire parameter space, the relic density is independent of the scalar
quartic coupling λs . This coupling does not affect the dominant dark-matter annihilation processes and therefore does not influence the relic-abundance calculation.
• In the region where the dark-matter mass satisfies mχ ⪆ mh2 , the relic density is
mostly insensitive to sin θ, but can be achieved only for relatively large values of gχ
(e.g., BP1, BP2 BP5 and BP9). However, larger gχ enhances spin independent direct
detection cross section. Therefore, σSI permits only very small values of the mixing
angle sin θ.
• In the Higgs-funnel region, where mχ ≈ mh1 /2 and thus lies far from the degenerate
regime mχ ≈ mh2 , the correct dark-matter relic density can be obtained only for
comparatively large values of the mixing angle sin θ. However, such large mixing
angles are generally excluded by current direct-detection constraints.

– 16 –

## PDF page 18

• For BP1 to BP6, where mχ ≃ mh2 (the degenerate region), a relatively large coupling
gχ is required to achieve the correct relic abundance. In contrast, in BP9 the relic
density can be reproduced with a smaller value of gχ , owing to the lighter mass of
the scalar h2 .
4.3

Future collider prospects

The non-resonant production of h1 h2 and h2 h2 at the LHC serves as a direct probe of the
extended Higgs potential. While these processes are suppressed by the small mixing angle
sin θ, their cross sections are fundamentally governed by the trilinear couplings λ112 and
λ122 . These couplings can remain substantial even when mixing is minimal, reflecting the
underlying symmetry-breaking scale of the singlet sector.
We compute the partonic production cross sections for the non-standard di-scalar
√
final states pp → h1 h2 and pp → h2 h2 at s = 14 TeV. The model is implemented
in FeynRules v2.3 [82], with the UFO output generated using NLOCT [83] and the UFO
interface [84, 85]. The cross sections are then evaluated in MadGraph5 aMC@NLO [72] using
the NNPDF23LO PDFs [86, 87].
For BP1-BP7, the predicted cross sections for both pp → h1 h2 and pp → h2 h2 remain far below the femtobarn level, reflecting the suppressed production of the non-SM
scalar states induced by the small Higgs-singlet mixing. An exception is BP8, where the
di-scalar rates are comparatively enhanced and reach the sub-femtobarn level, making this
benchmark the most promising target among the set for HL-LHC or future hadron-collider
searches. While BP9 features a much lighter h2 , in this benchmark, the non-standard
di-scalar signal is driven primarily by the available phase space rather than mixing enhancement, and its detailed collider prospects depend on dedicated analyses beyond the
scope of the present work.
An interesting observation is that the enhancement observed for BP8 is correlated
with a resonant configuration in which the dark-matter mass lies close to mh2 /2. To verify
this behaviour, we explicitly vary mχ in the vicinity of the resonance and find that the
scalar mixing angle can increase to moderately larger values while remaining consistent
with current collider and direct-detection constraints. As a consequence, the associated
production rate of the heavier scalar is significantly enhanced. In this resonant regime, the
associated production of the heavier scalar can approach the femtobarn level, potentially
placing such scenarios within the projected sensitivity of the HL-LHC and making them
interesting targets for future high-energy hadron colliders, such as the FCC-hh. A detailed
collider-level analysis of these channels is deferred to future work, as the present study
primarily focuses on cosmological probes, in particular the electroweak phase transition
and the associated stochastic gravitational-wave signatures.
While direct-detection experiments and collider searches impose strong and complementary constraints on the parameter space, they do not fully probe the regions favoured
by dark-matter phenomenology. In particular, the requirement of satisfying current directdetection bounds forces the scalar mixing angle to be very small, which in turn strongly
suppresses the production rates of the heavy scalar at colliders. As a result, much of the

– 17 –

## PDF page 19

viable parameter space is simultaneously difficult to access through both direct-detection
experiments and collider searches.
This motivates the exploration of complementary probes that are sensitive to the
thermal history of the scalar sector. In particular, the dynamics of the EWPT provide a
powerful handle on the underlying scalar interactions. A SFOEWPT sources a stochastic
GW background, offering an alternative observational window into regions of parameter
space that may remain inaccessible to conventional collider and direct-detection probes. We
therefore proceed to analyse the EWPT and the associated GW signatures of the model.

5

Electroweak phase transition and GW detection

To study the EWPT, we analyze the finite-temperature effective potential, starting from
the one-loop zero-temperature potential and incorporating the thermal corrections that
shape the phase transition dynamics. We then examine the associated stochastic GW
signal and assess its detectability in future experiments.
5.1

One-loop effective potential

The one-loop effective potential depends entirely on the field-dependent mass-squared
eigenvalues m2i (φ) of all bosonic and fermionic degrees of freedom, obtained by diagonalizing the corresponding tree-level mass matrices evaluated on the background field configuration φ = (h, s). For the CP-even scalar sector, the field-dependent mass-squared
matrix elements are
∂ 2 V0
λhs 2
= µ2h + 3λh h2 +
s + µhs s,
∂h2
2
λhs 2
∂ 2 V0
= µ2s + 3λs s2 +
h + 2µ3 s,
m2ss (h, s) ≡
∂s2
2
∂ 2 V0
m2hs (h, s) ≡
= λhs hs + µhs h.
∂h ∂s

m2hh (h, s) ≡

(5.1)
(5.2)
(5.3)

For the CP-odd Goldstone bosons χi , the field-dependent mass-squared is
m2χi (h, s) = µ2h + λh h2 +

λhs 2
s + µhs s.
2

(5.4)

The field-dependent masses of the SM fermions and electroweak gauge bosons read
1
g2
g 2 + g ′2 2
m2i (h) = yi2 h2 ,
m2W (h) = h2 ,
m2Z (h) =
h ,
(5.5)
2
4
4
√
where yi = 2 mi /v denotes the Yukawa coupling of fermion species i, where mi is the
corresponding fermion mass at zero temperature. The parameters g and g ′ are the gauge
couplings associated with the SU (2)L and U (1)Y gauge groups. For the numerical analysis,
we include all charged leptons and quarks.
The field-dependent mass of the BSM Dirac fermion χ is
mχ (s) = mχ − gχ s,

– 18 –

(5.6)

## PDF page 20

where gχ is the Yukawa coupling mentioned earlier.
The one-loop correction to the zero-temperature effective potential, known as the Coleman–Weinberg (CW) potential [88], arises from the sum of all one-particle-irreducible vacuum diagrams and encodes quantum fluctuations around the classical background field. In
M S scheme, its explicit form follows the standard expression [89]
CW
V1−loop
(h, s) =

]
[ ( 2
)
mi (h, s)
1 ∑
4
ni mi (h, s) log
− Ci .
64π 2
µ2

(5.7)

i

Here, µ denotes the renormalization scale of the theory. The constants Ci take the value
3/2 for scalars, fermions, and the longitudinal components2 of gauge bosons, while Ci = 1/2
for the transverse gauge modes [90–92]. The corresponding degrees of freedom are assigned
in the usual manner for bosonic and fermionic fields3 are
nWL = 2, nWT = 4, nZL /γL = 1, nZT = 2, nh/s/χi = 1, nq = −12, nℓ/χ = −4.

(5.8)

Here, q and ℓ denote the quarks and charged leptons, respectively. In the MS renormalization scheme, the choice of the renormalization scale µ introduces an intrinsic theoretical
uncertainty in thermodynamic quantities such as the critical and nucleation temperatures,
as well as in derived observables relevant for the electroweak phase transition [93–96]. The
explicit scale dependence of the one-loop Coleman-Weinberg potential can, in principle, be
reduced by employing an RGE-improved treatment of the effective potential, as formulated
in Refs. [97, 98].
In this work, we do not attempt a systematic study of renormalization-scale or gauge
uncertainties. Our analysis is instead intended to identify regions of parameter space that
robustly exhibit a strong first-order electroweak phase transition and potentially observable
gravitational-wave signals. For the benchmark points considered, we have checked that
moderate variations of the renormalization scale around the characteristic mass scales do
not alter the qualitative features of the phase transition.
More refined treatments based on dimensionally reduced effective field theory approaches can further reduce theoretical uncertainties and are left for future work [99–104].
For definiteness, throughout our numerical analysis, we fix the renormalization scale to
µ = mt .
The one-loop CW correction generically shifts both the vacuum location and the curvature of the scalar potential, thereby modifying the VEVs and physical masses at zero
temperature. These effects are removed by introducing a counterterm potential Vct (h, s)
that cancels the loop-induced deviations and restores the tree-level vacuum structure. The
counterterms are fixed by renormalization conditions that enforce the tree-level stationarity of the potential at the chosen VEVs and preserve its curvature, ensuring that the Higgs
and singlet masses remain at their tree-level values. The counterterm potential takes the
2

At high temperatures, the photon acquires field-dependent thermal mass and mixes with the longitudinal component of the Z boson, as discussed later.
3
A closed fermion loop contributes an extra minus sign due to the anticommutation of fermionic fields
in the trace, which is absorbed into the corresponding degrees of freedom.

– 19 –

## PDF page 21

form [67]
Vct (h, s) =

δµ2h 2 δλh 4 δµ2s 2 δµhs 2
h +
h +
s +
h s + δa1 s.
2
4
2
2

(5.9)

with the coefficients (e.g., δµ2h ) fixed by these renormalization conditions. The procedure
for determining the counterterm coefficients, along with their expressions in terms of derivatives of the CW potential, is presented in App. A.
The one-loop finite-temperature contribution to the effective potential is given by [105,
106]:
[
( 2
) ∑
)]
( 2
mF (h, s)
mB (h, s)
T4 ∑
T
+
nF JF
,
(5.10)
V1−loop (h, s, T ) = 2
nB J B
2π
T2
T2
F

B

where B = {WL/T , ZL/T , γL , h, s, χ1,2,3 } includes all bosonic degrees of freedom, and F
contains the six quarks, three charged leptons, and the BSM Dirac fermion χ. The thermal
bosonic and fermionic functions are
( 2
) ∫ ∞
)
(
√
m (h, s)
2
− x2 +m2 (h,s)/T 2
JB/F
,
(5.11)
=
dx
x
log
1
∓
e
T2
0
with the upper (lower) sign corresponding to bosons (fermions). For particles whose field–
dependent masses satisfy m2 (h, s) ≫ T 2 , the thermal functions JB,F become exponentially
Boltzmann suppressed. As a result, such heavy states contribute negligibly to the finite
temperature effective potential and thus have no significant impact on the dynamics of the
electroweak phase transition.
In the high-temperature limit, T 2 ≫ m2 , these functions admit the standard expansions [89]:
( 2)
( 2 )
m
π 4 π 2 m2 π (m2 )3/2
m4
m
JB
=− +
−
−
ln
+ ··· ,
(5.12)
2
2
3
4
T
45 12 T
6 T
32T
ab T 2
( 2)
( 2 )
m
7π 4 π 2 m2
m4
m
JF
=
−
−
ln
+ ··· ,
(5.13)
T2
360 24 T 2
32T 4
af T 2
where
af = π 2 e3/2−2γE ,

ab = 16π 2 e3/2−2γE ,

and γE = 0.577 is the Euler–Mascheroni constant. The first terms in the above two equations are field-independent and only shift the vacuum energy, leaving the phase transition
dynamics unaffected. The dominant contributions at finite temperature arise from the
quadratic m2 terms; therefore, particles with lighter field-dependent masses contribute
subleading corrections to the effective potential and have negligible impact on the phase
transition.
Ring resummation
At finite temperature, bosonic contributions to the effective potential suffer from infrared
divergences when the corresponding field-dependent masses become small [94, 107, 108].

– 20 –

## PDF page 22

These divergences originate from the zero Matsubara modes of the bosonic degrees of
freedom and are removed by incorporating the leading daisy (ring) diagrams. The ringimproved contribution to the effective potential is [106, 109, 110]
Vring (h, s, T ) = −

[(
)3/2 ( 2
)3/2 ]
T
ni m2i (h, s, T )
− mi (h, s)
,
12π

(5.14)

where m2i (h, s, T ) are the thermally resummed Debye masses. These resummed masses are
obtained by including the leading temperature-dependent self-energy corrections,
m2i (h, s, T ) = m2i (h, s) + Πi T 2 ,

(5.15)

where Πi represents the one-loop thermal self-energy of the corresponding field.
Using the high-temperature expansion of the thermal functions, the CP-even scalar
thermal self-energies are given by
y2
3g 2 g ′2 yq2
λh λhs
+
+
+ ℓ +
+
,
16
16
4
12
2
24
λhs
λs λhs gχ2
+
+ , Πhs =
.
Πss =
4
6
6
12

Πhh =

(5.16)
(5.17)

The CP-odd Goldstone bosons receive the same thermal correction as the Higgs direction,
Π χi =

y2
3g 2 g ′2 yq2
λh λhs
+
+
+ ℓ +
+
.
16
16
4
12
2
24

(5.18)

As in the previously given expressions for the mass–squared matrix elements in Eqs. (5.1)–
(5.3), once the thermal mass contributions (Debye masses) are included, the temperaturedependent mass-squared matrix of the CP-even scalars in the (h, s) basis is given by
)
(
)
(
2 (h, s) m2 (h, s)
Π
Π
m
hh
hs
hs
hh
,
+ T2
M 2 (h, s, T ) =
m2hs (h, s) m2ss (h, s)
Πhs Πss

(5.19)

and its eigenvalues correspond to the thermally corrected CP-even scalar masses. On the
other hand, the longitudinal components of the electroweak gauge bosons acquire Debye
masses in the thermal plasma. For the charged gauge bosons, the resummed thermal mass
takes the form [44, 110]
11
m2WL (h, T ) = m2WL (h) + g 2 T 2 .
(5.20)
6
In the neutral sector, the longitudinal components of the Z boson and the photon mix at
finite temperature. The corresponding thermal mass-squared matrix is [44, 110]
(
M2L (h, T ) =

1 2 2
11 2 2
− 41 gg ′ h2
4g h + 6 g T
1 ′2 2
11 ′2 2
− 41 gg ′ h2
4g h + 6 g T

)
,

whose eigenvalues give the temperature and field-dependent masses of ZL and γL .

– 21 –

(5.21)

## PDF page 23

5.2

Electroweak phase transition

The full one-loop effective potential at finite temperature is given by
CW
T
Veff (h, s, T ) = V0 (h, s) + V1−loop
(h, s, T ) + V1−loop
(h, s, T ) + Vct (h, s)

(5.22)

CW (h, s, T ), V T
where the individual contributions V0 (h, s), V1-loop
1-loop (h, s, T ), and Vct (h, s) are
CW (h, s, T )
defined in Eqs. (2.5), (5.7), (5.10), and (5.9), respectively. The CW term V1-loop
becomes explicitly temperature dependent once thermal screening is incorporated through
Daisy (ring) resummation, which regulates infrared divergences from bosonic zero modes
[94, 107, 108]. This may be done either by adding the ring contribution Vring (h, s, T ) [109]
or by replacing the bosonic masses with their thermally corrected counterparts m2i (h, T )
[111]; in this work, we follow the latter. Furthermore, each term in Eq. (5.22) acquires an
implicit temperature dependence through the thermal evolution of the VEV of the scalars.
For a given choice of parameters, the critical temperature Tc and the corresponding
VEVs of the Higgs field vc and the singlet field sc are determined by the conditions
∂Veff (h, s, Tc ) ∣∣
∂Veff (h, s, Tc ) ∣∣
=
0,
= 0,
(5.23)
∣
∣
∂h
∂s
ϕlow
ϕhigh
Veff (ϕlow , Tc ) = Veff (ϕhigh , Tc ),
(5.24)

where the two degenerate vacua at Tc are given by ϕlow ≡ (h = vc , s ≈ 0) and ϕhigh ≡ (h ≈
0, s = sc ). The strength of the phase transition along each field direction is quantified by
ξh =

vc
,
Tc

ξs =

sc
.
Tc

(5.25)

A SFOEWPT requires ξh ≳ 1 along the Higgs direction. In this work, we employ the
CosmoTransition package [90] to determine the phase transition pattern and to compute
Tc together with the field VEVs at the critical temperature.
In our analysis, we find that phase transitions take place in two steps. At very high
temperatures, the Universe resides in a phase where the singlet field develops a small but
nonvanishing4 VEV while the Higgs VEV remains zero, corresponding to (h, s) = (0, w1 ).
As the temperature decreases, the system undergoes a smooth crossover along the singlet
direction, transitioning to a vacuum configuration (0, w2 ) with w2 > w1 . Upon further
cooling, a SFOEWPT occurs from (0, sc ) → (vc , 0), with sc > w2 , once the Higgs field
acquires a nonzero VEV at the critical temperature Tc . For illustration, the phase transition
pattern corresponding to BP8 is displayed in Fig. 8, where the thermal evolution of the
Higgs and singlet VEVs clearly shows the sequential two-step transition discussed above.
For all benchmark points examined, the second step of the transition is strongly first
order along the Higgs direction, with the order-parameter ratio satisfying ξh ≡ vc /Tc ≳ 1
(see Tabs. 3 and 4). In contrast, only BP9 exhibit a strong first-order transition simultaneously along both scalar-field directions. As shown in Tabs. 3 and 4, the phase transition
4

At very high temperatures, the singlet scalar generally retains a nonzero VEV. Since the model lacks a
discrete symmetry, explicit Z2 -breaking terms prevent the restoration of the full symmetry along the singlet
direction, inducing a VEV that is suppressed but not exactly zero. Therefore, the finite-temperature effective
potential admits a nonzero minimum along the direction of the singlet field in the early Universe [66].

– 22 –

## PDF page 24

strengths ξh and ξs are comparatively weaker for BP4–BP7, which correspond to a heavier mass of the singlet scalar with mh2 = 350 GeV. For BP1–BP3 and BP8, where the
singlet scalar is lighter with mh2 = 200 GeV, the transition becomes noticeably stronger.
By contrast, BP9 yields a very strong transition in both field directions. This behavior is
consistent with the fact that when the additional scalar lies significantly above the electroweak scale, it effectively decouples from the thermal bath relevant for the electroweak
phase transition. Consequently, its contribution to the one-loop finite temperature effective potential is suppressed, reducing its influence on the transition dynamics, as discussed
earlier.
For the zero-temperature vacuum structure considered in this work, the primary parameter governing the electroweak phase transition is the Higgs portal coupling λhs , which
serves as a free input of the model. Achieving a SFOEWPT typically requires larger values
of λhs as the singlet-like scalar mass mh2 increases. The singlet quartic coupling λs also
plays an important role, as it significantly influences the shape of the scalar potential and
thereby the transition dynamics.
From the perspective of direct-detection constraints, the Higgs–singlet mixing angle
must be very small, which in turn implies that the associated trilinear coupling µhs is highly
suppressed. As a result, µhs has a subdominant role on the phase-transition dynamics. The
impact of the singlet trilinear coupling µ3 on the EWPT in this setup can be summarized
as follows. A sizable negative value of µ3 tends to enhance the barrier in the effective
potential, thereby strengthening the phase transition. Consequently, for a fixed singlet
mass, a relatively smaller Higgs portal coupling is sufficient to realize a SFOEWPT. In
contrast, when µ3 is positive and large, its contribution weakens the transition, requiring
a larger value of λhs to get a SFOEWPT. We also find that a SFOEWPT can be achieved
even when µ3 is set to zero. In the limit µ3 = 0 and µhs → 0, the model effectively reduces
to a Z2 -symmetric scalar extension, for which the correlation between λhs and the singlet
mass has been extensively discussed in Refs. [7, 29, 32, 112].
Finally, we comment on the role of the BSM fermion χ in EWPT. Its contributions
to the effective potential come from three sources. First, through thermal resummation,
χ induces a temperature-dependent correction to the singlet scalar thermal mass via its
Yukawa interaction (see Eq. (5.17)). In addition, χ contributes at one loop through both
the CW correction and the finite-temperature part of the potential. These fermionic contributions can affect the phase transition, with their impact controlled primarily by the
mixed term 2gχ mχ sc appearing in the field-dependent fermion mass squared evaluated at
the critical temperature. When this combination becomes comparable to Tc2 , the fermionic
contribution to the effective potential is maximized, thereby exerting its strongest influence
on the phase-transition dynamics.
5.3

Stochastic gravitational waves

As the temperature of the Universe drops below the critical temperature Tc , the electroweaksymmetric phase becomes metastable, and the transition to the true vacuum proceeds via
thermal tunneling through the potential barrier. This process occurs through the nucleation of critical bubbles of the broken phase, whose probability is governed by the

– 23 –

## PDF page 25

100

250

80

200

60

s(T) [GeV]

h(T) [GeV]

300

150
100
50

40
20
0

0
0

50

100

150

T [GeV]

200

250

20

300

0

100

200

300

T [GeV]

400

500

Figure 8: Evolution of VEVs of the scalars with temperature for BP8.
PT param.
(v, s)|high
Tc
(v, s)|low
Tc
Tc
(ξh , ξs )
(v, s)|high
Tn
(v, s)|low
Tn
Tn
αn
β/Hn

BP1

BP2

BP3

BP4

BP5

BP6

(0, 85)
(1, 81)
(1, 90)
(3, 49)
(4, 46)
(5, 47)
(199, 4)
(196, 3)
(194, 7)
(151, 4)
(141, 2)
(143, 6)
108
109
111
122
124
125
(1.84, 0.84) (1.79, 0.72) (1.74, 0.75) (1.21, 0.37) (1.10, 0.35) (1.10, 0.33)
(0, 87)
(0, 83)
(0, 92)
(3, 49)
(4, 47)
(5, 47)
(225, 1)
(221, 1)
(218, 3)
(167, 2)
(158, 1)
(156, 4)
87
91
95
118
120
122
0.07
0.06
0.05
0.02
0.02
0.02
428
789
772
4525
5902
8874

Table 3: Phase transition parameters. VEVs and temperatures units of GeV.
PT param.
(v, s|high
Tc
(v, s)|low
Tc
Tc
(ξh , ξs )
(v, s)|high
Tn
(v, s)|low
Tn
Tn
αn
β/Hn

BP7

BP8

BP9

(2, 50)
(1, 83)
(0, 148)
(175, 6)
(201, 6)
(232, 5)
116
108
78
(1.49, 0.38) (1.85, 0.71) (2.97, 1.83)
(2, 52)
(1, 86)
(1, 149)
(196, 4)
(226, 2)
(245, 1)
107
86
43
0.03
0.06
0.35
2030
719
587

Table 4: Phase transition parameters. All the VEVs and temperatures are in units of
GeV.

finite-temperature Euclidean (bounce) action [113–115]. The bounce action exponentially
suppresses the tunneling rate and determines the temperature at which the phase transition
effectively becomes complete.

– 24 –

## PDF page 26

In the finite-temperature regime relevant for the EWPT, the dominant tunneling configuration is O(3) symmetric, and the corresponding bounce solution is obtained by minimizing the three-dimensional Euclidean action constructed from the finite-temperature
effective potential [113, 116]. The associated bounce equation must satisfy regularity at
the bubble center and approach the false vacuum at large distances, ensuring a physically
consistent nucleation process.
In this work, the bounce action and the nucleation temperature are computed numerically using the CosmoTransitions package [90], which provides a reliable and efficient
framework for analyzing multi-field first-order phase transitions. This allows us to accurately determine the thermal tunneling dynamics and to characterize the EWPT relevant
for our benchmark scenarios.
With the phase transition dynamics determined, the resulting evolution of the scalar
fields leads to the formation and expansion of bubbles of the broken phase, whose subsequent collisions source a stochastic gravitational-wave background. Two parameters play
a central role in characterizing the GW signal from a first-order phase transition: the transition strength parameter αn and the inverse duration parameter β, both evaluated at the
nucleation temperature Tn .
The parameter αn is defined as the ratio of the latent heat released during the transition
to the radiation energy density,
∆ρ
αn =
,
(5.26)
ρrad
where ρrad = π 2 g∗ Tn4 /30 is the radiation energy density, with g∗ denoting the effective
number of relativistic degrees of freedom. For the SM, g∗ = 106.75 [117]. The latent heat
∆ρ is computed as [46, 118]
[
]
]
dVeff (ϕn , T )
dVeff (ϕ0 , T )
− Veff (ϕn , T ) − T
,
∆ρ = Veff (ϕ0 , T ) − T
dT
dT
T =Tn
T =Tn
[

(5.27)

where ϕ0 and ϕn correspond to the field values in the false and true vacua at Tn , respectively.
Their numerical values are summarized in Tabs. 3 and 4.
The inverse duration of the phase transition is quantified by the parameter β, defined
as
(
)∣
β
d SE (T ) ∣∣
= Tn
,
(5.28)
∣
∣
Hn
dT
T
T =Tn

where Hn denotes the Hubble expansion rate at the nucleation temperature. The nucleation temperature Tn is determined by solving the condition SE (Tn )/Tn ≃ 140, which
corresponds to the onset of efficient bubble nucleation [90].
The stochastic GW background generated by a first-order phase transition receives
contributions from three main sources: bubble wall collisions, sound waves in the plasma,
and magneto-hydrodynamic (MHD) turbulence. The total present-day GW energy density
spectrum can be expressed as [119]
ΩGW h2 ≃ Ωcol h2 + Ωsw h2 + Ωtur h2 ,

– 25 –

(5.29)

## PDF page 27

where h = H0 /(100 km s−1 Mpc−1 ) is the dimensionless Hubble parameter, with H0 being
the present-day Hubble constant [120]. The resulting GW spectrum thus provides a direct
observational probe of the underlying particle physics responsible for the phase transition.
The GW contribution sourced by bubble wall collisions can be computed using the
envelope approximation [121]. The resulting energy density spectrum as a function of
frequency f is given by
) (
) (
) (
)
(
3
0.11vw
3.8 (f /fcol )2.8
β −2 κc αn 2 100 1/3
2
−5
,
Ωcol h = 1.67 × 10
2
Hn
1 + αn
g∗
0.42 + vw
1 + 2.8 (f /fcol )3.8
(5.30)
where vw is the bubble wall velocity and κc is the efficiency factor describing the fraction of
vacuum energy converted into the kinetic energy of the bubble walls. The efficiency factor
is parametrized as
√
κc =

4
0.715αn + 27

3αn
2

.
1 + 0.715αn
The redshifted peak frequency associated with the collision contribution is
( )(
) ( ∗ )1/6
)(
β
g
Tn
−6 f∗
fcol = 16.5 × 10
Hz,
β
Hn
100 GeV
100

(5.31)

(5.32)

where the fitting function f∗ /β is given by [121]
f∗
0.62
=
.
2
β
1.8 − 0.1vw + vw

(5.33)

In the following analysis, we assume vw = 1 [46, 122], corresponding to relativistic bubble
expansion.
A dominant contribution to the GW signal typically arises from sound waves generated
in the plasma after bubble percolation [123–125]. The corresponding GW energy density
spectrum is
(
)
(
) (
) (
) [
]7/2
β −1
κsw αn 2 100 1/3 f 3
7
2
−6
Ωsw h = 2.65×10 Υ(τsw )
vw
,
Hn
1 + αn
g∗
fsw
4 + 3 (f /fsw )2
(5.34)
where κsw denotes the efficiency factor associated with the conversion of latent heat into
bulk fluid motion [46, 126],
√
αn
√
.
(5.35)
κsw =
0.135 + 0.98 + αn
The peak frequency of the sound wave contribution is given by
( )(
)(
) ( ∗ )1/6
1
β
Tn
g
−5
fsw = 1.9 × 10
Hz.
vw
Hn
100 GeV
100

(5.36)

The factor Υ(τsw ) accounts for the finite lifetime of the sound wave period and is defined
as
1
Υ(τsw ) = 1 − √
,
(5.37)
1 + 2τsw H∗

– 26 –

## PDF page 28

where τsw denotes the sound wave lifetime. Following Ref. [125], we approximate τsw ≈
Rn /U f , with the mean bubble separation Rn = (8π)1/3 vw βn−1 and the root-mean-squared
√
fluid velocity U f = 3κsw αn /4.
Finally, MHD turbulence generated in the fully ionized plasma provides an additional
GW source [127]. The corresponding contribution to the GW energy density spectrum is


(
)−1 (
)3/2 (
)1/3
3
β
κtur αn
100
(f /ftur )

) ,
(
Ωtur h2 = 3.35 × 10−4
vw
Hn
1 + αn
g∗
[1 + (f /f )]11/3 1 + 8πf
tur

h∗

(5.38)
(
−6

) ( g∗ )1/6

Tn
where h∗ = 16.5 × 10
Hz is the redshifted inverse Hubble time at GW
100 GeV
100
production. The peak frequency of the turbulence contribution is

ftur = 2.7 × 10

−5 1

vw

(

β
Hn

)(

Tn
100 GeV

)(

g∗
100

)1/6
Hz.

(5.39)

The turbulence efficiency factor is taken to be κtur = ϵκsw , where ϵ parametrizes the fraction
of bulk kinetic energy converted into turbulent motion. Following previous studies [128],
we adopt κtur ≃ 0.1 κsw in our numerical analysis.
To illustrate the GW phenomenology of the model, we evaluate the spectra for the
benchmark points listed in Tabs. 3 and 4. The resulting predictions are shown in Fig. 9.
For this analysis, we consider the “runaway” scenario, in which the bubbles of the broken
phase accelerate rapidly and reach velocities close to the speed of light. This assumption
is well motivated in the parameter space of our model, where the released vacuum energy
is sufficiently large to overcome plasma friction. In this regime, GWs are generated predominantly from the sound wave as the bubble wall pushes its way through the plasma
at relativistic speed 5 . The next largest contribution comes from collisions of the bubbles
expanding at high velocity. The amplitude of the GW energy density generated from the
turbulence of the medium becomes subdominant. The individual contributions to the total spectrum: the sound-wave component Ωsw h2 (top right), the turbulence contribution
Ωtur h2 (bottom left), and the bubble-collision envelope component Ωcol h2 (bottom right).
A few general features emerge from this analysis. First, since the peak frequency
scales inversely with the critical temperature, benchmarks with larger Tc naturally produce
spectra shifted toward higher frequencies, whereas those with lower Tc give rise to peaks
lying in the optimal sensitivity window of space-based interferometers. Second, the overall
amplitude of the spectrum increases with the strength of the phase transition, parametrized
by α, and conversely decreases with increasing β/Hn . The strength of the phase transition
and hence, the amplitude of the resultant gravitational wave increases as Tc − Tn increases,
which signifies how supercooled the universe was during the bubble nucleation. The GW
spectrum tends to become less pronounced as the scalar mass increases, as can be observed
from Fig. 9 where BP9 with mh2 = 70 GeV produces a much higher peak than BP4 with
mh2 = 350 GeV (see Tab. 1).
5

In non-runaway regimes, friction between bubble walls and the surrounding plasma prevents relativistic
runaway motion, causing long-lived acoustic waves to dominate the GW production [129].

– 27 –

## PDF page 29

BP7
BP8
BP9

ΩGWh

2

10-13
10-16

BP1

10-10

BP7

10-13

10-19

10-22

10-22
0.1

100

BP8
BP9

10-16

10-19

10-4

LISA
BBO
DECIGO
ET
CE
HLVK
UD
UDC
DC

BP4

2

LISA
BBO
DECIGO
ET
CE
HLVK
UD
UDC
DC

BP4

Ωswh

BP1

10-10

105

10-4

f [Hz]

Ωturh

2

BP9

10-16

10-10

BP7

10-13

10-19

10-22

10-22
100

BP8
BP9

10-16

10-19

0.1

LISA
BBO
DECIGO
ET
CE
HLVK
UD
UDC
DC

BP4

2

BP8

10-4

105

BP1

Ωcolh

LISA
BBO
DECIGO
ET
CE
HLVK
UD
UDC
DC

BP4
BP7

10-13

100

f [Hz]

BP1

10-10

0.1

105

10-4

f [Hz]

0.1

100

105

f [Hz]

Figure 9: Variation of gravitational amplitudes with frequency. The top left panel shows
the resultant GW spectrum, and the top right only the sound wave. The bottom left only
shows turbulence, and the bottom right panel shows only the bubble collision. The shaded
regions represent the projected sensitivity curves of future gravitational wave interferometers—LISA [130], BBO [131], DECIGO [132], Einstein Telescope (ET) [133], Cosmic Explorer (CE) [134], HLVK (Hanford (LIGO)-Livingston (LIGO)-Virgo-KAGRA) [135–137],
ultimate-DECIGO (UD), DECIGO-corr (DC) and ultimate-DECIGO-corr (UDC) [132] —
as indicated by the legend in the inset.

Several of our benchmark points lead to GW spectra with amplitudes that fall within
the projected sensitivity of next-generation experiments. In particular, the spectra corresponding to BP9 exhibit the largest signal, featuring a peak around f ∼ 0.01 Hz that lies
well within the expected discovery reach of LISA [130], BBO [131], and DECIGO [132].
Moreover, this framework can also be probed by proposed experiments targeting the higherfrequency band f ∼ 1–10 Hz, such as UD and UDC, providing an additional avenue for
testing the model. In fact, the GW amplitude is highest for BP9, since both Tc − Tn
and the corresponding strength parameter αn take their largest values in this benchmark.
By contrast, BP4 produces a significantly weaker signal that remains below the projected
reach of most planned detectors. Nevertheless, it can still be probed by Ultimate-DECIGO
and correlated-DECIGO [132]. On the other hand, the sensitivities of HLVK [135–137],
ET [133], and CE [134] (see the caption of Fig. 9 for the nomenclature) are insufficient to
test this scenario.
The wide range of frequencies present in the predicted GW spectra for this model, in
association with the varied sensitivity curves of existing and future GW detectors, under-

– 28 –

## PDF page 30

scores a key point: different GW observatories are complementary in their ability to probe
such an extended scalar sector model that predicts a SFOEWPT.

6

Summary and conclusions

In this work, we revisited a minimal and well-motivated extension of the Standard Model
in which a SM gauge-singlet Dirac fermion χ constitutes the dark matter candidate and
interacts with the visible sector through a real SM gauge-singlet scalar s. The scalar couples
to the SM Higgs doublet via cubic and quartic Higgs-portal interactions and mixes with
the Higgs after electroweak symmetry breaking. A central structural feature of this setup
is that the singlet scalar does not acquire a vacuum expectation value at zero temperature.
Consequently, the Higgs-singlet mixing is controlled entirely by the dimensionful portal
parameter µhs , while the quartic portal coupling λhs governs the finite-temperature scalar
potential.
This separation of roles has important phenomenological consequences. In particular,
the coupling λhs , which drives the strength of the EWPT, is largely decoupled from the
parameters controlling collider observables and dark-matter direct-detection rates. This
allows the model to avoid the tension typically encountered in singlet-extended scenarios
between achieving a strong first-order EWPT and satisfying experimental constraints.
We first imposed perturbative unitarity and vacuum-stability requirements on the
scalar potential. Collider and electroweak precision data further restrict the viable parameter space. Using the combined ATLAS Higgs signal-strength measurement, we obtained an
approximate 95% confidence-level bound | sin θ| ≲ 0.24, largely independent of the heavyscalar mass. Direct searches for heavy scalar resonances decaying into ZZ, W W , and h1 h1
final states further constrain the mixing angle to | sin θ| ≲ O(0.1) for mh2 ≲ 600 GeV.
Taken together, these results confine the model to a region with small but non-negligible
scalar mixing.
We then carried out a detailed analysis of the dark-matter phenomenology. Thermal
freeze-out of χ is dominated by scalar-mediated annihilation channels such as χχ̄ → hi hj
(i, j = 1, 2), with additional contributions from annihilation into SM final states near scalar
resonances. The observed relic abundance selects viable regions of parameter space with
distinct characteristics. In the Higgs-resonance region, achieving the correct relic density
typically requires relatively large mixing angles. In contrast, near the singlet-resonance
regime mχ ≃ mh2 /2, the observed abundance can be obtained over a wider range of sin θ
and gχ values. For mχ ≳ mh2 , the relic density is reproduced only for comparatively large
Yukawa couplings, with a reduced dependence on the mixing angle.
Direct-detection constraints play a dominant role in shaping the allowed parameter
space. The spin-independent dark-matter-nucleon scattering cross section depends sensitively on the scalar mixing angle and the heavy-scalar mass. Current bounds exclude large
mixing angles, while values as small as sin θ ∼ 10−3 remain well below present experimental
sensitivity even for O(1) Yukawa couplings. In addition, destructive interference between
the two scalar propagators gives rise to blind-spot regions where the scattering cross section is strongly suppressed. A combined analysis of relic density and direct-detection

– 29 –

## PDF page 31

constraints shows that several benchmark points lie close to the 2σ exclusion boundary of
current experiments.
From the collider perspective, the production rates for non-standard di-scalar final
states are generally suppressed due to the small Higgs-singlet mixing. For benchmark points
BP1-BP7, both pp → h1 h2 and pp → h2 h2 cross sections lie well below the femtobarn level.
An exception is BP8, for which the rates reach the sub-femtobarn level, making it the most
promising benchmark for future collider sensitivity. In BP9, the enhancement of di-scalar
production is primarily driven by phase-space effects associated with the lighter h2 mass
rather than by an increased mixing angle.
An important observation is that the enhancement observed for BP8 is correlated
with a resonant configuration in which the dark-matter mass lies close to mh2 /2. By
explicitly varying mχ near this resonance, we find that the scalar mixing angle can increase
to moderately larger values while remaining consistent with current collider and directdetection constraints. As a result, the associated production rate of the heavier scalar
is enhanced and can approach the femtobarn level. Such configurations may therefore
become accessible at the HL-LHC and constitute well-motivated targets for future highenergy hadron colliders such as the FCC-hh. A detailed collider-level analysis is left for
future work.
The central novelty of this study lies in the interplay between the dark-matter sector
and the electroweak phase transition. Using CosmoTransitions, we demonstrated that
the model exhibits a robust two-step phase-transition pattern. For all benchmark points
considered, the second step is strongly first order along the Higgs direction, satisfying ξh =
vc /Tc ≳ 1. The dominant contribution to strengthening the phase transition arises from the
scalar sector, while the fermionic dark matter affects the finite-temperature potential only
through Yukawa-induced loop corrections. Importantly, the small scalar mixing required
by direct-detection constraints does not weaken the phase transition.
We also investigated the stochastic gravitational-wave signals associated with the
strong first-order electroweak phase transition. Several benchmark points yield spectra
with peak amplitudes within the projected sensitivities of future space-based interferometers such as LISA, DECIGO, u-DECIGO, and BBO. In particular, BP9 produces the
strongest signal, with a peak frequency around f ∼ 10−2 Hz, well aligned with the optimal
sensitivity range of these experiments.
To summarise, the main outcomes of this study are:
• In conventional singlet-scalar extensions where the singlet field acquires a vacuum expectation value, realizing a strong first-order EWPT typically requires a large Higgs–
portal coupling. In the presence of a singlet VEV, this leads to sizable Higgs-singlet
mixing, which is strongly constrained by direct-detection experiments and collider
data. The key novelty of this work lies in disentangling λhs and sin θ by forbidding
a singlet VEV at zero temperature and introducing the dimensionful parameter µhs
to control the mixing independently.
• The absence of a singlet VEV allows the Higgs-portal quartic coupling λhs to be sizable while maintaining a small scalar mixing angle. This structure generates a tree-

– 30 –

## PDF page 32

level barrier in the finite-temperature potential, enabling a strong first-order EWPT,
while simultaneously suppressing direct-detection rates and deviations in Higgs observables. For suitable parameter choices, the model satisfies all current experimental
constraints and predicts GW signals testable by next-generation detectors.
A more comprehensive collider study, including refined projections for future facilities,
would further clarify the connection between the GW–favoured region and scalar-resonance
or di-Higgs signatures. Extensions of the framework with additional degrees of freedom
could further enrich the phase-transition dynamics while preserving the close connection between dark matter, collider phenomenology, and gravitational-wave signatures established
here.

Acknowledgment
The authors thank Prof. Debajyoti Choudhury for useful discussions and Dr. Yikun Wang
for his helpful communication. JD acknowledges SERB, Government of India, for the
National Postdoctoral Fellowship (NPDF) grant with File No. PDF/2023/001540. SN acknowledges funding from Anusandhan National Research Foundation (formerly Science and
Engineering Research Board (SERB)), Govt. of India with grant number SUR/2022/001404
of SURE scheme. TS is supported by the DST, Government of India through the DST
INSPIRE Faculty Fellowship (DST/INSPIRE/04/2024/004616). The work is also supported by the National Natural Science Foundation of China under Grant Nos. 12475094,
12135006, and 12075097.

A

Coefficients of Vct (h, s)

The renormalization conditions for calculating the coefficients of Vct (h, s) given in Eq. (5.9)
are
{
}
)∣
d d d2
d2 d2 ( CW
∣
, ,
, 2, 2
V1−loop (h, s, T ) + Vct (h, s) ∣
= 0.
(A.1)
dh ds dhds dh ds
h=v,s=0,T =0
Using the above conditions, the coefficients can be written as
(
)∣
CW
2 V CW ∣
1
dV
d
∣
δµ2h = −
3
−v
,
∣
∣
2v
dh
dh2
h=v,s=0
) ∣∣
( 2 CW
CW
1
d V
dV
∣
δλh = − 3 v
−
,
∣
2
∣
2v
dh
dh
h=v,s=0
∣
d2 V CW ∣∣
2
δµs = −
,
∣
ds2 ∣
h=v,s=0
∣
1 d2 V CW ∣∣
δµhs = −
,
∣
v dhds ∣
h=v,s=0

– 31 –

(A.2)

(A.3)

(A.4)

(A.5)

## PDF page 33

1
δa1 =
2

( 2 CW
)∣
d V
dV CW ∣∣
v
−2
∣
∣
dhds
ds

.

(A.6)

h=v,s=0

CW (h, s, T = 0).
Here, we have used the shorthand notation V CW ≡ V1−loop

References
[1] K. Kajantie, M. Laine, K. Rummukainen and M.E. Shaposhnikov, Is there a hot
electroweak phase transition at mH ≳ mW ?, Phys. Rev. Lett. 77 (1996) 2887
[hep-ph/9605288].
[2] P. Huet and E. Sather, Electroweak baryogenesis and standard model CP violation, Phys.
Rev. D 51 (1995) 379 [hep-ph/9404302].
[3] F. Csikor, Z. Fodor and J. Heitger, Endpoint of the hot electroweak phase transition, Phys.
Rev. Lett. 82 (1999) 21 [hep-ph/9809291].
[4] A.D. Sakharov, Violation of CP Invariance, C asymmetry, and baryon asymmetry of the
universe, Pisma Zh. Eksp. Teor. Fiz. 5 (1967) 32.
[5] G.W. Anderson and L.J. Hall, The Electroweak phase transition and baryogenesis, Phys.
Rev. D 45 (1992) 2685.
[6] D.E. Morrissey and M.J. Ramsey-Musolf, Electroweak baryogenesis, New J. Phys. 14 (2012)
125003 [1206.2942].
[7] J.M. Cline, K. Kainulainen, P. Scott and C. Weniger, Update on scalar singlet dark matter,
Phys. Rev. D 88 (2013) 055025 [1306.4710].
[8] GAMBIT collaboration, Status of the scalar singlet dark matter model, Eur. Phys. J. C 77
(2017) 568 [1705.07931].
[9] S. Profumo, M.J. Ramsey-Musolf and G. Shaughnessy, Singlet Higgs phenomenology and
the electroweak phase transition, JHEP 08 (2007) 010 [0705.2425].
[10] A. Noble and M. Perelstein, Higgs self-coupling as a probe of electroweak phase transition,
Phys. Rev. D 78 (2008) 063518 [0711.3018].
[11] XENON collaboration, First results on the scalar WIMP-pion coupling, using the
XENON1T experiment, Phys. Rev. Lett. 122 (2019) 071301 [1811.12482].
[12] G. Arcadi, A. Djouadi and M. Raidal, Dark Matter through the Higgs portal, Phys. Rept.
842 (2020) 1 [1903.03616].
[13] N. Craig, H.K. Lou, M. McCullough and A. Thalapillil, The Higgs Portal Above Threshold,
JHEP 02 (2016) 127 [1412.0258].
[14] T. Robens and T. Stefaniak, Status of the Higgs Singlet Extension of the Standard Model
after LHC Run 1, Eur. Phys. J. C 75 (2015) 104 [1501.02234].
[15] S. Profumo, M.J. Ramsey-Musolf, C.L. Wainwright and P. Winslow, Singlet-catalyzed
electroweak phase transitions and precision Higgs boson studies, Phys. Rev. D 91 (2015)
035018 [1407.5342].
[16] A. Beniwal, M. Lewicki, J.D. Wells, M. White and A.G. Williams, Gravitational wave,
collider and dark matter signals from a scalar singlet electroweak baryogenesis, JHEP 08
(2017) 108 [1702.06124].

– 32 –

## PDF page 34

[17] J.M. Cline and P.-A. Lemieux, Electroweak phase transition in two Higgs doublet models,
Phys. Rev. D 55 (1997) 3873 [hep-ph/9609240].
[18] A. Bhatnagar, D. Croon and P. Schicho, Interpreting the 95 GeV resonance in the Two
Higgs Doublet Model: Implications for the Electroweak Phase Transition, 2506.20716.
[19] B. Dı́az Sáez, P. Escalona, S. Norero and A.R. Zerwekh, Fermion singlet dark matter in a
pseudoscalar dark matter portal, JHEP 10 (2021) 233 [2105.04255].
[20] P. Ghorbani, Vacuum stability vs. positivity in real singlet scalar extension of the standard
model, Nucl. Phys. B 971 (2021) 115533 [2104.09542].
[21] J. Ellis, M. Lewicki, M. Merchand, J.M. No and M. Zych, The scalar singlet extension of
the Standard Model: gravitational waves versus baryogenesis, JHEP 01 (2023) 093
[2210.16305].
[22] K. Ghorbani and P.H. Ghorbani, Strongly First-Order Phase Transition in Real Singlet
Scalar Dark Matter Model, J. Phys. G 47 (2020) 015201 [1804.05798].
[23] V. Barger, P. Langacker, M. McCaskey, M.J. Ramsey-Musolf and G. Shaughnessy, LHC
Phenomenology of an Extended Standard Model with a Real Scalar Singlet, Phys. Rev. D 77
(2008) 035005 [0706.4311].
[24] M. Carena, Z. Liu and Y. Wang, Electroweak phase transition with spontaneous Z2 -breaking,
JHEP 08 (2020) 107 [1911.10206].
[25] J.R. Espinosa, T. Konstandin and F. Riva, Strong Electroweak Phase Transitions in the
Standard Model with a Singlet, Nucl. Phys. B 854 (2012) 592 [1107.5441].
[26] J.M. Cline and K. Kainulainen, Electroweak baryogenesis and dark matter from a singlet
Higgs, JCAP 01 (2013) 012 [1210.4196].
[27] T. Alanne, K. Tuominen and V. Vaskonen, Strong phase transition, dark matter and
vacuum stability from simple hidden sectors, Nucl. Phys. B 889 (2014) 692 [1407.0688].
[28] T. Srivastava, J. Das, A. Ghosh and A. Chaudhuri, Electroweak Phase Transition,
Gravitational Waves and Collider Probes in Multi-Scalar Dark Matter Scenarios,
2507.05917.
[29] A. Chaudhuri and J. Das, Study of entropy production due to electroweak phase transition
in Z2 symmetric extension of the Standard Model, Phys. Rev. D 106 (2022) 095016
[2206.08699].
[30] P. Borah, P. Ghosh and A.K. Saha, Prospecting bipartite dark matter through gravitational
waves, JCAP 05 (2025) 035 [2412.17141].
[31] C.-W. Chiang and B.-Q. Lu, First-order electroweak phase transition in a complex singlet
model with Z3 symmetry, JHEP 07 (2020) 082 [1912.12634].
[32] Z. Kang, P. Ko and T. Matsui, Strong first order EWPT & strong gravitational waves in
Z3 -symmetric singlet scalar extension, JHEP 02 (2018) 115 [1706.09721].
[33] K. Kannike, K. Loos and M. Raidal, Gravitational wave signals of pseudo-Goldstone dark
matter in the Z3 complex singlet model, Phys. Rev. D 101 (2020) 035001 [1907.13136].
[34] P. Ghorbani, Gravitational waves from thermal heavy scalar dark matter, Phys. Rev. D 110
(2024) 115002 [2408.16475].
[35] K. Ghorbani and P.H. Ghorbani, A Simultaneous Study of Dark Matter and Phase
Transition: Two-Scalar Scenario, JHEP 12 (2019) 077 [1906.01823].

– 33 –

## PDF page 35

[36] B. Dı́az Sáez, J. Lahiri and K. Möhling, Coscattering in the extended singlet-scalar Higgs
portal, JCAP 10 (2024) 001 [2404.19057].
[37] B. Dı́az Sáez, K. Möhling and D. Stöckinger, Two real scalar WIMP model in the assisted
freeze-out scenario, JCAP 10 (2021) 027 [2103.17064].
[38] K. Murai, K. Sakurai and F. Takahashi, Primordial black hole formation via inverted bubble
collapse, JHEP 07 (2025) 065 [2502.02291].
[39] N. Chakrabarty, H. Roy and T. Srivastava, Single-step first order phase transition and
gravitational waves in a SIMP dark matter scenario, Nucl. Phys. B 998 (2024) 116392
[2212.09659].
[40] T. Ferber, A. Grohsjean and F. Kahlhoefer, Dark Higgs bosons at colliders, Prog. Part.
Nucl. Phys. 136 (2024) 104105 [2305.16169].
[41] X.-m. Zhang, Operators analysis for Higgs potential and cosmological bound on Higgs mass,
Phys. Rev. D 47 (1993) 3065 [hep-ph/9301277].
[42] J.E. Camargo-Molina, R. Enberg and J. Löfgren, A new perspective on the electroweak phase
transition in the Standard Model Effective Field Theory, JHEP 10 (2021) 127 [2103.14022].
[43] K. Hashino and D. Ueda, SMEFT effects on the gravitational wave spectrum from an
electroweak phase transition, Phys. Rev. D 107 (2023) 095022 [2210.11241].
[44] V.K. Oikonomou and A. Giovanakis, Electroweak phase transition in singlet extensions of
the standard model with dimension-six operators, Phys. Rev. D 109 (2024) 055044
[2403.01591].
[45] D. Gazi, A. Mukherjee, S. Niyogi and S. Poddar, Search for Stochastic GW Signal as a
Complementary Approach to Multi-Higgs Productions at the Hadron Colliders to Probe
Dimension Six Operator, 2408.13326.
[46] M. Kamionkowski, A. Kosowsky and M.S. Turner, Gravitational radiation from first order
phase transitions, Phys. Rev. D 49 (1994) 2837 [astro-ph/9310044].
[47] J. Ellis, M. Lewicki and J.M. No, On the Maximal Strength of a First-Order Electroweak
Phase Transition and its Gravitational Wave Signal, JCAP 04 (2019) 003 [1809.08242].
[48] D. Croon, V. Sanz and G. White, Model Discrimination in Gravitational Wave spectra from
Dark Phase Transitions, JHEP 08 (2018) 203 [1806.02332].
[49] A. Beniwal, M. Lewicki, M. White and A.G. Williams, Gravitational waves and electroweak
baryogenesis in a global study of the extended scalar singlet model, JHEP 02 (2019) 183
[1810.02380].
[50] F.P. Huang and X. Zhang, Probing the gauge symmetry breaking of the early universe in
3-3-1 models and beyond by gravitational waves, Phys. Lett. B 788 (2019) 288 [1701.04338].
[51] K. Hashino, M. Kakizaki, S. Kanemura, P. Ko and T. Matsui, Gravitational waves from
first order electroweak phase transition in models with the U(1)X gauge symmetry, JHEP
06 (2018) 088 [1802.02947].
[52] S.V. Demidov, D.S. Gorbunov and D.V. Kirpichnikov, Gravitational waves from phase
transition in split NMSSM, Phys. Lett. B 779 (2018) 191 [1712.00087].
[53] A. Mazumdar and G. White, Review of cosmic phase transitions: their significance and
experimental signatures, Rept. Prog. Phys. 82 (2019) 076901 [1811.01948].

– 34 –

## PDF page 36

[54] A. Kobakhidze, A. Manning and J. Yue, Gravitational waves from the phase transition of a
nonlinearly realized electroweak gauge symmetry, Int. J. Mod. Phys. D 26 (2017) 1750114
[1607.00883].
[55] A. Kobakhidze, C. Lagger, A. Manning and J. Yue, Gravitational waves from a supercooled
electroweak phase transition and their detection with pulsar timing arrays, Eur. Phys. J. C
77 (2017) 570 [1703.06552].
[56] P.S.B. Dev and A. Mazumdar, Probing the Scale of New Physics by Advanced
LIGO/VIRGO, Phys. Rev. D 93 (2016) 104001 [1602.04203].
[57] LIGO Scientific, Virgo collaboration, Observation of Gravitational Waves from a
Binary Black Hole Merger, Phys. Rev. Lett. 116 (2016) 061102 [1602.03837].
[58] eLISA collaboration, The Gravitational Universe, 1305.5720.
[59] S. Kawamura et al., The Japanese space gravitational wave antenna: DECIGO, Class.
Quant. Grav. 28 (2011) 094011.
[60] V. Corbin and N.J. Cornish, Detecting the cosmic gravitational wave background with the
big bang observer, Class. Quant. Grav. 23 (2006) 2435 [gr-qc/0512039].
[61] X. Gong et al., Descope of the ALIA mission, J. Phys. Conf. Ser. 610 (2015) 012011
[1410.7296].
[62] TianQin collaboration, TianQin: a space-borne gravitational wave detector, Class. Quant.
Grav. 33 (2016) 035010 [1512.02076].
[63] D. O’Connell, M.J. Ramsey-Musolf and M.B. Wise, Minimal Extension of the Standard
Model Scalar Sector, Phys. Rev. D 75 (2007) 037701 [hep-ph/0611014].
[64] M. Fairbairn and R. Hogan, Singlet Fermionic Dark Matter and the Electroweak Phase
Transition, JHEP 09 (2013) 022 [1305.3452].
[65] Y.G. Kim, K.Y. Lee and S. Shin, Singlet fermionic dark matter, JHEP 05 (2008) 100
[0803.2932].
[66] J. Kozaczuk, M.J. Ramsey-Musolf and J. Shelton, Exotic Higgs boson decays and the
electroweak phase transition, Phys. Rev. D 101 (2020) 115035 [1911.10210].
[67] C.-Y. Chen, J. Kozaczuk and I.M. Lewis, Non-resonant Collider Signatures of a
Singlet-Driven Electroweak Phase Transition, JHEP 08 (2017) 096 [1704.05844].
[68] C.-Y. Chen, S. Dawson and I.M. Lewis, Exploring resonant di-Higgs boson production in the
Higgs singlet model, Phys. Rev. D 91 (2015) 035015 [1410.5488].
[69] C.-W. Chiang, D. Huang and B.-Q. Lu, Electroweak phase transition confronted with dark
matter detection constraints, JCAP 01 (2021) 035 [2009.08635].
[70] R. Zhou, J. Yang and L. Bian, Gravitational Waves from first-order phase transition and
domain wall, JHEP 04 (2020) 071 [2001.04741].
[71] S.K. Kang and J. Park, Unitarity Constraints in the standard model with a singlet scalar
field, JHEP 04 (2015) 009 [1306.6713].
[72] J. Alwall, M. Herquet, F. Maltoni, O. Mattelaer and T. Stelzer, MadGraph 5 : Going
Beyond, JHEP 06 (2011) 128 [1106.0522].
[73] ATLAS collaboration, Combination of searches for non-resonant and resonant Higgs boson

– 35 –

## PDF page 37

pair production in the bb̄γγ, bb̄τ + τ − and bb̄bb̄ decay channels using pp collisions at
TeV with the ATLAS detector, .

√

s = 13

[74] ATLAS collaboration, Highlights of the HL-LHC physics projections by ATLAS and CMS,
Tech. Rep. ATL-PHYS-PUB-2025-018, CERN, Geneva (2025).
[75] ATLAS collaboration, Search for heavy resonances decaying into a pair of Z bosons in the
ℓ+ ℓ− ℓ′+ ℓ′− and ℓ+ ℓ− ν ν̄ final states using 139 fb−1 of proton–proton collisions at
√
s = 13 TeV with the ATLAS detector, Eur. Phys. J. C 81 (2021) 332 [2009.14791].
[76] ATLAS collaboration, Search for heavy resonances decaying into a Z or W boson and a
Higgs boson in final states with leptons and b-jets in 139 fb−1 of pp collisions at
√
s = 13 TeV with the ATLAS detector, JHEP 06 (2023) 016 [2207.00230].
[77] G. Alguero, G. Belanger, F. Boudjema, S. Chakraborti, A. Goudelis, S. Kraml et al.,
micrOMEGAs 6.0: N-component dark matter, Comput. Phys. Commun. 299 (2024) 109133
[2312.14894].
[78] G. Belanger, F. Boudjema, A. Pukhov and A. Semenov, micrOMEGAs: Version 1.3,
Comput. Phys. Commun. 174 (2006) 577 [hep-ph/0405253].
[79] Planck collaboration, Planck 2018 results. VI. Cosmological parameters, Astron.
Astrophys. 641 (2020) A6 [1807.06209].
[80] ATLAS collaboration, Combination of searches for invisible decays of the Higgs boson
using 139 fb−1 of proton-proton collision data at s=13 TeV collected with the ATLAS
experiment, Phys. Lett. B 842 (2023) 137963 [2301.10731].
[81] LZ collaboration, Dark Matter Search Results from 4.2 Tonne-Years of Exposure of the
LUX-ZEPLIN (LZ) Experiment, Phys. Rev. Lett. 135 (2025) 011802 [2410.17036].
[82] N.D. Christensen and C. Duhr, FeynRules - Feynman rules made easy, Comput. Phys.
Commun. 180 (2009) 1614 [0806.4194].
[83] C. Degrande, Automatic evaluation of UV and R2 terms for beyond the Standard Model
Lagrangians: a proof-of-principle, Comput. Phys. Commun. 197 (2015) 239 [1406.3030].
[84] C. Degrande, C. Duhr, B. Fuks, D. Grellscheid, O. Mattelaer and T. Reiter, UFO - The
Universal FeynRules Output, Comput. Phys. Commun. 183 (2012) 1201 [1108.2040].
[85] P. de Aquino, W. Link, F. Maltoni, O. Mattelaer and T. Stelzer, ALOHA: Automatic
Libraries Of Helicity Amplitudes for Feynman Diagram Computations, Comput. Phys.
Commun. 183 (2012) 2254 [1108.2041].
[86] NNPDF collaboration, Parton distributions with QED corrections, Nucl. Phys. B 877
(2013) 290 [1308.0598].
[87] NNPDF collaboration, Parton distributions for the LHC Run II, JHEP 04 (2015) 040
[1410.8849].
[88] S.R. Coleman and E.J. Weinberg, Radiative Corrections as the Origin of Spontaneous
Symmetry Breaking, Phys. Rev. D 7 (1973) 1888.
[89] M. Quiros, Finite temperature field theory and phase transitions, in ICTP Summer School
in High-Energy Physics and Cosmology, pp. 187–259, 1, 1999 [hep-ph/9901312].
[90] C.L. Wainwright, CosmoTransitions: Computing Cosmological Phase Transition
Temperatures and Bubble Profiles with Multiple Fields, Comput. Phys. Commun. 183
(2012) 2006 [1109.4189].

– 36 –

## PDF page 38

[91] N. Blinov, S. Profumo and T. Stefaniak, The Electroweak Phase Transition in the Inert
Doublet Model, JCAP 07 (2015) 028 [1504.05949].
[92] M. Aoki, T. Komatsu and H. Shibuya, Possibility of a multi-step electroweak phase
transition in the two-Higgs doublet models, PTEP 2022 (2022) 063B05 [2106.03439].
[93] C.-W. Chiang, Y.-T. Li and E. Senaha, Revisiting electroweak phase transition in the
standard model with a real singlet scalar, Phys. Lett. B 789 (2019) 154 [1808.01098].
[94] P. Athron, C. Balazs, A. Fowlie, L. Morris, G. White and Y. Zhang, How arbitrary are
perturbative calculations of the electroweak phase transition?, JHEP 01 (2023) 050
[2208.01319].
[95] D. Croon, O. Gould, P. Schicho, T.V.I. Tenkanen and G. White, Theoretical uncertainties
for cosmological first-order phase transitions, JHEP 04 (2021) 055 [2009.10080].
[96] O. Gould and T.V.I. Tenkanen, On the perturbative expansion at high temperature and
implications for cosmological phase transitions, JHEP 06 (2021) 069 [2104.04399].
[97] A. Andreassen, W. Frost and M.D. Schwartz, Consistent Use of Effective Potentials, Phys.
Rev. D 91 (2015) 016009 [1408.0287].
[98] A. Andreassen, W. Frost and M.D. Schwartz, Consistent Use of the Standard Model
Effective Potential, Phys. Rev. Lett. 113 (2014) 241801 [1408.0292].
[99] O. Gould, Real scalar phase transitions: a nonperturbative analysis, JHEP 04 (2021) 057
[2101.05528].
[100] O. Gould and C. Xie, Higher orders for cosmological phase transitions: a global study in a
Yukawa model, JHEP 12 (2023) 049 [2310.02308].
[101] M. Chala, J.C. Criado, L. Gil and J.L. Miras, Higher-order-operator corrections to
phase-transition parameters in dimensional reduction, JHEP 10 (2024) 025 [2406.02667].
[102] M. Chala, L. Gil and Z. Ren, Phase transitions in dimensional reduction up to three loops,
Chin. Phys. 49 (2025) 123105 [2505.14335].
[103] P. Navarrete, R. Paatelainen, K. Seppänen and T.V.I. Tenkanen, Cosmological phase
transitions without high-temperature expansions, 2507.07014.
[104] T. Biekötter, A. Dashko, M. Löschner and G. Weiglein, Perturbative aspects of the
electroweak phase transition with a complex singlet and implications for gravitational wave
predictions, 2511.14831.
[105] L. Dolan and R. Jackiw, Symmetry Behavior at Finite Temperature, Phys. Rev. D 9 (1974)
3320.
[106] S. Weinberg, Gauge and Global Symmetries at High Temperature, Phys. Rev. D 9 (1974)
3357.
[107] E. Senaha, Symmetry Restoration and Breaking at Finite Temperature: An Introductory
Review, Symmetry 12 (2020) 733.
[108] K. Kainulainen, V. Keus, L. Niemi, K. Rummukainen, T.V.I. Tenkanen and V. Vaskonen,
On the validity of perturbative studies of the electroweak phase transition in the Two Higgs
Doublet model, JHEP 06 (2019) 075 [1904.01329].
[109] P.B. Arnold and O. Espinosa, The Effective potential and first order phase transitions:
Beyond leading-order, Phys. Rev. D 47 (1993) 3546 [hep-ph/9212235].

– 37 –

## PDF page 39

[110] M.E. Carrington, The Effective potential at finite temperature in the Standard Model, Phys.
Rev. D 45 (1992) 2933.
[111] R.R. Parwani, Resummation in a hot scalar field theory, Phys. Rev. D 45 (1992) 4695
[hep-ph/9204216].
[112] V. Vaskonen, Electroweak baryogenesis and gravitational waves from a real scalar singlet,
Phys. Rev. D 95 (2017) 123515 [1611.02073].
[113] A.D. Linde, Decay of the False Vacuum at Finite Temperature, Nucl. Phys. B 216 (1983)
421.
[114] I. Affleck, Quantum Statistical Metastability, Phys. Rev. Lett. 46 (1981) 388.
[115] C. Grojean and G. Servant, Gravitational Waves from Phase Transitions at the Electroweak
Scale and Beyond, Phys. Rev. D 75 (2007) 043507 [hep-ph/0607107].
[116] A.D. Linde, On the Vacuum Instability and the Higgs Meson Mass, Phys. Lett. B 70 (1977)
306.
[117] L. Husdal, On Effective Degrees of Freedom in the Early Universe, Galaxies 4 (2016) 78
[1609.04979].
[118] J. Kehayias and S. Profumo, Semi-Analytic Calculation of the Gravitational Wave Signal
From the Electroweak Phase Transition for General Quartic Scalar Effective Potentials,
JCAP 03 (2010) 003 [0911.0687].
[119] C. Caprini et al., Science with the space-based interferometer eLISA. II: Gravitational
waves from cosmological phase transitions, JCAP 04 (2016) 001 [1512.06239].
[120] DES collaboration, Dark Energy Survey Year 1 Results: A Precise H0 Estimate from DES
Y1, BAO, and D/H Data, Mon. Not. Roy. Astron. Soc. 480 (2018) 3879 [1711.00403].
[121] R. Jinno and M. Takimoto, Gravitational waves from bubble collisions: An analytic
derivation, Phys. Rev. D 95 (2017) 024009 [1605.01403].
[122] J.R. Espinosa, T. Konstandin, J.M. No and G. Servant, Energy Budget of Cosmological
First-order Phase Transitions, JCAP 06 (2010) 028 [1004.4187].
[123] M. Hindmarsh, S.J. Huber, K. Rummukainen and D.J. Weir, Gravitational waves from the
sound of a first order phase transition, Phys. Rev. Lett. 112 (2014) 041301 [1304.2433].
[124] M. Hindmarsh, Sound shell model for acoustic gravitational wave production at a first-order
phase transition in the early Universe, Phys. Rev. Lett. 120 (2018) 071301 [1608.04735].
[125] M. Hindmarsh, S.J. Huber, K. Rummukainen and D.J. Weir, Shape of the acoustic
gravitational wave power spectrum from a first order phase transition, Phys. Rev. D 96
(2017) 103520 [1704.05871].
[126] D. Borah, D. Mahanta and I. Saha, Gravitational wave signatures of dark sector portal
leptogenesis, 2504.14671.
[127] C. Caprini, R. Durrer and G. Servant, The stochastic gravitational wave background from
turbulence and magnetic fields generated by a first-order phase transition, JCAP 12 (2009)
024 [0909.0622].
[128] R. Zhou, L. Bian and Y. Du, Electroweak phase transition and gravitational waves in the
type-II seesaw model, JHEP 08 (2022) 205 [2203.01561].

– 38 –

## PDF page 40

[129] A. Roper Pol, S. Procacci and C. Caprini, Characterization of the gravitational wave
spectrum from sound waves within the sound shell model, Phys. Rev. D 109 (2024) 063531
[2308.12943].
[130] LISA collaboration, Laser Interferometer Space Antenna, 1702.00786.
[131] K. Yagi and N. Seto, Detector configuration of DECIGO/BBO and identification of
cosmological neutron-star binaries, Phys. Rev. D 83 (2011) 044011 [1101.3940].
[132] K. Nakayama and J. Yokoyama, Gravitational Wave Background and Non-Gaussianity as a
Probe of the Curvaton Scenario, JCAP 01 (2010) 010 [0910.0715].
[133] M. Punturo et al., The Einstein Telescope: A third-generation gravitational wave
observatory, Class. Quant. Grav. 27 (2010) 194002.
[134] D. Reitze et al., Cosmic Explorer: The U.S. Contribution to Gravitational-Wave Astronomy
beyond LIGO, Bull. Am. Astron. Soc. 51 (2019) 035 [1907.04833].
[135] LIGO Scientific collaboration, Advanced LIGO, Class. Quant. Grav. 32 (2015) 074001
[1411.4547].
[136] VIRGO collaboration, Advanced Virgo: a second-generation interferometric gravitational
wave detector, Class. Quant. Grav. 32 (2015) 024001 [1408.3978].
[137] KAGRA collaboration, KAGRA: 2.5 Generation Interferometric Gravitational Wave
Detector, Nature Astron. 3 (2019) 35 [1811.08079].

– 39 –
