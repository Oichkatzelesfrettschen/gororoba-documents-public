Source: see manifest row of the PDF
PDF sha256: bda025fd53596564354370f8cb9d9482f6eb7f9cda2e2a4add518aa9d63f2fd8
License: CC-BY-4.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of mi_2021_time_crystalline_eigenstate_order_quantum_processor.pdf

Transcription of `mi_2021_time_crystalline_eigenstate_order_quantum_processor.pdf` in this directory, 7 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-7 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Article

Time-crystalline eigenstate order on a
quantum processor
https://doi.org/10.1038/s41586-021-04257-w
Received: 30 July 2021
Accepted: 17 November 2021
Published online: 30 November 2021
Open access
Check for updates

Xiao Mi1,11, Matteo Ippoliti2,11, Chris Quintana1, Ami Greene1, Zijun Chen1, Jonathan Gross1,
Frank Arute1, Kunal Arya1, Juan Atalaya1, Ryan Babbush1, Joseph C. Bardin1,3, Joao Basso1,
Andreas Bengtsson1, Alexander Bilmes1, Alexandre Bourassa1,4, Leon Brill1,
Michael Broughton1, Bob B. Buckley1, David A. Buell1, Brian Burkett1, Nicholas Bushnell1,
Benjamin Chiaro1, Roberto Collins1, William Courtney1, Dripto Debroy1, Sean Demura1,
Alan R. Derk1, Andrew Dunsworth1, Daniel Eppens1, Catherine Erickson1, Edward Farhi1,
Austin G. Fowler1, Brooks Foxen1, Craig Gidney1, Marissa Giustina1, Matthew P. Harrigan1,
Sean D. Harrington1, Jeremy Hilton1, Alan Ho1, Sabrina Hong1, Trent Huang1, Ashley Huff1,
William J. Huggins1, L. B. Ioffe1, Sergei V. Isakov1, Justin Iveland1, Evan Jeffrey1, Zhang Jiang1,
Cody Jones1, Dvir Kafri1, Tanuj Khattar1, Seon Kim1, Alexei Kitaev1, Paul V. Klimov1,
Alexander N. Korotkov1,5, Fedor Kostritsa1, David Landhuis1, Pavel Laptev1, Joonho Lee1,6,
Kenny Lee1, Aditya Locharla1, Erik Lucero1, Orion Martin1, Jarrod R. McClean1, Trevor McCourt1,
Matt McEwen1,7, Kevin C. Miao1, Masoud Mohseni1, Shirin Montazeri1, Wojciech Mruczkiewicz1,
Ofer Naaman1, Matthew Neeley1, Charles Neill1, Michael Newman1, Murphy Yuezhen Niu1,
Thomas E. O’Brien1, Alex Opremcak1, Eric Ostby1, Balint Pato1, Andre Petukhov1,
Nicholas C. Rubin1, Daniel Sank1, Kevin J. Satzinger1, Vladimir Shvarts1, Yuan Su1, Doug Strain1,
Marco Szalay1, Matthew D. Trevithick1, Benjamin Villalonga1, Theodore White1, Z. Jamie Yao1,
Ping Yeh1, Juhwan Yoo1, Adam Zalcman1, Hartmut Neven1, Sergio Boixo1, Vadim Smelyanskiy1,
Anthony Megrant1, Julian Kelly1, Yu Chen1, S. L. Sondhi8,9, Roderich Moessner10,
Kostyantyn Kechedzhi1, Vedika Khemani2 ✉ & Pedram Roushan1 ✉

Quantum many-body systems display rich phase structure in their low-temperature
equilibrium states1. However, much of nature is not in thermal equilibrium.
Remarkably, it was recently predicted that out-of-equilibrium systems can exhibit
novel dynamical phases2–8 that may otherwise be forbidden by equilibrium
thermodynamics, a paradigmatic example being the discrete time crystal
(DTC)7,9–15. Concretely, dynamical phases can be defined in periodically driven
many-body-localized (MBL) systems via the concept of eigenstate order7,16,17.
In eigenstate-ordered MBL phases, the entire many-body spectrum exhibits
quantum correlations and long-range order, with characteristic signatures in
late-time dynamics from all initial states. It is, however, challenging to experimentally
distinguish such stable phases from transient phenomena, or from regimes in which
the dynamics of a few select states can mask typical behaviour. Here we implement
tunable controlled-phase (CPHASE) gates on an array of superconducting qubits to
experimentally observe an MBL-DTC and demonstrate its characteristic
spatiotemporal response for generic initial states7,9,10. Our work employs a
time-reversal protocol to quantify the impact of external decoherence, and leverages
quantum typicality to circumvent the exponential cost of densely sampling the
eigenspectrum. Furthermore, we locate the phase transition out of the DTC with an
experimental finite-size analysis. These results establish a scalable approach to
studying non-equilibrium phases of matter on quantum processors.
In an equilibrium setting, quantum phases of matter are classified
by long-range order or broken symmetries in low-temperature
states (Fig. 1a). The existence of ordered phases in periodically
driven (Floquet) systems, on the other hand, is counterintuitive: as
energy is not conserved, one expects thermalization to a featureless

maximum-entropy state that is incompatible with quantum order.
However, this heat death is averted in the presence of many-body localization, where strong disorder causes the emergence of an extensive
number of local conservation laws that prevent thermalization18–23,
making it possible to stabilize intrinsically dynamical phases7.

A list of affiliations appears at the end of the paper.

Nature | Vol 601 | 27 January 2022 | 531

## PDF page 2

Article
Ordered

Ĥ (t) = Ĥ 0

~
– |01001〉
– |10110〉

b

c

Energy

a

