Source: see manifest row of the PDF
PDF sha256: 8a4be0f80216a44dc536d9bf9b97c942344c5967eb014abbd008eef4da4f0310
License: CC-BY-4.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of xiang_2024_long_lived_topological_time_crystalline_order_quantum_processor.pdf

Transcription of `xiang_2024_long_lived_topological_time_crystalline_order_quantum_processor.pdf` in this directory, 9 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-9 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Article

https://doi.org/10.1038/s41467-024-53077-9

Long-lived topological time-crystalline order
on a quantum processor
Received: 7 February 2024
Accepted: 27 September 2024

1234567890():,;

1234567890():,;

Check for updates

Liang Xiang 1,13, Wenjie Jiang 2,13, Zehang Bao 1,13, Zixuan Song 1,
Shibo Xu 1, Ke Wang 1, Jiachen Chen 1, Feitong Jin 1, Xuhao Zhu 1,
Zitian Zhu 1, Fanhao Shen 1, Ning Wang 1, Chuanyu Zhang 1, Yaozu Wu 1,
Yiren Zou 1, Jiarun Zhong 1, Zhengyi Cui1, Aosai Zhang 1, Ziqi Tan 1,
Tingting Li 1, Yu Gao 1, Jinfeng Deng 1, Xu Zhang 1, Hang Dong 1,
Pengfei Zhang 1, Si Jiang 2, Weikang Li 2, Zhide Lu 2, Zheng-Zhi Sun 2,
Hekang Li 1, Zhen Wang 1,3, Chao Song 1, Qiujiang Guo 1,3 ,
Fangli Liu 4,5, Zhe-Xuan Gong6,7, Alexey V. Gorshkov 4, Norman Y. Yao 8,
Thomas Iadecola 9,10, Francisco Machado 8,11, H. Wang 1,3 &
Dong-Ling Deng 2,3,12

Topologically ordered phases of matter elude Landau’s symmetry-breaking
theory, featuring a variety of intriguing properties such as long-range entanglement and intrinsic robustness against local perturbations. Their extension
to periodically driven systems gives rise to exotic new phenomena that are
forbidden in thermal equilibrium. Here, we report the observation of signatures of such a phenomenon—a prethermal topologically ordered time
crystal—with programmable superconducting qubits arranged on a square
lattice. By periodically driving the superconducting qubits with a surface code
Hamiltonian, we observe discrete time-translation symmetry breaking
dynamics that is only manifested in the subharmonic temporal response of
nonlocal logical operators. We further connect the observed dynamics to the
underlying topological order by measuring a nonzero topological entanglement entropy and studying its subsequent dynamics. Our results demonstrate
the potential to explore exotic topologically ordered nonequilibrium phases
of matter with noisy intermediate-scale quantum processors.

Phases of matter are often classiﬁed by broken symmetries and local
order parameters1. However, the discovery of topological order has
transformed this simple paradigm2,3. Two topologically ordered phases
with the same symmetries can showcase topologically distinct features,

such as different patterns of long-range entanglement and the emergence of quasiparticles with different anyonic braiding statistics4–6.
These features are intrinsically nonlocal in that they cannot be distinguished by any local order parameter7,8 and also distinguish

1

School of Physics, ZJU-Hangzhou Global Scientiﬁc and Technological Innovation Center, and Zhejiang Key Laboratory of Micro-nano Quantum Chips and
Quantum Control, Hangzhou, China. 2Center for Quantum Information, IIIS, Tsinghua University, Beijing 100084, China. 3Hefei National Laboratory, Hefei
230088, China. 4Joint Quantum Institute and Joint Center for Quantum Information and Computer Science, NIST and University of Maryland, College Park,
MD, USA. 5QuEra Computing Inc., Boston, MA, USA. 6Department of Physics, Colorado School of Mines, Golden, CO, USA. 7National Institute of standards and
Technology, Boulder, CO, USA. 8Department of Physics, Harvard University, Cambridge 02138 MA, USA. 9Department of Physics and Astronomy, Iowa State
University, Ames, IA 50011, USA. 10Ames National Laboratory, Ames, IA 50011, USA. 11ITAMP, Harvard-Smithsonian Center for Astrophysics, Cambridge
Massachusetts 02138, USA. 12Shanghai Qi Zhi Institute, Shanghai 200232, China. 13These authors contributed equally: Liang Xiang, Wenjie Jiang, Zehang Bao.
e-mail: qguo@zju.edu.cn; hhwang@zju.edu.cn; dldeng@tsinghua.edu.cn

Nature Communications | (2024)15:8963

1

## PDF page 2

Article

https://doi.org/10.1038/s41467-024-53077-9

topologically ordered phases from symmetry protected topological
phases9. Unfortunately, topological order is usually restricted to the
ground state; mobile thermal excitations can hybridize nominally
degenerate ground states by traversing the system along nontrivial
closed loops. By introducing disorder, the motion of these excitations
can be arrested and the hybridization process suppressed. In the limit
where excitations are fully localized, the topological phase becomes
stable across the entire energy spectrum of the system10–18.
Time-periodic driving of a quantum many-body system enables
novel phases of matter that cannot exist in thermal equilibrium. A
prominent example is that of time crystals19–26, where discrete time
translation symmetry is spontaneously broken. Strikingly, the concept
of a time crystal can be extended to include topological order,
resulting in a new dynamical phase dubbed a topologically ordered
time crystal27. Unlike conventional time crystals, where the breaking of
time translation symmetry manifests in the dynamics of local observables, topologically ordered time crystals show such symmetry
breaking only for nonlocal logical operators. Whether or not this phase
has a truly inﬁnite lifetime depends on the late-time stability of manybody localization28–30; nevertheless, the dynamical features of the
system can still exhibit very long-lived signatures of localization persisting beyond current experimental timescales. While signatures of
conventional time crystals without topological order have been
observed in a number of distinct systems, including trapped ions31,32,
spins in nitrogen-vacancy centers33,34, ultracold atoms35,36, solid-state
spin ensembles37–39, and superconducting qubits23,40,41, the observation
of a topologically ordered time crystal remains an open challenge.
Here, we report the observation of a long-lived prethermal
topologically ordered discrete time crystal, with eighteen programmable superconducting transmon qubits arranged on a twodimensional square lattice. By optimizing the device fabrication and
control process, we push the median lifetime of these qubits to
T1 ≈ 163μs and the median simultaneous single- and two-qubit gate
ﬁdelities above 99.9% and 99.4%, respectively. Together with a neuroevolution algorithm42 that outputs near-optimal quantum circuits
for digitally simulating four-body interactions, this enables us to successfully implement Floquet surface code dynamics with an optimized
quantum circuit of depth exceeding 700, consisting of more than
2300 single- and 1400 two-qubit gates. We measure the dynamics of
nonlocal logical operators and local spin magnetizations and ﬁnd that
the former show a robust subharmonic response, whereas the latter
decay quickly to zero and do not show period-doubled oscillations.
This differs drastically from symmetry breaking and symmetryprotected topological discrete time crystals, where local, rather than
nonlocal, observables exhibit subharmonic response. We further
reveal the long-range quantum entangled nature of topological order
by preparing a many-body eigenstate of the Floquet unitary and
measuring its topological entanglement entropy with different subsystem sizes and geometries43,44. We obtain near-expected values for
the measured topological entanglement entropy, which deviates signiﬁcantly from the trivial-state value of zero and provides strong evidence for the presence of topological order.

