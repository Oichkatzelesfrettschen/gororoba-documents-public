Source: https://arxiv.org/abs/2306.16213v1
PDF sha256: 3a33495ae465768f832d5e55efff0769a6a6c41564ce8714e3f51ba929785aeb
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of arxiv_2306.16213_agazie_et_al_2023_nanograv_15yr_gwb.pdf

Transcription of `arxiv_2306.16213_agazie_et_al_2023_nanograv_15yr_gwb.pdf` in this directory, 30 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-30 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Draft version June 29, 2023
Typeset using LATEX twocolumn style in AASTeX63

arXiv:2306.16213v1 [astro-ph.HE] 28 Jun 2023

The NANOGrav 15-year Data Set: Evidence for a Gravitational-Wave Background
Gabriella Agazie,1 Akash Anumarlapudi,1 Anne M. Archibald,2 Zaven Arzoumanian,3 Paul T. Baker,4
Bence Bécsy,5 Laura Blecha,6 Adam Brazier,7, 8 Paul R. Brook,9 Sarah Burke-Spolaor,10, 11 Rand Burnette,5
Robin Case,5 Maria Charisi,12 Shami Chatterjee,7 Katerina Chatziioannou,13 Belinda D. Cheeseboro,10, 11
Siyuan Chen,14 Tyler Cohen,15 James M. Cordes,7 Neil J. Cornish,16 Fronefield Crawford,17
H. Thankful Cromartie,7, ∗ Kathryn Crowter,18 Curt J. Cutler,19, 13 Megan E. DeCesar,20 Dallas DeGan,5
Paul B. Demorest,21 Heling Deng,5 Timothy Dolch,22, 23 Brendan Drachler,24, 25 Justin A. Ellis,26
Elizabeth C. Ferrara,27, 28, 29 William Fiore,10, 11 Emmanuel Fonseca,10, 11 Gabriel E. Freedman,1
Nate Garver-Daniels,10, 11 Peter A. Gentile,10, 11 Kyle A. Gersbach,12 Joseph Glaser,10, 11 Deborah C. Good,30, 31
Kayhan Gültekin,32 Jeffrey S. Hazboun,5 Sophie Hourihane,13 Kristina Islo,1 Ross J. Jennings,10, 11, †
Aaron D. Johnson,1, 13 Megan L. Jones,1 Andrew R. Kaiser,10, 11 David L. Kaplan,1 Luke Zoltan Kelley,33
Matthew Kerr,34 Joey S. Key,35 Tonia C. Klein,1 Nima Laal,5 Michael T. Lam,24, 25 William G. Lamb,12
T. Joseph W. Lazio,19 Natalia Lewandowska,36 Tyson B. Littenberg,37 Tingting Liu,10, 11 Andrea Lommen,38
Duncan R. Lorimer,10, 11 Jing Luo,39, ‡ Ryan S. Lynch,40 Chung-Pei Ma,33, 41 Dustin R. Madison,42
Margaret A. Mattson,10, 11 Alexander McEwen,1 James W. McKee,43, 44 Maura A. McLaughlin,10, 11
Natasha McMann,12 Bradley W. Meyers,18, 45 Patrick M. Meyers,13 Chiara M. F. Mingarelli,31, 30, 46
Andrea Mitridate,47 Priyamvada Natarajan,48, 49 Cherry Ng,50 David J. Nice,51 Stella Koch Ocker,7
Ken D. Olum,52 Timothy T. Pennucci,53 Benetge B. P. Perera,54 Polina Petrov,12 Nihan S. Pol,12
Henri A. Radovan,55 Scott M. Ransom,56 Paul S. Ray,34 Joseph D. Romano,57 Shashwat C. Sardesai,1
Ann Schmiedekamp,58 Carl Schmiedekamp,58 Kai Schmitz,59 Levi Schult,12 Brent J. Shapiro-Albert,10, 11, 60
Xavier Siemens,5, 1 Joseph Simon,61, § Magdalena S. Siwek,62 Ingrid H. Stairs,18 Daniel R. Stinebring,63
Kevin Stovall,21 Jerry P. Sun,5 Abhimanyu Susobhanan,1 Joseph K. Swiggum,51, † Jacob Taylor,5
Stephen R. Taylor,12 Jacob E. Turner,10, 11 Caner Unal,64, 65 Michele Vallisneri,19, 13 Rutger van Haasteren,66
Sarah J. Vigeland,1 Haley M. Wahl,10, 11 Qiaohong Wang,12 Caitlin A. Witt,67, 68 Olivia Young,24, 25
The NANOGrav Collaboration

1 Center for Gravitation, Cosmology and Astrophysics, Department of Physics, University of Wisconsin-Milwaukee,

P.O. Box 413, Milwaukee, WI 53201, USA
2 Newcastle University, NE1 7RU, UK
3 X-Ray Astrophysics Laboratory, NASA Goddard Space Flight Center, Code 662, Greenbelt, MD 20771, USA
4 Department of Physics and Astronomy, Widener University, One University Place, Chester, PA 19013, USA
5 Department of Physics, Oregon State University, Corvallis, OR 97331, USA
6 Physics Department, University of Florida, Gainesville, FL 32611, USA
7 Cornell Center for Astrophysics and Planetary Science and Department of Astronomy, Cornell University, Ithaca, NY 14853, USA
8 Cornell Center for Advanced Computing, Cornell University, Ithaca, NY 14853, USA
9 Institute for Gravitational Wave Astronomy and School of Physics and Astronomy, University of Birmingham, Edgbaston, Birmingham
B15 2TT, UK
10 Department of Physics and Astronomy, West Virginia University, P.O. Box 6315, Morgantown, WV 26506, USA
11 Center for Gravitational Waves and Cosmology, West Virginia University, Chestnut Ridge Research Building, Morgantown, WV
26505, USA
12 Department of Physics and Astronomy, Vanderbilt University, 2301 Vanderbilt Place, Nashville, TN 37235, USA
13 Division of Physics, Mathematics, and Astronomy, California Institute of Technology, Pasadena, CA 91125, USA
14 Kavli Institute for Astronomy and Astrophysics, Peking University, Beijing, 100871 China
15 Department of Physics, New Mexico Institute of Mining and Technology, 801 Leroy Place, Socorro, NM 87801, USA
16 Department of Physics, Montana State University, Bozeman, MT 59717, USA
17 Department of Physics and Astronomy, Franklin & Marshall College, P.O. Box 3003, Lancaster, PA 17604, USA
18 Department of Physics and Astronomy, University of British Columbia, 6224 Agricultural Road, Vancouver, BC V6T 1Z1, Canada
19 Jet Propulsion Laboratory, California Institute of Technology, 4800 Oak Grove Drive, Pasadena, CA 91109, USA
20 George Mason University, resident at the Naval Research Laboratory, Washington, DC 20375, USA

Corresponding author: The NANOGrav Collaboration
comments@nanograv.org

## PDF page 2

2

The NANOGrav Collaboration
21 National Radio Astronomy Observatory, 1003 Lopezville Rd., Socorro, NM 87801, USA
22 Department of Physics, Hillsdale College, 33 E. College Street, Hillsdale, MI 49242, USA
23 Eureka Scientific, 2452 Delmer Street, Suite 100, Oakland, CA 94602-3017, USA
24 School of Physics and Astronomy, Rochester Institute of Technology, Rochester, NY 14623, USA
25 Laboratory for Multiwavelength Astrophysics, Rochester Institute of Technology, Rochester, NY 14623, USA
26 Bionic Health, 800 Park Offices Drive, Research Triangle Park, NC 27709
27 Department of Astronomy, University of Maryland, College Park, MD 20742
28 Center for Research and Exploration in Space Science and Technology, NASA/GSFC, Greenbelt, MD 20771
29 NASA Goddard Space Flight Center, Greenbelt, MD 20771, USA
30 Department of Physics, University of Connecticut, 196 Auditorium Road, U-3046, Storrs, CT 06269-3046, USA
31 Center for Computational Astrophysics, Flatiron Institute, 162 5th Avenue, New York, NY 10010, USA
32 Department of Astronomy and Astrophysics, University of Michigan, Ann Arbor, MI 48109, USA
33 Department of Astronomy, University of California, Berkeley, 501 Campbell Hall #3411, Berkeley, CA 94720, USA
34 Space Science Division, Naval Research Laboratory, Washington, DC 20375-5352, USA
35 University of Washington Bothell, 18115 Campus Way NE, Bothell, WA 98011, USA
36 Department of Physics, State University of New York at Oswego, Oswego, NY, 13126, USA
37 NASA Marshall Space Flight Center, Huntsville, AL 35812, USA
38 Department of Physics and Astronomy, Haverford College, Haverford, PA 19041, USA
39 Department of Astronomy & Astrophysics, University of Toronto, 50 Saint George Street, Toronto, ON M5S 3H4, Canada
40 Green Bank Observatory, P.O. Box 2, Green Bank, WV 24944, USA
41 Department of Physics, University of California, Berkeley, CA 94720, USA
42 Department of Physics, University of the Pacific, 3601 Pacific Avenue, Stockton, CA 95211, USA
43 E.A. Milne Centre for Astrophysics, University of Hull, Cottingham Road, Kingston-upon-Hull, HU6 7RX, UK
44 Centre of Excellence for Data Science, Artificial Intelligence and Modelling (DAIM), University of Hull, Cottingham Road,

Kingston-upon-Hull, HU6 7RX, UK
45 International Centre for Radio Astronomy Research, Curtin University, Bentley, WA 6102, Australia
46 Department of Physics, Yale University, New Haven, CT 06520, USA
47 Deutsches Elektronen-Synchrotron DESY, Notkestr. 85, 22607 Hamburg, Germany
48 Department of Astronomy, Yale University, 52 Hillhouse Ave, New Haven, CT 06511
49 Black Hole Initiative, Harvard University, 20 Garden Street, Cambridge, MA 02138
50 Dunlap Institute for Astronomy and Astrophysics, University of Toronto, 50 St. George St., Toronto, ON M5S 3H4, Canada
51 Department of Physics, Lafayette College, Easton, PA 18042, USA
52 Institute of Cosmology, Department of Physics and Astronomy, Tufts University, Medford, MA 02155, USA
53 Institute of Physics and Astronomy, Eötvös Loránd University, Pázmány P. s. 1/A, 1117 Budapest, Hungary
54 Arecibo Observatory, HC3 Box 53995, Arecibo, PR 00612, USA
55 Department of Physics, University of Puerto Rico, Mayagüez, PR 00681, USA
56 National Radio Astronomy Observatory, 520 Edgemont Road, Charlottesville, VA 22903, USA
57 Department of Physics, Texas Tech University, Box 41051, Lubbock, TX 79409, USA
58 Department of Physics, Penn State Abington, Abington, PA 19001, USA
59 Institute for Theoretical Physics, University of Münster, 48149 Münster, Germany
60 Giant Army, 915A 17th Ave, Seattle WA 98122
61 Department of Astrophysical and Planetary Sciences, University of Colorado, Boulder, CO 80309, USA
62 Center for Astrophysics, Harvard University, 60 Garden St, Cambridge, MA 02138
63 Department of Physics and Astronomy, Oberlin College, Oberlin, OH 44074, USA
64 Department of Physics, Ben-Gurion University of the Negev, Be’er Sheva 84105, Israel
65 Feza Gursey Institute, Bogazici University, Kandilli, 34684, Istanbul, Turkey
66 Max-Planck-Institut für Gravitationsphysik (Albert-Einstein-Institut), Callinstrasse 38, D-30167, Hannover, Germany
67 Center for Interdisciplinary Exploration and Research in Astrophysics (CIERA), Northwestern University, Evanston, IL 60208
68 Adler Planetarium, 1300 S. DuSable Lake Shore Dr., Chicago, IL 60605, USA

ABSTRACT
We report multiple lines of evidence for a stochastic signal that is correlated among 67 pulsars
from the 15-year pulsar-timing data set collected by the North American Nanohertz Observatory for
Gravitational Waves. The correlations follow the Hellings–Downs pattern expected for a stochastic
gravitational-wave background. The presence of such a gravitational-wave background with a powerlaw–spectrum is favored over a model with only independent pulsar noises with a Bayes factor in excess

## PDF page 3

NANOGrav 15-year Gravitational-Wave Background

3

of 1014 , and this same model is favored over an uncorrelated common power-law–spectrum model with
Bayes factors of 200–1000, depending on spectral modeling choices. We have built a statistical background distribution for these latter Bayes factors using a method that removes inter-pulsar correlations
from our data set, finding p = 10−3 (approx. 3σ) for the observed Bayes factors in the null no-correlation
scenario. A frequentist test statistic built directly as a weighted sum of inter-pulsar correlations yields
p = 5 × 10−5 –1.9 × 10−4 (approx. 3.5–4σ). Assuming a fiducial f −2/3 characteristic-strain spectrum,
as appropriate for an ensemble of binary supermassive black-hole inspirals, the strain amplitude is
−15
2.4+0.7
(median + 90% credible interval) at a reference frequency of 1 yr−1 . The inferred
−0.6 × 10
gravitational-wave background amplitude and spectrum are consistent with astrophysical expectations
for a signal from a population of supermassive black-hole binaries, although more exotic cosmological
and astrophysical sources cannot be excluded. The observation of Hellings–Downs correlations points
to the gravitational-wave origin of this signal.
Keywords: Gravitational waves – Black holes – Pulsars
1. INTRODUCTION

Almost a century had to elapse between Einstein’s prediction of gravitational waves (GWs, Einstein 1916) and
their measurement from a coalescing binary of stellarmass black holes (Abbott et al. 2016). However, their
existence had been confirmed in the late 1970s through
measurements of the orbital decay of the Hulse–Taylor
binary pulsar (Hulse & Taylor 1975; Taylor et al. 1979).
Today, pulsars are again at the forefront of the quest to
detect GWs, this time from binary systems of central
galactic black holes.
Black holes with masses of 105 –1010 M⊙ exist at the
center of most galaxies and are closely correlated with
the global properties of the host, suggesting a symbiotic evolution (Magorrian et al. 1998; McConnell &
Ma 2013). Galaxy mergers are the main drivers of hierarchical structure formation over cosmic time (Blumenthal et al. 1984) and lead to the formation of
close massive–black-hole binaries long after the mergers
(Begelman et al. 1980; Milosavljević & Merritt 2003).
The most massive of these (supermassive black-hole binaries, SMBHBs, with masses 108 –1010 M⊙ ) emit GWs
with slowly evolving frequencies, contributing to a noiselike broadband signal in the nHz range (the GW background, GWB; Rajagopal & Romani 1995; Jaffe &
Backer 2003; Wyithe & Loeb 2003; Sesana et al. 2004;
McWilliams et al. 2014; Burke-Spolaor et al. 2019). If
all contributing SMBHBs evolve purely by loss of circular orbital energy to gravitational radiation, the resultant GWB spectrum is well described by a simple
f −2/3 characteristic-strain power law (Phinney 2001).
∗ NASA Hubble Fellowship: Einstein Postdoctoral Fellow
† NANOGrav Physics Frontiers Center Postdoctoral Fellow
‡ Deceased
§ NSF Astronomy and Astrophysics Postdoctoral Fellow

However, GWB signals that are not produced by populations of inspiraling black holes may also lie within the
nHz band; these include primordial GWs from inflation,
scalar-induced GWs, and GW signals from multiple processes arising due to cosmological phase transitions, such
as collisions of bubbles of the post-transition vacuum
state, sound waves, turbulence, and the decay of any
defects such as cosmic strings or domain walls that may
have formed (see, e.g., Guzzetti et al. 2016; Caprini &
Figueroa 2018; Domènech 2021, and references therein).
The detection of nHz GWs follows the template outlined by Pirani (1956, 2009), whereby we time the propagation of light to measure modulations in the distance
between freely falling reference masses. Estabrook &
Wahlquist (1975) derived the GW response of electromagnetic signals traveling between Earth and distant
spacecraft, sparking interest in low-frequency GW detection. Sazhin (1978) and Detweiler (1979) described
nHz GW detection using Galactic pulsars and (effectively) the solar system barycenter as references, relying
on the regularity of pulsar emission and planetary motions to highlight GW effects. The fact that pulsars
are such accurate clocks enables precise measurements
of their rotational, astrometric, and binary parameters
(and more) from the times-of-arrival of their pulses,
which are used to develop ever-refining end-to-end timing models. Hellings & Downs (1983) made the crucial suggestion that the correlations between the timeof-arrival perturbations of multiple pulsars could reveal
a GW signal buried in pulsar noise; Romani (1989) and
Foster & Backer (1990) proposed that a pulsar timing
array (PTA) of highly stable millisecond pulsars (Backer
et al. 1982) could be used to search for a GWB. Nevertheless, the first multi-pulsar, long-term GWB limits
were obtained by analyzing millisecond-pulsar residuals
independently, rather than as an array (Stinebring et al.
1990; Kaspi et al. 1994).

## PDF page 4

4

The NANOGrav Collaboration

(a)

(c)

(b)

(d)

log10 AGWB

° ° ° ° ° °
14 14 14 14 14 13
.8 .6 .4 .2 .0 .8

𝛾GWB = 13/3

fref = 1 yr°1 ≈ 32 nHz
fref = 0.1 yr°1 ≈ 3.2 nHz

2.5

3.0

3.5

gGWB

4.0

4.5

