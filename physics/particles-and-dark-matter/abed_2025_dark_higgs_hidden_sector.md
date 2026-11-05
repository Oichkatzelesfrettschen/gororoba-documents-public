Source: https://arxiv.org/abs/2512.21457v1
PDF sha256: ede423b0afc61996c623894b731cfac97c404768cf7ca6c7837788d51d4850b8
License: http://creativecommons.org/licenses/by/4.0/

# Transcription of abed_2025_dark_higgs_hidden_sector.pdf

Transcription of `abed_2025_dark_higgs_hidden_sector.pdf` in this directory, 25 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 21, 25 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories; pages 1-20, 22-24 from the PDF's own text layer (pdftotext version 26.10.0, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Dark Higgs in Hidden Sector as a Probe for Dark Matter
Faeq Abed ,1, ∗ Asmaa AlMellah ,2, † and Gaber Faisel
1

2, ‡

Particle Physics Lab, Iraqi Nuclear Regulatory Authority, Nidhal, Bghd 28042, Iraq
2

Department of Physics, Faculty of Engineering and Natural Sciences,
Süleyman Demirel University, Isparta, Turkey 32260

arXiv:2512.21457v1 [hep-ex] 25 Dec 2025

Abstract
This study presents a sensitivity analysis of exotic Higgs boson decays at the electron–positron
stage of the Future Circular Collider (FCC-ee), performed within the FCCAnalyses framework. The
analysis investigates Higgs boson production in association with a Z boson in electron–positron
collisions at a center-of-mass energy of 240 GeV. The Higgs boson is assumed to decay into a
pair of long-lived scalar particles, while the Z boson decays leptonically. A hadronic final state
is considered, in which the long-lived scalars subsequently decay into bottom–antibottom quark
pairs.
The simulation chain is implemented using the FCCAnalyses framework, with event generation
performed using MadGraph and Pythia, and detector effects modeled with Delphes. Displaced
vertices arising from the decays of long-lived particles are reconstructed using the FCCAnalyses
implementation of the LCFIPlus secondary vertex finding algorithm, enhanced with extended
features such as customized track selection.
The final event selection requires the reconstruction of a Z boson together with at least two
displaced vertices. This strategy efficiently suppresses Standard Model backgrounds while retaining
at least three expected signal events, including statistical uncertainties, over most of the explored
parameter space. The study considers scalar masses of 20 GeV and 60 GeV and mixing angles of
10−5 , 10−6 , and 10−7 . The results demonstrate that FCC-ee will be sensitive to long-lived scalars
with decay lengths ranging from approximately 1 mm to 10 m, with optimal sensitivity around a
decay length of 0.3 m.

∗

faeq.abed@irsra.gov.iq

†

asmaa.almellah@gmail.com

‡

gaberfaisel@sdu.edu.tr

1

## PDF page 2

I.

INTRODUCTION

A substantial body of research has established that all matter in the Universe is composed
of a limited set of fundamental particles governed by four fundamental interactions: the
electromagnetic, strong, and weak forces, as well as gravity. Three of these forces—excluding
gravity—together with all known elementary particles are described by the Standard Model
(SM) of particle physics. The SM has achieved remarkable success in accurately predicting
a wide range of experimental results. Nevertheless, several key observations, such as the
matter–antimatter asymmetry of the Universe and the existence of dark matter, remain
unexplained within the SM framework, indicating the necessity for new physics beyond the
Standard Model (BSM) [1].
The Large Hadron Collider (LHC) is currently the world’s most powerful particle accelerator, colliding proton or heavy-ion beams at center-of-mass energies in the multi-TeV range,
and is expected to operate until 2026. The collider hosts four main interaction points, where
the ATLAS, CMS, ALICE, and LHCb experiments are located to investigate the properties
of particles produced in high-energy proton–proton collisions [2]. To extend and complement
the physics program of the LHC, a next-generation accelerator, the Future Circular Collider
(FCC), has been proposed. The FCC aims to significantly expand both the energy and
luminosity frontiers in order to enhance sensitivity to new physics phenomena. Its operation
is planned in two stages: an initial electron–positron collider phase (FCC-ee), followed by a
high-energy hadron collider phase (FCC-hh) [3].
One of the most significant achievements of the LHC was the discovery of the Higgs boson
in 2012 by the ATLAS and CMS collaborations [1]. As the only fundamental scalar particle
in the SM, the Higgs boson occupies a unique role, and extensive efforts have since been
devoted to measuring its properties with increasing precision. In parallel, numerous theoretical extensions of the SM have been developed to address its shortcomings and unresolved
questions. Many of these models predict the existence of exotic Higgs boson decays, in
which the Higgs decays into new, previously undiscovered particles [4]. Such particles may
appear as long-lived particles (LLPs), characterized by macroscopic lifetimes that lead to
distinctive experimental signatures, including displaced vertices (DVs) in particle detectors.
The primary objective of this thesis is to investigate exotic Higgs boson decays into LLPs
and to assess the feasibility of studying such scenarios at the FCC-ee. In particular, this
2

## PDF page 3

work focuses on models in which the LLPs are new long-lived scalar particles. This study
represents the first analysis of this type performed within the FCCAnalyses framework,
a newly developed computational tool designed to support simulation and analysis efforts
for the FCC physics program. To achieve this goal, the thesis is structured into three
successive studies. The first step involves defining and characterizing the production and
decay of long-lived scalars at the FCC-ee, which establishes the signal signature targeted in
the analysis.

II.

THE HIGGS BOSON

