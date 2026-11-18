Source: see manifest row of the PDF
PDF sha256: 9c377977871d739f45c435e937b3e44aac2b98dbae0c10b41000af57d672a5e4
License: CC-BY-4.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of oppenheim_2023_gravitationally_induced_decoherence_vs_space_time_diffusion_testing_the_quantum_nature_of_gravity.pdf

Transcription of `oppenheim_2023_gravitationally_induced_decoherence_vs_space_time_diffusion_testing_the_quantum_nature_of_gravity.pdf` in this directory, 24 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-24 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Article

https://doi.org/10.1038/s41467-023-43348-2

Gravitationally induced decoherence vs
space-time diffusion: testing the quantum
nature of gravity
Received: 12 July 2023

Check for updates

1234567890():,;

1234567890():,;

Accepted: 8 November 2023

Jonathan Oppenheim 1
Zachary Weller-Davies1,3

, Carlo Sparaciari

, Barbara Šoda

1

1,2,3

&

We consider two interacting systems when one is treated classically while the
other system remains quantum. Consistent dynamics of this coupling has been
shown to exist, and explored in the context of treating space-time classically.
Here, we prove that any such hybrid dynamics necessarily results in decoherence of the quantum system, and a breakdown in predictability in the
classical phase space. We further prove that a trade-off between the rate of this
decoherence and the degree of diffusion induced in the classical system is a
general feature of all classical quantum dynamics; long coherence times
require strong diffusion in phase-space relative to the strength of the coupling.
Applying the trade-off relation to gravity, we ﬁnd a relationship between the
strength of gravitationally-induced decoherence versus diffusion of the metric
and its conjugate momenta. This provides an experimental signature of theories in which gravity is fundamentally classical. Bounds on decoherence rates
arising from current interferometry experiments, combined with precision
measurements of mass, place signiﬁcant restrictions on theories where Einstein’s classical theory of gravity interacts with quantum matter. We ﬁnd that
part of the parameter space of such theories are already squeezed out, and
provide ﬁgures of merit which can be used in future mass measurements and
interference experiments.

When considering the dynamics of composite quantum systems, there
are many regimes where one system can be taken to be classical and
the other quantum-mechanical. For example, in quantum thermodynamics, we often have a quantum system interacting with a large
thermal reservoir that can be treated classically, whilst in atomic
physics it is common to consider the behaviour of quantum atoms in
the presence of classical electromagnetic ﬁelds. Things become more
complicated when one considers classical-quantum (CQ) dynamics
where the quantum system back-reacts on the classical system. This is
particularly relevant in gravity because we would like to study the
back-reaction of thermal radiation being emitted from black holes in
space–time, and while the matter ﬁelds can be described by quantum

ﬁeld theory, we only know how to treat space–time classically. Likewise
in cosmology, vacuum ﬂuctuations are a quantum effect that we
believe seeds galaxy formation, while the expanding space–time
they live on can only be treated classically. In addition to the need for
an effective theory that treats space–time in the classical limit, there
has long been a debate about whether one should quantise gravity1–12.
The prevailing view has been that a quantum–classical coupling is
inconsistent. Many proposals for such dynamics13,14 are not completely
positive (CP), meaning they are at best an approximation and fail
outside a regime of validity15,16. A map Λ is completely positive (CP), iff
1  Λ is positive. This is the required condition used to derive the GKSL
equation. If it is violated, the dynamics acting on half of an entangled

1

Department of Physics and Astronomy, University College London, Gower Street, London WC1E 6BT, UK. 2Department of Physics, University of Waterloo,
e-mail: j.oppenheim@ucl.ac.uk
Waterloo, ON, Canada. 3Perimeter Institute for Theoretical Physics, Waterloo, ON, Canada.

Nature Communications | (2023)14:7910

1

## PDF page 2

Article
state, give negative probabilities. The semi-classical Einstein’s
equation17–19, which replaces the quantum operator corresponding to
the stress-energy tensor by its expectation value, is another attempt to
treat the classical limit from an effective point of view, but it is nonlinear in the state, leading to pathological behaviour if quantum ﬂuctuations are of comparable magnitude to the stress-energy tensor20.
This is often the precise regime we would like to understand.
However, examples of classical–quantum dynamics such as those
ﬁrst introduced in refs. 21,22 and studied in refs. 11,23–27 do not suffer
from such problems and are consistent. More generally, the master
equation shown in Eq. (4)11, is linear in the state space, preserves the
division of classical degrees of freedom and quantum ones, and is
completely positive (CP), and preserves normalisation. This ensures
that probabilities of measurement outcomes remain positive and
always add to 1. The dynamics is related to the GKSL or Lindblad
equation28,29, which for bounded generators of the dynamics, is the
most general Markovian dynamics for an open quantum system.
More precisely, we consider dynamics which is autonomous, meaning
the couplings in the theory do not depend on time. Likewise, Eq. (4) is
the most general Markovian classical–quantum dynamics with bounded generators11,30. Sub-classes of this master equation, along with
measurement and feedback approaches, have been discussed in the
context of Newtonian models of gravity24,25,31–35 and further developed
into a spatially covariant framework so that Einstein gravity in the ADM
formalism36 emerges as a limiting case11,37. Dynamics which is manifestly diffeomorphism invariant has also been introduced using path
integral methods38,39.
In this work, we move away from speciﬁc realisations of CQ
dynamics, in order to discuss their common features and the experimental signatures that follow from this. An early precursor to the
discussion here is the insight of Diósi22, who added classical noise and
quantum decoherence to the master equation of ref. 13, and found
the noise and decoherence trade-off required for the dynamics to
become completely positive. Here we prove that the phenomena
found in refs. 11,22,26 are generic features of all CQ dynamics;
the classical–quantum interaction necessarily induces decoherence on
the quantum system, and there is a generic trade-off between the
rate of decoherence and the amount of diffusion in the classical phase
space. The stronger the interaction between the quantum system and
the classical one, the greater the trade-off. One cannot have quantum
systems with long-coherence times without inducing a lot of diffusion
in the classical system. One can also generalise this result to a trade-off
between the rate of diffusion and the strength of more general
couplings to Lindblad operators, with decoherence being a
special case.

Results
Our main result is expressed as Eqs. (26) and (23), which bounds
the product of diffusion coefﬁcients and Lindblad coupling constants
in terms of the strength of the CQ-interaction. It is precisely this
trade-off which allows the theories considered here, to evade the
no-go arguments of Feynmann1,2, Aharonov3, Eppley and Hannah4
and others1,7–9,15,16,40–48. The essence of arguments against
quantum–classical interactions is that they would prohibit superpositions of quantum systems that source a classical ﬁeld. Since different classical ﬁelds are perfectly distinguishable in principle, if
the classical ﬁeld is in a distinct state for each quantum state in the
superposition, the classical ﬁeld could always be used to determine the
state of the quantum system, causing it to decohere instantly. By
satisfying the trade-off, the quantum system preserves coherence
because diffusion of the classical degrees of freedom means that the
state of the classical ﬁeld does not determine the state of the quantum
system11,25. Equation (26) and other variants we derive, quantify the
amount of diffusion required to preserve any amount of coherence. If
space–time curvature is treated classically, then complete positivity of

Nature Communications | (2023)14:7910

https://doi.org/10.1038/s41467-023-43348-2

the dynamics means its interaction with quantum ﬁelds necessarily
results in unpredictability and gravitationally induced decoherence.
This trade-off between the decoherence rate and diffusion provides an experimental signature, not only of models of hybrid Newtonian dynamics such as refs. 24,33 or post-quantum theories of
general relativity such as refs. 11,39 but of any theory which treats
gravity as being fundamentally classical. The metric and their conjugate momenta necessarily diffuse away from what Einstein’s general
relativity predicts. This experimental signature squeezes
classical–quantum theories of gravity from both sides: if one has
shorter decoherence times for superpositions of different mass distributions, one necessarily has more diffusion of the metric and conjugate momenta. In the “Methods” subsection “Detecting gravitational
diffusion” we show that the latter effect causes imprecision in measurements of mass such as those undertaken in the Cavendish
experiment49–51 or in measurements of Newton’s constant “Big G"52–54.
The precision at which a mass can be measured in a short time, thus
provides an upper bound on the amount of gravitational diffusion, as
quantiﬁed by Eq. (42). In the other direction, decoherence experiments
place a lower bound on the diffusion. Our estimates suggest that
experimental lower bounds on the coherence time of large
molecules55–60, combined with gravitational experiments measuring
the acceleration of small masses61–63, already place strong restrictions
on theories where space–time is not quantised. In the section
“Physical constraints on the classicality of gravity” we show that several
realisations of CQ-gravity are already ruled out, while other realisations
produce enough diffusion away from general relativity to be detectable by future table-top experiments. Although the absence of such
deviations from general relativity would not be as direct a conﬁrmation
of the quantum nature of gravity, such as experiments proposed in
refs. 64–74 to exhibit entanglement or coherence generated by gravitons, it would effectively rule out any sensible theory that treats
space–time classically. While conﬁrmation of gravitational diffusion
would suggest that space-time is fundamentally classical. Experiments
to detect or bind gravitational diffusion also provide immediate-term
prospects for probing the quantumness of gravity, while
entanglement-based experiments will only be feasible in the long term.
The outline of the remainder of this paper is as follows. In the
subsection “Classical-quantum dynamics” we review the general form
of the CQ master equation of classical–quantum systems as derived in
refs. 11,30. The CQ-map can be represented in a manner akin to the
Kraus representation75 for quantum maps, with conditions for it to be
completely positive and trace preserving (CPTP). We can perform a
short time moment expansion of the CQ-map taking states at some
initial time, to states at a later time. This gives us the CQ version of the
Kramers–Moyal expansion76,77, presented in the subsection “The CQ
Kramers–Moyal expansion”. The physical meaning of the moments is
given in the subsection “Physical interpretation of the moments”. Our
main result is presented in the section “A trade-off between decoherence and diffusion”, where we show that there is a general trade-off
between decoherence of the quantum system and diffusion in the
classical system. We generalise the trade-off to the case of ﬁelds in the
subsection “Trade-off in the presence of ﬁelds” and in the subsection
“Physical constraints on the classicality of gravity”, we apply the
inequality in the gravitational setting. The positivity constraints mean
that the considerations do not depend on the speciﬁcs of the theory,
only that it treats gravity classically, and is time-local. This allows us to
discuss some of the observational implications of this result and we
comment on the relevant ﬁgures of merit required in interference and
precision mass measurements in order to constrain theories of gravity,
as they are not always readily available in published reports. In addition
to table-top constraints, we consider those due to cosmological
observations. We then conclude with a discussion of our results. The
“Methods” section collects or previews a number of technical results.
Since this paper appeared on the arXiv, we have found that when the
2

## PDF page 3

Article

https://doi.org/10.1038/s41467-023-43348-2

decoherence-diffusion trade-off is saturated, there are two important
consequences. The ﬁrst is that in the continuous class of dynamics, the
quantum state remains pure, conditioned on the classical trajectory78.
The second is that in the path integral formulation, one can show that
the dynamics are completely positive from the path integral alone39.
For a generic path integral of Feynman–Vernon form79, one typically
only knows that the dynamics are completely positive if it was derived
from a CPTP master equation.

Classical–quantum dynamics
Let us ﬁrst review the general map and master equation governing
classical–quantum dynamics. The classical degrees of freedom are
described by a differential manifold M and we shall generically denote
elements of the classical space by z. For example, we could take the
classical degrees of freedom to be position and momenta in which case
M = R2 and z = (q, p). The quantum degrees of freedom are described
by a Hilbert space H. Given the Hilbert space, we denote the set of
positive semi-deﬁnite operators with trace at most unity as S ≤ 1 ðHÞ.
Then the CQ object deﬁning the state of the CQ system at a given time
is a map ϱ : M ! S ≤ 1 ðHÞ subject to a normalisation constraint
R
M dzTrH ½ϱ = 1. To put it differently, we associate to each classical
degree of freedom an un-normalised density operator, ϱ(z), such that
distribution over the clasTrH ½ϱ = pðzÞ ≥ 0 is a normalised probability
R
sical degrees of freedom and M dzϱðzÞ is a normalised density
operator on H. An example of such a CQ-state is the CQ qubit depicted
as a 2 × 2 matrix over phase space26. More generally, we can deﬁne any
CQ operator f(z) which lives in the ﬁbre bundle with base space M and
ﬁbre H.
Just as the Lindblad equation is the most general evolution law
that maps density matrices to density matrices, we can ask what is the
most general evolution law that preserves the quantum-classical statespace. Any such dynamics, if it is to preserve probabilities, must be
completely positive, norm-preserving, and linear in the CQ-state. That
dynamics must be linear can be seen as follows: if someone prepares a
system in one of two states σ0 or σ1 depending on the value of a coin
toss (j0ih0j with probability p,j1ih1j with probability 1−p), then the
evolution L of the system must satisfy pj0ih0j  Lσ 0 + ð1  pÞj1ih1j 
Lσ 1 = Lð pσ 0 + ð1  pÞσ 1 Þ otherwise the system evolves differently
depending on whether we are aware of the value of the coin toss. A
violation of linearity further implies that when the system is in state σ0
it evolves differently depending on what state the system would have
been prepared in, had the coin been j1ih1j instead of j0ih0j. This
motivates our restriction to linear theories. We will also require the
map to be Markovian on the combined classical–quantum system,
which is equivalent to requiring that there is no hidden system that
acts as a memory. This is natural if the interaction is taken to be fundamental, but is the assumption that one might want to remove if one
thinks of the hybrid theory as an effective description. We thus take
these as the minimal requirements that any fundamental
classical–quantum theory must satisfy if it is to be consistent.
The most general CQ-dynamics, which maps CQ states onto
themselves can be written in the form11
Z
ϱðz, t + δtÞ =

dz 0

X
μν

Λμν ðzjz 0 , δtÞLμ ϱðz 0 , tÞLyν

ð1Þ

where the Lμ is an orthogonal basis of operators and Λμν ðzjz 0 , δtÞ is
positive semi-deﬁnite for each z, z 0 . Henceforth, we will adopt
the Einstein summation convention so that we can drop ∑μν with the
understanding that equal upper and lower indices are presumed to be
summed over. The normalisation of probabilities requires
Z

dzΛμν ðzjz 0 , δtÞLyν Lμ = I:

Nature Communications | (2023)14:7910

ð2Þ

The choice of basis Lμ is arbitrary, although there may be one
which allows for unique trajectories26. Equation (1) can be viewed as a
generalisation of the Kraus decomposition theorem.
In the case where the classical degrees of freedom are taken to be
discrete, Poulin25 used the diagonal form of this map to derive the most
general form of Markovian master equation for bounded operators,
which is the one introduced in ref. 21. When the classical degrees of
freedom are taken to live in a continuous conﬁguration space, we need
to be a little more careful, since ϱ(z) may only be deﬁned in a distributional sense; for example, ϱðzÞ = δðz, zÞϱðzÞ. In this case (1) is
μ
completely positive if the eigenvalues of Λμν ðzjz 0 , δtÞ, λ ðzjz 0 , δtÞ, are
R
0
0 μ
0
positive so that dzdz P μ ðz, z Þλ ðzjz , δtÞ ≥ 0 for any vector with
positive components P μ ðz, z 0 Þ30. One can derive the CQ master equation by performing a short time expansion of Eq. (1) in the case when
the Lμ is bounded11. To do so, we ﬁrst introduce an arbitrary basis of
traceless Lindblad operators on the Hilbert space, Lμ = {I, Lα}. Now, at
δt = 0, we know Eq. (1) is the identity map, which tells us that
Λ00 ðzjz 0 , δt = 0Þ = δðz, z 0 Þ. Looking at the short-time expansion coefﬁcients, by Taylor expanding in δt ≪ 1, we can write
μ

ν

Λμν ðzjz 0 , δtÞ = δ 0 δ 0 δðz, z 0 Þ + W μν ðzjz 0 Þδt + Oðδt 2 Þ:

ð3Þ

By substituting the short-time expansion coefﬁcients into Eq. (1)
and taking the limit δt → 0 we can write the master equation in the form
∂ϱðz, tÞ
=
∂t

Z

1
dz 0 W μν ðzjz 0 ÞLμ ϱðz 0 ÞLyν  W μν ðzÞfLyν Lμ , ϱg + ,
2

ð4Þ

where {, }+ is the anti-commutator, and preservation of normalisation
under the trace and ∫ dz deﬁnes
W μν ðzÞ =

Z

dz 0 W μν ðz 0 jzÞ:

ð5Þ

We see the CQ master equation is a natural generalisation of the
Lindblad equation and classical rate equation in the case of
classical–quantum coupling. We give a more precise interpretation of
the different terms arising when we perform the Kramers–Moyal
expansion of the master equation at the end of the section. The positivity conditions from Eq. (1) transfer to positivity conditions on the
master equation via (3). We can write the positivity conditions in an
illuminating form by writing the short time expansion of the transition
amplitude Λμν ðzjz 0 , δtÞ, as deﬁned by Eq. (3), in block form
"
μν

0

Λ ðzjz , δtÞ =

δðz, z 0 Þ + δtW 00 ðzjz 0 Þ

δtW 0β ðzjz 0 Þ

δtW α0 ðzjz 0 Þ

δtW αβ ðzjz 0 Þ

#
+ Oðδt 2 Þ

ð6Þ

and the dynamics will be positive if and only if Λμν ðzjz 0 , δtÞ is a positive
matrix. It is possible to introduce an arbitrary set of Lindblad operators
 and appropriately redeﬁne the couplings W μν ðzjz 0 Þ in Eq. (4)11. For
L
μ
most purposes, we shall work with a set of Lindblad operators that
includes the identity Lμ = (I, Lα); this is sufﬁcient since any CQ master
equation is completely positive if and only if it can be brought to the
form in Eq. (4), where the matrix (6) is positive.

The CQ Kramers–Moyal expansion
In order to study the positivity conditions it is ﬁrst useful to perform a
moment expansion of the dynamics in a classical-quantum version of
the Kramers–Moyal expansion as in ref. 11. In classical Markovian
dynamics, the Kramers–Moyal expansion relates the master equation
to the moments of the probability transition amplitude and proves to
be useful for a multitude of reasons. Firstly, the moments are related to
observable quantities; for example, the ﬁrst and second moments of
the probability transition amplitude characterise the amount of drift

3

## PDF page 4

Article

https://doi.org/10.1038/s41467-023-43348-2

and diffusion in the system. This is reviewed in the subsection “Physical
interpretation of the moments”. Secondly, the positivity conditions on
the master equation transfer naturally to positivity conditions on the
moments, which we can then relate to observable quantities. In the
classical–quantum case, we shall perform a short time moment
expansion of the transition amplitude Λμν ðzjz 0 , δtÞ and then show that
the master equation can be written in terms of these moments. We
then relate the moments to observational quantities, such as the
decoherence of the quantum system and the diffusion in the classical
system.
We work with the form of the dynamics in Eq. (4), using an arbitrary orthogonal basis of Lindblad operators Lμ = fI, Lα g. We take the
classical degrees of freedom M to be d dimensional, z = (z1, …zd), and
we label the components as zi, i ∈ {1, …d}. We begin by introducing the
moments of the transition amplitude W μν ðzjz 0 Þ appearing in the CQ
master Eq. (3)
Dn,μνi ...i ðz 0 Þ:¼
1

n

1
n!

Z

dzW μν ðzjz 0 Þðz  z 0 Þi1 . . . ðz  z 0 Þin :

ð7Þ

The subscripts ij ∈ {1, …d } label the different components of the
vectors ðz  z 0 Þ. For example, in the case where d = 2 and the classical
degrees of freedom are position and momenta of a particle,
then
we
have
z = (z1, z2) = (q, p),
ðz  z 0 Þ = ðz 1  z 01 , z 2  z 02 Þ = ðq  q0 , p  p0 Þ. The components are then
0
given by ðz  z 0 Þ1 = ðq  q0 Þ and ðz  z 0 Þ2 = ðp  p0 Þ. M μν
n, i1 ...in ðz , δtÞ is
seen to be an nth rank tensor with dn components.
In terms of the components Dn,μνi ...i the short time expansion of
1
n
the transition amplitude Λμν ðzjz 0 Þ is given by30
Λμν ðzjz 0 , δtÞ = δ μ0 δ ν0 δðz, z 0 Þ + δt

1
X
n=0

0
Dμν
n, i ...i ðz Þ
1

n

∂n
∂z 0i . . . ∂z 0i
1

!
δðz, z 0 Þ + Oðδt 2 Þ,
n

ð8Þ
and the master equation takes the form11

determines the diffusion of the classical degrees of freedom. For this
discussion, we shall take the classical degrees of freedom to live in a
phase space Γ = ðM, ωÞ, where ω is the symplectic form.
Consider R the expectation value of any CQ operator
OðzÞ, hOðzÞi :¼ dzTr½OðzÞϱ which does not have an explicit time
dependence. Its evolution law can be determined via Eq. (9)
dhOi
=
dt


 Z
∂ϱ
dzTr OðzÞ
=
dzTrϱ
∂t

Z


