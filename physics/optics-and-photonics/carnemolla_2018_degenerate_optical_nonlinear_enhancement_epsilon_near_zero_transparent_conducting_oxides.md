Source: see manifest row of the PDF
PDF sha256: adb91ceb91cdd00891d34eb442ba169d7b379f761b9bc81941e218219dddccc9
License: CC-BY-4.0
Language: eng
Fidelity: machine-gated

# Transcription of carnemolla_2018_degenerate_optical_nonlinear_enhancement_epsilon_near_zero_transparent_conducting_oxides.pdf

Transcription of `carnemolla_2018_degenerate_optical_nonlinear_enhancement_epsilon_near_zero_transparent_conducting_oxides.pdf` in this directory, 9 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-9 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Vol. 8, No. 11 | 1 Nov 2018 | OPTICAL MATERIALS EXPRESS 3392

Degenerate optical nonlinear enhancement in
epsilon-near-zero transparent conducting
oxides
ENRICO GIUSEPPE CARNEMOLLA,1 LUCIA CASPANI,2 CLAYTON DEVAULT,3
MATTEO CLERICI,4 STEFANO VEZZOLI,5 VINCENZO BRUNO,6 VLADIMIR M.
SHALAEV,7 DANIELE FACCIO,6 ALEXANDRA BOLTASSEVA,7 AND MARCELLO
FERRERA1
1

Institute of Photonics and Quantum Sciences, Heriot-Watt University, SUPA, Edinburgh, Scotland,
EH14 4AS, UK
2
Institute of Photonics, Department of Physics, University of Strathclyde, Glasgow G1 1RD, UK
3
Dept. of Physics & Astronomy and Birck Nanotechnology Center, Purdue University, West Lafayette,
IN, 47907, USA
4
School of Engineering, University of Glasgow, Glasgow G12 8QQ, UK
5
Department of Physics, King’s College London, Strand, London WCR 2LS, UK
6
School of Physics and Astronomy, University of Glasgow, Glasgow G12 8QQ, UK
7
School of Electrical and Computer Engineering, Purdue University, West Lafayette, IN 47907, USA
*m.ferrera@hw.ac.uk
www.asn-lab.org

Abstract: We report the simultaneous increase of both nonlinear Kerr coefficient n2 and
third-order nonlinear susceptibility χ(3) in aluminum zinc oxide (AZO) attained by pumpprobe spectroscopy in a frequency degenerate configuration. Our experiments demonstrate a
6-fold enhancement in the third-order nonlinear susceptibility and over one order of
magnitude increase in the nonlinear Kerr coefficient, while also determining two distinct
operational wavelengths for optimal modulation of either the real or the imaginary part of the
complex refractive index. These results, besides providing a broader spectral characterization
of the third-order nonlinearity in AZO thin films, also show the fundamental advantages of
performing nonlinear optics via degenerate excitation near the ENZ wavelength.
Published by The Optical Society under the terms of the Creative Commons Attribution 4.0 License.
Further distribution of this work must maintain attribution to the author(s) and the published article’s title,
journal citation, and DOI.

1. Introduction
Over the past decade, nanophotonics research has been heavily focusing on developing and
advancing material platforms for practical nanophotonic devices that are low-loss, tailorable
and can easily be integrated with existing semiconductor technologies. On the direction of
low-loss CMOS compatible technologies and metal-free nanophotonics, the scientific
community is moving towards all-dielectric components [1], where dielectric materials
replace the metallic inclusions in high refractive index contrast systems [2]. Important proofs
of concept include III-V semiconductor metasurface [3], dielectric metamaterials [4,5], and
multilayer nanopillars [6]. Although extremely promising, all-dielectric nano-devices do not
retain many of the desirable attributes of plasmonic devices while the requirement of
operating in high index-contrast systems poses further limitations to the possible
combinations of usable materials. Further limitations in the material choice arise from the
requirement of having high quality thin films, whose optical properties are linked to good
morphological and crystallographic matching with the surrounding environment.
Transparent Conductive Oxides (TCOs) have recently emerged as favorable hybrid
materials for plasmonic applications because of their unique properties stemming from a large
#340528
Journal © 2018

https://doi.org/10.1364/OME.8.003392
Received 24 Jul 2018; revised 28 Sep 2018; accepted 2 Oct 2018; published 17 Oct 2018