Results
Theoretical model and experimental setup
We consider the periodically driven rotated surface code model on a
2D lattice with open boundary conditions27,45 (see Methods):

HðtÞ =
H1 

H1,
H2,
πX
2

H2  

k
X

0 ≤ t < T 0,
T 0 ≤ t < T,
X
σ xk +
Bk  σ k ,
k

α p Ap 

p

Nature Communications | (2024)15:8963

X
q

β q Bq ,

where σ k = ðσ xk ,σ yk ,σ zk Þ is a vector of Pauli matrices acting on the k-th
qubit; Bk denotes an on-site ﬁeld drawn randomly and independently
Q
from a ball with radius B; the plaquette operators Ap = m2p σ zm and
Q
Bq = n2q σ xn are products of Pauli operators on the corresponding
plaquettes (Fig. 1a); αp and βq are coefﬁcients uniformly chosen from
[0, 2π); the drive period is ﬁxed as T = 2T 0 = 2, which roughly
corresponds to a 1.4-μs runtime for the corresponding quantum
circuit in our experiment.
We note that, other than the discrete time-translation symmetry,
H(t) breaks all microscopic symmetries due to the presence of the
random on-site ﬁelds Bk in H1. The Floquet unitary that fully characterizes the dynamics of the system reads UF = U2U1, with U 1 = eiH 1
and U 2 = eiH 2 being the unitary operators generated by the Hamiltonians H1 and H2, respectively. H2 represents the Hamiltonian of the
rotated surface code model, whose energy spectrum is two-fold
degenerate and whose eigenstates show topological order7,46. Owing
to their topological nature, the degenerate eigenstates can only be
Q
distinguished by nonlocal string operators such as Z L = k2P z σ zk or
Q
X L = k2P x σ xk , which traverse the lattice through the path Pz or Px (see
Fig. 1a). We label each eigenstate pair by ∣Z ðlÞ
L = ± 1i for each eigenstate
with quasi-energy ϵl (see Supplementary Note 1.A). In the limit B → 0, U1
represents a perfect ﬂip of all spins. As a result, the drive H1 reorganizes
the topologically ordered eigenstate pairs of H2 into Floquet eigenðlÞ
ðlÞ
ðlÞ
states ∣E ðlÞ
± i of the form ∣E ± i / ∣Z L = 1i ± ∣Z L =  1i. The quasi-energies
of the corresponding cat-like eigenstates are split by quasi-energy π
(Fig. 1b). As a result, the stroboscopic dynamics of the nonlocal
operator ZL exhibits a stable subharmonic oscillation with 2T periodicity as illustrated in Fig. 1c, which breaks the discrete time-translation
symmetry by the drive period T (see Supplementary Note 1.C). These
Floquet eigenstates also exhibit topological order, which is essential
for the robustness of the subharmonic response of the nonlocal string
operators ZL.
For small but ﬁnite B, the system’s integrability is broken and the
eigenstate pairs are no longer exactly split by π. However, this deviation arises from the motion of excitations across the system which
mixes the different topological sectors, which is strongly suppressed
by the disorder in αp and βp. Until this thermalization occurs, t ≲ tth, the
system’s dynamics will exhibit robust period doubling dynamics, much
like in the B = 0 case. All our experimental and theoretical observations
of period doubling behavior pertain to this “prethermal” regime which,
in the small-B regime, is much larger than the experimentally accessible timescales.
Our experiments are carried out on a programmable ﬂip-chip
superconducting processor with 18 transmon qubits arranged on a 2D
square lattice (see Supplementary Note 2.A for detailed information
about the device). To implement H(t), the four-body terms with random strengths in H2, which are vital for the eigenstate topological
order at high energy, pose an apparent challenge since four-body
interactions do not naturally appear in the superconducting system.
We therefore exploit the idea of digital quantum simulation to
implement H(t) with quantum circuits (Fig. 1d), which are obtained via
a neuroevolution algorithm42 (see Methods and Supplementary
Note 1.G). We mention that these quantum circuits are near-optimal
and can implement H(t) in an analytical fashion without any Trotter
error, independent of αp, βp, and Bk. With these efﬁcient quantum
circuits, improved gate ﬁdelities, and coherence times, we are able to
implement and probe the unconventional dynamics of the system up
to 20 driving periods.

Subharmonic response for nonlocal observables
ð1Þ

The characteristic signature of topological time-crystalline eigenstate
order is the breaking of the discrete time-translation symmetry for
nonlocal logical operators, manifested by persistent oscillations with
period 2T. To this end, we deﬁne the normalized auto-correlation
1=d
function AL ðtÞ = sign½hZ L ð0ÞZ L ðtÞijhZ L ðtÞij1=d for the d-body string
2

## PDF page 3

Article

https://doi.org/10.1038/s41467-024-53077-9

b

1

2

3

4

5

6

X L 12

11

10

9

8

7

13

14

15

16

17

18

ZL

c
|E(l)²= |ZL(l)=1² + |ZL(l)=-1²

...

ZL

Quasi-energies
εl
εl S

a

|E(l)²= |ZL(l)=1² − |ZL(l)=-1²

XL

-1

0

1

t

d
U1

U2

X( )

U(ZZ)

U(XX)

U(ZZZZ)

U(XXXX)

=

X( )

Y( )

Z( )

CZ

=

Fig. 1 | Periodically driven surface code model. a Rotated surface code model on a
three-by-six square lattice. The circled numbers label the qubits. The dark and light
gray regions represent plaquette operators Ap and Bq, respectively. The thick black
(red) line represents the nonlocal string operator ZL (XL). b Topologically ordered
Floquet eigenstates in the limit B → 0. The quasi-energies of each pair of eigenstates
∣E ðlÞ
± i are split by π. c Schematic of the stroboscopic dynamics of the string operators ZL and XL. Under periodic driving, the expectation value of ZL exhibits a persistent subharmonic oscillation with a period of 2T, while XL preserves a constant
value of zero. d Decomposition of the Floquet unitary UF (B = 0) into elementary

