Source: https://doi.org/10.1103/PhysRevLett.126.063602
PDF sha256: e606ea96881ef6b0e56c2cd987017250d612ce8069d7f3f64573f44fe6b67fb6
License: https://creativecommons.org/licenses/by/4.0/

# Transcription of ollivier_2021_hong_ou_mandel_interference_imperfect_single_photon_sources.pdf

Transcription of `ollivier_2021_hong_ou_mandel_interference_imperfect_single_photon_sources.pdf` in this directory, 6 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-6 from the PDF's own text layer (pdftotext version 26.10.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

PHYSICAL REVIEW LETTERS 126, 063602 (2021)

Hong-Ou-Mandel Interference with Imperfect Single Photon Sources
H. Ollivier,1 S. E. Thomas ,1,* S. C. Wein ,2 I. Maillette de Buy Wenniger ,1 N. Coste,1 J. C. Loredo ,1 N. Somaschi,3
A. Harouri,1 A. Lemaitre ,1 I. Sagnes ,1 L. Lanco ,1,4 C. Simon ,2 C. Anton ,1 O. Krebs ,1 and P. Senellart1,†
1

Centre for Nanosciences and Nanotechnology, CNRS, Université Paris-Saclay,
UMR 9001, 10 Boulevard Thomas Gobert, 91120 Palaiseau, France
2
Institute for Quantum Science and Technology and Department of Physics and Astronomy, University of Calgary,
Calgary, Alberta, Canada T2N 1N4
3
Quandela SAS, 10 Boulevard Thomas Gobert, 91120 Palaiseau, France
4
Université Paris Diderot—Paris 7, 75205 Paris CEDEX 13, France
(Received 4 May 2020; accepted 8 October 2020; published 12 February 2021)
Hong-Ou-Mandel interference is a cornerstone of optical quantum technologies. We explore both
theoretically and experimentally how unwanted multiphoton components of single-photon sources affect
the interference visibility, and find that the overlap between the single photons and the noise photons
significantly impacts the interference. We apply our approach to quantum dot single-photon sources to
access the mean wave packet overlap of the single-photon component. This study provides a consistent
platform with which to diagnose the limitations of current single-photon sources on the route towards the
ideal device.
DOI: 10.1103/PhysRevLett.126.063602

Quantum interference of indistinguishable single
photons is a critical element of quantum technologies. It
allows the implementation of logical photon-photon gates
for quantum computing [1,2] as well as the development of
quantum repeaters for secure long distance communications [3,4]. The development of efficient sources of single
and indistinguishable photons has become a challenge
of the utmost importance in this regard, with two predominant, distinct approaches. The first one is based on
nonlinear optical photon pair production [5,6], and multiplexing of heralded single photon sources is being explored
to overcome an intrinsic inefficiency [7–10]. The other is
based on single quantum emitters such as semiconductor
quantum dots [11,12] where ever-growing control of the
solid-state emitter has enabled the combination of high
efficiency and high indistinguishability [13–16].
The standard method to quantify the indistinguishability
of single-photon wavepackets is to perform Hong-OuMandel (HOM) interference [17]. In perfect HOM interference, two indistinguishable single photons incident at
each input of a 50∶50 beam splitter will exit the beam
splitter together, resulting in no two-photon coincidental
detection events at both outputs. In practice, however, the
two inputs only exhibit partial indistinguishability

Published by the American Physical Society under the terms of
the Creative Commons Attribution 4.0 International license.
Further distribution of this work must maintain attribution to
the author(s) and the published article’s title, journal citation,
and DOI.

0031-9007=21=126(6)=063602(6)

described by a nonunity mean wave packet overlap M s
(also defined as the single-photon trace purity [18,19]).
Partial indistinguishability of the input states leads to
coincidental detection events at the outputs and reduces
the HOM interference visibility. The interference visibility
V HOM can therefore give direct access to the single-photon
indistinguishability, M s ¼ V HOM [19].
For nonideal single-photon sources, for which the
photonic wave packets present a residual multiphoton
component, the HOM visibility remains the relevant
quantity that determines the quality of the above-mentioned
quantum operations. However, the visibility of HOM
interference is reduced due to multiphoton contributions,
even if Ms ¼ 1, i.e., for an ideal single-photon indistinguishability. In most cases, the multiphoton component of
the photonic wave packet, characterized by the second
order intensity autocorrelation at zero time delay gð2Þ ð0Þ,
depends on the system parameters in a manner that is
completely independent of the single photon indistinguishability, and it is critical to have tools to access the latter in
order to understand the physics at play and improve the
performance of single photon sources (SPSs).
Here we explore both theoretically and experimentally
HOM interference with imperfect SPSs. Previously, the
impact of multiphoton contributions on HOM interference
has been investigated in the limited case where the additional photons are in the same spectral and temporal mode
as the predominant ones [20–22]. It has been shown that the
visibility of HOM interference in this case is given by
V HOM ¼ M tot − gð2Þ ð0Þ [19,23,24], where M tot is the mean
wave packet overlap of the total input state, i.e., including

