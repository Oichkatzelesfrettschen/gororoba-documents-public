Source: https://doi.org/10.1103/wdfj-4nbt
PDF sha256: cd6613fd0c9b1ba73c2fe81c3a171565143c9ba4774bf914d7d14e66d29c1ab4
License: https://creativecommons.org/licenses/by/4.0/

# Transcription of valles_sanclemente_2026_tunable_coupler_frequency_positioning_spectator_effects.pdf

Transcription of `valles_sanclemente_2026_tunable_coupler_frequency_positioning_spectator_effects.pdf` in this directory, 7 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-7 from the PDF's own text layer (pdftotext version 26.10.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

PHYSICAL REVIEW LETTERS 136, 200801 (2026)

Optimizing the Frequency Positioning of Tunable Couplers in a Circuit QED Processor
to Mitigate Spectator Effects on Quantum Operations

1

S. Vallés-Sanclemente ,1 T. H. F. Vroomans ,1 T. R. van Abswoude ,2 T. Stavenga,3 F. Brulleman ,3
S. L. M. van der Meer ,1 Y. Xin ,1 A. Lawrence ,2 V. Singh,1,† M. A. Rol ,2 and L. DiCarlo 1,*
QuTech and Kavli Institute of Nanoscience, Delft University of Technology, P.O. Box 5046, 2600 GA Delft, The Netherlands
2
Orange Quantum Systems, Elektronicaweg 2, 2628 XG Delft, The Netherlands
3
Quantware B.V., Elektronicaweg 10, 2628 XG Delft, The Netherlands
(Received 15 April 2025; accepted 2 April 2026; published 18 May 2026)
We experimentally optimize the frequency of flux-tunable couplers in a superconducting quantum
processor to minimize the impact of spectator transmons during quantum operations (single-qubit gates,
two-qubit gates, and readout) on other transmons. We adapt a popular transmonlike tunable-coupling
element, achieving high-fidelity, low-leakage controlled-Z gates with unipolar, fast-adiabatic pulsing only
on the coupler. We demonstrate the ability of the tunable coupler to null residual-ZZ coupling as well as
exchange couplings in the one- and two-excitation manifolds. However, the nulling of these coherent
interactions is not simultaneous, prompting the exploration of trade-offs. We present experiments
pinpointing spectator effects on specific quantum operations. We also study the combined effect on
the three types of operations using repeated quantum parity measurements.
DOI: 10.1103/wdfj-4nbt

Residual quantum interactions between qubits are a key
source of crosstalk in multiqubit processors. In particular,
spectator (i.e., inactive) qubits during single-qubit gates,
two-qubit gates, and readout of other qubits can introduce
state-dependent errors. In legacy circuit quantum electrodynamics (QED) processors employing transmons coupled
via fixed-frequency resonators, a dominant residual interaction is ZZ coupling, which adds a Hamiltonian term
δH ¼ ℏξij
ZZ j1i 1j ih1i 1j j;
making the qubit transition frequency of transmon Qi
dependent on the state of Qj and vice versa. Here, ℏ is
the reduced Planck constant, and numbers indicate the
energy excitation level. It is not uncommon for the coupling
strength jξZZ j=ð2πÞ to reach MHz level for some pairs [1]
due to limited frequency targeting accuracy. Postfabrication
frequency trimming methods have allowed for taming
jξZZ j=ð2πÞ to the ∼100 kHz range in many cases [2,3].
*

Contact author: l.dicarlo@tudelft.nl
Present address: A*STAR Quantum Innovation Centre,
Institute of Materials Research and Engineering, Agency for
Science, Technology and Research, 2 Fusionopolis Way, 08-03,
Singapore, Republic of Singapore.
†

Published by the American Physical Society under the terms of
the Creative Commons Attribution 4.0 International license.
Further distribution of this work must maintain attribution to
the author(s) and the published article’s title, journal citation,
and DOI.

0031-9007=26=136(20)=200801(7)

Exchange interactions in the one- and two-excitation
manifolds are strong, adding Hamiltonian terms
ℏJij
1 j0i 1j ih1i 0j j þ H:c:;
ℏJij
2 j1i 1j ih0i 2j j þ H:c:;
with coupling strengths J1;2 =ð2πÞ typically at the 10 MHz
level. Only large detuning jΔj ≫ J between the coupled
levels limits their impact.
In recent years, significant effort has focused on the
development of flux-tunable couplers to mitigate these
quantum interactions, a crucial step in the pursuit of faulttolerant quantum computing [4–20]. A popular approach
uses flux-tunable transmonlike elements [21–36], with
variants including floating [37–42] and grounded [43–52],
also used in chiplet-linking configurations [53,54]. The
largest quantum processors demonstrated to date also
employ this tunable coupler [33,55]. A characteristic of
this approach is that ξZZ , J1 , and J 2 can all be nulled,
provided that the coupled transmons lie in the straddling
regime where the qubit ðj0i − j1iÞ transition of one transmon is flanked by the qubit and leakage ðj1i − j2iÞ
transitions of the other. Crucially though, ξZZ , J1 , and
J2 cannot be simultaneously nulled at a single couplerfrequency setting [47]. This constraint stems from the
structure of the dressed energy levels in the one- and
two-excitation manifolds. (See Supplemental Material [56]
for a detailed discussion of how these quantities depend
on the tunable-coupler frequency.) This fact motivates the
question, What tunable coupler positioning is best to

