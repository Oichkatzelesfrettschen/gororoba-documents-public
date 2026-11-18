Source: see manifest row of the PDF
PDF sha256: f1c023b719d36ba9b7636bae9ea33f8daf35753330f9b1739023eb298aa9583f
License: CC-BY-4.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of schroder_2020_high_resolution_sampling_beam_driven_plasma_wakefields.pdf

Transcription of `schroder_2020_high_resolution_sampling_beam_driven_plasma_wakefields.pdf` in this directory, 6 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-6 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

ARTICLE
https://doi.org/10.1038/s41467-020-19811-9

OPEN

High-resolution sampling of beam-driven
plasma wakeﬁelds

1234567890():,;

S. Schröder 1,2 ✉, C. A. Lindstrøm 1, S. Bohlen 1,2, G. Boyle 1, R. D’Arcy1, S. Diederichs 1,2, M. J. Garland1,
P. Gonzalez 1,2, A. Knetsch 1, V. Libov1, P. Niknejadi 1, Kris Põder 1, L. Schaper 1, B. Schmidt1,
B. Sheeran1,2, G. Tauscher1,2, S. Wesch 1, J. Zemella1, M. Zeng 1 & J. Osterhoff 1

Plasma-wakeﬁeld accelerators driven by intense particle beams promise to signiﬁcantly
reduce the size of future high-energy facilities. Such applications require particle beams with
a well-controlled energy spectrum, which necessitates detailed tailoring of the plasma
wakeﬁeld. Precise measurements of the effective wakeﬁeld structure are therefore essential
for optimising the acceleration process. Here we propose and demonstrate such a measurement technique that enables femtosecond-level (15 fs) sampling of longitudinal electric
ﬁelds of order gigavolts-per-meter (0.8 GV m−1). This method—based on energy collimation
of the incoming bunch—made it possible to investigate the effect of beam and plasma
parameters on the beam-loaded longitudinally integrated plasma wakeﬁeld, showing good
agreement with particle-in-cell simulations. These results open the door to high-quality
operation of future plasma accelerators through precise control of the acceleration process.

1 Deutsches Elektronen-Synchrotron DESY, Notkestraße 85, 22607 Hamburg, Germany. 2 Universität Hamburg, Mittelweg 177, 20148 Hamburg, Germany.
✉email: sarah.schroeder@desy.de

NATURE COMMUNICATIONS | (2020)11:5984 | https://doi.org/10.1038/s41467-020-19811-9 | www.nature.com/naturecommunications

1

## PDF page 2

2

time resolution are therefore needed. The ﬁrst example of this was
presented by Clayton et al.23, who were able to use correlations
within the complex energy transverse phase space measured on a
spectrometer screen to measure the wakeﬁeld indirectly at high
density. However, this particular method works only for mismatched beams (causing emittance growth24) and the temporal
resolution is highly restricted.
In this paper, we propose and demonstrate a more general
solution to measuring beam-driven plasma wakeﬁelds—by fully
separating the time and energy measurements of the longitudinal
phase space. The method works by linking the two measurements
using an energy collimator and bunches with a highly correlated
(chirped) longitudinal-phase-space distribution. This chirp allows
slice-by-slice collimation of the incoming beam-current proﬁle
(see Fig. 1), which can be used to progressively remove thin tail
slices from the energy spectrum after plasma-interaction. Full
time-resolvability necessitates a detailed temporal calibration
of the collimators prior to the measurement (see Methods) and is
then achieved by comparing the spectra as the collimator position
is varied to ﬁnd the energy of the charge that disappears between
steps. Crucially, the measurement of the longitudinal slice position within the bunch for each collimator step can now be entirely

a

Collimator

0.75
0.50

0.00
–0.25

1

–0.50
–0.75
–300

–250

–200

–150
 (µm)

Plasma density (2 × 1016 cm–3)
0

b

1

2

3

–100

–50

0
–0

Beam current (kA)

0.25

E (%)

Beam density (2 × 1016 cm–3)

4 0.0

0.5

1.0

1.5

2.0

50

0

0

Ez (GV m–1)

2

–2
–50

c

50

Progressive
charge removal

2

0

0
Bunch
propagation

–50
–300

–250

–200

–150

–000

–50

Ez (GV m–1)