quantum gates. U1 is realized by applying π pulses to all the qubits. Since all the
plaquette operators commute with each other, U2 is constructed by sequentially
applying four groups of them. Plaquette unitaries eiAp T=2 , labeled by U(ZZZZ) and
U(ZZ), and eiBq T=2 , labeled by U(XXXX) and U(XX), are further decomposed into
sequences of single-qubit rotations and two-qubit controlled-Z gates. X(θ), Y(θ),
and Z(θ) denote single-qubit rotations by an angle θ around the x-, y-, and z-axis,
respectively. eiBq T=2 can be implemented by sandwiching eiAq T=2 with Hadamard
gates. In the experiment, the whole circuit is further compiled to reduce the depth
and suppress hardware noise (Supplementary Note 2.E).

operator ZL, where 〈 ⋯ 〉 represents the expectation value and the
d-th root is used to indicate the geometric mean value. When d = 1, this
generalization reduces to the standard auto-correlation function for
single-qubit operators23,40, while allowing for a direct comparison
across different lengths of string operators (see Supplementary
Note 2.F for more details). We begin by studying the evolution of the

previous works23,31–33,40, where only local observables break timetranslation symmetry, we further demonstrate that the observed Floquet topological order is a nonlocal effect by contrasting with the
dynamical behavior of local operators fσ zk g. The auto-correlation

1=d

disorder-averaged auto-correlator ALi ðtÞ for operators fZ Li g (d = 3) at
the solvable limit B = 0, which are averaged over 24 random realizations by sampling Hamiltonian parameters αp, βq and random z-basis
initial states. From Fig. 2a, it is evident that, in the topologically

function hsign½σ zk ð0Þσ zk ðtÞi decays to zero quickly without evident
oscillations (Fig. 2c), even though the periodic drive is locally applied
to each qubit. The striking contrast between nonlocal operators fZ Li g
and local operators fσ zk g exposes the locally indistinguishable nature of
the Floquet topological order and rules out the possibility of trivial
oscillations arising from driving a noninteracting system.

1=d

ordered regime, ALi ðtÞ oscillates with a 2T periodicity for up to 20
1=d

driving cycles. We mention that ALi ðtÞ exhibits a gradually decaying
envelope due to extrinsic experimental imperfections, rather than
internal thermalization, which is conﬁrmed by numerical simulations
(lines in Fig. 2a) incorporating experimentally measured gate errors
and decoherence times. Indeed, the ideal numerical simulations show
that the internal thermalization time of the system without experimental noise is far longer than 20 driving cycles (Supplementary
1=d

Note 1.D). In the frequency domain, ALi

shows a peak at the sub-

harmonic frequency of the drive period ω/ω0 = 0.5, as shown in Fig. 2b.
We also note that the string operator XL does not show period-doubled
oscillations, and no subharmonic peak is observed in the frequency
domain.
Although the 2T-period subharmonic oscillations of nonlocal
observables fZ Li g already sharply distinguish our experiment from
Nature Communications | (2024)15:8963

Topologically ordered Floquet eigenstates
The Floquet eigenstates bear intrinsic topological order and exhibit
long-range quantum entanglement characterized by the topological
entanglement entropy Stopo43,44 (see Supplementary Note 1.B). To
reveal the underlying global entanglement, we prepare an eigenstate
of UF and measure its Stopo for different system sizes. In the B → 0 limit,
eigenstates of UF correspond to superpositions of degenerate eigenstates of H2 (see Fig. 1b). The eigenstate we prepare is the symmetric superposition of ground states of H2, given by
ð0Þ
ð0Þ
p1ﬃﬃ
∣E ð0Þ
+ i = 2 ð∣Z L = 1i + ∣Z L =  1iÞ. We prepare it from a simple initial
product state using a quantum circuit whose depth grows linearly with
the system size (see Supplementary Note 1.H)47:

∣E ð0Þ
+ i=

1
2

4

ð1 + X L Þ

Y

ð1 + Bq Þ∣0i18 :

ð2Þ

q

3

## PDF page 4

Article

https://doi.org/10.1038/s41467-024-53077-9

ZL

-1
1

ZL

-1
1

ZL

-1
1

ZL

-1
1

ZL

-1

1

2

3

0

5

c

6

1
1
1
-1
0

2

4

6

8

10

12

14

16

18

-1
XL

-1
XL

ZL

1

2

XL

i

0.5
/ 0

4

t
XL

0.5
0.4
0.3
0.2
0.1
0

1 0

i

0.5
/ 0

1

17
1

13
9

0

5

-1

sign[ z(0)] z(t)

ZL

-1
1

FFT amplitude

b

1

Qubit index

a

1
0

3

4

8

12

16

20

t/T

20

t/T
Fig. 2 | Time-translation symmetry breaking for nonlocal observables with
B = 0. a Dynamics of nonlocal observables. Auto-correlation function for the threebody string operators fZ Li g (thick black lines) and instantaneous expectation values
for the six-body string operators fX Li g (thick red lines) are shown in the upper six
and lower three panels, respectively. Experimental data points (dots) are obtained
from averaging over 24 random realizations, with error bars representing the
standard error of the statistical mean. The numerical results (lines) are computed
by taking into account qubit decoherence and gate errors (Supplementary Note 3).

Whereas the instantaneous expectation values for fX Li g remain zero, the autocorrelators for fZ Li g exhibit stable subharmonic oscillations for up to 20 cycles (see
Supplementary Note 2.F for measurement details). b Fourier spectra of timedomain signals observed in a, where a stable subharmonic frequency peak appears
for fZ Li g but not fX Li g. c Dynamics of the auto-correlation function for local
observables fσ zk g. Such auto-correlations decay quickly to zero, in sharp contrast to
those of the string operators fZ Li g.

We then measure the plaquette operators {Ap} and {Bq} (left panel of
Fig. 3a), and an average value of ~ 0.95 is observed, which is noteworthy given that these operators encode four-body correlations. The
high-ﬁdelity gates and long coherence times achieved in our
experiment are of crucial importance to obtain such a high average
value of the measured stabilizers (see Supplementary Note 2.B). We
also measure the expectation values of string operators fX Li ,Z Li g and
ð0Þ
ð0Þ
ð0Þ
ﬁnd that hE ð0Þ
+ ∣Z Li ∣E + i  0 and hE + ∣X Li ∣E + i  1 (right panel of Fig. 3a).
These experimental results are in good agreement with theoretical
predictions, providing strong evidence that the prepared state is
indeed a Floquet eigenstate as desired.
Having prepared the Floquet eigenstate, we further measure its
topological entanglement entropy for two different subsystem sizes:
four qubits and six qubits. We follow a protocol developed in ref. 47
and divide the subsystem into three parts: A, B, and C (upper panels of
Fig. 3b). Stopo can be extracted from the following combination of von
Neumann entanglement entropies43,44:

the prepared Floquet eigenstate. The deviation between the
measured Stopo and its corresponding ideal value is due to limited
coherence times and gate errors, which is conﬁrmed by numerical
results using a noise model estimated via independent measurements (our numerical simulations show that Stopo = ln 2 is 0.85 and
0.82 for the four-qubit and six-qubit subsystems, respectively; see
Methods and Supplementary Note 3).

Robustness against local perturbations
Topological order is expected to be robust against small local perturbations. In our experiment, we investigate the robustness of the
subharmonic response of nonlocal logical operators and of the
entanglement dynamics to local perturbations by turning on the random on-site ﬁelds in H1. We vary the perturbation strength B and
1=d
measure ALi ðtÞ and Stopo(t), with results plotted in Fig. 4.
Figure 4a shows the measured disorder-averaged auto-correlation
1=d

function ALi ðtÞ for fZ Li g under weak (B = 0.1) and strong (B = 3.0)

ð3Þ

perturbations, which are averaged over 24 realizations with randomly
drawn initial states, αp, βq, and Bk. With a small perturbation (B = 0.1),

where SA is the von Neumann entropy for region A, while AB means
the union of regions A and B, and similarly for other terms. For the
eigenstates of UF, the theoretically predicted value of Stopo is  ln 243.
For each region i, we perform quantum state tomography on the
whole (four-qubit or six-qubit) subsystem and reconstruct ρi to calpﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ
pﬃﬃﬃ
ρi and von Neuculate the corresponding ﬁdelity Fðρi Þ = tr pρﬃﬃﬃi ρideal
i
mann entropy Si =  trðρi ln ρi Þ, where ρideal
is
the
reduced density
i
matrix of region i obtained by tracing out the complementary region
of the ideal Floquet eigenstate. The experimentally measured Stopo,
Si, and F(ρi) are shown in the lower panels of Fig. 3b. The measured
von Neumann entropy for each region agrees well with the corresponding ideal value. In addition, we observe that Stopo = ln 2 is
0.86 ± 0.02 for the four-qubit and 0.84 ± 0.08 for the six-qubit
subsystem, which is incompatible with the trivial-state value of zero
and provides strong evidence for the nontrivial topological nature of

ALi ðtÞ continues to exhibit persistent subharmonic response up to 20

Stopo = SA + SB + SC  SAB  SAC  SBC + SABC ,

Nature Communications | (2024)15:8963

1=d

driving periods (upper panel of Fig. 4a), which is a deﬁning feature of
the time-translation symmetry breaking for nonlocal operators and
shows the robustness of the observed prethermal topologically
ordered discrete time crystal. In contrast, with a strong perturbation
1=d

(B = 3.0), the measured ALi ðtÞ decays quickly to zero and shows no
subharmonic response (lower panel of Fig. 4a); at large B, the large
onsite ﬁeld rapidly destroys the topological order preventing any
robust period doubling dynamics. To explore the crossover from the
time-crystalline to trivial dynamics, we vary the perturbation strength
B and Fourier transform the measured time-domain signals. Fig. 4b
shows the Fourier amplitudes at ω/ω0 = 0.5 with B ranging from 0 to
3.0. We ﬁnd a small plateau at B ≲ 0.25, which further supports the
robustness of the topologically ordered time-crystalline dynamics

4

## PDF page 5

Article
a
1

https://doi.org/10.1038/s41467-024-53077-9

97

2

3

96
11

96
14

-100

90
10

91

13

97

0

4

5

98

91

99

1

1

i

18

i

0

ZL 1

1 2 3

i

0
123456

100

2

3

C

4

5

6

100
1

A

Ideal

2

3

4

5

6

Exp.

B

12

11

10

9

8

7

12

13

14

15

16

17

18

13

C

11

10

9

8

7

14

15

16

17

18

1.0

1
0
-1
-2
-3
-4

0.9

F( )

A
B
C
AB
BC
AC
ABC
TOPO

0.8
A
B
C
AB
BC
AC
ABC
TOPO

-S/ln2

B

A

7

91
17

stabilizer

b

XL

i

8

97
16

6

91

9

15

100

96

99

12

93

98

Fig. 3 | Measured stabilizer values and topological entanglement entropy for a
Floquet eigenstate. a Measured expectation values of plaquette operators {Ap} and
{Bq} for the Floquet eigenstate ∣E ð0Þ
+ i are shown in the left panel. Expectation values
of string operators fX Li ,Z Li g are plotted in the right panel with solid (hollow) bars
representing experimental (theoretical) results. b Measuring topological entanglement entropy (TOPO, Stopo) on four- and six-qubit subsystems. The division of
subsystems and corresponding experimental results are shown in the upper and
lower panels, respectively. Blue squares (red circles) represent entanglement
entropy (region ﬁdelities F(ρi)). The topological entanglement entropy is extracted
from the measured von Neumann entropy for the regions Si. The error bars,
obtained by repeated measurements, are very small and not shown here. The black
rhombus markers are theoretical predictions for Stopo and Si, which agree well with
the corresponding experimental results.

against weak perturbations. As B increases, the Fourier amplitude
decays monotonically and becomes almost ﬂat at B ≳ 2.5, where the
topological order is very quickly destroyed and no period doubling
dynamics survives. Sample-to-sample amplitude ﬂuctuations over 24
random realizations (inset of Fig. 4b) display a sharp increase at the
same value of B where the Fourier amplitude starts to decay, further
highlighting the location of the crossover between the prethermal
topological time-crystalline and the trivial dynamics.
We further study the dynamics of the topological entanglement
entropy under local perturbations. We ﬁrst prepare the system in the
B = 0 Floquet eigenstate ∣E ð0Þ
+ i and then let it evolve under H(t) with
varying B. In Fig. 4c, we plot the measured Stopo ðtÞ for B = 0.1 and
B = 3.0, respectively. From this ﬁgure, we see that Stopo ðtÞ drops more
quickly at strong perturbation B = 3.0 due to the breakdown of the
topological phase. We note that Stopo ðtÞ also has a slow decay even for
B = 0.1 due to the accumulated gate errors in the circuit, which is
conﬁrmed by the numerical simulations (the dashed lines in Fig. 4c)
(see Supplementary Note 3). In addition, we measure plaquette and
string operators after evolution under UF for a single time step (see
Fig. 4d). From this ﬁgure, it is clear that their values are largely preserved for B = 0.1, unlike the case of B = 3.0, where these values drop to
near zero. We further measure the disorder-averaged Stopo ðt = TÞ as a
function of B (Fig. 4e). Similar to the Fourier spectrum amplitudes in
Fig. 4b, Stopo ðt = TÞ also decays monotonically with increasing disorder
Nature Communications | (2024)15:8963