200801-1

Published by the American Physical Society

## PDF page 2

PHYSICAL REVIEW LETTERS 136, 200801 (2026)
mitigate the impact of spectator transmons on the fidelity of
quantum operations (readout and single- and two-qubit
gates) performed on other transmons?.
In this Letter, we experimentally address this question
using a 5-transmon prototype of our tunable-coupler-based
processor architecture. [This 5-transmon processor is publicly available as the Tuna-5 backend on the Quantum
Inspire platform [67] together with a 9-transmon processor
(Tuna-9) using the same architecture.] After mapping out
the dependence of ξZZ , J1 , and J2 on coupler frequency, we
first find that spectator effects on single-qubit gates are
strongly mitigated over a wide range of coupler positioning, spanning both ξZZ ¼ 0 and J1 ¼ 0, but not J2 ¼ 0.
However, for readout, nulling J 1 or J2 is advantageous: it
avoids the excitation exchange activated by measurementinduced spectral overlap between transitions of coupled
transmons. To also consider the impact of spectators on
two-qubit gates, we first consider several options for
realizing controlled-Z (CZ) gates, converging on unipolar,
fast-adiabatic flux pulsing only on the tunable coupler,
achieving CZ error ϵCZ < 1% with leakage L1 ≈ 0.05%.
Our final experiment studies the combined effect of
spectators on readout and single- and two-qubit gates in
a minimal setting relevant for quantum error correction
(QEC): repeated weight-2 parity checks with a baseline
error-detection probability of ∼12%. When repeatedly
toggling a spectator, we observe that the detection probability is lowest with the coupler biased around ξZZ ¼ 0,
minimizing spectator effects on CZ.
Our device consists of five flux-tunable transmon qubits
in a starfish configuration, with central transmon Q0
connected to four corner transmons (Q1 -Q4 ) via dedicated,
also flux-tunable couplers C0i . (Please see Supplemental
Material [56] for device parameters and performance
characteristics.) This qubit count and connectivity is a
common choice for prototyping quantum-hardware architectures intended for QEC [68–70]. Numerical simulations
show that the targeted coupling strengths, gqq =ð2πÞ ¼
6 MHz and gqc =ð2πÞ ¼ 70 MHz [56], can null ξZZ with
the transmons in the so-called straddling regime and the
coupler positioned ∼700 MHz above the qubit transition
frequencies. Spectroscopy of the coupler at ξZZ ¼ 0 confirms this prediction [56]. In this device, we find all coupled
transmon pairs in the straddling regime with all biased
at their simultaneous sweet spot, making this the clear
choice of bias point for transmons as it maximizes qubit
coherence.
We start our Letter by mapping the dependence of ξZZ ,
J1 , and J2 on coupler bias frequency. Figure 1(a) shows
example results for pair ðQ1 ; Q0 Þ (see Supplemental
Material [56] for similar results for the other pairs). We
measure ξZZ using a modified echo sequence [71] and J1
(J 2 ) by spectroscopy of the j01 10 i − j11 00 i ðj11 10 i −
j01 20 iÞ avoided crossing reached by flux biasing Q0 (Q1 )
away from sweet spot. Decoherence limits the ability of

FIG. 1. Single-qubit gate performance as a function of tunable
coupler frequency. (a) J 1 , J 2 , and ξZZ between Q1 and Q0 as a
function of coupler C01 frequency. Vertical gray, golden, and
brown lines indicate the C01 frequencies at which J 1 , J 2 , and ξZZ
are nulled, respectively. (b) Single-qubit gate errors on Q0 and
Q1 , measured using simultaneous and individual randomized
benchmarking, as a function of C01 frequency. Error bars are the
standard deviation of the mean computed from 10 repetitions.
Inset: schematic of the subsystem formed by Q1, Q0 , and C01 . Q1
and Q0 are biased at their sweet spot frequencies of 5.218 and
5.295 GHz, respectively.

both methods to accurately extract these quantities at their
zero crossings. When necessary, we rely on polynomial fits
to exact the C01 frequencies at which they are nulled. The
results clearly illustrate that the three interaction strengths
can be nulled, but not simultaneously.
We first focus on single-qubit gates, studying the impact
of C01 bias frequency on the individual and simultaneous
single-qubit gate performance of Q1 and Q0 [Fig. 1(b)].
Individual single-qubit randomized benchmarking (RB)
with the other transmon kept in j0i provides a baseline
single-qubit native gate error ≲0.1% across most of the
650 MHz range covered in C01 . We attribute the increase
observed at the lower end of C01 frequency to increased
transmon dephasing due to hybridization with the coupler
and increased sensitivity of the bare coupler to 1=f flux
noise [56]. Simultaneous performance matches individual
performance over a wide C01 range, including ξ01
ZZ ¼ 0 and
J01
¼
0.
A
degradation
is
observed
in
simultaneous
per1
formance by J2 ¼ 0. Note that the C01 sweet spot limits our
ability to extensively cover the ξ01
ZZ > 0 regime. This is
intentional: we strategically targeted couplers to have sweet

200801-2

## PDF page 3

