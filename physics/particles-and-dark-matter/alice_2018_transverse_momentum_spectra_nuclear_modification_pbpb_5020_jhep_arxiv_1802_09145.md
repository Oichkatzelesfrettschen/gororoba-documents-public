Source: https://arxiv.org/abs/1802.09145v2
PDF sha256: 3d0cc130f9e5decd8fed662a04119308916cd1a571c85ea44fcd1f1e15553d80
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of alice_2018_transverse_momentum_spectra_nuclear_modification_pbpb_5020_jhep_arxiv_1802_09145.pdf

Transcription of `alice_2018_transverse_momentum_spectra_nuclear_modification_pbpb_5020_jhep_arxiv_1802_09145.pdf` in this directory, 28 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-28 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

EUROPEAN ORGANIZATION FOR NUCLEAR RESEARCH

CERN-EP-2018-025
16 Feb 2018

arXiv:1802.09145v2 [nucl-ex] 18 Jan 2019

Transverse momentum spectra and nuclear modification factors of
charged particles in pp, p–Pb and Pb–Pb collisions at the LHC
ALICE Collaboration∗

Abstract
We report the measured transverse momentum (pT ) spectra of primary charged particles from pp,
√
p–Pb and Pb–Pb collisions at a center-of-mass energy sNN = 5.02 TeV in the kinematic range
of 0.15 < pT < 50 GeV/c and |η| < 0.8. A significant improvement of systematic uncertainties
√
motivated the reanalysis of data in pp and Pb–Pb collisions at sNN = 2.76 TeV, as well as in p–Pb
√
collisions at sNN = 5.02 TeV, which is also presented. Spectra from Pb–Pb collisions are presented
in nine centrality intervals and are compared to a reference spectrum from pp collisions scaled by the
number of binary nucleon-nucleon collisions. For central collisions, the pT spectra are suppressed
by more than a factor of 7 around 6–7 GeV/c with a significant reduction in suppression towards
higher momenta up to 30 GeV/c. The nuclear modification factor RpPb , constructed from the pp and
p–Pb spectra measured at the same collision energy, is consistent with unity above 8 GeV/c. While
√
the spectra in both pp and Pb–Pb collisions are substantially harder at sNN = 5.02 TeV compared
to 2.76 TeV, the nuclear modification factors show no significant collision energy dependence. The
obtained results should provide further constraints on the parton energy loss calculations to determine
the transport properties of the hot and dense QCD matter.

c 2018 CERN for the benefit of the ALICE Collaboration.
⃝
Reproduction of this article or parts of it is allowed as specified in the CC-BY-4.0 license.
∗ See Appendix A for the list of collaboration members

## PDF page 2

Charged-particle spectra and nuclear modification factors

1

ALICE Collaboration

Introduction

The properties of hot and dense deconfined QCD matter, the Quark-Gluon Plasma (QGP), which is
formed in high-energy heavy-ion collisions, can be characterized by the measurement of high transverse momentum particles produced by hadronisation of hard scattered partons in the early stage of the
collision. It is expected that these partons lose energy by interactions with the hot and dense QCD
matter, which leads to jet quenching [1]. Manifested also as a suppression of high-pT particles, jet
quenching enables the extraction of the properties of the deconfined medium, in particular its transport
coefficient q̂ [2].
The modification of high-pT particle production is quantified with the nuclear modification factor RAA ,
defined as the ratio of the charged-particle pT spectrum in A–A collisions to that in pp collisions scaled
by the average number of binary nucleon–nucleon collisions ⟨Ncoll ⟩ for a given centrality class of A–A
collisions,
dN AA /dpT
dN AA /dpT
RAA =
=
,
(1)
⟨Ncoll ⟩dN pp /dpT ⟨TAA ⟩dσ pp /dpT
where N AA and N pp are the charged-particle yields in A–A and pp collisions and σ pp is the production
NN ,
cross section in pp collisions, respectively. The average nuclear overlap function, ⟨TAA ⟩ = ⟨Ncoll ⟩/σinel
which depends on the collision centrality, is determined from the Glauber model of the nuclear collision
NN is the total inelastic nucleon-nucleon cross section. Over the years, a number
geometry [3], where σinel
of results on RAA have been reported by experiments at the Relativistic Heavy-Ion Collider (RHIC) and
at the Large Hadron Collider (LHC). At RHIC, the yields of charged hadrons [4, 5] or neutral pions [6]
√
measured in the central Au–Au collisions at sNN = 130 and 200 GeV were found to be suppressed by
a factor of about 5 in the pT range of 5–25 GeV/c, indicating for the first time strong medium effects
on hadron production. The first RAA measurements for charged particles at the LHC [7–10] have shown
√
that in central Pb–Pb collisions at sNN = 2.76 TeV the yields are suppressed by a factor of up to 7 for
pT = 6–7 GeV/c. For larger pT , the suppression decreases, but remains significant (a factor of about 2)
in the range of 30–150 GeV/c.
√
The first Pb–Pb collisions at sNN = 5.02 TeV were delivered by the LHC in 2015. Data in pp collisions
at the same energy were also collected by the LHC experiments, allowing for a direct comparison of
√
particle production in pp, p–Pb and Pb–Pb collisions. The first results on charged-particle RAA at sNN =
5.02 TeV have recently become available from the CMS Collaboration [11], showing that in central
Pb–Pb collisions charged-particle production is suppressed by a factor of 7–8 for pT = 6–9 GeV/c.
The suppression continues up to the highest pT measured and approaches unity in the vicinity of pT =
200 GeV/c.
Measurements of p–Pb collisions at the LHC were performed to establish whether the initial state of
the colliding nuclei plays a role in the observed suppression of high-pT hadron production in Pb–Pb
collisions. The RpPb was found to be consistent with unity for pT up to a few tens of GeV/c, indicating
that in this domain initial state effects do not influence particle production [12–15].
In this paper, we report the measurement of transverse momentum spectra of charged particles in pp
√
and Pb–Pb collisions at sNN = 5.02 TeV. The resulting pT spectra are used to determine the nuclear
modification factors in Pb–Pb collisions at the highest energy currently accessible at the LHC. The pT
spectrum measured in pp collisions at the same collision energy as p–Pb is also used as the reference
to calculate RpPb . These measurements allow us to compare the particle production in pp, p–Pb and
√
Pb–Pb collisions at the same sNN , for the first time with ALICE at the LHC. In addition, we report
√
a reanalysis of data collected in pp and Pb–Pb collisions at sNN = 2.76 TeV, and in p–Pb collisions
√
at sNN = 5.02 TeV. The reanalysis is warranted by significant improvements in track selection and
efficiency corrections, which benefit from the experience accumulated in the past years as well as better
knowledge of the particle production at the LHC energies. This leads to significantly-reduced systematic
2

## PDF page 3

Charged-particle spectra and nuclear modification factors

ALICE Collaboration

uncertainties by a factor of about 2 as compared to previously published results [8, 13, 16], which the
√
current analysis supersedes. The increase in sNN from 2.76 TeV to 5.02 TeV for Pb–Pb collisions leads
to ∼ 20% increase in the particle multiplicity [17] indicating that the larger medium density is reached
at the higher collision energy. We characterize this medium by comparing the pT spectra and nuclear
modification factors measured at the two energies.

2

Experiment and data analysis

√
√
The data in Pb–Pb and pp collisions at sNN = 2.76 TeV and in p–Pb collisions at sNN = 5.02 TeV
were collected with the ALICE apparatus [18] in 2010, 2011 and 2013, respectively. Details on the
ALICE experimental conditions and the detector performance are given in [19]. The data in Pb–Pb and
√
pp collisions at sNN = 5.02 TeV were recorded in 2015.
2.1

Trigger and event selection

The analysis is based on tracking information from the Inner Tracking System (ITS) [20] and the Time
Projection Chamber (TPC) [21], both are located in the central barrel of the experiment and embedded
in a solenoidal magnetic field of 0.5 T parallel to its axis.
The minimum-bias (MB) interaction trigger was based on signals from the forward scintillator arrays
(V0A and V0C) and the two innermost layers of the ITS, the Silicon Pixel Detector (SPD), in coincidence
√
with two beam bunches crossing in the ALICE interaction region. The pp collisions at s = 2.76 TeV
were selected requiring a signal in either one of the V0A or the V0C detectors or in the SPD. The Pb–Pb
√
collisions at sNN = 2.76 TeV were selected based on different combinations of hits in the SPD and
either V0A or V0C detector. The efficiency for hadronic interactions is approximately 100% in the 0–
80% centrality range considered in this analysis, see details in [19]. For measurements of pp, p–Pb and
√
Pb–Pb collisions at sNN = 5.02 TeV the trigger required a signal in both V0A and V0C detectors.
The offline event selection was optimized to reject beam-induced background in all collision systems.
The background events were efficiently rejected by exploiting the timing signals in the two V0 detectors.
In Pb-Pb collisions background was also rejected exploiting the correlation between the arrival times
measured in each neutron Zero Degree Calorimeter (ZDC), positioned on both sides of the interaction
√
point at 114.0 m for pp and Pb–Pb data at sNN = 2.76 TeV and at 112.5 m for the rest data sets.
The contamination from electromagnetic interactions in Pb–Pb collisions was strongly suppressed using
signals from the ZDCs (see [19] for details).
The primary event vertex is determined with tracks from the central barrel. For the analysis of pp collisions, if no vertex is found using tracks, the vertex reconstruction is performed using SPD tracklets; track
segments reconstructed based on the information from the two innermost layers of the ITS. To ensure
a uniform acceptance and reconstruction efficiency in the pseudorapidity region |η| < 0.8, only events
with a reconstructed vertex within ±10 cm from the center of the detector along the beam direction are
used. It corresponds to around 2 standard deviations from the mean of the interaction region distribution
(Gaussian shape) determined for all collisions systems and energies.
In Pb–Pb collisions, the centrality quantifies the fraction of the geometrical cross-section of the colliding
nuclei, and it is related to their geometrical overlap region. It is determined using the sum of the amplitudes of the V0A and V0C signals [22]. The analysis is limited to the 0–80% most central events, to
ensure that effects of trigger inefficiency and contamination by electromagnetic processes [23], as well
as possible biases in the selection of more peripheral events [24], are negligible. The average quantities
characterizing a centrality class, such as the mean number of participants ⟨Npart ⟩, the mean number of
binary collisions ⟨Ncoll ⟩ or the average nuclear overlap function ⟨TAA ⟩ were obtained [22] by fitting the
experimental distributions with a Glauber Monte Carlo model [3], coupled to the model of particle production with f · Npart + (1 − f ) · Ncoll particle sources, each source producing particles according to a Neg3

## PDF page 4

Charged-particle spectra and nuclear modification factors

collision system
pp
p–Pb
Pb–Pb (0–80%)

√
sNN = 2.76 TeV
52 M
13 M

ALICE Collaboration
√
sNN = 5.02 TeV
109 M
107 M
20 M

Table 1: Number of events used in the analysis for various systems and energies. The analysis of Pb–Pb events
was performed for the 0–80% centrality range.

ative Binomial Distribution (NBD). This approach is inspired by two-component models [25, 26], which
decompose nucleus-nucleus collisions into soft and hard interactions, where the soft interactions produce
particles with an average multiplicity proportional to Npart , and the probability for hard interactions to
occur is proportional to Ncoll . The fit parameter f represents the contribution of soft processes to the particle production and amounts to about 0.8 for the two energies. In this calculations, we used an inelastic
√
nucleon–nucleon cross-section σNN = (67.6 ± 0.6) mb for sNN = 5.02 TeV and σNN = (61.8 ± 0.9) mb
√
for sNN = 2.76 TeV, obtained by interpolation [3] of the existing world data.
In p–Pb collisions, the average quantities ⟨Npart ⟩, ⟨Ncoll ⟩ and ⟨TpPb ⟩ were determined [22] following the
procedure described in [27], with the updated inelastic nucleon–nucleon cross-section σNN = (67.6 ±
√
0.6) mb at sNN = 5.02 TeV and nuclear density function. In order to omit potential biases on the pT
spectra related to p–Pb collision centrality determination [27], only p–Pb events in the 0–100% centrality
interval were used in the presented analysis.
The number of events satisfying the trigger and offline selection criteria for various collision systems and
energies are listed in Table 1.
2.2

Track selection

Primary charged particles are measured in the kinematic range |η| < 0.8 and 0.15 < pT < 50 GeV/c.
A primary charged particle is defined [28] to be a charged particle with a mean proper lifetime τ larger
than 1 cm/c which is either produced directly in the interaction, or from decays of particles with τ
smaller than 1 cm/c, excluding particles produced in interactions with the detector material. The trackselection criteria were identical for all data sets and were optimized for best track quality and minimal
contamination from secondary particles. Each track is required to have:
– at least 2 hits in the ITS detector, of which at least one hit is in the two innermost (SPD) layers;
– the length L (in cm) of its projection curve calculated in the TPC readout plane, excluding the
information from the pads at the sector boundaries (∼ 3 cm from the sector edges), larger than
A − B · pCT , with A = 130 cm, B = 1.0 cm · (GeV/c)−C , C = −1.5 and pT in units of GeV/c;
– the number of crossed TPC pad rows larger than 0.85·L (the height of pad rows varies from 7.5 mm
to 15 mm [21]); a TPC readout pad row is considered crossed if there is a cluster in this row and
in any of its neighboring 2 rows;
– the number of TPC clusters (one cluster per pad row) larger than 0.7 · L;
– the ratio of crossed TPC pad rows to the number of findable TPC clusters (maximum number of
clusters which can be assigned to a track in the TPC fiducial volume, excluding the information
from the pads at the sector boundaries) larger than 0.8;
– the fraction of TPC clusters shared with another track lower than 0.4;
2 /N
2
– the fit quality for the ITS and TPC track points satisfying χITS
hits < 36 and χTPC /Nclusters < 4,
respectively;

4

## PDF page 5

Charged-particle spectra and nuclear modification factors

ALICE Collaboration

2
2
– χTPC−ITS
< 36, where χTPC−ITS
is calculated comparing the track parameters of the helix fit from
the combined ITS+TPC track reconstruction to that derived only from the TPC and constrained by
the interaction point, see details in [8];

– the distance of closest approach to the primary vertex in the transverse plane |DCAxy | < A + B · pCT ,
with A = 0.0182 cm, B = 0.035 cm · (GeV/c)−C , C = −1.0 and pT in units of GeV/c; and along
the beam axis |DCAz | < 2 cm.
2.3

Corrections

The data are presented as differential cross sections for inelastic (INEL) pp collisions
rec
d2 σ
1 d2 N
pp
pp N (∆η, ∆pT ) ·C(∆η, ∆pT )
· εVZ ,
= σMB · MB
≡ σMB ·
rec · ∆η∆p
dηdpT
Nev dηdpT
Nev
T

(2)