strength. Although, in general, the topological entanglement entropy
tends to be destroyed by quench dynamics48,49, the fact that it exhibits
a plateau in the weak disorder regime (B ≲ 0.25) implies a slow decay of
the topological time-crystalline order, offering a different characterization of the topological time crystalline behavior and further validating its robustness against perturbations. We emphasize that the
relationship between the observed nonzero topological entanglement
entropy and the topological order in a general quantum state and away
from equilibrium is complex. Here, we interpret the slow decay of Stopo
as an indicator of slow melting of the topological order. This is supported by theoretical arguments based on prethermalization and by
experimental measurements of the ﬁdelity between the topologically
ordered initial state and the state obtained by evolution over up to ﬁve
Floquet periods, which remains large provided B is sufﬁciently weak
(see Supplementary Note 1.D).
We note that, for the generic local perturbations considered in
our experiment, the overlap between a bare logical operator and its
corresponding dressed logical operator may vanish in the thermodynamic limit. This would render the observation of time-crystalline
behavior for the bare logical operator infeasible27. In addition, to
observe the time-crystalline behavior, it is also crucial that
Q
f σ xk ,Z L g = 0 is satisﬁed, which requires that the length of ZL be odd. A
possible way to maintain time-crystalline signatures in bare logical
operators in the thermodynamic limit and to remove the requirement
of odd length ZL is to consider a surface code with a hole, as discussed
in depth in ref. 27. In our experiment, we do not adopt such a layout
because measuring the corresponding nonlocal logical operator would
become very challenging with the current device.

Discussion
In summary, we have experimentally observed signatures of a
long-lived topologically ordered time crystal in the prethermal
regime with a programmable superconducting quantum processor. In contrast to previously reported conventional time
crystals, the topologically ordered time crystal studied here
builds upon a truly long-range entangled phase, such that discrete time-translation symmetry breaking only occurs for nonlocal logical operators. As a result, this experiment is more
challenging than our previous one on symmetry-protected topological (SPT) time crystals23, requiring 2D qubit connectivity,
deeper circuit depth, higher gate ﬁdelity, and longer coherence
time. With signiﬁcantly improved quantum computing hardware
(see Supplementary Table 2), we observed persistent subharmonic response for logical operators independent of the
initial state and demonstrated the robustness of this response to
generic perturbations without any microscopic symmetry. In
addition, we also prepared a topologically ordered Floquet
eigenstate and measured its topological entanglement entropy,
which agrees well with theoretical predictions and clearly shows
the intrinsic topological nature of the observed time crystal. Our
work shows that the topologically ordered time crystal differs
from previously studied time crystals23,31–33,40 in terms of measurability, stability, and entanglement structure.
The topologically ordered eigenstates of the Floquet unitary
are theoretically predicted to exhibit a perimeter law, where the
expectation value of a Wilson loop scales with the perimeter
rather than the area enclosed17,27. As a result, the late-time values
of the nonlocal logical operators under the Floquet drive also
exhibit a perimeter law, i.e., they will exponentially decay with
their length (see Supplementary Note 1.E). However, it is still
challenging to experimentally observe such long-time behaviors
in current NISQ50 devices, so we leave this for future experimental
investigations. The high controllability and programmability of
the superconducting processor demonstrated in our experiment
also paves the way to exploring a wide range of other exotic non5

## PDF page 6

Article

https://doi.org/10.1038/s41467-024-53077-9

ZL

ZL

1

2

ZL

ZL

3

ZL

4

6

1

B=0.1

FFT amplitude at 0/2

0
-1

A 1/d
(t)
L

1

B=3.0

0
-1

0.05

0.4

0
0

1.0

2.0

3.0

B

0.2
Sim.

Exp.

0.5

1.0

0
5

10
t/T

c

d
B=3.0

0.6

77

1

76
12

65

0
0

1

2

3

4

5

t/T

-22

2

4
12

72

15

-4

0

7

-100

0

4

73

17

5

-1

47

6
7

-3
17

18

123456
XL 1
i0
1
ZL
i0

100
Stabilizer

Fig. 4 | Robustness of the topological time-crystalline eigenstate order.
1=d

a Measured disorder-averaged auto-correlation function ALi ðtÞ for string operators

i

1 2 3

i0

18

8

-3

ZL

1

100

1.5
B

2.0

2.5

3.0

e

1

i0

-1

-4
16

XL

7

69

4

0

6

75

9

15

92

8

63

15

-6
14

70

16

10

13

5

9

56

3

11

4

53
10

67
14

18

0.2

58

72

0

59

B=3.0

1

3

11

13

0.4

2

20

83

B=0.1

B=0.1

0.8

15

82

0

-S topo/ln2

0.10

0.6

i

i

1 2 3
123456
Ideal

i

Exp.

Sim.

0.6
-S topo (t=T)/ln2

A 1/d
(t)
L

b

ZL

5

S.D.

a

Exp.

0.4
0.2
0
0

1.0

2.0

3.0

B

entanglement entropy Stopo from the initial state ∣E ð0Þ
+ i (which is a Floquet eigenstate
at B = 0) for different B. Here, Stopo ðt ≠ 0Þ is obtained by performing state tomography

fZ Li g with B = 0.1 (upper panel) and B = 3.0 (lower panel). Error bars denote the

on a four-qubit subsystem and the average is over 12 random realizations; Stopo ðt = 0Þ

standard error of the statistical mean over 24 random realizations. b Amplitudes of

is obtained via the same state tomography process and averaging over ﬁve repetitions
of eigenstate preparation. d Measured plaquette and string operators for the eigen-

1=d

Fourier spectra at ω/ω0 = 0.5 as a function of B. Fourier transform of AL ðtÞ is performed using averaged time-domain signals over fZ Li g for up to t = 6T. Each data point

state ∣E ð0Þ
+ i after single-step UF evolution at B = 0.1 and B = 3.0. e, Stopo ðt = TÞ as a

