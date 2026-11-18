Source: https://iopscience.iop.org/article/10.3847/2041-8213/ac6674/pdf
PDF sha256: 49a21c9ab19d3f163b7f89a710132dfb3b2e39f5b0a0286d114155e057d8e126
License: CC-BY
Language: eng
Fidelity: machine-gated

# Transcription of akiyama_2022_first_sagittarius_event_horizon_telescope.pdf

Transcription of `akiyama_2022_first_sagittarius_event_horizon_telescope.pdf` in this directory, 21 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-21 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

The Astrophysical Journal Letters, 930:L12 (21pp), 2022 May 10

https://doi.org/10.3847/2041-8213/ac6674

© 2022. The Author(s). Published by the American Astronomical Society.

First Sagittarius A* Event Horizon Telescope Results. I. The Shadow of the Supermassive
Black Hole in the Center of the Milky Way
The Event Horizon Telescope Collaboration
(See the end matter for the full list of authors.)
Received 2022 March 25; revised 2022 April 4; accepted 2022 April 8; published 2022 May 12

Abstract
We present the ﬁrst Event Horizon Telescope (EHT) observations of Sagittarius A* (Sgr A*), the Galactic center source
associated with a supermassive black hole. These observations were conducted in 2017 using a global interferometric
array of eight telescopes operating at a wavelength of λ = 1.3 mm. The EHT data resolve a compact emission region with
intrahour variability. A variety of imaging and modeling analyses all support an image that is dominated by a bright, thick
ring with a diameter of 51.8 ± 2.3 μas (68% credible interval). The ring has modest azimuthal brightness asymmetry and
a comparatively dim interior. Using a large suite of numerical simulations, we demonstrate that the EHT images of
Sgr A* are consistent with the expected appearance of a Kerr black hole with mass ∼4 × 106 Me, which is inferred to
exist at this location based on previous infrared observations of individual stellar orbits, as well as maser proper-motion
studies. Our model comparisons disfavor scenarios where the black hole is viewed at high inclination (i > 50°), as well as
nonspinning black holes and those with retrograde accretion disks. Our results provide direct evidence for the presence of
a supermassive black hole at the center of the Milky Way, and for the ﬁrst time we connect the predictions from
dynamical measurements of stellar orbits on scales of 103–105 gravitational radii to event-horizon-scale images and
variability. Furthermore, a comparison with the EHT results for the supermassive black hole M87* shows consistency
with the predictions of general relativity spanning over three orders of magnitude in central mass.
Uniﬁed Astronomy Thesaurus concepts: Black holes (162); Kerr black holes (886); Rotating black holes (1406);
Heterodyne interferometry (726); Galactic center (565)
ebbs and ﬂows of black hole activity and growth proceed is a
major outstanding question in the ﬁeld.
With the advent of the Event Horizon Telescope (EHT), SMBHs
can now be studied with direct imaging (Event Horizon Telescope
Collaboration et al. 2019a, 2019b, 2019c, 2019d, 2019e,
2019f, 2021a, 2021b, hereafter M87* Papers I–VIII). The combination of an event horizon and strong lensing near black holes is
predicted to produce distinctive gravitational signatures in their
images (e.g., Hilbert 1917; Bardeen 1973; Luminet 1979;
Jaroszynski & Kurpiewski 1997; Falcke et al. 2000). In particular,
simulated images of black holes typically have a central brightness
depression encircled by a bright emission ring. The ring usually lies
near the gravitationally lensed photon orbits that deﬁne the
boundary of what we hereafter refer to as the black hole “shadow.”
The shadow has an angular diameter dsh ≈ 10GM/(c2D) ≡ 10θg,
where G is the gravitational constant, c is the speed of light, M is
the black hole mass, and D is the black hole distance.
From the ﬁrst realization that SMBHs could power bright radio
cores in many galactic nuclei (Lynden-Bell 1969, and references
therein), the search has been on to identify them. Within our own
Galaxy, the compact source Sgr A* has been intensely studied as a
candidate SMBH since its discovery as a bright source of radio
emission located near the Galactic center (Balick & Brown 1974;
Ekers et al. 1975; Lo et al. 1975). Decades of monitoring its proper
motion, as well as motions of individual stars in orbit around it,
have revealed Sgr A* to be an extremely dense concentration of
mass (M ≈ 4 × 106 Me) that is located at and nearly motionless
with respect to the dynamical center of the Galaxy (D ≈ 8 kpc),
providing strong evidence that it is the nuclear SMBH in our
Galaxy (e.g., Do et al. 2019; Gravity Collaboration et al. 2019;
Reid & Brunthaler 2020). As the nearest SMBH, Sgr A* provides
a unique opportunity to directly image such an object, together

1. Introduction
Black holes are among the boldest and most profound
predictions of Einstein’s theory of general relativity (GR;
Einstein 1915). Originally studied as a mathematical consequence of GR rather than as physically relevant objects
(Schwarzschild 1916), they are now believed to be generic and
sometimes inevitable outcomes of gravitational collapse (Oppenheimer & Snyder 1939; Penrose 1965). In GR, the spacetime
around astrophysical black holes is predicted to be uniquely
described by the Kerr metric, which is entirely speciﬁed by the
black holeʼs mass and angular momentum or “spin” (Kerr 1963).
The ﬁrst empirical evidence for their existence was through
stellar-mass black holes, beginning with observations of X-ray
binary orbits (Bolton 1972; Webster & Murdin 1972;
McClintock & Remillard 1986) and culminating in the
detection of gravitational waves from merging stellar-mass
black holes (Abbott et al. 2016). In parallel, the discovery that
quasars are not stellar in nature but are rather extremely
luminous, compact objects located in the centers of distant
galaxies (Schmidt 1963) led to an intensive effort to identify
and measure the supermassive black holes (SMBHs) energetically favored to power them (Lynden-Bell 1969). Observations now suggest that SMBHs not only lie at the center of
nearly every galaxy (Richstone et al. 1998) but also may play a
role in their evolution (see, e.g., Magorrian et al. 1998;
Fabian 2012; Kormendy & Ho 2013), though how exactly the
Original content from this work may be used under the terms
of the Creative Commons Attribution 4.0 licence. Any further
distribution of this work must maintain attribution to the author(s) and the title
of the work, journal citation and DOI.

1

## PDF page 2

The Astrophysical Journal Letters, 930:L12 (21pp), 2022 May 10

Event Horizon Telescope Collaboration et al.

with its accretion system, in the most common, quiescent state of
SMBHs across the universe. It also provides the chance to
elucidate some of the drivers of observed cycles in accretion power
and jet launching, via comparison with the more “active” galactic
nucleus M87*.
In this paper, we present the ﬁrst EHT observations of Sgr A*
and put them into context with our previous results on M87*. In
Section 2, we describe what was previously known about the
physical properties of Sgr A* and compare them to M87*. We
then summarize our Sgr A* observations with the EHT and other
observatories in Section 3 and discuss its variability in Section 4.
In Section 5, we present the ﬁrst EHT images of Sgr A* and
analyze its event-horizon-scale structure. In Section 6 we discuss
the astrophysical interpretation of these results using an extensive
suite of general relativistic magnetohydrodynamic (GRMHD)
simulations, and in Section 7 we present the constraints that these
results give for GR and black hole alternatives. We provide the
overall conclusions and outlook in Section 8. The ﬁve companion
papers of this series provide a more comprehensive discussion of
all these topics (Event Horizon Telescope Collaboration et al.
2022a, 2022b, 2022c, 2022d, 2022e, hereafter Papers II–VI).

2000). Such a spectrum can, however, result from any stratiﬁed,
self-absorbed synchrotron source, where successively higher
frequencies are produced at increasingly smaller scales, even
without a jet (e.g., Narayan et al. 1995). SgrA* shows an excess of
millimeter emission above the ﬂat centimeter-wave spectrum, the
so-called “submillimeter bump,” that was inferred to indicate the
presence of a very compact emitting region at these wavelengths
(e.g., Zylka et al. 1992; Falcke et al. 1998).
To clarify the nature of this source, the structure of Sgr A*
was investigated using very long baseline interferometry
(VLBI) at progressively shorter wavelengths (see Paper II,
and references therein). For wavelengths longer than several
centimeters, the observed source size is entirely determined by
scatter broadening in the ionized interstellar medium, scaling
with a wavelength dependence of λ2. At wavelengths of 7 mm
and shorter, the imprint of the intrinsic structure of Sgr A*
became discernible through the scattering (e.g., Rogers et al.
1994; Lo et al. 1998; Doeleman et al. 2001; Bower et al. 2004;
Shen et al. 2005; Bower et al. 2006). The source grows more
compact at shorter wavelengths, as expected (e.g., Özel et al.
2000), though it does not present a clear jet structure. For
wavelengths as short as ∼1 mm, Sgr A* is only slightly blurred
by scattering, and Falcke et al. (2000) predicted that
submillimeter VLBI could directly image a brightness depression within this region related to the black hole shadow.
In parallel with these developments and motivated by the
goal to study black holes, the capabilities of mm-VLBI
improved rapidly. At 1.4 mm, Padin et al. (1990) reported the
ﬁrst VLBI fringes and Krichbaum et al. (1998) obtained the
ﬁrst VLBI detections and associated source size measurements
for Sgr A*, each using a two-element interferometer. Doeleman
et al. (2008) observed Sgr A* at 1.3 mm with a three-element
VLBI array and reported the discovery of an intrinsic source
size comparable to the expected angular diameter of the black
hole shadow. These observations provided important constraints for theoretical models (e.g., Broderick et al. 2009;
Dexter et al. 2009; Mościbrodzka et al. 2009) and strongly
suggested that 1.3 mm VLBI has a clear view into the
innermost region around the Sgr A* black hole. Subsequent
VLBI studies of Sgr A* at 1.3 mm with progressively enhanced
arrays revealed the compact emission to be variable and
signiﬁcantly polarized, with measured “closure phases” that are
indicative of persistent asymmetry in the image structure (Fish
et al. 2011; Johnson et al. 2015; Lu et al. 2018).
Observations of Sgr A* outside the radio band were
important for completing the picture of this source as an
LLAGN. When X-ray and gamma-ray instruments ROSAT and
Sigma/GRANAT (Goldwurm et al. 1994; Predehl & Truemper 1994) could not identify a bright central source, it became
clear that Sgr A* must be either obscured or anomalously faint
compared to other known LLAGNs. The ﬁrst identiﬁcation of
Sgr A* as a compact and variable source in the X-rays was
achieved with the Chandra X-ray Observatory (Baganoff et al.
2001, 2003). This detection, together with the ∼ 4 × 106 Me
mass of Sgr A* determined from stellar orbits, sets a maximum
luminosity scale for the source, the so-called Eddington
luminosity,177 and the X-ray measurements conﬁrmed that
Sgr A* is approximately 9 orders magnitude less luminous than

2. Sgr A* and M87*
Decades of observations have provided a picture of our local
SMBH that is unmatched in any other galaxy (for details about the
full spectrum, see Paper II). Sgr A* has been detected from long
radio wavelengths (∼1 m) to the hard X-ray band, excepting
approximately 1 μm to 1 nm owing to extinction from dust in the
Galactic plane. Sgr A* is remarkable for its feeble emission,
producing a bolometric luminosity of 1036 erg s−1, only ∼100
times that of the Sun. Were it located in another galaxy, it would
likely go undetected. Nevertheless, by observing its spectrum and
variability, its environment, and its inﬂuence on surrounding
bodies, a great deal has been learned about this source speciﬁcally
and about the astrophysical processes that operate around SMBHs.
In this section we describe how we assembled our current
knowledge of Sgr A*, discuss important theoretical uncertainties
about its accretion and outﬂows, and compare it with the other
horizon-scale EHT target, M87*.
2.1. Properties of Sgr A*
The proximity of Sgr A* permits precise measurements of its
gravitating mass via the monitoring of resolved individual stellar
orbits. High-resolution infrared (IR) observations, using increasingly sophisticated instrumentation and analyses, have traced out
the three-dimensional orbits of several stars within the innermost
arcsecond around Sgr A* (Schödel et al. 2002; Ghez et al.
2003, 2008; Gillessen et al. 2009; Gravity Collaboration et al.
2018a; Do et al. 2019; Gravity Collaboration et al. 2019). These
orbits jointly determine the mass and distance to Sgr A* to high
precision, particularly the ratio M/D that determines the angular
size of the black hole on the sky. As discussed in Paper II and
Paper VI, the current values for the mass and distance suggest an
angular shadow diameter close to 50 μas, comparable to that of
M87*. The closest orbital periapses conﬁne the mass to within
∼1,000 Schwarzschild radii (RS = 2GM/c2).
Radio observations of SgrA* have provided a signiﬁcant
motivation for the development of the EHT experiment. SgrA*
shows a ﬂat/inverted radio spectrum, which often arises from
compact jet emission (Blandford & Königl 1979) in other lowluminosity active galactic nuclei (LLAGNs; Ho 1999; Nagar et al.

177

The Eddington luminosity is an idealized estimate of the maximum power
for an accreting black hole: LEdd º 4pGMcmp sT » 10 38(M M) erg s−1,
where σT is the Thomson cross section and mp is the mass of a proton.

2

## PDF page 3

The Astrophysical Journal Letters, 930:L12 (21pp), 2022 May 10

Event Horizon Telescope Collaboration et al.

its LEdd—the lowest Eddington ratio (L/LEdd) observed for any
black hole.
This particularly faint high-energy emission stimulated a
lively debate regarding the nature of Sgr A*’s accretion/
outﬂow properties and motivated new theoretical developments. If the emission primarily originates in the accretion
inﬂow, either it must be exceptionally radiatively inefﬁcient
(Narayan et al. 1995), or the accretion rate onto the black hole
must be very small compared to what is captured, or possibly
some combination of the two (Blandford & Begelman 1999;
Narayan et al. 2000; Quataert & Gruzinov 2000a; Yuan &
Narayan 2014). Alternately, the emission could be dominated
by an outﬂow, in which case a small accretion rate would also
be favored (Falcke et al. 1993), even during ﬂares (Markoff
et al. 2001). Fortunately, the proximity of Sgr A* enables
unparalleled study of the accretion ﬂow. Observations with
Chandra marginally resolve thermal bremsstrahlung emission
from near the gas capture radius, leading to an estimate of the
captured accretion rate of ∼ 10−6–10−5 Me yr−1 at ∼ 105RS
(Quataert 2002; Baganoff et al. 2003). The source of this gas
can be connected to the observable stellar winds of ∼ 30
individual massive stars found in the inner parsec (Coker et al.
1999; Russell et al. 2017; Ressler et al. 2020). The near-horizon
accretion rate has also been estimated to be
10−9–10−7 Me yr−1 through measurements of the Faraday
rotation of polarized millimeter emission from Sgr A* (Bower
et al. 2003; Marrone et al. 2006, 2007). This Faraday rotation is
orders of magnitude smaller than would be expected if the
accretion rate at the gas capture radius persisted to small radii
(Bower et al. 1999; Agol 2000; Quataert & Gruzinov 2000b;
Marrone et al. 2006). This conclusion is further supported by
radially resolved X-ray spectroscopy (Wang et al. 2013),
suggesting that only ∼ 1% of the captured mass makes it to the
SMBH. Taken together, the low luminosity, low radiative
efﬁciency, and weak Faraday rotation are consistent with a
weakly bound, magnetized accretion ﬂow so diffuse that the
electron and ion temperatures are unable to remain strongly
coupled.
Finally, Sgr A* exhibits ﬂaring emission at most wavelengths, including continuous variability at millimeter wavelengths. In particular, approximately daily ﬂares are observed at
X-ray and NIR wavelengths that are often (but not always)
simultaneous (e.g., Eckart et al. 2004) and that change on
timescales as short as minutes (e.g., Baganoff et al. 2001;
Genzel et al. 2003). These timescales suggest an origin from
within ∼ 5RS of the SMBH, which is consistent with
astrometry of NIR ﬂares using the GRAVITY instrument on
the Very Large Telescope Interferometer (Gravity Collaboration et al. 2018b).

Paper VIII). Most likely this higher power indicates that
M87* is being fed directly from a larger reservoir of gas rather
than a trickle from stellar winds. This difference may underlie
another substantial divergence between the sources: the
prominent, powerful jet launched from M87*, which can be
traced at multiple wavelengths and across nearly eight orders of
magnitude in size (EHT MWL Science Working Group et al.
2021). The M87* jet provides ﬁrm constraints on the source
orientation with respect to the line of sight; thus, an inclination
of ∼20° was used for numerical simulations in M87* Paper V,
while for Sgr A* we do not have any such constraints.
The difference in the masses of Sgr A* and M87* implies a
similar difference in their variability timescales. The period of
the innermost stable circular orbit (ISCO), which depends on
the mass and spin of the black hole, serves as an approximate
dynamical timescale. For prograde orbits, this period ranges
from 4πtg (maximal spin) to 12 6 ptg (zero spin), where
tg ≡ GM/c3. For M87*, this range corresponds to 5 days to
1 month, so the source structure is expected to be effectively
unchanged over the course of an observing night. Indeed, EHT
images of M87* reconstructed on consecutive nights are almost
identical (M87* Paper IV). However, for Sgr A*, the range is
only 4–30 minutes, so the source structure can evolve within a
single night.
3. EHT Observations and Data Processing
In this section we summarize the EHT observations and data
processing for Sgr A*. We refer the reader to M87* Paper II for
a comprehensive discussion of the EHT instrument, M87*
Paper III for details on the 2017 observing campaign and data
processing, and Paper II for additional details speciﬁc to the
Sgr A* data processing.
In 2017, the EHT observed Sgr A* on ﬁve nights between
April 5 and 11 using an array with eight participating
observatories (see Figure 1). Weather conditions were good
or excellent at all sites on all ﬁve observing nights. The most
sensitive element in the array, the Atacama Large Millimeter/
submillimeter Array (ALMA), only observed Sgr A* on April
6, 7, and 11; the IRAM 30 m Telescope (PV) only observed
Sgr A* on April 7. In this initial series of papers, we focus on
the observation with the best baseline coverage: April 7. In
addition, we utilize the April 6 observations for testing,
validation, and selected multiday analyses. Our multiwavelength coverage indicated that there was an X-ray ﬂare on
April 11, accompanied by increased 1.3 mm variability; we will
consider that more complex data set in future work.
Each site, except the JCMT and ALMA, received data in two
circular polarizations simultaneously. The JCMT received a
single circular polarization, and ALMA received orthogonal
linear polarizations that are converted to a circular basis in postprocessing. All EHT sites recorded data in two frequency bands
at 227.1 and 229.1 GHz, referred to as the “low” and “high”
bands, respectively. The total recording rate at each fully
outﬁtted station is 32 GB s–1. The data were written to arrays of
hard drives at each site, which were then brought from all sites
to common locations where we computed the complex crosscorrelation in the electric ﬁelds measured for each pair of
stations.
Following the initial computation of these correlations,
residual phase and bandpass errors were corrected with two
independent processing pipelines, EHT-HOPS (Blackburn
et al. 2019) and rPICARD (Janssen et al. 2019). The data

