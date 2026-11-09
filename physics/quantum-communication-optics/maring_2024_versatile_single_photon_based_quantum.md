Source: https://www.nature.com/articles/s41566-024-01403-4.pdf
PDF sha256: 0ee7b47bd7232f863f2984c3a8cc2c42fbf2787a017bfe08f0d4e23139248f98
License: CC-BY
Language: eng
Fidelity: machine-gated

# Transcription of maring_2024_versatile_single_photon_based_quantum.pdf

Transcription of `maring_2024_versatile_single_photon_based_quantum.pdf` in this directory, 9 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 3 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories; pages 1-2, 4-9 from the PDF's own text layer (pdftotext version 26.10.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

nature photonics
Article

https://doi.org/10.1038/s41566-024-01403-4

A versatile single-photon-based quantum
computing platform
Received: 2 June 2023
Accepted: 6 February 2024
Published online: 26 March 2024
Check for updates

Nicolas Maring 1, Andreas Fyrillas 1,3, Mathias Pont1,2,3, Edouard Ivanov1,3,
Petr Stepanov1, Nico Margaria 1, William Hease1, Anton Pishchagin1,
Aristide Lemaître 2, Isabelle Sagnes 2, Thi Huong Au1, Sébastien Boissier 1,
Eric Bertasi1, Aurélien Baert1, Mario Valdivia1, Marie Billard1, Ozan Acar1,
Alexandre Brieussel1, Rawad Mezher1, Stephen C. Wein1, Alexia Salavrakos 1,
Patrick Sinnott1, Dario A. Fioretto2, Pierre-Emmanuel Emeriau1, Nadia Belabas 2,
Shane Mansfield1, Pascale Senellart 2, Jean Senellart 1 &
Niccolo Somaschi 1

Quantum computing aims at exploiting quantum phenomena to efficiently
perform computations that are unfeasible even for the most powerful classical
supercomputers. Among the promising technological approaches, photonic
quantum computing offers the advantages of low decoherence, information
processing with modest cryogenic requirements, and native integration with
classical and quantum networks. So far, quantum computing demonstrations
with light have implemented specific tasks with specialized hardware, notably
Gaussian boson sampling, which permits the quantum computational advantage
to be realized. Here we report a cloud-accessible versatile quantum
computing prototype based on single photons. The device comprises a
high-efficiency quantum-dot single-photon source feeding a universal linear
optical network on a reconfigurable chip for which hardware errors are
compensated by a machine-learned transpilation process. Our full software
stack allows remote control of the device to perform computations via logic
gates or direct photonic operations. For gate-based computation, we benchmark
one-, two- and three-qubit gates with state-of-the art fidelities of 99.6 ± 0.1%,
93.8 ± 0.6% and 86 ± 1.2%, respectively. We also implement a variational quantum
eigensolver, which we use to calculate the energy levels of the hydrogen molecule
with chemical accuracy. For photon native computation, we implement a
classifier algorithm using a three-photon-based quantum neural network and
report a six-photon boson sampling demonstration on a universal reconfigurable
integrated circuit. Finally, we report on a heralded three-photon entanglement
generation, a key milestone toward measurement-based quantum computing.
Realizations of quantum computing have built on rapid progress in
controlling physical systems that can support quantum information;
for example, superconducting circuits1,2, trapped ions3,4, neutral atoms5
and light6,7. These technological breakthroughs have brought four

A full list of affiliations appears at the end of the paper.

Nature Photonics | Volume 18 | June 2024 | 603–609

platforms to the regime of quantum computational advantage1,2,8–10 by
solving specific sampling problems that would require unreasonable
computing time even for the most powerful classical supercomputers.
Two of these four are photonic, which highlights the position of

e-mail: jean.senellart@quandela.com; niccolo.somaschi@quandela.com

603

## PDF page 2

Article
light-based technology among the leading platforms. Quantum light
as a quantum information carrier offers the advantage of low decoherence and comes with a many degrees of freedom with which to encode
the information, while providing natural connectivity for distributed
or blind quantum computing11.
Over the years, a variety of proposals that take the discrete-variable
photonic approach to universal fault-tolerant computing have been
put forward, in which quantum information is encoded with single
photons12–15. With identified thresholds, these roadmaps motivate the
development of quantum computing hardware based on single-photon
sources, integrated photonic chips and single-photon detectors. Experimental progress of ever-increasing complexity has been achieved
with integrated sources exploiting nonlinear effects, including with
large-scale integrated chips16,17. However, the probabilistic nature of
the single-photon generation process, the need for it to be heralded
and the requirement for it to operate at low efficiency to limit multiphoton events are strong constraints on hardware architectures. This has
resulted in a limited number of manipulated photons with typical rates
in the megahertz range for four photons, and the demonstration of
specific information processing tasks that rely on dedicated photonic
chips17. Overcoming these limitations is foreseen through the use of
massive multiplexing of hundreds of heralded sources18.
Another path to large-scale quantum computing with single
photons has emerged, owing to deterministic single-photon source
devices based on semiconductor quantum dots19–21. Such sources
have demonstrated record single-photon generation efficiency that
is 10–20 times higher than their nonlinear counterparts, allowing for a
drastic reduction in resource requirements. Such efficiencies allowed
a record manipulation of 14 single photons in a free-space boson sampling experiment22. Very recently, the same quantum dot sources have
shown their ability to deterministically generate photonic cluster
states at high rates23, even further reducing the foreseen overheads for
large-scale measurement-based quantum computation24.
In this work we report a multipurpose cloud-accessible25 singlephoton-based quantum computing machine, named Ascella, which
is based on six photonic qubits generated by an on-demand quantum
dot source. The quantum information is encoded in the path degree of
freedom and arbitrarily manipulated in a 12-mode integrated universal
interferometer. A machine-learned transpilation process corrects for
the hardware manufacturing errors. Ascella operates the largest number of single photons on a chip so far with a six-photon sampling rate of
4 Hz, and shows operation stability over weeks. We benchmark its performances and demonstrate applications both in the gate-based and
photonic computation frameworks. Each reported result represents
either state-of-the-art performance or a novel experimental demonstration for which we provide the full code to reproduce through Quandela Cloud25. The numerous applications illustrate the general-purpose
potential of the machine for noisy near-term quantum computing. We
finally discuss the evolution of the reported platform towards scale-up,
and demonstrate a critical step for future measurement-based quantum computation: heralded entanglement generation of three-photon
Greenberger–Horne–Zeilinger (GHZ) states.

Results

Single-photon based computer
Ascella’s hardware (Fig. 1a) comprises an on-demand high-brightness
single-photon source; a programmable optical demultiplexer, which
allows up to six single photons to simultaneously interfere with a
12-mode reconfigurable universal interferometer; and a single-photon
detection and post-processing unit.
The on-demand single-photon source (see Supplementary
Section 1), which is based on an InGaAs quantum dot in a microcavity19,
is optically excited at an 80 MHz rate. It exploits a neutral dot and
longitudinal-acoustic-phonon-assisted near-resonant excitation26 to
emit linearly polarized single photons with 55% probability into the
Nature Photonics | Volume 18 | June 2024 | 603–609

https://doi.org/10.1038/s41566-024-01403-4

