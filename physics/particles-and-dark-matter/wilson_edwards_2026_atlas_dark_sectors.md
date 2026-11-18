Source: https://arxiv.org/abs/2601.13033v1
PDF sha256: a9446f6a3a18fac98df20e051861a69fc33d6f8a5a623f0d4a70ff9db401fc84
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of wilson_edwards_2026_atlas_dark_sectors.pdf

Transcription of `wilson_edwards_2026_atlas_dark_sectors.pdf` in this directory, 5 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-5 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Searches for unusual signatures from dark sectors with
the ATLAS Experiment
Danielle Wilson-Edwards𝑎,∗ on behalf of the ATLAS Collaboration
𝑎 School of Physics and Astronomy, University of Manchester

Manchester, United Kingdom

arXiv:2601.13033v1 [hep-ex] 19 Jan 2026

E-mail: danielle.joan.wilson@cern.ch
Presented at the 32nd International Symposium on Lepton Photon Interactions at High Energies, Madison,
Wisconsin, USA, August 25–29, 2025
Various theories beyond the Standard Model predict unusual signatures, including new, long-lived
particles decaying at a significant distance from the collision point. These unique signatures are
difficult to reconstruct and face unusual and challenging backgrounds. This contribution will focus
on recent results from searches for unusual signatures motivated by dark sector models, utilising
pp collision data collected by the ATLAS experiment at the Large Hadron Collider.

1. Introduction
Evidence of Dark Matter (DM) is abundant (for example, see Refs. [1–5]). Its interactions
with the Standard Model (SM) particles, however, remain unestablished. Many extensions to the
SM attempt to describe DM’s particle nature and interactions. One such extension is the dark sector
(DS) [6–8], comprising new particles that interact with the SM only via a mediator that couples to
both sectors. These mediators include dark photons, sterile neutrinos, axions, or new scalar or vector
bosons. The ATLAS [9] collaboration has conducted searches for different DS scenarios at the
Large Hadron Collider (LHC) [10], which can manifest as a wide variety of experimental signatures.
For instance, final states might be invisible or partially invisible, contain displaced decays, or feature
jets with atypical topologies. Since the ATLAS detector was optimised to detect and identify SM
particles which are produced in the prompt decay of SM or BSM particles, non-standard events
could be rejected by standard triggers or default reconstructions. Consequently, these searches
push the limits of detector performance by employing novel techniques such as dedicated triggers,
special reconstructions, and data-driven background estimation. These proceedings present two
unique signatures that probe different DS models.

2. Search for emerging jets
The ATLAS collaboration searched for emerging jets [11] using 51.8 fb −1 of proton–proton
√
collision data at 𝑠 = 13.6 TeV, collected during the LHC Run 3 (2022-2023). The search targets
a DS with QCD-like dynamics. In such models, “dark quarks” are charged under a new confining
SU(𝑁D ) gauge group, where 𝑁D is the number of dark colours, and couple to SM quarks via a new
mediator particle. Dark quarks hadronise into dark mesons (namely, the dark pion 𝜋D , and dark
vector meson 𝜌D ), whose lifetimes determine the decay modes: they may promptly decay back to
SM particles (dark jets), remain stable and invisible in the detector (potentially providing a DM
candidate), or be metastable and travel some distance before decaying, producing displaced vertices
∗ Speaker

© Copyright 2025 CERN for the benefit of the ATLAS Collaboration.
Reproduction of this article or parts of it is allowed as specified in the CC-BY-4.0 license

## PDF page 2

Searches for unusual signatures from dark sectors with ATLAS

Danielle Wilson-Edwards

