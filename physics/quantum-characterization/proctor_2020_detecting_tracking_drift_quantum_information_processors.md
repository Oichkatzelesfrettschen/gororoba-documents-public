Source: https://doi.org/10.1038/s41467-020-19074-4
PDF sha256: fab223c27dcef405d97ad107acd6658d84547950d2e1591f0a83da4738871934
License: https://creativecommons.org/licenses/by/4.0/

# Transcription of proctor_2020_detecting_tracking_drift_quantum_information_processors.pdf

Transcription of `proctor_2020_detecting_tracking_drift_quantum_information_processors.pdf` in this directory, 9 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-9 from the PDF's own text layer (pdftotext version 26.10.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

ARTICLE
https://doi.org/10.1038/s41467-020-19074-4

OPEN

Detecting and tracking drift in quantum information
processors

1234567890():,;

Timothy Proctor 1,2 ✉, Melissa Revelle3, Erik Nielsen1,2, Kenneth Rudinger1,2, Daniel Lobser3, Peter Maunz3,
Robin Blume-Kohout1,2 & Kevin Young1,2

If quantum information processors are to fulﬁll their potential, the diverse errors that affect
them must be understood and suppressed. But errors typically ﬂuctuate over time, and the
most widely used tools for characterizing them assume static error modes and rates. This
mismatch can cause unheralded failures, misidentiﬁed error modes, and wasted experimental
effort. Here, we demonstrate a spectral analysis technique for resolving time dependence in
quantum processors. Our method is fast, simple, and statistically sound. It can be applied to
time-series data from any quantum processor experiment. We use data from simulations and
trapped-ion qubit experiments to show how our method can resolve time dependence when
applied to popular characterization protocols, including randomized benchmarking, gate set
tomography, and Ramsey spectroscopy. In the experiments, we detect instability and localize
its source, implement drift control techniques to compensate for this instability, and then
demonstrate that the instability has been suppressed.

1 Quantum Performance Laboratory, Sandia National Laboratories, Albuquerque, NM 87185, USA. 2 Quantum Performance Laboratory, Sandia National
Laboratories, Livermore, CA 94550, USA. 3 Sandia National Laboratories, Albuquerque, NM 87185, USA. ✉email: tjproct@sandia.gov

NATURE COMMUNICATIONS | (2020)11:5396 | https://doi.org/10.1038/s41467-020-19074-4 | www.nature.com/naturecommunications

1

## PDF page 2

ARTICLE

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-020-19074-4

R

ecent years have seen rapid advances in quantum information processors (QIPs). Testbed processors containing tens of qubits are becoming commonplace1–4 and error
rates are being steadily suppressed1,5, fueling optimism that useful
quantum computations will soon be performed. Improved theories and models of the types and causes of errors in QIPs have
played a crucial role in these advances. These new insights have
been made possible by a range of powerful device characterization
protocols5–15 that allow scientists to probe and study QIP behavior. But almost all of these techniques assume that the QIP is
stable—that data taken over a second or an hour reﬂects some
constant property of the processor. These methods can malfunction badly if the actual error mechanisms are timedependent16–22.
Yet temporal instability in QIPs is ubiquitous21–32. The control
ﬁelds used to drive logic gates drift22, T1 times can change
abruptly32, low-frequency 1/fα noise is common24, and laboratory
equipment produces strongly oscillating noise (e.g., 50 Hz/60 Hz
line noise and ~1 Hz mechanical vibrations from refrigerator
pumps). These intrinsically time-dependent error mechanisms
are becoming more and more important as technological
improvements suppress stable and better-understood errors. As a
result, techniques to characterize QIPs with time-dependent
behavior are becoming increasingly necessary.
In this article, we introduce and demonstrate a general,
ﬂexible, and powerful methodology for detecting and measuring time-dependent errors in QIPs. The core of our techniques
can be applied to time-series data from any set of repeated
quantum circuits—so they can be applied to most QIP
experiments with only superﬁcial adaptations—and they are
sensitive to both periodic instabilities (e.g., 50 Hz/60 Hz line
noise) and aperiodic instabilities (e.g., 1/fα noise). This means
that they can be used for routine, consistent stability analyses
across QIP platforms and that they can be applied to data
gathered primarily for other purposes, e.g., data from running
an algorithm or error correction. Moreover, we show how to
use our methods to upgrade standard characterization protocols—including randomized benchmarking (RB)7–14 and gate
set tomography (GST)5,6—into time-resolved techniques. Our
methods, therefore, induce a suite of general-purpose drift
characterization techniques, complementing tools that focus on
speciﬁc types of drift23–26,33–43. We demonstrate our techniques using both simulations and experiments. In our experiments, we implemented high precision, time-resolved Ramsey
spectroscopy, and GST on a 171Yb+ ion qubit. We detected a
small instability in the gates, isolated its source, and modiﬁed
the experiment to compensate for the discovered instability. By
then repeating the GST experiment on the stabilized qubit, we
were able to show both improved error rates and that the drift
had been suppressed.
Results
Instability in quantum circuits. Experiments on QIPs almost
always involve choosing some quantum circuits and running
them many times. The resulting data is usually recorded as
counts5–15 for each circuit—i.e., the total number of times each
outcome was observed for each circuit. Dividing these counts by
the total number of trials yields frequencies that serve as good
estimates of the corresponding probabilities averaged over the
duration of the experiment. But if the QIP’s properties vary over
that duration, then the counts do not capture all the information
available in the data, and time-averaged probabilities do not
faithfully describe the QIP’s behavior. The counts may then be
irreconcilable with any model for the QIP that assumes that all
operations (state preparations, gates, and measurements) are
2