## PDF page 2

Vol. 8, No. 11 | 1 Nov 2018 | OPTICAL MATERIALS EXPRESS 3393

intrinsic bandgap and high carrier concentrations. The latter feature pushes the Fermi level
into the conduction band and widens the bandgap of the intrinsic material via the MossBurstein shift. Among the most exploited TCOs we find Indium Tin Oxide (ITO), Aluminum
Zinc Oxide (AZO), Gallium Zinc Oxide (GZO) and Indium Cadmium Oxide (ICO). These
compounds are routinely used for industrial purposes to fabricate touch-screen displays and
photovoltaic systems and only recently they have become metal substitutes for plasmonic
applications [7].
The use of TCOs for integrated photonic applications is also justified by their unique
nonlinear properties. For instance, photoexcitation was exploited in nanostructured nonlinear
systems by Guo et al. for both modulating the material absorption via interband excitation [8]
and tuning the mode resonance of localized plasmons using intraband nonlinearities [9].
TCO-mediated all-optical control of plasmon mode resonances in metallic nanoantennas has
also been demonstrated in [10,11], where ITO-gold systems were employed.
Following the idea of increasing optical nonlinearities even further, we notice that TCOs
allow to engineer the material dielectric permittivity so that it approaches zero at fundamental
operational wavelengths across the telecom band. This can be attained by altering fabrication
parameters and material stoichiometry. These Epsilon-Near-Zero (ENZ) conditions bring the
optical nonlinearities to unprecedented levels. In certain cases, for high pump intensity, the
optically induced change in the complex refractive index can be fitted to a semi-empirical
model accounting for the standard Taylor series expansion of the dielectric polarization
density inclusive of higher-order nonlinear susceptibility terms up to χ(7) [12–14]. These
results are of fundamental interest because they might be key to overcome the typical
nonlinear trade-off between magnitude and speed which has hampered the development of
practical integrated nonlinear devices for decades already. TCOs, under opportune
experimental conditions, can boost the typical figure of merit of nonlinear photonic devices
(FoM = n2/α, where n2 is the nonlinear refractive index and α represents the linear losses of
the material) by 5 orders of magnitude, making this class of material a game changer in
integrated photonics. In recent years, a few seminal works dealing with enhanced
nonlinearities in bulk TCOs probed at ENZ wavelengths, have been published. In particular,
in [15] Kinsey et al. reported ultra-fast and large interband nonlinearities in AZO thin films
probed at the ENZ wavelength. An important feature of this work deals with the particular
fabrication procedure developed to attain sub-picosecond recombination time [16]. More
specifically, all the thin films used in our experiments have been grown by using pulsed laser
deposition performed in an oxygen deprived atmosphere. The induced oxygen vacancies have
the twofold effect of increasing free carriers and enlarging the number of recombination
channels. The latter characteristic being responsible for shortening the photocarriers
recombination time by about two orders of magnitude with respect to commercially available
TCO films.
Because of the hybrid nature of TCOs being in the middle between semiconductors and
metals, both interband and intraband optical nonlinearities can be efficiently excited [17,18].
These nonlinearities can be judiciously combined to increase the material bandwidth up to
few THz, perform all-optical three-state logic operations, and attain ultra-fast signal routing
[19]. Such large and ultrafast modulation of the material optical properties has been exploited
also for efficient third harmonic generation and four-wave mixing in ITO and AZO films
[20,21].
Finally, very recently, tuning metallic nano-antennas in resonance with the ENZ
wavelength of an underlying TCO substrate, has been proved to be extremely effective for
maximizing the effective intensity-dependent index change [22,23]. The recorded
extraordinary nonlinear behavior is directly linked to a condition of “strong coupling”
between the antennas and the substrate which leads to unity order refractive index change and
an n2 coefficient up to six orders of magnitude higher than the one of silica glass.

## PDF page 3

Vol. 8, No. 11 | 1 Nov 2018 | OPTICAL MATERIALS EXPRESS 3394