The Higgs boson is the final fundamental particle predicted by the Standard Model (SM)
and was discovered in 2012 by the ATLAS and CMS experiments at the Large Hadron
Collider (LHC) [5, 6]. It is the only elementary particle with spin zero that has been
observed to date, making it a unique component of the SM. The Higgs boson carries neither
electric charge nor color charge; instead, it interacts with other particles through couplings
proportional to their masses.
This particle is associated with the Higgs field, which plays a central role in the generation
of mass for all quarks, charged leptons, and the weak gauge bosons. Unlike the other fields
in the SM, which have vanishing vacuum expectation values, the Higgs field is characterized
by a non-zero vacuum expectation value that permeates all of space. This property gives
rise to the Higgs mechanism, through which several fundamental particles acquire mass. At
the same time, this mechanism is responsible for the spontaneous breaking of the unified
electroweak interaction into the distinct electromagnetic and weak forces observed at low
energies.

A.

Beyond the Standard Model in Higgs Decays

In order for a new particle to be produced and detected at a collider, it must interact—directly or indirectly—with particles of the Standard Model (SM). The Higgs boson is
particularly well suited for probing such interactions, as its total decay width is extremely
small compared to its mass. Current experimental constraints on the Higgs total width therefore allow significant room for couplings to particles beyond the Standard Model (BSM).
3

## PDF page 4

These interactions can give rise to so-called exotic Higgs decays, in which the Higgs boson
decays into new, light BSM particles [4].
A wide variety of BSM theories predict the existence of exotic Higgs decays, including twoHiggs-doublet models, Little Higgs models, the Next-to-Minimal Supersymmetric Standard
Model, and Hidden Valley scenarios. These frameworks address several unresolved issues
in particle physics and often introduce new degrees of freedom that couple weakly to the
SM [4]. Hidden Valley models, in particular, postulate the existence of an additional sector
composed of light states that interact feebly with SM particles through a heavy mediator [7].
Such models are motivated, for example, by theories of neutral naturalness, which aim to
resolve the hierarchy problem without introducing colored top partners [8]. Because this
new sector couples only weakly to the SM, it is commonly referred to as a hidden or dark
sector. Similar hidden-sector constructions also arise in many models proposed to explain
the nature of dark matter [9].
The mediator connecting the SM and the hidden sector is often referred to as a portal.
In many scenarios, this portal is realized by a new scalar particle that couples to the Higgs
boson. Depending on the model parameters, this scalar can be long-lived, leading to distinctive experimental signatures. A comprehensive overview of exotic Higgs decays, their
theoretical motivations, and associated experimental signatures is provided in Ref. [4], while
a more recent review focusing on searches for long-lived particles (LLPs) can be found in
Ref. [10].
Future collider experiments offer enhanced sensitivity to such scenarios and enable detailed studies of long-lived scalars. Previous studies [11, 12] have examined the sensitivity
of the proposed FCC-ee collider to LLPs originating from exotic Higgs boson decays. As
discussed in Section 5, these analyses indicate a projected peak sensitivity corresponding to
an upper limit of
BR(h → ss) ∼ 5 × 10−5

(95% CL)

for scalar masses in the range 2.5–50 GeV and decay lengths between 0.01 mm and 10 m.
These results can be translated into a lower bound on the coupling strength, k ∼ 10−3 , and
constraints on the scalar–Higgs mixing angle in the range sin θ ∼ 10−7 to 10−4 for a scalar
mass of 50 GeV [12].
The integrated luminosity at each operational stage of the FCC-ee is determined by
the instantaneous luminosity and the duration of data taking. For instance, during the
4

## PDF page 5

Higgsstrahlung (Zh) stage, the expected integrated luminosity is L = 5 ab−1 . The corre√
sponding projected event yields are approximately 5 × 1012 Z bosons at s = 91 GeV, 108
W-boson pairs at 160 GeV, 106 Higgs bosons at 240 GeV, and 106 τ + τ − pairs at 350 GeV.
These exceptionally large data samples will enable measurements of unprecedented precision, significantly surpassing those achievable at current colliders. Any observed deviations
from SM predictions would provide indirect evidence for new physics at energy scales beyond
the direct reach of existing experiments [13].
While the primary physics goals of the FCC-ee include high-precision measurements of
the Higgs boson, electroweak gauge bosons, and the top quark, the clean experimental environment and high statistics of electron–positron collisions also offer powerful opportunities
for the direct discovery of BSM phenomena. In particular, theories predicting new particles
with very small couplings to the SM can be efficiently probed. Such particles may appear
experimentally as LLPs. Notable LLP scenarios with strong discovery potential at the FCCee include Heavy Neutral Leptons (HNLs), Axion-Like Particles (ALPs), and a wide class
of exotic Higgs boson decays to long-lived states

B.

Dark Matter

The scotogenic model extends the Standard Model (SM) by introducing additional
fermionic and scalar fields, namely the fermions N1,2,3 and the scalars S, P , and H ± . All of
these new particles are odd under an imposed Z2 symmetry, which guarantees the stability
of the lightest Z2 -odd particle and allows it to serve as a viable dark matter (DM) candidate.
In this work, we consider the commonly studied scenario in which the lightest fermion,
N1 , constitutes the DM particle, while N2 is assumed to be nearly mass-degenerate with N1 .
This mass configuration is phenomenologically favorable, as it enables consistency with both
the observed DM relic abundance and the experimental bounds on the lepton-flavor-violating
decay µ → eγ.
The DM relic abundance is conventionally expressed in terms of the present-day DM density relative to the critical density, Ω, multiplied by the squared reduced Hubble parameter,
ĥ2 . Its theoretical prediction is given by [14, 15]
Ωĥ2 = √

1.07 × 109 xf GeV−1

 ,
g∗ mPl aeff + 3(beff − aeff /4)/xf
5

## PDF page 6

xf


0.191 aeff + 6beff /xf M1 mPl
,
= ln
√
g∗ xf

(1)

where g∗ denotes the effective number of relativistic degrees of freedom at temperatures
below the freeze-out temperature Tf = M1 /xf , and mPl = 1.22 × 1019 GeV is the Planck
mass.
The coefficients aeff and beff arise from the non-relativistic expansion of the effective co2
, in terms of the relative velocity vrel of the
annihilation cross section, σeff vrel = aeff + beff vrel

annihilating particles in their center-of-mass frame. The effective cross section is defined as
σeff =

