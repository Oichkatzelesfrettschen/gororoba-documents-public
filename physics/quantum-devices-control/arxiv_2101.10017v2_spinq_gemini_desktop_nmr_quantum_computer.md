Source: https://arxiv.org/abs/2101.10017v2
PDF sha256: 622a31b12a7a8e6b0fef731ca652e31fba5bbff21875c77887d26f8127e92ec6
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of arxiv_2101.10017v2_spinq_gemini_desktop_nmr_quantum_computer.pdf

Transcription of `arxiv_2101.10017v2_spinq_gemini_desktop_nmr_quantum_computer.pdf` in this directory, 14 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-14 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

SpinQ Gemini: a desktop quantum computer for education and research
Shi-Yao Hou,1, 2, 3 Guanru Feng,1 Zipeng Wu,3, 4 Hongyang Zou,1 Wei Shi,1 Jinfeng Zeng,3 Chenfeng Cao,3 Sheng Yu,1
Zikai Sheng,1 Xin Rao,1 Bing Ren,1 Dawei Lu,5 Junting Zou,1 Guoxing Miao,6, 1, ∗ Jingen Xiang,1, † and Bei Zeng3, ‡

arXiv:2101.10017v2 [quant-ph] 22 Feb 2021

2

1
Shenzhen SpinQ Technology Co., Ltd., Shenzhen, China
College of Physics and Electronic Engineering & Center for Computational Sciences, Sichuan Normal University, Chengdu, China
3
Department of Physics, The Hong Kong University of Science and Technology, Clear Water Bay, Kowloon, Hong Kong
4
Department of Physics, Tsinghua University, Beijing, China
5
Department of Physics, Southern University of Science and Technology, Shenzhen, China
6
Institute for Quantum Computing, University of Waterloo, Waterloo, Ontario, Canada
(Dated: February 23, 2021)

SpinQ Gemini is a commercial desktop quantum computer designed and manufactured by SpinQ Technology. It is an integrated hardware-software system. The first generation product with two qubits was launched in
January 2020. The hardware is based on NMR spectrometer, with permanent magnets providing ∼ 1 T magnetic field. SpinQ Gemini operates under room temperature (0-30◦ C), highlighting its lightweight (55 kg with a
volume of 70×40×80 cm3 ), cost-effective (under 50k USD), and maintenance-free. SpinQ Gemini aims to provide real-device experience for quantum computing education for K-12 and at the college level. It also features
quantum control design capabilities that benefit the researchers studying quantum control and quantum noise.
Since its first launch, SpinQ Gemini has been shipped to institutions in Canada, Taiwan and Mainland China.
This paper introduces the system of design of SpinQ Gemini, from hardware to software. We also demonstrate
examples for performing quantum computing tasks on SpinQ Gemini, including one task for a variational quantum eigensolver of a two-qubit Heisenberg model. The next generations of SpinQ quantum computing devices
will adopt models of more qubits, advanced control functions for researchers with comparable cost, as well as
simplified models for much lower cost (under 5k USD) for K-12 education. We believe that low-cost portable
quantum computer products will facilitate hands-on experience for teaching quantum computing at all levels,
well-prepare younger generations of students and researchers for the future of quantum technologies.

I.

INTRODUCTION

SpinQ Gemini is a commercial desktop quantum computer
designed and manufactured by SpinQ Technology [1], and the
first generation product with two qubits was launched in January 2020. It is an integrated hardware-software system as
shown in Fig. 1: the left figure shows the exterior look of the
device, with a dimension of 70 × 40 × 80 cm3 , and a weight of
55kg; the right figure shows the user interface software SpinQuasar.
The hardware part of Gemini is based on NMR spectrometer. NMR was among the very first systems developed for
quantum computing [2–8]. Despite its limitations on scalability, a lot of pioneer research and techniques for quantum computing were first demonstrated in NMR systems [9–
21]. Notably, many quantum control techniques developed
in NMR can be readily applied to other quantum computing
platforms [8, 22–30] .
Traditional NMR quantum computing is performed on
commercial spectrometers with a superconducting magnet.
Those spectrometers are expensive (almost 1 million USD),
large (can be as high as ∼3 meters), and need to work in
specially designed labs. They also require regular liquid nitrogen and helium refills for maintenance. These issues on
cost, weight, volume and extreme physical conditions also in
general exist on other systems for quantum computing, mak-

∗ guo-xing.miao@uwaterloo.ca
† jxiang@spinq.cn
‡ zengb@ust.hk

ing them hard to be accessible for users in real life, but instead with only possible access on cloud, such as IBM Q [31],
IonQ [32] and Rigetti [33]. As an example, superconducting
qubits need to work in dilution fridges which usually cost almost 1 million USD. Similar as the NMR systems, they require special lab conditions and are not portable. Furthermore, special training is needed for operations of dilution
fridges [34–40].
With the development of permanent magnet technology in
recent years [41], it is possible to bring down the size and
cost of NMR spectrometers [42–46]. This then makes the
NMR technology an ideal choice for building portable quantum computers. By using a permanent magnet providing 1
T magnetic fields, SpinQ Gemini highlights its lightweight
(55 kg with a volume of 70×40×80 cm3 ) and cost-effective
(under 50k USD) features, and maintenance-free, making it
portable almost like a desktop PC.
Customised quantum algorithm circuit design and programming are supported on SpinQ Gemini using its software SpinQuasar (Fig. 1). SpinQ Gemini also provides demonstrations of > 10 famous quantum algorithms, such as Deutsch
algorithm [47], Grover algorithm [48, 49], and HHL algorithm [50]. It also has build-in teaching examples for quantum mechanic, such as Rabi oscillation observation and decoherence time measurement. Gemini not only provides a very
friendly platform for non-specialists who aim to learn quantum computing basics and quantum programming fast, but
also serves as a powerful tool for quantum computing related
research.
In this paper, we introduce the system of the first generation SpinQ Gemini. In Sec. II, we discuss the system design,

## PDF page 2

2

Figure 1. The photo of Gemini (left) and the homepage of S PIN Q UASAR (right). The Gemini connects with a personal computer (PC) installed
with S PIN Q UASAR. S PIN Q UASAR provides an interface for the users to manipulate the desktop quantum computer.

from hardware to software. In Sec. III, we discuss how to perform quantum computing with SpinQ Gemini. We give two
concrete examples of quantum computing tasks performed on
SpinQ Gemini, one on the measurement of geometric phase
of mixed state in Sec. IV, and the other on a variational quantum eigensolver for a two-qubit Heisenberg model in Sec. V.
A discussion on future plans of next generations products will
follow in Sec. VI.
We believe that low-cost portable quantum computer products will facilitate hands-on experience for teaching quantum
computing at all levels, well-prepare younger generations for
the future of quantum technologies. It will also be accessible to a wider range of researchers to operate under real world
conditions for quantum computers, benefiting them for further
studies on quantum control and quantum noise.
II.

SYSTEM

The overall schematic diagram is shown in Fig. 2. Gemini
is composed of a PC with S PIN Q UASAR, a control system on
the master board, a radio frequency (RF) system, a temperature control module, a pair of two permanent magnets, a field
shimming system, and a tube of sample.
The PC with S PIN Q UASAR and the master board together
realize the algorithms and interfaces to all the functions. The
magnets provide static stable magnetic field. The field shimming system and temperature control system together make
the field stable and homogeneous enough for nuclear magnetic
resonance as well as quantum computing. The RF system provides generation, modulation, amplification, transmission, detection and reception of the RF pulses so that we can control
and measure the quantum system.
The PC with S PIN Q UASAR and the master board altogether
realized the software part. The modules are shown in Fig. 3.
The software S PIN Q UASAR provide an interface for a user to
communicate with the quantum computer Gemini. The master board, of which the core device is an FPGA, realizes all
the algorithms to control the pulses (hence control the quantum state), the temperature and shimming of the field (hence

generate a stable homogeneous field). S PIN Q UASAR and the
master board communicate with each other through USB.
A.

