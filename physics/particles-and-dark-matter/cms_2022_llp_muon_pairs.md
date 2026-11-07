Source: https://arxiv.org/abs/2205.08582v2
PDF sha256: 1015f0fe92efe4b5a221de272e3e49104a9aca33add9ad8e1075c9f4af537fab
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of cms_2022_llp_muon_pairs.pdf

Transcription of `cms_2022_llp_muon_pairs.pdf` in this directory, 54 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 2, 36 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories; pages 1, 3-35, 37-54 from the PDF's own text layer (pdftotext version 26.10.0, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

EUROPEAN ORGANIZATION FOR NUCLEAR RESEARCH (CERN)

CERN-EP-2022-080
2023/06/22

CMS-EXO-21-006

arXiv:2205.08582v2 [hep-ex] 4 Jun 2023

Search for long-lived particles decaying
√ to a pair of muons
in proton-proton collisions at s = 13 TeV
The CMS Collaboration*

Abstract
An inclusive search for long-lived exotic particles decaying to a pair of muons is presented. The search uses data √
collected by the CMS experiment at the CERN LHC
in proton-proton collisions at s = 13 TeV in 2016 and 2018 and corresponding to
an integrated luminosity of 97.6 fb−1 . The experimental signature is a pair of oppositely charged muons originating from a common secondary vertex spatially separated from the pp interaction point by distances ranging from several hundred µm to
several meters. The results are interpreted in the frameworks of the hidden Abelian
Higgs model, in which the Higgs boson decays to a pair of long-lived dark photons
Z D , and of a simplified model, in which long-lived particles are produced in decays
of an exotic heavy neutral scalar boson. For the hidden Abelian Higgs model with
m(Z D ) greater than 20 GeV and less than half the mass of the Higgs boson, they provide the best limits to date on the branching fraction of the Higgs boson to dark photons for cτ (Z D ) (varying with m(Z D )) between 0.03 and ≈0.5 mm, and above ≈0.5 m.
Our results also yield the best constraints on long-lived particles with masses larger
than 10 GeV produced in decays of an exotic scalar boson heavier than the Higgs boson and decaying to a pair of muons.

Published in the Journal of High Energy Physics as doi:10.1007/JHEP05(2023)228.

© 2023 CERN for the benefit of the CMS Collaboration. CC-BY-4.0 license
* See Appendix A for the list of collaboration members

## PDF page 2



## PDF page 3

1

1

Introduction

Long-lived particles (LLPs) are predicted by many extensions of the standard model (SM), in
particular by various supersymmetric scenarios [1, 2] and “hidden sector” models [3, 4]. Such
particles could manifest themselves through decays to SM particles at macroscopic distances
from the proton-proton (pp) interaction point (IP).
This paper describes an inclusive search for an exotic massive LLP decaying to a pair of oppositely charged muons, referred to as a “displaced dimuon”, that originates from a common
secondary vertex spatially separated from the IP. The search is based on an analysis of pp collisions
corresponding to an integrated luminosity of 97.6 fb−1 collected with the CMS detector at
√
s = 13 TeV during Run 2 of the CERN LHC. A minimal set of requirements and loose event
selection criteria allow the search to be sensitive to a wide range of models predicting LLPs that
decay to final states that include a pair of oppositely charged muons. We interpret the results
of the search in the framework of two benchmark models: the hidden Abelian Higgs model
(HAHM), in which displaced dimuons arise from decays of hypothetical dark photons [5], and
a simplified model, in which a non-SM Higgs boson decays to a pair of long-lived exotic heavy
neutral scalar bosons, at least one of which decays into a pair of muons [6].
The present search explores the LLP mass range above 10 GeV accessible with the Run 2 dimuon
triggers and is sensitive to secondary vertex displacements ranging from several hundred µm
to several meters.
√ It is a continuation and extension of two CMS analyses performed using
data taken at s = 8 TeV during Run 1 of the LHC. One analysis was dedicated to a search
for LLPs decaying to two electrons or two muons in the tracker [7]; the other looked for LLP
decays to final states containing two muons reconstructed only in the muon system [8]. The
analysis of the Run 2 data described here contains numerous improvements over these Run 1
searches, notably in refined event selection and improved background evaluation procedures.
It also benefits
√ from an increase in integrated luminosity by almost a factor of five, collected
at a higher s. A search for LLPs decaying to displaced dimuons has also been performed
by the ATLAS Collaboration, using 2016 data corresponding to an integrated luminosity of
32.9 fb−1 [9].
This paper is organized as follows. Section 2 describes the CMS detector. Section 3 presents
the signal models as well as the samples analyzed from data and from the Monte Carlo simulation. Section 4 describes the analysis strategy, the triggers, and the offline event selection.
Estimation of backgrounds and the associated systematic uncertainties are described in Section 5. Section 6 summarizes the systematic uncertainties affecting signal efficiencies. Section 7
describes the results obtained in the individual dimuon categories and their combination. The
analysis summary is presented in Section 8. Tabulated results and supplementary material for
reinterpreting the results in the framework of models not explicitly considered in this paper are
provided in HEPData [10].

2

The CMS detector

The central feature of the CMS detector is a superconducting solenoid of 6 m internal diameter,
providing a magnetic field of 3.8 T. Within the solenoid volume are a silicon pixel and strip
tracker extending outwards to a radius of 1.1 m, a lead tungstate crystal electromagnetic calorimeter, and a brass and scintillator hadron calorimeter, each composed of a barrel and two
endcap sections. Forward calorimeters extend the coverage in pseudorapidity η provided by
the barrel and endcap detectors. Muons are detected in gas-ionization chambers covering the
range |η | < 2.4 and embedded in the steel flux-return yoke outside the solenoid. The muon

## PDF page 4

2
system is composed of three types of chambers: drift tubes (DTs) in the barrel, cathode strip
chambers (CSCs) in the endcaps, and resistive-plate chambers in both the barrel and the endcaps. The chambers are assembled into four “stations” at increasing distance from the IP; each
station provides reconstructed hits in several detection planes, which are combined into track
segments, forming the basis of muon reconstruction in the muon system [11]. A more detailed
description of the CMS detector, together with a definition of the coordinate system used and
the relevant kinematic variables, can be found in Ref. [12].
Events of interest are selected using a two-tiered trigger system. The first level (L1), composed
of custom hardware processors, uses information from the calorimeters and muon detectors
to select events at a rate of approximately 100 kHz within a fixed time interval of less than
4 µs [13]. The second level, known as the high-level trigger (HLT), consists of a farm of processors running a version of the full event reconstruction software optimized for fast processing,
and reduces the event rate to about 1 kHz before data storage [14].

3

Signal models, data and simulated samples

√
The search is performed using pp collision data collected at s = 13 TeV in 2016 and 2018
corresponding to integrated luminosities of 36.3 ± 0.4 and 61.3 ± 1.5 fb−1 , respectively [15, 16].
The data collected in 2017 are not used because the triggers required for the analysis were not
included when those data were recorded.
As mentioned above, two signal models with different final-state topologies and event kinematics are used in the optimization of event selection criteria and in the interpretation of results. The first belongs to a class of models featuring a “hidden” or “dark” sector of matter
that does not interact directly with SM particles, but can manifest itself through mixing effects.
This HAHM benchmark contains an extra dark U(1)D gauge group whose symmetry is broken
by a new dark Higgs field [5, 17]. The spin-1 mediator of the U(1)D group, known as the dark
photon Z D , mixes kinetically with the hypercharge SM gauge boson (“vector portal”), whereas
the dark Higgs boson H D mixes with the SM Higgs boson H (“Higgs portal”) and gives mass
m(Z D ) to the dark photon. If there are no hidden-sector states with masses smaller than m(Z D ),
the mixing through the vector portal with the SM photon and Z boson causes the dark photon
to decay exclusively to SM particles, with a sizable branching fraction to leptons. Pair production of the Z D via the Higgs portal with subsequent decays of dark photons via the vector
portal is shown in Fig. 1 (left).
The present search probes the regime of m(Z D ) > 10 GeV with small values of the Z–Z D kinetic mixing parameter ϵ [5]. In this regime, the dark photon is long-lived, since its mean proper
lifetime τ (Z D ) is proportional to ϵ−2 . In particular, the dark photon with 10 GeV ≲ m(Z D ) <
m(H )/2 is expected to have macroscopically large mean proper decay lengths cτ (Z D ) ≳ O(100 µm)
for ϵ < O(10−6 ). The Z D production rate is governed by the branching fraction B(H → Z D Z D ),
which does not depend on ϵ but is proportional to the square of κm2 (H )/|m2 (H ) − m2 (H D )|,
where κ is the H–H D mixing parameter. Since κ and m(H D ) affect only the overall dark photon production rate, sampling of m(Z D ) and ϵ is sufficient to explore different kinematical and
topological scenarios of the model. We generated a set of 24 HAHM samples with m(Z D ) between 10 and 60 GeV and ϵ between 10−6 and 2 × 10−9 . In this mass range, the model’s prediction for B(Z D → µµ ) varies between 15.4% at m(Z D ) = 10 GeV and 10.7% at m(Z D ) = 60 GeV.
The dark Higgs boson is assumed to be heavy enough such that H → H D H D decays are kinematically forbidden. In the sample generation, we specify m(H D ) = 400 GeV and κ = 0.1.
The production of dark photons is modeled at leading order by M AD G RAPH5 aMC @ NLO [18]

## PDF page 5

3

µ̄

H

ZD

κ
HD

ZD

µ̄

µ

X

µ

Φ

f̄

f

X

f̄

f

Figure 1: Feynman diagrams for (left) the HAHM model, showing the production of long-lived
dark photons Z D via the Higgs portal, through H–H D mixing with the parameter κ, with subsequent decays via the vector portal; and (right) the heavy-scalar model with Φ boson decaying
to a pair of long-lived bosons X. The symbols f and f represent, respectively, fermions and antifermions lighter than half the LLP mass.
version 2.4.2. The generation of the samples is done for the dominant gluon-fusion production
mechanism. The Higgs boson production cross section is normalized to the most recent theoretical prediction for the sum of all production modes for m(H ) = 125 GeV, 55.7 pb [19]. The
decays of the dark photons are modeled by PYTHIA 8.212 and 8.230 [20] in samples corresponding to the 2016 and 2018 data sets, respectively.
At the LHC, another way that LLPs might arise is via production of mediators heavier than
the Higgs boson that decay into LLPs. To explore ranges of kinematic variables and event
topologies broader than those offered by HAHM, we also consider a simplified benchmark
model [6], previously used in Run 1 searches for displaced dimuons [7, 8], in which the LLP
is an exotic spin-0 boson X. The scalar X has a non-zero branching fraction to dimuons and is
pair produced in the decay of a new heavier scalar boson Φ, which is produced in gluon-gluon
fusion: gg → Φ → XX, X → µ + µ − . The Feynman diagram for this process is shown in Fig. 1
(right).
The samples for Φ → XX are generated with PYTHIA. Two sets of samples are produced, depending on whether one or both X bosons are forced to decay to dimuons. Samples in each set
are generated with different combinations of Φ boson masses m(Φ) (ranging from 125 GeV to
1 TeV) and X boson masses m(X ) (ranging from 20 to 350 GeV). The width of the Φ boson is assumed to be small for the purpose of simulation, but the analysis has negligible dependence on
this assumption. Each sample is furthermore produced with three different mean proper lifetimes τ (X ) of the X bosons, corresponding to mean transverse decay lengths of approximately
3, 30, and 250 cm. Events generated at the selected values of m(Φ), m(X ), and τ (X ) allow us to
study wide ranges of signal displacements, kinematical variables, and event topologies.
Since the optimization of the event selection criteria and the evaluation of the residual backgrounds are performed using data, the simulated background samples are used primarily to
gain a better understanding of the nature and composition of surviving background events.
Simulated background samples used in the analysis include Drell–Yan (DY) dilepton production; tt, tW, and tW events; W and Z boson pair production (dibosons); W+jets; and events
comprised of jets produced through the strong interaction that are enriched in muons from
semileptonic decays of hadrons containing b or c quarks.
The 2016 simulated signal and background samples are produced with either the NNPDF2.3

## PDF page 6

4
(leading order) or NNPDF3.0 (next-to-leading order) parton distribution functions (PDFs) [21],
using the CUETP8M1 [22] tune to model the underlying event. All 2018 simulated samples are
produced with the NNPDF3.1 PDFs [23] (next-to-next-to-leading order), using the CP5 [24]
tune, which is optimized for the NNPDF3.1 PDFs. Simulation of the passage of particles
through detector material is performed by G EANT 4 [25]. Simulated minimum bias events are
superimposed on a hard interaction in simulated events to describe the effect of additional inelastic pp interactions within the same or neighboring bunch crossings, known as pileup; the
samples are weighted to match the pileup distribution observed in data. All simulated events
are then reconstructed with the same algorithms as used for data.

4

Analysis strategy and event selection

An LLP produced in the hard interaction of the colliding protons may travel a significant distance in the detector before decaying into muons. While trajectories of the muons produced
well within the silicon tracker can be reconstructed by both the tracker and the muon system,
tracks of muons produced in the outer tracker layers or beyond can only be reconstructed by
the muon system. Since the dimuon vertex resolution and the background composition differ
dramatically depending on whether the muon is reconstructed in the tracker, we classify all
reconstructed dimuon events into three mutually exclusive categories: a) both muons are reconstructed using both the tracker and the muon system (TMS-TMS category); b) both muons
are reconstructed using only the muon system, as “standalone” muons (STA-STA category);
and c) one muon is reconstructed only in the muon system, whereas the other muon is reconstructed using both the tracker and the muon system (STA-TMS category). These three categories of events are analyzed separately, each benefiting from dedicated event selection criteria
and background evaluation. The results in each category are statistically combined to provide
the final results.
The beamspot is identified with the mean position of the pp interaction vertices. The primary vertex (PV) is taken to be the vertex corresponding to the hardest scattering in the event,
evaluated using tracking information alone, as described in Section 9.4 of Ref. [26]. A pair of
reconstructed muon tracks is fitted to a common vertex (CV), which is expected to be displaced
with respect to the PV. The transverse decay length Lxy is defined as the distance between the
PV and the CV in the plane transverse to the beam direction. The transverse impact parameter
d0 is defined as the distance of closest approach (DCA) of the muon track in the transverse
plane with respect to the PV.
Events were collected with dedicated triggers aimed at recording dimuons produced both
within and outside of the tracker. Therefore, these triggers require two muons reconstructed in
the muon system alone, without using any information from the tracker, and do not impose the
beamspot constraint in the muon track fit at the HLT [27]. Each muon is required to be within
the region |η | < 2.0 and to have transverse momentum magnitude pT > 28(23) GeV in 2016
(2018) data taking. To reduce the trigger rate caused by hadron punch-through and poorly
measured muons, each muon track is required to be composed of segments found in two or
more muon stations. To reduce the contribution to the trigger rate from cosmic ray muons and
low-mass dimuon resonances, the trigger used to collect 2016 data also required that the 3D
angle between the muons be less than 2.5 rad, and that the invariant mass of the two muons
be larger than 10 GeV. The optimization of the online selection prior to the 2018 data taking
made it possible to remove these two requirements from the 2018 trigger, thus providing additional validation regions for background evaluation and increasing the signal efficiency. The
efficiency of triggering on signal events in 2018 was further improved by complementing the

## PDF page 7

5
above trigger with one very similar to it, but using a modified version of the initial “seeding”
stage of the muon trajectory building at the HLT. The seed generator used in the new trigger
was specifically designed for muons not pointing to the beamspot and helped to increase the
reconstruction efficiency for displaced muons.

1.4
1.2
1

CMS

Data

Cosmic ray muon data

Efficiency

Efficiency

The high-level triggers used in the analysis were seeded by L1 dimuon triggers that required
the pT of the muons to be above certain thresholds. The values of the thresholds were varied
during the data taking, depending on the instantaneous luminosity, from 11 and 4 GeV (for the
leading and subleading L1 muons, respectively) during most of 2016, to 15 and 7 GeV at the end
of Run 2. At L1, the pT assignment for muons was made under the assumption that the muons
originated at the beamspot. As a result, the pT of the displaced muons not pointing to the
beamspot were underestimated and could fall below the L1 trigger thresholds. The ensuing
signal efficiency loss was larger when higher L1 trigger pT thresholds were used. Since this
effect is decoupled from the collision environment (e.g., instantaneous luminosity), it can be
studied using cosmic ray muons recorded with very loose triggers during periods with no
beam. Figure 2 shows that the decrease in the L1 muon trigger efficiency as a function of the
impact parameter d0 for various L1 trigger pT thresholds used in 2016 (left) and 2018 (right) is
well reproduced by the signal simulation in the barrel.
pSTA > 33 GeV, 2016 pL1 thresholds
T
T
L1
(p > 4 GeV)
→XX (pL1 > 4 GeV)
T
T
L1
L1

Data (p > 11 GeV)
T

φ
φ→XX (p > 11 GeV)
T

1.4
1.2
1

0.8

0.8

0.6

0.6

0.4

0.4

0.2
0
0

CMS

Data

Cosmic ray muon data
pSTA > 28 GeV, 2018 pL1 thresholds
T
T
L1
(p > 7 GeV)
→XX (pL1 > 7 GeV)
T
T
L1
L1

Data (p > 15 GeV)
T

φ
φ→XX (p > 15 GeV)
T

0.2
20

40

60

80

100

d0 [cm]

0
0

20

40

60

80

100

d0 [cm]

Figure 2: L1 muon trigger efficiency in cosmic ray muon data (blue) and signal simulation
(red) as a function of d0 , for the L1 trigger pT thresholds used in (left) 2016 and (right) 2018.
The denominator in the efficiency calculations is the number of STA muons with |η | < 1.2 and
pT > 33 (28) GeV in 2016 (2018).
As noted in Section 1, no single muon reconstructor provides optimal performance over the
wide range of displacements of secondary vertices considered in the analysis. Muons produced
near the IP can be accurately reconstructed by using commonly used algorithms developed for
prompt muons and combining measurements in the tracker and the muon system. Among
them are the global muon and tracker muon reconstruction algorithms [11, 28]. The first algorithm builds “global muons” by using hits in the tracker and segments in the muon system in
a common track fit. The second constructs “tracker muons” by propagating tracks in the inner
tracker to the muon system and requiring loose geometrical matching to DT or CSC segments.
The efficiency of these algorithms, however, rapidly decreases as the distance between the IP
and muon origin increases, dropping to zero for muons produced in the outer tracker layers
and beyond. On the other hand, such muons can still be efficiently reconstructed by algorithms
that use only information from the muon system. These STA algorithms [11, 28] can reconstruct
muons with displacements of up to a few meters, but they have poorer spatial and momentum
resolution than muons reconstructed using more precise information from the silicon tracker.

## PDF page 8

6
To benefit from the advantages offered by both types of algorithms and to follow what was
done in the trigger, we begin the muon selection with the most efficient standalone muons and
replace them with more accurately reconstructed global and tracker muons whenever such
muons are found. We use muons reconstructed by an STA algorithm with the beamspot constraints removed from all stages of the muon reconstruction procedure, which yields the highest efficiency and the best resolution for displaced muons, out of all available STA algorithms.
The event selection starts with the requirement that the event is selected by the triggers described above and has at least two STA muons, each containing more than 12 valid CSC or
DT hits. The requirement of the minimal number of hits suppresses backgrounds from hadron
punch-through and other sources, and ensures that the STA muons have acceptable pT resolution and charge assignment. The STA muons that satisfy this basic quality requirement form
the initial list of the muon candidates retained for the analysis.
Next, we reject events in which no HLT muon pair that triggered the event matches two STA
muons in the list. This requirement suppresses events that triggered on muons not related to
the signal and facilitates application of trigger efficiency measurements in the analysis. We
then attempt to match each STA muon in the list with a TMS muon, i.e., a global or a tracker
muon. The STA and TMS muons are considered to be matched if
√they share at least two thirds
of their segments or if ∆RSTA−TMS < 0.1, where ∆RSTA−TMS = (ηhit − ηpca )2 + (ϕhit − ϕpca )2
is the separation between ηhit (ϕhit ) of the position of the innermost hit of the STA muon and
ηpca (ϕpca ) of the point of closest approach of the TMS muon to this hit. If an associated TMS
muon is found, it replaces the corresponding STA muon in the list of the muon candidates used
for further analysis; otherwise, the original STA muon is kept. The matching procedure was
optimized using events in the simulated signal and background samples as well as data in the
signal-free control regions discussed in Section 5. It eliminates most of the pp collision background to LLP decays outside of the tracker and greatly increases sensitivity to LLP decays in
the tracker, thanks to a far superior resolution of TMS muons compared to that of STA muons.
The impact of the STA-to-TMS muon association procedure on the event selection is further
illustrated in Fig. 3, which shows the fraction of simulated Φ → XX → µµ+anything signal
events with zero, one, and two STA muons matched to TMS muons as a function of Ltrue
xy , defined as the transverse distance between the simulated positions of the hard-interaction and
LLP decay vertices. While almost all dimuons produced close to the IP have both STA muons
matched to TMS muons, the fraction of these events rapidly decreases with Ltrue
xy , reflecting
true
the dependence on Lxy of the tracker reconstruction efficiency. Events with one STA muon
matched to a TMS muon start to dominate at Ltrue
xy = 25 cm and remain the dominant component up to ≈50 cm, where events with no STA-to-TMS matches take over. When LLPs decay
in the outer tracker layers or beyond the tracker, all STA-to-TMS associations are purely accidental and occur for fewer than 5% of the simulated signal muons. Therefore, the association
procedure gives rise to three categories of dimuons, each dominating in a certain Ltrue
xy range:
true
true
true
TMS-TMS at small Lxy , STA-TMS at intermediate Lxy , and STA-STA at large Lxy . The number of STA-STA dimuons beyond the solenoid, at Ltrue
xy > 3.2 m, is low because of the low trigger
efficiency.
The STA and TMS muons are then subjected to additional selection criteria optimized using
simulated signal and background samples, and samples of dimuons misreconstructed as displaced in the signal-free regions in data. The STA muons are required to have pT > 10 GeV and
to satisfy the following criteria:

• relative pT uncertainty σpT /pT < 1.0, where σpT is the internal uncertainty from the
muon track fit;

## PDF page 9

Fraction of dimuons by category

7

1

(13 TeV)

CMS Simulation

0.8
φ→XX→µµ+anything

0.6

TMS-TMS
STA-TMS
STA-STA

0.4
0.2
0
0

50

100

150

200

250

300

350

400

true
Lxy [cm]