Figure 1. Summary of the main Bayesian and optimal-statistic analyses presented in this paper, which establish multiple lines
of evidence for the presence of Hellings–Downs correlations in the 15-year NANOGrav data set. Throughout we refer to the
68.3%, 95.4%, and 99.7% regions of distributions as 1/2/3σ regions, even in two dimensions. (a): Bayesian “free-spectrum”
analysis, showing posteriors (gray violins) of independent variance parameters for a Hellings–Downs-correlated stochastic process
at frequencies i/T , with T the total data set time span. The blue represents the posterior median and 1/2σ posterior bandsa
for a power-law model; the dashed black line corresponds to a γ = 13/3 (SMBHB-like) power-law, plotted with the median
posterior amplitude. See §3 for more details. (b): Posterior probability distribution of GWB amplitude and spectral exponent
in a HD power-law model, showing 1/2/3σ credible regions. The value γGWB = 13/3 (dashed black line) is included in the 99%
credible region. The amplitude is referenced to fref = 1 yr−1 (blue) and 0.1 yr−1 (orange). The dashed blue and orange curves
in the log10 AGWB subpanel shows its marginal posterior density for a γ = 13/3 model, with fref = 1 yr−1 and fref = 0.1 yr−1 ,
respectively. See §3 for more details. (c): Angular-separation–binned inter-pulsar correlations, measured from 2,211 distinct
pairings in our 67-pulsar array using the frequentist optimal statistic, assuming maximum-a-posteriori pulsar noise parameters
and γ = 13/3 common-process amplitude from a Bayesian inference analysis. The bin widths are chosen so that each includes
approximately the same number of pulsar pairs, and central bin locations avoid zeros of the Hellings–Downs curve. This binned
reconstruction accounts for correlations between pulsar pairs (Romano et al. 2021; Allen & Romano 2022). The dashed black
line shows the Hellings–Downs correlation pattern, and the binned points are normalized by the amplitude of the γ = 13/3
common process to be on the same scale. Note that we do not employ binning of inter-pulsar correlations in our detection
statistics; this panel serves as a visual consistency check only. See §4 for more frequentist results. (d): Bayesian reconstruction
of normalized inter-pulsar correlations, modeled as a cubic spline within a variable-exponent power-law model. The violins plot
the marginal posterior densities (plus median and 68% credible values) of the correlations at the knots. The knot positions are
fixed, and are chosen on the basis of features of the Hellings–Downs curve (also shown as a dashed black line for reference): they
include the maximum and minimum angular separations, the two zero crossings of the Hellings–Downs curve, and the position
of minimum correlation. See §3 for more details.

## PDF page 5

NANOGrav 15-year Gravitational-Wave Background
From a statistical-inference standpoint, the problem
of detecting nHz GWs in PTA data is analogous to
GW searches with terrestrial and future space-borne
experiments, in which the propagation of light between reference masses is modeled with physical and
phenomenological descriptions of signal and noise processes. It is distinguished by the irregular observation
times, which encourage a time- rather than Fourierdomain formulation, and by noise sources (intrinsic pulsar noise, interstellar-medium–induced radio-frequency–
dependent fluctuations, and timing-model errors) that
are correlated on timescales common to the GWs of interest. This requires the joint estimation of GW signals and noise, which is similar to the kinds of global
fitting procedures already used in terrestrial GW experiments, and proposed for space-borne experiments.
GW analysts have therefore converged on a Bayesian
framework that represents all noise sources as Gaussian
processes (van Haasteren et al. 2009; van Haasteren &
Vallisneri 2014), and relies on model comparison (i.e.,
Bayes factors, which are ratios of fully marginalized likelihoods) to define detection (see, e.g., Taylor 2021). This
Bayesian approach is nevertheless complemented by null
hypothesis testing, using a frequentist detection statistic1 (the “optimal statistic” of Anholm et al. 2009; Demorest et al. 2013; Chamberlin et al. 2015) averaged
over Bayesian posteriors of the noise parameters (Vigeland et al. 2018).
The GWB—rather than GW signals from individually resolved binary systems—is likely to become the
first nHz source accessible to PTA observations (Rosado
et al. 2015). Because of its stochastic nature, the GWB
cannot be identified as a distinctive phase-coherent signal in the way of individual compact-binary-coalescence
GWs. Rather, as PTA data sets grow in extent and
sensitivity one expects to first observe the GWB as excess low-frequency residual power of consistent amplitude and spectral shape across multiple pulsars (Romano et al. 2021; Pol et al. 2021). An observation following this behavior was reported in 2020 (Arzoumanian
et al. 2020, henceforth NG12gwb) for the 12.5-year data
set collected by the North American Nanohertz Observatory for Gravitational waves (NANOGrav, McLaughlin
2013; Ransom et al. 2019), and then confirmed (Goncharov et al. 2021a; Chen et al. 2021) by the Parkes
Pulsar Timing Array (PPTA, Manchester et al. 2013)
and the European Pulsar Timing Array (EPTA, Desvignes et al. 2016), following many years of null results
and steadily decreasing upper limits on the GWB am1 See Jenet et al. (2006) for an early example of a cross-correlation

statistic for PTA GWB detection.

5

plitude. A combined International Pulsar Timing Array (IPTA, Perera et al. 2019) data release consisting of
older data sets from the constituent PTAs also confirmed
this observation (Antoniadis et al. 2022). Nevertheless,
the finding of excess power cannot be attributed to a
GWB origin merely by the consistency of amplitude and
spectral shape, which could arise from intrinsic pulsar
processes of similar magnitude (Goncharov et al. 2022;
Zic et al. 2022), or from a common systematic noise such
as clock errors (Tiburzi et al. 2016). Instead, definitive
proof of GW origin is sought by establishing the presence of phase-coherent inter-pulsar correlations with the
characteristic spatial pattern derived by Hellings and
Downs (1983, henceforth HD): for an isotropic GWB,
the correlation between the GW-induced timing delays
observed at Earth for any pair of pulsars is a universal,
quasi-quadrupolar function of their angular separation
in the sky. Even though this correlation pattern is modified if there is anisotropy in the GWB—which may be
the case for a GWB generated by a SMBHB population
(Mingarelli et al. 2013; Taylor & Gair 2013; Cornish &
Sesana 2013; Mingarelli & Sidery 2014; Mingarelli et al.
2017; Roebber & Holder 2017)—the HD template is effective for detecting even anisotropic GWBs in all but
the most extreme scenarios (Cornish & Sesana 2013;
Cornish & Sampson 2016; Taylor et al. 2020; Bécsy et al.
2022; Allen 2023).
In this letter we present multiple lines of evidence
for an excess low-frequency signal with HD correlations
in the NANOGrav 15-year data set (Figure 1). Our
key results are as follows. The Bayes factor between
an HD-correlated, power-law GWB model and a spatially uncorrelated common-spectrum power-law model
ranges from 200 to 1,000, depending on modeling choices
(Figure 2). The noise-marginalized optimal statistic,
which is constructed to be selectively sensitive to HDcorrelated power, achieves a signal-to-noise ratio of ∼ 5
(Figure 3 and Figure 4). We calibrated these detection
statistics by removing correlations from the 15-year data
set using the phase-shift technique, which removes interpulsar correlations by adding random phase shifts to the
Fourier components of the common process (Taylor et al.
2017). We find false-alarm probabilities of p = 10−3 and
p = 5 × 10−5 for the observed Bayes factor and optimal
statistic, respectively (see Figure 3).
For our fiducial power-law model (f −2/3 for characteristic strain and f −13/3 for timing residuals) and a
log-uniform amplitude prior, the Bayesian posterior of
GWB amplitude at the customary reference frequency
−15
1 yr−1 is AGWB = 2.4+0.7
(median with 90%
−0.6 × 10
credible interval), which is compatible with current astrophysical estimates for the GWB from SMBHBs (e.g.,

## PDF page 6

6

The NANOGrav Collaboration

Burke-Spolaor et al. 2019; Agazie et al. 2023a). This corresponds to a total integrated energy density of Ωgw =
−9
−17
9.3+5.8
or ρgw = 7.7+4.8
ergs cm−3 (as−4.0 × 10
−3.3 × 10
suming H0 = 70 km/s/Mpc) in our sensitive frequency
band. For a more general model of the timing-residual
power spectral density with variable power-law exponent
+4.2
−γ, we find AGWB = 6.4−2.7
× 10−15 , and γ = 3.2+0.6
−0.6 .
See panel (b) of Figure 1 for AGWB and γ posteriors.
The posterior for γ is consistent with the value of 13/3
predicted for a population of SMBHBs evolving by GW
emission, although smaller values of γ are preferred;
however, the recovered posteriors are consistent with
predictions from astrophysical models (see Agazie et al.
2023a). We also note that, unlike our detection statistics
(which are calibrated under our modeling assumptions),
the estimation of γ is very sensitive to minor details in
the data model of a few pulsars.
The rest of this paper is organized as follows. We
briefly describe our data set and data model in §2. Our
main results are discussed in detail in §3 and §4; they
are supported by a variety of robustness and validation
studies, including a spectral analysis of the excess signal (§5.2), a correlation analysis that finds no significant evidence for additional spatially correlated processes (§5.3), and cross-validation studies with singletelescope data sets and leave-one-pulsar-out techniques
(§5.4). In the past two years we have performed an endto-end review of the NANOGrav experiment, to identify and mitigate possible sources of systematic error or
data set contamination: our improvements and considerations are partly described in a set of companion papers:
on the NANOGrav statistical analysis as implemented
in software (Johnson et al. 2023), on the 15-year data
set (Agazie et al. 2023b, hereafter NG15), and on pulsar
models (Agazie et al. 2023c, hereafter NG15detchar).
More companion papers address the possible SMBHB
(Agazie et al. 2023a) and cosmological (Afzal et al. 2023)
interpretations of our results, with several more GW
searches and signal studies in preparation. We look forward to the cross-validation analysis that will become
possible with the independent data sets collected by
other IPTA members.
2. THE 15-YEAR DATA SET AND DATA MODEL

The NANOGrav 15-year data set2 (NG15) contains observations of 68 pulsars obtained between July
2004 and August 2020 with the Arecibo Observatory
2 While the time between the first and last observations we analyze

is 16.03 years, this data set is named “15-year data set” since no
single pulsar exceeds 16 years of observation; we will use this
nomenclature despite the discrepancy.

(Arecibo), the Green Bank Telescope (GBT), and the
Very Large Array (VLA), augmenting the 12.5-year data
set (Alam et al. 2021a,b) with 2.9 years of timing data
for the 47 pulsars in the previous data set, and with
21 new pulsars3 . For this paper we analyze narrowband times of arrival (TOAs), which are computed separately for sub-bands of each receiver, and focus on
the 67 pulsars with a timing baseline ≥ 3 years. We
adopt the TT(BIPM2019) timescale and the JPL DE440
ephemeris (Park et al. 2021), which improves Jupiter’s
orbit with ranging and VLBI observations of the Juno
spacecraft. Uncertainties in the Jovian orbit impacted
NANOGrav’s 11-year GWB search (Arzoumanian et al.
2018; Vallisneri et al. 2020), but they are now negligible.
For each pulsar, we fit the TOAs to a timing model
that includes pulsar spin period, spin period derivative,
sky location, proper motion, and parallax. While not
all pulsars have measurable parallax and proper motion, we always include these parameters because they
induce delays with the same frequencies for all pulsars
(f = 0.5 yr−1 for parallax and f = yr−1 plus a linear envelope for proper motion), so there is a risk that
a parallax or proper motion signal could be misidentified as a GW signal. Fitting for these parameters in all
pulsars reduces our sensitivity to GWs at those frequencies; however, this effect is minimal for GWB searches
since these frequencies are much higher than the frequencies at which we expect the GWB to be significant. For binary pulsars, the timing model includes also
five orbital elements for binary pulsars and additional
non-Keplerian parameters when these improve the fit as
determined by an F test. We fit variations in dispersion measure as a piecewise constant “DMX” function
(Arzoumanian et al. 2015; Jones et al. 2017). The individual analysis of each pulsar provides best-fit estimates of the timing residuals δt, of white measurement
noise, and of intrinsic red noise, modeled as a power
law (Cordes 2013; Lam et al. 2017; Jones et al. 2017).4
White measurement noise is described by three parameters: a linear scaling of TOA uncertainties (“EFAC”),
white noise added to the TOA uncertainties in quadrature (“EQUAD”), and noise common to all sub-bands
at the same epoch (“ECORR”), with independent parameters for every receiver/backend combination (see
NG15detchar). We summarize white noise by its maximum a posteriori (MAP) covariance C. See App. A for
more details of our instruments, observations, and data3 The data set is available at data.nanograv.org with the code used

to process it.
4 Throughout the paper we use “red noise” to describe noise whose

power spectrum decreases with increasing frequency.

## PDF page 7

