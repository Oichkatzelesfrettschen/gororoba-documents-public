Source: https://arxiv.org/abs/2507.13794v2
PDF sha256: 21ed5b3beebe9fc8a6d40b712879feb03f50c61302c6d0d45aa245afb64aa3b4
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of mroz_2025_ogle_smc_microlensing.pdf

Transcription of `mroz_2025_ogle_smc_microlensing.pdf` in this directory, 22 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-22 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Draft version October 24, 2025
Typeset using LATEX twocolumn style in AASTeX63

Microlensing optical depth, event rate, and limits on compact objects in dark matter based on
20 years of OGLE observations of the Small Magellanic Cloud

arXiv:2507.13794v2 [astro-ph.GA] 22 Oct 2025

Przemek Mróz,1 Andrzej Udalski,1 Michał K. Szymański,1 Igor Soszyński,1 Paweł Pietrukowicz,1
Szymon Kozłowski,1 Radosław Poleski,1 Jan Skowron,1 Dorota Skowron,1 Krzysztof Ulaczyk,2, 1
Mariusz Gromadzki,1 Krzysztof Rybicki,3, 1 Patryk Iwanek,1 Marcin Wrona,4, 1 and Milena Ratajczak1
1 Astronomical Observatory, University of Warsaw, Al. Ujazdowskie 4, 00-478 Warszawa, Poland
2 Department of Physics, University of Warwick, Coventry CV4 7 AL, UK
3 Department of Particle Physics and Astrophysics, Weizmann Institute of Science, Rehovot 76100, Israel
4 Department of Astrophysics and Planetary Science, Villanova University, 800 East Lancaster Avenue, Villanova, PA 19085, USA

(Received; Revised; Accepted)

ABSTRACT
Some previous studies have suggested that massive and intermediate-mass primordial black holes
(PBHs) could comprise a substantial fraction of dark matter in the Universe. Such black holes, if
they existed in the Milky Way halo, would give rise to long-duration microlensing events that may
potentially last for years. However, earlier searches were not sufficiently sensitive to detect such events.
Here, we present the results of searches for long-timescale gravitational microlensing events toward the
Small Magellanic Cloud (SMC) using nearly 20 yr of photometric observations collected by the Optical
Gravitational Lensing Experiment (OGLE) from 2001–2020. We found six events, three of which are
new discoveries. We use a sample of five events to measure the microlensing optical depth toward
the SMC τ = (0.32 ± 0.18) × 10−7 and the event rate Γ = (1.18 ± 0.57) × 10−7 yr−1 star−1 . The
properties of the detected events are consistent with lenses originating from known stellar populations
within the SMC or in the Milky Way disk. No events with timescales longer than 1 yr were detected,
which provides competitive limits on the fraction of massive compact objects, including PBHs, in the
Milky Way dark matter halo. Together with the earlier OGLE studies of microlensing events in the
direction of the Large Magellanic Cloud, these observations rule out PBHs and other compact objects
with masses ranging from 10−8 –103 M⊙ as dominant components of dark matter.
Keywords: Gravitational microlensing (672); Dark matter (353); Milky Way dark matter halo (1049);
Small Magellanic Cloud (1468); Primordial black holes (1292); Intermediate-mass black
holes (816)
1. INTRODUCTION

The hypothesis that primordial black holes (PBHs)
may account for a substantial part of dark matter has
gained some popularity in recent years, especially after the discoveries of mergers of unexpectedly massive black holes by gravitational-wave detectors LIGO
and Virgo (e.g., Bird et al. 2016; Sasaki et al. 2016;
Clesse & García-Bellido 2017). PBHs are hypothesized
to have formed in the very early Universe by the collapse of large density perturbations (e.g., Zel’dovich &
Corresponding author: Przemek Mróz
pmroz@astrouw.edu.pl

Novikov 1967; Hawking 1971; Carr & Hawking 1974;
Chapline 1975). Because the formation of PBHs is
thought to have occurred before the Big Bang nucleosynthesis, PBHs are nonbaryonic, and their current abundance is not constrained by primordial elemental abundances (e.g., Navas et al. 2024, and references therein).
Although PBHs cannot be directly observed, their existence would manifest in a number of phenomena, including (but not limited to) gravitational microlensing
of background stars, emission of Hawking radiation, production of gravitational waves, accretion of gas, impact
on the dynamics of dwarf galaxies and wide binary star
systems, or cosmological structure formation (see the re-

## PDF page 2

2

P. Mróz et al.

views by Green & Kavanagh 2021; Carr et al. 2021; Carr
et al. 2024).
Despite this rich phenomenology, searches for PBH
signatures have not provided compelling arguments for
the PBH dark matter hypothesis. Instead, these investigations have led to numerous constraints on the amount
of the PBH dark matter in the Universe as a function of
the PBH mass. These constraints are often calculated
under the assumption of a smooth distribution of dark
matter in galactic halos. However, numerical simulations of galaxy formation indicate that dark matter halos
may contain numerous substructures, with characteristic sizes depending on the specific dark matter model
(e.g., Bechtol et al. 2022). They may be detected, for
example, using observations of strongly lensed galaxies.
Vegetti et al. (2010, 2012) reported the discovery of such
substructures with masses of the order of 108 −109 M⊙
but it is unclear whether they are associated with lensing galaxies or some unrelated structures along the line
of sight (e.g., Li et al. 2017; Despali et al. 2018; Sengül
et al. 2022).
Some of the strongest constraints on the abundance of
PBHs with masses from 10−8 M⊙ to 103 M⊙ come from
searches for gravitational microlensing events in the
long-term photometric observations of stars in the Magellanic Clouds, as first proposed by Paczyński (1986).
The long-term observations of the Large Magellanic
Cloud (LMC) by the Optical Gravitational Lensing Experiment (OGLE; Mróz et al. 2024b,c, hereafter Paper 1
and Paper 2, respectively) demonstrate that less than
1% of dark matter may be composed of compact objects
with masses from 1.8 × 10−4 to 6.3 M⊙ . High-cadence
OGLE observations of the LMC and the Small Magellanic Cloud (SMC) provide strong limits on the abundance of planetary-mass PBHs (Mróz et al. 2024a, hereafter, Paper 3). These limits supersede the earlier constraints derived from searches for microlensing events toward the LMC by MACHO (Alcock et al. 1997b, 2000),
EROS (Tisserand et al. 2007; Blaineau et al. 2022),
OGLE-II (Wyrzykowski et al. 2009), and OGLE-III
(Wyrzykowski et al. 2011a) experiments by more than
an order of magnitude. However, to probe possible dark
matter substructures in the Milky Way halo, it is important to search for gravitational microlensing events
toward different sky directions.
One possible target is the Andromeda galaxy (M31).
The searches for massive compact halo objects in the direction of M31 by Calchi Novati et al. (2005) and de Jong
et al. (2006) yielded contradictory results due to the
difficulty in distinguishing self-lensing events (in which
stars from M31 are lensing stars in the same galaxy)
from those by PBHs (see also Calchi Novati 2010). On

the other hand, the high-cadence observations of M31 by
the Subaru Hyper Suprime-Cam (HSC) survey (Niikura
et al. 2019) provided strong limits on the abundance of
moon- to planetary-mass PBHs (10−10 − 10−6 M⊙ ) in
dark matter.
The SMC was also a target of microlensing surveys.
The MACHO project, which operated from 1992 to
1999, reported the discovery of two microlensing events
toward this galaxy (Alcock et al. 1997a, 1999). The
EROS-2 survey (1996–2003) detected only one event.
Only one event in the SMC was found in the OGLE-II
data (1996–2000) by Wyrzykowski et al. (2010), and
three events were found in the OGLE-III data (2001–
2009) by Wyrzykowski et al. (2011b). These small numbers were consistent with the expected number of selflensing events (Sahu 1994; Calchi Novati et al. 2013;
Mróz & Poleski 2018), in which both the microlensing source and lens are located in the same galaxy, and
events by nearby lenses in the Milky Way disk (Gould
et al. 1994). No PBHs were required to explain these
events.
Previous SMC surveys were not sensitive to very longduration microlensing events (with timescales of several
years) that are expected from massive and intermediatemass black holes, similar to those detected in large numbers by the LIGO and Virgo observatories. In this study,
we combined the data collected during the third and
fourth phases of the OGLE project to create nearly 20 yr
long, uniform light curves for about 7.4 million stars in
the SMC. In addition, 6.2 million stars were observed by
OGLE-IV only. This paper presents the results of our
search for the very long-duration microlensing events in
this data set.
The data set analyzed in this study is described in
Section 2. The selection criteria for microlensing events
are detailed in Section 3, while Section 4 presents the
properties of the events that we discovered. Sections
5, 6, and 7 outline the calculations of the number of
source stars, detection efficiencies, and the microlensing
optical depth in the direction of the SMC, respectively.
In Section 8, we demonstrate that the detected events
can be explained by the known stellar populations in
both the Milky Way and the SMC. Finally, in Sections 9
and 10, we calculate the limits on the PBH abundance
in dark matter and discuss our results.
2. DATA