collection lens. To send six single photons to every even input mode
of the chip, an active optical demultiplexer sequentially deflects the
photon stream into six optical fibres of different lengths adjusted to
synchronize the photons27. Using optical shutters, the demultiplexer
can prepare any input state from |000000000000⟩ to |101010101010⟩
(photon positions can subsequently be swapped; see Supplementary
Section 2). The 12-mode photonic integrated circuit (Si3N4 platform)
is composed of 126 voltage-controlled thermo-optic phase shifters and
132 directional couplers28 that are laid out in a rectangular universal
interferometer scheme (see Fig. 1a), allowing for the implementation
of all 12 × 12 unitary matrices with an average fidelity of F = 99.7 ± 0.08%
thanks to a custom compilation and transpilation process (see
Methods). Finally, the 12 outputs of the circuit are connected
to high-efficiency superconducting nanowire single-photon
detectors, and N-photon detection events are registered using a
time-to-digital converter.
The average total efficiency of the optical set-up is ∼8%, which
includes the single-photon source device brightness, the transmission
of all optical components, and the detection efficiencies (see Supplementary Section 2). This leads to record-breaking two- to four-photon
on-chip coincidence rates (Fig. 1b), and on-chip processing of five and
six photons, at rates of 50 Hz and 4 Hz, respectively. We measure high
single-photon purity of >99% and high indistinguishability of ∼94%;
these values are independent of the delays between photon emission
(up to 1 μs), resulting in a measured on-chip two-photon interference
visibility for all 15 pairs of 91−94% (see Supplementary Section 3). The
genuine four- and six-photon indistinguishability—defined as the
probability that the N photons are identical—establishes a new record
value of 0.85 ± 0.02 for four photons29, and a value of 0.76 ± 0.02 for
six photons. We ensure long-term stability and high-performance
operation of Ascella by monitoring key metrics and by performing
automated system optimization runs hourly. This guarantees a highly
stable and long-term operation over several weeks (see Fig. 1b), and
robustness against external temperature fluctuations and mechanical
perturbations.
To operate the machine, tasks are sent remotely using the
Python-based open-source framework Perceval30. The user can either
specify (see Fig. 1c) a photonic circuit, a gate-based circuit, or a unitary
transformation (U) to be applied to a specified input state containing
one to six photons, as well as optional post-selection criteria. Output
photon coincidences are then acquired up to the desired sample number, and data sample results are sent back to the user, either as a stream
of events or as an aggregated state:count inventory.

Gate-based quantum computation
Following the Knill–Laflamme–Milburn scheme31, Ascella can perform
probabilistic gate-based protocols. Within this quantum computation
framework, we benchmark quantum logic gates on up to three qubits
and implement a hybrid variational quantum eigensolver (VQE).
Benchmarking logic gates. Ideally, a gate U applied to an initial pure
state |ψ⟩ will produce the pure state U |ψ⟩. In reality, errors, which are
quantified by a noise channel Λ (ref. 32), corrupt the final state, which
is then described by a density matrix ρ = Λ(U |ψ⟩ ⟨ψ| U † ). A standard
figure of merit to quantify the gate performance is the quantum state
fidelity Fψ (U) = ⟨ψ|U † ρU|ψ⟩ of the final state ρ to the ideal state U |ψ⟩.
To assess Ascella’s performance for a given gate, we evaluate the
fidelity of the gate averaged over all possible input states |ψ⟩, that is,
Favg(U) = ∫Fψ(U)dψ, where the integral is taken over the Haar measure.
A brute-force approach to estimating Favg(U) requires an impractically large number of measurements. A more efficient method, randomized benchmarking, has been proposed for matter qubits33, but
applies long sequences of gates from specific sets of unitaries34. As
photonic quantum processing converts any quantum circuit to a photonic circuit35, we use a new method to evaluate Favg (R.M. & S.C.W.,
604

## PDF page 3

<b>Article</b>
https://doi.org/10.1038/s41566-024-01403-4
а
Filtering
Bandpass filter
Demultiplexer
SPS
Polarization
controller
Polarizer
Electrical
|Input>
connection
Optical path
5 µm
Universal
interferometer
Quandela Cloud
User
Correlator
<b>SNSPD</b>
b
10<sup>5</sup>
100.0
2-photon
Coincidence rates (Hz)
97.5
10<sup>4</sup>
Average value (%)
3-photon
95.0
10<sup>3</sup>
92.5
4-photon
10<sup>2</sup>
90.0

    Purity


    HOM 3T

5-photon
10<sup>1</sup>
HOM 4T

    HOM 1T

87.5

    HOM 2T


    HOM 5T

6-photon
10°
85.0
0
5
10
0
5
10
Days
Days
Ascella QPU
Perceval user
Quandela Cloud
C
Ascella CPU
Input state |input>
+
PIRCIVAL
OR

OR
Ф

Compilation
<math display="block">U \to \overrightarrow{\phi}</math>
<math display="block">\overrightarrow{\phi} \to \overrightarrow{V}</math>
Single-photon and
(PC)
(GB)
(U)
Transpilation
coincidence counts
Fig. 1 | Architecture, performance and stability of Ascella. a, Sketch of the
The rates are integrated for 50 s. The grey areas correspond to maintenance and
upgrade periods. In the right figure, we also monitor the on-chip photon
overall architecture of the six single-photon quantum computer. A quantum-dot
single-photon source (SPS) device at 5 K is operated at a repetition rate of
indistinguishability and single-photon purity, as quantified by the Hong-Ou-
Mandel (HOM) visibility <math>V_{\text{HOM}}</math> and <math>1 - g^{(2)}(0)</math>, respectively, where <math>g^{(2)}</math> is the
80 MHz. An active demultiplexer followed by fibred delays converts the train of
normalized second-order correlation function. HOM kT is <math>V_{\text{HOM}}</math> for delays <math>k \times \Delta T</math>
single photons into six photons arriving simultaneously at the universal 12-mode
photonic chip. Photons are detected at the chip output by superconducting
between emitted photons where <math>\Delta T = 180</math> ns. Each data point corresponds to a
nanowire single-photon detectors (SNSPD) and detection times are processed by
correlation histogram integrated over 10 s. c, Job execution flowchart on Ascella.
a correlator. A full software stack controls the unitary matrix <math>U</math> implemented on
Perceval users may send jobs consisting in photonic circuits, or a gate-based
the chip through the voltages <math>\vec{V}</math> applied on 126 thermal phase shifters, yielding
circuit (GB) or a unitary matrix <math>(U)</math>, along with the desired input state to the
phase shifts <math>\vec{\phi}</math>, and the photonic input state according to the job requested. It
Quandela Cloud. The job is first processed by a CPU, which computes the
necessary phase shifts <math>\vec{\phi}</math> to apply, and subsequently the voltages <math>\vec{V}</math> for the
also recalibrates hourly and readjusts all hardware control knobs for optimal
performance. The single photons are sent into a photonic chip featuring a
on-chip phase shifters from our compilation and transpilation process. Finally,
universal interferometer scheme capable of implementing any <math>12 \times 12</math> unitary
the user receives the collected single-photon and coincidence counts after the
matrix. <b>b</b>, Detected N-photon coincidence rates for N-photon inputs as a function
computation on the quantum processing unit (QPU).
of time, with the photonic circuit configured to implement the identity matrix.
Nature Photonics | Volume 18 | June 2024 | 603-609
605

## PDF page 4

Article

https://doi.org/10.1038/s41566-024-01403-4

Table 1 | Average gate fidelities of one-, two- and three-qubit
gates implemented by Ascella evaluated based on K
expectation values obtained from M measurement
configurations
Qubits, n

Gate, U

Success
probability

Favg (U) (%)

M

K

24n

1

T

1

99.6 ± 0.1

4

4

16

2

CNOT

1/9

93.8 ± 0.6

36

58

256

3

Toffoli

≈1/57

86 ± 1.2

340

593

4,096

The success probability of the CNOT62 and Toffoli67 gates are indicated.

manuscript in preparation). Our method exploits symmetries so that
the contribution of most Fψs to Favg cancel out, allowing Favg to be
K
expressed as a finite discrete sum Favg = ∑i=1 wi mi of K expectation
values mi with weight wi (see Supplementary Section 5). The wi and the
state preparation and measurement configurations for each mi
depend on the gate U and are pre-computed. Each configuration consists in preparing an unentangled initial state |ψ⟩, applying the gate and
performing single-qubit Pauli measurements. For the gates benchmarked on Ascella (see Table 1), the K expectation values mi are obtained
from M ≤ K measurement configurations, with K less than the ∼24n measurements required for full process tomography36 of an n-qubit gate.
The average gate fidelities measured for the T (defined as
i

π
4

T ∶= |0⟩ ⟨0| 𝕀 e |1⟩ ⟨1|), CNOT and Toffoli gates are shown in Table 1.
To the best of our knowledge, these are record fidelities for the
two-photon CNOT37,38 and three-photon Toffoli39 gates. This group of
measurements sets a benchmark for universal photonic quantum
computing, and is on par with the benchmarked performance of
open-access quantum computing platforms based on ions and superconducting qubits (see Supplementary Section 5). These values are a
lower bound on the true average gate fidelities, as they also include
errors related to state preparation and measurement roughly given by
(1 − Favg(T-gate)2n/3), which is 0.3 ± 0.1%, 0.5 ± 0.1% and 0.8 ± 0.2% for the
T, CNOT and Toffoli gates, respectively.