and transverse momentum spectra for non-single diffractive (NSD) p–Pb and centrality-selected INEL
Pb–Pb collisions
1 d2 N
N rec (∆η, ∆pT ) ·C(∆η, ∆pT )
· εMB · εVZ ,
(3)
≡
rec · ∆η∆p
Nev dηdpT
Nev
T
which are obtained by correcting the charged particle yields N rec reconstructed in the (∆η, ∆pT ) intervals
for all detector effects that either influence the event reconstruction, and thus are relevant only for the
overall normalization (event-level corrections), or influence the track reconstruction and are relevant for
both the spectral shape and normalization (track-level corrections). The εMB and εVZ denote the MB
trigger and event vertex reconstruction efficiencies, and C(∆η, ∆pT ) are track-level correction factors.
One should note that the εVZ is calculated for the triggered events. In general, both the εMB and εVZ are
multiplicity dependent. Details of the correction procedure and variables are described in the following.
2.3.1

Event-level corrections
pp

In Eq. 2 the minimum-bias cross section σMB in triggered pp collisions is determined by the van-der√
Meer scans and depends on the trigger settings, it was measured to be 55.4 ± 1.0 mb at s = 2.76 TeV
√
[29] and 51.2 ± 1.2 mb at s = 5.02 TeV [30], with the MB trigger OR (V0A or V0C or SPD) and AND
2
(V0A and V0C), respectively.
calculated for
( MB ) The differential charged-particle yields d N/dηdpT were
rec
the MB event class Nev by normalizing to the number of reconstructed events Nev , which have a
reconstructed event vertex within ±10 cm from of the center of the detector and correcting for the event
vertex reconstruction efficiency εVZ .
For INEL pp collisions, the εVZ was estimated using the PYTHIA 8 (Monash 2013 tune) event generator
[31, 32] and GEANT3 [33] detector response model. The resulting values εVZ = 88.3%(97.7%) at
√
s = 2.76 (5.02) TeV were used for corrections.
For NSD p–Pb collisions, the efficiency of the trigger (εMB ) and event vertex reconstruction (εVZ ), as
in Eq. 3, were estimated using GEANT3 detector simulation with a combination of event generators as
described in [12]. The obtained values εMB = 99.2% and εVZ = 98.6% were used for corrections.
For Pb–Pb collisions, the trigger and event vertex reconstruction is fully efficient for the centrality intervals considered in this work, as estimated using Monte Carlo simulations with GEANT3 and HIJING
[34] as event generator.
2.3.2

Track-level corrections

The differential charged-particle yields d2 N/dηdpT (Eqs 2 and 3) are obtained from the reconstructed
yields of tracks N rec (∆η, ∆pT ) corrected using correction factors C(∆η, ∆pT ), which are products of
acceptance, efficiency, purity and pT resolution.
5

## PDF page 6

1
ALICE pp s = 5.02 TeV |η| < 0.8
PYTHIA 8 (Monash-2013)

0.8

ALICE Collaboration

1

Relative abundance

Acceptance × efficiency

Charged-particle spectra and nuclear modification factors

10− 1

π+ +π-

0.6

p+p

+

-

Σ + +Σ

-

K +K

-

Σ +Σ

+

10− 2

Rest

ALICE pp |η| < 0.8
Open: PYTHIA 8 (Monash-2013)
s = 5.02 TeV
Full: Data+extrap., s = 7 TeV
π+ +πp+p
+
K +K
+
Σ +Σ (derived from Λ)
Σ + +Σ (derived from Λ)
Rest, PYTHIA 8

All

0.4

−3

10
0.2

10− 4
0
1

10

1
p (GeV/c )

10
p (GeV/c )

T

T

Figure 1: Left: Combined tracking efficiency and acceptance as a function of pT for different particle species
√
and the sum of all, obtained in Monte Carlo simulations of pp collisions at s = 5.02 TeV with PYTHIA 8
(Monash 2013 tune). For pT > 1 GeV/c parameterizations are shown. The relative systematic uncertainties on
parameterizations are small (< 0.2%) and are not shown. The statistical uncertainties for pT < 1 GeV/c are smaller
than the symbol size (< 0.5%). Right: The relative particle abundances as a function of pT in Monte Carlo (open
√
√
symbols, for s = 5.02 TeV) and in data (full symbols, for s = 7 TeV) [35–37]. The data are extrapolated beyond
the range of the measurements (see description in the text). The statistical and systematic uncertainties (combined
< 1.6%) are not shown.

The efficiency and purity of the primary charged particle reconstruction as well as acceptance correction
for the pp, p–Pb and Pb–Pb data are calculated using Monte Carlo event generators with GEANT3
detector modeling combined with data-driven corrections, which are discussed in detail in the following
sections.
Tracking efficiency The efficiency of the primary charged particle reconstruction is shown in Fig. 1
(left). While the low efficiency at low pT is related to the strong track curvature caused by the magnetic
field and to the energy loss in the detector material, the characteristic shape around pT of 1 GeV/c is
caused primarily by the track length requirement. Tracks in this momentum range are more likely to
cross the TPC sector boundaries and are thus reconstructed with lower efficiencies. The asymptotic
value reached at high pT reflects the acceptance limitations (detector boundaries and active channels) of
the measurement.
The tracking efficiency depends on particle species, as can be seen in Fig. 1 (left), and was calculated
using a detector simulation with the PYTHIA 8 (Monash 2013 tune) event generator and the GEANT3
transport code. The efficiency is particularly species-dependent at low pT (below 0.5 GeV/c) due to
differences in ionization energy loss in the detector material, hadronic interaction cross-section or decay
probability.
A particular case is that of charged hyperons, for which the reconstruction efficiency is very low and
essentially negligible below 10 GeV/c, due to the fact that they decay before any significant interaction
with the detector. For higher pT , they reach the detector and can be observed with increasing efficiency.
One should note that the reconstruction efficiency is different for the Σ+ and Σ− hyperons in the pT
range considered, because of their different lifetimes. The tracking efficiency for other primary charged
particle species, including electrons, muons and Ξ and Ω hyperons (denoted as ”Rest”) is also shown.

6

## PDF page 7

Charged-particle spectra and nuclear modification factors

ALICE Collaboration

In order to reduce statistical fluctuations at high pT , we parameterized the efficiency above pT = 1 GeV/c
for each particle species. Each parameterization is a combination of the universal (independent of particle
species) function f (pT ) = a (1 − b · e−cpT ) and the survival probability P(pT ) = e−d·m/pT ·τ that a particle
with the mass m and a mean proper lifetime τ survives a minimal distance d before decaying. The
fitting parameters (a, b and c) are determined from the fit to the efficiency calculated as an average of
efficiencies for stable particles. The calculations were performed for d = 200 cm, corresponding to the
minimum track length in the ITS and the TPC required in the analysis.

Contamination with secondary particles

Acceptance × efficiency

The parametrized efficiencies shown in Fig. 1 (left) were used to determine data-driven correction factors
in the efficiency rewieghting procedure, which is discussed below.

ALICE s NN = 5.02 TeV
charged particles | η | < 0.8

1

0.9

0.8

0.7

0.6

0.2

ALICE s NN = 5.02 TeV charged particles | η | < 0.8

0.1

Pb-Pb 0-5% HIJING
Full: Reweighted | Open: MC

0

0.2

1

10

Pb-Pb 70-80% HIJING

p T (GeV/ c )

0.1
0
0.2

1

10 p (GeV/ c )

p-Pb NSD -0.3< η cms< 1.3 DPMJET

T

0.1
0

Reweighted / MC

0.4

1.1

Pb-Pb
0-5% HIJING (+ 0.3)
Pb-Pb
70-80% HIJING (+ 0.2)
p-Pb NSD -0.3< η cms< 1.3 DPMJET (+ 0.1)
pp
PYTHIA 8 (Monash-2013)
Full: Reweighted | Open: MC

1

0.2

10

1

p T (GeV/ c )

0.9
1

10 p (GeV/ c )
T

0.1

1.05
0.95

1

pp PYTHIA 8 (Monash-2013)

Reweighted / MC

0.5

10

0
1

10 p (GeV/ c )
T

1.6
1.4
1.2
1

10

p T (GeV/ c )

p T (GeV/ c )

Figure 2: Left: Combined tracking efficiency and acceptance as a function of pT for pp, p–Pb, central (0-5%)
and peripheral (70–80%) Pb–Pb collisions determined using Monte Carlo simulations and a reweighting method
(see text for details). For better visibility, the curves for p–Pb and Pb–Pb are offset by the indicated values. The
effect of the reweighting on the efficiency corrections is shown in the bottom panel. The systematic uncertainties
of the reweighting (< 2.4%) are not shown. Right: Contamination from secondary particles estimated from Monte
Carlo simulations and from the impact parameter fits in data (see text for details). The effect of the reweighting of
secondary particles is shown in the bottom panel. The systematic uncertainties on the scaling factors (< 20%) are
not shown.

Reweighting with measured particle composition The experimental knowledge of the primary particle composition has significantly improved recently at the LHC [35–44], which allows for a precise
determination of the tracking efficiency. For the first time, we determined the tracking efficiency by
reweighting the primary particle composition based on data driven method.
In the right panel of Fig. 1, the relative particle abundances measured by ALICE in pp collisions at
√
s = 7 TeV are compared to those from Monte Carlo simulations with the PYTHIA 8 (Monash 2013
√
tune) event generator for s = 5.02 TeV. Charged pions, kaons and protons were measured from pT
7

## PDF page 8

Charged-particle spectra and nuclear modification factors

ALICE Collaboration

= 0.15, 0.2, and 0.3 GeV/c to 20 GeV/c [35, 36], respectively. It is known that Monte Carlo event
generators underestimate hyperon production substantially [38, 39]. In particular, the Σ+ (1385) and
Σ− (1385) hyperons and their antiparticles are underestimated by a factor of 2–3 in the recent PYTHIA
8 tunes. The pT spectra of Σ± hyperons have not been measured. Therefore, the pT spectra of Σ± are
approximated using the measured spectrum of Λ hyperons [37] scaled by the ratio of Σ± to Λ hyperons
from the Monte Carlo generator.
√
Relative particle abundances measured in pp collisions at s = 7 TeV are used to reweight the track√
ing efficiency determined for s = 2.76 and 5.02 TeV collision energies, based on the experimental
knowledge that their energy dependence is weak [37]. The relative abundance of other particle species
containing electrons, muons and Ξ and Ω hyperons (denoted “Rest” in Fig. 1) is taken from simulations
without further modification and has only a small influence on the final result (< 1%). The measured
pT spectra of kaons, protons and Λ are extrapolated down to pT = 0.15 GeV/c using a parameterization proposed by Bylinkin and Rostovtsev [45]. For high pT , beyond the reach of the identified particle
measurement, the relative abundances are assumed to be independent of pT , as motivated by pQCD [46].
The reweighting of the efficiency has also been applied in the analysis of p–Pb and Pb–Pb data. The relative particle abundances obtained from Monte Carlo simulations with DPMJET (p–Pb) [47] and HIJING
(Pb–Pb) event generators are reweighted using ALICE measurements of identified particle species (pi√
ons, kaons, protons and Λ hyperons) for p–Pb collisions at sNN = 5 TeV [36, 40] and Pb–Pb collisions
√
at sNN = 2.76 TeV [41–44]. The relative particle abundances at low pT are determined by extrapolating
the measured pT spectra of kaons, protons and Λ hyperons down to pT = 0.15 GeV/c using a blast-wave
parameterization [48]. As in the pp case, for pT beyond the reach of these measurements, the relative
abundances are assumed to be independent of pT .
In the left panel of Fig. 2 the combined tracking efficiency and acceptance obtained from MC simulations
(open symbols) and after reweighting (full symbols) is shown as a function of pT for pp, p–Pb, and
central (0-5%) and peripheral (70-80%) Pb–Pb collisions. The effect of the reweighting on the efficiency
corrections is shown in the bottom panel. It amounts to a difference of about 7% at pT around 3 GeV/c
for the most central Pb–Pb collisions, and is lower in peripheral Pb–Pb collisions, p–Pb and pp collisions.
When comparing central to peripheral Pb–Pb collisions, the importance of an increasing radial flow that
shifts the heavy Σ± baryons to larger momenta becomes apparent.
Purity The contribution from secondary particles, i.e. products of weak decays of kaons, Λ hyperons
and muons, and particles arising from interactions in the detector material, was estimated using the
transverse impact parameter dxy distributions of particles in data and Monte Carlo simulations. Exploiting
the differences, especially in the tails, of the dxy distributions between primary and secondary particles,
the measured distributions were fitted by a linear combination of dxy distributions (templates) for primary
and secondary particles obtained from the Monte Carlo simulations in different pT bins (as described in
more detail in [41]). The effect of this data-driven correction, shown in the bottom panel of Fig. 2 (right),
depends on pT and is different for pp, p–Pb and Pb–Pb collisions. The resulting contamination with
secondary particles, i.e. the fraction of secondary particles in the sample of selected particles, ranges
from 8.5% in pp to 20% in central Pb–Pb collisions at pT = 0.15 GeV/c and decreases to around 1.0%
for pT > 5 GeV/c, as shown in the upper panel of Fig. 2 (right).
Transverse momentum resolution The transverse momentum of charged particles is reconstructed
from the track curvature measured in the ITS and the TPC (see [19] for details). The modification
of the spectra arising from the finite momentum resolution is estimated from the error obtained from
the corresponding covariance matrix element of the Kalman fit. The relative pT resolution, σ (pT )/pT ,
depends on momentum and is approximately 3–4% at pT = 0.15 GeV/c, has a minimum of 1.0% at
pT = 1.0 GeV/c, and increases linearly for larger pT , approaching 3–10% at 50 GeV/c, depending on
collision energy, system or Pb–Pb centrality interval. The pT resolution has been verified by studying the
8

## PDF page 9

Charged-particle spectra and nuclear modification factors

Source of Uncertainty
Event selection
Track selection
Secondary particles
Particle composition
Matching efficiency
Trigger and vertex selection
pT resolution
Interaction rate
Material budget
Acceptance
Combined Uncertainty
Normalization
Centrality

pp
2.76 TeV
0.9
0.4–3.8
0.5–5.1
0.1–1.6
1.0–4.0
0.0–0.5
0.0–3.0
–
0.1–0.9
–
3.5–6.2
1.9
–

5.02 TeV
0.5
0.6–3.5
0.0–2.8
0.2–2.4
0.0–1.1
0.0–1.2
0.0–1.4
0.0
0.1–0.9
–
1.3–4.3
2.3
–

ALICE Collaboration

p–Pb
5.02 TeV
0.1
0.6–3.8
0.0–2.1
0.4–2.2
0.3–3.2
–
0.0–3.0
–
0.1–0.9
0.0–0.2
1.7–5.1
3.1
–

Pb–Pb
2.76 TeV 5.02 TeV
1.5
0.14
1.0–2.0
0.6–4.9
0.0–4.0
0.0–4.5
0.0–2.0
0.2–2.0
0.2–2.0
0.2–1.2
–
–
0.0–2.7
0.0–1.0
–
1.0
0.1–0.9
0.1–0.9
–
–
1.9–5.2
1.0–7.5
–
–
0.1–3.6
0.1–3.5