1
(σ11 + σ12 + σ21 + σ22 ) ,
4

where the individual cross sections σij (i, j = 1, 2) are given by
σij = σNi Nj →ℓ−i ℓ+j + σNi Nj →νi νj .
These annihilation cross sections have been calculated in Refs. [16, 17] and originate
from tree-level t- and u-channel processes mediated by the charged scalar H ± or the neutral
scalars (S, P ), depending on whether the final states consist of charged leptons or neutrinos.
In order to constrain the model parameter space using the observed DM relic abundance,
our analysis assumes that the DM particle and the scalar states are not mass-degenerate.
This assumption suppresses scalar co-annihilation contributions and isolates the fermionic
annihilation channels relevant for determining the relic density.

C.

Hidden Abelian Higgs Model

One of the simplest extensions of the Standard Model (SM) consists of introducing an
additional Abelian U (1) gauge symmetry associated with a hidden sector. This symmetry
is spontaneously broken by the vacuum expectation value of a dark Higgs field. As a result,
a new massive gauge boson, commonly denoted ZD , emerges and can kinetically mix with
the SM U (1)Y gauge boson. In parallel, the dark Higgs scalar S (or hS ) can mix with the
SM Higgs doublet through the Higgs portal interaction |H|2 |S|2 .
Depending on the dominant mixing mechanism, this framework allows for a variety of
exotic Higgs boson decay channels. If kinetic mixing dominates, decays such as h → ZZD
may occur, while Higgs mixing can lead to decays like h → ZD ZD or h → SS. The scalar
6

## PDF page 7

S inherits its decay modes from the SM Higgs boson, whereas the dark gauge boson ZD
couples proportionally to gauge charge, often resulting in lepton-rich final states. More
intricate cascade decays are also possible, for example
h → SS → ZD ZD ZD ZD ,
which can give rise to striking signatures with up to eight charged leptons in the final state.
The phenomenology of this model has been extensively explored in the literatures. In
addition, the Exotic Higgs Decays Working Group presented a comprehensive survey of
possible exotic Higgs decay modes, including scenarios involving a dark vector and a dark
Higgs field [4].
To facilitate experimental investigations of these channels, a dedicated MadGraph5
model has been constructed to implement this SM extension. The model is developed using
FeynRules 2.0.23 and is based on the Hidden Abelian Higgs Model (HAHM), but includes
several important improvements to ensure internal consistency and numerical accuracy.
These modifications include the correction of typographical errors, a fully self-consistent
determination of all mixing angles from the physical mass eigenvalues MZ , MZD , Mh , and
MhS , and the elimination of the small-mixing approximation.
The mixing angles are defined such that, for small Higgs or kinetic mixing (≪ 1), the
corresponding angles remain small regardless of the relative mass hierarchy between the SM
Higgs or Z boson and the dark scalar hS or dark gauge boson ZD . Furthermore, SM relations
modified by Z–ZD mixing are treated consistently using two alternative schemes: either by
shifting the W -boson mass or by redefining the Weinberg angle.
The model is additionally combined with the Higgs Effective Theory framework, allowing
for the inclusion of effective hgg and hγγ operators. By appropriately choosing the mixing
parameters, the model can also reproduce NMSSM-like decay topologies such as h → SS →
4b by suppressing kinetic mixing, or pure kinetic-mixing phenomenology by setting the Higgs
mixing to zero (while avoiding exactly vanishing values to maintain numerical stability).
In the scotogenic model considered in this study, the production of charged scalars at
an electron–positron collider proceeds via the process e+ (p+ )e− (p− ) → H + H − . The corresponding amplitude receives contributions from tree-level diagrams involving photon (γ),
Z-boson, and fermion N1,2,3 exchange. Neglecting the electron mass, the total cross section
7

## PDF page 8

is given by [17]


gL4 + gL2 gR2 β 3 s
πα2 β 3
α gL2 + gL gR β 3
σe+ e− →H + H − =
+
+
2
3s
12
s − m2Z
96π s − m2Z
! "
#
X |Y1k |4
wk + β
α
gL2

+
wk ln
− 2β +
+
2
64π
s
w
16s
64π
s
−
m
k −β
Z
k


X
 wk + β
2
2
2
− 2β wk
|Y1k | wk − β ln
wk − β
k
!
wj2 − β 2 wj + β
wk2 − β 2 wk + β
ln
+
ln
− 2β ,
+
64π s
wj − w k wj − β wk − w j wk − β
j, k>j
p
where j, k = 1, 2, 3, s = (p+ + p− )2 , α = e2 /(4π), β = 1 − 4m2H /s, and
X |Y1j Y1k |2

wk = 1 +

(2)

2Mk2 2m2H
−
β.
s
s

For the numerical analysis, we use the effective input values α = 1/128, g = 0.6517, and
s2w = 0.23146 [? ].

D.

Constraints

Dedicated searches for exotic Higgs boson decays into long-lived scalar particles, followed
by various Standard Model (SM) decay modes, are currently being pursued at several collider
experiments. To date, no evidence for such scalars has been observed, and upper limits have
been placed on the branching ratio BR(h → ss). Figure 4 summarizes the existing exclusion
limits for mean proper lifetimes ranging from 0.1 mm to 10 m and scalar masses in the
interval ms = 30–40 GeV. The curves shown correspond to different analyses performed by
the ATLAS, CMS, and LHCb collaborations, each probing complementary final states and
long-lived particle (LLP) signatures.
These searches target a wide variety of experimental signatures, including tracks with
large impact parameters and displaced vertices (DVs) reconstructed in the inner tracking
detector (ID), displaced hadronic jets or photons in the calorimeters, as well as displaced jet
or lepton signals in the muon system (MS). A more detailed discussion of LLP signatures
is provided in Section 6. All limits are reported at the 95% confidence level (CL), which is
the standard criterion for exclusion in particle physics analyses [10, 18].
Future collider facilities offer the opportunity to extend the sensitivity to long-lived scalars
well beyond current limits. In particular, a previous study [12] evaluated the projected reach
8