063602-1

Published by the American Physical Society

## PDF page 2

PHYSICAL REVIEW LETTERS 126, 063602 (2021)
the multiphoton component. Here we show that the properties of the additional or “noise” photons play a critical role
in HOM interference, and that it is crucial to know the
origin of the imperfections to be able to correctly extract the
intrinsic single-photon indistinguishability Ms.
We model an imperfect “single-photon” state
[gð2Þ ð0Þ > 0] by mixing a true single photon [gð2Þ ð0Þ ¼ 0]
with separable noise at a beam splitter. We limit our
analysis to small gð2Þ ð0Þ values so that the noise field itself
is well approximated by an optical field with at most one
additional photon and a large vacuum contribution. This
restriction to a weak, separable noise field is relevant in
practice for many SPSs, as discussed later.
It can be shown (see Supplemental Material [25]), that
for separable noise and a small resultant gð2Þ (typically
gð2Þ < 0.3), the visibility of HOM interference at a 50∶50
beam splitter is given by

1 þ Ms ð2Þ
g ;
V HOM ¼ Ms −
1 þ M sn


ð1Þ

where Msn is the mean wave packet overlap between the
single photon and an additional noise photon satisfying
0 ≤ M sn ≤ M s . We have defined gð2Þ ≡ gð2Þ ð0Þ for simplicity. The more general case where the HOM beam splitter
has an intensity reflectivity R and transmission T is given in
the Supplemental Material [25].
It is instructive to consider the two limiting cases of
Eq. (1). If the additional photons are identical to the single
photons, i.e., M sn ¼ M s , then Eq. (1) reduces to the simple
case that V HOM ¼ Ms − gð2Þ , showing that the total and
single photon mean wave packet overlaps coincide,
Ms ¼ M tot . Alternatively, if the noise has no overlap with
the single photons and M sn ¼ 0, then the visibility is further
reduced and given by V HOM ¼ M s − ð1 þ M s Þgð2Þ. The
degree to which HOM interference is affected by a nonzero
(a)

gð2Þ is therefore dependent on the origin of the additional
photons.
We experimentally test this model by emulating imperfect
SPSs. We prepare a train of near-optimal single photons and
mix them with additional photons to controllably increase
gð2Þ and measure the impact on the HOM interference. We
experimentally emulate the two limiting cases, M sn ¼ 0 and
Msn ¼ M s , and in each case we measure the gð2Þ and HOM
interference visibility of the resultant wave packet in an
unbalanced Mach-Zehnder interferometer (see Supplemental
Material [25] for further details).
We use a state-of-the-art SPS based on a quantum dot
(QD) deterministically embedded in an electrically contacted micropillar cavity [13]. The QD acts as an artificial
atom which we coherently control via resonant excitation to
generate single photons with high single photon purity,
gð2Þ < 0.05, and high indistinguishability, Mtot > 0.9. The
single photons are separated from the excitation laser using
a cross-polarization setup, as shown in Fig. 1(a).
The experimental setups that enable a controlled increase
of the multiphoton probability are shown in Figs. 1(b) and
1(c) for the two limiting cases. First, to add fully distinguishable photons, we mix the single photons from the
quantum dot based single photon source (QDSPS) with
attenuated laser pulses at a different wavelength (see
Supplemental Material [25] for more details). We adjust
the power of the laser beam to alter the magnitude of the
two-photon component, and measure the HOM visibility as
a function of gð2Þ of this effective source as shown in
Fig. 1(d). Since the spectral overlap between the QDSPS
photons and the additional laser photons is zero (M sn ¼ 0)
our model predicts that V HOM ¼ M s − ð1 þ M s Þgð2Þ . The
line in Fig. 1(d) shows that this model fits the data very well
with Ms ¼ 0.94  0.02.
To create a wave packet where the additional photons are
identical to the predominant single photon component, we
build another effective source where we add a small fraction

