Source: https://doi.org/10.1103/PRXQuantum.5.030350
PDF sha256: 452cc36bdfa37a638a0fcd0610f3b94131f0d771af35bd1c3aeceee01438f74e
License: https://creativecommons.org/licenses/by/4.0/

# Transcription of kosen_2024_signal_crosstalk_flip_chip_quantum_processor.pdf

Transcription of `kosen_2024_signal_crosstalk_flip_chip_quantum_processor.pdf` in this directory, 21 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-21 from the PDF's own text layer (pdftotext version 26.10.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

PRX QUANTUM 5, 030350 (2024)
Featured in Physics

Signal Crosstalk in a Flip-Chip Quantum Processor
Sandoko Kosen ,1,* Hang-Xi Li ,1 Marcus Rommel,1 Robert Rehammar ,1 Marco Caputo ,2
Leif Grönberg,2 Jorge Fernández-Pendás ,1 Anton Frisk Kockum ,1 Janka Biznárová,1
Liangyu Chen ,1 Christian Križan ,1 Andreas Nylander ,1 Amr Osman,1 Anita Fadavi Roudsari ,1
Daryoush Shiri ,1 Giovanna Tancredi ,1 Joonas Govenius ,2 and Jonas Bylander 1,†
1

2

Chalmers University of Technology, Gothenburg 412 96, Sweden
VTT Technical Research Centre of Finland, VTT Espoo FI-02044, Finland

(Received 9 March 2024; revised 13 June 2024; accepted 16 July 2024; published 12 September 2024)
Quantum processors require a signal-delivery architecture with high addressability (low crosstalk) to
ensure high performance already at the scale of dozens of qubits. Signal crosstalk causes inadvertent driving of quantum gates, which will adversely aﬀect quantum gate ﬁdelities in scaled-up devices. Here, we
demonstrate packaged ﬂip-chip superconducting quantum processors with signal-crosstalk performance
competitive with those reported in other platforms. For capacitively coupled qubit-drive lines, we ﬁnd
on-resonant crosstalk better than −27 dB (average −37 dB). For inductively coupled magnetic-ﬂux-drive
lines, we ﬁnd less than 0.13% direct-current ﬂux crosstalk (average 0.05%). These observed crosstalk levels are adequately small and indicate a decreasing trend with increasing distance, which is promising for
further scaling up to larger numbers of qubits. We discuss the implications of our results for the design of a
low-crosstalk on-chip signal-delivery architecture, including the inﬂuence of a shielding tunnel structure,
potential sources of crosstalk, and estimation of crosstalk-induced qubit-gate error in scaled-up quantum
processors.
DOI: 10.1103/PRXQuantum.5.030350

I. INTRODUCTION
The quest for demonstrating quantum computational
advantage and fault-tolerant quantum computation has
inspired the realization of integrated quantum processors
[1–4]. A prominent physical platform is based on superconducting qubits, which are typically submillimeter in
size, made of lithographically deﬁned thin-ﬁlm devices on
low-loss substrates and which operate at frequencies below
10 GHz in a cryogenic environment. Scaling up superconducting quantum processors requires microchip integration
in an extensible design while maintaining high-ﬁdelity
qubit performance through predictable device parameters
and high-yield fabrication.
An outstanding problem for extensible designs is onchip signal routing that enables components within the processor to be selectively addressed and read out. In current

*
†

Contact author: sandoko.kosen@gmail.com
Contact author: jonas.bylander@chalmers.se

Published by the American Physical Society under the terms of
the Creative Commons Attribution 4.0 International license. Further distribution of this work must maintain attribution to the
author(s) and the published article’s title, journal citation, and
DOI.

2691-3399/24/5(3)/030350(21)

technology, signals are usually routed from the edge of
the chip, where wire bonds make connection to a printed
circuit board (PCB) and further on to connectors on a
microwave package. If the signal is insuﬃciently shielded,
crosstalk ensues and results in quantum gate errors that
render quantum computation infeasible. Active crosstalksuppression techniques, which involve characterizing the
crosstalk matrix and applying its inverse [5–10], are prohibitively challenging at scale. We must thus ensure that
the circuit architecture supports adequate passive crosstalk
suppression by proper routing and shielding techniques.
Therefore, the road map for next-generation quantum processors requires an understanding of the inﬂuence of
densely routed signal lines and an informed strategy for
signal delivery with low crosstalk. This challenge has not
received the attention that it deserves.
Signal crosstalk can be investigated in dedicated
devices, yielding data that is conceptually simple to interpret. Alternatively, it can be performed with devices that
are designed for actual implementations of quantum algorithms. Such an approach enables a more accurate assessment of the relevant crosstalk level and can tease out
potential crosstalk mechanisms that are dominant at a
larger scale, although at the expense of a more complicated data interpretation. This work adopts the second
approach but we consider the two approaches to be equally

030350-1

Published by the American Physical Society

## PDF page 2

SANDOKO KOSEN et al.

PRX QUANTUM 5, 030350 (2024)

(a)

Q-chip
PCB
C-chip
(b)

copper lid

Q-chip

Si
Al
NbN

Bump pillar

wire bond

In

II. QUANTUM PROCESSOR ARCHITECTURE

NbN

C-chip

copper base

reasonable xy-crosstalk magnitude to aim for is such that
the total single-qubit gate error does not exceed the 0.1%
threshold recommended for quantum error correction [16].
We provide numerical estimates of the total single-qubit
gate error based on the measured xy crosstalk and sketch
the further improvement required for the total error to stay
below the 0.1% threshold for processors at the 100-qubit
level. We discuss potential sources of crosstalk, its impact
on gate ﬁdelities, and its implication for future designs of
low-crosstalk processors.

Al
Si

PCB

FIG. 1. A packaged 25-qubit superconducting quantum processor. (a) An enlargement of the ﬂip-chip processor packaged
with wire bonds and printed-circuit-board (PCB) technology.
(b) An illustration of the cross section, showing the copper lid
and base, with an enlargement showing the material stack (not
to scale—Si, silicon; Al, aluminum; NbN, niobium nitride; In,
indium).

valuable, necessary, and complementary to each other in
the long run.
In this work, we demonstrate packaged multiqubit processors consisting of 25 qubits in a ﬂip-chip module, as
shown in Fig. 1. The processor is designed according to
a repeating signal-line routing pattern, which is, in principle, scalable to hundreds of qubits. We characterize the
microwave crosstalk (selectivity of driving) of the qubit
drive lines (“xy lines”), which are capacitively coupled
to their target qubits, and of ﬂux lines (“z lines”), which
are inductively coupled to frequency-tunable couplers that
mediate two-qubit gates.
The results show crosstalk performance approaching average values of −40 dB for microwave-drive xy
crosstalk and 0.05% for direct-current ﬂux crosstalk, competitive with reported performance from other superconducting [5,8,9,11,12] and nonsuperconducting [13–15]
platforms. We show that a substantial contribution to the
ﬂux crosstalk is due to the proximity of the grounded end
of a victim z line to a neighboring source z line and it can
be suppressed either by a shielding tunnel structure or by
adequate separation. On the other hand, enclosing the xy
lines with shielding tunnels does not improve xy crosstalk
despite the denser routing layout, suggesting that the intrinsic crosstalk level due to direct capacitive interaction is
better than the observed performance (simulation of a simpliﬁed model of our processor also suggests that this is the
case).
It is generally desirable for the crosstalk level to be
not only low but also to decrease with increasing separation and our results suggest such a trend. To quantify, a

Our superconducting quantum processing unit (QPU)
consists of a two-tiered architecture [17–20] separating
the circuit into a qubit chip (“Q-chip”) and a control chip
(“C-chip”) [see Figs. 1 and 2(a)]. The Q-chip comprises 25
ﬁxed-frequency transmon (Xmon) qubits [21–23] and 40
frequency-tunable two-qubit couplers laid out on a square
grid with 2-mm pitch [24]. This relatively large pitch is
a choice made out of convenience, since the QPU performance is limited by gate performance rather than the
number of devices that can be ﬁtted on a die. The C-chip
comprises a signal-delivery system routed through coplanar waveguide transmission lines on the chip surface. This
signal-routing strategy is extensible to hundreds of qubits.
In Fig. 2(b), we show a part of the ﬂip-chip module with
the Q-chip overlaid on the C-chip.
In Fig. 2(c), we show the coupling points of the control wires to the qubit and coupler. The qubit-readout
resonators [“ro” in Fig. 2(c)] are quarter-wavelength resonators with the open end positioned directly opposite a
qubit. The resonators are undulated to reduce coupling
with neighboring couplers. The open ends of the qubitcontrol lines (xy) are positioned to ensure adequate capacitive coupling while minimizing Purcell decay of the qubit
into its own xy line. Finally, the coupler-control lines (z)
each terminate in a loop of wire that is shorted to ground
at one end, without a ground plane within the loop. The
current in the z loop couples magnetic ﬂux into the superconducting quantum interference device (SQUID) of the
coupler positioned opposite the loop; this SQUID connects
the island of the coupler to the ground plane.
The second processor discussed in this work has aluminum tunnel structures [25,26] added to the C-chip,
shielding the signal lines as shown in Fig. 2(d). These tunnels extend across the signal lines and connect the ground
planes on either side.
The Q-chip and C-chip consist of 12 mm × 12 mm and
14.3 mm × 14.3 mm silicon dies, respectively, which are
aligned and joined together by ﬂip-chip bonding, with a
target interchip separation of 8 µm. The bump-bond layout
is symmetrical across the dies, with 2900 superconducting bumps connecting the ground planes of the two tiers
and with a denser distribution surrounding the qubit and

030350-2

## PDF page 3

SIGNAL CROSSTALK IN A FLIP-CHIP QUANTUM PROCESSOR
(c) xy line and readout (ro)

Si
Al

Q-chip

NbN

(qubits,
couplers)

In

dtarget = 8 µm

NbN

C-chip

Q

Al (wiring layer)
Si (substrate)

z line

(d) Tunnel structure covering a signal line

(opposite a qubit on Q-chip) (facing a SQUID
on Q-chip)

C

I

(a)

PRX QUANTUM 5, 030350 (2024)

(side view)
3 µm

50 µm

bare signal line

(control,
readout,
interface
to PCB)

ro

(b)
2 mm

(top view)

(micrograph)

tunnel

Qubit index

(e)
11

12

13

14

15

16

17

18

19

20

21

22

23

24

25

(f) 2-frequency subgroup strategy
unit cell
b2

a1

b3

a4

b2

a3

b1

a2

b4

a3

b3

a4

b2

a1

b3

a2

b4

a3

b1

a2

b2

a1

b3

a4

b2

FIG. 2. The quantum processor architecture. (a) The two-tier ﬂip-chip material stack (not to scale). (b) An overlapped view of the
Q-chip (qubits and couplers) and C-chip (control and readout elements) for the bottom 15 qubits of a 25-qubit QPU, showing the bump
pattern (black dots). For an easier view, both ground planes are removed from this illustration. (c) Left: a transmon (Xmon) qubit
located on the Q-chip, with the xy line (qubit drive) and the readout resonator located on the C-chip. The cutout on the Q-chip layer
shows the end parts of the xy line and of the resonator. The panel on the far left shows an enlargement of the region around the tip of
the xy line. Right: a z loop (ﬂux loop) on the C-chip, the center of which lies directly opposite a superconducting quantum interference
device (SQUID) on the Q-chip (wiring and substrate on the Q-chip not shown). (d) The aluminum tunnel structure shielding a signal
line. The micrograph shows one part of the transmission line covered with a tunnel. (e) The qubit indexing used in this paper. (f) The
two-frequency subgroup strategy: the ﬁlled and empty circles indicate transmons with two diﬀerent anharmonicities; ak and bk indicate
diﬀerent qubit frequencies (ak < bk ), giving a total of eight diﬀerent frequencies that are tiled according to the schematic.

coupler devices. The bumps consist of evaporated indium
cylinders (25-µm-wide precompression) with a niobium
nitride underbump metallization layer [20].
The two-tier ﬂip-chip module represents a straightforward method for three-dimensional (3D) integration of
QPUs, oﬀering more ﬂexibility for signal-wire routing and
qubit-array layouts than planar layouts, with a modest
increase of fabrication-process complexity. It also enables
the use of diﬀerent fabrication processes for the two chips.
In more advanced 3D-integration implementations, superconducting bumps can be used to pass signals between tiers
and to provide shielding between components; hard stops
(e.g., posts or pillars) can help achieve precise interchip
separation [27,28]; furthermore, substrates with metallized
through-silicon vias (TSVs) and buried conductors can
help create signal redistribution layers [29–31].

Aluminum wire bonds along the periphery of the C-chip
transfer signals to and from a multilayer PCB (see Fig. 1).
Two wire bonds are placed on every signal launch pad and
two grounding wire bonds are placed in between neighboring signal lines. This wiring method works up to hundreds
of wires but begins to scale poorly beyond that, which is
why ultimately higher-density interconnects and packaging solutions, e.g., ball-grid arrays or land-grid arrays, need
to be adapted to superconducting QPU technology.
Our ﬂip-chip fabrication process has been demonstrated
to be compatible with qubit (transmon) coherence at the
100-µs level [20]. The wiring layer (signal and ground)
on each chip is fabricated in an aluminum process and
the Josephson junctions consist of an angle-evaporated
Al/AlOx /Al sandwich using the two-step Manhattan process [32,33]. The fabrication and packaging steps are

030350-3

## PDF page 4

SANDOKO KOSEN et al.

PRX QUANTUM 5, 030350 (2024)
We have designed and simulated the ﬂip-chip QPU
layout using a combination of the IBM QISKIT METAL
design toolkit [35], the ANSYS electromagnetic simulation
software [36], and the L-Edit layout editor [37]. The simulation technique for individual qubits and resonators is
described in Ref. [20].
Refer to Appendix D for the chosen numerical values of
the qubit frequencies, anharmonicities, readout-resonator
frequencies, and coupler frequencies at zero ﬂux bias.
Appendix E lists the measured frequency parameters and
coherence performance of both processors.
III. AGGREGATE CROSSTALK PERFORMANCE
Here, we quantify the crosstalk (unintended driving)
aﬀecting qubits and couplers due to signals applied to the
various xy lines and z lines of the circuit, respectively. To
begin with the microwave crosstalk of xy lines, consider
any pair of a victim qubit (qi ) and a source xy line (xyj ̸=i ) as
shown in Fig. 3(a). The crosstalk is quantiﬁed by the rotation of the quantum state vector of qi due to a signal being
delivered through xyj aiming to control its corresponding
qubit qj . In practice, we compare the Rabi frequency of
the victim qubit, i,j , with that of the qubit of the source
xy line, j ,j , for the same xyj signal amplitude. Due to the
low-crosstalk nature, we always drive the victim qubit on
resonance. Their ratio, expressed in decibels (dB), is the
(a)