Despite of all the remarkable results reported in literature, there is still a long way to go
for a full exploration of nonlinear optics in TCO-based systems. For instance, TCOs’
nonlinear optical response has been investigated only within a relatively narrow spectral
window including the visible and a small fraction of the NIR range. In particular, great
interest has been dedicated to the enhancement of the nonlinear refractive index due to the
index-near-zero nature of the material without exploring regimes of high intrinsic third-order
nonlinear susceptibility χ(3). Here we present one possible strategy to further enlarge the
intensity dependent refractive index change. Our approach relies on the simultaneous increase
of the χ(3) and of the nonlinear enhancement due to the ENZ regime. This is quite different
from [17] where a flat χ(3) around the cross-over wavelength allowed to define an overall
nonlinear enhancement factor that is solely dependent on linear indices.
Starting from few semi-empirical models (see section 2), which link first- and third-order
material susceptibilities, we gained some intuition about the general trend of the nonlinear
dispersion for the simplest case of degenerate excitation. Subsequently, by means of a
pump/probe set-up, where the operational wavelength is set within the ENZ material window,
we proceeded with the quantitative evaluation of the predicted nonlinear enhancement.
2. Experimental analysis and methodology
The fundamental goal of our study is to assess how far we can go in increasing the nonlinear
Kerr coefficient n2 of TCOs. Establishing this limit will provide an important insight into the
carrier dynamics in TCOs and will have impact on the design on novel nonlinear devices.
Increase in the nonlinear effects can be attained either by acting on the third-order intrinsic
nonlinear susceptibility or by exploiting the index-near-zero properties of TCOs. For instance,
the nonlinear photonics community used to rely on the former approach. Here we combine
the effects of both approaches. For the sake of clarity we describe in the following how n2,
χ(3), and the linear refractive index nL are linked together.
Considering a pump-probe configuration, the mathematical relation linking the nonlinear
refractive index n2 experienced by the probe beam with the third-order susceptibility χ(3)
(function of the pump and probe parameters) and the probe linear refractive index n = nr + i ni
is [24]:
n2 =

χ (3)

3
2ε 0 c n

pump
r

( nr + ini )

(1)

where n2 and χ(3) are also complex quantities, ε0 is the vacuum permittivity, c is the speed of
light in vacuum, nr,i are the real and imaginary part of the refractive index at the probe
wavelength, and nrpump is the real part of the linear refractive index at the optical pump
wavelength. The dependence of n2 on χ(3) implies that a straightforward tactic to increase the
nonlinear response is to utilize the largest components of a material’s third-order tensor χ(3).
This task is challenging because each tensor element will depend on both pump and probe
wavelengths. To facilitate this goal, different semi-empirical methods that link the linear
susceptibility χ(1) to the χ(3) are available in literature to predict the nonlinear properties of
materials [25]. The task is further simplified if the equations are calculated for the degenerate
case where all the photons involved in the parametric process have the same energy.
In Fig. 1(a), we plot the complex third-order nonlinear susceptibility χ(3) as a function of
the probe wavelength for three cases: i) Wang’s model (dashed lines) [26]; ii) Miller’s model
(solid lines) [24,27]; iii) numerical evaluation of χ(3) based on experimental results ( +
markers). The experimental procedure to measure χ(1) and χ(3) will be explained later in this
section.

## PDF page 4

Vol. 8, No. 11 | 1 Nov 2018 | OPTICAL MATERIALS EXPRESS 3395

Fig. 1. (a) Real and imaginary part of the experimentally measured nonlinear susceptibility χ(3)
(cross points) compared with the χ(3) trend obtained by the application of the Wang (dashed
curves) and Miller (solid curves) relations in the wavelength range 1120 nm - 1450 nm. (b)
Real (blue curve) and imaginary (red curve) part of the AZO film permittivity. The black
dashed lines indicate the cross-over wavelength, which was λENZ = 1360 nm. (c) Comparison
between the nonlinear Kerr coefficient n2r for the degenerate case (λpump = λprobe, magenta line)
and for the non-degenerate case (λpump = 787 nm, black line) as a function of λpump in the
wavelength range 1120 nm - 1450 nm. The values of the n2r are obtained using the Eq. (2).
Black and magenta asterisks indicate non-degenerate and degenerate experimental data,
respectively. (d) Comparison between the nonlinear absorption coefficient β2 for the
degenerate case (λpump = λprobe, magenta line) and for the non-degenerate case (λpump = 787 nm,
black line) as a function of λprobe in the wavelength range 1120 nm - 1450 nm. The values of
the n2i are obtained using the Eq. (3) and used in the Eq. (4) to calculate the β2. Black and
magenta asterisks indicate non-degenerate and degenerate experimental data, respectively.

