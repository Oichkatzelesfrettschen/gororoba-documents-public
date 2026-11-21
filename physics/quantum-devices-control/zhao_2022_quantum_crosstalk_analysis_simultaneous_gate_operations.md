Source: https://doi.org/10.1103/PRXQuantum.3.020301
PDF sha256: bca3f42ded74b9dd72ca80a2cebee6341c741c19541f51f6b7c91bfc916e1873
License: https://creativecommons.org/licenses/by/4.0/

# Transcription of zhao_2022_quantum_crosstalk_analysis_simultaneous_gate_operations.pdf

Transcription of `zhao_2022_quantum_crosstalk_analysis_simultaneous_gate_operations.pdf` in this directory, 21 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-21 from the PDF's own text layer (pdftotext version 26.10.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

PRX QUANTUM 3, 020301 (2022)

Quantum Crosstalk Analysis for Simultaneous Gate Operations on
Superconducting Qubits
Peng Zhao ,1,* Kehuan Linghu ,1,† Zhiyuan Li,1 Peng Xu,2 Ruixia Wang,1 Guangming Xue ,1,‡
Yirong Jin,1 and Haifeng Yu1
1

2

Beijing Academy of Quantum Information Sciences, Beijing 100193, China
Institute of Quantum Information and Technology, Nanjing University of Posts and Telecommunications,
Nanjing, Jiangsu 210003, China

(Received 27 October 2021; revised 30 December 2021; accepted 16 February 2022; published 1 April 2022)
Maintaining or even improving gate performance with growing numbers of parallel controlled qubits
is a vital requirement for fault-tolerant quantum computing. For superconducting quantum processors,
though isolated one- or two-qubit gates have been demonstrated with high ﬁdelity, implementing these
gates in parallel commonly shows worse performance. Generally, this degradation is attributed to various
crosstalks between qubits, such as quantum crosstalk due to residual inter-qubit coupling. An understanding of the exact nature of these crosstalks is critical to ﬁguring out respective mitigation schemes and
improved qubit architecture designs with low crosstalk. Here we give a theoretical analysis of quantum
crosstalk impact on simultaneous gate operations in a qubit architecture, where ﬁxed-frequency transmon
qubits are coupled via a tunable bus, and sub-100-ns controlled-Z (CZ) gates can be realized by applying
a baseband ﬂux pulse on the bus. Our analysis shows that for microwave-driven single-qubit gates, the
dressing from the qubit-qubit coupling can cause non-negligible cross-driving errors when qubits operate
near frequency collision regions. During CZ gate operations, although unwanted nearest-neighbor interactions are nominally turned oﬀ, sub-MHz parasitic next-nearest-neighbor interactions involving spectator
qubits can still exist, causing considerable leakage or control error when one operates qubit systems around
these parasitic resonance points. To ensure high-ﬁdelity simultaneous operations, a request could be raised
to ﬁgure out a better way to balance the gate error from target qubit systems themselves and the error
from nonparticipating spectator qubits. Overall, our analysis suggests that towards useful quantum processors, the qubit architecture should be examined carefully in the context of high-ﬁdelity simultaneous
gate operations in a scalable qubit lattice.
DOI: 10.1103/PRXQuantum.3.020301

I. INTRODUCTION
In pursuit of a useful quantum processor, the quality of qubits (e.g., qubit coherence time and ﬁdelity of
gate operations), and the number of qubits are two of
the most important ﬁgures of merit. Nonetheless, in the
practical implementation of quantum processors, an outstanding challenge is how to maintain or even improve
gate performance with growing numbers of parallel controlled qubits [1]. For quantum processors built with
*

shangniguo@sina.com
linghukh@baqis.ac.cn
‡
xuegm@baqis.ac.cn
†

Published by the American Physical Society under the terms of
the Creative Commons Attribution 4.0 International license. Further distribution of this work must maintain attribution to the
author(s) and the published article’s title, journal citation, and
DOI.

2691-3399/22/3(2)/020301(21)

superconducting qubits, isolated single-qubit gates with
gate error below 0.1% [2–5] and two-qubit gates with
gate error approaching 0.1% [2,6–13] have been demonstrated in various qubit architectures [2]. However, in
multiqubit systems, implementing gate operations in parallel has commonly shown worse gate performance, especially for simultaneous two-qubit gate operations applied
to nearby qubits, where gate errors are typically increased
by 0.1%–1% [14–18]. Generally, the performance degradation is caused by the crosstalk eﬀect [15,19] that breaks
the textbook assumption on quantum computing, i.e., gate
operations are implemented spatial locally and independently (for a high-level and hardware-agnostic deﬁnition
of crosstalk, we refer the reader to Ref. [19] for details).
Moreover, this crosstalk eﬀect can cause not just increased
gate errors but even a variety of correlated and nonlocal
errors, which are particularly harmful to the realization
of fault-tolerant quantum computing [20]. Thus, mitigating the crosstalk eﬀect is critical to improving gate

020301-1

Published by the American Physical Society

## PDF page 2

PENG ZHAO et al.

PRX QUANTUM 3, 020301 (2022)

performance in superconducting quantum processors and
achieving the long-term goal of fault-tolerant quantum
computing.
Recently, various studies on the detection, characterization, and mitigation of crosstalk have been published [8,18,
19,21–39]. From a high-level and hardware-agnostic perspective, several schemes have been proposed for detecting and characterizing crosstalk in multiqubit systems
[19,21–26]. Meanwhile, by taking software strategies, various mitigation schemes have also been proposed, such
as, at the qubit or gate level, one ﬁrst characterizes the
crosstalk and then actively cancels it with compensated
pulses [8,18,27–33] or optimal control pulses [34–36], and
at the quantum circuit level, one takes better crosstalkaware compilation schemes and instruction scheduling
schemes for implementing quantum algorithms [37–39].
However, these detection and characterization schemes
cannot, in general, directly clarify the exact nature of
crosstalk, and these software approaches for mitigating
crosstalk commonly require complex control and characterization, thus placing heavy resource burdens on the
control system and limiting their feasibility for large-scale
quantum computing. Given these considerations, besides
taking high-level software strategies, it is highly desirable to further understand crosstalk and ﬁgure out how to
mitigate crosstalk from a hardware perspective.
Crosstalk that appears in multiqubit superconducting
quantum processors is commonly very architecture dependent. For example, in qubit architectures with ﬁxed coupling and ﬁxed-frequency qubits [14], the dominated
crosstalk is associated with microwave crosstalk and
residual interqubit coupling [10,11,21], whereas in qubit
architectures with frequency-tunable qubits or tunable coupling [27,40,41], the ﬂux crosstalk is considered as more
involved [27,28]. Despite its architecture-dependent multiformity, from the hardware perspective, crosstalk can be
categorized into two types according to its physical origination [42]. One is the classical crosstalk associated with
unintended classical electromagnetic couplings, such as
dc or ac ﬂux crosstalk [28,29] and microwave crosstalk
[8,10,11]. The other one is quantum crosstalk resulting from interqubit couplings, such as residual nearestneighbor (NN) coupling [11,27] and next-nearest-neighbor
(NNN) coupling [27,41,43]. An understanding of the exact
nature of crosstalk or separating error contributions from
diﬀerent crosstalks is an urgent need for ﬁguring out
respective mitigation schemes and for obtaining improved
qubit-architecture designs with low crosstalk. Although
several works have previously examined various quantum crosstalk eﬀects, such as ZZ crosstalk for single-qubit
gates [21,44,45], two-qubit gates [10,11,33,44–54], and
spectator-qubit-induced crosstalk in multiqubit systems
[30–33,55–57], they are restricted mainly to isolated twoqubit gates. Crosstalk analysis in the context of simultaneous gate operations on a multiqubit lattice could provide

more physical insight into the nature of the crosstalk eﬀect
[18,58] on practically implemented quantum processors
[15,16].
In this work, we give a theoretical analysis of quantum crosstalk impact on simultaneous gate operations in a
qubit architecture with tunable ZZ coupling, as sketched
in Fig. 1, where ﬁxed-frequency transmon qubits [59]
are coupled via a tunable bus [60]. To do so, we ﬁrst
give detailed descriptions of the proposed qubit architecture, especially focusing on the tunable ZZ coupling
enabled by the tunable bus, gate operations, and the scalability of the architecture. We then turn to illustrate the
quantum crosstalk eﬀect on simultaneous gate operations
in this qubit architecture. We consider two typical gate
operations, i.e., single-qubit X gate and two-qubit CZ
gate.
(i) For simultaneous single-qubit X gate operations,
the dressing from the qubit-qubit coupling can induce
substantial quantum crosstalk, i.e., cross-driving eﬀect, and
the associated crosstalk strength is comparable with that of
classical microwave (see Fig. 4). Focusing on the nearestneighbor qubit pairs, we show that when qubit systems
approach the frequency-collision region, the cross-driving
eﬀect can make gate performance worse by almost an
order of magnitude (see Fig. 6). This suggests that to
ensure high-ﬁdelity single-qubit addressing, this dressinginduced cross-driving eﬀect should be considered as a
serious contender of the error sources.
(ii) For simultaneous CZ gate operations, we show that
due to the quantum crosstalk, the performance of simultaneous CZ gate operations can be almost an order of
magnitude worse than that of the isolated case (see Fig. 8).
We further illustrate the exact nature of these quantum
crosstalks, i.e., residual NNN interactions with small coupling strength, and argue that although unwanted NN
interactions are nominally turned oﬀ, sub-MHz parasitic
NNN interactions involving spectator qubits (enabled by
high-order processes) can still exist. To mitigate their
impact on simultaneous two-qubit gate operations, we
show that engineering system parameters (e.g., pushing
these parasitic NNN interaction points away from the
system working point) (see Fig. 10) or implementing
short-time gate operations (see Fig. 12) could mitigate
the quantum crosstalk impact on simultaneous gate operations. However, in contrast, gate operations with a
slower speed can, in general, suppress unwanted interactions within target qubit systems. Hence, we argue
that for high-ﬁdelity simultaneous gate operations, this
could give rise to a trade-oﬀ between the error resulting from target qubit systems themselves and the error
from nonparticipating spectator qubits (see Fig. 12).
More strikingly, this trade-oﬀ suggests that even without the consideration of qubit decoherence error, gate
operations with slower speeds do not always show better
performance.

020301-2

## PDF page 3

QUANTUM CROSSTALK ANALYSIS. . .

PRX QUANTUM 3, 020301 (2022)

Overall, the analysis presented in this work shows that
isolated gate performance, especially, obtained with all
nonparticipating spectator qubits in their ground states,
cannot capture its true performance for the realistic situation in which gates are implemented simultaneously.
Towards a functional quantum processor, the performance of quantum processors should be examined carefully in the context of simultaneous gate operations.
The analysis can improve our understanding of the
exact nature of quantum crosstalk and its impact on
simultaneous gate operations, thus may also pave the
way for ﬁguring out crosstalk mitigation schemes and
qubit-architecture
designs
with
low
crosstalk.
Additionally, the result of this analysis also suggests that
the proposed qubit architecture may be a promising architecture towards a large-scale superconducting quantum
processor with low crosstalk.
This paper is organized as follows. In Sec. II, we introduce our qubit architecture and give a detailed description
of the gate operation in this qubit architecture. In Sec. III,
we numerically study the performance of simultaneous
gate operations (i.e., simultaneous single-qubit and twoqubit gate operations) in the qubit architecture introduced
in Sec. II, analyze the leading error source (i.e., quantum crosstalk) of the added error for the parallel implemented gate operations, and show how to mitigate quantum crosstalk impact on gate operations. In Sec. IV, we
give conclusions of our investigation.

