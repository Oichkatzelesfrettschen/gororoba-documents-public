Source: https://arxiv.org/abs/2505.01634v2
PDF sha256: fc62f65f15e43ebe19b3301405332c8e88d916d30ab591e64aab8e759e93ecb2
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine (failed: characters)

# Transcription of atlas_2025_semi_visible_jets.pdf

Transcription of `atlas_2025_semi_visible_jets.pdf` in this directory, 45 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 10 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories; pages 1-9, 11-45 from the PDF's own text layer (pdftotext version 26.10.0, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

EUROPEAN ORGANISATION FOR NUCLEAR RESEARCH (CERN)

arXiv:2505.01634v2 [hep-ex] 27 Aug 2025

Phys. Rev. D 112 (2025) 012021
DOI: https://doi.org/10.1103/44zp-mh1q

CERN-EP-2025-101
August 29, 2025

Search for new physics in final states with
semi-visible jets or anomalous signatures using the
ATLAS detector
The ATLAS Collaboration

A search is presented for hadronic signatures of beyond the Standard Model (BSM) physics,
with an emphasis on signatures of a strongly-coupled hidden dark sector accessed via resonant
production of a 𝑍 ′ mediator. The ATLAS experiment dataset collected at the Large Hadron
√
Collider from 2015 to 2018 is used, consisting of proton–proton collisions at 𝑠 = 13 TeV and
corresponding to an integrated luminosity of 140 fb−1 . The 𝑍 ′ mediator is considered to decay
to two dark quarks, which each hadronize and decay to showers containing both dark and
Standard Model particles, producing a topology of interacting and non-interacting particles
within a jet known as “semi-visible". Machine learning methods are used to select these dark
showers and reject the dominant background of mismeasured multĳet events, including an
anomaly detection approach to preserve broad sensitivity to a variety of BSM topologies. A
resonance search is performed by fitting the transverse mass spectrum based on a functional
form background estimation. No significant excess over the expected background is observed.
Results are presented as limits on the production cross section of semi-visible jet signals,
parameterized by the fraction of invisible particles in the decay and the 𝑍 ′ mass, and by
quantifying the significance of any generic Gaussian-shaped mass peak in the anomaly region.

© 2025 CERN for the benefit of the ATLAS Collaboration.
Reproduction of this article or parts of it is allowed as specified in the CC-BY-4.0 license.

## PDF page 2

Contents
1

Introduction

2

2

ATLAS detector

4

3

Data and simulated samples

5

4

Object selection

7

5

Machine learning methodology
5.1 ParticleFlow Network
5.2 Semi-supervised anomaly detection

8
8
9

6

Event selection

12

7

Background estimation

13

8

Systematic uncertainties

14

9

Statistical analysis

16

10 Conclusions

21

1 Introduction
The particle nature of dark matter (DM) is one of the most pressing questions in fundamental particle
physics today. There is overwhelming experimental evidence from astrophysical experiments for its
existence [1–3], yet no particle in the Standard Model (SM) has all of its observed characteristics. The
range of experimentally allowed DM candidate masses is vast, from axion-like fields at masses as low as
10−22 eV up to macroscopic galactic objects which can be hundreds of solar masses, and there is a vast
experimental landscape attempting to cover these disparate targets [4, 5]. Further, DM is just one of several
outstanding mysteries in the SM that point to the existence of new physics, motivating a broad search
program without strong reliance on signal priors.
General purpose detectors at the Large Hadron Collider (LHC) [6] can provide sensitivity to key areas of
beyond the Standard Model (BSM) phase space. Past collider-based DM searches have primarily focused on
weakly interacting massive particles (WIMPs), with masses on the O(100) GeV scale, which can naturally
explain the thermal relic density of DM observed today [7]. This abundance calculation depends upon an
electroweak interaction between the SM and dark sector, making the search for a mediator particle viable
at colliders. A prominent collider signature is missing transverse energy (𝐸 Tmiss ), due to the non-interacting
WIMPs being produced in the proton-proton collision and passing through the detector without interacting.
However, multi-species dark sectors from Hidden Valley theories could yield a more complex picture,
predicting a new set of new particles, forces, and interactions with a small coupling to the SM [8, 9].
The wide variety of potential dark sector manifestations outlined here are representative of the breadth of
phase space that must be considered for a comprehensive search program at colliders. Anomaly detection
(AD) is a strategy that leverages data-driven tools to design search regions that are not designed for a

2

## PDF page 3

specific signal model, but rather isolate events within a dataset based on their deviation from the learned
background distribution [10]. The use of AD-based searches in high energy physics can enable access to
potential discoveries not yet predicted by theories, while their inherently generalized design can also allow
for more efficient traversal of classes of signal models.
The LHC can provide a unique handle on sensitivity to various BSM scenarios, particularly for strongly
interacting dark sectors that produce dark showers and hadronization in LHC detectors, as well as a means
for more generic anomaly-based searches. The theoretical underpinning of focus here is a dark quantum
chromodynamics (QCD) with a gauge group 𝑆𝑈 (𝑁 𝑑 ) leading to confinement at a scale Λ𝑑 [11, 12]. Dark
particles charged under this gauge group would hadronize and generate dark jet signatures. Some fraction
of the dark sector hadrons escape the detector and thus contribute to 𝐸 Tmiss , while others can decay back
to Standard Model quarks, which then shower and hadronize according to SM QCD. Depending on the
couplings in this dark sector, a range of jet topologies could be produced, ranging from fully visible or
invisible to the detector, and with fully prompt or very displaced tracks as the shower develops.
This search focuses on a particular signature within this class of models, looking for prompt semi-visible
jets (SVJs), where a fraction of dark hadrons decay back to SM particles while the others remain invisible,
leading to wide jets with high track multiplicity and significant 𝐸 Tmiss [13]. As the 𝐸 Tmiss arises from the
showering of dark particles in the jet, it will be distributed across the shower, in some cases leading
to jet clustering inefficiency. This class of dark QCD models and their phenomenology have been
discussed extensively [13–15] and signal models with theoretically motivated parameter values have been
benchmarked in the 2021 Snowmass community planning process [16]. The parameter Rinv controls the
branching ratio of the dark hadron to dark particles, which are non-interacting with the detector, such
that higher values of Rinv lead to larger total missing energy in the jet. A Feynman diagram of the signal
process, along with a graphic depicting the SVJ topology generated upon dark quark decay, can be seen in
the diagram in Figure 1.
The complex detector signature of strongly coupled dark sectors motivates the use of machine learning
(ML) techniques to isolate them from background processes [17, 18]. In particular, strongly coupled
dark sector models present excellent candidates for AD tools due to their sensitive dependence on model
parameters [19–24], with a diverse range of final-state topologies being predicted. This inherent variability
emphasizes the benefit of general and model-agnostic selection strategies to complement more signal
model-specific approaches. Furthermore, the non-perturbative nature of strong dynamics introduces
significant challenges in simulation reliability, making data-driven anomaly detection particularly valuable
for uncovering potential new physics in these scenarios.
Strongly coupled dark matter searches have recently been a significant topic of interest in collider physics.
The ATLAS experiment published previous searches on fully visible dark jets [25], a non-resonant
production of semi-visible jets [26], dark mesons decaying to top and bottom quarks [27], and for emerging
jets where the dark particles decay back to SM particles with a proper length on the detector scale [28].
The CMS experiment has published searches for resonant production of semi-visible jets [29], as well as
for emerging jets [30, 31]. As the extreme cases for semi-visible jets involve resonances with fully visible
dĳet or invisible final states, such searches have potential synergy of exclusions. Additionally, there has
been a broad community effort in the study of anomaly detection methods for model-independent search
programs at collider experiments [32, 33]. Both CMS [34] and ATLAS [35–38] have performed several
anomaly detection searches covering a variety of presentations of BSM physics.
This search focuses on the resonant s-channel production of a 𝑍 ′ mediator particle decaying to two dark
quarks which subsequently hadronize, leading to a final state of at least two jets. While both jets contain

3

## PDF page 4

invisible particle
visible particle

Rinv
Figure 1: Feynman diagram of the signal process, with leading order s-channel production of the 𝑍 ′ mediator which
subsequently decays to two dark quarks 𝜒. The dark quarks subsequently generate the semi-visible jet topology upon
decay, displaying varying patterns of visible (solid blue) and invisible (dashed pink) constituent energy, coming from
SM and dark particles respectively. The relative amount of invisible energy is govern by Rinv , defined as the particle
branching ratio to dark hadrons.

dark particles and thus missing energy, only the event-level 𝐸 Tmiss can be calculated, and any 𝐸 Tmiss that
persists due to imbalance or boosting of the dark jets will be primarily well-aligned with one of them.
The SM background varies with the amount of invisible energy in the SVJs, but is dominated by SM
multĳet processes. Discriminating signal from multĳet processes is challenging, as the signature of
𝐸 Tmiss well-aligned with a jet is a feature of jet mismeasurement. To address these challenges, ML is used to
define the signal regions based on high-dimensional and low-level detector information. In particular, two
ML-based signal regions are developed: one based on model-specific classification of SVJ signals from
background, and a second leveraging AD to broaden sensitivity to a variety of hadronic signatures with
𝐸 Tmiss . The final statistical treatment uses a fit to the transverse mass 𝑚 T , calculated using the two leading
jets and the 𝐸 Tmiss , in order to reconstruct the 𝑍 ′ mass. This analysis is unique with respect to previous
ATLAS anomaly searches in that it considers new physics signatures that are resonant in 𝑚 T , and is the
first use of semi-supervised machine learning (with partially labeled training inputs).

2 ATLAS detector
The ATLAS detector [39] at the LHC covers nearly the entire solid angle around the collision point.1 It
consists of an inner tracking detector surrounded by a thin superconducting solenoid, electromagnetic
and hadronic calorimeters, and a muon spectrometer incorporating three large superconducting air-core
toroidal magnets.
The inner-detector system (ID) is immersed in a 2 T axial magnetic field and provides charged-particle
tracking in the range |𝜂| < 2.5. The high-granularity silicon pixel detector covers the vertex region and
1 ATLAS uses a right-handed coordinate system with its origin at the nominal interaction point (IP) in the centre of the detector

and the 𝑧-axis along the beam pipe. The 𝑥-axis points from the IP to the centre of the LHC ring, and the 𝑦-axis points upwards.
Polar coordinates (𝑟, 𝜙) are used in the transverse plane, 𝜙 being the azimuthal angle around the
 𝑧-axis.
 The pseudorapidity is
𝐸+ 𝑝
defined in terms of the polar angle 𝜃 as 𝜂 = − ln tan(𝜃/2) and is equal to the rapidity 𝑦 = 12 ln 𝐸 − 𝑝𝑧𝑧 in the relativistic limit.
√︁
Angular distance is measured in units of Δ𝑅 ≡ (Δ𝑦) 2 + (Δ𝜙) 2 .

4

## PDF page 5

typically provides four measurements per track, the first hit generally being in the insertable B-layer (IBL)
installed before Run 2 [40, 41]. It is followed by the SemiConductor Tracker (SCT), which usually provides
eight measurements per track. These silicon detectors are complemented by the transition radiation tracker
(TRT), which enables radially extended track reconstruction up to |𝜂| = 2.0. The TRT also provides
electron identification information based on the fraction of hits (typically 30 in total) above a higher
energy-deposit threshold corresponding to transition radiation.
The calorimeter system covers the pseudorapidity range |𝜂| < 4.9. Within the region |𝜂| < 3.2,
electromagnetic calorimetry is provided by barrel and endcap high-granularity lead/liquid-argon (LAr)
calorimeters, with an additional thin LAr presampler covering |𝜂| < 1.8 to correct for energy loss in material
upstream of the calorimeters. Hadronic calorimetry is provided by the steel/scintillator-tile calorimeter,
segmented into three barrel structures within |𝜂| < 1.7, and two copper/LAr hadronic endcap calorimeters.
The solid angle coverage is completed with forward copper/LAr and tungsten/LAr calorimeter modules
optimised for electromagnetic and hadronic energy measurements respectively.
The muon spectrometer (MS) comprises separate trigger and high-precision tracking chambers measuring
the deflection of muons in a magnetic field generated by the superconducting air-core toroidal magnets.
The field integral of the toroids ranges between 2.0 and 6.0 T m across most of the detector. Three layers
of precision chambers, each consisting of layers of monitored drift tubes, cover the region |𝜂| < 2.7,
complemented by cathode-strip chambers in the forward region, where the background is highest. The
muon trigger system covers the range |𝜂| < 2.4 with resistive-plate chambers in the barrel, and thin-gap
chambers in the endcap regions.
The luminosity is measured mainly by the LUCID–2 [42] detector that records Cherenkov light produced
in the quartz windows of photomultipliers located close to the beampipe.
Events are selected by the first-level trigger system implemented in custom hardware, followed by selections
made by algorithms implemented in software in the high-level trigger [43]. The first-level trigger accepts
events from the 40 MHz bunch crossings at a rate below 100 kHz, which the high-level trigger further
reduces in order to record complete events to disk at about 1 kHz.
A software suite [44] is used in data simulation, in the reconstruction and analysis of real and simulated
data, in detector operations, and in the trigger and data acquisition systems of the experiment.

3 Data and simulated samples
This search is performed with 140 fb−1 of LHC 𝑝 𝑝 collision data collected by the ATLAS detector from
2015 to 2018. The integrated luminosity of the runs is estimated following the methodology described in
Ref. [45]. It is required that all the relevant elements of the ATLAS detector were fully operational and
efficient while the data were collected [46].
Events are further selected to pass a single-jet trigger selection, where events are required to have a jet at
trigger-level with a transverse momentum 𝑝 T exceeding a value that ranges from 360 to 420 GeV depending
on the data-taking year. The lowest 𝑝 T unprescaled single-jet trigger is used across data-taking periods.
Selections on jet 𝑝 T (described in Section 6) ensure these triggers are only used after reaching an efficiency
plateau, avoiding the effect of the trigger turn-on in the analysis. The data are subject to a blinding
strategy throughout the analysis design so as to mitigate analyzer-induced bias, namely that the data of

5

## PDF page 6

Table 1: Fixed parameters in the semi-visible jet signal model.

Parameter
Value

N 𝑐𝐷
3

𝑁 𝑓𝐷
2

Λ𝐷 [GeV]
10

𝑚 𝜋𝐷 [GeV]
17

𝑚 𝜌𝐷 [GeV]
31.77

𝑚 𝜒 [GeV]
10

𝑔q
1

𝑔𝜒
0.1

the signal-enriched region are not examined by the analyzers until a full validation of the background
estimation has been performed in signal-depleted regions.
Simulated events are generated with a variety of Monte Carlo (MC) generators. The 𝑝 𝑝 hard scatter physics
process is simulated first, and the final-state particles are subsequently showered and decayed. This full
description of the event is then propagated through a detailed detector simulation based on GEANT4 [47,
48], and simulated events are reconstructed with the same algorithms run on collision data. The generation
of the simulated event samples includes the effect of pile-up, defined as the mean number of interactions
per bunch crossing. The effect of pile-up is assessed with the inclusion of overlaid simulated inelastic 𝑝 𝑝
interactions, as well as the effect on the detector response due to interactions from bunch crossings before
or after the one containing the hard interaction. Events in the simulation are weighted by data-taking period
in order to reproduce the observed pile-up distribution.
Signal simulation is generated using Madgraph5 [49] followed by the Hidden Valley module of
Pythia8.244 [50]. The s-channel production of 𝑍 ′ is governed by a number of parameters. The
mass of the mediator m 𝑍 ′ can be set, together with the couplings of the 𝑍 ′ to the visible and dark quarks
𝑔𝑞 and 𝑔 𝜒 , respectively. The dark sector shower is governed by the number of dark colors 𝑁 𝑐𝐷 , the number
of dark flavors 𝑁 𝑓 𝐷 , and the dark sector confinement scale Λ𝐷 . There is also the characteristic scale of
the dark hadrons 𝑚 𝐷 that determines the mass of the dark hadrons, which can be pseudoscalars 𝜋 𝐷 or
vectors 𝜌 𝐷 , and the mass of the dark quark 𝑚 𝜒 . Finally, each dark hadron coming from the dark quark
decay or subsequent dark shower has a certain branching ratio to dark (invisible) particles, which is set by
𝑁had
Rinv = ( 𝑁had +𝑁𝐼had ) , where 𝑁had𝐼 refers to the number of invisible hadrons and 𝑁had𝑉 refers to the number
𝑉
𝐼
of visible hadrons. Signals with higher values of Rinv thus have larger missing energy in each dark quark
originated jet, as well as the event overall. Up to two additional partons are considered in the underlying
process. The MLM scheme [51] for merging tree-level matrix elements and partons showers is used with a
𝑘 𝑇 merging scale of 30 GeV, a cone radius of 0.4, and max jet |𝜂| of 2.5. The NNPDF2.3LO set of parton
distribution functions (PDF) [52] is used along with the ATLAS A14 [53] set of tuned parameters (tune).
The values of fixed model parameters are summarized in Table 1. Choices of these values are informed
by theoretical considerations and described in detail in Refs. [16, 54], among others. The mediator mass
m 𝑍 ′ and the per-dark hadron invisibility probability Rinv vary, and are used to define the search grid. The
value of m 𝑍 ′ varies between 2000 and 5000 GeV, while Rinv ranges from 0.2 to 0.6.
The anomaly detection region of the analysis is evaluated and studied with the use of alternate signal models,
which do not have SVJ topologies, but share some similar features such as high 𝐸 Tmiss and resonance in 𝑚 T .
One such model is the pair production of new heavy scalars 𝑋, which each decay to a quark and a dark
quark, the latter showering into an emerging jet, where the dark hadrons in the jet have a non-negligible
lifetime leading to the presence of displaced tracks within the shower. The emerging jet signal model
consists of five key signal parameters with the following values set: confinement scale Λ𝐷 = 1.6 GeV,
dark pion mass 𝑚 𝜋𝐷 = Λ𝐷 / 2, dark 𝜌 mass 𝑚 𝜌𝐷 = 2Λ𝐷 , dark scalar mass 𝑚 𝑋 = 1000 GeV, and decay
length of the dark pion 𝑐𝜏𝜋𝐷 = 1 mm. It is generated with the Hidden Valley module in Pythia8.230
with the NNPDF2.3LO PDF set and the ATLAS A14 tune, and filtered to have at least four jets with
𝑝 T > 100 GeV and |𝜂| < 2.7 before detector-level reconstruction. Additionally, the analysis considers a

6

## PDF page 7

split-supersymmetric model [55] with pair production of long-lived gluinos, each decaying to an R-hadron
and a lightest supersymmetric particle (LSP) which escapes the detector as 𝐸 Tmiss . Two points are evaluated
from this model, one with a gluino mass of 2000 GeV and another with a gluino mass of 3000 GeV; both
points share an LSP mass of 100 GeV and a gluino lifetime of 0.03 ns. The gluino signals are generated with
MadGraph 2.6.2 [49], interfaced to Pythia8.24 to simulate decays, parton showering, and the underlying
event, using the NNPDF2.3LO PDF set and the A14 tune.
While the background estimation for the analysis is fully data-driven, simulations of multĳet SM backgrounds
are used to train the ML tools, study modeling of key observables, and develop the statistical treatment.
Multĳet processes are generated using MadGraph5 2.9.9 interfaced to Pythia8.235 for shower and
hadronization with the NNPDF2.3LO PDF set and the A14 tune. The samples are generated in bins of
transverse momentum, to ensure good statistics across the momentum spectrum.

4 Object selection
Jets are reconstructed from constituent particles via the anti-𝑘 𝑡 algorithm [56] with a radius parameter of
0.4 using the FastJet package [57]. The constituents are particle-flow objects, which are built using a
combination of charged particle tracks and calorimeter clusters [58, 59]. Tracks must be matched to the
nominal primary vertex 2 with the requirement |𝑧0 sin𝜃| < 2.0 mm. The particle-flow construction uses ID
track observables to reconstruct the charged particles’ four-momentum for 𝑝 T <100 GeV and calorimeter
observables at higher 𝑝 T where the momentum resolution of the tracker deteriorates.
Baseline jets are required to have a minimum 𝑝 T of 20 GeV and |𝜂| < 4.5. The absolute jet energy scale
(JES) calibration is used to correct the jet four-momentum to the particle-level energy scale, as derived
using simulated jets in dĳet MC events. Finally, the jet resolution is corrected by applying a Gaussian
smearing to simulated jets to match the resolution observed in data [60].
The machine learning methods described in Section 5 train over jets using an input modeling of their
ghost-associated tracks. In the ghost-association process, tracks are treated as infinitesimally soft particles
by setting their 𝑝 T to 1 eV [61]. Starting from the jet built with the particle-flow algorithm, these
infinitesimally soft tracks are clustered in and can then be ghost-associated to a particular jet. Ghost
association is generally superior to geometric matching in dense subjet environments. For the ML tools,
the tracks are required to have 𝑝 T > 1 GeV and |𝜂| < 2.1. To ensure good modeling, jets are required to
have at least 3 ghost-associated tracks.
While leptons are not used for signal selection, lepton requirements are established for the purposes
of vetoing events that contain leptons and for removal of overlapping objects. Electron candidates are
built from the matching of a reconstructed track in the ID with an energy deposit in the electromagnetic
calorimeter that has 𝐸𝑇 > 7 GeV. Baseline electrons are required to have a minimum 𝑝 T of 20 GeV and
|𝜂| < 2.47. Requirements on the transverse and longitudinal impact parameters, defined with respect
to the primary vertex, are applied, specifically |𝑑0 |/𝜎(𝑑0 ) < 5 (where 𝜎(𝑑0 ) is the per-track estimated
uncertainty on 𝑑0 ) and |𝑧 0 𝑠𝑖𝑛(𝜃)| < 0.5 mm. Electrons are also required to pass the Tight identification
and Tight_VarRad isolation criteria [62].
Muons are reconstructed from combined tracks that incorporate information from both the ID and the muon
spectrometer. The combination involves the fitting of ID hits, calorimeter energy loss, and muon spectrometer
2 The primary vertex is defined as the one with the largest Σ 𝑝

T

7

2 of its associated tracks.

## PDF page 8

tracks. Baseline muons must have 𝑝 T > 20 GeV and |𝜂| < 2.5, as well as |𝑑0 |/𝜎(𝑑0 ) < 3 and |𝑧 0 𝑠𝑖𝑛(𝜃)| <
0.5 mm. Muons are further required to pass the Medium identification and PflowTight_VarRad isolation
criteria [63].
The 𝐸 Tmiss is computed from the jets, muons, and electrons which pass the baseline requirements. It
comprises a term based on hard objects, specifically the negative vectorial sum of the transverse momenta
of all baseline reconstructed objects, added to a soft term constructed from tracks associated with the
primary vertex that are not matched to any hard object [64]. After the initial selection, an overlap removal
(OR) is applied to deal with the case of a single object being reconstructed as multiple different objects by
the detector. The OR is applied on selected objects before isolation requirements are imposed. The key
overlaps between leptons and jets are resolved in two steps: first, jets within Δ𝑅 < 0.2 of electrons are
rejected. Following this, if a reconstructed lepton (electron or muon) is found to be within Δ𝑅 < 0.4 of a
jet, the lepton is rejected in favor of the jet.

5 Machine learning methodology
The signal models pursued in this search are particularly well-suited to ML-based selection tools to enrich
the signal-to-background ratio in analysis regions. Two different ML approaches are used in this search,
both providing a per-event score that is subsequently used in the event selection to define the relevant
analysis regions (see Section 6 for details).

