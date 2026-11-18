Source: see manifest row of the PDF
PDF sha256: 589a1272b73a7fbbea435ab5f42de02259b44288b7b626efc9f87859fcfb7b63
License: CC-BY-4.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of polino_2024_photonic_implementation_of_quantum_gravity_simulator.pdf

Transcription of `polino_2024_photonic_implementation_of_quantum_gravity_simulator.pdf` in this directory, 8 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-8 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Research Article

Photonic implementation of quantum gravity
simulator
Emanuele Polino,a Beatrice Polacchi ,a Davide Poderini ,a Iris Agresti,a Gonzalo Carvacho,a Fabio Sciarrino ,a,*
Andrea Di Biagio,a,b Carlo Rovelli ,c,d,e,* and Marios Christodouloub,f,*
a

Sapienza Università di Roma, Dipartimento di Fisica, Roma, Italy
Austrian Academy of Sciences, Institute for Quantum Optics and Quantum Information Vienna, Vienna, Austria
c
Aix-Marseille University, Université de Toulon, CPT-CNRS, Marseille, France
d
Western University, Department of Philosophy and the Rotman Institute of Philosophy, London, Ontario, Canada
e
Perimeter Institute, Waterloo, Ontario, Canada
f
University of Vienna, Vienna Center for Quantum Science and Technology, Faculty of Physics, Vienna, Austria
b

Abstract. Detecting gravity-mediated entanglement can provide evidence that the gravitational field obeys
quantum mechanics. We report the result of a simulation of the phenomenon using a photonic platform.
The simulation tests the idea of probing the quantum nature of a variable by using it to mediate
entanglement and yields theoretical and experimental insights, clarifying the operational tools needed for
future gravitational experiments. We employ three methods to test the presence of entanglement: the Bell
test, entanglement witness, and quantum state tomography. We also simulate the alternative scenario
predicted by gravitational collapse models or due to imperfections in the experimental setup and use
quantum state tomography to certify the absence of entanglement. The simulation reinforces two main
lessons: (1) which path information must be first encoded and subsequently coherently erased from the
gravitational field and (2) performing a Bell test leads to stronger conclusions, certifying the existence of
gravity-mediated nonlocality.
Keywords: quantum information; quantum gravity; quantum optics; quantum simulation; nonlocality.
Received Jan. 30, 2024; revised manuscript received Apr. 6, 2024; accepted for publication Apr. 28, 2024; published online
May 22, 2024.
© The Authors. Published by SPIE and CLP under a Creative Commons Attribution 4.0 International License. Distribution or
reproduction of this work in whole or in part requires full attribution of the original publication, including its DOI.
[DOI: 10.1117/1.APN.3.3.036011]

1 Introduction
The gravitational field is generally expected to obey quantum
mechanics, like any other physical field. But to this day, there
is no experimental evidence that this is the case. At the 1957
Chapel Hill conference, Richard Feynman famously emphasized that the gravitational field can be set into quantum superposition by simply setting a source, namely, a mass, into the
superposition of two positions.1 But, given the weakness of the
gravitational interaction, how can we find empirical evidence
for the superposition of field configurations?
The past few years have seen an intense interest in the possibility of obtaining such evidence on the laboratory bench, by
*Address all correspondence to Fabio Sciarrino, fabio.sciarrino@uniroma1.it; Carlo
Rovelli, rovelli@cpt.univ-mrs.fr; Marios Christodoulou, marios.christodoulou@
oeaw.ac.at

Advanced Photonics Nexus

detecting entanglement generated between quantum masses interacting gravitationally.2–22 The key idea is that if the field
mediating an interaction can be in a quantum superposition,
this interaction can entangle degrees of freedom. A well-known
result in quantum information theory states that quantum
entanglement cannot be created between two systems by local
operations and classical communication (LOCC).23–25 Gravitymediated entanglement (GME) can thus provide evidence
that the gravitational field that mediates the interaction is in a
quantum superposition.26 Rapid advances in quantum control
of larger masses27–30 and measuring the gravitational field of
smaller masses31,32 might soon make this momentous experimental test possible.
The effect is predicted by most current tentative quantum
gravity theories, such as loop quantum gravity, string theory,
as well as low-energy effective field theory. On the contrary,
it is not predicted by theories where the gravitational interaction

036011-1

May∕Jun 2024 • Vol. 3(3)

## PDF page 2

Polino et al.: Photonic implementation of quantum gravity simulator