2.2. Comparison to M87*
M87* and Sgr A* have the largest angular sizes of any
known SMBHs, making them the primary EHT targets.
However, they differ in several important ways. First, they
have substantially different luminosities and accretion rates,
both in absolute terms and when scaled by mass. M87*,
roughly 1500 × more massive (M = (6.5 ± 0.7) × 109 Me;
M87* I), has an inferred accretion rate of M ~ 10-3 M yr-1
and a bolometric luminosity of Lbol ≈ 1042 erg s−1 measured in
2017 (EHT MWL Science Working Group et al. 2021).
Estimates of the total kinetic power are typically ∼10–100
times larger, thus conservatively L/LEdd  10−5 (M87*
3

## PDF page 4

The Astrophysical Journal Letters, 930:L12 (21pp), 2022 May 10

Event Horizon Telescope Collaboration et al.

Figure 1. The 2017 EHT array as seen from Sgr A*. The array included eight observatories at six locations: the Atacama Large Millimeter/submillimeter Array
(ALMA) and the Atacama Pathﬁnder Experiment (APEX) on the Llano de Chajnantor in Chile, the Large Millimeter Telescope Alfonso Serrano (LMT) on Volcán
Sierra Negra in Mexico, the James Clerk Maxwell Telescope (JCMT) and Submillimeter Array (SMA) on Maunakea in Hawai’i, the Institut de Radioastronomie
Millimétrique 30 m telescope (PV) on Pico Veleta in Spain, the Submillimeter Telescope (SMT) on Mt. Graham in Arizona, and the South Pole Telescope (SPT) in
Antarctica.

were then a priori calibrated using the system equivalent ﬂux
densities (SEFDs) for each telescope. Multiplication by the
geometric mean of the SEFDs of the two stations on a given
baseline converts dimensionless correlation coefﬁcients to ﬂux
densities. SEFDs ranged from 60 Jy at ALMA to 5 × 104 Jy at
low elevation at SMT. Further corrections are still required, as
some sites do not measure the SEFD continuously, and in any
case the SEFD does not capture many amplitude-corrupting
effects such as pointing and focus errors. A “network
calibration” process, which uses redundancies in the array
(e.g., colocated telescopes) to provide more accurate timevariable gain normalization for sites with colocated partners,
was performed. Sgr A* presents a special case for calibration,
as it varies signiﬁcantly in time and is surrounded by extended
emission that corrupts the visibility amplitude for baselines
within local arrays like ALMA and SMA. Wielgus et al. (2022)
discuss the techniques used to estimate the time-resolved ﬂux
density of Sgr A* for this calibration. For the remaining
stations, gain corrections were computed using observations of
the calibrator targets J1924–2914 and NRAO 530 (Paper II).
Figure 2 shows the EHT baseline coverage and interferometric visibility amplitudes (“visibilities”) for Sgr A*. The
longest baselines have an interferometric fringe spacing of
1/|u| ≈ 24 μas, which deﬁnes the diffraction-limited angular
resolution of the EHT. The visibility amplitudes have two deep
minima, the ﬁrst at |u| ≈ 3.0 Gλ and the second at |u| ≈ 6.5 Gλ.
The amplitudes have a baseline dependence that is similar to
that of an inﬁnitesimally thin ring with a 54 μas diameter that
has been blurred with a circular Gaussian kernel with 23 μas
FWHM. The ring diameter is primarily constrained by the
minima locations, while the width is determined by the
amplitude of the secondary visibility peak between the minima.
For instance, to be consistent with both a ﬁrst minimum falling
between 2.5 and 3.5 Gλ and a second minimum falling between
6 and 7 Gλ, the ring must have a diameter of ∼50–60 μas.
However, the EHT data show evidence for complex and
asymmetric source structure beyond a simple ring model,

including a strong dependence on visibility amplitudes with the
baseline position angle (especially near the ﬁrst visibility
minimum) and in the closure phases measured on triangles of
EHT baselines, which differ signiﬁcantly from 0° and 180°.
The EHT visibility amplitudes also show indications of residual
calibration errors. To assess and quantify the source morphology of Sgr A* more generally, we applied a variety of
imaging and modeling methods using both the interferometric
visibility amplitude and phase information (Section 5). These
methods included a variety of approaches to account for
residual calibration errors, including iterative self-calibration,
simultaneous ﬁtting of a model and the residual station gains,
and analyses that used only closure quantities.
4. Horizon-scale Variability in Sgr A*
To characterize the spectrum and variability of Sgr A*, the
EHT observing campaign was supported by parallel observations at several other observatories. Longer-wavelength VLBI
observations, where interstellar scattering prevents direct
observation of structural changes, were arranged to occur
within a few days of the EHT campaign. IR and X-ray
observations were arranged to be as simultaneous as possible
with the EHT tracks on several days, and they resulted in one
conﬁrmed X-ray ﬂare on April 11.
For the observations of April 6 and 7, when no strong ﬂares
were observed in the parallel observations, we must evaluate
whether Sgr A* has structural variations within our observation
periods. The simplest evidence for variability at λ = 1.3 mm
comes from analysis of the total ﬂux density (the “light curve”),
which is measured during EHT observations using the ALMA
and SMA connected element arrays. As discussed in Wielgus
et al. (2022), the fractional variability across all days is
approximately 9%, with variations of 4%–13% seen within
individual nights (see, e.g., Figure 2). This variability is an
order of magnitude stronger than is expected from interstellar
4

## PDF page 5

The Astrophysical Journal Letters, 930:L12 (21pp), 2022 May 10

Event Horizon Telescope Collaboration et al.

Figure 2. EHT observations of Sgr A* on April 7. Top left: EHT baseline coverage, where dimensionless coordinates u = (u, v) give the projected baseline vector for
each antenna pair in units of the observing wavelength λ. Top right: calibrated visibility amplitudes of Sgr A* as a function of projected baseline length |u|. Error bars
show ±1σ thermal (statistical) uncertainties. Diamonds denote baselines to APEX and JCMT to distinguish them from baselines to their colocated observatories,
ALMA and SMA, respectively. The visibilities have been coherently averaged in 120 s intervals. For comparison, the gray dashed line shows the Fourier transform of
a thin ring with diameter 54 μas that has been convolved with a circular Gaussian kernel of FWHM 23 μas. The red line and shaded region show the rms variability
and associated 68% credible interval over the range of baselines for which it can be accurately measured (see Paper IV), while the blue horizontal ticks at zero baseline
length show the range of variations in the total ﬂux density. Bottom: the full light curve of Sgr A* on April 7, measured using ALMA and the SMA as stand-alone
interferometers.

scintillation. Thus, the light curves provide evidence for
intrinsic image variability in Sgr A*.
Each EHT baseline provides information about the detailed
structure of this variability on an angular scale determined by
the baseline length. On several triangles, EHT closure phases
show slightly more variation than is expected from their
thermal noise, the changing of projected baselines (from the
source view) with Earth rotation, and interstellar scintillation
(Paper II). Comparison of interferometric visibility amplitudes
for nearby baselines also reveals variability that signiﬁcantly
exceeds what is expected from thermal noise, calibration
uncertainties, and baseline evolution (Paper IV).
To quantify the variability, we developed a simple
parametric model for the spatiotemporal power spectrum for
the variability of Sgr A* (Georgiev et al. 2022). This model
represents the variance in the visibility amplitude as a function
of the radial distance in the (u, v)-plane, taking the form of a
broken power law, as motivated by studies of GRMHD
simulations. The source-integrated light curve is divided out in
order to isolate structural variation from overall changes in ﬂux
density. The variability power spectrum was also empirically
estimated by analyzing variations in visibility amplitudes on
nearby baselines (Broderick et al. 2022). This comparison

included the same baselines sampled on different days, as well
as nearby or crossing baseline tracks (e.g., SPT-LMT and SPTSMA sample nearly identical baselines, but at different times).
This analysis revealed that the fractional variability can be
order unity for EHT baselines located near the two deep
visibility minima (Figure 2), even after normalizing the data to
remove light-curve ﬂuctuations, and that it signiﬁcantly
exceeds the variability expected from interstellar scintillation
(Paper IV).
5. Horizon-scale Structure in Sgr A*
Each interferometric visibility samples a single complex
Fourier component of the image on the sky (e.g., Thompson
et al. 2017). Interferometric imaging algorithms seek to
produce images from this sparse Fourier-domain information
that are consistent with the data and physically plausible.
Techniques such as the classical CLEAN algorithm and
regularized maximum likelihood (RML) methods successfully
produced EHT images of M87*, with remarkable agreement
among methods (M87* Paper IV). The EHT baseline coverage
for Sgr A* is substantially better than for M87*, primarily
because of the additional telescope (SPT) with mutual visibility
5

## PDF page 6

The Astrophysical Journal Letters, 930:L12 (21pp), 2022 May 10

Event Horizon Telescope Collaboration et al.

*

of the source. Moreover, at λ = 1.3 mm, Sgr A has a compact
ﬂux density that is approximately four times larger than that of
M87*, with no appreciable contribution to the short-baseline
visibilities from an extended jet. However, producing an image
of Sgr A* requires additional assumptions because of the rapid
source variability and interstellar scattering.
Speciﬁcally, VLBI imaging typically relies on Earth-rotation
aperture synthesis, in which the projection of each baseline
sweeps out an arc in the (u, v)-plane as the Earth rotates,
allowing a sparse array of telescopes to obtain the (u, v)coverage necessary for the imaging of a static source
(Thompson et al. 2017). To account for the source structural
variability, we used a parametric model discussed in Section 4.
By incorporating this variability error budget, imaging and
modeling methods designed for a static source can be applied
to analyze data from a variable source.
To account for the interstellar scattering, we used two
approaches (Paper III). The ﬁrst, “on-sky imaging,” applies no
modiﬁcations to the data or images. In this approach, the
algorithms simply reconstruct the scattered image of the source.
The second, “descattered imaging,” adds an error budget to
interferometric visibilities to account for stochastic scattering
substructure before deconvolving the ensemble-average scattering kernel. Both the ensemble-average kernel and the power
spectrum of scattering are used (Psaltis et al. 2018), each of
which is precisely known from an analysis combining decades
of observations of Sgr A* at centimeter wavelengths (Johnson
et al. 2018).
To test these imaging techniques and to select appropriate
imaging parameters, we developed a suite of synthetic
observations of seven geometric models that share the
scattering and variability properties of Sgr A*. This suite
included models with widely varying morphologies: rings,
disks, a crescent, a double source, and a point-like source with
an extended halo. Each model was selected to produce
visibility amplitudes that were similar to those of Sgr A*, with
two deep visibility minima, a physical scattering model
applied, and stochastic temporal evolution generated by a
statistical model (Lee & Gammie 2021).
We then selected the sets of imaging parameters that
accurately reconstruct images across the entire test suite,
including both ring and nonring data sets. These “top set”
parameter choices yield a corresponding collection of reconstructed images of Sgr A* that provide both a representative
average image and a measure of its uncertainty. In addition, we
used a new Bayesian imaging method, which simultaneously
estimates both the reconstructed image and its associated
variability noise model (Broderick et al. 2020). This method
does not require training on synthetic data, although we used
the same test suite for comparison and validation of this
method.
When applied to the Sgr A* data, over 95% of the top set
images have a prominent ring morphology. For an analysis
using the combination of April 6 and 7 data, all samples from
the Bayesian imaging posterior show a ring morphology. In
addition, geometric modeling of the EHT data shows a
consistent statistical preference for ring morphologies over
alternatives with comparable complexity. The ring has a
diameter, width, and central brightness depression that are
consistent across the different choices of imaging methods and
parameters (see Paper III). However, the reconstructed images
show diversity in their speciﬁc attributes, particularly the

Figure 3. Representative EHT image of Sgr A* from observations on 2017
April 7. This image is an average over different reconstruction methodologies
(CLEAN, RML, and Bayesian) and reconstructed morphologies. Color denotes
the speciﬁc intensity, shown in units of brightness temperature. The inset circle
shows the restoring beam used for CLEAN image reconstructions (20 μas
FWHM). The bottom panels show average images within subsets with similar
morphologies, with their prevalence indicated by the inset bars. The
multiplicity of image modes reﬂects uncertainty due to the sparse baseline
coverage; it does not correspond to different snapshots of the variable source.
Nearly all reconstructed images show a prominent ring morphology. While the
diameter and thickness of the ring are generally consistent across the
reconstructions, the azimuthal structure of the ring is poorly constrained.

azimuthal intensity distribution around the ring. This uncertainty is a consequence of the limited EHT baseline coverage,
compounded by the challenges of imaging a variable source.
We categorized the reconstructed images into four clusters
spanning the primary reconstructed structures: three clusters are
ring modes with varying position angle, while the fourth is a
comparatively small set of reconstructed images with diverse
nonring morphologies. Figure 3 shows a representative average
image of Sgr A* on April 7, as well as the average image for
each of these clusters along with their relative occurrence
frequency.
To quantify the ring parameters in a complementary way, we
used several geometrical modeling methods, the parameterizations of which were guided by the reconstructed images of
Sgr A*. These models are deﬁned by a thick ring with
azimuthal variations determined by low-order Fourier coefﬁcients and an additional Gaussian brightness ﬂoor. Because
these simple geometric models have a small number of
parameters, they can be constrained using instantaneous
6

## PDF page 7

The Astrophysical Journal Letters, 930:L12 (21pp), 2022 May 10

Event Horizon Telescope Collaboration et al.

signs of image variability, we cannot reliably constrain the
underlying image evolution.

Table 1
Measured Parameters of Sgr A*
Parameter
Emission ring:a
Diameter, d
Fractional width, W/d
Orientation, η
Brightness asymmetry, A
Angular gravitational radius,a θg
Black hole mass,b M
Angular shadow diameter,c dsh
Schwarzschild shadow deviation,c δ
Parameter
Angular gravitational radius, θg:
Stellar orbits (VLTI)d
Stellar orbits (Keck)e
Black hole distance, D:
Stellar orbits (VLTI)d
Stellar orbits (Keck)e
Masers (cm VLBI)
Black hole mass, M:
Stellar orbits (VLTI)d
Stellar orbits (Keck)e

EHT Estimate

6. Implications for Accretion and Outﬂow Physics
51.8 ± 2.3 μas
∼30–50
L
∼0.04–0.3
+1.4
4.80.7 m as
+1.1
4.0-0.6 ´ 10 6 M
48.7 ± 7.0 μas
+0.09
-0.080.09 (VLTI)
+0.09
-0.040.10 (Keck)

What can we learn from these images and their variability
properties? Focusing ﬁrst on the astrophysics of the accretion
process and jet launching, we can explore which physical
scenarios are most consistent with our results, under the
assumption that Sgr A* is a Kerr black hole with mass and
distance accurately determined from stellar orbits. Our
constraints on the properties of the black hole and potential
deviations from GR are explored in Section 7.
We assume that the accretion structure around Sgr A* is
approximately governed by ideal GRMHD, as was done for
M87*, which is common in the literature for modeling SMBHs
(see, e.g., Gammie et al. 2003). Decades of observations and
semianalytical modeling (see Paper V for details, references,
and caveats) constrain the average plasma properties close to
the event horizon of Sgr A*, allowing us to make several
additional simplifying approximations. In particular, for Sgr A*
we can assume that radiative cooling does not strongly affect
the dynamics and that the electrons and ions are weakly
coupled by Coulomb collisions, so that ions and electrons can
have distinct temperatures in some parts of the ﬂow.
Because we model the plasma as a ﬂuid with a single
temperature, one of our main sources of uncertainty is the
treatment of the electrons, whose presence is not explicitly
accounted for in the simulation evolution equations. We
explore several parameterized models to assign the electron
distribution function (eDF), assuming that the electron
temperature is proportional to the proton temperature, with a
proportionality that depends on the ratio of gas to magnetic
pressure (Chan et al. 2015). The eDFs include thermal and
nonthermal variations, the latter of which were not explored in
the M87* 2017 papers. Our ﬁducial thermal models employ the
same eDF prescription as for the M87* papers, using only one
free parameter, Rhigh, to specify the proton-to-electron temperature ratio in regions where gas pressure dominates the
magnetic pressure (Mościbrodzka et al. 2016). This ratio is
typically larger in the disk midplane than in the jet/outﬂow.
Since the radiation is produced by electrons, increasing Rhigh
effectively increases the brightness of the jets/outﬂow region
relative to the disk and changes the resulting images/spectra
(M87* Paper V). Compared to M87*, we also allow the
inclination angle to vary.
We employ ﬁve different ideal GRMHD codes to explore a
large swath of overlapping parameter space, in some cases with
very similar setups allowing for consistency checks. In other
cases, with a more exploratory sampling of parameter space,
we also allow differences in, for example, adiabatic index,
resolution, and size of the tori and/or computational domain.
Most models are initialized with an orbiting torus of plasma
with characteristic radius ∼20G M/c2. The torus is seeded with
a weak, poloidal magnetic ﬁeld and can be either prograde or
retrograde with respect to the black hole spin (a free
parameter). We also consider a limited set of exploratory
models, such as those with “tilt” where the black hole spin axis
is misaligned from the rotation axis of the torus (Liska et al.
2018; Chatterjee et al. 2020; White & Quataert 2022), as well
as a model initiated on a very large grid using a more realistic
setup for the outer boundary conditions in which the accretion
ﬂow is directly fed by winds from orbiting stars (Ressler et al.

Previous Estimate
5.125 ± 0.009 ± 0.020 μas
4.92 ± 0.03 ± 0.01 μas
8277 ± 9 ± 33 pc
7935 ± 50 ± 32 pc
8150 ± 150 pc
(4.297 ± 0.013) × 106 Me
(3.951 ± 0.047) × 106 Me

Notes.
a
The orientation and magnitude of the ring’s brightness asymmetry are poorly
constrained; they vary signiﬁcantly among the reconstructed image modes and
among different modeling and imaging methods. For details, see Paper IV.
b
To translate our estimate of θg into an estimated mass of Sgr A*, we use the
distance to Sgr A* estimated using trigonometric VLBI parallaxes and proper
motions of molecular masers in spiral arms of the Milky Way (Reid et al.
2019). For details, see Paper IV.
c
Estimates of dsh are determined solely from EHT data, but estimates of δ use
priors for θg from resolved stellar orbits as indicated. For details, see Paper VI.
d
Gravity Collaboration et al. (2022).
e
Do et al. (2019).
f
Reid et al. (2019).

snapshots of data. Hence, we used two modeling approaches.
With “snapshot” modeling, we aggregate a series of independent ﬁts to 2-minute data segments. This approach does not
require a variability model. With “full-track” modeling, we ﬁt
both a static geometric source model and a variability noise
model simultaneously to the entire 12 hr observation. Table 1
summarizes the consensus ring parameters measured using
these methods (for detailed results from individual methods,
see Paper IV).
In Paper III, we also used dynamic imaging and snapshot
ring modeling to analyze the intraday image variability in
Sgr A*. We applied these analysis methods to the 100-minute
intervals on April 6 and 7 with the best sampling (Farah et al.
2022), adopting a strong ring prior to counteract the limited
baseline coverage. On April 6, most dynamic imaging and
modeling methods recover a nearly static image, while many
reconstructions on April 7 ﬁnd an evolving image. However,
the results on April 7 are strongly affected by the underlying
prior assumptions; different parameters in the dynamic imaging
method result in different modes of position angle evolution in
the reconstructed images, including some reconstructions that
are nearly static. Thus, while the EHT data show detectable
7

## PDF page 8

The Astrophysical Journal Letters, 930:L12 (21pp), 2022 May 10

Event Horizon Telescope Collaboration et al.

Figure 4. Summary of constraints on our 200 ﬁducial GRMHD simulations. Color indicates combined EHT constraints apart from structural or ﬂux variability, and
hatching indicates combined non-EHT constraints. For each constraint category and parameter combination, we delineate whether all of the three simulation codes run
with those parameters pass, whether only some pass, or whether none pass. These exclusions leave only two models, each a MAD with prograde spin, 30° inclination,
and Rhigh = 160. For details, see Paper V.

include the ﬂux densities at 86 GHz, 2.2 μm in the NIR, and
X-ray and the major-axis source size at 86 GHz, constrained
from observations with the Global mm-VLBI Array. Finally,
the variability constraints are (1) the fractional 230 GHz
variability on 3 hr timescales, derived from more than a decade
of measurements; and (2) the structural variability of the
source, calculated at a baseline length of 4Gλ after ﬁtting a
parameterized model to the visibility amplitude variation versus
baseline length. See Paper V for the full ranges of tests and
pass/fail conditions.
Compared to M87* Paper V, we explore a larger range of
models and model parameter space, and we also include some
additional observational constraints. These include the degree
of intrinsic variability and the broadband spectral constraints
given above. Accordingly, we ﬁnd that all our models fail at
least one of the observational constraints. These results indicate
the power of combining interferometric data with other
observational constraints to narrow down the viable physical
parameter space. We now summarize our main results and their
implications for our understanding of Sgr A*’s accretion state
and geometry.
We primarily focus on a set of “ﬁducial” simulations, which
use aligned (prograde or retrograde) accretion ﬂows and
thermal eDFs deﬁned via the Rhigh prescription. We declare a
model to fully pass a set of constraints only when all GRMHD
simulations with those parameters pass. This approach helps to
ensure that our selection of favored models is resilient to small
variations in the GRMHD simulation choices and software.
Figure 4 summarizes these results.
All edge-on (high inclination) models fail the combined set
of EHT-only constraints for at least one simulation, and almost
all retrograde models (a* < 0) fail. There are two interesting
groupings of models that pass all EHT constraints for all
simulations: both have positive/prograde spin (a* = 0.5, 0.94)
with lower (  50°) inclination, but some are MAD (10) and
some are SANE (8). With only ∼ 10% pass rate for all models,
it is clear that EHT imaging data alone are capable of strongly

2020). Both of these are more realistic physical scenarios but
also allow a much larger range of parameter space than we
could fully explore.
We classify the ﬁducial models as being in either the
magnetically arrested disk (MAD; Narayan et al. 2003) or
standard and normal evolution (SANE; Narayan et al. 2012)
modes. In MAD models the ordered magnetic ﬁelds signiﬁcantly affect the dynamics of the ﬂow, episodically halting
accretion onto the black hole, while SANE models have
weaker, more turbulent magnetic ﬁelds. Because the dynamical
timescale in Sgr A* is short compared to a night of
observations, it is important to run each model for enough
time to capture the range of spectral and structural variations.
The simulations are typically run for 30,000tg, while some are
run for more than 100,000tg in order to sample a broader
distribution of behavior.
For each time-dependent GRMHD simulation, with an eDF
prescription and inclination with respect to the line of sight, we
calculate a sequence of model images (movies) using raytracing and including synchrotron emission and absorption. We
also calculate spectra including synchrotron emission and
absorption, bremsstrahlung emission, and, using Monte Carlo
methods, Compton scattering. These synthetic data sets are
then used to generate simulated EHT images, as well as
multiwavelength light curves and spectral energy distributions
(SEDs), for comparison with the Sgr A* data described in
Paper II. We scale all images to a benchmark average ﬂux
density of 2.4 Jy at 230 GHz to match the average synchrotron
ﬂux density of Sgr A* (see Paper II; Wielgus et al. 2022).
We evaluate the simulations against three types of observational constraints: EHT interferometric measurements, emission at other wavelengths, and variability. The EHT constraints
include (1) a measure of the image size; (2) salient features
from the visibility amplitudes, such as the location of the ﬁrst
deep minimum; and (3) the diameter, asymmetry, and width of
simpliﬁed ring models ﬁtted to well-sampled portions of the
April 7 visibility data. The constraints from other wavelengths
8

## PDF page 9

The Astrophysical Journal Letters, 930:L12 (21pp), 2022 May 10

Event Horizon Telescope Collaboration et al.

Figure 5. Simulated images of Sgr A*. Left: a single snapshot image of a numerical simulation of Sgr A* that passes 10 out of the 11 observational criteria described in
Paper V. Middle: the average of this simulation with time sampling that matches the EHT observational cadence on April 7. Right: representative image reconstruction
using synthetic visibilities generated from the simulation in the adjacent panels (see Appendix H in Paper III). This image has been averaged across methodologies and
reconstructed morphologies, as in Figure 3. Each panel is shown on a linear brightness scale that is normalized to its peak.

(Satapathy et al. 2022). In general, SANE models are less
variable than MADs, and face-on models are somewhat less
variable than edge-on. However, there are limitations of the
modeling that may affect the variability. For instance,
collisionless effects, radiative cooling, and improved electron
heating models could all potentially reduce variability. Thus,
our variability constraints may be too strict.
There are only two models that pass everything but the
variability constraints. The models have similar parameters:
both are MAD, both are prograde spin (one has a* = 0.5, and
the other has a* = 0.94), and both have i = 30° and
Rhigh = 160. Figure 5 shows a representative snapshot from
one of these simulations and its corresponding image
reconstruction. If we take these two models as indicative,
there is a preference for accretion rates at the lower end of the
range found by other constraints, 10−9–10−8 Me yr−1, and an
outﬂow power of ∼ 1038 erg s−1, which is comparable to the
bolometric luminosity of stellar-mass black holes in X-ray
binaries. The combination of high Rhigh and relatively low
inclination satisﬁes the spectral constraints without their
associated jet structure producing too much asymmetry to
satisfy the EHT constraints. A low inclination is also consistent
with the independent estimate based on tracking the motions of
NIR ﬂaring structures using the VLTI (Gravity Collaboration
et al. 2018b). Our results highlight the value of continued EHT
plus multiwavelength monitoring of Sgr A*, and there is clearly
much more exploration to conduct, including improved
theoretical models and numerical simulations, full SED
modeling, and polarimetric imaging, all of which will yield
deeper physical insights (see, e.g., Event Horizon Telescope
Collaboration et al. 2021b).

down-selecting the potential model space. The more heterogeneous non-EHT constraints prefer a rather different set of
models. However, even with all these constraints, 11/200
models pass for all simulations; all of these are MADs, with all
but one having Rhigh = 160. On the other hand, they cover a
wider range of spin compared to EHT-only constraints, with a
slight preference for a*  0 and higher inclinations, and
including retrograde and edge-on models.
None of the 200 ﬁducial models pass all 11 constraints in
combination, the most strict of which are the 86 GHz size, the
ring diameter, and the light-curve variability on 3 hr timescales.
Of these, the light-curve variability turns out to be the most
stringent constraint, passing only 4% of ﬁducial models. SANE
models, which are less variable than MADs, are preferred,
while all the other EHT/non-EHT constraints generally favor
MADs. If we consider the set of models that pass 10/11
constraints, it is notable that for both MADs and SANEs there
is still a marked preference for models with prograde spin, a
lower inclination, and Rhigh > 40, with several clustered at the
maximum of Rhigh = 160.
The “exploratory” models cover less of a range in parameter
space but still indicate important trends. In particular, including
nonthermal electrons (which are especially important for
modeling ﬂares) tends to push the limits of allowed NIR ﬂux
and, to some extent, also the X-ray ﬂux. Because the
nonthermal particles also enhance the 230 GHz ﬂux density,
rescaling to a ﬁxed ﬂux density results in a smaller accretion
rate. The smaller resulting opacity then affects the image
properties, such as producing a somewhat narrower ring
morphology at 230 GHz and a larger image at 86 GHz.
Nevertheless, the addition of nonthermal models does not
drastically change the preferred parameter space, and passing
models also favor prograde spin and lower inclination.
Increased tilt of the accretion ﬂow tends to increase variability
and the NIR ﬂux and thus leads to model failures. Similarly,
neither of the two wind-fed models passed, but this is not
surprising, as they only model a single spin (a* = 0) and two
instances of the thermal Rhigh eDF. With such sparse sampling
of parameter space, these classes of models require a more
focused study to draw conclusions.
Overall, very few of our models are as quiet as the data.
Although this was not investigated in M87* Paper V,
subsequent work suggests a similar result for M87* simulations

7. Implications for Black Holes and General Relativity
As demonstrated using the suite of GRMHD simulations
discussed in Section 6, the EHT images of Sgr A* are
consistent with the expected appearance of a Kerr black hole.
Moreover, our images are consistent with an angular gravitational radius θg that matches the expectations from nearly
Keplerian orbits of stars on scales of (103–105)RS.
To quantify this consistency, we compute θg using EHT
measurements alone (for details, see Paper IV). Following the
procedure developed in M87* Paper VI, we estimate θg by
9

## PDF page 10

The Astrophysical Journal Letters, 930:L12 (21pp), 2022 May 10

Event Horizon Telescope Collaboration et al.

calibrating the observed emission ring diameter d to the known
angular gravitational scale θg for a suite of synthetic data sets
produced from the GRMHD library presented in Paper V.
Speciﬁcally, we generate 100 data sets from GRMHD
simulations with varying intrinsic θg and that span the explored
range in accretion states, black hole spins, viewing inclinations,
position angles, and phenomenological electron heating parameters Rhigh. Each synthetic data set matches the baseline
coverage and sensitivity of the EHT observations. We then
estimate the ring diameter using multiple geometric modeling
and imaging methods, deriving a separate calibration factor
α ≡ d/θg for each method and for every data set to attain a
method-dependent scaling relationship and associated
uncertainty.
*
+1.4
With this approach, we estimate qg = 4.80.7 m as for Sgr A ,
where the uncertainties correspond to a 68% credible interval.
This estimate is consistent with, but much less constraining than,
measurements of θg using resolved stellar orbits (see Table 1).
This procedure assumes the validity of the Kerr metric and relies
on our suite of GRMHD simulations to provide a reasonable
proxy for the space of viable emission models. The fractional
uncertainty in our estimate of θg for Sgr A* is broader than our
estimate for M87* (θg = 3.8 ± 0.4 μas), primarily because of the
increased calibration uncertainty associated with the unknown
inclination of Sgr A* and because of the increased diameter
measurement uncertainty associated with intrinsic variability
of Sgr A*.
We also used EHT images to constrain potential deviations
from the Kerr metric and to test the nature of the compact
object in Sgr A* (for details, see Paper VI). For instance, the
brightness depression has a contrast fc  0.3, which provides
support for the existence of an event horizon in Sgr A*. If the
compact object instead had an absorptive boundary that
radiated the thermalized energy of infalling material 
Mc 2 , it
could still produce a depression in the EHT images but would
generate IR emission that greatly exceeds the measured
spectrum of Sgr A* (Broderick & Narayan 2006; Narayan &
McClintock 2008). Alternatively, a partially reﬂecting surface
would reduce the depth of the depression; the EHT images
directly constrain the albedo of such a reﬂecting surface to be
0.3. The brightness depression also rules out several speciﬁc
black hole alternatives, including some models of naked
singularities (e.g., Joshi et al. 2014) and some models of boson
stars (e.g., Olivares et al. 2020), although other horizonless
black hole mimickers produce apparent shadows that are
consistent with the observed depression (e.g., Shaikh et al.
2019).
The measured ring diameter also provides constraints on the
spacetime metric. To obtain these constraints, we generate a
series of synthetic images to relate a measured emission ring
diameter to that of the underlying black hole shadow. These
images included a broad range of GRMHD simulations from
Paper V, as well as images for which the GRMHD and
underlying metric assumptions are relaxed. Speciﬁcally, we
generated sets of images of analytic models for accretion onto
(1) a Kerr black hole, (2) a black hole with parametric
deviations from Kerr given by the Johannsen−Psaltis metric
(Johannsen & Psaltis 2011), and (3) a non-Kerr black hole
deﬁned by the Kerr−Sen metric (García et al. 1995). For each
analytic model, we allow the emission prescriptions to vary
within physically plausible limits (for details, see Özel et al.
2021; Younsi et al. 2021). We ﬁnd a similar relationship

Figure 6. Comparison of posterior distributions for the Schwarzschild
fractional shadow deviation parameter δ measured by the EHT for Sgr A*
and M87*. For Sgr A*, δ is computed relative to the expected shadow size from
monitoring stellar orbits; for M87*, δ is computed for the expected shadow both
from stellar dynamics and from gas dynamics (for details, see M87* Paper VI).
The gray band shows the expected range of δ for the Kerr metric. For the
stellar-dynamical prior mass estimates, the EHT measurements show close
consistency with the same black hole metric over three orders of magnitude in
black hole mass.

between the diameter of the emission ring and that of the black
hole shadow in all these cases, indicating that this relationship
is insensitive to the details of the underlying spacetime.
Selecting a subset of these models, we then generate 145
synthetic data sets. We apply imaging and modeling methods
to compute the ring diameter for each data set to evaluate
method-dependent measurement uncertainties and biases. We
then use this calibration together with the EHT measurements
of the ring diameter to determine the angular diameter of the
black hole shadow for Sgr A*: dsh = 48.7 ± 7.0 μas. This result
is tighter than the range for θg derived above because of
differences in the calibration data sets and procedures used in
Paper IV and Paper VI. Speciﬁcally, Paper IV uses a calibration
suite that consists entirely of dynamic GRMHD models, and it
derives a scale factor between θg and the angular diameter of
the emission ring. In contrast, Paper VI uses a calibration suite
containing both static Kerr and non-Kerr images and dynamic
GRMHD models, and it derives a scale factor between dsh and
the angular diameter of the emission ring. Paper VI also
excludes data sets for which the range of reconstructed
diameters is more than 2–3 times the range that is measured
using the Sgr A* data. Thus, comparison of these results
provides a measure of the impact of our assumptions and
procedures on the inference of the black hole properties.
By comparing this shadow diameter with stellar-dynamical
measurements of the mass of Sgr A*, we also determine a
deviation parameter δ, which quantiﬁes the fractional difference
between the inferred shadow diameter and its expected value
for a nonspinning (Schwarzschild) black hole (for details, see
+0.09
Paper VI). We ﬁnd d = -0.080.09 when using VLTI
+0.09
measurements of θg and d = -0.040.10 when using Keck
measurements of θg (see Table 1). For comparison, a spinning
(Kerr) black hole has −0.08  δ  0.
Under the assumption that this range of calibration factors
applies generically to all non-Kerr spacetimes that have black
hole shadows, we can translate measurements of δ into
constraints on parameters of these spacetimes (Psaltis et al.
2020). In particular, our measurements exclude speciﬁc non10

## PDF page 11

The Astrophysical Journal Letters, 930:L12 (21pp), 2022 May 10

Event Horizon Telescope Collaboration et al.

*

ﬁeld conﬁguration of this source through polarimetric observations, as was done for M87*, and describe the structural
changes associated with ﬂare activity on April 11. Since 2017,
the EHT has continued to gather data using an increasing
number of array elements and doubled recording bandwidth.
These data will provide improved sensitivity and enable more
robust imaging of this dynamic source, eventually allowing
movie reconstructions of plasma motions on the ∼hour orbital
timescales.

Kerr solutions for Sgr A , such as the traversible Morris
−Thorne wormhole and the naked singularities in the Reissner
−Nordström metric, which predict shadows that are signiﬁcantly smaller than those of Kerr black holes.
Relative to M87*, the primary strengths of testing GR with
EHT observations of Sgr A* are the tight prior constraints on its
mass-to-distance ratio θg and its shorter gravitational timescale
that allows EHT observations to span many dynamical times.
Together, these results show SMBHs consistent with predictions of the Kerr metric over a spread of three orders of
magnitude in their mass (see Figure 6). The image of Sgr A*
probes a similar gravitational potential to M87* but spacetime
curvature ξ ∝ M−2 that is six orders of magnitude larger. When
combined with constraints from the measurement of gravitational waves from coalescing black hole binaries with LIGO/
Virgo, these results show a striking validation of the
predictions of GR over a vast range of scales, from stellarmass black holes to SMBHs that are billions of times larger.

We thank the anonymous referees for helpful comments that
improved the paper.
The Event Horizon Telescope Collaboration thanks the
following organizations and programs: the Academia Sinica;
the Academy of Finland (projects 274477, 284495, 312496,
315721); the Agencia Nacional de Investigación y Desarrollo
(ANID), Chile via NCN19_058 (TITANs) and Fondecyt
1221421, the Alexander von Humboldt Stiftung; an Alfred P.
Sloan Research Fellowship; Allegro, the European ALMA
Regional Centre node in the Netherlands, the NL astronomy
research network NOVA and the astronomy institutes of the
University of Amsterdam, Leiden University and Radboud
University; the ALMA North America Development Fund; the
Black Hole Initiative, which is funded by grants from the John
Templeton Foundation and the Gordon and Betty Moore
Foundation (although the opinions expressed in this work are
those of the author(s) and do not necessarily reﬂect the views of
these Foundations); Chandra DD7-18089X and TM6-17006X;
the China Scholarship Council; China Postdoctoral Science
Foundation fellowship (2020M671266); Consejo Nacional de
Ciencia y Tecnología (CONACYT, Mexico, projects U0004246083, U0004-259839, F0003-272050, M0037-279006,
F0003-281692, 104497, 275201, 263356); the Consejería de
Economía, Conocimiento, Empresas y Universidad of the Junta
de Andalucía (grant P18-FR-1769), the Consejo Superior de
Investigaciones Cientíﬁcas (grant 2019AEP112); the Delaney
Family via the Delaney Family John A. Wheeler Chair at
Perimeter Institute; Dirección General de Asuntos del Personal
Académico-Universidad Nacional Autónoma de México
(DGAPA-UNAM, projects IN112417 and IN112820); the
Dutch Organization for Scientiﬁc Research (NWO) VICI
award (grant 639.043.513) and grant OCENW.KLEIN.113;
the Dutch National Supercomputers, Cartesius and Snellius
(NWO Grant 2021.013); the EACOA Fellowship awarded by
the East Asia Core Observatories Association, which consists
of the Academia Sinica Institute of Astronomy and Astrophysics, the National Astronomical Observatory of Japan,
Center for Astronomical Mega-Science, Chinese Academy of
Sciences, and the Korea Astronomy and Space Science
Institute; the European Research Council (ERC) Synergy
Grant “BlackHoleCam: Imaging the Event Horizon of Black
Holes” (grant 610058); the European Union Horizon 2020
research and innovation programme under grant agreements
RadioNet (No 730562) and M2FINDERS (No 101018682); the
Generalitat Valenciana postdoctoral grant APOSTD/2018/177
and GenT Program (project CIDEGENT/2018/021); MICINN
Research Project PID2019-108995GB-C22; the European
Research Council for advanced grant “JETSET: Launching,
propagation and emission of relativistic jets from binary
mergers and across mass scales” (Grant No. 884631); the
Institute for Advanced Study; the Istituto Nazionale di Fisica
Nucleare (INFN) sezione di Napoli, iniziative speciﬁche

8. Conclusion and Outlook
Here we present the results of 2017 EHT observations of
Sgr A*, the central SMBH in the Milky Way. We ﬁnd evidence
for intraday structural variability in Sgr A*, conﬁrming changes
that were hinted at in prior observations across the electromagnetic spectrum. These variations challenge standard
approaches to interferometric analysis, so we have developed
a variety of methods to infer the structure of this source from
our data. From observations on April 7, on which we have the
best-sampled data, our analyses consistently reveal a ring-like
structure, similar to that seen in M87*. Less complete
observations on April 6 support this picture.
This ring of emission and its central brightness depression
closely mirror the structure expected from the plasma in
accretion and outﬂow structures bordering the event horizon of
a black hole and partially lensed by its gravity. The angular
diameter of this ring is consistent with that expected from the
black hole mass inferred from stellar orbits. This consistency
allows us to restrict the allowed values of parameters that
describe deviations from a Kerr black hole, as predicted by GR.
We compare our data, including measurements at other
wavelengths, with a large suite of GRMHD simulations. These
simulations are remarkably successful at predicting the 1.3 mm
image structure and broadband spectrum of Sgr A*. However,
the GRMHD simulations tend to be more variable than the
observations, which may be related to our ﬂuid modeling of a
collisionless plasma or our neglect of radiative cooling, and
only a few conﬁgurations can satisfy our full set of
observational constraints apart from variability. Our results
generally favor models with dynamically strong magnetic
ﬁelds, moderate (prograde) spin, a lower inclination viewing
angle, and strongly decoupled protons and electrons in the
emission region. Interestingly, these models also predict a
reasonably efﬁcient (compared to the accretion rate) jet
outﬂow, which points to interesting complementary future
studies. However, more work is needed to fully explore the
physical parameter space and to understand the variability.
As the nearest SMBH, Sgr A* can be scrutinized in ways that
are impossible for other sources, making it a unique laboratory
for exploring the astrophysics of black holes and testing the
predictions of GR. The results presented in these papers are the
ﬁrst EHT contributions to the study of this source, but they are
not the last. Subsequent work will characterize the magnetic
11

## PDF page 12

The Astrophysical Journal Letters, 930:L12 (21pp), 2022 May 10

Event Horizon Telescope Collaboration et al.

Fellowship Grant: grants NRF-2015H1A2A1033752, the Korea
Research Fellowship Program: NRF-2015H1D3A1066561, Brain
Pool Program: 2019H1D3A1A01102564, Basic Research Support Grant 2019R1F1A1059721, 2021R1A6A3A01086420,
2022R1C1C1005255); Netherlands Research School for Astronomy (NOVA) Virtual Institute of Accretion (VIA) postdoctoral
fellowships; Onsala Space Observatory (OSO) national infrastructure, for the provisioning of its facilities/observational
support (OSO receives funding through the Swedish Research
Council under grant 2017-00648); the Perimeter Institute for
Theoretical Physics (research at Perimeter Institute is supported by
the Government of Canada through the Department of Innovation,
Science and Economic Development and by the Province of
Ontario through the Ministry of Research, Innovation and
Science); the Spanish Ministerio de Ciencia e Innovación (grants
PGC2018-098915-B-C21,
AYA2016-80889-P,
PID2019108995GB-C21, PID2020-117404GB-C21); the University of
Pretoria for ﬁnancial aid in the provision of the new Cluster Server
nodes and SuperMicro (USA) for a SEEDING GRANT approved
towards these nodes in 2020; the Shanghai Pilot Program for
Basic Research, Chinese Academy of Science, Shanghai Branch
(JCYJ-SHFY-2021-013); the State Agency for Research of the
Spanish MCIU through the “Center of Excellence Severo Ochoa”
award for the Instituto de Astrofísica de Andalucía (SEV-20170709); the Spinoza Prize SPI 78-409; the South African Research
Chairs Initiative, through the South African Radio Astronomy
Observatory (SARAO, grant ID 77948), which is a facility of the
National Research Foundation (NRF), an agency of the
Department of Science and Innovation (DSI) of South Africa;
the Toray Science Foundation; Swedish Research Council (VR);
the US Department of Energy (USDOE) through the Los Alamos
National Laboratory (operated by Triad National Security, LLC,
for the National Nuclear Security Administration of the USDOE
(Contract 89233218CNA000001); and the YCAA Prize Postdoctoral Fellowship.
We thank the staff at the participating observatories,
correlation centers, and institutions for their enthusiastic support.
This paper makes use of the following ALMA data: ADS/JAO.
ALMA#2016.1.01154.V. ALMA is a partnership of the
European Southern Observatory (ESO; Europe, representing its
member states), NSF, and National Institutes of Natural Sciences
of Japan, together with National Research Council (Canada),
Ministry of Science and Technology (MOST; Taiwan),
Academia Sinica Institute of Astronomy and Astrophysics
(ASIAA; Taiwan), and Korea Astronomy and Space Science
Institute (KASI; Republic of Korea), in cooperation with the
Republic of Chile. The Joint ALMA Observatory is operated by
ESO, Associated Universities, Inc. (AUI)/NRAO, and the
National Astronomical Observatory of Japan (NAOJ). The
NRAO is a facility of the NSF operated under cooperative
agreement by AUI. This research used resources of the Oak
Ridge Leadership Computing Facility at the Oak Ridge National
Laboratory, which is supported by the Ofﬁce of Science of the
U.S. Department of Energy under Contract No. DE-AC0500OR22725. We also thank the Center for Computational
Astrophysics, National Astronomical Observatory of Japan. The
computing cluster of Shanghai VLBI correlator supported by the
Special Fund for Astronomy from the Ministry of Finance in
China is acknowledged.
APEX is a collaboration between the Max-Planck-Institut für
Radioastronomie (Germany), ESO, and the Onsala Space
Observatory (Sweden). The SMA is a joint project between the

TEONGRAV; the International Max Planck Research School
for Astronomy and Astrophysics at the Universities of Bonn
and Cologne; DFG research grant “Jet physics on horizon
scales and beyond” (Grant No. FR 4069/2-1); Joint Princeton/
Flatiron and Joint Columbia/Flatiron Postdoctoral Fellowships,
research at the Flatiron Institute is supported by the Simons
Foundation; the Japan Ministry of Education, Culture, Sports,
Science and Technology (MEXT; grant JPMXP1020200109);
the Japanese Government (Monbukagakusho: MEXT) Scholarship; the Japan Society for the Promotion of Science (JSPS)
Grant-in-Aid for JSPS Research Fellowship (JP17J08829); the
Joint Institute for Computational Fundamental Science, Japan;
the Key Research Program of Frontier Sciences, Chinese
Academy of Sciences (CAS, grants QYZDJ-SSW-SLH057,
QYZDJSSW-SYS008, ZDBS-LY-SLH011); the Leverhulme
Trust Early Career Research Fellowship; the Max-PlanckGesellschaft (MPG); the Max Planck Partner Group of the
MPG and the CAS; the MEXT/JSPS KAKENHI (grants
18KK0090, JP21H01137, JP18H03721, JP18K13594,
18K03709, JP19K14761, 18H01245, 25120007); the Malaysian Fundamental Research Grant Scheme (FRGS) FRGS/1/
2019/STG02/UM/02/6; the MIT International Science and
Technology Initiatives (MISTI) Funds; the Ministry of Science
and Technology (MOST) of Taiwan (103-2119-M-001-010MY2, 105-2112-M-001-025-MY3, 105-2119-M-001-042, 1062112-M-001-011, 106-2119-M-001-013, 106-2119-M-001027, 106-2923-M-001-005, 107-2119-M-001-017, 107-2119M-001-020, 107-2119-M-001-041, 107-2119-M-110-005, 1072923-M-001-009, 108-2112-M-001-048, 108-2112-M-001051, 108-2923-M-001-002, 109-2112-M-001-025, 109-2124M-001-005, 109-2923-M-001-001, 110-2112-M-003-007MY2, 110-2112-M-001-033, 110-2124-M-001-007, and 1102923-M-001-001); the Ministry of Education (MoE) of Taiwan
Yushan Young Scholar Program; the Physics Division,
National Center for Theoretical Sciences of Taiwan; the
National Aeronautics and Space Administration (NASA, Fermi
Guest Investigator grant 80NSSC20K1567, NASA Astrophysics Theory Program grant 80NSSC20K0527, NASA NuSTAR
award 80NSSC20K0645); NASA Hubble Fellowship grant
HST-HF2-51431.001-A awarded by the Space Telescope
Science Institute, which is operated by the Association of
Universities for Research in Astronomy, Inc., for NASA, under
contract NAS5-26555; the National Institute of Natural
Sciences (NINS) of Japan; the National Key Research and
Development Program of China (grant 2016YFA0400704,
2017YFA0402703, 2016YFA0400702); the National Science
Foundation (NSF, grants AST-0096454, AST-0352953, AST0521233, AST-0705062, AST-0905844, AST-0922984, AST1126433, AST-1140030, DGE-1144085, AST-1207704, AST1207730, AST-1207752, MRI-1228509, OPP-1248097, AST1310896, AST-1440254, AST-1555365, AST-1614868, AST1615796, AST-1715061, AST-1716327, AST-1716536, OISE1743747, AST-1816420, AST-1935980, AST-2034306); NSF
Astronomy and Astrophysics Postdoctoral Fellowship (AST1903847); the Natural Science Foundation of China (grants
11650110427, 10625314, 11721303, 11725312, 11873028,
11933007, 11991052, 11991053, 12192220, 12192223); the
Natural Sciences and Engineering Research Council of Canada
(NSERC, including a Discovery Grant and the NSERC Alexander
Graham Bell Canada Graduate Scholarships-Doctoral Program);
the National Youth Thousand Talents Program of China; the
National Research Foundation of Korea (the Global PhD
12

## PDF page 13

The Astrophysical Journal Letters, 930:L12 (21pp), 2022 May 10

Event Horizon Telescope Collaboration et al.

the observational campaigns of 2017 and 2018. We would like
to thank A. Deller and W. Brisken for EHT-speciﬁc support
with the use of DiFX. We thank Martin Shepherd for the
addition of extra features in the Difmap software that were used
for the CLEAN imaging results presented in this paper. We
acknowledge the signiﬁcance that Maunakea, where the SMA
and JCMT EHT stations are located, has for the indigenous
Hawaiian people. IMV acknowledges the use of LLuis Vives
HPC resources of the University of Valencia.
Facilities: EHT, ALMA, APEX, IRAM:30 m, JCMT,
LMT, SMA, ARO:SMT, SPT, Chandra, EAVN, GMVA,
NuSTAR, Swift, VLT.

SAO and ASIAA and is funded by the Smithsonian Institution
and the Academia Sinica. The JCMT is operated by the East
Asian Observatory on behalf of the NAOJ, ASIAA, and KASI,
as well as the Ministry of Finance of China, Chinese Academy
of Sciences, and the National Key Research and Development
Program (No. 2017YFA0402700) of China and Natural
Science Foundation of China grant 11873028. Additional
funding support for the JCMT is provided by the Science and
Technologies Facility Council (UK) and participating universities in the UK and Canada. The LMT is a project operated
by the Instituto Nacional de Astróﬁsica, Óptica, y Electrónica
(Mexico) and the University of Massachusetts at Amherst
(USA). The IRAM 30-m telescope on Pico Veleta, Spain is
operated by IRAM and supported by CNRS (Centre National
de la Recherche Scientiﬁque, France), MPG (Max-PlanckGesellschaft, Germany) and IGN (Instituto Geográﬁco Nacional,
Spain). The SMT is operated by the Arizona Radio Observatory,
a part of the Steward Observatory of the University of Arizona,
with ﬁnancial support of operations from the State of Arizona
and ﬁnancial support for instrumentation development from the
NSF. Support for SPT participation in the EHT is provided by
the National Science Foundation through award OPP-1852617
to the University of Chicago. Partial support is also provided by
the Kavli Institute of Cosmological Physics at the University of
Chicago. The SPT hydrogen maser was provided on loan from
the GLT, courtesy of ASIAA.
This work used the Extreme Science and Engineering
Discovery Environment (XSEDE), supported by NSF grant
ACI-1548562, and CyVerse, supported by NSF grants DBI0735191, DBI-1265383, and DBI-1743442. XSEDE Stampede2
resource at TACC was allocated through TG-AST170024 and
TG-AST080026N. XSEDE JetStream resource at PTI and
TACC was allocated through AST170028. This research is part
of the Frontera computing project at the Texas Advanced
Computing Center through the Frontera Large-Scale Community
Partnerships allocation AST20023. Frontera is made possible by
National Science Foundation award OAC-1818253. This
research was carried out using resources provided by the Open
Science Grid, which is supported by the National Science
Foundation and the U.S. Department of Energy Ofﬁce of
Science. Additional work used ABACUS2.0, which is part of
the eScience center at Southern Denmark University. Simulations were also performed on the SuperMUC cluster at the LRZ
in Garching, on the LOEWE cluster in CSC in Frankfurt, on the
HazelHen cluster at the HLRS in Stuttgart, and on the Pi2.0 and
Siyuan Mark-I at Shanghai Jiao Tong University. The computer
resources of the Finnish IT Center for Science (CSC) and the
Finnish Computing Competence Infrastructure (FCCI) project
are acknowledged. This research was enabled in part by support
provided by Compute Ontario (http://computeontario.ca),
Calcul Quebec (http://www.calculquebec.ca) and Compute
Canada (http://www.computecanada.ca).
The EHTC has received generous donations of FPGA chips
from Xilinx Inc., under the Xilinx University Program. The
EHTC has beneﬁted from technology shared under opensource license by the Collaboration for Astronomy Signal
Processing and Electronics Research (CASPER). The EHT
project is grateful to T4Science and Microsemi for their
assistance with Hydrogen Masers. This research has made use
of NASAʼs Astrophysics Data System. We gratefully acknowledge the support provided by the extended staff of the ALMA,
both from the inception of the ALMA Phasing Project through

ORCID iDs
Kazunori Akiyama https://orcid.org/0000-0002-9475-4254
Antxon Alberdi https://orcid.org/0000-0002-9371-1033
Juan Carlos Algaba https://orcid.org/0000-0001-6993-1696
Richard Anantua https://orcid.org/0000-0003-3457-7660
Keiichi Asada https://orcid.org/0000-0001-6988-8763
Rebecca Azulay https://orcid.org/0000-0002-2200-5393
Uwe Bach https://orcid.org/0000-0002-7722-8412
Anne-Kathrin Baczko https://orcid.org/0000-00033090-3975
Mislav Baloković https://orcid.org/0000-0003-0476-6647
John Barrett https://orcid.org/0000-0002-9290-0764
Michi Bauböck https://orcid.org/0000-0002-5518-2812
Bradford A. Benson https://orcid.org/0000-00025108-6823
Lindy Blackburn https://orcid.org/0000-0002-9030-642X
Raymond Blundell https://orcid.org/0000-0002-5929-5857
Katherine L. Bouman https://orcid.org/0000-00030077-4367
Geoffrey C. Bower https://orcid.org/0000-0003-4056-9982
Hope Boyce https://orcid.org/0000-0002-6530-5783
Christiaan D. Brinkerink https://orcid.org/0000-00022322-0749
Roger Brissenden https://orcid.org/0000-0002-2556-0894
Silke Britzen https://orcid.org/0000-0001-9240-6734
Avery E. Broderick https://orcid.org/0000-00023351-760X
Dominique Broguiere https://orcid.org/0000-00019151-6683
Thomas Bronzwaer https://orcid.org/0000-0003-1151-3971
Sandra Bustamante https://orcid.org/0000-0001-6169-1894
Do-Young Byun https://orcid.org/0000-0003-1157-4109
John E. Carlstrom https://orcid.org/0000-0002-2044-7665
Chiara Ceccobello https://orcid.org/0000-0002-4767-9925
Andrew Chael https://orcid.org/0000-0003-2966-6220
Chi-kwan Chan https://orcid.org/0000-0001-6337-6126
Koushik Chatterjee https://orcid.org/0000-0002-2825-3590
Shami Chatterjee https://orcid.org/0000-0002-2878-1502
Ming-Tang Chen https://orcid.org/0000-0001-6573-3318
Yongjun Chen (陈永军) https://orcid.org/0000-0001-56506770
Xiaopeng Cheng https://orcid.org/0000-0003-4407-9868
Ilje Cho https://orcid.org/0000-0001-6083-7521
Pierre Christian https://orcid.org/0000-0001-6820-9941
Nicholas S. Conroy https://orcid.org/0000-0003-2886-2377
John E. Conway https://orcid.org/0000-0003-2448-9181
James M. Cordes https://orcid.org/0000-0002-4049-1882
Thomas M. Crawford https://orcid.org/0000-00019000-5013
13

## PDF page 14

The Astrophysical Journal Letters, 930:L12 (21pp), 2022 May 10

Event Horizon Telescope Collaboration et al.

Geoffrey B. Crew https://orcid.org/0000-0002-2079-3189
Alejandro Cruz-Osorio https://orcid.org/0000-00023945-6342
Yuzhu Cui (崔玉竹) https://orcid.org/0000-0001-63114345
Jordy Davelaar https://orcid.org/0000-0002-2685-2434
Mariafelicia De Laurentis https://orcid.org/0000-00029945-682X
Roger Deane https://orcid.org/0000-0003-1027-5043
Jessica Dempsey https://orcid.org/0000-0003-1269-9667
Gregory Desvignes https://orcid.org/0000-0003-3922-4055
Jason Dexter https://orcid.org/0000-0003-3903-0373
Vedant Dhruv https://orcid.org/0000-0001-6765-877X
Sheperd S. Doeleman https://orcid.org/0000-00029031-0904
Sean Dougal https://orcid.org/0000-0002-3769-1314
Sergio A. Dzib https://orcid.org/0000-0001-6010-6200
Ralph P. Eatough https://orcid.org/0000-0001-6196-4135
Razieh Emami https://orcid.org/0000-0002-2791-5011
Heino Falcke https://orcid.org/0000-0002-2526-6724
Joseph Farah https://orcid.org/0000-0003-4914-5625
Vincent L. Fish https://orcid.org/0000-0002-7128-9345
Ed Fomalont https://orcid.org/0000-0002-9036-2747
H. Alyson Ford https://orcid.org/0000-0002-9797-0972
Raquel Fraga-Encinas https://orcid.org/0000-00025222-1361
Per Friberg https://orcid.org/0000-0002-8010-8454
Christian M. Fromm https://orcid.org/0000-00021827-1656
Antonio Fuentes https://orcid.org/0000-0002-8773-4933
Peter Galison https://orcid.org/0000-0002-6429-3872
Charles F. Gammie https://orcid.org/0000-0001-7451-8935
Roberto García https://orcid.org/0000-0002-6584-7443
Olivier Gentaz https://orcid.org/0000-0002-0115-4605
Boris Georgiev https://orcid.org/0000-0002-3586-6424
Ciriaco Goddi https://orcid.org/0000-0002-2542-7743
Roman Gold https://orcid.org/0000-0003-2492-1966
Arturo I. Gómez-Ruiz https://orcid.org/0000-00019395-1670
José L. Gómez https://orcid.org/0000-0003-4190-7613
Minfeng Gu (顾敏峰) https://orcid.org/0000-000244556946
Mark Gurwell https://orcid.org/0000-0003-0685-3621
Kazuhiro Hada https://orcid.org/0000-0001-6906-772X
Daryl Haggard https://orcid.org/0000-0001-6803-2138
Michael H. Hecht https://orcid.org/0000-0002-4114-4583
Ronald Hesper https://orcid.org/0000-0003-1918-6098
Dirk Heumann https://orcid.org/0000-0002-7671-0047
Luis C. Ho
(何子山) https://orcid.org/0000-0001-6947-5846
Paul Ho https://orcid.org/0000-0002-3412-4306
Mareki Honma https://orcid.org/0000-0003-4058-9000
Chih-Wei L. Huang https://orcid.org/0000-0001-5641-3953
Lei Huang (黄磊) https://orcid.org/0000-0002-1923-227X
Shiro Ikeda https://orcid.org/0000-0002-2462-1448
C. M. Violette Impellizzeri https://orcid.org/0000-00023443-2472
Makoto Inoue https://orcid.org/0000-0001-5037-3989
Sara Issaoun https://orcid.org/0000-0002-5297-921X
David J. James https://orcid.org/0000-0001-5160-4486

Buell T. Jannuzi https://orcid.org/0000-0002-1578-6582
Michael Janssen https://orcid.org/0000-0001-8685-6544
Britton Jeter https://orcid.org/0000-0003-2847-1712
Wu Jiang (江悟) https://orcid.org/0000-0001-7369-3539
Alejandra Jiménez-Rosales https://orcid.org/0000-00022662-3754
Michael D. Johnson https://orcid.org/0000-0002-4120-3029
Svetlana Jorstad https://orcid.org/0000-0001-6158-1708
Abhishek V. Joshi https://orcid.org/0000-0002-2514-5965
Taehyun Jung https://orcid.org/0000-0001-7003-8643
Mansour Karami https://orcid.org/0000-0001-7387-9333
Ramesh Karuppusamy https://orcid.org/0000-00025307-2919
Tomohisa Kawashima https://orcid.org/0000-00018527-0496
Garrett K. Keating https://orcid.org/0000-0002-3490-146X
Mark Kettenis https://orcid.org/0000-0002-6156-5617
Dong-Jin Kim https://orcid.org/0000-0002-7038-2118
Jae-Young Kim https://orcid.org/0000-0001-8229-7183
Jongsoo Kim https://orcid.org/0000-0002-1229-0426
Junhan Kim https://orcid.org/0000-0002-4274-9373
Motoki Kino https://orcid.org/0000-0002-2709-7338
Jun Yi Koay https://orcid.org/0000-0002-7029-6658
Prashant Kocherlakota https://orcid.org/0000-00017386-7439
Patrick M. Koch https://orcid.org/0000-0003-2777-5861
Shoko Koyama https://orcid.org/0000-0002-3723-3372
Carsten Kramer https://orcid.org/0000-0002-4908-4925
Michael Kramer https://orcid.org/0000-0002-4175-2271
Thomas P. Krichbaum https://orcid.org/0000-00024892-9586
Cheng-Yu Kuo https://orcid.org/0000-0001-6211-5581
Noemi La Bella https://orcid.org/0000-0002-8116-9427
Tod R. Lauer https://orcid.org/0000-0003-3234-7247
Daeyoung Lee https://orcid.org/0000-0002-3350-5588
Sang-Sung Lee https://orcid.org/0000-0002-6269-594X
Po Kin Leung https://orcid.org/0000-0002-8802-8256
Aviad Levis https://orcid.org/0000-0001-7307-632X
Zhiyuan Li (李志远) https://orcid.org/0000-0003-03556437
Rocco Lico https://orcid.org/0000-0001-7361-2460
Greg Lindahl https://orcid.org/0000-0002-6100-4772
Michael Lindqvist https://orcid.org/0000-0002-3669-0715
Mikhail Lisakov https://orcid.org/0000-0001-6088-3819
Jun Liu (刘俊) https://orcid.org/0000-0002-7615-7499
Kuo Liu https://orcid.org/0000-0002-2953-7376
Elisabetta Liuzzo https://orcid.org/0000-0003-0995-5201
Wen-Ping Lo https://orcid.org/0000-0003-1869-2503
Andrei P. Lobanov https://orcid.org/0000-0003-1622-1484
Laurent Loinard https://orcid.org/0000-0002-5635-3345
Colin J. Lonsdale https://orcid.org/0000-0003-4062-4654
Ru-Sen Lu (路如森) https://orcid.org/0000-0002-76927967
Jirong Mao (毛基荣) https://orcid.org/0000-0002-70777195
Nicola Marchili https://orcid.org/0000-0002-5523-7588
Sera Markoff https://orcid.org/0000-0001-9564-0876
Daniel P. Marrone https://orcid.org/0000-0002-2367-1080
Alan P. Marscher https://orcid.org/0000-0001-7396-3332
Iván Martí-Vidal https://orcid.org/0000-0003-3708-9611
Satoki Matsushita https://orcid.org/0000-0002-2127-7880

14

## PDF page 15

The Astrophysical Journal Letters, 930:L12 (21pp), 2022 May 10

Event Horizon Telescope Collaboration et al.

Lynn D. Matthews https://orcid.org/0000-0002-3728-8082
Lia Medeiros https://orcid.org/0000-0003-2342-6728
Karl M. Menten https://orcid.org/0000-0001-6459-0669
Daniel Michalik https://orcid.org/0000-0002-7618-6556
Izumi Mizuno https://orcid.org/0000-0002-7210-6264
Yosuke Mizuno https://orcid.org/0000-0002-8131-6730
James M. Moran https://orcid.org/0000-0002-3882-4414
Kotaro Moriyama https://orcid.org/0000-0003-1364-3761
Monika Moscibrodzka https://orcid.org/0000-00024661-6332
Cornelia Müller https://orcid.org/0000-0002-2739-2994
Alejandro Mus https://orcid.org/0000-0003-0329-6874
Gibwa Musoke https://orcid.org/0000-0003-1984-189X
Ioannis Myserlis https://orcid.org/0000-0003-3025-9497
Andrew Nadolski https://orcid.org/0000-0001-9479-9957
Hiroshi Nagai https://orcid.org/0000-0003-0292-3645
Neil M. Nagar https://orcid.org/0000-0001-6920-662X
Masanori Nakamura https://orcid.org/0000-00016081-2420
Ramesh Narayan https://orcid.org/0000-0002-1919-2730
Gopal Narayanan https://orcid.org/0000-0002-4723-6569
Iniyan Natarajan https://orcid.org/0000-0001-8242-4373
Joey Neilsen https://orcid.org/0000-0002-8247-786X
Roberto Neri https://orcid.org/0000-0002-7176-4046
Chunchong Ni https://orcid.org/0000-0003-1361-5699
Aristeidis Noutsos https://orcid.org/0000-0002-4151-3860
Michael A. Nowak https://orcid.org/0000-0001-6923-1315
Junghwan Oh https://orcid.org/0000-0002-4991-9638
Hiroki Okino https://orcid.org/0000-0003-3779-2016
Héctor Olivares https://orcid.org/0000-0001-6833-7580
Gisela N. Ortiz-León https://orcid.org/0000-00022863-676X
Tomoaki Oyama https://orcid.org/0000-0003-4046-2923
Feryal Özel https://orcid.org/0000-0003-4413-1523
Daniel C. M. Palumbo https://orcid.org/0000-00027179-3816
Georgios Filippos Paraschos https://orcid.org/0000-00016757-3098
Jongho Park https://orcid.org/0000-0001-6558-9053
Harriet Parsons https://orcid.org/0000-0002-6327-3423
Nimesh Patel https://orcid.org/0000-0002-6021-9421
Ue-Li Pen https://orcid.org/0000-0003-2155-9578
Dominic W. Pesce https://orcid.org/0000-0002-5278-9221
Richard Plambeck https://orcid.org/0000-0001-6765-9609
Oliver Porth https://orcid.org/0000-0002-4584-2557
Felix M. Pötzl https://orcid.org/0000-0002-6579-8311
Cora Prather https://orcid.org/0000-0002-0393-7734
Jorge A. Preciado-López https://orcid.org/0000-00024146-0113
Dimitrios Psaltis https://orcid.org/0000-0003-1035-3240
Hung-Yi Pu https://orcid.org/0000-0001-9270-8812
Venkatessh Ramakrishnan https://orcid.org/0000-00029248-086X
Ramprasad Rao https://orcid.org/0000-0002-1407-7944
Mark G. Rawlings https://orcid.org/0000-0002-6529-202X
Alexander W. Raymond https://orcid.org/0000-00025779-4767
Luciano Rezzolla https://orcid.org/0000-0002-1330-7103
Angelo Ricarte https://orcid.org/0000-0001-5287-0452
Bart Ripperda https://orcid.org/0000-0002-7301-3908
Freek Roelofs https://orcid.org/0000-0001-5461-3687
Alan Rogers https://orcid.org/0000-0003-1941-7458

Eduardo Ros https://orcid.org/0000-0001-9503-4892
Cristina Romero-Cañizales https://orcid.org/0000-00016301-9073
Arash Roshanineshat https://orcid.org/0000-00028280-9238
Alan L. Roy https://orcid.org/0000-0002-1931-0135
Ignacio Ruiz https://orcid.org/0000-0002-0965-5463
Chet Ruszczyk https://orcid.org/0000-0001-7278-9707
Kazi L. J. Rygl https://orcid.org/0000-0003-4146-9043
Salvador Sánchez https://orcid.org/0000-0002-8042-5951
David Sánchez-Argüelles https://orcid.org/0000-00027344-9920
Miguel Sánchez-Portal https://orcid.org/0000-00030981-9664
Mahito Sasada https://orcid.org/0000-0001-5946-9960
Kaushik Satapathy https://orcid.org/0000-0003-0433-3585
Tuomas Savolainen https://orcid.org/0000-0001-6214-1085
Jonathan Schonfeld https://orcid.org/0000-0002-8909-2401
Karl-Friedrich Schuster https://orcid.org/0000-00032890-9454
Lijing Shao https://orcid.org/0000-0002-1334-8853
Zhiqiang Shen (沈志强) https://orcid.org/0000-0003-35408746
Des Small https://orcid.org/0000-0003-3723-5404
Bong Won Sohn https://orcid.org/0000-0002-4148-8378
Jason SooHoo https://orcid.org/0000-0003-1938-0720
Kamal Souccar https://orcid.org/0000-0001-7915-5272
He Sun (孙赫) https://orcid.org/0000-0003-1526-6787
Fumie Tazaki https://orcid.org/0000-0003-0236-0600
Alexandra J. Tetarenko https://orcid.org/0000-00033906-4354
Paul Tiede https://orcid.org/0000-0003-3826-5648
Remo P. J. Tilanus https://orcid.org/0000-0002-6514-553X
Michael Titus https://orcid.org/0000-0001-9001-3275
Pablo Torne https://orcid.org/0000-0001-8700-6058
Efthalia Traianou https://orcid.org/0000-0002-1209-6500
Sascha Trippe https://orcid.org/0000-0003-0465-1559
Matthew Turk https://orcid.org/0000-0002-5294-0198
Ilse van Bemmel https://orcid.org/0000-0001-5473-2950
Huib Jan van Langevelde https://orcid.org/0000-00020230-5946
Daniel R. van Rossum https://orcid.org/0000-00017772-6131
Jesse Vos https://orcid.org/0000-0003-3349-7394
Jan Wagner https://orcid.org/0000-0003-1105-6109
Derek Ward-Thompson https://orcid.org/0000-00031140-2761
John Wardle https://orcid.org/0000-0002-8960-2942
Jonathan Weintroub https://orcid.org/0000-00024603-5204
Norbert Wex https://orcid.org/0000-0003-4058-2837
Robert Wharton https://orcid.org/0000-0002-7416-5209
Maciek Wielgus https://orcid.org/0000-0002-8635-4242
Kaj Wiik https://orcid.org/0000-0002-0862-3398
Gunther Witzel https://orcid.org/0000-0003-2618-797X
Michael F. Wondrak https://orcid.org/0000-00026894-1072
George N. Wong https://orcid.org/0000-0001-6952-2147
Qingwen Wu (吴庆文) https://orcid.org/0000-0003-47734987
Paul Yamaguchi https://orcid.org/0000-0002-6017-8199
Doosoo Yoon https://orcid.org/0000-0001-8694-8166
15

## PDF page 16

The Astrophysical Journal Letters, 930:L12 (21pp), 2022 May 10

Event Horizon Telescope Collaboration et al.

André Young https://orcid.org/0000-0003-0000-2682
Ken Young https://orcid.org/0000-0002-3666-4920
Ziri Younsi https://orcid.org/0000-0001-9283-1191
Feng Yuan (袁峰) https://orcid.org/0000-0003-3564-6437
Ye-Fei Yuan (袁业飞) https://orcid.org/0000-0002-73304756
J. Anton Zensus https://orcid.org/0000-0001-7470-3321
Shuo Zhang https://orcid.org/0000-0002-2967-790X
Guang-Yao Zhao https://orcid.org/0000-0002-4417-1659
Shan-Shan Zhao
(赵杉杉) https://orcid.org/0000-0002-97743606
Jennie L. Berghuis https://orcid.org/0000-0003-2287-158X
Jay Blanchard https://orcid.org/0000-0002-2756-395X
Tin Lok Chan https://orcid.org/0000-0001-9197-932X
Iain M. Coulson https://orcid.org/0000-0002-7316-4626
Nathalie Degenaar https://orcid.org/0000-0002-0092-3548
Carlos A. Durán https://orcid.org/0000-0001-7622-3890
Wendeline B. Everett https://orcid.org/0000-00025370-6651
Karl Forster https://orcid.org/0000-0001-5800-5531
Nils W. Halverson https://orcid.org/0000-0003-2606-9340
Ruben Herrero-Illana https://orcid.org/0000-00027758-8717
Akihiko Hirota https://orcid.org/0000-0002-0465-5421
Ryan E. Howie https://orcid.org/0000-0002-5451-3624
Caleb Kwon https://orcid.org/0000-0001-9006-7345
Robert Laing https://orcid.org/0000-0001-6786-3087
Erik M. Leitch https://orcid.org/0000-0001-8553-9336
Lupin C.-C. Lin https://orcid.org/0000-0003-4083-9567
John K. Maute https://orcid.org/0000-0002-5744-4249
Hugo Messias https://orcid.org/0000-0002-2985-7994
Francisco Montenegro-Montes https://orcid.org/0000-00027430-3771
Dirk Muders https://orcid.org/0000-0002-2315-2571
Juan Pablo Pérez-Beaupuits https://orcid.org/0000-00033536-2274
Michael Poirier https://orcid.org/0000-0001-6641-0959
Richard Qiu https://orcid.org/0000-0003-3462-0817
Alexandra S. Rahlin https://orcid.org/0000-00033953-1776
Sean Ressler https://orcid.org/0000-0003-0220-5723
Mark Reynolds https://orcid.org/0000-0003-1621-9392
Alejandro F. Saez-Madain https://orcid.org/0000-00020804-3414
Don Sousa https://orcid.org/0000-0002-2625-2607
Anthony A. Stark https://orcid.org/0000-0002-2718-9996
Chris White https://orcid.org/0000-0001-7448-4253
Rudy Wijnands https://orcid.org/0000-0002-3516-2152
Jan G. A. Wouterloot https://orcid.org/0000-00024694-6905
Wei Yu (于威) https://orcid.org/0000-0002-51686052

Blandford, R. D., & Begelman, M. C. 1999, MNRAS, 303, L1
Blandford, R. D., & Königl, A. 1979, ApJ, 232, 34
Bolton, C. T. 1972, Natur, 235, 271
Bower, G. C., Backer, D. C., Zhao, J.-H., Goss, M., & Falcke, H. 1999, ApJ,
521, 582
Bower, G. C., Falcke, H., Herrnstein, R. M., et al. 2004, Sci, 304, 704
Bower, G. C., Goss, W. M., Falcke, H., Backer, D. C., & Lithwick, Y. 2006,
ApJL, 648, L127
Bower, G. C., Wright, M. C. H., Falcke, H., & Backer, D. C. 2003, ApJ,
588, 331
Broderick, A. E., Fish, V. L., Doeleman, S. S., & Loeb, A. 2009, ApJ, 697, 45
Broderick, A. E., Gold, R., Georgiev, B., et al. 2022, ApJL, 930, L21
Broderick, A. E., Gold, R., Karami, M., et al. 2020, ApJ, 897, 139
Broderick, A. E., & Narayan, R. 2006, ApJL, 638, L21
Chan, C.-K., Psaltis, D., Özel, F., Narayan, R., & Saḑowski, A. 2015, ApJ,
799, 1
Chatterjee, K., Younsi, Z., Liska, M., et al. 2020, MNRAS, 499, 362
Coker, R., Melia, F., & Falcke, H. 1999, ApJ, 523, 642
Dexter, J., Agol, E., & Fragile, P. C. 2009, ApJL, 703, L142
Do, T., Hees, A., Ghez, A., et al. 2019, Sci, 365, 664
Doeleman, S. S., Shen, Z.-Q., Rogers, A. E. E., et al. 2001, AJ, 121, 2610
Doeleman, S. S., Weintroub, J., Rogers, A. E. E., et al. 2008, Natur, 455, 78
Eckart, A., Baganoff, F. K., Morris, M., et al. 2004, A&A, 427, 1
EHT MWL Science Working Group, Algaba, J. C., Anczarski, J., et al. 2021,
ApJL, 911, L11
Einstein, A. 1915, Sitzungsberichte der Königlich Preußischen Akademie der
Wissenschaften (Berlin: Deutsche Akademie der Wissenschaften zu Berlin)
Ekers, R. D., Goss, W. M., Schwarz, U. J., Downes, D., & Rogstad, D. H.
1975, A&A, 43, 159
Event Horizon Telescope Collaboration, Akiyama, K., Alberdi, A., et al.
2019a, ApJL, 875, L1 (M87* Paper I)
Event Horizon Telescope Collaboration, Akiyama, K., Alberdi, A., et al.
2019b, ApJL, 875, L2 (M87* Paper II)
Event Horizon Telescope Collaboration, Akiyama, K., Alberdi, A., et al.
2019c, ApJL, 875, L3 (M87* Paper III)
Event Horizon Telescope Collaboration, Akiyama, K., Alberdi, A., et al.
2019d, ApJL, 875, L4 (M87* Paper IV)
Event Horizon Telescope Collaboration, Akiyama, K., Alberdi, A., et al.
2019e, ApJL, 875, L5 (M87* Paper V)
Event Horizon Telescope Collaboration, Akiyama, K., Alberdi, A., et al. 2019f,
ApJL, 875, L6 (M87* Paper VI)
Event Horizon Telescope Collaboration, Akiyama, K., Alberdi, A., et al.
2021a, ApJL, 910, L12 (M87* Paper VII)
Event Horizon Telescope Collaboration, Akiyama, K., Alberdi, A., et al.
2021b, ApJL, 910, L13 (M87* Paper VIII)
Event Horizon Telescope Collaboration, Akiyama, K., Alberdi, A., et al.
2022a, ApJL, 930, L13 (Paper II)
Event Horizon Telescope Collaboration, Akiyama, K., Alberdi, A., et al.
2022b, ApJL, 930, L14 (Paper III)
Event Horizon Telescope Collaboration, Akiyama, K., Alberdi, A., et al.
2022c, ApJL, 930, L15 (Paper IV)
Event Horizon Telescope Collaboration, Akiyama, K., Alberdi, A., et al.
2022d, ApJL, 930, L16 (Paper V)
Event Horizon Telescope Collaboration, Akiyama, K., Alberdi, A., et al.
2022e, ApJL, 930, L17 (Paper VI)
Fabian, A. C. 2012, ARA&A, 50, 455
Falcke, H., Goss, W. M., Matsuo, H., et al. 1998, ApJ, 499, 731
Falcke, H., Mannheim, K., & Biermann, P. L. 1993, A&A, 278, L1
Falcke, H., Melia, F., & Agol, E. 2000, ApJL, 528, L13
Farah, J., Galison, P., Akiyama, K., et al. 2022, ApJL, 930, L18
Fish, V. L., Doeleman, S. S., Beaudoin, C., et al. 2011, ApJL, 727, L36
Gammie, C. F., McKinney, J. C., & Tóth, G. 2003, ApJ, 589, 444
García, A., Galtsov, D., & Kechkin, O. 1995, PhRvL, 74, 1276
Genzel, R., Schödel, R., Ott, T., et al. 2003, Natur, 425, 934
Georgiev, B., Pesce, D. W., Broderick, A. E., et al. 2022, ApJL, 930, L20
Ghez, A. M., Duchêne, G., Matthews, K., et al. 2003, ApJL, 586, L127
Ghez, A. M., Salim, S., Weinberg, N. N., et al. 2008, ApJ, 689, 1044
Gillessen, S., Eisenhauer, F., Fritz, T. K., et al. 2009, ApJL, 707, L114
Goldwurm, A., Cordier, B., Paul, J., et al. 1994, Natur, 371, 589
Gravity Collaboration, Abuter, R., Aimar, N., et al. 2022, A&A, 657, L12
Gravity Collaboration, Abuter, R., Amorim, A., et al. 2018a, A&A, 615, L15
Gravity Collaboration, Abuter, R., Amorim, A., et al. 2018b, A&A, 618, L10
Gravity Collaboration, Abuter, R., Amorim, A., et al. 2019, A&A, 625, L10
Hilbert, D. 1917, Nachrichten von der Königlichen Gesellschaft der
Wissenschaften zu Göttingen—Mathematisch-physikalische Klasse
(Berlin: Weidmannsche Buchhandlung), 53

References
Abbott, B. P., Abbott, R., Abbott, T. D., et al. 2016, PhRvL, 116, 061102
Agol, E. 2000, ApJL, 538, L121
Baganoff, F. K., Bautz, M. W., Brandt, W. N., et al. 2001, Natur, 413, 45
Baganoff, F. K., Maeda, Y., Morris, M., et al. 2003, ApJ, 591, 891
Balick, B., & Brown, R. L. 1974, ApJ, 194, 265
Bardeen, J. M. 1973, in Black Holes (Les Astres Occlus), ed. C Dewitt &
B. S. Dewitt (New York: Gordon and Breach), 215
Blackburn, L., Chan, C.-k., Crew, G. B., et al. 2019, ApJ, 882, 23

16

## PDF page 17

The Astrophysical Journal Letters, 930:L12 (21pp), 2022 May 10

Event Horizon Telescope Collaboration et al.

Ho, L. C. 1999, ApJ, 516, 672
Janssen, M., Goddi, C., van Bemmel, I. M., et al. 2019, A&A, 626, A75
Jaroszynski, M., & Kurpiewski, A. 1997, A&A, 326, 419
Johannsen, T., & Psaltis, D. 2011, PhRvD, 83, 124015
Johnson, M. D., Fish, V. L., Doeleman, S. S., et al. 2015, Sci, 350, 1242
Johnson, M. D., Narayan, R., Psaltis, D., et al. 2018, ApJ, 865, 104
Joshi, P. S., Malafarina, D., & Narayan, R. 2014, CQGra, 31, 015002
Kerr, R. P. 1963, PhRvL, 11, 237
Kormendy, J., & Ho, L. C. 2013, ARA&A, 51, 511
Krichbaum, T. P., Graham, D. A., Witzel, A., et al. 1998, A&A, 335, L106
Lee, D., & Gammie, C. F. 2021, ApJ, 906, 39
Liska, M., Hesp, C., Tchekhovskoy, A., et al. 2018, MNRAS, 474, L81
Lo, K. Y., Schilizzi, R. T., Cohen, M. H., & Ross, H. N. 1975, ApJL, 202, L63
Lo, K. Y., Shen, Z.-Q., Zhao, J.-H., & Ho, P. T. P. 1998, ApJL, 508, L61
Lu, R.-S., Krichbaum, T. P., Roy, A. L., et al. 2018, ApJ, 859, 60
Luminet, J.-P. 1979, A&A, 75, 228
Lynden-Bell, D. 1969, Natur, 223, 690
Magorrian, J., Tremaine, S., Richstone, D., et al. 1998, AJ, 115, 2285
Markoff, S., Falcke, H., Yuan, F., & Biermann, P. L. 2001, A&A, 379, L13
Marrone, D. P., Moran, J. M., Zhao, J., & Rao, R. 2007, ApJ, 654, L57
Marrone, D. P., Moran, J. M., Zhao, J.-H., & Rao, R. 2006, ApJ, 640, 308
McClintock, J. E., & Remillard, R. A. 1986, ApJ, 308, 110
Mościbrodzka, M., Falcke, H., & Shiokawa, H. 2016, A&A, 586, A38
Mościbrodzka, M., Gammie, C. F., Dolence, J. C., Shiokawa, H., &
Leung, P. K. 2009, ApJ, 706, 497
Nagar, N. M., Falcke, H., Wilson, A. S., & Ho, L. C. 2000, ApJ, 542, 186
Narayan, R., Igumenshchev, I. V., & Abramowicz, M. A. 2000, ApJ, 539, 798
Narayan, R., Igumenshchev, I. V., & Abramowicz, M. A. 2003, PASJ, 55, L69
Narayan, R., & McClintock, J. E. 2008, NewAR, 51, 733
Narayan, R., Sądowski, A., Penna, R. F., & Kulkarni, A. K. 2012, MNRAS,
426, 3241
Narayan, R., Yi, I., & Mahadevan, R. 1995, Natur, 374, 623
Olivares, H., Younsi, Z., Fromm, C. M., et al. 2020, MNRAS, 497, 521
Oppenheimer, J. R., & Snyder, H. 1939, PhRv, 56, 455

Özel, F., Psaltis, D., & Narayan, R. 2000, ApJ, 541, 234
Özel, F., Psaltis, D., & Younsi, Z. 2021, arXiv:2111.01123
Padin, S., Woody, D. P., Hodges, M. W., et al. 1990, ApJL, 360, L11
Penrose, R. 1965, PhRvL, 14, 57
Predehl, P., & Truemper, J. 1994, A&A, 290, L29
Psaltis, D., Johnson, M., Narayan, R., et al. 2018, arXiv:1805.01242
Psaltis, D., Medeiros, L., Christian, P., et al. 2020, PhRvL, 125, 141104
Quataert, E. 2002, ApJ, 575, 855
Quataert, E., & Gruzinov, A. 2000a, ApJ, 539, 809
Quataert, E., & Gruzinov, A. 2000b, ApJ, 545, 842
Reid, M. J., & Brunthaler, A. 2020, ApJ, 892, 39
Reid, M. J., Menten, K. M., Brunthaler, A., et al. 2019, ApJ, 885, 131
Ressler, S. M., White, C. J., Quataert, E., & Stone, J. M. 2020, ApJL, 896,
L6
Richstone, D., Ajhar, E. A., Bender, R., et al. 1998, Natur, 385, A14
Rogers, A. E. E., Doeleman, S., Wright, M. C. H., et al. 1994, ApJL, 434, L59
Russell, C. M. P., Wang, Q. D., & Cuadra, J. 2017, MNRAS, 464, 4958
Satapathy, K., Psaltis, D., Özel, F., et al. 2022, ApJ, 925, 13
Schmidt, M. 1963, Natur, 197, 1040
Schödel, R., Ott, T., Genzel, R., et al. 2002, Natur, 419, 694
Schwarzschild, K. 1916, AbhKP, 189
Shaikh, R., Kocherlakota, P., Narayan, R., & Joshi, P. S. 2019, MNRAS,
482, 52
Shen, Z.-Q., Lo, K. Y., Liang, M.-C., Ho, P. T. P., & Zhao, J.-H. 2005, Natur,
438, 62
Thompson, A. R., Moran, J. M., & Swenson, G. W., Jr. 2017, Interferometry
and Synthesis in Radio Astronomy (3rd ed.; Berlin: Springer)
Wang, Q. D., Nowak, M. A., Markoff, S. B., et al. 2013, Sci, 341, 981
Webster, B. L., & Murdin, P. 1972, Natur, 235, 37
White, C. J., & Quataert, E. 2022, ApJ, 926, 136
Wielgus, M., Marchili, N., Martí-Vidal, I., et al. 2022, ApJL, 930, L19
Younsi, Z., Psaltis, D., & Özel, F. 2021, arXiv:2111.01752
Yuan, F., & Narayan, R. 2014, ARA&A, 52, 529
Zylka, R., Mezger, P. G., & Lesch, H. 1992, A&A, 261, 119

Event Horizon Telescope Collaboration,
Kazunori Akiyama
, Antxon Alberdi , Walter Alef5, Juan Carlos Algaba6 , Richard Anantua3,7,8 , Keiichi Asada9 ,
5,10,11
Rebecca Azulay
, Uwe Bach5 , Anne-Kathrin Baczko5 , David Ball12, Mislav Baloković13 , John Barrett1 ,
Michi Bauböck14 , Bradford A. Benson15,16 , Dan Bintley17,18, Lindy Blackburn3,7 , Raymond Blundell7 ,
Katherine L. Bouman19 , Geoffrey C. Bower20,21 , Hope Boyce22,23 , Michael Bremer24, Christiaan D. Brinkerink25 ,
Roger Brissenden3,7 , Silke Britzen5 , Avery E. Broderick26,27,28 , Dominique Broguiere24 , Thomas Bronzwaer25 ,
Sandra Bustamante29 , Do-Young Byun30,31 , John E. Carlstrom16,32,33,34 , Chiara Ceccobello35 , Andrew Chael36,37 ,
Chi-kwan Chan12,38,39 , Koushik Chatterjee3,7 , Shami Chatterjee40 , Ming-Tang Chen20 , Yongjun Chen (陈永军)41,42 ,
Xiaopeng Cheng30 , Ilje Cho4 , Pierre Christian43 , Nicholas S. Conroy7,44 , John E. Conway35 , James M. Cordes40 ,
Thomas M. Crawford16,32 , Geoffrey B. Crew1 , Alejandro Cruz-Osorio45 , Yuzhu Cui (崔玉竹)46,47,48 ,
Jordy Davelaar25,49,50 , Mariafelicia De Laurentis45,51,52 , Roger Deane53,54,55 , Jessica Dempsey17,18,56 ,
Gregory Desvignes5,57 , Jason Dexter58 , Vedant Dhruv14 , Sheperd S. Doeleman3,7 , Sean Dougal12 ,
Sergio A. Dzib5,24 , Ralph P. Eatough5,59 , Razieh Emami7 , Heino Falcke25 , Joseph Farah60,61 , Vincent L. Fish1 ,
Ed Fomalont62 , H. Alyson Ford12 , Raquel Fraga-Encinas25 , William T. Freeman63,64, Per Friberg17,18 ,
Christian M. Fromm5,45,65 , Antonio Fuentes4 , Peter Galison3,66,67 , Charles F. Gammie14,44,68 , Roberto García24 ,
Olivier Gentaz24 , Boris Georgiev26,27,28 , Ciriaco Goddi69,70 , Roman Gold45,71 , Arturo I. Gómez-Ruiz72,73 ,
José L. Gómez4 , Minfeng Gu (顾敏峰)41,74 , Mark Gurwell7 , Kazuhiro Hada47,48 , Daryl Haggard22,23 , Kari Haworth7,
Michael H. Hecht1 , Ronald Hesper75 , Dirk Heumann12 , Luis C. Ho (何子山)76,77 , Paul Ho9,17,18 ,
Mareki Honma47,48,78 , Chih-Wei L. Huang9 , Lei Huang (黄磊)41,74 , David H. Hughes72, Shiro Ikeda2,79,80,81 ,
C. M. Violette Impellizzeri62,82 , Makoto Inoue9 , Sara Issaoun7,37 , David J. James83 , Buell T. Jannuzi12 ,
Michael Janssen5 , Britton Jeter9 , Wu Jiang (江悟)41 , Alejandra Jiménez-Rosales25 , Michael D. Johnson3,7 ,
Svetlana Jorstad84 , Abhishek V. Joshi14 , Taehyun Jung30,31 , Mansour Karami26,27 , Ramesh Karuppusamy5 ,
Tomohisa Kawashima85 , Garrett K. Keating7 , Mark Kettenis86 , Dong-Jin Kim5 , Jae-Young Kim5,30,87 ,
Jongsoo Kim30 , Junhan Kim12,19 , Motoki Kino2,88 , Jun Yi Koay9 , Prashant Kocherlakota45 , Yutaro Kofuji47,78,
Patrick M. Koch9 , Shoko Koyama9,89 , Carsten Kramer24 , Michael Kramer5 , Thomas P. Krichbaum5 ,
Cheng-Yu Kuo9,90 , Noemi La Bella25 , Tod R. Lauer91 , Daeyoung Lee14 , Sang-Sung Lee30 , Po Kin Leung92 ,
Aviad Levis19 , Zhiyuan Li (李志远)93,94 , Rocco Lico4,95 , Greg Lindahl7 , Michael Lindqvist35 , Mikhail Lisakov5 ,
1,2,3

4

17

## PDF page 18

The Astrophysical Journal Letters, 930:L12 (21pp), 2022 May 10

Event Horizon Telescope Collaboration et al.

Jun Liu (刘俊) , Kuo Liu , Elisabetta Liuzzo
, Wen-Ping Lo
, Andrei P. Lobanov5 , Laurent Loinard98,99 ,
1
5,41,42
Colin J. Lonsdale , Ru-Sen Lu (路如森)
, Jirong Mao (毛基荣)100,101,102 , Nicola Marchili5,96 ,
Sera Markoff103,104 , Daniel P. Marrone12 , Alan P. Marscher84 , Iván Martí-Vidal10,11 , Satoki Matsushita9 ,
Lynn D. Matthews1 , Lia Medeiros12,105,106 , Karl M. Menten5 , Daniel Michalik16,107 , Izumi Mizuno17,18 ,
Yosuke Mizuno45,46,108 , James M. Moran3,7 , Kotaro Moriyama1,45,47 , Monika Moscibrodzka25 , Cornelia Müller5,25 ,
Alejandro Mus10,11 , Gibwa Musoke25,103 , Ioannis Myserlis109 , Andrew Nadolski44 , Hiroshi Nagai2,48 ,
Neil M. Nagar110 , Masanori Nakamura9,111 , Ramesh Narayan3,7 , Gopal Narayanan29 , Iniyan Natarajan53,112 ,
Antonios Nathanail45,113, Santiago Navarro Fuentes109, Joey Neilsen114 , Roberto Neri24 , Chunchong Ni26,27,28 ,
Aristeidis Noutsos5 , Michael A. Nowak115 , Junghwan Oh116 , Hiroki Okino47,78 , Héctor Olivares25 ,
Gisela N. Ortiz-León5,99 , Tomoaki Oyama47 , Feryal Özel12 , Daniel C. M. Palumbo3,7 , Georgios Filippos Paraschos5 ,
Jongho Park9,117 , Harriet Parsons17,18 , Nimesh Patel7 , Ue-Li Pen9,26,118,119,120 , Dominic W. Pesce3,7 , Vincent Piétu24,
Richard Plambeck121 , Aleksandar PopStefanija29, Oliver Porth45,103 , Felix M. Pötzl5,122 , Cora Prather14 ,
Jorge A. Preciado-López26 , Dimitrios Psaltis12 , Hung-Yi Pu9,123,124 , Venkatessh Ramakrishnan110,125,126 ,
Ramprasad Rao7 , Mark G. Rawlings17,18,127 , Alexander W. Raymond3,7 , Luciano Rezzolla45,128,129 , Angelo Ricarte3,7 ,
Bart Ripperda50,130 , Freek Roelofs3,7,25 , Alan Rogers1 , Eduardo Ros5 , Cristina Romero-Cañizales9 ,
Arash Roshanineshat12 , Helge Rottmann5, Alan L. Roy5 , Ignacio Ruiz109 , Chet Ruszczyk1 , Kazi L. J. Rygl96 ,
Salvador Sánchez109 , David Sánchez-Argüelles72,73 , Miguel Sánchez-Portal109 , Mahito Sasada47,131,132 ,
Kaushik Satapathy12 , Tuomas Savolainen5,126,133 , F. Peter Schloerb29, Jonathan Schonfeld7 , Karl-Friedrich Schuster24 ,
Lijing Shao5,77 , Zhiqiang Shen (沈志强)41,42 , Des Small86 , Bong Won Sohn30,31,134 , Jason SooHoo1 ,
Kamal Souccar29 , He Sun (孙赫)19 , Fumie Tazaki47 , Alexandra J. Tetarenko37,135 , Paul Tiede3,7 ,
Remo P. J. Tilanus12,25,82,136 , Michael Titus1 , Pablo Torne5,109 , Efthalia Traianou4,5 , Tyler Trent12, Sascha Trippe137 ,
Matthew Turk44 , Ilse van Bemmel86 , Huib Jan van Langevelde82,86,138 , Daniel R. van Rossum25 , Jesse Vos25 ,
Jan Wagner5 , Derek Ward-Thompson139 , John Wardle140 , Jonathan Weintroub3,7 , Norbert Wex5 , Robert Wharton5 ,
Maciek Wielgus5 , Kaj Wiik141 , Gunther Witzel5 , Michael F. Wondrak25,142 , George N. Wong106,143 , Qingwen Wu
(吴庆文)144 , Paul Yamaguchi7 , Doosoo Yoon103 , André Young25 , Ken Young7 , Ziri Younsi45,145 , Feng Yuan
(袁峰)41,74,146 , Ye-Fei Yuan (袁业飞)147 , J. Anton Zensus5 , Shuo Zhang148 , Guang-Yao Zhao4 , Shan-Shan Zhao
(赵杉杉)41 , Claudio Agurto149, Alexander Allardi150, Rodrigo Amestica151, Juan Pablo Araneda149, Oriel Arriagada149,
Jennie L. Berghuis152 , Alessandra Bertarini5,153, Ryan Berthold17,18, Jay Blanchard154 , Ken Brown17,18, Mauricio Cárdenas149,
Michael Cantzler149, Patricio Caro149, Edgar Castillo-Domínguez73,155, Tin Lok Chan92 , Chih-Cheng Chang9,156,
Dominic O. Chang3,7, Shu-Hao Chang9, Song-Chu Chang156, Chung-Chen Chen9, Ryan Chilson20, Tim C. Chuter17,18,
Miroslaw Ciechanowicz5,149, Edgar Colin-Beltran72,73, Iain M. Coulson17,18 , Joseph Crowley1, Nathalie Degenaar103 ,
Sven Dornbusch5, Carlos A. Durán149 , Wendeline B. Everett157 , Aaron Faber158, Karl Forster159 , Miriam M. Fuchs160,
David M. Gale72, Gertie Geertsema161, Edouard González149, Dave Graham5, Frédéric Gueth24, Nils W. Halverson162 ,
Chih-Chiang Han9, Kuo-Chang Han156, Yutaka Hasegawa163, José Luis Hernández-Rebollar72, Cristian Herrera149,
Ruben Herrero-Illana149 , Stefan Heyminck5, Akihiko Hirota2,164 , James Hoge17,18, Shelbi R. Hostler Schimpf7,
Ryan E. Howie165 , Yau-De Huang9, Homin Jiang9, Hao Jinchi156, David John109, Kimihiro Kimura163, Thomas Klein149,
Derek Kubo20, John Kuroda17,18, Caleb Kwon114 , Richard Lacasse151, Robert Laing166,167 , Erik M. Leitch32 , Chao-Te Li9,
Ching-Tang Liu9, Kuan-Yu Liu9,17,18, Lupin C.-C. Lin168 , Li-Ming Lu156, Felipe Mac-Auliffe149, Pierre Martin-Cocher9,
Callie Matulonis17,18, John K. Maute7 , Hugo Messias149,164 , Zheng Meyer-Zhao56, Alfredo Montaña72,73,
Francisco Montenegro-Montes149 , William Montgomerie17,18,169, Marcos Emir Moreno Nolasco170, Dirk Muders5 ,
Hiroaki Nishioka9, Timothy J. Norton7, George Nystrom20, Hideo Ogawa163, Rodrigo Olivares149, Peter Oshiro20,
Juan Pablo Pérez-Beaupuits5,149,171 , Rodrigo Parra149, Neil M. Phillips167, Michael Poirier1 , Nicolas Pradel9,
Richard Qiu172,173 , Philippe A. Rafﬁn20, Alexandra S. Rahlin15,32 , Jorge Ramírez149, Sean Ressler174 , Mark Reynolds175 ,
Iván Rodríguez-Montoya72,73, Alejandro F. Saez-Madain151,164 , Jorge Santana149, Paul Shaw9, Leslie E. Shirkey, Jr.7,
Kevin M. Silva17,18, William Snow20, Don Sousa1 , T. K. Sridharan7, William Stahm17,18, Anthony A. Stark7 , John Test7,
Karl Torstensson149, Paulina Venegas149, Craig Walther17,18, Ta-Shun Wei9, Chris White130 , Gundolf Wieching5,
Rudy Wijnands103 , Jan G. A. Wouterloot17,18 , Chen-Yu Yu9, Wei Yu (于威)7 , and Milagros Zeballos72,176
5

5

96

9,97

1

Massachusetts Institute of Technology Haystack Observatory, 99 Millstone Road, Westford, MA 01886, USA
2
National Astronomical Observatory of Japan, 2-21-1 Osawa, Mitaka, Tokyo 181-8588, Japan
3
Black Hole Initiative at Harvard University, 20 Garden Street, Cambridge, MA 02138, USA
4
Instituto de Astrofísica de Andalucía-CSIC, Glorieta de la Astronomía s/n, E-18008 Granada, Spain
5
Max-Planck-Institut für Radioastronomie, Auf dem Hügel 69, D-53121 Bonn, Germany
6
Department of Physics, Faculty of Science, Universiti Malaya, 50603 Kuala Lumpur, Malaysia
7
Center for Astrophysics | Harvard & Smithsonian, 60 Garden Street, Cambridge, MA 02138, USA
8
Department of Physics & Astronomy, The University of Texas at San Antonio, One UTSA Circle, San Antonio, TX 78249, USA
9
Institute of Astronomy and Astrophysics, Academia Sinica, 11F of Astronomy-Mathematics Building, AS/NTU No. 1, Sec. 4, Roosevelt Rd., Taipei 10617, Taiwan,
R.O.C.
10
Departament d’Astronomia i Astrofísica, Universitat de València, C. Dr. Moliner 50, E-46100 Burjassot, València, Spain

18

## PDF page 19

The Astrophysical Journal Letters, 930:L12 (21pp), 2022 May 10

Event Horizon Telescope Collaboration et al.

11

Observatori Astronòmic, Universitat de València, C. Catedrático José Beltrán 2, E-46980 Paterna, València, Spain
Steward Observatory and Department of Astronomy, University of Arizona, 933 N. Cherry Ave., Tucson, AZ 85721, USA
13
Yale Center for Astronomy & Astrophysics, Yale University, 52 Hillhouse Avenue, New Haven, CT 06511, USA
14
Department of Physics, University of Illinois, 1110 West Green Street, Urbana, IL 61801, USA
15
Fermi National Accelerator Laboratory, MS209, P.O. Box 500, Batavia, IL 60510, USA
16
Department of Astronomy and Astrophysics, University of Chicago, 5640 South Ellis Avenue, Chicago, IL 60637, USA
17
East Asian Observatory, 660 N. A’ohoku Place, Hilo, HI 96720, USA
18
James Clerk Maxwell Telescope (JCMT), 660 N. A’ohoku Place, Hilo, HI 96720, USA
19
California Institute of Technology, 1200 East California Boulevard, Pasadena, CA 91125, USA
20
Institute of Astronomy and Astrophysics, Academia Sinica, 645 N. A’ohoku Place, Hilo, HI 96720, USA
21
Department of Physics and Astronomy, University of Hawaii at Manoa, 2505 Correa Road, Honolulu, HI 96822, USA
22
Department of Physics, McGill University, 3600 rue University, Montréal, QC H3A 2T8, Canada
23
McGill Space Institute, McGill University, 3550 rue University, Montréal, QC H3A 2A7, Canada
24
Institut de Radioastronomie Millimétrique (IRAM), 300 rue de la Piscine, F-38406 Saint Martin d’Hères, France
25
Department of Astrophysics, Institute for Mathematics, Astrophysics and Particle Physics (IMAPP), Radboud University, P.O. Box 9010, 6500 GL Nijmegen, The
Netherlands
26
Perimeter Institute for Theoretical Physics, 31 Caroline Street N, Waterloo, ON N2L 2Y5, Canada
27
Department of Physics and Astronomy, University of Waterloo, 200 University Avenue W, Waterloo, ON N2L 3G1, Canada
28
Waterloo Centre for Astrophysics, University of Waterloo, Waterloo, ON N2L 3G1, Canada
29
Department of Astronomy, University of Massachusetts, Amherst, MA 01003, USA
30
Korea Astronomy and Space Science Institute, Daedeok-daero 776, Yuseong-gu, Daejeon 34055, Republic of Korea
31
University of Science and Technology, Gajeong-ro 217, Yuseong-gu, Daejeon 34113, Republic of Korea
32
Kavli Institute for Cosmological Physics, University of Chicago, 5640 South Ellis Avenue, Chicago, IL 60637, USA
33
Department of Physics, University of Chicago, 5720 South Ellis Avenue, Chicago, IL 60637, USA
34
Enrico Fermi Institute, University of Chicago, 5640 South Ellis Avenue, Chicago, IL 60637, USA
35
Department of Space, Earth and Environment, Chalmers University of Technology, Onsala Space Observatory, SE-43992 Onsala, Sweden
36
Princeton Center for Theoretical Science, Jadwin Hall, Princeton University, Princeton, NJ 08544, USA
37
NASA Hubble Fellowship Program, Einstein Fellow
38
Data Science Institute, University of Arizona, 1230 N. Cherry Ave., Tucson, AZ 85721, USA
39
Program in Applied Mathematics, University of Arizona, 617 N. Santa Rita, Tucson, AZ 85721, USA
40
Cornell Center for Astrophysics and Planetary Science, Cornell University, Ithaca, NY 14853, USA
41
Shanghai Astronomical Observatory, Chinese Academy of Sciences, 80 Nandan Road, Shanghai 200030, Peopleʼs Republic of China
42
Key Laboratory of Radio Astronomy, Chinese Academy of Sciences, Nanjing 210008, Peopleʼs Republic of China
43
Physics Department, Fairﬁeld University, 1073 North Benson Road, Fairﬁeld, CT 06824, USA
44
Department of Astronomy, University of Illinois at Urbana-Champaign, 1002 West Green Street, Urbana, IL 61801, USA
45
Institut für Theoretische Physik, Goethe-Universität Frankfurt, Max-von-Laue-Straße 1, D-60438 Frankfurt am Main, Germany
46
Tsung-Dao Lee Institute, Shanghai Jiao Tong University, Shengrong Road 520, Shanghai, 201210, Peopleʼs Republic of China
47
Mizusawa VLBI Observatory, National Astronomical Observatory of Japan, 2-12 Hoshigaoka, Mizusawa, Oshu, Iwate 023-0861, Japan
48
Department of Astronomical Science, The Graduate University for Advanced Studies (SOKENDAI), 2-21-1 Osawa, Mitaka, Tokyo 181-8588, Japan
49
Department of Astronomy and Columbia Astrophysics Laboratory, Columbia University, 550 W. 120th Street, New York, NY 10027, USA
50
Center for Computational Astrophysics, Flatiron Institute, 162 Fifth Avenue, New York, NY 10010, USA
51
Dipartimento di Fisica “E. Pancini,” Universitá di Napoli “Federico II,” Compl. Univ. di Monte S. Angelo, Ediﬁcio G, Via Cinthia, I-80126, Napoli, Italy
52
INFN Sez. di Napoli, Compl. Univ. di Monte S. Angelo, Ediﬁcio G, Via Cinthia, I-80126, Napoli, Italy
53
Wits Centre for Astrophysics, University of the Witwatersrand, 1 Jan Smuts Avenue, Braamfontein, Johannesburg 2050, South Africa
54
Department of Physics, University of Pretoria, Hatﬁeld, Pretoria 0028, South Africa
55
Centre for Radio Astronomy Techniques and Technologies, Department of Physics and Electronics, Rhodes University, Makhanda 6140, South Africa
56
ASTRON, Oude Hoogeveensedijk 4, 7991 PD Dwingeloo, The Netherlands
57
LESIA, Observatoire de Paris, Université PSL, CNRS, Sorbonne Université, Université de Paris, 5 place Jules Janssen, F-92195 Meudon, France
58
JILA and Department of Astrophysical and Planetary Sciences, University of Colorado, Boulder, CO 80309, USA
59
National Astronomical Observatories, Chinese Academy of Sciences, 20A Datun Road, Chaoyang District, Beijing 100101, Peopleʼs Republic of China
60
Las Cumbres Observatory, 6740 Cortona Drive, Suite 102, Goleta, CA 93117-5575, USA
61
Department of Physics, University of California, Santa Barbara, CA 93106-9530, USA
62
National Radio Astronomy Observatory, 520 Edgemont Road, Charlottesville, VA 22903, USA
63
Department of Electrical Engineering and Computer Science, Massachusetts Institute of Technology, 32-D476, 77 Massachusetts Ave., Cambridge, MA
02142, USA
64
Google Research, 355 Main St., Cambridge, MA 02142, USA
65
Institut für Theoretische Physik und Astrophysik, Universität Würzburg, Emil-Fischer-Str. 31, D-97074 Würzburg, Germany
66
Department of History of Science, Harvard University, Cambridge, MA 02138, USA
67
Department of Physics, Harvard University, Cambridge, MA 02138, USA
68
NCSA, University of Illinois, 1205 W. Clark St., Urbana, IL 61801, USA
69
Dipartimento di Fisica, Università degli Studi di Cagliari, SP Monserrato-Sestu km 0.7, I-09042 Monserrato, Italy
70
INAF—Osservatorio Astronomico di Cagliari, Via della Scienza 5, 09047, Selargius, CA, Italy
71
CP3-Origins, University of Southern Denmark, Campusvej 55, DK-5230 Odense M, Denmark
72
Instituto Nacional de Astrofísica, Óptica y Electrónica. Apartado Postal 51 y 216, 72000. Puebla Pue., MÉxico
73
Consejo Nacional de Ciencia y Tecnologìa, Av. Insurgentes Sur 1582, 03940, Ciudad de México, MÉxico
74
Key Laboratory for Research in Galaxies and Cosmology, Chinese Academy of Sciences, Shanghai 200030, Peopleʼs Republic of China
75
NOVA Sub-mm Instrumentation Group, Kapteyn Astronomical Institute, University of Groningen, Landleven 12, 9747 AD Groningen, The Netherlands
76
Department of Astronomy, School of Physics, Peking University, Beijing 100871, Peopleʼs Republic of China
77
Kavli Institute for Astronomy and Astrophysics, Peking University, Beijing 100871, Peopleʼs Republic of China
78
Department of Astronomy, Graduate School of Science, The University of Tokyo, 7-3-1 Hongo, Bunkyo-ku, Tokyo 113-0033, Japan
79
The Institute of Statistical Mathematics, 10-3 Midori-cho, Tachikawa, Tokyo, 190-8562, Japan
80
Department of Statistical Science, The Graduate University for Advanced Studies (SOKENDAI), 10-3 Midori-cho, Tachikawa, Tokyo 190-8562, Japan
81
Kavli Institute for the Physics and Mathematics of the Universe, The University of Tokyo, 5-1-5 Kashiwanoha, Kashiwa, 277-8583, Japan
82
Leiden Observatory, Leiden University, Postbus 2300, 9513 RA Leiden, The Netherlands
83
ASTRAVEO LLC, PO Box 1668, Gloucester, MA 01931, USA
12

19

## PDF page 20

The Astrophysical Journal Letters, 930:L12 (21pp), 2022 May 10

Event Horizon Telescope Collaboration et al.

84

Institute for Astrophysical Research, Boston University, 725 Commonwealth Ave., Boston, MA 02215, USA
Institute for Cosmic Ray Research, The University of Tokyo, 5-1-5 Kashiwanoha, Kashiwa, Chiba 277-8582, Japan
86
Joint Institute for VLBI ERIC (JIVE), Oude Hoogeveensedijk 4, 7991 PD Dwingeloo, The Netherlands
87
Department of Astronomy and Atmospheric Sciences, Kyungpook National University, Daegu 702-701, Republic of Korea
88
Kogakuin University of Technology & Engineering, Academic Support Center, 2665-1 Nakano, Hachioji, Tokyo 192-0015, Japan
89
Niigata University, 8050 Ikarashi-nino-cho, Nishi-ku, Niigata 950-2181, Japan
90
Physics Department, National Sun Yat-Sen University, No. 70, Lien-Hai Road, Kaosiung City 80424, Taiwan, R.O.C.
91
National Optical Astronomy Observatory, 950 N. Cherry Ave., Tucson, AZ 85719, USA
92
Department of Physics, The Chinese University of Hong Kong, Shatin, N.T., Hong Kong
93
School of Astronomy and Space Science, Nanjing University, Nanjing 210023, Peopleʼs Republic of China
94
Key Laboratory of Modern Astronomy and Astrophysics, Nanjing University, Nanjing 210023, Peopleʼs Republic of China
95
INAF-Istituto di Radioastronomia, Via P. Gobetti 101, I-40129 Bologna, Italy
96
INAF-Istituto di Radioastronomia & Italian ALMA Regional Centre, Via P. Gobetti 101, I-40129 Bologna, Italy
97
Department of Physics, National Taiwan University, No. 1, Sec. 4, Roosevelt Rd., Taipei 10617, Taiwan, R.O.C
98
Instituto de Radioastronomía y Astrofísica, Universidad Nacional Autónoma de México, Morelia 58089, MÉxico
99
Instituto de Astronomía, Universidad Nacional Autónoma de México (UNAM), Apdo Postal 70-264, Ciudad de México, MÉxico
100
Yunnan Observatories, Chinese Academy of Sciences, 650011 Kunming, Yunnan Province, Peopleʼs Republic of China
101
Center for Astronomical Mega-Science, Chinese Academy of Sciences, 20A Datun Road, Chaoyang District, Beijing, 100012, Peopleʼs Republic of China
102
Key Laboratory for the Structure and Evolution of Celestial Objects, Chinese Academy of Sciences, 650011 Kunming, Peopleʼs Republic of China
103
Anton Pannekoek Institute for Astronomy, University of Amsterdam, Science Park 904, 1098 XH, Amsterdam, The Netherlands
104
Gravitation and Astroparticle Physics Amsterdam (GRAPPA) Institute, University of Amsterdam, Science Park 904, 1098 XH Amsterdam, The Netherlands
105
NSF Astronomy and Astrophysics Postdoctoral Fellow
106
School of Natural Sciences, Institute for Advanced Study, 1 Einstein Drive, Princeton, NJ 08540, USA
107
Science Support Ofﬁce, Directorate of Science, European Space Research and Technology Centre (ESA/ESTEC), Keplerlaan 1, 2201 AZ Noordwijk, The
Netherlands
108
School of Physics and Astronomy, Shanghai Jiao Tong University, 800 Dongchuan Road, Shanghai, 200240, Peopleʼs Republic of China
109
Institut de Radioastronomie Millimétrique (IRAM), Avenida Divina Pastora 7, Local 20, E-18012, Granada, Spain
110
Astronomy Department, Universidad de Concepción, Casilla 160-C, Concepción, Chile
111
National Institute of Technology, Hachinohe College, 16-1 Uwanotai, Tamonoki, Hachinohe City, Aomori 039-1192, Japan
112
South African Radio Astronomy Observatory, Observatory 7925, Cape Town, South Africa
113
Department of Physics, National and Kapodistrian University of Athens, Panepistimiopolis, GR 15783 Zografos, Greece
114
Department of Physics, Villanova University, 800 Lancaster Avenue, Villanova, PA 19085, USA
115
Physics Department, Washington University CB 1105, St. Louis, MO 63130, USA
116
Sejong University, 209 Neungdong-ro, Gwangjin-gu, Seoul, Republic of Korea
117
EACOA Fellow
118
Canadian Institute for Theoretical Astrophysics, University of Toronto, 60 St. George Street, Toronto, ON M5S 3H8, Canada
119
Dunlap Institute for Astronomy and Astrophysics, University of Toronto, 50 St. George Street, Toronto, ON M5S 3H4, Canada
120
Canadian Institute for Advanced Research, 180 Dundas St. W, Toronto, ON M5G 1Z8, Canada
121
Radio Astronomy Laboratory, University of California, Berkeley, CA 94720, USA
122
Department of Physics, University College Cork, Kane Building, College Road, Cork T12 K8AF, Ireland
123
Department of Physics, National Taiwan Normal University, No. 88, Sec. 4, Tingzhou Rd., Taipei 116, Taiwan, R.O.C.
124
Center of Astronomy and Gravitation, National Taiwan Normal University, No. 88, Sec. 4, Tingzhou Road, Taipei 116, Taiwan, R.O.C.
125
Finnish Centre for Astronomy with ESO, FI-20014 University of Turku, Finland
126
Aalto University Metsähovi Radio Observatory, Metsähovintie 114, FI-02540 Kylmälä, Finland
127
Gemini Observatory/NSF NOIRLab, 670 N. A’ohoku Place, Hilo, HI 96720, USA
128
Frankfurt Institute for Advanced Studies, Ruth-Moufang-Strasse 1, D-60438 Frankfurt, Germany
129
School of Mathematics, Trinity College, Dublin 2, Ireland
130
Department of Astrophysical Sciences, Peyton Hall, Princeton University, Princeton, NJ 08544, USA
131
Department of Physics, Tokyo Institute of Technology, 2-12-1 Ookayama, Meguro-ku, Tokyo 152-8551, Japan
132
Hiroshima Astrophysical Science Center, Hiroshima University, 1-3-1 Kagamiyama, Higashi-Hiroshima, Hiroshima 739-8526, Japan
133
Aalto University Department of Electronics and Nanoengineering, PL 15500, FI-00076 Aalto, Finland
134
Department of Astronomy, Yonsei University, Yonsei-ro 50, Seodaemun-gu, 03722 Seoul, Republic of Korea
135
Department of Physics and Astronomy, Texas Tech University, Lubbock, Texas 79409-1051, USA
136
Netherlands Organisation for Scientiﬁc Research (NWO), Postbus 93138, 2509 AC Den Haag, The Netherlands
137
Department of Physics and Astronomy, Seoul National University, Gwanak-gu, Seoul 08826, Republic of Korea
138
University of New Mexico, Department of Physics and Astronomy, Albuquerque, NM 87131, USA
139
Jeremiah Horrocks Institute, University of Central Lancashire, Preston PR1 2HE, UK
140
Physics Department, Brandeis University, 415 South Street, Waltham, MA 02453, USA
141
Tuorla Observatory, Department of Physics and Astronomy, University of Turku, Finland
142
Radboud Excellence Fellow of Radboud University, Nijmegen, The Netherlands
143
Princeton Gravity Initiative, Princeton University, Princeton, NJ 08544, USA
144
School of Physics, Huazhong University of Science and Technology, Wuhan, Hubei, 430074, Peopleʼs Republic of China
145
Mullard Space Science Laboratory, University College London, Holmbury St. Mary, Dorking, Surrey, RH5 6NT, UK
146
School of Astronomy and Space Sciences, University of Chinese Academy of Sciences, No. 19A Yuquan Road, Beijing 100049, Peopleʼs Republic of China
147
Astronomy Department, University of Science and Technology of China, Hefei 230026, Peopleʼs Republic of China
148
Bard College, 30 Campus Road, Annandale-on-Hudson, NY, 12504, USA
149
European Southern Observatory, Alonso de Córdova 3107, Vitacura, Casilla 19001, Santiago de Chile, Chile
150
University of Vermont, Burlington, VT 05405, USA
151
National Radio Astronomy Observatory, NRAO Technology Center, 1180 Boxwood Estate Road, Charlottesville, VA 22903, USA
152
Gemini Observatory, 670 N. A’ohoku Place, Hilo, HI 96720, USA
153
Institute of Geodesy and Geoinformation, University of Bonn, D-53113 Bonn, Germany
154
National Radio Astronomy Observatory, Socorro, NM 87801, USA
155
SRON-Netherlands Institute for Space Research, Landleven 12, 9747 AD Groningen, Netherlands
156
National Chung-Shan Institute of Science and Technology, No. 566, Ln. 134, Longyuan Rd., Longtan Dist., Taoyuan City 325, Taiwan, R.O.C.
157
CASA, Department of Astrophysical and Planetary Sciences, University of Colorado, Boulder, CO 80309, USA
85

20

## PDF page 21

The Astrophysical Journal Letters, 930:L12 (21pp), 2022 May 10

Event Horizon Telescope Collaboration et al.

158

Western University, 1151 Richmond Street, London, ON N6A 3K7, Canada
Space Radiation Laboratory, California Institute of Technology, 1200 East California Boulevard, Pasadena, CA 91125, USA
160
Drexel University, 3141 Chestnut Street, Philadelphia PA 19104, USA
161
Research and Development Weather and Climate Models, Royal Netherlands Meteorological Institute, Utrechtseweg 297, 3731 GA, De Bilt, The Netherlands
162
Department of Astrophysical and Planetary Sciences and Department of Physics, University of Colorado, Boulder, CO 80309, USA
163
Osaka Prefecture University, Gakuencyou Sakai Osaka, Sakai 599-8531, Kinki, Japan
164
Joint ALMA Observatory, Alonso de Córdova 3107, Vitacura 763-0355, Santiago de Chile, Chile
165
MMT Observatory, P.O. Box 210065, University of Arizona, Tucson, AZ 85721, USA
166
SKA Observatory, Jodrell Bank, Lower Withington, Macclesﬁeld SK11 9FT, USA
167
European Southern Observatory, Karl-Schwarzschild-Strasse 2, D-85478 Garching, Germany
168
Department of Physics, National Cheng Kung University, Tainan 701401, Taiwan, R.O.C.
169
SOFIA Science Center, Universities Space Research Association, NASA Ames Research Center, Moffett Field, CA 94035, USA
170
Coorporación Mexicana de Investigación en Materiales S.A. de C.V., Ciencia y Tecnología 790, Colonia Saltillo 400, Saltillo, Coahuila, C.P. 25290, Mexico
171
Centro de Astro-Ingeniería (AIUC), Pontiﬁcia Universidad Católica de Chile, Av. Vicuña Mackena 4860, Macul, Santiago, Chile
172
Department of Physics, Harvard University, 17 Oxford Street, Cambridge, MA 02138, USA
173
John A. Paulson School of Engineering and Applied Sciences, Harvard University, 29 Oxford Street, Cambridge, MA 02138, USA
174
Kavli Institute For Theoretical Physics, 2411 Kohn Hall, Santa Barbara, CA 93111 USA
175
Department of Astronomy, University of Michigan, 1085 South University Avenue, Ann Arbor, MI 48109, USA
176
Universidad de las Américas Puebla, Sta. Catarina Mártir S/N, San Andrés Cholula, Puebla, C.P. 72810, Mexico
159

21