PHYSICAL REVIEW LETTERS 136, 200801 (2026)
spots just above ξ01
ZZ ¼ 0 to avoid unnecessarily compromising on their coherence.
During the above study, we observed that ξ01
ZZ ¼ 0 is not
the optimal choice for readout. Specifically, at this C01 bias,
we found it impossible to achieve an average assignment
error [72] ϵRO < 2.5% for Q0, whose qubit transition
frequency is above that of Q1 . The underlying physical
reason is population exchange j10 01 i → j00 11 i activated
during readout: photons injected to the Q0 readout mode
cause a Stark shift of Q0 , displacing its qubit transition
downward in frequency and broadening its linewidth [73],
causing spectral overlap with Q1 . Similar physics has been
used to explain enhanced qubit relaxation during readout,
caused by Stark-shift activated exchange with lowerfrequency two-level defects [74]. Figure 2 evidences the
phenomenon, showing the excitation exchange from Q0 to

FIG. 2. Measurement-induced population exchange. (a) Schematic depicting a measurement pulse applied to Q1 after preparing it in the excited state. This pulse is followed by a
measurement of Q0 to quantify the population exchange between
the qubits. (b) Population of Q1 as a function of C01 frequency
and amplitude of the Q0 readout pulse. The amplitude is
expressed as a fraction of the maximum output of the Qblox
QRM-RF module used for readout. The pink trace shows the data
acquired with the chosen amplitude [56]. (c) Single-shot readout
characterization for Q0 at J 1 ¼ 0, yielding ϵRO ¼ 0.8%. (d) Similar characterization at ξZZ ¼ 0 and using identical readout
parameters, yielding ϵRO ¼ 2.5%.

Q1 as a function of both Q0 readout pulse amplitude and
C01 bias. The detuning between qubits also plays a role,
maximizing the exchange when it is comparable to the
Stark-shift induced by the readout pulse [56]. Population
exchange is strongly suppressed in a C01 frequency range
centered around J01
1 ¼ 0, where ϵRO < 1% is reached for
Q0 with a total readout duration of 800 ns (including
photon depletion). Remarkably, population exchange
j11i → j02i may also occur during readout and can be
mitigated at J2 ¼ 0 bias (see Supplemental Material [56]
for a study of this effect), although this configuration is
unattractive for single-qubit gates since it leads to
ξZZ =ð2πÞ > 1 MHz. As all coupled transmon pairs have
ξZZ =ð2πÞ < 100 kHz at J1 ¼ 0, and in consideration of
Fig. 1, it seems tempting to choose this bias as the default
for all couplers (see Supplemental Material [56] for a
summary of the operating frequencies at this coupler bias).
However, it remains important to also study spectator
effects on two-qubit gates.
To this end, we must now choose an implementation
of CZ gates drawing inspiration from prior work on
similar tunable-coupling architectures [28,38,40,43,44,47]
(Fig. 3). A general controlled-phase gate can be implemented by dynamically detuning the coupler, controllably
increasing ξZZ until the target conditional phase is acquired
[28,43,44,52]. We study the conditional phase and missing
fraction (a proxy for leakage) [75] of pair ðQ2 ; Q0 Þ in
response to a unipolar, fast-adiabatic pulse [76] on C02 and
a square pulse to the lower-frequency Q2, both of duration
60 ns. The conditional-phase landscape displays a contour
of 180°, the required phase for CZ. We select four points
along this contour to evaluate the performance of CZ gates
using interleaved RB with modifications to quantify leakage [77,78]. The best performance is achieved when Q2
remains at the sweet spot (i.e., only the coupler is pulsed).
Numerical simulations [56] show that the missing fraction
here is mostly due to leakage to state j1Q2 1C02 0Q0 i. Here,
we extract a CZ gate error ϵCZ ¼ ð0.62  0.03Þ% with
leakage L1 ¼ ð0.051  0.014Þ%. Most likely, this choice
maximizes fidelity because keeping Q2 at sweet spot
maximizes its coherence, as shown in Figs. 3(e) and 3(f).
However, we did not perform detailed numerical simulation
to dissect the contribution of different physical error
sources to the error budget [71,75].
We can now study the combined effect of spectators on
readout and single- and two-qubit gates in a minimal setting
relevant for QEC [79]. Specifically, we perform repeated
indirect measurements of the parity operator X2 X1 using Q0
as ancilla and Q4 as spectator (Fig. 4). We extract the errordetection probability for up to 100 rounds as a function
of C04 bias frequency without and with toggling Q4
between ground and first-excited state in every round
(similar results are obtained when using Q3 as the spectator [56]). The error-detection probability is a common
metric in QEC to evaluate the performance of a parity

200801-3

## PDF page 4

PHYSICAL REVIEW LETTERS 136, 200801 (2026)

FIG. 3. Study of a CZ gate between Q2 and Q0 , implemented by
applying a fast-adiabatic flux pulse to coupler C02 and a square
pulse to the lower-frequency qubit, Q2 . (a),(b) Conditional phase
and missing fraction extracted from conditional oscillation
experiments. (c),(d) CZ error and leakage measured using
interleaved RB at four points along the contour of 180° conditional phase [colored markers in (a), (b)]. Error bars are the
standard deviation of the mean computed from 5 repetitions. The
inset in (c) is a cartoon representation of frequency excursions of
C02 , Q0 , and Q2 . (e) Schematic of a Ramsey-like experiment that
interleaves 12 CZ gates between two π=2 pulses, the last of which
has phase ϕ. (f) Ramsey oscillations for the four chosen CZ
settings, clearly showing that the impact on coherence is lowest
when Q2 remains at its sweet spot, as expected.