time-independent. This discrepancy results in failed or unreliable
tomography and benchmarking experiments16–22.
Time-resolved analysis of the data from any set of circuits can
be enabled by simply recording the observed outcomes (clicks)
for each circuit in sequence, rather than aggregating this sequence
into counts. We call the sequence of outcomes x = (x1, x2, …, xN)
obtained at N data collection times t1, t2, …, tN a “clickstream.”
There is one clickstream for each circuit. We focus on circuits
with binary 0/1 outcomes (see Supplementary Note 1 for
discussion of the general case), and on data obtained by
“rastering” through the circuits. Rastering means running each
circuit once in sequence, then repeating that process until we have
accumulated N clicks per circuit (Fig. 1b). Under these
conditions, the clickstream associated with each circuit is a string
of bits, at successive times, each of which is sampled from a
probability distribution over {0, 1} that may vary with time. If this
probability distribution does vary over time, then we say that the
circuit is temporally unstable. In this article we present methods
for detecting and quantifying temporal instability, using clickstream data from any circuits, which are summarized in the
ﬂowchart of Fig. 1a.
Our methodology is based on transforming the data to the
frequency domain and then thresholding the resultant power
spectra. From this foundation, we generate a hierarchy of outputs:
(1) yes/no instability detection; (2) a set of drift frequencies; (3)
estimates of the circuit probability trajectories; and (4) estimates
of time-resolved parameters in a device model. To motivate this
strategy, we ﬁrst highlight some unusual aspects of this data
analysis problem.
Formally, a clickstream x is a single draw from a vector of
independent Bernoulli (coin) random variables X = (X1, X2,
…, XN) with biases p = (p1, p2, …, pN). Here pi = p(ti) is the
instantaneous probability to obtain 1 at the ith repetition time
of the circuit, and p(⋅) is the continuous-time probability
trajectory. The naive strategy for quantifying instability is to
estimate p from x assuming nothing about its form. However, p
consists of N independent probabilities and there are only N
bits from which to estimate them, so this strategy is ﬂawed. The
best ﬁt is always p = x, which is a probability jumping between
0 and 1, even if the data seems typical of draws from a ﬁxed
coin. This is overﬁtting.
To avoid overﬁtting, we must assume that p is within some
relatively small subset of all possible probability traces. Common
causes of time variation in QIPs are not restricted to any
particular portion of the frequency spectrum, but they are
typically sparse in the frequency domain, i.e., their power is
concentrated into a small range of frequencies. For example, step
changes and 1/fα noise have power concentrated at low
frequencies, while 50 Hz/60 Hz line noise has an isolated peak,
perhaps accompanied by harmonics. Broad-spectrum noise does
appear in QIP systems, but because it has an approximately ﬂat
spectrum, it acts like white noise—which produces uncorrelated
stochastic errors that are accurately described by timeindependent models. So, we model variations as sparse in the
frequency domain, but otherwise arbitrary. Note that we do not
make any other assumptions about p(t). We do not assume that it
is sampled from a stationary stochastic process, or that the
underlying physical process is, e.g., strongly periodic, deterministic, or stochastic.
Detecting instability. The expected value of a clickstream is the
probability trajectory, and this also holds in the frequency
~ ¼p
~, where E½ is the expectation value
domain. That is, E½X
and v~ denotes the Fourier transform of the vector v (see the
Methods for the particular transform that we use). In the time

NATURE COMMUNICATIONS | (2020)11:5396 | https://doi.org/10.1038/s41467-020-19074-4 | www.nature.com/naturecommunications

## PDF page 3

ARTICLE

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-020-19074-4

b
Time-series data from quantum circuits
(1)
Fourier transform

Power spectra

(see c)

(2)
Threshold

Drift frequencies

(5a)
Model selection

Spectral power

c
Parameterized
predictive
model

C1
C2

0
1

CC

Probability trajectories
(4)
Fit model to probabilities

(see e)

Parameter estimates

(5b)
Fit model to data

Probability

Time-resolved
parameterized
predictive
model

1

0

Cl =

1

1

103
102
101
100

0

Gx

Wait(ltw)

Gy

0

l = 32
l = 128

0
10–5

10–4
l = 32

Frequency (Hz)

l = 128

l = 512

l = 512
l = 2048

10–2
l = 2048

l = 8192
Threshold

10–1
l = 8192

0.5
0.0

e

0
0

1
1

Time

d

Detuning (Hz)

(see d)

0
0
1

1.0
(3)
Model selection & estimation

Example circuit suite

Rastered time-series data
Circuit

(see b)

0.5

0

2

Time (h)

6

8
25

Temperature

Temperature (C)

a

0.44

0.0

0.43

Detuning estimate

–0.5

0

All data

2

20% of data

Time (h)

6

8

22

Fig. 1 Diagnosing time-dependent errors in a quantum information processor. a A ﬂowchart of our methodology for detecting and quantifying drift in a
QIP, using time-series data from quantum circuits. The core steps (1–3) detect instability, identify the dominant frequencies in any drift, and estimate the
circuit outcome probabilities over time. They can be applied to data from any set of quantum circuits, including data collected primarily for other purposes.
Additional steps (4 and/or 5) estimate time-varying parameters (e.g., error rates) whenever a time-independent parameterized model is provided for
predicting circuit outcomes. Such a model is readily available whenever the circuits are from an existing characterization technique, such as Ramsey
spectroscopy or gate set tomography. b An example of circuits on which this technique can be implemented—Ramsey circuits with a variable wait
time ltw—as well as an illustration of data obtained by “rastering” (each circuit is performed once in sequence and this sequence is repeated N times). c–e
Results from performing these Ramsey circuits on a 171Yb+ ion qubit (l = 1, 2, 4, …, 8192, tw ≈ 400 μs, N = 6000). c The power spectra observed in this
experiment for selected values of l. Frequencies with power above the threshold almost certainly appear in the true time-dependent circuit probabilities,
pl(t). d Estimates of the probability trajectories (unbroken lines are estimates from applying step 3 of the ﬂowchart; dotted lines are the probabilities
implied by the time-resolved detuning estimate shown in e). e The standard Ramsey model pl ðtÞ ¼ A þ B sinð2πltw ΩÞ, where Ω is the qubit detuning, is
promoted to a time-resolved parameterized model (step 5a) and ﬁt to the data (step 5b) using maximum likelihood estimation, resulting in a time-resolved
detuning estimate (red unbroken line). The detuning is strongly correlated with ambient laboratory temperature (black dotted line), suggesting a causal
relationship that is supported by further experiments (see the main text). The detuning can still be estimated to high precision using only 20% of the data
(gray dashed line), which demonstrates that our techniques could be used for high precision, targeted drift tracking while also running application circuits.
The shaded areas are 2σ (~95%) conﬁdence regions.

domain, each xi is a very low-precision estimate of pi. In the
frequency domain, each x~ω is the weighted sum of N bits, so the
strong, independent shot noise inherent in each bit is largely
averaged out and any non-zero p~ω is highlighted. Of course,
simply converting to the frequency domain cannot reduce the
total amount of shot noise in the data. To actually suppress noise
we need a principled method for deciding when a data mode x~ω is
small enough to be consistent with p~ω ¼ 0. One option is to use a
regularized estimator inspired by compressed sensing44. But we
take a different route, as this problem naturally ﬁts within the
ﬂexible and transparent framework of statistical hypothesis
testing45,46.
We start from the null hypothesis that all the probabilities are
constant, i.e., ~pω ¼ 0 for every ω > 0 and every circuit. Then, for
each ω and each circuit, we conclude that j~pω j > 0 only if j~xω j is
so large that it is inconsistent with the null hypothesis at a prespeciﬁed signiﬁcance level α. If we standardize x, by subtracting
its mean and dividing by its variance, then this procedure

becomes particularly transparent: if the probability trace is
constant, then the marginal distribution of each Fourier
~ ω for ω > 0 is approximately normal, and so its
component X
~ ω j2 is χ 2 distributed. So if j~
xω j2 is larger than the (1 − α)power jX
1
percentile of a χ 21 distribution, then it is inconsistent with p~ω ¼ 0.
To test at every frequency in every circuit requires many
hypothesis tests. Using standard techniques45,46, we set an αsigniﬁcance power threshold such that the probability of falsely
concluding that j~pω j > 0 at any frequency and for any circuit is at
most α (i.e., we seek strong control of the family-wise error rate;
see Supplementary Note 1).
We now demonstrate this drift detection method with data
from a Ramsey experiment on a 171Yb+ ion qubit suspended
above a linear surface-electrode trap5 and controlled using
resonant microwaves. Shown in Fig. 1b, these circuits consist of
preparing the qubit on the x^ axis of the Bloch sphere, waiting for
a time ltw (l = 1, 2, 4, …, 8192, tw ≈ 400 μs), and measuring along
the y^ axis. We performed 6000 rasters through these circuits, over

