Source: see manifest row of the PDF
PDF sha256: cd4a806d00093ebb5924fc8c1f61ff3b000b021d4668a64cd35a1d05b6f180c1
License: CC-BY-4.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of oppenheim_2023_a_postquantum_theory_of_classical_gravity.pdf

Transcription of `oppenheim_2023_a_postquantum_theory_of_classical_gravity.pdf` in this directory, 37 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-37 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

PHYSICAL REVIEW X 13, 041040 (2023)
Featured in Physics

A Postquantum Theory of Classical Gravity?
Jonathan Oppenheim
Department of Physics and Astronomy, University College London,
Gower Street, London WC1E 6BT, United Kingdom
(Received 25 June 2021; revised 20 March 2023; accepted 5 October 2023; published 4 December 2023)
The effort to discover a quantum theory of gravity is motivated by the need to reconcile the
incompatibility between quantum theory and general relativity. Here, we present an alternative approach
by constructing a consistent theory of classical gravity coupled to quantum field theory. The dynamics is
linear in the density matrix, completely positive, and trace preserving, and reduces to Einstein’s theory of
general relativity in the classical limit. Consequently, the dynamics does not suffer from the pathologies of
the semiclassical theory based on expectation values. The assumption that general relativity is classical
necessarily modifies the dynamical laws of quantum mechanics; the theory must be fundamentally
stochastic in both the metric degrees of freedom and in the quantum matter fields. This breakdown in
predictability allows it to evade several no-go theorems purporting to forbid classical quantum interactions.
The measurement postulate of quantum mechanics is not needed; the interaction of the quantum degrees of
freedom with classical space-time necessarily causes decoherence in the quantum system. We first derive
the general form of classical quantum dynamics and consider realizations which have as its limit
deterministic classical Hamiltonian evolution. The formalism is then applied to quantum field theory
interacting with the classical space-time metric. One can view the classical quantum theory as fundamental
or as an effective theory useful for computing the backreaction of quantum fields on geometry. We discuss a
number of open questions from the perspective of both viewpoints.
DOI: 10.1103/PhysRevX.13.041040

Subject Areas: Gravitation,
Quantum Information

I. MUST WE QUANTIZE GRAVITY?
The two pillars of modern theoretical physics are general
relativity, which holds that gravity is the bending of spacetime by matter, and quantum field theory, which describes
the matter that lives in that space-time. Yet, they are
fundamentally inconsistent. Einstein’s equation for gravity
Gμν ¼

8πG μν
T
c4

ð1Þ

has a left-hand side which encodes the space-time degrees
of freedom via the Einstein tensor and is treated classically,
while on the right-hand side sits the energy-momentum
tensor encoding the matter degrees of freedom which must
become an operator T̂ μν according to quantum theory (we
henceforth denote quantum operators by placing a ^ on
them). The widespread belief is that this inconsistency
should be remedied by finding a quantum theory of gravity
so that the left-hand side of Eq. (1) is also an operator. Yet,

Published by the American Physical Society under the terms of
the Creative Commons Attribution 4.0 International license.
Further distribution of this work must maintain attribution to
the author(s) and the published article’s title, journal citation,
and DOI.

2160-3308=23=13(4)=041040(37)

although we have candidates such as string theory, which
is in its mid-50’s [1], and loop quantum gravity turning just
over 40 [2–4], a convincing theory of quantum gravity
remains elusive.
Another possibility is that gravity should still be treated
classically, but that Einstein’s equation should be modified.
There is some sense to this. Space-time, though dynamical,
can be understood as describing the background on which
quantum fields of matter interact. Gravity, through the
equivalence principle, is unique in this regard—no other
fields can be described as a universal geometry in which
quantum fields live. Having this classical background
structure appears crucial to our current understanding of
quantum mechanics. Quantum field theory allows us to
predict the result of future measurements on a spacelike
surface, based on past initial data. The identification of a
Cauchy surface on which to give these initial data, not to
mention the identification of a one parameter family of
future hypersurfaces, is natural when the background
structure is classical, while it is unclear whether it is possible
to quantize this causal structure in a way which is independent of these background choices. While this difficulty may
be merely technical, background-independent approaches
such as loop quantum gravity, string field theory [5], and
others [6,7] have yet to demonstrate that this is possible.

041040-1

Published by the American Physical Society

## PDF page 2

JONATHAN OPPENHEIM

PHYS. REV. X 13, 041040 (2023)

And while the ultraviolet catastrophe required the quantization of electromagnetism, the analogous issue in gravity is
less well understood [8] and muted by the fact that
gravitational systems in equilibrium occur in exotic situations [9], or would emit gravitational radiation over very
long timescales [10].
Nonetheless, there is no strong case that gravity is
exceptional, and the overwhelming consensus has been
that we must quantize it along with all the other fields. In
part, this is due to a number of no-go theorems and
arguments over the years [11–21] purporting to require
the quantization of the gravitational field. A recent no-go
theorem [21] holds not only for coupling classical mechanics with quantum theory, but also with modifications to
quantum mechanics, so-called postquantum theories which
alter the quantum state space or dynamics [22]. But given
the difficulties faced in constructing such a theory, it seems
important to revisit this consensus. The question of why
space-time might be fundamentally classical in contrast to
other forces will be considered elsewhere [24], while here
we merely consider the necessity of quantizing gravity.
Indeed, not only do we find that it is logically possible to
have quantum fields interacting with classical space-time,
we construct such a theory. The no-go theorems on the need
to quantize gravity implicitly or explicitly assume that the
coupling of quantum fields to space-time is not stochastic.
This loophole can be exploited to construct a theory of
classical space-time which can be acted upon by quantum
fields.
Although the construction of a consistent fundamental
theory is the principal motivation of the present work, two
other motivations remain even if one believes that the
fundamental theory of gravity is quantum. The first is to
better understand the backreaction that quantum fields have
on space-time. In many cases, such as in the evaporation of
large black holes, or in inflationary cosmology, we are
interested in the limit in which space-time can be treated
classically, while the matter itself, such as the black-hole
radiation, or vacuum fluctuations, must be treated quantumly. We would like to compute the backreaction that
quantum matter produces on space-time, yet we have no
consistent theory which enables us to do this. The current
approach to describe gravity classically is to take the
expectation value of the right-hand side of Eq. (1), leading
to the semiclassical Einstein equation [25–27]
Gμν ¼

8πG μν
hT̂ i:
c4

ð2Þ

Although this equation is often used to understand the
backreaction on space-time, it is valid only when fluctuations are small, while to understand quantum effects, we are
precisely interested in the case where quantum fluctuations
are significant. Taking the semiclassical Einstein equation
seriously leads to pathological behavior. If a heavy object is

in a statistical mixture of being in two locations (as depicted
in Fig. 1), a test mass will fall toward the point between the
two locations, and the object itself will be attracted to the
place where it might have been. This has been ruled out by
Page and Geilker through the performance of a gedanken
experiment in which a lead mass was placed in a position
that depended on the reading of a Geiger counter situated
near a radioactive source [28]. It will come as no surprise to
the reader, that they verified that the dynamics depicted in
the right panel of Fig. 1 is what occurs.
This problematic behavior of the semiclassical Einstein
equation has generally been viewed as a reason why we
must quantize gravity [31–34]. However, one sees the same
apparent paradox in a fully quantum or fully classical
theory of two systems. Take for example the interaction
Hamiltonian ĤMG ¼ ĤM ⊗ Ĥ G , and the limit where the M
and G system are close to a product state with density
matrix ρ̂MG ≈ σ̂ M ⊗ σ̂ G . Then, for as long as the two
systems remain approximately uncorrelated, Heisenberg’s
equation of motion for the M system, after tracing out the G
system gives
∂σ̂ M
≈ −i½σ̂ M ; Ĥ M  ⊗ hĤG i;
∂t

ð3Þ

where we use units where ℏ ¼ c ¼ 16πG ¼ 1. The state of
the system M also appears to be coupled to an expectation
value, even though we know that this is not what happens.
By tracing out the G system, we have lost view of the fact
that the two systems will get correlated. Once the systems
become correlated, the reduced dynamics is no longer even
linear in the reduced state σ̂ M since trG ĤG ρ̂MG ≠ hĤG iσ̂ M .
While this in no way suggests that the semiclassical
Einstein equation is correct even on average, its pathologies
have led to a widely held objection to theories which treat
gravity classically, while it is clear from the above example
that the pathologies of the semiclassical Einstein equations
have nothing to do with treating one system classically, and
everything to do with taking expectation values, and thus
losing sight of correlations. The same apparent pathologies
occur if both systems are classical, but we allow for
probabilistic mixtures of states. The theory presented here
does not suffer from these issues; the equations of motion
are linear in the density matrix, just like quantum mechanics and the classical Liouville equation. In order to understand the interaction of two systems, whether they are both
quantum, both classical, or are classical quantum, we need
to account for the correlations between them, and this is
more easily done by considering the evolution of a joint
density matrix or probability density.
This leads us to the second motivation for the present
work: Even if one does not regard the theory as fundamental, it provides a sandbox, or toy model, for understanding quantum gravity. Indeed, a natural first step to
quantizing gravity is to begin with the Liouville equation

041040-2

## PDF page 3

A POSTQUANTUM THEORY OF CLASSICAL GRAVITY?

PHYS. REV. X 13, 041040 (2023)

FIG. 1. The prediction of the semiclassical Einstein equation is depicted in the right panel, compared with what we expect to occur
based on the statistical interpretation of the density matrix in the left panel. If a planet is in a statistical mixture of being in two possible
locations (“L” and “R”), then we expect the gravitational field to become correlated with it. A test particle therefore falls toward one of
the planets. If one treats the semiclassical Einstein equations as fundamental, the test particle falls down the middle, which is indeed the
average trajectory of its path in the left-hand panel. The planets are also attracted toward the place they might have been. The systems in
the linear theory considered here exhibit the behavior depicted in the left-hand panel. The case where we attempt to put the planet in a
superposition of the two locations is discussed further in Refs. [29,30]. If the gravitational field is suitably different in the two cases, in
the sense of how distinguishable the field configurations are when noise is added to them, then there will be a limit on how coherent the
superposition can be [30]. In the case where there is coherent superposition, the initial trajectory of the test mass will be insufficiently
correlated with the planet’s position to enable a determination of where the planet is. However, after the decoherence time, it may be
possible to determine the planet’s location from the trajectory of the test mass, since its trajectory will become correlated to the planet’s
location [29]. This is also what one expects from a fully quantum theory, with the stochasticity of the test mass being due to vacuum
fluctuations of the metric.

for general relativity and a probability density ρðtÞ over its
phase space. After all, the probability density and the
Liouville equation have a lot in common with the quantum
density matrix and the Heisenberg equations of motion. As
we see with the semiclassical Einstein equation, some of
the conceptual difficulties faced in understanding quantum
gravity are also found in classical probabilistic theories and
are resolved by considering instead the Liouville equation.
The classical limit of the theory we present here should thus
be close to the Liouville equation for classical Einstein
gravity introduced as Eq. (103). Many issues which arise in
quantum gravity, especially in the canonical quantization
framework, will turn out to have a similar but more
tractable form here. In particular, the difficulty encountered
in understanding the role of diffeomorphism invariance
when one does not have a single 4-geometry or single time
slicing, as well as the technical difficulty encountered in
calculating the constraint algebra, also appear in the theory
considered here. And even in some cases, in the fully
classical limit of the theory.
Let us now turn to another widely held belief on why a
classical theory of gravity is incompatible with superpositions and the uncertainty relation. This argument is
usually attributed to Feynman [12,35] and Aharonov and
Rohrlich [36] in relation to the gravitational field (see also
Refs. [14,37–40]). As depicted in Fig. 2, if the gravitational
field produced by a particle is classical, the field can in

principle be measured to sufficiently high precision to
determine the particle’s position without disturbance. This
would reveal which slit it went through, and would either
prevent particles from being in superposition or would
violate the uncertainty principle if the interference experiment of Fig. 2 is carried out. However, if the classical field
responds to the quantum system stochastically [43], then
measuring the classical degrees of freedom will not
necessarily determine the particle’s quantum state to
arbitrary precision. This could be because the gravitational
field reacts in an indeterministic way to the presence of
matter, or because there is only a probability that the
gravitational field reacts to the position of the particle
during the time of the interference experiment [45]. In
either case, the gravitational degrees of freedom contain
only partial information about the location of the particle.
We thus see that previous arguments for requiring the
quantization of the space-time metric implicitly assume that
theory is deterministic, and are not a barrier to the theory
considered here.
The fact that coupling classical gravity to quantum theory
necessarily requires stochasticity [49] is particularly compelling in light of the black-hole information problem
[51–53], and its sharper version, the Almheiri-MarolfPolchinski-Sully (AMPS) “paradox” [54,55]. Since deterministic theories appear to require a breakdown of gravity at
low energies [56], serious consideration to nondeterministic

041040-3

## PDF page 4

JONATHAN OPPENHEIM

PHYS. REV. X 13, 041040 (2023)

FIG. 2. Consider a variation of the gedanken experiment proposed by Feynman [12,35] and Aharonov [36] in which a massive particle
travels through two slits as a plane wave. Quantum theory predicts an interference pattern on the screen behind the slits which enables a
determination of the particle’s momentum. The local Newtonian potential it creates can be measured everywhere. At late times, the state
of the electromagnetic field far from the slits will be slightly different depending on which slit the particle goes through, but these two
states need not be orthogonal. The quantum nature of the electromagnetic field prevents an experimenter from distinguishing these two
nonorthogonal states and while the electromagnetic interaction might lead to some decoherence of the particle, if the interaction is small
enough the interference pattern remains. On the other hand, if the gravitational field is classical and the interaction deterministic, then
one could imagine measuring the gravitational field close to the particle and during its flight, without disturbing the field to
unambiguously determine which path the particle went through. One could therefore never get interference fringes (or the uncertainty
principle would be violated). Two classical states cannot be different but nonorthogonal. Actually measuring the gravitational field is not
required since classical systems are undisturbed; even if we cannot actually measure the field to the required accuracy [48], it is
impossible to write down a pure quantum state of the particle which is correlated with a classical gravitational field determined by the
particle’s position. Since the theory presented here modifies quantum theory so that the interaction is stochastic, the gravitational field
need not become unambiguously correlated with the particle’s path and the interference pattern is restored. Probability densities over
classical states can be different and nonorthogonal.

theories should be given [59]. However, theories with
information destruction face imposing obstacles. Banks,
Peskin, and Susskind (BPS) argued that they lead either to
violations of locality or anomalous heating [60,61], and
Coleman argued that they merely result in false decoherence
corresponding to unknown coupling constants [62]. There
have been a few attempts to work around the issue raised by
BPS. Unruh and Wald proposed that if the information
destruction was at sufficiently high energy, then violations in
momentum and energy conservation would also be at high
energy, and hence, not observable in the lab [63]. Models
which are local, yet violate cluster decomposition [64] were
proposed in Ref. [65], and ones which have only mild
violations of energy conservation at the expense of some
nonlocality were proposed in Ref. [66]. However, none of
these attempts have been theories of gravity, and once the
backreaction to space-time is considered and the constraints
of general relativity taken into account, the situation is
different enough to warrant reconsidering the issue. The
class of theories presented here may allow us to resolve the
black-hole information paradox in favor of information loss.
We return to these points in the Discussion section.
We find that the issue of anomalous heating takes on a
different form in this theory but continues to raise questions.
These may be resolved simply by regularizing the theory, but
it is also possible that we need to introduce new physics at a

distance scale larger than the Planck scale, as needs to happen
in spontaneous collapse models [67–70]. Further research is
needed because the theory we present contains a number of
unspecified couplings and choices. These can be shown to be
greatly reduced if one demands that the theory should be
continuous in phase space [71]. However, this does not
completely fix the theory, and there remains some additional
freedom which we expect to be constrained by demanding
the theory be regularizable, and by experimental constraints.
Whether there is sufficient freedom in the couplings to satisfy
these demands, as well as ones coming from symmetry
principles such as diffeomorphism invariance, remains open.
Having argued that nothing forbids the coupling of
quantum systems to classical ones, let us turn to attempts
to construct such a theory. An early attempt to couple toy
models for classical gravity to quantum mechanics was
made in Ref. [72] using the Aleksandrov-Gerasimenko
(AG) bracket [73,74]
∂ρ̂ðz; tÞ
1
¼ −i½ĤðzÞ; ρ̂ðz; tÞ þ ðfĤðzÞ; ρ̂ðz; tÞg
∂t
2
− fρ̂ðz; tÞ; ĤðzÞgÞ;

ð4Þ

where Ĥ is a quantum Hamiltonian which can depend
on phase-space points z, and f·; ·g are Poisson brackets.

041040-4

## PDF page 5

A POSTQUANTUM THEORY OF CLASSICAL GRAVITY?
The object ρ̂ðz; tÞ, about which we say more in Sec. II, is
the classical quantum (CQ) state at time t—a positive
matrix in Hilbert space, and a functional of the classical
degrees of freedom z normalized such that
Z
dztrρ̂ðz; tÞ ¼ 1:

ð5Þ

However, the dynamics the AG bracket generated leads to
negative probabilities [72,75]. Unless we are prepared to
modify the Born rule, or equivalently, our interpretation of
the density matrix, any dynamics must be trace preserving
(TP) to conserve probability, and be completely positive
(CP), for probabilities to remain positive. So, although the
dynamics of Eq. (4) makes a frequent appearance in attempts
to couple quantum and classical degrees of freedom [76–78]
(cf. Ref. [79]), and while it may give insight into some
regimes, it cannot serve as a fundamental theory. Other
attempts, such as using the Schrödinger-Newton equation
[80,81] (cf. Refs. [82,83]), suffer from the problem that the
equations are nonlinear in the density matrix, and thus will
lead to superluminal signaling [84–86] and a breakdown of
the statistical mechanical interpretation of the density matrix
[87]. And yet, experimentalists working in the field of
quantum control routinely couple quantum and classical
degrees of freedom together, usually by invoking the
mysterious measurement postulate of quantum theory.
This presents another path to treat gravity classically, where
one imagines the system of interest is fundamentally quantum, but that observables are restricted or a measurement is
performed on them [75,88–90]. However, for gravity, this
would require first quantizing the theory, which might well
be an impossible task. Another approach is to apply a
measurement to the quantum system instead, and then couple
the output to the classical degrees of freedom such as the
Newtonian potential [91–94]. Both approaches, at least
initially, invoke the measurement postulate of quantum
mechanics, or an ad hoc field which produces a stochastic
collapse of the wave function [95–100], which then sources
the gravitational field.
Here lies the essence of the problem: If nature is
fundamentally quantum, our notion of classicality hinges
on the measurement postulate. Thus, the emphasis in this
work is to invert the logic: Assume that since space-time
describes causal structure and relationships between the
matter degrees of freedom, it is a priori and fundamentally
classical. Then, examine the implications of this. One
outcome will be that the quantum degrees of freedom
inherit classicality from space-time. By treating the spacetime metric as a classical degree of freedom, we obtain for
free not only a theory of quantum matter and gravity, but
also a theory which produces the gravitationally induced
collapse of the wave function conjectured by Karolyhazy
[101], Diósi [102], and Penrose [103,104]. Collapse arises
as a simple consequence of treating space-time classically.

PHYS. REV. X 13, 041040 (2023)

Such an approach can be found in Ref. [105] where a
variation of Eq. (2) is studied, but it is argued that the
interaction of a quantum system with a classical measuring
device necessarily leads to decoherence and consistency of
the measurement postulate. Likewise, Tilloy and Diósi
[92,93] point out that although they introduce a spontaneous collapse model to source the Newtonian potential,
this can be thought of as formal, and it is the consistency of
hybrid dynamics which requires decoherence of the quantum matter. Poulin [66] also note that the classical coupling
leads to decoherence of the quantum system.
The theory considered here, however, cannot be reduced
to a linear spontaneous collapse model, because the dynamics is not Markovian or even linear in the density matrix
when the gravitational degrees of freedom are traced out
(although it is linear and Markovian when we include the
metric degrees of freedom). It also leads not merely to
decoherence, but to a genuine objective collapse of the wave
function. In particular, there are realizations of the discrete
theory considered here, where stochastic jumps in phase
space can be finite and correlate to Lindblad operators. As a
result, changes in the quantum state correspond to changes
in the classical system. Consequently, the quantum state
remains pure and uniquely determined by the trajectory of
the classical system [106]. Purity of the quantum system
conditional on the classical trajectory has since been shown
to also hold in the continuous realizations under natural
conditions [29].
Before proposing a theory which couples classical general
relativity with quantum field theory, we first construct a
general framework for classical quantum dynamics. In order
to do so, we derive general linear dynamics which maps the
set of classical quantum states to itself. More precisely, we
wish to find the most general linear dynamics which is
completely positive, trace preserving, and preserves the
division of degrees of freedom into classical and quantum.
Two examples of such dynamics have previously been
proposed. In Refs. [46,107], a master equation with diagonal
coupling to Lindblad operators L̂α was considered of the
form
X
∂ρ̂ðz; tÞ
¼ −i½ĤðzÞ; ρ̂ðz; tÞ þ
W α ðzjz0 ÞL̂α ρ̂ðz0 ; tÞL̂†α
∂t
α;z0
1
− W α ðzÞfL̂†α L̂α ; ρ̂ðz; tÞgþ ;
2

ð6Þ

where z are discrete classical degrees of freedom, and f·gþ is
the anticommutator. When W α ðzjz0 Þ ¼ W α ðzÞδðz − z0 Þ, this
reduces to the Gorini-Kossakowski-Sudarshan-Lindblad
(GKSL) or Lindblad equation [108,109] controlled by an
external degree of freedom z. Equation (6) has been shown
by Poulin to be the most general master equation in the case
of discrete classical variables and bounded Lindblad operators by embedding the classical system in Hilbert space
[110]. However, for trajectories which are continuous in the

041040-5

## PDF page 6

JONATHAN OPPENHEIM

PHYS. REV. X 13, 041040 (2023)

classical degrees of freedom, it will turn out that nondiagonal
couplings are required. A master equation due to the early
work of Diósi [47] corresponds to the constant force
R
^
case ĤðqÞ ¼ dx qðxÞLðxÞ
or sum of such terms [113],
R
P
^
ĤðqÞ ¼ i dx qi ðxÞLi ðxÞ
∂ρ̂ðz; tÞ
¼ fH 0 ðzÞ; ρ̂ðz; tÞg − i½ĤðqÞ; ρ̂ðz; tÞ
∂t
1
þ ðfĤðqÞ; ρ̂ðz; tÞg − fρ̂ðz; tÞ; ĤðqÞgÞ
2Z
1
0
dxdx0 fqi ðx0 Þ; fqj ðxÞ; Dij
þ
2 ðx; x Þρ̂ðz; tÞgg
2
Z
1
þ
dxdx0 D0;ij ðx; x0 Þ
2
i
h
× fĤðqÞ; pi ðxÞg; ½ρ̂ðz; tÞ; fĤðqÞ; pj ðx0 Þg ; ð7Þ

which adds diffusion and a Lindbladian to the AleksandrovGerasimenko bracket of Eq. (4), and is completely positive
provided the matrix inequality D2 D0 ≽ 14 is satisfied. For
arbitrary Hamiltonians and dynamics which is continuous in
phase space, one should turn to the most general continuous
master equation since derived in [71]. Unravellings for
arbitrary Hamiltonians has since been taken up in [29]. In
this work, the classical quantum interaction Hamiltonian
ĤðqÞ is chosen to be minimally coupled, meaning that it is a
functional of phase-space fields qi ðxÞ and not on the
conjugate momenta pi ðxÞ, while H0 ðzÞ is any purely
classical Hamiltonian. The constant force case considered
in Ref. [47] corresponds to an interaction Hamiltonian
which is linearR in a single classical degree of freedom
qðxÞ, ĤðqÞ ¼ dxqðxÞL̂ðxÞ. The constant force case has
been studied in the context of measurement theory [111], in
the classical limit of the collisionless Boltzmann equation
[112], and in a model for Newtonian gravity [113]. The
discrete dynamics has appeared in discussions around blackhole evaporation [66].
In Sec. III, we show that Eq. (14) is the most general form
of time-local [114] classical quantum dynamics. It includes
the discreet dynamics of Eq. (6) and the continuous
Hamiltonian dynamics of Eq. (7). Our derivation uses a
fully classical quantum formalism and gives necessary
conditions for the dynamics to be completely positive.
These conditions are also sufficient in the case of discrete
dynamics, and in Ref. [71] with Sparaciari, Šoda and WellerDavies, we derive the necessary and sufficient conditions
when the dynamics is continuous in phase space. This
continuous master equation generalizes Ref. [47] to the
case of arbitrary interaction Hamiltonians and multiple
Lindblad operators and classical degrees of freedom.
Since the continuous master equation requires off-diagonal
Lindblad couplings, this can be shown to imply that the