Figure 3: Fractions of signal events with zero (green), one (blue), and two (red) STA muons
matched to TMS muons by the STA-to-TMS muon association procedure, as a function of true
Lxy , in all simulated Φ → XX → µµ+anything signal samples combined. The fractions are
computed relative to the number of signal events passing the trigger and containing two STA
muons with more than 12 muon detector hits and pT > 10 GeV matched to generated muons
from X → µµ decays.

• χ2 /dof of the muon track fit less than 2.5;
• more than 18 DT hits for muons reconstructed only in the barrel;
• time difference |∆t| with respect to the current bunch crossing less than 12 ns;
• muon identified as traveling outwards based on the timing measurements [11].
The σpT /pT , χ2 /dof, and DT hits requirements suppress background events arising from poorly
measured prompt muons and ensure acceptable pT resolution and charge assignment for signal muons. The muon timing requirement serves several purposes: it rejects events in which
the trigger timing is early, causing the tracker hits that are read out to be from unrelated pp
collisions 25 ns earlier and not to include any tracker hits of the triggering STA muons; it rejects
out-of-time collision muons; and it helps suppress background arising from cosmic ray muons
crossing the detector outside of the tracker acceptance, which are often reconstructed as two
STA muons with no associated TMS muons. The |∆t| < 12 ns requirement does not impact
signal efficiency in the studied mass range. The muon direction, determined using the muon
timing measurements, offers another handle for suppressing cosmic ray muon background by
identifying cosmic ray muons in the upper part of the detector, which travel inwards. We do
not impose any explicit requirements on the isolation of the STA muons, thus making the STASTA analysis sensitive to models predicting highly displaced b quarks, such as LLPs decaying
to bb.
The initial list of TMS muon candidates consists of the global and tracker muons with pT >
10 GeV that are matched to STA muons by the STA-to-TMS muon association procedure. These
TMS muon candidates are further required to satisfy the following criteria:

## PDF page 10

8

• σpT /pT < 1.0;
• be identified as tracker muons with two or more matched CSC or DT segments;
• be isolated from other activity in the event.
The first two requirements reject poorly measured muons and misidentified hadrons. The
isolation requirement suppresses copious background from dijet and multijet events. Specifically, we
p calculate the sum of the pT of other tracks reconstructed within a cone of radius

∆R = (∆η )2 + (∆ϕ)2 centered on the direction of the TMS muon track. Both the pT of the
muon track itself and the pT of the track of any other muon forming a dimuon (if it lies within
the cone) are not included in the sum. For the muon to be considered isolated, the relative
rel , defined as the ratio of the p sum in a cone of ∆R < 0.3 to the muon track
tracker isolation Itrk
T
pT , is required to be smaller than 0.075. The cone size, isolation threshold, and other parameters of the algorithm such as the minimum |∆z| between the reference point of the track and
that of the muon, are the result of the optimization procedure that uses displaced muons in the
simulated signal samples and background muons in the signal-free control regions in data.
Dimuon candidates are then formed from pairs of STA and TMS muons passing the above
muon selection criteria. All possible combinations of muons (STA-STA, STA-TMS, and TMSTMS) are considered. Each pair of selected muons with the distance of closest approach of
the muon tracks smaller than 15 cm is fit to a common vertex by means of the Kalman vertex fitter algorithm [29, 30] and forms a dimuon. If more than two muons pass the selection
criteria, multiple dimuons can be formed, including dimuons sharing one of the two muons;
this situation would be particularly common in signal events with two LLPs decaying to two
muons each. Using simulated signal samples, we developed a set of muon pairing criteria that
efficiently choose up to two dimuons among the formed dimuons. The selection is first done
separately in each of the three dimuon categories. In events with three selected muons, we
choose a dimuon with the lowest value of χ2 of the vertex fit, χ2vtx ; in events with four or more
selected muons, we choose the pair of dimuons whose χ2vtx sum is the smallest among all distinct pairs of dimuons formed from the four highest pT muons in the event. In rare cases, when
more than two dimuons are found in all categories combined, up to two dimuons with the
smallest χ2vtx are kept for further analysis; we also ensure that there are no STA or TMS muons
included in more than one dimuon. The efficiency of choosing the right dimuon is 85–95% for
4µ signal samples and close to 100% for 2µ samples.
To suppress background from dimuons formed from unrelated muons, the dimuons chosen
by the muon pairing criteria are required to have χ2 of the common vertex fit below a certain
threshold. Since χ2 distributions in data are difficult to reproduce accurately in the simulation,
the requirements on χ2vtx are chosen to be loose, leaving the signal efficiency almost intact while
rejecting a sizable fraction of background events in the control regions in data. The values of
the thresholds are determined separately in each of the dimuon categories and are χ2vtx < 10 in
the STA-STA and TMS-TMS categories, and χ2vtx < 20 in the STA-TMS category. To further ensure that the muon tracks are consistent with the vertex, we require that the number of tracker
hits assigned to the track of the TMS muon upstream of the vertex position does not exceed
2 in the TMS-TMS category and 5 in the STA-TMS category. In the TMS-TMS category, background from dimuons formed from unrelated or mismeasured muons is further suppressed by
requiring TMS muons forming the dimuon to have a similar number of pixel hits, namely that
the difference between the number of pixel hits on two TMS muons, ∆N (pixel hits), is smaller
than 3 hits.
A cosmic ray muon crossing the detector within the acceptance of the muon system is often
reconstructed as two back-to-back muons, one in the upper half and one in the lower half of

## PDF page 11

9
the detector. This background is very efficiently suppressed by requiring that the 3D opening
angle α between the two muons be less than a certain threshold value. In the analysis of 2016
data, we require α < 2.5 rad (or, equivalently, cos α > −0.8), consistent with the presence of
the cos α > −0.8 requirement in the 2016 version of the trigger. Since the 2018 version of the
trigger has no cos α requirement, the offline requirements on α in the analysis of 2018 data
are re-optimized in each of the dimuon categories separately, taking into account the angular
resolution of STA and TMS muons. As the result of this optimization, the 2018 selection criteria
are loosened to α < 2.7 rad (cos α > −0.9) for STA-STA and STA-TMS dimuons and to α <
3.0 rad (cos α > −0.99) for TMS-TMS dimuons.
The cos α requirements fail to reject one particular type of cosmic ray muon background occurring when a cosmic ray muon with a large incoming angle crosses the muon system diagonally
in the r-z plane. A cosmic ray muon of this type can lead to multiple STA muons, each reconstructed from a small number of segments. These poorly measured STA muons are not
necessarily back-to-back, and can give rise to a mistakenly formed displaced dimuon passing
the full event selection. To suppress such events, we reject STA-STA dimuons if the sum of the
numbers of segments belonging to the two muons, N(dimuon segments), is smaller than 5.
Furthermore, there are events with multiple cosmic ray muons produced in an atmospheric
shower. Such events typically result in a large number of nearly parallel STA muons reconstructed in both upper and lower halves of the detector. While dimuons formed from muons in
different hemispheres are rejected by the cos α requirement, dimuons formed from two muons
in the same hemisphere are not. To reject the background from cosmic ray muon showers,
we require that the event contain fewer than 4 nearly parallel STA muons and have at least
one reconstructed pp interaction vertex with more than 3 associated tracks and with transverse (longitudinal) coordinates within 2 (24) cm of the IP. In the STA-STA dimuon category, in
which the contribution from the cosmic ray muon showers is the largest, we also require that
neither of the two muons forming a dimuon be back-to-back (cos α < −0.9) with another STA
muon with pT > 10 GeV. The dimuon is rejected only if the time difference |∆tb2b | between
the muon in the dimuon and its back-to-back muon is larger than 20 ns, i.e., consistent with the
time difference between the two reconstructed parts of a cosmic ray muon. This requirement
also helps to suppress dimuons reconstructed from a cosmic ray muon and a muon from an
overlapping pp collision.
Displaced dimuons produced in decays of nonprompt J/ψ mesons and other low-mass SM resonances, or formed from the products of the b hadron cascade decays (b → cµ 1 X followed
by c → µ 2 X), are suppressed by requiring that the reconstructed dimuon invariant mass mµµ
be larger than 10 GeV. This requirement, applied in all three dimuon categories, also suppresses dimuons from decays of promptly produced low-mass SM resonances. However, lowpT muons can appear as muons with higher pT , with straighter tracks, when reconstructed
from a small number of measurements. This gives rise to dimuons with an overestimated mµµ
(above the 10 GeV threshold) and a mistakenly formed displaced vertex. To suppress such
events, we reject STA-STA dimuons whose separation in η is small (|∆ηµµ | < 0.1) if one of the
muons is reconstructed in the barrel from fewer than 25 DT hits or if N(dimuon segments) < 6.
In the other two dimuon categories, this background is suppressed by requiring that the hits
associated with each TMS muon populate a minimum number of tracker layers, N(tracker layers). This minimum number depends on Lxy and decreases from 6 for Lxy < 15 cm to 3 for
Lxy > 45 cm.
Another source of SM background events is prompt high-mass dimuons that are reconstructed
as displaced due to instrumental or reconstruction failures. Such dimuons mostly arise from

## PDF page 12

10
DY dimuon production; contributions from processes such as tt and diboson production are
relatively small. Events from DY ττ production with both τ leptons decaying to muons lead
to a background with characteristics similar to those of the mismeasured DY µµ events. An
important discriminating variable between signal and these backgrounds is the transverse
collinearity angle ∆Φ between p⃗T µµ of the dimuon system and L⃗xy . When a pair of muons
is produced in the decay of an LLP originating at the PV, both the resulting p⃗T µµ and L⃗xy point
away from the PV, and |∆Φ| is small. On the other hand, mismeasured prompt dimuons, in particular those arising from the DY process, are expected to have a |∆Φ| distribution symmetric
around π/2, because the directions of p⃗T µµ and L⃗xy are independent. We require |∆Φ| < π/4
in all three dimuon categories. The requirement is kept loose in order to preserve sensitivity to
signal models featuring LLPs that decay into a dimuon and a particle (or particles) escaping detection, such as neutrinos, dark matter particles, or lightest supersymmetric particles [31, 32].
We use the symmetric region |∆Φ| > 3π/4 as a control region for evaluating the contribution from DY and other prompt backgrounds, and the regions with π/4 < |∆Φ| < π/2 and
π/2 < |∆Φ| < 3π/4 for validating background predictions.
The last important source of SM backgrounds is dijet and multijet events yielding dimuons that
are formed from particles arising from different jets, either genuine muons or particles misidentified as muons. Such events contribute mainly to the TMS-TMS and STA-TMS categories and
are strongly suppressed by the isolation criteria applied to TMS muons, as well as by the requirement that at least one of the muons that form the TMS-TMS dimuon has pT > 25 GeV.
Furthermore, such events are expected to result in dimuons with both opposite-sign (OS) and
same-sign (SS) electric charges, each with a symmetric |∆Φ| distribution. Therefore, in addition to binning in |∆Φ|, we classify selected dimuons as OS or SS, based on the observed muon
charges. The signal selection requires that dimuons be OS, while SS dimuons constitute a control region used to evaluate backgrounds arising from dijet and multijet events, and from b
hadron cascade decays.
A class of background events peculiar to the STA-TMS category consists of dimuons with their
common vertex reconstructed on the wrong side of the PV relative to the direction of the TMS
momentum vector. Since the TMS muon is usually reconstructed much more precisely than the
STA muon, the reconstructed CV in STA-TMS events is usually located at or near the trajectory
of the TMS muon. With ϕµTMS defined as the angle between the TMS muon p⃗T and L⃗xy , the location of the CV along the TMS muon trajectory depends on the STA muon and can be situated
on either the correct side (|ϕµTMS | < π/2) or the wrong side (|ϕµTMS | > π/2) of the PV. We reject
events on the extreme wrong side (|ϕµTMS | ∼ π) by requiring |ϕµTMS | < 2.9.
Next, we require that the dimuons be displaced with respect to the primary vertex. This is
achieved by imposing requirements on the Lxy significance Lxy /σLxy and the muon d0 significance d0 /σd0 . The Lxy uncertainty σLxy is calculated by combining uncertainties in the transverse
positions of the CV and the PV; the d0 uncertainty σd0 includes both track and PV uncertainties. The optimal values of requirements on Lxy /σLxy and d0 /σd0 are chosen separately, for
each of the dimuon categories, by maximizing an approximate figure of merit for the expected
statistical significance of a discovery [33]. The expected number of signal events used for the
optimization is obtained from simulation, while the number of background events is estimated
from events in control regions in data using the procedures described in the next section. The
criteria applied to Lxy /σLxy and d0 /σd0 are:

• Lxy /σLxy > 6 in the STA-STA dimuon category;
• Lxy /σLxy > 6 and d0 /σd0 > 6 in the TMS-TMS dimuon category; and

## PDF page 13

11

• Lxy /σLxy > 3 and d0 /σd0 > 6 in the STA-TMS dimuon category.
In the STA-STA category, the analysis sensitivity does not increase appreciably for any requirement on the d0 significance once a requirement on Lxy /σLxy is in place; therefore, we do not
apply any selection on d0 /σd0 . In the TMS-TMS category, a requirement on d0 /σd0 is applied
to both muons and, since the residual background has a falling d0 /σd0 distribution, the signal
region is divided into three bins in the minimum of the two d0 /σd0 values, min(d0 /σd0 ): 6–10,
10–20, and >20. In the STA-TMS category, a requirement on d0 /σd0 is applied only to the TMS
muon, with no selection on d0 /σd0 of the STA muon. Since the Lxy resolution in the STA-TMS
category is of the order of a few cm, a requirement on Lxy /σLxy is kept loose to preserve good
gen

efficiency for events with 10 ≲ Lxy ≲ 60 cm, many of which are found in this category.
Table 1 summarizes the event, muon, and dimuon selection criteria used in the analysis.
Finally, to test for the existence of an LLP with a given mass, dimuons satisfying the selection
criteria are required to have mµµ within a specified interval containing the probed LLP mass.
The width of each interval is chosen according to the mass resolution and the expected background. The resulting intervals typically contain a large fraction (90–99%) of putative signal
with the probed mass. Since the mass resolution in the TMS-TMS category is far superior to
that in the other two categories (1–3% compared to 10–25%, for LLP masses between 20 and
350 GeV), the minimum width of mass intervals varies from 3 GeV in the TMS-TMS category to
≈20 GeV in the STA-STA category.
The signal efficiency is defined as the ratio of the number of simulated signal events in which
at least one dimuon candidate of any type passes all selection criteria (including the trigger)
to the total number of simulated signal events. The efficiencies are estimated for LLP lifetimes
corresponding to mean proper decay lengths in the range of 50 µm–1 km by reweighting events
in the available simulated signal samples. The maximum efficiency, which is attained in the
heavy-scalar model with m(Φ) = 1 TeV, m(X ) = 150 GeV, and cτ = 1 cm, is approximately
50% for events that have only one LLP (Z D or X) decaying to muons. The efficiency becomes
significantly smaller at low masses or at longer and shorter lifetimes, mostly because of a lower
trigger and geometric acceptance and insufficient displacement. For example, the efficiency at
the same set of masses decreases to approximately 15% at cτ = 100 cm, while the efficiency at
cτ = 100 cm drops to below 5% when m(Φ) = 125 GeV and m(X ) = 20 GeV. In accordance with
Fig. 3, the vast majority of the signal with the shortest (longest) lifetimes is found in the TMSTMS (STA-STA) dimuon category, whereas all three categories contain important fractions of
the signal with the intermediate lifetimes. The efficiency in 2018 is higher than that in 2016,
thanks mostly to the improved trigger and its relaxed requirements. The gain in efficiency is
especially large, about a factor of two, at m(Φ) = 125 GeV and long lifetimes.

5

Background estimation and associated systematic uncertainties

Since the background events passing the event selection criteria arise mostly from misreconstructed prompt muons and muons in jets, their yield cannot be reliably ascertained from simulation. Therefore, we evaluate the expected background using events in data. The control
regions used to estimate contributions from various types of background processes are chosen
by inverting one or more selection criteria in order to obtain a region populated mostly by a
given type of background and containing a negligible contribution from the signal processes.
The definitions of the control regions and the details of the background evaluation procedure

## PDF page 14

12
Table 1: Summary of the selection criteria used in the analysis, grouped into event, muon, and
dimuon requirements.
Event selection
N(PV)
HLT-STA muon matching
N(nearly parallel STA muons)

≥1
yes
<4

Muon selection
STA-to-TMS muon association
N(CSC+DT hits)
- associated STA muon
N(DT hits) for muons in barrel
tracker muon
N(matched muon segments)
pT
σpT /pT
χ2trk /dof
rel
Itrk
|∆t|
muon direction
d0 /σd0

Muon type
STA

TMS

not matched to TMS µ
>12
—
>18
—
—
>10 GeV
<1.0
<2.5
—
<12 ns
inside-out
—

matched to STA µ
—
>12
—
yes
>1
>10 GeV
<1.0
—
<0.075
—
—
>6

Dimuon selection

Dimuon category
STA-STA

DCA
pairing criteria
χ2vtx
∆N (pixel hits)
N(hits before vertex)
N(tracker layers) + floor(Lxy [cm]/15)
|ϕµTMS |
cos α
- 2016 data analysis
- 2018 data analysis
N(dimuon segments)
if |∆ηµµ | < 0.1
- N(dimuon segments)
- N(DT hits) for muons in barrel
no back-to-back muon
with |∆tb2b | > 20 ns
mµµ
pT of the leading muon
Lxy /σLxy
|∆Φ|
opposite-sign muons

STA-TMS

TMS-TMS

<15 cm
<15 cm
<15 cm
best 1–2 ranked dimuons selected
<10
<20
<10
—
—
<3
—
<6
<3
—
>5
>5
—
<2.9
—
>−0.8
>−0.9
>4

>−0.8
>−0.9
—

>−0.8
>−0.99
—

>5
>24

—
—

—
—

yes
>10 GeV
—
>6
<π/4
yes

—
>10 GeV
—
>3
<π/4
yes

—
>10 GeV
>25 GeV
>6
<π/4
yes

## PDF page 15

5.1

Estimation of Drell–Yan and other prompt backgrounds

13

differ for different dimuon categories and are described in the rest of this section. To avoid
potential bias in the event selection, the events passing the full selection (i.e., those in the signal
region) were “blinded” until the last steps of the analysis.
The contribution from cosmic ray muons is evaluated separately for each dimuon category
from the number of dimuons satisfying all selection criteria but failing the cos α requirements.
The evaluation procedure makes use of the efficiency of the cos α requirements measured from
a sample of cosmic ray muons collected during periods with no beam. In all dimuon categories,
the residual background arising from cosmic ray muons is estimated to be smaller than 0.1
events in all mass intervals combined.

5.1

Estimation of Drell–Yan and other prompt backgrounds

In all three dimuon categories, the contribution from prompt misreconstructed dimuons, collectively referred to as DY-like events, is evaluated from events in the signal-free |∆Φ|-symmetric
control region, |∆Φ| > 3π/4:
i
i
i
(OS; |∆Φ| < π/4) = NDY
(OS; |∆Φ| > 3π/4) RDY
,
NDY

(1)

i (OS; | ∆Φ | < π/4) and N i (OS; | ∆Φ | > 3π/4) are, respectively, the numbers of
where NDY
DY
i
DY background events in the signal and its |∆Φ|-symmetric control region; RDY
is the transfer
factor accounting for the residual asymmetry in the population of events in the two |∆Φ| regions and obtained from auxiliary measurements; and the index i denotes the dimuon category
(STA-STA, STA-TMS, or TMS-TMS). The number of DY dimuons in the |∆Φ| > 3π/4 region
is taken to be the total number of events in that region minus the expected contribution from
other types of background events estimated as discussed in Section 5.2.

The symmetry of the |∆Φ| distributions in this class of background events is studied using data
and simulated events. In the STA-STA and STA-TMS categories, we use events in the control
regions obtained by reversing the STA-to-TMS association. Specifically, we select events that
consist of STA-STA or, alternatively, STA-TMS dimuons passing all selection criteria, but in
which each of the constituent STA muons is associated with a TMS muon. To ensure that
such STA-STA and STA-TMS dimuons are promptly produced (and thus are not signal), we
require that the associated TMS-TMS dimuons, which have a far superior spatial resolution,
are prompt. This is achieved by requiring Lxy /σLxy < 1.0 for the associated TMS-TMS dimuon
in the STA-STA category, and d0 /σd0 < 1.5 for the TMS muon associated with the STA muon
in the STA-TMS category. To minimize contamination from muons from jets, which we discuss
separately in what follows, each TMS muon in the associated TMS-TMS dimuon is required to
rel < 0.05.
satisfy the isolation requirement Itrk
Since the TMS and STA muons are predominantly reconstructed from information in different
detectors (the tracker and the muon system, respectively), a genuine prompt muon giving rise
to a displaced STA muon is usually accurately reconstructed as prompt by the TMS muon reconstruction. As a result, the aforementioned control regions contain genuine prompt dimuons
that are reconstructed as displaced STA-STA or STA-TMS dimuons because of reconstruction
failures or vertex fit anomalies in these categories, i.e., exactly the type of background events
that we wish to study. The |∆Φ| distributions of STA-STA and STA-TMS dimuons in these
control regions, in 2018 data and simulated background samples, are shown in Fig. 4. (The distributions in 2016 data are very similar.) The observed distributions, sculpted by the interplay
between the geometric effects and the trigger and offline selection requirements, are well reproduced by the simulation. The distributions are still fairly symmetric around π/2, but there
is a small asymmetry caused by the event selection criteria. Corrections accounting for this

## PDF page 16

14
asymmetry are obtained from the ratio of events with |∆Φ| < π/4 and |∆Φ| > 3π/4 in the
aforementioned control regions,
rev,i
(OS; |∆Φ| > 3π/4)
NDY

61.3 fb-1 (13 TeV)

105

CMS
104

rev,i
(OS; |∆Φ| < π/4)
NDY

STA-STA

Data

Drell-Yan

tt

tW+t W

WW+WZ+ZZ

Stat. unc.

Events / 0.063 units

Events / 0.063 units

i
RDY
=

103
102

2

2.5

3

|∆Φ|

Drell-Yan

tt

tW+t W

WW+WZ+ZZ

Stat. unc.

102

1

1.5

STA-TMS

Data

103

1

1

61.3 fb-1 (13 TeV)

CMS
104

10

0.5

(2)

105

10

10−1
0

.

10−1
0

0.5

1

1.5

2

2.5

3

|∆Φ|