Experimentally observing a non-equilibrium phase such as the
MBL-DTC is a challenge owing to limited programmability, coherence
and size of noisy intermediate-scale quantum hardware. Subharmonic
response, by itself, is not a unique attribute of the MBL-DTC; rather, it
is a feature of many dynamical phenomena whose study has a rich history24 (also Ch. 8 in ref. 12). Most recently, interesting DTC-like dynamical
signatures have been observed in a range of quantum platforms from
trapped ions25 to nitrogen vacancy centres26 to NMR spins27,28. However,
each of these platforms lacks one or more necessary conditions for stabilizing an MBL-DTC12,29, either owing to an absence of the requisite type
of disorder25,27 or owing to the interactions being too long ranged26–28.
The observed signatures, instead, have been shown to arise from slow
thermalization26,30, effectively mean-field dynamics28, or prethermal
dynamics from special initial states12,29,31,32, and are separated from
the MBL-DTC by a spectral phase transition where eigenstate order
disappears. Thus, despite the recent progress, observing an MBL-DTC
remains an outstanding challenge12,29.
Here we perform the following necessary benchmarks for experimentally establishing an eigenstate-ordered non-equilibrium phase of matter:
drive parameters are varied to demonstrate stability of the phase in an
extended parameter region and across disorder realizations; the limitations of finite size and finite coherence time are addressed, respectively,
by varying system size and verifying that any decay of the subharmonic
response is consistent with purely extrinsic decoherence assessed in an
independent experiment; the existence of spatiotemporal order across
the entire spectrum is established. The flexibility of our quantum processor, combined with the scalable experimental protocols devised in
the following, allows us to fulfil these criteria and observe an MBL-DTC.
The experiment is conducted on an open-ended, linear chain of L = 20
superconducting transmon qubits (Q1 to Q20) that are isolated from a
two-dimensional grid. We drive the qubits via a time-periodic (Floquet)
t
circuit Û F with t identical cycles (Fig. 2a) of ÛF:

Unordered

Ĥ (t + T ) = Ĥ (t)

~ |00000〉 – |11111〉
–
~
– |00000〉 + |11111〉

~ |01001〉
–
– |10110〉

Fig. 1 | Order in eigenstates. a, Equilibrium phases are characterized by
long-range order in low-energy eigenstates of time-independent Hamiltonians
(for example, an Ising ferromagnet with a pair of degenerate ground states that
resemble ‘Schrödinger cats’ of polarized states). b, Thermalizing Floquet
systems typically have no ordered states in the spectrum. c, In MBL Floquet
systems, every eigenstate can show order. In MBL-DTC, every eigenstate
resembles a long-range ordered ‘Schrödinger cat’ of a random configuration of
spins and its inversion, with even/odd superpositions split by π.

Dynamics in a Floquet system is governed by a unitary time evolution
operator, whose eigenvalues lie on the unit circle. While the entire Floquet
spectrum is featureless in a thermalizing phase (Fig. 1b), an MBL Floquet
phase can have an order parameter associated with each eigenstate. As an
example, in the spatiotemporally ordered MBL-DTC, the spectrum has a
distinctive pattern of pairing between long-range ordered ‘Schrödinger
cat’ eigenstates whose eigenvalues are separated by an angle π (refs. 7,9,10;
Fig. 1c). This pairing manifests as a stable subharmonic response, wherein
local observables show period-doubled oscillations that spontaneously
break the discrete time translation symmetry of the drive for infinitely
long times. The unique combination of spatial long-range order and time
translation symmetry breaking in an isolated dissipation-free quantum
many-body system is the hallmark of the MBL-DTC.

Random Ii and hi

Q3: 0

0

1

Q4: 1

0

0

Xg

Q5: 1

1

0

Xg

...

...

Q20: 0

0

1

Xg
Xg

Disorder and initial-state averaged autocorrelators
1.0

...

Z (h2)

...

Z (h3)

...

Z (h4)

...

Z (h5)

...

Z (h20)

...

...

....

c

Xg

0

Thermal

–0.5

d

MBL-DTC

10

g = 0.97,

1.0

Q11

Q11

0.5

〈Ẑ (t)〉

–1.0
0

10

t

20

Qubit

Instance 1
Instance 2
Instance 3
Instance 4
Instance 5

0

20

40

t

60

80

100

0

20

40

60

t

100

80

MBL-DTC (g = 0.97)

0
–0.5
–1.0
20

Ā /Ā 0

15

0.5

1.0

10

0

5

–0.5
–1.0
0

Fig. 2 | Observing an MBL-DTC. a, The experimental circuit composed of t
identical cycles of the unitary ÛF. The local polarization of each qubit, ⟨ Zˆ (t )⟩,
is measured at the end. In the following panels, we investigate a number of
disorder instances each with a different random bit-string initial state.
b, Experimental values of ⟨ Zˆ (t )⟩ measured at Q11. Data are shown for five
representative circuit instances deep in the thermal (g = 0.60; left) and
MBL-DTC (g = 0.97; right) phases. c, Autocorrelator A = ⟨Zˆ (0)Zˆ (t )⟩ at Q11,

532 | Nature | Vol 601 | 27 January 2022

t

20

Thermal (g = 0.60)

g = 0.60,

0

g = 0.97, Q11

g = 0.60, Q11
0

0.5

–0.5

Ā 0 (ÛECHO)

(ÛF† )t

ÛFt

–1.0

Ā /Ā 0

1.0

Ā (ÛFt )

Ā 0 (ÛECHO)

ÛECHO

ÛF = (×t cycles)

b

Ā (ÛFt )

0.5

...

1

ZZ (I2)

0

ZZ (I4)

Q2: 1

ZZ (I1)

1

...

0

Q1: 0

Z (h1)

ZZ (I3)

Xg

〈Ẑ (t)〉

〈Ẑ (0)Ẑ (t)〉

a Random bit strings

10

20
t

0

20

40

60

80

100

t

obtained from averaging the results of 36 circuit instances. For the same circuit
†
t
instances, the average autocorrelator at the output of UˆECHO = (Uˆ F)t Uˆ F is also
measured and its square root, A 0, is shown alongside A for comparison. The left
(right) panels correspond to g = 0.60 (0.97). d, Top panels: the ratio A /A 0
obtained from c. Bottom panels: A /A 0 as a function of t and qubit location.
The left (right) panels correspond to g = 0.60 (0.97) .

## PDF page 3

1.0

Ii ∈[–1.5π, –0.5π]

Ii = –0.4

c

