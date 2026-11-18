Source: see manifest row of the PDF
PDF sha256: 927ab03fe1bbe9a681c5bd3ad7b07c9d28be5619ad248defd3cff80a5193b301
License: CC-BY-4.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of munoz_arias_2023_phase_space_geometry_and_optimal_state_preparation_in_quantum_metrology_with_collective_spins.pdf

Transcription of `munoz_arias_2023_phase_space_geometry_and_optimal_state_preparation_in_quantum_metrology_with_collective_spins.pdf` in this directory, 27 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-27 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

PRX QUANTUM 4, 020314 (2023)

Phase-Space Geometry and Optimal State Preparation in Quantum Metrology
with Collective Spins
Manuel H. Muñoz-Arias ,1,2,* Ivan H. Deutsch,1 and Pablo M. Poggi
1

1,3,†

Center for Quantum Information and Control, Department of Physics and Astronomy, University of New Mexico,
Albuquerque, New Mexico 87131, USA
2
Institut Quantique and Département de Physique, Université de Sherbrooke, Sherbrooke, Quebec J1K 2R1,
Canada
3
Department of Physics and SUPA, University of Strathclyde, Glasgow G4 0NG, United Kingdom
(Received 8 November 2022; revised 1 February 2023; accepted 28 March 2023; published 25 April 2023)
We revisit well-known protocols in quantum metrology using collective spins and propose a unifying
picture for optimal state preparation based on a semiclassical description in phase space. We show how
this framework allows for quantitative predictions of the timescales required to prepare various metrologically useful states, and that these predictions remain accurate even for moderate system sizes, surprisingly
far from the classical limit. Furthermore, this framework allows us to build a geometric picture that relates
optimal (exponentially fast) entangled probe preparation to the existence of separatrices connecting saddle
points in phase space. We illustrate our results with the paradigmatic examples of the two-axis countertwisting and twisting-and-turning Hamiltonians, where we provide analytical expressions for all the
relevant optimal timescales. Finally, we propose a generalization of these models to include p-body collective interaction (or p-order twisting), beyond the usual case of p = 2. Using our geometric framework,
we prove a no-go theorem for the local optimality of these models for p > 2.
DOI: 10.1103/PRXQuantum.4.020314

I. INTRODUCTION
Quantum metrology employs nonclassical states as a
resource for estimating unknown parameters with a sensitivity beyond that allowed by the standard quantum limit
[1–4]. Of particular interest are ensembles of qubits (real
or pseudospins) for use in clocks and magnetometers.
Typically, one considers collective spins of total angular
momentum components Jˆα . Examples of metrologically
useful quantum states of collective spins include spin
squeezed states of atoms [5–9], cat states or GreenbergerHorne-Zeilinger states [10,11], and Dicke states [12],
among others. The aforementioned examples share the
common property of being entangled, and it is well known
that entanglement is essential, but not suﬃcient, to enable
sensitivity going beyond what can be achieved with classical resources (i.e., with separable states) [1,13].
The problem of local quantum metrology [14] can be
regarded as a problem of optimal state preparation whereby
*
†

munm2002@usherbrooke.ca
ppoggi@unm.edu

Published by the American Physical Society under the terms of
the Creative Commons Attribution 4.0 International license. Further distribution of this work must maintain attribution to the
author(s) and the published article’s title, journal citation, and
DOI.

2691-3399/23/4(2)/020314(27)

one seeks to prepare a metrologically useful state in the
shortest amount of time possible. For example, in their pioneering work Kitagawa and Ueda [5] studied the preparation of spin squeezed states, introducing one-axis twisting
(OAT) and two-axis countertwisting (2ACT) Hamiltonians. Here, the term “twisting” refers to generators that
are quadratic in the collective spin operators (Jˆx , Jˆy , Jˆz ).
While both Hamiltonians successfully generate squeezing, the OAT (Ĥ ∼ Jˆ2x ) does not saturate the fundamental
bound of sensitivity dictated by quantum metrology and
the maximum squeezing is reached at a time that scales
as J 1/η , where J is the size of the collective spin and η >
1. On the other hand, the 2ACT (Ĥ ∼ Jˆ2x − Jˆ2y ) reaches
peak spin squeezing in a time that is logarithmic in the
size of the collective spin, and saturates the fundamental limit of sensitivity imposed by quantum mechanics.
Later, Micheli et al. [15] studied a model in which the
OAT generator is combined with a transverse ﬁeld, leading to twisting-and-turning (TaT) dynamics. They showed
that this new generator permits the preparation of highly
entangled metrologically relevant states, i.e., catlike states,
at times that are logarithmic in the size of the collective
spin, and that the best performance is obtained when the
ratio of twisting and external ﬁeld strengths assumes a critical value. Related work by Sorelli et al. [16] investigated
the twist-and-turn generator in the short time regime (complementary to Ref. [15]), and argued for the optimality of

020314-1

Published by the American Physical Society

## PDF page 2

MUÑOZ-ARIAS, DEUTSCH, and POGGI

PRX QUANTUM 4, 020314 (2023)

this dynamics in the generation of spin squeezing. Furthermore, previous works by Yukawa et al. [17] and Kajtoch
et al. [18] have explored in detail the dynamics generated by the 2ACT Hamiltonian, emphasizing the diﬀerent
types of metrologically relevant states that are generated
and verifying, either numerically or semianalytically, the
logarithmic dependence of their preparation times with the
size of the collective spin.
In this work we revisit these protocols and present a uniﬁed description of optimal state preparation for quantum
metrology in collective spin systems based on their semiclassical dynamics. In our approach, we consider the evolution of a state that is described as a distribution in phase
space and approximate the dynamics of that state at short
and intermediate times by evolving a point on a ﬁxed contour of such a distribution using the (mean-ﬁeld) classical
equations of motion. When starting from an uncorrelated
state, e.g., a spin coherent state, the dynamics generates
a spin squeezed state that indeed displays quantum correlations. These states are approximately described by our
framework as Gaussian states with unbalanced variances
along orthogonal directions. This is akin to the numerical sampling of the phase-space distribution employed in
solving for the quantum state using the truncated Wigner
approximation; see, for instance, Refs. [19,20]. We discuss
how optimal (i.e., exponentially fast) state preparation is
associated with the existence of saddle points in the classical ﬂow deﬁned by the collective spin Hamiltonian. Using
this picture, we develop a comprehensive analysis of the
geometry of the separatrix and identify the key properties that guarantee the local and global optimality for state
preparation in generic collective spin models. We revisit
the problems of 2ACT and TaT and use this semiclassical approach to derive new expressions for the timescales
required to achieve several types of useful states for
metrology. This establishes a solid theoretical foundation
to the timescales that were previously found numerically
[17,18]. We then apply this framework to the previously
unexplored problem of using higher-order twisting genp
erated by Hamiltonians of the form Jn̂ , with p ≥ 2, to
generate spin squeezing and metrologically useful states.
We show that, while p-body 2ACT is optimal only for
p = 2, a notion of optimality can be redeﬁned for p-body
TaT in the case of p = 3.
The remainder of the manuscript is organized as follows. In Sec. II we give an overview of the semiclassical
description of collective spin systems and of basic aspects
of quantum metrology. In Sec. III we study the 2ACT
Hamiltonian, its phase-space structure and dynamics, and
derive analytical results for the preparation times of several
entangled states useful for quantum metrology. From this
analysis we distill the conditions of the separatrix geometry that guarantee the local and global optimality of a
given collective spin Hamiltonian for state preparation.
In Sec. IV we turn our attention to the TaT Hamiltonian

and provide three diﬀerent physical interpretations for the
“critical coupling” regime ﬁrst identiﬁed in Ref. [15]. In
Sec. V we introduce generalizations of the 2ACT and
TaT Hamiltonians by adding higher-order twisting terms
and we prove several results that indicate that secondorder twisting is optimal. Finally, in Sec. VI we present
some concluding remarks and discuss potential avenues for
future work.
II. QUANTUM METROLOGY WITH
COLLECTIVE SPIN SYSTEMS
A. Collective spin systems and their classical limit
We consider systems of N spin- 12 particles described
by the set of collective angular
∑ momentum operators Ĵ =
(Jˆx , Jˆy , Jˆz ), where Jˆα = 12 Ni=1 σ̂α(i) and σ̂α(i) is a Pauli
operator acting on particle i, α = x, y, z. Any Hamiltonian
of the form
∑
∑
∑
Ĥ =
aα Jˆα +
bαβ Jˆα Jˆβ +
cαβγ Jˆα Jˆβ Jˆγ
α

+ · · · + H.c.

αβ

αβγ

(1)

describes a collective spin model, where particles interact uniformly among themselves and with external ﬁelds.
By construction, Hamiltonian Ĥ commutes with the total
angular momentum operator Jˆ2 , and so the total spin value
J is conserved. We focus on the subspace of J = N /2,
often called the symmetric subspace, which is composed
of all pure states that are invariant under permutation of
any two particles [21]. Two convenient choices of basis for
this subspace are the Dicke states {|J , m⟩}, m = −J , −J +
1, . . . , J , which are the eigenvectors of Jˆz , and the over|θ, φ⟩ =
complete basis of spin
states
∣ coherent
∣ (SCSs)
⟩⊗N
⟩
e−iφ Jˆz e−iθ Jˆy |J , J ⟩ = ∣↑θ ,φ
, where ∣↑θ ,φ describes the
state of a single qubit pointing up along the (θ, φ) direction
on the Bloch sphere, and 0 ≤ θ ≤ π , 0 ≤ φ ≤ 2π .
Any Hamiltonian of the form (1) admits a well-deﬁned
classical description in the thermodynamic limit N → ∞.
This description, in turn, coincides with the mean-ﬁeld
limit of the model, making these models quantum meanﬁeld models [22], and can be obtained from the equations
of motion for the expected values of spin components,
d⟨Jˆα ⟩/dt = −i⟨[Jˆα , H ]⟩ with α = x, y, z (ℏ = 1). In the
thermodynamic limit this leads to equations of motion
for a phase-space ﬂow for the classical variables R ≡
(X , Y, Z) = limJ →∞ ⟨Ĵ⟩/J by neglecting correlations and
setting ⟨AB⟩ = ⟨A⟩⟨B⟩. This ﬂow has the form dR/dt =
F[R] and describes the nonlinear motion of a “top” on
a unit sphere since X 2 + Y2 + Z 2 = 1. The properties of
the ﬂow can be studied locally by identifying the ﬁxed
points, i.e., R∗ such that F[R∗ ] = 0, and analyzing their
stability through calculation of the Jacobi matrix, M[R] =
∂F/∂R. If det M > 0, the ﬁxed point is stable or elliptic,

020314-2

## PDF page 3

PHASE-SPACE GEOMETRY AND OPTIMAL STATE PREPARATION. . .

PRX QUANTUM 4, 020314 (2023)

The resulting probe state then undergoes another transformation that imprints the unknown parameter μ into
the state, typically as in ρ̂μ (t) = e−iμĜ ρ̂(t)eiμĜ . Finally,
measurements are performed on ρ̂μ (t) according to a wellchosen positive operator-valued measurement (POVM),
from which an (unbiased) estimator μ̂ of the parameter μ
is constructed. The variance of such an estimator, denoted
μ, has a fundamental limit that is given by the quantum
Cramer-Rao bound,

(a)

(b)

μ≥

FIG. 1. (a) Phase-space portrait of the classical motion of a
collective spin system. Prominent phase-space structures include
stable orbits and saddle points. (b) Interferometric approach to
quantum metrology with collective spins. A product state ρ(0)
undergoes a state preparation procedure to yield the probe state
ρ(t), which is then used to sense an unknown parameter μ.

and if det M < 0, it is a saddle or hyperbolic ﬁxed point.
In Fig. 1(a) we illustrate the local motion of each case.
In particular, the vicinity of a saddle point is described
by two directions in phase space, one unstable n+ and
one stable n− , along which the motion is of the form
Ṙ± (t) = ±λR± (t) and so R± (t) ∝ e±λt R± (0). As a result,
local motion along an unstable branch leads to an exponential stretching of trajectories in phase space. Globally,
a given ﬂow may possess many hyperbolic ﬁxed points,
and their stable and unstable branches are typically connected by an isolated trajectory in phase space that is called
the separatrix. In Sec. III we illustrate how the geometric properties of the separatrix in the classical phase space
aﬀect the motion of quantum states, and in particular we
study how to use this knowledge to study the generation of
metrologically useful states.
B. Basic aspects of quantum metrology
The goal of quantum metrology [1] is to estimate the
value of a weak signal encoded as an unknown physical parameter μ in a quantum system, and to do so with
a precision beyond what is achievable with solely classical resources. There are many approaches to this problem,
including quantum critical metrology [23,24], the use of
chaotic sensors [25], nonlinear metrology [26–28], the use
of interaction-based readouts [29–32], or twist-and-untwist
protocols [33]. In this work, we focus on the interferometric approach [3], which is schematically depicted
in Fig. 1(b). In this scheme, a probe state is prepared
through evolution under a chosen Hamiltonian acting on
an easy to prepare initial state, ρ̂(t) = e−iĤprep t ρ̂(0)eiĤprep t .

1
μQCR = √
,
νFQ [ρ̂μ ]

(2)

where ν is the number of independent measurements and
FQ [ρ̂μ ] is the quantum Fisher information (QFI). For the
present scheme, assuming that ρ̂(t) = |ψ(t)⟩⟨ψ(t)| is pure
and in the absence of noise or decoherence, the QFI takes
the simple form
FQ [|ψ⟩, Ĝ] = 4⟨ Ĝ(t)⟩2 = 4(⟨G(t)2 ⟩ − ⟨G(t)⟩2 ),

(3)

where ⟨A(t)⟩ ≡ ⟨ψ(t)| Â |ψ(t)⟩. The maximum sensitivity
predicted by the quantum Cramer-Rao bound is achieved
only if one can implement the optimal measurement
(POVM), which is problem dependent and often challenging in practice. Nevertheless, we consider the QFI as one of
the ﬁgures of merit to quantify metrological performance.
For the purposes of this work, we consider the unknown
parameter μ to be a small angle of rotation of the collective spin around a known axis n such that Ĝ = Jˆn .
If the probe state |ψ(t)⟩ is a SCS, the maximum QFI
gives FQ [ρ̂μ ] ∝ N . This is often referred to as the standard
quantum limit (SQL), and provides a reference point to
gauge the usefulness of a proposed quantum metrological
strategy. Any strategy making use of quantum resources
that permits a sensitivity of the estimator going above the
standard quantum limit is advantageous. When entangled
states are allowed, the maximum possible QFI can scale as
FQ [ρ̂μ ] ∝ N 2 , which is referred to as the Heisenberg limit.
In this work we focus on how the semiclassical picture
ascribed to Ĥprep can be used to understand the preparation
of metrologically useful states, and to make predictions
about the times required to reach them. To quantify this,
one ﬁgure of merit is the metrological gain based on the
QFI, deﬁned as
ζ2 =

N
FQ [|ψ⟩, Jˆ ⃗n ]

,

(4)

where any value of ζ 2 < 1 will indicate improvement over
the SQL. In addition, we also consider metrology protocols in which the POVM is not necessarily optimal, but
restricted to a speciﬁc type. In particular, for a Ramseytype interferometer, as is used in clocks and magnetometers, the metrological gain is quantiﬁed by the Wineland

020314-3

## PDF page 4

MUÑOZ-ARIAS, DEUTSCH, and POGGI

PRX QUANTUM 4, 020314 (2023)
variables R = (X , Y, Z) read

squeezing parameter [9]
ξ ≡
2

ϕ2
⟨ Jˆ⊥ ⟩2
=
2J
.
2
ϕSCS
|⟨Ĵ⟩|2

(5)