NATURE COMMUNICATIONS | (2020)11:5396 | https://doi.org/10.1038/s41467-020-19074-4 | www.nature.com/naturecommunications

3

## PDF page 4

ARTICLE

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-020-19074-4

~8 h. A representative subset of the power spectra for these data
are shown in Fig. 1c, as well as the α-signiﬁcance threshold for
α = 5%. The spectra for circuits containing long wait times
exhibit power above the detection threshold, so instability was
detected. These data are inconsistent with constant probabilities.
Ramsey circuits are predominantly sensitive to phase accumulation, caused by detuning between the qubit and the control ﬁeld
frequencies, so it is reasonable to assume that it is this detuning
that is drifting. The detected frequencies range from the lowest
Fourier basis frequency for this experiment duration, which
is ~15 μHz, up to ~250 μHz. The largest power is more than
1700 standard deviations above the expected value under the null
hypothesis, which is overwhelming evidence of temporal
instability.
Quantifying instability. Statistically signiﬁcant evidence in data
for time-varying probabilities does not directly imply anything
about the scale of the detected instability. For instance, even the
weakest periodic drift will be detected with enough data. We can
quantify instability in any circuit by the size of the variations in its
outcome probabilities. We can measure this size by estimating the
probability trajectory p for each circuit (step 3, Fig. 1a). As noted
above, the unregularized best-ﬁt estimate of p is the observed bitstring x, which is overﬁtting. To regularize this estimate, we use
model selection. Speciﬁcally, we select the time-resolved parameterized model p(t) = γ0 + ∑kγkfk(t), where fk(t) is the kth basis
function of the Fourier transform, the summation is over those
frequencies with power above the threshold in the power spectrum, and the γk are parameters constrained only so that each p(t)
is a valid probability. We can then ﬁt this model to the clickstream for the corresponding circuit, using any standard data
ﬁtting routine, e.g., maximum likelihood estimation.
Estimates of the time-resolved probabilities for the Ramsey
experiment are shown in Fig. 1d (unbroken lines). Probability
traces are sufﬁcient for heuristic reasoning about the type and size
of the errors, and this is often adequate for practical debugging
purposes. For example, these probability trajectories strongly
suggest that the qubit detuning is slowly drifting. To draw more
rigorous conclusions, we can implement time-resolved parameter
estimation.
Time-resolved benchmarking and tomography. The techniques
presented so far provide a foundation for time-resolved parameter estimation, e.g., time-resolved estimation of gate error
rates, rotation angles, or process matrices. We introduce two
complementary approaches, which we refer to as “non-intrusive”
and “intrusive”, that can add time resolution to any benchmarking or tomography protocol. The non-intrusive approach is
to replace counts data with instantaneous probability estimates in
existing benchmarking/tomography analyses (step 4, Fig. 1a). It is
non-intrusive because it does not require modiﬁcations to existing analysis codes. In contrast, the intrusive approach builds an
explicitly time-resolved model and ﬁts its parameters to the timeseries data. We now detail and demonstrate these two techniques.
All standard characterization protocols, including all forms of
tomography5,6 and RB7–14, are founded on some timeindependent parameterized model that describes the outcome
probabilities for the circuits in the experiment, or a coarsegraining of them (e.g., mean survival probabilities in RB). When
analyzing data from these experiments, the counts data from
these circuits are fed into an analysis tool that estimates the model
parameters, which we denote {γi}. To upgrade such a protocol
using the non-intrusive method, we: (i) use the spectral analysis
tools above to construct time-resolved estimates of the probabilities; (ii) for a given time, tj, input the estimated probabilities
4

directly into the analysis tool in place of frequencies; (iii) recover
an estimate of the model parameters, {γi(ti)} at that time; and (iv)
repeat for all times of interest {tj}. This non-intrusive approach is
simple, but statistically ad hoc.
The intrusive approach permits statistical rigor at the cost of
more complex analysis. It consists of (i) selecting an appropriate
time-resolved model for the protocol and (ii) ﬁtting that model to
the time-series data (steps 5a-5b, Fig. 1a). In the model selection
step, we expand each model parameter γ into a sum of Fourier
components: γ → γ0 + ∑ωγωfω(t), where the γω are real-valued
amplitudes, and the summation is over some set of non-zero
frequencies. This set of frequencies can vary from one parameter
to another and may be empty if the parameter in question
appears to be constant. To choose these expansions we need to
understand how any drift frequencies in the model parameters
would manifest in the circuit probability trajectories, and thus in
the data.
To demonstrate the intrusive approach, we return to the
Ramsey experiment. In the absence of drift the probability of “1”
in a Ramsey circuit with a wait time of ltw is
pl ¼ A þ B expðl=l0 Þ sinð2πlt w ΩÞ, where Ω is the detuning
between the qubit and the control ﬁeld, 1/l0 is the rate of
decoherence per idle, and A, B ≈ 1/2 account for any state
preparation and measurement errors. In our Ramsey experiment,
the probability trace estimates shown in Fig. 1c suggest that the
state preparation, measurement, and decoherence error rates are
approximately time-independent, as the contrast is constant over
time. So we deﬁne a time-resolved model that expands only Ω
into a time-dependent summation:
pl ðtÞ ¼ A þ B expðl=l0 Þ sinð2πlt w ΩðtÞÞ;

ð1Þ

where Ω(t) = γ0 + ∑ωγωfω(t). To select the set of frequencies in
the summation, we observe that the dependence of the circuit
probabilities on Ω is approximately linear for small l (e.g., expand
Eq. (1) around ltwΩ(t) ≈ 0). Therefore, the oscillation frequencies
in the model parameters necessarily appear in the circuit
probabilities. So in our expansion of Ω, we include all 13
frequencies detected in the circuit probabilities (i.e., the ones with
power above the threshold in Fig. 1c). The circuit probabilities
will also contain sums, differences, and harmonics of the
frequencies in the true Ω—Fig. 1d shows clearly that the phase
is wrapping around the Bloch sphere in the circuits with the
longest wait times (l ≥ 2048), so these harmonic contributions will
be signiﬁcant in our data. Therefore, this frequency selection
strategy could result in erroneously including some of these
harmonics in our model. We check for this using standard
information-theoretic criteria47 and then discard any frequencies
that should not be in the model (Supplementary Note 2). This
avoids overﬁtting the data. Once the model is selected, we have a
time-resolved parameterized model that we can directly ﬁt to the
time-series data. We do this with maximum likelihood
estimation.
Figure 1e shows the estimated qubit detuning Ω(t) over time. It
varies slowly between approximately −0.5 and +0.5 Hz. The
detuning is correlated with an ancillary measurement of the
ambient laboratory temperature (the Spearman correlation
coefﬁcient magnitude is 0.92), which ﬂuctuates by ~1.5 °C over
the course of the experiment. This suggests that temperature
ﬂuctuations are causing the drift in the qubit detuning (this
conclusion is supported by further experiments: see later and the
Methods). The detuning has been estimated to high precision, as
highlighted by the 2σ conﬁdence regions in Fig. 1e. As with all
standard conﬁdence regions, these are in-model uncertainties, i.e.,
they do not account for any inadequacies in the model selection.
However, we can conﬁrm that the estimated detuning is
reasonably consistent with the data by comparing the pl(t)