dynamics of Eq. (6) has discrete, finite-sized jumps in phase
space [71].
With the general form of dynamics in hand, the next step
is to restrict ourselves to dynamics which is generated by a
Hamiltonian. This allows us to apply the framework to the
Hamiltonian formalism of general relativity. This follows
from considering a perturbative expansion of the more
general dynamics presented as Eq. (17). This expansion can
be thought of as a CQ version of the Kramers-Moyal
expansion [115,116] familiar in classical stochastic dynamics. We show in Sec. IV that continuous and deterministic
classical evolution emerges in some limit. Away from this
limit, the quantum system can retain some coherence, but
complete positivity requires the classical system to undergo
diffusion or discrete, finite-sized jumps in phase space. A
discrete realization of this dynamics makes use of a finite
and noncommuting directional divergence, Eqs. (73)–(75).
This dynamics corresponds to a discrete version of
Liouville dynamics on the classical system and the action
of a dynamical semigroup on the quantum system, thus
providing a natural generalization of both classical and
quantum evolution. A parameter τ governs how continuous
and classical the total system is, with the system’s trajectory
in the classical phase space going from finite-sized hops to
continuous deterministic dynamics as τ → 0. In this limit,
the quantum system decoheres and becomes classical. For
larger τ (or ℏ), the decoherence times are longer, while the
jump distance in the classical phase space increases
resulting in greater diffusion in the system’s trajectory.
The dynamics of Eq. (17) also includes the fully continuous
evolution of Eq. (7).
In Sec. IV B, we present a simple example of the discrete
dynamics, namely, a quantum spin system with a classical
position and momentum interacting with a potential. We
see that if the particle is initially in a superposition of spin
states, then it eventually collapses to one of them through
its interaction with the classical degrees of freedom. In
essence, the classical potential acts like a Stern-Gerlach
device, so that after some time, the particle’s classical
degrees of freedom uniquely determine the value of the
spin. Unlike standard decoherence, the collapse of the
quantum state happens suddenly, when the system undergoes a classical jump in its momentum. At that point,
monitoring the momentum unambiguously reveals the
particle’s spin. The quantum state of the system remains
pure, conditioned on the state of the classical system. There
is thus no need for the mysterious measurement postulate of
quantum theory, a postulate which has meant that the
interpretation of quantum theory has been open to dispute,
and whose problematic nature has received renewed
attention [117].
In Sec. IV C, we then extend the framework to include a
hybrid version of quantum field theory. In Sec. V, we apply
this hybrid formalism to the case of general relativity. We
work in the Arnowitt-Deser-Misner (ADM) formalism [118],

041040-6

## PDF page 7

A POSTQUANTUM THEORY OF CLASSICAL GRAVITY?
treating the metric as classical, while the matter living on
space time is quantum fields. In the classical limit, the
equations of motion reduce to Einstein equations, in the
sense of a CQ version of Ehrenenfest’s theorem, that after
taking the expectation value on the quantum fields, the
equations of motion are close to the semiclassical version
of the Liouville equation [Eq. (21)] applied to general
relativity [Eq. (103)]. There are nonetheless some deviations
from general relativity in the classical limit, because there
are additional contributions relating to diffusion and
decoherence, with some of the experimental bounds on these
terms since given in Ref. [50].
The equations we derive allow one to calculate the
backreaction of quantum fields on classical space-time.
This allows us to go beyond the semiclassical Einstein
equation, and we expect it to prove useful in attempts to
understand black-hole evaporation or the effect of vacuum
fluctuations in cosmology. The interaction of the quantum
system with classical space-time causes the wave function
to collapse at a rate determined by the system’s energymomentum tensor. The stochastic nature of the interaction
allows for the possibility that information is destroyed in
black holes, although the quantum state conditioned on the
metric degrees of freedom can remain pure. The theory
suggests a number of possible experiments which could
falsify or verify it, and we discuss this in Sec. VI. We now
begin in Sec. II by reviewing the formalism of classical
quantum dynamics and then discuss how the evolution law
we derive relates to both classical stochastic dynamics and
quantum maps. The form of the master equation, Eq. (14), is
then derived in Sec. III. Since the initial posting of this
manuscript in 2018 [119], a number of advancements have
been made. We continue to highlight some of these developments while maintaining the integrity of the original draft.
II. CONSISTENT CLASSICAL
QUANTUM DYNAMICS
The state of a quantum system is represented in a Hilbert
space HS by a density matrix—a positive trace one matrix
σ̂ðtÞ at time t. A discrete classical system is represented by a
discrete random variable z, and the system has a probability
pðz; tÞ of being at z. In the continuous case, we consider a
classical system to live in phase space, although we could
just as well consider any other classical sample space.
Phase space is a 2n-dimensional manifold M of points
z ¼ ðq; pÞT , and the state of the classical system can be
represented by a probability density—a non-negative distribution
R ρðz; tÞ defined over z at time t normalized such
that dzρðz; tÞ ¼ 1.
Here, as in Refs. [46,47,66,73,74,107,111,112], we consider a hybrid classical quantum system which lives on both
the Hilbert space and the classical phase space, an illustrative
example being the classical quantum qubit of Eq. (77). The
state of a hybrid system ρ̂ðtÞ at time t is defined over an
interval around z by a positive matrix ρ̂ðz; tÞ in HS [120],

PHYS. REV. X 13, 041040 (2023)

such that the normalization condition Eq. (5) holds. In
quantum theory, such a system is sometimes said to be in a cq
state (or CQ state), and has a density matrix of the form
Z
ð8Þ
ρ̂cq ¼ dzρðz; tÞjzihzj ⊗ σ̂ðz; tÞ
with σ̂ðz; tÞ a normalized density matrix and jzi an orthonormal basis. Since q̂ and p̂ do not commute in quantum
theory, if we want to encode phase-space degrees of freedom
in a quantum system, we could consider two separate
subsystems, one which encodes q and one which encodes
p. Here, we do not consider such an embedding, but rather
describe the classical quantum state as
ρ̂ðz; tÞ ¼ ρðz; tÞσ̂ðz; tÞ

ð9Þ

Rwith ρðz; tÞ ≔ trρ̂ðz; tÞ a phase-space density and
trρ̂ðz; tÞdz ≤ 1 when integrated over any interval.
Conditioned on the classical system being in state z, the
quantum system is in the state σ̂ðz; tÞ, the normalized state of
the quantum system. In finite dimension, we can also write
the CQ state as a matrix whose diagonal entries are phasespace densities, as with the CQ qubit of Eq. (77). When we
consider gravity, each point z is a classical field (the 3metric, and 3-momentum) over R3.
We now ask, what is the most general dynamical
map which take any cq state at time t ¼ 0 to another cq
state at a later time t? This requires us to adapt Kraus’s
representation theorem [121] to the classical quantum case.
Table I compares the classical-quantum map to the Kraus
map for quantum systems and the stochastic matrix for
classical systems. Table II compares the corresponding
master equations which we now review. Let us recall that
for quantum systems, a linear map Eðσ̂Þ which is completely positive trace preserving at every time t (we say it is
infinitesimally divisible [122]) is always generated by the
GKSL or Lindblad equation [108,109]
∂σ̂ðtÞ
i
¼ − ½ĤðtÞ; σ̂ðtÞ
∂t
ℏ


1 †
†
αβ
− λ ðtÞ L̂α σ̂ðtÞL̂β − fL̂β L̂α ; σ̂ðtÞgþ
2

ð10Þ

with ĤðtÞ the Hamiltonian, the set fL̂α g a traceless basis of
operators orthogonal in the Hilbert-Schmidt norm, and
λαβ ðtÞ are elements of a positive-semidefinite (PSD) matrix,
which we write as λ ≽ 0. Here, and throughout, we use
Einstein summation notation when there are raised and
lowered indices. One can always diagonalize λ, in which
case L̂α σ̂ L̂†α is sometimes called the jump term since one
could interpret it as giving the rate at which the system
jumps from being in another quantum state into σ̂, while
†
1
2 fL̂α L̂α ; σ̂gþ is sometimes called the no-event term and
acts to preserve the trace. If the map is non-Markovian

041040-7

## PDF page 8

JONATHAN OPPENHEIM

PHYS. REV. X 13, 041040 (2023)

TABLE I. Summary of Secs. II–III of the finite-time map acting on states for stochastic classical, quantum, and
classical quantum dynamics. We use Einstein summation notation, so an index which appears both raised and
lowered should be summed over. In the classical case, the probability density ρðz; tÞ over phase space z is given in
terms of the earlier probability density ρðz; 0Þ and the transition probabilities Pðzjz0 ; tÞ which define a classical
channel. In the quantum case, the necessary and sufficient condition for complete positivity is that λðtÞ as a matrix in
αβ is positive semidefinite [which we write as λðtÞ ≽ 0]. fL̂α g are a basis of operators. The classical quantum
positivity and norm conditions combine those of the purely classical and purely quantum dynamics, and generalizes
the Kraus decomposition theorem to the hybrid case in Eq. (34).

Classical
Quantum
Classical quantum

R

Map
0

Positivity condition
0

0

ρðz; tÞ ¼ dz Pðzjz ; tÞρðz ; 0Þ
σ̂ðtÞ ¼ λαβ ðtÞL̂α σ̂ð0ÞL̂†β
R
ρ̂ðz; tÞ ¼ dz0 Λαβ ðzjz0 ; tÞL̂α ρ̂ðz0 ; 0ÞL̂†β

Pðzjz0 ; tÞ ≥ 0;

∀ z; z0

λðtÞ ≽ 0
Λðzjz0 ; tÞ ≽ 0; ∀ z; z0

Norm condition
R
dzPðzjz0 ; tÞ ¼ 1
λαβ ðtÞL̂†β L̂α ¼ I
R
dzΛαβ ðzjz0 ; tÞL̂†β L̂α ¼ I

TABLE II. Summary of Secs. II and III of the master equations governing classical, quantum, and classical quantum
dynamics, along with the positivity condition in the case of continuous dynamics, or discrete jumps in the classical
degrees of freedom. In the classical case, continuous dynamics corresponds to the Fokker-Planck equation specified
by a drift term D1 ðzÞ and a positive-semidefinite diffusion matrix D2 ðzÞ ≽ 0 with elements D2;ij ðzÞ. One can always
choose L̂0 ¼ 1, and the remaining L̂α to be traceless [71]. The CQ master equation is a natural generalization of the
classical rate equation (or Fokker-Planck equation in the continuous case) and the Lindblad equation, and is here
presented as Eq. (14) (in this table, we use the convention of including the λαβ in the W αβ terms). In general, the
coupling constants can have an explicit time dependence which we drop for ease of presentation.

Master equation
Positivity (jumps)
Positivity (continuous)

Classical

R

R
∂t ρðz; tÞ ¼ dz0 Wðzjz0 Þρðz0 ; tÞ − dz0 Wðz0 jzÞρðz; tÞ
Wðzjz0 Þ ≥ 0; ∀ z ≠ z0
Wðzjz0 Þ ¼ −D1;i ðz0 Þ∂z0i δðz − z0 Þ þ D2;ij ðz0 Þ∂z0i ∂z0j δðz − z0 Þ, D2 ≽ 0
Quantum

Master equation
Positivity condition

Master equation
Positivity (jumps)
Positivity (continuous)

∂t σ̂ ¼ −i½H; σ̂ þ hαβ Lα σ̂L†β − 12 fhαβ L†β Lα ; σ̂gþ
hαβ a PSD matrix in α, β (h ≽ 0)
Classical quantum
R
∂t ρ̂ðz; tÞ ¼ dz W ðzjz ÞLα ρ̂ðz0 ; tÞL†β − 12 dz0 W αβ ðz0 jzÞfL†β Lα ; ρ̂ðz; tÞgþ
W αβ PSD in αβ ∀ z ≠ z0 , W αβ PSD in αβ for z ¼ z0
Equation (49)
R

(or more precisely, not infinitesimally divisible), but has an
inverse, then it can still be represented by Eq. (10), with the
positive-semidefinite condition on the λαβ ðtÞ lifted, provided the finite-time map is still CP [123]. In finitedimensional Hilbert spaces, CP maps have an inverse,
but this condition can fail in infinite dimension [124,125],
in which case, it may not be possible to write the master
equation in time-local form.
For a classical stochastic process, on the other hand, an
initial state at t ¼ 0, ρðz; 0Þ evolves into
Z
ρðz; tÞ ¼ dzPðzjz0 ; tÞρðz0 ; 0Þ
ð11Þ

0

αβ

0

positive and normalized. This is equivalent to Pðzjz0 ; tÞ
being the conditional probability that the state makes a
transition to z at time t given that it was initially at z0 . For a
time-local process, the most general dynamics is given by
the rate equation
dρðz; tÞ
¼
dt

Z

dz0 Wðzjz0 ; tÞρðz0 ; tÞ − Wðz; tÞρðz; tÞ;

ð12Þ

where Wðzjz0 ; tÞ are rates for the system to transition from
state z0 to state z (this can be thought of as the jump term).
To conserve probability, we require

R
with Pðzjz0 ; tÞ ≥ 0 and dzPðzjz0 ; tÞ ¼ 1. This simply
ensures that any initial probability density ρðz; 0Þ remains

041040-8

Z
Wðz; tÞ ¼

dz0 Wðz0 jz; tÞ

ð13Þ

## PDF page 9

A POSTQUANTUM THEORY OF CLASSICAL GRAVITY?
being the total rate for the system to transition away from
state z to one of the states z0 . Wðz; tÞρðzÞ is analogous to the
no-event term in the GKSL equation.
The dynamics can be discontinuous in z, containing
discrete finite-sized jumps, in which case it is necessary and
sufficient that Wðzjz0 ; tÞ ≥ 0, ∀ z ≠ z0 for the dynamics
to be positive. When Wðzjz0 ; tÞ ¼ −D1;i ðz0 Þ∂z0i δðz − z0 Þ þ
D2;ij ðz0 Þ∂z0i ∂z0j δðz − z0 Þ, the dynamics is continuous in z,
and positive if and only if D2;ij is a positive-semidefinite
matrix in ij corresponding to diffusion. D1i is called the
drift term and includes Hamiltonian evolution as a special
case. Wðz; tÞ ¼ 0 by integration by parts in Eq. (13). The
continuous dynamics is sometimes called the FokkerPlanck equation or forward Kolmogorov equation, while
the general form of the dynamics is sometimes referred to
as the differential Chapman-Kolmogorov equation [126].
Here we present the most general classical quantum
dynamical map which is linear and completely positive. In
Sec. III, we find the generators of this map, deriving
the most general continuous-time master equation for
the dynamics. As in the proof of the generality of the
GKSL equation, the proof presented here is valid for a
separable Hilbert space, and countable set of bounded
Lindblad operators L̂α , or alternatively, when the map has
an inverse at infinitesimal short times. In the case of
unbounded operators [127], one can cast the equation in
the form we derive, but it is possible the dynamics are not
unique.
Under these assumptions, we find that the most general
master equation can be put into the form

∂ρ̂ðz; tÞ
αβ
¼ −i½Ĥðz; tÞ; ρ̂ðz; tÞ þ λ ðz; tÞ L̂α ρ̂ðz; tÞL̂†β
∂t

1
− fL̂†β L̂α ; ρ̂ðz; tÞgþ
2
Z
þ dz0 W αβ ðzjz0 ; tÞL̂α ρ̂ðz0 ; tÞL̂†β
1
− W αβ ðz; tÞfL̂†β L̂α ; ρ̂ðz; tÞgþ :
2

ð14Þ

The condition that the master equation preserve probability
requires
Z

αβ

W ðz; tÞ ¼

dz0 W αβ ðz0 jz; tÞ

ð15Þ

for each α, β. One can verify this is the case by taking the
trace of Eq. (15) and integrating over phase space, and then
requiring the total probability to be conserved in time
∂
∂t

Z
dztrρ̂ðz; tÞ ¼ 0:

ð16Þ

PHYS. REV. X 13, 041040 (2023)

This norm-preserving condition is analogous to the purely
classical case of Eq. (13) and the pure-Lindbladian case.
Our derivation is general enough to allow for the
coupling terms to be time dependent, which would allow
for the inclusion of various non-Markovian effects, but
following our general derivation, we drop the time dependence from λαβ ðz; tÞ and W αβ ðzjz0 ; tÞ (one refers to such
dynamics as being autonomous). For the dynamics of
Eq. (14) to be infinitely divisible (i.e., CP as a generator
at every time t), it is necessary that W αβ ðzjz0 ; tÞ be a
positive-semidefinite matrix in α; β ∀ z ≠ z0 , and the
matrix with elements λαβ þ W αβ ðzjz; tÞ must be PSD.
These are sufficient conditions for discrete, jumping
dynamics while the conditions on W αβ ðzjz0 ; tÞ in the
continuous case are derived in Ref. [71] and previewed
here as Eq. (49). For continuous quantum systems, the
sum over αβ is replaced by an integral, an example
being the case where we take Lindblad operators to be
local field operators written in terms of the coordinate x.
L̂α can be any operator, but we can always rewrite the
above equation in terms of a basis of Lindblad operators
orthogonal in Hilbert-Schmidt norm, such that the L̂α
(distinguished by having α in bold font) are traceless,
and L̂0 ¼ 1.
The terms proportional to W 00 ðzjz0 Þ and W 00 ðzÞ are
thus purely classical and account for both stochastic and
deterministic evolution of the classical degrees of freedom.
In the case of continuous deterministic dynamics, this term
is just the Poisson bracket fh00 ðzÞ; ρ̂ðz; tÞg with h00 ðzÞ a
classical Hamiltonian. In Eq. (14), we separate out the
Lindbladian term with couplings λαβ ðzÞ to be consistent
with conventions of the classical literature, but it is often
convenient to include them in W αβ ðzjz0 ; tÞ. The W αβ ðzjz0 Þ
can be interpreted as the jump term in both phase space or
Hilbert space or both since it can induce transitions in both
the classical quantum system. λαβ ðzÞ causes transitions in
Hilbert space only, and W 00 ðzjz0 Þ transitions only in phase
space. The anticommutator terms are the collective noevent terms.
In the case that the quantum and classical systems do not
get correlated in z (for example, when one system acts as a
large heat bath weakly coupled to the other), the dynamics
derived here reduces to a semiclassical version of the
stochastic master Eq. (12) when we trace out the quantum
system, while if we integrate out z we get an averaged
version of GKSL dynamics. However, more generally,
tracing out the quantum or classical system results in
dynamics that are non-Markovian, since there can be
correlations between the classical and quantum systems,
and the reduced dynamics are not even linear on the quantum
state. When we integrate over z, the presence of correlations
between the classical system and the quantum one translate
into different effective coupling strengths WðzÞ for different
quantum states [128,129].

041040-9

## PDF page 10

JONATHAN OPPENHEIM

PHYS. REV. X 13, 041040 (2023)

In Sec. IV, we introduce a class of theories whose
dynamics is close to Hamiltonian dynamics. This master
equation can be expanded as
∂ρ̂ðz; tÞ
¼ −i½ĤðzÞ; ρ̂ðz; tÞ
∂t


W αβ
1
þ
L̂α ρ̂ðz; tÞL̂†β − fL̂†β L̂α ; ρ̂ðz; tÞgþ
2
τ

the semiclassical Einstein equation (2) as depicted on the
right side of Fig. 1. Instead, the dynamics of Eq. (21) is
linear in the total density matrix and similar to the situation
described in our discussion of Eq. (3) where we have linear
evolution of two coupled systems which account for the
correlation. For example, the correlated state of two
components labeled L and R,
1
1
ρ̂ðzÞ ¼ ρL ðzÞσ̂ L þ ρR ðzÞσ̂ R ;
2
2

αβ
†
†
− L̂α Xαβ
h ðzÞ · ∇ρ̂ðz; tÞL̂β þ τL̂α ∇ · ½γ h ðzÞρ̂ðz; tÞL̂β

þ τL̂α ∇ · Dαβ ðzÞρ̂ðz; tÞ · ∇ L̂†β þ    ;

ð17Þ

where ∇ ¼ ð∂q ; ∂p ÞT is the divergence in phase space
z ¼ q, p, and Xαβ
h a matrix of vector fields which, as we
detail, is generated by a Hamiltonian
ĤðzÞ ¼ hαβ ðzÞL̂†β L̂α

ð18Þ

over quantum and classical degrees of freedom via the
symplectic matrix


0
In
Ω¼
:
ð19Þ
−I n 0

ð22Þ

would evolve according to Eq. (21) as
∂ρðzÞ 1
1
¼ ftrĤðzÞσ̂ L ; ρL ðzÞg þ ftrĤðzÞσ̂ R ; ρR ðzÞg   
∂t
2
2
ð23Þ
with the component ρL ðzÞ evolving differently into ρR ðzÞ as
in the left side of Fig. 1. One can also think of ∂=∂p in
Eq. (21) acting on each matrix element of ρ̂ðz; tÞ, while the
velocities ∂ĤðzÞ=∂q are a matrix, and thus the backreaction
force depends on which state the quantum system is in and
correlates the quantum system with the classical one.
III. THE CLASSICAL QUANTUM MAP
AND MASTER EQUATION

The couplings
αβ
Xαβ
h ðzÞ ¼ Ω∇h ðzÞ

ð20Þ

are the terms which correspond to Hamiltonian evolution in
the classical limit. γ αβ
h ðzÞ is taken to correspond to a friction
term and is a vector in the 2n-dimensional phase space
αβ
at each z, with components γ αβ
h;i ðzÞ, while the D ðzÞ
corresponding to diffusion terms define a matrix both in
αβ and in phase space with elements Dαβ
ij ðzÞ at each z. One
typically considers Dαβ ðzÞ to depend only on q̄ and the
diffusion to be in p̄. Here, we include the pure-Lindbladian
term proportional to λαβ ðzÞ in the W αβ ðzÞ term.
Dropping terms of higher order in τ and taking the
expectation value on both sides by performing the trace
over the quantum degrees of freedom gives a semiclassical
version of the Liouville equation
∂ρðz; tÞ
¼ trfĤðzÞ; ρ̂ðz; tÞg þ    :
∂t

ð21Þ

If we retain the term proportional to τ, an appropriate
αβ
choice of γ αβ
h ðzÞ and D ðzÞ corresponds to a hybrid version
of the Fokker-Planck equation. Truncating the expansion in
Eq. (21) can result in negative probabilities, but the full
evolution equation is completely positive and provides
a natural generalization of both classical Hamiltonian
dynamics and the GKSL equation.
We also see that taking the trace over the quantum
system does not result in the pathological behavior found in

We first derive the classical quantum map which takes a
cq state ρ̂ðz; 0Þ to another cq state ρ̂ðz; tÞ and then derive the
continuous-time master equation. Recall that we restrict
ourselves to the case of trace-class operations. We also
restrict ourselves to the case where the map has an inverse
at infinitesimal times (which need not be completely
positive), so that we may write the master equation in
time-local form [123]. Recall also Kraus’s theorem, that the
most general map on quantum systems Eðσ̂Þ that is CP and
TP can be written so that
X
σ̂ðtÞ ¼ E(σ̂ð0Þ) ¼
K μ σ̂ð0ÞK †μ
ð24Þ
μ

with the operators K μ satisfying
K †μ K μ ¼ 1;

ð25Þ

where CP means that 1 ⊗ E acting on HS ⊗ HS takes
positive operators to positive operators, and together with
the trace-preserving condition, ensures that density matrices are mapped to density matrices, even if the map acts on
part of a system.
Let us now consider the case of a map which acts on cq
states. Because the map has to be linear in ρ̂ðz; tÞ, we can
write the total map Λt acting on ρ̂ð0Þ in terms of quantum
maps Λzjz0 ;t such that

041040-10