is averaged over 24 random realizations. Error bars are the standard deviation (S.D.)
for 24 disorder realizations. Insert: The S.D. of Fourier spectra amplitudes at ω/ω0 = 0.5
as a function of B. c Quench dynamics of the disorder-averaged topological

function of random ﬁeld strength B, which is averaged over 12 random realizations.
Numerical simulations (dashed lines) in b, c, and e are carried out with noisy quantum
gates (see Supplementary Note 3 for details).

equilibrium phases with intrinsic topological order that are not
accessible in natural materials. In particular, it would be interesting and important to realize various dynamically-enriched
topological orders51. Indeed, our experiment has demonstrated all
necessary building blocks for implementing the Floquet-enriched
topological order that hosts dynamical anyon permutation51 and
emergent non-Abelian anyons52,53. An observation of such an
unconventional phenomenon would also mark an important step
in deepening our understanding of exotic non-equilibrium
phases.

However, in current quantum devices, qubits are usually connected
with the nearest ones and periodic boundary condition is challenging
to accomplish. Instead, stabilizer codes deﬁned in open manifolds are
more likely to be realized. Therefore, we concern with a square lattice
with an open boundary condition.
To satisfy the requirements of a stabilizer code, the surface code
on an open manifold has two kinds of boundaries in alternating order:
the z-type boundary and the x-type boundary. At the z-type boundary,
one of the qubits associated with the plaquette operators is removed,
and at the x-type boundary, one of the qubits associated with the
vertex operators is removed. Thus, in the bulk, the stabilizer operators
are the same as those in the toric code. At the boundaries, the corresponding plaquette and vertex operators are only applied to the
reserved three qubits.
We note that, for each pair of operators, if they are both the
plaquette operators or vertex operators, they must commute with
each other. Besides, if they belong to different classes, they must share
an overlap with an even number
ofqubits (0 or 2). In addition with the

anti-commutative relation σ zk ,σ xk = 0, we conclude that any pair of
operators from different classes commute with each other. Without
modifying the topological properties, we can drop even more auxiliary
qubits and rotate the surface code to obtain the model we used in the
main text. For a m × n lattice, there are mn qubits, (m − 1)(n − 1) fourbody stabilizers, and m + n − 2 two-body stabilizers. Thus, such code
will encode a single qubit of quantum information (see Supplementary
Note 1.A for details).

Methods
Surface code model
Here, we provide a comprehensive introduction to the model, which
we use to realize the long-lived topological time-crystalline order.
Toric code is usually deﬁned on a square lattice with periodic
boundary condition. Thus, the deﬁning manifold is a torus. Consider a
L × L square lattice with periodic boundary condition. It contains L2
vertices, 2L2 edges, and L2 plaquettes. The qubit is put on each edge of
the lattice and two kinds of local operators can be deﬁned. For each
plaquette, we can deﬁne the product of the σ zk operators on each edge
surrounding the plaquette as the corresponding plaquette operator.
There are L2 plaquette operators. For each vertex, we deﬁne the product of the σ xk operators on each edge connecting with the vertex as
the corresponding vertex operator. There are L2 vertex operators. This
deﬁnition gives a stabilizer code that can store quantum information.

Nature Communications | (2024)15:8963

6

## PDF page 7

Article
Circuit
To implement the time evolution of surface code model, we decompose the evolution unitary into digital quantum circuits. It is straightforward to realize the Floquet drive U 1 ðtÞ = eitH 1 with tensor products
of single-qubit rotations, which can be represented with Euler angles.
However, the circuit construction of U 2 ðtÞ = eitH 2 is more challenging
due to the two-body and four-body operators.
The variational quantum circuit is a powerful tool for NISQ computation and quantum simulation and has been intensively studied in
recent years54,55. We adapt this method to construct the quantum circuit for the evolution. The circuit construction for the evolution
operator of H2 can be divided into two steps. First, we need to ﬁnd an
appropriate circuit ansatz with variational parameters. Second, we
optimize the variational parameters in this ansatz to minimize the
distance between the corresponding quantum circuit and the target
unitary. In our work, we use the neuroevolution method42 to ﬁnd a
suitable variational quantum circuit architecture. In short, we construct a directed graph where each node represents a block of quantum gates that can be implemented in parallel, and where the directed
edges denote allowed sequences of blocks. A quantum circuit can then
be represented as a directed path in this graph. We sample several
paths from this graph, and use the gradient descent method to optimize their parameters. Using such a method, we ﬁnd an experimentally
friendly ansatz analytically representing the target evolution unitary
(see Supplementary Note 1.G for details).

Numerical simulation of the noisy circuit
We employ the Monte Carlo wavefunction method56 to numerically simulate the noisy circuits. It requires fewer computational
resources than the master-equation approach because it evolves
the system state vector of size 2N during the calculation rather
than the density matrix of size 2N × 2N. In this context, we use the
state-vector simulator provided by Qiskit57 for the numerical
calculation of system dynamics.
To model realistic errors in experimental circuits, we use
quantum channels of energy relaxation, dephasing, and depolarizing. These channels are represented as probabilistic mixtures of
different operators. Parameters of each error channel are estimated from the experimental benchmarks of gate errors and
device performance (see Supplementary Note 3 for details). Error
operators are sampled according to the noise model and randomly inserted after each ideal gate. As a result, the state vectors
evolve along many quantum trajectories corresponding to many
noise realizations. Values of the desired observable are obtained
by averaging over an ensemble of such quantum trajectories,
which resembles repeated measurements for evaluating the
expectation value of an observable in experiments.

Data availability
The data generated in this study have been deposited in the Zenodo
database under accession code https://doi.org/10.5281/zenodo.
1369213458.

Code availability
The simulation codes used in this study are available in the Code Ocean
capsule at https://codeocean.com/capsule/8032749/tree/v1.

References
1.
2.

3.

Landau, L. D. & Lifshitz, E. M. Statistical Physics: Volume 5. Vol. 5
(Elsevier, 2013).
Tsui, D. C., Stormer, H. L. & Gossard, A. C. Two-dimensional magnetotransport in the extreme quantum limit. Phys. Rev. Lett. 48,
1559 (1982).
Wen, X.-G. Topological orders in rigid states. Int. J. Mod. Phys. B 4,
239 (1990).

Nature Communications | (2024)15:8963

https://doi.org/10.1038/s41467-024-53077-9
4.