lasma wakeﬁelds1 can accelerate charged particle beams
with gradients in excess of gigavolts-per-meter, promising
more compact accelerators for high energy physics and
photon science2,3. In a beam-driven plasma-wakeﬁeld accelerator4,5, a high-density charged-particle beam interacts with plasma
electrons to form an electron density wake, in which trailing
particles can rapidly gain energy from strong electric ﬁelds6. The
resulting energy spectrum of the accelerated particles is determined by the detailed structure of this plasma wakeﬁeld, which
again depends on the exact distributions of plasma density and
beam charge7. Free-electron lasers8 and particle colliders9 have
strict demands for precise control of the energy spectrum (e.g.,
low spread of energies), which have not yet been met by plasma
accelerators. To reach this level of precision, it is ﬁrst necessary to
measure the wakeﬁeld with high resolution—highly nontrivial at
the required plasma densities. Here we present a method that
enables such a high-resolution sampling of the effective wakeﬁeld
in a beam-driven plasma accelerator. The method is based on
separating the energy and time measurements of the longitudinal
phase space of particle beams by energy collimation of chirped
bunches, thereby overcoming the practical challenges faced by
previous methods of temporally resolving bunches after plasma
interaction. Using this technique, we demonstrate experimentally
how beam and plasma parameters affect the wakeﬁeld. The
method enables a new level of precision optimisation of the
plasma acceleration process necessary to attain the lower energy
spread, higher efﬁciency10, and higher transformer ratios11,12
desired for future applications.
Various techniques exist for measuring the structure of a
plasma wake13. The electron density distribution can be imaged
using laser-based methods like shadowgraphy14 and frequency
domain holography15. Also the magnetic ﬁelds inside the wake
can be measured using lasers via the Faraday effect16,17. However,
a direct measurement of the electric ﬁelds requires the use of
charged particles. This can be done by traversing the wake perpendicular to its direction of motion with a short probe electron
bunch, such that the transversely-integrated wakeﬁeld is
imprinted on the transverse proﬁle of the probe18. Alternatively,
in a beam-driven plasma accelerator the beam itself can be used
to measure the longitudinal wakeﬁeld, by comparing the longitudinal phase space (i.e., a time-resolved energy spectrum) of
bunches with and without plasma interaction. This gives access to
the effective wakeﬁeld, longitudinally integrated over the full
plasma accelerator module—ultimately the quantity that needs to
be optimised. The longitudinal phase space is typically measured
using a magnetic spectrometer in combination with either a
streak camera or an RF transverse deﬂecting structure (TDS)19,20.
Both methods have been used to measure wakeﬁelds11,12,21 in
plasmas with densities of order 1013–1014 cm−3, requiring picosecond resolution—close to the resolution limit of a streak
camera, whereas a TDS can, in principle, provide time resolution
down to the femtosecond-scale.
Reaching high gradients for compact acceleration requires
operating at plasma densities of 1016–1017 cm−3. In this range,
prior to being optimised, the plasma wakeﬁeld can generate large
energy spreads and complex, slice-dependent distributions in
transverse phase space—highly divergent beams that are difﬁcult to
transport. As a result, measuring the longitudinal phase space of
the plasma-interacted bunches becomes very challenging. The
energy spectrum is therefore commonly measured close to the
plasma module to avoid excessive chromaticity. This makes conventional use of a TDS highly impractical: the required ultrahighvacuum conditions cannot easily be met in the vicinity of a gas load
such as a high-density plasma cell; the structure can be damaged by
irradiation; and the diverging beams can sample off-axis longitudinal RF ﬁelds22. Alternative methods for providing the required

x (µm)

P

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-020-19811-9

x (µm)

ARTICLE

–2
0

 (µm)

Fig. 1 Plasma wakeﬁeld sampling by energy collimation. a A strongly
correlated longitudinal phase space allows tail slices to be progressively
removed from the bunch, e.g., by collimation in a dispersive section.
b An electron bunch interacts with a plasma and excites a density wake
with strong longitudinal electric ﬁelds (3D particle-in-cell simulation).
c Removing charge from the bunch tail alters the wakeﬁeld (compared to
the original ﬁeld, dotted line), but does not alter the wakeﬁeld experienced
by the remaining bunch charge. By subtracting the ﬁnal energy spectrum of
consecutive collimator steps, the energy change of each longitudinal slice
can be determined—revealing the effective wakeﬁeld.

NATURE COMMUNICATIONS | (2020)11:5984 | https://doi.org/10.1038/s41467-020-19811-9 | www.nature.com/naturecommunications

## PDF page 3

ARTICLE

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-020-19811-9

disentangled from the energy-spectrum measurement. As a
consequence, this temporal measurement (e.g., using a TDS) can
be performed elsewhere in the beamline, where conditions such
as beam optics and vacuum requirements can be optimised for
maximum time resolution, and not for the operation of a plasma
accelerator. The measurement can even be performed in a parallel
beamline if the difference in the longitudinal phase space can be
accurately determined.
While bunch-tail removal does affect the wakeﬁeld, it does not
inﬂuence the part being sampled—the wakeﬁeld experienced by
the removed tail slice is identical to that experienced within an
uncollimated bunch (see Fig. 1c). This is because the beam and
the plasma wake both travel at approximately the speed of light,
and therefore (by causality) cannot be affected by changes behind
the cut. By using energy collimation to manipulate the current
proﬁle, some constraints are imposed—in particular, a strictly
monotonic longitudinal-phase-space distribution is required. In
general, a linear monotonic correlation will result in an equidistant sampling of the wakeﬁeld for a constant collimator step
size. Non-linear correlations are applicable, but sample nonequidistantly. Moreover, the accuracy of the measurement will be
limited by the sliced energy spread of the chirped bunches relative
to their overall energy spread, as well as the beam-size-todispersion ratio at the location of the collimator.

