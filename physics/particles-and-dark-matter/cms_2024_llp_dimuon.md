Source: https://arxiv.org/abs/2402.14491v2
PDF sha256: 198188582676e446eaa04f85ffa955b8d339a874c5bde0b1b22295b4d71975de
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of cms_2024_llp_dimuon.pdf

Transcription of `cms_2024_llp_dimuon.pdf` in this directory, 49 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 2 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories; pages 1, 3-49 from the PDF's own text layer (pdftotext version 26.10.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

EUROPEAN ORGANIZATION FOR NUCLEAR RESEARCH (CERN)

CERN-EP-2024-025
2024/05/21

arXiv:2402.14491v2 [hep-ex] 20 May 2024

CMS-EXO-23-014

Search for long-lived particles decaying to final states with
a pair of muons√
in proton-proton collisions at
s = 13.6 TeV
The CMS Collaboration*

Abstract
An inclusive search for long-lived exotic particles (LLPs) decaying to final states with
a pair of muons is presented. The search uses data corresponding to an integrated
−1
luminosity
√of 36.6 fb collected by the CMS experiment from the proton-proton collisions at s = 13.6 TeV in 2022, the first year of Run 3 of the CERN LHC. The experimental signature is a pair of oppositely charged muons originating from a secondary
vertex spatially separated from the proton-proton interaction point by distances ranging from several hundred µm to several meters. The sensitivity of the search benefits
from new triggers for displaced dimuons developed for Run 3. The results are interpreted in the framework of the hidden Abelian Higgs model, in which the Higgs
boson decays to a pair of long-lived dark photons, and of an R-parity violating supersymmetry model, in which long-lived neutralinos decay to a pair of muons and a
neutrino. The limits set on these models are the most stringent to date in wide regions
of lifetimes for LLPs with masses larger than 10 GeV.

Published in the Journal of High Energy Physics as doi:10.1007/JHEP05(2024)047.

© 2024 CERN for the benefit of the CMS Collaboration. CC-BY-4.0 license
* See Appendix A for the list of collaboration members

## PDF page 2



## PDF page 3

1

1

Introduction

Long-lived particles (LLPs) that are unobserved as yet are predicted by many extensions of
the standard model (SM), in particular by various supersymmetry (SUSY) scenarios [1, 2] and
“hidden-sector” models [3, 4]. Such particles could manifest themselves through decays to SM
particles at macroscopic distances from the proton-proton (pp) interaction point (IP).
This paper describes an inclusive search for an exotic massive LLP decaying to a pair of oppositely charged muons, referred to as a “displaced dimuon”, originating from a secondary vertex
spatially separated from the IP. The analysis is based on a data set of pp collisions correspond√
ing to an integrated luminosity of 36.6 fb−1 collected with the CMS detector at s = 13.6 TeV
during 2022, the first year of Run 3 of the CERN LHC.
√ It is a continuation and extension of the
CMS analysis [5] performed using data collected at s = 13 TeV during Run 2 (2016–2018) and
corresponding to an integrated luminosity of 97.6 fb−1 (referred to below as the CMS Run 2
analysis). A minimal set of requirements and loose event selection criteria allow the search to
be sensitive to a wide range of models predicting LLPs that decay to final states that include a
pair of oppositely charged muons. Improvements in the triggers result in a significantly higher
efficiency for displaced dimuons in Run 3, particularly at dimuon masses of a few tens of GeV.
The present search explores the LLP mass range above 10 GeV and is sensitive to vertex displacements ranging from several hundred µm to several meters.
We interpret the results of the search in the frameworks of two benchmark models: the hidden
Abelian Higgs model (HAHM), in which displaced dimuons arise from decays of hypothetical
dark photons [6], and a simplified SUSY model, in which long-lived neutralinos decay to a pair
of muons and a neutrino as a result of R-parity violation (RPV) [2]. The results for the HAHM
model from Run 3 are statistically combined with the results of the Run 2 analysis [5]. The
Run 2 search [5] and the present search are complementary to a CMS search [7], which uses
data collected in Run 2 with a dedicated high-rate data stream in order to explore otherwise
inaccessible parameter space at low dimuon masses. A search for LLPs decaying
√ to displaced
dimuons has also been performed by CMS in Run 1, using data taken at s = 8 TeV and
corresponding to an integrated luminosity of 20.5 fb−1 [8, 9], and by the ATLAS Collaboration
in Run 2, using data corresponding to an integrated luminosity of 32.9 fb−1 [10, 11].
This paper is organized as follows. Section 2 describes the CMS detector. Section 3 presents
the signal models, as well as the simulated signal and background event samples. Section 4
describes the analysis strategy, the triggers, and the offline event selection. Estimation of backgrounds and the associated systematic uncertainties are described in Section 5. Section 6 summarizes the systematic uncertainties affecting signal efficiencies. Section 7 describes the results
of this analysis and their combination with the results of the CMS Run 2 analysis. The summary
of the paper is given in Section 8. Tabulated results and supplementary material for reinterpreting the results in the framework of models not explicitly considered in this paper are provided
in the HEPData record for this analysis [12].

2

The CMS detector

The central feature of the CMS detector is a superconducting solenoid of 6 m internal diameter,
providing a magnetic field of 3.8 T. Within the solenoid volume are a silicon pixel and strip
tracker extending outwards to a radius of 1.1 m, a lead tungstate crystal electromagnetic calorimeter, and a brass and scintillator hadron calorimeter, each composed of a barrel and two
endcap sections. Forward calorimeters extend the coverage in pseudorapidity η provided by
the barrel and endcap detectors. Muons are detected in gas-ionization chambers covering the

## PDF page 4

2
range |η | < 2.4 and embedded in the steel flux-return yoke outside the solenoid. The muon
system is composed of four types of chambers: drift tubes (DTs) in the barrel (|η | < 1.2), cathode strip chambers (CSCs) in the endcaps (0.9 < |η | < 2.4), resistive-plate chambers in both the
barrel and the endcaps, and gas electron multipliers in the forward regions of the endcaps. The
chambers are assembled into four “stations” at increasing distance from the IP. The stations in
the barrel are located approximately 4, 5, 6, and 7 m away from the IP radially, while the stations in the endcap are located approximately 7.0, 8.0, 9.5, and 10.5 m away from the IP along
the beam line axis on both ends of the detector. Each station provides reconstructed hits in
several detection planes, which are combined into track segments, forming the basis of muon
reconstruction in the muon system [13]. A more detailed description of the CMS detector, together with a definition of the coordinate system used and the relevant kinematical variables,
can be found in Refs. [14, 15].
Events of interest are selected using a two-tiered trigger system. The first level (L1), composed
of custom hardware processors, uses information from the calorimeters and muon detectors
to select events at a rate of approximately 100 kHz within a fixed latency of 4 µs [16]. At the
next stage, a farm of processors running a version of the full event reconstruction software
optimized for fast processing, known as the high-level trigger (HLT), reduces the event rate
to about 1 kHz before data storage [17]. At the HLT, muon candidates are reconstructed in
two steps. In the first step, referred to as Level 2 (L2), muons are reconstructed using only the
information from the muon detectors, whereas at the stage referred to as Level 3 (L3), tracker
information is also used.

3

Signal models and simulated samples

Two signal models with different final-state topologies and event kinematics are used in the
optimization of event selection criteria and in the interpretation of results. The first belongs
to a class of models featuring a “hidden” or “dark” sector of matter that does not interact
directly with the SM particles, but can manifest itself through mixing effects. This HAHM
benchmark [6, 18] contains an extra dark gauge field U(1)D , which mixes kinetically with the
hypercharge SM gauge field (“vector portal”) and gives rise to a spin-1 mediator known as
the dark photon Z D . The symmetry of U(1)D is broken by a new dark Higgs field H D , which
mixes with the SM Higgs boson H (“Higgs portal”) and gives mass m(Z D ) to the dark photon.
If there are no hidden-sector states with masses smaller than m(Z D ), the mixing through the
vector portal with the SM photon and Z boson causes the dark photon to decay exclusively to
SM particles, with a sizable branching fraction to leptons. Pair production of the Z D via the
Higgs portal with subsequent decays of dark photons via the vector portal is shown in Fig. 1
(left).
The present search probes the regime of m(Z D ) > 10 GeV with small values of the Z–Z D kinetic mixing parameter ϵ [6]. In this regime, the dark photon is long-lived, since its mean proper
lifetime τ (Z D ) is proportional to ϵ−2 . In particular, the dark photon with 10 GeV ≲ m(Z D ) <
m(H )/2 is expected to have macroscopically large mean proper decay lengths, for example,
cτ (Z D ) ≳ O(100 µm) for ϵ < O(10−6 ). The Z D production rate is governed by the branching
fraction B(H → Z D Z D ), which does not depend on ϵ but is proportional to the square of
κm2 (H )/|m2 (H ) − m2 (H D )|, where κ is the H–H D mixing parameter. Since κ and m(H D ) affect
only the overall dark photon production rate, sampling of m(Z D ) and ϵ is sufficient to explore
different kinematical and topological scenarios of the model. We generated a set of 24 simulated
HAHM event samples with m(Z D ) between 10 and 60 GeV and ϵ between 10−7 and 2 × 10−9 . In
this mass range, the model’s prediction for B(Z D → µ + µ − ) varies between 15.4% at m(Z D ) =

## PDF page 5

3

µ+

H

ZD

κ
HD

ZD

χ̃01

q̃

µ−

µ+
µ−
ν
ν

f̄

f

q

p

q̃
p

χ̃01

l
l

q

Figure 1: Feynman diagrams for (left) the HAHM model, showing the production of longlived dark photons Z D via the Higgs portal, through H–H D mixing with the parameter κ, with
subsequent decays to pairs of muons or other fermions via the vector portal; and (right) pair
production of squarks followed by q̃ → q χ̃ 01 decays, where the RPV neutralino is assumed to
be a long-lived particle that decays into a neutrino and two charged leptons.
10 GeV and 10.7% at m(Z D ) = 60 GeV. The dark Higgs boson is assumed to be heavy enough
so that H → H D H D decays are kinematically forbidden. (In the sample generation, we use
m(H D ) = 400 GeV and κ = 0.01.) The production of dark photons is modeled at leading
order by M AD G RAPH5 aMC @ NLO [19] version 2.9.9. The samples are generated only for the
dominant gluon-fusion production mechanism, but the Higgs boson production cross section
is normalized to the most
√ recent theoretical prediction for the sum of all production modes
for m(H ) = 125 GeV at s = 13.6 TeV, 59.8 pb [20, 21]. The decays of the dark photons are
modeled by PYTHIA 8.306 [22].
We also consider a simplified benchmark model inspired by RPV SUSY and featuring displaced
µ + µ − ν vertices. Unlike the HAHM, where the two-body LLP decay leads to displaced µ + µ −
vertices that are reconstructed with the dimuon invariant mass mµµ corresponding to the LLP
mass, the presence of a neutrino at the decay vertex leads to a nonpeaking mµµ distribution
with a broad spectrum below the endpoint at the LLP mass. In this model, which was used
by CMS in the Run 1 searches for displaced dimuons [8, 9] and by ATLAS in the Run 2 search
for pairs of displaced charged leptons [11], the LLP is assumed to be an RPV neutralino χ̃ 01
that results from decays of mass-degenerate squarks, q̃ → q χ̃ 01 , which are pair produced in pp
collisions. Nonzero values of RPV couplings λ122 and λ232 enable displaced χ̃ 01 decays into a
pair of oppositely charged muons and a neutrino, χ̃ 01 → µ + µ − ν [23, 24]. The Feynman diagram
for this process is shown in Fig. 1 (right).
The search uses benchmark signal samples that are generated assuming B(χ̃ 01 → µ + µ − ν ) =
B(χ̃ 01 → e + e − ν ) = 0.5, which gives rise to events with up to two displaced dimuon vertices.
To explore a wide range of kinematic variables and event topologies, we chose six m(q̃ ) values
in the range between 125 GeV and 1.6 TeV, and for each chosen m(q̃ ), generated sets of samples
with ∆m = m(q̃ ) − m(χ̃ 01 ) of 25, 200, and 650 GeV, and sets with constant m(χ̃ 01 ) values of 50
and 500 GeV such that m(χ̃ 01 ) < m(q̃ ). To study a wide range of signal displacements, each
set contains three samples with the generated cτ (χ̃ 01 ) values corresponding to mean transverse
decay lengths of approximately 3, 30, and 250 cm in the laboratory frame. All other SUSY particles (e.g., gluinos and sleptons) are assumed to be too heavy to be produced. (Their masses
1
are set to 10 TeV.) The samples are generated with PYTHIA 8.306. The squark-antisquark
production cross sections are calculated with NNLL-fast version 2.0 to approximate next-to-nextto-leading order (NNLO) in the strong coupling constant, including the resummation of soft

## PDF page 6

4
gluon emission at next-to-next-to-leading logarithmic accuracy [25]. The computation uses the
NNLO PDF4LHC21 parton distributions functions (PDFs) [26].
Since the optimization of the event selection criteria and the evaluation of the residual backgrounds are performed using data, the simulated background samples are used primarily to
gain a better understanding of the nature and composition of background events passing the
event selection. Simulated background samples used in the analysis include Drell–Yan (DY)
dilepton production; tt, tW, and tW events; W and Z boson pair production (dibosons); samples of J/ψ mesons produced in b hadron cascade decays; W+jets; and events comprised of jets
produced through the strong interaction that are enriched in muons from semileptonic decays
of hadrons containing b or c quarks.
The simulated signal and background samples are produced with PDFs NNPDF3.1 [27] at
NNLO, using the CP5 tune [28], which is optimized for these PDFs, to model the underlying
event. The passage of particles through the detector is simulated by G EANT 4 [29]. Simulated
minimum bias events are superimposed on a hard interaction in simulated events to describe
the effect of additional inelastic pp interactions within the same or neighboring bunch crossings, known as pileup. All simulated events are then reconstructed with the same algorithms
as used for data. A reweighting procedure that combines events in all simulated signal samples
at a given signal mass [30] is employed to calculate the efficiencies for lifetimes different from
those of the available samples.

4

Analysis strategy and event selection

4.1

Analysis strategy

An LLP produced in the hard interaction of the colliding protons may travel a significant distance in the detector before decaying into muons. While trajectories of the muons produced
well within the silicon tracker can be reconstructed by both the tracker and the muon system,
tracks of muons produced in the outer tracker layers or beyond can only be reconstructed by
the muon system. Since the dimuon vertex resolution and the background composition differ
dramatically depending on whether the muon is reconstructed in the tracker, we classify all
reconstructed dimuon events into three mutually exclusive categories: a) both muons are reconstructed using both the tracker and the muon system (TMS-TMS category); b) both muons
are reconstructed using only the muon system, as “standalone” muons (STA-STA category);
and c) one muon is reconstructed only in the muon system, whereas the other muon is reconstructed using both the tracker and the muon system (STA-TMS category). These three categories of events are analyzed separately, with each benefiting from dedicated event selection
criteria and background evaluation. The STA-TMS category, which had the lowest sensitivity
among the three categories in the Run 2 analysis [5], is not used for the results presented in this
paper; the results in the other two categories are statistically combined.
The beam spot is identified with the mean position of the pp interaction vertices. The primary
vertex (PV) is taken to be the vertex corresponding to the hardest scattering in the event, evaluated using tracking information alone, as described in Section 9.4.1 of Ref. [31]. A pair of
reconstructed muon tracks is fitted to a common secondary vertex (SV), which is expected to
be displaced with respect to the PV. The transverse decay vector ⃗Lxy is defined from the PV to
the SV in the plane transverse to the beam direction, while the transverse decay length Lxy is
the magnitude of this vector. The transverse impact parameter d0 is defined as the distance of
closest approach of the muon track in the transverse plane with respect to the PV.

## PDF page 7

4.2

Trigger algorithms

4.2

Trigger algorithms

5

Events were collected with dedicated triggers aimed at recording dimuons produced both
within and outside of the tracker. In Run 2, these triggers required two muons reconstructed
in the muon system alone, without using any information from the tracker [32]. They were
deployed in 2016 and 2018 and included a beam spot constraint in the muon track fits at L1
but not at the HLT. The values of the L1 pT thresholds varied from 11 and 4 GeV (for the leading and subleading L1 muons, respectively) during most of 2016 to 15 and 7 GeV at the end of
Run 2. Each HLT muon was required to be within the region |η | < 2.0 and to have transverse
momentum pT > 28 (23) GeV for 2016 (2018) data taking.
The primary goal of the trigger optimization performed for Run 3 data taking was to increase
the signal efficiency by lowering as much as possible the pT thresholds and by removing the
beam spot constraint at L1, without increasing considerably the resulting trigger rate. Two
additional sets of L1 triggers were introduced. One set comprises double-muon triggers with
either no or a very low (4.5 GeV) muon-pT threshold, which were made possible by requiring
that the L1 muon candidates have opposite
signs, segments in at least three different muon
√
stations, angular separation ∆Rµµ = (∆ηµµ )2 + (∆ϕµµ )2 that does not exceed a threshold
that varies between 1.2 and 1.4, and |η | < 1.5 in the trigger with no explicit pT requirement.
The other set takes advantage of a new track-finding procedure in the barrel section of the
L1 muon trigger. This procedure enables the reconstruction of L1 muon candidates and the
determination of their pT without using the beam spot constraint [15]. These triggers require
this pT be larger than 15 and 7 GeV for the leading and subleading L1 muon, respectively. The
pT thresholds are lowered to 6 and 4 GeV when d0 of both L1 muons is larger than 25 cm. The
new L1 triggers mitigate the efficiency loss that was present in Run 2 for displaced muons not
pointing to the beamspot [5], thereby improving the trigger efficiency for LLPs with cτ ≳ 10 cm.
The relative efficiency gain evaluated using the simulated HAHM signal events increases as cτ
increases, reaching a plateau at 20 to 50% (depending on m(Z D )) at cτ (Z D ) ≈ 10 m.
The events selected by the aforementioned L1 triggers were then required to be selected by
a logical OR of the 2018 L2 trigger paths used in the Run 2 analysis [5] and the newly designed HLT paths. The new paths use two complementary algorithms described below, and
are characterized by pT thresholds that depend on the muon d0 , as illustrated in Fig. 2. The
first algorithm, labeled Run 3 (2022, L2) in Fig. 2, imports some of the elements of the offline
analysis into the online selection, in order to take advantage of the superior tracker resolution
in determining muon d0 . Instead of stopping the online reconstruction at the L2 stage (muon
system alone) as it was done in the Run 2 trigger, the algorithm attempts to reconstruct the
muon candidates at the L3 stage as well (similar to offline TMS muons). If either of the two L2
muon candidates is reconstructed at L3 as a muon with d0 < 1 cm, the event is discarded, since
such an L2 muon candidate is likely to originate from the background processes. The resulting trigger operates with muon pT thresholds of 10 GeV and improves significantly the signal
efficiency in the STA-STA category, while contributing only about 1% additional HLT rate.
The second new HLT algorithm, labeled Run 3 (2022, L3) in Fig. 2, introduces new paths relying
entirely on the online L3 muon reconstruction. A moderate threshold on the impact parameter
of each muon, d0 > 0.01 cm, allows the pT thresholds to be fairly low: 16 GeV on the leading
muon µ 1 and 10 GeV on the subleading muon µ 2 . The resulting trigger greatly improves the
signal efficiency in the TMS-TMS category, while adding only another ≈1% of HLT rate. An
increase in the number of background events selected by the trigger led to the refinements in
the offline event selection described in Section 4.3.
The combined L1-HLT efficiency of the various displaced dimuon trigger paths and their com-

## PDF page 8

pT(𝜇1), pT(𝜇2) [GeV]

6

28, 28
23, 23

16, 10

Run 2 (2016)
Run 2 (2018)

Run 3 (2022, L3)

Run 3 (2022, L2)

10, 10

Axis not to scale

0.01

1

Tracker end

d0 [cm]

Figure 2: The pT and d0 coverage of the 2016 Run 2 triggers (light blue), 2018 Run 2 triggers
(blue), and newly designed 2022 Run 3 triggers described in the text (red). The two values of
the pT refer to the trigger thresholds for the muons.
bination as a function of cτ is shown in Fig. 3 for the simulated HAHM signal events with
m(Z D ) = 20 GeV. Because the Run 2 triggers (dashed black) have no restrictions on d0 , they
continue to have the highest efficiency (15%) at cτ < 0.02 cm. The addition of the Run 3 (2022,
L3) paths (blue) increases the overall efficiency (black) by more than a factor of 2 for cτ = 0.1–
1 cm. The efficiency of this trigger starts to drop at cτ ≳ 5 cm, when dimuons are produced
beyond the innermost tracker layers and the L3 muon reconstruction efficiency decreases. At
larger cτ values, the addition of the Run 3 (2022, L2) paths (red) strongly contributes to the
improvement of the signal efficiency, e.g., by more than a factor of 3 at cτ = 1 m. The decline
of the efficiencies at the largest cτ is driven by the increased fraction of dimuons produced
outside the CMS detector. Overall, the addition of new L1 and HLT paths improves the trigger
efficiency for Z D with m(Z D ) > 10 GeV and cτ ≳ 0.1 cm by a factor of 2 to 4, depending on cτ
and mass. The performance of the trigger was validated using data as described in Section 6.

