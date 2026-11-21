Source: https://doi.org/10.1038/s41534-022-00643-y
PDF sha256: 52cf6c0c5b20d4fc00f86759203bc24ee2da4531756235cbfa2b254098a58097
License: https://creativecommons.org/licenses/by/4.0/

# Transcription of carroll_2022_dynamics_of_superconducting_qubit_relaxation_times.pdf

Transcription of `carroll_2022_dynamics_of_superconducting_qubit_relaxation_times.pdf` in this directory, 7 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-7 from the PDF's own text layer (pdftotext version 26.10.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

www.nature.com/npjqi

ARTICLE

OPEN

Dynamics of superconducting qubit relaxation times
M. Carroll

1,2 ✉

, S. Rosenblatt

1,2 ✉

, P. Jurcevic

1

, I. Lauer1 and A. Kandala1,2 ✉

Superconducting qubits are a leading candidate for quantum computing but display temporal ﬂuctuations in their energy
relaxation times T1. This introduces instabilities in multi-qubit device performance. Furthermore, autocorrelation in these time
ﬂuctuations introduces challenges for obtaining representative measures of T1 for process optimization and device screening. These
T1 ﬂuctuations are often attributed to time varying coupling of the qubit to defects, putative two level systems (TLSs). In this work,
we develop a technique to probe the spectral and temporal dynamics of T1 in single junction transmons by repeated T1
measurements in the frequency vicinity of the bare qubit transition, via the AC-Stark effect. Across 10 qubits, we observe strong
correlations between the mean T1 averaged over approximately nine months and a snapshot of an equally weighted T1 average
over the Stark shifted frequency range. These observations are suggestive of an ergodic-like spectral diffusion of TLSs dominating
T1, and offer a promising path to more rapid T1 characterization for device screening and process optimization.

1234567890():,;

npj Quantum Information (2022)8:132 ; https://doi.org/10.1038/s41534-022-00643-y

INTRODUCTION
Superconducting qubits are a leading platform for quantum
computing1,2. This has been driven, in part, by improvements in
coherence times over ﬁve orders of magnitude since the
realization of coherent dynamics in a Cooper-pair box3. However,
further improving coherence times remains crucial for enhancing
the scope of noisy superconducting quantum processors as well
as the long-term challenge of building a fault tolerant quantum
computer. Recent advances4–7 in two-qubit gate control have
placed their ﬁdelities at the cusp of their coherence limit, implying
that improvements in coherence could directly drive gate ﬁdelities
past the fault tolerant threshold. In this context, coherence
stability and its impact on multi-qubit device performance is also
an important theme, since superconducting qubits have been
shown to display large and correlated temporal ﬂuctuations (i.e.,
1/fα) in their energy relaxation times T18–14. This places additional
challenges for benchmarking the coherence properties of these
devices13, and also for error mitigation strategies such as zero
noise extrapolation12.
The ﬂuctuations of qubit T1 are often attributed to resonant
couplings with two-level systems (TLSs) that have been historically
studied in the context of amorphous solids15,16 and their low
temperature properties. More recently, TLSs have attracted
renewed interest due to their effect on the coherence properties
of superconducting quantum circuits11,13,14,17–20, and are attributed to defects in amorphous materials at surfaces, interfaces, and
the Josephson junction tunnel barrier. Frequency resolved
measurements of T1 in ﬂux and stress tunable devices11,19–21
have also displayed ﬂuctuations, suggesting an environment of
TLSs with varying coupling strengths around the qubit frequency.
The variability of T1 over time is explained11,16, at least in part, by
temporal ﬂuctuations in this frequency environment, associated
with the spectral diffusion of the TLSs15,22.
Furthermore, two-qubit gates that involve frequency excursions5,11,23 can also interact with TLSs near the qubit frequency
leading to additional incoherent error. The ﬂuctuations in TLS
peak positions, therefore, can also introduce ﬂuctuations in
two-qubit ﬁdelity. Spectroscopy of defect TLS is, therefore,