(b)

15

source xyj

victim qi

bare

(+tunnel)

victim SQUID
source zj

(d)

bare
(+tunnel)

75

Count

(c)
Count

outlined in Appendix A. Details on the ﬂip-chip bonding
processes can be found in the supplementary material of
Ref. [20].
The qubits are labeled qi , where the index i starts in
the top left corner of the chip; see Fig. 2(e), which shows
q11 –q25 . The element xyi is the corresponding xy line for
qi . The couplers and the corresponding z lines are labeled
cpi and zi , where the index i is a pair of indices indicating the two qubits that are connected by the coupler; e.g.,
cp(11,16) is the coupler connecting q11 and q16 . The closest
separation between a qubit and another xy line (excluding
its own xy line) is about 500 µm.
The routing of signal lines is designed to be as identical
as possible for these rows of qubits: q6 –q10 , q11 –q15 , and
q16 –q20 . The control elements (xy, z) are always routed to
the desired positions from the corridor above the qubits,
while the readout elements are positioned below [see
Fig. 2(b)]. The signal lines are routed horizontally to the
periphery of the chip. In each corridor, there is always a z
line in between the closest pair of xy lines. These z lines are
needed to control horizontally oriented tunable couplers.
The vertically oriented couplers, however, are controlled
by z lines that are routed side by side. Nearest-neighbor
control lines are separated by at least 100 µm. For readout
purposes, a feed-through transmission line is routed across
each corridor and is coupled to ﬁve λ/4 resonators. Once a
signal line emerges at the qubit-array perimeter, it is routed
to the closest available wire-bond launch pad. For qubits
in the top row (q1 –q5 ), the bottom row (q21 –q25 ), and the
corresponding horizontally oriented couplers, the control
lines are routed vertically toward the closest wire-bond
launch pads. No bumps or air-bridge crossovers are used
for signal delivery, i.e., there is no intersection of signal
lines.
The allocation of qubit frequency and anharmonicity
follows the two-frequency subgroup strategy designed
to be compatible with the implementation of parametric
controlled-Z (CZ) and iSWAP gates, which avoids frequency
collision between neighboring couplers and minimizes
crosstalk due to frequency crowding [34]. Each subgroup,
labeled {ak } and {bk } (k = 1, 2, 3, 4), has four qubit frequencies that are distributed around a central frequency;
subgroup a has lower frequencies and anharmonicities than
subgroup b. The layout has a unit cell of 2 × 4 qubits
that can be repeatedly tiled as shown in Fig. 2(f). An
alternative visualization is the following: a qubit with frequency in one subgroup is pairwise coupled to qubits with
frequencies in the other subgroup.
The readout-resonator frequency allocation is set up to
ensure that at the targeted interchip separation, the qubitresonator frequency detuning is generally between 2.1 and
2.6 GHz, which provides suﬃcient leeway for tolerating
frequency shift in case the achieved chip separation is oﬀ
target. The coupler frequency at zero ﬂux bias is designed
to be above the readout-resonator frequency.

10
5

βmax

50

inset

25
Group 2

0

0
–50

–40

–30

Λ(xy) (dB)

0.0

0.13 0.25

0.4

β (dc) (%)

FIG. 3. The aggregate performance of xy crosstalk (xy) , and
dc-ﬂux crosstalk β (dc) . (a) An illustration of xy crosstalk from a
source xy line (j ) to a victim qubit (i) and (b) dc-ﬂux crosstalk
from a source z line (j ) to a SQUID loop of a victim coupler (i).
(c) The histogram of the on-resonant xy crosstalk, i,j , measured
on 72 pairs for one ﬂip-chip module with bare transmission lines
(labeled “bare”) and another module with the majority of the
transmission lines covered by “tunnel” structures (labeled “+tunnel”). (d) The histogram of the dc-ﬂux crosstalk, β (dc) , measured
on 240 pairs.The data indicated as Group 2 are associated with
a subset of pairs the z lines of which are nearest neighbor. With
the tunnels, the maximum value of the dc-ﬂux crosstalk drops to
βmax = 0.13%.

030350-4

## PDF page 5

SIGNAL CROSSTALK IN A FLIP-CHIP QUANTUM PROCESSOR

(
i,j = 10 × log10

i,j
j ,j

)2
.

(1)

The lower the magnitude of i,j , the better that xy line is
at selectively driving its corresponding qubit compared to
any other qubit (lower crosstalk).
We also characterize the magnetic ﬂux crosstalk in the z
lines by examining changes in the magnetic ﬂux (i ) that
threads the SQUID of a victim coupler cpi due to directcurrent (dc) or alternating-current (ac) signals on a source
z line (zj ̸=i ), aimed to control its corresponding coupler
cpj [see Fig. 3(b)]. The magnetic ﬂux crosstalk is deﬁned
as [38]
∣
∣
∣ i ∣
∣
∣.
(2)
βi,j = ∣
j ∣
(dc)

(ac)

(ac)

(ac)

Generally, i = i + i cos (ωi t + θi ), where ωi
is the angular frequency of the ac-ﬂux drive signal and θi
is its phase oﬀset. In practice, the dc- and ac-ﬂux crosstalk,
(dc)
(ac)
i.e., βi,j and βi,j , are characterized separately.
The measurement procedures for the xy, dc-ﬂux, and
ac-ﬂux crosstalk are discussed in Appendix C. As there
are also some defective elements in these ﬁrst-generation
processors, the data sets presented in this section are only
associated with source-victim pairs that are functional in
both processors (bare waveguides and with tunnels) to
allow fair comparisons. The complete data sets can be
found in Appendix F.
In Fig. 3(c), we show a histogram of the xy crosstalk
(xy)

with average and standard deviation values of
−39.4 ± 3.7 dB for the processor without tunnels and
−37.4 ± 3.9 dB for the processor with tunnels. These
results show that the addition of the tunnel structures
to shield the xy lines does not decrease the average xy
crosstalk for these packaged processors.
In Fig. 3(d), we show a histogram of the dc-ﬂux
crosstalk β (dc) measured both with and without the tunnel structures. Statistics from both data sets show average
values of approximately 0.05%. The data from the processor without the tunnels have outliers in between 0.3% and
0.6% (indicated as group 2), which originate from pairs
the z lines of which are not only nearest neighbor but also
arranged in a speciﬁc way (see Sec. IV). These outliers are
not present in the data from the processor with the tunnel
structures, indicating a suppression of dc-ﬂux crosstalk;
here, the maximum measured value is 0.13%. We also note
that the measured dc-ﬂux oﬀsets from the processor with
tunnels (oﬀset, tunnel /0 = −0.035 ± 0.008) are more narrowly distributed than those from the processor without
tunnels (oﬀset, no-tunnel /0 = −0.048 ± 0.044, excluding
an outlier at 0.3250 ).

As the ac-ﬂux crosstalk β (ac) measurement is more
involved, we have only characterized it for Group-2 pairs
of z lines and couplers, i.e., those that exhibit elevated dcﬂux crosstalk in the absence of tunnels. We have chosen to
characterize it at a signal frequency of 200 MHz, close to
the typical modulation frequency of our parametric couplers. Similarly to dc crosstalk, the largest ac crosstalk
drops from 0.85% to 0.24% for tunnel-covered z lines.
In Sec. IV, we examine the distance dependence of the
(xy) , β (dc) , and β (ac) data.
IV. CROSSTALK VERSUS DISTANCE
During the operation of a quantum processor, gate operations on diﬀerent qubits and couplers will be performed
simultaneously via multiple signal lines. It is therefore
important to design the QPU such that the crosstalk
decreases for larger separation. Such a property allows for
the reuse of the qubit parameters from one unit cell in
another as part of our qubit-frequency allocation scheme
[see Fig. 2(f)]. It also ensures that the total error due to
signal crosstalk remains suﬃciently small. In this section,
we begin to address this by demonstrating smaller average
crosstalk for larger separations.
We have sorted the (xy) data in Fig. 3(c) according to
the distance d(xy) between the victim qubit and the target
qubit of the source xy line; the results are shown in Fig. 4.
It should be pointed out that there are fewer data points
for larger d(xy) in Fig. 4, i.e., this is natural for planar connectivity such as that implemented in our processors. The
¯ (xy) , indidashed lines connecting average (xy) values (
cated by larger symbols of circles and crosses) hint at a
¯ (xy) with d(xy) . Fitting the average valtrend of decreasing 
ues with an empirical linear model (see Appendix J) yields
a slope of approximately −1 dB/mm for these processors.
–25
bare

(+tunnel)

d (xy)

–30

Λ(xy) (dB)

on-resonant xy crosstalk i,j (referred to as xy selectivity
in Ref. [12]),

PRX QUANTUM 5, 030350 (2024)

–35
–40
–45
–50

2

2.8

4 4.5

5.7 6 6.3 7.2

8.3 8.9

d (xy) (mm)
FIG. 4. The distance dependence of the xy crosstalk, (xy) .
The distance d(xy) is deﬁned as the separation between the victim qubit and the target qubit of the source xy line as illustrated
in the inset and further described in Sec. IV. The scatter plot indicates the distribution of the (xy) data for each d(xy) and the larger
symbols denote the average.

030350-5

## PDF page 6

SANDOKO KOSEN et al.

PRX QUANTUM 5, 030350 (2024)

For the ﬂux-crosstalk data associated with neighboring
z lines, we have measured a total of four diﬀerent conﬁgurations within the two lowest-routing corridors shown in
Fig. 2(b). Here, we focus speciﬁcally on two layouts of
neighboring z lines as shown in Figs. 5(a) and 5(b) but the
trend is similar in the other two. The ﬁrst layout consists
of the set {A, B, C} = {z(11,16) , z(12,17) , z(13,18) }, and the second consists of {A′ , B′ , C′ } = {z(16,21) , z(17,22) , z(18,23) }. The
two layouts are very similar: most of the lines are nearest
neighbors, beginning from the wire-bond launch pads and
leading all the way to the target position (see the chip layout in Fig. 2). The only major diﬀerence is in the third z
line: C’ is routed on the upper side of A’ and B’, while C

(a)

A: z(11,16)

A

(dc)

B: z (12,17)

adversary
B
C

bare

0.44%

0.58%

0.05%

A
0.00%

+tunnel
0.01%

0.05%

0.07%

0.06%

target

target

adversary
B
C

0.03%

B
0.00%

0.02%

0.01%

0.00%

0.00%

0.01%

C

0.09%

0.02%
0.10%

B
0.14%

0.13%

0.00%

0.00%

0.04%

0.06%

C

(b)

A': z(16,21)

A'

(dc)

adversary
B'
C'
0.35%

bare

C': z(18,23)

B': z(17,22)

A'

(ac)

adversary
B'
C'

0.59%

0.65%

A'

0.85%

A'
0.10%

+tunnel
0.06%

0.12%

0.14%

0.53%

target

target

A

(ac)

A

B'
0.08%

0.08%
0.03%

0.03%

n/a

n/a

C'

(dc)

0.75

0.13%

0.10%
0.50%

B'
0.24%

0.12%
0.10%

0.03%

n/a

n/a

C'

bare
(+tunnel)

dz

0.50
0.25

(ac)

0.75

β (ac) (%)

(c)

β (dc) (%)

C: z(13,18)

0.00

V. DISCUSSION
A. Qubit-drive crosstalk

bare
(+tunnel)

0.50
0.25
0.00

150

is routed on the lower side of A and B. The data with C’
as victim from the processor with tunnels are not available
due to a defective SQUID in coupler cp(18,23) .
On the ﬁrst layout without the tunnel structure, Fig. 5(a),
the highest crosstalk β (dc, 0.44%; ac, 0.58%) appears
with A as the victim and B as the source line. However,
a much lower crosstalk (dc, 0.06%; ac, 0.10%) appears
between victim B and source C despite these being nearestneighbor lines in the same way as victim A and source B.
Almost similar results are observed on the second layout
in Fig. 5(b), with the exception that substantial crosstalk is
also observed between victim A’ and source C’ (and also
between victim B’ and source C’).
Another noteworthy feature is the asymmetry of
crosstalk for nearest-neighbor lines. The eﬀect is most pronounced for the processor without tunnels. While there is
substantial crosstalk from source B to victim A (dc, 0.44%;
ac, 0.58%), much lower crosstalk is measured when the
roles of victim and source are interchanged (dc, 0.01%; ac,
0.09%). Similar asymmetry is observed in the other layout.
These observations, combined with the symmetric positioning of the wire-bond launch pads of the z lines, indicate
that the major source of ﬂux crosstalk in the processor
without tunnels is coming from the proximity of the end
(current loop) of a victim z line and the nearest section
of a source z line. Under this model, we have plotted the
ﬂux crosstalk for victim-source pairs arranged as shown
in the inset of Fig. 5(c). Without tunnels, the ﬂux crosstalk
becomes smaller for larger spatial separation dz . By adding
tunnels, the previously high ﬂux crosstalk at small separation (dz = 150 µm) decreases by close to a factor of 10,
down to the level of 0.1–0.2%. Flux crosstalk at larger
separation (dz = 250 µm) is relatively unaﬀected by the
presence of tunnels.

200

dz (µm)

250

150

200

dz (µm)

250

FIG. 5. The layout-dependent ﬂux-crosstalk behavior. (a),(b)
Detailed comparisons of the ﬂux crosstalk for two diﬀerent conﬁgurations of nearest-neighbor z lines (refer to the main text for
more detail). The darker the background color, the smaller is the
crosstalk. (c) The distance dependence of the dc- and ac-ﬂux
crosstalk for source-victim pairs arranged as shown in the inset,
where the red arrow indicates the source current. The dashed
lines connecting the data points are meant as a guide to the eye.