the total delivered charge to be 460 ± 5 pC. Two sets of quadrupoles were used to focus the beam tightly at the interaction point,
where the beam orbit was measured using two cavity-based
beam-position monitors (BPMs). The plasma was generated by a
high-voltage discharge in a 1.5-mm-diameter, 33-mm-long sapphire capillary ﬁlled with argon at a backing pressure of 40 mbar.
The plasma cell was separated from the accelerator vacuum by
three (windowless) differential pumping stations. After exiting
the plasma cell, the energy spectrum of the electron beam was
measured with a beam-imaging spectrometer, consisting of a
vertically-dispersive dipole magnet and a set of quadrupoles for
point-to-point beam imaging from the plasma exit plane to a
scintillating LANEX screen. Figure 2 shows the experimental
setup (see Methods for more details).
Experimental campaign. The wakeﬁeld sampling measurement
consisted of a set of tail-collimator scans, progressively removing
the rear part of the bunch until no charge was left. The plasma
density was chosen such that the ﬁrst oscillation of the plasma
wake could be probed by the full length of the current proﬁle (a
density of ~2 × 1016 cm−3). The evolution of the energy spectrum
of the collimated bunches is shown in Fig. 3. The scan was
repeated at three different imaging energies to ensure good energy
resolution over the entire spectrum. The ﬁnal energy of each
longitudinal slice was then determined by the spectral difference
between consecutive collimator steps (see Fig. 3c), resulting in a
distinct signal that can be programmatically extracted (see
Methods). The tail-collimator scan was then repeated with the
plasma turned off, in order to accurately determine the energy
change of each longitudinal slice. Some noise appears in the
difference measurement due to imperfect stability of the plasma
acceleration process, but this does not signiﬁcantly hinder the
extraction of the wakeﬁeld signal.
Time calibration of the tail-collimator steps was performed by
direct comparison to the longitudinal phase space measured by
the TDS. The cumulative charge below each energy in the
longitudinal phase space was compared to the charge readings of
the toroid downstream of the tail collimator (see Methods).
Additionally, a known compression factor of 1.09 (i.e., 9% shorter

d

0
–0.5

Transverse
deflecting cavity

Dispersive
section

–1000 –500
t (fs)

YAG
screen

Tail

1110
1100
(in)
Tail collimator scan

Cavity
BPM
Discharge
plasma cell

c
-3)

Head
collimator

1120

Toroid
Final-focusing
quadrupoles

Tail
collimator