Figure 4: Distributions of |∆Φ| for (left) STA-STA and (right) STA-TMS dimuons in 2018 data
(black dots) and simulated background processes (stacked histograms), for events in the control regions with the STA-to-TMS association of the STA muons reversed, as described in the
text. All nominal selection requirements, including dimuon Lxy /σLxy and TMS muon d0 /σd0 ,
are applied to the STA-STA and STA-TMS dimuons. The simulated processes are scaled to
correspond to the integrated luminosity of the data. The shaded area shows the statistical uncertainty in the simulated background yield.
i
In both STA-STA and STA-TMS categories, no dependence of the transfer factor RDY
on mass
i
is observed, and a single value is used for all signal mass intervals. The resulting RDY
values
only weakly depend on the dimuon category and the data-taking year, and are in the range
of 0.8–0.9. The statistical uncertainties of the measurements do not exceed a few per cent.
i
i
The systematic uncertainties in RDY
are assessed by comparing RDY
measured in individual
mass intervals with the result of the inclusive measurement and by varying the boundaries
and definitions of the auxiliary control regions. The latter includes repeating the measurements
of RSTA-STA
in the region with only one STA-to-TMS muon association and of RSTA-TMS
in the
DY
DY
region obtained by requiring Lxy /σLxy < 1.5 for the associated TMS-TMS dimuon. Based on

these studies, we assign systematic uncertainties of 15% in RSTA-STA
and 40% in RSTA-TMS
.
DY
DY
In the TMS-TMS dimuon category, the symmetry of the |∆Φ| distribution in DY-like backgrounds is assessed from events in the control region obtained by reversal of the requirement
on χ2vtx . We observe a strong correlation between vertex χ2 and DCA in both data and simulated DY events, which suggests that χ2vtx is effectively a measure of the distance between the
TMS muons forming the dimuon. Further studies of TMS-TMS dimuons in DY events passing
and failing the χ2vtx requirement confirm that they differ only in how far away the two muons
are reconstructed from each other, and have very similar properties otherwise.
We use events in the inverted vertex χ2 control region to evaluate the transfer factor RTMS-TMS
DY
following Eq. (2). The measured value of RTMS-TMS
agrees with unity within the statistical
DY
uncertainties in most mµµ intervals and d0 /σd0 bins. Since no systematic trends are observed,
we use the value of RTMS-TMS
= 1 at all masses and in all min(d0 /σd0 ) bins, and assign a 15%
DY
systematic uncertainty to account for the largest deviations of RTMS-TMS
from unity.
DY

## PDF page 17

5.2

Estimation of nonprompt backgrounds

5.2

Estimation of nonprompt backgrounds

15

The background evaluation method described above is based on the symmetry of the |∆Φ|
distribution and does not account for the contributions from background sources that yield dimuons exclusively or predominantly at small |∆Φ|. Such background sources include: dimuon
decays of nonprompt low-mass resonances such as a J/ψ meson from b hadron decay; cascade decays of b hadrons; and dimuons formed from a pair of unrelated nonprompt muons
in the same jet. If well reconstructed, most such background events have mµµ not exceeding
a few GeV and are rejected by the mµµ > 10 GeV requirement. However, a small fraction of
them with mismeasured mµµ can satisfy this requirement and pass the event selection. Such
µµ
dimuons mostly have small |∆Φ| values (because the pT and Lxy vectors are collinear) and
may have large, signal-like Lxy /σLxy and d0 /σd0 values. They are also likely to have invariant masses close to the 10 GeV threshold. The other source of nonprompt background consists
of dimuons formed from muons embedded in different jets. Since all these nonprompt background events arise from jets produced through the strong interaction, we collectively refer to
them as quantum chromodynamics (QCD) events.
To gain insight into a contribution from this class of background events to the STA-STA and
STA-TMS categories, we study events in control regions similar to those described above, but
tailored to select events with muons embedded in jets. Once again, we invert the STA-toTMS association and select STA-STA or, alternatively, STA-TMS dimuons passing all selection
criteria, except that at least one of the constituent STA muons is associated with a TMS muon.
To suppress |∆Φ|-symmetric background events such as DY as well as potential contributions
rel > 0.1
from signal processes, we require each TMS muon to be nonisolated, defined as Itrk
rel > 0.125 in the STA-TMS category. According to the simulation, this
in the STA-STA and Itrk
requirement selects a subset of events almost entirely composed of QCD events. Figure 5 (left)
shows the |∆Φ| distribution of OS STA-STA dimuons in 2018 data in the samples thus obtained.
Unlike the DY events in Fig. 4, which are approximately symmetric around π/2, the QCD
events have a signal-like peak at |∆Φ| = 0. Most of these events are genuine low-mass dimuons
that are reconstructed at higher mµµ because of poor pT resolution of STA muons, and hence
pass the mµµ > 10 GeV requirement. This is demonstrated by Fig. 5 (right), which shows the
distribution of well-measured mµµ of TMS-TMS dimuons associated with STA-STA dimuons
with mµµ > 10 GeV.
Many of the background processes yielding small-|∆Φ| OS dimuons also give rise to small|∆Φ| SS dimuons, either because these processes are charge symmetric or via the muon charge
misassignment. Thus, we evaluate the contribution from the QCD background to the signal
i
region, NQCD
(OS; |∆Φ| < π/4), from the number of small-|∆Φ| SS dimuons, N i (SS; |∆Φ| <
π/4):
i
i
NQCD
(OS; |∆Φ| < π/4) = N i (SS; |∆Φ| < π/4) RQCD
.
(3)
i
The transfer factor RQCD
between the numbers of QCD events in these two regions is obtained
from the ratio of OS to SS dimuons in the aforementioned control region with the STA-to-TMS
association reversed and TMS muons not isolated:
i
RQCD
=

rev,i
NQCD
(OS; |∆Φ| < π/4)
rev,i
(SS; |∆Φ| < π/4)
NQCD

.

(4)

Because the charge misassignment and the probability of finding the STA-to-TMS association
i
were found to be anticorrelated, the measurement of RQCD
in the STA-STA category is performed using dimuons with exactly one of the constituent STA muons associated with a TMS

## PDF page 18

61.3 fb-1 (13 TeV)

400
350

CMS

STA-STA
|∆Φ*| ≡ |∆Φ|
(|∆Φ| < π/2)
|∆Φ*| ≡ π − |∆Φ| (|∆Φ| > π/2)

300
250
200

61.3 fb-1 (13 TeV)

Events / GeV

Events / 0.20 units

16

105

CMS

STA-STA
mSTA-STA
> 10 GeV
µµ

4

10

103

150
102

100
50
0
0

10
0.2

0.4

0.6

0.8

1

1.2

1.4

|∆Φ*|

1

10

102

mTMS-TMS
[GeV]
µµ

Figure 5: Distributions of (left) |∆Φ∗ | (defined in the legend) of STA-STA dimuons and (right)
mµµ of TMS-TMS dimuons associated with STA-STA dimuons. Both distributions show STASTA dimuons in 2018 data in the control region enriched in QCD events, as described in the
text. (The distributions in 2016 data are very similar.) In the left plot, exactly one STA muon is
associated with a TMS muon, while in the right plot, both are. All nominal selection requirements, including mµµ > 10 GeV and Lxy /σLxy > 6, are applied to the STA-STA dimuons.
muon, providing events that are more representative of those in the signal region. Since the
i
composition of the QCD background varies as a function of mµµ , the evaluation of RQCD
is
performed separately in the individual mass intervals, with the exception of the STA-STA category, where a common value is used for mµµ > 35 GeV to avoid large statistical fluctuations
i
of RSTA-STA
. The measured values of RQCD
in these two categories vary between 1.1 and 2.3 deQCD
pending on the mass interval and year, with statistical uncertainties in the range of 10–30% in
the STA-STA and 2–20% in the STA-TMS category. The systematic uncertainties in RSTA-STA
are
QCD
assessed by evaluating the potential impact on RSTA-STA
of
the
correlation
between
the
success
QCD
rate of the STA-to-TMS association and STA muon charge misassignment. The systematic uncertainties in RSTA-TMS
are evaluated by varying the definitions of the auxiliary control regions,
QCD
e.g., performing the measurement of RSTA-TMS
in the region obtained by inverting the isolation
QCD
requirement applied to the TMS muon. Based on these studies, we assign a systematic uncertainty in the range of 10–30% in RSTA-STA
, depending on the mass interval and the year, and a
QCD
STA-TMS
fixed 30% systematic uncertainty in RQCD .
A priori, we do not expect a large contribution from |∆Φ|-asymmetric low-mass dimuons in
the TMS-TMS category, because of a far superior dimuon invariant mass resolution. Indeed,
the study of simulated QCD events shows that a vast majority of both OS and SS TMS-TMS
dimuons passing all selection criteria arise from a pair of unrelated nonprompt muons in two
different jets. Such events do not contain genuine displaced dimuons and are expected to have
a symmetric |∆Φ| distribution. Nevertheless, since some contribution from |∆Φ|-asymmetric
dimuons may still be present in the background events in data, we prefer not to rely on the
|∆Φ| symmetry in the evaluation of nonprompt backgrounds. Instead, similarly to the STASTA and STA-TMS categories, we use the fact that dijet and multijet events give rise to both OS
and SS dimuons, and base our estimate of the QCD background on the number of SS dimuons
following Eq. (3).
The transfer factor RTMS-TMS
is obtained from the ratio of OS to SS dimuons in the control region
QCD
with the muon isolation requirement reversed, which comprises dimuons passing the nominal
rel > 0.075 and both with I rel < 0.5. We have
event selection but with at least one muon with Itrk
trk

## PDF page 19

5.3

Validation of background predictions

17

verified that these events, as well as SS dimuons passing isolation requirements, contain negligible contributions from signal and DY events. As the signal region is divided into several
min(d0 /σd0 ) bins, the evaluation of RTMS-TMS
is performed separately in each min(d0 /σd0 ) bin.
QCD
TMS-TMS
Since no dependence of the value of RQCD
on mµµ is observed, RTMS-TMS
in each min(d0 /σd0 )
QCD
bin is calculated by integrating events in the entire invariant mass spectrum. The measured values of RTMS-TMS
decrease from ≈2 to ≈1 as min(d0 /σd0 ) increases, with statistical uncertainties
QCD
in the range of 5–20%. A systematic uncertainty of 15% is assigned to account for variations of
RTMS-TMS
as a function of the invariant mass and as the result of changing the definition and
QCD
boundaries of the auxiliary control region.
To avoid overestimating the DY background, the same QCD background evaluation method is
applied to dimuons in the |∆Φ| > 3π/4 control region. The obtained estimate of the QCD background is then subtracted from the total observed number of OS dimuons with |∆Φ| > 3π/4
i (OS; | ∆Φ | > 3π/4), used for
to obtain the number of DY dimuons in this |∆Φ| region, NDY
the evaluation of the DY backgrounds in the signal |∆Φ| < π/4 region according to Eq. (1).
This procedure is not applied in the STA-STA category, where the |∆Φ|-symmetric QCD background is negligible. The sum of the QCD and DY background estimates constitute the total
predicted background in the signal region. According to the background evaluation method,
the DY backgrounds are expected to dominate at small d0 /σd0 and Lxy /σLxy values, whereas the
relative QCD contribution becomes larger as d0 /σd0 and Lxy /σLxy increase. The uncertainty in
the background predictions is dominated by the statistical uncertainty in the numbers of events
in the |∆Φ| > 3π/4 and SS control regions.

5.3

Validation of background predictions

The background evaluation method described in Sections 5.1 and 5.2 is tested in several validation regions (VRs) that are expected to contain negligible contribution from signal. The
evaluation of DY backgrounds is examined in the VRs obtained by inverting the Lxy /σLxy and
d0 /σd0 requirements and thereby enriched in this class of events. One example of such studies
is shown in Fig. 6, which compares the background predictions to the observed distributions in
the Lxy /σLxy < 6 VR in the STA-STA category. The yields in data are consistent with predictions
of the method, which also correctly predicts a larger STA-STA background in 2016 compared
to 2018 due to a lower tracking efficiency in a part of 2016 data [34].
In another check, we apply the background evaluation procedure to the TMS-TMS dimuons
in the 2 < min(d0 /σd0 ) < 6 sideband. The comparison of the predicted background and data
in bins of Lxy /σLxy is shown in Fig. 7. The expected and observed numbers of events are in
agreement in the entire probed Lxy /σLxy range. There are more background events in 2018 data
than in 2016 data because of looser trigger requirements and larger integrated luminosity.
The evaluation of the |∆Φ|-asymmetric component of QCD backgrounds, which is particularly
important in the STA-STA category, is tested in the low-mass (6 < mµµ < 10 GeV) VR, as well
as in the region obtained by inverting the requirement on the minimum number of DT hits
and muon segments applied to dimuons with |∆ηµµ | < 0.1, referred to as the small-|∆ηµµ |
VR. Using dimuons with STA muons associated with TMS muons and taking well-measured
mµµ and |∆Φ| values of corresponding TMS-TMS dimuons as proxies for true values of these
quantities, we have verified that the samples of events in these VRs predominantly consist of
small-|∆Φ| dimuons with mismeasured mµµ . Figure 8 shows the comparison of the predicted
background yields and data in these two VRs. The low-mass VR is only available in 2018
data because the trigger used to collect 2016 data for this analysis included the mµµ > 10 GeV

## PDF page 20

18

CMS

Observed
Drell-Yan (predicted)
QCD (predicted)
Stat. uncertainty

STA-STA

25

61.3 fb-1 (13 TeV)

Events / 1 unit

Events / 1 unit

36.3 fb-1 (13 TeV)
30

20

CMS

Observed
Drell-Yan (predicted)
QCD (predicted)
Stat. uncertainty

STA-STA

25
20

15

15

10

10

5

5
0

Lxy/ σL

4
3
2
1
00

1

2

3

4

5

xy

Obs. / pred.

0

Obs. / pred.

30

6

Lxy/ σLxy

Lxy/ σL

4
3
2
1
00

1

2

3

4

5

xy

6

Lxy/ σLxy

104

CMS

TMS-TMS
2 < min(d / σd ) < 6
0

0

103

Events / 2 units

36.3 fb-1 (13 TeV)

105

Observed
Drell-Yan (predicted)
QCD (predicted)
Stat. uncertainty

102

104

10−1

10−1

2
1.5
1
0.5
00

2
1.5
1
0.5
00

20

25

30

Lxy/ σLxy

0

Observed
Drell-Yan (predicted)
QCD (predicted)
Stat. uncertainty

102

1

15

TMS-TMS
2 < min(d / σd ) < 6
0

1

10

CMS

103

10

5

61.3 fb-1 (13 TeV)

105

10

Obs. / pred.

Obs. / pred.

Events / 2 units

Figure 6: Distributions of Lxy /σLxy of STA-STA dimuons in the Lxy /σLxy < 6 VR, in (left) 2016
and (right) 2018 data, compared to the background predictions. The observed distributions
(black points with error bars) are overlayed on stacked histograms containing the expected
numbers of DY (green) and QCD (yellow) background events. The lower panels show the
ratio of the observed to predicted numbers of events. The shaded area shows the statistical
uncertainty in the total background prediction; the admixture of the QCD background in this
validation region is estimated separately and has a larger statistical uncertainty than the total
background.

5

10

15

20

25

30

Lxy/ σLxy

Figure 7: Distributions of Lxy /σLxy of TMS-TMS dimuons in the 2 < min(d0 /σd0 ) < 6 VR,
in (left) 2016 and (right) 2018 data, compared to the background predictions. The observed
distributions (black points with error bars) are overlayed on stacked histograms containing the
expected numbers of DY (green) and QCD (yellow) background events. The last bin includes
events in the overflow. The lower panels show the ratio of the observed to predicted numbers
of events. The shaded area shows the statistical uncertainty in the background prediction.

## PDF page 21

5.3

19

Validation of background predictions

Events / bin

requirement. The small-|∆ηµµ | VR is available in both data sets, but since the number of events
in this VR in 2016 data is small, an additional test is performed on a subset of 2018 data collected
using the 2016 trigger, and therefore enriched in events similar to those recorded in 2016. The
mµµ intervals of 10–32, 15–60, and 20–80 GeV shown for the small-|∆ηµµ | VRs are the intervals
chosen to probe LLP masses of 20, 30, and 50 GeV, respectively. The yields in data are found to
be consistent with background predictions in all tests and mµµ intervals.

60

97.6 fb-1 (13 TeV)

CMS
2018

2018

2018 (2016 HLT)

2016

low-mµµ

small-|∆ ηµµ|

small-|∆ ηµµ|

small-|∆ ηµµ|

50
STA-STA

40

Observed
QCD (predicted)
Stat. uncertainty

30
20
10
0
[6, 10]

[10, 32] [15, 60] [20, 80] [10, 32] [15, 60] [20, 80] [10, 32] [15, 60] [20, 80]

mµ µ [GeV]

Figure 8: Comparison of observed (black points with error bars) and predicted (histograms)
yields of STA-STA dimuons in the validation regions enriched in QCD background events. The
first bin shows the yields in the low-mass VR in 2018 data. The other three groups of bins,
separated by solid lines, show the yields in the small-|∆ηµµ | VR, in (from left to right) the
entire 2018 data set, a subset of 2018 data enriched in events collected in 2016, and the 2016
data set. Each of these three VRs is further subdivided into three mµµ intervals, 10–32, 15–60,
and 20–80 GeV. The expected number of background events is computed according to Eqs. (3)
and (4), separately in each mµµ bin. The shaded area shows the statistical uncertainty in the
background prediction.
Finally, to ensure the validity of the method at different values of the main discriminating
variable in the TMS-TMS and STA-TMS categories, the validation checks are performed in
bins of d0 /σd0 of the TMS muon. Such checks include comparisons in the d0 /σd0 sideband
(d0 /σd0 < 6) in the signal |∆Φ| region, as well as those in the entire d0 /σd0 range in the |∆Φ|
sideband, π/4 < |∆Φ| < π/2. In the latter, the region with π/4 < |∆Φ| < π/2 is used as
a signal-free proxy for the |∆Φ| < π/4 signal region. The background evaluation procedure
is applied to the OS and SS dimuons in the |∆Φ|-symmetric region, π/2 < |∆Φ| < 3π/4, as
well as SS dimuons with π/4 < |∆Φ| < π/2. The comparisons of the predicted background
and 2018 data in the TMS-TMS and STA-TMS categories in this VR are shown in Fig. 9. The
observed and expected numbers of events are consistent within statistical uncertainties.

## PDF page 22

61.3 fb-1 (13 TeV)

105
104

CMS

Events / 2 units

Events / 2 units

20

Observed
Drell-Yan (predicted)
QCD (predicted)
Stat. uncertainty

TMS-TMS
π/4 < |∆Φ| < π/2

103
102

61.3 fb-1 (13 TeV)

104

CMS

Observed
Drell-Yan (predicted)
QCD (predicted)
Stat. uncertainty

STA-TMS
π/4 < |∆Φ| < π/2

103

102

10
10
1

10−1

10−1

2
1.5
1
0.5
00

2.5
2
1.5
1
0.5
00

Obs. / pred.

Obs. / pred.

1

5

10

15

20

25

30

min(d / σd )
0

5

10

0

15

20

25

30

d0/ σd

0

Figure 9: Distributions in the π/4 < |∆Φ| < π/2 VR in 2018 data: (left) the smaller of the
two d0 /σd0 values for the TMS-TMS dimuon; (right) d0 /σd0 of the TMS muon in the STA-TMS
dimuon. The observed distributions (black points with error bars) are compared to the results
of the background prediction method applied to events with π/2 < |∆Φ| < 3π/4. The stacked
histograms show the expected numbers of DY (green) and QCD (yellow) background events.
The last bin includes events in the overflow. The lower panels show the ratios of the observed
to predicted numbers of events. The shaded area shows the statistical uncertainty in the background prediction.

6

Systematic uncertainties affecting the signal

Most of the systematic uncertainties affecting the signal efficiencies are evaluated separately
in each dimuon category and for each data-taking year. Unless stated otherwise, we consider
sources of uncertainties to be uncorrelated among different dimuon categories and years.
In the STA-STA and STA-TMS categories, the dominant systematic uncertainties come from
the STA muon identification and trigger efficiencies. At small displacements, both efficiencies are accurately measured as a function of muon pT and η by applying the “tag-and-probe
method” [28] to muons from J/ψ meson and Z boson decays. The differences in the identification and trigger efficiencies between data and simulation are used to correct the signal simulation yields. In the STA-STA category, these corrections range from 0.78 to 1.13, depending on
the signal sample. The evolution of efficiencies with displacement is studied using a sample
of cosmic ray muons collected during periods with no beam, and additional d0 -dependent corrections and systematic uncertainties are derived. At d0 = 10 (100) cm, the correction amounts
to 0.99 (0.96) per muon, whereas the uncertainty is on the order of 10 (35)%. Since the d0 dependent uncertainty is dominated by the accuracy of the L1 trigger efficiency measurements,
it is taken to be correlated among all dimuon categories.
The dominant systematic uncertainties in the TMS-TMS category come from the d0 dependence
of the L1 trigger efficiency discussed above and the efficiency to reconstruct displaced muons
in the tracker. The evolution of the tracking efficiency with d0 is measured using a sample of
cosmic ray muons and compared to the tracking efficiency predicted by simulation. Based on
the results of the comparison, we assign a 5% systematic uncertainty per muon for muons with
d0 > 1 cm. The overall efficiency corrections applied to the simulated signal yields range from
0.74 to 1.08, depending on the signal sample, and arise mostly from imperfect modeling of the
HLT efficiencies at small displacements.
The remaining systematic uncertainties related to the signal efficiency are much smaller. The
impact of mismodeling of the muon pT resolution on the signal yield is evaluated by smearing

## PDF page 23

21
the muon pT in simulated signal events according to the measurements performed using cosmic ray muons and muons from Z boson decays. This leads to variations that are less than 2%
at all signal masses except for m(Z D ) = 10 GeV. Corrections of up to 2% are applied to the TMS
muon efficiency to account for the difference in efficiency of isolation requirements measured
using muons from Z boson decays, and an additional systematic uncertainty of 2% is assigned.
A systematic uncertainty ranging from 1 to 8%, depending on the signal sample, is assigned to
account for mismodeling of the DCA requirement in the STA-STA category. The efficiency of
the vertex χ2 requirement as a function of displacement is studied using cosmic ray muons and
muons from Z boson decays in the STA-STA category, and muons from decays of nonprompt
J/ψ mesons in the TMS-TMS category. The differences between data and simulation contribute
an uncertainty of 2% in each category. The efficiencies of several other selection criteria, such
as requirements on the number of tracker hits upstream of the vertex position and the difference between the number of pixel hits on two TMS muons, are found to be well modeled by
simulation, and no additional uncertainty is assigned.
The uncertainty in the integrated luminosity, partially correlated between the years, is 1.2% in
2016 [15] and 2.5% in 2018 [16]. The uncertainty in the signal efficiency due to pileup is 2%.
Both uncertainties are correlated among dimuon categories.

7

Results

