Source: https://iopscience.iop.org/article/10.1088/1748-0221/12/02/P02014/pdf
PDF sha256: 00e9f466c1a01bf71018e889733473a5ae793c673ac0ec18f6067d5ba39bf232
License: CC-BY-3.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of khachatryan_2017_jet_energy_scale_resolution_cms.pdf

Transcription of `khachatryan_2017_jet_energy_scale_resolution_cms.pdf` in this directory, 95 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-95 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Journal of
Instrumentation

You may also like

OPEN ACCESS

Jet energy scale and resolution in the CMS
experiment in pp collisions at 8 TeV
To cite this article: V. Khachatryan et al 2017 JINST 12 P02014

View the article online for updates and enhancements.

- An embedding technique to determine
backgrounds in proton-proton collision
data
A.M. Sirunyan, A. Tumasyan, W. Adam et
al.
- Performance of the CMS muon detector
and muon reconstruction with protonproton collisions at s=13 TeV
A.M. Sirunyan, A. Tumasyan, W. Adam et
al.
- Performance of reconstruction and
identification of leptons decaying to
hadrons and v in pp collisions at s=13 TeV
A.M. Sirunyan, A. Tumasyan, W. Adam et
al.

This content was downloaded from IP address 47.33.86.95 on 02/11/2026 at 05:16

## PDF page 2

Published by IOP Publishing for Sissa Medialab
Received: July 13, 2016
Revised: January 22, 2017
Accepted: January 29, 2017
Published: February 22, 2017

Jet energy scale and resolution in the CMS experiment in

The CMS collaboration
E-mail: cms-publication-committee-chair@cern.ch
Abstract: Improved jet energy scale corrections, based on a data sample corresponding to an
integrated luminosity of 19.7 fb−1 collected by the CMS experiment in proton-proton collisions at
a center-of-mass energy of 8 TeV, are presented. The corrections as a function of pseudorapidity
η and transverse momentum pT are extracted from data and simulated events combining several
channels and methods. They account successively for the effects of pileup, uniformity of the detector
response, and residual data-simulation jet energy scale differences. Further corrections, depending
on the jet flavor and distance parameter (jet size) R, are also presented. The jet energy resolution
is measured in data and simulated events and is studied as a function of pileup, jet size, and jet
flavor. Typical jet energy resolutions at the central rapidities are 15–20% at 30 GeV, about 10% at
100 GeV, and 5% at 1 TeV. The studies exploit events with dijet topology, as well as photon+jet,
Z+jet and multijet events. Several new techniques are used to account for the various sources of
jet energy scale corrections, and a full set of uncertainties, and their correlations, are provided.The
final uncertainties on the jet energy scale are below 3% across the phase space considered by most
analyses (pT > 30 GeV and |η| < 5.0). In the barrel region (|η| < 1.3) an uncertainty below 1% for
pT > 30 GeV is reached, when excluding the jet flavor uncertainties, which are provided separately
for different jet flavors. A new benchmark for jet energy scale determination at hadron colliders is
achieved with 0.32% uncertainty for jets with pT of the order of 165–330 GeV, and |η| < 0.8.
Keywords: Large detector-systems performance; Performance of High Energy Physics Detectors
ArXiv ePrint: 1607.03663

© CERN 2017 for the benefit of the CMS collaboration, published under the terms of the
Creative Commons Attribution 3.0 License by IOP Publishing Ltd and Sissa Medialab
srl. Any further distribution of this work must maintain attribution to the author(s) and the published
article’s title, journal citation and DOI.

doi:10.1088/1748-0221/12/02/P02014

2017 JINST 12 P02014

pp collisions at 8 TeV

## PDF page 3

Contents
Introduction

1

2

The CMS detector and event reconstruction
2.1 Jet reconstruction

4
5

3

Event samples and selection criteria
3.1 Simulated samples
3.2 Data sets and event selection

6
6
6

4

Pileup offset corrections
4.1 Pileup observables
4.2 Pileup mitigation
4.3 Hybrid jet area method
4.4 Pileup offset correction uncertainties
4.5 Summary of pileup offset corrections

8
9
10
12
16
18

5

Simulated response corrections
5.1 Corrections versus η and pT
5.2 Dependence on the jet size
5.3 Detector simulation uncertainties
5.4 Jet energy corrections propagation to missing transverse momentum
5.5 Summary of simulated response corrections

20
21
21
22
23
24

6

Residual corrections for data
6.1 Relative η-dependent corrections
6.2 Relative correction uncertainties
6.3 Absolute corrections
6.4 Global fit of absolute corrections
6.5 Absolute correction uncertainties
6.6 Summary of residual corrections

25
26
30
32
38
40
42

7

Jet flavor corrections
7.1 Jet flavor definitions
7.2 Simulated flavor corrections
7.3 Flavor uncertainties
7.4 Z+b balance

43
43
43
46
49

8

Jet pT resolution
8.1 Methods
8.2 Simulated particle-level resolution
8.3 Dijet asymmetry

50
51
52
54

–i–

2017 JINST 12 P02014

1

## PDF page 4

8.4
9

The γ+jet balance

58

Systematic uncertainties
9.1 Uncertainties in 7 TeV analyses

60
65

10 The PF jet composition

66

11 Conclusions

69

The CMS collaboration

75

Introduction

The state-of-the-art techniques used in the CMS experiment at the CERN LHC for jet energy
scale (JES) and jet energy resolution (JER) calibration are presented, based on a data sample
corresponding to an integrated luminosity of 19.7 fb−1 collected in proton-proton collisions at a
center-of-mass energy of 8 TeV. Jets are the experimental signatures of energetic quarks and gluons
produced in high-energy processes. Like all experimentally-reconstructed objects, jets need to be
calibrated in order to have the correct energy scale: this is the aim of the jet energy corrections
(JEC). The detailed understanding of both the energy scale and the transverse momentum resolution
of the jets is of crucial importance for many physics analyses, and a leading component of their
associated systematic uncertainties. Improvements made in understanding the JES in the recent
years have resulted in very precise measurements of, e.g., the inclusive jet cross section [1–5], and
the top quark mass [6–9]. The JES uncertainties presented here propagate to uncertainties of 2–4%
in the jet cross sections in the central region, and of ±0.35 GeV in the top-quark mass determination.
The results in this paper are reported for jets reconstructed with the particle-flow (PF)
method [10, 11] using the anti-k T algorithm [12] with distance parameter R = 0.5. The jet
energy corrections are calculated using a detailed Monte Carlo (MC) simulation of the detector,
and are then adjusted for data using a combination of several channels and data-driven methods.
The JEC successively correct for the offset energy coming from multiple proton-proton collisions
in the same and adjacent beam crossings (pileup), the detector response to hadrons, and residual
differences between data and MC simulation as a function of the jet pseudorapidity η and transverse
momentum pT . The jet pT is corrected up to the so-called particle-level jets clustered from stable
(decay length cτ > 1 cm) and visible (excluding neutrinos) final-state particles.
Corrections depending on jet flavor (for quarks: u and d, s, c and b; and for gluons) and jet
distance parameter R are also presented. The uncertainties affecting the JES determination are
discussed, and a full set of uncertainties and their correlations are provided. Figure 1 shows the
jet response at the various stages of JEC for jets (produced in quantum chromodynamics (QCD)
hard-scattering processes) measured at central pseudorapidities (|η| < 1.3): for each bin in pT, ptcl ,
the jet response is defined as the average value of the ratio of measured jet pT to particle-level jet
pT, ptcl . The response is shown before any correction, after correcting for the effect of pileup, and
after all stages of corrections, that will be detailed in the following. Distributions corresponding

–1–

2017 JINST 12 P02014

1

## PDF page 5

Simulation

1.5
1.4
1.3
1.2

QCD Monte Carlo
Anti-kT R=0.5, PF+CHS
|η| < 1.3
No pileup (µ = 0)
0 < µ < 10
10 < µ < 20
20 < µ < 30
30 < µ < 40

1.1
1
0.9
0.8

30

100 200

1000 2000

pT, ptcl (GeV)

(8 TeV)

1.7
1.6

CMS
Simulation

1.5
1.4
1.3
1.2

QCD Monte Carlo
Anti-kT R=0.5, PF+CHS
|η| < 1.3
No pileup (µ = 0)
0 < µ < 10
10 < µ < 20
20 < µ < 30
30 < µ < 40

1.1

Corrected response

1.6

CMS

Pileup-corrected response

Response

(8 TeV)

1.7

1.6

CMS
Simulation

1.5
1.4
1.3
1.2

QCD Monte Carlo
Anti-kT R=0.5, PF+CHS
|η| < 1.3
No pileup (µ = 0)
0 < µ < 10
10 < µ < 20
20 < µ < 30
30 < µ < 40

1.1

1

1

0.9

0.9

0.8

(8 TeV)

1.7

30

100 200

1000 2000

pT, ptcl (GeV)

0.8

30

100 200

1000 2000

pT, ptcl (GeV)

to different average numbers of pileup interactions per bunch crossing (µ) are shown separately, to
display the dependence of the response on the pileup.
The jet pT resolution, measured after applying JEC, is extracted in data and simulated events.
It is studied as a function of pileup, jet size R, and jet flavor. The effect of the presence of neutrinos
in the jets is also studied. The typical JER is 15–20% at 30 GeV, about 10% at 100 GeV, and 5% at
1 TeV at central rapidities.
The general principles behind the methods of extraction of the JES, and the reasons why the
JES obtained with the PF algorithm is different from unity, are discussed. The results and methods
are compared to previous CMS studies done for 7 TeV proton-proton collisions [13]. Several new
techniques are introduced in this paper to account for pT -dependent pileup offset, out-of-time (OOT)
pileup, initial- and final-state radiation (ISR+FSR), and b-quark jet (b-jet) flavor response. We also
add the information from multijet balancing [14] and introduce a new technique that uses it as part
of a global pT -dependent fit which constrains the uncertainties by using their correlations between
channels and methods.
Pileup collisions result in unwanted calorimetric energy depositions and extra tracks. The
charged-hadron subtraction (CHS, section 4.2) reduces these effects by removing tracks identified
as originating from pileup vertices. The results in this paper are reported for jets reconstructed with
and without CHS.
The JEC are extracted for jets with pT > 10 GeV and |η| < 5.2, with uncertainties less than
or about 3% over the whole phase space. The minimum JES uncertainty of 0.32% for jets with
165 < pT < 330 GeV and |η| < 0.8, when excluding sample-dependent uncertainties due to jetflavor response and time-dependent detector response variations, surpasses the precision of previous
JES measurements at the Tevatron [15, 16] and the LHC [13, 17].
Outline of the paper and overview of the corrections
The CMS detector and reconstruction algorithms are briefly described in section 2. The data
and MC samples used throughout this document, together with the different selection criteria, are
detailed in section 3.

–2–

2017 JINST 12 P02014

Figure 1. Average value of the ratio of measured jet pT to particle-level jet pT, ptcl in QCD MC simulation, in
bins of pT, ptcl , at various stages of JEC: before any corrections (left), after pileup offset corrections (middle),
after all JEC (right). Here µ is the average number of pileup interactions per bunch crossing.

## PDF page 6

Applied to data
Pileup
Reconstructed MC + RC
Jets
MC

Response (pT , η)
MC

Residuals(η)
dijets

Residuals(pT )
Flavor
γ/Z+jet, MJB
MC

Calibrated
Jets

Applied to simulation

The pileup offset corrections, discussed in section 4, are determined from the simulation of
a sample of dijet events processed with and without pileup overlay. They are parameterized as a
function of offset energy density ρ, jet area A, jet pseudorapidity η, and jet transverse momentum
pT . Corrections for residual differences between data and detector simulation as a function of η are
determined using the random cone (RC, section 4.3) method in zero-bias events (section 3.2). The
pileup offset corrections are determined both before and after CHS, which removes tracks identified
as originating from pileup vertices.
The simulated jet response corrections are determined with a CMS detector simulation based
on Geant4 [18] combined with the pythia 6.4 [19] tune Z2* [20], as discussed in section 5. The
corrections are determined for various jet sizes. The default corrections are provided for the QCD
dijet flavor mixture as a function of pT and η. Uncertainties arising from the modeling of jet
fragmentation are evaluated with herwig++ 2.3 [21] tune EE3C [22], and uncertainties from the
detector simulation are evaluated with the CMS fast simulation [23].
The residual corrections for data are discussed in section 6. The η-dependent corrections are
determined with dijet events, relative to a jet of similar pT in the barrel reference region |η| < 1.3.
These corrections include a pT dependence of the JES relative to the JES of the barrel jet for
pT > 62 GeV and up to about 1 TeV, the limit of available dijet data. The absolute scale, together
with its pT dependence within |η| < 1.3 for 30 < pT < 800 GeV, is measured combining photon+jet,
Z(→ µµ)+jet and Z(→ ee)+jet events. The pT dependence at pT > 800 GeV is constrained with
multijet events. Detailed studies are performed to correct for biases in the data-based methods due
to differences with respect to the MC simulation in ISR+FSR as well as in jet pT resolution.
The optional jet-flavor corrections derived from MC simulation are discussed in section 7
together with the JEC flavor uncertainty estimates based on comparing pythia 6.4 and herwig++
2.3 predictions. These uncertainties are applicable to data vs. simulation comparisons regardless of
whether or not the jet-flavor corrections are applied. The flavor corrections and their uncertainties
for b-quark jets are checked in data with Z+b events. The consecutive steps of the JEC are illustrated
in figure 2.
The jet pT resolutions are determined with both dijet and photon+jet events, as discussed in
section 8. The reference resolutions obtained from simulation are parameterized as a function of
particle-level jet pT, ptcl (defined in section 2) and average number µ of pileup interactions in bins
of jet η. Corrections for differences between data and MC simulation are applied as η-binned scale
factors.

–3–

2017 JINST 12 P02014

Figure 2. Consecutive stages of JEC, for data and MC simulation. All corrections marked with MC are
derived from simulation studies, RC stands for random cone, and MJB refers to the analysis of multijet events.

## PDF page 7

The JES uncertainties, discussed in section 9, are provided in the form of a limited set of
sources that allow a detailed statistical analysis of uncertainty correlations. The final uncertainties
are below 1% across much of the phase space covered by these corrections at pT > 10 GeV and
|η| < 5.2. This sets a new benchmark for jet energy scale at hadron colliders.
In section 10 we describe additional studies made by investigating the particle composition
of reconstructed PF jets. These support the overall conclusions drawn from the determination of
residual jet energy corrections to be applied on data.

2

The CMS detector and event reconstruction

–4–

2017 JINST 12 P02014

The central feature of the CMS apparatus is a 3.8 T superconducting solenoid of 6 m internal
diameter. Within the field volume are the silicon tracker, the crystal electromagnetic calorimeter
(ECAL), and the brass and scintillator hadron calorimeter (HCAL). The muon system is installed
outside the solenoid and embedded in the steel flux-return yoke. CMS uses a right-handed coordinate
system, with the origin at the nominal interaction point, the z axis pointing along the direction of
the counterclockwise beam, the y axis pointing up (perpendicular to the plane of the LHC ring),
and the x axis chosen to make a right-handed coordinate system. The polar angle θ is measured
from the positive z axis, and the azimuthal angle φ is measured in the x-y plane in radians.
The CMS tracker consists of 1 440 silicon pixel and 15 148 silicon strip detector modules, with
full azimuthal coverage within |η| < 2.5. The ECAL consists of 75 848 lead tungstate crystals, which
provide coverage in pseudorapidity |η| < 1.479 in the central barrel region and 1.479 < |η| < 3.000
in the two forward endcap regions. The HCAL is a sampling calorimeter using alternating layers of
brass or steel as absorber and plastic scintillator as active material, it provides a coverage of |η| < 1.3
in the central region and 1.3 < |η| < 3.0 in the endcap regions. In the forward region (3.0 < |η| <
5.0), a different calorimeter technology is employed in the hadron forward (HF) detector, which uses
the Cherenkov light signals collected by short and long quartz readout fibers to aid the separation of
electromagnetic (EM) and hadronic signals. The muon system includes barrel drift tubes covering
the pseudorapidity range |η| < 1.2, endcap cathode strip chambers (0.9 < |η| < 2.5), and resistiveplate chambers (|η| < 1.6). A detailed description of the CMS detector can be found in ref. [24].
Events in CMS are reconstructed using the PF technique [10, 11], which reconstructs and identifies single particles with an optimized combination of all subdetector information. To suppress
noise in the calorimeters, only cells with energies above a given threshold are considered, this procedure is referred to as “zero suppression”. The energy of photons is obtained directly from the ECAL
measurement, corrected for zero-suppression effects. The energy of electrons is determined from a
combination of the track momentum at the main interaction vertex, the corresponding ECAL cluster
energy, and the energy sum of all bremsstrahlung photons associated with the track. The energy
of muons is obtained from the corresponding track momentum. The energy of charged hadrons is
determined from a combination of the track momentum and the corresponding ECAL and HCAL
energies, corrected for zero-suppression effects, and calibrated for the nonlinear response of the
calorimeters. Finally, the energy of neutral hadrons is obtained from the corresponding calibrated
ECAL and HCAL energies. In the forward region, energy deposits collected by the HF are considered as electromagnetic or hadronic, depending on the respective energy collected by long and short
fibers. The particles reconstructed with the PF algorithm are jointly referred to as PF candidates.

## PDF page 8

Jets are reconstructed by clustering the PF candidates, and the missing transverse momentum p⃗Tmiss is
the negative vectorial sum of the transverse momenta of all PF candidates reconstructed in an event.
Interaction vertices are reconstructed using track information only, and the primary interaction
vertex is defined as the vertex with the highest sum of the squared transverse momenta of the tracks
associated with it.
The first level (L1) of the CMS trigger system, composed of custom hardware processors, uses
information from the calorimeters and muon detectors to select the most interesting events in a fixed
time interval of less than 4 µs. The high-level trigger (HLT) processor farm further decreases the
event rate from around 100 kHz to less than 1 kHz before data storage.
Jet reconstruction

Jets considered in this paper are reconstructed with the anti-k T clustering algorithm [12]. The
nominal results are obtained for a jet distance parameter, R = 0.5, which was used in most CMS
analyses of 7 and 8 TeV data. Both the JES and JER are also studied for different values of the R
parameter, on simulated events.
The simulated particle-level jets are built by applying the clustering procedure to all stable
(lifetime cτ > 1 cm) particles excluding neutrinos. The lifetime of heavy hadrons (containing c
and b quarks) is shorter than cτ = 1 cm, so their decay products are the particles considered for jet
clustering. The exclusion of neutrinos is a convention adopted by CMS, but it is not universally
adopted by all experiments in high-energy physics. Indeed, neutrinos are often included at the
particle level, but the response is measured from samples with negligible neutrino content, leading
to practically no difference for inclusive JEC. The CMS convention allows us to define response in a
way that is experimentally accessible and significantly reduces response differences between heavyflavor (c, b) and light-quark (u, d, s) or gluon jets, caused by neutrinos produced in semileptonic
decays of heavy-flavor hadrons. It should be noted that the neutrino fraction leads to an additional
systematic uncertainty in the heavy hadrons fragmentation relative to the original b and c quarks that
is not included in JEC systematics, but should be considered in, e.g., measurements of the inclusive
b-jet cross section or of the top quark mass. The performance of the corrections for b jets is discussed
in section 7.4. The variables referring to particle-level jets are labeled “ptcl" in this document.
We consider two types of reconstructed jets, depending on how the subdetector information is
used: calorimeter jets and PF jets.
The calorimeter (CALO) jets are reconstructed from energy deposits in the calorimeter towers
alone. A calorimeter tower consists of one or more HCAL cells and the geometrically corresponding
ECAL crystals. In the barrel region of the calorimeters, the unweighted sum of one single HCAL
cell and 5×5 ECAL crystals form a projective calorimeter tower. The association between HCAL
cells and ECAL crystals is more complex in the endcap regions. A four-momentum is associated
with each tower deposit above a certain threshold, assuming zero mass, and taking the direction of
the tower position as seen from the interaction point.
The PF jets are reconstructed by clustering the four-momentum vectors of PF candidates. The
PF jet momentum and spatial resolutions are greatly improved with respect to calorimeter jets, as
the use of the tracking detectors and high granularity of the ECAL improves the energy resolution
through the independent measurements of charged hadrons and photons inside a jet, which together

–5–

2017 JINST 12 P02014

2.1

## PDF page 9

constitute ≈85% of the average jet energy. In reconstructing the PF candidate four-momentum,
photons are assumed massless and charged hadrons are assigned the charged pion mass.
Calorimeter jets result from a relatively simplistic yet robust approach and were widely used in
the early CMS publications. With the improvement of the understanding of the detector and the commissioning of the reconstruction with data, the performance of the PF reconstruction has proven to be
outstanding and reliable. The event description and reconstruction is more complete and consistent,
and for these reasons, we focus here on the PF jets used in the majority of recent CMS analyses.

Event samples and selection criteria

3.1

Simulated samples

Simulated samples are generated for QCD dijet and multijet, Z+jet, and γ+jet processes. A sample
with single-neutrino production is simulated as well, to reproduce empty events that only contain
pileup and detector noise. The dijet, γ+jet and single-neutrino samples are generated with pythia
6.4 [19], using the tune Z2* [20]. The Z+jet and multijet samples are generated with the MadGraph 4 [25] program matched with parton showers simulated by pythia 6.4 tune Z2*. Additional
samples for systematic uncertainty studies are available for QCD dijet and Z+jet processes, both
generated with herwig++ 2.3 [21], tune EE3C [22]. The single-neutrino sample is compared to
zero-bias data (section 4.3). The dijet sample is used to simulate the jet response (section 5) and
also in comparison to data in the dijet balance analysis (section 6.1). The Z+jet and γ+jet simulated
samples are used in comparisons of measured response with the corresponding selected samples of
data (section 6.3). The multijet sample is used in the multijet balance analysis (section 6.3).
Additional samples are used for the analysis of events with a Z boson and a b jet (section 7.4):
the MadGraph 4 program, together with pythia 6.4 for the hadronization, is used to simulate
top quark pair, W+jets and Drell-Yan+jets (DY+jets) production; and the powheg [26] program,
together with pythia 6.4 for the hadronization, is used for single top quark samples. A DY+jets
sample produced with herwig++ 2.3 is also used for studies of systematic uncertainties.
All generated samples are processed through the CMS detector simulation, based on
Geant4 [18]. Minimum bias events, generated with pythia 6.4 and tune Z2*, are overlayed
to all above samples to simulate the pileup. As will be detailed in section 4, the MC simulation is
reweighted to match the distribution of the average number of pileup interactions in data.
3.2

Data sets and event selection

The studies presented in this document use the data collected by the CMS experiment in protonproton collisions at a center-of-mass energy of 8 TeV, during the year 2012, corresponding to an
integrated luminosity of 19.7 fb−1 . In this section we describe the selection criteria used in the
different analyses presented in this paper. Only data collected during stable-conditions collisions
with a fully-functioning detector are considered. Apart from the zero-bias sample, all data samples
are required to fulfill some basic event preselection criteria. The presence of at least one wellreconstructed primary vertex (PV) is required [27], with at least four tracks considered in the vertex
fit, and with |z(PV)| < 24 cm, where z(PV) represents the position of the PV along the beam
axis. The radial position of the primary vertex, r xy (PV), has to satisfy the condition r xy (PV) < 2

–6–

2017 JINST 12 P02014

3

## PDF page 10

cm. Finally, the jets used in the analyses are required to satisfy basic identification criteria (“Jet
ID”) [28], which on simulation are found to retain more than 99% of genuine jets, while rejecting
most of the misreconstructed jets arising from detector noise or cosmic muons.

Dijet sample. The dijet sample, composed of events with at least two jets in the final state, is
collected using dedicated HLTs, which accept the events depending on the value of the average
pT (pT,ave = (pT, 1st jet + pT, 2nd jet )/2) of the two highest-pT jets in the event, to ensure an unbiased
data set. The HLT uses a PF reconstruction algorithm with simplified tracking, and the jet pT is
corrected for nonuniformity of the energy response as a function of the jet η and pT . Several pT,ave
thresholds are available, with different prescale factors. Depending on the value of the highest jet
pT in the event, only the least prescaled fully efficient HLT is used for the decision of keeping or
rejecting the event for further analysis. Events selected with single-jet triggers are also used for the
studies of jet composition shown in section 10.
The event selection requires at least one of the two leading jets to have |η| < 1.3 and the
angular separation between the two leading jets in the (x, y) plane to be |∆φ1st jet, 2nd jet | > 2.7.
Events are rejected if there is any third jet with pT, 3rd jet > 5 GeV not fulfilling the condition
pT, 3rdjet /pT,ave = α < 0.2. As will be explained in section 6.1, the results are studied as a function
of the α cut from α < 0.4 to α < 0.1 in order to correct for biases from ISR+FSR.
The Z+jet sample. The Z(→ µµ)+jet and Z(→ ee)+jet samples are collected using singlelepton HLTs with various pT thresholds. Events are required to contain either two oppositesign muons or two opposite-sign electrons, fulfilling standard tight isolation and identification
requirements [29, 30], with |η| < 2.3 and pT > 20 GeV. The dilepton (ℓℓ) system is required to
have pT,ll > 30 GeV and |mll − mZ | < 20 GeV, where mZ is the mass of the Z boson. The leading jet
in the event is required to have |η| < 1.3 and pT > 12 GeV, and to have a large angular separation
in the (x, y) plane with respect to the dilepton system, |∆φ(Z, 1st jet)| > 2.8. Events are rejected if
there is any second jet with pT, 2nd jet > 5 GeV not fulfilling the condition pT,2nd jet /pT,Z = α < 0.3.
The value of the cut on |∆φ(Z, 1st jet)| is such that it does not bias the distribution of α for α < 0.3.
As will be explained in section 6.3, the requirement on α is tightened from the nominal value of
0.3 and the results are studied as a function of its value. In the Z(→ ee)+jet
analysis an additional
√
requirement is enforced that no electron in the event lie within ∆R = (∆φ) 2 + (∆η) 2 = 0.5 of a
jet. The Z+jet selection is also used in section 7.4, with the additional requirement that the jet is
tagged as coming from a b quark using the combined secondary vertex tagger [31], with a typical
tagging efficiency of 70% and a misidentification probability for light-flavor jets of 1%.

–7–

2017 JINST 12 P02014

Zero-bias sample. The zero-bias sample is collected using a random trigger in the presence of a
beam crossing with filled bunches, active during the whole data-taking period with stable collisions
conditions and a fully-functioning detector. As these events are not triggered by any specific energy
deposit, they generally do not contain any contribution from hard-scattering processes. The main
sources of energy deposits in zero-bias events are detector noise and pileup. The events in the dataset
are weighted, according to the luminosity evolution during the running period, in order to be representative of the average pileup conditions of the datasets used in the analyses presented in this paper.

## PDF page 11

Multijet sample. The multijet sample is collected with single-jet HLTs with various pT thresholds
and different prescale factors. Depending on the value of the highest jet pT in the event, only the
least prescaled fully efficient HLT is used for the decision of keeping or rejecting the event for further
analysis. The event selection is inspired by the analysis described in ref. [14]. Events containing
isolated leptons or photons passing standard identification criteria are rejected. The events are
required to have a pT > 250 GeV jet in |η| < 1.3 balanced by a recoil system, composed of two
or more low-pT jets with 25 < pT < 750 GeV, which is within the range calibrated by the Z/γ+jet
events, and satisfying the condition pT, 2nd jet /pT,recoil < 0.6. The events are also required to have the
recoil jets at least ∆φ(1st jet, recoil jet) > 1 radians away from the leading jet in the transverse plane,
and to have the recoil system back-to-back with the leading jet with |∆φ(1st jet, recoil syst.) − π| <
0.3. As will be explained in section 6.3, all jets with |η| < 5, pT > 10 GeV are considered to be
part of the recoil system; the analysis is also repeated after changing to pT > 20 and 30 GeV the
transverse momentum threshold for jets to be considered in the recoil.

4

Pileup offset corrections

The high instantaneous luminosity at the LHC results in multiple proton-proton collisions taking
place within a single beam crossing. Such additional pp collisions occurring within the same
bunch-crossing as the primary hard interaction produce additional tracks in the tracker and deposit
energy in the calorimeters. This contribution is called in-time pileup (IT PU). Due to the finite
signal decay time in the calorimeters, the pp collisions occurring in the previous and subsequent
beam crossings also contribute to calorimetric energy in the same time window as the primary hard
interaction. This contribution is called out-of-time pileup (OOT PU).
The additional contributions to the jet energy and momentum due to pileup are referred to as
the “pileup offset", or “offset" in this document. This offset is studied to optimize the subtraction
of pileup from the data, with the corrections leading to an improved detector resolution and a more
accurate JES.
The observables used for monitoring and correcting pileup are described in section 4.1. The
pileup subtraction then proceeds in steps. The OOT PU is mitigated by calorimeter signal processing
(section 4.2), and the IT PU by identifying charged particles originating from pileup vertices and
removing them with charged-hadron subtraction (section 4.2). The pileup jets are tagged with pileup
jet identification (PUJetID) and removed (section 4.2). The remaining diffuse energy from neutral

–8–

2017 JINST 12 P02014

The γ+jet sample. The γ+jet sample is collected with single-photon HLTs with various pT
thresholds and different prescale factors. Depending on the value of the highest photon pT in the
event, only the least prescaled fully efficient HLT is used for the decision of keeping or rejecting the
event for further analysis. Events are required to contain one, and only one, photon with pT > 40 GeV
and |η| < 1.3 that fulfills the standard tight cut-based photon identification and isolation criteria [32].
The leading jet in the event is required to have |η| < 1.3 and pT > 12 GeV and to have a
significant angular separation in the (x, y) plane with respect to the photon, |∆φ(γ, 1st jet)| > 2.8.
Events are rejected if there is any second jet with pT, 2nd jet > 5 GeV not fulfilling the condition
pT,2nd jet /pT,γ = α < 0.3. As will be explained in section 6.3, the requirement on α is tightened
from the nominal value of 0.3 and the results are studied as a function of its value.

## PDF page 12

particles and OOT PU is estimated per event and then subtracted per jet using a calculation of the
effective jet area with the extended hybrid jet area method (section 4.3). The dependence of the
particle-level PU offset on jet η and pT for this method is determined from simulation (section 4.3),
and the data/simulation offset scale factor is determined from zero-bias data and neutrino gun
simulation, with the random cone (RC) method (section 4.3). The uncertainties are discussed in
section 4.4 and the results are summarized in section 4.5.
4.1

Pileup observables

–9–

2017 JINST 12 P02014

The amount of pileup present in the event can be estimated by counting the number of good-quality
primary vertices NPV or by calculating the diffuse offset energy density ρ [33, 34] in the event. It can
also be measured using luminosity monitors that estimate the average number of pileup interactions
per crossing.
The offset energy density ρ is calculated using the kT clustering algorithm [35–37] with distance
parameter D = 0.6 and |η| < 4.7. For this calculation, a large number of nonphysical particles
(ghosts) with infinitesimal momenta and random direction effectively mapping all the (η, φ) space,
is added to the event. When the jet clustering is run on the event, the hard particles in the event
are clustered together with such ghosts: a few jets will contain high-momentum particles from
the hard-scattering interaction, but most of the jets will be entirely made of ghosts, for which the
main real energy contributions come from detector noise and especially pileup. The offset energy
density ρ is defined, in each event, as the median of jet momenta pT,i divided by their area Ai ,
ρ = median(pT,i /Ai ) [38]. For this calculation, no selection on the jet momenta is applied. Using
the median instead of the mean makes ρ effectively insensitive to hard jets in the event, and including
zero-energy jets composed of only ghost particles reduces bias for low pileup energy densities. For
Run 2, a simpler approach is used to calculate ρ, which is evaluated as the median of the energies
calculated in a grid of η − φ cells, and does not make use of jet clustering anymore.
The number of good primary vertices NPV includes vertices consistent with the luminous region
(where the collisions happen) and with a number of degrees of freedom Ndof ≥ 4, corresponding to
a minimum of four tracks.
The average number of pileup interactions µ is obtained by multiplying the instantaneous luminosity with the effective minimum bias cross section of σMB = 69.4 mb for 8 TeV (68.0 mb for
7 TeV) [39]. Two detectors are exploited for the luminosity measurement: the hadron forward (HF)
calorimeter and the silicon pixel detector. The counting of pixel clusters is used for the offline precision measurement, because of its time stability and very small dependence on pileup. The HF allows
for online determination of instantaneous luminosity per bunch crossing. Its results, calibrated offline per luminosity section that corresponds to 23.3 seconds of data, are used for cross-checks [40].
The agreement between data and simulation on NPV and ρ, after reweighting the simulation to
match the distribution of the average number of pileup interactions (µ) in data, is shown in figure 3.
The agreement for NPV is excellent, while ρ exhibits a small, mostly linear, deviation that is due to
different offset densities in data and simulation in the endcap and forward calorimeters.
Both NPV and ρ are very nearly linearly dependent on µ over the tested range, as shown in
figure 4. The pileup vertex reconstruction and identification efficiency is about 70% (while nearly
100% for hard-scattering events), and IT PU contributes about 0.5 GeV to ρ per interaction. The
vertex z resolution is around 100–300 µm for minimum-bias vertices, improving to tens of microns

## PDF page 13

I

×106

19.7 fb−1 (8 TeV)
Events per GeV

Events per bin

1.0

Data
MC

CMS

0.8
0.6
0.4

19.7 fb−1 (8 TeV)
Data
MC

CMS

1.0
0.8
0.6
0.4
0.2

0

5

10

15

20

25

30

35

NPV

0.0

0

5

10

15

20

25

30

35

ρ (GeV)

Figure 3. Comparison of data (circles) and pythia 6.4 simulation (histograms) for the distributions of the
number of reconstructed primary vertices NPV (left), and of the offset energy density ρ (right).

for hard-scattering events. With a luminous region of root-mean-square (RMS) of about 4 cm in
the z direction, the vertex reconstruction is expected to remain linear up to 100–200 vertices. The
NPV versus µ exhibits a small negative quadratic term due to infrequent merging of pileup vertices,
while ρ versus µ exhibits a similarly small positive quadratic term owing to effects such as effective
failed zero-suppression of overlapping calorimeter deposits. These quadratic terms account for less
than 0.5 vertices in NPV and 0.5 GeV in ρ at µ = 20, respectively.
The correlation between IT PU and OOT PU is modeled by generating the number of interactions for each bunch crossing using a Poisson distribution with the same mean µ. This is a good
approximation for 2012 (8 TeV) data, given that the RMS of the bunch-to-bunch variation of µ
within a single luminosity section was only about 8%. The value of NPV is insensitive to OOT PU,
while ρ has a small (<5% of the total) OOT PU component with 50 ns bunch crossings. The NPV
variable is highly (≈94%) correlated with the number of IT PU interactions in the event, while ρ is
also sensitive to the amount of energy deposited by each interaction, and thus less strongly (≈85%)
correlated with the interaction multiplicity.
4.2

Pileup mitigation

Out-of-time pileup. The amount of OOT PU can be reduced by shortening the signal timeintegration window and by increasing the separation between bunches.
In HCAL, 68% of the signal is contained within a 25 ns time window [41], resulting in about
5% leakage to a subsequent crossing with 50 ns bunch spacing and 50 ns time integration window.
The signal decay time in ECAL is of the order of 100 ns, but the ECAL reconstruction involves
three samples of 25 ns before the signal and five on the signal, to remove a varying pedestal. This
removes OOT PU on average, but with performance depending on the position of the proton bunch
within the bunch train, and requiring simulation of up to six preceding bunch crossings (−300 ns).