Both models, although being differently dependent on the linear susceptibility χ(1), predict
a similar monotonic behavior for both real and imaginary parts of the χ(3). The same trend is
also supported by our experiments. As previously mentioned, the three plots are for the case
of degenerate optical excitation and they refer to a sample which exhibits cross-over
wavelength at 1360 nm. Wang and Miller curves are multiplied by a factor 1 × 10−19 m2/V2 to
be compared with the experimental evaluation of the χ(3). The values of the χ(1) are calculated
from the simple relation χ(1) = εL - 1, where εL is the linear permittivity estimated following
the process reported later in this section (Fig. 1(b)). The graphs, which for experimental
limitation are plotted within the wavelength range 1120 nm - 1450 nm, show a clear increase
of the real part of the nonlinear susceptibility χr(3) for longer wavelengths while an almost
symmetrical trend towards negative values is exhibited by the imaginary part χi(3). Note that
the two semi-empirical models are used only to predict the general trend of the χ(3) dispersion
without any aim at providing its quantitate evaluation. The latter task is out of reach for the
impossibility in evaluating within acceptable accuracy the multiplicative constants of the
empirical models (Miller’s → χ(3) ∝ [ χ(1)]4; Wang’s → χ(3) ∝ [ χ(1)]2).

## PDF page 5

Vol. 8, No. 11 | 1 Nov 2018 | OPTICAL MATERIALS EXPRESS 3396

To combine this trend with the nonlinear enhancement at the ENZ wavelength reported by
Caspani and co-authors [17], we recall the representation of the n2 into its real (n2r) and
imaginary (n2i) parts,
n2 r =

3 nr χ r(3) + ni χ i(3)
2ε 0 c
D

(2)

n2i =

3 nr χ r(3) − ni χ i(3)
2ε 0 c
D

(3)

where D = nrpump (nr2 + ni2). In [17] it was shown that under the condition χr(3) ≈χi(3) ≈const.,
which was adequately met for the non-degenerate case, n2r and n2i depend on the
enhancement factors Fr = (nr + ni)/D and Fi = (nr - ni)/D, respectively. For this case, near the
ENZ wavelength λENZ, Fr produces a peak enhancement of the n2r, while n2i becomes very
small in absolute value thus inducing a reduction of the nonlinear absorption coefficient β2,
defined as:

β 2 = 4π n2i / λ

(4)

where λ is the operational wavelength in vacuum.
For the degenerate case considered here, the condition χr(3) ≈χi(3) ≈const is no longer valid
and the enhancement of the intensity dependent refractive index within the ENZ window is
also mediated by the third-order nonlinear susceptibility. Figure 1(b) and 1(c) make a direct
comparison between degenerate and non-degenerate case (λpump = 787 nm) for both real and
imaginary nonlinear refractive index, respectively. These graphs illustrate how optical
nonlinearities are largely enhanced by employing a degenerate pumping scheme (see “Key
findings and discussion”). Our results prove that the degenerate optical excitation in the ENZ
region is optimal to fully exploit the nonlinear capability of TCOs. The nonlinear material
response was measured by using a standard pump and probe set-up in its degenerate
configuration as sketched in Fig. 2. The target sample was a 900-nm thin film of oxygendeprived aluminum zinc oxide (AZO) [15,28]. The film was grown by pulsed laser deposition
(PVD Products, Inc.) using a target of AZO via a 248 nm KrF excimer laser (Lambda Physik
GmbH) [29,30]. The fundamental source of our optical set-up was a Ti:Sapphire laser (λ =
787 nm) with a repetition rate of 100 Hz providing an optical pulse of ≈100 fs vertically
polarized. The output was directed into an Optical Parametric Amplifier (OPA) which
provided both pump and probe signals.

Fig. 2. Sketch of the degenerate pump and probe setup. A Ti:Sapphire laser pumps the optical
parametric oscillator, whose signal is split in a high intensity pump and a weak probe, both
vertically polarized and incident in the AZO sample with angle of incidence <10°.

We first measured the linear (i.e. no pump) transmission and reflection in the wavelength
range between 1120 nm and 1550 nm. Then we extracted the linear permittivity εL by means

## PDF page 6