check [27,31,33,55,80,81]. At a given round, it is defined
as the fraction of times that the declared parity outcome
does not match that declared in the previous round. For a
weight-2 parity check (like in Fig. 4), toggling a spectator
qubit can give a lower bound to the error-detection
probability of a weight-4 parity check that would include
all qubits in a larger QEC experiment. When Q4 is not
toggled, the error-detection probability is largely insensitive to C04 positioning, remaining < 12% over all bias
positions and all rounds. This value is higher than the stateof-the-art ∼5% [33]; we leave a more in-depth error
budgeting of the parity-check performance as future work.
By contrast, when Q4 is toggled, the error-detection
probability remains low and nearly round independent
only near ξ04
ZZ ¼ 0. This suggests that spectator effects

FIG. 4. Study of spectator effects during repeated parity checks.
(a) Simplified schematic of the device with color coding to
identify data qubits (Q1 and Q2 , red), ancilla (Q0 , blue), and
spectator (Q4 , purple). (b) Quantum circuit realizing the indirect
measurement of X 2 X 1 parity using Q0 as ancilla. A Xπ pulse is
applied to Q1 and Q2 during readout of Q0 . To study spectator
effects, a Xπ pulse is applied to Q4 , toggling it between ground
and first-excited state in every round. (c) Error-detection probability measured over 100 rounds at different C04 frequencies
(represented by the color scale), keeping spectator Q4 in the
ground state. (d) Error-detection probability measured now
toggling Q4 at every round. (e) Common plot of the errordetection probability at round 100 for data in (c) and (d). Vertical
04
04
lines mark the ξ04
ZZ ¼ 0, J 1 ¼ 0 and J 2 ¼ 0 coupler bias points.

on CZ are minimized at ξZZ ¼ 0. A slight degradation is
observed by J04
1 ¼ 0 (more noticeable when toggling Q3
instead of Q4 [56]). As jξ04
ZZ j further increases, the errordetection probability rises, showing a positive slope toward
a higher steady state with increasing rounds. This slope is a
hallmark of leakage [27,82] to higher-excited transmon
states (of Q0 in this case). Note that because the Q0 qubit
frequency is below that of Q4 , no measurement-induced
exchange is expected to take place in the one-excitation
manifold [56]. However, exchange can occur in the twoexcitation manifold as j14 10 i is Stark-shifted toward
j24 ; 00 i (In [56] we show that this effect is suppressed
at the J04
2 ¼ 0 bias.) This effect could underlie the
small increase in error-detection probability at ξZZ ¼ 0
observed when toggling Q4 . An isolated study of spectator

200801-4

## PDF page 5

PHYSICAL REVIEW LETTERS 136, 200801 (2026)
effects on the CZ gates played during the parity check
shows that the conditional phase remains unaffected when
toggling a spectator at any coupler bias, while errors on the
single-qubit phase can only be avoided at the ξZZ ¼ 0
condition [56].
In summary, we have performed an experimental study
to identify the best frequency positioning of flux-tunable,
transmonlike couplers to mitigate spectator effects on
quantum operations in a circuit QED processor. We show
that this type of tunable coupler can null ZZ and exchange
couplings, but not simultaneously. For single-qubit gates,
spectator effects are minimized at a coupler bias region that
spans J1 ¼ 0 and ξZZ ¼ 0. For two-qubit gates, the conditional phase remains mostly unaffected by spectator effects
independently of coupler bias, while errors in the singlequbit phase updates can only be suppressed at ξZZ ¼ 0
[56]. This is also the preferable configuration at which
spectator errors in a minimal multiqubit experiment are
mitigated. For readout, however, spectator effects are
minimized at J 1 ¼ 0 (J2 ¼ 0 to measure state j11i [56])
when the detuning to the spectator transmon is comparable
to the Stark shift introduced by the readout pulse.
Consequently, it could prove beneficial to dynamically
switch between nulling conditions for different quantum
operations, taking advantage of the fast flux tunability
already in place and calibrated for two-qubit gates. In [56],
we present a proof of principle of this flux-assisted readout
strategy, showing a clear decrease in average assignment
error by dynamically tuning the coupler to J1 ¼ 0 during
readout. Moving forward, it will also be important to
further test our device architecture and spectator-effect
mitigation strategies on larger devices, for example the
17-transmon, 24-coupler processor required for the
distance-3 surface code [31,80,81], where all transmons
couple to either two, three, or four nearest neighbors. It is
also interesting to explore alternative tunable-coupling
strategies with the capability to simultaneously null ZZ
and exchange interactions [83].
Acknowledgments—We thank S. Dobrovolskiy and G.
Limodio of QuantWare for fabricating the device; F.
Battistel, A. Radhakrishnan, and R. Navarathna of Qblox
for assistance with electronics; H. Ali and E. Y. Huang for
insightful discussions; and V. Sinha for project management assistance. We are grateful to G. Calusine and W.
Oliver for providing the traveling-wave parametric amplifier used in the amplification chain. This research is funded
by the Netherlands Organization for Scientific Research
(NWA.1292.19.194), Quantum Delta NL (DiagnostiQ and
National Growth Fund KAT-1), the Allowance for Top
Consortia for Knowledge and Innovation (TKI) of the
Dutch Ministry of Economic Affairs, the European Union
Flagship on Quantum Technology (OpenSuperQplus100,
No. 101113946), and Intel Corporation.