## PDF page 9

of the proposed FCC-ee collider for LLPs originating from exotic Higgs boson decays. As
described in Section 5, the FCC-ee is expected to achieve a peak sensitivity corresponding
to an upper limit of
BR(h → ss) ∼ 5 × 10−5

(95% CL),

for scalar masses in the range 2.5–50 GeV and decay lengths between 0.01 mm and 10 m.
These bounds can be translated into a lower limit on the effective coupling, k ∼ 10−3 , and
constraints on the scalar–Higgs mixing angle of sin θ ∼ 10−7 to 10−4 for a scalar mass of
50 GeV [12].
Throughout this work, we adopt the normal ordering (NO) for neutrino masses. The
leptonic mixing angles, Dirac CP-violating phase, and mass-squared differences |∆m231 | and
∆m221 are fixed using the global neutrino oscillation fit reported in Ref. [19]. This analysis
imposes the constraint
|∆m231 |
< 36.0
∆m221
on the parameter space at the 90% CL. In addition, cosmological observations from the
32.0 < Rm ≡

Planck satellite, baryon acoustic oscillations (BAO), measurements of H(z), and Type Ia
supernovae yield a stringent 2σ upper bound on the sum of neutrino masses,
X
mi < 0.12 eV.
i

Constraints from neutrinoless double beta decay experiments further restrict the effective
Majorana mass to
|⟨m⟩ee | < 0.06–0.2 eV (95% CL),
2
2
2
where ⟨m⟩ee = m1 Ue1
+ m2 Ue2
+ m3 Ue3
[20–22].

The Yukawa interactions involving the charged scalar H ± , as introduced in Eq. (??),
induce lepton-flavor-violating (LFV) processes at the one-loop level. A detailed discussion
of these contributions is provided in Ref. [23]. Current experimental upper limits on LFV
branching ratios are given by BR(µ → eγ) < 4.2 × 10−13 [24], BR(τ → eγ) < 3.3 × 10−8 ,
and BR(τ → µγ) < 4.4 × 10−8 [25], with the most stringent constraint arising from µ → eγ.
The corresponding expressions within the scotogenic framework can be found in Ref. [23].
The flavor-conserving counterparts of these processes contribute to the anomalous magnetic
moments of charged leptons, leading to [26]
 2
−m2ℓi X
Mk
2
∆aℓi =
|Y
|
F
.
ik
2
16π 2 mH k
m2H
9

(3)

## PDF page 10

Among these observables, the muon anomalous magnetic moment provides the strongest
constraint. The current discrepancy between the experimental measurement and the SM
prediction is
SM
−9
aexp
µ − aµ = (2.51 ± 0.59) × 10 ,

as reported in Ref. [27].
Direct detection constraints on dark matter (DM), arising from elastic scattering of N1 off
nucleons via one-loop Higgs exchange, have been analyzed in Ref. [28]. To avoid the stringent
bounds from direct detection experiments such as XENON1T and PandaX-4T [29, 30], we
follow Refs. [28, 31] and set λ3,4 = 0.01. This choice leads to
m0 ≃ mH ± + 21 λ4 v 2 ≃ mH ± + 350 GeV.
While direct detection constraints were not included in earlier analyses [17], they are incorporated in this work together with the latest global neutrino oscillation data [19].
In the following section, we present the numerical results of our analysis. The leptonic
mixing angles θ12 , θ23 , θ13 and the Dirac phase δ are fixed to their best-fit values from
Ref. [19]. A comprehensive scan is then performed over the remaining model parameters,
including the scalar masses mH and m0 , the singlet fermion masses M1,2,3 , and the Yukawa
couplings Y1,2,3 defined in Eq. (??). For light DM masses M1 < 100 GeV, the parameter space
is predominantly excluded by LFV constraints [32] and LHC searches [33, 34]. Additional
bounds on scalar masses arise from measurements of the W and Z boson widths and the
absence of new particle signals at e+ e− colliders, leading to the following constraints [35–37]:
mH ± + mS,P > mW ± ,
mH ± > 70 GeV,
mS + mP > mZ .

III.

(4)

SIMULATION SETTING

Simulations of particle collisions and detector responses play a central role in modern
particle physics, serving both precision measurements and searches for physics beyond the
Standard Model (BSM). Simulated data, grounded in theoretical predictions, provide the
basis for testing hypotheses against experimental observations. In feasibility and sensitivity
10

## PDF page 11

studies, simulations are indispensable for accurately modeling particle kinematics and detector effects, enabling reliable estimates of signal sensitivity and offering guidance for detector
design and optimization.
This analysis is performed within the FCCAnalyses framework [38]. Event generation and detector simulation are carried out using the software packages MadGraph [39],
PYTHIA [40], and DELPHES [41], with event outputs stored in the EDM4HEP format [42]. The subsequent analysis is implemented in Python and primarily relies on the
RDataFrame interface of the ROOT data analysis framework [18]. Within FCCAnalyses, the analysis workflow is organized into three sequential stages: the first processes the
simulated samples and extracts the relevant physics variables; the second defines the event
selection and specifies the quantities to be histogrammed; and the final stage produces the
corresponding distributions. The remainder of this section provides a detailed description
of the simulation tools used in each step.
An e− e+ collision event is inherently complex, involving multiple stages of particle interactions. For simulation purposes, the event generation is therefore decomposed into several
successive components. These include the hard scattering process of the initial electron–
positron collision, followed by parton showering and hadronization to model the formation
of final-state particles, and finally the detector simulation to reproduce the experimental
response. Each of these stages is computed using Monte Carlo (MC) generators, which employ stochastic sampling techniques to obtain numerical solutions for the underlying physical
processes.
At the level of the hard scattering, the cross section and kinematic properties of the
signal process are calculated for the transition from the initial e− e+ state to an N -particle
final state. At this stage, colored particles such as quarks, antiquarks, and gluons are
treated as free, non-interacting objects. In this study, these calculations are performed
using MadGraph, a widely used MC generator capable of simulating both SM and BSM
processes. MadGraph computes matrix elements at leading order, and can also incorporate
next-to-leading-order corrections to improve the theoretical precision [39].
Before and after the hard scattering, the incoming and outgoing charged particles may
emit additional radiation, giving rise to initial- and final-state radiation. These effects are
modeled using parton shower algorithms. Since free colored particles are not observed experimentally, all quarks and gluons produced either in the hard process or during the parton
11