Vol. 8, No. 11 | 1 Nov 2018 | OPTICAL MATERIALS EXPRESS 3397

of an inverse transfer matrix method (for details see [31]), finding the ENZ wavelength at λENZ
≈1360 nm. We investigated the nonlinear properties of our AZO film by first recording both
transient transmissivity and reflectivity of the probe signal as a function of the time delay ∆τ
between pump and probe. This was done for different operational wavelengths (within the
range 1120 nm and 1550 nm) and for different incident pump intensities Ipump (within the
range 20 GW/cm2 and 90 GW/cm2), which were corrected by subtracting the portion of the
pump reflected at the interface air-AZO (Îpump). Subsequently, the nonlinear permittivity εNL
was extracted from the measurements of transmission and reflection at ∆τ = 0 by means of
inverse transfer matrix method. Finally, the third-order susceptibility χ(3) was calculated using
the following relation:

χ (3) (ω pump , ω probe ) =

nrpump ε 0 c ∂ε NL (ω probe , I pump )
3
∂ I pump

(5)

where ωpump and ωprobe are the pump and the probe angular frequencies, respectively, and the
derivative with respect to the pump intensity is performed where εNL(Îpump) is approximately
linear [24]. The χ(3) was then used to find the nonlinear Kerr coefficients n2r and n2i using Eq.
(2) and (3), while the nonlinear absorption coefficient was calculated by Eq. (4). The values
of the εNL were also used to determine the variation of the refractive index ∆n, from the
following relations:
Δnr ,i = nNLr ,i − nLr ,i

(6)

where ∆nr and ∆ni are the real and imaginary part of ∆n, respectively. The terms nNLr and nNLi
are the real and imaginary part of the nonlinear refractive index, respectively, while the nLr
and nLi are the real and imaginary part of the linear refractive index. These four quantities can
be calculated from Eq. (7) and (8):
nLr =
nLi =

ε L + ε Lr
2

ε L − ε Lr
2

, nNLr =
, nNLi =

ε NL + ε NLr
2

ε NL − ε NLr
2

(7)

(8)

3. Key findings and discussion

The χr(3) extracted from our experiments is almost 6 times higher than that of the nondegenerate case [17], with values up to 3.5 × 10−19 m2/V2, while the χi(3) changes sign and
becomes negative. Figure 3(a) and 3(b) show ∆nr and ∆ni as a function of both Ipump and
wavelength, respectively. We observe that the maximum change of the refractive index,
corresponding to the highest pump intensity, is shifted in wavelength of about 80 nm with
respect to the maximum change ∆nr induced by the lowest Ipump. This spectral shift is
understood to be due to the shift in the ENZ wavelength due to the redistribution of electrons
in the conduction band caused by the intraband excitation [32].
In this work, the maximum value of the n2r was measured to be 5.17 × 10−12 cm2/W at
1311 nm, about 13 times larger than the value measured in the non-degenerate case. On the
other hand, the measured β2 was found to be negative in sign and monotonically decreasing
for increasing values of wavelength.

## PDF page 7

Vol. 8, No. 11 | 1 Nov 2018 | OPTICAL MATERIALS EXPRESS 3398

Fig. 3. Variation of the real (a) and imaginary (b) part of the refractive index ∆nr and ∆ni,
respectively, as a function of both pump/probe wavelength and the incident pump intensity
Ipump.

For operational purposes, it is useful to report both the minimum of β2 and its value at the
wavelength of maximum n2r, which are β2 = −1.4 × 10−6 cm/W (at 1449 nm, wavelength of
minimum β2) and β2 = −7.1 × 10−7 cm/W (at 1311nm, wavelength of maximum n2r),
respectively. This prove that for an opportune choice of the operational wavelength, the
degenerate configuration allows for considerably enhanced nonlinearities or efficient ultrafast saturable absorption [33]. In addition, because the peak of ∆nr is separated from the dip
of ∆ni by a large wavelength distance (~100 nm), AZO thin films could be exploited for
efficient ultra-fast modulation of optical signals in either amplitude or phase. Moreover, it is
worth noting that a ∆nr of about 0.17 was obtained for a Ipump of 90 GW/cm2 at around 1350
nm, whereas in the non-degenerate case the same ∆nr were observed at the same wavelength
for a Ipump of 400 GW/cm2 [17].
The very high nonlinearities reported in the present manuscript can also be used to
manipulate the spectral properties of optical pulses [17,19,32,34,35] and for applications in
ultrafast beam steering and wavefront shaping [36,37]. Finally, the same system can produce
highly efficient four-wave mixing, as already shown by Vezzoli and associates [21] or used as
an active medium in dynamic nanocavities [38].
4. Conclusion