Initial state 1: 00000000000000000000
Q12
Q11
0.5

〈Ẑ (t)〉

0
–0.5

Néel
Polarized
Random

0

20

b

t

20

P = 0.140
V = 0.018

|[Ā ]|
20

t

40

60

P = 0.391
V = 0.015

0.4
0.3

Ii ∈[–1.5π, –0.5π]

0.5

Ii ∈[–1.5π, –0.5π]

Ii = –0.4

30

]2

0

]1

–0.5
30

40

50

60

30

40

50

60

]r =
30

40

|]1 − ]2|
|]1 + ]2|
50

d

]¯ r

20

0

0.2

0.4

0.6

Ii ∈[–1.5π, –0.5π]

0.2

0.8

1.0
1.0

Ii = –0.4

–2

10

–1
0
1
2
Approximate energy (a.u.)

50

60

Ii ∈[–1.5π, –0.5π]
Ii = –0.4

0.4
0.2
0

0.15

0.20

0.25

0.30

0.35

0.40

0

Fig. 3 | Distinguishing MBL-DTC from prethermal phenomena. a, Site- and
disorder-averaged autocorrelators [A ] measured with g = 0.94. In the left panel
(MBL-DTC), each dataset is averaged over 24 disorder instances of ϕi and hi, with
the initial state fixed at one of the following: Néel, |01 ⊗10; polarized, |0 ⊗20;
random, |00111000010011001111⟩. In the right panel (prethermal), the same
values of hi and initial states are used but ϕi = −0.4. b, Histograms of [A ] , from
500 random bit-string initial states, averaged over cycles 30 and 31 and the same
disorder instances as in a. The standard deviation (mean) of [A ] , σ (μ), is also
listed. Location of the polarized (Néel) state is indicated by a purple (red) arrow.

−

i
h Zˆ
2∑ i i

e i


longitudinal fields

−

i
ϕ Zˆ Zˆ
4 ∑ i i i +1

ei


Ising interaction

20

40

60
t

|[Ā ]|

ÛF =

40

0.6
10
5

0
0.10

Ii = –0.4
30

0.8

15
0.1

60

t

Qubit

Number of states

60 0

40

0

–0.5

Néel
Polarized
Random

〈Ẑ (t)〉

[Ā ]

0.5

–1.0

Initial state 2: 00000000001000000000
Q13
Q14

]¯ r

a

i
− πg ∑ Xˆi
2

e i


(1)

x rotation by πg

where X̂i and Ẑi are Pauli operators. Each angle ϕi (hi ) is sampled randomly from [−1.5π,− 0.5π]([−π, π]) for every realization of the circuit.
Overall, ÛF implements an interacting Ising model that is periodically
‘kicked’ by a transverse pulse that rotates all qubits by πg about the
x axis. In this work, g is tuned within the range [0.5, 1.0]to explore the
DTC phase and its transition into a thermal phase. At g = 1, the model
implements a π pulse that exactly flips all qubits (in the z basis) and
returns them to the initial state over two periods. A key signature of
the DTC is the presence of robust period doubling, (that is, extending
over a finite extent in parameter space, even as g is tuned away from 1,
and for all initial states). Strong Ising interactions, which produce
long-range spatial order, are essential for this robustness7,10. This is in
contrast to a system of decoupled qubits (ϕ = 0) that rotate by a continuously varying angle πg every period instead of being locked at
period doubling. Prior theoretical work29 has shown that model (1) is
expect the range g > gc, and transition to a thermal phase at a critical
value gc ≈ 0.84.
Achieving MBL in this model for g ∼ 1 requires disorder in the twoqubit interaction, ϕi , which is even under Ising symmetry12,29, πi Xˆi , a
condition that was not met by some past DTC experiments25,27. Ising-odd
terms (that is, hi) are approximately dynamically decoupled by the x
pulses over two periods, thereby lowering their effective disorder
strength and hindering localization (in the absence of independent
disorder in the ϕi); see Appendix A in ref. 29. Utilizing continuously tunable CPHASE gates, described further in the Supplementary Information, allows us to engineer strong disorder in ϕi to fulfil this key
requirement. Recently, a complementary approach to MBL-DTC using
nuclear spins in diamond has also come into fruition33.

80

100 0

20

40

60
t

80

100

5

10
15
Qubit

20

Inset: same collection of [A ] plotted over the energies of the bit-string states,
calculated from the effective Hamiltonian Ĥeff approximating the drive (see
text). Dashed lines show averaged values within energy windows separated by
0.2. c, ⟨ Zˆ (t )⟩ for two bit-string initial states that differ only at Q 11. Top panel
shows a single circuit instance with disordered ϕi and bottom panel shows an
instance with uniform ϕi = −0.4. d, Left and middle panels: relative difference
between the two signals ζr as a function of t and qubit location, averaged over
time windows of 10 cycles and over 64 disorder instances for ÛF and 81 instances
for ÛF′. Right panel: qubit dependence of ζr, averaged from t = 51 to t = 60.

