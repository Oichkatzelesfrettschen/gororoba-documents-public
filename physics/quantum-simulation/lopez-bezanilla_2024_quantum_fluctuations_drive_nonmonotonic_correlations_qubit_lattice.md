Source: see manifest row of the PDF
PDF sha256: 4812c408e5a152d8783acf17844e3ab80ec9e02f59e4d68d690e348a3ff19ce4
License: CC-BY-4.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of lopez-bezanilla_2024_quantum_fluctuations_drive_nonmonotonic_correlations_qubit_lattice.pdf

Transcription of `lopez-bezanilla_2024_quantum_fluctuations_drive_nonmonotonic_correlations_qubit_lattice.pdf` in this directory, 7 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 3 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories; pages 1-2, 4-7 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Article

https://doi.org/10.1038/s41467-023-44281-0

Quantum ﬂuctuations drive nonmonotonic
correlations in a qubit lattice
Received: 20 June 2023
Accepted: 6 December 2023

1234567890():,;

1234567890():,;

Check for updates

Alejandro Lopez-Bezanilla1
Avadh Saxena1

, Andrew D. King

2

, Cristiano Nisoli1 &

Fluctuations may induce the degradation of order by overcoming ordering
interactions, consequently leading to an increase of entropy. This is particularly evident in magnetic systems characterized by nontrivial, constrained
disorder, where thermal or quantum ﬂuctuations can yield counterintuitive
forms of ordering. Using the proven efﬁciency of quantum annealers as programmable spin system simulators, we present a study based on entropy
postulates and experiments on a platform of programmable superconducting
qubits to show that a low level of uncertainty can promote ordering in a system
impacted by both thermal and quantum ﬂuctuations. A set of experiments is
proposed on a lattice of interacting qubits arranged in a triangular geometry
with precisely controlled disorder, effective temperature, and quantum ﬂuctuations. Our results demonstrate the creation of ordered ferrimagnetic and
layered anisotropic disordered phases, displaying characteristics akin to the
elegant order-by-disorder phenomenon. Extensive experimental evidence is
provided for the role of quantum ﬂuctuations in lowering the total energy of
the system by increasing entropy and defect clustering. Our thorough and
comprehensive application of an intentionally introduced noise on a quantum
platform provides insight into the dynamics of defects and ﬂuctuations in
quantum devices, which may help to reduce the cost associated with quantum
processing.

Entropy-driven ordering mechanisms have been successfully
employed to explain the formation of colloid materials1,2, although
only a few observations in macroscopic systems3 have been reported
thus far. Experimental investigations into magnetic ordering driven by
thermal and quantum ﬂuctuations have been limited, despite the
potential impact a deep understanding of the fundamental mechanisms governing the formation of ordered structures could have on the
assembly and organization of magnetic nanostructures.
The state of a disordered system is deﬁned by the even or
uniform distribution of its constituent elements throughout space.
Conversely, the concept of order pertains to the arrangement of
these elements, where they tend to segregate or group together
based on their similar properties. The second law of

thermodynamics established entropy as a measure of disorder, with
Boltzmann’s expression for the entropy of a closed system, S ∼ ln Ω,
stating that the entropy S increases with a higher number of
accessible states Ω for the system4. Temperature, which relates to
thermal ﬂuctuations, plays a crucial role in altering the entropy or
degree of ordering in a system. Higher temperatures provide more
ways to distribute energy among the available states, leading to
higher entropy values. While it may seem counterintuitive, an
increase in thermal ﬂuctuations can actually promote ordering
within a system through the phenomenon known as order by
disorder5–8. This phenomenon occurs in frustrated magnetic systems, where the classical ground state manifold possesses higher
symmetry than the underlying Hamiltonian. Both thermal and

1

Theoretical Division, Los Alamos National Laboratory, Los Alamos 87545 NM, USA. 2D-Wave Systems̥, V5G, Burnaby, BC, Canada.
e-mail: alejandrolb@gmail.com

Nature Communications | (2024)15:589

1

## PDF page 2

Article
quantum ﬂuctuations can break the degeneracy and induce ordering in the system while increasing its entropy.
In the present investigation, we design magnetic systems with a
highly frustrated classical ground state manifold in which to observe
an increase of correlations between magnetic moments when thermal
and quantum ﬂuctuations are ﬁnely tuned. The idea that adding
quantum ﬂuctuations could promote order appears counterintuitive.
For example, in magnetic kagome lattices a monotonic increase of
magnetic moment correlations is found with increasing temperature.
Here we demonstrate that the inclusion of quantum ﬂuctuations in
asymmetric (Lieb) kagome lattices can produce nonmonotonic correlations among magnetic moments.

https://doi.org/10.1038/s41467-023-44281-0