The predicted background yields in the representative mµµ intervals and the corresponding
numbers of observed events are shown in Fig. 10 for the STA-STA category and Fig. 11 for the
STA-TMS category. For illustration, signals at the level of the median expected exclusion limits
at 95% confidence level (CL) in the absence of signal are also shown. As expected, events observed in the STA-STA and STA-TMS categories are predominantly at low masses—14 out of 18
STA-STA and 9 out of 13 STA-TMS events have mµµ < 20 GeV—and have characteristics typical of those for QCD background events. The numbers of observed events and the predicted
background and signal yields in the TMS-TMS category are shown in Fig. 12 as functions of
mµµ in each of the three min(d0 /σd0 ) bins and in Fig. 13 as a function of min(d0 /σd0 ). The
observed TMS-TMS events have a steeply falling min(d0 /σd0 ) distribution and cluster at mµµ
values of a few tens of GeV, which are both consistent with the characteristics of the expected
background. The numbers of observed events are consistent with the predicted background
yields in all dimuon categories and mµµ intervals, in both data sets. No significant excess of
events above the SM background is observed.
For each of the two benchmark models, we compute upper limits on the product of the signal
production cross section σ and the branching fraction B to two muons as a function of mass
and mean proper decay length. The limit extraction is based on a modified frequentist approach [35, 36] and uses the CMS C OMBINE package developed for statistically combining the
results of Higgs boson searches [37]. The method yielding background predictions in the signal
region is implemented using a multibin likelihood, which is a product of Poisson distributions
corresponding to the signal region and the control regions. The systematic uncertainties affecting the signal yield are incorporated as nuisance parameters using log-normal distributions.
The expected and observed upper limits are evaluated through the use of simulated pseudoexperiments. For each signal model, the limits are first computed separately in each dimuon
category and for each data-taking year. The individual likelihoods are then combined to obtain
the combined limits.
The signal efficiencies are obtained from simulation and further corrected by the data-to-simulation scale factors described in Section 6; they are computed separately for each year, signal

## PDF page 24

36.3 fb-1 (13 TeV)

35
30

CMS
STA-STA

25

Observed (total: 2 events)
H→ZDZD(20 GeV, ε = 1 × 10-8) × 4
H→ZDZD(50 GeV, ε = 4 × 10-9) × 8
Drell-Yan (predicted)
QCD (predicted)
Stat. uncertainty
+ 3.8
Total bkg. (unbinned): 2.7
events

Events / bin

Events / bin

22

− 1.8

20

30

10

10

5

5
40

60

80

100

120

STA-STA

0

140

Observed (total: 16 events)
H→ZDZD(20 GeV, ε = 1 × 10-8) × 4
H→ZDZD(50 GeV, ε = 4 × 10-9) × 8
Drell-Yan (predicted)
QCD (predicted)
Stat. uncertainty
+ 6.4
Total bkg. (unbinned): 6.3
events
− 3.5

20
15

20

CMS

25

15

0

61.3 fb-1 (13 TeV)

35

20

40

60

80

100

mµµ [GeV]

120

140

mµµ [GeV]

36.3 fb-1 (13 TeV)

30

CMS
25

STA-TMS

20

Observed (total: 5 events)
H→ZDZD(30 GeV, ε = 6 × 10-8) × 40
H→ZDZD(60 GeV, ε = 3 × 10-8) × 40
Drell-Yan (predicted)
QCD (predicted)
Stat. uncertainty
+ 4.9
Total bkg. (unbinned): 3.5
events

Events / bin

Events / bin

Figure 10: Comparison of the number of events observed in (left) 2016 and (right) 2018 data
in the STA-STA dimuon category with the expected number of background events, in representative mµµ intervals. The black points with error bars show the number of observed events;
the green and yellow components of the stacked histograms represent the estimated numbers
of DY and QCD events, respectively. The last bin includes events in the overflow. The uncertainties in the total expected background (shaded area) are statistical only. Signal contributions
expected from simulated H → Z D Z D with m(Z D ) of 20 and 50 GeV are shown in red and blue,
respectively. Their yields are set to the corresponding combined median expected exclusion
limits at 95% CL, scaled up as indicated in the legend to improve visibility. The legends also
include the total number of observed events as well as the number of expected background
events obtained inclusively, by applying the background evaluation method to the events in all
mµµ intervals combined.
61.3 fb-1 (13 TeV)

30

CMS
25

STA-TMS

20

− 2.3

− 3.8

15

15

10

10

5

5

0

20

40

60

80

100

120

140

mµµ [GeV]

Observed (total: 8 events)
H→ZDZD(30 GeV, ε = 6 × 10-8) × 40
H→ZDZD(60 GeV, ε = 3 × 10-8) × 40
Drell-Yan (predicted)
QCD (predicted)
Stat. uncertainty
+ 6.7
Total bkg. (unbinned): 8.9
events

0

20

40

60

80

100

120

140

mµµ [GeV]

Figure 11: Comparison of the number of events observed in (left) 2016 and (right) 2018 data
in the STA-TMS dimuon category with the expected number of background events, in representative mµµ intervals. The black points with error bars show the number of observed events;
the green and yellow components of the stacked histograms represent the estimated numbers
of DY and QCD events, respectively. The last bin includes events in the overflow. The uncertainties in the total expected background (shaded area) are statistical only. Signal contributions
expected from simulated H → Z D Z D with m(Z D ) of 30 and 60 GeV are shown in red and blue,
respectively. Their yields are set to the corresponding combined median expected exclusion
limits at 95% CL, scaled up as indicated in the legend to improve visibility. The legends also
include the total number of observed events as well as the number of expected background
events obtained inclusively, by applying the background evaluation method to the events in all
mµµ intervals combined.

## PDF page 25

Events / bin

23

25

25

CMS
TMS-TMS

20

Drell-Yan (predicted)
QCD (predicted)
Stat. uncertainty

20
0

0

0

20

min(d / σd ) > 20
0

0

15

15

15

10

10

10

5

5

5

102

20 30 40

2×102

25

0
10

20

102

30 40

2×102

25

CMS
20

TMS-TMS

20

Drell-Yan (predicted)
QCD (predicted)
Stat. uncertainty

10

0

0

61.3 fb-1 (13 TeV)

0

10

10

10

5

5

5

2×102

0
10

20

30 40

102

2×102

mµµ [GeV]

min(d / σd ) > 20
15

102

2×102

H→ZDZD(20 GeV, ε = 5×10-7, cτ = 2.2 mm) × 12
H→ZDZD(50 GeV, ε = 7×10-7, cτ = 0.4 mm) × 8

0

15

20 30 40

102

30 40

20

15

0
10

20

10 < min(d / σd ) ≤ 20

6 < min(d / σd ) ≤ 10

0

0

25

Observed (total 36 events)
+ 17.3
Total bkg. (unbinned): 60.1 − 11.8 events

0

36.3 fb-1 (13 TeV)
H→ZDZD(20 GeV, ε = 5×10-7, cτ = 2.2 mm) × 12
H→ZDZD(50 GeV, ε = 7×10-7, cτ = 0.4 mm) × 8

10 < min(d / σd ) ≤ 20

6 < min(d / σd ) ≤ 10

0
10

Events / bin

25

Observed (total 6 events)
+ 9.8
Total bkg. (unbinned): 7.5 − 4.1 events

0

0
10

20

30 40

102

2×102

mµµ [GeV]

Figure 12: Comparison of the number of events observed in (upper) 2016 and (lower) 2018
data in the TMS-TMS dimuon category with the expected number of background events, in
representative mµµ intervals in each of the three min(d0 /σd0 ) bins. The black points with error
bars show the number of observed events; the green and yellow components of the stacked
histograms represent the estimated numbers of DY and QCD events, respectively. The last
bin in each min(d0 /σd0 ) interval includes events in the overflow. The uncertainties in the total expected background (shaded area) are statistical only. Signal contributions expected from
simulated H → Z D Z D with m(Z D ) of 20 and 50 GeV are shown in red and blue, respectively.
Their yields are set to the corresponding combined median expected exclusion limits at 95%
CL, scaled up as indicated in the legend to improve visibility. The legends also include the
total number of observed events as well as the number of expected background events obtained inclusively, by applying the background evaluation method to the events in all mµµ and
min(d0 /σd0 ) intervals combined.

## PDF page 26

36.3 fb-1 (13 TeV)

105

Observed
H→ZDZD(20 GeV, ε = 5×10-7) × 12
H→ZDZD(50 GeV, ε = 7×10-7) × 8
Drell-Yan (predicted)
QCD (predicted)
Stat. uncertainty

CMS
104

Events / bin

Events / bin

24

TMS-TMS

103

10

10

1

1

10

15

20

25

30

35

40

min(d / σd )
0

0

TMS-TMS

103
102

5

Observed
H→ZDZD(20 GeV, ε = 5×10-7) × 12
H→ZDZD(50 GeV, ε = 7×10-7) × 8
Drell-Yan (predicted)
QCD (predicted)
Stat. uncertainty

CMS
104

102

10−1
0

61.3 fb-1 (13 TeV)

105

10−1
0

5

10

15

20

25

30

35

40

min(d / σd )
0

0

Figure 13: Comparison of the number of events observed in (left) 2016 and (right) 2018 data in
the TMS-TMS dimuon category with the expected number of background events, as a function
of the smaller of the two d0 /σd0 values for the TMS-TMS dimuon. The black points with error
bars show the number of observed events; the green and yellow components of the stacked
histograms represent the estimated numbers of DY and QCD events, respectively. The last bin
includes events in the overflow. The uncertainties in the total expected background (shaded
area) are statistical only. Signal contributions expected from simulated H → Z D Z D with m(Z D )
of 20 and 50 GeV are shown in red and blue, respectively. Their yields are set to the corresponding combined median expected exclusion limits at 95% CL, scaled up as indicated in the legend
to improve visibility.
model, dimuon category, and mass interval. A reweighting procedure is employed to calculate
an estimated number of signal events for lifetimes other than the lifetimes used to produce the
available simulated signal samples. Given the smallness of the expected background and taking into account the selection efficiencies discussed in Section 4, an introduction of a separate
category for events with two dimuons does not increase the sensitivity of the analysis significantly even in the most favorable case for the 4µ signal events, namely B(X → µµ ) = 1. The
gain is negligible for smaller B(X → µµ ) values such as those predicted by the HAHM model.
Therefore, no distinction is made between events with one and two dimuons of the same type.
Events with two TMS-TMS dimuons are assigned to the min(d0 /σd0 ) bin encompassing the
larger of the two min(d0 /σd0 ) values.
The observed and expected 95% CL upper limits on the product σ(Φ → XX )B(X → µµ ) as a
function of cτ (X ) in the simplified heavy-scalar model for m(Φ) = 125, 200, 400, and 1000 GeV
are shown in Figs. 14, 15, 16, and 17, respectively. Each figure shows the limits obtained with
the ensemble of 2016 and 2018 data in the individual dimuon categories, as well as their combination. The search is sensitive to a broad range of cτ from 30 µm to more than 1 km. As
expected, the three dimuon categories reach maximum sensitivity at different cτ values and all
give relevant contributions to the overall sensitivity of the search. The limits are most restrictive
for cτ between 0.1 mm and 10–100 m, excluding σ(Φ → XX )B(X → µµ ) smaller than 1 fb, and
become more stringent at high LLP masses, owing to a higher signal efficiency and lower background. The smallest σ(Φ → XX )B(X → µµ ) value excluded is 0.05 fb, at m(X ) = 350 GeV
and cτ between 0.3 and 30 cm.
Figure 18 shows the observed and expected 95% CL upper limits obtained in the framework
of the HAHM model under the assumption of m(Φ) > m(H )/2. The limits in the individual
dimuon categories, as well as their combination, are set on the product σ(H → Z D Z D )B(Z D →
µµ ) for different m(Z D ) as a function of the mean proper decay length of Z D . The limits are

## PDF page 27

106
105
104
103

97.6 fb-1 (13 TeV)

CMS

95% CL upper limits:
Combined observed
Combined expected (median)
Combined expected (68% quantile)
Combined expected (95% quantile)
STA-STA expected (median)
TMS-TMS expected (median)
STA-TMS expected (median)

mφ = 125 GeV
mX = 20 GeV

10
10
2

10

1

σ(φ→XX)Β (X→µµ) [pb]

σ(φ→XX)Β (X→µµ) [pb]

25

106
105
104
103

1

10−2

10

10−4

10−3

−4

10

95% CL upper limits:
Combined observed
Combined expected (median)
Combined expected (68% quantile)
Combined expected (95% quantile)
STA-STA expected (median)
TMS-TMS expected (median)
STA-TMS expected (median)

mφ = 125 GeV
mX = 50 GeV

−1

10−2
10−3

CMS

102
10

10

−1

97.6 fb-1 (13 TeV)

−5

10−3 10−2 10−1

1

10

102

103

104

105

106

cτ [cm]

10−5 −3
10
10−2 10−1

1

10

102

103

104

105

106

cτ [cm]

106
105
104
10

3

97.6 fb-1 (13 TeV)

CMS

95% CL upper limits:
Combined observed
Combined expected (median)
Combined expected (68% quantile)
Combined expected (95% quantile)
STA-STA expected (median)
TMS-TMS expected (median)
STA-TMS expected (median)

mφ = 200 GeV
mX = 20 GeV

102
10

1

10−1

σ(φ→XX)Β (X→µµ) [pb]

σ(φ→XX)Β (X→µµ) [pb]

Figure 14: The 95% CL upper limits on σ(Φ → XX )B(X → µµ ) as a function of cτ (X ) in the
heavy-scalar model, for m(Φ) = 125 GeV and (left) m(X ) = 20 GeV and (right) m(X ) = 50 GeV.
The median expected limits obtained from the STA-STA, STA-TMS, and TMS-TMS dimuon
categories are shown as dashed green, blue, and red curves, respectively; the combined median
expected limits are shown as dashed black curves; and the combined observed limits are shown
as solid black curves. The green and yellow bands correspond, respectively, to the 68 and 95%
quantiles for the combined expected limits.

106
105
104
10

3

mφ = 200 GeV
mX = 50 GeV

1

10−2

10

10−4

10

10−3

−4

10−3 10−2 10−1

95% CL upper limits:
Combined observed
Combined expected (median)
Combined expected (68% quantile)
Combined expected (95% quantile)
STA-STA expected (median)
TMS-TMS expected (median)
STA-TMS expected (median)

10−1

−3

10

CMS

102
10

10−2
−5

97.6 fb-1 (13 TeV)

1

10

102

103

104

105

106

cτ [cm]

10−5 −3
10
10−2 10−1

1

10

102

103

104

105

106

cτ [cm]

Figure 15: The 95% CL upper limits on σ(Φ → XX )B(X → µµ ) as a function of cτ (X ) in the
heavy-scalar model, for m(Φ) = 200 GeV and (left) m(X ) = 20 GeV and (right) m(X ) = 50 GeV.
The median expected limits obtained from the STA-STA, STA-TMS, and TMS-TMS dimuon
categories are shown as dashed green, blue, and red curves, respectively; the combined median
expected limits are shown as dashed black curves; and the combined observed limits are shown
as solid black curves. The green and yellow bands correspond, respectively, to the 68 and 95%
quantiles for the combined expected limits.

## PDF page 28

106
105
10

4

103

97.6 fb-1 (13 TeV)

CMS

95% CL upper limits:
Combined observed
Combined expected (median)
Combined expected (68% quantile)
Combined expected (95% quantile)
STA-STA expected (median)
TMS-TMS expected (median)
STA-TMS expected (median)

mφ = 400 GeV
mX = 20 GeV

10
10
2

1

10−1

σ(φ→XX)Β (X→µµ) [pb]

σ(φ→XX)Β (X→µµ) [pb]

26
106
105
10

4

103

1

10−2

10

10−4

10

10−3

−4

1

10

102

σ(φ→XX)Β (X→µµ) [pb]

10−3 10−2 10−1

95% CL upper limits:
Combined observed
Combined expected (median)
Combined expected (68% quantile)
Combined expected (95% quantile)
STA-STA expected (median)
TMS-TMS expected (median)
STA-TMS expected (median)

mφ = 400 GeV
mX = 50 GeV

10−1

−3

10

CMS

102
10

10−2
−5

97.6 fb-1 (13 TeV)

106
105
104
10

3

103

104

105

106

cτ [cm]

CMS

10−5 −3
10
10−2 10−1

1

10

97.6 fb-1 (13 TeV)

102

103

104

105

106

cτ [cm]

95% CL upper limits:
Combined observed
Combined expected (median)
Combined expected (68% quantile)
Combined expected (95% quantile)
STA-STA expected (median)
TMS-TMS expected (median)
STA-TMS expected (median)

mφ = 400 GeV
mX = 150 GeV

102
10

1

10−1

10−2
10−3
10−4

10−5 −3
10
10−2 10−1

1

10

102

103

104

105

106

cτ [cm]

Figure 16: The 95% CL upper limits on σ(Φ → XX )B(X → µµ ) as a function of cτ (X ) in
the heavy-scalar model, for m(Φ) = 400 GeV and (upper left) m(X ) = 20 GeV, (upper right)
m(X ) = 50 GeV, and (lower) m(X ) = 150 GeV. The median expected limits obtained from
the STA-STA, STA-TMS, and TMS-TMS dimuon categories are shown as dashed green, blue,
and red curves, respectively; the combined median expected limits are shown as dashed black
curves; and the combined observed limits are shown as solid black curves. The green and
yellow bands correspond, respectively, to the 68 and 95% quantiles for the combined expected
limits.
compared to the theoretical predictions for a set of representative B(H → Z D Z D ) values ranging from 1% to 0.001%. In the m(Z D ) range of 20–60 GeV, the branching fraction B(H → Z D Z D )
of 1% is excluded in the cτ (Z D ) range from a few tens of µm to approximately 100 m, whereas
B(H → Z D Z D ) as low as 0.01% is excluded in the range of 1 mm to 1 m. These constraints on
rare SM Higgs boson decays are tighter than those derived from searches for invisible Higgs
boson decays [38] and from indirect constraints from measurements of the SM Higgs boson
couplings [39]. At m(Z D ) > 20 GeV, the limits obtained are the best to date for all cτ (Z D ) values except those between ≈0.5 and 500 mm (depending on m(Z D )), where our search is complemented by the CMS search using data collected with a dedicated high-rate data stream [40].
The observed 95% CL exclusion contours in the (m(Z D ), cτ (Z D )) plane, determined from the
observed 2016-18 upper limits on cτ (Z D ) for several representative values of B(H → Z D Z D ),
are shown in Fig. 19 (left). These results can be translated into limits on the kinetic mixing ϵ
following the relationship between the dark photon mass, lifetime, and ϵ. The resulting 95% CL
exclusion contours in the (m(Z D ), ϵ) plane are shown in Fig. 19 (right). Our analysis excludes
a wide range of ϵ values, between 9 × 10−9 and 6 × 10−6 at m(Z D ) = 10 GeV and between

## PDF page 29

106
105
104
10

3

97.6 fb-1 (13 TeV)

CMS

95% CL upper limits:
Combined observed
Combined expected (median)
Combined expected (68% quantile)
Combined expected (95% quantile)
STA-STA expected (median)
TMS-TMS expected (median)
STA-TMS expected (median)

mφ = 1000 GeV
mX = 20 GeV

102
10

1

10−1

σ(φ→XX)Β (X→µµ) [pb]

σ(φ→XX)Β (X→µµ) [pb]

27

106
105
104
10

3

10

10−4

10

10−3

−4

10−3 10−2 10−1

10

3

1

10

102

103

104

105

106

cτ [cm]

10−5 −3
10
10−2 10−1

97.6 fb-1 (13 TeV)

CMS

95% CL upper limits:
Combined observed
Combined expected (median)
Combined expected (68% quantile)
Combined expected (95% quantile)
STA-STA expected (median)
TMS-TMS expected (median)
STA-TMS expected (median)

mφ = 1000 GeV
mX = 150 GeV

102
10

1

10−1

σ(φ→XX)Β (X→µµ) [pb]

σ(φ→XX)Β (X→µµ) [pb]

−5

104

106
105
104
10

3

102

103

104

105

106

cτ [cm]

97.6 fb-1 (13 TeV)

CMS

95% CL upper limits:
Combined observed
Combined expected (median)
Combined expected (68% quantile)
Combined expected (95% quantile)
STA-STA expected (median)
TMS-TMS expected (median)
STA-TMS expected (median)

mφ = 1000 GeV
mX = 350 GeV

1

10−2

10

10−4

10

10−3

−4

10−3 10−2 10−1

10

10−1

−3

10

1

102
10

10−2
−5

mφ = 1000 GeV
mX = 50 GeV

1

10−2

105

95% CL upper limits:
Combined observed
Combined expected (median)
Combined expected (68% quantile)
Combined expected (95% quantile)
STA-STA expected (median)
TMS-TMS expected (median)
STA-TMS expected (median)

10−1

−3

106

CMS

102
10

10−2
10

97.6 fb-1 (13 TeV)

1

10

102

103

104

105

106

cτ [cm]

10−5 −3
10
10−2 10−1

1

10

102

103

104

105

106

cτ [cm]

Figure 17: The 95% CL upper limits on σ(Φ → XX )B(X → µµ ) as a function of cτ (X ) in
the heavy-scalar model, for m(Φ) = 1 TeV and (upper left) m(X ) = 20 GeV, (upper right)
m(X ) = 50 GeV, (lower left) m(X ) = 150 GeV, and (lower right) m(X ) = 350 GeV. The median
expected limits obtained from the STA-STA, STA-TMS, and TMS-TMS dimuon categories are
shown as dashed green, blue, and red curves, respectively; the combined median expected
limits are shown as dashed black curves; and the combined observed limits are shown as solid
black curves. The green and yellow bands correspond, respectively, to the 68 and 95% quantiles
for the combined expected limits.

## PDF page 30

10

103

CMS
mH = 125 GeV
mZD = 10 GeV
Β (Z →µµ) = 0.144
D

D

2

10
10

95% CL upper limits:
Combined observed
Combined expected (median)
Combined expected (68% quantile)
Combined expected (95% quantile)
STA-STA expected (median)
TMS-TMS expected (median)
STA-TMS expected (median)

1

Β (H→ZDZD) = 0.01%

10−4

Β (H→ZDZD) = 0.001%

10

105
104

D

σ(H→Z ZD)Β(Z →µµ) [pb]

106

3

10

D

2

10
10

10

102

103

104

105

−2

10

106

cτ [cm]

95% CL upper limits:
Combined observed
mH = 125 GeV
Combined expected (median)
Combined expected (68% quantile)
mZD = 30 GeV
Combined expected (95% quantile)
Β (Z →µµ) = 0.140
D
STA-STA expected (median)
TMS-TMS expected (median)
STA-TMS expected (median)