We first measure the hallmark of an MBL-DTC: the persistent oscillation of local qubit polarizations ⟨ Zˆ(t)⟩at a period twice that of ÛF,
irrespective of the initial state7,9,12,29. This subharmonic response is
probed using a collection of random bit-string states (for example,
|01011...⟩, where 0 (1) denotes a single-qubit ground (excited) state in
the z basis). For each bit-string state, we generate a random instance
of ÛF, and then measure ⟨ Zˆ(t)⟩ every cycle. Figure 2b shows ⟨ Zˆ(t)⟩in a
few different instances for a qubit near the centre of the chain, Q11,
measured with g = 0.60and g = 0.97. The former is deep in the thermal
phase, and indeed we observe rapid decay of ⟨ Zˆ(t)⟩ towards 0 within
10 cycles for each instance. In contrast, for g = 0.97, ⟨ Zˆ(t)⟩ shows large
period-doubled oscillations persisting to over 100 cycles, suggestive
of an MBL-DTC phase. The disorder-averaged autocorrelator,
A = ⟨Zˆ(0)Zˆ(t)⟩, shows similar features (Fig. 2c).
We note that the data for g = 0.97are modulated by a gradually decaying envelope, which may arise from either external decoherence or
slow internal thermalization26,30. To establish DTC, additional measurements are needed to quantify the impact of decoherence. This is
†
t
achieved via an ‘echo’ circuit UˆECHO = (UˆF)t UˆF that reverses the time
evolution after t steps (see Supplementary Information). Deviations
of ÛECHO from the identity operation are purely due to decoherence,
and can be quantified via decay of the autocorrelator
†
A0 ≡ (⟨ZˆUˆECHO ZˆUˆECHO⟩)1/2 (the square root accounts for the fact that
t
ÛECHO acts twice as long as Û F). Time-reversal techniques were also
recently used in an investigation of DTC in NMR systems27 and the study
of out-of-time-ordered commutators34.
Comparison between the disorder-averaged A0 and A reveals qualitatively different behaviours in the two phases (Fig. 2c). In the thermal
phase g = 0.60, A approaches 0 much more quickly than A0 does, indicating that the observed decay of A is mostly induced by intrinsic thermalization. In the MBL-DTC phase g = 0.97, A0 nearly coincides with the
envelope of A , suggesting that decay of the latter is primarily induced
Nature | Vol 601 | 27 January 2022 | 533

## PDF page 4

Article

534 | Nature | Vol 601 | 27 January 2022

for disordered ϕi. This slow propagation provides another experimental diagnostic in support of MBL.
Our measurement of [A ]for 500 initial states in Fig. 3d provides clear
evidence of initial-state independence. Still, a direct sampling of states
is practically limited to small fractions of the computational basis
(0.05% in this case) and would suffer from the exponential growth of
the Hilbert space on larger systems. A more scalable alternative is to
use random, highly entangled states to directly measure spectrally
averaged quantities (quantum typicality37–39; see Supplementary Information). The autocorrelator A averaged over all 2 L bit strings agrees,
up to an error exponentially small in L, with Aψ = ⟨ψ Zˆ(0)Zˆ(t) ψ ⟩, where
|ψ ⟩ is a typical Haar-random many-body state in the Hilbert space of L
qubits. We prepare such a state by evolving a bit string with a random
circuit ÛS of variable depth K (Fig. 4b), and couple an ancilla qubit to
the system to measure the two-time operator Zˆ(0)Zˆ(t)(Fig. 4a). Experimental results for the error-mitigated, spectrally averaged signal
Aψ /Aψ,0 on qubit Q11 (Fig. 4c) show behaviour consistent with a stable
MBL-DTC. The effect of the state-preparation circuit ÛS is illustrated
by the dependence of σ for Aψ on K . As shown in Fig. 4d, σ steadily
decreases as K increases, reducing from a value of 0.025 at K = 0 to a
value of 0.006 at K = 20, while μ remains largely unchanged. This is
consistent with the fact that|ψ⟩ becomes closer to a Haar-random state
as K increases. We use a single disorder instance to study the convergence of the quantum typicality protocol because disorder averaging
independently leads to narrow distributions even for K = 0 (Fig. 3b).
Results for prethermal and thermalizing dynamics are shown in Supplementary Fig. 10.
The scaling with L of the spectrally averaged autocorrelator, at a time
t ∼ poly(L), provides a sharp diagnostic: this saturates to a finite value

〈\|Ẑ (0)Ẑ (t)|\〉 = 〈X̂ 〉a

...

Q11

ÛFt

ÛS
CZ

R1,1

R1,2

R1,K

R2,1

R2,2

R2,K

R20,1

Q11, g = 0.94

0
A\(ÛFt )
A\,0 (ÛECHO)

–1.0
1.0
0.5
0

–0.5

R20,K

K=0
K=2
K = 20

40 V (P) =
0.006
20 (0.396)

0.5

–0.5

R20,2

d

0
Number of states

〈\|Ẑ (0)Ẑ (t)|\〉

1.0

–1.0

Cycle K

Cycle 2

Random single-qubit rotations
CZ

Q20

c

K~L

Cycle 1

|\〉

...

...

Q2

Random state

K=0

...

Q1

|Bit string〉

Qa: |+X〉

b |\〉: Product state

...

a

A\/A\,0