## PDF page 12

shower must undergo hadronization to form color-neutral hadrons. This step is handled
using PYTHIA, which supplements the hard-scattering events generated by MadGraph
with parton showering, hadronization, and other strong-interaction phenomena [40].
The final stage of the simulation chain models the interaction of the produced particles
with the detector material. This analysis employs the DELPHES framework with an IDEA
detector configuration to perform a fast, parametric detector simulation. In such simulations, the detector response is described using parameterized resolutions and efficiencies that
depend on the particle type and detector region. This approach contrasts with full detector
simulations, in which particles are propagated step-by-step through the detector geometry
and material, and physical interactions are modeled in detail using, for example, the Bethe–
Bloch formalism. The DELPHES simulation includes a tracking system in a magnetic field,
electromagnetic and hadronic calorimeters, and a muon system, and provides reconstructed
observables such as leptons, jets, and missing transverse energy [41].

IV.
A.

RESULTS AND DISCUSSION
Production and Decay at FCC-ee

The signal process studied in this thesis is h → ss → bb̄bb̄, corresponding to the decay
of the Higgs boson into a pair of scalar particles, each of which subsequently decays into a
bottom–antibottom quark pair. The choice of a b-quark final state is motivated by the fact
that it represents the dominant decay mode for scalar masses above 10 GeV, as illustrated
in Figure 3.
At the FCC-ee, Higgs bosons are primarily produced in association with a Z boson at a
√
center-of-mass energy of s = 240 GeV. In the simulated events, the Z boson is required
to decay leptonically into either an electron or a muon pair, according to Z → e+ e− or
Z → µ+ µ− . The full signal production process at the FCC-ee can therefore be written as

e+ e− → Zh,

Z → e+ e− or µ+ µ− ,

h → ss → bb̄bb̄.

(5)

This process is illustrated by the Feynman diagram shown in Figure 1. In the diagram,
the incoming electron and positron are represented by the leftmost lines. The production
12

## PDF page 13

of the Z boson and the Higgs boson proceeds via an intermediate Z boson, depicted in the
central part of the diagram. The upper branches correspond to the leptonic decay of the
Z boson into an e+ e− or µ+ µ− pair, while the rightmost branches show the decay of each
scalar particle s into a bb̄ quark pair.

FIG. 1. Feynman diagram of the complete signal process h → ss → bb̄bb̄ produced at the FCC-ee
via e+ e− → Zh, with the Z boson decaying into e+ e− or µ+ µ− .

B.

Simulating the Signal Process

In this analysis, the normal ordering (NO) of neutrino masses is assumed. The leptonic
mixing angles, the Dirac CP-violating phase, and the mass-squared differences |∆m231 | and
∆m221 are constrained by a variety of experimental measurements. For the numerical evaluation, we adopt the results of the global neutrino oscillation data fit presented in Ref. [19].
This fit imposes the condition
32.0 < Rm ≡

|∆m231 |
< 36.0
∆m221

at the 90% confidence level. In addition, cosmological observations from the Planck satellite,
baryon acoustic oscillation (BAO) data, measurements of H(z), and Type Ia supernovae
P
constrain the sum of neutrino masses to
mi < 0.12 eV at the 2σ level. Constraints from
13

## PDF page 14

neutrinoless double beta decay experiments further limit the effective Majorana mass to
2
2
2
|⟨m⟩ee | = 0.06–0.2 eV at 95% CL [20–22], where ⟨m⟩ee = m1 Ue1
+ m2 Ue2
+ m3 Ue3
.

To generate the signal process defined in 5, the HAHM-MG5 Model-v3 [4] is employed
within MadGraph. This model corresponds to the Hidden Abelian Higgs Model (HAHM),
which introduces an additional scalar particle as well as a vector boson commonly referred
to as the dark photon. The model is characterized by four input parameters: the dark
photon mass mZD , the kinetic mixing parameter ϵ, the scalar mass ms , and the scalar–Higgs
coupling constant.
In order to isolate the SM+scalar scenario, the dark photon is effectively decoupled by
assigning it a large mass, mZD = 1000 GeV, and a very small kinetic mixing, ϵ = 10−10 . To
produce long-lived scalar particles, the total decay width of the scalar is explicitly specified
in the MadGraph process card. For scalars decaying into a bb̄ final state, the total decay
width is given by [4]
3
ms m2b
Γs = sin θ
0.9 × 8π vh2
2


3/2
4m2b
.
1− 2
ms

(6)

Here, the branching ratio BR(s → bb̄) is fixed to 0.9, as shown in the left panel of Figure 3,
and the expression for the partial decay width at leading order The numerical values used
are mb = 4.2 GeV for the b-quark mass, vh = 246 GeV for the Higgs vacuum expectation
value, and the number of colors Nc = 3. This procedure allows precise control over the
scalar lifetime.
All signal samples are generated with 10,000 events each. The scalar masses, mixing
angles, and corresponding decay widths used in the analysis are summarized in Table I.
Two representative scalar masses, ms = 20 GeV and ms = 60 GeV, are considered, covering distinct regions of the parameter space where decays into bb̄ pairs are kinematically
allowed. For each mass point, the mixing angles are chosen as sin θ = 10−5 , 10−6 , and
10−7 , corresponding to proper decay lengths ranging approximately from 1 mm to 10 m.
The scalar–Higgs coupling constant is fixed to κ = 0.001 for all signal samples, yielding a
branching ratio of order BR(h → ss) ∼ 10−4 . This value is below current experimental
limits from LHC searches and lies well within the projected sensitivity of the FCC-ee [12].