ne (cm

b

1130

(out)

Matching
quadrupoles

Notch
collimator

1120

1140

Energy
collimators
Dipole

x (mm)
0
1

1150

0

Dipole

E (MeV)

Electron beam
(chirped)

–1
1130

OFF

1
0.5

E (MeV)

E (%)

a
Kicker
magnet

Plasma ON

Results
Experimental setup. This wakeﬁeld sampling measurement
technique was implemented and experimentally demonstrated at
the FLASHForward plasma accelerator facility25 at DESY. Highquality electron bunches were generated with a photocathode at a
repetition rate of 10 Hz and accelerated to 1.1 GeV using superconducting RF cavities in the FLASH linac26. The bunches were
linearised in longitudinal phase space and compressed to a bunch
length of 285 ± 2 fs rms, characterised using an S-band TDS in a
beam line parallel to the FLASHForward experimental area. The
beam was then extracted into a dispersive section with a set of
energy collimators for advanced shaping of the current proﬁle27.
The bunch head was collimated throughout the experiment to
optimise the plasma interaction. A downstream toroid measured

10

17

10

16

Beam
arrival

Cavity
BPM
Imaging
quadrupoles

Head

0

5
t (µs)

10

Dipole
spectrometer
LANEX
screen

Fig. 2 Experimental setup. a An electron beam with a linearly chirped longitudinal phase space is characterised in a parallel beam line using a TDS.
b A beam enters a dispersive section with energy collimators for optional removal of the tail (high energy), the head (low energy), and the centre (for twobunch generation). The beam charge is measured with a toroid after collimation and before the beam is focused into a discharge plasma cell. c The relative
time-of-arrival of the beam is adjusted to reach the desired plasma density: the temporal evolution of the average density was measured using two-colour
interferometry in a test stand with a replica cell. d Finally, the beam following plasma interaction passes through a quadrupole triplet and is vertically
dispersed by a spectrometer dipole to form a point-to-point image on a scintillating LANEX screen.
NATURE COMMUNICATIONS | (2020)11:5984 | https://doi.org/10.1038/s41467-020-19811-9 | www.nature.com/naturecommunications

3

## PDF page 4

ARTICLE

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-020-19811-9

Difference charge signal (pC MeV–1 step–1)

Spectral charge density (pC MeV–1)
0

5

10

1135

15
1122

20

25

30

35

40

1109

1150

45

1122

Plasma ON

1140

0

c
Energy, E (MeV)

Energy, E (MeV)

a

Focus
(MeV):

1130
1120
1110
1100
1090

d

1130

Plasma OFF

1120
1110

2

3

4

1150

5

Plasma ON

1140
1130
1120
1110
1100
1090

1122

0

5

10

15
20
25
30
Tail-collimator position (step)

35

40

E (MeV)

E (MeV)

b

Focus
(MeV):

1

1130

Plasma OFF

1120
1110

0

5

10

15
20
25
30
Tail-collimator position (step)

35

40

Fig. 3 Evolution of the tail-collimated energy spectrum. a As the tail collimator is moved in (horizontal axis), the tail particles are progressively removed
from the plasma-interacted energy spectrum; 70 shots are collected per step. b The same scan is repeated with no plasma (20 shots per step),
demonstrating the energy collimation of the incoming bunch. c The difference of (averaged) spectra at consecutive collimator steps reveals the energy of
each slice of the plasma-interacted bunch. d By subtracting the plasma-off energy of each slice, the wakeﬁeld signal can be extracted.

bunches) from the calculated longitudinal dispersion R56 of the
extraction sections was taken into account.
Interpretation of experimental data. Figure 4a shows the
resulting time-resolved wakeﬁeld measurement, sampled with
more than 40 data points separated by ~6 μm. The electric ﬁeld
is calculated as the slice energy change normalised by the full
33-mm length of the cell—giving the effective wakeﬁeld of the
plasma module. The wakeﬁeld is observed to have a zero-crossing
at −165 μm (behind the bunch head), and reaches a maximum
average accelerating gradient of 0.82 ± 0.08 GV m−1 at the bunch
tail.
Given that the effective wakeﬁeld is longitudinally averaged,
understanding the full evolution of the beam and the wakeﬁeld
requires a 3D particle-in-cell (PIC) simulation (see Methods). Since
the measurement is precise to the few-percent level, a similarly
detailed understanding of every aspect of the simulated system is
required—in particular the 6D phase space of the beam, as well as
the longitudinal density proﬁle of the plasma. Using quadrupole
scans and a two-BPM technique for determining the transverse
phase space28, sliced transverse beam parameters were estimated
(see Methods). Additionally, a longitudinally resolved measurement
of the plasma density was performed in a replica cell using Stark
broadening29, where the argon was doped with hydrogen (see
Methods). Due to the Gaussian-like longitudinal plasma-density
proﬁle, the wakeﬁeld and, as such, the peak electric-ﬁeld amplitude
evolve along the length of the plasma channel. The simulations
indicate that the largest instantaneous accelerating ﬁeld observed
was −1.8 GV m−1 at a plasma density of 2.6 × 1016 cm−3, 7 mm
after the peak of the Gaussian-like longitudinal density proﬁle. This
implies that the plasma accelerator was operating in a quasi-linear
regime, reaching ~12% of the wave-breaking ﬁeld. As a result of this
detailed characterisation of the beam and plasma parameters, a
good agreement between simulation and measurement was
achieved (as seen in Fig. 4)—lending credibility to the accuracy of
the method.
Having demonstrated the precise measurement of plasma
wakeﬁelds, we can now investigate the effects of changing key
parameters: (1) the plasma density, and (2) the current proﬁle.
Figure 4b shows the measured wakeﬁeld for a 80% higher plasma
4