4.3

Muon reconstruction and event selection

Optimal performance for the wide range of displacements of secondary vertices considered
in the analysis cannot be achieved by a single muon reconstruction algorithm. To accurately
reconstruct muons produced near the IP, commonly used algorithms developed for prompt
muons are employed. These algorithms combine measurements from both the tracker and the
muon system. Two such TMS algorithms are the global muon and tracker muon reconstruction
algorithms [13, 33]. The global muon algorithm reconstructs muons by fitting hits in the tracker
and segments in the muon system into a common track. The tracker muon algorithm, on the
other hand, builds muons by extrapolating tracks in the inner tracker to the muon system and
requiring loose geometric matching to DT or CSC segments. However, the efficiency of these
algorithms decreases rapidly as the distance between the IP and the muon origin increases. In
contrast, algorithms that rely solely on information from the muon system can still efficiently

## PDF page 9

7

Trigger efficiency

Muon reconstruction and event selection

1
0.9
0.8
0.7
0.6
0.5
0.4
0.3
0.2
0.1
0

Run 3 (2022)
Run 2 (2018)

4.3

5

(13.6 TeV)

CMS

Simulation

H → ZDZD

Run 2 (2018)

m(H) = 125 GeV
m(Z ) = 20 GeV

Run 3 (2022)
Run 3 (2022, L3)

D

Run 3 (2022, L2)

4
3
2
1
0

10−2

10−1

1

10

102

3

10

104

cτ [cm]

Figure 3: Efficiencies of the various displaced dimuon trigger paths and their combination as
a function of cτ for the HAHM signal events with m(Z D ) = 20 GeV. The efficiency is defined
as the fraction of simulated events that satisfy the detector acceptance and the requirements of
the following sets of trigger paths: the Run 2 (2018) triggers (dashed black); the Run 3 (2022,
L3) triggers (blue); the Run 3 (2022, L2) triggers (red); and the OR of all these triggers (Run 3
(2022), black). The lower panel shows the ratio of the overall Run 3 (2022) efficiency to the
Run 2 (2018) efficiency.
reconstruct muons produced in the outer tracker layers and beyond. These STA algorithms [13,
33] can reconstruct muons with displacements of up to a few meters. However, they exhibit
poorer spatial and momentum resolution compared to muons reconstructed using the more
precise information from the silicon tracker.
To benefit from the advantages offered by both types of algorithms, we begin the muon selection with the muons reconstructed by a specific STA algorithm that eliminates the beam spot
constraints from all stages of the muon reconstruction procedure. This approach yields the
highest efficiency and the finest resolution for highly displaced muons, surpassing all other
available STA algorithms. Subsequently, we attempt to match each STA muon with muons reconstructed using global muon and tracker muon algorithms, and replace the STA muon with
an associated TMS muon if a match is found. As in the Run 2 analysis [5], we reject events in
which no HLT muon pair that triggered the event matches two STA muons.
Due to the need to reduce large backgrounds as much as possible, careful optimization of the
event, muon, and dimuon selection was done for the Run 2 analysis, as described in Section 4
of Ref. [5]. A summary of the selection criteria used in the Run 2 analysis is given in Table 1
of Ref. [5]. Most of the selection criteria are unchanged, as is the association between STA and
TMS muons for those tracks originating within the tracker volume. The rest of this section of
the paper describes only the changes and refinements to the muon and dimuon selection for
this Run 3 search, while also introducing analysis variables that are used in the background
estimation.
Because of the increase in the background as a result of the lower pT trigger thresholds, an iso-

## PDF page 10

8
lation requirement is useful when applied to the STA muons. Both STA muons in the STA-STA
STA < 0.15, where I STA is defined as
category are required to have relative tracker isolation Irel,
rel, trk
trk
√
the sum of the pT of tracks within a cone of ∆R = (∆η )2 + (∆ϕ)2 < 0.3 around the trajectory
of the muon extrapolated to the point of closest approach to the PV divided by the muon track
pT . When evaluated using events that pass all other selection criteria, this isolation requirement
is more than 90% efficient for signal and suppresses background from events with jets that are
produced through the strong interaction, collectively referred to as quantum chromodynamTMS < 0.075,
ics (QCD) events, by about a factor of 2. The TMS muon isolation criterion, Irel,
trk
remained unchanged with respect to the Run 2 analysis [5].
The Run 2 analysis required that the dimuons be displaced with respect to the PV by imposing requirements on the Lxy significance Lxy /σLxy , where σLxy is the uncertainty in Lxy [5]. A
significant fraction of remaining events in the STA-STA category suffer from unreliable SV reconstruction; we thus require in addition that σLxy < 20 cm.
In the TMS-TMS category, the sensitivity of the search is further improved by binning events in
min(d0 /σd0 ), which is the minimum value of the ratio of d0 to its uncertainty for the two muons
forming a dimuon. Unlike signal events with macroscopic cτ values, the expected background
has a steeply falling min(d0 /σd0 ) distribution, which motivates the splitting of the signal region
(SR) into three bins of min(d0 /σd0 ) ranges. The bin ranges are the same as those in the Run 2
analysis, namely 6–10, 10–20, and >20.
A quantity that is useful for suppressing and evaluating the SM background that satisfies all
other selection requirements is the azimuthal angle ∆Φ between ⃗Lxy and the transverse momentum vector ⃗pT,µµ of the dimuon system. A major source of SM background events is from
prompt high-mass dimuons that are reconstructed as displaced due to instrumental or reconstruction failures. Such dimuons mostly arise from DY dimuon production. Events from DY
τ + τ − production with both τ leptons decaying to muons lead to a background with characteristics similar to those of the mismeasured DY µ + µ − events; contributions from processes
such as tt and diboson production are relatively small. Dimuons originating in these events,
collectively referred to as DY events, are expected to have a distribution of |∆Φ| symmetric
about π/2, because the dimuon momentum vector is uncorrelated with the ⃗Lxy vector. On the
other hand, when a pair of muons is produced in the decay of an LLP originating at the PV,
the resulting ⃗pT,µµ and ⃗Lxy are collinear, and the distribution of |∆Φ| peaks at zero. This can
be seen in Fig. 4, which compares the |∆Φ| distributions of TMS-TMS and STA-STA dimuons
in data samples obtained by inverting some of the selection criteria and enriched in DY events
with the |∆Φ| distributions for events passing the full selection except for the |∆Φ| requirement
in all HAHM and RPV SUSY signal samples combined. There is a small asymmetry in the |∆Φ|
distribution for DY events in the STA-STA category, which is caused by the event selection
criteria.
To address the different |∆Φ| distributions in the two types of signal models, we define different
critical values |∆Φ|C for requiring |∆Φ| < |∆Φ|C . To define the SR for the HAHM model, where
|∆Φ| strongly peaks at zero and the tail is driven by the resolution, we use |∆Φ|C = π/10 in the
STA-STA category and π/30 in the TMS-TMS category. The tighter requirement in the TMSTMS category takes advantage of the better tracker resolution. For the RPV SUSY model, where
the distribution is broader due to the undetected neutrino among the decay products, we use
a looser requirement of the Run 2 analysis, |∆Φ|C = π/4, in both dimuon categories. For the
chosen |∆Φ|C values, the signal efficiency is 90–99% in the HAHM and 60–99% in the RPV
SUSY models, depending on the Lorentz boost of the LLP; the corresponding DY background
rejection factors are, respectively, 15–20 and 4–6, depending on the dimuon category. We use the

## PDF page 11

4.3

9

Muon reconstruction and event selection

CMS
1

Data (DY control region)
0
0
~
q → q∼
χ,∼
χ → µµν
1
1
H → ZDZD, ZD → µµ

STA-STA

36.6 fb-1 (13.6 TeV)

Normalized to unity

Normalized to unity

36.6 fb-1 (13.6 TeV)

10−1

CMS
1

10−2

10−3

10−3
0.5

1

1.5

2

2.5

3

|∆Φ|

TMS-TMS

10−1

10−2

0

Data (DY control region)
0
0
~
q → q∼
χ,∼
χ → µµν
1
1
H → ZDZD, ZD → µµ

0

0.5

1

1.5

2

2.5

3

|∆Φ|

Figure 4: Distributions of |∆Φ| for (left) STA-STA and (right) TMS-TMS dimuons in data samples obtained by inverting some of the selection criteria and enriched in DY events (black circles) and for events passing all selection criteria except for a requirement on |∆Φ| in all HAHM
(blue triangles) and RPV SUSY (orange squares) generated signal samples combined. All distributions are normalized to unit area.
symmetric region, |∆Φ| > π − |∆Φ|C , as a control region (CR) for evaluating the contribution
from DY and other prompt backgrounds, and the validation regions (VR) with π/4 < |∆Φ| <
π/2 and π/2 < |∆Φ| < 3π/4 for validating background predictions, as discussed in Section 5.
In addition to defining |∆Φ| SR and CRs, we classify selected dimuons as opposite-sign (OS)
or same-sign (SS), based on the observed muon charges. The signal selection requires that
dimuons be OS, while SS dimuons constitute a CR used to evaluate backgrounds arising from
QCD events.
The last important source of SM backgrounds consists of QCD events in which there are dimuons produced in decays of J/ψ mesons and other low-mass SM resonances, or formed from
the products of the b hadron cascade decays (b → cµ 1 X followed by c → µ 2 X). These events
are suppressed by requiring that mµµ > 10 GeV. However, it was observed that low-pT muons
can appear as muons with higher pT , with straighter tracks, when reconstructed from a small
number of measurements. This gives rise to dimuons with an overestimated mµµ (above the
10 GeV threshold) and a mistakenly formed displaced vertex. These dimuons typically have
small |∆Φ| (either due to the collinearity of the ⃗pT,µµ and ⃗Lxy vectors or overestimated muon
pT ) and may exhibit large values of Lxy /σLxy and d0 /σd0 that resemble signal-like characteristics.
To suppress such events, which are particularly abundant in the STA-STA category due to its
low resolution, we reject STA-STA dimuons whose separation in η is small (|∆ηµµ | < 0.1) if
one of the muons is reconstructed in the barrel from fewer than 25 DT hits or if the sum of
the segments belonging to both muons in the dimuon is fewer than 6. These requirements are
identical to those used in the Run 2 analysis.
Finally, to test for the existence of an LLP with a given mass, dimuons satisfying the selection
criteria are required to have mµµ within a specified interval containing the probed LLP mass.
The width of each interval is chosen according to the mass resolution and the expected background. For the interpretation in the framework of the HAHM model, where the LLP decay
products do not contain any undetected particles, the full widths of the chosen mµµ intervals
are approximately equal to 6–8 times the mass resolution at this mass. This choice typically
yields intervals containing a large fraction (90–99%) of putative signal with the probed mass.
Since the mass resolution in the TMS-TMS category is far superior to that in the STA-STA category (1–3% compared to 10–25%, for LLP masses between 20 and 350 GeV), the minimum

## PDF page 12

10
width of mµµ intervals varies from 3 GeV in the TMS-TMS category to ≈20 GeV in the STA-STA
category.
In the RPV SUSY model, the presence of a neutrino in the χ̃ 01 → µ + µ − ν decay vertex leads to
a nonpeaking dimuon invariant mass distribution with an endpoint at m(χ̃ 01 ). To improve the
mass resolution and the signal-to-background discrimination in signals featuring an LLP decay
vertex formed by a dimuon plus neutral or unobserved particles, we use the quantity referred
to as the corrected SV mass, defined as
√
mcorr
=
m2µµ + p2µµ sin2 θ + pµµ sin θ,
(1)
µµ

where pµµ is the magnitude of the dimuon momentum vector ⃗pµµ , and θ is the angle between
⃗pµµ and the vector connecting the PV with the SV. The motivation behind this variable, which
was used at LEP and the SLC and recently by LHCb [34] and CMS [35], is to rely on the conservation of momentum and correct for the missing mass of the vertex due to unaccounted
particles. In the case where only the dimuon belongs to the LLP decay vertex (and before measurement error), θ = 0 and mcorr
µµ = mµµ . If, however, the decay vertex includes other particles,
then θ > 0, mcorr
>
m
,
and
the corrected mass is the minimum mass that the LLP, in this case
µµ
µµ
0
the χ̃ 1 , can have in order to be consistent with the measured direction of flight. The mcorr
µµ distri0
butions of simulated RPV SUSY events show a clear peak at m(χ̃ 1 ) in both dimuon categories.
corr
We profit from the improvement in mass resolution offered by mcorr
µµ and use mµµ intervals to
probe different m(χ̃ 01 ). As with mµµ intervals for the HAHM model, the width of the intervals
is chosen to contain a large fraction of the RPV SUSY signal (typically 80–90%). In the STA-STA
category, we additionally require mµµ > 15 GeV to avoid the leakage of background events
from small mµµ to large mcorr
µµ .
Figure 5 shows, as an example, the full event selection efficiency for the HAHM signal with
m(Z D ) = 20 GeV as a function of cτ, and illustrates relative improvements in the efficiencies
from the new trigger algorithms. A large increase in the overall efficiency, shown in the lower
panel, is apparent; most of the efficiency gain from the improvements in the trigger algorithms
and shown in Fig. 3 is retained after the full offline event selection. Similar efficiency increases
are seen at other probed Z D masses.

5

Background estimates and their systematic uncertainties

Background events that meet the event selection criteria cannot be reliably simulated since they
consist of misreconstructed prompt muons and muons in jets. Therefore, we rely on analyzing
events in the recorded data to estimate the expected background. To achieve this, we employ
CRs where one or more selection criteria are inverted, creating a region predominantly populated by a specific type of background while having an insignificant contribution from the
signal processes. The specific definitions of these CRs and the procedure for evaluating the
background differ across dimuon categories and are elaborated on in the rest of this section.
The background evaluation methods are nearly all identical to those employed in the Run 2
analysis [5]. The only exception is the evaluation of QCD backgrounds in the STA-STA category, which can now benefit from events rejected by the new STA muon isolation requirement.
In order to prevent potential bias in the event selection, the events that satisfy the full set of
selection criteria (i.e., those in the SR) were kept concealed (”blinded”) until the final stages of
the analysis.
One particular type of background events arises from cosmic ray muons crossing the detector
within the acceptance of the muon system. Such muons are often reconstructed as two back-to-

## PDF page 13

11

Estimation of Drell–Yan and other prompt backgrounds

Signal efficiency

5.1

(13.6 TeV)

102

CMS
10
1

Run 2 (2018)

Run 3 (2022)

H → ZDZD

STA-STA

STA-STA

m(H) = 125 GeV
m(Z ) = 20 GeV

TMS-TMS

TMS-TMS

Combined

Combined

Simulation

D

10− 1
10− 2

Combined (2022)
Combined (2018)

10− 3
5
4
3
2
1
0

10−2

10−1

1

10

102

3

10

104

cτ [cm]

Figure 5: Overall efficiencies in the STA-STA (green) and TMS-TMS (red) dimuon categories, as
well as their combination (black) as a function of cτ for the HAHM signal events with m(Z D ) =
20 GeV. The solid curves show efficiencies achieved with the 2022 Run 3 triggers, whereas
dashed curves show efficiencies for the subset of events selected by the triggers used in the
2018 Run 2 analysis. The efficiency is defined as the fraction of signal events that satisfy the
criteria of the indicated trigger as well as the full set of offline selection criteria. The lower panel
shows the relative improvement of the overall signal efficiency brought in by improvements in
the trigger.
back muons, one in the upper half and one in the lower half of the detector. For each dimuon
category, the contribution from cosmic ray muons is assessed independently by examining
the number of dimuons that meet all the selection criteria except for angular requirements
designed to reject putative dimuons that are formed from back-to-back muons [5]. To evaluate
this contribution, we use the rejection factors of these requirements, which are determined from
a sample of cosmic ray muons recorded during periods without any beam activity. In both
dimuon categories, the remaining background originating from cosmic ray muons is estimated
to be less than 0.1 events in all mass intervals combined.

5.1

Estimation of Drell–Yan and other prompt backgrounds

The contribution from misreconstructed prompt high-mass dimuons, mainly originating from
the DY process, to the total background is evaluated from events in the signal-free |∆Φ|symmetric CR as
i
i
i
NDY
(OS; |∆Φ| < |∆Φ|C ) = NDY
(OS; |∆Φ| > π − |∆Φ|C ) RDY
,

(2)

i (OS; | ∆Φ | < | ∆Φ | ) and N i (OS; | ∆Φ | > π − | ∆Φ | ) are, respectively, the numbers
where NDY
C
C
DY
of DY background events in the SR and its |∆Φ|-symmetric CR with |∆Φ|C representing the sei
lection criterion applied; RDY
is the transfer factor accounting for the residual asymmetry in the
population of events in the two |∆Φ| regions and obtained from auxiliary measurements; and
the index i denotes the dimuon category (STA-STA or TMS-TMS). The number of DY dimuons
in the CR is obtained from the total number of events in that region corrected by the expected
contribution from QCD background events, estimated as discussed in Section 5.2.

## PDF page 14

12
To assess the symmetry of the |∆Φ| distributions in this class of background events, events in
dedicated CRs are used. In the STA-STA category, we focus on events within data CRs that are
obtained by reversing the STA-to-TMS association. Specifically, we select events where STASTA dimuons satisfy all the selection criteria, except that each of the constituent STA muons is
associated with a TMS muon. To ensure that these STA-STA dimuons are promptly produced
(and not part of the signal), we require that the associated TMS-TMS dimuons, which offer
superior spatial resolution, are prompt. This is achieved by imposing Lxy /σLxy < 1.0 for the
associated TMS-TMS dimuon. To minimize contamination from muons originating from jets
(which are discussed separately below), each TMS muon in the associated TMS-TMS dimuon
TMS < 0.05. From this sample, we obtain RSTA-STA = 0.75 ± 0.02 (stat.) for
is required to have Irel,
DY
trk
|∆Φ|C = π/10 and RSTA-STA
=
0.73
±
0.02
(stat.)
for
|
∆Φ
|
=
π/4.
The value of RTMS-TMS
is set
C
DY
DY
to unity based on studies using simulation and data [5].
i
In both STA-STA and TMS-TMS categories, no significant dependence of the transfer factor RDY
on reconstructed dimuon mass is observed, and a single value is used for all signal mass intervals. The systematic uncertainties in RSTA-STA
are assessed by comparing RSTA-STA
measured
DY
DY
in individual mass intervals with the result of the inclusive measurement and by varying the
boundaries and definitions of the auxiliary CRs. The latter includes repeating the measurements of RSTA-STA
in the region with only one STA-to-TMS association. Based on these studies,
DY
we assign a systematic uncertainty of 30% in RSTA-STA
. The systematic uncertainty in RTMS-TMS
DY
DY
is assigned to be 15% based on the studies of the residual |∆Φ| asymmetry for events in the
min(d0 /σd0 ) and |∆Φ| side bins.

5.2

Estimation of QCD backgrounds

Many of the background processes yielding small-|∆Φ| OS dimuons also give rise to small|∆Φ| SS dimuons, either because these processes are charge symmetric or via muon charge
misassignment. Most of these dimuons are embedded in jets and are suppressed by the muon
isolation requirements. Thus, we evaluate the contribution from the QCD backgrounds to the
SR from events in CRs obtained by inverting two independent selection requirements: the
isolation requirement (i.e., we select events where at least one of the muons fails to satisfy the
isolation criteria used in the analysis) and the requirement of the OS dimuons (i.e., we select SS
dimuons).
In the STA-STA category, we base our estimate of the QCD backgrounds on the number of
events with OS nonisolated dimuons, using
STA-STA
STA-STA
NQCD
(OS; |∆Φ| < |∆Φ|C ) = Nnoniso
(OS; |∆Φ| < |∆Φ|C ) RSTA-STA
,
QCD

(3)

STA-STA (OS; | ∆Φ | < | ∆Φ | ) and N STA-STA (OS; | ∆Φ | < | ∆Φ | ) are, respectively, the
where NQCD
C
C
noniso
numbers of OS isolated and nonisolated dimuons with small |∆Φ|, and RSTA-STA
is the transfer
QCD
factor between these numbers. The transfer factor is evaluated using SS dimuons in the same
small-|∆Φ| region:
STA-STA (SS; | ∆Φ | < | ∆Φ | )
Niso
C
RSTA-STA
=
,
(4)
QCD
STA-STA (SS; | ∆Φ | < | ∆Φ | )
Nnoniso
C
STA-STA (SS; | ∆Φ | < | ∆Φ | ) and N STA-STA (SS; | ∆Φ | < | ∆Φ | ) representing the numbers
with Niso
C
C
noniso
of, respectively, isolated and nonisolated SS STA-STA dimuons with |∆Φ| < |∆Φ|C . To improve
the precision of the RSTA-STA
measurement, we enlarge the sample of SS dimuons by removing
QCD
tight requirements on the numbers of DT hits and muon segments applied to dimuons with
|∆ηµµ | < 0.1 (discussed in Section 4) as well as the generic requirement on the minimum number of DT hits [5]. We obtain RSTA-STA
values varying between 1.0 and 1.5 as a function of
QCD

