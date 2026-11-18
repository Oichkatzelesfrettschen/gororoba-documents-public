Source: https://doi.org/10.1140/epjc/s10052-021-09538-2
PDF sha256: 04054ba17ebfa8200d48f8f49af7d5588e96d6e4b8e6c24bf90fdb840addb8e6
License: CC-BY-4.0
Language: eng
Fidelity: machine-gated

# Transcription of sirunyan_2021_precision_luminosity_measurement_protonproton_collisions.pdf

Transcription of `sirunyan_2021_precision_luminosity_measurement_protonproton_collisions.pdf` in this directory, 42 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-42 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Eur. Phys. J. C (2021) 81:800
https://doi.org/10.1140/epjc/s10052-021-09538-2

Regular Article - Experimental Physics

Precision
luminosity measurement in proton–proton collisions at
√
s = 13 TeV in 2015 and 2016 at CMS
CMS Collaboration∗
CERN,1211 Geneva 23, Switzerland
Received: 5 April 2021 / Accepted: 9 August 2021 / Published online: 9 September 2021
© CERN for the benefit of the CMS collaboration 2021

Abstract The measurement of the luminosity recorded by
the CMS detector installed at LHC interaction point 5, using
√
proton–proton collisions at s = 13 TeV in 2015 and 2016,
is reported. The absolute luminosity scale is measured for
individual bunch crossings using beam-separation scans (the
van der Meer method), with a relative precision of 1.3 and
1.0% in 2015 and 2016, respectively. The dominant sources
of uncertainty are related to residual differences between the
measured beam positions and the ones provided by the operational settings of the LHC magnets, the factorizability of
the proton bunch spatial density functions in the coordinates
transverse to the beam direction, and the modeling of the
effect of electromagnetic interactions among protons in the
colliding bunches. When applying the van der Meer calibration to the entire run periods, the integrated luminosities
when CMS was fully operational are 2.27 and 36.3 fb−1 in
2015 and 2016, with a relative precision of 1.6 and 1.2%,
respectively. These are among the most precise luminosity
measurements at bunched-beam hadron colliders.

1 Introduction
Luminosity, L, is a key parameter at particle colliders. Along
with the energy available in the center-of-mass system, it is
one of the two main figures of merit that quantify the potential for delivering large data samples and producing novel
massive particles. The instantaneous luminosity L(t) is the
process-independent ratio of the rate R(t) of events produced
per unit of time dt to the cross section σ for a given process. The fundamental limitations on precise predictions for
these cross sections (e.g., from quantum chromodynamics)
motivate the techniques used for luminosity measurements
at various types of colliders.
∫ The precise determination of
the integrated luminosity, L(t)dt, has proven particularly
challenging at hadron colliders, with an achieved precision
typically ranging from 1 to 15% [1]. The “precision frontier”
target of 1% [2] does not reflect a fundamental limitation, but
⋆ e-mail: cms-publication-committee-chair@cern.ch

rather results from a variety of uncorrelated sources of systematic uncertainty with typical magnitudes of 0.1–0.5%. In
this paper, we report the precise determination of the absolute luminosity at the CERN LHC interaction point (IP) 5
with the CMS detector [3], using data from proton–proton
√
(pp) collisions at s = 13 TeV collected in 2015 and 2016.
A central component of the physics program at the LHC
consists of measurements that can precisely test the validity of standard model (SM) predictions, e.g., cross sections
for the production of electroweak gauge bosons [4,5] or top
quark pairs [6,7]. A good understanding of the luminosity is
critical to minimize the systematic uncertainty in these measurements. The uncertainty in the luminosity measurement is
often the dominant systematic uncertainty [5–7], motivating
an effort to improve its precision.
Stable luminosity information is also crucial to the efforts
of the LHC operators to optimize the performance of the
accelerator [8,9]. In this context, it is important to provide
luminosity information in real time at a high enough frequency to facilitate rapid optimization. The ability to measure the luminosity of individual bunch crossings (bunchby-bunch luminosity) is also necessary so that the distribution of number of collisions per crossings is known to the
experiments. This information is important when preparing
simulations as well as optimization of thresholds to keep
event-recording rates near data acquisition design targets.
An absolute luminosity scale is obtained with good
accuracy using the direct method of van der Meer (vdM)
scans [10–13]. In these scans, the transverse separation of
the two beams is varied over time and the resulting rate of
some physical observables (e.g., number of charged particles
passing through a silicon detector or energy deposited in a
calorimeter) as a function of separation is used to extract the
effective beam size. The absolute luminosity at one point in
time can then be calculated from measurable beam parameters – namely, the transverse spatial widths of the overlap of the beams and the number of protons in each beam.
To achieve the desired accuracy in the absolute luminosity calibration, the vdM scans are typically performed under

123

## PDF page 2

800 Page 2 of 42

carefully tailored conditions and with beam parameters optimized for that purpose [1], in conjunction with processing the
input from accelerator instrumentation and multiple detector systems. A relative normalization method is then needed
to transfer the absolute luminosity calibration to the complete data-taking period. To this end, for a given subdetector,
the cross section σvis in the “visible” phase space region,
defined by its acceptance, is measured for several observables. The integrated luminosity is obtained from the σvis calibrated counts accumulated for a given period of data taking. Changes in the detector response over time can result in
variations in σvis , which could appear as nonlinearity and/or
long-term instability in the measured luminosity.
To address these challenges, CMS employs a multifaceted
approach, in which measurements from various individual
subsystems are used to produce a final luminosity value with
high precision, good linearity, and stability. Several methods
and independent detectors are used to provide redundancy
and to minimize any bias originating from detector effects.
The LHC orbit is divided into a total of 3564 time windows
25 ns long (bunch crossing slots), each of which can potentially contain a colliding bunch. However, the total number
of filled bunch crossings is limited by design to a maximum
of 2808 by the choice of the beam production scheme in
the injectors and constraints from the rise times of injection and extraction kicker magnets in the various accelerators involved [14]. Furthermore, the length of the injections in
2015 and 2016 was limited by the maximal tolerable heat load
in the arcs due to electron clouds (2015) and safety considerations in the LHC injection system with very luminous beams
(2016) [15]. The bunch crossings are numbered with an identification number (BCID) in the range 1–3564. The specific
pattern of filled and empty bunch crossings used in a single
fill is known as the “filling scheme”; a typical filling scheme
is composed of long strings of consecutive bunches, up to 72
bunches long, called a “train”, with the individual trains separated by gaps of varying lengths. Generally, filling schemes
also include some number of noncolliding bunch crossings,
where one beam is filled but the other remains empty; these
can be used to study effects from beam-induced background.
The two LHC beams are designated “beam 1” and “beam 2”,
where beam 1 (beam 2) circulates in the clockwise (counterclockwise) direction, as viewed from above [14].
For Run 2 of the LHC, the period from 2015 to 2018
√
featuring pp collisions at s = 13 TeV, the CMS luminosity systems were significantly upgraded and expanded.
We report the results for the first two years [16], in which
the operational conditions feature a wide range in the number of colliding bunches n b and instantaneous luminosity,
reaching a maximum of 2232 and 2208, and 0.5 × 1034
and 1.5 × 1034 cm−2 s−1 in 2015 and 2016, respectively.
In the majority of pp LHC fills in Run 2, the bunches are
spaced 25 ns apart. The initial Run 2 data set delivered with

123

Eur. Phys. J. C (2021) 81:800

a bunch spacing of 50 ns is negligibly small [17], and hence
not included in this paper. In this paper, “pileup” refers to the
total number of pp interactions in a single bunch crossing,
and “out-of-time pileup” refers to additional pp collisions
in nearby bunches. For a total inelastic pp cross section of
80 mb [18,19], the pileup during nominal physics data-taking
conditions in 2015 (2016) extended from 5 to 35 (10 to 50)
with an expected average (μ) of about 14 (27) pp interactions.
This paper is structured as follows. In Sect. 2 the CMS
detector is described with special emphasis on the subdetectors used to derive observables for luminosity estimation,
and in Sect. 3 we review the methods to obtain the luminosity information. Section 4 describes the vdM scan calibration
method and the associated systematic uncertainty. Sections 5
and 6 outline the corrections applied to the luminosity algorithms and their resulting performance, respectively. Finally,
Sect. 7 outlines the sources of corrections and the associated systematic uncertainties, and presents the main results.
A summary is given in Sect. 8.

2 The CMS detector
The CMS detector is a multipurpose apparatus designed to
study high- pT physics processes in pp collisions, as well as
a broad range of phenomena in heavy ion collisions. The
central element of CMS is a 3.8 T superconducting solenoid,
13 m in length and 6 m in diameter. Within the solenoid volume are – in order of increasing radius from the beam pipe –
a silicon pixel and strip tracker of high granularity for measuring charged particles up to pseudorapidity (η) of ±2.5; a
lead tungstate crystal electromagnetic calorimeter for measurements of the energy of photons, electrons, and the electromagnetic component of hadronic showers (“jets”); and a
brass and scintillator hadron calorimeter, each composed of
a barrel and two endcap sections, for jet energy measurements. The forward hadron (HF) calorimeter uses steel as
an absorber and quartz fibers as the sensitive material. The
two halves of the HF are located 11.2 m from the interaction
region, one on each end, and together they provide coverage
in the range 3.0 < |η| < 5.2, hence extending the pseudorapidity coverage provided by the barrel and endcap detectors.
Outside the magnet, and within the range |η| < 2.4, is the
muon system [20], which is embedded in the iron flux-return
yoke. It is composed of detection planes made using three
technologies: drift tubes (DTs) in the barrel, cathode strip
chambers (CSCs) in the endcaps, and resistive plate chambers (RPCs) both in the barrel and in the endcaps.
Events of interest for physics are selected using a twotiered trigger system [21]. The first-level trigger, composed
of custom hardware processors, uses information from the
calorimeters and muon detectors to select events at a rate of
around 100 kHz. The second level, known as the high-level

## PDF page 3

Eur. Phys. J. C (2021) 81:800

trigger, consists of a farm of processors running a version
of the full event reconstruction software optimized for fast
processing, and reduces the event rate to around 1 kHz before
data storage.
Several subdetectors, although not part of the main CMS
data acquisition (DAQ) system, provide additional inputs
(e.g., binary logic signals) to the triggering system. The two
beam monitors closest to the IP for each LHC experiment,
the Beam Pick-up Timing for eXperiments (BPTX) detectors [22], are reserved for timing measurements. They are
located on either side of IP 5 at a distance of approximately
175 m. The BPTX system can be used to provide a set of
zero-bias events (i.e., events from nominally colliding bunch
crossings but without a requirement for any specific activity in the event) by requiring a coincidence between the
two BPTX sides. To suppress noise in triggers with high
background, the presence of this coincidence is typically
required [21].
The knowledge of the integrated luminosity requires stability over long periods of time, and hence benefits greatly
from redundant measurements whose combination can lead
to an improved precision. To that end, several upgrades were
completed during the first LHC long shutdown (LS1), the
transition period between LHC Run 1 (2009–2012) and Run
2. The main luminosity subdetectors (luminometers) in Run
1 were the silicon pixel detector and the HF. The HF backend electronics, which were upgraded during LS1, consist
of two independent readout systems: a primary readout over
optical links for physics data taking, and a secondary readout using Ethernet links, explicitly reserved for luminosity
data. In addition, two other luminometers were designed,
constructed, and commissioned: the Pixel Luminosity Telescope (PLT) [23] and the Fast Beam Conditions Monitor
(BCM1F) [24]. Finally, a separate DAQ system was developed that is independent of the central DAQ system [21,25],
so that HF, PLT, and BCM1F data, as well as LHC beamrelated data, are collected and stored in a time- rather than
event-based manner.
The luminometers, along with the accompanying algorithms used to estimate the instantaneous luminosity in Run
2, are briefly described in the following. Figure 1 shows an
overview of the position of these luminometers within CMS.
A more detailed description of the rest of the CMS detector,
together with a definition of the coordinate system used and
the relevant kinematic variables, is reported in Ref. [3].
2.1 Silicon pixel cluster counting
The pixel cluster counting (PCC) method, which uses the
mean number of pixel clusters in the silicon pixel detector,
exploits the very large number of pixels in the inner part of
the CMS tracking system. The number of pixels in 2015–
2016 was about 7 × 107 , which means that the probability

Page 3 of 42 800

of a given pixel being hit by two different charged particles
from the same bunch crossing is exceedingly small. The mean
number of pixel clusters in simulated zero-bias events is of
the order of 100 per pp collision, although the precise mean
depends on the fraction of the detector used for a given data
set. Assuming each pixel cluster comprises five pixels and
using a typical pileup for the 2016 running of μ = 27, the
fraction of pixels hit in a typical bunch crossing is roughly:
f =

hit
Npixel
total
Npixel

≃

100 × 5 × 27
= 0.02%.
7 × 107

(1)

The probability of accidental overlap between pixel clusters
is correspondingly small, and, as a consequence, the number
of pixel clusters per bunch crossing is linearly dependent on
pileup, and therefore an accurate measure of instantaneous
luminosity. Simulated pp collision events that contain only
in-time pileup and detector noise are generated using pythia
version 8.223 [19] with the CUETP8M1 [18,26] tune. The
simulated events include a full simulation of the CMS detector response based on Geant4 [27]. For the sake of simplicity, the number of pileup interactions present in each simulated event is randomly generated from a Poisson distribution
with μ up to 50. Figure 2 shows a representative PCC distribution at μ = 45 and the average PCC as a function of
μ. The latter distribution is fitted with a first-order polynomial, assuming no correlations among different values of μ.
Good agreement is seen based on the estimated goodnessof-fit χ 2 per degree of freedom (dof) value of about 0.5 [28],
indicating linearity under simulated conditions.
Only the components (modules) of the pixel subdetector
that are stable for the entire period of data taking are used
for the PCC rate measurements, excluding pixel modules
known to be defective or significantly affected by the limited
size of the readout buffer [29]. The measured σvis for PCC,
PCC , therefore depends on the data-taking period (i.e., one
σvis
calibration per year).
2.2 Primary vertex counting
The primary vertex counting (PVC) method uses the vertices
that have been reconstructed using the tracks in the CMS
detector. For this method, a good primary vertex is defined to
be one with 11 or more tracks. This requirement is sufficient
to suppress spurious vertices [29], and results in better vertex
resolution.
The PVC method is simple and robust, but suffers from
mild nonlinearity effects when there are many collisions in
a single bunch crossing. There are two competing effects.
In one effect, primary vertices from two collisions occurring close to one another in space are merged, leading to an
undercounting of vertices. In the other effect, the very large

123

## PDF page 4

800 Page 4 of 42

Eur. Phys. J. C (2021) 81:800

Fig. 1 Schematic cross section through the CMS detector in the r -z
plane. The main luminometers in Run 2, as described in the text, are
highlighted, showing the silicon pixel detector, PLT, BCM1F, DTs, and
HF. The two RAMSES monitors used as a luminometer in Run 2 are
located directly behind HF. In this view, the detector is symmetric about

the horizontal and vertical axes, so only one quarter is shown here. The
center of the detector, corresponding to the approximate position of the
pp collision point, is located at the origin. Solid lines represent distinct
η values

numbers of tracks associated with numerous collisions can
produce spurious vertices, leading to overcounting. The precision with which these effects are understood falls short of
the ≈ 1% level needed for luminosity studies. However, during vdM scans these effects are minimal because of the very
low pileup, and so PVC is very useful as a validation tool
for the vdM analysis in the measurement of beam-dependent
parameters.

channel measurements above an analog-to-digital converter
(ADC) threshold is used for each bunch slot in a configurable
time window. The ADC threshold is set high enough to avoid
most noise and as low as possible otherwise. Both the ADC
threshold and the integration time of the histograms between
readouts are configurable, but they were fixed during data
taking in 2015 and 2016. The number of valid measurements
is also stored, so the fraction of events with hits above threshold can be computed.

2.3 Forward hadron calorimeter
2.4 Pixel Luminosity Telescope
The HF luminosity measurement uses the separate readout
described above, so the measurement can be performed at
the full 40 MHz bunch crossing rate. The back-end electronics upgrade during LS1 added new electronics using fieldprogrammable gate array (FPGA) technology such that several features of the readout were separately programmable
for luminosity histogramming, i.e., identifying and counting
the readout channels. Although the whole HF is capable of
being read out for luminosity use, only the two outer rings in
η are used to ensure uniform occupancy and minimize minor
nonlinearities expected from simulation.
The computation of the HF observable is based on the
occupancy method (HFOC). In this method, the fraction of

123

The PLT is a dedicated system for measuring luminosity
using silicon pixel sensors, installed in Run 2, at the beginning of 2015. There are a total of 48 sensors arranged into
16 “telescopes”, eight at either end of CMS outside the pixel
endcap. Each telescope contains three sensor planes which
are arranged in a triplet that faces the IP. The sensors measure
8×8 mm2 , divided into 80 rows and 52 columns, although
only the central region of the sensors is used to reduce the
contribution from background. The PLT measures the rate of
triple coincidences, where a hit is observed in all three planes,
typically corresponding to a track from a particle originating
at the IP. The overall mean rate for PLT is estimated using the

## PDF page 5

Event count

Eur. Phys. J. C (2021) 81:800

3500

Page 5 of 42 800

CMS Simulation

2016 (13 TeV)
Pileup simulation

3000

Average pileup = 45

2500
2000
1500
1000
500
0
0

2000

4000

6000

8000 10000 12000 14000

Simulation - fit .

Average number of clusters

Number of pixel clusters
CMS Simulation
6000
5000

2016 (13 TeV)

Pileup simulation
Linear fit
2016 linearity uncertainty

4000
3000
2000

〈PCC〉/μ = 111.83 ± 0.09
χ2/dof = 9.0 / 19.0

1000

40 0
20
0
−20
−40

0

2.6 Drift tube muon detector

10

20

30

40

10

20

30

40

50

50

Average pileup

Fig. 2 The upper plot shows the number of pixel clusters and their
statistical uncertainty from simulation of pileup following a Poisson
distribution with a mean of 45. The lower plot shows the mean number
of pixel clusters from simulation as a function of mean pileup. The red
curve is a first-order polynomial fit with slope and χ 2 /dof values shown
in the legend. Only pixel modules considered for the PCC measurement
in data are included. The lower panel of the lower plot shows the difference between the simulation and the linear fit in black points. The
green band is the final linearity uncertainty for the 2016 data set

fraction of events where no triple coincidences are observed
(as described in Sect. 3) in order to avoid potential systematic
effects from overlapping tracks being counted as a single hit.

2.5 Fast beam conditions monitor
The BCM1F measures luminosity and beam-induced background separately. It consists of a total of 24 sensors mounted
on the same carriage as the PLT. Single-crystal diamond sensors are used with split-pad metallization. Each sensor has
two readout channels to keep the overall occupancy low,
given the experimental conditions in Run 2. The BCM1F
features a fast readout with 6.25 ns time resolution. The precise time measurement allows hits from collision products to
be separated from beam-induced background hits, while the
incoming background is separated in time from the outgoing
collision products due to the position of BCM1F 1.8 m from
the center of CMS.

The luminosity measurement based on the DT muon detector [20] is based on an efficient trigger on a low-background
physics object: muons produced in the CMS barrel. Muon
track segments from barrel muon DT stations are sent every
bunch crossing to track finder hardware, where tracks are
built and later used to generate first level triggers. The number of tracks in time windows of approximately 23 s is read
out and stored in a database. These data are used to estimate
luminosity. The rate of muons in the DTs is significantly
lower than the rate for most other observables from other
luminometers. Thus, there are not enough muon tracks during the vdM scans to provide a precise measurement of σvis ,
and so the system must be calibrated to the normalized PCC
luminosity measurement. On the other hand, the muon candidate rate has been observed to be linear with luminosity and
rather stable over time. The luminosity data of this system
are integrated over all bunches.
2.7 Radiation monitoring system for the environment and
safety
The Radiation Monitoring System for the Environment and
Safety (RAMSES) is a monitoring subsystem of the unified
supervisory CERN system [30,31]. There are 10 ionization
chambers filled with air at atmospheric pressure that are used
as monitors installed in the CMS experimental cavern. They
are sensitive to ionizing radiation and can monitor the ambient dose equivalent rate. Thus, they generate alarms and interlocks to ensure the safety of the personnel. This system is
maintained and calibrated by the LHC radiation protection
group.
While not designed as a luminometer, the two chambers with the highest rates (designated PMIL55X14 and
PMIL55X15) have been used to produce a luminosity measurement with good linearity and stability over time. However, similarly to the DT luminosity measurement, the overall rates are too low for bunch-by-bunch measurements or
extracting an absolute calibration during vdM scans. The
RAMSES luminosity is thus calibrated to the normalized
PCC luminosity measurement and is used as an additional
measurement for assessing the luminometer stability with
time.

3 Luminosity determination algorithms
Each bunch crossing gives rise to a certain number of pp
interactions. In a given luminometer, each interaction results
in some number of observables (e.g., hits, tracks, or clusters). If one averages over several unbiased measurements,

123

## PDF page 6

800 Page 6 of 42

Eur. Phys. J. C (2021) 81:800

the mean number of observables is
⟨Nobservables ⟩ = ⟨Nobservables/interaction ⟩⟨Ninteractions ⟩
≡ ⟨Nobservables/interaction ⟩μ,

according to Eq. (3):
(2)

where the average number of interactions per bunch crossing
is denoted by μ, in keeping with the Poisson nature of the
underlying probability distribution. Typically these observables are averaged over seconds or tens of seconds.
To measure the instantaneous luminosity, we use the fact
that μ is proportional to the single-bunch crossing instantaneous luminosity Lb via:
μ=

νr
νr
≡ ⟨Nobservables ⟩
.
⟨Nobservables/interaction ⟩ σ
σvis
⟨Nobservables ⟩

(4)

Luminosity is estimated from PCC, PVC, DT, and RAMSES
data using the rate-scaling algorithm.
The second method (zero counting) uses the average fraction of bunch crossings where no observables in a detector
are produced. This zero fraction is then used to infer the
mean number of observables per bunch crossing. The principal advantage of the zero-counting method is that it is not
affected by cases where two or more separate signals overlap
in the detector and produce only one reconstructed observable.
Assuming that the probability of no observables in a single
collision is p, then the probability of no observables seen in
a bunch crossing with k interactions is thus simply p k . Averaged over a large number of bunch crossings, with the number of interactions per bunch crossing distributed according
to a Poisson distribution of mean μ, the expected fraction of
events with zero observables recorded, ⟨ f 0 ⟩, can be expressed
as:
∞ −μ k
∑
e μ
k=0

k!

p k = e−μ(1− p) .

(5)

The logarithm of Eq. (5) is proportional to the mean number
of pp interactions per bunch crossing, and hence to the Lb

123

(6)