1 αβ
y
y
i½OðzÞ, HðzÞ + Dαβ
0 ðzÞLβ OðzÞLα  D0 ðzÞfLα Lβ , OðzÞg + ð10Þ
2
!
#
1


X μν
∂n
Lyν Lμ Oðz, tÞ ,
Dn, i ...i ðzÞ
+
1
n
∂z i1 . . . ∂z in
n=1

where we have used cyclicity of trace and integration by parts, to bring
the equation of motion into a form that would enable us to write a CQ
version of the Heisenberg representation11 for a CQ operator. If we are
interested in the expectation value of phase space variables OðzÞ = z i I
then Eq. (10) gives
dhz i i
=
dt

0μ y
HðzÞ = 2i ðDμ0
0 Lμ  D0 Lμ Þ

where we deﬁne the Hermitian operator
0μ*
(which is Hermitian since Dμ0
0 = D0 ). We see the ﬁrst line of Eq. (9)
describes purely classical dynamics, and is fully described by the
moments of the identity component of the dynamics Λ00 ðzjz 0 Þ. The
second line describes pure quantum Lindbladian evolution described
by the zeroth moments of the components Λα0 ðzjz 0 Þ, Λαβ ðzjz 0 Þ; speciﬁcally the (block) off diagonals, Dα0
0 ðzÞ, describe the pure Hamiltonian
evolution, whilst the components Dαβ
0 ðzÞ describe the dissipative part
of the pure quantum evolution. Note that the Hamiltonian and Lindblad couplings can depend on the classical degrees of freedom so the
second line describes the action of the classical system on the quantum one. The third line contains the non-trivial classical-quantum backreaction, where changes in the distribution over phase space are
induced and can be accompanied by changes in the quantum state.

h
i
y
dzDμν
1, i Tr Lν Lμ ϱðz, tÞ

ð11Þ

P
y
with all higher order terms vanishing, and we see that μν≠00 Dμν
1, i hLν Lμ i
governs the average rate at which the quantum system moves the
classical system through phase space, and with the back-reaction is
br αμ
quantiﬁed by the Hermitian matrix Dαμ
1 :¼ ðD1 Þ . The force of this
back-reaction is especially apparent if the equations of motion are
Hamiltonian in the classical limit as in ref. 11. I.e. if we deﬁne
αβ
αβ
j
with ω the symplectic form
H I ðzÞ :¼ h Lyβ Lα and take Dαβ
1, i = ωi d j h
and dj the exterior derivative. Then Eq. (11) is analogous to Hamilton’s
equations, and the CQ evolution equation after tracing out the
quantum system has the form of a Liouville’s equation to ﬁrst order
and in the classical limit,

!
1


∂ϱðz, tÞ X
∂n
n
=
D00
ð1Þ
n, i1 ...in ðzÞϱðz, tÞ
∂t
∂z i1 . . . ∂z in
n=1
1 αβ
y
y
ð9Þ
 i½HðzÞ, ϱðzÞ + Dαβ
0 ðzÞLα ϱðzÞLβ  D0 ðzÞfLβ Lα , ϱðzÞg +
2
!
n
1


X X
∂
y
Dμν
+
ð1Þn
n, i1 ...in ðzÞLμ ϱðz, tÞLν ,
∂z
.
i1 . . ∂z in
μν≠00 n = 1

Z



∂ρðz, tÞ
= fH c , ρðz, tÞg + tr fH I ðzÞ, ϱðzÞg + . . .
∂t

ð12Þ

with ρðzÞ :¼ Tr½ϱðzÞ.
The signiﬁcance of the second moment is also seen via Eq. (10) to
be related to the variance of phase space variables
σ z i z i :¼ hz i1 z i2 i  hz i1 ihz i2 i
1

2

dσ 2z i , z i
1

dt

2

αβ
αβ
y
y
y
= 2hDαβ
2, i , i Lβ Lα i + hz 2 D1, z i Lβ Lα i  hz i2 ihD1, z i Lβ Lα i
1

2

1

1

ð13Þ

αβ
y
y
+ hz i1 Dαβ
1, z i Lβ Lα i  hz i1 ihD1, z i Lβ Lα i:
2

2

In the case when D1, z i is uncorrelated with z i2 and D1, z i uncor1
2
related with z i1 , then the growth of the variance only depends on the
diffusion coefﬁcient.
The zeroth moment Dαβ
0 is just the pure Lindbladian couplings.
The simplest example is the case of a pure decoherence process with a
single Hermitian Lindblad operator L and decoherence coupling D0.
Then we can deﬁne a basis fjaig via the eigenvectors of L and
 
∂ϱ
1
2
a b =  i aj ½HðzÞ, ϱ jb  D0 ðLðaÞ  LðbÞÞ hajϱjbi,
∂t
2

ð14Þ

Physical interpretation of the moments
Let us now brieﬂy review the physical interpretation of the moments
that will appear in our trade-off relation. In particular, the zeroth
moment determines the rate of decoherence (and Lindbladian coupling more generally), the ﬁrst moment gives the force exerted by the
quantum system on the classical system, and the second moment

Nature Communications | (2023)14:7910

and we see that the matrix
elements of ϱ which quantify coherence

between the states jai, b decay exponentially fast with a decay rate of
D0(L(a)−L(b))2. For a damping/pumping process of a quantum harmonic oscillator with Hamiltonian H = ωa†a, L↓ = a, L↑ = a†, a the crea##
tion operator, and D""
0 , D0 the non-zero couplings, then standard
4

## PDF page 5

Article

https://doi.org/10.1038/s41467-023-43348-2

calculations26,80 show that an initial superposition p1ﬃﬃ2 jn + mi with n, m
large and n ≫ m will initially decohere at a rate of approximately
##
ðD""
0 + D0 Þðm + nÞ=2, and the state will eventually thermalise to a
""
temperature of ω= logðD##
0 =D0 Þ. So in this case, the Lindblad
couplings not only determine the rate of decoherence but also the
rate at which energy is pumped into the harmonic oscillator. In the
next section, we will derive the trade-off between Lindblad couplings
and the diffusion coefﬁcients. Although we will sometimes refer to this
as a trade-off between decoherence and diffusion, this terminology
is only strictly appropriate for pure decoherence processes, while
more generally, it is a trade-off between Lindblad couplings and
diffusion coefﬁcients.

 jj > 0, meaning
quantum system complete positivity demands that jjO
2
the Cauchy-Schwartz inequality in Equation (18) must hold. To reach
this conclusion one can insert the CQ state into the CQ
Cauchy–Schwartz inequality and repeat the proof of the Pawula
theorem30, which must now hold once averaged over the state. By
using the short-time moment expansion of Λμν ðzjz 0 Þ deﬁned in Eq. (8)
and using integration by parts, we then arrive at the observational
trade-off between decoherence and diffusion

A trade-off between decoherence and diffusion

which must hold for any positive CQ state ϱ(z). Stripping out the bi
vectors, (19) is equivalent to the matrix positivity condition

In this section, we present our main result by using positivity conditions to prove the trade-off between decoherence and diffusion seen in
models such as those of refs. 11,22,26 are in fact a general feature of all
classical-quantum interactions. We shall also generalise this, and
derive a trade-off between diffusion and arbitrary Lindbladian coupling strengths. The trade-off is in relation to the strength of the
dynamics and is captured by Eqs. (20), (23) and (26). In the subsection
“Trade off in the presence of ﬁelds” we extend the trade-off to the case
where the classical and quantum degrees of freedom can be ﬁelds and
use this to show that treating the metric as being classical necessarily
results in diffusion of the gravitational ﬁeld.
There are two separate possible sources for the force (or drift) of
the back-reaction of the quantum system on phase space—it can be
sourced by either the D0α
1, i components or the Lindbladian components
Dαβ
1, i . We shall deal with both sources simultaneously by considering a
CQ Cauchy-Schwartz inequality which arises from the positivity of
Z
Tr


dzdz 0 Λμν ðzjz 0 ÞOμ ðz, z 0 Þρðz 0 ÞOyν ðz, z 0 Þ ≥ 0

ð15Þ

for any vector of CQ operators Oμ. One can verify that this must be
positive directly from the positivity conditions on Λμν ðzjz 0 Þ and we go
through the details in the Appendix section “Positivity conditions and
the trade-off between decoherence and diffusion”. A common choice
for Oμ would be the set of operators Lμ = fI, Lα g appearing in the master
equation.
The inequality in Eq. (15) turns out to be especially useful since it
can be used to deﬁne a (pseudo) inner product on a vector of operators with components Oμ via
O2 i =
h
O1 , 

Z

h
i
dzdz 0 Tr Λμν ðzjz 0 ÞO1μ ϱðz 0 ÞOy2ν

ð16Þ

pﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ
where jj 
Ojj = h 
O, 
Oi ≥ 0 due to Eq. (15). Technically this is not positive
deﬁnite, but this shall not be important for our purpose. Taking the
 jj2 O  hO
 ,O
 iO for vectors O1μ, O2μ, posicombination Oμ = jjO
2
1μ
1
2
2μ
tivity of the norm gives


  hO
 jj2 O
 ,O
 iO
 jj2
 2 = jj jjO
jjOjj
2
1
1
2
2


 jj2  jh 
= jj 
O jj2 jj 
O jj2 jjO
O,
O ij2 ≥ 0,
2

1

2

1

ð17Þ

2

 jj ≠ 0 we have a Cauchy–Schwartz inequality
and as long as jjO
2
2
 jj2  jhO
 ,
jj 
O1 jj2 jjO
2
1 O2 ij ≥ 0:

ð18Þ

We can use Eq. (18) to get a trade-off between the observed difi
α
fusion and decoherence by picking O2μ = δ μ Lα and O1μ = b ðz  z 0 Þi Lμ ,
where Lμ = fI, Lα g are the Lindblad operators appearing in the master
i
of an arbitrary vector. In this case
equation
i
R and bh are the components
 jj = dzTr Dαβ L ϱLy and one can verify using CQ Pawula
jjO
2
0 α
β
theorem30 that in order to have non-trivial back-reaction on the

Nature Communications | (2023)14:7910

Z

h
iZ
h
i Z
h
i2
i*
j
αβ
y
y
 dzTr bi Dμα L ϱðzÞLy  ,
≥
b
L
ϱðzÞL
L
ϱðzÞL
dzTr 2b Dμν
dzTr
D
μ
ν
α 
0 α

2, ij
1, i μ
β

ð19Þ

y

br
0  2hD2 ihD0 i  hDbr
1 ihD1 i ,

8ϱðzÞ,

ð20Þ

where we deﬁne
Z
hD0 i =
hD2 iij =

Z

Z
h
i
h
i
y
br
y
dzTr Dαβ
dzTr Dμα
0 Lα ϱðzÞLβ , hD1 ii =
1, i Lμ ϱðzÞLα ,
h
i
y
dzTr Dμν
2, ij Lμ ϱðzÞLν :

ð21Þ

Since Eq. (20) holds for all states, the tightest bound is provided
by the inﬁmum over all states
y

br
0  inf f2hD2 ihD0 i  hDbr
1 ihD1 i g:
ϱðzÞ

ð22Þ

The quantities 〈D2〉 and 〈D0〉 appearing in Eq. (20) are related to
observational quantities. In particular 〈D2〉 is the expectation value of
the amount of classical diffusion which is observed and 〈D0〉 is related
to the amount of decoherence on the quantum system. The expectation value of the back-reaction matrix hDbr
1 i quantiﬁes the amount of
back-reaction on the classical system. In the trivial case Dbr
1 = 0, Eq. (20)
places little restriction on the diffusion and Lindbladian rates appearing on the left-hand side. We already knew from refs. 28,29 that the Dαβ
0
must be a positive semi-deﬁnite matrix, and we also know that diffusion coefﬁcients must be positive semi-deﬁnite. However, in the nontrivial case, the larger the back-reaction exerted by the quantum system, the stronger the trade-off between the diffusion coefﬁcients and
Lindbladian coupling. Equation (20) gives a general trade-off between
observed diffusion and Lindbladian rates, but we can also ﬁnd a tradeoff in terms of a theory’s coupling coefﬁcients alone. We show in the
Appendix section “General trade-off between decoherence and diffusion coefﬁcients” that the general matrix trade-off
1 bry
 2D2
Dbr
1 D0 D1

ð23Þ

αμ
αβ
holds for the matrix whose elements are the couplings Dμν
2, ij , D1, i , D0
br
for any CQ dynamics. Moreover, ðI  D0 D1
ÞD
=
0,
which
tells
us
that
0
1
D0 cannot vanish if there is non-zero back-reaction. Equation (23)
quantiﬁes the required amount of decoherence and diffusion in order
for the dynamics to be completely positive. In Eq. (23), and
αβ
αβ
throughout, D1
0 is the generalised inverse of D0 , since D0 is only
required to be positive semi-deﬁnite. In the special case of a single
Lindblad operator α = 1 and classical degree of freedom, and when the
00
0
only non-zero couplings are D11
0 :¼ D0 , D2, pp :¼ 2D2 and D1, q = 1 this
trade-off reduces to the condition D2D0 ≥ 1 used in ref. 22.
As a more general example, let us consider the class of theories
that are continuous in phase space, and whose back-reaction is gen^ ðmÞ which is only a
erated by a classical-quantum Hamiltonian H

5

## PDF page 6

Article

https://doi.org/10.1038/s41467-023-43348-2

function of the canonical coordinates qi30. These are given by
o
h ðmÞ i 1 n ðmÞ o 1 n
∂ϱ
^ ðmÞ
^ ,ϱ 
^ ,ϱ +
= fH c , ϱg  i H
ϱ, H
H
∂t
2
2
" ðmÞ "
##
^
^ ðmÞ
1
∂
H
∂H
i
j
, ϱ,
+ fp , fp , D2, ij ϱgg + D0, ij
2
∂qi
∂qj

classicality of the two systems can be written11
Z
ρðz, tÞ =

X Z
μν≠00

h
i
y
dzTr Dμν
1, i Lμ ϱðzÞLν :

ð25Þ

It follows directly from Eq. (20) that when the back-reaction is
αβ
sourced by either D0μ
1, i or D1, i we can arrive at the observational tradeoff in terms of the total drift
y

0  8hD2 ihD0 i  hDT1 ihDT1 i ,

8ϱðzÞ,

ð26Þ

where the quantities appearing in Eq. (26) are now all observational
quantities, related to drift, decoherence and diffusion as outlined in
the previous subsection “Physical interpretation of the moments”. We
believe that Eq. (26) should hold more generally, though we don’t have
a general proof.
In the case where the back-reaction is Hamiltonian at ﬁrst order in
the sense of Eq. (12), then Eq. (26) can be written as
∂H
ω  !I
∂z

∂H
ω  !I
∂z

y

 8hD2 ihD0 i,

8ϱðzÞ:

ð27Þ

As a result, we can derive a trade-off between diffusion and
decoherence for any theory that reproduces this classical limit and
treats one of the systems classically.
To summarise, whenever the back-reaction of the quantum system on the classical system induces a force on the phase space, then we
have a trade-off between the amount of diffusion on the classical
system and the strength of decoherence on the quantum system (or
more precisely the strength of the Lindbladian couplings Dαβ
0 ). This can
be expressed both as a condition on the matrix of coupling coefﬁcients in the master equation, via Eq. (23) or in terms of observable
quantities using Eqs. (20) and (26). In the case when the back-reaction
is Hamiltonian, we further have Equation (27). We would like to apply
this trade-off to the case of gravity in the non-relativistic, Newtonian
limit. In order to do so, we will need to generalise the trade-off to the
case of quantum ﬁelds interacting with classical ones, which we do in
the subsection “Trade-off in the presence of ﬁelds”. The goal will be to
understand the implications of treating the metric (or Newtonian
potential) as being classical by using the trade-off when the quantum
back-reaction induces a force on the gravitational ﬁeld which, on
expectation, is the same as the weak ﬁeld limit of General Relativity.

Trade-off in the presence of ﬁelds
We would like to explore the trade-off in the gravitational setting and
explore the consequences of treating the gravitational ﬁeld as being
classical and matter quantum. Since gravity is a ﬁeld theory, we must
ﬁrst discuss classical-quantum master equations in the presence of
ﬁelds. In the ﬁeld-theoretic case, both the Lindblad operators and the
phase space degrees of freedom can have spatial dependence,
z(x), Lμ(x) and a general bounded CP map which preserves the
Nature Communications | (2023)14:7910

ð28Þ

ð24Þ

where Hc is the purely classical Hamiltonian, pj are the conjugate
momenta, and D0 and D2 are qi dependent matrices with elements D0,ij
and D2,ij. Then the trade-off (23) implies that they must obey the matrix
equation 2D2D0 ⪯ 1.
It is also useful to try to obtain an observational trade-off in terms
of the total drift due to back-reaction as calculated in Eq. (11)
hDT1 ii =

dz 0 dxdyΛμν ðzjz 0 , t; x, yÞLμ ðx, z, z 0 Þϱðz 0 , 0ÞLyν ðy, z, z 0 Þ,

where, as is usually the case with ﬁelds, in Eq. (28) it should be implicitly understood that a smearing procedure has been implemented.
We elaborate on some of the details when ﬁelds are introduced in the
Appendix section “Classical-quantum dynamics with ﬁelds”. The condition for Eq. (28) to be completely positive on all CQ states is that for
all vectors at x with components Aν ðy, z, z 0 Þ
Z

dzdxdyA*μ ðx, z, z 0 ÞΛμν ðzjz 0 ; x, yÞAν ðy, z, z 0 Þ ≥ 0

ð29Þ

meaning that Λμν(x, y) can be viewed as a positive matrix in μν and a
positive kernel in x, y. In the ﬁeld-theoretic case, one can still perform
a Kramers–Moyal expansion and ﬁnd a trade-off between the
coefﬁcients D0(x, y), D1(x, y), D2(x, y) appearing in the master equation.
The coefﬁcients now have an x, y dependence, due to the spatial
dependence of the Lindblad operators. The coefﬁcients
D1(x, y), D2(x, y) still have a natural interpretation as measuring the
amount of force (drift) and diffusion, whilst D0(x, y) describes the
purely quantum evolution on the system and can be related to
decoherence.
Using the positivity condition in Eq. (29) we ﬁnd the same trade of
between coupling constants in Eq. (23) but where now D2(x, y) is the
br
(p + 1)n × (p + 1)n matrix-kernel with elements Dμν
2, ij ðx, yÞ, D1 ðx, yÞ is the
(p + 1)n × p matrix-kernel with rows labelled by μi, columns labelled by
β, and elements Dμβ
1, i ðx, yÞ, and D0(x, y) is the p × p decoherence matrixkernel with elements Dαβ
0 ðx, yÞ. Here i ∈ {1, …, n}α ∈ {1, …, p} and
μ ∈ {1, …, p + 1}. In the ﬁeld-theoretic trade off we are treating the
objects in Eq. (23) as matrix-kernels, so that for any positionR
i
μ
j
dependent vector bμ ðxÞ, ðD2 bÞi ðxÞ = dyDμν
ν ðyÞ, whilst for any
2, ij ðx, yÞbR
position-dependent
vector
aβ ðxÞ, ðD0 aÞα ðxÞ = dyDαβ
0 ðx, yÞaβ ðyÞ.
Explicitly, we ﬁnd that positivity of the dynamics is equivalent to the
matrix condition
Z

"
*

*

dxdy½b ðxÞ, a ðxÞ

2D2 ðx, yÞ Dbr
1 ðx, yÞ
Dbr
1 ðx, yÞ

D0 ðx, yÞ

#

bðyÞ
aðyÞ


≥0

ð30Þ
i

which should be positive for any position-dependent vectors bμ ðxÞ and
aα(x). This is equivalent to trade-off between coupling constants in
Eq. (23) if we view (23) as a matrix-kernel equation.
In order for the theory to be diffeomorphism invariant, we expect
D0(x, y) and D2(x, y) to approach delta functions. We will not assume
this, but we shall assume that the drift back-reaction is local, so that
br
Dbr
1 ðx, yÞ = δðx, yÞD1 ðxÞ. As we shall see in the next section, this is a
natural assumption if we want to have back-reaction which is given by a
local Hamiltonian. However, one might not want to assume that the
form of the Hamiltonian remains unchanged to arbitrarily small distances. With this locality assumption, Eq. (30) gives rise to the same
trade-off of Eq. (23), where the trade-off is to be interpreted as a matrix
kernel inequality. Writing this out explicitly we have
Z

βν 0 i
1
0
dxdyai*ν ðxÞDμα
1, i ðxÞðD0 Þαβ ðx, yÞD1, j ðx Þaν ðx Þ ≤

Z

j
dxdy2ai*μ ðxÞDμν
2, ij ðx, yÞaν ðyÞ,

ð31Þ
where asking that this inequality holds for all vectors aiμ ðxÞ is equivalent to the matrix-kernel trade-off condition of Eq. (23).
We give two examples of master equations satisfying the coupling
constant trade-off in the Appendix section “Examples of Kernels
saturating the decoherence diffusion coupling constants trade-off”.
The decoherence-diffusion trade-off tells us how much diffusion and
6

## PDF page 7

Article

https://doi.org/10.1038/s41467-023-43348-2