density. The wavelength is observed to decrease (zero-crossing at
−155 μm) and the wakeﬁeld amplitude increases, as expected.
Figure 4c shows the effect of introducing a notch collimator (see
Fig. 2b) to remove the central part of the bunch—producing a
double-bunch current proﬁle. This does not alter the wakeﬁeld
ahead of the notch, but drastically changes the shape of the
wakeﬁeld experienced by the trailing charge. In this case, the
zero-crossing of the wakeﬁeld occurs much earlier (at around
−130 μm) because the lack of beam current allows the expelled
plasma electrons to start returning to the axis earlier (the
wakeﬁeld is proportional to the radial velocity of the plasmasheath electrons7). This latter measurement is a direct demonstration of the physics of beam loading30, where the presence or
absence of beam electrons alters the shape of the plasma
wakeﬁeld.
Discussion
The precise measurement of the plasma wakeﬁeld is an essential
precursor to its optimisation. By using an energy-collimation
technique, we have demonstrated that the necessary precision can
be achieved—overcoming the practical challenges faced in a beamdriven plasma accelerator operating at high densities. Combined
with an ability to ﬁne-tune beam and plasma parameters, this
innovative method opens the door to achieving milestones that
require precisely tailored wakeﬁelds—such as optimised beam
loading31 for energy-spread preservation and high efﬁciency—
while operating at the plasma densities and accelerating gradients
necessary for many applications in high energy physics and photon
science.
Methods
Generation of electron bunches. The superconducting linear accelerator FLASH
was used to accelerate electron bunches of 600 pC total charge to a mean particle
energy of 1122 MeV. The bunches were compressed in two magnetic bunchcompressor chicanes to a peak current of 750 A. The longitudinal phase space of
the bunch was measured by a transverse deﬂecting structure in a beam line parallel
to the FLASHForward experimental area. The measured energy spread spans ~1%,
with slice energy spreads well below 0.1% (the measurement is limited by the
transverse beam size inside the TDS and on the screen). A kicker magnet was used
to extract the beam into a dispersive section where a set of three collimators27 were
used for energy proﬁle manipulation, which due to the strongly correlated longitudinal phase space also allows precise manipulation of the bunch current proﬁle.

NATURE COMMUNICATIONS | (2020)11:5984 | https://doi.org/10.1038/s41467-020-19811-9 | www.nature.com/naturecommunications

## PDF page 5

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-020-19811-9

a

1.0
Nominal plasma density
Simulation

–0.5

1

–1.0
1.0

EZ (GV m–1)

0.5

Higher plasma density
Simulation (higher density)
Nominal plasma density
Simulation (nom. density)

0.0
–0.5

1

–1.0

c

1.0
0.5

EZ (GV m–1)

0

Beam current (kA)

b

0

Beam current (kA)

0.0

Notch-collimated bunch
Simulation (collimated)
Full bunch
Simulation (full)

0.0
–0.5

1

–1.0

0
–250

–200

–150

–100

–50

Beam current (kA)

EZ (GV m–1)

0.5

0

 (µm)

Fig. 4 Measured longitudinally averaged plasma wakeﬁelds. a The wakeﬁeld of the nominal beam and plasma is sampled with a 6 μm granularity. Error
bars represent the shot-to-shot standard deviation. The solid line shows the
corresponding PIC simulated wakeﬁeld. b The measurement is repeated with
the same beam current proﬁle and an 80% higher plasma density (the beam
arrives 1.7 μs earlier), producing a shorter wavelength wakeﬁeld. c At the
nominal density (same as in a), the beam current is notch-collimated into a
double-bunch proﬁle, producing a wakeﬁeld which is identical at the head, but
strongly altered at the tail. The end point of ξ = −240 μm is determined by
signal-to-noise ratio.
Owing to collective effects during bunch compression, it was found that collimating the bunch head (down to a total charge of 460 pC) increases the stability of
beam–plasma interaction. This setting was chosen prior to the measurement
campaign and kept throughout it. Toroids were used to measure the beam charge
before and after the energy collimation. The bunches were further compressed by
an estimated 9% in the dispersive extraction line. A set of nine quadrupoles was
used to tightly focus the beam at the location of the plasma cell. Two cavity-based
beam-position monitors (50 cm upstream and 50 cm downstream of the plasma)
were used for beam alignment. Three differential pumping stations enabled a
windowless vacuum-to-plasma transition—ensuring high beam quality while also
meeting the ultrahigh vacuum requirements of the superconducting FLASH
accelerator.
Plasma source. A discharge plasma source was used to create the plasma, ignited
by a high-voltage thyratron supplying ~500 A of current at 25 kV for a duration of
400 ns. A thin 1.5-mm-diameter, 33-mm-long capillary was milled from two slabs
of sapphire, mounted in a PEEK plastic holder, again mounted on a hexapod
platform for high-precision alignment. A continuous ﬂow of argon was supplied
through two internal gas inlets from a buffer volume at a 40 mbar backing pressure.
The gas escaped the open-ended capillary through holed copper electrodes (cathode upstream, anode downstream) into a large 500-mm-diameter vacuum chamber
pumped to an ambient pressure of 4.3 × 10−3 mbar.
Electron imaging spectrometer. A dipole magnet was used to perform energy
dispersion of the beam vertically onto a LANEX (ﬁne) screen mounted just outside

ARTICLE