within the detector. The latter case is the focus of this analysis, where long-lived dark mesons
produce emerging jets [12] containing multiple secondary vertices.
This search targets emerging jets from two different mediator scenarios: an s-channel process
via a vector boson 𝑍 ′ that couples to SM and dark quarks separately, and a t-channel process via a
scalar Φ that couples simultaneously to one SM quark and one dark quark. Jets are classified using
two complementary analysis strategies: namely a cut-based strategy to increase interpretability
and a machine-learning (ML) based strategy to optimise signal sensitivity. Events are required to
have two large-radius jets, and classification is performed in two dijet invariant mass (𝑚 jj ) regions,
each with a trigger: 𝑚 jj < 1 TeV events use a dedicated emerging-jet trigger that exploits the jet’s
prompt track 𝑝 T fraction (PTF), while 𝑚 jj > 1 TeV events use a high-𝑝 T single-jet trigger. Dark
pion proper decay lengths between 1 and 1000 mm are considered, ensuring that most decays occur
within the inner detector. The dominant background from QCD multijet events is estimated using
two independent data-driven methods, corresponding to each tagging strategy.
The cut-based analysis identifies emerging jets using their displaced and multi-pronged structure. In both low- and high-𝑚 jj regions, the leading and subleading jets must each contain at least
one displaced vertex (DV). In the high- 𝑚 jj region, PTF and the 2-point energy correlation function
(ECF2)[13], which measures the jet’s angular energy dispersion, are used to select multi-pronged
emerging jets. In the low-𝑚 jj region, where PTF is already constrained by the emerging jet trigger,
selection is based on number of sub-jets within the large-radius jet. The background yield in the
signal region is estimated using the ABCD method.
The ML based strategy uses a transformer-based jet tagger, based on the ATLAS GN2 flavour
tagging algorithm [14], which takes features from the jet and up to 200 associated tracks. The
model simultaneously optimises three tasks: classifying the jet as emerging or not, identifying track
origins, and predicting whether track pairs originate from the same vertex. The jet classification
score is used to tag emerging jet candidates, with a high threshold defining the signal region. Events
with two or more tagged jets define the signal region. Correlations between jet features make the
standard ABCD method unsuitable for background estimation. Instead, a data-driven approach
based on the mistag rate - or, the probability of a background jet being tagged as signal - is used.
The mistag rate is measured in the control regions and parameterised in two dimensional bins of
the dominant correlated jet properties, 𝑝 T and PTF. These mistag rates are then used to predict the
background yield in the signal region.
No significant excess above the expected background is observed. Figure 1 shows the 95%
confidence level upper limits as a function of mediator mass or dark pion lifetime (𝑐𝜏𝜋D ). In the
𝑠-channel, limits are strongest in the high-𝑚 jj region, while the 𝑡-channel, they are less dependent
on the mediator mass due to a weaker correlation between the mediator mass and 𝑚 jj . Overall, the
ML-based approach achieves stronger exclusion limits, including in the 𝑡-channel scenario, which
was not included in training, demonstrating the ability of the transformer based tagger to generalise
to processes it was not trained on. 𝑍 ′ masses are excluded up 2.5 TeV (for coupling values of
𝑔𝑞 = 0.01 and 𝑔𝑞D = 0.1), and Φ masses are excluded up to 1350 GeV (for a quark-dark quark
coupling value of 0.1).

3. Search for events with one displaced vertex from long-lived neutral particles
decaying into hadronic jets in the muon spectrometer
The ATLAS Collaboration searched for a single displaced vertex in the muon spectrometer
√
(MS) [15] using 140 fb −1 of proton–proton collision data at 𝑠 = 13 TeV, recorded during the
LHC 2015–2018 data-taking period. The analysis is interpreted in the context of scalar portal, dark
2

## PDF page 3

Danielle Wilson-Edwards

10

10

3

Obs. limit (cut-based)
Exp. limit ±1 (cut-based)
Obs. limit (ML-based)
Exp. limit ±1 (ML-based)
gq = 0.005, gqD = 0.1
gq = 0.01, gqD = 0.1

s = 13.6 TeV, 51.8 fb 1
m D = 10 GeV, c D = 50 mm

2

10

1

10

0

10

ATLAS

1

500

1000

1500

2000

2500

3000

95% CL upper limit on (pp qDqD) [fb]

95% CL upper limit on (pp Z ′) × BR(Z ′ qDqD) [fb]

Searches for unusual signatures from dark sectors with ATLAS

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

Obs. limit (cut-based)
Exp. limit ±1 (cut-based)
Obs. limit (ML-based)
Exp. limit ±1 (ML-based)