A distinct feature in this processor is the presence of
densely routed signal lines in the proximity of qubits
within the ﬂip-chip environment [see Fig. 2(b)]. However, for xy crosstalk, direct capacitive interaction between
qubits and these signal lines cannot be the dominant mechanism, since we do not observe any decrease in average
crosstalk after covering the xy lines with shielding tunnel structures [see Figs. 3(c) and 4]. This conclusion is
consistent with several electrostatic simulations designed
to study the expected impact of the tunnel structure and
xy-crosstalk level due to the direct xy-qubit capacitive
interaction. First, we simulate a simpliﬁed model containing two victim qubits (denoted as q1 and q2 ) and two source
xy lines (denoted as xy3 and xy4 ) under two situations: with
and without a tunnel structure on xy4 (see Appendix G).
The result shows that while the coupling capacitances

030350-6

## PDF page 7

SIGNAL CROSSTALK IN A FLIP-CHIP QUANTUM PROCESSOR
between xy3 and both qubits remain unaﬀected, the coupling capacitances between xy4 and both qubits are lower
when the tunnel structure is present on top of xy4 . Second,
we simulate the expected xy-crosstalk level that is solely
caused by the direct capacitive interaction between the xy
lines in the processor (excluding wire bonds, PCB signal
traces, and tunnels) and the qubits (see Appendix H). The
result puts the expected xy-crosstalk level within the range
of −49 dB to −150 dB, much smaller than the measured
xy-crosstalk level in our work.
The average of (xy) is −36 dB for the nearest-neighbor
pairs (d(xy) = 2.0 mm) and −37 dB for the next-nearestneighbor pairs (d(xy) = 2.8 mm). The highest values are
−30 dB for both nearest and next-nearest neighbors.
This performance compares favorably with results from a
17-qubit processor (in a single-chip geometry) employed
in Ref. [11] for the demonstration of distance-three
quantum error correction. There, the highest crosstalk
among the reported values for next-nearest-neighbor qubit
(d(xy) = 2.4 mm) was −20 dB (excluding one outlier at
−4 dB). It is not straightforward to identify the factors
that have led to the lower xy-crosstalk level demonstrated
in our work despite having a denser signal-line layout.
However, there are good reasons to believe that the chip
geometry is important. The electric ﬁeld of a coplanar
waveguide is more conﬁned in a ﬂip-chip geometry than
in a planar chip, due to the presence of a ground plane on
the opposing chip (the typical size of a transmission line
is approximately 10 µm and our chip separation is 8 µm)
[20]. Additionally, in a single planar chip, the signal lines
can interact parasitically with qubits via the ﬁeld in the
substrate, whereas in our ﬂip-chip module, the signal lines
and qubits are separated onto diﬀerent chips.
The data for (xy) are sorted according to the qubitqubit distance d(xy) in Fig. 4 purely for a scaling argument.
We believe that for a signal-delivery architecture to be
scalable, not only should (xy) decrease with d(xy) but
the behavior should not be too dependent on the architecture itself. Such a behavior would not only unlock
favorable scaling behavior but it would also simplify the
hardware design process by reducing the number of factors that need to be accounted for. When combined with a
judicious choice of qubit-frequency allocation and a substantial decrease in (xy) for increasing d(xy) , it can lead to
very low total crosstalk error. Having said that, the relatively large spread of (xy) for every qubit-qubit distance
d(xy) in Fig. 4 provides a clue that the major parasitic interaction in our processors does not have a strong dependence
on d(xy) . The dominant source of crosstalk must therefore
be sought elsewhere. Nevertheless, there is a hint of lower
crosstalk for larger separation when comparing the average
value of (xy) versus d(xy) , suggesting a favorable scaling
behavior, at least for the size of processors examined in
this work.

PRX QUANTUM 5, 030350 (2024)

An alternative to ﬂip-chip geometry called the “coaxmon” has reported nearest-neighbor (d(xy) = 2 mm)
crosstalk (xy) ∼ −56 dB, roughly 20 dB better than the
result reported in this work [12]. This has been obtained
using a smaller 2 × 2 qubit chip (5 × 5 mm2 ) in an enclosure that is inductively shunted at the center to repel the
cavity modes to higher frequencies, an additional feature
that is yet to be present in our system. It will be interesting to compare the crosstalk performance between the two
geometries for increasing processor size.
Going forward, a combination of experimental investigations on more dedicated devices and numerical
validations will be useful to further understand various
xy-crosstalk mechanisms and conﬁgurations in which they
might prevail. Electromagnetic modeling of the whole
system (chips, wire bonds, packaging), such as the one presented here, is computationally challenging due to the wide
range of feature sizes (several micrometers for signal lines
to several centimeters for the packaging) that need to be
accounted for.
In this work, we have instead taken an alternative
approach of simulating simpliﬁed versions of the model to
understand the relative impact of direct capacitive interaction and the proximity of the signal lines to the xycrosstalk level. As discussed before and in more detail in
Appendix H, the expected xy-crosstalk level caused by the
direct xy-qubit capacitive interaction between the qubits
and the signal lines (excluding the wire bonds, PCB signal traces, and tunnels) is between −49 dB and −150
dB, with an average of −94 dB, which is much smaller
than the range measured in this work. In addition, we
simulate the expected microwave crosstalk between neighboring signal lines in a simpliﬁed model consisting of ﬁve
signal lines beginning at the PCB level all the way into
the ﬂip-chip environments (Appendix I). The results show
nearest-neighbor and next-nearest neighbor crosstalk at the
level of −55 dB and −69 dB at the PCB level, which are
then substantially increased to −40 dB and −49 dB after
including the wire bonds and signal launch pads. Further
extension of the signal lines into the ﬂip-chip environment does not substantially change the crosstalk level, a
trend that is attributed to the much smaller geometry of the
transmission line compared to the line-to-line separation.
Crucially, the closest pair of xy lines in our processor is
at least in a next-nearest neighbor conﬁguration, as there
is at least one z line needed to control the tunable coupler
connecting two neighboring qubits. The simulation puts a
bound of around −47 dB to the next-nearest neighbor signal lines, which is still one order of magnitude smaller than
the average xy crosstalk measured for qubits controlled by
the next-nearest neighbor pairs of xy lines (−36 dB).
The xy-crosstalk performance of our quantum processors compares competitively with those demonstrated in
trapped ions [13,39–44], neutral atoms [14,45,46], and

030350-7

## PDF page 8

SANDOKO KOSEN et al.

PRX QUANTUM 5, 030350 (2024)

spin qubits [15,47]. In trapped-ion systems, the lowest nearest-neighbor crosstalk (without active cancellation) has been reported to be 0.2% for a linear chain
of four 171 Yb+ ions, which is equivalent to an individual excitation-error probability of 10−5 [13]. In our
case, the qubit-frequency allocation strategy results in
nearest-neighbor qubits that are naturally far detuned. For
R /2π = 25 MHz and with the smallest nearest-neighbor
detuning being 420 MHz, the individual excitation-error
probability is already at the level of 10−6 ; larger detuning will further reduce the signal-crosstalk-induced error
probability. Neutral-atoms systems have reported an average spin-ﬂip crosstalk probability of 2 × 10−3 on a twodimensional array of 49 Cs atoms [14]. Spin-qubit systems,
such as the four-atom Ge processor in Ref. [15], show an
average individual single-qubit gate error between 10−2
and 10−4 .
B. Flux crosstalk
The ﬂux-crosstalk data [Figs. 5(a) and 5(b)] clearly illustrate speciﬁc conﬁgurations of z lines that cause some of
the largest ﬂux-crosstalk values measured in our processors (between 0.4 and 1%). We have demonstrated two
strategies to achieve lower ﬂux crosstalk. The ﬁrst strategy
uses a tunnel structure to suppress crosstalk for the same
pairs of z lines below approximately 0.2%. This conclusion
is only made possible due to the use of identical signalline footprints in the two devices. The second strategy is by
ensuring a suﬃciently large separation dz between the head
of the victim z line and the closest point of a source z line,
in our case dz = 250 µm. Further investigation is needed
to pinpoint precisely the cause of crosstalk reduction due
to the tunnel structure: whether the tunnel prevents current leakage to the victim z line and/or if it suppresses the
direct interaction between the source z line and the victim
SQUID.
The average dc-ﬂux crosstalk β (dc) over all measurable pairs is approximately 0.05%. At least another
tenfold reduction is possible through active ﬂux compensation, potentially pushing the dc-ﬂux crosstalk level below
0.01%. A similar reduction has also been demonstrated
in a 16-qubit processor [8]. Note that the passive stability of our system is much better: a variation of 32 µ0 is
measured for one of the z lines over a period of 3 h, corresponding to a lowest measurable β (dc) = 0.003% (for more
information, see Appendix C 2).
The relative standard deviation of dc-ﬂux oﬀset in the
processor with the tunnels (±0.0080 , 23%) is smaller
than the value in the processor without the tunnels
(±0.0440 , 92%). In our system, we believe that the dcﬂux oﬀsets are determined by the magnetic ﬁeld present
in the system when the aluminum ﬁlm becomes superconducting. The magnetic ﬁeld can be due to the remnant static
ﬁeld generated by sources external to the processor as well

as any circulating current in it. The two processors are
measured in the same cryogenic environment, except for
the diﬀerent PCBs, oxygen-free high-thermal-conductivity
copper base plate and cover lid, and screws. The remnant
static ﬁeld should, in principle, remain the same at the base
temperature and this is likely reﬂected in the nonzero average values. In addition, the input current into each z line
is always set to zero during the cool-down. Therefore, it
is not straightforward to determine the role of the tunnel
structure in narrowing down the dc-ﬂux oﬀset distribution
solely from the data presented in this work.
There is a varying degree of tolerable β (dc) performance.
An active ﬂux-calibration technique applied to devices
for quantum annealing applications achieves a maximum
calibration error of 0.17% [5], which is still higher than
the passive performance already obtained by our architecture. In another work employing a superconducting
quantum simulator to study many-body dynamics, β (dc)
has been reduced from 6% down to 0.01% through active
compensation [9].
Overall, this work demonstrates that careful routing
and shielding of z lines can already enable low crosstalk
without active ﬂux compensation. The crosstalk performance can be compared with various leading devices (ﬂipchip, single-chip) where the maximum ﬂux crosstalk (no
compensation) varies between 0.8% and 40% [5,9,11,
38,48–50]. In Refs. [49,50], the authors have noted an
improvement in maximum ﬂux crosstalk down to the level
of 1.6% when moving from single-chip to ﬂip-chip geometry on nominally similar chip sizes, attributed to the use of
a smaller SQUID area. Meanwhile, Ref. [11] has already
registered a maximum ﬂux crosstalk of 0.8% on a singlechip geometry, lower than those achieved in Ref. [50]. The
use of air-bridge crossovers meant to stitch the ground
plane of a z line does not immediately result in full
crosstalk reduction, as demonstrated by Ref. [48], where
the authors have measured ﬂux crosstalk of between 0.1%
and 4%. Finally, we note that in Ref. [51], the author has
obtained β (dc) = 0.8%, despite using a z line with a dedicated return-current line. This illustrates the complex story
of ﬂux-crosstalk improvement eﬀorts and the signal-line
architecture presented in this work is proof that it is still
possible to achieve lower crosstalk via careful design. Further investigations are required to understand the source of
ﬂux crosstalk at the 0.1% level.
C. Impact on gate fidelities
It is instructive to understand the detrimental eﬀect
of the xy-crosstalk performance on the single-qubit gate
ﬁdelity. In previous work, we have calculated the ﬁdelity
using the relative coupling strength between the relevant
processes and detuning between the associated transitions
[34]. The calculation models the qubits as two-level systems and assumes that the crosstalk activates undesired

030350-8

## PDF page 9

SIGNAL CROSSTALK IN A FLIP-CHIP QUANTUM PROCESSOR
processes one by one. The measured (xy) varies between
−56 dB and −27 dB, which corresponds to relative coupling strengths between 0.15% and 4%. Assuming a 20-ns
single-qubit gate, the worst (xy) of −27 dB would require
detuning between the relevant qubit transitions larger than
28 and 42 MHz (about 1% of typical qubit frequencies)
to have average gate ﬁdelities above 99.9% and 99.99%,
respectively.
The limits are more stringent when we consider inﬂuence from all other qubits on the chip. We examine the total
single-qubit gate ﬁdelity F1Q for increasing processor size.
We assume an empirical linear behavior of ¯
(xy) on d(xy)
and numerically simulate the impact on F1Q under certain
assumptions (see Appendixes J–L). For the data in Fig. 4,
the slope mxy and intercept 0 values of the empirical
linear model are approximately −1 dB/mm and −34 dB,
respectively. The simulations suggest, for QPUs with up to
1000 qubits, that an improvement to −2.0 dB/mm and −50
dB would result in a total single-qubit gate error (due to xy
crosstalk) well below the 0.1% threshold recommended for
quantum error correction using the surface-code [16]. This
¯ (xy) versus d(xy)
conclusion assumes linear dependence of 
for processor sizes beyond the one measured in this work.
We have no reasonable physical argument to assume that
it will be the case; nevertheless, this number can serve as a
guide for future hardware development and can hopefully
spur further eﬀort in verifying this relation for larger processors. Note that a sparser lattice architecture, such as the
heavy square or the heavy hexagon, will beneﬁt from less
stringent criteria due to fewer neighboring qubits and more
relaxed frequency constraints [52].
It is more challenging to analyze the inﬂuence of ﬂux
crosstalk on the two-qubit gate ﬁdelity, since the gate
strength depends on both the dc bias and the ac amplitude
in a nontrivial way (ωcp () is nonlinear). However, there
is a relevant situation for which the analysis becomes simpler, at least qualitatively: a parametric gate is applied to a
coupler while the other ones idle. Two related conditions
arise in that case: (1) the driving amplitude produced on the
idling couplers will be very small for low crosstalk such as
the one measured in this work, allowing for a perturbative
expansion; and (2) the dc contribution stemming from the
periodic modulation will be negligible, as it is a higherorder eﬀect in the small-amplitude perturbative expansion.
Furthermore, as the dc bias usually stays untouched during the parametric-gate operation, the eﬀect of dc crosstalk
on the idling couplers should not change during the gate
operations.
An expression for the ﬁrst-order contribution to the
gate strength of the iSWAP gate is known for this smallamplitude expansion [53], although the result is limited to
the regime in which the detunings between the coupler and
the qubits are much larger than their coupling strengths.
The expression clearly shows that the gate strength is less
sensitive to changes in both ac amplitude and dc bias near