2.1. OGLE-IV Data
The photometric data that are analyzed in this paper were collected during the fourth phase of the OGLE
survey (OGLE-IV; Udalski et al. 2015) between June
29, 2010 (JD = 2, 455, 377) and March 15, 2020 (JD =

## PDF page 3

3

Microlensing Optical Depth toward the SMC

Figure 1. OGLE-IV fields toward the Small Magellanic Cloud (SMC) are shown with white polygons. The numbers in the
center of each polygon in the right panel indicate the field number. The yellow lines mark the regions that were observed during
the OGLE-III phase. Detected microlensing events are marked with black circles. The background image of the SMC was
generated with bsrender written by Kevin Loch, using data from the ESA/Gaia database.
Table 1. OGLE-IV Fields toward the Small Magellanic Cloud
Field

R.A.

Decl.

(J2000)
SMC700
SMC701
SMC702
SMC703
SMC704
SMC705
SMC706
SMC707
SMC708
SMC709
...
Total

h

m

(J2000)
s

00 15 21
00h 14m 03s
00h 11m 02s
00h 05m 33s
00h 28m 58s
00h 28m 34s
00h 26m 26s
00h 22m 01s
00h 17m 23s
00h 10m 13s
...
...

◦

′

′′

−69 26 37
−70◦ 40′ 51′′
−71◦ 54′ 43′′
−73◦ 08′ 19′′
−68◦ 49′ 55′′
−70◦ 03′ 44′′
−71◦ 17′ 37′′
−72◦ 31′ 19′′
−73◦ 45′ 14′′
−74◦ 59′ 06′′
...
...

NEpochs

NEpochs

NStars

NStars

NStars

(2001–2009)

(2010–2020)

(2001–2020)

(2010–2020)

(Total)

0
0
0
0
0
0
0–1377
0–1371
0–1353
0–663
...
...

679
677
674
673
667
668
666
1090
658
654

0.0
0.0
0.0
0.0
0.0
0.0
90.7
336.0
89.7
3.8
...
7431.2

61.8
67.4
79.4
68.6
59.0
68.9
25.9
40.6
84.2
76.4

61.8
67.4
79.4
68.6
59.0
68.9
116.6
376.7
173.9
80.2
...
13611.4

...
...

...
6180.1

Note—The coordinates are given for the epoch J2000. NEpochs is the number of I-band epochs,
separately for OGLE-III (2001–2009) and OGLE-IV (2010–2020) phases of the survey. NStars is the
number of stars (in thousands) detected in the reference image of a given field. This number is not equal
to the number of microlensing source stars that enter the optical depth calculations. We separately
provide the number of stars observed during both OGLE-III and OGLE-IV (that is, from 2001–2020)
and during OGLE-IV only (2010–2020). Columns (6) and (7) may not sum to column (8) due to
rounding. (This table is available in its entirety in machine-readable form.)

## PDF page 4

4

P. Mróz et al.

2, 458, 924), when OGLE operations were halted because of the start of the COVID-19 pandemic. The
survey uses a dedicated 1.3 m Warsaw Telescope located at Las Campanas Observatory, Chile. The telescope is equipped with a mosaic CCD camera consisting
of 32 detectors, each with a resolution of 2048 × 4102
pixels. With a pixel scale of 0.26 arcsec pixel−1 , the
OGLE-IV camera covers the field of view of approximately 1.4 deg2 . Further details about the instrument
can be found in Udalski et al. (2015).
The OGLE-IV project observes an area of approximately 190 deg2 surrounding the SMC. This region is
divided into 135 fields, whose locations are shown in Figure 1. The equatorial coordinates of the center of each
field, along with the number of epochs and the number of
detected stars, are provided in Table 1. Most of the data
were taken in the I-band filter, whose transmission curve
closely resembles that of the standard Cousins photometric system. The number of I-band epochs varies
from 151 to 1090, with a median count of 376. In addition, a smaller number of images were taken through
the V -band filter (from 7 to 321 per field with a median
of 22). The cadence of observations differs depending on
the specific field. Fields covering the SMC center were
observed at a 2–5 day cadence, whereas the outer fields
were observed less frequently, typically every 4–6 days.
The typical seeing ranged from 0.9 to 2.0′′ , with a median seeing of 1.4′′ . Exposure times varied between 150
and 170 s.
We employed the difference image analysis (DIA)
technique (Tomaney & Crotts 1996; Alard & Lupton
1998), as implemented by Woźniak (2000), to extract
photometry. This method provides high-quality measurements, even in the most crowded stellar regions. For
every analyzed field, a reference image is constructed by
stacking several (from 2–10) low-seeing, low-background
individual images. Photometry is performed on difference (subtracted) images, which are generated by subtracting the reference image from the incoming frames.
Our photometric pipeline detects and flags stars that are
identified in the subtracted images. In addition, forced
photometry with fixed centroids is calculated for all stars
detected in the reference images. In total, the analyzed
fields contain about 13.6 million such stars. Please note
that the number of stars that are detected on reference
images is not equal to the number of microlensing source
stars, as discussed in Section 5.
2.2. Combined OGLE-III/OGLE-IV Data
Because our main scientific goal was to search for
long-duration microlensing events, we supplemented the
OGLE-IV light curves with data collected during the

third phase of the survey (OGLE-III; Udalski 2003),
following the methodology detailed in Paper 1. The
OGLE-III data were gathered from June 24, 2001 (JD =
2, 452, 085) to May 2, 2009 (JD = 2, 454, 954). This approach allowed us to extend the OGLE-IV light curves
to nearly 20 yr.
The OGLE-III project used the same Warsaw Telescope as OGLE-IV albeit with a smaller camera that
contained eight 2048 × 4096 detectors. Observations
were taken in the I-band filter, similar to that used
by OGLE-IV, with exposure times of 180 s. Because
the reference images from OGLE-III and OGLE-IV were
slightly different, we could not naively combine the light
curves from both data sets. For instance, some close
pairs of stars could be resolved in the OGLE-III reference images but not in OGLE-IV reference images, and
vice versa. These differences could lead to systematic
shifts between the two data sets. Fortunately, because
the pixel scales of the OGLE-III and OGLE-IV cameras
were identical, we were able to reduce the OGLE-III
images using OGLE-IV reference images using the standard OGLE DIA pipeline by Woźniak (2000). This procedure provided homogeneous light curves for all common stars. As demonstrated in Paper 1, the differences between the mean magnitudes from OGLE-III and
OGLE-IV were consistent with zero (see Figure 2 in
Mróz et al. 2024b).
The OGLE-III project observed an area of 14 deg2 in
the SMC, focusing on the central regions of this galaxy.
This area is marked with yellow lines in Figure 1 and
contains a total of 7.4 million stars (about 55% of all
SMC stars detected in OGLE-IV reference images). The
OGLE-III fields were observed between 583 and 762
times. Table 1 provides more detailed statistics about
the number of stars that have full 2001–2020 light curves
and the total number of available epochs.
A smaller number of 2.1 million stars located in the
central 2.4 deg2 of the SMC were observed during the
second phase of the OGLE survey (OGLE-II; Udalski
et al. 1997a; Wyrzykowski et al. 2010) from 1997–2000.
By combining this data set with the light curves from
OGLE-III and OGLE-IV, we can extend the full data
set to nearly 24,yr. However, the OGLE-II camera had
a larger pixel size of 0.417′′ compared to its successors,
which makes it nearly impossible to extract homogeneous light curves using the methodology developed in
Paper 1. Therefore, we use the OGLE-II data, if available, only to vet the microlensing event candidates detected in the combined OGLE-III/OGLE-IV data set.

2.3. Correction of Error Bars

## PDF page 5

Microlensing Optical Depth toward the SMC
Table 2. Error Bar Correction Coefficients for the I-band
Data
Field

γOGLE-III

εOGLE-III

γOGLE-IV

εOGLE-IV

SMC720.01
SMC720.02
SMC720.03
SMC720.04
SMC720.05
SMC720.06
SMC720.07
SMC720.08
SMC720.09
SMC720.10
...

1.549
1.522
1.531
1.653
1.569
1.522
1.588
1.617
1.388
1.465
...

0.0082
0.0085
0.0086
0.0077
0.0076
0.0078
0.0079
0.0080
0.0069
0.0084
...

1.660
1.500
1.517
1.574
1.506
1.454
1.520
1.536
1.458
1.529
...

0.0056
0.0054
0.0062
0.0057
0.0059
0.0066
0.0063
0.0064
0.0053
0.0054
...

Note—(This table is available in its entirety in
machine-readable form.)

The uncertainties returned by the DIA pipeline do
not accurately reflect the observed scatter in the light
curves of constant stars (e.g., Skowron et al. 2016).
Therefore,√they need to be rescaled using the formula
δmnew = (γδmold )2 + ε2 , where the parameters γ and
ε depend on the field and filter used. We followed the
procedure described by Skowron et al. (2016) to determine the values of these parameters, separately for the
new OGLE-III and OGLE-IV light curves. Our results
are reported in Table 2. For the original OGLE-IV data,
we found the median values of γ = 1.36 and ε = 0.015.
3. SEARCH FOR MICROLENSING EVENTS

For our search for microlensing events in the SMC
data, we employed a methodology very similar to that
developed in Paper 1, with some minor modifications
aimed at maximizing detection efficiency while minimizing contamination from non-microlensing light curves.
For a detailed discussion of the event selection criteria,
we refer readers to Mróz et al. (2024b). The list of all
selection criteria is presented in Table 3.
We began with light curves of 13.6 million stars that
were detected on OGLE-IV reference images. Of these,
7.4 million also had OGLE-III data available. We extracted their light curves as described in Section 2.2.
The uncertainties returned by the DIA pipeline were
corrected as discussed in Section 2.3, and the magnitudes were subsequently converted into flux units.
In the first step, we searched for objects that underwent at least one significant brightening (called a
“bump”) in their light curves. Specifically, we required
that at least five consecutive data points had to be

5

brighter than Fbase + 3σbase , where Fbase is the mean
flux, and σbase is its standard deviation measured outside the magnified section of the light curve. Additionally, we required that the object be detected by the DIA
pipeline on at least three subtracted images during the
bump, its amplitude be at least 0.1 mag, and it show
no significant variability beyond the main brightening.
This initial filtering reduced the number of candidate
events from 13.6 million to 25,973.
Next, we applied a series of selection cuts to eliminate
apparent non-microlensing light curves. We first algorithmically removed the main bump and searched for
any additional brightenings in the data. As microlensing events are expected to be non-repeating, we excluded
objects that displayed more than one bump in their light
curves. We also discarded “blue bumper” stars, which
are defined as those located in the color–magnitude diagram (CMD) region where (V − I)0 ≤ 0.5 and I0 ≤ 20.0
(notably, the magnitude cut differs from that used in Paper 1 to account for the larger SMC distance modulus).
The de-reddened colors and magnitudes were calculated
using the reddening map by Skowron et al. (2021).
In addition to the cuts described in Paper 1, we excluded objects located within 10′ of the globular cluster
47 Tuc, as their photometry was significantly affected
by extreme crowding. We also decided to discard high
proper-motion stars, which displayed significant trends
in their light curves that were picked up by our algorithm as microlensing candidates. To this end, we crossmatched the list of selected candidates with the Gaia
DR3 archive (Gaia Collaboration et al. 2016, 2021b) and
removed any objects with proper motions greater than
10 mas yr−1 . All of these criteria reduced the number of
candidate events to 9614.
In the final step, we fitted a microlensing point-source
point-lens (PSPL) model to the data and evaluated several goodness-of-the-fit statistics. In this model, the flux
is given by the formula
F (t) = F0 [1 + fs (A(t) − 1)],

(1)

where F0 is the baseline flux, fs is the dimensionless
blending parameter, and the magnification can be calculated using the equation
A(t) =

u(t)2 + 2
√
.
u(t) u(t)2 + 4

(2)

Here, u(t)2 = ((t − t0 )/tE )2 + u20 , with t0 being the time
of the maximum magnification, tE the Einstein radius
crossing timescale, and u0 the impact parameter in Einstein radius units.
Out of all analyzed light curves, only five met all
selection cuts. These events constitute the statisti-

## PDF page 6

6

P. Mróz et al.
Table 3. Event Selection Criteria

Cut 0.
Cut 1.

Cut 2.

Cut 3.

Criteria
All stars in the databases
Stars with at least one significant brightening in the light curve
At least five consecutive data points 3σ above the baseline flux (nbump ≥ 5)
Object detected on at least three subtracted images (nDIA ≥ 3)
∑
The total “significance” of the bump (χ3+ = i (Fi − Fbase )/σi ≥ 32)
Amplitude of the bump at least 0.1 mag (∆m ≥ 0.1 mag)
Amplitude of the bump at least 0.4 mag if the bump is longer than 100 days
No significant variability outside the window (χ2out /d.o.f. ≤ 2) if the bump is shorter than 1000 days
Removing false positives
Stars with multiple bumps in the data
“Blue bumpers” ((V − I)0 ≤ 0.5, I0 ≤ 20.0)
Stars in the vicinity of 47 Tuc
High proper-motion stars
Microlensing PSPL model describes the light curve well
Fit converged
χ2 /d.o.f. ≤ 2 (all data points)
χ2tE /d.o.f. ≤ 2 (for |t − t0 | < tE )
χ2bump /d.o.f. ≤ 2 (for data points within the bump)
Microlensing model significantly better than a straight line (χ2line − χ2 ≥ 250χ2 /dof)
t0 within the time range covered by the data
Impact parameter is smaller than 1 (u0 ≤ 1)
Uncertainty on the Einstein timescale (σ(tE )/tE ≤ 1)
Source star brighter than 22 mag (Is ≤ 22 mag)