In conclusion, the present paper puts into context the emerging field of TCO-based
plasmonics starting from material considerations and taking into account few among the most
important recent achievements towards metal-free nanophotonics. We report our recent study
of ultra-fast optical nonlinearities in AZO thin films probed at ENZ wavelengths and driven
by degenerate optical excitation. It is important to underline that the strategy presented in this
paper differs from the approach reported in [17], because the nonlinear response of the
degenerate case is mediated also by an increased third-order susceptibility. Our experimental
conditions are effective in enhancing the nonlinear Kerr coefficient by over one order of
magnitude and the third-order nonlinear susceptibility by 6 times when making a comparison
with the non-degenerate pumping scheme. The largest induced changes in the real and
imaginary refractive index have a wavelength separation of about 100 nm. This creates two
well defined operational wavelengths which can allow for efficient modulation of the optical
signal operated on either the amplitude or the phase of the propagating radiation. Our
observations make the degenerate nonlinearities of AZO thin films suitable for various
applications, ranging from the design of nanophotonics devices to the study of the
fundamental physics in time-varying media. Relevant data can be accessed at [39] under
ODC-By license.

## PDF page 8

Vol. 8, No. 11 | 1 Nov 2018 | OPTICAL MATERIALS EXPRESS 3399

Funding

M.F. acknowledges support from EPSRC (UK, Grant EP/P019994/1) and from The Royal
Society (Project num.: RG2017R1). M.C. acknowledges support from EPSRC and Innovate
UK (UK, Grant EP/S001573/1, EP/R043299/1), C.D., A.B., V.M.S. acknowledge support
from the U.S. Department of Energy, Office of Basic Energy Sciences, Division of Materials
Sciences and Engineering under Award DE-SC0017717 (C.D., Sample Fabrication) and
support from Air Force Office of Scientific Research (AFOSR) Grant No. FA9550-18-10002”. D.F. acknowledges financial support from EPSRC (UK, Grant No. EP/M009122/1).
References
1.