Z
ρ̂ðz; tÞ ¼

dz0 Λzjz0 ;t ρ̂ðz0 ; 0Þ:

ð26Þ

## PDF page 11

A POSTQUANTUM THEORY OF CLASSICAL GRAVITY?
Since the initial state could be ρ̂ðz0 ; 0Þ ¼ δðz0 − z0 Þσ̂ðz0 Þ,
i.e., a normalized quantum state, with vanishing support a
finite distance away from some initial point z0 , the map
Λzjz0 ;t must be completely positive for all z, z0 . The initial
state which could be peaked around any z0 must be mapped
to another positive (but not necessarily normalized) quantum state around z. In the case of discrete z, the maps need
not preserve the trace; they must merely be completely
positive, trace nonincreasing, since if we act on the
normalized state around some point z0 , a final state around
z cannot have a trace
R larger than 1, as this would correspond
to a probability dzρðz; tÞ larger than 1. Thus, one easily
sees that a necessary and sufficient condition for a cq map is
that each Λzjz0 ;t must be a completely positive, trace
nonincreasing map, with the total map
Z
0
Λz ;t ≔ dzΛzjz0 ;t
ð27Þ

PHYS. REV. X 13, 041040 (2023)
We now want to derive the generator L of this map

Z
t
Λt ¼ exp
ð31Þ
dsLs
0

using
ρ̂ðz; t þ δtÞ − ρ̂ðz; tÞ
:
δt→0
δt

Lt ρ̂ðz; tÞ ¼ lim

ð32Þ

This is possible, if at short times, the map has an inverse
(which need not be CP), since then it can always be
written in time-local form [123] (the proof contained in
Refs. [124,125] also applies to maps on CQ states). I.e.,
˙ρ̂ðz; tÞ ¼ KðtÞρ̂ðz0 ; tÞ:

ð33Þ

To this end, we write the Kraus operators in terms of an
orthonormal basis of operators L̂α to obtain
XZ
ρ̂ðz; tÞ ¼
dz0 Λαβ ðzjz0 ; tÞL̂α ρ̂ðz0 ; 0ÞL̂†β ; ð34Þ

being traceR preserving. This is the analog of the classical
condition dzPðzjz0 Þ ¼ 1. In the case where z is continuous, the above statements hold, except that because trρ̂ðz; tÞ
is a distribution, we should interpret statements about the
nonincreasing of its trace asRreferring to its trace smeared
over an indication function dztrρ̂ðz; tÞξðzÞ.
We can then write the map in terms of sets of Kraus
operators K μ ðzjz0 ; tÞ,
Z
X
ρ̂ðz; tÞ ¼ dz0 K μ ðzjz0 ; tÞρ̂ðz0 ; 0ÞK μ ðzjz0 ; tÞ† ; ð28Þ

where complete positivity for all z, z0 requires the
Λαβ ðzjz0 ; tÞ be a positive-semidefinite Hermitian matrix
in α, β for all z, z0 (see Ref. [130] and also Appendix A).
The trace-preserving condition Eq. (29) requires
XZ
dzΛαβ ðzjz0 ; tÞL̂†β L̂α ¼ 1:
ð35Þ

P
0
†
0
where
μ K μ ðzjz ; tÞ K μ ðzjz ; tÞ ≤ 1. This follows from
the fact that the action of the entire map must preserve the
trace; thus, summing over μ and taking the trace of both
sides of Eq. (28) on an arbitrary initial state ρ̂ðz0 ; 0Þ,
requires
XZ
dzK μ ðzjz0 ; tÞ† K μ ðzjz0 ; tÞ ¼ 1:
ð29Þ

Since fL̂α g is an arbitrary orthogonal basis of the
operator space, we can always take L̂0 ¼ 1, and the
orthogonality condition trL̂†β L̂α ¼ 0 for α ≠ β means that
the other L̂α are traceless, and we denote them with bold
font α. We are interested in changes of the state over
infinitesimally short times δt. Since the dynamics is time
local [Eq. (33)], we can expand the Λαβ as

α;β¼0

αβ

μ

μ

Λ00 ðzjz0 ; t þ δtÞ ¼ Λ00 ðzjz0 ; tÞ − δðz − z0 Þγ 00 ðz0 ; tÞδt

Equation (28), together with the normalization constraint of
Eq. (29), gives the most general map on hybrid classical
quantum states. It is the hybrid generalization of both the
classical probability map of Eq. (11), and in some sense, an
extension of the Kraus representation theorem Eq. (24).
However, it can also be considered a special case of a Kraus
decomposition, as we could restrict ourselves to quantum
states that have the form of Eq. (8) and write its action as
Z
X
ρ̂cq ðtÞ ¼ dzdz0 jzihz0 j ⊗ K μ ðzjz0 ; tÞρ̂cq ð0Þjz0 ihzj
μ

⊗ K μ ðzjz0 ; tÞ† :

ð30Þ

where the set of Kraus operators is fjzihz0 j ⊗ K μ ðzjz0 ; tÞg.

þ W 00 ðzjz0 ; tÞδt þ Oðδt2 Þ;

ð36Þ

Λαβ ðzjz0 ; t þ δtÞ ¼ Λαβ ðzjz0 ; tÞ þ δðz − z0 Þλαβ ðz0 ; tÞδt
þ W αβ ðzjz0 ; tÞδt þ Oðδt2 Þ;

αβ ≠ 00:
ð37Þ

This is just a Taylor expansion where we divide up the terms
proportional to δt into two contributions for later convenience and for comparison with existing convention. If the
map acts on an initial state ρ̂ðz; tÞ, then Λ00 ðzjz0 ; tÞ ¼
1δðz − z0 Þ, since when δt → 0 the system has to remain at
the same point in phase space and the quantum system does
not change. The other Λαβ ðzjz0 ; tÞ ¼ 0, since these terms are

041040-11

## PDF page 12

JONATHAN OPPENHEIM

PHYS. REV. X 13, 041040 (2023)

associated with Lindblad operators L̂α acting on the state and
nothing happens to the state in the limit δt → 0. This leaves
Λ00 ðzjz0 ; t þ δtÞ ¼ δðz − z0 Þð1 − δtγ 00 ðz0 ; tÞÞ
þ W 00 ðzjz0 ; tÞδt þ Oðδt2 Þ;

ð38Þ

so that we can write Eq. (41) as
∂ρ̂ðz; tÞ
¼ −i½Ĥðz; tÞ; ρ̂ðz; tÞ þ λαβ ðz; tÞρ̂ðz; tÞL̂α ρ̂ðz; tÞL̂†β
∂t
Z
þ

Λαβ ðzjz0 ;tþδtÞ ¼ δðz−z0 Þλαβ ðz0 ;tÞδt
þW αβ ðzjz0 ;tÞδtþOðδt2 Þ; αβ ≠ 00: ð39Þ
The first term proportional to δt in Eq. (39) can be
thought of as the probability per time δt the system does not
move in phase space while the quantum system has
L̂α ρ̂ðz; tÞL̂†β applied to it, while the W αβ ðzjz0 ; tÞ term in
both equations gives the rate that the system goes from z0 to
z and has L̂α ρ̂ðz; tÞL̂†β applied to it. We adopt the convention
that the sign in front of γ 00 is negative, anticipating that it
will contribute negatively; it is the no-event term, and the
probability that the system is unchanged can decrease only
with time.
The expansion for the Λ00 component is similar to the
one used to derive Eq. (12) for continuous classical
stochastic processes. Taking the limit dt → 0 and keeping
only the first-order terms usually require that the set of
operators L̂α be bounded in order for such terms to be
small, but here we replace that typical assumption with the
assumption that the map is invertible at short times [leading
to Eq. (33)]. To find the generator of the dynamics, we
substitute Eqs. (38) and (39) into Eq. (34) to get
Z
ρ̂ðz; t þ δtÞ ¼ dz0 δðz − z0 Þðð1 − δtγ 00 ðz0 ; tÞÞρ̂ðz0 ; tÞ
þ δtλα0 ðz; tÞL̂α ρ̂ðz0 ; tÞ þ δtλ0β ðz; tÞρ̂ðz0 ; tÞL̂†β
þ δtλαβ ðz; tÞL̂α ρ̂ðz0 ; tÞL̂†β Þ
XZ
dz0 δtW αβ ðzjz0 ; tÞL̂α ðxÞρ̂ðz0 ; tÞL̂†β ;
þ
αβ

ð40Þ
and subtracting ρ̂ðz; tÞ, dividing by δt, and taking the limit
δt → 0 gives
∂ρ̂ðz; tÞ
¼ −γ 00 ðz; tÞρ̂ðz; tÞ þ λα0 ðz; tÞL̂α ρ̂ðz; tÞ
∂t
þ λ0β ðz; tÞρ̂ðz; tÞL̂†β þ λαβ ðz; tÞL̂α ρ̂ðz; tÞL̂†β
XZ
dz0 W αβ ðzjz0 ; tÞL̂α ρ̂ðz0 ; tÞL̂†β :
þ
ð41Þ

þ fN̂ðz; tÞ; ρ̂ðz; tÞgþ :

1 0β †
ðλ L̂β − λα0 L̂α Þ;
2i
1
N̂ðz; tÞ ≔ −γ 00 ðz; tÞ þ ðλ0β L̂†β þ λα0 L̂α Þ;
2

Z
dztr

∂ρ̂ðz; tÞ
¼0
∂t

for any input state ρ̂ðz0 ; tÞ, which requires

1 X αβ 0
N̂ðz0 ; tÞ ¼
λ ðz ; tÞL̂†β L̂α
2 αβ

Z
X
†
αβ
0
þ dz W ðzjz ; tÞL̂β L̂α :

ð44Þ

αβ

Defining the outgoing flux W αβ ðz; tÞ by Eq. (15) gives the
desired form of the master equation (14).
The first term of Eq. (14) is the free evolution of the
quantum system at each point in phase space, the second
term corresponding to λαβ ðz; tÞ is pure Lindbladian, with a
rate determined by the classical degrees of freedom. The
remaining term corresponding to W αβ gives the interaction
term between the classical and quantum degrees of freedom. It is worth noting that the term corresponding to
αβ ¼ 00,
Z
∇00 ρ̂ðz; tÞ ≔ dz0 W 00 ðzjz0 Þρ̂ðz0 ; tÞ − W 00 ðzÞρ̂ðz; tÞ; ð45Þ
is the purely classical evolution of the system and is
identical to Eq. (12). It can be stochastic or it can
correspond to deterministic dynamics generated by a
classical Hamiltonian HðzÞ, in which case, we can write
it in terms of the Poisson bracket, or equivalently, as
∇00 ρ̂ðz; tÞ ¼ −X00
h · ∇ρ̂ðz; tÞ;

ð46Þ

where X00
h is the Hamiltonian vector field
X00
h ¼ Ω∇H:

ð47Þ

Recalling Eqs. (20) and (18)
X00
h ¼

Ĥðz; tÞ ≔

ð42Þ

ð43Þ

Having subtracted ρ̂ðz; tÞ from Eq. (35) the trace-preservation condition Eq. (27) becomes Eq. (16), i.e.,

αβ

As in the derivation of the GKSL equation, we now define
the two Hermitian operators

dz0 W αβ ðzjz0 ; tÞL̂α ρ̂ðz0 ; tÞL̂†β

 00

∂h
∂h00 T
;
;−
∂p
∂q

ð48Þ

∇00 could also include a diffusion term as in the FokkerPlanck equation, but it will be natural to treat it in the same

041040-12

## PDF page 13

A POSTQUANTUM THEORY OF CLASSICAL GRAVITY?
way as the other W αβ, in which case, it will be a stochastic
version of Hamiltonian dynamics.
Let us now return to Eqs. (38) and (39) and the condition
that complete positivity places on Λαβ ðzjz0 ; tÞ. In general,
all that is required is that the total map from some initial
state at t ¼ 0 to some final time is completely positive. In
this case, the generators at intermediate times t need not
generate completely positive dynamics if one were to
replace the current state of the system ρ̂ðz; tÞ with some
other state as long as they generate CP dynamics on the
state which had been evolving since t ¼ 0. In this way, one
can consider non-Markovian dynamics. However, in the
case where we demand that the generator is infinitesimally
divisible, i.e., generate CP dynamics at all times on any
state, then the positivity conditions for Λαβ ðzjz0 ; tÞ to be
completely positive can be determined from the right-hand
side of Eqs. (38) and (39). For z ≠ z0 [we can smear

Eqs. (38) and (39) over an indicator function with support
on or away from z ¼ z0 as is done in [71]], Λαβ ðzjz0 ; t þ δtÞ
is equal to W αβ ðzjz0 ; tÞδt, and so it is necessary that
W αβ ðzjz0 ; tÞ be a positive-semidefinite matrix in αβ.
When z ¼ z0 , we just have the usual GKSL dynamics,
and so we require W αβ ðzjz0 ; tÞ þ λαβ ðz; tÞ be positive semidefinite. These condition are also sufficient in the case of
discrete dynamics, because these two cases completely
specify the dynamics, and the only condition it has to
satisfy is complete positivity and norm preserving. The
necessary and sufficient conditions on W αβ ðzjz0 ; tÞ for
continuous evolution are derived in Ref. [71]. They are
best given in terms of the moment expansion of
W αβ ðzjz0 ; tÞ, which is not derived until Sec. IV, but for
completeness we conclude this section with it, expressed as
a matrix in α, β:

"P
0

Wðzjz ; tÞ ¼

0
M00
2
0
n ðz ;tÞ
∇⊗n
n¼0
z0 δðz − z Þ;
n!

P1

0
Mα0
0
n ðz ;tÞ
∇⊗n
n¼0
z0 δðz − z Þ;
n!

with
†
M2 ≽ M 1 M −1
0 M1 ;

ðI − M 0 M −1
0 ÞM 1 ¼ 0:

ð50Þ

Here, M−1
0 is the generalized inverse of the PSD matrix with
elements M αβ
0 , M 1 is a matrix in both α, i where i indexes the
00
components of z. It has entries M0α
1;i . M 2 is a PSD matrix in i,
00
j with entries M 2;ij . This generalizes the constant force
dynamics of Ref. [47], and gives Eq. (7), allowing for any
Hamiltonian Ĥðz; tÞ to generate classical quantum dynamics, as well as more general non-Hamiltonian backreaction,
such as those which include friction.
In the remainder of the article, we restrict our attention to
the autonomous case where the coupling constants have no
explicit time dependence.
IV. NONCOMMUTING
HAMILTONIAN DYNAMICS
We would like stochastic hybrid dynamics, which has
continuous Hamiltonian evolution in the classical limit. For
the continuous dynamics of Eq. (49), this is given as
Eq. (7). In this section, we explore the discrete master
equation corresponding to Eq. (17) whose first few terms in
its expansion correspond to classical quantum versions of
the Liouville equation at first order and Fokker-Planck
equation at second next order. We begin by taking z to be
phase-space variables q, p, and later present the case where
z represents canonically conjugate pairs of field degrees of
freedom over x, since the generalization is straightforward,

PHYS. REV. X 13, 041040 (2023)

P1

n¼0

0
M0β
0
n ðz ;tÞ
∇⊗n
z0 δðz − z Þ
n!

#

0
0
M αβ
0 ðz ; tÞδðz − z Þ

ð49Þ

while the notation is more cumbersome. The dynamics is
generated by a Hamiltonian operator, which can also
depend on phase-space variables z and a decomposition
of the Hamiltonian in terms of Lindblad operators L̂α given
by Eq. (18), which we recall as
ĤðzÞ ¼ hαβ ðzÞL̂†β L̂α :
When we get to the field theory case, we see that Lorentz
invariance, and later, diffeomorphism invariance, place
very tight constraints on this decomposition. The h00 ðzÞ
term is purely classical, since it couples only via 1 to the
quantum degrees of freedom. There is some ambiguity in
what is included in the L̂α and what in hαβ ðzÞ, but it will
turn out that this ambiguity is inconsequential when
applying this formalism to general relativity. The matrix
hαβ is Hermitian, and it is sometimes convenient to take it to
be positive as is the case for the coupling term of general
relativity. We define a generator of dynamics Xh which has
both phase-space components and components α,β in
Hilbert space determined by the Lindblad operators, i.e.,
 αβ

∂h
∂hαβ T
αβ
Xh ¼
:
ð51Þ
;−
∂p
∂q
Just as the Hamiltonian vector field determines the rate
of flow along different directions in phase space in the
case of purely deterministic classical evolution, here, Xαβ
h ,
additionally sets the rate of quantum jumps along different
Lindblad operators.
We have already expanded Λt in terms of infinitesimally
small times δt, and we now also expand it in terms of the

041040-13

## PDF page 14

JONATHAN OPPENHEIM

PHYS. REV. X 13, 041040 (2023)

phase-space vector Δ ≔ z − z0, which we can then take
arbitrarily small if we choose. To this end, let us write
Λαβ ðzjz0 ; tÞ ¼ Λαβ ðzjz − Δ; tÞ and perform both an expansion in δt and a Kramers-Moyal expansion [115,116] in Δ.
We can either do this directly on Eqs. (38) and (39), but it is
slightly less cumbersome to perform it on W αβ ðzjz − Δ; tÞ,
W αβ ðzjz − Δ; tÞρ̂ðz − Δ; tÞ
¼ W αβ ðz þ Δ − Δjz − Δ; tÞρ̂ðz − Δ; tÞ
∞
X ð−Δ · ∇Þn
½W αβ ðz þ Δjz; tÞρ̂ðz; tÞ:
¼
n!
n¼0

ð52Þ

in terms of the moments
Z
Mαβ
dΔðΔÞ⊗n W αβ ðz þ Δjz; tÞ:
n ðz; tÞ ¼

þ ∇ · Dαβ ðzÞρ̂ðz; tÞ · ∇ þ    ;
ð53Þ

ð54Þ

Here, we write M αβ
n ðz; tÞ as an n-fold tensor power, since
⊗n
⊗n
Δ · ∇ ¼ ðΔ · ∇Þn with Δ · ∇ the directional divergence in the direction Δ. This has the advantage that the
notation is compact, but the disadvantage that it distinguishes the moment corresponding to ∂q ∂p to that of ∂p ∂q
(for example). The zeroth moments
Z
αβ
ð55Þ
M0 ¼ dΔW αβ ðz þ Δjz; tÞ
are just W αβ ðz; tÞ of Eq. (15). The first moments are the
vectors
Z
αβ
ð56Þ
M 1 ¼ dΔΔW αβ ðz þ Δjz; tÞ:
For a Hamiltonian Ĥ and decomposition hαβ , we see that
there is a natural choice of W αβ ðz þ Δjz; tÞ so that the
vector of first moments has a contribution corresponding to
Hamiltonian flow
αβ
Xαβ
h ðzÞ ≔ Ω∇h ðzÞ;

ð57Þ

where we indicate that W αβ ðz þ ΔjzÞ is generated from the
field hαβ , with the subscript h. This we do in Sec. IVA. We
can also consider a contribution corresponding to friction
γ αβ
h so that
Z

αβ
αβ
dΔΔW αβ
h ðz þ ΔjzÞ ≔ X h ðzÞ − γ h ðzÞ:

Making the Markovian approximation so that we may
drop the explicit dependence on time, and putting this
together gives
Z
dΔW αβ ðzjz − ΔÞρ̂ðz − Δ; tÞ
αβ
¼ W h ðzÞρ̂ðz; tÞ − Xαβ
h · ∇ρ̂ðz; tÞ þ ∇ · γ h ρ̂ðz; tÞ

We now integrate this expression over Δ to write
Z
dΔW αβ ðzjz − Δ; tÞρ̂ðz − Δ; tÞ

 αβ
∞
X
M n ðz; tÞ
⊗n
ρ̂ðz; tÞ
¼
ð−∇Þ ×
n!
n¼0

Although there could be some arbitrariness in this division,
αβ
a standard friction term is of the form γ αβ
h ðzÞ ¼ τγ∂h =∂p
with γ a constant and τ included for later convenience.
Next, there is the matrix of diffusion terms
Z
1
Dαβ ðzÞ ≔
dΔΔ ⊗ ΔW αβ
ð59Þ
h ðz þ ΔjzÞ:
2

ð60Þ

where we use the fact that ∇ · Xαβ
h ¼ 0, and the notation ∇ is
to indicate that ∇ acts on the second Δ in the tensor product of
Dαβ ðzÞ, while ∇ acts on the first. One typically refers to the
terms which contain ∇ρ̂ðz; tÞ as the drift, since they determine the rate at which the expectation values of observables
change. The terms corresponding to second derivatives lead
to diffusion in phase space. Note that if Dαβ ðzÞ depends on
both the q and p, then it can also include contributions to the
drift, sometimes referred to as anomolous drift. Here we take
Dαβ ðzÞ to depend only on the q so that there are no anomalous
drift terms coming from this and higher-order terms.
The Pawula theorem [131] says that either the KramersMoyal expansion truncates at the second moment or requires
an infinite sum of terms. In the latter case, our truncated
master equation will not be completely positive, and should
be regarded as an approximation of the dynamics of Eq. (14).
We call a particular expansion of Ĥ in terms of Lindblad
operators, and the choice of W αβ ðz þ ΔjzÞ or Λαβ ðz þ ΔjzÞ a
realization, and although we present two simple realizations
in Sec. IVA, the main requirement we demand is that the
moment expansion include Xαβ
h ðzÞ, the Hamiltonian vector
field for hαβ ðzÞ in its first moment, Eq. (58). This ensures that
we are able to reproduce the deterministic classical equations of motion in the appropriate limit. When we consider
applying our results to field theory and later general
relativity, Lorentz covariance and parameter invariance
implies further constraints on W αβ ðzjz0 Þ.
Substituting the Kramers-Moyal expansion of W αβ ðzjz0 Þ
into Eq. (14) gives
∂ρ̂ðz; tÞ
¼ −i½ĤðzÞ; ρ̂ðz; tÞ þ ðλαβ ðzÞ
∂t


αβ
† 1
†
þ M 0 ðzÞÞ L̂α ρ̂ðz; tÞL̂β − fL̂β L̂α ; ρ̂ðz; tÞgþ
2
αβ
†
†
− L̂α Xαβ
h ðzÞ · ∇ρ̂ðz; tÞL̂β þ L̂α ∇ · ½γ h ðzÞρ̂ðz; tÞL̂β

ð58Þ

041040-14

þ L̂α ∇ · Dαβ ðzÞρ̂ðz; tÞ · ∇ L̂†β þ    :

## PDF page 15

A POSTQUANTUM THEORY OF CLASSICAL GRAVITY?
When we consider realizations of W αβ , we typically find
that each order in the expansion carries with it higher
powers of some constant τ. If we identify ð1=τÞW αβ ðzÞ ≔
αβ
λαβ ðzÞ þ Mαβ
→ τDαβ , this is Eq. (17) highlighted
0 and D
in the Sec. I.
An important category of realizations are ones in which
αβ
Mαβ
n ðzÞ for n ≥ 2 and γ h ðzÞ depend only on the conjugate
coordinates q, and the diffusion is only in the conjugate
momenta p, i.e.,
∂ρ̂ðz; tÞ
¼ −i½ĤðzÞ; ρ̂ðz; tÞ
∂t


W αβ ðzÞ
1 †
†
þ
L̂α ρ̂ðz; tÞL̂β − fL̂β L̂α ; ρ̂ðz; tÞgþ
τ
2
†
− L̂α Xαβ
h ðzÞ · ∇ρ̂ðz; tÞL̂β

∂
· ½γ αβ ðzÞρ̂ðz; tÞL̂†β
∂p h
⃖∂
∂
· Dαβ ðzÞρ̂ðz; tÞ · L̂†β þ    :
þ τL̂α
∂p
∂p
þ τL̂α

ð61Þ

This means that the q still obeys the equation of motion
q̇ ¼

∂h00
∂p

ð62Þ

and allows one to define p deterministically in terms of q
and q̇. This can be verified using the Heisenberg representation for all moments of q (see Appendix B).
Equation (61) is thus a classical quantum version of the
Wiener process or Fokker-Planck equation, and we refer to
such a master equation as Brownian. For such a master
equation, it is the conjugate momentum which is influenced
by the quantum system. In the more general case, p is
defined only in terms of expectation values.
It is worth noting that in our expansion, we have a purely
Lindbladian term which is itself trace preserving, and a