Number
13,611,366

25,973

9614

5

Table 4. Detected Microlensing Events
Event

R.A. (J2000)
h

m

s

Decl. (J2000)
◦

′

′′

OGLE-SMC-02

00 40 28. 12

−73 44 46. 5

OGLE-SMC-03
OGLE-SMC-04
OGLE-SMC-05
OGLE-SMC-06
OGLE-SMC-07

01h 02m 37.s 51
01h 00m 59.s 33
01h 04m 29.s 29
00h 51m 56.s 62
00h 50m 33.s 66

−73◦ 22′ 26.′′ 0
−73◦ 14′ 17.′′ 1
−72◦ 35′ 14.′′ 9
−73◦ 22′ 18.′′ 1
−73◦ 36′ 27.′′ 3

OGLE-IV ID

Ibase (mag)

(V − I)base (mag)

E(V − I) (mag)

SMC713.01.1243
SMC720.24.1511
SMC726.12.12326
SMC726.13.27861
SMC726.28.35652
SMC720.26.2296
SMC720.19.4610

18.427 ± 0.010

0.953 ± 0.014

0.035+0.026
−0.029

20.642 ± 0.011
18.505 ± 0.010
20.614 ± 0.012
18.205 ± 0.010
18.676 ± 0.010

0.067 ± 0.016
0.971 ± 0.014
0.001 ± 0.017
1.152 ± 0.014
0.771 ± 0.014

0.065+0.048
−0.053
0.060+0.039
−0.048
0.111+0.041
−0.044
0.045+0.065
−0.071
0.048+0.061
−0.070

Note—The table provides the mean observed I-band brightness and V − I color in the baseline. The reddening E(V − I)
toward each event was taken from Skowron et al. (2021).

cal sample that we use for the calculation of the microlensing optical depth, event rate (Section 7), and constraints on compact objects in dark matter (Section 9).
Events OGLE-SMC-03 and OGLE-SMC-04 were previously discovered by Wyrzykowski et al. (2011b) in the
OGLE-III data, while OGLE-SMC-05, OGLE-SMC-06,
and OGLE-SMC-07 are new discoveries. The equatorial
coordinates of all events, along with their mean I-band

magnitudes and (V − I) colors in the baseline, are listed
in Table 4.

## PDF page 7

0.150 ± 0.026
0.169 ± 0.029
0.117 ± 0.052

43.2+6.3
−5.3
41.8+5.7
−5.2
51.5+23.8
−13.8
36.8+5.3
−4.8
59.3+40.9
−20.9
18.6+2.0
−1.6
113.2+33.2
−25.3
214.7+21.0
−16.3
283.2+33.5
−32.3
238.3+18.7
−16.5
20.0+3.0
−2.1
18.7+2.8
−2.3
19.3+2.9
−2.3
17.8+2.7
−2.2
17.3+2.7
−2.2

2, 454, 476.09 ± 0.10

2, 454, 476.12 ± 0.12

2, 454, 476.19 ± 0.11

2, 454, 476.14 ± 0.09

2, 454, 476.20 ± 0.14

2, 452, 611.50 ± 0.17

2, 456, 112.40 ± 1.75

2, 456, 329.15 ± 1.98

2, 456, 366.85 ± 5.98

2, 456, 328.87 ± 4.65

2, 458, 459.05 ± 0.19

2, 458, 459.45 ± 0.20

2, 458, 459.48 ± 0.21

2, 458, 459.43 ± 0.19

2, 458, 459.43 ± 0.18

OGLE-SMC-03

OGLE-SMC-03

OGLE-SMC-03

OGLE-SMC-03

OGLE-SMC-03

OGLE-SMC-04

OGLE-SMC-05

OGLE-SMC-06

OGLE-SMC-06

OGLE-SMC-06

OGLE-SMC-07

OGLE-SMC-07

OGLE-SMC-07

OGLE-SMC-07

OGLE-SMC-07

Note—Is is the observed source I-band magnitude.

−0.375 ± 0.082

−0.376 ± 0.082

0.376 ± 0.084

0.377 ± 0.082

0.341 ± 0.067

−0.728 ± 0.076

0.349 ± 0.076

+3.45 ± 0.65

+2.15 ± 0.37

+3.20 ± 0.58

+1.95 ± 0.33

...

+0.0203 ± 0.0199

−0.0347 ± 0.0057

...

...

0.667 ± 0.098

...

0.159+0.081
−0.052

−1.04 ± 0.60

+2.01 ± 0.27

−0.91 ± 0.56

+1.80 ± 0.23

...

πE,N

0.318 ± 0.051

−0.111 ± 0.056

−0.166 ± 0.029

u0

tE (d)

t0

Event

−0.30 ± 0.15

+0.56 ± 0.36

−0.04 ± 0.20

+0.66 ± 0.37

...

−0.0556 ± 0.0133

+0.0250 ± 0.0100

...

...

...

+0.34 ± 0.27

+0.10 ± 0.15

+0.28 ± 0.23

+0.13 ± 0.13

...

πE,E

Table 5. Best-fit Parameters of Detected Events

18.69 ± 0.33

18.69 ± 0.33

18.69 ± 0.34

18.68 ± 0.33

18.84 ± 0.30

18.22 ± 0.21

19.33 ± 0.27

18.45 ± 0.27

20.94 ± 0.49

18.66 ± 0.24

20.70+0.69
−0.49

20.20 ± 0.21

20.63+0.60
−0.44

20.18 ± 0.21

20.33 ± 0.20

Is (mag)

0.99 ± 0.29

0.99 ± 0.29

0.99 ± 0.29

0.99 ± 0.28

0.86 ± 0.22

1.01+0.45
−0.49
1.51+0.30
−0.28
0.95+0.48
−0.52
0.87+0.19
−0.17
0.75+0.43
−0.26
0.80+0.21
−0.18
0.35+0.10
−0.07
0.99+0.14
−0.17

1.54+0.31
−0.28

1.33+0.27
−0.23

fs

1380.0/1401

1380.2/1401

1380.0/1401

1380.2/1401

1403.5/1403

1423.7/1403

1411.6/1403

1441.7/1405

1226.1/1191

1395.4/1383

1360.8/1371

1355.1/1371

1360.8/1371

1355.4/1371

1364.0/1371

χ2 /d.o.f.

Microlensing Optical Depth toward the SMC
7

## PDF page 8

16
8000

9000

Magnitude

7000

5000

6000

7000

4000

8000

9000

18.0
18.5
0.1
0.0
0.1

2500

2550

17.75
18.00
18.25
2000 3000 4000
17.6 OGLE-SMC-06
17.8

2600
2650
HJD - 2450000

5000

6000

2700

7000

8000

2750

9000

18.0
18.2
0.1
0.0
0.1

Magnitude

3600
3800
HJD - 2450000

Magnitude

3400

5600 5800 6000 6200 6400 6600 6800 7000 7200
HJD - 2450000

Residuals

3200

Residuals

18

Magnitude

Residuals
Magnitude
Magnitude
Residuals

6000

5000

6000

7000

8000

4450
4500
HJD - 2450000

4550

5000

7000

9000

20
21
0.5
0.0
0.5

4350

4400

4600

20.0
22.5
2000 3000 4000
19 OGLE-SMC-05

6000

8000

9000

20
21
0.5
0.0
0.5

5800 5900 6000 6100 6200 6300 6400 6500
HJD - 2450000

17.5
18.0
18.5
2000 3000 4000
OGLE-SMC-07

Magnitude

17.5
18.0
18.5
2000 3000 4000
OGLE-SMC-04
17.5

5000

20
22
2000 3000 4000
OGLE-SMC-03
19

18.0

Residuals

Magnitude

0.2
0.0
0.2

Magnitude

17

Residuals

18
2000 3000 4000
16 OGLE-SMC-02

Magnitude

P. Mróz et al.

Magnitude

Magnitude

8

0.1
0.0
0.1

5000

6000

7000

8000

9000

18.5

8350

8400

8450
8500
HJD - 2450000

8550

8600

Figure 2. I-band light curves of detected microlensing events. The solid blue line shows the best-fit microlensing model. The
dotted lines for OGLE-SMC-06 and OGLE-SMC-07 present the best-fit PSPL models without microlensing parallax.

## PDF page 9

Microlensing Optical Depth toward the SMC
For completeness, we visually inspected the light
curves of all 25,973 objects selected in the first step
of our criteria. We found only one additional event,
OGLE-SMC-02, which was included in the sample of
Wyrzykowski et al. (2011b). This event is a known
binary-lens event (Dong et al. 2007), whose light curve
significantly differs from that of a simple PSPL model.
Hence, it did not satisfy all of our selection criteria. In
addition, we checked the archival OGLE-II data (1997–
2000), which were available for all events except OGLESMC-03 and OGLE-SMC-04. We also retrieved the
archival MACHO light curves (1992–1999) for all events
except OGLE-SMC-02 and OGLE-SMC-07. These additional data did not reveal any suspicious variability,
which is consistent with the microlensing classification.
4. DETECTED EVENTS

Our final sample of microlensing events in the SMC
consists of five objects. We modeled their light curves
using the Markov Chain Monte Carlo (MCMC) techniques to refine the best-fit PSPL parameters and estimate their uncertainties. We used the same modeling
techniques as described in Paper 1. The results are summarized in Table 5, where we provide the median values
and the 68% confidence intervals of the marginalized
posterior distributions for all parameters. Note that
OGLE-SMC-02 is excluded from this table because it
is a binary-lens event that does not enter our statistical
sample. The parameters of this event were provided by
Dong et al. (2007). The light curves of analyzed events
and the best-fit models are presented in Figure 2.
In addition to PSPL models, we also included the annual microlensing parallax effect (Gould 2004) in the
fits. We found that the parallax is reliably measured for
OGLE-SMC-06, for which we identified two possible degenerate solutions. These models, differing by the sign
of u0 , are preferred over the standard PSPL model by
∆χ2 = 30.1 and ∆χ2 = 18.0 for the u0 > 0 and u0 < 0
solutions, respectively. This event, with an estimated
+18.7
timescale of 283.2+33.5
−32.3 days (u0 > 0) or 238.3−16.5 days
(u0 < 0), is the longest-timescale event identified toward
the SMC to date. The long timescale of this event, along
with a small value of the microlensing parallax, indicates
that both the lens and the source are most likely located
in the SMC.
A formally statistically significant signal of
the microlensing parallax was also identified for
OGLE-SMC-07. The fit improved by ∆χ2 = 23.5 when
including the parallax. This improvement mainly originates from the data points collected prior to the main
event, in the time range 2, 458, 284 < HJD < 2, 458, 411,
during which the event was magnified by ≈ 0.05 mag

9