D. G. Baranov, D. A. Zuev, S. I. Lepeshov, O. V. Kotov, A. E. Krasnok, A. B. Evlyukhin, and B. N. Chichkov,
“All-dielectric nanophotonics: the quest for better materials and fabrication techniques,” Optica 4(7), 814–825
(2017).
2. I. Staude and J. Schilling, “Metamaterial-inspired silicon nanophotonics,” Nat. Photonics 11(5), 274–284 (2017).
3. S. Liu, M. B. Sinclair, S. Saravi, G. A. Keeler, Y. Yang, J. Reno, G. M. Peake, F. Setzpfandt, I. Staude, T.
Pertsch, and I. Brener, “Resonantly Enhanced Second-Harmonic Generation Using III-V Semiconductor AllDielectric Metasurfaces,” Nano Lett. 16(9), 5426–5432 (2016).
4. Z Yue, B. Cai, L. Wang, X. Wang, and M. Gu, “Intrinsically core-shell plasmonic dielectric nanostructures with
ultrahigh refractive index,” Sci. Adv. 2, 1501536 (2016).
5. G. Kang, J. Yoo, J. Ahn, and K. Kim, “Transparent dielectric nanostructures for efficient light management in
optoelectronic applications,” Nano Today 10(1), 22–47 (2015).
6. M. R. Shcherbakov, S. Liu, V. V. Zubyuk, A. Vaskin, P. P. Vabishchevich, G. Keeler, T. Pertsch, T. V. Dolgova,
I. Staude, I. Brener, and A. A. Fedyanin, “Ultrafast all-optical tuning of direct-gap semiconductor metasurfaces,”
Nat. Commun. 8(1), 17 (2017).
7. J. Kim, S. Choudhury, C. DeVault, Y. Zhao, A. V. Kildishev, V. M. Shalaev, A. Alù, and A. Boltasseva,
“Controlling the Polarization State of Light with Plasmonic Metal Oxide Metasurface,” ACS Nano 10(10),
9326–9333 (2016).
8. P. Guo, R. P. H. Chang, and R. D. Schaller, “Transient negative optical nonlinearity of indium oxide nanorods
arrays in the full-visible range,” ACS Photonics 4(6), 1494–1500 (2017).
9. P. Guo, R. D. Schaller, J. B. Ketterson, and R. P. H. Chang, “Ultrafast switching of tunable infrared plasmons in
indium tin oxide nanorod arrays with large absolute amplitude,” Nat. Photonics 10(4), 267–273 (2016).
10. M. Abb, P. Albella, J. Aizpurua, and O. L. Muskens, “All-Optical Control of a Single Plasmonic NanoantennaITO Hybrid,” Nano Lett. 11(6), 2457–2463 (2011).
11. M. Abb, Y. Wang, C. H. de Groot, and O. L. Muskens, “Hotspot-mediated ultrafast nonlinear control of
multifrequency plasmonic nanoantennas,” Nat. Commun. 5(1), 4869 (2014).
12. I. Liberal and N. Engheta, “Near-zero refractive index photonics,” Nat. Photonics 11(3), 149–158 (2017).
13. X. Niu, X. Hu, S. Chu, and Q. Gong, “Epsilon-Near-Zero Photonics: A New Platform for Integrated Devices,”
Adv. Opt. Mater. 6(10), 1701292 (2018).
14. O. Reshef, E. Giese, M. Zahirul Alam, I. De Leon, J. Upham, and R. W. Boyd, “Beyond the perturbative
description of the nonlinear optical response of low-index materials,” Opt. Lett. 42(16), 3225–3228 (2017).
15. N. Kinsey, C. DeVault, J. Kim, M. Ferrera, V. M. Shalaev, and A. Boltasseva, “Epsilon-near-zero Al-doped ZnO
for ultrafast switching at telecom wavelengths,” Optica 2(7), 616–622 (2015).
16. A. M. Urbas, Z. Jacob, L. Dal Negro, N. Engheta, A. D. Boardman, P. Egan, A. B. Khanikaev, V. Menon, M.
Ferrera, N. Kinsey, C. DeVault, J. Kim, V. M. Shalaev, A. Boltasseva, J. Valentine, C. Pfeiffer, A. Grbic, E.
Narimanov, L. Zhu, S. Fan, A. Alù, E. Poutrina, N. M. Litchinitser, M. A. Noginov, K. F. Macdonald, E. Plum,
X. Liu, P. F. Nealey, C. R. Kagan, C. B. Murray, D. A. Pawlak, I. I. Smolyaninov, V. N. Smolyaninova, and D.
Chanda, “Roadmap on optical metamaterials,” J. Opt. 18(9), 093005 (2016).
17. L. Caspani, R. P. M. Kaipurath, M. Clerici, M. Ferrera, T. Roger, J. Kim, N. Kinsey, M. Pietrzyk, A. Di Falco,
V. M. Shalaev, A. Boltasseva, and D. Faccio, “Enhanced nonlinear refractive index in ε-near-zero materials,”
Phys. Rev. Lett. 116(23), 233901 (2016).
18. M. Z. Alam, I. De Leon, and R. W. Boyd, “Large optical nonlinearity of indium tin oxide in its epsilon-near-zero
region,” Science 352(6287), 795–797 (2016).
19. M. Clerici, N. Kinsey, C. DeVault, J. Kim, E. G. Carnemolla, L. Caspani, A. Shaltout, D. Faccio, V. Shalaev, A.
Boltasseva, and M. Ferrera, “Controlling hybrid nonlinearities in transparent conducting oxides via two-colour
excitation,” Nat. Commun. 8, 15829 (2017).
20. A. Capretti, Y. Wang, N. Engheta, and L. Dal Negro, “Enhanced third-harmonic generation in Si-compatible
epsilon-near-zero indium tin oxide nanolayers,” Opt. Lett. 40(7), 1500–1503 (2015).
21. S. Vezzoli, V. Bruno, C. DeVault, T. Roger, V. M. Shalaev, A. Boltasseva, M. Ferrera, M. Clerici, A. Dubietis,
and D. Faccio, “Optical Time Reversal from Time-Dependent Epsilon-Near-Zero Media,” Phys. Rev. Lett.
120(4), 043902 (2018).
22. M. Z. Alam, S. A. Schulz, J. Upham, I. De Leon and R. W. Boyd, “Unity-order nonlinear index change in a
metasurface”, Proc. Photonics North 2017, 255-wx55–265 (2017).