central to understanding the short and long time T1 and gate
ﬁdelity of qubits.
Single Josephson junction transmons with ﬁxed frequency
couplings represent a successful device architecture achieving
networks of over 60 qubits1 with all microwave control and state
of the art device coherence. The single junction conﬁguration
offers advantages such as reduced sensitivity to ﬂux noise, while
preserving the transmon charge insensitivity and also reducing
system complexity with fewer control inputs. However, there is
little TLS spectroscopy of single junction transmons because of
the limited tunability, despite the central importance of understanding the TLS environment both for device and process
characterization.
In this work, we introduce an all-microwave technique for the
fast spectroscopy of TLSs in single junction transmon qubits that
requires no additional hardware resources. In contrast to ﬂuxbased approaches to TLS spectroscopy, we employ off-resonant
microwave tones to drive AC-Stark shifts of the fundamental qubit
transition and spectrally resolve qubit relaxation times. Dips in
relaxation times serve as a probe of the frequency location of a
strongly coupled TLS. We use repeated frequency sweeps to
probe the time dynamics of the relaxation probabilities including
tracking the spectral diffusion of strongly coupled TLS. Across 10
qubits, we observe strong correlations between the long time
mean, averaged over several months hT 1 iT , and the short time
mean, averaged around the local qubit frequency hT 1 iω;t .
This strong correlation suggests a quasi-ergodic behavior of the
TLS spectral diffusion in the nearby frequency neighborhood of
the qubit. In contrast, there is lower correlation between hT 1 iT and
T1 measured over a single day. The hT 1 iω;t can provide, therefore,
a more rapid estimate of long-time behavior.

RESULTS
Device and spectroscopy technique
The experiments reported in this letter were performed
on ibmq_almaden, a 20 qubit processor based off single
junction transmons and ﬁxed couplings. The device topology is

1
IBM Quantum, IBM T.J. Watson Research Center, Yorktown Heights, NY 10598, USA. 2These authors contributed equally: M. Carroll, S. Rosenblatt, A. Kandala.
✉email: malcolm.carroll@ibm.com; srosenb@us.ibm.com; akandala@us.ibm.com

Published in partnership with The University of New South Wales

## PDF page 2

M. Carroll et al.

2

1234567890():,;

Fig. 1 Device map and T1s. a Map of a 20 qubit device including the qubit number, two-qubit connectivity, and the qubit frequency in (GHz).
b Box and whisker plot of T1’s measured daily.

shown in Fig. 1a, and qubit frequencies are around ~5 GHz.
Figure 1b depicts the characteristic spread of the qubit T1s and
their mean, from ~250 measurements over 9 months. The base
plate (to which the device was mounted) temperature of the
dilution refrigerator was typically ~13 mK excepting several
temperature excursions to ~1 K, which were not observed to
have any signiﬁcant effects on the long time T1 time series or
distributions of T1 values discussed in this work, discussed later.
Several qubits on the device display mean T1s exceeding 100 μs.
However, the large spread in individual qubit T1s highlights the
challenge for rapid benchmarking of device coherence, since
any single T1 measurement can disagree substantially from its
long-time mean.
We study the spectral dynamics of these T1 times by employing
off-resonant microwave tones24 to induce an effective frequency
shift Δωq in single junction transmons by the AC Stark effect. This
has been employed previously for coherent state transfer
between coupled qubits that are Stark shifted into resonance25.
In this work, shifting the qubit frequency into resonance with a
defect TLS induces a faster relaxation time, which in turn is used
to detect the frequency location of the TLS26, as depicted in
Fig. 2a. The Stark shift can be described analytically by a Dufﬁng
oscillator model27,28
Δωq ¼

δq Ω2s
2Δqs ðδq þ Δqs Þ

(1)

where δq is the qubit anharmonicity, Ωs is the drive amplitude and
Δqs = ωq − ωs is the detuning between the qubit frequency and
the Stark tone.
As seen from the expression above, the magnitude and sign of
the Stark shift can be manipulated by the detuning and the drive
amplitude of the Stark tone, Fig. 2c. Very large frequency shifts can
be obtained by driving close to the transmon transitions, but this
typically leads to undesired excitations/leakage out the two-state
manifold. In this work, we obtain Stark shifts of 10’s of MHz,
with modest drive amplitudes and a ﬁxed detuning Δqs of
±50 MHz. The frequency shifts are experimentally measured using
a modiﬁed Ramsey sequence29, schematically shown in Fig. 2b,
and display good agreement with the quadratic dependence of
the perturbative model in the low-drive limit. A representative
case is shown in Fig. 2d.
We focus on the spectrally resolved T1 measurements in Fig. 3
that we use as a probe of defect TLS transition frequencies.
However, instead of measuring the entire T1 decay, we use the
excited state probability, P1, after a ﬁxed delay time as a measure
of T1. This speeds up the spectral scans signiﬁcantly. Our
experiments are performed at a repetition rate of 1 kHz, but our
scheme can be further accelerated with reset techniques30, which
npj Quantum Information (2022) 132