s = 13.6 TeV, 51.8 fb 1
m D = 10 GeV, c D = 50 mm

11 = 12 = 13 = 0.1

10

1

10

2

3500

600

mZ [GeV]

800

1000

1200

1400

1600

1800

′

10

3

10

2

10

1

10

0

s = 13.6 TeV, 51.8 fb 1
m D = 10 GeV, mZ = 1500 GeV
′

(b) 𝑡-channel, 𝑐𝜏𝜋D = 50 mm
95% CL upper limit on (pp qDqD) [fb]

95% CL upper limit on (pp Z ′) × BR(Z ′ qDqD) [fb]

(a) 𝑠-channel, 𝑐𝜏𝜋D = 50 mm
ATLAS

Obs. limit (cut-based)
Exp. limit ±1 (cut-based)
Obs. limit (ML-based)
Exp. limit ±1 (ML-based)
gq = 0.005, gqD = 0.1
gq = 0.01, gqD = 0.1

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

10
10

0

10

1

10

2

2000

m [GeV]

10

3

ATLAS

s = 13.6 TeV, 51.8 fb 1
m D = 10 GeV, m = 1500 GeV

11 = 12 = 13 = 0.1

1

10

c D [mm]

Obs. limit (cut-based)
Exp. limit ±1 (cut-based)
Obs. limit (ML-based)
Exp. limit ±1 (ML-based)

0

10

1

10

2

10

3

c D [mm]

(d) 𝑡-channel, 𝑚 Φ = 1500 GeV

(c) 𝑠-channel, 𝑚 𝑍 ′ = 1500 GeV

Figure 1: The 95% CL exclusion limits on (a, c) 𝜎(𝑞𝑞 → 𝑍 ′ ) × Br(𝑍 ′ → 𝑞 D 𝑞 D ) and (b, d) 𝜎( 𝑝 𝑝 → 𝑞 D 𝑞 D )
for 𝑚 𝜋D = 10 GeV [11]. The cut-based and ML-based strategies are shown in triangles and circles,
respectively. Theoretical cross-section predictions are shown as solid lines.

photon, axion-like particle (ALP), and baryogenesis models, while remaining broadly sensitive
to other long-lived particle scenarios. The search is divided into two orthogonal channels, each
with a dedicated trigger strategy to targeting events with and without associated prompt 𝑍 boson
production.
Events without an associated 𝑍 boson, referred to as the “muon-RoI” channel, are selected using
a dedicated Muon RoI Cluster HLT trigger [19]. This channel primarily targets scalar portal [7] and
baryogenesis [16] models. In the scalar portal model, a Higgs (𝐻) or alternative scalar boson (Φ)
produces two dark scalars (𝑠), which subsequently decay to SM fermions (Φ/𝐻 → 𝑠𝑠 → 𝑓 𝑓¯ 𝑓 𝑓¯).
In the baryogenesis model, a weak-scale particle 𝜒 couples to the SM via a scalar Φ that mixes
with the Higgs. 𝜒 is pair produced through 𝑝 𝑝 → 𝐻 → 𝜒 𝜒 and decays into three SM fermions,
violating baryon or lepton number and generating the baryon asymmetry.
Events with an associated 𝑍 boson, referred to as the “lepton-triggered” channel, are selected
using single- or di-lepton triggers [20, 21] and primarily target the ALP [17] model. In this scenario,
a long-lived ALP 𝑎 is produced via an off-shell 𝑍 boson, 𝑝 𝑝 → 𝑍 ∗ → 𝑍𝑎, with 𝑎 → 𝑔𝑔, and
𝑍 → 𝑙 + 𝑙 − (𝑙 = 𝑒, 𝜇). This channel is also sensitive to the dark photon [18] model, where a scalar
Φ decays into a 𝑍 boson and a long-lived dark photon 𝑍D , i.e. 𝑝 𝑝 → Φ → 𝑍 𝑍D , with 𝑍D → 𝑞 𝑞¯
and 𝑍 → 𝑙 + 𝑙 − (𝑙 = 𝑒, 𝜇). It further probes the 𝑍-associated scalar portal model, which extends the
original scalar portal scenario by including an additional 𝑍 boson. The associated 𝑍 helps reduce
backgrounds, although the production cross-section is generally smaller.
The dominant background for LLP decays in the MS arises from hadronic or electromagnetic
showers escaping the calorimeter, known as punch-through jets. Additional contributions come
from multijet events with mismeasured energy or direction, as well as non-collision sources such
as detector noise, cosmic rays, and beam-induced activity. In the muon-RoI channel, these back3