is mediated by a local classical field,33–35 nor by theories
where the gravitational field does not display sufficiently longlasting massive superpositions of macroscopically different
configurations or where massive superpositions spontaneously
collapse.6,36–38 Thus, a negative result of the experiment would
also be of particular interest, as the absence of GME would
falsify common assumptions in quantum gravity research and
provide evidence for these unorthodox theories.
The logic of the GME experiments, however, is more subtle:
find evidence for a key property of certain collective degrees of
freedom by looking at the way these allow other degrees of freedom to get entangled. Unpacking this argument is the subject of
a lively debate on the precise epistemological conclusions that
can be drawn from the detection of GME. Recent overviews of
the debate are given in Refs. 39 and 40.
In this work, we report the photonic implementation of a
quantum circuit simulating the experimental proposal of Ref. 3.
The simulation sheds light on subtle aspects of the logic behind
the claim that detecting GME is tantamount to evidence for
the quantum nature of the gravitational interaction. Using an
entanglement witness and the violation of a Bell inequality,
we study how these different measurement protocols can certify
the presence of entanglement, given realistic levels of noise. To
study the possibility of a negative experimental outcome, we simulate spontaneous collapse models by introducing decoherence
into the simulator and employ quantum state tomography to certify the absence of entanglement. In this way, we clarify the operational and theoretical tools needed to realize the gravitational
experiment. We believe that the reported results can help the
understanding and analysis of future GME experiments.

2 Experiment and Results
2.1 Gravity-Mediated Entanglement Experiment:
Quantum Circuit Simulator
In the GME experiment, two masses are manipulated into a
macroscopic center of mass superposition through an inhomogeneous magnetic field that couples to a spin (NV-center) embedded in each mass; see Fig. 1. Once the superposition is
accomplished, the state of the full quantum system is
j↑↑ijgLR i þ j↑↓ijgLL i þ j↓↑ijgRR i þ j↓↓ijgRL i;

(1)

where j↑i and j↓i are spin-z eigenstates, and the states jgXY i are
coherent states of the gravitational field and center of mass
position of the masses.26,41 These states are approximate energy
eigenstates,13 and they simply accumulate a relative phase during the free fall stage. Once the superposition is undone, the
spins disentangle from the geometry. Tracing it out, we get
eiϕLR j↑↑i þ eiϕLL j↑↓i þ eiϕRR j↓↑i þ eiϕRL j↓↓i:

(2)

For generic values of the phases, this is an entangled state. A
detailed covariant derivation of this effect is given in Ref. 41.
Note that, although we described the experiment using spin qubits, this represents only a useful choice to describe a particular
physical spin-based experimental realization of the GME. The
argument is general and different platforms can be employed for
the realizations of this kind of experiment, such as nanomechanical oscillators and matter–wave interferometry.
The quantum circuit simulator is shown in Fig. 2(a) (note that
the quantum circuit has been also discussed in Ref. 42). It is a
Advanced Photonics Nexus

Fig. 1 Two masses in path superposition interacting gravitationally become entangled. Two massive particles with embedded
magnetic spins are put into a spin-dependent path superposition.
They are then left to free fall, where they interact via the gravitational field only. Then, the path superposition is undone, and
measurements are performed on the spins. During the free fall,
each branch of the superposition accumulates a different phase,
which entangles the two particles.

straightforward representation of the evolution of the experiment in the regime Δx ≫ d, where only the phase in the branch
of the closest approach needs to be considered. This regime simplifies the analysis, without compromising the physics.3,26
The circuit represents the two spins and the geometry as a
16-dimensional system. Each embedded spin is simulated with
a qubit, while the geometry degrees of freedom with two qubits
(a ququart). We write vectors as belonging to the Hilbert space,
C2 ⊗ C4 ⊗ C2 ¼ HspinA ⊗ Hgeometry ⊗ HspinB :

(3)

At the end of the free fall stage, the state of the full system is
1
ðj0000i þ j0011i þ j1100i þ eiϕ j1111iÞ:
2

(4)

After the recombination stage, the state of the geometry
ququart factorizes. At the moment of measurement, the spin
qubits are in the state
1
ðj00i þ j01i þ j10i þ eiϕ j11iÞ:
2

(5)

We implemented the quantum circuit simulator on the photonic platform shown in Fig. 2(b). The polarization of the
photons carries the qubits representing the spins, while the
geometry ququart is encoded in the paths of the photons. The
spin and path degrees of freedom are associated with different
Hilbert spaces, and therefore the path ququart of the photons
can be said to be mediating the interaction between the spin
qubits. The mapping from the massive experiment is coarsegrained, lumping the path of the particles and the geometry
in the ququart. As we will discuss below, in this framework,
the conclusions about the nature of the mediator are drawn from
minimal assumptions on the interaction and causal structure
and are independent of any specific and possibly unknown dynamics of the massive experiment.

036011-2

May∕Jun 2024 • Vol. 3(3)

## PDF page 3

Polino et al.: Photonic implementation of quantum gravity simulator

(a)

(b)

Fig. 2 The quantum circuit simulator and its photonic implementation. (a) Two qubits, js 1 i and js 2 i,
represent the spin degrees of freedom, while two qubits, jg 1 i and jg 2 i, represent the geometry.
Each stage of the experiment is mapped into quantum gates acting on the qubits. (b) The simulator
is implemented using the path and polarization degrees of freedom of two photons. The spin qubits
of the simulator are encoded in the polarization degree of freedom of the photons, while the geometry degrees of freedom are encoded in the photon paths. The two photons are independently
prepared in a superposition of horizontal and vertical polarization, and each one passes through
a BD, which completely entangles the path of each photon with its polarization. The control-phase
(CZ) gate is implemented due to bosonic interference, which is due to the indistinguishability of the
photons at the BS. Two HWPs momentarily make the polarization of all paths equal in order to allow
the realization of the CZ gate on this degree of freedom. Finally, the qubit state is restored by two
other HWPs and the paths are recombined by final BDs, which disentangles path and polarization.
Finally, the polarizations of the photons are measured using quarter- and half-waveplates and
polarizing beam splitter followed by single-photon detectors. BD, beam displacer; QWP, quarterwave plate; PBS, polarization beam splitter; HWP, half-wave plate; BS, beam splitter; APD, avalanche photo diode.