can be crucial for probing faster TLS dynamics. For an effective
frequency sweep, we run an amplitude sweep with off-resonant
pulses at ﬁxed detuning (±50 MHz) and duration (delay time of
50 μs), after exciting the qubit with an initial π pulse. The pulsed
Stark sequence enables faster spectroscopy by circumventing the
need to re-calibrate the π, π/2 pulses at every frequency. The offresonant pulses have Gaussian-square envelopes with a 2σ rise-fall
proﬁle, where σ = 10 ns. This pulse sequence is shown in Fig. 2b.
The amplitude points in the sweep are then related to Stark shifts
by Ramsey sequences. Figure 3 shows representative data of such
a sweep on qubit 19 (Q19) with distinctive dips in P1 that we
attribute to strongly coupled TLS at their transition frequencies. T1
measurements at Stark tone amplitudes corresponding to high/
low P1 points, as seen in the bottom panel of Fig. 3, explicitly show
the substantial variation in T1 as a function of frequency and the
consistent tracking of T1 with P1.
Variations in P1 can potentially be caused by sources other than
TLS. In our experiments, P1 is spectrally resolved to ~± 25 MHz
around the individual qubit frequencies. The narrow frequency
range combined with measuring non-neighbor sets of qubits
simultaneously avoids strong P1 suppression from resonances with
neighboring qubits, the coupling bus or common low-Q parasitic
microwave modes. Control experiments show that time insensitive
features in the P1 ﬁngerprint are robust to choice of the Stark
tone detuning, ruling out a power dependence for the power
range used in this work. Finally, while a recent report31 modeled
their broadband T1 scatter as arising from quasi-particle ﬂuctuations, this is not sufﬁcient to explain the sharp frequencydependent P1 features depicted, for instance in Fig. 3. Furthermore, recent experiments on our qubits suggest a quasi-particle
limit to T1 that exceeds several milliseconds32.
TLS dynamics and correlations of P1(ω, t) and 〈T1〉T
We repeat the line traces of Fig. 3 for both positive and negative
50 MHz detuning, approximately once every 3–4 h, extended
over hundreds of hours for all the qubits. A representative
example of the cumulative scans is shown in Fig. 4 for Q15.
Spectroscopy of the other qubits is shown in the supplemental
information S1. The TLS dynamics around the qubit frequency are
qualitatively similar to previous TLS spectroscopy using ﬂux or
stress tunable devices16.
In the case of Q15, Fig. 4, there are prominent dips in relaxation
probability around positive 1 MHz, negative 5–10 MHz, and
negative 15–20 MHz. The spectral diffusion of the positions of
the T1 dips can vary between order of 1 to 10 MHz over the 272 h
of measurement providing a qualitative measure of linewidths. A
more quantitative discussion of linewidths can be found in
supplemental information S2. The background is covered by an
Published in partnership with The University of New South Wales

## PDF page 3

M. Carroll et al.

3

Fig. 2 Stark tone implementation. a Schematic of qubit T1 response to shift in qubit frequency (red traces), at different times, t. The qubit
frequency is tuned by an amount Δωq by an off-resonant tone placed ∣Δqs∣ above the qubit frequency ωq. The dependence of the frequency
shift on the off-resonant tone amplitude Ωs is depicted by the blue trace. The T1 dips are indicative of the qubit coming into resonance with a
strongly coupled TLS, at the frequency ωTLS. The TLS frequency shifts in time due to spectral diffusion, schematically indicated by changes in
the T1 dips at different time snapshots. b Schematic of a Ramsey pulse sequence used to calibrate Δωq as a function of Ωs (top); and (bottom)
schematic pulse sequence for the relaxation time spectroscopy. For each Ωs (i.e., Δωq), the j1i occupation is measured at a ﬁxed time (i.e.,
τ = 50 μs in this work). c An illustrative case of the 01 transition dependence on ωs for constant Ωs. The 01 qubit frequency, ωq + Δωq, uses an
unperturbed frequency of ωq = 5.0 GHz and an anharmonicity of δq = −340 MHz. The locations of the unperturbed 01 and 12 transitions are
shown as vertical lines overlaid with 5 MHz offsets to make their locations more visible on the ﬁgure. Negative and positive qubit shifts can be
produced and large shifts can be induced depending on Δqs. d Measured Δωq as a function of normalized DAC amplitude, Ωs using the AC
Stark shifted Ramsey technique. Solid line is a quadratic ﬁt functionally consistent with a perturbative model.

Fig. 3 Representative example of relaxation time dependence on
frequency. a Measured probability of being in the j1i state, P1, at 50 μs
wait time with varying Δωq and tone detuned 50 MHz above ωq/2π for
Q19. b Example of Ramsey measurements used to extract frequency
shifts Δωq/2π from pulse amplitudes. The two curves result from
starting the Ramsey oscillations with a Xπ/2 or Yπ/2. c and d are T1
measurement with Stark shifts Δωq/2π = −18.9 and −5.3 MHz, respectively. e T1 measurement with no Stark shift (i.e., no Stark tone).

ensemble of smaller dips of relaxation, Fig. 3, that also dynamically
evolve, with features that are larger than the sampling noise in the
measurement.

Published in partnership with The University of New South Wales