NATURE COMMUNICATIONS | (2020)11:5396 | https://doi.org/10.1038/s41467-020-19074-4 | www.nature.com/naturecommunications

## PDF page 5

ARTICLE

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-020-19074-4

c

a
Truth

Rotation angle (rad)

Estimate

0.05

i

0.2
Phase

Error rate

0.06

0.0

0.04

1000

0

2000

0.03
0.02
0

500

1000

1500

250

0

d
Rotation angle (rad)

Success probability

Time 1000

0.75

Time 2000

0.50

x

–y

–y

–0.01

2000

Time 0

x

0.00

Time (arb. units)

b 1.00

i

0.01

500

750

1000

Time (arb. units)
0.006

0.000

–0.006

0.25
0

20

40

60

80

Randomized benchmarking length

660

700

740

Time (arb. units)

Fig. 2 Time-resolved benchmarking & tomography on simulated data. a, b Time-resolved RB on simulated data for gates with time-dependent phase
errors. a Inset: the simulated phase error over time. Main plot: the true, time-dependent RB error rate (r) versus time (grey line) and a time-resolved
estimate obtained by applying our techniques to simulated data (black line). b Instantaneous average-over-circuits (points) and per-circuit (distributions)
success probabilities at each circuit length, estimated by applying our spectral analysis techniques to the simulated time-series data, and ﬁts to an
exponential (curves), for the three times denoted by the vertical lines in a. Each instantaneous estimate of r, shown in a, is a rescaling of the decay rate of
the exponential ﬁt at that time. c, d Time-resolved GST on simulated data, for three gates Gi, Gx, and Gy that are subject to time-dependent coherent errors
around the ^z, x^, and y^ axes, respectively, by angles θi, θx, and θy. The estimates of these rotation angles (denoted θ^i , θ^x and θ^y ) track the true values closely.
The shaded areas are 2σ (~95%) conﬁdence regions.

predicted by the estimated model (dotted lines, Fig. 1d) with the
model-independent probability estimates obtained earlier (unbroken lines, Fig. 1d). These probabilities are in close agreement.
Demonstration on simulated data. RB7–14 and GST5,6 are two of
the most popular methods for characterizing a QIP. Both methods are robust to state preparation and measurement errors; RB is
fast and simple, whereas GST provides detailed diagnostic
information about the types of errors afﬂicting the QIP. We now
demonstrate time-resolved RB and GST on simulated data, using
the general methodology introduced above. The number of circuits and circuit repetitions in these simulated experiments are in
line with standard practice for these techniques, so they
demonstrate that our techniques can be applied to RB and GST
without additional experimental effort.
We simulated data from 2000 rasters through 100 randomly
sampled RB circuits7–9 on two qubits. The error model consisted
of 1% depolarization on each qubit and a time-dependent
coherent z^-rotation that is shown in the inset of Fig. 2a (see
Supplementary Note 2 for details). The general instability analysis
was implemented on this simulated data, after converting the 4outcome data to the standard “success”/“fail” format of RB. This
analysis yielded a time-dependent success probability for each
circuit. Following our non-intrusive framework, instantaneous
success probabilities at each time of interest were then fed into the
standard RB data analysis (ﬁtting an exponential) as shown for
three times in Fig. 2b. The instantaneous RB error rate estimate is
then (up to a constant9) the decay rate of the ﬁtted exponential at
that time. The resultant time-resolved RB error rate is shown in
Fig. 2a. It closely tracks the true error rate.
GST is a method for high-precision tomographic reconstruction of a set of time-independent gates, state preparations, and
measurements5,6. We consider GST on a gate set comprising
of standard z^-axis preparation and measurement, and three gates
Gx, Gy, and Gi. Here Gx/y are π/2 rotations around the x^=^y axes
and Gi is the idle gate. The GST circuits have the form

Sprep Skgerm Smeas (circuits are written in operation order where
the leftmost operation occurs ﬁrst). In this circuit: Sprep and Smeas
are each one of six short sequences chosen to generate
tomographically complete state preparations and measurements;
Sgerm is one of twelve short “germ” sequences, chosen so that
powers (repetitions) of these germs amplify all coherent,
stochastic and amplitude-damping errors; k runs over an
approximately logarithmically spaced set of integers, given by
k = ⌊L/∣Sgerm∣⌋ where ∣Sgerm∣ is the length of the germ and L ¼
20 ; 21 ; 22 ; ¼ ; Lmax for some maximum germ power Lmax .
We simulated data from 1000 rasters through these GST
circuits (with Lmax ¼ 128). The error model consisted of 0.1%
depolarization on each gate. Additionally, Gx and Gy are subject
to over/under-rotation errors that oscillate both quickly and
slowly, while Gi is subject to slowly varying z^-axis coherent errors.
We used our intrusive approach to time-resolved tomography:
the general instability analysis was implemented on this simulated
data, the results were used to select a time-resolved model for the
gates, and this model was then ﬁt to the time-series data using
maximum likelihood estimation (see Supplementary Note 2 for
details). The resulting time-resolved estimates of the gate rotation
angles are shown in Fig. 2c, d. The estimates closely track the true
values.
Demonstration on experimental data. Having veriﬁed that our
methods are compatible with data from GST circuits, we now
demonstrate time-resolved GST on two sets of experimental data,
using the three gates Gx, Gy, and Gi. These experiments comprehensively quantify the stability of our 171Yb+ qubit, because
the GST circuits are tomographically complete and they amplify
all standard types of error in the gates. The Gx and Gy gates were
implemented with BB1 compensated pulses48,49, and Gi was
implemented with a dynamical decoupling XπYπXπYπ sequence50,
where Xπ and Yπ represent π pulses around the x^ and y^ axes. The
ﬁrst round of data collection included the GST circuits to a

NATURE COMMUNICATIONS | (2020)11:5396 | https://doi.org/10.1038/s41467-020-19074-4 | www.nature.com/naturecommunications

5

## PDF page 6

ARTICLE

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-020-19074-4

b
Measurement sequence

Gi
Gx
Gy

L = 1024

Germ = Gi ,

L = 2048

{}
Gx
Gy
Gx2
Gx3
Gy3
{ } Gx Gy Gx2 Gx3 Gy3

GxGyGi
p

{ } Gx Gy Gx2 Gx3 Gy3

16

GxGi2

12

GyGi2

8

e 1.8

14

Exp. 1, Tx
Exp. 1, Ty
Exp. 1, Tx

Exp. 2, Tx
Exp. 2, Ty
Exp. 2, Tx

Exp. 1, Gi
Exp. 1, Gx
Exp. 1, Gy