Here, ϕ is the uncertainty in the measurement of the
desired phase in the interferometer and ϕSCS is the corresponding uncertainty when the input probe state is a SCS.
This can be reexpressed in terms of the collective spin
variables, where ⟨ Jˆ⊥ ⟩ is the projection noise of the collective spin perpendicular to the direction of rotation in
the sensor, and |⟨Ĵ⟩| is the length of the collective spin.
√
For an input SCS, ⟨ Jˆ⊥ ⟩ = J /2, |⟨Ĵ⟩| = J , and ξ 2 = 1.
For a spin squeezed state of the sort originally considered by Kitagawa and Ueda, one can have ξ 2 < 1 and
thus sensitivity in Ramsey interferometry beyond the SQL.
Furthermore, with suﬃcient squeezing one can attain scaling in improved sensitivity associated with the Heisenberg
limit, ξ 2 ∝ 1/N . In the next sections we analyze these
metrological ﬁgures of merit for diﬀerent state preparation protocols by leveraging the semiclassical picture of
collective spin systems.
III. PHASE-SPACE GEOMETRY AND QUANTUM
METROLOGY WITH THE TWO-AXIS
COUNTERTWISTING HAMILTONIAN
Two-axis countertwisting was introduced by Kitagawa
and Ueda as the mechanism to obtain the optimal spin
squeezed states, leading to Heisenberg scaling in the sensitivity [5]. Our goal in this section is to understand this fact
based on the geometrical properties of its classical phase
space. The 2ACT Hamiltonian describes the dynamics of
a collective spin Ĵ under the action of two twisting operations, i.e., quadratic nonlinearities, along the perpendicular
axis. As originally written in Ref. [5], this Hamiltonian is
given by
ĤCT = χ (Jˆ2π/2,π/4 − Jˆ2π/2,−π/4 ) =

χ 2
(Jˆ −Jˆ2 ),
2i + −

(6)

where χ is the countertwisting strength, and we have
chosen the two axes as the ±45◦ directions
√ in the xy plane, such that Jˆπ/2,±π/4 = (Jˆx ± Jˆy )/ 2. Using the
latter expression, Eq. (6) can be written as
ĤCT = χ (Jˆx Jˆy + Jˆy Jˆx ).

dX
= χ̃XZ,
dt
dY
= −χ̃YZ,
dt
dZ
= −χ̃(X 2 − Y2 ),
dt

(7)

To investigate the phase-space geometry of the model in
Eq. (7), we proceed as described in Sec. II A to compute
its associated classical ﬂow (further details can be found
in Appendix A). The equations of motion for the classical

(8a)
(8b)
(8c)

where χ̃ = N χ and the ﬁxed points are given by
(X , Y, Z) = (0, 0, ±1),
(
)
1
1
(X , Y, Z) = √ , ∓ √ , 0 ,
2
2
)
(
1
1
(X , Y, Z) = − √ , ± √ , 0 ,
2
2

(9a)
(9b)
(9c)

which correspond to the north and south poles of the unit
sphere, and the poles of each of the twisting axis. Their stability is deduced from the Jacobi matrix M[R] = ∂F/∂R,
which in this case takes the form
⎞
⎛
χ̃ Z
0
χ̃ X
−χ̃ Z
−χ̃ Y⎠ .
M[R] = ⎝ 0
(10)
−4χ̃ X
4χ̃ Y
0
When evaluated at the ﬁxed point (X , Y, Z) = (0, 0, ±1),
Eq. (10) is diagonal with eigenvalues (±χ̃ , ∓χ̃ , 0). As the
nonzero eigenvalues are real and come in pairs M± =
±χ̃ , the ﬁxed point is a saddle point, and here the principal directions of the separatrix curve are orthogonal and
aligned with the x and y axes. In other words, they deﬁne
great circles in the x-z and y-z planes, respectively. Furthermore, as discussed in the previous section, we know
that an initial condition placed on one of the separatrix
branches will evolve according to dP± /dt = ±χ̃ P± , where
P± = X , Y. The other four ﬁxed points in Eqs. (9) are stable centers. This can be easily veriﬁed by looking at the
eigenvalues of the Jacobi matrix evaluated at the ﬁxed
points, which are given by λ± = ±i2χ̃ . This most basic
information about the ﬁxed points of 2ACT classical ﬂow
allows us to produce an accurate picture of the global structure of its phase-space trajectories, whose exact form is
shown in Fig. 2(a).
The local and global geometries of the separatrices provide useful information about the quantum evolution of an
initial SCS placed at either of the two poles, |J , ±J ⟩. Without loss of generality, consider the case with m = +J . As
depicted in Fig. 2(b), while evolving under ĤCT , the center of the distribution is ﬁxed and the quantum projection
noise will be initially squeezed exponentially fast, as the
distribution will get stretched out along the great circle
in the x-z plane and squeezed in along the great circle in

020314-4

## PDF page 5

PHASE-SPACE GEOMETRY AND OPTIMAL STATE PREPARATION. . .
(a)

PRX QUANTUM 4, 020314 (2023)

(b)

(c)

(d)

(e)

FIG. 2. (a) Phase-space portrait of the 2ACT phase-space ﬂow in the thermodynamic limit; cf. Eqs. (8). The red trajectory shows
the separatrix. (b) Semiclassical picture for the dynamics of a spin coherent state located at the saddle point of the corresponding
classical phase-space ﬂow. (c) Metrological gains based on spin squeezing (solid blue) and QFI (solid red) for the 2ACT dynamics.
The dashed lines show the time to the peak of each metrological gain computed in the main text. The results shown are for N = 100.
(d) Comparison between analytical estimates and exact numerical simulations of the time required to peak QFI and spin squeezing for
the 2ACT dynamics. (e) Time scales to diﬀerent metrologically relevant quantum states prepared with 2ACT dynamics as a function
of N . For the Yurke state, we consider α = 0.678.

the y-z plane. As a result, the motion along the separatrix branches leads to spin squeezing and thus governs the
generation of metrologically useful quantum states.
This qualitative picture can be made rigorous and used
to estimate the timescales required to generate optimal
spin squeezing and other metrologically relevant quantum states. To do this, we calculate the time required for
points to travel along sections of the separatrix lines. When
restricted to the unstable branch of the separatrix, Y = 0
and thus X 2 = 1 − Z 2 . From Eqs. (8) we have
dZ
= −χ̃(1 − Z 2 ),
dt

(11)

which is solved by
χ̃ t = −

∫ Z(tf )
Z(0)

dZ
.
1 − Z2

(12)

We can then compute how long it takes for a point starting
√ at a contour of the SCS uncertainty patch, Z(0) =
1 − 1/N , to travel along the separatrix to some ﬁnal
point Z(tf ) < Z(0) with tf > 0,
√
√
]
(1 − Z(tf ))( N + N − 1)
√
.
χ̃ t = ln
1 − Z 2 (tf )

A. Time to optimal spin squeezing and the ﬁrst peak of
the quantum Fisher information
Given our choice of initial state, one can readily see
that the length of the mean spin is given by |Ĵ| = ⟨Jˆz ⟩t .
Furthermore, we know that the antisqueezed projection
is Jˆx , the direction determined by the unstable separatrix
branch. Thus, at any later time t > 0 we can write these
two quantities as
|Ĵ| = J cos(θ),

(14)

where θ = θ (t) is the polar angle of spherical coordinates.
In this setting the variance being squeezed is that of Jˆy .
To compute its value, we proceed as follows. At the initial time, t = 0, the area of the uncertainty patch √
of the
SCS is that of a circle with radius Jx = Jy = J /2.
At any later time, t > 0, this area is that of an ellipse with
semimajor axis equal to Jx and semiminor axis equal
to Jy . Hamiltonian dynamics preserves the areas and
thus, after equating these two areas and solving for Jy ,
we obtain Jˆy = 1/2 sin(θ). The squeezing parameter in
Eq. (5) generated by this countertwisting is thus