Photons of wavelength ∼785 nm are produced by spontaneous parametric downconversion from a nonlinear barium borate
crystal pumped by a pulsed laser at 392.5 nm. The CNOT gates
of the superposition and recombination stages are deterministically performed on each photon’s path-polarization space
through calcite beam displacers (BDs). The control-phase gate
with a phase equal to π acting on the paths of the photon, which
represents the effect of the free fall stage, is realized by a probabilistic scheme exploiting bosonic interference in a beam splitter (BS) with the reflection coefficient 1∕3.43 Further details on
the scheme and the experimental setup are provided in the
Supplementary Material.
At the end of the recombination stage, the polarization state
of the photons is
Advanced Photonics Nexus

1
ðjVVi þ jHVi þ jVHi − jHHiÞ;
2

(6)

where horizontal (jHi) and vertical (jVi) polarizations encode
the qubit states j1i and j0i in Eq. (5), respectively.
Before the finalpﬃﬃ
measurement, we apply the local unitary operation ðσ z þ σ x Þ∕ 2 on the second qubit, by means of a halfwave plate rotated by 22.5 deg with respect to its optical axis.
This step allows to recast the state as the maximally entangled
singlet state,
1
jΨ− i ¼ pﬃﬃ ðjHVi − jVHiÞ:
2

036011-3

(7)

May∕Jun 2024 • Vol. 3(3)

## PDF page 4

Polino et al.: Photonic implementation of quantum gravity simulator

This final rotation, which is equivalent to changing the
measurement basis, simplifies the analysis without loss of generality.
2.2 Experimental Results
To certify the presence or absence of entanglement at the measurement stage, we implemented three strategies: quantum state
tomography, an entanglement witness, and the violation of a
Bell inequality. Each comes with its own merits and shortcomings, which we briefly recall.
Quantum state tomography44 provides the maximum amount
of information about a quantum system by measuring enough
observables to fully reconstruct the quantum state. Of the three
methods considered, this is the only one capable of certifying
the absence of entanglement. Quantum state tomography requires the implementation of a large number of measurements
that for systems of larger dimensions can be too expensive to
perform. Entanglement can be detected with fewer resources
by means of entanglement witnesses45,46 that are observables
W such that hWi ≥ 0 for all separable states and hWi < 0 for
at least one entangled state. Therefore, a negative expectation
value implies the state is entangled. Alternatively, the violation
of a Bell inequality, such as the CHSH inequality,47 allows one
to draw conclusions with strictly weaker assumptions than

(a)

(b)

(c)

(d)

entanglement witnesses and tomography.12,48,49 This is because,
in contrast to the two previous techniques, Bell inequalities do
not rely on assuming the validity of quantum theory nor the correct implementation of the quantum measurements; that is, it
provides what is commonly called a device-independent certification of the presence of entanglement, one that relies on minimal assumptions about the experimental setup. Note, however,
that not all entangled states can violate a Bell inequality, while
an entanglement witness can be designed to detect arbitrary
amounts of entanglement.
After the fine alignment of the setup, we performed a CHSH
test on the polarization of the photons at the end of the circuit,
obtaining a value Sexp ¼ 2.402  0.015. That is, the classical
bound of 2 was violated by more than 26 standard deviations.
This provides a device-independent certification that entanglement was successfully mediated via the action of the CZ gate on
the path degree of freedom of the photons. Then, we measured
the following entanglement witness:
W ¼ 1−jhσ x ⊗ σ x i þ hσ y ⊗ σ y ij;

(8)

obtaining a value of W exp ¼ −0.72  0.02. This result violates
the separable bound of 0 by more than 36 standard deviations,
where the statistical uncertainty has been computed assuming

Fig. 3 Results of the simulator without and with decoherence. (a) Expectation values of the operators used for the CHSH test on the spin qubits. The lighter-colored parts in each bar (hardly
visible) represent the Poissonian experimental errors associated with each observable. The orange dashed bars are the values expected from an ideal maximally entangled state. (b) Real and
imaginary parts of the measured density matrix of the spin qubits. (c) Measured values of the
entanglement witness W as a function of the degree of decoherence η. The latter corresponds
to the relative time delay of different polarizations normalized to the coherence time of the photons.
The purple-shaded area indicates the region where the witness certifies the entanglement of the
state. The dashed black line represents the theoretical curve from the model of the experimental
setup. Error bars are due to Poissonian statistics of the measured events. (d) Real and imaginary
parts of the measured density matrix of the polarization state of the spin qubits, where the state
has experienced maximum decoherence effects (η ¼ 1) introduced by a delay between linear
polarizations greater than the photon coherence time. The off-diagonal terms are completely
suppressed and the state is separable.
Advanced Photonics Nexus