The complete simulation chain is executed sequentially using MadGraph [39] v3.4.1,
14

## PDF page 15

TABLE I. Scalar masses, mixing angles, and corresponding decay widths used in the analysis.
Mass of Scalar Mixing angle Width of Scalar
ms [GeV]

sin θ

Γs [GeV]

20

1 × 10−5

5.779 × 10−14

20

1 × 10−6

5.779 × 10−16

20

1 × 10−7

5.779 × 10−18

PYTHIA [40] v8.303, and DELPHES [41] v3.4.2. For each signal sample, the process and
parameter definitions listed in Table I are specified in a MadGraph process card, which
serves as input to generate the hard-scattering events. The resulting events are subsequently
passed to PYTHIA for parton showering and hadronization. Finally, detector effects are
simulated using DELPHES with the spring2021 IDEA detector card, which defines the
detector geometry and response for the fast parametric simulation.

C.

Validation of Generated Quantities

The validation of the signal samples is performed by examining selected truth-level quantities, that is, kinematic variables evaluated prior to the inclusion of detector effects. Particular attention is given to the decay lengths and time distributions of the long-lived scalar
particles. These observables provide an essential cross-check of the correct implementation
of the model parameters and the expected lifetime behavior of the scalars.
The results are presented in the form of histograms, where each bin is filled separately for
each scalar particle. The histograms include overflow entries, such that events with values
exceeding the upper bound of the x-axis are accumulated in the final bin. This treatment
accounts for the enhanced population observed in the last bin of some distributions.
Most of the histograms presented in the following sections share a common labeling
√
scheme. In the upper-left corner, the first line indicates the center-of-mass energy, s =
240 GeV, while the second line specifies the integrated luminosity, L = 5 ab−1 . The third
line displays the signal process defined in5, and the final line indicates that no event selection
has been applied.
In the legend, the individual signal samples are identified by their scalar mass ms and
mixing angle sin θ. The x-axis corresponds to the observable under study, whereas the y-axis
15

## PDF page 16

shows the number of events per bin width, displayed on a logarithmic scale. Event yields
are normalized to the corresponding production cross sections, listed in Table 8, and scaled
to the assumed integrated luminosity.
Finally, each plot title indicates that the simulations are performed for the FCC-ee using
the Delphes detector simulation within the FCCAnalyses framework.

1.

Generated Mass and Number of Scalars

As an initial validation step, the number of scalar particles produced per event is examined. Figure 2 displays the distribution of the number of generated scalars for the signal
sample with ms = 20 GeV and sin θ = 10−5 . According to the signal definition given in
Eq. (5), each event contains exactly two scalar particles. This expectation is confirmed by
Figure 2, which shows that all events populate the bin corresponding to two scalars, demonstrating that the event generation has been implemented correctly.

FIG. 2. The number of generated scalars in each event for the signal sample ms = 20 GeV and
sin θ = 1 × 10−5 .

The next quantity validated is the generated mass of the scalar particles. As summarized
in Table 1, the signal samples are produced with two distinct scalar masses, ms = 20 GeV
16

## PDF page 17

and ms = 60 GeV. Figure 3 shows the generated scalar mass distributions for samples
with a common mixing angle of sin θ = 10−6 and scalar masses of ms = 20 GeV (blue) and
ms = 60 GeV (orange). The distributions exhibit sharp peaks at the corresponding input
mass values, with no entries in the remaining bins, confirming that the scalar masses are
generated as expected.

FIG. 3. Generated mass of the scalars for signal samples with sin θ = 1 × 10−6 and masses
ms = 20 GeV and ms = 60 GeV.

It should be noted that both scalar particles produced in each event are included in the distribution shown in Figure 3. Consequently, the histogram is filled twice per event, once for
each scalar. This explains why the maximum bin content for the ms = 20 GeV, sin θ = 10−6
sample (blue) is twice that observed for the corresponding ms = 20 GeV, sin θ = 10−5
sample (red) shown previously.

2.

Generated Decay Lengths

To validate the implementation of long-lived scalar particles in the simulation, the decay
lengths Lxyz of the scalars are examined. This quantity corresponds to the distance traveled
by a scalar particle in the laboratory frame before decaying into a bb̄ pair. The decay length
17

## PDF page 18

is defined as

Ltruth
xyz =

p
∆x2 + ∆y 2 + ∆z 2 ,

(7)

where ∆x, ∆y, and ∆z denote the spatial separations between the production vertex of
the scalar s and the decay vertex of the resulting bb̄ pair in the x, y, and z directions,
respectively.
The decay length distributions for all signal samples are shown in Figure 4. The horizontal
axis spans the interval from 0 to 2000 mm, corresponding to the region from the e+ e−
interaction point to the outer radius of the IDEA drift chamber, Rout = 2 m, as illustrated
in Figure 9. For signal samples with a mixing angle of sin θ = 10−7 , both for ms = 20 GeV
(green) and ms = 60 GeV (light purple), more than 99% of the decays fall into the overflow
region. This indicates that, for these parameter choices, the scalars are sufficiently long-lived
that a large fraction of decays occur outside the tracking volume of the IDEA detector.
For the mixing angle sin θ = 10−6 , the signal sample with the larger scalar mass, ms =
60 GeV (orange), exhibits a shorter decay length compared to the sample with ms = 20 GeV
(blue). This behavior is consistent with the expectations discussed in Section 2.4.2, where
the decay width of a particle depends on both the matrix element and the available phase
space. For identical coupling strengths, a larger scalar mass leads to an increased decay
width and consequently a reduced decay length.
Finally, the dependence of the decay length on the mixing angle is evident when comparing samples with the same scalar mass. Within each mass group, the decay length increases
as the mixing angle decreases, in agreement with the scaling behavior described in Eq. (8.2).