PHYS. REV. X 13, 041040 (2023)

quantum evolution. One can have a purely deterministic
classical evolution term as well. Since L̂0 ¼ 1, the X00
h term
is generated by the pure classical term h00 in the expansion
of ĤðzÞ in Eq. (18),
00
−X00
h ðzÞ · ∇ψ ¼ fh ðzÞ; ρ̂ðz; tÞg:

The other deterministic term, at least on the classical system
†
and for a particular αβ, is L̂α Xαβ
h ðzÞ · ∇ρ̂ðz; tÞL̂β , which, if
we take the trace over the quantum system, gives the
required dynamics we are looking for, Eq. (21).
The other nondeterministic parts include the pureLindblad term, and if we trace out the quantum system
it contributes nothing to the dynamics of the classical
system, except indirectly, as it evolves the quantum system
which backreacts on the classical system. On the quantum
system, it can generate decoherence, and if the Lindblad
operators are diagonal in raising and lowering operators, it
raises and lowers the state of the quantum system. The final
two terms, if we trace out the quantum degrees of freedom
are the friction and diffusion terms on phase space
reminiscent of the Fokker-Planck equation, although here,
there is again some non-Markovianity as the quantum
system can serve as a memory for the classical system.
The Lindbladian term can determine the rate at which the
wave function decoheres, and if this rate is small then the
diffusion term tends to be large. This is to be expected since
as discussed in Sec. I, a purely deterministic evolution on
phase space would decohere the wave function instantly,
and so a slow rate of decoherence requires either a very
noisy stochastic evolution or a very slow jump rate.
It may be worth noting that we can now write a formal
solution of Eq. (17). One way to do this is to double the
Hilbert space [132–134] to write the density matrix ρ̂ðz; tÞ
in its eigenbasis
ρ̂ðz; tÞ ¼

X
pi ðzÞjiihij

ð64Þ

i

αβ
αβ
total divergence term, with the quantity Xαβ
h − γh − D ·

∇ acting as a current. Thus, if we integrate over phase
space, this term also conserves probability, contributing
only a boundary term. Generally though, this term is not
positive by itself, and one typically has to include the full
expansion to ensure this. Looking at each of the terms in
Eq. (17), we see that the first term is just the deterministic

ð63Þ

as a pure entangled state in the Schmidt basis
jρ̂ðz; tÞiAB ¼

X pﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ
pi ðzÞ jiiA ⊗ jiiB :

ð65Þ

i

The CQ master equation of Eq. (61) can then be written as




∂jρ̂ðz; tÞiAB
1 †
1
T

T 
αβ
αβ
¼ −iĤðzÞ ⊗ 1 þ i1 ⊗ Ĥ ðzÞ þ ½λ ðzÞ þ W ðzÞ L̂α ⊗ L̂β − L̂β L̂α ⊗ 1 − 1 ⊗ L̂α L̂β
2
2
∂t

αβ

 ⊗2
− L̂α ⊗ L̂β X αβ
· Dαβ ðzÞ þ    jρ̂ðz; tÞiAB ;
h · ∇ þ L̂α ⊗ L̂β ∇ · γ h ðzÞ þ L̂α ⊗ L̂β ∇

041040-15

ð66Þ

## PDF page 16

JONATHAN OPPENHEIM

PHYS. REV. X 13, 041040 (2023)

where we use the fact that applying an operator to one
subsystem of the entangled state is equivalent to applying
the transpose to the other subsystem [135]. If we designate
the operator in square brackets as L, then the formal
solution to the rate equation is
jρ̂ðz; tÞiAB ¼ eLt jρ̂ðz; 0Þi:

ð67Þ

The generator on the doubled system is in some sense a
Hamiltonian, albeit one with an imaginary part.
A. Realizations of W αβ ðz;z − ΔÞ
Here, we present some simple and constructive examples
for W αβ ðz; z − ΔÞ which have the properties we require,
namely, positive-semidefinite matrices whose first moment
contain a term which generates Hamiltonian flow via
Eq. (58). A simple realization valid for small τ is
1
W αβ ðz; z − ΔÞ ≈ δð2NÞ ½Δ − τXαβ
h ðzÞ:
τ

ð68Þ

This gives the Liouville term as the first moment as
required, and 1=τ as the zeroth moment governing the
collapse rate. We could take τ to depend on α, β, or include
a distribution f αβ over τ. The realization of Eq. (68) can be
considered an approximation of
Z
1
αβ
dΔW αβ ðz; z − ΔÞρ̂ðz − Δ; tÞ ¼ eτfh ;·g ρ̂ðz; tÞ
ð69Þ
τ
with the right-hand side being the exponential of
the
Poisson bracket evolution fhαβ ðq; pÞ; ·g ≔
P
αβ
αβ
k ½ð∂h =∂qk Þð∂=∂pk Þ − ð∂h =∂pk Þð∂=∂qk Þ which generates a finite shift in phase space along the flow generated
by h (dropping the αβ index for simplicity). This is the
classical analog of the evolution operator induced by the
quantum Hamiltonian Ĥ, e−iĤt since


Z τ
Z τ
∂h
∂h
τfh;·g
e
dt ; p þ
dt ; 0
ρ̂ðq; p; 0Þ ¼ ρ̂ q −
∂p
∂q
0
0


∂h
∂h
≈ ρ̂ q − τ ; p þ τ ; 0 :
ð70Þ
∂p
∂q
Then eτfh;·g − 1 acts like a finite-time divergence along the
direction of Hamiltonian flow generated by h.
This leads to a natural noncommuting generalization of
this directional divergence which for a CQ Hamiltonian
with a single Lindblad operator Ĥ ¼ hL̂† L̂, and for
small τ, is
1
1
∇ρ̂ðq; pÞ ≔ eτfh;·g L̂† ρ̂ L̂ − fL̂† L̂; ρ̂gþ :
τ
2τ

ð71Þ

In the case of many Lindblad operators, let us define
basis vectors eαβ and define

∇αβ ρ̂ðz; tÞe

αβ

1
≔
τ

Z

†
dΔW αβ
h ðzjz − ΔÞL̂α ρ̂ðz − Δ; tÞL̂β

1 †
αβ
ð72Þ
− W h ðzÞ fL̂β L̂α ; ρ̂ðz; tÞgþ
2

leading to
L̂α eτfh ;·g ρ̂ðz; tÞL̂†β − 12 fL̂†β L̂α ; ρ̂ðz; tÞgþ
αβ

∇αβ ρ̂ðz; tÞe

αβ

¼

τ

;

ð73Þ
which for small τ looks very much like a finite-directional
divergence (both along the direction X αβ
h and along the
Lindblad operators).
This definition depends on the decomposition of Ĥ into
Lindblad operators, but one can first diagonalize hαβ ðzÞ, in
which case, we write the left-hand side of Eq. (73) as
∇Ĥ ρ̂ðz; tÞ. In cases where
∇αβ ρ̂ðz; tÞeαβ ≈



1
1 †
†
L̂α ρ̂ðz − τXαβ
f
L̂
Þ
L̂
−
;
ρ̂ðz;
tÞg
L̂
þ ;
β
h
τ
2 β α
ð74Þ

it is sometimes the case that Xαβ
h is non-negative (or
nonpositive), in which case this discrete, noncommuting
directional derivative takes the simpler form of a noncommuting finite difference


Xαβ
1 †
αβ
†
h
Xh ∇αβ ρ̂ðz; tÞ ≈
L̂α ρ̂ðz − τÞL̂β − fL̂β L̂α ; ρ̂ðz; tÞgþ :
τ

2

ð75Þ
Care must be taken to ensure it is norm preserving, which is
the case if, for example, Xαβ
h depends only on q and the
jump is in p. Although Eq. (73) looks like a discrete CQ
Poisson bracket, ∇Ĥ ρ̂ðz; tÞ is only linear in ρ̂ðz; tÞ and not
Ĥ. On the other hand, the right-hand side of Eq. (4), which
uses the Aleksandrov-Gerasimenko bracket, is bilinear and
so it does have some properties more akin to a novel
bracket although its action is not CP. The same holds true if
we replace the Aleksandrov-Gerasimenko bracket in
Eq. (4) with the zeroth and first moment of ∇Ĥ ρ̂ðz; tÞ. In
some cases, we can have a bilinear map which is also CP as
in Eq. (75).
The noncommuting divergence is trace preserving and
completely positive, and allows us to write the master
equation as

041040-16

## PDF page 17

A POSTQUANTUM THEORY OF CLASSICAL GRAVITY?
∂ρ̂ðz; tÞ
i
¼ − ½ĤðzÞ; ρ̂ðz; tÞ þ ∇αβ ρ̂ðz; tÞeαβ
∂t
ℏ
i
¼ − ½ĤðzÞ; ρ̂ðz; tÞ
ℏ


1
1
þ L̂α ρ̂ðz; tÞL̂†β − fL̂†β L̂α ; ρ̂ðz; tÞgþ
τ
2
†
− Xαβ
h · L̂α ∇ρ̂ðz; tÞL̂β þ    :

ð76Þ

If we make the model more deterministic (τ → 0), the
strength of the pure-Lindbladian term increases to compensate, while if we make the Lindbladian term small, the
diffusion terms at second order become significant. Here,
we have temporarily switched units to show ℏ, since it
strongly suggests that we set τ ¼ ℏ. Thus, as ℏ → 0, the
decoherence renders the system completely classical, the
diffusion terms and those of higher order go to zero, and we
are left with purely continuous classical equations of
motion. For gravity, the realizations are more tightly
constrained due to diffeomorphism invariance, but similar
realizations can be used to obtain dynamics which recover
general relativity in the classical limit.
B. Example: Qubit coupled to a classical potential
Let us now review a simple system solved in Ref. [106]
with Sparaciari, Šoda and Weller-Davies, which contains
some features we will encounter with gravity [136]. While
the model bears some similarity to the Stern-Gerlach
experiment (cf. also Ref. [75]), the behavior of the spin
can differ depending on how one decomposes the
Hamiltonian in terms of Lindblad operators. Our system
consists of a classical particle which couples to the spin of a
two-level system or the energy of a quantum harmonic
oscillator. The classical degrees of freedom are the position

PHYS. REV. X 13, 041040 (2023)

q ¼ x and momentum p of the particle, with free evolution
given by h00 ¼ p2 =2. We could take the purely classical
evolution from W 00 ðzjz0 ; tÞ to be deterministic or stochastic, and we consider the former here and discuss the latter in
Ref. [106]. We take the total cq Hamiltonian to be given by
ĤðzÞ ¼ p2 =2m þ BðqÞĤ ðmÞ with Ĥ ðmÞ ¼ ω 12 ðâ† â þ ââ† Þ
0
for the oscillator and Ĥ ðmÞ ¼ ðω0 −ω
Þ for the qubit.
To model a Stern-Gerlach experiment, we consider a
two-level system with states j↑i,j↓i and a cq-density matrix
which depends on the classical degrees of freedom.

ρ̂ðq; pÞ ¼

u↑ ðq; pÞ

αðq; pÞ

α ðq; pÞ

u↓ ðq; pÞ


:

ð77Þ

For simplicity, we consider a linear potential BðqÞ ¼ Bq
and a decomposition of the Hamiltonian, Eq. (18), in terms
pﬃﬃﬃ
pﬃﬃﬃ
of Lindblad operators L̂↑ ¼ ωj↑ih↑j, L̂↓ ¼ ωj↓ih↓j
with h↑↑ ðzÞ ¼ −h↓↓ ðzÞ ¼ Bq and the others zero. An
example which builds toward understanding the field
theoretic case is the harmonic oscillator with Lindblad
operators â and â† . This is more interesting in the sense that
the pure-Lindbladian term raises and lowers the state of the
quantum system. In the qubit system, this corresponds to
pﬃﬃﬃ
choosing Lindblad operators L̂↑ ¼ ωj↓ih↑j, L̂↓ ¼
pﬃﬃﬃ
ωj↑ih↓j with diagonal couplings W αβ ðzjz − ΔÞ ¼
δαβ W αβ ðzjz − ΔÞ, or even a single Lindblad operator
pﬃﬃ
L̂ ¼ ðp0ﬃﬃω 0ωÞ. Here, we just present the more trivial first
case decomposition; the other cases, including nontrivial
BðqÞ, are studied both analytically and numerically using
an unraveling approach in Ref. [106]. We take a simple
realization of the discrete dynamics, that of Eq. (68) for
small τ,




X1
∂ρ̂ðq; pÞ
∂hαβ
∂hαβ † 1 †
ðmÞ
00
¼ −i½Ĥ ðq; pÞ; ρ̂ðq; pÞ þ fh ; ρ̂ðq; pÞg þ
L̂ ρ̂ q − τ
;p þ τ
L̂β − fL̂β L̂α ; ρ̂ðq; pÞgþ
∂t
τ α
2
∂p
∂q
α;β



  2
ω 0
p
ω
; ρ̂ðq; pÞ þ j↑ih↑jρ̂ðq; p þ τBÞj↑ih↑j
¼ −iBq
; ρ̂ðq; pÞ þ
τ
2m
0 −ω
ω
ω
þ j↓ih↓jρ̂ðx; p − τBÞj↓ih↓j − f1; ρ̂ðq; pÞgþ :
ð78Þ
τ
2τ
In terms of the matrix elements of the cq state, Eq. (78), the
master equation decouples into two equations for the diagonal
components and one for the off-diagonal coherence term
∂u↑ ðq; pÞ
p ∂u↑ ðq; pÞ ω
¼−
þ ½u↑ ðq; p þ τBÞ − u↑ ðq; pÞ;
m
τ
∂t
∂q
∂u↓ ðq; pÞ
p ∂u↓ ðq; pÞ ω
¼−
þ ½u↓ ðq; p − τBÞ − u↓ ðq; pÞ;
m
τ
∂t
∂q

∂αðq;pÞ
p ∂αðq; pÞ ω
¼ −2iBqωαðq; pÞ −
− αðq; pÞ: ð80Þ
∂t
m ∂q
τ

Equation (80) has a solution

ð79Þ

041040-17



pt
p
ωt
αðq; pÞ ¼ ρ q − t e−2iBωtðq−2mÞ− τ ;
m

ð81Þ

## PDF page 18

JONATHAN OPPENHEIM

PHYS. REV. X 13, 041040 (2023)

where ρðq − ptÞ is any normalized function of its argument.
We see that the coupling of the qubit results in decoherence,
since the off-diagonal elements decay exponentially fast.
More than that, the wave function collapses into a
definite state of being in the up or down state. This we
see through the equation for the diagonal terms. Comparing
Eq. (79) to Eq. (12), we see that at a rate of ω=τ the system
undergoes jumps in momentum by τB depending on its
state. Since we can monitor the classical degrees of freedom
without disturbing the system, measuring the change in
momentum will uniquely determine the value of the spin. In
this sense, the interaction leads to more than just
decoherence, but an objective collapse of the wave function
[69,100]. While the basis to which the quantum state
collapses can appear arbitrary in spontaneous collapse
models, here it is determined by the form of the CQ
interaction which will be tightly constrained by the requirement of reproducing Einstein gravity in the classical limit.
More generally, if the backreaction force ∇hαβ is unique
when diagonalized, then monitoring the classical system
uniquely determines which Lindblad operators were
applied to the state. Thus, an initially pure quantum state
remains pure conditioned on the classical degrees of
freedom. In the continuous realizations of the theory, this
has since been shown to be generically true in Ref. [29]
with Layton and Weller-Davies, provided an inequality we
call the decoherence-diffusion trade-off is saturated.
The solution (a Poisson distribution) for the diagonal
terms of ρ̂ in this and a more general setting is given in
Ref. [106], but the evolution can be understood in broad
terms by inspection. The particle is making a momentum
jump of τB at a rate of ω=τ, so on average it has an
acceleration of ωB exactly as we expect for a SternGerlach device. We can imagine that at each dt, there is a
probability of the particle undergoing a jump in momentum, so by the law of large numbers, we expect the particle
to have made on average ωt=τ jumps, normally distributed
with a variance of ωτ ½1 − ðω=τÞ. If we Taylor expand
Eq. (79)
∂uðq; pÞ
p ∂uðq; pÞ
∂uðq; pÞ
¼−
 ωB
∂t
m ∂x
∂p
þ

ωB2 τ ∂2 uðq; pÞ
þ 
2
∂p2

ð82Þ

(where u is u↑ or u↓ for , respectively), then to first order
we have a particle undergoing acceleration ωB depending
on its spin, as expected, with a diffusion term at higher
order. However, care must be taken, as if we truncate the
Taylor expansion, the density matrix can become negative.
Equation (78) is completely positive however, and can be
understood as follows: An initial pure state in superposition
will initially have a constant momentum, but will then
undergo jumps in momentum of finite size τB, and at a rate

ω=τ. This causes the state to collapse to the up or down
state, at a rate ω=τ.
If we trace out the qubit and look at the average value of
the particle’s trajectory, then for a uniform superposition of
up and down spin, it will have zero average acceleration,
but if we look at the full state, the particle undergoes
acceleration (albeit stochastically) in a direction which
depends on the value of the spin. We thus see that the
evolution of the particle corresponds to the left panel of
Fig. 1, not the right one.
C. Postquantum field theory
In order to consider applying our master equation to field
theories, we must first ensure that it can be made Lorentz
covariant. Although it was initially thought that such
dynamics are impossible [137], GKSL equations which
are covariant under the proper orthochronous Lorentz
group were introduced in Ref. [138]. This was further
taken up in Refs. [65,66] (see also Ref. [139]). A Lorentzinvariant Schwinger-Keldish action for open quantum
scalar field theory was used to show that the GKSL
equation for scalar field theories is renormalizable [140].
The formalism used there is manifestly Lorentz invariant.
There are however subtleties that have since been clarified
with Weller-Davies in Ref. [141]. The full master equation
of Ref. [140] is not completely positive, but one can find
Lorentz-invariant master equations which are CP, Lorentz
invariant, and renormalizable, as well as master equations
which are CP, renormalizable, and Lorentz covariant, but
not Lorentz invariant. The Lindbladian corresponding to
the discrete realization presented in Sec. V is covariant but
not invariant, while the Lindbladian of the continuous
realization is invariant but not covariant. This apparent
paradox is resolved by showing that transformations of
space-time are not generated by a unitary, but rather, by the
semigroup inherited from the Lindbladian, and thus, there
are different notions of invariance and covariance [141].
Here, we focus on covariance conditions, and address the
subtleties in more detail in Refs. [141,142].
In order to make the dynamics here Lorentz covariant,
one can begin by choosing Lindblad operators and couplings, such that the right-hand side of Eq. (14) transforms
like ∂=∂t, so that both sides of the equation transform in the
same way under a Lorentz boost. This has been referred to
as a minimal Lorentz-covariance requirement [137]. We
first construct a field theory version of Eq. (14) and then
discuss how to make it covariant under the proper orthochronous Lorentz group.
To obtain the field-theoretic version of the master
equation, we take the Lindblad operators L̂α to also depend
on the spatial coordinate x and in particular, take them to be
local field operators L̂α ðxÞ. We can think of them as
carrying a double index α, x. This requires the couplings
W to carry not just an index αβ but also x, y. Then, instead
of a sum or integral over just α, β, we also have an integral

041040-18

## PDF page 19

A POSTQUANTUM THEORY OF CLASSICAL GRAVITY?
over x,y, and write the couplings as W αβ ðzjz0 ; x; yÞ with the
phase-space degrees of freedom z being local fields at each
point x.
Cluster separability [64] demands that the coupling
constants W αβ ðzjz0 ; x; yÞ be delta functions in x, y [60],
and that the coupling to phase-space variables z be to the
local classical field zðxÞ. A violation of cluster separability
can result in violations of Lorentz invariance, with correlations or entanglement being created over spacelike separations. However, the creation of correlations need not
violate causality or allow for superluminal signaling [65].
Thus, while it is desirable to have W αβ ðzjz0 ; x; yÞ be delta
functions, for greater generality we allow the coupling
constants W αβ ðzjz0 ; x; yÞ to have support at finite jx − yj.

PHYS. REV. X 13, 041040 (2023)

Should these couplings not fall off fast enough with
increasing jx − yj, the theory is likely to run afoul of
experiment. For the cq state at z, we continue to write it
as ρ̂ðz; tÞ with the understanding that it lives in Fock space,
and is an operator-valued distribution functional of the
classical fields zðxÞ over the entire manifold of points x.
If we consider the points x to be on a lattice, with the
continuum obtained in the limit that the lattice spacing goes
to zero, then we can think of the measure Dz over phase
space as Πx dqðxÞdpðxÞ, and in the continuum limit, the
master equation is given by a functional integral.
If we take the Lindblad operators to be local field
operators L̂α ðxÞ, then the field-theoretic version of
Eqs. (14) and (17) is

Z
∂ρ̂ðz; tÞ
†
¼ −i½ĤðzÞ; ρ̂ðz; tÞ þ dxd3 yDΔW αβ
h ðzjz − Δ; x; yÞL̂α ðxÞρ̂ðz − Δ; tÞL̂β ðyÞ
∂t
1
− W αβ
ðz; x; yÞfL̂†β ðyÞL̂α ðxÞ; ρ̂ðz; tÞgþ
2 h


Z
1 †
†
f
L̂
ðz;
x;
yÞ
L̂
ðxÞρ̂ðz;
tÞ
L̂
ðyÞ
−
ðyÞ
L̂
ðxÞ;
ρ̂ðz;
tÞg
¼ −i½ĤðzÞ; ρ̂ðz; tÞ þ dxd3 yW αβ
α
α
þ
β
h
2 β

Z
αβ
†
†
− dx Xαβ
h ðz; xÞL̂α ðxÞ · ∇ρ̂ðz; tÞL̂β ðxÞ − ∇ · Dh ðz; x; yÞ · L̂α ðxÞρ̂ðz; tÞL̂β ðyÞ ∇

Z
†
− dx∇ · ½γ αβ
ðz;
x;
yÞ
L̂
ðxÞρ̂ðz;
tÞ
L̂
ðyÞ
þ :
α
β
h

ð83Þ

ð84Þ

One can also consider master equations which contain multiple jumps at higher order, i.e.,
Z
DΔdx1 dx2 …W α1 β1 ;α2 β2 … ðzjz − Δ; x1 ; x2 ; …Þ    L̂α2 ðx2 ÞL̂α1 ðx1 Þρ̂ðz − Δ; tÞL̂†β1 ðx1 ÞL̂†β2 ðx2 Þ    ;

but we do not do so here.
In flat space, one can consider as an example the scalar
field discussed later in Sec. V, and take the pure-Lindbladian
coupling term W αβ ðz; x; yÞ to be close to a delta function and
proportional to 1=τ. If we wish to reproduce Hamiltonian
dynamics in the classical limit, then we generally take the Xαβ
h
term to transform just as the Poisson bracket would for a
Lorentz-invariant classical field theory, since the only difference between it and fĤðzÞ; ρ̂ðz; tÞg is operator ordering.
As an example, we could decompose the Hamiltonian of
the field theory in terms of the Lindblad operators used in
Refs. [66,138,140]
Z
ĤðxÞ ¼ dxhαβ ðz; xÞL̂†β ðxÞL̂α ðxÞ
ð85Þ
with hαβ ðz; xÞ coupling the quantum field to a classical field
zðxÞ, which in the case of gravity, we can take to be the
3-metric and its conjugate 3-momentum. The couplings

Xαβ
h ðz; xÞ ¼

δhαβ ðz; xÞ
δzðxÞ

ð86Þ

then reproduce the Hamiltonian backreaction of the quantum fields on the classical ones. If one wants to be explicit
about W αβ ðzjz0 ; x; yÞ, one can use the realization presented
in Sec. V.
In Ref. [71], we show that depending on the decomposition hαβ ðz; xÞ, there are discrete dynamics or
continuous dynamics. In particular, it is shown that the
Kramers-Moyal expansion in Eq. (84) never terminates and
leads to finite-sized jumps in phase space unless the only
00
nonzero Dαβ
h ðz; x; yÞ is Dh ðx; yÞ, and the only nonzero
α0
0α
Xαβ
h ðz; xÞ is X h ðz; xÞ and X h ðz; xÞ, and the higher-order
terms all vanish. In other words, the continuous master
equation is obtained by restricting the decomposition of
Eq. (85) to include only terms

041040-19