## PDF page 15

5.3

Validation of background predictions

13

reconstructed dimuon mass and measured with an uncertainty of 20–40%. They are in good
agreement with RSTA-STA
values obtained from a sample of OS small-|∆Φ| events failing the
QCD
criteria for dimuons with |∆ηµµ | < 0.1. Systematic uncertainties arising from these two measurements are found to be much smaller than statistical uncertainties resulting from CR sample
sizes.
Based on the Run 2 studies [5], we do not anticipate a significant contribution from |∆Φ|asymmetric low-mass dimuons in the TMS-TMS category. This is primarily due to the superior
dimuon invariant mass resolution in this category. However, since there may still be a small
contribution from |∆Φ|-asymmetric dimuons, we prefer not to rely solely on the symmetry of
|∆Φ| in evaluating the background. Consequently, the method used is similar to that employed
in the STA-STA category and bases our estimate of the QCD backgrounds on the number of SS
dimuons, using
TMS-TMS
NQCD
(OS; |∆Φ| < |∆Φ|C ) = N TMS-TMS (SS; |∆Φ| < |∆Φ|C ) RTMS-TMS
.
QCD

(5)

The transfer factor RTMS-TMS
is obtained from the ratio of OS to SS dimuons in the CR with the
QCD
muon isolation requirement reversed, which consists of dimuons passing the nominal event
TMS > 0.075 and both with I TMS < 0.5. We have
selection but with at least one muon with Irel,
trk
rel, trk
verified that these events, as well as SS dimuons passing isolation requirements, contain negligible contributions from signal and DY events. As the SR is divided into several min(d0 /σd0 )
bins, the evaluation of RTMS-TMS
is performed separately in each min(d0 /σd0 ) bin. Since no sigQCD
TMS-TMS in each
nificant dependence of the value of RTMS-TMS
on mµµ and mcorr
µµ is observed, RQCD
QCD
min(d0 /σd0 ) bin is calculated by integrating events in the entire invariant mass spectrum. The
measured values of RTMS-TMS
decrease from 2.0 to 1.3 as min(d0 /σd0 ) increases, with the statisQCD
tical uncertainties in the range 5–15%. A systematic uncertainty of 15% is assigned to account
for variations of RTMS-TMS
as a function of the invariant mass and as the result of varying the
QCD
definition and boundaries of the auxiliary CR.
To avoid potential overestimation of the DY backgrounds, we use the same QCD background
evaluation technique for dimuons in the CR defined by |∆Φ| > π − |∆Φ|C . The obtained
estimate of the QCD backgrounds is subtracted from the total to derive the estimate of DY
dimuons in this |∆Φ| region, which is used for the evaluation of the DY backgrounds in the
SR according to Eq. (2). This procedure is not applied in the STA-STA category, where the
|∆Φ|-symmetric QCD background is negligible. The sum of the QCD and DY background
estimates constitutes the total predicted background in the SR. According to the background
evaluation method, the DY backgrounds are expected to dominate at small d0 /σd0 and Lxy /σLxy
values, whereas the relative QCD contribution becomes larger as d0 /σd0 and Lxy /σLxy increase.
The uncertainty in the background predictions is mainly driven by the statistical uncertainty
arising from the limited number of events observed in the CRs.

5.3

Validation of background predictions

To ensure the reliability of the background evaluation method described in Sections 5.1 and 5.2,
we examine the method’s performance in various VRs, which are chosen to have minimal or
no contribution from the signal being studied. Thus, we can verify that it accurately predicts
the background and that any observed discrepancies are within acceptable limits.
The evaluation of DY backgrounds is examined in the VRs obtained by inverting the Lxy /σLxy
and d0 /σd0 requirements and thereby enriched in this class of events. An example is shown
in Fig. 6, which compares the background predictions to the observed distributions in the

## PDF page 16

14

STA-STA

12

OS, Lxy/ σLxy < 6

10

mµ µ > 15 GeV

Events / 1 unit

CMS

14

36.6 fb-1 (13.6 TeV)

8

14

6
4

2

2

0

|∆Φ|

0.2

0.4

0.6

0.8

1

1.2

1.4

STA-STA

8

4

4
3
2
1
0

Observed
Drell-Yan
Stat. uncertainty

OS, |∆Φ| < π/4
mµ µ > 15 GeV

10

6

0

CMS

12

0

Obs. / pred.

Obs. / pred.

Events / 0.314 units

36.6 fb-1 (13.6 TeV)
Observed
Drell-Yan
Stat. uncertainty

Lxy/ σLxy

4
3
2
1
0

0

|∆Φ|

1

2

3

4

5

6

Lxy/ σLxy

36.6 fb-1 (13.6 TeV)

105
104

CMS

TMS-TMS
2 < min(d / σd ) < 6
0

0

|∆Φ| < π/4

103

Events / 2 units

Events / 2 units

Figure 6: Example of background prediction checks in the STA-STA category: distributions of
(left) |∆Φ| and (right) Lxy /σLxy for events with mµµ > 15 GeV in the Lxy /σLxy < 6 validation
region in data (black circles) compared to the background predictions (histograms). The lower
panels show the ratio of the observed to predicted number of events. Hatched histograms show
the statistical uncertainty in the background prediction.
Observed
Drell-Yan
QCD
Stat. uncertainty

102

104

TMS-TMS
2 < min(d / σd ) < 6
0

0

|∆Φ| < π/30

103
102

1

1

−1

−1

10

2
1.5
1
0.5
0
0

CMS

Observed
Drell-Yan
QCD
Stat. uncertainty

10

5

10

15

20

25

30

Lxy/ σLxy

Obs. / pred.

Obs. / pred.

10

36.6 fb-1 (13.6 TeV)

105

10

2
1.5
1
0.5
0
0

5

10

15

20

25

30

Lxy/ σLxy

Figure 7: Example of background prediction checks in the TMS-TMS category: Lxy /σLxy distributions for events with (left) |∆Φ| < π/4 and (right) |∆Φ| < π/30 in the 2 < min(d0 /σd0 ) < 6
validation regions compared to the background predictions. The number of observed events
(black circles) is overlaid with stacked histograms showing the expected numbers of QCD (yellow) and DY (green) background events. The last bin includes events in the histogram overflow. The lower panels show the ratio of the observed to predicted number of events. Hatched
histograms show the statistical uncertainty in the background prediction.
Lxy /σLxy < 6 VR for dimuons with mµµ > 15 GeV in the STA-STA category. To check how
the validity of the method depends on |∆Φ| and the dimuon displacement, we perform the
evaluation of the background in corresponding bins. The expected number of background
events in the given VR is computed according to Eq. (2) separately in each |∆Φ| or Lxy /σLxy
bin and compared to the observed data. The predictions of the method are consistent with the
yields in data.
In the TMS-TMS category, we apply the background evaluation procedure to the TMS-TMS
dimuons in the VR defined by 2 < min(d0 /σd0 ) < 6. The comparison of the predicted background and data in bins of Lxy /σLxy for two |∆Φ|C requirements is shown in Fig. 7. The expected and observed numbers of events are in agreement in the entire probed Lxy /σLxy range.

## PDF page 17

15

CMS

STA-STA
OS
6 < mµ µ < 10 GeV

102

36.6 fb-1 (13.6 TeV)

Events / 1 GeV

Events / 0.157 units

36.6 fb-1 (13.6 TeV)
103

Observed
QCD
Stat. uncertainty

10

CMS

Observed
QCD
Stat. uncertainty

STA-STA

80

OS
|∆Φ| < π/4

60
40
20

3

|∆Φ|

2
1
0

0

0.1

0.2

0.3

0.4

0.5

0.6

0.7

|∆Φ|

Obs. / pred.

1

Obs. / pred.

100

0
3

mµµ [GeV]

2
1
0

6

6.5

7

7.5

8

8.5

9

9.5

10

mµµ [GeV]

Figure 8: Example of background prediction checks in the STA-STA category: distributions of
(left) |∆Φ| and (right) mµµ for dimuons in the low-mass (6 < mµµ < 10 GeV) validation region
in data (black circles) compared to the background predictions (histograms). The lower panels
show the ratio of the observed to predicted number of events. Hatched histograms show the
statistical uncertainty in the background prediction.
The evaluation of the |∆Φ|-asymmetric component of the background, which is particularly
important in the STA-STA category, is tested in the low-mass (6 < mµµ < 10 GeV) VR where
the QCD backgrounds dominate. Figure 8 shows a comparison of predicted and measured
background in this VR as a function of |∆Φ| and mµµ for STA-STA dimuons. The yields in data
are found to be consistent with the background predictions in all |∆Φ| and mµµ intervals.
Finally, to ensure the validity of the method at different values of the main discriminating
variables in the TMS-TMS category, the validation checks are performed in bins of min(d0 /σd0 )
and mµµ of TMS-TMS dimuons. Such checks include comparisons in the d0 /σd0 sideband (2 <
d0 /σd0 < 6) in the |∆Φ| < π/4 SR, as well as those in the entire d0 /σd0 range in the |∆Φ|
sideband, π/4 < |∆Φ| < π/2. In the latter, the region with π/4 < |∆Φ| < π/2 is used as
a signal-free proxy for the |∆Φ| < π/4 SR. The background evaluation procedure is applied
to the OS and SS dimuons in the |∆Φ|-symmetric region, π/2 < |∆Φ| < 3π/4, as well as SS
dimuons with π/4 < |∆Φ| < π/2. The comparisons of the predicted background and data
as a function of min(d0 /σd0 ) and mµµ for TMS-TMS dimuons in these VRs are shown in Fig. 9.
The observed and expected numbers of events are consistent within statistical uncertainties.

6

Systematic uncertainties affecting signal

The modeling of signal efficiencies in simulation was extensively studied in the Run 2 search [5].
Since no changes affecting this analysis were made in the CMS detector or in the muon reconstruction algorithms between Run 2 and Run 3, many of the systematic uncertainties and datato-simulation corrections are taken directly from Ref. [5]. New studies include modeling of signal efficiencies related to the new trigger algorithms and modified event selection criteria, such
as the STA muon isolation. The studies are performed for each dimuon category separately,
using dedicated data samples. Unless stated otherwise, we consider sources of uncertainties to
be uncorrelated between different categories.
In both categories, the dominant systematic uncertainties and the largest data-to-simulation
corrections arise from muon identification, muon reconstruction, and trigger efficiencies. At
small displacements, the systematic effects related to these efficiencies are examined as a function of muon pT and η by applying the “tag-and-probe” method [33] to prompt muons from J/ψ

## PDF page 18

36.6 fb-1 (13.6 TeV)

105
104

CMS

Events / 20 GeV

Events / 2 units

16

Observed
Drell-Yan
QCD
Stat. uncertainty

TMS-TMS
π/4 < |∆Φ| < π/2

103
102

36.6 fb-1 (13.6 TeV)

104

CMS

Observed
Drell-Yan
QCD
Stat. uncertainty

TMS-TMS
2 < min(d / σd ) < 6

103

0

0

2

10

10

1

1

10−1
2
1.5
1
0.5
0
0

10−1
2
1.5
1
0.5
0

5

10

15

20

25

30

min(d / σd )
0

0

Obs. / pred.

Obs. / pred.

10

20

40

60

80

100

120

140

160

180

200

mµµ [GeV]

Figure 9: Example of background prediction checks in the TMS-TMS category: (left) distribution of min(d0 /σd0 ) for events in the π/4 < |∆Φ| < π/2 validation region; (right) distribution
of mµµ for events in the 2 < min(d0 /σd0 ) < 6 validation region. The number of observed
events (black circles) is overlaid with stacked histograms showing the expected numbers of
QCD (yellow) and DY (green) background events. The last bin includes events in the histogram overflow. The lower panels show the ratios of the observed to predicted number of
events. Hatched histograms show the statistical uncertainty in the background prediction.
meson and Z boson decays. The evolution of efficiencies as a function of displacement is studied using cosmic ray muons and muons from decays of nonprompt J/ψ mesons. These studies
yield corrections to the simulated signal yields that range, depending on the signal sample,
from 0.75 to unity for the STA-STA category and from 0.83 to unity for the TMS-TMS category.
The overall uncertainty increases continuously with displacement, from ≈5% for prompt-like
muons to ≈15% for muons with d0 = 100 cm, reflecting the precision of studies using cosmic
ray muons. Since a large part of this uncertainty stems from the evaluation of efficiencies of
trigger algorithms common to both dimuon categories, it is taken as correlated between the
categories.
Dedicated studies were performed to examine the effect of the d0 thresholds and looser muon
pT requirements of the new displaced dimuon triggers. The efficiency of the Run 3 (2022, L3)
triggers is evaluated using dimuons from decays of nonprompt J/ψ mesons selected by the
triggers that use jets and event pT imbalance. As a result of these studies, the simulated yields
of signal events selected by this set of triggers are scaled by a factor of 0.95, and an uncertainty
of 5% is assigned. The efficiency of the Run 3 (2022, L2) triggers is studied using cosmic ray
muons. While no systematic biases are observed, the largest data-simulation difference of 3%
in bins of d0 is assigned as a systematic uncertainty in the efficiency of these triggers. These
corrections and uncertainties are included in the overall corrections and uncertainties discussed
in the previous paragraph.
The accuracy of the modeling of the muon isolation requirements is assessed using muons
from Z boson decays and, in the case of STA muons, cosmic ray muons selected in pp collision
events. Based on the results of these studies, a systematic uncertainty of 6 (2)% is assigned to the
efficiency of STA (TMS) muons. The uncertainty in the Higgs boson production cross section
5%
at 13.6 TeV amounts to +
−7% [21]. The remaining systematic uncertainties, e.g., those related to
muon pT resolution and dimuon vertex reconstruction, are less than 5%. The uncertainty in
the integrated luminosity is 2.3% [36]. The uncertainty in the signal efficiency due to pileup
modeling is 2%. Both luminosity and pileup uncertainties are correlated among the dimuon
categories.

## PDF page 19

17

40

CMS

Observed
H → ZDZD (20 GeV, ε = 1 × 10− 8 ) × 3

H → ZDZD (50 GeV, ε = 4 × 10− 9 ) × 8

STA-STA
|∆Φ| < π/10

Drell-Yan
QCD

30

36.6 fb-1 (13.6 TeV)

Events / bin

Events / bin

36.6 fb-1 (13.6 TeV)

50

50
40

10

10

40

60

80

100

|∆Φ| < π/4

120

140

mµµ [GeV]

Observed
0
~ (125 GeV) → q∼
q
χ (50 GeV, cτ = 200 cm) × 3
1

0
~
q (350 GeV) → q∼
χ (150 GeV, cτ = 250 cm) × 4
1

Drell-Yan
QCD

20

20

STA-STA

30

Stat. uncertainty

20

0

CMS

0

Stat. uncertainty

100

200

300

400

500

mcorr
µµ [GeV]

Figure 10: Comparison of the observed (black points) and expected (histograms) numbers of
events in nonoverlapping (left) mµµ and (right) mcorr
µµ intervals in the STA-STA dimuon category,
in the signal regions optimized for the (left) HAHM and (right) RPV SUSY model. Yellow and
green stacked filled histograms represent mean expected background contributions from QCD
and DY, respectively, while statistical uncertainties in the total expected background are shown
as hatched histograms. Signal contributions expected from simulated signals indicated in the
legends are shown in red and blue. Their yields are set to the corresponding median expected
95% CL exclusion limits obtained from the ensemble of both dimuon categories, scaled up as
indicated in the legend to improve visibility. The last bin includes events in the histogram
overflow.

7

Results

The numbers of observed events and the predicted background yields in the STA-STA category
are shown in Fig. 10 in representative mµµ and mcorr
µµ intervals. The width of the mass intervals
and the |∆Φ| and mµµ requirements for events in Fig. 10 (left) and Fig. 10 (right) correspond
to those chosen, respectively, for the study of the HAHM and of the RPV SUSY model. For
illustrative purposes, signal distributions at the level of the median expected exclusion limits
at 95% confidence level (CL) obtained from the ensemble of both dimuon categories in the
background-only scenario are also shown. The numbers of observed events are consistent with
background predictions. As expected for background events, most of the observed events have
low mµµ .
The numbers of observed events and the predicted background yields in the TMS-TMS category are shown in Figs. 11–13. Figure 11 shows the distributions of min(d0 /σd0 ) for TMS-TMS
dimuons with (left) |∆Φ| < π/30 and (right) |∆Φ| < π/4, for events in all mass intervals
combined. As expected for background events, the events in data are predominantly at low
values of min(d0 /σd0 ). Figure 12 shows the distributions of mcorr
µµ in three min(d0 /σd0 ) bins,
6–10, 10–20, and >20, for dimuons with |∆Φ| < π/4, the looser |∆Φ| requirement used for the
study of the RPV SUSY model. The numbers of events in the SR chosen for the study of the
HAHM model, with the tighter requirement |∆Φ| < π/30, are smaller (with no more than one
event per mµµ bin), as shown in Fig. 13. The numbers of observed events are consistent with
background predictions in both SRs. The largest min(d0 /σd0 ) bin, min(d0 /σd0 ) > 20, contains
the lowest experimental background and, except for the smallest lifetimes, most of the signal
predicted by both models.
These results are used to set upper limits on B(H → Z D Z D ) in the HAHM model and on the
product of the squark-antisquark production cross section σ(pp → q̃ q̃ ) and B(q̃ → q χ̃ 01 ) in the
RPV SUSY model. The limit extraction is based on a modified frequentist approach [37, 38] and

## PDF page 20

18

Events / bin

CMS
104

Observed
H → ZDZD (20 GeV, ε = 5 × 10− 7 ) × 7

TMS-TMS

H → ZDZD (50 GeV, ε = 7 × 10− 7 ) × 5

|∆Φ| < π/30

103

Events / bin

36.6 fb-1 (13.6 TeV)

105

Drell-Yan

36.6 fb-1 (13.6 TeV)

105

CMS
104
103

Observed
0
~ (125 GeV) → q∼
q
χ (50 GeV, cτ = 2.2 mm) × 4

TMS-TMS

1

0
~
q (350 GeV) → q∼
χ (150 GeV, cτ = 0.4 mm) × 3

|∆Φ| < π/4

1

Drell-Yan

QCD

QCD

Stat. uncertainty

2

10

10

10

10

1

1

10−1
0

5

10

15

20

Stat. uncertainty

2

25

30

35

10−1
0

40

min(d / σd )
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

0

Figure 11: Distributions of min(d0 /σd0 ) for TMS-TMS dimuons with (left) |∆Φ| < π/30
and (right) |∆Φ| < π/4, for events in all mass intervals combined, for both the validation
(min(d0 /σd0 ) < 6) and signal (min(d0 /σd0 ) > 6) regions. The number of observed events (black
circles) is overlaid with the stacked histograms showing the expected numbers of QCD (yellow)
and DY (green) background events. Statistical uncertainties in the total expected background
are shown as hatched histograms. Signal contributions expected from simulated signals indicated in the legends are shown in red and blue. Their yields are set to the corresponding
median expected 95% CL exclusion limits obtained from the ensemble of both dimuon categories, scaled up as indicated in the legend to improve visibility. Events are required to satisfy
all nominal selection criteria with the exception of the d0 /σd0 requirement. The last bin includes
events in the histogram overflow.

Events / bin

45
40
35

45

CMS

Observed

TMS-TMS
|∆Φ| < π/4

30

40
35

6 < min(d / σd ) < 10
0

0

45

~
q (125 GeV) → qχ1 (50 GeV, cτ = 2.2 mm) × 4
40
0
~
q (350 GeV) → q∼
χ (150 GeV, cτ = 0.4 mm) × 3

Drell-Yan
QCD
Stat. uncertainty

35

10 < min(d / σd ) < 20

30

0

0

25

25

20

20

20

15

15

15

10

10

10

5

5

5

0

0
103

102

2×102

20 30

102

2×102

1

min(d / σd ) > 20

30

25

20 30

36.6 fb-1 (13.6 TeV)
∼0

0
103

0

20 30

102

0

2×102

103

mcorr
µµ [GeV]

Figure 12: Comparison of observed and expected numbers of events in bins of mcorr
µµ in the TMSTMS dimuon category, in the signal regions optimized for the RPV SUSY model. The number
of observed events (black circles) is overlaid with the stacked filled histograms showing the
expected numbers of QCD (yellow) and DY (green) background events in bins of mcorr
µµ in three
min(d0 /σd0 ) bins: (left) 6–10, (center) 10–20, and (right) >20. Hatched histograms show statistical uncertainties in the total expected background. Contributions expected from signal events
predicted by the RPV SUSY model with the parameters indicated in the legends are shown as
red and blue histograms. Their yields are set to the corresponding median expected 95% CL
exclusion limits obtained from the ensemble of both dimuon categories, scaled up as indicated
in the legend to improve visibility. The last bin includes events in the histogram overflow.