(b)

(d)

(c)

FIG. 1. (a) Schematic for the experimental setup of a quantum dot single photon source (QDSPS). For more details see the
Supplemental Material [25]. (b),(c) Experimental setup used to emulate an imperfect single photon source with (b) distinguishable
(M sn ¼ 0) and (c) identical noise M sn ¼ M s . The inset in (b) shows the spectrum of the spectrally distinct noise photons and QD
photons. (d) Visibility of HOM interference, V HOM measured as a function of gð2Þ for distinguishable (green squares) and identical (black
circles) noise sources. The lines are the predictions from the theoretical model.

063602-2

## PDF page 3

PHYSICAL REVIEW LETTERS 126, 063602 (2021)
of photons from the same QDSPS generated at a later time.
This is obtained by performing an unbalanced quantum
interference between two photon pulses produced by the
QDSPS with delay τ. The first half wave plate (HWP) and
polarizing beam splitter (PBS) in Fig. 1(c) allow us to tune
the relative intensity of the predominant single photon
pulse and the additional photons. When two subsequently
emitted photons arrive simultaneously at the second beam
splitter they will undergo HOM interference and exit the
beam splitter in the same output port. Therefore, the output
of the second BS has a higher gð2Þ, since there is a small
probability that some of the output pulses now contain two
identical photons. By adjusting the splitting ratio at the first
beam splitter, the gð2Þ of the output state can be controlled.
Figure 1(d) presents the HOM visibility as we increase the
gð2Þ via addition of identical photons, where a clear
difference is observed compared to the previous limiting
case. For Msn ¼ Ms, the model predicts V HOM ¼ Ms − gð2Þ ,
a linear dependence with slope of −1. The line in Fig. 1(d)
again demonstrates that the model gives a very good fit to
the data, with an extracted M s ¼ 0.89  0.01.
We note that the extracted values of Ms for these two
cases represent the upper and lower bound of the intrinsic
single photon indistinguishability of the QDSPS used in
these measurements. If the nonzero gð2Þ of the QDSPS was
due to distinguishable noise then we could deduce that
Ms ¼ 0.94  0.02. Similarly if the noise was identical then
the QDSPS has a single photon indistinguishability of
Ms ¼ 0.89  0.01. This demonstrates that it is necessary to
know the origin of the unwanted photon emission in order
to be able to extrapolate the data back to gð2Þ ¼ 0. To the
extent of our knowledge, this has so far only been done in
the indistinguishable case, independent of the physical
phenomena of the multi-photon components. In the following, we discuss how to properly estimate the single photon
indistinguishability for QD based SPSs.
There are two distinct categories of QDSPS, depending
on the charge state of the quantum dot: neutral excitons and
charged excitons (hereafter referred to as exciton and trion
states, respectively). The optical selection rules and photon
emission processes differ significantly between the excitons and trions [26], leading to a different origin of the
multiphoton component.
For a trion based source, the optical selection rules
correspond to a four level system with four possible linearly
polarized transitions [27]. In a cross-polarized setup, this
system behaves like an effective two-level system, and the
single photon emission shows a rapid rise time and
monoexponential decay as shown in Fig. 2(a). Since the
single photon emission process is fast, it can occur during
the laser pulse so that there is a probability that the quantum
dot returns to the ground state before the end of the laser
pulse and gets excited again, leading to the emission of a
second photon [28]. Therefore, the nonzero gð2Þ for a trion
based source is predominantly due to reexcitation.

(a)

(b)

FIG. 2. (a) Time traces of the single photon wave packet
emitted by trion (upper) and exciton (lower) sources. The
excitation laser pulse is shown in gray. (b) Measured gð2Þ for
trion (purple squares) and exciton (blue circles) sources as a
function of the excitation pulse duration at π pulse. The error bars
are within the size of the plotted points.