PRX QUANTUM 5, 030350 (2024)

the zero-ﬂux bias region. This region is also where the couplers are typically more far detuned from the qubits, thus
avoiding the physical consequences of being near avoided
level crossings, i.e., Rabi oscillations or extra phase acquisition. Therefore, the general prescription to avoid a large
impact of crosstalk during the application of parametric
gates would be to idle the other couplers to be as far
detuned as possible from the neighboring qubits.

VI. CONCLUSIONS AND OUTLOOK
We have demonstrated superconducting quantum processors utilizing an on-chip signal-delivery architecture
with competitive crosstalk performance—average onresonant xy crosstalk approximately 40 dB, average
dc-ﬂux crosstalk approximately 0.05%—surpassing the
majority of those demonstrated in other physical platforms.
The systematic comparison enabled by adding a tunnel
structure on an identical signal-line footprint combined
with electrostatic simulations shows that the direct capacitive interaction between densely routed signal lines and
the qubits is not the main contributor to the xy-crosstalk
level in these processors. Electromagnetic simulation of
the microwave crosstalk between neighboring signal lines
indicates a crosstalk level that is still one order of magnitude smaller than our measured xy-crosstalk level. Our
work demonstrates wiring layouts that can lead to ﬂux
crosstalk at the approximately 1% level and strategies to
reduce it down to approximately 0.1%.
Further investigations into the source of crosstalk would
be required before proposing reliable mitigation strategies;
the lists below are nonexhaustive. For xy crosstalk, there
are at least three possible avenues to investigate. The ﬁrst
is to numerically investigate the additional xy crosstalk
caused by the direct capacitive interaction between a victim qubit and the PCB signal traces, including the wire
bonds. While they are further away from the qubits, they
are also much larger in size compared to the on-chip signal
lines. The second is to investigate the role of packaging cavity modes in inﬂuencing the xy-crosstalk level, as
suggested in Ref. [54]; in particular, the indirect xy-qubit
interaction mediated by the cavity modes. The third is
to investigate the indirect xy-qubit interaction mediated
by other elements in the processor such as the qubits,
the couplers, the readout resonators, and possible parasitic
modes. For ﬂux crosstalk, it will be instructive to investigate if it is limited by the leakage of the return current
into the victim line (around the launch pads or the area
around the SQUID) or if the return current is contributing
non-negligible magnetic ﬂux at the location of the victim
SQUID.
More advanced signal-delivery architectures will beneﬁt from the use of on-chip signal multiplexers, bumps,
and especially redistribution layers enabled by TSVs in a

030350-9

## PDF page 10

SANDOKO KOSEN et al.

PRX QUANTUM 5, 030350 (2024)

multitiered stack [29–31,55,56]. Bumps and TSVs are typically a few tens of micrometers in size, which is relatively
large compared to typical transmission lines. The extent
to which they inﬂuence the overall signal-crosstalk level
remains to be seen.
The low crosstalk demonstrated in this work and other
cited works highlights the strength and ﬂexibility aﬀorded
by superconducting circuit architectures. There is still no
clear lower limit for the achievable passive crosstalk performance via further system design. We hope to inspire
further eﬀorts and discussion in the quantum hardware
community, both within and outside superconducting platforms, to investigate the source of crosstalk as well as its
behavior as systems scale up in size.
The data that support this work are available from the
corresponding author upon reasonable request.
ACKNOWLEDGMENTS
This work was funded by the Knut and Alice
Wallenberg (KAW) Foundation through the Wallenberg Centre for Quantum Technology (WACQT) and
the European Union Flagship on Quantum Technology HORIZON-CL4-2022-QUANTUM-01-SGA project
101113946 OpenSuperQPlus100. We are grateful to
Eleftherios Moschandreou for the technical support. We
acknowledge the use of support and resources from Myfab
Chalmers, the National Academic Infrastructure for Supercomputing in Sweden (NAISS), and the Swedish National
Infrastructure for Computing (SNIC) at Linköping University (partially funded by the Swedish Research Council
through Grant Agreements No. 2022-06725 and No. 201805973).
S.K. planned and performed the experiments, analyzed
the data, and produced the numerical simulations. S.K. and
H.X.L. designed the QPU with inputs from M.R., R.R.,
J.F.P., A.O., A.F.R., D.S., A.F.K., G.T., and J.Byl. M.R.,
S.K., A.N., and H.X.L. fabricated the control and quantum chips with inputs from J.Biz, A.O., and A.F.R. M.C.
and L.G. formed the In bumps and performed the ﬂipchip bonding. R.R., G.T., and S.K. developed the QPU
packaging. C.K. assisted with the writing of measurement
instrument drivers. S.K., L.C., C.K., H.X.L., and G.T. set
up and maintained the measurement and cryogenic facilities. S.K. and J.Byl wrote the manuscript with input from
all authors. G.T., J.G., and J.Byl supervised the project.
R.R., G.T., and S.K. are cofounders and shareholders
of Scalinq AB. The other authors declare no competing
interests.
APPENDIX A: FABRICATION AND PACKAGING
In this appendix, we outline the fabrication and packaging steps of the processors used in this work. The overall procedure, with the exception of the tunnel-structure
fabrication, closely follows Refs. [20,32,57].

The ﬁrst fabrication steps are done on our 2-in. wafers
at Chalmers University of Technology. We use two highresistivity intrinsic silicon wafers: one containing four
designs of C-chip, while the other has four designs of Qchip. The fabrication process of the ground and wiring
layer follows the “Chalmers standard fabrication process”
outlined in Ref. [57]. Each wafer goes through the SC-1
process, then a deionized- (DI) water rinse, followed by a
1-min dip in a 2% aqueous solution of hydroﬂuoric acid,
before another round of DI-water rinse. The wafer is blow
dried using nitrogen gas and is immediately loaded into
the load-lock chamber of an electron-beam evaporator to
minimize the reoxidation of the silicon surface. Inside the
vacuum chamber, the wafer is heated to 300◦ C for 10 min
and is left to cool down over the course of approximately
20 h. Then, a 150-nm-thick aluminum ﬁlm is evaporated
on the wafer, followed by static oxidation of the exposed
aluminum surface for 10 min before we unload the wafer
from the evaporator.
Next, a 50-nm-thick niobium nitride ﬁlm is sputtered on
electron-beam patterned resists (after an in situ ion-milling
step to remove the oxide layer on top of the aluminum
ﬁlm), followed by a lift-oﬀ process to create the underbump metallization layer on each wafer. Then, the ground
and wiring layer is formed on the aluminum ﬁlm using
optically patterned resists followed by a wet-etching step.
On the wafer containing the Q-chips, we form crosstype Josephson junctions using a two-step process similar
to that of Ref. [32]. The ﬁrst step is to pattern the junction
electrodes on a resist stack using electron-beam lithography, followed by a two-angle evaporation technique (aluminum junction) in an electron-beam evaporator, and then
a lift-oﬀ process. The second step is to form the patch layer
connecting each junction with the rest of the qubit circuitry.
The patch layer is electron-beam patterned on a resist
stack, followed by ion milling the exposed wiring layer
and aluminum-ﬁlm deposition, after which we perform a
lift-oﬀ process.
In parallel, we form the tunnel structures following
Ref. [25], on the wafer containing the C-chips. First, we
optically deﬁne a pattern of the tunnel “foot” across the
wafer on a resist layer, which is then reﬂowed to form
the arch of the tunnel. Then, we perform ion milling on
the exposed ground plane before evaporating another aluminum ﬁlm for the tunnel structure. At this point, the
tunnel foot region is the only place where the aluminum
tunnel structure is in contact with the ground plane of the
chip. Next, we add a second resist on top of the wafer and
optically expose the area that is not part of the tunnel structure. The wafer then goes through a wet-etching process
before we remove the rest of the resists from the wafer.
We package both wafers in an antistatic bag and send
them to VTT. There, 8-µm-tall indium pillars are formed
on both wafers on an optically patterned resist layer with a
side proﬁle optimized for lift-oﬀ. The wafers are then diced

030350-10

## PDF page 11

SIGNAL CROSSTALK IN A FLIP-CHIP QUANTUM PROCESSOR

APPENDIX B: EXPERIMENTAL SETUP
In Fig. 6, we show the measurement apparatus employed
in this work at cryogenic and room temperature.
APPENDIX C: MEASUREMENT TECHNIQUES
1. The xy crosstalk
The xy crosstalk i,j [Eq. (1)] is the ratio of the
on-resonant Rabi frequencies squared, i.e., (i,j / j ,j )2 ,
expressed in decibels for a ﬁxed drive amplitude Vj . We
obtain a series of Rabi frequencies for various drive amplitudes [Fig. 7(a)] and ﬁt the data with a linear relation

0 dB
0 dB

xy z(ac)

z(dc)

300 K
dc
IQ

dc
QBlox S4g

ZI HDAWG

ro

HEMT

0 dB
–20 dB
–10 dB

0 dB
–20 dB
–10 dB

0 dB
–20 dB

ro(out)

dc

up/down
dc conversion

–10 dB

SMA feed-through
Mini-circuits
VLFX-1100
RLC Electronics
RLC F-30-8000R
Keenlion
KL KBF-4/8-2S

VLFX

HEMT

KL

–20 dB

T (dB)

10
1
self Rabi (j,j)
cross Rabi (i,j)

0.0 0.3 0.6 0.9 1.2
Vp (V)

–99
–100
–101
–102
3.0 3.3 3.6 3.9 4.2
f (GHz)

FIG. 7. The xy-crosstalk measurement. (a) The measured Rabi
frequencies as a function of the drive amplitude for the self-drive
(i = j ) and cross-drive (i ̸= j ) cases. (b) An example of the combined output and transmission characteristics of an rf source with
the cables and components all the way down to the PCB level
(measured at room temperature).

i,j = ki,j Vj to obtain the slope ki,j . We obtain kj ,j in a separate measurement. i,j is then equal to the ratio (ki,j /kj ,j )2
expressed in decibels.
We operate the radio-frequency (rf) source (Rohde
& Schwarz SGS100A) in IQ modulation mode. We
ﬁx its output power to 14 dBm and vary the amplitudes Vj of the signals sent to its IQ input ports.
For each Vj , we obtain a Rabi oscillation and ﬁt it
with an exponentially decaying sinusoidal function. In
Fig. 7(a), we show i,j and j ,j versus Vj for i = 15,
j = 14.
In the measurement of i,j , we take into account the frequency dependence of the transmission of the cables and
components, measured using a vector network analyzer at
room temperature. We measure the output characteristic of
the rf source for diﬀerent frequencies with a spectrum analyzer (Rohde & Schwarz FSL18, frequency span 1 MHz,
intermediate frequency bandwidth 10 KHz, 20 averages,
101 points). In Fig. 7(b), we show an example of the
transmission characteristics of the cables and components.
2. The dc-flux crosstalk

Legend:

RLC

–20 dB
RLC

0 dB
–20 dB

–97
–98

ZI UHFQA

LNF-ISISC4_8A

Packaged QPU

(b)
100

300 K

–10 dB

10 mK

ro(in)

RLC

100 mK

–10 dB

800 mK

0 dB

3K

xy

0 dB

50 K

z(ac)

VLFX

z(dc)
300 K

(a)
Ω/2 (MHz)

into chips before being ﬂip-chip bonded at room temperature. The chip separation is characterized by measuring
the distance between the two chips at the various edges of
the ﬂip-chip module using a scanning electron microscope.
The ﬂip-chip modules are then sent back to Chalmers.
At Chalmers, we glue the ﬂip-chip module or processor on the four corners using GE varnish and let it dry
overnight. Afterward, aluminum wire bonds are applied
using an automatic wire-bonding machine. The packaged
module is ﬁnally installed at the mixing chamber stage of
the dilution fridge.

PRX QUANTUM 5, 030350 (2024)

LNF-LNC4_8C

R&S SGS100A

FIG. 6. The measurement apparatus at cryogenic and room
temperature.

The ﬁrst step in the characterization of ﬂux crosstalk is
to relate the direct current I of the z line with the magnetic ﬂux (dc) applied to the SQUID of the coupler [see
Figs. 2(c) and 3(b)]. This is done via continuous-wave (cw)
frequency spectroscopy of the neighboring qubit (which is
coupled to the victim coupler) [an example is shown in
Fig. 8(a)]. When the coupler comes close to resonance with
the qubit, we observe an avoided crossing. By identifying
a series of such crossings, we are able to deduce the current required to apply one ﬂux quantum to the SQUID, as
well as the dc oﬀset current corresponding to the true zero
dc-ﬂux bias on the SQUID. In our case, one ﬂux quantum
(0 = 2.067 × 10−15 Wb) corresponds to approximately
3 mA.

030350-11

## PDF page 12

SANDOKO KOSEN et al.

3.0

I (mA)

1.5
1ﬂux quantum

0.0

–1.5
–3.0
–1.5

peak
ﬁt

1.6
0.0
–1.6
–3.2
8

0.0
1.5
Detuning (MHz)

(c) 3

(d)

3

peak

2
1

10

–1 0 +1

Signal (arb. units) Φsource/Φ0

Isource (mA)

Time (h)

(dc)

(b)
×103 3.2
(Φvictim/Φ0 –a0)

(a)

PRX QUANTUM 5, 030350 (2024)

raw
compensated

0

–3

0
–8

–14 –12 –10 –8
Detuning (MHz)

0
8
I + 1062 (μA)