Table 2: Contributions to the relative systematic uncertainty for pT spectra in pp, p–Pb, and Pb–Pb collisions. The
ranges correspond to the maximal variation within the considered pT range of 0.15–50 GeV/c, as well as Pb–Pb
centrality intervals. The pT -dependent contributions are assumed to be independent and are summed in quadrature,
resulting in the combined uncertainty. All values are in %.

widths of the invariant mass distributions of Ks0 reconstructed from their decays to two charged pions.
To account for the finite pT resolution, correction factors to the spectra were determined based on the
Bayesian unfolding approach [49] implemented in the RooUnfold package [50]. This unfolding is
based on the response matrix, Rdet
m,t , which relates the measured spectrum Mm and the true spectrum
Tt , Mm = Rdet
·
T
,
where
m
and
t
are indices indicating the bin number. The response matrix was genert
m,t
ated for each data set and Pb–Pb collision centrality using GEANT3 detector simulations with different
Monte-Carlo generators. For pT > 10 GeV/c, another unfolding procedure similar to what was done in
previous work [16] was also used.
The correction factors depend on the collision energy and system as well as on the collision centrality, due
the change of the spectral shape. For momenta below 10 GeV/c, the corrections are significant only in
√
the first momentum bin pT = 0.15–0.2 GeV/c, and reach 3%(2.5%) for pp(Pb–Pb) at sNN = 2.76 TeV,
√
√
3% for p–Pb at sNN = 5.02 TeV and around 1% for pp(Pb–Pb) at sNN = 5.02 TeV. At low pT , these
corrections are independent of Pb–Pb collision centrality. For pT > 10 GeV/c, both unfolding methods
√
yield almost identical correction factors. For sNN = 5.02 TeV, the correction factors reach 5%, 1.5% and
3% (4%) at pT = 50 GeV/c for pp, p–Pb and 0-5%(70–80%) central Pb–Pb collisions, respectively. For
√
sNN = 2.76 TeV, they amount to 4% for pp and 4% (8%) for 0-5%(70–80%) central Pb–Pb collisions
at the highest pT . The resulting pT -dependent correction factors are applied (bin-by-bin) to the measured
pT spectra.
Trigger and vertex selection The event selection (trigger and vertex) introduces a small pT -dependence
in the correction on the pT spectra in pp collisions. This is due to the fact that the low-multiplicity pp
events, which are also characterized by a softer spectrum, are mostly rejected by the trigger and vertex
selection criteria. The effect on the pT spectra was calculated from simulations with the PYTHIA 8
(Monash 2013 tune) and the PYTHIA 6 (Perugia2011 tune) event generators and was estimated to be
√
around 0.4–0.6% (2.2–2.6%) for pT < 1 GeV/c at s = 2.76 (5.02) TeV. The spectra are corrected by the
average bias of these two generators, resulting in 0.5% (2.4%) corrections to the spectra.
Acceptance correction for the p–Pb data The two-in-one magnet design of the LHC imposes the
same magnetic rigidity of the beams in the two rings. The configuration for p–Pb collisions with pro9

## PDF page 10

Charged-particle spectra and nuclear modification factors

ALICE Collaboration

tons at 4 TeV energy colliding with 208
82 Pb ions at 82×4 TeV results in a shift in the rapidity of the
nucleon–nucleon center-of-mass system by ∆yNN = 0.465 in the direction of the proton beam (negative
z-direction). Therefore the detector coverage |ηlab | < 0.8 corresponds to roughly −0.3 < ηcms < 1.3. For
massless or high pT particles, ηcms = ηlab + yNN but the differential yield of non-massless particles at low
pT suffers from a distortion, which is estimated and corrected for based on the HIJING event generator
weighted by the measured relative particle abundances [36, 40]. For pT = 0.5 GeV/c the correction is 2%
for −0.3 < ηcms < 1.3.
2.4

Systematic uncertainty