For an exciton, the system is described by a three level
system where the excitation pulse creates a superposition of
the two excitonic linear dipoles with an energy difference
given by the fine-structure splitting [29]. This results in a
time-dependent phase between the two exciton eigenstates,
so that the single-photon emission in cross polarization
beats with a period determined by the fine structure
splitting [26,30], as shown in Fig. 2(a). These optical
selection rules imply that the single photon emission in
cross polarization is delayed with respect to the excitation
pulse, and this delay means that the probability of collecting two photons via reexcitation is very small.
To illustrate this, we measure the gð2Þ at maximum
emitted brightness for two QD sources, one exciton and
one trion, while increasing the temporal length of the
excitation pulse [Fig. 2(b)]. For the exciton source, the
single photon purity remains very high for pulse durations
up to 80 ps, whereas the single photon purity rapidly
degrades for longer pulses for the trion based source due to
an increased probability of reexcitation. We notice that for
both excitons and trions, the gð2Þ is higher for very short
pulses. This is because the power required to reach
maximum emitted brightness (π pulse) increases as the
pulse duration decreases [31]. For a fixed pulse area, the
Rabi frequency of a pulse of duration τ is proportional to
1=τ, corresponding to a pulse power proportional to 1=τ2
and a total energy per pulse (τ × P) proportional to 1=τ.
This implies that in the very short pulse regime (< 10 ps),
more excitation power is required to reach π pulse and the
gð2Þ is limited by imperfect suppression of the excitation
laser. This remains the dominant source of an imperfect gð2Þ
for exciton sources up to a pulse duration of 80 ps, whereas
trion sources are limited by reexcitation for pulses longer
than 15 ps.
To correctly extract the single photon indistinguishability for each type of QDSPS it is critical to account for these
different origins of the multiphoton component. To do so,

063602-3

## PDF page 4

PHYSICAL REVIEW LETTERS 126, 063602 (2021)
we experimentally increase the multiphoton component by
adjusting the main parameter that is responsible for multiphoton emission in each type of source, and then measure
the impact this has on the visibility of HOM interference.
By deliberately introducing noise with the same origin as
that which limits the gð2Þ for each type of source, we ensure
that we can extrapolate the relationship between gð2Þ and
V HOM to values below the lowest gð2Þ that we can measure.
Specifically, we increase the probability of reexcitation for
a trion source and the amount of laser photons for the
exciton source.
For the exciton based source, we have two different
methods to add laser photons to the single photon emission
from the QDSPS. First, we can decrease the pulse duration
which, as described above, means that we require more
power to reach π pulse, and therefore there is a higher
probability of detecting a laser photon. Second, we can
rotate the quarter-wave plate (QWP) of the excitation pulse
[see Fig. 1(a)], so that the excitation polarization is no
longer aligned along one of the polarization axes of the
cavity. The light will experience polarization rotation due to
the birefringence of the cavity, and some fraction of the
excitation pulse will now be collected in the orthogonal
polarization with the single photons. By adjusting the QWP
we can decrease the polarization extinction of the laser and
add more laser photons. We increase the gð2Þ of the effective
source according to each of these methods, and measure the
corresponding impact on HOM interference as shown in
Fig. 3(a). We fit Eq. (1) to the data (since the added noise
from the laser is separable), and we extract Ms ¼ 0.94 
0.01 (M s ¼ 0.91  0.01) and Msn ¼ −0.02  0.09 (Msn ¼
0.03  0.06) for the case where we change the pulse
duration (polarization extinction). In both cases, the
extracted value of M sn is equal to zero within error.
From Fig. 2(b), we can indeed see that there is very little
overlap between the laser photons and the single photons
emitted by the quantum dot, an observation compatible
with Msn ¼ 0. We note that the two datasets were
(a)

(b)

performed on different excitons which explains the slight
difference in M s of the two devices.
For the trion based source, since the imperfect gð2Þ arises
from reexcitation, the assumption of separable noise does
not hold because the emission of the first and second
photon are time correlated. However, the extra photon must
be emitted during the laser pulse for re-excitation to occur
[28], whereas the main single photon emission typically
takes place after the laser pulse with the trion radiative
decay time of approximately 170 ps. As a result, the noise
photon, while emitted by the QD, is temporally distinguishable from the predominant single-photon emission. This
noise can thus be considered mostly separable and distinguishable. The validity of this analysis is verified by
increasing the pulse duration to increase the probability of
reexcitation. The gð2Þ and HOM visibility are measured for
different pulse durations from 15 to 50 ps at π pulse, and the
results shown in Fig. 3(b). We fit our observations with
Eq. (1) and find M s ¼ 0.93  0.01 and M sn ¼ 0.09  0.02,
indicating that the overlap between the noise photons and
the single photons from the QDSPS is indeed very low. In
fact, if we fit the data using the distinguishable noise model
(M sn ¼ 0) we extract a single parameter Ms ¼ 0.94  0.01,
which is in good agreement with the value extracted
using Eq. (1).
For both the exciton and trion based sources we extract a
single-photon indistinguishability, M s , of around 0.93. The
residual distinguishability is due to phonon-assisted emission into the phonon sideband, as well as pure dephasing of
the zero phonon line. Both of these effects are reduced by
cavity quantum electrodynamics effects, and very high
values of indistinguishability have been measured in high
Q-factor cavities [32]. However, the current implementation is in a lower Q-factor cavity, and some phononinduced decoherence remains.
To summarize, we find that, despite their different
physical origins, the multiphoton component of both
exciton and trion based QDSPSs can be treated as separable
distinguishable noise. In the limit of low gð2Þ, the single
photon indistinguishability can thus be obtained using
Ms ¼