Fig. 4 Time dependence of energy relaxation spectroscopy. Time
dependence of the energy relaxation spectroscopy for Q15 using
Δωs = ± 50 MHz and varying Ωs over 501 different j amplitude
points, Ωs,j, to sweep Δωq(Ωs,j) in a positive or negative direction (see
Eqn. (1)). The P1 is measured at 50 μs.

As discussed previously, T1 ﬂuctuations introduce uncertainty
in the coherence benchmarking, stability of multi-qubit circuit
performance and process optimization of superconducting qubit
devices. In this context of better estimator, we examine if the
long-time averages (T ~ 9 months) hT 1 iT and hP1 iT are correlated

npj Quantum Information (2022) 132

## PDF page 4

M. Carroll et al.

4
Table 1.

List of symbols.

Symbol

Deﬁnition

ωq

Qubit frequency

Ωs,j

jth Stark drive amplitude point
in a frequency scan (see Eqn. (1))

ωj

jth Qubit Stark shift,
Δωq(Ωs,j) (see Eqn. (1))

dωj

Frequency bin size at the
Stark shifted frequency location

Δω

Maximum qubit Stark shift
Number of T1 measurements

N

for ~9 month time series in an average

d1
P

Total number of spectroscopy

n

ðhXiT;Qi  hXiT ÞðhXiω;t;Qi  hXiω;t Þ
k¼0
R ¼ sﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ
d1
P
P
2 d1
2
ðhXiT;Qk  hXiT Þ
ðhXiω;t;Qi  hXiω;t Þ

time slices in a moving average
Ti

Time of ith time bin for the

ti

~9 month T1 time series
Time of ith time bin

k¼0

of the spectroscopy time series
T1(Ti)

T1 measured at ith time

τ

Decay time at
which P1 was evaluated

P1(ωq + ωj, τ, ti)

Probability of j1i at τ delay for
time slice ti and frequency shift ωj

hP1 iT

Probability of j1i at τ
averaged over ~ 9 month time series

hP1 iω;t

Probability of j1i at τ averaged over
frequency and spectroscopy time

hT 1 iT 0!N

Moving average of Ti
measurements from T0 to Tn

hT 1 iT

T1 averaged over entire ~9 months

hT 1 iω;t

T1 average from hP1 iω;t

Qk
R(ti)

k’th qubit
hT 1 iT correlation to hT 1 iω at ti for {Qk}
hT 1 iT correlation to T1 at a single time

R(Ti)

Ti of the ~9 month series for {Qk}
hRit0!n

hT 1 iT correlation to hT 1 iω;t0!n for {Qk}

hRiT 0!N

hT 1 iT correlation to hT 1 iT 0!N for {Qk}

with the frequency neighborhood of the qubit hT 1 iω;t and hP1 iω;t ,
respectively. The averaged relaxation probabilities and T1s are
deﬁned as
hP1 iT ¼

X
1 N
P1 ðωq ; τ; T i Þ
N i¼1

(2)

hT 1 iT ¼

X
1 N
T 1 ðωq ; T i Þ
N i¼1

(3)

hP1 iω;t ¼

Δω
X 1 X
1 n
P1 ðωq þ ωj ; τ; t i Þdωj ;
n i¼1 2Δω ωj ¼Δω

(4)

hT 1 iω;t ¼

n
Δω
1X
1 X
τ
;
n i¼1 2Δω Δω lnðP1 ðωq þ ωj ; τ; ti Þdωj Þ

(5)

where deﬁnitions of variables can be found in Table 1.
We compare hP1 iω;t to hP1 iT from the daily T1 measurements
over T max  9 months evaluated at τ = 53 μs, shown in Fig. 1.
npj Quantum Information (2022) 132

The hP1 iω;t are calculated for a T1 delay time of τ = 50 μs for 10
qubits in the device for the ﬁrst time slice and a cutoff frequency
Δω/2π = 5 MHz. A qualitatively close agreement for all 10 qubits is
observed, see Fig. 5a.
A hT 1 iω;t can also be estimated for each hP1 iω;t at τ = 50 μs by
assuming an exponential decay. The approximate equivalence of
hT 1 iω;t and hT 1 iT is seen in the scatter plot of Fig. 5a inset. A near
1:1 relationship is observed when this approach is applied more
broadly across many IBM devices, see supplemental information
S3. Furthermore, the poorer correlation between hT 1 iT and a
single instance of T1 measurements, is also shown by larger
scatter, as seen in Fig. 5a inset.
To quantify with a single value the correlation between hT 1 iT or
hP1 iT and their estimators for many qubits, we use a Pearson R
measure across the ten odd-labeled qubits,

(6)

k¼0