Variational quantum eigensolver. We illustrate gate-based computation possibilities by implementing a VQE algorithm to compute the
ground-state energies of an H2 molecule; VQE exploits the variational
principle stating that, given a Hamiltonian ℋ̂ and an ansatz wavefunction ||ψ(θ ⃗ )⟩ parameterized by θ ⃗ , the ground-state energy associated
with ℋ̂ satisfies E0 ≤ ⟨ψ(θ ⃗ )|| ℋ̂ ||ψ(θ ⃗ )⟩ (ref. 40). In this context, VQE
explores the state space by minimizing the energy to find a chemically
accurate approximation of E0. Reaching chemical accuracy (defined
as obtaining a result within ±0.0016 Ha of the theoretical value) is critical for making realistic chemical predictions.
We build the fermionic Hamiltonian for H2 using the symmetryconserving Bravyi–Kitaev transformation41, which is available via the
OpenFermion42 Python package (see Methods). Symmetry allows
reduction of the problem to the effective Hamiltonian ℋ̂ qubit , which
acts on two qubits expressed in the standard Pauli basis (𝕀, X, Y and Z),
ℋ̂ qubit (r) = α𝕀𝕀𝕀𝕀 𝕀 βZ𝕀𝕀 𝕀 γ𝕀𝕀Z + δZZ + μXX

(1)

with real parameters α, β, γ, δ and μ, which depend on the choice of
bond length r. We create ansatz states ||ψ(θ ⃗ )⟩ made of two path-encoded
qubits using single-qubit operations R(θ ⃗ i ) and an entangling
post-selected controlled NOT (CNOT) gate (see Fig. 2a). To make a
chemically accurate prediction of E0, we first find the optimal bond
length (ropt), which is the one that corresponds to the lowest energy by
varying r between 0.2 and 2.05 Å.
The expectation value of ℋ̂ qubit (r) on ||ψ(θ ⃗ )⟩ is obtained from
the weighted averages of 10,000 post-processed two-photon samples,
Nature Photonics | Volume 18 | June 2024 | 603–609

giving an accuracy of ±0.01 Ha. The classical processor then evaluates
a loss function by using a gradient-free optimizer based on expectation
values obtained from Ascella, and corrected using an error-mitigation
scheme inspired by ref. 43. Then θ ⃗ is updated classically in a feedback
loop between Ascella and a classical processor to reach lower and lower
energies. We then make an additional experimental run at ropt with
400,000 post-processed two-photon samples to obtain an accuracy
of ±0.00158 Ha on the ground-state energy associated with
ℋ̂ qubit (r opt ) . We compare this value with E0 to confirm that we have
reached chemical accuracy. In the two steps highlighted above, we use
error mitigation to compute the minimal energies of ℋ̂ qubit (r) (see
Supplementary Section 8). For any initial random parameters and
bond lengths, the algorithm consistently converges to the theoretical
eigenvalues in 50 to 100 iterations (see Fig. 2a). The entire experiment
time per bond length is approximately four times faster than past
photonic VQE experiments of a system with the same number of
degrees of freedom40. At fixed initial conditions and ropt, chemical
accuracy was achieved with a success probability of 93%, with
greater accuracy than recent photonic VQE experiments43. These two
improvements are due to higher-quality single-photon sources and
chip control. Note that the accuracy is on par with VQE experiments
on superconducting qubits44,45 and ions traps46,47, and is reached by
using a photonic platform.

Photon-native quantum computation
We now demonstrate the operation of Ascella in its native photonic
framework, where the information is directly processed through
photonic quantum interferences in chosen unitary transformations
and detection.
Photon-based quantum neural network. We train a quantum neural
network48 on Ascella for a supervised learning classification task. We
build a VQE algorithm where, taking inspiration from ref. 49, we use a
native photonic ansatz. We perform multiclass classification on the
well-known IRIS dataset50. To the best of our knowledge, this is the first
experimental implementation of a variational quantum classifier with
single photons; we refer to ref. 51 for a realization on a superconducting platform and to ref. 52 for a two-photon classifier based on kernel
methods. Following our photon-native approach, we design the ansatz
of the variational algorithm directly using the beamsplitters and phase
shifters on five modes of Ascella, in which we input three photons. We
also implement partial pseudo photon-number resolution by exploiting four extra modes of the chip.
We train the model using a see-saw optimization between the
chip parameters and the output state parameters that define the
measurement observable. Each iteration requires 112 experiments,
one for each data point in the training set, and we gather 50,000
samples per run. A batch functionality in Perceval30 allows us to
send all data points as one job to the server. Details on the ansatz
and the training can be found in Methods and Supplementary
Section 7. After about 15 iterations, we find an accuracy of 0.92 and
0.95 on the training and test sets, respectively. Figure 2b provides
a summary of the model predictions versus actual labels as a
confusion matrix.
Boson sampling with six single photons. Boson sampling is a sampling problem suited for demonstrating a quantum-over-classical
advantage with optical quantum computing platforms53. The recent
demonstrations of quantum advantage6,10 in the Gaussian boson
sampling framework used squeezed light manipulated in free-space
interferometers to limit optical losses. Genuine single-photon-based
Boson sampling has progressed poorly on integrated chips due to the
low efficiency of heralded sources54–57. Here we demonstrate on-chip
boson sampling for a record number of six photons with a fully reconfigurable interferometer. A 12 × 12 Haar-random unitary matrix is
606