compared to the mean baseline brightness. The parallax is also marginally (∆χ2 = 8.6) detected in the light
curve of OGLE-SMC-03, as was originally noticed by
Wyrzykowski et al. (2011b). We identified four degenerate solutions for both events—two differing by the sign
of u0 (Smith et al. 2003) and two resulting from the
jerk-parallax degeneracy (Gould 2004). The parameters
of both events (short timescales and large microlensing
parallaxes) indicate that the lenses are located in the
foreground Milky Way disk.
For three events, the V -band photometry collected
during the magnified portion of the light curve was available. In these cases, we used model-independent regression to measure the color of the source star. We found
the following values: (V − I)s = 0.920 ± 0.003 mag for
OGLE-SMC-02, (V −I)s = 0.078±0.017 mag for OGLESMC-03, and (V − I)s = 1.214 ± 0.009 mag for OGLESMC-06. These values are quite similar to the baseline
colors (see Table 4), which confirms that the lens does
not substantially contribute to the event’s brightness or
that the color of the lens is similar to that of the source
star.
The positions of all detected events in the de-reddened
CMD are presented as blue dots in Figure 3. The background CMD shows the locations of stars in the field
SMC726.28, and blue dots mark the positions of the
discovered events in the baseline:
I0 = Ibase − 1.217E(V − I),
(V − I)0 = (V − I)base − E(V − I),

(3)

where we adopted the I-band extinction to reddening
ratio of AI /E(V −I) = 1.217 from Schlafly & Finkbeiner
(2011). The reddening toward each event was estimated
using optical reddening maps by Skowron et al. (2021).
Four of the detected events have sources situated close
to the red clump in the CMD, while the positions of the
other two events indicate main-sequence sources.
Among the newly identified events, the classification
of OGLE-SMC-05 as a microlensing event appears to be
the least certain. Although the data can be reasonably
well fitted with the PSPL model, a rising portion of the
light curve is missing. This raises the possibility that
the object might be a supernova. Additionally, as no
V -band observations were secured during the magnified
portion of the light curve, we cannot confirm whether
it is achromatic, as would be expected for microlensing
events. On a positive note, the source looks stellar in
the reference image, and there are no galaxies located
near this event.
4.1. Comparison with Previous Searches for
Microlensing Events toward the SMC

## PDF page 10

10

P. Mróz et al.

16
17

I0

18
07

19

02
04

06

20
05 03

21
22 0.5

0.0

0.5
(V I)0

1.0

1.5

Figure 3. De-reddened color–magnitude diagram of the
field SMC726.28. Blue circles mark the positions of the detected microlensing events in the baseline.

The analyzed data set, by construction, contains the
majority of OGLE-III light curves that were previously
studied by Wyrzykowski et al. (2011b), who reported the
discovery of three microlensing events. We were able to
successfully recover two of these events (OGLE-SMC03 and OGLE-SMC-04). Their best-fit parameters are
very similar to those measured by Wyrzykowski et al.
(2011b) (Table 5). However, one event (OGLE-SMC-02)
was not selected by our automated pipeline because it
did not pass all selection cuts, in particular those related
to the PSPL fit quality. That is not surprising because
this event is known to be a weak (non-caustic-crossing)
binary-lens event whose light curve significantly deviates
from a simple PSPL model (Dong et al. 2007). For completeness, we include the light curve of OGLE-SMC-02
in the upper-left panel of Figure 2.
We also examined the light curves of other SMC microlensing candidates that have been reported in the
literature. Thanks to the extended time span of observations, we were able to search for additional outbursts or variability that could disprove the microlensing
classification. For example, Wyrzykowski et al. (2010)

reported the discovery of one microlensing candidate
(called OGLE-SMC-01) in the OGLE-II data. This
event was considered to be “rather weak” because of a
sparsely sampled light curve and an unusually blue color
in the baseline, which placed the event in a relatively
empty region of the CMD between the main sequence
and the red giant branch. Although Wyrzykowski et al.
(2010) noted that the star did not show any additional outbursts in the OGLE-III data (2001–2009), the
OGLE-IV data reveal a second outburst occurring between January and November 2016, demonstrating that
this object is not a microlensing event.
Tisserand et al. (2007) reported the detection of
two microlensing candidates in the SMC. The first
event, EROS2-SMC-1 (a.k.a. MACHO-97-SMC-1), was
discovered by Alcock et al. (1997a) and PalanqueDelabrouille et al. (1998). The full OGLE light curve
of this event does not reveal any additional outbursts.
However, the source star exhibits sinusoidal variability
with a period of 5.12505(3) days. This derived period
is close to those measured by Alcock et al. (1997a),
Udalski et al. (1997b), and Palanque-Delabrouille et al.
(1998). The source is likely a binary system with an
orbital period twice as long as the photometric period.
Another candidate reported by Tisserand et al. (2007),
EROS2-SMC-5, underwent a second outburst in November 2017, which is inconsistent with a microlensing interpretation. Additionally, the caustic-crossing event
MACHO-98-SMC-1 (Alcock et al. 1999; Afonso et al.
2000) is located in a gap between the CCD detectors of
the OGLE-IV camera, and therefore, no recent data are
available for this event.
5. NUMBER OF SOURCE STARS

The number of stars that are detected on OGLE reference images differs from the number of source stars
that might give rise to microlensing events. This difference arises for two main reasons. First, the resolution
of ground-based images is limited by seeing, which can
cause two or more nearby stars to appear blended and
unresolved. Second, the probability that nearby foreground stars are microlensed is virtually zero; such stars
therefore do not significantly contribute to the observed
number of microlensing events.
We used the methods developed in Paper 1 to estimate
the number of possible source stars. In short, we first
compared the surface density of stars brighter than a
certain limiting magnitude on the OGLE reference images (ΣOGLE ) with the corresponding surface density
ΣHST derived from deep Hubble Space Telescope (HST)
observations of the same fields. We used the HST images
compiled and reduced by Holtzman et al. (2006). These

## PDF page 11

log Σforeground = ξ + η(|b| − 30◦ )

(4)

to stellar surface densities calculated in the outer SMC
fields (those with b < −52◦ or b > −37.5◦ ). Here, b is the
Galactic latitude, and ξ and η are numerical coefficients.
We obtained ξ = 0.783 ± 0.049, η = −0.0071 ± 0.0024
for stars brighter than I = 21 mag; ξ = 0.805 ± 0.074,
η = −0.0051 ± 0.0036 for stars brighter than I = 21.5
mag; ξ = 0.823 ± 0.081, η = −0.0047 ± 0.0040 for stars
brighter than I = 22 mag.
To calculate the number of source stars, we multiplied the number of stars detected on the OGLE reference images by the correction factor and subtracted the
estimated number of foreground stars. The results are
summarized in Table 6, which presents the total number
of stars (Ntot ) and the estimated number of SMC source
stars (Ncorr ) that are brighter than I = 21, I = 21.5, and
I = 22 mag in each subfield. Overall, we estimate that
OGLE-IV monitored about 6.32 ± 0.19 million source
stars brighter than I = 21 mag, 9.69±0.68 million source
stars brighter than I = 21.5 mag, and 12.4 ± 1.4 million
source stars brighter than I = 22 mag. The error bars
represent the accuracy of determination of star counts,
which we adopted from Paper 1. The surface density
of source stars brighter than I = 21 mag is presented in
Figure 4.
We compared our results with the number of sources
reported by Wyrzykowski et al. (2011b), who found
about 5.97 million source stars brighter than I = 21 mag
in the OGLE-III SMC fields. We estimate that about
91.6% of them (that is, about 5.47 million) should also
be detected in the OGLE-IV reference images, the re-

100

10

1
Figure 4. Surface density of source stars brighter than I =
21 mag in the analyzed fields. The black polygons mark the
area observed by OGLE-III. The map is presented in an
equal-area Hammer projection centered on R.A. = 0h 51m ,
Decl. = −73.1◦ .

1

Detection efficiency

HST images served as a “ground truth.” The data set
created by Holtzman et al. (2006) includes nine “priority
1” fields in the SMC—those with HST observations in
the F555W and F814W filters and exposure times longer
than 500 s. Two of these fields contain stellar clusters;
for the remaining seven, we calculated the correction
factor (CF), defined as CF = ΣHST /ΣOGLE , for stars
brighter than I = 21, I = 21.5, and I = 22 mag.
We found that these correction factors were very similar to those derived in Paper 1 for the LMC. This conclusion is further supported by analyses of simulations carried out by Wyrzykowski et al. (2011a) and Wyrzykowski
et al. (2011b), which show that the correction factors
for the LMC and SMC are consistent within 5%. Because the number of SMC fields included in the Holtzman et al. (2006) database is much smaller than the
number of LMC fields (64), we adopted the correction
factors derived in Paper 1.
We then estimated the surface density of foreground
stars by fitting the following formula:

Surface density of stars (arcmin )

11

Microlensing Optical Depth toward the SMC

SMC726
SMC734

0.1
Limiting magnitude:
I = 21 mag
I = 21.5 mag
I = 22 mag
0.011

10

100

1000

Einstein timescale tE (days)

10000

Figure 5. Example detection efficiency curves for representative fields SMC726 and SMC734. The solid, dashed, and
dash–dotted lines represent detection efficiencies averaged for
sources brighter than I = 21, I = 21.5, and I = 22 mag, respectively.

maining 8.4% are located in the gaps between the CCD
detectors or between the OGLE-IV fields. If we restrict
our sample to stars brighter than I = 21 mag and to
those located in the OGLE-III fields, we found a total
of 5.47 million stars (5.16 million after removing foreground contamination), in excellent agreement with the
results presented by Wyrzykowski et al. (2011b).

## PDF page 12

12

P. Mróz et al.
Table 6. Number of Microlensing Source Stars Observed in OGLE-IV Fields
Field
SMC700.01
SMC700.02
SMC700.03
SMC700.04
SMC700.05
SMC700.06
SMC700.07
SMC700.08
SMC700.09
SMC700.10
...
Total (million)

R.A. (deg)

Decl. (deg)

21 mag
Ntotal

21 mag
Ncorr

21.5 mag
Ntotal

21.5 mag
Ncorr

22 mag
Ntotal

22 mag
Ncorr

5.1554
4.7161
4.2768
3.8376
3.3983
2.9591
2.5198
5.5946
5.1554
4.7161
...
...

–69.9144
–69.9144
–69.9144
–69.9144
–69.9144
–69.9144
–69.9144
–69.5930
–69.5930
–69.5930
...
...

1188
1168
1229
1231
1142
1233
952
1419
1278
1150
...
9.606

413
393
453
455
365
456
174
649
507
379
...
6.316

1697
1606
1640
1732
1571
1637
1271
1881
1824
1593
...
13.364

817
725
758
850
688
754
387
1003
946
714
...
9.689

1895
1750
1812
1895
1699
1770
1390
2033
2066
1700
...
16.230

963
817
878
961
764
834
454
1103
1136
770
...
12.351

Note—(This table is available in its entirety in machine-readable form.)

6. DETECTION EFFICIENCY