036011-4

May∕Jun 2024 • Vol. 3(3)

## PDF page 5

Polino et al.: Photonic implementation of quantum gravity simulator

Poissonian statistics. The entanglement witness (8) is equivalent, up to local unitaries, to the one proposed in Ref. 3.
Results from the quantum state tomography of the generated
state are given in Fig. 3(b).
To simulate the effects of spontaneous collapse, we induced
decoherence by the implementation of time delays across different photon polarizations at the output of the BS. While in some
gravity-induced collapse models, the wave function collapses
because of stochastic fluctuations of the space–time metric36,37
and coupling with a classical gravitational field,33 here, we simulate the result of this effect (not its dynamics) by entangling the
polarization of the photons with the temporal degree of freedom.
When traced out, the temporal information induces an effective
decoherence. As long as the delay is shorter than the coherence
time of the photon wave packet, some degree of entanglement
can be generated and detected by the witness. However, when
the delay is longer than the photon coherence time, no entanglement can be detected in the final state.
If one of the photons passes through a birefringent slice after
the BS, the state before measurement becomes
1
jΨidel ¼ pﬃﬃ ðjHijVitV − jVijHitH Þ:
2

(9)

Here, tH and tV are the distinguishable delays acquired by
the horizontal and vertical polarizations, respectively. When the
delay is greater than the coherence time of the photons, tracing
out the information regarding the delays results in the completely mixed state,
1
ρpol
mix ¼ ðjHVihHVj þ jVHihVHjÞ:
2

(10)

In contrast, when the delay is shorter than the coherence time
of the photons, the state is
ð1 − ηÞjΨ− ihΨ− j þ ηρpol
mix ;

(11)

which is partially mixed. The parameter η quantifies the amount
of decoherence due to the polarization-dependent delay.
Changing the thickness of the birefringent slices allows one to
vary η from vanishing to maximum decoherence.
We measured the witness W and performed state tomography for five values of η. For η > 0.4, which corresponds to delays greater than around 450 ps, the observed witness does not
violate the separable bound; see Fig. 3(c). The state tomography
for the completely decohered state (η ¼ 1) is reported in
Fig. 3(d). Results for all values of η are reported in Fig. S2
in the Supplementary Material.
Quantum state tomography allows one to exclude the presence of entanglement in a quantum mechanical framework.
Indeed, failure to detect entanglement with the witness is not
proof of the absence of entanglement. For example, the entanglement witness did not detect entanglement for η ∼ 0.6, but a
positive partial transpose test45 on the results of state tomography revealed the presence of entanglement. The four eigenvalues were ð0.583; 0.357; 0.230; −0.170Þ  ð0.005; 0.007; 0.007;
0.008Þ. The error intervals were computed with the Monte Carlo
method. Note that, for two-qubit states, the presence of a negative eigenvalue in the partial transpose is a necessary and sufficient condition for entanglement.
Advanced Photonics Nexus

We also simulated a conceptually different effect by introducing noise in the state of the geometry ququart. Indeed, while
decoherence effects could be caused by the spontaneous collapse of the state of the particles, in a realistic experiment, it
may also be the case that the interaction among particles is
not strong enough to generate observable effects. For example,
this would be the case if the distance between the interferometer
paths is too large, or if the particles pass through the interferometers at different times. In both these cases, no gravitational
interaction would be present, and the two particles pass along
the interferometers in a fully independent way. In our experiment, this independence is provided by the distinguishability
of the photons. Therefore, the expected partially distinguishable
state ρpart: dist: will be a mixture of the following form:
ρpart: dist: ¼ vjΨ− ihΨ− j þ ð1 − vÞρdist ;

(12)

where the visibility v depends on the time delay between the
photons. The density matrix ρdist is the expected two-photon
state when the delay time is longer than the coherence time
of the photons and is given as
1
(13)
ρdist ¼ ðjHþihH þ j þ j þ HihþHjÞ;
2
pﬃﬃ
with jþi ¼ ðjHi þ jViÞ∕ 2. We implemented this by varying
the relative time arrival of the photons in the probabilistic control gate. The measured entanglement witnesses W and quantum state tomographies for different indistinguishability degrees
v are reported in Figs. S4 and S3 in the Supplementary Material.
The results of the tomography for the two kinds of decoherence
models are qualitatively different.
For the sake of completeness, we note another possible effect, relevant in massive experiments but not taken into account
in this simulation, that is, the presence of phases ϕ ≪ π in
Eq. (5). These smaller phases would be due to the weakness of
gravitational interaction and the challenge of tuning the experimental parameters to set ϕ ¼ π. The effect of noise and
decoherence would be even more marked in this regime.