Exp. 2, Gi
Exp. 2, Gx
Exp. 2, Gy

0.002

d 0.004
Experiment 1
Experiment 2

6
4
2

1.4

1.0

0

Gx2GyGxGy2
0

0.004

Expected shot noice

10

GxGy2Gi

0.006

0

Diamond distance error ( )

GxGiGy

Gx2GiGy

c 0.008

Preparation sequence

Spectral power

Germ sequence

GxGy

Germ = Gi ,

Rotation angles of Gi (rad)

a

2

4

8

16
32
64 128 256 512 1024 2048
Approximate circuit length (L)

0.6
10–5

10–3
10–4
Frequency (Hz)

10–2

0.003

0.002

0.001

0

0

0.25

0.5

0.75

1

Time (fraction of tmax)

Fig. 3 Measuring qubit stability using time-resolved GST. The results of two time-resolved GST experiments using the gates Gi, Gx, and Gy, with drift
compensation added for the second experiment. a, b The evidence for instability in each circuit in the ﬁrst experiment, quantiﬁed by λp ¼ log 10 ðpÞ where
p is the p-value of the largest power in the spectrum for that circuit. A pixel is colored green when λp is large enough to be 5% statistically signiﬁcant,
otherwise, it is greyscale. Each circuit consists of repeating a “germ” sequence in between six initialization and pre-measurement sequences. The data is
arranged by germ and approximate circuit length L, and then separated into the 6 × 6 different preparation and measurement sequence pairs, as shown on
the axes of B (“{}” denotes the null sequence). Only long circuits containing repeated applications of Gi exhibit evidence of drift. In the second experiment,
none of the λp are statistically signiﬁcant (data are not shown). c, d Time-resolved tomographic reconstructions of the gates in each experiment,
summarized by the diamond distance error of each gate, and the decomposition of the coherent errors in Gi into rotation angles around x^, y^ and z^
(tmax  5:5 h and tmax  40 h for the ﬁrst and second experiment, respectively). e The power spectrum for each experiment obtained by averaging the
individual power spectra for the different circuits, with ﬁlled points denoting power above the 5% signiﬁcance thresholds (the thresholds are not shown).

maximum germ power of Lmax = 2048 (resulting in 3889 circuits). These circuits were rastered 300 times over ~5.5 h.
Figure 3a, b summarizes the results of our general instability
assessment on this data, using a representation that is tailored to
GST circuits. Each pixel in this plot corresponds to a single circuit
and summarizes the evidence for instability by λp ¼ log 10 ðpÞ,
where p is the p-value of the largest power in the spectrum for
that circuit (λp is 5% signiﬁcant when it is above the multitest adjusted threshold λp,threshold ≈ 7). The only circuits that
displayed detectable instability are those that contain many
sequential applications of Gi. Figure 3b further narrows this down
to generalized Ramsey circuits, whereby the qubit is prepared on
the equator of the Bloch sphere, active idle gates are applied, and
then the qubit is measured on the equator of the Bloch sphere.
These circuits amplify erroneous z^-axis rotations in Gi. Other
GST circuits amplify all other errors, but none of those circuits
exhibit detectable drift. This is conclusive evidence that the angle
of these z^-axis rotations is varying over the course of the
experiment.
The instability in Gi can be quantiﬁed by implementing timeresolved GST, with the z^-axis error in Gi expanded into a
summation of Fourier coefﬁcients (see Supplementary Note 2 for
details). The results are summarized in Fig. 3c, d (dotted lines).
Figure 3d shows the diamond distance error rate (ϵ♢)51 in the
three gates over time. It shows that Gi is the worst performing
gate and that the error rate of Gi drifts substantially over the
course of the experiment (ϵ♢ varies by ~25%). The gate inﬁdelities
are an order of magnitude smaller (Supplementary Table 1).
Figure 3c shows the coherent component of the Gi gate over time,
resolved into rotation angles θx, θy, and θz around the three Bloch
sphere axes x^, y^, and z^. The varying z^-axis component is the
dominant source of error.
This ﬁrst round of experiments revealed instability, so we
changed the experimental setup. Changes included the addition
of periodic recalibration of the microwave drive frequency, the
6

π-pulse duration, and the pointing of the detection laser (details
in the Methods). We then repeated this GST experiment. To
increase sensitivity to any instability, we collected more data, over
a longer time period, and we included longer circuits. We ran the
GST circuits out to a maximum germ power of Lmax = 16,384,
rastering 328 times through this set of 5041 circuits over ~40 h.
The purpose of running such a comprehensive experiment was to
maximize sensitivity—our methods need much fewer experimental resources for useful results (see below). Repeating the
above analysis on this data, we found that none of the λp
were statistically signiﬁcant, i.e., no instability was detected in any
circuit, including circuits containing over 105 sequential Gi gates.
Again, we performed time-resolved GST. Since no time
dependence was detected, this reduces to standard timeindependent GST. The results are summarized in Fig. 3c, d
(unbroken lines). The gate error rates have been substantially
suppressed (ϵ♢ decreased by ~10× for Gi), and the z^-axis
coherent error in Gi reduced and stabilized. This is a
comprehensive demonstration that the recalibrations are stabilizing the qubit. Furthermore, the recalibrated parameters versus
time are strongly correlated with ambient laboratory temperature
(see the Methods), suggesting temperature stabilization as an
alternative route to qubit stabilization, and supporting the
conclusions of our Ramsey experiments.
No individual circuit exhibited signs of drift in this second GST
experiment, but we can also perform a collective test for
instability on the clickstreams from all the circuits. In particular,
we can average the per-circuit power spectra, and look for
statistically signiﬁcant peaks in this single spectrum. This
suppresses the shot noise inherent in each individual clickstream,
so it can reveal low-power drift that would otherwise be hidden in
the noise (Supplemental Note 1). This average spectrum is shown
for both experiments in Fig. 3e. The power at low frequencies
decreases substantially from the ﬁrst to the second experiment,
further demonstrating that our drift compensation is stabilizing

NATURE COMMUNICATIONS | (2020)11:5396 | https://doi.org/10.1038/s41467-020-19074-4 | www.nature.com/naturecommunications

## PDF page 7

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-020-19074-4