SpinQuasar

The left half of Fig. 3 shows the structure of S PIN Q UASAR.
It is composed of five modules: the quantum computing module, the NMR spectroscopy module, the instrument calibration module, the task management module and the dynamic
library module. These modules can be easily accessed from
the homepage of S PIN Q UASAR, as shown in the right column
of Fig. 1.
The quantum computing module provides an interface of
a two-qubit quantum computer and will be discussed later in
Sec. III.
The NMR spectroscopy module provides an interface of direct accessing to the 1 H and 31 P nuclear magnetic resonance
signal of our sample. It provides the direct control of the pulse
parameters on the two nuclei. Also, it provides both the free
induction decay (FID) signals and the spectra after fast Fourier
transform (FFT). This interface provides a good demonstration of a modern FFT based NMR spectrometer.
The instrument calibration module provides an interface for
users to calibrate the parameters of the spectrometer, such as
field shimming, phase calibration, and the temperature control
for the system.
Our quantum computer also supports cloud quantum computing. For cloud quantum computing, the tasks are managed
by the task management module. Also, to support more complicated control, such as the variational quantum eigensolver
(VQE) which requires adjusting the parameters of the pulses,
we provide the APIs for programmable control, and embedded these into the dynamic library.
B.

Master board

The master board integrates the digital parts of the hardware, including an FPGA, an analog-digital converter (ADC)

## PDF page 3

3

Figure 2. The overview of the schematic diagram of Gemini system and the interface S PIN Q UASAR. The master board equipped with an
FPGA, provides the control logic of Gemini. S PIN Q UASAR communicates with FPGA through USB so that the user can access Gemini. The
magnets, together with the temperature control unit and the field shimming system provide a stable static homogeneous magnetic. The RF
module provides the function required to control and measure the qubits.

C.

Figure 3. Software structure. The software could be divided into
two parts: one (the left block) we called S PIN Q UASAR provides an
interface for users with access to all the functions of Gemini, the
other (the right block) realizes the algorithms and controls required
for Gemini to function properly. These two parts communicate with
each other through USB.

The permanent magnets provide a stable static homogeneous magnetic field, which split the nuclei with spin-half into
two energy levels and therefore become a qubit. The permanent magnets are two NdFeB plates. The field generated is ∼1
Tesla. The field near the center of the two magnets is roughly
homogeneous: the homogeneity generated by such magnets
can reach a level of ∼20 ppm. Compared with modern commercial NMR spectrometers, of which the magnet is generated by the superconducting coil which requires a large cryogenic storage dewar and regular refilling of liquid helium and
nitrogen, the magnets of Gemini works under room temperature, hence maintenance free and portable. The disadvantages
are that the magnitude of the magnets could only reach about 2
T, and the magnetic field is highly sensitive to the temperature
of the magnets themselves.

D.

and a digital-analog converter (DAC). The digital parts, as
shown in the right block of Fig. 3, altogether realize the algorithms required to generate the RF pulse, measure the readout
signal, control the temperature and shimming. These algorithms will be described further in the introduction of each
module. The ADC converts the readout signal from the RF
part as measurement, while the DAC generate the initial RF
signal for state manipulation

Magnets

Sample

The sample we used is Dimethylphosphite ((CH3 O)2 PH)
molecules . The 31 P and 1 H atom are connected directly and
provide a two-qubit quantum processor. Both 31 P and 1 H nuclei have a 1/2-spin, and therefore have two energy levels.
The Lamor frequency of 31 P and 1 H in 1 T magnetic field are
17.2 MHz and 42.6 MHz, respectively. The structure and the
parameters of the sample are listed in (Fig. 4).

## PDF page 4

4

Figure 4. The molecule structure (left) and its parameter table (right).
The J coupling between the 1 H and 31 P nuclear spins is 697.4 Hz.
The control pulses are on resonance with 1 H and 31 P spins and thus
their frequency offsets are both 0 Hz. The spin Hamiltonian is H0 =
πJσzH σzP /2, where J = 697.4Hz.

E.

RF pulse generation

The states of the nuclei could be manipulated by irradiating electro-magnetic waves (pulses) with frequencies close to
there Larmor frequency (the physics behind this will be described later). Since the Larmor frequencies of the two nuclei lie in the range of RF range, an RF system is designed
and manufactured to operate the quantum state and realize the
quantum gates.

Figure 5. RF pulse generation and signal readout. The upper half
shows how an arbitrary wave is generated. After the wave is generated, it is power amplified and sent to the control coil (see Fig. 2) so
that the quantum state can be manipulated. After the RF pulse irradiation, the electro-magnetic signal induced during spin relaxation is
picked up by the coil, and then is sent to the preamplifier. After the
signal is amplified, it is sent to the ADC and processed by the master
board.

Figure 6. Temperature control. The temperature control is realized
by a famous feedback algorithm: the PID algorithm. The temperature probe picks the temperature signal and send it to the FPGA. The
FPGA decides what to do next according to the temperature signal
and then controls the power of the heating module accordingly.

G.

The homogeneity of the static magnetic field generated by
the permanent magnets is ∼20 ppm, which is too large. To
compensate this inhomogeneity, we designed a field shimming system to reduce the homogeneity to less than ∼ 1 ppm.
The best homogeneity could be reached to ∼ 0.3 ppm. As a
comparison, the homogeneity of a commercial nuclear magnetic spectrometer with a superconducting magnet is ∼ 0.01
ppm.

Figure 7. Shimming. Currently, the field shimming is accomplished
by measuring the FWHM of the hydrogen signal. It is also a feedback
algorithms by reading the FWHM information of the hydrogen signal
and adjust the current of the shimming coils.

III.
F.

Temprature control

The field generated by the permanent magnets is highly
sensitive to the temperature of the permanent magnets themselves. Therefore, a temperature control system is required
to guarantee that the field does not drift following the room
temperature.

Field Shimming

QUANTUM COMPUTATION
A.

The spin system

Gemini contains two qubits which are the two connected
P and 1 H nuclear spins in Dimethylphosphite ((CH4 O)2 PH)
molecules (Fig. 4). The molecules are placed in the center
of the parallel permanent magnets. The 31 P and 1 H larmor
frequencies are 17.2 MHz and 42.6 MHz, respectively. The

31

## PDF page 5

5
31

P spin has a T1 and T2 of 7.2 s and 0.5 s, respectively. The
H spin has a T1 and T2 of 4 s and 0.3 s, respectively. The
J coupling between the two spins is 697.4 Hz. The control
pulses are on resonance with 1 H and 31 P spins and thus their
frequency offsets are both 0 Hz. The spin Hamiltonian in the
rotating frame is
1

H0 = 2πJIzH IzP =

π H P
Jσ σ ,
2 z z

where J = 697.4 Hz.
B.

(1)

a liquid-state NMR system is subject to Boltzmann distribution and at room temperature can be expressed as follow:
ρeq =

1
e−Hs /kB T
1
≈ n I ⊗n + Σnk=1 ϵk σzk .
−H
/k
T
s
B
2
2
Tr(e
)

(4)

Here, Hs is the spin Hamiltonian in the lab frame, and n is
the number of qubits. The part Σnk=1 12 ϵk σzk gives NMR signals. At room temperature ϵ ∼ e−5 is small and thus this is a
highly mixed state. To implement quantum computation, researchers [2] proposed to use PPS as the initial state which has
the following form,