## PDF page 5

Article

https://doi.org/10.1038/s41566-024-01403-4

a

Classical processor
Compute loss
as the energy of
the system

Build expectation
values from
samples

Energy (Ha)

Gate-based

Gradient-free
optimizer for
feedback control

Theoretical eigenvalues of H2

→

θupdated
Ascella
→

R(θ1)

→

CNOT

R(θ2)

H/II

→

H/II

R(θ3)

VQE energies evaluated with Ascella

0

–1.05

–0.4

–1.10

0.6

–0.8

0.8

–1.2
0.25

0.50

0.75

1.00

1.25

1.50

1.75

2.00

Bond length (Å)
Classical processor

Train

θ1
0.02

x4

x1
x3

→

θ2 PPNR

35

0

0

1

0

34

5

2

0

4

34

1

2

0

|101010101010

0.01

0.01
0.02

|111111000000

Six-photon outcome
Ascella

U

0

0

1

0

10

1

2

0

1

11

1

2

Predicted label

Boson sampler
Uniform sampler

Boson sampler
Distinguishable sampler
2k

2k
1k
0
–1 k

12 × 12
Haar-random

15

0

3k

|000000111111

0

Predicted label

4k

0

A&A counter

c

x2

True label

→

Probability

Photon-based

Ascella

Test

0

True label

→

θupdated

Likelihood ratio counter

b

1k
0
–1 k
–2 k

–2 k
0

2.5 k

5k

7.5 k

Six-photon events

10 k

0

2.5 k

5k

7.5 k

10 k

Six-photon events

Fig. 2 | Computations of Ascella. a, Gate-based computation. Hybrid VQE.
On Ascella, the single-qubit gates R(θ⃗ i ), together with a CNOT gate, create an
ansatz two-qubit state. We then measure in the Z-basis (using the identity gate 𝕀)
or in the X-basis (using the Hadamard gate H). The output counts (grey arrows)
are sent to a classical processor, which reconstructs the corresponding energy
and implements a feedback loop to update the single-qubit gate angles θ⃗ i via a
gradient-free optimizer, and find an ansatz closer to the ground state. Each
iteration on the QPU takes about 22 s (including 14 s of QPU time and classical
communication to the cloud). Chemical accuracy was reached for ropt = 0.75Å.
Each data point corresponds to 10,000 post-processed two-photon coincidence
samples, except for ropt = 0.75 Å, which corresponds to 400,000. The error
bars correspond to ±1 s.d. of the photon counting statistics. b,c, Photon-native
computation. b, Left: classification task using a quantum neural network

and using the pseudo photon number resolving (PPNR) capabilities of the
photonic circuit. Right: confusion matrices for the classification of the IRIS
dataset on Ascella. The accuracy for the training and test sets is 0.92 and 0.95,
respectively; 50,000 samples were used for each experimental iteration. c, Left:
six single-photon boson sampling. Measured (top) and modelled (bottom)
six-photon output distributions for the input state |101010101010⟩. The 924
six-photon outcomes are canonically ordered from |000000111111⟩ to
|111111000000⟩. Right: discrimination between boson sampling and uniform
sampling hypothesis using the Aaronson and Arkhipov (A&A) counter, and
between boson sampling and distinguishable sampling hypothesis using the
likelihood ratio counter. The value of each discriminator is updated every 109
samples, which corresponds to ∼20 six-photon events. In both cases, a positive
slope validates the test (see Methods).

randomly chosen using the dedicated tool in Perceval. We record
the threshold statistics of all N-photon coincidences (N ∈ [[1; 6]])
and acquire in total 340.109 samples, with a six-photon coincidence
rate reduced by the strong bunching of photons in this sampling task
down to 0.16 Hz.
To validate our experimental results, we discriminate our collected
boson sampling statistics from the uniform58 and distinguishable59
sampler hypotheses. We also reconstruct the six-photon output distribution from the sampled data and compare it with the ideal output
distribution corresponding to the chosen unitary matrix. Both distributions are plotted in Fig. 2c, from which we deduce a fidelity
1
F = ∑i √pi qi and a total variation distance (TVD) D = ∑i |pi − qi | ,

where {pi} and {qi} are the ideal and experimental output probability

2

Nature Photonics | Volume 18 | June 2024 | 603–609

distributions, respectively, with i ∈ {1, … , 924} labelling the no-collision
output configuration of the boson-sampling device53. We measure
state-of-the-art values F = (0.97 ± 0.03) and D = (0.16 ± 0.02)22,60. Details
on the measurement simulation with Perceval as well as boson sampling
with k photons lost (k ∈ [[1; 4]]) are given in Supplementary Section 6.
Our experiment marks a demonstration of boson sampling with six
single photons on an integrated photonic circuit (see Supplementary
Table 4). In contrast with previous experimental demonstrations, our
fully reconfigurable chip admits to sampling from any target unitary
matrix, a critical feature for proving a quantum-over-classical advantage in boson sampling.

607

## PDF page 6

Article

https://doi.org/10.1038/s41566-024-01403-4

Online content

GHZ
factory

Qubit 2

Heralding

0.8
0.6
0.4

References

0.2

1.

0

III
XX
X

Qubit 3

Any methods, additional references, Nature Portfolio reporting summaries, source data, extended data, supplementary information,
acknowledgements, peer review information; details of author contributions and competing interests; and statements of data and code availability are available at https://doi.org/10.1038/s41566-024-01403-4.

1.0

ZZ
I
IZ
Z
ZI
Z
YY
X
XY
Y
YX
Y

Heralding

Measured expectation value

Measure
Qubit 1

Three-qubit stabilizing operators

Fig. 3 | Heralded generation of three-photon GHZ states. Measured
expectation values of the stabilizing operators of the heralded three-photon GHZ
+
state ||GHZ3 ⟩ yielding a fidelity of FGHZ+ = 0.82 ± 0.04. The expectations values
3
are computed from 500 samples. Error bars correspond to ±1 s.d. of the photon
counting statistics.

Discussion

Near-term improvements
The above results demonstrate the suitability of the architecture for
near-term quantum computing tasks. In the short-term, the record
4 Hz rate for six photons demonstrated here can be further pushed
to 12 photons by optimizing each hardware component (see Supplementary Table 1). These optimizations could be pushed even further in
the mid-term; for instance, the current single-photon source efficiency
of 55% at the first lens can be brought to 96% (ref. 61). The number of
modes in the photonic chip can be increased while reducing photon
transmission loss16,17,57. Finally, it is anticipated that heterogeneous
integration of the different components (source, chip, detectors) will
drastically reduce interconnection losses. For the high indistinguishability, our single-photon source technology has demonstrated ≥99.5%
indistinguishability19, which would bring the two-qubit gate fidelities
close to unity62. Altogether, these technological improvements will
allow high-fidelity linear-optical computing protocols to be performed
with dozens of photons.