where d is the number of qubits in the device or analysis, 10 in
this case, and X is the observable P1 or T1. The Pearson correlation
is a normalized covariance between two variables reﬂecting a
linear correlation from 1 to −1, where R = 1 (−1) represents a
100% positive (negative) correlation and R = 0 indicates no
correlation. Strong R correlation can therefore signal the existence
of a potential linear mapping between the estimator and hT 1 iT , in
particular, possibly one that is 1:1 or a scaling factor that will
reliably estimate hT 1 iT .
For a single frequency sweep that takes ~20 min, we obtain
0.76 < R(ti) < 0.84 correlation between hT 1 iT and hT 1 iω;t for
0.5 MHz < Δω < 5 MHz. Using the P1 values without assuming an
exponential dependence leads to stronger correlations of
0.87 < R(ti) < 0.91. Both of these are substantially stronger than
the correlation found between the representative instance of T1
and hT 1 iT , which was R = 0.29. We note this instance of R can have
a large spread, as seen by simulations of Gaussian-distributed
ﬂuctuations in supplemental information S4.
A better estimate of the hT 1 iT for each qubit, Qk, in the device
can be obtained from a moving average of multiple, N, measurements. We show the evolution of hRiT 0!N using a moving average of
the T1(Ti) measurements, hT 1 iT 0!N , for each qubit, Fig. 5b. The
hRiT 0!N exceeds R ~ 0.8 (i.e., strong correlation) after ~10 measurements, corresponding to a time exceeding 100 h. Approximately 10
independent measurements is sufﬁcient for ﬂuctuations with
magnitude  0:2hT 1 iT to obtain a strong correlation, R ~ 0.8,
between an estimator (e.g., hT 1 iT 0 !N ) and hT 1 iT . The details of R
dependence on ﬂuctuation magnitude and number of measurements in the moving average are discussed more completely in
supplemental information S4.
Autocorrelation between T1(Ti) and T1(Ti−1) measurements is an
underlying challenge to fast estimation of hT 1 iT . Evidence of
autocorrelation can be seen for example in long-term drifts in the
average and short-term correlations between T1, inset of Fig. 5b. On
shorter time scales, our experimental data shows evidence of stronger
autocorrelation frustrating faster accurate estimation of hT 1 iT and
that the fastest R ~ 0.8 can be obtained on order of 1–2 days, see
supplemental information S5 and S6. We conclude that hT 1 iω;t shows
promise as a method for faster estimation of hT 1 iT than repeated
T1(ω = ωq) measurements at only the qubit frequency. Extending the
hT 1 iω;t estimator to a set of many qubits, {Qk}, in a device result in
larger R, in the same time, compared to relying only on T1(ωq)
measurements for each qubit. The R value simply being a quantitative
single value expression of the high correlation between each hT 1 iω;t
and hT 1 iT across the entire set of qubits.
Published in partnership with The University of New South Wales

## PDF page 5

M. Carroll et al.

5

Fig. 5 Correlation between different T1 estimators. a Comparison of hP1 iω;t at 50 μs and hP1 iT averaged for ~9 months and evaluated at a τ
of 53 μs decay time. hP1 iω;t , is averaged over Δω/2π = 5 MHz after a single measurement that took ~ 20 min. (inset) A scatter plot using hT 1 iT ’s
averaged over 9 months of measurement as the dependent variable and hT 1 iω;t or T1s from a single day. The line is a guide to the eye showing
a 1:1 correlation. b The Pearson R dependence on time averaging of the T1’s of the odd numbered qubits up to time, T, for three cases: (i) the
entire time series (dash), (ii) the time series between temperature excursion B and D (dash-dot), lettered locations indicated in the inset, and
(iii) the time series between C and D for which no temperature excursions were recorded (solid). The intermediate time series are shifted in
time index to compare more directly at short times with the full-time series. The differences in R are within the standard deviation calculated
for sampling T1 time series with a Gaussian-distributed range of values, see supplemental information S4. (inset) The T1 (black, left) and mixing
chamber temperature (blue, right) time series for Q13. Spacing of measurements is non-uniform. The minimum spacing is ~ 24 h apart. Each
temperature excursion is labeled with a letter. c Pearson correlation, R, dependence on time slice averaging and frequency range, Δω, of the
odd numbered qubits.