## PDF page 21

19

Events / bin

25

25

CMS

20

|∆Φ| < π/30

20
6 < min(d / σd ) < 10
0

H → ZDZD (20 GeV, ε = 5 × 10− 7 ) × 7

Drell-Yan
QCD
Stat. uncertainty

Observed

TMS-TMS

−7
H → ZDZ20
)×5
D (50 GeV, ε = 7 × 10

10 < min(d / σd ) < 20
0

0

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

0
20

30 40

102

36.6 fb-1 (13.6 TeV)

25

2×102

0
20

30 40

102

2×102

0
20

30 40

0

102

2×102

mµµ [GeV]

Figure 13: Comparison of observed and expected numbers of events in bins of mµµ in the TMSTMS dimuon category, in the signal regions optimized for the HAHM. The number of observed
events (black circles) is overlaid with the stacked histograms showing the expected numbers
of QCD (yellow) and DY (green) background events in bins of mµµ in three min(d0 /σd0 ) bins:
(left) 6–10, (center) 10–20, and (right) >20. Hatched histograms show statistical uncertainties
in the total expected background. Signal contributions expected from simulated H → Z D Z D
events with the parameters indicated in the legends are shown as red and blue histograms.
Their yields are set to the corresponding median expected 95% CL exclusion limits obtained
from the ensemble of both dimuon categories, scaled up as indicated in the legend to improve
visibility. The last bin includes events in the histogram overflow.
uses the CMS statistical analysis tool C OMBINE [39]. The method yielding background predictions in the SR is implemented using a multibin likelihood, which is a product of Poisson distributions corresponding to the SR and CRs. The systematic uncertainties affecting the signal
yield are incorporated as nuisance parameters using log-normal distributions. The expected
and observed upper limits are evaluated through the use of simulated pseudo-experiments.
For each signal model, the limits are first computed separately in each dimuon category. The
individual likelihoods are then combined to obtain the limits in the ensemble of both categories.
For the interpretation in the framework of the HAHM model, the results obtained in this analysis are also combined with the results of the Run 2 analysis [5] to achieve even stronger bounds
on the model parameters. The combination of the two results takes into account the different
cross sections of the Higgs boson production in collisions at 13.0 and 13.6 TeV [20, 21].
The signal efficiencies used in the statistical interpretations of the results are obtained from
simulation and further corrected by the data-to-simulation scale factors described in Section 6.
They are computed separately for each dimuon category, mass interval, LLP lifetime, and signal model. Given the smallness of the expected background and taking into account the selection efficiencies discussed in Section 4, the introduction of a separate category for events
with two dimuons would not increase the sensitivity of the analysis significantly even in the
most favorable case for the 4µ signal events, namely B(LLP → µ + µ − X ) = 1. The gain would
be negligible for smaller B(Z D → µ + µ − ) values predicted by the HAHM model. Therefore,
no distinction is made between events with one and two reconstructed dimuons of the same
type. Events with two TMS-TMS dimuons are assigned to the min(d0 /σd0 ) bin encompassing
the larger of the two min(d0 /σd0 ) values.
Figures 14 and 15 show the 95% CL upper limits obtained in the framework of the HAHM
model under the assumption that m(H D ) > m(H )/2. The limits shown in these figures are set
on B(H → Z D Z D ) as functions of the mean proper decay length of Z D for m(Z D ) in the range
10–60 GeV. Figure 14 shows the results obtained in this analysis, namely the expected limits in

## PDF page 22

20

36.6 fb-1 (13.6 TeV)

CMS

10−1

m(Z ) = 10 GeV
D

10−2

Β (Z → µµ) = 0.144

Observed
Expected

68% quantile
95% quantile

1

10

102

10−5

TMS-TMS
STA-STA

103

104

105

36.6 fb-1 (13.6 TeV)

1

CMS
m(Z ) = 30 GeV
D

Β (Z → µµ) = 0.140

10−3

Observed
Expected

10−3 10−2 10−1

68% quantile
95% quantile

103

104

105

106

cτ [cm]

36.6 fb-1 (13.6 TeV)

H → ZDZD
m(Z ) = 40 GeV
D

−2

Β (Z → µµ) = 0.134
D

1

10

102

10−5

TMS-TMS
STA-STA

103

104

105

36.6 fb-1 (13.6 TeV)

1

CMS
m(Z ) = 50 GeV
D

Β (Z → µµ) = 0.122

10−3

1

10

102

TMS-TMS
STA-STA

103

104

105

106

cτ [cm]

36.6 fb-1 (13.6 TeV)

CMS
H → ZDZD
m(Z ) = 60 GeV
D

10−2

D

68% quantile
95% quantile

1

10−1

H → ZDZD

Observed
Expected

10−3 10−2 10−1

106

cτ [cm]

95% CL upper limit on Β(H→ZDZD)

95% CL upper limit on Β(H→ZDZD)

102

10−4

10−5

Β (Z → µµ) = 0.103
D

10−3

10−4
10−5

10

10−3

10−4

10−2

1

TMS-TMS
STA-STA

CMS

10

D

68% quantile
95% quantile

1

10−1

H → ZDZD

Observed
Expected

10−3 10−2 10−1

106

cτ [cm]

95% CL upper limit on Β(H→ZDZD)

95% CL upper limit on Β(H→ZDZD)

10−3 10−2 10−1

10−1

D

10−4

10−5

10

D

Β (Z → µµ) = 0.143

10−3

10−4

−2

H → ZDZD
m(Z ) = 20 GeV

10−2

D

10−3

10−1

CMS

10−1

H → ZDZD

36.6 fb-1 (13.6 TeV)

1

95% CL upper limit on Β(H→ZDZD)

95% CL upper limit on Β(H→ZDZD)

1

10−4

Observed
Expected

10−3 10−2 10−1

68% quantile
95% quantile

1

10

102

10−5

TMS-TMS
STA-STA

103

104

105

106

cτ [cm]

Observed
Expected

10−3 10−2 10−1

68% quantile
95% quantile

1

10

102

TMS-TMS
STA-STA

103

104

105

106

cτ [cm]

Figure 14: The 95% CL upper limits on B(H → Z D Z D ) as a function of cτ (Z D ) in the HAHM
model, for m(Z D ) ranging from (upper left) 10 GeV to (lower right) 60 GeV, in the STA-STA
and TMS-TMS dimuon categories in 2022 data and their combination. The median expected
limits obtained from the STA-STA and TMS-TMS dimuon categories are shown as dashed blue
and red curves, respectively; the combined median expected limits are shown as dashed black
curves; and the combined observed limits are shown as solid black curves. The green and
yellow bands correspond, respectively, to the 68 and 95% quantiles for the combined expected
limits.

## PDF page 23

1

10−1

95% CL upper limit on Β(H→ZDZD)

95% CL upper limit on Β(H→ZDZD)

21

CMS

10−1

H → ZDZD
m(Z ) = 10 GeV

10−2

D

D

Combined:
Observed
Expected

10

102

103

104

105

106

cτ [cm]

CMS
D

D

10−3

Combined:
Observed
Expected

1

10

10−5

Observed:
13 TeV (97.6 fb-1 )
13.6 TeV (36.6 fb-1 )

68% quantile
95% quantile

102

103

104

105

106

102

103

104

105

106

cτ [cm]

CMS
H → ZDZD
D

Β (Z → µµ) = 0.134
D

cτ [cm]

1

CMS
m(Z ) = 50 GeV
D

10−2

Β (Z → µµ) = 0.122
D

10−3

68% quantile
95% quantile

1

10

Observed:
13 TeV (97.6 fb-1 )
13.6 TeV (36.6 fb-1 )

102

103

104

105

106

cτ [cm]

1

10−1

H → ZDZD

Combined:
Observed
Expected

10−6
10−3 10−2 10−1

95% CL upper limit on Β(H→ZDZD)

95% CL upper limit on Β(H→ZDZD)

10

10−4

10−6
10−3 10−2 10−1

CMS
H → ZDZD
m(Z ) = 60 GeV
D

Β (Z → µµ) = 0.103
D

10−3

10−4
10−5

1

Observed:
13 TeV (97.6 fb-1 )
13.6 TeV (36.6 fb-1 )

10−3

10−4

10−2

68% quantile
95% quantile

m(Z ) = 40 GeV

10−2

Β (Z → µµ) = 0.140

Combined:
Observed
Expected

1

10−1

H → ZDZD
m(Z ) = 30 GeV

10−1

D

10−6
10−3 10−2 10−1

95% CL upper limit on Β(H→ZDZD)

95% CL upper limit on Β(H→ZDZD)

1

10−5

Observed:
13 TeV (97.6 fb-1 )
13.6 TeV (36.6 fb-1 )

68% quantile
95% quantile

1

10−5

D

Β (Z → µµ) = 0.143

10−4

10−6
10−3 10−2 10−1

10−2

H → ZDZD

10−3

10−4

10−1

CMS
m(Z ) = 20 GeV

10−2

Β (Z → µµ) = 0.144

10−3

10−5

1

10−4

Combined:
Observed
Expected

10−6
10−3 10−2 10−1

1

10

10−5

Observed:
13 TeV (97.6 fb-1 )
13.6 TeV (36.6 fb-1 )

68% quantile
95% quantile

2

10

3

10

4

10

5

10

6

10

cτ [cm]

Combined:
Observed
Expected

10−6
10−3 10−2 10−1

68% quantile
95% quantile

1

10

Observed:
13 TeV (97.6 fb-1 )
13.6 TeV (36.6 fb-1 )

102

103

104

105

106

cτ [cm]

Figure 15: The 95% CL upper limits on B(H → Z D Z D ) as a function of cτ (Z D ) in the HAHM
model, for m(Z D ) ranging from (upper left) 10 GeV to (lower right) 60 GeV, obtained in this
analysis, the Run 2 analysis [5], and their combination. The observed limits in this analysis and
in the Run 2 analysis [5] are shown as blue and red curves, respectively; the median combined
expected limits are shown as dashed black curves; and the combined observed limits are shown
as solid black curves. The green and yellow bands correspond, respectively, to the 68 and 95%
quantiles for the combined expected limits.

## PDF page 24

22

0
95% CL UL on σ(~
q~
q)Β(~
q→q∼
χ ) [pb]

36.6 fb-1 (13.6 TeV)

0
pp → ~
q~
q, ~
q → q∼
χ
1
m(~
q) = 125 GeV

10−1

1

1

CMS

1

1

∼0) [pb]
95% CL UL on σ(~
q~
q)Β(~
q→qχ

36.6 fb-1 (13.6 TeV)

CMS
0
pp → ~
q~
q, ~
q → q∼
χ
1
m(~
q) = 200 GeV

10−1

Β (∼χ → µµν) = 0.5
0
1

−2

10

Β (∼χ → µµν) = 0.5
0
1

−2

10

10−3

10−3

0
m(∼
χ1) = 50 GeV:
Observed
Expected

10−4
10−5

10−3 10−2 10−1

Observed, m(∼
χ1):
100 GeV

10−4

0

68% quantile
95% quantile

1

10

10−5
102

103

104

105

0
m(∼
χ1) = 50 GeV:
Observed
Expected

10−3 10−2 10−1

106

cτ [cm]

Observed, m(∼
χ1):
175 GeV
0

68% quantile
95% quantile

1

10

102

1

pp → ~
q~
q, ~
q → q∼
χ
1
m(~
q) = 350 GeV
0

−1

Β (∼χ → µµν) = 0.5

10

1

1

CMS

1

1

106

cτ [cm]

pp → ~
q~
q, ~
q → q∼
χ
1
m(~
q) = 700 GeV
0

−1

σth.(~
q~
q) ± unc.

Β (∼χ → µµν) = 0.5
0
1

10−2

10−3

10−3

0
m(∼
χ1) = 50 GeV:
Observed
Expected

10−4
10−5

10−3 10−2 10−1

∼ ):
Observed, m(χ
1
150 GeV
325 GeV

10−4

0

68% quantile
95% quantile

1

10

10−5
102

103

104

105

0
m(∼
χ1) = 50 GeV:
Observed
Expected

10−3 10−2 10−1

106

cτ [cm]

∼ ):
Observed, m(χ
1
500 GeV
675 GeV
0

68% quantile
95% quantile

1

10

102

0
pp → ~
q~
q, ~
q → q∼
χ
1
m(~
q) = 1150 GeV

10−1

1

1

CMS

1

10−1

Β (∼χ → µµν) = 0.5
0
1

σth.(~
q~
q) ± unc.

−2

10

103

10−5
−3

10

−2

10

−1

10

Observed, m(∼
χ1):
500 GeV
950 GeV
1125 GeV

0
pp → ~
q~
q, ~
q → q∼
χ
1
m(~
q) = 1600 GeV

Β (∼χ → µµν) = 0.5
0
1

−2

10−4

0

68% quantile
95% quantile

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

106

cτ [cm]

CMS

σth.(~
q~
q) ± unc.

10−3

0
m(∼
χ1) = 50 GeV:
Observed
Expected

105

10

10−3
10−4

104

36.6 fb-1 (13.6 TeV)
0
95% CL UL on σ(~
q~
q)Β(~
q→q∼
χ ) [pb]

36.6 fb-1 (13.6 TeV)
1

105

CMS

10

0

10−2

∼0) [pb]
95% CL UL on σ(~
q~
q)Β(~
q→qχ

104

36.6 fb-1 (13.6 TeV)
0
95% CL UL on σ(~
q~
q)Β(~
q→q∼
χ ) [pb]

∼0) [pb]
95% CL UL on σ(~
q~
q)Β(~
q→qχ

36.6 fb-1 (13.6 TeV)

103

10−5
6

10

cτ [cm]

0
m(∼
χ1) = 50 GeV:
Observed
Expected

10−3 10−2 10−1

68% quantile
95% quantile

Observed, m(∼
χ1):
500 GeV
950 GeV
1400 GeV
1575 GeV

1

102

0

10

103

104

105

106

cτ [cm]

Figure 16: The 95% CL upper limits on σ(pp → q̃ q̃ )B(q̃ → q χ̃ 01 ) as a function of cτ (χ̃ 01 ) in the
RPV SUSY model, for B(χ̃ 01 → µ + µ − ν ) = 0.5 and m(q̃ ) ranging from (upper left) 125 GeV to
(lower right) 1.6 TeV. The observed limits for various combinations of m(q̃ ) and m(χ̃ 01 ) indicated in the legends are shown as solid curves. The median expected limits and their 68 and
95% quantiles are shown, respectively, as dashed black curves and green and yellow bands for
the case of m(χ̃ 01 ) = 50 GeV and omitted for other neutralino masses for clarity. The gray horizontal lines indicate the theoretical values of the squark-antisquark production cross sections
with the uncertainties shown as gray shaded bands. The predicted cross sections for m(q̃ ) =
125, 200, and 350 GeV are, respectively, 7200, 840, and 50 pb, and fall outside the y-axis range.

## PDF page 25

23
the individual dimuon categories as well as the expected and observed limits obtained in the
ensemble of both categories. Figure 15 compares the observed limits obtained in this analysis
with the corresponding Run 2 limits [5], and shows the expected and observed limits obtained
in a combination of the two results.
Even though the size of the data sample used by this analysis is about a factor of 2.5 smaller
than that in the Run 2 analysis, the constraints on the parameters of the HAHM model are
comparable or tighter in a significant fraction of the parameter space, thanks mainly to improvements in the trigger algorithms. The combined limits on B(H → Z D Z D ) are approximately a factor of 2 more stringent than the limits obtained in the Run 2 analysis. They exclude
B(H → Z D Z D ) of 1% in the range of cτ (Z D ) from a few tens of µm to 30 m (700 m) for m(Z D )
= 10 GeV (60 GeV) at 95% CL. In the m(Z D ) interval 20–60 GeV, B(H → Z D Z D ) as low as 0.01%
is excluded at 95% CL in the cτ (Z D ) range of about 0.3 mm to 0.5 m, which corresponds to a
wide range of ϵ values from ≈10−8 to ≈10−6 . These constraints on rare SM Higgs boson decays are tighter than those derived from searches for invisible Higgs boson decays [40, 41] and
from measurements of the SM Higgs boson couplings [42]. At m(Z D ) > 20 GeV, the limits
obtained are the most stringent limits to date for all cτ (Z D ) values except those between ≈0.1
and ≈10 cm (depending on m(Z D )), where a previous CMS search [7] using data collected with
a dedicated high-rate data stream provides the best limits.
Figure 16 shows the observed and expected 95% CL upper limits obtained in the ensemble of
both dimuon categories in the framework of the RPV SUSY model. The limits are set on the
product σ(pp → q̃ q̃ )B(q̃ → q χ̃ 01 ) assuming B(χ̃ 01 → µ + µ − ν ) = 0.5. They are shown as functions of the mean proper decay length of χ̃ 01 for the various combinations of m(q̃ ) and m(χ̃ 01 )
indicated in the legends, for m(q̃ ) values ranging from 125 GeV to 1.6 TeV, and compared to the
theoretical predictions. At a squark mass of 700 GeV, the data exclude the mean proper neutralino decay lengths between 30 µm and 350 m (at m(χ̃ 01 ) = 50 GeV), and between 30 µm and
1.5 km (at m(χ̃ 01 ) = 500 GeV). At a squark mass of 1.6 TeV, the excluded cτ (χ̃ 01 ) range is between
0.07 and 4 cm for m(χ̃ 01 ) = 50 GeV and between 70 µm and 2 m for m(χ̃ 01 ) = 500 GeV. The limits
obtained in this analysis are tighter than those derived by CMS in the Run 1 search [8, 9] in all
of the relevant (m(q̃ ), m(χ̃ 01 ), cτ (χ̃ 01 )) parameter space and are more stringent at cτ (χ̃ 01 ) ≲ 1 cm
and cτ (χ̃ 01 ) ≳ 1 m than the limits on the λ122 RPV coupling set by the ATLAS Collaboration at
m(q̃ ) of 700 GeV and 1.6 TeV [11].

8

Summary

√
Data collected by the CMS experiment in proton-proton collisions at s = 13.6 TeV in 2022
and corresponding to an integrated luminosity of 36.6 fb−1 have been used to conduct an inclusive search for long-lived exotic neutral particles decaying to final states with a pair of oppositely charged muons. The search strategy is largely model independent and is sensitive to a
broad range of lifetimes and masses. No significant excess of events above the standard model
background is observed. The results are interpreted as limits on the parameters of the hidden
Abelian Higgs model, in which the Higgs boson H decays to a pair of long-lived dark photons
Z D , and of an R-parity violating supersymmetry model, in which long-lived neutralinos decay
to a pair of muons and a neutrino.
Even though the size of the data sample used by this analysis is about a factor of 2.5 smaller
than that used
√ in the previous search for displaced dimuons by the CMS experiment in pp
collisions at s = 13 TeV, the constraints on the parameters of the hidden Abelian Higgs model
are comparable or tighter in a significant fraction of the parameter space, thanks mainly to

## PDF page 26

24
improvements in the trigger
algorithms. The combination of the results of this analysis with
√
the results obtained at s = 13 TeV improves the constraints on the branching fraction of the
Higgs boson to dark photons, B(H → Z D Z D ), by approximately a factor of 2. In the range
10–60 GeV of the Z D mass m(Z D ), B(H → Z D Z D ) = 1% is excluded at 95% confidence level
in the range of proper decay length cτ (Z D ) from a few tens of µm to 30 m (700 m) for m(Z D )
= 10 GeV (60 GeV). For m(Z D ) greater than 20 GeV and less than m(H )/2, the combined limits
provide the most stringent constraints to date on B(H → Z D Z D ) for cτ (Z D ) between 30 µm
and ≈0.1 cm, and above ≈10 cm. When interpreted in the framework of the R-parity violating
supersymmetry model at a squark mass of 1.6 TeV, the results exclude mean proper neutralino
decay lengths between 0.07 and 4 cm for a 50 GeV neutralino and between 70 µm and 2 m for a
500 GeV neutralino.

Acknowledgments
We congratulate our colleagues in the CERN accelerator departments for the excellent performance of the LHC and thank the technical and administrative staffs at CERN and at other
CMS institutes for their contributions to the success of the CMS effort. In addition, we gratefully acknowledge the computing centers and personnel of the Worldwide LHC Computing
Grid and other centers for delivering so effectively the computing infrastructure essential to
our analyses. Finally, we acknowledge the enduring support for the construction and operation of the LHC, the CMS detector, and the supporting computing infrastructure provided
by the following funding agencies: SC (Armenia), BMBWF and FWF (Austria); FNRS and
FWO (Belgium); CNPq, CAPES, FAPERJ, FAPERGS, and FAPESP (Brazil); MES and BNSF
(Bulgaria); CERN; CAS, MoST, and NSFC (China); MINCIENCIAS (Colombia); MSES and CSF
(Croatia); RIF (Cyprus); SENESCYT (Ecuador); ERC PRG, RVTT3 and MoER TK202 (Estonia);
Academy of Finland, MEC, and HIP (Finland); CEA and CNRS/IN2P3 (France); SRNSF (Georgia); BMBF, DFG, and HGF (Germany); GSRI (Greece); NKFIH (Hungary); DAE and DST (India); IPM (Iran); SFI (Ireland); INFN (Italy); MSIP and NRF (Republic of Korea); MES (Latvia);
LMTLT (Lithuania); MOE and UM (Malaysia); BUAP, CINVESTAV, CONACYT, LNS, SEP, and
UASLP-FAI (Mexico); MOS (Montenegro); MBIE (New Zealand); PAEC (Pakistan); MES and
NSC (Poland); FCT (Portugal); MESTD (Serbia); MCIN/AEI and PCTI (Spain); MOSTR (Sri
Lanka); Swiss Funding Agencies (Switzerland); MST (Taipei); MHESI and NSTDA (Thailand);
TUBITAK and TENMAK (Turkey); NASU (Ukraine); STFC (United Kingdom); DOE and NSF
(USA).
Individuals have received support from the Marie-Curie program and the European Research
Council and Horizon 2020 Grant, contract Nos. 675440, 724704, 752730, 758316, 765710, 824093,
101115353, and COST Action CA16108 (European Union); the Leventis Foundation; the Alfred P. Sloan Foundation; the Alexander von Humboldt Foundation; the Science Committee,
project no. 22rl-037 (Armenia); the Belgian Federal Science Policy Office; the Fonds pour la Formation à la Recherche dans l’Industrie et dans l’Agriculture (FRIA-Belgium); the Agentschap
voor Innovatie door Wetenschap en Technologie (IWT-Belgium); the F.R.S.-FNRS and FWO
(Belgium) under the “Excellence of Science – EOS” – be.h project n. 30820817; the Beijing
Municipal Science & Technology Commission, No. Z191100007219010 and Fundamental Research Funds for the Central Universities (China); the Ministry of Education, Youth and Sports
(MEYS) of the Czech Republic; the Shota Rustaveli National Science Foundation, grant FR22-985 (Georgia); the Deutsche Forschungsgemeinschaft (DFG), under Germany’s Excellence
Strategy – EXC 2121 “Quantum Universe” – 390833306, and under project number 400140256 GRK2497; the Hellenic Foundation for Research and Innovation (HFRI), Project Number 2288
(Greece); the Hungarian Academy of Sciences, the New National Excellence Program - ÚNKP,

## PDF page 27

References

25

the NKFIH research grants K 124845, K 124850, K 128713, K 128786, K 129058, K 131991,
K 133046, K 138136, K 143460, K 143477, 2020-2.2.1-ED-2021-00181, and TKP2021-NKTA-64
(Hungary); the Council of Science and Industrial Research, India; ICSC – National Research
Center for High Performance Computing, Big Data and Quantum Computing, funded by the
NextGenerationEU program (Italy); the Latvian Council of Science; the Ministry of Education and Science, project no. 2022/WK/14, and the National Science Center, contracts Opus
2021/41/B/ST2/01369 and 2021/43/B/ST2/01552 (Poland); the Fundação para a Ciência e a
Tecnologia, grant CEECIND/01334/2018 (Portugal); the National Priorities Research Program
by Qatar National Research Fund; MCIN/AEI/10.13039/501100011033, ERDF “a way of making Europe”, and the Programa Estatal de Fomento de la Investigación Cientı́fica y Técnica de
Excelencia Marı́a de Maeztu, grant MDM-2017-0765 and Programa Severo Ochoa del Principado de Asturias (Spain); the Chulalongkorn Academic into Its 2nd Century Project Advancement Project, and the National Science, Research and Innovation Fund via the Program Management Unit for Human Resources & Institutional Development, Research and Innovation,
grant B37G660013 (Thailand); the Kavli Foundation; the Nvidia Corporation; the SuperMicro Corporation; the Welch Foundation, contract C-1845; and the Weston Havens Foundation
(USA).

References
[1] J. L. Hewett, B. Lillie, M. Masip, and T. G. Rizzo, “Signatures of long-lived gluinos in split
supersymmetry”, JHEP 09 (2004) 070, doi:10.1088/1126-6708/2004/09/070,
arXiv:hep-ph/0408248.
[2] R. Barbier et al., “R-parity-violating supersymmetry”, Phys. Rept. 420 (2005) 1,
doi:10.1016/j.physrep.2005.08.006, arXiv:hep-ph/0406039.
[3] M. J. Strassler and K. M. Zurek, “Echoes of a hidden valley at hadron colliders”, Phys.
Lett. B 651 (2007) 374, doi:10.1016/j.physletb.2007.06.055,
arXiv:hep-ph/0604261.
[4] T. Han, Z. Si, K. M. Zurek, and M. J. Strassler, “Phenomenology of hidden valleys at
hadron colliders”, JHEP 07 (2008) 008, doi:10.1088/1126-6708/2008/07/008,
arXiv:0712.2041.
[5] CMS Collaboration, “Search√for long-lived particles decaying to a pair of muons in
proton-proton collisions at s = 13 TeV”, JHEP 05 (2023) 228,
doi:10.1007/JHEP05(2023)228, arXiv:2205.08582.
[6] D. Curtin, R. Essig, S. Gori, and J. Shelton, “Illuminating dark photons with high-energy
colliders”, JHEP 02 (2015) 157, doi:10.1007/JHEP02(2015)157,
arXiv:1412.0018.
[7] CMS Collaboration, “Search√for long-lived particles decaying into muon pairs in
proton-proton collisions at s = 13 TeV collected with a dedicated high-rate data
stream”, JHEP 04 (2022) 062, doi:10.1007/JHEP04(2022)062,
arXiv:2112.13769.
[8] CMS Collaboration, “Search for long-lived particles that decay
√ into final states containing
two electrons or two muons in proton-proton collisions at s = 8 TeV”, Phys. Rev. D 91
(2015) 052012, doi:10.1103/PhysRevD.91.052012, arXiv:1411.6977.

## PDF page 28

26
[9] CMS Collaboration, “Search for long-lived particles that decay into final states containing
two muons, reconstructed using only the CMS muon chambers”, CMS Physics Analysis
Summary CMS-PAS-EXO-14-012, 2015.
[10] ATLAS Collaboration, “Search for long-lived
particles in final states with displaced
√
dimuon vertices in pp collisions at s = 13 TeV with the ATLAS detector”, Phys. Rev. D
99 (2019) 012001, doi:10.1103/PhysRevD.99.012001, arXiv:1808.03057.
[11] ATLAS Collaboration, “Search for displaced vertices
√ of oppositely charged leptons from
decays of long-lived particles in pp collisions at s = 13 TeV with the ATLAS detector”,
Phys. Lett. B 801 (2020) 135114, doi:10.1016/j.physletb.2019.135114,
arXiv:1907.10037.
[12] HEPData record for this analysis, 2024. doi:10.17182/hepdata.146759.
[13] CMS Collaboration, “Performance
√ of the CMS muon detector and muon reconstruction
with proton-proton collisions at s = 13 TeV”, JINST 13 (2018) P06015,
doi:10.1088/1748-0221/13/06/P06015, arXiv:1804.04528.
[14] CMS Collaboration, “The CMS experiment at the CERN LHC”, JINST 3 (2008) S08004,
doi:10.1088/1748-0221/3/08/S08004.
[15] CMS Collaboration, “Development of the CMS detector for the CERN LHC Run 3”, 2023.
arXiv:2309.05466. Accepted by JINST.
[16] CMS
√ Collaboration, “Performance of the CMS Level-1 trigger in proton-proton collisions
at s = 13 TeV”, JINST 15 (2020) P10017, doi:10.1088/1748-0221/15/10/P10017,
arXiv:2006.10165.
[17] CMS Collaboration, “The CMS trigger system”, JINST 12 (2017) P01020,
doi:10.1088/1748-0221/12/01/P01020, arXiv:1609.02366.
[18] J. D. Wells, “How to find a hidden world at the Large Hadron Collider”, in Perspectives
on LHC Physics, G. Kane and A. Pierce, eds., p. 283. World Scientific, Singapore, 2008.
arXiv:0803.1243. doi:10.1142/9789812779762_0015.
[19] J. Alwall et al., “The automated computation of tree-level and next-to-leading order
differential cross sections, and their matching to parton shower simulations”, JHEP 07
(2014) 079, doi:10.1007/JHEP07(2014)079, arXiv:1405.0301.
[20] M. Cepeda et al., “Report from working group 2: Higgs physics at the HL-LHC and
HE-LHC”, in Proceedings of the HL/HE-LHC Workshop, A. Dainese et al., eds., volume 7,
p. 221. 2019. arXiv:1902.00134. CERN Yellow Rep. Monogr.
doi:10.23731/CYRM-2019-007.221.
[21] LHC Higgs Cross Section Working Group, “Ad interim 13.6 TeV cross sections”, 2023.
https:
//twiki.cern.ch/twiki/bin/view/LHCPhysics/LHCHWG136TeVxsec_extrap.
[22] T. Sjöstrand et al., “An introduction to PYTHIA 8.2”, Comput. Phys. Commun. 191 (2015)
159, doi:10.1016/j.cpc.2015.01.024, arXiv:1410.3012.
[23] H. K. Dreiner, “An introduction to explicit R-parity violation”, Adv. Ser. Direct. High
Energy Phys. 21 (2010) 565, doi:10.1142/9789814307505_0017,
arXiv:hep-ph/9707435.

## PDF page 29

References

27

[24] D. Dercks et al., “R-parity violation at the LHC”, Eur. Phys. J. C 77 (2017) 856,
doi:10.1140/epjc/s10052-017-5414-4, arXiv:1706.09418.
[25] W. Beenakker et al., “NNLL-fast: predictions for coloured supersymmetric particle
production at the LHC with threshold and Coulomb resummation”, JHEP 12 (2016) 133,
doi:10.1007/JHEP12(2016)133, arXiv:1607.07741.
[26] PDF4LHC Working Group, R. D. Ball et al., “The PDF4LHC21 combination of global
PDF fits for the LHC Run III”, J. Phys. G 49 (2022) 080501,
doi:10.1088/1361-6471/ac7216, arXiv:2203.05506.
[27] NNPDF Collaboration, “Parton distributions from high-precision collider data”, Eur.
Phys. J. C 77 (2017) 663, doi:10.1140/epjc/s10052-017-5199-5,
arXiv:1706.00428.
[28] CMS Collaboration, “Extraction and validation of a new set of CMS PYTHIA8 tunes from
underlying-event measurements”, Eur. Phys. J. C 80 (2020) 4,
doi:10.1140/epjc/s10052-019-7499-4, arXiv:1903.12179.
[29] G EANT 4 Collaboration, “G EANT 4—a simulation toolkit”, Nucl. Instrum. Meth. A 506
(2003) 250, doi:10.1016/S0168-9002(03)01368-8.
[30] W. A. Nash, “Search for long-lived particles that decay to muon pairs at 13 TeV and an
algorithm to improve resolution in the muon system of the Compact Muon Solenoid”.
PhD thesis, University of California, Los Angeles, 2022.
https://escholarship.org/uc/item/3gw9h84p.
[31] CMS Collaboration, “Technical proposal for the Phase-II upgrade of the Compact Muon
Solenoid”, CMS Technical Proposal CERN-LHCC-2015-010, CMS-TDR-15-02, 2015.
[32] CMS Collaboration,
“Performance of the CMS muon trigger system in proton-proton
√
collisions at s = 13 TeV”, JINST 16 (2021) P07001,
doi:10.1088/1748-0221/16/07/P07001, arXiv:2102.04790.
[33] CMS
√ Collaboration, “Performance of CMS muon reconstruction in pp collision events at
s = 7 TeV”, JINST 7 (2012) P10002, doi:10.1088/1748-0221/7/10/P10002,
arXiv:1206.4071.
[34] LHCb Collaboration, “Identification of beauty and charm quark jets at LHCb”, JINST 10
(2015) P06013, doi:10.1088/1748-0221/10/06/P06013, arXiv:1504.07670.
[35] CMS Collaboration, “Identification of heavy-flavour jets with the CMS detector in pp
collisions at 13 TeV”, JINST 13 (2018) P05011,
doi:10.1088/1748-0221/13/05/P05011, arXiv:1712.07158.
[36] CMS Collaboration, “First measurement
of the top quark pair production cross section in
√
proton-proton collisions at s = 13.6 TeV”, JHEP 08 (2023) 204,
doi:10.1007/JHEP08(2023)204, arXiv:2303.10680.
[37] A. L. Read, “Presentation of search results: The CLs technique”, J. Phys. G 28 (2002) 2693,
doi:10.1088/0954-3899/28/10/313.
[38] T. Junk, “Confidence level computation for combining searches with small statistics”,
Nucl. Instrum. Meth. A 434 (1999) 435, doi:10.1016/S0168-9002(99)00498-2,
arXiv:hep-ex/9902006.

## PDF page 30

28
[39] CMS Collaboration, “The CMS statistical analysis and combination tool: C OMBINE”,
2024. arXiv:2404.06614. Submitted to Comput. Softw. Big Sci.
[40] CMS Collaboration, “A search for decays of the Higgs boson to invisible particles in
events
with a top-antitop quark pair or a vector boson in proton-proton collisions at
√
s = 13 TeV”, Eur. Phys. J. C 83 (2023) 933,
doi:10.1140/epjc/s10052-023-11952-7, arXiv:2303.01214.
[41] CMS Collaboration, “Search for invisible decays of√
a Higgs boson produced through
vector boson fusion in proton–proton collisions at s = 13 TeV”, Phys. Rev. D 105 (2022)
092007, doi:10.1103/PhysRevD.105.092007, arXiv:2201.11585.
[42] CMS Collaboration, “Combined
√ measurements of Higgs boson couplings in
proton–proton collisions at s = 13 TeV”, Eur. Phys. J. C 79 (2019) 421,
doi:10.1140/epjc/s10052-019-6909-y, arXiv:1809.10733.

## PDF page 31

29

A

The CMS Collaboration

Yerevan Physics Institute, Yerevan, Armenia
A. Hayrapetyan, A. Tumasyan1
Institut für Hochenergiephysik, Vienna, Austria
W. Adam , J.W. Andrejkovic, T. Bergauer , S. Chatterjee , K. Damanakis , M. Dragicevic , P.S. Hussain , M. Jeitler2 , N. Krammer , A. Li , D. Liko , I. Mikulec ,
J. Schieck2 , R. Schöfbeck , D. Schwarz , M. Sonawane , S. Templ , W. Waltenberger ,
C.-E. Wulz2
Universiteit Antwerpen, Antwerpen, Belgium
M.R. Darwish3 , T. Janssen , P. Van Mechelen
Vrije Universiteit Brussel, Brussel, Belgium
E.S. Bols , J. D’Hondt , S. Dansana , A. De Moor , M. Delcourt
I. Makarenko , D. Müller , S. Tavernier , M. Tytgat4 , G.P. Van Onsem
D. Vannerom

, S. Lowette
, S. Van Putte

,
,

Université Libre de Bruxelles, Bruxelles, Belgium
B. Clerbaux , A.K. Das, G. De Lentdecker , H. Evard , L. Favart , P. Gianneios
D. Hohov , J. Jaramillo , A. Khalilzadeh, F.A. Khan , K. Lee , M. Mahdavikhorrami
A. Malara , S. Paredes , L. Thomas , M. Vanden Bemden , C. Vander Velde
P. Vanlaer

,
,
,

Ghent University, Ghent, Belgium
M. De Coen , D. Dobur , Y. Hong , J. Knolle , L. Lambrecht , G. Mestdach,
K. Mota Amarilo , C. Rendón, A. Samalan, K. Skovpen , N. Van Den Bossche ,
J. van der Linden , L. Wezenbeek
Université Catholique de Louvain, Louvain-la-Neuve, Belgium
A. Benecke , A. Bethani , G. Bruno , C. Caputo , C. Delaere , I.S. Donertas
A. Giammanco , Sa. Jain , V. Lemaitre, J. Lidrych , P. Mastrapasqua , T.T. Tran
S. Wertz

,
,

Centro Brasileiro de Pesquisas Fisicas, Rio de Janeiro, Brazil
G.A. Alves , E. Coelho , C. Hensel , T. Menezes De Oliveira
P. Rebello Teles , M. Soeiro

,

, A. Moraes

Universidade do Estado do Rio de Janeiro, Rio de Janeiro, Brazil
W.L. Aldá Júnior , M. Alves Gallo Pereira , M. Barroso Ferreira Filho , H. Brandao Malbouisson , W. Carvalho , J. Chinellato5 , E.M. Da Costa , G.G. Da Silveira6 ,
D. De Jesus Damiao , S. Fonseca De Souza , R. Gomes De Souza, J. Martins7 ,
C. Mora Herrera , L. Mundim , H. Nogima , J.P. Pinheiro , A. Santoro , A. Sznajder ,
M. Thiel , A. Vilela Pereira
Universidade Estadual Paulista, Universidade Federal do ABC, São Paulo, Brazil
C.A. Bernardes6 , L. Calligaris , T.R. Fernandez Perez Tomei , E.M. Gregores
P.G. Mercadante , S.F. Novaes , B. Orzari , Sandra S. Padula

,

Institute for Nuclear Research and Nuclear Energy, Bulgarian Academy of Sciences, Sofia,
Bulgaria
A. Aleksandrov , G. Antchev , R. Hadjiiska , P. Iaydjiev , M. Misheva , M. Shopova ,
G. Sultanov

## PDF page 32

30
University of Sofia, Sofia, Bulgaria
A. Dimitrov , L. Litov , B. Pavlov

, P. Petkov

, A. Petrov

, E. Shumka

Instituto De Alta Investigación, Universidad de Tarapacá, Casilla 7 D, Arica, Chile
S. Keshri , S. Thakur
Beihang University, Beijing, China
T. Cheng , T. Javaid , L. Yuan
Department of Physics, Tsinghua University, Beijing, China
Z. Hu , J. Liu, K. Yi8,9
Institute of High Energy Physics, Beijing, China
G.M. Chen10 , H.S. Chen10 , M. Chen10 , F. Iemmi , C.H. Jiang, A. Kapoor11 ,
H. Liao , Z.-A. Liu12 , R. Sharma13 , J.N. Song12 , J. Tao , C. Wang10 , J. Wang , Z. Wang10 ,
H. Zhang
State Key Laboratory of Nuclear Physics and Technology, Peking University, Beijing, China
A. Agapitos , Y. Ban , A. Levin , C. Li , Q. Li , Y. Mao, S.J. Qian , X. Sun ,
D. Wang , H. Yang, L. Zhang , C. Zhou
Sun Yat-Sen University, Guangzhou, China
Z. You
University of Science and Technology of China, Hefei, China
K. Jaffel , N. Lu
Nanjing Normal University, Nanjing, China
G. Bauer14
Institute of Modern Physics and Key Laboratory of Nuclear Physics and Ion-beam
Application (MOE) - Fudan University, Shanghai, China
X. Gao15
Zhejiang University, Hangzhou, Zhejiang, China
Z. Lin , C. Lu , M. Xiao
Universidad de Los Andes, Bogota, Colombia
C. Avila , D.A. Barbosa Trujillo, A. Cabrera , C. Florez

, J. Fraga

, J.A. Reyes Vega

Universidad de Antioquia, Medellin, Colombia
J. Mejia Guisao , F. Ramirez , M. Rodriguez , J.D. Ruiz Alvarez
University of Split, Faculty of Electrical Engineering, Mechanical Engineering and Naval
Architecture, Split, Croatia
D. Giljanovic , N. Godinovic , D. Lelas , A. Sculac
University of Split, Faculty of Science, Split, Croatia
M. Kovac , T. Sculac
Institute Rudjer Boskovic, Zagreb, Croatia
P. Bargassa , V. Brigljevic , B.K. Chitroda
A. Starodumov16 , T. Susa

, D. Ferencek

, K. Jakovcic, S. Mishra

University of Cyprus, Nicosia, Cyprus
A. Attikis , K. Christoforou , A. Hadjiagapiou, S. Konstantinou , J. Mousa
F. Ptochos , P.A. Razis , H. Rykaczewski, H. Saka , A. Stepennov

,

, C. Nicolaou,

## PDF page 33

31
Charles University, Prague, Czech Republic
M. Finger , M. Finger Jr. , A. Kveton
Escuela Politecnica Nacional, Quito, Ecuador
E. Ayala
Universidad San Francisco de Quito, Quito, Ecuador
E. Carrera Jarrin
Academy of Scientific Research and Technology of the Arab Republic of Egypt, Egyptian
Network of High Energy Physics, Cairo, Egypt
H. Abdalla17 , Y. Assran18,19
Center for High Energy Physics (CHEP-FU), Fayoum University, El-Fayoum, Egypt
M.A. Mahmoud , Y. Mohammed
National Institute of Chemical Physics and Biophysics, Tallinn, Estonia
K. Ehataht , M. Kadastik, T. Lange , S. Nandan , C. Nielsen , J. Pata
L. Tani , C. Veelken

, M. Raidal

,

Department of Physics, University of Helsinki, Helsinki, Finland
H. Kirschenmann , K. Osterberg , M. Voutilainen
Helsinki Institute of Physics, Helsinki, Finland
S. Bharthuar , E. Brücken , F. Garcia , K.T.S. Kallonen , R. Kinnunen, T. Lampén ,
K. Lassila-Perini , S. Lehti , T. Lindén , L. Martikainen , M. Myllymäki , M.m. Rantanen , H. Siikonen , E. Tuominen , J. Tuominiemi
Lappeenranta-Lahti University of Technology, Lappeenranta, Finland
P. Luukka , H. Petrow
IRFU, CEA, Université Paris-Saclay, Gif-sur-Yvette, France
M. Besancon , F. Couderc , M. Dejardin , D. Denegri, J.L. Faure, F. Ferri , S. Ganjour ,
P. Gras , G. Hamel de Monchenault , V. Lohezic , J. Malcles , L. Portales , J. Rander,
A. Rosowsky , M.Ö. Sahin , A. Savoy-Navarro20 , P. Simkina , M. Titov , M. Tornago
Laboratoire Leprince-Ringuet, CNRS/IN2P3, Ecole Polytechnique, Institut Polytechnique
de Paris, Palaiseau, France
F. Beaudette , A. Buchot Perraguin , P. Busson , A. Cappati , C. Charlot , M. Chiusi ,
F. Damas , O. Davignon , A. De Wit , I.T. Ehle , B.A. Fontana Santos Alves ,
S. Ghosh , A. Gilbert , R. Granier de Cassagnac , A. Hakimi , B. Harikrishnan ,
L. Kalipoliti , G. Liu , J. Motta , M. Nguyen , C. Ochando , R. Salerno , J.B. Sauvan ,
Y. Sirois , A. Tarabini , E. Vernazza , A. Zabi , A. Zghiche
Université de Strasbourg, CNRS, IPHC UMR 7178, Strasbourg, France
J.-L. Agram21 , J. Andrea , D. Apparu , D. Bloch , J.-M. Brom , E.C. Chabert
C. Collard , S. Falke , U. Goerlach , C. Grimault, R. Haeberle , A.-C. Le Bihan
M. Meena , G. Saha , M.A. Sessini , P. Van Hove

,
,

Institut de Physique des 2 Infinis de Lyon (IP2I ), Villeurbanne, France
S. Beauceron , B. Blancon , G. Boudoul , N. Chanon , J. Choi , D. Contardo ,
P. Depasse , C. Dozen22 , H. El Mamouni, J. Fay , S. Gascon , M. Gouzevitch ,
C. Greenberg, G. Grenier , B. Ille , I.B. Laktineh, M. Lethuillier , L. Mirabito, S. Perries,
A. Purohit , M. Vander Donckt , P. Verdier , J. Xiao
Georgian Technical University, Tbilisi, Georgia

## PDF page 34

32
I. Lomidze

, T. Toriashvili23

, Z. Tsamalaidze16

RWTH Aachen University, I. Physikalisches Institut, Aachen, Germany
V. Botta , L. Feld , K. Klein , M. Lipinski , D. Meuser , A. Pauls
M. Teroerde

, N. Röwert

,

RWTH Aachen University, III. Physikalisches Institut A, Aachen, Germany
S. Diekmann , A. Dodonova , N. Eich , D. Eliseev , F. Engelke , J. Erdmann,
M. Erdmann , P. Fackeldey , B. Fischer , T. Hebbeker , K. Hoepfner , F. Ivone ,
A. Jung , M.y. Lee , F. Mausolf , M. Merschmeyer , A. Meyer , S. Mukherjee ,
D. Noll , F. Nowotny, A. Pozdnyakov , Y. Rath, W. Redjeb , F. Rehm, H. Reithler ,
U. Sarkar , V. Sarkisovi , A. Schmidt , A. Sharma , J.L. Spah , A. Stein ,
F. Torres Da Silva De Araujo24 , S. Wiedenbeck , S. Zaleski
RWTH Aachen University, III. Physikalisches Institut B, Aachen, Germany
C. Dziwok , G. Flügge , W. Haj Ahmad25 , T. Kress , A. Nowack
A. Stahl , T. Ziemons , A. Zotz

, O. Pooth

,

Deutsches Elektronen-Synchrotron, Hamburg, Germany
H. Aarup Petersen , M. Aldaya Martin , J. Alimena , S. Amoroso, Y. An , S. Baxter ,
M. Bayatmakou , H. Becerril Gonzalez , O. Behnke , A. Belvedere , S. Bhattacharya ,
F. Blekman26 , K. Borras27 , A. Campbell , A. Cardini , C. Cheng, F. Colombina ,
S. Consuegra Rodrı́guez , G. Correia Silva , M. De Silva , G. Eckerlin, D. Eckstein ,
L.I. Estevez Banos , O. Filatov , E. Gallo26 , A. Geiser , A. Giraldi , V. Guglielmi ,
M. Guthoff , A. Hinzmann , A. Jafari28 , L. Jeppe , N.Z. Jomhari , B. Kaech ,
M. Kasemann , C. Kleinwort , R. Kogler , M. Komm , D. Krücker , W. Lange,
D. Leyva Pernia , K. Lipka29 , W. Lohmann30 , F. Lorkowski , R. Mankel , I.-A. MelzerPellmann , M. Mendizabal Morentin , A.B. Meyer , G. Milella , A. Mussgiller ,
L.P. Nair , A. Nürnberg , Y. Otarid, J. Park , D. Pérez Adán , E. Ranken ,
A. Raspereza , D. Rastorguev , B. Ribeiro Lopes , J. Rübenach, A. Saggio ,
M. Scham31,27 , S. Schnake27 , P. Schütze , C. Schwanenberger26 , D. Selivanova ,
K. Sharko , M. Shchedrolosiev , R.E. Sosa Ricardo , D. Stafford, F. Vazzoler ,
A. Ventura Barroso , R. Walsh , Q. Wang , Y. Wen , K. Wichmann, L. Wiens27 ,
C. Wissing , Y. Yang , A. Zimermmane Castro Santos
University of Hamburg, Hamburg, Germany
A. Albrecht , S. Albrecht , M. Antonello , S. Bein , L. Benato , S. Bollweg,
M. Bonanomi , P. Connor , K. El Morabit , Y. Fischer , E. Garutti , A. Grohsjean ,
J. Haller , H.R. Jabusch , G. Kasieczka , P. Keicher, R. Klanner , W. Korcari ,
T. Kramer , V. Kutzner , F. Labe , J. Lange , A. Lobanov , C. Matthies , A. Mehta ,
L. Moureaux , M. Mrowietz, A. Nigamova , Y. Nissan, A. Paasch , K.J. Pena Rodriguez ,
T. Quadfasel , B. Raciti , M. Rieger , D. Savoiu , J. Schindler , P. Schleper ,
M. Schröder , J. Schwandt , M. Sommerhalder , H. Stadie , G. Steinbrück , A. Tews,
M. Wolf
Karlsruher Institut fuer Technologie, Karlsruhe, Germany
S. Brommer , M. Burkart, E. Butz , T. Chwalek , A. Dierlamm , A. Droll, N. Faltermann , M. Giffels , A. Gottmann , F. Hartmann32 , R. Hofsaess , M. Horzela ,
U. Husemann , J. Kieseler , M. Klute , R. Koppenhöfer , J.M. Lawhorn , M. Link,
A. Lintuluoto , B. Maier , S. Maier , S. Mitra , M. Mormile , Th. Müller , M. Neukum,
M. Oh , E. Pfeffer , M. Presilla , G. Quast , K. Rabbertz , B. Regnery , N. Shadskiy ,
I. Shvetsov , H.J. Simonis , M. Toms , N. Trevisani , R.F. Von Cube , M. Wassmer ,

## PDF page 35

33
S. Wieland

, F. Wittig, R. Wolf

, X. Zuo

Institute of Nuclear and Particle Physics (INPP), NCSR Demokritos, Aghia Paraskevi,
Greece
G. Anagnostou, G. Daskalakis , A. Kyriakis, A. Papadopoulos32 , A. Stakia
National and Kapodistrian University of Athens, Athens, Greece
P. Kontaxakis , G. Melachroinos, Z. Painesis , A. Panagiotou, I. Papavergou ,
I. Paraskevas , N. Saoulidou , K. Theofilatos , E. Tziaferi , K. Vellidis , I. Zisopoulos
National Technical University of Athens, Athens, Greece
G. Bakas , T. Chatzistavrou, G. Karapostoli , K. Kousouris
E. Siamarkou, G. Tsipolitis, A. Zacharopoulou

, I. Papakrivopoulos

,

University of Ioánnina, Ioánnina, Greece
K. Adamidis, I. Bestintzanos, I. Evangelou , C. Foudas, C. Kamtsikis, P. Katsoulis,
P. Kokkas , P.G. Kosmoglou Kioseoglou , N. Manthos , I. Papadopoulos , J. Strologas
HUN-REN Wigner Research Centre for Physics, Budapest, Hungary
M. Bartók33 , C. Hajdu , D. Horvath34,35 , K. Márton, A.J. Rádl36
V. Veszpremi

, F. Sikler

,

MTA-ELTE Lendület CMS Particle and Nuclear Physics Group, Eötvös Loránd University,
Budapest, Hungary
M. Csanád , K. Farkas , M.M.A. Gadallah37 , Á. Kadlecsik , P. Major , K. Mandal ,
G. Pásztor , G.I. Veres
Faculty of Informatics, University of Debrecen, Debrecen, Hungary
P. Raics, B. Ujvari , G. Zilizi
Institute of Nuclear Research ATOMKI, Debrecen, Hungary
G. Bencze, S. Czellar, J. Molnar, Z. Szillasi
Karoly Robert Campus, MATE Institute of Technology, Gyongyos, Hungary
T. Csorgo38 , F. Nemes38 , T. Novak
Panjab University, Chandigarh, India
J. Babbar , S. Bansal , S.B. Beri, V. Bhatnagar , G. Chaudhary , S. Chauhan
N. Dhingra39 , A. Kaur , A. Kaur , H. Kaur , M. Kaur , S. Kumar , K. Sandeep
T. Sheokand, J.B. Singh , A. Singla

,
,

University of Delhi, Delhi, India
A. Ahmed , A. Bhardwaj , A. Chhetri
M. Naimuddin , K. Ranjan , S. Saumya

, A. Kumar

,

Indian Institute of Technology Madras, Madras, India
M.M. Ameen , P.K. Behera , S.C. Behera , S. Chatterjee , P. Jana , P. Kalbhor
J.R. Komaragiri41 , D. Kumar41 , P.R. Pujahari , N.R. Saha , A. Sharma , A.K. Sikdar
S. Verma

,
,

, B.C. Choudhary

, A. Kumar

Saha Institute of Nuclear Physics, HBNI, Kolkata, India
S. Baradia , S. Barman40 , S. Bhattacharya , S. Dutta , S. Dutta, S. Sarkar

Tata Institute of Fundamental Research-A, Mumbai, India
S. Dugad, M. Kumar , G.B. Mohanty , P. Suryadevara
Tata Institute of Fundamental Research-B, Mumbai, India

## PDF page 36

34
A. Bala , S. Banerjee , R.M. Chatterjee, R.K. Dewanjee42 , M. Guchait , Sh. Jain
A. Jaiswal, S. Kumar , G. Majumder , K. Mazumdar , S. Parolia , A. Thachayath

,

National Institute of Science Education and Research, An OCC of Homi Bhabha National
Institute, Bhubaneswar, Odisha, India
S. Bahinipati43 , C. Kar , D. Maity44 , P. Mal , T. Mishra , V.K. Muraleedharan Nair Bindhu44 , K. Naskar44 , A. Nayak44 , P. Sadangi, S.K. Swain , S. Varghese44 ,
D. Vats44
Indian Institute of Science Education and Research (IISER), Pune, India
S. Acharya45 , A. Alpana , S. Dube , B. Gomber45 , B. Kansal , A. Laha
S. Sharma , K.Y. Vaish

, B. Sahu45

,

INFN Sezione di Baria , Università di Barib , Politecnico di Baric , Bari, Italy
M. Abbresciaa,b , R. Alya,c,50 , A. Colaleoa,b , D. Creanzaa,c , B. D’Anzia,b
N. De Filippisa,c , M. De Palmaa,b , A. Di Florioa,c , W. Elmetenaweea,b,50
L. Fiorea , G. Iasellia,c , M. Loukaa,b , G. Maggia,c , M. Maggia , I. Margjekaa,b
V. Mastrapasquaa,b , S. Mya,b , S. Nuzzoa,b , A. Pellecchiaa,b , A. Pompilia,b
G. Pugliesea,c , R. Radognaa , G. Ramirez-Sancheza,c , D. Ramosa , A. Ranieria
L. Silvestrisa , F.M. Simonea,b , Ü. Sözbilira , A. Stamerraa , R. Vendittia
P. Verwilligena , A. Zazaa,b

,
,
,
,
,
,

INFN Sezione di Bolognaa , Università di Bolognab , Bologna, Italy
G. Abbiendia , C. Battilanaa,b , D. Bonacorsia,b , L. Borgonovia , R. Campaninia,b
P. Capiluppia,b , A. Castroa,b , F.R. Cavalloa , M. Cuffiania,b , G.M. Dallavallea
T. Diotalevia,b , F. Fabbria , A. Fanfania,b , D. Fasanellaa,b , L. Giommia,b
C. Grandia , L. Guiduccia,b , S. Lo Meoa,51 , L. Lunertia,b , S. Marcellinia
G. Masettia , F.L. Navarriaa,b , A. Perrottaa , F. Primaveraa,b , A.M. Rossia,b
T. Rovellia,b , G.P. Sirolia,b

,
,
,
,
,

Isfahan University of Technology, Isfahan, Iran
H. Bakhshiansohi46 , E. Khazaie47 , M. Zeinali48
Institute for Research in Fundamental Sciences (IPM), Tehran, Iran
S. Chenarani49 , S.M. Etesami , M. Khakzad , M. Mohammadi Najafabadi
University College Dublin, Dublin, Ireland
M. Grunewald

INFN Sezione di Cataniaa , Università di Cataniab , Catania, Italy
S. Costaa,b,52 , A. Di Mattiaa , R. Potenzaa,b , A. Tricomia,b,52 , C. Tuvea,b
INFN Sezione di Firenzea , Università di Firenzeb , Firenze, Italy
P. Assiourasa , G. Barbaglia , G. Bardellia,b , B. Camaiania,b , A. Cassesea
R. Ceccarellia , V. Ciullia,b , C. Civininia , R. D’Alessandroa,b , E. Focardia,b
T. Kelloa , G. Latinoa,b , P. Lenzia,b , M. Lizzoa , M. Meschinia , S. Paolettia
A. Papanastassioua,b , G. Sguazzonia , L. Viliania
INFN Laboratori Nazionali di Frascati, Frascati, Italy
L. Benussi , S. Bianco , S. Meola53 , D. Piccolo
INFN Sezione di Genovaa , Università di Genovab , Genova, Italy
P. Chatagnona , F. Ferroa , E. Robuttia , S. Tosia,b
INFN Sezione di Milano-Bicoccaa , Università di Milano-Bicoccab , Milano, Italy

,
,
,

## PDF page 37

35
A. Benagliaa , G. Boldrinia,b , F. Brivioa , F. Cetorellia , F. De Guioa,b
M.E. Dinardoa,b , P. Dinia , S. Gennaia , R. Gerosaa,b , A. Ghezzia,b , P. Govonia,b
L. Guzzia , M.T. Lucchinia,b , M. Malbertia , S. Malvezzia , A. Massironia
D. Menascea , L. Moronia , M. Paganonia,b , S. Palluottoa,b , D. Pedrinia
B.S. Pinolinia , G. Pizzatia,b , S. Ragazzia,b , T. Tabarelli de Fatisa,b , D. Zuoloa

,
,
,
,

INFN Sezione di Napolia , Università di Napoli ’Federico II’b , Napoli, Italy; Università della
Basilicatac , Potenza, Italy; Scuola Superiore Meridionale (SSM)d , Napoli, Italy
S. Buontempoa , A. Cagnottaa,b , F. Carnevalia,b , N. Cavalloa,c , F. Fabozzia,c ,
A.O.M. Iorioa,b , L. Listaa,b,54 , P. Paoluccia,32 , B. Rossia , C. Sciaccaa,b
INFN Sezione di Padovaa , Università di Padovab , Padova, Italy; Università di Trentoc ,
Trento, Italy
R. Ardinoa , P. Azzia , N. Bacchettaa,55 , D. Biselloa,b , P. Bortignona , G. Bortolatoa,b ,
A. Bragagnoloa,b , A.C.M. Bullaa , P. Checchiaa , T. Dorigoa , F. Gasparinia,b ,
U. Gasparinia,b , E. Lusiania , M. Margonia,b , F. Marinia , A.T. Meneguzzoa,b ,
M. Migliorinia,b , M. Passaseoa , J. Pazzinia,b , P. Ronchesea,b , R. Rossina,b ,
F. Simonettoa,b , G. Stronga , M. Tosia,b , A. Triossia,b , S. Venturaa , H. Yarara,b ,
M. Zanettia,b , P. Zottoa,b , A. Zucchettaa,b , G. Zumerlea,b
INFN Sezione di Paviaa , Università di Paviab , Pavia, Italy
S. Abu Zeida,56 , C. Aimèa,b , A. Braghieria , S. Calzaferria , D. Fiorinaa
P. Montagnaa,b , V. Rea , C. Riccardia,b , P. Salvinia , I. Vaia,b , P. Vituloa,b

,

INFN Sezione di Perugiaa , Università di Perugiab , Perugia, Italy
S. Ajmala,b , G.M. Bileia , D. Ciangottinia,b , L. Fanòa,b , M. Magherinia,b
G. Mantovania,b , V. Mariania,b , M. Menichellia , F. Moscatellia,57 , A. Rossia,b
A. Santocchiaa,b , D. Spigaa , T. Tedeschia,b

,
,

INFN Sezione di Pisaa , Università di Pisab , Scuola Normale Superiore di Pisac , Pisa, Italy;
Università di Sienad , Siena, Italy
P. Asenova,b , P. Azzurria , G. Bagliesia , R. Bhattacharyaa , L. Bianchinia,b ,
T. Boccalia , E. Bossinia , D. Bruschinia,c , R. Castaldia , M.A. Cioccia,b ,
M. Cipriania,b , V. D’Amantea,d , R. Dell’Orsoa , S. Donatoa , A. Giassia ,
F. Ligabuea,c , D. Matos Figueiredoa , A. Messineoa,b , M. Musicha,b , F. Pallaa ,
A. Rizzia,b , G. Rolandia,c , S. Roy Chowdhurya , T. Sarkara , A. Scribanoa ,
P. Spagnoloa , R. Tenchinia , G. Tonellia,b , N. Turinia,d , F. Vasellia,c , A. Venturia ,
P.G. Verdinia
INFN Sezione di Romaa , Sapienza Università di Romab , Roma, Italy
C. Baldenegro Barreraa,b , P. Barriaa , C. Basilea,b , M. Campanaa,b , F. Cavallaria
L. Cunqueiro Mendeza,b , D. Del Rea,b , E. Di Marcoa , M. Diemoza , F. Erricoa,b
E. Longoa,b , P. Meridiania , J. Mijuskovica,b , G. Organtinia,b , F. Pandolfia
R. Paramattia,b , C. Quarantaa,b , S. Rahatloua,b , C. Rovellia , F. Santanastasioa,b
L. Soffia

,
,
,
,

INFN Sezione di Torinoa , Università di Torinob , Torino, Italy; Università del Piemonte
Orientalec , Novara, Italy
N. Amapanea,b , R. Arcidiaconoa,c , S. Argiroa,b , M. Arneodoa,c , N. Bartosika ,
R. Bellana,b , A. Belloraa,b , C. Biinoa , C. Borcaa,b , N. Cartigliaa , M. Costaa,b ,
R. Covarellia,b , N. Demariaa , L. Fincoa , M. Grippoa,b , B. Kiania,b , F. Leggera ,
F. Luongoa,b , C. Mariottia , L. Markovica,b , S. Masellia , A. Meccaa,b ,
E. Migliorea,b , M. Montenoa , R. Mulargiaa , M.M. Obertinoa,b , G. Ortonaa ,

## PDF page 38

36
L. Pachera,b , N. Pastronea , M. Pelliccionia , M. Ruspaa,c , F. Sivieroa,b
V. Solaa,b , A. Solanoa,b , A. Staianoa , C. Tarriconea,b , D. Trocinoa , G. Umoreta,b
E. Vlasova,b , R. Whitea
INFN Sezione di Triestea , Università di Triesteb , Trieste, Italy
S. Belfortea , V. Candelisea,b , M. Casarsaa , F. Cossuttia
G. Della Riccaa,b

,
,

K. De Leoa

,

Kyungpook National University, Daegu, Korea
S. Dogra , J. Hong , C. Huh , B. Kim , D.H. Kim , J. Kim, H. Lee, S.W. Lee
C.S. Moon , Y.D. Oh , M.S. Ryu , S. Sekmen , Y.C. Yang

,

,

Department of Mathematics and Physics - GWNU, Gangneung, Korea
M.S. Kim
Chonnam National University, Institute for Universe and Elementary Particles, Kwangju,
Korea
G. Bak , P. Gwak , H. Kim , D.H. Moon
Hanyang University, Seoul, Korea
E. Asilar , D. Kim , T.J. Kim , J.A. Merlin
Korea University, Seoul, Korea
S. Choi , S. Han, B. Hong , K. Lee, K.S. Lee

, S. Lee

, J. Park, S.K. Park, J. Yoo

Kyung Hee University, Department of Physics, Seoul, Korea
J. Goh , S. Yang
Sejong University, Seoul, Korea
H. S. Kim , Y. Kim, S. Lee
Seoul National University, Seoul, Korea
J. Almond, J.H. Bhyun, J. Choi , W. Jun , J. Kim , S. Ko , H. Kwon
J. Lee , B.H. Oh , S.B. Oh , H. Seo , U.K. Yang, I. Yoon

, H. Lee

, J. Lee

University of Seoul, Seoul, Korea
W. Jang , D.Y. Kang, Y. Kang , S. Kim
I.J. Watson

, I.C. Park

, Y. Roh,

, B. Ko, J.S.H. Lee

, Y. Lee

,

Yonsei University, Department of Physics, Seoul, Korea
S. Ha , H.D. Yoo
Sungkyunkwan University, Suwon, Korea
M. Choi , M.R. Kim , H. Lee, Y. Lee , I. Yu
College of Engineering and Technology, American University of the Middle East (AUM),
Dasman, Kuwait
T. Beyrouthy
Riga Technical University, Riga, Latvia
K. Dreimanis , A. Gaile , G. Pikurs, A. Potrebko

, M. Seidel

University of Latvia (LU), Riga, Latvia
N.R. Strautnieks
Vilnius University, Vilnius, Lithuania
M. Ambrozas , A. Juodagalvis , A. Rinkevicius

, G. Tamulaitis

## PDF page 39

37
National Centre for Particle Physics, Universiti Malaya, Kuala Lumpur, Malaysia
N. Bin Norjoharuddeen , I. Yusuff58 , Z. Zolkapli
Universidad de Sonora (UNISON), Hermosillo, Mexico
J.F. Benitez , A. Castaneda Hernandez , H.A. Encinas Acosta, L.G. Gallegos Marı́ñez,
M. León Coello , J.A. Murillo Quijada , A. Sehrawat , L. Valencia Palomo
Centro de Investigacion y de Estudios Avanzados del IPN, Mexico City, Mexico
G. Ayala , H. Castilla-Valdez , H. Crotte Ledesma, E. De La Cruz-Burelo , I. HerediaDe La Cruz59 , R. Lopez-Fernandez , C.A. Mondragon Herrera, A. Sánchez Hernández
Universidad Iberoamericana, Mexico City, Mexico
C. Oropeza Barrera , M. Ramı́rez Garcı́a
Benemerita Universidad Autonoma de Puebla, Puebla, Mexico
I. Bautista , I. Pedraza , H.A. Salazar Ibarguen , C. Uribe Estrada
University of Montenegro, Podgorica, Montenegro
I. Bubanja, N. Raicevic
University of Canterbury, Christchurch, New Zealand
P.H. Butler
National Centre for Physics, Quaid-I-Azam University, Islamabad, Pakistan
A. Ahmad , M.I. Asghar, A. Awais , M.I.M. Awan, H.R. Hoorani , W.A. Khan
AGH University of Krakow, Faculty of Computer Science, Electronics and Telecommunications, Krakow, Poland
V. Avati, L. Grzanka , M. Malawski
National Centre for Nuclear Research, Swierk, Poland
H. Bialkowska , M. Bluj , B. Boimska , M. Górski
P. Zalewski

, M. Kazana

, M. Szleper

,

Institute of Experimental Physics, Faculty of Physics, University of Warsaw, Warsaw, Poland
K. Bunkowski , K. Doroba , A. Kalinowski , M. Konecki , J. Krolikowski ,
A. Muhammad
Warsaw University of Technology, Warsaw, Poland
K. Pozniak , W. Zabolotny
Laboratório de Instrumentação e Fı́sica Experimental de Partı́culas, Lisboa, Portugal
M. Araujo , D. Bastos , C. Beirão Da Cruz E Silva , A. Boletti , M. Bozzo
T. Camporesi , G. Da Molin , P. Faccioli , M. Gallinaro , J. Hollar , N. Leonardo
T. Niknejad , A. Petrilli , M. Pisano , J. Seixas , J. Varela , J.W. Wulff

,
,

Faculty of Physics, University of Belgrade, Belgrade, Serbia
P. Adzic , P. Milenovic
VINCA Institute of Nuclear Sciences, University of Belgrade, Belgrade, Serbia
M. Dordevic , J. Milosevic , V. Rekovic
Centro de Investigaciones Energéticas Medioambientales y Tecnológicas (CIEMAT),
Madrid, Spain
M. Aguilar-Benitez, J. Alcaraz Maestre , Cristina F. Bedoya , Oliver M. Carretero ,
M. Cepeda , M. Cerrada , N. Colino , B. De La Cruz , A. Delgado Peris ,
A. Escalante Del Valle , D. Fernández Del Val , J.P. Fernández Ramos , J. Flix ,

## PDF page 40

38
M.C. Fouz , O. Gonzalez Lopez , S. Goy Lopez , J.M. Hernandez , M.I. Josa ,
D. Moran , C. M. Morcillo Perez , Á. Navarro Tobar , C. Perez Dengra , A. PérezCalero Yzquierdo , J. Puerta Pelayo , I. Redondo , D.D. Redondo Ferrero , L. Romero,
S. Sánchez Navas , L. Urda Gómez , J. Vazquez Escobar , C. Willmott
Universidad Autónoma de Madrid, Madrid, Spain
J.F. de Trocóniz
Universidad de Oviedo, Instituto Universitario de Ciencias y Tecnologı́as Espaciales de
Asturias (ICTEA), Oviedo, Spain
B. Alvarez Gonzalez , J. Cuevas , J. Fernandez Menendez , S. Folgueras , I. Gonzalez Caballero , J.R. González Fernández , P. Leguina , E. Palencia Cortezon ,
C. Ramón Álvarez , V. Rodrı́guez Bouza , A. Soto Rodrı́guez , A. Trapote ,
C. Vico Villalba , P. Vischia
Instituto de Fı́sica de Cantabria (IFCA), CSIC-Universidad de Cantabria, Santander, Spain
S. Bhowmik , S. Blanco Fernández , J.A. Brochero Cifuentes , I.J. Cabrillo ,
A. Calderon , J. Duarte Campderros , M. Fernandez , G. Gomez , C. Lasaosa Garcı́a ,
R. Lopez Ruiz, C. Martinez Rivero , P. Martinez Ruiz del Arbol , F. Matorras ,
P. Matorras Cuevas , E. Navarrete Ramos , J. Piedra Gomez , L. Scodellaro , I. Vila ,
J.M. Vizan Garcia
University of Colombo, Colombo, Sri Lanka
M.K. Jayananda , B. Kailasapathy60 , D.U.J. Sonnadara

, D.D.C. Wickramarathna

University of Ruhuna, Department of Physics, Matara, Sri Lanka
W.G.D. Dharmaratna61 , K. Liyanage , N. Perera , N. Wickramage
CERN, European Organization for Nuclear Research, Geneva, Switzerland
D. Abbaneo , C. Amendola , E. Auffray , G. Auzinger , J. Baechler, D. Barney
A. Bermúdez Martı́nez , M. Bianco , B. Bilin , A.A. Bin Anuar , A. Bocci , C. Botta
E. Brondolin , C. Caillol , G. Cerminara , N. Chernyavskaya , D. d’Enterria
A. Dabrowski , A. David , A. De Roeck , M.M. Defranchis , M. Deile , M. Dobson
L. Forthomme , G. Franzoni , W. Funk , S. Giani, D. Gigi, K. Gill , F. Glege
L. Gouskos , M. Haranko , J. Hegeman , B. Huber, V. Innocente , T. James
P. Janot , O. Kaluzinska , S. Laurila , P. Lecoq , E. Leutgeb , C. Lourenço
L. Malgeri , M. Mannelli , A.C. Marini , M. Matthewman, F. Meijers , S. Mersi
E. Meschi , V. Milosevic , F. Monti , F. Moortgat , M. Mulders , I. Neutelings
S. Orfanelli, F. Pantaleo , G. Petrucciani , A. Pfeiffer , M. Pierini , D. Piparo , H. Qu
D. Rabady , M. Rovere , H. Sakulin , S. Scarfi , C. Schwick, M. Selvaggi , A. Sharma
K. Shchelina , P. Silva , P. Sphicas62 , A.G. Stahl Leiton , A. Steen , S. Summers
D. Treille , P. Tropea , A. Tsirou, D. Walter , J. Wanczyk63 , J. Wang, S. Wuchterl
P. Zehetner , P. Zejdl , W.D. Zeuner

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
,
,

Paul Scherrer Institut, Villigen, Switzerland
T. Bevilacqua64 , L. Caminada64 , A. Ebrahimi , W. Erdmann , R. Horisberger
Q. Ingram , H.C. Kaestli , D. Kotlinski , C. Lange , M. Missiroli64 , L. Noehte64
T. Rohe

,
,

ETH Zurich - Institute for Particle Physics and Astrophysics (IPA), Zurich, Switzerland
T.K. Aarrestad , K. Androsov63 , M. Backhaus , G. Bonomelli, A. Calandri , C. Cazzaniga , K. Datta , A. De Cosa , G. Dissertori , M. Dittmar, M. Donegà , F. Eble ,
M. Galli , K. Gedia , F. Glessgen , C. Grab , N. Härringer , T.G. Harte, D. Hits ,

## PDF page 41

39
W. Lustermann , A.-M. Lyon , R.A. Manzoni , M. Marchegiani , L. Marchese
C. Martin Perez , A. Mascellani63 , F. Nessi-Tedaldi , F. Pauss , V. Perovic
S. Pigazzini , C. Reissel , T. Reitenspiess , B. Ristic , F. Riti , R. Seidita
J. Steggemann63 , D. Valsecchi , R. Wallny
Universität Zürich, Zurich, Switzerland
C. Amsler65 , P. Bärtschi , M.F. Canelli , K. Cormier , J.K. Heikkilä , M. Huwiler
W. Jin , A. Jofrehei , B. Kilminster , S. Leontsinis , S.P. Liechti , A. Macchiolo
P. Meiring , U. Molinatti , A. Reimers , P. Robmann, S. Sanchez Cruz , M. Senger
F. Stäger , Y. Takahashi , R. Tramontano
National Central University, Chung-Li, Taiwan
C. Adloff66 , D. Bhowmik, C.M. Kuo, W. Lin, P.K. Rout

, P.C. Tiwari41

,
,
,

,
,
,

, S.S. Yu

National Taiwan University (NTU), Taipei, Taiwan
L. Ceard, Y. Chao , K.F. Chen , P.s. Chen, Z.g. Chen, A. De Iorio , W.-S. Hou , T.h. Hsu,
Y.w. Kao, S. Karmakar , R. Khurana, G. Kole , Y.y. Li , R.-S. Lu , E. Paganis , X.f. Su ,
J. Thomas-Wilsker , L.s. Tsai, H.y. Wu, E. Yazgan
High Energy Physics Research Unit, Department of Physics, Faculty of Science,
Chulalongkorn University, Bangkok, Thailand
C. Asawatangtrakuldee , N. Srimanobhas , V. Wachirapusitanand
Çukurova University, Physics Department, Science and Art Faculty, Adana, Turkey
D. Agyel , F. Boran , Z.S. Demiroglu , F. Dolek , I. Dumanoglu67 , E. Eskut
Y. Guler68 , E. Gurpinar Guler68 , C. Isik , O. Kara, A. Kayis Topaksu , U. Kiminsu
G. Onengut , K. Ozdemir69 , A. Polatoz , B. Tali70 , U.G. Tok , S. Turkcapar
E. Uslan , I.S. Zorbakir

,
,
,

Middle East Technical University, Physics Department, Ankara, Turkey
G. Sokmen, M. Yalvac71
Bogazici University, Istanbul, Turkey
B. Akgun , I.O. Atakisi , E. Gülmez

, M. Kaya72

, O. Kaya73

Istanbul Technical University, Istanbul, Turkey
A. Cakir , K. Cankocak67,75 , G.G. Dincer , Y. Komurcu

, S. Tekten74

, S. Sen76

Istanbul University, Istanbul, Turkey
O. Aydilek25 , S. Cerci70 , V. Epshteyn , B. Hacisahinoglu , I. Hos77
S. Ozkorucuklu , O. Potok , H. Sert , C. Simsek , C. Zorbilmez

, B. Kaynak

,

Yildiz Technical University, Istanbul, Turkey
B. Isildak78 , D. Sunar Cerci70
Institute for Scintillation Materials of National Academy of Science of Ukraine, Kharkiv,
Ukraine
A. Boyaryntsev , B. Grynyov
National Science Centre, Kharkiv Institute of Physics and Technology, Kharkiv, Ukraine
L. Levchuk
University of Bristol, Bristol, United Kingdom
D. Anthony , J.J. Brooke , A. Bundock , F. Bury , E. Clement , D. Cussans
H. Flacher , M. Glowacki, J. Goldstein , H.F. Heath , M.-L. Holmberg , L. Kreczko
S. Paramesvaran , L. Robertshaw, S. Seif El Nasr-Storey, V.J. Smith , N. Stylianou79

,
,
,

## PDF page 42

40
K. Walkingshaw Pass
Rutherford Appleton Laboratory, Didcot, United Kingdom
A.H. Ball, K.W. Bell , A. Belyaev80 , C. Brew , R.M. Brown , D.J.A. Cockerill ,
C. Cooke , K.V. Ellis, K. Harder , S. Harper , J. Linacre , K. Manolopoulos,
D.M. Newbold , E. Olaiya, D. Petyt , T. Reis , A.R. Sahasransu , G. Salvi , T. Schuh,
C.H. Shepherd-Themistocleous , I.R. Tomalin , T. Williams
Imperial College, London, United Kingdom
R. Bainbridge , P. Bloch , C.E. Brown , O. Buchmuller, V. Cacchio, C.A. Carrillo Montoya , G.S. Chahal81 , D. Colling , J.S. Dancu, I. Das , P. Dauncey , G. Davies ,
J. Davies, M. Della Negra , S. Fayer, G. Fedi , G. Hall , M.H. Hassanshahi , A. Howard,
G. Iles , M. Knight , J. Langford , J. León Holgado , L. Lyons , A.-M. Magnan ,
S. Malik, M. Mieskolainen , J. Nash82 , M. Pesaresi , B.C. Radburn-Smith , A. Richards,
A. Rose , K. Savva, C. Seez , R. Shukla , A. Tapper , K. Uchida , G.P. Uttley ,
L.H. Vage, T. Virdee32 , M. Vojinovic , N. Wardle , D. Winterbottom
Brunel University, Uxbridge, United Kingdom
K. Coldham, J.E. Cole , A. Khan, P. Kyberd , I.D. Reid
Baylor University, Waco, Texas, USA
S. Abdullin , A. Brinkerhoff , B. Caraway
J. Hiltbrand , B. McMaster , M. Saunders

, E. Collins , J. Dittmann , K. Hatakeyama
, S. Sawant , C. Sutantawibul , J. Wilson

Catholic University of America, Washington, DC, USA
R. Bartek , A. Dominguez , C. Huerta Escamilla, A.E. Simsek
gas Hernandez
The University of Alabama, Tuscaloosa, Alabama, USA
B. Bam , R. Chudasama , S.I. Cooper , S.V. Gleyzer
E. Usai , R. Yi

, R. Uniyal

,

, A.M. Var-

, P. Rumerio83

,

Boston University, Boston, Massachusetts, USA
A. Akpinar , D. Arcaro , C. Cosby , Z. Demiragli , C. Erice , C. Fangmeier
C. Fernandez Madrazo , E. Fontanesi , D. Gastler , F. Golf , S. Jeon , I. Reed
J. Rohlf , K. Salyer , D. Sperka , D. Spitzbart , I. Suarez , A. Tsatsos , S. Yuan
A.G. Zecchinelli

,
,
,

Brown University, Providence, Rhode Island, USA
G. Benelli , X. Coubez27 , D. Cutts , M. Hadley , U. Heintz , J.M. Hogan84 , T. Kwon
G. Landsberg , K.T. Lau , D. Li , J. Luo , S. Mondal , M. Narain† , N. Pervan
S. Sagir85 , F. Simpson , M. Stamenkovic , X. Yan , W. Zhang

,
,

University of California, Davis, Davis, California, USA
S.
Abbott ,
J.
Bonilla ,
C.
Brainerd ,
R.
Breedon ,
H.
Cai
M. Calderon De La Barca Sanchez , M. Chertok , M. Citron , J. Conway , P.T. Cox
R. Erbacher , F. Jensen , O. Kukral , G. Mocellin , M. Mulhearn , D. Pellett
W. Wei , Y. Yao , F. Zhang

,
,
,

University of California, Los Angeles, California, USA
M. Bachtis , R. Cousins , A. Datta , G. Flores Avila, J. Hauser , M. Ignatenko
M.A. Iqbal , T. Lam , E. Manca , A. Nunez Del Prado, D. Saltzberg , V. Valuev

,

, C.U. Perez

University of California, Riverside, Riverside, California, USA
R. Clare , J.W. Gary , M. Gordon, G. Hanson , W. Si , S. Wimpenny†

## PDF page 43

41
University of California, San Diego, La Jolla, California, USA
J.G. Branson , S. Cittolin , S. Cooperstein , D. Diaz , J. Duarte , L. Giannini
J. Guiang , R. Kansal , V. Krutelyov , R. Lee , J. Letts , M. Masciovecchio
F. Mokhtar , S. Mukherjee , M. Pieri , M. Quinnan , B.V. Sathia Narayanan
V. Sharma , M. Tadel , E. Vourliotis , F. Würthwein , Y. Xiang , A. Yagil

,
,
,

University of California, Santa Barbara - Department of Physics, Santa Barbara, California,
USA
A. Barzdukas , L. Brennan , C. Campagnari , J. Incandela , J. Kim , A.J. Li ,
P. Masterson , H. Mei , J. Richman , U. Sarica , R. Schmitz , F. Setti , J. Sheplock ,
D. Stuart , T.Á. Vámi , S. Wang
California Institute of Technology, Pasadena, California, USA
A. Bornheim , O. Cerri, A. Latorre, J. Mao , H.B. Newman
M. Spiropulu , J.R. Vlimant , C. Wang , S. Xie , R.Y. Zhu

, G. Reales Gutiérrez,

Carnegie Mellon University, Pittsburgh, Pennsylvania, USA
J. Alison , S. An , M.B. Andrews , P. Bryant , M. Cremonesi, V. Dutta , T. Ferguson
A. Harilal , C. Liu , T. Mudholkar , S. Murthy , P. Palit , M. Paulini , A. Roberts
A. Sanchez , W. Terrill

,
,

University of Colorado Boulder, Boulder, Colorado, USA
J.P. Cumalat , W.T. Ford , A. Hart , A. Hassani , G. Karathanasis , N. Manganelli
A. Perloff , C. Savard , N. Schonbeck , K. Stenson , K.A. Ulmer , S.R. Wagner
N. Zipper

,
,

Cornell University, Ithaca, New York, USA
J. Alexander , S. Bright-Thonney , X. Chen , D.J. Cranshaw , J. Fan , X. Fan
S. Hogan , P. Kotamnives, J. Monroy , M. Oshiro , J.R. Patterson , J. Reichert
M. Reid , A. Ryd , J. Thom , P. Wittich , R. Zou

,
,

Fermi National Accelerator Laboratory, Batavia, Illinois, USA
M. Albrow , M. Alyari , O. Amram , G. Apollinari , A. Apresyan , L.A.T. Bauerdick ,
D. Berry , J. Berryhill , P.C. Bhat , K. Burkett , J.N. Butler , A. Canepa , G.B. Cerati ,
H.W.K. Cheung , F. Chlebana , G. Cummings , J. Dickinson , I. Dutta , V.D. Elvira ,
Y. Feng , J. Freeman , A. Gandrakota , Z. Gecse , L. Gray , D. Green, A. Grummer ,
S. Grünendahl , D. Guerrero , O. Gutsche , R.M. Harris , R. Heller , T.C. Herwig ,
J. Hirschauer , L. Horyn , B. Jayatilaka , S. Jindariani , M. Johnson , U. Joshi ,
T. Klijnsma , B. Klima , K.H.M. Kwok , S. Lammel , D. Lincoln , R. Lipton , T. Liu ,
C. Madrid , K. Maeshima , C. Mantilla , D. Mason , P. McBride , P. Merkel ,
S. Mrenna , S. Nahn , J. Ngadiuba , D. Noonan , V. Papadimitriou , N. Pastika ,
K. Pedro , C. Pena86 , F. Ravera , A. Reinsvold Hall87 , L. Ristori , E. SextonKennedy , N. Smith , A. Soha , L. Spiegel , S. Stoynev , J. Strait , L. Taylor ,
S. Tkaczyk , N.V. Tran , L. Uplegger , E.W. Vaandering , A. Whitbeck , I. Zoi
University of Florida, Gainesville, Florida, USA
C. Aruta , P. Avery , D. Bourilkov , L. Cadamuro , P. Chang , V. Cherepanov
R.D. Field, E. Koenig , M. Kolosova , J. Konigsberg , A. Korytov , K. Matchev
N. Menendez , G. Mitselmakher , K. Mohrman , A. Muthirakalayil Madhu
N. Rawal , D. Rosenzweig , S. Rosenzweig , J. Wang
Florida State University, Tallahassee, Florida, USA
T. Adams , A. Al Kadhim , A. Askew , S. Bower

, R. Habibullah

, V. Hagopian

,
,
,

,

## PDF page 44

42
R. Hashmi , R.S. Kim , S. Kim , T. Kolberg
M. Wulansatiti , R. Yohay , J. Zhang

, G. Martinez, H. Prosper

Florida Institute of Technology, Melbourne, Florida, USA
B. Alsufyani, M.M. Baarmand , S. Butalla , S. Das , T. Elkafrawy56
R. Kumar Verma , M. Rahmani, E. Yanes

, P.R. Prova,

, M. Hohlmann

,

University of Illinois Chicago, Chicago, USA, Chicago, USA
M.R. Adams , A. Baty , C. Bennett, R. Cavanaugh , R. Escobar Franco , O. Evdokimov , C.E. Gerber , M. Hawksworth, A. Hingrajiya, D.J. Hofman , J.h. Lee ,
D. S. Lemos , A.H. Merrit , C. Mills , S. Nanda , G. Oh , B. Ozek , D. Pilipovic ,
R. Pradhan , E. Prifti, T. Roy , S. Rudrabhatla , M.B. Tonjes , N. Varelas , Z. Ye ,
J. Yoo
The University of Iowa, Iowa City, Iowa, USA
M. Alhusseini , D. Blend, K. Dilsiz88 , L. Emediato , G. Karaman , O.K. Köseyan , J.P. Merlo, A. Mestvirishvili89 , J. Nachtman , O. Neogi, H. Ogul90 , Y. Onel , A. Penzo ,
C. Snyder, E. Tiras91
Johns Hopkins University, Baltimore, Maryland, USA
B. Blumenfeld , L. Corcodilos , J. Davis , A.V. Gritsan , L. Kang
P. Maksimovic , M. Roguljic , J. Roskes , S. Sekhar , M. Swartz

, S. Kyriacou

,

The University of Kansas, Lawrence, Kansas, USA
A. Abreu , L.F. Alcerro Alcerro , J. Anguiano , P. Baringer , A. Bean , Z. Flowers
D. Grove , J. King , G. Krintiras , M. Lazarovits , C. Le Mahieu , J. Marquez
N. Minafra , M. Murray , M. Nickel , M. Pitt , S. Popescu92 , C. Rogan , C. Royon
R. Salvatico , S. Sanders , C. Smith , Q. Wang , G. Wilson

,
,
,

Kansas State University, Manhattan, Kansas, USA
B. Allmond , A. Ivanov , K. Kaadze , A. Kalogeropoulos
J. Natoli , D. Roy , G. Sorrentino

,

, D. Kim, Y. Maravin

Lawrence Livermore National Laboratory, Livermore, California, USA
F. Rebassoo , D. Wright
University of Maryland, College Park, Maryland, USA
A. Baden , A. Belloni , Y.M. Chen , S.C. Eno , N.J. Hadley , S. Jabeen
R.G. Kellogg , T. Koeth , Y. Lai , S. Lascio , A.C. Mignerey , S. Nabili , C. Palmer
C. Papageorgakis , M.M. Paranjpe, L. Wang

,
,

Massachusetts Institute of Technology, Cambridge, Massachusetts, USA
J. Bendavid , I.A. Cali , M. D’Alfonso , J. Eysermans , C. Freer , G. Gomez-Ceballos
M. Goncharov, G. Grosso, P. Harris, D. Hoang, D. Kovalskyi , J. Krupa , L. Lavezzo
Y.-J. Lee , K. Long , A. Novak , C. Paus , D. Rankin , C. Roland , G. Roland
S. Rothman , G.S.F. Stephans , Z. Wang , B. Wyslouch , T. J. Yang

,
,
,

University of Minnesota, Minneapolis, Minnesota, USA
B. Crossman , B.M. Joshi , C. Kapsiak , M. Krohn , D. Mahon , J. Mans
B. Marzocchi , S. Pandey , M. Revering , R. Rusack , R. Saradhy , N. Schroeder
N. Strobbe , M.A. Wadud

,
,

University of Mississippi, Oxford, Mississippi, USA
L.M. Cremaldi

## PDF page 45

43
University of Nebraska-Lincoln, Lincoln, Nebraska, USA
K. Bloom , D.R. Claes , G. Haza , J. Hossain , C. Joo , I. Kravchenko
W. Tabb , A. Vagnerini , A. Wightman , F. Yan , D. Yu

, J.E. Siado

,

State University of New York at Buffalo, Buffalo, New York, USA
H. Bandyopadhyay , L. Hay , I. Iashvili , A. Kharchilava , M. Morris
S. Rappoccio , H. Rejeb Sfar, A. Williams

, D. Nguyen

,

Northeastern University, Boston, Massachusetts, USA
G. Alverson , E. Barberis , J. Dervan, Y. Haddad , Y. Han , A. Krishna , J. Li
M. Lu , G. Madigan , R. Mccarthy , D.M. Morse , V. Nguyen , T. Orimoto
A. Parker , L. Skinnari , B. Wang , D. Wood

,
,

Northwestern University, Evanston, Illinois, USA
S. Bhattacharya , J. Bueghly, Z. Chen , S. Dittmer , K.A. Hahn
D.G. Monk , M.H. Schmitt , A. Taliercio , M. Velasco

, Y. Miao

,

University of Notre Dame, Notre Dame, Indiana, USA
G. Agarwal , R. Band , R. Bucci, S. Castells , A. Das , R. Goldouzian , M. Hildreth
K.W. Ho , K. Hurtado Anampa , T. Ivanov , C. Jessop , K. Lannon , J. Lawrence
N. Loukas , L. Lutton , J. Mariano, N. Marinelli, I. Mcalister, T. McCauley , C. Mcgrady
C. Moore , Y. Musienko16 , H. Nelson , M. Osherson , A. Piccinelli , R. Ruchti
A. Townsend , Y. Wan, M. Wayne , H. Yockey, M. Zarucki , L. Zygala

,
,
,
,

The Ohio State University, Columbus, Ohio, USA
A. Basnet , B. Bylsma, M. Carrigan , L.S. Durkin
nelas , K. Wei, B.L. Winer , B. R. Yates

, C. Hill

, Y. Liu

, M. Joyce

, M. Nunez Or-

Princeton University, Princeton, New Jersey, USA
F.M. Addesa , H. Bouchamaoui , P. Das , G. Dezoort , P. Elmer , A. Frankenthal
B. Greenberg , N. Haubrich , G. Kopp , S. Kwan , D. Lange , A. Loeliger
D. Marlow , I. Ojalvo , J. Olsen , A. Shevelev , D. Stickland , C. Tully

,
,

University of Puerto Rico, Mayaguez, Puerto Rico, USA
S. Malik
Purdue University, West Lafayette, Indiana, USA
A.S. Bakshi , V.E. Barnes , S. Chandra , R. Chawla , A. Gu , L. Gutay, M. Jones
A.W. Jung , D. Kondratyev , A.M. Koshy, M. Liu , G. Negro , N. Neumeister
G. Paspalaki , S. Piperov , V. Scheurer, J.F. Schulte , M. Stojanovic , J. Thieman
A. K. Virdi , F. Wang , W. Xie

,
,
,

Purdue University Northwest, Hammond, Indiana, USA
J. Dolen , N. Parashar , A. Pathak
Rice University, Houston, Texas, USA
D. Acosta , T. Carnahan , K.M. Ecklund , P.J. Fernández Manteca , S. Freed, P. Gardner,
F.J.M. Geurts , W. Li , O. Miguel Colin , B.P. Padley , R. Redjimi, J. Rotter ,
E. Yigitbasi , Y. Zhang
University of Rochester, Rochester, New York, USA
A. Bodek , P. de Barbaro , R. Demina , J.L. Dulemba , A. Garcia-Bellido
O. Hindrichs , A. Khukhunaishvili , N. Parmar, P. Parygin93 , E. Popova93 , R. Taus
The Rockefeller University, New York, New York, USA

,

## PDF page 46

44
K. Goulianos
Rutgers, The State University of New Jersey, Piscataway, New Jersey, USA
B. Chiarito, J.P. Chou , S.V. Clark , D. Gadkari , Y. Gershtein , E. Halkiadakis
M. Heindl , C. Houghton , D. Jaroslawski , O. Karacheban30 , I. Laflotte , A. Lath
R. Montalvo, K. Nash, H. Routray , P. Saha , S. Salur , S. Schnetzer, S. Somalwar
R. Stone , S.A. Thayil , S. Thomas, J. Vora , H. Wang

,
,
,

University of Tennessee, Knoxville, Tennessee, USA
H. Acharya, D. Ally , A.G. Delannoy , S. Fiorendi , S. Higginbotham
A.R. Kanuganti , N. Karunarathna , L. Lee , E. Nibigira , S. Spanier

, T. Holmes

,

Texas A&M University, College Station, Texas, USA
D. Aebi , M. Ahmad , O. Bouhali94 , R. Eusebi , J. Gilmore , T. Huang
T. Kamon95 , H. Kim , S. Luo , R. Mueller , D. Overton , D. Rathjens , A. Safonov

,

Texas Tech University, Lubbock, Texas, USA
N. Akchurin , J. Damgov , V. Hegde , A. Hussain
S.W. Lee , A. Mankel , T. Peltola , I. Volobouev

, Y. Kazhykarim, K. Lamichhane

,

Vanderbilt University, Nashville, Tennessee, USA
E. Appelt , Y. Chen , S. Greene, A. Gurrola , W. Johns , R. Kunnawalkam Elayavalli
A. Melo , F. Romeo , P. Sheldon , S. Tuo , J. Velkovska , J. Viinikainen

,

University of Virginia, Charlottesville, Virginia, USA
B. Cardwell , B. Cox , J. Hakala , R. Hirosky
C.E. Perez Lara

, C. Neu

,

University of Wisconsin - Madison, Madison, Wisconsin, USA
A. Aravind, S. Banerjee , K. Black , T. Bose , S. Dasu , I. De Bruyn , P. Everaerts
C. Galloni, H. He , M. Herndon , A. Herve , C.K. Koraka , A. Lanaro, R. Loveless
J. Madhusudanan Sreekala , A. Mallampalli , A. Mohammadi , S. Mondal, G. Parida
L. Pétré , D. Pinna, A. Savin, V. Shang , V. Sharma , W.H. Smith , D. Teague, H.F. Tsoi
W. Vetens , A. Warden

,
,
,
,

, A. Ledovskoy

Wayne State University, Detroit, Michigan, USA
P.E. Karchin

Authors affiliated with an institute or an international laboratory covered by a cooperation
agreement with CERN
S. Afanasiev , V. Andreev , Yu. Andreev , T. Aushev , M. Azarkin , I. Azhgirey , A. Babaev , A. Belyaev , V. Blinov96 , E. Boos , V. Borshch , D. Budkouski , V. Bunichev , V. Chekhovsky, R. Chistov96 , M. Danilov96 , A. Dermenev ,
T. Dimova96 , D. Druzhkin97 , M. Dubinin86 , L. Dudko , A. Ershov , G. Gavrilov ,
V. Gavrilov , S. Gninenko , V. Golovtcov , N. Golubev , I. Golutvin , I. Gorbunov ,
A. Gribushin , Y. Ivanov , V. Kachanov , V. Karjavine , A. Karneyeu , V. Kim96 ,
M. Kirakosyan, D. Kirpichnikov , M. Kirsanov , V. Klyukhin , O. Kodolova98 , D. Konstantinov , V. Korenkov , A. Kozyrev96 , N. Krasnikov , A. Lanev , P. Levchenko99 ,
N. Lychkovskaya , V. Makarenko , A. Malakhov , V. Matveev96 , V. Murzin ,
A. Nikitenko100,98 , S. Obraztsov , V. Oreshkin , V. Palichik , V. Perelygin , M. Perfilov,
S. Petrushanko , S. Polikarpov96 , V. Popov , O. Radchenko96 , R. Ryutin, M. Savina ,
V. Savrin , V. Shalaev , S. Shmatov , S. Shulha , Y. Skovpen96 , S. Slabospitskii ,
V. Smirnov , D. Sosnov , V. Sulimov , E. Tcherniaev , A. Terkulov , O. Teryaev ,
I. Tlisova , A. Toropin , L. Uvarov , A. Uzunian , A. Vorobyev† , N. Voytishin ,

## PDF page 47

45
B.S. Yuldashev101 , A. Zarubin

, I. Zhizhin

, A. Zhokin

†: Deceased
1 Also at Yerevan State University, Yerevan, Armenia
2 Also at TU Wien, Vienna, Austria
3 Also at Institute of Basic and Applied Sciences, Faculty of Engineering, Arab Academy for
Science, Technology and Maritime Transport, Alexandria, Egypt
4 Also at Ghent University, Ghent, Belgium
5 Also at Universidade Estadual de Campinas, Campinas, Brazil
6 Also at Federal University of Rio Grande do Sul, Porto Alegre, Brazil
7 Also at UFMS, Nova Andradina, Brazil
8 Also at Nanjing Normal University, Nanjing, China
9 Now at The University of Iowa, Iowa City, Iowa, USA
10 Also at University of Chinese Academy of Sciences, Beijing, China
11 Also at China Center of Advanced Science and Technology, Beijing, China
12 Also at University of Chinese Academy of Sciences, Beijing, China
13 Also at China Spallation Neutron Source, Guangdong, China
14 Now at Henan Normal University, Xinxiang, China
15 Also at Université Libre de Bruxelles, Bruxelles, Belgium
16 Also at an institute or an international laboratory covered by a cooperation agreement with
CERN
17 Also at Cairo University, Cairo, Egypt
18 Also at Suez University, Suez, Egypt
19 Now at British University in Egypt, Cairo, Egypt
20 Also at Purdue University, West Lafayette, Indiana, USA
21 Also at Université de Haute Alsace, Mulhouse, France
22 Also at Department of Physics, Tsinghua University, Beijing, China
23 Also at Tbilisi State University, Tbilisi, Georgia
24 Also at The University of the State of Amazonas, Manaus, Brazil
25 Also at Erzincan Binali Yildirim University, Erzincan, Turkey
26 Also at University of Hamburg, Hamburg, Germany
27 Also at RWTH Aachen University, III. Physikalisches Institut A, Aachen, Germany
28 Also at Isfahan University of Technology, Isfahan, Iran
29 Also at Bergische University Wuppertal (BUW), Wuppertal, Germany
30 Also at Brandenburg University of Technology, Cottbus, Germany
31 Also at Forschungszentrum Jülich, Juelich, Germany
32 Also at CERN, European Organization for Nuclear Research, Geneva, Switzerland
33 Also at Institute of Physics, University of Debrecen, Debrecen, Hungary
34 Also at Institute of Nuclear Research ATOMKI, Debrecen, Hungary
35 Now at Universitatea Babes-Bolyai - Facultatea de Fizica, Cluj-Napoca, Romania
36 Also at MTA-ELTE Lendület CMS Particle and Nuclear Physics Group, Eötvös Loránd
University, Budapest, Hungary
37 Also at Physics Department, Faculty of Science, Assiut University, Assiut, Egypt
38 Also at HUN-REN Wigner Research Centre for Physics, Budapest, Hungary
39 Also at Punjab Agricultural University, Ludhiana, India
40 Also at University of Visva-Bharati, Santiniketan, India
41 Also at Indian Institute of Science (IISc), Bangalore, India
42 Also at Birla Institute of Technology, Mesra, Mesra, India
43 Also at IIT Bhubaneswar, Bhubaneswar, India
44 Also at Institute of Physics, Bhubaneswar, India

## PDF page 48

46
45 Also at University of Hyderabad, Hyderabad, India
46 Also at Deutsches Elektronen-Synchrotron, Hamburg, Germany
47 Also at Department of Physics, Isfahan University of Technology, Isfahan, Iran
48 Also at Sharif University of Technology, Tehran, Iran
49 Also

at Department of Physics, University of Science and Technology of Mazandaran,
Behshahr, Iran
50 Also at Helwan University, Cairo, Egypt
51 Also at Italian National Agency for New Technologies, Energy and Sustainable Economic
Development, Bologna, Italy
52 Also at Centro Siciliano di Fisica Nucleare e di Struttura Della Materia, Catania, Italy
53 Also at Università degli Studi Guglielmo Marconi, Roma, Italy
54 Also at Scuola Superiore Meridionale, Università di Napoli ’Federico II’, Napoli, Italy
55 Also at Fermi National Accelerator Laboratory, Batavia, Illinois, USA
56 Also at Ain Shams University, Cairo, Egypt
57 Also at Consiglio Nazionale delle Ricerche - Istituto Officina dei Materiali, Perugia, Italy
58 Also at Department of Applied Physics, Faculty of Science and Technology, Universiti
Kebangsaan Malaysia, Bangi, Malaysia
59 Also at Consejo Nacional de Ciencia y Tecnologı́a, Mexico City, Mexico
60 Also at Trincomalee Campus, Eastern University, Sri Lanka, Nilaveli, Sri Lanka
61 Also at Saegis Campus, Nugegoda, Sri Lanka
62 Also at National and Kapodistrian University of Athens, Athens, Greece
63 Also at Ecole Polytechnique Fédérale Lausanne, Lausanne, Switzerland
64 Also at Universität Zürich, Zurich, Switzerland
65 Also at Stefan Meyer Institute for Subatomic Physics, Vienna, Austria
66 Also at Laboratoire d’Annecy-le-Vieux de Physique des Particules, IN2P3-CNRS, Annecy-leVieux, France
67 Also at Near East University, Research Center of Experimental Health Science, Mersin,
Turkey
68 Also at Konya Technical University, Konya, Turkey
69 Also at Izmir Bakircay University, Izmir, Turkey
70 Also at Adiyaman University, Adiyaman, Turkey
71 Also at Bozok Universitetesi Rektörlügü, Yozgat, Turkey
72 Also at Marmara University, Istanbul, Turkey
73 Also at Milli Savunma University, Istanbul, Turkey
74 Also at Kafkas University, Kars, Turkey
75 Now at stanbul Okan University, Istanbul, Turkey
76 Also at Hacettepe University, Ankara, Turkey
77 Also at Istanbul University - Cerrahpasa, Faculty of Engineering, Istanbul, Turkey
78 Also at Yildiz Technical University, Istanbul, Turkey
79 Also at Vrije Universiteit Brussel, Brussel, Belgium
80 Also at School of Physics and Astronomy, University of Southampton, Southampton, United
Kingdom
81 Also at IPPP Durham University, Durham, United Kingdom
82 Also at Monash University, Faculty of Science, Clayton, Australia
83 Also at Università di Torino, Torino, Italy
84 Also at Bethel University, St. Paul, Minnesota, USA
85 Also at Karamanoğlu Mehmetbey University, Karaman, Turkey
86 Also at California Institute of Technology, Pasadena, California, USA
87 Also at United States Naval Academy, Annapolis, Maryland, USA

## PDF page 49

47
88 Also at Bingol University, Bingol, Turkey
89 Also at Georgian Technical University, Tbilisi, Georgia
90 Also at Sinop University, Sinop, Turkey
91 Also at Erciyes University, Kayseri, Turkey
92 Also at Horia Hulubei National Institute of Physics and Nuclear Engineering (IFIN-HH),

Bucharest, Romania
93 Now at an institute or an international laboratory covered by a cooperation agreement with
CERN
94 Also at Texas A&M University at Qatar, Doha, Qatar
95 Also at Kyungpook National University, Daegu, Korea
96 Also at another institute or international laboratory covered by a cooperation agreement
with CERN
97 Also at Universiteit Antwerpen, Antwerpen, Belgium
98 Also at Yerevan Physics Institute, Yerevan, Armenia
99 Also at Northeastern University, Boston, Massachusetts, USA
100 Also at Imperial College, London, United Kingdom
101 Also at Institute of Nuclear Physics of the Uzbekistan Academy of Sciences, Tashkent,
Uzbekistan