## PDF page 20

JONATHAN OPPENHEIM
Z
ĤðxÞ ¼

PHYS. REV. X 13, 041040 (2023)

dxh0α ðz; xÞ1L̂α ðxÞ;

ð87Þ

while otherwise, one has discrete dynamics.
The positivity conditions in the field-theoretic case
are analogous to the finite-dimensional conditions of
Eq. (50). Recalling that for 2n phase-space degrees of
freedom per point, D00
h ðz; x; yÞ is a 2n × 2n matrix over x, y
and denoting W h ðz; x; yÞ as the matrix with elements
W αβ
h ðz; x; yÞ, and X h ðz; xÞ as the vector with elements
0α
Xh ðz; xÞ, the continuous master equation is completely
positive, provided that the square matrix


D00
h ðx; yÞ

δðx; yÞXh ðz; yÞ

X†h ðz; xÞδðx; yÞ

W h ðz; x; yÞ


≽ 0;

ð88Þ

which for invertible W h ðz; x; yÞ is equivalent to the condition that D00
h ðx; yÞ be positive semidefinite along with its
Schur complement
†
−1
D00
h ðx; yÞ − X h ðz; xÞW h ðz; x; yÞX h ðz; yÞ ≽ 0;

ð89Þ

where W −1
h ðz; x; yÞ is the generalized inverse of W h ðz; x; yÞ.
The positivity condition for singular W h ðz; x; yÞ is a straightforward extension of Eq. (89); see, for example, Ref. [143].
We have since shown that the condition given by Eq. (89)
holds for the zeroth, first, and second moments of any
consistent classical quantum coupling, and provides an
experimentally testable signature of classical gravity [50],
Turning back to Lorentz covariance, one might worry
that in the master equation of Eq. (84), there is a
dependence on the choice ∂t ,
∂t ρ̂ðz; tÞ ¼ Lt ρ̂ðz; tÞ:

ð90Þ

As discussed in Ref. [138], we can consider any four-vector
a from the future cone F þ , i.e., a · a ≥ 0, and a0 ≥ 0, and
consider the dynamics ∂a ρ̂ðz; tÞ ¼ La . Indeed, consider M
an element of the proper orthochronous Lorentz group. Let
πða; MÞ be a representation of the Poincaré group and let
the evolution of the state ρ̂ðz; tÞ be given by a completely
positive trace-preserving Markovian map E a . The Lorentzcovariance condition as defined in Ref. [138] (see also
Refs. [66,144]) is then
πða; MÞE b πða; MÞ−1 ¼ E Mb

ð91Þ

considered in Ref. [138]. The relationship between this
covariance condition and Lorentz invariance is discussed in
Ref. [141].
V. POSTQUANTUM GENERAL RELATIVITY
We now have a procedure to take a Hamiltonian, which
couples classical and quantum degrees of freedom, and use
it to generate consistent hybrid dynamics. Let us now do
that for general relativity coupled to quantum matter via the
energy-momentum tensor. We do so in the ADM formulation of general relativity [118,145], whose classical
formulation we now recall. One starts with a slicing up
of space-time into spacelike hypersurfaces labeled by the
parameter t, and with coordinates x. The hypersurfaces are
endowed with a 3-metric gab with determinant g at each
point x. We often drop the explicit x dependence from field
degrees of freedom, since all quantities should be assumed
to be locally defined, unless they are a functional, in which
case, this is indicated with square brackets. We put in the
explicit x dependence when we have two integrals over
space, or if there could be any ambiguity. The components
of the 3-metric are the canonical coordinates, and π ab their
conjugate momenta
pﬃﬃ
π ab ¼ gðK ab − gab KÞ
ð92Þ
with K ab the extrinsic curvature and K its trace.
In general relativity, one is free to choose the timelike
direction by arbitrarily specifying a lapse N and shift vector
N a at each point x. The evolution of the hypersurfaces is
then governed by the classical ADM Hamiltonian
Z
ðtotÞ
HADM ½N; ⃗N ≔ dxðNHðtotÞ þ N a Ha Þ
I
þ ds × HðboundaryÞ ;
ð93Þ
and we now define the various terms appearing in it. HðtotÞ
is called the total super-Hamiltonian and is typically written
in terms of a pure gravity part, and a term which contains
the matter fields
HðtotÞ ¼ HðgrÞ þ HðmÞ :

The first term is the purely gravitational part of the superHamiltonian given by
HðgrÞ ≔ Gabcd π ab π cd − g1=2 R

þ

for any b ∈ F . In other words, if we perform a boost from
the lab frame, evolve the state, then boost back into the lab,
one gets the same final state as evolving the initial state in
the lab for the boost time. The open quantum scalar field
theory we consider in the next section satisfies this property
when the background space-time is flat, as can be seen from
the fact that in that limit, it is equivalent to the Lindbladian

ð94Þ

ð95Þ

with R the intrinsic curvature on the 3-manifold analogous
to a potential term, while the first term is analogous to a
kinetic term, with Gabcd the deWitt metric,

041040-20

1
Gabcd ¼ g−1=2 ðgac gbd þ gad gbc − gab gcd Þ:
2

ð96Þ

## PDF page 21

A POSTQUANTUM THEORY OF CLASSICAL GRAVITY?
HðmÞ is the matter Hamiltonian density, and we take it to
pﬃﬃ
also include the cosmological constant term ggab Λcc .
ðtotÞ
The total supermomentum Ha is given by
ðtotÞ

Ha

ðgrÞ

¼ Ha

ðmÞ

þ Ha

ðgrÞ

HðgrÞ ½N; ⃗N ≔
H

ðmÞ

½N; ⃗N ≔

Z

ðgrÞ

dxðNHðgrÞ þ N a Ha Þ;

Z

ðmÞ

dxðNH

ðmÞ
þ N Ha Þ:
a

ð98Þ

With the Hamiltonian now defined, let us turn to the
equations of motion. The dynamics is given by Hamilton’s
equations
∂gab δHADM ½N; ⃗N
¼
;
∂t
δπ ab

∂π ab
δH
½N; ⃗N
¼ − ADM
; ð99Þ
δgab
∂t

where δ indicates the Fréchet derivative. In order for these
dynamics to be invariant under the choice of the lapse N
and shift N a , we need to impose primary constraints on
their conjugate momenta
PN ≈ 0;

PN a ≈ 0;

ð100Þ

where ≈ denotes that the constraints are weakly zero in the
sense that they vanish only on part of the phase space (the
constraint surface). To ensure that these primary constraints
are conserved in time, i.e., that
ṖN ¼ 0;

ṖN a ¼ 0;

ð101Þ

we require secondary constraints
HðtotÞ ≈ 0;

ðtotÞ

Ha

≈ 0:

∂ρðg; π; tÞ
⃗ ρg
¼ fHADM ½N; N;
∂t
⃗ ρgg þ fH ðmÞ ½N; N;
⃗ ρgm
¼ fHðgrÞ ½N; N;
þ fHðmÞ ½N; ⃗N; ρgg ;

ð97Þ

with Ha ≔ −2gac ∇b π cb the purely gravitational contribution, and ∇b the covariant derivative with respect to the
ðmÞ
Levi-Civita connection for the 3-metric. Ha is the matter
contribution. The final term in Eq. (93) is the boundary term,
and we ignore it in the present paper, although the formalism
can be extended to apply to its inclusion. Finally, it proves
convenient to define the total gravitational Hamiltonian
⃗ and the total matter Hamiltonian HðmÞ ½N; N
⃗
HðgrÞ ½N; N
⃗ ¼ H ðgrÞ ½N; N
⃗ þ
as functionals so that HADM ½N; N
ðmÞ
H ½N; ⃗N and

ð103Þ

where we divided up the Poisson bracket into one with
respect to the pure gravitational degrees of freedom
fHðmÞ ½N; ⃗N; ρgg

 ðmÞ
Z
⃗ δρ δH ðmÞ ½N; N
⃗ δρ
δH ½N; N
;
≔ dx
−
δgab
δgab
δπ ab
δπ ab

ð104Þ

and one with respect to the matter degrees of freedom,
which for a scalar field with conjugate variables ϕ,π ϕ at
each point x would be
fHðmÞ ½N; ⃗N; ρgm

 ðmÞ
Z
δH ½N; ⃗N δρ δHðmÞ ½N; ⃗N δρ
:
¼ dx
−
δϕ
δπ ϕ
δπ ϕ
δϕ

ð105Þ

The Poisson bracket with respect to the lapse and shift and
their conjugate momenta is zero when the constraints are
satisfied and is usually not included in the definition of
the Poisson bracket. When we discuss the classical quantum theory, it may be useful to also include them in the
definition of the Poisson bracket.
When only matter is quantum, the matter Poisson
bracket of Eq. (105) just becomes the commutator
⃗ ρ̂ which is unproblematic, and just repre−i½ĤðmÞ ½N; N;
sents the evolution of the quantum fields on a spatial
manifold endowed with an evolving classical metric. This
is just quantum field theory in curved space. However, the
Poisson bracket of Eq. (104) is the backreaction of the
quantum fields on space-time, and this is the dynamics we
now seek to describe in terms of CQ dynamics.
We first replace T μν with the stress tensor of quantum
pﬃﬃ
field theory, ĤðmÞ ¼ gT̂ 00 . We can now write
ĤðtotÞ ¼ HðgrÞ þ ĤðmÞ ;

ð106Þ

as long as we recall that this object is hybrid and cannot be
used to derive classical or quantum evolution in the
traditional way. For the discrete master equation, we
expand ĤðtotÞ in terms of local field operators L̂α ðxÞ, so
that dropping the explicit x dependence

ð102Þ

The constraints, once initially satisfied, are preserved by the
dynamical equations of motion.
One can write a Liouville equation for classical general
relativity

PHYS. REV. X 13, 041040 (2023)

ĤðtotÞ ¼ HðgrÞ 1 þ hαβ ðg; πÞL̂†β L̂α

ð107Þ

with L̂0 ðxÞ ¼ 1 multiplying the purely classical part of the
super-Hamiltonian. For convenience, we explicitly separate
out the pure gravity contribution HðgrÞ , and one can then

041040-21

## PDF page 22

JONATHAN OPPENHEIM

PHYS. REV. X 13, 041040 (2023)

take h00 ¼ 0. Although in our derivation of the master
equation, we take the L̂α to be a basis and L̂α to be traceless,
one can show as with the Lindblad equation, that any set of
Lindblad operators can be put into this standard form [71],
and so we henceforth do not assume that the other L̂α are
traceless. We often consider matter which is minimally
coupled, meaning ĤðmÞ does not depend on π ij so that we
can write hαβ ðgÞ. For the continuous master equation, which
we consider elsewhere [146], we use Lindblad operators
ðmÞ
⃗
⃗ and L0 ¼ 1.
L̂ij ¼ δĤðmÞ ½N; N=δg
½N; N,
ij , Ĥ
The supermomentum can be treated similarly, where the
stress-energy term in Eq. (97) is replaced by its quantum
counterpart
ðmÞ

Ha

ðmÞ

→ Ĥa

ð108Þ

†
¼ Ha 1 þ pαβ
a ðgÞL̂β L̂α

ð109Þ

leading to
ðtotÞ

Ĥa

ðgrÞ

for the discrete master equation. Although the matrix with
elements N a pαβ
a is not generally a positive-semidefinite
matrix, the combination Nhαβ þ N a pαβ
a is.
To make things concrete, it is useful to have in mind a
scalar field, especially since the general case can be treated
similarly and Lindbladian evolution of ϕ4 theory has been
shown to be renormalizable in this case [140], albeit with
the caveats mentioned in Sec. IV C. We have [147]
1
pﬃﬃ
pﬃﬃ
ĤðmÞ ¼ ðg−1=2 π 2ϕ þ ggab ∇a ϕ∇b ϕ þ gm2 ϕðxÞ2
2
pﬃﬃ
− 4 gΛcc Þ;
ð110Þ
ðmÞ

Ĥa

¼ π ϕ ∇a ϕ:

ð111Þ

For the discrete evolution, we can now decompose the
Hamiltonian as in Eq. (107), with the metric degrees of
freedom included in hαβ ðg; πÞ.,
hππ ≔ g−1=2 ;
pﬃﬃ
hab ≔ ggab ;

pﬃﬃ
g;
p
ﬃﬃ
hΛΛ ¼ g;
hϕϕ ≔

ð112Þ

with the rest zero, leaving the local Lindblad operators as
1
L̂π ¼ pﬃﬃ π ϕ ;
2
1
L̂a ¼ pﬃﬃ ∂a ϕ;
2

m
L̂ϕ ¼ pﬃﬃ ϕ;
2
pﬃﬃﬃﬃﬃﬃ
L̂Λ ¼ 2ΛjΛihΛj:

ð113Þ

Note that the hαβ ðg; πÞ do not include the N prefactor, since
we use it to apply the constraint equation; however, when
we look at the dynamical equations of motion, we need to

include it. We choose a simple form for L̂Λ, but a priori,
other choices are possible, for example, the shift operator.
Their particular dependence is not important in terms of the
broad outline of this discussion, rather, what is important is
that we can decompose ĤðmÞ in terms of local field
operators. The expansion of the supermomentum in terms
of local operators could be treated similarly, with
L̂π ¼ π ϕ ;

L̂a ¼ ∂a ϕ;

L̂1 ¼ 1:

ð114Þ

ðmÞ

Note that Ĥa has no metric dependence and thus does not
contribute to the backreaction.
Although we cannot generally define Fock states locally
on a Cauchy slice, if we know, for example, that the
dynamics will lead to a space-time which asymptotically
has a timelike Killing vector, then we can choose a vacuum
state and set of creation and annihilation operators
â ⃗p ðgÞ,â†⃗p ðgÞ, which depend on the metric to expand the
matter Hamiltonian as
Z
1
d3 p
ðmÞ
⃗
H ½N; N ¼
ω ðâ† ðgÞâ ⃗p ðgÞ þ â ⃗p ðgÞâ†⃗p ðgÞÞ;
2 ð2πÞ3 ⃗p ⃗p
ð115Þ
where we drop the cosmological constant term for simplicity.
In a fixed background, for example, the Lindblad equation
using the Lindblad operators of Eq. (113) are equivalent to
those of Eq. (115). In this way, one sees the covariance of the
master equation; however, for general dynamical spacetimes, an expansion of local operators in terms of creation
and annihilation operators is not possible, and we use local
Lindblad operators such as those of Eq. (113).
The dynamical equations of motion are generated by the
CQ-ADM Hamiltonian
Z
ðtotÞ
Ĥ ADM ½N; ⃗N ¼ dxðN ĤðtotÞ þ N a Ĥa Þ
ð116Þ
ðtotÞ

with ĤðtotÞ and Ĥa given by Eqs. (107) and (109). If we
wish the dynamics to be invariant under the choice of lapse
and shift, this would place strong constraints on it. It seems
to require that the stochastic part of the master equation be
generated by NW αβ
h ðzjz − Δ; x; yÞ, i.e., that the model be
linear in the sense that W αβ
Nh ðzjz − Δ; x; yÞ can be replaced
αβ
by NW h ðzjz − Δ; x; yÞ and W αβ
N a pa ðzjz − Δ; x; yÞ by

N a W αβ
pa ðzjz − Δ; x; yÞ. This is analogous to replacing
fNHðtotÞ ; ρg by NfHðtotÞ ; ρg in the classical case, since
they are equal when the constraint HðtotÞ ≈ 0 is satisfied. In
what follows, we take the lapse and shift outside the
functional derivatives under the assumption that they either
have no explicit metric dependence or the constraints are
satisfied. The constraints in this theory will not be those of
GR, but must be modified. As noted in Ref. [156], it is not

041040-22

## PDF page 23

A POSTQUANTUM THEORY OF CLASSICAL GRAVITY?
strictly necessary that the dynamics be invariant under the
choice of N and N a , and there are sensible theories which
break this, such as shape dynamics [157–159] or unimodular gravity [160–166], but it is desirable to have some
local symmetry, even if it is not full diffeomorphism
invariance.
∂ρ̂ðz; tÞ
¼
∂t

Z

PHYS. REV. X 13, 041040 (2023)
We do not restrict ourselves to a particular realization of

αβ
W αβ
h ðzjz − Δ; x; yÞ and W pa ðzjz − Δ; x; yÞ at this point, but

we assume that the realization satisfies this linear condition
and then present realizations which have this property. We
thus have the master equation

Z

ðgrÞ
⃗ ρ̂ðz; tÞ
dxNfH ; ρ̂ðz; tÞg þ dxN a fHa ; ρ̂ðz; tÞg − i½HðmÞ ½N; N;


Z
1
αβ
αβ
†
†
þ dxdyDΔ NW h ðzjz − Δ; x; yÞL̂α ðxÞρ̂ðz − ΔÞL̂β ðyÞ − NW h ðz; x; yÞfL̂β ðyÞL̂α ðxÞ; ρ̂ðz; tÞgþ
2


Z
1
αβ
αβ
†
†
þ dxdyDΔ N a W pa ðzjz − Δ; x; yÞL̂α ðxÞρ̂ðz − ΔÞL̂β ðyÞ − N a W pa ðz; x; yÞfL̂β ðyÞL̂α ðxÞ; ρ̂ðz; tÞgþ ;
2
ðgrÞ

where we write z for the phase-space degrees of freedom
when gab ,π ab are too cumbersome and have absorbed the
bare term λαβ ðz; x; yÞ into W αβ
h ðzjz − Δ; x; yÞ. The functional integral DΔ is over the phase space. Here we take the
lapse N and shift N a outside the Poisson bracket, under
the assumption that the constraints (suitably modified from
the deterministic theory) are satisfied [156].
The first two terms of Eq. (117) correspond to the
deterministic classical evolution associated with the
Lindblad operators L̂0 ¼ 1. The dynamics associated with
this classical part could be stochastic, and could a priori
include jumping or diffusion terms as well as friction terms.
We take such terms to be included in W 00
h ðzjz − Δ; xÞ.
Because they are associated with L̂0 , they do not need to be
positive.
The next term is the commutator of the state with the
matter Hamiltonian describing how quantum matter
evolves in a background space-time. Finally, we have
∂ρ̂ðz; tÞ
¼
∂t

ð117Þ

the interaction terms between gravity and matter which
must be stochastic. Two particular choices of W αβ ðz; x; yÞ
are given as Eqs. (120) and (125), and in both cases, the
integral over Δ can be removed. As shorthand, we denote
Eq. (117) by
∂ρ̂ðg; π; tÞ
¼ LĤADM ρ̂ðg; π; tÞ
∂t
Z
¼ dx½NLρ̂ðg; π; tÞ þ N a La ρ̂ðg; π; tÞ: ð118Þ
ðmÞ

Because Ĥa has no metric dependence, the evolution along
N a can be pure Lindbladian or purely deterministic. In
Ref. [156], we argue that diffeomorphism invariance requires
αβ
the latter, i.e., that W αβ
pa ðzjz − Δ; x; yÞ ¼ W pa ðz; x; yÞ ¼ 0.
Equation (117) then simplifies to



ðgrÞ
ðgrÞ
a
ðmÞ
dx NfH ; ρ̂ðz; tÞg þ N fHa ; ρ̂ðz; tÞg − i½H ½N; ⃗N; ρ̂ðz; tÞ


Z
1 αβ
αβ
†
†
þ dxdyNDΔ W h ðzjz − Δ; x; yÞL̂α ðxÞρ̂ðz − Δ; tÞL̂β ðyÞ − W h ðz; x; yÞfL̂β ðyÞL̂α ðxÞ; ρ̂ðz; tÞgþ :
2
Z

This should be thought of as the fundamental dynamical equation, but we can perform a Kramers-Moyal
expansion on it. Since we expect all moments to appear,
the moment expansion will include terms such as
ðδhαβ =δgab Þ½δρ̂ðz; tÞ=δπ ab  since it transforms like a density. This moment at zeroth order in τ is needed to recover
the classical limit of general relativity. We now require a
positive transition matrix W αβ
h ðzjz − Δ; x; yÞ [except for
the W 00
ðzjz
−
Δ;
x;
yÞ
component],
and that each moment
h
transforms as a density to ensure invariance of the

ð119Þ

dynamics under spatial diffeomorphism. An example of
such a realization for the discrete master equation is given
in Ref. [156]; namely, for α, β ≠ 0,
Z
†
dyDΔNW αβ
h ðzjz − Δ;x;yÞL̂α ðxÞρ̂ðz − Δ; tÞL̂β ðyÞ

α
N
−1
¼ exp τðh Þðz;xÞfhðz;xÞ;·g
τ
γ

041040-23

× hβγ ðz;xÞL̂α ðxÞρ̂ðz;tÞL̂†β ðxÞ;

ð120Þ

## PDF page 24

JONATHAN OPPENHEIM

PHYS. REV. X 13, 041040 (2023)

where exp½Mαγ is the components of the matrix exponential of the matrix M and it is purely local in x. Here,
M has components Mki ¼ ½τðh−1 Þij ðzÞfhjk ðzÞ; ·g and
W αβ ðz;x;yÞ ¼ ð1=τÞhαβ ðz;xÞδðx;yÞ, and gives a KramersMoyal expansion up to constants of
Z
W αβ
h ðzjz − ΔÞρ̂ðz − Δ; tÞDΔ
1
δhαβ ðzÞ δρ̂ðz; tÞ δhαβ ðzÞ δρ̂ðz; tÞ
¼ hαβ ðgab Þρ̂ðz; tÞ þ
−
τ
δgab δπ ab
δπ ab δgab
þ τDabcd;αβ ðgÞ

δ2 ρ̂ðz; tÞ
þ ;
δπ ab δπ cd

ð121Þ

have only diffusion in π ab . Higher-order functional derivatives in π ab can be suitably smeared to control divergences. If we want to ensure that our evolution equation is
invariant under canonical transformations, we can express
it in terms of Poisson brackets, with the second-order term
being written, for example, as fJ o ; fJi ; ρ̂ðz; tÞgg. It may
also be necessary to include the lapse, shift, and their
conjugate momenta in the Poisson bracket, which is a
realization we pursued in Ref. [146].
There is more freedom when it comes to W 00
h ðzjz − Δ;
x; yÞ which could include dispersion terms, non-Brownian
terms, or even friction terms such as those of the form
δγ ab ρ̂
;
δπ ab

where the diffusion terms Dabcd;αβ ðgÞ and all higher-order
moments are tensor densities of the appropriate weight to
contract with the derivatives acting on the density matrix.
The absence of functional derivatives with respect to g
higher than δρ̂=δgab means that this is a Brownian
realization. As a result, Eq. (92) is unmodified, and we
∂ρ̂ðz; tÞ
¼
∂t

γ ab ≔ ηabcd

δHðgrÞ
δπ cd

ð122Þ

with ηabcd a local function of the metric. However, gauge
invariance places strong restrictions on these terms, and
here we leave them unspecified and denote them by the
differential operator Γ00 ρ̂. The resulting evolution law is



ðgrÞ
dx NfHðgrÞ ; ρ̂ðz; tÞg þ N a fHa ; ρ̂ðz; tÞg − i½HðmÞ ½N; ⃗N; ρ̂ðz; tÞ
 Z

Z
1 αβ
1 †
†
þ dx Nh ðzÞ L̂α ρ̂ðz; tÞL̂β − fL̂β L̂α ; ρ̂ðz; tÞgþ þ dxNΓ00 ρ̂ðz; tÞ
τ
2
 αβ
Z
δh
δρ̂ðz; tÞ †
δ2
abcd;αβ
þ dxN
þ
τD
ðgÞ
þ :
L̂α
L̂
π
β
δgab
δπ ab
δπ ab π cd
Z

Let us now see that in the classical limit, we recover
general relativity to leading order. For convenience of
presentation, we consider the case where the quantum
system is uncorrelated with the classical system. The more
general case is akin to Eq. (23). Recalling Eq. (9), that
ρðz; tÞ ≔ trρ̂ðz; tÞ, we perform the trace on the quantum
system in Eq. (123). Dropping terms of second order and
higher we are left with

ð123Þ

A realization which gives the continuous master equation will be discussed in Ref. [50] with Sparaciari, Šoda and
Weller-Davies and Ref. [146], and is given by

ð124Þ