FIG. 8. The dc-ﬂux crosstalk measurement. (a) Qubitfrequency spectroscopy versus current I applied to a neighboring
tunable coupler. Detuning refers to the frequency diﬀerence
between the probe tone and the qubit at I = 0. The avoidedcrossing regions are used to probe for small shifts in the coupler
frequency due to qubit-coupler hybridization. The “1 ﬂux quantum” label refers to the magnetic ﬂux periodicity of the coupler
frequency. (b) The shift in the ﬂux victim of the victim coupler
versus the ﬂux source of the source coupler. Each curve in the
left panel represents a narrow vertical slice of the data in (a)
in the vicinity of one of the avoided crossings (a0 = 0.365696).
For each source , we have extracted victim as shown in the right
panel. The slope yields the dc-ﬂux crosstalk coeﬃcient (here,
|βi,j | = 0.13%). (c) Repeated qubit-frequency spectroscopy for 3
h to demonstrate the stability of the system. Here, we have ﬁxed
the probe frequency and varied the current I at the neighboring
coupler. (d) A demonstration of active dc-ﬂux compensation by
subtraction of the crosstalk.
(dc)

To measure dc-ﬂux crosstalk βi,j [Eq. (2)], the victim
coupler cpi is ﬁrst biased close to one such avoided crossing. In the absence of a dedicated coupler-state readout
resonator, this is a sensitive region to probe β (dc) through
qubit-state readout. A small shift in the frequency of cpi ,
from fp to fp′ , can be inferred from the change in the
hybridized coupler-qubit frequency fp , imparted by the
source current Ij . In an ideal condition with zero crosstalk,
(dc)
i.e., βi,j = 0, fp is independent of the value of the current
Ij applied on source zj . Due to non-negligible crosstalk, fp′
will shift slightly as a function of Ij and the goal is to ﬁnd
the new current value Ii′ that restores fp′ to fp . In practice,
we ﬁx the qubit probe frequency fp (typically approximately 10 MHz away from the qubit bare frequency) and
determine Ii′ for three diﬀerent dc currents Ij corresponding to source coupler (cpj ) ﬂux bias values −0 , 0, and 0

[an example is shown in Fig. 8(b)]. Then, we obtain βi,j
by converting Ii′ to the corresponding ﬂux applied on zi .
In Fig. 8(c), we demonstrate the passive stability of the
dc-ﬂux environment of a z line for 3 h. There, we have
repeatedly swept the input current to the z line while maintaining the same probe frequency. From the positions of the
extracted peak, we have obtained a standard deviation of
the variation of the current to be 100 nA—or, equivalently,
32 µ0 —which is smaller than the minimum step in output current allowed by the source (approximately 380 nA).
Furthermore, this ﬂux variation is much smaller than the
typical dc-ﬂux crosstalk observed in our system, which is
around 500 µ0 when 1 0 is applied to the source z line.
We also demonstrate active dc-ﬂux compensation on
one of the victim z lines using the obtained crosstalk coefﬁcient, as shown in Fig. 8(d). As the dc ﬂux on the source
line is varied between −0 and 0 (the vertical axis is displayed in the equivalent unit of current), the range of variation in the resonance frequency (horizontal axis) drops
more than tenfold (when compared to the uncompensated
version, labeled as “raw” in the ﬁgure), from 7.12 MHz to
0.53 MHz. Further studies are required to understand this
number and optimize the crosstalk-calibration procedure to
push it below the limit allowed by the measurement setup.

3. The ac-flux crosstalk
For the case of ac-ﬂux crosstalk, interference between
ac-ﬂux signals applied to the victim z line and parasitic
signals from the source z line renders the technique used
for dc-ﬂux crosstalk measurement inapplicable. Instead,
we employ a modiﬁed Ramsey-pulse sequence following
Ref. [38]. We ﬁrst give an overview of this technique
before describing the calibration and measurement steps
leading up to the crosstalk data.
First, consider a qubit-coupler system (qi , cpi ). The original Ramsey-pulse sequence consists of two frequencydetuned π/2 pulses on the qubit, separated by an idle
time t [see Fig. 9(a)]. By measuring the qi population
as a function of t, we obtain a Ramsey fringe the oscilq
lation frequency δω = ωi − ωdrive of which corresponds
precisely to the detuning between the applied pulse and
the actual frequency of qi . In the modiﬁed Ramsey-pulse
(ac)
sequence, an ac-ﬂux pulse at angular frequency ωi is
also applied to the coupler, via zi , during that idle duration, as shown in Fig. 9(a). This ac pulse modulates the
qubit frequency and consequently also the detuning, which
makes the observed δω sensitive to the applied ac-ﬂux
pulse amplitude.
Now, we modulate the victim coupler cpi through a
(ac)
source line zj to quantify the ac-ﬂux crosstalk βi,j . The
victim coupler is biased at speciﬁc dc-ﬂux and ac-ﬂux bias
(ac)
points (angular frequency ωi , phase θi ) chosen to render
it susceptible to the detection of parasitic ac-ﬂux signals.

030350-12

## PDF page 13

SIGNAL CROSSTALK IN A FLIP-CHIP QUANTUM PROCESSOR
(a)

(ac)

ac-flux signal interference
2V (ac)i
victim
θi

ac-flux crosstalk
ac-flux calibration
original Ramsey
xy
victim
zi

source

source
zj

θj
Δθ

(b) 0.8

2V (ac)j

(c)

Φ (ac)i /Φ0

V (ac)i (volt)

0.08
0.6
0.4
0.2

0.06
0.04
0.02

Data

Simulation
0.00

0.0
0

1

2

3

0

1

(µs)
V (ac)i (volt)

δω/2π (MHz)

0

0.34

2
ac-bias point

1

Data
Fit, k = 8.6

0
0.00

0.04

Φ(ac)i /Φ0

(e)

0.08

3

ac-ﬂux crosstalk

0.68

δω/2π (MHz)

(d)

2

(μs)

1.20
1.15
Δ(δω/2π)

1.10
Data
Fit

1.05
0

2

3

(ac)

FIG. 9. The ac-ﬂux crosstalk measurement. (a) The controlpulse sequence. (b) The data obtained from running the ac-ﬂux
(ac)
calibration sequence for a series of ac voltages Vi . (c) The simulated version of the data in (b), using the measured parameters
(ac)
of the device for a series of i . (d) Fits of the extracted frequency δω of the data in (b) to the simulation in (c), assuming a
linear relation V(ac) = k((ac) /0 ). The star symbol indicates the
typical ac-ﬂux bias point. (e) The measured δω for 0 < θ < 3π
in the presence of source ac ﬂux. The oscillation amplitude (the
swing of δω) is proportional to the ac-ﬂux crosstalk β (ac) as
discussed in the text.
(ac)

modiﬁed Ramsey-pulse sequence. We measure δω for a
range of phase oﬀsets θ = |θj − θi | spanning [0, 3π ],
as shown in Fig. 9(e). The maximum swing of δω (or
(δω)) corresponds to an equivalent ac-ﬂux shift in cpi :
(ac)
(ac) (ac)
i = 2βi,j j .
In practice, we proceed with the following steps: (1)
relate (ac) to the ac-voltage amplitude V(ac) applied by
the instrument, (2) make a choice of dc- and ac-ﬂux bias
points for the victim cpi , (3) apply a large ac-ﬂux signal
on the source zj , and (4) run the sequence in Fig. 9(a)
(ac)
and relate the measured swing (δω) to i at the bias
(ac)
point, which in turn enables the determination of βi,j .

(ac)

(δω)/2j .
APPENDIX D: TARGET FREQUENCIES

The allocation of qubit frequencies in this processor follows the two-frequency subgroup strategy as described in
Ref. [34] and in Sec. II. The readout-resonator frequencies
are arranged to maintain qubit-resonator detunings that are
above 2 GHz throughout the processor. All couplers are
identical and the target frequency at the zero-ﬂux bias is
7.9 GHz. In Fig. 10, we show the target qubit frequencies (f01 ), the anharmonicity (η), and the readout-resonator
frequencies (fr ).

=

(ac)
ωi , will cause a noticeable shift in δω obtained via the

(ac)

To relate Vi to i for any pairs of zi and cpi , we
run the ac-ﬂux calibration pulse sequence in Fig. 9(a). In
Fig. 9(b), we show the measured Ramsey fringes for a
(ac)
range of voltages Vi . In parallel, we run a QuTiP simulation [58,59] of this pulse sequence using the measured
parameters of the qubit, the qubit drive, and the coupler
zero-ﬂux bias frequencies. This simulation leads to equiv(ac)
alent Ramsey fringes for a range of i ; an example is
shown in Fig. 9(c). Finally, the extracted frequencies of
the measured and the simulated Ramsey fringes are ﬁtted
(ac)
to each other by assuming a linear relation, i.e., Vi =
(ac)
ki (i /0 ). In our setup, we typically obtain ki in the
range from 6 to 10.
The choice of dc-ﬂux bias points is made by following
the typical bias points that we use for two-qubit gate operation, which are around 0.30 [20]. The ac-ﬂux bias point is
generally chosen for maximum sensitivity to small changes
in ac ﬂux; an example is shown in Fig. 9(c). For the ac-ﬂux
frequency, we set ω(ac) /2π = 200 MHz, which is a typical
frequency for parametric modulation in this system.
Next, we assume that the measured ac-ﬂux crosstalk
is small, which allows us to linearize the region around
(ac)
(ac)
(ac)
the bias point, i.e., i ≈ γi (δω). The slope γi
is extracted using the nearest data points and it allows
(ac)
(ac)
us to infer i from the measured (δω): βi,j =
γi

|Δθ| (rad)

An ac-ﬂux signal on a source line zj , at frequency ωj

PRX QUANTUM 5, 030350 (2024)

APPENDIX E: BASIC QPU PARAMETERS
In Table I, we list the range of measured or inferred qubit
frequencies (f01 ), anharmonicities (η), readout-resonator
frequencies (fr ), coupler frequencies at zero ﬂux bias
(fc0 ), and single-qubit coherences (T1 and T2∗ ). The frequencies of the qubits and couplers are approximately 1
GHz lower than the design values due to an oﬀ-target
Josephson-junction fabrication result.
APPENDIX F: COMPLETE DATA SETS
In Fig. 11, we show the complete data sets of measured
xy and dc-ﬂux crosstalk from both processors. Due to the
diﬀerent numbers of pairs present in each data set, we plot

030350-13

## PDF page 14

SANDOKO KOSEN et al.

PRX QUANTUM 5, 030350 (2024)
4.84
7.10

4.27
6.66

4.71
6.95

4.17
6.64

4.76
6.96

4.01
6.52

4.95
7.11

4.17
6.80

4.84
6.94
4.00
6.52
4.71
6.80

4.27
6.66
4.95
7.11
4.10
6.50

4.71
6.81
4.17
6.80
4.84
7.10

4.10
6.50
4.76
6.96
4.27
6.66

(a)

4.84
7.10

Group A (η : –188 MHz)

f01
fr

Group B (η: –229 MHz)

0.10

0.05

0.00

15

bare
(+tunnel)

10
0.1
5
Group 2
0

–50

–40

0.00

–30

4.00
6.65

0.25

0.50

β (dc) (%)

Λ(xy) (dB)

FIG. 11. The complete data sets on the aggregate performance
of xy crosstalk (xy) and dc-ﬂux crosstalk β (dc) . (a) The histogram of the on-resonant xy crosstalk i,j for a ﬂip-chip module
with bare transmission lines (labeled “bare”, 210 pairs, ¯
bare =
(39.8 ± 4.0) dB), and another ﬂip-chip module with the majority of the transmission lines covered in tunnel structures (labeled
¯ (+tunnel) = (37.4 ± 3.9) dB). (b) The his“+tunnel”, 72 pairs, 
togram of the dc-ﬂux crosstalk β (dc) (bare: 462 pairs, tunnel: 274
pairs). The data indicated as group 2 are associated with pairs the
z lines of which are nearest neighbor.

4.71
6.95

Legend
f01
fr

(b)
bare
(+tunnel)

Normalized Count

4.10
6.50

Normalized Count

4.70
6.81

FIG. 10. The target qubit frequencies (f01 , upper values) and
readout-resonator frequencies (fr , lower values). The alternating
background color illustrates the two-frequency subgroup strategy
with two distinct anharmonicity values (η).

a normalized histogram indicated by the normalized count
on the vertical axis.

in this model) and the closest distance between a source
xy line with a victim qubit (which is 500 µm, in contrast
to 375 µm in this model). The tunnel structure is modeled
as a metal enclosure with a sinusoidal roof proﬁle (3 µm
height, 50 µm width) and no opening along both sides of
the structure, which is diﬀerent from the actual structure,
where there are periodically spaced openings along the tunnel to allow access to the cleaning solvent [see Fig. 2(d)].

APPENDIX G: EXPECTED EFFECT OF THE
TUNNEL

(a)

1.5 mm

xy3