qubit-subspace, notation |Q1 Q2 ⟩ is used),
H=

]
∑[ †
ηl † †
ωl al al + al al al al
2
l
]
∑[
†
gn (a†n aTB + an aTB ) ,
+

(1)

n

where the subscript l ∈ {1, 2, TB} labels lth oscillator
{Q1 Q2 TB} with anharmonicity ηl and frequency ωl ,
†
al (al ) is the associated annihilation (creation) operator,
and gn (n = 1, 2) denotes the strength of the coupling
between qubit Qn and the tunable bus. The qubit-bus coupling can mediate an eﬀective ZZ coupling between qubits,
which is deﬁned as
ζZZ ≡ (E11 − E10 ) − (E01 − E00 ),

(a)

(2)

(b)

ZZ

Q1

Q2
2

1

TB

Q1

TB

Q2

(c)

II. FIXED-FREQUENCY QUBIT
ARCHITECTURES WITH TUNABLE BUSES
In this section, we propose a qubit architecture
comprising ﬁxed-frequency transmon qubits coupled via
a tunable bus, as shown in Fig. 1(b). We ﬁrst focus speciﬁcally on this single building block and show how qubit-bus
coupling can enable a high-contrast ZZ interaction. Therefore, high ﬁdelity single-qubit gates can be achieved with
suppression of ZZ crosstalk, and a sub-100-ns CZ gate can
be realized when we switch on the ZZ interaction between
qubits. Then, we consider scaling up this building block to
scalable two-dimensional (2D) qubit grids.

A. System Hamiltonian and tunable ZZ coupling
Here, we consider a system of two transmon qubits
depicted in Fig. 1(b), where two transmon qubits Q1,2
are coupled through a tunable bus (TB) (a third ancilla
frequency-tunable transmon qubit). The full system can be
modeled by a chain of three weakly anharmonic oscillators [59] with nearest-neighboring coupling, and can be
described by (hereafter ℏ = 1, notation |Q1 TB Q2 ⟩ represents states of the full system, and when restricted to the

FIG. 1. (a) Sketch of a coupled two-qubit system (Q1,2 )
with tunable ZZ interaction ζZZ enabled by the tunable bus
(TB). (b) Circuit diagram of two ﬁxed-frequency transmons
coupled via a frequency-tunable transmon (treated as a tunable bus). (c) ZZ coupling ζZZ as a function of bus frequency ωTB for the qubit system illustrated in (b) with qubit
frequency ω1(2) /2π = 5.000(5.200) GHz, anharmonicity η1 =
η2 = ηTB = η (η/2π = −300 MHz), and qubit-bus coupling
g1(2) = g (g/2π = 25 MHz) (at ω1(2) = ωTB = 5.500 GHz). The
blue-solid and orange-dashed lines represent the numerical and
perturbational results, respectively. The red arrow indicates the
working point where a strong ZZ coupling exists due to the resonance interaction |101⟩ ↔ |020⟩ (as shown in the inset outlined
with the red line), and gray arrow shows the ZZ-free point resulting from the destructive interference of ZZ contributions from
interactions |101⟩ ↔ {|200⟩, |002⟩, |020⟩} (as shown in the inset
outlined with the gray line). To ensure high-ﬁdelity single-qubit
addressing, besides the residual ZZ crosstalk, the cross-driving
crosstalk due to qubit state dressing should also be taken into
consideration (see Sec. II B for details). In light of this, the system idle point is typically 500 MHz above the qubit in frequency,
marked by the black arrow.

020301-3

## PDF page 4

PENG ZHAO et al.

PRX QUANTUM 3, 020301 (2022)

where 1(2) = ω1(2) − ωTB , and  = ω2 − ω1 denote the
qubit-bus detuning and qubit-qubit detuning, respectively.
In the above expression for ZZ coupling strength, the
ﬁrst two terms result from the interaction |101⟩ ↔
{|200⟩, |002⟩}, and the ﬁnal one contributes from interaction |101⟩ ↔ |020⟩ [50,63].
We ﬁrst consider how to suppress ZZ coupling at the
system idle point, where single-qubit gates can be implemented with suppression of ZZ crosstalk. From Eq. (3),
one can ﬁnd that ZZ-free point, i.e., ζZZ = 0, is independent of the qubit-bus coupling strengths. Assuming
η1 = η2 = ηTB = η and considering ω1 ≃ ω2 , the ZZ-free
point is at 1(2) ≃ 3η/2, where the qubit-bus detuning
has a magnitude similar to that of qubit anharmonicity
[64]. For transmon qubits with a typical anharmonicity
of 300 MHz and operated in the dispersive regime (i.e.,
|1(2) | ≥ 10g1(2) ), this means that to suppress residual ZZ
interaction, the qubit-bus coupling strength should take
a value far less than that of the conventional qubit-bus
coupling, the strength of which is typically 100 MHz
[60,63]. Note here that although qubit systems can, in principle, operate in the nondispersive regime (i.e., |1(2) | ≪
10g1(2) ), single-qubit addressing and eliminating unwanted
parasitic interactions, such as NNN coupling, may become
highly nontrivial [64].
Thus, below, we consider that the qubit-bus coupling
strength takes the value g1(2) /2π = g/2π = 25 MHz,
which is similar to the qubit-qubit coupling strength in the
conventional qubit architecture with ﬁxed direct coupling
[27]. In this way, at the idle point, where the qubit system
operates in the dispersive regime, both the qubit addressing
error and unwanted parasitic interaction could be suppressed heavily. However, one may doubt that how this
rather small qubit-bus coupling can enable a bus-mediated
interqubit interaction with adequate strength for implementing a successful two-qubit gate. Figure 1(c) shows
the ZZ coupling strength versus bus frequency with qubit
frequency ω1(2) /2π = 5.000(5.200) GHz, anharmonicity
η1 = η2 = ηTB = η (η/2π = −300 MHz). The observation is that the destructive interference of ZZ coupling contributions from interactions |101⟩ ↔ {|200⟩, |002⟩, |020⟩}
[see Fig. 1(c), the inset outlined with the red line] gives
rise to a ZZ-free point at frequency ωTB /2π = 5.475 GHz,

B. Gate operation
The above illustration shows that the proposed qubit
architecture is promising to achieve high-contrast ZZ
interactions in several diﬀerent parameter regions. Such
30
20
10
0

ωT B = ω1

−10
−20
−30
−2

−1

ω2

+ ω1

=2

ωT B

+η

ωT

0

1

B

=

ω2
101

100

|ζZZ |/2π (MHz)

(3)

ω2 = ω1 − η

]

ω2 = ω1

1
1
− 2
2
2 ( − η1 ) 1 ( + η2 )
[
]
2g12 g22
1 2
1
+
,
+
1 + 2 − ηTB 1 2

ω2 = ω1 + η

[

ζZZ = 2g12 g22

where the qubit-bus detuning is comparable to the qubit
anharmonicity. This conﬁrms the perturbational analysis
given above. When biasing the bus at frequency ωTB /2π ≃
5.250 GHz, there exists a ZZ coupling with a strength
of 10 MHz, which is adequate and suitable for implementing a sub-100-ns CZ gate. This ZZ interaction mainly
results from the resonance interaction |101⟩ ↔ |020⟩ [see
Fig. 1(c), the inset outlined with gray line] at the working
point ωon = ω̄ − ηTB /2, where ω̄ = (ω1 + ω2 )/2 denotes
the mean qubit frequency.
In addition, by ﬁxing Q1 ’s frequency at 5.000 GHz,
Fig. 2 shows the ZZ coupling strength ζZZ (data points with
ZZ coupling strengths below 10 kHz are removed) as a
function of qubit-qubit detuning  and bus-qubit detuning. One can ﬁnd that suppression of ZZ coupling can be
achieved in several parameter zones, such as the straddling
regime (i.e., qubit-qubit detuning |1(2) | < |η1(2) |) [44,64],
and out of the straddling regime with one qubit above and
one qubit below the bus in frequency. Moreover, contrary
to the conventional qubit-bus system [44], one can ﬁnd
that for systems operated out of the straddling regime with
qubits below or above the bus in frequency, ZZ interaction can still be heavily suppressed. This is to be expected,
because in the present qubit system, the qubit-bus coupling
is far smaller than that of the conventional case.

Bus-qubit detuning (ωTB − ω1)/g

where Ejk denotes the eigenenergy of the system associ˜ which is adiabatically
ated with dressed eigenstate |jk⟩,
connected to the bare state |j 0k⟩. According to the fourthorder perturbation theory [61], this eﬀective ZZ coupling
can be approximated as [44,47,62]

10−1

2

10−2

Qubit-qubit detuning Δ/η

FIG. 2. ZZ coupling ζZZ (data points with ZZ coupling
strengths below 10 kHz are removed) as a function of qubitqubit detuning and bus-qubit detuning, where the frequency of
Q2 is ﬁxed at ω1 /2π = 5.000 GHz. Other system parameters are
the same as those used in Fig. 1(c). Vertical cut (orange dashed
line) denotes the result plotted in Fig. 1(c), and open black square
marks the working point at ωon = ω̄ − ηTB /2 with the mean qubit
frequency ω̄ = (ω1 + ω2 )/2.

020301-4

## PDF page 5

QUANTUM CROSSTALK ANALYSIS. . .

PRX QUANTUM 3, 020301 (2022)

ﬂexibility in the choice of parameters can potentially be
used to explore various possible advantages for implementing a scalable quantum processor. In the following
discussion, we focus speciﬁcally on the straddling regime,
i.e., || < |η|.

For illustration purposes, here we consider a microwave
driving with a constant amplitude applied to Q1 in the
two-qubit system described by Hamiltonian in Eq. (1),
intending to implement a single-qubit gate on Q1 . The
driven Hamiltonian can be described by

1. Single-qubit gate

Hd = [x (t) cos(ωd t) + y (t) sin(ωd t)](a1 + a1 ),

†

As usual, the ZZ-free point is chosen as the system
idle point, thus single-qubit gates can be implemented
without the detrimental eﬀect from residual ZZ interaction. However, we note that for microwave-activated
single-qubit gates, while residual ZZ coupling is eliminated, there can exist another error source, i.e., crossdriving error. The cross-driving error describes a phenomenon that microwave driving applied to one qubit can
cause unintended driving on the others [21,42]. This can
be due to classical microwave crosstalk or qubit-statedressing- (resulting from interqubit coupling) induced
quantum crosstalk. Here, we restrict ourselves to the last
case. Unlike the cross-driving eﬀect resulting from classical microwave crosstalk, the qubit-dressing-induced one
can create a nonlocal coherent error on coupled qubits. The
exact nature of this cross-driving eﬀect is essentially the
same as the cross-resonance (CR) interaction [21,65,66],
and CR interaction can be seen as a special cross-driving
eﬀect, where one intends to maximize the “nonlocal coherent error,” thereby, enabling the implementation of a
two-qubit gate, i.e., CR gate.
Similar to the classical microwave crosstalk, when we
focus on an individual qubit, the dressing-induced cross
driving can excite qubits, causing unintended single-qubit
rotation or leakage out of the qubit subspace. This can
result in a substantially large gate error, especially when
considering the qubit system operated near the frequency
collision regions [56,67]. As shown in Fig. 3, there are
three main types of frequency collisions: (type 1) when
the frequencies of two coupled qubits are close to the
on-resonance condition, the cross driving between qubits
can cause transition within computational subspace, leading to unintended single-qubit rotations; when one qubit’s
frequency is nearly on resonance with the frequency of
two-photon transition |0⟩ ↔ |2⟩ (type 2) or high-level transitions |1⟩ ↔ |2⟩ (type 3) of others, the cross driving can
result in population leakage out of qubit subspace.
Two-qubit unit cell

with d (t) ≡ x (t) + iy (t), where d (t) =  denotes
the driving amplitude, and ωd is the driving frequency.
Similar to the CR interaction, the cross driving from Q1
to Q2 is dependent on the state of Q1 . By diagonalizing the
undriven system Hamiltonian (at the idle point) in Eq. (1),
one can obtain the dressed eigenstate | ˜
jk⟩. Then, rewriting the driven Hamiltonian Eq. (3) in terms of the dressed
eigenstate, one can obtain strength of the cross driving
from Q1 to Q2 (similar analysis can also be applied to the
cross driving from Q2 to Q1 ). For example, the strength of
the cross driving from Q1 to Q2 can be approximated as
J
,

J ( + η1 )
˜ 10↔11 ≃

,
( − η1 )
√
2J 
˜ 01↔02 ≃

,
 + η2
√
2J ( + η1 + η2 )
˜ 11↔12 ≃

,
( − η1 + η2 )( + η2 )
˜ 00↔01 ≃


(5)

˜ 0j ↔0k and 
˜ 1j ↔1k denote the cross driving applied
where 
to Q2 ’s transitions |j ⟩ ↔ |k⟩ for Q1 in the ground and
excited states, respectively [68], and J denotes the eﬀective
bus-mediated exchange coupling, which can be approximated as J = (g1 g2 /2)(1/1 + 1/2 ).
Similar to the characterization of classical microwave
crosstalk, we can deﬁne the crosstalk strength of this
˜ . Moreover,
dressing-induced cross driving as β ≡ /
to quantify the cross-driving-induced gate error, here we
also introduce the worst-case population error (since oﬀresonance driving can cause incomplete Rabi oscillation,
here we choose the maximum population amplitude as
an indicator of the gate error and set /2π = 25 MHz)
deﬁned as
ϵ≡

Collison condions Unwanted transions

FIG. 3. Qubit frequency collision conditions and their associated unwanted transitions.

(4)

˜2

˜ 2 + δ2


,

(6)

where δ denotes the detuning between the cross-driving
frequency and qubit’s transition frequencies between different energy levels.
To ensure high-ﬁdelity single-qubit gates, the crossdriving eﬀect should be minimized. From the expression
given in Eq. (5), this can be achieved by reducing exchange

020301-5

## PDF page 6

PENG ZHAO et al.

PRX QUANTUM 3, 020301 (2022)

10−1
00 ↔ 01
01 ↔ 02
10 ↔ 11
11 ↔ 12

00 ↔ 10
10 ↔ 20
01 ↔ 11
11 ↔ 21

10−2
(−40 dB)

10−3

10−4

00 → 01
01 → 02
10 → 11
11 → 12

(b)

10−3

00 → 10
10 → 20
01 → 11
11 → 21

10−6

10−5

10−6

5.40

5.50
5.60
5.70
ωTB/2π (GHz)

5.80

5.40

5.50
5.60
5.70
ωTB/2π (GHz)

5.80

5.40

10−1
10−4

10−2
(−40 dB)

10−3

10−3

(e)

5.50
5.60
5.70
ωTB/2π (GHz)

5.80

(f)

10−4

1−F

(d)
Population error

Crosstalk strength β

Added error per qubit
Q1 context error
Q2 context error
Leakage per qubit
Average isolated gate error ε̄sum

10−8

(−60 dB)

(−20 dB)

(c)

10−4

1−F

(a)

Population error

Crosstalk strength β

(−20 dB)

10−6

10−5

10−8
10−6

(−60 dB)

100
150
200
250
Qubit-qubit detuning Δ/2π (MHz)

100
150
200
250
Qubit-qubit detuning Δ/2π (MHz)

100
150
200
250
Qubit-qubit detuning Δ/2π (MHz)

FIG. 4. (a)–(c) Dressing induced cross-driving eﬀect between coupled qubits Q1(2) versus bus frequency with other system parameters the same as those used in Fig. 1. (d)–(f) Cross-driving eﬀect versus qubit-qubit detuning  with bus frequency ωTB /2π =
5.650 GHz and qubit frequency ω1 /2π = 5.000 GHz. Other system parameters are the same as in Fig. 1. For coupled qubits Q1(2) ,
˜
when a microwave driving with strength  is applied to one qubit, the nearby qubit can also be felt by driving with amplitude 
(i.e., cross driving), which is dependent on qubit states. (a),(d) Crosstalk strength between coupled qubits, deﬁned as β ≡ ˜
/ . Here,
0j ↔ 0k and 1j ↔ 1k label the cross driving applied on the transition |j ⟩ ↔ |k⟩ of Q2 with Q1 in its ground state and excited state,
respectively. Similarly, j 0 ↔ k0 and j 1 ↔ k1 label the cross driving applied on the transition |j ⟩ ↔ |k⟩ of Q1 with Q2 in its ground
state and excited state, respectively. (b),(e) Worst-case population error caused by cross driving. Here, 0j → 0k (1j → 1k) labels the
worst-case population on |k⟩ of Q2 , where Q2 is prepared in state |j ⟩ and the Q1 is in its ground state (excited state). (c),(f) Single-qubit
gate error (1 − F) under the inﬂuence of the cross-driving eﬀect between qubits.

coupling J and avoiding the qubit frequency collisions
shown in Fig. 3. Figures 4(a) and 4(b) show the crosstalk
strength β between Q1 and Q2 , and the cross-drivinginduced population error versus bus frequency. One can
ﬁnd that both the crosstalk strength and the population
error are indeed decreased as we increase the bus frequency. In Figs. 4(d) and 4(e), we also show the crosstalk
strength and the population error versus qubit-qubit detuning . We ﬁnd that the crosstalk strength itself is dependent on the detuning , and it is also highly asymmetric
[also see Fig. 4(a)]. For example, for qubits with lower
frequency, i.e., Q1 , the cross driving from Q2 (with a
higher qubit frequency) to Q1 becomes notable when Q2
˜ ↔ |11⟩).
˜
is in the excited state (e.g. |01⟩
Meanwhile, the
crosstalk from Q1 to Q2 especially tends to give leakage
out of qubit subspace (e.g., | ˜
11⟩ ↔ | ˜
12⟩ and | ˜
01⟩ ↔ | ˜
02⟩).
Nevertheless, as shown in Fig. 4(e), on the whole, the
cross-driving impact on gate ﬁdelity can still be captured
by the frequency collision analysis.
(i) For coupled qubits with small qubit-qubit detuning, the system approaches type-1 frequency collision,
thus the dominated error from cross driving is unintended

single-qubit rotations, whereas the leakage error is
suppressed.
(ii) When qubit-qubit detuning approaches the anharmonicity of qubits, i.e., the type-3 frequency collision,
the cross-driving-induced leakage error is dominated and
unintended rotation is greatly reduced. This suggests a
fundamental trade-oﬀ between control error and leakage
error.
(iii) The type-2 frequency collision seems to have less
impact on gate performance [69]. This is reasonable since
the type-2 frequency collision involves a second-order process that tends to be orders of magnitude weaker than that
of type 1 and type 3.
In the discussion given above, the population error is
just a rough estimation of the cross-driving-induced gate
error [70]. In practical implementations of single-qubit
gates, rather than using a constant magnitude driving, one
commonly uses a shaped pulse, e.g., derivative removal
by adiabatic gate (DRAG) pulse [3,4,71], thus suppressing
leakage out of qubit subspace. In the following discussion,
to implement a single qubit X gate, we consider using
a DRAG scheme with a 20-ns cosine-shaped pulse [3],

020301-6

## PDF page 7

QUANTUM CROSSTALK ANALYSIS. . .

PRX QUANTUM 3, 020301 (2022)

˙ x (t)/η, where x (t) =
given as DRAG (t) = x (t) − iα 
A[1 − cos(2π t/tg )]/2, tg is the gate time, A is the peak
pulse amplitude (for tg = 20 ns, A/2π ≃ 50 MHz), α is
a free parameter that is chosen to suppress leakage error
(see Appendix A 1 for details on the calibration procedure
of X gates) [3,4,71].
To give a more exact characterization of the crossdriving impact on single-qubit gates, we consider the
following virtual experiment: (1) First, an isolated singlequbit gate on qubit Q1(2) is tuned up and characterized
with the other qubit in its ground state, giving rise to the
isolated gate ﬁdelity, i.e., F■0 (here the subscript denotes
the state bitstring |■0⟩, and for the active target system to
which a gate operation is applied, its qubit state is labeled
by ■) for Q1 and F0■ for Q2 . (2) Then, the same gate is
recharacterized with the other qubit in its excited state,
giving rise to F■1 for Q1 and F1■ for Q2 . (3) Finally,
we consider that both gates are implemented simultaneously, characterization of this composite gate, i.e., X ⊗ X,
gives rise to the gate ﬁdelity FX⊗X . Here, we deﬁne Q1
(Q2 ) context error |F■0 − F■1 | (|F0■ − F1■ |) to characterize the cross-driving impact on isolated single-qubit gates,
and deﬁne added error per qubit (F■0 F0■ − FX ⊗X )/2 for
simultaneous single-qubit gate operations.
To quantify the eﬀect of cross driving on the gate performance, we use the metric of gate ﬁdelity given as (without
qubit decoherence) [72]
F=

Tr(Ũ† Ũ) + |Tr(U† Ũ)|2
,
d(d + 1)

(7)

where U and Ũ denote the target gate operation and implemented gate operation, respectively, and d represents the
system dimension. In Figs. 4(c) and 2(f), we show the
ﬁdelity of X gate as a function of bus frequency and
qubit-qubit detuning, respectively. Similar to the result
shown in Figs. 4(b) and 4(e), one can ﬁnd that reducing
exchange coupling J indeed suppresses the cross-driving
eﬀect on single-qubit gates, and a non-negligible gate error
of about 0.002%–0.1% (given the state-of-the-art singlequbit gate error approaching 0.01% [3,4]) appears when
the qubit-qubit detuning approaching type-1 or type-3 frequency collision region. To identify the nature of the added
error, we also show the added leakage error per qubit [73].
As shown in Fig. 4(f), for qubit-qubit detuning near the
type-3 frequency collision, the leakage error is indeed the
dominated error source, accounting for the added error during simultaneous gate operations. Moreover, the context
error also coincides with the leakage, this is true since
leakage out of qubit-subspace can occur only when the
cross-driven qubit is in the excited state. In contrast, the
context error and leakage errors are far less important near
the type-1 frequency collision region, in which the dominated error is the unintended single-qubit rotations, e.g.,
under- or over-rotation (bit-ﬂip error) and an additional

single-qubit phase error (phase error) when one focuses on
each individual qubit.
In addition, it is worth mentioning that under our
deﬁnition of gate characterization, we always assume that
the other nearby qubit is in the ground or excited state,
thereby, the cross-driving-induced ﬂip of nearby qubit
states contributes to errors of the isolated single-qubit gate,
i.e., leading to leakage error. Therefore, the added error
per qubit cannot capture the cross-driving-induced singlequbit rotation error. As shown in Fig. 4(f), near the type-1
frequency collision region, although the added error per
qubit is rather small, the averaged isolated single-qubit
error ε̄sum = (F■0 + F0■ )/2 is far larger than that for the
type-3 frequency region. As we mentioned before, when
the qubit system works nearby the type-1 frequency collision region, the cross-driving eﬀect can lead to unintended
single-qubit rotations on one qubit when single-qubit operations are applied to its neighboring qubits. This explains
the increase in average gate error ε̄sum when decreasing qubit-qubit detuning. We thus argue that restricted
totally to the isolated single-qubit system regardless of
nearby qubits states, i.e., tracing out nearby qubits, one
can achieve only a nominally high-ﬁdelity single-qubit
gate, which cannot account for its practical performance
on multiqubit systems.
Overall, for the present system operated in the straddling regime, the dressing from the qubit-qubit coupling
can induce a substantial cross-driving eﬀect, and the associated crosstalk strength [as shown in Figs. 4(c) and 4(d),
typically, from −40 dB to −20 dB] is comparable with
that of classical microwave crosstalk [42,74]. For systems
with small qubit-qubit detuning (i.e., near the type-1 frequency collision region), cross-driving favors bit-ﬂip error
or phase error, whereas, for large detuning cases (i.e.,
near the type-3 frequency collision region), cross driving tends to cause leakage error. To ensure high-ﬁdelity
single-qubit addressing, the bus-qubit detuning should be
large enough, thus bus-mediated exchange coupling is suppressed, and the qubit-qubit detuning should also be away
from the frequency collision regions, especially for type 1
and type 3 [69]. Note here that, in principle, the direct coupling between qubit and bus can also cause cross driving
from qubit to bus. However, according to Eqs. (5) and (6),
one can ﬁnd ϵ ∝ 1/3 , thus, here, the cross-driving eﬀect
on the bus is heavily suppressed by the large qubit-bus
detuning. This is checked for the present system and is
found to be less important.
2. Two-qubit gate
As demonstrated in Sec. II A, for the present qubit architecture operated in the straddling regime, a high-contrast
control over ZZ interaction can be achieved. When tuning
the system energy level |101⟩ on resonance with |020⟩, i.e.,
biasing the bus to the working point at ωon = ω̄ − ηTB /2,

020301-7

## PDF page 8

PENG ZHAO et al.

PRX QUANTUM 3, 020301 (2022)

a sub-100-ns CZ gate can be achieved by using a diabatic
scheme [6,75] or a fast-adiabatic scheme [9,76–78]. In
principle, during the idle time, the system (tunable bus) can
be biased to the exact ZZ-free point. However, as discussed
in Sec. II B 1, to have a high-ﬁdelity single-qubit addressing, besides residual ZZ crosstalk, the cross-driving eﬀect
should also be minimized. Thus, here the system idle point
is chosen so that the typical bus frequency is 500 MHz
above the qubit in frequency. In this way, the residual ZZ
coupling can still be suppressed below 10 kHz, as shown
in Figs. 1(c) (marked by the black arrow) and 2. Moreover,
to avoid the harmful frequency collision in the straddling
regime, the qubit-qubit detuning should be located within
speciﬁc limits, e.g., 100–200 MHz, thereby, the singlequbit gate error can be pushed below 0.01% (or even
approaches 0.001%), as shown in Fig. 4(f).
In the present qubit architecture, to implement a successful two-qubit gate, several practical experimental limitations also need to be considered seriously.
(1) Uncertainty of system parameters due to fabrication.
This is one of the most critical issues faced by ﬁxedfrequency qubits. As shown in Fig. 2, both the available
ZZ-free zone (where the ZZ coupling strength is below
10 kHz), and the available working zone (where resonance
interaction |101⟩ ↔ |020⟩ gives rise to a ZZ coupling with
strength about 10 MHz, indicated by black-dashed line
labeled by ω1 + ω2 = 2ωT B + η) in the straddling regime
show a promising insensitivity against variation of qubitqubit detuning and qubit-bus detuning. Thus, the parameter
uncertainty issues could be largely ﬁxed by combing this
parameter insensitivity and the state-of-the-art fabrication
techniques [79,80].
(2) Gate error resulting from qubit relaxation and
dephasing. Although ﬁxed-frequency transmon qubit itself
can have a long coherence time, qubit relaxation rate or
dephasing rate can be enhanced through the tunable bus,
which is more vulnerable to system noise, especially, 1/f
ﬂux noise. Moreover, during the CZ gate operation, a baseband ﬂux pulse is commonly applied to the tunable bus,
tuning its frequency from the idle point to the working
point. Considering the qubit system shown in Fig. 1, at
the working point, the qubit-bus detunings are 1 /2π =
−250 MHz and 2 /2π = −50 MHz. We expect that the
small qubit-bus detuning at the working point can cause a
strong hybrid between qubit and bus (qubit-bus dressing),
especially for Q2 , thus the qubit relaxation and dephasing
through the bus can become greatly serious [9,60,77,78].
For the 1/f noise-induced dephasing, this can be mitigated
by employing a tunable bus, whose maximum frequency
point (i.e., ﬂux-insensitive point) is around the idle point.
Therefore, at the idle point, the qubit dephasing through
the bus is reduced. Moreover, during CZ gate operations,
the needed frequency excursion of the bus is smaller
than 500 MHz, thereby potentially greatly reducing ﬂux
sensitivity of bus and mitigating the eﬀect of 1/f ﬂux

noise [15,81] (in principle, this could be further improved
by using tunable buses with asymmetric superconducting
quantum interference device (SQUID) [82]).
(3) Flux pulse distortion. Flux pulse distortion is a
critical problem faced by baseband ﬂux-controlled gate
operations. The presence of ﬂux pulse distortion can cause
a substantial gate error, such as leakage error and gate
bleedthrough, during CZ gate operations [27,69,76,81].
Although pulse distortion can be largely corrected, one
needs to characterize it at ﬁrst [27]. Unfortunately, in general, one cannot directly characterize this distortion without control and measurement of the system subjected to
pulse distortion. In qubit architectures with tunable buses
or couplers, the bus or coupler, in general, does not have
a dedicated driving line and readout resonator. Still, one
can put these back, but it will greatly increase circuit complexity [8]. Commonly, due to the presence of (classical or
dressed-induced) microwave crosstalk, the bus or coupler
can be addressed through the driveline of nearby qubits.
However, the readout of bus or coupler state through the
readout resonator of nearby qubits is still a challenge.
One possible strategy is that combined with the readout of
nearby qubits, full control on the bus could be achieved
through the qubit-bus interaction [83–85], then the distortion could be corrected [27,86,87]. Meanwhile, in the
present qubit architecture, the frequency excursion of the
bus is small, thereby potentially mitigating the eﬀect of
ﬂux setting tails caused by pulse distortion [81,88].
In the present work, we consider that during the CZ gate
operation, a fast-adiabatic pulse is applied to the tunable
bus, tuning its frequency from the idle point (θi ) to the
working point ωon (θf ) and then back. Expressed in terms
of Fourier basis functions, the pulse shape is described as
[76]
θ (t) = θi +

[
]
θf − θi ∑
2nπ t
λn 1 − cos
,
2 n=1,2,3···
T

(8)

with constraints on the odd coeﬃcients n odd λn = 1, and
control angle θ ≡ arctan(2J101 /101 ), where J101 denotes
the strength of resonance interaction |101⟩ ↔ |020⟩, 101
represents the detuning between |101⟩ and |020⟩, and T is
the gate time.
C. Scaling up to two-dimensional qubit grids
In principle, the above two-transmon-qubit system can
be exploited as building blocks of scalable qubit architectures. An illustration of a 2D qubit lattice, where
each transmon qubit is coupled to four nearest neighbors
through tunable buses, is shown in Fig. 5(a). In the 2D
qubit lattice, the allocation of qubit and bus frequency
follows the following rules.
(1) The frequency of the qubit in each row and column belongs to one of the two frequency bands, i.e.,

020301-8

## PDF page 9

QUANTUM CROSSTALK ANALYSIS. . .

PRX QUANTUM 3, 020301 (2022)

(a)

Frequency

/ 2 (GHz)

(c)

5.000
(4.700)

5.20

Qubit
5.00

5.650

5.720

(5.350)

5.72

(5.420)

5.70
Tunable
Bus

25 25

5.68

(b)

/2 (MHz)

/2 (GHz)
/2 (GHz)

25

25

25

25

25
25

5.180

5.65

(4.880)

25 25

25

25

5.000

5.200

5.050

5.220

(4.700)

(4.900)

(4.750)

(4.920)

25

5.200

25

(4.900)
2

5.680

5.700

(5.380)

(5.400)

5.700

5.650

5.705

5.020

(5.400)

(5.350)

(5.405)

(4.720)

FIG. 5. (a) Layout of a two-dimensional qubit lattice, where cross-shaped vertices (steel blue) denote qubits, and strip-shaped edges
(orange) between adjacent qubits represent tunable buses. Qubits in the lattice belong to one of the two frequency bands, i.e., a
lower frequency band with typical frequency ω/2π = 5.000 GHz (light steel blue) or a higher frequency band with typical frequency
ω/2π = 5.200 GHz (dark steel blue). The typical detuning between nearby qubits is about 200 MHz, and at the idle point, the bus
frequency is typically above 500 MHz of the qubits in the higher frequency band. Example of system parameters of four-qubit chain
and 2 × 2 four-qubit square shown in the gray shadow of (a) is presented in (b),(c), respectively, e.g., for Q0 in the four-qubit chain
shown in (b), the qubit frequency is ωQ /2π = 5.000 GHz, and its anharmonicity is −300 MHz (i.e., its transitions frequency between
|1⟩ and |2⟩ is 4.700 GHz), the interaction between qubit Q0 and bus TB0 is g/2π = 25 MHz (at ωQ /2π = ωTB /2π = 5.500 GHz).

a lower frequency band with typical frequency ω/2π =
5.000 GHz and a higher frequency band with typical
frequency ω/2π = 5.200 GHz, and qubits in the nearby
row or column belong to diﬀerent frequency bands. Thus,
typical detuning between NN qubits is about 200 MHz,
which is adequate to mitigate cross-driving eﬀect at idle
point (Sec. II B) and to implement a sub-100-ns CZ
gate, as demonstrated in Sec. II A. Moreover, to mitigate microwave crosstalk impact on qubit addressing
between next-nearest-neighbor qubits [27,69] at the idle
point and suppress NNN coupling between qubits at the
idle and the working point, frequency degeneracy in the
lower- or higher-frequency band breaks, yielding typical
qubit detuning between next-nearest-neighbors of about
20 MHz.
(2) To have a better balance between the requirement for
suppressing qubit-qubit residual interaction and to limit the
frequency excursion range during CZ gate operations, the
bus frequency is typically above 500 MHz of the qubit in
the higher-frequency band, as shown in Fig. 5(a).
When considering a practical realization of this qubit
lattice, frequency uncertainty due to fabrication is the most
critical issue, as discussed in Sec. II B 2. Besides striving to improve qubit device fabrication precision [79,80],
one could also try to adopt more sparse qubit connections
towards large-scale qubit lattice [80].
III. QUANTUM CROSSTALK ANALYSIS FOR
SIMULTANEOUS GATE OPERATIONS
In this section, we give a quantum crosstalk analysis for
simultaneous gate operations on two four-qubit systems

shown in Figs. 5(b) and 5(c), where system-speciﬁc parameters are also presented. Similar to the discussion in
Sec. II B 1, to characterize the quantum crosstalk eﬀect on
gate performance, we use the metric of gate ﬁdelity given
in Eq. (7). The isolated gate ﬁdelity is obtained by characterizing each gate operation individually with all other
nonparticipating spectator qubits at their ground states, and
the simultaneous gate ﬁdelity is obtained by characterizing
the parallel implemented gate operations (see Appendix A
for details on the calibration procedure). To have enough
sensitivity to the added error caused by quantum crosstalk
during simultaneous gate operations, each isolated gate
is optimized numerically, giving typically isolated singlequbit gate error at 10−6 and typical two-qubit CZ gate error
at 10−5 . Note here that we do not attempt to search for an
optimal isolated gate operation with the lowest error, but
only for gate operations with enough ﬁdelity, thus enabling
an adequate crosstalk sensitivity.
In addition, we note here that in the following discussion, notations |Q0 Q1 Q2 Q3 , TB0 TB1 TB2 TB3 ⟩ and
|Q0 Q1 Q2 Q3 , TB0 TB1 TB2 ⟩ represent states of the fourqubit square and four-qubit chain system, respectively.
When conﬁned to qubit subspace, notation |Q0 Q1 Q2 Q3 ⟩
is used.
A. Simultaneous single-qubit X -gate operations
Here, we consider that two 20-ns single-qubit X gates
are applied simultaneously to the arbitrary qubit pair of the
four-qubit system, i.e., implementing a composite X gate
(X ⊗ X ). All tunable buses are tuned to their idle points,
thus residual ZZ interaction between qubits is suppressed

020301-9

## PDF page 10

PENG ZHAO et al.
(a)

PRX QUANTUM 3, 020301 (2022)
(b)

FIG. 6. Gate error of simultaneous single-qubit X gates (i.e.,
composite gate X ⊗ X ) applied to an arbitrary qubit pair of (a)
the four-qubit chain system and (b) the 2 × 2 four-qubit square
system shown in Figs. 5(b) and 5(c). Elements in the upper triangular part of the error matrix denote ideal composite gate error
obtained by adding the errors of constituted isolated gates, and
elements in the lower triangular parts correspond to the gate error
of simultaneous gate operations.

below 10 kHz. Same as the discussion in Sec. II B 1, singlequbit gates are realized by using the DRAG scheme with a
cosine-shaped pulse.
Figures 6(a) and 6(b) show the error matrix of the parallel implemented X gates in the four-qubit chain system
shown in Fig. 5(b) and the four-qubit square system shown
in Fig. 5(c), respectively. Elements in the upper and lower
triangular part of the error matrix denote ideal composite gate error obtained by adding the errors of constituted isolated gates and directly characterizing the parallel
implemented gate operations, respectively. We ﬁnd that
almost no additional error is observed for the next-nearestneighbor qubits, and we thus conclude that the quantum crosstalk between next-nearest-neighbor qubits can
be neglected. However, focusing on the nearest-neighbor
qubit pairs, the performance of simultaneous gate operations is almost an order of magnitude worse than that of
the isolated case.
The above observations are consistent with the analysis
of dressing induced cross-driving eﬀect on the gate performance discussed in Sec. II B 1. As interactions between
next-nearest-neighbor qubits are commonly an order of
magnitude weaker than that of nearest-neighbor qubits,
the cross-driving eﬀect can be greatly suppressed. In contrast, the cross-driving eﬀect between nearest-neighbor
qubits cannot be ignored, and in general can cause a nonnegligible error on the simultaneous gate operations. The
error can become even more serious when the nearestneighbor qubit pair approaches the frequency collision
region. For example, focusing on the qubit pair (Q0 , Q1 )
in the chain system, the detuning between transition |0⟩ ↔
|1⟩ of Q0 and transition |1⟩ ↔ |2⟩ of Q1 (i.e., type-3 frequency collision) takes the smallest value (100 MHz)
among all nearby qubits, as marked (in pink shadow) in

Fig. 5(b). The closer to the frequency collision region, the
more serious the cross-driving error, which can explain that
simultaneous X gate on qubit pair (Q0 , Q1 ) has the worst
gate performance in the four-qubit chain system. Similar
results can also be obtained for the qubit pair (Q0 , Q3 ) in
the square system.
In addition, note that as discussed in Sec. II B 1, crossdriving-induced single-qubit rotation error has been taken
into account already for the characterization of the isolated
gate performance, and can lead to leakage error since we
always assume all the nonparticipating spectator qubit in
their ground states. However, during simultaneous singlequbit gate operations, this rotation error occurs within the
two-qubit computational subspace, thus here it does not
contribute to the leakage error but the control error for the
composite gate operation. The combination of decreased
leakage error and increased control error can explain that
for the next-nearest-neighbor qubit pair, whose detuning
approaches the type-1 frequency collision (as discussed in
Sec. II B 1, here the cross-driving eﬀect favors single-qubit
rotation error), the ideal composite gate appears to have
a little bit larger gate error than that of the simultaneous
gate operation, as shown in Fig. 6(a) (we have checked
this independency, and ﬁnd that without consideration of
leakage error, this feature indeed disappears).
To give a more concrete illustration of the crossdriving impact on the present four-qubit system, Figs. 7(a)
and 7(b) show the X gate error with the other three
spectator qubits in four diﬀerent state conﬁgurations for
the four-qubit chain and square system, respectively. Generally, we ﬁnd that compared with the isolated gate operation, gate error is increased when a state ﬂip of one nearby
qubit occurs. Moreover, qubits in the lower-frequency
band show a more prominent decrease in gate performance, such as Q0 in the two four-qubit systems. This is to
be expected, as detuning between the transition |0⟩ ↔ |1⟩
of the qubit in the lower-frequency band and the transition
|1⟩ ↔ |2⟩ of one in the higher-frequency band, typically,
100 MHz, is smaller than that in the reversed case, typically, 500 MHz. Thus, the cross-driving eﬀect from the
low-frequency qubit to the nearby high-frequency qubit is
more serious and can result in leakage error for the lowfrequency qubit. In Figs. 7(c) and 7(d), we also show the
time evolution of state population during XQ0 with one of
Q0 ’s nearby qubit in its excited state. For the four-qubit
system initialized in |0100⟩, we ﬁnd that during X gate on
Q0 , the qubit Q1 state can be excited from |1⟩ to |2⟩ [see
Figs. 7(c) and 7(d), P0200 and P1200 ], accounting for the
dominated leakage error Leak0100 ≡ 1 − (P0100 + P1100 ).
Similarly, for the four-qubit square system prepared in
|0001⟩, the leakage error Leak0001 ≡ 1 − (P0001 + P1001 )
is mainly resulted from the population leakage of Q3 [see
Fig. 7(d), dashed line]. Overall, the above analysis shows
that the dressed induced cross driving can explain the
performance degradation of simultaneous gate operations

020301-10

## PDF page 11

QUANTUM CROSSTALK ANALYSIS. . .

PRX QUANTUM 3, 020301 (2022)
eﬀect should be taken seriously into account to design and
construct a large multiqubit lattice.

(a)

B. Simultaneous two-qubit CZ gate operations
In this subsection, we turn to examine the performance
of simultaneous CZ gates in the two four-qubit systems
shown in Figs. 5(b) and 5(c). Similar to the analysis of
the single-qubit case, we consider that individual CZ gate
is tuned up and characterized with the other two nonparticipating qubits in their ground states. During gate
operations, except for the bus to which a baseband ﬂux
pulse is applied for realizing a CZ gate, the other buses
are all biased to their idle points. The CZ gate is implemented by using a fast-adiabatic pulse given in Eq. (8) with
three Fourier coeﬃcients {λ1 , λ2 , λ3 }, giving rise to totally
three free parameters {λ1 , λ2 , θf }. The other parameters
are as follows: gate time T = 68 ns, J101 /2π = 12 MHz.
For reaching a given target error at 10−5 , the three free
parameters are ﬁxed using numerical optimization (see
Appendix A 2 for details).

(b)

(c)

(d)

1. Gate performance

FIG. 7. X gate error with the other three spectator qubits
in four diﬀerent state conﬁgurations, e.g., marked by
{■000, ■100, ■010, ■001} for Q0 . (a) For the four-qubit chain
system shown in Fig. 5(b). (b) For the four-qubit square system
shown in Fig. 5(c). (c),(d) State population as a function of time
during the isolated single-qubit operations in the four-qubit chain
system and square system. Solid lines (dashed lines) denote the
result for the four-qubit system initialized in |0100⟩ (|0001⟩).
The leakages are deﬁned as Leak0100 = 1 − (P0100 + P1100 ),
Leak0001 = 1 − (P0001 + P1001 ), where Pijkl represents the
population in the four-qubit state |ijkl⟩.

applied to qubit pair (Q0 , Q1 ) in the four-qubit chain
system and (Q0 , Q3 ) in the four-qubit square system.
Before leaving this subsection, we note that although the
cross-driving eﬀect can cause almost an order of magnitude worse gate performance in the above illustration, on
average the added gate error is about 10−5 , which is an
order of magnitude lower than the state-of-the-art gate performance [3–5]. However, when qubit systems approach
the frequency collision region or have a larger interqubit
coupling at the idle point, this cross-driving eﬀect can
become a dominant error source for simultaneous singlequbit gate operations. This suggests that the cross-driving

In Figs. 8(a) and 8(b), we show simultaneous CZ gate
performance in the four-qubit chain system and four-qubit
square system. In the chain system, the added error of
simultaneous CZ gates is about 10−5 , giving an average
added error 0.5 × 10−5 for the individual CZ gate, and
in the four-qubit square system, the added error is about
2.4 × 10−4 and 1.1 × 10−4 for gate pairs {CZ01 , CZ23 } and
{CZ12 , CZ30 }, respectively, which are about an order of
magnitude larger than that of the isolated case. Given
the state-of-the-art two-qubit gate performance, although
it appears likely that the quantum crosstalk between the
gate pair {CZ01 , CZ23 } in the chain system is less important, the quantum crosstalk eﬀect on the square system can
become a near-term performance-limiting factor. Thus, in
the following discussion, we can restrict our attention to
the square system in which the quantum crosstalk eﬀect is
more prominent.
To explore the exact nature of the performance degradation, Figs. 8(c) and 8(d) show the CZ gate error with
the other two nonparticipating qubits in four diﬀerent state
conﬁgurations for the chain system and square system,
respectively. One can ﬁnd that except for CZ01 in the square
system, gate errors of all the CZ gates show only a weak
size dependence on the state of nonparticipating qubits.
Typically, here the added error is about 10−5 . However, in
the square system, when Q3 is in the excited state, the gate
error of CZ01 is increased by about a factor of 28, giving
rise to an added error of 4.5 × 10−4 .
To explain the above striking increase in the gate error,
we examine the time evolution of the square system during CZ01 with Q3 prepared in its excited state. We ﬁnd that

020301-11

## PDF page 12

PENG ZHAO et al.
(a)

PRX QUANTUM 3, 020301 (2022)
(b)

(c)

(d)

FIG. 8. Error matrix of simultaneous CZ gates in (a) the fourqubit chain system and (b) the four-qubit square system. (c),(d)
CZ gate error with the other two nonparticipating qubits in
four diﬀerent state conﬁgurations (i.e., 00, 01, 10, 11) for the
four-qubit chain system and the four-qubit square system.

the leakage error, which is caused by the high-order parasitic interaction among |1101, 0000⟩, |0002, 1000⟩, and
|0001, 2000⟩, can account for the added gate error, as
illustrated in Fig. 9(a). From the energy spectrum of the
four-qubit square system in the left panel of Fig. 9(a),
there exists two avoided crossings resulting from interaction |1101, 0000⟩ ↔ |0002, 1000⟩ and |0001, 2000⟩ ↔
|0002, 1000⟩, which are on either side of the working
point at ωon ≃ 5.240 GHz. Thus, when a ﬂux pulse
tunes the bus to the working point and then comes back
according to the fast-adiabatic pulse given in Eq. (8),
the system will ﬁrst sweep through the avoided crossing (|1101, 0000⟩ ↔ |0002, 1000⟩) at 5.2590 GHz, and
then approaches the avoided crossing (|0001, 2000⟩ ↔
|0002, 1000⟩) at 5.2305 GHz, as shown in the middle panel
of Fig. 9(a). In the right panel of Fig. 9(a), where the time
evolution of state population is presented, we ﬁnd that
leakage to |0002, 1000⟩ mainly occurs when the system
approaches the avoided crossing at 5.2305 GHz.
Before giving a more detailed analysis of the leakage error, we note that during an ideal fast-adiabatic CZ
gate operation, the qubit system should always be in
the instantaneous eigenstates of the qubit system. For
the system initialized in |1101, 0000⟩, the system dynamics should be restricted in the subspace spanned by

{|1101, 0000⟩, |0001, 2000⟩}. In light of this, the above
observation can be explained by the fact that as the ﬂux
pulse has a short-time ramp [right panel of Fig. 9(a),
black line], and the energy gap of the avoided crossing
at 5.2590 GHz is about 250 kHz, the system can thus
sweep through it with a negligible leakage to |0002, 1000⟩.
However, during the main part of the ﬂux pulse that
has a ﬂat shape, the system is almost settled at the
working point, where the instantaneous eigenstate is an
almost maximal superposition state of |1101, 0000⟩ and
|0001, 2000⟩. Moreover, the working point nears the second avoided crossing with a tiny energy gap of 500 kHz
at 5.2305 GHz, in which the detuning to the working
point is about 10 MHz. Thus, an oﬀ-resonance population swap between |0002, 1000⟩ and |0001, 2000⟩ occurs,
causing signiﬁcant leakage to |0002, 1000⟩. Note here that
during the main part of the ﬂux pulse, the oﬀ-resonance
population swap between |1101, 0000⟩ and |0002, 1000⟩
can also occur due to the avoided crossing at 5.2590 GHz.
However, as its detuning to the working point is about
20 MHz and its gap is 250 kHz, the leakage resulting
from the oﬀ-resonance interaction between |1101, 0000⟩
to |0002, 1000⟩ is expected to be far less than that from
the oﬀ-resonance interaction between |0001, 2000⟩ and
|0002, 1000⟩.
The above analysis suggests that although individual
gate operations with high gate ﬁdelity can be achieved,
implementing the gate operation in parallel can show
substantial performance degradation. Moreover, in
multiqubit systems, there can exist detrimental high-order
parasitic interactions that cannot be captured by only characterizing isolated gate operations with all other nonparticipating qubits in their ground states. In contrast, characterizing gate operations with other nonparticipating qubits at
diﬀerent state conﬁgurations may give further insight into
the quantum crosstalk behind the performance degradation
of the simultaneous gate operations [55].
2. Mitigation of parasitic interaction involving spectator
qubits
From the above, the leakage to state |0002, 1000⟩ is the
dominated error source for CZ01 with Q3 in its excited state.
Here, we intend to mitigate such errors from the hardware perspective. As the leakage is mainly caused by the
existence of the parasitic interaction (i.e., |1101, 0000⟩ ↔
|0002, 1000⟩ and |0001, 2000⟩ ↔ |0002, 1000⟩) around
the working point, here we intend to push them away from
the working point. As shown in the left panel of Figs. 9(b)
and 9(c), due to the increase of qubit anharmonicities,
the energy of state |0001, 2000⟩ is lowered, thereby, the
avoided crossings resulting from the parasitic interactions
are far away from the working point. In this way, due to
the increased detuning from state |0002, 1000⟩, the oﬀresonance population swap between state |0001, 2000⟩ and

020301-12

## PDF page 13

QUANTUM CROSSTALK ANALYSIS. . .

PRX QUANTUM 3, 020301 (2022)

Population

(a)

Population

(b)

Population

(c)

FIG. 9. (Left panel) Energy-level spectrum of the four-qubit square system shown in Fig. 5. The dashed black line indicates the
working point, and the orange (steel-blue) square marks the avoided crossing resulting from interaction |1101, 0000⟩ ↔ |0002, 1000⟩
and |0001, 2000⟩ ↔ |0002, 1000⟩, respectively, which are highlighted in the middle panel. (Right panel) Time evolution of state
population during the implementation of CZ01 with system prepared in the state |1101, 0000⟩. P1101,0000 and P0002,1000 denote the
population on state |1101, 0000⟩ and state |0002, 1000⟩. The black curves in the left panel and the right panel represent the 68-ns shaped
pulse used to realize CZ01 . (a) Qubit anharmonicities are ηQ /2π = −300 MHz. (b) Qubit anharmonicities are ηQ /2π = −310 MHz.
(c) Qubit anharmonicities are ηQ /2π = −320 MHz. Other parameters are the same as in Fig. 5(c).

state |0002, 1000⟩ can be suppressed. Thus, as shown in
the right panel of Figs. 9(b) and 9(c), the leakage to
|0002, 1000⟩ is indeed greatly reduced, in line with expectation. Note that this is similar to the incomplete Rabi
oscillation resulting from an oﬀ-resonance driving, and the
population error can be roughly estimated by Eq. (6).
Given the suppression of the leakage error, Figs. 10(a)
and 10(b) show the isolated gate ﬁdelity of CZ01 with qubit
anharmonicity ηQ /2π = −310 MHz and qubit anharmonicity ηQ /2π = −320 MHz, respectively. The gate
errors of CZ01 with Q3 in its excited state are indeed
greatly decreased in both cases. In particular, for the case
of ηQ /2π = −320 MHz, there is no fundamental diﬀerence between the gate error of the CZ gate on diﬀerent
qubit pairs, and gate errors of all pairs show a weak
dependence on the state of the nonparticipating qubits. On
average, the added error for each operation is suppressed
below 2 × 10−5 . Figures 10(c) and 10(d) also present the
error matrix of simultaneous CZ gates. We ﬁnd that compared to the result shown in Fig. 8(b), where ηQ /2π =
−300 MHz, on average the added error of the parallel implemented CZ gates is suppressed twofold for the

square system with ηQ /2π = −310 MHz, and sixfold for
ηQ /2π = −320 MHz.
Besides the leakage error, the remaining error could
be attributed to the parasitic interactions between nextnearest-neighbor qubits. As shown in Fig. 11, parasitic
swap interactions (double-headed arrow) among singleexcitation, two-excitation, and three-excitation subspace
can exist through high-order processes. Since the typical
detuning between next-nearest-neighbor qubits is 20 MHz
(see Fig. 5), when a ﬂux pulse tunes the tunable bus from
the idle point to the working point, the bus energy levels
will push down the qubit energy levels, thus potentially
diminishing the detuning between next-nearest-neighbor
qubits and leading to population swap between nextnearest-neighbor qubits. Thanks to the rather small qubitbus coupling, the population swap can be suppressed
below 10−4 (this was checked for the four-qubit square
system prepared in 24 diﬀerent qubit state conﬁgurations,
see Appendix B for details). In principle, this can be
further improved by increasing the detuning between nextnearest-neighbor qubits. This suggests that for systems
with increased qubit-bus or qubit-coupler coupling, as the

020301-13

## PDF page 14

PENG ZHAO et al.

PRX QUANTUM 3, 020301 (2022)
Two-excitaon
qubit subspace

Single-excitaon
qubit subspace

(a)

(a)

(b)

Three-excitaon
qubit subspace

(c)

(b)

(d)

FIG. 10. (a),(b) CZ gate error with the other two nonparticipating qubits in four diﬀerent state conﬁgurations (i.e.,
00, 01, 10, 11) for the four-qubit square system. (c),(d) Error
matrix of the parallel implemented CZ gate operations in the
four-qubit square system. In (a),(c), the qubit anharmonicity
is ηQ /2π = −310 MHz. In (b),(d), the qubit anharmonicity is
ηQ /2π = −320 MHz. The other system parameters are the same
as those in Fig. 5(c).

energy level shift is also increased, thereby, to ensure
high-ﬁdelity simultaneous gates, a large detuning between
next-nearest-neighbor qubits is needed.
3. Leakage from the avoid crossing with a tiny gap
We end this section by showing that without the
consideration of qubit decoherence, there could exist a
performance trade-oﬀ between isolated two-qubit gate
operations and simultaneous two-qubit gate operations,
i.e., in general, isolated gate operations with slower gate
speed can suppress parasitic interactions within target
qubit systems, but for simultaneous gate operations, fastspeed gates could mitigate parasitic interactions associated
with nonparticipating spectator qubits. In Fig. 12, the solid
line represents the isolated CZ01 gate error with the other
two nonparticipating qubits prepared in two diﬀerent state
conﬁgurations, i.e., 1 − F■■00 and 1 − F■■01 , versus gate
time in the four-qubit square system shown in Fig. 5(c). In
general, we ﬁnd that isolated gates with slow speed have a
lower error, but the increased gate error of CZ01 with Q3 in

the excited state and the leakage to state |0002, 1000⟩, i.e.,
P0002,1000 , suggest that the gate error of simultaneous gate
operations becomes serious.
To further elucidate the general physics behind the
trade-oﬀ, we consider that the present four-qubit system
can be simpliﬁed to a multianticrossing system that comprises a main avoided crossing with a dominated energy
gap (at the working point) and several avoided crossings
with tiny energy gaps (this is, in general, diﬀerent from the
parasitic interaction within target qubit systems, in which
the strength of the parasitic interactions is comparable to
or even larger than that of the desired interaction, thereby,

Gate error and populaon

(c)

FIG. 11. Next-nearest-neighbor interaction in (a) singleexcitation subspace, (b) two-excitation subspace, (c) threeexcitation subspace. In the four-qubit system shown in Fig. 5,
the typical detuning between next-nearest-neighbor qubits is
20 MHz. During the CZ gate operation, a ﬂux pulse tunes the tunable bus from the idle point to the working point, the bus energy
levels will push down the qubit energy levels, thus potentially
diminishing the detuning between next-nearest-neighbor qubits
and leading to population swap (double-headed arrow) between
next-nearest-neighbor qubits.

FIG. 12. Isolated CZ01 gate error with the other two nonparticipating qubits in two diﬀerent state conﬁgurations, i.e., 1 − F■■00
and 1 − F■■01 , as a function of gate time. P0002,1000 denotes
the population leakage to state |0002, 1000⟩ with the four-qubit
square system initialized in state |1101, 0000⟩. Solid lines and
dashed lines denote the result with qubit anharmonicity ηQ /2π =
−300 MHz and ηQ /2π = −310 MHz, respectively. The other
system parameters used here are the same as in Fig. 5(c).

020301-14

## PDF page 15

QUANTUM CROSSTALK ANALYSIS. . .

PRX QUANTUM 3, 020301 (2022)

the working point is chosen so that it is far detuned from
the parasitic resonance points). The main avoided crossing
results from the desired interaction used for realizing gate
operations, e.g., the interaction between |1101, 0000⟩ and
|0001, 2000⟩, and the tiny avoided crossing comes from
high-order parasitic interaction, e.g., interaction between
|1101, 0000⟩ and |0002, 1000⟩, and interactions between
next-nearest-neighbor qubits, as shown in Fig. 11. In
Fig. 13, we show two diﬀerent situations that correspond
to the two error sources discussed in Sec. III B 2.
(i) As shown in Fig. 13(a), there is a tiny avoided crossing resulting from the interaction between |j ⟩ and |α⟩.
Generally, to implement a gate operation, one needs to
bias the system to the working point. Therefore, during the
operation, the system will sweep through this tiny avoided
crossing and then come back. Thus, sweeping through this
avoided crossing with fast speed could suppress leakage to
state |j ⟩.
(ii) As shown in Fig. 13(b), around the working point,
a tiny avoided crossing, i.e., labeled as k, exists, corresponding to the parasitic interaction point (resulting from
the coupling between |γ ⟩ and |k⟩). During the gate operation, the system approaches the parasitic resonance point,
thus the detuning between |γ ⟩ and |k⟩ is reduced. In addition, the energy level |γ ⟩ is pushed down due to its coupling to the state |α⟩, thereby, further reducing its detuning
from |k⟩. Ideally, the system dynamics should be restricted
in the subspace spanned by {|α⟩, |γ ⟩}. However, the oﬀresonance interaction between the |γ ⟩ and |k⟩ can result
in an incomplete population swap between the two states,
especially, when the detuning between |γ ⟩ and |k⟩ becomes
smaller, a population swap with a larger magnitude will
present, thus potentially causing non-negligible control or

(b)

(a)
Working point

Parasic resonance
point with a ny gap

Working point

Parasic resonance
point with a ny gap

FIG. 13. Leakage channel in a multianticrossing system comprising a main avoided crossing (resulting from the resonance
interaction between |α⟩ and |γ ⟩) with a dominated energy gap
(working point) and an avoided crossing involving (a) |j ⟩ or (b)
|k⟩ with a tiny energy gap. In (a) during gate operations, the
system will sweep through the parasitic resonance point, potentially causing leakage to state |j ⟩ and in (b) the system will
approach the parasitic resonance point, resulting in a population
swap between |k⟩ and |γ ⟩.

leakage error (here, i.e., leakage to the state |k⟩). Note that
the same as the oﬀ-resonance error in single-qubit systems
[70], in general, the oﬀ-resonance swap can be suppressed
by increasing the detuning between the two states, as
demonstrated in Sec. III B 2. Furthermore, the exact oﬀresonance swap error should be studied by considering the
shape and the gate time of the control pulse [8,70,81].
In general, pulses with a long ramp can mitigate the oﬀresonance swap error. Moreover, the error itself exhibits a
periodic dependence on the gate time, and the period generally is inversely proportional to the detuning. As shown
in Fig. 12, the dashed line denotes the isolated CZ01 gate
error versus gate time with an increased qubit anharmonicity ηQ /2π = −310 MHz, giving a larger detuning between
state |0002, 1000⟩ and state |0001, 2000⟩ [Fig. 9(b), about
20 MHz]. Compared to the case of ηQ /2π = −300 MHz
(see Fig. 13, solid lines), we can ﬁnd that due to the
increased detuning, both the magnitude of leakage to state
|0002, 1000⟩ and the time of the oscillation period are
decreased as expected. Thus, to mitigate the oﬀ-resonance
error, particular attention should be paid to the parasitic
resonance point (where a tiny avoided crossing exists) with
a small detuning to the working point. In this case, the
smaller the detuning, the longer the period of the error
oscillation, thereby, implementing a gate operation within
a short time can mitigate the oﬀ-resonance swap error (see
Fig. 12, solid lines).
To circumvent the detrimental eﬀect from these tiny-gap
avoided crossings, on the whole, we argue that implementing short gates or pushing away these avoided crossings
could greatly relieve the population leakage and swap
process involving parasitic next-nearest-neighbor interactions. However, fast-speed gate operations are commonly
realized with potentially increased gate error within target qubit systems, such as the leakage error [81]. In the
present qubit architecture, to suppress diabatic transitions
within the target two-qubit system, the gate length cannot be reduced below 50 ns, limited by the small qubitbus coupling. This could raise a trade-oﬀ between gate
error resulting from target qubit systems themselves and
error from nonparticipating spectator qubits, as shown in
Fig. 12. With regard to engineering quantum systems to
remove harmful tiny-gap avoided crossings, although its
success has been demonstrated in the four-qubit square
system (see Sec. III B 2), it is still an open question
as to whether this will prove useful in a large qubit
lattice.
IV. CONCLUSION AND DISCUSSION
In this work, we ﬁrst propose a qubit architecture
with tunable ZZ coupling, where ﬁxed-frequency transmon qubits are coupled via a tunable bus, and sub-100-ns
CZ gates can be realized by applying a fast-adiabatic ﬂux
pulse to the bus. Then, we thoroughly analyze the quantum

020301-15

## PDF page 16

PENG ZHAO et al.

PRX QUANTUM 3, 020301 (2022)

crosstalk impact on simultaneous gate operations in this
qubit architecture. In general, we ﬁnd that characterization of isolated gate errors, especially, with all nonparticipating spectator qubits in their ground states, cannot
capture the full physical picture of error sources behind
simultaneous gate operations. Given this insight, we examine the isolated gate performance with nonparticipating
spectator qubits in various state conﬁgurations. Combined
with an inspection of the system dynamics during gate
operations, we ﬁnd that to ensure high simultaneous singlequbit gate ﬁdelities, dressing-induced cross driving should
be seriously considered when one operates qubits near
the frequency collision regions. For simultaneous twoqubit gates, while parasitic nearest-neighbor interactions
are commonly suppressed, parasitic next-nearest-neighbor
interactions involving spectator qubit can still exist, causing considerable leakage or control error when qubit systems sweep through or approach these parasitic resonance
points slowly. As gate operations with slower speed can, in
general, suppress unwanted interactions within target qubit
systems, but for high-order parasitic interactions involving
spectator qubits, one tends to favor short gates. This could
give rise to a trade-oﬀ between the error resulting from
target qubit systems themselves and the error from nonparticipating spectator qubits. Thus, our analysis suggests
that in pursuit of a functional quantum processor, the qubit
architecture should be examined carefully in the context of
high-ﬁdelity simultaneous gate operations.
To mitigate the dominated high-order parasitic interaction in the proposed qubit architecture, we also consider a
hardware approach to mitigate their detrimental eﬀect. We
demonstrate that by engineering qubit parameters, we can
push these parasitic resonance points far away from the
working point of desired interaction. In this way, on average, there is almost an order of magnitude improvement
in gate performance, giving the added error for simultaneous CZ gates below 1.5 × 10−5 . The remaining error could
be further suppressed by increasing the detuning between
next-nearest-neighbor qubits. This suggests that the proposed qubit architecture may be a potential architecture
towards a large-scale superconducting quantum processor
with low quantum crosstalk.
Although our present analysis of quantum crosstalk
focuses on superconducting qubit architecture with tunable buses, we expect that many of our conclusions may
also be applied to other qubit architecture, such as the
qubit architecture with tunable coupler [9,12,41,77,81],
and or at the very least, may give some physical insight
into the exact nature of quantum crosstalk in these qubit
architectures. Meanwhile, the analysis procedure may also
provide a preliminary guideline for analyzing quantum
crosstalk in other qubit architecture, and may help motivate future work on bridging the gap between high-level,
hardware-agnostic crosstalk characterization [19] and the
exact nature of crosstalk.

ACKNOWLEDGMENTS
We would like to thank Yanwu Gu, Mengjun Hu,
Yingshan Zhang, Jingning Zhang, and Teng Ma for
many helpful discussions. We also thank Yu Song and
Shuang Yang for helpful suggestions on the paper.
This work was supported by the Beijing Natural Science Foundation (Grant No. Z190012), the National
Natural Science Foundation of China (Grants No.
11890704, No. 12004042, and No. 11905100), the
National Key Research and Development Program of
China (Grant No. 2016YFA0301800), and the Key-Area
Research and Development Program of Guang Dong
Province (Grant No. 2018B030326001). P.X. was supported by the Young Fund of Jiangsu Natural Science
Foundation of China (Grant No. BK20180750) and the
National Natural Science Foundation of China (Grant No.
12105146).
APPENDIX A: CALIBRATION PROCEDURE OF
GATE OPERATIONS
In this Appendix, we give further detailed descriptions
on the calibration procedure of gate operations (i.e., singlequbit X gate and two-qubit CZ gate) discussed in the main
text. Here, for illustration purposes only, we consider the
two-qubit system shown in Fig. 1. In the following discussion, we show how the single-qubit X gate and the
two-qubit CZ gate are calibrated in the two-qubit system.
As in Fig. 1, the system parameters are as follows: qubit
frequency ω1(2) /2π = 5.000(5.200) GHz, anharmonicity
η1 = η2 = ηTB = η (η/2π = −300 MHz), and qubit-bus
coupling g1(2) = g (g/2π = 25 MHz) (at ω1(2) = ωTB =
5.500 GHz). In addition, the idle point of the tunable
bus is at ωTB /2π = 5.65 GHz, as marked by the black
arrow in Fig. 1(c). In the following discussion, notations
|Q1 Q2 TB⟩ represent the full system states, and when
conﬁned to the qubit subspace, notation |Q1 Q2 ⟩ is used.
In addition, we note that the following introduced calibration procedures are also applied to the calibration of
single-qubit gates and two-qubit gates in the four-qubit
system studied in Sec. III.
1. Calibration of single-qubit X gates
As we mentioned in Sec. II B 1, in the present work, the
single-qubit X gate is implemented by using the DRAG
scheme [3,4,71]. For illustration purposes, here, we consider the implementation of a single-qubit X gate applied
to the qubit Q1 . As shown in Eq. (4), the driven Hamiltonian for implementing XQ1 is
†

Hd (t) = [x (t) cos(ωd t) + y (t) sin(ωd t)](a1 + a1 ),
x (t) =

020301-16

A
α
˙ x (t), (A1)
[1 − cos(2π t/tg )], y (t) = − 
2
η

## PDF page 17

QUANTUM CROSSTALK ANALYSIS. . .
(a)

PRX QUANTUM 3, 020301 (2022)
where ŨX denote the actual implemented X gate operation,
and
(
)
0 1
X =
.
(A3)
1 0

(b)

According to the two-qubit system Hamiltonian given in
Eq. (1) and the driven Hamiltonian given in Eq. (A1), the
actual evolution operator is
( ∫ tg
)
U1 = T̂ exp −i
HX (t)dt ,

(A4)

0

(c)

where HX (t) = H + Hd (t), and T̂ denotes the timeordering operator. Thus, in the single-qubit computational
subspace for Q1 , the actual implemented X gate operation
is given as
†

ŨX = P1 U1 P1 ,
FIG. 14. Tune-up procedure for the single-qubit X gate. (a)
Population error 1 − P100 as a function of the driving amplitude
A and the driving detuning (ωd − ω1 ) for the two-qubit system
initialized in state |000⟩, and the ﬁxed gate length tg = 20 ns. (b)
Same as in (a), instead showing the leakage 1 − (P000 + P100 )
versus the driving amplitude A and the driving detuning (ωd −
ω1 ) for the single-qubit gate operations. (c) System dynamics
during the gate operation with the optimal parameter set indicated by the red stars in (a),(b) where both the population error
and the leakage are suppressed below 10−6 .

The XQ1 gate is tuned up by adjusting the driving amplitude A and the driving detuning of the pulse from the qubit
bare frequency (ωd − ω1 ) for a ﬁxed gate length (tg =
20 ns) and the parameter α = 0.5. Figure 14(a) shows
the population error 1 − P100 (P100 denotes the population in state |100⟩ at the end of the gate operation) as a
function of the driving amplitude A and the driving detuning (ωd − ω1 ) for the two-qubit system initialized in state
|000⟩. In Fig. 14(b), we also show the leakage error 1 −
(P000 + P100 ). One can ﬁnd that at the minimal error point,
i.e., {A/2π ≃ 50.15 MHz, (ωd − ω1 )/(2π ) ≃ 0.9 MHz},
marked by the red stars in Figs. 14(a) and (b), both the
population error and leakage is suppressed below 10−6 , as
shown in Fig. 14(c). Note here that in the present setting, as
expected, the obtained optimal driving frequency is indeed
at the dressed qubit frequency of Q1 .
After obtaining the optimal parameter set from the result
shown in Fig. 14, we characterize the ﬁdelity of XQ1 gate
by using the metric given in Eq. (7), i.e.,
†

F(ŨX , X ) =

Tr(ŨX ŨX ) + |Tr(X † ŨX )|2
,
6

(A2)

(A5)

where P1 is the projected operator deﬁned in the computational subspace of the full system, i.e., the subspace
spanned by {|000⟩, |100⟩}. Finally, to account for the
local single-qubit phase [3,4], the gate ﬁdelity is obtained
as [43,47]
F = maximize{φ} F[Upost1 (φ)ŨX , X ],

(A6)

with Upost1 (φ) = e−iφZ/2 , where Z represents the singlequbit Pauli operator σz .
2. Calibration of CZ gates
As mentioned in Secs. II B 2 and III B, the CZ gate
⎛

1
⎜ 0
CZ = ⎝
0
0

0
1
0
0

0
0
1
0

⎞
0
0 ⎟
0 ⎠
−1

(A7)

is realized by applying a ﬁxed-length (T = 68 ns) ﬂux
pulse to the tunable bus, tuning its frequency from its idle
point (θ0 ) to the working point (θf ) and then coming back.
The pulse shape is given in Eq. (8) with three Fourier coefﬁcients {λ1 , λ2 , λ3 }, where λ1 + λ3 = 1. Thus, this gives
rise to totally three free parameters {λ1 , λ2 , θf }. For reaching a target error at around 10−5 , the free parameter set is
determined by optimizing the CZ gate ﬁdelity according to
the metric given in Eq. (7), i.e.,
†

F(ŨCZ , CZ) =

Tr(ŨCZ ŨCZ ) + |Tr(CZ† ŨCZ )|2
.
20

(A8)

Similar to the case of single-qubit gates, according to the
system Hamiltonian given in Eq. (1) and the pulse shape

020301-17

## PDF page 18

PENG ZHAO et al.

PRX QUANTUM 3, 020301 (2022)

given in Eq. (8), the actual evolution operator for the gate
operation is

APPENDIX B: POPULATION SWAP BETWEEN
NEXT-NEAREST-NEIGHBORING QUBITS

( ∫ T
)
H (t)dt .
U2 = T̂ exp −i

As shown in Fig. 11 and mentioned in Sec. II B 2,
the population swap between next-nearest-neighbor qubit
pairs, which results from oﬀ-resonance interaction among
them in the four-qubit system, can contribute to the gate
error of simultaneous CZ gates. Figure 15 shows the population swap matrix P(o|i) in the single-excitation subspace {|1000⟩, |0010⟩, |0100⟩, |0001⟩}, the two-excitation
subspace {|1100⟩, |1001⟩, |0110⟩, |0011⟩}, and the threeexcitation subspace {|1110⟩, |1011⟩, |1101⟩, |0111⟩} of the
four-qubit square system shown in Fig. 5(c). Each matrix
element P(o|i) denotes the population in state |o⟩ after the
gate operation with the qubit system initialized in state |i⟩.
From Fig. 15, one can ﬁnd that a signiﬁcant population
swap exists only for the state transition process involving next-nearest-neighboring qubits. These transitions are
indicated by double-headed arrows connecting the states
of next-nearest-neighboring qubits, as shown in Fig. 11.
Moreover, as these population swaps are enabled by highorder processes, the population swap errors are suppressed
below 10−4 .

(A9)

0

Thus, truncated to the two-qubit computational subspace,
the actual implemented CZ gate operation is given as
†

ŨCZ = P2 U2 P2 ,

(A10)

where P2 is the projected operator deﬁned in the two-qubit
subspace spanned by {|000⟩, |010⟩, |100⟩, |110⟩}. Finally,
to account for the local single-qubit phases [43,47], the
gate ﬁdelity is obtained as
F = maximize{φ1 ,φ2 } F[Upost2 (φ1 , φ2 )ŨCZ , CZ],

(A11)

with Upost2 (φ1 , φ2 ) = e−iφ1 ZI /2 e−iφ2 IZ/2 , where Z and I
represent the single-qubit Pauli operator σz and identity
operators, and the order indexes the qubit number.

(a)

(b)

(c)

(d)

(e)

(f)

FIG. 15. Population swap matrix P(o|i) for the implementation of simultaneous CZ gates in the four-qubit square system shown
in Fig. 5(c). The matrix element P(o|i) denotes the population in state |o⟩ for the qubit system initialized in state |i⟩. [(a),(d)] for
the qubit system initialized in the single-excitation subspace {|1000⟩, |0010⟩, |0100⟩, |0001⟩}, [(b),(e)] for the two-excitation subspace
{|1100⟩, |1001⟩, |0110⟩, |0011⟩}, and [(c),(f)] for the three-excitation subspace {|1110⟩, |1011⟩, |1101⟩, |0111⟩}. (a)–(c) Population swap
matrix for the parallel implementation of CZ01 and CZ23 . (d)–(f) Population swap matrix for the parallel implementation of CZ12
and CZ30 .

020301-18

## PDF page 19

QUANTUM CROSSTALK ANALYSIS. . .

PRX QUANTUM 3, 020301 (2022)

[1] J. M. Martinis, Qubit metrology for building a fault tolerant
quantum computer, npj Quantum Inf. 1, 15005 (2015).
[2] M. Kjaergaard, M. E. Schwartz, J. Braumüller, P. Krantz,
J. I.-J. Wang, S. Gustavsson, and W. D. Oliver, Superconducting qubits: Current state of play, Annu. Rev. Condens.
Matter Phys. 11, 369 (2020).
[3] Z. Chen, et al., Measuring and Suppressing Quantum State
Leakage in a Superconducting Qubit, Phys. Rev. Lett. 116,
020501 (2016).
[4] D. C. McKay, C. J. Wood, S. Sheldon, J. M. Chow, and
J. M. Gambetta, Eﬃcient z gates for quantum computing,
Phys. Rev. A 96, 022330 (2017).
[5] A. Somoroﬀ, Q. Ficheux, R. A. Mencia, H. Xiong, R. V.
Kuzmin, and V. E. Manucharyan, Millisecond coherence in
a superconducting qubit, ArXiv:2103.08578.
[6] R. Barends, C. M. Quintana, A. G. Petukhov, Y. Chen,
D. Kafri, and K. Kechedzhi, et al., Diabatic Gates for
Frequency-Tunable Superconducting Qubits, Phys. Rev.
Lett. 123, 210501 (2019).
[7] M. A. Rol, F. Battistel, F. K. Malinowski, C. C. Bultink,
B. M. Tarasinski, R. Vollmer, N. Haider, N. Muthusubramanian, A. Bruno, B. M. Terhal, and L. DiCarlo, Fast,
High-Fidelity Conditional-Phase Gate Exploiting Leakage Interference in Weakly Anharmonic Superconducting
Qubits, Phys. Rev. Lett. 123, 120502 (2019).
[8] Y. Sung, L. Ding, J. Braumüller, A. Vepsäläinen, B. Kannan, M. Kjaergaard, A. Greene, G. O. Samach, C. McNally,
D. Kim, A. Melville, B. M. Niedzielski, M. E. Schwartz, J.
L. Yoder, T. P. Orlando, S. Gustavsson, and W. D. Oliver,
Realization of High-Fidelity CZ and ZZ-Free iSWAP
Gates with a Tunable Coupler, Phys. Rev. X 11, 021058
(2021).
[9] Y. Xu, J. Chu, J. Yuan, J. Qiu, Y. Zhou, L. Zhang, X. Tan,
Y. Yu, S. Liu, J. Li, F. Yan, and D. Yu, High-Fidelity, HighScalability Two-Qubit Gate Scheme for Superconducting
Qubits, Phys. Rev. Lett. 125, 240503 (2020).
[10] B. K. Mitchell, R. K. Naik, A. Morvan, A. Hashim,
J. M. Kreikebaum, B. Marinelli, W. Lavrijsen, K.
Nowrouzi, D. I. Santiago, and I. Siddiqi, Hardware-eﬃcient
microwave-activated tunable coupling between superconducting qubits, ArXiv:2105.05384.
[11] K. X. Wei, E. Magesan, I. Lauer, S. Srinivasan, D. F.
Bogorin, S. Carnevale, G. A. Keefe, Y. Kim, D. Klaus,
W. Landers, N. Sundaresan, C. Wang, E. J. Zhang, M.
Steﬀen, O. E. Dial, D. C. McKay, and A. Kandala, Quantum crosstalk cancellation for fast entangling gates and
improved multi-qubit performance, ArXiv:2106.00675.
[12] E. A. Sete, N. Didier, A. Q. Chen, S. Kulshreshtha, R.
Manenti, and S. Poletto, Parametric-Resonance Entangling
Gates with a Tunable Coupler, Phys. Rev. Appl. 16, 024050
(2021).
[13] Q. Ficheux, L. B. Nguyen, A. Somoroﬀ, H. Xiong, Ko. N.
Nesterov, M. G. Vavilov, and V. E. Manucharyan, Realization of Fast Logic with Slow Qubits: Microwave-Activated
Controlled-Z Gate on Low-Frequency Fluxoniums, Phys.
Rev. X 11, 021026 (2021).
[14] J. M. Chow, S. J. Srinivasan, E. Magesan, A. D. Córcoles, D. W. Abraham, J. M. Gambetta, and M. Steﬀen,
Characterizing a four-qubit planar lattice for arbitrary error
detection, Proc. SPIE 9500, Quantum Inf. Comput. 13,
95001G (2015).

[15] F. Arute, K. Arya, R. Babbush, D. Bacon, J. C. Bardin, R.
Barends, R. Biswas, S. Boixo, F. G. Brandao, and D. A.
Buell, et al., Quantum supremacy using a programmable
superconducting processor, Nature 574, 505 (2019).
[16] Q. Zhu, S. Cao, F. Chen, M.-C. Chen, X. Chen, T.-H.
Chung, H. Deng, Y. Du, D. Fan, and M. Gong, et al., Quantum computational advantage via 60-qubit 24-cycle random
circuit sampling, ArXiv:2109.03494.
[17] X. Zhang, W. Jiang, J. Deng, K. Wang, J. Chen, P. Zhang,
W. Ren, H. Dong, S. Xu, Y. Gao, F. Jin, X. Zhu, Q. Guo, H.
Li, C. Song, Z. Wang, D.-L. Deng, and H. Wang, Observation of a symmetry-protected topological time crystal with
superconducting qubits, ArXiv:2109.05577.
[18] D. M. Zajac, J. Stehlik, D. L. Underwood, T. Phung,
J. Blair, S. Carnevale, D. Klaus, G. A. Keefe, A. Carniol,
M. Kumph, M. Steﬀen, and O. E. Dial, Spectator errors in
tunable coupling architectures, ArXiv:2108.11221.
[19] M. Sarovar, T. Proctor, K. Rudinger, K. Young, E.
Nielsen, and R. Blume-Kohout, Detecting crosstalk errors
in quantum information processors, Quantum 4, 321
(2020).
[20] A. G. Fowler, M. Mariantoni, J. M. Martinis, and A. N. Cleland, Surface codes: Towards practical large-scale quantum
computation, Phys. Rev. A 86, 032324 (2012).
[21] J. M. Gambetta, A. D. Córcoles, S. T. Merkel, B. R. Johnson, John A. Smolin, J. M. Chow, C. A. Ryan, C. Rigetti, S.
Poletto, T. A. Ohki, M. B. Ketchen, and M. Steﬀen, Characterization of Addressability by Simultaneous Randomized
Benchmarking, Phys. Rev. Lett. 109, 240504 (2012).
[22] K. Rudinger, T. Proctor, D. Langharst, M. Sarovar, K.
Young, and R. Blume-Kohout, Probing Context-Dependent
Errors in Quantum Processors, Phys. Rev. X 9, 021045
(2019).
[23] C. Huang, X. Ni, F. Zhang, M. Newman, D. Ding, X.
Gao, T. Wang, H. Zhao, F. Wu, G. Zhang, C. Deng, H.
Ku, J. Chen, and Y. Shi, Alibaba Cloud Quantum Development Platform: surface code simulations with crosstalk,
ArXiv:2002.08918.
[24] S. Niu and A. Todri-Sanial, Analyzing crosstalk error in the
NISQ era, ArXiv:2106.01671.
[25] A. Ash-Saki, M. Alam, and S. Ghosh, Experimental characterization, modeling, and analysis of crosstalk in a quantum
computer, IEEE Trans. Quantum Eng. 1, 1 (2021).
[26] K. Rudinger, C. W. Hogle, R. K. Naik, A. Hashim, D.
Lobser, D. I. Santiago, M. D. Grace, E. Nielsen, T. Proctor, S. Seritan, S. M. Clark, R. Blume-Kohout, I. Siddiqi, and K. C. Young, Experimental characterization of
crosstalk errors with simultaneous gate set tomography,
ArXiv:2103.09890.
[27] R. Barends, et al., Superconducting quantum circuits at the
surface code threshold for fault tolerance, Nature 508, 500
(2014).
[28] D. M. Abrams, N. Didier, S. A. Caldwell, B. R. Johnson,
and C. A. Ryan, Methods for Measuring Magnetic Flux
Crosstalk between Tunable Transmons, Phys. Rev. Appl.
12, 064022 (2019).
[29] X. Dai, D. M. Tennant, R. Trappen, A. J. Martinez, D.
Melanson, M. A. Yurtalan, Y. Tang, S. Novikov, J. A.
Grover, S. M. Disseler, J. I. Basham, R. Das, D. K. Kim,
A. J. Melville, B. M. Niedzielski, S. J. Weber, J. L. Yoder,
D. A. Lidar, and A. Lupascu, Calibration of ﬂux crosstalk in

020301-19

## PDF page 20

PENG ZHAO et al.

PRX QUANTUM 3, 020301 (2022)

large-scale ﬂux-tunable superconducting quantum circuits,
ArXiv:2105.14360.
[30] M. Takita, A. D. Córcoles, E. Magesan, B. Abdo, M. Brink,
A. Cross, J. M. Chow, and J. M. Gambetta, Demonstration
of Weight-Four Parity Measurements in the Surface Code
Architecture, Phys. Rev. Lett. 117, 210505 (2016).
[31] M. Takita, A. W. Cross, A. D. Córcoles, J. M. Chow,
and J. M. Gambetta, Experimental Demonstration of FaultTolerant State Preparation with Superconducting Qubits,
Phys. Rev. Lett. 119, 180501 (2017).
[32] D. C. McKay, S. Sheldon, J. A. Smolin, J. M. Chow, and
J. M. Gambetta, Three Qubit Randomized Benchmarking,
Phys. Rev. Lett. 122, 200502 (2019).
[33] N. Sundaresan, I. Lauer, E. Pritchett, E. Magesan, P. Jurcevic, and J. M. Gambetta, Reducing unitary and spectator
errors in cross resonance with optimized rotary echoes,
PRX Quantum 1, 020318 (2020).
[34] A. Winick, J. J. Wallman, and J. Emerson, Simulating and
Mitigating Crosstalk, Phys. Rev. Lett. 126, 230502 (2021).
[35] X. Deng, Y. Hai, J. Li, and Y. Song, Correcting correlated errors for quantum gates in multi-qubit systems using
smooth pulse control, ArXiv:2103.08169.
[36] V. Tripathi, H. Chen, M. Khezri, K. Yip, E. M.
Levenson-Falk, and D. A. Lidar, Suppression of crosstalk
in superconducting qubits using dynamical decoupling,
ArXiv:2108.04530.
[37] P. Murali, D. C. McKay, M. Martonosi, and A.
Javadi-Abhari, Software mitigation of crosstalk on noisy
intermediate-scale quantum computers, ArXiv:2001.
02826.
[38] Y. Ding, P. Gokhale, S. F. Lin, R. Rines, T. Propson, and F. T. Chong, Systematic crosstalk mitigation for
superconducting qubits via frequency-aware compilation,
ArXiv:2008.09503.
[39] K. N. Smith, G. S. Ravi, P. Murali, J. M. Baker, N.
Earnest, A. Javadi-Abhari, and F. T. Chong, Error mitigation in quantum computers through instruction scheduling,
ArXiv:2105.01760.
[40] Y. Chen, et al., Qubit Architecture with High Coherence
and Fast Tunable Coupling, Phys. Rev. Lett. 113, 220502
(2014).
[41] F. Yan, P. Krantz, Y. Sung, M. Kjaergaard, D. L. Campbell, T. P. Orlando, S. Gustavsson, and W. D. Oliver,
Tunable Coupling Scheme for Implementing High-Fidelity
Two-Qubit Gates, Phys. Rev. Appl. 10, 054062 (2018).
[42] A. D. Patterson, J. Rahamim, T. Tsunoda, P. A. Spring,
S. Jebari, K. Ratter, M. Mergenthaler, G. Tancredi,
B. Vlastakis, M. Esposito, and P. J. Leek, Calibration
of a Cross-Resonance Two-Qubit Gate Between Directly
Coupled Transmons, Phys. Rev. Appl. 12, 064013 (2019).
[43] P. Zhao, P. Xu, D. Lan, X. Tan, H. Yu, and Y. Yu, Switchable Next-Nearest-Neighbor Coupling for Controlled TwoQubit Operations, Phys. Rev. Appl. 14, 064016 (2020).
[44] P. S. Mundada, G. Zhang, T. Hazard, and A. A. Houck,
Suppression of Qubit Crosstalk in a Tunable Coupling
Superconducting Circuit, Phys. Rev. Appl. 12, 054023
(2019).
[45] X. Li, T. Cai, H. Yan, Z. Wang, X. Pan, Y. Ma, W. Cai, J.
Han, Z. Hua, X. Han, Y. Wu, H. Zhang, H. Wang, Yipu
Song, Luming Duan, and Luyan Sun, Tunable Coupler
for Realizing a Controlled-Phase Gate with Dynamically

Decoupled Regime in a Superconducting Circuit, Phys.
Rev. Appl. 14, 024070 (2020).
[46] J. Ku, X. Xu, M. Brink, D. C. McKay, J. B. Hertzberg, M.
H. Ansari, and B. L. T. Plourde, Suppression of Unwanted
ZZ Interactions in a Hybrid Two-Qubit System, Phys. Rev.
Lett. 125, 200504 (2020).
[47] P. Zhao, P. Xu, D. Lan, J. Chu, X. Tan, H. Yu, and Y.
Yu, High-Contrast ZZ Interaction Using Superconducting
Qubits with Opposite-Sign Anharmonicity, Phys. Rev. Lett.
125, 200503 (2020).
[48] X. Xu and M. H. Ansari, ZZ Freedom in two Qubit Gates,
Phys. Rev. Appl. 15, 064074 (2021).
[49] A. Kandala, K. X. Wei, S. Srinivasan, E. Magesan, S.
Carnevale, G. A. Keefe, D. Klaus, O. Dial, and D. C.
McKay, Demonstration of a high-ﬁdelity CNOT for ﬁxedfrequency transmons with engineered ZZ suppression,
ArXiv:2011.07050.
[50] P. Zhao, D. Lan, P. Xu, G. Xue, M. Blank, X. Tan, H. Yu,
and Y. Yu, Suppression of static ZZ interaction in an alltransmon quantum processor, Phys. Rev. Appl. 16, 024037
(2021).
[51] A. D. K. Finck, S. Carnevale, D. Klaus, C. Scerbo, J.
Blair, T. G. McConkey, C. Kurter, A. Carniol, G. Keefe,
M. Kumph, and O. E. Dial, Suppressed crosstalk between
two-junction superconducting qubits with mode-selective
exchange coupling, ArXiv:2105.11495.
[52] A. Noguchi, A. Osada, S. Masuda, S. Kono, K. Heya, S. P.
Wolski, H. Takahashi, T. Sugiyama, D. Lachance-Quirion,
and Y. Nakamura, Fast parametric two-qubit gates with
suppressed residual interaction using the second-order nonlinearity of a cubic transmon, Phys. Rev. A 102, 062408
(2020).
[53] A. Petrescu, C. L. Calonnec, C. Leroux, A. D. Paolo, P.
Mundada, S. Sussman, A. Vrajitoarea, A. A. Houck, and
A. Blais, Accurate methods for the analysis of strong-drive
eﬀects in parametric gates, ArXiv:2107.02343.
[54] C. Leroux, A. D. Paolo, and A. Blais, Superconducting coupler with exponentially large on-oﬀ ratio,
ArXiv:2107.09861.
[55] S. Krinner, S. Lazar, A. Remm, C. K. Andersen, N. Lacroix,
G. J. Norris, C. Hellings, M. Gabureac, C. Eichler, and
A. Wallraﬀ, Benchmarking Coherent Errors in ControlledPhase Gates due to Spectator Qubits, Phys. Rev. Appl. 14,
024042 (2020).
[56] M. Malekakhlagh, E. Magesan, and D. C. McKay, Firstprinciples analysis of cross-resonance gate operation,
Phys. Rev. A 102, 042605 (2020).
[57] T.-Q. Cai, X.-Y. Han, Y.-K. Wu, Y.-L. Ma, J.-H. Wang, Z.L. Wang, H.-Y Zhang, H.-Y Wang, Y.-P. Song, and L.-M.
Duan, Impact of Spectators on a Two-Qubit Gate in a Tunable Coupling Superconducting Circuit, Phys. Rev. Lett.
127, 060505 (2021).
[58] J. Chu and F. Yan, Coupler-assisted controlled-phase gate
with enhanced adiabaticity, ArXiv:2106.00725.
[59] J. Koch, T. M. Yu, J. Gambetta, A. A. Houck, D. I. Schuster, J. Majer, A. Blais, M. H. Devoret, S. M. Girvin, and
R. J. Schoelkopf, Charge-insensitive qubit design derived
from the cooper pair box, Phys. Rev. A 76, 042319
(2007).
[60] D. C. McKay, S. Filipp, A. Mezzacapo, E. Magesan,
J. M. Chow, and J. M. Gambetta, Universal Gate for

020301-20

## PDF page 21

QUANTUM CROSSTALK ANALYSIS. . .

PRX QUANTUM 3, 020301 (2022)

Fixed-Frequency Qubits via a Tunable bus, Phys. Rev.
Appl. 6, 064007 (2016).
[61] R. Krishnan and J. A. Pople, Approximate fourth-order perturbation theory of the electron correlation energy, Int. J.
Quantum Chem. 14, 91 (1978).
[62] L. DiCarlo, J. M. Chow, J. M. Gambetta, L. S. Bishop, B.
R. Johnson, D. I. Schuster, J. Majer, A. Blais, L. Frunzio, S. M. Girvin, and R. J. Schoelkopf, Demonstration
of two-qubit algorithms with a superconducting quantum
processor, Nature (London) 460, 240 (2009).
[63] L. Jin, Implementing high-ﬁdelity two-qubit gates in
superconducting coupler architecture with novel parameter
regions, ArXiv:2105.13306.
[64] M. H. Goerz, F. Motzoi, K. B. Whaley, and C. P. Koch,
Charting the circuit QED design landscape using optimal
control theory, npj Quantum Inf. 3, 37 (2017).
[65] G. S. Paraoanu, Microwave-induced coupling of superconducting qubits, Phys. Rev. B 74, 140504(R) (2006).
[66] C. Rigetti and M. Devoret, Fully microwave-tunable universal gates in superconducting qubits with linear couplings
and ﬁxed transition frequencies, Phys. Rev. B 81, 134507
(2010).
[67] M. Brink, J. M. Chow, J. Hertzberg, E. Magesan, and Sami
Rosenblatt, Device challenges for near term superconducting quantum processors: frequency collisions, 2018 IEEE
Int. Electron Devices Meeting (IEDM), (2018).
[68] E. Magesan and J. M. Gambetta, Eﬀective Hamiltonian
models of the cross-resonance gate, Phys. Rev. A 101,
052308 (2020).
[69] J. Kelly, et al., Optimal Quantum Control Using Randomized Benchmarking, Phys. Rev. Lett. 112, 240504 (2014).
[70] M. Malekakhlagh and E. Magesan, Mitigating oﬀ-resonant
error in the cross-resonance gate, ArXiv:2108.03223.
[71] F. Motzoi, J. M. Gambetta, P. Rebentrost, and F. K. Wilhelm, Simple Pulses for Elimination of Leakage in Weakly
Nonlinear Qubits, Phys. Rev. Lett. 103, 110501 (2009).
[72] L. H. Pedersen, N. M. Møller, and K. Mølmer, Fidelity of
quantum operations, Phys. Lett. A 367, 47 (2007).
[73] C. J. Wood and J. M. Gambetta, Quantiﬁcation and characterization of leakage errors, Phys. Rev. A 97, 032306
(2018).
[74] S. Huang, B. Lienhard, G. Calusine, A. Vepsäläinen, J.
Braumüller, D. K. Kim, A. J. Melville, B. M. Niedzielski, J.
L. Yoder, B. Kannan, T. P. Orlando, S. Gustavsson, and W.
D. Oliver, Microwave package design for superconducting
quantum processors, PRX Quantum 2, 020306 (2021).
[75] K. Linghu, et al., in preparation. (2020).
[76] J. M. Martinis and M. R. Geller, Fast adiabatic qubit gates
using only σ z control, Phys. Rev. A 90, 022307 (2014).
[77] M. C. Collodo, J. Herrmann, N. Lacroix, C. K. Andersen, A. Remm, S. Lazar, J. Besse, T. Walter, A. Wallraﬀ,
and C. Eichler, Implementation of Conditional Phase Gates

Based on Tunable ZZ Interactions, Phys. Rev. Lett. 125,
240502 (2020).
[78] J. Stehlik, D. M. Zajac, D. L. Underwood, T. Phung, J.
Blair, S. Carnevale, D. Klaus, G. A. Keefe, A. Carniol,
M. Kumph, M. Steﬀen, and O. E. Dial, Tunable Coupling
Architecture for Fixed-Frequency Transmon Superconducting Qubits, Phys. Rev. Lett. 127, 080505 (2021).
[79] J. M. Kreikebaum, K. P. O’Brien, A. Morvan, and I. Siddiqi, Improving wafer-scale josephson junction resistance
variation in superconducting quantum coherent circuits,
Supercond. Sci. Technol. 33, 06LT02 (2020).
[80] J. B. Hertzberg, E. J. Zhang, S. Rosenblatt, E. Magesan, J.
A. Smolin, J.-B. Yau, V. P. Adiga, M. Sandberg, M. Brink,
Je. M. Chow, and J. S. Orcutt, Laser-annealing josephson
junctions for yielding scaled-up superconducting quantum
processors, npj Quantum Inf. 7, 129 (2021).
[81] B. Foxen, C. Neill, A. Dunsworth, P. Roushan, B. Chiaro,
A. Megrant, J. Kelly, Z. Chen, K. Satzinger, and R.
Barends, et al., Demonstrating a Continuous Set of TwoQubit Gates for Near-Term Quantum Algorithms, Phys.
Rev. Lett. 125, 120504 (2020).
[82] M. D. Hutchings, J. B. Hertzberg, Y. Liu, N. T. Bronn, G. A.
Keefe, M. Brink, J. M. Chow, and B. L. T. Plourde, Tunable
Superconducting Qubits with Flux-Independent Coherence,
Phys. Rev. Appl. 8, 044003 (2017).
[83] P. J. Leek, S. Filipp, P. Maurer, M. Baur, R. Bianchetti, J. M.
Fink, M. Göppl, L. Steﬀen, and A. Wallraﬀ, Using sideband
transitions for two-qubit operations in superconducting
circuits, Phys. Rev. B 79, 180511(R) (2009).
[84] S. A. Caldwell, N. Didier, C. A. Ryan, E. A. Sete, A.
Hudson, P. Karalekas, R. Manenti, M. P. da Silva, R. Sinclair, and E. Acala, et al., Parametrically Activated Entangling Gates Using Transmon Qubits, Phys. Rev. Appl. 10,
034050 (2018).
[85] M. Pechal, G. Salis, M. Ganzhorn, D. J. Egger, M. Werninghaus, and S. Filipp, Characterization and tomography of
a hidden qubit, ArXiv:2011.08987.
[86] M. Jerger, A. Kulikov, Z. Vasselin, and A. Fedorov, In
Situ Characterization of Qubit Control Lines: A Qubit as
a Vector Network Analyzer, Phys. Rev. Lett. 123, 150501
(2019).
[87] M. A. Rol, L. Ciorciaro, F. K. Malinowski, B. M. Tarasinski, R. E. Sagastizabal, C. C. Bultink, Y. Salathe, N. Haandbaek, J. Sedivy, and L. DiCarlo, Time-domain characterization and correction of on-chip distortion of control pulses in
a quantum processor, Appl. Phys. Lett. 116, 054001 (2020).
[88] B. Foxen, J. Y. Mutus, E. Lucero, E. Jeﬀrey, D. Sank, R.
Barends, K. Arya, B. Burkett, Y. Chen, Z. Chen, B. Chiaro,
A. Dunsworth, A. Fowler, C. Gidney, and M. Giustina,
et al., High speed ﬂux sampling for tunable superconducting qubits with an embedded cryogenic transducer,
Supercond. Sci. Technol. 21, 015012 (2019).

020301-21