by decoherence. We also find, consistent with theoretical models (see
Supplementary Section IV), that the reference signal A0 may be used to
normalize A and reveal its ideal behaviour: A /A0, shown in the upper
panels of Fig. 2d, decays rapidly for g = 0.60 but retains near-maximal
amplitudes for g = 0.97 . Similar contrast between the two phases is
seen in the error-mitigated autocorrelators A /A0 for all qubits (bottom
panels of Fig. 2d). The observation of a stable noise-corrected subharmonic response is suggestive of an MBL-DTC phase.
We now demonstrate the insensitivity of the subharmonic response
to the choice of initial states, a necessary consequence of eigenstate
order. In contrast, various prethermal mechanisms in driven systems
predict strong dependence of the thermalization rate on the initial state
(for example, through its quantum numbers27,32 or its energy under an
effective time-independent Hamiltonian Ĥeff (refs. 31,35,36) that approximately governs the dynamics for small system sizes and/or finite times).
To elucidate this aspect of the MBL-DTC phase, we measure in detail the
distribution of autocorrelator values over initial bit-string states.
We begin by examining the position- and disorder-averaged autocorrelator [A ] over three representative bit-string initial states, shown in
the left panel of Fig. 3a. The square brackets indicate averaging over
qubits in the chain. The three time traces are nearly indistinguishable.
This behaviour is in clear contrast with a model without eigenstate
′
order, implemented by a family of drives Û F where the ϕi angles are set
to a uniform value, ϕi = −0.4. Note that this value of ϕi = −0.4 is chosen
to be small enough that a leading-order high-frequency Floquet–
Magnus expansion to obtain Ĥeff is a reasonable approximation
(see Supplementary Information). Without disorder in the ϕi, the drive
′
Û F is not asymptotically localized but exhibits prethermal DTC-like
′
behaviour (see Methods). Here, [A ] for Û F (disorder averaged over
random hi alone), shown in the right panel of Fig. 3a, reveals markedly
different decay rates for the three states. The random bit-string state,
in particular, decays faster than the polarized or Néel states.
A more comprehensive analysis is based on sampling the absolute
values of [A ] for 500 random initial bit-string states (Fig. 3b). For the
MBL-DTC ÛF, the histogram is symmetrical with a mean μ = 0.391. Here
the non-zero standard deviation σ probably arises from finite experimental accuracy and number of disorder instances, as analysis in the
Supplementary Information shows that [A ]is independent of the initial
′
state. In contrast, the Û F model has a significantly lower mean μ = 0.140.
Moreover, the histogram is asymmetrical, with outliers at high [A ]
including the polarized and Néel states (51% and 88% higher than the
mean, respectively). These two states are special because they are lowtemperature states that sit near the edge of the spectrum of Ĥeff (see
Supplementary Information). Plotting the autocorrelator [A ] against
the energy of each bit string under Ĥeff , in the inset of Fig. 3b, reveals a
clear correlation. No such correlation is present in the MBL model.
Independent confirmation of MBL as the mechanism underlying the
stability of DTC is achieved by characterizing the propagation of correlations. In MBL dynamics, local perturbations spread at most logarithmically in time20, as opposed to algebraic ( ∼t α) spreading in
thermalizing dynamics. We prepare two initial bit-string states differing by only a single bit flip at Q11 and measure ⟨ Zˆ(t)⟩ for each site in both
states (Fig. 3c). It can be seen that the difference in the two signals, ζ1
and ζ2, decays rapidly with the distance from Q11 for disordered ϕi and
becomes undetectable at Q14. On the other hand, for uniform ϕi = −0.4,
ζ1 and ζ2 have a much more pronounced difference that remains significant at Q14 . This difference is further elucidated by the ratio
ζr = |ζ1 − ζ2|/(|ζ1| + |ζ2|), shown in Fig. 3d. Physically, ζr corresponds to the
relative change in local polarization as a result of the bit flip, and is
inherently robust against qubit decoherence (see Supplementary
Information). We observe that up to t = 100, ζr remains sharply peaked
around the initial perturbation (Q11) for disordered ϕi . In contrast, a
propagating light cone is visible for ϕi = −0.4, with the perturbation
reaching all qubits across the chain as t increases. The spatial profiles
of ζr at t = 51 to t = 60(right panel of Fig. 3d) show that ζr is much sharper

40 0.012
(0.400)
20
0
0.025
40 (0.405)
20

0

20

40

60

t

80

100

0

0.35

0.40

0.45

[A\]

Fig. 4 | Probing average spectral response via quantum typicality.
a, Scheme for measuring the autocorrelator, A ψ = ⟨ψ Zˆ (0)Zˆ (t ) ψ⟩, on Q 11, of a
scrambled quantum state |ψ⟩. |ψ⟩ is created by scrambling a bit-string state with
a circuit ÛS. The x-axis projection of an ancilla qubit Q a, X̂ a, is measured at the
end. b, ÛS contains K layers of controlled-Z (CZ) gates interleaved with random
single-qubit rotations, Ri, k, around a random axis along the equatorial plane of
the Bloch sphere by an angle ∈[0.4π , 0.6π ]. c, Upper panel: A ψ for a single
disorder instance with K = 20 cycles in ÛS. The square root of the autocorrelator,
t
obtained by replacing Û F with ÛECHO, A ψ,0, is also shown. Bottom panel:
normalized autocorrelator, A ψ /A ψ,0, as a function of t. d, Histograms of A ψ
from a single disorder instance, averaged over cycles 30 and 31. Each histogram
corresponds to a different number of scrambling cycles, K , and includes data
from 500 random initial bit-string states before ÛS.

## PDF page 5

in the MBL-DTC, while it scales to zero with increasing L in the thermal
phase and in prethermal cases where, for instance, a vanishing fraction
of the spectrum of an appropriate Ĥeff shows order (see Supplementary
Information). While the averaged autocorrelator may be unduly
affected by outlier states and/or long (but O(1)) thermalization times
at small system sizes and times (thereby making the complementary
bit-string analysis of Fig. 3 essential), the polynomial scaling of this
protocol establishes a proof of principle for efficiently verifying the
presence or absence of an MBL-DTC in a range of models as quantum
processors scale up in size to surpass the limits of classical simulation40.
Finally, we systematically vary g in small increments and obtain an
experimental finite-size analysis to establish the extent of the MBL
phase and the transition out of it. Defining phases of matter, whether
in or out of equilibrium, requires a limit of large system size. Thus, it is
important to examine the stability of the MBL-DTC and thermalizing
regimes observed in our finite-size quantum processor as the size of
the system is increased. To address this, we measure an Edwards–Anderson spin-glass order parameter41,42

χ SG =

1
2
∑′ ⟨Zˆ Zˆ ⟩
L − 2 i≠ j i j

(2)

simulability. The efficient verification of eigenstate order can inspire a
general strategy for establishing whether a desired property, such as a
particular phase, is in fact present in a quantum processor.

Online content
Any methods, additional references, Nature Research reporting summaries, source data, extended data, supplementary information,
acknowledgements, peer review information; details of author contributions and competing interests; and statements of data and code availability are available at https://doi.org/10.1038/s41586-021-04257-w.
1.
2.

3.
4.
5.

6.
7.

(the primed sum excludes edge qubits Q1, Q L), as a function of time.
This quantity measures the persistence of random (‘glassy’) spatial
patterns in the initial bit-string state: at late times, χSG vanishes with
increasing L in the thermalizing phase g < gc, while it is extensive in the
MBL-DTC g > gc. As a result, it is expected to show a finite-size crossing
at g ≃ gc (although the precise location is subject to strong finite-size
and finite-time drifts43,44). Experimentally, χ SG is constructed from
bit-string samples obtained by jointly reading out all qubits and then
averaged over cycles and disorder instances (Fig. 5). The size of the
qubit chain is varied by restricting the drive ÛF to contiguous subsets
of 8, 12 and 16 qubits (as well as the entire 20-qubit chain). We observe
increasing (decreasing) trends in χ SG versus L when g is above (below)
a critical value gc. The data indicate 0.83 ≲ gc ≲ 0.88, consistent with
numerical simulations (see Supplementary Information).
In conclusion, we have demonstrated the possibility of engineering and
characterizing non-equilibrium phases of matter on a quantum processor,
providing the experimental observation of an MBL-DTC. The scalability of
our protocols sets a blueprint for future studies of non-equilibrium phases
and phase transitions on complex quantum systems beyond classical

