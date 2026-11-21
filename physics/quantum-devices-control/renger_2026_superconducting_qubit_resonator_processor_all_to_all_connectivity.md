Source: https://doi.org/10.1103/8x68-cx1w
PDF sha256: 1ec542b27e87fc1cb49500b443e867e918db1c063f2a6125831aa938a81ced1c
License: https://creativecommons.org/licenses/by/4.0/

# Transcription of renger_2026_superconducting_qubit_resonator_processor_all_to_all_connectivity.pdf

Transcription of `renger_2026_superconducting_qubit_resonator_processor_all_to_all_connectivity.pdf` in this directory, 29 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-29 from the PDF's own text layer (pdftotext version 26.10.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

Superconducting qubit-resonator quantum processor with effective all-to-all connectivity
Michael Renger ,1,*,† Jeroen Verjauw ,1,*,‡ Nicola Wurz ,1,*,§ Amin Hosseinkhani ,1 Caspar Ockeloen-Korppi ,2
Wei Liu ,2 Aniket Rath ,1 Manish J. Thapa,1 Florian Vigneau ,1 Elisabeth Wybo ,1 Ville Bergholm ,2 Chun Fai Chan,2
Bálint Csatári ,2 Saga Dahl,2 Rakhim Davletkaliyev ,2 Rakshyakar Giri ,1 Daria Gusenkova ,1 Hermanni Heimonen,2
Tuukka Hiltunen,2 Hao Hsu ,1 Eric Hyyppä ,2 Joni Ikonen ,2 Tyler Jones ,1 Shabeeb Khalid ,2 Seung-Goo Kim,2
Miikka Koistinen ,2 Anton Komlev ,2 Janne Kotilahti ,2 Vladimir Kukushkin,2 Julia Lamprich ,1 Alessandro Landra ,2
Lan-Hsuan Lee ,2 Tianyi Li ,2 Per Liebermann ,2 Sourav Majumder ,1 Janne Mäntylä ,2 Fabian Marxer ,2
Arianne Meijer - van de Griend ,2 Vladimir Milchakov ,2 Jakub Mrożek ,2 Jayshankar Nath,1 Tuure Orell ,2
Miha Papič ,1,3 Matti Partanen ,2 Alexander Plyushch ,2 Stefan Pogorzalek,1 Jussi Ritvas ,2 Pedro Figueroa Romero,1
Ville Sampo,2 Marko Seppälä,2 Ville Selinmaa ,2 Linus Sundström,2 Ivan Takmakov ,2 Brian Tarasinski ,2 Jani Tuorila ,2
Olli Tyrkkö ,2 Alpo Välimaa ,2 Jaap Wesdorp ,2 Ping Yang,1 Liuqi Yu,2 Johannes Heinsoo ,2 Antti Vepsäläinen,2
William Kindel,1 Hsiang-Sheng Ku ,1 and Frank Deppe 1,ࢱ
1

IQM Quantum Computers, Georg-Brauchle-Ring 23-25, 80992 Munich, Germany
2
IQM Quantum Computers, Keilaranta 19, 02150 Espoo, Finland
3
Department of Physics and Arnold Sommerfeld Center for Theoretical Physics, Ludwig-Maximilians-Universität München,
Theresienstrasse 37, 80333 Munich, Germany
(Received 22 April 2025; revised 29 September 2025; accepted 5 December 2025; published 11 February 2026)
In this work, we introduce a superconducting quantum processor architecture that uses a transmission-line
resonator to implement effective all-to-all connectivity between six transmon qubits. This architecture can be
used as a test bed for algorithms that benefit from high connectivity. We show that the central resonator can be
used as a computational element, which offers the flexibility to encode a qubit for quantum computation or to
utilize its bosonic modes that further enables quantum simulation of bosonic systems. To operate the quantum
processing unit (QPU), we develop and benchmark the qubit-resonator conditional Z gate and the qubit-resonator
MOVE operation. The latter allows for transferring a quantum state between one of the peripheral qubits and
the computational resonator. We benchmark the QPU performance and achieve a genuinely multiqubit entangled
Greenberger-Horne-Zeilinger state over all six qubits with a readout-error mitigated fidelity of F|ψ⟩GHZ = 0.86.
DOI: 10.1103/8x68-cx1w

I. INTRODUCTION

The design flexibility of superconducting qubits facilitates
the exploration of innovative quantum processing architectures with different topologies [1–4]. Currently, quantum
processors built from regular lattices of sparsely connected
superconducting qubits have been at the center of the effort
in scaling superconducting quantum processing units (QPUs)
by major industrial and governmental players, with example
topologies including square lattice [5–9], heavy hex [10],
and square-octagon [11]. In these topologies, each of the
qubits is connected to at most four neighboring qubits. These
QPUs are conceptually straightforward to scale, suited for

*

These authors contributed equally to this work.
Contact author: michael.renger@meetiqm.com
‡
Contact author: jeroen.verjauw@meetiqm.com
§
Contact author: nicola.wurz@meetiqm.com
ࢱ
Contact author: frank.deppe@meetiqm.com
†

Published by the American Physical Society under the terms of the
Creative Commons Attribution 4.0 International license. Further
distribution of this work must maintain attribution to the author(s)
and the published article’s title, journal citation, and DOI.
2643-1564/2026/8(1)/013148(29)

applications such as the square-lattice surface code [12,13],
and have achieved breakthroughs in science and engineering, including the simulation of a Bose-Hubbard lattice
[14] and trotterized Ising model [15], as well as lattice
surgery [16]. However, achieving quantum utility remains
elusive [17–20].
A large benefit of square-lattice QPUs is the possibility
of algorithm execution with a high level of parallelization.
On the other hand, entangling distant qubits on such a hardware platform requires the concatenation of multiple gates in
SWAP networks [21]. This leads to a gate-count overhead
in case the connectivity of the QPU in terms of native twoqubit gates is not matched to the algorithm of interest [22].
Consequently, it can be beneficial to increase the connectivity between qubits at the cost of reduced parallelism for
a given application. Examples for such applications include
quantum error correcting codes with high encoding rates [23]
and noisy intermediate scale quantum (NISQ) algorithms [2].
Particularly high connectivity is provided by a star topology
where all qubits are connected to a central element [24–26].
A promising choice for this central node is a resonator that
has a long history in circuit QED [27–29]. In particular,
the combination of superconducting qubits and resonators
has been employed to realize a quantum von Neumann architecture [30] or the resonator–zero-qubit (RezQu) scheme

013148-1

Published by the American Physical Society

## PDF page 2

MICHAEL RENGER et al.

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

[31]. In addition, QPUs consisting of qubits coupled to a bus
resonator have demonstrated genuine multipartite entangled
states for up to 20 qubits [32,33]. Furthermore, they allow for
combining conventional qubit-based quantum computing with
bosonic resonator modes that provide additional computational degrees of freedom [34–38]. Such quantum computing
modality combines the precise control of qubits with the large
Hilbert space of bosonic modes. Realizing QPUs with these
architectures requires engineering and mastering the control
of qubit-resonator interactions and developing methods for
benchmarking.
In this paper, we introduce a qubit-resonator QPU where a
computational resonator is connected to six peripheral qubits
in a star topology. A crucial limitation in previous work on
qubit-resonator QPUs relying on passive capacitive coupling
is hybridization crosstalk to the spectator qubits. One way to
suppress the resulting idling error has been demonstrated in
Ref. [31] by introducing the RezQu architecture, relying on
additional memory resonators for storing the quantum state
of the spectator qubits during idling. In this work, we follow
an alternative approach by employing frequency-tunable couplers. These active elements have been successfully employed
to mediate the coupling between individual qubit-qubit pairs
[6,39–45]. They feature a large on-off ratio in the coupling
strength, while simultaneously suppressing the hybridization
crosstalk. We implement and benchmark two qubit-resonator
operations, which combined with single-qubit gates form a
universal set of quantum operations for this QPU. The qubitresonator operations are based on the Jaynes-Cummings (JC)
interaction between a qubit (QB) and the central computational resonator (CR) [28]. For the MOVE operation [31],
we restrict the input state of the qubit-resonator pair to the
single-photon manifold and tune the qubit and the resonator
into resonance in order to fully transfer a state between them.
In addition, we implement a conditional Z (CZ) gate to create entanglement between a qubit and the resonator. The
CZ gate is implemented by tuning the e-f transition of the
qubit into resonance with the computational resonator [43].
After a full Rabi cycle, the state where both the qubit and
the computational resonator are in the first excited state has
acquired a π phase shift. By combining these qubit-resonator
operations, we can effectively implement a CZ gate between
any two qubits. We consider our system as a QPU with effective all-to-all connectivity between the qubits, because a
constant overhead of two MOVE operations is required to
realize a qubit-qubit CZ gate—independent of the physical
distance between the qubits. Depending on the algorithm,
however, it may be beneficial to treat the resonator as a
proper computational element by applying MOVE and CZ
operations individually. As an example for such an algorithm
and to provide a global benchmark for the quantum computing capability of our QPU, we entangle all qubits in a
Greenberger-Horne-Zeilinger (GHZ) state. As an outlook toward hybrid quantum computing including higher-order Fock
states, we demonstrate that the higher resonator levels can
be populated by repeatedly exciting the qubit and applying
the MOVE operation. We eventually provide a NISQ application use case for our QPU by applying error mitigation to
determine the ground-state energy of the transverse-field Ising
model.

FIG. 1. (a) Schematic illustration of the qubit-resonator QPU.
The readout resonators (one for each qubit) have been omitted for
the sake of clarity. (b) Operational frequencies of the qubits (blue
circles), the tunable couplers (green squares), the computational resonator (red line), and the dispersively coupled resonators used for
multiplexed readout (black diamonds). The qubits and couplers are
biased at their first-order flux-insensitive point and their frequencies
are tunable from this maximum attainable value down to nearly zero.

II. QUBIT-RESONATOR QPU

The QPU consists of six frequency-tunable superconducting transmon qubits [46], connected to a central computational resonator in a star topology [see Fig. 1(a)]. The central
resonator is implemented by a coplanar waveguide transmission line in the quarter-wavelength configuration. To achieve
tunable coupling with a large on-off ratio, we employ an additional frequency-tunable transmon qubit as coupling element
[43,44] between the resonator and each qubit. Analog to their
use in qubit-qubit gates, these tunable couplers (TCs) mediate
an effective qubit-resonator interaction, by creating an indirect
coupling with a tunable sign and magnitude in addition to a
small fixed qubit-resonator coupling. During gate operation,
the couplers are dynamically tuned near the qubit and computational resonator frequencies, enabling fast nonadiabatic gate
operation. On the other hand, in the idling configuration the
total ZZ coupling can be suppressed to a very small value on
the order of a few kilohertz by choosing the tunable coupler
frequency such that the coupler-mediated and direct couplings
cancel each other. The frequencies of all the QPU components
are shown in Fig. 1(b).
To maximize the coupling strengths, we connect the tunable couplers to the open-circuit end of the resonator. To
enable flexible positioning of the qubits with respect to
the computational resonator, we employ coupler extender
waveguides between the components and the coupler. This
modification to the tunable couplers ensures large qubit-qubit
separations, thereby suppressing parasitic crosstalk [44]. We
note that the star topology with a computational resonator as
the central element can be extended beyond the six peripheral qubits shown here without fundamental limitations. We
estimate that, using similar coupling values as reported here
and maintaining the millimeter-scale spacing between neighboring qubits, up to 12 qubits can be coupled to such a single
computational resonator. The qubit-resonator QPU design and
fabrication methodology are discussed in Appendix A.
The QPU further contains drive lines for XY control of the
qubits, flux bias lines to control the qubit and tunable coupler
frequencies, and readout resonators that enable multiplexed

013148-2

## PDF page 3

SUPERCONDUCTING QUBIT-RESONATOR QUANTUM …

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

dispersive readout of the qubit state. The design of the control lines and readout structures closely follows the design in
Ref. [44].
III. QUBIT-RESONATOR OPERATIONS
AND CHARACTERIZATION

We achieve effective all-to-all connectivity on the qubitresonator QPU with star topology by implementing CZ gates
between each pair of qubits. To realize a CZ gate CZ(QB 2,
QB 1) between a pair of qubits, QB 1 and QB 2, we transfer
the state from one of the qubits, i.e., QB 1 to the computational
resonator by applying MOVE(QB 1, CR). Consecutively,
we perform a CZ(QB 2, CR) gate between the CZ qubit,
QB 2, and the resonator to entangle the two components.
Then, as the last step, we apply a second MOVE operation
MOVE(QB 1, CR), which transfers the entanglement with
QB 2 from the computational resonator to the MOVE qubit,
QB 1. Hence, to create entanglement between the peripheral
qubits of the device, both native qubit-resonator operations are
required, the MOVE operation and the CZ gate.
The MOVE operation transfers a state from a qubit to the
computational resonator, or vice versa, assuming that only
one of the two components is populated beforehand. We implement this operation using the resonant Jaynes-Cummings
interaction described by the Hamiltonian
(
)
h̄
h̄ωQB
1
†
ĤJC =
σ̂z + h̄ωCR â â +
+
(âσ̂ + + â† σ̂ − ),
2
2
2
(1)
where â (â† ) is the annihilation (creation) operator
for the computational resonator mode, σ̂ + ≡ |e⟩⟨g| = (σ̂ − )†
are the raising and lowering operators for the qubit, and 
is the Rabi rate. For the MOVE operation, the qubit frequency, ωQB , is adjusted to match the computational resonator
frequency, ωCR . We experimentally realize this operation by
applying a magnetic flux pulse on the qubit superconducting
quantum interference device (SQUID) loop.
In general, the Jaynes-Cummings interaction couples a
qubit with the entire ladder of resonator number states. By
integrating the time evolution of the Jaynes-Cummings interaction given in Eq. (1) for a fixed duration, we derive the
unitary of the Jaynes-Cummings gate given by the transformation of the basis states
|g, n⟩ → cn ()|g, n⟩ − isn ()|e, n − 1⟩,
|e, n⟩ → cn+1 ()|e, n⟩ − isn+1 ()|g, n + 1⟩,
where we define

(2)

(√ )
(√ )
n
n
 , sn () ≡ sin
 . (3)
2
2
∫
Here, the angle 2 = 21 (t )dt is the exchange angle that
parametrizes the Jaynes-Cummings gate. The MOVE operation, defined for the input states |g, 1⟩, |e, 0⟩, and |g, 0⟩, is
calibrated to achieve a full population exchange of |g, 1⟩ and
|e, 0⟩, corresponding to an exchange angle of  = π . In this
case, we use the abbreviations cn ≡ cn (π ) and sn ≡ sn (π ).
For conventional quantum computing applications, we restrict the resonator such that it is never occupied beyond the
cn () ≡ cos

first excited state, and thus it can be effectively mapped onto
the state space of a qubit. Specifically, we carefully design
the gate sequences so that the MOVE operation is never applied to a qubit-resonator state with an |e, 1⟩ contribution. As
can be seen from the description of the Jaynes-Cummings
gate in Eq. (2), the system evolves into the state c2 |e, 1⟩ −
is2 |g, 2⟩ if the MOVE operation is applied to |e, 1⟩, thereby
breaking the qubit mapping of the resonator by occupying
its |2⟩ state.
By avoiding the |e, 1⟩ state when applying the MOVE
operation, we can operate within the single-photon manifold,
where we can conceptually treat the resonator as a qubit. By
subsequently removing the restrictions on the resonator, we
can access higher resonator modes.

A. QPU characterization

To perform quantum operations on the qubit-resonator
QPU, we employ six microwave drive lines for XY control
of the qubits and twelve flux lines to enable frequency tuning of the qubits and the tunable couplers with Z pulses.
Details of the experimental setup can be found in Appendix B.
We determine the qubit frequencies from a variable delay
Ramsey experiment and extract the qubit and coupler flux
dispersion by sweeping the applied dc bias. We implement
single-qubit gates using the derivative removal by adiabatic
gate method with a cosine shaped envelope of the in-phase
component [47]. We employ error amplification techniques
to reach an average individual single-qubit gate fidelity of
99.94 ± 0.09% [48]. We characterize the coherence times of
all qubits in their first-order flux-insensitive configuration.
We calculate the average energy relaxation time T1 = 41.3 ±
1.3 µs, i.e., the arithmetic mean over all qubits. Using a Ramsey sequence, we find an average dephasing time of T2∗ =
33.0 ± 1.2 µs. To remove the effect of quasistatic noise, we
perform a Hahn echo experiment and obtain an average echo
dephasing time of T2e = 45.8 ± 1.2 µs. We find an exponential
decay envelope, implying white noise as dominating source of
decoherence [49,50].
Since the computational resonator state cannot be directly
prepared and read out, we measure its coherence properties
indirectly by transferring a state between one of the qubits
and the resonator using the MOVE operation. For the resonator relaxation time, we obtain T1 = 5.53 ± 0.32 µs. Via a
Ramsey sequence, we measure a resonator dephasing time of
T2∗ = 10.9 ± 1.0 µs close to 2T1 , implying that the resonator
coherence is limited by energy relaxation. We furthermore
extract the computational resonator frequency at the idling
configuration, ωCR = 4.218 GHz. The resonator relaxation is
one of the limiting factors of the presented QPU performance.
Ongoing efforts to reduce the Purcell decay and the energy
participation ratio [51], in addition to employing flip-chip
architecture, are expected to yield significant improvements
in the T1 time of the computational resonator. Details about
the measurement techniques for the resonator characterization
as well as a more detailed discussion about the main factors
impacting the relaxation time and possible future advancements are presented in Appendix D 3. A summary of the QPU
parameters can be found in Appendix D 4.

013148-3

## PDF page 4

MICHAEL RENGER et al.

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

FIG. 2. Qubit-resonator gate calibration. (a), (b) Pulse level
schedules used for tuning up the population exchange of the MOVE
operation and the CZ gate, respectively. For the MOVE operation,
initially only the qubit is in the excited state, while for the CZ
gate both the qubit and the computational resonator start in the first
excited state. (c), (d) Energy level diagrams showing the relevant
states involved in the MOVE operation and the CZ gate, respectively.
Both diagrams depict the diabatic (dotted gray line) and dressed
(black solid line) energy levels. The energy splittings (2g̃MOVE , 2g̃CZ )
are tuned by adjusting the coupler frequency ωTC . (e), (f) Population
oscillations between the energy levels shown in panels (c) and (d),
respectively, are obtained by scanning the qubit frequency during
the gate, ωQB , over the resonance condition (indicated by the black
dashed line), and by tuning the effective interaction strength between
the qubit and the computational resonator during the gate by adjusting the coupler frequency, ωTC . The white crosses indicate the initial
guesses for the operating point of the gates based on the population
oscillations.