Scaling
Beyond noisy intermediate-scale tasks, the current platform constitutes a step towards large-scale fault-tolerant quantum computing.
By experimentally implementing quantum algorithms and protocols
on such a platform, we have demonstrated key ingredients to scale
up, specifically, high-fidelity multiphoton interference and entanglement generation on an integrated platform, which, moreover,
is robust for continuous operation63. The next steps in reducing
the overhead of probabilistic linear-optical protocols will involve
shifting to a measurement-based paradigm that relies ultimately
on the generation of large graph states12. Heralded three-photon
GHZ states are a sufficient resource to build larger entangled states
through type-II fusion13,15,64. This is the last demonstration we report
on Ascella.
We use a scheme adapted from ref. 13,65 where three out of the six
single photons are consumed to herald the generation of the
+
three-photon state ||GHZ3 ⟩ = (|000⟩ 𝕀 |111⟩)/√2 .
+
Using the stabilizer operators of ||GHZ3 ⟩ , we experimentally
+
measure a fidelity of FGHZ = 0.82 ± 0.04 (see Fig. 3 and Methods)
3
providing a reference value and benchmark of heralded GHZ state
generation.
Finally, our recent demonstration of efficient generation of linear
cluster states directly from the same quantum dot source technology23—combined with ingredients demonstrated by this platform—
could lead to additional reductions in hardware resource overheads
required for fault-tolerance66.
Nature Photonics | Volume 18 | June 2024 | 603–609

Arute, F. et al. Quantum supremacy using a programmable
superconducting processor. Nature 574, 505–510 (2019).
2. Zhu, Q. et al. Quantum computational advantage via 60-qubit
24-cycle random circuit sampling. Sci. Bull. 67, 240–245 (2022).
3. Moses, S. A. et al. A race-track trapped-ion quantum processor.
Phys. Rev. X 13, 041052 (2023).
4. Debnath, S. et al. Demonstration of a small programmable
quantum computer with atomic qubits. Nature 536, 63–66 (2016).
5. Bluvstein, D. et al. A quantum processor based on coherent
transport of entangled atom arrays. Nature 604, 451–456 (2022).
6. Zhong, H.-S. et al. Phase-programmable gaussian boson sampling
using stimulated squeezed light. Phys. Rev. Lett. 127, 180502 (2021).
7. Arrazola, J. M. et al. Quantum circuits with many photons on a
programmable nanophotonic chip. Nature 591, 54–60 (2021).
8. Wu, Y. et al. Strong quantum computational advantage using
a superconducting quantum processor. Phys. Rev. Lett. 127,
180501 (2021).
9. Madsen, L. S. et al. Quantum computational advantage with a
programmable photonic processor. Nature 606, 75–81 (2022).
10. Zhong, H.-S. et al. Quantum computational advantage using
photons. Science 370, 1460–1463 (2020).
11. Broadbent, A., Fitzsimons, J. & Kashefi, E. Universal blind
quantum computation. In 2009 50th Annual IEEE Symposium on
Foundations of Computer Science 517–526 (IEEE, 2009).
12. Raussendorf, R. & Briegel, H. J. A one-way quantum computer.
Phys. Rev. Lett. 86, 5188 (2001).
13. Li, Y., Humphreys, P. C., Mendoza, G. J. & Benjamin, S. C. Resource
costs for fault-tolerant linear optical quantum computing. Phys.
Rev. X 5, 041007 (2015).
14. Auger, J. M., Anwar, H., Gimeno-Segovia, M., Stace, T. M. &
Browne, D. E. Fault-tolerant quantum computation with
nondeterministic entangling gates. Phys. Rev. A 97, 030301 (2018).
15. Bartolucci, S. et al. Fusion-based quantum computation. Nat.
Commun. 14, 912 (2023).
16. Vigliar, C. et al. Error-protected qubits in a silicon photonic chip.
Nat. Phys. 17, 1137–1143 (2021).
17. Bao, J. et al. Very-large-scale integrated quantum graph
photonics. Nat. Photon. 17, 573–581 (2023).
18. Bombin, H. et al. Interleaving: modular architectures for
fault-tolerant photonic quantum computing. Preprint at https://
arxiv.org/abs/2103.08612 (2021).
19. Somaschi, N. et al. Near-optimal single-photon sources in the
solid state. Nat. Photon. 10, 340–345 (2016).
20. Wang, H. et al. Towards optimal single-photon sources from
polarized microcavities. Nat. Photon. 13, 770–775 (2019).
21. Tomm, N. et al. A bright and fast source of coherent single
photons. Nat. Nanotechnol. 16, 399–403 (2021).
22. Wang, H. et al. Boson sampling with 20 input photons and a
60-mode interferometer in a 1014-dimensional hilbert space.
Phys. Rev. Lett. 123, 250503 (2019).
23. Coste, N. et al. High-rate entanglement between a semiconductor spin and indistinguishable photons. Nat. Photon. 17,
582–587 (2023).
24. Gimeno-Segovia, M., Shadbolt, P., Browne, D. E. & Rudolph, T.
From three-photon Greenberger–Horne–Zeilinger states to
ballistic universal quantum computation. Phys. Rev. Lett. 115,
020502 (2015).
608

## PDF page 7