This challenging problem for established macroscopic magnetic
realizations9–13 can be implemented in a straightforward manner in a
quantum annealer hardware. Free of spurious interactions and defects
that plague spin ice systems, the platform of interconnected qubits
provided by D-Wave Quantum (Fig. 1a) enables the observation of
many-body interactions driven uniquely by entropic effects. By using
entanglement and superposition of tailor-designed quantum states,
we unveil with a high degree of accuracy the interplay between temperature and domain-wall correlation in a continuously distorted while
frustrated qubit lattice. In particular, the maximally frustrated kagome
lattice is taken as a reference, and an effective deformation is introduced by modifying coupling parameters that mimics an applied strain
to the real-space lattice. The kagome lattice is thus placed in a broader
antiferromagnet geometry, showing that its constrained and correlated disorder is a critical point between fully ordered and uncorrelated disordered states. This ﬂexibility of the degree of disorder in one
single topology allows us to study the nonmonotonic evolution of
qubit-qubit ordering within an effective range of temperature.
Our model of lattice transformation is described as the continuous deformation of a kagome (depleted triangular lattice) to a Lieb
lattice (depleted square lattice), and to a deformed hexagonal lattice,
as shown in Fig. 1c–e. Each site has
 a classical
  representation given by a
magnetic moment in either " or # state orientation. In the

following, we will refer to two types of sites, σ and Σ, denoting the Ising
qubits circled in black and yellow, respectively. The unit cell in Fig. 1b
features three nodes and two antiferromagnetic coupling constants J
and JL. Different classical ground states can be obtained depending on
the ratio JL/J, which controls the system frustration.
JL/J < 1 yields an ordered ferrimagnetic conﬁguration (Fig. 1c),
where all σ qubits have the same alignment, and opposite to that of Σ
qubits. The net magnetic moment per unit cell is ∣M∣ = 1/3. If JL/J > 1, the
weaker coupler J is frustrated in a layered ground state. σ-site qubits
align antiferromagnetically (Fig. 1e) along the stronger (shorter in the
lattice representation) bond JL, forming layered, parallel antiferromagnetic lines, as shown by the solid gray lines in Fig. 1e. The Σsite qubits can be viewed as buffers that do not transfer information
between antiferromagnetic lines, namely the energy of the ground
state is unaltered upon a spin-ﬂip operation on any of those sites. They
are shown in white since they exhibit no speciﬁc order. The ordered
lines are thus mutually uncorrelated and disordered in the vertical
direction. This is only true in the ground state, as we shall see below,
much as in the prototypical domino model of order by disorder5.
Fluctuations develop correlations among antiferromagnetic lines,
making the layered phase a quasi-one-dimensional (Q1D) phase, and
the average magnetization zero.
At the critical point, JL = J, the lattice becomes a frustrated Ising
antiferromagnet on a kagome lattice14,15 (Fig. 1d). The low-energy state
manifold of the two models consists of disordered qubits that obey the
ice rule, namely the three spins in a triangle must add up to ± 1. In the
ground state at zero temperature qubits are disordered and strongly
correlated, with a ﬁnite correlation length16. The average magnetization is zero.
Note that both the ferrimagnetic (JL/J < 1) and the layered (JL/J > 1)
phases are deviation from the kagome ice conﬁguration (JL/J = 1), as
both obey the ice rule as deﬁned above in terms of minimal ± 1
charge16. Therefore, at T = 0 the hexagonal qubit ice is the structural
critical point between an ordered ferrimagnetic phase and an anisotropically disordered layered phase. Analogously, square ice had been
also shown to be a structural critical point between antiferromagnetic
order and a state of subextensive disorder 15,17,18. After discussing the

Fig. 1 | The system under study in its three ground states. a The D-Wave quantum
processing unit in use. (b) Unit cell of studied model composed of three nodes
coupled in a triangle with two different couplers, J and JL. Panels (c–e) show the Lieb
lattice with anisotropic couplings J (solid gray lines), and JL (dotted gray lines). Solid
gray lines represent stronger couplings. Topological Lieb-to-kagome

transformation is equivalent to reducing JL with respect to J that is kept constant. In
(c), J > JL yields a ferrimagnetic ground state conﬁguration. The kagome ice conﬁguration in (d) is reached when JL = J. The layered conﬁguration in (e) is equivalent
to considering J < JL. Up and down magnetic moments are depicted in blue and red
respectively.

Results and discussion

Nature Communications | (2024)15:589

2

## PDF page 3