We used methods developed in Paper 1 to calculate
the event detection efficiency as a function of the event
timescale. A detailed description of our calculations can
be found in Paper 1. In brief, we created synthetic
light curves of microlensing events by injecting artificial signals into the light curves of randomly selected
stars from the database. This approach allows us to preserve the sampling of the original light curves, as well
as the variability and noise present in the actual data,
which would be challenging to simulate otherwise. We
applied exactly the same selection criteria outlined in
Section 3 to the simulated light curves and ultimately
measured the fraction of synthetic events that satisfied
all selection criteria. The resulting detection efficiency
was subsequently lowered by 10% to account for possible binary-lens events (Wyrzykowski et al. 2011b; Mróz
et al. 2024b) that may be missed by our automated detection pipeline.
The parameters of events were drawn from physically
motivated distributions. The time of the maximum
was sampled from a uniform distribution within the
time ranges 2, 452, 000 ≤ t0 ≤ 2, 459, 000 (for objects
observed during both OGLE-III and OGLE-IV) and
2, 455, 000 ≤ t0 ≤ 2, 459, 000 (for stars observed during
OGLE-IV only). The impact parameters were drawn
from a uniform distribution from the range 0 ≤ u0 ≤ 1,
while the Einstein timescales were drawn from a loguniform distribution from the range 1 ≤ tE ≤ 104 days.
For the blending parameter fs , we used an empirical distribution created by matching stars detected on OGLE
reference images with those detected by HST.

We simulated 10,000 light curves per detector (totaling 320,000 light curves per field) and calculated the
detection efficiency across 25 identical bins in log tE .
For each field, we calculated detection efficiencies averaged over sources brighter than I = 21, I = 21.5, and
I = 22 mag. Figure 5 shows example detection efficiency
curves for representative fields SMC726 (observed during both OGLE-III and OGLE-IV) and SMC734 (observed during OGLE-IV only).
7. OPTICAL DEPTH AND EVENT RATE

Given the statistical sample of five microlensing events
toward the SMC (Section 3), event detection efficiency
ε(tE ) calculated in Section 6, and the total number of
observed source stars Ns (Section 5), we can compute the
microlensing optical depth τ and event rate Γ using the
following equations:
π ∑ 1 tE,i
τ=
,
2Ns i ∆Ti ε(tE,i )
(5)
1 ∑ 1
1
Γ=
,
Ns i ∆Ti ε(tE,i )
where ∆T is the duration of observations. For fields
observed during both OGLE-III and OGLE-IV surveys,
we use ∆T = 7000 days, while for field observed only
during OGLE-IV, we use ∆T = 4000 days. To account
for uncertainties on the event timescale, we replace the
terms tE,i /ε(tE,i ) and 1/ε(tE,i ) with their means calculated from the posterior distribution of tE (see Paper 1
for more details).
For our calculations, we use the five events that
met all selection criteria outlined in Section 3, alongside the number of sources brighter than I = 22 mag

## PDF page 13

Microlensing Optical Depth toward the SMC
(Ns = (12.4 ± 1.4) × 106 ) and the detection efficiencies calculated for sources brighter than this limit. The
total microlensing optical depth toward the OGLE-IV
SMC fields is found to be τ = (0.32 ± 0.18) × 10−7 ,
while the event rate is determined to be Γ = (1.18 ±
0.57) × 10−7 yr−1 star−1 . The uncertainties of these
quantities were calculated using methods proposed by
Han & Gould (1995) and Mróz et al. (2019a). These
error bars reflect only the uncertainties caused by the
small number of events and by the uncertainties in Einstein timescales. There is an additional source of error
(approximately 11%) related to the accuracy of measuring the number of source stars. The contribution of each
event to the total optical depth and event rate is detailed
in Table 7.
8. EXPECTED NUMBER OF EVENTS FROM

then calculate its mean value. To speed up the calculations, we change from the variable M to log M . All
integrals are evaluated with precision better than 1%.
As a byproduct of the Monte Carlo integration, we
also evaluate the expected event timescale distribution
dΓ/d log tE (where tE = θE /µ). The total number of
expected events in a given field can be found by
∫
dΓ
Nexp = Ns ∆T
ε(tE )d log tE ,
(8)
d log tE
where Ns is the number of source stars, ∆T is the duration of the experiment (∆T = 7000 days or ∆T = 4000
days, depending on whether the field was observed during OGLE-III, see Section 7), and ε(tE ) is the event
detection efficiency measured in that field.
8.1. SMC Self-Lensing Models

STELLAR POPULATIONS
In this section, we present simple models of microlensing by stellar populations (stars, brown dwarfs, and stellar remnants) in the SMC and the foreground Milky Way
disk, and demonstrate that they can explain the number
and timescales of observed microlensing events toward
the SMC. The differential event rate toward a source
star at a distance of Ds is given by the formula
d4 Γ
= 2θE µDl2 ν(Dl )f (µ)g(M ),
dDl dM d2 µ

13

(6)

which was first introduced by Batista et al. (2011). Here,
M is the mass of the lens, f (µ) is the 2D probability
function for a given source–lens relative proper motion
µ, θE is the angular Einstein radius, ν(Dl ) is the number
density of lenses at a given distance Dl , and g(M ) is the
mass function of lenses. The total event rate in a given
direction can be expressed as the following integral:
∫∞
∫D
4
ρ(Ds )Ds2−2β dDs 0 s dDlddMΓd2 µ dDl dM d2 µ
0
Γ=
,
∫∞
ρ(Ds )Ds2−2β dDs
0
(7)
where ρ(Ds ) is the density of sources, and the coefficient
β quantifies how the number of observed sources changes
with their distance (Kiraga & Paczyński 1994). It is
generally assumed that 0 ≤ β ≤ 1. Here, we adopt β = 0
as a fiducial value, but we demonstrate below that the
results weakly depend on the choice of this parameter.
The integrals in Equation (7) are evaluated numerically using the Monte Carlo integration technique. For
example, to calculate the multidimensional integral in
the numerator of Equation (7), we draw a random sample of 108 points from a 5D cube Dl,min ≤ Dl ≤ Dl,max ,
Ds,min ≤ Ds ≤ Ds,max , Mmin ≤ M ≤ Mmax , µmin ≤
µx,y ≤ µmax , evaluate the integrand at each point, and

We analyze two SMC self-lensing models. The first
one is based on the model proposed by Calchi Novati
et al. (2013), in which the total stellar mass (within 5 kpc
of the SMC center) is taken to be M∗ = 1.0 × 109 M⊙
(Bekki & Chiba 2009). However, this quantity is by no
means well determined, and Calchi Novati et al. (2013)
argued that M∗ is known with an accuracy of up to a
factor of 2. For example, McConnachie (2012) reported
M∗ = 4.6 × 108 M⊙ . Because the derived microlensing
event rate is directly proportional to the total stellar
mass, the former quantity is also accurate up to a factor
of 2.
The model of stellar populations comprises two components, the old and young stellar populations, whose
mass ratio is assumed to be 3:2 (Bekki & Chiba 2009).
The young stellar population is approximated with a
3D Gaussian profile with length scales of 0.8, 3.5, and
1.3 kpc. On the other hand, the young population is described using the Gaussian profile along the line of sight
(length scale of 2.1 kpc) and a smoother exponential profile in the plane of the sky (with length scales of 0.8 and
1.2 kpc). Following Calchi Novati et al. (2013), we adopt
the coordinates of the SMC center as reported by Gonidakis et al. (2009) (α = 0h 51m , δ = −73.1◦ , J2000),
and the SMC distance of 61.5 kpc. Graczyk et al. (2020)
recently reported a slightly greater geometric distance to
the SMC center of 62.44 ± 0.47 kpc, but we found that
the choice of this quantity has a negligible effect on our
results. The inclination and position angles of the reference frames of the young and old stellar populations
are taken from Calchi Novati et al. (2013).
An alternative self-lensing model is based on the
methodology proposed by Mróz & Poleski (2018). In
this approach, the spatial distribution of both young and
old stellar populations is approximated using a Gaus-

## PDF page 14

14

P. Mróz et al.
Table 7. Microlensing Optical Depth and Event Rate Toward the LMC
Event

⟨ε(tE )⟩

⟨1/ε(tE )⟩

⟨tE /ε(tE )⟩
(days)

OGLE-SMC-03
OGLE-SMC-04
OGLE-SMC-05
OGLE-SMC-06
OGLE-SMC-07
Total:

0.1848
0.1205
0.2635
0.3599
0.1336
...

5.430
8.379
3.827
2.783
7.593
...

sian mixture model, in which the total density is represented as a sum of 3D Gaussians with different weights.
That enables us to more accurately model the irregular shape of this galaxy. We used the scikit-learn
package (Pedregosa et al. 2011) to fit 32 Gaussian components to the 3D distributions of classical Cepheids
(Jacyszyn-Dobrzeniecka et al. 2016) and RR Lyrae stars
(Jacyszyn-Dobrzeniecka et al. 2017) in the SMC. These
stars are intended to represent the young and old stellar
populations, respectively. The SMC center, as adopted
by Jacyszyn-Dobrzeniecka et al. (2016) and JacyszynDobrzeniecka et al. (2017), has equatorial coordinates
of α = 1h 05m , δ = −72◦ 25.2′ (J2000). We assume a
total stellar mass of M∗ = 1.0 × 109 M⊙ , with a mass
ratio of old to young stellar population set as 3:2.
The contours of the microlensing optical depth in both
models are presented in Figure 6. The Calchi Novati
et al. (2013) model has a peak value of 1.3 × 10−7 ,
whereas the Gaussian mixture model (Mróz & Poleski
2018) predicts a higher maximal value of 1.9×10−7 . The
optical depth contours in the latter model are not symmetric, and reflect the irregular distribution of classical
Cepheids in the SMC.
For both stellar distribution models, we use the empirical model of the SMC kinematics that was derived using
the Gaia DR3 data (see the Appendix A). We assume
that the mass function of lenses is identical to that measured by Kroupa (2001). For the evaluation of integrals
in Equation (7), we adopt Dl,min = Ds,min = 48 kpc,
Dl,max = Ds,max = 76 kpc, µmin = −0.5 mas yr−1 ,
µmax = 0.5 mas yr−1 , Mmin = 0.01 M⊙ , and Mmax =
10 M⊙ . The event rate was evaluated at the center of
each field (Table 2). For four central fields (SMC719,
SMC720, SMC725, and SMC726), the integrals in Equation (7) were evaluated at the centers of all 32 subfields
(that is, separately for each CCD detector), and then
averaged using the expected number of sources (denominator in Equation (7)) as a weight.

235.76
156.17
439.51
787.51
153.36
...

τ
−7

(10

Γ
(10

)

0.0428
0.0284
0.0799
0.1431
0.0279
0.32 ± 0.18

−7

yr−1 )

0.2294
0.3540
0.1617
0.1176
0.3208
1.18 ± 0.57