S. V. S. and L. D. C. conceptualized the experimental
study. S. V. S. performed the experiment with contributions
from T. H. F. V., T. R. A., A. L., and M. A. R. S. V. S.
performed the data analysis with contributions from
T. H. F. V., S. L. M. M., and Y. X. S. V. S., T. H. F. V., and
L. D. C. designed the Hamiltonian parameters of device,
with contributions from V. S. T. S. and F. B. designed the
device layout to target these parameters. T. S. performed the
numerical simulations of the CZ gate. S. V. S. and L. D. C.
wrote the manuscript with contributions from T. S. and
F. B., with feedback from all coauthors. L. D. C. supervised
the project.
Data availability—The data that support the findings of
this article are openly available [84].

[1] J. F. Marques, B. M. Varbanov, M. S. Moreira, H. Ali, N.
Muthusubramanian, C. Zachariadis, F. Battistel, M.
Beekman, N. Haider, W. Vlothuizen, A. Bruno, B. M.
Terhal, and L. DiCarlo, Nat. Phys. 18, 80 (2022).
[2] E. J. Zhang et al., Sci. Adv. 8, eabi6690 (2022).
[3] D. P. Pappas, M. Field, C. J. Kopas, J. A. Howard, X. Wang,
E. Lachman, J. Oh, L. Zhou, A. Gold, G. M. Stehl, K.
Yadavalli, E. A. Sete, A. Bestwick, M. J. Kramer, and J. Y.
Mutus, Commun. Mater. 5, 150 (2024).
[4] T. Hime, P. A. Reichardt, B. L. T. Plourde, T. L. Roberson,
C.-E. Wu, A. V. Ustinov, and J. Clarke, Science 314, 1427
(2006).
[5] P. Bertet, C. J. P. M. Harmans, and J. E. Mooij, Phys. Rev. B
73, 064512 (2006).
[6] A. O. Niskanen, K. Harrabi, F. Yoshihara, Y. Nakamura, S.
Lloyd, and J. S. Tsai, Science 316, 723 (2007).
[7] S. H. W. van der Ploeg, A. Izmalkov, A. M. van den Brink,
U. Hübner, M. Grajcar, E. Il’ichev, H.-G. Meyer, and A. M.
Zagoskin, Phys. Rev. Lett. 98, 057004 (2007).
[8] R. Harris, A. J. Berkley, M. W. Johnson, P. Bunyk, S.
Govorkov, M. C. Thom, S. Uchaikin, A. B. Wilson, J.
Chung, E. Holtham, J. D. Biamonte, A. Y. Smirnov,
M. H. S. Amin, and A. Maassenvandenbrink, Phys. Rev.
Lett. 98, 177001 (2007).
[9] M. S. Allman, F. Altomare, J. D. Whittaker, K. Cicak, D. Li,
A. Sirois, J. Strong, J. D. Teufel, and R. W. Simmonds,
Phys. Rev. Lett. 104, 177004 (2010).
[10] R. C. Bialczak, M. Ansmann, M. Hofheinz, M. Lenander, E.
Lucero, M. Neeley, A. O’Connell, D. Sank, H. Wang, M.
Weides, J. Wenner, T. Yamamoto, A. N. Cleland, and J. M.
Martinis, Phys. Rev. Lett. 106, 060501 (2011).
[11] S. J. Srinivasan, A. J. Hoffman, J. M. Gambetta, and A. A.
Houck, Phys. Rev. Lett. 106, 083601 (2011).
[12] Y. Yin, Y. Chen, D. Sank, P. J. J. O’Malley, T. C. White, R.
Barends, J. Kelly, E. Lucero, M. Mariantoni, A. Megrant, C.
Neill, A. Vainsencher, J. Wenner, A. N. Korotkov, A. N.
Cleland, and J. M. Martinis, Phys. Rev. Lett. 110, 107001
(2013).

200801-5

## PDF page 6