FIG. 3. (a) Measured HOM visibility as a function of the gð2Þ
for an exciton source. The gð2Þ is increased by either decreasing
the pulse duration of the excitation pulse (red), or decreasing the
suppression of the excitation laser (blue). The two methods are
performed on different exciton sources. (b) Measured HOM
visibility as a function of the gð2Þ for a trion source as the pulse
duration is increased. In both plots, the solid line gives the
theoretical prediction for these data. The error bars are within the
size of the plotted points.

V HOM þ gð2Þ
:
1 − gð2Þ

ð2Þ

This correction factor allows one to extract the intrinsic
single photon indistinguishability Ms, given a measurement
of gð2Þ and V HOM .
We note that, among the large number of works dedicated
to QDSPSs, the correction factor that has been used to
account for an imperfect gð2Þ differs significantly, with some
using M ¼ V HOM þ gð2Þ [32,33], others using M ¼
V HOM þ 2gð2Þ [13,16], and some using M ¼ V HOM × ð1 þ
2gð2Þ Þ [34], with none of them discussing the nature of the
noise. For the cases where the lower bound was taken,
our study shows that for these QDSPS the actual

063602-4

## PDF page 5

PHYSICAL REVIEW LETTERS 126, 063602 (2021)
indistinguishability is larger than previously claimed. The
correction factor derived here has been applied to a recent
benchmarking of multiple QDSPSs based on both charged
and neutral excitons [26]. It was found that, despite the gð2Þ
of the different sources varying between 2% and 7%, the
extracted single-photon indistinguishability was consistently
between 92% and 95% for 12 of the sources.
We finally note that our approach applies to many SPSs,
including all SPSs based on single quantum emitters,
whether the residual gð2Þ arises from imperfect laser filtering or re-excitation. It is also applicable to SPSs based on
nonlinear optical frequency conversion where the nonzero
gð2Þ is predominantly due to multiple photon-pair generation. For single-mode sources, the two-photon component
is described by a two-photon Fock state with indistinguishable photons in a single, well-defined mode. This can be
reproduced by the beam splitter model presented here via
photon bunching, and hence the separable noise model with
indistinguishable noise photons applies. The case of multi
photon-pair generation in multimode sources, however,
would require further investigations.
In conclusion, we have theoretically and experimentally
revisited the emblematic Hong-Ou-Mandel interference.
This experiment is commonly implemented to test the
indistinguishability of single particles including single
photons, single plasmons, single electrons, or single atoms
[35–37]. We believe that the new insight brought by our
study will benefit these fundamental studies as well as the
development of single photon sources. Here we have
showed how to extract the single-photon indistinguishability Ms, which gives the upper bound to the indistinguishability that could be achieved with an ideal
experimental setup and fundamentally quantifies how
temporally coherent the source itself is. While this does
not circumvent the fact that it is the overall wave packet
indistinguishability that is crucial for quantum technologies, this deepened understanding of the Hong-Ou-Mandel
experiment enables us to carefully account for the impact of
multiphoton events on the HOM visibility which is
essential to properly identify the remaining limitations in
the journey towards an ideal SPS.
This work was partially supported by the ERC PoC
PhoW, the French Agence Nationale pour la Recherche
(grant ANR QuDICE), the IAD—ANR support ASTRID
program Projet No. ANR-18-ASTR-0024 LIGHT, the
QuantERA ERA-NET Cofund in Quantum Technologies,
project HIPHOP, the French RENATECH network, a public
grant overseen by the French National Research Agency
(ANR) as part of the “Investissements dAvenir” programme
(Labex NanoSaclay, reference: ANR-10-LABX-0035). J. C.
L. and C. A. acknowledge support from Marie SklodowskaCurie Individual Fellowships SMUPHOS and SQUAPH,
respectively. H. O. acknowledges support from the Paris
Ile-de-France Rgion in the framework of DIM SIRTEQ.
S. C. W. and C. S. acknowledge support from NSERC