8.2. Milky Way Disk
We consider two possible Milky Way disk models (Han
& Gould 2003; Cautun et al. 2020), identical to those
used in Paper 2 for calculating the expected number of
microlensing events toward the LMC. However, because
the SMC center (b = −44◦ ) is located at higher Galactic
latitude than the LMC center (b = −33◦ ), the expected
event rate from foreground Milky Way lenses is smaller
by ≈ 30%. Both Milky Way disk models are composed
of two stellar populations (thin and thick disk) that are
described by the double exponential profiles:
(
)
(
)
R
|z|
ρ(R, z) = ρ0 exp −
exp −
,
(9)
hR
hz
where R is the Galactocentric distance, z is the distance
from the Milky Way plane, and hR and hz are the radial
scale length and scale height, respectively. The model
parameters are shown in Table 8. We assume that stars
in the disk are moving with the velocity given by the
Milky Way rotation curve (Section 9) with the dispersion of 30 km s−1 , and their mass function follows that
of Kroupa (2001).
For the numerical calculation of the event rate (Equation (7)) we use the following limits Ds,min = 48 kpc,
Ds,max = 76 kpc, Dl,min = 0.01 kpc, Dl,max = 10 kpc,
µmin = −200 mas yr−1 , µmax = 200 mas yr−1 , Mmin =
0.01 M⊙ , and Mmax = 10 M⊙ .
8.3. Comparison with Observations
Table 9 presents the expected number of microlensing events toward the SMC with sources brighter than
I = 22 mag, separately for β = 0 and β = 1. (Recall
that we assume that the number of observable sources
scales as ρ(Ds )Ds2−2β ). For self-lensing models, we find
that those with β = 0 predict 6–11% more events than
those with β = 1. In contrast, the expected number of
events with lenses located in the Milky Way disk does
not significantly depend on the choice of β.

## PDF page 15

15

Microlensing Optical Depth toward the SMC

1h30m

Calchi Novati et al. (2013) model

1h00m

1h30m

Mróz & Poleski (2018) model
70

1.8

1h00m

1.6

70

Microlensing optical depth (10 7)

1.4

0.5

1.2

0.5

1.0
0h30m

0h30m
1.0

0.8

1.6

1.0

0.6
0.4
0.2

75

75

0.0

Figure 6. Contours of the microlensing optical depth for two self-lensing SMC models: Calchi Novati et al. (2013) (left panel)
and Mróz & Poleski (2018) (right). The filled circles indicate the positions of five microlensing events that are included in the
statistical sample analyzed in this paper, while the empty circles represent other known microlensing events.
Table 8. Milky Way Disk Models

Thin disk
hR (kpc)
hz (kpc)
ρ0 (M⊙ pc−3 )
Thick disk
hR (kpc)
hz (kpc)
ρ0 (M⊙ pc−3 )

Table 9. Expected Number of Events

Han & Gould 2003

Cautun et al. 2020

Model

β=0

β=1

2.75
0.156
0.6623

2.63
0.30
1.2183

SMC self-lensing (Calchi Novati et al. 2013)
SMC self-lensing (Mróz & Poleski 2018)
Milky Way disk (Cautun et al. 2020)
Milky Way disk (Han & Gould 2003)

6.7
7.3
3.3
1.6

6.3
6.6
3.3
1.6

2.75
0.439
0.4077

3.80
0.90
0.0561

SMC and the Milky Way disk:
∑ dΓi
dNobs
=
εi (tE )Ns,i ∆Ti ,
d log tE
d log tE
i

Depending on the model selected, we expect 6.7–7.3
self-lensing events and 1.6–3.3 events with Milky Way
lenses. This should be compared to the total of five
events included in our statistical sample (Section 3). For
example, the Poisson probability of observing five events
when more than 8.3 events are expected is just 0.165.
The expected number of events is highly sensitive to the
total stellar mass of the SMC, which is not precisely
known. If we adopt the mass of M∗ = 4.6 × 108 M⊙
(McConnachie 2012), then the number of expected selflensing events is scaled down to 3.1–3.4 (β = 0). Then,
the total number of expected events is 4.7–6.7, in better
agreement with the observed value.
Figure 7 shows the expected distributions of observed
event timescales from known stellar populations in the

(10)

where the summation is performed over all observed
fields, Ns,i is the number of source stars brighter than
I = 22 mag in a given field, and ∆Ti is the duration
of its observations. Self-lensing events are expected to
have relatively long timescales, with the average Einstein timescale being ⟨tE ⟩ ≈ 110 days, primarily because
of low relative lens–source proper motions. In contrast,
events with Milky Way lenses tend to have much shorter
timescales due to higher relative proper motions, leading
to an average of ⟨tE ⟩ ≈ 30 days.
The comparison between the observed cumulative distribution of event timescales and the predictions from
our models is presented in Figure 8. The expected
distributions match the observations reasonably well.
To quantify that, we performed a Kolmogorov–Smirnov
test, resulting in p-values of 0.957 and 0.965 for the mod-

## PDF page 16

16

P. Mróz et al.

els including Han & Gould (2003) and Cautun et al.
(2020) Milky Way disk models, respectively (for β = 0
and the Calchi Novati et al. (2013) SMC model). We
found similar p-values for models with β = 1 and those
calculated using the Mróz & Poleski (2018) approach.
The results of these tests confirm that there are not any
statistically significant deviations between the observed
and expected timescales.
9. LIMITS ON PRIMORDIAL BLACK HOLES IN

DARK MATTER
The results presented in the previous section indicate
that all microlensing events detected by OGLE in the
SMC direction can be easily explained by the known
stellar populations located either within the SMC or in
the foreground Milky Way disk. Thus, there is no need
to invoke compact objects in the Milky Way dark matter
halo to explain them.
We use the same methodology as described in Paper 2
to infer upper limits on the abundance of PBHs in dark
matter. We quantify this by introducing the parameter
f = MPBH /MDM , where MDM is the total mass of the
dark matter halo (inferred from rotation curve measurements), and MPBH is the total mass of PBHs within it.
We note that these limits must apply not only to PBHs
but also any other types of compact objects (dark matter subhalos, boson stars, quark nuggets; e.g., Croon
et al. 2020).
The limits are calculated under the assumption of a
delta-function mass function of PBH, meaning we assume all PBHs have the identical mass M . While some
PBH formation models predict more complex and extended PBH mass functions, our results are not highly
sensitive to the shape of the mass function as long as
most PBHs fall within the mass range probed by microlensing (as discussed in Paper 2). In the case of extended mass functions, the limits depend on the choice
of the specific model. Therefore, for simplicity, we stick
to a delta-function PBH mass function, as we cannot
analyze all possible PBH models. Nonetheless, we publish our detection efficiencies and other supporting data,
allowing any compelling PBH model that predicts an extended mass function to be independently tested.
We assume that the distribution of PBHs within the
dark matter halo can be described by the contracted
halo model of Cautun et al. (2020). This model was
fitted to the Milky Way’s rotation curve, which was
inferred from the Gaia DR2 data (Eilers et al. 2019)
and other sources. For the PBHs velocities, we use a
Maxwellian distribution with the standard
√ deviation of
velocities in one direction set to V0 (R)/ 2, where V0 (R)
is the Milky Way rotation curve predicted by the model.

We neglect dark matter located in the SMC halo, as its
mass (about 6.5 × 109 M⊙ ; Bekki & Stanimirović 2009)
is significantly smaller than that of the Milky Way halo.
The expected number of microlensing events in a given
field was calculated using Equations (7) and (8), assuming β = 0 and employing the model of Calchi Novati
et al. (2013) for the distribution of source stars.
Figure 9 shows the total expected number of microlensing events, assuming that the entire Milky Way
dark matter halo consists of compact objects of identical
mass M . We expect the largest number of events (approximately 233) for M = 0.013 M⊙ . We should have
detected about 103 events if the Milky Way’s entire dark
matter halo was made of 1 M⊙ PBHs, 47 events—10 M⊙ ,
and 18 events—100 M⊙ . That should be compared to
five events in our statistical sample (Section 3).
We calculated the 95% upper limits on f using the
same methodology as in Paper 2. We present two types
of limits. For the strict limits, we assumed that all five
microlensing events in our statistical sample are due to
known stellar populations in the SMC or in the Milky
Way disk. These limits are marked with a solid red line
in Figure 10. When we relax this assumption and allow
for a possibility of a PBH origin for these microlensing events, the inferred limits become slightly weaker.
They are shown by red dashed and dotted lines in Figure 10. The relaxed limits slightly depend on the choice
of the Milky Way disk or the SMC model. In Figure 10
we present two example results for the Han & Gould
(2003) (dashed line) and Cautun et al. (2020) (dotted
line) Milky Way disk models.
The strict limits reach f = 1.3% for M = 0.013 M⊙
for which we expect the largest number of microlensing
events. We find that less than f = 2.9% of dark matter
may be composed of compact objects of 1 M⊙ , less than
f = 6.4% for 10 M⊙ , less than f = 16% for 100 M⊙ .
The difference between strict and relaxed limits (for the
Han & Gould (2003) Milky Way disk model) is largest
for log M = −0.7 and amounts to 0.24 dex (that is, the
relaxed limits are a factor of 1.8 weaker for that mass).
10. DISCUSSION AND CONCLUSIONS

10.1. Optical Depth toward the SMC
The only previously published measurements of the
microlensing optical depth toward the SMC were by
Wyrzykowski et al. (2010) and Wyrzykowski et al.
(2011b), based on the OGLE-II and OGLE-III data,
respectively. Wyrzykowski et al. (2010) measured the
optical depth of τ = (1.15 ± 1.15) × 10−7 based on just
one event candidate, OGLE-SMC-01. However, as we
found that this object is a variable star rather than
a microlensing event, this measurement should be re-

## PDF page 17

17

Microlensing Optical Depth toward the SMC

Milky Way disk
(Han & Gould 2003)
SMC
Total

100

dNobs/dlogtE

dNobs/dlogtE

100

10 1

10 1

10 2

10 2

10 3

10 3
1

10

Milky Way disk
(Cautun+2020)
SMC
Total

100

tE (days)

1000

10000

1

10

100

1000

tE (days)

10000

Figure 7. Expected distributions of observed event timescales of microlensing events from known stellar populations in the
SMC (Calchi Novati et al. 2013; blue line) and the foreground Milky Way disk (red line). Left panel: assuming the Milky Way
model of Han & Gould (2003); right panel: Cautun et al. (2020).

Expected number of events

1.0

CDF

0.8
0.6
Observed CDF
SMC + MW disk
(Cautun+2020)
SMC + MW disk
(Han & Gould 2003)

0.4
0.2
0.0

1

10

100

tE (days)

1000

10000

Figure 8.
Expected cumulative distribution of event
timescales of microlensing events from known stellar populations in the SMC and the foreground Milky Way disk, assuming the Milky Way models of Cautun et al. (2020) (blue
line) and Han & Gould (2003) (red line). The observed cumulative distribution function is shown by the black line.

garded as an upper limit. Wyrzykowski et al. (2011b)
found τ = (1.30 ± 1.01) × 10−7 based on a sample of
three events. Of these three events, OGLE-SMC-02
had the largest contribution to this measurement (about
65%). The corresponding microlensing event rate is
Γ = (4.4 ± 2.6) × 10−7 yr−1 star−1 .
Using the combined OGLE-III and OGLE-IV data
set, we found smaller values for both the optical depth
(τ = (0.32 ± 0.18) × 10−7 ) and the event rate (Γ =
(1.18 ± 0.57) × 10−7 yr−1 star−1 ). However, because of

102

101

100
(

)