The actual value of p does not need to be known beforehand,
since it is effectively absorbed in σvis , although it could be
extracted from the measured σvis value. The raw inputs from
HFOC, PLT, and BCM1F are converted to luminosity using
the zero-counting method.

(3)

where νr = 11 245.6 Hz is the LHC revolution frequency
during collisions, and σ is the total interaction cross section.
At the LHC, Lb is typically expressed in units of Hz/µb ≡
1030 cm−2 s−1 .
Two algorithms have been developed for extracting the
instantaneous luminosity. One method is rate-scaling, where
the raw rate of observables is scaled with calibration constants to the luminosity. Rearranging Eqs. (2) and (3), one
can estimate the instantaneous luminosity using the average
number of observables at a given time:

⟨ f0 ⟩ =

νr
1 νr
νr
= − ln ⟨ f 0 ⟩
≡ − ln ⟨ f 0 ⟩
.
σ
1− p σ
σvis

4 Absolute luminosity calibration

σ Lb
,
νr

Lb =

Lb = μ

Any luminometer requires an externally determined absolute
calibration. Approximate σvis values can be obtained using
Monte Carlo (MC) simulation, but these ultimately rely on
theory, i.e., the inelastic pp cross section, and are not expected
to be reliable at the percent level that represents the target
accuracy for the CMS luminosity measurement. At the LHC,
the precision of theoretical predictions for SM processes is
typically limited by the knowledge of the parton distribution
functions in the proton. Although methods independent of
theoretical assumptions have been proposed at the expense
of introducing correlations between low- and high-μ datataking periods [32], a more precise and purely experimental
method to determine the luminosity is based on the vdM scan
technique, which is used in this paper.
Beam-separation scans are therefore performed to obtain
calibrated σvis for the luminosity measurement. These were
pioneered by Simon van der Meer at the ISR [10], extended
by Carlo Rubbia to the case of a collider with bunched
beams [11], and have been extensively used by all four major
LHC experiments [12,13]. The key principle of the vdM
scan method is to infer the beam-overlap integral from the
rates measured at different beam separations – provided the
beam displacements are calibrated as absolute distances – as
opposed to measuring the bunch density functions directly.
The basic formalism is described in the following.
4.1 The van der Meer method
The instantaneous luminosity for a single colliding bunch
pair in a colliding-beam accelerator is given by:
Lb =

νr n 1 n 2
,
Aeff

(7)

where n 1 and n 2 are the numbers of particles in each of
the two bunches, and Aeff is the effective area of overlap
between the bunches. In general, each of the bunches will be
distributed in the plane transverse to the beam direction, in
which case 1/Aeff can be replaced by an overlap integral of

## PDF page 7

Eur. Phys. J. C (2021) 81:800

Page 7 of 42 800

Σx = Weff =

the bunch densities, i.e.,
∫∫
Lb = νr n 1 n 2

ρ1 (x, y)ρ2 (x, y)dxdy,

(8)

where x and y represent the horizontal and vertical coordinates in the plane transverse to the beams, and ρ1 and ρ2
are the normalized two-dimensional density distributions for
the two bunches. Here, we have integrated over time and the
longitudinal coordinate z.
If one assumes that the bunch profiles can be factorized
into terms depending only on x and y [10,11], then ρi can be
written as the product of one-dimensional density functions
of the form ρi (x, y) = f i (x)gi (y) (i = 1, 2), and 1/Aeff can
be written
1
=
Aeff

∫

∫
f 1 (x) f 2 (x)dx

g1 (y)g2 (y)dy ≡

1 1
,
Weff Heff
(9)

where Weff and Heff are the effective width and the effective
height of the luminous region. For the ideal case of Gaussiandistributed bunches with the same width in both beams and
undergoing head-on collisions, Eq. (8) reduces to:
Lb =

νr n 1 n 2
,
4π σx σ y

(10)

where σx and σ y are the root-mean-square (RMS) widths
of the horizontal and vertical bunch profiles in either beam,
respectively.
In the case of round beams, σx = σ y ≡ σb ≡
√
ϵN β ∗ /γ , where ϵN is the so-called normalized emittance,
γ the relativistic Lorentz factor, and β ∗ corresponds to the
value of the optical function β at the IP [33].
We designate the luminosity when the beams are displaced
with respect to each other by an amount w in the x direction,
or an amount h in the y direction, as L(w, h). As shown
in Ref. [10], when a separation scan is performed in the x
direction, in which w is varied in a systematic way from −∞
to +∞, the effective width can be determined from:
∫∫
Weff =

f 1 (x) f 2 (x − w)dxdw
∫
=
f 1 (x) f 2 (x)dx

∫

Lb (w, 0)dw
,
Lb (0, 0)

(11)

where common normalization factors have been canceled in
the second step. Similarly, if a scan is performed in the y
direction, the effective beam-overlap height is given by
∫∫
Heff =

g1 (y)g2 (y − h)dydh
∫
=
g1 (y)g2 (y)dy

∫

Lb (0, h)dh
.
Lb (0, 0)

(12)

For Gaussian-distributed bunches, the resulting scan curves,
L(w, 0) and L(0, h), are also Gaussian with RMS widths of

Lb =

√
√
2σx and Σ y = Heff = 2σ y , yielding

νr n 1 n 2
.
2π Σx Σ y

(13)