3 Materials and Methods
3.1 Experimental Details
To quantify the degree of indistinguishability of the photons
imprinting the BS, we measured the visibility of the Hong–
Ou–Mandel (HOM) dip of the coincidences with respect to
the time delay between the two photons. The experimental
value found for the visibility is V exp ¼ 0.73  0.02 that we compare to the ideal (perfect indistinguishable photons) theoretical
one V theo ¼ 0.8, obtaining a ratio equal to V exp ∕V theo ¼
0.913  0.025.
The calcite BDs act as the entangling gates of the superposition and recombination stages between the path and polarization of the single photons with a fidelity >99.5%.
The measured value of the reflectivities of the BS is jrH j2 ¼
0.329  0.001 for the horizontal polarization and jrV j2 ¼
0.337  0.001 for the vertical polarization of the incoming
photons.
The fidelity of the scheme is also affected by the degree of
indistinguishability of the interfering photons in all their degrees
of freedom. Polarization, frequency, time of arrival, and spatial
mode overlap all affect indistinguishability. Time of arrival and

036011-5

May∕Jun 2024 • Vol. 3(3)

## PDF page 6

Polino et al.: Photonic implementation of quantum gravity simulator

spatial mode overlap are crucial: the arrival time on the BS is
controlled by suitable delay lines, while spatial modes are recombined by fine alignment through optical mirrors.

4 Conclusions
We detected the creation of mediated entanglement in the photonic simulator using three different methods: Bell inequality
violation, entanglement witness, and quantum state tomography. We simulated two kinds of decoherence: those due to
noise and due to unknown physics, and noted they may be
distinguished with state tomography. The considered noises are
indicative, since they represent some of the main challenges of
future massive experiments.6
The study of the GME experimental proposals is merging the
scientific culture of the two research communities of quantum
gravity and quantum information. It is shedding light theoretically and experimentally on the possibilities of quantum gravity
phenomenology and has sparked a lively debate that reaches the
foundations of quantum theory.
A core aspect of the debate is the concept of witnessing the
nonclassicality of the gravitational field, and more in general the
distinction between “classical” and “nonclassical” behavior.
Within quantum mechanics, superposition is a hallmark of
nonclassical behavior. Superposition is, however, a theory- and
basis-dependent concept. Its operational content can be encapsulated in the existence of noncommuting observables. The
existence of noncommuting observables is the defining characteristic of nonclassical systems employed in the recent theoryindependent generalizations of the LOCC theorems used to
analyze GME.17,50
The main goal of this work is to apply known quantum information results and notions to the interpretation of GME
experiments.
Our simulation makes explicit the crucial role of the noncommuting variables of the gravitational mediator. The mediating
ququart entangles with the spin qubits due to the presence of
the X ⊗ I and I ⊗ X observables in the CNOT gates. The
phases are then generated by the ZZ observable. Introducing
decoherence in the mediator removes the noncommutativity,
since trXYI ¼ trYXI. Once the noncommutativity is removed,
no entanglement is generated between the spins.
While high-level abstract tools like the LOCC theorems can
be very powerful, in practice, they are only informative insofar
as they can be applied to well-developed theories that physicists
are interested in testing. Linearized quantum gravity is the effective quantum field theory expected to correctly describe the
physics in this regime. Here, different approaches try to define
what type of field excitations are responsible for the mediation
of entanglement: the Newtonian potential,51,52 off-shell gravitons,10,53 or superposition of spacetime geometries.26,41
Then, a question is how the mediator carries quantum information and gives rise to GME. In some sense, the entanglement
has to be mediated via an interaction that is nonradiative. A hint
of what is going on is provided by our simulation. During each
run of the simulation, the geometry ququart acquires which-path
information about the spin qubits only for a limited amount of
time. The initial CNOT gates write the state of the spins in the
geometry, while the final CNOT gates erase this information in a
coherent way. This is a crucial point: since the geometry ququart
is not measured, it would be impossible to detect the entanglement in the spins qubits if they were still entangled with it at the
moment of measurement. In the gravitational experiment, the
Advanced Photonics Nexus

which-path information about the masses should not propagate
to infinity. Instead, the which-path information must be coherently erased from the field states by the time of measurement. In
the actual experiment, this erasure in the recombination stage is
possible due to the fact that the interaction between the gravitational field and the masses is small and can be approximated as
“elastic” so that the final state of the field is unentangled with
the masses.5
A second important lesson of the simulation is that, rather
than certifying an entanglement witness, Bell tests would
provide more convincing evidence that a quantum gravitational
effect has been observed. Similarly, concluding a definitive negative experimental outcome would require state tomography.
Much of the literature on possible experimental protocols for
detecting GME focuses somewhat misleadingly on employing
an entanglement witness to certify, or fail to certify, GME.
Consider first the case of the negative experimental outcome,
in which no GME is detected. This measurement would be of
extraordinary consequence for fundamental physics, upending
convictions held by generations of theoretical physicists. It
would immediately falsify all mainstream quantum gravity
theories, such as loop quantum gravity and string theory, as well
as any other approach that claims linearized quantum gravity as
its low energy limit. Such a conclusion would be accepted by the
wider competent community only once extraordinary evidence
is provided. Even after sources of noise have been excluded, it is
likely that scientific consensus would form not with the failure
to verify an entanglement witness but when high-precision state
tomography has been performed. State tomography yields maximal information of the quantum state of the spins and, unlike
a Bell test or an entanglement witness, can certify the complete
absence of entanglement. If precise knowledge of the apparatus
cannot be assumed, an alternative method to detect entanglement may be provided by automated optimizations for fully
black-box approaches.54
Consider next the case of the positive outcome. The detection
of GME would provide empirical evidence for the existence of
quantum gravity, as it would verify a prediction of linearized
quantum gravity. A question that remains is whether a theoryindependent conclusion may also be drawn by invoking the
LOCC-type theorems. The main difficulty in applying these
theorems is that they rely on the assumption of the theory possessing a specific tensor decomposition of the state space. In this
direction, we suggest that a Bell test would considerably
strengthen the case for the importance of detecting GME. The
Bell test, being a theory-independent measurement of nonclassical behavior, does not rely on assumptions about the state space
of an underlying theory but only makes reference to observed
data. The violation of a Bell inequality as a result of the experiment allows for a crisp conclusion: gravitational interactions
create Bell nonlocality. Note that, clearly, one would need to
make sure that there are no other forms of interactions besides
the gravitational ones between the masses during the experiment.
Nonlocality is perhaps the most distinctive of quantum
phenomena.45,48,49,55 It is a resource at the basis of quantum information theory, providing a quantum advantage over classical
computers.56 So, it is fitting that the first glimpse of quantum
gravity might come from the detection of gravity-mediated
nonlocality.
We finally note that the direction of this work is also aligned
with recent research,57,58 where linear optical platforms are used,