## PDF page 4

Danielle Wilson-Edwards

Searches for unusual signatures from dark sectors with ATLAS

10−2
10−3
10−4

BH→ ss = 1%

BH→ ss = 0.1%
Exp. ±1σexp

ATLAS

Obs.

mH,ms = [125,35] GeV
s=13 TeV, 140 fb-1

10−5 −2
10

10−1

Channel

Two DV
One DV
One DV + two DV

1
10
102
103
Scalar proper decay length (cτ) [m]

(a) Scalar portal

1

10−1

10−2

ma = 40 GeV

ATLAS

This work

-1

10−3 −4
10

10

d

BH→ ss = 10%

10

95% CL upper limit on σ × BZ → ff [pb]

1
−1

95% CL upper limit on σ × Ba → gg [pb]

95% CL upper limit on (σ/ σggF) × BH → ss

grounds are suppressed through isolation requirements, thresholds on missing transverse energy
and hadronic energy, and a minimum number of muon segments to reject non-collision events. In
the lepton-triggered channel, the 𝑍 selection significantly reduces punch-through and non-collision
backgrounds, leaving 𝑍+ jets as the dominant source. Consequently, looser isolation criteria are
applied, along with a threshold on missing transverse energy.
Since no reliable simulation exists for all backgrounds in the MS, a data-driven ABCD method
is used. The ABCD planes are defined by two multilayer perceptron (MLP) neural networks
(NN) trained on distinct input features: NN1 targets DV isolation and suppression of non-collision
backgrounds, while NN2 uses input features to target the DV’s characteristics. Separate networks are
trained for the barrel and endcap regions to account for differences in magnetic field conditions and
background behaviour. Vertex reconstruction efficiency is higher in the endcaps due to straight-line
tracklet fitting in the weak magnetic field, though this also reduces background rejection compared
to the curvature-based reconstruction in the barrel. The NN1 and NN2 outputs define the ABCD
planes used for data-driven background estimation in both detector regions.
No significant excess above the expected background is observed in the signal regions. Figure
2a shows the expected and observed limits from this one-DV search, the previous ATLAS two-DV
search [22], and their combination for the scalar portal benchmark with the SM Higgs boson and
𝑚 𝑠 = 35 GeV. The two-DV search, which has very low background, provides the best sensitivity
for lifetimes of O (10) m, while the one-DV search extends coverage to both shorter and longer
lifetimes. For the SM Higgs boson portal, branching fractions above 1% are excluded at 95% CL for
LLP proper decay lengths between 5 cm and 40 m. Figure 2b compares the expected and observed
limits from this search with previous ATLAS displaced jet [24] and inner-detector DV [23] searches,
showing this analysis sets the most stringent ATLAS limits to date for proper decay lengths above
O (10−1 ) m. Figure 2c shows the limits set on the cross-section times branching fraction for dark
photons decaying to fermion pairs.

s=13 TeV, 140 fb

JHEP 11 (2024) 036

Obs. (solid) & Exp. (dashed)

PRL 133 (2024) 161803

10−3

10−2

10−1
1
10
102
103
ALP proper decay length (c τ) [m]

(b) 𝑍+ ALP

1
−1

10

mΦ, mZ [GeV]
d

125, 5

10−2
10−3

ATLAS

125, 15

s=13 TeV, 140 fb-1

250, 50

Observed limit

250, 100

10−1

1
10
102
Dark photon proper decay length (cτ) [m]

(c) Dark photon

