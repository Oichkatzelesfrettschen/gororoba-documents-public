Source: https://doi.org/10.1103/PRXQuantum.5.030353
PDF sha256: cd88b550767ea735aea17096faf4bded446f81b3d258749809e5fe0d8a470882
License: https://creativecommons.org/licenses/by/4.0/

# Transcription of hyyppa_2024_reducing_leakage_single_qubit_gates_analytical_pulse_envelopes.pdf

Transcription of `hyyppa_2024_reducing_leakage_single_qubit_gates_analytical_pulse_envelopes.pdf` in this directory, 28 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-28 from the PDF's own text layer (pdftotext version 26.10.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

PRX QUANTUM 5, 030353 (2024)

Reducing Leakage of Single-Qubit Gates for Superconducting Quantum
Processors Using Analytical Control Pulse Envelopes
Eric Hyyppä ,1,* Antti Vepsäläinen ,1 Miha Papič ,2,3 Chun Fai Chan ,1 Sinan Inel ,1
Alessandro Landra ,1 Wei Liu ,1 Jürgen Luus ,1 Fabian Marxer ,1 Caspar Ockeloen-Korppi ,1
Sebastian Orbell ,1,4 Brian Tarasinski ,1 and Johannes Heinsoo 1
1

IQM Quantum Computers, Keilaranta 19, Espoo 02150, Finland
IQM Quantum Computers, Georg-Brauchle-Ring 23-25, Munich 80992, Germany
3
Department of Physics and Arnold Sommerfeld Center for Theoretical Physics, Ludwig-Maximilians-Universität
München, Theresienstr. 37, Munich 80333, Germany
4
Department of Materials, University of Oxford, Oxford, United Kingdom
2

(Received 15 March 2024; revised 21 June 2024; accepted 26 August 2024; published 19 September 2024)
Improving the speed and ﬁdelity of quantum logic gates is essential to reach quantum advantage with
future quantum computers. However, fast logic gates lead to increased leakage errors in superconducting
quantum processors based on qubits with low anharmonicity, such as transmons. To reduce leakage errors,
we propose and experimentally demonstrate two new analytical methods, Fourier ansatz spectrum tuning
derivative removal by adiabatic gate (FAST DRAG) and higher-derivative (HD) DRAG, both of which
enable shaping single-qubit control pulses in the frequency domain to achieve stronger suppression of
leakage transitions compared to previously demonstrated pulse shapes. Using the new methods to suppress
the ef transition of a transmon qubit with an anharmonicity of −212 MHz, we implement RX (π/2) gates
achieving a leakage error below 3.0 × 10−5 down to a gate duration of 6.25 ns without the need for
iterative closed-loop optimization. The obtained leakage error represents a 20-fold reduction in leakage
compared to a conventional cosine DRAG pulse. Employing the FAST DRAG method, we further achieve
an error per gate of (1.56 ± 0.07) × 10−4 at a 7.9-ns gate duration, outperforming conventional pulse
shapes both in terms of error and gate speed. Furthermore, we study error-amplifying measurements for
the characterization of temporal microwave control-pulse distortions, and demonstrate that non-Markovian
coherent errors caused by such distortions may be a signiﬁcant source of error for sub-10-ns single-qubit
gates unless corrected using predistortion.
DOI: 10.1103/PRXQuantum.5.030353

I. INTRODUCTION
Superconducting qubits provide a promising platform
for realizing large-scale quantum computers as they enable
high-ﬁdelity quantum logic gate operations in the nanosecond regime [1–8], potentially resulting in signiﬁcantly
faster computations compared to other state-of-the-art
quantum computing platforms, such as neutral atoms
[9–11] or trapped ions [12,13]. Improving the gate speed
further would not only increase the clock speed of the
quantum computer but it would also reduce the incoherent gate errors caused by decoherence, thus enabling even
*

Contact author: eric@meetiqm.com

Published by the American Physical Society under the terms of
the Creative Commons Attribution 4.0 International license. Further distribution of this work must maintain attribution to the
author(s) and the published article’s title, journal citation, and
DOI.

2691-3399/24/5(3)/030353(28)

higher ﬁdelities. Currently, the large-scale superconducting quantum processing units (QPU) are based on transmon qubits, which suﬀer from frequency crowding and a
low anharmonicity typically in the range of |α/(2π )| ∈
[150, 300] MHz [1,2,14]. Thus, fast logic gates cause the
frequency spectra of the control pulses to overlap with
transitions out of the computational subspace—such as the
ef transition—resulting in leakage errors [15–18]. Leakage is particularly harmful for quantum error-correction
applications [19–21] in transmon-based processors due to
the generation of nonlocal errors as a result of leakage
being propagated by entangling two-qubit gates [22].
There are two main strategies to mitigate leakage errors
in superconducting qubits. The ﬁrst strategy aims to prevent the occurrence of leakage in the ﬁrst place, e.g.,
using pulse-shape engineering [1,7,15–18,23–31], whereas
the second strategy relies on leakage reduction units converting already occurred leakage errors into Pauli errors
[22,32,33]. In this work, we focus on the ﬁrst strategy

030353-1

Published by the American Physical Society

## PDF page 2

ERIC HYYPPÄ et al.

PRX QUANTUM 5, 030353 (2024)

that enables the reduction of the overall error for fast
logic operations. Leakage errors caused by single-qubit
control pulses are often suppressed using the derivative
removal by adiabatic gate (DRAG) method that sets the
quadrature envelope of a control pulse equal to a scaled
derivative of its in-phase envelope [15,17,18]. This eﬀectively suppresses the frequency spectrum of the control
pulse at a speciﬁc frequency, such as the ef -transition
frequency, reducing leakage related to the suppressed transition. Additionally, the leakage error can be reduced by
the choice of the control-pulse envelopes, for example,
using the Slepian pulse shape [4,5,26] that is commonly
applied in two-qubit gates to minimize the spectral energy
above a given cutoﬀ frequency. Furthermore, optimal control methods have been shown to reduce leakage errors of
fast gates. For example, the lowest leakage error for fast
transmon-based single-qubit gates has been achieved using
experimental closed-loop optimization of piecewise constant RX (π/2) control pulses with 23 parameters, which
resulted in a leakage rate per Cliﬀord gate of 4.4 × 10−4
at a pulse duration of tg = 4.16 ns (tg |α|/(2π ) ≈ 1.31)
[7]. However, such closed-loop optimization methods may
require a large number of iterations, leading to increased
calibration time [7]. Open-loop optimal control techniques
may provide signiﬁcantly faster convergence by optimizing the control pulses in a simulation [34–39], but the
obtained pulse shapes may not transfer well to an experimental implementation if the assumed model Hamiltonian
does not capture all the relevant details of the experimental
system, such as electronics limitations, pulse distortions, or
parasitic interactions.
Two-qubit gate ﬁdelities in superconducting quantum processors have recently improved considerably
[4–6,40–42], and hence, further improvements are needed
for single-qubit gates that typically appear in quantum
circuits in higher numbers compared to two-qubit gates
[14,40,43]. In this work, we demonstrate two new methods
for engineering single-qubit gate pulse shapes that enable
a more ﬂexible control of the frequency spectrum resulting in signiﬁcantly reduced leakage errors for fast gates
without the need for closed-loop optimization. Applying
the new methods to implement single-qubit gates on a
transmon with an anharmonicity of α/(2π ) = −212 MHz,
we experimentally achieve an average leakage error per
RX (π/2) gate below 3 × 10−5 down to a gate duration of
tg = 6.25 ns (tg |α|/(2π ) ≈ 1.33) approaching the speed
limit of single-qubit gates tg ∼ 2π/|α| [27,44]. At such
short gate durations, the proposed methods reduce the leakage error by a factor of 20 compared to DRAG with a
conventional cosine envelope and by an order of magnitude compared to the previous lowest leakage rate at a
comparable gate duration [7]. Importantly, one of the novel
approaches presented here, Fourier ansatz spectrum tuning
(FAST) DRAG, enables the implementation of a 7.9-ns
RX (π/2) gate with a gate error of (1.56 ± 0.07) × 10−4 ,