B. Calibration of qubit-resonator gates

In the following, we discuss the calibration of the qubitresonator MOVE operation and the qubit-resonator CZ gate.
We use the notation |QB, TC, CR⟩ to represent the eigenstates of the system (with |g⟩, |e⟩, | f ⟩ for qubit and coupler
eigenstates, and |0⟩, |1⟩ as resonator number states), which
approximate the diabatic eigenstates of the system, i.e., at the
idling configuration. The idling configuration is a chosen set
of qubit, coupler, and resonator frequencies that results in a
minimal residual ZZ interaction. We implement the qubitresonator gates using nonadiabatic transitions between |eg0⟩
and |gg1⟩ for the MOVE operation, and |eg1⟩ and | f g0⟩ for the
CZ gate [see Figs. 2(a) and 2(b)]. This population exchange is
initiated by first bringing the involved qubit-resonator states

into resonance and then quickly tuning the frequency of the
coupler to increase the interaction strength g̃MOVE between
|eg0⟩ and |gg1⟩, or g̃CZ between |eg1⟩ and | f g0⟩, respectively.
As shown in Figs. 2(c) and 2(d), the interaction between the
involved qubit-resonator states opens up an avoided crossing
with an energy gap of 2g̃MOVE or 2g̃CZ , respectively, and shifts
the energy levels downward due to the dispersive interaction
with the coupler. For the MOVE operation, the eigenenergies of the dressed states fulfill ω̃QB = ω̃CR . This resonance
condition differs from the bare frequencies and is the result
of different hybridizations between the qubit, coupler, and
resonator, as illustrated in Appendix C. The operating point of
the MOVE operation is determined from a measurement of the
population exchange, as shown in Fig. 2(e). For the CZ gate,
we tune the |eg1⟩ and | f g0⟩ states close to resonance such
that ω̃QB = ω̃CR + |α|. Here, α is the anharmonicity of the
qubit participating in the CZ gate. Similarly to the MOVE, we
measure the population exchange of the CZ qubit as shown in
Fig. 2(f). In contrast to the above, however, the operating point
of the CZ gate is where the qubit, starting in |e⟩, completes
a full oscillation through | f ⟩ and returns back to the initial
|e⟩ state, as the CZ gate only modifies the phase and not the
population of the basis states. The full tune-up procedure for
both qubit-resonator gates, including the calibration of the
conditional π phase shift required for the CZ gate, is discussed
in detail in Appendix D. A derivation of the analytical expression for the conditional phase is presented in Appendix C.
During the qubit-resonator gates, the transition frequencies
of both components change, resulting in the accumulation of
single-qubit phases. We correct for these phases by applying
virtual Z (VZ) gates to the respective XY qubit drive pulses
[52]. To obtain the optimal VZ correction for the qubit when
applying the MOVE operation, we perform the operation an
even number of times and calibrate the common phase obtained when moving a superposition state from the qubit to
the computational resonator and back. For the CZ gate, two
separate VZ corrections are calibrated, one for the computational resonator and one for the CZ qubit. The VZ correction
of the computational resonator is determined indirectly via
the qubit that was used to prepare the state in the resonator
(MOVE qubit). The relative phase rotation of a state that has
been transferred to the computational resonator with respect
to the rotating frame of the MOVE qubit results in a timedependent phase that accumulates at a rate corresponding
to the frequency difference between the MOVE qubit and
the resonator [53]. To properly correct for single-qubit phase
accumulation in arbitrary algorithms, we need to distinguish
this time-dependent phase from fixed phase corrections that
depend only on the flux pulse shape implementing a certain
gate. Details on the calibration of the single-qubit phase corrections can be found in Appendixes D 1 and D 2.
C. Benchmarking Qubit-Resonator Gates

For benchmarking qubit-resonator gates, we employ the
technique of interleaved randomized benchmarking (iRB)
[54,55]. The average gate fidelity is estimated from the decay of the measured qubit population as a function of the
applied sequence length m. The iRB circuit for the MOVE
operation is shown in Fig. 3(a). Since we apply the MOVE

013148-4

## PDF page 5

SUPERCONDUCTING QUBIT-RESONATOR QUANTUM …

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

FIG. 3. Interleaved randomized benchmarking experiments for qubit-resonator gates. (a) Circuit for benchmarking the MOVE operation
via interleaved randomized benchmarking. The sequence consists of m single-qubit Clifford gates C1 interleaved with k repetitions of two
subsequent MOVE operations, which effectively implement an identity. The final operation U −1 inverts the applied sequence. (b) Circuit for
benchmarking the CZ gate via interleaved randomized benchmarking. Two-qubit Clifford gates C2 are interleaved with MOVE-lCZ-MOVE
operations for a varying number of CZ gates l. (c) Experimental data of the sequence fidelity for randomized benchmarking with k = 1, . . . , 4
interleaved double MOVE operations and the reference single-qubit Clifford sequence (open blue circles) as a function of the number of
Clifford gates. (d) Extracted fidelity of the interleaved gate sequence as a function of k (solid black circles) and quadratic fit (dashed line).
(e) Experimental data of the sequence fidelity for randomized benchmarking with interleaved MOVE-lCZ-MOVE gate sequences and the
reference two-qubit Clifford sequence (open blue circles) as a function of the number of Clifford gates. (f) Extracted fidelity of the interleaved
MOVE-lCZ-MOVE gate sequence as a function of l (solid black circles) and quadratic fit (dashed line).

operation only to states for which either the qubit or the
computational resonator is unpopulated, the problem of calculating the average gate fidelity reduces from an integration
over all possible input states for a bipartite quantum system to considering only a single effective two-level system.
Consequently, we benchmark the MOVE operation in the
framework of single-qubit RB interleaving pairs of MOVE
operations, which effectively implement an identity gate. To
reduce the uncertainty of the extracted double MOVE fidelity,
we perform multiple instances of the iRB experiment, interleaving the effective identity gate (MOVE)2k for different
integer numbers k. The ground-state probability of the qubit
is then fitted by Pk (m) = Apmk + B, where the depolarization
probability pk is treated as independent fit parameter for each
k, and the amplitude A as well as the offset B are fitted
simultaneously for all k. For each dedicated m in the iRB
experiment, we apply 60 different random Clifford sequences
and average the experiment over 256 repetitions. In Fig. 3(c),
we show the result of such an iRB experiment for QB 2 for up
to k = 4. We extract the fidelity per interleaved gate sequence
as a function of k, as shown in Fig. 3(d). We observe that
the interleaved fidelity can be approximated by the fitting
function fm (k) = 1 − αm k 2 − βm k [56], where the quadratic
contribution results from quasistatic noise and remaining gate
calibration errors, and the linear term corresponds to depolarization errors. For example, a small error in the exchange

angle of the MOVE operation would subsequently lead to populating higher resonator modes with increasing k, according
to Eq. (2), and the loss in qubit population is, to first order,
proportional to k 2 . From the fit, we obtain αm = 4.6 × 10−4
and βm = 6.1 × 10−3 . We determine the fidelity of the double MOVE operation as Fmm = fm (1) = 99.34 ± 0.03. The
single-qubit Clifford fidelity, averaged over all six qubits, is
0.9990 ± 0.0002 and the double MOVE fidelity, averaged
over all qubit-resonator pairs, is F̄mm = 0.988 ± 0.006, where
the error bars represent the standard deviation of the respective
individual fidelities. We note that recent work has introduced
network benchmarking [57] and demonstrated its utility in
evaluating state transfer operations in the context of quantum
networks [58]. However, this technique requires direct control
over the state of all computational components, which is not
feasible in our device due to the inability to apply single-qubit
gates to the computational resonator.
Figure 3(b) shows the iRB circuit for estimating the qubitresonator CZ gate fidelity. In order to sample all possible
input states for the CZ gate acting between a qubit and a
computational resonator, we use the MOVE operation to populate the resonator with an arbitrary state. After applying the
CZ gate, the resonator has to be brought back to its vacuum
state by applying another MOVE operation. In contrast to the
benchmarking of the MOVE operation, here we can use twoqubit Clifford benchmarking and integrate over all possible

013148-5

## PDF page 6

MICHAEL RENGER et al.

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

two-qubit states of the MOVE and CZ qubits. We generate
two-qubit Clifford gates from single-qubit gates and effective
CZ gates acting between the MOVE and the CZ qubit, which
are composed of the native qubit-resonator MOVE and CZ
operations. Similar to iterative iRB [59], we vary the number
l of interleaved CZ gates between the two MOVE operations
and refer to this experiment as MOVE-lCZ-MOVE iRB. In
Fig. 3(e), we show the corresponding iRB result when using QB 1 as the CZ qubit and QB 2 as the MOVE qubit,
for up to l = 5 CZ gates. The data are obtained using 30
different random Clifford sequences and averaged over 256
repetitions. We extract the interleaved fidelity as a function
of l, as shown in Fig. 3(f). Notably, this quantity reflects not
only the performance of the qubit-resonator CZ gate but also
the fidelity of the state transfer between the MOVE qubit
and the computational resonator, CR, since this is a crucial
prerequisite for entangling nonadjacent qubits using this gate
sequence for odd values of l. The interleaved fidelity follows
fcz (l ) = γm − αcz l 2 − βcz l, in analogy to fm (k). Here, the
offset γm quantifies the errors induced by the MOVE operation
at the beginning and at the end of the interleaved sequence.
We note that the data point at l = 0 follows the quadratic
trend for l ⩾ 1; therefore, we can assign individual errors
to the MOVE and CZ operations, even though they do not
commute. More generally, the interleaved sequence fidelity
exhibits a consistent trend for both even and odd values of
l, which correspond to benchmarking an identity and CZ
gate unitary, respectively. From the quadratic fit shown in
Fig. 3(f), we obtain αcz = 7.32 × 10−4 , βcz = 1.01 × 10−2 ,
and γm = 0.989. We observe that γm is slightly smaller than
the double MOVE fidelity Fmm extracted from the single-qubit
RB presented above. We attribute the mismatch in the fidelity
to the idling infidelity of the CZ qubit during the two MOVE
operations, which only affects γm . Furthermore, the input state
sampling in two-qubit Clifford benchmarking is different as
compared to single-qubit RB, which can slightly affect the
inferred double MOVE fidelity. The fidelity of the qubit-qubit
CZ gate, implemented as a sequence of MOVE-CZ-MOVE
gates, is directly measured using the iRB protocol for l = 1
and the result is 0.978 ± 0.002. The corresponding two-qubit
Clifford fidelity is 0.9625 ± 0.0007. We extract the fidelity
of an individual CZ gate between QB 1 and the computational resonator as Fcz = fcz (1)/γm = 98.90 ± 0.05. Because
the value of the quadratic coefficient, αcz , is small compared to
the linear coefficient, βcz , we conclude that the depolarization
error is the main mechanism limiting the CZ gate fidelity.
Furthermore, we average the fidelity of all six qubit-resonator
CZ gates and obtain F̄cz = 0.983 ± 0.009, where the error
bar represents the standard deviation over the respective individual gate fidelities. The individual double MOVE and CZ
fidelities are listed in Appendix D 4.
Next, we estimate the fidelity limits set by decoherence
[60]. For the CZ gate, we additionally take into account that
we leave the computational space during the |1, e⟩ ↔ |2, g⟩
population exchange cycle [61]. Details about the coherence
limit estimation are provided in Appendix E. An estimate for
the coherence limit averaged over all qubit-resonator pairs is
c
F̄mm
= 0.993 ± 0.001 for the double MOVE operation and
F̄czc = 0.993 ± 0.002 for the CZ gate. These values provide
an upper bound for the coherence-limited fidelity because the

coherence times used in the calculation are measured at the
qubit idling frequency configuration, while there is increased
flux sensitivity due to qubit frequency tuning during the gate
operation. In addition, we do not take hybridization with the
coupler into account. Consequently, at least 58.3% (41.2%) of
the double MOVE (CZ) infidelity is attributed to decoherence
during the operation.
IV. QUBIT-RESONATOR QPU APPLICATIONS

We demonstrate the capabilities of our qubit-resonator
QPU and inspire further algorithmic development by presenting four distinct examples. First, we investigate the generation
of multipartite entanglement by preparing GHZ states. Next,
we use the Q-score benchmark to determine the ability of
our QPU to solve combinatorial optimization problems. Finally, we discuss how the MOVE operation can be used as
a true Jaynes-Cummings gate to access the higher levels of
the computational resonator and present a simulation of the
ground-state energy of the transverse-field Ising model using
a variational approach.
A. GHZ state preparation

As a global benchmark for the QPU performance, we examine its quantum entanglement properties. A fundamental
criterion for quantum computing is the ability to entangle all
qubits in the processor into a genuinely multiqubit entangled
(GME) state. Here, we demonstrate GME by preparing an n⊗n
⊗n
qubit GHZ state [62], which is defined as |ψ⟩GHZ = |g⟩ √+|e⟩
.
2
We generate the GHZ state by employing two MOVE operations between a single qubit and the computational resonator
and an interleaved cascade of qubit-resonator CZ gates [see
Fig. 4(a)]. In between, multiple CZ gates are applied to entangle the computational resonator with all the peripheral qubits
(apart from the MOVE qubit). Therefore, the only overhead in
the number of gates, as compared to the case of a square-grid
topology, are the two MOVE operations, which are required to
(de)populate the computational resonator. Note that no singlequbit gates are applied to the MOVE qubit [QB 1 in Fig. 4(a)]
between the first and second MOVE operations. This ensures
that this qubit is in the ground state when the second MOVE
operation is applied.
A quantum state |ψ⟩ is declared to be GME if the fidelity
of the experimental state ρ with respect to the pure state is
F|ψ⟩ = ⟨ψ| ρ |ψ⟩ > 0.5 [63]. We estimate the fidelity of the
prepared GHZ state using the multiple quantum coherences
method [64,65] to certify its entanglement properties.
Figure 4(b) presents GHZ state fidelities both with and
without readout-error mitigation (REM). The results successfully confirm the presence of GME for all six qubits,
demonstrating that the entire device is entangled. Without
mitigation, we obtain a GHZ state fidelity of F|ψ⟩GHZ = 0.815.
Furthermore, we mitigate readout errors by multiplying the
raw readout results by the inverse of the readout assignment
matrix, which includes both state preparation and measurement errors. The assignment matrix is a tensor product of all
single-qubit assignment matrices and therefore assumes the
readout errors to be completely uncorrelated. The mitigated
GHZ fidelity for N = 6 qubits is F|ψ⟩GHZ = 0.86.

013148-6

## PDF page 7

SUPERCONDUCTING QUBIT-RESONATOR QUANTUM …

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

FIG. 5. Measured Q-score ratio as a function of problem size
n. For each problem size, the average is taken over 60 randomly
sampled Erdős-Rényi graphs. The error bars show the standard error
of the mean.

FIG. 4. GHZ state characterization. (a) Circuit for preparing a
GHZ state with a variable number of entangled qubits N on a
qubit-resonator QPU with star topology. (b) The fidelity F|ψ⟩GHZ is
calculated from the GHZ state population and its coherence, inferred
via multiple quantum coherences. We show the GHZ state fidelity as
a function of the qubit number N, obtained by analyzing the data both
with (blue circles) and without (red triangles) applying readout-error
mitigation.
B. Q-score benchmark

In this section, we assess the performance of the qubitresonator QPU in solving combinatorial optimization problems. Specifically, we benchmark its ability to compute
solutions for the maximum-cut problem using the Q-score
benchmark [66]. The Q-score is defined for random ErdősRényi graphs, where each edge is included with probability
1/2. A quantum processor passes the Q-score test for a given
problem size n if it achieves a performance metric β(n) ⩾
β ⋆ , where β(n) quantifies the fraction of the optimality gap
between a random guess and the optimal solution that is
measured on the quantum system on average. If β(n) = 1,
exact solutions are found, but if β(n) = 0, random solutions
are found. Following Ref. [66], we take β ⋆ = 0.2, meaning
that the system passes the Q-score test for a given n if it
performs on average 20% better than random guessing. Due to
the accumulation of noise, passing the Q-score test becomes
increasingly challenging as the problem size grows.
We evaluate Q-score performance β(n) by using a depth
p = 1 quantum approximate optimization algorithm (QAOA)
circuit [67,68], where the optimal circuit parameters are determined through analytical calculations [69]. By ensuring that
the quantum processor operates with optimally pretuned parameters, we avoid expensive quantum-classical optimization
loops and ensure the most efficient use of quantum resources.
In the QAOA algorithm, the number of RZZ interactions
equals the number of edges |E | in the problem graph. As we

consider random Erdős-Rényi graphs with edge probability
1/2, we would need to implement on average n(n − 1)/2 CZ
gates on an all-to-all connected topology. We note that on
a square-grid topology, we would require 50%–75% more
CZ gates for large n depending on which SWAP strategy is
used [70]. This highlights the potential of the star topology in
solving dense optimization tasks.
To further enhance performance, we execute quantum circuits on an optimized qubit layout, following the methodology
introduced in Ref. [71]. This preprocessing step evaluates a
noise score for each possible qubit layout, considering the gate
count of the circuit along with the single- and two-qubit gate
error rates of the hardware. Furthermore, we apply readouterror mitigation using the mthree package [72], allowing us to
exclude measurement errors from the noise score evaluation.
We demonstrate that our QPU passes the Q-score test for
problem sizes defined across all n = 6 qubits of the QPU, as
illustrated in Fig. 5. Additionally, we increase the Q score to
n + 1 = 7 by using the virtual node technique [73,74], which
breaks the Z2 symmetry of the maximum-cut problem and
introduces only a minor overhead from a few single-qubit Z
gates.
We note that for such small problem sizes, the CZ gatecount advantage of the star topology is rather small: e.g., for
n = 6, we require on average 15 CZ gates on the star topology
and 17 CZ gates on a square-grid topology. In addition, we
also need to implement 2(n − 1) MOVE operations on the
qubit-resonator star. For larger n, however, the gate-count
advantage of the star topology becomes significant and approaches the asymptotic percentages stated above. Therefore,
scaling up the qubit-resonator star topology is a worthwhile
effort.
C. Jaynes-cummings gate to access
the higher resonator levels