CMS

Β (H→ZDZD) = 1%

−4

Β (H→ZDZD) = 0.001%

10

D

2

10
10

1

10

102

103

104

105

106

−2

10

103
102
10

10

102

103

104

105

106

cτ [cm]

97.6 fb-1 (13 TeV)

95% CL upper limits:
Combined observed
mH = 125 GeV
Combined expected (median)
Combined expected (68% quantile)
mZD = 40 GeV
Combined expected (95% quantile)
Β (Z →µµ) = 0.134
D
STA-STA expected (median)
TMS-TMS expected (median)
STA-TMS expected (median)

CMS

1
10−1

Β (H→ZDZD) = 1%
Β (H→ZDZD) = 0.1%

−3

Β (H→ZDZD) = 0.01%

−4

Β (H→ZDZD) = 0.001%

10

cτ [cm]

97.6 fb-1 (13 TeV)

95% CL upper limits:
Combined observed
mH = 125 GeV
Combined expected (median)
Combined expected (68% quantile)
mZD = 50 GeV
Combined expected (95% quantile)
Β (Z →µµ) = 0.122
D
STA-STA expected (median)
TMS-TMS expected (median)
STA-TMS expected (median)

CMS

1
10−1

104

Β (H→ZDZD) = 1%

104
103
102
10

Β (H→ZDZD) = 0.01%

−4

Β (H→ZDZD) = 0.001%

10
10

10

102

103

104

105

1

10

102

105

106

cτ [cm]

95% CL upper limits:
Combined observed
mH = 125 GeV
Combined expected (median)
Combined expected (68% quantile)
mZD = 60 GeV
Combined expected (95% quantile)
Β (Z →µµ) = 0.103
D
STA-STA expected (median)
TMS-TMS expected (median)
STA-TMS expected (median)

CMS

Β (H→ZDZD) = 1%
Β (H→ZDZD) = 0.1%
Β (H→ZDZD) = 0.01%

10

−4

Β (H→ZDZD) = 0.001%

10
106

104

97.6 fb-1 (13 TeV)

−3

cτ [cm]

103

1
10−1

10

−3

1

105

−2

Β (H→ZDZD) = 0.1%

10−5 −3
10
10−2 10−1

10−3 10−2 10−1

106

D

10

105

D

3

106

1

10

σ(H→Z ZD)Β(Z →µµ) [pb]

104

D

σ(H→Z ZD)Β(Z →µµ) [pb]

105

Β (H→ZDZD) = 0.001%

10−5 −3
10
10−2 10−1

−5

10−3 10−2 10−1

106

Β (H→ZDZD) = 0.01%

10

−5

10

Β (H→ZDZD) = 0.1%

10−4

10

10

Β (H→ZDZD) = 1%

−3

−2

Β (H→ZDZD) = 0.1%
Β (H→ZDZD) = 0.01%

D

95% CL upper limits:
Combined observed
Combined expected (median)
Combined expected (68% quantile)
Combined expected (95% quantile)
STA-STA expected (median)
TMS-TMS expected (median)
STA-TMS expected (median)

1
10−1

97.6 fb-1 (13 TeV)

−3

mH = 125 GeV
mZD = 20 GeV
Β (Z →µµ) = 0.143

10

1
10−1

CMS

102
10

10

−3

1

103

−2

Β (H→ZDZD) = 0.1%

10−5 −3
10
10−2 10−1

10

D

10

4

D

−2

Β (H→ZDZD) = 1%

σ(H→Z ZD)Β(Z →µµ) [pb]

10−1

105

D

4

97.6 fb-1 (13 TeV)

106

D

105

σ(H→Z ZD)Β(Z →µµ) [pb]

97.6 fb-1 (13 TeV)

106

D

σ(H→Z ZD)Β(Z →µµ) [pb]

28

10−5 −3
10
10−2 10−1

1

10

102

103

104

105

106

cτ [cm]

Figure 18: The 95% CL upper limits on σ(H → Z D Z D )B(Z D → µµ ) as a function of cτ (Z D ) in
the HAHM model, for m(Z D ) ranging from 10 GeV (upper left) to 60 GeV (lower right). The median expected limits obtained from the STA-STA, STA-TMS, and TMS-TMS dimuon categories
are shown as dashed green, blue, and red curves, respectively; the combined median expected
limits are shown as dashed black curves; and the combined observed limits are shown as solid
black curves. The green and yellow bands correspond, respectively, to the 68 and 95% quantiles for the combined expected limits. The horizontal lines in gray correspond to the theoretical
predictions for values of B(H → Z D Z D ) indicated next to the lines.

## PDF page 31

29

97.6 fb-1 (13 TeV)

108
107

Β (H→ZDZD) = 1%
Β (H→ZDZD) = 0.1%
Β (H→ZDZD) = 0.05%
Β (H→ZDZD) = 0.01%
Β (H→ZDZD) = 0.005%

CMS
95% CL exclusion contours

106

ε

cτ [cm]

5 × 10−10 and 1.5 × 10−6 at m(Z D ) = 60 GeV for B(H → Z D Z D ) = 1%.

105

10−4

Β (H→ZDZD) = 1%
Β (H→ZDZD) = 0.1%
Β (H→ZDZD) = 0.05%
Β (H→ZDZD) = 0.01%
Β (H→ZDZD) = 0.005%

CMS
95% CL exclusion contours

−5

10

104

10−6

103
2

10
10

10−7

1

10−8

−1

10

10−9

10−2
10−3

97.6 fb-1 (13 TeV)

10−3

10

20

30

40

50

60

m(Z ) [GeV]
D

10−10

10

20

30

40

50

60

m(Z ) [GeV]
D

Figure 19: Observed 95% CL exclusion contours in the HAHM model, in the (left) (m(Z D ),
cτ (Z D )) and (right) (m(Z D ), ϵ) planes. The contours correspond to several representative values of B(H → Z D Z D ) ranging from 0.005 to 1%.

8

Summary

√
Data collected by the CMS experiment in proton-proton collisions at s = 13 TeV in 2016 and
2018 and corresponding to an integrated luminosity of 97.6 fb−1 have been used to conduct
an inclusive search for long-lived exotic neutral particles (LLPs) decaying to a pair of oppositely charged muons. The search is largely model-independent and is sensitive to a broad
range of LLP lifetimes and masses. No significant excess of events above the standard model
background is observed. The results are interpreted as limits on the parameters of the hidden
Abelian Higgs model, in which the Higgs boson decays to a pair of long-lived dark photons
Z D , and of a simplified model, in which LLPs are produced in decays of an exotic heavy neutral scalar boson. In the mass range 20 < m(Z D ) < 60 GeV, a branching fraction of the Higgs
boson to dark photons of 1% is excluded at 95% confidence level in the range of proper decay
length cτ (Z D ) from a few tens of µm to ≈100 m. The results of this search significantly extend
the previously excluded range of model parameters. For the hidden Abelian Higgs model with
m(Z D ) greater than 20 GeV and less than half the mass of the Higgs boson, they provide the
best limits to date on the branching fraction of the Higgs boson to dark photons for cτ (Z D )
(varying with m(Z D )) between 0.03 and ≈0.5 mm, and above ≈0.5 m. At exotic scalar boson
masses larger than the Higgs boson mass, our results represent the best current constraints for
all considered LLP masses and lifetimes.

Acknowledgments
We congratulate our colleagues in the CERN accelerator departments for the excellent performance of the LHC and thank the technical and administrative staffs at CERN and at other
CMS institutes for their contributions to the success of the CMS effort. In addition, we gratefully acknowledge the computing centres and personnel of the Worldwide LHC Computing
Grid and other centres for delivering so effectively the computing infrastructure essential to
our analyses. Finally, we acknowledge the enduring support for the construction and operation of the LHC, the CMS detector, and the supporting computing infrastructure provided
by the following funding agencies: BMBWF and FWF (Austria); FNRS and FWO (Belgium);
CNPq, CAPES, FAPERJ, FAPERGS, and FAPESP (Brazil); MES and BNSF (Bulgaria); CERN;

## PDF page 32

30
CAS, MoST, and NSFC (China); MINCIENCIAS (Colombia); MSES and CSF (Croatia); RIF
(Cyprus); SENESCYT (Ecuador); MoER, ERC PUT and ERDF (Estonia); Academy of Finland,
MEC, and HIP (Finland); CEA and CNRS/IN2P3 (France); BMBF, DFG, and HGF (Germany);
GSRI (Greece); NKFIH (Hungary); DAE and DST (India); IPM (Iran); SFI (Ireland); INFN
(Italy); MSIP and NRF (Republic of Korea); MES (Latvia); LAS (Lithuania); MOE and UM
(Malaysia); BUAP, CINVESTAV, CONACYT, LNS, SEP, and UASLP-FAI (Mexico); MOS (Montenegro); MBIE (New Zealand); PAEC (Pakistan); MES and NSC (Poland); FCT (Portugal); J
MESTD (Serbia); MCIN/AEI and PCTI (Spain); MOSTR (Sri Lanka); Swiss Funding Agencies (Switzerland); MST (Taipei); MHESI and NSTDA (Thailand); TUBITAK and TENMAK
(Turkey); NASU (Ukraine); STFC (United Kingdom); DOE and NSF (USA).
Individuals have received support from the Marie-Curie programme and the European Research Council and Horizon 2020 Grant, contract Nos. 675440, 724704, 752730, 758316, 765710,
824093, 884104, and COST Action CA16108 (European Union); the Leventis Foundation; the
Alfred P. Sloan Foundation; the Alexander von Humboldt Foundation; the Belgian Federal
Science Policy Office; the Fonds pour la Formation à la Recherche dans l’Industrie et dans
l’Agriculture (FRIA-Belgium); the Agentschap voor Innovatie door Wetenschap en Technologie (IWT-Belgium); the F.R.S.-FNRS and FWO (Belgium) under the “Excellence of Science –
EOS” – be.h project n. 30820817; the Beijing Municipal Science & Technology Commission,
No. Z191100007219010; the Ministry of Education, Youth and Sports (MEYS) of the Czech
Republic; the Hellenic Foundation for Research and Innovation (HFRI), Project Number 2288
(Greece); the Deutsche Forschungsgemeinschaft (DFG), under Germany’s Excellence Strategy –
EXC 2121 “Quantum Universe” – 390833306, and under project number 400140256 - GRK2497;
the Hungarian Academy of Sciences, the New National Excellence Program - ÚNKP, the NKFIH research grants K 124845, K 124850, K 128713, K 128786, K 129058, K 131991, K 133046, K
138136, K 143460, K 143477, 2020-2.2.1-ED-2021-00181, and TKP2021-NKTA-64 (Hungary); the
Council of Science and Industrial Research, India; the Latvian Council of Science; the Ministry
of Education and Science, project no. 2022/WK/14, and the National Science Center, contracts Opus 2021/41/B/ST2/01369 and 2021/43/B/ST2/01552 (Poland); the Fundação para
a Ciência e a Tecnologia, grant CEECIND/01334/2018 (Portugal); the National Priorities Research Program by Qatar National Research Fund; MCIN/AEI/10.13039/501100011033, ERDF
“a way of making Europe”, and the Programa Estatal de Fomento de la Investigación Cientı́fica
y Técnica de Excelencia Marı́a de Maeztu, grant MDM-2017-0765 and Programa Severo Ochoa
del Principado de Asturias (Spain); the Chulalongkorn Academic into Its 2nd Century Project
Advancement Project, and the National Science, Research and Innovation Fund via the Program Management Unit for Human Resources & Institutional Development, Research and Innovation, grant B05F650021 (Thailand); the Kavli Foundation; the Nvidia Corporation; the SuperMicro Corporation; the Welch Foundation, contract C-1845; and the Weston Havens Foundation (USA).

References
[1] R. Barbier et al., “R-parity violating supersymmetry”, Phys. Rept. 420 (2005) 1,
doi:10.1016/j.physrep.2005.08.006, arXiv:hep-ph/0406039.
[2] J. L. Hewett, B. Lillie, M. Masip, and T. G. Rizzo, “Signatures of long-lived gluinos in split
supersymmetry”, JHEP 09 (2004) 070, doi:10.1088/1126-6708/2004/09/070,
arXiv:hep-ph/0408248.

## PDF page 33

References

31

[3] M. J. Strassler and K. M. Zurek, “Echoes of a hidden valley at hadron colliders”, Phys.
Lett. B 651 (2007) 374, doi:10.1016/j.physletb.2007.06.055,
arXiv:hep-ph/0604261.
[4] T. Han, Z. Si, K. M. Zurek, and M. J. Strassler, “Phenomenology of hidden valleys at
hadron colliders”, JHEP 07 (2008) 008, doi:10.1088/1126-6708/2008/07/008,
arXiv:0712.2041.
[5] D. Curtin, R. Essig, S. Gori, and J. Shelton, “Illuminating dark photons with high-energy
colliders”, JHEP 02 (2015) 157, doi:10.1007/JHEP02(2015)157,
arXiv:1412.0018.
[6] M. J. Strassler and K. M. Zurek, “Discovering the Higgs through highly-displaced
vertices”, Phys. Lett. B 661 (2008) 263, doi:10.1016/j.physletb.2008.02.008,
arXiv:hep-ph/0605193.
[7] CMS Collaboration, “Search for long-lived particles that decay
√ into final states containing
two electrons or two muons in proton-proton collisions at s = 8 TeV”, Phys. Rev. D 91
(2015) 052012, doi:10.1103/PhysRevD.91.052012, arXiv:1411.6977.
[8] CMS Collaboration, “Search for long-lived particles that decay into final states containing
two muons, reconstructed using only the CMS muon chambers”, CMS Physics Analysis
Summary CMS-PAS-EXO-14-012, 2015.
[9] ATLAS Collaboration, “Search for long-lived
particles in final states with displaced
√
dimuon vertices in pp collisions at s = 13 TeV with the ATLAS detector”, Phys. Rev. D
99 (2019) 012001, doi:10.1103/PhysRevD.99.012001, arXiv:1808.03057.
[10] HEPData record for this analysis, 2022. doi:10.17182/hepdata.129518.
[11] CMS Collaboration, “Performance
√ of the CMS muon detector and muon reconstruction
with proton-proton collisions at s = 13 TeV”, JINST 13 (2018) P06015,
doi:10.1088/1748-0221/13/06/P06015, arXiv:1804.04528.
[12] CMS Collaboration, “The CMS experiment at the CERN LHC”, JINST 3 (2008) S08004,
doi:10.1088/1748-0221/3/08/S08004.
[13] CMS
√ Collaboration, “Performance of the CMS Level-1 trigger in proton-proton collisions
at s = 13 TeV”, JINST 15 (2020) P10017, doi:10.1088/1748-0221/15/10/P10017,
arXiv:2006.10165.
[14] CMS Collaboration, “The CMS trigger system”, JINST 12 (2017) P01020,
doi:10.1088/1748-0221/12/01/P01020, arXiv:1609.02366.
[15] CMS
√ Collaboration, “Precision luminosity measurement in proton-proton collisions at
s = 13 TeV in 2015 and 2016 at CMS”, Eur. Phys. J. C 81 (2021) 800,
doi:10.1140/epjc/s10052-021-09538-2, arXiv:2104.01927.
[16] CMS
√ Collaboration, “CMS luminosity measurement for the 2018 data-taking period at
s = 13 TeV”, CMS Physics Analysis Summary CMS-PAS-LUM-18-002, 2018.
[17] J. D. Wells, “How to find a hidden world at the Large Hadron Collider”, in Perspectives
on LHC Physics, G. Kane and A. Pierce, eds., p. 283. World Scientific, Singapore, 2008.
arXiv:0803.1243. doi:10.1142/9789812779762_0015.

## PDF page 34

32
[18] J. Alwall et al., “The automated computation of tree-level and next-to-leading order
differential cross sections, and their matching to parton shower simulations”, JHEP 07
(2014) 079, doi:10.1007/JHEP07(2014)079, arXiv:1405.0301.
[19] M. Cepeda et al., “Report from working group 2: Higgs physics at the HL-LHC and
HE-LHC”, in Proceedings of the HL/HE-LHC Workshop, A. Dainese et al., eds., volume 7,
p. 221. 2019. arXiv:1902.00134. CERN Yellow Rep. Monogr.
doi:10.23731/CYRM-2019-007.221.
[20] T. Sjöstrand et al., “An introduction to PYTHIA 8.2”, Comput. Phys. Commun. 191 (2015)
159, doi:10.1016/j.cpc.2015.01.024, arXiv:1410.3012.
[21] J. Butterworth et al., “PDF4LHC recommendations for LHC Run II”, J. Phys. G 43 (2016)
023001, doi:10.1088/0954-3899/43/2/023001, arXiv:1510.03865.
[22] CMS Collaboration, “Event generator tunes obtained from underlying event and
multiparton scattering measurements”, Eur. Phys. J. C 76 (2016) 155,
doi:10.1140/epjc/s10052-016-3988-x, arXiv:1512.00815.
[23] NNPDF Collaboration, “Parton distributions from high-precision collider data”, Eur.
Phys. J. C 77 (2017) 663, doi:10.1140/epjc/s10052-017-5199-5,
arXiv:1706.00428.
[24] CMS Collaboration, “Extraction and validation of a new set of CMS PYTHIA8 tunes from
underlying-event measurements”, Eur. Phys. J. C 80 (2020) 4,
doi:10.1140/epjc/s10052-019-7499-4, arXiv:1903.12179.
[25] G EANT 4 Collaboration, “G EANT 4—a simulation toolkit”, Nucl. Instrum. Meth. A 506
(2003) 250, doi:10.1016/S0168-9002(03)01368-8.
[26] CMS Collaboration, “Technical proposal for the Phase-II upgrade of the Compact Muon
Solenoid”, CMS Technical Proposal CERN-LHCC-2015-010, CMS-TDR-15-02, 2015.
[27] CMS Collaboration,
“Performance of the CMS muon trigger system in proton-proton
√
collisions at s = 13 TeV”, JINST 16 (2021) P07001,
doi:10.1088/1748-0221/16/07/P07001, arXiv:2102.04790.
[28] CMS
√ Collaboration, “Performance of CMS muon reconstruction in pp collision events at
s = 7 TeV”, JINST 7 (2012) P10002, doi:10.1088/1748-0221/7/10/P10002,
arXiv:1206.4071.
[29] R. Frühwirth, “Application of Kalman filtering to track and vertex fitting”, Nucl. Instrum.
Meth. A 262 (1987) 444, doi:10.1016/0168-9002(87)90887-4.
[30] T. Speer et al., “Vertex fitting in the CMS tracker”, CMS Note CMS-NOTE-2006-032, 2006.
[31] B. C. Allanach et al., “Mass spectrum in R-parity violating mSUGRA and benchmark
points”, Phys. Rev. D 75 (2007) 035002, doi:10.1103/PhysRevD.75.035002,
arXiv:hep-ph/0609263.
[32] F. Deppisch, S. Kulkarni, and W. Liu, “Heavy neutrino production via Z ′ at the lifetime
frontier”, Phys. Rev. D 100 (2019) 035005, doi:10.1103/PhysRevD.100.035005,
arXiv:1905.11889.

## PDF page 35

References

33

[33] R. D. Cousins, J. T. Linnemann, and J. Tucker, “Evaluation of three methods for
calculating statistical significance when incorporating a systematic uncertainty into a test
of the background-only hypothesis for a Poisson process”, Nucl. Instrum. Meth. A 595
(2008) 480, doi:10.1016/j.nima.2008.07.086, arXiv:physics/0702156.
[34] CMS Collaboration, “Search for new particles decaying to a jet and an emerging jet”,
JHEP 02 (2019) 179, doi:10.1007/JHEP02(2019)179, arXiv:1810.10069.
[35] A. L. Read, “Presentation of search results: The CLs technique”, J. Phys. G 28 (2002) 2693,
doi:10.1088/0954-3899/28/10/313.
[36] T. Junk, “Confidence level computation for combining searches with small statistics”,
Nucl. Instrum. Meth. A 434 (1999) 435, doi:10.1016/S0168-9002(99)00498-2,
arXiv:hep-ex/9902006.
[37] ATLAS and CMS Collaborations, and LHC Higgs Combination Group, “Procedure for
the LHC Higgs boson search combination in Summer 2011”, Technical Report
CMS-NOTE-2011-005. ATL-PHYS-PUB-2011-11, 2011.
[38] CMS Collaboration, “Search for invisible decays
√ of the Higgs boson produced via vector
boson fusion in proton–proton collisions at s = 13 TeV”, 2022. arXiv:2201.11585.
Accepted by Phys. Rev. D.
[39] CMS Collaboration, “Combined
√ measurements of Higgs boson couplings in
proton–proton collisions at s = 13 TeV”, Eur. Phys. J. C 79 (2019) 421,
doi:10.1140/epjc/s10052-019-6909-y, arXiv:1809.10733.
[40] CMS Collaboration, “Search√for long-lived particles decaying into muon pairs in
proton-proton collisions at s = 13 TeV collected with a dedicated high-rate data stream”,
JHEP 04 (2022) 062, doi:10.1007/JHEP04(2022)062, arXiv:2112.13769.

## PDF page 36

34

## PDF page 37

35

A

The CMS Collaboration

Yerevan Physics Institute, Yerevan, Armenia
A. Tumasyan1
Institut für Hochenergiephysik, Vienna, Austria
W. Adam , J.W. Andrejkovic, T. Bergauer , S. Chatterjee , K. Damanakis , M. Dragicevic , A. Escalante Del Valle , P.S. Hussain , M. Jeitler2 , N. Krammer , S. Kulkarni3 ,
L. Lechner , D. Liko , I. Mikulec , P. Paulitsch, F.M. Pitters, J. Schieck2 , R. Schöfbeck ,
D. Schwarz , M. Sonawane , S. Templ , W. Waltenberger , C.-E. Wulz2
Universiteit Antwerpen, Antwerpen, Belgium
M.R. Darwish4 , T. Janssen , T. Kello5 , H. Rejeb Sfar, P. Van Mechelen
Vrije Universiteit Brussel, Brussel, Belgium
E.S. Bols , J. D’Hondt , A. De Moor , M. Delcourt , H. El Faham , S. Lowette ,
S. Moortgat , A. Morton , D. Müller , A.R. Sahasransu , S. Tavernier , W. Van Doninck,
D. Vannerom
Université Libre de Bruxelles, Bruxelles, Belgium
B. Clerbaux , G. De Lentdecker , L. Favart , J. Jaramillo , K. Lee , M. Mahdavikhorrami , I. Makarenko , A. Malara , S. Paredes , L. Pétré , N. Postiau, E. Starling ,
L. Thomas , M. Vanden Bemden, C. Vander Velde , P. Vanlaer
Ghent University, Ghent, Belgium
D. Dobur , J. Knolle , L. Lambrecht , G. Mestdach, M. Niedziela , C. Rendón,
C. Roskas , A. Samalan, K. Skovpen , M. Tytgat , N. Van Den Bossche , B. Vermassen,
L. Wezenbeek
Université Catholique de Louvain, Louvain-la-Neuve, Belgium
A. Benecke , A. Bethani , G. Bruno , F. Bury , C. Caputo , P. David , C. Delaere
I.S. Donertas , A. Giammanco , K. Jaffel , Sa. Jain , V. Lemaitre, K. Mondal
J. Prisciandaro, A. Taliercio , T.T. Tran , P. Vischia , S. Wertz