reducing the gate error and improving the gate speed over
the conventional pulse shapes. In addition to low errors,
the proposed methods also reduce the required peak power
of sub-10-ns single-qubit gates compared to conventional
pulse shapes. Furthermore, we study error mechanisms
relevant for fast single-qubit gates with ﬁdelities approaching 99.99%, and ﬁnd that non-Markovian coherent errors
caused by microwave control pulse distortions [45] may
be a major error source in addition to incoherent errors
and leakage. We characterize the microwave pulse distortions in our experimental system using simple errorampliﬁcation experiments and show that the gate ﬁdelity
can be improved by predistorting the microwave control
pulses.
II. CONTROL PULSES FOR SUPPRESSING
LEAKAGE ERRORS
A. Introduction to single-qubit gates and DRAG
Single-qubit rotations of superconducting qubits are typically implemented with nearly resonant microwave drive
pulses as illustrated in Fig. 1(a) with the drive pulses
applied to a drive line, which is either capacitively or
inductively coupled to the qubit. In the frame rotating at
the microwave drive frequency fd = ωd /(2π ), the Hamiltonian of a driven nonlinear oscillator, such as a transmon
qubit, can be written as [15]
)
∑(
Q (t) y
I (t) x
HR = ℏ
δj |j ⟩⟨j | +
+
σ
σj −1,j ,
2 j −1,j
2
j
(1)
where δj = ωj − j ωd is the detuning corresponding to
the j th energy level with energy ℏωj , I (t) and Q (t)
are the in-phase and quadrature components of the complex envelope IQ (t) = I (t) − iQ (t) related to the control pulse rf (t) = I (t) cos(ωd t) + Q (t) sin(ωd t) with
a pulse duration tp , and the Pauli-like operators are
y
given by σjx−1,j = λj (|j ⟩⟨j − 1| + |j − 1⟩⟨j |) and σj −1,j =
iλj (|j ⟩⟨j − 1| − |j − 1⟩⟨j |). For a resonantly driven transmon qubit, the drive frequency ωd matches the qubit frequency ωq = ω1 − ω0 , and the state space can be approximately truncated to the three lowest levels
with δ1 = 0,
√
δ2 = ω2 − 2ω1 = α, λ1 = 1, and λ2 ≈ 2. From Eq. (1),
we observe that I (Q ) induces rotations around the x
axis (y axis) in the computational subspace with the angle
of rotation controlled by the integral of the envelope.
For superconducting qubits, errors during single-qubit
gates are mainly caused by decoherence and the coupling
of the qubit drive to state transitions other than the target
transition, which induces phase errors and leakage out of
the computational subspace if left uncorrected [17,18,23,
46–48]. Phase errors arise if the phase of the microwave
drive evolves at a diﬀerent rate compared to the phase of
the qubit. Even though the drive frequency would be equal

030353-2

## PDF page 3

REDUCING LEAKAGE OF SINGLE-QUBIT GATES. . .

I

(c)

Q

tp=6 ns

FAST DRAG-L

100
10 1
10 2
FAST DRAG-L
Cosine DRAG-L

10 3

750 500 250

I

Q
tp=6 ns

FAST DRAG-L

(f)

0.5

1.0

Amplitude spectrum | IQ(f)|

(e) FAST DRAG-P

Q

10 1
10 2

10 1
10 2
10 3

FAST DRAG-P,
0.5

10 4

FAST DRAG-L,
1.0

10 1

10 3

10 3
10 4
250
750 500 250 0

250 500 750

10 1
10 2
10 3
10 4
10 5
10 6
10 7
0

250 500 750

200

250 500 750

Baseband frequency (MHz)

(h)

100

750 500 250 0

I

(g)

fl, 1 fh, 1fl, 2

/(2 ) fl, 1 fh, 1fl, 2

100

Baseband frequency (MHz)

Q
/(2 )

0

f-state population pf

I

(d)

fl, 1 fh, 1fl, 2

/(2 )

Amplitude spectrum | IQ(f)|

(b) Cosine DRAG-L
In-phase spectrum | I(f)|

(a)

PRX QUANTUM 5, 030353 (2024)

1

FAST DRAG-P,

= 0.47

FAST DRAG-L,

= 0.92

Cosine DRAG-P,

= 0.57

Cosine DRAG-L,

= 1.0

2

3

4

5

6

Time t (ns)

Baseband frequency (MHz)

FIG. 1. Fourier anzatz spectrum tuning for fast low-leakage single-qubit gates. (a) Lowest energy levels of a transmon qubit with
a control pulse inducing state transfer (arrows), leakage errors (red), and ac Stark shift (dashed lines). (b) Envelopes of the in-phase
(I , solid) and quadrature (Q, dashed) components for a conventional cosine DRAG pulse (red here and later) and the proposed FAST
ˆ I (f )| of the in-phase envelope I
DRAG pulse (blue here and later) sampled (square markers) for our AWG. (c) Amplitude spectrum |
for the same pulses, with the blue regions illustrating the frequency intervals, across which the spectral energy of the in-phase envelope
ˆ IQ (f )| of the complex IQ envelope IQ for the same pulses using
is suppressed for the FAST DRAG pulse. (d) Amplitude spectrum |
DRAG to suppress the spectrum at the qubit anharmonicity α/(2π ) (dashed line). The inset shows a close up around α/(2π ). (e)
In-phase (I ) and quadrature (Q) envelopes for two variants of FAST DRAG with β ≈ 0.5 (light blue) resulting in minimal phase errors
ˆ IQ (f )| of the
(FAST DRAG-P) and β ≈ 1.0 (dark blue) resulting in minimal leakage (FAST DRAG-L). (f) Amplitude spectrum |
complex IQ envelope for the same pulses, with frequencies suppressed by DRAG (dashed lines), and frequencies corresponding to
maximal spectral energy density (dotted lines). (g) Simulated trajectory of the qubit state during a RX (π/2) gate for the same pulses,
with a virtual Z rotation (blue arrow) needed with the FAST DRAG-L pulse. (h) Simulated population leakage of a RX (π/2) gate
starting from |1⟩ for the same pulses together with cosine DRAG-P and cosine DRAG-L.

to the qubit frequency during idling, phase errors may
arise during gates due to an ac Stark shift of the qubit frequency δac (t) ≈ −λ22 I (t)2 /(4α) resulting from a coupling
between the higher energy states and the qubit drive, see
Fig. 1(a). Leakage errors during fast single-qubit gates are
primarily caused by the frequency spectrum of the control
pulse overlapping with leakage transitions. Thus, leakage
can be reduced by engineering ∫control pulses with a low
ˆ rf (f )| = | rf (t) exp(−i2π ft)dt| at
spectral amplitude |
undesired leakage transitions [15,16].
Conventionally, single-qubit control pulses are shaped
with DRAG to reduce either phase errors—which we
here refer to as DRAG-P—or both phase and leakage errors, which we refer to as DRAG-L [17,18].
For both of the DRAG variants, the quadrature enve˙ I (t)/α, where β denotes
lope is given by Q (t) = −β 
the DRAG coeﬃcient, and I (t) is the in-phase pulse
envelope, which can be, e.g., a Gaussian with I (t) =

exp[−(t − tp /2)2 /(2σ 2 )] − exp[−t2p /(8σ 2 )] or a raised
cosine with I (t) = [1 − cos(2π t/tp )]/2, as shown in
Fig. 1(b). In the DRAG-P variant, the DRAG coeﬃcient β
is tuned to cancel the ac Stark shift during the gate, which
for a transmon occurs at β ≈ 0.5 [24,46]. For suﬃciently
slow gates, the leakage errors can be ignored.
In the second variant, DRAG-L, the DRAG coeﬃcient
β is tuned such that the spectrum of the control pulse has a
zero crossing in the vicinity of the ef -transition frequency,
which occurs at β ≈ 1.0. This spectral suppression leads to
a lower leakage error, thus potentially enabling faster and
more accurate gates compared to DRAG-P. Despite lower
errors provided by DRAG-L, the DRAG-P variant has
been more commonly used in the literature due to easier
calibration and the dominance of phase errors over leakage
in early superconducting qubits [23,46,49–51]. Namely,
the choice of β ≈ 1.0 is not optimal for eliminating the
ac Stark shift, and thus phase errors need to be corrected

030353-3

## PDF page 4

ERIC HYYPPÄ et al.

PRX QUANTUM 5, 030353 (2024)

with another approach for the DRAG-L variant, such as
by detuning the drive frequency during the gate [17] or
by applying virtual Z rotations, i.e., updating the phase
of the microwave drive, before and after each gate [18].
If the phase errors are accounted for by tuning the drive
frequency during the gate, the optimal values of the drive
detuning and β are coupled, which complicates calibration.
On the other hand, virtual Z rotations are straightforward
to use with gate sets based on RX (π/2) rotations and
two-qubit gates commuting with σ̂z . However, the implementation of a RX (π ) gate requires two separate RX (π/2)
gates as the qubit state cannot be evolved from pole to pole
without applying virtual Z rotations at some point between
the poles. In principle, arbitrary-angle single-qubit gates
can be decomposed with at most two RX (π/2) gates and
three virtual Z rotations [18]. In this work, we decompose
the single-qubit Cliﬀord group using RX (π/2) gates as
explained in Sec. III and use virtual Z rotations to mitigate
phase errors of DRAG-L pulses.
B. Control pulses based on Fourier ansatz spectrum
tuning
For short microwave pulses or in the presence of multiple leakage transitions, it would be desirable to suppress the frequency spectrum across one or many frequency intervals of adjustable width, which is not possible
with conventional DRAG pulses suppressing the spectrum across a single narrow frequency range. Importantly,
the frequencies of the leakage transitions may shift during short gates due to ac Stark shifts or they may have
ﬁnite widths induced by dephasing [48]. Thus, it may be
beneﬁcial to suppress the spectrum of the control pulse
across wider frequency intervals around leakage transitions to reduce the leakage errors of fast gates beyond the
performance oﬀered by conventional DRAG pulses.
To overcome these issues, we present a novel pulseshaping method that parametrizes a control-pulse envelope
in terms of one or multiple conﬁgurable frequency intervals, across which the spectral energy is minimized to
reduce leakage. We call the method Fourier ansatz spectrum tuning since the spectral shaping is achieved using a
control-pulse envelope expressed as a Fourier cosine series
I (t) = A

N
∑

cn gn (t),

(2)

n=1

where gn (t) = [1 − cos(2π nt/tp )] (t/tp − 1/2) is the nth
basis function parametrized to ensure continuity of the
cosine series similar to Ref. [27]. Furthermore, A is the
overall amplitude, N is the number of cosine terms, {cn }
are the set of Fourier coeﬃcients, tp denotes the pulse duration, and (x) is the rectangular window function between
x ∈ [−1/2, 1/2], which sets the pulse envelope to 0 outside
of [0, tp ].

To solve for the coeﬃcients {cn }, we analytically minimize the spectral energy of the control envelope across
undesired frequency intervals as highlighted in Fig. 1(c),
while associating each interval with a weight controlling
the amount of suppression. The minimization problem can
be written as
min.

k
∑

∫ fh,j
wj

j =1

such that

N
∑

ˆ I (f )|2 df ,
|

(3)

fl,j

cn tp = θ ,

(4)

n=1

where k is the number of frequency intervals to suppress,
the hat denotes Fourier transform, wj is the weight associated with the j th undesired frequency interval [fl,j , fh,j ],
and the constraint ﬁxes the rotation angle of the gate. Here,
the frequencies are deﬁned in the baseband, and the spectrum of the up-converted control pulse is suppressed across
frequency intervals {fd ± [fl,j , fh,j ]} symmetrically located
around the drive frequency fd . Importantly, the quadratic
minimization problem with a linear constraint allows an
analytical solution for the coeﬃcient vector c ∈ RN ×1 for
a given set of frequency intervals and weights by inverting
the matrix equation

where

[
A + AT
bT

−b
0

∑k

∫ fh,j

Anm =
N ×1

j =1 wj

]
][ ] [
c
0
,
=
μ
θ/tp

fl,j

ĝn (f )ĝm∗ (f )df ,
N ×1

(5)
b = (1, . . . ,

1) ∈ R , 0 = (0, . . . , 0) ∈ R , and μ is the
Lagrangian multiplier. A more detailed derivation is provided in Appendix A. The FAST method can be viewed
as an extension of the Slepian [26], and it parametrizes
the control pulse in the frequency domain, while providing a mapping to the time-domain parameters {cn } using
Eq. (5). Alternatively, one can view N , {[fl,j , fh,j ]}, and {wj }
as hyperparameters controlling the pulse shape.
To implement fast, low-leakage single-qubit gates, we
combine the FAST method with DRAG by using FAST
to shape the in-phase envelope of the control pulse and
applying DRAG to obtain the quadrature component. The
resulting FAST DRAG pulse illustrated in Fig. 1(b) has
multiple beneﬁts compared to using DRAG with traditional pulse envelopes, such as the raised cosine. First, the
FAST DRAG pulse enables a stronger and wider spectral
suppression of the ef transition compared to conventional
approaches as shown in Fig. 1(d), which helps to mitigate
leakage to the f state. To achieve this, we apply the FAST
method to suppress the spectrum of the in-phase component across a frequency interval [fl,1 , fh,1 ] = [fl,ef , fh,ef ] ∋
|α|/(2π ), and use DRAG-L with β ≈ 1 to further suppress
the Fourier transform ˆ
IQ of the complex envelope that
T

030353-4

T

## PDF page 5

REDUCING LEAKAGE OF SINGLE-QUBIT GATES. . .

PRX QUANTUM 5, 030353 (2024)

ˆ IQ (f ) = [1 − 2πβf /α] × 
ˆ I ( f ).
is of the product form 
ˆ IQ (f ) around α/(2π ) then
The strong suppression of 
ˆ rf ( f )| around the
leads to a low spectral amplitude |
ef -transition frequency assuming ωd = ωq . In addition to
suppressing the signal around the ef transition, we use a
second frequency interval [fl,2 , fh,2 ] to reduce the spectral
energy above a given cutoﬀ frequency fc = fl,2 . This favorably reduces the bandwidth of the control pulse and often
indirectly lowers the peak amplitude, thus eﬀectively regularizing the pulse shape. As a further beneﬁt, it is relatively
straightforward to calibrate FAST DRAG pulses since the
parameters A, β, and {[fl,j , fh,j ]} are mostly decoupled,
and the locations of the suppressed frequency intervals
{[fl,j , fh,j ]} do not aﬀect the eﬀective drive frequency due
to a symmetric suppression of the spectrum [see Fig. 1(c)].
In this work, we select the hyperparameters {N , fl,ef ,
fh,ef , fc , wef = w1 /w2 } using physics-inspired heuristics
based on the measured anharmonicity α/(2π ) without
optimizing the hyperparameters. In Appendix F, we provide general heuristic guidelines for the hyperparameter
selection in systems with a single dominant leakage transition and discuss an extension to systems with multiple
leakage transitions important for simultaneous single-qubit
gates. The heuristic hyperparameter selection is possible because the leakage error is relatively robust against
moderate changes in the hyperparameters as discussed in
Sec. III and Appendix J. After the hyperparameter selection, the remaining single-qubit gate parameters can be
calibrated similarly to conventional DRAG pulses, which
renders the calibration of FAST DRAG pulses eﬃcient
and robust avoiding the challenges with closed-loop and
open-loop optimal control methods mentioned in Sec. I.
When using FAST DRAG, we study both of the abovedescribed DRAG-P and DRAG-L variants, the envelope
pulses and spectra of which are illustrated in Figs. 1(e)
and 1(f). In our calibration, we set the drive frequency
equal to the qubit frequency and use virtual Z rotations to
correct the phase errors caused by FAST DRAG-L pulses
as illustrated in Fig. 1(g). According to simulations, FAST
DRAG-L indeed achieves a lower simulated leakage error
for a 6-ns RX (π/2) gate compared to FAST DRAG-P and
the conventional cosine-based approaches, see Fig. 1(h).

derivatives to achieve a strong spectral suppression of the
dominant leakage transition, i.e., the ef transition instead
of suppressing multiple separate transitions as in Ref. [16].
We also propose an ansatz based on a simple cosine series
to ensure the continuity of the obtained control envelopes.
In analogy to FAST DRAG, our version of the higherderivative DRAG method (see Appendix B) minimizes the
spectrum of the in-phase envelope around the qubit anharmonicity while additionally using DRAG to obtain the
quadrature component and further suppressing the leakage.
In this work, we consider a special case of the HD DRAG
method containing derivatives up to the second order in I
and up to the third order in Q as

C. Control pulses based on higher-derivative (HD)
extension of DRAG
In this section, we present an alternative pulse-shaping
method for implementing fast, low-leakage single-qubit
gates by extending the theoretical ideas of Ref. [16], in
which a higher-derivative version of the DRAG method
was theoretically proposed to mitigate multiple leakage
transitions. In contrast to Ref. [16], we obtain Q (t) from
I (t) using standard DRAG, decoupling the parameters
of the in-phase and quadrature components, thus simplifying the calibration. Furthermore, we use the higher-order

I (t) = A[g(t) + β2 g̈(t)],
Q (t) = −

...
Aβ
[ġ(t) + β2 g (t)],
α

(6)
(7)

where g(t) denotes a basis envelope shape, and β2 is a
coeﬃcient tuned to minimize the spectrum at the anharmonicity. Note that the orders of the derivative are not
related to the order of DRAG as deﬁned in Ref. [24].
The Fourier transform of the complex envelope IQ
deﬁned by Eqs. (6) and (7) is consequently given
ˆ IQ (f ) = A × [1 − β2 (2π f )2 ] × [1 − 2πβf /α] × ĝ(f ),
by 
and the desired strong suppression at f = α/(2π ) is
obtained by setting β2 = 1/α 2 and β = 1 in line with
DRAG-L. As ˆ
IQ (f ) factors as a product, the parameters
β and β2 are decoupled simplifying calibration and allowing the use of DRAG-P to avoid phase errors if desired.
This is not the case if the third derivative term is left out
from Eq. (7) like in the Supplemental Material of Ref. [17],
where the minimization of leakage errors required a twodimensional sweep of {β, β2 } and phase errors could not
be avoided.
Importantly, the basis function g(t) and its three ﬁrst
derivatives should be continuous to ensure smooth control pulses, which we achieve by proposing the use of a
short cosine series given by g(t) = 1 − 4/3 cos(2π t/tp ) +
1/3 cos(4π t/tp ). The resulting envelopes of a thirdderivative HD DRAG pulse in comparison to lowerderivative versions of DRAG are shown in Fig. 2(a). After
expressing g(t) as a cosine series, this version of HD
DRAG is a special case of FAST DRAG with N = 2 and
a single suppressed frequency interval deﬁned by (fl,ef +
fh,ef )/2 = |α|/(2π ) and fh,ef − fl,ef → 0.
Thus, HD DRAG and FAST DRAG have many common advantages since they share similar design criteria.
Most importantly, HD DRAG enables strong spectral suppression of leakage transitions similarly to FAST DRAG
as illustrated in Fig. 2(b). Multiple leakage transitions can
also be suppressed with HD DRAG by introducing higherorder derivatives as explained in Appendix B. Despite
these similarities, there are also several key diﬀerences
between the two methods. HD DRAG has less parameters

030353-5

## PDF page 6

ERIC HYYPPÄ et al.

PRX QUANTUM 5, 030353 (2024)

(a)

(b)

FIG. 2. Higher-derivative DRAG. (a) In-phase (I , solid) and
quadrature (Q, dashed) envelopes of 6-ns HD DRAG pulses
based on diﬀerent maximum order of derivatives sampled
(square markers) for our AWG and compared to a pulse without DRAG. The pulse without DRAG sets Q = 0, the ﬁrstderivative DRAG pulse equals the conventional DRAG, the
second-derivative DRAG pulse sets I according to Eq. (6)
with Q = 0 similarly to the second-derivative DRAG solution
of Ref. [16] , and the third-derivative DRAG pulse is based
ˆ IQ (f )| of the
on Eqs. (6) and (7). (b) Amplitude spectrum |
complex IQ envelope IQ for the same pulses, with the qubit
anharmonicity α/(2π ) suppressed by DRAG shown with the
dashed vertical line and the inset presenting a close up around
α/(2π ).

than FAST DRAG, and the third-derivative HD DRAG
studied in this work introduces only a single additional
parameter β2 determined by the measured anharmonicity
α/(2π ). However, HD DRAG does not allow straightforward control over the pulse bandwidth, the average power,
or the exact strength and width of the spectral suppression unlike FAST DRAG, which oﬀers more ﬂexibility
for the pulse design. Hence, we foresee that the ﬂexibility of FAST DRAG is beneﬁcial especially in scenarios
with multiple leakage transitions, such as in simultaneous
single-qubit gates as brieﬂy discussed in Appendix F.
III. EXPERIMENTAL IMPLEMENTATION OF
FAST, LOW-LEAKAGE SINGLE-QUBIT GATES
To experimentally demonstrate the proposed pulseshaping methods, we benchmark the error and leakage per
gate for fast single-qubit gates implemented using FAST

DRAG and HD DRAG and compare the results to conventional pulse shapes, such as cosine DRAG. In this work,
we utilize a two-qubit test device with a design and fabrication similar to Ref. [4]. We focus on one of the two
ﬂux-tunable qubits that is operated at its sweet spot with a
frequency of 4.417 GHz, an anharmonicity of −212 MHz,
and average coherence times of about 37 and 22 μs for T1
and T2e (Hahn echo), respectively. We implement singlequbit rotations by sending microwave pulses to a charge
line coupled to the qubit through a targeted capacitance
of 0.12 fF. The microwave pulses are generated by upconverting intermediate-frequency pulses from a Zurich
Instruments HDAWG using an IQ mixer, and then propagated to the sample attached to the cold plate of a dilution
refrigerator (Bluefors LD400) through coaxial lines with
67-dB room-temperature attenuation at 4.5 GHz, see Fig. 6
in Appendix D. Since our gate decomposition is based on
RX (π/2) gates, it is suﬃcient to calibrate the pulse amplitude for a single rotation angle θ = π/2 allowing us to
neglect drive nonlinearities [52].
To implement single-qubit gates using FAST DRAG,
we suppress the spectrum of the in-phase component
across a baseband frequency interval of [fl,1 , fh,1 ] =
[fl,ef , fh,ef ] = [194, 214] MHz covering the qubit anharmonicity, while using another frequency interval of
[fl,2 , fh,2 ] = [450, 1000] MHz eﬀectively setting a cutoﬀ
frequency of fc = 450 MHz. In addition, we use a weight
ratio of wef = w1 /w2 = 5 (wef = 100) and set the number
of cosine terms to N = 4 (N = 5) for FAST DRAGL (DRAG-P). Here, a higher weight ratio is used for
FAST DRAG-P to enable suﬃcient spectral suppression
as the DRAG coeﬃcient is reserved for correcting phase
errors. The parameter values are chosen using physicsbased heuristics and prior simulations to provide a low
leakage rate across the studied gate durations tg ∈ [5, 20]
ns. See Appendix F for general heuristic guidelines on
the selection of these hyperparameters and Appendix J
for parameter sweeps demonstrating that the leakage error
stays low under moderate changes to the hyperparameter
values. For HD DRAG, we set β2 = 1/α 2 to minimize
the spectral energy density of the in-phase envelope at
the anharmonicity. In all of the results of this section, we
include a 0.41-ns delay between consecutive pulses as a
part of the reported gate duration tg , i.e., tg = tp + 0.41 ns,
and apply predistortion for the control-pulse envelopes as
discussed in more detail in Sec. III A and Appendix H.
To compare the error and leakage per gate for the
proposed and conventional pulse shapes, we calibrate
the single-qubit gate parameters A, β, ωd /(2π ) and the
virtual Z-rotation phase increment ϕZ using sequences
of error-ampliﬁcation experiments without any iterative
closed-loop optimization as explained in Appendix G, and
benchmark the resulting gate performance using randomized benchmarking (RB) [53–56] combined with threestate discrimination (see Appendix E) to further enable

030353-6

## PDF page 7

REDUCING LEAKAGE OF SINGLE-QUBIT GATES. . .

PRX QUANTUM 5, 030353 (2024)

leakage RB analysis [17,57]. The RB protocol enables estimating the average gate error by ﬁtting an exponential
model pg (NCl ) = Ag + Bg p NCl to the ground-state probability pg measured as a function of the Cliﬀord sequence
length NCl and then extracting the average error per Clifford as εCl = (1 − p)/2. Since we decompose the Cliﬀord
gates using on average Ng ≈ 2.21 native gates from the
gate set {I , RX (±π/2), RY (±π/2)} [56], we estimate the
error per gate as εg = εCl /Ng similarly to prior work using
an equivalent Cliﬀord decomposition [3,7,18]. We further
estimate the leakage error by ﬁtting an exponential model
N
pf (NCl ) = Af + Bf λ1 Cl to the f -state population and then
computing the leakage per gate as Lg = Af (1 − λ1 )/Ng .
From Fig. 3(a) showing the simulated (see Appendix C)
and experimental gate error as a function of gate duration,
we observe that cosine DRAG-L calibrated to minimize
leakage enables signiﬁcantly lower gate errors compared
to cosine DRAG-P minimizing phase errors. For cosine
DRAG-P, the gate error begins to increase already below a
gate duration of 14 ns, whereas the minimum gate error for
cosine DRAG-L reaches a value of (1.84 ± 0.06) × 10−4

at a gate duration of 10.8 ns. Importantly, the two novel
pulse shapes based on FAST DRAG-L and HD DRAGL enable a signiﬁcantly reduced gate error compared to
cosine DRAG-L for fast gates with tg ∈ [6, 9] ns. As illustrated in the close up of Fig. 3(b), FAST DRAG-L reaches
a minimum average gate error of (1.56 ± 0.07) × 10−4 at a
gate duration of 7.9 ns, clearly outperforming the conventional cosine DRAG-L pulse both in terms of gate error
and duration. For FAST DRAG-L, the gate error stays
at or below 2.0 × 10−4 down to a gate duration of 6.25
ns. To reduce the eﬀect of temporal ﬂuctuations of T1 in
Figs. 3(a)–3(c), the gate error was measured for cosine
DRAG-L and FAST DRAG-L in an interleaved fashion
and the full sweep was repeated on three separate days to
acquire more statistics. The measurements for HD DRAGL were conducted at a later date, during which T1 was
lower, explaining the slightly higher gate error compared
to FAST DRAG-L.
From the measured leakage error shown in Fig. 3(c), we
conﬁrm that the error for short gates is dominated by leakage. We also ﬁnd a good agreement between the measured

(a)
2

tg | |/(2 )

(b)

tg | |/(2 )
1

3

1.5

4

(c)

2.0

1

3 × 10 4
2 × 10 4

Leakage per gate Lg

)
g (×10

4 × 10 4

2.5

4

FAST DRAG-L
HD DRAG-L
Cosine DRAG-L
Cosine DRAG-P

6 × 10 4

3

4

2.0

1.5

FAST DRAG-L
HD DRAG-L
Cosine DRAG-L
Cosine DRAG-P

10 3

10 4

10 5

4

8

10

12

14

16

18

5

20

Gate duration: tg = 6.25 ns
FAST DRAG-L,
4
g = (1.8 ± 0.2) × 10

1.0
0.9

Cosine DRAG-L,
4
g = (7.3 ± 0.5) × 10

0.8
0.7
0.6
0.5
0.4
0.3

(e)
f-state probability pf

(d)

6

7

8

9

10

11

12

Gate duration: tg = 6.25 ns

0.5

FAST DRAG-L,
Lg = (1.8 ± 0.5) × 10 5

0.4

Cosine DRAG-L,
Lg = (4.1 ± 0.9) × 10 4

0.3
0.2
0.1
0.0

0

500

1000

1500

2000

2500

Number of Cliffords NCl

13

6

Gate duration tg (ns)

Gate duration tg (ns)

8

10

12

14

16

18

20

Gate duration tg (ns)

(f)
In-phase amplitude A (V)

6

Ground state probability pg

2

10 2

Gate error

Gate error

g

10 3

10

tg | |/(2 )

2.5

2.00

FAST DRAG-L
HD DRAG-L
Cosine DRAG-L

1.75
1.50
1.25
1.00
0.75
0.50
0.25
0.00

0

500

1000

1500

2000

2500

Number of Cliffords NCl

5.0

7.5 10.0 12.5 15.0 17.5 20.0 22.5

Gate duration tg (ns)

FIG. 3. Experimental benchmarking of fast low-leakage single-qubit gates. (a) Experimental error per gate εg from RB (markers)
and simulated error for the RX (π/2) gate (solid lines) as functions of the gate duration for FAST DRAG-L (dark blue here and later),
HD DRAG-L (dark gray here and later), cosine DRAG-L (dark red here and later) and cosine DRAG-P (light red here and later). The
error bars show 1σ uncertainty of the mean based on 4–10 RB experiments. (b) Close up to the gate error in panel (a) on the interval
tg ∈ [5, 13] ns. (c) Experimental leakage per gate Lg from leakage RB (markers) as a function of gate duration with simulated leakage
error for the RX (π/2) gate (solid lines). (d) Average ground-state probability (square markers) as a function of the number of Cliﬀord
gates in an RB experiment for FAST DRAG-L and cosine DRAG-L with tg = 6.25 ns. The dots show results for 25 random Cliﬀord
sequences, while the solid lines show exponential ﬁts estimating the error per gate εg . (e) Average f -state probability (square markers)
as a function of the number of Cliﬀord gates in the same RB experiment as in panel (d) with exponential ﬁts estimating the leakage
per gate Lg (solid lines). (f) Amplitude A of the in-phase envelope at the AWG output for the RX (π/2) gate as a function of the gate
duration.

030353-7

## PDF page 8

ERIC HYYPPÄ et al.

PRX QUANTUM 5, 030353 (2024)

leakage error and master equation simulations based on a
four-level Duﬃng oscillator model even though the simulations ignore any potential nonidealities of the control
electronics, such as ﬁnite bandwidth, dynamic range, or
sampling rate, see Appendix C for more details. Importantly, the experimental leakage per gate stays at or below
3.0 × 10−5 down to a gate duration of 6.25 ns for both
FAST DRAG-L and HD DRAG-L, providing up to a 20fold reduction in leakage compared to cosine DRAG-L.
However, the leakage error for FAST DRAG-L showcases
a shallow local maximum around tg |α|/(2π ) ≈ 2 since our
heuristics for the hyperparameter selection have been primarily designed to enable low leakage errors for fast gates
tg |α|/(2π ) ∈ [1, 2]. As shown in the example RB experiment of Figs. 3(d) and 3(e), FAST DRAG-L with a gate
duration of tg = 6.25 ns reduces the error and leakage
per gate by factors of 4 and 23, respectively, compared
to cosine DRAG-L with equivalent duration. The average
leakage per gate of (2.7 ± 0.3) × 10−5 and the corresponding leakage per Cliﬀord of (6 ± 1) × 10−5 obtained using
FAST DRAG-L at tg = 6.25 ns, i.e., tg |α|/(2π ) = 1.33,
are lower compared to the lowest value we have found in
the literature for such short pulses [7]. In Ref. [7], closedloop optimization of a piecewise constant RX (π/2) pulse
resulted in an order of magnitude higher leakage per Clifford of 4.4 × 10−4 using a transmon with an anharmonity
of −315 MHz and a gate duration of 4.16 ns corresponding to a normalized gate duration of tg |α|/(2π ) = 1.31
practically equivalent to our work.
In comparison to conventional cosine DRAG-L pulses,
the novel pulse shapes do not require any higher
peak amplitude, see Fig. 3(f). In contrast, the required

P

P

P

P
12

L

P

10

L
L

D
RA
G

H
D

pi

an

D
RA
G
Sl
e

Co

si

ne

n
ia

RB error

Limit from T1 and T2e

10 4

Purity RB error
Leakage error

10 5
0

5

10

15

20

Time from calibration (h)

(c)
80
70
60

FAST DRAG-L: tg = 6.67 ns
RB error: (1.60 ± 0.01) × 10 4
PRB error: (1.14 ± 0.02) × 10 4
Leakage: (2.58 ± 0.03) × 10 5

50
40
30
20
10
0
10 5

10 4

Magnitude of error

G

au
ss

D
RA
G

6

FA
ST

L

D
RA
G

L

8

FAST DRAG-L: tg = 6.67 ns

Number of observations

14

Magnitude of error

(b)

D
RA
G

Min. gate duration
with Lg < 5 × 10 5 (ns)

(a)

amplitudes of FAST DRAG-L and HD DRAG-L are
signiﬁcantly lower for gate durations below 9 ns due to
a faster increase of voltage at the beginning and end of the
pulse [see Figs. 1(b) and 2(a)]. For FAST DRAG-L and
HD DRAG-L, the nonmonotonic increase of peak amplitude when reducing gate duration is explained by the inphase envelope changing from having a single maximum
to having two maxima.
To compare the gate performance of the novel pulse
shapes against other conventional pulses beyond cosine
DRAG, we further experimentally benchmark the leakage rate for DRAG pulses based on Gaussian and Slepian
in-phase envelopes. For the Gaussian envelope, we use
tp = 5σ ns and subtract the discontinuity similar to, e.g.,
Ref. [24]. To construct the Slepian envelope, we use
FAST pulse shaping with an eﬀective cutoﬀ frequency of
185 MHz < α/(2π ). Further results obtained for Gaussian
and Slepian envelopes with diﬀerent parameter choices
are provided in Appendixes I and J. Based on measurements of leakage per gate as a function of gate duration
in Appendix I, we estimate an experimental speed limit
for each of the control pulses by determining the shortest gate duration with a leakage per gate below 5 × 10−5 .
As shown in Fig. 4(a), FAST DRAG-L and HD DRAG-L
enable the fastest low-leakage gates, reaching the leakage threshold at a gate duration of approximately 6 ns.
The corresponding speed limits are 7.5, 8.7, and 10.4
ns for Slepian DRAG-L, cosine DRAG-L, and Gaussian
DRAG-L. When calibrating DRAG to minimize phase
errors, the corresponding speed limit is 12–13 ns for all
the other pulses than FAST DRAG-P, for which the leakage rate stays below the threshold down to a gate duration

FIG. 4. Comparison of gate speed for diﬀerent pulse shapes and temporal stability of FAST DRAG gates. (a) Shortest gate duration
with an experimental leakage error below Lg < 5 × 10−5 for conventional and proposed pulse shapes calibrated using DRAG-P (light
color) or DRAG-L (dark color). For Gaussian DRAG, we use σ = tp /5 and subtract away the discontinuity. For Slepian DRAG, we
minimize the spectral energy above fc = 185 MHz. See also Fig. 12(a) for the duration-dependent leakage error of each pulse and
Fig. 12(b) for an illustration of the pulse shapes, respectively. (b) Experimental error per gate εg from RB (blue triangles), incoherent
error per gate εg,inc from purity RB (gray circles), and leakage per gate Lg from leakage RB (red squares) as a function of time since
the calibration of a RX (π/2) gate using a FAST DRAG-L pulse with tg = 6.67 ns. The markers and error bars are based on the mean
and the standard error of mean estimated from three (leakage) RB and two purity RB experiments conducted at each point of time. The
dashed gray line shows the coherence limit based on T1 and T2e . (c) Histograms of RB gate error, purity RB error, and leakage error
based on data in panel (b).

030353-8

## PDF page 9

REDUCING LEAKAGE OF SINGLE-QUBIT GATES. . .

PRX QUANTUM 5, 030353 (2024)

of 9.6 ns thanks to a strong spectral suppression around the
ef transition provided by FAST pulse shaping.
We further study the temporal stability of gate errors and
leakage for FAST DRAG-L pulses by calibrating a 6.67-ns
RX (π/2) gate and subsequently conducting repeated measurements of RB, leakage RB, and purity RB over a time
period of 23 hours. The purity RB experiment incorporates state-tomography characterization after each random
Cliﬀord sequence to measure the average purity of the
ﬁnal state as a function of the Cliﬀord sequence length,
which enables estimating
the incoherent error per gate as
√
εg,inc = 1/2 × (1 − u)/Ng [58,59]. Here, u is the unitarity obtained by ﬁtting an exponential model P̄norm (NCl ) =
A′ uNCl + B′ to the averaged normalized purity computed
for each sequence as Pnorm = 2tr(ρ̂ 2 ) − 1 using the estimated density operator ρ̂. As illustrated in Fig. 4(b), the
total error from RB, the incoherent error from purity RB
and the leakage per gate remain practically constant over
the studied time period, demonstrating that the FAST
DRAG pulses enable the implementation of stable gates
in our setup. As shown in the histograms of Fig. 4(c),
the mean values of the total gate error, incoherent error
and leakage per gate are (1.60 ± 0.01) × 10−4 , (1.14 ±
0.01) × 10−4 , and (2.58 ± 0.03) × 10−5 suggesting that
other sources contribute to the total gate error in addition
to incoherent errors and leakage. We attribute the remaining errors to non-Markovian coherent errors resulting from
microwave-pulse distortions as discussed in more detail in
the following Sec. III A.

from gate-set tomography [60,61], whereas the characterization of the full-process tensor [62–64] capturing nonMarkovian errors would be time consuming. Here, we
instead characterize the I and C distortions using straightforward error-ampliﬁcation experiments, which are almost
exclusively sensitive to only one type of distortion.
To characterize C distortions, we use a circuit consisting of repeated (RX (π ), RX (−π )) pairs as suggested in
Ref. [45] and append the sequence with a ﬁnal RY (π/2)
gate to make the sequence linearly sensitive to phase
errors, see Fig. 5(a). As a result, the sequence is eﬃcient
in detecting C distortions causing phase errors, the magnitude of which varies depending on the delay td between
pulses. For the characterization of I distortions, we propose a circuit consisting of repeated (RX (π ), RY+ϕ (π ))
pairs prepended with a RX (π/2) gate and appended with a
RY (π/2) gate to make the measured excited-state probability linearly sensitive to distortion-induced coherent errors.
In this experiment, each pair of (RX (π ), RY (π )) gates
would ideally result in a Z rotation. In the presence of
I distortions, the tail of the previous pulse tilts the rotation axis of the following pulse, resulting in a change of
the relative angle between the axes of RX (π ) and RY (π ),
as shown in Fig. 5(b). This further causes the resulting
Z rotation to have an over-rotation that can be ampliﬁed with repeated gates. Other common types of errors,
such as amplitude miscalibration or phase errors, do not
result in such an over-rotation to ﬁrst order, but instead
change the resulting rotation axis and thus do not contribute to the error ampliﬁcation. We sweep the relative
phase between RX (π ) and RY+ϕ (π ) through ϕ in order
to determine an axis-shift angle ϕs leading to a vanishing over-rotation angle of the composite Z rotation, thus
indicating cancelation of the axis tilt caused by the pulse
tails as schematically illustrated in Fig. 5(b). Therefore, we
regard the axis shift ϕs as a measure of the magnitude of
the I distortions. Furthermore, we accompany the I- and Cdistortion characterization experiments with a sweep of the
delay between pulses to characterize the temporal proﬁle
of the pulse distortions.
We mitigate I distortions by separately predistorting the
I and Q control-pulse envelopes using an exponential inﬁnite impulse response (IIR) inverse ﬁlter in analogy to
the predistortion of ﬂux pulses [5,65,66], see Fig. 5(c)
and Appendix H for more details. This choice of the
ﬁlter function is motivated by the observation that the
axis shift ϕs measured from the I-distortion characterization decays approximately exponentially as a function of
the delay between pulses, as shown in Fig. 5(d). Using
calibration measurements explained in Appendix H, we
obtain a time constant τ1 = 8 ns and amplitude coeﬃcient a1 = −0.028 as the predistortion parameters used
for both I and Q envelopes. When using predistortion,
we observe that the exponential dependence is removed in
the I-distortion characterization, resulting in a signiﬁcantly

A. Characterization and precompensation of
control-pulse distortions
As mentioned in the previous section, coherent errors
related to microwave-pulse distortions appear to prevent us from implementing coherence-limited sub-10-ns
gates. Here, we discuss experimental evidence of such
pulse distortions using the qubit as a sensor and present
our approach for predistorting control-pulse envelopes to
improve gate ﬁdelity. We classify the pulse distortions into
two types based on their eﬀect on the pulse envelopes
similarly to Ref. [45], see Fig. 5(a). The ﬁrst type of
distortion, named intraquadrature distortion (I distortion),
corresponds to a distortion of the in-phase (quadrature)
envelope resulting from a pulse in the in-phase (quadrature) envelope. The second type of distortion, named
cross-quadrature distortion (C distortion), refers to a distortion of the quadrature (in-phase) envelope caused by a
pulse in the in-phase (quadrature) envelope. Both types of
distortions result in coherent errors, the eﬀects of which
depend on previous gates and the delay td between pulses
in a way that cannot be corrected by optimizing the
sample amplitudes during the gate, e.g., as in Ref. [7].
As such errors are non-Markovian, the gates cannot be
described by ﬁxed Pauli-transfer matrices extracted, e.g.,

030353-9

## PDF page 10

ERIC HYYPPÄ et al.
I

I

intra-quadrature
distortion
(I-distortion)

1.0

Possible sweep variables: Nr, delay,
Nr repeats

I-distortion
characterization

=0 rad

pe(Nr)

(a)

PRX QUANTUM 5, 030353 (2024)

delay

Q

Q

C-distortion
characterization

Nr repeats

1.0

delay

pe(Nr)

0.0

cross-quadrature
distortion
(C-distortion)

At qubit

At AWG

Delay td

0.0

I

0.0

s (deg.)

I

Q

Q

Target

Predistorted

Delay td

Pulse duration: tp = 9.17 ns

(d)

(c)

0.2
FAST DRAG-P,
no predistortion
FAST DRAG-P,
with predistortion

0.4

Axis shift

(b)

0.6

Nr repeats

0.8

td

1.0
0

)
4
g (×10

2.0
1.5
1.0
0.5

3.0

FAST DRAG-L
no predistortion

2.5

2.0

1.5

15

20

25

6

8

10

12

14

16

Gate duration tg (ns)

18

20

5

6

7

8

9

10

Gate duration tg (ns)

11

12

35

0.9

175

0.8

150
0.7

125
0.6

100

0.5

75
50

Nr repeats

25

td

0.4
0.3
0.2

0

0.0

30

Pulse duration: tp = 9.17 ns

200

FAST DRAG-L
with predistortion

10

Excited state probability pe

3.5
FAST DRAG-L with predistortion
FAST DRAG-L no predistortion
FAST DRAG-P with predistortion
FAST DRAG-P no predistortion

Number of repeats Nr

2.5

5

Delay between pulses td (ns)

(g)

(f)

Gate error

Absolute axis shift | s| (deg.)

(e)

0.1

0

2

4

6

8

10

Delay between pulses td (ns)

FIG. 5. Characterization and mitigation of microwave-pulse temporal distortions. (a) Microwave-pulse distortions are classiﬁed into
intraquadrature distortions (I distortion, red) and cross-quadrature distortions (C distortion, blue). We experimentally characterize I
and C distortions using diﬀerent error-amplifying circuits with the measured excited-state probability pe being mainly sensitive to one
type of distortion and depending on the delay td between consecutive pulses. (b) Eﬀective rotation axes (long arrows) of consecutive
RX (π ) (red) and RY+ϕ (π ) (blue) gates in I-distortion characterization when envelope tails (short arrows) due to I distortions are present.
The axis tilt ϕs caused by the envelope tails (left) can be canceled by shifting the phase of the RY+ϕ (π ) gate with ϕ = ϕs (right). (c)
Schematic of envelope predistortion using an exponential IIR inverse ﬁlter to mitigate I distortions for the I (red) and Q envelopes
(blue). (d) Axis shift ϕs measured from I-distortion characterization as a function of the delay td between consecutive gates for a 9.17ns-long FAST DRAG-P pulse with (light blue) and without (light red) predistortion. The error bars represent 1σ uncertainty, and the
solid line shows an exponential ﬁt to the data without predistortion. (e) Absolute axis shift |ϕs | as a function of gate duration for FAST
DRAG-L (dark color) and FAST DRAG-P (light color) with (blue) and without (red) envelope predistortion when using the default
delay of td = 0.41 ns between pulses. (f) Error per gate εg from RB (markers) and simulated error of RX (π/2) (solid line) as functions
of the gate duration for FAST DRAG-L with (blue) and without (red) predistortion. (g) Excited-state probability as a function of delay
td between consecutive pulses and the number of repeated (RX (π ), RX (−π )) sequences in C-distortion characterization using FAST
DRAG-P with envelope predistortion and tp = 9.17 ns.

smaller axis shift as shown in Fig. 5(d), providing support
for the used predistortion model. In Fig 5(e), we further
show that the predistortion signiﬁcantly reduces the axis
shift ϕs for FAST DRAG-P and FAST DRAG-L pulses
across gate durations tg ∈ [6, 20] ns. For FAST DRAG-L,
the remaining axis shift is higher since the virtual Z rotations preceding each pulse eﬀectively convert part of the
noncorrected C distortion into I distortion. In Fig. 5(f), we
compare the RB gate error obtained using FAST DRAG-L

pulses with and without predistortion and demonstrate that
the gate error is systematically reduced by (2–6) × 10−5
across the tested gate durations between 6 and 11 ns.
When applying the predistortion, we still ﬁnd a small
coherent error as discussed above and illustrated in
Fig. 4(c). We attribute this remaining coherent error to
C distortions that we were not able to correct in this
work, see Appendix H. To verify this conclusion, we conduct a C-distortion characterization experiment for varying

030353-10

## PDF page 11

REDUCING LEAKAGE OF SINGLE-QUBIT GATES. . .

PRX QUANTUM 5, 030353 (2024)

pulse-to-pulse delays using a FAST DRAG-P pulse with
tp = 9.17 ns. As shown in Fig. 5(g), the gates indeed suffer from delay-dependent phase errors that we attribute to
remaining C distortions. Note that we do not use the measurement scheme proposed in Ref. [45] to obtain the ﬁnite
impulse response ﬁlter corresponding to the C distortions
since the assumption of vanishing gate duration does not
hold well for a transmon-based system unlike for the ﬂux
qubit studied in Ref. [45].

gates in systems with high coherence. Namely, the proposed methods provide good initial parameter guesses and
a natural basis for the optimization, potentially reducing
the required number of iterations and wall clock time
signiﬁcantly.
We also demonstrate that non-Markovian coherent
errors arising from microwave-pulse distortions contribute
to the gate error of sub-10-ns single-qubit gates. Hence,
we develop and demonstrate methods to observe errors
caused by such distortions and subsequently apply controlpulse predistortion to reduce gate errors. However, our
approach did not mitigate the pulse distortions completely,
and further work is needed to develop methods for more
precise characterization of such distortions using the qubit
as a sensor to enable improved predistortion of the control
pulses. All in all, we expect that our work contributes to
improving the ﬁdelity and speed of quantum logic gates,
bringing the advent of useful quantum computation one
step closer.

IV. OUTLOOK
In this work, we propose and demonstrate two new
methods for shaping the frequency spectrum of singlequbit control pulses, enabling stronger spectral suppression
of leakage transitions and thus lower leakage errors for
fast logic gates compared to state-of-the-art approaches.
Using the proposed methods, we calibrate RX (π/2) gates
and experimentally demonstrate a gate error of (1.56 ±
0.07) × 10−4 at a gate duration of 7.9 ns without experimental closed-loop optimization, outperforming conventional approaches both in terms of gate error and speed.
The developed pulse-shaping methods are not only limited to superconducting qubits or to the suppression of the
ef transition of a single transmon qubit, but they may also
be applied to other platforms or to suppress multiple leakage transitions or other undesired transitions. Thus, the
proposed methods may improve simultaneous single-qubit
gates on quantum processing units of any type that suffer from frequency-crowding issues. This may be achieved
by minimizing the spectral energy of the control pulses
across crosstalk-induced transitions in addition to the ef
transition, while using a cutoﬀ frequency to regularize the
pulse shape. Even though HD DRAG and FAST DRAG
provide an approximately equal leakage error in the studied single-qubit system, we foresee that the ﬂexibility of
FAST DRAG may be beneﬁcial to appropriately adjust
the relative strength and width of spectral suppression in
the case of multiple undesired transitions as discussed in
Appendix F.
The proposed methods may also ﬁnd applications in
the optimization of two-qubit gate control pulses based on
microwave pulses [6,67] or ﬂux pulses [4,5]. As an example, architectures based on the cross-resonance eﬀect [29,
68,69] or the recently demonstrated ﬂuxonium-transmonﬂuxonium scheme [6] rely on microwave-activated twoqubit gates that suﬀer from frequency crowding. Hence,
the analytical pulse-shaping methods developed in this
work may help to suppress undesired transitions improving
the microwave-activated two-qubit gates, and potentially
speeding up the calibration compared to, e.g., the reinforcement learning approach employed in Ref. [6]. Furthermore, we expect that combining the proposed methods
with experimental closed-loop optimization may result in
further improvements to the ﬁdelity of fast quantum logic

Data supporting the ﬁndings of this article are available
at [70]. The dataset in Zenodo also includes a Jupyter notebook that provides Python helper functions for evaluating
and plotting the FAST DRAG and HD DRAG pulse shapes
deﬁned by Eqs. (2) and (5)–(7).

ACKNOWLEDGMENTS
We thank the whole staﬀ at IQM Quantum Computers for their support. In particular, we acknowledge Lucas
Ortega, Roope Kokkoniemi, and Matthew Sarsby for supporting the maintenance and improvement of the experimental setup; Tuure Orell, Jani Tuorila, and Hao Hsu
for simulation-related discussions; and Attila Geresdi on
discussions related to single-qubit gates. E.H. thanks the
Finnish Foundation for Technology Promotion (Grant No.
9230) and Jenny and Antti Wihuri Foundation (Grant No.
00230115) for funding. We acknowledge the provision
of facilities and technical support by Aalto University at
OtaNano—Micronova Nanofabrication Center and LTL
infrastructure.
All authors declare that IQM has ﬁled a patent application regarding the new methods for shaping the frequency
spectrum of control pulses having the following inventors:
Eric Hyyppä, Antti Vepsäläinen, and Johannes Heinsoo.
E.H. developed the concept and theory for FAST DRAG
and HD DRAG. A.V., E.H., and J.H. planned the simulations and the experiments. E.H. conducted the simulations
with support from M.P. and S.I. E.H. conducted the experiments and analyzed the measurement data with support
from C.F.C., F.M., J.L., and S.O. on measurement code,
F.M. on experiment setup, and B.T. on experiment software. A.L. and C.O.-K designed the sample. W.L. fabricated the device. The paper was written by E.H. with

030353-11

## PDF page 12

ERIC HYYPPÄ et al.

PRX QUANTUM 5, 030353 (2024)

support from A.V., and J.H. All authors commented on the
paper. A.V., and J.H. supervised the work.
APPENDIX A: DERIVATION OF FAST PULSE
SHAPES
Here, we provide a more detailed derivation for Eq. (5)
that allows us to solve the coeﬃcients {cn } of a FAST pulse
from a given set of weights and frequency intervals to be
suppressed. At the end of this section, we also brieﬂy discuss some useful properties of the pulse-shaping method in
more detail compared to the main text.
In the FAST method, the control-pulse envelope I (t)
with a duration tp is expressed as a ﬁnite sum of basis
functions
I (t) = A ×

N
∑

cn gn (t),

measured with respect to the center drive frequency, and
the spectrum of the modulated microwave control pulse
will consequently be minimized across frequency intervals fd ± [fl,j , fh,j ] symmetrically located around the central
drive frequency fd .
By expanding the control envelope I (t) using Eq. (A1),
the optimization problem in Eq. (A3) can be written in a
matrix form as
k
∑

=

k
∑

cn [1 − cos(2π nt/tp )] (t/tp − 1/2),

=

j =1

s.t.

N
∑

wj

ˆ I (f )|2 df ,
|

(A3)

fl,j

cn × tp = θ,

(A4)

n=1

m=1

j =1

∑

fl,j

cn cm Anm

n,m

= cT Ac,

(A5)

where c ∈ RN ×1 is a column vector containing the coefﬁcients cn as its elements, and A ∈ CN ×N is a hermitian
∫f
∑
matrix with elements Anm = kj=1 wj fl,jh,j ĝn (f )ĝm∗ (f )df .
Here, the Fourier transform ĝn (f ) of the nth basis function
can be analytically solved as
∫ ∞
ĝn (f ) =
gn (t)e−i2π tf dt
(A6)
−∞

=

where (x) is the rectangular window function between
x ∈ [−1/2, 1/2], which sets the pulse envelope to 0 outside
of [0, tp ].
The coeﬃcients {cn } are obtained by minimizing the
spectral energy of the pulse across undesired frequency
intervals corresponding to, e.g., leakage transitions. We
solve for the coeﬃcients {cn } by employing the following
linearly constrained quadratic optimization problem:
minimize

fl,j

)( N
)
∑
∗
cn ĝn (f )
cm ĝm (f ) df