the 1-mm-thick stainless-steel vacuum chamber wall, ~3 m downstream of the
plasma cell. Five quadrupoles (acting as a triplet) located just upstream of the
dipole were used to point-to-point image the beam from the plasma cell exit
(the object plane) to the screen (the image plane) with a magniﬁcation of R11 =
−5 (horizontally) and R33 = − 0.43 (vertically), where R is the object-to-imageplane transfer matrix. The spatial resolution of the optical system was ~50 μm (i.e.,
~2 pixels), corresponding to an energy resolution of 0.05% for particles close to the
imaged energy. Away from this imaged energy, the energy resolution degrades
depending on the vertical divergence of the bunch.
Wakeﬁeld signal extraction. The wakeﬁeld signal of a bunch slice is given by the
difference in the energy spectrum between two consecutive collimator steps. All
energy spectra (shots i) at collimator step s + 1 are subtracted from all energy
spectra (shots j) at collimator step s, and subsequently ﬁtted with a Gaussian
distribution. Difference signals with a Gaussian peak μij further away than 10 MeV
from an initial peak estimate areP
rejected. Each event i of collimator step s has an
attributed mean signal at Ei ¼ n1 nj¼1 μij , where n is the number of shots per step.
The resulting energy signal
P between collimator steps s and s + 1 is given by the
mean energy Esþ1=2 ¼ n1 ni¼1 Ei . The standard deviation of Es is used as the
uncertainty of the signal. This uncertainty represents statistical ﬂuctuations and is
connected to the stability of the beam–plasma interaction. The same wakeﬁeldsignal extraction routine is used for all datasets. The presented wakeﬁelds are
spliced from three datasets imaging at low, middle and high energies onto the
spectrometer screen (1109, 1122 and 1135 MeV, respectively).
Temporal calibration of collimator steps. The collimator position scan is
mimicked by a virtual energy-collimation scan on the reconstructed longitudinalphase-space measurement (Supplementary Fig. 1a). The subtraction signal of two
current proﬁles of consecutive collimator positions is ﬁtted with a Gaussian distribution, where the peak position is used for the collimator-to-longitudinalposition calibration. Comparing the remaining charge measured in both the real
and the virtual collimator scans (Supplementary Fig. 1b) can then be used to
determine the corresponding longitudinal position within the bunch at each
individual collimator step (Supplementary Fig. 1c). An additional compression
factor of 1.09 from the extraction line is also taken into account—this factor is
determined by the lattice conﬁguration (R56 = −3 mm) in the dispersive section of
the beamline.
Transverse beam characteristics. The transverse phase space of the beam was
measured using a two-BPM tomography technique28. The phase space of the
centroid jitter measured with two BPMs (upstream and downstream of the plasma
chamber) allows the Twiss parameters of the beam to be estimated—a measurement based on the observation that the Twiss parameters of the jitter phase space
are similar to those of the beam phase space. Combining this measurement with a
head-and-tail-collimator position scan, which allows passage of 0.1% rms energy
slices, enables an energetically resolved (and because of the strong chirp also
temporally resolved) characterisation of the transverse phase space. The sliced
emittance in the horizontal plane was determined using a quadrupole scan on the
electron spectrometer, indicating a normalised emittance between 1 mm mrad
(tail) and 10 mm mrad (head)—a variation likely to be caused by transverse kicks
from coherent synchrotron radiation (CSR). The emittance in the vertical plane
could not be measured directly, but was estimated to be 0.5–1 mm mrad—a typical
value measured directly at the gun, not expected to be affected by CSR during
transport. The beam was focused to beta functions of ~10 × 10 mm2, with a waist
close to the plasma entrance, with a relatively large chromaticity (correlation
between slice energy and waist location) in the vertical plane caused by asymmetric
focusing in the ﬁnal-focusing quadrupoles.
Longitudinal plasma density proﬁle. Two complimentary diagnostics techniques
were used to characterise the density proﬁle evolution of the argon plasma29. Twocolour laser interferometry was used to measure the longitudinally integrated
average plasma density (see Fig. 2c), and Stark broadening allowed the density to be
longitudinally resolved. This was performed with a replica cell in a dedicated test
laboratory. Supplementary Figure 2 shows the proﬁle and evolution of the plasma
density between 4 and 10 μs after the discharge, where the argon was doped with
5% hydrogen to enable Stark broadening of the H-alpha line. The density measurements were ﬁtted (see Supplementary Fig. 2a) to obtain longitudinal proﬁles at
7.5 and 9.3 μs, which were then scaled to the corresponding absolute average
density in pure argon (shown in Supplementary Fig. 2b).
Particle-in-cell simulations. The 3D quasistatic particle-in-cell code HIPACE32
was used to simulate the full evolution of the beam–plasma interaction. The input
beam was generated based on the 6D-phase-space information of the experimentally characterised beam. It was modeled with 0.2 × 106 constant-weight numerical
particles. Similarly, a 33-mm-long longitudinally tailored plasma-density proﬁle
was implemented based on density measurements (see above). The plasma
was sampled with 4 particles per cell. A simulation box of size 20 × 20 × 7 k3
p
(in x × y × ξ) was resolved by a grid of 1024 × 1024 × 200 cells, evolved with a