the qubit. However, there is power above the 5% signiﬁcance
threshold for both experiments. So there is still some residual
instability after the experimental improvements. But this residual
drift is no longer a signiﬁcant source of errors, as demonstrated
by the low and stable error rates shown in Fig. 3d.
Experiment design. Our method is an efﬁcient way to identify
time dependence in the outcome probability distribution of any
quantum circuit. In its most basic application, it can verify the
stability of application or benchmarking data. No special-purpose
circuits are required, as the drift detection can be applied to data
that is already being taken. The analysis will then be sensitive to
any drifting errors that impact this application, in proportion to
their effect on the application.
As we have demonstrated, our method can also be used to
create dedicated drift characterization protocols. This mode
requires a carefully chosen set of quantum circuits that are
sensitive to the speciﬁc parameters under study. Without a priori
knowledge about what may be drifting, this circuit set should be
sensitive to all of the parameters of a gate set. The GST circuits
are a good choice. However, if only a few parameters are expected
to drift, a smaller set of circuits sensitive only to these parameters
can be used, resulting in a more efﬁcient experiment. For
example, Ramsey circuits serve as excellent probes of time
variation in qubit phase rotation rates. Many of the most sensitive
circuits, such as those used in GST, Ramsey spectroscopy, and
robust phase estimation15, are periodic and extensible. These
circuits achieve Oð1=LÞ precision scaling, with L the maximum
circuit length, up until decoherence dominates. So, by choosing a
suitably large L, very high-precision drift tracking can be
achieved, as in our experiments.
Interleaving dedicated drift characterization circuits with
application circuits combines the two use cases for our methods
—dedicated drift characterization and auxiliary analysis. This
reduces the data acquisition rate for both the application and
characterization circuits, but it directly probes whether time
variation in a parametric model is correlated with drift in the
outcomes of an application circuit. While this reduces sensitivity
to high-frequency instabilities, much of the drift seen in the
laboratory is on timescales that are long compared to the data
acquisition rate. As a simple demonstration of this, we note that
discarding 80% of our Ramsey data—keeping only every ﬁfth bit
for each circuit—still yields a high-precision time-resolved phase
estimate, as shown in Fig. 1e (gray dashed line).
The sensitivity of our analysis depends on both the number of
times a circuit is repeated (N) and the sampling rate (tgap). As in
all signal analysis techniques, the sampling rate sets the Nyquist
limit—the highest frequency the analysis is sensitive to without
aliasing—while (N − 1)tgap sets the lowest frequency drift that
will be visible. While the sensitivity of our methods increases with
more data, statistically signiﬁcant results can be achieved without
dedicating hours or days to data collection. For example, both the
simulated GST and RB experiments (Fig. 2) used a number of
circuits and repetitions consistent with standard practices.
Further details relating to the sampling parameters and the
analysis sensitivity are provided in Supplementary Note 3.
Discussion
Reliable quantum computation demands stable hardware. But
current standards for characterizing QIPs assume stability—they
cannot verify that a QIP is stable, nor can they quantify
any instabilities. This is becoming a critical concern as stable
sources of errors are steadily reduced. For example, drift signiﬁcantly impacted the recent tomographic experiments of
Wan et al.22 but this was only veriﬁed using a complicated,

ARTICLE

special-purpose analysis. In this article, we have introduced a
general, ﬂexible, and powerful methodology for diagnosing
instabilities in a QIP. We have applied these methods to a trappedion qubit, demonstrating both time-resolved phase estimation and
time-resolved tomographic reconstructions of logic gates. Using
these tools, we were able to identify the most unstable gate, conﬁrm that periodic recalibration stabilized the qubit to an extent
that drift is no longer a signiﬁcant source of error, and isolate the
probable source of the instabilities (temperature changes).
Our methods are widely-applicable, platform-independent, and
do not require special-purpose experiments. This is because the
core techniques are applicable to the data from any set of
quantum circuits—as long as it is recorded as a time series—and
the data analysis is fast and simple (speed is limited only by the
fast Fourier transform). These techniques enable routine stability
analysis on data gathered primarily for other purposes, such as
data from algorithmic, benchmarking, or error correction circuits.
These techniques are even applicable outside of the context of
quantum computing—they could be used for time-resolved
quantum sensing. We have incorporated these tools into an
open-source software package52,53, making it easy to check any
time-series QIP data for signs of instability. Because of the disastrous impact of drift on characterization protocols16–22, its
largely unknown impact on QIP applications, and the minimal
overhead required to implement our methods, we hope to see this
analysis broadly and quickly adopted.
Methods

Experiment details. We trap a single 171Yb+ ion ~34 μm above a Sandia multilayer surface ion trap with integrated microwave antennae, shown in Supplementary Fig. 1. The radial trapping potential is formed with 170 V of rf-drive at 88
MHz; the axial ﬁeld is generated by up to 2 V on the segmented dc control
electrodes. This yields secular trap frequencies of 0.7, 5, and 5.5 for the axial and
radial modes, respectively. An electromagnetic coil aligned with its axis perpendicular to the trap surface creates the quantization ﬁeld of ~5 G at the ion. The ﬁeld
magnitude is calibrated using the qubit transition frequency, which has a secondorder dependence on the magnetic ﬁeld of f = 12.642 812 118 GHz + 310.8B2 Hz,
where B is the externally applied magnetic ﬁeld in Gauss54. The qubit is encoded in
the hyperﬁne clock states of the 2S1/2 ground state of 171Yb+, with logical 0 and 1
deﬁned as jF ¼ 0; mF ¼ 0i and jF ¼ 1; mF ¼ 0i, respectively.
Each run of a quantum circuit consists of four steps: cooling the ion, preparing
the input state, performing the gates, and then measuring the ion. First, using an
adaptive length Doppler cooling scheme, we verify the presence of the ion. The ion
is Doppler cooled for 1 ms, during which ﬂuorescence events are counted. If the
number of detected photons is above a threshold (~85% of the average ﬂuorescence
observed for a cooled ion) Doppler cooling is complete, otherwise, the cooling is
repeated. If the threshold is not reached after 300 repetitions, the experiment is
halted to load a new ion. This ensures that an ion is present in the trap and that it is
approximately the same temperature for each run. After cooling and verifying the
presence of the ion, it is prepared in the jF ¼ 0; mF ¼ 0i ground state using an
optical pumping pulse55. All active gates are implemented by directly driving the
12.6428 GHz hyperﬁne qubit transition, using a near-ﬁeld antenna integrated into
the trap (Supplementary Fig. 1). The methods used for generating microwave
radiation are discussed in ref. 5. A standard state ﬂuorescence technique55 is used to
measure the ﬁnal state of the qubit.
The gates we use are Gx, Gy, and Gi, which are π/2 rotations around the x^- and
y^-axes, and an idle gate. The Gx and Gy gates, used in both the Ramsey and GST
experiments, are implemented using BB1 pulse sequences48,49. The Gi gate, used
only in the GST experiments, is a second-order compensation sequence:
Gi = XπYπXπYπ, where Xπ and Yπ denote π pulses about the x^- and y^-axis,
respectively50. To maintain a constant power on the microwave ampliﬁer and
reduce the errors from ﬁnite on/off times, active gates are performed gapless, i.e.,
we transition from one pulse to the next by adjusting the phase of the microwave
signal without changing the amplitude of the microwave radiation. In the ﬁrst GST
experiment, the Rabi frequency was 119 kHz.
Changing the phase in the analog output signal takes ~5 ns and this causes
errors because the pulse sequences are performed gapless. These errors are larger
for shorter π-pulse times. To reduce this error, in this second GST experiment the
Rabi frequency was decreased to 74 kHz. To compensate for the drift that we
observed in both the Ramsey experiment and the ﬁrst GST experiment, in the
second GST experiment we incorporated three forms of active drift control. The
detection laser position was recalibrated every 45 minutes, and both the π-time (τπ)
and the microwave drive frequency (f) were updated based on the results of
interleaved calibration circuits. After every 4th circuit, a circuit consisting of a