It is important to note that our calculations of hT 1 iω;t employ
an equal weighting of P1 associated with every frequency bin
and the same choice of Δω for every qubit. However, it is not a
priori clear that equal weighting is a representative choice over
the Δω range. For example, how evenly does the spectral
diffusion of each TLS contribute to the T1 of the qubit? The
strong correlation of hT 1 iω;t with hT 1 iT with equal weighting
suggests that an ergodic-like sampling of the TLSs near the qubit
frequency is a reasonable ﬁrst approximation. The ergodic
behavior of the T1 estimators is examined more completely in
supplemental information S7 and supplemental information S8.
Central to the question of assigning a T1 estimate to any qubit,
we observe that hT 1 iT behaves ergodically for all the qubits
despite short-term 1/fα correlated behavior (i.e., a constant mean
hT 1 iT can be identiﬁed). Assignment of any T1 estimate could
alternatively be made impossible in the presence of drift, which
is not observed in these qubits, see supplemental information S9
and supplemental information S7 for further details about weak
stationarity and ergodicity. Furthermore, the strong correlation
of hT 1 iT to hT 1 iω;t using only the P1(ω, τ, t) spectrum around the
qubit is consistent with a leading hypothesis that the hT 1 iT is
dominated by TLS behavior rather than other stochastic or static
contributions.
Correlation dependence on frequency and measurement time
A natural question about the estimator hT 1 iω;t is, what are the
optimal parameter choices for frequency range Δω, n autocorrelated samples and the spacing in time, Δt = ti − ti−1, to obtain
sufﬁciently weakly autocorrelated measurements and a fast,
accurate measure of hT 1 iT . Since the optimum choices are
presently not known a priori, we evaluate and plot hRit0!n versus
Δω and ti in Fig. 5c to guide future application of this approach.
Equal frequency bin weighting of P1 is used. While this order of
magnitude choice of Δω produces a reasonably good ﬁrst
approximation for correlation across the entire range, the plot
displays several unexplained features (e.g., non-monotonic
dependence on Δω) indicating the unsurprising insufﬁciency of
these two globally applied parameters (i.e., Δω and t) alone to
weight the frequency contribution of all the qubits and approach
R ~ 1. Additional sensitivity analysis in supplemental information
S8 also examines correlation between frequencies and highlights
Published in partnership with The University of New South Wales

that individual qubits have different sensitivity to the range
sampled, Δω. We see that a wide span of Δω produces high
hRit0!n , comparable or better than R(Ti) from a single T1(ωq)
measurement. We further show that not only is there a strong R
correlation (e.g., linear dependence) but that hT 1 iω;t approaches
1:1 quantitative agreement with hT 1 iT . The degree to which a T1
estimator, from sampling the nearby frequency space, is quasiergodic and would converge to 1:1 agreement is addressed in
much more detail in supplemental information S8 and supplemental information S3.
DISCUSSION
Implications for process characterization
The strong correlation between hT 1 iω;t and hT 1 iT suggests that
long-time T1 averages might be estimated relatively rapidly
using spectroscopy. This is in contrast to overcoming correlation times in T1 at a single ωq to obtain a representative hT 1 iT
for the qubit.
Identiﬁcation of better choices of Δω and n in this study were
made with pre-knowledge of what hT 1 iT was. These parameters will
have to be chosen without this pre-characterization for future
implementation of this method. Encouragingly, the R dependence
on both these parameters appears to be relatively weak suggesting
that a heuristic choice for a single Δω and n might be sufﬁcient to
obtain useful estimates (i.e., R > 0.8) of hT 1 iT for new processes
when using this simple equal weighting approach until improved
choices can be formulated (i.e., different frequency spans for each
qubit and or weighted averaging over frequency).
More speciﬁcally we observe that O(10) independent measurements is sufﬁcient to obtain an R ~ 0.8 or higher, see
supplemental information S4. We conjecture that one can obtain
10 approximately independent samples, S, in a single scan by
sampling at frequency spacings, χ, that are greater than the
autocorrelation frequency width (i.e., a frequency spacing
where correlation drops below ~ 0.2). In this work, we found
the correlation to become weak for O(1 MHz), see supplemental
information S8. Then by this heuristic, a single spectroscopy scan
would require a Δω = ðS1Þ
2 χ, where S = 10 for the target of
R ~ 0.8. We assume one of the measurements is done at the
qubit frequency, T1(ωq), so for a χ ~ 1 MHz, a scan from ± 4.5 MHz
npj Quantum Information (2022) 132

## PDF page 6

M. Carroll et al.