Article
25. Quandela Cloud. Quandela https://cloud.quandela.com (2022).
26. Thomas, S. E. et al. Bright polarized single-photon source based
on a linear dipole. Phys. Rev. Lett. 126, 233601 (2021).
27. Pont, M. et al. High-fidelity generation of four-photon ghz states
on-chip. Preprint at https://arxiv.org/abs/2211.15626 (2022).
28. Taballione, C. et al. A universal fully reconfigurable 12-mode quantum
photonic processor. Mater. Quantum Technol. 1, 035002 (2021).
29. Pont, M. et al. Quantifying n-photon indistinguishability with a
cyclic integrated interferometer. Phys. Rev. X 12, 031033 (2022).
30. Heurtel, N. et al. Perceval: a software platform for discrete
variable photonic quantum computing. Quantum 7, 931 (2023).
31. Knill, E., Laflamme, R. & Milburn, G. J. A scheme for efficient
quantum computation with linear optics. Nature 409, 46–52 (2001).
32. Nielsen, M. A & Chuang, I. Quantum Computation and Quantum
Information (Massachusetts Institute of Technology, 2002).
33. Magesan, E., Gambetta, J. M. & Emerson, J. Characterizing
quantum gates via randomized benchmarking. Phys. Rev. A 85,
042311 (2012).
34. Dankert, C., Cleve, R., Emerson, J. & Livine, E. Exact and
approximate unitary 2-designs and their application to fidelity
estimation. Phys. Rev. A 80, 012304 (2009).
35. Clément, A., Heurtel, N., Mansfield, S., Perdrix, S. & Valiron, B.
LOv-Calculus: a graphical language for linear optical quantum circuits.
In Proc. 47th International Symposium on Mathematical Foundations
of Computer Science (MFCS) Vol. 241 (Eds Szeider, S. et al.) 35:1–35:16
(Schloss Dagstuhl - Leibniz-Zentrum für Informatik, 2002).
36. Mohseni, M., Rezakhani, A. T. & Lidar, D. A. Quantum-process
tomography: resource analysis of different strategies. Phys. Rev. A
77, 032322 (2008).
37. Crespi, A. et al. Integrated photonic quantum gates for
polarization qubits. Nat. Commun. 2, 566 (2011).
38. Zhang, M. et al. Supercompact photonic quantum logic gate on a
silicon chip. Phys. Rev. Let. 126, 130501 (2021).
39. Li, M. et al. On-chip path encoded photonic quantum toffoli gate.
Photon. Res. 10, 1533–1542 (2022).
40. Peruzzo, A. et al. A variational eigenvalue solver on a photonic
quantum processor. Nat. Commun. 5, 4213 (2014).
41. Bravyi, S., Gambetta, J. M, Mezzacapo, A. & Temme, K. Tapering
off qubits to simulate fermionic hamiltonians. Preprint at https://
arxiv.org/abs/1701.08213 (2017).
42. McClean, J. R. et al. Openfermion: the electronic structure package
for quantum computers. Quantum Sci. Technol. 5, 034014 (2020).
43. Lee, D. et al. Error-mitigated photonic variational quantum
eigensolver using a single-photon ququart. Optica 9, 88–95 (2022).
44. Zhang, Y. et al. Variational quantum eigensolver with reduced
circuit complexity. npj Quantum Inf. 8, 96 (2022).
45. Kandala, A. et al. Error mitigation extends the computational
reach of a noisy quantum processor. Nature 567, 491–495 (2019).
46. Nam, Y. et al. Ground-state energy estimation of the water
molecule on a trapped-ion quantum computer. npj Quantum Inf.
6, 33 (2020).
47. Goings, J., Zhao, L., Jakowski, J., Morris, T. & Pooser, R. Molecular
symmetry in VQE: a dual approach for trapped-ion simulations of
benzene. Preprint at https://arxiv.org/abs/230 (2023).
48. McClean, J. R., Romero, J., Babbush, R. & Aspuru-Guzik, A. The
theory of variational hybrid quantum-classical algorithms. New J.
Phys. 18, 023023 (2016).
49. Gan, B. Y., Leykam, D. & Angelakis, D. G. Fock state-enhanced
expressivity of quantum machine learning models. EPJ Quantum
Technol. 9, 16 (2022).
50. Fisher, R. A. The use of multiple measurements in taxonomic
problems. Ann. Eugenic. 7, 179–188 (1936).

https://doi.org/10.1038/s41566-024-01403-4
51. Havlíček, V. et al. Supervised learning with quantum-enhanced
feature spaces. Nature 567, 209–212 (2019).
52. Bartkiewicz, K. et al. Experimental kernel-based quantum machine
learning in finite feature space. Sci. Rep. 10, 12356 (2020).
53. Aaronson, S. & Arkhipov, A. The computational complexity of
linear optics. In Proc. 43rd Annual ACM Symposium on Theory of
Computing 333–342 (ACM, 2011).
54. Zhong, H.-S. et al. 12-Photon entanglement and scalable scattershot
boson sampling with optimal entangled-photon pairs from
parametric down-conversion. Phys. Rev. Lett. 121, 250505 (2018).
55. Paesani, S. et al. Generation and sampling of quantum states of
light in a silicon chip. Nat. Phys. 15, 925–929 (2019).
56. Gao, Jun et al. Experimental collision-free dominant boson
sampling. Preprint at https://arxiv.org/abs/1910.11320 (2019).
57. Hoch, F. et al. Reconfigurable continuously-coupled 3D photonic
circuit for boson sampling experiments. npj Quantum Inf. 8, 55 (2022).
58. Aaronson, S. & Arkhipov, A. Bosonsampling is far from uniform.
Quantum Info. Comput. 14, 1383–1423 (2014).
59. Spagnolo, N. et al. Experimental validation of photonic boson
sampling. Nat. Photon. 8, 615–620 (2014).
60. Wang, H. et al. Toward scalable boson sampling with photon loss.
Phys. Rev. Lett. 120, 230502 (2018).
61. Wang, B.-Y., Denning, E. V., Gür, U. M., Lu, C.-Y. & Gregersen, N.
Micropillar single-photon source design for simultaneous near-unity
efficiency and indistinguishability. Phys. Rev. B 102, 125301 (2020).
62. Ralph, T. C., Langford, N. K., Bell, T. B. & White, A. G. Linear optical
controlled-not gate in the coincidence basis. Phys. Rev. A 65,
062324 (2002).
63. Maring, N. et al. One nine availability of a photonic quantum
computer on the cloud toward HPC integration. In 2023 IEEE
International Conference on Quantum Computing and Engineering
(QCE) Vol. 2, 112–116 (IEEE, 2023).
64. Varnava, M., Browne, D. E. & Rudolph, T. How good must single
photon sources and detectors be for efficient linear optical
quantum computation? Phys. Rev. Lett. 100, 060502 (2008).
65. Gouriou, C. Design and Fabrication of an Integrated Photonic
Circuit for Producing a Maximally-Entangled Three-Photon State.
Politecnico di Milano. MSc Thesis, Polytecnico Milano (2019).
66. Paesani, S. & Brown, B. J. High-threshold quantum computing by
fusing one-dimensional cluster states. Phys. Rev. Lett. 131, 120603
(2023).
67. Kieling, K., O’Brien, J. L. & Eisert, J. On photonic controlled phase
gates. New J. Phys. 12, 013003 (2010).
Publisher’s note Springer Nature remains neutral with regard to
jurisdictional claims in published maps and institutional affiliations.
Open Access This article is licensed under a Creative Commons
Attribution 4.0 International License, which permits use, sharing,
adaptation, distribution and reproduction in any medium or format,
as long as you give appropriate credit to the original author(s) and
the source, provide a link to the Creative Commons licence, and
indicate if changes were made. The images or other third party
material in this article are included in the article’s Creative Commons
licence, unless indicated otherwise in a credit line to the material. If
material is not included in the article’s Creative Commons licence
and your intended use is not permitted by statutory regulation
or exceeds the permitted use, you will need to obtain permission
directly from the copyright holder. To view a copy of this licence, visit
http://creativecommons.org/licenses/by/4.0/.
© The Author(s) 2024

Quandela, Massy, France. 2Université Paris-Saclay, CNRS, Centre de Nanosciences et de Nanotechnologies, Palaiseau, France. 3These authors
contributed equally: Andreas Fyrillas, Mathias Pont and Edouard Ivanov.
e-mail: jean.senellart@quandela.com; niccolo.somaschi@quandela.com

1

Nature Photonics | Volume 18 | June 2024 | 603–609

609

## PDF page 8

Article

Methods

Architecture
Ascella is accessible remotely via a cloud service25. Tasks can be dispatched either to Ascella, to a perfect simulator, or to a noisy simulator
through a generic scheduler handling multiple users' access limitations
and task prioritization. Following a compilation and transpilation process, Ascella then sets the demultiplexer configuration and the photonic
circuit phases to apply the required unitary matrix to the input state. For
applications such as quantum machine learning, for which each training
data sample corresponds to a task, users can prepare and send a batch
of tasks that will execute sequentially on the QPU with fast incremental
chip reconfiguration and without any communication overhead.