– 10 –

2017 JINST 12 P02014

0.2
0.0

I

×106

## PDF page 14

I

19.7 fb−1 (8 TeV)
ρ (GeV)

NPV

I

CMS

35
30

NPV (µ) = 1.11 + 0.70 µ − 0.0013 µ2
NPV (µ) = 1.14 + 0.67 µ − 0.0008 µ2

25

19.7 fb−1 (8 TeV)

CMS

25
ρ(µ) = 1.00 + 0.54 µ + 0.0005 µ2
ρ(µ) = 1.01 + 0.50 µ + 0.0007 µ2

20

20

15

15

5

5

Data
MC
0

10

20

30

0

40

µ

Data
MC
0

10

20

30

40

µ

Figure 4. Mean of the number of good primary vertices per event, ⟨NPV ⟩ (left), and mean diffuse offset
energy density, ⟨ρ⟩ (right), versus the average number of pileup interactions per bunch crossing, µ, for data
(circles) and pythia 6.4 simulation (diamonds).

The variation in the offset correction can be up to 10% in the endcaps when selecting bunches
in the front of bunch trains, which represent a small fraction (< 10%) of data. The correction is
evaluated on the whole dataset and hence this effect averages out. In HF, the signal is only 10 ns
wide, resulting in negligible OOT PU without any special treatment of the signal.
More advanced techniques are used in Run 2, exploiting the signal timing and pulse shape to
fit in-time and out-of-time pulses simultaneously.
Charged-hadron subtraction. The IT PU from charged particles is reduced by identifying which
vertex the charged PF candidates originate from, and removing those unambiguously associated
with pileup vertices before clustering jets and p⃗Tmiss . This method is referred to as charged-hadron
subtraction.
The leading primary vertex is chosen based on the largest sum of squares of the tracks transverse
∑
momenta ( |pTtrack | 2 ) associated with the vertex. Subleading PV’s, classified as pileup vertices, are
required to pass further quality criteria on the compatibility with the luminous region and on their
minimum number of degrees of freedom
Ndof = −3 + 2

nTracks
∑

wi ,

and wi ∈ [0, 1],

(4.1)

i=1

where wi is the weight assigned to the corresponding track by the adaptive vertex fit [27], based on
its compatibility with the vertex. The minimum requirement Ndof > 4 corresponds to at least four
tracks. Tracks are matched to vertices based on their chi-squared per degree of freedom ( χ2 /Ndof ).
If χ2 /Ndof < 20 for a vertex, then the track is associated with this and only this vertex. If the track
from a charged hadron is associated with a pileup PV, passing the above quality requirements, it is

– 11 –

2017 JINST 12 P02014

10

10

0

30

## PDF page 15

Pileup jet identification. In addition to diffuse energy, PU interactions often generate soft jets with
pT of a few GeV. Overlaying multiple PU interactions in a single beam-crossing leads to nonnegligible probability of two or more of these soft jets overlapping, resulting in hard jets of tens of GeV in pT ,
far above the average PU pT density. These overlaps are referred to as pileup jets, which are particularly problematic for physics analyses as they can pass typical jet pT requirements, e.g., pT > 30 GeV.
The pileup jets lack the relatively hard core typically found in hard-scattering jets, and can be identified by using a multivariate analysis (MVA) of the jet shape variables and the fraction of charged
particles contributed by pileup vertices. This MVA tool is called PUJetID, can be run on jets with
or without CHS, and it is documented in ref. [44]. For jets in the region |η| < 2.5 and pT > 30 GeV,
the PUJetID efficiency for hard-scattering jets is around 99%, at a pileup-rejection of 90 − 95%.
Removing pileup jets can improve the performance of physics analyses, but applying PUJetID
has no direct impact on the JEC. PUJetID is currently not used in the JEC measurements to avoid
biases arising from the occasional removal of soft jets from the hard-scattering vertex, which affects
the ISR+FSR correction. Instead, CHS is used, which indirectly removes most of the jets tagged by
PUJetID by significantly lowering their pT .
4.3

Hybrid jet area method

The jet area method uses the effective area of the jets multiplied by the average energy density in
the event to calculate the offset energy to be subtracted from the jets. This method was introduced
in ref. [33] and was first used on data in ref. [13] with slight modifications to account for the
oversubtraction of the underlying event (UE) and for the η-dependence of the offset. This slightly

– 12 –

2017 JINST 12 P02014

considered a pileup track, and removed in the CHS procedure. All other tracks, including those not
associated with any PV, are kept.
The CHS can remove approximately 50% of IT PU within the tracker coverage, as illustrated
later by the solid red component labeled “charged hadrons” in figures 6 and 7. The remaining
unassociated charged hadrons are either not pointing to any reconstructed vertex, or are associated
with a vertex that did not pass all the quality requirements, or have too large χ2 /Ndof for robust
vertex association. The vertex reconstruction and identification inefficiency is about 30% for pileup
vertices, and it is responsible for a large proportion of the unassociated tracks from pileup.
The charged hadrons from PU are typically soft and have an exponentially decreasing pT
distribution, with ⟨pT ⟩ ≈ 0.5 GeV [42]. Many of the unassociated hadrons in contrast have much
higher pT and are often coming from the leading primary vertex, but have too high χ2 /Ndof for
robust vertex association. This is particularly common for tracks that are of high pT and therefore
very straight and have merged pixel hits within dense jet cores. For jets of several hundred GeV
the tracking efficiency within the jet core can fall as low as 60%, with a correspondingly large
increase of the fraction of unassociated tracks. Future improvements of CHS aimed at removing a
higher proportion of pileup tracks, e.g., with more efficient track-vertex association, must therefore
maintain a very low misreconstruction rate for tracks from high-pT jets, or also consider the pT and
local environment of the tracks, as done with the pileup per particle ID (PUPPI) method [43].
The PU offset subtraction has been derived with and without CHS, and the later stages of JEC
are practically identical after the application of the corresponding offset corrections. Application
of CHS improves the jet pT resolution, however, as discussed in section 8.

## PDF page 16