5.1 ParticleFlow Network
The first ML-based region uses a method built to maximize sensitivity to the generated SVJ signal models.
The specific choice of ML model is motivated by two primary considerations: permutation invariant
input modeling given that collider events are inherently unordered sets of particles, and a low-level input
modeling (over tracks) to take advantage of the available high-dimensional information to best exploit
correlations within the event.
These requirements are satisfied with a Particle Flow Network (PFN) [65], which is used to model input
events as a DeepSet [66], in this case an unordered set of tracks. Given the unordered and variable-length
nature of particles in an event, this choice of modeling as a set can enable the ML tool to better learn the
most important features of the dataset that enable a signal-to-background classification. For the specific
case of SVJs, track-level modeling further allows the ML model to use the distinctive pattern of particles and
𝐸 Tmiss within the jet shower, which is a key topological feature to discriminate from multĳet background.
Constructing the PFN first involves the learning of a new unordered representation Φ for each particle.
Permutation invariance is then enforced by summing over the per-particle Φ representation to create a
new permutation invariant, symmetric, and fixed length latent space basis O. A masking layer is used
to suppress any zero-padded inputs, making the architecture length agnostic as well. Finally, a classifier
is trained over this latent space basis to distinguish signal from background, where truth event labels are
used to facilitate training. The trained PFN can then be used to provide an output score for each event
that indicates its probability of being from signal or background processes, enabling the definition of a
signal-enriched region.

8

## PDF page 9

The PFN is trained to separate SVJs from background considering events using a track-level input modeling.
An event-level picture is built by modeling events by the 80 highest-𝑝 T tracks each of the leading and
subleading jet, where the value of 80 is chosen to capture the most significant information of the jet
while reducing the input multiplicity with respect to the full track content. Each track is described using
six variables: its four-vector (𝑝 T , 𝜂, 𝜙, E) assuming the track has the pion mass, and the track impact
parameters 𝑑0 and 𝑧 0 . These tracks (up to 160 total) are given to the PFN as a single object. The tracks are
re-centered in 𝜂 and 𝜙 such that the average direction of the two leading jets is mapped to (𝜂, 𝜙) = (0, 0),
aligning the coordinate system with the center of the jet pair. Each track is scaled to its relative fraction of
the total system energy and transverse momentum, enforcing agnosticism to the total energy and transverse
momentum of the event. Finally, each of the six track variables is scaled per-event so that its range is
[0,1].
The PFN model used in this analysis consists of two dense layers with 75 nodes each with rectified linear
unit (ReLU) activation [67], a Φ latent space dimension of 64, followed by three more dense layers of
dimension 75 with ReLU activation, and a final softmax layer [68] to determine the event-level classification
with categorical cross-entropy loss. The Adam optimizer is used with an initial learning rate of 10−3 [69].
The model is developed using 500,000 events at preselection (defined in Section 6) of both signal and
background divided into a split of train/test/validation corresponding to 78%:20%:2%. The signal sample
consists of an unweighted combination of all SVJ simulated signal points, and the background consists
of simulated multĳet processes, both described in Section 3. Optimization studies were performed to
determine the optimal values for best classification performance considering the number of training epochs,
batch size, learning rate, number of neurons, and dimensions of the Φ space; this model represents the
optimal choice across these parameters.
After training, the performance of the PFN is evaluated on the test set. Figure 2 shows distributions of the
PFN score in data, background multĳet simulation, and signal. The PFN is able to achieve an average
area-under-curve of the receiver operating characteristic (ROC) of 0.93 for the combined signal including
all simulated points. This performance was benchmarked against alternate approaches, namely the use
of high-level jet variables with a boosted decision tree, which does not perform as well as the PFN and
introduces a stronger correlation to energy scale. As the PFN score shape is not directly used in the analysis,
qualitative shape differences between multĳet background and data do not impact the analysis. The crucial
metric for agreement between data and simulation is the selection efficiency; here a difference of < 5% is
assessed for the signal region selection of at least 0.6 on the PFN score as defined in Section 6. A diagram
of the PFN can be seen in the upper half of Figure 3.

5.2 Semi-supervised anomaly detection
To broaden the coverage of the analysis, an anomaly detection tool is developed as a companion to the
model-focused PFN tool described above. Anomaly detection involves the application of algorithms
that identify abnormalities within a dataset based on their incompatibility with learned Standard Model
properties, offering a data-driven way to pursue the unknown unknowns in the BSM landscape and thus
expand discovery reach at high energy physics experiments.
A typical component of an AD analysis is the use of data-driven classification tools, which mitigates
reliance on simulation. However, this requires an approach to training the ML model that does not require
full and true labeling of training inputs. The training metholodogy here is a hybrid approach between full
labeling (supervised) and no labeling (unsupervised) known as semi-supervised, where only some training

9

## PDF page 10