PHYSICAL REVIEW LETTERS 136, 200801 (2026)
[13] B. Peropadre, D. Zueco, F. Wulschner, F. Deppe, A. Marx,
R. Gross, and J. J. García-Ripoll, Phys. Rev. B 87, 134504
(2013).
[14] I.-C. Hoi, A. F. Kockum, T. Palomaki, T. M. Stace, B. Fan,
L. Tornberg, S. R. Sathyamoorthy, G. Johansson, P. Delsing,
and C. M. Wilson, Phys. Rev. Lett. 111, 053601 (2013).
[15] M. Pierre, I.-M. Svensson, S. Raman Sathyamoorthy, G.
Johansson, and P. Delsing, Appl. Phys. Lett. 104, 232604
(2014).
[16] Y. Chen, C. Neill, P. Roushan, N. Leung, M. Fang, R.
Barends, J. Kelly et al., Phys. Rev. Lett. 113, 220502
(2014).
[17] D. C. McKay, S. Filipp, A. Mezzacapo, E. Magesan, J. M.
Chow, and J. M. Gambetta, Phys. Rev. Appl. 6, 064007
(2016).
[18] S. J. Weber, G. O. Samach, D. Hover, S. Gustavsson, D. K.
Kim, A. Melville, D. Rosenberg, A. P. Sears, F. Yan, J. L.
Yoder et al., Phys. Rev. Appl. 8, 014004 (2017).
[19] Y. Lu, S. Chakram, N. Leung, N. Earnest, R. K. Naik, Z.
Huang, P. Groszkowski, E. Kapit, J. Koch, and D. I.
Schuster, Phys. Rev. Lett. 119, 150502 (2017).
[20] M. Kounalakis, C. Dickel, A. Bruno, N. K. Langford, and
G. A. Steele, npj Quantum Inf. 4, 1 (2018).
[21] J. Koch, T. M. Yu, J. Gambetta, A. A. Houck, D. I. Schuster,
J. Majer, A. Blais, M. H. Devoret, S. M. Girvin, and R. J.
Schoelkopf, Phys. Rev. A 76, 042319 (2007).
[22] F. Yan, D. Campbell, P. Krantz, M. Kjaergaard, D. Kim, J. L.
Yoder, D. Hover, A. Sears, A. J. Kerman, T. P. Orlando, S.
Gustavsson, and W. D. Oliver, Phys. Rev. Lett. 120, 260504
(2018).
[23] S. Rosenblum, Y. Y. Gao, P. Reinhold, C. Wang, C. J.
Axline, L. Frunzio, S. M. Girvin, L. Jiang, M. Mirrahimi,
M. H. Devoret et al., Nat. Commun. 9, 652 (2018).
[24] Y. Y. Gao, B. J. Lester, K. S. Chou, L. Frunzio, M. H.
Devoret, L. Jiang, S. Girvin, and R. J. Schoelkopf, Nature
(London) 566, 509 (2019).
[25] F. Arute, K. Arya, R. Babbush, D. Bacon, J. C. Bardin, R.
Barends, R. Biswas, S. Boixo, F. G. Brandao, D. A. Buell
et al., Nature (London) 574, 505 (2019).
[26] B. Foxen, C. Neill, A. Dunsworth, P. Roushan, B. Chiaro, A.
Megrant, J. Kelly, Z. Chen, K. Satzinger, R. Barends et al.,
Phys. Rev. Lett. 125, 120504 (2020).
[27] Google Quantum AI, Nature (London) 595, 383 (2021).
[28] J. Stehlik, D. M. Zajac, D. L. Underwood, T. Phung, J. Blair,
S. Carnevale, D. Klaus, G. A. Keefe, A. Carniol, M. Kumph,
M. Steffen, and O. E. Dial, Phys. Rev. Lett. 127, 080505
(2021).
[29] H. Goto, Phys. Rev. Appl. 18, 034038 (2022).
[30] K. Kubo and H. Goto, Appl. Phys. Lett. 122, 064001
(2023).
[31] Google Quantum AI, Nature (London) 614, 676 (2023).
[32] K. Kubo, Y. Ho, and H. Goto, Phys. Rev. Appl. 22, 024057
(2024).
[33] Google Quantum AI, Nature (London) 638, 920 (2025).
[34] X. Zhang, X. Zhang, C. Chen, K. Tang, K. Yi, K. Luo, Z.
Xie, Y. Chen, and T. Yan, Phys. Rev. Appl. 24, 034003
(2025).
[35] R. Li, K. Kubo, Y. Ho, Z. Yan, S. Inoue, Y. Nakamura, and
H. Goto, Phys. Rev. Appl. 23, 064069 (2025).