036011-6

May∕Jun 2024 • Vol. 3(3)

## PDF page 7

Polino et al.: Photonic implementation of quantum gravity simulator

with different objectives, to study and simulate loop quantum
gravity.
Possible future perspectives could be integrating these studies and extending the GME simulations to new variants of the
proposed experiment.59

Disclosures
The authors declare no competing interest.

Code and Data Availability
All data needed to evaluate the conclusions are presented in this
paper and/or the Supplementary Material.

Acknowledgments
We acknowledge support from the John Templeton Foundation,
The Quantum Information Structure of Spacetime (QISS)
Project (qiss.fr) (the opinions expressed in this paper are those
of the authors and do not necessarily reflect the views of the
John Templeton Foundation) (Grant No. 61466) and QISS2
(Grant No. 62312).

References
1. C. DeWitt-Morette and D. Rickles, Eds., The Role of Gravitation
in Physics: Report from the 1957 Chapel Hill Conference, MaxPlanck-Gesellschaft zur Förderung der Wissenschaften (2011).
2. C. Marletto and V. Vedral, “Gravitationally-induced entanglement
between two massive particles is sufficient evidence of quantum
effects in gravity,” Phys. Rev. Lett. 119, 240402 (2017).
3. S. Bose et al., “A spin entanglement witness for quantum gravity,”
Phys. Rev. Lett. 119, 240401 (2017).
4. T. Krisnanda et al., “Observable quantum entanglement due to
gravity,” NPJ Quantum Inf. 6, 12 (2020).
5. C. Marletto and V. Vedral, “When can gravity path-entangle two
spatially superposed masses?” Phys. Rev. D 98, 046001 (2018).
6. D. Carney, P. C. E. Stamp, and J. M. Taylor, “Tabletop experiments for quantum gravity: a user’s manual,” Classical Quantum
Gravity 36, 034001 (2019).
7. D. L. Danielson, G. Satishchandran, and R. M. Wald,
“Gravitationally mediated entanglement: Newtonian field versus
gravitons,” Phys. Rev. D 105, 086001 (2022).
8. R. Howl, R. Penrose, and I. Fuentes, “Exploring the unification of
quantum theory and general relativity with a Bose–Einstein
condensate,” New J. Phys. 21, 043047 (2019).
9. R. Howl et al., “Non-gaussianity as a signature of a quantum
theory of gravity,” PRX Quantum 2, 010325 (2021).
10. R. J. Marshman, A. Mazumdar, and S. Bose, “Locality and entanglement in table-top testing of the quantum nature of linearized
gravity,” Phys. Rev. A 101, 052110 (2020).
11. D. Carney, H. Müller, and J. M. Taylor, “Using an atom interferometer to infer gravitational entanglement generation,” PRX
Quantum 2, 030330 (2021).
12. A. Kent and D. Pitalúa-Garca, “Testing the nonclassicality of
spacetime: what can we learn from Bell–Bose et al.-MarlettoVedral experiments?” Phys. Rev. D 104, 126030 (2021).
13. H. Chevalier, A. J. Paige, and M. S. Kim, “Witnessing the
non-classical nature of gravity in the presence of unknown interactions,” Phys. Rev. A 102, 022428 (2020).
14. S. Rijavec et al., “Decoherence effects in non-classicality tests of
gravity,” New J. Phys. 23, 043040 (2021).
15. M. Carlesso et al., “Testing the gravitational field generated by a
quantum superposition,” New J. Phys. 21, 093052 (2019).

Advanced Photonics Nexus