Single-photon source
The single-photon source is a single InAs quantum dot deterministically embedded in the centre of a micropillar19. The sample was
fabricated from a wafer grown by molecular beam epitaxy and is composed of a λ-cavity and two distributed Bragg reflectors made of GaAs/
Al0.95Ga0.05As λ/4 layers with 36 (18) pairs for the bottom (top); the top
(bottom) distributed Bragg reflectors are gradually p(n)-doped and
electrically contacted.

Photonic circuit
The photonic integrated circuit is a 12 mode universal Clements style
interferometer, including 126 phase shifters and 1,323 dB directional
couplers. The chip size is 20 × 20 mm2. The circuit is etched on stochiometric silicon nitride waveguides with the Triplex technology designed
for 925 nm wavelength. Further details on the system and fabrication
technology can be found in refs. 28,68.
The rectangular universal interferometer layout (see Fig. 1a) is
ideally based on balanced directional couplers (that is 50% reflectivity).
Experimentally, we observe reflectivities with average values of
56.7(6)% for our chip at the operation wavelength of 928 nm. The
random error stems from the fabrication tolerance and the systematic
error from the wavelength dependency. These errors reduce the range
of implementable 12 × 12 unitary matrices69,70 and, if not compensated
for, affect the fidelity of the implemented unitary matrix to the target
unitary matrix. To address these limitations, we designed a custom
compilation and transpilation process that converts with high-fidelity
user-provided photonic circuits, unitary matrices or gate-based circuits
into interferometer phase shift values (compilation) then into voltages
to apply on the chip phase shifters (transpilation). The compilation
process features a global optimization step executed on a CPU that
simultaneously fine-tunes all the phase shifts to enhance matrix fidelity, thereby mitigating the impact of reflectivity errors. Subsequently,
the transpilation process calculates the voltages to apply on the chip
phase shifters while compensating for thermal cross-talk. To achieve
this, it solves the phase-voltage relation ϕ⃗ = AV ⃗ ⊙2 𝕀 b ⃗ that models the
behaviour of the thermo-optic phase shifters, where the vector ϕ⃗
contains all 126 physical phase shifts, V ⃗ the 126 applied voltages and ⊙2
represents element-wise squaring. Off-diagonal elements of the
126 × 126 matrix A represent thermal cross-talk between phase shifters
To find suitable values for A and b ⃗ , we engineered a machine
learning-based photonic chip characterization process that optimizes
their values, constituting more than 16,000 free parameters to determine. The same process also estimates individual directional coupler
reflectivities and relative output losses (see Supplementary Section 4
for values). This process offers a seven-fold improvement on the transpilation ( ϕ⃗ to V ⃗ process) over more standard characterization techniques involving interference-fringe measurements.
We benchmark the transpilation process by applying 300 random
phase configurations on the photonic chip and measuring the photon
countrates at the 12 outputs. We compare them to a simulation of the chip
which is taken into account the estimated directional coupler reflectivities and relative output losses (see Supplementary Section 4 for values).
Nature Photonics

https://doi.org/10.1038/s41566-024-01403-4

We quantify the difference between the measured and simulated values
using the TVD. At 925 nm, with a standard characterization of the chip
based on interference fringes measurements28, the TVD evaluated on
the configurations is (21 ± 11)%, where the error bar is the standard deviation of the dataset. At the operating wavelength of our single-photon
source (928 nm), with our machine learning process, we achieve a TVD
of (3.0 ± 1.3)%, greatly improving our control over the chip. The relative
variation on the obtained average TVD between successive benchmarkings is of the order of 3%, showing repeatability of the obtained value. The
full compilation and transpilation processes achieve an average fidelity
of F = 99.7 ± 0.08 following the fidelity evaluation procedure from ref. 28.

Variational quantum eigensolver
The ansatz for the VQE algorithm implements the gate-based circuit
shown in Fig. 2a which consists of a generic two-qubit state generator.
It comprises single-qubit rotations and a CNOT gate62. This is implemented on six modes (modes 1 to 6) comprising two path-encoded
qubits and two extra modes for the postselected Ralph CNOT. Arbitrary
rotations are implemented via tunable Mach–Zehnder interferometers
with thermo-optic phase shifters. Extra phase shifters are used to
mitigate systematic errors in the reflectivity of beamsplitters and to
converge faster to the ground state energy. On average, an entire VQE
experiment for H2 takes about 30 min per bond length with 10,000
post-processed two-photon samples (that is the time to construct
Supplementary Fig. 15). This time comprises of the actual experimental time and the classical pre- and post-processing. For the final run at
ropt to reach chemical accuracy, gathering 400,000 post-processed
two-photon samples for each iteration takes 4 h 30 min.

Boson sampling
Two statistical tests are used to discriminate the experimental data
against the uniform sampler and distinguishable particle hypotheses.
The A&A counter and the likelihood ratio counter, respectively, are
increased or decreased according to a likelihood ratio test. The A&A
counter A is defined as57,58
n 2

A 𝕀 1 if 𝒫𝒫 𝒫 ( )
⎧
⎪ k−1
m
Ak ∶=
2
⎨
⎪ A − 1 if 𝒫𝒫 𝒫 ( n )
⎩ k−1
m

where n and m are, respectively, the number of photons and optical
modes, and 𝒫𝒫 ∶= ∏i ∑j |Uij |2, where i labels the modes in which photons
are detected, j the input modes and U is the unitary sampling matrix.
The likelihood ratio counter C is defined as57,59
n 2

C 𝕀 1 if ℒ 𝒫 ( )
⎧
⎪ k−1
m
Ck ∶=
2
⎨
⎪ C − 1 if ℒ 𝒫 ( n )
⎩ k−1
m
q

where ℒ ∶= p with q: = ∣Perm(U(ij))∣2, p: = ∣Perm(∣U(ij)∣2) and U(ij) denoting
the sub-matrix restricted to the input labels i and output labels j.

Photon-based quantum neural network
We build the ansatz of our variational quantum classifier using
modes 3 to 7 of Ascella. We input three photons into the chip, in modes
3, 5 and 7. We use 32 of the reconfigurable thermo-optic phase shifters as the variational parameters, and 4 phase shifters in the middle
of the chip for the data encoding. We use extra modes for pseudo
photon-number resolution: by setting four phase shifters to π/2 in
the final layer of the chip, we redirect a portion of the photons from
modes 3 and 7 into modes 1, 2 and 8, 9 respectively. For the classical
optimization process, we use a see-saw approach based on Gaussian
processes and Nelder–Mead optimizers. More details regarding the
circuit ansatz, model definition, pseudo photon-number resolution
and the optimization methods are in Supplementary Section 7.

## PDF page 9

Article

https://doi.org/10.1038/s41566-024-01403-4

Heralded three-photon GHZ on-chip generation
The generation of a path-encoded three-photon GHZ state is characterized with three reconfigurable integrated Mach–Zehnder interferometers (MZIi, i = 1, 2, 3). The layout of the optical circuit is provided in
the Supplementary Section 9. Measuring six photons with threshold
detectors, the output state of the circuit is given by65
|Out⟩ =