Equations (11) and (12) are quite general, and do not depend
on the assumption of Gaussian-distributed bunches. Indeed,
it is frequently the case that simple Gaussians do not provide
an adequate description of the scan-curve data. In such cases,
we use double-Gaussian functions of the form
)
)]
[
(
(
1 − ϵx
ϵx
1
x2
x2
+
,
f (x) = √
exp −
exp
−
2
2
σ2x
2σ1x
2σ2x
2π σ1x

(14)
where ϵx is the fraction of the Gaussian with width σ1x . Normally the Gaussian with the smaller width σ1x is considered
the core Gaussian, while the Gaussian with the larger width
σ2x is used to fit the tails of the scan curve. Similar relations apply for the y coordinate. The effective value of Σi
(i = x, y) is then given by
Σi =

σ1i σ2i
.
ϵi σ2i + (1 − ϵi )σ1i

(15)

To calibrate a given luminosity algorithm, the absolute luminosity computed from beam parameters via Eq. (13) is used
in conjunction with Eq. (3) to obtain
σvis = μvis

2π Σx Σ y
,
n1n2

(16)

where μvis is the visible interaction rate. In this analysis,
μvis is taken as the arithmetic mean of the peak values from
L(w, 0) and L(0, h) in scans that are performed sufficiently
close in time to minimize the impact of varying bunch distributions over the course of a fill. Equation (16) therefore
provides a direct calibration of the visible cross section for
each algorithm in terms of Σx Σ y and n 1 n 2 .
In the LHC, bunches typically cross at a small angle φ in
the horizontal plane at IP 5. This introduces a reduction in
the luminosity relative to the case of head-on collisions [1],
given by:
[
) ]−1/2
(
σz
φ 2
L
= 1+
tan
,
L0
σx
2

(17)

where σx is the width of the luminous region in the crossing
plane and σz is the width in the longitudinal direction. For typical LHC physics running conditions in 2016, φ ≃ 140 µrad,
σx ≃ 12 µm, and σz ≃ 8 cm, and so the reduction from
Eq. (17) is around 10% [34]. The vdM scans are typically carried out under special conditions, where φ = 0, as described
in the following. The values of σvis do not depend on the
crossing angle.

123

## PDF page 8

800 Page 8 of 42

4.2 Analysis of vdM scan data
While σvis does not depend on beam conditions, the LHC
delivers beams under special conditions to improve the precision of measurements and to reduce systematic effects. The
vdM filling schemes are characterized by a low number of
colliding bunch pairs at IP 5 (n b = 30–50). The bunches are
widely separated from each other in the LHC orbit, to reduce
the effect of afterglow (as discussed in Sect. 5.1). Special
beam optics with β ∗ ≈ 19 m and transverse emittance of
ϵN ≈ 3.0 µm are implemented to produce a relatively large
bunch size of approximately σb = 100 µm. Large bunches
reduce the impact of vertex reconstruction resolution in analyses where vertex positions are utilized. A crossing angle of
0 is used for collisions at IP 5 in vdM scans. To minimize the
effect of potential nonlinear response in the luminometers,
the target pileup is set to μ ≈ 0.6, which is 1–2 orders of
magnitude lower than typical physics fills. To achieve that
goal, in addition to the large beam size, the beams have relatively low intensities, which typically begin at (8–9)×1010
protons per filled bunch, resulting in a total intensity of (3.5–
4.0)×1012 per beam for 44 bunches.
The total beam intensities are measured with the DC current transformers (DCCT) [35], and the bunch currents measured with the fast beam current transformers (FBCT) [36],
and cross-checked with the longitudinal density monitors
(LDMs) [37,38] and the beam quality monitors [39]. Because
of the low beam intensity and low collision rate, the luminosity remains nearly constant over the course of time, in
contrast to typical physics fills [9]. The beam orbit is monitored using two systems, the Diode Orbit and Oscillation
(DOROS) beam position monitors (BPMs) [40] located near
IP 5, and the BPMs located in the LHC arcs adjacent to CMS
(referred to as “LHC arc BPMs”). The latter are transformed
to a beam position at IP 5 using the LHC optics files that are
centrally provided by LHC operators [41]. The orbit is also
tracked using the movements of the luminous region at IP 5
based on the vertices reconstructed with the CMS tracker.
The vdM scan program at IP 5 consists of a series of x-y
scan pairs. Figure 3 shows the progression of these scans in
a calibration fill, with the beam displacement measured by
the DOROS BPMs [40,42].
Typical scan sessions consist of at least three vdM scan
pairs, with one scan in each of the transverse coordinates
per pair. There are two at the start of the fill and another at
the end of fill. In the absence of systematic effects, all scans
are expected to produce compatible results. In each pair, the
scans are typically performed first in the x and then in the
y direction, although sometimes the pair is performed in the
opposite order. In the vdM scans, the two beams are separated
by up to 6σb , and scanned across one another in a sequence
of 25 steps of 30 s each to obtain a statistically significant
measurement.

123

Eur. Phys. J. C (2021) 81:800

Dedicated length scale calibration (LSC) scans (described
in Sect. 4.3.4), which are used to calibrate the distance by
which the steering magnets displace the beams, are also
performed typically close in time to the rest of the scans
and using the same collision optics configuration. The LSC
implemented at IP 5 is of a constant-separation type, in which
the two beams are positioned at −2.5 and −1.5σb relative to
nominal and moved together forward in steps of 1σb , maintaining the 1σb separation between the two beams, until they
reach the +2.5σb point. Then, their positions are swapped,
and they are moved together backward in −1σb steps back
to −2.5σb . The scan is performed once in the x direction and
once in the y direction, with a total of 10 steps of 60 s in
each direction. The LSC scans are performed with successive forward and backward displacements for multiple measurements under slightly different conditions in case there
are compounding effects that limit precision. The transverse
position of the luminous region is needed for this calibration and is measured using reconstructed primary vertices in
CMS data.
To test the assumption of transversely factorizable bunch
profiles in Eq. (9), four dedicated beam-imaging (BI) scans
are performed, one for each beam and each transverse direction. One beam is kept fixed at its head-on position, while the
other is moved and scanned in 19 steps from −4.5 to +4.5σb
along x or y with a duration of 40 s per step. Primary vertices are reconstructed, and their positions are then analyzed
to perform a global fit to derive the transverse bunch density
distributions of the beams (as discussed in Sect. 4.4.1). The
BI scans are also analyzed as regular beam-separation scans.
During both BI and regular vdM scans, the transverse bunch
density distributions are also determined by simultaneously
fitting the beam-separation dependence (“evolution”) on the
luminosity and the luminous region position, orientation, and
spatial width, as reflected in the reconstructed primary vertices (as discussed in Sect. 4.4.2).
The LHC conditions at IP 5 for the luminosity calibration
fills discussed in this paper for 2015 and 2016 are summarized
in Table 1.
Pixel data are collected for PCC and for methods involving collision vertices using a zero-bias trigger, which collects data from five BCIDs with a total rate of approximately
20 kHz. Figure 4 shows vdM scan data from PCC recorded in
the fifth scan pair of the session in fill 4954. The fit function
corresponds to the double-Gaussian formalism of Eq. (14),
and the parameters are estimated by simultaneously fitting
the PCC and PVC rate measurements. An additional constant term is included to estimate the background originating
from noncollision sources. This function provides a good
description of the data in a range that extends over nearly
three orders of magnitude in rate (χ 2 /dof ≈ 1 in Fig. 4). For
other luminometers, background rates are either negligible
(PLT and PVC) or estimated and subtracted (BCM1F and

## PDF page 9

Eur. Phys. J. C (2021) 81:800

Page 9 of 42 800

Fig. 3 Relative change in the positions of beams 1 and 2 measured by the DOROS BPMs during fill 4954 in the horizontal (x) or vertical (y)
directions, as a function of the time elapsed from the beginning of the program. The gray vertical lines delineate vdM, BI, or LSC scans
Table 1 Summary of the LHC conditions at IP 5 for the scan sessions
luminosity. The columns corresponding to “No. of scans” indicate the
in pp collisions in 2015 and 2016. The column labeled μ is the average
total number of vdM, BI, and LSC scans that were performed in either
pileup corresponding to Linit , the latter denoting the initial instantaneous
transverse coordinate, counting only scans used for analysis
√
∗
Fill
s (TeV)
Date
nb
φ (µrad)
β (cm)
μ
Linit (×1030 cm−2 s−1 )
No. of scans
vdM

BI

LSC

4266

13

Aug. 2015

30

0

1917

0.6

2.7

6

4

3

4945

13

May 2016

32

0

1917

0.6

2.5

–

–

2

4954

13

May 2016

32

0

1917

0.6

2.5

6

4

2

HFOC) prior to the beam parameter fit. Since the instantaneous luminosity is relatively low, any nonlinear effect has
a negligibly small impact in any method. The beam-width
parameters (Eq. (15)) measured using different luminometers are in excellent agreement, which is shown in Fig. 5 with
comparisons of Aeff with the nominal PCC+PVC results.
Although the accelerator parameters, such as bunch transverse sizes or intensities, vary during the course of a fill, such
changes cancel in the calculation of σvis , which should remain
PCC as
invariant. This is shown in Fig. 6 for the measured σvis
a function of time for vdM scans taken in fills 4266 and
4954. After including all the effects described in Sect. 4.3,
PCC = 9.166 ± 0.056 (stat) and 8.429 ± 0.029 (stat) barns
σvis
in 2015 and 2016, respectively, where the bunch-by-bunch
fit uncertainty in Σx , Σ y , and μvis is propagated to the meaPCC per scan. Since these uncertainties are statistical
sured σvis
in nature, they contribute to the scan-to-scan combination in
an uncorrelated way. The assumption of factorizable proton
bunch densities limits the level of accuracy in the luminosity
scale inferred from Eq. (13). A common approach is thus
adopted at the LHC that includes a dedicated tailoring of the
proton bunch injection chain to minimize the emergence of
non-Gaussian bunch density distributions [43]. Since the factorizability between the x and y distributions could impact
the vdM scan result of the different IPs differently, CMS
reconstructs the individual proton bunch densities during the
BI and vdM scans, as described in Sect. 4.4.

4.3 Corrections to vdM scan data
Several systematic effects can change the measurement of
σvis , and the following sections describe the measurement of
these effects, the corrections used, and the resulting systematic uncertainty in σvis .
Adjustments to the bunch-by-bunch charge measurement
are made to correct for spurious charge that is present outside the nominally filled part of the slot (Sect. 4.3.1). Then,
we correct for potential sources of bias associated with the
beam position monitoring at the scale of µm. We distinguish
between “orbit drifts”, which we model with smooth, linear
functions, and residual differences relative to the nominal
beam positions, where corrections per scan step are assessed.
Since both effects are time dependent, thereby biasing σvis
incoherently, they are monitored continuously during each
scan (Sect. 4.3.2).
Another source of correction originates from the electromagnetic interaction between charged particles in the colliding bunches (beam-beam effects); when the beams are
displaced, rather than being head-on, a beam deflection and
change in β ∗ may be induced. The former causes the beams
to be more separated than the nominal value from LHC beam
position estimates, whereas the latter influences the spatial
distributions of proton bunches and thus the observed rate.
The resulting corrections to σvis are evaluated at IP 5 [44,45],
and depend on the LHC optics, beam parameters, and filling
scheme (as discussed in Sect. 4.3.3).

123

## PDF page 10

800 Page 10 of 42

Eur. Phys. J. C (2021) 81:800

103

CMS

102

2016 (13 TeV)

Fill 4954, fth x scan, PCC
Data
Fit
Gauss 1
Gauss 2
Const

Residuals [σ] Normalized rate [a.u.]

Residuals [σ] Normalized rate [a.u.]

2016 (13 TeV)

10

1

3
0
−3
−0.6

−0.4

−0.2

0

0.2

0.4

0.6

Horizontal beam separation [mm]

Aeff / Aeff,PCC+PVC

1.04

CMS

102

Fill 4954, fth y scan, PCC
Data
Fit
Gauss 1
Gauss 2
Const

10

1

3
0
−3
−0.6

−0.4

−0.2

0

0.2

0.4

0.6

Vertical beam separation [mm]
low, and green curves show the first and second Gaussian components
and the constant component, respectively. All corrections described in
Sect. 4.3 are applied. The lower panels display the difference between
the measured and fitted values divided by the statistical uncertainty

Fig. 4 Example vdM scans for PCC for BCID 41, from the last scan
pair in fill 4954, showing the rate normalized by the product of beam
currents and its statistical uncertainty as a function of the beam separation in the x (left) and y (right) direction, and the fitted curves. The
purple curve shows the overall double-Gaussian fit, while the blue, yel-

CMS

2015 (13 TeV)

1.03
1.02

BCM1F

± RMS

PLT

± RMS

PVC

± RMS

1.01
1
0.99
0.98
0.97

Aeff / Aeff,PCC+PVC

Fig. 5 The two figures show
comparisons of effective area
(Aeff ) of cross-check
luminometers with respect to the
nominal PCC+PVC for fills
4266 (upper) and 4954 (lower).
The points are the ratio of the
Aeff of the labeled luminometer
to PCC+PVC. There are 25 Aeff
values because there are five
scan pairs with five BCIDs
analyzed for each scan pair. The
solid lines are the average of all
the Aeff while the bands are the
standard deviations. In both sets
of data the average comparison
is compatible with unity within
or near the standard deviation

103

1.04

0

5

10

15

20

25

Scan Pair
2016 (13 TeV)

CMS

1.03
1.02

HFOC

± RMS

PLT

± RMS

PVC

± RMS

1.01
1
0.99
0.98
0.97

0

5

10

15

20

25

Scan Pair

123

## PDF page 11

Eur. Phys. J. C (2021) 81:800

σPCC
[b]
vis

9.45

Page 11 of 42 800

CMS

2015 (13 TeV)
Bunch crossing identification number

9.4

9.35

51

771

2211

2674

1631

9.3
9.25
9.2
9.15
9.1
9.05
9

1

2

3

5

4

σPCC
[b]
vis

Scans in x and y
8.6

CMS

2016 (13 TeV)
Bunch crossing identification number

8.55

41

281

1783

2063

872

8.5
8.45

of the two beams; since it is more precise than the FBCT
sum, its scale is used to normalize the sum of the FBCT
measurements.
Both the DCCT and FBCT measurements are sensitive to
additional charges outside the actual colliding bunch. These
components must be measured and subtracted. The LHC
radio frequency (RF) cavities operate at 400 MHz, so a single
25 ns wide bunch slot contains ten 2.5 ns wide “RF buckets”.
Only one RF bucket in a given bunch slot is filled with protons, and, in principle, the other nine RF buckets are empty.
Similarly, of the total 3564 bunch slots, only a predefined
subset is filled, according to the filling scheme. In practice,
however, a small amount of spurious charge is present in the
nominally empty RF buckets and bunch slots, which should
be subtracted from the n 1 and n 2 values in Eq. (13). The
amount of “ghost” charge in the nominally empty bunch slots
is included in the DCCT but not in the FBCT measurement,
since the latter is insensitive to bunch charges below a certain threshold. The out-of-time (satellite) charge occupies RF
buckets adjacent to the main bunch. As such, it can experience long-range interactions with the main bunch in the other
beam and is visible in the FBCT measurement. The corrected
value for n j (where j denotes the BCID) is therefore given
by:
(
)
j
j
n FBCT 1 − f sat
(
)
nj =
NDCCT 1 − f ghost ,
∑ j
j n FBCT

8.4
8.35
1

2

3

4

(18)

5

Scans in x and y
PCC , corrected for all the effects described in
Fig. 6 The measured σvis
Sect. 4.3, shown chronologically for all vdM scan pairs (where 3 and 4
are BI scans) taken in fills 4266 (upper) and 4954 (lower), respectively.
Each of the five colliding bunch pairs is marked with a different color.
The error bars correspond to the statistical uncertainty propagated from
PCC . The band is the standard deviation of all fitted
the vdM fit to σvis
PCC values
σvis

The vdM method requires an accurate knowledge of the
beam separation. Possible differences in the absolute scale
between the nominal beam separation produced by the steering of the LHC magnets, as used in Eqs. (11) and (12), and the
actual separation are determined by using the LSC procedure
(Sect. 4.3.4).
4.3.1 Beam current calibration and spurious charge
The LHC beam currents are measured by dedicated devices.
The FBCT system is used to measure the current of individual
bunches in 25 ns bunch slots. The DCCT system provides
a precise (0.2%) measurement of the total current for each

j

where f sat represents the per-bunch correction due to the
satellite bunch population and f ghost is the correction for the
ghost charge.
The spurious charge is measured by the LHC LDM system, which provides a precise longitudinal distribution of the
beam charge with a time resolution of 90 ps. The data from
the LDMs for fills 4266 and 4954 indicate that both the ghost
and satellite charges are small. The latter is estimated to be
< 0.1% for each of the two beams and is neglected. No particular time dependence for either beam is observed, and the
resulting overall spurious-charge correction in σvis amounts
to +0.2 and +0.3% in 2015 and 2016, respectively. This is
applied as a correction to the beam currents in Eq. (16).
The ghost charge is also measured using the beam-gas
imaging method [12,46,47], which compares the beam-gas
rates in bunch crossings at IP 8 (the location of the LHCb
detector) where only one beam contains protons, or where
neither beam contains protons, leading to consistent results
with the LDM measurement. The systematic uncertainty of
0.1% is assigned to cover the difference between the two
estimates of the ghost contributions to the beam current.

123

## PDF page 12

800 Page 12 of 42

4.3.2 Beam position monitoring
Although the LHC beam orbits are generally stable during
a fill, even a small variation (either random or systematic in
nature) in the beam positions during scans can significantly
affect the resulting calibrations. The beam positions are measured primarily using the DOROS BPM system. The LHC
arc BPMs, when possible, are used to confirm the stability
of the orbits during the scan.
To measure the orbit drift, we use the beam position measurements in x and y in three 15 s periods when the beams are
nominally colliding head-on: immediately before and after
each scan, as well as at the middle point of the scan, where
the beams are also head-on. For each scan, a fit using a firstorder polynomial is performed from the point before the scan
to the middle point, and it is used to derive the correction for
the first half of the scan. Similarly, a fit from the middle to
the point after the scan is used to correct the second half of
the scan. Figure 7 shows the measured positions along with
the resulting fits. In general, the orbit drift during the 2015
and 2016 vdM scans is less than about 5 µm for most of the
scans. However, in the third scan of both series, the orbit
drift was significant enough to shift σvis by approximately
+1.0%. The corrections are derived using the average of the
two BPM systems, and the largest deviation of the correction
from each individual system from the nominal correction is
taken as the value of the systematic uncertainty due to orbit
drift. This is typically 0.1–0.2% overall.
At each scan step, the actual beam separation can be also
affected by systematic or random deviations of the beam positions from their nominal settings, which, in turn, impact the
observed rate at each scan point. The magnitude of this potential bias is evaluated from consecutive single-beam orbit measurements at IP 5, provided by the DOROS BPMs and with a
duration of a few seconds each. They are further corrected for
the beam-beam effects (as discussed in Sect. 4.3.3) and the
length scale (as described in Sect. 4.3.4) using the position of
reconstructed vertices as the calibration target. The impact
from beam-beam deflection at the location of the DOROS
m)away from IP 5) is magnified by
BPMs (z DOROS = ±21.5
(
a factor of 1 + tan π Q x/y z DOROS /β ∗ , where Q x and Q y
are the betatron tune values in the x and y directions [33].
Because these values are different, the resulting factors are
2.7 in the x direction and 2.8 in the y direction. The measurements from the DOROS BPMs are integrated over all
bunches. Therefore, the observed beam-beam deflection may
be overestimated because of the inclusion of noncolliding,
nondeflected bunches. In this analysis, a reduction factor of
0.6 is thus applied on top of the geometric factor in both
years, which is the approximate fraction of the total number
of bunches in the vdM fills that collide at IP 5. The orbit
drift, as described above, is also subtracted from the singlebeam DOROS measurements before forming the actual beam

123

Eur. Phys. J. C (2021) 81:800

separation. Finally, an additional length scale correction is
made to DOROS data for each beam and in both of the two
transverse directions. The calibration using vertices, both for
DOROS and nominal LHC positions, determines only the
average length scale for the two beams. The calibrations of
each beam are also not necessarily the same for the two sets
of data. Therefore, a final, relative calibration of the DOROS
data is made to align each beam in both transverse directions
to the scale of the LHC beams. Figure 8 shows the residual difference in beam separation in all y scans in 2015 and
2016 as well as the residuals per beam in a single scan, which
shows symmetric behavior. The resulting impact on σvis is
in the range −0.6 to +0.4 and −0.5 to −0.2%, with average
values of −0.1 and −0.3%, in 2015 and 2016, respectively.
Corrections are applied for each scan, and the uncertainty
comes from the reduction factor in the beam-beam deflection correction at the location of the DOROS BPMs.
4.3.3 Beam-beam effects
We distinguish two types of beam-beam interactions that
affect the vdM and BI scan measurements: coherent and
incoherent beam-beam effects. The total correction originates from the combination of both effects, which affect the
nominal beam separation (coherent) and the detector rate
(incoherent) via the change of the beam shapes.
The closed orbits of the bunches in the scans are shifted
coherently by the angular kick induced by their electromagnetic repulsion, resulting in an increase in the absolute beam
separation. The size of this additional beam-beam deflection depends on the transverse beam size, bunch intensities, collision optics, and separation between the orbits of
colliding bunches. It is calculated based on the Bassetti–
Erskine formalism for the electric field of elliptically distributed bunches, as discussed in Ref. [48]. The orbit shift
depends linearly on the separation for small nominal beam
separations, reaches a maximum near 2σb (≈ 0.2 mm in fills
4266 and 4954), and decreases nonlinearly towards zero at
larger separations. Figure 9 (left) [44,45] shows the resulting
correction as a function of nominal beam separation, for the
conditions during the scans in fill 4954 (Table 1). The beambeam deflection correction increases the Σx and Σ y values,
impacting the σvis measurement by about +2.0 (+1.6)% in
2015 (2016).
The incoherent effect corresponds to the change of the
proton bunch density distribution functions ρ(x, y) at the IP
due to deflection at the per-particle level. It causes a change in
the effective β ∗ , and thus results in a change in the measured
luminosity. This dynamic evolution of β ∗ is usually referred
to as the “dynamic-β” effect. The correction for the dynamicβ effect is evaluated numerically by using a dedicated particle tracking program that calculates Aeff under different
hypotheses [44,45]. Considering the dynamic-β effect inde-

## PDF page 13

Eur. Phys. J. C (2021) 81:800

Page 13 of 42 800

Beam-separation correction [μm]

3

CMS

2.5
2

2015 (13 TeV)

vdM (1)

vdM (2)

BI (1)

BI (2)

vdM (3)

1.5
1
0.5
0

−0.5
−1
−2

3

CMS

2.5

Beam 1

2

Beam 2

1.5
1
0.5
0
−1

−1.5

−0.6

−0.4

−0.2

0

0.2

0.4

−2

0.6

−0.6

−0.4

2016 (13 TeV)

CMS

2.5
2

vdM (1)

vdM (2)

BI (1)

BI (2)

vdM (3)

1.5
1
0.5
0

−0.5

0

0.2

0.4

0.6

3

CMS

2016 (13 TeV)

2.5

Beam 1

2

Beam 2

1.5
1
0.5
0

−0.5

−1

−1.5
−2

−0.2

Nominal vertical separation [mm]
DOROS BPMs-nominal [μm]

Nominal vertical separation [mm]
3

2015 (13 TeV)

−0.5

−1.5

Beam-separation correction [μm]

Fig. 8 The beam-separation
residuals in y during all scans in
fills 4266 (upper) and 4954
(lower) are shown on the left.
The dots correspond to the
difference (in terms of beam
separation in µm) between the
corrected beam positions
measured by the DOROS BPMs
and the beam separation
provided by LHC magnets
(“nominal”). The error bars
denote the standard deviation in
the measurements. The figures
on the right show the residual
position differences per beam
between the DOROS BPMs and
LHC positions for the first vdM
scans in y in fills 4266 (upper)
and 4954 (lower)

DOROS BPMs-nominal [μm]

First-order polynomial fits are subsequently made to the input from
BPMs (dots) and are used to estimate the orbit drift at each scan step.
Slow, linear orbit drifts are corrected exactly in this manner, and more
discrete discontinuities are corrected on average

Fig. 7 Effect of orbit drift in the horizontal (upper) and vertical (lower)
beam-separation directions during fill 4954. The dots correspond to the
beam positions measured by the DOROS or LHC arc BPMs in µm at
times when the beams nominally collide head-on and in three periods
per scan (before, during, and after) represented by the vertical lines.

−1

−1.5

−0.6

−0.4

−0.2

0

0.2

0.4

0.6

Nominal vertical separation [mm]

−2

−0.6

−0.4

−0.2

0

0.2

0.4

0.6

Nominal vertical separation [mm]

123

## PDF page 14

2.0

Eur. Phys. J. C (2021) 81:800
(2016) 13 TeV

CMS

(2016) 13 TeV

CMS
Fill 4954 (first x scan, BCID 992)

0.996

Fill 4954 (first x scan, BCID 992)

1.5
1.0

Dynamic-β correction

Beam-beam deflection correction [μm]

800 Page 14 of 42

0.5
0.0
-0.5
-1.0

0.992
0.990
0.988
0.986

-1.5
-2.0

0.994

-0.6

-0.4 -0.2
0.0
0.2
0.4
Nominal beam separation [mm]

0.6

0.984

-0.6

-0.4 -0.2
0.0
0.2
0.4
Nominal beam separation [mm]

0.6

Fig. 9 Calculated beam-beam deflection due to closed-orbit shift (left)
and the multiplicative rate correction for PLT due to the dynamic-β
effect (right) as a function of the nominal beam separation for the beam

parameters associated with fill 4954 (first scan, BCID 992). Lines represent first-order polynomial interpolations between any two adjacent
values

pendently of the beam-beam deflection, we obtain the ratio
of the detector rate as shown in Fig. 9 (right). At vdM conditions, the dynamic-β correction can be up to about −2%
at large values of beam separation. Figure 9 shows the effect
is typically larger at higher beam separation. In contrast to
the beam-beam deflection, the dynamic-β correction thus
decreases the original Σx and Σ y values. The corresponding
impact on the calculated σvis is about −1.7 (−1.4)% in 2015
(2016).
The total beam-beam correction (i.e., when both the beambeam deflection and dynamic-β effects are included) results
in an increase in the calculated σvis of about 0.3 (0.2)% in
2015 (2016) at IP 5. In addition, when considering further
head-on collisions at the IP at the opposite side of the ring
(IP 1 at ATLAS), the effect is approximated as a single-IP
simulation but with shifted betatron tune values. The impact
on σvis is enhanced by a factor of about two, leading to a total
beam-beam correction of +0.6 (+0.4)% in 2015 (2016). The
uncertainty in this calculation is dominated by the uncertainty
in the betatron tune values, which was estimated taking into
account the symmetric tune spread as well as the full shift due
to head-on collisions at a second interaction point (in ATLAS
at IP 1). These considerations translate into an uncertainty of
0.5% in the corrected σvis [44,45].

of the steering dipoles themselves (e.g., magnet hysteresis) or
lattice imperfection [41], i.e., higher multipole components
in the quadrupoles located within those orbit bumps. For a
given IP, there are four possible bumps, for the two possible
displacement directions of the two beams.
An accurate calibration for the size of the bumps can be
obtained using the CMS tracker. In particular, for small vertex displacements, the uncertainty in the reconstructed vertex
position in x or y is ≈ 20 µm for zero-bias collisions [29].
During LSC scans, the data for each separation distance contains several hundred thousand reconstructed vertices, yielding a position measurement with submicron precision.
The vdM scans described in Sect. 4.2 are typically done
by moving the beams in equal steps in opposite directions.
Since the two beams have independent length scales, the
full separation correction is obtained from the mean of the
length scale corrections per beam. Separate scans, wherein
both beams are moved in steps in the same direction, are
thus required to obtain the LSC. A more detailed description
on the relationship between the calibration constant associated with the “offset” (i.e., the arithmetic mean between the
transverse beam positions) and the observed quantities during LSC scans can be found in Ref. [12]. Here, for each scan
step, the centroid of the luminous region is measured as the
mean from a Gaussian fit to the observed vertex positions. A
calibration constant for each transverse direction is extracted
with a first-order polynomial fit to the difference between the
measured mean position and the nominal offset as a function
of the latter. This constant corresponds to the average calibration of the bumps of the two beams. It is then applied as
a scale factor to correct the nominal beam displacement.
The nominal offset is also affected by the random and
systematic beam position deviations described in Sect. 4.3.2.
The beam positions at each step are monitored using DOROS

4.3.4 Length scale calibration
In the canonical vdM formalism described in Sect. 4.1,
it is implicitly assumed that the beam separation is perfectly known. Operationally, the nominal displacement of
the beams at the IP is achieved based on a local distortion
(bump) of the orbit using a pair of steering dipoles located on
either side of the IP [49]. The size of the nominal separation is
subject to potential uncertainty associated with the response

123

## PDF page 15

Eur. Phys. J. C (2021) 81:800

Page 15 of 42 800

plane. The combined correction to the visible cross section is
(−0.4±0.2) and (−1.3±0.3)%. The total uncertainty, equal
to the uncertainty contributions from the x and y planes added
in quadrature, includes the statistical uncertainty in the firstorder polynomial fits (< 0.1%), the variation between the
two scan directions and the different scans (0.1%), a tracker
alignment uncertainty (< 0.1%), and the uncertainty from
the estimated beam position deviations (0.1–0.2%).
4.4 Transverse factorizability
The use of the vdM scan technique to measure Aeff relies
on the assumption that the proton bunch density functions
are factorizable into x- and y-dependent components, as
described in Sect. 4.1. If this condition is not met exactly,
the measurements of Aeff and σvis will be biased. To correct for this potential bias, the bunch density distributions
are measured independently with two methods, which are
used in a combined way to evaluate Aeff . In both methods,
primary vertices are reconstructed from tracks measured in
the CMS silicon tracker.
4.4.1 Beam-imaging method

Fig. 10 Fits to LSC forward (purple) and backward (green) scan data
for the x (upper) and y (lower) LSC scans in fill 4945. The error bars
denote the statistical uncertainty in the fitted luminous region centroid

BPMs. We estimate the arithmetic mean of the measured step
sizes as a good representation of the nominal settings, after
excluding outlier step sizes based on an iterative procedure.
The difference of the remaining step sizes from the mean is
used to correct the nominal offsets, and their standard deviation is the uncertainty due to beam position deviations. The
correction improves the quality of the first-order polynomial
fits and the forward-to-backward scan agreement. Consistent
results are also found using the LHC arc BPMs to derive the
correction for beam position deviations.
The fit results for the x and y LSC scans are shown in
Fig. 10 for fill 4945. The difference between the measured
displacement of the beam centroid and the nominal displacement of the beams, corrected for the estimated beam position deviation, is plotted as a function of the latter. In all
cases, the data are well described by first-order polynomial
fits with calibration constants differing on average from zero
by −0.3 and −0.8% in the horizontal plane in 2015 and
2016, respectively, and by −0.1 and −0.5% in the vertical

In the BI method [50,51], the distributions of reconstructed
vertices during BI scans are used to obtain an image of the
transverse bunch profiles integrated over the scanning direction. A primary vertex resolution comparable to or smaller
than the transverse beam sizes is necessary to extract the
beam profiles from the measured distributions. The twodimensional distribution in x and y of the reconstructed vertices depends on the overlap of the bunch density functions,
their transverse separations Δx and Δy, and the vertex resolution V of the CMS tracker system as:
N vtx (x, y; Δx, Δy) ∝ ρ1 (x, y)ρ2 (x + Δx, y + Δy) ⊗ V.
(19)
The combination of the vertex distributions from all steps of
the BI scan in the x direction is approximated as:
+4.5σ
∑b

N vtx (x, y; Δx, Δy)

Δx=−4.5σb

[∫

≈

]
ρ1 (x, y)ρ2 (x + Δx, y)d(Δx) ⊗ V

= ρ1 (x, y)(Mx ρ2 )(y) ⊗ V.
(20)
∫
Here, (Mx ρ2 )(y) = ρ2 (x, y)dx denotes that the proton
bunch density of the second beam appears marginalized in
the direction of the scan. This results from the assumption
that the step size is small enough with respect to the width of
the bunch densities, so we can replace the sum over discrete

123

## PDF page 16

800 Page 16 of 42

Eur. Phys. J. C (2021) 81:800
2016 (13 TeV)

0.6

CMS

Fill 4954, beam-imaging method
Scan #4, t model: g1 + g2 – g3

4

0.4

0.2
0

Pull

y [mm]

2

0
−2

−0.2
−4
−0.4
−0.4

−0.2

0

0.2

0.4

x [mm]
2016 (13 TeV)

0.5
0
−0.5
−1
0

0.1

0.2

0.3

0.4

1

Average pull

Average pull

Fill 4954, beam-imaging method
Scan #4, t model: g1 + g2 – g3

CMS

1

2016 (13 TeV)

0.5
0
−0.5
−1
−π

Radius [mm]
Fig. 11 Example of the pull distributions of the fit model of Eq. (22)
with respect to the vertex distribution that constrains beam 2 in the
y direction recorded in fill 4954. The upper plot shows the twodimensional pull distributions, and the lower plots show the per-bin

scan points with a continuous integral over Δx. This twodimensional vertex distribution can be exploited to constrain
the transverse correlations of the bunch density of the first
beam.
Combining four such vertex distributions accumulated
during the BI scan set, we reconstruct the two-dimensional
proton bunch densities of the two beams from a simultaneous
fit. This requires knowledge of the primary vertex resolution,
which is modeled with a two-dimensional Gaussian function.
Convolving with the primary vertex resolution is then analytically possible for bunch density models built from Gaussian
functions.
Models for the proton bunch density are built from Gaussian distributions parameterized with an additional correlation parameter ϱ:

123

Fill 4954, beam-imaging method
Scan #4, t model: g1 + g2 – g3

CMS

−π/2

0

π/2

π

Angle
pulls averaged over the same radial distance (lower left) or angle (lower
right). The error bars in the lower plot denote the standard error in the
mean of the pulls in each bin. The fluctuations observed in the radial
projection of the residuals are included in the uncertainty estimation

g j (x, y) =

(
1
1
exp −
√
2(1 − ϱ2j )
2π σ j x σ j y 1 − ϱ2j
])
[ 2
2ϱ j x y
x
y2
,
× 2 + 2 −
σ jxσ jy
σjx
σ jy

(21)

where j indicates the beam number ( j = 1 or 2). More
complicated models are constructed with sums of these individual correlated Gaussian distributions. Distributions with
a wide tail are better described by adding a Gaussian component with a small weight and a large width. Distributions
with a flattened central part can be modeled with an additional component with a small negative weight and a narrow
width. Typically, both nonzero correlation parameters and
different widths are required to describe the nonfactorizability observed in data.

## PDF page 17

Eur. Phys. J. C (2021) 81:800

Page 17 of 42 800

The best description of the BI data collected in 2015 and
2016 for the five bunch crossings used is achieved consistently with a sum of three Gaussian distributions, where the
narrow component has a negative weight:
ρ j (x, y) = −w j,1 g j,1 (x, y) + w j,2 g j,2 (x, y)
+(1 + w j,1 − w j,2 )g j,3 (x, y).

(22)

Figure 11 shows the two-dimensional pull distribution, i.e.,
vtx − N vtx )/σ
(Ndata
data , and the one-dimensional projections for
fit
the vertex distributions collected in the BI scan where the first
beam is moved vertically for one bunch crossing in fill 4954.
In these fits, the effects from the beam-beam deflection and
dynamic-β are included in the positions of the reconstructed
vertices and as per-vertex weights, respectively, whereas the
impact of orbit drift is negligibly small.
The value of Aeff can then be calculated from an integration
∫∫ of the overlap of the bunch densities directly (i.e., Aeff =
ρ1 (x, y)ρ2 (x, y)dxdy). This is compared to the value of
Aeff obtained from an MC simulated vdM scan pair generated
with the reconstructed bunch densities as input, and analyzed
with the vdM method (i.e., Aeff = 1/(2π ΣxMC Σ yMC )). The
difference between the two values yields the bias of the vdM
results, and is applied as a correction to σvis values. The bias is
computed separately for each bunch crossing, and the results
are shown in Fig. 12. The values for the estimated bias are
averaged, resulting in a correction of +1.3 (0.9)% in σvis for
2015 (2016) because of the assumption of x-y factorization.
To estimate the uncertainty in the measured bias, the MC
simulation of the vdM scans is repeated multiple times and
the RMS of the resulting biases is 0.1% for both years, which
is considered as the statistical uncertainty in the vdM scans.
Additionally, a systematic uncertainty is evaluated with a
closure test: simulated models are constructed by randomly
drawing parameters of the fit model in Eq. (22). These are
used to simulate MC pseudo-experiments by generating BI
scan data, which are then fitted with the same model and procedure. Comparing simulated models with fit quality and fitted correction values similar to the data fits, the bias obtained
from the bunch densities reconstructed from the fit agrees
well on average with the true bias of the simulated model.
The RMS of the distributions of deviations is 0.5% for both
years. We assign this RMS as the systematic uncertainty.
4.4.2 Luminous region evolution
In this method, which was inspired by Ref. [13], the luminosity and luminous region geometry are used to reconstruct the bunch density distributions in three dimensions
and as a function of time. Using single-beam parameters,
described in the following, bunch profiles are then generated for simulated vdM scans and treated as genuine vdM
scan data. Similar to the BI method, the impact of factoriza-

Fig. 12 Factorization bias estimated from the fits to the BI bunch-bybunch data in fills 4266 (upper) and 4954 (lower). The error bars denote
sources of uncertainty (statistical and systematic), added in quadrature,
in the factorization bias estimates

tion is extracted by comparing the “measured” luminosity
extracted from the one-dimensional vdM simulated bunch
profiles with the “true” luminosity from the computed fourdimensional (x, y, z, t) overlap integral of the single-bunch
distributions. The luminous region is modeled by a threedimensional ellipsoid whose parameters (nine in total) are
extracted from an unbinned maximum likelihood fit of a
three-dimensional Gaussian function to the spatial distribution of the primary vertices [29]. The vertex resolution is
determined from data as part of the fitting procedure.
The bunch profiles ρ j (x, y, z), parameterized per beam
j, are the sum of three individual Gaussian distributions
g j,1...3 (x, y, z) with common mean, but arbitrary width and
orientation parameters (referred to as “bunch parameters” in
the following):
ρ j (x, y, z) = w j,1 g j,1 (x, y, z) + w j,2 g j,2 (x, y, z)
+(1 − w j,1 − w j,2 )g j,3 (x, y, z).

(23)

The overlap integral of Eq. (23) is evaluated at each scan
step to predict the true luminosity and the geometry of the

123

## PDF page 18

800 Page 18 of 42

Eur. Phys. J. C (2021) 81:800

Fig. 13 Beam-separation
dependence of the luminosity
and some luminous region
parameters during the first
horizontal vdM scan in fill 4954.
The points represent the
luminosity normalized by the
beam current product (upper
left), the horizontal position of
the luminous centroid (upper
right), and the horizontal and
vertical luminous region widths
(lower left and right). The error
bars represent the statistical
uncertainty in the luminosity,
and the fit uncertainty in the
luminous region parameters.
The line is the result of the
three-Gaussian (g1 + g2 ± g3 )
fit described in the text. In all
cases, the lower panels show the
one-dimensional pulls

luminous region for a given set of bunch parameters. In this
calculation, we consider the impact of beam-beam effects,
LSC, and orbit drifts. The bunch parameters are then adjusted
according to a χ 2 minimization procedure to determine the
best-fit centroid position, orientation, and the widths (corrected for the primary vertex resolution) of the luminous
region measured at each step of a BI or vdM scan. An example
of a fit to the PCC luminosity and luminous region geometry is illustrated in Fig. 13 for one of the horizontal scans
in fill 4954 and a subset of the three-dimensional ellipsoid
parameters. One of the four figures shows the variation in the
beam width in y during the x-separation beam scan, which
is indicative of nonfactorization. The goodness of fit is better than χ 2 /dof = 1.8 for both years, with some systematic
deviations being apparent mainly in the tails of the scan. The
fits are repeated by substituting PLT as the luminosity input,
but no particular dependence is seen.
This procedure is applied to all (i.e., BI and vdM) scans
in fills 4266 and 4954, and the results are summarized in
Fig. 14. The σvis extracted from the standard vdM analysis
with the assumption that factorization is valid is smaller by
0.6–1.1 (0.2)% than that computed from the reconstructed

123

single-bunch parameters in fill 4266 (4954). Similar to the
evaluation in the BI method, the uncertainty amounts to
0.6%. This uncertainty is dominated by the standard deviation in simulation-driven closure tests, and includes the
fit uncertainty in data and the contributions from beambeam effects, length scale, and orbit drift. These observations are thus consistent with the ones obtained in Sect. 4.4.1
in terms of absolute magnitude during the BI scans. The
two results are combined to produce the final correction in
σvis of +(0.8–1.3 ± 0.5) and +(0.6 ± 0.5)% in 2015 and
2016, respectively. The final corrections retain the time evolution derived uniquely from the luminous region evolution
method.

5 Rate corrections under physics running conditions
The calibration scans described in the previous sections are
performed with a small number of well-separated proton
bunches with low bunch intensity. In contrast, during nominal
conditions, the collision rate is generally maximized to produce large data sets for physics measurements and searches.

## PDF page 19

Eur. Phys. J. C (2021) 81:800

Page 19 of 42 800

Fig. 14 Ratio of the σvis evaluated from the overlap integral of the
reconstructed single-bunch profiles in two (BI method) or three (luminous region evolution) spatial dimensions to that determined by the vdM
method, assuming factorization, and their combination. The central values are displayed as points or with a line while the corresponding full

uncertainties are shown as hatched areas. Different methods (including
the combination) are color coded. Each point corresponds to one scan
pair in fills 4266 (left) and 4954 (right). The statistical uncertainty is
shown by the error bars

This section describes the corrections that are applied to
uncalibrated luminometer rates to ensure that the final luminosity values are accurate. These corrections, summarized in
Table 2 for 2016, compensate for out-of-time pileup, efficiency, and nonlinearity effects for each individual luminometer.

In contrast, T2 afterglow tends to impact all bunch crossings, because the half-life of the activated material can be
longer than several bunch crossings. The response can be
modeled with a single- or double-exponential distribution.
The impact of T2 afterglow varies by filling scheme and
by detector. In fills where n b is low and where the bunches
are well separated, the T2 corrections are very small and
often completely negligible, as is the case by design in the
vdM calibration fills. When LHC fills contain several hundred bunches, the corrections start to contribute at the percent
level in most bunches. With maximally full filling schemes,
the corrections can be up to about 4 (15)% for PCC (HFOC).
Although there are clearly two distinct components, a
combined (T1 and T2) model can be constructed that gives
the response for a specific bunch crossing, accounting for
contributions from all other 3563 bunch crossing slots. This
model is referred to as the single-bunch response (SBR). The
SBR for HFOC luminosity is taken directly from data in a
reference fill with n b = 2 for approximately the first half
of the bunch crossings, and the bunches in the second half
are smoothly extrapolated using an exponential model. The
SBR is normalized to Lb (n) and it is then subtracted from all
other bunch slots. This procedure is repeated for all bunch
crossings.
After the corrections from the SBR are applied, empty
bunch slots, where there are no collisions, should have a rate
of zero. For PCC, the SBR is determined by optimizing αT1 ,
which is time dependent and measured in intervals of about
20 min, and the parameters of the exponential used for T2
corrections, such that there is minimal residual rate in the
noncolliding bunch slots. Figure 15 shows per-bunch data in

5.1 Out-of-time pileup corrections
The measurements in most detectors have out-of-time pileup
contributions that do not arise from the in-time pp collision within the 25 ns window of the bunch crossing. Ideally, these contributions should be subtracted from all bunch
crossings before the total instantaneous luminosity is computed. There are generally two types of effects that are considered: spillover of electronic signals and real additional
response from material activation. These are denoted as type
1 (T1) and 2 (T2) afterglow, respectively.
The T1 afterglow generally only impacts the following
bunch crossing because electronic signals tend to decline
exponentially and hence two bunches later (50 ns) the signal
is again below threshold. The T1 contribution in bunch n + 1
from bunch n is proportional to Lb (n). Thus, the model for
the correction is:
Lb,corr (n + 1) = Lb,uncorr (n + 1) − αT1 Lb,corr (n),

(24)

where αT1 is detector dependent and sometimes time dependent; αT1 ranges from 0.005 for BCM1F to 0.02 for HFOC
to as large as 0.09 for PCC.

123

## PDF page 20

800 Page 20 of 42

Eur. Phys. J. C (2021) 81:800
agreement of the luminometers in terms of Aeff relative to PCC during
fill 4954 are given, respectively. The DT luminosity is also corrected for
a very small additional muon rate from beam halo and cosmic sources,
which is treated as a constant per fill

Table 2 Summary of the rate corrections under physics running conditions in 2016 applied separately to each luminometer. For HFOC, two
distinct sources of out-of-time pileup corrections are provided. In the
first and second columns, the vdM calibration condition and the relative
vdM calibrated

vdM calibration agreement to PCC (%)

Out-of-time pileup
corrections (%)

Efficiency corrections (%)

PCC

Yes

–

0–4

1

–

DT

No

–

–

–

–

HFOC

Yes

0.2

0–15, 1–5

1

0–10

PLT

Yes

0.1

–

0–10

−0.2 to +1.4/(Hz/µb)

PVC

Yes

<0.1

–

–

–

RAMSES

No

–

–

–

–

a fill from 2016 before and after the afterglow corrections for
PCC are applied.
The empty bunch slots are also used to estimate the residual afterglow after the full set of corrections is applied. The
corrected rate in the first empty bunch slot after a colliding
bunch slot is used to estimate the residual T1 response. Likewise, the 2nd to 30th empty bunch slots are used to estimate
the residual T2 effect. This procedure is performed for the
entire 2015 and 2016 data sets for PCC and HFOC luminosity measurements. A window covering all residuals over the
course of each data set is used as the systematic uncertainty
in the final corrections. The resulting uncertainty for PCC
⨁
⨁
in the two corrections is 0.3 0.1 (0.3 0.3)% in 2015
(2016).
These types of per-bunch luminosity corrections are
applied for PCC, HFOC, and BCM1F, whereas PLT is
almost completely background free and no such correction is
needed. Since the DT and RAMSES measurements integrate
over all bunch crossings, out-of-time pileup corrections can
only be applied on average to the integrated rates. For DT
these amount to 0–1%, while no corrections are applied to
RAMSES.
A second type of T1 afterglow affects the HFOC luminosity. This is the case where the afterglow from a preceding bunch and the signal from the current bunch are both
under the threshold to be counted as a hit, but their sum
exceeds the threshold. This effect is referred to as the “bunch
train effect”, because it affects only active bunches preceded
by other active bunches (that is, bunches within a train, as
opposed to “leading” bunches at the beginning of a train).
The method previously described for estimating T1 afterglow does not include this contribution. This effect is measured in a dedicated study comparing the double ratio of
the leading bunch in a train relative to the second bunch for
HFOC divided by the same ratio for PCC. A single correction model with magnitude 1–5%, linearly increasing with
instantaneous luminosity, is determined utilizing most valid
data from 2016.

123

Nonlinear
response (%)

Fig. 15 The upper plot shows the instantaneous luminosity measured
from PCC as a function of BCID before (filled blue points) and after
(open red points) afterglow corrections are applied for each colliding
bunch. The upper panel shows a subset of bunch crossings colliding at
IP 5, and the lower panel shows empty bunch crossings (the scale is
different in the two panels to show differences more clearly). The open
red points in the lower panel lie close to 0, indicating that any residual
PCC response is small in empty bunch slots. The lower plot shows the
estimated residual T1 and T2 afterglow as a function of time during the
full range of 2016 data for both PCC and HFOC, which use the same
afterglow subtraction methodology

## PDF page 21

Eur. Phys. J. C (2021) 81:800

Page 21 of 42 800

5.2 Efficiency corrections

the course of 2015 and 2016. These corrections, amounting to −0.2 to +1.4/(Hz/µb), are derived by comparing with
RAMSES data in five different periods.

Radiation damage can affect the detector response by reducing efficiency, increasing noise, or both. Noise is typically
a small effect for most luminometers, but reduced response
in detectors due to radiation damage can have significant
(percent-level) effects, and so corrections are required. Corrections are measured against a stable benchmark relative to
the performance at or near the vdM scans, and are applied to
σvis . Shifts of 0–10% in detector response in the PLT in 2016
are corrected using RAMSES as a benchmark, whereas the
impact of radiation damage on the HF efficiency is corrected
using a parameterization derived from a model of aging. An
HF efficiency correction of 1% is derived by measuring the
average energy deposits in the HF in events characterized by
the presences of Zbosons that decay to two muons with large
transverse momentum.
A further efficiency correction is necessary for the PCC
measurement. The pixel detector has a static internal memory buffer for data storage before the trigger decision is
taken. When the buffer is filled, the oldest data overflows
and are lost. This effect is proportional to the total instantaneous luminosity, and it can be estimated by studying
the frequency of missing pixel clusters in otherwise wellreconstructed tracks [29]. In 2016, the effect was 1.0%
at 1.4×1034 cm−2 s−1 . A correction proportional to total
instantaneous luminosity is applied, and the total impact on
integrated luminosity is 0.2%. Since the total luminosity in
2015 is substantially lower, no correction is applied. The PCC
also has very small noise corrections.
5.3 Nonlinear response
In the absence of out-of-time pileup, the PCC luminosity is
expected to be linear, according to simulations, so no corrections are applied. Moreover, the ratios of PCC to both DT
and RAMSES luminosity measurements are highly compatible as a function of the instantaneous luminosity without any
corrections. The HFOC response in 2015 and 2016, on the
other hand, exhibits significant nonlinearity compared to the
other luminometers. The main source of nonlinearity is the
uncalibrated ADC-to-charge conversion applied at the time
of data taking. Data from fill 5416, which exhibit a wide range
of instantaneous luminosity, are used to model the correction
for HFOC with a fourth-order polynomial. This smooth function extrapolates to the σvis calibration at low pileup within
uncertainty. This single model is used to correct the nonlinear
behavior of HFOC (0–10% higher response when compared
to PCC) throughout 2016.
As described in Sect. 3, nonlinearity corrections are
also needed for PLT. The corrections are modeled with a
first-order polynomial. The parameters are time dependent,
because of changes in the PLT operating conditions during

6 Detector stability and linearity
After the rate corrections are applied (as discussed in Sect. 5),
comparisons between different luminometers are performed
to assess remaining systematic effects impacting the luminosity measurement. Since PCC is expected to suffer the
least from nonlinearities, as described in Sect. 2.1, once outof-time pileup effects are corrected, PCC is the preferred
luminometer for these data sets in the following estimates
for stability and potential nonlinearity.
6.1 Upper bounds on stability
One measurement of potential instability in the PCC luminosity comes from intrinsic monitoring (i.e., comparing rates
from different sections/parts of the subdetector over time).
In a perfectly stable system, the fractional rates among different subcomponents would exhibit no variation with time.
Figure 16 shows the result of applying out-of-time pileup corrections (as discussed in Sect. 5.1) separately to each pixel
layer or disk. The sum of the per-region corrections matches
the total, nominal correction made for all PCC regions to better than 0.1%. After the corrections are applied, the relative
rates are quite stable over the course of 2015 and 2016. This
is also shown in Fig. 16, where the relative PCC rates over
time are simultaneously fit to a first-order polynomial.
However, this method cannot detect global shifts in σvis ,
and so it is crucial to make comparisons with completely
independent systems. With multiple independent systems
available for comparison, luminometers displaying brief
periods of instability can be clearly identified. The crossdetector comparison is repeated for the entire data set for each
year to detect periods where a single luminometer experiences transient effects (e.g., data quality issues, some detector
components off, anomalous signals, etc.). Figure 17 shows
the ratio of the luminosity measurements for different pairs
of detectors throughout 2016, highlighting (in red) periods
where the ratios significantly deviate from unity and so the
associated data are invalidated.
After the exclusion of invalidated data, which amount to
≲5% for each luminometer, the remaining input from different luminometers is used to assess an upper limit on the
stability of the luminosity. PCC measurements are valid for
98.3 (94.3)% of the data set in 2015 (2016). The rest of the
luminosity is provided by the next most stable luminometer,
which is RAMSES (HFOC) for 2015 (2016). The primary
luminosity, which is PCC or luminosity from the next most
stable detector when PCC is unavailable, is compared with

123

## PDF page 22

Fig. 16 The relative
contribution to the total number
of observed pixel clusters from
the four regions of the pixel
detector used in the luminosity
measurement (barrel layers 2
and 3, and inner and outer
forward pixel disks), as a
function of time throughout
2016. The lines represent
first-order polynomial fits to the
relative contributions from each
region

Eur. Phys. J. C (2021) 81:800

Relative contribution

800 Page 22 of 42

2016 (13 TeV)

CMS
0.34
0.32
0.3
0.28

Barrel layer 2
Barrel layer 3
Forward disk 1
Forward disk 2

0.26
0.24
0.22
0.2
0.18
24/04

01/07

06/09

12/11

Date [Day/Month]
the next-best available luminometer (secondary). In Fig. 18,
the latter is selected using the lowest standard deviation in
the ratio relative to PCC over fixed time intervals of approximately 20 min each. The position of the mean shows the
agreement between the luminometers on the integrated luminosity. The width reflects stability effects, as well as residual
statistical uncertainty in the luminosity measurement in each
interval. From the distribution over the course of each year,
the width is an upper limit on the uncertainty due to time
dependencies in the luminometers. For 2015 (2016) a systematic uncertainty due to detector stability of 0.6 (0.5)% is
derived.

nosity of the 2015 (2016) data set, where the average Lb is
approximately 2.0 (3.3) Hz/µb.
The alternative method makes use of the entire data set
throughout the year, and extracts a single relative slope with
a first-order polynomial fit. To remove effects from variations
in the absolute luminosity scale over time, the per-fill ratios
are shifted such that their extrapolation at zero luminosity
is unity. The results are consistent with the primary method
described above.

6.2 Time dependence of linearity

For each data set, final rate corrections and final calibrations
are applied to data in small time windows of 218 LHC orbits,
approximately 23 s. All the measurements are summed to
derive a total integrated luminosity measurement. The contributions to the systematic uncertainty in the integrated luminosity are divided into two general categories:

We make use of two methods for assessing the detector
linearity. The primary method compares the ratio of the
instantaneous luminosity from two luminometers per fill as
a function of the instantaneous luminosity, which is estimated from the numerator. A first-order polynomial fit is
performed and the slope is extracted. The slopes per fill are
then studied as a function of time. No significant deviation
over time is observed between DT/PCC or RAMSES/PCC
and HFOC/PCC, DT/PCC, or RAMSES/PCC in 2015 and
2016, respectively.
To estimate the uncertainty, the fitted slopes are weighted
according to the per-fill integrated luminosity. The mean values deviate slightly from 0, and the largest deviation is the
systematic uncertainty in the linearity of PCC luminosity.
Figure 19 shows the summary of these slopes for 2015 and
√
2016 at s = 13 TeV both for the whole year, and for subsets
of each data set with equal luminosity. The largest average
slope is 0.26 (0.08)%/(Hz/µb) in 2015 (2016), which translates into a 0.5 (0.3)% uncertainty in the integrated lumi-

123

7 Total luminosity correction and uncertainty

– “normalization” uncertainty in the absolute luminosity
scale, σvis , determined from the vdM scan procedure
– “integration” uncertainty associated with σvis variations
over time (stability) and pileup (linearity and out-of-time
pileup corrections).
The magnitudes of the corrections applied to the absolute normalization from the vdM calibration are listed in Table 3, and
Table 4 summarizes the sources of uncertainty. The dominant
sources of normalization uncertainty are associated with the
beam position monitoring (as discussed in Sect. 4.3.2), transverse factorizability (as explained in Sect. 4.4), and beambeam effects (as described in Sect. 4.3.3).

## PDF page 23

Fig. 17 The luminosity
measurements from PCC,
HFOC, and RAMSES are
compared as a function of the
integrated luminosity in 2016.
Comparison among three
luminometers facilitates the
identification of periods where a
single luminometer suffers from
transient stability issues. The
ratios that are plotted in red
contain invalidated data. The
dashed line delineates the vdM
calibration (fill 4954)

Page 23 of 42 800

Ratio of integrated luminosity

Eur. Phys. J. C (2021) 81:800

CMS

1.05

2016 (13 TeV)
RAMSES/PCC
RAMSES/PCC (invalidated)

1.04

HFOC/PCC
HFOC/PCC (invalidated)

1.03
1.02
1.01
1
0.99
0.98
0.97

0

5

10

15

20

25

30

35

Integrated luminosity [fb-1]

Fig. 18 The ratio of the primary (best available) to secondary (nextbest available) luminosity as computed in time windows of approximately 20 min each. The left plot shows the 2015 results (principally

PCC/RAMSES), and the right plot shows the 2016 results (principally
PCC/HFOC). Each entry is weighted by the integrated luminosity for
the time period

The dominant sources of integration uncertainty arise
from the linearity and stability of the primary relative to
secondary luminosity measurements over the course of each
year (as discussed in Sect. 6). In addition, the subleading systematic uncertainty due to out-of-time pileup corrections is
considered for the PCC method since it is primarily used for
the luminosity estimate.
Several sources of normalization uncertainty are considered to be correlated for the years studied because the scan
procedures and analysis methodology are identical between
the two vdM calibrations. The sources of the normalization
uncertainty that are not correlated between the two vdM programs, and are partly statistical in nature, are the orbit drift,

along with the scan-to-scan and bunch-to-bunch variations
in the measured σvis . The latter are collectively referred to as
“other variations in σvis ” in Table 4.
Among the sources of integration uncertainty, the afterglow corrections are treated identically in the two data sets,
and so this source of systematic uncertainty is correlated. The
estimate of the uncertainty due to linearity is considered to be
correlated, since it is derived from the PCC linearity in both
years. On the other hand, the stability assessment is based on
cross-detector comparisons. Although PCC is the primary
luminometer in each data set, the secondary luminometer is
different for each year. Since the source of instability can-

123

## PDF page 24

800 Page 24 of 42

Eur. Phys. J. C (2021) 81:800
Table 3 Summary of the BCID-averaged √
corrections to σvis (in %)
obtained with the vdM scan calibrations at s = 13 TeV in 2015 and
2016. When a range is shown, it is because of possible scan-to-scan
variations. To obtain the impact on σvis , each correction is consecutively
included, the fits are redone following the order below, and the result is
compared with the baseline. The impact from transverse factorizability
is obtained separately (as discussed in Sect. 4.4)
Source

√
Fig. 19 Linearity summary for 2015 (upper) and 2016 (lower) at s =
13 TeV. The slopes are plotted for each detector relative to PCC. The
markers are averages of fill-by-fill slopes from fits binned in roughly
equal fractions of the total integrated luminosity through the year. The
error bars on the markers are the propagated statistical uncertainty from
fitted slope parameters in each fill, which are weighted by integrated
luminosities of each fill. The dashed lines and corresponding hatched
areas show the average from the entire data set and its uncertainty

not be assessed and contains time-dependent features, the
uncertainty is not correlated.
The tool used for providing luminosity values to physics
analyses applies the corrections to the raw luminosity values
using the average per-bunch luminosity, rather than the individual bunch-by-bunch values. This potentially introduces an
error in the case where these corrections include a nonlinear
term and the bunch-by-bunch luminosity varies significantly
among bunches. We evaluated the effect of this approximation on 2016 data, and found that the overall impact on the
integrated luminosity was <0.1%.

123

Impact on σvis (%)
2015

2016

Ghost and satellite charge

+0.2

+0.3

Orbit drift

+0.6 to +1.0

+0.2 to +1.0

Residual beam position corrections

−0.6 to +0.4

−0.5 to −0.2

Beam-beam effects

+0.6

+0.4

Length scale calibration

−0.4

−1.3

Transverse factorizability

+0.8 to +1.3

+0.6

Finally, the quantity measured by the luminometers is the
luminosity delivered to CMS; however, the quantity of interest to most physics analyses is the luminosity corresponding
to the data actually recorded by the CMS DAQ system. These
are related by the deadtime, as obtained from the trigger and
clock system of CMS [21]. In 2015 this measurement was
affected by an algorithm issue in the trigger system and has
an uncertainty of 0.5%, but this problem was resolved before
data taking began in 2016, so in 2016 the impact is negligible
(<0.1%) and uncorrelated with 2015.
When applying the vdM calibration to the entire periods,
the total integrated luminosity is 2.27 fb−1 with a relative
precision of 1.6% in 2015, and 36.3 fb−1 with a relative precision of 1.2% in 2016. The combined 2015 + 2016 luminosity measurement has a precision of 1.2%, which is the same
as the 2016 precision since it is the significantly larger data
set and the precision in 2015 is similar.

8 Summary
The luminosity calibration using beam-separation (van der
Meer, vdM) scans has been presented for data from proton–
proton collisions recorded by the CMS experiment in 2015
and 2016 when all subdetectors were fully operational. The
main sources of systematic uncertainty are related to residual differences between the measured beam positions and the
ones provided by the operational settings of the LHC magnets, the factorizability of the transverse spatial distributions
of proton bunches, and the modeling of effects on the proton distributions due to electromagnetic interactions among
protons in the colliding bunches. When applying the vdM
calibration to the entire data-taking period, the relative stability and linearity of luminosity subdetectors (luminometers)

## PDF page 25

Eur. Phys. J. C (2021) 81:800

Page 25 of 42 800

Table 4 Summary of√contributions to the relative systematic uncertainty in σvis (in %) at s = 13 TeV in 2015 and 2016. The systematic
uncertainty is divided into groups affecting the description of the vdM
profile and the bunch population product measurement (normalization),
and the measurement of the rate in physics running conditions (integration). The fourth column indicates whether the
√sources of uncertainty
are correlated between the two calibrations at s = 13 TeV
Source

2015 (%)

2016 (%)

Corr

Ghost and satellite charge

0.1

0.1

Yes

Beam current normalization

0.2

0.2

Yes

Orbit drift

0.2

0.1

No

Residual differences

0.8

0.5

Yes

Normalization uncertainty
Bunch population

Beam position monitoring

Beam overlap description
Beam-beam effects

0.5

0.5

Yes

Length scale calibration

0.2

0.3

Yes

Transverse factorizability

0.5

0.5

Yes

0.6

0.3

No

Type 1 corrections

0.3

0.3

Yes

Type 2 corrections

0.1

0.3

Yes

Cross-detector stability

0.6

0.5

No

Linearity

0.5

0.3

Yes

CMS deadtime

0.5

< 0.1

No

Total normalization uncertainty

1.3

1.0

–

Total integration uncertainty

1.0

0.7

–

Total uncertainty

1.6

1.2

–

Result consistency
Other variations in σvis
Integration uncertainty
Out-of-time pileup corrections

Detector performance

Data acquisition

are included in the uncertainty in the integrated luminosity
measurement as well.
The resulting relative precision in the calibration from the
√
vdM scans is 1.3 (1.0)% in 2015 (2016) at s = 13 TeV; the
integration uncertainty due to luminometer-specific effects
contributes 1.0 (0.7)%, resulting in a total uncertainty of
1.6 (1.2)%; when applying the vdM calibration to the entire
periods, the total integrated luminosity is 2.27 (36.3) fb−1 .
The final precision is among the best achieved at bunchedbeam hadron colliders. Advanced techniques are used to
estimate and correct for the bias associated with the beam
position monitoring at the scale of µm, the factorizability of
the transverse beam distribution, and beam-beam effects. In
addition, detailed luminometer rate corrections and the inclusion of novel measurements (such as the data from the Radiation Monitoring System for the Environment and Safety)

lead to precise estimates of the stability and linearity over
time.
In the coming years, a similarly precise calibration of
the real-time luminosity delivered to the LHC will become
increasingly important for standard operations. Under those
conditions, the impact of out-of-time pileup effects is
expected to be larger, but in principle they can be mitigated
using techniques described in this paper.
Acknowledgements Bundes-ministerium Forschungs-gemeinschaft
Forschungs-zentren Rachada-pisek We congratulate our colleagues in
the CERN accelerator departments for the excellent performance of
the LHC machine. We thank all contributors to the LHC Luminosity
Calibration and Monitoring Working Group and, in particular, its cocoordinator Witold Kozanecki for the discussions on beam instrumentation and beam physics. We also thank the technical and administrative
staffs at CERN and at other CMS institutes for their contributions to
the success of the CMS effort. In addition, we gratefully acknowledge
the computing c enters and personnel of the Worldwide LHC Computing Grid and other centers for delivering so effectively the computing
infrastructure essential to our analyses. Finally, we acknowledge the
enduring support for the construction and operation of the LHC, the
CMS detector, and the supporting computing infrastructure provided by
the following funding agencies: the Austrian Federal Ministry of Education, Science and Research and the Austrian Science Fund; the Belgian
Fonds de la Recherche Scientifique, and Fonds voor Wetenschappelijk
Onderzoek; the Brazilian Funding Agencies (CNPq, CAPES, FAPERJ,
FAPERGS, and FAPESP); the Bulgarian Ministry of Education and Science; CERN; the Chinese Academy of Sciences, Ministry of Science
and Technology, and National Natural Science Foundation of China;
the Ministerio de Ciencia Tecnología e Innovación (MINCIENCIAS),
Colombia; the Croatian Ministry of Science, Education and Sport, and
the Croatian Science Foundation; the Research and Innovation Foundation, Cyprus; the Secretariat for Higher Education, Science, Technology
and Innovation, Ecuador; the Ministry of Education and Research, Estonian Research Council via PRG780, PRG803 and PRG445 and European Regional Development Fund, Estonia; the Academy of Finland,
Finnish Ministry of Education and Culture, and Helsinki Institute of
Physics; the Institut National de Physique Nucléaire et de Physique des
Particules/CNRS, and Commissariat à l’Énergie Atomique et aux Énergies Alternatives/CEA, France; the Bundesministerium für Bildung
und Forschung, the Deutsche Forschungsgemeinschaft (DFG), under
Germany’s Excellence Strategy – EXC 2121 “Quantum Universe” –
390833306, and under project number 400140256 - GRK2497, and
Helmholtz-Gemeinschaft Deutscher Forschungszentren, Germany; the
General Secretariat for Research and Technology, Greece; the National
Research, Development and Innovation Fund, Hungary; the Department of Atomic Energy and the Department of Science and Technology, India; the Institute for Studies in Theoretical Physics and Mathematics, Iran; the Science Foundation, Ireland; the Istituto Nazionale di
Fisica Nucleare, Italy; the Ministry of Science, ICT and Future Planning, and National Research Foundation (NRF), Republic of Korea;
the Ministry of Education and Science of the Republic of Latvia; the
Lithuanian Academy of Sciences; the Ministry of Education, and University of Malaya (Malaysia); the Ministry of Science of Montenegro; the Mexican Funding Agencies (BUAP, CINVESTAV, CONACYT, LNS, SEP, and UASLP-FAI); the Ministry of Business, Innovation and Employment, New Zealand; the Pakistan Atomic Energy
Commission; the Ministry of Science and Higher Education and the
National Science Center, Poland; the Fundação para a Ciência e a Tecnologia, Portugal; JINR, Dubna; the Ministry of Education and Science of the Russian Federation, the Federal Agency of Atomic Energy
of the Russian Federation, Russian Academy of Sciences, the Russian Foundation for Basic Research, and the National Research Center

123

## PDF page 26

800 Page 26 of 42
“Kurchatov Institute”; the Ministry of Education, Science and Technological Development of Serbia; the Secretaría de Estado de Investigación, Desarrollo e Innovación, Programa Consolider-Ingenio 2010,
Plan Estatal de Investigación Científica y Técnica y de Innovación 2017–
2020, research project IDI-2018-000174 del Principado de Asturias,
and Fondo Europeo de Desarrollo Regional, Spain; the Ministry of Science, Technology and Research, Sri Lanka; the Swiss Funding Agencies
(ETH Board, ETH Zurich, PSI, SNF, UniZH, Canton Zurich, and SER);
the Ministry of Science and Technology, Taipei; the Thailand Center
of Excellence in Physics, the Institute for the Promotion of Teaching
Science and Technology of Thailand, Special Task Force for Activating Research and the National Science and Technology Development
Agency of Thailand; the Scientific and Technical Research Council of
Turkey, and Turkish Atomic Energy Authority; the National Academy
of Sciences of Ukraine; the Science and Technology Facilities Council, UK; the US Department of Energy, and the US National Science
Foundation. Individuals have received support from the Marie-Curie
program and the European Research Council and Horizon 2020 Grant,
contract nos. 675440, 724704, 752730, 765710, and 824093 (European
Union); the Leventis Foundation; the Alfred P. Sloan Foundation; the
Alexander von Humboldt Foundation; the Belgian Federal Science Policy Office; the Fonds pour la Formation à la Recherche dans l’Industrie
et dans l’Agriculture (FRIA-Belgium); the Agentschap voor Innovatie
door Wetenschap en Technologie (IWT-Belgium); the F.R.S.-FNRS and
FWO (Belgium) under the “Excellence of Science – EOS” – be.h project
n. 30820817; the Beijing Municipal Science and Technology Commission, no. Z191100007219010; the Ministry of Education, Youth and
Sports (MEYS) of the Czech Republic; the Lendület (“Momentum”)
Program and the János Bolyai Research Scholarship of the Hungarian
Academy of Sciences, the New National Excellence Program ÚNKP,
the NKFIA research grants 123842, 123959, 124845, 124850, 125105,
128713, 128786, and 129058 (Hungary); the Council of Scientific
and Industrial Research, India; the National Science Center (Poland),
contracts Opus 2014/15/B/ST2/03998 and 2015/19/B/ST2/02861; the
National Priorities Research Program by Qatar National Research Fund;
the Ministry of Science and Higher Education, project no. 0723-20200041 (Russia); the Programa de Excelencia María de Maeztu, and
the Programa Severo Ochoa del Principado de Asturias; the Thalis
and Aristeia programs cofinanced by EU-ESF, and the Greek NSRF;
the Rachadapisek Sompot Fund for Postdoctoral Fellowship, Chulalongkorn University, and the Chulalongkorn Academic into Its 2nd Century Project Advancement Project (Thailand); the Kavli Foundation; the
Nvidia Corporation; the SuperMicro Corporation; the Welch Foundation, contract C-1845; and the Weston Havens Foundation (USA).
Data Availability Statement This manuscript has no associated data
or the data will not be deposited. [Authors’ comment: Release and
preservation of data used by the CMS Collaboration as the basis
for publications is guided by the CMS policy as written in its
document “CMS data preservation, re-use and open access policy”
(https://cms-docdb.cern.ch/cgi-bin/PublicDocDB/RetrieveFile?docid=
6032\&filename=CMSDataPolicyV1.2.pdf\&version=2).]
Declarations

Conflict of interest The authors declare that they have no conflict of
interest.
Open Access This article is licensed under a Creative Commons Attribution 4.0 International License, which permits use, sharing, adaptation,
distribution and reproduction in any medium or format, as long as you
give appropriate credit to the original author(s) and the source, provide a link to the Creative Commons licence, and indicate if changes
were made. The images or other third party material in this article

123

Eur. Phys. J. C (2021) 81:800
are included in the article’s Creative Commons licence, unless indicated otherwise in a credit line to the material. If material is not
included in the article’s Creative Commons licence and your intended
use is not permitted by statutory regulation or exceeds the permitted use, you will need to obtain permission directly from the copyright holder. To view a copy of this licence, visit http://creativecomm
ons.org/licenses/by/4.0/.
Funded by SCOAP3 .

References
1. P. Grafström, W. Kozanecki, Luminosity determination at proton
colliders. Prog. Part. Nucl. Phys. 81, 97 (2015). https://doi.org/10.
1016/j.ppnp.2014.11.002
2. ATLAS and CMS Collaborations, Addendum to the report on the
physics at the HL-LHC, and perspectives for the HE-LHC: collection of notes from ATLAS and CMS. CERN (2019). https://doi.
org/10.23731/CYRM-2019-007.Addendum. arXiv:1902.10229
3. CMS Collaboration, The CMS experiment at the CERN LHC.
JINST 3, S08004 (2008). https://doi.org/10.1088/1748-0221/3/08/
S08004
4. CMS Collaboration, Measurement of the differential cross sections
for the associated production
of a W boson and jets in proton–
√
proton collisions at s = 13 TeV. Phys. Rev. D 96, 072005 (2017).
https://doi.org/10.1103/PhysRevD.96.072005. arXiv:1707.05979
5. CMS Collaboration, Measurement of the differential
Drell–Yan
√
cross section in proton–proton collisions at s = 13 TeV.
JHEP 12, 059 (2019). https://doi.org/10.1007/JHEP12(2019)059.
arXiv:1812.10529
6. CMS Collaboration, Measurement of the t t̄ production cross section
√using events with one lepton and at least one jet in pp collisions
at s = 13 TeV. JHEP 09, 051 (2017). https://doi.org/10.1007/
JHEP09(2017)051. arXiv:1701.06228
7. CMS Collaboration, Measurement of the t t̄ production cross section, the top quark mass, and the strong
coupling constant using
√
dilepton events in pp collisions at s = 13 TeV. Eur. Phys. J. C
79, 368 (2019). https://doi.org/10.1140/epjc/s10052-019-6863-8.
arXiv:1812.10505
8. M. Hostettler et al., Luminosity scans for beam diagnostics. Phys.
Rev. Accel. Beams 21, 102801 (2018). https://doi.org/10.1103/
PhysRevAccelBeams.21.102801. arXiv:1804.10099
9. F. Antoniou et al., Can we predict luminosity?, in Proceedings of
the 7th Evian Workshop on LHC Beam Operation, p. 125 (2016).
http://cds.cern.ch/record/2293678
10. S. van der Meer, Calibration of the effective beam height in the
ISR. ISR Report CERN-ISR-PO-68-31 (1968). https://cds.cern.ch/
record/296752
11. C. Rubbia, Measurement of the luminosity of pp̄ collider with a
(generalized) van der Meer method. CERN pp̄ Note 38 (1977).
https://cds.cern.ch/record/1025746
12. LHCb Collaboration, Precision luminosity measurements at LHCb.
JINST 9, P12005 (2014). https://doi.org/10.1088/1748-0221/9/12/
P12005. arXiv:1410.0149
13. ATLAS √
Collaboration, Luminosity determination in pp collisions at s = 8 TeV using the ATLAS detector at the LHC.
Eur. Phys. J. C 76, 653 (2016). https://doi.org/10.1140/epjc/
s10052-016-4466-1. arXiv:1608.03953
14. L. Evans, P. Bryant, LHC machine. JINST 3, S08001 (2008).
https://doi.org/10.1088/1748-0221/3/08/S08001
15. B. Salvachua, Overview of proton–proton physics during Run 2, in
Proceedings of the 9th Evian Workshop on LHC Beam Operation
(2019), p. 7. http://cds.cern.ch/record/2750272

## PDF page 27

Eur. Phys. J. C (2021) 81:800
16. J. Boyd, C. Schwick, Experiments—experience and future, in Proceedings of the 7th Evian Workshop on LHC Beam Operation
(2017), p. 229. https://cds.cern.ch/record/2293538
17. CMS Collaboration, Measurement of the double-differential
inclu√
sive jet cross section in proton–proton collisions at s = 13 TeV.
Eur. Phys. J. C 76, 451 (2016). https://doi.org/10.1140/epjc/
s10052-016-4286-3. arXiv:1605.04436
18. P. Skands, S. Carrazza, J. Rojo, Tuning PYTHIA 8.1: the Monash
2013 tune. Eur. Phys. J. C 74, 3024 (2014). https://doi.org/10.1140/
epjc/s10052-014-3024-y. arXiv:1404.5630
19. T. Sjöstrand et al., An introduction to PYTHIA 8.2. Comput. Phys.
Commun. 191, 159 (2015). https://doi.org/10.1016/j.cpc.2015.01.
024. arXiv:1410.3012
20. CMS Collaboration, Performance of the CMS muon detector
√ and muon reconstruction with proton–proton collisions at
s = 13 TeV. JINST 13, P06015 (2018). https://doi.org/10.1088/
1748-0221/13/06/p06015. arXiv:1804.04528
21. CMS Collaboration, The CMS trigger system. JINST 12,
P01020
(2017).
https://doi.org/10.1088/1748-0221/12/01/
P01020. arXiv:1609.02366
22. A.J. Bell, Beam and radiation monitoring for CMS, in Proceedings,
2008 IEEE Nuclear Science Symposium (2008), p. 2322. https://
doi.org/10.1109/NSSMIC.2008.4774822
23. P. Lujan, Performance of the Pixel Luminosity Telescope for luminosity measurement at CMS during Run 2. PoS 314, 504 (2017).
https://doi.org/10.22323/1.314.0504
24. M. Hempel, Development of a novel diamond based detector for machine induced background and luminosity measurements. PhD thesis, Brandenburg University of Technology CottbusSenftenberg, 2017. DESY-THESIS-2017-030. https://doi.org/10.
3204/PUBDB-2017-06875
25. CMS Collaboration, CMS technical design report for the level1 trigger upgrade. CMS Technical Design Report CERNLHCC-2013-011, CMS-TDR-012 (2013). https://cds.cern.ch/
record/1556311
26. CMS Collaboration, Event generator tunes obtained from underlying event and multiparton scattering measurements. Eur. Phys. J. C
76, 155 (2016). https://doi.org/10.1140/epjc/s10052-016-3988-x.
arXiv:1512.00815
27. Geant4 Collaboration, Geant4—a simulation toolkit. Nucl.
Instrum. Methods A 506, 250 (2003). https://doi.org/10.1016/
S0168-9002(03)01368-8
28. W. Verkerke, D.P. Kirkby, The RooFit toolkit for data modeling, in Proceedings of the 13th International Conference for
Computing in High-Energy and Nuclear Physics (CHEP03)
(2003), p. MOLT007. arXiv:physics/0306116. http://inspirehep.
net/literature/621398
29. CMS Collaboration, Description and performance of track and
primary-vertex reconstruction with the CMS tracker. JINST 9,
P10009 (2014). https://doi.org/10.1088/1748-0221/9/10/P10009.
arXiv:1405.6569
30. G. Segura Millan, D. Perrin, L. Scibile, RAMSES: the LHC
radiation monitoring system for the environment and safety, in
Proceedings of the 10th International Conference on Accelerator and Large Experimental Physics Control Systems (ICALEPCS
2005) (2005). TH3B.1-3O. https://accelconf.web.cern.ch/ica05/
proceedings/pdf/O4_011.pdf
31. A. Ledeul et al., CERN supervision, control, and data acquisition system for radiation and environmental protection, in
Proceedings of the 12th International Workshop on Emerging Technologies and Scientific Facilities Controls (PCaPAC’18) (2019), p. 248 (FRCC3). https://doi.org/10.18429/
JACoW-PCaPAC2018-FRCC3
32. J. Salfeld-Nebgen, D. Marlow, Data-driven precision luminosity measurements with Z bosons at the LHC and HL-LHC.

Page 27 of 42 800
JINST 13, P12016 (2018). https://doi.org/10.1088/1748-0221/13/
12/P12016. arXiv:1806.02184
33. O.S. Brüning et al., LHC design report vol. 1: the LHC main ring.
CERN (2004). https://doi.org/10.5170/CERN-2004-003-V-1
34. M. Hostettler, LHC luminosity performance. PhD thesis, University of Bern. CERN-THESIS-2018-051 (2018). https://cds.cern.
ch/record/2319396
35. C. Barschel et al., Results of the LHC DCCT calibration studies. Technical Report CERN-ATS-Note-2012-026 PERF (2012).
https://cds.cern.ch/record/1425904
36. D. Belohrad et al., The LHC fast BCT system: a comparison
of design parameters with initial performance. Technical Report
CERN-BE-2010-010 (2010). https://cds.cern.ch/record/1267400
37. A. Jeff et al., Longitudinal density monitor for the LHC. Phys.
Rev. ST Accel. Beams 15, 032803 (2012). https://doi.org/10.1103/
PhysRevSTAB.15.032803
38. A. Jeff, A longitudinal density monitor for the LHC. PhD thesis,
University of Liverpool. CERN-THESIS-2012-240 (2012). https://
cds.cern.ch/record/1513180
39. G. Papotti, T. Bohl, F. Follin, U. Wehrle, Longitudinal beam
measurements at the LHC: the LHC Beam Quality Monitor,
in Proceedings, 2nd International Particle Accelerator Conference (IPAC 2011) (2011), p. 1852 (TUPZ022). https://cds.cern.
ch/record/1399087
40. M. Gasior, J. Olexa, R. Steinhagen, BPM electronics based on
compensated diode detectors—results from development systems,
in Proceedings of the 2012 Beam Instrumentation Workshop
(BIW’12). (2012), p. 44 (MOPG010). https://cds.cern.ch/record/
1476070
41. T. Persson et al., LHC optics corrections in Run 2, in Proceedings,
9th Evian Workshop on LHC Beam Operation. (2019), p. 59. https://
cds.cern.ch/record/2750277
42. M. Gasior, G. Baud, J. Olexa, G. Valentino, First operational experience with the LHC Diode ORbit and OScillation (DOROS) system, in Proceedings of the 5th International Beam Instrumentation
Conference (IBIC 2016) (2017), p. 43 (MOPG07). https://doi.org/
10.18429/JACoW-IBIC2016-MOPG07
43. H. Bartosik, G. Rumolo, Production of the single bunch for van
der Meer scans in the LHC injector chain. CERN Accelerator
Note CERN-ACC-NOTE-2013-0008 (2013). https://cds.cern.ch/
record/1590405
44. V. Balagura, Van der Meer scan luminosity measurement and
beam–beam correction. Eur. Phys. J. C 81, 26 (2021). https://doi.
org/10.1140/epjc/s10052-021-08837-y. arXiv:2012.07752
45. A. Babaev et al., Impact of beam-beam effects on absolute luminosity calibrations at the CERN Large Hadron Collider. Phys. Rev.
ST Accel. Beams (2021) (to be submitted)
46. C. Barschel, Precision luminosity measurement at LHCb with
beam–gas imaging. PhD thesis, RWTH Aachen University (2014).
CERN-THESIS-2013-301. https://cds.cern.ch/record/1693671
47. G. Coombs, M. Ferro-Luzzi, R. Matev, Beam–gas imaging measurements at LHCb, in Proceedings, 7th International Beam Instrumentation Conference (IBIC 2018) (2019), p. 459 (WEPB13).
https://doi.org/10.18429/JACoW-IBIC2018-WEPB13
48. W. Kozanecki, T. Pieloni, J. Wenninger, Observation of beam–
beam deflections with LHC orbit data. CERN Accelerator
Note CERN-ACC-NOTE-2013-0006 (2013). https://cds.cern.ch/
record/1581723
49. S.M. White, Determination of the absolute luminosity at the LHC.
PhD thesis, Université Paris-Sud 11. CERN-THESIS-2010-139,
LAL-10-154 (2010). https://cdsweb.cern.ch/record/1308187
50. M. Klute, C. Medlock, J. Salfeld-Nebgen, Beam imaging and luminosity calibration. JINST 12, P03018 (2017). https://doi.org/10.
1088/1748-0221/12/03/P03018. arXiv:1603.03566
51. J. Knolle, Measuring luminosity and the t t̄Z production cross
section with the CMS experiment. PhD thesis, Universität Ham-

123

## PDF page 28

800 Page 28 of 42

Eur. Phys. J. C (2021) 81:800

CMS Collaboration
Yerevan Physics Institute, Yerevan, Armenia
A. M. Sirunyan † , A. Tumasyan
Institut für Hochenergiephysik, Vienna, Austria
W. Adam , J. W. Andrejkovic, T. Bergauer, S. Chatterjee, M. Dragicevic , A. Escalante Del Valle , R. Frühwirth 1 ,
M. Jeitler 1 , N. Krammer, L. Lechner, D. Liko, I. Mikulec, F. M. Pitters, J. Schieck 1 , R. Schöfbeck , M. Spanring,
S. Templ, W. Waltenberger , C.-E. Wulz 1
Institute for Nuclear Problems, Minsk, Belarus
V. Chekhovsky, A. Litomin, V. Makarenko
Universiteit Antwerpen, Antwerp, Belgium
M. R. Darwish 2 , E. A. De Wolf, X. Janssen , T. Kello 3 , A. Lelek, H. Rejeb Sfar, P. Van Mechelen, S. Van Putte,
N. Van Remortel
Vrije Universiteit Brussel, Brussels, Belgium
F. Blekman , E. S. Bols , J. D’Hondt , J. De Clercq , M. Delcourt, S. Lowette
D. Müller, A. R. Sahasransu , S. Tavernier, W. Van Doninck, P. Van Mulders

, S. Moortgat

, A. Morton

Université Libre de Bruxelles, Brussels, Belgium
D. Beghin, B. Bilin , B. Clerbaux , G. De Lentdecker, L. Favart , A. Grebenyuk, A. K. Kalsi , K. Lee,
M. Mahdavikhorrami, I. Makarenko , L. Moureaux, L. Pétré, A. Popov , N. Postiau, E. Starling , L. Thomas
M. Vanden Bemden, C. Vander Velde , P. Vanlaer , D. Vannerom, L. Wezenbeek
Ghent University, Ghent, Belgium
T. Cornelis , D. Dobur, M. Gruchala, G. Mestdach, M. Niedziela, C. Roskas, K. Skovpen
B. Vermassen, M. Vit

,

,

, M. Tytgat

, W. Verbeke,

Université Catholique de Louvain, Louvain-la-Neuve, Belgium
A. Bethani , G. Bruno, F. Bury, C. Caputo , P. David , C. Delaere , I. S. Donertas, A. Giammanco
K. Mondal, J. Prisciandaro, A. Taliercio, M. Teklishyn, P. Vischia , S. Wertz , S. Wuyckens

, V. Lemaitre,

Centro Brasileiro de Pesquisas Fisicas, Rio de Janeiro, Brazil
G. A. Alves , C. Hensel, A. Moraes
Universidade do Estado do Rio de Janeiro, Rio de Janeiro, Brazil
W. L. Aldá Júnior , M. Barroso Ferreira Filho, H. Brandao Malbouisson, W. Carvalho , J. Chinellato 4 ,
E. M. Da Costa , G. G. Da Silveira 5 , D. De Jesus Damiao , S. Fonseca De Souza , D. Matos Figueiredo,
C. Mora Herrera , K. Mota Amarilo, L. Mundim , H. Nogima, P. Rebello Teles , L. J. Sanchez Rosas, A. Santoro,
S. M. Silva Do Amaral , A. Sznajder , M. Thiel, F. Torres Da Silva De Araujo, A. Vilela Pereira
Universidade Estadual Paulistaa , Universidade Federal do ABCb , São Paulo, Brazil
C. A. Bernardes a , L. Calligaris a , T. R. Fernandez Perez Tomei a , E. M. Gregores a ,b , D. S. Lemos
P. G. Mercadante a ,b , S. F. Novaes a , Sandra S. Padula a

a,

Institute for Nuclear Research and Nuclear Energy, Bulgarian Academy of Sciences, Sofia, Bulgaria
A. Aleksandrov, G. Antchev, I. Atanasov, R. Hadjiiska, P. Iaydjiev, M. Misheva, M. Rodozov, M. Shopova, G. Sultanov
University of Sofia, Sofia, Bulgaria
A. Dimitrov, T. Ivanov, L. Litov , B. Pavlov, P. Petkov, A. Petrov
Beihang University, Beijing, China
T. Cheng, W. Fang 3 , Q. Guo, T. Javaid 6 , M. Mittal, H. Wang, L. Yuan
Department of Physics, Tsinghua University, Beijing, China
M. Ahmad, G. Bauer, C. Dozen 7 , Z. Hu , J. Martins 8 , Y. Wang, K. Yi 9,10

123

## PDF page 29

Eur. Phys. J. C (2021) 81:800

Page 29 of 42 800

Institute of High Energy Physics, Beijing, China
E. Chapon , G. M. Chen 6 , H. S. Chen 6 , M. Chen , A. Kapoor , D. Leggat, H. Liao, Z.-A. LIU
A. Spiezia, J. Tao , J. Thomas-Wilsker, J. Wang, H. Zhang, S. Zhang 6 , J. Zhao

6 , R. Sharma

State Key Laboratory of Nuclear Physics and Technology, Peking University, Beijing, China
A. Agapitos, Y. Ban, C. Chen, Q. Huang, A. Levin , Q. Li , M. Lu, X. Lyu, Y. Mao, S. J. Qian, D. Wang
J. Xiao

, Q. Wang

,

,

Sun Yat-Sen University, Guangzhou, China
Z. You
Institute of Modern Physics and Key Laboratory of Nuclear Physics and Ion-beam Application (MOE)-Fudan
University, Shanghai, China
X. Gao 3 , H. Okawa
Zhejiang University, Hangzhou, China
M. Xiao
Universidad de Los Andes, Bogotá, Colombia
C. Avila , A. Cabrera, C. Florez , J. Fraga, A. Sarkar, M. A. Segura Delgado
Universidad de Antioquia, Medellín, Colombia
J. Jaramillo, J. Mejia Guisao, F. Ramirez, J. D. Ruiz Alvarez

, C. A. Salazar González, N. Vanegas Arbelaez

Faculty of Electrical Engineering, Mechanical Engineering and Naval Architecture, University of Split, Split, Croatia
D. Giljanovic, N. Godinovic , D. Lelas, I. Puljak
Faculty of Science, University of Split, Split, Croatia
Z. Antunovic, M. Kovac, T. Sculac
Institute Rudjer Boskovic, Zagreb, Croatia
V. Brigljevic , D. Ferencek , D. Majumder
University of Cyprus, Nicosia, Cyprus
A. Attikis, E. Erodotou, A. Ioannou, G. Kole
P. A. Razis, H. Rykaczewski, H. Saka

, M. Roguljic, A. Starodumov 11 , T. Susa
, M. Kolosova, S. Konstantinou, J. Mousa

, C. Nicolaou, F. Ptochos

,

Charles University, Prague, Czech Republic
M. Finger 12 , M. Finger Jr. 12 , A. Kveton
Escuela Politecnica Nacional, Quito, Ecuador
E. Ayala
Universidad San Francisco de Quito, Quito, Ecuador
E. Carrera Jarrin
Academy of Scientific Research and Technology of the Arab Republic of Egypt, Egyptian Network of High Energy
Physics, Cairo, Egypt
S. Abu Zeid 13 , S. Khalil 14 , E. Salama 13,15
Center for High Energy Physics (CHEP-FU), Fayoum University, El-Fayoum, Egypt
M. A. Mahmoud , Y. Mohammed
National Institute of Chemical Physics and Biophysics, Tallinn, Estonia
S. Bhowmik , A. Carvalho Antunes De Oliveira , R. K. Dewanjee , K. Ehataht, M. Kadastik, J. Pata, M. Raidal
C. Veelken

,

Department of Physics, University of Helsinki, Helsinki, Finland
P. Eerola , L. Forthomme , H. Kirschenmann , K. Osterberg, M. Voutilainen

123

## PDF page 30

800 Page 30 of 42

Eur. Phys. J. C (2021) 81:800

Helsinki Institute of Physics, Helsinki, Finland
E. Brücken, F. Garcia, J. Havukainen, V. Karimäki, M. S. Kim, R. Kinnunen, T. Lampén, K. Lassila-Perini, S. Lehti,
T. Lindén, H. Siikonen, E. Tuominen , J. Tuominiemi
Lappeenranta University of Technology, Lappeenranta, Finland
P. Luukka , H. Petrow, T. Tuuva
IRFU, CEA, Université Paris-Saclay, Gif-sur-Yvette, France
C. Amendola , M. Besancon, F. Couderc , M. Dejardin, D. Denegri, J. L. Faure, F. Ferri , S. Ganjour, A. Givernaud,
P. Gras, G. Hamel de Monchenault , P. Jarry, B. Lenzi, E. Locci, J. Malcles, J. Rander, A. Rosowsky, M. Ö. Sahin ,
A. Savoy-Navarro 16 , M. Titov , G. B. Yu
Laboratoire Leprince-Ringuet, CNRS/IN2P3, Ecole Polytechnique, Institut Polytechnique de Paris, Palaiseau,
France
S. Ahuja , F. Beaudette , M. Bonanomi, A. Buchot Perraguin, P. Busson, C. Charlot, O. Davignon, B. Diab,
G. Falmagne, S. Ghosh, R. Granier de Cassagnac , A. Hakimi, I. Kucher , A. Lobanov , M. Nguyen , C. Ochando,
P. Paganini , J. Rembser, R. Salerno , J. B. Sauvan , Y. Sirois , A. Zabi, A. Zghiche
Université de Strasbourg, CNRS, IPHC UMR 7178, Strasbourg, France
J.-L. Agram 17 , J. Andrea, D. Apparu, D. Bloch , G. Bourgatte, J.-M. Brom, E. C. Chabert, C. Collard
J.-C. Fontaine 17 , U. Goerlach, C. Grimault, A.-C. Le Bihan, P. Van Hove

, D. Darej,

Institut de Physique des 2 Infinis de Lyon (IP2I ), Villeurbanne, France
E. Asilar , S. Beauceron , C. Bernet, G. Boudoul, C. Camen, A. Carle, N. Chanon , D. Contardo, P. Depasse
H. El Mamouni, J. Fay, S. Gascon, M. Gouzevitch, B. Ille, Sa. Jain , I. B. Laktineh, H. Lattaud, A. Lesauvage,
M. Lethuillier , L. Mirabito, K. Shchablo, L. Torterotot, G. Touquet, M. Vander Donckt, S. Viret

,

Georgian Technical University, Tbilisi, Georgia
A. Khvedelidze 12 , Z. Tsamalaidze 12
I. Physikalisches Institut, RWTH Aachen University, Aachen, Germany
L. Feld , K. Klein, M. Lipinski, D. Meuser, A. Pauls, M. P. Rauch, J. Schulz, M. Teroerde
III. Physikalisches Institut A, RWTH Aachen University, Aachen, Germany
D. Eliseev, M. Erdmann , P. Fackeldey, B. Fischer, S. Ghosh , T. Hebbeker , K. Hoepfner, H. Keller,
L. Mastrolorenzo, M. Merschmeyer , A. Meyer, G. Mocellin, S. Mondal, S. Mukherjee , D. Noll, A. Novak, T. Pook
A. Pozdnyakov , Y. Rath, H. Reithler, J. Roemer, A. Schmidt , S. C. Schuler, A. Sharma, S. Wiedenbeck, S. Zaleski
III. Physikalisches Institut B, RWTH Aachen University, Aachen, Germany
C. Dziwok, G. Flügge, W. Haj Ahmad 18 , O. Hlushchenko, T. Kress, A. Nowack
H. Sert, A. Stahl 19 , T. Ziemons

,

, C. Pistone, O. Pooth, D. Roy,

Deutsches Elektronen-Synchrotron, Hamburg, Germany
H. Aarup Petersen, M. Aldaya Martin, P. Asmuss, I. Babounikau , S. Baxter, O. Behnke, A. Bermúdez Martínez,
A. A. Bin Anuar , K. Borras 20 , V. Botta, D. Brunner, A. Campbell, A. Cardini, P. Connor, S. Consuegra Rodríguez ,
V. Danilov, M. M. Defranchis, L. Didukh, G. Eckerlin, D. Eckstein, L. I. Estevez Banos, E. Gallo 21 , A. Geiser, A. Giraldi,
A. Grohsjean , M. Guthoff, A. Harb , A. Jafari 22 , N. Z. Jomhari , H. Jung, A. Kasem 20 , M. Kasemann , H. Kaveh,
C. Kleinwort , J. Knolle , D. Krücker, W. Lange, T. Lenz, J. Leonard , J. Lidrych, K. Lipka, W. Lohmann 23 ,
T. Madlener, R. Mankel, I.-A. Melzer-Pellmann, J. Metwally, A. B. Meyer, M. Meyer, J. Mnich , A. Mussgiller,
V. Myronenko , Y. Otarid, D. Pérez Adán, D. Pitzl, A. Raspereza, B. Ribeiro Lopes, J. Rübenach, A. Saggio, A. Saibel,
M. Savitskyi, V. Scheurer, C. Schwanenberger 21 , A. Singh, R. E. Sosa Ricardo , N. Tonon , O. Turkot ,
A. Vagnerini, M. Van De Klundert, R. Walsh, D. Walter, Y. Wen , K. Wichmann, C. Wissing, S. Wuchterl, R. Zlebcik
University of Hamburg, Hamburg, Germany
R. Aggleton, S. Bein, L. Benato , A. Benecke, K. De Leo, T. Dreyer, M. Eich, F. Feindt, A. Fröhlich, C. Garbers ,
E. Garutti , P. Gunnellini, J. Haller , A. Hinzmann , A. Karavdina, G. Kasieczka, R. Klanner , R. Kogler,
V. Kutzner, J. Lange , T. Lange, A. Malara, A. Nigamova, K. J. Pena Rodriguez, O. Rieger, P. Schleper, M. Schröder
J. Schwandt , D. Schwarz, J. Sonneveld, H. Stadie, G. Steinbrück, A. Tews, B. Vormwald , I. Zoi

123

,

## PDF page 31

Eur. Phys. J. C (2021) 81:800

Page 31 of 42 800

Karlsruher Institut fuer Technologie, Karlsruhe, Germany
J. Bechtel, T. Berger, E. Butz , R. Caspart, T. Chwalek, W. De Boer, A. Dierlamm, A. Droll, K. El Morabit,
N. Faltermann , K. Flöh, M. Giffels, J. O. Gosewisch, A. Gottmann, F. Hartmann 19 , C. Heidecker, U. Husemann ,
I. Katkov 24 , P. Keicher, R. Koppenhöfer, S. Maier, S. Mallows, M. Metzler, S. Mitra , Th. Müller, M. Musich,
M. Neukum, G. Quast , K. Rabbertz , J. Rauser, D. Savoiu, D. Schäfer, M. Schnepf, D. Seith, I. Shvetsov, H. J. Simonis,
R. Ulrich , J. Van Der Linden, R. F. Von Cube, M. Wassmer, M. Weber, S. Wieland, R. Wolf, S. Wozniewski, S. Wunsch
Institute of Nuclear and Particle Physics (INPP), NCSR Demokritos, Aghia Paraskevi, Greece
G. Anagnostou, P. Asenov, G. Daskalakis, T. Geralis, A. Kyriakis, D. Loukas, A. Stakia
National and Kapodistrian University of Athens, Athens, Greece
M. Diamantopoulou, D. Karasavvas, G. Karathanasis, P. Kontaxakis, C. K. Koraka, A. Manousakis-Katsikakis,
A. Panagiotou, I. Papavergou, N. Saoulidou, K. Theofilatos, E. Tziaferi, K. Vellidis, E. Vourliotis
National Technical University of Athens, Athens, Greece
G. Bakas, K. Kousouris , I. Papakrivopoulos, G. Tsipolitis, A. Zacharopoulou
University of Ioánnina, Ioannina, Greece
I. Evangelou, C. Foudas, P. Gianneios, P. Katsoulis, P. Kokkas, N. Manthos, I. Papadopoulos, J. Strologas
MTA-ELTE Lendület CMS Particle and Nuclear Physics Group, Eötvös Loránd University, Budapest, Hungary
M. Csanad , M. M. A. Gadallah 25 , S. Lökös 26 , P. Major, K. Mandal, A. Mehta , G. Pasztor , A. J. Rádl, O. Surányi,
G. I. Veres
Wigner Research Centre for Physics, Budapest, Hungary
M. Bartók 27 , G. Bencze, C. Hajdu , D. Horvath 28 , F. Sikler

, V. Veszpremi, G. Vesztergombi †

Institute of Nuclear Research ATOMKI, Debrecen, Hungary
S. Czellar, J. Karancsi 27 , J. Molnar, Z. Szillasi, D. Teyssier
Institute of Physics, University of Debrecen, Debrecen, Hungary
P. Raics, Z. L. Trocsanyi 29 , B. Ujvari
Eszterhazy Karoly University, Karoly Robert Campus, Gyongyos, Hungary
T. Csorgo 30 , F. Nemes 30 , T. Novak
Indian Institute of Science (IISc), Bangalore, India
S. Choudhury, J. R. Komaragiri , D. Kumar, L. Panwar, P. C. Tiwari
National Institute of Science Education and Research, HBNI, Bhubaneswar, India
S. Bahinipati 31 , D. Dash , C. Kar, P. Mal, T. Mishra, V. K. Muraleedharan Nair Bindhu 32 , A. Nayak 32 , P. Saha, N. Sur
S. K. Swain

,

Panjab University, Chandigarh, India
S. Bansal , S. B. Beri, V. Bhatnagar, G. Chaudhary, S. Chauhan, N. Dhingra 33 , R. Gupta, A. Kaur, S. Kaur, P. Kumari,
M. Meena, K. Sandeep, J. B. Singh, A. K. Virdi
University of Delhi, Delhi, India
A. Ahmed, A. Bhardwaj, B. C. Choudhary
K. Ranjan, A. Shah

, R. B. Garg, M. Gola, S. Keshri

, A. Kumar, M. Naimuddin

, P. Priyanka,

Saha Institute of Nuclear Physics, HBNI, Kolkata, India
M. Bharti 34 , R. Bhattacharya, S. Bhattacharya , D. Bhowmik, S. Dutta, B. Gomber 35 , M. Maity 36 , S. Nandan, P. Palit,
P. K. Rout, G. Saha, B. Sahu, S. Sarkar, M. Sharan, B. Singh 34 , S. Thakur 34
Indian Institute of Technology Madras, Chennai, India
P. K. Behera , S. C. Behera, P. Kalbhor, A. Muhammad, R. Pradhan, P. R. Pujahari, A. Sharma, A. K. Sikdar

123

## PDF page 32

800 Page 32 of 42

Eur. Phys. J. C (2021) 81:800

Bhabha Atomic Research Centre, Mumbai, India
D. Dutta, V. Jha, V. Kumar, D. K. Mishra, K. Naskar 37 , P. K. Netrakanti, L. M. Pant, P. Shukla
Tata Institute of Fundamental Research-A, Mumbai, India
T. Aziz, S. Dugad, G. B. Mohanty , U. Sarkar
Tata Institute of Fundamental Research-B, Mumbai, India
S. Banerjee, S. Bhattacharya, R. Chudasama, M. Guchait, S. Karmakar, S. Kumar, G. Majumder, K. Mazumdar,
S. Mukherjee, D. Roy
Indian Institute of Science Education and Research (IISER), Pune, India
S. Dube , B. Kansal, S. Pandey, A. Rane, A. Rastogi, S. Sharma
Department of Physics, Isfahan University of Technology, Isfahan, Iran
H. Bakhshiansohi 38 , M. Zeinali 39
Institute for Research in Fundamental Sciences (IPM), Tehran, Iran
S. Chenarani 40 , S. M. Etesami, M. Khakzad, M. Mohammadi Najafabadi
University College Dublin, Dublin, Ireland
M. Felcini , M. Grunewald
INFN Sezione di Baria , Universit’a di Barib , Politecnico di Baric , Bari, Italy
M. Abbrescia a ,b , R. Alya ,b,41 , C. Arutaa ,b , A. Colaleo a , D. Creanza a ,c , N. De Filippis a ,c , M. De Palma a ,b ,
A. Di Florioa ,b , A. Di Pilatoa ,b , W. Elmetenawee a ,b , L. Fiore a , A. Gelmia ,b , M. Gul a , G. Iaselli a ,c , M. Ince a ,b ,
S. Lezki a ,b , G. Maggi a ,c , M. Maggi a , I. Margjekaa ,b , V. Mastrapasquaa ,b , J. A. Merlina , S. My a ,b ,
S. Nuzzo a ,b , A. Pompili a ,b , G. Pugliese a ,c , A. Ranieri a , G. Selvaggi a ,b , L. Silvestris a , F. M. Simonea ,b ,
R. Venditti a , P. Verwilligen a
INFN Sezione di Bolognaa , Università di Bolognab , Bologna, Italy
G. Abbiendi a , C. Battilana a ,b , D. Bonacorsi a ,b , L. Borgonovia , S. Braibant-Giacomelli a ,b , L. Brigliadoria ,
R. Campanini a ,b , P. Capiluppi a ,b , A. Castro a ,b , F. R. Cavallo a , C. Ciocca a , M. Cuffiani a ,b ,
G. M. Dallavalle a , T. Diotalevia ,b , F. Fabbri a , A. Fanfani a ,b , E. Fontanesia ,b , P. Giacomelli a , L. Giommia ,b ,
C. Grandi a , L. Guiduccia ,b , F. Iemmia ,b , S. Lo Meoa ,42 , S. Marcellini a , G. Masetti a , F. L. Navarria a ,b ,
A. Perrotta a , F. Primavera a ,b , A. M. Rossi a ,b , T. Rovelli a ,b , G. P. Siroli a ,b , N. Tosi a
INFN Sezione di Cataniaa , Università di Cataniab , Catania, Italy
S. Albergo a ,b,43 , S. Costa a ,b,43 , A. Di Mattia a , R. Potenzaa ,b , A. Tricomi

a ,b,43 , C. Tuve

a ,b

INFN Sezione di Firenzea , Università di Firenzeb , Florence, Italy
G. Barbagli a , A. Cassese a , R. Ceccarellia ,b , V. Ciulli a ,b , C. Civinini a , R. D’Alessandro a ,b , F. Fioria ,b ,
E. Focardi a ,b , G. Latino a ,b , P. Lenzi a ,b , M. Lizzoa ,b , M. Meschini a , S. Paoletti a , R. Seiditaa ,b ,
G. Sguazzoni a , L. Viliani a
INFN Laboratori Nazionali di Frascati, Frascati, Italy
L. Benussi , S. Bianco , D. Piccolo
INFN Sezione di Genovaa , Università di Genovab , Genoa, Italy
M. Bozzo a ,b , F. Ferro a , R. Mulargiaa ,b , E. Robutti a , S. Tosi

a ,b

INFN Sezione di Milano-Bicoccaa , Università di Milano-Bicoccab , Milan, Italy
A. Benaglia a , F. Brivioa ,b , F. Cetorellia ,b , V. Cirioloa ,b,19 , F. De Guio a ,b , M. E. Dinardo a ,b , P. Dini a ,
S. Gennai a , A. Ghezzi a ,b , P. Govoni a ,b , L. Guzzia ,b , M. Malbertia , S. Malvezzi a , A. Massironi a ,
D. Menasce a , F. Montia ,b , L. Moroni a , M. Paganoni a ,b , D. Pedrini a , S. Ragazzi a ,b , T. Tabarelli de Fatis
D. Valsecchia ,b,19 , D. Zuolo a ,b

a ,b ,

INFN Sezione di Napolia , Università di Napoli ‘Federico II’b , Naples, Italy, Università della Basilicatac , Potenza,
Italy, Università G. Marconid , Rome, Italy
S. Buontempo a , F. Carnevalia ,b , N. Cavallo a ,c , A. De Iorioa ,b , F. Fabozzi a ,c , A. O. M. Iorio a ,b , L. Lista a ,b ,
S. Meola a ,d ,19 , P. Paolucci a ,19 , B. Rossi a , C. Sciacca a ,b

123

## PDF page 33

Eur. Phys. J. C (2021) 81:800

Page 33 of 42 800

INFN Sezione di Padovaa , Università di Padovab , Padua, Italy, Università di Trentoc , Trento, Italy
P. Azzi a , N. Bacchetta a , D. Bisello a ,b , P. Bortignon a , A. Bragagnoloa ,b , R. Carlin a ,b , P. Checchia a ,
P. De Castro Manzanoa , T. Dorigo a , F. Gasparini a ,b , U. Gasparini a ,b , S. Y. Hoh a ,b , L. Layera ,44 ,
M. Margoni a ,b , A. T. Meneguzzo a ,b , M. Presillaa ,b , P. Ronchese a ,b , R. Rossina ,b , F. Simonetto a ,b , G. Stronga ,
M. Tosi a ,b , H. YARARa ,b , M. Zanetti a ,b , P. Zotto a ,b , A. Zucchetta a ,b , G. Zumerle a ,b
INFN Sezione di Paviaa , Università di Paviab , Pavia, Italy
C. Aime‘a ,b , A. Braghieri a , S. Calzaferria ,b , D. Fiorinaa ,b , P. Montagnaa ,b , S. P. Rattia ,b , V. Re
C. Riccardi a ,b , P. Salvini a , I. Vai a , P. Vitulo a ,b

a , M. Ressegottia ,b ,

INFN Sezione di Perugiaa , Università di Perugiab , Perugia, Italy
G. M. Bilei a , D. Ciangottini a ,b , L. Fanò a ,b , P. Laricciaa ,b , G. Mantovania ,b , V. Mariania ,b , M. Menichelli
F. Moscatelli a , A. Piccinellia ,b , A. Rossi a ,b , A. Santocchia a ,b , D. Spiga a , T. Tedeschia ,b

a,

INFN Sezione di Pisaa , Università di Pisab , Scuola Normale Superiore di Pisac , Pisa, Italy, Università di Sienad ,
Siena, Italy
P. Azzurri a , G. Bagliesi a , V. Bertacchia ,c , L. Bianchini a , T. Boccali a , E. Bossinia , R. Castaldi a ,
M. A. Ciocci a ,b , R. Dell’Orso a , M. R. Di Domenicoa ,d , S. Donato a , A. Giassi a , M. T. Grippo a ,
F. Ligabue a ,c , E. Manca a ,c , G. Mandorlia ,c , A. Messineo a ,b , F. Palla a , G. Ramirez-Sancheza ,c , A. Rizzi a ,b ,
G. Rolandi a ,c , S. Roy Chowdhurya ,c , A. Scribanoa , N. Shafieia ,b , P. Spagnolo a , R. Tenchini a , G. Tonelli a ,b ,
N. Turinia ,d , A. Venturi a , P. G. Verdini a
INFN Sezione di Romaa , Sapienza Università di Romab , Rome, Italy
F. Cavallari a , M. Cipriani a ,b , D. Del Re a ,b , E. Di Marco a , M. Diemoz a , E. Longo a ,b , P. Meridiani a ,
G. Organtini a ,b , F. Pandolfia , R. Paramatti a ,b , C. Quarantaa ,b , S. Rahatlou a ,b , C. Rovelli a , F. Santanastasio
L. Soffi a ,b , R. Tramontanoa ,b

a ,b ,

INFN Sezione di Torinoa , Università di Torinob , Turin, Italy, Università del Piemonte Orientalec , Novara, Italy
N. Amapane a ,b , R. Arcidiacono a ,c , S. Argiro a ,b , M. Arneodo a ,c , N. Bartosika , R. Bellan a ,b , A. Belloraa ,b ,
J. Berenguer Antequeraa ,b , C. Biino a , A. Cappatia ,b , N. Cartiglia a , S. Cometti a , M. Costa a ,b , R. Covarelli a ,b ,
N. Demaria a , B. Kiania ,b , F. Leggera , C. Mariotti a , S. Maselli a , E. Migliore a ,b , V. Monaco a ,b ,
E. Monteil a ,b , M. Monteno a , M. M. Obertino a ,b , G. Ortona a , L. Pacher a ,b , N. Pastrone a , M. Pelliccioni a ,
G. L. Pinna Angionia ,b , M. Ruspa a ,c , R. Salvaticoa ,b , K. Shchelinaa ,b , F. Sivieroa ,b , V. Sola a , A. Solanoa ,b ,
D. Soldi a ,b , A. Staiano a , M. Tornagoa ,b , D. Trocino a ,b
INFN Sezione di Triestea , Università di Triesteb , Trieste, Italy
S. Belforte a , V. Candelise a ,b , M. Casarsa a , F. Cossutti a , A. Da Rold
F. Vazzoler a ,b
Kyungpook National University, Daegu, Korea
S. Dogra , C. Huh, B. Kim, D. H. Kim, G. N. Kim
B. C. Radburn-Smith, S. Sekmen , Y. C. Yang

, J. Lee, S. W. Lee

a ,b , G. Della Ricca

, C. S. Moon

a ,b , G. Sorrentinoa ,b ,

, Y. D. Oh

, S. I. Pak,

Institute for Universe and Elementary Particles, Chonnam National University, Kwangju, Korea
H. Kim, D. H. Moon
Hanyang University, Seoul, Korea
T. J. Kim , J. Park
Korea University, Seoul, Korea
S. Cho, S. Choi , Y. Go, B. Hong

, K. Lee, K. S. Lee, J. Lim, J. Park, S. K. Park, J. Yoo

Department of Physics, Kyung Hee University, Seoul, Republic of Korea
J. Goh , A. Gurtu
Sejong University, Seoul, Korea
H. S. Kim , Y. Kim

123

## PDF page 34

800 Page 34 of 42

Eur. Phys. J. C (2021) 81:800

Seoul National University, Seoul, Korea
J. Almond, J. H. Bhyun, J. Choi, S. Jeon, J. Kim, J. S. Kim, S. Ko, H. Kwon, H. Lee
H. Seo, U. K. Yang, I. Yoon
University of Seoul, Seoul, Korea
D. Jeon, J. H. Kim, B. Ko, J. S. H. Lee

, S. Lee, B. H. Oh, M. Oh, S. B. Oh,

, I. C. Park, Y. Roh, D. Song, I. J. Watson

Department of Physics, Yonsei University, Seoul, Korea
S. Ha, H. D. Yoo
Sungkyunkwan University, Suwon, Korea
Y. Choi, Y. Jeong, H. Lee, Y. Lee, I. Yu
College of Engineering and Technology, American University of the Middle East (AUM), Egaila, Kuwait
T. Beyrouthy, Y. Maghrbi
Riga Technical University, Riga, Latvia
V. Veckalns 45
Vilnius University, Vilnius, Lithuania
M. Ambrozas, A. Juodagalvis , A. Rinkevicius

, G. Tamulaitis, A. Vaitkevicius

National Centre for Particle Physics, Universiti Malaya, Kuala Lumpur, Malaysia
W. A. T. Wan Abdullah, M. N. Yusli, Z. Zolkapli
Universidad de Sonora (UNISON), Hermosillo, Mexico
J. F. Benitez , A. Castaneda Hernandez , J. A. Murillo Quijada

, L. Valencia Palomo

Centro de Investigacion y de Estudios Avanzados del IPN, Mexico City, Mexico
G. Ayala, H. Castilla-Valdez, E. De La Cruz-Burelo , I. Heredia-De La Cruz 46 , R. Lopez-Fernandez,
C. A. Mondragon Herrera, D. A. Perez Navarro, A. Sanchez-Hernandez
Universidad Iberoamericana, Mexico City, Mexico
S. Carrillo Moreno, C. Oropeza Barrera, M. Ramirez-Garcia, F. Vazquez Valencia
Benemerita Universidad Autonoma de Puebla, Puebla, Mexico
I. Pedraza, H. A. Salazar Ibarguen, C. Uribe Estrada
University of Montenegro, Podgorica, Montenegro
J. Mijuskovic 47 , N. Raicevic
University of Auckland, Auckland, New Zealand
D. Krofcheck
University of Canterbury, Christchurch, New Zealand
S. Bheesette, A. P. H. Butler, P. H. Butler , A. Lokhovitskiy, P. Lujan
National Centre for Physics, Quaid-I-Azam University, Islamabad, Pakistan
A. Ahmad, M. I. Asghar, A. Awais, M. I. M. Awan, H. R. Hoorani, W. A. Khan, M. A. Shah, M. Shoaib

, M. Waqas

Faculty of Computer Science, Electronics and Telecommunications, AGH University of Science and Technology,
Kraków, Poland
V. Avati, L. Grzanka, M. Malawski
National Centre for Nuclear Research, Swierk, Poland
H. Bialkowska, M. Bluj , B. Boimska, T. Frueboes, M. Górski, M. Kazana, M. Szleper, P. Traczyk, P. Zalewski
Institute of Experimental Physics, Faculty of Physics, University of Warsaw, Warsaw, Poland
K. Bunkowski, K. Doroba, A. Kalinowski , M. Konecki , J. Krolikowski, M. Walczak
Laboratório de Instrumentação e Física Experimental de Partículas, Lisbon, Portugal
M. Araujo, P. Bargassa , D. Bastos, A. Boletti , P. Faccioli , M. Gallinaro , J. Hollar, N. Leonardo
J. Seixas , O. Toldaiev , J. Varela

123

, T. Niknejad,

## PDF page 35

Eur. Phys. J. C (2021) 81:800

Page 35 of 42 800

Joint Institute for Nuclear Research, Dubna, Russia
S. Afanasiev, D. Budkouski, P. Bunin, M. Gavrilenko, I. Golutvin, I. Gorbunov, A. Kamenev, V. Karjavine, A. Lanev,
A. Malakhov, V. Matveev 48,49 , V. Palichik, V. Perelygin, M. Savina, D. Seitova, V. Shalaev, S. Shmatov, S. Shulha,
V. Smirnov, O. Teryaev, N. Voytishin, A. Zarubin, I. Zhizhin
Petersburg Nuclear Physics Institute, Gatchina (St. Petersburg), Russia
G. Gavrilov, V. Golovtcov, Y. Ivanov, V. Kim 50 , E. Kuznetsova 51 , V. Murzin, V. Oreshkin, I. Smirnov, D. Sosnov,
V. Sulimov, L. Uvarov, S. Volkov, A. Vorobyev
Institute for Nuclear Research, Moscow, Russia
Yu. Andreev , A. Dermenev, S. Gninenko , N. Golubev, A. Karneyeu, M. Kirsanov, N. Krasnikov, A. Pashenkov,
G. Pivovarov , D. Tlisov † , A. Toropin
Institute for Theoretical and Experimental Physics named by A.I. Alikhanov of NRC ‘Kurchatov Institute’, Moscow,
Russia
V. Epshteyn, V. Gavrilov, N. Lychkovskaya, A. Nikitenko 52 , V. Popov, G. Safronov, A. Spiridonov, A. Stepennov,
M. Toms, E. Vlasov , A. Zhokin
Moscow Institute of Physics and Technology, Moscow, Russia
T. Aushev
National Research Nuclear University ‘Moscow Engineering Physics Institute’ (MEPhI), Moscow, Russia
O. Bychkova, M. Danilov 53 , P. Parygin, E. Popova, V. Rusinov
P.N. Lebedev Physical Institute, Moscow, Russia
V. Andreev, M. Azarkin, I. Dremin, M. Kirakosyan, A. Terkulov
Skobeltsyn Institute of Nuclear Physics, Lomonosov Moscow State University, Moscow, Russia
A. Belyaev, E. Boos , M. Dubinin 54 , L. Dudko , A. Ershov, A. Gribushin, A. Kaminskiy 55 , V. Klyukhin
O. Kodolova, I. Lokhtin , S. Obraztsov, S. Petrushanko, V. Savrin
Novosibirsk State University (NSU), Novosibirsk, Russia
V. Blinov 56 , T. Dimova 56 , L. Kardapoltsev 56 , I. Ovtin 56 , Y. Skovpen

,

56

Institute for High Energy Physics of National Research Centre ‘Kurchatov Institute’, Protvino, Russia
I. Azhgirey , I. Bayshev, V. Kachanov, A. Kalinin, D. Konstantinov, V. Petrov, R. Ryutin, A. Sobol, S. Troshin
N. Tyurin, A. Uzunian, A. Volkov

,

National Research Tomsk Polytechnic University, Tomsk, Russia
A. Babaev, V. Okhotnikov, L. Sukhikh
Tomsk State University, Tomsk, Russia
V. Borchsh, V. Ivanchenko , E. Tcherniaev
Faculty of Physics and VINCA Institute of Nuclear Sciences, University of Belgrade, Belgrade, Serbia
P. Adzic 57 , M. Dordevic , P. Milenovic, J. Milosevic , V. Milosevic
Centro de Investigaciones Energéticas Medioambientales y Tecnológicas (CIEMAT), Madrid, Spain
M. Aguilar-Benitez, J. Alcaraz Maestre , A. Álvarez Fernández, I. Bachiller, M. Barrio Luna, Cristina F. Bedoya ,
C. A. Carrillo Montoya, M. Cepeda , M. Cerrada, N. Colino , B. De La Cruz, A. Delgado Peris ,
J. P. Fernández Ramos , J. Flix , M. C. Fouz, O. Gonzalez Lopez , S. Goy Lopez, J. M. Hernandez , M. I. Josa,
J. León Holgado, D. Moran, Á. Navarro Tobar, A. Pérez-Calero Yzquierdo , J. Puerta Pelayo , I. Redondo ,
L. Romero, S. Sánchez Navas, M. S. Soares , L. Urda Gómez, C. Willmott
Universidad Autónoma de Madrid, Madrid, Spain
J. F. de Trocóniz, R. Reyes-Almanza

123

## PDF page 36

800 Page 36 of 42

Eur. Phys. J. C (2021) 81:800

Instituto Universitario de Ciencias y Tecnologías Espaciales de Asturias (ICTEA), Universidad de Oviedo, Oviedo,
Spain
B. Alvarez Gonzalez, J. Cuevas , C. Erice, J. Fernandez Menendez , S. Folgueras , I. Gonzalez Caballero ,
E. Palencia Cortezon , C. Ramón Álvarez, J. Ripoll Sau, V. Rodríguez Bouza , A. Trapote
Instituto de Física de Cantabria (IFCA), CSIC-Universidad de Cantabria, Santander, Spain
J. A. Brochero Cifuentes , I. J. Cabrillo, A. Calderon , B. Chazin Quero, J. Duarte Campderros , M. Fernandez
C. Fernandez Madrazo, P. J. Fernández Manteca , A. García Alonso, G. Gomez, C. Martinez Rivero,
P. Martinez Ruiz del Arbol , F. Matorras , J. Piedra Gomez , C. Prieels, F. Ricci-Tam , T. Rodrigo ,
A. Ruiz-Jimeno , L. Scodellaro , N. Trevisani , I. Vila, J. M. Vizan Garcia

,

University of Colombo, Colombo, Sri Lanka
M. K. Jayananda, B. Kailasapathy 58 , D. U. J. Sonnadara, D. D. C. Wickramarathna
Department of Physics, University of Ruhuna, Matara, Sri Lanka
W. G. D. Dharmaratna , K. Liyanage, N. Perera, N. Wickramage
CERN, European Organization for Nuclear Research, Geneva, Switzerland
T. K. Aarrestad, D. Abbaneo, J. Alimena , E. Auffray, G. Auzinger, J. Baechler, P. Baillon † , A. H. Ball, D. Barney,
J. Bendavid, N. Beni, M. Bianco , A. Bocci, E. Brondolin, T. Camporesi, M. Capeans Garrido, G. Cerminara,
S. S. Chhibra , L. Cristella , D. d’Enterria , A. Dabrowski, N. Daci, A. David , A. De Roeck , M. Deile,
R. Di Maria , M. Dobson, M. Dünser , N. Dupont, A. Elliott-Peisert, N. Emriskova, F. Fallavollita 59 , D. Fasanella ,
S. Fiorendi , A. Florent , G. Franzoni , J. Fulcher , W. Funk, S. Giani, D. Gigi, K. Gill, F. Glege, L. Gouskos,
M. Haranko , J. Hegeman , Y. Iiyama , V. Innocente, T. James, P. Janot , J. Kaspar, J. Kieseler , M. Komm ,
N. Kratochwil, C. Lange , S. Laurila, P. Lecoq , K. Long, C. Lourenço , L. Malgeri , S. Mallios, M. Mannelli,
F. Meijers, S. Mersi , E. Meschi , F. Moortgat , M. Mulders , S. Orfanelli, L. Orsini, F. Pantaleo , L. Pape,
E. Perez, M. Peruzzi, A. Petrilli, G. Petrucciani , A. Pfeiffer , M. Pierini , H. Qu , T. Quast, D. Rabady , A. Racz,
M. Rieger , M. Rovere, H. Sakulin, J. Salfeld-Nebgen , S. Scarfi, C. Schäfer, C. Schwick, M. Selvaggi, A. Sharma,
P. Silva , W. Snoeys , P. Sphicas 60 , S. Summers, V. R. Tavolaro , D. Treille, A. Tsirou, P. Tsrunchev,
G. P. Van Onsem , M. Verzetti, J. Wanczyk 61 , K. A. Wozniak, W. D. Zeuner
Paul Scherrer Institut, Villigen, Switzerland
L. Caminada 62 , A. Ebrahimi , W. Erdmann, R. Horisberger, Q. Ingram, H. C. Kaestli, D. Kotlinski, U. Langenegger,
M. Missiroli , T. Rohe
ETH Zurich-Institute for Particle Physics and Astrophysics (IPA), Zurich, Switzerland
K. Androsov 61 , M. Backhaus , P. Berger, A. Calandri, N. Chernyavskaya, A. De Cosa, G. Dissertori , M. Dittmar,
M. Donegà, C. Dorfer, F. Eble, T. Gadek, T. A. Gómez Espinosa , C. Grab , D. Hits, W. Lustermann, A.-M. Lyon,
R. A. Manzoni , C. Martin Perez, M. T. Meinhard, F. Micheli, F. Nessi-Tedaldi, J. Niedziela , F. Pauss, V. Perovic,
G. Perrin, S. Pigazzini , M. G. Ratti , M. Reichmann, C. Reissel, T. Reitenspiess, B. Ristic, D. Ruini,
D. A. Sanz Becerra, M. Schönenberger , V. Stampf, J. Steggemann 61 , R. Wallny , D. H. Zhu
Universität Zürich, Zurich, Switzerland
C. Amsler 63 , C. Botta , D. Brzhechko, M. F. Canelli , A. De Wit , R. Del Burgo, J. K. Heikkilä , M. Huwiler,
A. Jofrehei, B. Kilminster , S. Leontsinis , A. Macchiolo, P. Meiring, V. M. Mikuni, U. Molinatti, I. Neutelings,
G. Rauco, A. Reimers, P. Robmann, S. Sanchez Cruz , K. Schweiger , Y. Takahashi
National Central University, Chung-Li, Taiwan
C. Adloff 64 , C. M. Kuo, W. Lin, A. Roy, T. Sarkar

36 , S. S. Yu

National Taiwan University (NTU), Taipei, Taiwan
L. Ceard, P. Chang , Y. Chao, K. F. Chen, P. H. Chen, W.-S. Hou
E. Yazgan , P.r. Yu

, Y.y. Li, R.-S. Lu, E. Paganis, A. Psallidas, A. Steen,

Department of Physics, Faculty of Science, Chulalongkorn University, Bangkok, Thailand
B. Asavapibhop , C. Asawatangtrakuldee, N. Srimanobhas

123

## PDF page 37

Eur. Phys. J. C (2021) 81:800

Page 37 of 42 800

Physics Department, Science and Art Faculty, Çukurova University, Adana, Turkey
F. Boran, S. Damarseckin 65 , Z. S. Demiroglu , F. Dolek, I. Dumanoglu 66 , E. Eskut, G. Gokbulut, Y. Guler,
E. Gurpinar Guler 67 , I. Hos 68 , C. Isik, E. E. Kangal 69 , O. Kara, A. Kayis Topaksu, U. Kiminsu , G. Onengut,
K. Ozdemir 70 , A. Polatoz, A. E. Simsek, B. Tali 71 , U. G. Tok, S. Turkcapar, I. S. Zorbakir , C. Zorbilmez
Physics Department, Middle East Technical University, Ankara, Turkey
B. Isildak 72 , G. Karapinar 73 , K. Ocalan 74 , M. Yalvac 75
Bogazici University, Istanbul, Turkey
B. Akgun, I. O. Atakisi, Y. C. Cekmecelioglu, E. Gülmez
E. A. Yetkin 79

, M. Kaya 76 , O. Kaya 77 , Ö. Özçelik, S. Tekten 78 ,

Istanbul Technical University, Istanbul, Turkey
A. Cakir , K. Cankocak 66 , Y. Komurcu, S. Sen 80
Istanbul University, Istanbul, Turkey
F. Aydogmus Sen, S. Cerci 71 , B. Kaynak, S. Ozkorucuklu, D. Sunar Cerci 71
Institute for Scintillation Materials of National Academy of Science of Ukraine, Kharkov, Ukraine
B. Grynyov
National Scientific Center, Kharkov Institute of Physics and Technology, Kharkov, Ukraine
L. Levchuk
University of Bristol, Bristol, UK
E. Bhal, S. Bologna, J. J. Brooke , A. Bundock , E. Clement , D. Cussans, H. Flacher , J. Goldstein , G. P. Heath,
H. F. Heath , L. Kreczko , B. Krikler , S. Paramesvaran, T. Sakuma , S. Seif El Nasr-Storey, V. J. Smith,
N. Stylianou 81 , J. Taylor, A. Titterton
Rutherford Appleton Laboratory, Didcot, UK
K. W. Bell, A. Belyaev 82 , C. Brew , R. M. Brown, D. J. A. Cockerill, K. V. Ellis, K. Harder, S. Harper, J. Linacre
K. Manolopoulos, D. M. Newbold , E. Olaiya, D. Petyt, T. Reis , T. Schuh, C. H. Shepherd-Themistocleous,
A. Thea , I. R. Tomalin, T. Williams

,

Imperial College, London, UK
R. Bainbridge , P. Bloch, S. Bonomally, J. Borg , S. Breeze, O. Buchmuller, V. Cepaitis, G. S. Chahal 83 , D. Colling,
P. Dauncey , G. Davies, M. Della Negra , S. Fayer, G. Fedi , G. Hall , M. H. Hassanshahi, G. Iles, J. Langford,
L. Lyons, A.-M. Magnan, S. Malik, A. Martelli , J. Nash 84 , V. Palladino , M. Pesaresi, D. M. Raymond, A. Richards,
A. Rose, E. Scott , C. Seez, A. Shtipliyski, A. Tapper , K. Uchida, T. Virdee 19 , N. Wardle , S. N. Webb,
D. Winterbottom, A. G. Zecchinelli
Brunel University, Uxbridge, UK
J. E. Cole , A. Khan, P. Kyberd , C. K. Mackay, I. D. Reid

, L. Teodorescu, S. Zahid

Baylor University, Waco, USA
S. Abdullin , A. Brinkerhoff , B. Caraway, J. Dittmann, K. Hatakeyama, A. R. Kanuganti, B. McMaster, N. Pastika,
S. Sawant, C. Smith, C. Sutantawibul, J. Wilson
Catholic University of America, Washington, DC, USA
R. Bartek , A. Dominguez , R. Uniyal, A. M. Vargas Hernandez
The University of Alabama, Tuscaloosa, USA
A. Buccilli , O. Charaf, S. I. Cooper, D. Di Croce, S. V. Gleyzer, C. Henderson

, C. U. Perez

, P. Rumerio, C. West

Boston University, Boston, USA
A. Akpinar, A. Albert , D. Arcaro, C. Cosby, Z. Demiragli, D. Gastler, J. Rohlf, K. Salyer, D. Sperka, D. Spitzbart
I. Suarez, A. Tsatsos, S. Yuan, D. Zou

,

123

## PDF page 38

800 Page 38 of 42

Eur. Phys. J. C (2021) 81:800

Brown University, Providence, USA
G. Benelli, B. Burkle , X. Coubez 20 , D. Cutts , Y.t. Duh, M. Hadley, U. Heintz, J. M. Hogan 85 , E. Laird,
G. Landsberg , K. T. Lau, J. Lee, J. Luo, M. Narain, S. Sagir 86 , E. Usai , W. Y. Wong, X. Yan, D. Yu, W. Zhang
University of California, Davis, Davis, USA
C. Brainerd , R. Breedon, M. Calderon De La Barca Sanchez, M. Chertok, J. Conway , P. T. Cox, R. Erbacher,
F. Jensen, O. Kukral, R. Lander, M. Mulhearn, D. Pellett, B. Regnery, D. Taylor , M. Tripathi , Y. Yao, F. Zhang
University of California, Los Angeles, USA
M. Bachtis, R. Cousins , A. Dasgupta, A. Datta, D. Hamilton, J. Hauser , M. Ignatenko, M. A. Iqbal, T. Lam,
N. Mccoll, W. A. Nash, S. Regnard , D. Saltzberg , C. Schnaible, B. Stone, V. Valuev
University of California, Riverside, Riverside, USA
K. Burt, Y. Chen, R. Clare , J. W. Gary , G. Hanson, G. Karapostoli, O. R. Long
M. Olmedo Negrete, W. Si, S. Wimpenny, Y. Zhang

, N. Manganelli,

University of California, San Diego, La Jolla, USA
J. G. Branson, P. Chang, S. Cittolin, S. Cooperstein, N. Deelen, J. Duarte , R. Gerosa , L. Giannini, D. Gilbert
J. Guiang, R. Kansal, V. Krutelyov , R. Lee, J. Letts , M. Masciovecchio, S. May, S. Padhi, M. Pieri ,
B. V. Sathia Narayanan, V. Sharma , M. Tadel, A. Vartak , F. Würthwein , Y. Xiang, A. Yagil

,

Department of Physics, University of California, Santa Barbara, Santa Barbara, USA
N. Amin, C. Campagnari, M. Citron, A. Dorsett, V. Dutta, J. Incandela , M. Kilpatrick, B. Marsh, H. Mei, A. Ovcharova,
M. Quinnan, J. Richman, U. Sarica , D. Stuart, S. Wang
California Institute of Technology, Pasadena, USA
A. Bornheim , O. Cerri, I. Dutta, J. M. Lawhorn , N. Lu , J. Mao, H. B. Newman
M. Spiropulu , J. R. Vlimant , C. Wang, S. Xie , Z. Zhang , R. Y. Zhu
Carnegie Mellon University, Pittsburgh, USA
J. Alison, M. B. Andrews, T. Ferguson , T. Mudholkar, M. Paulini
University of Colorado Boulder, Boulder, USA
J. P. Cumalat, W. T. Ford , E. MacDonald, R. Patel, A. Perloff

, J. Ngadiuba, T. Q. Nguyen

,

, I. Vorobiev

, K. Stenson

Cornell University, Ithaca, USA
J. Alexander, Y. Cheng, J. Chu, D. J. Cranshaw, K. Mcdermott , J. Monroy
A. Ryd, W. Sun , S. M. Tan, Z. Tao, J. Thom, P. Wittich , M. Zientek

, K. A. Ulmer
, J. R. Patterson

, S. R. Wagner
, D. Quach

, J. Reichert,

Fermi National Accelerator Laboratory, Batavia, USA
M. Albrow , M. Alyari, G. Apollinari, A. Apresyan , A. Apyan , S. Banerjee, L. A. T. Bauerdick , A. Beretvas ,
D. Berry , J. Berryhill , P. C. Bhat, K. Burkett , J. N. Butler, A. Canepa, G. B. Cerati , H. W. K. Cheung ,
F. Chlebana, M. Cremonesi, K. F. Di Petrillo, V. D. Elvira , J. Freeman, Z. Gecse, L. Gray, D. Green, S. Grünendahl ,
O. Gutsche , R. M. Harris , R. Heller, T. C. Herwig, J. Hirschauer , B. Jayatilaka , S. Jindariani, M. Johnson,
U. Joshi, P. Klabbers , T. Klijnsma, B. Klima , M. J. Kortelainen , K. H. M. Kwok, S. Lammel , D. Lincoln ,
R. Lipton, T. Liu, J. Lykken, C. Madrid, K. Maeshima, C. Mantilla , D. Mason, P. McBride , P. Merkel, S. Mrenna ,
S. Nahn, V. O’Dell, V. Papadimitriou, K. Pedro , C. Pena 54 , O. Prokofyev, F. Ravera , A. Reinsvold Hall ,
L. Ristori , B. Schneider , E. Sexton-Kennedy , N. Smith, A. Soha , L. Spiegel, S. Stoynev , J. Strait ,
L. Taylor , S. Tkaczyk, N. V. Tran, L. Uplegger , E. W. Vaandering , H. A. Weber , A. Woodard
University of Florida, Gainesville, USA
D. Acosta, P. Avery, D. Bourilkov , L. Cadamuro , V. Cherepanov, F. Errico, R. D. Field, D. Guerrero, B. M. Joshi,
M. Kim, J. Konigsberg, A. Korytov, K. H. Lo, K. Matchev, N. Menendez, G. Mitselmakher , D. Rosenzweig, K. Shi ,
J. Sturdy , J. Wang , E. Yigitbasi, X. Zuo
Florida State University, Tallahassee, USA
T. Adams , A. Askew, D. Diaz, R. Habibullah , S. Hagopian
G. Martinez, H. Prosper, C. Schiber, R. Yohay , J. Zhang

123

, V. Hagopian, K. F. Johnson, R. Khurana, T. Kolberg

,

## PDF page 39

Eur. Phys. J. C (2021) 81:800

Page 39 of 42 800

Florida Institute of Technology, Melbourne, USA
M. M. Baarmand , S. Butalla, T. Elkafrawy 13 , M. Hohlmann
M. Saunders, F. Yumiceva

, R. Kumar Verma, D. Noonan, M. Rahmani,

University of Illinois at Chicago (UIC), Chicago, USA
M. R. Adams, L. Apanasevich , H. Becerril Gonzalez, R. Cavanaugh , X. Chen , S. Dittmer, O. Evdokimov ,
C. E. Gerber , D. A. Hangal, D. J. Hofman , C. Mills , G. Oh, T. Roy, M. B. Tonjes, N. Varelas, J. Viinikainen ,
X. Wang, Z. Wu , Z. Ye
The University of Iowa, Iowa City, USA
M. Alhusseini, K. Dilsiz 87 , S. Durgut, R. P. Gandrajula
A. Mestvirishvili 88 , A. Moeller, J. Nachtman, H. Ogul
J. Wetzel

, M. Haytmyradov, V. Khristenko, O. K. Köseyan, J.-P. Merlo,
89 , Y. Onel, F. Ozok 90 , A. Penzo, C. Snyder, E. Tiras 91 ,

Johns Hopkins University, Baltimore, USA
O. Amram, B. Blumenfeld , L. Corcodilos, M. Eminizer, A. V. Gritsan
M. Swartz, T.Á. Vámi

, S. Kyriacou, P. Maksimovic, J. Roskes

The University of Kansas, Lawrence, USA
C. Baldenegro Barrera, P. Baringer , A. Bean , A. Bylinkin , T. Isidori, S. Khalil , J. King, G. Krintiras
A. Kropivnitskaya, C. Lindsey, N. Minafra , M. Murray, C. Rogan , C. Royon, S. Sanders, E. Schmitz,
J. D. Tapia Takaki , Q. Wang , J. Williams, G. Wilson
Kansas State University, Manhattan, USA
S. Duric, A. Ivanov , K. Kaadze, D. Kim, Y. Maravin

,

,

, T. Mitchell, A. Modak, K. Nam

Lawrence Livermore National Laboratory, Livermore, USA
F. Rebassoo, D. Wright
University of Maryland, College Park, USA
E. Adams, A. Baden, O. Baron, A. Belloni , S. C. Eno , Y. Feng, N. J. Hadley, S. Jabeen, R. G. Kellogg, T. Koeth,
A. C. Mignerey, S. Nabili, M. Seidel , A. Skuja, S. C. Tonwar, L. Wang, K. Wong
Massachusetts Institute of Technology, Cambridge, USA
D. Abercrombie, G. Andreassi, R. Bi, S. Brandt, W. Busza , I. A. Cali, Y. Chen , M. D’Alfonso , G. Gomez Ceballos,
M. Goncharov, P. Harris, M. Hu, M. Klute, D. Kovalskyi , J. Krupa, Y.-J. Lee , B. Maier, A. C. Marini , C. Mironov,
C. Paus, D. Rankin, C. Roland, G. Roland, Z. Shi , G. S. F. Stephans , K. Tatar , J. Wang, Z. Wang, B. Wyslouch
University of Minnesota, Minneapolis, USA
R. M. Chatterjee, A. Evans , P. Hansen, J. Hiltbrand, Sh. Jain
M. Revering, R. Rusack, R. Saradhy, N. Schroeder, N. Strobbe

, M. Krohn, Y. Kubota, Z. Lesko, J. Mans
, M. A. Wadud

,

University of Mississippi, Oxford, USA
J. G. Acosta, S. Oliveros
University of Nebraska-Lincoln, Lincoln, USA
K. Bloom , M. Bryson, S. Chauhan , D. R. Claes, C. Fangmeier, L. Finco
C. Joo, I. Kravchenko , J. E. Siado, G. R. Snow † , W. Tabb, F. Yan

, F. Golf

State University of New York at Buffalo, Buffalo, USA
G. Agarwal, H. Bandyopadhyay, L. Hay, I. Iashvili , A. Kharchilava, C. McLean
S. Rappoccio , A. Williams

, J. R. González Fernández,

, D. Nguyen, J. Pekkanen,

Northeastern University, Boston, USA
G. Alverson , E. Barberis, C. Freer, Y. Haddad , A. Hortiangtham, J. Li, G. Madigan, B. Marzocchi , D. M. Morse ,
V. Nguyen, T. Orimoto, A. Parker, L. Skinnari , A. Tishelman-Charny, T. Wamorkar, B. Wang, A. Wisecarver, D. Wood
Northwestern University, Evanston, USA
S. Bhattacharya, J. Bueghly, Z. Chen, A. Gilbert

, T. Gunter, K. A. Hahn, N. Odell, M. H. Schmitt

, K. Sung, M. Velasco

123

## PDF page 40

800 Page 40 of 42

Eur. Phys. J. C (2021) 81:800

University of Notre Dame, Notre Dame, USA
R. Band, R. Bucci, N. Dev , R. Goldouzian, M. Hildreth, K. Hurtado Anampa , C. Jessop, K. Lannon, N. Loukas ,
N. Marinelli, I. Mcalister, F. Meng, K. Mohrman, Y. Musienko 48 , R. Ruchti, P. Siddireddy, M. Wayne, A. Wightman,
M. Wolf , M. Zarucki, L. Zygala
The Ohio State University, Columbus, USA
B. Bylsma, B. Cardwell, L. S. Durkin, B. Francis, C. Hill

, A. Lefeld, B. L. Winer, B. R. Yates

Princeton University, Princeton, USA
F. M. Addesa, B. Bonham, P. Das, G. Dezoort, P. Elmer , A. Frankenthal , B. Greenberg, N. Haubrich,
S. Higginbotham, A. Kalogeropoulos , G. Kopp, S. Kwan, D. Lange, M. T. Lucchini , D. Marlow , K. Mei
I. Ojalvo, J. Olsen , C. Palmer, D. Stickland , C. Tully , Z. Xie

,

University of Puerto Rico, Mayagüez, USA
S. Malik , S. Norberg
Purdue University, West Lafayette, USA
A. S. Bakshi, V. E. Barnes , R. Chawla, S. Das, L. Gutay, M. Jones, A. W. Jung , S. Karmarkar, M. Liu, G. Negro,
N. Neumeister , G. Paspalaki, C. C. Peng, S. Piperov , A. Purohit, J. F. Schulte , M. Stojanovic 16 , J. Thieman,
F. Wang , R. Xiao, W. Xie
Purdue University Northwest, Hammond, USA
J. Dolen, N. Parashar
Rice University, Houston, USA
A. Baty , S. Dildick, K. M. Ecklund , S. Freed, F. J. M. Geurts
J. Roberts † , W. Shi , A. G. Stahl Leiton

, A. Kumar, W. Li, B. P. Padley

, R. Redjimi,

University of Rochester, Rochester, USA
A. Bodek , P. de Barbaro, R. Demina, J. L. Dulemba, C. Fallon, T. Ferbel, M. Galanti, A. Garcia-Bellido, O. Hindrichs,
A. Khukhunaishvili, E. Ranken, R. Taus
Rutgers, The State University of New Jersey, Piscataway, USA
B. Chiarito, J. P. Chou , A. Gandrakota, Y. Gershtein , E. Halkiadakis , A. Hart, M. Heindl , E. Hughes, S. Kaplan,
O. Karacheban 23 , I. Laflotte, A. Lath , R. Montalvo, K. Nash, M. Osherson, S. Salur , S. Schnetzer, S. Somalwar ,
R. Stone, S. A. Thayil, S. Thomas, H. Wang
University of Tennessee, Knoxville, USA
H. Acharya, A. G. Delannoy , S. Spanier
Texas A&M University, College Station, USA
O. Bouhali 92 , M. Dalchenko , A. Delgado, R. Eusebi, J. Gilmore, T. Huang, T. Kamon 93 , H. Kim, S. Luo, S. Malhotra,
R. Mueller, D. Overton, D. Rathjens , A. Safonov
Texas Tech University, Lubbock, USA
N. Akchurin, J. Damgov, V. Hegde, S. Kunori, K. Lamichhane, S. W. Lee
S. Undleeb, I. Volobouev, Z. Wang, A. Whitbeck

, T. Mengke, S. Muthumuni, T. Peltola

Vanderbilt University, Nashville, USA
E. Appelt , S. Greene, A. Gurrola, W. Johns, C. Maguire, A. Melo, H. Ni, K. Padeken, F. Romeo, P. Sheldon
J. Velkovska
University of Virginia, Charlottesville, USA
M. W. Arenton, B. Cox, G. Cummings, J. Hakala, R. Hirosky
B. Tannenwald , E. Wolfe
Wayne State University, Detroit, USA
P. E. Karchin, N. Poudyal , P. Thapa

123

, M. Joyce, A. Ledovskoy, A. Li, C. Neu

,

,

, S. Tuo,

## PDF page 41

Eur. Phys. J. C (2021) 81:800

Page 41 of 42 800

University of Wisconsin-Madison, Madison, WI, USA
K. Black, T. Bose, J. Buchanan, C. Caillol, S. Dasu , I. De Bruyn , P. Everaerts , F. Fienga, C. Galloni, H. He,
M. Herndon , A. Hervé, U. Hussain, A. Lanaro, A. Loeliger, R. Loveless, J. Madhusudanan Sreekala , A. Mallampalli,
A. Mohammadi, D. Pinna, A. Savin, V. Shang, V. Sharma , W. H. Smith , D. Teague, S. Trembath-Reichert, W. Vetens
† Deceased

1: Also at Vienna University of Technology, Vienna, Austria
2: Also at Institute of Basic and Applied Sciences, Faculty of Engineering, Arab Academy for Science, Technology and
Maritime Transport, Alexandria, Egypt
3: Also at Université Libre de Bruxelles, Brussels, Belgium
4: Also at Universidade Estadual de Campinas, Campinas, Brazil
5: Also at Federal University of Rio Grande do Sul, Porto Alegre, Brazil
6: Also at University of Chinese Academy of Sciences, Beijing, China
7: Also at Department of Physics, Tsinghua University, Beijing, China
8: Also at UFMS, Nova Andradina, Brazil
9: Also at Department of Physics, Nanjing Normal University, Nanjing, China
10: Now at The University of Iowa, Iowa City, USA
11: Also at Institute for Theoretical and Experimental Physics named by A.I. Alikhanov of NRC ‘Kurchatov Institute’,
Moscow, Russia
12: Also at Joint Institute for Nuclear Research, Dubna, Russia
13: Also at Ain Shams University, Cairo, Egypt
14: Also at Zewail City of Science and Technology, Zewail, Egypt
15: Also at British University in Egypt, Cairo, Egypt
16: Also at Purdue University, West Lafayette, USA
17: Also at Université de Haute Alsace, Mulhouse, France
18: Also at Erzincan Binali Yildirim University, Erzincan, Turkey
19: Also at CERN, European Organization for Nuclear Research, Geneva, Switzerland
20: Also at III. Physikalisches Institut A, RWTH Aachen University, Aachen, Germany
21: Also at University of Hamburg, Hamburg, Germany
22: Also at Department of Physics, Isfahan University of Technology, Isfahan, Iran
23: Also at Brandenburg University of Technology, Cottbus, Germany
24: Also at Skobeltsyn Institute of Nuclear Physics, Lomonosov Moscow State University, Moscow, Russia
25: Also at Physics Department, Faculty of Science, Assiut University, Assiut, Egypt
26: Also at Eszterhazy Karoly University, Karoly Robert Campus, Gyongyos, Hungary
27: Also at Institute of Physics, University of Debrecen, Debrecen, Hungary
28: Also at Institute of Nuclear Research ATOMKI, Debrecen, Hungary
29: Also at MTA-ELTE Lendület CMS Particle and Nuclear Physics Group, Eötvös Loránd University, Budapest, Hungary
30: Also at Wigner Research Centre for Physics, Budapest, Hungary
31: Also at IIT Bhubaneswar, Bhubaneswar, India
32: Also at Institute of Physics, Bhubaneswar, India
33: Also at G.H.G. Khalsa College, Punjab, India
34: Also at Shoolini University, Solan, India
35: Also at University of Hyderabad, Hyderabad, India
36: Also at University of Visva-Bharati, Santiniketan, India
37: Also at Indian Institute of Technology (IIT), Mumbai, India
38: Also at Deutsches Elektronen-Synchrotron, Hamburg, Germany
39: Also at Sharif University of Technology, Tehran, Iran
40: Also at Department of Physics, University of Science and Technology of Mazandaran, Behshahr, Iran
41: Now at INFN Sezione di Baria , Università di Barib , Politecnico di Baric , Bari, Italy
42: Also at Italian National Agency for New Technologies, Energy and Sustainable Economic Development, Bologna, Italy
43: Also at Centro Siciliano di Fisica Nucleare e di Struttura Della Materia, Catania, Italy
44: Also at Università di Napoli ‘Federico II’, Naples, Italy
45: Also at Riga Technical University, Riga, Latvia

123

## PDF page 42

800 Page 42 of 42

Eur. Phys. J. C (2021) 81:800

46: Also at Consejo Nacional de Ciencia y Tecnología, Mexico City, Mexico
47: Also at IRFU, CEA, Université Paris-Saclay, Gif-sur-Yvette, France
48: Also at Institute for Nuclear Research, Moscow, Russia
49: Now at National Research Nuclear University ‘Moscow Engineering Physics Institute’ (MEPhI), Moscow, Russia
50: Also at St. Petersburg State Polytechnical University, St. Petersburg, Russia
51: Also at University of Florida, Gainesville, USA
52: Also at Imperial College, London, UK
53: Also at P.N. Lebedev Physical Institute, Moscow, Russia
54: Also at California Institute of Technology, Pasadena, USA
55: Also at INFN Sezione di Padovaa , Università di Padovab , Università di Trentoc , Trento, Italy, Padua, Italy
56: Also at Budker Institute of Nuclear Physics, Novosibirsk, Russia
57: Also at Faculty of Physics, University of Belgrade, Belgrade, Serbia
58: Also at Trincomalee Campus, Eastern University, Nilaveli, Sri Lanka
59: Also at INFN Sezione di Paviaa , Università di Paviab , Pavia, Italy
60: Also at National and Kapodistrian University of Athens, Athens, Greece
61: Also at Ecole Polytechnique Fédérale Lausanne, Lausanne, Switzerland
62: Also at Universität Zürich, Zurich, Switzerland
63: Also at Stefan Meyer Institute for Subatomic Physics, Vienna, Austria
64: Also at Laboratoire d’Annecy-le-Vieux de Physique des Particules, IN2P3-CNRS, Annecy-le-Vieux, France
65: Also at Şırnak University, Sirnak, Turkey
66: Also at Research Center of Experimental Health Science, Near East University, Nicosia, Turkey
67: Also at Konya Technical University, Konya, Turkey
68: Also at Faculty of Engineering, Istanbul University-Cerrahpasa, Istanbul, Turkey
69: Also at Mersin University, Mersin, Turkey
70: Also at Piri Reis University, Istanbul, Turkey
71: Also at Adiyaman University, Adiyaman, Turkey
72: Also at Ozyegin University, Istanbul, Turkey
73: Also at Izmir Institute of Technology, Izmir, Turkey
74: Also at Necmettin Erbakan University, Konya, Turkey
75: Also at Bozok Universitetesi Rektörlügü, Yozgat, Turkey
76: Also at Marmara University, Istanbul, Turkey
77: Also at Milli Savunma University, Istanbul, Turkey
78: Also at Kafkas University, Kars, Turkey
79: Also at Istanbul Bilgi University, Istanbul, Turkey
80: Also at Hacettepe University, Ankara, Turkey
81: Also at Vrije Universiteit Brussel, Brussels, Belgium
82: Also at School of Physics and Astronomy, University of Southampton, Southampton, UK
83: Also at IPPP Durham University, Durham, UK
84: Also at Faculty of Science, Monash University, Clayton, Australia
85: Also at Bethel University, St. Paul, Minneapolis, USA
86: Also at Karamanoğlu Mehmetbey University, Karaman, Turkey
87: Also at Bingol University, Bingol, Turkey
88: Also at Georgian Technical University, Tbilisi, Georgia
89: Also at Sinop University, Sinop, Turkey
90: Also at Mimar Sinan University, Istanbul, Turkey
91: Also at Erciyes University, Kayseri, Turkey
92: Also at Texas A&M University at Qatar, Doha, Qatar
93: Also at Kyungpook National University, Daegu, Korea

123