NATURE COMMUNICATIONS | (2020)11:5984 | https://doi.org/10.1038/s41467-020-19811-9 | www.nature.com/naturecommunications

5

## PDF page 6

ARTICLE

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-020-19811-9

constant time step of 3.5 ω1
p , where kp and ωp are the plasma wavenumber and
frequency, respectively. The resulting longitudinally averaged, on-axis electric ﬁelds
were used for comparison to the experimentally measured wakeﬁelds (see Fig. 4).

Data availability
The data that support the ﬁndings of this study are available from the corresponding
author upon reasonable request.

Received: 10 July 2020; Accepted: 29 October 2020;

26. Ayvazyan, V. et al. First operation of a free-electron laser generating GW
power radiation at 32 nm wavelength. Eur. Phys. J. D 37, 297–303 (2006).
27. Schröder, S. et al. Tunable and precise two-bunch generation at
FLASHForward. J. Phys. Conf. Ser. 1596, 012002 (2020).
28. Lindstrøm, C. A. et al. Matching small β functions using centroid jitter and
two beam position monitors. Phys. Rev. Accel. Beams 23, 052802 (2020).
29. Garland, J. M. et al. Evolution of longitudinal plasma-density proﬁles in
discharge capillaries for plasma wakeﬁeld accelerators. Preprint at http://arxiv.
org/abs/2010.02567 (2020).
30. Katsouleas, T. et al. Beam loading in plasma accelerators. Part. Accel. 18,
81–99 (1987).
31. Tzoufras, M. et al. Beam loading in the nonlinear regime of plasma-based
acceleration. Phys. Rev. Lett. 101, 145002 (2008).
32. Mehrling, T. et al. HiPACE: a quasi-static particle-in-cell code. Plasma Phys.
Control. Fusion 56, 84012 (2014).

References
1.
2.
3.
4.

5.
6.
7.

8.
9.

10.
11.
12.

13.

14.

15.
16.
17.
18.

19.

20.

21.
22.

23.
24.
25.

6

Tajima, T. & Dawson, J. M. Laser electron accelerator. Phys. Rev. Lett. 4,
267–270 (1979).
Joshi, C. & Katsouleas, T. C. Plasma accelerators at the energy frontier and on
tabletops. Phys. Today 56, 47–53 (2003).
Couprie, M. E., Loulergue, A., Labat, M., Lehe, R. & Malka, V. Towards a free
electron laser based on laser plasma accelerators. J. Phys. B 47, 234001 (2014).
Chen, P., Dawson, J. M., Huff, R. W. & Katsouleas, T. Acceleration of electrons
by the interaction of a bunched electron beam with a plasma. Phys. Rev. Lett.
54, 693–696 (1985).
Ruth, R. D., Chao, A. W., Morton, P. L. & Wilson, P. B. A plasma wake ﬁeld
accelerator. Part. Accel. 17, 171 (1985).
Blumenfeld, I. et al. Energy doubling of 42 GeV electrons in a metre-scale
plasma wakeﬁeld accelerator. Nature 445, 741 (2007).
Lu, W., Huang, C., Zhou, M., Mori, W. B. & Katsouleas, T. Nonlinear theory
for relativistic plasma wakeﬁelds in the blowout regime. Phys. Rev. Lett. 96,
165002 (2006).
Madey, J. M. J. Stimulated emission of bremsstrahlung in a periodic magnetic
ﬁeld. J. Appl. Phys. 42, 1906–1913 (1971).
Adli, E. et al. A beam driven plasma-wakeﬁeld linear collider: from higgs
factory to multi-tev. SLAC Internal Report SLAC–PUB–15426. Preprint at
http://arxiv.org/abs/1308.1145 (2013).
Litos, M. et al. High-efﬁciency acceleration of an electron beam in a plasma
wakeﬁeld accelerator. Nature 515, 92 (2014).
Loisch, G. et al. Observation of high transformer ratio plasma wakeﬁeld
acceleration. Phys. Rev. Lett. 121, 693–696 (2018).
Roussel, R. et al. Single shot characterization of high transformer ratio
wakeﬁelds in nonlinear plasma acceleration. Phys. Rev. Lett. 124, 044802
(2020).
Downer, M. C., Zgadzaj, R., Debus, A., Schramm, U. & Kaluza, M. C.
Diagnostics for plasma-based electron accelerators. Rev. Mod. Phys. 90,
035002 (2018).
Sävert, A. et al. Direct observation of the injection dynamics of a laser
wakeﬁeld accelerator using few-femtosecond shadowgraphy. Phys. Rev. Lett.
115, 055002 (2015).
Matlis, N. H. et al. Snapshots of laser wakeﬁelds. Nat. Phys. 2, 749 (2006).
Kaluza, M. C. et al. Measurement of magnetic-ﬁeld structures in a laserwakeﬁeld accelerator. Phys. Rev. Lett. 105, 115002 (2010).
Buck, A. et al. Real-time observation of laser-driven electron acceleration. Nat.
Phys. 7, 543–548 (2011).
Zhang, C. J. et al. Femtosecond probing of plasma wakeﬁelds and observation
of the plasma wake reversal using a relativistic electron bunch. Phys. Rev. Lett.
119, 064801 (2017).
Altenmueller, O. H., Larsen, R. R. & Loew, G. A. Investigations of travelingwave separators for the stanford two-mile linear accelerator. Rev. Sci. Instrum.
35, 438–442 (1964).
Emma, P., Frisch, J. & Krejcik, P. A transverse RF deﬂecting structure for
bunch length and phase space diagnostics. SLAC LCLS Technical Report No.
LCLS–TN–00–12, SLAC, California, USA (2000).
Muggli, P. et al. Meter-scale plasma-wakeﬁeld accelerator driven by a matched
electron beam. Phys. Rev. Lett. 93, 014802 (2004).
Behrens, C. & Gerth, C. Measurement of the slice energy spread induced by a
transverse deﬂecting rf structure at ﬂash. in Proc. DIPAC2011 (JACoW,
Hamburg, Germany, 2011).
Clayton, C. E. et al. Self-mapping the longitudinal ﬁeld structure of a
nonlinear plasma accelerator cavity. Nat. Commun. 7, 12483 (2016).
Mehrling, T. et al. Transverse emittance growth in staged laser-wakeﬁeld
acceleration. Phys. Rev. ST Accel. Beams 15, 111303 (2012).
D’Arcy, R. et al. FLASHForward: plasma wakeﬁeld accelerator science
for high-average-power applications. Phil. Trans. R. Soc. A 377, 20180392
(2019).