1
16

−

−

(− |GHZ3 ⟩ |h1 ⟩ 𝕀 |GHZ3 ⟩ [|h4 ⟩ 𝕀 |h6 ⟩ 𝕀 |h7 ⟩]
+

+

−i ||GHZ3 ⟩ |h8 ⟩ 𝕀 i ||GHZ3 ⟩ [|h2 ⟩ 𝕀 |h3 ⟩ 𝕀 |h5 ⟩]) .

Acknowledgements

±

+

We target the state ||GHZ3 ⟩, where ||GHZ3 ⟩ = (|000⟩ ± |111⟩)/√2 , which is
obtained by conditioning the analysis of the state on the detection of
one of the heralding states |h2 ⟩, |h3 ⟩, |h5 ⟩ and |h8 ⟩.
The heralding channels signal the generation of a specific GHZ
+
state. The heralding conditions for the generation of ||GHZ3 ⟩ are
|h2 ⟩ = |02 13 04 17 18 09 ⟩
⎧
⎪|
⎪ h3 ⟩ = |12 03 04 17 08 19 ⟩
⎨ |h5 ⟩ = |12 03 14 07 18 09 ⟩
⎪
⎪
⎩ |h8 ⟩ = |02 13 14 07 08 19 ⟩

where |0i ⟩ (|1i ⟩) correspond to detecting 0 (1) photons in mode i (modes
are labelled from 1 to 12 from top to bottom).
+
The state ||GHZ3 ⟩ is a stabilizer state, and therefore can uniquely
be expressed in terms of its stabilizers71.
1
+
||GHZ+
|
S,
3 ⟩ ⟨GHZ3 | = ∑
|𝒮𝒮𝒮 i

(2)

Si ∈𝒮𝒮

+

+

where Si is a stabilizer of ||GHZ3 ⟩, 𝒮𝒮 is the stabilizer group of ||GHZ3 ⟩ and
|𝒮𝒮𝒮 is the number of elements of 𝒮𝒮. The fidelity of some experimental
+
implementation ρ of ||GHZ3 ⟩ is given by
+

+

FGHZ+3 = Tr( ||GHZ3 ⟩ ⟨GHZ3 || ρ),
+

+

Plugging the expansion of ||GHZ3 ⟩ ⟨GHZ3 || into FGHZ+3 and using linearity
of the trace, one obtains
FGHZ+3 =

1
1
∑ Trace(Si ρ) =
∑ 𝒫 Si > .
|𝒮𝒮𝒮 S ∈𝒮𝒮
|𝒮𝒮𝒮 S ∈𝒮𝒮
i

71. Hein, M. et al. Entanglement in graph states and its applications.
In Proceedings of the International School of Physics “Enrico Fermi”
115–218 (IOS Press, 2006).
72. Cao, H. et al. A photonic source of heralded GHZ states. Preprint
at https://arxiv.org/abs/2308.05709 (2023).
73. Chen, S. et al. Heralded three-photon entanglement from a
single-photon source on a photonic chip. Preprint at https://arxiv.
org/abs/2307.02189 (2023).

i

The fidelity of the heralded state to the target state is characterized
on Ascella using this equation, where Si ∈ {III, XXX, ZZI, IZZ, ZIZ, − YYX,
− XYY, − YXY}, the stabilizer operators of the target state, are experimentally accessed through the three-qubit operators XXX, ZZZ, YYX, XYY
and YXY. Note that after the submission of this manuscript, two works
reported on the heralded generation of three-photon GHZ states72,73.

Data availability

We would like to thank A. White for fruitful feedback, R. Osellame and
his team for valuable interactions on the generation of heralded GHZ
states, and J.J. Dormard, G. Parent and J. Herlent for their support
in the electronic modules. We acknowledge I. Maillette de Buy
Wenniger, V. Guichard, F. Hoch and A. Henry for preliminary work
on the classification experiment, and G. de Gliniasty for discussions
on the Toffoli gate scheme. This work has received funding from the
European Union’s Horizon 2020 Research and Innovation Programme
QUDOT-TECH under the Marie Sklodowska Curie Grant Agreement No.
861097, from the European Union’s Horizon 2020 FET OPEN project
QLUSTER (grant no. 862035), from the European Commission as
part of the EIC accelerator program under the grant SEPOQC (grant
agreement no. 190188855), and from BPI France Concours Innovation
PIA3 projects DOS0148634/00 and DOS0148633/00—Reconfigurable
Optical Quantum Computing (ROQC), from the Plan France 2030
through the project ANR-22-PETQ-0011.

Author contributions

The quantum dot single photon source was fabricated by
A.P., N. Margaria, W.H., A.L., I.S., S.B. and T.H.A., and its optical
characterization was performed by P. Stepanov, A.F., E.I., M.P. and
M.B. O.A. and A. Brieussel integrated all of the hardware components
under the close supervision of N. Maring. A.F., N. Maring, N.B. and
J.S. developed the machine-learned chip control. E.I., A.F. and
M.P. developed the software layer controlling all instruments and
realizing the remote tasks. M.V. architected the software stack, E.B.
implemented the control code within Perceval, and A. Baert wrote
the interface between Perceval and the cloud worker. R.M., S.C.W.
P. Sinnott and J.S. conducted the gate benchmarking. M.P. and R.M.
ran the boson sampling task. M.P. implemented the six-photon
indistinguishability test and heralded three-photon GHZ state
generation. A.S. and D.A.F. realized the classification experiment,
P. Sinnott and P.-E.E. defined and realized the VQE. S.M. supervised
and coordinated the theoretical work. P. Senellart and N.S. guided the
source fabrication process and hardware integration. J.S. coordinated
the full assembly of the hardware and software. N.S. supervised the
overall project; M.P., P.-E.E., A.S., R.M., N.M., P. Sinnott, A.F., S.C.W.,
N.S., N.B, S.M., J.S. and P. Senellart wrote the paper.

The data generated as part of this work are available on reasonable
request from the corresponding authors.

Competing interests

Code availability

Additional information

References

Correspondence and requests for materials should be addressed to
Jean Senellart or Niccolo Somaschi.

The code used to run the presented applications is available at https://
github.com/Quandela/Ascella.

68. Roeloffzen, C. G. H. et al. Low-loss Si3N4 triplex optical
waveguides: technology and applications overview. IEEE J. Sel.
Top. Quantum Electron. 24, 1–21 (2018).
69. Burgwal, R. et al. Using an imperfect photonic network to
implement random unitaries. Opt. Express 25, 28236–28245 (2017).
70. Russell, N. J., Chakhmakhchyan, L., O’Brien, J. L. & Laing, A. Direct
dialling of haar random unitary matrices. New J. Phys. 19, 033007
(2017).
Nature Photonics

N.S. and P. Senellart are co-founders of Quandela.

Supplementary information The online version contains supplementary
material available at https://doi.org/10.1038/s41566-024-01403-4.

Peer review information Nature Photonics thanks Leong-Chuan Kwek,
Xian-Min Jin and the other, anonymous, reviewer(s) for their
contribution to the peer review of this work.
Reprints and permissions information is available at
www.nature.com/reprints.