Z
dxNfH; ρ̂g þ dxN a fHa ; ρ̂g − i½ĤðmÞ ½N; ⃗N; ρ̂
Z
1
þ
dxNðfĤðmÞ ; ρ̂Þg − fρ̂; ĤðmÞ gÞ
2


Z
1
þ
dxdyNλμνσ̂τ ðg;x;yÞ L̂μν ðxÞ; ½ρ̂; L̂σ̂τ ðyÞ
2
Z
1
0
þ
dxdyNfDαβ
2 ðx;yÞJ α ðg; xÞ;fJ β ðg; yÞ; ρ̂gg ð125Þ
2

which, when the constraints of GR are satisfied, is the
classical Liouville equation for the gravitational degrees of
freedom of general relativity sourced by quantum matter.
The third term gives the backreaction we expect. We thus
see that in the classical limit we recover Einstein’s
equations. To leading order, the evolution of the quantum
fields is seen from Eq. (123) to correspond to the ordinary
commutator terms (quantum field theory in curved space)
plus a Lindbladian term.

when the constraints are satisfied. Here, L̂ij ≔
ðδĤðmÞ =δgij Þ, L̂nn ≔ ĤðmÞ , and the pure-Lindbladian couplings λμνσ̂τ ðg; x; yÞ consist of submatrices with elements
λijkl ≔ D0;ijkl ðg; x; yÞ, λijnn ðg; x; yÞ, λnnkl ðg; x; yÞ, and the
constant λnnnn ðg; x; yÞ. Here, greek indices are akin to
space-time indices μ ¼ n, i, and we use n instead of 0
since 0 already corresponds to the 1 Lindblad operator.
The condition for complete positivity can be found from
Eq. (89). Denoting the generalized inverse of the matrix

∂ρ̂ðz; tÞ
¼
∂t

Z

ðgrÞ

Z

∂ρ̂
¼
∂t

ðgrÞ

dxNfH ; ρg þ N a dxfHa ; ρg
Z
pﬃﬃ
þ dx gtrNfĤðmÞ ; ρ̂g þ    ;

041040-24

Z

## PDF page 25

A POSTQUANTUM THEORY OF CLASSICAL GRAVITY?
D0 ðg; x; yÞ as D−1
0 , we require that the matrix with elements
ijkl
0
D0 ðx; yÞ
and
Dαβ
2 ½δJ α ðg; xÞ=δgij ½δJ β ðg; yÞ=δgkl  −
ijkl
ðD−1
ðx; yÞ be positive semidefinite as a matrix and
0 Þ
kernel to guarantee complete positivity of the master equa⃗
⃗
tion. Dαβ
2 ðx; yÞ, J α ðN; N; g; xÞ, and D0;ijkl ðN; N; g; x; yÞ
are chosen so that the realization is linear in the lapse
and shift. If we take the Jα to be local in the metric,
pﬃﬃ
the simplest case is then J ¼ g, so that the diffusion
p
ﬃﬃﬃﬃﬃﬃﬃﬃ
pﬃﬃﬃﬃﬃﬃﬃﬃ
R
term is 12 dxdyNðxÞD2 ðx;yÞ gðxÞ gðyÞgij ðxÞgkl ðyÞ½δρ̂=
δπ ij ðxÞδπ kl ðyÞ þ   , but there are other more complicated
realizations which also recover the dynamical Einstein
equation as a limited case (by adding friction and additional
diffusion terms, for example). The additional Lindbladian
couplings corresponding to the Lindblad operator ĤðmÞ are
not needed in order to reproduce general relativity in the
classical limit or to preserve positivity, but instead appear to
be required by gauge invariance. The constraint equations for
this realization are derived in Ref. [146] by following the
procedure outlined in Ref. [156]. Alternatively, one can
include the lapse, shift, and their conjugate momenta as
canonical degrees of freedom and thus part of the Poisson
bracket in Eq. (125).
This realization has the clear advantage of being continuous, while the former realization has the advantage of
being linear in the Hamiltonian. In terms of the evolution of
the quantum system, for each classical space-time manifold, the quantum system undergoes both decoherence, as
well as unitary evolution generated by the Hamiltonian, and
quantum jumps which are accompanied by a backreaction
on the space-time. The diffusion terms imply that the
solution of Eqs. (123) and (125) [or alternatively, Eq. (125)]
should be a distribution which has a variance about the
solution to Einstein’s equations when we perform the trace
over the quantum system. This presents a testable deviation
from classical general relativity, potentially observable
when the other terms are small, such as at low acceleration
[167]. The absence of such terms is likely to falsify this
model. On the other hand, since diffusion of the metric can
result in stronger gravitational fields when we might
otherwise expect none to be present, it raises the possibility
that diffusion may explain galaxy rotation curves [169] and
galaxy formation without the need for dark matter.
In addition to the dynamical equation of motion,
Eq. (117) or Eq. (123), we need to impose the constraints
of general relativity. Let us recall how this is done
classically. There, the Hamiltonian and momentum constraint of Eq. (102) follows from demanding that the
Lagrangian be invariant under arbitrary time reparametrizations and spatial diffeomorphisms. This leads to the
primary constraints on their conjugate momenta, pN ¼ 0
and pN i ¼ 0. Preservation of the primary constraints is
implemented in the ADM formalism by requiring that
p˙N ¼ 0 and p˙N a ¼ 0 (the supermomentum and superHamiltonian constraints). These are just constraints on

PHYS. REV. X 13, 041040 (2023)

the classical phase space, and so we can constrain ρ to
lie on the surface in phase space where the constraints
are zero.
Were we to impose the constraint in an equivalent
manner here, it would amount to demanding that ĤADM
be invariant under the action of PN and PN a . This would
lead to a Hamiltonian constraint of the form
?

HðgrÞ þ 16πGĤðmÞ ≈ 0

ð126Þ

at every x which would be impossible to satisfy, since it
contains both a classical term HðgrÞ and a local quantum
operator ĤðmÞ. However, such a constraint is not needed;
rather, we should instead ask, what restrictions are required
such that the equations of motion satisfy the required
symmetry? In the classical case, we demand that physical
degrees of freedom do not depend on the choice of lapse N
and shift N a , i.e., that these are gauge choices. This
requirement necessarily leads to the constraints of general
relativity. Likewise here, we should not first demand that
the constraints be satisfied, but rather, require that the
equations of motion be invariant under the choice of lapse
and shift. This turns out to lead to modified constraints
which are not of the form (126). We discuss how the
constraints can be generated from gauge invariance of
the equations of motion in Ref. [156]. Invariance of the
equations of motion under spatial diffeomorphisms is
already guaranteed, as the evolution equation involves
only integrals over scalar densities.
In order to find a solution to the dynamical and constraint
equations, we need the equations to be compatible.
Attempts to quantize gravity have floundered on this point,
as the constraints are operators and typically do not
commute, so no simultaneous solution of the constraints
exist. This is the case in loop quantum gravity, although it is
hoped that one can find an operator ordering such that the
constraints close. Likewise, string theory is background
dependent, which presumably means that in the full theory,
gauge invariance is broken. While it is hoped that frameworks for string field theory could result in a backgroundindependent approach, it is not clear whether this can be
maintained. Here, we also require constraint compatibility,
but it takes on a different form. Because we have attempted
to implement gauge invariance on the level of the equations
of motion rather than as operator identities, the relevant
notion of constraint compatibility is not simply the
commutation of operators, but whether the evolution
operators and constraints and generators “commute” with
one another when applied to the state. In other words, we
require for example
La ðxÞLðyÞρ̂ðz; tÞ − LðyÞLa ðxÞρ̂ðz; tÞ ≈ 0;

ð127Þ

and similarly, we require that the “commutation relations”
for all other generators vanish on the constraint surface; the

041040-25

## PDF page 26

JONATHAN OPPENHEIM

PHYS. REV. X 13, 041040 (2023)

right-hand side must be a linear combination of generators
and constraint equations. This notion of constraint compatibility replaces the closure of the Dirac algebra in the
classical theory.
This program is initiated in Ref. [156] in the Heisenberg
representation to find gauge-invariant observables A. This
constraint structure, while involved, is far simpler than the
constraint structure of loop quantum gravity or canonical
quantization, and provides a model in which to understand
some of the conceptual challenges these theories face.
While the constraints are more complicated because they
are implemented on the level of equations of motion, the
classical nature of the gravitational field means they do not
suffer from operator ordering issues and are more tractable.
Nonetheless, it may be impossible to find a realization of
the theory and a symmetry principle, such that the set of
constraint equations close. In that case, one could still
impose the standard constraints of general relativity as
initial conditions, as is done in the ADM formulation, but
they may not be conserved in time. One could instead
impose the standard constraints as expectation values, but
again, it is possible these may also not be conserved in time.
This would likely mean the theory was not invariant under
diffeomorphisms of the (3 þ 1)-dimensional space-time,
but it would not render the theory inconsistent, since we
formulated the theory here, not as a 3 þ 1 theory of spacetime, but rather, as a Hamiltonian theory of the spatial
metric. The evolution of matter is governed by the
Hamiltonian and Lindblad operators, which are functionals
only of the 3-metric. To be consistent, the theory needs to
be invariant under spatial diffeomorphisms, which it
manifestly is. However, although it would be a consistent
theory, it would be unclear how to justify imposing the
constraint as a mere initial condition. So while the theory
may be consistent, it would require further motivation.
An alternative approach can be pursued now that
classical quantum path integral methods have recently
been developed [170]. Since the path integral is computed
in configuration space, this allows for the construction of
manifestly diffeomorphism-invariant theories. These
have since been proposed together with Weller-Davies
[142]. One, based on the trace of Einstein’s equations, is
different from Einstein’s general relativity, but does at
least demonstrate that diffeomorphism-invariant classical
quantum theories are possible in principle. A theory
which contains all components of the Einstein equations
is also proposed, but it is not yet known whether
dynamics which deviate from general relativity are
suitably suppressed.
VI. DISCUSSION
The general form of hybrid classical quantum dynamics
is presented here as Eq. (14), which includes discrete
evolution and a continuous form [71]. Based on this, we
exhibite a theory of classical general relativity coupled to

quantum field theory which is invariant under spatial
diffeomorphisms. The theory is consistent: The dynamics
is completely positive, norm preserving, and linear in the
density matrix. We specify the dynamics up to a choice of
the positive-semidefinite matrix W αβ
h ðzjz − Δ; x; yÞ. The
choice is constrained by gauge invariance, and thus must
satisfy further criteria, as discussed in Ref. [156]. Two
particular choices of W αβ
h ðzjz − Δ; x; yÞ, are the model of
Eq. (120) and that corresponding to Eq. (125). These are
further considered in Ref. [156] and Refs. [50,146],
respectively, along with the constraint equations which
correspond to them. In Ref. [71], it is shown that the first
realization leads to discrete jumps in phase space, while the
second realization follows from demanding that the dynamics be continuous in phase space. The first moment in their
Kramers-Moyal expansion corresponds to general relativity
in the ADM formulation, and thus both recover classical
general relativity as a limiting case. A proposal based on the
path integral is introduced in Ref. [142].
We require that the metric remains classical even when
backreacted upon by quantum fields, and this has two
important consequences. First, the interaction is necessarily
stochastic, which is important, since a principle motivation
behind the theory are attempts to resolve the black-hole
information problem. That there exists a fully quantum
theory of gravity has been an argument against theories
which have fundamental information loss, in the sense that
given any such dynamics one can always find a purification
of the state onto some environment, such that the full theory
is unitary. In this case, Coleman has shown that when we
trace out the environment, the dynamics is equivalent to a
unitary theory with unknown coupling constants [62]. This
renders the information loss trivial: In a universe with a
finite number of random coupling constants, an observer
has only to perform a sufficient number of experiments to
determine these coupling constants, after which time the
theory will behave arbitrarily close to a unitary one from
the point of view of this experienced experimentalist.
However, the argument in Ref. [62] need not apply here.
Any purification which keeps some degrees of freedom
classical would need to obey an unnatural condition,
namely, that it remain of the form
X
ρ̂AB ¼
jg; πiA ⊗ jg; πiB ⊗ jρ̂matter ðg; πÞiAB ð128Þ
with system A encoding the classical degrees of freedom
and system B being the purifying system [171]. For these
degrees of freedom to remain classical, one further needs to
impose the condition that one can measure only in the basis
where jg; πiA is diagonal. If one lifts this restriction on
measurements, or allows dynamics more general than the
one preserving the form of the state of Eq. (128), then it is
far from clear that the dynamics would still be completely
positive and trace preserving. The dynamics here needs
only to give positive probabilities on measurements which

041040-26

## PDF page 27

A POSTQUANTUM THEORY OF CLASSICAL GRAVITY?
commute with the basis representing the classical degrees
of freedom. It does not need to give positive probabilities
for all measurements. Thus, we cannot conclude that this
theory has consistent dynamics on the purified state. Or to
put it another way, it is unlikely to be the case that the
dynamics considered here can be viewed as unitary
quantum dynamics with a local environment which is
traced out. The fact that the quantum system couples to
a classical one, thus provides a potential loophole to the nogo theorem of Ref. [62] ruling out nontrivial information
destruction, while as argued in Sec. I, information destruction provides the loophole out of the no-go argument of
Feynman and Aharonov against quantum systems interacting with classical ones. The two no-go theorems annihilate
each other.
There may appear to be some tension between the claim
that the theory may evade the no-go argument of Coleman,
and the idea that the theory presented here could be an
effective theory which emerges as the classical limit of a
fully quantum theory. However, this is not necessarily in
contradiction. In Ref. [176], we consider fully quantum
descriptions, which effectively act like a classical quantum
description. The classical system corresponds to a quantum
system decohered into a family of coherent states, and for
some potentials, this description is valid for long times.
Since this description is fully quantum, Coleman’s argument would imply that it corresponds to a unitary theory on
an enlarged Hilbert space with unknown coupling constants, and that there exist measurements which would
allow an experimenter to determine these constants.
However, in the classical quantum description of this fully
quantum theory, we do not allow arbitrary measurements
on the “classical” system—only measurements of q and p
are allowed. Coleman’s argument allows the experimenter
to perform measurements in an arbitrary basis, and it
appears unlikely one could use fixed measurements to
determine the coupling constants.
The second consequence of having a quantum classical
interaction is that the measurement postulate of quantum
theory is no longer needed. One has fundamental
decoherence of the quantum field by the classical metric.
In this view, classicality is not an emergent or effective
property of large quantum systems, but rather, fundamental.
In the discrete theory discussed here, hαβ is diagonal and
unique for each Lindblad operator. As with the SternGerlach example, the accompanying jump in phase space
unambiguously determines which Lindblad operator was
applied to the quantum state. If we know the initial pure
state of the quantum system, then by monitoring the
classical system, we know which sequence of Lindblad
operators were applied to the quantum state and at what
times. As such, the quantum state conditioned on the
classical degrees of freedom remains pure. Likewise, in
the continuous case, we have since found that there is a very
natural class of theories in which the quantum state remains

PHYS. REV. X 13, 041040 (2023)

pure conditioned on the classical trajectory [29]. This is
ironic given the motivation of obtaining dynamics which
allowed for the destruction of information in black-hole
evaporation. The dynamics here, while stochastic, can leave
the quantum state pure. It is the classical degrees of
freedom which gain entropy. This suggests that in blackhole evaporation, the associated entropy is the entropy of
the classical space-time. Since the formalism introduced
here allows one to study the backreaction of matter fields
on the gravitational field, there is hope that we can better
understand black holes, as well as other systems where
gravity and quantum effects are important.
Let us next address a number of open questions and
challenges that the theory faces, starting with the objection
to theories of information destruction due to Banks, Peskin,
and Susskind (BPS) [60]. BPS argued that a local interaction which leads to decoherence will lead to anomolous
heating to such a degree that it will contradict observation.
Although the BPS argument was not made in the context of
classical quantum theories, it does apply to Lindbladian
evolution of the quantum state σ̂ with Lindblad operators
being local field operators, and our theory does contain such
terms. In particular, BPS considered an evolution equation
∂σ̂ðtÞ
¼ −i½ĤðmÞ ; σ̂ðtÞ
∂t

Z
0 αβ
0
þ dxdx D0 ðx − x Þ L̂α ðxÞσ̂ðtÞL̂†β ðx0 Þ

1 † 0
− fL̂β ðx ÞL̂α ðxÞ; σ̂ðtÞgþ
2

ð129Þ

0
and couplings Dαβ
0 ðx − x Þ. The Hamiltonian of the matter
ðmÞ
0
fields Ĥ will not be conserved, and when Dαβ
0 ðx − x Þ has
0
short range (decays rapidly with jx − x j) there may be
significant anomalous heating. In essence, local operators
L̂α ðxÞ do not commute with the Hamiltonian, and in the
0
limit where Dαβ
0 ðx − x Þ is a delta function, the average rate
of energy production contains terms which diverge. This is
easily seen in the Heisenberg representation, since when
0
0
Dαβ
0 ðx − x Þ is symmetric in x, x , and α, β,

dĤðmÞ 1
¼
2
dt

Z

dxdx0 D0 ðx−x0 Þ½L̂α ðxÞ;½Ĥ ðmÞ ; L̂†β ðx0 Þ: ð130Þ

If the L̂α ðxÞ contain only a finite number of derivatives of
local field operators, then the commutator gives terms
proportional to δðx − x0 Þ, or kth derivatives ∇k δðx − x0 Þ.
These terms will diverge if D0 ðϵÞ diverges as ϵ → 0. For
example, if D0 ðx − x0 Þ ∝ δðx − x0 Þ.
This anomalous heating should trouble us if it contradicts observation, but it need not trouble us on a fundamental level. If the dynamics is Lindbladian, there is no
reason to expect energy conservation; the dynamics is not

041040-27

## PDF page 28

JONATHAN OPPENHEIM

PHYS. REV. X 13, 041040 (2023)

unitary and so Noether’s theorem does not apply. The
generator of time translations is not the Hamiltonian but the
Lindbladian [177]. In fact, there is no way to canonically
define energy, since by choosing a different basis of
Lindblad operators, the Hamiltonian will change. In the
case of classical quantum systems, the notion of energy
becomes even harder to define, since the Hamiltonian is a
hybrid object. On top of this, in general relativity there is no
local definition of energy or conservation law for energy
integrated over an infinitesimal spatial surface [180]. From
a physical point of view, this is arguably the more relevant
quantity, and so the question of energy conservation is not a
matter of principle, but rather, consistency with experiment.
One must ensure that the vacuum is stable enough that it
does not contradict experimental observation.
The vacuum can be made stable by turning down the
Lindbladian coupling so that D0 ðϵÞ decreases as ϵ → 0.
Since dĤðmÞ =dt goes as D0 ðϵÞ, we can regularize it by
discretizing space-time, and scaling D0 ðϵÞ with ϵ. In the
pure-Lindbladian case, there is no reason not to take the
Lindbladian coupling to be arbitrarily small, in which case
the effect is weak in flat space and only strong when the
3-metric becomes singular, since
we expect
D0 ðx − x0 Þ to
pﬃﬃﬃﬃﬃﬃﬃﬃ
pﬃﬃﬃﬃﬃﬃﬃﬃﬃ
contain terms proportional to gðxÞ and gðx0 Þ. Seen in
this light, the problem raised by BPS is merely one of
having to introduce another scale.
A similar issue occurs in spontaneous collapse models
[67–69], but in and of itself, this does not present a
problem, since again, one can tune down the
Lindbladian coupling D0 ðϵÞ as small as one wishes.
Those who advocate for spontaneous collapse models
typically require D0 ðx − x0 Þ to be large enough to account
for the level of decoherence we see around us. This
requirement on D0 is not needed here for three reasons.
First, environmental decoherence is expected to account for
most of the decoherence we observe. Second, the collapse
of the wave function is a byproduct which occurs only
when sufficient correlations has build up between the
gravitational field and the quantum state together with
its correlated environment. And third, decreasing D0 ðϵÞ
requires more gravitational diffusion [50], which causes
additional decoherence once the gravitational field is
integrated out [30,92]. The heating effect of this secondary
decoherence is a source of concern, but appears to be
milder than in BPS [30,50], although whether this is within
experimental limits requires further investigation since at
short distances, we are operating in a regime where
relativistic effects become important.
The question of whether the couplings can be tuned
down as we decrease ϵ is related to the question of whether
the theory is regularizable [170]. In the case of a scalar field
with a single Lindblad operator ϕðxÞ, the Lindbladian
dynamics is both renormalizable and Lorentz invariant
[140,141], and we can choose the coupling constant to
generate as little anomalous heating as we wish, since we

do not require the amount of entropy production to be large.
Understanding whether the theory can be regularized,
remains an important open question for the program
presented here. The question is complicated by the fact
that relativistic corrections in the gravitational field become
important at short distances [168] and by the fact that some
aspects of the heating appear to be gauge artifacts [181].
Other strategies have been considered, but they may
make the theory less compelling. One may be able to make
the anomalous heating small by introducing a small
violation of locality as has been attempted in the case of
Lindbladians in the context of field theories [66], or as is
done in spontaneous collapse models where the coupling is
modified at a length scale at the order of the proton radius.
It is worth emphasizing that if one reduces heating by
0
allowing Dαβ
0 ðx − x Þ to have finite range, this does not
necessarily violate locality. If L̂α ðxÞ are local operators,
then it is possible for local observables to still evolve
0
locally even though Dαβ
0 ðx − x Þ. The price we pay if
0
0
Dαβ
0 ðx − x Þ does not fall off fast enough with jx − x j is
that correlations can be created over finite distances
[60,65]. While this seems to suggest some correlated
environment should be evoked, it does not lead to superluminal signaling or inconsistencies. It will however
naively violate Lorentz invariance, since one has spatial
correlations but no temporal ones. This could be rectified
0
by taking Dαβ
0 ðx − x Þ to not depend on the spatial distance
0
jx − x j, but rather the space-time distance. For example,
one could take it to be the Green’s function of the LaplaceBeltrami operator. This would then suggest a nonMarkovian evolution reminiscent of an effective theory
rather than a fundamental one. Another alternative is to
modify gravity at short distances. Since gravity is tested
only to within the milometer scale, such modifications have
often been considered, but would likely necessitate some
additional structure such as extra dimensions [182].
Whether such measures are required is unclear. In the
context of the theories considered here, the situation is
significantly different from the pure-Lindbladian evolution
considered by BPS. First, the action of the Lindblad
operators on the quantum field is accompanied by a backaction on the classical degrees of freedom, and in particular,
the gravitational degrees of freedom. While the argument of
BPS suggests there will be an increase in the expectation
value of the energy density of the matter Hamiltonian
density ĤðmÞ, this can be accompanied by a decrease in
the energy of the classical system due to this backreaction. In
this case, this is the kinetic energy density Gijkl π ij π kl of the
pure gravity part of the super-Hamiltonian, HðgrÞ . In the case
of a discrete realization of this theory, such as Eq. (120), the
action of the Lindblad operator is accompanied by a jump in
π ij ðxÞ. Likewise, the diffusion term of the continuous
realization, Eq. (125) acts on the kinetic term of HðgrÞ ðxÞ
in the Heisenberg representation producing an energy
density flux of Dijkl
2 ðx; xÞGijkl ðxÞ which can be negative

041040-28

## PDF page 29

A POSTQUANTUM THEORY OF CLASSICAL GRAVITY?
and state independent, and also needs to be regularized. For
example, consider
pﬃﬃ
gN ik jl
ijkl
0
lim D2 ðx; x Þ ¼ D2
ðg g þ gil gjk − 2βgij gkl Þ
2
x−x0 →l
ð131Þ
with D2 some constant which depends on the cutoff l, and
β < 1=3 to ensure Dijkl
2 is positive semidefinite. If we wish

PHYS. REV. X 13, 041040 (2023)

0
Dijkl
2 ðx; x Þ to include only the final term in Eq. (131)
proportional to gij gkl , then we can take D2 → D2 =β and
β → −∞.
Using the diffusion coefficient of Eq. (131), we can
compute the apparent flux of gravitational kinetic energy
density using the continuous realization of Eq. (125) in the
Heisenberg representation. Ignoring any boundary terms,
this gives