The relative systematic uncertainties on the pT spectra are summarized in Table 2.
– The effect of the selection of events based on the vertex position is studied by comparing the fully
corrected pT spectra obtained with alternative vertex selections corresponding to ±5 and ±20 cm.
– The systematic uncertainties related to the track selection criteria (listed above) were studied by
varying the track quality cuts. In particular, we varied the upper limits of the track fit quality
2 /N ) and the TPC (χ 2 /N
parameters in the ITS (χITS
hits
clusters ) in the ranges of 25–49 and 3–5,
TPC
respectively. The systematic uncertainties related to high-pT fake tracks [8] were estimated by
2
modifying the upper limits of the track matching criteria given by the χTPC−ITS
in the range of
25–49. The resulting uncertainty dominates at high pT for all collision systems.
– The systematic uncertainty on the secondary-particle contamination (Fig. 2, right) includes contributions from the template fits to the measured impact parameter distributions. We have varied the
fit model using templates with two (primaries, secondaries) or three (primaries, secondaries from
material, secondaries from weak decays of Ks0 and Λ) components, as well as the fit ranges. The
maximum difference between the data and the 2 component-template fit is summed in quadrature
with the difference between results obtained from the 2 and the 3 component-template fits and
result is assigned as the systematic uncertainty on the contamination. This contribution dominates
for the lowest pT independently of the collision system.
– The systematic uncertainty on the primary particle composition consists of several contributions,
including the extrapolation of the spectra to low pT , the approximation of the relative particle
abundances at high pT , the efficiency parameterization at high pT , the uncertainties of the measured particle spectra and the MC assumptions on the Σ± /Λ spectra ratios. For the extrapolation to
low pT , we have studied different parameterizations (Bylinkin and Rostovtsev, modified Hagedorn
[51], Blast-Wave) and fit ranges. We have varied the pT thresholds for the approximation of the
relative particle abundances as well as the efficiency parameterization at high pT . The measured
particle spectra were varied within systematic uncertainties (one particle species at a time), and the
resulting differences to the nominal spectra were added in quadrature to the systematic uncertainties. We have also assigned an additional uncertainty related to the different spectral shape of Σ±
and Λ from the MC generators.
– To account for the imperfect description of the experimental setup in simulations, we compared
the track matching between the TPC and the ITS information in data and Monte Carlo after scaling
of the fraction of secondary particles obtained from the fits to the dxy distributions. After rescaling
the fraction of secondary particles, the agreement between data and Monte Carlo is within 4%.
This value is assigned as an additional systematic uncertainty.
– The systematic uncertainty on the pT resolution at low pT (only first pT bin) was estimated by
changing Monte-Carlo generators in the unfolding procedure. The pp collisions were simulated
with PYTHIA and PHOJET, p–Pb collisions with HIJING and DPMJET, and Pb–Pb collisions

10

## PDF page 11

Charged-particle spectra and nuclear modification factors

ALICE Collaboration

with HIJING and AMPT [52]. The average correction factor of two generators was assigned as
systematic uncertainty. At low pT , we observe a weak dependence of correction factors on the
considered Monte-Carlo generators. The resulting uncertainties amount to 3%(2.5%) for pp(Pb–
√
√
Pb) collisions at sNN = 2.76 TeV, to 3% for p–Pb collisions at sNN = 5.02 TeV, and to 1% for
√
pp and Pb–Pb collisions at sNN = 5.02 TeV. The systematic uncertainty on the pT resolution at
high pT (> 10 GeV/c) was estimated using the azimuthal angle dependence of the 1/pT spectra for
positively and negatively charged particles. The relative shift of the spectra for oppositely charged
particles along 1/pT determines the size of uncertainty for a given angle. We used the RMS of the
1/pT shift distribution for the full azimuth as additional smearing of the pT resolution. We checked
that these shifts are due to detector effects (such as E × B effect) and are not related to the physics
of hadronic interaction in GEANT3. To take into account the decrease in the pT resolution with
increasing interaction rate, we have studied the systematic uncertainty for the pp and Pb–Pb data
√
sets at sNN = 5.02 TeV, obtained from the difference of the spectra at high and low interaction
rate. The uncertainty is negligible for pp collisions, and is about 1% for Pb–Pb collisions.
– For the correction due to the trigger and vertex selection, calculated as the average bias of two
generators, half of the value is assigned as systematic uncertainty.
– The systematic uncertainty for the acceptance correction on the p–Pb data was estimated by varying the relative particle abundances within their measured uncertainties and by changing the fit
function for the low-pT extrapolation. The uncertainty is sizable only at low pT where it reaches
0.2%.
– The material budget in the simulation was varied by ±4.5% [19], resulting in the systematic uncertainty in the range of 0.1–0.9%.
– The normalization uncertainty on the spectra in pp collisions was propagated from the cross section
measurements.
– The systematic uncertainties related to centrality selection were estimated by a comparison of the
pT spectra when the limits of the centrality classes are shifted due to an uncertainty of ± 0.5%
in the fraction of the hadronic cross section used in the analysis and by a comparison of results
obtained using the SPD detector to estimate centrality as opposed to the V0A and V0C.
For the evaluation of the total systematic uncertainty all contributions are considered to be uncorrelated
and they are summed in quadrature. The improved reconstruction and track selection in the reanalysis of
√
√
pp and Pb–Pb data at sNN = 2.76 TeV and p–Pb data at sNN = 5.02 TeV lead to significantly reduced
systematic uncertainties by a factor of about 2 as compared to previously published results [8, 13, 16].

3

Results and discussion

3.1

Spectra

The fully corrected pT spectra of primary charged particles measured in INEL pp and Pb–Pb collisions
√
√
at sNN = 2.76 TeV and 5.02 TeV and in NSD p–Pb collisions at sNN = 5.02 are shown in Fig. 3.
The Pb–Pb spectra are presented in nine centrality classes. For pp collisions, the pT -differential cross
√
sections are divided by the corresponding inelastic nucleon-nucleon cross section at s = 2.76 (61.8 mb)
and 5.02 TeV (67.6 mb) [3], respectively. The relative systematic uncertainties for the various datasets
are shown in the bottom panels. Substantial improvements in track selection and efficiency corrections
√
have been achieved. However the uncertainty on the pp data at sNN = 2.76 TeV is still larger than for
√
the data at sNN = 5.02 TeV due to larger number of inactive channels in the SPD [19], which affects
the track reconstruction and the determination of the secondary particle contribution.
11

## PDF page 12

1012

ALICE, charged particles
s NN = 2.76 TeV, | η | < 0.8

10

10

108
106
104

1/N ev d2N /dp Tdη (GeV-1c )

1/N ev d2N /dp Tdη (GeV-1c )

Charged-particle spectra and nuclear modification factors

1012

10−4

Syst. Unc. (%)

10−6
10−8

6

s NN = 5.02 TeV, | η | < 0.8

108
106
104
102
1

Pb-Pb
9
0-5%
× 10
5-10% × 108
7
10-20% × 10
20-30% × 106
30-40% × 105
40-50% × 104
50-60% × 103
60-70% × 102
70-80% × 10
pp INEL

pp

Pb-Pb
1 0-5%

10−2
10−4
10−6

Syst. Unc. (%)

10−2

ALICE, charged particles

10

10

102
1

ALICE Collaboration

Pb-Pb 10
70-80%

4
2

p T (GeV/ c )

0
1

10

10−8

6

Pb-Pb
0-5%
× 109
5-10% × 108
10-20% × 1076
20-30% × 105
30-40% × 104
40-50% × 103
50-60% × 10
60-70% × 102
70-80% × 10
p-Pb NSD -0.3 < η cms < 1.3
pp INEL

pp

Pb-Pb10-5%

p-Pb

4
2

p T (GeV/ c )

0
1

p T (GeV/ c )

Pb-Pb 70-80%
10

10

p T (GeV/ c )

Figure 3: Transverse momentum distributions of primary charged particles in |η| < 0.8 in nine centrality intervals
√
in Pb–Pb collisions at sNN = 2.76 (left) and 5.02 TeV (right) (scale factors as indicated are used for better visibilNN , and NSD p–Pb at √s
ity). The data for pp collisions, obtained scaling the cross section by σinel
NN = 5.02 TeV
are also shown. The relative systematic uncertainties are shown in the lower panels for various datasets; these do
not contain the normalization uncertainty.

In Pb–Pb collisions the shape of the pT spectrum varies strongly with collision centrality. For peripheral
collisions, the spectral shape is similar to that measured in pp collisions as well as to the spectrum in
p–Pb collisions. With increasing collision centrality, a marked depletion of the Pb–Pb spectra develops
for pT > 5 GeV/c. These measurements supersede our previous results [8, 13, 16], which allows for a
better discrimination between jet quenching scenarios.
Figure 4 compares the measured pT spectra in pp collisions with results from PYTHIA 8 (Monash-2013
tune), including colour reconnection, and EPOS LHC [53], which incorporates collective (flow-like)
effects. These event generators show a similar description of the pT spectra at both energies. They
reproduce the spectral shape within 20%.
√
√
Figure 5 shows the ratios of pT spectra measured at sNN = 5.02 and sNN = 2.76 TeV in Pb–Pb and pp
collisions. The ratios for Pb–Pb collisions are determined in nine centrality classes ranging from 0–5%
(top-left) to the 70–80% (bottom-right). As indicated by the ratios, the pT spectra measured at higher
collision energy are significantly harder for both Pb–Pb and pp collision systems. One can see that there
is a similar energy dependence of the ratio for peripheral (70–80%) Pb–Pb and in pp collisions, while
towards central Pb–Pb collisions a gradual reduction of the ratio is apparent.
3.2

Nuclear modification factors

In order to quantify in-medium modification of charged-particle transverse momentum spectrum, the
nuclear modification factors are determined. Figure 6 shows the RAA for Pb–Pb collisions measured at
12

## PDF page 13

Charged-particle spectra and nuclear modification factors

Data / MC

1.5

ALICE Collaboration

ALICE pp, INEL, charged particles, | η | < 0.8
EPOS LHC
PYTHIA 8 (Monash-2013)

1
s = 2.76 TeV
Norm. ± 1.9%

Data / MC

1.5

1

10

Data+Model stat. uncert.
Data syst. uncert.

p (GeV/c )
T

1
s = 5.02 TeV
Norm. ± 2.3%

1

10

p (GeV/c )
T

Figure 4: Comparison of the charged-particle transverse momentum spectra measured in pp collisions to PYTHIA
√
8 (Monash-2013 tune) [31, 32] and EPOS [53] model calculations at s = 2.76 (top) and 5.02 TeV (bottom). The
statistical uncertainties of the data and model calculations are added in quadrature. The boxes represent systematic
uncertainties of the data.

√
sNN = 2.76 and 5.02 TeV. The nuclear modification factor has a strong centrality dependence, and is
very similar in magnitude for the two collision energies.
√
Given that the pT spectra are harder at the higher sNN (see Fig. 5) and that the medium density in√
creases with sNN by ∼ 20% [17], this similarity of the RAA may indicate a larger parton energy loss
in the hotter/denser and longer-lived deconfined medium produced at the higher center-of-mass energy.
Assuming that the initial parton pT spectrum, parton distribution and fragmentation functions are not
significantly modified by the energy increase, and that the parton energy loss in expanding medium is
√
sublinear to the medium density increase, we would expect larger energy loss at sNN = 5.02 TeV than
√
at sNN = 2.76 TeV, but no more than 20%.
In 0–5% central collisions the yield is suppressed by a factor of about 8 (RAA ≈ 0.13) at pT = 6–7 GeV/c.
Above pT = 7 GeV/c, there is a significant rise of the nuclear modification factor, which reaches a value
of about 0.4 for our highest pT bin, 30–50 GeV/c. In peripheral collisions (70–80%), the suppression
is 30% for intermediate momenta and approaches unity for the highest pT bin. The normalization uncertainties for RAA originate from the pp measurement and centrality determination and were added in
quadrature.
Figure 7 (left) shows the RpPb factor compared to RAA measured in the 0–5% and 70–80% centrality
√
classes for Pb–Pb collisions at sNN = 5.02. The RpPb factor exhibits a maximum for the intermediate pT
range, 2 < pT < 6 GeV/c, a feature generically called the Cronin effect [54]. A study on its dependence
on the particle species [40] suggested that protons are responsible for the observed maximum. The
maximum occurs at values of pT (3–5 GeV/c) larger than the maximum of RAA seen in the pT range
13

## PDF page 14

Charged-particle spectra and nuclear modification factors

Ratio of spectra (5.02 TeV / 2.76 TeV)

0-5%
Pb-Pb
3 pp INEL
(Norm. ± 3%)

5-10%
ALICE
charged particles
| η | < 0.8
3

ALICE Collaboration

3.5

3.5

3.5

2.5

2.5

2.5

3

2

2

2

1.5

1.5

1.5

Norm. ± 0.08%

1

3

10
3.5
p (GeV/
c)
T
3

2.5

2.5

3.5

Norm. ± 0.24%

1

20-30%1

30-40%1

10
3.5
p (GeV/
c)
T
3

40-50%1

2

2

1.5

1.5

Norm. ± 0.81%

Norm. ± 1.26%

T

1

Norm. ± 1.86%

1

10 c ) 60-70%1
p (GeV/
3.5
T

70-80%1
p 10
(GeV/
c)
3.5
T

3

3

3

2.5

2.5

2.5

2

2

2

3.5

1.5
1

1.5

1.5

Norm. ± 2.64%

Norm. ± 3.67%

1

1

10
p (GeV/c )
T

10
p (GeV/c )

2.5

2

50-60%1

Norm. ± 0.46%

1

1.5
1

10-20%

1

T

T

Norm. ± 5.01%

1

10
p (GeV/c )

10 c )
p (GeV/

1

10
p (GeV/c )
T

√
√
Figure 5: Ratio of transverse momentum spectra at sNN = 5.02 and sNN = 2.76 TeV for Pb–Pb collisions, for
nine centrality classes, and in pp collisions (repeated in each panel). The relative normalization uncertainties due to
the centrality determination are indicated for each centrality class. For the pp spectrum, the relative normalization
uncertainty is ±3%.

1.5–3 GeV/c. The RpPb factor is consistent with unity for pT ≳ 8 GeV/c, demonstrating that the strong
suppression observed in central Pb–Pb collisions is not related to initial state effects but rather to the
√
formation of hot and dense QCD matter. The ALICE results for RAA and RpPb measured at sNN =
5.02 TeV are compared to measurements by CMS [14] in Fig. 7 (right). Agreement within 1.5σ is
observed for both RAA and RpPb taking into account the current uncertainties.
3.3

Comparison with theoretical models

√
In Fig. 8 the measured RAA for 0-5% central collisions at sNN = 5.02 TeV is compared to model
predictions. All presented models are based on the pQCD factorization, where the entire effect of energy
loss is encoded in the medium-modified parton fragmentation function. All models include radiative
energy loss based on different approaches. The model by Djordjevic et al. [57, 58] and CUJET 3.0 [60,
61] include in addition collisional energy loss. The energy loss is calculated in dynamically expanding
medium in all models except that of Vitev et al. [55, 56], in which the medium is composed of static
scattering centers. In the following, the models are discussed in more detail.
The calculations by Vitev et al. are based on the SCETG model [55, 56], which uses an extended softcollinear effective theory to describe inclusive particle production and suppression in the heavy-ion environment. This theoretical framework provides an analytic connection between generalized DGLAP
evolution equations for the fragmentation functions in dense strongly-interacting matter and parton energy loss for hard processes. The calculations employ the pQCD-based hard cross section and QGP
medium evolved parton-to-hadron fragmentation functions, combined with initial-state cold nuclear mat-

14

## PDF page 15

R PbPb

Charged-particle spectra and nuclear modification factors

Norm.

1

0.8

1
sNN = 5.02 TeV

0.8

sNN = 2.76 TeV

ALICE
charged particles
| η | < 0.8

ALICE Collaboration

1
0.8

0.6

0.6

0.6

0.4

0.4

0.4

0.2

0-5% 0.2

5-10%0.2

1

0 10 20 30 40 50 0 10 20 30 40 50 0 10 20 30 40 50
p (GeV/c1)
p (GeV/c1)
p (GeV/c )
T

T

T

0.8

0.8

0.8

0.6

0.6

0.6

0.4

0.4

0.4

0.2

0.2
20-30%

0.2
30-40%

1

10-20%

40-50%

0 10 20 30 40 50 0 10 20 30 40 50 0 10 20 30 40 50
p (GeV/c )
p (GeV/c )
p (GeV/c )
T
T
T
1
1

0.8

0.8

0.8

0.6

0.6

0.6

0.4

0.4

0.4

0.2

0.2
50-60%

0.2
60-70%

70-80%

0 10 20 30 40 50 0 10 20 30 40 50 0 10 20 30 40 50
p (GeV/c )
p (GeV/c )
p (GeV/c )
T

T

T

Figure 6: The transverse momentum dependence of the nuclear modification factor measured in Pb–Pb collisions,
√
for nine centrality classes. The new data at sNN = 5.02 (full symbols) are compared to the reanalyzed data at
√
sNN = 2.76 TeV (open symbols). The normalization uncertainties are shown as boxes around unity.

ter (CNM) effects, which include dynamical nuclear shadowing, the Cronin effect and initial-state parton
energy loss (see [56] and references therein for details). The two upper and lower curves represent calculations for the nuclear modification factor with variations of the coupling strength g = 1.9 ± 0.1 between
the jet and the medium, which is a free parameter in the calculations. Djordjevic et al. [57, 58] use a
dynamical energy loss formalism based on pQCD calculations in a finite size dynamical QCD medium.
While the initial pT spectrum is the same as that used in the SCETG model, the dynamical description
of the medium provides a consistent treatment of both radiative and collisional energy loss, including
a finite magnetic screening mass, which modifies the gluon self energy and therefore changes the energy loss, as well as a running coupling constant for the strongly-interacting medium. The two curves
correspond to different electric-to-magnetic screening mass ratios in the range 0.4 < µM /µE < 0.6. The
model of Bianchi et al. [59] uses the pQCD factorization scheme with a pQCD-based radiative energy
loss in a hydrodynamically expanding medium. In this framework, high pT hadrons arise from fragmentation of hard partons, which lose energy prior to hadronization via interactions with the medium.
The amount of energy loss is regulated by the medium transport coefficient q̂, which varies with the
temperature-dependent entropy density of the medium as well as with the energy scale of jets propagating in the medium. The CUJET 3.0 model [60, 61] is an extension of the perturbative-QCD-based
CUJET 2.0 model, with the two complementary non-perturbative features of the QCD cross-over phase
transition: the suppression of quark and gluon degrees of freedom and the emergence of chromomagnetic monopoles. The calculations were performed varying the value of the QCD running coupling αc
from 0.95 to 1.33 for Q < TC , and the ratio of electric to magnetic screening scales cm = gs µE /µM
(cm = 0, 0.3, 0.4), where gs is the strong coupling constant. The value of αc was fixed for each cm value
by fitting a single reference datum, RAA (pT = 12 GeV/c) ≈ 0.3, for charged hadrons in 20–30% central
15

## PDF page 16

R PbPb, R pPb

R PbPb, R pPb

Charged-particle spectra and nuclear modification factors

ALICE sNN = 5.02 TeV
charged particles | η | < 0.8

1.2
Norm.

1

ALICE Collaboration

1.4
1.2

sNN = 5.02 TeV, charged particles
Pb-Pb,0-5%
p-Pb
ALICE
ALICE
CMS
CMS
Norm.

1
0.8
0.8
0.6
0.6
0.4

0.4

0.2
0

Pb-Pb,0-5%
Pb-Pb,70-80%
p-Pb NSD -0.3 < η cms< 1.3

0

10

20

30

0.2
ALICE | η | < 0.8 (p-Pb -0.3 < η cms< 1.3), CMS | η | < 1.0

0

40
50
p (GeV/c )

1

T

10

102
p (GeV/c )
T

Figure 7: Left: Nuclear modification factors measured by ALICE in central (0–5%) and peripheral (70–80%)
√
Pb–Pb collisions and in p–Pb collisions at sNN = 5.02 TeV. Right: A comparison of the nuclear modification
factors for central (0-5%) Pb–Pb and p–Pb collisions measured by ALICE and CMS [11, 14]. In both figures, the
pT -dependent systematic uncertainties are shown as boxes around data points. The normalization uncertainties are
shown as boxes around unity.

Pb–Pb collisions at the LHC. The calculations by Andrés et al. [62] use the jet quenching formalism of
quenching weights. This approach consists of fitting a K factor, defined as K ≡ q̂/2ε 3/4 , that quantifies
departure of this parameter from the perturbative estimate, q̂ideal ∼ 2ε 3/4 [63], where the local energy
density ε is taken from a hydrodynamical model of the medium. The K factor is the only free parameter
√
in the fit of nuclear modification factors. Without including new data at sNN = 5.02 TeV in the fit pro√
√
cedure, they predict a ∼ 15% larger suppression at sNN = 5.02 TeV as compared to sNN = 2.76 TeV,
assuming the same value of K as the one obtained from the fit to the data at the lower energy.
All models presented here describe the main features of the data. The models by Vitev et al., Djordjevic
et al. and CUJET 3.0 give quantitatively good description of the data. The model by Bianchi et al. is
consistent with data within 1.5σ while that by Andrés et al. underestimates the data at high pT . However,
one should note that this comparison is made between unbinned theory calculations and binned data in
relatively large pT bins, which might introduce additional uncertainty.

4

Summary

√
In summary, we measured the primary charged particle pT spectra in pp and Pb–Pb collisions at sNN =
√
5.02 TeV. We also reanalyzed the data collected in pp and Pb–Pb collisions at sNN = 2.76 TeV as
√
well as in p–Pb collisions at sNN = 5.02 TeV with the revised techniques. Thanks to an improved
reconstruction, track selection and data-driven efficiency correction procedure we were able to reduce
the systematic uncertainties by a factor of ∼ 2 as compared to previously published ALICE results. The
measured spectra were used to determine the nuclear modification factors RpPb and RAA . The nuclear
modification factor in p–Pb collisions is consistent with unity at high pT , showing that the strong suppression observed in Pb–Pb is not due to CNM effects but rather due to final state partonic energy loss
in the hot and dense QGP created in Pb–Pb collisions. This suppression is weak in peripheral collisions
and increases with centrality reaching a value of RAA = 0.13 at pT = 6–7 GeV, indicating an increasing
√
parton energy loss with centrality. This suppression is found to be similar at sNN = 2.76 and 5.02 TeV,
despite the much harder pT spectrum at the top energy, which may indicate a stronger parton energy loss

16

## PDF page 17

R PbPb

Charged-particle spectra and nuclear modification factors

ALICE Collaboration

0.6

ALICE Pb-Pb sNN = 5.02 TeV 0-5%
charged particles | η | < 0.8

0.5

Data (Norm. ± 2.7%)

0.4
0.3

Bianchi et al.
CUJET3.0
Andres et al.

0.2

R PbPb

0.1
0

10

20

30

0.6

40

50

p (GeV/ c )
T

0.5
0.4
0.3

SCET G-Vitev
Djordjevic et al.

0.2
0.1
0

10

20

30

40

50

p (GeV/ c )
T

Figure 8: The charged-particle nuclear modification factor measured in the 0–5% most central Pb–Pb collisions
√
at sNN = 5.02 TeV in comparison to model predictions [55–58] (lower panel) and [59–62] (upper panel). The
red boxes around data points represent pT dependent systematic uncertainties. The normalization uncertainty of
the data (±2.7%) is not part of the uncertainties of the plotted data points.

and a larger energy density of the medium at the higher energy. All models presented here describe the
main features of the data with Vitev et al., Djordjevic et al. and CUJET 3.0 being compatible with data
within uncertainties. However, further precision in the theoretical calculations is needed to extract the
transport properties of the hot and dense deconfined QCD matter.

Acknowledgements
The ALICE Collaboration would like to thank all its engineers and technicians for their invaluable contributions to the construction of the experiment and the CERN accelerator teams for the outstanding
performance of the LHC complex. The ALICE Collaboration gratefully acknowledges the resources and
support provided by all Grid centres and the Worldwide LHC Computing Grid (WLCG) collaboration.
The ALICE Collaboration acknowledges the following funding agencies for their support in building and
running the ALICE detector: A. I. Alikhanyan National Science Laboratory (Yerevan Physics Institute)
Foundation (ANSL), State Committee of Science and World Federation of Scientists (WFS), Armenia; Austrian Academy of Sciences and Nationalstiftung für Forschung, Technologie und Entwicklung,
Austria; Ministry of Communications and High Technologies, National Nuclear Research Center, Azerbaijan; Conselho Nacional de Desenvolvimento Cientı́fico e Tecnológico (CNPq), Universidade Federal
do Rio Grande do Sul (UFRGS), Financiadora de Estudos e Projetos (Finep) and Fundação de Amparo à Pesquisa do Estado de São Paulo (FAPESP), Brazil; Ministry of Science & Technology of China
(MSTC), National Natural Science Foundation of China (NSFC) and Ministry of Education of China
(MOEC) , China; Ministry of Science, Education and Sport and Croatian Science Foundation, Croatia;
Ministry of Education, Youth and Sports of the Czech Republic, Czech Republic; The Danish Council
17

## PDF page 18

Charged-particle spectra and nuclear modification factors

ALICE Collaboration

for Independent Research — Natural Sciences, the Carlsberg Foundation and Danish National Research
Foundation (DNRF), Denmark; Helsinki Institute of Physics (HIP), Finland; Commissariat à l’Energie
Atomique (CEA) and Institut National de Physique Nucléaire et de Physique des Particules (IN2P3) and
Centre National de la Recherche Scientifique (CNRS), France; Bundesministerium für Bildung, Wissenschaft, Forschung und Technologie (BMBF) and GSI Helmholtzzentrum für Schwerionenforschung
GmbH, Germany; General Secretariat for Research and Technology, Ministry of Education, Research
and Religions, Greece; National Research, Development and Innovation Office, Hungary; Department
of Atomic Energy Government of India (DAE), Department of Science and Technology, Government
of India (DST), University Grants Commission, Government of India (UGC) and Council of Scientific and Industrial Research (CSIR), India; Indonesian Institute of Science, Indonesia; Centro Fermi
- Museo Storico della Fisica e Centro Studi e Ricerche Enrico Fermi and Istituto Nazionale di Fisica
Nucleare (INFN), Italy; Institute for Innovative Science and Technology , Nagasaki Institute of Applied
Science (IIST), Japan Society for the Promotion of Science (JSPS) KAKENHI and Japanese Ministry
of Education, Culture, Sports, Science and Technology (MEXT), Japan; Consejo Nacional de Ciencia (CONACYT) y Tecnologı́a, through Fondo de Cooperación Internacional en Ciencia y Tecnologı́a
(FONCICYT) and Dirección General de Asuntos del Personal Academico (DGAPA), Mexico; Nederlandse Organisatie voor Wetenschappelijk Onderzoek (NWO), Netherlands; The Research Council of
Norway, Norway; Commission on Science and Technology for Sustainable Development in the South
(COMSATS), Pakistan; Pontificia Universidad Católica del Perú, Peru; Ministry of Science and Higher
Education and National Science Centre, Poland; Korea Institute of Science and Technology Information
and National Research Foundation of Korea (NRF), Republic of Korea; Ministry of Education and Scientific Research, Institute of Atomic Physics and Romanian National Agency for Science, Technology and
Innovation, Romania; Joint Institute for Nuclear Research (JINR), Ministry of Education and Science of
the Russian Federation and National Research Centre Kurchatov Institute, Russia; Ministry of Education,
Science, Research and Sport of the Slovak Republic, Slovakia; National Research Foundation of South
Africa, South Africa; Centro de Aplicaciones Tecnológicas y Desarrollo Nuclear (CEADEN), Cubaenergı́a, Cuba and Centro de Investigaciones Energéticas, Medioambientales y Tecnológicas (CIEMAT),
Spain; Swedish Research Council (VR) and Knut & Alice Wallenberg Foundation (KAW), Sweden; European Organization for Nuclear Research, Switzerland; National Science and Technology Development
Agency (NSDTA), Suranaree University of Technology (SUT) and Office of the Higher Education Commission under NRU project of Thailand, Thailand; Turkish Atomic Energy Agency (TAEK), Turkey;
National Academy of Sciences of Ukraine, Ukraine; Science and Technology Facilities Council (STFC),
United Kingdom; National Science Foundation of the United States of America (NSF) and United States
Department of Energy, Office of Nuclear Physics (DOE NP), United States of America.

References
[1] J. Bjorken, “Energy loss of energetic Partons in quark - gluon plasma: possible extinction of high
pT jets in hadron - hadron collisions,” Tech. Rep. FERMILAB-PUB-82-059-T, Fermilab, 1982.
http://lss.fnal.gov/archive/preprint/fermilab-pub-82-059-t.shtml.
[2] JET Collaboration, K. M. Burke et al., “Extracting the jet transport coefficient from jet quenching
in high-energy heavy-ion collisions,” Phys. Rev. C90 (2014) 014909, arXiv:1312.5003
[nucl-th].
[3] C. Loizides, J. Kamin, and D. d’Enterria, “Improved Monte Carlo Glauber predictions at present
and future nuclear colliders,” Phys. Rev. C97 (2018) 054910, arXiv:1710.07098 [nucl-ex].
[4] PHENIX Collaboration, K. Adcox et al., “Suppression of hadrons with large transverse
√
momentum in central Au+Au collisions at sNN = 130 GeV,” Phys. Rev. Lett. 88 (2002) 022301,
arXiv:nucl-ex/0109003 [nucl-ex].
18

## PDF page 19

Charged-particle spectra and nuclear modification factors

ALICE Collaboration

[5] STAR Collaboration, C. Adler et al., “Centrality dependence of high pT hadron suppression in
√
Au+Au collisions at sNN = 130 GeV,” Phys. Rev. Lett. 89 (2002) 202301,
arXiv:nucl-ex/0206011 [nucl-ex].
[6] PHENIX Collaboration, A. Adare et al., “Suppression Pattern of Neutral Pions at High
√
Transverse Momentum in Au+Au Collisions at sNN = 200 GeV and Constraints on Medium
Transport Coefficients,” Phys. Rev. Lett. 101 (2008) 232301, arXiv:0801.4020 [nucl-ex].
[7] ALICE Collaboration, K. Aamodt et al., “Suppression of charged Particle production at large
√
transverse momentum in central Pb–Pb collisions at sNN = 2.76 TeV,” Phys. Lett. B696 (2011)
30–39, arXiv:1012.1004 [nucl-ex].
[8] ALICE Collaboration, B. Abelev et al., “Centrality dependence of charged particle production at
√
large transverse momentum in Pb–Pb collisions at sNN = 2.76 TeV,” Phys. Lett. B720 (2013)
52–62, arXiv:1208.2711 [hep-ex].
[9] CMS Collaboration, S. Chatrchyan et al., “Study of high-pT charged particle suppression in PbPb
√
compared to pp collisions at sNN = 2.76 TeV,” Eur. Phys. J. C72 (2012) 1945,
arXiv:1202.2554 [nucl-ex].
[10] ATLAS Collaboration, G. Aad et al., “Measurement of charged-particle spectra in Pb+Pb
√
collisions at sNN = 2.76 TeV with the ATLAS detector at the LHC,” JHEP 09 (2015) 050,
arXiv:1504.04337 [hep-ex].
[11] CMS Collaboration, V. Khachatryan et al., “Charged-particle nuclear modification factors in PbPb
√
and pPb collisions at sNN = 5.02 TeV,” JHEP 04 (2017) 039, arXiv:1611.01664 [nucl-ex].
[12] ALICE Collaboration, B. Abelev et al., “Transverse momentum distribution and nuclear
√
modification factor of charged particles in p+Pb collisions at sNN = 5.02 TeV,” Phys. Rev. Lett.
110 (2013) 082302, arXiv:1210.4520 [nucl-ex].
[13] ALICE Collaboration, B. Abelev et al., “Transverse momentum dependence of inclusive primary
√
charged-particle production in p-Pb collisions at sNN = 5.02 TeV,” Eur. J. Phys. C74 (2014)
3054, arXiv:1405.2737 [nucl-ex].
[14] CMS Collaboration, V. Khachatryan et al., “Nuclear effects on the transverse momentum spectra
√
of charged particles in pPb collisions at sNN = 5.02 TeV,” Eur. Phys. J. C75 (2015) 237,
arXiv:1502.05387 [nucl-ex].
[15] ATLAS Collaboration, G. Aad et al., “Transverse momentum, rapidity, and centrality dependence
√
of inclusive charged-particle production in sNN = 5.02 TeV p+Pb collisions measured by the
ATLAS experiment,” Phys. Lett. B763 (2016) 313–336, arXiv:1605.06436 [hep-ex].
[16] ALICE Collaboration, B. Abelev et al., “Energy dependence of the transverse momentum
distributions of charged particles in pp collisions measured by ALICE,” Eur. Phys. J. C73 (2013)
2662, arXiv:1307.1093 [nucl-ex].
[17] ALICE Collaboration, J. Adam et al., “Centrality dependence of the charged-particle multiplicity
√
density at midrapidity in Pb–Pb collisions at sNN = 5.02 TeV,” Phys. Rev. Lett. 116 (2016)
222302, arXiv:1512.06104 [nucl-ex].
[18] ALICE Collaboration, K. Aamodt et al., “The ALICE experiment at the CERN LHC,” JINST 3
(2008) S08002.
[19] ALICE Collaboration, B. B. Abelev et al., “Performance of the ALICE experiment at the CERN
LHC,” Int. J. Mod. Phys. A29 (2014) 1430044, arXiv:1402.4476 [nucl-ex].
19

## PDF page 20

Charged-particle spectra and nuclear modification factors

ALICE Collaboration

[20] ALICE Collaboration, “ALICE Technical Design Report of the Inner Tracking System (ITS),”
Tech. Rep. CERN-LHCC-99-012, CERN, 1999. http://cds.cern.ch/record/391175.
[21] ALICE Collaboration, “ALICE Technical Design Report of the Time Projection Chamber,” Tech.
Rep. CERN-LHCC-2000-001, CERN, 2000. http://cds.cern.ch/record/451098.
[22] ALICE Collaboration, “Centrality determination in heavy ion collisions,” Tech. Rep.
ALICE-PUBLIC-2018-011, CERN, 2018. https://cds.cern.ch/record/2636623.
[23] ALICE Collaboration, B. Abelev et al., “Measurement of the Cross Section for Electromagnetic
√
Dissociation with Neutron Emission in Pb-Pb Collisions at sNN = 2.76 TeV,” Phys. Rev. Lett.
109 (2012) 252302, arXiv:1203.2436 [nucl-ex].
[24] C. Loizides and A. Morsch, “Absence of jet quenching in peripheral nucleus-nucleus collisions,”
Phys. Lett. B773 (2017) 408–411, arXiv:1705.08856 [nucl-ex].
[25] D. Kharzeev, E. Levin, and M. Nardi, “Color glass condensate at the LHC: Hadron multiplicities
in pp, pA and AA collisions,” Nucl. Phys. A747 (2005) 609–629, arXiv:hep-ph/0408050
[hep-ph].
[26] W.-T. Deng, X.-N. Wang, and R. Xu, “Hadron production in p+p, p+Pb, and Pb+Pb collisions with
the HIJING 2.0 model at energies available at the CERN Large Hadron Collider,” Phys. Rev. C83
(2011) 014915, arXiv:1008.1841 [hep-ph].
[27] ALICE Collaboration, J. Adam et al., “Centrality dependence of particle production in p–Pb
√
Collisions at sNN = 5.02 TeV,” Phys. Rev. C 91 (2015) 064905, arXiv:1412.6828 [nucl-ex].
[28] ALICE Collaboration, “The ALICE definition of primary particles,” Tech. Rep.
ALICE-PUBLIC-2017-005, CERN, 2017. https://cds.cern.ch/record/2270008.
[29] ALICE Collaboration, B. Abelev et al., “Measurement of inelastic, single- and double-diffraction
cross sections in proton-proton collisions at the LHC with ALICE,” Eur. Phys. J. C73 (2013)
2456, arXiv:1208.4968 [hep-ex].
√
[30] ALICE Collaboration, “ALICE luminosity determination for pp collisions at s = 5 TeV,” Tech.
Rep. ALICE-PUBLIC-2016-005, CERN, 2016. https://cds.cern.ch/record/2202638.
[31] T. Sjöstrand, S. Mrenna, P. Skands, “A brief introduction to PYTHIA 8.1,” Comput. Phys.
Commun. 178 (2008) 852–867, arXiv:0710.3820 [hep-ph].
[32] P. Skands, S. Carrazza, J. Rojo, “Tuning PYTHIA 8.1: the Monash 2013 tune,” Eur. Phys. J. C74
(2014) 3024, arXiv:1404.5630 [hep-ph].
[33] R. Brun, F. Bruyant, F. Carminati, S. Giani, M. Maire, A. McPherson, G. Patrick, and L. Urban,
GEANT: Detector Description and Simulation Tool; Oct 1994. CERN Program Library. CERN,
Geneva, 1993. https://cds.cern.ch/record/1082634. Long Writeup W5013.
[34] X.-N. Wang and M. Gyulassy, “HIJING: A Monte Carlo model for multiple jet production in p–p,
p–A and A–A collisions,” Phys. Rev. D44 (1991) 3501–3516.
[35] ALICE Collaboration, J. Adam et al., “Measurement of pion, kaon and proton production in
√
proton-proton collisions at s = 7 TeV,” Eur. Phys. J. C75 (2015) 226, arXiv:1504.00024
[nucl-ex].
[36] ALICE Collaboration, J. Adam et al., “Multiplicity dependence of charged pion, kaon, and
√
(anti)proton production at large transverse momentum in p–Pb Collisions at sNN = 5.02 TeV,”
Phys. Lett. B760 (2016) 720–735, arXiv:1601.03658 [nucl-ex].
20

## PDF page 21

Charged-particle spectra and nuclear modification factors

ALICE Collaboration

[37] ALICE Collaboration, J. Adam et al., “Enhanced production of multi-strange hadrons in
high-multiplicity proton-proton collisions,” Nature Physics 13 (2017) 535–539,
arXiv:1606.07424 [nucl-ex].
[38] ALICE Collaboration, B. Abelev et al., “Production of Σ(1385)± and Ξ(1530)0 in proton-proton
√
collisions at s = 7 TeV,” Eur. Phys. J. C75 (2015) 1, arXiv:1406.3206 [nucl-ex].
[39] ALICE Collaboration, D. Adamová et al., “Production of Σ(1385)± and Ξ(1530)0 in p-Pb
√
collisions at sNN = 5.02 TeV,” Eur. Phys. J. C77 (2017) 389, arXiv:1701.07797 [nucl-ex].
[40] ALICE Collaboration, B. Abelev et al., “Multiplicity Dependence of Pion, Kaon, Proton and
√
Lambda Production in p–Pb Collisions at sNN = 5.02 TeV,” Phys. Lett. B728 (2014) 25–38,
arXiv:1307.6796 [nucl-ex].
[41] ALICE Collaboration, B. Abelev et al., “Centrality dependence of π, K, p production in Pb-Pb
√
collisions at sNN = 2.76 TeV,” Phys. Rev. C88 (2013) 044910, arXiv:1303.0737 [hep-ex].
√
[42] ALICE Collaboration, B. Abelev et al., “KS0 and Λ production in Pb–Pb collisions at sNN = 2.76
TeV,” Phys. Rev. Lett. 111 (2013) 222301, arXiv:1307.5530 [nucl-ex].
[43] ALICE Collaboration, B. Abelev et al., “Production of charged pions, kaons and protons at large
√
transverse momenta in pp and Pb–Pb collisions at sNN = 2.76 TeV,” Phys. Lett. B736 (2014)
196–207, arXiv:1401.1250 [nucl-ex].
[44] ALICE Collaboration, J. Adam et al., “Centrality dependence of the nuclear modification factor
√
of charged pions, kaons, and protons in Pb–Pb collisions at sNN = 2.76 TeV,” Phys. Rev. C93
(2016) 034913, arXiv:1506.07287 [nucl-ex].
[45] A. A. Bylinkin and A. A. Rostovtsev, “Parametrization of the shape of hadron-production spectra
in high-energy particle interactions,” Phys. Atom. Nucl. 88 (2012) 999–1005.
[46] D. de Florian, M. Epele, R. J. Hernandez-Pinto, R. Sassot, and M. Stratmann, “Parton-to-Kaon
Fragmentation Revisited,” Phys. Rev. D95 (2017) 094019, arXiv:1702.06353 [hep-ph].
[47] S. Roesler, R. Engel, and J. Ranft, “The Monte Carlo event generator DPMJET-III,” in Advanced
Monte Carlo for radiation physics, particle transport simulation and applications. Proceedings,
Conference, MC2000, Lisbon, Portugal, October 23-26, 2000, pp. 1033–1038. 2000.
arXiv:hep-ph/0012252 [hep-ph]. http://www-public.slac.stanford.edu/sciDoc/
docMeta.aspx?slacPubNumber=SLAC-PUB-8740.
[48] E. Schnedermann, J. Sollfrank, and U. W. Heinz, “Thermal phenomenology of hadrons from
200-A/GeV S+S collisions,” Phys. Rev. C48 (1993) 2462–2475, arXiv:nucl-th/9307020
[nucl-th].
[49] G. D’Agostini, “A Multidimensional unfolding method based on Bayes’ theorem,” Nucl. Instrum.
Meth. A362 (1995) 487–498.
[50] T. Adye, “Unfolding algorithms and tests using RooUnfold,” in Proceedings, PHYSTAT 2011
Workshop on Statistical Issues Related to Discovery Claims in Search Experiments and Unfolding,
CERN,Geneva, Switzerland 17-20 January 2011, pp. 313–318, CERN. CERN, Geneva, 2011.
arXiv:1105.1160 [physics.data-an].
https://inspirehep.net/record/898599/files/arXiv:1105.1160.pdf.
[51] R. Hagedorn, “Multiplicities, pT distributions and the expected hadron → quark-gluon phase
transition,” Riv. Nuovo Cim. 6 (1983) 1–50.
21

## PDF page 22

Charged-particle spectra and nuclear modification factors

ALICE Collaboration

[52] Z.-W. Lin, C. M. Ko, B.-A. Li, B. Zhang, and S. Pal, “A Multi-phase transport model for
relativistic heavy ion collisions,” Phys. Rev. C72 (2005) 064901, arXiv:nucl-th/0411110
[nucl-th].
[53] T. Pierog, I. Karpenko, J. Katzy, E. Yatsenko, and K. Werner, “EPOS LHC: Test of collective
hadronization with data measured at the CERN Large Hadron Collider,” Phys. Rev. C92 (2015)
034906, arXiv:1306.0121 [hep-ph].
[54] J. W. Cronin, H. J. Frisch, M. J. Shochet, J. P. Boymond, R. Mermod, P. A. Piroue, and R. L.
Sumner, “Production of hadrons with large transverse momentum at 200, 300, and 400 GeV,”
Phys. Rev. D11 (1975) 3105–3123.
[55] Z.-B. Kang, R. Lashof-Regas, G. Ovanesyan, P. Saad, and I. Vitev, “Jet quenching phenomenology
from soft-collinear effective theory with Glauber gluons,” Phys. Rev. Lett. 114 (2015) 092002,
arXiv:1405.2612 [hep-ph].
[56] Y.-T. Chien, A. Emerman, Z.-B. Kang, G. Ovanesyan, and I. Vitev, “Jet quenching from QCD
evolution,” Phys. Rev. D93 (2016) 074030, arXiv:1509.02936 [hep-ph].
[57] M. Djordjevic and M. Djordjevic, “Predictions of heavy-flavor suppression at 5.1 TeV Pb+Pb
collisions at the CERN Large Hadron Collider,” Phys. Rev. C92 (2016) 024918,
arXiv:1505.04316 [nucl-th].
[58] M. Djordjevic, B. Blagojevic, and L. Zivkovic, “Mass tomography at different momentum ranges
in quark-gluon plasma,” Phys. Rev. C94 (2016) 044908, arXiv:1601.07852 [nucl-th].
[59] E. Bianchi, J. Elledge, A. Kumar, A. Majumder, G.-Y. Qin, and C. Shen, “The x and Q2
dependence of q̂, quasi-particles and the JET puzzle,” arXiv:1702.00481 [nucl-th].
[60] J. Xu, J. Liao, and M. Gyulassy, “Consistency of perfect fluidity and jet quenching in
semi-quark-gluon monopole plasmas,” Chin. Phys. Lett. 32 (2015) 092501, arXiv:1411.3673
[hep-ph].
[61] J. Xu, J. Liao, and M. Gyulassy, “Bridging soft-hard transport properties of quark-gluon plasmas
with CUJET3.0,” JHEP 02 (2016) 169, arXiv:1508.00552 [hep-ph].
[62] C. Andrés, N. Armesto, M. Luzum, C. A. Salgado, and P. Zurita, “Energy versus centrality
dependence of the jet quenching parameter q̂ at RHIC and LHC: a new puzzle?,” Eur. Phys. J. C76
(2016) 475, arXiv:1606.04837 [hep-ph].
[63] R. Baier, “Jet quenching,” Nucl. Phys. A715 (2003) 209–218, arXiv:hep-ph/0209038
[hep-ph].

22

## PDF page 23

Charged-particle spectra and nuclear modification factors

A

ALICE Collaboration

The ALICE Collaboration

S. Acharya139 , F.T.-. Acosta22 , D. Adamová94 , J. Adolfsson81 , M.M. Aggarwal98 , G. Aglieri Rinella36 ,
M. Agnello33 , N. Agrawal48 , Z. Ahammed139 , S.U. Ahn77 , S. Aiola144 , A. Akindinov64 , M. Al-Turany104 ,
S.N. Alam139 , D.S.D. Albuquerque120 , D. Aleksandrov88 , B. Alessandro58 , R. Alfaro Molina72 , Y. Ali16 ,
A. Alici11 ,53 ,29 , A. Alkin3 , J. Alme24 , T. Alt69 , L. Altenkamper24 , I. Altsybeev138 , C. Andrei47 ,
D. Andreou36 , H.A. Andrews108 , A. Andronic104 , M. Angeletti36 , V. Anguelov102 , C. Anson17 , T. Antičić105 ,
F. Antinori56 , P. Antonioli53 , N. Apadula80 , L. Aphecetche112 , H. Appelshäuser69 , S. Arcelli29 , R. Arnaldi58 ,
O.W. Arnold103 ,115 , I.C. Arsene23 , M. Arslandok102 , B. Audurier112 , A. Augustinus36 , R. Averbeck104 ,
M.D. Azmi18 , A. Badalà55 , Y.W. Baek60 ,76 , S. Bagnasco58 , R. Bailhache69 , R. Bala99 , A. Baldisseri135 ,
M. Ball43 , R.C. Baral86 , A.M. Barbano28 , R. Barbera30 , F. Barile52 , L. Barioglio28 , G.G. Barnaföldi143 ,
L.S. Barnby93 , V. Barret132 , P. Bartalini7 , K. Barth36 , E. Bartsch69 , N. Bastid132 , S. Basu141 , G. Batigne112 ,
B. Batyunya75 , P.C. Batzing23 , J.L. Bazo Alba109 , I.G. Bearden89 , H. Beck102 , C. Bedda63 , N.K. Behera60 ,
I. Belikov134 , F. Bellini29 ,36 , H. Bello Martinez2 , R. Bellwied124 , L.G.E. Beltran118 , V. Belyaev92 ,
G. Bencedi143 , S. Beole28 , A. Bercuci47 , Y. Berdnikov96 , D. Berenyi143 , R.A. Bertens128 , D. Berzano36 ,58 ,
L. Betev36 , P.P. Bhaduri139 , A. Bhasin99 , I.R. Bhat99 , B. Bhattacharjee42 , J. Bhom116 , A. Bianchi28 ,
L. Bianchi124 , N. Bianchi51 , J. Bielčı́k38 , J. Bielčı́ková94 , A. Bilandzic103 ,115 , G. Biro143 , R. Biswas4 ,
S. Biswas4 , J.T. Blair117 , D. Blau88 , C. Blume69 , G. Boca136 , F. Bock36 , A. Bogdanov92 , L. Boldizsár143 ,
M. Bombara39 , G. Bonomi137 , M. Bonora36 , H. Borel135 , A. Borissov20 , M. Borri126 , E. Botta28 ,
C. Bourjau89 , L. Bratrud69 , P. Braun-Munzinger104 , M. Bregant119 , T.A. Broker69 , M. Broz38 , E.J. Brucken44 ,
E. Bruna58 , G.E. Bruno36 ,35 , D. Budnikov106 , H. Buesching69 , S. Bufalino33 , P. Buhler111 , P. Buncic36 ,
O. Busch131 , Z. Buthelezi73 , J.B. Butt16 , J.T. Buxton19 , J. Cabala114 , D. Caffarri36 ,90 , H. Caines144 ,
A. Caliva104 , E. Calvo Villar109 , R.S. Camacho2 , P. Camerini27 , A.A. Capon111 , F. Carena36 , W. Carena36 ,
F. Carnesecchi11 ,29 , J. Castillo Castellanos135 , A.J. Castro128 , E.A.R. Casula54 , C. Ceballos Sanchez9 ,
S. Chandra139 , B. Chang125 , W. Chang7 , S. Chapeland36 , M. Chartier126 , S. Chattopadhyay139 ,
S. Chattopadhyay107 , A. Chauvin115 ,103 , C. Cheshkov133 , B. Cheynis133 , V. Chibante Barroso36 ,
D.D. Chinellato120 , S. Cho60 , P. Chochula36 , S. Choudhury139 , T. Chowdhury132 , P. Christakoglou90 ,
C.H. Christensen89 , P. Christiansen81 , T. Chujo131 , S.U. Chung20 , C. Cicalo54 , L. Cifarelli11 ,29 , F. Cindolo53 ,
J. Cleymans123 , F. Colamaria52 ,35 , D. Colella36 ,52 ,65 , A. Collu80 , M. Colocci29 , M. Concas58 ,ii , G. Conesa
Balbastre79 , Z. Conesa del Valle61 , J.G. Contreras38 , T.M. Cormier95 , Y. Corrales Morales58 , I. Cortés
Maldonado2 , P. Cortese34 , M.R. Cosentino121 , F. Costa36 , S. Costanza136 , J. Crkovská61 , P. Crochet132 ,
E. Cuautle70 , L. Cunqueiro95 ,142 , T. Dahms115 ,103 , A. Dainese56 , M.C. Danisch102 , A. Danu68 , D. Das107 ,
I. Das107 , S. Das4 , A. Dash86 , S. Dash48 , S. De49 , A. De Caro32 , G. de Cataldo52 , C. de Conti119 , J. de
Cuveland40 , A. De Falco26 , D. De Gruttola32 ,11 , N. De Marco58 , S. De Pasquale32 , R.D. De Souza120 ,
H.F. Degenhardt119 , A. Deisting104 ,102 , A. Deloff85 , S. Delsanto28 , C. Deplano90 , P. Dhankher48 , D. Di
Bari35 , A. Di Mauro36 , B. Di Ruzza56 , R.A. Diaz9 , T. Dietel123 , P. Dillenseger69 , Y. Ding7 , R. Divià36 ,
Ø. Djuvsland24 , A. Dobrin36 , D. Domenicis Gimenez119 , B. Dönigus69 , O. Dordic23 , L.V.R. Doremalen63 ,
A.K. Dubey139 , A. Dubla104 , L. Ducroux133 , S. Dudi98 , A.K. Duggal98 , M. Dukhishyam86 , P. Dupieux132 ,
R.J. Ehlers144 , D. Elia52 , E. Endress109 , H. Engel74 , E. Epple144 , B. Erazmus112 , F. Erhardt97 , M.R. Ersdal24 ,
B. Espagnon61 , G. Eulisse36 , J. Eum20 , D. Evans108 , S. Evdokimov91 , L. Fabbietti103 ,115 , M. Faggin31 ,
J. Faivre79 , A. Fantoni51 , M. Fasel95 , L. Feldkamp142 , A. Feliciello58 , G. Feofilov138 , A. Fernández Téllez2 ,
A. Ferretti28 , A. Festanti31 ,36 , V.J.G. Feuillard135 ,132 , J. Figiel116 , M.A.S. Figueredo119 , S. Filchagin106 ,
D. Finogeev62 , F.M. Fionda24 ,26 , M. Floris36 , S. Foertsch73 , P. Foka104 , S. Fokin88 , E. Fragiacomo59 ,
A. Francescon36 , A. Francisco112 , U. Frankenfeld104 , G.G. Fronze28 , U. Fuchs36 , C. Furget79 , A. Furs62 ,
M. Fusco Girard32 , J.J. Gaardhøje89 , M. Gagliardi28 , A.M. Gago109 , K. Gajdosova89 , M. Gallio28 ,
C.D. Galvan118 , P. Ganoti84 , C. Garabatos104 , E. Garcia-Solis12 , K. Garg30 , C. Gargiulo36 , P. Gasik115 ,103 ,
E.F. Gauger117 , M.B. Gay Ducati71 , M. Germain112 , J. Ghosh107 , P. Ghosh139 , S.K. Ghosh4 , P. Gianotti51 ,
P. Giubellino104 ,58 , P. Giubilato31 , P. Glässel102 , D.M. Goméz Coral72 , A. Gomez Ramirez74 , V. Gonzalez104 ,
P. González-Zamora2 , S. Gorbunov40 , L. Görlich116 , S. Gotovac127 , V. Grabski72 , L.K. Graczykowski140 ,
K.L. Graham108 , L. Greiner80 , A. Grelli63 , C. Grigoras36 , V. Grigoriev92 , A. Grigoryan1 , S. Grigoryan75 ,
J.M. Gronefeld104 , F. Grosa33 , J.F. Grosse-Oetringhaus36 , R. Grosso104 , R. Guernane79 , B. Guerzoni29 ,
M. Guittiere112 , K. Gulbrandsen89 , T. Gunji130 , A. Gupta99 , R. Gupta99 , I.B. Guzman2 , R. Haake36 ,
M.K. Habib104 , C. Hadjidakis61 , H. Hamagaki82 , G. Hamar143 , J.C. Hamon134 , M.R. Haque63 , J.W. Harris144 ,
A. Harton12 , H. Hassan79 , D. Hatzifotiadou53 ,11 , S. Hayashi130 , S.T. Heckel69 , E. Hellbär69 , H. Helstrup37 ,
A. Herghelegiu47 , E.G. Hernandez2 , G. Herrera Corral10 , F. Herrmann142 , K.F. Hetland37 , T.E. Hilden44 ,
H. Hillemanns36 , C. Hills126 , B. Hippolyte134 , B. Hohlweger103 , D. Horak38 , S. Hornung104 ,
R. Hosokawa131 ,79 , P. Hristov36 , C. Hughes128 , P. Huhn69 , T.J. Humanic19 , H. Hushnud107 , N. Hussain42 ,

23

## PDF page 24

Charged-particle spectra and nuclear modification factors

ALICE Collaboration

T. Hussain18 , D. Hutter40 , D.S. Hwang21 , J.P. Iddon126 , S.A. Iga Buitron70 , R. Ilkaev106 , M. Inaba131 ,
M. Ippolitov92 ,88 , M.S. Islam107 , M. Ivanov104 , V. Ivanov96 , V. Izucheev91 , B. Jacak80 , N. Jacazio29 ,
P.M. Jacobs80 , M.B. Jadhav48 , S. Jadlovska114 , J. Jadlovsky114 , S. Jaelani63 , C. Jahnke115 ,119 ,
M.J. Jakubowska140 , M.A. Janik140 , P.H.S.Y. Jayarathna124 , C. Jena86 , M. Jercic97 , R.T. Jimenez
Bustamante104 , P.G. Jones108 , A. Jusko108 , P. Kalinak65 , A. Kalweit36 , J.H. Kang145 , V. Kaplin92 , S. Kar7 ,139 ,
A. Karasu Uysal78 , O. Karavichev62 , T. Karavicheva62 , L. Karayan104 ,102 , P. Karczmarczyk36 ,
E. Karpechev62 , U. Kebschull74 , R. Keidel46 , D.L.D. Keijdener63 , M. Keil36 , B. Ketzer43 , Z. Khabanova90 ,
S. Khan18 , S.A. Khan139 , A. Khanzadeev96 , Y. Kharlov91 , A. Khatun18 , A. Khuntia49 , M.M. Kielbowicz116 ,
B. Kileng37 , B. Kim131 , D. Kim145 , D.J. Kim125 , E.J. Kim14 , H. Kim145 , J.S. Kim41 , J. Kim102 , M. Kim60 ,
S. Kim21 , T. Kim145 , T. Kim145 , S. Kirsch40 , I. Kisel40 , S. Kiselev64 , A. Kisiel140 , G. Kiss143 , J.L. Klay6 ,
C. Klein69 , J. Klein36 ,58 , C. Klein-Bösing142 , S. Klewin102 , A. Kluge36 , M.L. Knichel102 ,36 , A.G. Knospe124 ,
C. Kobdaj113 , M. Kofarago143 , M.K. Köhler102 , T. Kollegger104 , V. Kondratiev138 , N. Kondratyeva92 ,
E. Kondratyuk91 , A. Konevskikh62 , M. Konyushikhin141 , O. Kovalenko85 , V. Kovalenko138 , M. Kowalski116 ,
I. Králik65 , A. Kravčáková39 , L. Kreis104 , M. Krivda65 ,108 , F. Krizek94 , M. Krüger69 , E. Kryshen96 ,
M. Krzewicki40 , A.M. Kubera19 , V. Kučera94 ,60 , C. Kuhn134 , P.G. Kuijer90 , J. Kumar48 , L. Kumar98 ,
S. Kumar48 , S. Kundu86 , P. Kurashvili85 , A. Kurepin62 , A.B. Kurepin62 , A. Kuryakin106 , S. Kushpil94 ,
M.J. Kweon60 , Y. Kwon145 , S.L. La Pointe40 , P. La Rocca30 , C. Lagana Fernandes119 , Y.S. Lai80 ,
I. Lakomov36 , R. Langoy122 , K. Lapidus144 , C. Lara74 , A. Lardeux23 , P. Larionov51 , A. Lattuca28 , E. Laudi36 ,
R. Lavicka38 , R. Lea27 , L. Leardini102 , S. Lee145 , F. Lehas90 , S. Lehner111 , J. Lehrbach40 , R.C. Lemmon93 ,
E. Leogrande63 , I. León Monzón118 , P. Lévai143 , X. Li13 , X.L. Li7 , J. Lien122 , R. Lietava108 , B. Lim20 ,
S. Lindal23 , V. Lindenstruth40 , S.W. Lindsay126 , C. Lippmann104 , M.A. Lisa19 , V. Litichevskyi44 , A. Liu80 ,
H.M. Ljunggren81 , W.J. Llope141 , D.F. Lodato63 , V. Loginov92 , C. Loizides95 ,80 , P. Loncar127 , X. Lopez132 ,
E. López Torres9 , A. Lowe143 , P. Luettig69 , J.R. Luhder142 , M. Lunardon31 , G. Luparello59 , M. Lupi36 ,
A. Maevskaya62 , M. Mager36 , S.M. Mahmood23 , A. Maire134 , R.D. Majka144 , M. Malaev96 , L. Malinina75 ,iii ,
D. Mal’Kevich64 , P. Malzacher104 , A. Mamonov106 , V. Manko88 , F. Manso132 , V. Manzari52 , Y. Mao7 ,
M. Marchisone129 ,73 ,133 , J. Mareš67 , G.V. Margagliotti27 , A. Margotti53 , J. Margutti63 , A. Marı́n104 ,
C. Markert117 , M. Marquard69 , N.A. Martin104 , P. Martinengo36 , M.I. Martı́nez2 , G. Martı́nez Garcı́a112 ,
M. Martinez Pedreira36 , S. Masciocchi104 , M. Masera28 , A. Masoni54 , L. Massacrier61 , E. Masson112 ,
A. Mastroserio52 , A.M. Mathis103 ,115 , P.F.T. Matuoka119 , A. Matyja128 , C. Mayer116 , M. Mazzilli35 ,
M.A. Mazzoni57 , F. Meddi25 , Y. Melikyan92 , A. Menchaca-Rocha72 , J. Mercado Pérez102 , M. Meres15 ,
C.S. Meza109 , S. Mhlanga123 , Y. Miake131 , L. Micheletti28 , M.M. Mieskolainen44 , D.L. Mihaylov103 ,
K. Mikhaylov64 ,75 , A. Mischke63 , A.N. Mishra70 , D. Miśkowiec104 , J. Mitra139 , C.M. Mitu68 ,
N. Mohammadi36 ,63 , A.P. Mohanty63 , B. Mohanty86 , M. Mohisin Khan18 ,iv , D.A. Moreira De Godoy142 ,
L.A.P. Moreno2 , S. Moretto31 , A. Morreale112 , A. Morsch36 , V. Muccifora51 , E. Mudnic127 , D. Mühlheim142 ,
S. Muhuri139 , M. Mukherjee4 , J.D. Mulligan144 , M.G. Munhoz119 , K. Münning43 , M.I.A. Munoz80 ,
R.H. Munzer69 , H. Murakami130 , S. Murray73 , L. Musa36 , J. Musinsky65 , C.J. Myers124 , J.W. Myrcha140 ,
B. Naik48 , R. Nair85 , B.K. Nandi48 , R. Nania53 ,11 , E. Nappi52 , A. Narayan48 , M.U. Naru16 , H. Natal da
Luz119 , C. Nattrass128 , S.R. Navarro2 , K. Nayak86 , R. Nayak48 , T.K. Nayak139 , S. Nazarenko106 , R.A. Negrao
De Oliveira69 ,36 , L. Nellen70 , S.V. Nesbo37 , G. Neskovic40 , F. Ng124 , M. Nicassio104 , J. Niedziela140 ,36 ,
B.S. Nielsen89 , S. Nikolaev88 , S. Nikulin88 , V. Nikulin96 , F. Noferini11 ,53 , P. Nomokonov75 , G. Nooren63 ,
J.C.C. Noris2 , J. Norman79 ,126 , A. Nyanin88 , J. Nystrand24 , H. Oeschler20 ,102 ,i , H. Oh145 , A. Ohlson102 ,
L. Olah143 , J. Oleniacz140 , A.C. Oliveira Da Silva119 , M.H. Oliver144 , J. Onderwaater104 , C. Oppedisano58 ,
R. Orava44 , M. Oravec114 , A. Ortiz Velasquez70 , A. Oskarsson81 , J. Otwinowski116 , K. Oyama82 ,
Y. Pachmayer102 , V. Pacik89 , D. Pagano137 , G. Paić70 , P. Palni7 , J. Pan141 , A.K. Pandey48 , S. Panebianco135 ,
V. Papikyan1 , P. Pareek49 , J. Park60 , S. Parmar98 , A. Passfeld142 , S.P. Pathak124 , R.N. Patra139 , B. Paul58 ,
H. Pei7 , T. Peitzmann63 , X. Peng7 , L.G. Pereira71 , H. Pereira Da Costa135 , D. Peresunko92 ,88 , E. Perez
Lezama69 , V. Peskov69 , Y. Pestov5 , V. Petráček38 , M. Petrovici47 , C. Petta30 , R.P. Pezzi71 , S. Piano59 ,
M. Pikna15 , P. Pillot112 , L.O.D.L. Pimentel89 , O. Pinazza53 ,36 , L. Pinsky124 , S. Pisano51 , D.B. Piyarathna124 ,
M. Płoskoń80 , M. Planinic97 , F. Pliquett69 , J. Pluta140 , S. Pochybova143 , P.L.M. Podesta-Lerma118 ,
M.G. Poghosyan95 , B. Polichtchouk91 , N. Poljak97 , W. Poonsawat113 , A. Pop47 , H. Poppenborg142 ,
S. Porteboeuf-Houssais132 , V. Pozdniakov75 , S.K. Prasad4 , R. Preghenella53 , F. Prino58 , C.A. Pruneau141 ,
I. Pshenichnov62 , M. Puccio28 , V. Punin106 , J. Putschke141 , S. Raha4 , S. Rajput99 , J. Rak125 ,
A. Rakotozafindrabe135 , L. Ramello34 , F. Rami134 , D.B. Rana124 , R. Raniwala100 , S. Raniwala100 ,
S.S. Räsänen44 , B.T. Rascanu69 , D. Rathee98 , V. Ratza43 , I. Ravasenga33 , K.F. Read128 ,95 , K. Redlich85 ,v ,
A. Rehman24 , P. Reichelt69 , F. Reidt36 , X. Ren7 , R. Renfordt69 , A. Reshetin62 , J.-P. Revol11 , K. Reygers102 ,
V. Riabov96 , T. Richert63 ,81 , M. Richter23 , P. Riedler36 , W. Riegler36 , F. Riggi30 , C. Ristea68 , M. Rodrı́guez

24

## PDF page 25

Charged-particle spectra and nuclear modification factors

ALICE Collaboration

Cahuantzi2 , K. Røed23 , R. Rogalev91 , E. Rogochaya75 , D. Rohr36 , D. Röhrich24 , P.S. Rokita140 ,
F. Ronchetti51 , E.D. Rosas70 , K. Roslon140 , P. Rosnet132 , A. Rossi56 ,31 , A. Rotondi136 , F. Roukoutakis84 ,
C. Roy134 , P. Roy107 , O.V. Rueda70 , R. Rui27 , B. Rumyantsev75 , A. Rustamov87 , E. Ryabinkin88 ,
Y. Ryabov96 , A. Rybicki116 , S. Saarinen44 , S. Sadhu139 , S. Sadovsky91 , K. Šafařı́k36 , S.K. Saha139 ,
B. Sahoo48 , P. Sahoo49 , R. Sahoo49 , S. Sahoo66 , P.K. Sahu66 , J. Saini139 , S. Sakai131 , M.A. Saleh141 ,
S. Sambyal99 , V. Samsonov96 ,92 , A. Sandoval72 , A. Sarkar73 , D. Sarkar139 , N. Sarkar139 , P. Sarma42 ,
M.H.P. Sas63 , E. Scapparone53 , F. Scarlassara31 , B. Schaefer95 , H.S. Scheid69 , C. Schiaua47 , R. Schicker102 ,
C. Schmidt104 , H.R. Schmidt101 , M.O. Schmidt102 , M. Schmidt101 , N.V. Schmidt95 ,69 , J. Schukraft36 ,
Y. Schutz36 ,134 , K. Schwarz104 , K. Schweda104 , G. Scioli29 , E. Scomparin58 , M. Šefčı́k39 , J.E. Seger17 ,
Y. Sekiguchi130 , D. Sekihata45 , I. Selyuzhenkov92 ,104 , K. Senosi73 , S. Senyukov134 , E. Serradilla72 , P. Sett48 ,
A. Sevcenco68 , A. Shabanov62 , A. Shabetai112 , R. Shahoyan36 , W. Shaikh107 , A. Shangaraev91 , A. Sharma98 ,
A. Sharma99 , N. Sharma98 , A.I. Sheikh139 , K. Shigaki45 , M. Shimomura83 , S. Shirinkin64 , Q. Shou110 ,7 ,
K. Shtejer28 , Y. Sibiriak88 , S. Siddhanta54 , K.M. Sielewicz36 , T. Siemiarczuk85 , S. Silaeva88 , D. Silvermyr81 ,
G. Simatovic90 , G. Simonetti36 ,103 , R. Singaraju139 , R. Singh86 , V. Singhal139 , T. Sinha107 , B. Sitar15 ,
M. Sitta34 , T.B. Skaali23 , M. Slupecki125 , N. Smirnov144 , R.J.M. Snellings63 , T.W. Snellman125 , J. Song20 ,
F. Soramel31 , S. Sorensen128 , F. Sozzi104 , I. Sputowska116 , J. Stachel102 , I. Stan68 , P. Stankus95 ,
E. Stenlund81 , D. Stocco112 , M.M. Storetvedt37 , P. Strmen15 , A.A.P. Suaide119 , T. Sugitate45 , C. Suire61 ,
M. Suleymanov16 , M. Suljic36 ,27 , R. Sultanov64 , M. Šumbera94 , S. Sumowidagdo50 , K. Suzuki111 ,
S. Swain66 , A. Szabo15 , I. Szarka15 , U. Tabassam16 , J. Takahashi120 , G.J. Tambave24 , N. Tanaka131 ,
M. Tarhini61 ,112 , M. Tariq18 , M.G. Tarzila47 , A. Tauro36 , G. Tejeda Muñoz2 , A. Telesca36 , C. Terrevoli31 ,
B. Teyssier133 , D. Thakur49 , S. Thakur139 , D. Thomas117 , F. Thoresen89 , R. Tieulent133 , A. Tikhonov62 ,
A.R. Timmins124 , A. Toia69 , N. Topilskaya62 , M. Toppi51 , S.R. Torres118 , S. Tripathy49 , S. Trogolo28 ,
G. Trombetta35 , L. Tropp39 , V. Trubnikov3 , W.H. Trzaska125 , T.P. Trzcinski140 , B.A. Trzeciak63 , T. Tsuji130 ,
A. Tumkin106 , R. Turrisi56 , T.S. Tveter23 , K. Ullaland24 , E.N. Umaka124 , A. Uras133 , G.L. Usai26 ,
A. Utrobicic97 , M. Vala114 , J. Van Der Maarel63 , J.W. Van Hoorne36 , M. van Leeuwen63 , T. Vanat94 , P. Vande
Vyvre36 , D. Varga143 , A. Vargas2 , M. Vargyas125 , R. Varma48 , M. Vasileiou84 , A. Vasiliev88 , A. Vauthier79 ,
O. Vázquez Doce115 ,103 , V. Vechernin138 , A.M. Veen63 , A. Velure24 , E. Vercellin28 , S. Vergara Limón2 ,
L. Vermunt63 , R. Vernet8 , R. Vértesi143 , L. Vickovic127 , J. Viinikainen125 , Z. Vilakazi129 , O. Villalobos
Baillie108 , A. Villatoro Tello2 , A. Vinogradov88 , L. Vinogradov138 , T. Virgili32 , V. Vislavicius81 ,
A. Vodopyanov75 , M.A. Völkl101 , K. Voloshin64 , S.A. Voloshin141 , G. Volpe35 , B. von Haller36 ,
I. Vorobyev115 ,103 , D. Voscek114 , D. Vranic36 ,104 , J. Vrláková39 , B. Wagner24 , H. Wang63 , M. Wang7 ,
Y. Watanabe130 ,131 , M. Weber111 , S.G. Weber104 , A. Wegrzynek36 , D.F. Weiser102 , S.C. Wenzel36 ,
J.P. Wessels142 , U. Westerhoff142 , A.M. Whitehead123 , J. Wiechula69 , J. Wikne23 , G. Wilk85 , J. Wilkinson53 ,
G.A. Willems36 ,142 , M.C.S. Williams53 , E. Willsher108 , B. Windelband102 , W.E. Witt128 , R. Xu7 , S. Yalcin78 ,
K. Yamakawa45 , P. Yang7 , S. Yano45 , Z. Yin7 , H. Yokoyama131 ,79 , I.-K. Yoo20 , J.H. Yoon60 , V. Yurchenko3 ,
V. Zaccolo58 , A. Zaman16 , C. Zampolli36 , H.J.C. Zanoli119 , N. Zardoshti108 , A. Zarochentsev138 , P. Závada67 ,
N. Zaviyalov106 , H. Zbroszczyk140 , M. Zhalov96 , H. Zhang7 , X. Zhang7 , Y. Zhang7 , Z. Zhang132 ,7 ,
C. Zhao23 , N. Zhigareva64 , D. Zhou7 , Y. Zhou89 , Z. Zhou24 , H. Zhu7 , J. Zhu7 , Y. Zhu7 , A. Zichichi29 ,11 ,
M.B. Zimmermann36 , G. Zinovjev3 , J. Zmeskal111 , S. Zou7 ,

Affiliation notes
i Deceased
ii Dipartimento DET del Politecnico di Torino, Turin, Italy
iii M.V. Lomonosov Moscow State University, D.V. Skobeltsyn Institute of Nuclear, Physics, Moscow, Russia
iv Department of Applied Physics, Aligarh Muslim University, Aligarh, India
v Institute of Theoretical Physics, University of Wroclaw, Poland

Collaboration Institutes
1 A.I. Alikhanyan National Science Laboratory (Yerevan Physics Institute) Foundation, Yerevan, Armenia
2 Benemérita Universidad Autónoma de Puebla, Puebla, Mexico
3 Bogolyubov Institute for Theoretical Physics, National Academy of Sciences of Ukraine, Kiev, Ukraine
4 Bose Institute, Department of Physics and Centre for Astroparticle Physics and Space Science (CAPSS),

Kolkata, India
5 Budker Institute for Nuclear Physics, Novosibirsk, Russia
6 California Polytechnic State University, San Luis Obispo, California, United States

25

## PDF page 26

Charged-particle spectra and nuclear modification factors

ALICE Collaboration

7 Central China Normal University, Wuhan, China
8 Centre de Calcul de l’IN2P3, Villeurbanne, Lyon, France
9 Centro de Aplicaciones Tecnológicas y Desarrollo Nuclear (CEADEN), Havana, Cuba
10 Centro de Investigación y de Estudios Avanzados (CINVESTAV), Mexico City and Mérida, Mexico
11 Centro Fermi - Museo Storico della Fisica e Centro Studi e Ricerche “Enrico Fermi’, Rome, Italy
12 Chicago State University, Chicago, Illinois, United States
13 China Institute of Atomic Energy, Beijing, China
14 Chonbuk National University, Jeonju, Republic of Korea
15 Comenius University Bratislava, Faculty of Mathematics, Physics and Informatics, Bratislava, Slovakia
16 COMSATS Institute of Information Technology (CIIT), Islamabad, Pakistan
17 Creighton University, Omaha, Nebraska, United States
18 Department of Physics, Aligarh Muslim University, Aligarh, India
19 Department of Physics, Ohio State University, Columbus, Ohio, United States
20 Department of Physics, Pusan National University, Pusan, Republic of Korea
21 Department of Physics, Sejong University, Seoul, Republic of Korea
22 Department of Physics, University of California, Berkeley, California, United States
23 Department of Physics, University of Oslo, Oslo, Norway
24 Department of Physics and Technology, University of Bergen, Bergen, Norway
25 Dipartimento di Fisica dell’Università ’La Sapienza’ and Sezione INFN, Rome, Italy
26 Dipartimento di Fisica dell’Università and Sezione INFN, Cagliari, Italy
27 Dipartimento di Fisica dell’Università and Sezione INFN, Trieste, Italy
28 Dipartimento di Fisica dell’Università and Sezione INFN, Turin, Italy
29 Dipartimento di Fisica e Astronomia dell’Università and Sezione INFN, Bologna, Italy
30 Dipartimento di Fisica e Astronomia dell’Università and Sezione INFN, Catania, Italy
31 Dipartimento di Fisica e Astronomia dell’Università and Sezione INFN, Padova, Italy
32 Dipartimento di Fisica ‘E.R. Caianiello’ dell’Università and Gruppo Collegato INFN, Salerno, Italy
33 Dipartimento DISAT del Politecnico and Sezione INFN, Turin, Italy
34 Dipartimento di Scienze e Innovazione Tecnologica dell’Università del Piemonte Orientale and INFN

Sezione di Torino, Alessandria, Italy
35 Dipartimento Interateneo di Fisica ‘M. Merlin’ and Sezione INFN, Bari, Italy
36 European Organization for Nuclear Research (CERN), Geneva, Switzerland
37 Faculty of Engineering and Science, Western Norway University of Applied Sciences, Bergen, Norway
38 Faculty of Nuclear Sciences and Physical Engineering, Czech Technical University in Prague, Prague,

Czech Republic
39 Faculty of Science, P.J. Šafárik University, Košice, Slovakia
40 Frankfurt Institute for Advanced Studies, Johann Wolfgang Goethe-Universität Frankfurt, Frankfurt,

Germany
41 Gangneung-Wonju National University, Gangneung, Republic of Korea
42 Gauhati University, Department of Physics, Guwahati, India
43 Helmholtz-Institut für Strahlen- und Kernphysik, Rheinische Friedrich-Wilhelms-Universität Bonn, Bonn,

Germany
44 Helsinki Institute of Physics (HIP), Helsinki, Finland
45 Hiroshima University, Hiroshima, Japan
46 Hochschule Worms, Zentrum für Technologietransfer und Telekommunikation (ZTT), Worms, Germany
47 Horia Hulubei National Institute of Physics and Nuclear Engineering, Bucharest, Romania
48 Indian Institute of Technology Bombay (IIT), Mumbai, India
49 Indian Institute of Technology Indore, Indore, India
50 Indonesian Institute of Sciences, Jakarta, Indonesia
51 INFN, Laboratori Nazionali di Frascati, Frascati, Italy
52 INFN, Sezione di Bari, Bari, Italy
53 INFN, Sezione di Bologna, Bologna, Italy
54 INFN, Sezione di Cagliari, Cagliari, Italy
55 INFN, Sezione di Catania, Catania, Italy
56 INFN, Sezione di Padova, Padova, Italy
57 INFN, Sezione di Roma, Rome, Italy
58 INFN, Sezione di Torino, Turin, Italy

26

## PDF page 27

Charged-particle spectra and nuclear modification factors

ALICE Collaboration

59 INFN, Sezione di Trieste, Trieste, Italy
60 Inha University, Incheon, Republic of Korea
61 Institut de Physique Nucléaire d’Orsay (IPNO), Institut National de Physique Nucléaire et de Physique des

Particules (IN2P3/CNRS), Université de Paris-Sud, Université Paris-Saclay, Orsay, France
62 Institute for Nuclear Research, Academy of Sciences, Moscow, Russia
63 Institute for Subatomic Physics, Utrecht University/Nikhef, Utrecht, Netherlands
64 Institute for Theoretical and Experimental Physics, Moscow, Russia
65 Institute of Experimental Physics, Slovak Academy of Sciences, Košice, Slovakia
66 Institute of Physics, Bhubaneswar, India
67 Institute of Physics of the Czech Academy of Sciences, Prague, Czech Republic
68 Institute of Space Science (ISS), Bucharest, Romania
69 Institut für Kernphysik, Johann Wolfgang Goethe-Universität Frankfurt, Frankfurt, Germany
70 Instituto de Ciencias Nucleares, Universidad Nacional Autónoma de México, Mexico City, Mexico
71 Instituto de Fı́sica, Universidade Federal do Rio Grande do Sul (UFRGS), Porto Alegre, Brazil
72 Instituto de Fı́sica, Universidad Nacional Autónoma de México, Mexico City, Mexico
73 iThemba LABS, National Research Foundation, Somerset West, South Africa
74 Johann-Wolfgang-Goethe Universität Frankfurt Institut für Informatik, Fachbereich Informatik und

Mathematik, Frankfurt, Germany
75 Joint Institute for Nuclear Research (JINR), Dubna, Russia
76 Konkuk University, Seoul, Republic of Korea
77 Korea Institute of Science and Technology Information, Daejeon, Republic of Korea
78 KTO Karatay University, Konya, Turkey
79 Laboratoire de Physique Subatomique et de Cosmologie, Université Grenoble-Alpes, CNRS-IN2P3,

Grenoble, France
80 Lawrence Berkeley National Laboratory, Berkeley, California, United States
81 Lund University Department of Physics, Division of Particle Physics, Lund, Sweden
82 Nagasaki Institute of Applied Science, Nagasaki, Japan
83 Nara Women’s University (NWU), Nara, Japan
84 National and Kapodistrian University of Athens, School of Science, Department of Physics , Athens,

Greece
85 National Centre for Nuclear Research, Warsaw, Poland
86 National Institute of Science Education and Research, HBNI, Jatni, India
87 National Nuclear Research Center, Baku, Azerbaijan
88 National Research Centre Kurchatov Institute, Moscow, Russia
89 Niels Bohr Institute, University of Copenhagen, Copenhagen, Denmark
90 Nikhef, National institute for subatomic physics, Amsterdam, Netherlands
91 NRC Kurchatov Institute IHEP , Protvino, Russia
92 NRNU Moscow Engineering Physics Institute, Moscow, Russia
93 Nuclear Physics Group, STFC Daresbury Laboratory, Daresbury, United Kingdom
94 Nuclear Physics Institute of the Czech Academy of Sciences, Řež u Prahy, Czech Republic
95 Oak Ridge National Laboratory, Oak Ridge, Tennessee, United States
96 Petersburg Nuclear Physics Institute, Gatchina, Russia
97 Physics department, Faculty of science, University of Zagreb, Zagreb, Croatia
98 Physics Department, Panjab University, Chandigarh, India
99 Physics Department, University of Jammu, Jammu, India
100 Physics Department, University of Rajasthan, Jaipur, India
101 Physikalisches Institut, Eberhard-Karls-Universität Tübingen, Tübingen, Germany
102 Physikalisches Institut, Ruprecht-Karls-Universität Heidelberg, Heidelberg, Germany
103 Physik Department, Technische Universität München, Munich, Germany
104 Research Division and ExtreMe Matter Institute EMMI, GSI Helmholtzzentrum für

Schwerionenforschung GmbH, Darmstadt, Germany
105 Rudjer Bošković Institute, Zagreb, Croatia
106 Russian Federal Nuclear Center (VNIIEF), Sarov, Russia
107 Saha Institute of Nuclear Physics, Kolkata, India
108 School of Physics and Astronomy, University of Birmingham, Birmingham, United Kingdom
109 Sección Fı́sica, Departamento de Ciencias, Pontificia Universidad Católica del Perú, Lima, Peru

27

## PDF page 28

Charged-particle spectra and nuclear modification factors

ALICE Collaboration

110 Shanghai Institute of Applied Physics, Shanghai, China
111 Stefan Meyer Institut für Subatomare Physik (SMI), Vienna, Austria
112 SUBATECH, IMT Atlantique, Université de Nantes, CNRS-IN2P3, Nantes, France
113 Suranaree University of Technology, Nakhon Ratchasima, Thailand
114 Technical University of Košice, Košice, Slovakia
115 Technische Universität München, Excellence Cluster ’Universe’, Munich, Germany
116 The Henryk Niewodniczanski Institute of Nuclear Physics, Polish Academy of Sciences, Cracow, Poland
117 The University of Texas at Austin, Austin, Texas, United States
118 Universidad Autónoma de Sinaloa, Culiacán, Mexico
119 Universidade de São Paulo (USP), São Paulo, Brazil
120 Universidade Estadual de Campinas (UNICAMP), Campinas, Brazil
121 Universidade Federal do ABC, Santo Andre, Brazil
122 University College of Southeast Norway, Tonsberg, Norway
123 University of Cape Town, Cape Town, South Africa
124 University of Houston, Houston, Texas, United States
125 University of Jyväskylä, Jyväskylä, Finland
126 University of Liverpool, Liverpool, United Kingdom
127 University of Split, Faculty of Electrical Engineering, Mechanical Engineering and Naval Architecture,

Split, Croatia
128 University of Tennessee, Knoxville, Tennessee, United States
129 University of the Witwatersrand, Johannesburg, South Africa
130 University of Tokyo, Tokyo, Japan
131 University of Tsukuba, Tsukuba, Japan
132 Université Clermont Auvergne, CNRS/IN2P3, LPC, Clermont-Ferrand, France
133 Université de Lyon, Université Lyon 1, CNRS/IN2P3, IPN-Lyon, Villeurbanne, Lyon, France
134 Université de Strasbourg, CNRS, IPHC UMR 7178, F-67000 Strasbourg, France, Strasbourg, France
135 Université Paris-Saclay Centre dÉtudes de Saclay (CEA), IRFU, Department de Physique Nucléaire

(DPhN), Saclay, France
136 Università degli Studi di Pavia, Pavia, Italy
137 Università di Brescia, Brescia, Italy
138 V. Fock Institute for Physics, St. Petersburg State University, St. Petersburg, Russia
139 Variable Energy Cyclotron Centre, Kolkata, India
140 Warsaw University of Technology, Warsaw, Poland
141 Wayne State University, Detroit, Michigan, United States
142 Westfälische Wilhelms-Universität Münster, Institut für Kernphysik, Münster, Germany
143 Wigner Research Centre for Physics, Hungarian Academy of Sciences, Budapest, Hungary
144 Yale University, New Haven, Connecticut, United States
145 Yonsei University, Seoul, Republic of Korea

28