stochasticity are required to maintain coherence when the quantum
system back-reacts on the classical one. If the interaction between the
classical and quantum degrees of freedom is dictated by unbounded
operators, such as the mass density, then there can exist states for
which the back-reaction can be made arbitrarily large. This is the case
for a quantum particle interacting with its Newtonian potential
through its mass density at arbitrarily short distances. Hence, if one
considers a particle in a superposition of two peaked mass densities,
then there can be an arbitrarily large response in the Newtonian
potential around those points, and either there must be an arbitrary
amount of diffusion, or the decoherence must occur arbitrarily fast.
The former is unphysical, while the latter turns out to be the case in
simple examples of theories such as those discussed in the Methods
subsection “Decoherence rates”.
Since our goal is to experimentally constrain classical-quantum
theories of gravity, we shall hereby ask that the map (28) is CP when
acting on all physical states ρ. If one allows for arbitrarily peaked mass
distributions then the coupling constant trade-off of Eq. (31) should be
satisﬁed. In the ﬁeld-theoretic case, we can similarly ﬁnd an observational trade-off, relating the expected value of the diffusion matrix
〈D2(x, y)〉 to the expected value of the drift in a physical state ϱ as we
did in subsection “A trade-off between decoherence and diffusion”.
This is done explicitly in the “Methods” subsection “Classical-quantum
dynamics with ﬁelds”, using a ﬁeld-theoretic version of the
Cauchy–Schwartz inequality given by Eq.n (73), we ﬁnd
Z
2hD2 ðx, xÞi

y

br
dx 0 dy0 hD0 ðx 0 , y0 ÞikhDbr
1 ðxÞihD1 ðxÞi ,

ð32Þ

where Eq. (34) is to be understood as a matrix inequality with entries
Z
hD0 ðx, yÞi =

h

i
y
dzTr Dαβ
0 Lα ðxÞϱLβ ðyÞ ,

Z
hDbr
1 ðx, yÞii =

dzTr

h

observational quantities. This trade-off puts tight observational constraints on classical theories of gravity which we now discuss.

Physical constraints on the classicality of gravity
In this section, we apply the trade-off of Eq. (30) to the case of gravity.
A number of classical-quantum models of Newtonian gravity have
been proposed24,31–33, but since the trade-offs derived in the previous
section depend only on the back-reaction, or drift term, they are
insensitive to the particulars of the theory. We shall consider the
Newtonian, non-relativistic limit of a classical gravitational ﬁeld which
we reproduce in the “Methods” subsection “Newtonian limit of CQ
theory”. A fuller discussion, including a derivation of the Newtonian
limit starting from the covariant theories of refs. 11,39 can be found in
ref. 81. It is in taking this limit where some care should be taken, since
one is gauge ﬁxing the full general relativistic theory. We denote Φ to
be the Newtonian potential and in the weak ﬁeld limit of General
Relativity, it has a conjugate momenta we denote by πΦ. We assume:
(i) The theory satisﬁes the assumptions used to derive the master
equation as in subsections “Trade-off in the presence of ﬁelds”; in
particular that the theory be a completely positive normpreserving Markovian map, and that we can perform a shorttime Kramers–Moyal expansion as in “Methods” subsection
“Classical-quantum dynamics with ﬁelds”.
(ii) We apply the theory to the weak ﬁeld limit of General Relativity,
whereas recalled in “Methods” subsection “Newtonian limit of CQ
theory” the Newtonian potential interacts with matter through its
mass density m(x),
Z
H I ðΦÞ =

hD2 ðx, yÞiij =

and the conjugate momentum to Φ satisﬁes

i

y
Dμα
1, i Lμ ðxÞϱLα ðxÞ ,

ð33bÞ
Φ
 mðxÞ,
π_ Φ = ∇4πG

h

i
y
dzTr Dμν
2, ij Lα ðxÞϱLβ ðyÞ :

Z

y

dx 0 dy0 hD0 ðx 0 , y0 ÞikhDT1 ðxÞihDT1 ðxÞi ,

ð34Þ

where
Z
hDT1 ðxÞii =

h
i
αβ
y
y
α0
dzTr D0α
1, i ðxÞϱLα ðxÞ + D1, i ðxÞLα ϱðxÞ + D1, i ðxÞLα ðxÞϱLβ ðxÞ :
ð35Þ

We shall now use the trade-off to study the consequences of
treating the gravitational ﬁeld classically. We will consider the backreaction of the mass on the gravitational ﬁeld to be governed by the
Newtonian interaction (or more accurately, a weak ﬁeld limit of General Relativity). We shall then ﬁnd that experimental bounds on
coherence lifetimes for particles in superposition require large diffusion in the gravitational ﬁeld in order to be maintained and this can be
upper bounded by gravitational experiments.
To summarise this section, we have derived the trade-off between
decoherence and diffusion for classical–quantum ﬁeld theories, both
in terms of coupling constants of the theory and in terms of

Nature Communications | (2023)14:7910

ð37Þ

ð33cÞ

αβ
Similarly, when the back-reaction is sourced by either D0μ
1, i or D1, i it
follows from Eq. (32) we can arrive at the observational trade-off in
terms of the total drift due to back-reaction

8hD2 ðx, xÞi

ð36Þ

ð33aÞ

2

Z

3

d xΦðxÞmðxÞ:

where in the c → ∞ limit the momentum constraint πΦ ≈ 0 is imposed
and we recover Poisson’s equation for the Newtonian potential. We
assume this limit of General Relativity is satisﬁed on expectation, at
least to leading order. This may be an overly strong assumption, since
the weak ﬁeld limit may cease to be valid at short distances when the
diffusion becomes large. A relativistic treatment is initiated in (J.
Oppenheim and A. Russo, manuscript in preparation). It is also worth
noting that General Relativity has not been tested at distances shorter
than the millimeter scale, and here we assume it holds to arbitrarily
short distances.
(iii) In relating D0 to the decoherence rate of a particle in superposition, we shall assume that the state of interest is well
approximated by a state living in a Hilbert space of ﬁxed particle
number. We believe this is a mild assumption: ordinary nonrelativistic quantum mechanics is described via a single particle
Hilbert space, and we frequently place composite massive
particles in superposition and they do not typically decay into
multiple particles.
(iv) We will assume that the diffusion kernel D2 ðΦ, x, x 0 Þ does not
depend on πΦ i.e. it is minimally coupled. This is reasonable, since
in the purely classical case matter couples to the Newtonian
potential and not its conjugate momenta.
With these assumptions, and treating the matter density as a
quantum operator ^
mðxÞ, this tells us that in order for the back-reaction
7

## PDF page 8

Article

https://doi.org/10.1038/s41467-023-43348-2

term to reproduce the Newtonian interaction on average
Z



δϱ
3
d x^
mðxÞ
Tr fH I , ϱg = Tr
δπ Φ
Z
 ð38Þ
X
δϱ y
3
=
Tr
d xDμν
ðΦ,
π
,
xÞL
ðxÞ
L
ðxÞ
,
Φ
μ
1, π Φ
δπ Φ ν
μν≠00
then we must pick
^
hDT1, π ϕ ðΦ, π Φ , xÞi =  hmðxÞi,

ð39Þ

meaning that the back-reaction matrix Dμα
1, π Φ is nonvanishing. In the
“Methods” subsection “Newtonian limit of CQ theory” we give
examples of master equations for which Eq. (39) is satisﬁed, but their
details are irrelevant since we only require the expectation of the backreaction force to be the expectation value of the mass—a necessary
condition for the theory to reproduce Newtonian gravity.
As a consequence of the coupling constant and observational
trade-offs derived in Eqs. (31) and (32), a non-zero D1, π Φ implies that
there must be diffusion in the momenta conjugate to πΦ. This diffusion
is equivalent to adding a stochastic random process J(x, t) (the Langevin picture), to the equation of motion (37) to give
π_ Φ =

∇2 Φ
 mðxÞ + uðΦ, ^
mÞ Jðt, xÞ,
4πG

ð40Þ

where we allow some colouring to the noise via a function uðΦ, ^
mÞ
^ (assumption
which can depend on Φ, and the matter distribution m
(iv)). The noise process satisﬁes
Em, Φ ½uJðx, tÞ = 0,

In30 it was shown that there are two classes of CQ dynamics, at
least in the sense that there are those with continuous trajectories in
phase space and those which contain discrete jumps. For the class of
continuous CQ models (see ref. 24 and Appendix section “Continuous
master equation”), we know that J(x, t) should be described by a white
noise process in time, and its statistics should be independent of the
mass density of the particle.
For the discrete class (see ref. 11 and J. Oppenheim, “The constraints of a continuous realisation of post-quantum-classical gravity",
manuscript in preparation) and “Methods” subsection “Discrete master equation”), J(x, t) can involve higher order moments, and will generally be described by a jump process26,30. Its statistics can also depend
on the mass density, since in general the diffusion matrix Dμν
2, ij couples
to Lindblad operators. It is worth noting that the discrete CQ theories
considered in11,26,37 generically suppress higher order moments, and
often we expect that we can approximate the dynamics by a Gaussian
process, but this need not be the case in general.
The stochastic contribution to the Newtonian potential leads to
observational consequences which can be used to experimentally test
and constrain CQ theories of gravity for various choices of kernels
appearing in the CQ master equation. One immediate consequence is
that the variation in Newtonian potential leads to a variation of force
experienced
a
particle
or
composite
mass
via
R 3 by
!
F tot =  dR xmðxÞ∇ΦðxÞ. We can also estimate the time-averaged
ΔT !
1
F tot where ΔT is the time resolution over which the
force via ΔT
0
force is measured and is the useful quantity when compared with
experiments. In the “Methods” subsection “Table-top experiments” we
impose the constraint π ≈ 0 in Eq. (40) and ﬁnd that the variance of the
magnitude of the time-averaged force experienced by a particle in a
Newtonian potential is given by Eq. (146),

Em, Φ ½uJðx, tÞuJðy, t 0 Þ = 2hD2 ðx, y, ΦÞiδðt, t 0 Þ, ð41Þ

y
where we have deﬁned hD2 ðx, y, ΦÞi = Tr½Dμν
2 ðx, y, ΦÞLμ ðxÞρLν ðyÞ, and ρ
is the quantum state for the decohered mass density. Here the m, Φ
subscripts of Em, Φ allow for the possibility that the statistics of the
noise process can be dependent on the Newtonian potential and mass
distribution of the particle. The restriction on Em, Φ ½uJðx, tÞ follows
from assumption (ii). If uJ(x, t) is Gaussian, Eq. (41) completely determines the noise process, but in general, higher-order correlations are
possible, although they need not concern us here, since we are only
interested in bounding the effects due to D2(x, y, Φ).
In the non-relativistic limit, where c → ∞, we impose the momentum constraint πΦ ≈ 0 and we recover Poisson’s equation for gravity,
but with a stochastic contribution to the mass. This is precisely as
expected on purely physical grounds: in order to maintain coherence
of any mass in superposition, there must be noise in the Newtonian
potential and this must be such that we cannot tell which element of
the superposition the particle will be in, meaning the Newtonian
potential should look like it is being sourced in part by a random mass
distribution. In other words, the trade-off requires that the stochastic
component of the coupling obscures the amount of mass m at the
different points in space where the mass may be found.
In the case where u is independent of Φ, it is simple to solve
Eq. (40) in terms of Green’s function for Poisson’s equation as in the
“Methods” subsection “Detecting gravitational diffusion”. A formal
treatment of solutions to non-linear stochastic integrals of the more
general form of Eq. (40) can be found in ref. 82. A higher precision
calculation would involve a full simulation of CQ dynamics, for
example using unravelling methods26,78 or the path integral as in ref. 81.
However, care should be taken, as we have found that relativistic
corrections put constraints on the degree of diffusion even at low
energy (J. Oppenheim and A. Russo, manuscript in preparation), and
one should bear this in mind when drawing conclusions on the models
presented here.

Nature Communications | (2023)14:7910

σ 2F =

Z
2G2
d3 xd3 yd3 x 0 d3 y0 mðxÞmðyÞ
ΔT
! !0 ! !0
ðx  x Þð y  y Þ
hD2 ðx 0 , y0 , ΦÞi,
jx  x 0 j3 jy  y0 j3

ð42Þ

where the variation is averaged over the time resolution ΔT. We will use
this to estimate the variation in precision measurements of mass, such
as modern versions of the Cavendish experiment for various choices
of hD2 ðx 0 , y0 , ΦÞi.
On the other hand, experimentally measured decoherence rates
can be related to D0. The important point is that the decoherence rate
is dominated by the background Newtonian potential Φb due to the
Earth. In the “Methods” subsection “Decoherence rates”, we show that
for a mass whose quantum state is a superposition of two states jLi and
jRi of approximately orthogonal mass densities mL(x), mR(x), and
whose separation we take to be larger than the correlation range of
D0(x, y), the decoherence rate is given by
λ=

1
2

Z

y
y
dxdyDαβ
0 ðx, yÞðhLjLβ ðyÞLα ðxÞjLi + hRjLβ ðyÞLα ðxÞjRiÞ:

ð43Þ

Via the coupling constant trade-off, Eqs. (42) and (43) then give
rise to a double-sided squeeze on the coupling D2. Equation (42) upper
bounds D2 in terms of the uncertainty of acceleration measurements
seen in gravitational torsion experiments, whilst the coupling constant
trade-off Eq. (43) lower bounds D2 in terms of experimentally measured decoherence rates arising from interferometry experiments.
We now show this for various choices of diffusion kernel, with the
details given in the “Methods” subsection “Table-top experiments”.
The bounds are summarised in Table 1. The diffusion coupling strength
will be characterised by the coupling constant D2, which we take to be a
dimension-full quantity with units kg2 sm−3, and is related to the rate of
diffusion for the conjugate momenta of the Newtonian potential. We
upper bound D2 by considering the variation of the time averaged
8

## PDF page 9

Article

https://doi.org/10.1038/s41467-023-43348-2

Table 1 | Current experimental bounds on classical-quantum theories for different master equations and functional dependence on the diffusion coefﬁcient
Master equation

Diffusion kernel

Experimental squeeze

Continuous (ultra-local, non-rel.)

D2(Φ; x, y) = D2(Φ)δ(x, y)D2(Φ) = ∑ncnΦn

10−41  D2  10−9 kg2 sm−3 (Eq. (44))

P
2
D2 ðΦ; x,yÞ =  lp D2 ðΦÞ∇2 δðx,yÞD2 ðΦÞ = n cn Φn
P n n
l2P
D2 ðΦ; x,yÞ = m D2 ðΦÞδðx,yÞD2 ðΦÞ = n c Φ

Continuous (Eq. (116) or (118))
Discrete (ultra-local)

P

109  lP D2  1035 kg sm1 (Eq. (47))
2

10

1

2

l2 D
 Pm 2  1025 kg (Eq. (46))
P

The diffusion coefﬁcient is bounded from above by observed acceleration variations σ 2a seen in precision mass experiments via Eq. (42). In all cases the master equation is assumed to saturate the
bound which is used to ﬁnd the lower bound the amount of diffusion on the quantum system by bounding D0 from coherence rates via Eq. (43). It is seen that minimally coupled continuous models
which are non-relativistic and do not create spatial correlations (we call these ultra-local) and have polynomial dependence on the Newtonian potential are ruled out, while continuous models with
non-local correlations, such as the Diosi–Penrose (DP) kernel of Eq. (116)or the relativity inspired kernel of Eq. (118), and ultra-local discrete models are less constrained. Here lP, mP are the Planck
length and Planck mass respectively, which are required in order for the dimensions of D2(Φ) to be the same in all cases.

acceleration σ a = σMF for a composite mass M which contains N atoms
which we treat as spheres of constant density ρ with radius rN and mass
mN. We lower bound D2 via the coupling constant trade-off of Eq. (30)
and then by considering bounds on the coherence time for composite
particles with total mass Mλ and which are made up of Nλ constituents,
each with typical length scale when in superposition Rλ and volume Vλ.
For continuous dynamics 〈D2(x, y, Φ)〉 = D2(x, y, Φ) since the diffusion is not associated with any Lindblad operators. Let us now consider a very natural kernel, namely D2(x, y; Φ) = D2(Φ)δ(x, y) which is
both translation invariant, and does not create any correlations over
space-like separated regions. We call dynamics which does not create
correlations over space-like separated regions ultra-local since theories that are not of this form can still be non-signalling. This is a
natural kernel from the point of view of constructing theories which
are diffeomorphism invariant. We also label this model as being nonrelativistic since it does not include various relativistic corrections to
the diffusion.
The decoherence rate for this kernel is found in the “Method”
subsection “Decoherence rates” and follows immediately from Eq.
(137). For a nucleon of mass Mλ and wavepacket volume Vλ, it is
λ = 2D0 M 2λ =V λ . In general, the squeeze will depend on the functional
choice of D2(Φ) on the Newtonian potential. However, in the presence
of a large background potential Φb, such as that of the Earth’s, we will
often be able to approximate D2(Φ) = D2(Φb). This is true for kernels
that depend on Φ and ∇ Φ, though the approximation does not hold
for all kernels, for example D2 ~ −∇2Φ of Eq. (118) which creates diffusion only where there is mass density. For diffusion kernels D2(Φb)
where the background potential is dominant, we ﬁnd the promised
squeeze on D2(Φb)
σ 2a Nr 4N ΔT
V b G2

N M2
≥ D2 ≥ λ λ ,
V λλ

ð44Þ

where Vb is the volume of space over which the background Newtonian
potential is signiﬁcant. Vb enters since the variation in acceleration is
found to be
σ 2a ∼

D2 G2
r 4N NΔT

Z

d x 0 D2 ðΦb Þ,
3

3

ð45Þ

where the d x 0 integral is over all space.
This immediately rules out continuous theories of Newtonian
gravity with noise everywhere, i.e., with a diffusion coefﬁcient independent of the Newtonian potential, since the integral will diverge. We
consider the relativistic case elsewhere.
Standard Cavendish-type classical torsion balance experiments49
measure accelerations of the order 10−7 m s−2 over minutes ΔT ~ 102, so
a very conservative bound is σa ~ 10−7 m s−2, whilst for a kg mass N ~ 1026
and rN ~ 10−15 m. Conservatively taking V b ∼ r 2E h m3 where rE is the
radius of the Earth and h is the atmospheric height gives
D2 ≤ 10−41 kg2 sm−3. The decoherence rate λ is bounded by various
experiments83. Typically, the goal of such experiments is to witness
interference patterns of molecules that are as massive as possible.

Nature Communications | (2023)14:7910

Taking a conservative bound on λ, for example, that arising from the
interferometry experiment of59 which saw coherence in large organic
fullerene molecules with total mass Mλ = 10−24 kg over a timescale of
0.1s, gives an upper bound on the decoherence rate λ < 101 s−1. Fullerene molecules are made up of Nλ ~ 103 particles with a typical atomic
size 10−15 m. After passing through the slits the molecule becomes
delocalised in the transverse direction on the order of 10−7 m before
being detected. Since the interference effects are due to the superposition in the transverse x direction, which is the direction of alignment of the gratings, it seems like a reasonable assumption to take the
size of the wavepacket in the remaining y, z direction to be the size of
the fullerene, since we could imagine measuring the y, z directions
without effecting the coherence. We, therefore, take the volume
Vλ ~ 10−1510−1510−7 m3 = 10−37 m3, which gives D2 ≥ 10−9 kg2 sm−3, and suggests that classical–quantum theories of Newtonian gravity with ultralocal continuous noise are ruled out by experiment.
On the other hand, the discrete models appear less constrained
due to the suppression of the noise away from the mass density. For
example consider the ultra-local discrete jumping models, such as the
one given in the section “Discrete master equation” which have
qﬃﬃﬃ
3
l D ðΦ Þ
hD2 ðx, y, Φb Þi = P m2 b mðxÞ, where mP = _c
G is the Planck mass and
P
qﬃﬃﬃﬃ
is the Planck length, required to ensure D2 has the units of
l P = _G
c3
kg2 sm−3. We ﬁnd the squeeze on D2
σ 2a Nr 4N ΔT
mN G2

3

≥

lP
M
D ≥ λ,
mP 2
λ

ð46Þ

and plugging in the numbers tells us that discrete theories of classical
gravity are 3 not ruled out by experiments and we
l
ﬁnd 101 kg ≥ mP D2 ≥ 1025 kg.
P
We can also consider other noise kernels, with examples and some
discussion is given in the section “Examples of Kernels saturating the
decoherence diffusion coupling constants trade-off”. A natural kernel
2
is D2 ðx, y, Φb Þ =  l P DðΦb Þ∇2 δðx, yÞ. The inverse Lindbladian kernel
satisfying the coupling constants trade-off is to zeroeth order in Φ(x),
0 ðΦb Þ
. We here consider higherthe Diosi-Penrose kernel D0 ðx, y, Φb Þ = Djxyj
order terms such as those coming from the relativistic theory and in
particular the diffusion kernel of Eq. (118). For this choice of dynamics,
we ﬁnd the squeeze for D2 in terms of the variation in acceleration
σ 2a Nr 3N ΔT
G

2

2