(the Natural Sciences and Engineering Research Council),
AITF (Alberta Innovates Technology Futures), and the SPIE
Education Scholarships program. P. S. acknowledges the
support from the iXcore Foundation for research.
H. O. and S. E. T. contributed equally to this work.

*

sarah.thomas@c2n.upsaclay.fr
pascale.senellart-mardon@c2n.upsaclay.fr
[1] E. Knill, R. Laflamme, and G. J. Milburn, Nature (London)
409, 46 (2001).
[2] J. L. O’Brien, Science 318, 1567 (2007).
[3] L.-M. Duan, M. D. Lukin, J. I. Cirac, and P. Zoller,
Nature (London) 414, 413 (2001).
[4] N. Sangouard, C. Simon, H. de Riedmatten, and N. Gisin,
Rev. Mod. Phys. 83, 33 (2011).
[5] P. G. Kwiat, E. Waks, A. G. White, I. Appelbaum, and P. H.
Eberhard, Phys. Rev. A 60, R773 (1999).
[6] H.-S. Zhong et al., Phys. Rev. Lett. 121, 250505 (2018).
[7] F. Kaneda and P. G. Kwiat, Sci. Adv. 5, eaaw8586 (2019).
[8] C. Joshi, A. Farsi, S. Clemmen, S. Ramelow, and A. L.
Gaeta, Nat. Commun. 9, 847 (2018).
[9] C. Xiong, X. Zhang, Z. Liu, M. J. Collins, A. Mahendra,
L. G. Helt, M. J. Steel, D.-Y. Choi, C. J. Chae, P. H. W.
Leong, and B. J. Eggleton, Nat. Commun. 7, 10853 (2016).
[10] R. J. A. Francis-Jones, R. A. Hoggarth, and P. J. Mosley,
Optica 3, 1270 (2016).
[11] I. Aharonovich, D. Englund, and M. Toth, Nat. Photonics
10, 631 (2016).
[12] P. Senellart, G. Solomon, and A. White, Nat. Nanotechnol.
12, 1026 (2017).
[13] N. Somaschi, V. Giesz, L. De Santis, J. C. Loredo, M. P.
Almeida, G. Hornecker, S. L. Portalupi, T. Grange, C.
Antón, J. Demory, C. Gómez, I. Sagnes, N. D.
Lanzillotti-Kimura, A. Lemaítre, A. Auffeves, A. G. White,
L. Lanco, and P. Senellart, Nat. Photonics 10, 340 (2016).
[14] H. Wang, Z.-C. Duan, Y.-H. Li, S. Chen, J.-P. Li, Y.-M. He,
M.-C. Chen, Y. He, X. Ding, C.-Z. Peng, C. Schneider, M.
Kamp, S. Höfling, C.-Y. Lu, and J.-W. Pan, Phys. Rev. Lett.
116, 213601 (2016).
[15] Y.-M. He, H. Wang, C. Wang, M. C. Chen, X. Ding, J. Qin,
Z. C. Duan, S. Chen, J. P. Li, R.-Z. Liu, C. Schneider, M.
Atatüre, S. Höfling, C.-Y. Lu, and J.-W. Pan, Nat. Phys. 15,
941 (2019).
[16] H. Wang et al., Nat. Photonics 13, 770 (2019).
[17] C. K. Hong, Z. Y. Ou, and L. Mandel, Phys. Rev. Lett. 59,
2044 (1987).
[18] K. A. Fischer, R. Trivedi, and D. Lukin, Phys. Rev. A 98,
023853 (2018).
[19] R. Trivedi, K. A. Fischer, J. Vukovi, and K. Mller, Adv.
Quantum Technol. 3, 1900007 (2020).
[20] A. J. Bennett, R. B. Patel, C. A. Nicoll, D. A. Ritchie, and
A. J. Shields, Nat. Phys. 5, 715 (2009).
[21] S. V. Polyakov, A. Muller, E. B. Flagg, A. Ling, N.
Borjemscaia, E. Van Keuren, A. Migdall, and G. S.
Solomon, Phys. Rev. Lett. 107, 157402 (2011).
[22] T. Huber, M. Prilmller, M. Sehner, G. S. Solomon, A.
Predojević, and G. Weihs, Quantum Sci. Technol. 2,
034016 (2017).