.<br>∪.
<b>ATLAS</b>
Data
Multijet QCD
<math>\sqrt{s}</math> = 13 TeV, 140 fb<sup>-1</sup>
<math>m_{Z'} = 2500 \text{ GeV}, R_{inv} = 0.2</math>
<math>m_{Z'} = 4000 \text{ GeV}, R_{inv} = 0.2</math>
10<sup>-1</sup>
<math>m_{Z'} = 2500 \text{ GeV}, R_{inv} = 0.6</math>
<math>m_{Z'} = 4000 \text{ GeV}, R_{inv} = 0.6</math>
10<sup>-2</sup>
10<sup>-3</sup> }
0.2
0.4
0.6
8.0
0.0
1.0
PFN score
Figure 2: Distributions of the PFN score in data, multijet simulation, and representative SVJ signals, after application
of the analysis preselection (defined in Section 6). All histograms are normalized to unity. The PFN provides good
discrimination between signal and background.
Learned per-particle set representation <math>\Phi</math>
Supervised classifier F
Step 1
<math display="block">\mathcal{O}_a = \Sigma_i \Phi_a(p_{Ti}, \eta_i, \phi_i, E_i, d_{0_i}, z_{0_i})</math>
<b>PFN</b>
x 160
Step 2
Variational Auto-encoder
Figure 3: An annotated diagram of the ANTELOPE architecture [70]. Step 1 refers to the fully supervised training of
the PFN network to classify semi-visible jet signals from SM multijet background. In Step 2, data events are encoded
in the permutation-invariant basis O obtained from the PFN training, and used for unsupervised training of a VAE,
where Z nodes specify the latent space.
events have correct labels. This approach informs the AD tool with partial knowledge of the signal model,
honing it to the specific task of detecting dark jets within the broad task of classifying anomalous events.
Additionally, the key event characteristics discussed above, namely the relevance of modeling events as
unordered and variable-length sets of tracks, motivate a similar input modeling for the AD tool.
10

## PDF page 11

A. U.

10

2

10

1

10

0

10

1

10

2

10

3

10

4

10

5

10

6

ATLAS

Emerging jets
mX = 1000 GeV, d = 1 ns
Gluino R-hadron
mg = 2000 GeV, g = 0.03 ns
Gluino R-hadron
mg = 3000 GeV, g = 0.03 ns

s = 13 TeV, 140 fb 1
Data
mZ = 2500 GeV, Rinv = 0.2
mZ = 4000 GeV, Rinv = 0.6
0
0

0.65

0.70

0.75

0.80

0.85

0.90

0.95

1.00

ANTELOPE score

Figure 4: Distribution of the ANTELOPE score in data, SVJ signals, and alternate signal models at preselection,
where higher values of the ANTELOPE score indicate higher likelihood of anomaly. All histograms are normalized
to unity. Though the ANTELOPE training never sees emerging jet or gluino R-hadron signals in its training, it is still
able to distinguish them as more anomalous than the data.

With these considerations in mind, a new tool is developed for this analysis, referred to as ANomaly
deTEction on particle fLOw latent sPacE (ANTELOPE) [70], to perform particle-level and permutationinvariant AD on collider events. In this way, the ANTELOPE model is trained in two stages. The first is the
fully supervised PFN that was already trained to classify the combined SVJ signal from simulated multĳet
background. The pre-trained PFN is subsequently used to encode data events into the basis O, and in this
format they are given as input to the training of a variational autoencoder (VAE) [71]. A VAE is a common
tool that can perform AD via fully unsupervised training by learning to reconstruct data events after forcing
them through a lossy compression that motivates the model to extract the most salient features of the
inputs, thus learning the underlying data distribution. The ANTELOPE technique leverages permutation
invariance and a signal model to learn a new representation for the events. Embedding each data event into
this representation for VAE training thus leads to a more performant AD method, as compared to a VAE
using an input modeling based on fixed-length track features.
Figure 3 provides a diagram of the ANTELOPE architecture. The specific ANTELOPE model used here
takes the same inputs as the PFN described in the previous section, namely the 80 highest 𝑝 T tracks
from each of the leading jets, each described by six variables. The VAE model used for the ANTELOPE
architecture is trained (tested) with 80% (20%) of a subset of 200,000 data events subject to preselection
requirements (detailed in Section 6). The loss L is that of the standard VAE, namely the sum of two
terms: the mean-squared error (MSE) of the output and the input to test reconstruction quality, and the
Kullback-Leibler divergence (KLD) measuring the distance between the learned and tested distributions in
the latent space. The VAE is trained for 50 epochs with a learning rate of 10−5 on data events only. The
final ANTELOPE score is produced by applying a log followed by sigmoid transformation function to the
total evaluated L. Figure 4 shows the distribution of the ANTELOPE score in data and signal simulation
with all preselection requirements imposed.
The performance of the ANTELOPE tool is evaluated through its sensitivity breadth to a wide variety
of signal models rather than its depth to the SVJ signal in particular. To quantify this, several additional
simulated signals are considered as test sets, and a selection of > 0.7 is imposed on the ANTELOPE score

11

## PDF page 12

to maximally enrich the signal sensitivity for the SVJ simulated samples (defined in Section 6). This
threshold for the ANTELOPE SR, determined with no awareness of the alternate signal models, is found
to enrich the signal sensitivity with respect to the PFN SR cut by over three times for the emerging jet
signal, and to the gluino R-hadron signals by greater than a factor of five. While it is inherently difficult to
interpret the outcomes of a less-than-supervised ML tool, studies of the ANTELOPE score along with
traditional observables indicate that it is correlated to track displacement variables, as well as event-level
kinematic quantities such as missing energy and 𝑚 T .

6 Event selection
Events are required to have at least one 𝑝 𝑝 interaction vertex with at least two tracks with 𝑝 T greater than
500 MeV [72]. An event-level jet cleaning is applied to reduce the presence of beam-induced background,
cosmic rays, and calorimeter noise bursts [73]. A tight working point explicitly designed to provide higher
background rejection is used given the similarity of the semi-visible jet signal to non-collision backgrounds.
In addition to the standard cleaning, events containing jets in the bad hadronic calorimeter tiles have been
removed from the data sample [46].
A common preselection is applied to all events considered in the analysis. In order to reconstruct the
resonance mass, events must have at least 2 jets, each containing at least 3 tracks to ensure good modeling.
Since the signal process for this analysis does not directly produce leptons, events containing leptons
are vetoed from the data sample. To ensure full efficiency of the jet trigger, a requirement on the 𝑝 T of
the leading jet of at least 450 GeV is imposed. The subleading jet is required to have 𝑝 T > 150 GeV; in
conjunction with a selection that the Δ𝜙 between the leading two jets be greater than 0.8, this is found to
suppress contributions from non-collision background. Both leading jets must have |𝜂| < 2.1, to ensure
full tracking coverage. The absolute value of the difference in rapidity between the two leading jets, |Δy|,
must be < 2.8 to ensure final state objects that are central in 𝜂, an event characteristic that is associated
to heavy resonance production. A selection of 𝐸 Tmiss > 200 GeV is imposed to focus on events with the
key semi-visible jet characteristic of high missing energy due to dark particles in the shower. Finally,
𝑚 T is required to be greater than 1.5 TeV, to ensure that signal fits are performed on a smoothly falling
background.
A signal region (SR) is defined to enrich the presence of signal and remove SM background processes. The
background estimation in the SR is constructed using a control region (CR), which is defined to provide an
orthogonal set of data events enriched in background and similar in kinematic phase space to the SR. A
validation region (VR) is further defined to provide additional validation of the background estimation
strategy. A diagram summarizing the analysis regions and demonstrating the analysis flow can be seen in
Figure 5, with details of the selections provided below.
Three sensitive analysis variables are used to define the various analysis regions. Dark showers tend
to have higher track multiplicty and broader showers than SM multĳet processes, resulting in good
signal-background discrimination from the jet width, defined by the distance between the calorimeter
clusters and the jet axis scaled by the cluster energy:
𝑊j =

Σ𝑖 𝑝 𝑖T × Δ𝑅𝑖,jet
Σ𝑖 𝑝 𝑖T

where 𝑖 refers to a sum over calorimeter clusters and Δ𝑅𝑖,jet is the distance in 𝜂-𝜙 space between calorimeter
cluster 𝑖 and the jet axis [74].

12

## PDF page 13

CWoLa for anomaly detection

Preselection

25

J. Collins, K. Howe, BPN
PRD 99 (2019) 014038

VR
CWoLa for anomaly
detection

SR

25

Wj2 > 0.05

PFN

background
signal ?

CWoLa for anomaly detection

(supervised ML)

J. Collins, K. Howe, BPN
PRD 99 (2019) 014038

background

ANTELOPE

CR

(semi-supervised ML)

signal

Wj2 < 0.05
mmresT

Wj2

t

25

m
mTres

J. Collins, K. Howe, BPN
PRL 121 (2018) 241803

dN/dmres

J. Collins, K. Howe, BPN
PRD 99 (2019) 014038

dN/dmres

J. Collins, K. Howe, BPN
PRL 121 (2018) 241803

PFN Score < 0.6
OR
ANTELOPE Score < 0.7

dN/dmres

J. Collins, K. Howe, BPN
PRL 121 (2018) 241803

t
background
signal

mmresT

fi

fi

ML Score

Figure 5: Diagram indicating the analysis selections and background estimation/validation fitting strategy, where
𝑚 T refers to the transverse mass calculated with the leading two jets and 𝐸 Tmiss , Wj2 refers to the width of the
subleading jet, and PFN (ANTELOPE) score refer to the evaluated output of the PFN (ANTELOPE) models. The
CR and VR fit validations as well as the unblinded SR fit are done twice, once for each of the ML regions.

In particular, the subleading jet width Wj2 was found to provide discriminating power for all signals across
Rinv values, allowing for the definition of a signal-enriched region and a corresponding CR with a less than
1% signal contamination across all simulated signal grid points. A requirement of Wj2 > 0.05 is used to
define the SR, with the orthogonal requirement of Wj2 < 0.05 defining the CR.
The PFN and ANTELOPE scores (collectively referred to as “ML scores") as defined in Section 5 are also
highly useful to isolate signal-like events. Selections on both ML scores are chosen to maximize signal
sensitivity across the (m 𝑍 ′ , Rinv ) grid, leading to SR requirements of PFN score (ANTELOPE score) to be
greater than 0.6 (0.7) to define the SRPFN (SRAD ).
Figure 6 shows distributions of Wj2 , 𝑚 T , and 𝐸 Tmiss in data, as well as in background and signal simulation.
A fundamental assumption of the background estimation strategy is that Wj2 and ML scores are not strongly
correlated to 𝑚 T , to ensure no substantial sculpting of 𝑚 T could arise in the SR that would weaken the fit
studies performed in the CR and VR; this is observed to be true in data at preselection. A summary of
region selections can be found in Table 2.

7 Background estimation
The SM background in the SR is predominantly composed of multĳet events, and due to the poor modeling
of QCD by MC, it is estimated in a fully data-driven way. An empirical functional form is used for the
background shape of 𝑚 T . The ability of this function to model the background behavior is tested both in
MC and in data (CR and VR) and the shape parameters are left free in all the fits. Similarly, for the final
results, the shape parameters will be determined from the data fit in the SR.

13

## PDF page 14

1

10

0

10

1

ATLAS

A. U.

A. U.

10

Data
Multijet QCD
mZ = 2500 GeV, Rinv = 0.2
mZ = 4000 GeV, Rinv = 0.2
mZ = 2500 GeV, Rinv = 0.6
mZ = 4000 GeV, Rinv = 0.6

s = 13 TeV, 140 fb 1

0
0
0

10

1

10

0

1

10

2

10

2

10

3

10

3

10

4

10

4

10

5

10

5

10

6

10

6

10

7

7

10 0.00

0.05

0.10

0.15

0.20

0.25

0.30

Data
Multijet QCD
mZ = 2500 GeV, Rinv = 0.2
mZ = 4000 GeV, Rinv = 0.2
mZ = 2500 GeV, Rinv = 0.6
mZ = 4000 GeV, Rinv = 0.6

s = 13 TeV, 140 fb 1

0
0

10

0

ATLAS

0
0

2000

Wj2

4000

5000

6000

mT [GeV]

(b)

A. U.

(a)

3000

10

1

10

0

10

1

10

2

10

3

10

4

10

5

10

6

ATLAS

Data
Multijet QCD
mZ = 2500 GeV, Rinv = 0.2
mZ = 4000 GeV, Rinv = 0.2
mZ = 2500 GeV, Rinv = 0.6
mZ = 4000 GeV, Rinv = 0.6

s = 13 TeV, 140 fb 1

0
0
0
0

7

10 250

500

750

1000

1250

1500

1750

2000

Emiss
T [GeV]

(c)

Figure 6: Distributions of analysis variables (a) Wj2 , (b) 𝑚 T , and (c) 𝐸 Tmiss in data, background simulation, and signal
at preselection. All histograms are normalized to unity.

The fits are performed for 𝑚 T > 1500 GeV. The functional form is chosen for its fitting performance among
other lower/higher order functions and was used in several dĳet search analyses [75, 76]:
2

𝑓 (𝑥) = 𝑝 1 (1 − 𝑥) 𝑝2 𝑥 𝑝3 + 𝑝4 ln𝑥+ 𝑝5 ln 𝑥
√
where x = m𝑇 / 𝑠 and the 𝑝 𝑖 are free parameters. For SRPFN , the 𝑚 T distribution is fit to 90 even-width
bins, while SRAD uses 180 bins to ensure good granularity for the subsequent rebinning incorporating the
signal mass resolution that is described in Section 9.

8 Systematic uncertainties
As the background estimation procedure relies on fitting a functional form to the data, any smooth variation
on the 𝑚 T spectrum itself is absorbed by the background fit and the impact on the residuals is expected to be
small. Any remaining sources of systematic uncertainty apply to either the signal shape or normalization.

14

## PDF page 15

Table 2: Preselection requirements, as well as optimized requirements defining the SRs and background estimation
regions.

Variable
Njets
Ntracks (jet)
Nlep
𝑝 T 𝑗1 ( 𝑗2 ) [GeV]
Δ𝜙 ( 𝑗1 , 𝑗2 )
|𝜂 𝑗1 , 𝑗2 |
Δy
𝐸 Tmiss [GeV]
𝑚 T [GeV]
SRPFN
Wj2
PFN score
ANTELOPE score

> 0.6
–

Preselection requirements
≥2
≥3
=0
> 450 (> 150)
> 0.8
< 2.1
< 2.8
> 200
> 1500
SRAD VRPFN VRAD
CR
> 0.05
< 0.05
–
< 0.6
–
–
> 0.7
–
< 0.7
–

A background uncertainty is ascribed to the possible fitting of spurious signal from fluctuations in the
𝑚 T spectrum. This systematic is assessed as a normalization uncertainty on the signal model shape by
performing a signal-plus-background fit on blinded data events from the signal-depleted CR. Beforehand
the CR data is subject to a smoothing procedure based on functional decomposition to accommodate
statistical fluctuations at high 𝑚 T [77]. The amount of fitted spurious signal varies with Rinv and m 𝑍 ′ , but
is consistently below a level of 0.5𝜎, in line with recommendations [78]. This value is added as a number
of events that can be attributed to the spurious signal, which is custom for each simulated signal point.
A second normalization uncertainty is ascribed to the impact of theoretical modeling effects, of which
three sources are considered. The first arises from variations to the strong coupling constant 𝛼𝑠 and parton
distribution functions (PDFs), and the corresponding uncertainty is estimated through study of the signal
𝑚 T distribution under alternate PDF sets and taking an envelope of these variations in the 𝑚 T window
corresponding to the signal 𝑍 ′ mass, as prescribed by the PDF4LHC group [52]. Second, effects of
generator-level variations of the A14 tune on the initial-state and final-state radiation as well as multiple
parton interactions, are estimated by varying the strong coupling constant (𝛼s ), the renormalization scale
(𝜇r ), and the factorization scale (𝜇f ) and similarly evaluating the envelope in the relevant 𝑚 T window
for a given signal. Both of these theoretical sources of uncertainty are modeled as a flat 20% variation
on the theoretical cross section of the signal. The uncertainty in the combined 2015–2018 integrated
luminosity is 0.83%, obtained using the LUCID-2 detector [42] for the primary luminosity measurements,
complemented by measurements using the ID and calorimeters.
Systematic uncertainties that affect the shape of the signal in 𝑚 T come from instrumental effects, namely in
the small-R jet 𝑝 T scale. Such uncertainties are potentially impactful on an analysis that looks for localized
excesses on top of a smoothly falling background because they can shift the peak of the resonance. Jet
𝑝 T scale uncertainties are estimated using a methodology that compares track-to-calorimeter 𝑝 T double
ratios from data to simulation, from which baseline differences are ascribed to systematic effects [60]. In
this analysis, the total jet 𝑝 T scale uncertainty has a very small effect on the shape of the 𝑚 T spectrum, but
variations are nonetheless incorporated into the final signal-plus-background fits as nuisance parameters
with Gaussian constraints.

15

## PDF page 16

9 Statistical analysis
The statistical treatment of both the SRPFN and SRAD are developed through functional fitting of the
𝑚 T spectrum. Studies of the signal mass peak in 𝑚 T using double-sided Crystal Ball functions reveal
that the mass resolution varies from approximately 200 GeV for m 𝑍 ′ =2000 GeV and up to 800–1000
GeV for higher m 𝑍 ′ , depending on the Rinv value. Each 𝑚 T fit is performed with the five functional
parameters of the background function floating, including the background normalization. The CR and VR
are used to validate and test the function’s capability to fit different 𝑚 T spectra, but the final SRPFN and
SRAD functions are obtained from a new fit of each corresponding SR 𝑚 T distribution. Systematics are
modeled as nuisance parameters with Gaussian constraints, and can be either yield or shape uncertainties,
as discussed in Section 8.
A variety of fit tests are performed with the CR and VR data samples to ensure good quality of the
background expectation. The functional form in Section 7 is used to perform a background-only fit on
both simulated background and data in the CR and VR selection. To ensure that the fit tests are done on a
region with similar expected statistics to that of the SR, the SR yield is unblinded and the fit test region
is randomly downsampled to match the SR event yield. As the overall event count in the SR does not
incorporate the sensitive 𝑚 T shape information, this can be considered to not fully unblind the analysis
during fit development and risk the introduction of bias.
To further validate the fit in more instances, pseudo-data is created from the CR/VR data distributions.
It is created following the Asimov prescription with smoothing to accommodate fluctuations in the high
𝑚 T tail. The smoothing applied follows the procedure for functional decomposition described in Ref. [77].
Toys thrown from the resulting smoothed template produce distributions of background-only p-values
that are consistent with good modeling. A final fit check is performed by injecting signal into the CR
data template. These injections range in significance in the 𝑍 ′ mass window from 1𝜎 to 5𝜎, and a good
linearity is observed of the post-fit extracted number of signal events with respect to the injected number.
SRPFN Signal interpretations are extracted from SRPFN only via signal-plus-background fits using a
histogram of the SVJ signal template. The parameter of interest in the statistical analysis is the signal
strength 𝜇, defined as a scale factor multiplying the nominal yield predicted by a 1 pb signal cross section
so as to match the observed number of signal events. The background-only hypothesis corresponds to
𝜇 = 0. To accurately perform the fit, equidistant narrow-width bins are required as the fit function is
performed with RooPDF and evaluates the function at the center of the bin rather than integrating across
the bin [78]. Therefore, a narrow binning (90 across the 𝑚 T spectrum) is chosen to perform the functional
form background-only and signal-plus-background 𝑚 T fits for SRPFN .
SRAD As SRAD is built using an anomaly detection tool, it is not used to perform any signal-plusbackground fits. However, the generality of the tool used in its construction results in a region with broad
expected sensitivity to new physics producing resonances in 𝑚 T . Therefore, BumpHunter [79] is used to
quantify the significance of adjacent bins in 𝑚 T without a particular signal model shape. BumpHunter looks
for significant excesses in the 𝑚 T spectrum incorporating only the statistical uncertainty of the data and
the adjacency of bins that disagree between data and expectation. It outputs a p-value that provides a
goodness-of-fit metric to quantify the most significant excess across the spectrum, along with a window in
𝑚 T corresponding to this excess. To do this, the 180 narrow bins used for the functional fit are subsequently
rebinned to a wider variable binning that reflects the expected signal mass resolution, informed by the

16

## PDF page 17

10

4

10

3

10

2

10
10

Data - Fit
(Data)

10

ATLAS

Entries / 25 GeV

5

10

5

10

4

10

3

10

2

1

10

1

0

10

0

1

10

Data
Background-only fit
f(x) = p1(1 x)p2xp3 + p4lnx + p5ln2 x
SRPFN: p-value = 0.26

s = 13 TeV, 140 fb 1

2 / ndf = 1.09

2

Data - Fit
(Data)

Entries / 50 GeV

10

0
2
2000

3000

4000

5000

6000

ATLAS

2 / ndf = 0.93

1

2
0
2
2000

mT [GeV]

(a)

Data
Background-only fit
f(x) = p1(1 x)p2xp3 + p4lnx + p5ln2 x
SRAD: p-value = 0.74

s = 13 TeV, 140 fb 1

3000

4000

5000

6000

mT [GeV]

(b)

Figure 7: Distribution of data in the 𝑚 T spectrum of the (a) PFN and (b) ANTELOPE signal regions. No significant
excesses are found and good fit quality is obtained.

double-sided Crystal Ball mass peak fits, and thus increases in width for higher 𝑚 T . There is potential for a
spurious signal in the SRAD 𝑚 T spectrum that can be found by the BumpHunter procedure. To evaluate
this, BumpHunter fits are performed over Asimov data in the ANTELOPE CR and VR. In 100 trials, no
fits are found with BumpHunter 𝑝-values less than 0.01, indicating a small impact of potential spurious
signal effects.
The unblinded 𝑚 T distributions for the PFN and ANTELOPE signal regions can be seen in Figure 7. The
fit quality of the background function to the data is good, with 𝑝-values of 0.26 and 0.74 for the SRPFN and
SRAD respectively. No significant excesses of the data with respect to the background-only model are
observed. BumpHunter is run on the SRAD 𝑚 T distribution rebinned according to expected signal mass
resolution as described in Section 9 allowing for excesses with widths of at least 2 and at most 6 bins. The
BumpHunter interval of the SRAD 𝑚 T spectrum with the most significant excess is found to be between
1700 and 1900 GeV, with a corresponding BumpHunter p-value of 0.81, indicating that no significant
Gaussian resonance shape can be found in the data.
Upper limits on the signal production cross section 𝜎 times branching ratio 𝐵, are set at 95% confidence
level (CL) using the CL𝑠 method [80]. Figure 8 shows the 95% CL observed and expected limits obtained
from fitting the unblinded SR. As the data were found to be compatible with background prediction, a good
agreement of observed and expected limits is seen. The analysis delivers the best limits for low Rinv signal
points, with a loss of exclusion power at higher Rinv points due to the very broad signal shape in 𝑚 T . Values
of m 𝑍 ′ from 2000 to 3200 GeV are excluded to varying Rinv fractions ranging from 0.37 to 0.2, respectively.
Figure 9 shows the expected and observed exclusion to 95% confidence in the two-dimensional plane of
m 𝑍 ′ and Rinv . The analysis has the strongest exclusion power for low values of Rinv , where the signature is
more visible, and lower masses, where the production cross section of the signal is higher. These exclusions
are the first set by ATLAS on 𝑍 ′ -mediated semi-visible jet signals.
While the ANTELOPE region is not used to set limits on the signal grid, it can still be used to compare the
reach of the PFN SR to a less model-dependent approach. This is done through signal injection into the

17

## PDF page 18

4

10

3

10

2

10

1

10

0

ATLAS

95% CL upper limit on B [fb]

95% CL upper limit on B [fb]

10

Observed
Expected
Expected ±1
Expected ±2
Theory prediction

s = 13 TeV, 140 fb 1
SRPFN: Rinv = 0.2

Semi-visible jets s-channel

2000

2500

3000

3500

4000

4500

10

4

10

3

10

2

10

1

10

0

5000

ATLAS

Semi-visible jets s-channel

2000

mZ [GeV]

Observed
Expected
Expected ±1
Expected ±2
Theory prediction

s = 13 TeV, 140 fb 1
SRPFN: Rinv = 0.4

2500

3000

3500

0

4000

4500

5000

mZ [GeV]
0

(b)

95% CL upper limit on B [fb]

(a)

10

4

10

3

10

2

10

1

10

0

ATLAS

Observed
Expected
Expected ±1
Expected ±2
Theory prediction

s = 13 TeV, 140 fb 1
SRPFN: Rinv = 0.6

Semi-visible jets s-channel

2000

2500

3000

3500

4000

4500

5000

mZ [GeV]
0

(c)

Figure 8: Observed (solid) and expected (dashed) limits at 95% CL on the production cross section 𝜎 times branching
ratio 𝐵 of the 𝑍 ′ mediator as a function of 𝑍 ′ mass in GeV, for simulated Rinv of (a) 0.2, (b) 0.4, and (c) 0.6. The dark
(light) band around the limits represents the ±1 (2) uncertainty band. The predicted theoretical cross section is also
included in red obtained from the model discussed in Section 3.

ANTELOPE data to determine the 95% upper limit on the signal strength 𝜇 of both the SVJ and alternate
signal models discussed in Section 3. The background is taken to be the background-only functional fit.
The 95% upper limit is defined as the amount of signal at which BumpHunter returns a 2𝜎 significance.
As this check uses only BumpHunter, none of the signal systematics are applied, meaning these limits
cannot be compared to dedicated analyses for theses signals. Figure 10 shows the resulting limit plot
comparing the PFN and ANTELOPE SRs. As expected, the dedicated PFN region designed for the SVJ
signals provides the better limit on the SVJ grid points by approximately a factor of two. However, the
ANTELOPE region takes over with nearly an order of magnitude improvement on the emerging jet and
gluino R-hadron alternate signals. This demonstrates the generality of the ANTELOPE tool and its utility
to provide anomaly detection capability in this search.

18

## PDF page 19

0.60

s = 13 TeV, 140 fb 1

0.55
0.50

Semi-visible jets s-channel
Observed
Expected
Expected ±1
Expected ±2

10

3

10

2

10

1

0.45
0.40
0.35
0.30
0.25
0.20
2000

2500

3000

3500

4000

4500

95% CL upper limit on B [fb]

Rinv

ATLAS

5000

mZ [GeV]
0

Figure 9: The expected and observed exclusion contours at 95% CL for the generated signal parameterized by Rinv on
the vertical axis and m 𝑍 ′ on the horizontal axis. The dashed line indicates the expected limit and the solid line
corresponds to the observed limit derived from the unblinded SRPFN .

19

## PDF page 20

1

10

0

ATLAS

s = 13 TeV, 140 fb 1

1

10

2

Injected signal

0

0

mZ

m g eV, s)
n(
T
n
d ro = 2
=1
g
-h a
d
o R on (m V,
r
uin
Te
Gl
ad
h
= 1 6)
o R (m X
.
uin
=0
s
Gl
jet
inv
.2)
ing V, R
=0
e rg
Te
Em = 4 , R inv
m Z TeV
J(
5
SV = 2.

10

SRAD / SRPFN
Uncertainty

J(
SV

Ratio of 95% CL upper limit on

10

=3
V,
Te
g

g

=0

=0

ns
)

.03

ns
)

.03

Figure 10: The ratio of the 95% upper limit on the signal strength for five benchmark signal processes, including two
SVJ signals and three alternate models, comparing the PFN and ANTELOPE signal regions. The signal strength is
obtained by injecting signal into the observed data until 2𝜎 sensitivity is achieved as determined by the BumpHunter
interval 𝑝-value. The background is taken to be the result of the background-only functional fit on each unblinded
region. The uncertainty band reflects the standard deviation of obtained signal strength values for 100 trials. SVJ
signals are labeled by their m 𝑍 ′ and Rinv values, gluino signals by the gluino mass and lifetime, and the emerging jet
signal has 𝑚 𝑍 ′ = 1000 GeV and 𝑐𝜏𝜋𝑑 = 1 mm. The PFN SR provides the best limit for the SVJ signal models which
it saw in training, while the ANTELOPE region takes over for alternate signal models, indicating its lower degree of
model dependence.

20

## PDF page 21

10 Conclusions
A search has been presented for strongly coupled dark sector particles in semi-visible jet signatures. The
SVJ signal is generated through the resonant production of a heavy 𝑍 ′ mediator decaying to two dark
quarks which decay to jets with a fraction Rinv of constituent particles that are invisible to the detector.
Signal-like events are selected with the assistance of two machine learning tools which focus on track-level
permutation invariant modeling of the events. One of these, a ParticleFlow Network, provides the highest
sensitivity to the simulated SVJ signal, while the second tool ANTELOPE focuses on anomaly detection
through generalized sensitivity to a wide variety of signal models. The analysis searches for excesses
on top of a smoothly falling 𝑚 T spectrum, which is estimated with a five-parameter functional fit. No
significant excesses are observed in the unblinded PFN and ANTELOPE regions, and upper limits are
set on the production cross section of the 𝑍 ′ . Signal points with m 𝑍 ′ between 2000 and 3200 GeV are
excluded at 95% CL for Rinv ranging from 0.2 to 0.37.

Acknowledgements
We thank CERN for the very successful operation of the LHC and its injectors, as well as the support staff
at CERN and at our institutions worldwide without whom ATLAS could not be operated efficiently.
The crucial computing support from all WLCG partners is acknowledged gratefully, in particular from
CERN, the ATLAS Tier-1 facilities at TRIUMF/SFU (Canada), NDGF (Denmark, Norway, Sweden),
CC-IN2P3 (France), KIT/GridKA (Germany), INFN-CNAF (Italy), NL-T1 (Netherlands), PIC (Spain),
RAL (UK) and BNL (USA), the Tier-2 facilities worldwide and large non-WLCG resource providers.
Major contributors of computing resources are listed in Ref. [81].
We gratefully acknowledge the support of ANPCyT, Argentina; YerPhI, Armenia; ARC, Australia; BMWFW
and FWF, Austria; ANAS, Azerbaĳan; CNPq and FAPESP, Brazil; NSERC, NRC and CFI, Canada; CERN;
ANID, Chile; CAS, MOST and NSFC, China; Minciencias, Colombia; MEYS CR, Czech Republic; DNRF
and DNSRC, Denmark; IN2P3-CNRS and CEA-DRF/IRFU, France; SRNSFG, Georgia; BMBF, HGF and
MPG, Germany; GSRI, Greece; RGC and Hong Kong SAR, China; ICHEP and Academy of Sciences
and Humanities, Israel; INFN, Italy; MEXT and JSPS, Japan; CNRST, Morocco; NWO, Netherlands;
RCN, Norway; MNiSW, Poland; FCT, Portugal; MNE/IFA, Romania; MSTDI, Serbia; MSSR, Slovakia;
ARIS and MVZI, Slovenia; DSI/NRF, South Africa; MICIU/AEI, Spain; SRC and Wallenberg Foundation,
Sweden; SERI, SNSF and Cantons of Bern and Geneva, Switzerland; NSTC, Taipei; TENMAK, Türkiye;
STFC/UKRI, United Kingdom; DOE and NSF, United States of America.
Individual groups and members have received support from BCKDF, CANARIE, CRC and DRAC,
Canada; CERN-CZ, FORTE and PRIMUS, Czech Republic; COST, ERC, ERDF, Horizon 2020, ICSCNextGenerationEU and Marie Skłodowska-Curie Actions, European Union; Investissements d’Avenir Labex,
Investissements d’Avenir Idex and ANR, France; DFG and AvH Foundation, Germany; Herakleitos, Thales
and Aristeia programmes co-financed by EU-ESF and the Greek NSRF, Greece; BSF-NSF and MINERVA,
Israel; NCN and NAWA, Poland; La Caixa Banking Foundation, CERCA Programme Generalitat de
Catalunya and PROMETEO and GenT Programmes Generalitat Valenciana, Spain; Göran Gustafssons
Stiftelse, Sweden; The Royal Society and Leverhulme Trust, United Kingdom.
In addition, individual members wish to acknowledge support from Armenia: Yerevan Physics Institute
(FAPERJ); CERN: European Organization for Nuclear Research (CERN DOCT); Chile: Agencia Nacional

21

## PDF page 22

de Investigación y Desarrollo (FONDECYT 1230812, FONDECYT 1240864); China: Chinese Ministry
of Science and Technology (MOST-2023YFA1605700, MOST-2023YFA1609300), National Natural
Science Foundation of China (NSFC - 12175119, NSFC 12275265); Czech Republic: Czech Science
Foundation (GACR - 24-11373S), Ministry of Education Youth and Sports (ERC-CZ-LL2327, FORTE
CZ.02.01.01/00/22_008/0004632), PRIMUS Research Programme (PRIMUS/21/SCI/017); EU: H2020
European Research Council (ERC - 101002463); European Union: European Research Council (BARD No.
101116429, ERC - 948254, ERC 101089007), European Regional Development Fund (SMASH COFUND
101081355, SLO ERDF), Horizon 2020 Framework Programme (MUCCA - CHIST-ERA-19-XAI-00),
European Union, Future Artificial Intelligence Research (FAIR-NextGenerationEU PE00000013), Italian
Center for High Performance Computing, Big Data and Quantum Computing (ICSC, NextGenerationEU);
France: Agence Nationale de la Recherche (ANR-21-CE31-0022, ANR-22-EDIR-0002); Germany: BadenWürttemberg Stiftung (BW Stiftung-Postdoc Eliteprogramme), Deutsche Forschungsgemeinschaft (DFG
- 469666862, DFG - CR 312/5-2); China: Research Grants Council (GRF); Italy: Istituto Nazionale
di Fisica Nucleare (ICSC, NextGenerationEU), Ministero dell’Università e della Ricerca (NextGenEU
I53D23000820006 M4C2.1.1, SOE2024_0000023); Japan: Japan Society for the Promotion of Science
(JSPS KAKENHI JP22H01227, JSPS KAKENHI JP22H04944, JSPS KAKENHI JP22KK0227, JSPS
KAKENHI JP23KK0245, JSPS KAKENHI JP24K23939); Norway: Research Council of Norway
(RCN-314472); Poland: Ministry of Science and Higher Education (IDUB AGH, POB8, D4 no 9722),
Polish National Science Centre (NCN 2021/42/E/ST2/00350, NCN OPUS 2023/51/B/ST2/02507, NCN
OPUS nr 2022/47/B/ST2/03059, NCN UMO-2019/34/E/ST2/00393, UMO-2022/47/O/ST2/00148, UMO2023/49/B/ST2/04085, UMO-2023/51/B/ST2/00920, UMO-2024/53/N/ST2/00869); Portugal: Foundation
for Science and Technology (FCT); Spain: Ministry of Science and Innovation (MCIN & NextGenEU
PCI2022-135018-2, MICIN & FEDER PID2021-125273NB, RYC2019-028510-I, RYC2020-030254-I,
RYC2021-031273-I, RYC2022-038164-I); Sweden: Carl Trygger Foundation (Carl Trygger Foundation CTS
22:2312), Swedish Research Council (Swedish Research Council 2023-04654, VR 2021-03651, VR 202203845, VR 2022-04683, VR 2023-03403, VR 2024-05451), Knut and Alice Wallenberg Foundation (KAW
2018.0458, KAW 2022.0358, KAW 2023.0366); Switzerland: Swiss National Science Foundation (SNSF PCEFP2_194658); United Kingdom: Leverhulme Trust (Leverhulme Trust RPG-2020-004), Royal Society
(NIF-R1-231091); United States of America: U.S. Department of Energy (ECA DE-AC02-76SF00515),
Neubauer Family Foundation.

References
[1]

M. Persic, P. Salucci, and F. Stel,
The universal rotation curve of spiral galaxies - I. The dark matter connection,
Mon. Not. Roy. Astron. Soc. 281 (1996) 27, arXiv: astro-ph/9506004.

[2]

D. Clowe et al., A Direct Empirical Proof of the Existence of Dark Matter*,
Astrophys. J. Lett. 648 (2006) L109, arXiv: astro-ph/0608407.

[3]

C. Chang et al., Dark Energy Survey Year 1 results: curved-sky weak lensing mass map,
Mon. Not. Roy. Astron. Soc. 475 (2018) 3165, arXiv: 1708.01535 [astro-ph.CO].

[4]

M. Cirelli, A. Strumia, and J. Zupan, Dark Matter, 2024, arXiv: 2406.01705 [hep-ph].

[5]

C. Balazs, T. Bringmann, F. Kahlhoefer, and M. White, A Primer on Dark Matter, 2024,
arXiv: 2411.05062 [astro-ph.CO].

[6]

L. Evans and P. Bryant, LHC Machine, JINST 3 (2008) S08001.

22

## PDF page 23

[7]

G. Jungman, M. Kamionkowski, and K. Griest, Supersymmetric dark matter,
Phys. Rept. 267 (1996) 195, arXiv: hep-ph/9506380.

[8]

M. J. Strassler and K. M. Zurek, Echoes of a hidden valley at hadron colliders,
Phys. Lett. B 651 (2007) 374, arXiv: hep-ph/0604261.

[9]

T. Han, Z. Si, K. M. Zurek, and M. J. Strassler,
Phenomenology of hidden valleys at hadron colliders, JHEP 07 (2008) 008,
arXiv: 0712.2041 [hep-ph].

[10]

V. Belis, P. Odagiu, and T. K. Aarrestad,
Machine learning for anomaly detection in particle physics, Rev. Phys. 12 (2024) 100091,
arXiv: 2312.14190 [physics.data-an].

[11]

H. Beauchesne, E. Bertuzzo, and G. Grilli di Cortona,
Dark matter in Hidden Valley models with stable and unstable light dark mesons,
JHEP 04 (2019) 118, arXiv: 1809.10152 [hep-ph].

[12]

Y. Bai and P. Schwaller, Scale of dark QCD, Phys. Rev. D 89 (2014) 063522,
arXiv: 1306.4676 [hep-ph].

[13]

T. Cohen, M. Lisanti, and H. K. Lou, Semivisible Jets: Dark Matter Undercover at the LHC,
Phys. Rev. Lett. 115 (2015) 171804, arXiv: 1503.00009 [hep-ph].

[14]

M. J. Strassler, On the Phenomenology of Hidden Valleys with Heavy Flavor, 2008,
arXiv: 0806.2385 [hep-ph].

[15]

E. Bernreuther, F. Kahlhoefer, M. Krämer, and P. Tunney,
Strongly interacting dark sectors in the early Universe and at the LHC through a simplified portal,
JHEP 01 (2020) 162, arXiv: 1907.04346 [hep-ph].

[16]

G. Albouy et al.,
Theory, phenomenology, and experimental avenues for dark showers: a Snowmass 2021 report,
Eur. Phys. J. C 82 (2022) 1132, arXiv: 2203.09503 [hep-ph].

[17]

T. Faucett, S.-C. Hsu, and D. Whiteson, Learning to identify semi-visible jets, JHEP 12 (2022) 132,
arXiv: 2208.10062 [hep-ph].

[18]

B. Liu and K. Pedro, Semi-visible jets + X: illuminating dark showers with radiation,
JHEP 12 (2024) 105, arXiv: 2409.04741 [hep-ph].

[19]

J. Barron, D. Curtin, G. Kasieczka, T. Plehn, and A. Spourdalakis,
Unsupervised hadronic SUEP at the LHC, JHEP 12 (2021) 129, arXiv: 2107.12379 [hep-ph].

[20]

F. Canelli et al., Autoencoders for semivisible jet detection, JHEP 02 (2022) 074,
arXiv: 2112.02864 [hep-ph].

[21]

L. Favaro, M. Krämer, T. Modak, T. Plehn, and J. Rüschkamp,
Semi-visible jets, energy-based models, and self-supervision, SciPost Phys. 18 (2025) 042,
arXiv: 2312.03067 [hep-ph].

[22]

K. Pedro and P. Shyamsundar, Optimal mass variables for semivisible jets,
SciPost Phys. Core 6 (2023) 067, arXiv: 2303.16253 [hep-ph].

[23]

D. Bardhan, Y. Kats, and N. Wunch,
Searching for dark jets with displaced vertices using weakly supervised machine learning,
Phys. Rev. D 108 (2023) 035036, arXiv: 2305.04372 [hep-ph].

23

## PDF page 24

[24]

K. Bai, R. Mastandrea, and B. Nachman,
Non-resonant anomaly detection with background extrapolation, JHEP 04 (2024) 059,
arXiv: 2311.12924 [hep-ph].

[25]

ATLAS Collaboration,
Search for resonant production of dark quarks in the dĳet final state with the ATLAS detector,
JHEP 02 (2024) 128, arXiv: 2311.03944 [hep-ex].

[26]

ATLAS Collaboration,
Search for non-resonant production of semi-visible jets using Run 2 data in ATLAS,
Phys. Lett. B 848 (2024) 138324, arXiv: 2305.18037 [hep-ex].

[27]

ATLAS Collaboration, Search for dark mesons decaying to top and bottom quarks in proton-proton
√
collisions at s = 13 TeV with the ATLAS detector, JHEP 09 (2024) 005,
arXiv: 2405.20061 [hep-ex].

[28]

ATLAS Collaboration,
√
Search for emerging jets in 𝑝 𝑝 collisions at 𝑠 = 13.6 TeV with the ATLAS experiment,
CERN-EP-2025-099, 2025.

[29]

CMS Collaboration,
Search for resonant production of strongly coupled dark matter in proton-proton collisions at 13 TeV,
JHEP 6 (2022) 156, arXiv: 2112.11125 [hep-ex].

[30]

CMS Collaboration, Search for new particles decaying to a jet and an emerging jet,
JHEP 02 (2019) 179, arXiv: 1810.10069 [hep-ex].

[31]

CMS Collaboration,
√
Search for dark QCD with emerging jets in proton-proton collisions at 𝑠 = 13 TeV,
JHEP 07 (2024) 142, arXiv: 2403.01556 [hep-ex].

[32]

G. Kasieczka et al.,
The LHC Olympics 2020 a community challenge for anomaly detection in high energy physics,
Rept. Prog. Phys. 84 (2021) 124201, arXiv: 2101.08320 [hep-ph].

[33]

T. Aarrestad et al., The Dark Machines Anomaly Score Challenge: Benchmark Data and Model
Independent Event Classification for the Large Hadron Collider, SciPost Phys. 12 (2022) 043,
arXiv: 2105.14027 [hep-ph].

[34]

CMS Collaboration, Model-agnostic search for dĳet resonances with anomalous jet substructure in
√
proton-proton collisions at 𝑠 = 13 TeV, 2024, arXiv: 2412.03747 [hep-ex].
√
[35] ATLAS Collaboration, Dĳet Resonance Search with Weak Supervision Using 𝑠 = 13 TeV 𝑝 𝑝
Collisions in the ATLAS Detector, Phys. Rev. Lett. 125 (2020) 131801,
arXiv: 2005.02983 [hep-ex].
[36]

ATLAS Collaboration,
Anomaly detection search for new resonances decaying into a Higgs boson and a generic new
√
particle 𝑋 in hadronic final states using 𝑠 = 13 TeV 𝑝 𝑝 collisions with the ATLAS detector,
Phys. Rev. D 108 (2023) 052009, arXiv: 2306.03637 [hep-ex].

[37]

ATLAS Collaboration,
Search for New Phenomena in Two-Body Invariant Mass Distributions Using Unsupervised
√
Machine Learning for Anomaly Detection at 𝑠 = 13 TeV with the ATLAS Detector,
Phys. Rev. Lett. 132 (2024) 081801, arXiv: 2307.01612 [hep-ex].

24

## PDF page 25

[38]

ATLAS Collaboration, Weakly supervised anomaly detection for resonant new physics in the dĳet
√
final state using proton-proton collisions at 𝑠 = 13 TeV with the ATLAS detector, 2025,
arXiv: 2502.09770 [hep-ex].

[39]

ATLAS Collaboration, The ATLAS Experiment at the CERN Large Hadron Collider,
JINST 3 (2008) S08003.

[40]

ATLAS Collaboration, ATLAS Insertable B-Layer: Technical Design Report,
ATLAS-TDR-19; CERN-LHCC-2010-013, 2010,
url: https://cds.cern.ch/record/1291633, Addendum: ATLAS-TDR-19-ADD-1;
CERN-LHCC-2012-009, 2012, url: https://cds.cern.ch/record/1451888.

[41]

B. Abbott et al., Production and integration of the ATLAS Insertable B-Layer,
JINST 13 (2018) T05008, arXiv: 1803.00844 [physics.ins-det].

[42]

G. Avoni et al., The new LUCID-2 detector for luminosity measurement and monitoring in ATLAS,
JINST 13 (2018) P07017.

[43]

ATLAS Collaboration, Performance of the ATLAS trigger system in 2015,
Eur. Phys. J. C 77 (2017) 317, arXiv: 1611.09661 [hep-ex].

[44]

ATLAS Collaboration, Software and computing for Run 3 of the ATLAS experiment at the LHC,
Eur. Phys. J. C 85 (2025) 234, arXiv: 2404.06335 [hep-ex].

[45]

ATLAS Collaboration,
√
Luminosity determination in 𝑝 𝑝 collisions at 𝑠 = 13 TeV using the ATLAS detector at the LHC,
Eur. Phys. J. C 83 (2023) 982, arXiv: 2212.09379 [hep-ex].

[46]

ATLAS Collaboration, ATLAS data quality operations and performance for 2015–2018 data-taking,
JINST 15 (2020) P04003, arXiv: 1911.04632 [physics.ins-det].

[47]

ATLAS Collaboration, The ATLAS Simulation Infrastructure, Eur. Phys. J. C 70 (2010) 823,
arXiv: 1005.4568 [physics.ins-det].

[48]

S. Agostinelli et al., Geant4 – a simulation toolkit, Nucl. Instrum. Meth. A 506 (2003) 250.

[49]

J. Alwall et al., The automated computation of tree-level and next-to-leading order differential cross
sections, and their matching to parton shower simulations, JHEP 07 (2014) 079,
arXiv: 1405.0301 [hep-ph].

[50]

T. Sjöstrand et al., An introduction to PYTHIA 8.2, Comput. Phys. Commun. 191 (2015) 159,
arXiv: 1410.3012 [hep-ph].

[51]

N. Lavesson and L. Lönnblad, Merging parton showers and matrix elements—back to basics,
JHEP 04 (2008) 085, arXiv: 0712.2966 [hep-ph].

[52]

J. Butterworth et al., PDF4LHC recommendations for LHC Run II, J. Phys. G 43 (2016) 023001,
arXiv: 1510.03865 [hep-ph].

[53]

ATLAS Collaboration, ATLAS Pythia 8 tunes to 7 TeV data, ATL-PHYS-PUB-2014-021, 2014,
url: https://cds.cern.ch/record/1966419.

[54]

T. Cohen, M. Lisanti, H. K. Lou, and S. Mishra-Sharma, LHC searches for dark sector showers,
JHEP 11 (2017) 196, arXiv: 1707.05326 [hep-ph].

[55]

A. Arvanitaki, N. Craig, S. Dimopoulos, and G. Villadoro, Mini-Split, JHEP 02 (2013) 126,
arXiv: 1210.0555 [hep-ph].

25

## PDF page 26

[56]

M. Cacciari, G. P. Salam, and G. Soyez, The anti-𝑘 𝑡 jet clustering algorithm, JHEP 04 (2008) 063,
arXiv: 0802.1189 [hep-ph].

[57]

M. Cacciari, G. P. Salam, and G. Soyez, FastJet user manual, Eur. Phys. J. C 72 (2012) 1896,
arXiv: 1111.6097 [hep-ph].

[58]

ATLAS Collaboration,
Topological cell clustering in the ATLAS calorimeters and its performance in LHC Run 1,
Eur. Phys. J. C 77 (2017) 490, arXiv: 1603.02934 [hep-ex].

[59]

ATLAS Collaboration,
Jet reconstruction and performance using particle flow with the ATLAS Detector,
Eur. Phys. J. C 77 (2017) 466, arXiv: 1703.10485 [hep-ex].

[60]

ATLAS Collaboration, Jet energy scale and resolution measured in proton–proton collisions at
√
𝑠 = 13 TeV with the ATLAS detector, Eur. Phys. J. C 81 (2021) 689,
arXiv: 2007.02645 [hep-ex].

[61]

ATLAS Collaboration, Performance of jet substructure techniques for large-𝑅 jets in proton–proton
√
collisions at 𝑠 = 7 TeV using the ATLAS detector, JHEP 09 (2013) 076,
arXiv: 1306.4945 [hep-ex].

[62]

ATLAS Collaboration, Electron and photon performance measurements with the ATLAS detector
using the 2015–2017 LHC proton–proton collision data, JINST 14 (2019) P12006,
arXiv: 1908.00005 [hep-ex].

[63]

ATLAS Collaboration, Muon reconstruction and identification efficiency in ATLAS using the full
√
Run 2 𝑝 𝑝 collision data set at 𝑠 = 13 TeV, Eur. Phys. J. C 81 (2021) 578,
arXiv: 2012.00578 [hep-ex].

[64]

ATLAS Collaboration, The performance of missing transverse momentum reconstruction and its
√
significance with the ATLAS detector using 140 fb−1 of 𝑠 = 13 TeV 𝑝 𝑝 collisions, (2024),
arXiv: 2402.05858 [hep-ex].

[65]

P. T. Komiske, E. M. Metodiev, and J. Thaler, Energy flow networks: deep sets for particle jets,
JHEP 01 (2019) 121, arXiv: 1810.05165 [hep-ph].

[66]

M. Zaheer et al., Deep Sets, 2018, arXiv: 1703.06114 [cs.LG].

[67]

X. Glorot, A. Bordes, and Y. Bengio, “Deep Sparse Rectifier Neural Networks,”
Proceedings of the Fourteenth International Conference on Artificial Intelligence and Statistics,
ed. by G. Gordon, D. Dunson, and M. Dudík, vol. 15, Proceedings of Machine Learning Research,
Fort Lauderdale, FL, USA: PMLR, 2011 315.

[68]

C. M. Bishop, Pattern Recognition and Machine Learning (Information Science and Statistics),
Berlin, Heidelberg: Springer-Verlag, 2006.

[69]

D. P. Kingma and J. Ba, Adam: A Method for Stochastic Optimization, 2017,
arXiv: 1412.6980 [cs.LG].

[70]

G. Matos, E. Busch, K. R. Park, and J. Gonski,
Semi-supervised permutation invariant particle-level anomaly detection, 2024,
arXiv: 2408.17409 [hep-ph].

[71]

D. P. Kingma and M. Welling, Auto-Encoding Variational Bayes, (2022),
arXiv: 1312.6114 [stat.ML].

26

## PDF page 27

[72]

√
ATLAS Collaboration, Vertex Reconstruction Performance of the ATLAS Detector at 𝑠 = 13 TeV,
ATL-PHYS-PUB-2015-026, 2015, url: https://cds.cern.ch/record/2037717.

[73]

ATLAS Collaboration,
Selection of jets produced in 13 TeV proton–proton collisions with the ATLAS detector,
ATLAS-CONF-2015-029, 2015, url: https://cds.cern.ch/record/2037702.

[74]

ATLAS Collaboration,
√
Jet energy measurement with the ATLAS detector in proton–proton collisions at 𝑠 = 7 TeV,
Eur. Phys. J. C 73 (2013) 2304, arXiv: 1112.6426 [hep-ex].

[75]

ATLAS Collaboration, Search for dĳet resonances in events with an isolated charged lepton using
√
𝑠 = 13 TeV proton–proton collision data collected by the ATLAS detector, JHEP 06 (2020) 151,
arXiv: 2002.11325 [hep-ex].

[76]

ATLAS Collaboration, Search for low-mass dĳet resonances using trigger-level jets with the ATLAS
√
detector in 𝑝 𝑝 collisions at 𝑠 = 13 TeV, Phys. Rev. Lett. 121 (2018) 081801,
arXiv: 1804.03496 [hep-ex].

[77]

R. Edgar, D. Amidei, C. Grud, and K. Sekhon,
Functional Decomposition: A new method for search and limit setting, 2018,
arXiv: 1805.04536 [physics.data-an].

[78]

ATLAS Collaboration, Recommendations for the Modeling of Smooth Backgrounds,
ATL-PHYS-PUB-2020-028, 2020, url: https://cds.cern.ch/record/2743717.

[79]

G. Choudalakis, On hypothesis testing, trials factor, hypertests and the BumpHunter, 2011,
arXiv: 1101.0390 [physics.data-an].

[80]

A. L. Read, Presentation of search results: the 𝐶 𝐿 𝑠 technique, J. Phys. G 28 (2002) 2693.

[81]

ATLAS Collaboration, ATLAS Computing Acknowledgements, ATL-SOFT-PUB-2025-001, 2025,
url: https://cds.cern.ch/record/2922210.

27

## PDF page 28

The ATLAS Collaboration
G. Aad 104 , E. Aakvaag 17 , B. Abbott 123 , S. Abdelhameed 119a , K. Abeling 55 , N.J. Abicht 49 ,
S.H. Abidi 30 , M. Aboelela 45 , A. Aboulhorma 36e , H. Abramowicz 157 , Y. Abulaiti 120 ,
B.S. Acharya 69a,69b,m , A. Ackermann 63a , C. Adam Bourdarios 4 , L. Adamczyk 86a ,
S.V. Addepalli 149 , M.J. Addison 103 , J. Adelman 118 , A. Adiguzel 22c , T. Adye 137 ,
A.A. Affolder 139 , Y. Afik 40 , M.N. Agaras 13 , A. Aggarwal 102 , C. Agheorghiesei 28c ,
F. Ahmadov 39,ad , S. Ahuja 97 , X. Ai 143b , G. Aielli 76a,76b , A. Aikot 169 , M. Ait Tamlihat 36e ,
B. Aitbenchikh 36a , M. Akbiyik 102 , T.P.A. Åkesson 100 , A.V. Akimov 151 , D. Akiyama 174 ,
N.N. Akolkar 25 , S. Aktas 22a , G.L. Alberghi 24b , J. Albert 171 , P. Albicocco 53 , G.L. Albouy 60 ,
S. Alderweireldt 52 , Z.L. Alegria 124 , M. Aleksa 37 , I.N. Aleksandrov 39 , C. Alexa 28b ,
T. Alexopoulos 10 , F. Alfonsi 24b , M. Algren 56 , M. Alhroob 173 , B. Ali 135 , H.M.J. Ali 93,w ,
S. Ali 32 , S.W. Alibocus 94 , M. Aliev 34c , G. Alimonti 71a , W. Alkakhi 55 , C. Allaire 66 ,
B.M.M. Allbrooke 152 , J.S. Allen 103 , J.F. Allen 52 , P.P. Allport 21 , A. Aloisio 72a,72b ,
F. Alonso 92 , C. Alpigiani 142 , Z.M.K. Alsolami 93 , A. Alvarez Fernandez 102 ,
M. Alves Cardoso 56 , M.G. Alviggi 72a,72b , M. Aly 103 , Y. Amaral Coutinho 83b , A. Ambler 106 ,
C. Amelung37 , M. Amerl 103 , C.G. Ames 111 , T. Amezza 130 , D. Amidei 108 , B. Amini 54 ,
K. Amirie 161 , A. Amirkhanov 39 , S.P. Amor Dos Santos 133a , K.R. Amos 169 ,
D. Amperiadou 158 , S. An84 , C. Anastopoulos 145 , T. Andeen 11 , J.K. Anders 94 ,
A.C. Anderson 59 , A. Andreazza 71a,71b , S. Angelidakis 9 , A. Angerami 42 , A.V. Anisenkov 39 ,
A. Annovi 74a , C. Antel 37 , E. Antipov 151 , M. Antonelli 53 , F. Anulli 75a , M. Aoki 84 ,
T. Aoki 159 , M.A. Aparo 152 , L. Aperio Bella 48 , M. Apicella31 , C. Appelt 157 , A. Apyan 27 ,
M. Arampatzi 10 , S.J. Arbiol Val 87 , C. Arcangeletti 53 , A.T.H. Arce 51 , J-F. Arguin 110 ,
S. Argyropoulos 158 , J.-H. Arling 48 , O. Arnaez 4 , H. Arnold 151 , G. Artoni 75a,75b ,
H. Asada 113 , K. Asai 121 , S. Asai 159 , S. Asatryan 179 , N.A. Asbah 37 ,
R.A. Ashby Pickering 173 , A.M. Aslam 97 , K. Assamagan 30 , R. Astalos 29a , K.S.V. Astrand 100 ,
S. Atashi 165 , R.J. Atkin 34a , H. Atmani36f , P.A. Atmasiddha 131 , K. Augsten 135 , A.D. Auriol 41 ,
V.A. Austrup 103 , G. Avolio 37 , K. Axiotis 56 , G. Azuelos 110,ah , A. Azzam 13 , D. Babal 29b ,
H. Bachacou 138 , K. Bachas 158,q , A. Bachiu 35 , E. Bachmann 50 , M.J. Backes 63a , A. Badea 40 ,
T.M. Baer 108 , P. Bagnaia 75a,75b , M. Bahmani 19 , D. Bahner 54 , K. Bai 126 , J.T. Baines 137 ,
L. Baines 96 , O.K. Baker 178 , E. Bakos 16 , D. Bakshi Gupta 8 , L.E. Balabram Filho 83b ,
V. Balakrishnan 123 , R. Balasubramanian 4 , E.M. Baldin 38 , P. Balek 86a , E. Ballabene 24b,24a ,
F. Balli 138 , L.M. Baltes 63a , W.K. Balunas 33 , J. Balz 102 , I. Bamwidhi 119b , E. Banas 87 ,
M. Bandieramonte 132 , A. Bandyopadhyay 25 , S. Bansal 25 , L. Barak 157 , M. Barakat 48 ,
E.L. Barberio 107 , D. Barberis 18b , M. Barbero 104 , M.Z. Barel 117 , T. Barillari 112 ,
M-S. Barisits 37 , T. Barklow 149 , P. Baron 136 , D.A. Baron Moreno 103 , A. Baroncelli 62 ,
A.J. Barr 129 , J.D. Barr 98 , F. Barreiro 101 , J. Barreiro Guimarães da Costa 14 ,
M.G. Barros Teixeira 133a , S. Barsov 38 , F. Bartels 63a , R. Bartoldus 149 , A.E. Barton 93 ,
P. Bartos 29a , A. Basan 102 , M. Baselga 49 , S. Bashiri87 , A. Bassalat 66,b , M.J. Basso 162a ,
S. Bataju 45 , R. Bate 170 , R.L. Bates 59 , S. Batlamous101 , M. Battaglia 139 , D. Battulga 19 ,
M. Bauce 75a,75b , M. Bauer 79 , P. Bauer 25 , L.T. Bayer 48 , L.T. Bazzano Hurrell 31 ,
J.B. Beacham 112 , T. Beau 130 , J.Y. Beaucamp 92 , P.H. Beauchemin 164 , P. Bechtle 25 ,
H.P. Beck 20,p , K. Becker 173 , A.J. Beddall 82 , V.A. Bednyakov 39 , C.P. Bee 151 ,
L.J. Beemster 16 , M. Begalli 83d , M. Begel 30 , J.K. Behr 48 , J.F. Beirer 37 , F. Beisiegel 25 ,
M. Belfkir 119b , G. Bella 157 , L. Bellagamba 24b , A. Bellerive 35 , C.D. Bellgraph 68 ,
P. Bellos 21 , K. Beloborodov 38 , D. Benchekroun 36a , F. Bendebba 36a , Y. Benhammou 157 ,

28

## PDF page 29

K.C. Benkendorfer 61 , L. Beresford 48 , M. Beretta 53 , E. Bergeaas Kuutmann 167 , N. Berger 4 ,
B. Bergmann 135 , J. Beringer 18a , G. Bernardi 5 , C. Bernius 149 , F.U. Bernlochner 25 ,
F. Bernon 37 , A. Berrocal Guardia 13 , T. Berry 97 , P. Berta 136 , A. Berthold 50 , A. Berti133a ,
R. Bertrand 104 , S. Bethke 112 , A. Betti 75a,75b , A.J. Bevan 96 , L. Bezio 56 , N.K. Bhalla 54 ,
S. Bharthuar 112 , S. Bhatta 151 , P. Bhattarai 149 , Z.M. Bhatti 120 , K.D. Bhide 54 ,
V.S. Bhopatkar 124 , R.M. Bianchi 132 , G. Bianco 24b,24a , O. Biebel 111 , M. Biglietti 77a ,
C.S. Billingsley45 , Y. Bimgdi 36f , M. Bindi 55 , A. Bingham 177 , A. Bingul 22b , C. Bini 75a,75b ,
G.A. Bird 33 , M. Birman 175 , M. Biros 136 , S. Biryukov 152 , T. Bisanz 49 , E. Bisceglie 24b,24a ,
J.P. Biswal 137 , D. Biswas 147 , I. Bloch 48 , A. Blue 59 , U. Blumenschein 96 , J. Blumenthal 102 ,
V.S. Bobrovnikov 39 , L. Boccardo 57b,57a , M. Boehler 54 , B. Boehm 172 , D. Bogavac 13 ,
A.G. Bogdanchikov 38 , L.S. Boggia 130 , V. Boisvert 97 , P. Bokan 37 , T. Bold 86a , M. Bomben 5 ,
M. Bona 96 , M. Boonekamp 138 , A.G. Borbély 59 , I.S. Bordulev 38 , G. Borissov 93 ,
D. Bortoletto 129 , D. Boscherini 24b , M. Bosman 13 , K. Bouaouda 36a , N. Bouchhar 169 ,
L. Boudet 4 , J. Boudreau 132 , E.V. Bouhova-Thacker 93 , D. Boumediene 41 , R. Bouquet 57b,57a ,
A. Boveia 122 , J. Boyd 37 , D. Boye 30 , I.R. Boyko 39 , L. Bozianu 56 , J. Bracinik 21 ,
N. Brahimi 4 , G. Brandt 177 , O. Brandt 33 , B. Brau 105 , J.E. Brau 126 , R. Brener 175 ,
L. Brenner 117 , R. Brenner 167 , S. Bressler 175 , G. Brianti 78a,78b , D. Britton 59 , D. Britzger 112 ,
I. Brock 25 , R. Brock 109 , G. Brooĳmans 42 , A.J. Brooks68 , E.M. Brooks 162b , E. Brost 30 ,
L.M. Brown 171,162a , L.E. Bruce 61 , T.L. Bruckler 129 , P.A. Bruckman de Renstrom 87 ,
B. Brüers 48 , A. Bruni 24b , G. Bruni 24b , D. Brunner 47a,47b , M. Bruschi 24b , N. Bruscino 75a,75b ,
T. Buanes 17 , Q. Buat 142 , D. Buchin 112 , A.G. Buckley 59 , O. Bulekov 82 , B.A. Bullard 149 ,
S. Burdin 94 , C.D. Burgard 49 , A.M. Burger 91 , B. Burghgrave 8 , O. Burlayenko 54 ,
J. Burleson 168 , J.C. Burzynski 148 , E.L. Busch 42 , V. Büscher 102 , P.J. Bussey 59 ,
J.M. Butler 26 , C.M. Buttar 59 , J.M. Butterworth 98 , W. Buttinger 137 , C.J. Buxo Vazquez 109 ,
A.R. Buzykaev 39 , S. Cabrera Urbán 169 , L. Cadamuro 66 , D. Caforio 58 , H. Cai 132 ,
Y. Cai 24b,114c,24a , Y. Cai 114a , V.M.M. Cairo 37 , O. Cakir 3a , N. Calace 37 , P. Calafiura 18a ,
G. Calderini 130 , P. Calfayan 35 , G. Callea 59 , L.P. Caloba83b , D. Calvet 41 , S. Calvet 41 ,
R. Camacho Toro 130 , S. Camarda 37 , D. Camarero Munoz 27 , P. Camarri 76a,76b ,
C. Camincher 171 , M. Campanelli 98 , A. Camplani 43 , V. Canale 72a,72b , A.C. Canbay 3a ,
E. Canonero 97 , J. Cantero 169 , Y. Cao 168 , F. Capocasa 27 , M. Capua 44b,44a , A. Carbone 71a,71b ,
R. Cardarelli 76a , J.C.J. Cardenas 8 , M.P. Cardiff 27 , G. Carducci 44b,44a , T. Carli 37 ,
G. Carlino 72a , J.I. Carlotto 13 , B.T. Carlson 132,r , E.M. Carlson 171 , J. Carmignani 94 ,
L. Carminati 71a,71b , A. Carnelli 4 , M. Carnesale 37 , S. Caron 116 , E. Carquin 140g , I.B. Carr 107 ,
S. Carrá 73a,73b , G. Carratta 24b,24a , A.M. Carroll 126 , M.P. Casado 13,h , P. Casolaro 72a,72b ,
M. Caspar 48 , F.L. Castillo 4 , L. Castillo Garcia 13 , V. Castillo Gimenez 169 , N.F. Castro 133a,133e ,
A. Catinaccio 37 , J.R. Catmore 128 , T. Cavaliere 4 , V. Cavaliere 30 , L.J. Caviedes Betancourt 23b ,
E. Celebi 82 , S. Cella 37 , V. Cepaitis 56 , K. Cerny 125 , A.S. Cerqueira 83a , A. Cerri 74a,74b,ak ,
L. Cerrito 76a,76b , F. Cerutti 18a , B. Cervato 71a,71b , A. Cervelli 24b , G. Cesarini 53 , S.A. Cetin 82 ,
P.M. Chabrillat 130 , R. Chakkappai 66 , S. Chakraborty 173 , J. Chan 18a , W.Y. Chan 159 ,
J.D. Chapman 33 , E. Chapon 138 , B. Chargeishvili 155b , D.G. Charlton 21 , C. Chauhan 136 ,
Y. Che 114a , S. Chekanov 6 , S.V. Chekulaev 162a , G.A. Chelkov 39,a , B. Chen 157 , B. Chen 171 ,
H. Chen 114a , H. Chen 30 , J. Chen 144a , J. Chen 148 , M. Chen 129 , S. Chen 89 , S.J. Chen 114a ,
X. Chen 144a , X. Chen 15,ag , Z. Chen 62 , C.L. Cheng 176 , H.C. Cheng 64a , S. Cheong 149 ,
A. Cheplakov 39 , E. Cherepanova 117 , R. Cherkaoui El Moursli 36e , E. Cheu 7 , K. Cheung 65 ,
L. Chevalier 138 , V. Chiarella 53 , G. Chiarelli 74a , G. Chiodini 70a , A.S. Chisholm 21 ,
A. Chitan 28b , M. Chitishvili 169 , M.V. Chizhov 39,s , K. Choi 11 , Y. Chou 142 , E.Y.S. Chow 116 ,
K.L. Chu 175 , M.C. Chu 64a , X. Chu 14,114c , Z. Chubinidze 53 , J. Chudoba 134 ,

29

## PDF page 30

J.J. Chwastowski 87 , D. Cieri 112 , K.M. Ciesla 86a , V. Cindro 95 , A. Ciocio 18a , F. Cirotto 72a,72b ,
Z.H. Citron 175 , M. Citterio 71a , D.A. Ciubotaru28b , A. Clark 56 , P.J. Clark 52 , N. Clarke Hall 98 ,
C. Clarry 161 , S.E. Clawson 48 , C. Clement 47a,47b , Y. Coadou 104 , M. Cobal 69a,69c ,
A. Coccaro 57b , R.F. Coelho Barrue 133a , R. Coelho Lopes De Sa 105 , S. Coelli 71a ,
L.S. Colangeli 161 , B. Cole 42 , P. Collado Soto 101 , J. Collot 60 , R. Coluccia70a,70b ,
P. Conde Muiño 133a,133g , M.P. Connell 34c , S.H. Connell 34c , E.I. Conroy 129 ,
M. Contreras Cossio11 , F. Conventi 72a,ai , A.M. Cooper-Sarkar 129 , L. Corazzina 75a,75b ,
F.A. Corchia 24b,24a , A. Cordeiro Oudot Choi 142 , L.D. Corpe 41 , M. Corradi 75a,75b ,
F. Corriveau 106,ab , A. Cortes-Gonzalez 159 , M.J. Costa 169 , F. Costanza 4 , D. Costanzo 145 ,
B.M. Cote 122 , J. Couthures 4 , G. Cowan 97 , K. Cranmer 176 , L. Cremer 49 ,
D. Cremonini 24b,24a , S. Crépé-Renaudin 60 , F. Crescioli 130 , T. Cresta 73a,73b , M. Cristinziani 147 ,
M. Cristoforetti 78a,78b , V. Croft 117 , J.E. Crosby 124 , G. Crosetti 44b,44a , A. Cueto 101 , H. Cui 98 ,
Z. Cui 7 , B.M. Cunnett 152 , W.R. Cunningham 59 , F. Curcio 169 , J.R. Curran 52 ,
M.J. Da Cunha Sargedas De Sousa 57b,57a , J.V. Da Fonseca Pinto 83b , C. Da Via 103 ,
W. Dabrowski 86a , T. Dado 37 , S. Dahbi 154 , T. Dai 108 , D. Dal Santo 20 , C. Dallapiccola 105 ,
M. Dam 43 , G. D’amen 30 , V. D’Amico 111 , J. Damp 102 , J.R. Dandoy 35 , D. Dannheim 37 ,
G. D’anniballe 74a,74b , M. Danninger 148 , V. Dao 151 , G. Darbo 57b , S.J. Das 30 , F. Dattola 48 ,
S. D’Auria 71a,71b , A. D’Avanzo 72a,72b , T. Davidek 136 , J. Davidson 173 , I. Dawson 96 , K. De 8 ,
C. De Almeida Rossi 161 , R. De Asmundis 72a , N. De Biase 48 , S. De Castro 24b,24a ,
N. De Groot 116 , P. de Jong 117 , H. De la Torre 118 , A. De Maria 114a , A. De Salvo 75a ,
U. De Sanctis 76a,76b , F. De Santis 70a,70b , A. De Santo 152 , J.B. De Vivie De Regie 60 ,
J. Debevc 95 , D.V. Dedovich39 , J. Degens 94 , A.M. Deiana 45 , J. Del Peso 101 , L. Delagrange 130 ,
F. Deliot 138 , C.M. Delitzsch 49 , M. Della Pietra 72a,72b , D. Della Volpe 56 , A. Dell’Acqua 37 ,
L. Dell’Asta 71a,71b , M. Delmastro 4 , C.C. Delogu 102 , P.A. Delsart 60 , S. Demers 178 ,
M. Demichev 39 , S.P. Denisov 38 , H. Denizli 22a,l , L. D’Eramo 41 , D. Derendarz 87 ,
F. Derue 130 , P. Dervan 94 , A.M. Desai 1 , K. Desch 25 , F.A. Di Bello 57b,57a ,
A. Di Ciaccio 76a,76b , L. Di Ciaccio 4 , A. Di Domenico 75a,75b , C. Di Donato 72a,72b ,
A. Di Girolamo 37 , G. Di Gregorio 37 , A. Di Luca 78a,78b , B. Di Micco 77a,77b , R. Di Nardo 77a,77b ,
K.F. Di Petrillo 40 , M. Diamantopoulou 35 , F.A. Dias 117 , M.A. Diaz 140a,140b , A.R. Didenko 39 ,
M. Didenko 169 , S.D. Diefenbacher 18a , E.B. Diehl 108 , S. Díez Cornell 48 , C. Diez Pardos 147 ,
C. Dimitriadi 150 , A. Dimitrievska 21 , A. Dimri 151 , Y. Ding62 , J. Dingfelder 25 , T. Dingley 129 ,
I-M. Dinu 28b , S.J. Dittmeier 63b , F. Dittus 37 , M. Divisek 136 , B. Dixit 94 , F. Djama 104 ,
T. Djobava 155b , C. Doglioni 103,100 , A. Dohnalova 29a , Z. Dolezal 136 , K. Domĳan 86a ,
K.M. Dona 40 , M. Donadelli 83d , B. Dong 109 , J. Donini 41 , A. D’Onofrio 72a,72b ,
M. D’Onofrio 94 , J. Dopke 137 , A. Doria 72a , N. Dos Santos Fernandes 133a , P. Dougan 103 ,
M.T. Dova 92 , A.T. Doyle 59 , M.A. Draguet 129 , M.P. Drescher 55 , E. Dreyer 175 ,
I. Drivas-koulouris 10 , M. Drnevich 120 , M. Drozdova 56 , D. Du 62 , T.A. du Pree 117 , Z. Duan114a ,
M. Dubau 4 , F. Dubinin 39 , M. Dubovsky 29a , E. Duchovni 175 , G. Duckeck 111 , P.K. Duckett98 ,
O.A. Ducu 28b , D. Duda 52 , A. Dudarev 37 , E.R. Duden 27 , M. D’uffizi 103 , L. Duflot 66 ,
M. Dührssen 37 , I. Duminica 28g , A.E. Dumitriu 28b , M. Dunford 63a , S. Dungs 49 ,
K. Dunne 47a,47b , A. Duperrin 104 , H. Duran Yildiz 3a , M. Düren 58 , A. Durglishvili 155b ,
D. Duvnjak 35 , G.I. Dyckes 18a , M. Dyndal 86a , B.S. Dziedzic 37 , Z.O. Earnshaw 152 ,
G.H. Eberwein 129 , B. Eckerova 29a , S. Eggebrecht 55 , E. Egidio Purcino De Souza 83e ,
G. Eigen 17 , K. Einsweiler 18a , T. Ekelof 167 , P.A. Ekman 100 , S. El Farkh 36b , Y. El Ghazali 62 ,
H. El Jarrari 37 , A. El Moussaouy 36a , V. Ellajosyula 167 , M. Ellert 167 , F. Ellinghaus 177 ,
T.A. Elliot 97 , N. Ellis 37 , J. Elmsheuser 30 , M. Elsawy 119a , M. Elsing 37 , D. Emeliyanov 137 ,
Y. Enari 84 , I. Ene 18a , S. Epari 110 , D. Ernani Martins Neto 87 , F. Ernst37 , M. Errenst 177 ,

30

## PDF page 31

M. Escalier 66 , C. Escobar 169 , E. Etzion 157 , G. Evans 133a,133b , H. Evans 68 , L.S. Evans 97 ,
A. Ezhilov 38 , S. Ezzarqtouni 36a , F. Fabbri 24b,24a , L. Fabbri 24b,24a , G. Facini 98 ,
V. Fadeyev 139 , R.M. Fakhrutdinov 38 , D. Fakoudis 102 , S. Falciano 75a ,
L.F. Falda Ulhoa Coelho 133a , F. Fallavollita 112 , G. Falsetti 44b,44a , J. Faltova 136 , C. Fan 168 ,
K.Y. Fan 64b , Y. Fan 14 , Y. Fang 14,114c , M. Fanti 71a,71b , M. Faraj 69a,69b , Z. Farazpay 99 ,
A. Farbin 8 , A. Farilla 77a , T. Farooque 109 , J.N. Farr 178 , S.M. Farrington 137,52 , F. Fassi 36e ,
D. Fassouliotis 9 , L. Fayard 66 , P. Federic 136 , P. Federicova 134 , O.L. Fedin 38,a , M. Feickert 176 ,
L. Feligioni 104 , D.E. Fellers 18a , C. Feng 143a , Z. Feng 117 , M.J. Fenton 165 , L. Ferencz 48 ,
B. Fernandez Barbadillo 93 , P. Fernandez Martinez 67 , M.J.V. Fernoux 104 , J. Ferrando 93 ,
A. Ferrari 167 , P. Ferrari 117,116 , R. Ferrari 73a , D. Ferrere 56 , C. Ferretti 108 , M.P. Fewell 1 ,
D. Fiacco 75a,75b , F. Fiedler 102 , P. Fiedler 135 , S. Filimonov 39 , M.S. Filip 28b,t , A. Filipčič 95 ,
E.K. Filmer 162a , F. Filthaut 116 , M.C.N. Fiolhais 133a,133c,c , L. Fiorini 169 , W.C. Fisher 109 ,
T. Fitschen 103 , P.M. Fitzhugh138 , I. Fleck 147 , P. Fleischmann 108 , T. Flick 177 , M. Flores 34d,af ,
L.R. Flores Castillo 64a , L. Flores Sanz De Acedo 37 , F.M. Follega 78a,78b , N. Fomin 33 ,
J.H. Foo 161 , A. Formica 138 , A.C. Forti 103 , E. Fortin 37 , A.W. Fortman 18a , L. Foster 18a ,
L. Fountas 9,i , D. Fournier 66 , H. Fox 93 , P. Francavilla 74a,74b , S. Francescato 61 ,
S. Franchellucci 56 , M. Franchini 24b,24a , S. Franchino 63a , D. Francis37 , L. Franco 116 ,
V. Franco Lima 37 , L. Franconi 48 , M. Franklin 61 , G. Frattari 27 , Y.Y. Frid 157 , J. Friend 59 ,
N. Fritzsche 37 , A. Froch 56 , D. Froidevaux 37 , J.A. Frost 129 , Y. Fu 109 ,
S. Fuenzalida Garrido 140g , M. Fujimoto 104 , K.Y. Fung 64a , E. Furtado De Simas Filho 83e ,
M. Furukawa 159 , J. Fuster 169 , A. Gaa 55 , A. Gabrielli 24b,24a , A. Gabrielli 161 , P. Gadow 37 ,
G. Gagliardi 57b,57a , L.G. Gagnon 18a , S. Gaid 88b , S. Galantzan 157 , J. Gallagher 1 ,
E.J. Gallas 129 , A.L. Gallen 167 , B.J. Gallop 137 , K.K. Gan 122 , S. Ganguly 159 , Y. Gao 52 ,
A. Garabaglu 142 , F.M. Garay Walls 140a,140b , C. García 169 , A. Garcia Alonso 117 ,
A.G. Garcia Caffaro 178 , J.E. García Navarro 169 , M.A. Garcia Ruiz 23b , M. Garcia-Sciveres 18a ,
G.L. Gardner 131 , R.W. Gardner 40 , N. Garelli 164 , R.B. Garg 149 , J.M. Gargan 52 , C.A. Garner161 ,
C.M. Garvey 34a , V.K. Gassmann164 , G. Gaudio 73a , V. Gautam13 , P. Gauzzi 75a,75b ,
J. Gavranovic 95 , I.L. Gavrilenko 133a , A. Gavrilyuk 38 , C. Gay 170 , G. Gaycken 126 ,
E.N. Gazis 10 , A. Gekow122 , C. Gemme 57b , M.H. Genest 60 , A.D. Gentry 115 , S. George 97 ,
T. Geralis 46 , A.A. Gerwin 123 , P. Gessinger-Befurt 37 , M.E. Geyik 177 , M. Ghani 173 ,
K. Ghorbanian 96 , A. Ghosal 147 , A. Ghosh 165 , A. Ghosh 7 , B. Giacobbe 24b , S. Giagu 75a,75b ,
T. Giani 117 , A. Giannini 62 , S.M. Gibson 97 , M. Gignac 139 , D.T. Gil 86b , A.K. Gilbert 86a ,
B.J. Gilbert 42 , D. Gillberg 35 , G. Gilles 117 , D.M. Gingrich 2,ah , M.P. Giordani 69a,69c ,
P.F. Giraud 138 , G. Giugliarelli 69a,69c , D. Giugni 71a , F. Giuli 76a,76b , I. Gkialas 9,i ,
L.K. Gladilin 38 , C. Glasman 101 , M. Glazewska 20 , R.M. Gleason 165 , G. Glemža 48 ,
M. Glisic126 , I. Gnesi 44b , Y. Go 30 , M. Goblirsch-Kolb 37 , B. Gocke 49 , D. Godin110 ,
B. Gokturk 22a , S. Goldfarb 107 , T. Golling 56 , M.G.D. Gololo 34c , D. Golubkov 38 ,
J.P. Gombas 109 , A. Gomes 133a,133b , G. Gomes Da Silva 147 , A.J. Gomez Delegido 169 ,
R. Gonçalo 133a , L. Gonella 21 , A. Gongadze 155c , F. Gonnella 21 , J.L. Gonski 149 ,
R.Y. González Andana 52 , S. González de la Hoz 169 , M.V. Gonzalez Rodrigues 48 ,
R. Gonzalez Suarez 167 , S. Gonzalez-Sevilla 56 , L. Goossens 37 , B. Gorini 37 , E. Gorini 70a,70b ,
A. Gorišek 95 , T.C. Gosart 131 , A.T. Goshaw 51 , M.I. Gostkin 39 , S. Goswami 124 ,
C.A. Gottardo 37 , S.A. Gotz 111 , M. Gouighri 36b , A.G. Goussiou 142 , N. Govender 34c ,
R.P. Grabarczyk 129 , I. Grabowska-Bold 86a , K. Graham 35 , E. Gramstad 128 ,
S. Grancagnolo 70a,70b , C.M. Grant1 , P.M. Gravila 28f , F.G. Gravili 70a,70b , H.M. Gray 18a ,
M. Greco 112 , M.J. Green 1 , C. Grefe 25 , A.S. Grefsrud 17 , I.M. Gregor 48 , K.T. Greif 165 ,
P. Grenier 149 , S.G. Grewe112 , A.A. Grillo 139 , K. Grimm 32 , S. Grinstein 13,x , J.-F. Grivaz 66 ,

31

## PDF page 32

E. Gross 175 , J. Grosse-Knetter 55 , L. Guan 108 , G. Guerrieri 37 , R. Guevara 128 , R. Gugel 102 ,
J.A.M. Guhit 108 , A. Guida 19 , E. Guilloton 173 , S. Guindon 37 , F. Guo 14,114c , J. Guo 144a ,
L. Guo 48 , L. Guo 114b,v , Y. Guo 108 , A. Gupta 49 , R. Gupta 132 , S. Gupta 27 , S. Gurbuz 25 ,
S.S. Gurdasani 48 , G. Gustavino 75a,75b , P. Gutierrez 123 , L.F. Gutierrez Zagazeta 131 ,
M. Gutsche 50 , C. Gutschow 98 , C. Gwenlan 129 , C.B. Gwilliam 94 , E.S. Haaland 128 ,
A. Haas 120 , M. Habedank 59 , C. Haber 18a , H.K. Hadavand 8 , A. Haddad 41 , A. Hadef 50 ,
A.I. Hagan 93 , J.J. Hahn 147 , E.H. Haines 98 , M. Haleem 172 , J. Haley 124 , G.D. Hallewell 104 ,
L. Halser 20 , K. Hamano 171 , H. Hamdaoui 167 , M. Hamer 25 , S.E.D. Hammoud 66 ,
E.J. Hampshire 97 , J. Han 143a , L. Han 114a , L. Han 62 , S. Han 14 , K. Hanagaki 84 ,
M. Hance 139 , D.A. Hangal 42 , H. Hanif 148 , M.D. Hank 131 , J.B. Hansen 43 , P.H. Hansen 43 ,
D. Harada 56 , T. Harenberg 177 , S. Harkusha 179 , M.L. Harris 105 , Y.T. Harris 25 , J. Harrison 13 ,
N.M. Harrison 122 , P.F. Harrison173 , M.L.E. Hart 98 , N.M. Hartman 112 , N.M. Hartmann 111 ,
R.Z. Hasan 97,137 , Y. Hasegawa 146 , F. Haslbeck 129 , S. Hassan 17 , R. Hauser 109 ,
M. Haviernik 136 , C.M. Hawkes 21 , R.J. Hawkings 37 , Y. Hayashi 159 , D. Hayden 109 ,
C. Hayes 108 , R.L. Hayes 117 , C.P. Hays 129 , J.M. Hays 96 , H.S. Hayward 94 , M. He 14,114c ,
Y. He 48 , Y. He 98 , N.B. Heatley 96 , V. Hedberg 100 , C. Heidegger 54 , K.K. Heidegger 54 ,
J. Heilman 35 , S. Heim 48 , T. Heim 18a , J.G. Heinlein 131 , J.J. Heinrich 126 , L. Heinrich 112 ,
J. Hejbal 134 , M. Helbig 50 , A. Held 176 , S. Hellesund 17 , C.M. Helling 170 , S. Hellman 47a,47b ,
A.M. Henriques Correia37 , H. Herde 100 , Y. Hernández Jiménez 151 , L.M. Herrmann 25 ,
T. Herrmann 50 , G. Herten 54 , R. Hertenberger 111 , L. Hervas 37 , M.E. Hesping 102 ,
N.P. Hessey 162a , J. Hessler 112 , M. Hidaoui 36b , N. Hidic 136 , E. Hill 161 , T.S. Hillersoy 17 ,
S.J. Hillier 21 , J.R. Hinds 109 , F. Hinterkeuser 25 , M. Hirose 127 , S. Hirose 163 ,
D. Hirschbuehl 177 , T.G. Hitchings 103 , B. Hiti 95 , J. Hobbs 151 , R. Hobincu 28e , N. Hod 175 ,
A.M. Hodges 168 , M.C. Hodgkinson 145 , B.H. Hodkinson 129 , A. Hoecker 37 , D.D. Hofer 108 ,
J. Hofer 169 , M. Holzbock 37 , L.B.A.H. Hommels 33 , V. Homsak 129 , B.P. Honan 103 ,
J.J. Hong 68 , T.M. Hong 132 , B.H. Hooberman 168 , W.H. Hopkins 6 , M.C. Hoppesch 168 ,
Y. Horii 113 , M.E. Horstmann 112 , S. Hou 154 , M.R. Housenga 168 , A.S. Howard 95 ,
J. Howarth 59 , J. Hoya 6 , M. Hrabovsky 125 , T. Hryn’ova 4 , P.J. Hsu 65 , S.-C. Hsu 142 ,
T. Hsu 66 , M. Hu 18a , Q. Hu 62 , S. Huang 33 , X. Huang 14,114c , Y. Huang 136 , Y. Huang 114b ,
Y. Huang 102 , Y. Huang 14 , Z. Huang 66 , Z. Hubacek 135 , M. Huebner 25 , F. Huegging 25 ,
T.B. Huffman 129 , M. Hufnagel Maranha De Faria 83a , C.A. Hugli 48 , M. Huhtinen 37 ,
S.K. Huiberts 17 , R. Hulsken 106 , C.E. Hultquist 18a , D.L. Humphreys 105 , N. Huseynov 12 ,
J. Huston 109 , J. Huth 61 , R. Hyneman 7 , G. Iacobucci 56 , G. Iakovidis 30 ,
L. Iconomidou-Fayard 66 , J.P. Iddon 37 , P. Iengo 72a,72b , R. Iguchi 159 , Y. Iiyama 159 ,
T. Iizawa 159 , Y. Ikegami 84 , D. Iliadis 158 , N. Ilic 161 , H. Imam 36a , G. Inacio Goncalves 83d ,
S.A. Infante Cabanas 140c , T. Ingebretsen Carlson 47a,47b , J.M. Inglis 96 , G. Introzzi 73a,73b ,
M. Iodice 77a , V. Ippolito 75a,75b , R.K. Irwin 94 , M. Ishino 159 , W. Islam 176 , C. Issever 19 ,
S. Istin 22a,am , K. Itabashi 84 , H. Ito 174 , R. Iuppa 78a,78b , A. Ivina 175 , V. Izzo 72a , P. Jacka 135 ,
P. Jackson 1 , P. Jain 48 , K. Jakobs 54 , T. Jakoubek 175 , J. Jamieson 59 , W. Jang 159 ,
S. Jankovych 136 , M. Javurkova 105 , P. Jawahar 103 , L. Jeanty 126 , J. Jejelava 155a,ae , P. Jenni 54,f ,
C.E. Jessiman 35 , C. Jia 143a , H. Jia 170 , J. Jia 151 , X. Jia 14,114c , Z. Jia 114a , C. Jiang 52 ,
Q. Jiang 64b , S. Jiggins 48 , M. Jimenez Ortega 169 , J. Jimenez Pena 13 , S. Jin 114a , A. Jinaru 28b ,
O. Jinnouchi 141 , P. Johansson 145 , K.A. Johns 7 , J.W. Johnson 139 , F.A. Jolly 48 ,
D.M. Jones 152 , E. Jones 48 , K.S. Jones8 , P. Jones 33 , R.W.L. Jones 93 , T.J. Jones 94 ,
H.L. Joos 55,37 , R. Joshi 122 , J. Jovicevic 16 , X. Ju 18a , J.J. Junggeburth 37 , T. Junkermann 63a ,
A. Juste Rozas 13,x , M.K. Juzek 87 , S. Kabana 140f , A. Kaczmarska 87 , M. Kado 112 ,
H. Kagan 122 , M. Kagan 149 , A. Kahn 131 , C. Kahra 102 , T. Kaji 159 , E. Kajomovitz 156 ,

32

## PDF page 33

N. Kakati 175 , N. Kakoty 13 , I. Kalaitzidou 54 , S. Kandel 8 , N.J. Kang 139 , D. Kar 34h ,
K. Karava 129 , E. Karentzos 25 , O. Karkout 117 , S.N. Karpov 39 , Z.M. Karpova 39 ,
V. Kartvelishvili 93 , A.N. Karyukhin 38 , E. Kasimi 158 , J. Katzy 48 , S. Kaur 35 , K. Kawade 146 ,
M.P. Kawale 123 , C. Kawamoto 89 , T. Kawamoto 62 , E.F. Kay 37 , F.I. Kaya 164 , S. Kazakos 109 ,
V.F. Kazanin 38 , J.M. Keaveney 34a , R. Keeler 171 , G.V. Kehris 61 , J.S. Keller 35 ,
J.J. Kempster 152 , O. Kepka 134 , J. Kerr 162b , B.P. Kerridge 137 , B.P. Kerševan 95 ,
L. Keszeghova 29a , R.A. Khan 132 , A. Khanov 124 , A.G. Kharlamov 38 , T. Kharlamova 38 ,
E.E. Khoda 142 , M. Kholodenko 133a , T.J. Khoo 19 , G. Khoriauli 172 , Y. Khoulaki 36a ,
J. Khubua 155b,* , Y.A.R. Khwaira 130 , B. Kibirige34h , D. Kim 6 , D.W. Kim 47a,47b , Y.K. Kim 40 ,
N. Kimura 98 , M.K. Kingston 55 , A. Kirchhoff 55 , C. Kirfel 25 , F. Kirfel 25 , J. Kirk 137 ,
A.E. Kiryunin 112 , S. Kita 163 , O. Kivernyk 25 , M. Klassen 164 , C. Klein 35 , L. Klein 172 ,
M.H. Klein 45 , S.B. Klein 56 , U. Klein 94 , A. Klimentov 30 , T. Klioutchnikova 37 , P. Kluit 117 ,
S. Kluth 112 , E. Kneringer 79 , T.M. Knight 161 , A. Knue 49 , M. Kobel 50 , D. Kobylianskii 175 ,
S.F. Koch 129 , M. Kocian 149 , P. Kodyš 136 , D.M. Koeck 126 , T. Koffas 35 , O. Kolay 50 ,
I. Koletsou 4 , T. Komarek 87 , K. Köneke 55 , A.X.Y. Kong 1 , T. Kono 121 , N. Konstantinidis 98 ,
P. Kontaxakis 56 , B. Konya 100 , R. Kopeliansky 42 , S. Koperny 86a , K. Korcyl 87 ,
K. Kordas 158,d , A. Korn 98 , S. Korn 55 , I. Korolkov 13 , N. Korotkova 38 , B. Kortman 117 ,
O. Kortner 112 , S. Kortner 112 , W.H. Kostecka 118 , M. Kostov 29a , V.V. Kostyukhin 147 ,
A. Kotsokechagia 37 , A. Kotwal 51 , A. Koulouris 37 , A. Kourkoumeli-Charalampidi 73a,73b ,
C. Kourkoumelis 9 , E. Kourlitis 112 , O. Kovanda 126 , R. Kowalewski 171 , W. Kozanecki 126 ,
A.S. Kozhin 38 , V.A. Kramarenko 38 , G. Kramberger 95 , P. Kramer 25 , M.W. Krasny 130 ,
A. Krasznahorkay 105 , A.C. Kraus 118 , J.W. Kraus 177 , J.A. Kremer 48 , N.B. Krengel 147 ,
T. Kresse 50 , L. Kretschmann 177 , J. Kretzschmar 94 , P. Krieger 161 , K. Krizka 21 ,
K. Kroeninger 49 , H. Kroha 112 , J. Kroll 134 , J. Kroll 131 , K.S. Krowpman 109 , U. Kruchonak 39 ,
H. Krüger 25 , N. Krumnack81 , M.C. Kruse 51 , O. Kuchinskaia 39 , S. Kuday 3a , S. Kuehn 37 ,
R. Kuesters 54 , T. Kuhl 48 , V. Kukhtin 39 , Y. Kulchitsky 39 , S. Kuleshov 140d,140b , J. Kull 1 ,
E.V. Kumar 111 , M. Kumar 34h , N. Kumari 48 , P. Kumari 162b , A. Kupco 134 , T. Kupfer49 ,
A. Kupich 38 , O. Kuprash 54 , H. Kurashige 85 , L.L. Kurchaninov 162a , O. Kurdysh 4 ,
Y.A. Kurochkin 38 , A. Kurova 38 , M. Kuze 141 , A.K. Kvam 105 , J. Kvita 125 , N.G. Kyriacou 108 ,
C. Lacasta 169 , F. Lacava 75a,75b , H. Lacker 19 , D. Lacour 130 , N.N. Lad 98 , E. Ladygin 39 ,
A. Lafarge 41 , B. Laforge 130 , T. Lagouri 178 , F.Z. Lahbabi 36a , S. Lai 55 , J.E. Lambert 171 ,
S. Lammers 68 , W. Lampl 7 , C. Lampoudis 158,d , G. Lamprinoudis 102 , A.N. Lancaster 118 ,
E. Lançon 30 , U. Landgraf 54 , M.P.J. Landon 96 , V.S. Lang 54 , O.K.B. Langrekken 128 ,
A.J. Lankford 165 , F. Lanni 37 , K. Lantzsch 25 , A. Lanza 73a , M. Lanzac Berrocal 169 ,
J.F. Laporte 138 , T. Lari 71a , D. Larsen 17 , L. Larson 11 , F. Lasagni Manghi 24b , M. Lassnig 37 ,
S.D. Lawlor 145 , R. Lazaridou173 , M. Lazzaroni 71a,71b , H.D.M. Le 109 , E.M. Le Boulicaut 178 ,
L.T. Le Pottier 18a , B. Leban 24b,24a , F. Ledroit-Guillon 60 , T.F. Lee 162b , L.L. Leeuw 34c ,
M. Lefebvre 171 , C. Leggett 18a , G. Lehmann Miotto 37 , M. Leigh 56 , W.A. Leight 105 ,
W. Leinonen 116 , A. Leisos 158,u , M.A.L. Leite 83c , C.E. Leitgeb 19 , R. Leitner 136 ,
K.J.C. Leney 45 , T. Lenz 25 , S. Leone 74a , C. Leonidopoulos 52 , A. Leopold 150 ,
J.H. Lepage Bourbonnais 35 , R. Les 109 , C.G. Lester 33 , M. Levchenko 38 , J. Levêque 4 ,
L.J. Levinson 175 , G. Levrini 24b,24a , M.P. Lewicki 87 , C. Lewis 142 , D.J. Lewis 4 , L. Lewitt 145 ,
A. Li 30 , B. Li 143a , C. Li108 , C-Q. Li 112 , H. Li 143a , H. Li 103 , H. Li 15 , H. Li62 , H. Li 143a ,
J. Li 144a , K. Li 14 , L. Li 144a , R. Li 178 , S. Li 14,114c , S. Li 144b,144a , T. Li 5 , X. Li 106 ,
Z. Li 159 , Z. Li 14,114c , Z. Li 62 , S. Liang 14,114c , Z. Liang 14 , M. Liberatore 138 , B. Liberti 76a ,
K. Lie 64c , J. Lieber Marin 83e , H. Lien 68 , H. Lin 108 , S.F. Lin 151 , L. Linden 111 ,
R.E. Lindley 7 , J.H. Lindon 37 , J. Ling 61 , E. Lipeles 131 , A. Lipniacka 17 , A. Lister 170 ,

33

## PDF page 34

J.D. Little 68 , B. Liu 14 , B.X. Liu 114b , D. Liu 144b,144a , D. Liu 139 , E.H.L. Liu 21 ,
J.K.K. Liu 120 , K. Liu 144b , K. Liu 144b,144a , M. Liu 62 , M.Y. Liu 62 , P. Liu 14 ,
Q. Liu 144b,142,144a , X. Liu 62 , X. Liu 143a , Y. Liu 114b,114c , Y.L. Liu 143a , Y.W. Liu 62 ,
Z. Liu 66,k , S.L. Lloyd 96 , E.M. Lobodzinska 48 , P. Loch 7 , E. Lodhi 161 , T. Lohse 19 ,
K. Lohwasser 145 , E. Loiacono 48 , J.D. Lomas 21 , J.D. Long 42 , I. Longarini 165 , R. Longo 168 ,
A. Lopez Solis 13 , N.A. Lopez-canelas 7 , N. Lorenzo Martinez 4 , A.M. Lory 111 , M. Losada 119a ,
G. Löschcke Centeno 152 , X. Lou 47a,47b , X. Lou 14,114c , A. Lounis 66 , P.A. Love 93 , M. Lu 66 ,
S. Lu 131 , Y.J. Lu 154 , H.J. Lubatti 142 , C. Luci 75a,75b , F.L. Lucio Alves 114a , F. Luehring 68 ,
B.S. Lunday 131 , O. Lundberg 150 , J. Lunde 37 , N.A. Luongo 6 , M.S. Lutz 37 , A.B. Lux 26 ,
D. Lynn 30 , R. Lysak 134 , V. Lysenko 135 , E. Lytken 100 , V. Lyubushkin 39 , T. Lyubushkina 39 ,
M.M. Lyukova 151 , M.Firdaus M. Soberi 52 , H. Ma 30 , K. Ma 62 , L.L. Ma 143a , W. Ma 62 ,
Y. Ma 124 , J.C. MacDonald 102 , P.C. Machado De Abreu Farias 83e , R. Madar 41 , T. Madula 98 ,
J. Maeda 85 , T. Maeno 30 , P.T. Mafa 34c,j , H. Maguire 145 , M. Maheshwari 33 , V. Maiboroda 66 ,
A. Maio 133a,133b,133d , K. Maj 86a , O. Majersky 48 , S. Majewski 126 , R. Makhmanazarov 38 ,
N. Makovec 66 , V. Maksimovic 16 , B. Malaescu 130 , J. Malamant128 , Pa. Malecki 87 ,
V.P. Maleev 38 , F. Malek 60,o , M. Mali 95 , D. Malito 97 , U. Mallik 80,* , A. Maloizel 5 ,
S. Maltezos10 , A. Malvezzi Lopes 83d , S. Malyukov39 , J. Mamuzic 13 , G. Mancini 53 ,
M.N. Mancini 27 , G. Manco 73a,73b , J.P. Mandalia 96 , S.S. Mandarry 152 , I. Mandić 95 ,
L. Manhaes de Andrade Filho 83a , I.M. Maniatis 175 , J. Manjarres Ramos 91 , D.C. Mankad 175 ,
A. Mann 111 , T. Manoussos 37 , M.N. Mantinan 40 , S. Manzoni 37 , L. Mao 144a , X. Mapekula 34c ,
A. Marantis 158 , R.R. Marcelo Gregorio 96 , G. Marchiori 5 , M. Marcisovsky 134 , C. Marcon 71a ,
E. Maricic 16 , M. Marinescu 48 , S. Marium 48 , M. Marjanovic 123 , A. Markhoos 54 ,
M. Markovitch 66 , M.K. Maroun 105 , G.T. Marsden103 , E.J. Marshall 93 , Z. Marshall 18a ,
S. Marti-Garcia 169 , J. Martin 98 , T.A. Martin 137 , V.J. Martin 52 , B. Martin dit Latour 17 ,
L. Martinelli 75a,75b , M. Martinez 13,x , P. Martinez Agullo 169 , V.I. Martinez Outschoorn 105 ,
P. Martinez Suarez 13 , S. Martin-Haugh 137 , G. Martinovicova 136 , V.S. Martoiu 28b ,
A.C. Martyniuk 98 , A. Marzin 37 , D. Mascione 78a,78b , L. Masetti 102 , J. Masik 103 ,
A.L. Maslennikov 39 , S.L. Mason 42 , P. Massarotti 72a,72b , P. Mastrandrea 74a,74b ,
A. Mastroberardino 44b,44a , T. Masubuchi 127 , T.T. Mathew 126 , J. Matousek 136 , D.M. Mattern 49 ,
J. Maurer 28b , T. Maurin 59 , A.J. Maury 66 , B. Maček 95 , C. Mavungu Tsava 104 ,
D.A. Maximov 38 , A.E. May 103 , E. Mayer 41 , R. Mazini 34h , I. Maznas 118 , S.M. Mazza 139 ,
E. Mazzeo 37 , J.P. Mc Gowan 171 , S.P. Mc Kee 108 , C.A. Mc Lean 6 , C.C. McCracken 170 ,
E.F. McDonald 107 , A.E. McDougall 117 , L.F. Mcelhinney 93 , J.A. Mcfayden 152 ,
R.P. McGovern 131 , R.P. Mckenzie 34h , T.C. Mclachlan 48 , D.J. Mclaughlin 98 , S.J. McMahon 137 ,
C.M. Mcpartland 94 , R.A. McPherson 171,ab , S. Mehlhase 111 , A. Mehta 94 , D. Melini 169 ,
B.R. Mellado Garcia 34h , A.H. Melo 55 , F. Meloni 48 , A.M. Mendes Jacques Da Costa 103 ,
L. Meng 93 , S. Menke 112 , M. Mentink 37 , E. Meoni 44b,44a , G. Mercado 118 , S. Merianos 158 ,
C. Merlassino 69a,69c , C. Meroni 71a,71b , J. Metcalfe 6 , A.S. Mete 6 , E. Meuser 102 , C. Meyer 68 ,
J-P. Meyer 138 , Y. Miao114a , R.P. Middleton 137 , M. Mihovilovic 66 , L. Mĳović 52 ,
G. Mikenberg 175 , M. Mikestikova 134 , M. Mikuž 95 , H. Mildner 102 , A. Milic 37 ,
D.W. Miller 40 , E.H. Miller 149 , L.S. Miller 35 , A. Milov 175 , D.A. Milstead47a,47b , T. Min114a ,
A.A. Minaenko 38 , I.A. Minashvili 155b , A.I. Mincer 120 , B. Mindur 86a , M. Mineev 39 ,
Y. Mino 89 , L.M. Mir 13 , M. Miralles Lopez 59 , M. Mironova 18a , M.C. Missio 116 , A. Mitra 173 ,
V.A. Mitsou 169 , Y. Mitsumori 113 , O. Miu 161 , P.S. Miyagawa 96 , T. Mkrtchyan 63a ,
M. Mlinarevic 98 , T. Mlinarevic 98 , M. Mlynarikova 37 , S. Mobius 20 , M.H. Mohamed Farook 115 ,
S. Mohapatra 42 , S. Mohiuddin 124 , G. Mokgatitswane 34h , L. Moleri 175 , U. Molinatti 129 ,
L.G. Mollier 20 , B. Mondal 134 , S. Mondal 135 , K. Mönig 48 , E. Monnier 104 ,

34

## PDF page 35

L. Monsonis Romero169 , J. Montejo Berlingen 13 , A. Montella 47a,47b , M. Montella 122 ,
F. Montereali 77a,77b , F. Monticelli 92 , S. Monzani 69a,69c , A. Morancho Tarda 43 , N. Morange 66 ,
A.L. Moreira De Carvalho 48 , M. Moreno Llácer 169 , C. Moreno Martinez 56 , J.M. Moreno Perez23b ,
P. Morettini 57b , S. Morgenstern 37 , M. Morii 61 , M. Morinaga 159 , M. Moritsu 90 ,
F. Morodei 75a,75b , P. Moschovakos 37 , B. Moser 54 , M. Mosidze 155b , T. Moskalets 45 ,
P. Moskvitina 116 , J. Moss 32 , P. Moszkowicz 86a , A. Moussa 36d , Y. Moyal 175 ,
H. Moyano Gomez 13 , E.J.W. Moyse 105 , T.G. Mroz 87 , O. Mtintsilana 34h , S. Muanza 104 ,
M. Mucha25 , J. Mueller 132 , R. Müller 37 , G.A. Mullier 167 , A.J. Mullin33 , J.J. Mullin51 ,
A.C. Mullins45 , A.E. Mulski 61 , D.P. Mungo 161 , D. Munoz Perez 169 , F.J. Munoz Sanchez 103 ,
W.J. Murray 173,137 , M. Muškinja 95 , C. Mwewa 48 , A.G. Myagkov 38,a , A.J. Myers 8 ,
G. Myers 108 , M. Myska 135 , B.P. Nachman 18a , K. Nagai 129 , K. Nagano 84 , R. Nagasaka159 ,
J.L. Nagle 30,aj , E. Nagy 104 , A.M. Nairz 37 , Y. Nakahama 84 , K. Nakamura 84 , K. Nakkalil 5 ,
A. Nandi 63b , H. Nanjo 127 , E.A. Narayanan 45 , Y. Narukawa 159 , I. Naryshkin 38 ,
L. Nasella 71a,71b , S. Nasri 119b , C. Nass 25 , G. Navarro 23a , J. Navarro-Gonzalez 169 ,
A. Nayaz 19 , P.Y. Nechaeva 38 , S. Nechaeva 24b,24a , F. Nechansky 134 , L. Nedic 129 , T.J. Neep 21 ,
A. Negri 73a,73b , M. Negrini 24b , C. Nellist 117 , C. Nelson 106 , K. Nelson 108 , S. Nemecek 134 ,
M. Nessi 37,g , M.S. Neubauer 168 , J. Newell 94 , P.R. Newman 21 , Y.W.Y. Ng 168 , B. Ngair 119a ,
H.D.N. Nguyen 110 , J.D. Nichols 123 , R.B. Nickerson 129 , R. Nicolaidou 138 , J. Nielsen 139 ,
M. Niemeyer 55 , J. Niermann 37 , N. Nikiforou 37 , V. Nikolaenko 38,a , I. Nikolic-Audit 130 ,
P. Nilsson 30 , I. Ninca 48 , G. Ninio 157 , A. Nisati 75a , R. Nisius 112 , N. Nitika 69a,69c ,
J-E. Nitschke 50 , E.K. Nkadimeng 34b , T. Nobe 159 , T. Nommensen 153 , M.B. Norfolk 145 ,
B.J. Norman 35 , M. Noury 36a , J. Novak 95 , T. Novak 95 , R. Novotny 135 , L. Nozka 125 ,
K. Ntekas 165 , N.M.J. Nunes De Moura Junior 83b , J. Ocariz 130 , A. Ochi 85 , I. Ochoa 133a ,
S. Oerdek 48,y , J.T. Offermann 40 , A. Ogrodnik 136 , A. Oh 103 , C.C. Ohm 150 , H. Oide 84 ,
M.L. Ojeda 37 , Y. Okumura 159 , L.F. Oleiro Seabra 133a , I. Oleksiyuk 56 , G. Oliveira Correa 13 ,
D. Oliveira Damazio 30 , J.L. Oliver 165 , R. Omar 68 , Ö.O. Öncel 54 , A.P. O’Neill 20 ,
A. Onofre 133a,133e,e , P.U.E. Onyisi 11 , M.J. Oreglia 40 , D. Orestano 77a,77b , R. Orlandini 77a,77b ,
R.S. Orr 161 , L.M. Osojnak 131 , Y. Osumi 113 , G. Otero y Garzon 31 , H. Otono 90 ,
M. Ouchrif 36d , F. Ould-Saada 128 , T. Ovsiannikova 142 , M. Owen 59 , R.E. Owen 137 ,
V.E. Ozcan 22a , F. Ozturk 87 , N. Ozturk 8 , S. Ozturk 82 , H.A. Pacey 129 , K. Pachal 162a ,
A. Pacheco Pages 13 , C. Padilla Aranda 13 , G. Padovano 75a,75b , S. Pagan Griso 18a ,
G. Palacino 68 , A. Palazzo 70a,70b , J. Pampel 25 , J. Pan 178 , T. Pan 64a , D.K. Panchal 11 ,
C.E. Pandini 60 , J.G. Panduro Vazquez 137 , H.D. Pandya 1 , H. Pang 138 , P. Pani 48 ,
G. Panizzo 69a,69c , L. Panwar 130 , L. Paolozzi 56 , S. Parajuli 168 , A. Paramonov 6 ,
C. Paraskevopoulos 53 , D. Paredes Hernandez 64b , A. Pareti 73a,73b , K.R. Park 42 , T.H. Park 112 ,
F. Parodi 57b,57a , J.A. Parsons 42 , U. Parzefall 54 , B. Pascual Dias 41 , L. Pascual Dominguez 101 ,
E. Pasqualucci 75a , S. Passaggio 57b , F. Pastore 97 , P. Patel 87 , U.M. Patel 51 , J.R. Pater 103 ,
T. Pauly 37 , F. Pauwels 136 , C.I. Pazos 164 , M. Pedersen 128 , R. Pedro 133a , S.V. Peleganchuk 38 ,
O. Penc 134 , E.A. Pender 52 , S. Peng 15 , G.D. Penn 178 , K.E. Penski 111 , M. Penzin 38 ,
B.S. Peralva 83d , A.P. Pereira Peixoto 142 , L. Pereira Sanchez 149 , D.V. Perepelitsa 30,aj ,
G. Perera 105 , E. Perez Codina 37 , M. Perganti 10 , H. Pernegger 37 , S. Perrella 75a,75b ,
O. Perrin 41 , K. Peters 48 , R.F.Y. Peters 103 , B.A. Petersen 37 , T.C. Petersen 43 , E. Petit 104 ,
V. Petousis 135 , A.R. Petri 71a,71b , C. Petridou 158,d , T. Petru 136 , A. Petrukhin 147 , M. Pettee 18a ,
A. Petukhov 82 , K. Petukhova 37 , R. Pezoa 140g , L. Pezzotti 24b,24a , G. Pezzullo 178 ,
L. Pfaffenbichler 37 , A.J. Pfleger 37 , T.M. Pham 176 , T. Pham 107 , P.W. Phillips 137 ,
G. Piacquadio 151 , E. Pianori 18a , F. Piazza 126 , R. Piegaia 31 , D. Pietreanu 28b ,
A.D. Pilkington 103 , M. Pinamonti 69a,69c , J.L. Pinfold 2 , G. Pinheiro Matos 42 ,

35

## PDF page 36

B.C. Pinheiro Pereira 133a , J. Pinol Bel 13 , A.E. Pinto Pinoargote 130 , L. Pintucci 69a,69c ,
K.M. Piper 152 , A. Pirttikoski 56 , D.A. Pizzi 35 , L. Pizzimento 64b , A. Plebani 33 ,
M.-A. Pleier 30 , V. Pleskot 136 , E. Plotnikova39 , G. Poddar 96 , R. Poettgen 100 , L. Poggioli 130 ,
S. Polacek 136 , G. Polesello 73a , A. Poley 148 , A. Polini 24b , C.S. Pollard 173 , Z.B. Pollock 122 ,
E. Pompa Pacchi 123 , N.I. Pond 98 , D. Ponomarenko 68 , L. Pontecorvo 37 , S. Popa 28a ,
G.A. Popeneciu 28d , A. Poreba 37 , D.M. Portillo Quintero 162a , S. Pospisil 135 , M.A. Postill 145 ,
P. Postolache 28c , K. Potamianos 173 , P.A. Potepa 86a , I.N. Potrap 39 , C.J. Potter 33 , H. Potti 153 ,
J. Poveda 169 , M.E. Pozo Astigarraga 37 , R. Pozzi 37 , A. Prades Ibanez 76a,76b , S.R. Pradhan 145 ,
J. Pretel 171 , D. Price 103 , M. Primavera 70a , L. Primomo 69a,69c , M.A. Principe Martin 101 ,
R. Privara 125 , T. Procter 86b , M.L. Proffitt 142 , N. Proklova 131 , K. Prokofiev 64c , G. Proto 112 ,
J. Proudfoot 6 , M. Przybycien 86a , W.W. Przygoda 86b , A. Psallidas 46 , J.E. Puddefoot 145 ,
D. Pudzha 53 , D. Pyatiizbyantseva 116 , J. Qian 108 , R. Qian 109 , D. Qichen 103 , Y. Qin 13 ,
T. Qiu 52 , A. Quadt 55 , M. Queitsch-Maitland 103 , G. Quetant 56 , R.P. Quinn 170 ,
G. Rabanal Bolanos 61 , D. Rafanoharana 112 , F. Raffaeli 76a,76b , F. Ragusa 71a,71b , J.L. Rainbolt 40 ,
J.A. Raine 56 , S. Rajagopalan 30 , E. Ramakoti 39 , L. Rambelli 57b,57a , I.A. Ramirez-Berend 35 ,
K. Ran 48,114c , D.S. Rankin 131 , N.P. Rapheeha 34h , H. Rasheed 28b , D.F. Rassloff 63a ,
A. Rastogi 18a , S. Rave 102 , S. Ravera 57b,57a , B. Ravina 37 , I. Ravinovich 175 , M. Raymond 37 ,
A.L. Read 128 , N.P. Readioff 145 , D.M. Rebuzzi 73a,73b , A.S. Reed 112 , K. Reeves 27 ,
J.A. Reidelsturz 177 , D. Reikher 126 , A. Rej 49 , C. Rembser 37 , H. Ren 62 , M. Renda 28b ,
F. Renner 48 , A.G. Rennie 59 , A.L. Rescia 48 , S. Resconi 71a , M. Ressegotti 57b,57a , S. Rettie 37 ,
W.F. Rettie 35 , M.M. Revering 33 , E. Reynolds 18a , O.L. Rezanova 39 , P. Reznicek 136 ,
H. Riani 36d , N. Ribaric 51 , E. Ricci 78a,78b , R. Richter 112 , S. Richter 47a,47b , E. Richter-Was 86b ,
M. Ridel 130 , S. Ridouani 36d , P. Rieck 120 , P. Riedler 37 , E.M. Riefel 47a,47b , J.O. Rieger 117 ,
M. Rĳssenbeek 151 , M. Rimoldi 37 , L. Rinaldi 24b,24a , P. Rincke 167,55 , G. Ripellino 167 ,
I. Riu 13 , J.C. Rivera Vergara 171 , F. Rizatdinova 124 , E. Rizvi 96 , B.R. Roberts 18a ,
S.S. Roberts 139 , D. Robinson 33 , M. Robles Manzano 102 , A. Robson 59 , A. Rocchi 76a,76b ,
C. Roda 74a,74b , S. Rodriguez Bosca 37 , Y. Rodriguez Garcia 23a , A.M. Rodríguez Vera 118 ,
S. Roe37 , J.T. Roemer 37 , O. Røhne 128 , R.A. Rojas 37 , C.P.A. Roland 130 , A. Romaniouk 79 ,
E. Romano 73a,73b , M. Romano 24b , A.C. Romero Hernandez 168 , N. Rompotis 94 , L. Roos 130 ,
S. Rosati 75a , B.J. Rosser 40 , E. Rossi 129 , E. Rossi 72a,72b , L.P. Rossi 61 , L. Rossini 54 ,
R. Rosten 122 , M. Rotaru 28b , B. Rottler 54 , D. Rousseau 66 , D. Rousso 48 , S. Roy-Garand 161 ,
A. Rozanov 104 , Z.M.A. Rozario 59 , Y. Rozen 156 , A. Rubio Jimenez 169 , V.H. Ruelas Rivera 19 ,
T.A. Ruggeri 1 , A. Ruggiero 129 , A. Ruiz-Martinez 169 , A. Rummler 37 , Z. Rurikova 54 ,
N.A. Rusakovich 39 , H.L. Russell 171 , G. Russo 75a,75b , J.P. Rutherfoord 7 ,
S. Rutherford Colmenares 33 , M. Rybar 136 , P. Rybczynski 86a , A. Ryzhov 45 ,
J.A. Sabater Iglesias 56 , H.F-W. Sadrozinski 139 , F. Safai Tehrani 75a , S. Saha 1 , M. Sahinsoy 82 ,
B. Sahoo 175 , A. Saibel 169 , B.T. Saifuddin 123 , M. Saimpert 138 , G.T. Saito 83c , M. Saito 159 ,
T. Saito 159 , A. Sala 71a,71b , A. Salnikov 149 , J. Salt 169 , A. Salvador Salas 157 , F. Salvatore 152 ,
A. Salzburger 37 , D. Sammel 54 , E. Sampson 93 , D. Sampsonidis 158,d , D. Sampsonidou 126 ,
J. Sánchez 169 , V. Sanchez Sebastian 169 , H. Sandaker 128 , C.O. Sander 48 , J.A. Sandesara 176 ,
M. Sandhoff 177 , C. Sandoval 23b , L. Sanfilippo 63a , D.P.C. Sankey 137 , T. Sano 89 ,
A. Sansoni 53 , M. Santana Queiroz 18b , L. Santi 37 , C. Santoni 41 , H. Santos 133a,133b ,
A. Santra 175 , E. Sanzani 24b,24a , K.A. Saoucha 88b , J.G. Saraiva 133a,133d , J. Sardain 7 ,
O. Sasaki 84 , K. Sato 163 , C. Sauer37 , E. Sauvan 4 , P. Savard 161,ah , R. Sawada 159 ,
C. Sawyer 137 , L. Sawyer 99 , C. Sbarra 24b , A. Sbrizzi 24b,24a , T. Scanlon 98 ,
J. Schaarschmidt 142 , U. Schäfer 102 , A.C. Schaffer 66,45 , D. Schaile 111 , R.D. Schamberger 151 ,
C. Scharf 19 , M.M. Schefer 20 , V.A. Schegelsky 38 , D. Scheirich 136 , M. Schernau 140f ,

36

## PDF page 37

C. Scheulen 56 , C. Schiavi 57b,57a , M. Schioppa 44b,44a , B. Schlag 149 , S. Schlenker 37 ,
J. Schmeing 177 , E. Schmidt 112 , M.A. Schmidt 177 , K. Schmieden 102 , C. Schmitt 102 ,
N. Schmitt 102 , S. Schmitt 48 , N.A. Schneider 111 , L. Schoeffel 138 , A. Schoening 63b ,
P.G. Scholer 35 , E. Schopf 147 , M. Schott 25 , S. Schramm 56 , T. Schroer 56 ,
H-C. Schultz-Coulon 63a , M. Schumacher 54 , B.A. Schumm 139 , Ph. Schune 138 ,
H.R. Schwartz 139 , A. Schwartzman 149 , T.A. Schwarz 108 , Ph. Schwemling 138 ,
R. Schwienhorst 109 , F.G. Sciacca 20 , A. Sciandra 30 , G. Sciolla 27 , F. Scuri 74a ,
C.D. Sebastiani 37 , K. Sedlaczek 118 , S.C. Seidel 115 , A. Seiden 139 , B.D. Seidlitz 42 , C. Seitz 48 ,
J.M. Seixas 83b , G. Sekhniaidze 72a , L. Selem 60 , N. Semprini-Cesari 24b,24a , A. Semushin 179 ,
D. Sengupta 56 , V. Senthilkumar 169 , L. Serin 66 , M. Sessa 72a,72b , H. Severini 123 ,
F. Sforza 57b,57a , A. Sfyrla 56 , Q. Sha 14 , E. Shabalina 55 , H. Shaddix 118 , A.H. Shah 33 ,
R. Shaheen 150 , J.D. Shahinian 131 , M. Shamim 37 , L.Y. Shan 14 , M. Shapiro 18a , A. Sharma 37 ,
A.S. Sharma 170 , P. Sharma 30 , P.B. Shatalov 38 , K. Shaw 152 , S.M. Shaw 103 , Q. Shen 144a ,
D.J. Sheppard 148 , P. Sherwood 98 , L. Shi 98 , X. Shi 14 , S. Shimizu 84 , C.O. Shimmin 178 ,
I.P.J. Shipsey 129,* , S. Shirabe 90 , M. Shiyakova 39,z , M.J. Shochet 40 , D.R. Shope 128 ,
B. Shrestha 123 , S. Shrestha 122,al , I. Shreyber 39 , M.J. Shroff 171 , P. Sicho 134 , A.M. Sickles 168 ,
E. Sideras Haddad 34h,166 , A.C. Sidley 117 , A. Sidoti 24b , F. Siegert 50 , Dj. Sĳacki 16 , F. Sili 92 ,
J.M. Silva 52 , I. Silva Ferreira 83b , M.V. Silva Oliveira 30 , S.B. Silverstein 47a , S. Simion66 ,
R. Simoniello 37 , E.L. Simpson 103 , H. Simpson 152 , L.R. Simpson 6 , S. Simsek 82 ,
S. Sindhu 55 , P. Sinervo 161 , S.N. Singh 27 , S. Singh 30 , S. Sinha 48 , S. Sinha 103 ,
M. Sioli 24b,24a , K. Sioulas 9 , I. Siral 37 , E. Sitnikova 48 , J. Sjölin 47a,47b , A. Skaf 55 ,
E. Skorda 21 , P. Skubic 123 , M. Slawinska 87 , I. Slazyk 17 , I. Sliusar 128 , V. Smakhtin175 ,
B.H. Smart 137 , S.Yu. Smirnov 140b , Y. Smirnov 82 , L.N. Smirnova 38,a , O. Smirnova 100 ,
A.C. Smith 42 , D.R. Smith165 , J.L. Smith 103 , M.B. Smith 35 , R. Smith149 , H. Smitmanns 102 ,
M. Smizanska 93 , K. Smolek 135 , P. Smolyanskiy 135 , A.A. Snesarev 39 , H.L. Snoek 117 ,
S. Snyder 30 , R. Sobie 171,ab , A. Soffer 157 , C.A. Solans Sanchez 37 , E.Yu. Soldatov 39 ,
U. Soldevila 169 , A.A. Solodkov 34h , S. Solomon 27 , A. Soloshenko 39 , K. Solovieva 54 ,
O.V. Solovyanov 41 , P. Sommer 50 , A. Sonay 13 , A. Sopczak 135 , A.L. Sopio 52 , F. Sopkova 29b ,
J.D. Sorenson 115 , I.R. Sotarriva Alvarez 141 , V. Sothilingam63a , O.J. Soto Sandoval 140c,140b ,
S. Sottocornola 68 , R. Soualah 88a , Z. Soumaimi 36e , D. South 48 , N. Soybelman 175 ,
S. Spagnolo 70a,70b , M. Spalla 112 , D. Sperlich 54 , B. Spisso 72a,72b , D.P. Spiteri 59 ,
L. Splendori 104 , M. Spousta 136 , E.J. Staats 35 , R. Stamen 63a , E. Stanecka 87 ,
W. Stanek-Maslouska 48 , M.V. Stange 50 , B. Stanislaus 18a , M.M. Stanitzki 48 , B. Stapf 48 ,
E.A. Starchenko 38 , G.H. Stark 139 , J. Stark 91 , P. Staroba 134 , P. Starovoitov 88b ,
R. Staszewski 87 , C. Stauch 111 , G. Stavropoulos 46 , A. Stefl 37 , A. Stein 102 , P. Steinberg 30 ,
B. Stelzer 148,162a , H.J. Stelzer 132 , O. Stelzer-Chilton 162a , H. Stenzel 58 , T.J. Stevenson 152 ,
G.A. Stewart 37 , J.R. Stewart 124 , M.C. Stockton 37 , G. Stoicea 28b , M. Stolarski 133a ,
S. Stonjek 112 , A. Straessner 50 , J. Strandberg 150 , S. Strandberg 47a,47b , M. Stratmann 177 ,
M. Strauss 123 , T. Strebler 104 , P. Strizenec 29b , R. Ströhmer 172 , D.M. Strom 126 ,
R. Stroynowski 45 , A. Strubig 47a,47b , S.A. Stucci 30 , B. Stugu 17 , J. Stupak 123 , N.A. Styles 48 ,
D. Su 149 , S. Su 62 , X. Su 62 , D. Suchy 29a , K. Sugizaki 131 , V.V. Sulin 38 , M.J. Sullivan 94 ,
D.M.S. Sultan 129 , L. Sultanaliyeva 38 , S. Sultansoy 3b , S. Sun 176 , W. Sun 14 ,
O. Sunneborn Gudnadottir 167 , N. Sur 100 , M.R. Sutton 152 , H. Suzuki 163 , M. Svatos 134 ,
P.N. Swallow 33 , M. Swiatlowski 162a , T. Swirski 172 , A. Swoboda 37 , I. Sykora 29a ,
M. Sykora 136 , T. Sykora 136 , D. Ta 102 , K. Tackmann 48,y , A. Taffard 165 , R. Tafirout 162a ,
Y. Takubo 84 , M. Talby 104 , A.A. Talyshev 38 , K.C. Tam 64b , N.M. Tamir 157 , A. Tanaka 159 ,
J. Tanaka 159 , R. Tanaka 66 , M. Tanasini 151 , Z. Tao 170 , S. Tapia Araya 140g , S. Tapprogge 102 ,

37

## PDF page 38

A. Tarek Abouelfadl Mohamed 109 , S. Tarem 156 , K. Tariq 14 , G. Tarna 37 , G.F. Tartarelli 71a ,
M.J. Tartarin 91 , P. Tas 136 , M. Tasevsky 134 , E. Tassi 44b,44a , A.C. Tate 168 , G. Tateno 159 ,
Y. Tayalati 36e,aa , G.N. Taylor 107 , W. Taylor 162b , A.S. Tegetmeier 91 , P. Teixeira-Dias 97 ,
J.J. Teoh 161 , K. Terashi 159 , J. Terron 101 , S. Terzo 13 , M. Testa 53 , R.J. Teuscher 161,ab ,
A. Thaler 79 , O. Theiner 56 , T. Theveneaux-Pelzer 104 , D.W. Thomas97 , J.P. Thomas 21 ,
E.A. Thompson 18a , P.D. Thompson 21 , E. Thomson 131 , R.E. Thornberry 45 , C. Tian 62 ,
Y. Tian 56 , V. Tikhomirov 82 , Yu.A. Tikhonov 39 , S. Timoshenko38 , D. Timoshyn 136 ,
E.X.L. Ting 1 , P. Tipton 178 , A. Tishelman-Charny 30 , K. Todome 141 , S. Todorova-Nova 136 ,
L. Toffolin 69a,69c , M. Togawa 84 , J. Tojo 90 , S. Tokár 29a , O. Toldaiev 68 , G. Tolkachev 104 ,
M. Tomoto 84,113 , L. Tompkins 149,n , E. Torrence 126 , H. Torres 91 , E. Torró Pastor 169 ,
M. Toscani 31 , C. Tosciri 40 , M. Tost 11 , D.R. Tovey 145 , T. Trefzger 172 , P.M. Tricarico 13 ,
A. Tricoli 30 , I.M. Trigger 162a , S. Trincaz-Duvoid 130 , D.A. Trischuk 27 , A. Tropina39 ,
L. Truong 34c , M. Trzebinski 87 , A. Trzupek 87 , F. Tsai 151 , M. Tsai 108 , A. Tsiamis 158 ,
P.V. Tsiareshka39 , S. Tsigaridas 162a , A. Tsirigotis 158,u , V. Tsiskaridze 155a , E.G. Tskhadadze 155a ,
M. Tsopoulou 158 , Y. Tsujikawa 89 , I.I. Tsukerman 38 , V. Tsulaia 18a , S. Tsuno 84 , K. Tsuri 121 ,
D. Tsybychev 151 , Y. Tu 64b , A. Tudorache 28b , V. Tudorache 28b , S.B. Tuncay 129 ,
S. Turchikhin 57b,57a , I. Turk Cakir 3a , R. Turra 71a , T. Turtuvshin 39,ac , P.M. Tuts 42 ,
S. Tzamarias 158,d , E. Tzovara 102 , Y. Uematsu 84 , F. Ukegawa 163 , P.A. Ulloa Poblete 140c,140b ,
E.N. Umaka 30 , G. Unal 37 , A. Undrus 30 , G. Unel 165 , J. Urban 29b , P. Urrejola 140a ,
G. Usai 8 , R. Ushioda 160 , M. Usman 110 , F. Ustuner 52 , Z. Uysal 82 , V. Vacek 135 ,
B. Vachon 106 , T. Vafeiadis 37 , A. Vaitkus 98 , C. Valderanis 111 , E. Valdes Santurio 47a,47b ,
M. Valente 37 , S. Valentinetti 24b,24a , A. Valero 169 , E. Valiente Moreno 169 , S. Valjee 96 ,
A. Vallier 91 , J.A. Valls Ferrer 169 , D.R. Van Arneman 117 , T.R. Van Daalen 142 ,
A. Van Der Graaf 49 , H.Z. Van Der Schyf 34h , P. Van Gemmeren 6 , M. Van Rĳnbach 37 ,
S. Van Stroud 98 , I. Van Vulpen 117 , P. Vana 136 , M. Vanadia 76a,76b , U.M. Vande Voorde 150 ,
W. Vandelli 37 , E.R. Vandewall 124 , D. Vannicola 157 , L. Vannoli 53 , R. Vari 75a , M. Varma 178 ,
E.W. Varnes 7 , C. Varni 118 , D. Varouchas 66 , L. Varriale 169 , K.E. Varvell 153 , M.E. Vasile 28b ,
L. Vaslin84 , M.D. Vassilev 149 , A. Vasyukov 39 , L.M. Vaughan 124 , R. Vavricka136 ,
T. Vazquez Schroeder 13 , J. Veatch 32 , V. Vecchio 103 , M.J. Veen 105 , I. Veliscek 30 ,
I. Velkovska 95 , L.M. Veloce 161 , F. Veloso 133a,133c , S. Veneziano 75a , A. Ventura 70a,70b ,
A. Verbytskyi 112 , M. Verducci 74a,74b , C. Vergis 96 , M. Verissimo De Araujo 83b ,
W. Verkerke 117 , J.C. Vermeulen 117 , C. Vernieri 149 , M. Vessella 165 , M.C. Vetterli 148,ah ,
A. Vgenopoulos 102 , N. Viaux Maira 140g , T. Vickey 145 , O.E. Vickey Boeriu 145 ,
G.H.A. Viehhauser 129 , L. Vigani 63b , M. Vigl 112 , M. Villa 24b,24a , M. Villaplana Perez 169 ,
E.M. Villhauer40 , E. Vilucchi 53 , M. Vincent 169 , M.G. Vincter 35 , A. Visibile117 , C. Vittori 37 ,
I. Vivarelli 24b,24a , E. Voevodina 112 , F. Vogel 111 , J.C. Voigt 50 , P. Vokac 135 , Yu. Volkotrub 86b ,
E. Von Toerne 25 , B. Vormwald 37 , K. Vorobev 51 , M. Vos 169 , K. Voss 147 , M. Vozak 37 ,
L. Vozdecky 123 , N. Vranjes 16 , M. Vranjes Milosavljevic 16 , M. Vreeswĳk 117 , N.K. Vu 144b,144a ,
R. Vuillermet 37 , O. Vujinovic 102 , I. Vukotic 40 , I.K. Vyas 35 , J.F. Wack 33 , S. Wada 163 ,
C. Wagner149 , J.M. Wagner 18a , W. Wagner 177 , S. Wahdan 177 , H. Wahlberg 92 , C.H. Waits 123 ,
J. Walder 137 , R. Walker 111 , K. Walkingshaw Pass59 , W. Walkowiak 147 , A. Wall 131 ,
E.J. Wallin 100 , T. Wamorkar 18a , A. Wang 62 , A.Z. Wang 139 , C. Wang 102 , C. Wang 11 ,
H. Wang 18a , J. Wang 64c , P. Wang 103 , P. Wang 98 , R. Wang 61 , R. Wang 6 , S.M. Wang 154 ,
S. Wang 14 , T. Wang 62 , T. Wang 62 , W.T. Wang 80 , W. Wang 14 , X. Wang 168 , X. Wang 144a ,
X. Wang 48 , Y. Wang 114a , Y. Wang 62 , Z. Wang 108 , Z. Wang 144b , Z. Wang 108 ,
C. Wanotayaroj 84 , A. Warburton 106 , A.L. Warnerbring 147 , N. Warrack 59 , S. Waterhouse 97 ,
A.T. Watson 21 , H. Watson 52 , M.F. Watson 21 , E. Watton 59 , G. Watts 142 , B.M. Waugh 98 ,

38

## PDF page 39

J.M. Webb 54 , C. Weber 30 , H.A. Weber 19 , M.S. Weber 20 , S.M. Weber 63a , C. Wei 62 ,
Y. Wei 54 , A.R. Weidberg 129 , E.J. Weik 120 , J. Weingarten 49 , C. Weiser 54 , C.J. Wells 48 ,
T. Wenaus 30 , B. Wendland 49 , T. Wengler 37 , N.S. Wenke112 , N. Wermes 25 , M. Wessels 63a ,
A.M. Wharton 93 , A.S. White 61 , A. White 8 , M.J. White 1 , D. Whiteson 165 ,
L. Wickremasinghe 127 , W. Wiedenmann 176 , M. Wielers 137 , R. Wierda 150 , C. Wiglesworth 43 ,
H.G. Wilkens 37 , J.J.H. Wilkinson 33 , D.M. Williams 42 , H.H. Williams131 , S. Williams 33 ,
S. Willocq 105 , B.J. Wilson 103 , D.J. Wilson 103 , P.J. Windischhofer 40 , F.I. Winkel 31 ,
F. Winklmeier 126 , B.T. Winter 54 , M. Wittgen149 , M. Wobisch 99 , T. Wojtkowski60 , Z. Wolffs 117 ,
J. Wollrath37 , M.W. Wolter 87 , H. Wolters 133a,133c , M.C. Wong139 , E.L. Woodward 42 ,
S.D. Worm 48 , B.K. Wosiek 87 , K.W. Woźniak 87 , S. Wozniewski 55 , K. Wraight 59 , C. Wu 161 ,
C. Wu 21 , J. Wu 159 , M. Wu 114b , M. Wu 116 , S.L. Wu 176 , S. Wu 14 , X. Wu 62 , Y. Wu 62 ,
Z. Wu 4 , J. Wuerzinger 112 , T.R. Wyatt 103 , B.M. Wynne 52 , S. Xella 43 , L. Xia 114a ,
M. Xia 15 , M. Xie 62 , A. Xiong 126 , J. Xiong 18a , D. Xu 14 , H. Xu 62 , L. Xu 62 , R. Xu 131 ,
T. Xu 108 , Y. Xu 142 , Z. Xu 52 , R. Xue 132 , B. Yabsley 153 , S. Yacoob 34a , Y. Yamaguchi 84 ,
E. Yamashita 159 , H. Yamauchi 163 , T. Yamazaki 18a , Y. Yamazaki 85 , S. Yan 59 , Z. Yan 105 ,
H.J. Yang 144a,144b , H.T. Yang 62 , S. Yang 62 , T. Yang 64c , X. Yang 37 , X. Yang 14 ,
Y. Yang 159 , Y. Yang62 , W-M. Yao 18a , C.L. Yardley 152 , J. Ye 14 , S. Ye 30 , X. Ye 62 , Y. Yeh 98 ,
I. Yeletskikh 39 , B. Yeo 18b , M.R. Yexley 98 , T.P. Yildirim 129 , K. Yorita 174 , C.J.S. Young 37 ,
C. Young 149 , N.D. Young126 , Y. Yu 62 , J. Yuan 14,114c , M. Yuan 108 , R. Yuan 144b,144a ,
L. Yue 98 , M. Zaazoua 62 , B. Zabinski 87 , I. Zahir 36a , A. Zaio57b,57a , Z.K. Zak 87 ,
T. Zakareishvili 169 , S. Zambito 56 , J.A. Zamora Saa 140d , J. Zang 159 , R. Zanzottera 71a,71b ,
O. Zaplatilek 135 , C. Zeitnitz 177 , H. Zeng 14 , J.C. Zeng 168 , D.T. Zenger Jr 27 , O. Zenin 38 ,
T. Ženiš 29a , S. Zenz 96 , D. Zerwas 66 , M. Zhai 14,114c , D.F. Zhang 145 , G. Zhang 14 ,
J. Zhang 143a , J. Zhang 6 , K. Zhang 14,114c , L. Zhang 62 , L. Zhang 114a , P. Zhang 14,114c ,
R. Zhang 114a , S. Zhang 91 , T. Zhang 159 , Y. Zhang 142 , Y. Zhang 98 , Y. Zhang 62 ,
Y. Zhang 114a , Z. Zhang 143a , Z. Zhang 66 , H. Zhao 142 , T. Zhao 143a , Y. Zhao 35 , Z. Zhao 62 ,
Z. Zhao 62 , A. Zhemchugov 39 , J. Zheng 114a , K. Zheng 168 , X. Zheng 62 , Z. Zheng 149 ,
D. Zhong 168 , B. Zhou 108 , H. Zhou 7 , N. Zhou 144a , Y. Zhou 15 , Y. Zhou 114a , Y. Zhou7 ,
C.G. Zhu 143a , J. Zhu 108 , X. Zhu144b , Y. Zhu 144a , Y. Zhu 62 , X. Zhuang 14 , K. Zhukov 68 ,
N.I. Zimine 39 , J. Zinsser 63b , M. Ziolkowski 147 , L. Živković 16 , A. Zoccoli 24b,24a , K. Zoch 61 ,
A. Zografos 37 , T.G. Zorbas 145 , O. Zormpa 46 , L. Zwalinski 37 .
1 Department of Physics, University of Adelaide, Adelaide; Australia.
2 Department of Physics, University of Alberta, Edmonton AB; Canada.
3 (𝑎) Department of Physics, Ankara University, Ankara; (𝑏) Division of Physics, TOBB University of

Economics and Technology, Ankara; Türkiye.
4 LAPP, Université Savoie Mont Blanc, CNRS/IN2P3, Annecy; France.
5 APC, Université Paris Cité, CNRS/IN2P3, Paris; France.
6 High Energy Physics Division, Argonne National Laboratory, Argonne IL; United States of America.
7 Department of Physics, University of Arizona, Tucson AZ; United States of America.
8 Department of Physics, University of Texas at Arlington, Arlington TX; United States of America.
9 Physics Department, National and Kapodistrian University of Athens, Athens; Greece.
10 Physics Department, National Technical University of Athens, Zografou; Greece.
11 Department of Physics, University of Texas at Austin, Austin TX; United States of America.
12 Institute of Physics, Azerbaĳan Academy of Sciences, Baku; Azerbaĳan.
13 Institut de Física d’Altes Energies (IFAE), Barcelona Institute of Science and Technology, Barcelona;

Spain.

39

## PDF page 40

14 Institute of High Energy Physics, Chinese Academy of Sciences, Beĳing; China.
15 Physics Department, Tsinghua University, Beĳing; China.
16 Institute of Physics, University of Belgrade, Belgrade; Serbia.
17 Department for Physics and Technology, University of Bergen, Bergen; Norway.
18 (𝑎) Physics Division, Lawrence Berkeley National Laboratory, Berkeley CA; (𝑏) University of California,

Berkeley CA; United States of America.
19 Institut für Physik, Humboldt Universität zu Berlin, Berlin; Germany.
20 Albert Einstein Center for Fundamental Physics and Laboratory for High Energy Physics, University of

Bern, Bern; Switzerland.
21 School of Physics and Astronomy, University of Birmingham, Birmingham; United Kingdom.
22 (𝑎) Department of Physics, Bogazici University, Istanbul; (𝑏) Department of Physics Engineering,
Gaziantep University, Gaziantep; (𝑐) Department of Physics, Istanbul University, Istanbul; Türkiye.
23 (𝑎) Facultad de Ciencias y Centro de Investigaciónes, Universidad Antonio Nariño,
Bogotá; (𝑏) Departamento de Física, Universidad Nacional de Colombia, Bogotá; Colombia.
24 (𝑎) Dipartimento di Fisica e Astronomia A. Righi, Università di Bologna, Bologna; (𝑏) INFN Sezione di
Bologna; Italy.
25 Physikalisches Institut, Universität Bonn, Bonn; Germany.
26 Department of Physics, Boston University, Boston MA; United States of America.
27 Department of Physics, Brandeis University, Waltham MA; United States of America.
28 (𝑎) Transilvania University of Brasov, Brasov; (𝑏) Horia Hulubei National Institute of Physics and Nuclear
Engineering, Bucharest; (𝑐) Department of Physics, Alexandru Ioan Cuza University of Iasi, Iasi; (𝑑) National
Institute for Research and Development of Isotopic and Molecular Technologies, Physics Department,
Cluj-Napoca; (𝑒) National University of Science and Technology Politechnica, Bucharest; ( 𝑓 ) West
University in Timisoara, Timisoara; (𝑔) Faculty of Physics, University of Bucharest, Bucharest; Romania.
29 (𝑎) Faculty of Mathematics, Physics and Informatics, Comenius University, Bratislava; (𝑏) Department of
Subnuclear Physics, Institute of Experimental Physics of the Slovak Academy of Sciences, Kosice; Slovak
Republic.
30 Physics Department, Brookhaven National Laboratory, Upton NY; United States of America.
31 Universidad de Buenos Aires, Facultad de Ciencias Exactas y Naturales, Departamento de Física, y
CONICET, Instituto de Física de Buenos Aires (IFIBA), Buenos Aires; Argentina.
32 California State University, CA; United States of America.
33 Cavendish Laboratory, University of Cambridge, Cambridge; United Kingdom.
34 (𝑎) Department of Physics, University of Cape Town, Cape Town; (𝑏) iThemba Labs, Western
Cape; (𝑐) Department of Mechanical Engineering Science, University of Johannesburg,
Johannesburg; (𝑑) National Institute of Physics, University of the Philippines Diliman
(Philippines); (𝑒) Department of Physics, Stellenbosch University, Matieland; ( 𝑓 ) University of South Africa,
Department of Physics, Pretoria; (𝑔) University of Zululand, KwaDlangezwa; (ℎ) School of Physics,
University of the Witwatersrand, Johannesburg; South Africa.
35 Department of Physics, Carleton University, Ottawa ON; Canada.
36 (𝑎) Faculté des Sciences Ain Chock, Université Hassan II de Casablanca; (𝑏) Faculté des Sciences,
Université Ibn-Tofail, Kénitra; (𝑐) Faculté des Sciences Semlalia, Université Cadi Ayyad,
LPHEA-Marrakech; (𝑑) LPMR, Faculté des Sciences, Université Mohamed Premier, Oujda; (𝑒) Faculté des
sciences, Université Mohammed V, Rabat; ( 𝑓 ) Institute of Applied Physics, Mohammed VI Polytechnic
University, Ben Guerir; Morocco.
37 CERN, Geneva; Switzerland.
38 Affiliated with an institute formerly covered by a cooperation agreement with CERN.
39 Affiliated with an international laboratory covered by a cooperation agreement with CERN.

40

## PDF page 41

40 Enrico Fermi Institute, University of Chicago, Chicago IL; United States of America.
41 LPC, Université Clermont Auvergne, CNRS/IN2P3, Clermont-Ferrand; France.
42 Nevis Laboratory, Columbia University, Irvington NY; United States of America.
43 Niels Bohr Institute, University of Copenhagen, Copenhagen; Denmark.
44 (𝑎) Dipartimento di Fisica, Università della Calabria, Rende; (𝑏) INFN Gruppo Collegato di Cosenza,

Laboratori Nazionali di Frascati; Italy.
45 Physics Department, Southern Methodist University, Dallas TX; United States of America.
46 National Centre for Scientific Research "Demokritos", Agia Paraskevi; Greece.
47 (𝑎) Department of Physics, Stockholm University; (𝑏) Oskar Klein Centre, Stockholm; Sweden.
48 Deutsches Elektronen-Synchrotron DESY, Hamburg and Zeuthen; Germany.
49 Fakultät Physik , Technische Universität Dortmund, Dortmund; Germany.
50 Institut für Kern- und Teilchenphysik, Technische Universität Dresden, Dresden; Germany.
51 Department of Physics, Duke University, Durham NC; United States of America.
52 SUPA - School of Physics and Astronomy, University of Edinburgh, Edinburgh; United Kingdom.
53 INFN e Laboratori Nazionali di Frascati, Frascati; Italy.
54 Physikalisches Institut, Albert-Ludwigs-Universität Freiburg, Freiburg; Germany.
55 II. Physikalisches Institut, Georg-August-Universität Göttingen, Göttingen; Germany.
56 Département de Physique Nucléaire et Corpusculaire, Université de Genève, Genève; Switzerland.
57 (𝑎) Dipartimento di Fisica, Università di Genova, Genova; (𝑏) INFN Sezione di Genova; Italy.
58 II. Physikalisches Institut, Justus-Liebig-Universität Giessen, Giessen; Germany.
59 SUPA - School of Physics and Astronomy, University of Glasgow, Glasgow; United Kingdom.
60 LPSC, Université Grenoble Alpes, CNRS/IN2P3, Grenoble INP, Grenoble; France.
61 Laboratory for Particle Physics and Cosmology, Harvard University, Cambridge MA; United States of

America.
62 Department of Modern Physics and State Key Laboratory of Particle Detection and Electronics,
University of Science and Technology of China, Hefei; China.
63 (𝑎) Kirchhoff-Institut für Physik, Ruprecht-Karls-Universität Heidelberg, Heidelberg; (𝑏) Physikalisches
Institut, Ruprecht-Karls-Universität Heidelberg, Heidelberg; Germany.
64 (𝑎) Department of Physics, Chinese University of Hong Kong, Shatin, N.T., Hong Kong; (𝑏) Department
of Physics, University of Hong Kong, Hong Kong; (𝑐) Department of Physics and Institute for Advanced
Study, Hong Kong University of Science and Technology, Clear Water Bay, Kowloon, Hong Kong; China.
65 Department of Physics, National Tsing Hua University, Hsinchu; Taiwan.
66 ĲCLab, Université Paris-Saclay, CNRS/IN2P3, 91405, Orsay; France.
67 Centro Nacional de Microelectrónica (IMB-CNM-CSIC), Barcelona; Spain.
68 Department of Physics, Indiana University, Bloomington IN; United States of America.
69 (𝑎) INFN Gruppo Collegato di Udine, Sezione di Trieste, Udine; (𝑏) ICTP, Trieste; (𝑐) Dipartimento
Politecnico di Ingegneria e Architettura, Università di Udine, Udine; Italy.
70 (𝑎) INFN Sezione di Lecce; (𝑏) Dipartimento di Matematica e Fisica, Università del Salento, Lecce; Italy.
71 (𝑎) INFN Sezione di Milano; (𝑏) Dipartimento di Fisica, Università di Milano, Milano; Italy.
72 (𝑎) INFN Sezione di Napoli; (𝑏) Dipartimento di Fisica, Università di Napoli, Napoli; Italy.
73 (𝑎) INFN Sezione di Pavia; (𝑏) Dipartimento di Fisica, Università di Pavia, Pavia; Italy.
74 (𝑎) INFN Sezione di Pisa; (𝑏) Dipartimento di Fisica E. Fermi, Università di Pisa, Pisa; Italy.
75 (𝑎) INFN Sezione di Roma; (𝑏) Dipartimento di Fisica, Sapienza Università di Roma, Roma; Italy.
76 (𝑎) INFN Sezione di Roma Tor Vergata; (𝑏) Dipartimento di Fisica, Università di Roma Tor Vergata,
Roma; Italy.
77 (𝑎) INFN Sezione di Roma Tre; (𝑏) Dipartimento di Matematica e Fisica, Università Roma Tre, Roma;
Italy.

41

## PDF page 42

78 (𝑎) INFN-TIFPA; (𝑏) Università degli Studi di Trento, Trento; Italy.
79 Universität Innsbruck, Department of Astro and Particle Physics, Innsbruck; Austria.
80 University of Iowa, Iowa City IA; United States of America.
81 Department of Physics and Astronomy, Iowa State University, Ames IA; United States of America.
82 Istinye University, Sariyer, Istanbul; Türkiye.
83 (𝑎) Departamento de Engenharia Elétrica, Universidade Federal de Juiz de Fora (UFJF), Juiz de

Fora; (𝑏) Universidade Federal do Rio De Janeiro COPPE/EE/IF, Rio de Janeiro; (𝑐) Instituto de Física,
Universidade de São Paulo, São Paulo; (𝑑) Rio de Janeiro State University, Rio de Janeiro; (𝑒) Federal
University of Bahia, Bahia; Brazil.
84 KEK, High Energy Accelerator Research Organization, Tsukuba; Japan.
85 Graduate School of Science, Kobe University, Kobe; Japan.
86 (𝑎) AGH University of Krakow, Faculty of Physics and Applied Computer Science, Krakow; (𝑏) Marian
Smoluchowski Institute of Physics, Jagiellonian University, Krakow; Poland.
87 Institute of Nuclear Physics Polish Academy of Sciences, Krakow; Poland.
88 (𝑎) Khalifa University of Science and Technology, Abu Dhabi; (𝑏) University of Sharjah, Sharjah; United
Arab Emirates.
89 Faculty of Science, Kyoto University, Kyoto; Japan.
90 Research Center for Advanced Particle Physics and Department of Physics, Kyushu University, Fukuoka ;
Japan.
91 L2IT, Université de Toulouse, CNRS/IN2P3, UPS, Toulouse; France.
92 Instituto de Física La Plata, Universidad Nacional de La Plata and CONICET, La Plata; Argentina.
93 Physics Department, Lancaster University, Lancaster; United Kingdom.
94 Oliver Lodge Laboratory, University of Liverpool, Liverpool; United Kingdom.
95 Department of Experimental Particle Physics, Jožef Stefan Institute and Department of Physics,
University of Ljubljana, Ljubljana; Slovenia.
96 Department of Physics and Astronomy, Queen Mary University of London, London; United Kingdom.
97 Department of Physics, Royal Holloway University of London, Egham; United Kingdom.
98 Department of Physics and Astronomy, University College London, London; United Kingdom.
99 Louisiana Tech University, Ruston LA; United States of America.
100 Fysiska institutionen, Lunds universitet, Lund; Sweden.
101 Departamento de Física Teorica C-15 and CIAFF, Universidad Autónoma de Madrid, Madrid; Spain.
102 Institut für Physik, Universität Mainz, Mainz; Germany.
103 School of Physics and Astronomy, University of Manchester, Manchester; United Kingdom.
104 CPPM, Aix-Marseille Université, CNRS/IN2P3, Marseille; France.
105 Department of Physics, University of Massachusetts, Amherst MA; United States of America.
106 Department of Physics, McGill University, Montreal QC; Canada.
107 School of Physics, University of Melbourne, Victoria; Australia.
108 Department of Physics, University of Michigan, Ann Arbor MI; United States of America.
109 Department of Physics and Astronomy, Michigan State University, East Lansing MI; United States of
America.
110 Group of Particle Physics, University of Montreal, Montreal QC; Canada.
111 Fakultät für Physik, Ludwig-Maximilians-Universität München, München; Germany.
112 Max-Planck-Institut für Physik (Werner-Heisenberg-Institut), München; Germany.
113 Graduate School of Science and Kobayashi-Maskawa Institute, Nagoya University, Nagoya; Japan.
114 (𝑎) Department of Physics, Nanjing University, Nanjing; (𝑏) School of Science, Shenzhen Campus of Sun
Yat-sen University; (𝑐) University of Chinese Academy of Science (UCAS), Beĳing; China.
115 Department of Physics and Astronomy, University of New Mexico, Albuquerque NM; United States of

42

## PDF page 43

America.
116 Institute for Mathematics, Astrophysics and Particle Physics, Radboud University/Nikhef, Nĳmegen;
Netherlands.
117 Nikhef National Institute for Subatomic Physics and University of Amsterdam, Amsterdam;
Netherlands.
118 Department of Physics, Northern Illinois University, DeKalb IL; United States of America.
119 (𝑎) New York University Abu Dhabi, Abu Dhabi; (𝑏) United Arab Emirates University, Al Ain; United
Arab Emirates.
120 Department of Physics, New York University, New York NY; United States of America.
121 Ochanomizu University, Otsuka, Bunkyo-ku, Tokyo; Japan.
122 Ohio State University, Columbus OH; United States of America.
123 Homer L. Dodge Department of Physics and Astronomy, University of Oklahoma, Norman OK; United
States of America.
124 Department of Physics, Oklahoma State University, Stillwater OK; United States of America.
125 Palacký University, Joint Laboratory of Optics, Olomouc; Czech Republic.
126 Institute for Fundamental Science, University of Oregon, Eugene, OR; United States of America.
127 Graduate School of Science, University of Osaka, Osaka; Japan.
128 Department of Physics, University of Oslo, Oslo; Norway.
129 Department of Physics, Oxford University, Oxford; United Kingdom.
130 LPNHE, Sorbonne Université, Université Paris Cité, CNRS/IN2P3, Paris; France.
131 Department of Physics, University of Pennsylvania, Philadelphia PA; United States of America.
132 Department of Physics and Astronomy, University of Pittsburgh, Pittsburgh PA; United States of
America.
133 (𝑎) Laboratório de Instrumentação e Física Experimental de Partículas - LIP, Lisboa; (𝑏) Departamento
de Física, Faculdade de Ciências, Universidade de Lisboa, Lisboa; (𝑐) Departamento de Física,
Universidade de Coimbra, Coimbra; (𝑑) Centro de Física Nuclear da Universidade de Lisboa,
Lisboa; (𝑒) Departamento de Física, Escola de Ciências, Universidade do Minho, Braga; ( 𝑓 ) Departamento
de Física Teórica y del Cosmos, Universidad de Granada, Granada (Spain); (𝑔) Departamento de Física,
Instituto Superior Técnico, Universidade de Lisboa, Lisboa; Portugal.
134 Institute of Physics of the Czech Academy of Sciences, Prague; Czech Republic.
135 Czech Technical University in Prague, Prague; Czech Republic.
136 Charles University, Faculty of Mathematics and Physics, Prague; Czech Republic.
137 Particle Physics Department, Rutherford Appleton Laboratory, Didcot; United Kingdom.
138 IRFU, CEA, Université Paris-Saclay, Gif-sur-Yvette; France.
139 Santa Cruz Institute for Particle Physics, University of California Santa Cruz, Santa Cruz CA; United
States of America.
140 (𝑎) Departamento de Física, Pontificia Universidad Católica de Chile, Santiago; (𝑏) Millennium Institute
for Subatomic physics at high energy frontier (SAPHIR), Santiago; (𝑐) Instituto de Investigación
Multidisciplinario en Ciencia y Tecnología, y Departamento de Física, Universidad de La
Serena; (𝑑) Universidad Andres Bello, Department of Physics, Santiago; (𝑒) Universidad San Sebastian,
Recoleta; ( 𝑓 ) Instituto de Alta Investigación, Universidad de Tarapacá, Arica; (𝑔) Departamento de Física,
Universidad Técnica Federico Santa María, Valparaíso; Chile.
141 Department of Physics, Institute of Science, Tokyo; Japan.
142 Department of Physics, University of Washington, Seattle WA; United States of America.
143 (𝑎) Institute of Frontier and Interdisciplinary Science and Key Laboratory of Particle Physics and Particle
Irradiation (MOE), Shandong University, Qingdao; (𝑏) School of Physics, Zhengzhou University; China.
144 (𝑎) State Key Laboratory of Dark Matter Physics, School of Physics and Astronomy, Shanghai Jiao Tong

43

## PDF page 44

University, Key Laboratory for Particle Astrophysics and Cosmology (MOE), SKLPPC, Shanghai; (𝑏) State
Key Laboratory of Dark Matter Physics, Tsung-Dao Lee Institute, Shanghai Jiao Tong University,
Shanghai; China.
145 Department of Physics and Astronomy, University of Sheffield, Sheffield; United Kingdom.
146 Department of Physics, Shinshu University, Nagano; Japan.
147 Department Physik, Universität Siegen, Siegen; Germany.
148 Department of Physics, Simon Fraser University, Burnaby BC; Canada.
149 SLAC National Accelerator Laboratory, Stanford CA; United States of America.
150 Department of Physics, Royal Institute of Technology, Stockholm; Sweden.
151 Departments of Physics and Astronomy, Stony Brook University, Stony Brook NY; United States of
America.
152 Department of Physics and Astronomy, University of Sussex, Brighton; United Kingdom.
153 School of Physics, University of Sydney, Sydney; Australia.
154 Institute of Physics, Academia Sinica, Taipei; Taiwan.
155 (𝑎) E. Andronikashvili Institute of Physics, Iv. Javakhishvili Tbilisi State University, Tbilisi; (𝑏) High
Energy Physics Institute, Tbilisi State University, Tbilisi; (𝑐) University of Georgia, Tbilisi; Georgia.
156 Department of Physics, Technion, Israel Institute of Technology, Haifa; Israel.
157 Raymond and Beverly Sackler School of Physics and Astronomy, Tel Aviv University, Tel Aviv; Israel.
158 Department of Physics, Aristotle University of Thessaloniki, Thessaloniki; Greece.
159 International Center for Elementary Particle Physics and Department of Physics, University of Tokyo,
Tokyo; Japan.
160 Graduate School of Science and Technology, Tokyo Metropolitan University, Tokyo; Japan.
161 Department of Physics, University of Toronto, Toronto ON; Canada.
162 (𝑎) TRIUMF, Vancouver BC; (𝑏) Department of Physics and Astronomy, York University, Toronto ON;
Canada.
163 Division of Physics and Tomonaga Center for the History of the Universe, Faculty of Pure and Applied
Sciences, University of Tsukuba, Tsukuba; Japan.
164 Department of Physics and Astronomy, Tufts University, Medford MA; United States of America.
165 Department of Physics and Astronomy, University of California Irvine, Irvine CA; United States of
America.
166 University of West Attica, Athens; Greece.
167 Department of Physics and Astronomy, University of Uppsala, Uppsala; Sweden.
168 Department of Physics, University of Illinois, Urbana IL; United States of America.
169 Instituto de Física Corpuscular (IFIC), Centro Mixto Universidad de Valencia - CSIC, Valencia; Spain.
170 Department of Physics, University of British Columbia, Vancouver BC; Canada.
171 Department of Physics and Astronomy, University of Victoria, Victoria BC; Canada.
172 Fakultät für Physik und Astronomie, Julius-Maximilians-Universität Würzburg, Würzburg; Germany.
173 Department of Physics, University of Warwick, Coventry; United Kingdom.
174 Waseda University, Tokyo; Japan.
175 Department of Particle Physics and Astrophysics, Weizmann Institute of Science, Rehovot; Israel.
176 Department of Physics, University of Wisconsin, Madison WI; United States of America.
177 Fakultät für Mathematik und Naturwissenschaften, Fachgruppe Physik, Bergische Universität
Wuppertal, Wuppertal; Germany.
178 Department of Physics, Yale University, New Haven CT; United States of America.
179 Yerevan Physics Institute, Yerevan; Armenia.
𝑎 Also at Affiliated with an institute formerly covered by a cooperation agreement with CERN.
𝑏 Also at An-Najah National University, Nablus; Palestine.

44

## PDF page 45

𝑐 Also at Borough of Manhattan Community College, City University of New York, New York NY; United

States of America.
𝑑 Also at Center for Interdisciplinary Research and Innovation (CIRI-AUTH), Thessaloniki; Greece.
𝑒 Also at Centre of Physics of the Universities of Minho and Porto (CF-UM-UP); Portugal.
𝑓 Also at CERN, Geneva; Switzerland.
𝑔 Also at Département de Physique Nucléaire et Corpusculaire, Université de Genève, Genève;
Switzerland.
ℎ Also at Departament de Fisica de la Universitat Autonoma de Barcelona, Barcelona; Spain.
𝑖 Also at Department of Financial and Management Engineering, University of the Aegean, Chios; Greece.
𝑗 Also at Department of Mathematical Sciences, University of South Africa, Johannesburg; South Africa.
𝑘 Also at Department of Modern Physics and State Key Laboratory of Particle Detection and Electronics,
University of Science and Technology of China, Hefei; China.
𝑙 Also at Department of Physics, Bolu Abant Izzet Baysal University, Bolu; Türkiye.
𝑚 Also at Department of Physics, King’s College London, London; United Kingdom.
𝑛 Also at Department of Physics, Stanford University, Stanford CA; United States of America.
𝑜 Also at Department of Physics, Stellenbosch University; South Africa.
𝑝 Also at Department of Physics, University of Fribourg, Fribourg; Switzerland.
𝑞 Also at Department of Physics, University of Thessaly; Greece.
𝑟 Also at Department of Physics, Westmont College, Santa Barbara; United States of America.
𝑠 Also at Faculty of Physics, Sofia University, ’St. Kliment Ohridski’, Sofia; Bulgaria.
𝑡 Also at Faculty of Physics, University of Bucharest ; Romania.
𝑢 Also at Hellenic Open University, Patras; Greece.
𝑣 Also at Henan University; China.
𝑤 Also at Imam Mohammad Ibn Saud Islamic University; Saudi Arabia.
𝑥 Also at Institucio Catalana de Recerca i Estudis Avancats, ICREA, Barcelona; Spain.
𝑦 Also at Institut für Experimentalphysik, Universität Hamburg, Hamburg; Germany.
𝑧 Also at Institute for Nuclear Research and Nuclear Energy (INRNE) of the Bulgarian Academy of
Sciences, Sofia; Bulgaria.
𝑎𝑎 Also at Institute of Applied Physics, Mohammed VI Polytechnic University, Ben Guerir; Morocco.
𝑎𝑏 Also at Institute of Particle Physics (IPP); Canada.
𝑎𝑐 Also at Institute of Physics and Technology, Mongolian Academy of Sciences, Ulaanbaatar; Mongolia.
𝑎𝑑 Also at Institute of Physics, Azerbaĳan Academy of Sciences, Baku; Azerbaĳan.
𝑎𝑒 Also at Institute of Theoretical Physics, Ilia State University, Tbilisi; Georgia.
𝑎 𝑓 Also at National Institute of Physics, University of the Philippines Diliman (Philippines); Philippines.
𝑎𝑔 Also at The Collaborative Innovation Center of Quantum Matter (CICQM), Beĳing; China.
𝑎ℎ Also at TRIUMF, Vancouver BC; Canada.
𝑎𝑖 Also at Università di Napoli Parthenope, Napoli; Italy.
𝑎 𝑗 Also at University of Colorado Boulder, Department of Physics, Colorado; United States of America.
𝑎𝑘 Also at University of Sienna; Italy.
𝑎𝑙 Also at Washington College, Chestertown, MD; United States of America.
𝑎𝑚 Also at Yeditepe University, Physics Department, Istanbul; Türkiye.
∗ Deceased

45