Figure 2: Summary of the expected and observed 95% CL upper limits for the Φ/𝐻 → 𝑠𝑠 model [15]. (a)
Comparison of the one DV [15] and two DV [22] results and their combined limits on (𝜎/𝜎𝑔𝑔𝐻 ) × 𝐵 for
the Higgs-portal mediator with 𝑚 𝑠 = 35 GeV. (b) Upper limits on the 𝑍+ALP production cross-section for
𝑚 𝑎 = 40 GeV compared with previous limits from [24] and [23]. (c) Observed 95% CL upper limits on
𝜎 × 𝐵(𝑍D → 𝑓 𝑓¯) for the dark photon 𝑍D model.

4. Summary
These proceedings summarise two recent ATLAS searches for dark sectors with unconventional
signatures at the LHC. Results are presented from the first search for emerging jet pair production
via a vector mediator, 𝑍 ′ , as well as for emerging jets produced through the t-channel exchange of
a scalar mediator, Φ. The second search targets a single displaced vertex in the muon spectrometer,
4

## PDF page 5

Searches for unusual signatures from dark sectors with ATLAS

Danielle Wilson-Edwards

improving or extending limits for the Higgs-portal and axion-like particle models compared to
previous ATLAS results. The ATLAS Collaboration has ongoing efforts to continue exploring
the vast phenomenological space that dark sectors present, seeking to leverage the Run-2 and
forthcoming full Run-3 datasets.

References
[1] D. Clowe et al., Astrophys. J. 648 (2006) L109.
[2] V.C. Rubin et al., Astrophys. J. 238 (1980) 471.
[3] M. Persic et al., Mon. Not. Roy. Astron. Soc. 281 (1996) 27, arXiv:astro-ph/9506004.
[4] DES Collaboration, Mon. Not. Roy. Astron. Soc. 475 (2018) 3165, arXiv:1708.01535 [astroph.CO].
[5] Planck Collaboration, Astron.Astrophys. 652 (2021) C4, arXiv:1807.06209 [astro-ph.CO].
[6] M.J. Strassler et al., Phys. Lett. B 651 (2007) 374, arXiv:hep-ph/0604261.
[7] M.J. Strassler et al., Phys. Lett. B 661 (2008) 263, arXiv:hep-ph/0605193.
[8] T. Han et al., JHEP 07 (2008) 008, arXiv:0712.2041 [hep-ph].
[9] ATLAS Collaboration, JINST 3 (2008) S08003.
[10] L. Evans et al., JINST 3 (2008) S08001, .
[11] ATLAS Collaboration, Rept. Prog. Phys. 88 (2025) 097801, arXiv:2505.02429 [hep-ex].
[12] P. Schwaller et al., JHEP 05 (2015) 059, arXiv:1502.05409 [hep-ph].
[13] A.J. Larkoski et al., JHEP 06 (2013) 108, arXiv:1305.0007 [hep-ph].
[14] ATLAS Collaboration, arXiv:2505.19689 [hep-ex] (2025).
[15] ATLAS Collaboration, arXiv:2503.20445 [hep-ex] (2025).
[16] Y. Cui et al., JHEP 02 (2015) 049, arXiv:1409.6729 [hep-ph].
[17] I. Brivio et al., Eur. Phys. J. C 77 (2017) 5111, arXiv:1701.05379 [hep-ph].
[18] H. Davoudiasl et al., Phys. Rev. D 85 (2012) 115019, arXiv:1203.2947 [hep-ph].
[19] ATLAS Collaboration, JINST 8 (2013) P07015, arXiv:1305.2284 [hep-ex].
[20] ATLAS Collaboration, JINST 15 (2020) P09015, arXiv:2004.13447 [physics.ins-det].
[21] ATLAS Collaboration, Eur. Phys. J. C 80 (2020) 47, arXiv:1909.00761 [hep-ex].
[22] ATLAS Collaboration, Phys. Rev. D 106 (2022) 032005, arXiv:2203.00587 [hep-ex].
[23] ATLAS Collaboration, Phys. Rev. Lett. 133 (2024) 161803, arXiv:2403.15332 [hep-ex].
[24] ATLAS Collaboration, JHEP 11 (2024) 036, arXiv:2407.09183 [hep-ex].
5