Z
dH ðgrÞ ½N; ⃗N
1
δ2
ðgrÞ
0Þ
⃗
⃗
⃗
¼ fH ½N; N; ĤADM ½N; Ng þ
dxdx0 Dijkl
ðx;
x
HðgrÞ ½N; N
2
dt
2
δπ ij ðxÞδπ kl ðx0 Þ
Z
pﬃﬃ 1
¼ fHðgrÞ ½N; ⃗N; ĤðmÞ ½N; ⃗Ng þ dxN 2 D2 g ðgik gjl þ gil gjk − 2βgij gkl ÞGijkl
2


Z
d
ðmÞ
ðgrÞ
2
⃗
⃗
¼ fH ½N; N; Ĥ ½N; Ng þ d − ð1 þ βÞD2 dxN 2 ;
2
where d is the number of spatial dimensions. We assume
that the lapse and shift N; ⃗N depend only on the metric and
not its conjugate momenta. The first term is just the change
in energy due to the backreaction of the matter Hamil⃗
tonian, and is compensated for by the action of H ðgrÞ ½N; N
ðmÞ
on Ĥ ½N; ⃗N which results in an equal and opposite
⃗ ĤðmÞ ½N; Ng
⃗
energy flux −fHðgrÞ ½N; N;
into the matter
degrees of freedom. It is the second term which is due
to the diffusion. Taking β < 1 results in an apparent
negative flux of gravitational kinetic energy. It can at least
partially compensate for the heating of the matter field
given in Eq. (130). The question is a subtle one; for
example, in the weak-field limit, what initially appears to
be constant anomalous energy production in the gravitational degrees of freedom turns out to be a gauge artifact
[181]. The dependence of Eq. (132) on the lapse suggests
this might be the case more generally.
Whether this backreaction is enough to restore equilibrium or slow the production of energy in the matter sector
of the theory is an open question. It may merely be that the
total Hamiltonian is conserved on average, with heating
occurring in the matter degrees of freedom, and a negative
flux of kinetic energy occurring in the gravitational degrees
of freedom. To what extent this would be observable has
since been partially taken up in Ref. [50], where it is shown
that the decoherence (and heating) in the matter degrees of
freedom can be made small, but only at the expense of a
large diffusion in the gravitational degrees of freedom.
However, because gravity is so weak, the effect appears to
be within current experimental bounds, although they do
0
constrain Dijkl
2 ðx; x Þ. The question then becomes whether
the anomalous heating and diffusion are within experimental bounds, while at the same time, respecting various local
symmetry properties such as diffeomorphism invariance or
some weaker version.

ð132Þ

Related to this is the question of whether the
Hamiltonian and momentum constraint is preserved in
time. In the deterministic theory, this says that the total
energy and momentum density is everywhere zero. These
constraints are however modified in the theory considered
here. Since conservation of the constraints in general
relativity enforces diffeomorphism invariance, the issue
of diffusion of gravitational kinetic energy and anomalous
heating is linked with whether diffeomorphism invariance
or a related local symmetry will be respected. Whether the
theory satisfies some local symmetry then becomes a
question of satisfying some potentially modified constraint
equations, and whether one can satisfy them all at the same
time. This turns on the question of the compatibility of the
constraint equations, i.e., whether the algebroid of constraints [183] closes. Of course in the CQ theory, the
constraint is not of the form Eq. (126), and the full
dynamics are subtle. A fuller understanding of the algebroid of constraint equations thus remains an open issue,
with some initial progress reported in Ref. [156] where
these issues are further explored (cf. Ref. [142]).
There is some reason to believe 3 þ 1 diffeomorphism
invariance or something related to it can be respected, given
the diffeomorphism-invariant realization of Ref. [142]
based on the trace of Einstein’s equations, and using the
path integral formulation of CQ dynamics [170]. In
Ref. [142], we also present a diffeomorphism-invariant
theory which gives all of Einstein’s equations, although we
have not proven that the dynamics preserves positivity of
initial states. The challenge then is to see if the realization is
consistent with experimental constraints such as those on
anomalous heating and gravitational diffusion, and is
ideally also renormalizable in the matter degrees of freedom. While realizations exist which are renormalizable,
and realizations exist which have small amounts of

041040-29

## PDF page 30

JONATHAN OPPENHEIM

PHYS. REV. X 13, 041040 (2023)

anomalous heating, the question of whether a realization
exists which satisfies all these requirements remains open.
The classical quantum theory has a number of experimental signatures, some of which have since been quantified in Ref. [50]. It predicts a form of gravitational
decoherence, which already a number of experiments are
looking for [184–186]. It predicts stochastic, finite-sized
jumps, or continuous diffusion of the gravitational field
which might be detectable in the lab with current technology. The theory also predicts diffusion which might be
observable in astrophysical systems and in cosmology. The
theory is highly constrained, especially if τ the parameter in
Eq. (17) is taken to be of order ℏ, since increasing the
coherence time results in larger jumps and more diffusion.
Finally, the locally correlated realizations considered here
predict a null result to recently proposed experiments to test
the quantum nature of gravity [187–190].
Here, space-time is treated as fundamentally classical,
but one could instead view this theory as a candidate for an
effective theory which results from taking the classical limit
of the gravitational degrees of freedom of a fully quantum
theory of gravity. There are a number of ways of taking this
partial classical limit. The extent and the conditions under
which this gives the equations of motion presented here is
taken up in Ref. [176]. We find that care should be taken,
since an effective theory might violate our assumptions of
complete positivity at short timescales or of being time
local. Nonetheless we find that there is a regime, and a
choice of parameters, such that Eq. (14) describes the
consistent evolution of interacting quantum systems in the
limit where a subsystem behaves classically.
Whether the theory presented here is taken to be
fundamental or not, it provides a consistent way to explore
the regime where space-time is classical in a manner which
does not suffer from the pathologies of the semiclassical
equations. This has been lacking in our investigation into
how space-time reacts to quantum systems. This gives hope
that the ability to consistently study backreaction effects
finds application on large-distance scales, in cosmology,
and in black-hole evaporation.
ACKNOWLEDGMENTS
I would like to thank Dorit Aharonov, Robert Alicki,
Sougato Bose, Lajos Diosi, Patrick Hayden, Michal
Horodecki, Veronika Hubeny, David Jennings, Don
Marolf, Lluis Masanes, Sandu Popescu, John Preskill,
Benni Reznik, Lenny Susskind, Bill Unruh, and groups
17 and 18 of PHAS3441 (2018) for interesting discussions.
I would especially like to thank Joan Camps, Barbara Šoda,
Carlo Sparaciara, and Zach Weller-Davies for the helpful
discussion clarifying some of the points raised here. I am
grateful to David Poulin for introducing me to Eq. (6) and
his comments on an early version of the ADM realization of
the theory during the KITP QINFO17 program, as well as
Lajos Diosi and Antoine Tilloy for drawing my attention to

their work. I would also like to thank Lydia Marie
Williamson for correcting a number of typos from an
earlier version of this draft. I am very grateful to the
anonymous referees of PRX for their comments and
attention to detail, which have helped improve this work.
This research was supported by an EPSRC Established
Career Fellowship, a Royal Society Wolfson Merit grant,
the National Science Foundation under Grant No. NSF
PHY11-25915, and by the Simons Foundation It from
Qubit Network.
APPENDIX A: CONDITIONS FOR COMPLETE
POSITIVITY OF A CQ MAP
Here we extend a theorem due to Kossakowski [194] for
a cq map EðtÞ to be completely positive on a separable
Hilbert space; see also Ref. [50] for a more complete proof
using indicator functions. Let us consider all complete sets
of projectors Pr ðzÞ on the doubled Hilbert space HS ⊗ HS
and classical degrees of freedom z.
Theorem 1. L is a generator of continuous-time,
completelyRpositive, Markovian evolution of ρ̂ðz; tÞ which
preserves dztrρ̂ðz; tÞ if and only if for all sets of
orthogonal projectors fPr ðzÞg:
trPs ðzÞLzjz0 ⊗ 1(Pr ðz0 Þ) ≥ 0;

∀ r ≠ s; z; z0 ;

ðA1Þ

trPs ðzÞLzjz0 ⊗ 1(Ps ðz0 Þ) ≥ 0;

∀ s; z ≠ z0 ;

ðA2Þ

∀ r; z0 ;

ðA3Þ

Z

trLzjz0 ⊗ 1(Pr ðz0 Þ) ¼ 0;

z

R
where Lρ̂ðz; tÞ ¼ dz0 Lzjz0 ρ̂ðz0 ; tÞ.
As a consequence of the above, we automatically get
Z
tr dz0 δðz − z0 ÞPs ðzÞLzjz0 ⊗ 1(Ps ðz0 Þ) ≤ 0 ∀ s;z
ðA4Þ
since the probability conservation condition, Eq. (A3)
ensures that outward flux from any Ps ðzÞ contributes
negatively to the probability rate. The proof of Theorem
1 follows from writing
E zjz0 ðδtÞ − 1δðz − z0 Þ
;
ðA5Þ
δt→0
δt
R
where EðtÞρ̂ðz; tÞ ¼ dz0 E zjz0 ðtÞρ̂ðz0 ; tÞ, and using the fact
that the map E zjz0 is completely positive, probabilityconserving map if and only if
Lzjz0 ≔ lim

trPs ðzÞE zjz0 ⊗ 1(Pr ðz0 Þ) ≥ 0

∀ fPs ðzÞg; fPr ðz0 Þg; z; z0
ðA6Þ

and

041040-30

## PDF page 31

A POSTQUANTUM THEORY OF CLASSICAL GRAVITY?
X
trE zjz0 ⊗ 1(Pr ðz0 Þ) ¼ 1

∀ fPr ðzÞg; r; z0 :

ðA7Þ

z

It follows that E zjz0 is trace nonincreasing

E zjz0 ⊗ 1(Pr ðz0 Þ) ≤ 1:

ðA8Þ

Equation (A2) is an additional constraint on the quantum
system not found in Ref. [194], although if one considers
the projector to also be on the classical degree of freedom,
then it becomes subsumed by Eq. (A1). From Kraus’s
theorem, we know that this implies that Λαβ ðzjz0 ; tÞ in
Eq. (34) needs to be positive semidefinite in α, β for all z, z0 .

PHYS. REV. X 13, 041040 (2023)

APPENDIX B: HEISENBERG REPRESENTATION
Equations (14) and (17) tell us how the classical quantum
state evolves. As with both quantum and classical mechanics, there is an alternative “Heisenberg” picture in which the
state does not evolve but the operators do. One can easily
derive the time evolution of operators in this representation,
since it follows from demanding that for all ρ̂ðz; tÞ,
d
dt

Z

d
dztrÂS ðz; tÞρ̂S ðzÞ ¼
dt

Z
dztrÂH ðz; tÞρ̂H ðzÞ;

ðB1Þ

where the subscript S indicates the Schrödinger representation, and H the Heisenberg representation. Using this and
Eq. (14) for the evolution of ρ̂S ðzÞ leads to the Heisenberg
evolution equation for the operator Âðz; tÞ over phase space

dÂH ðz; tÞ ∂ÂH ðz; tÞ
¼
þ i½ĤðzÞ; ÂH ðz; tÞ
dt
∂t
Z

1
dΔW αβ ðz þ ΔjzÞL̂†β ÂH ðz þ Δ; tÞL̂α − W αβ ðzÞfL̂†β L̂α ; ÂH ðz; tÞgþ
2


∂ÂH ðz; tÞ
1
†
†
αβ
þ i½ĤðzÞ; ÂH ðz; tÞ þ W ðzÞ L̂β ÂH ðz; tÞL̂α − fÂH ðz; tÞ; L̂β ðxÞL̂α gþ
¼
∂t
2
þ

− L̂†β fhαβ ; ÂH ðz; tÞgL̂α  þ    ;

ðB2Þ

where we use cyclicity of operators under the trace and integration by parts. We include the purely classical term in W 00 , but
for deterministic evolution, it would be −fHðzÞ; ÂH ðz; tÞg. For a field theory, and in general relativity, we are usually
interested in the evolution of diffeomorphism-invariant operators such as
Z
pﬃﬃ
ðB3Þ
ÂH ðzÞ ¼ dx gÂðz; xÞ;
where Aðz; xÞ is a local scalar operator. In such a case, we have
dÂH ðz; tÞ ∂ÂH ðz; tÞ
¼
þ i½ĤðzÞ; ÂH ðz; tÞ
dt
∂t


Z
1
†
†
αβ
þ dx dΔW ðz þ Δjz; x; yÞL̂β ðyÞÂH ðz þ Δ; tÞL̂α ðxÞ − Wðz; x; yÞfL̂β ðyÞL̂α ðxÞ; ÂH ðz; tÞgþ
2


Z
∂ÂH ðz; tÞ
1 †
†
αβ
þ i½ĤðzÞ; ÂH ðz; tÞ þ W ðz; x; yÞ L̂β ðyÞÂH ðz; tÞL̂α ðxÞ − fL̂β ðyÞL̂α ðxÞ; ÂH ðz; tÞgþ dx
¼
∂t
2
Z
− dxL̂†β ðxÞfhαβ ðz; xÞ; ÂH ðz; tÞgL̂α ðxÞ þ    :

ðB4Þ

Note that care must be taken here. The Heisenberg representation allows one to compute the change of the expectation value
of an observable Â with time. However, if the evolution is nonunitary, then it is not necessarily the case that
hÂn ðtÞi ¼ hÂðtÞin . For example, if there is dispersion, than typically hp̂2 i − hp̂i2 will increase with time. Thus, knowing
ÂðtÞ does not necessarily allow one to deduce the expectation value other moments of the operator.

041040-31

## PDF page 32

JONATHAN OPPENHEIM

PHYS. REV. X 13, 041040 (2023)

[1] Gabriele Veneziano, Construction of a crossing-simmetric,
Regge-behaved amplitude for linearly rising trajectories,
Nuovo Cimento A 57, 190 (1968).
[2] Amitabha Sen, Gravity as a spin system, Phys. Lett. 119B,
89 (1982).
[3] Abhay Ashtekar, New variables for classical and quantum
gravity, Phys. Rev. Lett. 57, 2244 (1986).
[4] Carlo Rovelli and Lee Smolin, Knot theory and quantum
gravity, Phys. Rev. Lett. 61, 1155 (1988).
[5] Edward Witten, On background-independent open-string
field theory, Phys. Rev. D 46, 5467 (1992).
[6] Lucien Hardy, Probability theories with dynamic causal
structure: A new framework for quantum gravity, arXiv:
gr-qc/0509120.
[7] Ognyan Oreshkov, Fabio Costa, and Časlav Brukner,
Quantum correlations with no causal order, Nat. Commun.
3, 1 (2012).
[8] Lee Smolin, The thermodynamics of gravitational radiation, Gen. Relativ. Gravit. 16, 205 (1984).
[9] Stephen W. Hawking and Don N. Page, Thermodynamics
of black holes in Anti–de Sitter space, Commun. Math.
Phys. 87, 577 (1983).
[10] Petar Simidzija, Achim Kempf, and Eduardo MartinMartinez, Gravitational wave emission from the CMB
and other thermal fields, Phys. Lett. B 816, 136208 (2021).
[11] Neils Bohr and Leon Rosenfeld, On the question of the
measurability of electromagnetic field quantities, in Quantum Theory and Measurement, edited by John A. Wheeler
and Wojciech H. Zurek (Princeton University Press,
Princeton, NJ, 1933, 1983), pp. 479–522.
[12] Cécile M. DeWitt and Dean Rickles, The Role of Gravitation in Physics: Report from the 1957 Chapel Hill
Conference (Max-Planck-Gesellschaft zur Förderung der
Wissenschaften, Berlin, 2011), Vol. 5, pp. 247–260,
https://edition-open-sources.org/sources/5/.
[13] Bryce S. DeWitt, Definition of commutators via the
uncertainty principle, J. Math. Phys. (N.Y.) 3, 619 (1962).
[14] Kenneth Eppley and Eric Hannah, The necessity of quantizing the gravitational field, Found. Phys. 7, 51 (1977).
[15] J. Caro and L. L. Salcedo, Impediments to mixing classical
and quantum dynamics, Phys. Rev. A 60, 842 (1999).
[16] L. L. Salcedo, Absence of classical and quantum mixing,
Phys. Rev. A 54, 3657 (1996).
[17] Debendranath Sahoo, Mixing quantum and classical mechanics and uniqueness of Planck’s constant, J. Phys. A
37, 997 (2004).
[18] Daniel R. Terno, Inconsistency of quantum-classical dynamics, and what it implies, Found. Phys. 36, 102 (2006).
[19] L. L. Salcedo, Statistical consistency of quantum-classical
hybrids, Phys. Rev. A 85, 022127 (2012).
[20] Carlos Barceló, Raúl Carballo-Rubio, Luis J. Garay, and
Ricardo Gómez-Escalante, Hybrid classical-quantum
formulations ask for hybrid notions, Phys. Rev. A 86,
042120 (2012).
[21] Chiara Marletto and Vlatko Vedral, Why we need to
quantise everything, including gravity, npj Quantum Inf.
3, 29 (2017).
[22] For a discussion of postquantum theories in the context of
gravity, see, for example, Ref. [23], which considers

modifications of the state space of quantum theory, while
here, we consider modifications of the dynamics and
dropping the measurement postulate of quantum theory.
[23] Markus P. Müller, Jonathan Oppenheim, and Oscar C. O.
Dahlsten, The black hole information problem beyond
quantum theory, J. High Energy Phys. 09 (2012) 116.
[24] Jonathan Oppenheim, Is it time to rethink quantum
gravity?, Int. J. Mod. Phys. D (2023), 10.1142/
S0218271823420245.
[25] Iwao Sato, An attempt to unite the quantum theory of wave
field with the theory of general relativity, Sci. Rep. Tohoku
Univ., 1st Ser., Phys. Chem. Astron. 33, 30 (1950).
[26] Christian Møller et al., The energy-momentum complex in
general relativity and related problems, Les théories
relativistes de la gravitation 91, 2 (1962).
[27] Leon Rosenfeld, On quantization of fields, Nucl. Phys. 40,
353 (1963).
[28] Don N. Page and C. D. Geilker, Indirect evidence for
quantum gravity, Phys. Rev. Lett. 47, 979 (1981).
[29] Isaac Layton, Jonathan Oppenheim, and Zachary WellerDavies, A healthier semi-classical dynamics, arXiv:
2208.11722.
[30] Jonathan Oppenheim, Barbara Soda, Carlo Sparaciari, and
Zachary Weller-Davies, A coherence limit on superpositions constrained by classical gravity (to be published).
[31] Bryce DeWitt, New directions for research in the theory of
gravitation, 1953.
[32] Michael J. Duff, Inconsistency of quantum field theory in
curved spacetime, in Proceedings of 2nd Oxford Symposium on Quantum Gravity (Clarendon Press, Oxford,
1980), Vol. 2, pp. 81–105, https://cds.cern.ch/record/
99451?ln=en.
[33] W. G. Unruh, Steps towards a quantum theory of gravity,
in Quantum Theory of Gravity: Essays in honor of the 60th
birthday of Bryce S. DeWitt, edited by S. M. Christensen
(Adam Hilger Ltd., 1984).
[34] Steve Carlip, Is quantum gravity necessary?, Classical
Quantum Gravity 25, 154010 (2008).
[35] R. P. Feynman, Feynman Lectures on Gravitation, edited
by F. B. Morinigo, W. G. Wagner, and B. Hatfield (1996),
pp. 10–12.
[36] Yakir Aharonov and Daniel Rohrlich, Quantum Paradoxes: Quantum Theory for the Perplexed (Wiley-VCH,
New York, 2003), pp. 212–213.
[37] Andrea Mari, Giacomo De Palma, and Vittorio
Giovannetti, Experiments testing macroscopic quantum
superpositions must be slow, Sci. Rep. 6, 22777 (2016).
[38] Gordon Baym and Tomoki Ozawa, Two-slit diffraction
with highly charged particles: Niels Bohr’s consistency
argument that the electromagnetic field must be quantized,
Proc. Natl. Acad. Sci. U.S.A. 106, 3035 (2009).
[39] Alessio Belenchia, Robert M. Wald, Flaminia Giacomini,
Esteban Castro-Ruiz, Časlav Brukner, and Markus
Aspelmeyer, Quantum superposition of massive objects
and the quantization of gravity, Phys. Rev. D 98, 126009
(2018).
[40] The argument in Ref. [14] additionally contains a claim
concerning superluminal signaling which is addressed in
Refs. [41,42].

041040-32

## PDF page 33

A POSTQUANTUM THEORY OF CLASSICAL GRAVITY?
[41] Mark Albers, Claus Kiefer, and Marcel Reginatto, Measurement analysis and quantum gravity, Phys. Rev. D 78,
064051 (2008).
[42] Adrian Kent, Simple refutation of the Eppley-Hannah
argument, arXiv:1807.08708.
[43] Although there is some similarity in language, the theory
introduced here is not related to the theory which goes by
the name of stochastic gravity [44]. There, noise is added
on top of the semiclassical Einstein equations, and one can
restrict oneself to the regime in which the nonlinearity
reviewed in Fig. 1 is small.
[44] Bei Lok Hu and Enric Verdaguer, Stochastic gravity: Theory
and applications, Living Rev. Relativity 11, 3 (2008).
[45] A similar refutation was independently reached by
David Poulin (private communication) and is implicit in
Refs. [46,47].
[46] Ph. Blanchard and Arkadiusz Jadczyk, Event-enhanced
quantum theory and piecewise deterministic dynamics,
Ann. Phys. (Berlin) 507, 583 (1995).
[47] Lajos Diosi, Quantum dynamics with two Planck constants
and the semiclassical limit, arXiv:quant-ph/9503023.
[48] James Mattingly, Why Eppley and Hannah’s thought
experiment fails, Phys. Rev. D 73, 064025 (2006).
[49] That classical-quantum dynamics requires stochasticity,
has since been proven rigorously in Ref. [50] under the
assumptions that the dynamics is Markovian and is a
completely positive and trace-preserving map.
[50] Jonathan Oppenheim, Carlo Sparaciari, Barbara Šoda,
and Zachary Weller-Davies, Gravitationally induced
decoherence vs space-time diffusion: Testing the quantum
nature of gravity, arXiv:2203.01982.
[51] S. W. Hawking, Breakdown of predictability in gravitational collapse, Phys. Rev. D 14, 2460 (1976).
[52] S. W. Hawking, The unpredictability of quantum gravity,
Commun. Math. Phys. 87, 395 (1982).
[53] , For background reading, we refer the reader to the
review of John Preskill, Do black holes destroy information?, arXiv:hep-th/9209058.
[54] Ahmed Almheiri, Donald Marolf, Joseph Polchinski, and
James Sully, Black holes: Complementarity or firewalls?,
J. High Energy Phys. 02 (2013) 62.
[55] Samuel L. Braunstein, Entangled black holes as ciphers of
hidden information, arXiv:0907.1190v1.
[56] For a strong case for nonunitarity, see, for example,
Refs. [57,58].
[57] Bill Unruh, Black holes: Complementarity, fuzz, or fire?
(2013).
[58] William G. Unruh and Robert M. Wald, Information loss,
Rep. Prog. Phys. 80, 092002 (2017).
[59] John Ellis, John S. Hagelin, Dimitri V. Nanopoulos, and M.
Srednicki, Search for violations of quantum mechanics,
Nucl. Phys. B241, 381 (1984).
[60] T. Banks, M. E. Peskin, and L. Susskind, Difficulties for
the evolution of pure states into mixed states, Nucl. Phys.
B244, 125 (1984).
[61] David J. Gross, Is quantum gravity unpredictable?, Nucl.
Phys. B236, 349 (1984).
[62] Sidney Coleman, Black holes as red herrings: Topological
fluctuations and the loss of quantum coherence, Nucl.
Phys. B307, 867 (1988).