[36] N. Mehta, J. D. Teoh, T. Noh, A. Agrawal, R. Chamberlain,
T.-C. Chien, J. C. Curtis, B. H. Elfeky, S. Farzaneh, B.
Gudlewski et al., arXiv:2503.10935.
[37] P. Mundada, G. Zhang, T. Hazard, and A. Houck, Phys. Rev.
Appl. 12, 054023 (2019).
[38] E. A. Sete, A. Q. Chen, R. Manenti, S. Kulshreshtha, and S.
Poletto, Phys. Rev. Appl. 15, 064063 (2021).
[39] I. N. Moskalenko, I. A. Simakov, N. N. Abramov, A. A.
Grigorev, D. O. Moskalev, A. A. Pishchimova, N. S.
Smirnov, E. V. Zikiy, I. A. Rodionov, and I. S. Besedin,
npj Quantum Inf. 8, 130 (2022).
[40] F. Marxer, A. Vepsäläinen, S. W. Jolin, J. Tuorila, A.
Landra, C. Ockeloen-Korppi, W. Liu, O. Ahonen, A.
Auer, L. Belzane et al., PRX Quantum 4, 010314 (2023).
[41] H.-T. Liu et al., Phys. Rev. Lett. 135, 050602 (2025).
[42] F. Marxer, J. Mrożek, J. Andersson, L. Abdurakhimov, J.
Adam, V. Bergholm, R. Beriwal, C. F. Chan, S. Dahl, S. R.
Das et al., arXiv:2508.16437.
[43] M. C. Collodo, J. Herrmann, N. Lacroix, C. K. Andersen, A.
Remm, S. Lazar, J.-C. Besse, T. Walter, A. Wallraff, and C.
Eichler, Phys. Rev. Lett. 125, 240502 (2020).
[44] Y. Xu, J. Chu, J. Yuan, J. Qiu, Y. Zhou, L. Zhang, X. Tan, Y.
Yu, S. Liu, J. Li, F. Yan, and D. Yu, Phys. Rev. Lett. 125,
240503 (2020).
[45] X. Li, T. Cai, H. Yan, Z. Wang, X. Pan, Y. Ma, W. Cai, J.
Han, Z. Hua, X. Han, Y. Wu, H. Zhang, H. Wang, Y. Song,
L. Duan, and L. Sun, Phys. Rev. Appl. 14, 024070 (2020).
[46] X. Y. Han, T. Q. Cai, X. G. Li, Y. K. Wu, Y. W. Ma, Y. L.
Ma, J. H. Wang, H. Y. Zhang, Y. P. Song, and L. M. Duan,
Phys. Rev. A 102, 022619 (2020).
[47] Y. Sung, L. Ding, J. Braumüller, A. Vepsäläinen, B. Kannan,
M. Kjaergaard, A. Greene, G. O. Samach, C. McNally, D.
Kim, A. Melville, B. M. Niedzielski, M. E. Schwartz, J. L.
Yoder, T. P. Orlando, S. Gustavsson, and W. D. Oliver, Phys.
Rev. X 11, 021058 (2021).
[48] E. A. Sete, N. Didier, A. Q. Chen, S. Kulshreshtha, R.
Manenti, and S. Poletto, Phys. Rev. Appl. 16, 024050
(2021).
[49] Y. Ye, S. Cao, Y. Wu, X. Chen, Q. Zhu, S. Li, F. Chen, M.
Gong, C. Zha, H.-L. Huang et al., Chin. Phys. Lett. 38,
100301 (2021).
[50] L. Ding, M. Hays, Y. Sung, B. Kannan, J. An, A. Di Paolo,
A. H. Karamlou, T. M. Hazard, K. Azar, D. K. Kim, B. M.
Niedzielski, A. Melville, M. E. Schwartz, J. L. Yoder, T. P.
Orlando, S. Gustavsson, J. A. Grover, K. Serniak, and W. D.
Oliver, Phys. Rev. X 13, 031035 (2023).
[51] C. Križan, J. Biznárová, L. Chen, E. Hogedal, A. Osman,
C. W. Warren, S. Kosen, H.-X. Li, T. Abad, A. Aggarwal
et al., New J. Phys. 27, 074507 (2025).
[52] N. J. Glaser, F. A. Roy, I. Tsitsilin, L. Koch, N. Bruckmoser,
J. Schirk, J. H. Romeiro, G. B. P. Huber, F. Wallner, M.
Singh et al., Phys. Rev. Appl. 24, 024048 (2025).
[53] P. Zhao, Y. Zhang, G. Xue, Y. Jin, and H. Yu, Appl. Phys.
Lett. 121, 032601 (2022).
[54] D. L. Campbell, A. Kamal, L. Ranzani, M. Senatore, and
M. D. LaHaye, Phys. Rev. Appl. 19, 064043 (2023).
[55] L. Caune, L. Skoric, N. S. Blunt, A. Ruban, J. McDaniel,
J. A. Valery, A. D. Patterson, A. V. Gramolin, J. Majaniemi,
K. M. Barnes et al., arXiv:2410.05202.

200801-6

## PDF page 7

PHYSICAL REVIEW LETTERS 136, 200801 (2026)
[56] See Supplemental Material at http://link.aps.org/suppleme
ntal/10.1103/wdfj-4nbt for additional information supporting statements and claims made in the main text, which
includes Refs. [57–66].
[57] J. Heinsoo, C. K. Andersen, A. Remm, S. Krinner, T.
Walter, Y. Salathé, S. Gasparinetti, J.-C. Besse, A.
Potočnik, A. Wallraff, and C. Eichler, Phys. Rev. Appl.
10, 034040 (2018).
[58] S. Vallés-Sanclemente, S. L. M. van der Meer, M. Finkel, N.
Muthusubramanian, M. Beekman, H. Ali, J. F. Marques, C.
Zachariadis, H. M. Veen, T. Stavenga, N. Haider, and L.
DiCarlo, Appl. Phys. Lett. 123, 034004 (2023).
[59] C. Macklin, K. O’brien, D. Hover, M. Schwartz, V.
Bolkhovsky, X. Zhang, W. Oliver, and I. Siddiqi, Science
350, 307 (2015).
[60] J. Braumüller, L. Ding, A. P. Vepsäläinen, Y. Sung, M.
Kjaergaard, T. Menke, R. Winik, D. Kim, B. M. Niedzielski,
A. Melville, J. L. Yoder, C. F. Hirjibehedin, T. P. Orlando, S.
Gustavsson, and W. D. Oliver, Phys. Rev. Appl. 13, 054079
(2020).
[61] C. Zhang, T.-L. Wang, L.-L. Guo, X.-Y. Yang, X.-X. Yang,
P. Duan, Z.-L. Jia, W.-C. Kong, and G.-P. Guo, Appl. Phys.
Lett. 122, 024001 (2023).
[62] M. A. Rol, L. Ciorciaro, F. K. Malinowski, B. M. Tarasinski,
R. E. Sagastizabal, C. C. Bultink, Y. Salathe, N. Haandbaek,
J. Sedivy, and L. DiCarlo, Appl. Phys. Lett. 116, 054001
(2020).
[63] C. Hellings, N. Lacroix, A. Remm, R. Boell, J. Herrmann,
S. Lazăr, S. Krinner, F. Swiadek, C. K. Andersen, C. Eichler,
and A. Wallraff, arXiv:2503.04610.
[64] C. C. Bultink, M. A. Rol, T. E. O’Brien, X. Fu, B. C. S.
Dikken, C. Dickel, R. F. L. Vermeulen, J. C. de Sterke, A.
Bruno, R. N. Schouten, and L. DiCarlo, Phys. Rev. Appl. 6,
034008 (2016).
[65] E. Magesan, J. M. Gambetta, A. D. Córcoles, and J. M.
Chow, Phys. Rev. Lett. 114, 200501 (2015).
[66] C. A. Ryan, B. R. Johnson, J. M. Gambetta, J. M. Chow,
M. P. da Silva, O. E. Dial, and T. A. Ohki, Phys. Rev. A 91,
022118 (2015).
[67] Quantum Inspire website: https://www.quantum-inspire.com/.
[68] J. F. Marques, M. Moreira, A. Chapple, O. Benhayoune
Khadraoui, B. Varbanov, A. McDonald, W. Banner, G.
Cutter, M. Hays, H. Zhang, K. Nesterov, Y. Sung, M.
Gingras, J. Knecht, B. Niedzielski, H. Stickler, M.
Schwartz, A. Blais, K. Serniak, J. Grover, and W. Oliver,
A fluxonium architecture for QEC, Part 2: Extensible and
spectator-error-free two-qubit gate scheme, in APS Global
Summit 2025 (American Physical Society, Anaheim, CA,
2025), MAR-J18/11.
[69] T. Noh, N. Mehta, J. Teoh, K. Chow, P. Lu, G. Liu, T. Keen,
J. Yuan, S. Mundhada, J. Aumentado, S. H. Moseley, and R.