6
would be suggested by such a heuristic. Extra n measurements
can be obtained by waiting longer than the autocorrelation
time. The autocorrelation width, furthermore, can be evaluated
in the same scan as that used for the hT 1 iT estimate as long as a
sufﬁciently wide range is sampled. Alternatively, a second scan
can be taken if the initial Δω guess was too small.
Empirically we see diminishing gains in using ever larger Δω.
Further research is needed to guide better limits on Δω beyond
the operational observation that S  Oð10Þ produces a quasiergodic result for qubits with hT 1 iT in the range of 10–200 μs, see
supplemental information S8 for more details on quasi-ergodicity.
Since we do ﬁnd ~ 1:1 agreement using a relatively small
Δω ~ 10 MHz for the ~9 month time series and we observe that
the distribution of T1(ωq, Ti) produces a constant standard
deviation, see supplemental information p
S9,ﬃﬃ rather than growing
(e.g., proportional to a random walk / t ), we speculate that
optimal Δω is bounded rather than growing indeﬁnitely from
spectral diffusion processes. Notably, Klauder et al. calculate that
dipole-coupled ensembles that are proposed for TLS spectral
diffusion22, will produce a truncated linewidth33.
Remarks on technique, correlations, and ergodicity
In this work, we probe the temporal and spectral dynamics of
superconducting qubit relaxation times. We study these dynamics
in high coherence, single-junction transmons by developing a
technique for energy relaxation spectroscopy of defect TLSs via the
AC Stark effect. Our technique requires no additional hardware
resources and can be easily sped up further by integration with
reset schemes. Autocorrelation of T1 frustrates rapid characterization of the long-time average hT 1 iT and therefore accurate
characterization of devices. Our analysis of the dynamics identiﬁes
a strong correlation between hT 1 iT and its short time average over
the local frequency span, hT 1 iω;t . The strong correlation of hT 1 iT
with hT 1 iω;t is also consistent with a TLS dominated T1 that quasiergodically samples the qubit local frequency neighborhood in
contrast to static or uncorrelated stochastic processes. This work
opens up several new promising directions for rapid process
characterization and evaluation of device stability.
DATA AVAILABILITY
The data that support the ﬁndings of this study are available from the corresponding
author on reasonable request.

10. Weissman, M. B. 1f noise and other slow, nonexponential kinetics in condensed
matter. Rev. Mod. Phys. 60, 537–571 (1988).
11. Klimov, P. et al. Fluctuations of energy-relaxation times in superconducting
qubits. Phys. Rev. Lett. 121, 090502 (2018).
12. Kandala, A. et al. Error mitigation extends the computational reach of a noisy
quantum processor. Nature 567, 491–495 (2019).
13. Burnett, J. J. et al. Decoherence benchmarking of superconducting qubits. npj
Quantum Inf. 5, 1–8 (2019).
14. Schlör, S. et al. Correlating decoherence in transmon qubits: low frequency noise
by single ﬂuctuators. Phys. Rev. Lett. 123, 190502 (2019).
15. Phillips, W. Tunneling states in amorphous solids. J. Low. Temp. Phys. 7, 351–360
(1972).
16. Müller, C., Cole, J. H. & Lisenfeld, J. Towards understanding two-level-systems in
amorphous solids—insights from quantum circuits. Rep. Prog. Phys. 82, 124501 (2019).
17. Martinis, J. M. et al. Decoherence in Josephson qubits from dielectric loss. Phys.
Rev. Lett. 95, 210503 (2005).
18. Grabovskij, G. J., Peichl, T., Lisenfeld, J., Weiss, G. & Ustinov, A. V. Strain tuning of
individual atomic tunneling systems detected by a superconducting qubit. Science 338, 232–234 (2012).
19. Barends, R. et al. Coherent Josephson qubit suitable for scalable quantum integrated circuits. Phys. Rev. Lett. 111, 080502 (2013).
20. Lisenfeld, J. et al. Electric ﬁeld spectroscopy of material defects in transmon
qubits. npj Quantum Inf. 5, 1–6 (2019).
21. Abdurakhimov, L. V. et al. Driven-state relaxation of a coupled qubit-defect system in spin-locking measurements. Phys. Rev. B 102, 100502 (2020).
22. Black, J. L. & Halperin, B. I. Spectral diffusion, phonon echoes, and saturation
recovery in glasses at low temperatures. Phys. Rev. B 16, 2879–2895 (1977).
23. Stehlik, J. et al. Tunable coupling architecture for ﬁxed-frequency transmons.
Phys. Rev. Lett. 127, 080505 (2021).
24. Gambetta, J. et al. Qubit-photon interactions in a cavity: measurement-induced
dephasing and number splitting. Phys. Rev. A 74, 042318 (2006).
25. Majer, J. et al. Coupling superconducting qubits via a cavity bus. Nature 449,
443–447 (2007).
26. Simmonds, R. W., Lang, K. M., Hite, D. A., Pappas, D. P. & Martinis, J. M. Decoherence
in Josephson qubits from junction resonances. Phys. Rev. Lett. 93, 077003 (2004).
27. Magesan, E. & Gambetta, J. M. Effective hamiltonian models of the crossresonance gate. Phys. Rev. A 101, 052308 (2020).
28. Schneider, A. et al. Local sensing with the multilevel ac stark effect. Phys. Rev. A
97, 062334 (2018).
29. Ramsey, N. F. A molecular beam resonance method with separated oscillating
ﬁelds. Phys. Rev. 78, 695–699 (1950).
30. Egger, D. J. et al. Pulsed reset protocol for ﬁxed-frequency superconducting
qubits. Phys. Rev. Appl. 10, 044030 (2018).
31. Yan, F. et al. The ﬂux qubit revisited to enhance coherence and reproducibility.
Nat. Commun. 7, 1–9 (2016).
32. Kurter, C. et al. Quasiparticle tunneling as a probe of Josephson junction barrier
and capacitor material in superconducting qubits. npj Quantum Inf. 8, 31 (2022).
33. Klauder, J. R. & Anderson, P. W. Spectral diffusion decay in spin resonance
experiments. Phys. Rev. 125, 912–932 (1962).