<b>Article</b>
https://doi.org/10.1038/s41467-023-44281-0
b)
<math>-2\pi</math>
<math>a)_{0.35}</math>
<math>1\mu s</math>
<math>100 \mu s</math>
0.30
<math>q_{y}</math>
<math>= 0.5</math>
0.25
<math>= 0.6</math>
<math>= 0.7</math>
0.20
<math>\widehat{\boldsymbol{\varepsilon}}</math>
<math>= 0.8</math>
0.15
<math>= 0.9</math>
<math>J = 1.0</math>
0.10
<math>2\pi</math>
<math>\langle m \rangle = \sqrt{\sum} M^2</math>
0.05
0
0.00
<math>q_x</math>
0 25 0 50 0 75 1 00 1 25 1 50 1 75 2 00
<math>J_L/J</math>
<math>2\pi</math>
<math>-2\pi</math>
c)
d)
<math>q_{y}_{\mathsf{o}}</math>
<math>q_y^{\, \, \scriptscriptstyle 0}</math>
<math>-2\pi</math>
<math>2\pi \sqrt{2}</math>
0
<math>-2\pi</math>
<math>q_x</math>
<math>2\pi\,q_x</math> o
<math>2\pi</math>
e)
<math>I/J_L = 2.0</math>
<math>J/J_L = 1.8</math>
1.00
<math>-J/J_L = 1.6</math>
<math>J/J_L = 1.4</math>
0.95
<math>J/J_L = 1.2</math>
<math>-</math> <math>J/J_L = 1.1</math>
J/J<sub>L</sub> = 1.0
Fraction
0.90
<math>J/J_L = 0.99</math>
<math>- J/J_L = 0.98</math>
<math>J/J_L = 0.95</math>
0.85
<math>J/J_L = 0.9</math>
<math>J/J_L = 0.8</math>
0.80
<math>t_s = 100 \mu s</math>
<math>t_s = 1 \mu s</math>
<math>I/I_1 = 0.5</math>
<math>= 0.4</math>
0.75
<math>= 0.3</math>
<math>10^{1}</math>
<math>10^{1}</math>
10<sup>2</sup>10<sup>0</sup>
10°
10
<math>J/J_L = 0.2</math>
<math>T_{eff} \sim 1/J_I</math>
<math>T_{eff} \sim 1/J_L</math>
<math>J/J_L = 0.1</math>
after annealing for <math>J/J_L = 1.5, 1.0, 0.75</math>. <b>b</b> corresponds to the ferrimagnetic case, (<b>c</b>) to
Fig. 2 | Structure factors of three ground states obtained from quantum
the kagome ice, and (d) the layered case. All phases obey the ice rule, as shown in
<b>annealing experiments. a</b> Average magnetization per qubit <math>\langle m \rangle</math> vs. <math>J_I/J</math> obtained
from quantum annealing for different values of J and therefore different effective
plots of fraction of ice-rule obeying vertices vs. <math>T_{\rm eff}</math> for fast (e) and slow (f)
temperatures, <math>T_{eff}</math>. In the ground states <math>|M| > 0</math> only for <math>J_L/J < 1</math>. The various ground
annealings.
state symmetries are shown via the Fourier transform of the qubit-qubit correlation
where <math>\hat{\sigma}</math>, <math>\hat{\Sigma}</math> are Pauli matrices of the corresponding qubits on <math>\sigma</math>, <math>\Sigma</math> sites,
anticipated ground state, we move on to investigating a finite-sized
respectively. In the absence of the transverse field, <math>\Gamma = 0</math>, Fock products
realization of <math>J_L < J</math> kagome-derived lattices, where the system dynam-
of eigenstates of <math>\sigma^z</math> are eigenvalues of the Hamiltonian, and the pro-
ics is dominated by quantum rather than thermal fluctuations.
Our finite-size qubit model consists of a lattice of 21 × 21 anti-
blem maps exactly onto the classical one described above. If <math>\Gamma \neq 0</math>, the
ferromagnetic (AFM) chains, along with the mediating qubits, resulting
terms within the first parenthesis do not commute with the terms
in a total of 641 logical qubits. To represent a logical spin, three qubits
within the second parenthesis, and the transverse field subjects the
are connected by strong ferromagnetic couplings with a magnitude of
spin degrees of freedom to quantum fluctuations. The unitless para-
<math>J=-2</math>, resulting in a total of 1923 qubits embedded in a D-Wave
meter <math>s = t/t_f</math> controls the annealing progress from the quantum-
Pegasus topology. The collective dynamics of these qubits is described
mechanical superpositions of states at <math>s = 0</math> to the classical state at <math>s = 1</math>.
The Ising energy scale is thus controlled by <math>\mathcal{J}(s)</math> which increases as the
by a quantum transverse-field Ising model, governed by the Hamilto-
nian:
quantum fluctuations <math>\Gamma(s)</math> away out according to well-established
annealing protocols.
Starting from a transverse-field induced quantum-superposition
<math display="block">H = \mathcal{J}(s) \left( J_L \sum_{\langle \sigma, \sigma' \rangle} \hat{\sigma}^z \hat{\sigma}^{/z} + J \sum_{\langle \sigma, \Sigma \rangle} \hat{\sigma}^z \hat{\Sigma}^z \right) - \Gamma(s) \left( \sum_{\sigma} \hat{\sigma}^x + \sum_{\Sigma} \hat{\Sigma}^x \right)</math>
(1)
state, the forward annealing protocol is used to obtain thousands of
classical configurations at different <math>J_1/J</math> ratios. Figure 2a shows the
magnetization per qubit vs. <math>J_L/J</math> for a series of <math>J</math> values, averaged over
Nature Communications | (2024)15:589
3

## PDF page 4

Article

Fig. 3 | Entropy-induced correlations of the domain walls. a A domain wall sitting
on top of a Σ site ﬁxes the qubit with an entropic cost that is lower in energy than in
the case shown in (b). In (c), two σ-site domain walls are “paired” if both sit around
the same Σ site. Pairing creates entropic advantage with respect to two domain
walls away from each other by releasing a Σ ﬂoppy qubit. Dotted red lines point out
the transverse correlation between the domain walls. Up and down magnetic
moments are depicted in blue and red, respectively.

25600 annealed samples. In the ground state of an inﬁnite lattice in
the ferrimagnetic phase (JL/J < 1), where the magnetization is the order
parameter, the two twofold coordinated spins antialign with the spin in
the fourfold vertex. The stepwise dashed-dotted line points out the
absolute value of its magnetization at T = 0, with a constant value of 1/3
for JL/J < 1 and of zero for JL ≥ J. The open boundaries in the chains
induce ﬂuctuations that cause the initially ﬂat line to transform into a
smoothly increasing curve for JL/J > 1. The ﬁnite value of J precludes the
magnetization 〈m〉 from abruptly transitioning to 1/3, allowing for the
possibility of deviations from the 2-up-1-down rule in the ferrimagnetic
phase. At the exact value of J = JL, the ensemble meets the degenerate
ice-rule ground states of the kagome lattice, with a ± 1 net magnetization on each triangle realizing an overall 〈m〉 = 0. The magnetization of
the slab acquires ﬁnite values due to its ﬁnite size. The quality of the
annealing process is reﬂected in the two sets of lines plotted in Fig. 2e,
f. A swift annealing of tf = 1μs demonstrates to be less efﬁcient than a
slower tf = 100 μs annealing yielding lower 〈m〉 in the ferrimagnetic phase.
Structure factors indicating the underlying spin alignment
D
Efor
P
each JL/J ratio are displayed in Fig. 2b-d. SðqÞ ∼ i,j eqðri rj Þ si  sj is
the Fourier transform of the correlation between the ith- and the jthspin, and pinpoints a number of features: the ferrimagnetic order is
clearly visible in Fig. 2b with peaks at q = ( ± π, ± π) of the Brillouin zone.
The S(q) ≠ 0 at q = (0, 0) shows evidence of long-range correlations.
Figure 2d shows a ridged line structure expected in the layered phase
as corresponds to the one-dimensional antiferromagnetic order. Figure 2c shows the smeared hexagonal pattern typical of the kagome
antiferromagnet.
It is also possible to explore higher energy states for ﬁxed
frustration JL/J, by varying both JL and J at a constant ratio. The
coupling strength is subjected to at-will variations to mimic the
effect of temperature, so that increasing J is equivalent to reducing the effect of thermal ﬂuctuations. With discrete variations of
the coupling strength (JL = 0.1. . 1.0 in steps of 0.1) the system’s
effective temperature is mimicked, and it can be regarded as
inversely proportional to the coupling strength between logical
qubits. In this scenario, Teff = 1/JL has been used15 to represent a
useful notion of effective temperature, Teff. Figure 2d, e display
the fraction of triangles obeying the ice rule plotted as a function

Nature Communications | (2024)15:589

https://doi.org/10.1038/s41467-023-44281-0

of Teff = 1/JL, for ﬁxed values of JL/J during fast (d) and slow (e)
annealings. The system obeys the ice rule at low Teff.
The dimensionally reduced phase affords interesting similarities
with the domino model5, where correlations develop as the system is
subject to thermal ﬂuctuations. The elegant order-by-disorder
mechanism is due to the presence of excitations, absent in the
ground state. Other layered nanomagnets recently realized19,20 behave
similarly by promoting linear arrangements that are mutually uncorrelated in the ground state, but can be correlated by entropy under
stress. Interestingly, an analogous mechanism of entropy-induced
correlations in the Q1D phase can also be expected, which relies on the
sea of free Σ spins, that are uncorrelated in the ground state but correlate under ﬂuctuating excitations.
Figure 3 illustrates that this mechanism proceeds through an
entropic gain stemming from the correlation of domain walls. It is
essential to note that in the ground state of the quasi-one-dimensional
(Q1D) system, all σ-qubits lines (indicated by black circles) exhibit
antiferromagnetic ordering, while the Σ qubits (indicated by yellow
circles) have random orientations because their net coupling with the
antiferromagnetic σ spins is zero. Consequently, in the ground state,
there is no correlation among the antiferromagnetic lines. Excited
states, on the other hand, involve the formation of domain walls on
these lines, which separate domains with different antiferromagnetic
orientations.
It is important to observe that a domain wall in an antiferromagnetic line possesses lower energy when located at the position of a Σ qubit, effectively locking it in an orientation opposite to that
of the domain wall. In this scenario, the energy cost of creating a
domain wall between two contiguous σ sites at both sides of a Σ spin is
ΔE = 2(JL − J). In contrast, placing the same domain wall away from a Σ
spin (as depicted in Fig. 3b) would result in a higher energy cost,
ΔE = 2JL. It is therefore energetically advantageous for a domain wall to
be adjacent to a Σ spin.
Next, consider two domain walls on two adjacent antiferromagnetic lines, with Σ spins in between. If these two domain walls
lock onto the same Σ spin, they, and the domain they separate, adopt
the same orientation, thereby contributing to a transverse correlation.
However, there is no energy preference for having the two domain
walls aligned by the same Σ spin. The energy remains the same if they
lock onto two different Σ qubits. Nevertheless, there is an entropic
advantage in having the two domain walls aligned because it allows
one Σ spin to remain free to ﬂuctuate, resulting in an energy gain of
ΔS = ln2. Consequently, we can deduce that entropy promotes the
alignment of domain walls in parallel chains and favors the existence of
ﬂoppy spins, increasing the transverse correlation among these lines.
To investigate this ﬂuctuation-induced transverse correlation,
both perpendicular across lines, hσσ 0 i? , and parallel along a line, hσσ 0 ik ,
nearest-neighbor correlations are considered and deﬁned as
hσσ 0 i? =

*
*
X
l,i

*
hσσ 0 ik =

*
X
l,i

+
σ iðlÞ σ ðli + 1Þ

ð2Þ

+
ðlÞ
σ ðlÞ
i σi + 1

ð3Þ

where the star * denotes the normalized sum over σ spins at the ith
position along the lth line. 〈〉 denotes the average over 25600 classical
states. At T = 0, hσσ 0 i? = 0, since the prevalent energy is the coupling
term that antiferromagnetically aligns the mutually uncorrelated
chains preventing the formation of domain walls. At large temperature, J is overwhelmed by thermal ﬂuctuations and the whole system
becomes uncorrelated. As a result, it is anticipated that hσσ 0 i? will
exhibit a non-monotonic behavior with respect to the (effective)
temperature.
4

## PDF page 5

Article

https://doi.org/10.1038/s41467-023-44281-0

Fig. 4 | Entropic transverse correlations. a The transverse correlation hσσ 0 i? vs.
Teff = 1/JL showing its nonmonotonic behavior. Curves obtained after annealing time

of tf = 1μs. b Longitudinal correlation along the antiferromagnetic lines. c, d Same as
in (a) and (b), respectively, for an annealing time of tf = 100 μs.

In the following, the effective temperature of the parallel chain
system will be taken as inversely proportional to the coupling strength
between logical qubits, Teff ~ 1/JL15. Figure 4b, d shows hσσ 0 ik plotted as
a function of Teff for a series of values of JL/J. Annealing procedures are
set to last tf = 1μs and tf = 100 μs, respectively. As it is generally the case
for correlations, the curves are monotonic in Teff for J/JL < 1 (i.e. when
the system is in the Q1D phase). At low-Teff, assuming that the frustration quantiﬁer J/JL remains close to 1, an antiferromagnetic state
(hσσ 0 ik = 1) is reached at the lowest Teff. If J/JL → 1−, the curves approach
uniformly the kagome ice behavior (black line). The collinear correlation for kagome ice at low-Teff is only slightly higher than the value
hσσ 0 ik =  4=6 + 2=6 =  1=3, which can be readily obtained via a
counting argument on an ice-rule obeying triangle. Curves for J/JL > 1
correspond to a ferrimagnetic regime whose correlations become
positive at low-Teff. Linear correlations are slightly stronger for slower
annealings as generally expected in optimal an annealing process.
We analyze the transverse correlations hσσ 0 i? , plotted in Figure 4a, c, which exhibit a nonmonotonic behavior for J/JL < 1. As the
value of J/JL increases, the correlations become stronger at the same
effective temperature due to the inﬂuence of the Σ qubits, whose
coupling with σ qubits is J. For each curve, the temperature associated
with the maximum transverse correlation decreases as J/JL → 1, indicating the transition to an isotropically correlated kagome ice state. In
this state, the correlations are monotonic in temperature, with the
maximum occurring at the ground state.
The obtained correlation at low Teff, hσσ 0 i? ≈0:14, agrees well with
experimental ﬁndings for kagome systems discussed in refs. 21,22 for a
nanomagnetic, artiﬁcial kagome annealed via AC demagnetization.
The observed correlations, consistently weaker than those of kagome
ice, suggest the absence of symmetry breaking in a large system. The
extraction of an order parameter reveals at most very small values of
around 18% which are explainable with counting arguments for a ﬁnite
system made of an odd number of lines.
Notably, the transverse correlations shown in Fig. 4a, c exhibit
stronger values during faster annealings. While faster annealings

demonstrate only slightly smaller collinear correlations, they display
signiﬁcantly larger transverse correlations. For example, in the case of
J/JL = 0.9 at Teff = 1, the faster annealing exhibits an approximately 50%
increase in transverse correlation compared to the slower annealing,
while experiencing only a 7% decrease in collinear correlation. This
suggests that the enhancement of transverse correlation during faster
annealings arises primarily from quantum ﬂuctuations rather than
from a large number of domain walls.
In the presence of a small transverse ﬁeld Γ, the system experiences quantum ﬂuctuations, leading to increased transverse correlations. The second term of the Hamiltonian in Equation (1) can be
considered as a perturbative term that breaks the degeneracy of the
classical ground state manifold. Conﬁgurations with more unlocked
qubits, which correspond to more paired domain walls, have lower
total energy23,24. Therefore, the full quantum Hamiltonian including the
transverse ﬁeld Γ generates conﬁgurations that, with more paired
domain walls and fewer locked Σ qubits, are energetically favored.
Although Γ = 0 always at the end of an annealing, decreasing it faster
can promote states that are energetically advantageous when Γ ≠ 0.
This explains the larger transverse correlation observed during faster
annealings.
A comparison between the hσσ 0 i? and hσσ 0 ik panels of Figure 4
reveals their opposite evolution at low Teff. This can be attributed to
the increased formation of domain walls, leading to a decrease in
longitudinal correlation and an increase in transverse correlation
through the mechanism of domain wall pairing described earlier. In the
ferrimagnetic phase, hσσ 0 ik is equal to 1, while in the layered phase it is
equal to − 1, due to the ﬁnite size of the sample.
Subtle variations in the annealing protocols can have signiﬁcant
effects on quantifying the degree of order, as quantum ﬂuctuations
play a crucial role in enhancing the spin-spin correlation represented
by hσσ 0 i? . The slow forward annealing protocol used so far anneals an
open quantum system that drops out of thermal equilibrium as
quantum ﬂuctuations (Γ(s)) decrease, causing the system response
time to exceed the annealing time. By introducing a pause-and-quench

Nature Communications | (2024)15:589

5

## PDF page 6

Article

Fig. 5 | s-Dependent transverse correlations. Correlations are probed at individual s values using a pause/quench protocol. To eliminate dependence of Γ(s)/J(s)
on s over the region of measurement, a prefactor α(s) is introduced. Inset shows the
ﬂat energy range obtained by multiplying J ðsÞ by the set of α values shown in the
black curve. As a function of Γ(s)/J, we see a peak in transverse correlations hσσ 0 i? .
This is consistent with a region of order between the perturbative regime (Γ ≪ J) and
the paramagnetic regime (Γ ≫ J).

protocol, we can probe midanneal properties: pausing at an s* < 1
allows the system to approach thermal equilibrium of the open
quantum system. After the pause, rapidly quenching s to 1 collapses
the wavefunction, approximately reading out the system at s*. Note
that a change of s* changes both Γ(s*) and J ðs* Þ, when the goal is to
change only Γ(s*). To achieve that, the couplings Jij are multiplied by a
prefactor α(s*) such that the product α(s*)J(s*) remains constant across
the range of s* values to be probed.
Considering the terms proportional to Γ in the Hamiltonian of
Eq. (1) as the interaction Hamiltonian, a perturbative treatment at
ﬁrst order shows that conﬁgurations with the maximum number of
ﬂoppy qubits are energetically favored. In other words, a small Γ
ﬁeld causes a ﬁne splitting of the degeneracy of the classical ground
state into a number of energy levels, favoring conﬁgurations with a
larger number of ﬂoppy spins. When Γ is annealed very slowly, this
mechanism is less relevant although signiﬁcant than in a swift
annealing dynamics where it resembles more a quench on
the Γ ﬁeld.
Figure 5 displays the dependence of hσσ 0 i? with the degree by
which the system is affected by quantum ﬂuctuations induced in the
lattice according to a reverse annealing protocol. The ﬁgure plots
hσσ 0 ik vs. Γ/JL, which represents a good quantiﬁer for the amplitude of
quantum ﬂuctuations induced in the system. The plot clearly illustrates
that the transverse correlation increases with the ratio of the transverse ﬁeld strength Γ to the exchange coupling JL: Larger quantum
ﬂuctuations lead to stronger correlations. The curve reaches a maximum value, and for larger Γ, the transverse Ising models are known to
undergo a transition to a quantum paramagnetic phase, typically

Nature Communications | (2024)15:589

https://doi.org/10.1038/s41467-023-44281-0

occurring at Γ ≈ J, as shown in the ﬁgure. This behavior serves as a
signiﬁcant signature of observable quantum effects arising from
quantum ﬂuctuations, as it provides experimental evidence of the
ability of quantum ﬂuctuations to induce correlations among the
chains that are absent otherwise. When considering the same number
of defects, those located at both sides of a locked qubit exhibit a lower
conﬁguration energy compared to the defects situated in different
regions of the parallel chains that involve two intermediate
qubits (Fig. 3c).
In summary, we have conducted a series of experiments in a
frustrated magnetic lattice to provide understanding of the ability
of quantum ﬂuctuations to enhance ordering. Based on fundamental entropic principles, we have demonstrated that groundstate modiﬁcation by quantum-mechanical ﬂuctuations may induce
a domain-wall entropic-interaction mechanism that reduces the
disorder in the perpendicular direction leading to nonmonotonic
transverse correlations of antiferromangnetically aligned magnetic
moments. We have demonstrated the continuous deformation of a
kagome lattice to ferrimagnetic and layered structures, by engineering the ratio between coupling constants. This ﬂexibility in
controlling the degree of disorder within a single topology has
enabled us to explore the nonmonotonic evolution of qubit-qubit
ordering within an effective range of temperature, to ﬁnd that a
given amount of uncertainty in the form of ﬂuctuations can promote ordering within the quantum system. Our ﬁndings shed light
on the mechanisms and physical conditions leading to defect clustering under the action of quantum ﬂuctuations, which can pave the
way for improved quantum annealing systems. Furthermore, our
experiments on entropic crystallization have revealed the remarkable inﬂuence of random ﬂuctuations in inducing the emergence of
ordered patterns in qubit systems, providing a solid foundation for
future investigations into the manipulation and control of quantum
states for improved computational performance.
Our embedding of nearly 2000 qubits in a superconducting
quantum annealer to study large magnetic lattices demonstrates the
effectiveness of quantum annealing in modeling the mechanisms that
enhance correlations between quantum states. A detailed understanding of the physics of defect clustering can be obtained to guide
the development of targeted strategies for minimizing errors and
devising innovative approaches for interconnected qubit arrays. These
ﬁndings may have implications for the design and organization of
magnetic nanostructures as well as the engineering of quantum
materials with desired properties.

Data availability
Data supporting the ﬁndings of this paper are available from the corresponding author upon request.

References
1.

2.

3.
4.

5.

van Anders, G., Klotsa, D., Ahmed, N. K., Engel, M. & Glotzer, S. C.
Understanding shape entropy through local dense packing. Proc.
Natl Acad. Sci. USA 111, E4812-E4821 (2014).
Je, K., Lee, S., Teich, E. G., Engel, M. & Glotzer, S. C. Entropic formation of a thermodynamically stable colloidal quasicrystal with
negligible phason strain. Proc. Natl Acad. Sci. USA 118,
e2011799118 (2021).
Saglam, H. et al. Entropy-driven order in an array of nanomagnets.
Nat. Phys. 18, 706–712 (2022).
Boltzmann, L.Über die Beziehung zwischen dem zweiten Hauptsatze der mechanischen Wärmetheorie und der Wahrscheinlichkeitsrechnung resp. den Sätzen über das Wärmegleichgewicht, vol.
2 of Cambridge Library Collection—Physical Sciences, 164–223
(Cambridge University Press, 2012).
Villain, J., Bidaux, R., Carton, J.-P. & Conte, R. Order as an effect of
disorder. J. Phys. 41, 1263–1272 (1980).
6

## PDF page 7

Article
6.

Green, A. G., Conduit, G. & Krüger, F. Quantum order-by-disorder in
strongly correlated metals. Annu. Rev. Condens. Matter Phys. 9,
59–77 (2018).
7. Tchernyshyov, O., Moessner, R. & Sondhi, S. L. Order by distortion
and string modes in pyrochlore antiferromagnets. Phys. Rev. Lett.
88, 067203 (2002).
8. Zhitomirsky, M. E., Gvozdikova, M. V., Holdsworth, P. C. W. &
Moessner, R. Quantum order by disorder and accidental soft mode
in er2ti2o7. Phys. Rev. Lett. 109, 077204 (2012).
9. Nisoli, C., Moessner, R. & Schiffer, P. Colloquium: Artiﬁcial spin ice:
designing and imaging magnetic frustration. Rev. Mod. Phys. 85,
1473 (2013).
10. Skjærvø, S. H., Marrows, C. H., Stamps, R. L. & Heyderman, L. J.
Advances in artiﬁcial spin ice. Nat. Rev. Phys. 2, 1–16 (2019).
11. Schiffer, P. & Nisoli, C. Artiﬁcial spin ice: Paths forward. Appl. Phys.
Lett. 118, 110501 (2021).
12. Ortiz-Ambriz, A., Nisoli, C., Reichhardt, C., Reichhardt, C. J. & Tierno,
P. Colloquium: Ice rule and emergent frustration in particle ice and
beyond. Rev. Mod. Phys. 91, 041003 (2019).
13. Morrison, M. J., Nelson, T. R. & Nisoli, C. Unhappy vertices in artiﬁcial
spin ice: new degeneracies from vertex frustration. N. J. Phys. 15,
045009 (2013).
14. Wills, A., Ballou, R. & Lacroix, C. Model of localized highly frustrated
ferromagnetism: The kagomé spin ice. Phys. Rev. B 66,
144407 (2002).
15. King, A. D., Nisoli, C., Dahl, E. D., Poulin-Lamarre, G. & Lopez-Bezanilla, A. Qubit spin ice. Science 373, 576–580 (2021).
16. Kanô, K. & Naya, S. Antiferromagnetism. the kagomé ising net. Prog.
Theor. Phys. 10, 158–172 (1953).
17. Nisoli, C. The concept of spin ice graphs and a ﬁeld theory for their
charges. AIP Adv. 10, 115102 (2020).
18. Möller, G. & Moessner, R. Artiﬁcial square ice and related dipolar
nanoarrays. Phys. Rev. Lett. 96, 237202 (2006).
19. Gilbert, I. et al. Emergent reduced dimensionality by vertex frustration in artiﬁcial spin ice. Nat. Phys. 12, 162–165 (2016).
20. Stopfel, H. et al. Multiple energy scales in mesospin systems: the
vertex-frustrated saint George lattice. Phys. Rev. Mater. 5,
114410 (2021).
21. Rougemaille, N. et al. Artiﬁcial kagome arrays of nanomagnets: a
frozen dipolar spin ice. Phys. Rev. Lett. 106, 057209 (2011).
22. Zhang, S. et al. Perpendicular magnetization and generic realization
of the ising model in artiﬁcial spin ice. Phys. Rev. Lett. 109,
087201 (2012).
23. King, A. D. et al. Observation of topological phenomena in a programmable lattice of 1,800 qubits. Nature 560, 456–460 (2018).
24. Boixo, S., Albash, T., Spedalieri, F. M., Chancellor, N. & Lidar, D. A.
Experimental signature of programmable quantum annealing. Nat.
Commun. 4, 2067 (2013).

https://doi.org/10.1038/s41467-023-44281-0
the Laboratory Directed Research and Development program of Los
Alamos National Laboratory under project numbers 20230546DR (A.L.-B.)
and 20230049DR (A.S.). A.L.B., C.N., and A.S. work was carried out under
the auspices of the U.S. DOE through Los Alamos National Laboratory,
operated by Triad National Security, LLC (Contract No.
892333218NCA000001).

Author contributions
A.L.B. and A.D.K. conducted the experiments on the D-Wave chip. C.N.
provided a theoretical explanation of the phases and proposed the
nonmonotonic transverse correlation that A.L.B. experimentally veriﬁed.
A.S. proposed investigating frustrated deformed kagome lattices. A.L.B.,
C.N., and A.D.K. wrote the manuscript. All co-authors contributed to the
ﬁnal version of the manuscript.

Competing interests
The authors declare no competing interests.

Additional information
Supplementary information The online version contains
supplementary material available at
https://doi.org/10.1038/s41467-023-44281-0.
Correspondence and requests for materials should be addressed to
Alejandro Lopez-Bezanilla.
Peer review information Nature Communications thanks Huo Chen, and
the other, anonymous, reviewer for their contribution to the peer review
of this work. A peer review ﬁle is available.
Reprints and permissions information is available at
http://www.nature.com/reprints
Publisher’s note Springer Nature remains neutral with regard to jurisdictional claims in published maps and institutional afﬁliations.
Open Access This article is licensed under a Creative Commons
Attribution 4.0 International License, which permits use, sharing,
adaptation, distribution and reproduction in any medium or format, as
long as you give appropriate credit to the original author(s) and the
source, provide a link to the Creative Commons license, and indicate if
changes were made. The images or other third party material in this
article are included in the article’s Creative Commons license, unless
indicated otherwise in a credit line to the material. If material is not
included in the article’s Creative Commons license and your intended
use is not permitted by statutory regulation or exceeds the permitted
use, you will need to obtain permission directly from the copyright
holder. To view a copy of this license, visit http://creativecommons.org/
licenses/by/4.0/.

Acknowledgements
The authors acknowledge the contributions of the technical staff at
D-Wave Quantum. The research presented in this paper was supported by

Nature Communications | (2024)15:589

© The Author(s) 2024

7