,
,

Centro Brasileiro de Pesquisas Fisicas, Rio de Janeiro, Brazil
G.A. Alves , E. Coelho , C. Hensel , A. Moraes , P. Rebello Teles
Universidade do Estado do Rio de Janeiro, Rio de Janeiro, Brazil
W.L. Aldá Júnior , M. Alves Gallo Pereira , M. Barroso Ferreira Filho , H. Brandao Malbouisson , W. Carvalho , J. Chinellato6 , E.M. Da Costa , G.G. Da Silveira7 ,
D. De Jesus Damiao , V. Dos Santos Sousa , S. Fonseca De Souza , J. Martins8 ,
C. Mora Herrera , K. Mota Amarilo , L. Mundim , H. Nogima , A. Santoro ,
S.M. Silva Do Amaral , A. Sznajder , M. Thiel , F. Torres Da Silva De Araujo9 ,
A. Vilela Pereira
Universidade Estadual Paulista, Universidade Federal do ABC, São Paulo, Brazil
C.A. Bernardes7 , L. Calligaris , T.R. Fernandez Perez Tomei , E.M. Gregores
P.G. Mercadante , S.F. Novaes , Sandra S. Padula

,

Institute for Nuclear Research and Nuclear Energy, Bulgarian Academy of Sciences, Sofia,
Bulgaria
A. Aleksandrov , G. Antchev , R. Hadjiiska , P. Iaydjiev , M. Misheva , M. Rodozov,
M. Shopova , G. Sultanov
University of Sofia, Sofia, Bulgaria

## PDF page 38

36
A. Dimitrov

, T. Ivanov

, L. Litov

, B. Pavlov

, P. Petkov

, A. Petrov, E. Shumka

Beihang University, Beijing, China
T. Cheng , T. Javaid10 , M. Mittal , L. Yuan
Department of Physics, Tsinghua University, Beijing, China
M. Ahmad , G. Bauer11 , Z. Hu , S. Lezki , K. Yi11,12
Institute of High Energy Physics, Beijing, China
G.M. Chen10 , H.S. Chen10 , M. Chen10 , F. Iemmi , C.H. Jiang, A. Kapoor , H. Liao
Z.-A. Liu13 , V. Milosevic , F. Monti , R. Sharma , J. Tao , J. Thomas-Wilsker
J. Wang , H. Zhang , J. Zhao

,
,

State Key Laboratory of Nuclear Physics and Technology, Peking University, Beijing, China
A. Agapitos , Y. An , Y. Ban , C. Chen, A. Levin , Q. Li , X. Lyu, Y. Mao, S.J. Qian ,
X. Sun , D. Wang , J. Xiao , H. Yang
Sun Yat-Sen University, Guangzhou, China
M. Lu , Z. You
Institute of Modern Physics and Key Laboratory of Nuclear Physics and Ion-beam
Application (MOE) - Fudan University, Shanghai, China
X. Gao5 , D. Leggat, H. Okawa , Y. Zhang
Zhejiang University, Hangzhou, Zhejiang, China
Z. Lin , C. Lu , M. Xiao
Universidad de Los Andes, Bogota, Colombia
C. Avila , D.A. Barbosa Trujillo, A. Cabrera , C. Florez

, J. Fraga

Universidad de Antioquia, Medellin, Colombia
J. Mejia Guisao , F. Ramirez , M. Rodriguez , J.D. Ruiz Alvarez
University of Split, Faculty of Electrical Engineering, Mechanical Engineering and Naval
Architecture, Split, Croatia
D. Giljanovic , N. Godinovic , D. Lelas , I. Puljak
University of Split, Faculty of Science, Split, Croatia
Z. Antunovic, M. Kovac , T. Sculac
Institute Rudjer Boskovic, Zagreb, Croatia
V. Brigljevic , B.K. Chitroda , D. Ferencek
A. Starodumov14 , T. Susa

,

D. Majumder

,

M. Roguljic

University of Cyprus, Nicosia, Cyprus
A. Attikis , K. Christoforou , G. Kole , M. Kolosova , S. Konstantinou
C. Nicolaou, F. Ptochos , P.A. Razis , H. Rykaczewski, H. Saka

, J. Mousa

,

,

Charles University, Prague, Czech Republic
M. Finger14 , M. Finger Jr.14 , A. Kveton
Escuela Politecnica Nacional, Quito, Ecuador
E. Ayala
Universidad San Francisco de Quito, Quito, Ecuador
E. Carrera Jarrin
Academy of Scientific Research and Technology of the Arab Republic of Egypt, Egyptian

## PDF page 39

37
Network of High Energy Physics, Cairo, Egypt
S. Elgammal15 , A. Ellithi Kamel16
Center for High Energy Physics (CHEP-FU), Fayoum University, El-Fayoum, Egypt
M. Abdullah Al-Mashad , M.A. Mahmoud
National Institute of Chemical Physics and Biophysics, Tallinn, Estonia
S. Bhowmik , R.K. Dewanjee , K. Ehataht , M. Kadastik, S. Nandan
J. Pata , M. Raidal , L. Tani , C. Veelken

, C. Nielsen

,

Department of Physics, University of Helsinki, Helsinki, Finland
P. Eerola , H. Kirschenmann , K. Osterberg , M. Voutilainen
Helsinki Institute of Physics, Helsinki, Finland
S. Bharthuar , E. Brücken , F. Garcia , J. Havukainen , M.S. Kim , R. Kinnunen,
T. Lampén , K. Lassila-Perini , S. Lehti , T. Lindén , M. Lotti, L. Martikainen ,
M. Myllymäki , J. Ott , M.m. Rantanen , H. Siikonen , E. Tuominen , J. Tuominiemi
Lappeenranta-Lahti University of Technology, Lappeenranta, Finland
P. Luukka , H. Petrow , T. Tuuva
IRFU, CEA, Université Paris-Saclay, Gif-sur-Yvette, France
C. Amendola , M. Besancon , F. Couderc , M. Dejardin , D. Denegri, J.L. Faure,
F. Ferri , S. Ganjour , P. Gras , G. Hamel de Monchenault , P. Jarry , V. Lohezic ,
J. Malcles , J. Rander, A. Rosowsky , M.Ö. Sahin , A. Savoy-Navarro17 , P. Simkina ,
M. Titov
Laboratoire Leprince-Ringuet, CNRS/IN2P3, Ecole Polytechnique, Institut Polytechnique
de Paris, Palaiseau, France
C. Baldenegro Barrera , F. Beaudette , A. Buchot Perraguin , P. Busson , A. Cappati ,
C. Charlot , O. Davignon , B. Diab , G. Falmagne , B.A. Fontana Santos Alves ,
S. Ghosh , R. Granier de Cassagnac , A. Hakimi , B. Harikrishnan , J. Motta ,
M. Nguyen , C. Ochando , L. Portales , J. Rembser , R. Salerno , U. Sarkar ,
J.B. Sauvan , Y. Sirois , A. Tarabini , E. Vernazza , A. Zabi , A. Zghiche
Université de Strasbourg, CNRS, IPHC UMR 7178, Strasbourg, France
J.-L. Agram18 , J. Andrea, D. Apparu , D. Bloch , G. Bourgatte, J.-M. Brom
E.C. Chabert , C. Collard , D. Darej, U. Goerlach , C. Grimault, A.-C. Le Bihan
E. Nibigira , P. Van Hove

,
,

Institut de Physique des 2 Infinis de Lyon (IP2I ), Villeurbanne, France
S. Beauceron , C. Bernet , G. Boudoul , C. Camen, A. Carle, N. Chanon , J. Choi ,
D. Contardo , P. Depasse , C. Dozen19 , H. El Mamouni, J. Fay , S. Gascon ,
M. Gouzevitch , G. Grenier , B. Ille , I.B. Laktineh, M. Lethuillier , L. Mirabito, S. Perries,
K. Shchablo, V. Sordini , L. Torterotot , M. Vander Donckt , P. Verdier , S. Viret
Georgian Technical University, Tbilisi, Georgia
D. Chokheli , I. Lomidze , Z. Tsamalaidze14
RWTH Aachen University, I. Physikalisches Institut, Aachen, Germany
V. Botta , L. Feld , K. Klein , M. Lipinski , D. Meuser , A. Pauls
M. Teroerde

, N. Röwert

,

RWTH Aachen University, III. Physikalisches Institut A, Aachen, Germany
S. Diekmann , A. Dodonova , N. Eich , D. Eliseev , M. Erdmann , P. Fackeldey

,

## PDF page 40

38
B. Fischer , T. Hebbeker , K. Hoepfner , F. Ivone , M.y. Lee , L. Mastrolorenzo,
M. Merschmeyer , A. Meyer , S. Mondal , S. Mukherjee , D. Noll , A. Novak ,
F. Nowotny, A. Pozdnyakov , Y. Rath, H. Reithler , A. Schmidt , S.C. Schuler,
A. Sharma , L. Vigilante, S. Wiedenbeck , S. Zaleski
RWTH Aachen University, III. Physikalisches Institut B, Aachen, Germany
C. Dziwok , G. Flügge , W. Haj Ahmad20 , O. Hlushchenko, T. Kress , A. Nowack
O. Pooth , A. Stahl21 , T. Ziemons , A. Zotz

,

Deutsches Elektronen-Synchrotron, Hamburg, Germany
H. Aarup Petersen, M. Aldaya Martin , P. Asmuss, S. Baxter , M. Bayatmakou ,
O. Behnke, A. Bermúdez Martı́nez , S. Bhattacharya , A.A. Bin Anuar , F. Blekman22 ,
K. Borras23 , D. Brunner , A. Campbell , A. Cardini , C. Cheng, F. Colombina,
S. Consuegra Rodrı́guez , G. Correia Silva , M. De Silva , L. Didukh , G. Eckerlin,
D. Eckstein, L.I. Estevez Banos , O. Filatov , E. Gallo22 , A. Geiser , A. Giraldi ,
G. Greau, A. Grohsjean , V. Guglielmi , M. Guthoff , A. Jafari24 , N.Z. Jomhari ,
B. Kaech , A. Kasem23 , M. Kasemann , H. Kaveh , C. Kleinwort , R. Kogler ,
D. Krücker , W. Lange, D. Leyva Pernia, K. Lipka , W. Lohmann25 , R. Mankel , I.A. Melzer-Pellmann , M. Mendizabal Morentin , J. Metwally, A.B. Meyer , G. Milella ,
M. Mormile , A. Mussgiller , A. Nürnberg , Y. Otarid, D. Pérez Adán , A. Raspereza,
B. Ribeiro Lopes , J. Rübenach, A. Saggio , A. Saibel , M. Savitskyi , M. Scham26,23 ,
V. Scheurer, S. Schnake23 , P. Schütze , C. Schwanenberger22 , M. Shchedrolosiev ,
R.E. Sosa Ricardo , D. Stafford, N. Tonon† , M. Van De Klundert , F. Vazzoler ,
A. Ventura Barroso , R. Walsh , D. Walter , Q. Wang , Y. Wen , K. Wichmann,
L. Wiens23 , C. Wissing , S. Wuchterl , Y. Yang, A. Zimermmane Castro Santos
University of Hamburg, Hamburg, Germany
R. Aggleton, A. Albrecht , S. Albrecht , M. Antonello , S. Bein , L. Benato ,
M. Bonanomi , P. Connor , K. De Leo , M. Eich, K. El Morabit , F. Feindt, A. Fröhlich,
C. Garbers , E. Garutti , M. Hajheidari, J. Haller , A. Hinzmann , H.R. Jabusch ,
G. Kasieczka , R. Klanner , W. Korcari , T. Kramer , V. Kutzner , J. Lange ,
T. Lange , A. Lobanov , C. Matthies , A. Mehta , L. Moureaux , M. Mrowietz,
A. Nigamova , Y. Nissan, A. Paasch , K.J. Pena Rodriguez , M. Rieger , O. Rieger,
P. Schleper , M. Schröder , J. Schwandt , H. Stadie , G. Steinbrück , A. Tews, M. Wolf
Karlsruher Institut fuer Technologie, Karlsruhe, Germany
J. Bechtel , S. Brommer , M. Burkart, E. Butz , R. Caspart , T. Chwalek
A. Dierlamm , A. Droll, N. Faltermann , M. Giffels , J.O. Gosewisch, A. Gottmann
F. Hartmann21 , C. Heidecker, M. Horzela , U. Husemann , P. Keicher, M. Klute
R. Koppenhöfer , S. Maier , S. Mitra , Th. Müller , M. Neukum, G. Quast
K. Rabbertz , J. Rauser, D. Savoiu , M. Schnepf, D. Seith, I. Shvetsov, H.J. Simonis
R. Ulrich , J. van der Linden , R.F. Von Cube , M. Wassmer , M. Weber , S. Wieland
R. Wolf , S. Wozniewski , S. Wunsch

,
,
,
,
,
,

Institute of Nuclear and Particle Physics (INPP), NCSR Demokritos, Aghia Paraskevi,
Greece
G. Anagnostou, P. Assiouras , G. Daskalakis , A. Kyriakis, A. Stakia
National and Kapodistrian University of Athens, Athens, Greece
M. Diamantopoulou, D. Karasavvas, P. Kontaxakis , A. Manousakis-Katsikakis , A. Panagiotou, I. Papavergou , N. Saoulidou , K. Theofilatos , E. Tziaferi , K. Vellidis ,
E. Vourliotis

## PDF page 41

39
National Technical University of Athens, Athens, Greece
G. Bakas , T. Chatzistavrou, K. Kousouris , I. Papakrivopoulos
A. Zacharopoulou

, G. Tsipolitis,

University of Ioánnina, Ioánnina, Greece
K. Adamidis, I. Bestintzanos, I. Evangelou , C. Foudas, P. Gianneios
P. Kokkas , N. Manthos , I. Papadopoulos , J. Strologas

, P. Katsoulis,

MTA-ELTE Lendület CMS Particle and Nuclear Physics Group, Eötvös Loránd University,
Budapest, Hungary
M. Csanád , K. Farkas , M.M.A. Gadallah27 , S. Lökös28 , P. Major , K. Mandal ,
G. Pásztor , A.J. Rádl29 , O. Surányi , G.I. Veres
Wigner Research Centre for Physics, Budapest, Hungary
M. Bartók30 , G. Bencze, C. Hajdu , D. Horvath31,32 , F. Sikler

, V. Veszpremi

Institute of Nuclear Research ATOMKI, Debrecen, Hungary
N. Beni , S. Czellar, D. Fasanella , J. Karancsi30 , J. Molnar, Z. Szillasi, D. Teyssier
Institute of Physics, University of Debrecen, Debrecen, Hungary
P. Raics, B. Ujvari33
Karoly Robert Campus, MATE Institute of Technology, Gyongyos, Hungary
T. Csorgo29 , F. Nemes29 , T. Novak
Panjab University, Chandigarh, India
J. Babbar , S. Bansal , S.B. Beri, V. Bhatnagar , G. Chaudhary , S. Chauhan
N. Dhingra34 , R. Gupta, A. Kaur , A. Kaur , H. Kaur , M. Kaur , S. Kumar
P. Kumari , M. Meena , K. Sandeep , T. Sheokand, J.B. Singh35 , A. Singla
A. K. Virdi

,
,
,

University of Delhi, Delhi, India
A. Ahmed , A. Bhardwaj , B.C. Choudhary , M. Gola, S. Keshri
M. Naimuddin , P. Priyanka , K. Ranjan , S. Saumya , A. Shah

,

, A. Kumar

Saha Institute of Nuclear Physics, HBNI, Kolkata, India
S. Baradia , S. Barman36 , R. Bhattacharya , S. Bhattacharya , D. Bhowmik, S. Dutta ,
S. Dutta, B. Gomber37 , M. Maity36 , P. Palit , P.K. Rout , G. Saha , B. Sahu , S. Sarkar
Indian Institute of Technology Madras, Madras, India
P.K. Behera , S.C. Behera , P. Kalbhor , J.R. Komaragiri38 , D. Kumar38 , A. Muhammad , L. Panwar38 , R. Pradhan , P.R. Pujahari , A. Sharma , A.K. Sikdar ,
P.C. Tiwari38 , S. Verma
Bhabha Atomic Research Centre, Mumbai, India
K. Naskar39
Tata Institute of Fundamental Research-A, Mumbai, India
T. Aziz, S. Dugad, M. Kumar , G.B. Mohanty , P. Suryadevara
Tata Institute of Fundamental Research-B, Mumbai, India
S. Banerjee , R. Chudasama , M. Guchait , S. Karmakar
K. Mazumdar , S. Mukherjee , A. Thachayath

, S. Kumar

, G. Majumder

,

National Institute of Science Education and Research, An OCC of Homi Bhabha National
Institute, Bhubaneswar, Odisha, India

## PDF page 42

40
S. Bahinipati40 , A.K. Das, C. Kar , P. Mal , T. Mishra , V.K. Muraleedharan Nair Bindhu41 , A. Nayak41 , P. Saha , N. Sur , S.K. Swain, D. Vats41
Indian Institute of Science Education and Research (IISER), Pune, India
A. Alpana , S. Dube , B. Kansal , A. Laha , S. Pandey , A. Rastogi , S. Sharma
Isfahan University of Technology, Isfahan, Iran
H. Bakhshiansohi42 , E. Khazaie , M. Zeinali43
Institute for Research in Fundamental Sciences (IPM), Tehran, Iran
S. Chenarani44 , S.M. Etesami , M. Khakzad , M. Mohammadi Najafabadi
University College Dublin, Dublin, Ireland
M. Grunewald
INFN Sezione di Baria , Università di Barib , Politecnico di Baric , Bari, Italy
M. Abbresciaa,b , R. Alya,c,45 , C. Arutaa,b , A. Colaleoa , D. Creanzaa,c
N. De Filippisa,c , M. De Palmaa,b , A. Di Florioa,b , W. Elmetenaweea,b , F. Erricoa,b
L. Fiorea , G. Iasellia,c , M. Incea,b , G. Maggia,c , M. Maggia , I. Margjekaa,b
V. Mastrapasquaa,b , S. Mya,b , S. Nuzzoa,b , A. Pellecchiaa,b , A. Pompilia,b
G. Pugliesea,c , R. Radognaa , D. Ramosa , A. Ranieria , G. Selvaggia,b
L. Silvestrisa , F.M. Simonea,b , Ü. Sözbilira , A. Stamerraa , R. Vendittia
P. Verwilligena , A. Zazaa,b

,
,
,
,
,
,

INFN Sezione di Bolognaa , Università di Bolognab , Bologna, Italy
G. Abbiendia , C. Battilanaa,b , D. Bonacorsia,b , L. Borgonovia , L. Brigliadoria ,
R. Campaninia,b , P. Capiluppia,b , A. Castroa,b , F.R. Cavalloa , M. Cuffiania,b ,
G.M. Dallavallea , T. Diotalevia,b , F. Fabbria , A. Fanfania,b , P. Giacomellia ,
L. Giommia,b , C. Grandia , L. Guiduccia,b , S. Lo Meoa,46 , L. Lunertia,b ,
S. Marcellinia , G. Masettia , F.L. Navarriaa,b , A. Perrottaa , F. Primaveraa,b ,
A.M. Rossia,b , T. Rovellia,b , G.P. Sirolia,b
INFN Sezione di Cataniaa , Università di Cataniab , Catania, Italy
S. Costaa,b,47 , A. Di Mattiaa , R. Potenzaa,b , A. Tricomia,b,47 , C. Tuvea,b
INFN Sezione di Firenzea , Università di Firenzeb , Firenze, Italy
G. Barbaglia , B. Camaiania,b , A. Cassesea , R. Ceccarellia,b , V. Ciullia,b
C. Civininia , R. D’Alessandroa,b , E. Focardia,b , G. Latinoa,b , P. Lenzia,b
M. Lizzoa,b , M. Meschinia , S. Paolettia , R. Seiditaa,b , G. Sguazzonia , L. Viliania

,
,

INFN Laboratori Nazionali di Frascati, Frascati, Italy
L. Benussi , S. Bianco , D. Piccolo
INFN Sezione di Genovaa , Università di Genovab , Genova, Italy
M. Bozzoa,b , F. Ferroa , R. Mulargiaa , E. Robuttia , S. Tosia,b
INFN Sezione di Milano-Bicoccaa , Università di Milano-Bicoccab , Milano, Italy
A. Benagliaa , G. Boldrinia , F. Brivioa,b , F. Cetorellia,b , F. De Guioa,b
M.E. Dinardoa,b , P. Dinia , S. Gennaia , A. Ghezzia,b , P. Govonia,b , L. Guzzia,b
M.T. Lucchinia,b , M. Malbertia , S. Malvezzia , A. Massironia , D. Menascea
L. Moronia , M. Paganonia,b , D. Pedrinia , B.S. Pinolinia , S. Ragazzia,b , N. Redaellia
T. Tabarelli de Fatisa,b , D. Zuoloa,b

,
,
,
,

INFN Sezione di Napolia , Università di Napoli ’Federico II’b , Napoli, Italy; Università della
Basilicatac , Potenza, Italy; Università G. Marconid , Roma, Italy

## PDF page 43

41
S. Buontempoa , F. Carnevalia,b , N. Cavalloa,c , A. De Iorioa,b , F. Fabozzia,c
A.O.M. Iorioa,b , L. Listaa,b,48 , S. Meolaa,d,21 , P. Paoluccia,21 , B. Rossia
C. Sciaccaa,b

,
,

INFN Sezione di Padovaa , Università di Padovab , Padova, Italy; Università di Trentoc ,
Trento, Italy
P. Azzia , N. Bacchettaa,49 , D. Biselloa,b , P. Bortignona , A. Bragagnoloa,b ,
R. Carlina,b , P. Checchiaa , T. Dorigoa , F. Gasparinia,b , U. Gasparinia,b ,
G. Grossoa , L. Layera,50 , E. Lusiania , M. Margonia,b , F. Marinia , A.T. Meneguzzoa,b ,
J. Pazzinia,b , P. Ronchesea,b , R. Rossina,b , F. Simonettoa,b , G. Stronga , M. Tosia,b ,
H. Yarara,b , M. Zanettia,b , P. Zottoa,b , A. Zucchettaa,b , G. Zumerlea,b
INFN Sezione di Paviaa , Università di Paviab , Pavia, Italy
C. Aimèa,b , A. Braghieria , S. Calzaferria,b , D. Fiorinaa,b
C. Riccardia,b , P. Salvinia , I. Vaia , P. Vituloa,b