In this appendix, we are interested in the expected reduction of the coupling between a source xy line and a victim
qubit due to the tunnel structure. To do so, we have simulated the coupling-capacitance values between two xy lines
on the C-chip with two qubits on the Q-chip. In Fig. 12(a),
we show a simpliﬁed version of the simulation model. The
major diﬀerences with the actual processor layout are the
qubit-qubit distance (which is 2 mm, in contrast to 1.5 mm

xy4

q1

q2
tunnel

0.375 mm

0.375 mm

(b) Simulated coupling capacitance (× 10–6 fF)
TABLE I. The range of the measured parameters of the two
QPUs examined in this work. QPU 1 has the tunnels; QPU 2
does not have any tunnels.
Parameters

QPU 1

QPU 2

f01 (GHz)
η (MHz)
fr (GHz)
fc0 (GHz)
T1 (µs)
T2∗ (µs)

[3.262, 4.077]
[−249, −191]
[6.317, 6.987]
[6.476, 7.049]
[76, 143]
[19, 83]

[3.166, 3.982]
[−245, −193]
[6.335, 7.059]
[6.470, 7.329]
[30, 80]
[16, 42]

xy3
xy4

With tunnel
q1
q2
530
18
61
2

Without tunnel
q1
q2
xy3
530
18
xy4
403
14

FIG. 12. Simulation of the eﬀect of the tunnel structure in
reducing the direct xy-qubit coupling capacitance. (a) A simpliﬁed model of the simulation: two qubit structures (q1 and q2 ) on
the Q-chip and two xy lines (xy3 and xy4 ) on the C-chip. The
ground planes on both the C-chip and the Q-chip and the coupler structure on the Q-chip are not shown. (b) The extracted
coupling-capacitance values between two models: one with a
tunnel structure on xy4 and the other without a tunnel structure.

030350-14

## PDF page 15

SIGNAL CROSSTALK IN A FLIP-CHIP QUANTUM PROCESSOR

In this appendix, we are interested in the expected
crosstalk level due to the direct capacitive interaction
between a victim qubit with any other source xy line
(excluding its own xy line). The model includes both the
full-sized C-chip and the Q-chip, without the wire bonds
and the PCB packaging around it. To simplify the model,
we retain the 25 transmon objects on the Q-chip and
replace the coupler structures with a ground plane. On the
C-chip, we only retain the 15 xy lines controlling the three
bottom rows of the qubits (q11 to q25 ). The rest of the xy
lines and z lines are replaced with a ground plane. The
model retains the full bump structures connecting the two
chips. No tunnels are included in the model.
We have employed ANSYS MAXWELL [36] to simulate
the capacitance matrix of such a problem. The relation
between the capacitance values and the Rabi frequency
(R ) is obtained via the relation
∫ Tπ

κ = Ztml

C2κ ωq2
Cq

,

(H3)

where Ztml is the xy-line characteristic impedance (50 
in our case), Cκ is the coupling capacitance between the
xy line and the qubit, ωq is the qubit angular frequency,
and Cq is the qubit capacitance. This treatment closely
follows the derivation described in Ref. [60] (speciﬁcally,
Secs. VIII.A, IV.F, and IV.B, and Appendix C in Ref. [60]).
Reexpressing the xy-crosstalk deﬁnition in terms of the
simulated capacitance values, we obtain
(
)
i,j 2
(xy)
dir := i,j = 10 × log10
(H4)
j ,j
√ )
(
ωi Ci,j Cj
,
(H5)
= 20 × log10
ωj Cj ,j Ci
where Ci,j is the coupling capacitance between the victim qubit i and the source xy line j and {Ci , Cj } are the
capacitances of qubits i and j .
In Fig. 13(a), we show a histogram of the predicted
(xy)
crosstalk dir due to direct xy-qubit capacitive interaction. The average value is −95 dB, with the worst at −49
dB, which are much lower values than those measured
in our processor. This simulation shows that the direct
capacitive interaction between a victim qubit and any other
source xy line cannot be the major contributor to the xycrosstalk level measured in our processors, at least within
the simpliﬁed model used here.
(a)

(b)
Simulated Λ(xy)
dir (dB)

APPENDIX H: CROSSTALK DUE TO DIRECT
xy-QUBIT CAPACITIVE INTERACTION

integration (b = 1 for a square pulse, b = 2/π for a
sinusoidal-shape pulse), A0 is the pulse amplitude, and Tπ
is the characteristic pulse duration to create a π pulse. The
expression for κ is

30

Count

However, these diﬀerences should not, in principle, matter
for the purpose of this simulation.
We have used ANSYS MAXWELL [36] to obtain the
capacitance matrix. The table in Fig. 12(b) shows the
coupling-capacitance values in two situations: with and
without the tunnel structure on xy4 . First, the coupling
capacitance is smaller for larger separation: compare
C(xy3 , q1 ) and C(xy3 , q2 ) in both cases. As a reference, the
coupling capacitance between a qubit and its own xy line,
e.g., C(xy1 , q1 ), is at least 100 times larger than C(xy3 , q1 ).
Second, by comparing the coupling-capacitance values
between xy4 and either q1 or q2 before and after adding the
tunnel structure, we can see that it does indeed weaken the
direct coupling between the xy line and the qubits. Note
that C(xy4 , q2 ) < C(xy3 , q1 ), despite both of them being
identical in length and equally spaced from the respective qubits; this is because the CPW geometry of xy4 is
slightly narrower to retain 50- characteristic impedance
after adding the tunnel.
Therefore, we have shown that the tunnel structure can
indeed reduce the direct capacitive coupling between an
xy line located on the C-chip and a qubit located on the
Q-chip, at least for the simpliﬁed model discussed in this
appendix. Given that the tunnel structure modiﬁes the
radiation proﬁle of the xy line, it is possible that other xycrosstalk mechanisms may be impacted as well and future
work should investigate this in more detail.

PRX QUANTUM 5, 030350 (2024)

20
10
0
–150

–100

–50

Simulated Λ(xy)
dir (dB)

–50

d (xy)

–100

–150

m = –8.8 dB/mm, Λ0 = –57 dB

2.5

5.0

(xy)

R (t)dt = π ,

(H1)

√
2 κbA0 Tπ = π ,

(H2)

0

where κ is the photon loss rate via the xy line, b is
the pulse-shape-dependent constant obtained from the

7.5

d(xy) (mm)

FIG. 13. Simulation of the xy crosstalk dir between victim
qubits and other source xy lines due to direct xy-qubit interac(xy)
tion. (a) The histogram of dir with an average and standard
(xy)
deviation of (−96 ± 26) dB. (b) dir versus d(xy) , which is the
distance between the victim qubits and the target qubits of the
source xy lines. The parameters m and 0 are from the linear ﬁt
(xy)
to the average of dir versus d(xy) .

030350-15

## PDF page 16

SANDOKO KOSEN et al.

PRX QUANTUM 5, 030350 (2024)

We have plotted the distance-dependent xy crosstalk
(due to the direct xy-qubit interaction) in Fig. 13(b), similarly to Fig. 4. The data exhibit a relatively large spread
(xy)
of dir versus di,j (the distance between the victim qubit
i and the target qubit of the source xy line j ). We have
performed an empirical linear ﬁt of the average crosstalk
(xy)
¯
dir versus di,j and obtained the distance-scaling parameters mxy = −8.8 dB/mm and 0 = −57 dB, well below
the values needed to bring the total single-qubit gate
error below the 0.1% threshold for 100-qubit processors
(mxy = −2.0 dB/mm and 0 = −50 dB; see Sec. IV and
Appendix K).
As discussed previously, the model used in this simulation does not include the wire bonds and the PCB signal
traces. While they are positioned further away from the
qubits, they are also much larger than the rest of the signal lines in the processor. Including them in the model
is computationally expensive and future investigations
should look into the strength of the interaction between the
combined wire bonds and the PCB system with the qubits.

(a)

(b)

(c)

PCB wire bond C-chip

Q-chip

gnd
V out (j = i + 1)

gnd
Vin (i )
gnd

600 µm
V out (j = i)

via
xA
reference plane
j=i±1

A

xB

B

xC

j=i±2

C

xD

j=i±3

D
j=i±4

Ref - A –55.8 ± 1.5 –69.8 ± 1.4 –80.7 ± 1.4 –90.4 ± 1.4
Ref - B –40.2 ± 1.3 –49.0 ± 1.3 –54.5 ± 1.2 –58.3 ± 1.2
Ref - C –40.0 ± 1.3 –49.6 ± 1.2 –55.9 ± 1.1 –60.0 ± 1.2
Ref - D –38.9 ± 1.3 –48.2 ± 1.3 –55.0 ± 1.2 –60.3 ± 1.2

(d)

APPENDIX I: CROSSTALK BETWEEN SIGNAL
LINES
In this appendix, we are interested in the expected
rf-crosstalk level between neighboring signal lines. To do
so, we have performed electromagnetic simulation of a
small-scale model shown in Fig. 14(a). The model includes
a representative section of the PCB signal traces, wire
bonds, and a section of the chips. No tunnel structure is
included in this simulation.
In Fig. 14(c), we show a simpliﬁed version of the model.
We model ﬁve neighboring signal lines with input ports
located at the PCB side (labeled “reference plane” or “ref”)
and consider signal output ports at various locations. The
latter is to illustrate the relative contribution from various parts of the signal lines. The quoted crosstalk levels
S(j , i) = Vout (j )/Vin (i), expressed in decibels, are the average between the highest and lowest values obtained for the
considered pairs and the uncertainty is half of that range.
The various locations correspond to the boundary between
the PCB and the C-chip (location A, no wire bonds and
chips in the model), after the launch pad (location B, with
wire bonds and C-chip, no Q-chip in the model), just before
the Q-chip (location C, but no Q-chip is included in the
model), and within the ﬂip-chip environment (location D).
The simulations have employed ANSYS HFSS [36] (driven
modal, maximum S : 0.005, 4 GHz frequency, and the
outer boundary of the model set by default to the Perfect
E boundary condition). Due to the limited computational
resources, we have only included a certain section of the
PCB (xA = 5.0 mm) and the Q-chip (xD = 2.0). When simulating the results for intermediate locations, e.g., location
A, we have removed the rest of the signals lines (from B all
the way to D) from the model.

600 µm

100 µm

Vin (i)

Vout (j = i)
Vout (j = i –2)

xA
reference plane
j=i±1

A

xC + xB

j=i±2

xD
j=i±3

D
j=i±4

Ref - D –38.4 ± 1.3 –47.3 ± 1.1 –53.5 ± 0.9 –58.0 ± 0.8

FIG. 14. Simulation of the crosstalk between signal lines. (a)
The actual simulation model, showing a part of the PCB (with its
vias), the wire bonds, and the C-chip with its signal lines. The Qchip is not shown but is included in the model when required.
Five signal lines are included in the simulation. (b) A photograph of the actual packaging and the chips (the wire bonds are
not shown). (c) A simpliﬁed model of (a) showing an input port
[Vin (i)] and two output ports [Vin (j )] (drawing not to scale). The
table summarizes the simulated S parameter S(j , i) (in decibels)
between the input port i at the reference plane and the output port
j at one of the locations (A, B, C, and D). The model assumes
xA = 5.0 mm, xB = 500 µm, xC = 650 µm, and xD = 2 mm. (d)
A model that is similar to (c) but with the signal lines within the
ﬂip-chip environment spaced by 100 µm to replicate the actual
separation between lines in our processors. Here, xA = 5.0 mm,
xB = 500 µm, xC = 650 µm, and xD = 5 mm (drawing is not to
scale).

First of all, we see that up to the edge of the PCB [location A, row “Ref-A” in Fig. 14(c)], nearest-neighbor line
crosstalk (j = i ± 1) is at the level of −56 dB, with rapidly

030350-16

## PDF page 17

SIGNAL CROSSTALK IN A FLIP-CHIP QUANTUM PROCESSOR

criteria used are adequate to yield results that are representative of the actual processor. In the future, it will be useful
to test the accuracy of such simulations on smaller-scale
devices before employing them to predict the performance
of much larger devices. It will be also interesting to look
for alternative modeling techniques that can yield suﬃciently reliable results with a much lower computational
cost.
¯ (xy)
APPENDIX J: EMPIRICAL LINEAR FIT OF 
(xy)
VERSUS d
To further illustrate the trend within the data of average xy crosstalk ¯
(xy) versus the qubit-qubit distance d(xy) ,
we have performed an empirical linear ﬁt of the form
¯
(xy) = mxy d(xy) + 0 . The ﬁt is performed by assigning
equal weight to each data point. The results are shown in
Fig. 15. The associated error bars of mxy and 0 are the
ﬁt uncertainties. The analyses yield approximately similar
mxy and 0 for both processors.
APPENDIX K: SINGLE-QUBIT GATE ERROR
We have introduced the distance-scaling parameters,
denoted as mxy and 0 , which are obtained from an empiri¯ (xy) versus d(xy) . These parameters
cal linear ﬁt to the data 
can be used as a starting point in estimating the impact
of xy crosstalk on the total gate ﬁdelity during parallel
applications of single-qubit gates. From the hardwarearchitecture perspective, these parameters should be as low
as possible. We ﬁnd approximately mxy = −1.1 dB/mm
and 0 = −33.9 dB.
Clearly, the actual error depends on the pulse sequences
(implementing quantum gates) that are being applied to
all of the qubits. Here, we consider a speciﬁc scenario to
obtain a concrete estimate of the eﬀect on gate ﬁdelity: a
situation in which single-qubit X gates are simultaneously
applied on all qubits. The qubit frequencies are allocated
–25

d (xy)

–30

Λ(xy) (dB)

decreasing crosstalk down to the level of −90 dB for thirdnext-nearest-neighbor lines (j = i ± 4). However, after
including the wire bonds and the launch-pad area (row
“Ref-B”), the crosstalk level worsens substantially, to the
level of −40 dB for nearest neighbors and −58 dB for
third-next-nearest neighbors. The subsequent addition of
signal lines at the chip level (“Ref-C”, “Ref-D”) does not
substantially worsen the crosstalk, even though we have
only simulated a 2-mm portion of the signal lines within
the ﬂip-chip environment. The relatively small change in
the crosstalk level for the transmission lines within the
chip can be explained by the much narrower transmission
lines used at the chip area (approximately 10 µm excluding the launch-pad structure) compared to the line-to-line
separation, which is 600 µm.
In Fig. 14(d), we have modiﬁed the model for the neighboring signal lines within the ﬂip-chip environment to be
spaced by 100 µm, corresponding to the actual separation
in our processor layout. To account for the additional space
required to bend the signal lines and bring them closer to
each other, we have extended xD to 5 mm. We also note
that xD is close to half the width of the Q-chip (12 µm).
The simulation results show a crosstalk level that is not
substantially worse than those obtained in Fig. 14(c).
In our processor design, there is no pair of qubits controlled by xy lines that are nearest neighbors, as we always
need at least a signal line for ﬂux control of the tunable
coupler in between two qubits. For any pair of nearestneighbor qubits, they are controlled by xy lines that are at
least next-nearest neighbors. Typically, the corresponding
qubits are located along the same row. In the index notation introduced in Fig. 14, they correspond to pairs of i, j
with j = i ± 2. For next-nearest qubits, they are controlled
by xy lines that are at least in third-next-nearest neighbor
conﬁguration, i.e., j = i ± 4.
The average xy-crosstalk level measured for pairs
of qubits that are controlled by next-nearest neighbor
and third-next-nearest-neighbor xy lines are −36.2 dB
−38.5 dB, respectively. Simulation results from Fig. 14(d)
(−47 dB for next-nearest, −58 dB for third-nearest) suggest that the crosstalk between signal lines is not the
dominant source of crosstalk, at least within the simpliﬁed
model considered here.
The accuracy of this result is limited by the model, in
which we consider only ﬁve signal lines on a small section
of the combined PCB and QPU system. In addition, the
actual layout of neighboring signal lines is not quite as simple as illustrated in Figs. 14(c) and 14(d). However, these
simpliﬁed models are already very challenging to simulate,
given the available computational resources and the large
range of physical sizes that need to be taken into account
(from a few tens of micrometers up to a few tens of millimeters). It is possible that the overall crosstalk level may
change when we consider an area that is larger than the
one considered here. It is also unclear if the convergence

PRX QUANTUM 5, 030350 (2024)

–35
–40
–45
bare: mxy = (1.1 ± 0.2) dB/mm, Λ0 = (34.9 ± 0.9) dB
+tunnel: mxy = (1.2 ± 0.1) dB/mm, Λ0 = (32.3 ± 0.7) dB

–50

2

3

4

5

6

7

8

9

d (xy) (mm)
FIG. 15. The data of the xy crosstalk (xy) versus the qubitqubit distance d(xy) with an empirical log-linear ﬁt (i.e., empirical
here means that the ﬁt expression is not based on a physical
model or numerical simulation of (xy) ).

030350-17

## PDF page 18

SANDOKO KOSEN et al.

PRX QUANTUM 5, 030350 (2024)
small qubit arrays due to the small d(xy) . The diﬀerence
is more pronounced for larger qubit arrays, as there are
more contributions from victim-source pairs with larger
d(xy) . In such a setting, the total gate ﬁdelities for processors beyond 1000 qubits (33 × 33) increase to 99.95%
for mxy = −1.5 dB/mm, 0 = −45 dB and 99.99% for
mxy = −2.0 dB/mm, 0 = −50 dB.
We emphasize that this is a very simpliﬁed model; we
have no quantitative model predicting a log-linear behavior, nor one predicting that a similar trend would continue
beyond the range of dxy examined in this work. However,
we believe that these parameters can be useful as a set
of quantitative metrics to help guide near-term scaling-up
eﬀort and to guide hardware road maps.

10–1

1–F1Q

10–2

10–3

10–4
mxy: –1.1 dB/mm, Λ0: –33.9 dB
mxy: –1.5 dB/mm, Λ0: –45 dB
mxy: –2.0 dB/mm, Λ0: –50 dB
>1000Q

3
x
5 3
x
7 5
x
9 7
11 x 9
13 x 1
x 1
13
17
x
17
21
x
21

>100Q

31
33 x 3
x 1
35 33
x
35

10

–5

NxN
FIG. 16. The predicted total single-qubit gate error in a square
lattice of N × N qubits (the nearest-neighbor separation is
2 mm). The gate error is assumed to only come from the oﬀresonant excitation due to adversary single-qubit signals applied
on other xy lines. The solid line represents a scenario described
in the text and the dashed line assumes additional phase related
to propagation from the location of the source line to the victim
qubit.

according to the two-frequency subgroup strategy shown
in Fig. 2(f) and speciﬁed in Appendix D. Here, the gate
error is due to parasitic excitation (both oﬀ-resonant and
on-resonant) of the victim qubit from adversary X gates
applied to all other source xy lines. These signals are
assumed to be on resonant with the qubits that they are
meant to excite. The details of the simulation are described
in Appendix L.
The results are shown in Fig. 16. The simulation yielding the solid lines assumes no additional phase oﬀset
between the signal and the adversary signals. In this case,
the total gate error begins to plateau (up to the considered processor sizes) as we begin to consider processors
with hundreds of qubits, which is attributed to weakening
crosstalk due to larger values of d(xy) . This assumption of
no phase oﬀset is not a realistic one but we believe that it
provides an easily understandable setting and a relatively
stringent criterion to give us an idea of the total gate error.
If we could improve the crosstalk and its scaling behavior
to mxy = −1.5 dB/mm and 0 = −45 dB, for processors
with roughly 1000 qubits, we would ﬁnd a projected total
single-qubit gate ﬁdelity in excess of 99.7%, and for even
better crosstalk, mxy = −2.0 dB/mm and 0 = −50 dB,
we would ﬁnd 99.97%.
We have also simulated the total single-qubit gate error
(dashed lines in Fig. 16) by assuming additional phase
oﬀset due to signal propagation between the positions
of the source xy line (approximated as the position of
the target qubit of the source xy line) and the victim
qubit. The assumption makes a negligible diﬀerence for

APPENDIX L: NUMERICAL SIMULATIONS
In this appendix, we brieﬂy describe the models used to
numerically simulate the ac-ﬂux calibration curve and the
total single-qubit gate error due to xy crosstalk.
1. The ac-flux calibration curve
In this simulation, we focus on a system comprising a
ﬁxed-frequency qubit coupled to a frequency-tunable coupler. The goal is to extract the Ramsey-fringe frequency
of a qubit when the coupler is being subjected to speciﬁc
dc-ﬂux bias and ac-ﬂux modulation.
The system Hamiltonian Hsys is

Hsys = Hq + Hc + Hint ,

(L1)

where Hq , Hc , and Hint represent the Hamiltonian of the
qubit, the coupler, and their interaction, respectively. We
employ a doubly rotating frame at the qubit-drive angular
frequency ω(xy) and the coupler angular frequency at its
dc-ﬂux bias, ωc ( = (dc) ).
The qubit Hamiltonian is as follows:

Hq /ℏ = −q (σz ⊗ I) + (xy) (t)(σx ⊗ I),

(L2)

where ωq is the qubit angular frequency, q = ω(xy) − ωq ,
(xy) (t) is the time-dependent qubit-drive signal appropriately expressed in the angular-frequency unit, and σx/z are
the Pauli matrices.
The coupler Hamiltonian is

Hc /ℏ = −c (t)(I ⊗ σz ),

(L3)

(dc)
(dc)
(ac)
where
c (t)
and
√ = ωc ( ) − ωc ( +  (t))
ωc () = ωc0 | cos (π /0 )|. The parameters ωc0 and
0 are the coupler angular frequency at zero-ﬂux bias and
the magnetic ﬂux quantum, respectively.

030350-18

## PDF page 19

SIGNAL CROSSTALK IN A FLIP-CHIP QUANTUM PROCESSOR
The interaction Hamiltonian is

Hint /ℏ = gei(ω

(xy) −ω ((dc) ))t
c

(σ + ⊗σ − ) + H.c.,

(L4)

where g is the coupler-qubit coupling strength expressed
in the angular-frequency unit. Here, we make use of
the rotating-wave approximation to neglect the counterrotating terms.
We simulate the state of the combined system (both
the qubit and the coupler are initially in the ground state)
evolving under Hsys with the pulse sequence shown in
Fig. 9(a). The solver is QUTIP.SESOLVE [58,59] and the simulation time step is 1 ns. From the expectation value of
σz ⊗ I at the end of the pulse sequence, we reconstruct the
expected Ramsey fringes. An example of the simulation
result is shown in Fig. 9(c).
2. Single-qubit error
In this simulation, we consider a system comprising a
square array of qubits (total N × N qubits), each of them
being driven by an on-resonant X gate. Due to nonzero
xy crosstalk, each qubit also experiences parasitic qubit
driving from the rest of the qubits.
We assume distance-dependent xy-crosstalk behavior
that follows the empirical linear model described in
Appendix J. We focus on a victim qubit at the center of
this array (we assume that N is an odd number). Our goal
is to calculate the resultant single-qubit error on this victim
qubit due to the parasitic drives.
The Hamiltonian of interest considers a single qubit that
is being driven by microwave signals. We ignore the evolution of other qubits and group the parasitic drives into the
drive term; speciﬁcally,

Hsys = Hi + Hi,j .

(L5)

We employ a reference frame rotating with the drive
frequency of the victim qubit.
The Hamiltonian Hi is

Hi /ℏ = −i σz + i,i (t)σx ,

(L6)

(xy)

where i = ωi − ωi is the qubit-drive detuning,
assumed to be zero in this simulation. The parameter i,i (t)
is the time-dependent microwave-drive-pulse amplitude
applied to the victim qubit by its own xy line and is
appropriately expressed in the angular-frequency unit. The
symbols σx/y/z are the Pauli matrices.
The Hamiltonian corresponding to the parasitic drives
from other qubits is
∑
Hi,j /ℏ =
i,j (t)(σx cos (φj (t)) + σy sin (φj (t)), (L7)
j ̸=i

where φj (t) = δi,j t + φi,j . The parameters δi,j and φi,j are
the detuning (ωj − ωi ) and the additional phase, respectively. For simplicity, each qubit drive is assumed to

PRX QUANTUM 5, 030350 (2024)

produce the same Rabi angular frequency to its own
qubit. Thus i,i (t) = (xy) (t) for any i. The parasitic Rabi
amplitude i,j is
i,j (t) = 10i,j /20 (xy) (t),

(L8)

where i,j = mxy di,j + 0 and di,j is the distance between
qi and qj . The phase φi,j is the phase related to crosstalk
between the source xy line xyj and the victim qubit qi .
In Fig. 16, we have simulated two speciﬁc cases: φi,j = 0
(solid line), and φi,j = (ωj /c)di,j (dashed line) corresponding to the phase delay due to signal propagation from the
location of the target qubit of the source xy line to the
location of the victim qubit, through vacuum.
We employ the QUTIP.SESOLVE solver [58,59], with a
simulation time step of 0.125 ns. From the expectation
value of σz , we extract the probability Pg of the qubit being
in the ground state at the end of the pulse sequence. We
repeat this simulation for a victim qubit with the eight
diﬀerent frequencies in Appendix D, and we average the
probabilities. This is the single-qubit gate error (1 − F1Q )
that is plotted on the vertical axis of Fig. 16.

[1] Google Quantum AI, Exponential suppression of bit or
phase errors with cyclic error correction, Nature 595, 383
(2021).
[2] Y. Kim, A. Eddins, S. Anand, K. X. Wei, E. Van Den
Berg, S. Rosenblatt, H. Nayfeh, Y. Wu, M. Zaletel, K.
Temme, and A. Kandala, Evidence for the utility of quantum computing before fault tolerance, Nature 618, 500
(2023).
[3] C. Ryan-Anderson, J. G. Bohnet, K. Lee, D. Gresh, A.
Hankin, J. P. Gaebler, D. Francois, A. Chernoguzov, D.
Lucchetti, N. C. Brown, T. M. Gatterman, S. K. Halit, K.
Gilmore, J. A. Gerber, B. Neyenhuis, D. Hayes, and R. P.
Stutz, Realization of real-time fault-tolerant quantum error
correction, Phys. Rev. X 11, 041058 (2021).
[4] D. Bluvstein, et al., Logical quantum processor based on
reconﬁgurable atom arrays, Nature 626, 58 (2023).
[5] X. Dai, D. M. Tennant, R. Trappen, A. J. Martinez, D.
Melanson, M. A. Yurtalan, Y. Tang, S. Novikov, J. A.
Grover, S. M. Disseler, J. I. Basham, R. Das, D. K. Kim,
A. J. Melville, B. M. Niedzielski, S. J. Weber, J. L. Yoder,
D. A. Lidar, and A. Lupascu, Calibration of ﬂux crosstalk in
large-scale ﬂux-tunable superconducting quantum circuits,
PRX Quantum 2, 040313 (2021).
[6] Y. Sung, L. Ding, J. Braumüller, A. Vepsäläinen, B. Kannan, M. Kjaergaard, A. Greene, G. O. Samach, C. McNally,
D. Kim, A. Melville, B. M. Niedzielski, M. E. Schwartz, J.
L. Yoder, T. P. Orlando, S. Gustavsson, and W. D. Oliver,
Realization of high-ﬁdelity CZ and ZZ-free iSWAP gates
with a tunable coupler, Phys. Rev. X 11, 021058 (2021).
[7] W. Nuerbolati, Z. Han, J. Chu, Y. Zhou, X. Tan, Y. Yu, S.
Liu, and F. Yan, Canceling microwave crosstalk with ﬁxedfrequency qubits, Appl. Phys. Lett. 120, 174001 (2022).

030350-19

## PDF page 20

SANDOKO KOSEN et al.

PRX QUANTUM 5, 030350 (2024)

[8] C. N. Barrett, A. H. Karamlou, S. E. Muschinske, I. T.
Rosen, J. Braumüller, R. Das, D. K. Kim, B. M. Niedzielski, M. Schuldt, K. Serniak, M. E. Schwartz, J. L. Yoder, T.
P. Orlando, S. Gustavsson, J. A. Grover, and W. D. Oliver,
Learning-based calibration of ﬂux crosstalk in transmon
qubit arrays, Phys. Rev. Appl. 20, 024070 (2023).
[9] X. Zhang, E. Kim, D. K. Mark, S. Choi, and O. Painter, A
superconducting quantum simulator based on a photonicbandgap metamaterial, Science 379, 278 (2023).
[10] X. Dai, R. Trappen, R. Yang, S. M. Disseler, J. I. Basham,
J. Gibson, A. J. Melville, B. M. Niedzielski, R. Das, D.
K. Kim, J. L. Yoder, S. J. Weber, C. F. Hirjibehedin,
D. A. Lidar, and A. Lupascu, Optimizing for periodicity:
A model-independent approach to ﬂux crosstalk calibration for superconducting circuits, Quantum Sci. Technol. 9,
025007 (2024).
[11] S. Krinner, N. Lacroix, A. Remm, A. Di Paolo, E. Genois,
C. Leroux, C. Hellings, S. Lazar, F. Swiadek, J. Herrmann,
G. J. Norris, C. K. Andersen, M. Müller, A. Blais, C.
Eichler, and A. Wallraﬀ, Realizing repeated quantum error
correction in a distance-three surface code, Nature 605, 669
(2022).
[12] P. A. Spring, S. Cao, T. Tsunoda, G. Campanaro, S. Fasciati,
J. Wills, M. Bakr, V. Chidambaram, B. Shteynas, L. Carpenter, P. Gow, J. Gates, B. Vlastakis, and P. J. Leek, High
coherence and low cross-talk in a tileable 3D integrated
superconducting circuit architecture, Sci. Adv. 8, eabl6698
(2022).
[13] Y. Wang, S. Crain, C. Fang, B. Zhang, S. Huang, Q. Liang,
P. H. Leung, K. R. Brown, and J. Kim, High-ﬁdelity twoqubit gates using a microelectromechanical-system-based
beam steering system for individual qubit addressing, Phys.
Rev. Lett. 125, 150505 (2020).
[14] T. Xia, M. Lichtman, K. Maller, A. W. Carr, M. J. Piotrowicz, L. Isenhower, and M. Saﬀman, Randomized benchmarking of single-qubit gates in a 2D array of neutral-atom
qubits, Phys. Rev. Lett. 114, 100503 (2015).
[15] W. I. L. Lawrie, M. Rimbach-Russ, F. V. Riggelen,
N. W. Hendrickx, S. L. D. Snoo, A. Sammak, G. Scappucci,
J. Helsen, and M. Veldhorst, Simultaneous single-qubit
driving of semiconductor spin qubits at the fault-tolerant
threshold, Nat. Commun. 14, 3617 (2023).
[16] J. M. Martinis, Qubit metrology for building a fault-tolerant
quantum computer, npj Quantum Inf. 1, 15005 (2015).
[17] D. Rosenberg, D. Kim, R. Das, D. Yost, S. Gustavsson, D.
Hover, P. Krantz, A. Melville, L. Racz, G. O. Samach, S. J.
Weber, F. Yan, J. L. Yoder, A. J. Kerman, and W. D. Oliver,
3D integrated superconducting qubits, npj Quantum Inf. 3,
42 (2017).
[18] B. Foxen, et al., Qubit compatible superconducting interconnects, Quantum Sci. Technol. 3, 014005 (2018).
[19] A. Gold, J. P. Paquette, A. Stockklauser, M. J. Reagor, M.
S. Alam, A. Bestwick, N. Didier, A. Nersisyan, F. Oruc,
A. Razavi, B. Scharmann, E. A. Sete, B. Sur, D. Venturelli, C. J. Winkleblack, F. Wudarski, M. Harburn, and
C. Rigetti, Entanglement across separate silicon dies in a
modular superconducting qubit device, npj Quantum Inf. 7,
142 (2021).
[20] S. Kosen, et al., Building blocks of a ﬂip-chip integrated
superconducting quantum processor, Quantum Sci. Technol. 7, 035018 (2022).

[21] J. Koch, T. M. Yu, J. Gambetta, A. A. Houck, D. I. Schuster, J. Majer, A. Blais, M. H. Devoret, S. M. Girvin, and
R. J. Schoelkopf, Charge-insensitive qubit design derived
from the Cooper pair box, Phys. Rev. A 76, 042319
(2007).
[22] J. A. Schreier, A. A. Houck, J. Koch, D. I. Schuster, B. R.
Johnson, J. M. Chow, J. M. Gambetta, J. Majer, L. Frunzio, M. H. Devoret, S. M. Girvin, and R. J. Schoelkopf,
Suppressing charge noise decoherence in superconducting
charge qubits, Phys. Rev. B 77, 180502(R) (2008).
[23] R. Barends, J. Kelly, A. Megrant, D. Sank, E. Jeﬀrey, Y.
Chen, Y. Yin, B. Chiaro, J. Mutus, C. Neill, P. O’Malley,
P. Roushan, J. Wenner, T. C. White, A. N. Cleland, and J.
M. Martinis, Coherent Josephson qubit suitable for scalable
quantum integrated circuits, Phys. Rev. Lett. 111, 080502
(2013).
[24] D. C. McKay, S. Filipp, A. Mezzacapo, E. Magesan, J.
M. Chow, and J. M. Gambetta, Universal gate for ﬁxedfrequency qubits via a tunable bus, Phys. Rev. Appl. 6,
064007 (2016).
[25] Z. Chen, A. Megrant, J. Kelly, R. Barends, J. Bochmann, Y.
Chen, B. Chiaro, A. Dunsworth, E. Jeﬀrey, J. Y. Mutus, P. J.
J. O’Malley, C. Neill, P. Roushan, D. Sank, A. Vainsencher,
J. Wenner, T. C. White, A. N. Cleland, and J. M. Martinis,
Fabrication and characterization of aluminum airbridges for
superconducting microwave circuits, Appl. Phys. Lett. 104,
052602 (2014).
[26] A. Dunsworth, et al., A method for building low loss multilayer wiring for superconducting microwave devices, Appl.
Phys. Lett. 112, 063502 (2018).
[27] B. M. Niedzielski, J. L. Yoder, D. Ruth-Yost, W. D. Oliver,
D. K. Kim, M. E. Schwartz, D. Rosenberg, G. Calusine, R.
Das, A. J. Melville, J. Plant, and L. Racz, in IEEE International Electron Devices Meeting (IEDM) (IEEE, San
Francisco, CA, USA, 2019).
[28] G. J. Norris, L. Michaud, D. Pahl, M. Kerschbaum, C.
Eichler, J.-C. Besse, and A. Wallraﬀ, Improved parameter
targeting in 3D-integrated superconducting circuits through
a polymer spacer process, EPJ Quantum Technol. 11, 5
(2024).
[29] M. Vahidpour, W. O’Brien, J. T. Whyland, J. Angeles, J.
Marshall, D. Scarabelli, G. Crossman, K. Yadav, Y. Mohan,
C. Bui, V. Rawat, R. Renzas, N. Vodrahalli, A. Bestwick,
and C. Rigetti, Superconducting through-silicon vias for
quantum integrated circuits, ArXiv:1708.02226.
[30] J. L. Mallek, D.-R. W. Yost, D. Rosenberg, J. L. Yoder,
G. Calusine, M. Cook, R. Das, A. Day, E. Golden, D.
K. Kim, J. Knecht, B. M. Niedzielski, M. Schwartz,
A. Sevi, C. Stull, W. Woods, A. J. Kerman, and W.
D. Oliver, Fabrication of superconducting through-silicon
vias, ArXiv:2103.08536.
[31] K. Grigoras, et al., Qubit-compatible substrates with superconducting through-silicon vias, IEEE Trans. Quantum
Eng. 3, 5100310 (2022).
[32] J. J. Burnett, A. Bengtsson, M. Scigliuzzo, D. Niepce, M.
Kudra, P. Delsing, and J. Bylander, Decoherence benchmarking of superconducting qubits, npj Quantum Inf. 5, 54
(2019).
[33] A. Osman, J. Simon, A. Bengtsson, S. Kosen, P. Krantz, D.
P. Lozano, M. Scigliuzzo, P. Delsing, J. Bylander, and A.
Fadavi Roudsari, Simpliﬁed Josephson-junction fabrication

030350-20

## PDF page 21

SIGNAL CROSSTALK IN A FLIP-CHIP QUANTUM PROCESSOR
process for reproducibly high-performance superconducting qubits, Appl. Phys. Lett. 118, 064002 (2021).
[34] A. Osman, J. Fernández-Pendás, C. Warren, S. Kosen,
M. Scigliuzzo, A. Frisk Kockum, G. Tancredi, A. Fadavi
Roudsari, and J. Bylander, Mitigation of frequency collisions in superconducting quantum processors, Phys. Rev.
Res. 5, 043001 (2023).
[35] P. A. Shah, et al., Qiskit-community/qiskit-metal: QISKIT
METAL 0.1.5a1 (2023).
[36] ANSYS Electronics Desktop, Release 21.2 (2021).
[37] Tanner L-Edit IC (2021).
[38] D. M. Abrams, N. Didier, S. A. Caldwell, B. R.
Johnson, and C. A. Ryan, Methods for measuring magnetic
ﬂux crosstalk between tunable transmons, Phys. Rev. Appl.
12, 064022 (2019).
[39] U. Warring, C. Ospelkaus, Y. Colombe, R. Jördens, D.
Leibfried, and D. J. Wineland, Individual-ion addressing with microwave ﬁeld gradients, Phys. Rev. Lett. 110,
173002 (2013).
[40] C. Piltz, T. Sriarunothai, A. Varón, and C. Wunderlich, A
trapped-ion-based quantum byte with 10−5 next-neighbour
cross-talk, Nat. Commun. 5, 4679 (2014).
[41] D. P. L. Aude Craik, N. M. Linke, M. A. Sepiol, T. P. Harty,
J. F. Goodwin, C. J. Ballance, D. N. Stacey, A. M. Steane,
D. M. Lucas, and D. T. C. Allcock, High-ﬁdelity spatial
and polarization addressing of 43 Ca+ qubits using near-ﬁeld
microwave control, Phys. Rev. A 95, 022337 (2017).
[42] I. Pogorelov, T. Feldker, Ch. D. Marciniak, L. Postler,
G. Jacob, O. Krieglsteiner, V. Podlesnic, M. Meth, V.
Negnevitsky, M. Stadler, B. Höfer, C. Wächter, K.
Lakhmanskiy, R. Blatt, P. Schindler, and T. Monz, Compact
ion-trap quantum computing demonstrator, PRX Quantum
2, 020343 (2021).
[43] C. Fang, Y. Wang, S. Huang, K. R. Brown, and J. Kim,
Crosstalk suppression in individually addressed two-qubit
gates in a trapped-ion quantum computer, Phys. Rev. Lett.
129, 240504 (2022).
[44] A. Binai-Motlagh, M. L. Day, N. Videnov, N. Greenberg, C.
Senko, and R. Islam, A guided light system for agile individual addressing of Ba+ qubits with 10−4 level intensity
crosstalk, Quantum Sci. Technol. 8, 045012 (2023).
[45] H. Levine, A. Keesling, G. Semeghini, A. Omran, T. T.
Wang, S. Ebadi, H. Bernien, M. Greiner, V. Vuletić, H.
Pichler, and M. D. Lukin, Parallel implementation of highﬁdelity multiqubit gates with neutral atoms, Phys. Rev.
Lett. 123, 170503 (2019).
[46] Y. Wang, A. Kumar, T.-Y. Wu, and D. S. Weiss, Singlequbit gates based on targeted phase shifts in a 3D neutral
atom array, Science 352, 1562 (2016).
[47] B. Undseth, X. Xue, M. Mehmandoost, M. RimbachRuss, P. T. Eendebak, N. Samkharadze, A. Sammak, V.
V. Dobrovitski, G. Scappucci, and L. M. K. Vandersypen,
Nonlinear response and crosstalk of electrically driven
silicon spin qubits, Phys. Rev. Appl. 19, 044078 (2023).
[48] C. Neill, et al., A blueprint for demonstrating quantum
supremacy with superconducting qubits, Science 360, 195
(2018).
[49] J. Braumüller, A. H. Karamlou, Y. Yanay, B. Kannan,
D. Kim, M. Kjaergaard, A. Melville, B. M. Niedzielski,

PRX QUANTUM 5, 030350 (2024)

Y. Sung, A. Vepsäläinen, R. Winik, J. L. Yoder, T. P.
Orlando, S. Gustavsson, C. Tahan, and W. D. Oliver, Probing quantum information propagation with out-of-timeordered correlators, Nat. Phys. 18, 172 (2022).
[50] A. H. Karamlou, I. T. Rosen, S. E. Muschinske, C. N.
Barrett, A. Di Paolo, L. Ding, P. M. Harrington, M. Hays, R.
Das, D. K. Kim, B. M. Niedzielski, M. Schuldt, K. Serniak,
M. E. Schwartz, J. L. Yoder, S. Gustavsson, Y. Yanay,
J. A. Grover, and W. D. Oliver, Probing entanglement
in a 2D hard-core Bose-Hubbard lattice, Nature 629, 561
(2024).
[51] V. Schmitt, Ph.D. thesis, Pierre and Marie Curie University—Paris VI (2015), https://theses.hal.science/tel-012
14394/.
[52] J. B. Hertzberg, E. J. Zhang, S. Rosenblatt, E. Magesan, J.
A. Smolin, J.-B. Yau, V. P. Adiga, M. Sandberg, M. Brink,
J. M. Chow, and J. S. Orcutt, Laser-annealing Josephson
junctions for yielding scaled-up superconducting quantum
processors, npj Quantum Inf. 7, 129 (2021).
[53] M. Roth, M. Ganzhorn, N. Moll, S. Filipp, G. Salis,
and S. Schmidt, Analysis of a parametrically driven
exchange-type gate and a two-photon excitation gate
between superconducting qubits, Phys. Rev. A 96, 062323
(2017).
[54] J. Wenner, M. Neeley, R. C. Bialczak, M. Lenander, E.
Lucero, A. D. O’Connell, D. Sank, H. Wang, M. Weides, A.
N. Cleland, and J. M. Martinis, Wirebond crosstalk and cavity modes in large chip mounts for superconducting qubits,
Supercond. Sci. Technol. 24, 065001 (2011).
[55] D. R. W. Yost, M. E. Schwartz, J. Mallek, D. Rosenberg, C.
Stull, J. L. Yoder, G. Calusine, M. Cook, R. Das, A. L. Day,
E. B. Golden, D. K. Kim, A. Melville, B. M. Niedzielski, W.
Woods, A. J. Kerman, and W. D. Oliver, Solid-state qubits
integrated with superconducting through-silicon vias, npj
Quantum Inf. 6, 59 (2020).
[56] T. M. Hazard, W. Woods, D. Rosenberg, R. Das, C. F.
Hirjibehedin, D. K. Kim, J. M. Knecht, J. Mallek, A.
Melville, B. M. Niedzielski, K. Serniak, K. M. Sliwa, D.
R. W. Yost, J. L. Yoder, W. D. Oliver, and M. E. Schwartz,
Characterization of superconducting through-silicon vias as
capacitive elements in quantum circuits, Appl. Phys. Lett.
123, 154004 (2023).
[57] L. Chayanun, J. Biznárová, L. Zeng, P. Malmberg, A.
Nylander, A. Osman, M. Rommel, P. L. Tam, E. Olsson, P.
Delsing, A. Yurgens, J. Bylander, and A. Fadavi Roudsari,
Characterization of process-related interfacial dielectric
loss in aluminum-on-silicon by resonator microwave measurements, materials analysis, and imaging, APL Quantum
1, 026115 (2024).
[58] J. Johansson, P. Nation, and F. Nori, QuTiP: An opensource PYTHON framework for the dynamics of open
quantum systems, Comput. Phys. Commun. 183, 1760
(2012).
[59] J. Johansson, P. Nation, and F. Nori, QuTiP 2: A PYTHON
framework for the dynamics of open quantum systems,
Comput. Phys. Commun. 184, 1234 (2013).
[60] A. Blais, A. L. Grimsmo, S. M. Girvin, and A. Wallraﬀ,
Circuit quantum electrodynamics, Rev. Mod. Phys. 93,
025005 (2021).

030350-21