In the previous section, we have restricted the MOVE
operation to the single-excitation manifold of the coupled
qubit-resonator system to ensure that the resonator remains
in the {|0⟩ , |1⟩} subspace. Here, we remove this restriction
and populate higher resonator levels by applying the MOVE
operation on the |1, e⟩ state to verify that we are indeed
implementing a Jaynes-Cummings gate as defined in Eq. (2).
We construct circuits to investigate the dynamics of multiple

013148-7

## PDF page 8

MICHAEL RENGER et al.

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

Expt.

Expt.

Expt.

FIG. 6. (a) Quantum circuit to populate higher excited levels of the computational resonator by repeated excitation of QB 3, followed by
application of the MOVE operation. In addition, a second idle qubit QB 2 is read out. (b) Circuit for measuring the free time evolution of the
population of the first two excited CR levels. After populating CR using QB 3, QB 2 is used to implement a Ramsey sequence that enables the
measurement of the free resonator state evolution as a function of the delay time τ . The protocol additionally contains two physical Z rotations,
Zϕ and Zϕ ′ , which are used to compensate for phase offsets induced by the JC interaction. (c) Detected population of QB 3 and QB 2 (blue) for
the circuit shown in panel (a) and comparison with the ideal JC model (orange). (d) Detected population of QB 2 as a function of τ (blue dots)
for ϕ = ϕ ′ = 0. The red line corresponds to a fit according to Eq. (6). (e) QB 2 population as a function of τ (blue dots) after compensating all
the phase offsets by employing physical Z rotations, ϕ and ϕ ′ . The orange line is the theoretical prediction from the ideal JC model.

resonator excitations |n⟩ interfering with each other, similar
to Ref. [75]. With these interference fringes, we measure and
then correct nonideal phases introduced by the MOVE operation to recover the dynamics of an ideal Jaynes-Cummings
gate.
We can populate higher levels of the computational resonator by repeatedly employing the MOVE operation, thus
providing additional computational degrees of freedom. In
fact, exploiting the equidistant resonator energy spectrum can
be used, for example, for digital quantum simulation [36] or
for the implementation of the quantum Fourier transformation
in oscillating modes. In the remainder of this section, we
experimentally demonstrate how higher energy levels of the
computational resonator can be accessed by applying successive MOVE operations, and we provide an exemplary circuit
for phase calibration.
The MOVE operation is calibrated in the single-photon
manifold. For states containing n resonator photons, Eq. (2)
predicts that the effective
Rabi frequency increases character√
istically as n = n [76], implying swap angles exceeding
π /2 and thus creation of superposition states containing n ⩾ 2
photons. In this case, the JC interaction implements a mapping analogous to a fermionic simulation gate [6,77]. If the
interaction is switched on for a gate time τ , the propagator
corresponding to Eq. (1) leads to the general JC gate:
|g, n⟩ → cn− |g, n⟩ − isn+ |e, n − 1⟩,
+
−
|e, n⟩ → cn+1
|e, n⟩ − isn+1
|g, n + 1⟩,

(4)

cn± ≡ e−i(γn ±ζn ) cos(n τ ),

(5)

where
sn± ≡ e−i(γn ±χn ) sin(n τ ).

The phases γn , ζn , and χn are single-qubit phases resulting
from the dynamic frequency change of the involved components [78]. The calibration of the MOVE operation sets the
constraint τ = π /2.
A simple circuit for demonstrating the JC interaction by
subsequent application of two MOVE operations between
QB 3 and CR is shown in Fig. 6(a). A second idle qubit, QB 2,
is read out to test for potential crosstalk and state leakage. The
qubit-qubit population as well as the theoretically expected
probabilities Pee = |s2± |2 ≃ 0.63 and Peg = |c2± |2 ≃ 0.37 are
plotted in Fig. 6(c). We observe that the experimental data
can be well explained by climbing the JC ladder, according
to Eq. (4).
The aforementioned |e, 1⟩ ↔ |g, 2⟩ population exchange
experiment is independent of potential phase shifts in the twophoton manifold. This is not generally the case for circuits
involving superposition states or excitation swaps between the
computational resonator and different qubits. In a more general case involving superposition of states containing different
resonator photon number or in case of JC interaction between
the resonator and multiple qubits, the phases γn , ζn , and χn
need to be determined accurately, e.g., by the use of physical
Z rotations or Floquet theory [78]. These phase shifts depend
on the flux pulse window and are required to be calibrated
separately for each JC manifold to realize the ideal JC interaction. For the conventional MOVE operation, the only relevant
phase, γ1 , is compensated by employing a VZ rotation for the
involved qubit drive signal. Correcting for these phase offsets
in circuits leading to photon number contributions n ⩾ 2 requires additional control degrees of freedom, such as physical
Z rotations.
An example for such a circuit is shown in Fig. 6(b). First,
we move an excitation into the computational resonator using

013148-8

## PDF page 9

SUPERCONDUCTING QUBIT-RESONATOR QUANTUM …

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

QB 3. Subsequently, we use QB 2 to implement a Ramsey
sequence for the populated resonator. After the first (second)
MOVE operation involving QB 2, we insert a physical Z rotation Zϕ (Zϕ ′ ). The frequency detuning  between QB 2 and
CR induces a change of the rotating reference frame when the
MOVE operation is applied. This change of reference frame
induces a phase evolution proportional to the delay τ , manifesting as Ramsey oscillations. For the circuit in Fig. 6(b), the
QB 2 population can be expressed as
[
]
Pe = 21 1 − c22 cos(t + φ) + s22 cos(2t + φ ′ ) , (6)
where φ ≡ −2γ2 − 2ζ2 + ϕ ′ and φ ′ ≡ −2γ2 + ϕ ′ − ϕ. Consequently, in contrast to the conventional Ramsey experiment
with an oscillation frequency , we expect additional beating with frequency 2 due to the computational resonator
state contributions from n = 2 during the free state evolution.
Figure 6(d) shows the experimental result for the populatedresonator Ramsey experiment for detuning /2π = 281 MHz
and ϕ = ϕ ′ = 0, as well as a fit according to Eq. (6). From
the two fit parameters, φ = −2.73 and φ ′ = −1.18, we can
determine the angles γ2 and ζ2 as well as the correct choice
of ϕ and ϕ ′ to implement an ideal JC gate. The result from a
subsequent experiment after employing the physical Z corrections is shown in Fig. 6(e). Following this phase calibration,
the circuit output can be well described by the ideal JC theory.
These proof-of-principle results demonstrate that the JC gate
phases can be controlled using physical Z rotations. Additional information, as well as the derivation of Eq. (6), is
provided in Appendix F.
Note that while restricting the maximal resonator photon
number to 1 enables effective all-to-all connectivity via the
MOVE operation, releasing this constraint leads to an alternative operation regime with all peripheral qubits coupled to
a central active multilevel element. Consequently, our quantum hardware can be operated in two fundamentally different
ways depending on a given application using the same native
gate set.
D. Error mitigation to improve circuit execution reliability

The presence of noise in near-term quantum devices introduces significant errors in measured expectation values,
limiting the accuracy of quantum computations. Error mitigation techniques provide a means to recover meaningful results
without requiring additional hardware resources, making them
a crucial component of practical quantum computation. We
demonstrate that the presented QPU is fully compatible with
the state-of-the-art and established error mitigation methods,
which can substantially diminish the impact of the hardware
noise on the quantum algorithm execution.
We focus on estimating the ground-state energy of the
transverse-field Ising model (TFIM), a well-known system in
quantum many-body physics. We consider this system in its
critical phase (associated with a transverse-field strength of
g = 1) for a six-qubit system with periodic boundary conditions and nearest-neighbor connectivity. The Hamiltonian of
the model is given by
∑ j ∑
H = −g
σX −
σZi σZj ,
(7)
j

(i, j)

FIG. 7. (a) Measured ground-state energy of the TFIM, relative
to its noise-free value, as a function of the noise scale factor λ.
(b) Error-mitigated ground-state energy of the TFIM, relative to its
noise-free value, obtained using NRE and ZNE for different choices
of noise scale factors. In the case of ZNE, an exponential fitting procedure is employed. NRE is performed following the same approach
outlined in Ref. [79]. Error bars for all error mitigated data points
represent statistical uncertainties associated with a total of 240 000
measurement shots.

where the summation over (i, j) accounts for qubit pairs with
direct interactions.
We estimate the ground-state energy with a variational
approach based on QAOA with p = 3 layers [80]. The circuit
parameters are optimized in a noise-free setting and subsequently transpiled to match the connectivity constraints and
native gate set of the QPU. The resulting target circuit consists
of 36 entangling CZ gates and 36 MOVE operations, which
introduce noise and lead to errors in the measured energy
expectation values.
To mitigate these errors, we employ a recently introduced
algorithmic error mitigation technique known as noise-robust
estimation (NRE) [79]. This method has been demonstrated
to effectively recover noise-free expectation values with high
accuracy, even without applying additional error-reduction
techniques such as readout-error mitigation or randomized
compiling [81]. For comparison, we also apply the wellestablished zero-noise extrapolation (ZNE) method [82].
Both NRE and ZNE require amplification of hardware
noise, necessitating the execution of the target circuit at different noise levels. Assuming that the circuit noise rate can
be characterized by ϵ0 , we parametrize the noise as ϵ = λϵ0 ,
where λ is the dimensionless noise scale factor. We realize
different values of λ by using gate-level unitary folding [83].
This method amplifies noise by scaling the entire circuit unitary, U . For example, a noise amplification factor of λ = 3
is realized by replacing U with UU †U , increasing the circuit
depth proportionally. For λ = 2, one first considers a unitary
Uh that corresponds to a subset of the qubit operations, having
half the depth of the original circuit. Then, U is replaced by
UUh†Uh , introducing some unknown approximation error in
the noise amplification process. Importantly, the performance
of NRE is known to be largely insensitive to imprecise noise
amplification [79]. This, in turn, relaxes the demanding requirement for precise noise amplification.
Figure 7(a) presents the measured ground-state energy as
a function of noise scale factors. Due to inherent hardware

013148-9

## PDF page 10

MICHAEL RENGER et al.

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

FIG. 8. Simplified linearized circuit diagram of the QPU, showing a single QB coupled via a TC to the CR. The couplings are mediated by
coupler extender waveguides (Ext). The direct capacitance Cdirect is part of of the TC geometry and ensures that there is an idling configuration
where the ZZ interaction is zero. The remaining five qubits are connected to the CR in a similar fashion, each with a similar TC. In the model,
each node also contains a parasitic capacitance to ground, which is omitted from the drawing for clarity.

noise, the measured energy is reduced by approximately 20%
from its ideal noiseless value at λ = 1. In Fig. 7(b), we show
the results after applying error mitigation with various different selections for noise scale factors. We find that NRE
substantially improves the accuracy of noisy measurements of
the QPU, yielding a final accuracy exceeding 96%, regardless
of the specific noise amplification settings.

V. CONCLUSION

We have demonstrated a QPU based on qubits coupled to
a common computational resonator. We have calibrated and
benchmarked the qubit-resonator CZ gate and the MOVE operation, which, in combination with single-qubit gates, form a
universal set of quantum gates. Furthermore, we have generated genuine multipartite entanglement between six qubits in
the form of a GHZ state with a readout-error mitigated fidelity
of 0.86 and provided a proof-of-principle demonstration on
how to populate and calibrate higher level resonator states,
eventually realizing a Jaynes-Cummings gate. Such a gate can
be used as a building block for hybrid quantum computing
schemes involving continuous and discrete variables [37]. In
addition, we have shown a practical use case by employing our
qubit-resonator QPU for QAOA applications including error
mitigation. Finally, the presented proof of concept QPU shows
a paradigm for connectivity in superconducting architectures
to match targeted applications. These include, for example,
advanced quantum error correction strategies such as the color
code [84–86].

ACKNOWLEDGMENTS

This work was supported by the German Federal Ministry of Education and Research through the projects DAQC
(13N15688), QSolid (13N16155), and Q-Exa (13N16065).

DATA AVAILABILITY

The data that support the findings of this article are not
publicly available. The data are available from the authors
upon reasonable request.

APPENDIX A: QPU DESIGN AND FABRICATION

The star topology QPU consists of a 4.2 mm long coplanar
waveguide resonator in the quarter-wavelength configuration
(computational resonator), six frequency-tunable couplers,
and six frequency-tunable qubits. The latter two are implemented using symmetric SQUIDs, enabling to tune the
transition frequency close to zero [87]. We model this QPU
as a linearized circuit, where the SQUIDs have been replaced by linear inductors, as shown schematically for a
single QB-TC-CR connection in Fig. 8. Here, the localized
qubit and coupler islands are modeled as pure capacitive structures (including a capacitance to ground at each
island) extracted from finite element simulations of the respective geometry. The TCs are coupled with interdigital
capacitors near the open-circuit end of the CR. The QBTC and TC-CR connections are formed by coupler extender
waveguides, similar to those used in Ref. [44], which enable physically spacing out the qubits while still coupling
them all near the maximum voltage of the computational
resonator mode. The coupler extender waveguides and the
computational resonator are modeled as transmission lines to
accurately include their inductive contributions. All elements
are referenced to a common ground plane in the design and
the model.
We extract the mode frequencies in this model from the
divergences of the frequency-dependent impedance Z (ω) calculated at the respective qubit or coupler island, or for the CR
at its open end. We use the following procedure to numerically
estimate the frequencies and coupling strengths of the full
six-qubit star system. First, we tune all QB and TC modes
far away from the resonator mode by adjusting their inductance values, and from the remaining model extract the bare
resonator frequency ωr = 4.3 GHz. Then, we pairwise tune
two modes on coresonance, while tuning all remaining modes
far away, and extract the corresponding normalized coupling
strength βi j = gi j /ω from the frequency splitting 2gi j . For
tuning the CR mode, we adjust the modeled transmissionline length. Table I shows the modeled and experimentally
measured coupling strengths.
The QPUs were fabricated at the OtaNano Micronova
cleanroom. A high-resistivity (ρ > 10 k cm) n-type undoped (100) 6-in. silicon wafer, precleaned to ensure a

013148-10

## PDF page 11

SUPERCONDUCTING QUBIT-RESONATOR QUANTUM …

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

TABLE I. Coupler parameters extracted from the design model, and for QB-TC couplings measured experimentally. The subscripts q, c,
and r represent the QB, TC, and CR, respectively.
Parameter

Description

QB 1

QB 2

QB 3

QB 4

QB 5

QB 6

βqc
βcr
βqr

Design model

0.0226
0.0225
0.0020

0.0226
0.0225
0.0020

0.0226
0.0226
0.0020

0.0226
0.0226
0.0020

0.0230
0.0225
0.0020

0.0230
0.0225
0.0020

βqc

Experimentally measured

0.017

0.022

0.021

0.021

0.021

0.022

nonoxidized surface, served as the substrate. A 200-nm-thick
high-purity niobium (Nb) layer was first deposited via sputtering to form the base superconducting circuit layer. Coplanar
waveguides and capacitive structures were patterned using
photolithography with a mask aligner, followed by reactive
ion etching to define the Nb features. Postetching, photoresist
residuals were removed via ultrasonic cleaning in acetone
and isopropanol (IPA), followed by nitrogen drying. Josephson junctions for the transmon qubits were fabricated on
individual dice via electron-beam lithography. A bilayer of
methylmethacrylate/polymethylmethacrylate resist was employed, with development in a sequence of methyl isobutyl
ketone:IPA (1:3), methyl glycol, and IPA. Residual resist
was removed via an oxygen plasma descum process. The
junctions were fabricated using electron-beam shadow evaporation technique, depositing two aluminum (Al) layers under
ultrahigh vacuum. Lift-off in heated acetone finalized the
junction structures. Airbridges for interlayer connections were
formed by Al, followed by a second lift-off process. Postfabrication, the room-temperature resistance of the Josephson
junctions was measured to verify junction integrity prior to
cryogenic characterization. This process integrates high-yield
lithography, contamination-minimized etching, and precise
junction fabrication, ensuring robust superconducting circuits
for quantum computing applications.

electron mobility transistor and a warm amplifier. A group of
isolators protects the readout resonator from noise.
APPENDIX C: ANALYTIC DESCRIPTION OF
QUBIT-RESONATOR MOVE AND CZ OPERATIONS

We consider here the approximate diagonalization of a
setup that can be modeled with the Hamiltonian
Ĥ = Ĥ0 + V̂ ,

(C1)

where Ĥ0 is an uncoupled (diagonal) Hamiltonian and V̂ is
a Hermitian operator describing the interactions between the
eigenstates of Ĥ0 . In particular, we concentrate on a system
that comprises a qubit, a resonator, and a tunable coupler.
Consequently, the unperturbed Hamiltonian can be written as
h̄
Ĥ0 = h̄ωq âq† âq + αq âq† âq† âq âq + h̄ωr âr† âr + h̄ωc âc† âc
2
h̄
+ αc âc† âc† âc âc ,
(C2)
2
where ωq , ωr , and ωc are the (angular) frequencies of the qubit,
resonator, and coupler, respectively, αq is the anharmonicity of
the qubit, αc is the anharmonicity of the coupler, and âi and
âi† are the annihilation and creation operators for the qubit,
resonator, and coupler, respectively, for i ∈ {q, r, c}. The interaction part, V̂ = V̂1 + V̂2 , describes the couplings between
the qubit, resonator, and coupler degrees of freedom. We have
defined the interaction Hamiltonians as
V̂1 = −h̄gqc (âq† − âq )(âc† − âc ) − h̄grc (âr† − âr )(âc† − âc ),

APPENDIX B: EXPERIMENTAL SETUP