8.
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

0.03

g = 0.90

FSG

0.025

FSG

Spin-glass order parameter, FSG

0.030

0.0022
0.0020
0.0018
0.0016

23.
24.
25.
26.

0.020

0.02

g = 0.78

27.
28.
8

0.01

12

16

Number of qubits, L

20

29.

L=8
L = 12
L = 16
L = 20

0
0.72

0.74

0.76

0.78

0.82

0.80

0.84

0.86

0.88

0.90

g
Fig. 5 | Estimating phase transition by varying system size.
Disorder-averaged spin-glass order parameter χ SG as a function of g for
different chain lengths L, measured between t = 51 and t = 60. Error bars
correspond to statistical errors alone and do not include hardware (for
example, gate) errors. Inset shows the size dependence of χ SG for two different
values of g. See Methods for measurement details.

30.
31.
32.
33.
34.
35.

36.
37.

Wen, X.-G. Quantum Field Theory of Many-Body Systems: From the Origin of Sound to an
Origin of Light and Electrons (Oxford Univ. Press, 2007).
Bukov, M., D’Alessio, L. & Polkovnikov, A. Universal high-frequency behavior of
periodically driven systems: from dynamical stabilization to Floquet engineering. Adv.
Phys. 64, 139–226 (2015).
Harper, F., Roy, R., Rudner, M. S. & Sondhi, S. Topology and broken symmetry in Floquet
systems. Annu. Rev. Condens. Matter Phys. 11, 345–368 (2020).
Oka, T. & Aoki, H. Photovoltaic Hall effect in graphene. Phys. Rev. B 79, 081406 (2009).
Rudner, M. S., Lindner, N. H., Berg, E. & Levin, M. Anomalous edge states and the
bulk-edge correspondence for periodically driven two-dimensional systems. Phys. Rev. X
3, 031005 (2013).
Titum, P., Berg, E., Rudner, M. S., Refael, G. & Lindner, N. H. Anomalous Floquet–Anderson
insulator as a nonadiabatic quantized charge pump. Phys. Rev. X 6, 021013 (2016).
Khemani, V., Lazarides, A., Moessner, R. & Sondhi, S. Phase structure of driven quantum
systems. Phys. Rev. Lett. 116, 250401 (2016).
Po, H. C., Fidkowski, L., Morimoto, T., Potter, A. C. & Vishwanath, A. Chiral Floquet phases
of many-body localized bosons. Phys. Rev. X 6, 041070 (2016).
Else, D. V., Bauer, B. & Nayak, C. Floquet time crystals. Phys. Rev. Lett. 117, 090402 (2016).
von Keyserlingk, C. W., Khemani, V. & Sondhi, S. L. Absolute stability and spatiotemporal
long-range order in Floquet systems. Phys. Rev. B 94, 085112 (2016).
Sacha, K. & Zakrzewski, J. Time crystals: a review. Rep. Prog. Phys. 81, 016401 (2017).
Khemani, V., Moessner, R. & Sondhi, S. A brief history of time crystals. Preprint at
https://arxiv.org/abs/1910.10745 (2019).
Wilczek, F. Quantum time crystals. Phys. Rev. Lett. 109, 160401 (2012).
Bruno, P. Impossibility of spontaneously rotating time crystals: a no-go theorem.
Phys. Rev. Lett. 111, 070402 (2013).
Watanabe, H. & Oshikawa, M. Absence of quantum time crystals. Phys. Rev. Lett. 114,
251603 (2015).
Huse, D. A., Nandkishore, R., Oganesyan, V., Pal, A. & Sondhi, S. L. Localization-protected
quantum order. Phys. Rev. B 88, 014206 (2013).
Pekker, D., Refael, G., Altman, E., Demler, E. & Oganesyan, V. Hilbert-glass transition: new
universality of temperature-tuned many-body dynamical quantum criticality. Phys. Rev. X
4, 011052 (2014).
Basko, D., Aleiner, I. & Altshuler, B. Metal-insulator transition in a weakly interacting manyelectron system with localized single-particle states. Ann. Phys. 321, 1126–1205 (2006).
Nandkishore, R. & Huse, D. A. Many-body localization and thermalization in quantum
statistical mechanics. Annu. Rev. Condens. Matter Phys. 6, 15–38 (2015).
Abanin, D. A., Altman, E., Bloch, I. & Serbyn, M. Colloquium: Many-body localization,
thermalization, and entanglement. Rev. Mod. Phys. 91, 021001 (2019).
Ponte, P., Papić, Z., Huveneers, F. M. C. & Abanin, D. A. Many-body localization in
periodically driven systems. Phys. Rev. Lett. 114, 140401 (2015).
Lazarides, A., Das, A. & Moessner, R. Fate of many-body localization under periodic
driving. Phys. Rev. Lett. 115, 030402 (2015).
Bordia, P., Luschen, H., Schneider, U., Knap, M. & Bloch, I. Periodically driving a
many-body localized quantum system. Nat. Phys. 13, 460–464 (2017).
Faraday, M. On a peculiar class of acoustical figures; and on certain forms assumed by
groups of particles upon vibrating elastic surfaces. Phil. Trans. R. Soc. 121, 299–340 (1831).
Zhang, J. et al. Observation of a discrete time crystal. Nature 543, 217–220 (2017).
Choi, S. et al. Observation of discrete time-crystalline order in a disordered dipolar
many-body system. Nature 543, 221–225 (2017).
Rovny, J., Blum, R. L. & Barrett, S. E. Observation of discrete-time-crystal signatures in an
ordered dipolar many-body system. Phys. Rev. Lett. 120, 180603 (2018).
Pal, S., Nishad, N., Mahesh, T. S. & Sreejith, G. J. Temporal order in periodically driven
spins in star-shaped clusters. Phys. Rev. Lett. 120, 180602 (2018).
Ippoliti, M., Kechedzhi, K., Moessner, R., Sondhi, S. & Khemani, V. Many-body physics in the
NISQ era: quantum programming a discrete time crystal. PRX Quantum 2, 030346 (2021).
Ho, W. W., Choi, S., Lukin, M. D. & Abanin, D. A. Critical time crystals in dipolar systems.
Phys. Rev. Lett. 119, 010602 (2017).
Else, D., Bauer, B. & Nayak, C. Prethermal phases of matter protected by time-translation
symmetry. Phys. Rev. X 7, 011026 (2017).
Luitz, D. J., Moessner, R., Sondhi, S. L. & Khemani, V. Prethermalization without
temperature. Phys. Rev. X 10, 021046 (2020).
Randall, J. et al. Many-body-localized discrete time crystal with a programmable
spin-based quantum simulator. Science 374, 1474–1478 (2021).
Mi, X. et al. Information scrambling in quantum circuits. Science 374, 1479–1483 (2021).
Abanin, D. A., De Roeck, W., Ho, W. W. & Huveneers, F. Effective Hamiltonians,
prethermalization, and slow energy absorption in periodically driven many-body
systems. Phys. Rev. B 95, 014112 (2017).
Mori, T., Ikeda, T. N., Kaminishi, E. & Ueda, M. Thermalization and prethermalization in
isolated quantum systems: a theoretical overview. J. Phys. B 51, 112001 (2018).
Popescu, S., Short, A. J. & Winter, A. Entanglement and the foundations of statistical
mechanics. Nat. Phys. 2, 754–758 (2006).