Received: 21 July 2021; Accepted: 17 October 2022;
ACKNOWLEDGEMENTS

REFERENCES
1. Zhang, E. J. et al. High-performance superconducting quantum processors via
laser annealing of transmon qubits. Sci. Adv. 8, eabi6690 (2022).
2. Arute, F. et al. Quantum supremacy using a programmable superconducting
processor. Nature 574, 505–510 (2019).
3. Nakamura, Y., Pashkin, Y. A. & Tsai, J. S. Coherent control of macroscopic quantum
states in a single-cooper-pair box. Nature 398, 786–788 (1999).
4. Hong, S. S. et al. Demonstration of a parametrically activated entangling gate
protected from ﬂux noise. Phys. Rev. A 101, 012302 (2020).
5. Kandala, A. et al. Demonstration of a high-ﬁdelity CNOT for ﬁxed-frequency
transmons with engineered zz suppression. Phys. Rev. Lett. 127, 130501 (2021).
6. Hashim, A. et al. Randomized compiling for scalable quantum computing on a
noisy superconducting quantum processor. Phys. Rev. X 11, 041039 (2021).
7. Foxen, B. et al. Demonstrating a continuous set of two-qubit gates for near-term
quantum algorithms. Phys. Rev. Lett. 125, 120504 (2020).
8. Müller, C., Lisenfeld, J., Shnirman, A. & Poletto, S. Interacting two-level defects as
sources of ﬂuctuating high-frequency noise in superconducting circuits. Phys.
Rev. B 92, 035442 (2015).
9. Paladino, E., Galperin, Y. M., Falci, G. & Altshuler, B. L. 1f noise: Implications for
solid-state quantum information. Rev. Mod. Phys. 86, 361–418 (2014).

npj Quantum Information (2022) 132

We acknowledge technical support on the ibmq_almaden device from the IBM Quantum
deployment team. Additional insightful discussions, suggestions and assistance came
from Nick Bronn, Andrew Cross, Oliver Dial, Doug McClure, Easwar Magesan, Hasan
Nayfeh, James Raferty, Martin Sandberg, Srikanth Srinivasan, Neereja Sundaresan, Jerry
Tersoff, Ben Fearon, Karthik Balakrishnan, James Hannon, and Jerry Chow. M.C. also
acknowledges support from Princeton Plasma Physics Laboratory through the
Department of Energy Laboratory Directed Research and Development program and
contract number DE-AC02-09CH11466 to complete parts of the analysis and manuscript.

AUTHOR CONTRIBUTIONS
S.R. and A.K. developed the technique with contributions from M.C., I.L., and P.J. M.C.
and S.R. performed the experiments. M.C., S.R., and A.K. analyzed the data. M.C., S.R.,
and A.K. wrote the manuscript with feedback from the other authors.

COMPETING INTERESTS
The authors declare that elements of this work will be included in patents ﬁled by the
International Business Machines Corporation with the US Patent and Trademark
ofﬁce. The authors declare no other ﬁnancial or non/ﬁnancial competing interests in
relation to this published work.

Published in partnership with The University of New South Wales

## PDF page 7

M. Carroll et al.

7
ADDITIONAL INFORMATION
Supplementary information The online version contains supplementary material
available at https://doi.org/10.1038/s41534-022-00643-y.
Correspondence and requests for materials should be addressed to M. Carroll,
S. Rosenblatt or A. Kandala.
Reprints and permission information is available at http://www.nature.com/
reprints
Publisher’s note Springer Nature remains neutral with regard to jurisdictional claims
in published maps and institutional afﬁliations.

Open Access This article is licensed under a Creative Commons
Attribution 4.0 International License, which permits use, sharing,
adaptation, distribution and reproduction in any medium or format, as long as you give
appropriate credit to the original author(s) and the source, provide a link to the Creative
Commons license, and indicate if changes were made. The images or other third party
material in this article are included in the article’s Creative Commons license, unless
indicated otherwise in a credit line to the material. If material is not included in the
article’s Creative Commons license and your intended use is not permitted by statutory
regulation or exceeds the permitted use, you will need to obtain permission directly
from the copyright holder. To view a copy of this license, visit http://
creativecommons.org/licenses/by/4.0/.

© The Author(s) 2022

Published in partnership with The University of New South Wales

npj Quantum Information (2022) 132