⎛
⎞
∫ fh,j
k
∑
∑
=
cn cm ⎝
wj
ĝn (f )ĝm∗ (f )df ⎠

(A2)

∫ fh,j

wj

n,m

n=1

k
∑

∫ fh,j (∑
N

j =1

(A1)

where N is the number of basis functions, {gn (t)} is the
set of basis functions deﬁned to be 0 outside of the interval [0, tp ], and {cn } are the corresponding coeﬃcients. In
this work, we have chosen the sum of basis functions to
represent a Fourier cosine series parametrized such that
the control envelope I : R → R and its derivative have
no discontinuities, thus reducing slow sinc-type decay of
the pulse spectrum. Thus, we write the control envelope
I (t) as
I (t) = A ×

|ˆ
I (f )|2 df

fl,j

j =1

n=1

N
∑

∫ fh,j
wj

∫ tp

[1 − cos(2π nt/tp )]e−i2π tf dt

0

(

= tp e−iπ tp f sinc(π tp f )
1
− eiπ(n/tp −f )tp sinc[π(n/tp − f )tp ]
2
)
1 −iπ(n/tp +f )tp
− e
sinc[π(n/tp + f )tp ] , (A7)
2
where sinc(x) = sin(x)/x. Importantly, the analytic form
of ĝn (f ) ensures eﬃcient computation of the matrix elements Anm via numerical integration. Using Eq. (A5), the
optimization problem can then be rewritten in a matrix
form as

n=1

where wj represents the weight, i.e., importance, for the
j th frequency interval [fl,j , fh,j ], k is the number of the frequency intervals to suppress, and θ is the desired rotation
angle that can be chosen arbitrarily since the amplitude
parameter A is at any rate adjusted in experimental calibration. Note that the frequencies are in the baseband, i.e.,

cT Ac

(A8)

such that c b − θ/tp = 0,

(A9)

minimize

T

where we have further deﬁned b = (1, . . . , 1)T ∈ RN ×1 .
Now, the minimization problem can be analytically
solved using the method of Lagrangian multipliers. The

030353-12

## PDF page 13

REDUCING LEAKAGE OF SINGLE-QUBIT GATES. . .

PRX QUANTUM 5, 030353 (2024)

Lagrangian corresponding to the optimization problem
reads L(c, μ) = cT Ac − μ(cT b − θ/tp ), and the optimality
conditions are thus given by

essentially approximating a square pulse with the given
number of harmonic terms.
As a further beneﬁt of the FAST method, the most
important parameters (A, β, {[fl,j , fh,j ]}) of a single-qubit
˙ I (t)/α sin(ωd t)
control pulse rf (t) = I (t) cos(ωd t) − β 
are practically independent. This means that the rotation
angle of the gate is mainly controlled by the amplitude
parameter A, whereas β and {[fl,j , fh,j ]} independently control which parts of the frequency spectrum are suppressed
since the Fourier transform of the complex envelope IQ
ˆ IQ (f ) = [1 − 2πβf /α] ×
is given by the product form 
ˆ
I (f ). The baseband frequency intervals {[fl,j , fh,j ]} are
symmetrically suppressed around the center drive frequency, and have thus no eﬀect on the resulting eﬀective
drive frequency (unlike the DRAG parameter β).
Finally, we note that other choices for the basis functions
{gn (t)} beyond the cosine series are also possible and the
coeﬃcients {cn } of the basis functions can still be solved
using Eq. (A12). The expression for ĝn (f ) needs to be
analytically evaluated for the new set of basis functions
or numerically computed across the undesired frequency
intervals, which may, however, increase the computational
cost of solving {cn }.

∇c L = (A + AT )c − μb = 0

(A10)

∇μ L = cT b − θ/tp = 0.

(A11)

These two conditions can be combined into a single matrix
equation
Ãc̃ = b̃,

(A12)

where c̃ = (cT , μ)T is the coeﬃcient vector extended by the
Lagrangian multiplier, b̃ = (0T , θ/tp )T ∈ R(N +1)×1 with
0 = (0, . . . , 0)T ∈ RN ×1 , and the matrix Ã ∈ R(N +1)×(N +1)
is deﬁned as
(
)
A + AT −b
Ã =
.
(A13)
bT
0
This concludes the derivation of Eq. (5).
Subsequently, we brieﬂy discuss some useful properties
of the FAST method. See also Appendix F for guidelines on the selection of the hyperparameters. First, we
emphasize that the FAST method enables the construction
of pulses with a given duration. Thus, the method diﬀers
from ﬁlter-based solutions, such as the use of band-pass
or low-pass ﬁlters [18], which may ﬁlter out speciﬁc frequency intervals from the spectrum of a control pulse but
which also result in pulse distortions, potentially signiﬁcantly changing the pulse duration. As already discussed
in Sec. II B, the FAST method enables one to control the
width and strength of the spectral suppression. Thus, a
combination of FAST and DRAG may be helpful to reach
a lower leakage error for fast logic gates compared to
conventional DRAG pulses since the spectral suppression
provided by conventional DRAG pulses may not be suﬃcient, e.g., in the presence of multiple leakage transitions
or frequency shifts occurring during the gate. However,
one should bear in mind that the suppression of several
frequency intervals using the FAST method may lead to
increased spectral power at nonsuppressed frequencies.
As another important property of the FAST method, it
is possible to limit the bandwidth of the pulse by suppressing the spectrum across an additional frequency interval
ranging from a given cutoﬀ frequency fc up to some high
frequency. This not only helps to abide by the bandwidth
limitations of the control electronics, but may also help
to reduce the peak amplitude of the pulse as observed in
Fig. 3(f) avoiding compression of analog electronics and
heatload to the cryostat. Reducing the cutoﬀ frequency
eﬀectively favors pulses with a lower average power. In
the limit of suppressing the spectrum across [fl,1 , fh,1 ] =
[0, ∞], one obtains the minimum-energy pulse for realizing a rotation with the given angle in the given time,

APPENDIX B: HIGHER-DERIVATIVE DRAG
In this section, we provide a more general formulation
of the HD DRAG framework beyond the special case containing derivatives up to the third order as discussed in
Sec. II C. Using the ﬁrst 2K + 1 derivatives for the inphase and quadrature envelopes, the envelope functions
can be written as
I (t) = A

[∑
K

β2n g

(2n)

]
(t) ,

(B1)

n=0

β
˙ I,
Q (t) = − 
α

(B2)

where g(t) is a basis envelope, and {β2n }2K
n=0 are coeﬃcients
for the even-order derivatives with β0 = 1. To avoid leakage transitions or other harmful frequencies, we require
ˆ I (f ) to equal zero at K diﬀerent
the Fourier transform 
baseband frequencies {fj }Kj=1
ˆ I (fj ) = 0,


j = 1, . . . , K.

(B3)

Using the relation F [s(n) ](f ) = (i2π f )n ŝ(f ) with F [·]
denoting Fourier transform, we simplify the expression of
ˆ I (f ) as
the Fourier transform 

030353-13

ˆ I (f ) = Aĝ(f )


[ K
∑
n=0

]
β2n (−1)n (2π f )2n .

(B4)

## PDF page 14

ERIC HYYPPÄ et al.

PRX QUANTUM 5, 030353 (2024)

Thus, the condition in Eq. (B3) reduces to the following
system of linear equations
K
∑

β2n (−1)n (2π fj )2n = 0,

j = 1, . . . , K,

(B5)

n=0

from which the coeﬃcients {β2n }Kn=1 can be straightforwardly solved assuming that the suppressed frequencies
{fj }Kj=1 are distinct. However, it is also possible to suppress the spectrum more heavily around a single baseband
frequency, such as α/(2π ), for K > 1 by engineering the
polynomial in Eq. (B4) to have a Kth-order zero at α/(2π ).
ˆ I being a fourth-order polynomial in f ,
For K = 2 with 
this can be achieved by setting β2 = 2/α 2 and β4 = 1/α 4 .
The formulation of HD DRAG in Eqs. (B1) and (B2)
decouples the in-phase parameters {β2n }Kn=1 and associated
suppressed frequencies {fj }Kj=1 from the DRAG coeﬃcient
β, which simpliﬁes the calibration experiments especially
for the case of K = 1 considered in Sec. II C and also
enables one to tune β to avoid phase errors if desired
(see Sec. II A). By solving both {β2n }Kn=1 and β to suppress a given undesired baseband frequency fs , a stronger
and wider spectral suppression can be obtained than with
conventional DRAG pulses. Furthermore, the in-phase
parameters {β2n }Kn=1 do not aﬀect the eﬀective drive frequency (unlike β), which can be beneﬁcial for calibration
experiments in some scenarios.
As discussed in Sec. II C, the basis function g(t) should
be chosen with care to ensure continuity and avoid slow
decay of the Fourier transform as a function of frequency.
One possibility is to use a cosine series
g(t) =

K+1
∑

dk [1 − cos(2π kt/tp )],

(B6)

k=1

where tp is the pulse duration and {dk }K+1
k=1 denote
the coeﬃcients to be solved, such that the continuity requirements g(0) = g (1) (0) = · · · = g (2K+1) (0) =
g(tp ) = g (1) (tp ) = · · · = g (2K+1) (tp ) = 0 are satisﬁed. Due
to the form of g(t) in Eq. (B6) the odd derivatives are automatically zero, whereas the conditions for the even derivatives can be met by solving {dk }K+1
k=1 from the following
linear system of equations:
K+1
∑

dk (−1)n+1 k 2n = 0,

n = 1, . . . , K,

(B7)

k=1
K+1
∑

dk = 1,

(B8)

k=1

where the latter equation simply normalizes the sum of
the coeﬃcients to a value that can be set arbitrarily.

Even though this approach ensures the smoothness of the
control pulse and was found to enable fast, low-leakage
single-qubit gates with up to 2K + 1 = 3 derivatives, the
higher-order solutions may lead to rapidly oscillating envelope functions, the bandwidth and peak amplitude of which
cannot be regularized unlike with the proposed FAST
method.
APPENDIX C: SINGLE-QUBIT GATE
SIMULATIONS
In this section, we describe the methods used to simulate
the gate error and leakage as illustrated in Figs. 3, 8, 12–15.
For the simulations, we model the bare transmon using an
anharmonic Duﬃng oscillator Hamiltonian as
Hq /ℏ = ωq a† a +

α † †
a a aa,
2

(C1)

where ωq /(2π ) ≈ 4.417 GHz and α/(2π ) ≈ −212 MHz
are the qubit frequency and anharmonicity, and a† and a are
the raising and lowering operators of a harmonic oscillator.
The capacitively coupled microwave drive is modeled by
the following drive term:
(
)
Hd /ℏ = rf (t) a† + a ,

(C2)

where the drive signal is of the form rf (t) =
I (t) cos(ωd t + ϕ) + Q (t) sin(ωd t + ϕ) with ωd /(2π )
being the drive frequency and ϕ describing the accumulated phase due to virtual Z rotations.
For the simulations, we transform to a frame rotating
at the qubit frequency using the unitary U = exp(iωq a† at)
and make the rotating-wave approximation resulting in the
following Hamiltonian:
HR /ℏ =

α † †
1{
a a aa + a† e−i(ωd −ωq )t [ ˜
I (ϕ, t) + i ˜
Q (ϕ, t)]
2
2
}
˜ I (ϕ, t) − i
˜ Q (ϕ, t)] ,
(C3)
+aei(ωd −ωq )t [

˜ Q (ϕ, t) =
where ˜
I (ϕ, t) = I (t) cos ϕ + Q (t) sin ϕ and 
−I (t) sin ϕ + Q (t) cos ϕ incorporate the accumulated
phase ϕ. In addition to the coherent dynamics governed by
the Hamiltonian in Eq. (C3), our simulation incorporates
decoherence by solving the system dynamics from the
following Lindblad master equation using the mesolvefunction in QuTiP [71]
)]
(
∑[
i
† 1
†
†
ρ̇ = − [HR , ρ] +
Li ρLi − ρLi Li + Li Li ρ ,
ℏ
2
i
(C4)
where ρ denotes the density
operator,
and √
we use
√
√
√ the
jump operators L− = 1 + n̄/ T1 a, L+ = n̄/ T1 a† ,

030353-14

## PDF page 15

REDUCING LEAKAGE OF SINGLE-QUBIT GATES. . .
states, i.e.,
L≈

APPENDIX D: EXPERIMENTAL SETUP
The experimental setup used for the single-qubit gate
experiments is illustrated in the wiring diagram of Fig. 6.
For the experiments, a two-qubit test device is cooled
down to 10-mK base temperature using a commercial dilution refrigerator. The used test device has a similar design
as that used in Ref. [4], in which more details are provided
regarding target design parameters and sample fabrication.
Both of the qubits on the device are grounded ﬂux-tunable
transmons, the frequencies of which can be controlled
through individual on-chip ﬂux lines connected to a roomtemperature voltage source via a twisted-pair cable and a
pair of low-pass ﬁlters.
To implement single-qubit rotations, the qubits are
capacitively coupled to individual drive lines that are connected to room-temperature electronics via 50 dB of total
nominal attenuation separated across diﬀerent temperature
stages of the cryostat. At the qubit frequency, the total
room-temperature attenuation in the cryostat was characterized to be approximately 67 dB. At room temperature,
the single-qubit control pulses are generated at an intermediate frequency using a channel pair of a HDAWG (Zurich

Vbias

HDAWG
LO

Q

I

LO

UC Board

OUT
I Q

UC Board

UHFQA

Voltage source

DC Board

Local oscillator

HEMT

–20 dB

Up-conversion
board

Still

DC Board

100 mK

Down-conversion
board

10 mK

Qubit

Splitter

UC Board

RO + Purcell

–20 dB –20 dB

–20 dB

50 K
4K

Vbias

IN
I Q

WAMP

RT

1∑
εg ≈ 1 −
⟨ψi |RX (π/2)† ρ(ψi )RX (π/2)|ψi ⟩, (C5)
6 i
where ρ(ψi ) is the resulting density operator (including
the ﬁnal Z correction) starting from the initial state ψi ,
and the sum of the initial states
√ goes over the√six cardinal states
{|0⟩,
|1⟩,
(|0⟩
+
|1⟩)/
2, (|0⟩ − |1⟩)/ 2, (|0⟩ +
√
√
i|1⟩)/ 2, (|0⟩ − i|1⟩)/ 2}. The leakage per gate is subsequently computed as the average probability to leave
the computational subspace across the six cardinal initial

1∑
{1 − Tr[|0⟩⟨0|ρ(ψi )] − Tr[|1⟩⟨1|ρ(ψi )]}.
6 i
(C6)

–10 dB –20 dB

√
and Lϕ = 1/ Tϕ a† a to model thermal relaxation, thermal excitation, and dephasing, respectively [57,72]. For
the simulations, we set the thermal steady-state population as n̄ = 0.02 based on single-shot readout experiments,
the relaxation time as T1 = 35 µs, and the dephasing time
as Tϕ = 40 µs in line with experimental results. In the
simulations, we further truncate the state space of the
anharmonic oscillator to the four lowest-energy levels. We
use four levels instead of three since we observe that the
three-level simulation sometimes underestimates the leakage error in comparison to experimental results for short
gate durations.
To simulate the application of a single-qubit RX (π/2)
gate for given control pulse envelopes I and Q , we
evolve the system dynamics according to Eq. (C4) starting from a known pure initial state, and include a zero
padding of 0.41 ns after each pulse as in the experiments.
Importantly, we aim to study the leakage and ﬁdelity under
ideal pulses and thus we do not model nonidealities of
the control electronics, such as pulse distortions or a ﬁnite
sampling rate, dynamic range, or bandwidth. In the case of
control pulses based on DRAG-L, we advance the phase ϕ
by ϕZ /2 before and after each pulse to correct for phase
errors using virtual Z rotations [18]. As a result of the
applied virtual Z rotations during Ngates gates, a ﬁnal Z
rotation by −ϕ = −Ngates ϕZ emerges [18], which does
not aﬀect experimentally measured probabilities since the
measurement occurs along the Z axis. However, this extra
Z rotation needs to be undone for the simulated density
operator using an additional Z rotation by ϕ to evaluate the
gate ﬁdelity using the density operator.
For a given control pulse shape and gate duration, we
set the drive frequency equal to the qubit frequency and
calibrate the pulse parameters {A, β, ϕZ } for a RX (π/2)
gate based on DRAG-P or DRAG-L using a simulated
calibration sequence similar to the one used in the experiments and described in Appendix G. As a minor diﬀerence,
the leakage per gate needed for calibrating β in the case
of DRAG-L is estimated based on a single simulated
RX (π/2) gate instead of using a leakage RB sequence.
After the calibration, the system dynamics are simulated for several initial states, and the error per gate is
approximated as

PRX QUANTUM 5, 030353 (2024)

WAMP
RT amplifier box

HEMT amplifier
attenuator
low-pass filter

isolator

FIG. 6. Wiring diagram of the experimental setup. Schematic
of the experimental setup used in the single-qubit gate experiments showing one of the two ﬂux-tunable qubits on the used test
device. Brief explanations for some of the symbols are presented
in the column on the right.

030353-15

## PDF page 16

ERIC HYYPPÄ et al.

PRX QUANTUM 5, 030353 (2024)

Instruments) with a sampling rate of 2.4 GSa/s and a peakto-peak maximum amplitude range of 3 or 4 V enabled by
an internal ampliﬁer, which limits the analog bandwidth to
300 MHz. To attain a sample-level granularity for the gate
duration and facilitate envelope predistortion discussed in
Appendix H, we evaluate the I and Q envelope waveforms
of each gate sequence on a computer accounting for the
virtual Z rotations, after which we send these long waveforms to the HDAWG. The intermediate-frequency control
pulses are up-converted to the qubit frequency using an IQ
mixer and an in-house-built local oscillator with an integrated root-mean-squared phase jitter below 4 mrad from
1 kHz to 10 MHz.
For qubit-state readout, the qubits are capacitively coupled to individual readout structures consisting of a readout
resonator and a Purcell ﬁlter with both of the readout structures further coupled to a common probe transmission line.
We generate the readout pulses at an intermediate frequency using an UHFQA (Zurich Instruments) and upconvert the pulses with an IQ mixer and a single SGS100A
microwave generator (Rohde & Schwarz) that is used both
for the up-conversion and down-conversion of the readout signal. On its way to the sample, the readout signal is
passed through 60 dB of nominal attenuation. The readout
signal transmitted through the probe line is ampliﬁed using
an high-electron-mobility transistor (HEMT) at the 4-K
stage with further ampliﬁcation applied at room temperature. The ampliﬁed readout signal is downconverted back
to an intermediate frequency and subsequently digitized
using the UHFQA. Note that our setup does not include
a quantum-limited parametric ampliﬁer despite which we
reach a decent two-state readout assignment ﬁdelity of up
to approximately 95%.

APPENDIX E: THREE-STATE READOUT
In this section, we brieﬂy describe our approach for
performing three-state readout on the qubit used for the
single-qubit gate studies. At the ﬂux-insensitive operation point, we measure a dispersive shift of χ /(2π ) = 4.0
MHz. For the readout pulse, we use a readout frequency of
6.146 GHz and a relatively long pulse duration of 1.5 µs
due to the absence of a quantum-limited ampliﬁer in the
readout chain. For the integration of the acquired readout signal, we use an integration time of 1.5 µs and set
all integration weights to unity. To calibrate the classiﬁcation boundaries for three-state readout, we repeatedly
prepare the qubit in each of the states |0⟩, |1⟩, and |2⟩, and
record 215 = 32 678 single-shot IQ voltages for each state,
as shown in Fig. 7. For each prepared state, the mean of
the acquired IQ voltages is computed and for new readout
events, the qubit is assigned to the state with the smallest
distance between the recorded single-shot IQ voltage and
the state mean. The resulting readout assignment matrix is

FIG. 7. Three-state classiﬁcation. Single-shot readout voltages
in the IQ plane for the prepared states |0⟩ (blue dots), |1⟩ (red
dots), and |2⟩ (black dots). The colored regions illustrate the
state-classiﬁcation boundaries. To compute the readout assignment matrix, we use 215 = 32 768 shots for each of the prepared
states, but we have down-sampled the number of points by a
factor of 15 for illustration purposes.

given by
⎡

0.972
β = ⎣0.095
0.024

0.025
0.742
0.126

⎤
0.003
0.162⎦ ,
0.850

(E1)

where βij corresponds to the probability of assigning the
qubit to the j th state after preparing it to the ith state. We
attribute the readout errors to ﬁnite state overlap between
the states |1⟩ and |2⟩, state-preparation errors due to a thermal e-state population of approximately 2%, and T1 decay
during the readout.
Similarly to, e.g., Ref. [18], we correct most of the
remaining readout errors using the inverse of the stateassignment matrix as
pcorr = β−T pmeas ,

(E2)

where pcorr = (pg , pe , pf ) ∈ R3×1 is the corrected vector of
state probabilities, and pmeas ∈ R3×1 is the measured vector of state probabilities before the correction. We point out
that the readout correction is important for accurate measurement of leakage per gate since the leakage RB protocol
is sensitive to SPAM errors unlike the standard RB and
interleaved RB protocols.
APPENDIX F: HYPERPARAMETER SELECTION
FOR FAST DRAG AND HD DRAG
In this section, we provide guidelines for selecting and
calibrating the hyperparameters for FAST DRAG (N , {wj },
{[fl,j , fh,j ]}) and HD DRAG ({β2n }). We ﬁrst consider a scenario where the ef transition is the dominant source of

030353-16

## PDF page 17

REDUCING LEAKAGE OF SINGLE-QUBIT GATES. . .

For HD DRAG, the procedure is simpler as the only additional parameter is β2 , which can be set as β2 = 1/α 2 to
mitigate f -level leakage. According to simulations shown
in Fig. 8(a), the above guidelines are expected to outperform cosine DRAG-L at least for typical transmon anharmonicities |α|/(2π ) ∈ (150, 300) MHz across fast gate
durations tg |α|/(2π ) ∈ (1, 2), for which cosine DRAG-L
is not suﬃcient to suppress leakage errors. Note that the
hyperparameters obtained with these guidelines are very
close to the parameters used for the experiments in Sec. III.
The above heuristic guidelines are based on the following reasoning. In the experiments and the simulations,
the optimal center frequency (fl,ef + fh,ef )/2 is observed
to approximately equal the anharmonicity |α|/(2π ), with
the minimum of leakage being relatively broad, as shown
in Figs. 13(e) and 14(e) in Appendix J. By selecting
(fl,ef + fh,ef )/2 = |α|/(2π ), one is expected to obtain a
leakage rate that is typically within a factor of 2 of the
optimal leakage rate, see Fig. 8(b). The choice of the
cutoﬀ frequency fc = 2|α|/(2π ) provides a reasonable balance between leakage suppression and regularization of
the pulse shape, which ensures a low leakage error for
fast gates while limiting the peak amplitude compared to
cosine DRAG-L pulses [see Fig. 3(f)]. When it comes

Leakage per gate Lg

FAST DRAG-L:
| |/(2 ) = 100 MHz

10 3

| |/(2 ) = 160 MHz
| |/(2 ) = 212 MHz
| |/(2 ) = 300 MHz
10 4

Cosine DRAG-L:
| |/(2 ) = 212 MHz

10 5

1.0

1.5

2.0

2.5

3.0

tg | |/(2 )
(b)

FAST DRAG-L
tg | |/(2 )
1.0

1.5

2.0

2.5

3.0

3.5

14

16

4.0

240

ef-range center

(1) Parametrize the weight ratio as wef = w1 /w2
and the frequency intervals to be suppressed
as [fl,1 , fh,1 ] = [fl,ef , fh,ef ] and [fl,2 , fh,2 ] = [fc , ∞].
Now, the hyperparameters to be determined are
{fl,ef , fh,ef , fc , wef , N }.
(2) Measure the anharmonicity α/(2π ) of the qubit
in Hz.
(3) Set the center of the ﬁrst frequency interval to
the measured anharmonicity and the width, e.g.,
as 0.1 × |α|/(2π ) (approximately 20 MHz for typical transmon anharmonicities) resulting in fl,ef =
0.95 × |α|/(2π ) and fh,ef = 1.05 × |α|/(2π ).
(4) Set the cutoﬀ frequency as fc = 2|α|/(2π ) based on
the measured anharmonicity.
(5) Set the weight as wef = 5 for DRAG-L and wef =
100 for DRAG-P similarly to the experiments in this
work.
(6) The number of Fourier terms can be set, e.g., as
N = 4.
(7) To implement single-qubit gates, use Eqs. (2)
and (5) to obtain the pulse shape for the selected
hyperparameters

(a)

(f l, ef + fh, ef)/2 (MHz)

leakage as in this work. Subsequently, we brieﬂy cover the
expected modiﬁcations that are needed to mitigate multiple leakage transitions, e.g., in simultaneous single-qubit
gates suﬀering from crosstalk.
To mitigate leakage to the f -level, the hyperparameters
of the FAST method can be selected using the following
physics-based heuristic algorithm:

PRX QUANTUM 5, 030353 (2024)

230
220
210
Optimum
Lg at most twice
the optimum
| |/(2 )

200
190
180
6

8

10

12

18

Gate duration tg (ns)

FIG. 8. Hyperparameter selection for FAST DRAG. (a) Simulated leakage per gate Lg as a function of the normalized
gate duration tg |α|/(2π ) for diﬀerent anharmonicities α/(2π ) ∈
{−100, −160, −212, −300} MHz (shades of blue) when selecting the hyperparameters of FAST DRAG-L using the heuristic
algorithm of Appendix F. For comparison, we show the leakage
of cosine DRAG-L (red line) for α/(2π ) = −212 MHz. In the
simulations, we assume T1 = 35 µs, Tϕ = 40 µs, and n̄ = 0.02
as explained in Appendix C. (b) Optimal value for the center of
the suppressed frequency interval (fl,ef + fh,ef )/2 (dark blue) to
minimize simulated leakage per gate Lg as a function of the gate
duration for FAST DRAG-L when selecting other parameters
based on the heuristic algorithm of Appendix F. The colored area
shows values of (fl,ef + fh,ef )/2 yielding a leakage per gate at
most twice the optimal value, while the dashed line corresponds
to |α|/(2π ). For each gate duration, the DRAG coeﬃcient β is
calibrated assuming (fl,ef + fh,ef )/2 = |α|/(2π ) and kept ﬁxed
while sweeping (fl,ef + fh,ef )/2.

to the weight wef and the interval width fh,ef − fl,ef , we
observe that the resulting leakage error for FAST DRAGL pulses is largely insensitive to the exact value of these
parameters both in simulations and experiments as long
as the parameters have the correct order of magnitude,

030353-17

## PDF page 18

ERIC HYYPPÄ et al.

PRX QUANTUM 5, 030353 (2024)
FAST DRAG, N = 6, fc

(a)

tp | |/(2 )

1.0

1.5

2.0

2.5

or wef

3.0

3.5

4.0

Coefficient |cn|

1.0
0.8

c1
c2
c3

0.6

c4
c5

0.4

c6

0.2
0.0
6

8

10

12

14

16

18

20

Pulse duration tp (ns)
FAST DRAG, fc

(b)
1.0

1.5

2.0

or wef

tp | |/(2 )
2.5

3.0

12

14

3.5

7

Ncrit

6
5
4
3
2
6

8

10

16

18

Pulse duration tp (ns)
FAST DRAG, N = 6, fc = 450 MHz, wef = 100

(c)

tp | |/(2 )

1.0

1.5

2.0

2.5

3.0

3.5

4.0

0.35

Coefficient |cn|

see Figs. 14(d) and 14(f) in Appendix J. However, we
observe that too aggressive spectral suppression with an
excessively high value of wef may lead to increased leakage errors with the DRAG-L calibration, as shown in
Fig. 14(d).
Furthermore, there is some freedom in the selection of
the number of Fourier terms since already N = 2 provides
a low leakage rate for FAST DRAG-L in the studied system with one dominant leakage transition, as shown in
Fig. 14(b). However, a higher number of basis functions
N ≥ 3 may be beneﬁcial to suppress the in-phase spectrum across more than one leakage transitions or to control
the strength of the spectral suppression. This is exempliﬁed
in Fig. 13(b) demonstrating that the leakage errors caused
by FAST DRAG-P pulses are reduced by increasing the
number of basis functions, which allows a stronger spectral suppression around the ef transition for fast gates.
Importantly, the use of a ﬁnite cutoﬀ frequency fc and
weight wef render the pulse shape and the leakage error
less sensitive to the choice of N . For fc → ∞ or wef → ∞,
there exists a critical value Ncrit below which the choice
of N naturally limits the bandwidth and peak power but
above which the Fourier coeﬃcients {cn } attain high absolute values leading to a high peak power and bandwidth
of the control pulse. Here, we deﬁne the critical value
Ncrit as the largest value of N ensuring that the highestfrequency component remains bounded according to the
condition |cN | < θ/tp in the case of fc → ∞ or wef → ∞,
where θ is the rotation angle of Eq. (4). As the pulse duration is reduced, the Fourier coeﬃcients of high-frequency
components increase ﬁrst as illustrated in Fig. 9(a), thus
implying that the critical value Ncrit is reduced for short
gate durations, as shown in Fig. 9(b). For fast gates with
tp |α|/(2π ) ∈ (1, 2), the number of basis functions would
need to be limited to N = 2 to ensure a reasonable bandwidth and peak power in the case of fc → ∞ or wef →
∞. For these reasons, we favor the use of a ﬁnite cutoﬀ frequency and weight, which lead to bounded Fourier
coeﬃcients across gate durations of interest, see Fig. 9(c).
Thus, the cutoﬀ frequency allows us to regularize the
pulse shape, while still beneﬁting from the stronger and
more ﬂexible spectral suppression and potentially reduced
leakage errors obtained with increasing N .
We note that further performance improvements compared to the heuristic algorithm may be achieved by performing closed-loop optimization of the hyperparameters
as a part of the single-qubit gate calibration. The parameter values predicted by the heuristic algorithm can be used
as educated initial values to enhance convergence.
In the presence of multiple leakage transitions, e.g., in
simultaneous single-qubit gates, the heuristic algorithm for
FAST DRAG needs to be extended. Similarly to the singlequbit case, one should measure the frequencies of potential
undesired transitions, and estimate the coupling strength
to each of these transitions. Subsequently, one can choose

0.30

c1
c2
c3

0.25
0.20

c4
c5

0.15
0.10

c6

0.05
0.00
6

8

10

12

14

16

18

20

Pulse duration tp (ns)

FIG. 9. Regularizing eﬀect of the cutoﬀ frequency on the
Fourier coeﬃcients in FAST DRAG pulses. (a) Absolute value
of the Fourier coeﬃcients |cn | as a function of pulse duration
for a FAST DRAG pulse with N = 6 and a single suppressed
frequency interval [fl,ef , fh,ef ] = [194, 214] MHz, i.e., fc → ∞ or
wef → ∞. (b) Critical number of basis functions Ncrit as a function of pulse duration for a FAST DRAG pulse with fc → ∞ or
wef → ∞. (c) Same as (a) but using a second frequency interval to specify a cutoﬀ frequency fc = 450 MHz and a weight
wef = 100 controlling the relative suppression across the two
frequency intervals.

to suppress frequency intervals corresponding to the ef
transition and the dominant crosstalk-induced transitions,
while reserving an additional frequency interval to regularize the pulse shape. A good starting point for FAST

030353-18

## PDF page 19

REDUCING LEAKAGE OF SINGLE-QUBIT GATES. . .
DRAG is to set the center frequencies of the intervals
equal to the frequencies of the undesired transitions. To
enable strong spectral suppression across more than one
frequency interval, one should also use N ≥ 3 basis functions. Furthermore, one should be aware that aggressive
spectral suppression across multiple frequency intervals
leads to increased spectral power across nonsuppressed
frequencies and a wider bandwidth, which may have unintended consequences in systems with high crosstalk or
with many transitions to avoid. Thus, further research is
needed to design reliable heuristics for setting the weights
and widths of the frequency intervals using the measured
frequencies and the associated coupling strengths. With
HD DRAG, the suppressed baseband frequencies {fj } can
be directly set to the undesired transition frequencies, after
which the parameters {β2n } can be solved from Eq. (B5).
As emphasized in Sec. II C, HD DRAG cannot control the
relative strength of spectral suppression between the different frequency intervals in contrast to FAST DRAG that
provides more ﬂexibility, which is expected to enable an
enhanced performance in systems with multiple leakage
transitions. As the multiqubit system is more challenging
and the required number of parameters is higher compared to the single-qubit system, closed-loop optimization
may be needed to reach close-to-optimal performance.
However, physics-based heuristics are expected to help in
ﬁnding good initial values for the optimization.

APPENDIX G: SINGLE-QUBIT GATE
CALIBRATION
Here, we describe our procedure for calibrating
the parameters of a single-qubit RX (π/2) gate implemented with a control pulse of the form rf (t) =
I (t) cos(ωd t + ϕ) + Q (t) sin(ωd t + ϕ), where I (t) =
A × norm
(t) with A being the in-phase amplitude,
I
˙ I (t)/α, and the phase ϕ is either set to zero
Q (t) = −β 
for DRAG-P or advanced by ϕZ before each gate for
DRAG-L. Diﬀerent calibration experiments are needed for
DRAG-P and DRAG-L as DRAG-P tunes β to minimize
phase errors, whereas DRAG-L calibrates β to minimize
leakage as discussed in Sec. II A. See Fig. 10 for a ﬂow
chart of the calibration procedure.
For DRAG-P, we calibrate the set of parameters
{A, β, ωd /(2π )}, such that the amplitude A controls the
rotation angle of the gate, β minimizes phase errors during
the gate and ωd /(2π ) is set to the qubit frequency to avoid
phase errors during idling. Assuming the qubit frequency
is roughly known, we ﬁrst determine an initial estimate for
the amplitude A by sweeping its value in a Rabi oscillation
experiment. Subsequently, the qubit frequency ωq /(2π )
is obtained from a Ramsey experiment, and the drive
frequency is set as ωd /(2π ) = ωq /(2π ). An initial estimate for the DRAG coeﬃcient β is then obtained using

PRX QUANTUM 5, 030353 (2024)

FIG. 10. Calibration ﬂow chart. Flow chart of the single-qubit
gate calibration. See Appendix H and Fig. 11 for more details
on microwave-pulse predistortion calibration and Appendix F for
more details on hyperparameter selection.

a Q-scale experiment, in which the excited-state probability is recorded for gate sequences (RX (π ), RY (π/2)) and
(RY (π ), RX (π/2)) for varying β to ﬁnd the value of β
with equal excited-state probability after both sequences,
which ideally corresponds to vanishing phase errors [49].
Finally, the estimates for A and β are improved by iterating a loop of error-ampliﬁcation measurements. In the
loop, the amplitude estimate A is reﬁned in a BangBang
experiment, in which the excited state probability is measured after a gate sequence consisting of an initial RX (π/2)
gate followed by repeated (RX (π/2), RX (π/2), RX (π/2),
RX (π/2)) sequences amplifying amplitude errors. By
sweeping the amplitude A and the number of rotations
around the Bloch sphere, the optimal value of A is
accurately determined based on the measured excitedstate probability. Subsequently, we conduct a phase errorampliﬁcation experiment consisting of repeated (RX (π/2),
RX (π/2), RX (−π/2), RX (−π/2)) sequences [17,50] followed by a ﬁnal RY (π/2) gate, thanks to which the measured excited-state probability is linearly sensitive to phase
errors [73]. By sweeping β and the number of repeated
sequences, the value of β minimizing phase errors can
be accurately measured. Typically, we iterate the loop of
error-ampliﬁcation experiments 2–3 times, and the whole
calibration procedure lasts a few minutes with signiﬁcant
room for improvement using, e.g., restless measurements
[74,75] or active qubit reset.
For DRAG-L, we calibrate the set of parameters
{A, β, ϕZ , ωd /(2π )} such that the amplitude A controls the

030353-19

## PDF page 20

ERIC HYYPPÄ et al.

PRX QUANTUM 5, 030353 (2024)

rotation angle of the gate, β minimizes leakage, ϕZ counteracts the accumulated phase error during the gate, and
ωd /(2π ) is set to equal the qubit frequency to avoid phase
errors during idling. Similarly to the case of DRAG-P, we
ﬁrst determine an initial estimate for A from a Rabi oscillation experiment followed by a characterization of the
qubit frequency from a Ramsey experiment. Subsequently,
a leakage RB experiment is conducted with a ﬁxed number of Cliﬀord gates and the f -state population after the
RB sequence is measured as a function of β to minimize
the f -state leakage. The leakage RB experiment with a
sweep of β is repeated with a longer Cliﬀord sequence
and a narrower sweep range to improve the estimate of
β. Finally, the virtual-Z parameter ϕZ and the amplitude
A are estimated from an iterative loop of error ampliﬁcation experiments: First, the value of ϕZ minimizing phase
errors is determined by sweeping ϕZ and the number of
repeated gates in a phase-error-ampliﬁcation experiment.
Subsequently, the amplitude A is obtained from a similar BangBang experiment as used for DRAG-P. Typically,
we iterate the loop 2–3 times, and the whole calibration
procedure lasts approximately 10 min with the leakage calibration dominating the calibration time. For both DRAG
variants, the commonly employed AllXY sequence [49]
may be used as a simple check of whether the calibration
has been successful.
APPENDIX H: IMPLEMENTATION AND
CALIBRATION OF CONTROL-PULSE
PREDISTORTION
In this section, we provide more details on our approach
for predistorting the control-pulse envelopes. Similarly to
Ref. [45], we apply the framework of linear time-invariant
(LTI) systems to model the distortions of the control-pulse
envelopes occurring between the generation of the control
pulse and the arrival of the pulse to the qubit device. For
performing the predistortion, we more speciﬁcally assume
that both the I and Q control envelopes suﬀer from I
distortions (see Fig. 5) modeled with a continuous-time
exponential IIR ﬁlter. We expect the step response at the
qubit to be
∑
yi (t) = h(t) ∗ ui (t) = ui (t) × (1 +
aj e−t/τj ), (H1)
j

where for the component i ∈ {I , Q}, h(t) is the impulse
response, i.e., the kernel function assumed equal for both
components, ui (t) is a step function, {aj } is the set of amplitude coeﬃcients and {τj } are the respective decay time
constants. We need to predistort the generated controlpulse envelopes as xi,pred (t) = h−1 (t) ∗ xi,target (t) such that
the control-pulse envelopes reaching the qubit match the
targeted envelope functions xi,target (t). In practice, it is
more convenient to implement the predistortion in the frequency domain [45], in which convolutions are converted

into products and the Fourier transform of the predistorted
control-pulse envelope is given by
x̂i,pred (f ) =

x̂i,target (f )
ĥ(f )

,

(H2)

with the Fourier transform of the exponential IIR kernel
function ĥ(f ) given by
ĥ(f ) = 1 +

∑ iaj 2π f τj
.
1 + i2π f τj
j

(H3)

In our predistortion approach, we use only a single exponential with parameters a1 and τ1 .
In practice, the predistortion procedure is as follows [45]: First, the targeted waveforms xI ,target [n] and
xQ,target [n] for the I and Q components are constructed
based on the gate sequence to be executed, and suﬃcient
zero padding is added to the end of the waveforms. Subsequently, the discrete Fourier transforms x̂I ,target [f ] and
x̂Q,target [f ] are computed using the fast Fourier transform
(FFT) algorithm, and the Fourier transforms for the predistorted envelopes x̂I ,pred [f ] and x̂Q,pred [f ] are obtained using
Eqs. (H2) and (H3). Finally, the predistorted waveforms
xI ,pred [n] and xQ,pred [n] are obtained in the time domain by
taking the inverse discrete Fourier transform.
To calibrate the predistortion parameters {τ1 , a1 } and
to validate the use of the exponential IIR ﬁlter model
for I distortions, we use the I-distortion characterization
experiment consisting of repeated (RX (π ), RY+ϕ (π )) =
(RX (π/2), RX (π/2), RY+ϕ (π/2), RY+ϕ (π/2)) sequences
that amplify coherent errors caused by I distortions, while
being practically insensitive to other common coherent
errors, such as amplitude miscalibration or phase errors as
explained in Sec. III A. First, we characterize the decay
time constant τ1 by measuring the axis shift ϕs from an
I-distortion characterization experiment as a function of
the delay td between consecutive pulses without applying predistortion as illustrated in Fig. 11(a). To approximate a square pulse and the resulting exponential tail, we
parametrize the in-phase envelope as
⎧
⎪
t ∈ [0, tr )
⎨[1 − cos(2π t/(2tr )]/2,
I (t) = 1,
t ∈ [tr , tp − tr )
⎪
⎩[1 − cos(2π(t − t)/(2t )]/2, t ∈ [t − t , t ],
p
r
p
r p
(H4)
where tr = 6.25 ns is a ﬁxed rise time. The quadrature envelope is obtained using DRAG-P to avoid virtual Z rotations used by DRAG-L from mixing I and C
distortions.
As shown in Fig. 11(a), we estimate the decay time τ1
from an exponential ﬁt to the results of an I-distortion characterization experiment, which we repeat for varying gate

030353-20

## PDF page 21

REDUCING LEAKAGE OF SINGLE-QUBIT GATES. . .

6.25 ns

tp = 13.3 ns
tp = 17.1 ns

0.4

I

0.5

10

10

6
4
2

tp = 32.1 ns

tp

0.6
0

tp = 23.8 ns

Q

8

20

30

Experiment
1 = 8 ns for predistortion

0
12.5 15.0 17.5 20.0 22.5 25.0 27.5 30.0 32.5

40

Pulse duration tp (ns)

Delay between pulses td (ns)

(d)

(e)

FAST DRAG-P

0.00

FAST DRAG-P

101

i

0.50

0.25
0.50

a1 =

0.06, tp = 9.6 ns

0.75

a1 =

0.03, tp = 9.6 ns

a1 = 0.00, tp = 9.6 ns

1.00
0

5

10

15

20

25

Cost function

0.25

CosRiseFall DRAG-P

Pulse duration tp (ns)
40 30 25

0.6
0.5

tp = 15.8 ns

100

a1 = 0.028
for pre-distortion

10 1

Delay between pulses td (ns)

a1 coefficient

13

0.3
0.2
0.1
0.0
0.1

0.2

0.3

0.4

0.5

0.6

0.7

RX ( /2) pulse amplitude A (V)
FAST DRAG

1.0

1.0
0.9

0.8

0.8

0.6

0.02

0.4

0.02

0

1

2

3

4

5

6

0.00

10

0.2

20

15

25

No predistortion
With predistortion

0.0

0.06 0.05 0.04 0.03 0.02 0.01 0.00

15

0.4

tp = 11.2 ns
tp = 13.3 ns

20

Experiment
Linear fit

(f)

tp = 9.6 ns

2
s (td, i )

s (deg.)

0.75

Axis shift

1.00

(c)

I

0.2

1 (ns)

0.1

12

Decay time

s (deg.)

Axis shift

0.0

0.3

CosRiseFall DRAG-P

14

Absolute axis shift | s| (deg.)

(b)

CosRiseFall DRAG-P
0.1

I envelope

(a)

PRX QUANTUM 5, 030353 (2024)

0

5

10

15

20

25

Time t (ns)

FIG. 11. Parameter calibration for envelope predistortion using an exponential IIR inverse ﬁlter. (a) Axis shift ϕs (circles) measured
from I-distortion characterization [see Fig. 5(a)] as a function of the delay td between consecutive pulses for pulse durations tp ∈
{13.3, 17.1, 23.8, 32.1} ns. The solid lines show exponential ﬁts estimating the time constant τ1 for each pulse duration. The inset
shows the used pulse shape, the in-phase envelope of which has a 6.25-ns-long cosine-shaped rise and fall. (b) Decay time constant
τ1 measured as in panel (a) as a function of the pulse duration tp . The blue, red, orange, and gray circles correspond to the results for
the pulse durations of panel (a). The dashed line shows τ1 = 8 ns chosen for exponential IIR predistortion. (c) Absolute axis shift |ϕs |
without any delay between consecutive pulses, i.e., td = 0 as a function of pulse duration and thus pulse amplitude. The dashed line
shows a linear ﬁt to data. (d) Axis shift ϕs from I-distortion characterization as a function of delay td between consecutive
∑ pulses for
three values of the predistortion coeﬃcient a1 when using a FAST DRAG-P pulse with tp = 9.6 ns. (e) Cost function i ϕs (td,i )2 as a
function of a1 for four diﬀerent pulse durations of FAST DRAG-P, with the minimum of the cost function at a1 = −0.028 indicated
by the dashed line. (f) In-phase envelope for a 6.25-ns-long FAST DRAG pulse with (dashed dark blue) and without (solid light blue)
envelope predistortion. The insets show close ups to the peaks and tail of the pulse.

durations. As shown in Fig. 11(b), the decay times vary
between 6 and 12 ns with the results being less reliable
for pulse durations above 30 ns due to a reduced signal-tonoise ratio [see, e.g., the gray points in Fig. 11(a)]. Based
on the data, the measured decay time is approximately 8 ns
across a wide range of pulse durations tp ∈ [18, 28] ns, for
which the square pulse approximation is reasonable while
the signal-to-noise ratio is still high. Hence, we choose
to use τ1 = 8 ns for the exponential IIR predistortion. In
Fig. 11(c), we further show the axis shift |ϕs | measured
without delay between pulses as a function of the pulse
duration and the corresponding pulse amplitude, which
allows us to verify that the axis shift |ϕs | is linearly proportional to the pulse amplitude as expected for distortions
caused by an LTI ﬁlter.
Having determined the decay time τ1 , we calibrate the
amplitude coeﬃcient a1 . To achieve this, we again measure
the axis shift ϕs as a function of the delay td between pulses
in an I-distortion characterization experiment but this time
we predistort the control envelopes using the calibrated

decay time τ1 = 8 ns and try diﬀerent values of a1 , as
shown in Fig. 11(d). For
∑each value of a1 , we evaluate
a cost function c(a1 ) = i ϕs (a1 , td,i )2 based on the axisshift values measured for diﬀerent delays {td,i }. Sweeping
a1 and trying few diﬀerent pulse durations, we ﬁnd that
the cost function reaches its minimum at approximately
a1 = −0.028, where its value is an order of magnitude
smaller compared to a1 = 0 for pulse durations tp ∼ 10 ns.
Using the obtained parameters τ1 = 8 ns and a1 = −0.028,
we illustrate the in-phase envelope of a FAST DRAG-P
pulse with and without predistortion in Fig. 11(f).
We point out that the current calibration procedure for
the predistortion parameters {τ1 , a1 } is relatively time consuming, but fortunately the same calibration works across
diﬀerent pulse shapes and gate durations. We observed
that the calibrated parameters systematically improved the
gate performance over the cooldown, during which the
data for the main text was collected. In a subsequent
cooldown without any changes to the cabling, the I distortions measured from the I-distortion characterization

030353-21

## PDF page 22

ERIC HYYPPÄ et al.

PRX QUANTUM 5, 030353 (2024)

experiment were observed to no longer follow an exponential decay and could not be corrected well using an
exponential IIR inverse ﬁlter with a single exponential
term. After a further thermal cycle without any changes
to the cabling, the simple exponential decay was recovered
in the I-distortion characterization experiment and essentially the same parameters τ1 = 8 ns and a1 = −0.028
were found to provide optimal performance.
We also attempted to correct the C distortions observed
in Fig. 5(f) by assuming the C distortions to be described

by a cross-quadrature exponential IIR ﬁlter model of
the form
⎛
⎞
∑
y(t) = u(t) × ⎝1 + i
ãj e−t/τ̃j ⎠ ,
(H5)
j

where y(t) = yI (t) + iyQ (t) is the complex envelope seen
by the qubit, u(t) = uI (t) + iuQ (t) is the step function in
both I and Q components, and {ãj , τ̃j } are the distortion

tg | |/(2 )

(a)

1.0

1.5

2.0

2.5

3.0

12

14

3.5

4.0

Leakage per gate Lg

10 2

10 3

10 4

10 5
6

8

10

16

18

20

Leakage threshold
FAST DRAG-L
FAST DRAG-P
HD DRAG-L
HD DRAG-P
Slepian DRAG-L
Slepian DRAG-P
Cosine DRAG-L
Cosine DRAG-P
Gaussian DRAG-L
Gaussian DRAG-P

Gate duration tg (ns)

(b)

FAST DRAG-L

HD DRAG-L

I

I

Q

Q

Slepian DRAG-L

I

Cosine DRAG-L

I

Q

Gaussian DRAG-L

I

Q

Q

tp=6 ns
Gaussian DRAG-P
2

tg | |/(2 )
3

4

Gaussian DRAG-L

(d)

5

10 3

tp = 4 , discont.
tp = 4 , cont.
tp = 5 , cont.

10 4

tp = 6 , cont.
10 5
10

15

20

Leakage per gate Lg

Leakage per gate Lg

(c)

2

tg | |/(2 )
3

4

5

10 3

tp = 4 , discont.
tp = 4 , cont.
tp = 5 , cont.

10 4

tp = 6 , cont.
10 5

25

5

Gate duration tg (ns)

10

15

20

25

Gate duration tg (ns)

FIG. 12. Relation between leakage and gate duration. (a) Experimental leakage error per gate Lg (markers) and simulated leakage
error of RX (π/2) as functions of gate duration (tg = tp + 0.41 ns) for pulse shapes based on FAST DRAG (blue), HD DRAG (gray),
Slepian DRAG (green), cosine DRAG (red), and Gaussian DRAG (orange) calibrated using DRAG-P (light color) or DRAG-L (dark
color). The experimental results are based on the mean of 3–14 RB measurements with the error bars showing the standard error of the
mean. For Gaussian DRAG, we use σ = tp /5 and subtract the discontinuity of the in-phase envelope. For Slepian DRAG, we minimize
the spectral energy above fc = 185 MHz. The dashed line shows the leakage threshold of Lg = 5 × 10−5 used to determine the speed
limit for Fig. 4(a). (b) In-phase (I , solid) and quadrature (Q, dashed) envelopes for the pulse shapes of panel (a) using DRAG-L and
a pulse duration of tp = 6 ns. Square markers illustrate the sampling rate of our AWG. (c) Experimental leakage per gate (markers)
and simulated leakage error for RX (π/2) as functions of the gate duration for diﬀerent versions of Gaussian DRAG-P. For the diﬀerent
versions, we vary the tp /σ ratio using values from the set tp /σ ∈ {4, 5, 6}. We also either subtract the oﬀset of the Gaussian making
the in-phase envelope continuous (dark color) or do not subtract the oﬀset leaving the in-phase envelope discontinuous (light color).
(d) Same as (c) but calibrating the DRAG coeﬃcient using DRAG-L.

030353-22

## PDF page 23

REDUCING LEAKAGE OF SINGLE-QUBIT GATES. . .

PRX QUANTUM 5, 030353 (2024)

parameters. However, we were not able reduce coherent errors observed in the C-distortion characterization
experiment by predistorting the control pulses under the
distortion model of Eq. (H5) despite optimizing the distortion parameters. Hence, a more appropriate model for the
C distortions would be needed to enable successful predistortion since our distortion characterization experiments
require the assumption of a speciﬁc ﬁlter model. Therefore, further research is needed to understand the exact
origins of the distortions and to devise more appropriate
ﬁlter models. One promising distortion model to be tested
in the future are control line reﬂections that could result in
both I and C distortions due to an additional phase accrued
by the reﬂected pulses. An alternative direction of research
is to develop methods for characterizing the full transfer
function of the control lines, e.g., by extending the methods
of Ref. [76].

APPENDIX I: FURTHER RESULTS ON LEAKAGE
ERROR FOR DIFFERENT PULSE SHAPES

n=2

(b)

N=4

0.4

n=1

0.2

n=3

0.0
0

1

n=4

2

3

4

5

6

wef

100
10

1

tg = 9.2 ns

10 3

10 4

10 2

1

0 fl, ef fh, ef fc

Default
tg = 7.9 ns
tg = 9.2 ns

10 3

10 4

10 5
100

101

102

103

Weight of suppression wef

104

Leakage per gate Lg

Leakage per gate Lg

(e)

FAST DRAG-P

10 2

tg = 9.2 ns

10 3

10 4

2

3

4

5

6

7

8

300

9

10 2

(f)

FAST DRAG-P
Default
tg = 7.9 ns
tg = 9.2 ns

10 3

10 4

10 5

350

400

450

500

550

Cutoff frequency fc (MHz)

Number of cosine terms N

Baseband frequency (MHz)

(d)

Default
tg = 7.9 ns

10 5

10 5

10 3

FAST DRAG-P

10 2
Default
tg = 7.9 ns

Leakage per gate Lg

| I(f )|

Time (ns)

(c)

FAST DRAG-P

10 2

Leakage per gate Lg

0.6

Leakage per gate Lg

I

0.8

I envelope

(a)

Here, we compare experimental and simulated leakage
error as a function of gate duration, see Fig. 12(a), for all
the studied pulse shapes: FAST DRAG-L/P, HD DRAGL/P, cosine DRAG-L/P, Slepian DRAG-L/P, and Gaussian
DRAG-L/P. In general, the experimental results agree with
the simulations across the diﬀerent pulse shapes and gate
durations. As an exception, the simulated leakage rate for
Slepian DRAG-L is lower than measured for the fastest
gates as discussed in Appendix J. To obtain the speed
limit presented in Fig. 4(a) for each of the pulses, we linearly interpolate the experimental leakage error to estimate
the gate duration, for which the leakage error exceeds the
threshold value of Lg = 5 × 10−5 . From Fig. 12(b) showing the envelopes of the studied pulses, we see that the
envelopes of FAST DRAG-L and HD DRAG-L resemble

FAST DRAG-P

10 2

Default
tg = 7.9 ns
tg = 9.2 ns

10 3

10 4

10 5
170 180 190 200 210 220 230 240

ef-range center (fl, ef + fh, ef)/2 (MHz)

0

10

20

30

40

50

ef-range width fh, ef

60

70

80

fl, ef (MHz)

FIG. 13. Dependence of leakage error on the parameters of FAST DRAG-P pulses. (a) Schematic of the FAST DRAG parameters
varied in panels (b)–(f). The top ﬁgure illustrates the use of N = 4 cosine waves to construct the I envelope, whereas the lower ﬁgure
ˆ I (f )| of the I envelope together with parameters controlling it, including the weight ratio wef =
shows the amplitude spectrum |
w1 /w2 , the frequency interval suppressing the ef transition [fl,ef , fh,ef ], and the cutoﬀ frequency fc controlling the bandwidth of the
pulse. The shaded blue regions show the resulting suppressed frequency intervals. (b) Experimental leakage error per gate Lg (markers)
and simulated leakage error of RX (π/2) (solid lines) as functions of the number of cosine terms N for gate durations (tg = tp + 0.41
ns) of tg = 7.9 ns (blue) and tg = 9.2 ns (red). The experimental results are based on the mean of 3–4 repeated RB experiments while
the error bars show the standard error of the mean. The dashed colored horizontal lines correspond to the experimental leakage error
of cosine DRAG-P for the corresponding gate durations, whereas the vertical dashed line shows the default parameter value used in
the main text. (c) Same as (b) but as a function of the cutoﬀ frequency fc . (d) Same as (b) but as a function of the weight ratio wef . (e)
Same as (b) but as a function of the center of the suppressed frequency interval (fl,ef + fh,ef )/2, while ﬁxing the width of the suppressed
frequency interval to the default value of 20 MHz. (f) Same as (b) but as a function of the width of the suppressed frequency interval
fh,ef − fl,ef , while keeping the center of the suppressed frequency interval at the default value of 204 MHz. The data for this ﬁgure
were collected in a later cooldown compared to the results in the main text.

030353-23

## PDF page 24

ERIC HYYPPÄ et al.

PRX QUANTUM 5, 030353 (2024)
power at the ef transition, resulting in a lower leakage in
the experiments.
Furthermore, we see from Figs. 12(c) and 12(d) that the
experiments replicate relatively well the narrow minima
in leakage error especially for the discontinuous Gaussian
envelope with tp /σ = 4. The narrow leakage minima are
caused by one of the pulse-duration-dependent dips of the
in-phase spectrum coinciding with the ef transition, see
the analogous in-phase spectrum of the cosine envelope
in Fig. 1(c). Since the location of these spectral minima
are dependent on the pulse duration for the conventional
pulse shapes, they do not enable reaching a low leakage
rate across a range of gate durations. As a ﬁnal observation from Figs. 12(c) and 12(d), we see that the leakage
rate is typically lower for a smaller tp /σ ratio at short gate
durations, whereas the situation may be the opposite for
longer gate durations. We ﬁnd that the continuous Gaussian envelope with tp /σ = 5 provides a good compromise
across the studied Gaussian parameters, though we point

n=2

(b)

N=4

0.4

n=1

0.2

n=3

0.0
0

1

n=4

2

3

4

5

| I(f)|

Time (ns)
wef

100
10 1

6

tg = 7.9 ns

10 4

3

10

Default
tg = 6.2 ns

Leakage per gate Lg

Leakage per gate Lg

(e)

FAST DRAG-L
3

tg = 7.9 ns

10 4

10 5
100

101

102

103

Weight of suppression wef

tg = 7.9 ns

10 4

2

3

4

5

6

250

7

Number of cosine terms N

Baseband frequency (MHz)

(d)

Default
tg = 6.2 ns

10 5

1

0 fl, ef fh, ef fc

FAST DRAG-L

10 3

Default
tg = 6.2 ns

10 5

10 2
10

(c)

FAST DRAG-L

10 3

Leakage per gate Lg

0.6

(f)

FAST DRAG-L

10 3

Default
tg = 6.2 ns
tg = 7.9 ns

10 4

10 5
180

190

200

210

220

300

350

400

450

500

Cutoff frequency fc (MHz)

Leakage per gate Lg

0.8

Leakage per gate Lg

I

(a)

I envelope

each other for the used parameters and require a lower
peak amplitude compared to cosine DRAG-L or Gaussian
DRAG-L.
We further study the leakage of the conventional Gaussian DRAG pulses by varying gate duration, tp /σ ratio,
and removal of the oﬀset exp[−t2p /(8σ 2 )] resulting in a
continuous or discontinuous in-phase envelope. We conclude that Gaussian DRAG does not enable as fast gates
with low leakage as does FAST DRAG or HD DRAG
for any set of parameters, see Figs. 12(c) and 12(d) for
DRAG-P and DRAG-L. The pulse with the discontinuous Gaussian envelope suﬀers from a signiﬁcantly higher
leakage error for tg > 15 ns compared to the continuous envelopes. However, the experimental leakage error is
somewhat lower than the result obtained from simulations,
in which we ignore any nonidealities of the control electronics, see Appendix C. Thus, we suspect that the ﬁnite
bandwidth of the physical control electronics eﬀectively
reduces the abrupt in-phase discontinuity and the spectral

230

ef-range center (fl, ef + fh, ef)/2 (MHz)

FAST DRAG-L

10 3

Default
tg = 6.2 ns
tg = 7.9 ns

10 4

10 5
0

10

20

30

40

50

ef-range width fh, ef

60

70

80

fl, ef (MHz)

FIG. 14. Dependence of leakage error on the parameters of FAST DRAG-L pulses. (a) Schematic of the FAST DRAG parameters
varied in panels (b)–(f). See also the caption of Fig. 13(a) for more detailed explanation. (b) Experimental leakage error per gate Lg
(markers) and simulated leakage error for RX (π/2) (solid lines) as a function of the number of cosine terms N for gate durations
(tg = tp + 0.41 ns) of tg = 6.2 ns (blue) and tg = 7.9 ns (red). The experimental results are based on the mean of four repeated RB
experiments while the error bars show the standard error of the mean. The dashed colored horizontal lines show the experimental
leakage rate of the cosine DRAG-L pulse for the corresponding gate durations, whereas the vertical dashed line shows the default
parameter value used in the main text. (c) Same as (b) but as a function of the cutoﬀ frequency fc . (d) Same as (b) but as a function
of the weight ratio wef . (e) Same as (b) but as a function of the center of the suppressed frequency interval (fl,ef + fh,ef )/2, while
ﬁxing the width of the suppressed frequency interval to the default value of 20 MHz. (f) Same as (b) but as a function of the width
of the suppressed frequency interval fh,ef − fl,ef , while keeping the center of the suppressed frequency interval at the default value of
approximately 204 MHz. The data for this ﬁgure were collected in a later cooldown compared to the results in the main text.

030353-24

## PDF page 25

REDUCING LEAKAGE OF SINGLE-QUBIT GATES. . .

PRX QUANTUM 5, 030353 (2024)

out that FAST DRAG, HD DRAG, and Slepian DRAG
provide superior performance for fast gates.

up to N = 7 for tg = 7.9 ns. For N > 7, the experimental
leakage rate is increased due to the emergence of highfrequency components, which we attribute to using a ﬁxed
upper limit fh,2 = 1000 MHz for the second frequency
interval [fc , fh,2 ] to be suppressed. By using a higher value
of fh,2 , the high-frequency components could be suppressed
and this issue could be mitigated.
From Figs. 13(c), 13(d), and 13(f), we see that the leakage rate of FAST DRAG-P is in general reduced as the
ef transition is more strongly suppressed, which can be
achieved by increasing the cutoﬀ frequency fc , the weight
ratio wef or the width fh,ef − fl,ef of the frequency interval to be suppressed. Importantly, a stronger suppression is
required to reduce the leakage rate at the shorter gate duration of tg = 7.9 ns. We further observe that the simulations
predict a somewhat lower leakage error than measured
experimentally for large values of fc , wef and fh,ef − fl,ef .
We suspect that the diﬀerence is caused by the simulations
not accounting for the nonidealities of the control electronics, such as ﬁnite bandwidth and sampling rate that hinder
the experimental performance. From Fig. 13(e), we further
see that the central frequency of the suppressed interval is
slightly shifted when changing the gate duration, though
the minimum is relatively broad.
Figure 14 shows the experimental and simulated parameter sweeps of the leakage error for FAST DRAG-L at
gate durations tg = tp + 0.41 ns of tg = 6.2 ns and tg =
7.9 ns. From Fig. 14(b), we see that using only N = 2
cosine terms results in a low leakage error even for the
gate duration of tg = 6.2 ns. Based on Figs. 14(c), 14(d),

APPENDIX J: PARAMETER SWEEPS FOR FAST
DRAG, HD DRAG, AND SLEPIAN DRAG
Here, we study the experimental and simulated leakage
error when sweeping the parameters of FAST DRAG-L/P,
HD DRAG-L, and Slepian DRAG-L. All the experimental results presented in this section have been acquired in a
later cooldown but using the same qubit device and setup
compared to the results of the main text. For FAST DRAGP/L, we consider sweeping the number of cosine terms N ,
the cutoﬀ frequency fc , the weight (ratio) wef = w1 /w2 of
ef -transition suppression, as well as the center frequency
(fl,ef + fh,ef )/2 and width fh,ef − fl,ef of the ef -transition
suppression. The meaning of each parameter value is further illustrated in Fig. 13(a). We sweep only one of the
parameters at a time and use the values provided in Sec. III
as defaults.
The parameter sweeps for the measured and simulated
leakage error obtained using a FAST DRAG-P pulse are
shown in Figs. 13(b)–13(f) for gate durations tg = tp +
0.41 ns of tg = 7.9 ns and tg = 9.2 ns. Overall, we observe
that the experimental results and simulations agree well,
and FAST DRAG-P reduces the leakage rate by up to a
factor of 30 compared to cosine DRAG-P (dashed horizontal lines) at tg = 7.9 ns. From Fig. 13(b), we see that
three cosine terms is suﬃcient to obtain a low leakage
error at tg = 9.2 ns, whereas the leakage rate is reduced
10 3

(b)

HD DRAG-L
Default
tg = 6.2 ns
tg = 7.9 ns

10 4

10 5

Leakage per gate Lg

Leakage per gate Lg

(a)

Slepian DRAG-L
Default
tg = 6.2 ns

10 3

tg = 7.9 ns

10 4

10 5
180 190 200 210 220 230 240 250

Suppressed frequency (MHz)

100

120

140

160

180

200

220

Cutoff frequency fc (MHz)

FIG. 15. Dependence of leakage error on the parameters of HD DRAG-L and Slepian DRAG-L. (a) Experimental leakage error
per gate
√ (markers) and simulated leakage error of RX (π/2) (solid lines) as functions of the suppressed baseband frequency f =
1/(2π β2 ) in the in-phase spectrum of a HD DRAG-L pulse when using a gate duration (tg = tp + 0.41 ns) of tg = 6.2 ns (gray)
and tg = 7.9 ns (pink). The experimental results are based on the mean of four repeated RB experiments while the error bars show
the standard error of the mean. The dashed colored horizontal lines correspond to the experimental leakage error of cosine DRAG-L
pulse for the corresponding gate durations, whereas the dashed vertical line shows the default parameter value used in the main text. (b)
Experimental leakage error per gate (markers) and simulated leakage error of RX (π/2) (solid lines) as functions of the cutoﬀ frequency
fc for a Slepian DRAG-L pulse when using a gate duration (tg = tp + 0.41 ns) of tg = 6.2 ns (dark green) and tg = 7.9 ns (light green).
The experimental results are based on the mean of three repeated RB experiments while the error bars show the standard error of the
mean. The dashed and solid lines have corresponding meaning as in (a). The data for this ﬁgure were collected in a later cooldown
compared to the results in the main text.

030353-25

## PDF page 26

ERIC HYYPPÄ et al.

PRX QUANTUM 5, 030353 (2024)

and 14(f), FAST DRAG-L achieves a low leakage error
with less aggressive suppression of the in-phase spectrum
compared to FAST DRAG-P since the DRAG coeﬃcient
β also contributes to leakage minimization. Hence, a low
leakage rate is reached at signiﬁcantly lower values of fc ,
wef and fh,ef − fl,ef compared to FAST DRAG-P, and in
fact, too high values of these parameters increase leakage.
From Figs. 14(b)–14(f), we further observe that moderate
changes to the parameter values have a relatively small
eﬀect on the leakage error, which can be regarded as a sign
of robustness. We observe that the diﬀerences between the
simulated and measured leakage rates are higher compared
to FAST DRAG-P, which is likely caused by the use of
shorter gate durations that may be more susceptible to the
nonidealities of the control electronics.
From Fig. 15(a) showing the leakage error of HD
DRAG-L as a function of the suppressed frequency, we
observe that the minimum of the leakage error occurs
approximately at a suppressed (baseband) frequency of
|α|/(2π ) corresponding to the default value used to obtain
the results of the main text. Furthermore, we ﬁnd that the
minimum is relatively broad. When sweeping the cutoﬀ
frequency of Slepian DRAG-L as shown in Fig. 15(b), we
observe that the default cutoﬀ frequency of fc = 185 MHz
provides a representative leakage error that cannot be much
improved by further optimizing the cutoﬀ frequency. We
also observe that the measured leakage rate at tg = 6.25 ns
is systematically higher than the simulated leakage, which
may again be caused by the ﬁnite sampling rate and bandwidth of the control electronics that do not capture well
the rapid changes in the quadrature envelope of the Slepian
DRAG-L pulse, see Fig. 12(b).

[1] Google Quantum AI, Suppressing quantum errors by scaling a surface code logical qubit, Nature 614, 676 (2023).
[2] D. C. McKay, I. Hincks, E. J. Pritchett, M. Carroll, L. C.
Govia, and S. T. Merkel, Benchmarking quantum processor
performance at scale, ArXiv:2311.05933.
[3] Z. Li, P. Liu, P. Zhao, Z. Mi, H. Xu, X. Liang, T. Su, W.
Sun, G. Xue, J.-N. Zhang, et al., Error per single-qubit gate
below 10−4 in a superconducting qubit, npj Quantum Inf.
9, 111 (2023).
[4] F. Marxer, A. Vepsäläinen, S. W. Jolin, J. Tuorila, A. Landra, C. Ockeloen-Korppi, W. Liu, O. Ahonen, A. Auer,
L. Belzane, et al., Long-distance transmon coupler with
CZ-gate ﬁdelity above 99.8%, PRX Quantum 4, 010314
(2023).
[5] Y. Sung, L. Ding, J. Braumüller, A. Vepsäläinen, B. Kannan, M. Kjaergaard, A. Greene, G. O. Samach, C. McNally,
D. Kim, et al., Realization of high-ﬁdelity CZ and ZZfree iSWAP gates with a tunable coupler, Phys. Rev. X 11,
021058 (2021).
[6] L. Ding, M. Hays, Y. Sung, B. Kannan, J. An, A. Di Paolo,
A. H. Karamlou, T. M. Hazard, K. Azar, D. K. Kim, B. M.
Niedzielski, A. Melville, M. E. Schwartz, J. L. Yoder, T. P.

Orlando, S. Gustavsson, J. A. Grover, K. Serniak, and W.
D. Oliver, High-ﬁdelity, frequency-ﬂexible two-qubit ﬂuxonium gates with a transmon coupler, Phys. Rev. X 13,
031035 (2023).
[7] M. Werninghaus, D. J. Egger, F. Roy, S. Machnes, F. K.
Wilhelm, and S. Filipp, Leakage reduction in fast superconducting qubit gates via optimal control, npj Quantum Inf. 7,
14 (2021).
[8] D. A. Rower, L. Ding, H. Zhang, M. Hays, J. An, P. M.
Harrington, I. T. Rosen, J. M. Gertler, T. M. Hazard, B.
M. Niedzielski, M. E. Schwartz, S. Gustavsson, K. Serniak, J. A. Grover, and W. D. Oliver, Suppressing counterrotating errors for fast single-qubit gates with ﬂuxonium,
ArXiv:2406.08295.
[9] X.-F. Shi, Quantum logic and entanglement by neutral Rydberg atoms: Methods and ﬁdelity, Quantum Sci. Technol. 7,
023002 (2022).
[10] D. Bluvstein, S. J. Evered, A. A. Geim, S. H. Li, H.
Zhou, T. Manovitz, S. Ebadi, M. Cain, M. Kalinowski,
D. Hangleiter, et al., Logical quantum processor based on
reconﬁgurable atom arrays, Nature 626, 58 (2024).
[11] S. J. Evered, D. Bluvstein, M. Kalinowski, S. Ebadi, T.
Manovitz, H. Zhou, S. H. Li, A. A. Geim, T. T. Wang, N.
Maskara, et al., High-ﬁdelity parallel entangling gates on a
neutral atom quantum computer, Nature 622, 268 (2023).
[12] T. P. Harty, D. T. C. Allcock, C. J. Ballance, L. Guidoni, H.
A. Janacek, N. M. Linke, D. N. Stacey, and D. M. Lucas,
High-ﬁdelity preparation, gates, memory, and readout of
a trapped-ion quantum bit, Phys. Rev. Lett. 113, 220501
(2014).
[13] J. P. Gaebler, T. R. Tan, Y. Lin, Y. Wan, R. Bowler, A. C.
Keith, S. Glancy, K. Coakley, E. Knill, D. Leibfried, et al.,
+
High-ﬁdelity universal gate set for 9 Be ion qubits, Phys.
Rev. Lett. 117, 060505 (2016).
[14] S. Krinner, N. Lacroix, A. Remm, A. Di Paolo, E. Genois,
C. Leroux, C. Hellings, S. Lazar, F. Swiadek, J. Herrmann,
et al., Realizing repeated quantum error correction in a
distance-three surface code, Nature 605, 669 (2022).
[15] F. Motzoi, J. M. Gambetta, P. Rebentrost, and F. K. Wilhelm, Simple pulses for elimination of leakage in weakly
nonlinear qubits, Phys. Rev. Lett. 103, 110501 (2009).
[16] F. Motzoi and F. K. Wilhelm, Improving frequency selection of driven pulses using derivative-based transition suppression, Phys. Rev. A 88, 062318 (2013).
[17] Z. Chen, et al., Measuring and suppressing quantum state
leakage in a superconducting qubit, Phys. Rev. Lett. 116,
020501 (2016).
[18] D. C. McKay, C. J. Wood, S. Sheldon, J. M. Chow, and
J. M. Gambetta, Eﬃcient Z gates for quantum computing,
Phys. Rev. A 96, 022330 (2017).
[19] P. Aliferis and B. M. Terhal, Fault-tolerant quantum computation for local leakage faults, Quantum Inf. Comput. 7,
139 (2007).
[20] A. G. Fowler, Coping with qubit leakage in topological
codes, Phys. Rev. A 88, 042308 (2013).
[21] M. Suchara, A. W. Cross, and J. M. Gambetta, Leakage suppression in the toric code, Quantum Inf. Comput. 15, 997
(2015).
[22] M. McEwen, D. Kafri, Z. Chen, J. Atalaya, K. Satzinger,
C. Quintana, P. V. Klimov, D. Sank, C. Gidney, A. Fowler,

030353-26

## PDF page 27

REDUCING LEAKAGE OF SINGLE-QUBIT GATES. . .

PRX QUANTUM 5, 030353 (2024)

et al., Removing leakage-induced correlated errors in
superconducting quantum error correction, Nat. Commun.
12, 1761 (2021).
[23] J. M. Chow, L. DiCarlo, J. M. Gambetta, F. Motzoi,
L. Frunzio, S. M. Girvin, and R. J. Schoelkopf, Optimized driving of superconducting artiﬁcial atoms for
improved single-qubit gates, Phys. Rev. A 82, 040305(R)
(2010).
[24] J. M. Gambetta, F. Motzoi, S. T. Merkel, and F. K. Wilhelm,
Analytic control methods for high-ﬁdelity unitary operations in a weakly nonlinear oscillator, Phys. Rev. A 83,
012308 (2011).
[25] V. Vesterinen, O.-P. Saira, A. Bruno, and L. DiCarlo,
Mitigating information leakage in a crowded spectrum of
weakly anharmonic qubits, ArXiv:1405.0450.
[26] J. M. Martinis and M. R. Geller, Fast adiabatic qubit gates
using only σz control, Phys. Rev. A 90, 022307 (2014).
[27] L. S. Theis, F. Motzoi, and F. K. Wilhelm, Simultaneous
gates in frequency-crowded multilevel systems using fast,
robust, analytic control shapes, Phys. Rev. A 93, 012324
(2016).
[28] L. S. Theis, F. Motzoi, S. Machnes, and F. K. Wilhelm,
Counteracting systems of diabaticities using drag controls:
The status after 10 years, Europhys. Lett. 123, 60001
(2018).
[29] B. Li, T. Calarco, and F. Motzoi, Experimental error suppression in cross-resonance gates via multi-derivative pulse
shaping, npj Quantum Inf. 10, 66 (2024).
[30] H. Ribeiro, A. Baksic, and A. A. Clerk, Systematic
Magnus-based approach for suppressing leakage and nonadiabatic errors in quantum dynamics, Phys. Rev. X 7,
011021 (2017).
[31] F. Setiawan, P. Groszkowski, H. Ribeiro, and A. A. Clerk,
Analytic design of accelerated adiabatic gates in realistic
qubits: General theory and applications to superconducting
circuits, PRX Quantum 2, 030306 (2021).
[32] N. Lacroix, L. Hofele, A. Remm, O. BenhayouneKhadraoui, A. McDonald, R. Shillito, S. Lazar, C. Hellings,
F. Swiadek, D. Colao-Zanuz, et al., Fast ﬂux-activated
leakage reduction for superconducting quantum circuits,
ArXiv:2309.07060.
[33] J. F. Marques, H. Ali, B. M. Varbanov, M. Finkel, H. M.
Veen, S. L. M. van der Meer, S. Valles-Sanclemente, N.
Muthusubramanian, M. Beekman, N. Haider, B. M. Terhal,
and L. DiCarlo, All-microwave leakage reduction units for
quantum error correction with superconducting transmon
qubits, Phys. Rev. Lett. 130, 250602 (2023).
[34] N. Khaneja, T. Reiss, C. Kehlet, T. Schulte-Herbrüggen,
and S. J. Glaser, Optimal control of coupled spin dynamics: Design of NMR pulse sequences by gradient ascent
algorithms, J. Magn. Reson. 172, 296 (2005).
[35] T. Caneva, T. Calarco, and S. Montangero, Chopped
random-basis quantum optimization, Phys. Rev. A 84,
022326 (2011).
[36] N. Rach, M. M. Müller, T. Calarco, and S. Montangero, Dressing the chopped-random-basis optimization:
A bandwidth-limited access to the trap-free landscape,
Phys. Rev. A 92, 062343 (2015).
[37] S. Machnes, E. Assémat, D. Tannor, and F. K. Wilhelm,
Tunable, ﬂexible, and eﬃcient optimization of control

pulses for practical qubits, Phys. Rev. Lett. 120, 150401
(2018).
[38] M. Y. Niu, S. Boixo, V. N. Smelyanskiy, and H. Neven,
Universal quantum control through deep reinforcement
learning, npj Quantum Inf. 5, 33 (2019).
[39] Y. Song, J. Li, Y.-J. Hai, Q. Guo, and X.-H. Deng, Optimizing quantum control pulses with complex constraints
and few variables through autodiﬀerentiation, Phys. Rev. A
105, 012616 (2022).
[40] J. Stehlik, D. M. Zajac, D. L. Underwood, T. Phung, J.
Blair, S. Carnevale, D. Klaus, G. A. Keefe, A. Carniol,
M. Kumph, M. Steﬀen, and O. E. Dial, Tunable coupling
architecture for ﬁxed-frequency transmon superconducting
qubits, Phys. Rev. Lett. 127, 080505 (2021).
[41] H. Zhang, C. Ding, D. K. Weiss, Z. Huang, Y. Ma, C.
Guinn, S. Sussman, S. P. Chitta, D. Chen, A. A. Houck,
J. Koch, and D. I. Schuster, Tunable inductive coupler for
high-ﬁdelity gates between ﬂuxonium qubits, PRX Quantum 5, 020326 (2024).
[42] R. Li, K. Kubo, Y. Ho, Z. Yan, Y. Nakamura, and H.
Goto, Realization of high-ﬁdelity CZ gate based on a
double-transmon coupler, ArXiv:2402.18926.
[43] R. Barends, et al., Superconducting quantum circuits at the
surface code threshold for fault tolerance, Nature 508, 500
(2014).
[44] D. Zhu, T. Jaako, Q. He, and P. Rabl, Quantum computing with superconducting circuits in the picosecond regime,
Phys. Rev. Appl. 16, 014024 (2021).
[45] S. Gustavsson, O. Zwier, J. Bylander, F. Yan, F. Yoshihara,
Y. Nakamura, T. P. Orlando, and W. D. Oliver, Improving quantum gate ﬁdelities by using a qubit to measure
microwave pulse distortions, Phys. Rev. Lett. 110, 040502
(2013).
[46] E. Lucero, J. Kelly, R. C. Bialczak, M. Lenander, M.
Mariantoni, M. Neeley, A. D. O’Connell, D. Sank, H.
Wang, M. Weides, J. Wenner, T. Yamamoto, A. N. Cleland, and J. M. Martinis, Reduced phase error through
optimized control of a superconducting qubit, Phys. Rev.
A 82, 042339 (2010).
[47] M. Papič, A. Auer, and I. de Vega, Fast estimation of physical error contributions of quantum gates,
ArXiv:2305.08916.
[48] S. Lazăr, Improving single-qubit gates in superconducting
quantum devices, Ph.D. thesis, ETH Zurich, 2023.
[49] M. Reed, Entanglement and quantum error correction
with superconducting qubits, Ph.D. thesis, Yale University,
2013.
[50] A. Bengtsson, Quantum information processing with tunable and low-loss superconducting circuits, Ph.D. thesis,
Chalmers Tekniska Högskola (Sweden), 2020.
[51] E. Hyyppä, S. Kundu, C. F. Chan, A. Gunyhó, J. Hotari,
D. Janzso, K. Juliusson, O. Kiuru, J. Kotilahti, A. Landra,
et al., Unimon qubit, Nat. Commun. 13, 6895 (2022).
[52] S. Lazăr, Q. Ficheux, J. Herrmann, A. Remm, N. Lacroix,
C. Hellings, F. Swiadek, D. C. Zanuz, G. J. Norris, M. B.
Panah, et al., Calibration of drive nonlinearity for arbitraryangle single-qubit gates using error ampliﬁcation, Phys.
Rev. Appl. 20, 024036 (2023).
[53] E. Knill, D. Leibfried, R. Reichle, J. Britton, R. B.
Blakestad, J. D. Jost, C. Langer, R. Ozeri, S. Seidelin, and

030353-27

## PDF page 28

ERIC HYYPPÄ et al.

PRX QUANTUM 5, 030353 (2024)

D. J. Wineland, Randomized benchmarking of quantum
gates, Phys. Rev. A 77, 012307 (2008).
[54] J. M. Chow, J. M. Gambetta, L. Tornberg, J. Koch,
L. S. Bishop, A. A. Houck, B. R. Johnson, L. Frunzio, S.
M. Girvin, and R. J. Schoelkopf, Randomized benchmarking and process tomography for gate errors in a solid-state
qubit, Phys. Rev. Lett. 102, 090502 (2009).
[55] E. Magesan, J. M. Gambetta, and J. Emerson, Scalable and
robust randomized benchmarking of quantum processes,
Phys. Rev. Lett. 106, 180504 (2011).
[56] J. M. Epstein, A. W. Cross, E. Magesan, and J. M. Gambetta, Investigating the limits of randomized benchmarking
protocols, Phys. Rev. A 89, 062321 (2014).
[57] C. J. Wood and J. M. Gambetta, Quantiﬁcation and characterization of leakage errors, Phys. Rev. A 97, 032306
(2018).
[58] J. Wallman, C. Granade, R. Harper, and S. T. Flammia, Estimating the coherence of noise, New J. Phys. 17, 113020
(2015).
[59] G. Feng, J. J. Wallman, B. Buonacorsi, F. H. Cho, D. K.
Park, T. Xin, D. Lu, J. Baugh, and R. Laﬂamme, Estimating
the coherence of noise in quantum control of a solid-state
qubit, Phys. Rev. Lett. 117, 260501 (2016).
[60] E. Nielsen, K. Rudinger, T. Proctor, A. Russo, K. Young,
and R. Blume-Kohout, Probing quantum processor performance with pyGSTi, Quantum Sci. Technol. 5, 044002
(2020).
[61] E. Nielsen, J. K. Gamble, K. Rudinger, T. Scholten,
K. Young, and R. Blume-Kohout, Gate set tomography,
Quantum 5, 557 (2021).
[62] G. A. L. White, C. D. Hill, F. A. Pollock, L. C. L. Hollenberg, and K. Modi, Demonstration of non-Markovian process characterisation and control on a quantum processor,
Nat. Commun. 11, 6301 (2020).
[63] G. White, Characterization and control of non-Markovian
quantum noise, Nat. Rev. Phys. 4, 287 (2022).
[64] G. A. L. White, F. A. Pollock, L. C. L. Hollenberg, K.
Modi, and C. D. Hill, Non-Markovian quantum process
tomography, PRX Quantum 3, 020344 (2022).
[65] B. Foxen, J. Mutus, E. Lucero, E. Jeﬀrey, D. Sank, R.
Barends, K. Arya, B. Burkett, Y. Chen, Z. Chen, et al., High

speed ﬂux sampling for tunable superconducting qubits
with an embedded cryogenic transducer, Supercond. Sci.
Technol. 32, 015012 (2018).
[66] M. A. Rol, L. Ciorciaro, F. K. Malinowski, B. M. Tarasinski, R. E. Sagastizabal, C. C. Bultink, Y. Salathe, N. Haandbæk, J. Sedivy, and L. DiCarlo, Time-domain characterization and correction of on-chip distortion of control pulses
in a quantum processor, Appl. Phys. Lett. 116, 054001
(2020).
[67] C. Rigetti and M. Devoret, Fully microwave-tunable universal gates in superconducting qubits with linear couplings
and ﬁxed transition frequencies, Phys. Rev. B 81, 134507
(2010).
[68] Y. Kim, A. Eddins, S. Anand, K. X. Wei, E. Van Den Berg,
S. Rosenblatt, H. Nayfeh, Y. Wu, M. Zaletel, K. Temme,
et al., Evidence for the utility of quantum computing before
fault tolerance, Nature 618, 500 (2023).
[69] M. Malekakhlagh, E. Magesan, and D. C. McKay, Firstprinciples analysis of cross-resonance gate operation, Phys.
Rev. A 102, 042605 (2020).
[70] https://doi.org/10.5281/zenodo.13365033.
[71] J. R. Johansson, P. D. Nation, and F. Nori, QuTiP: An
open-source Python framework for the dynamics of open
quantum systems, Comput. Phys. Commun. 183, 1760
(2012).
[72] H. M. Wiseman and G. J. Milburn, Quantum Measurement
and Control (Cambridge University Press, Cambridge,
2009).
[73] M. Werninghaus, Experimental optimal control of superconducting qubits, Ph.D. thesis, Technische Universität
München, 2022.
[74] M. A. Rol, C. C. Bultink, T. E. O’Brien, S. R. de Jong,
L. S. Theis, X. Fu, F. Luthi, R. F. L. Vermeulen, J. C. de
Sterke, A. Bruno, D. Deurloo, R. N. Schouten, F. K. Wilhelm, and L. DiCarlo, Restless tuneup of high-ﬁdelity qubit
gates, Phys. Rev. Appl. 7, 041001(R) (2017).
[75] C. J. Haupt and D. J. Egger, Leakage in restless quantum
gate calibration, Phys. Rev. A 108, 022614 (2023).
[76] M. Jerger, A. Kulikov, Z. Vasselin, and A. Fedorov, In situ
characterization of qubit control lines: A qubit as a vector
network analyzer, Phys. Rev. Lett. 123, 150501 (2019).

030353-28