Nature | Vol 601 | 27 January 2022 | 535

## PDF page 6

Article
38. Goldstein, S., Lebowitz, J. L., Tumulka, R. & Zanghì, N. Canonical typicality. Phys. Rev. Lett.
96, 050403 (2006).
39. Richter, J. & Pal, A. Simulating hydrodynamics on noisy intermediate-scale quantum
devices with random circuits. Phys. Rev. Lett. 126, 230501 (2021).
40. Arute, F. et al. Quantum supremacy using a programmable superconducting processor.
Nature 574, 505–510 (2019).
41. Edwards, S. F. & Anderson, P. W. Theory of spin glasses. J. Phys. F 5, 965–974 (1975).
42. Kjäll, J. A., Bardarson, J. H. & Pollmann, F. Many-body localization in a disordered quantum
Ising chain. Phys. Rev. Lett. 113, 107204 (2014).
43. Pal, A. & Huse, D. A. Many-body localization phase transition. Phys. Rev. B 82, 174411 (2010).
44. Abanin, D. et al. Distinguishing localization from chaos: challenges in finite-size systems.
Ann. Phys. 427, 168415 (2021).
Publisher’s note Springer Nature remains neutral with regard to jurisdictional claims in
published maps and institutional affiliations.
Open Access This article is licensed under a Creative Commons Attribution
4.0 International License, which permits use, sharing, adaptation, distribution
and reproduction in any medium or format, as long as you give appropriate
credit to the original author(s) and the source, provide a link to the Creative Commons license,
and indicate if changes were made. The images or other third party material in this article are

536 | Nature | Vol 601 | 27 January 2022

included in the article’s Creative Commons license, unless indicated otherwise in a credit line
to the material. If material is not included in the article’s Creative Commons license and your
intended use is not permitted by statutory regulation or exceeds the permitted use, you will
need to obtain permission directly from the copyright holder. To view a copy of this license,
visit http://creativecommons.org/licenses/by/4.0/.
© The Author(s) 2021

Google Research, Mountain View, CA, USA. 2Department of Physics, Stanford University,
Stanford, CA, USA. 3Department of Electrical and Computer Engineering, University of
Massachusetts, Amherst, MA, USA. 4Pritzker School of Molecular Engineering, University of
Chicago, Chicago, IL, USA. 5Department of Electrical and Computer Engineering, University
of California, Riverside, CA, USA. 6Department of Chemistry, Columbia University, New York,
NY, USA. 7Department of Physics, University of California, Santa Barbara, CA, USA.
8
Department of Physics, Princeton University, Princeton, NJ, USA. 9Rudolf Peierls Centre for
Theoretical Physics, University of Oxford, Oxford, UK. 10Max-Planck-Institut für Physik
komplexer Systeme, Dresden, Germany. 11These authors contributed equally: Xiao Mi, Matteo
Ippoliti. ✉e-mail: vkhemani@stanford.edu; pedramr@google.com
1

## PDF page 7