, P. Montagnaa,b

, V. Rea

,

INFN Sezione di Perugiaa , Università di Perugiab , Perugia, Italy
P. Asenova,51 , G.M. Bileia , D. Ciangottinia,b , L. Fanòa,b , M. Magherinia,b
G. Mantovania,b , V. Mariania,b , M. Menichellia , F. Moscatellia,51 , A. Piccinellia,b
M. Presillaa,b , A. Rossia,b , A. Santocchiaa,b , D. Spigaa , T. Tedeschia,b

,
,

INFN Sezione di Pisaa , Università di Pisab , Scuola Normale Superiore di Pisac , Pisa, Italy;
Università di Sienad , Siena, Italy
P. Azzurria , G. Bagliesia , V. Bertacchia,c , L. Bianchinia,b , T. Boccalia ,
E. Bossinia,b , D. Bruschinia,c , R. Castaldia , M.A. Cioccia,b , V. D’Amantea,d ,
R. Dell’Orsoa , M.R. Di Domenicoa,d , S. Donatoa , A. Giassia , F. Ligabuea,c ,
E. Mancaa,c , G. Mandorlia,c , D. Matos Figueiredoa , A. Messineoa,b , M. Musicha,b ,
F. Pallaa , S. Paroliaa,b , G. Ramirez-Sancheza,c , A. Rizzia,b , G. Rolandia,c ,
S. Roy Chowdhurya,c , A. Scribanoa , N. Shafieia,b , P. Spagnoloa , R. Tenchinia ,
G. Tonellia,b , N. Turinia,d , A. Venturia , P.G. Verdinia
INFN Sezione di Romaa , Sapienza Università di Romab , Roma, Italy
P. Barriaa , M. Campanaa,b , F. Cavallaria , D. Del Rea,b , E. Di Marcoa
M. Diemoza , E. Longoa,b , P. Meridiania , G. Organtinia,b , F. Pandolfia
R. Paramattia,b , C. Quarantaa,b , S. Rahatloua,b , C. Rovellia , F. Santanastasioa,b
L. Soffia , R. Tramontanoa,b

,
,
,

INFN Sezione di Torinoa , Università di Torinob , Torino, Italy; Università del Piemonte
Orientalec , Novara, Italy
N. Amapanea,b , R. Arcidiaconoa,c , S. Argiroa,b , M. Arneodoa,c , N. Bartosika ,
R. Bellana,b , A. Belloraa,b , J. Berenguer Antequeraa,b , C. Biinoa , N. Cartigliaa ,
M. Costaa,b , R. Covarellia,b , N. Demariaa , M. Grippoa,b , B. Kiania,b ,
F. Leggera , C. Mariottia , S. Masellia , A. Meccaa,b , E. Migliorea,b , E. Monteila,b ,
M. Montenoa , M.M. Obertinoa,b , G. Ortonaa , L. Pachera,b , N. Pastronea ,
M. Pelliccionia , M. Ruspaa,c , K. Shchelinaa , F. Sivieroa,b , V. Solaa , A. Solanoa,b ,
D. Soldia,b , A. Staianoa , M. Tornagoa,b , D. Trocinoa , G. Umoreta,b ,
A. Vagnerinia,b
INFN Sezione di Triestea , Università di Triesteb , Trieste, Italy
S. Belfortea , V. Candelisea,b , M. Casarsaa , F. Cossuttia
G. Della Riccaa,b , G. Sorrentinoa,b
Kyungpook National University, Daegu, Korea

, A. Da Rolda,b

,

## PDF page 44

42
S. Dogra , C. Huh , B. Kim , D.H. Kim , G.N. Kim
C.S. Moon , Y.D. Oh , S.I. Pak , S. Sekmen , Y.C. Yang

, J. Kim, J. Lee

, S.W. Lee

,

Chonnam National University, Institute for Universe and Elementary Particles, Kwangju,
Korea
H. Kim , D.H. Moon
Hanyang University, Seoul, Korea
E. Asilar , T.J. Kim , J. Park
Korea University, Seoul, Korea
S. Cho, S. Choi , B. Hong , K. Lee, K.S. Lee

, J. Lim, J. Park, S.K. Park, J. Yoo

Kyung Hee University, Department of Physics, Seoul, Korea
J. Goh
Sejong University, Seoul, Korea
H. S. Kim , Y. Kim, S. Lee, G.B. Yu
Seoul National University, Seoul, Korea
J. Almond, J.H. Bhyun, J. Choi , S. Jeon , W. Jun , J. Kim , J. Kim , J.S. Kim, S. Ko ,
H. Kwon , H. Lee , J. Lee , S. Lee, B.H. Oh , M. Oh , S.B. Oh , H. Seo , U.K. Yang,
I. Yoon
University of Seoul, Seoul, Korea
W. Jang , D.Y. Kang, Y. Kang , D. Kim , S. Kim , B. Ko, J.S.H. Lee
I.C. Park , Y. Roh, M.S. Ryu , D. Song, Watson, I.J. , S. Yang

, Y. Lee

, J.A. Merlin,

Yonsei University, Department of Physics, Seoul, Korea
S. Ha , H.D. Yoo
Sungkyunkwan University, Suwon, Korea
M. Choi , H. Lee, Y. Lee , I. Yu
College of Engineering and Technology, American University of the Middle East (AUM),
Dasman, Kuwait
T. Beyrouthy, Y. Maghrbi
Riga Technical University, Riga, Latvia
K. Dreimanis , A. Gaile , A. Potrebko

, T. Torims, V. Veckalns

Vilnius University, Vilnius, Lithuania
M. Ambrozas , A. Carvalho Antunes De Oliveira
G. Tamulaitis

, A. Juodagalvis

, A. Rinkevicius

,

National Centre for Particle Physics, Universiti Malaya, Kuala Lumpur, Malaysia
N. Bin Norjoharuddeen , S.Y. Hoh52 , I. Yusuff52 , Z. Zolkapli
Universidad de Sonora (UNISON), Hermosillo, Mexico
J.F. Benitez , A. Castaneda Hernandez , H.A. Encinas Acosta, L.G. Gallegos Marı́ñez,
M. León Coello , J.A. Murillo Quijada , A. Sehrawat , L. Valencia Palomo
Centro de Investigacion y de Estudios Avanzados del IPN, Mexico City, Mexico
G. Ayala , H. Castilla-Valdez , E. De La Cruz-Burelo , I. Heredia-De La Cruz53
R. Lopez-Fernandez ,
C.A. Mondragon Herrera,
D.A. Perez Navarro
A. Sánchez Hernández

,
,

## PDF page 45

43
Universidad Iberoamericana, Mexico City, Mexico
C. Oropeza Barrera , F. Vazquez Valencia
Benemerita Universidad Autonoma de Puebla, Puebla, Mexico
I. Pedraza , H.A. Salazar Ibarguen , C. Uribe Estrada
University of Montenegro, Podgorica, Montenegro
I. Bubanja, J. Mijuskovic54 , N. Raicevic
National Centre for Physics, Quaid-I-Azam University, Islamabad, Pakistan
A. Ahmad , M.I. Asghar, A. Awais , M.I.M. Awan, M. Gul , H.R. Hoorani
W.A. Khan , M. Shoaib , M. Waqas

,

AGH University of Science and Technology Faculty of Computer Science, Electronics and
Telecommunications, Krakow, Poland
V. Avati, L. Grzanka , M. Malawski
National Centre for Nuclear Research, Swierk, Poland
H. Bialkowska , M. Bluj , B. Boimska , M. Górski
P. Zalewski

, M. Kazana

, M. Szleper

,

Institute of Experimental Physics, Faculty of Physics, University of Warsaw, Warsaw, Poland
K. Bunkowski , K. Doroba , A. Kalinowski , M. Konecki , J. Krolikowski
Laboratório de Instrumentação e Fı́sica Experimental de Partı́culas, Lisboa, Portugal
M. Araujo , P. Bargassa , D. Bastos , A. Boletti , P. Faccioli , M. Gallinaro , J. Hollar
N. Leonardo , T. Niknejad , M. Pisano , J. Seixas , O. Toldaiev , J. Varela

,

VINCA Institute of Nuclear Sciences, University of Belgrade, Belgrade, Serbia
P. Adzic55 , M. Dordevic , P. Milenovic , J. Milosevic
Centro de Investigaciones Energéticas Medioambientales y Tecnológicas (CIEMAT),
Madrid, Spain
M. Aguilar-Benitez, J. Alcaraz Maestre , A. Álvarez Fernández , M. Barrio Luna,
Cristina F. Bedoya , C.A. Carrillo Montoya , M. Cepeda , M. Cerrada , N. Colino ,
B. De La Cruz , A. Delgado Peris , J.P. Fernández Ramos , J. Flix , M.C. Fouz ,
O. Gonzalez Lopez , S. Goy Lopez , J.M. Hernandez , M.I. Josa , J. León Holgado ,
D. Moran , C. Perez Dengra , A. Pérez-Calero Yzquierdo , J. Puerta Pelayo ,
I. Redondo , D.D. Redondo Ferrero , L. Romero, S. Sánchez Navas , J. Sastre ,
L. Urda Gómez , J. Vazquez Escobar , C. Willmott
Universidad Autónoma de Madrid, Madrid, Spain
J.F. de Trocóniz
Universidad de Oviedo, Instituto Universitario de Ciencias y Tecnologı́as Espaciales de
Asturias (ICTEA), Oviedo, Spain
B. Alvarez Gonzalez , J. Cuevas , J. Fernandez Menendez , S. Folgueras , I. Gonzalez Caballero , J.R. González Fernández , E. Palencia Cortezon , C. Ramón Álvarez ,
V. Rodrı́guez Bouza , A. Soto Rodrı́guez , A. Trapote , N. Trevisani , C. Vico Villalba
Instituto de Fı́sica de Cantabria (IFCA), CSIC-Universidad de Cantabria, Santander, Spain
J.A. Brochero Cifuentes , I.J. Cabrillo , A. Calderon , J. Duarte Campderros ,
M. Fernandez , C. Fernandez Madrazo , P.J. Fernández Manteca , A. Garcı́a Alonso,
G. Gomez , C. Lasaosa Garcı́a , C. Martinez Rivero , P. Martinez Ruiz del Arbol ,
F. Matorras , P. Matorras Cuevas , J. Piedra Gomez , C. Prieels, A. Ruiz-Jimeno ,

## PDF page 46

44
L. Scodellaro

, I. Vila

, J.M. Vizan Garcia

University of Colombo, Colombo, Sri Lanka
M.K. Jayananda , B. Kailasapathy56 , D.U.J. Sonnadara

, D.D.C. Wickramarathna

University of Ruhuna, Department of Physics, Matara, Sri Lanka
W.G.D. Dharmaratna , K. Liyanage , N. Perera , N. Wickramage
CERN, European Organization for Nuclear Research, Geneva, Switzerland
D. Abbaneo , J. Alimena , E. Auffray , G. Auzinger , J. Baechler, P. Baillon† ,
D. Barney , J. Bendavid , M. Bianco , B. Bilin , A. Bocci , E. Brondolin , C. Caillol ,
T. Camporesi , G. Cerminara , N. Chernyavskaya , S.S. Chhibra , S. Choudhury,
M. Cipriani , L. Cristella , D. d’Enterria , A. Dabrowski , A. David , A. De Roeck ,
M.M. Defranchis , M. Deile , M. Dobson , M. Dünser , N. Dupont, A. Elliott-Peisert,
F. Fallavollita57 , A. Florent , L. Forthomme , G. Franzoni , W. Funk , S. Ghosh ,
S. Giani, D. Gigi, K. Gill, F. Glege , L. Gouskos , E. Govorkova , M. Haranko ,
J. Hegeman , V. Innocente , T. James , P. Janot , J. Kaspar , J. Kieseler , M. Komm ,
N. Kratochwil , S. Laurila , P. Lecoq , A. Lintuluoto , C. Lourenço , B. Maier ,
L. Malgeri , M. Mannelli , A.C. Marini , F. Meijers , S. Mersi , E. Meschi ,
F. Moortgat , M. Mulders , S. Orfanelli, L. Orsini, F. Pantaleo , E. Perez, M. Peruzzi ,
A. Petrilli , G. Petrucciani , A. Pfeiffer , M. Pierini , D. Piparo , M. Pitt , H. Qu ,
T. Quast, D. Rabady , A. Racz, G. Reales Gutiérrez, M. Rovere , H. Sakulin , J. SalfeldNebgen , S. Scarfi, M. Selvaggi , A. Sharma , P. Silva , W. Snoeys , P. Sphicas58 ,
A.G. Stahl Leiton , S. Summers , K. Tatar , V.R. Tavolaro , D. Treille , P. Tropea ,
A. Tsirou, J. Wanczyk59 , K.A. Wozniak , W.D. Zeuner
Paul Scherrer Institut, Villigen, Switzerland
L. Caminada60 , A. Ebrahimi , W. Erdmann , R. Horisberger , Q. Ingram
H.C. Kaestli , D. Kotlinski , C. Lange , M. Missiroli60 , L. Noehte60 , T. Rohe

,

ETH Zurich - Institute for Particle Physics and Astrophysics (IPA), Zurich, Switzerland
T.K. Aarrestad , K. Androsov59 , M. Backhaus , P. Berger, A. Calandri , A. De Cosa
G. Dissertori , M. Dittmar, M. Donegà , F. Eble , M. Galli , K. Gedia , F. Glessgen
T.A. Gómez Espinosa , C. Grab , D. Hits , W. Lustermann , A.-M. Lyon
R.A. Manzoni , L. Marchese , C. Martin Perez , A. Mascellani59 , M.T. Meinhard
F. Nessi-Tedaldi , J. Niedziela , F. Pauss , V. Perovic , S. Pigazzini , M.G. Ratti
M. Reichmann , C. Reissel , T. Reitenspiess , B. Ristic , D. Ruini, D.A. Sanz Becerra
J. Steggemann59 , D. Valsecchi21 , R. Wallny

,
,
,
,
,
,

Universität Zürich, Zurich, Switzerland
C. Amsler61 , P. Bärtschi , C. Botta , D. Brzhechko, M.F. Canelli , K. Cormier ,
A. De Wit , R. Del Burgo, J.K. Heikkilä , M. Huwiler , W. Jin , A. Jofrehei , B. Kilminster , S. Leontsinis , S.P. Liechti , A. Macchiolo , P. Meiring ,
V.M. Mikuni , U. Molinatti , I. Neutelings , A. Reimers , P. Robmann, S. Sanchez Cruz ,
K. Schweiger , M. Senger , Y. Takahashi
National Central University, Chung-Li, Taiwan
C. Adloff62 , C.M. Kuo, W. Lin, S.S. Yu
National Taiwan University (NTU), Taipei, Taiwan
L. Ceard, Y. Chao , K.F. Chen , P.s. Chen, H. Cheng , W.-S. Hou
E. Paganis , A. Psallidas, A. Steen , H.y. Wu, E. Yazgan , P.r. Yu

, Y.y. Li

, R.-S. Lu

Chulalongkorn University, Faculty of Science, Department of Physics, Bangkok, Thailand

,

## PDF page 47

45
C. Asawatangtrakuldee

, N. Srimanobhas

Çukurova University, Physics Department, Science and Art Faculty, Adana, Turkey
D. Agyel , F. Boran , Z.S. Demiroglu , F. Dolek , I. Dumanoglu63 , E. Eskut,
Y. Guler64 , E. Gurpinar Guler64 , C. Isik , O. Kara, A. Kayis Topaksu , U. Kiminsu ,
G. Onengut , K. Ozdemir65 , A. Polatoz , A.E. Simsek , B. Tali66 , U.G. Tok ,
S. Turkcapar , E. Uslan , I.S. Zorbakir
Middle East Technical University, Physics Department, Ankara, Turkey
G. Karapinar, K. Ocalan67 , M. Yalvac68
Bogazici University, Istanbul, Turkey
B. Akgun , I.O. Atakisi , E. Gülmez
S. Tekten71

, M. Kaya69

, O. Kaya70

, Ö. Özçelik

,

, B. Isildak74

, B. Kaynak

,

Istanbul Technical University, Istanbul, Turkey
A. Cakir , K. Cankocak63 , Y. Komurcu , S. Sen72
Istanbul University, Istanbul, Turkey
O. Aydilek , S. Cerci66 , B. Hacisahinoglu , I. Hos73
S. Ozkorucuklu , C. Simsek , D. Sunar Cerci66

Institute for Scintillation Materials of National Academy of Science of Ukraine, Kharkiv,
Ukraine
B. Grynyov
National Science Centre, Kharkiv Institute of Physics and Technology, Kharkiv, Ukraine
L. Levchuk
University of Bristol, Bristol, United Kingdom
D. Anthony , E. Bhal , J.J. Brooke , A. Bundock , E. Clement , D. Cussans
H. Flacher , M. Glowacki, J. Goldstein , G.P. Heath, H.F. Heath , L. Kreczko
B. Krikler , S. Paramesvaran , S. Seif El Nasr-Storey, V.J. Smith , N. Stylianou75
K. Walkingshaw Pass, R. White

,
,
,

Rutherford Appleton Laboratory, Didcot, United Kingdom
A.H. Ball, K.W. Bell , A. Belyaev76 , C. Brew , R.M. Brown , D.J.A. Cockerill ,
C. Cooke , K.V. Ellis, K. Harder , S. Harper , M.-L. Holmberg77 , J. Linacre ,
K. Manolopoulos, D.M. Newbold , E. Olaiya, D. Petyt , T. Reis , T. Schuh, C.H. ShepherdThemistocleous , I.R. Tomalin, T. Williams
Imperial College, London, United Kingdom
R. Bainbridge , P. Bloch , S. Bonomally, J. Borg , S. Breeze, C.E. Brown , O. Buchmuller,
V. Cacchio, V. Cepaitis , G.S. Chahal78 , D. Colling , J.S. Dancu, P. Dauncey ,
G. Davies , J. Davies, M. Della Negra , S. Fayer, G. Fedi , G. Hall , M.H. Hassanshahi ,
A. Howard, G. Iles , J. Langford , L. Lyons , A.-M. Magnan , S. Malik, A. Martelli ,
M. Mieskolainen , D.G. Monk , J. Nash79 , M. Pesaresi, B.C. Radburn-Smith ,
D.M. Raymond, A. Richards, A. Rose , E. Scott , C. Seez , A. Shtipliyski, R. Shukla ,
A. Tapper , K. Uchida , G.P. Uttley , L.H. Vage, T. Virdee21 , M. Vojinovic ,
N. Wardle , S.N. Webb , D. Winterbottom
Brunel University, Uxbridge, United Kingdom
K. Coldham, J.E. Cole , A. Khan, P. Kyberd , I.D. Reid
Baylor University, Waco, Texas, USA

, L. Teodorescu

## PDF page 48

46
S. Abdullin , A. Brinkerhoff , B. Caraway , J. Dittmann , K. Hatakeyama , A.R. Kanuganti , B. McMaster , M. Saunders , S. Sawant , C. Sutantawibul , J. Wilson
Catholic University of America, Washington, DC, USA
R. Bartek , A. Dominguez , R. Uniyal , A.M. Vargas Hernandez
The University of Alabama, Tuscaloosa, Alabama, USA
A. Buccilli , S.I. Cooper , D. Di Croce , S.V. Gleyzer
P. Rumerio80 , C. West

, C. Henderson

, C.U. Perez

,

Boston University, Boston, Massachusetts, USA
A. Akpinar , A. Albert , D. Arcaro , C. Cosby , Z. Demiragli , C. Erice
E. Fontanesi , D. Gastler , S. May , J. Rohlf , K. Salyer , D. Sperka , D. Spitzbart
I. Suarez , A. Tsatsos , S. Yuan

,
,

Brown University, Providence, Rhode Island, USA
G. Benelli , B. Burkle , X. Coubez23 , D. Cutts , M. Hadley , U. Heintz , J.M. Hogan81
T. Kwon , G. Landsberg , K.T. Lau , D. Li, J. Luo , M. Narain, N. Pervan , S. Sagir82
F. Simpson , E. Usai , W.Y. Wong, X. Yan , D. Yu , W. Zhang

,
,

University of California, Davis, Davis, California, USA
J. Bonilla , C. Brainerd , R. Breedon , M. Calderon De La Barca Sanchez , M. Chertok
J. Conway , P.T. Cox , R. Erbacher , G. Haza , F. Jensen , O. Kukral , G. Mocellin
M. Mulhearn , D. Pellett , B. Regnery , D. Taylor , Y. Yao , F. Zhang

,
,

University of California, Los Angeles, California, USA
M. Bachtis , R. Cousins , A. Dasgupta, A. Datta
M. Ignatenko , M.A. Iqbal , T. Lam , W.A. Nash
B. Stone , V. Valuev

,
,

, D. Hamilton , J. Hauser
, S. Regnard , D. Saltzberg

University of California, Riverside, Riverside, California, USA
Y. Chen, R. Clare , J.W. Gary , M. Gordon, G. Hanson , G. Karapostoli
N. Manganelli , W. Si , S. Wimpenny

, O.R. Long

,

University of California, San Diego, La Jolla, California, USA
J.G. Branson, P. Chang , S. Cittolin, S. Cooperstein , D. Diaz , J. Duarte , R. Gerosa ,
L. Giannini , J. Guiang , R. Kansal , V. Krutelyov , R. Lee , J. Letts , M. Masciovecchio , F. Mokhtar , M. Pieri , B.V. Sathia Narayanan , V. Sharma , M. Tadel ,
F. Würthwein , Y. Xiang , A. Yagil
University of California, Santa Barbara - Department of Physics, Santa Barbara, California,
USA
N. Amin, C. Campagnari , M. Citron , G. Collura , A. Dorsett , V. Dutta ,
J. Incandela , M. Kilpatrick , J. Kim , A.J. Li , B. Marsh, P. Masterson , H. Mei ,
M. Oshiro , M. Quinnan , J. Richman , U. Sarica , R. Schmitz , F. Setti , J. Sheplock ,
P. Siddireddy, D. Stuart , S. Wang
California Institute of Technology, Pasadena, California, USA
A. Bornheim , O. Cerri, I. Dutta , J.M. Lawhorn , N. Lu , J. Mao , H.B. Newman ,
T. Q. Nguyen , M. Spiropulu , J.R. Vlimant , C. Wang , S. Xie , Z. Zhang , R.Y. Zhu
Carnegie Mellon University, Pittsburgh, Pennsylvania, USA
J. Alison , S. An , M.B. Andrews , P. Bryant , T. Ferguson , A. Harilal , C. Liu
T. Mudholkar , S. Murthy , M. Paulini , A. Roberts , A. Sanchez , W. Terrill