## PDF page 9

Vol. 8, No. 11 | 1 Nov 2018 | OPTICAL MATERIALS EXPRESS 3400

23. M. Z. Alam, S. A. Schulz, J. Upham, I. De Leon, and R. W. Boyd, “Large optical nonlinearity of nanoantennas
coupled to an epsilon-near-zero material,” Nat. Photonics 12(2), 79–83 (2018).
24. R. W. Boyd, Nonlinear Optics, 3rd ed. (Elsevier, 2008).
25. E. M. Vogel, M. J. Weber, and D. M. Krol, “Nonlinear optical phenomena in glass,” Phys. Chem. Glasses 32(6),
231–254 (1991).
26. C. C. Wang, “Empirical Relation between the Linear and the Third-order Nonlinear Optical Susceptibilities,”
Phys. Rev. B 2(6), 2045–2048 (1970).
27. R. C. Miller, “Optical second harmonic generation in piezoelectric crystals,” Appl. Phys. Lett. 5(1), 17–19
(1964).
28. G. V. Naik, J. Liu, A. V. Kildishev, V. M. Shalaev, and A. Boltasseva, “Demonstration of Al:ZnO as a
plasmonic component for near-infrared metamaterials,” Proc. Natl. Acad. Sci. U.S.A. 109(23), 8834–8838
(2012).
29. A. V. Singh, R. M. Mehra, N. Buthrath, A. Wakahara, and A. Yoshida, “Highly conductive and transparent
aluminum-doped zinc oxide thin films prepared by pulsed laser deposition in oxygen ambient,” J. Appl. Phys.
90(11), 5661–5665 (2001).
30. H. Kim, J. Horwitz, S. Qadri, and D. Chrisey, “Epitaxial growth of Al-doped ZnO thin films grown by pulsed
laser deposition,” Thin Solid Films 420–421, 107–111 (2002).
31. R. M. Kaipurath, M. Pietrzyk, L. Caspani, T. Roger, M. Clerici, C. Rizza, A. Ciattoni, A. Di Falco, and D.
Faccio, “Optically induced metal-to-dielectric transition in Epsilon-Near-Zero metamaterials,” Sci. Rep. 6(1),
27700 (2016).
32. P. Kelly and L. Kuznetsova, “Pulse shaping in the presence of enormous second-order dispersion in
Al:ZnO/ZnO epsilon-near-zero metamaterial,” Appl. Phys. B 124(4), 60 (2018).
33. J. Guo, H. Zhang, C. Zhang, Z. Li, Y. Sheng, C. Li, X. Bao, B. Man, Y. Jiao, and S. Jiang, “Indium tin oxide
nanocrystals as saturable absorbers for passively Q-switched erbium-doped fiber laser,” Opt. Mater. Express
7(10), 3494–3502 (2017).
34. M. Ferrera and E. G. Carnemolla, “Ultra-fast transient plasmonics using transparent conductive oxides,” J. Opt.
20(2), 024007 (2018).
35. A. Shaltout, A. Kildishev, and V. Shalaev, “Time-varying metasurfaces and Lorentz non-reciprocity,” Opt.
Mater. Express 5(11), 2459–2467 (2015).
36. S. B. Raghunathan, H. F. Schouten, W. Ubachs, B. E. Kim, C. H. Gan, and T. D. Visser, “Dynamic beam
steering from a subwavelength slit by selective excitation of guided modes,” Phys. Rev. Lett. 111(15), 153901
(2013).
37. H. Frostig, E. Small, A. Daniel, P. Oulevey, S. Derevyanko, and Y. Silberberg, “Focusing light by wavefront
shaping through disorder and nonlinearity,” Optica 4(9), 1073–1079 (2017).
38. J. Kim, E. G. Carnemolla, C. DeVault, A. M. Shaltout, D. Faccio, V. M. Shalaev, A. V. Kildishev, M. Ferrera,
and A. Boltasseva, “Dynamic Control of Nanocavities with Tunable Metal Oxides,” Nano Lett. 18(2), 740–746
(2018).
39. DOI: 10.17861/f9701bb5-2534-4f91-bd25-2e605b22e0f0