NATURE COMMUNICATIONS | (2020)11:5396 | https://doi.org/10.1038/s41467-020-19074-4 | www.nature.com/naturecommunications

7

## PDF page 8

ARTICLE

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-020-19074-4

References
1.

T (K)

2.
3.

f (Hz)

4.
5.

x (m)

6.

 (s)

7.
8.

Fig. 4 Ancillary measurements in the stabilized GST experiment. The
microwave drive frequency f, the horizontal and vertical detection beam
offsets x, and microwave π-pulse time τπ were periodically recalibrated and
tracked over the course of the experiment. The Spearman correlation
coefﬁcient (ρ) conﬁrms that the ambient temperature T is well correlated
with the drive frequency (ρ = 0.64) and the horizontal and vertical beam
offsets (ρ = 0.86 and ρ = 0.84), but it is not well correlated with the
π-pulse time (ρ = 0.05).
10.5π pulse was performed. If the outcome was 0 (resp., 1) then 1.25 ns was added
to τπ (resp., subtracted from τπ). The applied π-time is τπ rounded to an integer
multiple of 20 ns, so only consistently bright or dark measurements result in
changes of the pulse time. After every 16th circuit, a 10 ms wait Ramsey circuit was
performed. If the outcome was 0 (resp., 1) 10 mHz is added to f (resp., subtracted
from f).
Figure 4 shows the detection beam position, τπ, f, and ambient laboratory
temperature over the course of the second GST experiment. The calibrated f is
correlated with the ambient temperature. This is consistent with the observed
correlation between the ambient temperature and the estimated detuning in the
Ramsey experiment (Fig. 1e). The temperature is also strongly correlated with the
calibrated detection beam location points, suggesting that thermal expansion is a
plausible underlying cause of the frequency shift.
Data analysis details. To generate a power spectrum from a clickstream, we use
the Type-II discrete cosine transform with an orthogonal normalization. This is the
matrix F with elements
sﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ
 

21δω;0
ωπ
1
ð2Þ
F ωi ¼
cos
iþ
;
N
N
2
where ω, i = 0, …, N − 156. However, note that the exact transform used is not
important: we only require that F is an orthogonal and Fourier-like matrix (Supplementary Note 1). Our hypothesis testing is all at a statistical signiﬁcance of 5%
and uses a Bonferroni correction to maintain this signiﬁcance when implementing
many hypothesis tests (Supplementary Note 1). All data ﬁtting uses maximum
likelihood estimation, except for the p(t) estimation in the time-resolved RB
simulations. In that case, we use a simple form of signal ﬁltering (see Supplementary Note 1), so that the entire analysis chain maintains the speed and simplicity inherent to RB. When choosing between multiple time-resolved models, as
in the time-resolved Ramsey tomography and GST analyses, we use the Akaike
information criteria47 to avoid overﬁtting (Supplementary Note 2). Further details
on these methods, and supporting theory, is provided in Supplementary Notes 1–3.

Data availability
All experimental and simulated data presented in this paper are available at https://doi.
org/10.5281/zenodo.4033077.

Code availability
The code for implementing the general drift characterization methods introduced in this
paper has been incorporated into the open-source Python package pyGSTi52,53. The
pyGSTi-based Python scripts and notebooks used for the data analysis reported in this
paper are available at https://doi.org/10.5281/zenodo.4033077.

Received: 31 July 2019; Accepted: 21 September 2020;

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
26.
27.
28.

29.

30.

31.
32.
33.
34.
35.
36.

8

Rol, M. A. et al. Restless tuneup of high-ﬁdelity qubit gates. Phys. Rev. Appl. 7,
041001 (2017).
Otterbach, J. S. et al. Unsupervised machine learning on a hybrid quantum
computer. Preprint at http://arxiv.org/abs/1712.05771 (2017).
Friis, N. et al. Observation of entangled states of a fully controlled 20-qubit
system. Phys. Rev. X 8, 021012 (2018).
Arute, F. et al. Quantum supremacy using a programmable superconducting
processor. Nature 574, 505–510 (2019).
Blume-Kohout, R. et al. Demonstration of qubit operations below a rigorous
fault tolerance threshold with gate set tomography. Nat. Commun. 8, 14485
(2017).
Merkel, S. T. et al. Self-consistent quantum process tomography. Phys. Rev. A
87, 062119 (2013).
Knill, E. et al. Randomized benchmarking of quantum gates. Phys. Rev. A 77,
012307 (2008).
Magesan, E., Gambetta, J. M. & Emerson, J. Scalable and robust randomized
benchmarking of quantum processes. Phys. Rev. Lett. 106, 180504 (2011).
Proctor, T. J. et al. Direct randomized benchmarking for multiqubit devices.
Phys. Rev. Lett. 123, 030503 (2019).
Magesan, E. et al. Efﬁcient measurement of quantum gate error by interleaved
randomized benchmarking. Phys. Rev. Lett. 109, 080505 (2012).
Cross, A. W., Magesan, E., Bishop, L. S., Smolin, J. A. & Gambetta, J. M.
Scalable randomised benchmarking of non-clifford gates. NPJ Quantum Inf. 2,
16012 (2016).
Barends, R. et al. Rolling quantum dice with a superconducting qubit. Phys.
Rev. A 90, 030303 (2014).
Carignan-Dugas, A., Wallman, J. J. & Emerson, J. Characterizing universal
gate sets via dihedral benchmarking. Phys. Rev. A 92, 060302 (2015).
Gambetta, J. M. et al. Characterization of addressability by simultaneous
randomized benchmarking. Phys. Rev. Lett. 109, 240504 (2012).
Kimmel, S., Low, G. H. & Yoder, T. J. Robust calibration of a universal singlequbit gate set via robust phase estimation. Phys. Rev. A 92, 062315 (2015).
Dehollain, J. P. et al. Optimization of a solid-state electron spin qubit using
gate set tomography. New J. Phys. 18, 103018 (2016).
Epstein, J. M., Cross, A. W., Magesan, E. & Gambetta, J. M. Investigating the
limits of randomized benchmarking protocols. Phys. Rev. A 89, 062321 (2014).
van Enk, S. J. & Blume-Kohout, R. When quantum tomography goes wrong:
drift of quantum sources and other errors. New J. Phys. 15, 025024 (2013).
Fong, B. H. & Merkel, S. T. Randomized benchmarking, correlated noise, and
ising models. Preprint at http://arxiv.org/abs/1703.09747 (2017).
Chow, J. M. et al. Randomized benchmarking and process tomography for
gate errors in a solid-state qubit. Phys. Rev. Lett. 102, 090502 (2009).
Fogarty, M. A. et al. Nonexponential ﬁdelity decay in randomized
benchmarking with low-frequency noise. Phys. Rev. A 92, 022326 (2015).
Wan, Y. et al. Quantum gate teleportation between separated qubits in a
trapped-ion processor. Science 364, 875–878 (2019).
Harris, R. et al. Probing noise in ﬂux qubits via macroscopic resonant
tunneling. Phys. Rev. Lett. 101, 117003 (2008).
Bylander, J. et al. Noise spectroscopy through dynamical decoupling with a
superconducting ﬂux qubit. Nat. Phys. 7, 565 (2011).
Chan, K. W. et al. Assessment of a silicon quantum dot spin qubit
environment via noise spectroscopy. Phys. Rev. Appl. 10, 044017 (2018).
Klimov, P. V. et al. Fluctuations of energy-relaxation times in superconducting
qubits. Phys. Rev. Lett. 121, 090502 (2018).
Megrant, A. et al. Planar superconducting resonators with internal quality
factors above one million. Appl. Phys. Lett. 100, 113510 (2012).
Müller, C., Lisenfeld, J., Shnirman, A. & Poletto, S. Interacting two-level
defects as sources of ﬂuctuating high-frequency noise in superconducting
circuits. Phys. Rev. B 92, 035442 (2015).
Meißner, S. M., Seiler, A., Lisenfeld, J., Ustinov, A. V. & Weiss, G. Probing
individual tunneling ﬂuctuators with coherently controlled tunneling systems.
Phys. Rev. B 97, 180505 (2018).
De Graaf, S. E. et al. Suppression of low-frequency charge noise in
superconducting resonators by surface spin desorption. Nat. Commun. 9, 1143
(2018).
Merkel, B. et al. Magnetic ﬁeld stabilization system for atomic physics
experiments. Rev. Sci. Instrum 90, 044702 (2019).
Burnett, J. et al. Decoherence benchmarking of superconducting qubits. NPJ
Quantum Inf. 5, 54 (2019).
Cortez, L. et al. Rapid estimation of drifting parameters in continuously
measured quantum systems. Phys. Rev. A 95, 012314 (2017).
Bonato, C. & Berry, D. W. Adaptive tracking of a time-varying ﬁeld with a
quantum sensor. Phys. Rev. A 95, 052348 (2017).
Wheatley, T. A. Adaptive optical phase estimation using time-symmetric
quantum smoothing. Phys. Rev. Lett. 104, 093601 (2010).
Young, K. C. & Whaley, K. B. Qubits as spectrometers of dephasing noise.
Phys. Rev. A 86, 012314 (2012).