16. A. Belenchia et al., “Information content of the gravitational field
of a quantum superposition,” Int. J. Mod. Phys. D 28(14), 1943001
(2019).
17. T. D. Galley, F. Giacomini, and J. H. Selby, “A no-go theorem on
the nature of the gravitational field beyond quantum theory,”
Quantum 6, 779 (2022).
18. D. Carney, “Newton, entanglement, and the graviton,” Phys. Rev.
D 105, 024029 (2022).
19. C. Marletto and V. Vedral, “Interference in quantum field theory:
detecting ghosts with phases,” arXiv:2207.11349 (2022).
20. S. Pal et al., “Experimental localisation of quantum entanglement
through monitored classical mediator,” Quantum 5, 478 (2021).
21. S. Aimet, H. Chevalier, and M. S. Kim, “Gravity mediated
entanglement between light beams as a table-top test of quantum
gravity,” arXiv:2210.12713 (2022).
22. B. Yi et al., “Spatial qubit entanglement witness for quantum
natured gravity,” arXiv:2211.03661 (2022).
23. C. H. Bennett et al., “Concentrating partial entanglement by local
operations,” Phys. Rev. A 53, 2046–2052 (1996).
24. C. H. Bennett et al., “Mixed state entanglement and quantum error
correction,” Phys. Rev. A 54, 3824–3851 (1996).
25. S. Popescu and D. Rohrlich, “Thermodynamics and the measure
of entanglement,” Phys. Rev. A 56, R3319–R3321 (1997).
26. M. Christodoulou and C. Rovelli, “On the possibility of laboratory
evidence for quantum superposition of geometries,” Phys. Lett. B
792, 64–68 (2019).
27. U. Delić et al., “Cooling of a levitated nanoparticle to the motional
quantum ground state,” Science 367, 892–895 (2020).
28. L. Magrini et al., “Real-time optimal quantum control of mechanical motion at room temperature,” Nature 595, 373–377 (2021).
29. F. Tebbenjohanns et al., “Quantum control of a nanoparticle
optically levitated in cryogenic free space,” Nature 595, 378–382
(2021).
30. Y. Margalit et al., “Realization of a complete Stern-Gerlach
interferometer: towards a test of quantum gravity,” Sci. Adv. 7,
eabg2879 (2021).
31. T. Westphal et al., “Measurement of gravitational coupling
between millimeter-sized masses,” Nature 591, 225–228 (2021).
32. S. Barzanjeh et al., “Optomechanics for quantum technologies,”
Nat. Phys. 18(1), 15–24 (2022).
33. J. Oppenheim, “A postquantum theory of classical gravity?” Phys.
Rev. X 13(4), 041040 (2023).
34. P. Pearle, “Combining stochastic dynamical state-vector reduction
with spontaneous localization,” Phys. Rev. A 39, 2277–2289
(1989).
35. I. C. Percival, “Quantum space-time fluctuations and primary
state diffusion,” Proc. R. Soc. Lond. Ser. A Math. Phys. Sci. 451,
503–513 (1995).
36. R. Penrose, “On gravity’s role in quantum state reduction,” Gen.
Relativ. Gravit. 28, 581–600 (1996).
37. L. Diósi, “A universal master equation for the gravitational
violation of quantum mechanics,” Phys. Lett. A 120, 377–381
(1987).
38. A. Bassi et al., “Models of wave-function collapse, underlying
theories, and experimental tests,” Rev. Mod. Phys. 85, 471–527
(2013).
39. V. Fragkos, M. Kopp, and I. Pikovski, “On inference of quantization from gravitationally induced entanglement,” AVS Quantum
Sci. 4(4), 045601 (2022).
40. N. Huggett, N. Linnemann, and M. Schneider, “Quantum gravity
in a laboratory?” arXiv:2205.09013 (2022).
41. M. Christodoulou et al., “Locally mediated entanglement in
linearized quantum gravity,” Phys. Rev. Lett. 130(10), 100202
(2023).
42. G. Bhole et al., “Witnesses of non-classicality for simulated hybrid
quantum systems,” J. Phys. Commun. 4, 025013 (2020).
43. J. L. O’Brien et al., “Demonstration of an all-optical quantum
controlled-NOT gate,” Nature 426, 264–267 (2003).

036011-7

May∕Jun 2024 • Vol. 3(3)

## PDF page 8