Nayak, C., Simon, S. H., Stern, A., Freedman, M. & Das Sarma, S.
Non-abelian anyons and topological quantum computation. Rev.
Mod. Phys. 80, 1083 (2008).
5. Andersen, T. I. et al. Non-Abelian braiding of graph vertices in a
superconducting processor. Nature 618, 264 (2023).
6. Xu, S. et al. Digital Simulation of Projective Non-Abelian Anyons
with 68 Superconducting Qubits. Chinese Phys. Lett. 40, 060301
(2023).
7. Kitaev, A. Y. Fault-tolerant quantum computation by anyons. Ann.
Phys. 303, 2 (2003).
8. Freedman, M. H. P/NP, and the quantum ﬁeld computer. Proc. Natl.
Acad. Sci. 95, 98 (1998).
9. Chen, X., Gu, Z.-C., Liu, Z.-X. & Wen, X.-G. Symmetry-protected
topological orders in interacting bosonic systems. Science 338,
1604 (2012).
10. Nandkishore, R. & Huse, D. A. Many-body localization and thermalization in quantum statistical mechanics. Annu. Rev. Condens.
Matter Phys. 6, 15 (2015).
11. Abanin, D. A., Altman, E., Bloch, I. & Serbyn, M. Colloquium: Manybody localization, thermalization, and entanglement. Rev. Mod.
Phys. 91, 021001 (2019).
12. Wahl, T. B. & Béri, B. Local integrals of motion for topologically
ordered many-body localized systems. Phys. Rev. Res. 2, 033099
(2020).
13. Wahl, T. B., Venn, F. & Béri, B. Local integrals of motion detection of
localization-protected topological order. Phys. Rev. B 105, 144205
(2022).
14. Huse, D. A., Nandkishore, R., Oganesyan, V., Pal, A. & Sondhi, S. L.
Localization-protected quantum order. Phys. Rev. B 88, 014206
(2013).
15. Khemani, V., Lazarides, A., Moessner, R. & Sondhi, S. L. Phase structure of driven quantum systems. Phys. Rev. Lett. 116, 250401 (2016).
16. Potter, A. C., Morimoto, T. & Vishwanath, A. Classiﬁcation of interacting topological ﬂoquet phases in one dimension. Phys. Rev. X 6,
041001 (2016).
17. Bauer, B. & Nayak, C. Area laws in a many-body localized state and
its implications for topological order. J. Stat. Mech. 2013, P09005
(2013).
18. Bahri, Y., Vosk, R., Altman, E. & Vishwanath, A. Localization and
topology protected quantum coherence at the edge of hot matter.
Nat. Commun. 6, 7341 (2015).
19. Wilczek, F. Quantum time crystals. Phys. Rev. Lett. 109, 160401
(2012).
20. Else, D. V., Bauer, B. & Nayak, C. Floquet time crystals. Phys. Rev.
Lett. 117, 090402 (2016).
21. Yao, N. Y., Potter, A. C., Potirniche, I.-D. & Vishwanath, A. Discrete
time crystals: Rigidity, criticality, and realizations. Phys. Rev. Lett.
118, 030401 (2017).
22. Khemani, V., Moessner, R. & Sondhi, S. L., A Brief History of Time
Crystals, arXiv.1910.10745 (2019)
23. Zhang, X. et al. Digital quantum simulation of Floquet symmetryprotected topological phases. Nature 607, 468 (2022).
24. Bomantara, R. W., Mu, S. & Gong, J. Topological and dynamical
features of periodically driven spin ladders. Phys. Rev. B 103,
235404 (2021).
25. Chew, A., Mross, D. F. & Alicea, J. Time-Crystalline Topological
Superconductors. Phys. Rev. Lett. 124, 096802 (2020).
26. Giergiel, K., Dauphin, A., Lewenstein, M., Zakrzewski, J. & Sacha, K.
Topological time crystals. New J. Phys. 21, 052003 (2019).
27. Wahl, T. B., Han, B. & Béri, B. Topologically ordered time crystals,
arXiv:2105.09694 https://doi.org/10.48550/arXiv.2105.09694
(2021).
28. Doggen, E. V. H., Gornyi, I. V., Mirlin, A. D. & Polyakov, D. G. Slow
many-body delocalization beyond one dimension. Phys. Rev. Lett.
125, 155701 (2020).
7

## PDF page 8

Article
29. Potirniche, I.-D., Banerjee, S. & Altman, E. Exploration of the stability
of many-body localization in d > 1.Phys. Rev. B 99, 205149 (2019).
30. De Roeck, W. & Imbrie, J. Z. Many-body localization: Stability and
instability. Philos. Trans. R. Soc. Math. Phys. Eng. Sci. 375, 20160422
(2017).
31. Zhang, J. et al. Observation of a discrete time crystal. Nature 543,
217 (2017).
32. Kyprianidis, A. et al. Observation of a prethermal discrete time
crystal. Science 372, 1192 (2021).
33. Choi, S. et al. Observation of discrete time-crystalline order in a
disordered dipolar many-body system. Nature 543, 221 (2017).
34. Randall, J. et al. Many-body-localized discrete time crystal with a
programmable spin-based quantum simulator. Science 374, 1474
(2021).
35. Smits, J., Liao, L., Stoof, H. T. C. & van der Straten, P. Observation of
a Space-Time Crystal in a Superﬂuid Quantum Gas. Phys. Rev. Lett.
121, 185301 (2018).
36. Autti, S., Eltsov, V. B. & Volovik, G. E. Observation of a Time Quasicrystal and Its Transition to a Superﬂuid Time Crystal. Phys. Rev.
Lett. 120, 215301 (2018).
37. O’Sullivan, J., Lunt, O., Zollitsch, C. W., Thewalt, M. L. W., Morton, J.
J. L. & Pal, A. Signatures of discrete time crystalline order in dissipative spin ensembles. New J. Phys. 22, 085001 (2020).
38. Pal, S., Nishad, N., Mahesh, T. S. & Sreejith, G. J. Temporal Order in
Periodically Driven Spins in Star-Shaped Clusters. Phys. Rev. Lett.
120, 180602 (2018).
39. Rovny, J., Blum, R. L. & Barrett, S. E. Observation of Discrete-TimeCrystal Signatures in an Ordered Dipolar Many-Body System. Phys.
Rev. Lett. 120, 180603 (2018).
40. Mi, X. et al. Time-crystalline eigenstate order on a quantum processor. Nature 601, 531 (2022).
41. Ying, C. et al. Floquet prethermal phase protected by U(1) symmetry
on a superconducting quantum processor. Phys. Rev. A 105, 012418
(2022).
42. Lu, Z., Shen, P.-X. & Deng, D.-L. Markovian Quantum Neuroevolution
for Machine Learning. Phys. Rev. Appl. 16, 044039 (2021).
43. Kitaev, A. & Preskill, J. Topological Entanglement Entropy. Phys.
Rev. Lett. 96, 110404 (2006).
44. Levin, M. & Wen, X.-G. Detecting topological order in a ground state
wave function. Phys. Rev. Lett. 96, 110405 (2006).
45. Bomantara, R. W. Nonlocal discrete time crystals in periodically
driven surface codes. Phys. Rev. B 104, 064302 (2021).
46. Wen, X.-G. Quantum Orders in an Exact Soluble Model. Phys. Rev.
Lett. 90, 016803 (2003).
47. Satzinger, K. J. et al. Realizing topologically ordered states on a
quantum processor. Science 374, 1237 (2021).
48. Zeng, Y., Hamma, A. & Fan, H. Thermalization of topological entropy
after a quantum quench. Phys. Rev. B 94, 125104 (2016).
49. Zhang, Y.-R. et al. Multipartite entanglement of the topologically
ordered state in a perturbed toric code. Phys. Rev. Res. 4, 023144
(2022).
50. Preskill, J. Quantum Computing in the NISQ era and beyond.
Quantum 2, 79 (2018).
51. Potter, A. C. & Morimoto, T. Dynamically enriched topological orders
in driven two-dimensional systems. Phys. Rev. B 95, 155126 (2017).
52. Wootton, J. R., Lahtinen, V., Wang, Z. & Pachos, J. K. Non-abelian
statistics from an abelian model. Phys. Rev. B 78, 161102 (2008).
53. Kalinowski, M., Maskara, N. & Lukin, M. D. Non-Abelian Floquet Spin
Liquids in a Digital Rydberg Simulator. Phys. Rev. X 13, 031008
(2023).
54. Cerezo, M. et al. Variational quantum algorithms. Nat. Rev. Phys. 3,
625 (2021).
55. Li, W., Lu, Z. & Deng, D.-L. Quantum Neural Network Classiﬁers: A
Tutorial. SciPost Phys. Lect. Notes 061 https://doi.org/10.21468/
SciPostPhysLectNotes.61 (2022).