3.

Generated Time Distributions

The lifetime properties of the scalar particles are further examined in their rest frame.
The measured decay length Lxyz is related to the proper lifetime through
Lxyz = c τ γ,
18

(8)

## PDF page 19

FIG. 4. Generated decay lengths, Lgen
xyz , for all signal samples.

where τ denotes the proper lifetime and γ = Es /ms is the Lorentz boost factor of the scalar.
The proper lifetime can therefore be expressed as
τ=

Lxyz
.
cγ

(9)

Figure 5 presents the lifetime distributions of the scalar particles for the samples with
ms = 20 GeV (Fig. 15a) and ms = 60 GeV (Fig. 15b). As expected, smaller mixing angles
correspond to longer lifetimes. In agreement with the decay-length distributions discussed
previously, a fixed mixing angle results in a shorter lifetime for the heavier scalar mass. This
effect is particularly evident for sin θ = 10−6 , where the lifetime distribution for ms = 20 GeV
(blue) extends up to approximately 8 ns, while for ms = 60 GeV (orange) the distribution
falls off around 1 ns.

As an additional validation step, the mean proper lifetime obtained from the simulated
distributions is compared with the theoretically calculated value. The lifetime spectra are
fitted with an exponential function, following Eq. (2.5), to extract the mean proper lifetime
τ0 . The corresponding theoretical prediction is derived from Eq. (2.4), using the scalar decay
width calculated according to Eq. (8.2).
19

## PDF page 20

FIG. 5. Distribution of the lifetimes for all signal samples.

In Figure 16, the lifetime distributions for the signal samples with ms = 20 GeV are
shown separately for each considered mixing angle. The simulated lifetime distributions are
displayed in blue, while the exponential fits are overlaid in red. The extracted values of τ0
from the fits are compared with the theoretical estimates and reported in the legend of each
plot.

In all three cases, the mean lifetime extracted from the simulation is found to be slightly
smaller than the corresponding theoretical prediction, even when statistical uncertainties are
taken into account. This discrepancy may arise from the fact that the analytical expressions
used to compute the proper lifetime are evaluated at leading order, as given in Eq. (3.2), and
that the branching ratio is taken from Figure 3. In contrast, the event generation includes
higher-order effects. Employing more precise calculations for the decay width and branching
ratio is therefore expected to improve the level of agreement.
Nevertheless, the relative difference between the theoretical estimates and the fitted values
20

## PDF page 21

Lifetime of scalar with <math>m_s = 20</math> GeV, <math>\sin \theta = 10^{-5}</math>
<math>10^{3}</math>
lifetimeHS
Entries
20000
<math>10^{1}</math>
Mean
0.01087
0.0108
Std Dev
<math>10^{-1}</math>
<math>N_{\mathsf{Events}}</math>
Calculated <math>\tau = 0.0114 \text{ ns}</math>
<math>10^{-3}</math>
<math>10^{-5}</math>
<math>10^{-7}</math>
generated scalar
<math>e^{-t/\tau}</math> fit with <math>\tau = 0.0108 \pm 0.0001</math> ns
0.15
0.05
0.10
0.20
0.25
0.30
0.00
Time distribution [ns]
FIG. 6. Generated lifetime distribution for the signal sample with <math>\sin \theta = 1 \times 10^{-5}</math> and <math>m_s =</math>
<math display="inline">20~{\rm GeV}.</math>
Lifetime of scalar with <math>m_c = 20</math> GeV, <math>\sin \theta = 10^{-6}</math>
10<sup>3</sup>
lifetimeHS
Entries
20000<br>1.083<br>1.086
<math>10^{2}</math>
Mean
Std Dev
<math>10^{1}</math>
Nevents
Calculated <math>\tau = 1.139 \text{ ns}</math>
10°
<math>10^{-1}</math>
<math>10^{-2}</math>
generated scalar
<math>e^{-t/	au}</math> fit with <math>	au=</math> 1.079 <math>\pm</math> 0.0078 ns
<math>10^{-3}</math>
10
2
8
12
6
0
4
Time distribution [ns]
FIG. 7. Generated lifetime distribution for the signal sample with <math>\sin \theta = 1 \times 10^{-6}</math> and <math>m_s =</math>
<math display="inline">20~{\rm GeV}.</math>
21

## PDF page 22

FIG. 8. Generated lifetime distribution for the signal sample with sin θ = 1 × 10−7 and ms =
20 GeV.

does not exceed 5.2%. Based on this level of agreement, and in conjunction with the previous
validation results, the generated signal samples are considered sufficiently accurate and
reliable for the purposes of this analysis.

V.

CONCLUSION

In this work, we investigated the process e+ e− → H + H − within the framework of the
scotogenic model. The scattering amplitude receives contributions from tree-level diagrams
involving photon and Z-boson exchange, as well as from the exchange of the singlet righthanded fermions N1,2,3 . We examined the experimental and theoretical constraints that
significantly restrict the region of parameter space relevant to the process e+ e− → H + H − .
In addition, the individual contributions of the photon, the Z boson, and the fermions N1,2,3
to the total production cross section were evaluated, taking into account all stringent bounds
imposed on the model parameters.
Our analysis shows that the dominant contribution to the cross section arises from the
exchange of the singlet right-handed fermions N1,2,3 . We further studied the dependence
of the cross section on the center-of-mass energy for a set of benchmark points that satisfy
22

## PDF page 23

the most restrictive constraints. Future high-energy e+ e− colliders will be able to probe the
process e+ e− → H + H − with high precision, thereby providing an opportunity to test these
predictions by either strengthening existing bounds or validating the results presented in
this study.