Schoelkopf, Error-detected entangling gate operations between dual-rail cavity cavity qubit—Part 1, in APS Global
Summit 2025 (American Physical Society, Anaheim, CA,
2025), MAR-L17/2.
[70] N. Mehta, T. Noh, J. Teoh, K. Chow, P. Lu, G. Liu, T. Keen,
J. Yuan, S. Mundhada, J. Aumentado, S. H. Moseley, and R.
Schoelkopf, Error-detected entangling gate operations between dual-rail cavity cavity qubit—Part 2, in APS Global
Summit 2025 (American Physical Society, Anaheim, CA,
2025), MAR-L17/3.
[71] V. Negîrneac, H. Ali, N. Muthusubramanian, F. Battistel, R.
Sagastizabal, M. S. Moreira, J. F. Marques, W. J.
Vlothuizen, M. Beekman, C. Zachariadis, N. Haider, A.
Bruno, and L. DiCarlo, Phys. Rev. Lett. 126, 220502
(2021).
[72] E. H. Chen, T. J. Yoder, Y. Kim, N. Sundaresan, S.
Srinivasan, M. Li, A. D. Corcoles, A. W. Cross, and M.
Takita, Phys. Rev. Lett. 128, 110504 (2022).
[73] D. I. Schuster, A. Wallraff, A. Blais, L. Frunzio, R.-S.
Huang, J. Majer, S. M. Girvin, and R. J. Schoelkopf, Phys.
Rev. Lett. 94, 123602 (2005).
[74] T. Thorbeck, Z. Xiao, A. Kamal, and Luke C. Govia, Phys.
Rev. Lett. 132, 090602 (2024).
[75] M. A. Rol, F. Battistel, F. K. Malinowski, C. C. Bultink,
B. M. Tarasinski, R. Vollmer, N. Haider, N.
Muthusubramanian, A. Bruno, B. M. Terhal, and L.
DiCarlo, Phys. Rev. Lett. 123, 120502 (2019).
[76] J. M. Martinis and M. R. Geller, Phys. Rev. A 90, 022307
(2014).
[77] E. Magesan, J. M. Gambetta, and J. Emerson, Phys. Rev. A
85, 042311 (2012).
[78] C. J. Wood and J. M. Gambetta, Phys. Rev. A 97, 032306
(2018).
[79] A. G. Fowler, M. Mariantoni, J. M. Martinis, and A. N.
Cleland, Phys. Rev. A 86, 032324 (2012).
[80] S. Krinner, N. Lacroix, A. Remm, A. Di Paolo, E. Genois,
C. Leroux et al., Nature (London) 605, 669 (2022).
[81] I. Besedin, M. Kerschbaum, J. Knoll, I. Hesner, L. Bödeker,
L. Colmenarez, L. Hofele, N. Lacroix, C. Hellings, F.
Swiadek et al., Nat. Phys. 22, 189 (2026).
[82] M. McEwen, D. Kafri, Z. Chen, J. Atalaya, K. Satzinger, C.
Quintana, P. V. Klimov, D. Sank, C. Gidney, A. Fowler
et al., Nat. Commun. 12, 1761 (2021).
[83] L. Heunisch, C. Eichler, and M. J. Hartmann, Phys. Rev.
Appl. 20, 064037 (2023).
[84] S. Vallés-Sanclemente, T. H. F. Vroomans, T. R. van
Abswoude, T. Stavenga, F. Brulleman, S. L. M. van der
Meer, Y. Xin, A. Lawrence, V. Singh, M. A. Rol, and
L. DiCarlo, SpectatorEffectsTunableCouplers (2025),
https://github.com/DiCarloLab-Delft/SpectatorEffectsTuna
bleCouplers.

200801-7