Figure 9 illustrates the experimental setup with a simplified
QPU circuit diagram featuring one qubit QB (including its
readout resonator RO and Purcell filter), the computational
resonator CR, and a tunable coupler TC that couples the
qubit to the computational resonator. The QPU and some
electrical components are maintained at cryogenic temperature in a Bluefors XLD400 cryostat. The control electronics
instruments, at room temperature, are connected to the QPU
via coaxial cables. These contain microwave attenuators and
filters distributed over the various temperature stages of the
cryostat. Flux pulses and flux biases are generated by arbitrary waveform generators (Zurich Instrument HDAWG8), the
qubit drive pulses are generated by signal generators (Zurich
Instrument SHFQC6+), and the readout pulses are generated and acquired by a quantum analyzer (contained in the
same SHFQC6+ instrument). Before digitization, the readout
pulses are amplified by a cryogenic amplifier based on a high

V̂2 = −h̄gqr (âq† − âq )(âr† − âr ).

(C3)

Above, we denote the coupling strength between the qubit and
the resonator with gqr , the coupling strength between the qubit
and the coupler with gqc , and the coupling strength between
the resonator and the coupler with grc .
Here, we assume that coupling to the coupler is dispersive,
i.e., gqc ≪ |qc | and grc ≪ |rc |. However, we do not make
such assumption for the qubit-resonator coupling gqr . Since
the coupler is in the dispersive limit, we make a SchriefferWolff transformation ÛSW = eŜ in order to eliminate the
first-order interaction V̂1 with the coupler, and consequently
obtain an effective Hamiltonian for the qubit-resonator system. In general, the Schrieffer-Wolff transformation can be
expanded using the Baker-Campbell-Hausdorff lemma as

013148-11

†
ÛSW Ĥ ÛSW
= Ĥ + [Ŝ, Ĥ ] +

1
[Ŝ, [Ŝ, Ĥ ]] + · · · .
2!

(C4)

## PDF page 12

MICHAEL RENGER et al.

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

FIG. 9. Experiment setup schematically depicting the QPU in its cryogenic environment. The QPU is connected via coaxial lines to control
electronics at room temperature. The temperature of each stage is indicated.

Here, we assume that [Ŝ, Ĥ0 + V̂2 ] = −V̂1 , which removes the first-order dependence on V̂1 from the transformed Hamiltonian.
The condition obtained above is fulfilled in our setup if we write Ŝ = Ŝq + Ŝr and define [88,89]
[
∑ √
( nq +1,nq nc ,nc +1
)
gqc
n ,n +1
Ŝq =
π̂q
(nq + 1)(nc + 1)
π̂c
− π̂q q q π̂cnc +1,nc
qc + nq αq − nc αc
nq ,nc ∈{0,1}
]
( nq +1,nq nc +1,nc
)
gqc
n ,n +1
−
π̂q
(C5)
π̂c
− π̂q q q π̂cnc ,nc +1 ,
qc + nq αq + nc αc
[
∑ √
( nr +1,nr nc ,nc +1
)
grc
Ŝr =
(nr + 1)(nc + 1)
π̂c
− π̂rnr ,nr +1 π̂cnc +1,nc
π̂r
rc − nc αc
nr ,nc ∈{0,1}
]
( nr +1,nr nc +1,nc
)
grc
−
π̂r
(C6)
π̂c
− π̂rnr ,nr +1 π̂cnc ,nc +1 ,
rc + nc αc
where the operators π̂kn,m = |n⟩⟨m| act in the Hilbert space
of k ∈ {q, r, c}, and we have defined rc = ωr − ωc , qc =
ωq − ωc , qc = ωq + ωc , and rc = ωr + ωc . Consequently,
the transformed Hamiltonian can be written in second order

in the coupling strengths as

013148-12

†
ÛSW Ĥ ÛSW
= Ĥ0 + V̂2 + 21 [Ŝ, V̂1 ].

(C7)

## PDF page 13

SUPERCONDUCTING QUBIT-RESONATOR QUANTUM …

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

In our architecture, we typically consider that the coupling
strength gqr is almost an order of magnitude smaller than gqc
and grc .
After performing the Schrieffer-Wolff transformation
[evaluating Eq. (C7)] [43,88], we obtain corrections to qubit
and resonator frequencies and effective couplings between
the relevant (coupler-dressed) states that govern the MOVE
and CZ operations. By additionally setting the energy of the
ground state to zero, we obtain that the qubit and resonator
frequencies and the effective couplings between the relevant
single- and two-excitation eigenstates can be written as
ω̃q = ωq +

g2qc

2g2qc

+

g2qc

,
(C8)
qc + αq
qc
g2
g2
(C9)
ω̃r = ωr + rc − rc ,
qc
rc
(
)
gqc grc 1
1
1
1
,
g̃MOVE ≡ g̃0e,1g = gqr +
+
−
−
2
qc
rc
qc
rc
(C10)
√
(C11)
g̃1e,2g = 2g̃0e,1g,
(
[
√
gqc grc 1
1
1
g̃CZ ≡ g̃1e,0 f = 2 gqr +
+
−
2
rc
qc + αq
rc
)]
1
.
(C12)
−
qc + αq
qc

−

Here, we have defined that g̃0e,1g is the coupling strength
between the (coupler-dressed) states |eg0⟩ and |gg1⟩,
g̃1e,2g between the states |eg1⟩ and |gg2⟩, and g̃1e,0 f between the states |eg1⟩ and | f g0⟩ (state labeling goes as
|qubit, coupler, resonator⟩). We assume here that the coupler
is in the ground state. Furthermore, we also assume that
the qubit and coupler frequencies are constant and, thus, the
relations obtained above are a good approximation only for
idling gates or for longer (adiabatic) gates dominated by a
long interaction time. Our effective Hamiltonian (not shown)
also includes other nonzero terms that couple states, such as
|gg0⟩ to |eg1⟩ and |gg0⟩ to |gg2⟩, but these leakage transitions can be neglected under the rotating-wave approximation
(RWA). The effective coupling strengths g̃0e,1g and g̃1e,0 f are
responsible for the MOVE and CZ gate dynamics, and from
hereafter we refer to them as g̃MOVE and g̃CZ , respectively.
We note that Eq. (C11) indicates that populating the |eg1⟩
state during the MOVE gate results in undesired population
transfer to the |gg2⟩ state that is outside of the computational
subspace. Furthermore, Eqs. (C11) and (C12) can be further
generalized. For n photons in the resonator, the effective
cou√
pling strengths
can
be
written
as
g̃
=
ng̃
and
(n−1)e,ng
0e,1g
√
g̃ne,(n−1) f = ng̃1e,0 f . As is the case in the Jaynes-Cummings
physics, coupling
strengths are seen to scale with the photon
√
number as n.
Utilizing Eq. (C12) and truncating the Hamiltonian
given in Eq. (C7) to a five-level subspace spanned by
{|gg0⟩, |eg0⟩, |gg1⟩, |eg1⟩, | f g0⟩}, we obtain analytical expressions for the population of the |eg1⟩ state and the acquired
conditional phase during the CZ gate operation. In doing so,
we assume that the leakage outside of the truncated subspace
is negligible, and that at the CZ gate operational point, i.e., at
ω̃q = ω̃r − αq , the single-excitation swapping g̃MOVE can be

neglected because |ω̃q − ω̃r | ≫ g̃MOVE . We obtain the effective time-evolution operator as Û = exp(−iH̃t ), where H̃ is
the truncated Hamiltonian in the coupler-dressed eigenbasis
and, by applying it to the initial |eg1⟩ state, we obtain that the
population in the state |eg1⟩ can be written as [90]
P|eg1⟩ (t ) = 1 −