Methods
Edge qubits
In computing various site-averaged quantities such as [A ] or χ SG, we
have excluded contributions from the edge qubits Q1 and Q20. This is
because they may be affected by the presence of edge modes independent of the bulk DTC response45.
Estimating distribution of autocorrelation functions
The measurements in Fig. 3a, b are conducted without error mitigation
(that is, normalization via the echo circuits ÛECHO). This is primarily
due to the already high number of experimental circuits that need to
be measured given the large collection of initial states and disorder
instances. Adding echo circuits to each of these instances would make
the data acquisition time unfeasibly long. We note that the experimental conclusions for Fig. 3a, b are in agreement with noiseless simulation
of the same circuit instances, which reveals the same features as experimental data. See Supplementary Fig. 9 for details.
‘Prethermalization’ in Û F′ model
We refer to the circuit Û F′ (with uniform angles ϕi = −0.4) used in Fig. 3
as prethermal. The choice of value for ϕi is such that the dynamics is
governed by an effective Hamiltonian Ĥeff for long times (see Supplementary Information for a derivation). Strictly speaking, a prethermal DTC requires Ĥeff to have a symmetry-breaking phase transition
at a finite temperature Tc—in that case, ordered initial states at temperatures T < Tc show long-lived oscillations (with an amplitude that
depends on the equilibrium value of the symmetry-breaking order
parameter at temperature T (ref. 31)). While short-ranged models in
one dimension (such as the one under consideration) cannot have
order at any finite temperature, thermal correlation lengths at low
temperatures may still exceed the system size. This allows
low-temperature states to show long-lived oscillations with a finite
amplitude, even if the equilibrium order parameter is asymptotically
zero for such states.
Measurement of the spin-glass order parameter
In Fig. 5, every data point is averaged over 40 disorder instances and
10 cycles (t = 51to t = 60). To construct χ SG, we sample 40,000 bit strings
t
at the output of Û F for each cycle and disorder instance. To address the
inhomogeneity of qubit coherence, smaller qubit chains are also averaged over different possible combinations of qubits. For example,
L = 12 is averaged over 12-qubit chains made from Q1 to Q12, Q3 to Q15 and
so on. The|0⟩⊗Lstate is used as the initial state for all disorder instances.
Error bars are estimated by resampling data from the 40 disorder
instances via the jackknife method.
Comparison between many-body echo and single-qubit errors
†
t
The many-body echo circuits UˆECHO = (UˆF)t UˆF are chosen for characterizing decoherence effects since they capture the complex interplay
between Floquet dynamics and single-qubit errors. More specifically,
the decay of a particular observable (for example, Zˆ(t) ) depends not
only on single-qubit error rates, but also on how much the quantum
operator Ẑ is ‘spread’ to different qubits over time. This effect is visible
in the different decay rates for the echo data with g = 0.60 and g = 0.97
in Fig. 2. Nevertheless, for values of g close to 1, the decay rate of local
observables A0 should be close to single-qubit error rates29 and at least
some basic comparison may be made.
A description of gate errors, characterized through cross-entropy
benchmarking40, can be found in Supplementary Fig. 1. The single-qubit
errors are also characterized through standard metrics of T1, T ⁎2 and
. We find T1 = 16.1 (5.3) µs across the 20-qubit chain, where the
T CPMG
2
value in parenthesis represents the standard deviation. T ⁎2, which is
characterized through Ramsey measurements, is found to be

, characterized through CPMG measurements,
T ⁎2 = 5.8 (2.8) µs. T CPMG
2
is found to be T CPMG
= 16.6 (3.7) µs.
2
These values may be compared to the characteristic decay rates of
the echo experiment (that is, A0 in Fig. 2c) at g = 0.97, which are found
to be 6.4 (1.1) µs across the qubit chain. Here the quantum system is
strongly localized, and the decay of the echo experiment is dominated
by single-qubit decoherence29. Given that this decay rate is closest to
the value of T ⁎2, the extrinsic decoherence in our experiments is probably limited by low-frequency noise (the main contributor to T ⁎2) and,
to some extent, energy relaxation and high-frequency noise as well.
A more detailed characterization of decoherence mechanisms is left
as the subject of future research.

Classical computational complexity of DTC circuits
The computational complexity of DTC circuits in the thermal and critical regimes asymptotically scales as an exponent of depth and number
of qubits. Even though our 20-qubit experiment can be simulated on
classical computers, it demonstrates a scalable protocol that could
be applied to larger systems with higher connectivity geometries
beyond the capacity of classical algorithms. We expect the circuit- and
geometry-dependent scaling exponent to be smaller than that for the
two-dimensional random circuits implemented in refs. 40,34. Therefore,
to challenge classical supercomputers, we would need DTC circuits
larger than those in refs. 40,34. Calculation of this threshold is beyond
the scope of this paper.

Data availability
The experimental data contained in the main text and Supplementary
Information are available for download at https://doi.org/10.5281/
zenodo.5570676.

Code availability
The Python simulation code used in theoretical analysis is available for
download at https://doi.org/10.5281/zenodo.5570676.
45. Yates, D. J., Abanov, A. G. & Mitra, A. Long-lived π edge modes of interacting and
disorder-free Floquet spin chains. Preprint at https://arxiv.org/abs/2105.13766 (2021).
Acknowledgements This work was supported in part by the Defense Advanced Research
Projects Agency via the DRINQS programme (M.I., V.K., R.M. and S.L.S.), by a Google Research
Award: Quantum Hardware For Scientific Research In Physics (V.K. and M.I.), and by the Sloan
Foundation through a Sloan Research Fellowship (V.K.) The views, opinions and/or findings
expressed are those of the authors and should not be interpreted as representing the official
views or policies of the Department of Defense or the US Government. M.I. was funded in part
by the Gordon and Betty Moore Foundation’s EPiQS Initiative through grant GBMF8686. This
work was partly supported by the Deutsche Forschungsgemeinschaft under grant SFB 1143
(project-id 247310070), the cluster of excellence ct.qmat (EXC 2147, project-id 390858490)
and a Leverhulme International Professorship (S.L.S.).
Author contributions M.I., K.K., V.K., R.M. and S.L.S. conceived the project. X.M., C.Q. and P.R.
executed the experiment. All the aforementioned discussed the project in progress and
interpreted the results. M.I., K.K., V.K. and X.M. designed measurement protocols. Z.C., A.G.,
J.G. and X.M. implemented and calibrated the CPHASE gates. M.I. and V.K. performed
theoretical and numerical analyses. M.I., K.K., V.K., R.M., X.M. and P.R. wrote the manuscript.
M.I. and X.M. wrote the Supplementary Information. Y.C., K.K., V.K., H.N., P.R. and
V. Smelyanskiy led and coordinated the project. Infrastructure support was provided by
Google Quantum AI. All authors contributed to revising the manuscript and the
Supplementary Information.
Competing interests The authors declare no competing interests.
Additional information
Supplementary information The online version contains supplementary material available at
https://doi.org/10.1038/s41586-021-04257-w.
Correspondence and requests for materials should be addressed to Vedika Khemani or
Pedram Roushan.
Peer review information Nature thanks Mohammad Hafezi and the other, anonymous,
reviewer(s) for their contribution to the peer review of this work.
Reprints and permissions information is available at http://www.nature.com/reprints.