The gate set

ρpps =

1 − η ⊗n
I + η|ψ⟩⟨ψ|.
2n

(5)
Single-qubit 90 degree rotation gates can be realized using
square pulses of 20us and 10us for 31 P and 1 H, respectively.
|ψ⟩ is a pure state. The PPS above has the same unitary dyThe hardware-level pulse design and engineering are available
namics and observable effects as the pure state |ψ⟩ except for
in later versions of Gemini which provide an arbitrary wavethe factor η. PPS is widely used in NMR quantum computaform generation function to users. In the current paper, all
tion.
quantum gates are realized using square pulses which are resGemini utilizes the relaxation method in Ref. [51] to preonant with 1 H or 31 P and combined with free evolution. The
pare the two-qubit PPS starting from the thermal equilibrium
available quantum gates contain single-qubit and two-qubit
state. As shown in Fig. 8, the first four pulses realize a basis
gates. The single-qubit gates are as follows:
permutation gate which can be expressed as
(
)
(
)
(
)
⎛
⎞
0 1
0 −i
1 0
−i 0 0 0
X = σx =
, Y = σy =
, Z = σy =
,
1 0
i 0
0 −1
⎜ 0 0 0 −i⎟
Upermute = ⎝
.
(6)
π
π
0 −1 0 0 ⎠
−i π
σ
−i
σ
−i
σ
x
y
z
X90 = e 4 , Y 90 = e 4 , Z90 = e 4 ,
0 0 1 0
β
γ
α
Rx = e−i 2 σx , Ry = e−i 2 σy , Rz = e−i 2 σz ,
(
)
(
)
Upermute permutes the basis |01⟩, |10⟩ and |11⟩ and leaves
1 1 1
1 0
|00⟩ unchanged upon a phase. The relaxation method in
H=√
,I =
.
(2)
0 1
2 1 −1
Ref. [51] combines Upermute and a delay after it during which
T1 relaxation takes effect. By properly choosing the number
Here, α, β and γ are the rotation angles defined by users. The
of the repetitions of this combination and the delay time t, the
two-qubit gates are as follows
system can reach a state whose dominantly occupied basis is
⎛
⎞
⎛
⎞
|00⟩ and the other three base have the same but smaller prob1 0 0 0
1 0 0 0
ability. This obtained state is a PPS and can be used as the
⎜ 0 1 0 0⎟
⎜0 1 0 0 ⎟
CX = ⎝
, CY = ⎝
,
⎠
⎠
initial state |00⟩ in NMR quantum computing.
0 0 0 1
0 0 0 −i
0 0 1 0
0 0 i 0
⎛
⎞
1 0 0 0
D. Density matrix reconstruction
⎜0 1 0 0 ⎟
−itH0
−it π
JσzH σzP
2
CZ = ⎝
, delay = e
=e
,
0 0 1 0⎠
Gemini implements quantum state tomography [52] to re0 0 0 −1
construct the density matrix of the quantum state after a cer(3)
tain gate sequence is applied. Any two-qubit density matrix
can be expressed in the following way,
where CX gate is the famous control NOT (CNOT) gate.
Here, the delay gate is a free evolution gate with the dura1∑
1
tion t defined by users. It should be noted that when t is large
cij σi σj ,
ρ = I ⊗2 +
4
4 i,j
noise plays a non-negligible role and the action of this gate is
not ideal as the form in the above equation. The single-qubit
i(j) = x, y, z, 0, but (i, j) ̸= (0, 0).
(7)
gate fidelity is estimated to be ∼0.99 and the two-qubit gate
fidelity is estimated to be ∼0.98.
Here σ0 = I is the 2×2 identity matrix. To reconstruct a
density matrix, one need to measure all the cij which are
cij = Tr(ρσi σj ), in other words, the expectation values of
C. The pseudo-pure state
the Pauli matrices σi σj . There are total 15 of σi σj . But only
{σx I, σx σz ,σy I, σy σz ,Iσx , σz σx ,Iσy , σz σy } are observables
The initial state of the two-qubit system is prepared to be a
in NMR. Additional readout pulses are needed to transform
the unobservable components to be observable. For example,
pseudo-pure state (PPS) [2]. The thermal equilibrium state of

## PDF page 6

6
by applying a readout pulse Y 90 prior to measurement, cz0
can be obtained, cz0 = Tr(Y 90ρY 90† σx I). In Gemini, the
reconstruction is realized by repeating a experiment six times,
each time with a different readout pulse and observing either
31
P or 1 H. The readout pulses and cij obtained in each of the
six repetitions are listed in Fig. 9. The reconstructed PPS has
a fidelity of higher than 0.99.

Figure 10. The S PIN Q UASAR interface for quantum computing.
There is a quantum circuit composer where users can drag and drop
the supported quantum gates to construct a desired circuit. The corresponding pulse sequence is shown below the quantum circuit. There
are two buttons, ’Run’ and ’Simulate’, for activation of the experiment and the simulation, respectively. The density matrices from the
experiment and the simulation are shown in the bottom half of the
interface.
Figure 8. The pulse sequence for pseudo-pure state preparation. The
first four pulses realize a basis permutation gate. After it is a long
delay within which the natural relaxation takes effect. By properly
choosing the repetition number, N , and the duration of the delay,
t, the system can be steered to the pseudo-pure state |00⟩ from the
thermal equilibrium state.

Figure 11. Realization of the quantum computing system. It consists of the experiment on the two-qubit processor and the numerical
simulation.
Figure 9. The readout pulses, observed spins and the obtained cij
of the six experiments needed to reconstruct a density matrix in the
form of Eq. (7).

E.

Software interface

The user can use the quantum computing interface of S PIN Q UASAR to access the quantum computing function of Gemini (Fig. 10). The structure and flow-chart of quantum computing is shown in Fig. 11. This system wraps up the calibrated pulses into the quantum gates aforementioned. Users
can drag the supported gates into the circuits and press Run,
the two-qubit quantum computer will start running. The final
result will be shown in the form of density matrix which is reconstructed in the way discussed in the last section. There is
also a noiseless simulator embedded in this system so that one
can easily compare the experimental results with theoretical
results.

IV.

APPLICATION: MEASUREMENT OF GEOMETRIC
PHASE OF MIXED STATE

Gemini provides demonstrations of > 10 famous quantum algorithms, such as Deutsch-Jozsa algorithm [53], Grover
search [48], and HHL algorithm [50]. In this paper, we provide two more advanced examples that demonstrate Gemini’s
ability on running quantum algorithms. In this section, we
will demonstrate the measurement of the geometric phase of
mixed states.

A.

Theory

Geometric phase [54] is a very important concept in quantum mechanics. It is a type of phase gained by a system that
is determined by the geometry of the system’s evolution path.
The most famous geometric phase is berry phase [55] which

## PDF page 7