2g̃2CZ
˜ )],
[1 − cos(t
˜2


(C13)

√
where ˜
= (˜
 − αq )2 + 4g̃2CZ and ˜
 = ω̃r − ω̃q . Equation (C13) suggests that during the CZ gate, the population
periodically returns to the |eg1⟩ state, exhibiting the Rabi
physics [91]. The conditional phase that the state |eg1⟩ picks
up during the CZ gate can also be analytically extracted and
is given as [90]
φ(t ) =

1
˜ + π (1 − sign{cos(t/2)})]
˜
[(αq − )t
2
(
)
˜
 − αq
+ arctan
tan( ˜
t/2) ,
(C14)
˜


where the first term composes a geometric phase, while the
latter is related to the dynamic phase. In the experiment,
˜ and 
˜ are tuned via the
the gate time τCZ is fixed, and 
amplitudes of the qubit and coupler flux pulses such that
φ(τCZ ) = π .
The analytical expression for the conditional phase
is an approximation valid near the resonance condition,
ω̃q ≈ ω̃r − αq , and describes the conditional phase acquired
when applying a nonadiabatic CPhase gate. To complement the discussion of the conditional phase, we present
a numerical simulation of the longitudinal ZZ-coupling
strength between a qubit and a computational resonator,
defined as
ζ = ω̃eg1 + ω̃gg0 − ω̃gg1 − ω̃eg0 .

(C15)

Including the lowest three energy levels and assuming dimensionless coupling strengths βqr = 0.001 97, βqc = 0.0219, and
βcr = 0.022 64, a resonator frequency ωr /(2π ) = 4.3 GHz, a
qubit anharmonicity αq /(2π ) = −0.187 GHz, and a coupler
anharmonicity αc /(2π ) = −0.11 GHz, we simulate the ZZ
coupling for a broad range of the bare qubit-resonator detuning,  = ωr − ωq , and the bare coupler frequency, ωc .
In contrast to the ZZ coupling between two qubits, the results shown in Fig. 10 exhibit distinct behavior depending
on the sign of the qubit-resonator detuning due to the vanishing anharmonicity of the resonator. The simulation results
demonstrate that ζ can reach several tens of megahertz and
also reveal the existence of an idling configuration, where the
ZZ coupling vanishes (see the white ellipse-shaped contour).
We note that the value of ζ determines the speed limit for a
fully adiabatic gate, while in this work we have employed the
nonadiabatic gate protocol.
Next, we investigate the residual transverse and longitudinal couplings between the computational resonator and the
spectator qubits during qubit-resonator gate operation. These
interactions are important to consider because they impact
spectator coherence times and spectator leakage. We perform
a numerical simulation using the chip-specific characteristics
and vary the frequency of the tunable coupler implementing

013148-13

## PDF page 14

MICHAEL RENGER et al.

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

qubit. The resulting ZZ couplings between the resonator and
the spectators are obtained by calculating the eigenvalues of
the same Hamiltonian as a function of the TC1 frequency. We
determine the effective transverse coupling g̃ [cf. Eq. (C10)]
between the central resonator and the qubits in a couplerhybridized basis. We plot the resulting transverse coupling
strength for the spectator qubits together with the coupling
strength between QB1 and the resonator in Fig. 11(a). Figure 11(b) shows the ZZ coupling between the spectator
qubits and the resonator. We find that the transverse coupling
between the resonator and the target qubit (QB1) strongly
depends on the coupler frequency, as desired for a tunable
coupling scheme. In contrast, the transverse coupling to the
spectators is below 1 MHz. Similarly, the spectator ZZ coupling remains almost constant and is on the order of a few
kilohertz.
FIG. 10. Longitudinal ZZ-coupling landscape as a function
of the bare coupler frequency, ωc , and the bare qubit-resonator
detuning, .

the qubit-resonator gate. In Fig. 11, we show the theory results
on the residual couplings to the five spectator qubits for a CZ
gate between QB1 and the computational resonator.
For the simulation of the ZZ coupling, the computational
states are chosen from the eigenstates of the idling Hamiltonian with the largest overlap with the uncoupled qubit states.
We calculate these eigenstates from the system Hamiltonian
with six qubits, six tunable couplers, and the resonator. The
idling configuration is chosen such that the overall ZZ coupling is minimized. During the CZ gate, QB1 is taken to a
frequency where its second excited state is in resonance with
the state where both QB1 and the resonator are excited. The
coupling between QB1 and the resonator is then achieved
by sweeping the corresponding tunable coupler closer to the

APPENDIX D: CALIBRATION AND BENCHMARKING

In the following, we describe the calibration procedure of
the qubit-resonator MOVE operation and the CZ gate, and
report on the basic characterization of the QPU.
1. Calibration of the MOVE operation

The initial calibration of the MOVE operation is presented
in the main text; therefore, only the fine calibration of the
operating point and the calibration of the single-qubit phase
correction of the MOVE operation are discussed here. The fine
calibration experiment for the MOVE operation individually
calibrates both the qubit and coupler flux pulse amplitudes by
making the MOVE insensitive to the relative phase of qubit
and resonator, which signals a complete population transfer.
As shown in the pulse schedule in Fig. 12(a), we first excite
the qubit using an Xπ gate and subsequently move this excitation to the computational resonator. We adjust the relative

FIG. 11. (a) Calculated effective transverse coupling g̃ between the CR and the spectator qubits during a CZ gate involving QB1 and the
CR. (b) Corresponding simulated ZZ coupling between the CR and the spectator qubits.
013148-14

## PDF page 15

SUPERCONDUCTING QUBIT-RESONATOR QUANTUM …

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

FIG. 12. Calibration of the MOVE operation. (a), (b) Pulse schedules used for the fine calibration of the MOVE operating point and the
calibration of the single-qubit phase correction of the MOVE, respectively. The schedules are described in detail in the text. (c) Experimental
data showing the fine calibration measurement to optimize the flux pulse amplitude of the qubit Z pulse, i.e., the diabatic qubit frequency ωQB
at the operation point of the MOVE. The optimal qubit frequency is visualized by the horizontal dashed line. (d) Experimental data for the
calibration of the VZ phase correction. The optimal phase is visualized by the vertical dashed line.

phase between qubit and resonator by applying a physical
Z rotation to the qubit by an angle ϕ. This is achieved by
applying the following pulse sequence to the qubit: a π /2
pulse around the y axis, followed by a rotation around the x
axis by an angle ϕ, and another π /2 pulse around the y axis
but rotating in the opposite direction. We repeat the sequence
consisting of the MOVE operation and the Z rotation N − 1
times and apply a final MOVE operation before measuring
the state of the qubit. The total number of moves N should be
chosen to be an even number, such that most of the population
is back in the qubit at the end of the experiment. If the MOVE
operation does not fully transfer the state, the excited-state
probability measured at the end of the sequence oscillates as
a function of the relative phase ϕ. This oscillation is due to
the quantum interference of the residual superposition state
of the qubit after the first MOVE with the part of the state
that has been moved to the computational resonator and back
to the qubit. The more MOVE operations are applied in the
fine calibration sequence, the more sensitive the resulting interference pattern is to a deviation from the optimal operating
point. Experimental data are depicted in Fig. 12(c) for a total
number of N = 4 MOVE operations. For the data shown, we
vary the amplitude of the qubit flux pulse and convert this
voltage into the qubit frequency using the measured qubit flux
dispersion. We take the average along the relative phase ϕ and
approximate the resulting data by a second-order polynomial
to obtain the optimal qubit frequency where the average qubit
excited-state probability is maximal. We perform a similar
measurement (not shown here) to optimize the amplitude of
the coupler flux pulse for fixed qubit flux pulse amplitude.

Next, we determine the optimal VZ phase for the MOVE
qubit, which corrects for the single-qubit phase that is accumulated depending on the frequency trajectory during the
MOVE operation. Since we cannot directly probe the phase
of a state in the computational resonator, we apply the MOVE
operation in pairs and thus calibrate the common phase [53],
i.e., the phase obtained when moving an excitation from the
qubit to the resonator and back. To achieve this, we consider
the pulse schedule shown in Fig. 12(b). First, an equal superposition state is prepared in the qubit by applying an X π2 pulse.
Next, we move this superposition state back and forth between the qubit and the resonator, amplifying the accumulated
single-qubit phase. Finally, we apply another X π2 pulse with
the rotation axis defined by ϕ in order to map the azimuthal
angle of the qubit state to an excited-state probability. If the
phase of the qubit state was not changed by the application of
the MOVE operations, we expect an excited-state probability
of 1, independent of N. In Fig. 12(d), we show experimental
data, where we vary the rotation axis of the second π /2 pulse,
ϕ, for an even number of MOVE operations. We average the
data along the number of MOVE operations to extract the
VZ phase correction. For demonstration purposes, we show
the phase landscape for up to 60 MOVE operations, while
for the benchmarking data we typically average over 2N =
2, 4, . . . , 10 MOVE operations only.
2. Calibration of the CZ Gate

The initial calibration of the CZ gate is presented in
the main text; therefore, only the fine optimization of the

013148-15

## PDF page 16

MICHAEL RENGER et al.

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

FIG. 13. Calibration of the CZ gate. (a), (b) Pulse schedules to calibrate the population exchange and conditional phase, respectively.
The flux pulses implementing the CZ gate to be calibrated are annotated with the measurement data figures, for which the respective pulse
amplitude is varied. (c), (d) Experimental data showing the population exchange and conditional phase measured as a function of both the qubit
and coupler frequencies realized during the gate operation by varying the respective flux pulse amplitudes. The blue dashed lines indicate the
sweep ranges used for the one-dimensional data shown in panels (e) and (f), respectively. The white markers represent the operating point of
the CZ gate inferred from the initial calibration discussed in the main text (cross) and the final calibration after several iterations of optimizing
the flux pulse parameters based on the measurement of the population exchange and the conditional phase (circle). (e) Experimental data
of the excited-state probability of the MOVE qubit vs the coupler frequency during the gate. We approximate the minimum in the excited-state
probability with a quadratic fit (black solid line) that is applied to a subset of the data points (blue solid circles) obtained by removing data
points from either side based on the R-squared value of the fit. (f) Experimental data of the conditional phase vs the qubit frequency during the
gate. The optimal operating point of the CZ gate is indicated by the black dashed lines in panels (e) and (f).

operating point, including the measurement of the conditional
phase and the population exchange, as well as the calibration of the single-qubit phase corrections of the CZ gate are
discussed here. We refine the calibration of the CZ gate by
iteratively optimizing the qubit and coupler flux pulse parameters based on the measurement of the conditional phase and
the population exchange, respectively. Typically, three cycles
of iteration are sufficient to converge to the optimal operating
point. We start by optimizing the coupler frequency during
the gate using the sequence shown in Fig. 13(a). To prepare
the |eg1⟩ state, we excite both the MOVE and CZ qubits
with a Xπ pulse and transfer the state of the MOVE qubit
to the computational resonator. Next, we initiate the |eg1⟩ →
| f g0⟩ → |eg1⟩ population oscillations by applying flux pulses
to the CZ qubit and the coupler connecting the CZ qubit and

the computational resonator. Finally, we move the population
of the computational resonator back to the MOVE qubit and
apply Xπ pulses to the MOVE and CZ qubits to de-excite them
to the ground state, assuming that the CZ gate performed a full
population oscillation. We extract the operating point of the
CZ gate from the minimum in the excited state probability of
the MOVE qubit. The excited-state probability of the CZ qubit
also reveals the population oscillations; however, in general
we obtain higher signal to noise for the MOVE qubit, as
the readout is optimized to distinguish the qubit states |g⟩
and |e⟩, whereas the CZ qubit oscillates between |g⟩ and | f ⟩.
When varying the flux pulse amplitudes of both the CZ qubit
and coupler pulses, we obtain the two-dimensional population
landscape shown in Fig. 13(c). We use the qubit and coupler
flux dispersions to express the flux pulse amplitudes in terms

013148-16

## PDF page 17

SUPERCONDUCTING QUBIT-RESONATOR QUANTUM …

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

FIG. 14. Calibration of the single-qubit phase corrections for the CZ gate. (a), (b) Pulse schedules to extract the single-qubit phase
corrections of the computational resonator and the CZ qubit, respectively. (c), (d) Experiment data of the excited-state probability of the
qubit with the Ramsey sequence corresponding to the circuits shown in panels (a) and (b). We vary the angle ϕ and the total number of
CZ gates N to obtain the optimal phase corrections. Since the additional contributions (VZMOVE , tCZ ) have been accounted for during the
execution of the experiment, the vertical black dashed lines directly represent the optimal VZ rotation angle.

of the respective component frequency during the gate. We
obtain the optimal coupler frequency by fitting the excitedstate probability of the MOVE qubit for a one-dimensional
subset of the data as shown in Fig. 13(e).
Next, we optimize the qubit frequency during the CZ gate
based on the measurement of the conditional phase. The pulse
schedule used for measuring the phase accumulation of the CZ
qubit depending on the state of the computational resonator is
shown in Fig. 13(b). The CZ qubit is prepared in a superposition state by applying an X π2 pulse to enable the measurement
of the phase accumulation. The state of the computational
resonator during the CZ gate depends on whether we apply the
initial Xπ pulse on the MOVE qubit before moving the qubit
state to the resonator. After the first MOVE operation, we
apply flux pulses to the CZ qubit and the coupler connecting
the CZ qubit and the computational resonator to implement
the CZ gate. Finally, we apply an additional π2 pulse on the CZ
qubit with rotation axis ϕ to map the azimuthal angle of the
qubit state to the Z basis, i.e., to an excited-state probability.
From the measurement of the excited-state probability versus
the angle ϕ, we determine the single-qubit phase accumulation of the CZ qubit for the two cases where the resonator is
in the ground state or the first excited state. Figure 13(d) shows
the measurement of the conditional phase when sweeping the
frequencies during gate operation of both the CZ qubit and
its tunable coupler. We obtain the optimal qubit frequency
during the CZ gate from a fit to a one-dimensional subset of
the data with fixed coupler frequency at the point where the
conditional phase is equal to π , as shown in Fig. 13(f).
Next, we discuss the calibration of the single-qubit phase
corrections of the CZ gate for both the computational resonator and the CZ qubit using the circuits shown in Figs. 14(a)
and 14(b), respectively. First, we prepare an equal superposition state in the target qubit by applying an X π2 pulse. The
target qubit can be either the MOVE qubit or the CZ qubit.
Before applying the CZ gate N times between the computational resonator and the CZ qubit, we move the population of

the MOVE qubit to the resonator. Finally, we apply another
MOVE operation followed by a X π2 pulse in order to map the
azimuthal angle of the qubit state to an excited-state probability. If the phase of the target qubit has not been changed
by applying the CZ gates, we expect the excited-state probability to be equal to 1. We note that we apply the MOVE
operations in the circuit shown in Fig. 14(b) even though there
is no population in the MOVE qubit, because the flux pulses
that implement a MOVE operation between the MOVE qubit
and the computational resonator can affect the single-qubit
phase accumulation of the CZ qubit due to flux crosstalk.
Experiment data of the calibration of the single-qubit phase
corrections for the CZ gate are shown in Figs. 14(c) and
14(d). If the CZ qubit is the target qubit, the phase accumulation that we measure originates purely from the frequency
change of the CZ qubit during the CZ gate (ignoring flux
crosstalk). However, if the MOVE qubit is the target qubit, the
total accumulated phase between the π2 pulses generally contains different contributions. To measure the pure single-qubit
phase accumulation of the computational resonator due to
the dynamic frequency tuning during the CZ gate, we ensure
that the previously calibrated VZ correction of the MOVE
operation, VZMOVE , is applied. Furthermore, we account for
the time-dependent phase due to the relative rotation of the
rotating frames of the MOVE qubit and the computational resonator by adding a phase NtCZ = (ωQB − ωCR )NtCZ , which
is proportional to the detuning of the MOVE qubit and the
resonator, as well as to the total time in between the MOVE
operations, NtCZ .
3. Characterization of the computational resonator

We characterize the frequency and coherence properties of
the computational resonator by employing the MOVE operation to (de)populate the resonator. The circuit to measure
the relaxation time is shown in Fig. 15(a): we excite one
of the qubits using an Xπ pulse. After moving the excitation

013148-17

## PDF page 18

MICHAEL RENGER et al.

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

µs

µs

µs

FIG. 15. Characterization of the computational resonator. (a), (b) Circuit and corresponding experiment data to determine the relaxation
time of the computational resonator T1 . (c), (d) Circuit and measurement data from which the dephasing time of the resonator T2∗ is determined.
(e) Experiment data with additional sweep over the virtual detuning  for the circuit shown in panel (c). (f) Fast Fourier transform of the qubit
excited-state probability vs delay time t shown in panel (e). We fit a sawtooth model to obtain the value of the virtual detuning corresponding to
the frequency difference of the qubit and the computational resonator. The sweep range of the detuning is centered around the initial estimate
for the qubit-resonator detuning obtained from a similar measurement but with much larger Nyquist frequency of approximately 250 MHz.
Therefore, the qubit-resonator detuning (indicated by the orange circle) is obtained as the value of the detuning  that is closest to the center
of the sweep range and where the Nyquist fit is equal to zero.

to the resonator, it will decay according to the resonator relaxation rate. After a variable delay time, we use a second
MOVE operation to move the state back and measure the
remaining population in the qubit. The data in Fig. 15(b) show
the exponential decay from which we extract the resonator relaxation time T1 = 5.53 ± 0.32 µs. Several factors contribute
to the small resonator relaxation time. Simulations suggest
that the close proximity of two qubit flux lines to the grounded
end of the computational resonator results in strong inductive
coupling and hence Purcell decay, limiting the resonator T1
time to 14.5 µs. Multiple other Purcell decay channels from
other flux and drive lines may further reduce T1 . The coupling
between the resonator and the control lines is mostly mediated
by the high-dielectric constant of the silicon substrate. Switching to a flip-chip architecture, where the control lines can be
on a different substrate, can strongly reduce this loss channel.
Furthermore, optimizing the coplanar waveguide geometry by
adjusting the width of the center conductor and the gap to the
grounding plane is expected to reduce the energy participation
ratio (EPR). In addition, the design of the tunable couplers
can be improved to further decrease the EPR. In this work,

waveguide extenders are incorporated in the coupling structure with large interdigitated capacitors on each side of the
tunable coupler. Removing the extender between the computational resonator and the tunable coupler may further reduce
the EPR. By addressing these design and fabrication aspects,
we are confident that improving the resonator relaxation time
by an order of magnitude is possible.
To measure the T2∗ coherence time of the resonator, we
employ Ramsey interferometry as shown in Fig. 15(c). This
measurement is based on a technique outlined in Ref. [92].
We prepare a superposition state in the MOVE qubit by applying an X π2 pulse and use the MOVE operation to transfer
the prepared state into the resonator. After a certain delay
time t, we use a subsequent MOVE operation to move the
superposition back to the qubit. Finally, we apply an X π2 (φ)
pulse with a rotation axis that forms an angle of φ with the X
axis. The excited-state probability of the qubit at the end of
the circuit oscillates at the difference frequency of the qubit
and the computational resonator, which can be quite large,
i.e., on the order of 100 MHz. We use a virtual detuning  to
advance the phase of the second π /2 pulse by φ = t to

013148-18

## PDF page 19

SUPERCONDUCTING QUBIT-RESONATOR QUANTUM …

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

TABLE II. QPU performance. If provided, the uncertainty corresponds to the empirical standard deviation measured over a 238 h period.
For the qubit/resonator frequency, the standard deviation is on the order of 10 kHz.
Parameter

Description

QB 1

QB 2

QB 3

QB 4

QB 5

QB 6

CR

f (GHz)
Transition frequency
4.67
4.47
4.41
4.52
4.63
4.93
4.22
Lifetime
25.6 ± 4.1
44.0 ± 5.3
55.3 ± 1.1
46.2 ± 9.0
45.9 ± 8.6 30.6 ± 5.6 5.53 ± 0.32
T1 (µs)
Dephasing time
36.5 ± 6.1
27.1 ± 3.4
29.0 ± 4.3
22.2 ± 2.0
51.5 ± 9.9 31.9 ± 8.2 10.9 ± 1.0
T2∗ (µs)
Hahn echo dephasing time
44.2 ± 7.1
56.0 ± 5.5
42.3 ± 4.5
29.9 ± 2.2
58.6 ± 8.8 43.8 ± 8.1
T2e (µs)
Effective qubit temperature
46.3
42.0
43.6
40.9
43.0
45.8
Tq (mK)
14.8
13.8
13.3
13.9
14.6
16.5
EJ /h (GHz) Josephson energy
Energy ratio
74.2
68.8
66.5
69.6
73.0
82.3
EJ /EC
Simultaneous readout fidelity 98.3 ± 0.3
98.6 ± 0.2
98.7 ± 0.3
99.1 ± 0.2
98.9 ± 0.2 98.7 ± 0.6
FRO (%)
99.93 ± 0.02 99.94 ± 0.04 99.96 ± 0.02 99.96 ± 0.01 99.96 ± 0.01 99.89 ± 0.3
Fsq,ind (%) Individual SQG fidelity
99.93 ± 0.02 99.92 ± 0.04 99.96 ± 0.03 99.95 ± 0.01 99.59 ± 0.01 99.87 ± 0.3
Fsq,sim (%) Simultaneous SQG fidelity

effectively slow down the oscillations in the excited-state
probability of the qubit, such that the observed oscillation
frequency ω = ωQB − ωCR −  is comparable to the inverse
of the T2∗ time. Both the oscillation frequency ω and the dephasing time T2∗ are extracted from an exponentially decaying
sinusoidal fit. The measurement data in Fig. 15(d) show the
Ramsey fringes from which we extract T2∗ = 10.9 ± 1.0 µs.
By additionally sweeping the virtual detuning as shown in
Fig. 15(e), we can measure the eigenfrequency of the computational resonator. The excited-state probability of the qubit
versus the delay time is Fourier transformed via FFT. In
Fig. 15(f), we show the extracted dominant frequency component versus the virtual detuning. We fit a sawtooth model
to extract the value of the detuning, which corresponds to the
detuning of the qubit and the computational resonator, i.e.,
 = ωQB − ωCR .
4. QPU characterization

We summarize the QPU characterization and single-qubit
benchmarking data in Table II. The data for the coherence
times, readout fidelity, and single-qubit gate fidelity have been
taken over a time frame of 238 h. The statistics consist of
208 data points for the coherence times, 210 data points for
the readout fidelity, and 49 data points for the single-qubit
gate fidelities, which have been characterized individually
and simultaneously on all qubits. In between the individual
benchmarking measurements, the QPU has been recalibrated
by an automatic service. The Josephson energy EJ has been
determined by fitting the coupler flux dispersion. The energy
ratio EJ /EC is determined by using the design parameters
for the charging energy EC . The individual gate fidelities
for the MOVE operation and for the CZ gate are shown in
Table III. The error bars are determined from the corresponding fit errors by error propagation. We implement single-qubit
gates using the derivative removal by adiabatic gate method
with a cosine shaped envelope of the in-phase component

[47]. For the MOVE operation and for the CZ gate, we use
cosine flux pulses on the qubits and square pulses smoothed
by truncated Gaussian ramps for the tunable couplers. The
respective gate durations, including buffer time to account for
residual flux pulse distortions affecting the performance of the
qubit-resonator operations, are summarized in Table IV.
APPENDIX E: COHERENCE LIMIT

To estimate the coherence limit Fczc for the MOVE operation and for the CZ gate, we employ the weak dissipation
result F c , valid at absolute zero, from Ref. [60]:
Fc = 1 −

N
∑
( (k)
)
dτ
γ1 + γϕ(k) .
2(d + 1) k=1

(E1)

Here, N is the number of involved components, d is the
Hilbert space dimension, τ the gate duration, and γ1k (γϕ(k) )
is the energy relaxation (dephasing) rate for component k.
Equation (E1) is valid as long as we do not leave the computational subspace during the operation. Furthermore, Eq. (E1)
contains the implicit assumption that dephasing is caused by
a white noise spectrum. In case of additional low frequency
noise with 1/ f noise spectral density, Eq. (E1) would contain
an additional quadratic contribution for the dephasing rate. In
the parking configuration, we verify that we are dominated
by white noise since the envelope of the Ramsey oscillations
is exponential and not Gaussian. We thus only consider the
linear white noise contributions, although the contribution of
Gaussian noise is expected to be significant during the gate
operation due to the flux pulse, detuning the qubit away from
the flux-insensitive parking configuration. In addition, we also
neglect hybridization effects during the gate; thus, we obtain
an upper bound for the coherence limit.
To apply Eq. (E1) for a single MOVE operation with a
duration τm , we treat it as an effective single-qubit gate and
simplify the calculation by assuming that the decoherence is

TABLE III. Individual double MOVE and CZ fidelities.
Parameter

Description

Fmm (%)
Fcz (%)

Double MOVE fidelity
CZ fidelity

QB 1

QB 2

QB 3

QB 4

QB 5

QB 6

99.11 ± 0.05
98.90 ± 0.05

99.34 ± 0.03
98.75 ± 0.04

99.00 ± 0.03
98.97 ± 0.03

99.30 ± 0.03
98.04 ± 0.08

98.31 ± 0.06
98.53 ± 0.14

97.95 ± 0.10
96.61 ± 0.05

013148-19

## PDF page 20

MICHAEL RENGER et al.

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

TABLE IV. Duration of single-qubit gates, multiplexed readout, and qubit-resonator operations.
Parameter

Description

QB 1

QB 2

QB 3

QB 4

QB 5

QB 6

τs (ns)
τro (ns)
τm (ns)
τcz (ns)

Single-qubit gate duration
Readout pulse duration
MOVE operation duration
CZ gate duration

40
800
88
96

40
800
80
80

40
800
96
80

40
800
80
112

40
800
96
96

40
800
96
80

caused only by the qubit for the first half of the gate, and only
by the computational resonator for the second half, thus
)
τm ( q
γ + γ1r + γϕq + γϕr ,
Fmc = 1 −
6 1
where the superscript q (r) refers to the MOVE qubit (computational resonator). The coherence limit of the double MOVE
c
= (Fmc )2 . During the CZ gate, we leave
operation satisfies Fmm
the computational space and apply the formula from Ref. [61]:
3
61
29
τcz γ1r − 80
τcz γϕq − 80
τcz γϕr ,
Fczc = 1 − 21 τcz γ1q − 10

(E2)

where τcz is the CZ gate time. In the presence of a thermal
qubit (resonator) population of nq (nr ) photons, the coherence
limits reduce further according to
Fmc → Fmc − 13 τm γ1q nq − 13 τm γ1r nr ,
Fczc → Fczc − 95 τcz γ1q nq − 75 τcz γ1r nr .

(E3)

The qubit and resonator decay rates are given in Table II, and
the gate durations of both MOVE and CZ in Table IV. We
neglect thermal effects since we operate the QPU in the saturation regime of Planck statistics, i.e., for qubit temperatures
below 50 mK [93,94].
We can also estimate the effect of decoherence on the
GHZ state preparation. For this, we consider the transpiled
circuit we employ for N-qubit GHZ state generation shown in
Fig. 4(a), which can be schematically written as
π + X .
CZ + MOVE
Y π2 + MOVE
π
⏟ ⏞⏞ ⏟ + ⏟⏞⏞⏟
⏟ ⏞⏞ ⏟ + Y
⏟⏞⏞⏟
⏟ 2 ⏞⏞ ⏟
(2)
(3)
(4)

(1)

Step (1) corresponds to a π /2 rotation about the y axis, which
is applied to all N qubits. In step (2), we employ a MOVE
operation between a dedicated MOVE qubit and the computational resonator. Step (3) corresponds to a cascade of (N − 1)
CZ operations, followed by a MOVE operation in step (4) that
transfers the state of the resonator back to the MOVE qubit.
Finally, we apply a π /2 rotation about the y axis and a π
rotation about the x axis to each of the CZ qubits. In case
Fi corresponds to the coherence-limited fidelity of step (i),
we approximate the coherence limit of the entire circuit by
assuming
(E5)

In the following, we assume that qubit l is used as the MOVE
qubit. The individual fidelity contributions are estimated by
∏ (k)
∏
Fs(k) ,
F2 = F4 = Fm(l )
Fi,m ,
F1 =
k

F3 =

∏
k̸=l

( (k) )N−2
Fcz(k) Fi,cz
,

k̸=l

∏(
)2 (
)2
Fs(k) Fi,s(l ) . (E6)
F5 =
k̸=l

Here, Fm(l ) corresponds to the MOVE operation coherence
(k)
limit and Fi,m
corresponds to the fidelity limit for qubit k,
which idles during the MOVE operation. The quantity Fcz(k)
corresponds to the fidelity limit for the CZ gate between the
(k)
computational resonator and qubit k and Fi,cz
denotes the
idling fidelity of qubit k during the CZ gates with other qubits.
The exponent N − 2 in F3 results from the fact that there is
one CZ gate per qubit applied and each qubit idles during the
remaining (N − 2) CZ gates. Finally, Fi,s(l ) is the idling fidelity
limit for the MOVE qubit during the final two single-qubit
gates. For simplicity, we dropped the superscript c for the
coherence limits. We exploit the fact that the coherence limit
is in first order independent of the applied gate. Therefore,
we approximate the idling fidelities by the measured single(k)
qubit gate fidelities. Thus, Fi,s = Fs and Fi,s(l ) as well as Fi,cz
are treated like an effective single-qubit gate with the same
gate time as the respective qubit-resonator operation. As a
consequence, Eq. (E5) can be expressed as
(
)2 ∏ ( (k) )3 ( (k) )2 ( (k) )N−2 (k)
Fcz .
Fs
Fi,m Fi,cz
FGHZ = (Fm(l ) )2 Fs(l ) Fi,s(l )
k̸=l

(E8)

(E4)

(5)

FGHZ = F1 F2 F3 F4 F5 .

Here, Fs(k) denotes the single-qubit gate fidelity coherence
limit for qubit k, given by [60]
) 2
τs ( (k)
γ1 + γϕ(k) − nq(k) γ1(k) τs .
Fs(k) = 1 −
(E7)
3
3

As a consistency check, we employ Eq. (E8) for the measured simultaneous single-qubit gate fidelities from Table II
and the two-qubit gate fidelities from Table III. Idling infidelities are modeled via Eq. (E7) using the QPU parameters
from Table II and the gate durations from Table IV. In our
particular case, we have employed QB3 as the MOVE qubit
while the CZ cascade has been applied to all remaining qubits.
We estimate FGHZ ≃ 0.85, which is close to the measured
GHZ fidelity of 0.86, thereby demonstrating consistency of
our model. Next, we use Eq. (E7) to estimate the coherence
limit of the GHZ fidelity. As for the coherence limit estimation
for the individual gates, hybridization effects with tunable
couplers are neglected. However, we take the finite temperature into account this time, since even for a qubit temperature
of 40 mK, finite temperature effects accumulate due to the
large amount of gates in the circuit. Since we cannot directly
measure the temperature of the computational resonator, we
perform a work case estimation and assume its temperature
to coincide with the hottest qubit in Table II, Tr = 46.3 mK.
For the six-qubit GHZ state, we then find a fidelity limit of
FGHZ ≃ 0.910. After multiplying with the readout fidelities,
this limit reduces to 0.842. As a comparison, we measured
a GHZ fidelity of 0.815 without REM and 0.860 with REM.

013148-20

## PDF page 21

SUPERCONDUCTING QUBIT-RESONATOR QUANTUM …

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

Although the model [Eq. (E8)] is relatively simple, we conclude that the main effect of GHZ infidelity results from
decoherence.
We particularly observe that the resonator lifetime is significantly shorter than the lifetime of the qubits. Since the
resonator is involved in all qubit-resonator operations, this
low lifetime is expected to set a dominant limitation on the
GHZ state fidelity. For that, we employ the approximation
that the qubits and the computational resonator are T1 limited
and drop all dephasing terms (for the resonator, this is a very
accurate assumption). Simultaneously, we assume that the
qubit-resonator operations add significantly more infidelity
than the single-qubit gates, implying that we treat all singlequbit gates as ideal. We furthermore assume a temperature of
absolute zero and, for simplicity, equal duration τ of CZ gate
(k)
(k)
and MOVE operation, implying Fi,m
= Fi,cz
. With these rough
approximations, we have
FGHZ ≃

∏ ( (k) )N
Fi,cz Fcz(k)
k̸=l

=

∏(

1−

k̸=l

APPENDIX F: JAYNES-CUMMINGS GATE
1. Time evolution in the rotating frame

Let us consider here the dynamics of a quantum state
|ψ⟩, governed by the time-dependent Hamiltonian Ĥ (t ) =
Ĥ0 + V̂ (t ). Here, we have separated the full Hamiltonian into
a time-independent part Ĥ0 , and into an interaction part V̂ (t )
that can be time dependent. In general, Ĥ0 and V̂ (t ) do not
commute.
We define a change in the rotating frame by a unitary operator, and here we choose R̂(t ) = eiĤ0 t/h̄ , which transforms the
state vector as follows: |ψ⟩′ = R̂(t ) |ψ⟩. The time evolution
in the rotating frame is given by the (modified) Schrödinger
equation:
i h̄∂t |ψ⟩′ = R̂(t )V̂ R̂† (t ) |ψ⟩′ .
⏟ ⏞⏞ ⏟

(F1)

Ĥ ′

The unitary time evolution operators in the two frames are
related according to

(
)
τ
τ (k) )N
3
1 − γ1(k) − γ1r .
γ1
3
2
10

Û ′ (t, t0 ) = R̂(t )Û (t, t0 )R̂† (t0 ).

(E9)

(F2)

2. Derivation of the time evolution of the Jaynes-Cummings gate

In the limit N ≫ 1, γ1(k) τ ≪ 1, and γ1r τ ≪ 1, we can further

approximate by

FGHZ ≃

∏

τ

∏

(k)

e−N 3 γ1

k̸=l

= e−τ (

τ

(k)

e− 2 γ1 − 10 γ1
3τ

r

k̸=l
N
1
3 +2

)

∑

(k)
k̸=l γ1

e−(N−1) 10 γ1 ,
3τ

r

Qubit decay

(E11)

qubits. By comparing the decay constants, the constraint that
the resonator lifetime limits the GHZ fidelity is then given by
(

= h̄ωr â† â + h̄ωq

)
5 q
10N
+
γ̄ .
9
3 1

(E12)

For our six-qubit QPU, this implies γ1r ≫ 8.3γ̄1q . For our
QPU, we have γ1r ≃ 6.7γ̄1q , implying that this condition is not
met. As such, the decoherence of the computational resonator
is expected to have a significant effect on the GHZ coherence
limit, but the dominating error contribution is the depolarization of the qubits during idling gates. In fact, setting γ1r = 0 in
Eq. (E8) raises FGHZ from 0.842 to 0.867 (taking finite readout
fidelity into account). Equation (E12) also implies that for
N ≫ 1, it can be beneficial to use the qubit with the lowest
lifetime as MOVE qubit since during the long CZ cascade, it
always idles in the ground state and does not contribute to γ̄1q .

h̄ +
σ̂z
+
(σ̂ + σ̂ − )(â + â† ).
2
2

(F3)

Using Eq. (F1), we can transform the Hamiltonian from the
Schrödinger picture (lab frame) to the interaction picture
(computational frame), which is defined by the choice of
rotating frame, Ĥ0 = Ĥresonator + Ĥqubit ,

Resonator decay

where γ̄1q is the mean energy decay rate of the involved CZ

γ1r ≫

Ĥ = Ĥresonator + Ĥqubit + Ĥinteraction

(E10)

where we use an exponential approximation, analogous as has
been used for the derivation of the Porter-Thomas distribution
in Ref. [95]. With this approximation, FGHZ decouples into a
qubit and a resonator decay term:
q
N
1
3τ r
2 ) (N−1)γ̄1 × e−(N−1) 10 γ1 ,
FGHZ ≃ ⏟e−τ ( 3 +⏞⏞
⏟ ⏟ ⏞⏞ ⏟

The Rabi Hamiltonian describes the time evolution of a
two-level system, i.e., a qubit, interacting with a bosonic
mode, here called a computational resonator. In the laboratory
frame and ignoring the zero-point energy of the computational
resonator, the Hamiltonian is given by

Ĥcomp =

h̄ iĤ0 t/h̄
e
(âσ̂ − + â† σ̂ + + âσ̂ + + â† σ̂ − )e−iĤ0 t/h̄ .
2
(F4)

Using
the
Baker-Campbell-Hausdorff
lemma
(eX Ye−X = Y + [X, Y ] + 1/2![X, [X, Y ]] + · · · +
1/n![X, [X, · · · [X, Y ] · · · ]]) and the commutation relations
[â† â, â] = −â, [â† â, â† ] = â† , and [σ̂z , σ̂ ± ] = ±2σ̂ ± , we
have
Ĥcomp =

h̄
(âσ̂ − e−i(ωr +ωq )t + â† σ̂ + ei(ωr +ωq )t
2
+ âσ̂ + e−i(ωr −ωq )t + â† σ̂ − ei(ωr −ωq )t ).

(F5)

According to the RWA, the two quickly oscillating terms may
be ignored. In this case, we end up with the Jaynes-Cummings
Hamiltonian in the interaction picture:

013148-21

Ĥ = Ĥ0 +

h̄ † −
(â σ̂ + âσ̂ + ).
2

(F6)

## PDF page 22

MICHAEL RENGER et al.

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

According to the Jaynes-Cummings Hamiltonian in Eq. (F6),
where non-excitation-conserving transitions have been
dropped by applying the RWA, we only have to consider
excitation-conserving transitions between the qubit-resonator
states |r, q⟩:
|n, g⟩ ↔ |n − 1, e⟩ ,

interaction term in the Hamiltonian:
[Ĥint , N̂] =

(F7)

=

where n is the total number of excitations of the
qubit-resonator state and the eigenvalue of the operator
N̂ = |e⟩ ⟨e| + â† â. This operator commutes with the
⎡

1

⎢
⎢0
⎢
⎢0
⎢
Ĥ = ⎢ ..
⎢.
⎢.
⎢ ..
⎣
..
.

0

···
...

···
...

0
...

...

...

0
...

Ĥn
...

0
...

0

0

Ĥ1

0

0
...
...

Ĥ2
...
...

...

h̄ † −
(â σ̂ − â† σ̂ − − âσ̂ + + âσ̂ + ) = 0.
2

(F8)

Using the eigenstates of N̂ as a basis, the Hamiltonian can
be represented by a block-diagonal matrix:

0

...

h̄ † −
(â [σ̂ , |e⟩ ⟨e|] + [â† , â† â]σ̂ −
2
+ â[σ̂ + , |e⟩ ⟨e|] + [â, â† â]σ̂ + )

...

...

⎤
···
. . .⎥
⎥
. . .⎥
⎥
⎥
.
. . .⎥
⎥
⎥
. . .⎥
⎦
...

(F9)

The (2 × 2) matrices representing the manifolds with equal number of excitations n, are given by
(
)
√
(
)
ω
 n
ωr (n − √1) + 2q
⟨n − 1, e|Ĥ |n − 1, e⟩ ⟨n − 1, e|Ĥ |n, g⟩
2
= h̄
.
Ĥn =
ω
 n
⟨n, g|Ĥ |n − 1, e⟩
⟨n, g|Ĥ |n, g⟩
nω
− 2q
r
2

(F10)

When reintroducing the zero-point energy of the computational resonator (+Iˆh̄ωr /2) in Ĥn and defining  = ωr − ωq , we can
rewrite the elements in the block-diagonal matrix as
(
)
√
√
 n
h̄
h̄ n
nωr √− 2
2
ˆ
Ĥn = h̄
σ̂
σ̂x .
I
−
+
(F11)
=
n
h̄ω
r
z
 n
2
2
nωr + 2
2
The time evolution in the laboratory frame can be calculated by the propagator
⎛ (
⎞
√
)
·sin ( 21 (,n)t )
 n·sin ( 21 (,n)t )
1
cos
(,
n)t
+
i
−i
2
(,n)
(,n)
⎠.
√
Un,lab (t, 0) = e−iĤn t/h̄ = e−inωr t ⎝
(1
)
 n·sin ( 21 (,n)t )
·sin ( 21 (,n)t )
−i
cos
(,
n)t
−
i
(,n)
2
(,n)
Here, we have defined the photon number and detuning-dependent generalized Rabi frequency (, n) =
characterizes the effective coupling between the states |n − 1, e⟩ and |n, g⟩.

√

(F12)

2 + n2 , which

a. Free time evolution

√
When the detuning between the √
qubit and the computational resonator is much larger than the Rabi frequency ( n/ ≪ 1),
we can approximate (, n) =  1 + n2 /2 ≈ . In this case, the unitary operator simplifies to the free time evolution:
( 
)
i2t
√
e
0
Un,lab ( n/ ≪ 1) ≃ e−inωr t
.
(F13)

0
e−i 2 t
b. Resonant population exchange

To obtain a full population exchange between the states |n − 1, e⟩ and |n, g⟩, the qubit and computational resonator have to
be on resonance, i.e.,  = 0 during the MOVE operation. Therefore, the time evolution in the laboratory frame simplifies to
(
( √
)
( √
))
cos 21 nt
−isin 21 nt
−inωg t
Un,lab ( = 0) = e
(F14)
)
( √
) ,
( √
cos 21 nt
−isin 21 nt
where ωg is the gate frequency, meaning the frequency of both the qubit and the computational resonator during the JaynesCummings gate. The Jaynes-Cummings gate is calibrated to achieve a full population exchange in the single-excitation manifold,
n = 1. Assuming that  is constant during the gate, i.e., square flux pulse applied to the tunable coupler, the gate time follows as
t = π /. By transforming from the laboratory frame to a rotating frame where both the qubit and the computational resonator
013148-22

## PDF page 23

SUPERCONDUCTING QUBIT-RESONATOR QUANTUM …

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

ˆ

are oscillating at ωg (gate frame), i.e., R̂g = einωg t I , the time evolution for the lowest four excitation manifolds simplifies to
|0, g⟩|0, e⟩|1, g⟩

|1, e⟩

|2, g⟩

|2, e⟩

|3, g⟩

|3, e⟩|4, g⟩

⎡ 1 0 0
0
0
0
0
0 0 ⎤
0
0
0
0
0 0 ⎥
⎢ 0 0 −i
⎢ 0 −i 0
0√
0√
0
0
0 0 ⎥
⎥
⎢
( 2 )
( 2 )
⎥
⎢
0
0
0 0 ⎥
⎢ 0 0 0 cos 2 π −i sin 2 π
√
√
⎥
⎢
)
(
)
(
⎢ 0 0 0 −i sin 2 π cos 2 π
0
0
0 0 ⎥
.
⎥
⎢
2
2
( √3 )
( √3 )
⎥
⎢
⎢ 0 0 0
0
0
cos 2 π −i sin 2 π 0 0 ⎥
⎥
⎢
(√ )
(√ )
⎥
⎢
0 0 ⎥
0
0
−i sin 23 π cos 23 π
⎢ 0 0 0
⎦
⎣
0 0 0
0
0
0
0
−1 0
0 0 0
0
0
0
0
0 −1

(F15)

In most cases, the rotating frame of choice is the so-called computational frame, where the free time evolution of all components
is effectively fully compensated by the rotating frame, which means that the unitary transformation going from laboratory to the
computational frame is constructed using Ĥ0 = nh̄ωr Iˆ − h̄
σ̂ :
2 z




R̂lab→comp = ei (nωr I− 2 σ̂z )t = einωr t I e−i 2 t σ̂z .
ˆ

ˆ

The Hamiltonian in the computational frame follows from Eq. (F1):
√
√ (
h̄ n −i  t σ̂z i  t σ̂z
h̄ n 0
†
Ĥn,comp = R̂lab→compV̂ R̂lab→comp =
e 2 σ̂x e 2 =
eit
2
2

(F16)
)
e−it
.
0

(F17)

The time evolution in the computational frame can be calculated using Eqs. (F2), (F14), and (F16):
†
Un,comp (t, t0 ) = R̂lab→compUn,lab (t, t0 )R̂lab→comp
( 
(√
)
−i 2 (t−t0 )
cos 2n (t − t0 )
in(ωr −ωg )(t−t0 ) e
=e
(√
)
t+t0
−iei 2 sin 2n (t − t0 )

(√
))
t+t0
−ie−i 2 sin 2n (t − t0 )
(√
) .

ei 2 (t−t0 ) cos 2n (t − t0 )

(F18)

In the computational frame, we see that the frame tracking needs to take into account all the times when a Jaynes-Cummings gate
is applied. Assuming the Jaynes-Cummings gate to be instantaneous (t = t0 ) and calibrated to obtain a full population exchange
in the one-excitation manifold, the time evolution operator simplifies to
⎛
(√ )
( √ )⎞
cos 2nπ
−ie−it sin 2nπ
⎠.
Un,comp (t = t0 , t0 ) = ⎝
(F19)
(√ )
(√ )
−ieit sin 2nπ
cos 2nπ
3. Populated-resonator Ramsey experiment

Next, we derive the time evolution for the populated Ramsey experiment, demonstrated in the main text, for arbitrary
excitations. We change to obtained when changing to the reference frame defined by Ĥref = h̄ωq (â† â + σ̂2z ). As we will see
below, in this frame the time evolution adds phase factors proportional to the detuning  and the number of excitations in the
resonator. Therefore, when sweeping the wait time, we will observe two frequency components in the excited-state probability
of the second move qubit, one at f1 =  and another one at f2 = 2, corresponding to one and two photons in the resonator,
respectively. To transform the Hamiltonian into this frame, we use the unitary
( iω t
)
† ˆ σ̂z
e q
0
ˆ ωq
R̂1 = eiωq t (a aI+ 2 ) = einωq t I ei 2 t σ̂z = einωq t
,
(F20)
0
1
where we drop global phase terms. The second exponential adds an excitation-dependent phase to the corresponding state,
while the matrix adds a qubit-state dependent phase. Using the considered reference frame Hamiltonian, the Jaynes-Cummings
Hamiltonian can be rewritten as
h̄ † −
σ̂z
Ĥ = h̄ωr â† â + h̄ωq +
(â σ̂ + âσ̂ + )
2
2
σ̂z
h̄ † −
(â σ̂ + âσ̂ + )
= h̄ωq â† â + h̄ωq + h̄(ωr − ωq )â† â +
2
2
h̄ † −
(â σ̂ + âσ̂ + ).
(F21)
= Ĥref + h̄â† â +
2
013148-23

## PDF page 24

MICHAEL RENGER et al.

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

By applying Eq. (F20), the interaction Hamiltonian becomes

√
h̄
h̄ n
Ĥint =
σ̂z +
[cos(ωq t )σ̂x − sin(ωq t )σ̂y ].
(F22)
2
2
We invoked the matrix representation of the Hamiltonian for a given excitation manifold n and neglect the constant offset term
that does not contribute to the dynamics of the system. The unitary operator in this frame becomes
h̄nIˆ −

−i

e−iĤint t/h̄ = e−itn e
⎛

)
√ (
eff t  n

2 ( eff cos(ωq t )σ̂x −sin(ωq t )σ̂y )− eff σ̂z

( eff t )
( eff t ) 
cos
+
i
·
sin
2
2
eff
= e−itn ⎝
( eff t ) √n −iω t
q
−i · sin 2 eff e

where we define eff =

⎞
) √
(
−i · sin 2eff t effn eiωq t
)
(
) ⎠,
(
cos 2eff t − i · sin 2eff t eff

√
2 + n2 . For free evolution when  → 0, we get
( 
) (
it
0
e−it (n−1)
−iĤint t/h̄
−itn e 2
e
= e
=

0
0
e−it 2

)
,
e−itn
0

(F23)

(F24)

where we neglect global phase factors. Considering the following bare eigenstates, their free time evolution becomes
|0, e⟩ → 1,

|1, e⟩ → e−it ,

|2, g⟩ → e−it2 .

(F25)

The state evolution with the first qubit and computational resonator right after the MOVE derived from the circuit can now be
written as
|0, g⟩ → −i |0, e⟩ → − |1, g⟩ .

(F26)

Since√ −1 is a global phase,
we can neglect it. In the following, we use the previously introduced shorthand notation c2 =
√
cos( 22π ) and s2 = sin( 22π ). In the subsequent part of the circuit up to the second MOVE, the second qubit and computational
resonator state becomes
|1, g⟩ − i |1, e⟩
−i
1
|1, g⟩ →
(F27)
→ √ (−i |0, e⟩ − i(c2 |1, e⟩ − is2 |2, g⟩)) = √ (|0, e⟩ + c2 |1, e⟩ − is2 |2, g⟩).
√
2
2
2
In the reference frame, when the qubit and resonator are far detuned and the interaction term is considered to be negligible, we
see from Eq. (F25) that the free time evolution of the state becomes
1
e−iĤt/h̄ |ψ⟩ = √ (|0, e⟩ + c2 |1, e⟩ e−it − i · s2 |2, g⟩ e−it2 ).
2

(F28)

After the second MOVE gate, we have
−i
√ ( |1, g⟩ + i |1, e⟩ ((c2 )2 e−it − (s2 )2 e−it2 ) + |2, g⟩ c2 s2 (e−it + e−it2 )).
2

(F29)

After the final π2 pulse, we obtain the state
1
(|1, g⟩ (1 + (c2 )2 e−it − (s2 )2 e−it2 ) − i |1, e⟩ (1 − (c2 )2 e−it + (s2 )2 e−it2 )
2

(F30)

+ |2, g⟩ c2 s2 (e−it + e−it2 ) − i |2, e⟩ c2 s2 (e−it + e−it2 )).

(F31)

The final probabilities of the qubit being in the excited state can be written as
Pe =

∞
∑

| ⟨n, e|ψ⟩ |2 = ⟨ψ|1, e⟩ ⟨1, e|ψ⟩ + ⟨ψ|2, e⟩ ⟨2, e|ψ⟩ .

(F32)

n=0

The last equality follows from the fact that we only consider the first and the second excitation manifold. These terms are
P1e = | ⟨ψ|1, e⟩ |2 = 41 [1 − 2(c2 )2 cos(t) + 2(s2 )2 cos(t2) − 2(c2 )2 (s2 )2 cos(t) + (c2 )4 + (c2 )4 ],
(c2 s2 )2
(1 + cos(t)).
2
Taking the sum of these equations, the full qubit excitation becomes
(
)
Pe = 21 1 − c22 cos(t ) + s22 cos(2t ) .
P2e = | ⟨ψ|2, e⟩ |2 =

013148-24

(F33)
(F34)

(F35)

## PDF page 25

SUPERCONDUCTING QUBIT-RESONATOR QUANTUM …

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

As an outlook, we generalize the populated Ramsey experiment to arbitrary resonator states. For simplicity, we assume ideal JC
interaction without any additional phase shifts here; the calculation for the imperfect JC interaction is analogous but requires a
bit more book keeping. We assume the initial state
∑
|ψ⟩ =
αn |g, n⟩.
(F36)
n

Applying the first π /2 pulse, followed by the first MOVE gate in the Ramsey sequence leads to
1 ∑
αn {cn |g, n⟩ − isn |e, n − 1⟩ − icn+1 |e, n⟩ − sn+1 |g, n + 1⟩}.
|ψ⟩ = √
2 n

(F37)

Subsequent time evolution in the laboratory frame is
|g, n⟩ → |g, n⟩einωr t ,

|e, n⟩ → |g, n⟩einωr t+iωq t .

After the final MOVE gate, the state can be written as
1 ∑
|ψ⟩ = √
αn {βn |g, n⟩ + γn |e, n⟩ + λn |e, n − 1⟩ + κn |g, n + 1⟩},
2 n

(F38)

(F39)

where
]
[ 2 inωr t+iωq
2
γn ≡ −i cn+1
e
− sn+1
ei(n+1)ωr t ,

βn ≡ cn2 einωr t − sn2 ei(n−1)ωr t+iωq t ,
λn ≡ −icn sn [ei(n−1)ωr t+iωq t + einωr t ],

κn ≡ −cn+1 sn+1 [einωr t+iωq t + ei(n+1)ωr t ].

The final state contributions with the qubit in the excited state are
1∑
⟨e|ψ⟩ =
αn {(γn − iβn )|n⟩ + λn |n − 1⟩ + κn |n + 1⟩}.
2 n

(F40)
(F41)

(F42)

Thus, the excited-state probability is
Pe =

1∑
|αn |2 {|γn − iβn |2 + |λn |2 + |κn |2 }.
4 n

(F43)

The individual probabilities can be expressed as
4
4
2
2
+ sn+1
− 2cn+1
sn+1
cos((ωr − ωr )t )
|γn − iβn |2 = cn4 + sn4 + cn+1
2
2
2
+2cn2 cn+1
cos(ωq t ) − 2cn+1
sn2 cos(ωr t ) − 2cn2 sn+1
cos(ωr t )
2
−2ss2 sn+1
cos((2ωr − ωq )t ) − 2cn2 sn2 cos((ωr − ωq )t ),

|λn |2 ≡ 2cn2 sn2 [1 + cos((ωr − ωq )t )],

2
2
|κn |2 ≡ 2cn+1
sn+1
[1 + cos((ωr − ωq )t )].

(F44)

Note that just as for the two-photon case, there are only second harmonic contributions 2ωr from the resonator. The reason is the
equidistant spacing of the harmonic oscillator combined with the 2 × 2 block-diagonal matrix structure of the JC Hamiltonian,
implying that all rotating contributions spaced apart further than 2ωr act as a global phase for the respective state probabilities
and thus drop out. The final result in the laboratory frame is given by
{
)
( 2 2
}
1∑
2
2
Pe =
cos(ωr t ) + sn2 sn+1
|αn |2 1 + cn2 sn2 cos(ωq t ) − cn+1
sn + cn2 sn+1
cos((2ωr − ωq )t ) .
(F45)
2 n
And the detected probability (assuming virtual detuning  = 0) is
( 2 2
}
{
)
1∑
2
2
|αn |2 1 + cn2 sn2 − cn+1
sn + cn2 sn+1
cos(2t ) .
cos(t ) + sn2 sn+1
Pe =
2 n

(F46)

In the case n = 0, this expression reproduces the standard Ramsey oscillations and for n = 1, we reproduce Eq. (6) without any
phase shifts.
4. Calibration of the Jaynes-Cummings gate phase corrections

In this section, we explain how the populated Ramsey experiment can be used to calibrate the single-qubit phase corrections
appearing in the unitary of the JC gate for up to two excitations in the qubit-resonator system. In a realistic experimental
setting, the JC interaction is of the form of a general excitation-preserving exchange. To use the JC gate for actual algorithm
applications, the phases (γn , χn , ζn ) appearing in Eq. (6) need to be calibrated for each n-photon manifold of the block-diagonal
013148-25

## PDF page 26

MICHAEL RENGER et al.

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

JC time-evolution operator. Since we apply the MOVE operation only in pairs and assume the MOVE to perform a full state
transfer in the n = 1 manifold, the phases χ1 and ζ1 are irrelevant here. In the single-photon manifold, only the common
phase γ1 needs to be calibrated and is corrected for using a VZ gate as explained in Appendix D 1. Therefore, we set γ1 = 0
in the following, as we compensate this nonideal phase in the experiment sequence. The populated Ramsey experiment can then
be used to calibrate the phases for the two-photon manifold. The state after the second MOVE gate in the populated-resonator
Ramsey sequence can be expressed as
i
√ (|1, g⟩eiωq t + a|1, e⟩ + b|2, g⟩),
2

(F47)

where we have
2 i(ωq +ωr )t
a ≡ i(c+
e
− s− s+ e2iωr t ),

b ≡ c+ s− ei(ωq +ωr )t + c− s− e2iωr t ,

(F48)

with the abbreviation c± , s± ≡ c2± , s2± [cf. Eq. (5)]. In this case, we find
[
]
P1e = 41 1 + c24 + s24 − 2c22 cos(ωr t − 2γ2 − 2ζ2 ) + 2s22 cos(2ωr t − ωq t − 2γ2 ) − 2c22 s22 cos(ωr t − ωq t + 2ζ2 ) ,

(F49)

c22 s22
[1 + cos((ωr − ωq )t + 2ζ2 )].
(F50)
2
Also in this case, the Ramsey sequence filters the terms rotating with frequency ωr − ωq . The detected excited-state probability
in the qubit rotating frame is
]
[
Pe = 21 1 − c22 cos(t − 2γ2 − 2ζ2 ) + s22 cos(2t − 2γ2 ) ,
(F51)
P2e =

i.e., the noncalibrated phases in the JC interaction directly manifest as phase shifts of the detected populated Ramsey interference
pattern. To restore the ideal interference pattern, one can compensate for these phase shifts by introducing additional control
degrees of freedom. Since the relative phase χ2 cancels out when applying an even number of MOVE operations, only two
degrees of freedom, γ2 and ζ2 , are required in Eq. (F51). In the simplest case, those can be included in the form of subsequent
physical z rotations with phases ϕ and ϕ ′ after the two MOVE operations in the Ramsey sequence, as shown in Fig. 6(b).
For this modified circuit, the state after the first MOVE gate in the Ramsey sequence transforms to
1
− √ (|0, e⟩eiϕ + c+ |1, e⟩eiϕ − is− |2, g⟩),
2

(F52)

i
√ (|1, g⟩eiωq t+iϕ + a|1, e⟩ + b|2, g⟩),
2

(F53)

and after the second MOVE gate

where we have to redefine a and b as
′

′

2 i(ωq +ωr )t+iϕ
a ≡ i(c+
e
− s− s+ e2iωr t+i(ϕ−ϕ ) ),

b ≡ c+ s− ei(ωq +ωr )t+iϕ + c− s− e2iωr t .

The final excited-state probability is given by
[
]
Pe = 21 1 − c22 cos(t − 2γ2 − 2ζ2 + ϕ ′ ) + s22 cos(2t − 2γ2 + ϕ ′ − ϕ) ,

(F54)

(F55)

and therefore, we can restore the ideal Jaynes-Cummings evolution by applying the following phase corrections:
ϕ ′ = 2γ2 + 2ζ2 .

ϕ = 2ζ2 ,

[1] A. Blais, A. L. Grimsmo, S. M. Girvin, and A. Wallraff, Circuit
quantum electrodynamics, Rev. Mod. Phys. 93, 025005 (2021).
[2] M. Kjaergaard, M. E. Schwartz, J. Braumüller, P. Krantz, J. I.J. Wang, S. Gustavsson, and W. D. Oliver, Superconducting
qubits: Current state of play, Annu. Rev. Condens. Matter Phys.
11, 369 (2020).
[3] G. Wendin, Quantum information processing with superconducting circuits: A review, Rep. Prog. Phys. 80, 106001 (2017).
[4] S. Bravyi, O. Dial, J. M. Gambetta, D. Gil, and Z. Nazario,
The future of quantum computing with superconducting qubits,
J. Appl. Phys. 132, 160902 (2022).
[5] R. Acharya, D. A. Abanin, L. Aghababaie-Beni, I. Aleiner,
T. I. Andersen, M. Ansmann, F. Arute, K. Arya, A. Asfaw,

(F56)

N. Astrakhantsev, et al., Quantum error correction below the
surface code threshold, Nature (London) 638, 920 (2025).
[6] F. Arute, K. Arya, R. Babbush, D. Bacon, J. C. Bardin, R.
Barends, R. Biswas, S. Boixo, F. G. S. L. Brandao, D. A. Buell,
et al., Quantum supremacy using a programmable superconducting processor, Nature (London) 574, 505 (2019).
[7] S. Krinner, N. Lacroix, A. Remm, A. Di Paolo, E. Genois, C.
Leroux, C. Hellings, S. Lazar, F. Swiadek, J. Herrmann, G. J.
Norris, C. K. Andersen, M. Müller, A. Blais, C. Eichler, and
A. Wallraff, Realizing repeated quantum error correction in a
distance-three surface code, Nature (London) 605, 669 (2022).
[8] Y. Wu, W.-S. Bao, S. Cao, F. Chen, M.-C. Chen, X. Chen,
T.-H. Chung, H. Deng, Y. Du, D. Fan, et al., Strong quantum

013148-26

## PDF page 27

SUPERCONDUCTING QUBIT-RESONATOR QUANTUM …

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

computational advantage using a superconducting quantum processor, Phys. Rev. Lett. 127, 180501 (2021).
[9] L. Abdurakhimov, J. Adam, H. Ahmad, O. Ahonen, M.
Algaba, G. Alonso, V. Bergholm, R. Beriwal, M. Beuerle, C.
Bockstiegel, et al., Technology and performance benchmarks
of IQM’s 20-qubit quantum computer, arXiv:2408.12433.
[10] J. B. Hertzberg, E. J. Zhang, S. Rosenblatt, E. Magesan, J. A.
Smolin, J.-B. Yau, V. P. Adiga, M. Sandberg, M. Brink, J. M.
Chow, et al., Laser-annealing josephson junctions for yielding
scaled-up superconducting quantum processors, npj Quantum
Inf. 7, 129 (2021).
[11] M. Dupont, B. Evert, M. J. Hodson, B. Sundar, S. Jeffrey, Y.
Yamaguchi, D. Feng, F. B. Maciejewski, S. Hadfield, M. S.
Alam, et al., Quantum-enhanced greedy combinatorial optimization solver, Sci. Adv. 9, eadi0487 (2023).
[12] E. Dennis, A. Kitaev, A. Landahl, and J. Preskill, Topological
quantum memory, J. Math. Phys. 43, 4452 (2002).
[13] A. G. Fowler, M. Mariantoni, J. M. Martinis, and A. N. Cleland,
Surface codes: Towards practical large-scale quantum computation, Phys. Rev. A 86, 032324 (2012).
[14] A. H. Karamlou, I. T. Rosen, S. E. Muschinske, C. N. Barrett,
A. Di Paolo, L. Ding, P. M. Harrington, M. Hays, R. Das,
D. K. Kim, et al., Probing entanglement in a 2D hard-core
Bose–Hubbard lattice, Nature (London) 629, 561 (2024).
[15] Y. Kim, A. Eddins, S. Anand, K. X. Wei, E. van den Berg, S.
Rosenblatt, H. Nayfeh, Y. Wu, M. Zaletel, K. Temme, and A.
Kandala, Evidence for the utility of quantum computing before
fault tolerance, Nature (London) 618, 500 (2023).
[16] N. Lacroix, A. Bourassa, F. J. H. Heras, L. M. Zhang, J. Bausch,
A. W. Senior, T. Edlich, N. Shutty, V. Sivak, A. Bengtsson,
et al., Scaling and logic in the colour code on a superconducting
quantum processor, Nature (London) 645, 614 (2025).
[17] F. Pan and P. Zhang, Simulation of quantum circuits using the
big-batch tensor network method, Phys. Rev. Lett. 128, 030501
(2022).
[18] J. Tindall, M. Fishman, E. M. Stoudenmire, and D. Sels, Efficient tensor network simulation of IBM’s eagle kicked ising
experiment, PRX Quantum 5, 010308 (2024).
[19] X. Gao, M. Kalinowski, C.-N. Chou, M. D. Lukin, B. Barak,
and S. Choi, Limitations of linear cross-entropy as a measure
for quantum advantage, PRX Quantum 5, 010334 (2024).
[20] T. Begušić, J. Gray, and G. K.-L. Chan, Fast and converged
classical simulations of evidence for the utility of quantum computing before fault tolerance, Sci. Adv. 10, eadk4321 (2024).
[21] B. O’Gorman, W. J. Huggins, E. G. Rieffel, and K. B. Whaley,
Generalized swap networks for near-term quantum computing,
arXiv:1905.05118.
[22] M. G. Algaba, M. Ponce-Martinez, C. Munuera-Javaloy, V.
Pina-Canelles, M. J. Thapa, B. G. Taketani, M. Leib, I. de Vega,
J. Casanova, and H. Heimonen, Co-design quantum simulation
of nanoscale nmr, Phys. Rev. Res. 4, 043089 (2022).
[23] S. Bravyi, A. W. Cross, J. M. Gambetta, D. Maslov, P. Rall,
and T. J. Yoder, High-threshold and low-overhead fault-tolerant
quantum memory, Nature (London) 627, 778 (2024).
[24] X. Wu, H. Yan, G. Andersson, A. Anferov, M.-H. Chou, C. R.
Conner, J. Grebel, Y. J. Joshi, S. Li, J. M. Miller, et al.,
Modular quantum processor with an all-to-all reconfigurable
router, Phys. Rev. X 14, 041030 (2024).
[25] S. Hazra, A. Bhattacharjee, M. Chand, K. V. Salunkhe, S.
Gopalakrishnan, M. P. Patankar, and R. Vijay, Ring-resonator-

based coupling architecture for enhanced connectivity in a
superconducting multiqubit network, Phys. Rev. Appl. 16,
024018 (2021).
[26] M. Malekakhlagh, T. Phung, D. Puzzuoli, K. Heya, N.
Sundaresan, and J. Orcutt, Enhanced quantum state transfer and
bell-state generation over long-range multimode interconnects
via superadiabatic transitionless driving, Phys. Rev. Appl. 22,
024006 (2024).
[27] A. Wallraff, D. I. Schuster, A. Blais, L. Frunzio, R.-S. Huang,
J. Majer, S. Kumar, S. M. Girvin, and R. J. Schoelkopf, Strong
coupling of a single photon to a superconducting qubit using
circuit quantum electrodynamics, Nature (London) 431, 162
(2004).
[28] A. Blais, R.-S. Huang, A. Wallraff, S. M. Girvin, and
R. J. Schoelkopf, Cavity quantum electrodynamics for superconducting electrical circuits: An architecture for quantum
computation, Phys. Rev. A 69, 062320 (2004).
[29] G. B. P. Huber, F. A. Roy, L. Koch, I. Tsitsilin, J. Schirk,
N. J. Glaser, N. Bruckmoser, C. Schweizer, J. Romeiro, G.
Krylov, et al., Parametric multi-element coupling architecture
for coherent and dissipative control of superconducting qubits,
PRX Quantum 6, 030313 (2025).
[30] M. Mariantoni, H. Wang, T. Yamamoto, M. Neeley, R. C.
Bialczak, Y. Chen, M. Lenander, E. Lucero, A. D. O’Connell,
D. Sank, M. Weides, J. Wenner, Y. Yin, J. Zhao, A. N. Korotkov,
A. N. Cleland, and J. M. Martinis, Implementing the quantum von neumann architecture with superconducting circuits,
Science 334, 61 (2011).
[31] A. Galiautdinov, A. N. Korotkov, and J. M. Martinis,
Resonator–zero-qubit architecture for superconducting qubits,
Phys. Rev. A 85, 042321 (2012).
[32] C. Song, K. Xu, W. Liu, C.-p. Yang, S.-B. Zheng, H. Deng, Q.
Xie, K. Huang, Q. Guo, L. Zhang, et al., 10-qubit entanglement
and parallel logic operations with a superconducting circuit,
Phys. Rev. Lett. 119, 180511 (2017).
[33] C. Song, K. Xu, H. Li, Y.-R. Zhang, X. Zhang, W. Liu, Q. Guo,
Z. Wang, W. Ren, J. Hao, et al., Generation of multicomponent
atomic Schrödinger cat states of up to 20 qubits, Science 365,
574 (2019).
[34] S. Lloyd and S. L. Braunstein, Quantum computation over
continuous variables, Phys. Rev. Lett. 82, 1784 (1999).
[35] S. L. Braunstein and P. van Loock, Quantum information with
continuous variables, Rev. Mod. Phys. 77, 513 (2005).
[36] N. K. Langford, R. Sagastizabal, M. Kounalakis, C. Dickel,
A. Bruno, F. Luthi, D. J. Thoen, A. Endo, and L. DiCarlo,
Experimentally simulating the dynamics of quantum light
and matter at deep-strong coupling, Nat. Commun. 8, 1715
(2017).
[37] Y. Liu, S. Singh, K. C. Smith, E. Crane, J. M. Martyn, A.
Eickbusch, A. Schuckert, R. D. Li, J. Sinanan-Singh, M. B.
Soley, et al., Hybrid oscillator-qubit quantum processors:
Instruction set architectures, abstract machine models, and applications, PRX Quantum 7, 010201 (2025).
[38] J. Leppäkangas, P. Stadler, D. Golubev, R. Reiner, J.-M. Reiner,
S. Zanker, N. Wurz, M. Renger, J. Verjauw, D. Gusenkova,
et al., Quantum algorithms for simulating systems coupled to
bosonic modes using a hybrid resonator-qubit quantum computer, arXiv:2503.11507.
[39] Y. Chen, C. Neill, P. Roushan, N. Leung, M. Fang, R. Barends,
J. Kelly, B. Campbell, Z. Chen, B. Chiaro, et al., Qubit

013148-27

## PDF page 28

MICHAEL RENGER et al.

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

architecture with high coherence and fast tunable coupling,
Phys. Rev. Lett. 113, 220502 (2014).
[40] X. Li, T. Cai, H. Yan, Z. Wang, X. Pan, Y. Ma, W. Cai, J. Han,
Z. Hua, X. Han, Y. Wu, H. Zhang, H. Wang, Y. Song, L. Duan,
and L. Sun, Tunable coupler for realizing a controlled-phase
gate with dynamically decoupled regime in a superconducting
circuit, Phys. Rev. Appl. 14, 024070 (2020).
[41] Y. Xu, J. Chu, J. Yuan, J. Qiu, Y. Zhou, L. Zhang, X. Tan, Y. Yu,
S. Liu, J. Li, F. Yan, and D. Yu, High-fidelity, high-scalability
two-qubit gate scheme for superconducting qubits, Phys. Rev.
Lett. 125, 240503 (2020).
[42] M. C. Collodo, J. Herrmann, N. Lacroix, C. K. Andersen,
A. Remm, S. Lazar, J.-C. Besse, T. Walter, A. Wallraff, and
C. Eichler, Implementation of conditional phase gates based
on tunable ZZ interactions, Phys. Rev. Lett. 125, 240502
(2020).
[43] Y. Sung, L. Ding, J. Braumüller, A. Vepsäläinen, B. Kannan,
M. Kjaergaard, A. Greene, G. O. Samach, C. McNally, D.
Kim, et al., Realization of high-fidelity CZ and ZZ-free
ISWAP gates with a tunable coupler, Phys. Rev. X 11, 021058
(2021).
[44] F. Marxer, A. Vepsäläinen, S. W. Jolin, J. Tuorila, A. Landra,
C. Ockeloen-Korppi, W. Liu, O. Ahonen, A. Auer, L. Belzane,
et al., Long-distance transmon coupler with cz-gate fidelity
above 99.8%, PRX Quantum 4, 010314 (2023).
[45] H. Zhang, C. Ding, D. K. Weiss, Z. Huang, Y. Ma, C. Guinn,
S. Sussman, S. P. Chitta, D. Chen, A. A. Houck, J. Koch, and
D. I. Schuster, Tunable inductive coupler for high-fidelity gates
between fluxonium qubits, PRX Quantum 5, 020326 (2024).
[46] J. Koch, T. M. Yu, J. Gambetta, A. A. Houck, D. I. Schuster,
J. Majer, A. Blais, M. H. Devoret, S. M. Girvin, and R. J.
Schoelkopf, Charge-insensitive qubit design derived from the
cooper pair box, Phys. Rev. A 76, 042319 (2007).
[47] F. Motzoi, J. M. Gambetta, P. Rebentrost, and F. K. Wilhelm,
Simple pulses for elimination of leakage in weakly nonlinear
qubits, Phys. Rev. Lett. 103, 110501 (2009).
[48] E. Hyyppä, A. Vepsäläinen, M. Papič, C. F. Chan, S. Inel, A.
Landra, W. Liu, J. Luus, F. Marxer, C. Ockeloen-Korppi, et al.,
Reducing leakage of single-qubit gates for superconducting
quantum processors using analytical control pulse envelopes,
PRX Quantum 5, 030353 (2024).
[49] J. M. Martinis, S. Nam, J. Aumentado, K. M. Lang, and C.
Urbina, Decoherence of a superconducting qubit due to bias
noise, Phys. Rev. B 67, 094510 (2003).
[50] J. Bylander, S. Gustavsson, F. Yan, F. Yoshihara, K. Harrabi,
G. Fitch, D. G. Cory, Y. Nakamura, J.-S. Tsai, and W. D.
Oliver, Noise spectroscopy through dynamical decoupling with
a superconducting flux qubit, Nat. Phys. 7, 565 (2011).
[51] Z. K. Minev, Z. Leghtas, S. O. Mundhada, L. Christakis, I. M.
Pop, and M. H. Devoret, Energy-participation quantization of
Josephson circuits, npj Quantum Inf. 7, 131 (2021).
[52] D. C. McKay, C. J. Wood, S. Sheldon, J. M. Chow, and J. M.
Gambetta, Efficient z gates for quantum computing, Phys. Rev.
A 96, 022330 (2017).
[53] F. Bao, H. Deng, D. Ding, R. Gao, X. Gao, C. Huang, X.
Jiang, H.-S. Ku, Z. Li, X. Ma, et al., Fluxonium: An alternative
qubit platform for high-fidelity operations, Phys. Rev. Lett. 129,
010502 (2022).
[54] E. Magesan, J. M. Gambetta, B. R. Johnson, C. A.
Ryan, J. M. Chow, S. T. Merkel, M. P. da Silva,

G. A. Keefe, M. B. Rothwell, T. A. Ohki, et al., Efficient measurement of quantum gate error by interleaved
randomized benchmarking, Phys. Rev. Lett. 109, 080505
(2012).
[55] E. Knill, D. Leibfried, R. Reichle, J. Britton, R. B. Blakestad,
J. D. Jost, C. Langer, R. Ozeri, S. Seidelin, and D. J. Wineland,
Randomized benchmarking of quantum gates, Phys. Rev. A 77,
012307 (2008).
[56] H. Xiong, J. Wang, J. Song, J. Yang, Z. Bao, Y. Li, Z.-Y.
Mi, H. Zhang, H.-F. Yu, Y. Song, and L. Duan, Scalable lowoverhead superconducting non-local coupler with exponentially
enhanced connectivity, arXiv:2502.18902.
[57] J. Helsen and S. Wehner, A benchmarking procedure for quantum networks, npj Quantum Inf. 9, 17 (2023).
[58] K. Heya, T. Phung, M. Malekakhlagh, R. Steiner, M. Turchetti,
W. Shanks, J. Mamin, W.-S. Lu, Y. P. Kandel, N. Sundaresan,
et al., Randomized benchmarking of a high-fidelity remote
CNOT gate over a meter-scale microwave interconnect, Phys.
Rev. Lett. 135, 200801 (2025).
[59] S. Sheldon, L. S. Bishop, E. Magesan, S. Filipp, J. M. Chow,
and J. M. Gambetta, Characterizing errors on qubit operations via iterative randomized benchmarking, Phys. Rev. A 93,
012301 (2016).
[60] T. Abad, J. Fernández-Pendás, A. Frisk Kockum, and G.
Johansson, Universal fidelity reduction of quantum operations from weak dissipation, Phys. Rev. Lett. 129, 150504
(2022).
[61] T. Abad, Y. Schattner, A. F. Kockum, and G. Johansson, Impact
of decoherence on the fidelity of quantum gates leaving the
computational subspace, Quantum 9, 1684 (2025).
[62] D. M. Greenberger, M. A. Horne, and A. Zeilinger, Going
beyond Bell’s theorem, in Bell’s Theorem, Quantum Theory and
Conceptions of the Universe, edited by M. Kafatos (Springer
Netherlands, Dordrecht, 1989), pp. 69–72.
[63] T.-C. Wei and P. M. Goldbart, Geometric measure of entanglement and applications to bipartite and multipartite quantum
states, Phys. Rev. A 68, 042307 (2003).
[64] K. X. Wei, I. Lauer, S. Srinivasan, N. Sundaresan, D. T.
McClure, D. Toyli, D. C. McKay, J. M. Gambetta, and S.
Sheldon, Verifying multipartite entangled Greenberger-HorneZeilinger states via multiple quantum coherences, Phys. Rev. A
101, 032343 (2020).
[65] J. Baum, M. Munowitz, A. N. Garroway, and A. Pines,
Multiple-quantum dynamics in solid state NMR, J. Chem. Phys.
83, 2015 (1985).
[66] S. Martiel, T. Ayral, and C. Allouche, Benchmarking quantum
coprocessors in an application-centric, hardware-agnostic, and
scalable way, IEEE Trans. Quantum Eng. 2, 1 (2021).
[67] E. Farhi, J. Goldstone, and S. Gutmann, A quantum approximate optimization algorithm, arXiv:1411.4028.
[68] K. Bharti, A. Cervera-Lierta, T. H. Kyaw, T. Haug, S. AlperinLea, A. Anand, M. Degroote, H. Heimonen, J. S. Kottmann,
T. Menke, et al., Noisy intermediate-scale quantum algorithms,
Rev. Mod. Phys. 94, 015004 (2022).
[69] A. Ozaeta, W. van Dam, and P. L. McMahon, Expectation
values from the single-layer quantum approximate optimization
algorithm on Ising problems, Quantum Sci. Technol. 7, 045036
(2022).
[70] J. Weidenfeller, L. C. Valor, J. Gacon, C. Tornow, L. Bello, S.
Woerner, and D. J. Egger, Scaling of the quantum approximate

013148-28

## PDF page 29

SUPERCONDUCTING QUBIT-RESONATOR QUANTUM …

PHYSICAL REVIEW RESEARCH 8, 013148 (2026)

optimization algorithm on superconducting qubit based hardware, Quantum 6, 870 (2022).
[71] P. D. Nation and M. Treinish, Suppressing quantum circuit
errors due to system variability, PRX Quantum 4, 010327
(2023).
[72] P. D. Nation, H. Kang, N. Sundaresan, and J. M. Gambetta,
Scalable mitigation of measurement errors on quantum computers, PRX Quantum 2, 040326 (2021).
[73] S. Bravyi, A. Kliesch, R. Koenig, and E. Tang, Obstacles to
variational quantum optimization from symmetry protection,
Phys. Rev. Lett. 125, 260505 (2020).
[74] J. Rönkkö, O. Ahonen, V. Bergholm, A. Calzona, A. Geresdi,
H. Heimonen, J. Heinsoo, V. Milchakov, S. Pogorzalek, M.
Sarsby, et al., On-premises superconducting quantum computer
for education and research, EPJ Quantum Technol. 11, 32
(2024).
[75] M. Hofheinz, H. Wang, M. Ansmann, R. C. Bialczak, E.
Lucero, M. Neeley, A. D. O’Connell, D. Sank, J. Wenner, J. M.
Martinis, and A. N. Cleland, Synthesizing arbitrary quantum
states in a superconducting resonator, Nature (London) 459, 546
(2009).
[76] J. M. Fink, M. Göppl, M. Baur, R. Bianchetti, P. J. Leek, A.
Blais, and A. Wallraff, Climbing the Jaynes–Cummings ladder
and observing its nonlinearity in a cavity QED system, Nature
(London) 454, 315 (2008).
[77] H.-F. Wang, A.-D. Zhu, S. Zhang, and K.-H. Yeon, Simple implementation of discrete quantum Fourier transform via cavity
quantum electrodynamics, New J. Phys. 13, 013021 (2011).
[78] F. Arute, K. Arya, R. Babbush, D. Bacon, J. C. Bardin, R.
Barends, A. Bengtsson, S. Boixo, M. Broughton, B. B. Buckley,
et al., Observation of separated dynamics of charge and spin in
the Fermi-Hubbard model, arXiv:2010.07965.
[79] A. Hosseinkhani, F. Šimkovic, A. Calzona, T. Liu, A. Auer, and
I. de Vega, Noise-robust estimation of quantum observables in
noisy hardware, arXiv:2503.06695.
[80] W. W. Ho and T. H. Hsieh, Efficient variational simulation of
non-trivial quantum states, SciPost Phys. 6, 029 (2019).
[81] A. Hashim, R. K. Naik, A. Morvan, J.-L. Ville, B. Mitchell,
J. M. Kreikebaum, M. Davis, E. Smith, C. Iancu, K. P. O’Brien,
et al., Randomized compiling for scalable quantum computing
on a noisy superconducting quantum processor, Phys. Rev. X
11, 041039 (2021).
[82] A. Kandala, K. Temme, A. D. Córcoles, A. Mezzacapo, J. M.
Chow, and J. M. Gambetta, Error mitigation extends the

computational reach of a noisy quantum processor, Nature
(London) 567, 491 (2019).
[83] K. Schultz, R. LaRose, A. Mari, G. Quiroz, N. Shammah, B. D.
Clader, and W. J. Zeng, Impact of time-correlated noise on zeronoise extrapolation, Phys. Rev. A 106, 052406 (2022).
[84] H. Bombin and M. A. Martin-Delgado, Topological quantum
distillation, Phys. Rev. Lett. 97, 180501 (2006).
[85] A. J. Landahl, J. T. Anderson, and P. R. Rice, Fault-tolerant
quantum computing with color codes, arXiv:1108.5738.
[86] Y. Takada and K. Fujii, Improving threshold for fault-tolerant
color-code quantum computing by flagged weight optimization,
PRX Quantum 5, 030352 (2024).
[87] P. Krantz, M. Kjaergaard, F. Yan, T. P. Orlando, S. Gustavsson,
and W. D. Oliver, A quantum engineer’s guide to superconducting qubits, Appl. Phys. Rev. 6, 021318 (2019).
[88] F. Yan, P. Krantz, Y. Sung, M. Kjaergaard, D. L. Campbell, T. P.
Orlando, S. Gustavsson, and W. D. Oliver, Tunable coupling
scheme for implementing high-fidelity two-qubit gates, Phys.
Rev. Appl. 10, 054062 (2018).
[89] L. Heunisch, C. Eichler, and M. J. Hartmann, Tunable coupler to fully decouple and maximally localize superconducting
qubits, Phys. Rev. Appl. 20, 064037 (2023).
[90] M. Papič, J. Tuorila, A. Auer, I. de Vega, and A.
Hosseinkhani, Charge-parity switching effects and optimisation
of transmon-qubit design parameters, npj Quantum Inf. 10, 69
(2024).
[91] M. O. Scully and M. S. Zubairy, Quantum Optics (Cambridge
University Press, Cambridge, 1997).
[92] Y. Chu, P. Kharel, W. H. Renninger, L. D. Burkhart, L. Frunzio,
P. T. Rakich, and R. J. Schoelkopf, Quantum acoustics with
superconducting qubits, Science 358, 199 (2017).
[93] M. Mariantoni, E. P. Menzel, F. Deppe, M. A. Araque
Caballero, A. Baust, T. Niemczyk, E. Hoffmann, E. Solano, A.
Marx, and R. Gross, Planck spectroscopy and quantum noise
of microwave beam splitters, Phys. Rev. Lett. 105, 133601
(2010).
[94] S. Gandorfer, M. Renger, W. Yam, F. Fesquet, A. Marx, R.
Gross, and K. Fedorov, Two-dimensional planck spectroscopy
for microwave photon calibration, Phys. Rev. Appl. 23, 024064
(2025).
[95] S. Boixo, S. V. Isakov, V. N. Smelyanskiy, R. Babbush, N.
Ding, Z. Jiang, M. J. Bremner, J. M. Martinis, and H. Neven,
Characterizing quantum supremacy in near-term devices, Nat.
Phys. 14, 595 (2018).

013148-29