Acknowledgements
We gratefully acknowledge the Gauss Centre for Supercomputing e.V. (www.gausscentre.eu) for funding this project by providing computing time through the John von
Neumann Institute for Computing (NIC) on the GCS Supercomputer JUWELS at Jülich
Supercomputing Centre (JSC). This work was supported by the Helmholtz ARD program. The authors would like to show their gratitude to the FLASH Leadership as well as
the DESY FH and M divisions for their scientiﬁc, engineering and technical support.

Author contributions
S.S. and J.O. conceived the idea of the wakeﬁeld sampling method. S.S. and C.A.L. carried
out the experiments with the assistance of S.W., J.Z, P.G. and V.L., S.S. performed the
data analysis with the assistance of J.O. and C.A.L., C.A.L. determined the transverse
beam characteristics. S.S. performed the simulations with assistance of S.D. and M.Z. L.S.,
G.T. and M.J.G. set up the plasma density diagnostics with the assistance of S.B. and K.P.
M.J.G. measured the longitudinal plasma density proﬁle. G.B. developed the model for
the plasma density extrapolation. S.S. and C.A.L. prepared the paper with the assistance
of J.O., R.D., B.Schmidt and G.B.. C.A.L. created the equipment diagram Fig. 2. S.W.,
V.L., S.S., J.Z., R.D., P.N., L.S., A.K. and B.Sheeran contributed to the commissioning of
the beam line. J.O., R.D. and B.Schmidt supervised the project. All authors discussed the
results presented in the paper.

Funding
Open Access funding enabled and organized by Projekt DEAL.

Competing interests
The authors declare no competing interests.

Additional information
Supplementary information is available for this paper at https://doi.org/10.1038/s41467020-19811-9.
Correspondence and requests for materials should be addressed to S.S.
Peer review information Nature Communications thanks Vladimir N Litvinenko and
the other, anonymous, reviewer(s) for their contribution to the peer review of this work.
Peer reviewer reports are available.
Reprints and permission information is available at http://www.nature.com/reprints
Publisher’s note Springer Nature remains neutral with regard to jurisdictional claims in
published maps and institutional afﬁliations.

Open Access This article is licensed under a Creative Commons
Attribution 4.0 International License, which permits use, sharing,
adaptation, distribution and reproduction in any medium or format, as long as you give
appropriate credit to the original author(s) and the source, provide a link to the Creative
Commons license, and indicate if changes were made. The images or other third party
material in this article are included in the article’s Creative Commons license, unless
indicated otherwise in a credit line to the material. If material is not included in the
article’s Creative Commons license and your intended use is not permitted by statutory
regulation or exceeds the permitted use, you will need to obtain permission directly from
the copyright holder. To view a copy of this license, visit http://creativecommons.org/
licenses/by/4.0/.
© The Author(s) 2020, corrected publication 2021

NATURE COMMUNICATIONS | (2020)11:5984 | https://doi.org/10.1038/s41467-020-19811-9 | www.nature.com/naturecommunications