Figure 9. Expected number of microlensing events to be
detected in the SMC direction if the entire Milky Way’s dark
matter halo was composed of compact objects with identical
mass.

the small sample sizes, these measurements are formally
statistically consistent. For the same reason, the optical
depth measurements are prone to large statistical fluctuations. For example, including OGLE-SMC-02 in our
statistical sample would increase the optical depth by
20%.
One difference between our work and that of
Wyrzykowski et al. (2011b) is that we averaged the
optical depth over a much larger area than that observed by OGLE-III and used sources brighter than
I = 22 mag. In contrast, Wyrzykowski et al. (2011b)
took into account sources brighter than I = 21 mag.

## PDF page 18

18

P. Mróz et al.

100

Kepler
EROS

10 2

10103 12

OGLE-III
+OGLE-IV
(LMC)

OGLE-IV
high-cadence fields

10 9

MACHO+
EROS

This work
OGLE-III
+OGLE-IV
(SMC)

HSC

f

10 1

OGLE-III

10 6

10 3
M (M )

100

103

Figure 10. 95% upper limits on the fraction of dark matter in the form of PBHs and other compact objects. The shaded red
area is excluded at 95% confidence based on the presented observations of the SMC. The solid red line represents the strict
limits, whereas the dashed and dotted red lines indicate the relaxed limits for the Han & Gould (2003) and Cautun et al. (2020)
Milky Way disk models, respectively. Other limits are taken from Tisserand et al. (2007) (EROS), Wyrzykowski et al. (2011b)
(OGLE-III), Griest et al. (2013) (Kepler), Niikura et al. (2019) (HSC), Blaineau et al. (2022) (EROS+MACHO), Mróz et al.
(2024c) (OGLE-III + OGLE-IV), and Mróz et al. (2024a) (OGLE-IV high-cadence).

1

10.2. Limits on Compact Objects as Dark Matter
The limits on the abundance of compact objects in
dark matter, as derived in the previous section, were calculated for source stars brighter than I = 22 mag. However, the event detection efficiency substantially drops
with the decreasing source brightness, while the uncertainties on the number of source stars become larger.
These factors may increase the risk of introducing systematic errors into the analysis.
To evaluate the possible impact of these systematic
errors, we repeated the entire analysis using brighter
sources, for which these effects are substantially smaller.
The results are presented in Figure 11, which shows the
95% upper limits on f derived from sources brighter
than I = 21 (red line), I = 21.5 (blue line), and I = 22
mag (black line). As expected, the limits become slightly
weaker for brighter sources. However, the differences are
minimal; for example, the maximum difference between
the limits on f obtained using sources brighter than I =
21 and I = 22 mag is only 0.21 dex.
The inferred limits depend on the choice of the Milky
Way halo model. In this study, we used the contracted

f

When we restricted our measurements to the OGLE-III
footprint and used only sources brighter than I = 21
mag, we found τ = (0.52 ± 0.29) × 10−7 and Γ =
(1.76±0.83)×10−7 yr−1 star−1 , in better agreement with
the findings of Wyrzykowski et al. (2011b).

0.1

0.01
10 6

Limiting magnitude:
I = 21 mag
I = 21.5 mag
I = 22 mag

10 4

10 2

100

M (M )

102

104

Figure 11. Dependence of inferred upper limits on the limiting magnitude.

halo model from Cautun et al. (2020), which was fitted
to the Milky Way’s rotation curve derived from the Gaia
DR2 data (Eilers et al. 2019). However, several recent
works (e.g., Wang et al. 2023; Jiao et al. 2023; Ou et al.
2024) have indicated evidence for a declining Milky Way
rotation curve at Galactocentric distances greater than
15–20 kpc, based on the more recent Gaia DR3 data.
This suggests that the estimated mass of the Milky Way
halo may be smaller than previously thought. These
new findings, however, are in tension with other mass

## PDF page 19

Microlensing Optical Depth toward the SMC
estimates derived from observations of globular clusters,
dwarf satellites, and streams. Koop et al. (2024) pointed
out that—at large Galactocentric radii—disequilibrium
and deviations from axisymmetry could lead to large
systematic errors in the inferred rotation curves.
Nevertheless, we found that our results are not
strongly influenced by the choice of these models. The
inferred limits on the frequency of PBHs are inversely
proportional to the expected number of microlensing
events, which in turn is directly proportional to the optical depth in a given direction. For example, the microlensing optical depth due to the Milky Way’s dark
matter halo in the direction of the SMC center (l = 303◦ ,
b = −44◦ , DSMC = 62.44 kpc) in our fiducial model
(Cautun et al. 2020) is τ = 6.4 × 10−7 . For the B2 halo
model from Jiao et al. (2023), we find τ = 6.2 × 10−7 ,
while the halo model from Ou et al. (2024) yields τ =
6.0 × 10−7 . These results indicate that the inferred limits on f would be reduced by less than 6% if the halo
model from Cautun et al. (2020) was replaced by that
of Jiao et al. (2023) or Ou et al. (2024).
Additionally, Green (2025) investigated how the
choice of the halo model impacts microlensing constraints on the abundance of PBHs. They considered
two power-law halo models (Evans 1994) from Alcock
et al. (1996) (models B and C) and found that the
tightest limit on f is a factor of 1.7 (1.5) lower (higher)
for model B (C) compared to the standard halo model.
We note, however, that none of these models accurately
fit the Milky Way rotation curve (Mróz et al. 2019b):
model B consistently predicts higher rotation speeds,
while model C predicts lower speeds than actually observed. In contrast, the rotation curves predicted by the
models from Cautun et al. (2020), Jiao et al. (2023), and
Ou et al. (2024) match the data very well. We conclude
that the uncertainties on f associated with the choice
of the Milky Way halo model are substantially smaller
than those indicated by the predictions of the B and C
halo models of Alcock et al. (1996).
Recently, Li et al. (2025) studied the constraints on
the abundance of planetary-mass PBHs based on a sample of 2617 events detected by OGLE in the direction
of the Galactic bulge (Mróz et al. 2017). They investigated the dependence of these constraints on the
choice of dark matter halo models and found that the
constraints derived assuming the Einasto and Burkert
profiles are much weaker than those from the standard
Navarro–Frenk–White profile. We check the same models to study the robustness of our results.
The Einasto profile used by Li et al. (2025) was taken
from Hertzberg et al. (2021), who in turn used the dark
matter profile from Pieri et al. (2011). The latter model

19

was found from the Milky Way Aquarius simulations by
Springel et al. (2008). Unfortunately, the parameters of
the model changed during this telephone game: Pieri
et al. (2011) reported the normalization of the profile of
ρs = 2.8×106 M⊙ kpc−1 , while Li et al. (2025) used ρs =
2.08 × 106 M⊙ kpc−1 (thus, the constrains published by
Li et al. (2025) are underestimated by 35%). Assuming
that the parameters from Pieri et al. (2011) are correct,
the microlensing optical depth toward the SMC center
is τ = 11.1 × 10−7 , i.e., a factor 1.7 larger than in our
fiducial model. However, the Milky Way rotation curve
predicted by the former model does not match the data
(Mróz et al. 2019b). We also found that the rotation
curves calculated using Burkert profiles considered in Li
et al. (2025) do not match the observed one at all (Mróz
et al. 2019b). That is not surprising, as these models
come from Donato et al. (2009) and they were intended
to fit the weak gravitational lensing observations of some
galaxies, but not the Milky Way dark matter profile.
10.3. Summary
This paper concludes the current searches for microlensing events toward the Magellanic Clouds using
data from the OGLE survey. In Paper 1 and Paper 2,
we presented the results of the searches for very longtimescale microlensing events toward the LMC using the
combined OGLE-III and OGLE-IV data. Such longduration events were expected if dark matter in the
Milky Way halo consisted of massive PBHs, with masses
ranging from dozens to hundreds M⊙ , similar to black
holes detected by the gravitational-wave observatories.
In Paper 3, we searched for short-duration microlensing
events that could have been caused by planetary-mass
PBHs. No such events were discovered, which provided
very strict limits on the abundance of PBHs and other
compact objects in the Milky Way halo with masses
ranging from 10−8 to 103 M⊙ .
In this paper, we extended our search for longtimescale microlensing events to stars located in the
SMC. Thanks to combining OGLE-III and OGLE-IV
data, we created nearly 20-year-long light curves for
about 7.4 million stars. For an additional 6.2 million
stars, we used 10-year-long OGLE-IV light curves. The
analysis of this data set allowed us to achieve high sensitivity to long-timescale microlensing events.
We recovered three previously known events and discovered three new ones. We measured the microlensing optical depth toward the SMC to be τ = (0.32 ±
0.18) × 10−7 and the event rate to be Γ = (1.18 ± 0.57) ×
10−7 yr−1 star−1 . The properties of the detected events
are consistent with lenses originating from known stellar
populations within the SMC or in the Milky Way disk,

## PDF page 20

20

P. Mróz et al.

leaving little room for PBHs or other dark compact objects in the dark matter halo.
In particular, our findings indicate that PBHs with
a mass of 1 M⊙ may account for at most 2.9% of the
dark matter in the Milky Way, 10 M⊙ —6.4%, 100 M⊙ —
16%. While these limits are weaker than those derived in
Paper 2, they are still stronger than the results reported
by Tisserand et al. (2007), Wyrzykowski et al. (2011b),
and Blaineau et al. (2022) for the mass range of 10−4 −
102 M⊙ . In addition, our results provide independent
information about the number of compact objects along
a different line of sight through the Galactic halo.
The data presented in this paper are publicly available at https://www.astrouw.edu.pl/ogle/ogle4/SMC_

OPTICAL_DEPTH/ and via doi:
odo.16735482.

105281/zen-

ACKNOWLEDGEMENTS
We thank the anonymous referee for providing constructive comments that helped improve the paper.
We thank all of the OGLE observers for their contribution to the collection of the photometric data
over the decades. We thank Łukasz Wyrzykowski for
his comments on the manuscript. This research was
funded in part by National Science Centre, Poland,
grants OPUS 2021/41/B/ST9/00252 and SONATA
2023/51/D/ST9/00187 awarded to P.M. The OGLE
project has received funding from the Polish National
Science Centre grant OPUS 2024/55/B/ST9/00447
awarded to A.U.

REFERENCES
Afonso, C., Alard, C., Albert, J. N., et al. 2000, ApJ, 532,
340

Carr, B. J., Clesse, S., García-Bellido, J., Hawkins,
M. R. S., & Kühnel, F. 2024, PhR, 1054, 1

Alard, C., & Lupton, R. H. 1998, ApJ, 503, 325

Carr, B. J., & Hawking, S. W. 1974, MNRAS, 168, 399

Alcock, C., Allsman, R. A., Axelrod, T. S., et al. 1996,
ApJ, 461, 84

Cautun, M., Benítez-Llambay, A., Deason, A. J., et al.
2020, MNRAS, 494, 4291

Alcock, C., Allsman, R. A., Alves, D., et al. 1997a, ApJL,
491, L11

Chapline, G. F. 1975, Nature, 253, 251