PHYS. REV. X 13, 041040 (2023)
[63] William G. Unruh and Robert M. Wald, Evolution laws
taking pure states to mixed states in quantum field theory,
Phys. Rev. D 52, 2176 (1995).
[64] Evolution can be local, in the sense that two local
operators Aðx; tÞ and Bðx0 ; t0 Þ commute at spacelike
separated points ½Aðx;tÞ;Bðx0 ;t0 Þ ¼ 0 whenever ðx − x0 Þ2 −
ðt − t0 Þ2 ≥ 0, but still violate cluster separability, meaning
that
ðd=dtÞðAðx; tÞBðx0 ; tÞÞ ≠ ½dAðx; tÞ=dtBðx0 ; tÞ þ
Aðx; tÞ½dBðx0 ; tÞ=dt, and so correlations get destroyed
or are created over spacelike distances.
[65] J. Oppenheim and B. Reznik, Fundamental destruction of
information and conservation laws, arXiv:0902.2361.
[66] David Poulin and John Preskill, Information loss in
quantum field theories, in Fronteiers of Quantum Information, KITP Santa Barbara, 2017, https://online.kitp.ucsb
.edu/online/qinfo_c17/ and https://online.kitp.ucsb.edu/
online/qinfo_c17/poulin/.
[67] L. E. Ballentine, Failure of some theories of state reduction, Phys. Rev. A 43, 9 (1991).
[68] Michael R. Gallis and Gordon N. Fleming, Comparison of
quantum open-system models with localization, Phys. Rev.
A 43, 5778 (1991).
[69] Abner Shimony, Desiderata for a modified quantum
dynamics, in Proceedings of the Biennial Meeting of the
Philosophy of Science Association (Cambridge University
Press, New York, 1990), Vol. 1990, pp. 49–59.
[70] Sandro Donadi, Kristian Piscicchia, Catalina Curceanu,
Lajos Diósi, Matthias Laubenstein, and Angelo Bassi,
Underground test of gravity-related wave function collapse, Nat. Phys. 17, 74 (2021).
[71] Jonathan Oppenheim, Carlo Sparaciari, Barbara Šoda, and
Zachary Weller-Davies, The two classes of hybrid
classical-quantum dynamics, arXiv:2203.01332.
[72] Wayne Boucher and Jennie Traschen, Semiclassical
physics and quantum fluctuations, Phys. Rev. D 37,
3522 (1988).
[73] I. V. Aleksandrov, The statistical dynamics of a system
consisting of a classical and a quantum subsystem,
Z. Naturforsch. 36A, 902 (1981).
[74] Viktor Ivanovych Gerasimenko, Dynamical equations
of quantum-classical systems, Theor. Math. Phys. 50, 49
(1982).
[75] Lajos Diósi, Nicolas Gisin, and Walter T. Strunz, Quantum
approach to coupling classical and quantum dynamics,
Phys. Rev. A 61, 022108 (2000).
[76] Arlen Anderson, Quantum backreaction on “classical”
variables, Phys. Rev. Lett. 74, 621 (1995).
[77] Raymond Kapral and Giovanni Ciccotti, Mixed quantumclassical dynamics, J. Chem. Phys. 110, 8919 (1999).
[78] Raymond Kapral, Progress in the theory of mixed
quantum-classical dynamics, Annu. Rev. Phys. Chem.
57, 129 (2006).
[79] Oleg V. Prezhdo and Vladimir V. Kisil, Mixing quantum
and classical mechanics, Phys. Rev. A 56, 162
(1997).
[80] Lajos Diosi, A universal master equation for the gravitational violation of quantum mechanics, Phys. Lett. A 120,
377 (1987).
[81] Roger Penrose, On gravity's role in quantum state reduction, Gen. Relativ. Gravit. 28, 581 (1996).

041040-33

## PDF page 34

JONATHAN OPPENHEIM

PHYS. REV. X 13, 041040 (2023)

[82] Lev P. Pitaevskii, Vortex lines in an imperfect Bose gas,
Sov. Phys. JETP 13, 451 (1961), http://jetp.ras.ru/cgi-bin/
dn/e_013_02_0451.pdf.
[83] Eugene P. Gross, Structure of a quantized vortex in boson
systems, Nuovo Cimento 20, 454 (1961).
[84] Nicolas Gisin, Stochastic quantum dynamics and relativity,
Helv. Phys. Acta 62, 363 (1989), https://www.e-periodica
.ch/cntmng?pid=hpa-001:1989:62::1121.
[85] Nicolas Gisin, Weinberg’s non-linear quantum mechanics
and supraluminal communications, Phys. Lett. A 143, 1
(1990).
[86] Joseph Polchinski, Weinberg’s nonlinear quantum mechanics and the Einstein-Podolsky-Rosen paradox, Phys.
Rev. Lett. 66, 397 (1991).
[87] If someone prepares a system in one of two states σ̂ 0 or σ̂ 1
depending on the value of a coin toss (j0ih0j with
probability p, j1ih1j with probability 1 − p), then the
evolution L of the system must satisfy pj0ih0j ⊗
Lσ̂ 0 þ ð1 − pÞj1ih1j ⊗ Lσ̂ 1 ¼ L(pσ̂ 0 þ ð1 − pÞσ̂ 1 ), otherwise the system evolves differently depending on
whether we are aware of the value of the coin toss. A
violation of linearity further implies that when the system
is in state σ̂ 0 , it evolves differently depending on what state
the system would have been prepared in, had the coin been
j1ih1j instead of j0ih0j. This motivates our restriction to
linear theories.
[88] J. M. Jauch, The problem of measurement in quantum
mechanics, Helv. Phys. Acta 37, 293 (1964), https://access
.archive-ouverte.unige.ch/access/metadata/52b454c9-a77e4a3c-ac74- 59d2b21e7570/download.
[89] Lajos Diósi and Jonathan J. Halliwell, Coupling classical
and quantum variables using continuous quantum measurement theory, Phys. Rev. Lett. 81, 2846 (1998).
[90] Asher Peres and Daniel R. Terno, Hybrid classicalquantum dynamics, Phys. Rev. A 63, 022101 (2001).
[91] D. Kafri, J. M. Taylor, and G. J. Milburn, A classical
channel model for gravitational decoherence, New J.
Phys. 16, 065020 (2014).
[92] Antoine Tilloy and Lajos Diósi, Sourcing semiclassical
gravity from spontaneously localized quantum matter,
Phys. Rev. D 93, 024026 (2016).
[93] Antoine Tilloy and Lajos Diósi, Principle of least
decoherence for Newtonian semiclassical gravity, Phys.
Rev. D 96, 104045 (2017).
[94] Fay Dowker and Yousef Ghazi-Tabatabai, Dynamical
wavefunction collapse models in quantum measure theory,
J. Phys. A 41, 205306 (2008).
[95] Philip Pearle, Combining stochastic dynamical state-vector
reduction with spontaneous localization, Phys. Rev. A 39,
2277 (1989).
[96] G. C. Ghirardi, A. Rimini, and T. Weber, A model for a
unified quantum description of macroscopic and microscopic systems, in Quantum Probability and Applications,
edited by L. Accardi et al. (Springer, Berlin, 1985).
[97] G. C. Ghirardi, A. Rimini, and T. Weber, Unified dynamics
for microscopic and macroscopic systems, Phys. Rev. D
34, 470 (1986).
[98] N. Gisin and I. C. Percival, The quantum-state diffusion
model applied to open systems, J. Phys. A 25, 5677
(1992).

[99] Stephen L. Adler and Todd A. Brun, Generalized stochastic Schrödinger equations for state vector collapse,
J. Phys. A 34, 4797 (2001).
[100] Giancarlo Ghirardi and Angelo Bassi, Collapse theories, in
The Stanford Encyclopedia of Philosophy, Summer 2020
ed., edited by Edward N. Zalta (Stanford University,
Stanford, 2020).
[101] Frederick Karolyhazy, Gravitation and quantum mechanics of macroscopic objects, Nuovo Cimento A 42, 390
(1966).
[102] Lajos Diósi, Models for universal reduction of macroscopic
quantum fluctuations, Phys. Rev. A 40, 1165 (1989).
[103] Roger Penrose, On gravity’s role in quantum state reduction, Gen. Relativ. Gravit. 28, 581 (1996).
[104] The original motivation for gravitational decoherence is
based on nonlinear interactions, which is not present in the
linear theory considered here. Penrose’s motivation was
that one branch in a superposition would cause the timelike
Killing vectors in another branch to be uncertain, while in a
linear theory, different branches evolve independently.
Diosi originally postulated gravitational decoherence via
the nonlinear Schrödinger-Newton equation, while more
recent approaches are based on a linear hybrid theory
[92,93] as we also consider here.
[105] Michael J. W. Hall and Marcel Reginatto, Interacting
classical and quantum ensembles, Phys. Rev. A 72,
062109 (2005).
[106] Jonathan Oppenheim, Carlo Sparaciari, Barbara Šoda,
and Zachery Weller-Davies, Objective trajectories in
hybrid classical-quantum dynamics, Quantum 7, 891
(2023).
[107] Philippe Blanchard and Arkadiusz Jadczyk, On the interaction between classical and quantum systems, Phys. Lett.
A 175, 157 (1993).
[108] V. Gorini, A. Kossakowski, and E. C. G. Sudarshan,
Completely positive dynamical semigroups of N-level
systems, J. Math. Phys. (N.Y.) 17, 821 (1976).
[109] G. Lindblad, On the generators of quantum dynamical
semigroups, Commun. Math. Phys. 48, 119 (1976).
[110] David Poulin (private communication; result announced in
Ref. [70]).
[111] Lajos Diósi, Hybrid quantum-classical master equations,
Phys. Scr. 2014, 014004 (2014).
[112] Robert Alicki and Stanisław Kryszewski, Completely
positive Bloch-Boltzmann equations, Phys. Rev. A 68,
013809 (2003).
[113] Lajos Diósi, The gravity-related decoherence master
equation from hybrid dynamics, J. Phys. Conf. Ser. 306,
012006 (2011).
[114] Dynamics is time local if it can be written as
˙ ¼ KðtÞσ̂ðtÞ rather than in convoluted form ˙σ̂ðtÞ ¼
Rσ̂ðtÞ
t
0 dsKðt; sÞσ̂ðsÞ.
[115] Hendrik Anthony Kramers, Brownian motion in a field of
force and the diffusion model of chemical reactions,
Physica (Utrecht) 7, 284 (1940).
[116] J. E. Moyal, Stochastic processes and statistical physics,
J. R. Stat. Soc. Ser. B 11, 150 (1949).
[117] Daniela Frauchiger and Renato Renner, Quantum
theory cannot consistently describe the use of itself,
Nat. Commun. 9, 3711 (2018).

041040-34

## PDF page 35

A POSTQUANTUM THEORY OF CLASSICAL GRAVITY?
[118] Richard Arnowitt, Stanley Deser, and Charles W. Misner,
Republication of: The dynamics of general relativity, Gen.
Relativ. Gravit. 40, 1997 (2008).
[119] Jonathan Oppenheim, A post-quantum theory of classical
gravity, arXiv:1811.03116.
[120] As Šoda noted, one can generalize this formalism to the
case where the connection between the Hilbert spaces at
points z is nontrivial.
[121] K. Kraus, Complementary observables and uncertainty
relations, Phys. Rev. D 35, 3070 (1987).
[122] Michael M. Wolf and J. Ignacio Cirac, Dividing quantum
channels, Commun. Math. Phys. 279, 147 (2008).
[123] To the best of our knowledge, this argument was first made
by Bóna and appears as a private communication in
Ref. [124] and is also described, along with a counterexample, independently and around the same time in
Ref. [125]. We first learned about it in discussion with
Patrick Hayden and Jonathan Sorce.
[124] Vladimir Buzek, Reconstruction of Liouvillian superoperators, Phys. Rev. A 58, 1723 (1998).
[125] Heinz-Peter Breuer, Bernd Kappler, and Francesco
Petruccione, Stochastic wave-function method for nonMarkovian quantum master equations, Phys. Rev. A 59,
1633 (1999).
[126] C. W. Gardiner, Handbook of Stochastic Methods for
Physics, Chemistry and the Natural Sciences, 3rd ed.,
Springer Series in Synergetics Vol. 13 (Springer-Verlag,
Berlin, 2004).
[127] Inken Siemon, Alexander S Holevo, and Reinhard F
Werner, Unbounded generators of dynamical semigroups,
Open Syst. Inf. Dyn. 24, 1740015 (2017).
[128] Robert Alicki, Comment on “Reduced dynamics need
not be completely positive”, Phys. Rev. Lett. 75, 3020
(1995).
[129] Peter Stelmachovic and Vladimir Buzek, Dynamics of
open quantum systems initially entangled with environment: Beyond the Kraus representation, Phys. Rev. A 64,
062106 (2001).
[130] For a review, see, for example, R. Alicki and K. Lendi,
Quantum Dynamical Semigroups and Applications
(Springer, New York, 2007); H.-P. Breuer and F.
Petruccione, The Theory of Open Quantum Systems
(Oxford University Press, New York, 2002).
[131] R. F. Pawula, Approximation of the linear Boltzmann
equation by the Fokker-Planck equation, Phys. Rev.
162, 186 (1967).
[132] R. P. Feynman and F. L. Vernon, The theory of a general
quantum system interacting with a linear dissipative
system, Ann. Phys. (N.Y.) 24, 118 (1963).
[133] Andrzej Jamiołkowski, Linear transformations which
preserve trace and positive semidefiniteness of operators,
Rep. Math. Phys. 3, 275 (1972).
[134] Man-Duen Choi, Completely positive linear maps on
complex matrices, Linear Algebra Its Appl. 10, 285 (1975).
[135] Richard Jozsa, Fidelity for mixed quantum states, J. Mod.
Opt. 41, 2315 (1994) (Lemma 7 introduced this result to
the quantum information community).
[136] A helpful suggestion by Carlo Sparaciari has streamlined
the presentation of this section.

PHYS. REV. X 13, 041040 (2023)

[137] Mark Srednicki, Is purity eternal?, Nucl. Phys. B410, 143
(1993).
[138] R. Alicki, M. Fannes, and A. Verbeure, Unstable particles
and the Poincare semigroup in quantum field theory,
J. Phys. A 19, 919 (1986).
[139] David Beckman, Daniel Gottesman, M. A. Nielsen, and
John Preskill, Causal and localizable quantum operations,
Phys. Rev. A 64, 052309 (2001).
[140] Avinash Baidya, Chandan Jana, R. Loganayagam, and
Arnab Rudra, Renormalization in open quantum field
theory. Part I. Scalar field theory, J. High Energy Phys.
11 (2017) 204; also, initial work by D. Poulin and J.
Preskill (unpublished).
[141] Jonathan Oppenheim and Zachery Weller-Davies, Lorentz
invariant information destruction is not Lorentz covariant
(to be published).
[142] Jonathan Oppenheim and Zachary Weller-Davies, Covariant path integrals for quantum fields back-reacting on
classical space-time, arXiv:2302.07283.
[143] Stephen Boyd, Stephen P. Boyd, and Lieven
Vandenberghe, Convex Optimization (Cambridge University Press, Cambridge, England, 2004), Appendix A.5.5.
[144] A Holevo, Covariant quantum Markovian evolutions,
J. Math. Phys. (N.Y.) 37, 1812 (1996).
[145] Bryce S. DeWitt, Quantum theory of gravity. I. The
canonical theory, Phys. Rev. 160, 1113 (1967).
[146] Jonathan Oppenheim, The constraints of a continuous
realisation of hybrid classical-quantum gravity (to be
published).
[147] More rigorously, for any Cauchy surface we define
observables
R in terms of a smearing function Fðx; tÞ and
ϕ½F ≔ dxdtϕðx; tÞFðx; tÞ over a small interval in time.
We then have the covariant commutation relations
½ϕ½F; ϕ½G ¼ ΔðF; GÞ where Δ is the Pauli-Jordan function. This can be used to define the algebra of observables for operators ð□ þ m2 Þϕ ¼ 0, ϕ½ð□ þ m2 ÞF ¼ 0.
Then we use the GNS theorem to relate the algebraic states
to the Hilbert space. See, for example, Refs. [148–151].
In general, care must be taken in defining the algebra
of observables for quantum fields in evolving space-times,
or in the case of some time-dependent Hamiltonians
[152–155].
[148] Romeo Brunetti, Klaus Fredenhagen, and Rainer Verch,
The generally covariant locality principle–a new paradigm for local quantum field theory, Commun. Math. Phys.
237, 31 (2003).
[149] Christopher J. Fewster and Rainer Verch, Dynamical
locality and covariance: What makes a physical theory
the same in all spacetimes?, Ann. Inst. Henri Poincaré 13,
1613 (2012).
[150] Klaus Fredenhagen and Falk Lindner, Construction of
KMS states in perturbative QFT and renormalized
Hamiltonian dynamics, Commun. Math. Phys. 332, 895
(2014).
[151] Klaus Fredenhagen and Kasia Rejzner, Quantum field
theory on curved spacetimes: Axiomatic framework and
examples, J. Math. Phys. (N.Y.) 57, 031101 (2016).
[152] Abhay Ashtekar and Anne Magnon, Quantum fields in
curved space-times, Proc. R. Soc. A 346, 375 (1975).

041040-35

## PDF page 36

JONATHAN OPPENHEIM

PHYS. REV. X 13, 041040 (2023)

[153] M. Asorey, Jose F. Carinena, and M. Paramio, Quantum
evolution as a parallel transport, J. Math. Phys. (N.Y.) 23,
1451 (1982).
[154] Charles G. Torre and Madhavan Varadarajan, Functional
evolution of free quantum fields, Classical Quantum
Gravity 16, 2651 (1999).
[155] Ivan Agullo and Abhay Ashtekar, Unitarity and ultraviolet
regularity in cosmology, Phys. Rev. D 91, 124010 (2015).
[156] Jonathan Oppenheim and Zachary Weller-Davies, The
constraints of post-quantum classical gravity, J. High
Energy Phys. 02 (2022) 080.
[157] Flavio Mercati, A shape dynamics tutorial, arXiv:
1409.0105.
[158] E. Anderson, J. Barbour, B. Z. Foster, B. Kelleher, and
N. O. Murchadha, The physical gravitational degrees of
freedom, Classical Quantum Gravity 22, 1795 (2005).
[159] Henrique Gomes and Tim Koslowski, The link between
general relativity and shape dynamics, Classical Quantum
Gravity 29, 075009 (2012).
[160] Albert Einstein, Do gravitational fields play an essential
part in the structure of the elementary particles of matter?,
189 (1952).
[161] Jochum J. Van der Bij, H. Van Dam, and Yee Jack Ng,
The exchange of massless spin-two particles, Physica
(Amsterdam) A116, 307 (1982).
[162] Steven Weinberg, The cosmological constant problem,
Rev. Mod. Phys. 61, 1 (1989).
[163] William G. Unruh, Unimodular theory of canonical
quantum gravity, Phys. Rev. D 40, 1048 (1989).
[164] Enrique Alvarez, Can one tell Einstein’s unimodular
theory from Einstein’s general relativity?, J. High Energy
Phys. 03 (2005) 002.
[165] Lee Smolin, Quantization of unimodular gravity and the
cosmological constant problems, Phys. Rev. D 80, 084003
(2009).
[166] Mikhail Shaposhnikov and Daniel Zenhäusern, Scale
invariance, unimodular gravity and dark energy, Phys.
Lett. B 671, 187 (2009).
[167] This deviation has since been made more precise in
Refs. [50,168].
[168] Jonathan Oppenheim and Andrea Russo, Gravity in the
diffusion regime (to be published).
[169] Vera C. Rubin and W. Kent Ford, Jr., Rotation of the
andromeda nebula from a spectroscopic survey of emission regions, Astrophys. J. 159, 379 (1970).
[170] Jonathan Oppenheim and Zachary Weller-Davies, Path integrals for classical-quantum dynamics, arXiv:2301.04677.
[171] This purified state is reminiscent of the thermofield double
state, so ubiquitous in discussions around the AdS=CFT
correspondence. It suggests that some of the apparent
paradoxes [172–175] found in that context might be
resolved by restricting measurements in this manner.
[172] Donald Marolf and Aron C. Wall, Eternal black holes and
superselection in AdS=CFT, Classical Quantum Gravity
30, 025001 (2012).
[173] Kyriakos Papadodimas and Suvrat Raju, State-dependent
bulk-boundary maps and black hole complementarity,
Phys. Rev. D 89, 086010 (2014).
[174] Daniel Louis Jafferis, Bulk reconstruction and the HartleHawking wavefunction, arXiv:1703.01519.

[175] Jonathan Oppenheim, Does Ads/CFT have an ensemble
ambiguity problem? (unpublished).
[176] Isaac Layton and Jonathan Oppenheim, The classicalquantum limit, arXiv:2310.18271.
[177] See Refs. [65,144,178,179] for extensions of Noether’s
theorem to semigroups.
[178] John C. Baez and Brendan Fong, A Noether theorem for
Markov processes, J. Math. Phys. (N.Y.) 54, 013301 (2013).
[179] Iman Marvian and Robert W. Spekkens, Extending
Noether’s theorem by quantifying the asymmetry of quantum states, Nat. Commun. 5, 3821 (2014).
[180] J. David Brown and J. W. York, Jr., Quasilocal energy in
general relativity, Quasilocal energy in general relativity,
IFP-421-UNC, TAR-014-UNC, 1991.
[181] Isaac Layton, Jonathan Oppenheim, Andrea Russo, and
Zachary Weller-Davies, The weak field limit of quantum
matter back-reacting on classical spacetime, J. High
Energy Phys. 08 (2023) 163.
[182] Nima Arkani-Hamed, Savas Dimopoulos, and Gia Dvali,
The hierarchy problem and new dimensions at a millimeter, Phys. Lett. B 429, 263 (1998).
[183] We use the term to mean a generalization of the usual
constraint algebra, since we may require more than one
bilinear map (the Poisson bracket, the commutator, a CQ
bracket such as that of Sec. IVA, as well as the stochastic
terms of the master equation, which are generally not
bilinear maps).
[184] Angelo Bassi, Kinjalk Lochan, Seema Satin, Tejinder P.
Singh, and Hendrik Ulbricht, Models of wave-function
collapse, underlying theories, and experimental tests, Rev.
Mod. Phys. 85, 471 (2013).
[185] Jonas Schmöle, Mathias Dragosits, Hans Hepach, and
Markus Aspelmeyer, A micromechanical proof-of-principle
experiment for measuring the gravitational force of milligram masses, Classical Quantum Gravity 33, 125031 (2016).
[186] Daniel Carney, Philip C. E. Stamp, and Jacob M. Taylor,
Massive non-classical states and the observation of quantum gravity: A user’s manual, arXiv:1807.11494.
[187] Dvir Kafri and J. M. Taylor, A noise inequality for classical
forces, arXiv:1311.4558.
[188] Sougato Bose, Anupam Mazumdar, Gavin W. Morley,
Hendrik Ulbricht, Marko Toroš, Mauro Paternostro,
Andrew A. Geraci, Peter F. Barker, M. S. Kim, and
Gerard Milburn, Spin entanglement witness for quantum
gravity, Phys. Rev. Lett. 119, 240401 (2017).
[189] Chiara Marletto and Vlatko Vedral, Gravitationally induced entanglement between two massive particles is
sufficient evidence of quantum effects in gravity, Phys.
Rev. Lett. 119, 240402 (2017).
[190] This follows from results in entanglement theory [191,192]
that entanglement between two separated systems cannot be
created through the exchange of fully decohered systems
[193] (sometimes called local operations and classical
communication). In this case, the gravitational degrees of
freedom are the fully decohered system, as can be seen by
writing the state in the form of Eq. (8). There is an assumption
that the transfer of preexisting entanglement from the
vacuum to the separated systems is small. Another
assumption is that the interactions do not violate cluster
separation, which some realizations of classical quantum

041040-36

## PDF page 37

A POSTQUANTUM THEORY OF CLASSICAL GRAVITY?
dynamics could do, but we would anticipate this to be a small
effect, comparable to the transfer of vacuum entanglement.
[191] John Preskill, Lecture notes for physics 229: Quantum
information and computation, California Institute of
Technology, 1998, http://theory.caltech.edu/~preskill/ph229/.
[192] Michael A. Nielsen and Isaac L. Chuang, Quantum
Computation and Quantum Information (Cambridge
University Press, Cambridge, England, 2010).

PHYS. REV. X 13, 041040 (2023)

[193] Reinhard F. Werner, Quantum states with einsteinPodolsky-Rosen correlations admitting a hidden-variable
model, Phys. Rev. A 40, 4277 (1989).
[194] A Kossakowski, On necessary and sufficient conditions for
a generator of a quantum dynamical semi-group, Bull.
Acad. Polon. Sci. Math. 20, 1021 (1972), https://pascalfrancis.inist.fr/vibad/index.php?action=getRecordDetail&
idt=PASCAL7313011632.

041040-37