≥ l P D2 ≥

N λ M 2λ
:
Rλ λ

ð47Þ

Using the same numbers as for the ultra-local continuous model,
1=3
with Rλ ∼ V λ ∼ 1012 m we ﬁnd that classical torsion experiments
2
2
upper bound D2 by 109 kg sm1 ≥ l P D2 , whilst interferometry
2
2
experiments bound D2 from below via l P D2 ≥ 1035 kg sm1 .
Equations (44), (46) and (47) show that classical theories of gravity
are squeezed by experiments from both ways. We have here been
extremely conservative, and we anticipate that further analysis, as well
as near-term experiments, can tighten the bounds by orders of
9

## PDF page 10

Article
magnitude. There are several proposals for table-top experiments to
precisely measure gravity, some of which have recently been performed, and which could give rise to tighter upper bounds on D2. Some
of these experiments involve millimeter-sized masses whose gravitational coupling is measured via torsional pendula61,62, or rotating
attractors63. With such devices, the gravitational coupling between
small masses can be measured while limiting the amount of other
sources of noise. There are proposals for further mitigating the noise
due to the environment, including inertial noise, gas particle collisions,
photon scattering on the masses, and curvature ﬂuctuations due to
other sources84–86. Other experiments are based on interference
between masses; for example, atomic interferometers allow for the
measurement of the curvature of space-time over a macroscopic
superposition87–89.
We can get stronger lower bounds via improved coherence
experiments. Typically, the goal of such experiments is to witness
interference patterns of molecules that are as massive as possible,
while here, we see that the experimental bound on CQ theories is
generically obtained by maximising the coherence time for massive
particles with as small wave-packet size Vλ.
Thus far we have considered local effects on particles due to
diffusion. While this enables us to rule out some types of theories, the
bounds are generally weak if one wants to rule out all of them. However, it may be possible to do so via cosmological considerations. In
attempting to place experimental constraints on this diffusion, it is
also worth considering other regimes, such as longer range effects
which might be detected by gravitational wave detectors such as LIGO,
or table-top interferometers90,91. We leave a detailed study of the effect
of gravitational diffusion on cosmological scales and LIGO to future
work. It sufﬁces to mention that the effect will again depend on the
form of the kernel D2 ðx, x 0 Þ. Our estimates (J. Oppenheim and Z. WellerDavies, “Estimating space-time diffusion in interferometers", unpublished note) suggest that local effects from table-top experiments
currently place a stronger bound on gravitational theories than LIGO
currently does. In particular, unlike gravitational wave measurements,
which are reasonably high-frequency events requiring extraordinarily
high precision in the relative displacement of the arm length from its
average, it is preferential to have a lower precision measurement,
which occurs over a longer time period to allows for the diffusion in
path length to build up, and with a smaller uncertainty in the average
length of the arm itself. Furthermore, since the LIGO arm is kept in a
vacuum, we do not expect strong bounds on discrete models where
the diffusion is associated with an energy density.

Discussion
A number of direct proposals to test the quantum nature of gravity are
expected to come online in the next decade or two. These are based on
the detection of entanglement between mesoscopic masses inside
matter-wave interferometers64–70,72,73. For these experiments, some
theoretical assumptions are needed: one requires that it is only gravitons that travel between the two masses and mediate the creation of
entanglement. If this is the case, then the onset of entanglement
implies that gravity is not a classical ﬁeld. These can be thought of as
experiments that if successful, would conﬁrm the quantum nature of
gravity (although other alternatives to quantum theory are possible92).
Here, we come from the other direction, by supposing that gravity
is instead classical, and then exploring the consequences. Theories in
which gravity is fundamentally classical were thought to have been
ruled out by various no-go theorems and conceptual difﬁculties.
However, these no-go theorems are avoided if one allows for nondeterministic coupling as in11,21–26,30,37. We have here proven that this
feature is indeed necessary and made it quantitative by exploring the
consequences of complete positivity on any dynamics that couples
quantum and classical degrees of freedom. Complete positivity is
required to ensure the probabilities of measurement outcomes remain

Nature Communications | (2023)14:7910

https://doi.org/10.1038/s41467-023-43348-2

positive throughout the dynamics. We have shown that any theory
which preserves probabilities and treats one system classically is
required to have fundamental decoherence of the quantum system,
and diffusion in phase space, both of which are signatures of information loss. Using a CQ version of the Kramers–Moyal expansion, we
have derived a trade-off between decoherence on the quantum system, and the system’s diffusion in phase space. The trade-off is
expressed in terms of the strength of the back-reaction of the quantum
system on the classical one. We have derived the trade-off both in
terms of coupling constants of the theory and in terms of observational quantities that can be measured experimentally.
In the case of gravity, the trade-off places a lower bound on the
rate of diffusion of the gravitational degrees of freedom in terms of the
decoherence rate of particles in superposition. We ﬁnd that theories
that treat gravity as fundamentally classical, are not ruled out by current experiments, however, we have been able to rule out a broad
parameter space of Newtonian theories. This is done partly through
table-top observations via Eqs. (44), (46) and (47). Given any diffusion
kernel, we can compute the inaccuracy of mass measurements due to
ﬂuctuations in the gravitational ﬁeld, and using the trade-off, we can
derive a bound on the associated decoherence rate. This allows us to
rule out broad classes of theories in terms of their diffusion kernel. For
example, we are able to rule out a number of non-relativistic theories
which back-react continuously in phase space.
Any theory that treats gravity classically has fairly limited freedom
to evade the effects of the trade-off. There is the freedom to choose the
diffusion or decoherence kernels D2 ðx, x 0 Þ and D0 ðx, x 0 Þ, but the tradeoff restricts one in terms of the other. Then, because of the results
proven in30, one can consider two classes of theory, those which are
continuous realisations and whose diffusion can only depend on the
gravitational degrees of freedom, and discrete theories whose diffusion can also depend directly on the matter ﬁelds. Examples of both
classes of the theory are given in the “Methods” subsection “Newtonian
limit of CQ theory”. Finally, one could consider theories that do not
reproduce the weak ﬁeld limit of General Relativity to all distances,
namely we could imagine that the interaction Hamiltonian of Eq. (36)
does not hold to arbitrarily short distances, or arbitrarily high mass
densities. This is reasonable since we do expect the Newtonian theory
to break down at short distances where relativistic corrections at high
energy affect the low-energy behaviour of the theory. One could also
consider modifying D1 ðx, x 0 Þ in some other way, for example, by
making it slightly non-local, or by disallowing arbitrarily high mass
densities, or by including an additional contribution such as the friction term discussed in the continuous master equation. All of these
modiﬁcations would seem to violate Lorentz invariance in some way,
and likely lead to observational consequences93.
Here, we have only given an order of magnitude estimate of when
gravitational diffusion will lead to appreciable deviations from Newtonian gravity. The most promising experiments bounding the diffusion appear to be table-top experiments which precisely measure the
mass of an object. This is an area that is important from the perspective
of weight standards, for example, those undertaken by NIST on the 1 kg
mass standard K20 and K494. The increased precision and measuring
time of Kibble Balances95 and atomic interferometers87,88,96,97 would
make such measurements an ideal testing ground, both to further
constrain the diffusion kernel and to look for diffusion effects, whose
dependence on the test mass is outlined in the “Methods” subsection
“Detecting gravitational diffusion”. Here, we have found that the
resolution time ΔT over which variations of acceleration are estimated
affects the strength of the bound, and it would be helpful if future
experiments reported this value. Since we have found that CQ theories
predict an uncertainty in mass measurements it is perhaps intriguing
that different experiments to measure Newton’s constant G yield
results whose relative uncertainty differs by as much as
5 × 10−4 m3 kg−1 s−2, which is more than an order of magnitude larger
10

## PDF page 11

Article
than the average reported uncertainty52–54. If one were to try and
explain the discrepancy in G measurements via gravitational diffusion,
then for all the kernels we studied in Section ’Physical constraints on
the classicality of gravity’ we ﬁnd that the variation in acceleration
the number of nucleons in the test mass, so that masses
depends on p1ﬃﬃﬃ
N
with smaller volume should yield larger uncertainty and this would be
the effect to look for in measurement discrepancies. The relatively
large uncertainty in such measurements, also makes it challenging for
table-top experiments to place strong upper bounds on gravitational
diffusion.
Turning to the other side of the trade-off, improved decoherence
times would further squeeze theories in which gravity remains classical. While a current experimental challenge is to demonstrate interference patterns using larger and larger mass particles, we here ﬁnd
the bounds in Eqs. (44) and (46) depend on the expectation of the
particle’s mass density in ways that depend on the particular kernel.
Thus interference experiments with particles of high mass density
rather than mass can be preferable. There are also kernels, for which
the relevant quantity is the expectation of the mass density or M 2λ =V λ ,
which will depend on both the particle’s mass Mλ and volume Vλ of the
wave-packet used in the interference experiment, a quantity which is
not always obtainable from many reports on such experiments. While
this dependence might initially appear counter-intuitive, it follows
from the fact that in order to relate the trade-off in terms of coupling
constants to observational quantities, and in particular, the decoherence rate, we took expectation values of the relevant quantities to
get a trade-off in terms of only averages. And indeed the decoherence
rate, which is an expectation value, can easily depend on the wavepacket density, as we see from examples in the section “Decoherence rates”.
Since we here show that all theories that treat gravity classically
necessarily decohere the quantum system, another constraint on
theories that treat gravity classically is given by constraints on fundamental decoherence. These are usually constrained by bounds on
anomalous heating of the quantum system98. However, these constraints are not in themselves very strong, since fundamental decoherence effects can be made arbitrarily weak. In the simpliﬁed model in
the “Methods” subsection “Newtonian limit of CQ theory”, the strength
of the decoherence depends on the strength of the gravitational ﬁeld,
thus, constraints due to heating98–111 can be suppressed, either by
scaling the Lindbladian coupling constants or by having strong decoherence effects more pronounced near stronger gravitational ﬁelds
such as near black holes where one expects information loss to occur.
The necessity for decoherence to heat the quantum system is further
weakened by the fact that the dynamics are not Markovian on the
quantum ﬁelds, if one integrates out the classical degrees of freedom,
space-time acts as a memory. This potentially captures some of the
non-Markovian features advocated in ref. 112, who recognised that
Markovianity is a key assumption in attempts to rule out fundamental
decoherence or information loss. Here, however, we see that there is
less freedom than one might imagine. If the Lindbladian coupling
constants are made small to reduce direct heating, the gravitational
diffusion must be large. Thus, heating constraints which place bounds
on D0 ðx, x 0 Þ place additional constraints on D2 ðx, x 0 Þ. In35, it was found
that for the Newtonian models of ref. 33, large D2 ðx, x 0 Þ creates secondary heating which further constrain the theory experimentally. The
decoherence-diffusion trade-off implies that this is a general feature of
all theories which treat gravity classically.
While the absence of diffusion could rule out theories where
gravity is fundamentally classical, the presence of such deviations, at
least on short time scales, might not by itself be a conﬁrmation of the
classical nature of gravity. Such effects could instead be caused by
quantum theories of gravity whose classical limit is effectively described

Nature Communications | (2023)14:7910

https://doi.org/10.1038/s41467-023-43348-2

by Oppenheim11. In other words, one might expect some gravitational
diffusion, because, from an effective theory point of view, one is in a
regime where space-time is behaving classically. There are even claims
that holographic effects could cause stochasticity113–115 in the gravitational ﬁeld. However, the trade-off we have derived is a direct consequence of treating the background space-time as fundamentally
classical. In a fully quantum theory of gravity, the interaction of the
gravitational ﬁeld with particles in a superposition of two trajectories
will cause decoherence, but coherence can then be restored when the
two trajectories converge. This is because the particle’s position is
entangled with the gravitational ﬁeld (or dressed by it), and this
entanglement is erased when the different paths of the superposition
converge. This is what happens when electrons interact with the electromagnetic ﬁeld while passing through a diffraction grating, yet still
form an interference pattern at the screen. This is a non-Markovian
effect—the which-path superposition decoheres almost immediately,
but this is false-decoherence116 so the amount of diffusion can be arbitrarily small and is unrelated to the coherence time of the superposition.
On the other hand, the trade-off we derived is a direct consequence of the positivity condition, which is a direct consequence of
the Markovian assumption. In the non-Markovian theory where General Relativity is treated classically, one still expects the master equation to take the form found in11, but without the matrix whose elements
117,118
. It would
are Dμν
n needing to be positive semi-deﬁnite at all times
therefore be surprising, if a quantum theory of gravity predicted
anything close to the level of diffusion predicted by the decoherencevs-diffusion trade-off, as there would be no need for diffusion to
explain the coherence of superpositions. The regime in which the
classical–quantum theory can be regarded as an effective one is taken
up in ref. 119, both to address the issue of false decoherence, and also
to explore the regime in which the classical–quantum theory may be a
useful tool to understand the back-reaction of quantum matter in
space–time, such as during black-hole evaporation, and during inﬂation. If we instead regard the theory as describing a fundamentally
classical space-time, then it follows from the decoherence-diffusion
trade-off, that the diffusion is either fundamental or its source is not
describable within quantum or classical mechanics (J. Oppenheim,
“Post-quantum soup", unpublished note).

Methods
Positivity conditions and the trade-off between decoherence
and diffusion
In this section, we will introduce two forms of positivity conditions
used to prove the decoherence diffusion trade-off.
The ﬁrst inequality we would like to introduce is
Z

dzA*μ ðz, z 0 ÞΛμν ðzjz 0 , δtÞAν ðz, z 0 Þ ≥ 0,

ð48Þ

which holds for any Aμ ðz, z 0 Þ for which Eq. (48) is well deﬁned: i.e., so
that the distributional derivatives in Eq. (48) are well deﬁned.
We can derive the positivity condition (48) from the positivity of
Λμν ðzjz 0 Þ, which must be a positive semi-deﬁnite matrix in μν. More
μ
precisely, the eigenvalues of Λμν ðzjz 0 Þ, which we denote by λ ðzjz 0 Þ
must be positive. They must be positive in the distributional sense,
μ
since we allow for the case that λ ðzjz 0 Þ is a positive distribution, for
0
example λ ðzjz 0 Þ ∼ δðz  z 0 Þ. Hence we require
Z

μ

dzdz 0 λ ðzjz 0 ÞPðz, z 0 Þ

ð49Þ

is positive for any positive smearing function Pðz, z 0 Þ. Since each λμ
must be positive, we can also pick a different smearing function for

11

## PDF page 12

Article

https://doi.org/10.1038/s41467-023-43348-2

each μ, so that
Z

Since we know D2 and D0 must be positive semi-deﬁnite, we know from
Schur decomposition that
μ

dzdz 0 λ ðzjz 0 ÞP μ ðz, z 0 Þ

ð50Þ

should be positive for any vector P μ ðz, z 0 Þ with all positive entries. We
can then write the matrix Λμν ðzjz 0 Þ in terms of its eigenvalues
ρ

ν
0
0
0
Λμν ðzjz 0 Þ = U μy
ρ ðzjz Þλ ðzjz ÞU ρ ðzjz Þ:

dzA*μ ðz, z 0 ÞΛμν ðzjz 0 , δtÞAν ðz, z 0 Þ =

Z
Z

=

μ

dzðUAÞyμ ðzjz 0 Þλ ðzjz 0 ÞðUAÞμ ðz, z 0 Þ
μ

dzjðUAÞμ j2 ðz, z 0 Þλ ðzjz 0 Þ

which is positive as a consequence of Eq. (50).
As a consequence of Eq. (48) being positive, we also know that
Z


dzΛμν ðzjz 0 ÞOμ ðz, z 0 Þρðz 0 ÞOyν ðz, z 0 Þ ≥ 0

ð53Þ

will be positive for any vector of operators (potentially phase space
dependent) Oμ ðz, z 0 Þ. This follows from the cyclicity of the trace and
the fact that Λμν ðzjz 0 ÞOyν ðz, z 0 ÞOμ ðz, z 0 Þ will be a positive operator so
long as Eq. (48) holds. A common choice of Oμ would be the Lindblad
operator Lμ appearing in the master equation.
The inequality in Eq. (48) proves useful to derive positivity
conditions on the coupling constants appearing in the master
equation, whilst Eq. (53) is useful in deriving the observational
trade-off for the continuous master equation as we shall now
discuss.

We can get a general trade-off between the decoherence and diffusion
coefﬁcients which appear in the master equation, arriving at a trade-off
between the decoherence and diffusion coefﬁcients in terms of the
back-reaction drift coefﬁcient Dμα
1, i .
i
Consider Eq. (48), and choose Aμ = δ αμ aα + bμ ðz  z 0 Þi . By integrating parts over the phase space degrees of freedom, we ﬁnd
i*
j
i* μβ
* αμ i
* αβ
2bμ Dμν
2, ij bν + bμ D1, i aβ + aα D1, i bμ + aα D0 aβ ≥ 0:

*

½b , a* 

2D2
Dbr
1

2D2
Dbr
1

Dbr
1
D0

#
k0:

Z

dzdxdyΛμν ðzjz 0 ; x, yÞLμ ðx, z, z 0 Þϱðz 0 ÞLyν ðy, z, z 0 Þ,

ð58Þ

where the positivity condition states
Z

dzdxdyA*μ ðx, z, z 0 ÞΛμν ðzjz 0 ; x, yÞAν ðy, z, z 0 Þ ≥ 0:

ð59Þ

CQ Kramers–Moyal expansion for ﬁelds

Just as in the section “The CQ Kramers–Moyal expansion”, we can
formally introduce the moments of the transition amplitude
M μν
n, i ...i ðw1 , . . . wn ; x, y, δtÞ =

Z

n

1

DzΛμν ðzjz 0 ; x, y, δtÞ ðz  z 0 Þi1 ðw1 Þ . . . ðz  z 0 Þin ðwn Þ

ð60Þ
which we assume to exist; which might involve a smearing of the
operators z(x). Deﬁning L0 ðxÞ = δðxÞI, we can deﬁne the coefﬁcients
Dμν
n, i ...i implicitly via
n

1

μ

ð55Þ

br
where D2 is the (p + 1)n × (p + 1)n matrix with elements Dμν
2, ij , D1 is
the (p + 1)n × p matrix with rows labelled by μi and columns
labelled by β with elements Dμβ
1, i and D0 is the p × p decoherence
br
matrix with elements Dαβ
0 . D1, i describes the quantum backreacting components of the drift. Equation (55) is equivalent to
the condition that the ððp + 1Þn + pÞ × ððp + 1Þn + pÞ matrix

"

ρ0 ðzÞ =

ð54Þ

Taking i ∈ {1, …, n}α ∈ {1, …, p} and μ ∈ {1, …, p + 1}, we can write
this as a matrix positivity condition
# 
b
Dbr
1
≥0
a
D0

In this section, we describe CQ dynamics in the case where the Lindblad operators and the phase-space degrees of freedom can have
spatial dependence z(x), Lμ(x).
For the case of ﬁelds, operators O(x) constructed out of local
ﬁelds ϕ(x) will in general be unbounded and hence the Stinespring
dilation theorem does not hold. This problem is a common one in the
study of algebraic quantum ﬁeld theory and we can get around it by
considering the case in which operators of interest are obtained by
smearing the local ﬁelds over bounded functionals F. For example, we
can ﬁrst smear the local ﬁeld ﬁelds over a smearing function
f, ϕf = ∫dxϕ(x)f(x) and then consider bounded functions of ϕf such as
Fðϕf Þ = eiϕf . In doing this we can write a CQ version of the Stinespring
dilation theorem exactly and proceed along the lines of Oppenheim11
to show that any completely positive CQ map can be written in the
form

We shall assume that we deal with dynamics which can be written
in Lindblad form, as is usually assumed in the unbounded case120.

General trade-off between decoherence and diffusion
coefﬁcients

"

and ðI  D0 D0  1ÞDbr
1 = 0, where D0 is the generalised inverse of D0.
Furthermore, if D0 vanishes, then clearly Dbr
1 must also vanish in order
for (56) to be positive semi-deﬁnite.

Classical-quantum dynamics with ﬁelds

ð52Þ

Tr

ð57Þ

ð51Þ

We can then see the positivity of Eq. (48) directly since
Z

1 bry
2D2 kDbr
1 D0 D1 ,

ð56Þ

ν

μν
0
M μν
n, i ...i ðz , w1 , . . . wn ; x, y, δtÞ = δ 0 δ 0 + δtn!Dn, i ...i ðw1 , . . . wn ; x, y, δtÞ:
1

n

n

1

ð61Þ
The characteristic function then takes the form
C μν ðu, z 0 ; x, yÞ =

Z

Dzei

R

dwuðwÞðzðwÞz 0 ðwÞÞ μν

Λ ðzjz 0 ; x, yÞ

ð62Þ

and expanding out the exponential this takes the form
C μν ðu, z 0 ; x, yÞ =

1 Z
X
n=0

dw1 . . . dwn

ui ðw1 Þ . . . uin ðwn Þ
n!

0
M μν
n, i ...i ðz , w1 , . . . wn ; x, y, δtÞ
1

n

ð63Þ
performing the inverse Fourier transform, allows us to write the
transition amplitude in terms of functional derivatives of the delta

Nature Communications | (2023)14:7910

12

## PDF page 13

Article

https://doi.org/10.1038/s41467-023-43348-2

function

Since we know D2 and D0 must be positive semi-deﬁnite, we know
from Schur decomposition that

Λμν ðzjz 0 ; x, y, δtÞ =

1 Z
X

dw1 . . . dwn

0
M μν
n, i ...i ðz , w1 , . . . wn ; x, y, δtÞ
1

n

n!

n=0

n

δ
δðz, z 0 Þ
δz 0i ðw1 Þ . . . z 0i ðwn Þ
n

1

ð64Þ

1 bry
2D2 kDbr
1 D0 D1

ð69Þ

br
ðI  D0 D1
0 ÞD1 = 0,

ð70Þ

and
and we can use this to write a CQ master equation in the form
n
1


XZ
∂ϱðz, δtÞ
δ
D00 ðz, w1 , . . . wn ÞϱðzÞ  i½H, ϱðzÞ
=
dw1 . . . dwn ð1Þn
δz i1 ðw1 Þ . . . z in ðwn Þ n, i1 ...in
∂t
n=1
Z
1 αβ
y
+
dxdyDαβ
0 ðz; x, yÞLα ðxÞϱðzÞLβ ðyÞ  D0 ðz; x, yÞfLβ ðyÞLα ðxÞ, ϱg
2
Z
1 X
X
+
dxdydw1 . . . dwn ð1Þn
n = 0 μν≠00
n



δ
Dμν
ðz, w1 , . . . wn ; x, yÞLμ ðxÞϱðzÞLyν ðyÞ :
δz i1 ðw1 Þ . . . z in ðwn Þ n, i1 ...in

Observational trade-off in the presence of ﬁelds
ð65Þ

Since we are interested in studying dynamics with local backμν
reaction, we shall hereby take Dμν
1 ðz, w; x, yÞ = D1 ðxÞδðx, yÞδðx, wÞ.
By the decoherence diffusion trade-off, which we derive in the
next subsection, this also means that the diffusion matrix
is
lower
bounded
by
the
matrix
Dμν
2, ij ðz, w1 , w2 , x, yÞ
βν*
1
seen more preDμα
1 ðxÞðD0 Þαβ ðx, yÞD1 ðyÞδðw1 , xÞδðw2 , yÞ. This can be
R
i
α
cisely, by taking Eq. (59) with Aμ ðxÞ = δ μ aα ðxÞ + dwbμ ðx, wÞðz 
0
z Þðx, wÞ and applying the same methods as in the subsection “Tradeoff between diffusion and decoherence couplings in the presence of
ﬁelds”.
Without
loss
of
generality
we
thus
take
D2(z, w1, w2, x, y) = D2(z, x, y)δ(x, w1)δ(y, w2).

Trade-off between diffusion and decoherence couplings in the
presence of ﬁelds

In the ﬁeld-theoretic case, the positivity condition is given by Eq. (59)
and we can ﬁnd a trade-off between decoherence and diffusion by
R
i
α
considering Aμ ðxÞ = δ μ aα ðxÞ + dxbμ ðxÞðz  z 0 ÞðxÞ. So that
Z

μβ
αμ
*
dxdy2bμ ðxÞDμν
2, ij ðx, yÞbν ðyÞ + bμ ðxÞD1, i ðx, yÞaβ ðyÞ + aα ðxÞD1, i ðx, yÞbμ ðyÞ
i*

j

where D1
0 is the generalised inverse of D0. Furthermore, from Equation (70), we see if D0 vanishes, then clearly Dbr
1 must also vanish in
order for (68) to be positive semi-deﬁnite.

i*

i

+ a*α ðxÞDαβ
0 ðx, yÞaβ ðyÞ ≥ 0

We can use the same methods to arrive at an observational trade-off
using the ﬁeld-theoretic version of the Cauchy–Schwartz inequality in
Eq. (18). This arises from the positivity of
Z
Tr


dzdz 0 dxdyΛμν ðzjz 0 , x, yÞOμ ðz, z 0 , xÞρðz 0 ÞOyν ðz, z 0 , yÞ ≥ 0

for any local vector of CQ operators Oμ ðz, z 0 , xÞ. We have to be careful,
since (71) is not in general well deﬁned since Oμ may not be trace-class.
We hence assume that we consider states ρ(z) and operators Oμ ðz, z 0 , xÞ
for which Eq. (71) is well deﬁned. Since we are interested in getting an
observational trade-off we expect this to always be the case for
physical classical–quantum states ρ(z).
We shall use Eq. (71) to arrive at a (pseudo) inner product on a
vector of operators Oμ via
 i=
 ,O
hO
1
2

and

Taking i ∈ {1, …, n}α ∈ {1, …, p} and μ ∈ {1, …, p + 1}, we can write
this as a matrix positivity condition
R

"
*

dxdy½b ðxÞ, a*ðxÞ

2D2 ðx, yÞ

Dbr
1 ðx, yÞ

Dbr
1 ðx, yÞ

D0 ðx, yÞ

#

bðyÞ
αðyÞ


≥0

"

2D2

Dbr
1

Dbr
1

D0

#
k0

ð68Þ

be positive semi-deﬁnite. Here we are viewing the objects of
Eq. (68) as matrix-kernels, so that for any position-dependent
R
i
μ
j
vector bμ ðxÞ, ðD2 bÞi ðxÞ = dyDμν
2, ij ðx, yÞbν ðyÞ.

Nature Communications | (2023)14:7910

h
i
dzdz 0 dxdyTr Λμν ðzjz 0 x, yÞO1μ ðxÞϱðz 0 ÞOy2ν ðyÞ

 jj2  jhO
 ,O
 ij2 ≥ 0:
 jj2 jjO
jjO
1
2
1
2

ð72Þ

ð73Þ

α

Choosing
O1, μ ðxÞ = δ μ Lα ðxÞ
R
i
O2, μ ðxÞ = dx 0 b ðxÞðz  z 0 Þi ðxÞLμ ðxÞ, one ﬁnds
 jj2 =
jjO
1

ð67Þ

where D2(x, y) is the (p + 1)n × (p + 1)n matrix-kernel with elements
br
Dμν
2, ij ðx, yÞ, D1 ðx, yÞ is the (p + 1)n × p matrix-kernel with rows labelled by
μi and columns labelled by β with elements Dμβ
1, i ðx, yÞ and D0(x, y) is the
br
p × p decoherence matrix-kernel with elements Dαβ
0 ðx, yÞ. D1, i describes
the quantum back-reacting components of the drift.
Equation (67) is equivalent to the condition that the
ððp + 1Þn + pÞ × ððp + 1Þn + pÞ matrix of operators

Z

pﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ
 = hO,
 Oi
 ≥ 0 due to Eq. (71). Technically this is not positive
where jjOjj
 jj≠0,
deﬁnite, but again, this will not worry us. Hence, so long as jjO
2
which holds due to the CQ inequality derived in the derivation of the
Pawula theorem30, we again have a Cauchy–Schwartz inequality

ð66Þ
μν
where we use the shorthand notation Dμν
2, ij ðz, x, yÞ :¼ D2, ij ðx, yÞ
αμ
αμ
similarly D1, i ðz; x, yÞ :¼ D1, i ðx, yÞ.

ð71Þ

 jj2 = 2
jjO
2

Z

Z

and

h
i
y
dzdxdyTr Dαβ
0 ðz; x, yÞLα ðxÞϱðzÞLβ ðyÞ :¼ hD0 i

ð74aÞ

h
i
j*
i
y
dzdxdyTr b ðxÞDμν
2, ij ðz; x, yÞLμ ðxÞϱðzÞLν ðyÞb ðyÞ

ð74bÞ

Z
h
i2  Z

i*
 ,O
 ij2 =  dzdxTr bi* ðxÞDαν ðz; xÞL ðxÞϱðzÞLy ðxÞ  :¼ 
jhO
dxb ðxÞDbr
1
2
α
1, i
ν
1, i ðxÞ




2




ð74cÞ
Taking the limit b ðxÞ ! δðx, x Þb ðx Þ, we arrive at a local tradeoff between diffusion, drift and total decoherence. In particular,
using (74), the deﬁnitions of the expectation values of couplings
deﬁned in Eq. (33) and the fact that for back-reaction the
expectation value of D0 cannot vanish, we arrive at the observational trade-off of Eq. (34)
i

i

h
i
i
 2 j 
b ðx Þ 2hD2, ij ðx , x ÞihD0 i  jhDbr
1, i ðx Þij b ðx Þ ≥ 0

ð75Þ

13

## PDF page 14

Article

https://doi.org/10.1038/s41467-023-43348-2

coupled matter

which we write in matrix form as
y

Z

ð76Þ

br 

2hD2 ðx , x ÞihD0 ikhDbr
1 ðx ÞihD1 ðx Þi :

It then follows directly from Eq. (76) that when the back-reaction
αβ
is sourced by either D0μ
1, i or D1, i components we can arrive at the
observational trade-off in terms of the total drift
y

ð77Þ

8hD2 ðx , x ÞihD0 ikhDT1 ðx ÞihDT1 ðx Þi ,

S=



∂g ij
∂ϕ
d4 x π ij
+ π m m  NH  N i Hi ,
∂t
∂t

ð84Þ

where we are ignoring the boundary contributions to the action. Here,



c4
16πG 1
1
g 1=2 R +
g ik g jl π ij π kl  π 2 + HðmÞ ,
H 
2
1=2
16πG
c g
2

ð85Þ

y

where in Eq. (77) recall that the deﬁnition of hDT1 ðx Þi is given by Eq. (35)
in the main body.

A spatially averaged observational trade-off
It is also useful to note that one can arrive at a spatially averaged
observational trade-off which can be used to bound all of the elements
of the diffusion matrix, not just its diagonals. Speciﬁcally, taking Eq.
(74) with bi(x) = bi a constant, we arrive at the trade-off
Z

Z
8

Z
dxDT1 ðxÞ

dxdyhD2 ðx, yÞihD0 ik

y

dxDT1 ðxÞ

,

ð78Þ

Z

dxdyhD2 ðx, yÞi ≥

M2
:
16λ

Z
8

hD2 ðx, yÞi
hD ik
dxdy
jx  xjjx  yj 0

*Z

+*Z
+y
DT1 ðxÞ
DT1 ðxÞ
dx
dx
jx  xj
jx  xj

Z

R
2
^

hD2, πΦ π Φ ðx, yÞi  dx hjmðxÞi
jh ^
Φðx Þij2
x xj
≥
=
,
dxdy
jx  xjjx  yj
16λ
16G2 λ

where we have deﬁned
R
^
as h ^
Φi =  G dx hjmðxÞi
x xj .

the

effective

Newtonian

ð82Þ



Φ
N = 1 + 2 , N i = 0,
c

pﬃﬃﬃ 0
g NT i :

ð88bÞ



2Φ
c2
g ij = 1  2 δ ij , π ij =  π Φ δ ij ,
6
c

ð89Þ

with Φ(x) corresponding to the Newtonian potential. The choice of
2
ij
π ij =  c6 π Φ δ , is to ensure that πΦ is canonically conjugate to Φ. A
more detailed derivation starts from the full weak ﬁeld metric, and
gauge ﬁxing of the shift can be found in81. Here, we ﬁnd the effective
action can be written
Z
S=



∂Φ
∂ϕ
4
+ π m m  H Newt ,
d x πΦ
∂t
∂t

ð90Þ

where the Newtonian Hamiltonian is given by
H Newt = H c + H 0ðmÞ + H I

ð91Þ

with
Z

potential

ð88aÞ

We here take the Newtonian limit of the gravitational ﬁeld to be
given by

ð81Þ
which for the Newtonian limit gives a trade-off between the diffusion
matrix and the effective Newtonian potential of the particle as sourced
by its expectation value

pﬃﬃﬃ 2 00
gN T ,

HiðmÞ =

ð80Þ

We can also arrive at a trade-off in terms of the effective Newi
1
tonian potential sourced by the masses by taking b ðxÞ = jxxj
. In this
case, we ﬁnd the trade-off

ð87Þ

It is useful to note that the matter densities HðmÞ , HiðmÞ can be
related to the matter stress-energy Tμν via

ð79Þ

For the Newtonian limit discussed in the main body this bounds
the diffusion in terms of the total mass of the particle
Z



c3
g 1=2 K ij  Kg ij :
16πG

π ij  

HðmÞ =

h
i
y
dzTr Dμν
2, ij ðz; x, yÞLμ ðxÞϱðzÞLν ðyÞ :

ð86Þ

are the Hamiltonian and momentum constraints and πij is deﬁned in
terms of the extrinsic curvature tensor of constant t surfaces, Kij, via

where we deﬁne the expectation matrix
hD2 ðx, yÞiij =

c3
g ∇ π jk + HðmÞ
i ,
8πG ij k

Hi 

Hc =

2Gπc2 2 ð∇ΦÞ2
πΦ +
d x 
3
8πG
3

!
ð92Þ

the pure gravity Hamiltonian, and

Newtonian limit of CQ theory
In this section we motivate the Newtonian limit of gravity used in
Section ’Physical constraints on the classicality of gravity’121. A fuller
treatment can be found in81. We begin with classical General Relativity
in the ADM formulation36. To derive the Hamiltonian, we start from the
3+1 split of the four metric



2
ds2 =  ðNc dtÞ + g ij dx i + N i c dt dx j + N j c dt ,

ð83Þ

in which case, denoting ϕm, πm as canonical variables for the
matter degrees of freedom, we can write the action for minimally

Nature Communications | (2023)14:7910

Z
HI =

d3 xΦðxÞmðxÞ

ð93Þ

is the interaction Hamiltonian, from which we see that non-relativistic
matter couples to the Newtonian potential through its mass density
m(x). In the case where we have the state of matter being described by a
point particle δ(x−x(t)) of mass m the pure matter Hamiltonian would be
H 0ðmÞ = mc2 +

ij

δ pi pj
:
2m

ð94Þ

14

## PDF page 15

Article

https://doi.org/10.1038/s41467-023-43348-2

The equations of motion for the gravitational degrees of freedom
reads
2

_ =  4πGc π ,
Φ
Φ
3

ð95Þ

∇2 Φ
 mðxÞ,
4πG

ð96Þ

π_ Φ =

which, for πΦ = 0 yields the Newtonian solution for a stationary mass
density. In a Louivile formulation the dynamics for the density
ρ(Φ, πΦ, xi, pi) is given by
∂ρ
∂ρ
= fH c + H 0ðmÞ , ρg  ∂i ΦðxÞ
+
∂t
∂pi

Z

3

d x mðxÞ

δρ
,
δπ Φ ðxÞ

ð97Þ

where the Hamiltonian and momentum constraints tell us that
ρ(Φ, πΦ, xi, pi) should only have support over phase space degrees of
freedom which satisfy the constraint πΦ ρ(Φ, πΦ) = 0. From Eq. (97) we
can identify the classical drift associated to the back-reaction of the
matter on the gravitational ﬁeld from the mðxÞ δπδρðxÞ term, so that
Φ

Dbr
1, π Φ ðxÞ =  mðxÞ:

ð98Þ

In the classical-quantum case, we promote m(x) to an operator ^
m.
In this case Eq. (93) is the interaction Hamiltonian used in ref. 24 to
study CQ gravity. We see from Eq. (97) that in any theory whose ﬁrst
moment reproduces the Newtonian back-reaction on average


Tr fH I , ϱg =

Z


3
d x Tr ^
mðxÞ


δρ
δπ Φ ðxÞ

ð99Þ

must have a Dbr
1, π Φ given by
^
hDbr
1π Φ ðxÞi =  hmðxÞi,

ð100Þ

from which the discussion at the beginning of the section “Physical
constraints on the classicality of gravity” follows.
Note that the present discussion is insensitive to the details of the
theory provided it satisﬁes Poisson’s equation on average. Nonetheless, it’s interesting that when starting from the relativistic theories
of refs. 11,39, we ﬁnd that the weak ﬁeld limit resembles the models of
Tilloy and Di´osi33, which is discontinuous in Φ, rather than the continuous model of Di´osi24. This is because24 allows for non-zero conjugate momentum πΦ with the kinetic energy of a different sign, while
in ref. 81, the momentum is set to zero via the constraint equations and
gauge ﬁxing of the lapse. The discontinuity then arises because we are
operating in the c → ∞ limit, while in ref. 33, the discontinuity arises due
to sourcing the Newtonian potential via a weak measurement process.
We refer the reader to ref. 81 for details.

Weak ﬁeld CQ master equations
Although the trade-off we derive does not depend on the particulars of the classical–quantum theory (provided it reproduces
Newtonian gravity in the classical limit), we give two concrete
examples for completeness. In ref. 30 we show that there are two
classes of classical-quantum dynamics, one which is continuous in
phase space, and one which has discrete jumps in phase space.
We will give examples of each. Although they are the weak ﬁeld
limit of Oppenheim11, it is worth stressing that taking the Newtonian limit entails certain coordinate choices and restrictions on
the metric. For example, here, we have restricted ourselves to
metrics of the form of Eq. (89). Any gauge ﬁxing of General
Relativity which is done before deriving the master equation, is

Nature Communications | (2023)14:7910

generally not equivalent to taking the master equations of
Oppenheim11, and then taking the appropriate limit81.

Continuous master equation
For the class of master equations with continuous back-reaction,
specifying that the ﬁrst moment on average satisﬁes Eq. (100) is
enough (up to drift terms which vanish under trace) to ensure the
master Equation includes a term


Z
∂ϱ
δϱ
δϱ
^
^
d3 x mðxÞ
+
≈ fH c ðΦÞ, ϱg  i½H 0ðmÞ , ϱ +
mðxÞ
∂t
δπ Φ δπ Φ
Z
2
δ
ðD ðΦ, π Φ ; x, yÞϱÞ
+
d3 xd3 y
δπ Φ ðxÞδπ Φ ðx 0 Þ 2
Z


1
^
^
½ϱ, mðyÞ
,
+
d3 xdy D0 ðΦ, x, x 0 Þ ½mðxÞ,
2

ð101Þ

where Hc is the purely classical gravity Hamiltonian. We have
taken the dynamics, i.e., the drift to be local in x, while we allow
for the decoherence and diffusion terms to have some range. In
this case, the evolution law is still local but correlations can be
created122. One can also add extra diffusion and decoherence into
Eq. (101) which we do not consider here since it only leads to
worse experimental bounds. However, adding additional diffusion in Φ will generally be required in order to impose the constraint πΦ ≈ 081. This master equation is close to the one
considered in ref. 24, where the decoherence and diffusion kernels are chosen to be the ones discussed in the second example
of Examples of Kernels saturating the decoherence diffusion
coupling constants trade-off. This is the weak ﬁeld limit of the
simplest realisation in ref. 11. The case where the diffusion is
spatially uncorrelated D2 ðx, yÞ = ϵðx  x 0 Þ a regulator which
approaches a scalar delta function correspondsp
toﬃﬃﬃﬃﬃﬃﬃﬃﬃ
the Newtonian
pﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ
limit of the diffusion term ϵðx  x 0 ÞfNðxÞ gðxÞ, f gðx 0 Þ, ϱgg.
Another
natural
diffusion
kernel
is
D2 ðx, yÞ =  D2 ð1 + Φðx 0 ÞÞΔx0 δðx, yÞ, which can be understood as the
Newtonian limit of the spatial diffeomorphism invariant kernel
discussed in the section “Diffeomorphism invariant kernel”.
One can supplement the kernel by some mechanism to control
the diffusion. For example, a friction term such as
F ðϱÞ = Df 21

R

pﬃﬃﬃﬃﬃﬃﬃﬃﬃ pﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ
dxdx 0 dyfNðxÞ gðxÞ, f gðx 0 Þϵðx  x 0 Þ, HðyÞgϱg:

ð102Þ

In the weak ﬁeld limit, this would add a term proportional to
Z
F ðϱÞ ≈

dxdx 0


δ 
π ðx 0 Þϱ
δπ Φ ðxÞ Φ

ð103Þ

to the master equation of Eq. (101). Such a term would break Lorentz
invariance since it sets a temperature scale, although this is not
necessarily a deal breaker, since it is believed by many that quantum
gravity is also likely to also have an anomaly. However, the friction
term is a modiﬁcation to D1(x), and if too large, could run afoul of
precision tests of General Relativity, such as the orbital decay of binary
pulsars.

Discrete master equation
An example of a discrete master equation satisfying Eq. (100) is
Z
∂ϱ
c2
≈ fH c ðΦÞ, ϱg  i½H 0ðmÞ , ϱ +
d3 x
∂t
_τ


" R
# ð104Þ


_τ
δ
dyϵðxyÞ 1 + 2ΦðyÞ
2ΦðxÞ
1
δπ Φ ðyÞ
y
c2
c2
1
ψðxÞϱψ ðxÞ  fmðxÞ, ϱg + ,
e
c2
2

with τ a dimensionless constant, and ^
mðxÞ = ψy ψ. We have here included ℏ and c to make it easier to compare with experiments. To
15

## PDF page 16

Article

https://doi.org/10.1038/s41467-023-43348-2

leading order, we could drop terms proportional to Φ(x)/c2 in both the
pﬃﬃﬃ
exponential and in N g ≈1  2Φ=c2 inside the integral over x. This
gives
∂ϱ
c2
≈ fH c ðΦÞ, ϱg  i½H ðmÞ
0 , ϱ +
∂t
_τ

Z

 R

_τ
1
dyϵðxyÞδπ δ ðyÞ
y
Φ ψðxÞϱψ ðxÞ 
fmðxÞ, ϱg + :
d x e c2
2
3

ð105Þ
These dynamical equations are supplemented with modiﬁed
constraint equations as outlined in ref. 37. In any case, the trade-off in
Eq. (31) is a statement independent of constraints and constraint preservation, at least in the weak ﬁeld limit.

Examples of Kernels saturating the decoherence diffusion coupling constants trade-off
In this section, we give examples of kernels satisfying the decoherence
diffusion coupling constant trade-off in Eq. (23). For any choice of
kernel, we can compute the degree of diffusion it induces in precision
mass measurements (see the section “Detecting gravitational diffusion”) and decoherence experiments (see the section “Decoherence
rates”) which allows us to rule out certain kernels experimentally.
Diffeomorphism invariance may single out having both D0(x, y) and
D2(x, y) approach delta functions at short distances39, but other alternatives may be possible.
As a ﬁrst example, we shall take the Lindbladian coupling to be
Gaussian, taking
Dαβ
0 ðx, yÞ =

λαβ r 30
g ðx, yÞ
m20 N

ð106Þ

where g N ðx, yÞ is a normalised Gaussian distribution. The mass m0 is a
reference mass, and we shall take it equal to the mass of the nucleons
which were considered in the section “Physical constraints on the
classicality of gravity”, meanwhile λαβ is a coupling constant that
determines the strength of the Lindbladian.
It should be noted that with this choice of smearing function,
the pure Lindbladian evolution appearing in Eq. (101) can be taken
to resemble the Lindbladian part of spontaneous collapse
models60,99,123–125, except here, there is no need to think about any adhoc ﬁeld, nor think of the collapse as being a physical process. Rather,
one necessarily gets decoherence of the wave function for free, via
gravitationally induced decoherence11,25,33,35,126
We now ﬁnd the diffusion kernel D2(x, y) using the coupling
constants trade-off in (23). For simplicity, we shall assume the trade-off
is saturated, and we will take the back-reaction to be local, so that
μα
br μα
ðDbr
1 Þi ðx, yÞ = ðD1 Þi ðxÞδðx, yÞ. In this case we ﬁnd
Dμν
2, ij ðx, yÞ =

μα
m2
1 br μα
ðD Þ ðxÞ 3 0 g 1
ðx, yÞðDbr*
1 Þi ðyÞ,
2 1 i
r0λ N

ð107Þ

where g 1
N ðx, yÞ is the kernel inverse of a normalised Gaussian
distribution.
It is shown in ref. 127, that the inverse distribution takes the form
g 1
N ðx, yÞ = Fðx, yÞg N ðx, yÞ,

ð108Þ

In total then, we arrive at the expression for the D2 which saturates
the bound
D2 ðx, yÞ =

μα
m2
1 br μα
ðD Þ ðxÞ 3 0 Fðx, yÞg N ðx, yÞðDbr*
1 Þi ðyÞ:
2 1 i
r0λ

ð110Þ

If we further take the back-reaction that of the Newtonian limit in
the
section
“Newtonian
limit
of
CQ
theory”
μα
1 0m π Φ
Þ
ðx,
yÞ
=
δ
δ
δðx,
yÞ
then
we
ﬁnd
the
D
which
saturates
the
ðDbr
2
1 i
i
2
bound is
D2 ðx, yÞ =

1 m20
Fðx, yÞg N ðx, yÞ:
8 r 30 λ

ð111Þ

Another example of a Lindbladian coupling which is familiar in the
literature is,
Dαβ
0 ðx, yÞ =

Dαβ
0
:
jx  yj

ð112Þ

For a single Lindblad operator, this is the coupling introduced in24
used to reproduce a CQ master equation of gravity with a decoherence
rate given by the Diosi–Penrose formula128–130. Here we consider the
special case where the x, y dependence of D0(x, y) is the same for all
α, β which need not hold in general. The fact that it gives the same
decoherence rate as Diosi–Penrose can be seen by plugging Eq. (112)
into the classical-quantum master equation in Eq. (101).
To invert the kernel in Eq. (112) we use the fact that




1 2
1
∇x
= δðx, yÞ,
4π
jx  yj

ð113Þ

from which one can immediately read of the generalised inverse
ðD1
0 Þαβ ðx, yÞ to be
ðD1
0 Þαβ ðx, yÞ =

ðD1
0 Þαβ
4π

∇2y ðδðx, yÞÞ,

ð114Þ

where ðD1
0 Þαβ are the matrix elements of the generalised inverse of D0.
As a consequence, we ﬁnd for this speciﬁc choice of kernel that the
diffusion matrix saturating the coupling constants bound in Eq. (31) is
Dμν
2, ij ðx, yÞ =

1
1 μα ðD0 Þαβ 2
∇y ðδðx, yÞÞDβν
D1, i ðxÞ
1, j ðyÞ,
4π
2

ð115Þ

where we have also assumed the back-reaction is local. Taking the
back-reaction to further be that of the Newtonian limit of Eq. (101)
μα
1 0m π Φ
δ i we ﬁnd
ðDbr
1 Þi ðxÞ = 2 δ
D2 ðx, yÞ =

1 ðD1
0 Þ 2
∇ ðδðx, yÞÞ:
8 4π y

ð116Þ

This diffusion kernel is argued for on the grounds of having the
ﬂuctuations satisfy a Poisson equation, in ref. 24.

Diffeomorphism invariant kernel

where


x  yi
,
cn ðr 0 ÞH 2n i
Fðx, yÞ =
r0
i=1 n=0
d X
N
Y

n

ð109Þ
2n

and the limit N → ∞ is taken. In Eq. (109) cn ðr 0 Þ = ð1Þ ðr2n0 Þ n! and d is the
spatial dimension, so that x = (x1, x2, …, xd).

Nature Communications | (2023)14:7910

Attempts to derive the constraint algebra of a generally covariant CQ
theory37 (and J. Oppenheim, “The constraints of a continuous realisation of post-quantum-classical gravity", manuscript in preparation),
motivates the spatial diffeomorphism invariant kernel
0
Dijkl
2 ðx, x Þ = 

1 pﬃﬃﬃﬃﬃﬃﬃﬃﬃ
D gðxÞNðxÞg ij g kl Δx0 δðx, x 0 Þ,
8

ð117Þ

16

## PDF page 17

Article

https://doi.org/10.1038/s41467-023-43348-2

where Δx is the Laplace–Beltrami operator. One can also consider the
full 3 + 1 kernel, via Δð4Þ δðx, x 0 Þδðt, t 0 Þ along with the associated Green’s
function of Δ(4) but this is irrelevant for the Newtonian limit. It is
however useful in removing the apparent asymmetry in the expressions below, since one must recall that the δðx, x 0 Þ is a scalar in the ﬁrst
coordinate and a tensor density in the second, and likewise δðt, t 0 Þ has
an implicit lapse Nðx 0 Þ in the second position. This kernel’s weak ﬁeld
limit is
ij kl

0
1
0
Dijkl
2 ðx, x Þ =  8 Dδ δ ð1 + ΦðxÞÞΔx 0 δðx, x Þ,

ð118Þ

which is close to that of Eq. (116), but with a correction term that turns
out to be important.
pﬃﬃﬃ
Using D1 ðx, x 0 Þ =  21 N g δðx, x 0 Þ, the Lindbladian kernel in
dimension d which saturates the trade-off for this diffusion kernel is
D0, ijkl ðx, x 0 Þ =

1
2

2d D

pﬃﬃﬃﬃﬃﬃﬃﬃﬃ
gðxÞNðx 0 Þg ij ðxÞg jk ðx 0 ÞGðx, x 0 Þ,

ð119Þ

with Gðx, x 0 Þ the Green’s function for −Δ. It is a density in the x 0 coordinate and a scalar in x. In the weak ﬁeld limit, and to 0th order in Φ(x),
this gives the Diosi–Penrose kernel, Eq. (112).
One could also consider the kernel
0
Dijkl
2 ðx, x Þ = 

1 pﬃﬃﬃﬃﬃﬃﬃﬃﬃ ij kl
D gðxÞg g Δx NðxÞδðx, x 0 Þ,
8

ð120Þ

which in the weak ﬁeld limit is
ij kl

0
1
0
Dijkl
2 ðx, x Þ =  8 Dδ δ ΔΦðxÞδðx, x Þ:

ð121Þ

A comment on divergences
The kernel examples given above give rise to divergent variance in the
classical degrees of freedom, since in both cases the diffusion coefﬁcient diverges when evaluated at the same point D2(x, x). Though we
do not have a general proof, this seems to be a general feature of the
coupling constant trade-off: for the examples where we can compute
the kernel inverse, at least one of D2(x, x) and D0(x, x) diverge. A
divergent D2(x, x) generally leads to a formally divergent classical
energy production, whilst a divergent Lindbladian coupling D0(x, x)
can lead to a divergent energy production in the matter degrees of
freedom. The latter is related to the BPS problem98 of anomalous
heating, although it isn’t necessarily equivalent since some kernels may
diverge and be well-behaved from the point of view of energy production. This is not an issue from a conceptual point of view, since the
only reason we expect energy to be conserved is due to Noether’s
theorem, and Noether’s theorem doesn’t apply when the evolution
isn’t unitary.
In the standard BPS problem, energy production in open
quantum ﬁeld theory can be made small by renormalizing the
Lindbladian coefﬁcient D0(x, y) appearing in the master equation.
Thus the problem is merely one akin to the hierarchy problem,
where we are required to introduce another energy scale. However, in the case of classical–quantum coupling, the coupling
constant trade-off tells us that we cannot re-normalise D0(x, y)
without affecting D2(x, y). In particular, tuning the diagonals
D0(x, x) to be arbitrarily small (large) has the effect of tuning
D2(x, x) to be arbitrarily (large) small: heuristically, one trades
energy production in the classical system with energy production
in the quantum system, and the relationship is ﬁxed by the tradeoff. On expectation, the total energy could be preserved, and the
back-reaction can even slow down the ﬂow of energy, but it’s
unclear if this is enough.

Nature Communications | (2023)14:7910

However, it is worth noting that while D2 ðx, x 0 Þ may appear
to diverge at a R single point as x ! x 0 , when integrated over
test functions,
dxdx 0 D2 ðx, x 0 Þf ðxÞf ðx 0 Þ is usually well-behaved.
The kernels discussed above have this property. When it comes
to physically relevant quantities, such as measuring the gravitational diffusion in tabletop experiments, it is the smeared wellbehaved quantity that is physically relevant. However, in cosmology, we typically take the constraint equation of General
Relativity to be exactly satisﬁed at each point, and so one
might imagine that π 2Φ ðxÞ, and hence D2(x, x) is the relevant
quantity (see the discussion in the section “Detecting gravitational diffusion”). However, one can set πΦ ≈ 0 via a gauge
freedom81. In GR, the counterpart to the π 2Φ kinetic term is
Gijklπijπkl(x), and it’s perhaps worth noting that this quantity is not
positive deﬁnite. It is also important to note that here, we have
taken the weak ﬁeld and c → ∞ limit of General Relativity. At short
distances when the diffusion becomes large, we expect this
approximation to break down. One possible method of studying
this problem rigorously would be through the regularisation
properties of the classical-quantum path integral which we
introduce in38,39.

Decoherence rates
In this section, Rwe relate decoherence rates to D0, and also to the
y
average hD0 i = dzTr½Dαβ
0 ðz; x, yÞLα ðxÞϱLβ ðyÞ. In particular, we shall
show that the decoherence rate of a mass in superposition, is given by
Eq. (131) in terms of the Lindblad operators and Dαβ
0 , and can be related
to the quantity 〈D0〉.
We consider the case of a quantum mass initially in a partially
decohered superposition of state jLi and jRi. We describe the
quantum state using creation and annihilation operators
ψ(x), ψ†(x) on a Fock space, related to the usual momentum-based
R
Fock operators as ψðxÞ = dpei~px~ap~. The mass density operator is
deﬁned via ^
mðxÞ = mψy ðxÞψðxÞ, where m is the mass of the particle.
We assume that the state remains well approximated by a state
with ﬁxed particle number, and the superposition can be taken to
be distributions centred around x = xL and x = xR with total mass
M,
i.e.,
for
a
one-particle
state
we
could
take
R 3
y
jL=Ri = d xf L=R ðxÞψ ðxÞj0i. We will take them to be well separated so that fL(x)fR(x) ≈ 0, and we take the separation distance to
be larger than the scale of the non-locality in D0(x, y). Mathemay
tically this means that hLjDαβ
0 ðz; x, yÞLβ ðyÞLα ðxÞjRi ≈ 0 for any local

operators Lα(x) and Lβ(y).
With this orthogonality condition, we can then (at least initially)
consider the joint quantum classical state restricted to the twodimensional Hilbert space of these two states so that the total
quantum-classical system can be written as

ϱðΦ, π Φ , tÞ =

uL ðΦ, π Φ , tÞ
?

αðΦ, π Φ , tÞ

α ðΦ, π Φ , tÞ uR ðΦ, π Φ , tÞ


,

ð122Þ

where uL(Φ, πΦ, t) and uR(Φ, πΦ, t) correspond to some subnormalised
probability distribution over the classical states of the
gravitational ﬁeld.
We deﬁne the total quantum state ρQ by integrating over the
classical degrees of freedom
Z
ρQ =

DΦDπ Φ ϱðΦ, π Φ , tÞ,

ð123Þ

and we shall relate 〈D0〉 appearing in the trade-off to the
decoherence rate of the off diagonals of ρQ. Integrating over
the classical phase space in Eq. (9), one ﬁnds the following expression
17

## PDF page 18

Article

https://doi.org/10.1038/s41467-023-43348-2

for the evolution of ρQ
∂ρQ
=
∂t

Z
DϕDπ Φ  i½HðΦ, π Φ Þ, ϱðΦ, π Φ Þ
Z
Z
h
y
dxdy Dαβ
+
DϕDπ Φ
0 ðΦ, π Φ ; x, yÞLα ðxÞϱðΦ, π Φ , tÞLβ ðyÞ

1
y
ðΦ,
π
;
x,
yÞfL
ðyÞL
ðxÞ,
ϱðΦ,
π
,
tÞg
:
 Dαβ
Φ
α
Φ
β
2 0
ð124Þ

Equation (129) already expresses the fact that the off-diagonal
terms will decay, and the particle will decohere at a rate determined by
the integrand of Eq. (129).
We can go slightly further when in the presence of a background
Newtonian potential which is dominant, such as the Earth’s Φb. The
Earth’s background potential dominates over small ﬂuctuations in Φ
due to the particles and we can approximate Eq. (129) by
1
ðx, yÞðhLjLyβ ðyÞLyβ ðyÞLα ðxÞjLi + hRjLyβ ðyÞLyβ ðyÞLα ðxÞjRiÞhLjρQ jRi,
 Dαβ
2 0
ð130Þ

∂ρ

In particular, one ﬁnds that the off-diagonals hLj ∂tQ jRi evolve in
part according to the commutator, and in part due to the Lindbladian
term
Z

Z
DϕDπ Φ

h
y
dxdy hLjDαβ
0 ðΦ, π Φ ; x, yÞLα ðxÞϱðΦ, π Φ , tÞLβ ðyÞjRi
 ð125Þ
1
y
 Dαβ
0 ðΦ, π Φ ; x, yÞhLjfLβ ðyÞLα ðxÞ, ϱðΦ, π Φ , tÞgjRi :
2

where the coupling Dαβ
0 ðx, yÞ depends on the background Newtonian
potential, but is otherwise phase-space independent. The result is to
exponentially decrease the coherence 〈L∣ρQ∣R〉 with a rate λ determined by
λ=

Care must be taken however, because both the quantum Hamiltonian and the Lindbladian coupling constants depend on the classical
degrees of freedom which are affected by the quantum degrees of
freedom, and thus the evolution of the quantum system is nonMarkovian in general.
We shall now study the two terms appearing in Eq. (125) separately, starting with the ﬁrst term. Since we assume that the state is
well approximated by a state with ﬁxed particle number then the
contributions to the ﬁrst term in Eq. (125) only come from
terms where Lα(x) and Lβ(y) have the same number of creation and
annihilation operators. To compute the expression, one
commutes through the creation operators to act on the hLj bra, and
picks up a term fL(x). Similarly, one commutes the annihilation
operators to the act on the jRi ket, and picks up a term fR(y). As a
consequence
αβ
y
hLjDαβ
0 ðΦ, π Φ ; x, yÞLα ðxÞϱðΦ, π Φ , tÞLβ ðyÞjRi ∼ D0 ðΦ, π Φ ; x, yÞf L ðxÞf R ðyÞ ≈ 0,



1
2

Z

Z
DϕDπ Φ

y
dxdyDαβ
0 ðΦ, π Φ ; x, yÞhLjfLβ ðyÞLα ðxÞ, ϱðΦ, π Φ , tÞgjRi,

ð127Þ
which is negative deﬁnite and acts to exponentially suppress the
coherence. To see this, note that expanding out ϱ(Φ, πΦ, t) in terms of
the approximate 2 dimensional Hilbert space
ϱðΦ, π Φ , tÞ = uL ðΦ, π Φ , tÞjLihLj + uR ðΦ, π Φ , tÞjRihRj

ð128Þ

Z

y
y
dxdyDαβ
0 ðx, yÞðhLjLβ ðyÞLα ðxÞjLi + hRjLβ ðyÞLα ðxÞjRiÞ:

ð131Þ

Let us now show that the 〈D0〉 term appearing in the trade-off (34)
is always less than (twice) this decoherence rate when in the presence
of a background potential. Speciﬁcally, we show that
Z

Z

hD0 i =

DΦDπ Φ

h
i
y
dxdyTr Dαβ
0 ðΦ, π Φ ; x, yÞLβ ðyÞLα ðxÞϱðΦ, π Φ Þ ≤ 2λ,
ð132Þ

where we assume that we are in the presence of a background
potential. To see this, we ﬁrst expand out the CQ state in terms of
Eq. (128) and use the fact that D0 has a range less than the separation of
the masses. We then arrive at the following expression for the left-hand
side of Eq. (132)
Z

Z
DΦDπ Φ

ð126Þ
where the last equality follows from the fact that we are taking the
masses to be well separated and the range of D0(x, y) is assumed to be
much less than the separation between the masses.
Hence, the evolution of the off-diagonals comes from the
(off-diagonals) of the unitary evolution and the second term in Eq.
(125), the so-called no-event term. The off-diagonals of the no-event
term is

1
2

y
y
dxdyDαβ
0 ðΦ, π Φ ; x, yÞðhLjLβ ðyÞLα ðxÞjLiuL ðΦ, π Φ , tÞ + hRjLβ ðyÞLα ðxÞjRiuR ðΦ, π Φ , tÞÞ,

ð133Þ
In the presence of a background potential, this dominates the
contribution to the decoherence and we are left with
Z

y
y
dxdyDαβ
0 ðx, yÞðhLjLβ ðyÞLα ðxÞjLihLjρQ jLi + hRjLβ ðyÞLα ðxÞjRihRjρQ jRiÞ:

ð134Þ
Due to the positivity of the CQ density matrix 〈L∣ρQ∣L〉 and 〈R∣ρQ∣R〉
must both be positive. Furthermore, they must sum to one due to
normalisation, from which Eq. (131) directly follows.
It is also important to note that though λ is the decoherence rate
of a particle in superposition of L/R states, the bound (132) holds even
for fully decohered masses in any mixture of jLihLj, jRihRj states. This
can be seen directly from (133) which depends only on uL, uR.

Decoherence rate examples

In this section, we give an explicit example of a decoherence rate
calculation. Importantly, we see that in general, the decoherence rate
and using the fact that the range of D0(x, y) is much less than the can depend on the probability density. This suggests that the terms
separation between the left and right masses, we can write the off- appearing in the trade-off relation will need to depend on expectation
values such as the expectation value of the mass at a point x, rather
diagonals of the no-event term as
than a stronger bound in terms of the mass density. This is perhaps not
Z


1
surprising, since the decoherence rate itself can be thought of as an
y
y

DΦDπDαβ
0 ðΦ, π Φ ; x, yÞ hLjLβ ðyÞLα ðxÞjLi + hRjLβ ðyÞLα ðxÞjRi hLjϱðΦ, π Φ ÞjRi:
2
expectation value, being related to the average time it takes for offð129Þ diagonal elements to decay. In conclusion, this motivates us to
+ αðΦ, π Φ , tÞjLihRj + α * ðΦ, π Φ , tÞjRihLj,

Nature Communications | (2023)14:7910

18

## PDF page 19

Article

https://doi.org/10.1038/s41467-023-43348-2

advocate for the volume of the wave packet to be included in the ﬁgure
of merit in future interference experiments.
We take the Newtonian limit master equation deﬁned by Eq. (101).
We ignore the unitary part of the evolution, since it will not directly
contribute to the decoherence rate, and can be small for a free particle
in superposition. From Eq. (101) we ﬁnd the relevant evolution for the
quantum state ρQ, obtained by integrating over the classical degrees of
freedom to be
∂ρQ 1
=
∂t
2

Z



mðxÞ, ½ρQ , ^
mðyÞ :
d3 xd3 yD0 ðx, yÞ ½ ^

ð135Þ

We now compute the off-diagonal elements for a particle in
superposition of orthogonal jLi, jRi states


Z
∂ρ 
d3 xd3 yD0 ðx, yÞ ðmL ðxÞ  mR ðxÞÞðmL ðyÞ  mR ðyÞÞhLjρQ jRi:
L Q R = 
∂t

ð136Þ
where mL ðxÞ ≈ hLj ^
mðxÞjLi and similarly for the right state. We see that
the off-diagonals decay exponentially with a rate determined by
Z
λ=

d3 xd3 yD0 ðx, yÞðmL ðxÞ  mR ðxÞÞðmL ðyÞ  mR ðyÞÞ:

ð137Þ

In the main body, and the previous subsection, we have assumed
that the superposition of the particle is much less than the typical scale
of D0(x, y). In this example, this means that we take the particles sufﬁciently separated so that we can approximate D0(x, y)mL(x)mR(y) ≈ 0,
in which case Eq. (137) is precisely the decoherence rate calculated in
^
Eq. (131) with LðxÞ = mðxÞ,
as is to be expected.
The natural decoherence kernel from the point of view of diffeomorphism invariance is D0(x, y) = D0δ(x, y), in which case for a
particle of mass M, and uniform wave-packet volume V, Eq. (137) gives
λ = 2D0M2/V.
As another example, we can take D0 ðx, x 0 Þ to be the Diosi–Penrose
D0
, so that the offdecoherence kernel deﬁned via D0 ðx, yÞ = jxyj
diagonals decay exponentially with a rate proportional to the
Diosi–Penrose decoherence rate
Z
λ=

d3 xd3 y

D0
ðm ðxÞ  mR ðxÞÞðmL ðyÞ  mR ðyÞÞ:
jx  yj L

ð138Þ

(140), which gives an extra factor of N relative to the single particle
2
case λ = 6D05RNM .
Both Eqs. (138) and (139) depend on the probability density of the
mass. In particular, taking the probability density to be arbitrarily
peaked, one ﬁnds that the decoherence rate also diverges. This has to
be the case: recall from the section “A Trade-off between decoherence
and diffusion” that if one considers a particle in a superposition of two
arbitrarily peaked probability densities, then there can be an arbitrarily
large response in the Newtonian potential around those points. As a
consequence, for such states, the decoherence must occur arbitrarily
fast, or there must be an arbitrarily large amount of diffusion to cover
up the back-reaction and maintain coherence. For the continuous
master equation, such as that of Eq. (101) this diffusion must also occur
throughout space, although it can depend on the gravitational degrees
of freedom. Since divergent energy production throughout space is
clearly unphysical, it must be the case that the decoherence rate must
also depend on the expected mass density, as is the case for this
example. This argument allows us to rule out continuous master
equations that have pure Lindbladian terms that predict decoherence
rates which remain ﬁnite as the mass density becomes arbitrarily
peaked since the coupling constant trade-off will demand that an
inﬁnite amount of diffusion is required to cover up the back-reaction
and maintain coherence. This is the case for the class of models with
CSL-type Lindbladian couplings which are phase space independent,
for example in Eq. (106).

Detecting gravitational diffusion
In this section, we show how the diffusion induced on the Newtonian
potential can be measured experimentally. metric leads to observable
effects, such as variations in the accelerations involved in torsion
experiments and stochastic wave production in cosmology. As shown
in the main body of the text, in the non-relativistic limit, c → ∞, the CQ
dynamics can be approximated by sourcing the Newtonian potential
by a random mass term, and in order to maintain the coherence of any
mass is superposition, there must be noise in the Newtonian potential
such that we cannot tell which element of the superposition the particle will be in
mÞ Jðx, tÞ,
∇2 Φ = 4πG½mðx, tÞ + uðΦ, ^
with
Em ½ Jðx, tÞ = 0, Em ½uJðx, tÞuJðy, t 0 Þ = 2hD2 ðx, y, ΦÞiδðt, t 0 Þ,

In this example, taking the superposition to be sufﬁciently sepa0
≈ 0 in comparison with
rated means that we are approximating jx Dx
L
Rj
the rest of the terms appearing in Eq. (138). We are then left with
Z
λ=

3

3

d xd y

D0
ðm ðxÞmL ðyÞ + mR ðxÞmR ðyÞÞ,
jx  yj L

ð139Þ

which for spherical distributions of radius R and total mass M is proportional to the average gravitational self-energy of each mass
2
0M
.
distribution λ = 6D5R
For a composite particle of mass M, made up of N constituents
each of radius R, the mass density will be represented by a sum over all
of the particles m(x) = ∑imi(x). The decoherence rate is given by
Z
λ=

!
X
X
D0
m ðxÞmL, j ðyÞ +
mR, i ðxÞmR, j ðyÞ :
d xd y
jx  yj i, j L, i
i, j
3

3

ð140Þ
Since the cross terms involving i, j are suppressed by a factor of
inter-atomic scales, to leading order the contribution to the decoherence rate is lower bounded by the i = j component of the sums in Eq.

Nature Communications | (2023)14:7910

ð141Þ

ð142Þ

y
where hD2 ðx, y, ΦÞi :¼ Tr½Dμν
2 ðx, y, Φb ÞLμ ðxÞρLν ðyÞ and ρ is the quantum state for the decohered mass density. The diffusion coefﬁcient in
Eq. (142) is chosen in order for the dynamics to have the same
moments as the CQ master equation (4). The solution to Eq. (141),
having absorbed u into J is given by

Z
Φðt, xÞ =  G

d x0
3

½mðx 0 , tÞ  uðΦ, ^
mÞJðx 0 , tÞ
,
0
jx  x j

ð143Þ

where the statistics of J are described by Eq. (142). A formal treatment
of solutions to non-linear stochastic integrals of the form Eq. (141) can
be found in ref. 82.
One can also verify this behaviour in speciﬁc cases. In the continuous model of the section “Continuous master equation”, the noise
is taken to be Gaussian, and this, as well as the evolution of the
quantum state, is what determines the diffusion in Eq. (143). For the
class of discrete models, the higher order moments such as
Em ½Jðx, tÞJðy, t 0 ÞJðz, t 00 Þ are suppressed by an order parameter11,26,37 and
whenever this is true we expect we can approximate the dynamics of
the Newtonian potential by a Gaussian process. Whether this is the
case or not, it is the second-order moment that enters into our
19

## PDF page 20

Article

https://doi.org/10.1038/s41467-023-43348-2

discussion of the variance here. As such, for minimally coupled theories, the Newtonian potential will appear to be sourced by a random
mass distribution.
In the discrete case, a precise understanding of the effects of the
diffusion beyond the Gaussian approximation involves solving the full
classical-quantum dynamics, perhaps using the methods of Oppenheim et al.26. In Eq. (141) we are also taking the time scale of the diffusion to be faster than the dynamics of the matter distribution.
Likewise for the decoherence—we showed in the “Methods” subsection
“Decoherence rates” for continuous models the evolution of the
quantum state acts to decohere it into a mass density eigenbasis m(x).
One could of course also include the quantum state evolution in a
simulation of full CQ dynamics, but this is beyond the scope of the
current work.
Note that if the moments of the noise process are Galilean
invariant, then the theory given by Eq. (141) is Galilean invariant as we
would expect in the Newtonian limit. One can further derive Eq. (141)
from manifestly diffeomorphism invariant theories81, such as those of
refs. 39,131.

Table-top experiments
In this section we estimate the variation in force which would be seen
in table-top experiments which bounds the diffusion of classical theories of gravity from above, giving a squeezed bound on D2 due to
lower bounds on diffusion arising from coherence experiments. We do
this for dynamics in Eq. (141), but the methodology is general and
could also be used in a full simulation of CQ dynamics.
The variation in force induced on a composite mass is found via
!
F tot = 

Z

d3 xmðxÞ∇Φ:

ð144Þ

Using the solution in Eq. (143), the total force can be written
!
F tot =  G

Z

d3 xd3 x 0 mðxÞ

! !0
ðx  x Þ
½mðx 0 , tÞ  Jðx 0 , tÞ:
jx  x 0 j3

ð145Þ

In reality, we measure time-averaged force by measuring timeaveraged
R ΔT accelerations over the time resolution of the experiment
1
ΔT ΔT
0 dtF tot . The total variation in the force’s time-averaged magnitude. The full covariance matrix for various kernels in the Newtonian
limit is given in (J. Oppenheim and A. Russo, manuscript in prepara!
!
tion), σ 2F :¼ F tot  F tot can be written as
σ 2F =

1
2G2
ΔT

Z

! !0 ! !0
ðx  x Þð y  y Þ
3
3
3
3
d xd yd x 0 d y0 mðxÞmðyÞ
hD2 ðx 0 , y0 , ΦÞi:
jx  x 0 j3 jy  y0 j3

This is true for the kernels with functional dependence of the form
D2 ~ Φn, D2 ~ ∇ Φ, though the approximation does not hold for all kernels, for example, D2 ~ ∇2Φ which creates diffusion only where there is
the mass density. We hereby shall only consider diffusion kernels
D2(x, y, Φb) where the background potential is dominant, leaving more
general considerations for future work.
For local translation invariant dynamics for which the background
Newtonian potential is dominant, for example, D2 ~ Φn, we have
〈D2(x, y, Φb)〉 = 〈D2(Φb)〉δ(x, y) and we arrive at the expression for the
total variation in time-averaged force
σ 2F =

2G2 X
ΔT ij

Z

d3 xd3 yd3 x 0 mi ðxÞmj ðyÞ

ð147Þ
To leading order, the integral in Eq. (147) is dominated by the self
variation term where i = j, since nuclear scales 10−15 m dominate over
P
P
inter-atomic scales 10−9 m, so that E½ ij F i F j  ∼ i E½F 2i . Approximating the mass density of the atoms as coming from their nucleus, and
taking them to be spheres of constant density ρ with radius rN and mass
mN, we ﬁnd that the integral in Eq. (147) is approximately
σ 2F ∼

NG2 ρ2 r 2N
ΔT

Nature Communications | (2023)14:7910

Z

d3 x 0 hD2 ðΦb Þi:

ð148Þ

For the class of continuous dynamics 〈D2(Φb)〉 = D2(Φb), since the
diffusion is not associated with any Lindblad operators. If there is noise
everywhere throughout space, then the integral in Eq. (148) diverges
and gives evidence that continuous CQ theories with noise everywhere
should be ruled out.
As such, we expect that continuous CQ theory must contain nonlinear terms proportional to the Newtonian potential appearing in Eq.
R
(141), in which case we can approximate dx 0 D2 by VbD2 where Vb is
the volume of the region over which the background Newtonian
potential is signiﬁcant. In total then, we ﬁnd for continuous local CQ
dynamics
σ 2F ∼

D2 NG2 ρ2 r 2N V b
:
ΔT

ð149Þ

From this, we can
calculate D2 in terms of the total variance of the
σ2
acceleration σ 2a = m2F to get a lower bound
tot

D2 ≤

σ 2a Nr 4N ΔT

ð146Þ
We shall use Eq. (146) to provide an upper bound on coupling
constants of CQ theories for different choices of kernels D2 ðx 0 , y0 , ΦÞ.
Given a choice of functional form of the kernel, all that remains is the
strength of the diffusion coupling, which for the translation invariant
kernels we consider here takes the form of a single coupling constant
D2. We take D2 to be a dimension-full quantity with units kg2 sm−3 which
characterises the rate of diffusion for the conjugate momenta of the
Newtonian potential.
For a composite mass, we can approximate the mass density by
summing over N individual atoms of mass density mi(x), m(x) = ∑imi(x).
P!
!
!
The total force is the given by F tot = i F i , where F i is the force on
R
!
each individual atom F i =  V dxmi ðxÞ∇ΦðxÞ, and the total variation
P
P
of force is then σ 2F = E½ ij F i F j   E½ i F i 2 .
In general, the squeeze will depend on the functional choice of
D2(x, y, Φ) on the Newtonian potential. As mentioned in the main body,
in the presence of a large background potential Φb, such as that of the
Earth’s, we will often be able to approximate D2(x, y, Φ) = D2(x, y, Φb).

! !0 ! !0
ðx  x Þð y  x Þ
hD2 ðx 0 , Φb Þi:
jx  x 0 j3 jy  x 0 j3

V b G2

:

ð150Þ

Standard Cavendish type classical torsion experiments measure
accelerations of the order 10−7 m s−2, and we can take the time over
which the acceleration is averaged to be that of minutes ΔT ~ 102 s, so a
very conservative bound is σa ~ 10−7 m s−2, whilst N will be N ~ 1026 and
rN ~ 10−15 m. We take the background Newtonian potential to be that of
the Earth and we (conservatively) take Vb to be V b ∼ r 2E h ∼ 1015 m3
where rE is the Earth’s radius and h is the atmospheric height. We see
that this bounds D2 from above by D2 ≤ 10−41 kg2 sm−3.
On the other hand, D2 is bounded from below from interferometry
experiments which bound the decoherence rate. From Eq. (137) and the
coupling constant trade-off, for the kernel D2(x, y) = D2δ(x, y) we see
(ignoring constant factors) that the decoherence rate is found to be
λ∼

N λ M 2λ
,
V λ D2

ð151Þ

where Mλ is the mass of a composite particle in the interferometry
experiment, which is made up of Nλ particles, each with volume Vλ. This
20

## PDF page 21

Article

https://doi.org/10.1038/s41467-023-43348-2

gives rise to the squeeze
σ 2a Nr 4N ΔT
V bG

2

≥ D2 ≥

N λ M 2λ
:
V λλ

ð152Þ

Using the numbers from ref. 59, with Mλ ~ 10−24 kg, Nλ ~ 103, and
Vλ ~ 10−1510−1510−7 m3 = 10−37 m3, λ ~ 101 s−1 we ﬁnd that D2 ≥ 10−9 kg2 sm−3.
This suggests that the D2(x, y) = D2δ(x, y) kernel for classical gravity is
already ruled out by experiment.
For the local discrete models, such as that of Eq. (104), the theory
is less constrained due to the
dependence of the diffusion on the mass
3
l
density. In this case hD2 ðΦb Þi = mP D2 ðΦb ÞmðxÞ, where the factors of
P
Planck length and Planck mass are to ensure that D2(Φb) has the
required units. We arrive at the upper bound for D2
σ 2a Nr 4N ΔTmP
3

mN G2 l P

≥ D2 :

ð153Þ

Meanwhile, from Eq. (131), and coupling constant trade-off (30)
the decoherence rate for local discreet jumping models goes as

In general then, we expect that by simulating full CQ dynamics
satisfying the decoherence diffusion trade-off we will be able to
squeeze D2 from above and below. We bound D2 from above by
studying the effects of diffusion on gravitational experiments, and we
bound D2 from below using the coupling constant trade-off and
coherence experiments lower bounding the decoherence rate. As we
have seen in this section, it appears that classes of continuous CQ
hybrid theories of gravity, including models without spatial correlations, are already experimentally ruled out, whilst others, such as the
kernels in subsection “Diffeomorphism invariant kernel” require
stronger bounds from both gravitational and coherence experiments.
We have been very conservative in our estimates, and so we expect a
more thourough analysis will tighten the bounds by orders of
magnitute.

References
1.
2.

λ ∼ M3λ mP , which gives rise to the lower bound for D2. From this, we

3.

arrive at the squeeze

4.

l P D2

σ 2a Nr 4N ΔT

3

ð154Þ

5.

and plugging in the numbers we ﬁnd the bound given by Eq. (46) which
gives rise 3to the squeeze for local discrete modl
els 101 kgs ≥ mP D2 ≥ 1025 kgs.
P
We can also consider other diffusion kernels, for example, that of
Eq. (118). In this case, for continuous dynamics, we have that
2
hD2 ðx, yÞi =  l P D2 ðΦb Þ∇2 δðx, yÞ. The Lindbladian kernel saturating the
coupling constants trade-off at zeroeth order in Φ(x), is the
0 ðΦb Þ
, as we saw in the section
Diosi–Penrose kernel D0 ðx, y, Φb Þ = Djxyj
“Examples of Kernels saturating the decoherence diffusion coupling
constants trade-off”. Approximating the masses as spheres of constant
density we ﬁnd from a substitution of the kernel into Eq. (146) that the
variation in time-averaged force is given by

6.

2

mN G

l D
M
≥ P 2 ≥ λ,
mP
λ

2
l G2 m2N ND2
:
σ 2F ∼ P
ΔTr 3N

ð155Þ

We therefore ﬁnd a lower bound for D2 in terms of the variation in
acceleration
ΔTl P σ 2a Nr 3N
G2

8.

9.

10.
11.
12.

13.

2

D2 ≤

7.

,

ð156Þ
14.

which for classical torsion experiments σa ~ 10−7 m s−2, T ~ 102 s, N ~ 1026
2
and rN ~ 10−15 m gives D2 l p ≤ 109 kg m1 . On the other hand, for this
kernel the decoherence rate can be calculated via Eq. (139)

16.

NM 2
λ∼ 2 λ ,
l P D2 Rλ

17.

ð157Þ

15.

which gives the squeeze on D2
18.

ΔTσ 2a Nr 3N
G2

N M2
2
≥ l P D2 ≥ λ λ :
Rλ λ

ð158Þ

For the numbers used in the main body of the
text59Mλ ~ 10−24 kg, Nλ ~ 103, Rλ ~ V1/3 = 10−12 m, λ ~ 101 s,
this
yields
2
1
D2 l P ≥ 1035 kg m and so this model is not ruled out by experiment.
Nature Communications | (2023)14:7910

19.
20.
21.

DeWitt, C. M. & Rickles, D. The Role of Gravitation in Physics: Report
from the 1957 Chapel Hill Conference, Vol. 5 (epubli, 2011).
Feynman, R. P. In Feynman Lectures on Gravitation (eds Morinigo,
F. B., Wagner, W. G. & Hatﬁeld, B.) 10–11 (1996).
Aharonov, Y. & Rohrlich, D. Quantum Paradoxes: Quantum Theory
for the Perplexed 212–213 (Wiley-VCH, 2003).
Eppley, K. & Hannah, E. The necessity of quantizing the gravitational ﬁeld. Found. Phys. 7, 51 (1977).
Unruh, W. G. Steps towards a quantum theory of gravity. In
Quantum Theory of Gravity: Essays in honor of the 60th birthday
of Bryce S. DeWitt (ed Christensen, S. M.) (Adam Hilger Ltd., 1984).
Carlip, S. Is quantum gravity necessary? Class. Quantum Gravity
25, 154010 (2008).
Mari, A., De Palma, G. & Giovannetti, V. Experiments testing
macroscopic quantum superpositions must be slow. Sci. Rep. 6,
22777 (2016).
Baym, G. & Ozawa, T. Two-slit diffraction with highly charged
particles: Niels Bohr’s consistency argument that the electromagnetic ﬁeld must be quantized. Proc. Natl Acad. Sci. USA 106,
3035 (2009).
Belenchia, A. et al. Quantum superposition of massive objects and
the quantization of gravity. Phys. Rev. D 98, (2018) https://doi.org/
10.1103/physrevd.98.126009.
Kent, A. Simple refutation of the Eppleyhannah argument. Class.
Quantum Gravity 35, 245008 (2018).
Oppenheim, J. A post-quantum theory of classical gravity?.
arXiv:1811.03116 [hep-th] (2018).
Rydving, E., Aurell, E. & Pikovski, I. Do gedanken experiments
compel quantization of gravity? Phys. Rev. D 104, 086024
(2021).
Aleksandrov, I. & Naturf, Z. 36a, 902 (1981); a. anderson. Phys. Rev.
Lett 74, 621 (1995).
Kapral, R. Progress in the theory of mixed quantum-classical
dynamics. Annu. Rev. Phys. Chem. 57, 129–157 (2006).
Boucher, W. & Traschen, J. Semiclassical physics and quantum
ﬂuctuations. Phys. Rev. D 37, 3522 (1988).
Diósi, L., Gisin, N. & Strunz, W. T. Quantum approach to
coupling classical and quantum dynamics. Phys. Rev. A 61,
022108 (2000).
Sato, I. An attempt to unite the quantum theory of wave ﬁeld with
the theory of general relativity. Sci. Rep. Tohoku Univ. 1st ser. Phys.
Chem. Astron. 33, 30 (1950).
Møller, C. et al. Les théories relativistes de la gravitation. In Colloques Internationaux CNRS Vol. 91 (1962).
Rosenfeld, L. On quantization of ﬁelds. Nucl. Phys. 40, 353 (1963).
Page, D. N. & Geilker, C. Indirect evidence for quantum gravity.
Phys. Rev. Lett. 47, 979 (1981).
Blanchard, P. & Jadczyk, A. Event-enhanced quantum theory and
piecewise deterministic dynamics. Ann. Phys. 507, 583 (1995).
21

## PDF page 22

Article
22.
23.
24.
25.

26.

27.
28.

29.
30.

31.
32.

33.

34.

35.
36.

37.
38.
39.

40.

41.
42.
43.
44.
45.
46.

Diosi, L. Quantum dynamics with two Planck constants and the
semiclassical limit. arXiv:quant-ph/9503023 [quant-ph] (1995).
Alicki, R. & Kryszewski, S. Completely positive Bloch–Boltzmann
equations. Phys. Rev. A 68, 013809 (2003).
Diósi, L. The gravity-related decoherence master equation from
hybrid dynamics. J. Phys.-Conf. Ser. 306, 012006 (2011).
Poulin, D. & Preskill, J. Information loss in quantum ﬁeld theories.
Front. Quantum Inf. Phys. KITP https://online.kitp.ucsb.edu/
online/qinfo_c17/poulin/ (2017).
Oppenheim, J., Sparaciari, C., Šoda, B., & Weller-Davies, Z.
Objective trajectories in hybrid classical-quantum dynamics.
Quantum 7, 891 (2023).
Layton, I., Oppenheim, J. & Weller-Davies, Z. A healthier
semi-classical dynamics. arxiv2208.11722 (2022).
Gorini, V., Kossakowski, A. & Sudarshan, E. C. G. Completely
positive dynamical semigroups of N-level systems. J. Math. Phys.
17, 821 (1976).
Lindblad, G. On the generators of quantum dynamical semigroups. Commun. Math. Phys. 48, 119 (1976).
Oppenheim, J., Sparaciari, C., Šoda, B. & Weller-Davies, Z. The two
classes of hybrid classical–quantum dynamics. arXiv:2203.01332
[quant-ph] (2022).
Kafri, D., Taylor, J. M. & Milburn, G. A classical channel model for
gravitational decoherence. New J. Phys. 16, 065020 (2014).
Kafri, D., Milburn, G. J. & Taylor, J. M. Bounds on quantum
communication via Newtonian gravity. N. J. Phys. 17, 015006
(2015).
Tilloy, A. & Diósi, L. Sourcing semiclassical gravity from spontaneously localized quantum matter. Phys. Rev. D 93, 024026
(2016).
Tilloy, A. & Diósi, L. On gkls dynamics for local operations and
classical communication. Open Syst. Inf. Dyn. 24, 1740020
(2017).
Tilloy, A. & Diósi, L. Principle of least decoherence for Newtonian
semiclassical gravity. Phys. Rev. D 96, 104045 (2017).
Arnowitt, R., Deser, S. & Misner, C. W. Republication of: the
dynamics of general relativity. Gen. Relativ. Gravit. 40, 1997
(2008).
Oppenheim, J., Weller-Davies, Z. The constraints of post-quantum
classical gravity. JHEP. 2022, 80 (2022).
Oppenheim, J. & Weller-Davies, Z. Path integrals for classicalquantum dynamics. arXiv:2301.04677 (2023).
Oppenheim, J. & Weller-Davies, Z. Covariant path integrals
for quantum ﬁelds back-reacting on classical space–time.
arXiv:2302.07283 (2023).
Bohr, N. & Rosenfeld, L. On the question of the measurability of
electromagnetic ﬁeld quantities. In Quantum Theory and Measurement (eds Wheeler, J. A. & Wojciech H. Zurek, W. H.). Translated by Aage Petersen. Originally published as “Zur Frage der
Messbarkeit der Elektromagnetischen Feldgr6ssen" 479–522
(Mat.-fys. Medd Dan. Vid Selsk. 12). (Princeton University Press,
Princeton, [1933]
1983).
DeWitt, B. S. Deﬁnition of commutators via the uncertainty
principle. J. Math. Phys. 3, 619 (1962).
Gisin, N. Stochastic quantum dynamics and relativity. Helv. Phys.
Acta 62, 363 (1989).
Caro, J. & Salcedo, L. Impediments to mixing classical and quantum dynamics. Phys. Rev. A 60, 842 (1999).
Salcedo, L. Absence of classical and quantum mixing. Phys. Rev. A
54, 3657 (1996).
Sahoo, D. Mixing quantum and classical mechanics and uniqueness of Planck’s constant. J. Phys. A: Math. Gen. 37, 997 (2004).
Terno, D. R. Inconsistency of quantumclassical dynamics, and
what it implies. Found. Phys. 36, 102 (2006).

Nature Communications | (2023)14:7910

https://doi.org/10.1038/s41467-023-43348-2
47.

48.
49.
50.
51.

52.
53.

54.

55.
56.

57.
58.

59.
60.
61.

62.

63.

64.
65.
66.
67.

68.

69.

70.

71.

Barceló, C., Carballo-Rubio, R., Garay, L. J. & Gómez-Escalante, R.
Hybrid classical-quantum formulations ask for hybrid notions.
Phys. Rev. A 86, 042120 (2012).
Marletto, C. & Vedral, V. Why we need to quantise everything,
including gravity. npj Quantum Inf. 3, 29 (2017).
Cavendish, H. Xxi experiments to determine the density of the
earth. Philos.Trans. R. Soc. Lond. 88, 469-526 (1798).
Luther, G. G. & Towler, W. R. Redetermination of the Newtonian
gravitational constant g. Phys. Rev. Lett. 48, 121 (1982).
Gundlach, J. H. & Merkowitz, S. M. Measurement of Newton’s
constant using a torsion balance with angular acceleration feedback. Phys. Rev. Lett. 85, 2869 (2000).
Quinn, T. Measuring big g. Nature 408, 919 (2000).
Gillies, G. & Unnikrishnan, C. The attracting masses in measurements of g: an overview of physical characteristics and performance. Philos. Trans. R. Soc. A: Math. Phys. Eng. Sci. 372,
20140022 (2014).
Rothleitner, C. & Schlamminger, S. Invited review article: measurements of the Newtonian constant of gravitation, g. Rev. Sci.
Instrum. 88, 111101 (2017).
Arndt, M. et al. Wave–particle duality of c60 molecules. Nature
401, 680 (1999).
Nimmrichter, S., Hornberger, K., Haslinger, P. & Arndt, M. Testing
spontaneous localization theories with matter-wave interferometry. Phys. Rev. A 83, 043621 (2011).
Juffmann, T. et al. Real-time single-molecule imaging of quantum
interference. Nat. Nanotechnol. 7, 297 (2012).
Juffmann, T., Nimmrichter, S., Arndt, M., Gleiter, H. & Hornberger,
K. New prospects for de Broglie interferometry. Found. Phys. 42,
98 (2012).
Gerlich, S. et al. Quantum interference of large organic molecules.
Nat. Commun. 2, 263 (2011).
Bassi, A. & Ghirardi, G. Dynamical reduction models. Phys. Rep.
379, 257–426 (2003).
Westphal, T., Hepach, H., Pfaff, J. et al. Measurement of gravitational coupling between millimetre-sized masses. Nature 591,
225–228 (2021).
Schmöle, J., Dragosits, M., Hepach, H. & Aspelmeyer, M. A
micromechanical proof-of-principle experiment for measuring the
gravitational force of milligram masses. Class. Quantum Gravity
33, 125031 (2016).
Lee, J. G., Adelberger, E. G., Cook, T. S., Fleischer, S. M. & Heckel,
B. R. New test of the gravitational 1/r2 law at separations down to
52 μm. Phys. Rev. Lett. 124, 101101 (2020).
Kafri, D. & Taylor, J. M. A noise inequality for classical forces.
arXiv:1311.4558 [quant-ph] (2013).
Kafri, D., Milburn, G. & Taylor, J. Bounds on quantum communication via Newtonian gravity. N. J. Phys. 17, 015006 (2015).
Bose, S. et al. Spin entanglement witness for quantum gravity.
Phys. Rev. Lett. 119, 240401 (2017).
Marletto, C. & Vedral, V. Gravitationally induced entanglement
between two massive particles is sufﬁcient evidence of quantum
effects in gravity. Phys. Rev. Lett. 119, 240402 (2017).
Marshman, R. J., Mazumdar, A. & Bose, S. Locality and entanglement in table-top testing of the quantum nature of linearized
gravity. Phys. Rev. A 101, https://doi.org/10.1103/physreva.101.
052110 (2020).
Pedernales, J. S., Streltsov, K., & Plenio, M. B. (2022). Enhancing
Gravitational Interaction between Quantum Systems by a Massive
Mediator. Phys. Rev. Lett. 128, 110401 (2022).
Carney, D., Müller, H., & Taylor, J. M. Using an Atom Interferometer
to Infer Gravitational Entanglement Generation. PRX Quantum 2,
030330 (2021).
Kent, A. & Pitala-Garca, D. Testing the nonclassicality of spacetime: What can we learn from Bellbose et al.-Marletto-Vedral

22

## PDF page 23

Article

72.
73.

74.
75.
76.
77.
78.
79.

80.
81.

82.
83.

84.

85.

86.

87.
88.

89.

90.

91.

92.

93.
94.
95.
96.

experiments? Phys. Rev. D 104, https://doi.org/10.1103/physrevd.
104.126030 (2021).
Christodoulou, M. et al. Locally mediated entanglement through
gravity from ﬁrst principles. Phys. Rev. Lett. 130, 100202 (2023).
Danielson, D. L., Satishchandran, G. & Wald, R. M. gravitationally
mediated entanglement: Newtonian ﬁeld vs. gravitons. Phys. Rev.
D 105, 086001 (2022).
Lami, L., Pedernales, J. S. & Plenio, M. B. Testing the quantumness
of gravity without entanglement. arXiv:2302.03075 (2023).
Kraus, K. Complementary observables and uncertainty relations.
Phys. Rev. D 35, 3070 (1987).
Kramers, H. A. Brownian motion in a ﬁeld of force and the diffusion
model of chemical reactions. Physica 7, 284 (1940).
Moyal, J. Stochastic processes and statistical physics. J. R. Stat.
Soc. Ser. B (Methodological) 11, 150 (1949).
Layton, I., Oppenheim, J. & Weller-Davies, Z. A healthier semiclassical dynamics. arXiv:2208.11722 [quant-ph] (2022).
Feynman, R. & Vernon, F. The theory of a general quantum system
interacting with a linear dissipative system. Ann. Phys. 281,
547 (2000).
Breuer, H.-P. & Petruccione, F. et al. The Theory of Open Quantum
Systems (Oxford University Press on Demand, 2002).
Layton, I., Oppenheim, J., Russo, A. & Weller-Davies, Z. The weak
ﬁeld limit of quantum matter back-reacting on classical spacetime. J. High Energy Phys. 2023, 1 (2023).
Conus, D. & Dalang, R. The non-linear stochastic wave equation in
high dimensions. Electron. J. Probab. 13, 629 (2008).
Bassi, A., Lochan, K., Satin, S., Singh, T. P. & Ulbricht, H. Models of
wave-function collapse, underlying theories, and experimental
tests. Rev. Mod. Phys. 85, 471 (2013).
Chevalier, H., Paige, A. J. & Kim, M. S. Witnessing the nonclassical
nature of gravity in the presence of unknown interactions. Phys.
Rev. A 102, https://doi.org/10.1103/physreva.102.022428 (2020).
van de Kamp, T. W., Marshman, R. J., Bose, S. & Mazumdar, A.
Quantum gravity witness via entanglement of masses: Casimir
screening. Phys. Rev. A 102, 062807 (2020).
Toroš, M. et al. Relative acceleration noise mitigation for
nanocrystal matter-wave interferometry: Applications to
entangling masses via quantum gravity. Phys. Rev. Research 3,
023178 (2021).
Chou, C. W., Hume, D. B., Rosenband, T. & Wineland, D. J. Optical
clocks and relativity. Science 329, 1630 (2010).
Asenbaum, P. et al. Phase shift in an atom interferometer due to
spacetime curvature across its wave function. Phys. Rev. Lett. 118,
183602 (2017).
Overstreet, C., Asenbaum, P., Curti, J., Kim, M. & Kasevich, M. A.
Observation of a gravitational Aharonov–Bohm effect. Science
375, 226 (2022).
Abbott, B. P. et al. Prospects for observing and localizing
gravitational-wave transients with advanced ligo, advanced Virgo
and Kagra. Living Rev. Relativ. 23, 1 (2020).
McCuller, L. Single-photon signal sideband detection for highpower Michelson interferometers. arXiv preprint
arXiv:2211.04016 (2022).
Galley, T. D., Giacomini, F., & Selby, J. H. A no-go theorem on the
nature of the gravitational ﬁeld beyond quantum theory. Quantum
6, 779 (2022).
Mattingly, D. Modern tests of Lorentz invariance. Living Rev.
Relativ. 8, 1 (2005).
Abbott, P. J. & Kubarych, Z. Mass calibration at NIST in the revised
SI. Metrolologist 21, 1 (2019).
Chao, L. et al. The design and development of a tabletop kibble
balance at NIST. IEEE Trans. Instrum. Meas. 68, 2176 (2019).
Peters, A., Chung, K. Y. & Chu, S. High-precision gravity measurements using atom interferometry. Metrologia 38, 25 (2001).

Nature Communications | (2023)14:7910

https://doi.org/10.1038/s41467-023-43348-2
97.

98.
99.

100.
101.

102.
103.

104.

105.

106.

107.
108.

109.

110.
111.
112.
113.

114.

115.

116.

117.

118.

119.
120.

Ménoret, V. et al. Gravity measurements below 10-9g
with a transportable absolute quantum gravimeter. Sci. Rep. 8,
1 (2018).
Banks, T., Peskin, M. E. & Susskind, L. Difﬁculties for the evolution
of pure states into mixed states. Nucl. Phys. B 244, 125 (1984).
Ghirardi, G. C., Rimini, A. & Weber, T. Uniﬁed dynamics for
microscopic and macroscopic systems. Phys. Rev. D 34,
470 (1986).
Ballentine, L. Failure of some theories of state reduction. Phys. Rev.
A 43, 9 (1991).
Pearle, P., Ring, J., Collar, J. I. & Avignone, F. T. The CSL collapse
model and spontaneous radiation: an update. Found. Phys. 29,
465 (1999).
Bassi, A., Ippoliti, E. & Vacchini, B. On the energy increase in spacecollapse models. J. Phys. A: Math. Gen. 38, 8017 (2005).
Adler, S. L. Lower and upper bounds on CSL parameters from
latent image formation and IgM heating. J. Phys. A: Math. Theor.
40, 2935 (2007).
Lochan, K., Das, S. & Bassi, A. Constraining continuous spontaneous localization strength parameter λ from standard cosmology
and spectral distortions of cosmic microwave background radiation. Phys. Rev. D 86, 065016 (2012).
Nimmrichter, S., Hornberger, K. & Hammerer, K. Optomechanical
sensing of spontaneous wave-function collapse. Phys. Rev. Lett.
113, 020405 (2014).
Bahrami, M., Bassi, A. & Ulbricht, H. Testing the quantum superposition principle in the frequency domain. Phys. Rev. A 89,
032127 (2014).
Laloë, F., Mullin, W. J. & Pearle, P. Heating of trapped ultracold
atoms by collapse dynamics. Phys. Rev. A 90, 052119 (2014).
Bahrami, M., Paternostro, M., Bassi, A. & Ulbricht, H. Proposal for a
noninterferometric test of collapse models in optomechanical
systems. Phys. Rev. Lett. 112, 210404 (2014).
Goldwater, D., Paternostro, M. & Barker, P. Testing wave-functioncollapse models using parametric heating of a trapped nanosphere. Phys. Rev. A 94, 010104 (2016).
Tilloy, A. & Stace, T. M. Neutron star heating constraints on wavefunction collapse models. Phys. Rev. Lett. 123, 080402 (2019).
Donadi, S. et al. Underground test of gravity-related wave function
collapse. Nat. Phys.17, 74–78 (2021).
Unruh, W. G. & Wald, R. M. Evolution laws taking pure states to
mixed states in quantum ﬁeld theory. Phys. Rev. D 52, 2176 (1995).
Ellis, J., Mavromatos, N. & Nanopoulos, D. V. Quantumgravitational diffusion and stochastic ﬂuctuations in the velocity of
light. Gen. Relativ. Gravit. 32, 127 (2000).
Parikh, M., Wilczek, F. & Zahariade, G. Signatures of the quantization of gravity at gravitational wave detectors. Phys. Rev. D 104,
046021 (2021).
Verlinde, E. P. & Zurek, K. M. Observational signatures of
quantum gravity in interferometers. Phys. Lett. B 822,
136663 (2021).
Unruh, W. G. False loss of coherence. In Relativistic Quantum
Measurement and Decoherence: Lectures of a Workshop Held at
the Istituto Italiano per gli Studi Filosoﬁci Naples, (eds Breuer, H.-P.
& Petruccione, F.) April 9–10, 1999, 125–140 (Springer, 2000).
Hall, M. J. W., Cresser, J. D., Li, L. & Andersson, E. Canonical form of
master equations and characterization of non-Markovianity. Phys.
Rev. A 89, https://doi.org/10.1103/physreva.89.042120 (2014).
Breuer, H.-P., Laine, E.-M., Piilo, J. & Vacchini, B. Colloquium: nonMarkovian dynamics in open quantum systems. Rev. Mod. Phys.
88, https://doi.org/10.1103/revmodphys.88.021002 (2016).
Layton, I. & Oppenheim, J. The classical-quantum limit.
arXiv:2310.18271 (2022).
Siemon, I., Holevo, A. S. & Werner, R. F. Unbounded generators of
dynamical semigroups. Open Syst. Inf. Dyn. 24, 1740015 (2017).
23

## PDF page 24

Article
121.

122.

123.

124.
125.

126.
127.

128.
129.
130.
131.

Schäfer, G. & Jaranowski, P. Hamiltonian formulation of general
relativity and post-Newtonian dynamics of compact binaries. Living Rev. Relativ. 21, 7 (2018).
Oppenheim, J. & Reznik, B. Fundamental destruction of information and conservation laws. arXiv:0902.2361 [hep-th] (2009) (the
manuscript was never submitted to a journal, but an updated
version is available upon request).
Ghirardi, G., Rimini, A. & Weber, T. A model for a uniﬁed quantum
description of macroscopic and microscopic systems. In Quantum Probability and Applications (eds Accardi, L. et al.) (Springer,
Berlin, 1985).
Pearle, P. M. Combining stochastic dynamical state vector reduction with spontaneous localization. Phys. Rev. A 39, 2277 (1989).
Ghirardi, G. C., Pearle, P. & Rimini, A. Markov processes in Hilbert
space and continuous spontaneous localization of systems of
identical particles. Phys. Rev. A 42, 78 (1990).
Hall, M. J. & Reginatto, M. Interacting classical and quantum
ensembles. Phys. Rev. A 72, 062109 (2005).
Ulmer, W. Deconvolution of a linear combination of Gaussian
kernels by an inhomogeneous Fredholm integral equation of
second kind and applications to image processing.
arXiv:1105.3401 [physics.data-an] (2011).
Karolyhazy, F. Gravitation and quantum mechanics of macroscopic objects. Il Nuovo Cimento A (1965–1970) 42, 390 (1966).
Diósi, L. Models for universal reduction of macroscopic quantum
ﬂuctuations. Phys. Rev. A 40, 1165 (1989).
Penrose, R. On gravity’s role in quantum state reduction. Gen.
Relativ. Gravit. 28, 581 (1996).
Oppenheim, J., Russo, A. & Weller-Davies, Z. Diffeomorphism
invariant classical-quantum path integrals for Nordstrom gravity.
To appear (2023).

Acknowledgements
We would like thank Sougato Bose, Joan Camps, Matt Headrick, Isaac
Layton, Juan Maldacena, Andrea Russo, Andy Svesko and Bill Unruh for
valuable discussions and Lajos Diósi and Antoine Tilloy for their very
helpful comments on an earlier draft of this manuscript. J.O. is supported by an EPSRC Established Career Fellowship, and a Royal Society
Wolfson Merit Award, C.S. and Z.W.D. acknowledges ﬁnancial support
from EPSRC. This research was supported by the National Science
Foundation under Grant No. NSF PHY11-25915 and by the Simons
Foundation It from Qubit Network. Research at Perimeter Institute is
supported in part by the Government of Canada through the Department of Innovation, Science and Economic Development Canada and by

Nature Communications | (2023)14:7910

https://doi.org/10.1038/s41467-023-43348-2
the Province of Ontario through the Ministry of Economic Development,
Job Creation and Trade.

Author contributions
J.O., C.S., B.S. and Z.W.D. contributed to this work.

Competing interests
The authors declare no competing interests.

Additional information
Supplementary information The online version contains
supplementary material available at
https://doi.org/10.1038/s41467-023-43348-2.
Correspondence and requests for materials should be addressed to
Jonathan Oppenheim.
Peer review information Nature Communications thanks Michele
Arzano, Frank Saueressig and the other, anonymous, reviewer(s) for their
contribution to the peer review of this work. A peer review ﬁle is available.
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
© The Author(s) 2023

24