[

2
ξCT
=

(13)

Finding the time to the diﬀerent metrologically relevant
quantum states is then translated into the problem of
ﬁnding the appropriate value of Z(tf ).

Jx = J sin(θ),

4
.
N sin2 (2θ )

(15)

This expression has a minimum at θ = π/4, the value at
2
which the optimal spin squeezing is achieved,√ξCT
= 4/N
[34]. We can see immediately that Z(tf ) = 1/ 2 gives the

020314-5

## PDF page 6

MUÑOZ-ARIAS, DEUTSCH, and POGGI

PRX QUANTUM 4, 020314 (2023)

timescale to optimal squeezing. Substituting this value into
Eq. (13) we obtain a principal result of this analysis:
√
√
√
sq
(16)
(χ̃t)CT = ln[( 2 − 1)( N + N − 1)].
We note that this straightforward geometric analysis permits the exact identiﬁcation of the numerical factor inside
the logarithm, improving over the numerical or semianalytical approaches of Refs. [17,18].
Let us now turn our attention to the evolution of the
QFI. In our setting, time evolution leads to squeezing of
Jˆy and so we consider the QFI with respect to small rotations around the x axis. This has a maximum whenever the
variance of Jˆx has a maximum, and the latter is guaranteed
to happen at the time at which the edges of the uncertainty
patch are as far from each other as is allowed by the phasespace geometry. This occurs when the state reaches points
on the separatrix that are diametrically opposed. Given our
choice of initial state, this happens when Z(tf ) = 0. Thus,
substituting this value of Z(tf ) into Eq. (13) we obtain the
time to the ﬁrst peak of the QFI, and consequently the time
to the ﬁrst peak of the metrological gain,
√
√
QFI
(χ̃t)CT = ln( N + N − 1) ≈ 12 ln(4N ),
(17)
where the rightmost side of Eq. (17) is valid in the limit of
N → ∞.
The expressions in Eqs. (16) and (17), albeit computed
from a completely classical perspective, give quantitative
predictions of the time required for a quantum system of
system size N evolving according to the 2ACT Hamiltonian to optimize metrological gain, be it measured by the
QFI or spin squeezing. In order to test this prediction, we
numerically simulate the quantum dynamics for various
values of N and compute the time-dependent metrological gains for each case. The case of N = 100 is shown
as an example in Fig. 2(c), where it can be seen that the
peaks of both quantities coincide with the predictions provided by our expressions. Furthermore, Fig. 2(d) shows a
systematic comparison between the exact numerical results
and the analytical predictions as a function of the system
size N . We ﬁnd excellent agreement between both, even
for system sizes as small as N ≃ 30, which is far from the
classical limit.
Finally, we point out that exploiting information about
the classical motion of points along sections of the separatrix allows us to also write explicit expressions for the
spin-squeezing parameter and quantum Fisher information
as a function of time. Further details of this analysis are
discussed in Appendix A 3.
B. Time to other quantum states relevant for quantum
metrology
Previous works [17,18] showed that starting from the
state |↑⟩⊗N = |J , J ⟩, namely, the stretched up state, one

can employ the dynamics of the 2ACT to prepare several
other quantum states that are useful for quantum metrology
with almost unit ﬁdelity, that is, |⟨|e−itĤCT |J , J ⟩|2 ≈ 1,
where |⟩ is one of the following: the Berry-Wiseman
state (BWS) [35], the equally weighted superposition state
(EWSS) [17], some Yurke states (YUSs) [36], and the
twin-Fock state [17]. Following our previous discussion,
here we use our semiclassical framework to derive expressions for the timescales required to prepare each of the ﬁrst
three states mentioned above, as these are the ones whose
ﬁdelity peaks before the ﬁrst peak of the QFI. In these
short timescales a Gaussian description suﬃces. Given
our choice of initial state, we only need to consider the
variance in order to compute the state overlap. For the
interested reader, we discuss the details in Appendix A 4.
As before, the time to the peaks of ﬁdelity to each of
these three states can be estimated using Eq. (13), and thus
we only need an appropriate value of Z(tf ). Recognizing
that, under the current setting, the variance of the timeevolved state goes as Jˆx = J sin(θ), then Z(tf ) can be
obtained from the variance of each of the states; see the
detailed discussion in Appendix A. Here we only list the
ﬁnal results.
For the BWS, we can ﬁnd lower and upper bounds for
the timescale, given by
√
√ √
√
<
(χ̃ t)BWS
= ln[( 8 − 7)( N + N − 1)],
CT
√ √
√
√
>
(χ̃ t)BWS
= ln[( 7 − 6)( N + N − 1)].
CT

(18a)
(18b)

For the EWSS, we ﬁnd that
√ √
√
√
= ln[( 3 − 2)( N + N − 1)],
(χ̃t)EWSS
CT

(19)

where the second line in Eq. (19) which holds in the limit
of N ≫ 1. For the family of Yurke states, we ﬁnd that
[(
(χ̃ t)YUS
CT = ln

√
)
]
√
2 − 2 + sin2 (α) √
√
( N + N − 1) ,
2 − sin2 (α)
(20)

an expression that is valid in the limit of N ≫ 1. The full
expression is given in Appendix A. Furthermore, we note
that only Yurke states with relatively small values of α are
prepared by the 2ACT dynamics (see Ref. [18] for a more
detailed discussion).
From the results above, one might ask why the classical picture allows us to predict the timescales fairly well.
To answer this, we can directly compare them with the
Ehrenfest time. For systems with exponential instabilities
originating at a saddle point, which can be characterized
with a positive Lyapunov exponent [37,38], this time is

020314-6

## PDF page 7

PHASE-SPACE GEOMETRY AND OPTIMAL STATE PREPARATION. . .
given by
)
(
1
1
,
ln
tErfst =
2sd
ℏeﬀ

(21)

ln(N )
.
2

experimentally. An alternative approach is to use a single
twisting operation complemented with a linear term, i.e., a
rotation term, resulting in a Hamiltonian of the form
ĤTaT = Jˆx + χ Jˆ2z ,

where sd is the Lyapunov exponent of the saddle and ℏeﬀ
is the eﬀective Plank constant. For collective spin systems,
one has ℏeﬀ = 1/N , and for the 2ACT Hamiltonian, we
know that CT
sd = χ̃; thus, the Ehrenfest time is given by
(χ̃ t)Erfst
CT =

PRX QUANTUM 4, 020314 (2023)

(22)

We show the diﬀerent timescales computed in this section,
including the Ehrenfest time, in Fig. 2(e). Excluding the
timescale to that peak QFI, all of the timescales with
the 2ACT correspond to times shorter than the Ehrenfest time, and thus one expects a semiclassical treatment
to yield accurate predictions. Note that our approach still
provides accurate results for timescales that are longer
than the Ehrenfest time, as illustrated by the validity of
QFI
the expression for (χ̃ t)CT . At this timescale most of the
support of the time-evolved state is still concentrated on
the eigenstate that overlaps considerably with the classical
separatrix [37], and thus our semiclassical approach based
on the separatrix geometry retains validity.
C. Summary
The analysis presented in this section provides us with
an intuitive picture of how collective spin Hamiltonians
generate metrologically useful states. The ﬁrst important
aspect is that one wants to construct a Hamiltonian having, in the classical limit, a saddle point, which is always
accompanied by a separatrix line. Then the geometrical
arrangement of the separatrix branches completely dictates
the evolution and metrological utility of states generated
from a SCS centered at the saddle point through Hamiltonian evolution. It is in this sense that the two-axis
countertwisting represents the optimal choice of Hamiltonian. The geometry of its separatrix is locally optimal,
since the branches are orthogonal, and it is globally optimal, since its branches deﬁned great circles on the unit
sphere, i.e., geodesics on the surface deﬁning phase space.
In the remainder of this work we use these lessons to study
other collective spin Hamiltonians and their potential for
the generation of metrologically useful quantum states.
IV. PHASE-SPACE GEOMETRY AND QUANTUM
METROLOGY WITH A
TWISTING-AND-TURNING HAMILTONIAN
While locally and globally optimal for preparation of
metrologically useful quantum states, the 2ACT Hamiltonian requires the use of two twisting operations along
the perpendicular axis, which is diﬃcult to implement

(23)

where  is the rate of turning and χ the twisting strength.
This model is often referred to as twisting and turning
in the quantum metrology literature [3,15,16,39–41], and
it has been implemented in spinor Bose-Einstein condensates [40], and could be readily implemented in certain
cavity QED setups [42,43]. One also recognizes this as
the Lipkin-Meshkov-Glick (LMG) model, describing a
transverse Ising model with all-to-all coupling [44–50].
In an early pioneering work [15] it was recognized that
the TaT dynamics generated by Eq. (23) prepares highly
entangled states at times that are logarithmic in the system
size N when starting from a spin coherent state centered at
the point (X , Y, Z) = (1, 0, 0), that is, |θ0 , ϕ0 ⟩ = |π/2, 0⟩.
This presents a signiﬁcant improvement over what is
achievable with the use of only a single twisting operation,
the so-called one-axis twisting Hamiltonian [3], and positions the TaT Hamiltonian on similar footing as the 2ACT
Hamiltonian. Our goal is to use the phase-space dynamics and separatrix geometry of this model to quantitatively
explain this fact. We point out that the phase-space description of this model has a direct connection to ground-state,
excited state, and dynamical quantum phase transitions of
the LMG model; we discuss this connection in Sec. IV D.
At the same time, it is directly connected to the rate of
entanglement generation, as was explored in Ref. [51].
Introducing χ̃ = N χ as before, the phase-space ﬂow
associated with the classical TaT dynamics is given by (see
Appendix B for further details)
dX
= −χ̃ YZ,
dt
dY
= −Z + χ̃ XZ,
dt
dZ
= Y.
dt

(24a)
(24b)
(24c)

The solutions of dX/dt = 0, leading to the ﬁxed points of
the ﬂow, depend on the system parameters. For /χ̃ > 1,
there are only two ﬁxed points at (X , Y, Z) = (±1, 0, 0),
i.e., the poles with respect to the turning axis. These are
stable, and so phase space is ﬁled with trajectories representing Larmor precession of the mean spin. On the
other hand, for /χ̃ < 1, there are four ﬁxed points, two
given by (X , Y, Z) = (±1, 0, 0), where the one at X = −1
is stable and the one at X = 1 is a saddle point. The two
additional ﬁxed points are at
√
(
( )2 )


(X , Y, Z) =
.
(25)
, 0, ± 1 −
χ̃
χ̃

020314-7

## PDF page 8

MUÑOZ-ARIAS, DEUTSCH, and POGGI

PRX QUANTUM 4, 020314 (2023)

The two parameter regimes are connected through a pitchfork bifurcation of the stable point at (X , Y, Z) = (1, 0, 0)
that occurs at the critical point, /χ̃ = 1. The stability of
the ﬁxed points in these two parameter regimes can be
investigated using the Jacobi matrix associated with the
ﬂow in Eqs. (24), and it is given by
⎛

0
M[X] = ⎝χ̃ Z
0

χ̃ Z
0


⎞
χ̃ Y
− + χ̃ X ⎠ .
0

(a)

(b)

(26)

As before, we focus on the motion around the saddle
point. The separatrix branches emerge from this point, and
conservation of energy guarantees that all points on the
separatrix have the same energy as the saddle. By evaluating the eigenvalues of the Jacobi matrix in Eq. (26) at
this saddle, one obtains its local Lyapunov exponent
√
TaT
sd = χ̃

(
)


1−
.
χ̃
χ̃

(27)

Equation (27) dictates the exponential rate at which points
move away from the saddle point. This rate is maximum when /χ̃ = 1/2, and the corresponding Lyapunov
exponent is given by TaT
sd |CC = χ̃ /2. In Ref. [15] this
parameter regimes was denoted “critical coupling,” and it
was shown to provide the fastest preparation time towards
a catlike state. Furthermore, Sorelli et al. [16] studied the
dynamics of TaT in the short time regime and it was argued
that the same parameter regime, i.e., critical coupling, was
locally optimal. The maximum of Eq. (27) already extends
the results of Refs. [15,16], as it shows that at critical
coupling, a point on the separatrix line travels with the
maximum velocity allowed by ĤTaT . We present a formal
result of this statement in Sec. IV C.
A. Separatrix geometry and the physical meaning of
critical coupling
The importance of the separatrix geometry was already
recognized in Ref. [15]. In fact, they deﬁned critical
coupling as the parameter regime at which the distance
between opposite ends of the separatrix was maximal, i.e.,
equal to one diameter of the unit sphere [52]. We illustrate
the structure of the TaT phase-space ﬂow and separatrix
line at critical coupling in Fig. 3(a).
From our previous discussion, we learned that critical
coupling is also the parameter regime at which the Lyapunov exponent of the saddle point is maximum. One can
also show that at critical coupling the branches of the separatrix in the vicinity of the saddle point are orthogonal. In
Appendix B we show that, for an arbitrary value of /χ̃ ,

FIG. 3. (a) Phase portrait of the phase-space ﬂow of the TaT
Hamiltonian at critical coupling. The separatrix is shown in solid
red. (b) Metrological gains, at critical coupling, based on the
squeezing (solid blue) and the QFI (solid red) for an initial SCS
along the positive x direction. The dashed lines show our result
for the time to peak of each metrological gain. Results are for a
system with N = 1024.

the angle between separatrix branches is
cos(υ) =

2
2 − χ̃ /  + (χ̃ /2)2 Z 2
− 1,
≈
2
2
χ̃ /  − (χ̃ /2) Z
χ̃

(28)

where υ is the angle between separatrix branches, and
the far right holds in the vicinity of the saddle point, i.e.,
Z, Y → 0. Thus, when χ̃ = 2, at critical coupling, we
have υ = π/2 and the separatrix branches are orthogonal.
Qualitatively, the result in Eq. (28) tells us that, locally
in the vicinity of the saddle point and at critical coupling,
the TaT Hamiltonian is, eﬀectively, a 2ACT Hamiltonian.
One can formalize this statement by an appropriate choice
of the collective spin axis. In particular, if we consider
Jˆ1 =

Jˆy + Jˆz
,
√
2

Jˆ2 =

Jˆz − Jˆy
,
√
2

Jˆx = J − ô,
(29)

with Jˆ1 and Jˆ2 representing two orthogonal directions in
the y-z plane at 45◦ and −45◦ , respectively. Furthermore,
we are only interested in dynamics taking place within the
vicinity of the saddle point, and exploit this fact to write
Jˆx = J − ô, its mean-ﬁeld minus ﬂuctuations, with ô an
operator representing the ﬂuctuations. Using Eq. (29), we

020314-8

## PDF page 9

PHASE-SPACE GEOMETRY AND OPTIMAL STATE PREPARATION. . .
can rewrite Eq. (23) as
(
eﬀ
ĤTaT
= J −

)
χ
χ
ô + (Jˆ1 Jˆ2 + Jˆ2 Jˆ1 ),
−
2
2

(30)

for a point at the border of the √
uncertainty patch, which
now takes the form Z(0) = 1/ 2N , to travel to some
ﬁnal location Z(tf ) along the separatrix. This timescale is
given by
√
√
]
Z(tf )( 2N + 2N − 1)
√
(χ̃ t)TaT = 2 ln
.
1 + 1 − Z 2 (tf )
[

where we have ignored terms O(ô2 ); see Appendix B for
details.
At critical coupling Eq. (30) becomes
eﬀ
=
ĤTaT

χ
(Jˆ1 Jˆ2 + Jˆ2 Jˆ1 ),
2

(31)

which is a 2ACT Hamiltonian, as that in Eq. (7). The form
of the Hamiltonian in Eq. (31) points at a general result.
Any collective spin Hamiltonian whose associated phasespace ﬂow has a saddle point with orthogonal separatrix
branches can always be mapped locally to an eﬀective
2ACT Hamiltonian under the appropriate choice of axis.
In summary, the diﬀerent properties that deﬁne critical coupling, χ̃ = 2, for the TaT Hamiltonian are as
follows.
1. The distance between the separatrix branches is
maximal, and equal to the diameter in the unit
sphere.
2. The Lyapunov exponent of the saddle point is maximal, and equal to TaT
sd |CC = χ̃ /2.
3. The separatrix branches are orthogonal in the vicinity of the saddle point, and thus, locally, the TaT
Hamiltonian is eﬀectively a 2ACT Hamiltonian.
4. Also, the local wells of the classical energy surface to the left and right sides of the saddle point
have the same depth, and thus time evolution happens symmetrically around the saddle point (see
Appendix B).
Condition 4 above is fundamental to the validity of our
semiclassical approach. Up to now we did not require it
explicitly, as both 2ACT and TaT satisfy it for all parameter ranges. However, it will be essential in generalizations
of TaT, and we comment further on its importance in
Sec. V.
B. Time scales to peak spin squeezing and to the ﬁrst
peak of the QFI
In this subsection we focus on the special case of critical
coupling and compute the timescales to peak spin squeezing and the ﬁrst peak of the QFI using the traveling time
of points along some sections of the separatrix branches.
Following Refs. [15,16] we consider an initial SCS centered at the positive x direction, that is, |θ0 , ϕ0 ⟩ = |π/2, 0⟩.
In a similar fashion to the 2ACT analysis, the center of
the uncertainty patch is ﬁxed, and the TaT dynamics only
stretches and squeezes the uncertainty patch. As before, we
can approximate the desired timescales by the time it takes

PRX QUANTUM 4, 020314 (2023)

(32)

The details of its derivation are given in Appendix B. The
problem now becomes how to ﬁnd the appropriate value of
Z(tf ) for a given timescale.
1. Time scale to peak spin squeezing
The third bullet point at the end of Sec. IV A points at
the fact that, locally, the separatrix branches of TaT must
be aligned with great circles. Here we exploit this fact in
order to estimate the appropriate value of Z(tf ) for the peak
squeezing timescale. The key ingredient in this analysis is
the fundamental theorem of the local theory of parametric curves (see Chapter 1 of Ref. [53]). This result tells us
that, up to rigid motions (displacements and rotations), a
curve is completely characterized by its values of curvature κ and torsion τ . Hence, given two curves of interest,
one can investigate their local equivalence by ﬁnding the
range of parameter values for which they both have the
same curvature and torsion.
A great circle on the unit sphere has curvature and
torsion given by
κCT = 1,

τCT = 0.

(33)

We estimate Z(tf ) as the limit value for which the curvature κTaT and torsion τTaT of the TaT separatrix at critical coupling give the same values as those in Eq. (33).
This value is given by Z ∗ (tf ) = cos(θ ∗ ) ≈ 0.132 684 (see
Appendix B). In order to obtain an analytical expression of the value of Z(tf ) recall that at critical coupling
the two stable ﬁxed points emerging
at /χ̃√= 0 have Z
√
coordinate given by Z± = ± 1 − (/χ̃ ) = 3/2, where
the last equality holds at critical coupling. It immediately
follows that
Z ∗ (tf ) ≤ 1 − Z+

(34)

is a tight bound.
√ We then approximate Z(tf ) as Z(tf ) =
1 − Z+ = 1 − 3/2, and substituting the latter into
Eq. (32), we obtain the timescale to peak spin squeezing as
[(
sq
(χ̃t)TaT = 2 ln

020314-9

√
]
)
√
√
2− 3
√√
( 2N + 2N − 1) .
2+
48 − 3
(35)

## PDF page 10

MUÑOZ-ARIAS, DEUTSCH, and POGGI

PRX QUANTUM 4, 020314 (2023)

2. Time scale to the first peak of the QFI
As discussed in Ref. [15], the ﬁrst peak of the QFI
occurs when the quantum uncertainty patch has been
stretched all the way to opposite ends of the separatrix.
Because of our choice of axis in Eq. (23) and our choice
of initial state, we know that at the ﬁrst peak of the QFI
the state is stretched along the z direction; thus, we consider the QFI associated with the generator Ĝ = Jˆz . This
conditions then tell us that the appropriate value of Z(tf )
for this timescale is given by Z(tf ) = 1. Substituting this
value into Eq. (32) we obtain
√
√
QFI
(36)
(χ̃ t)TaT = 2 ln[ 2N + 2N − 1] ≈ ln[8N ],
where the rightmost side of Eq. (36) holds in the limit of
N ≫ 1. We illustrate how well the expressions in Eqs. (35)
and (36) give the timescales to peak spin squeezing and
peak QFI, respectively, in Fig. 3(b).
3. Time to the first peak of the QFI: 2ACT versus TaT at
critical coupling
The timescales to the ﬁrst peak of the QFI in Eq. (17)
and in Eq. (36) look deceptively similar. In fact, in the
limit of large N ≫ 1, they only diﬀer by a constant factor,
whose origin is purely geometrical. In order to show this,
we assume that there is only a ﬁnite amount of twisting
strength that can be achieved in a given implementation,
and thus, if one is required to twist along two diﬀerent
axes, the strength of each twist will be halved compared
to that of a Hamiltonian that twists along a single axis.
Given that the Lyapunov exponents of the 2ACT saddle and the TaT saddle at critical coupling are CT
sd = χ̃
and TaT
|
=
χ̃
/2,
this
assumption
implies
that
the
expoCC
sd
TaT
nents are equal. In other words, we take CT
=

|
sd
sd CC =
sd , and measure timescales in terms of this exponent.
Then, in the limit of large N ≫ 1, we can write
QFI

(sd t)CT = 12 ln[4N ],

QFI

(sd t)TaT = 12 ln[8N ].

(37)

The diﬀerence between these two timescales is given by
QFI

QFI

(sd t)CT − (sd t)TaT =

ln(2)
.
2

(38)

The origin of this can be traced back to the additional
length that a point has to travel along the separatrix
between Z(0) and Z(tf ). At critical coupling, and in the
limit N → ∞, the length diﬀerence between the 2ACT and
TaT separatrices is given by
lTaT − lCT = E(i) −

π
ln(2)
≈ 0.3393 ≈
,
2
2

see then that the small diﬀerence in timescale in the limit of
large N ≫ 1 is only due to the additional length of the TaT
separatrix at critical coupling with respect to the length of
a great circle.
C. Local optimality of twisting and turning at critical
coupling as a quantum speed limit
In the previous section we showed that the Lyapunov
exponent of the saddle point of the TaT phase-space ﬂow
is maximum at critical coupling. This implies that in the
classical limit, a point traveling along the separatrix moves
with the maximum allowed velocity. This has direct consequences for the quantum dynamics, and it can be recast
as the saturation of a quantum speed limit [54,55]. To this
end, we use recent results derived in Ref. [56] for quantum
speed limits in Gaussian-preserving bosonic dynamics.
We are interested in a quantum speed limit constrained
to local dynamics, i.e., times such that the quantum state
remains mostly in the vicinity of the saddle point. The ﬁrst
step to show that at critical coupling the speed of evolution saturates the quantum speed limit is to write the
TaT Hamiltonian using the Holsten-Primakoﬀ approximation [57]. We deﬁne it with the ﬁxed component of angular
momentum relative to the position of the saddle point, i.e.,
the positive x direction, and ﬂuctuations
orthogo√ in the
√
nal directions, and thus Jˆx ≈ J , Jˆy ≈ J q̂, Jˆz ≈ J p̂,
where q̂, p̂ are two bosonic quadrature operators. After this
procedure the TaT Hamiltonian takes the form
ĤTaT = −

(40)

Details of this derivation are discussed in Appendix C.
Equation (40) can be written as
ĤTaT = 12 Z T GZ ,

(41)

where Z = (q̂, p̂) is a vector of quadratures and G is a 2 ×
2 matrix given by
(
)
1
0
G = −
.
(42)
0
1 − χ̃ / 
From this last expression we see that at critical coupling,
locally, the TaT Hamiltonian is a perfect squeezer, i.e.,
it is phase matched [58]. In this context we consider the
quantum speed limit as the maximum speed of evolution
allowed by this Hamiltonian. The quantum speed Vt is
deﬁned as the rate of change of the ﬁdelity between |ψt ⟩
and |ψt+dt ⟩,
F(ψt , ψt+dt ) = 1 − V2t dt2 ,

(39)

where E(i) is the complete elliptic integral of the second
kind. We give the details of this result in Appendix B. We

 2 1
q̂ + (χ̃ − )p̂ 2 ,
2
2

(43)

and for pure states, F(ψ1 , ψ2 ) = |⟨ψ1 |ψ2 ⟩|2 . Using results
from Ref. [56], we can compute the speed for a generic

020314-10

## PDF page 11

PHASE-SPACE GEOMETRY AND OPTIMAL STATE PREPARATION. . .

PRX QUANTUM 4, 020314 (2023)

-

FIG. 4. Behavior of the ratio in Eq. (46) between the actual
quantum speed of the initial state and the maximum possible
one, as a function of χ̃ / , for diﬀerent values of the squeezing r. Note how the quantum speed limit is saturated at critical
coupling, independently of the amount of squeezing.

FIG. 5. Schematic of the diﬀerent parameter regimes of the
TaT (LMG) Hamiltonian of Eq. (23) as a function of /χ̃ .
Depicted are aspects related to metrological state preparation,
dynamical quantum phase transitions, ground-state phase quantum phase transitions, and classical phase-space structures.

Gaussian state with a ﬁxed level of squeezing r (see
Appendix C for details). With these constraints, the maximum speed of evolution given the TaT Hamiltonian is

instructive to recall that the separatrix also plays a major
role in the descriptions of equilibrium and nonequilibrium
phases in collective spin models. The case of the TaT
Hamiltonian, Eq. (23), is paradigmatic in this sense, since
it also corresponds to a special case of the LMG model,
which has been extensively investigated in the context of
quantum phase transitions [44–48,50,59]. In fact, there is a
one-to-one correspondence between the phase diagram of
the LMG and the regimes of optimal probe state preparation with TaT dynamics, which are schematically depicted
in Fig. 5 and analyzed in the following.
We can deﬁne an equilibrium order parameter describing the character of the ground state as

V2max (r) =

χ̃ 2 1
+ χ̃ |χ̃ − 2|r.
8
4

(44)

On the other hand, the speed of evolution for our initial
state is given by
V20 = ⟨

2

ĤTaT ⟩0 =

χ̃ 2
.
8

(45)

In order to explore if there is a parameter regime where the
quantum speed limit is saturated, we study the ratio
χ̃ 2

V20
2
= 2 2
.
2
Vmax (r)
χ̃ / + (2χ̃ / )|χ̃ /  − 2|r

(46)

This expression has a maximum equal to one at χ̃/ = 2,
i.e., critical coupling. Notably, this fact is independent of
the value of the squeezing r, which we illustrate in Fig. 4.
D. Quantum metrology and phase diagrams in
many-body systems: twisting and turning and the
Lipkin-Meshkov-Glick model
Throughout this work, we have discussed the prominent role played by the classical phase-space structures of
collective spin models in the preparation of probe states
for quantum metrology. In particular, we have shown that
the geometric and dynamical properties of the separatrix
dictate the parameter regimes leading to the exponential
increase of spin squeezing and QFI. In this context it is

ZGS =

1
⟨φGS | Jˆz |φGS ⟩
J

(equilibrium),

(47)

where |φGS ⟩ is the ground state of the Hamiltonian in
Eq. (23). Similarly, we deﬁne a nonequilibrium or dynamical order parameter
∫
1 T 1
Z ∞ = lim
dt ⟨ψ(t)| Jˆz |ψ(t)⟩ (dynamical),
T→∞ T 0
J
(48)
where |ψ(t)⟩ = e−iĤ t |ψ(0)⟩ and the initial state is the
spin coherent state |ψ(0)⟩ = |↑⟩⊗N . As discussed previously, analysis of the TaT (LMG) model classical ﬂow
reveals a bifurcation at /χ̃ = 1. For  < χ̃, all trajectories revolve around the stable ﬁxed points at (±1, 0, 0).
As a result, in this regime we have both ZGS = 0 and
Z ∞ = 0. At the bifurcation (where the separatrix is born)
the ground state of the system, identiﬁed with trajectories of minimal classical energy, begins shifting towards

020314-11

## PDF page 12

MUÑOZ-ARIAS, DEUTSCH, and POGGI

PRX QUANTUM 4, 020314 (2023)

the Z axis, and ZGS > 0. This then corresponds to the
ground-state critical point. However, the dynamical order
parameter still vanishes, Z ∞ = 0, since the initial condition still revolves around the x axis. As we decrease the
value of the external ﬁeld and  < χ̃ < 1, the stable ﬁxed
points get closer to the z axis and the separatrix grows bigger. Eventually, this trajectory will pass through (0, 0, 1).
At this stage, the initial condition in Eq. (48) gets trapped
inside the separatrix, and rotates around the stable ﬁxed
point, leading to Z ∞ > 0. This is the dynamical critical
point, /χ̃ = 12 , which coincides with the critical coupling
regime discussed previously.
Furthermore, the separatrix line has been recognized
as the classical origin of a certain type of excited state
quantum phase transition (ESQPT) [60,61]. In particular,
for a system whose thermodynamic limit is described by
a single degree of freedom, this ESQPT is given as a
logarithmic divergence of the density of states as a consequence of the clustering of eigenstates whose energy is
inside a small energy window centered at the separatrix
energy. As such, as we sweep /χ̃ towards zero and, for
/χ̃ < 1, diﬀerent excited states undergo ESQPT as their
energy becomes equal to the energy of the separatrix. Since
this type of quantum phase transition refers to macroscopic
changes in the structure of excited states, its consequences
are observable in the dynamics of appropriately chosen initial states. In fact, there is a direct correspondence between
ESQPT in a group of excited states and the type of dynamical quantum phase transition (DQPT) discussed above
(see, for instance, Refs. [62,63]) that has implications for
quantum enhanced metrology [64].
Finally, the connection depicted in Fig. 5 goes beyond
just the TaT (LMG) model, and its applicable to generic
collective spin models. In the next section we introduce
and study two additional examples.
V. BEYOND HAMILTONIANS WITH TWO-BODY
INTERACTIONS: p-ORDER TWISTING
So far, we have considered the paradigmatic examples
of 2ACT and TaT to analyze the preparation of metrologically useful states of collective spins. However, the tools
we have employed in their analysis are agnostic to the speciﬁc model under study, and the geometry of phase-space
ﬂows and separatrices allows us to study any collective
spin Hamiltonian. In this section we turn our attention
to generalizations of the 2ACT and TaT models studied
before, to account for higher-order many-body twisting
operations. In particular, we consider interactions such as
p
Jˆα associated with a p-body collective coupling between
p spin- 12 particles.

(p)

ĤCT = χ (Jˆpx − Jˆpy ),

where, for convenience, we have rotated the axis so that the
twisting directions correspond with x and y. Proceeding as
in Sec. III, we can derive the equations of motion for the
classical ﬂow, which read
dX
= −χ̃Yp−1 Z,
dt
dY
= −χ̃X p−1 Z,
dt
dZ
= χ̃(X p−1 Y + Yp−1 X ).
dt

(50a)
(50b)
(50c)

The ﬁxed points of the ﬂow can be readily computed from
Eqs. (50) and turn out to be independent of p and located,
as before, on the north and south poles (0, 0, ±1) and along
the twisting directions (±1, 0, 0) and (0, ±1, 0). The stability analysis (see Appendix D) reveals that the equatorial
ﬁxed points are stable for all values of p. For the polar
ones, however, we ﬁnd that the eigenvalues of the Jacobi
matrix M are ±1 (leading to saddle points) only for p = 2.
For p > 2, we ﬁnd that M = 0 when evaluated at these
ﬁxed points and thus the standard linear stability analysis
is insuﬃcient to classify the local motion of the system.
We can still study the behavior in this regime by considering the dynamics near Z ≃ 1, and looking at the motion
along the branches x = y = v and u = x = −y, for which
we obtain
dv
= −χ̃ v p−1
dt

and

du
= −χ̃(−1)p−1 up−1 .
dt

(51)

We focus on the case of p even, for which the local motion
clearly shows saddle-point-like behavior, with a stable (v)
and an unstable (u) branch. For p = 2, we get exponential
motion up=2 (t) ∼ eχ̃ t , as described in Sec. III, while for
p > 2, we obtain upon direct integration
(
up (t) =

)−1/(p−2)
−
(p
−
2)
χ̃
t
,
p−2
u0
1

(52)

which grows more slowly. Thus, while the p-2ACT Hamiltonian will produce spin squeezing, it will not do so
exponentially in time unless p = 2.
B. Twisting and turning with a p-spin
Consider now a generalization of the TaT Hamiltonian,
which we refer to as pTaT, given by
ĤpTaT = Jˆx + χ Jˆpz

A. Two-axis countertwisting with a p-order twist
Consider a generalization of the Hamiltonian in Eq. (6)
to include p-order twisting (p ≥ 2 throughout),

(49)

(53)

with  the turning rate and χ the p-twisting strength. The
Hamiltonian in Eq. (53) is an unnormalized version of the

020314-12

## PDF page 13

PHASE-SPACE GEOMETRY AND OPTIMAL STATE PREPARATION. . .
p-spin models, largely studied in the context of quantum
annealing [22,65,66], and equilibrium and nonequilibrium
quantum phase transitions [67–70].
Our ﬁrst goal is to explore whether a notion of “critical coupling” exists for the family of pTaT Hamiltonians.
From our discussion of 2TaT in Sec. IV we saw that critical
coupling is given by the parameter regime at which conditions 1–4 in Sec. IV A are satisﬁed simultaneously. In this
subsection we study each of these conditions for the whole
family of pTaT Hamiltonians. We see that such a strong
notion of critical coupling cannot be extended to the other
pTaT models with p > 2. However, a less stringent notion
can still be satisﬁed by at least one more pTaT Hamiltonian: we show that the only other case for which more
than one of the conditions can be satisﬁed simultaneously
is p = 3.
Condition 1 deﬁnes critical coupling as the parameter
choice such that opposite ends of the separatrix are diametrically opposed. This statement holds only for the pTaT
with even values of p. This can be seen in the following way. Recall that pTaT Hamiltonians with even p have
a parity symmetry, given by the operator ˆ
 = eiπ Jˆx and
ˆ = 0. Thus, pairs of points that are diametrically
[ĤpTaT , ]
opposed can have the same energy, as, for instance, the
north and south poles with respect to the twisting axis, represented by the two stretched states |J , ±J ⟩, with mean
energy ⟨ĤpTaT ⟩ = χ̃/pJ . Given that the separatrix is an
isoenergetic curve, the classical ﬂow associated with the
pTaT Hamiltonian for even values of p admits a regime of
parameters where the separatrix has points diametrically
opposed. On the contrary, the lack of parity symmetry for
the models with odd values of p rules out this possibility.
We now turn to condition 3. We ﬁnd that there is no
parameter regime for which the separatrix branches are
orthogonal in the vicinity of the saddle point, for any pTaT
with p > 2. This is formalized in the following theorem,
whose proof we give in Appendix D.
Theorem 1 (Absence of local optimality in pTaT). Given
the real-valued control parameter /χ̃ > 0, there is no
value of this parameter for which the pTaT dynamics, with
p > 2, is locally optimal.
Let us now consider the other two conditions. Condition
4 demands that the energy wells on both sides of the saddle
point have equal depth [71]. This property can be investigated using the classical energy E(X) = ⟨ĤpTaT ⟩/J , where
the expectation value is taken in a spin coherent state, in
the limit J → ∞. All the pTaT models have a parameter regime where the classical energy is a single well, and
a parameter regime where the classical energy has a double (p = 2, p > 2, and odd) or triple well structure (p > 2
and even). These diﬀerent regimes are separated by bifurcation points and ground-state critical points (for a detailed
discussion, see Refs. [22,69]). For 2TaT, parity symmetry

PRX QUANTUM 4, 020314 (2023)

guarantees that the individual wells of the double well have
equal depth for all parameter regimes. For pTaT with odd
values of p, the condition of having wells with the same
depth deﬁnes the ground-state critical point; as such, this
condition is satisﬁed only at one speciﬁc parameter value,
χ̃/|GS . For pTaT with p > 2 and even, parity symmetry guarantees that the two outermost wells have the same
depth for all parameter regimes. However, these lie at the
right and left sides of two diﬀerent saddle points. Similar
to the case of odd values of p, the outer and central wells
will have the same depth at a single parameter value, also
given by χ̃ / |GS . An immediate consequence is that, for
pTaT with p > 2 and even, conditions 1 and 4 in Sec. IV A
are satisﬁed at two completely diﬀerent parameter regimes,
and thus they cannot be considered to deﬁne a notion of
critical coupling.
The previous analysis implies that, for pTaT with p > 2,
there is no parameter regime for which at least three of
the conditions in Sec. IV A are satisﬁed simultaneously. In
fact, we will see that, for the models with p > 2 and even,
all four conditions occur at diﬀerent parameter values, and
thus a notion of critical coupling cannot be introduced. We
are then left with the question of whether, for models with
p > 2 and odd, conditions 2 and 4 in Sec. IV A can be
satisﬁed simultaneously. In the following we show that this
is true only for p = 3, and thus this is the only other pTaT
Hamiltonian admitting a notion of critical coupling.
In order to show this, we need explicit expressions
for χ̃/|GS , the ground-state critical point, and χ̃/|LE ,
the maximum of the saddle point Lyapunov exponent,
both as a function of p. An explicit computation of the
ground-state critical point for this family of models was
presented in Appendix B of Ref. [72]. Here, we only mention the explicit expression. The ground-state critical point
is given by
√
ZGS =

p(p − 2)
,
(p − 1)2

∣
χ̃ ∣∣
(p − 1)p−1
√
=
, (54)
 ∣GS
(p(p − 2))p−2

where ZGS is the z coordinate of the new global minimum
of the classical energy density. An explicit expression for
the maximum of the saddle point Lyapunov exponent is
given by
ZLE =

p −2
,
p −1

∣
χ̃ ∣∣
(p − 1)p−1
√
=
,
 ∣LE (p − 2)p−2 (p − 1)2 − (p − 2)2

(55a)
(55b)

where ZLE is the z coordinate of the saddle point for the
parameter values at which the Lyapunov exponent is maximum. We give the explicit derivations of Eqs. (55) in
Appendix D.

020314-13

## PDF page 14

MUÑOZ-ARIAS, DEUTSCH, and POGGI
The forms of Eqs. (54) and (55) imply that
∣
∣
χ̃ ∣∣
χ̃ ∣∣
≥
 ∣GS  ∣LE

PRX QUANTUM 4, 020314 (2023)
(a)

(56)

with equality only when p = 3. Hence, the only other
pTaT Hamiltonian that admits a notion of critical coupling, similar to that of TaT, is 3TaT, with critical coupling
deﬁned as the ground-state critical point.
Before closing this subsection let us mention that the
diﬀerent coupling regimes of the pTaT family, deﬁning
the bifurcation (spinodal) point, ground-state critical point,
dynamical critical point, and maximum of the saddle point
Lyapunov exponent, establish a classiﬁcation of this family of models. In fact, one encounters four diﬀerent types of
inequality chains. If p = 2, these parameter values satisfy
∣
∣
∣
∣
χ̃ ∣∣
χ̃ ∣∣
χ̃ ∣∣
χ̃ ∣∣
=
<
=
,
(57)
 ∣spino  ∣GS  ∣DQPT  ∣LE

(b)

(c)

where (χ̃ / )|DQPT indicates the critical point of the
dynamical quantum phase transition. If p = 3, these
parameter values satisfy
∣
∣
∣
∣
χ̃ ∣∣
χ̃ ∣∣
χ̃ ∣∣
χ̃ ∣∣
<
=
<
.
(58)
 ∣spino  ∣GS  ∣LE  ∣DQPT
If p = 4, these parameter values satisfy
∣
∣
∣
∣
χ̃ ∣∣
χ̃ ∣∣
χ̃ ∣∣
χ̃ ∣∣
<
<
<
.
 ∣spino  ∣LE  ∣GS  ∣DQPT

(59)

For all other values of p > 4, these parameter values
satisfy
∣
∣
∣
∣
χ̃ ∣∣
χ̃ ∣∣
χ̃ ∣∣
χ̃ ∣∣
<
<
<
.
(60)
 ∣spino  ∣LE  ∣DQPT  ∣GS
We gave explicit expressions for the spinodal, groundstate critical, and dynamical critical points of this family
of models in Appendix B of Ref. [72].
C. Time scale to the ﬁrst peak of the QFI with 3TaT
Our second goal in this section is to give an explicit
expression for the timescale to the ﬁrst peak of the QFI,
for the dynamics with 3TaT. The fact that at critical coupling the semiclassical energy is a double well with wells
of equal depth indicates that one can prepare a “catlike”
state where the peaks of each lobe lie at the bottom of each
of the wells, and the timescale to this state is estimated
similarly to that of TaT in Sec. IV. We show the separatrix
of 3TaT at critical coupling in Fig. 6(a).
Given that the position of the saddle at critical coupling is Zsd = 12 , we consider an initial SCS centered at

FIG. 6. (a) Phase portrait of the phase-space ﬂow of the 3TaT
Hamiltonian at critical coupling. The separatrix is shown in solid
red. (b) Metrological gain based on the QFI (solid red), at critical
coupling, for an initial SCS centered at the position of the saddle
point. The dashed line shows our result for the time to the ﬁrst
peak. Results are for a system with N = 1024. (c) Time scale to
the ﬁrst peak of the QFI with 3TaT at critical coupling, contrasted
against the Ehrenfest time.

the saddle, that is, |θ0 , ϕ0 ⟩ = |π/3, 0⟩. Since the separatrix is extended in the z direction, the catlike state being
prepared will be extend in this direction as well. We then
consider Ĝ = Jˆz , and will look at the QFI FQ [|ψ⟩, Jˆz ]. We
then approximate the desired time scale as the traveling
time of a point starting at the border of the SCS uncertainty patch and moving, along the separatrix, all the way
to its end. This procedure can be tracked analytically, but
we include details in Appendix D. The initial point Z(0)
turns out to be
Z(0) =

1
1
,
+ √
√
2 2 (1 + [cos−1 ( 3/5)]−2 /3)N

(61)

and the end point is given by one of the two points at the
intersection of the great circle in the x-z plane and the separatrix, which has the same energy as the saddle point.
This leads to Z(tf ) ≈ 0.96. The desired timescale is then

020314-14

## PDF page 15

PHASE-SPACE GEOMETRY AND OPTIMAL STATE PREPARATION. . .
given by
QFI

(χ̃ t)3TaT =

∫ Z(tf )
Z(0)

12dZ
√
.
27(1 − Z 2 ) − (5 − 4Z 3 )2

(62)

We compare this timescale with the respective Ehrenfest
time in Fig. 6(c). In this case the saddle point Lyapunov
exponent at critical coupling is given by
∣

∣ =
3TaT
sd
CC

√

7
χ̃ ,
4

(63)

and thus, following from Eq. (21), the Ehrenfest time for
3TaT at critical coupling is given by
2
(χ̃ t)Erfst
3TaT = √ ln[N ].
7

(64)

The time to the ﬁrst peak of the QFI and the Ehrenfest time
for the 3TAT at critical coupling are compared in Fig. 6(c).
QFI
We immediately see that (χ̃ t)3TAT > (χ̃ t)Erfst
3TaT for all values
of N . As such, one would have expected a semiclassical
analysis to give inaccurate predictions. However, we see
that this is not the case, pointing at a deeper connection
between the geometry of separatrices and the generation
of nonclassical states.
VI. SUMMARY AND OUTLOOK
In this work we have studied the preparation of nonclassical states for use in quantum metrology with collective
spin systems based on the geometry of classical phase
space. This picture is completely general for states generated by an arbitrary collective spin Hamiltonian. Using
this, we have framed the quantum dynamics problem of
state preparation as a problem involving the geometry of
curves on the surface of the unit sphere. We have established a notion of local optimality for state preparation,
which is given by the existence of a saddle point together
with the orthogonality of separatrix branches in its vicinity, giving a geometrical interpretation to a pure squeezing
Hamiltonian. Correspondingly, this framework also leads
to a natural notion of global optimality, given by separatrix branches that are aligned with geodesics on the
phase space, which, for collective spins, correspond to
great circles on the unit sphere.
With these geometric tools in hand, we analyzed two
paradigmatic examples of collective spin Hamiltonians
that generate metrologically relevant quantum states at
an exponential rate: the two-axis countertwisting and the
twisting-and-turning Hamiltonians. We gave a geometrical
interpretation to the parameter regime known as “critical
coupling” in the TaT Hamiltonian composed of four main
properties, and proved the local optimality of this parameter regime. Furthermore, we extended the TaT Hamiltonian

PRX QUANTUM 4, 020314 (2023)

to a large family of models, the p-twisting-and-turning
Hamiltonians, by allowing ourselves to consider arbitrary
p-body collective interaction terms. We proved a no-go
theorem for the local optimality of pTaT dynamics with
p > 2, and showed that the only model that still admits a
notion of critical coupling involving more than one of its
geometric properties is 3TaT.
It is thus the geometry of the classical separatrix that
controls these exponentially short time scales. We focused
on initial spin coherent states centered at the saddle points,
but our conclusions are general, in the sense that any initial spin coherent state with considerable overlap with the
separatrix line will have an exponentially short evolution
time to a metrologically relevant state. The physical reason
behind this fact can be traced back to the structure of the
eigenstates that in the classical limit correspond to trajectories within a small neighborhood of the separatrix [73].
It is known that these states live at the border of the principle of correspondence and behave as WKB states [37],
thus leading to a dynamics of wave packed spreading that
inherits many of the characteristics of the underlying classical dynamics. Furthermore, it was noted that these states
lead to “saddle point scrambling” [74,75], a process where
out-of-time-order correlators grow exponentially but the
system does not equilibrate, pointing at an interesting connection between this type of scrambling and metrological
advantage.
The analysis done here is not only restricted to the standard approach to local quantum metrology involving state
preparation, sensing, and then measurement, but can, in
fact, be readily applied to other quantum metrology protocols. For example, consider the spin ampliﬁcation protocol
studied in Ref. [76]. The key mechanism behind the ampliﬁcation procedure in this protocol can be understood by
considering the phase-space ﬂow associated with collective dissipative dynamics, that
√is, by Lindbladian dynamics
with the jump operator L̂ =  Jˆ− . The motion described
by its phase-space ﬂow is that of an overdamped pendulum (see, for instance, Ref. [77]), given by the classical
equations
dθ
= k sin(θ),
dt

dφ
=0
dt

(65)

with k some positive number and (θ , φ) the two angular
coordinates on the unit sphere. As discussed in Ref. [76],
one has k = . Note that canonical equations of motion
for the 2ACT in Eqs. (A8) map exactly to those in Eq. (65)
when we take k = χ̃ , use angular variables, and constrain
to the separatrices. In other words, the separatrices of the
2ACT are spin ampliﬁers, and the protocol in Ref. [76] can
be executed in a fully coherent manner by replacing the
collective dissipation with the 2ACT dynamics. A more
detailed study of this latter fact is the object of ongoing
work.

020314-15

## PDF page 16

MUÑOZ-ARIAS, DEUTSCH, and POGGI

PRX QUANTUM 4, 020314 (2023)

Beyond its application to spin ampliﬁcation, the present
analysis can be used in other types of quantum metrology
protocols, where one expects the separatrix line to play a
role. For instance, in certain tasks of critical metrology, or
in situations where one is interested in reﬁning the knowledge about some Hamiltonian parameter. In the latter case,
the best strategy will always be to choose an initial spin
coherent state placed on top of the separatrix. Furthermore, some types of dynamical sensors might be described
with the tools presented in this work, as for instance Floquet time crystals [72], or chaotic sensors [25]. There, the
idea of a separatrix generalizes to that of a classical border between regions of distinct macroscopic motion, and
spin coherent states placed at these borders are known to
provide the best strategy [25].
ACKNOWLEDGMENTS
The authors are grateful to Tyler J. Volkoﬀ and Jason
Twamley for engaging discussions. This work is supported
by NSF Grant No. PHY-1606989 and the Quantum Leap
Challenge Institutes program (Grant No. 2016244). This
material is based upon work supported by the U.S. Department of Energy, Oﬃce of Science, National Quantum
Information Science Research Centers, Quantum Systems
Accelerator (QSA). In the last stages of the manuscript
conception, M.H.M.-A. was supported in part via funding from NSERC, the Canada First Research Excellence
Fund, and the Ministère de l’Économie et de l’Innovation
du Québec.
APPENDIX A: DERIVATIONS OF SOME RESULTS
WITH THE TWO-AXIS COUNTERTWISTING
HAMILTONIAN
1. Derivation of phase-space ﬂow, ﬁxed points, and
their stability
In order to compute the phase-space ﬂow, we need to
introduce a rescaled version of Eq. (7), so that its energy
will be extensive in the thermodynamic limit. This can
be achieved by introducing the rescaled countertwisting
strength χ = χ̃/N ; then
ĤCT =

χ̃
(Jˆx Jˆy + Jˆy Jˆx ).
N

(A1)

Using the Hamiltonian in Eq. (A1), we can write the
Heisenberg equations of motion, dJˆγ /dt = i[Ĥ , Jˆγ ] with
γ = x, y, z, for the components of the collective spin. They
are
χ̃
dJˆx
= (Jˆx Jˆz + Jˆz Jˆx ),
dt
N
ˆ
dJ y
χ̃
= − (Jˆy Jˆz + Jˆz Jˆy ),
dt
N

(A2a)
(A2b)

2χ̃
dJˆz
= − (Jˆ2x − Jˆ2y ).
dt
N

(A2c)

In the thermodynamic limit, J → ∞, Eqs. (A2) lead
to the phase-space ﬂow of the classical variables X =
⟨Ĵ⟩/J , which after neglecting correlations ⟨ÂB̂⟩ = ⟨Â⟩⟨B̂⟩,
is given by
dX
= χ̃XZ,
dt
dY
= −χ̃YZ,
dt
dZ
= −χ̃(X 2 − Y2 ).
dt

(A3a)
(A3b)
(A3c)

Fixed points of a phase-space ﬂow are those initial conditions with a trivial evolution, that is, solutions of dX/dt =
0. The phase-space ﬂow in Eqs. (8) has six diﬀerent ﬁxed
points given by
(X , Y, Z) = (0, 0, ±1),
)
(
1
1
(X , Y, Z) = √ , ∓ √ , 0 ,
2
2
(
)
1
1
(X , Y, Z) = − √ , ± √ , 0 .
2
2

(A4a)
(A4b)
(A4c)

Thus, the phase-space ﬂow has ﬁxed points in the north
and south poles of the unit sphere, and in the poles of each
of the twisting axes.
The stability of ﬁxed points can be analyzed using the
eigenvalues of the Jacobi matrix, M[X] = (∂/∂X)(dX/dt),
evaluated at the ﬁxed point. For the phase-space ﬂow in
Eqs. (8), this matrix is given by
⎛

χ̃ Z
⎝
0
M[X] =
−4χ̃ X

0
−χ̃ Z
4χ̃ Y

⎞
χ̃X
−χ̃Y⎠ .
0

(A5)

When evaluated at the ﬁxed point (X , Y, Z) = (0, 0, ±1),
Eq. (A5) is diagonal, with the diagonal equal to
Diag[M] = (±χ̃ , ∓χ̃, 0). Thus, the two eigenvalues are
real and equal to M± = ±χ̃. This implies that the ﬁxed
point is a saddle point, and that the principal directions of
the separatrix emerging from it are orthogonal and aligned
with the x and y axes, respectively. In other words, they
deﬁne great circles in the x-z and y-z planes, respectively.
Furthermore, we know that in the vicinity of the saddle
point, an initial condition on one of the separatrix branches
evolves according to dP± /dt = ±χ̃ P± , where P± = X , Y.
The other four ﬁxed points in Eqs. (A4) are stable
centers. This can be easily veriﬁed by looking at the eigenvalues of the Jacobi matrix evaluated at the ﬁxed points,
which are given by M = ±i2χ̃ .

020314-16

## PDF page 17

PHASE-SPACE GEOMETRY AND OPTIMAL STATE PREPARATION. . .

√
√
]
(1 − Z(tf ))( N + N − 1)
√
,
χ̃ t = ln
1 − Z 2 (tf )
[

2. Classical energy and the separatrix
Using the form of the 2ACT Hamiltonian in Eq. (A1),
we can write down an expression for the classical energy
by taking the thermodynamic limit of ⟨ĤCT ⟩/J , then,
after neglecting correlation and in terms of the classical
variables X, the classical energy density reads
E(X , Y; χ̃ ) =

⟨ĤCT ⟩
= χ̃ XY.
J

(A6)

Introducing spherical coordinates (X , Y, Z) = (sin(θ)
cos(φ), sin(θ) sin(φ), cos θ) and noting that the variables
φ and Z are classical conjugate variables playing the role
of “position” and “momentum,” respectively, we can write
Eq. (A6) as
E(Z, φ; χ̃ ) =

χ̃
(1 − Z 2 ) sin(2φ).
2

(A7)

We can use the expression of the classical energy in
Eq. (A7) to compute an equation for the classical separatrix and, subsequently, the time required for points to travel
along sections of this curve.
First of all, recall that the separatrix connects the two
saddles at (0, 0, ±1); thus, conservation of energy says that
any point along the curve has energy Esepa = 0. Thus, the
separatrix equation is E(Z, φ; χ̃ ) = 0; this is true if Z =
±1, and also for the range of allowed values of φ ∈ [0, 2π ].
Then the separatrix is deﬁned by all the pairs (Z, φ) with
φ = 0, π/2, deﬁning the two great circles in the x-z plane
and the y-z plane, respectively.
The equations of motion for the classical conjugate
variables are given by
dZ
∂E
=−
= −χ̃(1 − Z 2 ) cos(2φ),
dt
∂φ
∂E
dφ
=
= −χ̃Z sin(2φ).
dt
∂Z

(A8a)
(A8b)

For the saddle at (X , Y, Z) = (0, 0, 1), the x direction is
the unstable manifold of the separatrix, thus, motion of
points along the separatrix satisfy φ(t) = 0 for all times.
Constrained to the separatrix, we then have
dZ
= −χ̃(1 − Z 2 ),
dt

∫ Z(tf )
Z(0)

dZ
.
1 − Z2

(A11)

which is the same as Eq. (13) in the main text.
3. Explicit expressions for the spin-squeezing
parameter and quantum Fisher information
Our starting point in this section is the fact that the solution to the integral in Eq. (12) allows us to write an explicit
expression for Z(t). It is given by
Z(t) =

− sinh(χ̃ t) + Z(0) cosh(χ̃ t)
Z(0) − tanh(χ̃ t)
=
.
cosh(χ̃ t) − Z(0) sinh(χ̃ t)
1 − Z(0) tanh(χ̃ t)
(A12)

With this expression at hand we can go forward and
write explicit expressions for the squeezing parameter and
quantum Fisher information.
a. Explicit expression for the squeezing parameter
Let us write Eq. (15) of the main text in terms of Z
instead of the polar angle θ . It is given by
2
ξCT
(Z) =

1
NZ 2 (t)(1 − Z 2 (t))

.

(A13)

Then, by substituting Eq. (A12) into Eq. (A13), we obtain
2
=
ξCT

(1 − Z(0) tanh(χ̃ t))4
,
N (1 − Z 2 (0))(1 − tanh2 (χ̃ t))(Z(0) − tanh(χ̃ t))2
(A14)

recalling
that our initial state of interest provides Z(0) =
√
1 − 1/N , and thus N (1 − Z 2 (0)) = 1. Substituting these
into the last expression we obtain the explicit form of
the squeezing parameter under evolution with the two-axis
countertwisting:
2
ξCT
=

√
√
[ N − N − 1 tanh(χ̃ t)]4
.
√
√
N (1 − tanh(χ̃ t))[ N − 1 − N tanh(χ̃ t)]2
(A15)

b. Explicit expression for the quantum Fisher
information

(A9)

Recall that the metrological gain based on the QFI is
deﬁned as

and the desired timescale is given by
χ̃ t = −

PRX QUANTUM 4, 020314 (2023)

ζ2 =

(A10)

After
solving this integral, and recalling that Z(0) =
√
1 − 1/N , as explained in the main text, we obtain

N
.
FQ

(A16)

Furthermore, recall that the variance in the x direction goes
as Jx = J sin(θ). Thus, after taking Jˆx as the generator,

020314-17

## PDF page 18

MUÑOZ-ARIAS, DEUTSCH, and POGGI

PRX QUANTUM 4, 020314 (2023)

we can write the QFI as

For the family of Yurke states,

FQ = N 2 sin2 (θ ) = N 2 (1 − Z 2 (t));

(A17)

after substituting Eq. (A12) into Eq. (A17) we obtain
FQ = N 2

(1 − tanh2 (χ̃ t))(1 − Z(0)2 )
,
(1 − Z(0) tanh(χ̃ t))2

(A18)

√
recalling that in our setting Z(0) = 1 − 1/N . Then we
can write
1 − tanh2 (χ̃ )
FQ = N 2 √
.
√
( N − N − 1 tanh(χ̃ t))2

(A19)

This last expression allows us to write the classical estimate for the metrological gain based on the QFI as
ζ 2 (t)CT =

√
√
( N − N − 1 tanh(χ̃ t))2
N (1 − tanh2 (χ̃))

.

(A20)

In this section we illustrate how the timescales for the
BWS, EWSS, and YUS are computed using the traveling
time for motion of points along sections of the separatrix.
This calculation is based on the values of the variances
of the states of interest. In order to obtain them, we need
explicit expressions for these states. Let us start with the
Berry-Wiseman state. Initially introduced by Berry and
Wiseman [35], as the optimal state for phase encoding
in an interferometric setting, it was latter considered by
Combes and Wiseman [36] as the optimal state for phase
estimation. It is given by

J
∑

N + 1 M =−J

|J , M ⟩

with variance equal to ( Jz )2 = J (J + 1)/3.

J
[(J + 1)(2 − sin2 (α)) − 2 sin2 (α)]. (A24)
4

We note, however, that only Yurke states with relatively
small values of α are prepared by the 2ACT dynamics.
Now that we know the structures of the states in the
Dicke basis and their respective variance values, let us
illustrate how the timescales are calculated.

In the limit of large N ≫ 1, the variance of the
2
state goes
approximately as 0.13J
√
√ ; thus, the two val>
<
ues J = J / 8 and J = J / 7 are good lower and
upper bounds, respectively. From the above observation
we have
1
sin(θ > ) = √ ,
8

1
sin(θ < ) = √ .
7

(A25)

Hence, we get the values of Z(tf ) for the timescale to a
BWS as
√
>

Z (tf ) =

(A21)

with variance, for N ≫ 1, equal to ( Jz )2 ≈ 0.13J 2 .
The EWSS is the pure state version of the maximally
mixed state, that is, a superposition of all Dicke states with
equal weight:
1

( Jz )2 =

7
,
8

√
<

Z (tf ) =

6
,
7

(A26)

giving the following lower and upper bounds for the
timescale to the peak of the ﬁdelity to the BWS state:

[

]
1
Mπ
|BW⟩ = √
cos
|J , M ⟩
N +2
1 + N /2 M =−J

|EWSS⟩ = √

with variance equal to

a. Timescale to the Berry-Wiseman state

4. Some other quantum states relevant for metrology
accessible with two-axis countertwisting

J
∑

sin(α)
sin(α)
|Yu⟩ = √ |J , 1⟩ + cos(α)|J , 0⟩ + √ |J , −1⟩
2
2
(A23)

(A22)

√
√ √
√
7)( N + N − 1)],
(χ̃ t)>
CT = ln[( 8 −
√ √
√
√
(χ̃ t)<
6)( N + N − 1)].
CT = ln[( 7 −

(A27a)
(A27b)

These bounds are the same as those in Eqs. (18) in the main
text.
b. Timescale to the equally weighted superposition
state
√
The variance of this state is J = J (J + 1)/3. Thus,
at the time at which the ﬁdelity to this state peaks, θ is

020314-18

## PDF page 19

PHASE-SPACE GEOMETRY AND OPTIMAL STATE PREPARATION. . .

by introducing the normalized twisting strength χ = χ̃/N ;
we write

given by
√
1
1
sin(θ ) = √ 1 + ,
J
3

ĤTaT = Jˆx +

(A28)

dJˆx
χ̃
= − (Jˆy Jˆz + Jˆz Jˆy ),
dt
N
ˆ
dJ y
χ̃
= −Jˆz + (Jˆx Jˆz + Jˆz Jˆx ),
dt
N
ˆ
dJ z
= Jˆy .
dt

(A29)

From here, it is easy to get the timescale
[( √

√
)
]
√
3 − 2 − 2/N √
( N + N − 1)
√
1 + 2/N
√ √
√
√
= ln[( 3 − 2)( N + N − 1)],
(A30)

= ln
(χ̃ t)EWSS
CT

which is the same as Eq. (19) in the main text.

dX
= −χ̃ YZ,
dt
dY
= −Z + χ̃ XZ,
dt
dZ
= Y.
dt

Using the expression for the variance, we get

(A31)

from which we obtain
√

Z(tf ) = cos(θ) =

(B1)

1
4 − 6 sin2 (α)
,
2 + sin2 (α) −
2
N
(A32)

leading to a timescale to Yurke states of
√
)
2 + sin2 (α) − [4 − 6 sin2 (α)]/N
2
−
YUS
√
(χ̃ t)CT = ln
2 − sin2 (α) + [4 − 6 sin2 (α)]/N
)]
(√
√
N + N −1 ,
(A33)
×
[(

where Eq. (20) is recovered from Eq. (A33) in the limit
N → ∞.
APPENDIX B: DERIVATION OF SOME RESULTS
WITH THE TWISTING-AND-TURNING
HAMILTONIAN AT CRITICAL COUPLING
1. Derivation of the phase-space ﬂow, ﬁxed points, and
their stability
In order to construct the phase-space ﬂow in the thermodynamic limit, we need to rescale the TaT Hamiltonian in
Eq. (23) so that in the thermodynamic limit, we can guarantee the extensivity of the energy density. This is achieved

(B2a)
(B2b)
(B2c)

In the thermodynamic limit, J → ∞, Eqs. (B2) lead
to the phase-space ﬂow of the classical variables X =
⟨Ĵ⟩/J , which after neglecting correlations ⟨ÂB̂⟩ = ⟨Â⟩⟨B̂⟩,
is given by

c. Timescale to some Yurke states
√
4 − 6 sin2 (α)
1
,
2 − sin2 (α) +
sin(θ) =
2
N

χ̃ 2
Jˆ .
N z

With this Hamiltonian we write the Heisenberg equations
for the components of the collective spin; they are given by

giving the value
√
2J − 1
.
Z(tf ) = cos(θ ) = √
3J

PRX QUANTUM 4, 020314 (2023)

(B3a)
(B3b)
(B3c)

The ﬁxed points of the phase-space ﬂow in Eqs. (B3),
which are solutions of dX/dt = 0, deﬁne two diﬀerent type
of sets, depending on whether /χ̃ > 1 or /χ̃ < 1. In
the case of the former there are only two ﬁxed points at
(X , Y, Z) = (±1, 0, 0), i.e., the poles with respect to the
turning axis, and phase space is ﬁlled with trajectories
representing Larmor precessions of the mean spin. In the
case of the latter parameter regime, there are four ﬁxed
points, two given by (X , Y, Z) = (±1, 0, 0), where the one
at X = −1 is stable and the one at X = 1 is a saddle. The
two additional ﬁxed points are at
√
(
( )2 )


(X , Y, Z) =
.
(B4)
, 0, ± 1 −
χ̃
χ̃
The two parameter regimes are connected through a pitchfork bifurcation of the stable point at (X , Y, Z) = (1, 0, 0)
happening at /χ̃ = 1. The stability of the ﬁxed points in
these two parameter regimes can be investigated using the
Jacobi matrix associated with the ﬂow in Eqs. (B3), and it
is given by
⎞
⎛
0
χ̃ Z
χ̃ Y
0
− + χ̃X ⎠ .
(B5)
M[X] = ⎝χ̃ Z
0

0
The saddle point at (X , Y, Z) = (1, 0, 0) existing for
parameters such that /χ̃ < 1 is of key importance for our

020314-19

## PDF page 20

MUÑOZ-ARIAS, DEUTSCH, and POGGI

PRX QUANTUM 4, 020314 (2023)

analysis. We know that separatrix branches emerge from it
and conservation of energy guarantees that all points on
the separatrix have the same energy as the saddle. Furthermore, by evaluating the eigenvalues of the Jacobi matrix at
this saddle, one obtains its Lyapunov exponent as
√
TaT
sd = χ̃

(
)


1−
.
χ̃
χ̃

write X and Y in terms of Z as
χ 2
Z ,
X =1−
2

2. Classical energy and the separatrix
Similarly to how we obtained the classical energy density of the 2ACT Hamiltonian, we can obtain the energy
density of the TaT Hamiltonian by computing ⟨ĤTaT ⟩/J
for Eq. (B1) in the thermodynamic limit. After neglecting
correlations and in terms of the classical variables X, this
energy density reads
⟨ĤTaT ⟩
χ̃
= X + Z 2 ,
J
2

S⃗± (Z; χ̃ , )

√
)
(
) (
)
(
χ
χ 2 2
χ 2
Z ,Z ,
Z , ±Z
−1 −
= 1−
2

2
(B11)

(B7)

where “±” denotes the two diﬀerent separatrix branches.
From Eq. (B11) we take its projection onto the y-z plane,
given by
xy
S⃗± (Z; χ̃ , )

√
) (
) )
(
(
χ 2 2
χ
χ 2
Z , ±Z
−1 −
Z .
= 1−
2

2
(B12)

From this last expression, the angle between the (+) and
(−) separatrix branches can be readily computed, giving

which we can write in terms of the classical conjugated
variables Z and φ as
√
χ̃
E(Z, φ; , χ̃ ) =  1 − Z 2 cos(φ) + Z 2 .
2

(B8)

The separatrix equation can be constructed by noting that
conservation of energy guarantees that points on the separatrix have the same energy as the energy of the saddle,
which is given by E(0, 0; χ̃ , ) = , and thus the separatrix is deﬁned by E(Z, φ; χ̃ , ) = . We can use this last
expression to write the following explicit equation for the
separatrix line of the TaT phase-space ﬂow:

cos(φ) =

1 − cos2 (θ)/ω
.
sin(θ )

Y = ±Z

) (
)
χ
χ 2 2
Z ;
−1 −

2
(B10)

then the parametric equation for the separatrix is given by
(B6)

Importantly, the Lyapunov exponent in Eq. (27) has, as a
function of the ratio /χ̃ , a maximum when /χ̃ = 12 , a
parameter regime that deﬁnes critical coupling.

E(X , Z; , χ̃ ) =

√
(

cos(υ) =

(yz)
(yz)
S⃗+ · S⃗−
2 − χ /  + (χ /2)2 Z 2
=
,
(yz)
(yz)
χ /  − (χ /2)2 Z 2
|S⃗+ ||S⃗− |
(B13)

which recovers Eq. (28) in the main text.
b. Eﬀective 2ATC Hamiltonian at critical coupling
Let us now turn our attention to the derivation of the
eﬀective 2ACT Hamiltonian for the TaT Hamiltonian. Our
starting point is to write the TaT Hamiltonian in Eq. (B1)
using the new collective operators deﬁned in Eq. (29).
After this procedure we ﬁnd that
eﬀ
ĤTaT
= Jˆx +

(B9)

χ̃
χ̃ 2
(Jˆ1 Jˆ2 + Jˆ2 Jˆ1 ) +
(J − Jˆ2x ).
2N
2N
(B14)

a. Angle between separatrix branches

We then write Jˆx = J − ô, that is, its mean-ﬁeld minus
ﬂuctuations, and keep terms up to linear in the ﬂuctuations
ô, to obtain
)
(
χ̃
χ̃
eﬀ
ĤTaT = J −  −
ô +
(Jˆ1 Jˆ2 + Jˆ2 Jˆ1 ). (B15)
2
2N

Let us now use Eq. (B9) to derive the result in Eq. (28)
of the main text. The ﬁrst step is to write a parametric
equation for the separatrix. Equation (B9) allows us to

This last expression recovers, at critical coupling χ̃ = 2,
Eq. (31) in the main text.

Here we have explicitly written Z = cos(θ ) and deﬁned
ω = 2/χ̃ .

020314-20

## PDF page 21

PHASE-SPACE GEOMETRY AND OPTIMAL STATE PREPARATION. . .
c. Details of the computation of timescales at critical
coupling
Let us now look into the details of the calculation of the
timescales to the peak spin squeezing and the ﬁrst peak
of the QFI for the TaT dynamics at critical coupling. Our
starting point is the equation of motion for the classical
conjugated variables Z and φ, which are
√
dZ
∂E
=−
=  1 − Z 2 sin(φ),
dt
∂φ
∂E
Z
dφ
=
= −√
cos(φ) + χ̃ Z.
dt
∂Z
1 − Z2

(B16a)
(B16b)

(B17)

χ̃ t = 2

Z(0)

dZ

,
√
Z 1 − Z2

(B18)

recalling that our initial state is√a SCS along the positive x
direction, and thus Z(0) ≈ 1/ 2N . Using this value, and
after solving the integral, we ﬁnd that
√
√
]
Z(tf )( 2N + 2N − 1)
√
χ̃ t = 2 ln
.
1 + 1 − Z 2 (tf )
[

(B19)

For the timescale to peak spin squeezing, we use the fact
that, locally, the TaT separatrices at critical coupling must
be aligned with great circles on the unit sphere. We then
identify Z(tf ) as the limit value for which this statement
holds.
We then exploit the fundamental theorem of the local
theory of curves [53], and compute the curvature κ and
torsion τ for both the 2ACT separatrices and the TaT separatrices at critical coupling. For a great circle in the unit
sphere, the values of these two quantities are
κCT = 1,

τCT = 0.

(B22a)
(B22b)

where we have translated the “origin” to the position of
the saddle point. We look for the value of θ in [0, π/2]
such that these two quantities diﬀer from those of the CT
dynamics by at most 1%. For the curvature, we solve the
equation
(B23)

in the desired range. Equation (B23) has the solution θ ∗ ≈
1.437 72; thus, Z ∗ (tf ) = cos(θ ∗ ) ≈ 0.132 684. At the same
time θ ∗ gives a torsion τTaT (θ ∗ ) ≈ 10−3 ≈ 0. Value which
satisﬁes our requirement and provide the right-hand side of
Eq. (34) in the main text.
d. Length diﬀerence between the separatrices of 2ACT
and TaT at critical coupling

and thus the desired timescale is given by
∫ Z(tf )

torsion for this curve are given by
√
2 13 − 3 cos(2θ )
,
κTaT (θ) =
(3 − cos(2θ ))3/2
12 sin(θ)
3
,
τTaT (θ) = −
4 13 − 3 cos(2θ )

κTaT (θ) = 1.01

Noting that at critical coupling Eq. (B9) simpliﬁes to
cos(φ) = sin(θ), and thus sin(φ) = | cos(θ )|, we can write
the equation for Z in Eqs. (B16) constrained to motion
along the separatrix as
√
dZ
χ̃ √
= Z 1 − Z 2 = Z 1 − Z 2 ,
dt
2

PRX QUANTUM 4, 020314 (2023)

For the separatrix length of the 2ACT dynamics, we
have
∫ π/2 √
π
lCT =
dθ sin2 (θ) + cos2 (θ) = − θ0 , (B24)
2
θ0
√
where θ0 = cos−1 ( 1 − 1/N ).
For TaT at critical coupling, the separatrix length is
given by
∫ θf
√
lTaT =
dθ 1 + sin2 (θ) = E(θf , i),
(B25)
0

√
where θf = cos−1 (1/ 2N ), E(ϕ, k) is the incomplete
elliptic integral of the second kind, and i is the imaginary
unit.
Finally, in the limit N → ∞, we ﬁnd the diﬀerence in
lengths to be
lTaT − lCT = E(i) −

which recovers Eq. (39) in the main text.

(B20)

To compute the curvature and torsion of the TaT separatrix,
we consider the following parametric expression for the
separatrix:

π
ln(2)
≈ 0.3393 ≈
,
2
2

APPENDIX C: DETAILS OF THE QUANTUM
SPEED LIMIT SECTION

(B21)

We introduced the Holstein-Primakoﬀ approximation
with respect to the positive x direction, that is,
√
√
Jˆy = J q̂,
Jˆy = J p̂, (C1)
Jˆx = J − â† â,

with θ the polar angle of spherical coordinates; we only
need to consider the positive branch. The curvature and

where â† (â) is the creation (annihilation) operator for
a single bosonic mode, and q̂, p̂ are bosonic quadrature

S⃗+ (θ) = (sin2 (θ ), sin(θ ) cos(θ ), cos(θ ))

020314-21

## PDF page 22

MUÑOZ-ARIAS, DEUTSCH, and POGGI

PRX QUANTUM 4, 020314 (2023)

operators. Using Eq. (C1), we can write Eq. (B1) as
ĤTaT = −n̂ +

χ̃ 2
p̂ ,
2

(C2)

where n̂ = â† â is the bosonic number operator. Recalling
that q̂2 + p̂ 2 = n̂ + 12 , we can rewrite Eq. (C2) as
(
)
1
1

ĤTaT =  J +
− q̂2 + (χ̃ − )p̂ 2 ,
2
2
2

(C3)

which, after dropping a constant factor, recovers Eq. (40)
in the main text.
We want to compare the speed of evolution of our initial
state under unitary dynamics generated by ĤTaT , V20 , with
the maximum speed of evolution optimized over all quantum states, V2max . Restricted to Gaussian initial states, the
speed is given by [56]
V2Gauss = 18 (Tr[(G)2 ] + Tr[(GJ )2 ]),

The speed in Eq. (C4) is in general unbounded, and
so V2max → ∞. We then restrict ourselves to consider the
speed of evolution under the Gaussian optimized over all
states with a given squeezing r. Under this consideration,
Eq. (C4) can be written as
V2max =

V2max (r) =

(C6)

where matrices R and D are given by
(
)
( r
cos(β)
sin(β)
e
R=
,
D=
0
− sin(β) cos(β)

0
e−r

)

V20 = ⟨

0
M[X] = χ̃ ⎝ −(p − 1)X p−2 Z
(p − 1)X p−2 Y + Yp−1

We focus on the case of p even for this model, with the
case p = 2 covered before. For p > 2, the Jacobi matrix
evaluated at the equatorial ﬁxed points is

ĤTaT ⟩0 =

χ̃ 2
.
8

(C10)

χ̃ 2

V20
2
= 2 2
,
V2max (r)
χ̃ / + (2χ̃ / )|χ̃/ − 2|r

(C11)

which recovers Eq. (46) in the main text.

1. 2ACT with p-order twisting
Starting from the classical ﬂow given in Eqs. (50), we
can compute the Jacobi matrix, which reads

−(p − 1)Yp−2 Z
0
p−2
(p − 1)Y X + X p−1

and

(D2)

⎞
−Yp−1
−X p−1 ⎠ .
0

⎛

0
M[(0, ±1, 0)] = χ̃ ⎝ 0
±1

⎞

0
∓1⎠
0

2

Thus, we can explore the parameter regime where the
quantum speed limit is saturated by considering the ratio
of Eqs. (C10) and (C9), given by

(C7)

⎛

0
0
±1

(C9)

APPENDIX D: DERIVATION OF SOME RESULTS
WITH p-TWISTING HAMILTONIANS

with β an angle of rotation and r ∈ R the squeezing
parameter.

⎛
0
M[(±1, 0, 0)] = χ̃ ⎝0
0

χ̃ 2 1
+ χ̃ |χ̃ − 2| r.
8
4

On the other hand, the speed of unitary evolution for our
initial state is given by

and  is the covariance matrix, which, for a single-mode
Gaussian state, is given by
 = RDRT ,

(C8)

By noting that, when χ̃ < 2, one has cos(2β) = −1,
and when χ̃ > 2, one has cos(2β) = 1, we can write
Eq. (C8) as

(C4)

which holds for undisplaced states, where G is deﬁned in
Eq. (42), J is the symplectic form matrix given by
(
)
0 1
J =
,
(C5)
−1 0

χ̃ 2 1
+ χ̃ (χ̃ − 2) cos(2β)r + O(r2 ).
8
4

(D1)

0
0
0

⎞
∓1
0 ⎠.
0

(D3)

All these cases lead to purely imaginary eigenvalues ±iχ̃ ,
meaning that the ﬁxed points are elliptic or stable. For

020314-22

## PDF page 23

PHASE-SPACE GEOMETRY AND OPTIMAL STATE PREPARATION. . .
the ﬁxed points at the pole (0, 0, ±1) however, we obtain
M = 0, meaning that we need to study the system beyond
linearization, as done in the main text.

PRX QUANTUM 4, 020314 (2023)

the classical variables X, this energy density reads
E(X , Z; , χ̃ ) =

2. Phase-space ﬂow and classical energy for pTaT
In order to construct the phase-space ﬂow in the thermodynamic limit, we need to rescale the pTaT Hamiltonian in
Eq. (53) so that in the thermodynamic limit, we can guarantee the extensivity of the energy density. This is achieved
by introducing the normalized p-twisting strength χ =
χ̃ /pJ p−1 ; we write
ĤpTaT = Jˆx +

χ̃
Jˆp .
pJ p−1 z

dX
= χ̃ YZ p−2 ,
dt
dY
= Z − χ̃ XZ p−2 ,
dt
dZ
= −Y.
dt

(D5a)
(D5b)
(D5c)

Fixed points of this ﬂow are deﬁned as solutions of
dX/dt = 0. Then, solving for the ﬁxed points of Eqs. (D5)
gives the conditions
(
Y = 0,

and

X =

)

1
.
χ̃ Z p−2

(D6)

These conditions, together with |X|2 = 1, give the same
algebraic equation
(
Z 2p−2 − Z 2p−4 +


χ̃

0
M[X] = ⎝−χ̃Z p−1
0

χ̃ Z p−1
0
−

⎞
(p − 1)χ̃ Z p−1 Y
 − (p − 1)χ̃ Z p−1 X ⎠ .
0
(D8)

We can obtain the energy density of the pTaT Hamiltonian
by computing ⟨ĤpTaT ⟩/J for Eq. (D4) in the thermodynamic limit. After neglecting correlations and in terms of

(D10)

3. Proof of Theorem 1
The proof of Theorem 1 follows from the results in the
previous subsection. To see this, we need to rewrite the
statement of the theorem. Local optimality is a geometric
statement; it implies that the phase-space ﬂow has a saddle point, and that the separatrix branches are orthogonal
in the vicinity of the saddle. As such, lack of local optimality implies that there is no parameter regime for which
the separatrix branches are orthogonal. Furthermore, this
implies that there is no parameter regime for which the
principal directions of the saddle point are orthogonal. This
last statement is the one we use to build the proof.
Proving the theorem then reduces to studying the principal directions of the Jacobi matrix in Eq. (D8) evaluated
at the saddle point. Furthermore, we know that these principal directions will be described by orthogonal vectors if
and only if the Jacobi matrix evaluated at the saddle point
is real and symmetric. Noting that the saddle point is a
ﬁxed point of Eqs. (D5), it is true that it should satisfy the
condition in Eq. (D6).
We then evaluate the Jacobi matrix, Eq. (D8), at the saddle via the condition in Eq. (D6), recognizing two diﬀerent
scenarios. First, if p = 2, i.e., TaT, then one has
⎛
0
M[Xsd ] = ⎝0
0

(D7)

whose solution is the Z coordinate of the ﬁxed points.
The Jacobi matrix associated with the phase-space ﬂow
in Eqs. (D5) is given by
⎛

√
χ̃
E(Z, φ; , χ̃ ) =  1 − Z 2 cos(φ) + Z p .
p

)2
= 0,

(D9)

which we can write in terms of the classical conjugated
variables Z and φ as

(D4)

Using the Heisenberg equations of motion for the collective angular momentum Ĵ, and deﬁning the classical
variables X = ⟨Ĵ⟩/J , in the thermodynamic limit, we can
write the pTaT phase-space ﬂow as

χ̃
⟨ĤTaT ⟩
= X + Z p ,
J
p

⎞
0
 − χ̃ ⎠ ,
0

0
0
−

(D11)

which is real and symmetric whenever χ̃ = 2, i.e., at
critical coupling. Second, for all p > 2, one has
⎛

0
p−1
M[Xsd ] = ⎝−χ̃ Zsd
0

p−1

χ̃Zsd
0
−

⎞
0
−(p − 2)⎠ ,
0
(D12)

which is only real and symmetric when p = 3 and Zsd →
0. The latter only happens in the limit χ̃/ → ∞, and thus
there is no parameter regime at which pTaT, with p > 2,
is locally optimal.

020314-23

## PDF page 24

MUÑOZ-ARIAS, DEUTSCH, and POGGI

PRX QUANTUM 4, 020314 (2023)

4. Maximum saddle point Lyapunov exponent for the
pTaT family

5. Angle between separatrix branches at critical
coupling for 3TaT

The ﬁrst step in this calculation is to consider a
reduced form of the classical energy density, obtained from
Eq. (D10) by setting φ = 0, given by

For 3TaT at critical coupling, the positions of the saddle
and control parameters are given by
∣
1
4
χ̃ ∣∣
@max[sd ]
(D21)
= ,
=√ .
Zsd
∣
2
 max[sd ]
3

√
χ̃
E(Z; , χ̃ ) =  1 − Z 2 + Z p .
p

(D13)

This reduced energy only looks at the great circle on the xz plane, along which extreme points of the classical energy,
i.e., ﬁxed points of the phase-space ﬂow, might emerge. In
order to ﬁnd the value of χ̃/ at which the saddle point
Lyapunov exponent is maximum, we need an auxiliary
equation, such that the system of equations can be solved
for the pair
∣
(
)
@max[sd ] χ̃ ∣∣
Zsd
, ∣
.
(D14)
 max[sd ]
To ﬁnd this auxiliary equation, we solve for the eigenvalues of Eq. (D12), and write an expression for the Lyapunov
exponent of the saddle point
√
(p − 2)
2p−2
sd = χ̃
− Zsd ,
(D15)
U2

Given these two values, it is easy to see that the energy
of the saddle√ and thus the energy of the separatrix is
Esep = 5/3 3. With this we can write an equation for
the separatrix line of 3TaT√at critical coupling, by writing E(Z, φ; χ̃ , ) = 5/3 3. In terms of the angular
variables we ﬁnd that
1
cos(φ) = √
(4 − 5 cos3 (θ)).
3 3 sin(θ)

We can use Eq. (D22) to write the separatrix in parametric
form as
S⃗± (θ) = (X (θ), Y± (θ), Z(θ)),

1
X (θ) = √ (4 − 5 cos3 (θ)),
3 3
√
1
Y± (θ) = ± sin2 (θ) − (4 − 5 cos3 (θ))2 ,
27
Z(θ) = cos(θ).

(D16)

where E(Z) is deﬁned in Eq. (D13). From this expression
we can write the ratio χ̃ /  as
U=

Z p−2

1
.
√
1 − Z2

(D17)

max[sd ]

Zsd

=

p −2
.
p −1

cos(υ) =

Together, Eqs. (D19) and (D20) recover Eqs. (55) in the
main text.

(D24b)
(D24c)

(YZ) ⃗ (YZ)
S⃗+
·S−
,
(YZ)
(YZ)
|S⃗+ ||S⃗−
|

(D25)

where
(YZ)
S⃗±
=

(D19)

By substituting Eq. (D19) into Eq. (D17), we obtain
∣
χ̃ ∣∣
(p − 1)p−1
√
=
. (D20)
 ∣max[sd ] (p − 2)p−2 (p − 1)2 − (p − 2)2

(D24a)

To compute the angle between separatrix branches, we
take the projection of the separatrix onto the y-z plane
and translate the saddle to the origin, that is, we take
Z(θ) = cos(θ) − 12 ; then the angle is calculated as the dot
product between the two branches, i.e.,

By substituting Eq. (D17) into Eq. (D15), we obtain
√
sd = χ̃Z p−2 (p − 1) − (p − 2)Z 2 ;
(D18)
then, by solving dsd /dZ = 0, we obtain the position of
the saddle point when the Lyapunov exponent is maximum, given by

(D23)

whose components are given by

where U = χ̃/. In order to proceed further, we use the
fact that the saddle point is an extreme point of the classical
energy density, and thus it satisﬁes
√
dE(Z)
= 0 → Z = UZ p−1 1 − Z 2 ,
dZ

(D22)

)
( √
1
1
2
3
2
.
± sin (θ) − (4 − 5 cos (θ)) , cos(θ ) −
27
2
(D26)

In the vicinity of the saddle point, we ﬁnd that cos(υ) = 15 .
6. Time scale to the ﬁrst peak of the QFI with 3TaT
The fact that at critical coupling the semiclassical energy
is a double well with wells of equal depth indicates that one
can prepare a “catlike” state where the peaks of each lobe
lie at the bottom of each of the wells, and the timescale

020314-24

## PDF page 25

PHASE-SPACE GEOMETRY AND OPTIMAL STATE PREPARATION. . .
to this state can, in principle, be estimated via a similar
argument to that used for the p = 2 spin.
Our starting point is the canonical equations of motion
obtained from the classical energy density in Eq. (D10),
given by
√
dZ
∂E
=−
=  1 − Z 2 sin(φ),
dt
∂φ
dφ
∂E
cos(φ)Z
=
= − √
+ χ̃Z 2 .
dt
∂Z
1 − Z2

(D27a)
(D27b)

Using the equation of the separatrix at critical coupling,
we can write an equation of motion for Z constrained to
the separatrix branches; it reads
dZ
χ̃ √
=
27(1 − Z 2 ) − (5 − 4Z 3 )2 ,
dt
12

(D28)

projected back to the z axis. Given that the angle between
separatrix branches is cos(υ) = 1/5, we can get the angle
between the separatrix branch and the z axis. It is given by
√
cos(υ̃) =

χ̃t =

Z(0)

12dZ
√
.
27(1 − Z 2 ) − (5 − 4Z 3 )2

√
3
a= √ ,
2 N

In order to complete this computation, we need to specify
the limits of integration in Eq. (D29). Specifying these limits of integration requires us to think a little bit more about
the separatrix geometry.
The value of Z(tf ) is either one of the two “end” points
of the separatrix, that is, either of the two points at the
intersection of the separatrix with the great circle in the
x-z plane having the same energy as the saddle point. We
can ﬁnd them by equating the energy of the saddle with
the semiclassical energy and solving for the roots of the
resulting algebraic equation. Such an algebraic equation is
given by
16Z 6 − 40Z 3 + 27Z 2 − 2 = 0,

(D30)

Zl = −0.234 334 06

(D34)

4N 2
Y = 1.
3

(D35)

(

Zsp
tan
Ysp

)

sin(υ̃)
=
=
cos(υ̃)

√

2
;
3

(D36)

thus,
Zsp
Ysp =
= tan−1
υ̃

(√ )
2
.
3

(D37)

Substituting Eq. (D37) into Eq. (D35) gives
1
,
Zsp = √
2 (1 + 1/3υ̃ 2 )N

(D38)

and, thus,
Z(0) =

1
1
.
+ √
2 2 (1 + 1/3υ̃ 2 )N

(D39)

(D31)

for the “upper” and “lower” end points, respectively. For
the timescale calculation, we assume that Z(tf ) = Zu , that
is, motion from the saddle to the “upper” end point (note
that motion happens symmetrically towards Zl as well).
For the initial condition, it is not hard to see that it should
have the form
Z0 = 12 + dsp ,

1
b= √ ,
2 N

On the other hand, the point at the intersection between the
ellipse and the separatrix branch satisﬁes

which has three solutions, Z = 1/2, i.e., the saddle point,
and
Zu = 0.959 078 9,

(D33)

and thus the ellipse is described by the equation
4NZ 2 +

(D29)

3
.
5

From Eq. (D33) we can compute dsp in the following
way. Consider the initial uncertainty patch of the SCS projected onto the y-z plane. It corresponds with an ellipse
whose semimajor and semiminor axes, on the y and z axes,
respectively, are given by

and thus the desired timescale is given by
∫ Z(tt )

PRX QUANTUM 4, 020314 (2023)

(D32)

that is, the position of the saddle plus a small increment
dsp . The latter is the distance from the center of the SCS
distribution to the edge measured along the separatrix and

After which the timescale is completely determined, and it
completes the derivation of Eq. (62) in the main text.

[1] V. Giovannetti, S. Lloyd, and L. Maccone, Quantum
Metrology, Phys. Rev. Lett. 96, 010401 (2006).
[2] V. Giovannetti, S. Lloyd, and L. Maccone, Advances in
quantum metrology, Nat. Photon. 5, 222 (2011).
[3] L. Pezzè, A. Smerzi, M. K. Oberthaler, R. Schmied, and P.
Treutlein, Quantum metrology with nonclassical states of
atomic ensembles, Rev. Mod. Phys. 90, 035005 (2018).
[4] C. L. Degen, F. Reinhard, and P. Cappellaro, Quantum
sensing, Rev. Mod. Phys. 89, 035002 (2017).

020314-25

## PDF page 26

MUÑOZ-ARIAS, DEUTSCH, and POGGI

PRX QUANTUM 4, 020314 (2023)

[5] M. Kitagawa and M. Ueda, Squeezed spin states, Phys. Rev.
A 47, 5138 (1993).
[6] A. S. Sørensen and K. Mølmer, Entanglement and Extreme
Spin Squeezing, Phys. Rev. Lett. 86, 4431 (2001).
[7] J. Ma, X. Wang, C.-P. Sun, and F. Nori, Quantum spin
squeezing, Phys. Rep. 509, 89 (2011).
[8] C. Gross, Spin squeezing, entanglement and quantum
metrology with Bose–Einstein condensates, J. Phys. B: At.,
Mol. Opt. Phys. 45, 103001 (2012).
[9] D. J. Wineland, J. J. Bollinger, W. M. Itano, F. L. Moore,
and D. J. Heinzen, Spin squeezing and reduced quantum
noise in spectroscopy, Phys. Rev. A 46, R6797 (1992).
[10] G. Tóth and I. Apellaniz, Quantum metrology from a quantum information science perspective, J. Phys. A: Math.
Theor. 47, 424006 (2014).
[11] J. Huang, X. Qin, H. Zhong, Y. Ke, and C. Lee, Quantum
metrology with spin cat states under dissipation, Sci. Rep.
5, 1 (2015).
[12] R. H. Dicke, Coherence in spontaneous radiation processes,
Phys. Rev. 93, 99 (1954).
[13] L. Pezzé and A. Smerzi, Entanglement, Nonlinear Dynamics, and the Heisenberg Limit, Phys. Rev. Lett. 102, 100401
(2009).
[14] Here we emphasize that the type of quantum metrology
protocol that exploits the quantum states we are about to
mention is often referred as local quantum metrology. This
clariﬁcation is made with the aim of avoiding confusion
with the quantum metrology protocols known as Bayesian
quantum metrology.
[15] A. Micheli, D. Jaksch, J. I. Cirac, and P. Zoller, Manyparticle entanglement in two-component Bose-Einstein
condensates, Phys. Rev. A 67, 013607 (2003).
[16] G. Sorelli, M. Gessner, A. Smerzi, and L. Pezzè, Fast and
optimal generation of entanglement in bosonic Josephson
junctions, Phys. Rev. A 99, 022329 (2019).
[17] E. Yukawa, G. J. Milburn, C. A. Holmes, M. Ueda, and
K. Nemoto, Precision measurements using squeezed spin
states via two-axis countertwisting interactions, Phys. Rev.
A 90, 062132 (2014).
[18] D. Kajtoch and E. Witkowska, Quantum dynamics generated by the two-axis countertwisting Hamiltonian, Phys.
Rev. A 92, 013623 (2015).
[19] A. Polkovnikov, Phase space representation of quantum
dynamics, Ann. Phys. (N. Y) 325, 1790 (2010).
[20] B. Zhu, A. M. Rey, and J. Schachenmayer, A generalized
phase space approach for solving quantum spin dynamics,
New J. Phys. 21, 082001 (2019).
[21] J. K. Stockton, J. Geremia, A. C. Doherty, and H.
Mabuchi, Characterizing the entanglement of symmetric
many-particle spin- 12 systems, Phys. Rev. A 67, 022112
(2003).
[22] V. Bapst and G. Semerjian, On quantum mean-ﬁeld models
and their quantum annealing, J. Stat. Mech.: Theory Exp.
2012, P06007 (2012).
[23] G. Salvatori, A. Mandarino, and M. G. A. Paris, Quantum
metrology in Lipkin-Meshkov-Glick critical systems, Phys.
Rev. A 90, 022111 (2014).
[24] I. Frérot and T. Roscilde, Quantum Critical Metrology,
Phys. Rev. Lett. 121, 020402 (2018).
[25] L. J. Fiderer and D. Braun, Quantum metrology with
quantum-chaotic sensors, Nat. Commun. 9, 1 (2018).

[26] S. Boixo, A. Datta, M. J. Davis, S. T. Flammia, A.
Shaji, and C. M. Caves, Quantum Metrology: Dynamics versus Entanglement, Phys. Rev. Lett. 101, 040403
(2008).
[27] S. Boixo, A. Datta, S. T. Flammia, A. Shaji, E. Bagan,
and C. M. Caves, Quantum-limited metrology with product
states, Phys. Rev. A 77, 012317 (2008).
[28] M. Beau and A. del Campo, Nonlinear Quantum Metrology
of Many-Body Open Systems, Phys. Rev. Lett. 119, 010403
(2017).
[29] T. Macrì, A. Smerzi, and L. Pezzè, Loschmidt echo for
quantum metrology, Phys. Rev. A 94, 010102 (2016).
[30] E. Davis, G. Bentsen, and M. Schleier-Smith, Approaching the Heisenberg Limit without Single-Particle Detection,
Phys. Rev. Lett. 116, 053601 (2016).
[31] F. Anders, L. Pezzè, A. Smerzi, and C. Klempt, Phase magniﬁcation by two-axis countertwisting for detection-noise
robust interferometry, Phys. Rev. A 97, 043813 (2018).
[32] S. P. Nolan, S. S. Szigeti, and S. A. Haine, Optimal
and Robust Quantum Metrology Using Interaction-Based
Readouts, Phys. Rev. Lett. 119, 193601 (2017).
[33] T. J. Volkoﬀ and M. J. Martin, Asymptotic optimality of
twist-untwist protocols for Heisenberg scaling in atombased sensing, Phys. Rev. Res. 4, 013236 (2022).
[34] This is a well-known result of Heisenberg-limited spin
squeezing achieved with 2ACT [5]; for N = 1024, this
gives a squeezing of 80 log10 (2) ≈ 25 dB.
[35] D. W. Berry and H. M. Wiseman, Optimal States and
Almost Optimal Adaptive Measurements for Quantum
Interferometry, Phys. Rev. Lett. 85, 5098 (2000).
[36] J. Combes and H. M. Wiseman, States for phase estimation
in quantum interferometry, J. Opt. B: Quantum Semiclass.
Opt. 7, 14 (2004).
[37] R. Schubert, R. O. Vallejos, and F. Toscano, How do wave
packets spread? Time evolution on Ehrenfest time scales, J.
Phys. A: Math. Theor. 45, 215307 (2012).
[38] S. Pappalardi, A. Russomanno, B. Žunkovič, F. Iemini, A.
Silva, and R. Fazio, Scrambling and entanglement spreading in long-range spin chains, Phys. Rev. B 98, 134303
(2018).
[39] H. Strobel, W. Muessel, D. Linnemann, T. Zibold, D. B.
Hume, L. Pezzè, A. Smerzi, and M. K. Oberthaler, Fisher
information and entanglement of non-Gaussian spin states,
Science 345, 424 (2014).
[40] W. Muessel, H. Strobel, D. Linnemann, T. Zibold, B. JuliáDíaz, and M. K. Oberthaler, Twist-and-turn spin squeezing
in Bose-Einstein condensates, Phys. Rev. A 92, 023603
(2015).
[41] S. S. Mirkhalaf, S. P. Nolan, and S. A. Haine, Robustifying twist-and-turn entanglement with interaction-based
readout, Phys. Rev. A 97, 053618 (2018).
[42] B. Braverman, A. Kawasaki, E. Pedrozo-Peñaﬁel, S.
Colombo, C. Shu, Z. Li, E. Mendez, M. Yamoah, L.
Salvi, D. Akamatsu, Y. Xiao, and V. Vuletić, Near-Unitary
Spin Squeezing in 171 Yb, Phys. Rev. Lett. 122, 223203
(2019).
[43] Z. Li, B. Braverman, S. Colombo, C. Shu, A. Kawasaki,
A. F. Adiyatullin, E. Pedrozo-Peñaﬁel, E. Mendez, and V.
Vuletić, Collective Spin-Light and Light-Mediated SpinSpin Interactions in an Optical Cavity, PRX Quantum 3,
020308 (2022).

020314-26

## PDF page 27

PHASE-SPACE GEOMETRY AND OPTIMAL STATE PREPARATION. . .
[44] H. Lipkin, N. Meshkov, and A. Glick, Validity of manybody approximation methods for a solvable model: (I).
Exact solutions and perturbation theory, Nucl. Phys. 62, 188
(1965).
[45] J. Vidal, G. Palacios, and C. Aslangul, Entanglement
dynamics in the Lipkin-Meshkov-Glick model, Phys. Rev.
A 70, 062304 (2004).
[46] S. Dusuel and J. Vidal, Finite-Size Scaling Exponents of the
Lipkin-Meshkov-Glick Model, Phys. Rev. Lett. 93, 237204
(2004).
[47] J. I. Latorre, R. Orús, E. Rico, and J. Vidal, Entanglement
entropy in the Lipkin-Meshkov-Glick model, Phys. Rev. A
71, 064101 (2005).
[48] S. Dusuel and J. Vidal, Continuous unitary transformations
and ﬁnite-size scaling exponents in the Lipkin-MeshkovGlick model, Phys. Rev. B 71, 224420 (2005).
[49] W. D. Heiss, F. G. Scholtz, and H. B. Geyer, The large n
behaviour of the Lipkin model and exceptional points, J.
Phys. A: Math. Gen. 38, 1843 (2005).
[50] D. Gutiérrez-Ruiz, D. Gonzalez, J. Chávez-Carlos, J. G.
Hirsch, and J. D. Vergara, Quantum geometric tensor and
quantum phase transitions in the Lipkin-Meshkov-Glick
model, Phys. Rev. B 103, 174104 (2021).
[51] A. Lerose and S. Pappalardi, Origin of the slow growth
of entanglement entropy in long-range interacting spin
systems, Phys. Rev. Res. 2, 012041 (2020).
[52] This fact implies that opposite ends of the separatrix
touch the points (X , Y, Z) = (0, 0, ±1). In other words, the
state |ψ⟩ = |J , J ⟩ has energy equal to that of the separatrix line. This deﬁnes the dynamical critical point of the
dynamical quantum phase transition of Hamiltonian (23).
Interestingly, the metrological relevance of this dynamical quantum phase transition was recently investigated in
Ref. [78].
[53] M. P. do Carmo, Diﬀerential Geometry of Curves and
Surfaces (Prentice-Hall, New Jersey, 1976).
[54] D. P. Pires, M. Cianciaruso, L. C. Céleri, G. Adesso, and D.
O. Soares-Pinto, Generalized Geometric Quantum Speed
Limits, Phys. Rev. X 6, 021031 (2016).
[55] S. Deﬀner and S. Campbell, Quantum speed limits: from
Heisenberg’s uncertainty principle to optimal quantum control, J. Phys. A: Math. Theor. 50, 453001 (2017).
[56] P. M. Poggi, S. Campbell, and S. Deﬀner, Diverging Quantum Speed Limits: A Herald of Classicality, PRX Quantum
2, 040349 (2021).
[57] T. Holstein and H. Primakoﬀ, Field dependence of the
intrinsic domain magnetization of a ferromagnet, Phys.
Rev. 58, 1098 (1940).
[58] C. M. Trail, P. S. Jessen, and I. H. Deutsch, Strongly
Enhanced Spin Squeezing via Quantum Control, Phys. Rev.
Lett. 105, 193602 (2010).
[59] Q. Wang and F. Pérez-Bernal, Probing an excited-state
quantum phase transition in a quantum many-body system via an out-of-time-order correlator, Phys. Rev. A 100,
062113 (2019).
[60] P. Stránský, M. Macek, and P. Cejnar, Excited-state quantum phase transitions in systems with two degrees of freedom: Level density, level dynamics, thermal properties,
Ann. Phys. (N. Y.) 345, 73 (2014).

PRX QUANTUM 4, 020314 (2023)

[61] P. Cejnar, P. Stránský, M. Macek, and M. Kloc, Excitedstate quantum phase transitions, J. Phys. A: Math. Theor.
54, 133001 (2021).
[62] Á. L. Corps and A. Relaño, Theory of dynamical phase
transitions in collective quantum systems, (2022), arXiv
preprint ArXiv:2205.03443.
[63] A. L. Corps and A. Relaño, Dynamical and excited-state
quantum phase transitions in collective systems, Phys. Rev.
B 106, 024311 (2022).
[64] L. Zhou, J. Kong, Z. Lan, and W. Zhang, Dynamical quantum phase transitions in a spinor Bose-Einstein condensate
and criticality enhanced quantum sensing, (2022), arXiv
preprints ArXiv:2209.11415.
[65] T. Jörg, F. Krzakala, J. Kurchan, A. C. Maggs, and J. Pujos,
Energy gaps in quantum ﬁrst-order mean-ﬁeld–like transitions: The problems that quantum annealing cannot solve,
EPL (Europhys. Lett.) 89, 40004 (2010).
[66] S. Matsuura, H. Nishimori, W. Vinci, T. Albash, and D. A.
Lidar, Quantum-annealing correction at ﬁnite temperature:
Ferromagnetic p-spin models, Phys. Rev. A 95, 022308
(2017).
[67] M. Filippone, S. Dusuel, and J. Vidal, Quantum phase transitions in fully connected spin models: An entanglement
perspective, Phys. Rev. A 83, 022327 (2011).
[68] L. Del Re, M. Fabrizio, and E. Tosatti, Nonequilibrium and
nonhomogeneous phenomena around a ﬁrst-order quantum
phase transition, Phys. Rev. B 93, 125131 (2016).
[69] M. H. Muñoz Arias, I. H. Deutsch, P. S. Jessen, and P.
M. Poggi, Simulation of the complex dynamics of meanﬁeld p-spin models using measurement-based quantum
feedback control, Phys. Rev. A 102, 022610 (2020).
[70] L. Correale and A. Silva, Changing the order of a dynamical
phase transition through ﬂuctuations in a quantum p-spin
model, (2021), arXiv preprint ArXiv:2110.13524.
[71] This is a central point in the phase-space approach presented in this work. Approximating the timescales to certain metrologically useful states, via the motion of points
along separatrix branches, requires this motion to take place
symmetrically with respect to the saddle point.
[72] M. H. Muñoz Arias, K. Chinni, and P. M. Poggi, Floquet
time crystals in driven spin systems with all-to-all p-body
interactions, Phys. Rev. Res. 4, 023018 (2022).
[73] One can deﬁne this neighborhood by taking a small energy
window centered at the separatrix energy.
[74] T. Xu, T. Scaﬃdi, and X. Cao, Does Scrambling Equal
Chaos?, Phys. Rev. Lett. 124, 140602 (2020).
[75] R. A. Kidd, A. Safavi-Naini, and J. F. Corney, Saddlepoint scrambling without thermalization, Phys. Rev. A 103,
033304 (2021).
[76] M. Koppenhöfer, P. Groszkowski, H.-K. Lau, and
A. A. Clerk, Dissipative superradiant spin ampliﬁer
for enhanced quantum sensing, (2021), arXiv preprint
ArXiv:2111.15647.
[77] R. Grobe and F. Haake, Dissipative death of quantum
coherences in a spin system, Z. für Phys. B - Condens.
Matter 68, 503 (1987).
[78] Q. Guan and R. J. Lewis-Swan, Identifying and harnessing
dynamical phase transitions for quantum-enhanced sensing,
Phys. Rev. Res. 3, 033199 (2021).

020314-27