[1] CERN, The Standard Model (2025), accessed: 2025-11-04.
[2] CERN, The Large Hadron Collider (2025), accessed: 2025-11-04.
[3] CERN, The Future Circular Collider (2025), accessed: 2025-11-04.
[4] D. Curtin, R. Essig, S. Gori, J. Shelton, P. Jaiswal, A. Katz, T. Liu, Z. Liu, and C. E. M.
Wagner, Phys. Rev. D 90, 075004 (2014), arXiv:1312.4992 [hep-ph].
[5] ATLAS Collaboration, Phys. Lett. B 716, 1 (2012), arXiv:1207.7214 [hep-ex].
[6] CMS Collaboration, Phys. Lett. B 716, 30 (2012), arXiv:1207.7235 [hep-ex].
[7] M. J. Strassler and K. M. Zurek, Phys. Lett. B 651, 374 (2007), arXiv:hep-ph/0604261 [hepph].
[8] N. Craig, A. Katz, M. J. Strassler, and R. Sundrum, Naturalness in the Dark at the LHC
(2015), arXiv:1501.05310 [hep-ph].
[9] G. Krnjaic, Phys. Rev. D 94, 073009 (2016), arXiv:1512.04119 [hep-ph].
[10] M. Cepeda, S. Gori, V. Outschoorn, and J. Shelton, Ann. Rev. Nucl. Part. Sci. 72, 395 (2022),
arXiv:2111.12751 [hep-ph].
[11] A. L. Read, J. Phys. G 28, 2693 (2002).
[12] S. Alipour-Fard, N. Craig, et al., Chin. Phys. C 43, 053101 (2019), arXiv:1812.05588 [hep-ph].
[13] A. Abada, M. Abbrescia, et al., Eur. Phys. J. Spec. Top. 228, 261 (2019).
[14] J. Kubo, E. Ma, and D. Suematsu, Phys. Lett. B 642, 18 (2006), arXiv:hep-ph/0604114
[hep-ph].
[15] G. Jungman, M. Kamionkowski, and K. Griest, Phys. Rept. 267, 195 (1996), arXiv:hepph/9506380 [hep-ph].
[16] S. Y. Ho and J. Tandean, Phys. Rev. D 87, 095015 (2013), arXiv:1303.5700 [hep-ph].
[17] S. Y. Ho and J. Tandean, Phys. Rev. D 89, 114025 (2014), arXiv:1311.0449 [hep-ph].
[18] ROOT Team, ROOT Reference Guide (v6.26) (2022), accessed: 2025-11-04.
[19] P. F. de Salas, D. V. Forero, S. Gariazzo, P. Mart

23

## PDF page 24

’inez-Mirav
’e, O. Mena, C. A. Ternes, M. T
’ortola, and J. W. F. Valle, JHEP 02, 071, arXiv:2006.11237 [hep-ph].
[20] G. Anton et al., Phys. Rev. Lett. 123, 161802 (2019), arXiv:1906.02723 [nucl-ex].
[21] A. Gando et al., Phys. Rev. Lett. 117, 082503 (2016), arXiv:1605.02889 [hep-ex].
[22] M. Agostini et al., Phys. Rev. Lett. 125, 252502 (2020), arXiv:2009.06079 [nucl-ex].
[23] T. Toma and A. Vicente, JHEP 01, 160, arXiv:1312.2840 [hep-ph].
[24] A. M. Baldini et al., Eur. Phys. J. C 76, 434 (2016), arXiv:1605.05081 [hep-ex].
[25] B. Aubert et al., Phys. Rev. Lett. 104, 021802 (2010), arXiv:0908.2381 [hep-ex].
[26] E. Ma and M. Raidal, Phys. Rev. Lett. 87, 011802 (2001), erratum: Phys. Rev. Lett. 87,
159901 (2001), arXiv:hep-ph/0102255 [hep-ph].
[27] T. Aoyama et al., Phys. Rept. 887, 1 (2020), arXiv:2006.04822 [hep-ph].
[28] A. Ibarra, C. E. Yaguna, and O. Zapata, Phys. Rev. D 93, 035012 (2016), arXiv:1601.01163
[hep-ph].
[29] E. Aprile et al., Phys. Rev. Lett. 121, 111302 (2018), arXiv:1805.12562 [astro-ph.CO].
[30] Y. Meng et al., Phys. Rev. Lett. 127, 261802 (2021), arXiv:2107.13438 [hep-ex].
[31] J. Liu, Z.-L. Han, Y. Jin, and H. Li, JHEP 12, 057, arXiv:2207.07382 [hep-ph].
[32] A. Vicente and C. E. Yaguna, JHEP 02, 144, arXiv:1412.2545 [hep-ph].
[33] G. Aad et al., Phys. Rev. D 101, 052005 (2020), arXiv:1911.12606 [hep-ex].
[34] A. M. Sirunyan et al., JHEP 04, 123, arXiv:2012.08600 [hep-ex].
[35] A. Arhrib, R. Benbrik, and N. Gaur, Phys. Rev. D 85, 095021 (2012), arXiv:1201.2644 [hepph].
[36] Q.-H. Cao, E. Ma, and G. Rajasekaran, Phys. Rev. D 76, 095011 (2007), arXiv:0705.1186
[hep-ph].
[37] A. Pierce and J. Thaler, JHEP 08, 026, arXiv:hep-ph/0703056 [hep-ph].
[38] FCC Collaboration, FCCAnalyses GitHub repository (2025), accessed: 2025-11-04.
[39] J. Alwall, R. Frederix, S. Frixione, V. Hirschi, F. Maltoni, O. Mattelaer, H.-S. Shao, T. Stelzer,
P. Torrielli, and M. Zaro, JHEP 07, 079, arXiv:1405.0301 [hep-ph].
[40] C. Bierlich, S. Chakraborty, et al., A comprehensive guide to the physics and usage of PYTHIA
8.3 (2022), arXiv:2203.11601 [hep-ph].
[41] S. Ovyn, X. Rouby, and V. Lemaitre, Delphes, a framework for fast simulation of a generic

24

## PDF page 25

collider experiment (2009), <math>arXiv:0903.2225</math> [hep-ph].
[42] Key4HEP Collaboration, EDM4hep format (2025), accessed: 2025-11-04.
25