063602-5

†

## PDF page 6

PHYSICAL REVIEW LETTERS 126, 063602 (2021)
[23] A. Kiraz, M. Atatüre, and A. Imamoğlu, Phys. Rev. A 69,
032305 (2004).
[24] A. B. U’Ren, C. Silberhorn, J. L. Ball, K. Banaszek, and I.
A. Walmsley, Phys. Rev. A 72, 021802(R) (2005).
[25] See Supplemental Material at http://link.aps.org/
supplemental/10.1103/PhysRevLett.126.063602 for a theoretical derivation of the relationship between Hong-OuMandel interference visibility and single-photon purity in a
separable noise model, as well as further experimental details.
[26] H. Ollivier, I. Maillette de Buy Wenniger, S. Thomas, S. C.
Wein, A. Harouri, G. Coppola, P. Hilaire, C. Millet, A.
Lemaitre, I. Sagnes, O. Krebs, L. Lanco, J. C. Loredo, C.
Anton, N. Somaschi, and P. Senellart, ACS Photonics 7,
1050 (2020).
[27] X. Xu, Y. Wu, B. Sun, Q. Huang, J. Cheng, D. G. Steel,
A. S. Bracker, D. Gammon, C. Emary, and L. J. Sham,
Phys. Rev. Lett. 99, 097401 (2007).
[28] K. A. Fischer, L. Hanschke, M. Kremser, J. J. Finley, K. Mller,
and J. Vučković, Quantum Sci. Technol. 3, 014006 (2017).
[29] M. Bayer, G. Ortner, O. Stern, A. Kuther, A. A. Gorbunov,
A. Forchel, P. Hawrylak, S. Fafard, K. Hinzer, T. L.
Reinecke, S. N. Walck, J. P. Reithmaier, F. Klopf, and
F. Schäfer, Phys. Rev. B 65, 195315 (2002).
[30] A. S. Lenihan, M. V. Gurudev Dutt, D. G. Steel, S.
Ghosh, and P. K. Bhattacharya, Phys. Rev. Lett. 88,
223601 (2002).

[31] V. Giesz, N. Somaschi, G. Hornecker, T. Grange, B. Reznychenko, L. De Santis, J. Demory, C. Gomez, I. Sagnes, A.
Lemaitre, O. Krebs, N. D. Lanzillotti-Kimura, L. Lanco, A.
Auffeves, and P. Senellart, Nat. Commun. 7, 11986
(2016).
[32] T. Grange, N. Somaschi, C. Antón, L. De Santis, G.
Coppola, V. Giesz, A. Lemaître, I. Sagnes, A. Auffèves,
and P. Senellart, Phys. Rev. Lett. 118, 253602 (2017).
[33] G. Kirsanske, H. Thyrrestrup, R. S. Daveau, C. L. Dreeßen, T.
Pregnolato, L. Midolo, P. Tighineanu, A. Javadi, S. Stobbe, R.
Schott, A. Ludwig, A. D. Wieck, S. I. Park, J. D. Song, A. V.
Kuhlmann, I. Söllner, M. C. Löbl, R. J. Warburton, and P.
Lodahl, Phys. Rev. B 96, 165306 (2017).
[34] N. Tomm, J. Javadi, N. O. Antoniadis, D. Najer, M. C. Lobl,
A. R. Korsch, R. Schott, S. R. Valentin, A. D. Wieck, A.
Ludwig, and R. J. Warburton, arXiv:2007.12654.
[35] G. Di Martino, Y. Sonnefraud, M. S. Tame, S. Kéna-Cohen,
F. Dieleman, S. K. Özdemir, M. S. Kim, and S. A. Maier,
Phys. Rev. Applied 1, 034004 (2014).
[36] E. Bocquillon, V. Freulon, J.-M. Berroir, P. Degiovanni, B.
Plaçais, A. Cavanna, Y. Jin, and G. Fève, Science 339, 1054
(2013).
[37] R. Lopes, A. Imanaliev, A. Aspect, M. Cheneau, D. Boiron,
and C. I. Westbrook, Nature (London) 520, 66 (2015).

063602-6