(
)]
ρ0 (η) + ρ β(η) 1 + γ(η) log(pT, uncorr ) A j
Chybrid (pT, uncorr, η, A j , ρ) = 1 −
.
pT, uncorr
[

(4.2)

The input parameters are pT, uncorr , jet pseudorapidity η, jet area A j , and the per-event pT offset
density ρ. In this formula the parameters ρ0 (η), β(η), and γ(η) introduce the required shaping of
the offset versus η. There is no explicit correction for the UE density ρUE as in ref. [13], but that
term is effectively absorbed into ρ0 (η). Because ρ → ρUE and Chybrid → 1 when µ → 0, we have
ρ0 (η) = −ρUE β(η) at pT,uncorr → 1 GeV in the ideal situation. The multiplicative factor, β(η),
corrects for the nonuniformity of the IT and OOT PU offsets versus η, and the residual correction
factor, γ(η), adds their logarithmic jet pT dependence.
The parameters ρ0 (η), β(η), and γ(η) are determined from the simulated particle-level offset,
and the offset scale factor for the ρ0 (η) and β(η) in data is determined using the random cone
method in zero-bias data, as discussed in the following. The ρ0 (η) parameter effectively contains
the ρUE for the QCD multijet sample, while β(η) and γ(η) parameterize the pythia 6.4 MinBias
overlay, which matches data well. The RC method consists of reconstructing many jets in each
event, clustering particles in randomly placed cones, effectively mapping all the (η, φ) space. The
average pT of these jets is a measurement, in each event, of the average energy density that gets
clustered in a jet. When the method is applied in events with no contribution from hard scattering,
as it is the case for zero-bias events, the main contributions to the jet energies come from noise and
pileup. Assuming the noise energy contribution to be negligible with respect to the pileup one, the
average pT of the jets as measured from the RC method indicates the average energy offset due to
pileup, for the considered jet algorithm and jet distance parameter.
Simulated particle-level offset. In simulation, the most direct way to calculate the particlelevel offset in jet pT caused by pileup is to reconstruct the same events with and without pileup
overlay and match the reconstructed jets between these samples. This is done on a QCD multijet
sample generated with pythia 6.4, tune Z2*. Some care needs to be taken to reproduce the same
signal fluctuations as before the overlaying pileup, to avoid random smearing of jet pT between
these two samples. All measurements are binned in µ to decouple pileup reweighting from offset
measurement, and to effectively incorporate the correct average amount of OOT PU in the offset
correction (OOT and IT PU are correlated through the shared Poisson mean µ). The µ bins are
then mapped to the average measured value of ⟨ρ⟩ for parameterizing the correction. Similarly, the
pT dependence of the offset is measured in bins of particle jet pT (pT, ptcl ) to decouple the offset

– 13 –

2017 JINST 12 P02014

modified version is referred to as the hybrid jet area method, where the “hybrid” in the name derives
from the fact that this method combines an η-dependent average offset O(η) correction versus NPV ,
as already used at the Tevatron [16], with the original η-independent jet area method using only
offset pT density ρ and jet area A j . This is effectively done by replacing (NPV − 1)O(η) in the
Tevatron method with ( ρ − ρUE )( β(η) A j ), where each of the terms NPV and ρ, −1 and −ρUE , and
O(η) and β(η)⟨A j ⟩ have the same basic meaning, which will be detailed in the following.
In this paper we further extend the hybrid method by adding a logarithmic jet pT dependence.
The previous separate UE correction is absorbed in the new η-dependent constant term. The full
correction formula used as a multiplicative factor for the uncorrected jet transverse momentum
pT,uncorr at CMS is

## PDF page 17

12
10

〉 (GeV)

Simulation

Anti-kT, R=0.5 (PF+CHS)
|η|<1.3
0 ≤ µ < 10
10 ≤ µ < 20
20 ≤ µ < 30
30 ≤ µ < 40
0 ≤ µ < 40

8

(8 TeV)

1.4
1.2

T,offset

14 CMS

〈p

〈p

T,offset

〉 (GeV)

(8 TeV)

CMS
Simulation

1
0.8
0.6

Anti-kT, R=0.5 (PF+CHS)
|η|<1.3
0 ≤ µ < 10
10 ≤ µ < 20
20 ≤ µ < 30
30 ≤ µ < 40
0 ≤ µ < 40

0.4

6

0.2

4

0

0

-0.4
20 30

100 200

1000

pT, ptcl (GeV)

-0.6

20 30

100 200

1000

pT, ptcl (GeV)

Figure 5. Simulated particle-level offset ⟨pT,offset ptcl ⟩ defined in eq. (4.3) (left), and residual offset after
correcting for pileup with eq. (4.2) (right) for |η| < 1.3, versus particle jet pT , for different values of average
number of pileup interactions per bunch crossing ⟨µ⟩.

from the pT spectrum and JER, before mapping to the average uncorrected measured ⟨pT,uncorr ⟩ for
parameterization.
We define the particle-level offset ⟨pT,offset ptcl ⟩ as the average difference in pT between matched
jets in simulated samples with and without pileup overlay:
[
]
[ ]
⟨pT,offset ptcl ⟩(⟨ρ⟩, η , ⟨pT,uncorr ⟩) = ⟨pT,with PU − pT,without PU ⟩ µPU, η, pT, ptcl .

(4.3)

The square brackets [ ] denote the binning variables, while the angle brackets ⟨ ⟩ denote the
averages within those bins for the variables that are used to parameterize the corrections. This subtle
distinction is made explicit here due to its importance for various observational biases, and due to
the fact that the binning and parameterization variables are not the same. To have an unambiguous
particle-level reference, both reconstructed jets are required to match the same particle jet within a
distance less than ∆R < R/2, where R is the jet distance parameter. The matching efficiency for
jets in the without-PU sample to jets in the with-PU sample for ⟨µ⟩ = 20 is better than 80% (98%)
for jets of pT > 10 (30) GeV. In the with-PU sample there is also a large fraction of unmatched jets
with pT < 60 GeV that are due to pileup.
The simulated particle-level offset ⟨pT,offset ptcl ⟩ is parameterized as a function of offset density
ρ and jet η, pT,uncorr and area A j to obtain the ρ0 (η), β(η) and γ(η) used in eq. (4.2), where
Chybrid = 1 − ⟨pT,offset ptcl ⟩/pT,uncorr. . The particle-level simulated offset versus particle jet pT is
shown in figure 5 (left) for |η| < 1.3. The relative slope in offset is parameterized by a logarithmic
pT dependence and is reasonably independent of the level of pileup in the event, while the offset
versus ρ is assumed linear. The resultant level of pileup after applying the corrections is presented
in figure 5 (right), showing the effect of the subtraction. The results are consistent with the absence
of additional pileup energy within about 0.2 GeV for the full sample. For µ > 30, small residual
offset is visible due to a small unparameterized quadratic dependence of offset on ρ.

– 14 –

2017 JINST 12 P02014

-0.2
2

## PDF page 18

0.7
0.6

Anti-kT, R=0.5 (PF+CHS)
|η|<1.3
Photons
Neutral hadrons
Unassoc. ch. hadrons
Charged hadrons

0.5
0.4

Simulation

0.7
0.6

η = 0.0, PF
p
= 100 GeV
T,ptcl
p
= 50 GeV
T,ptcl
p
= 30 GeV
T,ptcl
p
= 10 GeV
T,ptcl
Random cone

0.5

〈p

0.3

0.8 CMS

j

0.8

CMS
Simulation

〉 / (〈µ〉 × A ) (GeV)

0.9

(8 TeV)

T,offset

〉/〈µ〉 (GeV)

T,offset

〈p

(8 TeV)

1

0.4

0.1
0

20 30 40

100

0.3

200

pT,ptcl (GeV)

0.2 0.3 0.4 0.5 0.6 0.7 0.8 0.9

1

R

Figure 6. Simulated particle-level offset versus pT separately for each type of PF candidate (left). Average
pT offset density versus jet distance parameter R for various pT,ptcl compared to a random-cone offset density
versus cone radius (right). The jet or cone area A j corresponds to πR2 .

Figure 6 (left) shows the pT dependence of the offset for each PF candidate type. The ⟨pT,offset ⟩ is
divided by the average number of pileup interactions, hence showing the average offset per additional
interaction. While the reconstruction thresholds for charged hadrons and photons are of the order
of a few hundred MeV, the effective detector reconstruction thresholds for neutral hadrons (mostly
KL0 , KS0 , and neutrons) are of the order of 3 GeV. This is far above the typical ⟨pT,offset ⟩ ≈ 5 GeV
for a pileup particle, making the neutral hadron contribution barely visible in figure 6 (left). The
observed pT dependence comes from an interplay of several effects for overlapping particles, such
as failed zero-suppression in calorimeter energy, nonlinearity of PF hadron corrections, fake tracks
arising from hit combinations, and misreconstructed tracks arising from pixel hit merging and
tracker dynamic inefficiency at high µ. The rate of overlaps is highest in the jet core, which results
in the simulated offset correction depending on the jet size. Figure 6 (right) shows the average
offset density within the jet versus jet distance parameter R and jet pT . The simulated particle-level
offset converges to an RC offset measurement at low pT , as well as for large jet size parameters. The
shallow slope in RC offset versus distance parameter is due to vector summation of PF candidate
momenta, which reduces the offset pT relative to the offset energy by cos(∆R) at the cone edges.
Offset scale factor. The offset data/simulation scale factor is estimated from zero-bias data and
simulation using the RC method [13]. Because zero-bias data contain no energy deposition from
hard interactions, and the noise contribution is small, the average transverse momentum ⟨pT,cone ⟩(η)
of PF candidates in a randomly placed cone centered at (η, φ) can be identified with the average
offset due to pileup, ⟨pT,offset ⟩RC (η):
⟨pT,offset ⟩RC (η, ⟨ρ⟩) = ⟨pT,cone ⟩[η, µ].

(4.4)

As in the case of the simulated particle-level offset, the parameterization variables (η, ⟨ρ⟩) and
the binning variables [η, µ] are explicitly marked in order to signal their impact on the observational
biases.

– 15 –

2017 JINST 12 P02014

0.2

## PDF page 19

Markers: Data, Histograms: MC

1 CMS
0.8

Photons
EM deposits
Neutral hadrons
Hadronic deposits
Unassoc. charged hadrons
Charged hadrons

Anti-kT R=0.5
<µ> = 19

0.6

〈p

T,offset

〉 / 〈µ〉 (GeV)

19.7 fb-1 (8 TeV)

0.4

Data/MC

-5

-4

-3

-2

-1

0

1

2

3

4

5

1

2

3

4

η

PF
PF+CHS

1.2
1

-5 -4 -3 -2 -1 0

5

Figure 7. Random-cone offset measured in data (markers) and MC simulation (histograms) normalized by
the average number of pileup interactions ⟨µ⟩, separated by the type of PF candidate. The fraction labeled
‘charged hadrons’ is removed by CHS. The ratio of data over simulation, representing the scale factor applied
for pileup offset in data, is also shown for PF and PF+CHS.

For deriving the offset scale factor, the RC measurement is fitted with a quadratic function of ρ,
⟨pT,offset ⟩RC = p0 +p1 ρ+p2 ρ2 . The constant and quadratic terms are small, but are required for a good
χ2 /Ndof of the fit. The constant term has usually a small positive value, because the mean ⟨pT,cone ⟩
can still have a small nonzero value when the median ρ is already zero. This low-PU behavior of ρ is
discussed in ref. [45]. The offset scale factor for parameters ρ0 (η) and β(η) in eq. (4.2) is defined as
⟨pT,offset ⟩RC
data (η, ⟨ρ⟩data )
⟨pT,offset ⟩RC
MC (η, ⟨ρ⟩MC )

.

(4.5)

Using different ⟨ρ⟩ working points for data and simulation is necessary due to the slight
difference of about 4% in ⟨ρ⟩ between data and simulation, seen in figure 3 (right).
The offsets in data and simulation are shown in figure 7 (top), separated by PF candidate type.
The offset scale factor for PF and PF+CHS is shown in figure 7 (bottom). The offset scale factor at
|η| < 2.4 is less than 5%, but increases up to 20% outside of the tracking coverage near the inner
edge of HF at η ≈ 3.2. The triangular shape is caused by smearing sharp detector effects over a
cone area within ∆η < 0.5. The uncertainty from varying the ⟨ρ⟩ working point within the 68%
confidence interval of the ρ distribution is less than 2% up to |η| < 4.7.
4.4

Pileup offset correction uncertainties

The pileup offset correction uncertainties come from two main sources: uncertainty in the offset
scale factor used for the η dependence in data, and uncertainty in the offset jet pT dependence that is

– 16 –

2017 JINST 12 P02014

0.2

## PDF page 20

derived from simulation only. The former uncertainty is evaluated by varying the ⟨ρ⟩ working point
used for deriving the offset scale factor within one standard deviation of the ρ distribution, while
the latter is evaluated using the difference between the simulated particle-level offset and the RC
offset. Of these, the jet pT dependence is the dominant uncertainty across most of the phase space.
Any residual pileup offset is absorbed on average, within the constraints of their respective
parameterizations, by the relative η and absolute pT corrections derived from dijet, Z+jet, γ+jet
and multijet data. Therefore the dominant pT -dependence uncertainty is propagated through the fit
procedure used in the data-based methods to account for this reduction and shaping of pileup offset
correction uncertainties. This results in a set of five uncertainty sources:

• PileUpPtEta (Eta=BB,EC1,EC2,HF) results from the propagation of the PileUpEnvelope
uncertainty through the η-dependent correction evaluation from dijet balance. This uncertainty accounts for the residual difference between the PileUpEnvelope with shape
(p0 + p1 log(pT ))/pT and the η-dependent correction fit in the range of dijet data at
60 < pT < 2000/ cosh(η) GeV with shape p0 + p1 log(pT ).
• PileUpPtRef results from the propagation of the PileUpEnvelope uncertainty through the
evaluation of the absolute-scale pT dependence from Z/γ+jet and multijet data. This uncertainty accounts for the residual difference between the PileUpEnvelope and the absolute-scale
fit in the range of Z/γ+jet and multijet data at 30 < pT < 1000/ cosh(η) GeV.
• PileUpDataMC accounts for uncertainty in the offset scale factor for data, based on variation
of the ⟨ρ⟩ working point within one standard deviation of the ρ distribution.
• PileUpMuZero is evaluated from the nominal result of the fit for η- and pT -dependent databased corrections, and accounts for the bias that results from deriving them at ⟨µ⟩ ≈ 20 instead
of ⟨µ⟩ ≈ 0. This uncertainty is to be used for zero-pileup data (⟨µ⟩ ≈ 0, e.g., in the 2.76 TeV
data collected in 2013) and replaces PileUpPtEta, PileUpPtRef and PileUpDataMC.
The pileup offset correction uncertainties are summarized in figure 8. The dominant
uncertainty is from the residual jet pT dependency remaining after the application of the data-based
methods. It is at the level of 1% for pT = 30 GeV, and rapidly decreases to the 10−3 level in the
range constrained by the data-based methods. There is a small increase in uncertainty again at
high pT outside the range of data-based methods, where the constrained parameterizations used for
data-based residuals result in a small seesaw effect. The uncertainty for ⟨µ⟩ = 0 data is in many
cases similar or even larger than for ⟨µ⟩ = 20, owing to the absorption of the residual offset into
relative η and absolute pT corrections at pT > 30 GeV.

– 17 –

2017 JINST 12 P02014

• PileUpEnvelope is taken as 30% of the difference between simulated particle-level offset and
RC offset. This is the pileup uncertainty we would have if the later calibrations did not reduce
the uncertainty. It is not directly included in the JEC uncertainties, but is propagated through
the relative η and absolute pT corrections to give the uncertainties PileUpPtEta, PileUpPtRef
(for ⟨µ⟩ ≈ 20 data) and PileUpMuZero (for ⟨µ⟩ = 0 data), described below.

## PDF page 21

2

R=0.5 PF+CHS
p = 30 GeV
T

1.5

JEC uncertainty (%)

2.5

SubTotalPileUp
PileUpPtEta
PileUpPtRef
PileUpDataMC
PileUpMuZero (opt)

CMS
2.5
2

0.5

0

3

CMS
2.5
2

R=0.5 PF+CHS
|η | = 2.7
jet

2

4

0

η

100 200

1000

p (GeV)

19.7 fb-1 (8 TeV)

19.7 fb-1 (8 TeV)

SubTotalPileUp
PileUpPtEta
PileUpPtRef
PileUpDataMC
PileUpMuZero (opt)

T

3

CMS
2.5
2

1

0.5

0.5

100 200

0

1000

p (GeV)

R=0.5 PF+CHS
|η | = 3.5
jet

SubTotalPileUp
PileUpPtEta
PileUpPtRef
PileUpDataMC
PileUpMuZero (opt)

1.5

1

20

20

jet

1.5

0

jet

20

100 200

1000

p (GeV)

T

T

Figure 8. Pileup offset correction uncertainties for the average 2012 (8 TeV) conditions for PF jets with
CHS and R = 0.5 as a function of η jet for fixed pT = 30 GeV (top left) and as a function of jet pT (top
right, and bottom panels). The plots are limited to a jet energy E = pT cosh η = 4000 GeV so as to show
only uncertainties for reasonable pT in the considered data-taking period. PileUpMuZero is an optional
alternative uncertainty for zero-pileup (⟨µ⟩ ≈ 0) events, and it is therefore not included in the quadratic
sum SubTotalPileUp. It accounts for the pileup uncertainty absorbed in the residual response corrections at
⟨µ⟩ ≈ 20, which is particularly prominent at 1.5 < |η| < 3.

4.5

Summary of pileup offset corrections

The pileup offset corrections for the anti-k T algorithm (R = 0.5) with and without charged-hadron
subtraction are summarized in figure 9 for typical 2012 (8 TeV) conditions of ⟨µ⟩ ≈ 20, compared to
corrections for 7 TeV data taken in 2010 and 2011. The average pileup per interaction for R = 0.5 is
about 0.5 GeV, adding up to a total of about 10 GeV per jet. This results in a typical offset correction
of about 0.75 for a pT,corr = 30 GeV (pT,uncorr = 40 GeV) jet. The CHS removes approximately half
of this offset before jet clustering by matching tracks to pileup vertices, reducing the residual offset

– 18 –

2017 JINST 12 P02014

0.5
−2

R=0.5 PF+CHS
|η | = 0

SubTotalPileUp
PileUpPtEta
PileUpPtRef
PileUpDataMC
PileUpMuZero (opt)

1.5
1

−4

19.7 fb-1 (8 TeV)

3

1

JEC uncertainty (%)

JEC uncertainty (%)

CMS

0

JEC uncertainty (%)

19.7 fb-1 (8 TeV)

3

## PDF page 22

1.2
1.1

CMS

R = 0.5, PF
20 fb-1 (8 TeV)
5 fb-1 (7 TeV)
36 pb-1 (7 TeV)

|η| = 0
〈µ〉 = 20.0

1
0.9
0.8

1.3
1.2
1.1

-1

1.3
1.2
1.1

0.5
0 0.5 1 1.5 2 2.5 3 3.5 4 4.5 5

1000

|η|

(GeV)

-1

-1

19.7 fb (8 TeV) + 4.9 fb (7 TeV)

1.4

CMS
|η| = 0

R = 0.5, PF+CHS
20 fb-1 (8 TeV)
5 fb-1 (7 TeV)

〈µ〉 = 20.0

1
0.9
0.8

1.3
1.2
1.1

T,corr

T,corr

= 30 GeV

〈µ〉 = 20.0

0.8

0.6

p

p

R = 0.5, PF+CHS
20 fb-1 (8 TeV)
5 fb-1 (7 TeV)

0.9

0.6
100 200

CMS

1

0.7

20

-1

19.7 fb (8 TeV) + 4.9 fb (7 TeV)

1.4

0.7

0.5

= 30 GeV

0.5
0 0.5 1 1.5 2 2.5 3 3.5 4 4.5 5

1000

|η|

(GeV)

Figure 9. Pileup offset correction Chybrid including data/MC scale factors, with systematic uncertainty band,
for the average 2012 (8 TeV) conditions of ⟨µ⟩ = 20 for PF jets without CHS and R = 0.5 at |η| = 0 versus
pT,corr (top left), and at pT,corr = 30 GeV versus |η| (top right), compared to corrections for 2010 [13] and
2011 [46] data at 7 TeV after extrapolation to similar pileup conditions. The same results are also shown for
PF jets with CHS and R = 0.5 at |η| = 0 versus pT (bottom left), and at pT,corr = 30 GeV versus |η| (bottom
right), compared to corrections for 2011 data at 7 TeV [46].

correction to about 0.85 at pT,corr = 30 GeV (pT,uncorr = 35 GeV). Roughly one third of the remaining
pileup is from PF charged hadrons that have not been matched to good pileup vertices, and much
of the rest is from PF photons. The CHS algorithm was only fully commissioned at 7 TeV in 2011,
and the 2010 (7 TeV) version of the offset corrections did not yet take into account the remaining
unmatched pileup tracks. Therefore only results without CHS are shown for 7 TeV in 2010.
The pileup offset corrections have been relatively stable over time at 7 TeV in 2010 and 2011,
when scaled to similar pileup conditions. This is in part due to the good linearity of the offset
corrections for PF and continuous development on the detector side to reduce OOT PU in the
calorimeters, and in part due to the adaptability of the jet area method to the prevailing pileup offset.

– 19 –

2017 JINST 12 P02014

T,corr

T,corr

〈µ〉 = 20.0

0.8

0.6

p

p

R = 0.5, PF
20 fb-1 (8 TeV)
5 fb-1 (7 TeV)
36 pb-1 (7 TeV)

0.9

0.6
100 200

CMS

1

0.7

20

19.7 fb-1 (8 TeV) + 36 pb-1 + 4.9 fb-1 (7 TeV)

1.4

0.7

0.5

Pileup offset correction

Pileup offset correction

1.3

19.7 fb-1 (8 TeV) + 36 pb-1 + 4.9 fb-1 (7 TeV)

Pileup offset correction

Pileup offset correction

1.4

## PDF page 23

5

Simulated response corrections

The simulated response corrections are derived and applied on jets that have been corrected for pileup
offset. The CMS detector simulation contains a detailed model of the detector geometry, data-based
alignment and calibration of the detector elements, and emulation of the readout electronics. It is
based upon the Geant4 package [18] that simulates the evolution of the electromagnetic (EM) and
hadronic showers and their interactions with the detector material. In addition, the pythia 6.4 tune
Z2* event generator is used to simulate the fragmentation of the initial quarks and gluons. Together
these two components provide an accurate and detailed description of the jet response, which is used
for the bulk of the JEC. Data-based methods (section 6) are needed only for small residual corrections
on top of the simulated response and the simulated offset corrections discussed in section 4.
The benefit of relying heavily on simulation to derive the jet response is that we are not sensitive
to many of the biases inherent in the data-based methods and can cover corners of phase space that
are not easily accessible in data. This includes samples of jets with very low (pT < 30 GeV) and
very high (pT > 1 TeV) momenta, heavy-flavor jets, and samples with particularly low (µ < 5) and
high (µ > 40) pileup. Describing jet response in terms of variables accessible in simulation also
facilitates the understanding of data-based methods, as we can better model the correlation between
various samples and corrections. For the following discussion, jets are assumed to be corrected for
the pileup offset as described in section 4.
Sample definitions
We derive the simulated response from a QCD multijet sample of 10 million events generated with
pythia 6.4 tune Z2*. To ensure event generation with efficient coverage of the full kinematic phase
space at the LHC with small statistical uncertainty, the events are generated with a flat pT spectrum
and reweighted by p̂T−4.5 , where p̂T is the transverse momentum of the generated 2 → 2 hard process,
which allows the recovery of the original pT spectrum in pythia 6.4 and the production of unbiased
results for pT, jet > 30 GeV. The generated and simulated events are overlaid with pileup generated

– 20 –

2017 JINST 12 P02014

The largest differences are visible in the 2.5 < |η| < 3.0 region, where OOT PU increased at 7 TeV
in 2011, but was again brought down in ECAL at 8 TeV in 2012 using more advanced reconstruction
algorithms. The OOT PU is also partially responsible for the 2011–2012 differences in the endcaps
within tracker coverage of 1.5 < |η| < 2.5, and for differences between 2010 and 2011–2012 in
the barrel at |η| < 1.5. In addition, the JEC were improved at 7 TeV in 2011 to take into account
the difference between the offset outside jets (RC offset) and inside jets (particle-level offset). This
increased the offset correction inside the tracker coverage (failed zero-suppression), and lowered it
outside (calorimeter response nonlinearity), compared to the 2010 (7 TeV) corrections.
The pileup uncertainties have been steadily reduced despite rapidly increasing pileup. This can
be credited to improvements in the correction methods, more events at high pileup to determine the
trends versus pileup, and a reduction of double counting. The 2012 (8 TeV) corrections explicitly
take into account the additional constraints from data-based methods, which reduce the offset
uncertainty in the endcaps by up to 50% for PF+CHS at pT,corr = 30 GeV compared to 7 TeV in
2011. The dominant systematic uncertainty is from the pT dependence of the pileup offset, which
is only indirectly constrained by data.

## PDF page 24

by pythia 6.4 tune Z2*, with events reweighted such that the pileup distribution matches that found
in data.
To estimate pileup offset in jets, we simulate the same generated events also without additional
pileup overlay, as was discussed in section 4. To estimate the jet response dependence on the
fragmentation model and jet flavor, a complementary sample is produced with herwig++ 2.3
tune EE3C. To estimate the jet response dependence on the detector calibration, we also produce
additional samples with the CMS fast simulation.
Definition of simulated particle response

Rptcl (⟨pT ⟩, η) =

⟨pT ⟩
[pT, ptcl, η],
⟨pT, ptcl ⟩

(5.1)

in bins of particle-level pT (pT, ptcl ) and reconstructed η (where pT is the transverse momentum
of the reconstructed jet). As in the previous sections, the square brackets [ ] denote the binning
variables, and the angle brackets ⟨ ⟩ indicate the averages within those bins for the variables that are
used to parameterize the response.
5.1

Corrections versus η and pT

Simulated anti-k T jets, with a distance parameter R = 0.5, are used to study the detector response
as a function of the jet pT . The simulated particle response is shown in figure 10 (left) as a function
of the reconstructed jet η. The simulated particle response after JEC is shown in figure 10 (right)
as a function of the particle-level jet pT, ptcl in various η regions. The results show that the response
is corrected to within 0.5% with respect to the particle-level jet, for pT from about 20 GeV to 2 TeV.
5.2

Dependence on the jet size

The dependence of the jet response on the jet distance parameter R has been checked in the range
R = 0.3–1.0. The response is similar after accounting for the increasing PU offset due to the larger
jet area (Ajet ≈ πR2 ). Smaller effects come primarily from two sources:
• The UE energy within the jet has lower response than the energy from the hard scattering,
lowering the response at low pT for jets with large R.
• A larger distance parameter averages the jet response over a larger area, smearing sharp
features in the detector response versus η.
Figure 11 (left) shows the comparison of the JEC factor for various jet sizes at pT = 30 GeV. As
expected from the larger fraction of UE energy, the corrections rise slightly for larger distance
parameters. The very small distance parameter R = 0.3 is an exception to this rule, because
the detector granularity smears some energy out of the cone. These differences mostly disappear

– 21 –

2017 JINST 12 P02014

A particle-level jet is matched to the closest reconstructed jet if it is within half of the jet distance
parameter R. For a distance parameter of R = 0.5 this corresponds to 0.25. The method ensures
a high matching efficiency (reaching 100% around pT = 30 GeV) and provides a unique match for
the anti-k T jets. In the present paper, the simulated particle response Rptcl is defined as the ratio of
arithmetic means of matched reconstructed and particle-level jets transverse momenta,

## PDF page 25

1.2
1.1

(8 TeV)

2012 JES: Anti-kT R = 0.5, PF+CHS
Barrel
BB

Endcap
EC1
EC2

Forward
HF

1.04

CMS
Simulation

1.03

QCD Monte Carlo
Anti-kT R=0.5, PF+CHS

1.02

1
0.9

1.01
1

0.99

0.8

p = 10 GeV
T
p = 30 GeV
T
p = 100 GeV

0.97

p = 400 GeV
T
p = 2000 GeV

0.96

T

T

0.95

0.5
0 0.5 1 1.5 2 2.5 3 3.5 4 4.5

Jet |η|

20

100 200

1000

pT, ptcl (GeV)

Figure 10. Simulated jet response Rptcl versus |η| for R = 0.5 (left). Simulated jet response Rptcl , after JEC
have been applied, versus pT, ptcl for R = 0.5 in various η regions, and with statistical uncertainties (right).

at higher pT for R ≥ 0.4, with the smaller jet sizes showing slightly sharper detector features.
Simulated jet responses after the application of the JEC are shown in figure 11 (right) as a function
of jet pT for a range of distance parameters from 0.3 to 1. The response is consistent with unity
within 1% for pT ≳ 30 GeV. During Run 1 of the LHC, the supported jet size parameters in pp
collisions were R = 0.5 and R = 0.7. The full jet energy corrections and uncertainties were derived
and provided centrally only for these two jet size parameters.
5.3

Detector simulation uncertainties

We evaluate several systematic uncertainties using simulation, with the uncertainties further constrained using data-based methods, as discussed later. We discuss here the uncertainties arising
from the propagation of detector calibration uncertainties to the jet response. The effects of jet
fragmentation and flavor response are discussed in section 7.3. Because the jet response is later
constrained using measurements based on data, these systematics are explicitly set to zero at certain
reference points, discussed in section 6. They are then used to extrapolate the systematics from
these reference points to regions of the phase space not directly calibrated with data.
Single-pion response. The jet response is sensitive to the underlying detector calibrations. The
CMS calorimeters have been calibrated in test beam studies, and the single-pion response (SPR) has
subsequently been checked on proton-proton data with charged pions [47], confirming good modeling of the barrel response in simulation to within ±3%. Because the PF reconstruction relies heavily
on tracking for low-pT jets, the sensitivity to the detector calibration is strongly reduced compared to
the calorimeter-only reconstruction. To show this effect, the ratio of the response when varying the
SPR with respect to the nominal response is shown in figure 12, for jets reconstructed with the PF
algorithm and for jets reconstructed with only calorimetric energy deposits, both using the anti-k T
algorithm. For this study, the SPR has been propagated to the JEC using the CMS fast simulation.

– 22 –

2017 JINST 12 P02014

|η| < 1.3
1.3 < |η| < 2.5
2.5 < |η| < 3.0
3.0 < |η| < 5.0

0.98

0.7
0.6

(8 TeV)

1.05

Corrected response

Simulated jet response

CMS

## PDF page 26

Corr. factor

(8 TeV)

1.5

CMS
1.45 Simulation
1.4
1.3

T

R=0.3

R=0.4

R=0.5

R=0.7

1.25

QCD Monte Carlo
Anti-kT (PF+CHS)
|η| < 1.3

CMS
Simulation

1.04

1.2

1.02

1.15

1.05

1

0.98

1.05
0.96

1

0.95

-4 -3 -2

-1

0

1

2

3

0.94

4

R=0.3

R=0.4

R=0.7

R=1.0

20

100 200

η

R=0.5

1000

pT,ptcl (GeV)

Figure 11. Jet energy correction factors for a jet with pT = 30 GeV, as a function of η and for various jet
sizes R (left). Simulated jet energy response Rptcl after JEC for |η| < 1.3 as a function of the particle-level
jet pT for various jet sizes R (right).

At low pT , PF is directly sensitive to SPR only through neutral hadrons, which on average
contribute 15% of the jet energy at particle level, leading to a sensitivity of about 0.5% for a simultaneous change of ±3% in both ECAL and HCAL SPR. At high pT the PF performance approaches
that of the calorimetric reconstruction, because the tracking efficiency drops in the dense jet core and
the leading tracks become too straight for a reliable pT measurement. Since 25% of the jet energy is
deposited as photons (section 10), the JEC sensitivity to a ±3% change in SPR is at most 2.3%. The
sensitivity to changes in SPR has been also studied separately for a 3% change in the response of the
ECAL and HCAL, as shown in figure 13. The results are qualitatively similar to an overall change in
SPR, but show larger sensitivity to the SPR in HCAL at high pT . This is because hadronic showers
become deeper for high-pT particles, and deposit a larger fraction of their energy in the HCAL.
5.4

Jet energy corrections propagation to missing transverse momentum

The jet energy corrections are propagated to p⃗Tmiss by using the so-called type-I correction:
∑
∑
∑
miss
miss
i
i
⃗i ,
p⃗T,typeI
= p⃗T,uncorr
+
p⃗T,uncorr
−
p⃗T,corr
−
O
RC
i

i

(5.2)

i

miss
where p⃗T,uncorr
is the uncorrected p⃗Tmiss , p⃗T,uncorr is the uncorrected jet pT , p⃗T,corr is the fully
⃗ i is the average offset due to pileup, as obtained with the RC method (see
corrected jet pT , and O
RC

section 4.3). The sum runs over all jets with pT,corr > 10 GeV in the event. Including the average
RC offset underneath jets in the missing transverse momentum vector sum ensures that the pileup

– 23 –

2017 JINST 12 P02014

1.1

Ratio to R=0.5

(8 TeV)

1.06

R=1.0

Corrected response

1.35

QCD Monte Carlo
Anti-kT (PF+CHS)
p = 30 GeV

## PDF page 27

Response ratio

(8 TeV)

1.05 CMS
1.04 Fast simulation

PFJet SPR +3%
PFJet SPR -3%
CaloJet SPR +3%
CaloJet SPR -3%

1.03
1.02
1.01
1
0.99
0.97
0.96

|η| < 1.3
Anti-kT R=0.5

40

100

200

1000 2000

p (GeV)
T

Figure 12. Changes in PF jet and calorimeter jet response resulting from ±3% variations of single-pion
response in parameterized fast simulation in HCAL+ECAL.
(8 TeV)

Response ratio

Response ratio

(8 TeV)

1.05 CMS
1.04 Fast simulation

PFJet ECAL +3%
PFJet ECAL -3%
CaloJet ECAL +3%
CaloJet ECAL -3%

1.03
1.02
1.01

1.05 CMS
1.04 Fast simulation
1.03
1.02
1.01

1

1

0.99

0.99

0.98

0.98

0.97
0.96

0.97

|η| < 1.3
Anti-kT R=0.5

40

100

0.96
200

1000 2000

p (GeV)

PFJet HCAL +3%
PFJet HCAL -3%
CaloJet HCAL +3%
CaloJet HCAL -3%

|η| < 1.3
Anti-kT R=0.5

40

100

200

1000 2000

p (GeV)

T

T

Figure 13. Changes in PF jet and calorimeter jet response resulting from ±3% variations of single-pion
response in parameterized fast simulation in ECAL (left), and HCAL (right).

offset remains isotropic and does not bias p⃗Tmiss . The type-I correction is recommended for physics
analyses and is used in most CMS results, as well as for deriving residual JEC for data.
5.5

Summary of simulated response corrections

The simulated particle response corrections are summarized in figure 14 for data collected at 8 TeV
and compared to corrections for 7 TeV data taken in 2010 and 2011. At low pT , the JEC rise
toward 1.15 due to the 15% neutral hadron energy that largely falls below calorimeter thresholds.
The response is quite flat at pT > 50 GeV, where the competing effects of increasing calorimeter

– 24 –

2017 JINST 12 P02014

0.98

## PDF page 28

6

Residual corrections for data

The residual data/simulation scale factors for JEC are determined after correcting jets for pileup and
simulated particle response. For consistency, the variations of the jet momenta due to corrections
for pileup and simulated response are propagated to the p⃗Tmiss definition à la eq. (5.2). The residual
corrections for data are first determined with a sample of dijet events with low statistical uncertainty,
where the response of jets over a wide range of pT is corrected relative to the one of jets with
|η| < 1.3, and then with a combination of Z(→ µµ)+jet, Z(→ ee)+jet, γ+jet, and multijet events
for jets with |η| < 1.3 from a pT of around 30 GeV to 1 TeV. The basic idea, in all the considered
topologies, is to exploit the transverse momentum balance, at hard-scattering level, between the jet
to be calibrated and a reference object: a jet energy scale different from unity generates imbalance
at the reconstructed level.
The jet energy response is studied using the pT balance and MPF (missing transverse momentum
projection fraction) methods [13]. While in the pT -balance method the jet response is evaluated by
comparing the reconstructed jet momentum (pT, jet ) directly to the momentum of the reference object
(pT,ref ), the MPF method considers the response of the whole hadronic activity in the event, recoiling
versus the reference object. This leads to the following definition of response for the two methods:
pT, jet
Rjet, pT =
,
(6.1)
pT,ref
p⃗ miss · p⃗T,ref
Rjet,MPF = 1 + T
.
(6.2)
(pT,ref ) 2
The difference and complementarity of the two response determinations will be studied in the
following sections.
Part of the transverse momentum imbalance between the jet to be calibrated and the reference
object can also come from the presence of additional jets in the event; this effect depends on
the studied topology and is not correlated with the jet energy response. For this reason, all the
corrections are studied as a function of the additional jet activity in the event, quantified by the
variable α. This is defined as the ratio of the most energetic jet that does not originate from the
event topology under study, divided by the typical momentum scale of the event. In other words
α = pT, 3rd jet /pT,ave for dijet events and α = pT, 2nd jet /pT,γ/Z for Z+jet and γ+jet events. The
corrections are then extrapolated to the value they would have for α = 0 in order to address only
genuine jet energy response effects.

– 25 –

2017 JINST 12 P02014

response and falling tracking efficiency within the jet core compensate each other. In the barrel
and endcap regions, the corrections rise with |η|, due to the increasing amount of material located
in front of the calorimeters, which leads to effects such as an increased rate of nuclear interactions
in the tracker. The corrections are higher around |η| = 1.3 and 3.0 due to the degradation of the
response in the transition regions.
Significant improvements in the simulation occurred after the first year of running at 7 TeV in
2010, when in situ collision data became available for tuning the detector simulation. After that, the
simulated particle response corrections have been stable in 2011–2012 despite continuous development of the reconstruction software, and the changes have remained within the steadily-reducing
√
systematic uncertainties. The differences introduced by the change in s are practically negligible.

## PDF page 29

R = 0.5, PF+CHS
20 fb-1 (8 TeV)
5 fb-1 (7 TeV)
36 pb-1 (7 TeV)

|η| = 0

1.4
1.3
1.2
1.1
1
0.9
20

100 200

p

T,corr

1.6
1.5

CMS
p

T,corr

= 100 GeV

1.6

CMS
p

T,corr

1.5
1.4
1.3
1.2
1.1
1
0.9

-1

R = 0.5, PF+CHS
20 fb-1 (8 TeV)
5 fb-1 (7 TeV)
36 pb-1 (7 TeV)

1.4
1.3
1.2
1.1
1
0.9

= 30 GeV

R = 0.5, PF+CHS
20 fb-1 (8 TeV)
5 fb-1 (7 TeV)
36 pb-1 (7 TeV)

|η|

(GeV)

-1

19.7 fb (8 TeV) + 36 pb + 4.9 fb (7 TeV)

1.8
1.7

-1

1.7

0 0.5 1 1.5 2 2.5 3 3.5 4 4.5 5

1000

Simulated response correction

Simulated response correction

-1

Simulated response correction

CMS
1.5

19.7 fb-1 (8 TeV) + 36 pb-1 + 4.9 fb-1 (7 TeV)

1.8

0 0.5 1 1.5 2 2.5 3 3.5 4 4.5 5

1.6
1.5

-1

19.7 fb (8 TeV) + 36 pb + 4.9 fb (7 TeV)

1.8
1.7

-1

CMS
p

T,corr

= 1000 GeV

R = 0.5, PF+CHS
20 fb-1 (8 TeV)
5 fb-1 (7 TeV)
36 pb-1 (7 TeV)

1.4
1.3
1.2
1.1
1
0.9
0 0.5 1 1.5 2 2.5 3 3.5 4 4.5 5

|η|

|η|

Figure 14. Response correction factors with their systematic uncertainty band from simulation for the 2012
data collected at 8 TeV for PF jets with CHS and R = 0.5, compared to corrections at 7 TeV corresponding to
36 pb−1 of data taken in 2010 [13] and 5 fb−1 taken in 2011 [46]. The comparison is shown at |η| = 0 versus
pT,corr (top left), and as a function of |η| at pT,corr = 30 GeV (top right), pT,corr = 100 GeV (bottom left) and
pT,corr = 1000 GeV (bottom right). The plots are limited to a jet energy E = pT cosh η = 3500 GeV so as to
show only the correction factors for reasonable pT in the considered data-taking periods.

6.1

Relative η-dependent corrections

Residual η-dependent corrections to the jet response are obtained using dijet events, where the “tag"
jet has |η| < 1.3, and the “probe" jet pseudorapidity is unconstrained. In this way, the response for
all jets is corrected relative to the response for central jets (|η| < 1.3). These residual corrections
are derived from jets already corrected with the simulation-based corrections and account for any
residual difference between data and simulation, as a function of both η and pT .
For dijet events, where the reference object (barrel jet) has poor resolution, the biases from
JER are minimized by binning in average jet pT instead of pT,tag : pT,ave = 0.5(pT,tag + pT,probe ).

– 26 –

2017 JINST 12 P02014

Simulated response correction

19.7 fb-1 (8 TeV) + 36 pb-1 + 4.9 fb-1 (7 TeV)

1.6

## PDF page 30

This symmetric pT binning also cancels out to first order the relative biases from ISR+FSR.
In general, ⟨y/x⟩ , ⟨y⟩/⟨x⟩, unless x is constant, which is generally the case only for a sufficiently
narrow bin in x. To avoid biases in the ratio variables, the denominator must therefore also use
pT,ave . This leads to the following definitions for pT balance and MPF in dijet events:
(6.3)
(6.4)
(6.5)
(6.6)

With sufficiently fine binning in pT, ave , and by extrapolating the additional jet activity, not
p
MPF reduce
coming from the leading jet, to zero with α = pT, 3rd jet /pT, ave , both variables RrelT and Rrel
to Rrel = ⟨pT, probe ⟩/⟨pT, tag ⟩. Under the assumption that ⟨pT, probe, ptcl ⟩ = ⟨pT, tag, ptcl ⟩, which is true
after correcting for the various small second-order biases from JER and ISR+FSR, this is equivalent
to the ratio of the jet responses for the tag and probe jets such that Rrel = Rjet, probe /Rjet, tag . The
residual η-dependent corrections are based on results obtained with the MPF method, the pT balance
results are used as a crosscheck.
As shown in figure 15, the relative η- and pT -dependent correction Rrel,MC /Rrel,data varies
between 0.99 and 1.01 in the barrel at |η| < 1.3, between 0.99 and 1.06 at 1.3 < |η| < 2.9, and
increases to 1.15 in HF. Some pT dependence is observed in the endcaps relative to the barrel,
with the residual corrections approaching unity at high pT , where nonlinearities in calorimeter
response are reduced. In the following we will review the corrections for ISR+FSR, JER, and jet
pT dependence, as well as the associated uncertainties for the η-dependent corrections.
Initial- and final-state radiation correction. For central-forward jet pairs there is a higher
probability for the ISR to be radiated opposite to the central jet, and the FSR activity may differ
slightly for the jets at different η, which leads to some residual dependence of the measured value of
the pT -balance or MPF response, Rrel , on additional jet activity α. We evaluate this dependence in
bins of η, for the linearly extrapolated α → 0 and α < 0.2 respectively, and compute the following
data/simulation double ratio:
data (α → 0) / Rdata (α < 0.2)
Rrel
*
+ * rel
+.
k FSR (α = 0.2) =
(6.7)
MC (α → 0)
MC (α < 0.2)
R
R
, rel
- , rel
The correction factor k FSR (we use the subscript FSR instead of ISR+FSR for brevity) is
determined separately for the MPF and pT -balance methods and for pythia 6.4 and herwig++ 2.3,
as shown in figure 16, and is then parameterized versus |η| with the same functional form as in
ref. [13]. The differences between pythia 6.4 and herwig++ 2.3 for the pT -balance method are
up to 6% at |η| < 5.2 prior to the application of ISR+FSR corrections, as seen in figure 16 (left).
Both agree well after the ISR+FSR correction, as shown in figure 16 (right), but the MPF method is
much less sensitive to ISR and FSR biases than the pT -balance method, because the entire hadronic
recoil is used for the MPF balance.

– 27 –

2017 JINST 12 P02014

1 + ⟨A⟩
, where
1 − ⟨A⟩
pT, probe − pT, tag
, and
A=
2pT, ave
1 + ⟨B⟩
MPF
Rrel
=
, where
1 − ⟨B⟩
pT, tag /pT, tag )
p⃗ miss · (⃗
B= T
.
2pT, ave
p

RrelT =

## PDF page 31

Relative correction

19.7 fb-1 (8 TeV)

1.18 CMS
1.16

Anti-kT R=0.5 PF+CHS

1.14 p (jet)
T
1.12
60 GeV
1.1

1.08
1.06
1.04

120 GeV
240 GeV
480 GeV

1
0.98
0

1

2

3

4

5

|η|

Figure 15. Relative energy scale correction for pT = 60, 120, 240 and 480 GeV as a function of |η|. The
residual corrections increase toward high rapidity and low pT , where effects from nonlinear calorimeter
response become more important. The curves are limited to a jet energy E = pT cosh η = 4000 GeV
(corresponding to η ≈ 2.8 for a jet with pT = 480 GeV) so as to show only the correction factors for
reasonable pT in the considered data-taking period. The statistical uncertainty associated with a constant fit
versus pT is shown for pT = 120 GeV (markers).

Resolution correction. The MPF and pT -balance methods are both sensitive to the relative differences in JER between the jets. This bias is expected to cancel out for the data/MC ratio of Rrel when
the jets in the simulation are smeared to match the measured resolution in data using the relation:
)
(
√
(6.8)
pT,smeared = pT Gaussian µ = 1, σ = k 2 − 1 σMC ,
where k is the data/MC scale factor for JER determined in section 8 and σMC is the JER in the MC
simulation. The factor k varies between 1.05 and 1.40 depending on η. The jet pT is multiplied
by a random number drawn from a Gaussian distribution with mean µ = 1 and width σ, such
that the smeared jet has the same resolution kσMC as the jets in data. The smearing is applied
on a jet-by-jet basis to all jets in the event, such that the resolution correction is propagated to the
pT -balance and MPF methods in a consistent way.
Relative correction: pT dependence. The η-dependent corrections are studied in bins of average
jet pT , where a slight pT dependence is observed. For this reason, the η-dependent corrections
are parameterized with a log-linear pT -dependence, according to the formula p0 + p1 log(pT ). The
correction factor as a function of η, as obtained from the pT -dependent fit is shown in figure 17 (left),
compared to the result from a constant fit. Here, the central value is obtained from evaluating the
pT -dependent correction at the pT value for which the constant fit and the logarithmic fit agree, p̄T .
The blue band is obtained by varying the pT at which the logarithmic fit is evaluated between 0.5
times and 2 times p̄T . The p̄T is typically close to the mean pT of the dijet samples, and is shown
in figure 17 (right). The pT -dependent fit is used as the central result over the whole η range, with
the exception of the HF (|η| >3). For this region, to mitigate the effect of statistical fluctuations

– 28 –

2017 JINST 12 P02014

1.02

## PDF page 32

19.7 fb-1 (8 TeV)

-1

1.04

PF+CHS

CMS

MPF Pythia6
Pt Pythia6
MPF Herwig++

1.02

1.25

Relative correction

kFSR

19.7 fb (8 TeV)

Pt Herwig++

CMS
1.2

PF+CHS
Uncertainty
MPF (Pythia6)
Pt (Pythia6)
MPF (Herwig++)
Pt (Herwig++)

1.15

1.1

1

1.05
0.98

anti-kT R=0.5
0.96

[1] cosh(|η|)
fit: [0]+
1+[2] cosh(|η|)
0.94
0

1

2

3

4

5

|η|

1.02

anti-kT R=0.5
-4

-2

0

2

4

-4

-2

0

2

4

1.01
1
0.99
0.98
0.97

η

Figure 16. The kFSR (α = 0.2) correction factor (defined in eq. (6.7)) plotted vs. |η| (left). This ratio
is used for ISR+FSR corrections that are applied to dijet events with α < 0.2, for the MPF and pT balance methods, and for pythia 6.4 tune Z2* and herwig++ 2.3 tune EE3C. The points are fitted with
f (η) = p0 + p1 cosh(η)/(1 + p2 cosh(η)) as in ref. [13]. Relative η corrections obtained with the MPF and
balance methods and the pythia 6.4 tune Z2* and herwig++ 2.3 tune EE3C MC generators (right). The
results are shown after corrections for ISR+FSR, and compared to the central values, obtained with the MPF
method and pythia 6.4 tune Z2* simulated events.
-1

19.7 fb (8 TeV)

-1

(GeV)

1.18 CMS
1.16

Anti-kT R=0.5
PF+CHS

T, ave

T

1⋅ p

1.12

bin edge

103

2 ⋅ p

1.14

CMS

PF+CHS jets

bin center
p

T

anti-kT R=0.5

p

Relative correction

19.7 fb (8 TeV)

T

1⋅ p
T
2

1.1

1.08
1.06
1.04
1.02
102

1
0.98

-4

-2

0

2

4

−4

η

−2

0

2

4

η

Figure 17. Relative η correction factor at the crossover p̄T (defined as the value of pT where the log-linear and
constant fits versus pT,ave agree) value, and at half and twice the p̄T values (left). The statistical uncertainty
in the constant fit at each value of p̄T is also shown. Distribution of the pT and η bins used in the dijet balance
measurement, with a point at the average pT and η for each bin (right). The horizontal red lines indicate the
crossover p̄T value for each bin.

(visible e.g. in figure 17 (left)), the correction is taken from the constant fit and symmetrized over
positive and negative η values.

– 29 –

2017 JINST 12 P02014

Ratio to Pythia6 MPF

1

## PDF page 33

6.2

Relative correction uncertainties

The largest uncertainties in the relative corrections arise from the following sources:
• ISR+FSR, ≤0.2%. The RelativeFSR uncertainty in k FSR is estimated by using herwig++ 2.3
as “data" and comparing how well the different methods reproduce the ratio of particle-level
simulated responses. This uncertainty increases smoothly with increasing |η|, up to 0.2%
in HF.

• Relative correction pT dependence, ≤1.4%. Half of the difference between the log-linear
and constant fits observed in figure 17 is taken as a RelativePt systematic uncertainty to
account for uncertainties coming from the choice of the log-linear shape for the fit. This is
the dominant uncertainty in the barrel and endcaps.
• Statistical uncertainty, ≤0.9%. The number of events available in data for the η-dependent
corrections is limited in the endcap and HF regions due to the large prescales applied to
the dijet triggers during data taking. To estimate the impact of this on physics analyses, the
corrections are symmetrized and determined in wide bins of |η|. The remaining statistical
uncertainty of up to 2.5% is assigned as RelativeStat systematic uncertainty.
• Time dependence, ≤1.0%. The TimeEta systematic uncertainty is estimated as the RMS of
the η-dependent correction factors for a set of about ten data-taking periods, chosen arbitrarily
in order to have comparable integrated luminosities. The variation is assumed to come from
residual scale shifts remaining after the radiation damage corrections have been applied to the
ECAL and HCAL, and increases toward high rapidities, which suffer larger radiation damage.
Uncertainty correlations versus η. The RelativeJER, RelativePt, and RelativeStat systematic
uncertainties are assumed to be correlated versus η within the barrel (BB: |η| < 1.3), the region of
the endcap that is within tracker coverage (EC1: 1.3 < |η| < 2.5), the region of the endcap which
is outside the tracker coverage (EC2: 2.5 < |η| < 3), and within the hadron forward calorimeter
(HF: 3 < |η| < 5.2), but not between these regions. The RelativeStat uncertainty is significant only
in the more forward regions, and is only provided for the two latter regions (EC2 and HF, which are
considered uncorrelated). All other systematic uncertainties relevant for η-dependent corrections
(RelativeFSR, TimeEta) are considered to be fully correlated versus η. Each correlated region is
treated with a separate systematic source, and these are provided separately to the users.
The systematic uncertainties in the relative η-dependent corrections are summarized in figure 18, for low (30 GeV) and medium (100 GeV) pT versus η, and for the outer endcap (η = 2.7)
versus pT . The time-dependent uncertainties are optional for analyses that are performed on the
full 2012 data and are shown separately versus η at pT = 30 GeV. Among the time-dependent
systematic uncertainties only the TimeEta is relevant. The uncertainties are small at high pT and
for central rapidities within the tracker coverage. They increase to 2.1% at high rapidity mainly

– 30 –

2017 JINST 12 P02014

• Jet pT resolution, ≤1.4%. The RelativeJER systematic uncertainty on the JER correction
is estimated by varying the data/MC scale factor k in eq. (6.8) within the uncertainties
determined in section 8, which are between 2% and 20%, depending on η. This uncertainty
mainly affects the η bins in the HF, where JER is poorly constrained from data.

## PDF page 34

CMS
3.5
3 R=0.5 PF+CHS
|η | = 2.7
jet

JEC uncertainty (%)

JEC uncertainty (%)

19.7 fb-1 (8 TeV)

4

SubTotalRelative
RelativePt
RelativeJER
RelativeFSR
RelativeStat

2.5
2
1.5

CMS
3.5
3 R=0.5 PF+CHS
p = 30 GeV
T

2
1.5

0.5

0.5
100 200

0

1000

−4

−2

0

2

4

p (GeV)
-1

19.7 fb (8 TeV)

CMS
3.5
3 R=0.5 PF+CHS
p = 100 GeV
T

JEC uncertainty (%)

JEC uncertainty (%)

-1

4

SubTotalRelative
RelativePt
RelativeJER
RelativeFSR
RelativeStat

2.5
2
1.5

3 R=0.5 PF+CHS
p = 30 GeV
T

2.5
2
1.5

0.5

0.5
−2

0

2

4

0

η

jet

TimeEta

CMS
3.5

1

−4

19.7 fb (8 TeV)

4

1

0

η

jet

T

−4

−2

0

2

4

η

jet

Figure 18. Systematic uncertainties for the relative η-dependent corrections as a function of jet pT (top left)
and as a function of jet η for jets with pT = 30 GeV (top right) and for jets with pT = 100 GeV (bottom
left). Time-dependent uncertainties as a function of jet η for jets with pT = 30 GeV (bottom right). The
plots are limited to a jet energy E = pT cosh η = 4000 GeV so as to show only uncertainties for reasonable
pT in the considered data-taking period. SubTotalRelative is the quadratic sum of RelativePt, RelativeJER,
RelativeFSR and RelativeStat.

due to the limited number of events available in the data for deriving the JEC, JER and ISR+FSR
corrections. The dominant PileUpPt uncertainty is inherently asymmetric and has the largest visible
differences in the HF region, where the asymmetric log-linear fit is compared to a symmetrized
constant fit used for central value in HF. The uncertainty versus pT changes sign around 100 GeV
for the negative η side while it remains same-sign for the positive η.

– 31 –

2017 JINST 12 P02014

1

20

SubTotalRelative
RelativePt
RelativeJER
RelativeFSR
RelativeStat

2.5

1

0

19.7 fb-1 (8 TeV)

4

## PDF page 35

6.3

Absolute corrections

The absolute JES at |η| < 1.3 is determined with Z(→ µµ)+jet, Z(→ ee)+jet and γ+jet events
for jet pT between 30 and 800 GeV by comparing the reconstructed pT of the jet to that of a
precisely measured object (the Z boson, or the photon). The response for jets with pT > 800 GeV
is constrained using multijet events, where a high-pT jet in the barrel region is balanced by a recoil
system, composed of two or more lower-pT jets.

Methods. The absolute jet response is measured relative to a photon or Z boson momentum scale,
using the pT -balance (Rjet,pT ) and MPF (Rjet,MPF ) methods [13], as defined in eqs. (6.1) and (6.2),
with pT, ref = pT,γ/Z . The measurements are affected by biases from ISR+FSR, underlying event
(UE) and out-of-cone (OOC) showering. To correct for the FSR+ISR bias, we define a k FSR
correction as follows:
pT,2nd jet
Rjet (α → 0)
k FSR (α) =
, α=
,
(6.9)
Rjet (α)
pT,γ/Z
where the jet response Rjet is measured with the MPF or the pT -balance method, with separate
corrections for each. As shown in figure 19, the value of k FSR (α) is linearly dependent on α for
0.05 < α < 0.3. Because the average pT of the Z boson decreases with α, the particle-level jet
response obtained from simulation also shows a dependence on α. Figure 19 demonstrates that the
MPF method is significantly less sensitive to ISR+FSR and the modeling of these processes, than
the pT -balance method: the slope ∆Rjet /∆α is about −0.3 for the pT -balance method and +0.06 for
the MPF method. For the data/MC ratio these slopes are further reduced by an order of magnitude,
confirming a good modeling of the OOC and UE effects. It can be shown that the ratio of MPF and
pT -balance slopes versus α is
RFSR+ISR jets
dRjet,MPF /dα
=1−
.
dRjet, pT /dα
Rjet

(6.10)

The difference in jet response between the leading jet and the ISR+FSR jets is typically less
than 20%, as seen in figure 14, but the sign can be either positive or negative. The slope of k FSR
has some dependence on the jet flavor (gluons radiate more than quarks) and it depends, e.g., on
the parton shower model used in the MC simulation. As shown in section 6.4, determining k FSR in
narrow bins of pT,ref is needed in order to study the pT dependence of the JES.

– 32 –

2017 JINST 12 P02014

For all these analyses, the corrections are derived by comparing the jet energy response (with
different methods) in data and simulation, using events in the central region, where jets are already
corrected with the simulation-based corrections and η-dependent residual corrections. As detailed
below, the response is observed to be slightly lower in data than in simulation. In addition, the
ratio of data over the MC prediction of the response shows a pT dependence. The two effects are
factorized and addressed in successive steps. First, a rough estimate of the pT independent correction
is derived from the analysis of Z(→ µµ)+jet events. Second, the response and its pT dependence
are determined precisely from a global fit (described in section 6.4), with the individual response
values obtained from the different channels (Z(→ µµ)+jet, Z(→ ee)+jet, γ+jet, multijet) as input.

## PDF page 36

I
Jet response

19.7 fb−1 (8 TeV)
1.05

CMS

1.00

0.95

Data / MC

0.85
1.02
1.01
1.00
0.99
0.98

MPF
pT balance

0.00 0.05 0.10 0.15 0.20 0.25

α

Figure 19. Jet response obtained with the pT -balance and MPF methods in Z+jet events (points), for both
data and simulation (MadGraph 4+pythia 6.4 tune Z2*), plotted as a function of α = pT,2nd jet /pT,Z (top).
The response in data is scaled by a factor of 1.02, constant as a function of pT . A fit to a first-order polynomial
(dashed lines) is shown, together with the statistical uncertainty from the fit (shaded bands). Only events
with pT,Z > 30 GeV and |η jet | < 1.3 are considered. The ratio of the jet response from the pT -balance and
MPF methods in data and simulation shown in the bottom panel. The simulated jet response pT,jet /pT, ptcl is
higher than unity because the jets are corrected with JEC from QCD dijet events with lower jet response than
Z+jet events due to higher gluon fraction and larger underlying event.

The remaining effects of UE and OOC affect MPF and pT balance slightly differently. It can
be shown that, having corrected for ISR+FSR, the balancing and MPF responses can be written as
OOC
UE
pT,
pT,
ptcl
ptcl +
Rjet, pT = Rjet *1 −
+
,
p
p
T,
ptcl
T,
ptcl
,
(
) pOOC
(
) UE ⎤
⎡⎢
RUE pT, ptcl ⎥⎥
ROOC T, ptcl
+ 1−
,
Rjet,MPF = Rjet ⎢⎢1 − 1 −
Rjet pT, ptcl
Rjet pT, ptcl ⎥⎥
⎢⎣
⎦

(6.11)
(6.12)

OOC , pUE
where pT,
ptcl
T, ptcl are OOC and UE transverse momenta projected to the reference object axis,
and ROOC , RUE are their effective responses. Compared to the pT balance, the residual biases for
MPF are multiplied by a factor that is typically about 10% or less, and can be safely ignored. The
corrections for OOC and UE compensate each other, but for jet radii R ≥ 0.5 the OOC effect is
smaller than the one coming from the UE at low pT . We can therefore estimate an upper limit on
these biases by assuming an UE energy density of about 1 GeV per unit of jet area, which gives

– 33 –

2017 JINST 12 P02014

0.90

MPF (Data)
MPF (MC)
pT balance (Data)
pT balance (MC)
pT, jet /pT, ptcl

## PDF page 37

|η| < 1.3

Simulation

40

0.27
0.24
0.21
0.18

30

0.15
0.12

20

0.09

10

0.03
50

100

150

200

250

0.00

50

CMS

|η| < 1.3

Simulation

40

0.30
0.27
0.24
0.21
0.18

30

0.15
0.12

20

0.09
0.06

10

0.03
50

pT,Z (GeV)

8 TeV
pT balance

100

150

200

250

0.00

pT,Z (GeV)

Figure 20. Relative resolution (blue scale) in the plane of mean number of pileup events (µ) and Z boson
transverse momentum (pT,Z ) for the MPF balance (left) and pT -balance methods (right).

a correction of at most ≈2.6% for pT, ptcl = 30 GeV and jet distance parameter R = 0.5. This is
compatible with the magnitude and sign of the observed difference of less than 2% between MPF
and pT balance at the α → 0 limit in figure 19.
Although the MPF and pT -balance methods are biased in different ways, both can be corrected
for ISR+FSR and are complementary to each other. The remaining biases from OOC and UE
(both magnitude and response, see eqs. (6.11) and (6.12)) affect the pT balance and MPF methods
differently, and therefore fitting both simultaneously reduces the overall systematic uncertainty in
the global fit. The relative statistical power (quantified by the relative resolution of the measured
response, compared to the particle-level response) of pT balance and MPF depends on the jet pT
and the level of PU, as seen in figure 20. The MPF method is sensitive to smearing in p⃗Tmiss caused
by PU, while the pT balance is sensitive to the smearing in the momentum balance caused by
ISR+FSR. The former effect dominates at low pT , while the latter dominates at high pT , such that
both methods have similar sensitivity at pT ≈ 100 GeV for ⟨µ⟩ = 20.
Z+jet and γ+jet balance. The event selection is described in section 3.2. The JES is determined
relative to precisely measured muons, electrons, and photons, with a tracker scale uncertainty of
0.2% for muons at |η| < 2.4 [29], an ECAL scale uncertainty of 0.5% for electrons at |η| < 2.4 [48],
and 0.2% for photons at |η| < 1.3 [32].
The peak of the invariant-mass distribution of Z → µµ(ee) events is used to validate the muon
(electron) energy scale between data and simulation. These are found to agree within 0.2% (0.5%).
Additional checks ensure that the p⃗Tmiss used in the MPF method is not biased by minimum-ionizing
particle deposits of muons in the calorimeters, or by residual leakage of electron and photon energy
into ECAL or HCAL not clustered in the reconstructed electron or photon. As the photon energy
scale includes corrections for these unclustered contributions, special care is taken in order to avoid
double counting of the leakage energy from fully calibrated PF photon superclusters to p⃗Tmiss (such
double counting will be referred to as electromagnetic footprint effect).

– 34 –

2017 JINST 12 P02014

0.06

µ

CMS

I
0.30

RMS((Rptcl − Rjet,pT )/Rptcl )

50

8 TeV
MPF

RMS((Rptcl − Rjet,MPF )/Rptcl )

µ

I

## PDF page 38

Multijet balance. The extrapolation of the JEC to high pT is constrained using data with the multijet balance (MJB) method introduced in ref. [14], with events where a high-pT barrel jet is balanced
by a recoil system, composed of two or more lower-pT jets. In addition to the traditional balancing
variable, MJB = pT,lead /pT,recoil , the response is also studied using an MPF method, where MPF =
1 + (⃗
pTmiss · p⃗T,recoil )/|⃗
pT,recoil | 2 . The jets used in the analysis are corrected for all the previous stages,
including residual η-dependent corrections from dijets, but excluding the final absolute correction
versus pT . The response in data is scaled by a rough factor of 1.02, constant as a function of pT ,
extracted from the study of Z(→ µµ)+jet events. The p⃗Tmiss is corrected for all jets with |η| < 5 and
pT > 10 GeV in the MPF method, but only jets with pT > 30 GeV are used for the event selection and
for constructing the pT,recoil . The pT > 30 GeV threshold ensures that the event selection is not biased
by pileup jets, and that the recoil is composed of jets directly calibrated with data-based methods.
To interpret the results for JES we define an effective average pT,eff ptcl of the jets in the recoil,
such that
∑
Rjet (pT,eff ptcl )⃗
pT,recoil ptcl =
Rjet (pT,i ptcl )⃗
pT,i ptcl,
(6.13)
i ∈recoil jets

where Rjet (pT ) is the response of a jet of transverse momentum pT .

– 35 –

2017 JINST 12 P02014

Events are binned in photon or Z boson pT to avoid resolution bias from the relatively poorly
measured jets. The asymmetric ISR and FSR is accounted for by extrapolating to zero the additional
jet activity (using the α variable, defined in eq. (6.9)). The response for Z(→ µµ)+jet events is about
2% lower in data than in simulation, in agreement with what is observed for the jet response in the
7-TeV data. In figures 21 to 23, the jet response in data is first corrected by this factor, independent of
the jet pT . This correction is reabsorbed in the global fit, that constraints simultaneously the overall
normalisation and the pT -dependence of the ratio of data over simulation responses, to obtain the
final correction.
The initial results are obtained after correcting jets and p⃗Tmiss for pileup, jet energy response
as extracted from simulation studies, and after applying the residual η-dependent corrections based
on the dijet balance and the data/MC scale factor of 1.02 from Z(→ µµ)+jet events. The MPF
and pT -balance methods have different sensitivities to ISR and FSR, which further reduces the
uncertainty on the correction. Jet response measurements obtained from these two methods are
shown in figure 21 for the nominal working point α < 0.3. The results are presented for the three
event samples (Z(→ µµ)+jet, Z(→ ee)+jet and γ+jet) and are shown for data and simulation. The
ratio of data to simulation is shown in figure 22. These results are displayed before extrapolating
the additional jet radiation to zero and correcting for the pT dependence of the JES: these effects
will be taken into account in the global fit described in section 6.4. The agreement between the
measured response in different samples is reasonable for data and MC simulation separately, and
most remaining differences cancel out in the data/MC ratio. The differences between Z(→ ee)+jet
and Z(→ µµ)+jet/γ+jet events in the MPF method are due to a double counting of leakage from PF
electrons and photons to p⃗Tmiss (EM footprint effect on p⃗Tmiss ), which is absent for muons and corrected
for photons, but not for electrons. The differences between the MPF and the pT -balance methods
arise from ISR+FSR effects, and largely disappear in the data/MC ratio when k FSR corrections are
applied. Residual biases from ISR and FSR, as well as effects from lepton/photon scales and EM
footprint in p⃗Tmiss , are dealt with in the global fit described in section 6.4.

## PDF page 39

1.1

CMS

MPF type-I (CHS)
γ +jet
Z(→ee)+jet
Z(→µµ)+jet

1.05

(8 TeV)

Response (MC)

Response (data)

19.7 fb-1 (8 TeV)

1.1

1

0.95

0.95

40

100

200

p

T,ref

|η| < 1.3, α < 0.3

0.9
40

1000

(GeV)

100

200

1000

p

T,ref

1.1

CMS

p balance (CHS)
T
γ +jet
Z(→ee)+jet
Z(→µµ)+jet

1.05

(8 TeV)

Response (MC)

Response (data)

19.7 fb-1 (8 TeV)

1.1

1

0.95

0.95
|η| < 1.3, α < 0.3

40

100

200

p

T,ref

CMS

p balance (CHS)
T
γ +jet
Z(→ee)+jet
Z(→µµ)+jet

Simulation

1.05

1

0.9

(GeV)

|η| < 1.3, α < 0.3

0.9
40

1000

(GeV)

100

200

p

1000

T,ref

(GeV)

Figure 21. Comparison of jet response measurements from Z(→ µµ)+jet, Z(→ ee)+jet, and γ+jet samples
as a function of Z boson or photon pT . The jet response from the MPF method (top) and the pT -balance
method (bottom) is shown as a function of Z and γ pT for data (left) and simulation (right). The Z(→ ee)+jet
sample has not been corrected for the electron EM footprint in p⃗Tmiss , explaining the low MPF response in
both data and simulation. The footprint effect is absent for muons and corrected for photons.

This is solved for pT,eff ptcl in the log-linear approximation, Rjet (pT ) = p0 + p1 log(pT ), giving
∑
pT,eff ptcl = pT,recoil ptcl exp *
Fi log( f i ) + , where
, i
pT,i ptcl
fi =
, and Fi = f i cos(∆φi ).
pT,recoil ptcl
The ∆φi is the angle between the jet four-vector and the recoil, and by construction
Labeling further
Crecoil = pT,eff ptcl /pT,recoil ptcl,

– 36 –

(6.14)
(6.15)
i Fi = 1.

∑

(6.16)

2017 JINST 12 P02014

|η| < 1.3, α < 0.3

MPF type-I (CHS)
γ +jet
Z(→ee)+jet
Z(→µµ)+jet

1.05

1

0.9

CMS
Simulation

## PDF page 40

1.1

CMS

MPF type-I (CHS)
γ +jet
Z(→ee)+jet
Z(→µµ)+jet

1.05
1
0.95

19.7 fb-1 (8 TeV)

Data/MC response ratio

Data/MC response ratio

19.7 fb-1 (8 TeV)

40

100

200

p

T,ref

CMS

p balance (CHS)
T
γ +jet
Z(→ee)+jet
Z(→µµ)+jet

1.05
1
0.95

|η| < 1.3, α < 0.3

0.9
40

1000

(GeV)

100

200

p

T,ref

1000

(GeV)

Figure 22. Ratio of the jet response measurement obtained from data and simulation with the MPF method
(left) and pT -balance method (right). Results are shown for the Z(→ µµ)+jet, Z(→ ee)+jet, and γ+jet
samples. The Z(→ ee)+jet sample has not been corrected for the electron EM footprint in p⃗Tmiss , but the
effect cancels out in the ratio of data over simulation.

we can write
MJB =

Rjet (pT,lead ptcl )pT,lead ptcl
Rjet (pT )
≈
,
Rjet (pT,eff ptcl )pT,recoil ptcl Rjet (Crecoil pT )

(6.17)

where the last approximation uses pT,lead ptcl ≈ pT,recoil ptcl ≡ pT . The pT,eff represents the effective
average jet pT in the recoil system (see eq. (6.13)), and the high-pT jets are calibrated relative to
pT,eff . In the actual calculation, Crecoil is evaluated from reconstructed jets pT (corrected with MCbased corrections and data-driven corrections for pileup effects and η dependence of the response),
which is equivalent to the particle-level Crecoil to sufficient precision. Crecoil , shown in figure 23
(left), is therefore a measure of the lever arm of the multijet balance method in measuring pT
dependence of JES. Because the MPF method indirectly uses jets also below pT = 30 GeV, its lever
arm Crecoil is calculated from all jets of pT > 10 GeV, while that of MJB is calculated only from
jets of pT > 30 GeV. The MPF method is stable with respect to the jet pT threshold, while the MJB
drops below MPF at low pT when the pT threshold is lowered to 10–20 GeV.
As the leading jet is calibrated using the recoil system as a reference object, the scale obtained
for high-pT jets using this method is relative to the average scale for the lower pT jets, which
are subject to systematic uncertainties particularly from jet-flavor response, pileup offset and ηdependent corrections. Systematic uncertainties arising from JEC, JER uncertainties, and PU
modeling are propagated to the multijet analysis. As shown in figure 23 (right), the leading high-pT
jet is well balanced against the recoil within the JEC uncertainties, and the multijet balance method
constrains the response of jets with a pT as high as 1.3 TeV. The global fit takes as input the
measured MJB, MPF and Crecoil , using the formulation of eq. (6.17).

– 37 –

2017 JINST 12 P02014

|η| < 1.3, α < 0.3

0.9

1.1

## PDF page 41

19.7 fb-1 (8 TeV)

CMS

Response

Crecoil

0.46
0.44
0.42

1.02

19.7 fb-1 (8 TeV)

CMS

1.01
1
0.99
0.98

0.4

0.97
0.96

0.38

0.95

0.36

MJB, MC
MJB, data
MPF, MC
MPF, data

0.94

T

1.05

400

600

800

1000

1200

1400

Fit pT > 30 GeV:
p 0.9864 ± 0.0006
(GeV)
recoil± 0.0006
Fit pT > 10 GeV:T,
0.9774

1
0.95

400

600

800

1000

p

1200

T, recoil

Data / MC

Data / MC

0.93

1400

(GeV)

1.05

400

600

800

1000

1200

1400

(GeV)
Fit MJB: p
1.0013 ± 0.0008
T, recoil
Fit MPF: 0.9984 ± 0.0008

1
0.95

400

600

800

1000

p

1200

T, recoil

1400

(GeV)

Figure 23. Crecoil ratio of the effective jet pT of jets in the recoil over the total recoil pT , (eq. (6.16)),
calculated with recoil jets of pT > 30 GeV (for MJB) and pT > 10 GeV (for MPF) in data and MC simulation
(left). Multijet balance response calculated with the MJB and MPF methods for data and MC simulation
(right). The filled bands show the statistical uncertainty on MC for the left plot and the total (statistical and
systematic) uncertainty on MC for the right plot. The error bars show the statistical uncertainty on data.

6.4

Global fit of absolute corrections

The absolute jet pT scale is fitted simultaneously to the muon and electron (for 30 < pT, Z <
400 GeV), photon (40 < pT,γ < 800 GeV), and multijet (220 < pT,recoil < 1300 GeV) data sets. The
muon, photon, and electron scales are allowed to vary within their a priori uncertainties of 0.2%,
0.2%, and 0.5%, respectively. The results used as input to the global fit (α < 0.3) with initial k FSR
corrections α < 0.3 → 0 are shown in figure 24 (left), overlaid with the final determination of JES
and its uncertainties. The global fit is implemented as a χ2 minimization. The fit results depend on
some parameters that are known within given uncertainties, these are treated as nuisance parameters
in the fit and added quadratically to the χ2 expression. The nuisance parameters are related to the
following effects:
• Lepton/photon scale uncertainties (0.2% for µ± , 0.2% for γ, and 0.5% for e± , assumed to
be uncorrelated, and independent of pT ).
• ISR+FSR uncertainty on the k FSR correction fit used in the MPF and pT -balance methods.
The fit is performed in each sample using a three-parameter log-polynomial pT dependence:
its results, with their uncertainties, are used as input to the global fit and are shown as the
shaded band labeled ‘In’ in figure 25.

– 38 –

2017 JINST 12 P02014

p > 30 GeV, MC
T
p > 30 GeV, data
T
p > 10 GeV, MC
T
p > 10 GeV, data

## PDF page 42

pbal MPF
T
Multijet
γ +jet
Z(→ee)+jet
Z(→µµ)+jet
JES unc.

CMS
1.06
1.04

|η| < 1.3
α < 0.3 → 0

1.02
1
0.98

CMS
1.06
1.04

100

200

0.98
0.96
After global fit
χ2 / Ndof = 107.5 / 92

40

1000

p (GeV)

pbal MPF
T
Multijet
γ +jet
Z(→ee)+jet
Z(→µµ)+jet
JES unc.

1

0.94
40

|η| < 1.3
α < 0.3 → 0

1.02

Before global fit

0.94

19.7 fb-1 (8 TeV)

1.08

100

200

1000

p (GeV)

T

T

Figure 24. Comparison of the data-to-simulation ratio of the jet response measurements from Z(→ µµ)+jet,
Z(→ ee)+jet, γ+jet, and multijet samples after applying the corrections for JES and ISR+FSR (left) and after
applying, in addition, the nuisance parameter values found by the global fit (right). The uncertainty in the
ratio, excluding jet-flavor and time-dependent effects, is shown by the shaded region. The solid line shows
the global fit central value and the dotted curves the statistical uncertainty of the fit. As the multijet analysis
connects the energy scale of jets in two different pT ranges (eq. (6.17)), it can be used to constrain the high-pT
region given the low-pT one (black triangles) or vice versa (grey triangles).

• EM footprint uncertainty for photons and electrons in the MPF method (0.2% for photons
with footprint correction, and 0.5% for electrons without footprint correction, independently
of each other, and independent of pT ).
• Pileup uncertainty coming from the difference in the offset calculated inside versus outside
of the jet distance parameter.
• Multijet uncertainties from JES, JER, and pileup, separately for MPF and MJB.
The total number of nuisance parameters is three for the lepton/photon scales, 2 × 3 × 3 = 18 for
ISR+FSR, two for EM footprint, one for pileup, and 2 × 3 = 6 for multijet balance, for a total of 30
sources.
The global fit has two parameters of interest, one for fitting the absolute scale and one for fitting
the pT dependence under the assumption that the shape of the response variation is consistent with
the one caused by a constant shift in single-pion response in HCAL, shown in figure 13 (right),
and referred to as f HCAL (pT ) in the following. This assumption is supported by the time stability
of charged-pion E/p in HCAL barrel. The function used to fit the pT dependence is of the form
a+b( f HCAL (pT ) − f HCAL (pT,0 )), hence introducing a reference momentum pT,0 and fitting the shape
relative to it. The value of pT,0 = 208 GeV is chosen to minimize the correlation between a and b.
The result of the pT -dependent fit is shown in figure 24 (right). The data points are shifted by
the nuisance parameter values found by the global fit in order to demonstrate the good consistency
between the data sets. The nuisance parameters are normally distributed, with no outliers beyond

– 39 –

2017 JINST 12 P02014

0.96

Post-fit jet response (ratio)

Jet response (ratio)

19.7 fb-1 (8 TeV)

1.08

## PDF page 43

0.1

CMS

In Out
γ +jet
Z(→ee)+jet
Z(→µµ)+jet

0.05

19.7 fb-1 (8 TeV)

dR / dαmax (ratio)

dR / dαmax (ratio)

19.7 fb-1 (8 TeV)

0

−0.05

In Out
γ +jet
Z(→ee)+jet
Z(→µµ)+jet

0.03
0.02
0.01
0

p balance method

40

100

MPF method

−0.02

T

200 300

40

p (GeV)
T

100

200 300

p (GeV)
T

Figure 25. Central value of the data-to-simulation ratio of dR/dαmax , and its 68% probability region, as a
function of jet pT , for the pT -balance (left) and MPF (right) methods. The dR/dαmax is the derivative of
the jet response evaluated in events with α < αmax . The y-axis scale for the MPF method is zoomed by ×4
compared to the pT -balance method, demonstrating the much smaller initial ISR+FSR uncertainty for this
method. The shadowed regions show the input distributions to the global fit, while the full color regions
show the post-fit distributions. The uncertainties on dR/dαmax before the global fit are labeled ‘In’, and the
uncertainties constrained by the global fit are labeled ‘Out’.

the 2σ limit. The reduced goodness-of-fit, χ2 /Ndof , is 107.5/92 ≈ 1 for all degrees of freedom
and for data points and nuisance parameters combined, indicating appropriate coverage by the
systematic and statistical uncertainties. The statistical uncertainty band of the global fit, which is
shown by the dotted curves, can be separated into two independent components, one describing the
uncertainty in absolute scale, the other describing the uncertainty in pT dependence coming from
HCAL response. Other JES systematic uncertainties are calculated with respect to the factorization
point pT = 208 GeV that also has the smallest fit uncertainty.
The initial ISR+FSR corrections are constrained by the global fit, and their uncertainties before
and after the fit are shown in figure 25 by the solid bands labeled ‘In’ and ‘Out’, respectively. The
ISR+FSR correction for α < 0.3 varies from about 1.5% for pT balance (k FSR ≈ −5%) to less than
0.3% for MPF (|kFSR | < 1%). This is consistent with the expectation that MPF is only sensitive
to FSR and ISR to second order through differences in the response between the leading jet and
the rest of the hadronic recoil, which are expected to be less than 20%. The ISR+FSR corrections
as constrained by the fit are within the uncertainty of the input values, with the exception of the
pT -balance method for Z(→ µµ)+jet events, which stays within twice the input uncertainty and
whose initial tension with respect to the Z(→ ee)+jet channel is reduced by the fit.
6.5

Absolute correction uncertainties

Scale uncertainty.
sources:

The dominant uncertainties for the scale factor arise from the following

– 40 –

2017 JINST 12 P02014

−0.01

−0.1
−0.15

0.04 CMS

## PDF page 44

• Absolute scale, 0.11%. The uncertainty in the fitted absolute scale is driven by the muon
scale of 0.2%, obtained from the position of the Z boson mass peak, and by the photon scale
uncertainty of 0.2%, achieved via a precise regression correction [32].
• HCAL scale, ≤0.6%. The uncertainty in the fitted HCAL scale is driven by the statistical
uncertainty of the Z+jet sample at low pT and by the γ+jet sample at high pT . This uncertainty
is labeled SinglePionHCAL.

• MPF bias, 0.28%. The bias on the MPF method is composed of two subsources:
– Neutrino production, 0.2%. This uncertainty is estimated from the 0.1% excess of both
electron and muon energies in the PF jet compositions (shown in figure 46), which is
assumed to be associated with a neutrino excess from decays of heavy-flavor hadrons,
of similar order of magnitude. The estimate is compatible with uncertainties in the
fraction of heavy-flavors from gluon splitting.
– ISR outside detector acceptance, 0.2%. The extrapolation to zero additional jet activity
cannot correct for ISR activity outside detector acceptance, which biases both MPF and
pT balance by the same amount. Phase space constraints limit ISR jet pT outside the
detector to pT ≤ 30 GeV, which together with the results on the MPF and pT -balance
response in simulation after the JEC set an upper limit of 0.2% on this source.
Single-particle response and fragmentation systematics. We consider additional shape uncertainties from single-pion response and jet fragmentation using simulation. These studies were
reported in section 5. The JEC at pT = 208 GeV is known to high accuracy from the global fit so
the simulation-based shape uncertainties are assumed to be zero at this reference pT , but increase
further away from the reference point. The single-particle response uncertainty of 3% is imple√
mented using independent variations of ± 23% in responses in the ECAL and HCAL separately.
The variation in the HCAL is included in the global fit and constrained to −3.50 ± 1.35%. The
fragmentation uncertainty is taken directly as the pythia 6.4/herwig++ 2.3 response difference.
Time dependence
The JES pT dependence is believed to originate mostly from a reduction in the HCAL energy scale
due to various effects, including uncorrected radiation damage in the front layers of the barrel
calorimeter. To estimate the stability of the HCAL scale with time, the ratio of the calorimeter
energy to track momentum EHCAL /ptrack of isolated barrel hadrons was plotted as a function of time
for pions that did not interact in the EM calorimeter. The 2012 (8 TeV) data sample is divided in four
subsequent run periods, with slightly different conditions and trigger requirements: run A (with an
integrated luminosity of 0.88 fb−1 ), B (with 4.41 fb−1 ), C (with 7.05 fb−1 ) and D (with 7.37 fb−1 ).
The EHCAL /ptrack shows variation of up to 4.5% between run A and run D for p = 10 GeV hadrons.

– 41 –

2017 JINST 12 P02014

• Statistical uncertainty, ≤0.1%. The statistical uncertainty covers the small residual difference between the global fit uncertainty calculated with the full covariance matrix and the
uncertainty calculated from its diagonal elements (absolute scale and HCAL scale, above)
only. Only positive contributions are included.

## PDF page 45

4

CMS

3 R=0.5 PF+CHS
|η | = 0
jet

JEC uncertainty (%)

JEC uncertainty (%)

19.7 fb-1 (8 TeV)

TimePt
TimePtRunA
TimePtRunB
TimePtRunC
TimePtRunD

2
1
0

19.7 fb-1 (8 TeV)

3
2.5

CMS

2 R=0.5 PF+CHS
1.5

|η | = 0
jet

1

SubTotalAbsolute
AbsoluteScale
AbsoluteStat
Fragmentation
SinglePionECAL
SinglePionHCAL
MPFBias

0.5
0

−1

−2
20

100 200

−1.5

1000

p (GeV)

20

100 200

1000

p (GeV)

T

T

Figure 26. Absolute scale time-dependent uncertainty as a function of jet pT for various data-taking periods
(left). Systematic uncertainties for the absolute jet scale as a function of pT (right). SubTotalAbsolute is
the quadratic sum of AbsoluteScale, AbsoluteStat, Fragmentation, SinglePionECAL, SinglePionHCAL and
MPFBias.

The HCAL scale variations relative to the full 2012 (8 TeV) data set were taken as uncertainties
for each data-taking run (TimePtRunA, TimePtRunB, TimePtRunC and TimePtRunD for runs A,
B, C and D, respectively), and then propagated to the jet response, as shown in figure 26 (left).
The integrated-luminosity-weighted RMS of these run variations is taken as the time-dependent
uncertainty in the absolute scale versus pT , TimePt. In a similar fashion, the time-dependent
uncertainty in the relative η-dependent corrections is estimated as the RMS of the correction
factors obtained for short data-taking time periods, each weighted by the corresponding integrated
luminosity. Neither uncertainty needs to be applied to analyses performed using the complete 2012
(8 TeV) dataset with unprescaled triggers, for which the time-dependent effects average out.
The SinglePionECAL, Fragmentation, and MPFBias uncertainties are summarized in figure 26
(right), together with the AbsoluteScale, SinglePionHCAL, and AbsoluteStat uncertainties, which
are effectively the constant, pT -dependent, and residual components of the statistical uncertainty in
the global fit, respectively.
6.6

Summary of residual corrections

The data-based residual corrections for the relative JES versus η have been derived with dijet events
using the MPF method, and for the absolute JES versus pT with a global fit combining results from
Z(→ µµ)+jet, Z(→ ee)+jet, γ+jet and multijet analyses with both MPF and pT -balance methods.
The residual corrections are summarized in figure 27, and are compared to the results for 7 TeV
proton-proton collision data in 2010 and 2011. The residual response corrections are less than
3% in the barrel, less than 10% in the endcaps, and about 10% in the forward detector, with the
exception of the narrow endcap-forward boundary region at 3.0 < |η| < 3.2.
The uncertainty in JEC pT dependence, which comes from detector simulation and from
fragmentation modeling, is estimated to be less than 1% for 30 < pT < 2000 GeV. This uncertainty

– 42 –

2017 JINST 12 P02014

−0.5

−1

## PDF page 46

7

Jet flavor corrections

7.1

Jet flavor definitions

The QCD dijet sample is enriched in gluon jets, while the Z+jet and γ+jet samples are enriched in
quark jets, which is important for latest stages of JEC estimation. We define jet flavor in terms of the
parton flavor (’physics definition’), where the particle jet is matched to the nearest generator-level
parton, considering only partons belonging to the hard scattering matrix element process, within
∆R < 0.25. According to this physics definition, jets resulting from hard gluon radiation without a
matching parton have an undefined flavor. This convention is well-defined for both pythia 6.4 and
herwig++ 2.3. According to this definition, jets containing heavy-quark hadrons produced through
gluon splitting (e.g., g → bb) are still classified as gluons.
The definition typically used for b-tagging purposes uses parton shower flavor (’algorithmic
definition’) that reclassifies jets with heavy-quark hadrons from gluon splitting as b- or c-quark
jets. However, because this algorithm uses information from the final stage of the parton shower,
it currently cannot identify gluon jets in herwig++ 2.3, which forces g → qq splitting for all
gluons. The algorithmic definition also has a tendency to reclassify jets with light quarks from
gluon splitting as quark jets, and quark jets with early hard gluon radiation as gluon jets, mixing
quark and gluon fractions.
We show the jet-flavor fractions for both definitions in figure 28 for QCD dijet, Z+jet, and
γ+jet samples. The flavor fractions in the γ+jet sample are very similar to those of Z+jet in the
pT > 200 GeV range, except for a somewhat larger fraction of directly produced charm jets.
7.2

Simulated flavor corrections

The differences in response (pT /pT, ptcl ) for different jet flavors arise mainly from variations in jet
fragmentation energy and variations in particle composition of the jet. Softer jet fragmentation
results in more particles outside the detector acceptance. With respect to particle composition, the
neutral hadron fraction of the jet, f nh , is seen to affect the response most. Jets from u and d quarks
have the highest response, while those from gluons have the lowest, as a result of gluons fragmenting
into the largest number of soft particles. The response values for heavy-flavor jets from c and b

– 43 –

2017 JINST 12 P02014

is evaluated after the global fit with Z+jet and γ+jet data in the range of about 30 < pT < 700 GeV,
and multijet data extending to over 1 TeV. The uncertainty in JEC η dependence derives mainly from
ISR+FSR modeling, the effect of JER, and the uncertainty in fitting any additional pT dependence,
with a total uncertainty rising from less than about 0.5% at |η| < 2.5 up to 2.5% at |η| > 3.
The residual corrections have been quite stable since 2011, when improvements to simulation
and reconstruction algorithms were implemented after the first year of data-taking in 2010, after
a hardware intervention in the HF readout helped reducing the rate of anomalous signals in the
readout photomultiplier tubes. The most significant changes are seen at high pT in the barrel, where
we attribute the increase in residual corrections to a drop in the HCAL scale in data. The changes
between 7 TeV in 2011 and 8 TeV in 2012 in the endcaps are at least partly attributable to the pT
dependence of the η-dependent corrections implemented at 8 TeV in 2012 for pT > 60 GeV, and
the changes in HF are due to statistical fluctuations.

## PDF page 47

1.3

R = 0.5, PF+CHS
20 fb-1 (8 TeV)
5 fb-1 (7 TeV)
36 pb-1 (7 TeV)

|η| = 0

1.2
1.1
1
0.9
20

100 200

p

T,corr

-1

-1

Residual response correction

1.4 CMS

19.7 fb-1 (8 TeV) + 36 pb-1 + 4.9 fb-1 (7 TeV)

1.4 CMS
1.3

p

T,corr

1.2
1.1
1
0.9
0 0.5 1 1.5 2 2.5 3 3.5 4 4.5 5

1000

|η|

(GeV)

-1

-1

1.3

p

T,corr

= 100 GeV

R = 0.5, PF+CHS
20 fb-1 (8 TeV)
5 fb-1 (7 TeV)
36 pb-1 (7 TeV)

1.2
1.1
1
0.9

-1

-1

19.7 fb (8 TeV) + 36 pb + 4.9 fb (7 TeV)

Residual response correction

Residual response correction

19.7 fb (8 TeV) + 36 pb + 4.9 fb (7 TeV)

1.4 CMS

= 30 GeV

R = 0.5, PF+CHS
20 fb-1 (8 TeV)
5 fb-1 (7 TeV)
36 pb-1 (7 TeV)

0 0.5 1 1.5 2 2.5 3 3.5 4 4.5 5

1.4 CMS
1.3

p

T,corr

= 1000 GeV

R = 0.5, PF+CHS
20 fb-1 (8 TeV)
5 fb-1 (7 TeV)
36 pb-1 (7 TeV)

1.2
1.1
1
0.9
0 0.5 1 1.5 2 2.5 3 3.5 4 4.5 5

|η|

|η|

Figure 27. Residual data/simulation response correction factors for the 2012 data collected at 8 TeV for PF
jets with CHS and R = 0.5, compared to corrections at 7 TeV corresponding to 36 pb−1 of data taken in
2010 [13] and 5 fb−1 taken in 2011 [46]. The comparison is shown at |η| = 0 versus pT,corr (top left), and
as a function of |η| for pT,corr = 30 GeV (top right), pT,corr = 100 GeV (bottom left), and pT,corr = 1000 GeV
(bottom right). The plots are limited to a jet energy E = pT cosh η = 3500 GeV so as to show only correction
factors for reasonable pT in the considered data-taking period.

quarks are in between those for u/d and g jets due to additional soft particles from heavy-flavor
hadron decays compared to u and d jets. As a reminder, the CMS definition of jet energy response
R excludes neutrinos, which would otherwise lower b and c jet response significantly. The jets from
strange quarks also have relatively low response due to the high probability of producing long-lived
strange neutral hadrons (mainly KL0 ) with significant pT . This effect is specific to PF jets, which
have a larger difference between charged and neutral hadron responses than calorimeter jets.
These effects are quantitatively demonstrated for jet response in figure 29 (left) for Z+jet events
with 50 < pT,Z < 70 GeV, |η jet | < 1.3, and pT,jet2 < 0.3pTZ , where the jets are fully calibrated with
the corrections relevant for simulated jets, as discussed in the previous sections. The biggest differ-

– 44 –

2017 JINST 12 P02014

Residual response correction

19.7 fb-1 (8 TeV) + 36 pb-1 + 4.9 fb-1 (7 TeV)

## PDF page 48

CMS Simulation

(8 TeV)

Dijet, |η|<1.3, α<0.2
Pythia6 Z2*

CMS Simulation

(8 TeV)

Al Ph
Quark
Gluon
1
Charm
Bottom
0.8
Unmatched

Flavor fraction

Al Ph
Quark
Gluon
1
Charm
Bottom
0.8
Unmatched

Flavor fraction

Flavor fraction

CMS Simulation

Z+jet, |η|<1.3, α<0.2
MG+Pythia6 Z2*

Al Ph
Quark
Gluon
1
Charm
Bottom
0.8
Unmatched

0.6

0.6

0.6

0.4

0.4

0.4

0.2

0.2

0.2

0

60

200

100

0

2000

1000

pT,jet (GeV)

40 50

100

200

p

T,Z

0

300

40

(GeV)

(8 TeV)

γ +jet, |η|<1.3, α<0.2
Pythia6 Z2*

200 300

100

pT,γ (GeV)

1.08

CMS

Simulation

I

8 TeV

|η| < 1.3

Leading jet PF energy fraction

Leading jet response pT, jet /pT, ptcl

I
1.10

50 < pT,Z < 70GeV
Anti-kT R=0.5 PF+CHS

Herwig++ Tune EE3C
Pythia 6 Tune Z2*

1.06
1.04
1.02
1.00

d

u

s

c

b

1.0
0.8

Flavor (physics definition)

CMS

|η| < 1.3

Simulation

0.6
µ
e
γ
Charged hadron
Neutral hadron

0.4
0.2
0.0

g undef.

8 TeV

d

u

s

c

b

g undef.

Flavor (physics definition)

Figure 29. Comparison of jet response (left) and simulated composition (right) for different flavors of leading
jets in Z+jet events with 50 < pTZ < 70 GeV, |η jet | < 1.3, and α = 0.3 (defined in eq. (6.9)). The response
values are compared for pythia 6.4 and herwig++ 2.3, the composition is from pythia 6.4.

ences between pythia 6.4 and herwig++ 2.3 are observed for the gluon jets. The response is higher
than unity for all flavors, since Z+jet events have lower contributions from the underlying event than
dijet events, leading to a small bias from the hybrid jet area method, defined in section 4.3. Moreover,
as shown in figure 28, Z+jet events have a smaller gluon fraction (25% for pT = 60 GeV) with respect
to dijet (65% for pT = 60 GeV) events, and the different response of gluons and light-quark jets, visible in figure 30 (right), raises the average response for Z+jet events. Figure 29 (right) demonstrates
the simulated jet composition for different jet flavors. The s-quark jets have higher neutral hadron
fractions due to KL0 production, while the neutrino production in c and b jets is evident through the
associated muons and electrons. The softer fragmentation of gluon jets has relatively little impact
on the particle composition, but results in low effective response for the neutral hadrons Rnh .

– 45 –

2017 JINST 12 P02014

Figure 28. Jet-flavor fractions in the physics (Ph) and algorithmic (Al) flavor definitions for QCD dijet (left),
Z+jet (middle), and γ+jet (right) samples. As explained in section 6, the variable α = pT, 3rd jet /pT,ave for
dijet events and α = pT, 2nd jet /pT,γ/Z for Z+jet and γ+jet events.

## PDF page 49

(8 TeV)

CMS

1.04

Simulation

(8 TeV)

0.08

Rud-Rg

Jet flavor correction

1.06

QCD Monte Carlo
Anti-kT R=0.5, PF+CHS
0 < η < 1.3

0.07

CMS

Anti-kT R=0.5, PF+CHS

Simulation

|η|<1.3
Parton Flavor
PYTHIA Z2*
HERWIG++ EE3C

0.06

1.02

0.05

1

0.04
all
ud
s
c
b
g

0.98

0.94

30

100 200

p

0.02
0.01

1000 2000
T, corr

(GeV)

0

30

100

200

1000

pT, ptcl (GeV)

Figure 30. Residual jet-flavor correction factor as a function of jet pT, corr from pythia 6.4 tune Z2*, derived
on top of inclusive JEC and defined relative to the QCD flavor mixture (left). The neutrinos are excluded
from particle jets, which brings c- and b-jet response in between that of light quarks and gluons. The lines
show the parameterizations used for residual jet-flavor corrections. Difference in light-quark and gluon jet
response as a function of jet pT, corr , as predicted by pythia 6.4 and herwig++ 2.3 (right).

Figure 30 (left) shows the inverse of the response for different flavors versus pT , relative to the
one for the QCD flavor mixture. The relative behavior of the differences has a weak dependence
on pT , but the absolute differences become smaller at high pT . This can be explained by the
asymptotic rise of the neutral hadron response towards unity at high pT and detector acceptance
effects becoming less significant for high-pT jets.
While pythia 6.4 and herwig++ 2.3 agree well on quark flavor response, there are significant
differences in the gluon response modeling. A useful metric for the JES sensitivity to flavor response
modeling is the difference in light-quark (uds) and gluon jet response, shown in figure 30 (right).
The flavor sensitivity of the CMS PF algorithm is much reduced with respect to the CALO jets
reconstruction, as was demonstrated in ref. [13].
7.3

Flavor uncertainties

We investigate the jet fragmentation and flavor response differences by comparing pythia 6.4 tune
Z2* and herwig++ 2.3 tune EE3C in balanced QCD dijet events. These two tunes have been shown
to cover differences between data and simulation in many studies of jet structure and fragmentation,
in particular for the variables used for quark and gluon tagging [49]. The jet flavors are tagged with
the matching parton flavor, based on the physics definition. As shown in figure 31, we observe
the largest response differences for the gluon jets, while the light-quark and heavy-flavor jets are in
good agreement in both MCs.
The parameterized response differences as a function of η and pT , combined with the flavor
fractions in figure 28, are propagated through the fitting procedure used for data-based residual
corrections to evaluate the systematic uncertainties from jet flavor. Jets in the barrel reference
region |η| < 1.3 have flavor uncertainty only when the flavor mixture differs from the Z/γ+jet

– 46 –

2017 JINST 12 P02014

0.96

0.03

## PDF page 50

19.7 fb-1 (8 TeV)

CMS

Dijet, |η| < 1.3
Parton flavor

Simulation

Gluon
Quark
Charm
Bottom

1.04
1.02
1
0.98

10

Unmatched
Envelope

100

Herwig++ EE3C / Pythia6 Z2*

1.06

1000

1.04

CMS

|η| < 1.3
Parton flavor

Simulation

Dijet
Z+jet
20% glue
Gluon
Quark

1.03
1.02
1.01
1
10

100

1000

Jet p (GeV)

Jet p (GeV)
T

T

Figure 31. Left: ratio of jet responses in pythia 6.4 (tune Z2*) and herwig++ 2.3 (tune EE3C) versus jet
pT , for pure jet flavors selected using the physics definition, where the shaded envelope highlights the largest
differences observed for the gluon jets. Right: pythia 6.4/herwig++ 2.3 response differences as a function of
jet pT for QCD dijet and Z/γ+jet flavor mixtures calculated from the parameterized flavor response differences
(diamonds) and compared to the full simulation for dijet (squares) and Z+jet (circles) samples. The “20%
glue” corresponds to the effective Z/γ+jet flavor mixture at pT = 200 GeV, which has 20% of gluons. The
ratio of the responses is also shown for pure gluon (dashed curve) and quark (dot-dashed curve) jets.

flavor mixture used in the data-based methods, which is roughly 20% gluons at pT = 200 GeV.
The η-dependent corrections influence the jet-flavor systematics through both the tag and the probe
jet. The flavor mixture of the central tag jet is different from that in Z/γ+jet calibration samples,
which leads to a flavor uncertainty for dijets within the reference region in the barrel. This barrel
uncertainty for the dijet measurement is then propagated to the more forward regions through the
dijet-based η-dependent corrections, with additional flavor uncertainties relative to the dijet flavor
mixture for other samples.
The total flavor uncertainty ∆Rflavor for any given flavor mixture is estimated based on pure
flavor response R f (in pythia 6.4 Z2* and herwig++ 2.3) and flavor fractions Ff in pythia 6.4 Z2*:
∆Rflavor (pT, η) = R̂mix (pT, η) − Rref (pT, η),

(7.1)

∑

(7.2)

where
R̂mix (pT, η) =

(R f ,herwig++ (pT, η) − R f ,pythia6 (pT, η))Ff ,mix (pT, η),

f

(
)
Rref (pT, η) = R̂Z+jet (200 GeV, 0) + R̂dijet (pT, η) − R̂dijet (pT, 0) .

(7.3)

The symbol R̂ indicates the linear combination of response differences for a given flavor mixture,
and Rref is relative to the Z/γ+jet flavor mixture used in the data-based methods. The various flavor
uncertainties are compared in figure 32. This calculation returns by design zero flavor uncertainty
for the Z/γ+jet flavor mixture at pT = 200 GeV and η = 0 (about 20% gluons), which is where the

– 47 –

2017 JINST 12 P02014

Herwig++ EE3C / Pythia6 Z2*

19.7 fb-1 (8 TeV)

## PDF page 51

CMS
6
4

R=0.5 PF+CHS
|η | = 0
jet

Gluons
QCD mixture
Z+jet mixture
γ +jet mixture
Light quarks
Bottom quarks

2

19.7 fb-1 (8 TeV)

JEC uncertainty (%)

JEC uncertainty (%)

19.7 fb-1 (8 TeV)

CMS
6
4

−2

−2
−4

1000

−2

0

2

4

p (GeV)
-1

-1

CMS
R=0.5 PF+CHS

4 |ηjet| = 2.7

Gluons
QCD mixture
Z+jet mixture
γ +jet mixture
Light quarks
Bottom quarks

2

19.7 fb (8 TeV)

JEC uncertainty (%)

JEC uncertainty (%)

19.7 fb (8 TeV)

6

CMS
6
R=0.5 PF+CHS

4 pT = 100 GeV

0

−2

−2
100 200

−4

1000

p (GeV)

Gluons
QCD mixture
Z+jet mixture
γ +jet mixture
Light quarks
Bottom quarks

2

0

20

η

jet

T

−2

0

2

4

η

jet

T

Figure 32. Systematic uncertainties in jet energy corrections for various flavor mixtures (QCD dijets, Z+jet
and γ+jet) and pure flavors (gluons, light quarks and bottom quarks) as a function of jet pT (left, for fixed
|η jet | = 0, top, and |η jet | = 2.7, bottom) and η jet (right, for fixed pT = 30 GeV, top, and 100 GeV, bottom).
The sign of the systematic source indicates the sign of the pythia 6.4 tune Z2* and herwig++ 2.3 tune EE3C
difference. The shaded band shows gluon flavor response uncertainty symmetrically around zero.

constant absolute data/simulation scale factor is effectively determined in the (pT , η, flavor) space.
For the dijet sample the flavor uncertainty is constant versus η by design, but increases with pT away
from the effective flavor reference point. For other samples the flavor uncertainty depends both on
pT and η. The respective flavor uncertainties are provided for the Z+jet (FlavorZJet), γ+jet (FlavorPhotonJet), and dijet (FlavorQCD) mixtures as well as for the pure flavors (FlavorPureGluon,
FlavorPureQuark, FlavorPureCharm, FlavorPureBottom). The flavor uncertainties are reliably
determined only at pT > 30 GeV, where the flavor assignment for the leading jets has a small
ambiguity. However, the flavor differences are reduced at pT < 30 GeV in PF so the uncertainty at
pT = 30 GeV is used as a conservative upper limit on flavor uncertainties at lower pT as well.

– 48 –

2017 JINST 12 P02014

0

100 200

T

2

0

20

R=0.5 PF+CHS
p = 30 GeV

Gluons
QCD mixture
Z+jet mixture
γ +jet mixture
Light quarks
Bottom quarks

## PDF page 52

19.7 fb-1 (8 TeV)

Events

CMS
2500

α < 0.3, pZT > 30 GeV

Data
Z+b
Z+c
Z+l
Others
tt

2000

19.7 fb-1 (8 TeV)

CMS
MPF, α < 0.3

1500

1000

MPF, α → 0
(Stat. unc.)

RpT , α < 0.3

Data/MC

0
0
1.5

0.2 0.4 0.6 0.8

1

1.2 1.4 1.6 1.8

2

RMPF
RpT , α → 0

1
0.5
0

0.2 0.4 0.6 0.8

1

1.2 1.4 1.6 1.8

0.92 0.94

2

0.96 0.98

1

1.02 1.04

1.06 1.08

Ccorr

RMPF

Figure 33. Distribution of the Z+b-jet response using the MPF method with a fixed requirement α < 0.3
(left). Data-to-simulation ratio of the Z+b-jet response relative to the inclusive Z+jet sample with the MPF
and the pT -balance methods (right).

7.4

Z+b-jet balance

To check the flavor corrections and their uncertainties in data, we use a Z+b-jet pT -balancing
technique [50] that is a straightforward extension of the Z+jet balancing methods described in
section 6.3. In addition to the Z+jet event selection criteria described in section 3.2, the leading
jet is required to be b-tagged with the combined secondary vertex tagger at the medium working
point [31], and the b-jet response is determined with both the MPF and the pT -balance methods,
as in the nominal Z+jet analysis described in section 6.3. The purity of the Z+b sample is about
70–80% and the MPF response distribution is well modeled by simulation, as shown in figure 33.
To reduce systematic uncertainties, the main result is reported as a ratio of response in the Z+b-jet
sample to that in inclusive Z+jet sample. This check is particularly important for the top quark mass
measurements, which uses light-quark jets from W boson decays to constrain the energy scale for
b jets from the top quark decay t → Wb, assuming the same momentum scale for light-quark jets
and b jets with similar kinematics [6].
The most precise result is obtained using the MPF method with a fixed requirement α < 0.3
(’MPF, α < 0.3’ in figure 33). This gives a residual b-jet correction of Ccorr = 0.998 ± 0.004 (stat) ±
0.004 (syst) relative to pythia 6.4 tune Z2*, which is consistent with unity and comparable in
precision to the current b-jet flavor uncertainty of about 0.5%, shown in figure 32. The results
from the response extrapolated to α → 0 (bottom symbols in figure 33 right) and from the pT balance method (RpT ) are consistent with the central MPF result. The systematic uncertainties,
which include b-tagging efficiency and mistag rate, lepton scales, ISR- and FSR-related effects, and
jet fragmentation, are dominated by the uncertainty in the fraction of pT carried by the neutrinos

– 49 –

2017 JINST 12 P02014

(Total unc.)

500

## PDF page 53

19.7 fb-1 (8 TeV)

1.04

19.7 fb-1 (8 TeV)
1.05

CbMPF/C inc
MPF

CbMPF

1.05

CMS

1.04

1.03

CMS

1.03

1.02

1.02

1.01

1.01

1

1

0.99

0.99

0.98

0.98

b-tagged
0.97

inclusive

0.96
0.95

20 40

0.96
0.95

60 80 100 120 140 160 180 200

Z boson p (GeV)

20 40

60 80 100 120 140 160 180 200

T

Z boson p (GeV)
T

Figure 34. Residual correction factors (calculated as the ratio of the MC and data MPF response) as a
function of Z boson pT , for Z+b-jet and Z+jet events with α < 0.3 (left), and their ratio (right).

produced in semileptonic decays of heavy-quark hadrons, which contributes 0.32% compared to
0.21% from all the other sources combined.
The corresponding result, as derived from herwig++ 2.3 tune EE3C, is
Ccorr = 1.005 ± 0.006 (stat) ± 0.004 (syst),

(7.4)

and has a systematic uncertainty comparable with the one obtained for pythia 6.4. The results of
Ccorr for pythia 6.4 and herwig++ 2.3 differ by 0.5%, which is consistent with the expected flavor
differences shown in figure 31.
To check for a possible pT -dependence, the residual b-jet correction is shown as a function of
pT in figure 34, where the uncertainties are statistical and systematic. This figure shows the MPF
results with the fixed α < 0.3 requirement for the Z+b-jet and inclusive Z+jet events separately (left)
and for their ratio (right), where most systematic uncertainties cancel out. As a result, while the
uncertainties in figure 34 (left) are dominated by the systematic contributions, the uncertainties in
figure 34 (right) are mostly statistical. The separate results are not corrected for the pT -dependence
of the absolute JES, which cancels in the ratio. The ratio is compatible with the assumption of
no pT -dependence, although it is limited by statistical uncertainties at the expected level of the
systematic flavor uncertainties.

8

Jet pT resolution

The jet pT resolution is relatively poor compared to the resolution of many other physics objects
(electrons, muons, photons), and the biases caused by jet resolution smearing can be important
for steeply falling spectra and for resonance decays. In this section we present a determination of
particle-level JER from MC simulation and the results from data-based methods for extracting a
data/MC scale factor. The particle-level JER is defined as the width (estimated with a Gaussian

– 50 –

2017 JINST 12 P02014

0.97

## PDF page 54

fit) of the distribution of pT, reco /pT, ptcl , where pT, reco and pT, ptcl are the transverse momenta of the
reconstructed and corresponding particle-level jets. JEC are applied before deriving JER.
8.1

Methods

Our measurement of JER is an extension of the methods used for measuring JES, but instead of
looking at the mean of the response distribution, we are interested in its width. In addition, we need
to correct for effects that do not produce an overall shift in the mean, but can widen the distribution.
For γ+jet (and Z+jet) events we can expand the pT balance as follows:
pT, jet
pT, jet pT, jet ptcl pT,γ ptcl
=
,
pT,γ
pT, jet ptcl pT,γ ptcl pT,γ

(8.1)

where pT, jet and pT,γ are the reconstructed jet and photon transverse momenta, and pT, jet ptcl and
pT,γ ptcl the corresponding transverse momenta at particle level. For a sum of independent and
identically distributed (IID) random variables, the quadratic summation of widths applies. For the
product of eq. (8.1) we can take logarithms and apply log(1 + X ) ≈ X for X ≪ 1, which means that
the normally distributed variables are also log-normally distributed with the same width σ. In the
following, the symbols ⊕ and ⊖ indicate quadratic sum and subtraction respectively. For the widths
σ we then have
(
)
(
)
(
)
(
)
pT,γ ptcl
pT, jet
pT, jet
pT, jet ptcl
σ
=σ
⊕σ
⊕σ
, i.e.
(8.2)
pT,γ
pT, jet ptcl
pT,γ ptcl
pT,γ
σ pT
⊕ σUE+OOC+ISR+FSR ⊕ σγ .
(8.3)
σB =
pT
In equation (8.3), all widths, apart from σ pT , are relative quantities. The first part on the
right-hand side is identified with the particle-level JER, σJER = σ pT /pT . The second term is
the combined effect of UE, OOC, ISR+FSR, and presence of neutrinos. The final term is due
to the photon pT resolution and FSR, σγ . After extrapolating the secondary jet activity to zero,
or equivalently correcting the measured resolution with the effective k rad = σ B (α → 0)/σ B , the
effects of ISR and FSR become negligible. In this case the second term reduces to the effects from
UE and OOC alone, and is referred to as the particle level imbalance (PLI), σPLI :
σ B k rad = σJER ⊕ σPLI ⊕ σγ .

(8.4)

Equation (8.4) can be rearranged as follows:
σJER = σ B k rad ⊖ σPLI ⊖ σγ .

(8.5)

k rad is determined from data by fitting the resolution as a function of secondary jet activity
α = pT, 2nd jet /pT,γ , while σPLI and σγ are taken from MC simulation, after extrapolating to α → 0
for consistency. Since k rad σγ is negligible compared to other effects, it is implicitly absorbed in the
σPLI factor.
The quadratic addition and subtraction of widths is strictly correct only for RMS, or for
resolutions that are approximately Gaussian. In practical cases, the dominant terms (σ pT , σ B k rad )
can be determined consistently from the RMS or a fit to the Gaussian core of the distribution,

– 51 –

2017 JINST 12 P02014

B=

## PDF page 55

while the smaller contributions (σPLI , σγ ) should typically use RMS. This is because the small
contributions (with sufficiently steeply falling power-law tails) get folded into the Gaussian core of
the distribution, as predicted, e.g., by the Central Limit Theorem (CLT), which states that the sum
of multiple IID random variables tends to a Gaussian distribution, provided their power-law tails fall
off sufficiently steeply (x −m , with m > 3). For a variable that can be thought of as a multiplicative
product of many independent random variables, the CLT applies in the logarithmic domain.
For dijet events the factorization is similar, except that JER now appears once for each jet,
and PLI is derived from the asymmetry between two particle jets and includes the UE and OOC
contributions twice. The dijet asymmetry [13] is defined as
pT, 1st jet − pT, 2nd jet
,
pT, 1st jet + pT, 2nd jet

(8.6)

and its resolution σ A is given by
σ A k rad =

σJER,probe σJER,tag
⊕
⊕ σPLI,dijet,
2
2

(8.7)

where σPLI,dijet is the resolution of the asymmetry variable, built with the momenta of particle-level
ptcl ptcl
jets, and extrapolated to zero additional jet activity σPLI,dijet = σ A k rad . It is related to the single
jets PLI resolutions through 2σPLI,dijet = σPLI,tag ⊕ σPLI,probe .
For the special case where both jets are in the same region and share the same JER (σJER,probe =
σJER,tag = σJER ), we obtain:
√
σJER = 2(σ A k rad ⊖ σPLI,dijet ).
(8.8)
For the case of one central and one forward jet, we can solve for the forward JER by subtracting
the central JER determined from eq. (8.8):
σJER,forward = 2σ A k rad ⊖ 2σPLI,central−forward ⊖ σJER,central .

(8.9)

In this case the σPLI,central−forward is σPLI,dijet , determined consistently for the same combination
of central and forward jets.
8.2

Simulated particle-level resolution

The jet pT resolution is reasonably Gaussian, although some nongaussian low-response tails are
present, e.g., due to rare detector effects such as inactive areas of the ECAL and to high-pT particles
punching through the HCAL. At low pT symmetric tails appear due to combinations where two
generator jets produce a single reconstructed jet, or vice versa. Such effects are typically wellmodeled by a double-sided Crystal Ball function [51], as seen in figure 35. Low tails in response
measurements are also commonly produced by neutrinos from semileptonic decays of heavy-flavor
hadrons. This does not apply to particle-level resolutions, because CMS particle jets exclude
neutrinos, but this does impact the dijet balance method used to measure JER in data.
We define the particle-level JER in simulation as the σ of a Gaussian fit to the pT, reco /pT, ptcl
distribution in the range [m − 2σ, m + 2σ], where pT, reco and pT, ptcl are the reconstructed jet pT and
generated particle-level jet pT , respectively, and m and σ are the mean and width of the Gaussian
fit, determined with an iterative procedure. To maximize matching efficiency while still ensuring a

– 52 –

2017 JINST 12 P02014

A=

## PDF page 56

10
1

97 ≤ p

T,ptcl

< 114 GeV

|η| < 0.5, PF
R = 0.5
∆R < R / 2

CMS Simulation

(8 TeV)

1 / (N dRptcl)

1 / (N dRptcl)

CMS Simulation

MC
Gaussian
Crystal Ball

10
1

967≤ p

(8 TeV)

< 1032 GeV

T,ptcl

|η| < 0.5, PF
R = 0.5
∆R < R / 2

MC
Gaussian
Crystal Ball

10−1

10−2

10−2

10−3

10−3

10−4
0 0.2 0.4 0.6 0.8 1 1.2 1.4 1.6 1.8 2

10−4
0 0.2 0.4 0.6 0.8 1 1.2 1.4 1.6 1.8 2

Rptcl = pT / pT,ptcl

Rptcl = pT / pT,ptcl

Figure 35. Jet pT resolution distributions in the barrel for two bins of jet pT . ∆R indicates the distance
parameter value used for matching reconstructed jets to the corresponding particle-level jets. The nongaussian
tails due to inactive areas of the ECAL and HCAL punchthrough become more visible for narrow high-pT jets
with small core resolution. The Gaussian core resolution is fit to within ±2σ (solid line) and its extrapolation
is indicated with a dotted line. The tails are well modeled by a double-sided Crystal Ball function.

unique match, the reconstructed and the generated jets are required to be within ∆R < R/2 of each
other, with R being the jet distance parameter.
The nongaussian tails increase the RMS of the distribution, and the differences affect the databased dijet asymmetry, where two JER distributions are folded together with other (non) Gaussian
distributions. The dijet asymmetry is effective in symmetrizing the tails, and according to the CLT
the folded distribution will asymptotically approach a Gaussian distribution. The treatment of these
effects will be discussed in more detail in the next section.
The particle-level JER in simulation with a pileup profile matched to 2012 (8 TeV) data is
presented in figure 36 in bins of true number of PU interactions µ. The particle-level JER in
simulation is parameterized with the “N SC” fit for calorimeter resolutions, where N is for noise
√
(and pileup), S is for stochastic fluctuations that scale as 1/ E, and C is a constant term with no pT
scaling (e.g., intercalibration):
√
σ pT
sgn(N )N 2 S 2
=
+
+ C2.
(8.10)
pT
pT
pT2
As shown already in [13], for PF jets the possibility of having a negative N 2 term improves
the description of the jet resolutions at low PU. As visible in figure 36, in the absence of pileup
larger jets have better resolution due to several effects. These include better jet angular resolution
(relevant for pT < 30 GeV) and a smaller constant term from intercalibration, due to the jet energy
being spread over more particles. These small gains are quickly negated in the presence of pileup,
to which larger jets are more sensitive.
The noise term is very sensitive to the PU in jets, with each additional PU interaction contributing about 1 GeV of smearing in quadrature for R = 0.5 jets. The PU offset increases approximately

– 53 –

2017 JINST 12 P02014

10−1

## PDF page 57

CMS Simulation

(8 TeV)

JER

JER

0.5

Anti-kT, R=0.7 (PF+CHS)
|η|<1.3
µ=0
0 ≤ µ < 10
10 ≤ µ < 20
20 ≤ µ < 30
30 ≤ µ < 40

0.45
0.4
0.35
0.3

0.5

CMS Simulation

0.4
0.35
0.3

0.2

0.2

0.15

0.15

0.1

0.1

0.05

0.05
20 30

100 200

1000

pT, ptcl (GeV)

0

20 30

100 200

1000

pT, ptcl (GeV)

Figure 36. JER versus pT in the barrel for varying levels of pileup µ. The results are shown separately for
PF+CHS jets with size R = 0.7 (left), and for PF+CHS jets with size R = 0.5 (right).

linearly with number of collisions and jet area, µA, so that the noise from pileup is proportional to
√
µA. In contrast, the stochastic and constant terms are stable with respect to pileup, as shown in
figure 37.
The JER also depends to some extent on the jet flavor. Gluon jets are wider than quark jets,
and therefore less sensitive to local η–φ intercalibration of the detector. This is manifested as a
smaller constant term and better JER at high pT , as seen in figure 38 (left), where the constant term is
0.0338±0.0002 for gluons, and 0.0406±0.0002 for quarks. The intrinsic JER of c and b jets is similar
to uds jets when excluding neutrinos at particle level. However, when neutrinos are included, as in
figure 38 (right), the neutrinos produced in semileptonic decays of heavy-quark hadrons produce
long response tails for the data-based measurements and cause substantial smearing of JER.
8.3

Dijet asymmetry

The jet pT resolution in data is measured with the dijet asymmetry method [13] versus pT,ave :
A=

pT, 1st jet − pT, 2nd jet pT, 1st jet − pT, 2nd jet
=
,
pT, 1st jet + pT, 2nd jet
2pT, ave

(8.11)

where the width of the asymmetry distribution σ A is related to the single jet resolutions as explained
in equations (8.6)–(8.9).
The measured asymmetry distributions are Gaussian-like at low pT , but some tails are evident
at high pT , as seen in figure 39 (left). These tails are reasonably well modeled by simulation. The
particle-level JER in simulation is defined as a Gaussian fit to the core of the distribution within 2σ
so we limit the impact of these tails and of outlier events by using a truncated RMS with 98.5% of
the events in the core of the distribution for data and simulation. The truncation value is chosen to
ensure that the core of the distribution is reasonably well described by a Gaussian. The resolutions
are then extrapolated to zero secondary jet activity for data, reconstructed MC simulation, and
generated MC simulation, as shown in figure 39 (right).

– 54 –

2017 JINST 12 P02014

0.25

0

Anti-kT, R=0.5 (PF+CHS)
|η|<1.3
µ=0
0 ≤ µ < 10
10 ≤ µ < 20
20 ≤ µ < 30
30 ≤ µ < 40

0.45

0.25

(8 TeV)

## PDF page 58

JER parameter

14
12

CMS Simulation

(8 TeV)

PF PF+CHS
N (GeV)
S ( GeV) × 10
C (1) × 100

|η| < 1.3
R=0.2-1.0

10
8

4
2

2

(A = 〈Ajet 〉 = πR )

σ
pT =

N0 ⋅|N |+σ 2PUµA
0

p2

T

S2
2
+p + C
T

0
0 10 20 30 40 50 60 70 80 90 100

µ ×A

(8 TeV)

0.3

CMS
0.25

Simulation

Anti-kT, R=0.5 (PF+CHS)
|η| < 1.3

JER

JER

Figure 37. JER parameters (N, S, C; see text) fitted in bins of µ for various values of the distance parameter
R (R = 0.2–1), as a function of their average value of pileup times jet area (µA). The results are compared
between PF (solid symbols) and PF+CHS (open symbols). The dotted and dash-dotted curves represent the
fit for PF and PF+CHS jets, respectively.

0.2

CMS
0.25

gluons
uds quarks
cb quarks

0.15

0.1

0.1

0.05

0.05
excluding ν's in particle jet

30

100

Simulation

Anti-kT, R=0.5 (PF+CHS)
|η| < 1.3
gluons
uds quarks
cb quarks

0.2

0.15

0

(8 TeV)

0.3

including ν's in particle jet

200
p

T,ptcl

0

1000
(GeV)

30

100

200
p

T,ptcl

1000
(GeV)

Figure 38. True JER in simulation for different jet flavors in the γ+jet sample, for jets with |η| < 0.5.
The distributions are shown for particle-level jets with no neutrinos (left), and with neutrinos exceptionally
included (right) to demonstrate the large fluctuations this induces for c and b jets.

– 55 –

2017 JINST 12 P02014

6

## PDF page 59

19.7 fb-1 (8 TeV)

105

Anti-kT (R=0.5) PF+CHS Jets
0.0 ≤ |η| ≤ 0.5, 242 ≤ pT, ave ≤ 270 (GeV)
α ≤ 0.125

104
3

10

102

19.7 fb-1 (8 TeV)

CMS

σA , σptcl
A

Events

CMS

Anti-kT (R=0.5) PF+CHS Jets
0.0 ≤ |η| ≤ 0.5, 242 ≤ pT, ave ≤ 270 (GeV)

0.1

0.08

Data
Simulation
98.5% data
98.5% simulation

0.06
0.04

10

10-1
0 0.1 0.2 0.3 0.4 0.5 0.6 0.7 0.8 0.9 1

|A|

0
0

0.05

0.1

0.15

0.2

0.25

0.3

αmax

Figure 39. Left: asymmetry distribution, eq. (8.11), for data and simulation for jets with pT ≈ 250 GeV
and |η| < 0.5. Right: asymmetry measured for various thresholds αmax , extrapolated to zero additional jet
activity, for jets with pT ≈ 250 GeV and |η| < 0.5 in data and MC simulation at the detector- and particlelevel. The light horizontal line indicates the average particle-level resolution obtained as the difference in
quadrature of MC simulation reconstructed asymmetry and particle-level imbalance, extrapolated to zero
additional jet activity.

The extrapolated asymmetry is finally corrected for the residual PLI effects, which are
significantly smaller than the asymmetry, as shown in figure 40. This final stage does not
significantly affect the data/MC ratio, as is also shown in figure 40, because the same PLI correction
is applied to both data and MC simulation. The main effect of the correction is a slight increase
in the data/MC ratio. The data/MC ratio is well-modeled by a constant fit in all the rapidity
regions. These constant data/MC scale factors are summarized in figure 41. The fit is also repeated
assuming different scale factors for the N, S (k N S ) and C (kC ) terms, which gives reasonable
results although the statistical uncertainties are too big to distinguish the two cases. The difference
between the measured scale factors k N S and kC and the central value obtained by the constant fit
is considered as a systematic uncertainty.
The systematic uncertainties in the data-based method come from three main sources: correction for ISR and FSR, particle-level imbalance, and nongaussian tails. The data/MC ratio is also
affected by the uncertainties in PU reweighting and JEC. The parameterization uncertainty comes
mainly from the potential difference between the data/MC scale factors for the noise and stochastic
terms k N S and the one for the constant terms kC . The systematic uncertainties for the data/MC
ratio are evaluated as follows:
• ISR+FSR correction: the fit shown in figure 39 (right) uses a linear extrapolation σ =
σ0 (1 + kα), which comes with an associated shape uncertainty beyond the first measured
point. As a reminder, for dijet events, α = pT, 3rd jet /pT,ave . Equation (8.11) suggests that
another good functional form would be σ = σ0 ⊕ k ′ α, which is used as an alternative model
to estimate the systematic uncertainty in the ISR+FSR correction.

– 56 –

2017 JINST 12 P02014

Data
MC (detector level)
MC (particle level)
MC (det - ptcl)

0.02

1

## PDF page 60

σJER

0.3

19.7 fb-1 (8 TeV)

CMS
Anti-kT (R=0.5) PF+CHS Jets
0.0 ≤ |η| ≤ 0.5

0.25

Data

0.2

MC

0.15

PLI correction

0.1

Data / MC

1.3
1.2
1.1
1
0.9
0.8

102

p

103

T, ave

(GeV)

Data/MC ratio

Figure 40. Extrapolated JER as a function of jet pT obtained with the asymmetry method on dijet events
for data (solid circles), reconstructed MC simulation (open squares), and particle-level simulation with PLI
(dashed line). The bottom plot shows the ratio of data over MC.

2

CMS

19.7 fb-1 (8 TeV) + 5.1 fb-1 (7 TeV)

Anti-k T (R=0.5) PF+CHS Jets

1.8

19.7 fb-1 (8 TeV)

Anti-k T (R=0.5) PF Jets

1.6

5.1 fb-1 (7 TeV)

1.4
1.2
1
0.8
0 0.5 1 1.5 2 2.5 3 3.5 4 4.5 5

|η|
Figure 41. Jet energy resolution data/MC scale factor versus |η| for dijet data collected at 8 TeV (closed
circles, solid area) compared to results at 7 TeV (open circles, dashed area).

– 57 –

2017 JINST 12 P02014

0.05

## PDF page 61

• FSR+ISR radiation: the α spectrum is not perfectly modeled in simulation, as shown in
figure 42 (left). This affects the extrapolation correction. The systematics are evaluated by
reweighting the α spectrum in simulation to match the data, and repeating the analysis.
• Particle-level imbalance: the PLI uncertainty is estimated by comparing the PLI obtained
from two different MC simulations, pythia 6.4 tune Z2* and herwig++ 2.3 tune EE3C, as
shown in figure 42 (right). Based on these results we vary the PLI by ±25% to estimate the
impact of PLI uncertainty on JER.

• PU reweighting: the PU reweighting uncertainty is estimated by changing the minimum bias
pp cross section from the nominal 69.4 to 73.5 mb when generating the target PU profile for
simulation.
• Jet energy scale: the uncertainty arising from the knowledge of JES is evaluated by scaling
up and down, according to the JEC uncertainty, all jet momenta in the simulation.
• Parameterization uncertainty: the parameterization uncertainty is estimated by considering
different scale factors for the noise term N as well as the stochastic and constant terms S and
C. Because the available range of data is not sensitive to the noise term, the noise term scale
factor is varied by 10%.
The total uncertainty varies between 2–4% in the tracker covered region |η| < 2.3, and increases
up to 6% in the endcaps and 20% in the HF, where the uncertainty is driven by the large differences
between the results based on pythia 6.4 and on herwig++.
8.4

The γ+jet balance

Complementary measurements of the jet pT resolution in data are done with the γ+jet balancing
versus pT,γ :
pT,jet
B=
.
(8.12)
pT,γ
The width of the balance distribution can be written as a convolution of the jet pT resolution
with additional smearing effects, as in eq. (8.7) for the case of dijets:
σ B = σ ⊕ σISR+FSR ⊕ σPLI .

(8.13)

The JER is extracted from data and MC simulation that are binned in exclusive bins of α.
In the procedure, σPLI is fixed to the value obtained from a fit to the particle-level imbalance.
The results from the photon+jet analysis are shown in figure 43, compared to the 7 TeV dijet data
from 2011 (left) and to the 8 TeV dijet results from 2012 (right).
The following systematic uncertainties have been considered for γ+jet balancing:
• QCD dijet background: the uncertainty from QCD dijet contamination in the γ+jet sample
is estimated by measuring JER with and without the dijet simulated sample added to the γ+jet
sample.

– 58 –

2017 JINST 12 P02014

• Non-Gaussian tails: the uncertainty from nongaussian tails is estimated by changing the
nominal 98.5% truncation for RMS to 97%.

## PDF page 62

19.7 fb-1 (8 TeV)

CMS

Anti-kT (R=0.5) PF+CHS Jets
0.0 ≤ |η| ≤ 5.0, ∆φ > 2.7

Data
Simulation

108

0.15

σA,gen(α → 0)

Events

1011
1010

106
4

10

19.7 fb-1 (8 TeV)

CMS
Anti-kT (R=0.5) PF+CHS Jets
0.0 ≤ |η| ≤ 0.5

0.1

Pythia
Herwig

0.05

Data/Sim.

1
1.4
1.2
1
0.8
0.6
0

0.1

0.2

0.3

α

0
1.4
1.2
1
0.8
0.6
102

p

103

T, ave

(GeV)

1.5

-1

CMS

-1

19.7 fb (8 TeV) + 5.1 fb (7 TeV)

Data/MC ratio

Data/MC ratio

Figure 42. Left: the α distribution in data (circles) and simulation (histogram), with the function used for
simulation reweighting overlaid on the ratio of data over simulation in the bottom plot. Right: comparison of
particle-level imbalances σ A,gen (α → 0) in pythia 6.4 tune Z2* and herwig++ 2.3 tune EE3C as a function
of jet pT,ave . The bottom plot shows the ratio of pythia over herwig.

Anti-kT (R=0.5) PF+CHS Jets

1.4
1.3

19.7 fb-1 (8 TeV) γ +jet
Anti-kT (R=0.5) PF Jets
5.1 fb-1 (7 TeV) dijet

1.2

2

19.7 fb-1 (8 TeV)

CMS
Anti-k T (R=0.5) PF+CHS Jets

1.8

19.7 fb-1 (8 TeV) dijet
19.7 fb-1 (8 TeV) γ +jet

1.6
1.4

1.1

1.2
1

1
0.9
0.8
0

0.5

1

1.5

2

0.8
0 0.5 1 1.5 2 2.5 3 3.5 4 4.5 5

|η|

|η|

Figure 43. Data/MC scale factors for the jet pT resolution as a function of |η|, determined from 8-TeV γ+jet
data (hatched boxes) compared to those obtained from dijet data (solid boxes) at 7 TeV (left) and at 8 TeV
(right).

– 59 –

2017 JINST 12 P02014

10

Pythia / Herwig

2

## PDF page 63

• Flavor uncertainty: the poor resolution for c and b jets when including neutrinos at particle
level, as shown in figure 38, can bias the JER measurement if the flavor fractions in data and
simulation differ. To estimate this uncertainty, the quark and gluon fractions are varied by
±10%.
• Out-of-cone showering: out-of-cone showering is an important contribution to the PLI correction. To evaluate the systematic variation, the analysis was repeated for jet reconstruction
with distance parameter R = 0.7 and the difference to the nominal R = 0.5 is taken as a
systematic uncertainty.

• PU reweighting: the PU reweighting uncertainty is estimated by varying the minimum bias
pp cross section by ±5% from the nominal 69.4 mb when generating the target PU profile for
MC simulation.
The total uncertainty varies between 3–8% in the measured region at |η| < 2.3, increasing toward
higher rapidity.

9

Systematic uncertainties

The JEC uncertainties for each correction have been detailed in their corresponding sections. They
are also summarized in figure 44. For the purposes of physics analyses, the uncertainties are
provided as systematic sources that include correlations across pT and η. Each source represents a
1σ systematic shift that is fully correlated in pT and η. The decorrelation in η (and pT ) is obtained by
providing a single uncertainty from multiple sources that span only limited regions of phase space
and can also overlap. Their sum in quadrature will always correspond to the original uncertainty,
and the quadratic sum of all the sources equals the total JEC uncertainty. This approach is very
similar to the set of eigenvectors provided, e.g., by the CTEQ collaboration [52].
The correlation factor ρi j between any two points x i = (pT,i, η i ) and x j = (pT, j , η j ) of the
phase space can be calculated using the systematic sources s k :
√∑
√∑
Si =
s2ki, S j =
s2k j ,
k

∑
ρi j =

k

k s ki s k j

Si S j

,

(9.1)

where s ki is the relative uncertainty related to the systematic source k and Si the relative total
systematic uncertainties, for the point x i . Figure 45 shows the level of correlation between various
bins in pT and η.
We recommend that in fits to the theoretical predictions (Ti ) in data (Di ), the JEC systematic
sources s k are propagated as multiplicative factors to the theoretical predictions and their nuisance
parameters ϵ k are added in quadrature to the global χ2 :
∑ [ Di − Ti (1 + ∑ ϵ k s ki ) ] 2 ∑
k
2
χ =
+
ϵ 2k ,
(9.2)
2
σ̂
Di
i
k

– 60 –

2017 JINST 12 P02014

• Jet energy scale: the uncertainty arising from the knowledge of JES is evaluated by scaling
all jet momenta in simulation up and down by the JEC uncertainty.

## PDF page 64

CMS
5
4

R=0.5 PF+CHS
|η | = 0
jet

JEC uncertainty (%)

JEC uncertainty (%)

19.7 fb-1 (8 TeV)

6

Total uncertainty
Excl. flavor, time
Absolute scale
Relative scale
Pileup (〈µ〉=20)
Jet flavor (QCD)
Time stability

3

CMS
5
4

1

1

100 200

T

0

1000

−4

−2

0

2

4

p (GeV)
CMS
5
4

R=0.5 PF+CHS
|η | = 2.7
jet

JEC uncertainty (%)

JEC uncertainty (%)

19.7 fb-1 (8 TeV)

6

Total uncertainty
Excl. flavor, time
Absolute scale
Relative scale
Pileup (〈µ〉=20)
Jet flavor (QCD)
Time stability

3

CMS
5
4

1

1

100 200

R=0.5 PF+CHS
p = 100 GeV
T

0

1000

Total uncertainty
Excl. flavor, time
Absolute scale
Relative scale
Pileup (〈µ〉=20)
Jet flavor (QCD)
Time stability

3
2

20

19.7 fb-1 (8 TeV)

6

2

0

−4

−2

0

2

4

p (GeV)

5
4

R=0.5 PF+CHS
|η | = 3.5
jet

JEC uncertainty (%)

JEC uncertainty (%)

19.7 fb-1 (8 TeV)

CMS

Total uncertainty
Excl. flavor, time
Absolute scale
Relative scale
Pileup (〈µ〉=20)
Jet flavor (QCD)
Time stability

3

CMS
5
4

1

1

100 200

0

1000

p (GeV)

R=0.5 PF+CHS
p = 1000 GeV
T

Total uncertainty
Excl. flavor, time
Absolute scale
Relative scale
Pileup (〈µ〉=20)
Jet flavor (QCD)
Time stability

3
2

20

19.7 fb-1 (8 TeV)

6

2

0

η

jet

T

6

η

jet

T

−4

−2

0

2

4

η

jet

T

Figure 44. Summary of JES systematic uncertainties as a function of jet pT (for 3 different |η jet | values,
left) and of η jet (for 3 different pT values, right). The markers show the single effect of different sources, the
gray dark band the cumulative total uncertainty. The total uncertainty, when excluding the effects of time
dependence and flavor, is also shown in yellow light. The plots are limited to a jet energy E = pT cosh η =
4000 GeV so as to show only the correction factors for reasonable pT in the considered data-taking period.

– 61 –

2017 JINST 12 P02014

2

20

R=0.5 PF+CHS
p = 30 GeV

Total uncertainty
Excl. flavor, time
Absolute scale
Relative scale
Pileup (〈µ〉=20)
Jet flavor (QCD)
Time stability

3

2

0

19.7 fb-1 (8 TeV)

6

## PDF page 65

100 × p (GeV)

1000

Anti-kT R=0.5, PF+CHS
Total excl. time+flavor

0.8

jη

0.4

400
300
200

0.2

100

30

100 200

19.7 fb-1 (8 TeV)

HF

10

Anti-kT R=0.5, PF+CHS

0.8

108

0.6

107

EC2

0.4

106

0

105

−0.2

104

−0.4

3

10

−0.6

102

1000

0.2
EC1

0
−0.2
−0.4

BB

−0.6
102 103 104 105 106 107 108 109
jη

100 × p (GeV)

p (GeV)
T

T

Figure 45. Correlation of total JES systematic uncertainties excluding time-dependent and flavor uncertainties (TotalNoTimeNoFlavor) for PF+CHS versus pT at |η| < 1.3 (left). The color represents the degree
of correlation (between −1 and 1). Correlation of JES systematic uncertainties (TotalNoTimeNoFlavor) for
PF+CHS versus pT (multiplied by 100jη ) and jη bin (right). The integer jη is introduced for illustration
purposes, with jη = 0 for the barrel region (BB), jη = 1 for the endcap inside tracker coverage (EC1), jη = 2
for the endcap outside tracker coverage (EC2), and jη = 3 for the forward region (HF).

where σ̂ Di is the statistical uncertainty (σ̂ Di denotes an estimated value for σ Di ). The a priori
expectation for the χ2 minimum is that the ϵ k will be Gaussian distributed with mean 0 and RMS
1. Alternatively, the global χ2 can be calculated using the correlations from eq. (9.1):
∑
(Di − Ti )Mi−1
χ2 =
where
(9.3)
j (D j − T j ),
i, j

Mi j =

∑

s ki s k j + σ̂ Di σ̂ D j δi j ,

(9.4)

k

and δi j is the Kronecker delta function. The resulting χ2 should be identical, but the former method
also provides the nuisance parameters and the best fit theoretical predictions for sanity checks.
The implementation of correlations across η uses a rough subdivision based on detector
structure to limit the final number of sources. The main regions are the barrel (BB: |η| < 1.3),
endcap with tracking coverage (EC1: 1.3 < |η| < 2.5), endcap outside tracking coverage (EC2:
2.5 < |η| < 3.0), and hadron forward (HF: 3.0 < |η| < 5.2). This division is applied to
the systematic uncertainties sensitive to the detector response (RelativePt, PileUpPt), resolution
(RelativeJER) modeling, and coming from statistical uncertainties (RelativeStat). Other systematic
uncertainties are treated as fully correlated across the η bins.
The systematic sources are listed in table 1 together with their applicable η ranges. They are
also briefly described in the following, summarizing the discussion in the respective sections. The
uncertainty sources are also provided in special combinations, specific to different analysis use
cases, described in table 2.

– 62 –

2017 JINST 12 P02014

30

CMS
9

T

0.6

T

p (GeV)

19.7 fb-1 (8 TeV)

CMS

## PDF page 66

Table 1. List of JES uncertainty sources, grouped by categories, with numbering, a short description, and
range of validity in |η|.
Source
Pileup
PileUpDataMC

01
02
03
04
05
06

Description
Data vs. MC simulation offset
with random cone (RC) method
True offset vs. RC ⊗ absolute pT
True offset vs. RC ⊗ relative η
True offset vs. RC ⊗ relative η
True offset vs. RC ⊗ relative η
True offset vs. RC ⊗ relative η

Range
|η| < 5.2
|η| < 5.2
|η| < 1.3
1.3 < |η| < 2.5
2.5 < |η| < 3.0
3.0 < |η| < 5.2

(alternative source)
PileUpMuZero

02-06b

True offset vs. RC ⊗ residual JES
for ⟨µ⟩ = 0

|η| < 5.2

(benchmark source)
PileUpEnvelope

02-06c

True offset vs. RC × 30%

|η| < 5.2

07
08
09
10
11
12
13
14
15
16
17
18

Jet pT resolution
Jet pT resolution
Jet pT resolution
ISR+FSR correction
ISR+FSR statistical uncertainty
Statistical uncertainty
Statistical uncertainty
Log-lin. vs. flat fit × 50%
Log-lin. vs. flat fit × 50%
Log-lin. vs. flat fit × 50%
Log-lin. vs. flat fit × 50%
Relative η time dependence

1.3 < |η| < 2.5
2.5 < |η| < 3.0
3.0 < |η| < 5.2
|η| < 5.2
|η| < 5.2
2.5 < |η| < 3.0
3.0 < |η| < 5.2
|η| < 1.3
1.3 < |η| < 2.5
2.5 < |η| < 3.0
3.0 < |η| < 5.2
|η| < 5.2

AbsoluteScale

19

|η| < 5.2

AbsoluteMPFBias

20

AbsoluteStat
SinglePionECAL
SinglePionHCAL
Fragmentation

21
22
23
24

TimePt

25

Lepton scale, ±0.11%
MPF bias, ±0.28%
(from ν’s ⊕ ISR acceptance, 0.2% ⊕ 0.2%)
Statistical uncertainty vs. pT
Single-pion response in ECAL, ±4.2%
Single-pion response in HCAL, ±1.5%
Jet fragmentation in pythia 6.4 vs. herwig++ 2.3
Absolute pT time dependence
(indirectly with charged-pion EHCAL /p)

QCD dijet mixture (default)
Z+jet mixture
γ+jet mixture

|η| < 5.2
|η| < 5.2
|η| < 5.2

Relative JES (vs. η)
RelativeJEREC1
RelativeJEREC2
RelativeJERHF
RelativeFSR
RelativeStatFSR
RelativeStatEC2
RelativeStatHF
RelativePtBB
RelativePtEC1
RelativePtEC2
RelativePtHF
TimeEta
Absolute JES (vs. pT )
|η| < 5.2
|η| < 5.2
|η| < 5.2
|η| < 5.2
|η| < 5.2
|η| < 5.2

Jet flavor
(only one of these)
FlavorQCD
FlavorZJet
FlavorPhoton

26a
26b
26c

(or mixture of these)
FlavorGluon

26d1

FlavorQuark
FlavorCharm

26d2
26d3

FlavorBottom

26d4

Pure gluon (g)
(incl. g → qq and unmatched)
Pure light quark (uds)
Pure charm (c)
Pure bottom (b)
(Pure flavors refer to the Physics definition)

– 63 –

|η| < 5.2
|η| < 5.2
|η| < 5.2
|η| < 5.2

2017 JINST 12 P02014

PileUpPtRef
PileUpPtBB
PileUpPtEC1
PileUpPtEC2
PileUpPtHF

#

## PDF page 67

Table 2. List of JES uncertainty source combinations with a short description and list of uncertainty
components. The numbering of the sources (3rd column) corresponds to that used in table 1 (2nd column).
Enumerator

Description

List of sources

Total

Default uncertainty applicable for most CMS analyses

01–25, 26a

TotalNoFlavor
TotalNoTime

as basis for other mixtures
Uncertainty for unprescaled analyses
with full 8 TeV data set
Same as above without FlavorQCD,
as basis for other mixtures

01–25
01–17, 19–24, 26a
01–17, 19–24

SubTotalPileUp

Combination of pileup offset uncertainties

01–06

SubTotalRelative

Combination of relative η correction uncertainties

07–17

SubTotalAbsolute

Combination of absolute scale uncertainties

19–24

SubTotalScale

Scale uncertainties independent of pT ,

SubTotalPt

Combination of absolute scale pT dependence

SubTotalMC

Default uncertainty without PileUpPt sources

plus statistical uncertainty
uncertainties

19–21
22–24
01,07–25,26a

The JES uncertainties are classified in four broad categories: pileup offset, relative calibration
of JES versus η, absolute energy scale versus pT , and jet-flavor response. In addition, the residual
JES time-dependence is considered as an extra source of systematic uncertainty for samples other
than the full unprescaled 8 TeV data set.
The pileup offset (section 4) is mostly important at low pT . The pileup correction is taken
from the true offset in simulation, and then scaled by the ratio of random cone offsets for data and
simulation. The main systematic uncertainty is evaluated as 30% of the pT -dependent difference
between the true offset and the random cone offset in simulation. This difference is propagated
through the fit procedure using Z/γ+jet (absolute pT ) and dijet (relative η) balancing to estimate
the remaining residual pileup uncertainty after residual JES (section 6.4). A special alternative
systematic (PileUpMuZero) is added to estimate the bias introduced by the data-based calibration
for no-pileup (⟨µ⟩ = 0) conditions. A residual uncertainty on the scale factor (PileUpDataMC) is
estimated by varying ρ within one standard deviation.
The relative η-dependent correction (section 6.1) calibrates forward regions relative to |η| <
1.3 using dijet events. The main systematic uncertainties come from JER (RelativeJER) and the
ISR+FSR (RelativeFSR) bias corrections. The JER uncertainty is evaluated by varying the JER
for each detector region independently within the JER uncertainties estimated in section 8, when
applying smearing to the simulation. The differences obtained from comparisons based on pythia
6.4 and herwig++ 2.3 simulations are used to assign an ISR+FSR uncertainty. The η-dependent
correction is parameterized with a log-linear function versus pT at |η| < 3.0, and as a constant in
HF (3 ≤ |η| < 5.2). Half the difference between a log-linear fit and a constant fit is taken as a
pT -dependent parameterization uncertainty (RelativePt). For |η| > 2.5, the statistical uncertainty
(RelativeStat) is also a significant contribution.

– 64 –

2017 JINST 12 P02014

TotalNoFlavorNoTime

Default uncertainty without FlavorQCD,

## PDF page 68

9.1

Uncertainties in 7 TeV analyses

For comparisons to published 7 TeV analyses, using the 2011 data set corresponding to an integrated
luminosity of 5 fb−1 , we briefly summarize the main differences in the JEC and JES uncertainty
sources relative to the ones reported in the previous publication [13]:
• Pileup offset: the 7 TeV uncertainties did not consider the absorption of the pileup offset jet pT
dependence into the residual η and pT -dependent corrections, and the five PileUpPt sources
(#02–#06 in table 1) were reported as a single large PileUpPt uncertainty without η decorrelation. The pileup offset correction was derived from the study of the offset, obtained with
the RC method, as a function of the number of primary vertices NPV for data only. This lead
to a larger PileUpDataMC (#01) uncertainty, necessitating additional PileUpOOT, PileUpJetRate and PileUpBias uncertainties. The PileUpOOT covered the variation due to out-of-time
pileup, now accounted for by deriving the offset versus µ before mapping to NPV . The PileUpJetRate accounted for the offset pT dependence, now corrected using pT -dependent true
offset from simulation. The 7 TeV offset correction was calibrated for jets in the pT range
of 20–30 GeV using simulation, with PileUpBias accounting for the uncertainty in the bias
correction for data. In the current scheme, PileUpBias is absorbed into the PileUpPt sources.
• Relative scale: the 7 TeV JEC used a constant correction for each η bin, and the uncertainties
did not provide the four RelativePt sources (#14–#17) to account for the small residual pT dependence versus η. This led to some overestimates in the uncertainty correlation versus η. The

– 65 –

2017 JINST 12 P02014

The absolute scale (section 6.5) uncertainties for constant scale (AbsoluteScale) and
pT -dependent scale (AbsoluteStat) are extracted from a global fit to Z/γ+jet and multijet data. The
former is essentially related to the lepton momentum scale for muons in Z(→ µµ)+jet, while the latter to the single-pion response in HCAL. Additional constant scale uncertainty is added for the biases
of the MPF and pT -balance methods (AbsoluteMPFbias) coming from neutrinos and ISR outside of
detector acceptance. Shape uncertainties for the pT dependence are considered from the following
sources relative to the global fit reference of pT = 208 GeV at |η| < 1.3: single-pion responses
in ECAL and HCAL (SinglePionECAL, SinglePionHCAL) and jet response differences due to the
different fragmentation models implemented in pythia 6.4 and herwig++ 2.3 (Fragmentation).
The flavor response differences (section 7.3) are estimated using simulation, and crosschecked with Z+b-jet, and quark- and gluon-tagged photon+jet and Z+jet events. The flavor
uncertainties are assigned based on pythia 6.4 and herwig++ 2.3 differences, which are propagated
through the data-based calibration chain with dijet, photon+jet, and Z+jet events. As a result, the
flavor uncertainties are minimized for these flavor mixtures. The flavor differences in pythia 6.4
and herwig++ 2.3 are largest for gluon jets, while the two MC simulations agree well on both lightand heavy-quark jets.
As explained in section 6.2, the JES in the endcaps shows some residual time dependence,
even after correcting for radiation damage to the ECAL and HCAL. Prescaled triggers sample
different run periods with different weights, leading to slight scale differences between different
data sets. This time-dependence uncertainty is estimated as the RMS variation of the η-dependent
corrections determined with dijet events for different run periods.

## PDF page 69

recommended way to address a posteriori the underestimated decorrelation in the 7 TeV uncertainties is to clone the 7 TeV SinglePion source (roughly corresponding to current uncertainties
#22–#23) into five separate sources, spanning η ranges |η| < 0.5, 0.5 < |η| < 1.0, 1.0 < |η| <
√
1.5, |η| < 1.5 and |η| > 1.5, with weight 1 for the last source and 1/ 2 for the four others. This
ensures 50% decorrelation for the SinglePion source within the barrel bins, and 100% decorrelation between the barrel and endcap, while preserving the total uncertainty. The RelativeFSR
(#10) and RelativeStatFSR (#11) sources were reported as a single RelativeFSR uncertainty.

• Time dependence: there was neither evidence of residual JEC pT dependence at 7 TeV, nor
of time dependence in the absolute correction. Therefore, the TimePt source (#25) was not
provided.
In total, the 7 TeV uncertainties included sixteen uncertainty sources, ten fewer than the current
recommendations (#1–#26): one less for pileup (four new sources and three obsolete), five less
for relative scale, three less for absolute scale and one less for time dependence. The current
uncertainties provide a more detailed description of correlations versus both η and pT .

10

The PF jet composition

The different detector contributions to the JES can be understood in more detail by looking at the fractions of jet energy reconstructed as the various types of PF candidates. Although this information is
not yet used to directly constrain JES, it gives valuable information in monitoring the stability of JES.
The PF jet composition is determined from the dijet sample, selected as described in section 3.2,
using the tag-and-probe method. In this method the tag jet, which is in the barrel and matched to
the trigger in data, provides measurement of the jet pT , while the back-to-back probe jet is used
for an unbiased determination for PF candidate energy fractions. This indirect method avoids the
selection bias that would enhance energy fractions correlated with upward fluctuations in jet pT .
This is particularly important because data and simulation are known to have different resolutions,
and we want to avoid introducing JER biases in the composition measurement.
The measured PF energy fractions are shown in figure 46 as a function of pT and η. The agreement between data and simulation is at the level of 1–2% in the barrel, consistent with the measured
residual JEC. In particular, the fraction of charged hadrons associated with pileup agrees well between data and simulation. The differences increase at high pT , where the tracking efficiency within
the densely populated jet core drops significantly, and PF becomes more sensitive to the calorimeter
scale. The differences also increase at higher rapidities, where the observed residual JEC are larger.

– 66 –

2017 JINST 12 P02014

• Absolute scale: the 7 TeV absolute correction was a single constant factor and did not include
any pT dependence except for the uncertainties. The three flat absolute scale factor uncertainties (#19–#21) were reported as a single source (Absolute), as were the pT -dependent uncertainties from single-pion response in the ECAL (#22) and HCAL (#23). The 7 TeV SinglePion
uncertainty, which corresponds to the latter two uncertainties, was a factor two larger and is
uncorrelated with the 8 TeV SinglePionHCAL (#23) source, which is now based on the value
obtained from the global pT -dependent fit. The AbsoluteScale (#19) and AbsoluteStat (#21)
are also based on the global fit, and therefore uncorrelated with the 7 TeV source Absolute.

## PDF page 70

0.8
0.7
0.6
0.5

Markers: Data
Histogram: MC

0.3
0.2
0.1
40

100

200

1000

2000

−2
200

0.6
0.5

0.1

0

100

0.7

0.2

T

40

0.8

0.3

p (GeV)

2

0.9

0.4

|η| < 1.3
Anti-kT R=0.5

1000 2000

p (GeV)
T

19.7 fb-1 (8 TeV)

CMS

56 < p < 74 GeV
T
Anti-kT R=0.5
Markers: Data
Histogram: MC
Charged pileup
Charged hadrons
Photons
Neutral hadrons
Leptons
Forward hadrons
Forward photons

4−5 −4 −3 −2 −1 0

1

2

3

4

1

2

3

4

2

5

η

0
−2
−4
−5 −4 −3 −2 −1 0

5

η

Figure 46. PF jet composition in data and simulation versus pT at |η| < 1.3 (left), and versus η at
56 < pT < 74 GeV (right).

Interpretation of the results
To interpret the implications for JEC of composition differences in data and simulation, we can
start from the definition of the jet response, in the absence of pileup, and in bins of particle-level
jet pT, ptcl and reconstructed η (pT is the reconstructed jet transverse momentum):
⟨
⟩
⟨pT ⟩
pT
R(⟨pT ⟩, η) ≡
[pT, ptcl, η] 
[pT, ptcl, η].
(10.1)
⟨pT, ptcl ⟩
pT, ptcl
The last equivalence holds if the pT, ptcl bins are narrow enough. Leaving aside corrections for
overlapping particles caused, e.g., by calorimeter zero-suppression or neutral hadron shadowing in
the PF algorithm, we can write
∑
i
∑
⟨ i R f (⟨pTi ⟩, η i )pT,
ptcl ⟩
i
R(⟨pT ⟩, η) =
, pT, ptcl =
pT,
(10.2)
ptcl,
pT, ptcl
i
where the sum runs over all stable (cτ >1 cm) particles i of different particle species f , excluding
neutrinos. Figure 47 illustrates the average particle jet composition in QCD dijet sample versus pT
at |η| < 1.3, which is about 60% charged hadrons (red hues), 15% neutral hadrons (green hues) and
25% photons (blue hues). About 65% of the jet energy is carried by pions (π + , π − , π 0 → γγ). The
nucleons (p, p, n, n) and kaons (K+ , K− , KL0 , KS0 ) carry about 15% each, with the remaining 5% in
fragmentation photons (γ), lambda (Λ0 ), and sigma (Σ0 ) baryons, leptons (e, µ) and other particles.
The composition does not significantly depend on η.

– 67 –

2017 JINST 12 P02014

Charged pileup
Charged hadrons
Photons
Neutral hadrons
Leptons

0.4

Data-MC (%)

PF energy fraction

0.9

Data-MC (%)

PF energy fraction

19.7 fb-1 (8 TeV)

CMS

## PDF page 71

Jet energy fraction

CMS Simulation

(8 TeV)

1
0.9
0.8
0.7
0.6
0.5

0.3
0.2
0.1
100 200

T

Figure 47. Jet composition at particle level in the pythia 6.4 tune Z2* for QCD dijet sample, shown versus pT
at |η| < 1.3. The component labeled ‘γ (rest)’ denotes all photons not coming from π 0 s, and the component
labeled ‘rest’ refers to all particles not listed specifically.

The PF algorithm [10, 11] uses tracking to measure charged particles pT down to pT ≈ 0.3 GeV,
which effectively results in response Rch (pT ) ≈ 1 for all charged particles (charged hadrons, electron,
muons) within the tracking coverage at |η| < 2.4, when neglecting tracking inefficiencies and the
low pT acceptance. The finely segmented ECAL has a linear response to photons down to its
acceptance of about 0.1 GeV, which also results in response Rγ ≈ 1.
Neutral hadrons (predominantly n, KL0 , Λ0 ), hadrons outside the tracking coverage, and hadrons
with failed tracking (e.g., KS0 decaying in the outer layers of tracking, or unreconstructed nuclear
interactions within the tracker) are reconstructed with a nonlinear calorimeter response Rcalo (pT ) ≈
1 − apTm−1 [53] separately in the ECAL (as PF photons) and the HCAL (as PF neutral hadrons). For
particles with |η| > 2.5, overlapping ECAL and HCAL energy deposits are linked to build neutral
hadrons. The combination of the HCAL reconstruction threshold of pT > 0.8 GeV, the low response
of Rcalo ≈ 0.3 for soft hadrons, and many neutral hadrons showering early in ECAL, result in an
effective neutral hadron response Rnh ≪ 1 at low pT despite the PF neutral hadron calibration for
HCAL deposits. However, the neutral hadron response approaches unity asymptotically at high pT .
Rearranging eq. (10.2) in terms of the main particle categories seen by the detector gives
Rjet = f ch Rch + f γ Rγ + f nh Rnh,

(10.3)

where f i are the average fractions of energy carried by each particle category at particle level, such
∑
that i f i = 1. The effective categories are charged hadrons+electrons+muons (ch), photons (γ),
and neutral hadrons (nh). These effective categories have some ambiguity in the classification of,
e.g., KS0 → π + + π − and KS0 → π 0 + π 0 decays within the tracker volume. Typical generated fractions
are f ch ≈ 60%, f γ ≈ 25%, and f nh ≈ 15%. These values differ slightly from typical measured

– 68 –

2017 JINST 12 P02014

0.4

0
20 30

rest
e,µ
γ (rest)
γ (π0)
Λ
KL
KS
n
n
p
p
Σ±
K
+
K
π
π+
1000 2000
p (GeV)

Pythia 6 Z2*

## PDF page 72

11

Conclusions

The understanding of jet energy scale and resolution achieved by the CMS experiment exploiting
the pp data taken at 8 TeV, corresponding to an integrated luminosity of 19.7 fb−1 , has been
documented. The CMS strategy involves the sequential correction of the jets for the pileup offset,
simulated response, and residual η and pT dependencies in data with respect to simulation, with
optional corrections depending on the jet flavor.
The pileup offset corrections are determined from QCD dijet simulations processed with and
without pileup overlay, with additional corrections for residual differences between data and detector
simulation, extracted using the random-cone method in zero-bias events. The simulated jet response
corrections are determined from a Monte Carlo event sample, as a function of jet pT and η, for
various jet algorithms and distance parameter sizes. The η-dependent corrections for residual
differences between data and MC simulation are determined with dijet events, relative to a jet in the
central region |η| < 1.3. The pT -dependent corrections for residual differences within |η| < 1.3 at
30 < pT < 800 GeV are measured combining photon+jet, Z(→ µµ)+jet, and Z(→ ee)+jet events.
The pT dependence at pT > 800 GeV is directly constrained with multijet events. The optional
jet-flavor corrections are derived from MC simulation and checked for b jets.
The simulated jet pT resolution is determined, as a function of jet pT and η, for different levels
of pileup. The dependence of the resolution on the jet flavor is also studied. The η-dependent
corrections for residual differences between data and MC simulation in the jet resolution are
determined with both dijet and γ+jet events.
In all methods using MC simulation, the uncertainties arising from the modeling of jet radiation and hadronization are constrained from the study of the differences between pythia 6.4 and
herwig++ 2.3 generators. Detailed studies are performed to correct for biases in the data-based
methods due to differences with respect to the MC simulation, in initial- and final-state radiation

– 69 –

2017 JINST 12 P02014

fractions f ch, meas ≈ 65%, f γ,meas ≈ 30%, and f nh,meas ≈ 5% due to different detector responses
(Rch ≈ Rγ ≈ 1, Rnh ≈ 0.6, thus Rjet ≈ 0.95) and ambiguities in particle identification, specially
between neutral hadrons and photons.
The impact of typical detector mismodeling effects can be estimated with the help of eq. (10.3).
A change of −1% in the charged hadron fraction through tracking inefficiencies would result in a
corresponding but smaller increase of the neutral hadron fraction, for a total relative jet response variation of −0.4%. A variation of −1% of the ECAL scale in data would change the relative jet response
by −0.3%, while a variation of the single-pion response of −3% would also change it by −0.3%.
Adding these a priori uncertainty estimates in quadrature gives 0.6%, while summing them up
gives −1.0%. Incidentally, these are about the order of magnitude of the minimum energy scale uncertainty and the data/MC correction applied at the moment in the reference region |η| < 1.3. The PF
energy fractions between data and simulation in figure 46 are in almost perfect agreement to the level
of about 10−3 at pT ≈ 200 GeV, which is consistent with the jet response difference of −1%, assuming the inefficiencies for charged hadrons, photons, and neutral hadrons all go in the same direction.
The corrections and uncertainties increase outside the tracking coverage at |η| > 2.5, where
effectively f ch = 0 and f nh = 75%, resulting in about five times higher sensitivity to single-pion
response and threshold effects in Rnh .

## PDF page 73

as well as in jet pT resolution. The systematic uncertainties in the jet energy corrections, and their
correlations, are provided as a function of η and pT .
The final uncertainties on the jet energy scale are below 3% across the phase space considered
by most analyses (pT > 30 GeV and |η| < 5.0). In the barrel region we reach an uncertainty below
1% for pT > 30 GeV, when excluding the jet-flavor uncertainties, provided separately for different
jet-flavor mixtures. At its lowest, the core uncertainty (excluding optional time-dependent and
flavor systematics) is 0.32% for jets with pT between 165 and 330 GeV, and |η| < 0.8. These results
set a new benchmark for jet energy scale determination at hadron colliders.

We congratulate our colleagues in the CERN accelerator departments for the excellent performance
of the LHC and thank the technical and administrative staffs at CERN and at other CMS institutes
for their contributions to the success of the CMS effort. In addition, we gratefully acknowledge
the computing centers and personnel of the Worldwide LHC Computing Grid for delivering so
effectively the computing infrastructure essential to our analyses. Finally, we acknowledge the
enduring support for the construction and operation of the LHC and the CMS detector provided
by the following funding agencies: the Austrian Federal Ministry of Science, Research and Economy and the Austrian Science Fund; the Belgian Fonds de la Recherche Scientifique, and Fonds
voor Wetenschappelijk Onderzoek; the Brazilian Funding Agencies (CNPq, CAPES, FAPERJ, and
FAPESP); the Bulgarian Ministry of Education and Science; CERN; the Chinese Academy of
Sciences, Ministry of Science and Technology, and National Natural Science Foundation of China;
the Colombian Funding Agency (COLCIENCIAS); the Croatian Ministry of Science, Education
and Sport, and the Croatian Science Foundation; the Research Promotion Foundation, Cyprus; the
Secretariat for Higher Education, Science, Technology and Innovation, Ecuador; the Ministry of Education and Research, Estonian Research Council via IUT23-4 and IUT23-6 and European Regional
Development Fund, Estonia; the Academy of Finland, Finnish Ministry of Education and Culture,
and Helsinki Institute of Physics; the Institut National de Physique Nucléaire et de Physique des
Particules / CNRS, and Commissariat à l’Énergie Atomique et aux Énergies Alternatives / CEA,
France; the Bundesministerium für Bildung und Forschung, Deutsche Forschungsgemeinschaft,
and Helmholtz-Gemeinschaft Deutscher Forschungszentren, Germany; the General Secretariat for
Research and Technology, Greece; the National Scientific Research Foundation, and National Innovation Office, Hungary; the Department of Atomic Energy and the Department of Science and
Technology, India; the Institute for Studies in Theoretical Physics and Mathematics, Iran; the Science
Foundation, Ireland; the Istituto Nazionale di Fisica Nucleare, Italy; the Ministry of Science, ICT
and Future Planning, and National Research Foundation (NRF), Republic of Korea; the Lithuanian
Academy of Sciences; the Ministry of Education, and University of Malaya (Malaysia); the Mexican
Funding Agencies (BUAP, CINVESTAV, CONACYT, LNS, SEP, and UASLP-FAI); the Ministry of
Business, Innovation and Employment, New Zealand; the Pakistan Atomic Energy Commission; the
Ministry of Science and Higher Education and the National Science Centre, Poland; the Fundação
para a Ciência e a Tecnologia, Portugal; JINR, Dubna; the Ministry of Education and Science of
the Russian Federation, the Federal Agency of Atomic Energy of the Russian Federation, Russian
Academy of Sciences, and the Russian Foundation for Basic Research; the Ministry of Education,

– 70 –

2017 JINST 12 P02014

Acknowledgments

## PDF page 74

Science and Technological Development of Serbia; the Secretaría de Estado de Investigación, Desarrollo e Innovación and Programa Consolider-Ingenio 2010, Spain; the Swiss Funding Agencies
(ETH Board, ETH Zurich, PSI, SNF, UniZH, Canton Zurich, and SER); the Ministry of Science and
Technology, Taipei; the Thailand Center of Excellence in Physics, the Institute for the Promotion of
Teaching Science and Technology of Thailand, Special Task Force for Activating Research and the
National Science and Technology Development Agency of Thailand; the Scientific and Technical
Research Council of Turkey, and Turkish Atomic Energy Authority; the National Academy of Sciences of Ukraine, and State Fund for Fundamental Researches, Ukraine; the Science and Technology
Facilities Council, U.K.; the U.S. Department of Energy, and the U.S. National Science Foundation.

References
[1] CMS collaboration, Measurements of differential jet cross sections in proton-proton collisions at
√
s = 7 TeV with the CMS detector, Phys. Rev. D 87 (2013) 112002 [Erratum ibid. D 87 (2013)
119902] [arXiv:1212.6660].
√
[2] CMS collaboration, Measurement of the inclusive jet cross section in pp collisions at s = 7 TeV,
Phys. Rev. Lett. 107 (2011) 132001 [arXiv:1106.0208].
[3] CMS collaboration, Measurement of the differential dijet production cross section in proton-proton
√
collisions at s = 7 TeV, Phys. Lett. B 700 (2011) 187 [arXiv:1104.1693].
[4] CMS collaboration, Measurement of the ratio of inclusive jet cross sections using the anti-kT
√
algorithm with radius parameters R = 0.5 and 0.7 in pp collisions at s = 7 TeV, Phys. Rev. D 90
(2014) 072006 [arXiv:1406.0324].
[5] CMS collaboration, Distributions of topological observables in inclusive three- and four-jet events in
√
pp collisions at s = 7 TeV, Eur. Phys. J. C 75 (2015) 302 [arXiv:1502.04785].
[6] CMS collaboration, Measurement of the top-quark mass in all-jets t t¯ events in pp collisions at
√
s = 7 TeV, Eur. Phys. J. C 74 (2014) 2758 [arXiv:1307.4617].

– 71 –

2017 JINST 12 P02014

Individuals have received support from the Marie-Curie program and the European Research
Council and EPLANET (European Union); the Leventis Foundation; the A. P. Sloan Foundation;
the Alexander von Humboldt Foundation; the Belgian Federal Science Policy Office; the Fonds
pour la Formation à la Recherche dans l’Industrie et dans l’Agriculture (FRIA-Belgium); the
Agentschap voor Innovatie door Wetenschap en Technologie (IWT-Belgium); the Ministry of
Education, Youth and Sports (MEYS) of the Czech Republic; the Council of Science and Industrial
Research, India; the HOMING PLUS program of the Foundation for Polish Science, cofinanced
from European Union, Regional Development Fund, the Mobility Plus program of the Ministry
of Science and Higher Education, the OPUS program contract 2014/13/B/ST2/02543 and contract
Sonata-bis DEC-2012/07/E/ST2/01406 of the National Science Center (Poland); the Thalis and
Aristeia programs cofinanced by EU-ESF and the Greek NSRF; the National Priorities Research
Program by Qatar National Research Fund; the Programa Clarín-COFUND del Principado de
Asturias; the Rachadapisek Sompot Fund for Postdoctoral Fellowship, Chulalongkorn University
and the Chulalongkorn Academic into Its 2nd Century Project Advancement Project (Thailand);
and the Welch Foundation, contract C-1845.

## PDF page 75

[7] CMS collaboration, Determination of the top-quark pole mass and strong coupling constant from the
√
t t¯ production cross section in pp collisions at s = 7 TeV, Phys. Lett. B 728 (2014) 496 [Erratum ibid.
B 738 (2014) 526] [arXiv:1307.1907].
[8] CMS collaboration, Measurement of the top-quark mass in t t¯ events with lepton+jets final states in pp
√
collisions at s = 7 TeV, JHEP 12 (2012) 105 [arXiv:1209.2319].
√
[9] CMS collaboration, Measurement of the top quark mass using proton-proton data at s = 7 and
8 TeV, Phys. Rev. D 93 (2016) 072004 [arXiv:1509.04044].
[10] CMS collaboration, Particle-flow event reconstruction in CMS and performance for jets, taus and
MET, CMS-PAS-PFT-09-001, CERN, Geneva Switzerland, (2009).

[12] M. Cacciari, G.P. Salam and G. Soyez, The anti-k t jet clustering algorithm, JHEP 04 (2008) 063
[arXiv:0802.1189].
[13] CMS collaboration, Determination of jet energy calibration and transverse momentum resolution in
CMS, 2011 JINST 6 P11002 [arXiv:1107.4277].
[14] ATLAS collaboration, Jet energy measurement with the ATLAS detector in proton-proton collisions at
√
s = 7 TeV, Eur. Phys. J. C 73 (2013) 2304 [arXiv:1112.6426].
[15] CDF collaboration, A. Bhatti et al., Determination of the jet energy scale at the collider detector at
Fermilab, Nucl. Instrum. Meth. A 566 (2006) 375 [hep-ex/0510047].
[16] D0 collaboration, V.M. Abazov et al., Jet energy scale determination in the D0 experiment, Nucl.
Instrum. Meth. A 763 (2014) 442 [arXiv:1312.6873].
[17] ATLAS collaboration, Jet energy measurement and its systematic uncertainty in proton-proton
√
collisions at s = 7 TeV with the ATLAS detector, Eur. Phys. J. C 75 (2015) 17 [arXiv:1406.0076].
[18] GEANT4 collaboration, S. Agostinelli et al., GEANT4: a simulation toolkit, Nucl. Instrum. Meth. A
506 (2003) 250.
[19] T. Sjöstrand, S. Mrenna and P.Z. Skands, PYTHIA 6.4 physics and manual, JHEP 05 (2006) 026
[hep-ph/0603175].
[20] CMS collaboration, Event generator tunes obtained from underlying event and multiparton scattering
measurements, Eur. Phys. J. C 76 (2016) 155 [arXiv:1512.00815].
[21] M. Bähr et al., HERWIG++ physics and manual, Eur. Phys. J. C 58 (2008) 639 [arXiv:0803.0883].
[22] S. Gieseke, C. Rohr and A. Siodmok, Colour reconnections in HERWIG++, Eur. Phys. J. C 72
(2012) 2225 [arXiv:1206.0041].
[23] A. Giammanco, The fast simulation of the CMS experiment, J. Phys. Conf. Ser. 513 (2014) 022012.
[24] CMS collaboration, The CMS experiment at the CERN LHC, 2008 JINST 3 S08004.
[25] J. Alwall, M. Herquet, F. Maltoni, O. Mattelaer and T. Stelzer, MadGraph 5: going beyond, JHEP 06
(2011) 128 [arXiv:1106.0522].
[26] S. Frixione, P. Nason and C. Oleari, Matching NLO QCD computations with parton shower
simulations: the POWHEG method, JHEP 11 (2007) 070 [arXiv:0709.2092].
[27] CMS collaboration, Description and performance of track and primary-vertex reconstruction with the
CMS tracker, 2014 JINST 9 P10009 [arXiv:1405.6569].

– 72 –

2017 JINST 12 P02014

[11] CMS collaboration, Commissioning of the particle-flow event reconstruction with the first LHC
collisions recorded in the CMS detector, CMS-PAS-PFT-10-001, CERN, Geneva Switzerland, (2010).

## PDF page 76

[28] CMS collaboration, Jet performance in pp collisions at 7 TeV, CMS-PAS-JME-10-003, CERN,
Geneva Switzerland, (2010).
√
[29] CMS collaboration, Performance of CMS muon reconstruction in pp collision events at s = 7 TeV,
2012 JINST 7 P10002 [arXiv:1206.4071].
[30] CMS collaboration, Performance of electron reconstruction and selection with the CMS detector in
√
proton-proton collisions at s = 8 TeV, 2015 JINST 10 P06005 [arXiv:1502.02701].
[31] CMS collaboration, Identification of b-quark jets with the CMS experiment, 2013 JINST 8 P04013
[arXiv:1211.4462].

[33] M. Cacciari, G.P. Salam and G. Soyez, FastJet user manual, Eur. Phys. J. C 72 (2012) 1896
[arXiv:1111.6097].
[34] M. Cacciari and G.P. Salam, Dispelling the N 3 myth for the k t jet-finder, Phys. Lett. B 641 (2006) 57
[hep-ph/0512210].
[35] S. Catani, Y.L. Dokshitzer and B.R. Webber, The k⊥ -clustering algorithm for jets in deep inelastic
scattering and hadron collisions, Phys. Lett. B 285 (1992) 291.
[36] S. Catani, Y.L. Dokshitzer, M.H. Seymour and B.R. Webber, Longitudinally invariant k⊥ clustering
algorithms for hadron hadron collisions, Nucl. Phys. B 406 (1993) 187.
[37] S.D. Ellis and D.E. Soper, Successive combination jet algorithm for hadron collisions, Phys. Rev. D
48 (1993) 3160 [hep-ph/9305266].
[38] M. Cacciari and G.P. Salam, Pileup subtraction using jet areas, Phys. Lett. B 659 (2008) 119
[arXiv:0707.1378].
√
[39] CMS collaboration, Measurement of the inelastic proton-proton cross section at s = 7 TeV, Phys.
Lett. B 722 (2013) 5 [arXiv:1210.6718].
[40] CMS collaboration, CMS luminosity based on pixel cluster counting — Summer 2013 update,
CMS-PAS-LUM-13-001, CERN, Geneva Switzerland, (2013).
[41] CMS collaboration, CMS technical design report, volume II: physics performance, J. Phys. G 34
(2007) 995.
[42] CMS collaboration, Transverse-momentum and pseudorapidity distributions of charged hadrons in pp
√
collisions at s = 7 TeV, Phys. Rev. Lett. 105 (2010) 022002 [arXiv:1005.3299].
[43] D. Bertolini, P. Harris, M. Low and N. Tran, Pileup per particle identification, JHEP 10 (2014) 059
[arXiv:1407.6013].
[44] CMS collaboration, Pileup jet identification, CMS-PAS-JME-13-005, CERN, Geneva Switzerland,
(2013).
√
[45] CMS collaboration, Measurement of the underlying event activity in pp collisions at s = 0.9 and
7 TeV with the novel jet-area/median approach, JHEP 08 (2012) 130 [arXiv:1207.2392].
[46] CMS collaboration, Jet energy scale performance in 2011, CMS-DP-2012-006, CERN, Geneva
Switzerland, (2012).
[47] CMS collaboration, Single-particle response in the CMS calorimeters, CMS-PAS-JME-10-008,
CERN, Geneva Switzerland, (2010).

– 73 –

2017 JINST 12 P02014

[32] CMS collaboration, Performance of photon reconstruction and identification with the CMS detector in
√
proton-proton collisions at s = 8 TeV, 2015 JINST 10 P08010 [arXiv:1502.02702].

## PDF page 77

[48] CMS collaboration, Energy calibration and resolution of the CMS electromagnetic calorimeter in pp
√
collisions at s = 7 TeV, 2013 JINST 8 P09009 [arXiv:1306.2016].
[49] CMS collaboration, Performance of quark/gluon discrimination in 8 TeV pp data,
CMS-PAS-JME-13-002, CERN, Geneva Switzerland, (2013).
[50] CMS collaboration, Calculation of residual energy correction for b jets using Z + b events in 8 TeV pp
collisions, CMS-PAS-JME-13-001, CERN, Geneva Switzerland, (2013).
[51] M.J. Oreglia, A study of the reactions ψ ′ → γγψ, see appendix D, SLAC report SLAC-R-236, Ph.D.
thesis, Stanford University, U.S.A., (1980).

[53] D.E. Groom, A simplistic view of hadron calorimetry, AIP Conf. Proc. 896 (2007) 137.

– 74 –

2017 JINST 12 P02014

[52] H.L. Lai et al., Global QCD analysis and the CTEQ parton distributions, Phys. Rev. D 51 (1995)
4763 [hep-ph/9410404].

## PDF page 78

The CMS collaboration
Yerevan Physics Institute, Yerevan, Armenia
V. Khachatryan, A.M. Sirunyan, A. Tumasyan
Institut für Hochenergiephysik der OeAW, Wien, Austria

National Centre for Particle and High Energy Physics, Minsk, Belarus
V. Mossolov, N. Shumeiko, J. Suarez Gonzalez
Universiteit Antwerpen, Antwerpen, Belgium
S. Alderweireldt, T. Cornelis, E.A. De Wolf, X. Janssen, A. Knutsson, J. Lauwers, S. Luyckx,
M. Van De Klundert, H. Van Haevermaet, P. Van Mechelen, N. Van Remortel, A. Van Spilbeeck
Vrije Universiteit Brussel, Brussel, Belgium
S. Abu Zeid, F. Blekman, J. D’Hondt, N. Daci, I. De Bruyn, K. Deroover, N. Heracleous, J. Keaveney,
S. Lowette, L. Moreels, A. Olbrechts, Q. Python, D. Strom, S. Tavernier, W. Van Doninck, P. Van
Mulders, G.P. Van Onsem, I. Van Parijs
Université Libre de Bruxelles, Bruxelles, Belgium
P. Barria, H. Brun, C. Caillol, B. Clerbaux, G. De Lentdecker, G. Fasanella, L. Favart, A. Grebenyuk,
G. Karapostoli, T. Lenzi, A. Léonard, T. Maerschalk, A. Marinov, L. Perniè, A. Randle-conde,
T. Reis, T. Seva, C. Vander Velde, P. Vanlaer, R. Yonamine, F. Zenoni, F. Zhang3
Ghent University, Ghent, Belgium
K. Beernaert, L. Benucci, A. Cimmino, S. Crucy, D. Dobur, A. Fagot, G. Garcia, M. Gul, J. Mccartin,
A.A. Ocampo Rios, D. Poyraz, D. Ryckbosch, S. Salva, M. Sigamani, N. Strobbe, M. Tytgat, W. Van
Driessche, E. Yazgan, N. Zaganidis
Université Catholique de Louvain, Louvain-la-Neuve, Belgium
S. Basegmez, C. Beluffi4 , O. Bondu, S. Brochet, G. Bruno, A. Caudron, L. Ceard, G.G. Da
Silveira, C. Delaere, D. Favart, L. Forthomme, A. Giammanco5 , J. Hollar, A. Jafari, P. Jez,
M. Komm, V. Lemaitre, A. Mertens, C. Nuttens, L. Perrini, A. Pin, K. Piotrzkowski, A. Popov6 ,
L. Quertenmont, M. Selvaggi, M. Vidal Marono
Université de Mons, Mons, Belgium
N. Beliy, G.H. Hammad
Centro Brasileiro de Pesquisas Fisicas, Rio de Janeiro, Brazil
W.L. Aldá Júnior, F.L. Alves, G.A. Alves, L. Brito, M. Correa Martins Junior, M. Hamer, C. Hensel,
C. Mora Herrera, A. Moraes, M.E. Pol, P. Rebello Teles

– 75 –

2017 JINST 12 P02014

W. Adam, E. Asilar, T. Bergauer, J. Brandstetter, E. Brondolin, M. Dragicevic, J. Erö, M. Flechl,
M. Friedl, R. Frühwirth1 , V.M. Ghete, C. Hartl, N. Hörmann, J. Hrubec, M. Jeitler1 , V. Knünz,
A. König, M. Krammer1 , I. Krätschmer, D. Liko, T. Matsushita, I. Mikulec, D. Rabady2 ,
B. Rahbaran, H. Rohringer, J. Schieck1 , R. Schöfbeck, J. Strauss, W. Treberer-Treberspurg,
W. Waltenberger, C.-E. Wulz1

## PDF page 79

Universidade do Estado do Rio de Janeiro, Rio de Janeiro, Brazil
E. Belchior Batista Das Chagas, W. Carvalho, J. Chinellato7 , A. Custódio, E.M. Da Costa, D. De
Jesus Damiao, C. De Oliveira Martins, S. Fonseca De Souza, L.M. Huertas Guativa, H. Malbouisson,
D. Matos Figueiredo, L. Mundim, H. Nogima, W.L. Prado Da Silva, A. Santoro, A. Sznajder,
E.J. Tonelli Manganote7 , A. Vilela Pereira

Institute for Nuclear Research and Nuclear Energy, Sofia, Bulgaria
A. Aleksandrov, R. Hadjiiska, P. Iaydjiev, M. Rodozov, S. Stoykova, G. Sultanov, M. Vutova
University of Sofia, Sofia, Bulgaria
A. Dimitrov, I. Glushkov, L. Litov, B. Pavlov, P. Petkov
Institute of High Energy Physics, Beijing, China
M. Ahmad, J.G. Bian, G.M. Chen, H.S. Chen, M. Chen, T. Cheng, R. Du, C.H. Jiang, R. Plestina9 ,
F. Romeo, S.M. Shaheen, J. Tao, C. Wang, Z. Wang, H. Zhang
State Key Laboratory of Nuclear Physics and Technology, Peking University, Beijing, China
C. Asawatangtrakuldee, Y. Ban, Q. Li, S. Liu, Y. Mao, S.J. Qian, D. Wang, Z. Xu
Universidad de Los Andes, Bogota, Colombia
C. Avila, A. Cabrera, L.F. Chaparro Sierra, C. Florez, J.P. Gomez, B. Gomez Moreno, J.C. Sanabria
University of Split, Faculty of Electrical Engineering, Mechanical Engineering and Naval
Architecture, Split, Croatia
N. Godinovic, D. Lelas, I. Puljak, P.M. Ribeiro Cipriano
University of Split, Faculty of Science, Split, Croatia
Z. Antunovic, M. Kovac
Institute Rudjer Boskovic, Zagreb, Croatia
V. Brigljevic, K. Kadija, J. Luetic, S. Micanovic, L. Sudic
University of Cyprus, Nicosia, Cyprus
A. Attikis, G. Mavromanolakis, J. Mousa, C. Nicolaou, F. Ptochos, P.A. Razis, H. Rykaczewski
Charles University, Prague, Czech Republic
M. Bodlak, M. Finger10 , M. Finger Jr.10
Academy of Scientific Research and Technology of the Arab Republic of Egypt, Egyptian
Network of High Energy Physics, Cairo, Egypt
Y. Assran11 , S. Elgammal12 , A. Ellithi Kamel13 , M.A. Mahmoud14 , Y. Mohammed14
National Institute of Chemical Physics and Biophysics, Tallinn, Estonia
B. Calpas, M. Kadastik, M. Murumaa, M. Raidal, A. Tiko, C. Veelken

– 76 –

2017 JINST 12 P02014

Universidade Estadual Paulista a , Universidade Federal do ABC b , São Paulo, Brazil
S. Ahujaa , C.A. Bernardesb , A. De Souza Santosb , S. Dograa , T.R. Fernandez Perez Tomeia ,
E.M. Gregoresb , P.G. Mercadanteb , C.S. Moona, 8 , S.F. Novaesa , Sandra S. Padulaa , D. Romero
Abad, J.C. Ruiz Vargas

## PDF page 80

Department of Physics, University of Helsinki, Helsinki, Finland
P. Eerola, J. Pekkanen, M. Voutilainen
Helsinki Institute of Physics, Helsinki, Finland
J. Härkönen, V. Karimäki, R. Kinnunen, T. Lampén, K. Lassila-Perini, S. Lehti, T. Lindén,
P. Luukka, T. Mäenpää, T. Peltola, E. Tuominen, J. Tuominiemi, E. Tuovinen, L. Wendland
Lappeenranta University of Technology, Lappeenranta, Finland
J. Talvitie, T. Tuuva

Laboratoire Leprince-Ringuet, Ecole Polytechnique, IN2P3-CNRS, Palaiseau, France
I. Antropov, S. Baffioni, F. Beaudette, P. Busson, L. Cadamuro, E. Chapon, C. Charlot, T. Dahms,
O. Davignon, N. Filipovic, A. Florent, R. Granier de Cassagnac, S. Lisniak, L. Mastrolorenzo,
P. Miné, I.N. Naranjo, M. Nguyen, C. Ochando, G. Ortona, P. Paganini, P. Pigard, S. Regnard,
R. Salerno, J.B. Sauvan, Y. Sirois, T. Strebler, Y. Yilmaz, A. Zabi
Institut Pluridisciplinaire Hubert Curien, Université de Strasbourg, Université de Haute
Alsace Mulhouse, CNRS/IN2P3, Strasbourg, France
J.-L. Agram15 , J. Andrea, A. Aubin, D. Bloch, J.-M. Brom, M. Buttignol, E.C. Chabert, N. Chanon,
C. Collard, E. Conte15 , X. Coubez, J.-C. Fontaine15 , D. Gelé, U. Goerlach, C. Goetzmann, A.-C. Le
Bihan, J.A. Merlin2 , K. Skovpen, P. Van Hove
Centre de Calcul de l’Institut National de Physique Nucleaire et de Physique des Particules,
CNRS/IN2P3, Villeurbanne, France
S. Gadrat
Université de Lyon, Université Claude Bernard Lyon 1, CNRS-IN2P3, Institut de Physique
Nucléaire de Lyon, Villeurbanne, France
S. Beauceron, C. Bernet, G. Boudoul, E. Bouvier, C.A. Carrillo Montoya, R. Chierici, D. Contardo,
B. Courbon, P. Depasse, H. El Mamouni, J. Fan, J. Fay, S. Gascon, M. Gouzevitch, B. Ille, F. Lagarde,
I.B. Laktineh, M. Lethuillier, L. Mirabito, A.L. Pequegnot, S. Perries, J.D. Ruiz Alvarez, D. Sabes,
L. Sgandurra, V. Sordini, M. Vander Donckt, P. Verdier, S. Viret
Georgian Technical University, Tbilisi, Georgia
T. Toriashvili16
Tbilisi State University, Tbilisi, Georgia
Z. Tsamalaidze10
RWTH Aachen University, I. Physikalisches Institut, Aachen, Germany
C. Autermann, S. Beranek, M. Edelhoff, L. Feld, A. Heister, M.K. Kiesel, K. Klein, M. Lipinski,
A. Ostapchuk, M. Preuten, F. Raupach, S. Schael, J.F. Schulte, T. Verlage, H. Weber, B. Wittmer,
V. Zhukov6

– 77 –

2017 JINST 12 P02014

IRFU, CEA, Université Paris-Saclay, Gif-sur-Yvette, France
M. Besancon, F. Couderc, M. Dejardin, D. Denegri, B. Fabbro, J.L. Faure, C. Favaro, F. Ferri,
S. Ganjour, A. Givernaud, P. Gras, G. Hamel de Monchenault, P. Jarry, E. Locci, M. Machet,
J. Malcles, J. Rander, A. Rosowsky, M. Titov, A. Zghiche

## PDF page 81

RWTH Aachen University, III. Physikalisches Institut A, Aachen, Germany
M. Ata, M. Brodski, E. Dietz-Laursonn, D. Duchardt, M. Endres, M. Erdmann, S. Erdweg, T. Esch,
R. Fischer, A. Güth, T. Hebbeker, C. Heidemann, K. Hoepfner, D. Klingebiel, S. Knutzen, P. Kreuzer,
M. Merschmeyer, A. Meyer, P. Millet, M. Olschewski, K. Padeken, P. Papacz, T. Pook, M. Radziej,
H. Reithler, M. Rieger, F. Scheuch, L. Sonnenschein, D. Teyssier, S. Thüer
RWTH Aachen University, III. Physikalisches Institut B, Aachen, Germany

Deutsches Elektronen-Synchrotron, Hamburg, Germany
M. Aldaya Martin, I. Asin, N. Bartosik, O. Behnke, U. Behrens, A.J. Bell, K. Borras17 , A. Burgmeier,
A. Cakir, L. Calligaris, A. Campbell, S. Choudhury, F. Costanza, C. Diez Pardos, G. Dolinska,
S. Dooling, T. Dorland, G. Eckerlin, D. Eckstein, T. Eichhorn, G. Flucke, E. Gallo18 , J. Garay
Garcia, A. Geiser, A. Gizhko, P. Gunnellini, J. Hauk, M. Hempel19 , H. Jung, A. Kalogeropoulos,
O. Karacheban19 , M. Kasemann, P. Katsas, J. Kieseler, C. Kleinwort, I. Korol, W. Lange, J. Leonard,
K. Lipka, A. Lobanov, W. Lohmann19 , R. Mankel, I. Marfin19 , I.-A. Melzer-Pellmann, A.B. Meyer,
G. Mittag, J. Mnich, A. Mussgiller, S. Naumann-Emme, A. Nayak, E. Ntomari, H. Perrey, D. Pitzl,
R. Placakyte, A. Raspereza, B. Roland, M.Ö. Sahin, P. Saxena, T. Schoerner-Sadenius, M. Schröder,
C. Seitz, S. Spannagel, K.D. Trippkewitz, R. Walsh, C. Wissing
University of Hamburg, Hamburg, Germany
V. Blobel, M. Centis Vignali, A.R. Draeger, J. Erfle, E. Garutti, K. Goebel, D. Gonzalez, M. Görner,
J. Haller, M. Hoffmann, R.S. Höing, A. Junkes, R. Klanner, R. Kogler, T. Lapsien, T. Lenz,
I. Marchesini, D. Marconi, M. Meyer, D. Nowatschin, J. Ott, F. Pantaleo2 , T. Peiffer, A. Perieanu,
N. Pietsch, J. Poehlsen, D. Rathjens, C. Sander, H. Schettler, P. Schleper, E. Schlieckau, A. Schmidt,
J. Schwandt, M. Seidel, V. Sola, H. Stadie, G. Steinbrück, H. Tholen, D. Troendle, E. Usai,
L. Vanelderen, A. Vanhoefer, B. Vormwald
Institut für Experimentelle Kernphysik, Karlsruhe, Germany
M. Akbiyik, C. Barth, C. Baus, J. Berger, C. Böser, E. Butz, T. Chwalek, F. Colombo,
W. De Boer, A. Descroix, A. Dierlamm, S. Fink, F. Frensch, M. Giffels, A. Gilbert, D. Haitz,
F. Hartmann2 , S.M. Heindl, U. Husemann, I. Katkov6 , A. Kornmayer2 , P. Lobelle Pardo, B. Maier,
H. Mildner, M.U. Mozer, T. Müller, Th. Müller, M. Plagge, G. Quast, K. Rabbertz, S. Röcker,
F. Roscher, H.J. Simonis, F.M. Stober, R. Ulrich, J. Wagner-Kuhr, S. Wayand, M. Weber, T. Weiler,
C. Wöhrmann, R. Wolf
Institute of Nuclear and Particle Physics (INPP), NCSR Demokritos, Aghia Paraskevi, Greece
G. Anagnostou, G. Daskalakis, T. Geralis, V.A. Giakoumopoulou, A. Kyriakis, D. Loukas,
A. Psallidas, I. Topsis-Giotis
National and Kapodistrian University of Athens, Athens, Greece
A. Agapitos, S. Kesisoglou, A. Panagiotou, N. Saoulidou, E. Tziaferi

– 78 –

2017 JINST 12 P02014

V. Cherepanov, Y. Erdogan, G. Flügge, H. Geenen, M. Geisler, F. Hoehle, B. Kargoll, T. Kress,
Y. Kuessel, A. Künsken, J. Lingemann2 , A. Nehrkorn, A. Nowack, I.M. Nugent, C. Pistone, O. Pooth,
A. Stahl

## PDF page 82

University of Ioánnina, Ioánnina, Greece
I. Evangelou, G. Flouris, C. Foudas, P. Kokkas, N. Loukas, N. Manthos, I. Papadopoulos, E. Paradas,
J. Strologas
Wigner Research Centre for Physics, Budapest, Hungary
G. Bencze, C. Hajdu, A. Hazi, P. Hidas, D. Horvath20 , F. Sikler, V. Veszpremi, G. Vesztergombi21 ,
A.J. Zsigmond
Institute of Nuclear Research ATOMKI, Debrecen, Hungary

University of Debrecen, Debrecen, Hungary
M. Bartók23 , A. Makovec, P. Raics, Z.L. Trocsanyi, B. Ujvari
National Institute of Science Education and Research, Bhubaneswar, India
P. Mal, K. Mandal, D.K. Sahoo, N. Sahoo, S.K. Swain
Panjab University, Chandigarh, India
S. Bansal, S.B. Beri, V. Bhatnagar, R. Chawla, R. Gupta, U.Bhawandeep, A.K. Kalsi, A. Kaur,
M. Kaur, R. Kumar, A. Mehta, M. Mittal, J.B. Singh, G. Walia
University of Delhi, Delhi, India
Ashok Kumar, A. Bhardwaj, B.C. Choudhary, R.B. Garg, A. Kumar, S. Malhotra, M. Naimuddin,
N. Nishu, K. Ranjan, R. Sharma, V. Sharma
Saha Institute of Nuclear Physics, Kolkata, India
S. Bhattacharya, K. Chatterjee, S. Dey, S. Dutta, Sa. Jain, N. Majumdar, A. Modak, K. Mondal,
S. Mukherjee, S. Mukhopadhyay, A. Roy, D. Roy, S. Roy Chowdhury, S. Sarkar, M. Sharan
Bhabha Atomic Research Centre, Mumbai, India
A. Abdulsalam, R. Chudasama, D. Dutta, V. Jha, V. Kumar, A.K. Mohanty2 , L.M. Pant, P. Shukla,
A. Topkar
Tata Institute of Fundamental Research, Mumbai, India
T. Aziz, S. Banerjee, S. Bhowmik24 , R.M. Chatterjee, R.K. Dewanjee, S. Dugad, S. Ganguly,
S. Ghosh, M. Guchait, A. Gurtu25 , G. Kole, S. Kumar, B. Mahakud, M. Maity24 , G. Majumder,
K. Mazumdar, S. Mitra, G.B. Mohanty, B. Parida, T. Sarkar24 , N. Sur, B. Sutar, N. Wickramage26
Indian Institute of Science Education and Research (IISER), Pune, India
S. Chauhan, S. Dube, S. Sharma
Institute for Research in Fundamental Sciences (IPM), Tehran, Iran
H. Bakhshiansohi, H. Behnamian, S.M. Etesami27 , A. Fahim28 , R. Goldouzian, M. Khakzad,
M. Mohammadi Najafabadi, M. Naseri, S. Paktinat Mehdiabadi, F. Rezaei Hosseinabadi,
B. Safarzadeh29 , M. Zeinali
University College Dublin, Dublin, Ireland
M. Felcini, M. Grunewald

– 79 –

2017 JINST 12 P02014

N. Beni, S. Czellar, J. Karancsi22 , J. Molnar, Z. Szillasi

## PDF page 83

INFN Sezione di Bari a , Università di Bari b , Politecnico di Bari c , Bari, Italy
M. Abbresciaa, b , C. Calabriaa, b , C. Caputoa, b , A. Colaleoa , D. Creanzaa, c , L. Cristellaa, b , N. De
Filippisa, c , M. De Palmaa, b , L. Fiorea , G. Iasellia, c , G. Maggia, c , M. Maggia , G. Minielloa, b ,
S. Mya, c , S. Nuzzoa, b , A. Pompilia, b , G. Pugliesea, c , R. Radognaa, b , A. Ranieria , G. Selvaggia, b ,
L. Silvestrisa, 2 , R. Vendittia, b , P. Verwilligena
INFN Sezione di Bologna a , Università di Bologna b , Bologna, Italy

INFN Sezione di Catania a , Università di Catania b , Catania, Italy
G. Cappelloa , M. Chiorbolia, b , S. Costaa, b , F. Giordanoa, b , R. Potenzaa, b , A. Tricomia, b ,
C. Tuvea, b
INFN Sezione di Firenze a , Università di Firenze b , Firenze, Italy
G. Barbaglia , V. Ciullia, b , C. Civininia , R. D’Alessandroa, b , E. Focardia, b , S. Gonzia, b , V. Goria, b ,
P. Lenzia, b , M. Meschinia , S. Paolettia , G. Sguazzonia , A. Tropianoa, b , L. Viliania, b
INFN Laboratori Nazionali di Frascati, Frascati, Italy
L. Benussi, S. Bianco, F. Fabbri, D. Piccolo, F. Primavera
INFN Sezione di Genova a , Università di Genova b , Genova, Italy
V. Calvellia, b , F. Ferroa , M. Lo Veterea, b , M.R. Mongea, b , E. Robuttia , S. Tosia, b
INFN Sezione di Milano-Bicocca a , Università di Milano-Bicocca b , Milano, Italy
L. Brianza, M.E. Dinardoa, b , S. Fiorendia, b , S. Gennaia , R. Gerosaa, b , A. Ghezzia, b , P. Govonia, b ,
S. Malvezzia , R.A. Manzonia, b , B. Marzocchia, b, 2 , D. Menascea , L. Moronia , M. Paganonia, b ,
D. Pedrinia , S. Ragazzia, b , N. Redaellia , T. Tabarelli de Fatisa, b
INFN Sezione di Napoli a , Università di Napoli ’Federico II’ b , Napoli, Italy, Università della
Basilicata c , Potenza, Italy, Università G. Marconi d , Roma, Italy
S. Buontempoa , N. Cavalloa, c , S. Di Guidaa, d, 2 , M. Espositoa, b , F. Fabozzia, c , A.O.M. Iorioa, b ,
G. Lanzaa , L. Listaa , S. Meolaa, d, 2 , M. Merolaa , P. Paoluccia, 2 , C. Sciaccaa, b , F. Thyssen
INFN Sezione di Padova a , Università di Padova b , Padova, Italy, Università di Trento c ,
Trento, Italy
P. Azzia, 2 , N. Bacchettaa , M. Bellatoa , L. Benatoa, b , D. Biselloa, b , A. Bolettia, b , A. Brancaa, b ,
R. Carlina, b , P. Checchiaa , M. Dall’Ossoa, b, 2 , T. Dorigoa , U. Dossellia , F. Fanzagoa ,
F. Gasparinia, b , U. Gasparinia, b , F. Gonellaa , A. Gozzelinoa , K. Kanishcheva, c , S. Lacapraraa ,
G. Marona, 30 , J. Pazzinia, b , N. Pozzobona, b , P. Ronchesea, b , M. Tosia, b , S. Vaninia, b , S. Venturaa ,
M. Zanetti, A. Zucchettaa, b, 2 , G. Zumerlea, b

– 80 –

2017 JINST 12 P02014

G. Abbiendia , C. Battilana2 , A.C. Benvenutia , D. Bonacorsia, b , S. Braibant-Giacomellia, b ,
L. Brigliadoria, b , R. Campaninia, b , P. Capiluppia, b , A. Castroa, b , F.R. Cavalloa , S.S. Chhibraa, b ,
G. Codispotia, b , M. Cuffiania, b , G.M. Dallavallea , F. Fabbria , A. Fanfania, b , D. Fasanellaa, b ,
P. Giacomellia , C. Grandia , L. Guiduccia, b , S. Marcellinia , G. Masettia , A. Montanaria ,
F.L. Navarriaa, b , A. Perrottaa , A.M. Rossia, b , T. Rovellia, b , G.P. Sirolia, b , N. Tosia, b ,
R. Travaglinia, b

## PDF page 84

INFN Sezione di Pavia a , Università di Pavia b , Pavia, Italy
A. Braghieria , A. Magnania , P. Montagnaa, b , S.P. Rattia, b , V. Rea , C. Riccardia, b , P. Salvinia ,
I. Vaia , P. Vituloa, b
INFN Sezione di Perugia a , Università di Perugia b , Perugia, Italy
L. Alunni Solestizia, b , M. Biasinia, b , G.M. Bileia , D. Ciangottinia, b, 2 , L. Fanòa, b , P. Laricciaa, b ,
G. Mantovania, b , M. Menichellia , A. Sahaa , A. Santocchiaa, b , A. Spieziaa, b

INFN Sezione di Roma a , Università di Roma b , Roma, Italy
L. Baronea, b , F. Cavallaria , G. D’imperioa, b, 2 , D. Del Rea, b , M. Diemoza , S. Gellia, b , C. Jordaa ,
E. Longoa, b , F. Margarolia, b , P. Meridiania , G. Organtinia, b , R. Paramattia , F. Preiatoa, b ,
S. Rahatloua, b , C. Rovellia , F. Santanastasioa, b , P. Traczyka, b, 2
INFN Sezione di Torino a , Università di Torino b , Torino, Italy, Università del Piemonte
Orientale c , Novara, Italy
N. Amapanea, b , R. Arcidiaconoa, c, 2 , S. Argiroa, b , M. Arneodoa, c , R. Bellana, b , C. Biinoa ,
N. Cartigliaa , M. Costaa, b , R. Covarellia, b , A. Deganoa, b , N. Demariaa , L. Fincoa, b, 2 ,
B. Kiania, b , C. Mariottia , S. Masellia , E. Migliorea, b , V. Monacoa, b , E. Monteila, b , M. Musicha ,
M.M. Obertinoa, b , L. Pachera, b , N. Pastronea , M. Pelliccionia , G.L. Pinna Angionia, b ,
F. Raveraa, b , A. Romeroa, b , M. Ruspaa, c , R. Sacchia, b , A. Solanoa, b , A. Staianoa , U. Tamponia
INFN Sezione di Trieste a , Università di Trieste b , Trieste, Italy
S. Belfortea , V. Candelisea, b, 2 , M. Casarsaa , F. Cossuttia , G. Della Riccaa, b , B. Gobboa , C. La
Licataa, b , M. Maronea, b , A. Schizzia, b , A. Zanettia
Kangwon National University, Chunchon, Korea
A. Kropivnitskaya, S.K. Nam
Kyungpook National University, Daegu, Korea
D.H. Kim, G.N. Kim, M.S. Kim, D.J. Kong, S. Lee, Y.D. Oh, A. Sakharov, D.C. Son
Chonbuk National University, Jeonju, Korea
J.A. Brochero Cifuentes, H. Kim, T.J. Kim33
Chonnam National University, Institute for Universe and Elementary Particles, Kwangju,
Korea
S. Song
Korea University, Seoul, Korea
S. Choi, Y. Go, D. Gyun, B. Hong, M. Jo, H. Kim, Y. Kim, B. Lee, K. Lee, K.S. Lee, S. Lee,
S.K. Park, Y. Roh

– 81 –

2017 JINST 12 P02014

INFN Sezione di Pisa a , Università di Pisa b , Scuola Normale Superiore di Pisa c , Pisa, Italy
K. Androsova, 31 , P. Azzurria , G. Bagliesia , J. Bernardinia , T. Boccalia , G. Broccoloa, c ,
R. Castaldia , M.A. Cioccia, 31 , R. Dell’Orsoa , S. Donatoa, c, 2 , G. Fedi, L. Foàa, c † , A. Giassia ,
M.T. Grippoa, 31 , F. Ligabuea, c , T. Lomtadzea , L. Martinia, b , A. Messineoa, b , F. Pallaa ,
A. Rizzia, b , A. Savoy-Navarroa, 32 , A.T. Serbana , P. Spagnoloa , P. Squillaciotia, 31 , R. Tenchinia ,
G. Tonellia, b , A. Venturia , P.G. Verdinia

## PDF page 85

Seoul National University, Seoul, Korea
H.D. Yoo
University of Seoul, Seoul, Korea
M. Choi, H. Kim, J.H. Kim, J.S.H. Lee, I.C. Park, G. Ryu, M.S. Ryu
Sungkyunkwan University, Suwon, Korea
Y. Choi, J. Goh, D. Kim, E. Kwon, J. Lee, I. Yu

National Centre for Particle Physics, Universiti Malaya, Kuala Lumpur, Malaysia
I. Ahmed, Z.A. Ibrahim, J.R. Komaragiri, M.A.B. Md Ali34 , F. Mohamad Idris35 , W.A.T. Wan
Abdullah, M.N. Yusli
Centro de Investigacion y de Estudios Avanzados del IPN, Mexico City, Mexico
E. Casimiro Linares, H. Castilla-Valdez, E. De La Cruz-Burelo, I. Heredia-De La Cruz36 ,
A. Hernandez-Almada, R. Lopez-Fernandez, A. Sanchez-Hernandez
Universidad Iberoamericana, Mexico City, Mexico
S. Carrillo Moreno, F. Vazquez Valencia
Benemerita Universidad Autonoma de Puebla, Puebla, Mexico
I. Pedraza, H.A. Salazar Ibarguen
Universidad Autónoma de San Luis Potosí, San Luis Potosí, Mexico
A. Morelos Pineda
University of Auckland, Auckland, New Zealand
D. Krofcheck
University of Canterbury, Christchurch, New Zealand
P.H. Butler
National Centre for Physics, Quaid-I-Azam University, Islamabad, Pakistan
A. Ahmad, M. Ahmad, Q. Hassan, H.R. Hoorani, W.A. Khan, T. Khurshid, M. Shoaib
National Centre for Nuclear Research, Swierk, Poland
H. Bialkowska, M. Bluj, B. Boimska, T. Frueboes, M. Górski, M. Kazana, K. Nawrocki,
K. Romanowska-Rybinska, M. Szleper, P. Zalewski
Institute of Experimental Physics, Faculty of Physics, University of Warsaw, Warsaw, Poland
G. Brona, K. Bunkowski, A. Byszuk37 , K. Doroba, A. Kalinowski, M. Konecki, J. Krolikowski,
M. Misiura, M. Olszewski, M. Walczak
Laboratório de Instrumentação e Física Experimental de Partículas, Lisboa, Portugal
P. Bargassa, C. Beirão Da Cruz E Silva, A. Di Francesco, P. Faccioli, P.G. Ferreira Parracho,
M. Gallinaro, N. Leonardo, L. Lloret Iglesias, F. Nguyen, J. Rodrigues Antunes, J. Seixas,
O. Toldaiev, D. Vadruccio, J. Varela, P. Vischia

– 82 –

2017 JINST 12 P02014

Vilnius University, Vilnius, Lithuania
A. Juodagalvis, J. Vaitkus

## PDF page 86

Joint Institute for Nuclear Research, Dubna, Russia
S. Afanasiev, P. Bunin, M. Gavrilenko, I. Golutvin, I. Gorbunov, A. Kamenev, V. Karjavin,
V. Konoplyanikov, A. Lanev, A. Malakhov, V. Matveev38 , P. Moisenz, V. Palichik, V. Perelygin,
S. Shmatov, S. Shulha, N. Skatchkov, V. Smirnov, A. Zarubin
Petersburg Nuclear Physics Institute, Gatchina (St. Petersburg), Russia
V. Golovtsov, Y. Ivanov, V. Kim39 , E. Kuznetsova, P. Levchenko, V. Murzin, V. Oreshkin, I. Smirnov,
V. Sulimov, L. Uvarov, S. Vavilov, A. Vorobyev

Institute for Theoretical and Experimental Physics, Moscow, Russia
V. Epshteyn, V. Gavrilov, N. Lychkovskaya, V. Popov, I. Pozdnyakov, G. Safronov, A. Spiridonov,
E. Vlasov, A. Zhokin
National Research Nuclear University ’Moscow Engineering Physics Institute’ (MEPhI),
Moscow, Russia
A. Bylinkin
P.N. Lebedev Physical Institute, Moscow, Russia
V. Andreev, M. Azarkin40 , I. Dremin40 , M. Kirakosyan, A. Leonidov40 , G. Mesyats, S.V. Rusakov
Skobeltsyn Institute of Nuclear Physics, Lomonosov Moscow State University, Moscow, Russia
A. Baskakov, A. Belyaev, E. Boos, M. Dubinin41 , L. Dudko, A. Ershov, A. Gribushin,
A. Kaminskiy42 , V. Klyukhin, O. Kodolova, I. Lokhtin, I. Myagkov, S. Obraztsov, S. Petrushanko,
V. Savrin
State Research Center of Russian Federation, Institute for High Energy Physics, Protvino,
Russia
I. Azhgirey, I. Bayshev, S. Bitioukov, V. Kachanov, A. Kalinin, D. Konstantinov, V. Krychkine,
V. Petrov, R. Ryutin, A. Sobol, L. Tourtchanovitch, S. Troshin, N. Tyurin, A. Uzunian, A. Volkov
University of Belgrade, Faculty of Physics and Vinca Institute of Nuclear Sciences, Belgrade,
Serbia
P. Adzic43 , J. Milosevic, V. Rekovic
Centro de Investigaciones Energéticas Medioambientales y Tecnológicas (CIEMAT), Madrid,
Spain
J. Alcaraz Maestre, E. Calvo, M. Cerrada, M. Chamizo Llatas, N. Colino, B. De La Cruz, A. Delgado
Peris, D. Domínguez Vázquez, A. Escalante Del Valle, C. Fernandez Bedoya, J.P. Fernández
Ramos, J. Flix, M.C. Fouz, P. Garcia-Abia, O. Gonzalez Lopez, S. Goy Lopez, J.M. Hernandez,
M.I. Josa, E. Navarro De Martino, A. Pérez-Calero Yzquierdo, J. Puerta Pelayo, A. Quintario
Olmeda, I. Redondo, L. Romero, J. Santaolalla, M.S. Soares
Universidad Autónoma de Madrid, Madrid, Spain
C. Albajar, J.F. de Trocóniz, M. Missiroli, D. Moran

– 83 –

2017 JINST 12 P02014

Institute for Nuclear Research, Moscow, Russia
Yu. Andreev, A. Dermenev, S. Gninenko, N. Golubev, A. Karneyeu, M. Kirsanov, N. Krasnikov,
A. Pashenkov, D. Tlisov, A. Toropin

## PDF page 87

Universidad de Oviedo, Oviedo, Spain
J. Cuevas, J. Fernandez Menendez, S. Folgueras, I. Gonzalez Caballero, E. Palencia Cortezon,
J.M. Vizan Garcia
Instituto de Física de Cantabria (IFCA), CSIC-Universidad de Cantabria, Santander, Spain
I.J. Cabrillo, A. Calderon, J.R. Castiñeiras De Saa, P. De Castro Manzano, J. Duarte Campderros,
M. Fernandez, J. Garcia-Ferrero, G. Gomez, A. Lopez Virto, J. Marco, R. Marco, C. Martinez
Rivero, F. Matorras, F.J. Munoz Sanchez, J. Piedra Gomez, T. Rodrigo, A.Y. Rodríguez-Marrero,
A. Ruiz-Jimeno, L. Scodellaro, N. Trevisani, I. Vila, R. Vilar Cortabitarte
D. Abbaneo, E. Auffray, G. Auzinger, M. Bachtis, P. Baillon, A.H. Ball, D. Barney, A. Benaglia,
J. Bendavid, L. Benhabib, J.F. Benitez, G.M. Berruti, P. Bloch, A. Bocci, A. Bonato, C. Botta,
H. Breuker, T. Camporesi, R. Castello, G. Cerminara, M. D’Alfonso, D. d’Enterria, A. Dabrowski,
V. Daponte, A. David, M. De Gruttola, F. De Guio, A. De Roeck, S. De Visscher, E. Di Marco,
M. Dobson, M. Dordevic, B. Dorney, T. du Pree, M. Dünser, N. Dupont, A. Elliott-Peisert,
G. Franzoni, W. Funk, D. Gigi, K. Gill, D. Giordano, M. Girone, F. Glege, R. Guida, S. Gundacker,
M. Guthoff, J. Hammer, P. Harris, J. Hegeman, V. Innocente, P. Janot, H. Kirschenmann,
M.J. Kortelainen, K. Kousouris, K. Krajczar, P. Lecoq, C. Lourenço, M.T. Lucchini, N. Magini,
L. Malgeri, M. Mannelli, A. Martelli, L. Masetti, F. Meijers, S. Mersi, E. Meschi, F. Moortgat,
S. Morovic, M. Mulders, M.V. Nemallapudi, H. Neugebauer, S. Orfanelli44 , L. Orsini, L. Pape,
E. Perez, M. Peruzzi, A. Petrilli, G. Petrucciani, A. Pfeiffer, D. Piparo, A. Racz, G. Rolandi45 ,
M. Rovere, M. Ruan, H. Sakulin, C. Schäfer, C. Schwick, A. Sharma, P. Silva, M. Simon,
P. Sphicas46 , J. Steggemann, B. Stieger, M. Stoye, Y. Takahashi, D. Treille, A. Triossi, A. Tsirou,
G.I. Veres21 , N. Wardle, H.K. Wöhri, A. Zagozdzinska37 , W.D. Zeuner
Paul Scherrer Institut, Villigen, Switzerland
W. Bertl, K. Deiters, W. Erdmann, R. Horisberger, Q. Ingram, H.C. Kaestli, D. Kotlinski,
U. Langenegger, D. Renker, T. Rohe
Institute for Particle Physics, ETH Zurich, Zurich, Switzerland
F. Bachmair, L. Bäni, L. Bianchini, B. Casal, G. Dissertori, M. Dittmar, M. Donegà, P. Eller, C. Grab,
C. Heidegger, D. Hits, J. Hoss, G. Kasieczka, W. Lustermann, B. Mangano, M. Marionneau,
P. Martinez Ruiz del Arbol, M. Masciovecchio, D. Meister, F. Micheli, P. Musella, F. Nessi-Tedaldi,
F. Pandolfi, J. Pata, F. Pauss, L. Perrozzi, M. Quittnat, M. Rossini, A. Starodumov47 , M. Takahashi,
V.R. Tavolaro, K. Theofilatos, R. Wallny
Universität Zürich, Zurich, Switzerland
T.K. Aarrestad, C. Amsler48 , L. Caminada, M.F. Canelli, V. Chiochia, A. De Cosa, C. Galloni,
A. Hinzmann, T. Hreus, B. Kilminster, C. Lange, J. Ngadiuba, D. Pinna, P. Robmann, F.J. Ronga,
D. Salerno, Y. Yang
National Central University, Chung-Li, Taiwan
M. Cardaci, K.H. Chen, T.H. Doan, Sh. Jain, R. Khurana, M. Konyushikhin, C.M. Kuo, W. Lin,
Y.J. Lu, S.S. Yu

– 84 –

2017 JINST 12 P02014

CERN, European Organization for Nuclear Research, Geneva, Switzerland

## PDF page 88

National Taiwan University (NTU), Taipei, Taiwan
Arun Kumar, R. Bartek, P. Chang, Y.H. Chang, Y.W. Chang, Y. Chao, K.F. Chen, P.H. Chen,
C. Dietz, F. Fiori, U. Grundler, W.-S. Hou, Y. Hsiung, Y.F. Liu, R.-S. Lu, M. Miñano Moya,
E. Petrakou, J.f. Tsai, Y.M. Tzeng
Chulalongkorn University, Faculty of Science, Department of Physics, Bangkok, Thailand
B. Asavapibhop, K. Kovitanggoon, G. Singh, N. Srimanobhas, N. Suwonjandee

Middle East Technical University, Physics Department, Ankara, Turkey
I.V. Akin, B. Bilin, S. Bilmis, B. Isildak54 , G. Karapinar55 , M. Yalvac, M. Zeyrek
Bogazici University, Istanbul, Turkey
E.A. Albayrak56 , E. Gülmez, M. Kaya57 , O. Kaya58 , T. Yetkin59
Istanbul Technical University, Istanbul, Turkey
K. Cankocak, S. Sen60 , F.I. Vardarlı
Institute for Scintillation Materials of National Academy of Science of Ukraine, Kharkov,
Ukraine
B. Grynyov
National Scientific Center, Kharkov Institute of Physics and Technology, Kharkov, Ukraine
L. Levchuk, P. Sorokin
University of Bristol, Bristol, United Kingdom
R. Aggleton, F. Ball, L. Beck, J.J. Brooke, E. Clement, D. Cussans, H. Flacher, J. Goldstein,
M. Grimes, G.P. Heath, H.F. Heath, J. Jacob, L. Kreczko, C. Lucas, Z. Meng, D.M. Newbold61 ,
S. Paramesvaran, A. Poll, T. Sakuma, S. Seif El Nasr-storey, S. Senkin, D. Smith, V.J. Smith
Rutherford Appleton Laboratory, Didcot, United Kingdom
K.W. Bell, A. Belyaev62 , C. Brew, R.M. Brown, D. Cieri, D.J.A. Cockerill, J.A. Coughlan,
K. Harder, S. Harper, E. Olaiya, D. Petyt, C.H. Shepherd-Themistocleous, A. Thea, I.R. Tomalin,
T. Williams, W.J. Womersley, S.D. Worm
Imperial College, London, United Kingdom
M. Baber, R. Bainbridge, O. Buchmuller, A. Bundock, D. Burton, S. Casasso, M. Citron, D. Colling,
L. Corpe, N. Cripps, P. Dauncey, G. Davies, A. De Wit, M. Della Negra, P. Dunne, A. Elwood,
W. Ferguson, J. Fulcher, D. Futyan, G. Hall, G. Iles, M. Kenzie, R. Lane, R. Lucas61 , L. Lyons,
A.-M. Magnan, S. Malik, J. Nash, A. Nikitenko47 , J. Pela, M. Pesaresi, K. Petridis, D.M. Raymond,
A. Richards, A. Rose, C. Seez, A. Tapper, K. Uchida, M. Vazquez Acosta63 , T. Virdee, S.C. Zenz
Brunel University, Uxbridge, United Kingdom
J.E. Cole, P.R. Hobson, A. Khan, P. Kyberd, D. Leggat, D. Leslie, I.D. Reid, P. Symonds,
L. Teodorescu, M. Turner

– 85 –

2017 JINST 12 P02014

Cukurova University, Adana, Turkey
A. Adiguzel, S. Cerci49 , Z.S. Demiroglu, C. Dozen, I. Dumanoglu, S. Girgis, G. Gokbulut, Y. Guler,
E. Gurpinar, I. Hos, E.E. Kangal50 , A. Kayis Topaksu, G. Onengut51 , K. Ozdemir52 , S. Ozturk53 ,
B. Tali49 , H. Topakli53 , M. Vergili, C. Zorbilmez

## PDF page 89

Baylor University, Waco, U.S.A.
A. Borzou, K. Call, J. Dittmann, K. Hatakeyama, A. Kasmi, H. Liu, N. Pastika
The University of Alabama, Tuscaloosa, U.S.A.
O. Charaf, S.I. Cooper, C. Henderson, P. Rumerio
Boston University, Boston, U.S.A.
A. Avetisyan, T. Bose, C. Fantasia, D. Gastler, P. Lawson, D. Rankin, C. Richardson, J. Rohlf,
J. St. John, L. Sulak, D. Zou
J. Alimena, E. Berry, S. Bhattacharya, D. Cutts, N. Dhingra, A. Ferapontov, A. Garabedian,
J. Hakala, U. Heintz, E. Laird, G. Landsberg, Z. Mao, M. Narain, S. Piperov, S. Sagir,
T. Sinthuprasith, R. Syarif
University of California, Davis, Davis, U.S.A.
R. Breedon, G. Breto, M. Calderon De La Barca Sanchez, S. Chauhan, M. Chertok, J. Conway,
R. Conway, P.T. Cox, R. Erbacher, M. Gardner, W. Ko, R. Lander, M. Mulhearn, D. Pellett, J. Pilot,
F. Ricci-Tam, S. Shalhout, J. Smith, M. Squires, D. Stolp, M. Tripathi, S. Wilbur, R. Yohay
University of California, Los Angeles, U.S.A.
R. Cousins, P. Everaerts, C. Farrell, J. Hauser, M. Ignatenko, D. Saltzberg, E. Takasugi, V. Valuev,
M. Weber
University of California, Riverside, Riverside, U.S.A.
K. Burt, R. Clare, J. Ellison, J.W. Gary, G. Hanson, J. Heilman, M. Ivova PANEVA, P. Jandir,
E. Kennedy, F. Lacroix, O.R. Long, A. Luthra, M. Malberti, M. Olmedo Negrete, A. Shrinivas,
H. Wei, S. Wimpenny, B. R. Yates
University of California, San Diego, La Jolla, U.S.A.
J.G. Branson, G.B. Cerati, S. Cittolin, R.T. D’Agnolo, A. Holzner, R. Kelley, D. Klein, J. Letts,
I. Macneill, D. Olivito, S. Padhi, M. Pieri, M. Sani, V. Sharma, S. Simon, M. Tadel, A. Vartak,
S. Wasserbaech64 , C. Welke, F. Würthwein, A. Yagil, G. Zevi Della Porta
University of California, Santa Barbara, Santa Barbara, U.S.A.
D. Barge, J. Bradmiller-Feld, C. Campagnari, A. Dishaw, V. Dutta, K. Flowers, M. Franco Sevilla,
P. Geffert, C. George, F. Golf, L. Gouskos, J. Gran, J. Incandela, C. Justus, N. Mccoll, S.D. Mullin,
J. Richman, D. Stuart, I. Suarez, W. To, C. West, J. Yoo
California Institute of Technology, Pasadena, U.S.A.
D. Anderson, A. Apresyan, A. Bornheim, J. Bunn, Y. Chen, J. Duarte, A. Mott, H.B. Newman,
C. Pena, M. Pierini, M. Spiropulu, J.R. Vlimant, S. Xie, R.Y. Zhu
Carnegie Mellon University, Pittsburgh, U.S.A.
M.B. Andrews, V. Azzolini, A. Calamba, B. Carlson, T. Ferguson, M. Paulini, J. Russ, M. Sun,
H. Vogel, I. Vorobiev

– 86 –

2017 JINST 12 P02014

Brown University, Providence, U.S.A.

## PDF page 90

University of Colorado Boulder, Boulder, U.S.A.
J.P. Cumalat, W.T. Ford, A. Gaz, F. Jensen, A. Johnson, M. Krohn, T. Mulholland, U. Nauenberg,
K. Stenson, S.R. Wagner
Cornell University, Ithaca, U.S.A.
J. Alexander, A. Chatterjee, J. Chaves, J. Chu, S. Dittmer, N. Eggert, N. Mirman, G. Nicolas
Kaufman, J.R. Patterson, A. Rinkevicius, A. Ryd, L. Skinnari, L. Soffi, W. Sun, S.M. Tan, W.D. Teo,
J. Thom, J. Thompson, J. Tucker, Y. Weng, P. Wittich

University of Florida, Gainesville, U.S.A.
D. Acosta, P. Avery, P. Bortignon, D. Bourilkov, A. Carnes, M. Carver, D. Curry, S. Das, G.P. Di
Giovanni, R.D. Field, I.K. Furic, J. Hugon, J. Konigsberg, A. Korytov, J.F. Low, P. Ma, K. Matchev,
H. Mei, P. Milenovic65 , G. Mitselmakher, D. Rank, R. Rossin, L. Shchutska, M. Snowball,
D. Sperka, N. Terentyev, L. Thomas, J. Wang, S. Wang, J. Yelton
Florida International University, Miami, U.S.A.
S. Hewamanage, S. Linn, P. Markowitz, G. Martinez, J.L. Rodriguez
Florida State University, Tallahassee, U.S.A.
A. Ackert, J.R. Adams, T. Adams, A. Askew, J. Bochenek, B. Diamond, J. Haas, S. Hagopian,
V. Hagopian, K.F. Johnson, A. Khatiwada, H. Prosper, M. Weinberg
Florida Institute of Technology, Melbourne, U.S.A.
M.M. Baarmand, V. Bhopatkar, S. Colafranceschi66 , M. Hohlmann, H. Kalakhety, D. Noonan,
T. Roy, F. Yumiceva
University of Illinois at Chicago (UIC), Chicago, U.S.A.
M.R. Adams, L. Apanasevich, D. Berry, R.R. Betts, I. Bucinskaite, R. Cavanaugh, O. Evdokimov,
L. Gauthier, C.E. Gerber, D.J. Hofman, P. Kurt, C. O’Brien, I.D. Sandoval Gonzalez, C. Silkworth,
P. Turner, N. Varelas, Z. Wu, M. Zakaria
The University of Iowa, Iowa City, U.S.A.
B. Bilki67 , W. Clarida, K. Dilsiz, S. Durgut, R.P. Gandrajula, M. Haytmyradov, V. Khristenko,
J.-P. Merlo, H. Mermerkaya68 , A. Mestvirishvili, A. Moeller, J. Nachtman, H. Ogul, Y. Onel,
F. Ozok56 , A. Penzo, C. Snyder, P. Tan, E. Tiras, J. Wetzel, K. Yi

– 87 –

2017 JINST 12 P02014

Fermi National Accelerator Laboratory, Batavia, U.S.A.
S. Abdullin, M. Albrow, J. Anderson, G. Apollinari, S. Banerjee, L.A.T. Bauerdick, A. Beretvas,
J. Berryhill, P.C. Bhat, G. Bolla, K. Burkett, J.N. Butler, H.W.K. Cheung, F. Chlebana, S. Cihangir,
V.D. Elvira, I. Fisk, J. Freeman, E. Gottschalk, L. Gray, D. Green, S. Grünendahl, O. Gutsche,
J. Hanlon, D. Hare, R.M. Harris, S. Hasegawa, J. Hirschauer, Z. Hu, S. Jindariani, M. Johnson,
U. Joshi, A.W. Jung, B. Klima, B. Kreis, S. Kwan† , S. Lammel, J. Linacre, D. Lincoln,
R. Lipton, T. Liu, R. Lopes De Sá, J. Lykken, K. Maeshima, J.M. Marraffino, V.I. Martinez
Outschoorn, S. Maruyama, D. Mason, P. McBride, P. Merkel, K. Mishra, S. Mrenna, S. Nahn,
C. Newman-Holmes, V. O’Dell, K. Pedro, O. Prokofyev, G. Rakness, E. Sexton-Kennedy, A. Soha,
W.J. Spalding, L. Spiegel, L. Taylor, S. Tkaczyk, N.V. Tran, L. Uplegger, E.W. Vaandering,
C. Vernieri, M. Verzocchi, R. Vidal, H.A. Weber, A. Whitbeck, F. Yang

## PDF page 91

Johns Hopkins University, Baltimore, U.S.A.
I. Anderson, B.A. Barnett, B. Blumenfeld, N. Eminizer, D. Fehling, L. Feng, A.V. Gritsan,
P. Maksimovic, C. Martin, M. Osherson, J. Roskes, A. Sady, U. Sarica, M. Swartz, M. Xiao,
Y. Xin, C. You
The University of Kansas, Lawrence, U.S.A.
P. Baringer, A. Bean, G. Benelli, C. Bruner, R.P. Kenny III, D. Majumder, M. Malek, M. Murray,
S. Sanders, R. Stringer, Q. Wang
Kansas State University, Manhattan, U.S.A.

Lawrence Livermore National Laboratory, Livermore, U.S.A.
D. Lange, F. Rebassoo, D. Wright
University of Maryland, College Park, U.S.A.
C. Anelli, A. Baden, O. Baron, A. Belloni, B. Calvert, S.C. Eno, C. Ferraioli, J.A. Gomez,
N.J. Hadley, S. Jabeen, R.G. Kellogg, T. Kolberg, J. Kunkle, Y. Lu, A.C. Mignerey, Y.H. Shin,
A. Skuja, M.B. Tonjes, S.C. Tonwar
Massachusetts Institute of Technology, Cambridge, U.S.A.
A. Apyan, R. Barbieri, A. Baty, K. Bierwagen, S. Brandt, W. Busza, I.A. Cali, Z. Demiragli, L. Di
Matteo, G. Gomez Ceballos, M. Goncharov, D. Gulhan, Y. Iiyama, G.M. Innocenti, M. Klute,
D. Kovalskyi, Y.S. Lai, Y.-J. Lee, A. Levin, P.D. Luckey, A.C. Marini, C. Mcginn, C. Mironov,
X. Niu, C. Paus, D. Ralph, C. Roland, G. Roland, J. Salfeld-Nebgen, G.S.F. Stephans, K. Sumorok,
M. Varma, D. Velicanu, J. Veverka, J. Wang, T.W. Wang, B. Wyslouch, M. Yang, V. Zhukova
University of Minnesota, Minneapolis, U.S.A.
B. Dahmes, A. Evans, A. Finkel, A. Gude, P. Hansen, S. Kalafut, S.C. Kao, K. Klapoetke, Y. Kubota,
Z. Lesko, J. Mans, S. Nourbakhsh, N. Ruckstuhl, R. Rusack, N. Tambe, J. Turkewitz
University of Mississippi, Oxford, U.S.A.
J.G. Acosta, S. Oliveros
University of Nebraska-Lincoln, Lincoln, U.S.A.
E. Avdeeva, K. Bloom, S. Bose, D.R. Claes, A. Dominguez, C. Fangmeier, R. Gonzalez Suarez,
R. Kamalieddin, J. Keller, D. Knowlton, I. Kravchenko, J. Lazo-Flores, F. Meier, J. Monroy,
F. Ratnikov, J.E. Siado, G.R. Snow
State University of New York at Buffalo, Buffalo, U.S.A.
M. Alyari, J. Dolen, J. George, A. Godshalk, C. Harrington, I. Iashvili, J. Kaisen, A. Kharchilava,
A. Kumar, S. Rappoccio, B. Roozbahani
Northeastern University, Boston, U.S.A.
G. Alverson, E. Barberis, D. Baumgartel, M. Chasco, A. Hortiangtham, A. Massironi, D.M. Morse,
D. Nash, T. Orimoto, R. Teixeira De Lima, D. Trocino, R.-J. Wang, D. Wood, J. Zhang

– 88 –

2017 JINST 12 P02014

A. Ivanov, K. Kaadze, S. Khalil, M. Makouski, Y. Maravin, A. Mohammadi, L.K. Saini,
N. Skhirtladze, S. Toda

## PDF page 92

Northwestern University, Evanston, U.S.A.
K.A. Hahn, A. Kubik, N. Mucia, N. Odell, B. Pollack, A. Pozdnyakov, M. Schmitt, S. Stoynev,
K. Sung, M. Trovato, M. Velasco
University of Notre Dame, Notre Dame, U.S.A.
A. Brinkerhoff, N. Dev, M. Hildreth, C. Jessop, D.J. Karmgard, N. Kellams, K. Lannon, S. Lynch,
N. Marinelli, F. Meng, C. Mueller, Y. Musienko38 , T. Pearson, M. Planer, A. Reinsvold, R. Ruchti,
G. Smith, S. Taroni, N. Valls, M. Wayne, M. Wolf, A. Woodard
L. Antonelli, J. Brinson, B. Bylsma, L.S. Durkin, S. Flowers, A. Hart, C. Hill, R. Hughes, W. Ji,
K. Kotov, T.Y. Ling, B. Liu, W. Luo, D. Puigh, M. Rodenburg, B.L. Winer, H.W. Wulsin
Princeton University, Princeton, U.S.A.
O. Driga, P. Elmer, J. Hardenbrook, P. Hebda, S.A. Koay, P. Lujan, D. Marlow, T. Medvedeva,
M. Mooney, J. Olsen, C. Palmer, P. Piroué, X. Quan, H. Saka, D. Stickland, C. Tully, J.S. Werner,
A. Zuranski
University of Puerto Rico, Mayaguez, U.S.A.
S. Malik
Purdue University, West Lafayette, U.S.A.
V.E. Barnes, D. Benedetti, D. Bortoletto, L. Gutay, M.K. Jha, M. Jones, K. Jung, D.H. Miller,
N. Neumeister, B.C. Radburn-Smith, X. Shi, I. Shipsey, D. Silvers, J. Sun, A. Svyatkovskiy,
F. Wang, W. Xie, L. Xu
Purdue University Calumet, Hammond, U.S.A.
N. Parashar, J. Stupak
Rice University, Houston, U.S.A.
A. Adair, B. Akgun, Z. Chen, K.M. Ecklund, F.J.M. Geurts, M. Guilbaud, W. Li, B. Michlin,
M. Northup, B.P. Padley, R. Redjimi, J. Roberts, J. Rorie, Z. Tu, J. Zabel
University of Rochester, Rochester, U.S.A.
B. Betchart, A. Bodek, P. de Barbaro, R. Demina, Y. Eshaq, T. Ferbel, M. Galanti, A. Garcia-Bellido,
J. Han, A. Harel, O. Hindrichs, A. Khukhunaishvili, G. Petrillo, M. Verzetti
Rutgers, The State University of New Jersey, Piscataway, U.S.A.
S. Arora, A. Barker, J.P. Chou, C. Contreras-Campana, E. Contreras-Campana, D. Duggan,
D. Ferencek, Y. Gershtein, R. Gray, E. Halkiadakis, D. Hidas, E. Hughes, S. Kaplan, R. Kunnawalkam Elayavalli, A. Lath, K. Nash, S. Panwalkar, M. Park, S. Salur, S. Schnetzer, D. Sheffield,
S. Somalwar, R. Stone, S. Thomas, P. Thomassen, M. Walker
University of Tennessee, Knoxville, U.S.A.
M. Foerster, G. Riley, K. Rose, S. Spanier, A. York

– 89 –

2017 JINST 12 P02014

The Ohio State University, Columbus, U.S.A.

## PDF page 93

Texas A&M University, College Station, U.S.A.
O. Bouhali69 , A. Castaneda Hernandez69 , M. Dalchenko, M. De Mattia, A. Delgado, S. Dildick,
R. Eusebi, J. Gilmore, T. Kamon70 , V. Krutelyov, R. Mueller, I. Osipenkov, Y. Pakhotin, R. Patel,
A. Perloff, A. Rose, A. Safonov, A. Tatarinov, K.A. Ulmer2
Texas Tech University, Lubbock, U.S.A.
N. Akchurin, C. Cowden, J. Damgov, C. Dragoiu, P.R. Dudero, J. Faulkner, S. Kunori,
K. Lamichhane, S.W. Lee, T. Libeiro, S. Undleeb, I. Volobouev

University of Virginia, Charlottesville, U.S.A.
M.W. Arenton, B. Cox, B. Francis, J. Goodell, R. Hirosky, A. Ledovskoy, H. Li, C. Lin, C. Neu,
X. Sun, Y. Wang, E. Wolfe, J. Wood, F. Xia
Wayne State University, Detroit, U.S.A.
C. Clarke, R. Harr, P.E. Karchin, C. Kottachchi Kankanamge Don, P. Lamichhane, J. Sturdy
University of Wisconsin - Madison, Madison, WI, U.S.A.
D.A. Belknap, D. Carlsmith, M. Cepeda, S. Dasu, L. Dodd, S. Duric, E. Friis, B. Gomber,
M. Grothe, R. Hall-Wilton, M. Herndon, A. Hervé, P. Klabbers, A. Lanaro, A. Levine, K. Long,
R. Loveless, A. Mohapatra, I. Ojalvo, T. Perry, G.A. Pierro, G. Polese, T. Ruggles, T. Sarangi,
A. Savin, A. Sharma, N. Smith, W.H. Smith, D. Taylor, N. Woods
†: Deceased
1: Also at Vienna University of Technology, Vienna, Austria
2: Also at CERN, European Organization for Nuclear Research, Geneva, Switzerland
3: Also at State Key Laboratory of Nuclear Physics and Technology, Peking University, Beijing, China
4: Also at Institut Pluridisciplinaire Hubert Curien, Université de Strasbourg, Université de Haute Alsace
Mulhouse, CNRS/IN2P3, Strasbourg, France
5: Also at National Institute of Chemical Physics and Biophysics, Tallinn, Estonia
6: Also at Skobeltsyn Institute of Nuclear Physics, Lomonosov Moscow State University, Moscow, Russia
7: Also at Universidade Estadual de Campinas, Campinas, Brazil
8: Also at Centre National de la Recherche Scientifique (CNRS) - IN2P3, Paris, France
9: Also at Laboratoire Leprince-Ringuet, Ecole Polytechnique, IN2P3-CNRS, Palaiseau, France
10: Also at Joint Institute for Nuclear Research, Dubna, Russia
11: Now at Suez University, Suez, Egypt
12: Now at British University in Egypt, Cairo, Egypt
13: Also at Cairo University, Cairo, Egypt
14: Also at Fayoum University, El-Fayoum, Egypt
15: Also at Université de Haute Alsace, Mulhouse, France
16: Also at Tbilisi State University, Tbilisi, Georgia
17: Also at RWTH Aachen University, III. Physikalisches Institut A, Aachen, Germany
18: Also at University of Hamburg, Hamburg, Germany
19: Also at Brandenburg University of Technology, Cottbus, Germany

– 90 –

2017 JINST 12 P02014

Vanderbilt University, Nashville, U.S.A.
E. Appelt, A.G. Delannoy, S. Greene, A. Gurrola, R. Janjam, W. Johns, C. Maguire, Y. Mao,
A. Melo, H. Ni, P. Sheldon, B. Snook, S. Tuo, J. Velkovska, Q. Xu

## PDF page 94

– 91 –

2017 JINST 12 P02014

20: Also at Institute of Nuclear Research ATOMKI, Debrecen, Hungary
21: Also at Eötvös Loránd University, Budapest, Hungary
22: Also at University of Debrecen, Debrecen, Hungary
23: Also at Wigner Research Centre for Physics, Budapest, Hungary
24: Also at University of Visva-Bharati, Santiniketan, India
25: Now at King Abdulaziz University, Jeddah, Saudi Arabia
26: Also at University of Ruhuna, Matara, Sri Lanka
27: Also at Isfahan University of Technology, Isfahan, Iran
28: Also at University of Tehran, Department of Engineering Science, Tehran, Iran
29: Also at Plasma Physics Research Center, Science and Research Branch, Islamic Azad University,
Tehran, Iran
30: Also at Laboratori Nazionali di Legnaro dell’INFN, Legnaro, Italy
31: Also at Università degli Studi di Siena, Siena, Italy
32: Also at Purdue University, West Lafayette, U.S.A.
33: Now at Hanyang University, Seoul, Korea
34: Also at International Islamic University of Malaysia, Kuala Lumpur, Malaysia
35: Also at Malaysian Nuclear Agency, MOSTI, Kajang, Malaysia
36: Also at Consejo Nacional de Ciencia y Tecnología, Mexico city, Mexico
37: Also at Warsaw University of Technology, Institute of Electronic Systems, Warsaw, Poland
38: Also at Institute for Nuclear Research, Moscow, Russia
39: Also at St. Petersburg State Polytechnical University, St. Petersburg, Russia
40: Also at National Research Nuclear University ’Moscow Engineering Physics Institute’ (MEPhI),
Moscow, Russia
41: Also at California Institute of Technology, Pasadena, U.S.A.
42: Also at INFN Sezione di Padova; Università di Padova; Università di Trento (Trento), Padova, Italy
43: Also at Faculty of Physics, University of Belgrade, Belgrade, Serbia
44: Also at National Technical University of Athens, Athens, Greece
45: Also at Scuola Normale e Sezione dell’INFN, Pisa, Italy
46: Also at National and Kapodistrian University of Athens, Athens, Greece
47: Also at Institute for Theoretical and Experimental Physics, Moscow, Russia
48: Also at Albert Einstein Center for Fundamental Physics, Bern, Switzerland
49: Also at Adiyaman University, Adiyaman, Turkey
50: Also at Mersin University, Mersin, Turkey
51: Also at Cag University, Mersin, Turkey
52: Also at Piri Reis University, Istanbul, Turkey
53: Also at Gaziosmanpasa University, Tokat, Turkey
54: Also at Ozyegin University, Istanbul, Turkey
55: Also at Izmir Institute of Technology, Izmir, Turkey
56: Also at Mimar Sinan University, Istanbul, Istanbul, Turkey
57: Also at Marmara University, Istanbul, Turkey
58: Also at Kafkas University, Kars, Turkey
59: Also at Yildiz Technical University, Istanbul, Turkey
60: Also at Hacettepe University, Ankara, Turkey
61: Also at Rutherford Appleton Laboratory, Didcot, United Kingdom
62: Also at School of Physics and Astronomy, University of Southampton, Southampton, United Kingdom
63: Also at Instituto de Astrofísica de Canarias, La Laguna, Spain
64: Also at Utah Valley University, Orem, U.S.A.
65: Also at University of Belgrade, Faculty of Physics and Vinca Institute of Nuclear Sciences, Belgrade,
Serbia

## PDF page 95

66: Also at Facoltà Ingegneria, Università di Roma, Roma, Italy
67: Also at Argonne National Laboratory, Argonne, U.S.A.
68: Also at Erzincan University, Erzincan, Turkey
69: Also at Texas A&M University at Qatar, Doha, Qatar
70: Also at Kyungpook National University, Daegu, Korea

2017 JINST 12 P02014

– 92 –