,

## PDF page 49

47
University of Colorado Boulder, Boulder, Colorado, USA
J.P. Cumalat , W.T. Ford , A. Hassani , G. Karathanasis , E. MacDonald, R. Patel,
A. Perloff , C. Savard , N. Schonbeck , K. Stenson , K.A. Ulmer , S.R. Wagner ,
N. Zipper
Cornell University, Ithaca, New York, USA
J. Alexander , S. Bright-Thonney , X. Chen , D.J. Cranshaw , J. Fan , X. Fan
D. Gadkari , S. Hogan , J. Monroy , J.R. Patterson , D. Quach , J. Reichert
M. Reid , A. Ryd , J. Thom , P. Wittich , R. Zou

,
,

Fermi National Accelerator Laboratory, Batavia, Illinois, USA
M. Albrow , M. Alyari , G. Apollinari , A. Apresyan , L.A.T. Bauerdick , D. Berry
J. Berryhill , P.C. Bhat , K. Burkett , J.N. Butler , A. Canepa , G.B. Cerati
H.W.K. Cheung , F. Chlebana , K.F. Di Petrillo , J. Dickinson , V.D. Elvira , Y. Feng
J. Freeman , A. Gandrakota , Z. Gecse , L. Gray , D. Green, S. Grünendahl
O. Gutsche , R.M. Harris , R. Heller , T.C. Herwig , J. Hirschauer , L. Horyn
B. Jayatilaka , S. Jindariani , M. Johnson , U. Joshi , T. Klijnsma , B. Klima
K.H.M. Kwok , S. Lammel , D. Lincoln , R. Lipton , T. Liu , C. Madrid
K. Maeshima , C. Mantilla , D. Mason , P. McBride , P. Merkel , S. Mrenna
S. Nahn , J. Ngadiuba , V. Papadimitriou , N. Pastika , K. Pedro , C. Pena83
F. Ravera , A. Reinsvold Hall84 , L. Ristori , E. Sexton-Kennedy , N. Smith
A. Soha , L. Spiegel , J. Strait , L. Taylor , S. Tkaczyk , N.V. Tran , L. Uplegger
E.W. Vaandering , H.A. Weber , I. Zoi

,
,
,
,
,
,
,
,
,
,
,

University of Florida, Gainesville, Florida, USA
P. Avery , D. Bourilkov , L. Cadamuro , V. Cherepanov , R.D. Field, D. Guerrero ,
M. Kim, E. Koenig , J. Konigsberg , A. Korytov , K.H. Lo, K. Matchev , N. Menendez ,
G. Mitselmakher , A. Muthirakalayil Madhu , N. Rawal , D. Rosenzweig , S. Rosenzweig , K. Shi , J. Wang , Z. Wu
Florida State University, Tallahassee, Florida, USA
T. Adams , A. Askew , R. Habibullah , V. Hagopian , R. Khurana, T. Kolberg
G. Martinez, H. Prosper , C. Schiber, O. Viazlo , R. Yohay , J. Zhang

,

Florida Institute of Technology, Melbourne, Florida, USA
M.M. Baarmand , S. Butalla , T. Elkafrawy85 , M. Hohlmann
D. Noonan , M. Rahmani, F. Yumiceva

, R. Kumar Verma

,

University of Illinois at Chicago (UIC), Chicago, Illinois, USA
M.R. Adams , H. Becerril Gonzalez , R. Cavanaugh , S. Dittmer , O. Evdokimov
C.E. Gerber , D.J. Hofman , D. S. Lemos , A.H. Merrit , C. Mills , G. Oh , T. Roy
S. Rudrabhatla , M.B. Tonjes , N. Varelas , X. Wang , Z. Ye , J. Yoo

,
,

The University of Iowa, Iowa City, Iowa, USA
M. Alhusseini , K. Dilsiz86 , L. Emediato , R.P. Gandrajula , O.K. Köseyan , J.-P. Merlo,
A. Mestvirishvili87 , J. Nachtman , H. Ogul88 , Y. Onel , A. Penzo , C. Snyder,
E. Tiras89
Johns Hopkins University, Baltimore, Maryland, USA
O. Amram , B. Blumenfeld , L. Corcodilos , J. Davis
P. Maksimovic , J. Roskes , M. Swartz , T.Á. Vámi

, A.V. Gritsan

The University of Kansas, Lawrence, Kansas, USA
A. Abreu , L.F. Alcerro Alcerro , J. Anguiano , P. Baringer

, A. Bean

, S. Kyriacou

,

, Z. Flowers

,

## PDF page 50

48
T. Isidori , S. Khalil , J. King , G. Krintiras , M. Lazarovits , C. Le Mahieu
C. Lindsey, J. Marquez , N. Minafra , M. Murray , M. Nickel , C. Rogan , C. Royon
R. Salvatico , S. Sanders , E. Schmitz , C. Smith , Q. Wang , Z. Warner, J. Williams
G. Wilson
Kansas State University, Manhattan, Kansas, USA
B. Allmond , S. Duric, R. Gujju Gurunadha , A. Ivanov
Y. Maravin , T. Mitchell, A. Modak, K. Nam, J. Natoli , D. Roy

, K. Kaadze

,
,
,

, D. Kim,

Lawrence Livermore National Laboratory, Livermore, California, USA
F. Rebassoo , D. Wright
University of Maryland, College Park, Maryland, USA
E. Adams , A. Baden , O. Baron, A. Belloni , S.C. Eno , N.J. Hadley , S. Jabeen
R.G. Kellogg , T. Koeth , Y. Lai , S. Lascio , A.C. Mignerey , S. Nabili , C. Palmer
C. Papageorgakis , M. Seidel , L. Wang , K. Wong

,
,

Massachusetts Institute of Technology, Cambridge, Massachusetts, USA
D. Abercrombie, R. Bi, W. Busza , I.A. Cali , Y. Chen , M. D’Alfonso , J. Eysermans
C. Freer , G. Gomez-Ceballos , M. Goncharov, P. Harris, M. Hu , D. Kovalskyi
J. Krupa , Y.-J. Lee , K. Long , C. Mironov , C. Paus , D. Rankin , C. Roland
G. Roland , Z. Shi , G.S.F. Stephans , J. Wang, Z. Wang , B. Wyslouch

,
,
,

University of Minnesota, Minneapolis, Minnesota, USA
R.M. Chatterjee, B. Crossman, A. Evans , J. Hiltbrand , Sh. Jain , B.M. Joshi
M. Krohn , Y. Kubota , J. Mans , M. Revering , R. Rusack , R. Saradhy
N. Schroeder , N. Strobbe , M.A. Wadud

,
,

University of Mississippi, Oxford, Mississippi, USA
L.M. Cremaldi
University of Nebraska-Lincoln, Lincoln, Nebraska, USA
K. Bloom , M. Bryson, S. Chauhan , D.R. Claes , C. Fangmeier , L. Finco , F. Golf
C. Joo , I. Kravchenko , I. Reed , J.E. Siado , G.R. Snow† , W. Tabb , A. Wightman
F. Yan , A.G. Zecchinelli

,
,

State University of New York at Buffalo, Buffalo, New York, USA
G. Agarwal , H. Bandyopadhyay , L. Hay , I. Iashvili , A. Kharchilava
M. Morris, D. Nguyen , J. Pekkanen , S. Rappoccio , A. Williams

, C. McLean

,

Northeastern University, Boston, Massachusetts, USA
G. Alverson , E. Barberis , Y. Haddad , Y. Han , A. Krishna , J. Li , J. Lidrych
G. Madigan , B. Marzocchi , D.M. Morse , V. Nguyen , T. Orimoto , A. Parker
L. Skinnari , A. Tishelman-Charny , T. Wamorkar , B. Wang , A. Wisecarver
D. Wood

,
,
,

Northwestern University, Evanston, Illinois, USA
S. Bhattacharya , J. Bueghly, Z. Chen , A. Gilbert
N. Odell , M.H. Schmitt , M. Velasco

,

, T. Gunter

, K.A. Hahn

, Y. Liu

University of Notre Dame, Notre Dame, Indiana, USA
R. Band , R. Bucci, M. Cremonesi, A. Das , R. Goldouzian , M. Hildreth ,
K. Hurtado Anampa , C. Jessop , K. Lannon , J. Lawrence , N. Loukas , L. Lutton ,
J. Mariano, N. Marinelli, I. Mcalister, T. McCauley , C. Mcgrady , K. Mohrman ,
C. Moore , Y. Musienko14 , R. Ruchti , A. Townsend , M. Wayne , H. Yockey,

## PDF page 51

49
M. Zarucki

, L. Zygala

The Ohio State University, Columbus, Ohio, USA
B. Bylsma, L.S. Durkin , B. Francis , C. Hill , A. Lesauvage
K. Wei, B.L. Winer , B. R. Yates

, M. Nunez Ornelas

,

Princeton University, Princeton, New Jersey, USA
F.M. Addesa , B. Bonham , P. Das , G. Dezoort , P. Elmer , A. Frankenthal
B. Greenberg , N. Haubrich , S. Higginbotham , A. Kalogeropoulos , G. Kopp
S. Kwan , D. Lange , D. Marlow , K. Mei , I. Ojalvo , J. Olsen , D. Stickland
C. Tully

,
,
,

University of Puerto Rico, Mayaguez, Puerto Rico, USA
S. Malik , S. Norberg
Purdue University, West Lafayette, Indiana, USA
A.S. Bakshi , V.E. Barnes , R. Chawla , S. Das , L. Gutay, M. Jones , A.W. Jung
D. Kondratyev , A.M. Koshy, M. Liu , G. Negro , N. Neumeister , G. Paspalaki
S. Piperov , A. Purohit , J.F. Schulte , M. Stojanovic , J. Thieman , F. Wang
R. Xiao , W. Xie

,
,
,

Purdue University Northwest, Hammond, Indiana, USA
J. Dolen , N. Parashar
Rice University, Houston, Texas, USA
D. Acosta , A. Baty , T. Carnahan , M. Decaro, S. Dildick , K.M. Ecklund , S. Freed,
P. Gardner, F.J.M. Geurts , A. Kumar , W. Li , B.P. Padley , R. Redjimi, J. Rotter ,
W. Shi , S. Yang , E. Yigitbasi , L. Zhang90 , Y. Zhang , X. Zuo
University of Rochester, Rochester, New York, USA
A. Bodek , P. de Barbaro , R. Demina , J.L. Dulemba , C. Fallon, T. Ferbel , M. Galanti,
A. Garcia-Bellido , O. Hindrichs , A. Khukhunaishvili , E. Ranken , R. Taus ,
G.P. Van Onsem
The Rockefeller University, New York, New York, USA
K. Goulianos
Rutgers, The State University of New Jersey, Piscataway, New Jersey, USA
B. Chiarito, J.P. Chou , Y. Gershtein , E. Halkiadakis , A. Hart , M. Heindl
O. Karacheban25 , I. Laflotte , A. Lath , R. Montalvo, K. Nash, M. Osherson , S. Salur
S. Schnetzer, S. Somalwar , R. Stone , S.A. Thayil , S. Thomas, H. Wang
University of Tennessee, Knoxville, Tennessee, USA
H. Acharya, A.G. Delannoy , S. Fiorendi , T. Holmes

,
,

, S. Spanier

Texas A&M University, College Station, Texas, USA
O. Bouhali91 , M. Dalchenko , A. Delgado , R. Eusebi , J. Gilmore , T. Huang
T. Kamon92 , H. Kim , S. Luo , S. Malhotra, R. Mueller , D. Overton , D. Rathjens
A. Safonov
Texas Tech University, Lubbock, Texas, USA
N. Akchurin , J. Damgov , V. Hegde , K. Lamichhane , S.W. Lee
S. Muthumuni , T. Peltola , I. Volobouev , Z. Wang, A. Whitbeck
Vanderbilt University, Nashville, Tennessee, USA
E. Appelt , S. Greene, A. Gurrola , W. Johns , A. Melo

, F. Romeo

,
,

, T. Mengke,

, P. Sheldon

,

## PDF page 52

50
S. Tuo

, J. Velkovska

, J. Viinikainen

University of Virginia, Charlottesville, Virginia, USA
B. Cardwell , B. Cox , G. Cummings , J. Hakala , R. Hirosky
A. Ledovskoy , A. Li , C. Neu , C.E. Perez Lara , B. Tannenwald

, M. Joyce

,

Wayne State University, Detroit, Michigan, USA
P.E. Karchin , N. Poudyal
University of Wisconsin - Madison, Madison, Wisconsin, USA
S. Banerjee , K. Black , T. Bose , S. Dasu , I. De Bruyn , P. Everaerts , C. Galloni,
H. He , M. Herndon , A. Herve , C.K. Koraka , A. Lanaro, A. Loeliger , R. Loveless ,
J. Madhusudanan Sreekala , A. Mallampalli , A. Mohammadi , D. Pinna, A. Savin,
V. Shang , V. Sharma , W.H. Smith , D. Teague, W. Vetens
Authors affiliated with an institute or an international laboratory covered by a cooperation
agreement with CERN
S. Afanasiev, V. Andreev , Yu. Andreev , T. Aushev , M. Azarkin , A. Babaev ,
A. Belyaev , V. Blinov93 , E. Boos , V. Borshch , D. Budkouski , V. Bunichev ,
O. Bychkova, M. Chadeeva93 , V. Chekhovsky, A. Dermenev , T. Dimova93 , I. Dremin ,
M. Dubinin83 , L. Dudko , V. Epshteyn , G. Gavrilov , V. Gavrilov , S. Gninenko ,
V. Golovtcov , N. Golubev , I. Golutvin, I. Gorbunov , A. Gribushin , V. Ivanchenko ,
Y. Ivanov , V. Kachanov , L. Kardapoltsev93 , V. Karjavine , A. Karneyeu , V. Kim93 ,
M. Kirakosyan, D. Kirpichnikov , M. Kirsanov , V. Klyukhin , O. Kodolova94 , D. Konstantinov , V. Korenkov , A. Kozyrev93 , N. Krasnikov , E. Kuznetsova95 , A. Lanev ,
P. Levchenko , A. Litomin, N. Lychkovskaya , V. Makarenko , A. Malakhov ,
V. Matveev93 , V. Murzin , A. Nikitenko96 , S. Obraztsov , V. Okhotnikov ,
I. Ovtin93 , V. Palichik , P. Parygin , V. Perelygin , M. Perfilov, G. Pivovarov , V. Popov,
E. Popova , O. Radchenko93 , V. Rusinov, M. Savina , V. Savrin , D. Selivanova ,
V. Shalaev , S. Shmatov , S. Shulha , Y. Skovpen93 , S. Slabospitskii , V. Smirnov ,
A. Snigirev , D. Sosnov , A. Stepennov , V. Sulimov , E. Tcherniaev , A. Terkulov ,
O. Teryaev , I. Tlisova , M. Toms , A. Toropin , L. Uvarov , A. Uzunian , E. Vlasov ,
A. Vorobyev, N. Voytishin , B.S. Yuldashev97 , A. Zarubin , I. Zhizhin , A. Zhokin
†: Deceased
1 Also at Yerevan State University, Yerevan, Armenia
2 Also at TU Wien, Vienna, Austria
3 Now at Institute of Physics, University of Graz, Graz, Austria
4 Also at Institute of Basic and Applied Sciences, Faculty of Engineering, Arab Academy for
Science, Technology and Maritime Transport, Alexandria, Egypt
5 Also at Université Libre de Bruxelles, Bruxelles, Belgium
6 Also at Universidade Estadual de Campinas, Campinas, Brazil
7 Also at Federal University of Rio Grande do Sul, Porto Alegre, Brazil
8 Also at UFMS, Nova Andradina, Brazil
9 Also at The University of the State of Amazonas, Manaus, Brazil
10 Also at University of Chinese Academy of Sciences, Beijing, China
11 Also at Nanjing Normal University Department of Physics, Nanjing, China
12 Now at The University of Iowa, Iowa City, Iowa, USA
13 Also at University of Chinese Academy of Sciences, Beijing, China
14 Also at an institute or an international laboratory covered by a cooperation agreement with
CERN
15 Now at British University in Egypt, Cairo, Egypt

## PDF page 53

51
16 Now at Cairo University, Cairo, Egypt
17 Also at Purdue University, West Lafayette, Indiana, USA
18 Also at Université de Haute Alsace, Mulhouse, France
19 Also at Department of Physics, Tsinghua University, Beijing, China
20 Also at Erzincan Binali Yildirim University, Erzincan, Turkey
21 Also at CERN, European Organization for Nuclear Research, Geneva, Switzerland
22 Also at University of Hamburg, Hamburg, Germany
23 Also at RWTH Aachen University, III. Physikalisches Institut A, Aachen, Germany
24 Also at Isfahan University of Technology, Isfahan, Iran
25 Also at Brandenburg University of Technology, Cottbus, Germany
26 Also at Forschungszentrum Jülich, Juelich, Germany
27 Also at Physics Department, Faculty of Science, Assiut University, Assiut, Egypt
28 Also at Karoly Robert Campus, MATE Institute of Technology, Gyongyos, Hungary
29 Also at Wigner Research Centre for Physics, Budapest, Hungary
30 Also at Institute of Physics, University of Debrecen, Debrecen, Hungary
31 Also at Institute of Nuclear Research ATOMKI, Debrecen, Hungary
32 Now at Universitatea Babes-Bolyai - Facultatea de Fizica, Cluj-Napoca, Romania
33 Also at Faculty of Informatics, University of Debrecen, Debrecen, Hungary
34 Also at Punjab Agricultural University, Ludhiana, India
35 Also at UPES - University of Petroleum and Energy Studies, Dehradun, India
36 Also at University of Visva-Bharati, Santiniketan, India
37 Also at University of Hyderabad, Hyderabad, India
38 Also at Indian Institute of Science (IISc), Bangalore, India
39 Also at Indian Institute of Technology (IIT), Mumbai, India
40 Also at IIT Bhubaneswar, Bhubaneswar, India
41 Also at Institute of Physics, Bhubaneswar, India
42 Also at Deutsches Elektronen-Synchrotron, Hamburg, Germany
43 Also at Sharif University of Technology, Tehran, Iran
44 Also

at Department of Physics, University of Science and Technology of Mazandaran,
Behshahr, Iran
45 Also at Helwan University, Cairo, Egypt
46 Also at Italian National Agency for New Technologies, Energy and Sustainable Economic
Development, Bologna, Italy
47 Also at Centro Siciliano di Fisica Nucleare e di Struttura Della Materia, Catania, Italy
48 Also at Scuola Superiore Meridionale, Università di Napoli ’Federico II’, Napoli, Italy
49 Also at Fermi National Accelerator Laboratory, Batavia, Illinois, USA
50 Also at Università di Napoli ’Federico II’, Napoli, Italy
51 Also at Consiglio Nazionale delle Ricerche - Istituto Officina dei Materiali, Perugia, Italy
52 Also at Department of Applied Physics, Faculty of Science and Technology, Universiti
Kebangsaan Malaysia, Bangi, Malaysia
53 Also at Consejo Nacional de Ciencia y Tecnologı́a, Mexico City, Mexico
54 Also at IRFU, CEA, Université Paris-Saclay, Gif-sur-Yvette, France
55 Also at Faculty of Physics, University of Belgrade, Belgrade, Serbia
56 Also at Trincomalee Campus, Eastern University, Sri Lanka, Nilaveli, Sri Lanka
57 Also at INFN Sezione di Pavia, Università di Pavia, Pavia, Italy
58 Also at National and Kapodistrian University of Athens, Athens, Greece
59 Also at Ecole Polytechnique Fédérale Lausanne, Lausanne, Switzerland
60 Also at Universität Zürich, Zurich, Switzerland
61 Also at Stefan Meyer Institute for Subatomic Physics, Vienna, Austria

## PDF page 54

52
62 Also at Laboratoire d’Annecy-le-Vieux de Physique des Particules, IN2P3-CNRS, Annecy-le-

Vieux, France
63 Also at Near East University, Research Center of Experimental Health Science, Mersin,
Turkey
64 Also at Konya Technical University, Konya, Turkey
65 Also at Izmir Bakircay University, Izmir, Turkey
66 Also at Adiyaman University, Adiyaman, Turkey
67 Also at Necmettin Erbakan University, Konya, Turkey
68 Also at Bozok Universitetesi Rektörlügü, Yozgat, Turkey
69 Also at Marmara University, Istanbul, Turkey
70 Also at Milli Savunma University, Istanbul, Turkey
71 Also at Kafkas University, Kars, Turkey
72 Also at Hacettepe University, Ankara, Turkey
73 Also at Istanbul University - Cerrahpasa, Faculty of Engineering, Istanbul, Turkey
74 Also at Yildiz Technical University, Istanbul, Turkey
75 Also at Vrije Universiteit Brussel, Brussel, Belgium
76 Also at School of Physics and Astronomy, University of Southampton, Southampton, United
Kingdom
77 Also at University of Bristol, Bristol, United Kingdom
78 Also at IPPP Durham University, Durham, United Kingdom
79 Also at Monash University, Faculty of Science, Clayton, Australia
80 Also at Università di Torino, Torino, Italy
81 Also at Bethel University, St. Paul, Minnesota, USA
82 Also at Karamanoğlu Mehmetbey University, Karaman, Turkey
83 Also at California Institute of Technology, Pasadena, California, USA
84 Also at United States Naval Academy, Annapolis, Maryland, USA
85 Also at Ain Shams University, Cairo, Egypt
86 Also at Bingol University, Bingol, Turkey
87 Also at Georgian Technical University, Tbilisi, Georgia
88 Also at Sinop University, Sinop, Turkey
89 Also at Erciyes University, Kayseri, Turkey
90 Also at Institute of Modern Physics and Key Laboratory of Nuclear Physics and Ion-beam
Application (MOE) - Fudan University, Shanghai, China
91 Also at Texas A&M University at Qatar, Doha, Qatar
92 Also at Kyungpook National University, Daegu, Korea
93 Also at another institute or international laboratory covered by a cooperation agreement
with CERN
94 Also at Yerevan Physics Institute, Yerevan, Armenia
95 Also at University of Florida, Gainesville, Florida, USA
96 Also at Imperial College, London, United Kingdom
97 Also at Institute of Nuclear Physics of the Uzbekistan Academy of Sciences, Tashkent,
Uzbekistan