7
is associated with cyclic adiabatic evolution. Here we use a
spin half system as an example. A spin in a magnetic field
is aligned with the field and is in the state |0⟩. If the field
direction changes slowly and the adiabatic conditions are satisfied, the spin direction changes also adiabatically and is always along the field direction. When the magnetic field returns to its initial direction, the spin returns to its initial direction as well. However, the spin state gains a global phase and
is ei(α+β) |0⟩, where α is the dynamic phase and β is the Berry
phase. α and β have expressions as follows:
∫
1 τ
E(t)dt,
(8)
α=−
ℏ 0
1
β = − Ω.
(9)
2
E(t) is the energy of |0⟩ at the time t and is determined by the
instant Hamiltonian. Ω is the solid angle enclosed by the path.
If the initial state is in |1⟩, and the magnetic field changes
along the same path, then the geometric phase gained by the
spin is Ω/2. This is because the spin is opposite in this case
and hence its path encloses a solid angle of −Ω.
Berry phase is discussed above in the context of adiabatic
evolution. Researchers have proved that adiabatic evolution is
not a necessary condition for geometric phase [56]. Geometric
phase stays the same as long as the geometry of the evolution
path stays the same, and is not affected by the Hamiltonian
that drives this evolution.
Geometric phase is believed to be robust to local noise and
fluctuations of Hamiltonian parameters because of its connection with the path geometry. Therefore, geometric quantum computation is proposed as a candidate for fault-tolerant
quantum computation [20, 57–66]. Geometric phase in noisy
environments is also studied. When the environment is noisy,
quantum systems are always in mixed states due to the interaction with the environment. The work in Ref. [67] provides
a definition for the geometric phase of a mixed state: It is the
phase shift of the interference oscillations in interferometry
gained by the mixed state after a unitary evolution. The unitary evolution must satisfy the parallel transport requirement
[54, 67]: The state at any instant is in-phase with the state after an infinitesimal time. It can be proved that the dynamical
phase is 0 if the parallel transport requirement can be satisfied.
After such a unitary evolution, each eigen state of the density
matrix of the initial mixed state gains a phase denoted as γn ,
and has the interference visibility νn . The geometric phase γ
of the mixed state and its interference visibility ν satisfy the
following equation:
νeiγ = Σn pn νn eiγn .

(10)

Here, pn is the eigen value of the nth eigen state of the density
matrix.
B.

Experimental protocol

We adapt the protocol used in Ref. [68] to measure the
geometric phase in mixed states as defined in Eq. 10. A twoqubit system is used in this protocol. The first qubit is an

Figure 12. The unitary evolution path for the mixed state. The state
vector of the initial mixed state is prepared to be along -x axis pointing to A. It evolves along the path A-B-C-D-A to return back to point
to A. Ω is the solid angle enclosed by this path. θ = Ω/4 is the angle
between the x-y plane and either of the half paths (A-B-C or C-D-A).

ancilla qubit and the second qubit is in the mixed states whose
geometric√
phase is to be measured. The
√mixed state is a mix
of |+⟩ = 2(|0⟩ + |1⟩)/2 and |−⟩ = 2(|0⟩ − |1⟩)/2. The
initial mixed state is:
ρ(0) =

1
1
⃗·⃗
(I + r
σ ) = (I − rσx ).
2
2

(11)

⃗ is the Bloch vector, and r is its length that corresponds
Here r
to the purity of the state. If r = 1, the state is a pure state
which is |−⟩. If r = 0, the state is totally mixed. |−⟩ and |+⟩
are the two eigen states of the above density matrix with eigen
values of (1 + r)/2 and (1 − r)/2. Here we steer the state
along the path (A-B-C-D-A) which encloses a solid angle Ω
as shown in Fig. 12. Because the path is made up of geodesic
curves, the parallel transport requirement can be satisfied and
thus the dynamical phase is zero. The |−⟩ and |+⟩ states gain
geometric phases of −Ω/2 and Ω/2, and change to e−iΩ/2 |−⟩
and eiΩ/2 |+⟩, respectively. It can be proved that the interference visibility of the two eigen states are both 1. Then the
geometric phase γ of the mixed state satisfies
Ω
Ω
1
1
Ω
Ω
(1 + r)e−i 2 + (1 − r)ei 2 = cos − ir sin
2
2
2
2
(12)
Ω
(13)
γ = − tan−1 (r tan )
2

νeiγ =

In
√ order to measure γ, the ancilla qubit is prepared in theastate
2(|0⟩a + |1⟩a )/2, which has the density matrix (I + σx )/2.
We control the two-qubit system so that when the ancilla qubit
is in |1⟩a , the mixed state undergoes the unitary evolution and
when the ancilla qubit is in |0⟩a nothing happens. The phases
gained by |−⟩ and |+⟩ in the mixed state (which are ∓Ω/2)
are passed to the ancilla qubit. Thus√
after the controlled evolution, the state of the ancilla qubit is 2(|0⟩a + e∓iΩ/2 |1⟩a )/2.
The weighted average phase gained by the ancilla qubit has
the form of Eq. (13).
Next, we discuss how to prepare a mixed state in the form
of Eq. (11) from the initial PPS state |00⟩. The most used
method in NMR to prepare such a mixed state is to use a
pulsed gradient field, which can dephase the spin polarization

## PDF page 8

8
in the x-y plane fast. However, there is no pulsed gradient field
in Gemini. Considering the time scale of dephasing caused by
the static field inhomogeneity as well as T2 is much smaller
than T1 , we exploit the natural dephasing to remove the unwanted polarization. To prepare a state in Eq. 11, first the
state (I + rσz )/2 is prepared from |0⟩:
√
1
Rx (cos−1 r) 1
(I + σz ) −−−−−−−→ (I + rσz − 1 − r2 σy ).
2
2
(14)
√
The − 1 − r2 σy part in the above equation can be removed
using natural dephasing and we can get (I + rσz )/2. Then,
rotate (I + rσz )/2 about y axis by −π/2, we get (I − rσx )/2.
The |1⟩a -controlled unitary can be realized using the following sequence.

V.

APPLICATION: VARIATIONAL QUANTUM
EIGENSOLVER

In this section, we implement a variational quantum eigensolver for a two-qubit Heisenberg model.

|0⟩ =

Rx (−θ) → CZ → Rx (2θ − π) → CZ

(15)

θ is the angle between either of the two half paths and the x-y
plane, θ = Ω/4. Rx (−θ) operation rotates the first half of the
path to the x<0 half of the x-y plane. CZ is the controlledZ gate. When the ancilla qubit is in |0⟩a , CZ does nothing;
when the ancilla qubit is in |1⟩a , CZ rotates the mixed state
about z axis by π counterclockwise, which means the mixed
state evolves along the first half of the path. Rx (2θ−π) rotates
the second half of the path to the x>0 half of the x-y plane.
The CZ after it realizes the evolution of the mixed state along
the second half of the path when the ancilla qubit is |1⟩a . In
this way, the mixed state undergoes a closed path evolution
conditional on the |1⟩a state of the ancilla qubit. CZ can be
further decomposed as
π
π
π
1
Rx ( ) → Ry ( ) → Rx (− ) →
,
2
2
2
2J

(16)

here 1/2J refers to the free evolution for a duration of 1/2J
under the J coupling between the two qubits. The Rx (π/2)
gate in CZ can be combined with the Rx (−θ) and Rx (2θ − π)
operations in Eq. 15 and simplified. After this simplification,
the quantum circuit is shown in Fig. 13. The first qubit is the
ancilla qubit. φ1 = π/2 − θ, φ2 = 2θ − π/2. The geometric
phase γ can be measured by measuring the phase change of
the ancilla qubit after implementing the circuit in Fig. 13.
C.

Results

Experiments with Ω = 180◦ and Ω = 240◦ are carried out.
In each situation, r is chosen to be [0.26, 0.50, 0.71, 0.87,
0.97]. And for each of the r values, the experiment is repeated
for five times to get a mean value of the measured phases as
the result of γ (Fig. 14). The main error sources are the nonideal initial mixed state and RF pulse imperfections, such as
finite pulse width. The large fluctuations in the experimental
results come from the uncertainty in fitting the NMR spectra.
In spite of those errors and imperfections in experiments, the
change trend of the geometric phase as a function of the purity and the solid angle of the path can be observed from the
results.

A.