NANOGrav 15-year Gravitational-Wave Background
reduction pipeline: a complete discussion of the data set
can be found in NG15.
In our Bayesian GWB analysis, we model δt as a finite Gaussian process consisting of time-correlated fluctuations that include intrinsic red pulsar noise and (potentially) a GW signal, along with timing-model uncertainties (van Haasteren et al. 2009; van Haasteren &
Vallisneri 2014; Taylor 2021). The red noise is modeled with Fourier basis F and amplitudes c (Lentati
et al. 2013). All Fourier bases (the columns of F ) are
sines and cosines computed on the TOAs with frequencies fi = i/T , where T = 16.03 yr is the TOA extent. The timing-model uncertainties are modeled with
design-matrix basis M and coefficients ϵ. The singlepulsar log likelihood is then
ln p(δt|c, ϵ) = −
with

]
1 [ T −1
r C r + ln det (2πC) ,
2

r = δt − F c − M ϵ.

(1)

(2)

The prior for the ϵ is taken to be uniform with infinite
extent, so the posterior is driven entirely by the likelihood. The set of the {c} for all pulsars take a joint
normal prior with zero mean and covariance
⟨cai cbj ⟩ = δij (δab φai + Φab,i ) ;

(3)

here a, b range over pulsars and i, j over Fourier components; δij is Kronecker’s delta. The term φai describes the spectrum of intrinsic red noise in pulsar
a, while Φab,i describes processes with common spectrum across all pulsars and (potentially) phase-coherent
inter-pulsar correlations. The {c} prior ties together the
single-pulsar likelihoods (Equation 1) into a joint posterior, p(c, ϵ, η|δt) ∝ p(δt|c, ϵ)p(c, ϵ|η)p(η), where we
have dropped subscripts to denote the concatenation of
vectors for all pulsars, and where η denotes all the hyperparameters (such as red-noise and GWB power spectrum amplitudes) that determine the covariances. We
marginalize over c and ϵ analytically, and use Markov
chain Monte Carlo techniques (see App. B) to estimate
p(η|δt) for different models of the intrinsic red noise and
common spectrum.
The data-model variants adopted in this paper all
share this probabilistic setup, but differ in the structure and parametrization of Φab,i . For a model with
intrinsic red noise only (henceforth irn), Φab,i = 0;
for common-spectrum spatially-uncorrelated red noise
(curn), Φab,i = δab ΦCURN,i ; for an isotropic GWB with
Hellings–Downs correlations (hd), Φab,i = Γ(ξab )ΦHD,i ,
with Γ the Hellings–Downs function of pulsar angular

7

separations ξab
3
1
1 1
x ln(x) − x + + δab ,
2
4
2 2
1 − cos ξab
x=
.
2

Γ(ξab ) =

(4)
(5)

In NG12gwb we established strong Bayesian evidence for
curn over irn; finding that hd is preferred over curn
would point to the GWB origin of the common-spectrum
signal. We also investigate other spatial correlation patterns, e.g., monopole or dipole, introduced in §5.3.
Throughout this paper, we set the spectral components φai of intrinsic pulsar noise (which have units of
s2 , as appropriate for the variance of timing residuals)
to a power law,
(
)−γa
A2a 1 fi
−3
φai =
fref
,
(6)
12π 2 T fref
introducing two dimensionless hyperparameters for each
pulsar: the intrinsic-noise amplitude Aa and spectral
index γa . We use log-uniform and uniform priors, respectively, on these hyperparameters; their bounds are
described in App. B. More sophisticated intrinsic-noise
models are discussed in §5.1 and NG15detchar. In models curnγ and hdγ , the common spectra ΦCURN,i and
ΦHD,i follow Equation 6,
(
)−γCURN
A2CURN 1 fi
−3
fref
,
(7)
ΦCURN,i =
12π 2 T fref
(
)−γHD
A2 1 fi
−3
ΦHD,i = HD2
fref
,
(8)
12π T fref
introducing hyperparameters ACURN , γCURN and
AHD , γHD respectively. However, we set γHD = 13/3
for the GWB from a stationary ensemble of inspiraling
binaries, and refer to that fiducial model as hd13/3 . For
specific “free spectrum” studies we will instead model
the individual ΦCURN,i or ΦHD,i elements, and refer to
models curnfree and hdfree . Throughout this article we
use frequencies fi = i/T with i = 1–30 for intrinsic noise
(f = 2–59 nHz), covering a frequency range over which
pulsar noise transitions from red-noise–dominated to
white–noise-dominated. For common-spectrum noise,
we limit the frequency range in order to reduce correlations with excess white noise at higher frequencies.
Following NG12gwb, we fit a curnγ model enhanced
with a power-law break to our data, and limit frequencies to the MAP break frequencies (i = 1–14 or
f = 2–28 nHz; see App. C).
3. BAYESIAN ANALYSIS

When fit to the 15-year data set, the curnγ and hdγ
models agree on the presence of a loud time-correlated

## PDF page 8

8

The NANOGrav Collaboration
dipole

HDγ + dipole

< 10–7
intrinsic pulsar
noise only (IRN)

1012.1±0.1

commonspectrum red
noise (CURNγ)

0.48 ± 0.01
226 ± 70
(965 with 5 freqs.)

< 10–8

HD-correlated,
common spectrum
red noise (HDγ)

0.78 ± 0.09

HDγ + sin

0.6 ± 0.2
monopole

HDγ + monopole

Figure 2. Bayes factors between models of correlated red noise in the NANOGrav 15-year data set (see §5.3 and App. B). All
models feature variable-γ power laws. curnγ is vastly favored over irn (i.e., we find very strong evidence for common-spectrum
excess noise over pulsar intrinsic red-noise alone); hdγ is favored over curnγ (i.e., we find positive evidence for Hellings–Downs
correlations in the common-spectrum process); dipole and monopole processes are strongly disfavored with respect to curnγ ;
adding correlated processes to hdγ is disfavored. While the interpretation of “raw” Bayes factors is somewhat subjective, they
can be given a statistical significance within the hypothesis-testing framework by computing their background distributions and
deriving the p-values of the observed factors, e.g., Figure 3.

stochastic signal with common amplitude and spectrum across pulsars5 . The joint AHD – γHD Bayesian
posterior is shown in panel (b) of Figure 1, with 1-D
marginal posteriors in the horizontal and vertical subplots. The posterior medians and 5–95% quantiles are
+0.6
−15
AHD = 6.4+4.2
and γHD = 3.2−0.6
. The thicker
−2.7 × 10
curve in the vertical subplot is the AHD posterior for
+0.7
the hd13/3 model, for which AHD,13/3 = 2.4−0.6
× 10−15 .
These amplitudes are compatible with astrophysical expectations of a GWB from inspiraling SMBHBs (see
§6). The AHD posterior has essentially no support below
10−15 .
The strong AHD – γHD correlation is an artifact of using the conventional frequency fref = 1 yr−1 in Equation 6, and it largely disappears when fref is moved to
the band of greatest PTA sensitivity; see the dashed contours in panel (b) of Figure 1 for fref = (10 yr)−1 . The
γHD posterior is in moderate tension with the theoretical
universal binary-inspiral value γHD = 13/3, which lies at
the 99% credible boundary: smaller values of γHD could
be an indication that astrophysical effects, such as stellar
scattering and gas dynamics, play a role in the evolution
of SMBHBs emitting GWs in this frequency range (see
§6 and Agazie et al. 2023a). This highlights the importance of measuring this parameter. Furthermore, its estimation is sensitive to details in the modeling of intrinsic red noise and of interstellar-medium timing delays in
a few pulsars (see the analysis in §5.2). Notably, in the
12.5-year data set γHD = 13/3 was recovered at ∼ 1σ
below the median (NG12gwb); this anomaly is reversed
in the newer data set. It is likely that more expansive
5 See App. B for details about our Bayesian methods, including

the calculation of Bayes factors.

data sets or more sophisticated chromatic noise models,
e.g., next generation Gaussian process models such as
in §5.1 (Goncharov et al. 2021b; Chalumeau et al. 2022;
Lam et al. 2018), will be needed to infer the presence of
possible systematic errors in γHD .
Our Bayesian analysis provides evidence that the
common-spectrum signal includes Hellings–Downs interpulsar correlations. Specifically, the Bayes factor between the hdγ and curnγ models ranges from 200 (when
14 Fourier frequencies are included in Φi ) to 1,000 (when
5 frequencies are included, as in NG12gwb). Results
are similar for hd13/3 vs. curn13/3 . Figure 2 recapitulates Bayes factors between a variety of models, including some with the alternative spatial-correlation structures discussed in §5.3. The very peaked AHD posterior
in panel (b) of Figure 1, significantly separated from
smaller amplitudes, supports the very large Bayes factor between irn and curnγ . The 15-year data set favors hdγ over curnγ , and over models with monopolar
or dipolar correlations, and it is inconclusive about, i.e.,
gives roughly even odds for, the presence of spatially
correlated signals in addition to hdγ .
We can also regard the hdγ vs. curnγ Bayes factor as
a detection statistic in a hypothesis-testing framework,
and derive the p-value of the observed Bayes factor with
respect to its empirical distribution under the curnγ
model. We do so by computing Bayes factors on 5,000
bootstrapped data sets where inter-pulsar spatial correlations are removed by introducing random phase shifts,
drawn from a uniform distribution from 0 to 2π, to
the common-process Fourier components (Taylor et al.
2017). This procedure alters inter-pulsar correlations to
have a mean of zero, while leaving the amplitudes of intrinsic pulsar noise and CURN unchanged, thus provid-

## PDF page 9

9

NANOGrav 15-year Gravitational-Wave Background

100
1−CDF

10−1

2σ

2σ

3σ

3σ

10−2
10−3

Phase shifts

10−4

Phase shifts
Simulations
Analytic background

4σ

4σ

10−5
−4

−2

0
log10 BHD
CURN

2

4

−2

0
2
4
Noise-Marginalized Mean S/N

6

Figure 3. Empirical background distribution of hdγ -to-curnγ Bayes factor (left, see §3) and noise-marginalized optimal
statistic (right, see §4), as computed by the phase-shift technique (Taylor et al. 2017) to remove inter-pulsar correlations. We
only compute 5,000 Bayesian phase shifts, compared to 400,000 optimal statistic phase shifts, because of the huge computational
resources needed to perform the Bayesian analyses. For the optimal statistic, we also compute the background distribution using
27,000 simulations (orange line) and compare to an analytic calculation (green line). Dotted lines indicate Gaussian-equivalent
2σ, 3σ, and 4σ thresholds. The dashed vertical lines indicate the values of the detection statistics for the unshifted data sets.
For the Bayesian analyses, we find p = 10−3 (approx. 3σ); for the optimal statistic analyses, we find p = 5 × 10−5 –1.9 × 10−4
(approx. 3.5–4σ).

ing a way to test the null hypothesis that no inter-pulsar
correlations are present. The resulting background distribution of Bayes factors is shown in the left panel of
Figure 3—they exceed the observed value in five of the
5,000 phase shifts (p = 10−3 ). We also performed sky
scramble analyses (Cornish & Sampson 2016), which
remove the dependence of inter-pulsar spatial correlations on the angular separations between the pulsars by
attributing random sky positions to the pulsars. Sky
scrambles generate a background distribution for which
inter-pulsar correlations are present in the data but they
are independent of the pulsars’ angular separations: for
this distribution, we find p = 1.6 × 10−3 . A detailed discussion of sky scrambles and the results of these analyses
can be found in App. F.
As in NG12gwb, we also carried out a minimally modeled Bayesian reconstruction of the inter-pulsar correlation pattern, using spline interpolation over seven splineknot positions. The choice of seven spline-knot positions is based on features of the Hellings–Downs pattern:
two correspond to the maximum and minimum angular
separations (0◦ and 180◦ , respectively), two are chosen
to be at the theoretical zero crossings of the Hellings–
Downs pattern (49.2◦ and 121.8◦ ), one is at the theoretical minimum (82.5◦ ), and the final two are between
the end points and zero crossings (25◦ and 150◦ ) to allow additional flexibility in the fit. Panel (d) of Figure 1 shows the marginal 1-D posterior densities at these
spline-knot positions for a power-law varied-exponent
model. The reconstruction is consistent with the overplotted Hellings–Downs pattern; furthermore, the joint
2-D marginal posterior densities for the knots, not shown

in panel (d) of Figure 1, at the HD zero-crossings is consistent with (0, 0) within 1σ credibility.
4. OPTIMAL STATISTIC ANALYSIS

We complement our Bayesian search with a frequentist analysis using the optimal statistic (Anholm et al.
2009; Demorest et al. 2013; Chamberlin et al. 2015), a
summary statistic designed to measure correlated excess
power in PTA residuals. (Note that there is no accepted
definition of “optimal statistic” in modern statistical usage, but the term has become established in the PTA
literature to refer to this specific method, so we use it
for this reason.) It is enlightening to describe the optimal statistic as a weighted average of the inter-pulsar
correlation coefficients
ρab =

−1
δtTa P−1
a Φ̃ab Pb δtb
−1
Tr P−1
a Φ̃ab Pb Φ̃ba

,

(9)

T
where
δt
⟨
⟩ a are the residuals of pulsar a, and Pa =
T
δta δta is their total auto-covariance matrix. The
cross-covariance matrix Φ̃ab encodes the spectrum of
the HD-correlated signal, normalized so that Φab =
A2 Γ(ξab )Φ̃ab (see Pol et al. 2022), and where elements
of Φab are given by Equation 3. Indeed, the ρab have
2
expectation value A2 Γ(ξab ), but their variance σab
=
−1
−1
−1
4
(Tr Pa Φ̃ab Pb Φ̃ba ) + O(A ) is too large to use them
directly as estimators. Thus we assemble the optimal
statistic as the variance-weighted, Γ-template-matched
average of the ρab ,
∑
2
ρab Γ(ξab )/σab
2
Â = ∑a>b 2
(10)
2 .
a>b Γ (ξab )/σab

## PDF page 10

10

The NANOGrav Collaboration
Varied γ
γ = 13/3

0.4

PDF

0.3
0.2
0.1
0.0

2

4

6
S/N

8

10

Figure 4. Optimal statistic S/N for HD correlations, distributed over curnγ (solid lines) and curn13/3 (dashed lines)
noise-parameter posteriors. The vertical lines indicate the
mean S/Ns. We find S/Ns of 5 ± 1 and 4 ± 1 for curnγ and
curn13/3 , respectively.

This equation represents the optimal estimator of the
HD amplitude A2 ; it can also be interpreted as the
best-fit Â2 obtained by least-squares–fitting the ρab to
the Hellings–Downs model Â2 Γ(ξab ). Because Â2 is a
function of intrinsic–red-noise and common-process hyperparameters through the Pa , we use the results of
an initial Bayesian-inference run to refer the statistic to
MAP hyperparameters, or to marginalize it over their
posteriors. As discussed in Vigeland et al. (2018), we
obtain more accurate values of the amplitude by this
marginalization.
To search for inter-pulsar correlations using the optimal statistic, we evaluate the frequency (the p-value)
with which an uncorrelated common-spectrum process
with parameters estimated from our data set would yield
Â2 greater than we observe. In the absence of a signal,
the expectation value of Â2 is zero, and its distribution
is approximately normal. Thus we divide the observed
Â2 by its standard deviation to define a formal signalto-noise ratio
∑
2
ρab Γ(ξab )/σab
S/N = [∑ a>b
.
(11)
]
2 1/2
2
a>b Γ (ξab )/σab

Figure 4 shows the distribution of this S/N over curnγ
and curn13/3 noise-parameter posteriors, with S/Ns of
5 ± 1 and 4 ± 1, respectively (means ± standard deviations across noise-parameter posteriors). We use 14
frequency components to model the signal: the dependence on the number of frequency components is very
weak.
Because the distribution of Â2 is only approximately
normal (Hazboun et al. 2023), the S/N of Equation 11
does not map analytically to a p-value, and it cannot
be interpreted as a “sigma” level. Instead, optimalstatistic p-values can be computed empirically by re-

moving inter-pulsar correlations from the 15-year data
set with phase shifts (Taylor et al. 2017). We draw random phase offsets from 0 to 2π for the common-process
Fourier components, which is equivalent to making uniform draws from the background distribution of CURN,
and ask how often a random choice of phase offsets
produces a HD-correlated signal. The right panel of
Figure 3 shows the distribution of noise-marginalized
S/N over 400,000 phase shifts. There are 19 phase
shifts with noise-marginalized S/N greater than observed, with p = 5 × 10−5 . We compare the phase-shift
distribution with backgrounds obtained by simulation
(right panel of Figure 3, orange line) and analytic calculation (green line). For the former, we simulate 27,000
curnγ realizations using MAP hyperparameters from
the 15-yr data and compute the optimal-statistic S/N for
each; for the latter, we evaluate the generalized χ2 distribution (Hazboun et al. 2023) with median curnγ hyperparameters. Although neither method includes the
marginalization over noise-parameter posteriors, we find
good agreement with phase shifts, with p = 1.8 × 10−4
from simulations, and p = 1.9 × 10−4 from the analytic
calculation. Finally, we use sky scrambles to compute
the p-value for the null hypothesis that inter-pulsar correlations are present, but they have no dependence on
the angular separation between the pulsars, for which
we find p < 10−4 (see App. F).
Averaging the cross-correlations ρab in angularseparation bins with equal numbers of pulsar pairs reveals the Hellings–Downs pattern, as shown in panel
(c) of Figure 1 for 15 bins. The ρab were evaluated with MAP curn13/3 noise parameters. The black
dashed curve traces the expected correlations for an HDcorrelated background with the MAP amplitude; the
vertical error bars display the expected 1σ spreads of the
binned cross-correlations, accounting for the ⟨ρab ρcd ⟩
covariances induced by the HD-correlated process (Romano et al. 2021; Allen & Romano 2022). (Neglecting
those covariances yields 20–40% smaller spreads. Note
that they are not included in p-value estimates because
those are calculated under the null hypothesis of no spatially correlated process.)
Although each draw from the noise-parameter posterior would generate a slightly different plot, as would
different binnings, the quality of the fit seen in Figure 1 provides a visual indication that the excess lowfrequency power in the 15-year data set harbors HD
correlations. The χ2 for this 15-bin reconstruction with
respect to the Hellings–Downs curve is 8.1, where we account for ρab covariance in constructing the bins, and the
covariance between bins in constructing the χ2 (Allen &
Romano 2022). This corresponds to a p-value of 0.75,

## PDF page 11

11

5.1. Alternative DM models
In this paper and in previous GW searches (e.g.,
NG12gwb), we model fluctuations in the DM using
DMX parameters (a piecewise-constant representation,
see NG15). Adopting this DM model as the standard
makes it easier to directly compare the results here to
those in NG12gwb. An alternative model where DM
variations are modeled as a Fourier-domain Gaussian
process, DMGP, has been used by Antoniadis et al.
(2022), Chen et al. (2021), and Goncharov et al. (2021a).
The Fourier coefficients follow a power law similar to
those of intrinsic and common-spectrum red noise, but
their basis vectors include a ν −2 radio-frequency dependence, and the component frequencies fi = i/T range
through i = 1–100. Under the DMGP model we also include a deterministic solar-wind model (Hazboun et al.
2022) and the two chromatic events in PSR J1713+0747
reported in Lam et al. (2018) which are modeled as deterministic exponential dips with the chromatic index
quantifying the radio-frequency dependence of the dips
left as a free parameter. If these chromatic events are
not modeled, they raise estimated white noise (Hazboun
et al. 2020). A detailed discussion of chromatic noise effects can be found in NG15detchar.
Using the DMGP model in place of DMX has minimal
effects on nearly all pulsars in the array. Only PSRs
J1713+0747 and J1600−3053 show notable differences
in their recovered intrinsic-noise parameters. However,
DMGP does affect the parameter estimation of common
red noise, as seen in Figure 5, shifting the posterior for

4.
8

4.
0

3.
2

Prior to analyzing the 15-year data set, we extensively
reviewed our data collection and analysis procedures,
methods, and tools, in an effort to eliminate contamination from systematic effects and human error. Furthermore, the results presented in §3 and §4 are supported
by a variety of consistency checks and auxiliary studies. In this section we present those that offer evidence
for or against the presence of HD correlations, reveal
anomalies, or otherwise highlight features of note in the
data: alternative DM modeling (§5.1), the spectral content (§5.2) and correlation pattern (§5.3) of the excessnoise signal, as well as the consistency of our findings
across data set “slices,” pulsars, and telescopes (§5.4).

DMX
DMGP

2.
4

5. CHECKS AND VALIDATION

log10 ACURN

calculated using simulations based on the hdγ model, or
0.92 if one assumes this value follows a canonical χ2 with
15 degrees of freedom. These p-values are representative
of what we find with different binnings: we find p > 0.3
when using eight to 20 bins (assuming a canonical χ2
distribution).

−
−
−
−
14
14
14
13
.8
.4
.0
.6

NANOGrav 15-year Gravitational-Wave Background

γCURN
γ

Figure 5. curn posterior distributions using DMGP (red)
and DMX (blue) to model DM variations. The dashed line
marks γCURN = 13/3. While the posteriors are broadly consistent, DMGP shifts the γCURN posterior to higher values,
making it more consistent with γCURN = 13/3.

γ to higher values that are more consistent with 13/3.
Despite this, we still recover HD correlations at the same
significance as when we use DMX to model fluctuations
in the DM, implying that the evidence reported for the
presence of correlations in this work is independent of
the choice of DM noise modeling.
5.2. Spectral analysis
Adopting power-law spectra for curn and hd is a
useful simplification that reduces the number of fit parameters and yields more informative constraints; furthermore, it is expedient to identify hd13/3 with the
hypothesis that we are observing the GWB from SMBHBs. Nevertheless, the standard γ = 13/3 power law
for GW inspirals may be altered by astrophysical processes such as stellar and gas friction in nuclei (see, e.g.,
Merritt & Milosavljević 2005 for a review), by appreciable eccentricity in SMBHB orbits (Enoki & Nagashima
2007), and by low-number SMBHB statistics (Sesana
et al. 2008). hdγ parameter recovery may also be biased
if intrinsic pulsar noise is not modeled well by a power
law. Indeed, our data show hints of a discrepancy from
the idealized hd13/3 model: the γHD posterior in panel
(b) of Figure 1 favors slopes much shallower than 13/3,
and the hdγ -to-curnγ Bayes factor drops from 1,000 to
200 when Fourier components at more than five frequencies are included in the model.
We examine the spectral content of the 15-year data
set using the curnfree and hdfree models, which are
parametrized by the variances of the Fourier components
at each frequency. Their marginal posteriors are shown
in the left panel of Figure 6, where bin number i corresponds to fi = i/T , with T = 16.03 yr the extent of
the data set. For the purpose of illustration, we overlay
best-fit power laws that thread the posteriors in a way

## PDF page 12

12

The NANOGrav Collaboration

i =1 2

3

4

5

6

7

8

9

10

11

12

13

14

CURN
HD
monopole
dipole

best fit (γ = 3.2)
−7

log10

√

Φi / s2

−6

−8
CURN
HD

−9
0.0

best fit fixing γ = 13/3
0.2

0.4
f [1/yr]

0.6

0.8

−9

−8

log10

√

−7

Φ2

/ s2

−6

Figure 6. Left: Posteriors of Fourier component variance Φi for the curnfree (left) and hdfree (right) models (see §2), plotted
at their corresponding frequencies fi = i/T with T the 16.03-yr extent of the data set. Excess power is observed in bins 1–8
(somewhat marginally in bin 6); Hellings–Downs-correlated power in bins 1–5 and 8. The dashed line plots the best-fit power
law, which has γ ≃ 3.2 (as in panel (d) of Figure 1); the fit is pushed to lower γ by bins 1 and 8. The dotted line plots the best-fit
power law when γ is fixed to 13/3; it overshoots in bin 1 and undershoots in bin 8. Right: Posteriors of variance Φ2 in Fourier
bin 2 (f2 = 3.95 nHz) in a curnfree + hdfree + monopolefree + dipolefree model, showing evidence of a quasi-monochromatic
monopole process (dashed). No monopole or dipole power is observed in all other bins of that joint model, with ΦCURN,i and
ΦHD,i posteriors consistent with the left panel.

similar to the factorized PTA likelihood of Taylor et al.
(2022) and Lamb et al. (2023).
We deem excess power, either uncorrelated for
curnfree or correlated for hdfree , to be observed in a
bin when the support of the posterior is concentrated
away from the lowest amplitudes. No power of either
kind is observed above f8 , consistent with the presence
of a floor of white measurement noise. Furthermore,
no correlated power is observed in bins 6 and 7, where a
power-law model would expect a smooth continuation of
the trend of bins 1–5 (cf. the dashed fit of Figure 6): this
may explain the drop in the Bayes factor. However, correlated power reappears in bin 8, pushing the fit toward
shallower slopes. Indeed, repeating the fit by omitting
subsets of the bins suggests that the low recovered γHD
is due mostly to bin 8 and to the lower-than-expected
correlated power found in bin 1. Obviously, excluding
those bins leads to higher γHD estimates.
To explore deviations from a pure power law that may
arise from statistical fluctuations of the astrophysical
background or from unmodeled systematics (perhaps related to the timing model), in App. D we relax the normal ck prior (cf. Equation 3) to a multivariate Student’s
t-distribution that is more accepting of mild outliers.
The resulting estimate of γCURN peaks at a higher value
and is broader than in curnγ , with posterior medians
and 5-95% quantiles of γCURN = 3.5+1.0
−1.0 .
Similarly, spectral turnovers due to interactions between SMBHBs and their environments can result in
reduced GWB power at lower frequencies, which might
explain the slightly lower correlated power in bin 1. We
investigate this hypothesis in App. E using the turnover

spectrum of Sampson et al. (2015). For this curnturnover
model, the 15-year data favor a spectral bend below 10
nHz (near f5 ), but the Bayes factor against the standard
hdγ is inconclusive.
Future data sets with longer time spans and the comparison of our data set with those of other PTAs should
help clarify the astrophysical or systematic origin of
these possible spectral features.
5.3. Alternative correlation patterns
Sources other than GWs can produce inter-pulsar
residual correlations with spatial patterns other than
HD. For example, errors in the solar-system ephemerides
create time-dependent Roemer delays with dipolar correlations (Roebber 2019; Vallisneri et al. 2020), and errors in the correction of telescope time to an inertial
timescale (Hobbs et al. 2012, 2020) create an identical
time-dependent delay for all pulsars (i.e., a delay with
monopolar correlations).
Gair et al. (2014) showed that, for a pulsar array distributed uniformly across the sky, HD correlations can
be decomposed as
ΓHD,ab =

∞
∑

gl Pl (cos ξab ),

l=0

g0 = 0, g1 = 0, gl =

3
(l − 2)!
(2l + 1)
for l ≥ 2, (12)
2
(l + 2)!

where the Pl (cos ξab ) are Legendre polynomials of order
l evaluated at the pulsar angular separation ξab . In other
words, a HD-correlated signal should have no power at
l = 0 or l = 1.

## PDF page 13

NANOGrav 15-year Gravitational-Wave Background

Figure 7. Multiple-component optimal statistic for a Legendre polynomial basis (Equation 12) with with lmax = 5. The
violin plots show the distributions of the normalized Legendre coefficients A2l = A2 gl over curnγ noise-parameter posteriors. The black dashed line shows the Legendre spectrum
of a pure-HD signal, with the median posterior Â2HD .

We can perform a frequentist generic correlation
search using Legendre polynomials6 with the multiplecomponent optimal statistic (MCOS; Sardesai & Vigeland 2023)—a generalized statistic that allows multiple
correlation patterns to be fit simultaneously to the correlation coefficients ρab . Figure 7 shows the constraints
on A2l = A2 gl obtained by fitting the correlations ρab to
this Legendre series using the MCOS and marginalizing
over curnγ noise-parameter posteriors. The quadrupolar structure of the data is evident, along with a small
but significant monopolar contribution.
The same feature from the Legendre decomposition
appears if we use the MCOS to search for multiple correlations simultaneously: a multiple regression analysis favors models that contain both significant HD and
monopole correlations (see App. G). From simulations
of 15-year-like data sets (see App. H.1), we find a pvalue of 0.11 (approx. 2σ) for observing a monopole at
this significance or higher with a pure-HD injection of
amplitude similar to what we observe. We also perform a model-checking study to assess whether the observed monopole is consistent with the hd13/3 model
(see App. H.2), and we find a p-value of 0.11 for producing an apparent monopole when the signal is purely
hd13/3 . Thus, we conclude that it is possible for a HDcorrelated signal to appear to have monopole correlations in an optimal statistic analysis at this significance
level.
6 A Bayesian method for fitting correlations using Legendre poly-

nomials can be found in Nay et al. (2023).

13

In contrast, Bayesian searches for additional correlations do not find evidence of additional monopole- or
dipole-correlated red noise processes: as shown in Figure 2, the Bayes factors for these processes are ∼ 1. We
also perform a general Bayesian search for correlations
using a curnfree + hdfree + monopolefree + dipolefree
model, which allows for independent uncorrelated and
correlated components at every frequency bin. We note
that this analysis is more flexible than the ones described
above, which assume a power-law power spectral density. We find no significant dipole-correlated power at
any frequency, and we find monopole-correlated power
only in the second frequency bin (f2 = 3.95 nHz); posteriors of variance for that bin are shown in the right
panel of Figure 6.
Motivated by this finding, we perform a search for hdγ
+ sinusoid, which includes a deterministic sinusoidal
delay (applied to all pulsars alike, as appropriate for a
monopole) with free frequency, amplitude, and phase.
The sinusoid’s posteriors match the free-spectral analysis in frequency and amplitude; however, the Bayes factor between hdγ + sinusoid and hdγ calculated using
two methods (Hee et al. 2015; Hourihane et al. 2023),
is only ∼ 1, so the signal cannot be considered statistically significant. Astrophysically motivated searches
for sources that produce sinusoidal or sinusoid-like delays in the residuals, such as an individual SMBHB or
perturbations to the local gravitational field induced by
fuzzy dark matter (Khmelnitsky & Rubakov 2014), also
yield Bayes factors ∼ 1. Thus we conclude that there
is some evidence of additional power at 3.95 nHz with
monopole correlations; however, the significance in the
Bayesian analyses is low, while the optimal-statistic S/N
could be produced by a HD-correlated signal. Therefore, we cannot definitively say whether the signal is
present, or determine the source. We note that performing an MCOS analysis after subtracting off realizations of a sinusoid using hdγ + sinusoid posteriors reduces the (S/N)monopole ≃ 0 while (S/N)HD remains unchanged, indicating that this single-frequency
monopole-correlated signal is likely causing the nonzero
monopole signal observed in the MCOS analysis.
Similar hints of a monopolar signal (though weaker)
were found in the NANOGrav 12.5-year data set, unsurprisingly given that it is a subset of the current data set.
To exercise due diligence, we audited the correction of
telescope time to GPS time at the Arecibo Observatory
and at the Green Bank Telescope, and found nothing
that could explain our observations. The subsequent
steps in the time-correction pipeline rely on very accurate atomic clocks and are unlikely to introduce considerable systematics (Petit 2022). An important test will

## PDF page 14

14

The NANOGrav Collaboration

5.4. Dropout and cross-validation
The GWB is by its nature a signal affecting all of the
pulsars in the PTA, although it may appear more significant in some based on their observing time span, noise
properties, and on the particular realization of pulsar
and Earth contributions (Speri et al. 2023). One way
to assess the significance of the GWB in each pulsar is
a Bayesian dropout analysis (Aggarwal et al. 2019; Arzoumanian et al. 2020), which introduces a binary parameter that turns on and off the common signal (or its
inter-pulsar correlations) for a single pulsar, leaving all
other pulsars unchanged. The Bayes factor associated
with this parameter, also referred to as the “dropout
factor,” describes how much each pulsar likes to “participate” in the common signal.
Figure 8 plots curnγ vs. irn dropout factors for all
67 pulsars (blue). We find positive dropout factors (i.e.,
dropout factors > 2) for an uncorrelated common process in twenty pulsars, while only one has a dropout
factor < 0.5. For comparison, in the NANOGrav 12.5year data set ten pulsars showed positive dropout factors for an uncorrelated common process, while three
had negative dropout factors. We also show HD correlations vs. curnγ dropout factors (orange). For these,
the uncorrelated common process is always present in
all pulsars, but the cross-correlations for all pulsar pairs
involving a given pulsar may be dropped from the likelihood. We find positive factors for HD correlations vs.
curnγ in seven pulsars, while three are negative. We
expect more pulsars to have positive dropout factors for
curnγ vs. irn than for Hellings–Downs vs. curnγ because the Bayes factor comparing the first two models
is significantly higher than the one comparing the second two models (see Figure 2). Negative dropout factors
could be caused by noise fluctuations or they could be
an indication that more advanced chromatic noise modeling is necessary (Alam et al. 2021a). They could also
be caused by the GWB itself, which induces both correlated and uncorrelated noise in the pulsars (the so-called
“Earth terms” and “pulsar terms”; Mingarelli & Mingarelli 2018).
In addition to Bayes factors, the goodness-of-fit of
probabilistic models can be evaluated by assessing their
predictive performance (Gelman et al. 2013). Specifically, given that the GWB is correlated across pulsars,
we can (partially) predict the timing residuals δta of

Observation Span [yrs]

be whether this signal persists in future data sets. If this
monopolar feature is a truly an astrophysical signal, we
would expect it to increase in significance as our data
set grows. Comparisons with other PTAs and combined
IPTA data sets will also provide crucial insight.
15

10

5
−0.5

Dropout factors, CURN
Dropout factors, HD correlations

0.0
0.5
log10 (Dropout Factor)

1.0

Figure 8. Support for curnγ (blue) and hdγ correlations
(orange) in each pulsar, as measured by a dropout analysis. Dropout factors greater than 1 indicate support for the
curnγ or hdγ while those less than 1 show that the pulsar
disfavors it. We find significant spread in the dropout factors
among pulsars with long observation times, but overall more
pulsars favor curnγ participation and hdγ correlations than
disfavor them.

pulsar a from the residuals δt−a of all other pulsars by
way of the “leave-one-out” posterior predictive likelihood
(PPL)
∫
p(δta |δt−a ) = dθa p(δta |θa ) p(θa |δt−a ),
(13)
where θa are all the parameters and hyperparameters
that affect pulsar a in a given model. As discussed in
Meyers et al. (2023), we compare the predictive performance of curn13/3 and hd13/3 for each pulsar in turn
by taking the ratio of the corresponding leave-one-out
PPLs. These ratios are closely related to the dropout
factors plotted in Figure 8. Multiplying the PPL ratios
for all pulsars yields the pseudo Bayes factor (PBF).
For the 15-year data set we find PBF15 yr = 1,400 in
favor of hd13/3 over curn13/3 . The PBF does not have
a “betting odds” interpretation, but we obtain a crude
estimate of its significance by building its background
distribution on 40 curn13/3 simulations with the MAP
log10 ACURN inferred from the 15-year data set. For all
simulations except one, the PBF favors the null hypothesis, and log10 PBF15 yr is displaced by approx. three
standard deviations from the mean log10 PBF.
A different sort of cross-validation relies on evaluating
the optimal statistic for temporal subsets of the data
set, as in Hazboun et al. (2020). In the regime where

## PDF page 15

15

NANOGrav 15-year Gravitational-Wave Background
HD S/N

−2

Number of pulsars

6.0

8.0

10.0
12.0
Years in data set

14.0

20

16.0

Entire PTA
AO only
GBT only

5

30

4

0

3

40

2

2

1

50

log10 ACURN

4

−
−
−
−
15
1
1
1
.0 4.5 4.0 3.5

60
Npsrs

S/N

6

γCURN
γ

Figure 9. S/N growth as a function of time and number of
pulsars. As we move from left to right we add an additional
six months of data at each step. New pulsars are added
when they accumulate three years of data. The blue violin
plot shows the distribution of the optimal statistic S/N over
curnγ noise parameters. The dashed orange line shows the
number of pulsars used for each time slice.

the lowest frequencies of our data are dominated by the
GWB, the optimal statistic S/N should grow with the
square root of the time span of the data and linearly
with the number of pulsars in the array (Siemens et al.
2013); in this regime increasing the number of pulsars is
the best way to boost PTA sensitivity to the GWB. To
verify that this is indeed the case, we analyze “slices”
of the data set in six-month increments, starting from
a six-year data set. Once a new pulsar accumulates
three years of data, we add it to the array. We perform a separate Bayesian curnγ analysis for each slice
and calculate the Hellings–Downs optimal statistic over
the noise-parameter posterior. In Figure 9, we plot the
S/N distributions against time span and the number of
pulsars. As expected, we observe essentially monotonic
growth associated with the increase in the number of
pulsars.
The signal should also be consistent between timing observations made with Arecibo and GBT. To test
this, we analyze the two split-telescope data sets (see
App. A); both show evidence of common-spectrum excess noise. Figure 10 shows Arecibo (orange) and GBT
(green) curnγ posteriors, which are broadly consistent
with each other and with full-data posteriors (blue).
+0.18
Arecibo yields log10 A = −14.02−0.22
and γ = 2.78+0.70
−0.64
(medians with 68% credible intervals), while GBT yields
+0.15
log10 A = −14.2−0.17
and γ = 3.37+0.40
−0.38 .
The split-telescope data sets are significantly less sensitive to spatial correlations than the full data set, because they have fewer pulsars and therefore pulsar pairs
(see Figure 12 of App. A). Nevertheless, we can search
them for spatial correlations using the optimal statistic. We find a noise-marginalized Hellings–Downs S/N

Figure 10. curn posterior distributions for Arecibo (orange) and GBT (green) split-telescope data sets, and for the
full data set (blue). The dashed line marks γCURN = 13/3.
The posteriors for the split-telescope data sets are consistent
with each other and with the posteriors for the full data set.

of 2.9 for Arecibo and 3.3 for GBT, consistent with the
split-telescope data sets having about half the number
of pulsars as the full data set. The S/Ns for Arecibo
and GBT are comparable: while telescope sensitivity,
observing cadence, and distribution of pulsars all affect
GWB sensitivity, the dominant factor is the number of
pulsars because the S/N scales linearly with the num√
ber of pulsars but only as ∝ (σ c)−1/γ , where σ is the
residual root-mean-squared, and c is the observing cadence (Siemens et al. 2013). We also note that the distributions of angular separations probed by Arecibo and
GBT are similar, although GBT observes more pulsar
pairs with large angular separations (see Figure 12).
6. DISCUSSION

In this letter we have reported on a search for an
isotropic stochastic GWB in the 15-year NANOGrav
data set.
A previous analysis of the 12.5-year
NANOGrav data set found strong evidence for excess low-frequency noise with common spectral properties across the array, but inconclusive evidence for
Hellings–Downs inter-pulsar correlations, which would
point to the GW origin of the background. By contrast, the 12.5-year data disfavored purely monopolar (clock-error–like) and dipolar (ephemeris-error–like)
correlations. Subsequent independent analyses by the
PPTA and EPTA collaborations reported results consistent with ours (Goncharov et al. 2021a; Chen et al.
2021), as did the search of a combined data set (Antoniadis et al. 2022)—a syzygy of tantalizing discoveries
that portend the rise of low-frequency GW astronomy.
We analyzed timing data for 67 pulsars in the 15-year
data set (those that span > 3 years), with a total time
span of 16.03 years, and more than twice the pulsar pairs
than in the 12.5-year data set. The common-spectrum
stochastic signal gains even greater significance and is

## PDF page 16

16

The NANOGrav Collaboration

detected in a larger number of pulsars. For the first time,
we find compelling evidence of Hellings–Downs interpulsar correlations, using both Bayesian and frequentist detection statistics (see Figure 1), with false-alarm
probabilities of p = 10−3 and p = 5 × 10−5 –1.9 × 10−4 ,
respectively (see Figure 3).
The significance of Hellings–Downs correlations increases as we increase the number of frequency components in the analysis up to five, indicating that the
correlated signal extends over a range of frequencies.
A detailed spectral analysis supports a power-law signal, but at least two frequency bins show deviations
that may skew the determination of spectral slope (Figure 6). These discrepancies may arise from astrophysical or systematic effects. Furthermore, slope determination changes significantly using an alternative DM
model (Figure 5). The study of spatial correlations with
the optimal statistic confirms a Hellings–Downs quasiquadrupolar pattern (Figure 7 and panel c of Figure 1),
with some indications of an additional monopolar signal
confined to a narrow frequency range near 4 nHz. However, the Bayesian evidence for this monopolar signal is
inconclusive, and we could not ascribe it to any astrophysical or terrestrial source (e.g., an individual SMBHB
or errors in the chain of timing corrections).
The GWB is a persistent signal that should increase in
significance with number of pulsars and observing time
span. This is indeed what we observe by analyzing slices
of the data set (see Figure 9). Furthermore, the signal is
present in multiple pulsars (Figure 8), and can be found
in independent single-telescope data sets (Figure 10).
We are preparing a number of other papers searching
the 15-year data set for stochastic and deterministic signals, including an all-sky, all-frequency search for GWs
from individual circular SMBHBs. This search, together
with the same analysis of the 12.5-year data set (Arzoumanian et al. 2023), indicates that the spectrum and
correlations we observe cannot be produced by an individual circular SMBHB.
If the Hellings–Downs-correlated signal is indeed an
astrophysical GWB, its origin remains indeterminate.
Among the many possible sources in the PTA frequency
band, numerous studies have focused on the unresolved
background from a population of close-separation SMBHBs. The SMBHB population is a direct byproduct
of hierarchical structure formation, which is driven by
galaxy mergers (e.g., Blumenthal et al. 1984). In a
post-merger galaxy, the SMBHs sink to the center of
the common merger remnant through dynamical interactions with their astrophysical environment, eventually
leading to the formation of a binary (Begelman et al.
1980). GW emission from a SMBHB at nHz frequencies

is quasi-monochromatic because the binaries evolve very
slowly. Under the assumption of purely GW-driven binary evolution, the expected characteristic-strain spectrum is ∝ f −2/3 (or f −13/3 for pulsar-timing residuals).
The GWB spectrum may also feature a low-frequency
turnover induced by the dynamical interactions of binaries with their astrophysical environment (e.g., with
stars or gas, see Armitage & Natarajan 2002; Sesana
et al. 2004; Merritt & Milosavljević 2005) or possibly by
non-negligible orbital eccentricities persisting to small
separations (Enoki & Nagashima 2007). We find little
support for a low-frequency turnover in our data (see
App. E).
The GWB amplitude is determined primarily by
SMBH masses and by the occurrence rate of close binaries, which in turn depends on the galaxy merger
rate, the occupation fraction of SMBHs, and the binary
evolution timescale; population models predict amplitudes ranging over more than an order of magnitude
(Rajagopal & Romani 1995; Wyithe & Loeb 2003; Jaffe
& Backer 2003; McWilliams et al. 2014; Sesana 2013),
under a variety of assumptions. Figure 11 displays a
comparison of hdγ parameter posteriors with power-law
spectral fits from an observationally constrained semianalytic model of the SMBHB population constructed
with the holodeck package (Kelley et al. 2023). This
particular set of SMBHB populations assumes purely
GW-driven binary evolution, and uses relatively narrow distributions of model parameters based on literature constraints from galaxy-merger observations (see,
e.g., Tomczak et al. 2014). While the amplitude recovered in our analysis is consistent with models derived
directly from our understanding of SMBH and galaxy
evolution, it is toward the upper end of predictions implying a combination of relatively high SMBH masses
and binary fractions. A detailed discussion of the GWB
from SMBHBs in light of our results is given in Agazie
et al. (2023a).
In addition to SMBHBs, more exotic cosmological
sources such as inflation, cosmic strings, phase transitions, domain walls, and curvature-induced GWs can
also produce detectable GWBs in the nHz range (see,
e.g., Guzzetti et al. 2016; Caprini & Figueroa 2018, and
references therein). Similarities in the spectral shapes of
cosmological and astrophysical signals make it challenging to determine the origin of the background from its
spectral characterization (Kaiser et al. 2022). The question could be settled by the detection of signals from
individual loud SMBHBs or by the observation of spatial anisotropies, since the anisotropies expected from
SMBHBs are orders of magnitude larger than those produced by most cosmological sources (Caprini & Figueroa

## PDF page 17

NANOGrav 15-year Gravitational-Wave Background

−
14
.4

−
13
.6

ACKNOWLEDGMENTS

−
15
.2

log10 AGWB

4.
8

4.
2

3.
6

3.
0

NANOGrav 15-year
holodeck Sims

2.
4

−
16
.0
−
16
.8

17

γGWB
Figure 11. Posteriors of hd amplitude (for fref = 1 yr−1 )
and spectral slope for the 15-year data set (blue), compared
to power-law fits to simulated GWB spectra (red, dashed)
from a population of SMBHBs generated by holodeck (Kelley et al. 2023) under the assumption of purely GW-driven
binary evolution, and narrowly distributed model parameters based on galaxy merger-observations. We show 1/2/3σ
regions, and the dashed line indicates γ = 13/3. The broad
contours confirm that population variance can lead to a significant spread of spectral characteristics.
γ

2018; Bartolo et al. 2022). We discuss these models in
the context of our results in Afzal et al. (2023).
The EPTA and Indian Pulsar Timing Array (InPTA;
Joshi et al. 2018), PPTA, and Chinese Pulsar Timing
Array (CPTA; Lee 2016) collaborations have also recently searched their most recent data for signatures of
a gravitational-wave background (Antoniadis et al. 2023;
Reardon et al. 2023; Xu et al. 2023), and an upcoming
IPTA paper will compare the results of these searches.
The IPTA’s forthcoming Data Release 3 will combine
the NANOGrav 15-year data set with observations from
the EPTA, PPTA, and InPTA collaborations, comprising about 80 pulsars with time spans up to 24 years, and
offering significantly greater sensitivity to spatial correlations and spectral characteristics than single-PTA
data sets. Future PTA observation campaigns will improve our understanding of this signal and of its astrophysical and cosmological interpretation. Longer data
sets will tighten spectral constraints on the GWB, clarifying its origin (Pol et al. 2021). Greater numbers of
pulsars will allow us to probe anisotropy in the GWB
(Pol et al. 2022) and its polarization structure (see, e.g.,
Arzoumanian et al. 2021, and references therein). The
observation of a stochastic signal with spatial correlations in PTA data, suggesting a GWB origin, expands
the horizon of GW astronomy with a new Galaxy-scale
observatory sensitive to the most massive black-hole systems in the Universe and to exotic cosmological processes.

Author contributions. An alphabetical-order author
list was used for this paper in recognition of the fact that
a large, decade timescale project such as NANOGrav is
necessarily the result of the work of many people. All
authors contributed to the activities of the NANOGrav
collaboration leading to the work presented here, and
reviewed the manuscript, text, and figures prior to the
paper’s submission. Additional specific contributions
to this paper are as follows. G.A., A.A., A.M.A.,
Z.A., P.T.B., P.R.B., H.T.C., K.C., M.E.D., P.B.D.,
T.D., E.C.F., W.F., E.F., G.E.F., N.G., P.A.G., J.G.,
D.C.G., J.S.H., R.J.J., M.L.J., D.L.K., M.K., M.T.L.,
D.R.L., J.L., R.S.L., A.M., M.A.M., N.M., B.W.M.,
C.N., D.J.N., T.T.P., B.B.P.P., N.S.P., H.A.R., S.M.R.,
P.S.R., A.S., C.S., B.J.S., I.H.S., K.S., A.S., J.K.S., and
H.M.W. developed the 15-year data set through a combination of observations, arrival time calculations, data
checks and refinements, and timing model development
and analysis; additional specific contributions to the
data set are summarized in NG15. S.R.T. and S.J.V. led
the search and coordinated the writing of this paper.
P.T.B., J.S.H., P.M.M., N.S.P., J.S., S.R.T., M.V., and
S.J.V. wrote the paper, made the figures, and generated the bibliography. K.P.I., N.L., N.S.P., X.S., J.S.,
J.P.S., S.R.T., and S.J.V. performed analyses and developed new techniques on a preliminary 14-year data
set. P.T.B., B.B., B.D.C., S.C., B.D., G.E.F., K.G.,
A.D.J., A.R.K., L.Z.K., N.L., W.G.L., N.S.P., S.C.S.,
L.S., X.S., J.S., J.P.S., S.R.T., C.U., M.V., S.J.V.,
Q.W., and C.A.W. analyzed preliminary versions of the
15-year data set. J.S.H., J.G., N.L., N.S.P., J.P.S., and
J.K.S. performed noise analyses on the data set. P.T.B.,
B.B., R.B., R.C., M.C., N.J.C., D.D., H.D., G.E.F.,
K.A.G., S.H., A.D.J., N.L., W.G.L., P.M.M., P.P.,
N.S.P., S.C.S., X.S., J.S., J.P.S., J.T., S.R.T., M.V.,
S.J.V., and C.A.W. performed the Bayesian and frequentist analyses presented in this paper. K.G., J.S.H.,
P.M.M., J.D.R., and S.J.V. computed the background
distribution of our detection statistics. P.R.B., P.M.M.,
N.S.P., and M.V. performed simulations that were used
to compute false alarm probabilities. A.M.A., P.T.B.,
B.B., B.D., S.C., J.A.E., G.E.F., J.S.H., A.D.J., A.R.K.,
N.L., M.T.L., K.D.O., T.T.P., N.S.P., J.S., J.P.S.,
J.K.S., S.R.T., M.V., and S.J.V. contributed to the development of our code. P.T.B., N.J.C., J.S.H., A.D.J.,
T.B.L., P.M.M., J.D.R., and M.V. performed an internal code review. K.C., C.C., J.A.E., J.S.H., D.R.M.,
M.A.Mc., C.M.F.M., K.D.O., N.S.P., S.R.T., M.V.,
R.v.H., and S.J.V. were part of a NANOGrav Detection
Study Group. M.A.M. and P.N. served on the IPTA
Detection Committee. K.C., J.S.H., T.J.W.L., P.M.M.,
N.S.P., J.D.R., X.S., S.R.T., S.J.V., and C.A.W. responded to the Detection Checklist from the IPTA Detection Committee.

## PDF page 18

18

The NANOGrav Collaboration

Acknowledgments. The NANOGrav collaboration receives support from National Science Foundation (NSF)
Physics Frontiers Center award numbers 1430284 and
2020265, the Gordon and Betty Moore Foundation, NSF
AccelNet award number 2114721, an NSERC Discovery
Grant, and CIFAR. The Arecibo Observatory is a facility of the NSF operated under cooperative agreement
(AST-1744119) by the University of Central Florida
(UCF) in alliance with Universidad Ana G. Méndez
(UAGM) and Yang Enterprises (YEI), Inc. The Green
Bank Observatory is a facility of the NSF operated under cooperative agreement by Associated Universities,
Inc. The National Radio Astronomy Observatory is a facility of the NSF operated under cooperative agreement
by Associated Universities, Inc. This work used the
Extreme Science and Engineering Discovery Environment (XSEDE), which is supported by National Science
Foundation grant number ACI-1548562. Specifically, it
used the Bridges-2 system, which is supported by NSF
award number ACI-1928147, at the Pittsburgh Supercomputing Center (PSC). This work was conducted using the Thorny Flat HPC Cluster at West Virginia University (WVU), which is funded in part by National Science Foundation (NSF) Major Research Instrumentation Program (MRI) Award number 1726534, and West
Virginia University. This work was also conducted in
part using the resources of the Advanced Computing
Center for Research and Education (ACCRE) at Vanderbilt University, Nashville, TN. This work was facilitated through the use of advanced computational, storage, and networking infrastructure provided by the Hyak
supercomputer system at the University of Washington.
This research was supported in part through computational resources and services provided by Advanced Research Computing at the University of Michigan, Ann
Arbor. NANOGrav is part of the International Pulsar Timing Array (IPTA); we would like to thank our
IPTA colleagues for their feedback on this paper. We
thank members of the IPTA Detection Committee for
developing the IPTA Detection Checklist. We thank
Bruce Allen for useful feedback. We thank Valentina
Di Marco and Eric Thrane for uncovering a bug in the
sky scramble code. We thank Jolien Creighton and Leo
Stein for helpful conversations about background estimation. L.B. acknowledges support from the National
Science Foundation under award AST-1909933 and from
the Research Corporation for Science Advancement under Cottrell Scholar Award No. 27553. P.R.B. is supported by the Science and Technology Facilities Council,
grant number ST/W000946/1. S.B. gratefully acknowledges the support of a Sloan Fellowship, and the support of NSF under award #1815664. The work of R.B.,

R.C., D.D., N.La., X.S., J.P.S., and J.T. is partly supported by the George and Hannah Bolinger Memorial
Fund in the College of Science at Oregon State University. M.C., P.P., and S.R.T. acknowledge support from
NSF AST-2007993. M.C. and N.S.P. were supported
by the Vanderbilt Initiative in Data Intensive Astrophysics (VIDA) Fellowship. K.Ch., A.D.J., and M.V.
acknowledge support from the Caltech and Jet Propulsion Laboratory President’s and Director’s Research and
Development Fund. K.Ch. and A.D.J. acknowledge
support from the Sloan Foundation. Support for this
work was provided by the NSF through the Grote Reber
Fellowship Program administered by Associated Universities, Inc./National Radio Astronomy Observatory.
Support for H.T.C. is provided by NASA through the
NASA Hubble Fellowship Program grant #HST-HF251453.001 awarded by the Space Telescope Science Institute, which is operated by the Association of Universities for Research in Astronomy, Inc., for NASA, under
contract NAS5-26555. K.Cr. is supported by a UBC
Four Year Fellowship (6456). M.E.D. acknowledges support from the Naval Research Laboratory by NASA
under contract S-15633Y. T.D. and M.T.L. are supported by an NSF Astronomy and Astrophysics Grant
(AAG) award number 2009468. E.C.F. is supported by
NASA under award number 80GSFC21M0002. G.E.F.,
S.C.S., and S.J.V. are supported by NSF award PHY2011772. K.A.G. and S.R.T. acknowledge support from
an NSF CAREER award #2146016. The Flatiron Institute is supported by the Simons Foundation. S.H. is
supported by the National Science Foundation Graduate
Research Fellowship under Grant No. DGE-1745301.
N.La. acknowledges the support from Larry W. Martin and Joyce B. O’Neill Endowed Fellowship in the
College of Science at Oregon State University. Part
of this research was carried out at the Jet Propulsion
Laboratory, California Institute of Technology, under a
contract with the National Aeronautics and Space Administration (80NM0018D0004). D.R.L. and M.A.Mc.
are supported by NSF #1458952. M.A.Mc. is supported by NSF #2009425. C.M.F.M. was supported in
part by the National Science Foundation under Grants
No. NSF PHY-1748958 and AST-2106552. A.Mi. is
supported by the Deutsche Forschungsgemeinschaft under Germany’s Excellence Strategy - EXC 2121 Quantum Universe - 390833306. P.N. acknowledges support
from the BHI, funded by grants from the John Templeton Foundation and the Gordon and Betty Moore
Foundation. The Dunlap Institute is funded by an endowment established by the David Dunlap family and
the University of Toronto. K.D.O. was supported in
part by NSF Grant No. 2207267. T.T.P. acknowledges

## PDF page 19

NANOGrav 15-year Gravitational-Wave Background
support from the Extragalactic Astrophysics Research
Group at Eötvös Loránd University, funded by the
Eötvös Loránd Research Network (ELKH), which was
used during the development of this research. S.M.R.
and I.H.S. are CIFAR Fellows. Portions of this work
performed at NRL were supported by ONR 6.1 basic research funding. J.D.R. also acknowledges support from
start-up funds from Texas Tech University. J.S. is supported by an NSF Astronomy and Astrophysics Postdoctoral Fellowship under award AST-2202388, and acknowledges previous support by the NSF under award
1847938. C.U. acknowledges support from BGU (Kreitman fellowship), and the Council for Higher Education
and Israel Academy of Sciences and Humanities (Excellence fellowship). C.A.W. acknowledges support from
CIERA, the Adler Planetarium, and the Brinson Foundation through a CIERA-Adler postdoctoral fellowship.
O.Y. is supported by the National Science Foundation

19

Graduate Research Fellowship under Grant No. DGE2139292.
Dedication. This paper is dedicated to the memory
of Donald Backer: a pioneer in pulsar timing arrays,
a term he coined; a discoverer of the first millisecond
pulsar; a master developer of pulsar timing instrumentation; a founding member of NANOGrav; and a friend
and mentor to many of us.

Facilities: Arecibo, GBT, VLA
Software: acor, astropy (Astropy Collaboration et al. 2022), ceffyl (Lamb et al. 2023),
chainconsumer (Hinton 2016), ENTERPRISE (Ellis et al.
2019), enterprise extensions (Taylor et al. 2018),
hasasia (Hazboun et al. 2019), holodeck (Kelley et al.
2023), Jupyter (Kluyver et al. 2016), libstempo (Vallisneri 2020), matplotlib (Hunter 2007), numpy (Harris
et al. 2020), PINT (Luo et al. 2021), PTMCMC (Ellis & van
Haasteren 2017), scipy (Virtanen et al. 2020), Tempo2
(Hobbs & Edwards 2012)

REFERENCES
Abbott, B. P., Abbott, R., Abbott, T. D., et al. 2016,
PhRvL, 116, 061102,
doi: 10.1103/PhysRevLett.116.061102
Afzal, A., et al. 2023, in preparation,
doi: 10.3847/2041-8213/acdc91
Agazie, G., et al. 2023a, in preparation
—. 2023b, in preparation, doi: 10.3847/2041-8213/acda9a
—. 2023c, in preparation, doi: 10.3847/2041-8213/acda88
Aggarwal, K., Arzoumanian, Z., Baker, P. T., et al. 2019,
ApJ, 880, 116, doi: 10.3847/1538-4357/ab2236
Akaike, H. 1998, Information Theory and an Extension of
the Maximum Likelihood Principle, ed. E. Parzen,
K. Tanabe, & G. Kitagawa (New York, NY: Springer
New York), 199–213, doi: 10.1007/978-1-4612-1694-0 15
Alam, M. F., Arzoumanian, Z., Baker, P. T., et al. 2021a,
ApJS, 252, 4, doi: 10.3847/1538-4365/abc6a0
—. 2021b, ApJS, 252, 5, doi: 10.3847/1538-4365/abc6a1
Allen, B. 2023, PhRvD, 107, 043018,
doi: 10.1103/PhysRevD.107.043018
Allen, B., & Romano, J. D. 2022, arXiv e-prints,
arXiv:2208.07230, doi: 10.48550/arXiv.2208.07230
Anholm, M., Ballmer, S., Creighton, J. D. E., Price, L. R.,
& Siemens, X. 2009, PhRvD, 79, 084030,
doi: 10.1103/PhysRevD.79.084030
Antoniadis, J., Arzoumanian, Z., Babak, S., et al. 2022,
MNRAS, 510, 4873, doi: 10.1093/mnras/stab3418
Antoniadis, J., et al. 2023, in preparation

Armitage, P. J., & Natarajan, P. 2002, ApJL, 567, L9,
doi: 10.1086/339770
Arzoumanian, Z., Brazier, A., Burke-Spolaor, S., et al.
2015, ApJ, 813, 65, doi: 10.1088/0004-637X/813/1/65
—. 2016, ApJ, 821, 13, doi: 10.3847/0004-637X/821/1/13
Arzoumanian, Z., Baker, P. T., Brazier, A., et al. 2018,
ApJ, 859, 47, doi: 10.3847/1538-4357/aabd3b
Arzoumanian, Z., Baker, P. T., Blumer, H., et al. 2020, The
Astrophysical Journal Letters, 905, L34,
doi: 10.3847/2041-8213/abd401
Arzoumanian, Z., Baker, P. T., Blumer, H., et al. 2021,
ApJL, 923, L22, doi: 10.3847/2041-8213/ac401c
Arzoumanian, Z., Baker, P. T., Blecha, L., et al. 2023,
arXiv e-prints, arXiv:2301.03608,
doi: 10.48550/arXiv.2301.03608
Astropy Collaboration, Price-Whelan, A. M., Lim, P. L.,
et al. 2022, ApJ, 935, 167, doi: 10.3847/1538-4357/ac7c74
Backer, D. C., Kulkarni, S. R., Heiles, C., Davis, M. M., &
Goss, W. M. 1982, Nature, 300, 615,
doi: 10.1038/300615a0
Bartolo, N., Bertacca, D., Caldwell, R., et al. 2022, JCAP,
2022, 009, doi: 10.1088/1475-7516/2022/11/009
Bécsy, B., Cornish, N. J., & Kelley, L. Z. 2022, ApJ, 941,
119, doi: 10.3847/1538-4357/aca1b2
Begelman, M. C., Blandford, R. D., & Rees, M. J. 1980,
Nature, 287, 307, doi: 10.1038/287307a0

## PDF page 20

20

The NANOGrav Collaboration

Blumenthal, G. R., Faber, S. M., Primack, J. R., & Rees,
M. J. 1984, Nature, 311, 517, doi: 10.1038/311517a0
Burke-Spolaor, S., Taylor, S. R., Charisi, M., et al. 2019,
A&A Rv, 27, 5, doi: 10.1007/s00159-019-0115-7
Caprini, C., & Figueroa, D. G. 2018, Classical and
Quantum Gravity, 35, 163001,
doi: 10.1088/1361-6382/aac608
Carlin, B. P., & Chib, S. 1995, Journal of the Royal
Statistical Society. Series B (Methodological), 57, 473.
http://www.jstor.org/stable/2346151
Chalumeau, A., Babak, S., Petiteau, A., et al. 2022,
MNRAS, 509, 5538, doi: 10.1093/mnras/stab3283
Chamberlin, S. J., Creighton, J. D. E., Siemens, X., et al.
2015, PhRvD, 91, 044048,
doi: 10.1103/PhysRevD.91.044048
Chen, S., Caballero, R. N., Guo, Y. J., et al. 2021,
MNRAS, 508, 4970, doi: 10.1093/mnras/stab2833
Cordes, J. M. 2013, Classical and Quantum Gravity, 30,
224002, doi: 10.1088/0264-9381/30/22/224002
Cornish, N. J., & Littenberg, T. B. 2015, Classical and
Quantum Gravity, 32, 135012
Cornish, N. J., & Sampson, L. 2016, PhRvD, 93, 104047,
doi: 10.1103/PhysRevD.93.104047
Cornish, N. J., & Sesana, A. 2013, Class. Quant. Grav., 30,
224005, doi: 10.1088/0264-9381/30/22/224005
Demorest, P. B. 2007, PhD thesis, University of California,
Berkeley
Demorest, P. B., Ferdman, R. D., Gonzalez, M. E., et al.
2013, ApJ, 762, 94, doi: 10.1088/0004-637X/762/2/94
Desvignes, G., Caballero, R. N., Lentati, L., et al. 2016,
MNRAS, 458, 3341, doi: 10.1093/mnras/stw483
Detweiler, S. 1979, ApJ, 234, 1100, doi: 10.1086/157593
Dickey, J. M. 1971, The Annals of Mathematical Statistics,
42, 204. http://www.jstor.org/stable/2958475
Domènech, G. 2021, Universe, 7, 398,
doi: 10.3390/universe7110398
DuPlain, R., Ransom, S., Demorest, P., et al. 2008, in
Proc. SPIE, Vol. 7019, Advanced Software and Control
for Astronomy II, 70191D, doi: 10.1117/12.790003
Einstein, A. 1916, Sitzungsber. Preuss. Akad. Wiss. Berlin
(Math. Phys.), 1916, 1
Ellis, J., & van Haasteren, R. 2017,
jellis18/PTMCMCSampler: Official Release,
doi: 10.5281/zenodo.1037579
Ellis, J. A., Vallisneri, M., Taylor, S. R., & Baker, P. T.
2019, ENTERPRISE: Enhanced Numerical Toolbox
Enabling a Robust PulsaR Inference SuitE.
http://ascl.net/1912.015
Enoki, M., & Nagashima, M. 2007, Progress of Theoretical
Physics, 117, 241, doi: 10.1143/PTP.117.241

Estabrook, F. B., & Wahlquist, H. D. 1975, General
Relativity and Gravitation, 6, 439,
doi: 10.1007/BF00762449
Ford, J. M., Demorest, P., & Ransom, S. 2010, in
Proc. SPIE, Vol. 7740, Software and Cyberinfrastructure
for Astronomy, 77400A, doi: 10.1117/12.857666
Foster, R. S., & Backer, D. C. 1990, ApJ, 361, 300,
doi: 10.1086/169195
Gair, J., Romano, J. D., Taylor, S., & Mingarelli, C. M. F.
2014, Phys. Rev. D, 90, 082001,
doi: 10.1103/PhysRevD.90.082001
Gelman, A., Carlin, J., Stern, H., et al. 2013, Bayesian
Data Analysis, Third Edition, Chapman & Hall/CRC
Texts in Statistical Science (Taylor & Francis)
Gelman, A., & Meng, X.-L. 1998, Statistical science, 163,
doi: 10.1214/ss/1028905934
Gelman, A., Meng, X.-L., & Stern, H. 1996, Statistica
Sinica, 6, 733. http://www.jstor.org/stable/24306036
Gelman, A., & Rubin, D. B. 1992, Statistical Science, 7,
457. http://www.jstor.org/stable/2246093
Godsill, S. J. 2001, Journal of Computational and Graphical
Statistics, 10, 230. http://www.jstor.org/stable/1391010
Goncharov, B., Shannon, R. M., Reardon, D. J., et al.
2021a, ApJL, 917, L19, doi: 10.3847/2041-8213/ac17f4
Goncharov, B., Reardon, D. J., Shannon, R. M., et al.
2021b, MNRAS, 502, 478, doi: 10.1093/mnras/staa3411
Goncharov, B., Thrane, E., Shannon, R. M., et al. 2022,
ApJL, 932, L22, doi: 10.3847/2041-8213/ac76bb
Guzzetti, M. C., Bartolo, N., Liguori, M., & Matarrese, S.
2016, La Rivista del Nuovo Cimento, 39, 399,
doi: 10.1393/ncr/i2016-10127-1
Harris, C. R., Millman, K. J., van der Walt, S. J., et al.
2020, Nature, 585, 357, doi: 10.1038/s41586-020-2649-2
Hazboun, J., Meyers, P. M., Romano, J. D., Siemens, X., &
Archibald, A. M. 2023, arXiv e-prints, arXiv:2305.01116.
https://arxiv.org/abs/2305.01116
Hazboun, J., Romano, J., & Smith, T. 2019, The Journal of
Open Source Software, 4, 1775, doi: 10.21105/joss.01775
Hazboun, J. S., Romano, J. D., & Smith, T. L. 2019, Phys.
Rev. D, 100, 104028, doi: 10.1103/PhysRevD.100.104028
Hazboun, J. S., Simon, J., Taylor, S. R., et al. 2020, ApJ,
890, 108, doi: 10.3847/1538-4357/ab68db
Hazboun, J. S., Simon, J., Madison, D. R., et al. 2022, ApJ,
929, 39, doi: 10.3847/1538-4357/ac5829
Heck, D. W., Overstall, A. M., Gronau, Q. F., &
Wagenmakers, E.-J. 2019, Statistics and Computing, 29,
631, doi: 10.1007/s11222-018-9828-0
Hee, S., Handley, W. J., Hobson, M. P., & Lasenby, A. N.
2015, Monthly Notices of the Royal Astronomical
Society, 455, 2461, doi: 10.1093/mnras/stv2217

## PDF page 21

NANOGrav 15-year Gravitational-Wave Background
Hellings, R. W., & Downs, G. S. 1983, ApJL, 265, L39,
doi: 10.1086/183954
Hinton, S. R. 2016, The Journal of Open Source Software,
1, 00045, doi: 10.21105/joss.00045
Hobbs, G., & Edwards, R. 2012, Tempo2: Pulsar Timing
Package. http://ascl.net/1210.015
Hobbs, G., Coles, W., Manchester, R. N., et al. 2012,
MNRAS, 427, 2780,
doi: 10.1111/j.1365-2966.2012.21946.x
Hobbs, G., Guo, L., Caballero, R. N., et al. 2020, MNRAS,
491, 5951, doi: 10.1093/mnras/stz3071
Hourihane, S., Meyers, P., Johnson, A., Chatziioannou, K.,
& Vallisneri, M. 2023, PhRvD, 107, 084045,
doi: 10.1103/PhysRevD.107.084045
Hulse, R. A., & Taylor, J. H. 1975, ApJL, 195, L51,
doi: 10.1086/181708
Hunter, J. D. 2007, Computing in Science and Engineering,
9, 90, doi: 10.1109/MCSE.2007.55
Jaffe, A. H., & Backer, D. C. 2003, Astrophysical Journal,
583, 616, doi: 10.1086/345443
Jenet, F. A., Hobbs, G. B., van Straten, W., et al. 2006,
ApJ, 653, 1571, doi: 10.1086/508702
Johnson, A., et al. 2023, in preparation
Jones, M. L., McLaughlin, M. A., Lam, M. T., et al. 2017,
ApJ, 841, 125, doi: 10.3847/1538-4357/aa73df
Joshi, B. C., Arumugasamy, P., Bagchi, M., et al. 2018,
Journal of Astrophysics and Astronomy, 39, 51,
doi: 10.1007/s12036-018-9549-y
Kaiser, A. R., Pol, N. S., McLaughlin, M. A., et al. 2022,
ApJ, 938, 115, doi: 10.3847/1538-4357/ac86cc
Kaspi, V. M., Taylor, J. H., & Ryba, M. F. 1994, ApJ, 428,
713, doi: 10.1086/174280
Kelley, L. Z., et al. 2023, in preparation
Khmelnitsky, A., & Rubakov, V. 2014, JCAP, 2014, 019,
doi: 10.1088/1475-7516/2014/02/019
Kluyver, T., Ragan-Kelley, B., Pérez, F., et al. 2016, in
Positioning and Power in Academic Publishing: Players,
Agents and Agendas, ed. F. Loizides & B. Schmidt, IOS
Press, 87 – 90
Lam, M. T., Cordes, J. M., Chatterjee, S., et al. 2017, ApJ,
834, 35, doi: 10.3847/1538-4357/834/1/35
Lam, M. T., Ellis, J. A., Grillo, G., et al. 2018, ApJ, 861,
132, doi: 10.3847/1538-4357/aac770
Lamb, W. G., Taylor, S. R., & van Haasteren, R. 2023,
arXiv e-prints, arXiv:2303.15442,
doi: 10.48550/arXiv.2303.15442
Lee, K. J. 2016, in Astronomical Society of the Pacific
Conference Series, Vol. 502, Frontiers in Radio
Astronomy and FAST Early Sciences Symposium 2015,
ed. L. Qain & D. Li, 19

21

Lentati, L., Alexander, P., Hobson, M. P., et al. 2013,
PhRvD, 87, 104021, doi: 10.1103/PhysRevD.87.104021
Luo, J., Ransom, S., Demorest, P., et al. 2021, ApJ, 911,
45, doi: 10.3847/1538-4357/abe62f
Magorrian, J., Tremaine, S., Richstone, D., et al. 1998, AJ,
115, 2285, doi: 10.1086/300353
Manchester, R. N., Hobbs, G., Bailes, M., et al. 2013,
PASA, 30, e017, doi: 10.1017/pasa.2012.017
McConnell, N. J., & Ma, C.-P. 2013, ApJ, 764, 184,
doi: 10.1088/0004-637X/764/2/184
McLaughlin, M. A. 2013, Classical and Quantum Gravity,
30, 224008, doi: 10.1088/0264-9381/30/22/224008
McWilliams, S. T., Ostriker, J. P., & Pretorius, F. 2014,
ApJ, 789, 156, doi: 10.1088/0004-637X/789/2/156
Merritt, D., & Milosavljević, M. 2005, Living Reviews in
Relativity, 8, 8, doi: 10.12942/lrr-2005-8
Meyers, P. M., Chatziioannou, K., Vallisneri, M., & Chua,
A. J. K. 2023, arXiv e-prints, arXiv:2306.05559,
doi: 10.48550/arXiv.2306.05559
Milosavljević, M., & Merritt, D. 2003, ApJ, 596, 860,
doi: 10.1086/378086
Mingarelli, C. M. F., & Mingarelli, A. B. 2018, Journal of
Physics Communications, 2, 105002,
doi: 10.1088/2399-6528/aae06d
Mingarelli, C. M. F., & Sidery, T. 2014, PhRvD, 90,
062011, doi: 10.1103/PhysRevD.90.062011
Mingarelli, C. M. F., Sidery, T., Mandel, I., & Vecchio, A.
2013, PhRvD, 88, 062005,
doi: 10.1103/PhysRevD.88.062005
Mingarelli, C. M. F., Lazio, T. J. W., Sesana, A., et al.
2017, Nature Astronomy, 1, 886,
doi: 10.1038/s41550-017-0299-6
Nay, J., Boddy, K. K., Smith, T. L., & Mingarelli, C. M. F.
2023, arXiv e-prints, arXiv:2306.06168,
doi: 10.48550/arXiv.2306.06168
Ogata, Y. 1989, Numerische Mathematik, 55, 137,
doi: 10.1007/BF01406511
Park, R. S., Folkner, W. M., Williams, J. G., & Boggs,
D. H. 2021, AJ, 161, 105, doi: 10.3847/1538-3881/abd414
Perera, B. B. P., DeCesar, M. E., Demorest, P. B., et al.
2019, MNRAS, 490, 4666, doi: 10.1093/mnras/stz2857
Petit, G. 2022, personal communication
Phinney, E. S. 2001, arXiv e-prints, astro,
doi: 10.48550/arXiv.astro-ph/0108028
Pirani, F. A. E. 1956, Acta Physica Polonica, 15, 389,
doi: 10.1007/s10714-009-0787-9
Pirani, F. A. E. 2009, General Relativity and Gravitation,
41, 1215, doi: 10.1007/s10714-009-0787-9
Pol, N., Taylor, S. R., & Romano, J. D. 2022, ApJ, 940,
173, doi: 10.3847/1538-4357/ac9836

## PDF page 22

22

The NANOGrav Collaboration

Pol, N. S., Taylor, S. R., Kelley, L. Z., et al. 2021, ApJL,
911, L34, doi: 10.3847/2041-8213/abf2c9
Rajagopal, M., & Romani, R. W. 1995, ApJ, 446, 543,
doi: 10.1086/175813
Ransom, S., Brazier, A., Chatterjee, S., et al. 2019, in
BAAS, Vol. 51, 195. https://arxiv.org/abs/1908.05356
Reardon, D. J., et al. 2023, in preparation
Roebber, E. 2019, ApJ, 876, 55,
doi: 10.3847/1538-4357/ab100e
Roebber, E., & Holder, G. 2017, ApJ, 835, 21,
doi: 10.3847/1538-4357/835/1/21
Romani, R. W. 1989, in Timing Neutron Stars, ed.
H. Ögelman & E. P. J. Heuvel (Springer), 113–117
Romano, J. D., Hazboun, J. S., Siemens, X., & Archibald,
A. M. 2021, PhRvD, 103, 063027,
doi: 10.1103/PhysRevD.103.063027
Rosado, P. A., Sesana, A., & Gair, J. 2015, MNRAS, 451,
2417, doi: 10.1093/mnras/stv1098
Sampson, L., Cornish, N. J., & McWilliams, S. T. 2015,
PhRvD, 91, 084055, doi: 10.1103/PhysRevD.91.084055
Sardesai, S. C., & Vigeland, S. J. 2023, arXiv e-prints,
arXiv:2303.09615. https://arxiv.org/abs/2303.09615
Sazhin, M. V. 1978, Soviet Ast., 22, 36
Sesana, A. 2013, MNRAS, 433, L1,
doi: 10.1093/mnrasl/slt034
Sesana, A., Haardt, F., Madau, P., & Volonteri, M. 2004,
ApJ, 611, 623, doi: 10.1086/422185
Sesana, A., Vecchio, A., & Colacino, C. N. 2008, MNRAS,
390, 192, doi: 10.1111/j.1365-2966.2008.13682.x
Siemens, X., Ellis, J., Jenet, F., & Romano, J. D. 2013,
Class. Quant. Grav., 30, 224015,
doi: 10.1088/0264-9381/30/22/224015
Speri, L., Porayko, N. K., Falxa, M., et al. 2023, MNRAS,
518, 1802, doi: 10.1093/mnras/stac3237
Stinebring, D. R., Ryba, M. F., Taylor, J. H., & Romani,
R. W. 1990, PhRvL, 65, 285,
doi: 10.1103/PhysRevLett.65.285
Taylor, J. H., Fowler, L. A., & McCulloch, P. M. 1979,
Nature, 277, 437, doi: 10.1038/277437a0
Taylor, S. R. 2021, Nanohertz Gravitational Wave
Astronomy (Boca Raton, FL: CRC Press)

Taylor, S. R., Baker, P. T., Hazboun, J. S., Simon, J. J., &
Vigeland, S. J. 2018, enterprise extensions.
https://github.com/nanograv/enterprise extensions
Taylor, S. R., & Gair, J. R. 2013, PhRvD, 88, 084001,
doi: 10.1103/PhysRevD.88.084001
Taylor, S. R., Lentati, L., Babak, S., et al. 2017, PhRvD,
95, 042002, doi: 10.1103/PhysRevD.95.042002
Taylor, S. R., Simon, J., Schult, L., Pol, N., & Lamb, W. G.
2022, PhRvD, 105, 084049,
doi: 10.1103/PhysRevD.105.084049
Taylor, S. R., van Haasteren, R., & Sesana, A. 2020,
PhRvD, 102, 084039, doi: 10.1103/PhysRevD.102.084039
Tiburzi, C., Hobbs, G., Kerr, M., et al. 2016, MNRAS, 455,
4339, doi: 10.1093/mnras/stv2143
Tomczak, A. R., Quadri, R. F., Tran, K.-V. H., et al. 2014,
ApJ, 783, 85, doi: 10.1088/0004-637X/783/2/85
Vallisneri, M. 2020, libstempo: Python wrapper for
Tempo2. http://ascl.net/2002.017
Vallisneri, M., Taylor, S. R., Simon, J., et al. 2020, ApJ,
893, 112, doi: 10.3847/1538-4357/ab7b67
van Haasteren, R., Levin, Y., McDonald, P., & Lu, T. 2009,
MNRAS, 395, 1005,
doi: 10.1111/j.1365-2966.2009.14590.x
van Haasteren, R., & Vallisneri, M. 2014, PhRvD, 90,
104012, doi: 10.1103/PhysRevD.90.104012
Vehtari, A., Gelman, A., Simpson, D., Carpenter, B., &
Bürkner, P.-C. 2021, Bayesian Analysis, 16, 667 ,
doi: 10.1214/20-BA1221
Vigeland, S. J., Islo, K., Taylor, S. R., & Ellis, J. A. 2018,
PhRvD, 98, 044003, doi: 10.1103/PhysRevD.98.044003
Virtanen, P., Gommers, R., Oliphant, T. E., et al. 2020,
Nature Methods, 17, 261, doi: 10.1038/s41592-019-0686-2
Wilcox, R. 2012, Introduction to Robust Estimation and
Hypothesis Testing, Statistical Modeling and Decision
Science (Elsevier Science)
Wyithe, J. S. B., & Loeb, A. 2003, ApJ, 590, 691,
doi: 10.1086/375187
Xu, H., Chen, S., Gio, Y., et al. 2023, in preparation
Zic, A., Hobbs, G., Shannon, R. M., et al. 2022, MNRAS,
516, 410, doi: 10.1093/mnras/stac2100

## PDF page 23

23

NANOGrav 15-year Gravitational-Wave Background
APPENDIX
A. ADDITIONAL DATA SET DETAILS

B. BAYESIAN METHODS & DIAGNOSTICS

The prior probability distributions assumed for all
analyses in this paper are listed in Table 1. We use
Markov chain Monte Carlo (MCMC) techniques to sample randomly from the joint posterior distribution of our
model parameters. Marginal distributions are obtained
simply by considering only the parameter of interest

60°

45°
30°
15°
0°
-15°
-30°
-45°
-60°

pulsar pairs in bin

The observations included in the NANOGrav 15-year
data set were performed between July 2004 and August
2020 with the 305-m Arecibo Observatory (Arecibo), the
100-m Green Bank Telescope (GBT), and, since 2015,
the 27 25-m antennae of the Very Large Array (VLA).
We used Arecibo to observe the 33 pulsars that lie within
its declination range (0◦ < δ < +39◦ ); GBT to observe the pulsars that lie outside of Arecibo’s range,
plus J1713+0747 and B1937+21, for a total of 36 pulsars; the VLA to observe the seven pulsars J0437−4715,
J1600−3053, J1643−1224, J1713+0747, J1903+0327,
J1909−3744, and B1937+21. Six of these were also observed with Arecibo, GBT, or both; J0437−4715 was
only visible to the VLA. Figure 12 shows the sky locations of the 67 pulsars used for the GWB search (top)
and the distribution of angular separations for the pulsar
pairs (bottom).
Initial observations were performed with the ASP
(Arecibo) and GASP (GBT) systems, with 64-MHz
bandwidth (Demorest 2007). Between 2010 and 2012,
we transitioned to the PUPPI (Arecibo) and GUPPI
(GBT) systems, with bandwidths up to 800 MHz (DuPlain et al. 2008; Ford et al. 2010). We observe pulsars
in two different radio-frequency bands in order to measure pulse dispersion from the interstellar medium: at
Arecibo, we use the 1.4 GHz receiver plus either the 430
MHz or 2.1 GHz receiver (and the 327 MHz receiver for
early observations of J2317+1439); at GBT, we use the
820 MHz and 1.4 GHz receivers; at the VLA, we use the
1.4 GHz and 3 GHz receivers with the YUPPI system.
In §5.4 we analyze also two split-telescope data sets:
33 pulsars for Arecibo, and 35 for GBT (excluding
J0614−3329, which was observed for less than three
years). For the two pulsars timed by both telescopes
(J1713+0747 and B1937+21), we partition the timing
data between the telescopes and obtain independent
timing solutions for each. We do not analyze a VLA-only
data set, which would have shorter observation spans
and significantly reduced sensitivity.

75°

16h

12h

8h

4h
VLA
Arecibo
GBT

-75°

all
Arecibo
GBT

300
200
100
0

0

50
100
angular separation (deg)

150

Figure 12. Top: Sky locations of the 67 pulsars used in the
15-year GWB analysis. Markers indicate which telescopes
observed the pulsar. Bottom: Distribution of angular separations probed by the pulsars in the full data set (orange),
the Arecibo data set (blue), and the GBT data set (red).
Because Arecibo and GBT mostly observed pulsars at different declinations, there are few inter-telescope pairs at small
angular separations, resulting in a deficit of pairs for the full
data set in the first bin.

in each sample. To assess convergence of our MCMC
runs beyond visual inspection we use the Gelman–Rubin
statistic, requiring R̂ < 1.01 for all parameters (Gelman
& Rubin 1992; Vehtari et al. 2021). We performed most
runs discussed in this paper with the PTMCMC sampler
(Ellis & van Haasteren 2017) and postprocessed samples with chainconsumer (Hinton 2016).
In NG12gwb we use an analytic approximation for the
uncertainty of marginalized-posterior statistics (Wilcox
2012). Here we instead adopt a boostrap approach:
we resample the original MCMC samples (with replacement) to generate new sets that act as independent sampling realizations. We then calculate the distributions of
the desired summary statistics (e.g., quantiles, marginalized posterior values) over these sets. From these distributions, we determine central values and uncertainties
(either medians and 68% confidence intervals, or means
and standard deviations).

## PDF page 24

24

The NANOGrav Collaboration
Table 1. Prior distributions used in all analyses performed in this paper.
parameter

description

Ek
Qk [s]
Jk [s]

EFAC per backend/receiver system
EQUAD per backend/receiver system
ECORR per backend/receiver system

Uniform [0, 10]
log-Uniform [−8.5, −5]
log-Uniform [−8.5, −5]
intrinsic red noise

single-pulsar analysis only
single-pulsar analysis only
single-pulsar analysis only

Ared
γred

red-noise power-law amplitude
log-Uniform [−20, −11]
red-noise power-law spectral index
Uniform [0, 7]
all common processes, free spectrum

one parameter per pulsar
one parameter per pulsar

ρi [s2 ]

power-spectrum coefficients at f = i/T
log-Uniform in ρi [−18, −8]
all common processes, power-law spectrum

one parameter per frequency

A

common process strain amplitude

log-Uniform [−18, −14] (γ = 13/3)
log-Uniform [−18, −11] (γ varied)
common process power-law spectral index
delta function (γ = 13/3)
Uniform [0, 7]
all common processes, broken–power-law spectrum

one parameter for PTA
one parameter for PTA
fixed
one parameter for PTA

A
γ
δ
fbend [Hz]
ℓ

broken–power-law amplitude
log-Uniform [−18, −11]
broken–power-law low-freq. spectral index
Uniform [0, 7]
broken–power-law high-freq. spectral index
delta function (δ = 0)
broken–power-law bend frequency
log-Uniform [−8.7,−7]
broken–power-law high-freq. transition sharpness delta function (ℓ = 0.1)
all common processes, t-process spectrum

one parameter for PTA
one parameter per PTA
fixed
one parameter for PTA
fixed

A
γ
xi

power-law amplitude
power-law spectral index
modification factor

A
γ
κ
f0 [Hz]

turnover power-law amplitude
log-Uniform [−18, −11]
turnover power-law high-freq. spectral index
Uniform [0, 7]
turnover power-law low-freq. spectral index
Uniform [0, 7]
turnover power-law bend frequency
log-Uniform [−9,−7]
all common processes, cross-correlation spline model

one parameter for PTA
one parameter per PTA
one parameter per PTA
one parameter for PTA

y

normalized cross-correlation values at spline
knots (10−3 , 25, 49.3, 82.5, 121.8, 150, 180)◦

seven parameters for PTA

γ

prior
white noise

log-Uniform [−18, −11]
Uniform [0, 7]
Inverse Gamma Distribution
all common processes, turnover spectrum

We rely on a variety of techniques to perform Bayesian
model comparison. The first is thermodynamic integration (e.g., Ogata 1989; Gelman & Meng 1998), which
computes Bayesian evidence integrals directly through
parallel tempering: we run Nβ MCMC chains that explore variants of the likelihood function raised to different exponents β, then approximate the evidence for
model H as

ln p(d|H) =

∫ 1
0

⟨ln p(d|θ)⟩β dβ ≈

1 ∑
⟨ln p(d|θ)⟩β ,
Nβ
β

(B1)
where all likelihoods and posteriors are computed
within model H, θ denotes all of the model’s parameters, and the expectation ⟨ln p(d|θ)⟩β is approximated
by MCMC with respect to the posterior pβ (θ|d) ∝
p(d|θ, H)β p(θ, H). The inverse temperatures β are
spaced geometrically, as is the default in PTMCMC.
To compare nested models, which differ by “freezing”
a subset of parameters, we also use the Savage–Dickey
density ratio (Dickey 1971): if models H and H0 differ

Uniform [−0.9, 0.9]

comments

one parameter for PTA
one parameter per PTA
one parameter per frequency

by the fact that (say) θ0 is frozen to 0 in the latter, then
p(d|H0 )/p(d|H) = p(θ0 = 0|d, H)/p(θ0 = 0|H).
When comparing disjoint models with different likelihoods (e.g., hd versus curn), we use product-space
sampling (Carlin & Chib 1995; Godsill 2001). This
method treats model comparison as a parameter estimation problem, where we sample the union of the unique
parameters of all models, plus a model-indexing parameter that activates the relevant likelihood function and
parameter space of one of the sub-models. Bayes factors are then obtained by counting how often the model
index falls in each activation region and taking ratios of
those counts.
In some situations, it can be difficult to sample a computationally expensive model directly. In these cases,
we sample a computationally cheaper approximate distribution and reweight those posterior samples to estimate the posterior for the computationally expensive
model (Hourihane et al. 2023). The reweighted posterior can be used in the thermodynamic-integration or
Savage–Dickey methods. In addition, the mean of the
weights yields the Bayes factor between the expensive

## PDF page 25

NANOGrav 15-year Gravitational-Wave Background
and approximate models, which may be of direct interest
(e.g., hd can be approximated by curn). We estimate
Bayes-factor uncertainties using bootstrapping and, for
product-space sampling, with the Markov-model techniques of Cornish & Littenberg (2015) and Heck et al.
(2019).
C. BROKEN POWER-LAW MODEL

As shown in NG12gwb, the simultaneous Bayesian estimation of white measurement noise and of red-noise
processes described by power laws biases the recovery
of the spectral index of the latter (Lam et al. 2017;
Hazboun et al. 2019). Just as in NG12gwb and Antoniadis et al. (2022), we impose a high-frequency cutoff
on the red-noise processes. To choose the cutoff frequency, we perform inference on our data with a curnγ
model modified so that the common process has power
spectral density
A2
S(f ) =
12π 2

(

f
fref

)−γ [
(
1+

f
fbreak

)1/ℓ ]ℓγ

−3
fref
;

(C2)
then set the cutoff to the MAP fbreak . Equation C2 is
fairly generic, allowing for separate spectral indices at
low (γ) and high (δ) frequencies. The break frequency
fbreak dictates where the broken power law changes spectral index, while ℓ (which we set to 0.1) controls the
smoothness of the transition.
The marginal posterior for fbreak , obtained in the
factorized-likelihood approximation using the techniques of Lamb et al. (2023), has median and 90% cred+5.4
ible region of 3.2−1.2
× 10−8 Hz, and a MAP value of
2.75 × 10−8 Hz. The latter is close to f14 = 14/T in our
frequency basis (with T the total span of the data set),
so we use 14 frequencies to model common-spectrum
noise processes (see §2 and NG12gwb).
D. T -PROCESS SPECTRUM MODEL

The free-spectrum analysis of our data (§5.2 and Figure 6) shows that the frequency bins at f1 , f6 , f7 , and
f8 appear to be in tension with a pure power law, skewing the estimation of γ and reducing the hd13/3 vs.
curn13/3 Bayes factor. Assuming that those frequency
components reflect unmodeled systematics or strongerthan-expected statistical fluctuations, we can make our
inference more robust to such outliers with a “fuzzy”
power-law model that allows the individual Φi to vary
more freely around their expected values. To wit, we
introduce the t-process spectrum (TPS)
ΦTPS,i = xi Φpowerlaw,i

with x ∼ invgamma(xi ; 1, 1),
(D3)

25

where Φpowerlaw,i follows Equation 6 and x follows the
inverse gamma distribution with parameters α = β = 1;
the resulting Gaussian mixture yields a Student’s-t distribution for the ΦTPS,i . Figure 13 shows curnγ powerlaw posteriors and curnTPS modified power-law posteriors, obtained in the factorized-likelihood approximation
(Taylor et al. 2022; Lamb et al. 2023) and compared
to curnfree bin variances. The TPS model is spread
more widely and deviates from the perfect power law at
bins f1 , f6 , f7 , and f8 , as expected. The right panel of
Figure 13 shows the joint log10 A, γ posteriors for curnγ
and curnTPS . The latter is more consistent with steeper
power laws, and it includes γ = 13/3 at 1σ credibility.
E. TURNOVER MODEL

The final parameterized spectral model that we investigate is motivated by the idea that the dynamics
of SMBHBs are influenced by their environments at
sub-parsec separations (Armitage & Natarajan 2002;
Sesana et al. 2004; Merritt & Milosavljević 2005). These
interactions affect binary evolution and the resulting
spectrum of the GWB. The process of bringing two
SMBHs together after galaxy mergers involves a complex chain of interactions: despite significant theoretical
work, the lack of observational constraints makes it difficult to draw any conclusions. PTAs, however, provide
a unique opportunity to probe the timescale over which
two SMBHs evolve from the merger of their galaxies to
a bound binary that produces GW signals in the PTA
sensitivity band.
When dynamical interactions dominate orbital evolution, binaries will traverse the GW spectrum more
quickly, reducing GW emission compared to a GWdriven inspiral. This kind of behavior is captured by
the turnover model (Sampson et al. 2015):
)−γ [
( )κ ]−1
(
A2
f0
f
−3
S(f ) =
1+
fref
. (E4)
2
12π
fref
f
This is qualitatively similar to the broken power law discussed earlier, except that here f0 represents the GW
frequency at which typical binary evolution transitions
from environmentally dominated (at lower frequencies
and wider separations) to GW-dominated (at higher frequencies and smaller separations). The parameter κ
controls the shape of the spectrum below f0 , and depends on the orbital-evolution mechanism. Note that
the actual turning point of the spectrum is not at f0
but at fbend = f0 × (3κ/4 − 1)1/κ (NG9gwb).
Applying this model to our data, we find hints of departures from a pure power law: the transition frequency
f0 lies below 10 nHz with 65% credibility, while the
bend frequency lies below 10 nHz with 75% credibility.

## PDF page 26

26

CURNγ power law

6.
0

4.
5

3.
0

CURNTPS modified power law

1.
5

−
15
.5

−
15
.0

−
14
.5

log10 A

−
14
.0

The NANOGrav Collaboration

γ
Figure 13. Power-law (curnγ , blue) and t-process power-law (curnTPS , orange) spectral posteriors. Left: reconstructed
spectra, compared to free-spectral bin-variance posteriors (curnTPS , violin plots). Right: joint (log10 A, γ) posteriors. The
“fuzzy” t-process allows local deviations from a perfect power law, producing wider constraints that are more consistent with
γ = 13/3 (dashed line).

Nevertheless, Bayesian comparison of this curnturnover
model with curnγ reports an inconclusive Bayes factor of 1.46 ± 0.02 in favor of curnturnover . Furthermore,
the estimation of curnturnover parameters is sensitive to
DM modeling (see §5.1). While the spectra are broadly
consistent whether we use DMX or DMGP to model DM
fluctuations, there are differences in the power at certain
frequencies that lead to differences in the turnover parameters. This is discussed in greater detail in Agazie
et al. (2023a).
F. SKY SCRAMBLES

In the sky-scramble method (Cornish & Sampson
2016), inter-pulsar correlations are analyzed as if the
pulsars occupied random sky positions, with the purpose
of creating a background distribution of PTA detection
statistics for null-hypothesis testing, in alternative to
phase shifts (Taylor et al. 2017; see §3 and §4). If a correlated signal is present in the data, phase shifts and sky
scrambles actually test different null hypotheses: phase
shifts test the hypothesis that no inter-pulsar correlations are present, while sky scrambles assume that interpulsar correlations are present at the level measured in
the data, but test the hypothesis that these correlations
have no dependence on angular separation.
As is the convention in the literature, we require that
scrambled overlap reduction functions (ORFs) be independent of each other and of the unscrambled ORF using a match statistic,

M̄ = √(

∑

′
a,b̸=a Γab Γab

∑

a,b̸=a Γab Γab

) (∑

′
′
a,b̸=a Γab Γab

),

(F5)

where Γab and Γ′ab are two different ORFs. For the
sky scrambles used in our analysis, the scrambled ORFs
have M̄ < 0.1 with respect to the unscrambled ORF,
and M̄ < 0.17 with each other. We generate 10,000
sky scrambles, owing to the difficulty in obtaining large
numbers of scrambled ORFs that satisfy the match
threshold; because of limitations of computational resources, we obtain our detection statistics for 5,000 of
those ORFs. Figure 14 shows the resulting background
distributions for the hdγ -to-curnγ Bayes factor (left
panel) and the optimal-statistic S/N (right panel). The
Bayes factors exceed the observed value in eight of the
5,000 sky scrambles (p = 1.6 × 10−3 ), while none of
the sky scrambles have noise-marginalized mean S/N
greater than observed (p < 10−4 ).
We note that the null distribution recovered by the
sky scrambles is not very sensitive to the choice of
match threshold for |M̄ | ≲ 0.2. Figure 15 compares
the null distributions when the match threshold for all
ORFs with each other and with the unscrambled ORF
is set to |M̄ | < 0.17 (blue), |M̄ | < 0.1 (orange), and
|M̄ | < 0.08 (green). There is very little difference among
the distributions; however, imposing a smaller threshold means that fewer sky scrambles can be used (6,043
with |M̄ | < 0.1 and 1,534 with |M̄ | < 0.08, compared
to 10,000 with |M̄ | < 0.17), which limits the precision
with which the p-value can be measured. We find no
evidence that the recovered null distribution is biased
when including sky scrambles with matches up to 0.17.

## PDF page 27

27

NANOGrav 15-year Gravitational-Wave Background
100
1−CDF

10−1

2σ

2σ

3σ

3σ

10−2
10−3

Sky scrambles

Sky scrambles

10−4

4σ

4σ

10−5
−4

−2

0
log10 BHD
CURN

2

4

−2

0
2
4
Noise-Marginalized Mean S/N

6

Figure 14. Empirical background distribution of hdγ -to-curnγ Bayes factor (left, see §3) and noise-marginalized optimal
statistic (right, see §4), as computed in 5,000 sky scrambles, which erases the dependence of inter-pulsar correlations on the
angular separation between the pulsars. Dotted lines indicate Gaussian-equivalent 2σ, 3σ, and 4σ thresholds. The dashed
vertical lines indicate the values of the detection statistics for the unscrambled data set. We find p = 1.6 × 10−3 (approx. 3σ)
for the Bayesian analysis, and p < 10−4 (> 3σ) for the optimal-statistic analysis.
Table 2. Multiple-correlation optimal statistic best-fit coefficients Â2k , S/Ns, and AIC probabilities

Model
HD only
Monopole only
Dipole only
HD + monopole
HD + dipole
monopole + dipole
HD + monopole + dipole

HD Correlations
S/N
Â2HD
−30
6.8(9) × 10
4(1)
···
···
···
···
5.5(8) × 10−30 3.4(8)
5.5(8) × 10−30 3.2(7)
···
···
5.1(8) × 10−30 2.9(6)

Monopole Correlations
Â2mo
S/N
···
···
1.1(1) × 10−30
4(1)
···
···
8(1) × 10−31
2.9(8)
···
···
8(1) × 10−31
2.7(7)
7(1) × 10−31
2.4(6)

Dipole Correlations
Mean Â2di
S/N
···
···
···
···
1.5(3) × 10−30
4(1)
···
···
−31
8(2) × 10
1.7(7)
9(2) × 10−31
1.9(6)
3(2) × 10−31
0.6(4)

p(AIC)
3 × 10−2
6 × 10−3
8 × 10−4
1
6 × 10−2
1 × 10−2
0.48

Note—All values were computed for the 15-year data set, assuming a power-law power spectral density using the 14 lowest
frequency components. Here Â2 , S/N, and AIC are marginalized over pulsar noise parameters with fixed γ = 13/3. The numbers
in parentheses represent the mean least-squares errors for the Â2k coefficients and standard deviations over noise-parameter
posteriors for S/Ns. We compute p(AIC) with respect to the model with the lowest mean AIC (i.e., HD + monopole).
G. MULTIPLE-CORRELATION OPTIMAL

STATISTIC
The multiple-correlation optimal statistic (MCOS;
Sardesai & Vigeland 2023) fits the inter-pulsar correlation coefficients ρab with a linear model that includes
multiple components with different correlation patterns,
but with the same spectral shape. The linear-model coefficients are the squared amplitudes of the components.
Within such a model, the significance of each component
can be quoted as a S/N given by its best-fit coefficient divided by the fit error. Just as for the noise-marginalized
optimal statistic (Vigeland et al. 2018), the posterior
distribution of pulsar noise parameters induces a distribution of MCOS statistics.
We fit the 15-year data with models that include HD,
monopole, and dipole-correlated components in various
combinations. Table 2 lists the noise-marginalized am-

plitude estimates and S/N for all models. The goodnessof-fit of the models can be compared using the Akaike
Information Criterion (AIC; Akaike 1998):
AIC = 2k + χ2 ,

(G6)

where k is the number of model parameters and χ2 is
the fit’s chi-squared, computed without accounting for
GW-induced ρab correlations. (This can be thought of
as a pseudo-Bayes factor, with the factor of 2k imposing
an Occam penalty.) The relative probability of a model
compared to the most-favored model is then given by
p(AIC) = exp [(AICmin − AIC)/2] ,

(G7)

where AICmin is the minimum AIC across all models.
Table 2 lists the AIC probabilities, computed by averaging the AIC of each model over pulsar noise parameters. The HD-correlated model is preferred among

## PDF page 28

28

The NANOGrav Collaboration
0.6

100

0.4
PDF

2σ

10−2
3σ

10−3

M̄ < 0.17
M̄ < 0.1
M̄ < 0.08

10−4
−2

0
2
4
Noise-Marginalized Mean S/N

0.2
γ = 13/3

4σ

0.0

Figure 15. Comparison between empirical background distributions for the noise-marginalized optimal statistic, as
computed by the sky-scramble technique. We show distributions computed using a match threshold of M̄ < 0.17
(blue), M̄ < 0.1 (orange), and M̄ < 0.08 (green). Dotted
lines indicate Gaussian-equivalent 2σ, 3σ, and 4σ thresholds.
The dashed vertical lines indicate the values of the detection
statistics for the unscrambled data set. We find little difference between the background distributions computed using
different match thresholds, modulo the fact that imposing
a smaller threshold yields fewer sky scrambles, which limits
the precision to which the p-value can be measured.

the models with a single correlated process. The models with both HD and monopole correlations are preferred among all models: for a model with HD and
monopole correlations, we find S/N of 3.4 ± 0.8 for HD
correlations and 2.9 ± 0.8 for monopolar correlations,
while for a model with HD, monopole, and dipole correlations, we find S/N of 2.9 ± 0.6 for HD correlations,
2.4 ± 0.6 for monopole correlations, and 0.6 ± 0.4 for
dipole correlations (means ± standard deviations across
noise-parameter posteriors). The statistical significance
of these S/Ns can be quantified empirically using simulations of 15-year–like data sets (see App. H.1), which
report p-values < 10−2 and ≃ 4 × 10−2 for the observed
mean HD and monopole statistics across data replications with no spatially correlated injections.
As discussed in Sardesai & Vigeland (2023), the optimal statistic and the MCOS are metrics of the apparent
spatial correlation pattern of the data, but they have
a limited ability to identify its actual source. That is
because a real HD signal may also excite the monopole
optimal statistic and the monopole component of the
MCOS; conversely, a real monopolar signal may also excite the HD optimal statistic and the HD component
of the MCOS; and so on. The S/Ns quoted in Table 2
quantify how often we would expect to measure the observed value of the optimal statistic if only uncorrelated
noise is present, but they do not describe how often one
type of correlated noise would produce a given value of
the optimal statistic for a different type of correlation.

0

2

4

6

S/N

6
4.0
Â2 Γ(ξab ) [×10−30 ]

PDF

10−1

HD
Monopole

3.0

HD correlations
HD + monopole

2.0
1.0
0.0
-1.0
-2.0

γ = 13/3

0
30
60
90
120
150
180
Separation Angle Between Pulsars ξ [degrees]

Figure 16. Results of the MCOS analysis, which prefers a
model including both HD and monopole correlations. Top:
MCOS S/N for HD correlations (solid blue) and monopole
correlations (dashed orange), marginalized over curn13/3
noise-parameter posteriors. The vertical lines indicate the
mean S/Ns. We find a S/N of 3.4 ± 0.8 for HD correlations and 2.9 ± 0.8 for monopole correlations. Bottom:
Binned cross-correlations ρab (black error bars), computed
with MAP noise parameters from a curn13/3 run. The
solid blue and dashed orange curves show best-fit HD and
HD+monopole correlation patterns, corresponding to Â2 =
6.8×10−30 and to Â2HD = 5.5×10−30 , Â2monopole = 8×10−31 ,
respectively. The monopolar component accounts for the
vertical shift of the cross-correlations with respect to the HD
curve. We use the standard version of the optimal statistic
that does not include inter-pulsar correlations to compute
ρab , so the points and errors do not match those shown in
panel (c) of Figure 1.

This effect can be characterized using simulations (see
App. H.1), which report a p-value of 0.11 for the observed mean monopole statistic when a HD-correlated
signal with the MAP 15-year amplitude is included in
the simulated data sets. We conclude that there are
some indications of a possible monopole-correlated signal in the data with S/N comparable to but smaller than
the S/N for HD correlations; however, from simulations
we conclude that it is possible for such a signal to appear
in an MCOS analysis if only a HD-correlated stochastic
process is present.

## PDF page 29

Simulated Monopole S/N

NANOGrav 15-year Gravitational-Wave Background

5

0

−5
−5

Figure 17. Top: MCOS HD S/N values recovered in
the three simulations described in App. H.1, compared to
the MCOS HD S/N measured in the real data set (vertical
dashed red line), which has p-values of < 10−2 for simulations i and iii, and 0.64 for simulations ii. Bottom: MCOS
monopole S/N values recovered in the three simulations,
compared to the real-data MCOS monopole S/N (vertical
dashed red line), which has p-values of 4 × 10−2 , 1.1 × 10−1 ,
and < 10−2 for simulation i, ii, and iii respectively.
H. MULTIPLE-CORRELATION OPTIMAL

STATISTIC SIMULATIONS
In this appendix we obtain the distribution of the
MCOS over an ensemble of simulated data sets, with
the goal of characterizing the probability that the observed S/Ns could have been produced by pulsar noise
alone, or by a GWB with HD correlations. Unlike our
Bayesian analysis, the MCOS prefers a model that includes both HD and monopolar components. So we are
especially interested in asking how frequently we may
expect the observed MCOS monopole if the data contain only the GWB. In Apps. H.1 and H.2 we present two
different types of simulations: “astrophysical,” where we
generate synthetic data with MAP noise parameters inferred from the 15-year data set, both with and without
the GWB; and “model checking,” where we create data
replications following the hd13/3 posteriors for the real
data set. Note that neither simulation attempts to account for the monochromatic character of the putative
monopolar signal (see §5.2).
H.1. Astrophysical simulations
Following Pol et al. (2021), we generate simulated data
sets adopting MAP pulsar-noise parameters obtained
from the real data independently for each pulsar; these
“noise runs” include an additional power-law process to
reduce contamination between the putative GWB and
the pulsars’ intrinsic red noise (Taylor et al. 2022). We
produce 100 realizations each of three different simu-

29

0
5
15 yr Monopole S/N

Figure 18. Distribution of real-data and replicated MCOS
monopole S/Ns. Each point represents a draw η (k) from
hd13/3 posterior, which is used to simulate δtsim,(k) and to
compute both S/Ns. The replicated monopole S/N is greater
for 11% of the simulations.

lations: (i) injecting no spatially correlated power-law
GWB or excess uncorrelated common-spectrum noise;
(ii) injecting a spatially correlated power-law GWB with
amplitude 2.7 × 10−15 and spectral index 13/3; and (iii)
injecting no GWB or common-spectrum noise, but omitting the additional power-law process in the estimation
of intrinsic pulsar noise, with the goal of testing how
often excess common-spectrum noise is recognized as a
spatially correlated GWB.
We compute HD + monopole + dipole MCOS S/Ns
for all synthetic data sets (see Figure 17). The mean
HD S/Ns observed in the real data (see App. G) correspond to p-values of < 10−2 for simulations (i) and (iii),
and 0.64 for simulation (ii). The mean monopole S/Ns
observed in the real data set correspond to p-values of
4 × 10−2 , 1.1 × 10−1 , and < 10−2 for simulations (i),
(ii), and (iii) respectively. We conclude that it is unlikely that we would measure HD correlations at the
level observed in real data when no correlated signal
is present (simulation (i)) or when only uncorrelated
common-spectrum red noise is present (simulation (iii)).
In addition, the HD S/Ns obtained from a HD-correlated
GWB injection (simulation (ii)) are fully consistent with
the S/N observed in real data. By contrast, the observed
monopole S/N could have been produced by intrinsic
pulsar noise alone, or by a real HD signal.
H.2. Model-checking simulations
In App. H.1 we have tackled the question of monopole
S/N significance using simulations based on real-data
MAP estimates η MAP of pulsar-noise and GW parameters. In this appendix we adopt a procedure with

## PDF page 30

30

The NANOGrav Collaboration

a stronger Bayesian flavor, evaluating the MCOS on
a population of data replications created using hd13/3
as a generative model with noise hyperparameters η
drawn from the hd13/3 real-data posterior. This can be
seen also as a Bayesian model-checking exercise (Gelman
et al. 1996, 2013): if we find that the summary statistic of interest (the monopole MCOS) has a much more
extreme value in real data than in data replications,
we should suspect that the data model (here hd13/3 )
is missing something.
We perform the test by drawing 500 parameter vectors
{η (k) } from the hd13/3 real-data posterior; for each η (k)
we simulate a data set δtsim,(k) ∼ p(δt|η (k) ) and compare MCOS(δtsim,(k) ; η (k) ) with MCOS(δt; η (k) ). Our
notation emphasizes the dependence of the MCOS on
the pulsar noise parameters through the P matrices in
Equation 9. Figure 18 shows the resulting distribution
of monopole S/Ns. The replicated monopole S/N is
greater than its observed counterpart for 11% of the
draws. Thus, it is plausible that the MCOS could measure the observed monopole S/N in data that contain
only a HD-correlated GWB. Conversely, the observed
monopole S/N does not by itself suggest that hd13/3 is
misspecified.