Polino et al.: Photonic implementation of quantum gravity simulator
44. D. F. V. James et al., “On the measurement of qubits,” Phys. Rev. A
64, 052312 (2001).
45. R. Horodecki et al., “Quantum entanglement,” Rev. Mod. Phys.
81, 865–942 (2009).
46. N. Friis et al., “Entanglement certification: from theory to experiment,” Nat. Rev. Phys. 1, 72–87 (2019).
47. J. F. Clauser et al., “Proposed experiment to test local hiddenvariable theories,” Phys. Rev. Lett. 23, 880–884 (1969).
48. J. S. Bell, “On the Einstein Podolsky Rosen paradox,” Phys.
Physique Fizika 1, 195–200 (1964).
49. N. Brunner et al., “Bell nonlocality,” Rev. Mod. Phys. 86, 419–478
(2014).
50. C. Marletto and V. Vedral, “Witnessing non-classicality beyond
quantum theory,” Phys. Rev. D 102, 086012 (2020).
51. C. Anastopoulos and B.-L. Hu, “Comment on ‘A spin entanglement
witness for quantum gravity” and on “gravitationally induced
entanglement between two massive particles is sufficient evidence
of quantum effects in gravity,’” arXiv:1804.11315 (2018).
52. C. Anastopoulos, M. Lagouvardos, and K. Savvidou, “Gravitational
effects in macroscopic quantum systems: a first-principles analysis,”
Classical Quantum Gravity 38, 155012 (2021).
53. S. Bose et al., “Mechanism for the quantum natured gravitons to
entangle masses,” Phys. Rev. D 105, 106028 (2022).
54. D. Poderini et al., “Ab initio experimental violation of Bell
inequalities,” Phys. Rev. Res. 4(1), 013159 (2022).
55. B. Dakic and Č. Brukner, “Quantum theory and beyond: is entanglement special?” in Deep Beauty: Understanding the Quantum
World through Mathematical Innovation, H. Halvoroson, Ed.,
pp. 365–392, Cambridge University Press (2009).
56. M. A. Nielsen and I. L. Chuang, Quantum Computation and
Quantum Information, 10th anniversary ed., Cambridge University
Press, Cambridge; New York (2010).
57. L. Cohen et al., “Efficient simulation of loop quantum gravity: a
scalable linear-optical approach,” Phys. Rev. Lett. 126(2), 020501
(2021).
58. R. van der Meer et al., “Experimental simulation of loop quantum
gravity on a photonic chip,” NPJ Quantum Inf. 9(1), 32 (2023).
59. E. Martín-Martínez and T. R. Perche, “What gravity mediated
entanglement can really tell us about quantum gravity,” Phys.
Rev. D 108(10), L101702 (2023).
Emanuele Polino received his PhD in 2020 from the Physics Department
of Sapienza University of Rome. Then, he was a postdoc in the Physics
Department of Sapienza University, working on photonic technologies for
quantum foundations studies and quantum information tasks. In particular, he worked on fundamental tests of nonlocality in causal structures and
quantum metrology. Currently, he is working as a postdoc at the Centre
for Quantum Dynamics with a focus on quantum nonlocality.
Beatrice Polacchi is currently a postdoctoral researcher at the Physics
Department of Sapienza University of Rome, in the Quantum Lab led by
Prof. Fabio Sciarrino. She will soon obtain her PhD in physics with a thesis entitled “Quantum networks on a hybrid photonic platform.” Her main
fields of research are quantum information and quantum optics, with
works on certification of quantum networks, quantum foundations, blind

Advanced Photonics Nexus

quantum computing, and hybrid building blocks for photonic quantum
networks.
Davide Poderini received his PhD in 2021 from Sapienza University of
Rome, with a thesis on experimental quantum optics and causal inference
in quantum information. Since then, he has been working as a postdoc at
the International Institute of Physics of Natal, Brazil. His main research
interests include various topics in quantum information and foundations,
such as classical and quantum causal modeling, quantum networks,
quantum cryptography, and quantum opt1ics.
Iris Agresti received her PhD in 2020 with an experimental thesis in
quantum information. She is a senior postdoc in Professor Philip
Walther’s group at the University of Vienna. Since 2021, she has been
a fellow of the "Early Stage Program of Research Training and
Innovation" offered by the Austrian Science Fund. Her main fields of research are quantum information and quantum computation, with works on
quantum foundations, quantum machine learning, and boson sampling.
Gonzalo Carvacho graduated in 2014 at the University of Concepción.
In 2017, he received his PhD from Sapienza University of Roma with a
thesis on “Multiphoton hybrid systems and their applications in quantum
information and quantum communication.” Currently, he works as a
lecturer at the Sapienza University. His research fields are foundational
and practical implications of quantum causality with different photonic
platforms as well as field quantum communications through hybrid technologies.
Fabio Sciarrino received his PhD in 2004 with a thesis in experimental
quantum optics. He is a full professor and a head of the Quantum Lab in
the Department of Physics of Sapienza Università di Roma. Since 2013,
he has been a fellow of the Sapienza School for Advanced Studies. His
main field of research is quantum information and quantum optics, with
works on quantum teleportation, optimal quantum machines, fundamental
tests, quantum communication, and orbital angular momentum.
Andrea Di Biagio is a postdoctoral researcher at IQOQI Vienna. His research focuses on low-energy quantum gravity experiments and quantum
field theory, and on foundational topics such as the time-orientation of
probability and the interpretation of quantum mechanics. He received
his PhD in 2022.
Carlo Rovelli’s research interests are loop quantum gravity, relational
quantum mechanics, and the history and philosophy of science. He is a
professor at Aix-Marseille University, an associate member of the Rotman
Institute of Philosophy, an adjunct professor in the Department of
Philosophy at Western University, and a distinguished visiting research
chair at the Perimeter Institute. He is the founder of the quantum gravity
group of the Centre de Physique Théorique of the Aix-Marseille University.
Marios Christodoulou is an independent research group leader at the
Institute for Quantum Optics and Quantum Information, Vienna. His research interests include tests for tabletop quantum gravity, black holes,
quantum information theory, and loop quantum gravity.

036011-8

May∕Jun 2024 • Vol. 3(3)