Background

Quantum algorithms such as the Grover search [48], Shor
factorization [69, 70] and HHL [50], have proven advantages
over their best known classical counterparts. However, these
algorithms cannot be efficiently implemented on near-term
quantum devices due to inevitable physical noises in quantum gates. Variational quantum algorithms (VQA) [71–77], a
class of algorithms under the hybrid quantum-classical framework, are more promising to have practical applications on
noisy intermediate-scale quantum quantum computers [78].
VQA use a parameterized quantum circuit to estimate the cost
function C(θ) and update θ with a classical optimizer. Variational quantum eigensolver (VQE) [72, 79] is a paradigmatic
example of VQA that aims to find the ground state and ground
state energy of a given Hamiltonian H. In this section, we will
demonstrate the experimental realization of VQE on Gemini.

B.

Algorithm

In classical computaitional physics (chemistry), we usually
estimate the ground state energy of H through variational approaches: parameterize a wave function |ψ⟩ = |ψ(θ)⟩, update θ to minimize the expectation value ⟨ψ(θ)|H|ψ(θ)⟩ until convergence. VQE facilitates the above procedure with a
quantum computer, the wave function is parameterized with a
quantum circuit U (θ) applied to the initial state |0⟩ = |0⟩⊗n ,
we optimize θ to minimize the expectation value,
E(θ) = ⟨0|U † (θ)HU (θ)|0⟩.

(17)

The classical optimizer can either be gradient-based methods
like SGD, Adam, RMSprop, BFGD, or gradient-free methods
like Nelder-Mead, Powell. Hardware-efficient ansatz [72],
unitary coupled clustered ansatz [80], and Hamiltonian variational ansatz [81, 82] are common choices for U (θ). In VQE,
the gradient can be directly estimated via the parameter-shift
rule [83, 84], i.e.,
∂E(θ)
= (⟨H⟩θ+ − ⟨H⟩θ− )/2,
i
i
∂θi

(18)

where θi± = θ ± π2 ei , ei is the i-th unit vector in the param2

3

E(θ) ∂ E(θ)
eter space. Higher order derivatives ∂ ∂θ
, ∂θ3 , which
2
i
i
are required in some optimizers, can be estimated in a similar
way [85].

## PDF page 9

9

Figure 13. The experimental circuit for the measurement of the geometric phase for mixed states.

Figure 15. The hardware efficient circuit for 2-qubit VQE. θ1 - θ4
are the parameters to be optimized.

Figure 14. The theoretical and experimental results of the mixed state
geometric phase in two situations: Ω = 180◦ and Ω = 240◦ . For
each situation, five purity values were chosen for the initial mixed
state, r=[0.26, 0.50, 0.71, 0.87, 0.97]. For each experimental data
point, the experiments were repeated for 5 times and the mean value
of the geometric phase was calculated. The error bar indicates the
standard deviation of the geometric phase in the 5 repetitions. The
theoretical values of the geometric phase are also shown as circles
(Ω = 180◦ ) and diamonds (Ω = 240◦ ) in the figure.

C.

Q1

Q3

Q4

Q5

Experimental protocol

In this work, we apply VQE to find the ground state of 2qubit Heisenberg model. The Hamiltonian is
HH = X1 X2 + Y1 Y2 + Z1 Z2 ,

Q2

Figure 16. The hardware structure of IBM Q Yorktown.

(19)

where Xj , Yj , Zj are the Pauli operator on the j-th qubit. The
hardware efficient circuit is shown in Fig. 15.
We implement experiments on SpinQ Gemini and IBM Q Yorktown with initial parameter
θ = [10.2◦ , 8.35◦ , 108◦ , 91.5◦ ], learning rate α = 0.25,
and carry out numerical simulations.
IBM Q Yorktown is a superconducting quantum computer
with 5 qubits [86], the structure is shown in Fig. 16. We only

use the first two qubits Q1 and Q2 , the single-gate error rates
are 1.173 × 10−3 and 9.810 × 10−4 , the readout errors are
2.280×10−2 and 3.660×10−2 , the CNOT error rate is 1.825×
10−2 .
The experimental procedures are as follows:
• Initialize the circuit parameters θ,
• Estimate the derivatives of θ via parameter-shift rule,

## PDF page 10

10
∂E(θ)
+
−
∂θi = (⟨H⟩θi − ⟨H⟩θi )/2.

• Update the parameters with gradient descent; θ ′ = θ −
α · ∇E(θ);
• Estimate the expectation value ⟨0|U † (θ)HU (θ)|0⟩;

thermal relaxation error model applies the amplitude damping noise after dephasing noise in each one- or two-qubit gate.
This thermal relaxation error model is characterized through
the parameters (T1 , T2∗ , tq ) and the noise probability is formulated by
tq