Alcock, C., Allsman, R. A., Alves, D., et al. 1997b, ApJ,
486, 697
Alcock, C., Allsman, R. A., Alves, D., et al. 1999, ApJ, 518,
44
Alcock, C., Allsman, R. A., Alves, D. R., et al. 2000, ApJ,
542, 281
Batista, V., Gould, A., Dieters, S., et al. 2011, A&A, 529,
A102
Bechtol, K., Birrer, S., Cyr-Racine, F.-Y., et al. 2022, arXiv
e-prints, arXiv:2203.07354
Bekki, K., & Chiba, M. 2009, PASA, 26, 37
Bekki, K., & Stanimirović, S. 2009, MNRAS, 395, 342
Bird, S., Cholis, I., Muñoz, J. B., et al. 2016, PhRvL, 116,
201301
Blaineau, T., Moniez, M., Afonso, C., et al. 2022, A&A,
664, A106
Calchi Novati, S. 2010, General Relativity and Gravitation,
42, 2101
Calchi Novati, S., Mirzoyan, S., Jetzer, P., & Scarpetta, G.
2013, MNRAS, 435, 1582
Calchi Novati, S., Paulin-Henriksson, S., An, J., et al. 2005,
A&A, 443, 911
Carr, B., Kohri, K., Sendouda, Y., & Yokoyama, J. 2021,
Reports on Progress in Physics, 84, 116902

Clesse, S., & García-Bellido, J. 2017, Physics of the Dark
Universe, 15, 142
Croon, D., McKeen, D., & Raj, N. 2020, PhRvD, 101,
083013
de Jong, J. T. A., Widrow, L. M., Cseresnjes, P., et al.
2006, A&A, 446, 855
Despali, G., Vegetti, S., White, S. D. M., Giocoli, C., & van
den Bosch, F. C. 2018, MNRAS, 475, 5424
Donato, F., Gentile, G., Salucci, P., et al. 2009, MNRAS,
397, 1169
Dong, S., Udalski, A., Gould, A., et al. 2007, ApJ, 664, 862
Eilers, A.-C., Hogg, D. W., Rix, H.-W., & Ness, M. K.
2019, ApJ, 871, 120
Evans, N. W. 1994, MNRAS, 267, 333
Gaia Collaboration, Prusti, T., de Bruijne, J. H. J., et al.
2016, A&A, 595, A1
Gaia Collaboration, Helmi, A., van Leeuwen, F., et al.
2018, A&A, 616, A12
Gaia Collaboration, Luri, X., Chemin, L., et al. 2021a,
A&A, 649, A7
Gaia Collaboration, Brown, A. G. A., Vallenari, A., et al.
2021b, A&A, 649, A1
Gonidakis, I., Livanou, E., Kontizas, E., et al. 2009, A&A,
496, 375
Gould, A. 2004, ApJ, 606, 319

## PDF page 21

Microlensing Optical Depth toward the SMC
Gould, A., Miralda-Escude, J., & Bahcall, J. N. 1994,
ApJL, 423, L105
Graczyk, D., Pietrzyński, G., Thompson, I. B., et al. 2020,
ApJ, 904, 13
Green, A. M. 2025, JCAP, 2025, 023
Green, A. M., & Kavanagh, B. J. 2021, Journal of Physics
G Nuclear Physics, 48, 043001
Griest, K., Cieplak, A. M., & Lehner, M. J. 2013, PhRvL,
111, 181302
Han, C., & Gould, A. 1995, ApJ, 449, 521
Han, C., & Gould, A. 2003, ApJ, 592, 172
Hawking, S. 1971, MNRAS, 152, 75
Hertzberg, M. P., Nurmi, S., Schiappacasse, E. D., &
Yanagida, T. T. 2021, PhRvD, 103, 063025
Holtzman, J. A., Afonso, C., & Dolphin, A. 2006, ApJS,
166, 534
Jacyszyn-Dobrzeniecka, A. M., Skowron, D. M., Mróz, P.,
et al. 2016, AcA, 66, 149
Jacyszyn-Dobrzeniecka, A. M., Skowron, D. M., Mróz, P.,
et al. 2017, AcA, 67, 1
Jiao, Y., Hammer, F., Wang, H., et al. 2023, A&A, 678,
A208
Kiraga, M., & Paczyński, B. 1994, ApJL, 430, L101
Koop, O., Antoja, T., Helmi, A., Callingham, T. M., &
Laporte, C. F. P. 2024, A&A, 692, A50
Kroupa, P. 2001, MNRAS, 322, 231
Li, B., Tang, C.-Y., Huang, Z.-R., & Liu, L.-H. 2025, arXiv
e-prints, arXiv:2507.00770
Li, R., Frenk, C. S., Cole, S., Wang, Q., & Gao, L. 2017,
MNRAS, 468, 1426
McConnachie, A. W. 2012, AJ, 144, 4
Mróz, P., & Poleski, R. 2018, AJ, 155, 154
Mróz, P., Udalski, A., Skowron, J., et al. 2017, Nature, 548,
183
Mróz, P., Udalski, A., Skowron, J., et al. 2019a, ApJS, 244,
29
Mróz, P., Udalski, A., Skowron, D. M., et al. 2019b, ApJL,
870, L10
Mróz, P., Udalski, A., Szymański, M. K., et al. 2024a,
ApJL, 976, L19, (Paper III)
Mróz, P., Udalski, A., Szymański, M. K., et al. 2024b,
ApJS, 273, 4, (Paper I)
Mróz, P., Udalski, A., Szymański, M. K., et al. 2024c,
Nature, 632, 749, (Paper II)
Navas, S., Amsler, C., Gutsche, T., et al. 2024, PhRvD,
110, 030001
Niikura, H., Takada, M., Yasuda, N., et al. 2019, Nature
Astronomy, 3, 524
Ou, X., Eilers, A.-C., Necib, L., & Frebel, A. 2024,
MNRAS, 528, 693
Paczyński, B. 1986, ApJ, 304, 1

21

Palanque-Delabrouille, N., Afonso, C., Albert, J. N., et al.
1998, A&A, 332, 1
Pedregosa, F., Varoquaux, G., Gramfort, A., et al. 2011,
Journal of Machine Learning Research, 12, 2825
Pieri, L., Lavalle, J., Bertone, G., & Branchini, E. 2011,
PhRvD, 83, 023518
Sahu, K. C. 1994, Nature, 370, 275
Sasaki, M., Suyama, T., Tanaka, T., & Yokoyama, S. 2016,
PhRvL, 117, 061101
Schlafly, E. F., & Finkbeiner, D. P. 2011, ApJ, 737, 103
Sengül, A. Ç., Dvorkin, C., Ostdiek, B., & Tsang, A. 2022,
MNRAS, 515, 4391
Skowron, D. M., Skowron, J., Udalski, A., et al. 2021,
ApJS, 252, 23
Skowron, J., Udalski, A., Kozłowski, S., et al. 2016, AcA,
66, 1
Smith, M. C., Mao, S., & Paczyński, B. 2003, MNRAS,
339, 925
Springel, V., Wang, J., Vogelsberger, M., et al. 2008,
MNRAS, 391, 1685
Tisserand, P., Le Guillou, L., Afonso, C., et al. 2007, A&A,
469, 387
Tomaney, A. B., & Crotts, A. P. S. 1996, AJ, 112, 2872
Udalski, A. 2003, AcA, 53, 291
Udalski, A., Kubiak, M., & Szymański, M. 1997a, AcA, 47,
319
Udalski, A., Szymanski, M., Kubiak, M., et al. 1997b, AcA,
47, 431
Udalski, A., Szymański, M. K., & Szymański, G. 2015,
AcA, 65, 1
Vegetti, S., Koopmans, L. V. E., Bolton, A., Treu, T., &
Gavazzi, R. 2010, MNRAS, 408, 1969
Vegetti, S., Lagattuta, D. J., McKean, J. P., et al. 2012,
Nature, 481, 341
Wang, H.-F., Chrobáková, Ž., López-Corredoira, M., &
Sylos Labini, F. 2023, ApJ, 942, 12
Woźniak, P. R. 2000, AcA, 50, 421
Wyrzykowski, Ł., Kozłowski, S., Skowron, J., et al. 2009,
MNRAS, 397, 1228
Wyrzykowski, Ł., Kozłowski, S., Skowron, J., et al. 2010,
MNRAS, 407, 189
Wyrzykowski, Ł., Kozłowski, S., Skowron, J., et al. 2011a,
MNRAS, 413, 493
Wyrzykowski, Ł., Skowron, J., Kozłowski, S., et al. 2011b,
MNRAS, 416, 2949
Zel’dovich, Y. B., & Novikov, I. D. 1967, Soviet Ast., 10,
602

## PDF page 22

22

P. Mróz et al.
Table 10. Parameters of the SMC Proper-Motion Model
ρ

∂µx /∂x

∂µx /∂y

µx,0

∂µy /∂x

∂µy /∂y

µy,0

rms(µx )

rms(µy )

(deg)

(mas yr−1 rad−1 )

(mas yr−1 rad−1 )

(mas yr−1 )

(mas yr−1 rad−1 )

(mas yr−1 rad−1 )

(mas yr−1 )

(mas yr−1 )

(mas yr−1 )

0<ρ<1
1<ρ<2
2<ρ<3
3<ρ<4
4<ρ<5

1.0474
2.3849
2.2517
1.8572
1.9689

1.3827
0.4965
−0.2830
−0.6033
−0.5812

0.6737
0.6883
0.7019
0.7423
0.7527

−1.5333
−1.7648
−1.8570
−1.7579
−1.9031

−0.4887
0.0268
0.3592
0.4468
0.7271

−1.2330
−1.2429
−1.2580
−1.2857
−1.2893

0.024
0.024
0.041
0.069
0.074

0.064
0.075
0.099
0.072
0.063

APPENDIX

A. SMC PROPER MOTION AND ROTATION

Following Paper 2, we used the Gaia DR3 data (Gaia
Collaboration et al. 2016, 2021b) to model the kinematics of the SMC. We used a similar approach to that used
by Gaia Collaboration et al. (2018) and Gaia Collaboration et al. (2021a). We first selected stars brighter
than G = 19.5 mag and located within the angular distance ρ = 8◦ of the center of the SMC (α0 = 12.80◦ ,
δ0 = −73.15◦ ; Gaia Collaboration et al. 2021a). We selected stars with well-measured astrometric parameters
(RUWE ≤ 1.4) and parallaxes consistent with those of
SMC stars (ϖ ≤ 1.0 mas and ϖ/σϖ < 10), in total
approximately 1.8 million objects. The positions and
proper motions of all stars were transformed to Cartesian coordinates (x, y, µx , µy ) using the orthographic
projection centered on (α0 , δ0 ) (Paper 2). We divided
the area defined by |x| ≤ 0.15 rad and |y| ≤ 0.15 rad
into 100 × 100 bins, and calculated the median proper
motions within each bin. We then fitted the following
linear model to the binned data (using bins with at least
10 stars):
∂µx
∂µx
x+
y,
∂x
∂y
∂µy
∂µy
µy = µy,0 +
x+
y.
∂x
∂y

µx = µx,0 +

(A1)

The best-fit parameters—for five annuli with a width of
1◦ —are reported in Table 10. Table 10 also reports the
dispersion of proper motions in each annulus.