NATURE COMMUNICATIONS | (2020)11:5396 | https://doi.org/10.1038/s41467-020-19074-4 | www.nature.com/naturecommunications

## PDF page 9

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-020-19074-4

37. Gupta, R. S. & Biercuk, M. J. Machine learning for predictive estimation of
qubit dynamics subject to dephasing. Phys. Rev. Appl. 9, 064042 (2018).
38. Granade, C., Combes, J. & Cory, D. G. Practical bayesian tomography. New J.
Phys. 18, 033024 (2016).
39. Granade, C. et al. Qinfer: Statistical inference software for quantum
applications. Quantum 1, 5 (2017).
40. Huo, M.-X. & Li, Y. Learning time-dependent noise to reduce logical errors:
Real time error rate estimation in quantum error correction. N. J. Phys. 19,
123032 (2017).
41. Kelly, J. et al. Scalable in situ qubit calibration during repetitive error
detection. Phys. Rev. A 94, 032321 (2016).
42. Huo, M. & Li, Y. Self-consistent tomography of temporally correlated errors.
Preprint at http://arxiv.org/abs/1811.02734 (2018).
43. Rudinger, K. et al. Probing context-dependent errors in quantum processors.
Phys. Rev. X 9, 021045 (2019).
44. Donoho, D. L. Compressed sensing. IEEE Trans. Inf. Theory 52, 1289–1306
(2006).
45. Lehmann, E. L. & Romano, J. P. Testing Statistical Hypotheses (Springer
Science, Business Media, 2006).
46. Shaffer, J. P. Multiple hypothesis testing. Ann. Rev. Psychol. 46, 561–584
(1995).
47. Hirotugu, A. A new look at the statistical model identiﬁcation. IEEE Trans.
Autom. Control 19, 716–723 (1974).
48. Stephen, W. Broadband, narrowband, and passband composite pulses for
use in advanced nmr experiments. J. Magn. Reson. Series A 109, 221–231
(1994).
49. True Merrill, J. & Kenneth R. B. Progress in compensating pulse sequences for
quantum computation. Preprint at http://arxiv.org/abs/1203.6392 (2012).
50. Khodjasteh, K. & Viola, L. Dynamical quantum error correction of unitary
operations with bounded controls. Phys. Rev. A 80, 032314 (2009).
51. Aharonov, D., Kitaev, A. & Nisan, N. Proc. Thirtieth Annual ACM Symposium
on Theory of Computing 20–30 (ACM, 1998).
52. Nielsen, E. et al. PyGSTi Pre-release of Version 0.9.10: 7c6ddd1. https://github.
com/pyGSTio/pyGSTi/tree/7c6ddd1de209b795ea39bfb69d010b687e812d07
(2020).
53. Nielsen, E. et al. Probing quantum processor performance with pyGSTi.
Quantum Sci. Technol. 5, 044002 (2020).
54. Fisk, P. T. H., Sellars, M. J., Lawn, M. A. & Coles, G. Accurate measurement of
the 12.6 GHz “clock” transition in trapped 71Yb+ ions. IEEE Trans.
Ultrasonics Ferroelectr. Freq. Control 44, 344–354 (1997).
55. Olmschenk, S. et al. Manipulation and detection of a trapped Yb+ hyperﬁne
qubit. Phys. Rev. A 76, 052314 (2007).
56. Nasir, A., Natarajan, T. & Rao, K. R. Discrete cosine transform. IEEE Trans.
Comput. 100, 90–93 (1974).

ARTICLE

Director of National Intelligence (ODNI), Intelligence Advanced Research Projects
Activity (IARPA); and the Laboratory Directed Research and Development program at
Sandia National Laboratories. Sandia National Laboratories is a multi-program laboratory managed and operated by National Technology and Engineering Solutions of
Sandia, LLC, a wholly-owned subsidiary of Honeywell International, Inc., for the U.S.
Department of Energy’s National Nuclear Security Administration under contract DENA-0003525. All statements of fact, opinion, or conclusions contained herein are those
of the authors and should not be construed as representing the ofﬁcial views or policies of
IARPA, the ODNI, the U.S. Department of Energy, or the U.S. Government.

Author contributions
T.P., E.N., K.R., R.B.-K., and K.Y. developed the methods. M.R., D.L., and P.M. performed the experiments.

Competing interests
The authors declare no competing interests.

Additional information
Supplementary information is available for this paper at https://doi.org/10.1038/s41467020-19074-4.
Correspondence and requests for materials should be addressed to T.P.
Peer review information Nature Communications thanks the anonymous reviewer(s) for
their contribution to the peer review of this work.
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

Acknowledgements
This work was supported by the U.S. Department of Energy, Ofﬁce of Science, Ofﬁce of
Advanced Scientiﬁc Computing Research Quantum Testbed Program; the Ofﬁce of the

This is a U.S. government work and not under copyright protection in the U.S.; foreign
copyright protection may apply 2020

NATURE COMMUNICATIONS | (2020)11:5396 | https://doi.org/10.1038/s41467-020-19074-4 | www.nature.com/naturecommunications

9