pdamping = 1 − e− T1 ,
)
1(
pdephasing =
1 − e−2γ ,
2

• Repeat steps 2-4 until convergence.
D.

Results and simulation
t

The results are shown in Fig. 17 (a). show the original result
of VQE experiment on SpinQ Gemini and IBMQ Yorktown,
respectively. The ground state energy of HH is -3, which is
shown by the ... line. SpinQ Gemini and IBM Q Yorktown
perform similar, both converge to E(θ) ≈ −2.6 after enough
iterations, as shown by the ... line and the ... line, respectively.
According to our simulations and analysis, the error for Gemini mainly comes from the inhomogeneous of the magnetic
field, while the error from IBMQ mainly comes from the readout error.
The noise in quantum computer can not be neglected. To
study the noise effect and stability of SpinQ Gemini, we construct a noise model to capture the quantum error of the SpinQ
Genimi. In the realistic noise NMR quantum device, the basic noise channel are dephasing and amplitude damping noise.
For initial state ρ of the system and the quantum circuit unitary transformation U , the local noise model for single-qubit
and two-qubit quantum gates can be described by the Kraus
representation
ρ→

∑
k

Ek U ρU † Ek† =

∑

Ek ρ′ Ek† ,

(20)

k

∑
where Ek s are the Kraus operators and k Ek Ek† = I. The
Ek s acting on the same single qubit and two qubits as U acts
on. The amplitude damping noise can be characterized by the
Kraus operators,
(
)
( √ )
1 √ 0
0 p
K1 =
, K2 =
,
0 0
0 1−p
where p ∈ [0, 1] is the probability of the noise. For amplitude
damping noise on single-qubit gate U , the Kraus operators
Ek s in Eq. (20) run over the set {K1 , K2 }. The Kraus operators Ek s run over the set {K1 , K2 } ⊗ {K1 , K2 } for two-qubit
noisy gate. The dephasing noise is characterized by the Kraus
operators,
√
√
K1 = 1 − pI2 , K2 = pσZ ,
(21)
where I2 is the two dimensional identity matrix and σZ is
Pauli operator. For dephasing noise on single-qubit gate U ,
the Kraus operators Ek s in Eq. (20) run over the set {K1 , K2 }.
The Kraus operators Ek s run over the set {K1 , K2 } ⊗
{K1 , K2 } for two-qubit noisy gate.
We model the noise consisting of single qubit thermal relaxation error and two qubit thermal relaxation error. The

(22)
(23)

t

where γ = Tq∗ − 2Tq1 . When the thermal relaxation error
2
model apply to single qubit gate, tq = t1q and tq = t2q for
two qubit gate. The final noise model to approximate the noise
of NMR quantum device is characterized by the parameters
{T1 , T2∗ , t1q , t2q }. We set {T1 = 5.6s, T2∗ = 0.025s, t1q =
25µs, t2q = 800µs} in the noise simulation for the NMR
quantum computer. In NMR system, the dephasing effect is
caused by both the spin relaxation and the field inhomogeneity. T2 is used to measure the spin relaxation rate, while T2∗ is
used to measure the field inhomogeneity. The T2 data is measured using the technique called spin echo, which can refocus
the magnetisation and remove the effect of inhomogeneous
field. In our VQE experiment, we did not use such technique,
so we use T2∗ instead of T2 .
With the noise model described above, we first record every
parameters θ in each iteration of the SpinQ Gemini VQE experiment. Then we take these parameters θ as the parameters
of quantum circuit ansatz (Fig. 15) and calculate the energy
of the Hamiltonian with respect to the ideal circuit and noisy
circuit output in each iteration. As shown in Fig. 17 (b) , the
noisy circuit result shows great consistancy to the experiment
data. The paramaters θ found by SpinQ Gemini is close to the
parameters for ground state. These results indicate that our
desktop quantum computer can run VQE algorithm well.

E.

Error mitigation

Quantum error mitigation [87–89] is a technique to diminish the influence of errors from the statistical perspective.
From the comparison and the simulation described above,
we can see that the dephasing error caused by the inhomogeneous magnetic field is dominant. Our circuit consists of four
single qubits rotations and one CNOT gate. The time for a
CNOT gate is about 800 µs and for single qubit gates is ∼ 20
µs. Therefore, the imperfections of the CNOT gate causes
primary error. Consider the error model:
∑
∑
ρ → ρf =
Ek U ρU † Ek† =
Ek ρ′ Ek† ,
(24)
k

k

where Ek ’s are the Kraus operators, ρ′ is the ideal density matrix, and ρf is the measured density matrix. Error mitigation is
a procedure that for a given ρf obtained from the experiment,
find a density matrix ρ0 , which is as close to ρ′ as possible,
so that the final experiment result could be improved. Here,
we employ the superoperator formalism to obtain ρ0 . This
formalism works as follows. First, let us rewrite the density

## PDF page 11

11

(a)

(b)
SpinQ Gemini
SpinQ Gemini - CEM
Ideal VQE simulation
IBMQ Yorktown
IBMQ Yorktown - REM

0.0

Energy

0.5

0.5

1.0

1.0

1.5

1.5

2.0

2.0

2.5

2.5

3.0

SpinQ Gemini
SpinQ Gemini - CEM
Noisy circuit
Ideal circuit

0.0

3.0
0

2

4

6

8

Iteration

10

12

14

0

5

10

15

Iteration

20

25

30

Figure 17. Results of VQE. (a) The VQE energy with respect to each iteration on different quantum computers and simulation. The blue
dot line represents the experimental result on SpinQ Gemini. The purple dot line reperents the CNOT error mitigated(CEM) result on SpinQ
Gemini. The red triangle line represents the numerical simulation without gate errors. The green square line represents the experimental
result on IBM Q Yorktown. The gray square line represents the readout error mitigated(REM) result on IBM Q Yorktown. (b) Numerical
simulation for quantum circuit in VQE experiment. The blue dot line represents the experimental result on SpinQ Gemini. The purple dot line
reperents the CNOT error mitigated result on SpinQ Gemini. The orange triangle line represents the energy calculate by the noisy circuit with
the SpinQ Gemini experimental parameters. The brown square line represents the energy calculate by the ideal circuit with the SpinQ Gemini
experimental parameters.

matrix ρ′ from an n × n matrix into an n2 × 1 vector ρ′ :
∑
∑
ρ′ =
ρ′ij |i⟩⟨j| → ρ′ =
ρ′ij |i⟩|j⟩.
(25)
ij

ij

Then the final state ρf , which is also an n2 × 1 vector is
ˆ
ρf = Ŝρ′ ,

Cmitigated = P −1 Cnoisy
(26)

ˆ
where Ŝ is the superoperator. With known Kraus operators
Ek , it can be obtained as
ˆ ∑
Ŝ =
Ek ⊗ Ek† .
(27)
k

ˆ
Therefore, with known ρf and Ŝ, we can get
ˆ
ρ′ = Ŝ −1 ρf .

tomography of measurement process, we get the probability
of string Sj becoming Sk , denoted by Pkj . Suppose we repeat the same measurement many times and have the string
probability distribution Cnoisy , then

(28)

The original result and the mitigated result of Gemini is shown
in Fig. 17(b). The blue line and the purple line show the original result and the CNOT error mitigated result. We can see
that the error mitigated result of the ground state of HH could
reach about −2.98, much closer to the ideal result. With both
the simulation result and the error mitigated result, we can see
that the error model we used is a good approximation.
For the IBMQ devices, the readout errors are dominant.
Here we consider the simplest linear algebra measurement error mitigation scheme. On IBMQ Santiago we do projective
measurement and obtain one of the strings {0, 1}⊗2 . Through

(29)

provides the probability distribution with measurement error
mitigated, although P −1 is not a physical operation. Measurement error mitigation can efficiently improve the performance
of VQE on IBMQ Santiago, as shown in Fig. 17(a).

VI.

DISCUSSION

For the next generations of SpinQ desktop quantum computer products, we will develop products running with more
qubits (3∼4). Currently, the design of a 3-qubit machine is
underway and the product is expected to be released in the
second quarter of 2021, with a comparable price as SpinQ
Gemini (i.e. under 50k USD). Along the way, compatible
software modules with advanced pulse control functions will
also be developed, providing more powerful abilities for quantum algorithm/control/error mitigation designs to meet the research needs of advanced users. Meanwhile, another direction
is to make a simplified version of the current model, making it
more portable and much lower cost (under 5k USD). This simplified version is expected to be released in the fourth quarter
of 2021, such that it can be more affordable for most K-12
schools around the world.

## PDF page 12

12
ACKNOWLEDGEMENT

We thank Jun Li and Tao Xin for their contribution to the
early stage of this project.

[1] Desktop nuclear magnetic resonance quantum computer (China
[17] E. Knill, R. Laflamme, R. Martinez, and C. Negrevergne,
Patent ZL 2020 2 1195611.3, 2020).
Benchmarking quantum computers: The five-qubit error cor[2] D. G. Cory, A. F. Fahmy, and T. F. Havel, Ensemrecting code, Phys. Rev. Lett. 86, 5811 (2001).
ble quantum computing by nmr spectroscopy, Proceedings
[18] L. M. K. Vandersypen, M. Steffen, G. Breyta, C. S. Yannoni,
of the National Academy of Sciences 94, 1634 (1997),
M. H. Sherwood, and I. L. Chuang, Experimental realization
https://www.pnas.org/content/94/5/1634.full.pdf.
of shor’s quantum factoring algorithm using nuclear magnetic
[3] N. A. Gershenfeld and I. L. Chuang, Bulk spin-resonance quanresonance, Nature 414, 883 (2001).
tum computation, Computation,” Science 275, 350 (1997).
[19] N. Linden, H. Barjat, and R. Freeman, An implementation
[4] I. L. Chuang, N. Gershenfeld, M. G. Kubinec, and D. W.
of the deutsch–jozsa algorithm on a three-qubit nmr quantum
Leung, Bulk quantum computation with nuclear magcomputer, Chemical Physics Letters 296, 61 (1998).
netic resonance:
theory and experiment, Proceedings
[20] J. A. Jones, V. Vedral, A. Ekert, and G. Castagnoli, Geometric
of the Royal Society of London. Series A: Mathematiquantum computation using nuclear magnetic resonance, Nacal, Physical and Engineering Sciences 454, 447 (1998),
ture 403, 869–871 (2000).
https://royalsocietypublishing.org/doi/pdf/10.1098/rspa.1998.0170. [21] M. Steffen, W. van Dam, T. Hogg, G. Breyta, and I. Chuang,
[5] D. G. Cory, M. D. Price, and T. F. Havel, Nuclear magnetic resExperimental implementation of an adiabatic quantum optionance spectroscopy: An experimentally accessible paradigm
mization algorithm, Phys. Rev. Lett. 90, 067903 (2003).
for quantum computing, Physica D: Nonlinear Phenomena 120,
[22] H. Y. Carr and E. M. Purcell, Effects of diffusion on free pre82 (1998), proceedings of the Fourth Workshop on Physics and
cession in nuclear magnetic resonance experiments, Phys. Rev.
Consumption.
94, 630 (1954).
[6] E. Knill and R. Laflamme, Power of one bit of quantum infor[23] S. Meiboom and D. Gill, Modified spin-echo method for meamation, Phys. Rev. Lett. 81, 5672 (1998).
suring nuclear relaxation times, Review of Scientific Instru[7] D. Cory, R. Laflamme, E. Knill, L. Viola, T. Havel, N. Boulant,
ments 29, 688 (1958), https://doi.org/10.1063/1.1716296.
G. Boutis, E. Fortunato, S. Lloyd, R. Martinez, C. Ne[24] N. Khaneja, T. Reiss, C. Kehlet, T. Schulte-Herbrüggen, and
grevergne, M. Pravia, Y. Sharf, G. Teklemariam, Y. Weinstein,
S. J. Glaser, Optimal control of coupled spin dynamics: design
and W. Zurek, Nmr based quantum information processing:
of nmr pulse sequences by gradient ascent algorithms, Journal
Achievements and prospects, Fortschritte der Physik 48, 875
of Magnetic Resonance 172, 296 (2005).
(2000).
[25] T. Schulte-Herbrüggen, A. Spörl, N. Khaneja, and S. J. Glaser,
[8] L. M. K. Vandersypen and I. L. Chuang, Nmr techniques for
Optimal control-based efficient synthesis of building blocks of
quantum control and computation, Rev. Mod. Phys. 76, 1037
quantum algorithms: A perspective from network complexity
(2005).
towards time complexity, Phys. Rev. A 72, 042331 (2005).
[9] I. L. Chuang, L. M. K. Vandersypen, X. Zhou, D. W. Leung,
[26] E. M. Fortunato, M. A. Pravia, N. Boulant, G. Teklemariam,
and S. Lloyd, Experimental realization of a quantum algorithm,
T. F. Havel, and D. G. Cory, Design of strongly modulating
Nature 393, 143 (1998).
pulses to implement precise effective hamiltonians for quantum
[10] J. A. Jones, M. Mosca, and R. H. Hansen, Implementation of a
information processing, The Journal of Chemical Physics 116,
quantum search algorithm on a quantum computer, Nature 393,
7599 (2002), https://doi.org/10.1063/1.1465412.
344 (1998).
[27] S. Wimperis, Broadband, narrowband, and passband composite
[11] M. A. Nielsen, E. Knill, and R. Laflamme, Complete quantum
pulses for use in advanced nmr experiments, Journal of Magteleportation using nuclear magnetic resonance, Nature 396, 52
netic Resonance, Series A 109, 221 (1994).
(1998).
[28] K. R. Brown, A. W. Harrow, and I. L. Chuang, Arbitrarily ac[12] S. Somaroo, C. H. Tseng, T. F. Havel, R. Laflamme, and D. G.
curate composite pulse sequences, Phys. Rev. A 70, 052318
Cory, Quantum simulations on a quantum computer, Phys. Rev.
(2004).
Lett. 82, 5381 (1999).
[29] W. G. Alway and J. A. Jones, Arbitrary precision composite
[13] E. Knill, R. Laflamme, R. Martinez, and C. H. Tseng, An algopulses for nmr quantum computing, Journal of Magnetic Resorithmic benchmark for quantum information processing, Nature
nance 189, 114 (2007).
404, 368 (2000).
[30] A. M. Souza, G. A. Álvarez, and D. Suter, Robust dynami[14] L. M. K. Vandersypen, M. Steffen, G. Breyta, C. S. Yannoni,
cal decoupling for quantum computing and quantum memory,
R. Cleve, and I. L. Chuang, Experimental realization of an
Phys. Rev. Lett. 106, 240501 (2011).
order-finding algorithm with an nmr quantum computer, Phys.
[31] A. Cross, The ibm q experience and qiskit open-source quanRev. Lett. 85, 5452 (2000).
tum computing software, in APS March Meeting Abstracts, Vol.
[15] Y. S. Weinstein, M. A. Pravia, E. M. Fortunato, S. Lloyd, and
2018 (2018) pp. L58–003.
D. G. Cory, Implementation of the quantum fourier transform,
[32] C. Monroe, Ionq quantum computers: Clear to scale, Bulletin
Phys. Rev. Lett. 86, 1889 (2001).
of the American Physical Society.
[16] D. G. Cory, M. D. Price, W. Maas, E. Knill, R. Laflamme, W. H.
[33] Https://www.rigetti.com/.
Zurek, T. F. Havel, and S. S. Somaroo, Experimental quantum
[34] M. Kjaergaard, M. E. Schwartz, J. Braumüller, P. Krantz, J. I.error correction, Phys. Rev. Lett. 81, 2152 (1998).
J. Wang, S. Gustavsson, and W. D. Oliver, Superconducting

## PDF page 13

13
qubits: Current state of play, Annual Review of Condensed
Matter Physics 11, 369 (2020).
[35] P. Krantz, M. Kjaergaard, F. Yan, T. P. Orlando, S. Gustavsson,
and W. D. Oliver, A quantum engineer’s guide to superconducting qubits, Applied Physics Reviews 6, 021318 (2019).
[36] G. Wendin, Quantum information processing with superconducting circuits: a review, Reports on Progress in Physics 80,
106001 (2017).
[37] X. Gu, A. F. Kockum, A. Miranowicz, Y.-x. Liu, and F. Nori,
Microwave photonics with superconducting quantum circuits,
Physics Reports 718, 1 (2017).
[38] J. You and F. Nori, Superconducting circuits and quantum information, Phys. Today 58, 42 (2006).
[39] J. You and F. Nori, Atomic physics and quantum optics using
superconducting circuits, Nature 474, 589 (2011).
[40] G. Wendin and V. Shumeiko, Quantum bits with josephson
junctions, Low Temperature Physics 33, 724 (2007).
[41] D. Brown, B.-M. Ma, and Z. Chen, Developments in the processing and properties of ndfeb-type permanent magnets, Journal of Magnetism and Magnetic Materials 248, 432 (2002).
[42] M. Calin and E. Helerea, Temperature influence on magnetic
characteristics of ndfeb permanent magnets, in 2011 7TH INTERNATIONAL SYMPOSIUM ON ADVANCED TOPICS IN
ELECTRICAL ENGINEERING (ATEE) (2011) pp. 1–6.
[43] https://magritek.com/products/spinsolve/.
[44] https://nmr.oxinst.com/x-pulse.
[45] https://www.nanalysis.com/nmready-60pro.
[46] https://www.aiinmr.com/.
[47] D. David and J. Richard, Rapid solution of problems by quantum computation, Proc. R. Soc. Lond. A 439, 553–558 (1992).
[48] L. K. Grover, A fast quantum mechanical algorithm for
database search, in Proceedings of the twenty-eighth annual
ACM symposium on Theory of computing (1996) pp. 212–219.
[49] G. L. Long, Grover algorithm with zero theoretical failure rate,
Phys. Rev. A 64, 022307 (2001).
[50] A. W. Harrow, A. Hassidim, and S. Lloyd, Quantum algorithm
for linear systems of equations, Physical review letters 103,
150502 (2009).
[51] J. Li, D. Lu, Z. Luo, R. Laflamme, X. Peng, and J. Du, Approximation of reachable sets for coherently controlled open quantum systems: Application to quantum state engineering, Phys.
Rev. A 94, 012312 (2016).
[52] J.-S. Lee, The quantum state tomography on an nmr system,
Physics Letters A 305, 349 (2002).
[53] D. Deutsch and R. Jozsa, Rapid solution of problems by quantum computation, Proceedings of the Royal Society of London.
Series A: Mathematical and Physical Sciences 439, 553 (1992).
[54] J. Anandan, The geometric phase, Nature 360, 307–313 (1992).
[55] M. V. Berry, Quantal phase factors accompanying adiabatic
changes, Proc. R. Soc. Lond. A 392, 45–57 (1984).
[56] Y. Aharonov and J. Anandan, Phase change during a cyclic
quantum evolution, Phys. Rev. Lett. 58, 1593 (1987).
[57] P. Zanardi and M. Rasetti, Holonomic quantum computation,
Physics Letters A 264, 94 (1999).
[58] L.-M. Duan, J. I. Cirac, and P. Zoller, Geometric manipulation of trapped ions for quantum
computation,
Science
292,
1695
(2001),
https://science.sciencemag.org/content/292/5522/1695.full.pdf.
[59] S.-L. Zhu and Z. D. Wang, Unconventional geometric quantum
computation, Phys. Rev. Lett. 91, 187902 (2003).
[60] L.-A. Wu, P. Zanardi, and D. A. Lidar, Holonomic quantum
computation in decoherence-free subspaces, Phys. Rev. Lett.
95, 130501 (2005).

[61] O. Oreshkov, T. A. Brun, and D. A. Lidar, Fault-tolerant holonomic quantum computation, Phys. Rev. Lett. 102, 070502
(2009).
[62] W. Xiang-Bin and M. Keiji, Nonadiabatic conditional geometric phase shift with nmr, Phys. Rev. Lett. 87, 097901 (2001).
[63] E. Sjöqvist, D. M. Tong, L. M. Andersson, B. Hessmo, M. Johansson, and K. Singh, Non-adiabatic holonomic quantum
computation, New Journal of Physics 14, 103035 (2012).
[64] G. F. Xu, J. Zhang, D. M. Tong, E. Sjöqvist, and L. C. Kwek,
Nonadiabatic holonomic quantum computation in decoherencefree subspaces, Phys. Rev. Lett. 109, 170501 (2012).
[65] G. Feng, G. Xu, and G. Long, Experimental realization of nonadiabatic holonomic quantum computation, Phys. Rev. Lett. 110,
190501 (2013).
[66] C. Zu, W.-B. Wang, L. He, W.-G. Zhang, C.-Y. Dai, F. Wang,
and L.-M. Duan, Experimental realization of universal geometric quantum gates with solid-state spins, Nature 514, 72–75
(2014).
[67] E. Sjöqvist, A. K. Pati, A. Ekert, J. S. Anandan, M. Ericsson,
D. K. L. Oi, and V. Vedral, Geometric phases for mixed states
in interferometry, Phys. Rev. Lett. 85, 2845 (2000).
[68] J. Du, P. Zou, M. Shi, L. C. Kwek, J.-W. Pan, C. H. Oh, A. Ekert, D. K. L. Oi, and M. Ericsson, Observation of geometric
phases for mixed states using nmr interferometry, Phys. Rev.
Lett. 91, 100403 (2003).
[69] P. W. Shor, Algorithms for quantum computation: discrete logarithms and factoring, in Proceedings 35th Annual Symposium
on Foundations of Computer Science (1994) pp. 124–134.
[70] P. W. Shor, Polynomial-time algorithms for prime factorization
and discrete logarithms on a quantum computer, SIAM review
41, 303 (1999).
[71] M. Cerezo, A. Arrasmith, R. Babbush, S. C. Benjamin,
S. Endo, K. Fujii, J. R. McClean, K. Mitarai, X. Yuan, L. Cincio, et al., Variational quantum algorithms, arXiv preprint
arXiv:2012.09265 (2020).
[72] A. Kandala, A. Mezzacapo, K. Temme, M. Takita, M. Brink,
J. M. Chow, and J. M. Gambetta, Hardware-efficient variational
quantum eigensolver for small molecules and quantum magnets, Nature 549, 242 (2017).
[73] R. LaRose, A. Tikku, É. O’Neel-Judy, L. Cincio, and P. J. Coles,
Variational quantum state diagonalization, npj Quantum Information 5, 1 (2019).
[74] J. Zeng, C. Cao, C. Zhang, P. Xu, and B. Zeng, A variational quantum algorithm for hamiltonian diagonalization,
arXiv preprint arXiv:2008.09854 (2020).
[75] J. Romero, J. P. Olson, and A. Aspuru-Guzik, Quantum autoencoders for efficient compression of quantum data, Quantum Science and Technology 2, 045001 (2017).
[76] C. Cao and X. Wang, Noise-assisted quantum autoencoder,
arXiv preprint arXiv:2012.08331 (2020).
[77] X. Yuan, S. Endo, Q. Zhao, Y. Li, and S. C. Benjamin, Theory
of variational quantum simulation, Quantum 3, 191 (2019).
[78] J. Preskill, Quantum computing in the nisq era and beyond,
Quantum 2, 79 (2018).
[79] C. Hempel, C. Maier, J. Romero, J. McClean, T. Monz,
H. Shen, P. Jurcevic, B. P. Lanyon, P. Love, R. Babbush, et al.,
Quantum chemistry calculations on a trapped-ion quantum simulator, Physical Review X 8, 031022 (2018).
[80] J. Lee, W. J. Huggins, M. Head-Gordon, and K. B. Whaley,
Generalized unitary coupled cluster wave functions for quantum computation, Journal of chemical theory and computation
15, 311 (2018).
[81] D. Wecker, M. B. Hastings, and M. Troyer, Progress towards
practical quantum variational algorithms, Physical Review A

## PDF page 14

14
92, 042303 (2015).
[82] R. Wiersema, C. Zhou, Y. de Sereville, J. F. Carrasquilla, Y. B.
Kim, and H. Yuen, Exploring entanglement and optimization
within the hamiltonian variational ansatz, PRX Quantum 1,
020319 (2020).
[83] K. Mitarai, M. Negoro, M. Kitagawa, and K. Fujii, Quantum
circuit learning, Phys. Rev. A 98, 032309 (2018).
[84] M. Schuld, V. Bergholm, C. Gogolin, J. Izaac, and N. Killoran,
Evaluating analytic gradients on quantum hardware, Phys. Rev.
A 99, 032331 (2019).
[85] A. Mari, T. R. Bromley, and N. Killoran, Estimating the gradient and higher-order derivatives on quantum hardware, Physical
Review A 103, 012405 (2020).

[86] 5-qubit backend: IBM Q team, “IBM Q 5 Yorktown backend specification V2.2.5,". Retrieved from https://quantumcomputing.ibm.com (2021).
[87] Y. Li and S. C. Benjamin, Efficient variational quantum simulator incorporating active error minimization, Physical Review
X 7, 021050 (2017).
[88] S. Endo, S. C. Benjamin, and Y. Li, Practical quantum error
mitigation for near-future applications, Physical Review X 8,
031027 (2018).
[89] G. S. Barron and C. J. Wood, Measurement error mitigation for variational quantum algorithms, arXiv preprint
arXiv:2010.08520 (2020).