Nature Communications | (2024)15:8963

https://doi.org/10.1038/s41467-024-53077-9
56. Mølmer, K., Berg-Sørensen, K., Castin, Y. & Dalibard, J. A monte
carlo wave function method in quantum optics, in Optical Society of
America Annual Meeting (Optica Publishing Group, p. MFF1 https://
doi.org/10.1364/OAM.1992.MFF1 1992).
57. Qiskit contributors, Qiskit: An open-source framework for
quantum computing https://doi.org/10.5281/zenodo.2573505
(2023).
58. Xiang, L. xlelephant/long-lived-topological-time-crystalline-orderon-a-quantum-processor: v1.0 https://doi.org/10.5281/ZENODO.
13692134 (2024).

Acknowledgements
We thank X.-J. Liu, L.-M. Duan, and D. Yuan for helpful discussions. The
device was fabricated at the Micro-Nano Fabrication Center of Zhejiang
University. We acknowledge the support from the Innovation Program
for Quantum Science and Technology (Grant Nos. 2021ZD0300200 and
2021ZD0302203), the National Natural Science Foundation of China
(Grant Nos. 92365301, 12274368, 12075128, T2225008), the Zhejiang
Provincial Natural Science Foundation of China (Grant No.
LR24A040002), and Zhejiang Pioneer (Jianbing) Project (No.
2023C01036). T.I. acknowledges support from the National Science
Foundation under Grant No. DMR-2143635. F.M. acknowledges support
from the NSF through a grant for ITAMP (Award No. 2116679) at Harvard
University. A.V.G. was supported in part by the NSF QLCI program
(award No. OMA-2120757). N.Y.Y. acknowledges support from the U.S.
Department of Energy via the National Quantum Information Science
Research Centers Quantum Systems Accelerator, from the Army
Research Ofﬁce (Grant NO. W911NF-24-1-0079) and from a Simons
Investigator award. W.J., S.J., W.L., Z.L., Z.-Z.S., and D.-L.D. acknowledge
in addition support from the Tsinghua University Dushi Program and
Shanghai Qi Zhi Institute.

Author contributions
L.X. and Z.B. carried out the experiments and analyzed the experimental
data under the supervision of Q.G. and H.W.; W.J., L.X., S.J., and Z.B.
performed the numerical simulations under the supervision of D.-L.D.,
Q.G., F.L., F.M., Z.-X.G., A.V.G., and T.I.; D.-L.D., W.J., F.L., F.M., Z.-X.G.,
A.V.G., N.Y., T.I., W.L., Z.L., and Z.-Z.S. conducted the theoretical analysis; H.L. and J.C. fabricated the device supervised by H.W.; D.-L.D.,
Q.G., W.J., L.X., H.W., F.L., Z.-X.G., A.V.G., F.M., and T.I. co-wrote the
manuscript; H.W., Q.G., C.S., Z.W., L.X., Z.B., Z.S., S.X., K.W., J.C., F.J.,
X.Z., Z.Z., F.S., N.W., C.Z., Y.W., Y.Z., J.Z., Z.C., A.Z., Z.T., T.L., Y.G., J.D.,
X.Z., H.D., and P.Z. contributed to experimental setup. All authors contributed to the discussions of the results.

Competing interests
The authors declare no competing interests.

Additional information
Supplementary information The online version contains
supplementary material available at
https://doi.org/10.1038/s41467-024-53077-9.
Correspondence and requests for materials should be addressed to
Qiujiang Guo, H. Wang or Dong-Ling Deng.
Peer review information Nature Communications thanks David Long,
Petr Zapletal and the other, anonymous, reviewer for their contribution
to the peer review of this work. A peer review ﬁle is available.
Reprints and permissions information is available at
http://www.nature.com/reprints
Publisher’s note Springer Nature remains neutral with regard to jurisdictional claims in published maps and institutional afﬁliations.

8

## PDF page 9

Article

https://doi.org/10.1038/s41467-024-53077-9

Open Access This article is licensed under a Creative Commons
Attribution 4.0 International License, which permits use, sharing,
adaptation, distribution and reproduction in any medium or format, as
long as you give appropriate credit to the original author(s) and the
source, provide a link to the Creative Commons licence, and indicate if
changes were made. The images or other third party material in this
article are included in the article’s Creative Commons licence, unless
indicated otherwise in a credit line to the material. If material is not
included in the article’s Creative Commons licence and your intended
use is not permitted by statutory regulation or exceeds the permitted
use, you will need to obtain permission directly from the copyright
holder. To view a copy of this licence, visit http://creativecommons.org/
licenses/by/4.0/.
© The Author(s) 2024

Nature Communications | (2024)15:8963

9
