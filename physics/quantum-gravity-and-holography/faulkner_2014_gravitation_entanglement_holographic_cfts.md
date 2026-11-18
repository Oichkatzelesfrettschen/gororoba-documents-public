Source: https://link.springer.com/content/pdf/10.1007/JHEP03(2014)051.pdf
PDF sha256: 35a3e03302fe56c86f5404918f793174a1ff72360b321c912158864968bafe28
License: CC-BY-4.0
Language: eng
Fidelity: machine-gated

# Transcription of faulkner_2014_gravitation_entanglement_holographic_cfts.pdf

Transcription of `faulkner_2014_gravitation_entanglement_holographic_cfts.pdf` in this directory, 41 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-41 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Published for SISSA by

Springer

Received: January 14, 2014
Accepted: February 6, 2014
Published: March 11, 2014

Gravitation from entanglement in holographic CFTs

a

Institute for Advanced Study,
Princeton, NJ 08540, U.S.A.
b
Department of Physics and Astronomy, University of Pennsylvania,
209 S. 33rd St., Philadelphia, PA 19104-6396, U.S.A.
c
Kavli Institute for Theoretical Physics, University of California,
Santa Barbara, CA 93106-4030 U.S.A.
d
Perimeter Institute for Theoretical Physics,
31 Caroline Street N., Waterloo, Ontario N2L 2Y5, Canada
e
Department of Physics and Astronomy, University of British Columbia,
6224 Agricultural Road, Vancouver, B.C. V6T 1W9, Canada

E-mail: faulkner@ias.edu, mguica@sas.upenn.edu,
thartman@kitp.ucsb.edu, rmyers@perimeterinstitute.ca, mav@phas.ubc.ca
Abstract: Entanglement entropy obeys a ‘first law’, an exact quantum generalization of
the ordinary first law of thermodynamics. In any CFT with a semiclassical holographic
dual, this first law has an interpretation in the dual gravitational theory as a constraint
on the spacetimes dual to CFT states. For small perturbations around the CFT vacuum
state, we show that the set of such constraints for all ball-shaped spatial regions in the CFT
is exactly equivalent to the requirement that the dual geometry satisfy the gravitational
equations of motion, linearized about pure AdS. For theories with entanglement entropy
computed by the Ryu-Takayanagi formula S = A/(4GN ), we obtain the linearized Einstein
equations. For theories in which the vacuum entanglement entropy for a ball is computed
by more general Wald functionals, we obtain the linearized equations for the associated
higher-curvature theories. Using the first law, we also derive the holographic dictionary for
the stress tensor, given the holographic formula for entanglement entropy. This method
provides a simple alternative to holographic renormalization for computing the stress tensor
expectation value in arbitrary higher derivative gravitational theories.
Keywords: Gauge-gravity correspondence, AdS-CFT Correspondence
ArXiv ePrint: 1312.7856

Open Access, c
⃝ The Authors.
Article funded by SCOAP3 .

doi:10.1007/JHEP03(2014)051

JHEP03(2014)051

Thomas Faulkner,a Monica Guica,b Thomas Hartman,c Robert C. Myersd
and Mark Van Raamsdonke

## PDF page 2

Contents
2

2 Background
2.1 The first law of entanglement entropy
2.2 The first law in conformal field theories
2.3 Interpretation of the first law in holographic CFTs
2.3.1 Holographic interpretation of the entanglement entropy
2.3.2 Holographic interpretation of the modular energy EB
2.3.3 Summary

5
5
6
8
8
10
10

3 The holographic first law of entanglement from the first law of black hole
thermodynamics
11
4 Linearized gravity from the holographic first law
4.1 The holographic stress tensor from the holographic entanglement functional
4.2 The linearized Fefferman-Graham expansion
4.3 Linearized equations from the holographic entanglement functional

12
12
14
14

5 Linearized equations in general theories of gravity
5.1 The covariant formalism for entropy and conserved charges
5.2 Definition of χ
5.3 Equivalence of the holographic and the canonical modular energy

18
18
21
22

6 Application: the holographic dictionary in higher curvature gravity
6.1 General results
6.2 Examples
6.2.1 The holographic stress tensor in R2 gravity
6.2.2 An R4 example
6.3 Other terms in the FG expansion

24
25
28
28
30
30

7 Discussion

32

A Vanishing of the integrand

34

B Noether identities and the off-shell Hamiltonian

34

C Example: Einstein gravity coupled to a scalar

35

D Form of the bulk charge

36

–1–

JHEP03(2014)051

1 Introduction

## PDF page 3

1

Introduction

The ‘first law’ of entanglement entropy
The crucial piece of CFT physics giving rise to linearized gravitational equations in the
dual theory is a ‘first law’ of entanglement entropy,
δSA = δ⟨HA ⟩

(1.1)

equating the first order variation in the entanglement entropy for a spatial region A with
the first order variation in the expectation value of HA , the modular (or entanglement)
Hamiltonian. The latter operator is defined as the logarithm of the unperturbed state, i.e.
ρA ≃ e−HA — see section 2.1 for further details. The first law was derived in [17]1 as a
special case of a more general result for finite perturbations
∆SA ≤ ∆⟨HA ⟩

(1.2)

obtained using the positivity of ‘relative entropy’.2 A more direct demonstration of (1.1)
is reviewed in section 2.1 below.
1

Related observations had been made independently using various holographic calculations, e.g. [18–21].
Relative entropy can be viewed as a statistical measure of the distance between two states (i.e. density
matrices) in the same Hilbert space — e.g. see [22, 23] for reviews.
2

–2–

JHEP03(2014)051

According to the AdS/CFT correspondence, spacetime and gravitational physics in AdS
emerge from the dynamics of certain strongly-coupled conformal field theories with a large
number of degrees of freedom. A central question is to understand why and how this
happens. In recent work, it has been suggested that the physics of quantum entanglement
plays an essential role, e.g. [1–11]. This was motivated in part by the importance of
quantum entanglement for understanding quantum phases of matter in condensed matter
systems [12–15]. Ryu and Takayanagi have proposed [1–4] that entanglement entropy, one
measure of entanglement between subsets of degrees of freedom in general quantum systems,
provides a direct window into the emergent spacetime geometry, giving the areas of certain
extremal surfaces. This provides a quantitative connection between CFT entanglement and
the dual spacetime geometry. Recently, this connection has been utilized to understand
the emergence of spacetime dynamics (i.e. gravity) from the CFT physics [16]. Making
use of a ‘first law’ for entanglement entropy derived in [17], it was shown [16] that in any
holographic theory for which the Ryu-Takayanagi prescription computes the entanglement
entropy of the boundary CFT, spacetimes dual to small perturbations of the CFT vacuum
state must satisfy Einstein’s equations linearized around pure AdS spacetime.
In this paper, we provide further insight into the results of [16, 17] and extend them
to general holographic CFTs, for which the classical bulk equations may include terms at
higher order in the curvatures or derivatives. We show further that the first law for entanglement entropy in the CFT can be understood as the microscopic origin of a particular case
of the first law of black hole thermodynamics, applied to AdS-Rindler horizons. We begin
with a brief review of some essential background before summarizing our main results.

## PDF page 4

In general, the modular Hamiltonian HA is a complicated object that cannot be expressed as an integral of local operators. However, starting from the vacuum state of a
CFT in flat space and taking A to be a ball-shaped spatial region of radius R centered at
x0 , denoted B(R, x0 ), the modular Hamiltonian is given by a simple integral [24]
HB = 2π

∫

dd−1 x
B(R,x0 )

R2 − |⃗x − ⃗x0 |2
Ttt ,
2R

(1.3)

where HB and SB denote the modular Hamiltonian and the entanglement entropy for a
ball, respectively.
The holographic interpretation
For conformal field theories with a gravity dual, the first law for ball-shaped regions can
be translated into a geometrical constraint obeyed by any spacetime dual to a small perturbation of the CFT vacuum. To understand this, we first recall the holographic interpretation of entanglement entropy and energy density in the general case (see section 2.3
for more details).
As shown by [24] in deriving (1.3), the vacuum entanglement entropy of a CFT for a
ball-shaped region in flat space can be reinterpreted as the thermal entropy of the CFT
on a hyperbolic cylinder at temperature set by the hyperbolic space curvature scale, by
relating the two backgrounds with a conformal mapping. For a holographic CFT, the
latter thermal entropy may then be calculated as the horizon entropy of the “black hole”
dual to this thermal state on hyperbolic space. In this case, the black hole is simply a
Rindler wedge (which we call the AdS-Rindler patch) of the original pure AdS space, as
shown in figure 2. If the gravitational theory in the bulk is Einstein gravity, then the
horizon entropy is given by the usual Bekenstein-Hawking formula, SBH = A/(4GN ), and
this construction [24] provides a derivation of the Ryu-Takayanagi prescription [1, 2] for
a spherical entangling surface.3 However, we note that the same analysis applies for any
classical and covariant gravity theory in the bulk, in which case the horizon entropy is
given by Wald’s formula [26–28]
∫
√
δL
nab ncd ,
(1.5)
SWald = −2π
dn σ h
δRab cd
H
where L denotes the gravitational Lagrangian and nab is the binormal to the horizon H.
To summarize, in general holographic theories, entanglement entropy in the vacuum
state for a ball-shaped region B is computed by the Wald functional applied to the horizon
3

Recently, this approach was extended to a general argument for the Ryu-Takayanagi prescription for
arbitrary entangling surfaces in time-independent (and some special time-dependent) backgrounds [25].

–3–

JHEP03(2014)051

of the energy density over the interior of the sphere (weighted by a certain spatial profile).
Thus, given any perturbation to the CFT vacuum we have for any ball-shaped region
∫
R2 − |⃗x − ⃗x0 |2
δSB = 2π
dd−1 x
δ⟨Ttt ⟩ ,
(1.4)
2R
B(R,x0 )

## PDF page 5

Main results
Our first main result, presented in section 3, is that this first law for AdS-Rindler spacetimes, i.e. the gravitational version of (1.4), is a special case of a first law proved by Iyer and
Wald for stationary spacetimes with bifurcate Killing horizons (i.e. at finite temperature)
in general classical theories of gravity. According to Iyer and Wald, for any perturbation of a stationary background that satisfies the linearized equations of motion following
from some Lagrangian, the first law holds provided we define horizon entropy using the
Wald functional (1.5) associated with this Lagrangian. Thus, the CFT result (1.4) can
be seen as an exact quantum version of the Iyer-Wald first law, at least for the case of
AdS-Rindler horizons.
Our second result, presented in sections 4 and 5, provides a converse to the theorem
of Iyer and Wald. In AdS space, we can associate an AdS-Rindler patch to any ballshaped spatial region on the boundary in any Lorentz frame, as in figure 2. An arbitrary
perturbation to the AdS metric can be understood as a perturbation to each of these
Rindler patches. We show that if the first law is satisfied for every AdS-Rindler patch,
then the perturbation must satisfy the linearized gravitational equations. Thus, the set
of non-local constraints (one for each ball-shaped region in each Lorentz frame) implied
by (1.4) is equivalent to the set of local gravitational equations.
The result in the previous paragraph — that the first law for AdS-Rindler patches
implies the linearized gravitational equations — is completely independent of AdS/CFT
and holds for any classical theory of gravity in AdS. However, since for holographic CFTs
this gravitational first law is implied by the entanglement first law, we conclude that
the linearized gravitational equations for the dual spacetime can be derived from any
holographic CFT, given the entanglement functional. This extends the results of [16] to
general holographic CFTs.
As a further application of the entanglement first law, we point out (see section 4.1)
that eq. (1.1), applied to infinitesimal balls, can be used to deduce the ‘holographic stress
tensor,’ i.e. the gravitational quantity that computes the expectation value of the CFT
stress tensor, given the holographic prescription for computing entanglement entropy. This
provides a simple alternative approach to the usual holographic renormalization procedure,

–4–

JHEP03(2014)051

of the AdS-Rindler patch associated with B. We will argue in section 2.3 that this should
remain true for perturbations to the vacuum state, so the left side of (1.4) computes the
change in entropy of the AdS-Rindler horizon under a small variation of the CFT state.
Meanwhile, the expectation value of the stress tensor is related to the asymptotic behaviour
of the metric, so the right side of (1.4) may be expressed as an integral involving the
asymptotic metric over a ball-shaped region of the boundary. In section 2.3, we show that
this integral may be interpreted as the variation in energy of the AdS-Rindler spacetime.
Thus, the gravity version of the entanglement first law (1.4) may be interpreted as a first
law for AdS-Rindler spacetimes. At a technical level, this represents a non-local constraint
on the spacetime fields, equating an integral involving the asymptotic metric perturbation
over a boundary surface to an integral involving the bulk metric perturbation (and possibly
matter fields) over a bulk surface.

## PDF page 6

as we illustrate with examples in section 6. Finally, we show that eq. (1.1) also provides information about the operators in the boundary theory corresponding to additional degrees
of freedom that can be associated with the metric in the context of higher derivative gravity.
We conclude in section 7 with a brief discussion of our results. In particular, we discuss
the relation of our work to the work of Jacobson [29], who obtained gravitational equations
by considering a gravitational first law applied to local Rindler horizons.

2

Background

2.1

The first law of entanglement entropy

For any state in a general quantum system, the state of a subsystem A is described by a
reduced density matrix ρA = trĀ ρtotal , where ρtotal is the density matrix describing the
global state of the full system and Ā is the complement of A. The entanglement of this
subsystem with the rest of the system may be quantified by the entanglement entropy SA ,
defined as the von Neumann entropy
SA = − tr ρA log ρA

(2.1)

of the density matrix ρA .
Since the reduced density matrix ρA is both hermitian and positive (semi)definite, it
can be expressed as
e−HA
,
(2.2)
ρA =
tr(e−HA )
where the Hermitian operator HA is known as the modular Hamiltonian. The denominator
is included on the right in the expression above to ensure that the reduced density matrix
has unit trace. Note the eq. (2.2) only defines HA up to an additive constant.
Now, consider any infinitesimal variation to the state of the system. The first order
variation4 of the entanglement entropy (2.1) is given by
(
)
δSA = − tr(δρA log ρA ) − tr ρA ρ−1
A δρA
= tr(δρA HA ) − tr(δρA ) .

(2.3)

Since the the trace of the reduced density matrix equals one by definition, we must have
tr(δρA ) = 0. Hence, the variation of the entanglement entropy obeys
δSA = δ⟨HA ⟩ ,

(2.4)

where HA is the modular Hamiltonian associated with the original unperturbed state.
4

Here and below, the variations are defined by considering a one-parameter family of states |Ψ(λ)⟩ such
that |Ψ(0)⟩ = |0⟩. The variation δO of any quantity associated with |Ψ⟩ is then defined by δO = ∂λ O(λ)|λ=0 .

–5–

JHEP03(2014)051

In this section, we review some basic facts about entanglement entropy, modular Hamiltonians and their holographic interpretation. In section 2.1, following [17], we review the
first law-like relation δSA = δ⟨HA ⟩ satisfied by entanglement entropy, specializing to entanglement for ball-shaped regions in a conformal field theory in section 2.2. In section 2.3,
we review the bulk interpretation of SA and ⟨HA ⟩ in a holographic CFT.

## PDF page 7

D
d-1

B

H

In cases where we start with a thermal state ρA = e−βH / tr(e−βH ), equation (2.4) gives
δ⟨H⟩ = T δSA , an exact quantum version of the first law of thermodynamics. Thus, (2.4)
represents a generalization of the first law of thermodynamics valid for arbitrary perturbations to arbitrary (non-equilibrium) states.
2.2

The first law in conformal field theories

We now specialize to the case of local quantum field theories. Here, for any fixed Cauchy
surface, the field configurations on this time slice are representative of the Hilbert space
of the underlying quantum theory. We can then define a subsystem A by introducing
a smooth boundary or ‘entangling surface’, which divides the Cauchy surface into two
separate regions, A and Ā; the local fields in the region A define a subsystem.
In general, the relation (2.4) is of limited use. For a general quantum field theory, a
general state, and a general region A, the modular Hamiltonian is not known and there is
no known practical method to compute it. Typically, HA is expected to be a complicated
non-local operator. However, there are a few situations where the modular Hamiltonian
has been established to have a simple form as the integral of a local operator, and in which
it generates a simple geometric flow.
One example is when we consider a conformal field theory in its vacuum state, ρtotal =
|0⟩⟨0| in d-dimensional Minkowski space, and choose the region A to be a ball B(R, x0 )
of radius R on a time slice t = t0 and centered at xi = xi0 .5 For this particular case, the
modular Hamiltonian takes the simple form [24, 30]
∫
R2 − |⃗x − ⃗x0 |2
dd−1 x
HB = 2π
Ttt (t0 , ⃗x) ,
(2.5)
2R
B(R,x0 )
where Tµν is the stress tensor.
5

Our notation for the flat space coordinates will be xµ = (t, ⃗x) or (t, xi ) where i = 1 . . . d − 1, while
x = (z, t, ⃗x) denotes a coordinate on AdSd+1 .
a

–6–

JHEP03(2014)051

Figure 1. Causal development D (left) of a ball-shaped region B on a spatial slice of Minkowski
space, showing the evolution generated by HB . A conformal transformation maps D to a hyperbolic
cylinder H d−1 × time (right), taking HB to the ordinary Hamiltonian for the CFT on H d−1 .

## PDF page 8

ζB =

iπ 2
(R Pt + Kt )
R

(2.6)

where
iPt = ∂t ,

and

iKt = −[(t − t0 )2 + |⃗x − ⃗x0 |2 ]∂t − 2(t − t0 )(xi − xi0 )∂i .

(2.7)

It is straightforward to check that ζB generates a flow which remains entirely in D, acting
as a null flow on ∂D and vanishing on the sphere ∂B(R, x0 ) and at the future and past
tips of D. The generator of this flow in the underlying CFT may be written covariantly as
∫
ν
dΣµ Tµν ζB
(2.8)
HB =
S

where dΣµ is the volume-form on the (d − 1)-dimensional surface S. The integral may be
evaluated on any spatial surface S within the causal diamond D whose boundary is ∂B, but
for the particular choice S = B(R, x0 ), we recover (2.5). Note that the normalization of the
conformal Killing vector ζB was chosen in (2.6) to ensure that modular Hamiltonian HB
and the Hamiltonian on the hyperbolic cylinder Hτ are related by HB = 2πR U0 Hτ U0−1
where U0 is the unitary transformation which implements the conformal mapping between
the two backgrounds [24].
In summary, starting from the vacuum state of any conformal field theory and considering a ball-shaped region B, the first law (2.4) simplifies to
δSB = δEB ,
where we define
EB ≡ 2π

∫

dd−1 x
B(R,x0 )

R2 − |⃗x − ⃗x0 |2
⟨Ttt (t0 , ⃗x)⟩ .
2R

6

(2.9)

(2.10)

The causal development D of the ball (also known as the domain of dependence) comprises all points
p for which all causal curves through p necessarily intersect B(R, ⃗x0 ).

–7–

JHEP03(2014)051

To understand the origin of this expression, we recall that the causal development6 D
of B is related by a conformal transformation to a hyperbolic cylinder H = H d−1 × Rτ
(time) as shown in figure 1. As argued in [24], this transformation induces a map of
CFT states that takes the vacuum density matrix on B to the thermal density matrix
ρH ∼ exp(−2πRHτ ) for the CFT on hyperbolic space, where R is the curvature radius of
the hyperbolic space and Hτ is the CFT Hamiltonian generating time translations in H.
The modular Hamiltonian for ρH is then just 2πRHτ . Going back to D, it follows that
the modular Hamiltonian for the density matrix ρB is the Hamiltonian which generates
the image under the inverse conformal transformation of these time translations back in
D, shown on the left in figure 1.
To obtain the explicit expression (2.5), we define ζB to be the image of the Killing
vector 2πR ∂τ under the inverse conformal transformation. This is a conformal Killing
vector on the original Minkowski space which can be written as a combination of a time
translation Pt and a certain special conformal transformation Kt ,

## PDF page 9

2.3

Interpretation of the first law in holographic CFTs

2.3.1

Holographic interpretation of the entanglement entropy

The holographic prescription for computing the entanglement entropy is not known in
general, but in the known cases (e.g., [1, 2, 25, 32–38]), it is given by extremizing a certain
functional of the bulk metric over codimension-two bulk surfaces whose boundary coincides
with ∂A in the boundary CFT. However, here we are only interested in the holographic
entanglement entropy for a ball-shaped region B in the CFT when the total state is the
vacuum or a small perturbation thereof. This particular case is well-understood due to the
observation of [24], reviewed in the previous section, that the vacuum density matrix for B
maps by a conformal transformation to a thermal state of the CFT on hyperbolic space.
Using the AdS/CFT correspondence, the thermal state of the CFT on hyperbolic space
1
is dual to a hyperbolic ‘black hole’ spacetime at this temperature,
at temperature T = 2πR
i.e., AdS-Rindler space, with metric
ds2 = −

ρ2 − ℓ 2 2
ℓ2 dρ2
dτ
+
+ ρ2 (du2 + sinh2 u dΩ2d−2 ) .
R2
ρ2 − ℓ 2

(2.11)

The entanglement entropy for the region B equals the thermal entropy of the hyperbolic
space CFT, which can be interpreted as the entropy of this ‘black hole.’ In an arbitrary
theory of gravity, black hole entropy is computed by evaluating the Wald functional (1.5)
on the horizon. In terms of the Poincaré coordinates on AdS space
ds2 =

)
ℓ2 ( 2
dz + ηµν dxµ dxν ,
2
z

(2.12)

the hyperbolic ‘black hole’ associated with the ball B(R, x0 ) is simply the wedge shown
in figure 2, the intersection of the causal past and the casual future of the region D on
the boundary. The coordinate transformation between the two metrics is described in [24].
7

More precisely, the states that we will consider have energy of order ε cT , where cT is the central charge
of the boundary CFT (e.g. see [31]) which provides a measure of the number of degrees of freedom in the
CFT. Since we consider classical gravity in the bulk, cT → ∞; we take ε ≪ 1 in order for the perturbation
to be classical, but small. The first law relation also holds for quantum states in the bulk, whose CFT
energy does not scale with cT , but we will not consider them in this article.

–8–

JHEP03(2014)051

The first law (2.4) reviewed in the previous section is a general result. Hence for ballshaped regions in an arbitrary CFT in any number of spacetime dimensions, δSB = δEB
with EB defined in eq. (2.10). We will be interested in understanding this relation for
holographic CFT’s with a classical bulk dual, i.e. theories for which at least a subset of the
states have a dual interpretation as smooth, asymptotically AdS field configurations. In
this case, the vacuum state of the boundary CFT corresponds to pure anti-de Sitter space,
while certain small perturbations around the vacuum state should correspond to spacetime
geometries that are small perturbations around empty AdS.7 In holographic theories, both
SB and EB should match with observables on the gravity side, so δSB = δEB will translate
grav
grav
that must be satisfied for any spacetime dual to a small
into a constraint δSB
= δEB
perturbation of the vacuum AdS spacetime.

## PDF page 10

Σ

~
B

Figure 2. AdS-Rindler patch associated with a ball B(R, x0 ) on a spatial slice of the boundary.
Solid blue paths indicate the boundary flow associated with HB and the conformal Killing vector
ζ. Dashed red paths indicate the action of the Killing vector ξ.

The horizon slice approached with ρ → ℓ and τ fixed in the black hole metric (2.11)
corresponds to the hemisphere B̃ = {t = t0 , (xi − xi0 )2 + z 2 = R2 } in Poincaré coordinates.
By design [24], this is also the extremal surface in AdS bulk with boundary ∂B. Thus,
the entanglement entropy SB for the vacuum state can be calculated gravitationally by
evaluating the Wald functional (1.5) on the surface B̃.
If we consider a perturbation of the original vacuum state, the perturbation of the
entanglement entropy must equal the perturbation of the thermal entropy of the CFT on
the hyperbolic cylinder. Assuming that this equals the perturbation to the black hole
grav
Wald . In general, the entanglement entropy
entropy, we must also have that δSB
= δSB
functional is known to differ from the Wald functional [34–37, 39] by terms quadratic in the
extrinsic curvature of the extremal bulk surface. These terms are important for arbitrarilyshaped entangling surfaces or general states in the CFT. However, for the special case of a
spherical entangling surface considered here and a CFT in the vacuum, the extremal surface
B̃ in the bulk is the bifurcation surface of the Killing horizon defining the boundary of the
grav
AdS-Rindler patch and the extrinsic curvatures of this surface vanish. Therefore, δSB
Wald are equal at linear order in the perturbations we are considering.8
and δSB
8

Further, note that in the perturbed spacetime, the extremal surface will not necessarily correspond to
the bifurcation surface of the AdS-Rindler horizon. However, since B̃ is an extremal surface for the Wald
functional, changes in the Wald functional due to variations in the surface come in only at second order in

–9–

JHEP03(2014)051

B

## PDF page 11

grav
To summarize, the holographic dictionary implies that SB
for a small perturbation
around AdS is the Wald functional of the perturbed metric evaluated on B̃.

2.3.2

Holographic interpretation of the modular energy EB

grav
EB
=

∫

µ

dΣ
S

grav ν
Tµν
ζB = 2π

∫

dd−1 x
B(R,⃗
x0 )

R2 − |⃗x − ⃗x0 |2 grav
Ttt (t0 , ⃗x)
2R

(2.13)

grav
giving EB
as an integral of a local functional of the asymptotic metric over the region
B(R, x0 ) at the AdS boundary.
As discussed above, EB is the conserved quantity associated with the boundary conformal Killing vector ζB . An alternate definition [28] of the gravitational quantity associated
with this is as the canonical conserved charge associated to translations along a bulk asymptotic Killing vector ξB that asymptotically agrees with ζB , limz→0 ξB = ζB . We review this
grav
[ξB ] in section 5 below and show in section 5.3 that it agrees with (2.13)
definition EB
(at least for the perturbations we are considering). Thus, for perturbations to the vacuum
grav
can be interpreted as the perturbation to the energy of the AdS-Rindler patch
state, EB
associated with the region B, as in figure 2.
Note that under the conformal map from D to H, the conserved charge associated
to ζB maps to (2πR times) the energy associated to τ translations, computed using
either formalism.

2.3.3

Summary

In summary, for states of a holographic CFT with a classical gravity dual description, the
CFT relation δSB = δEB translates to a statement that the integral of the Wald functional
over the bulk surface B̃ must equal the integral of the energy functional, as given in (2.13),
over the boundary surface B. This provides one nonlocal constraint on the metric for each
ball B in each Lorentz frame. The constraints may be interpreted as the statement that
the perturbation to the entropy of the AdS-Rindler patch associated with the region B
equals the perturbation to the energy.
the metric perturbation. To calculate the Wald functional at leading order in the metric perturbation, we
Wald
therefore need only evaluate δSB
on B̃, the bifurcation surface of the unperturbed AdS-Rindler horizon.
9
Other fields in the bulk may also contribute to the holographic stress tensor (e.g. a bilinear of gauge
fields when d = 2), but their contributions are always nonlinear in the fields and vanish at the linearized
order around pure AdS that we are considering.

– 10 –

JHEP03(2014)051

In the CFT, the expression (2.10) defines EB in terms of the expectation value of the field
theory stress energy tensor. On the gravity side, the latter is computed by the “holographic
grav
stress tensor” Tµν
, a quantity constructed locally from the asymptotic metric.9 For
grav
a general theory, Tµν can be obtained via a systematic procedure known as holographic
grav
can be
renormalization [40–45]. Alternatively, as we show in sections 4.1 and 6 below, Tµν
derived using the holographic entanglement entropy function and the relation δSB = δEB .
The gravitational version of EB is simply obtained by replacing the stress tensor expectation value in (2.8) or (2.10) with the holographic stress tensor

## PDF page 12

3

The holographic first law of entanglement from the first law of black
hole thermodynamics

grav
grav
In this section, we will verify that δSB
= δEB
follows from the equations of motion
in a general theory of gravity. The crucial observation, described in the previous section,
is that this gravitational relation can be interpreted as a statement of the equivalence
of energy and entropy for perturbations of AdS-Rindler space. This equivalence follows
directly from the generalized first law of black hole thermodynamics proved by Iyer and
Wald [46].

The Iyer-Wald theorem states that for a stationary spacetime with a bifurcate Killing
κ
δSWald =
horizon generated by a Killing vector ξ, arbitrary on-shell perturbations satisfy 2π
δE[ξ]. Here SWald is the Wald entropy defined in the introduction, E[ξ] is a canonical energy
associated to the Killing vector ξ and κ is the surface gravity: ξ a ∇a ξ b = κ ξ b on the horizon.
The key observation that connects this to our holographic version of the entanglement
first law is that the Iyer-Wald theorem applies to AdS-Rindler horizons. It is straightforward to check that the vector
ξB = −

2π
π
(t − t0 )[z∂z + (xi − xi0 )∂i ] + [R2 − z 2 − (t − t0 )2 − (⃗x − x⃗0 )2 ] ∂t
R
R

(3.1)

is an exact Killing vector of the standard Poincaré metric (2.12), which vanishes on
B̃(R, ⃗x0 ). This vector is in fact proportional to ∂τ in the AdS-Rindler coordinates (2.11).
Thus, the hemisphere B̃ is the bifurcation surface of the Killing horizon for ξB and the
region Σ(R, ⃗x0 ) enclosed by B̃ and B is a spacelike slice that plays the role of the black
hole exterior. The Iyer-Wald theorem applies, and the Killing vector has been normalized
Wald = δE [ξ ].
such that κ = 2π, so δSB
B B
The definition of modular energy entering the above equality is the Iyer-Wald one; we
grav
show in section 5.3 that this quantity agrees with δEB
defined in terms of the holographic
grav
Wald , and therefore
stress tensor. Finally, we argued in the previous section that δSB
= δSB
grav
grav
it follows that δSB
= δEB
. This generalizes the result of [17] to an arbitrary higherderivative theory of gravity.

– 11 –

JHEP03(2014)051

In holographic CFTs, whenever the gravitational observables corresponding to SB and EB
are known, the first law of entanglement entropy (2.4) applied to a ball, i.e. δSB = δEB ,
grav
gives a prediction for the equivalence of two corresponding gravitational quantities, δSB
grav
and δEB
, in any spacetime dual to a small perturbation of the CFT vacuum state. This
prediction must hold assuming the validity of the AdS/CFT correspondence and of our
holographic interpretation of EB and SB . As we will see in the next section, the power
of this equivalence arises because in fact, we have an infinite number of predictions since
δSB = δEB can be applied for any ball-shaped region in any Lorentz frame in the boundary
geometry. For the case of Einstein gravity, where entanglement entropy is calculated by
grav
grav
the Ryu-Takayanagi proposal [1–4], the equivalence of δSB
and δEB
was confirmed
in [17], and by a different method in [16].

## PDF page 13

4

Linearized gravity from the holographic first law

4.1

The holographic stress tensor from the holographic entanglement functional

To begin, we show that given the holographic prescription for computing entanglement
entropy, the equation δSB = δEB applied to ball-shaped regions of vanishing size can be
used to determine the relation between the expectation value of the field theory stress
tensor and the asymptotic metric in the dual spacetime.
Recall the result (2.10),
∫
R2 − |⃗x − ⃗x0 |2
δ⟨Ttt (t0 , ⃗x)⟩ .
(4.1)
dd−1 x
δEB(R,x0 ) = 2π
2R
B(R,x0 )
In the limit of a very small spherical region, i.e. R → 0, the expectation value of
the stress tensor is approximately constant throughout the ball B(R, x0 ). Thus, the
leading contribution to δEB is obtained by replacing δ⟨Ttt (t0 , ⃗x)⟩ with its central value
δ⟨Ttt (t0 , ⃗x0 )⟩ ≡ δ⟨Ttt (x0 )⟩, which yields
∫
R2 − ⃗x2
2πRd Ωd−2
R→0
dd−1 x
δEB(R,x0 ) −−−→ 2π δ⟨Ttt (x0 )⟩
=
δ⟨Ttt (x0 )⟩
(4.2)
2R
d2 − 1
|x|≤R
where Ωd−2 is the volume of a unit (d − 2)-sphere. Now using the CFT relation δEB = δSB ,
we find
(
)
d2 − 1
1
δ⟨Ttt (x0 )⟩ =
lim
δS
.
(4.3)
2π Ωd−2 R→0 Rd B(R,x0 )

– 12 –

JHEP03(2014)051

In the previous section, making use of the theorem of Iyer and Wald [46], we argued that in
a general theory of gravity, any perturbation to AdS satisfying the linearized gravitational
grav
equations will obey the holographic version of the entanglement first law, i.e. δSB
=
grav
δEB
. In this section, we will demonstrate a converse statement: any asymptotically AdS
grav
grav
spacetime for which δSB
= δEB
for all balls B in all Lorentz frames must satisfy the
linearized gravitational equations and have the appropriate boundary conditions at the
asymptotic boundary.
grav
grav
We begin in section 4.1 by showing that δSB
= δEB
applied to infinitesimal ballshaped regions allows us to determine the holographic stress tensor in a general theory of
gravity and to constrain the asymptotic behavior of the metric. In section 4.3, we explain
grav
grav
how δSB
= δEB
, when applied to balls of arbitrary radius and centered at arbitrary
locations in arbitrary Lorentz frames, can be used to deduce the linearized gravitational
equations of motion, generalizing the results of [16]. Since we have already argued in secgrav
grav
= δEB
, it follows that the holographic
tion 3 that these equations of motion imply δSB
version of the entanglement first law is equivalent to the linearized gravitational equations
in general theories of gravity.
In situations where the metric perturbation is the only field turned on in the bulk,
the asymptotic behavior of the metric together with the linearized equations of motion
determine the metric perturbation everywhere. In this case, knowledge of the entanglement
functional allows us to recover the complete mapping from states to dual spacetimes at the
linearized level.

## PDF page 14

The meaning of this equation is the following: SB is a bulk Wald functional that depends
on a small metric perturbation hab , as well as the radius R and center x0 of the entangling
surface. The above equation tells us that SB [h]/Rd cannot be arbitrary, but rather it must
have a finite limit as R → 0.
Repeating the same calculation for a frame of reference defined by some proper dvelocity uµ , we find
(
)
d2 − 1
1
(u)
µ ν
u u δ⟨Tµν (x0 )⟩ =
lim
δS
,
(4.4)
2πΩd−2 R→0 Rd B(R,x0 )

Example: theories with entropy equal to area
As an example, consider a d-dimensional field theory for which the entanglement entropy
is computed by the Ryu-Takayanagi prescription [1, 2] in the dual (d + 1)-dimensional bulk
grav
SB
=

AB̃
.
4GN

(4.5)

We consider a small metric perturbation hab of the AdS metric (2.12), chosen to be in
radial gauge,
hzµ = hzz = 0 .
(4.6)
The change in the entanglement entropy of the ball due to this bulk perturbation is
(
)
∫
1 i
Rℓd−3
grav
j
ij
d−1
2−d
i
j
δ − 2 (x − x0 )(x − x0 ) hij (z, t0 , ⃗x) .
d xz
(4.7)
δSB =
8GN |⃗x−⃗x0 |≤R
R
In the limit R → 0, we can replace hij (z, xµ ) by hij (z, xµ0 ) under the integral sign. To
compute the R-scaling of the entropy and check whether it can satisfy (4.3), it is useful to
define the rescaled variables
z
xi − xi0
,
ẑ =
(4.8)
x̂i =
R
R
which are to be kept fixed as R → 0. Then, the only way that (4.7) has a finite limit as
R → 0 is if
z→0
λ
hµν (z, xλ0 ) −−−−→ z d−2 h(d)
(4.9)
µν (x0 )
(d)

where hµν does not scale with R. Performing the xi integral and substituting into (4.3),
we find
dℓd−3 (d)i
δ⟨Ttt ⟩ =
h i.
(4.10)
16πGN
In order to generalize this result to an arbitrary Lorentz frame as in (4.4), it is useful to
(d)
(d)λ
rewrite h(d)i i = h00 − η00 hλ . Passing to an arbitrary frame and equating the coefficients
of uµ uν , we find
dℓd−3 (d)
(d)λ
(hµν − ηµν hλ ) .
(4.11)
δ⟨Tµν ⟩ =
16πGN

– 13 –

JHEP03(2014)051

(u)

where δSB(R,x0 ) is the variation of the entanglement entropy for a ball of radius R, centered
at x0 on a spatial slice in the frame of reference of an observer moving with the d-velocity
uµ . From the result (4.4), it is clear that given the bulk prescription for calculating δSB ,
this formula provides us the holographic dictionary for the stress tensor.

## PDF page 15

Now tracelessness and conservation of the CFT stress tensor imply that this leading perturbation of the bulk metric must satisfy
h(d)µ
=0,
µ

∂µ h(d)µν = 0 .

(4.12)

These equations correspond to the initial value constraints on the z = 0 surface in Einstein
gravity. Applying the tracelessness condition allows the stress tensor to be simplified to
grav
δ⟨Tµν ⟩ ≡ δTµν
=

dℓd−3 (d)
h
.
16πGN µν

(4.13)

4.2

The linearized Fefferman-Graham expansion

We have just shown how the R → 0 limit of the first law relation constrains the leading
behavior of the metric for small z and determines the holographic stress tensor. By equatgrav
grav
ing terms at higher orders in the expansion of δSB(R,x
= δEB(R,x
in powers of R, we
0)
0)
can obtain additional constraints on the metric. At each higher order in R, the equations
involve successively higher terms in the Fefferman-Graham expansion of the metric (i.e. the
expansion in powers of z). In [16], it was shown, for theories with holographic entanglement entropy computed by area, that these constraints completely determine the linearized
metric to all orders in the Fefferman-Graham expansion. At the linearized level, this gives
the complete metric perturbation everywhere in the bulk, and the result is precisely the
solution to the linearized Einstein’s equations with boundary behavior governed by the
holographic stress tensor.
While we could apply the same approach to more general theories of gravity, we will
instead take another route that leads to the full equations of motion without having to
assume a series expansion for the quantities in the first law relation.
4.3

Linearized equations from the holographic entanglement functional

In this section, we will show that knowledge of the holographic entanglement functional
allows us to deduce the linearized gravitational equations for the entire dual spacetime, by
making use of the relation δSB = δEB for ball shaped regions B(R, x0 ) of arbitrary radius
R and center position xµ0 in arbitrary Lorentz frames.
Figure 3 shows the unperturbed bulk AdS spacetime, with the region B(R, x0 ) on the
boundary, together with the bulk extremal surface B̃(R, x0 ) with the same boundary as B
(d)

10

This result can understood using conformal invariance, since hµν is the only spin-2 tensor that we can
write down with scaling dimension d under z → λz. Here we are assuming that there are no scalar fields,
coupled linearly to curvature, with mass tuned so that the conformal dimension of the dual operators is
∆ = d, and similarly for other matter fields.

– 14 –

JHEP03(2014)051

Of course, this expression is the usual result for the linearized holographic stress tensor in
Einstein gravity in AdSd+1 [40–44].
In section 5.3 we show, using a scaling argument, that even in the presence of higher
(d)
derivative terms, the CFT stress tensor Tµν ∝ hµν , but with a non-trivial coefficient that
depends on the higher curvature couplings10 — see also section 6.

## PDF page 16

t
z

x

R

x0

Σ

~
B

B

and the spatial region Σ on a constant time slice bounded by these two surfaces. Using
the definition (2.13) and the result (4.4) for the holographic stress tensor, we can write
grav
the quantity δEB
as an integral over the corresponding region B(R, x0 ) on the boundary
of the dual spacetime of some local quantity, a (d − 1)-form, that is constructed from the
asymptotic limit of the metric perturbation hab .
In a similar way, the holographic entanglement functional gives us a prescription for
writing the entanglement entropy δSB as an integral over the extremal surface B̃(R, x0 )
in the bulk (shown in figure 2). Again, the form that we integrate is locally constructed
grav
grav
from the metric perturbation hab (and possibly matter fields). The relation δSB
= δEB
grav
then places a constraint on the perturbation: the two integrals corresponding to δEB and
grav
δSB
must be equal. This must be true for any R and xµ0 , in any Lorentz frame. We will
show that this infinite set of nonlocal integral equations together implies the local differg
g
ential equations δEab
= 0, where δEab
are the linearized gravitational equations of motion.
Turning the nonlocal constraint into a local equation
To convert the nonlocal integral equations into a local equation, the strategy is to make
use of the machinery used by Iyer and Wald to derive the first law from the equations of
motion. The Iyer-Wald formalism is reviewed in detail in the next section, but for now we
just need one fact: the crucial step in the derivation is the construction of a (d − 1)-form
χ that satisfies
∫
∫
grav
grav
(4.14)
χ = δEB
χ = δSB
B

B̃

and for which dχ = 0 on shell (i.e. when the gravitational equations of motion are satisfied).
∫
The first law follows immediately by writing Σ dχ = 0 and applying Stokes theorem (i.e.
integrating by parts).

– 15 –

JHEP03(2014)051

Figure 3. Notation for regions in AdSd+1 , with radial coordinate z and boundary space coordinate
⃗x. B(R, x0 ) is the (d − 1)-dimensional ball on the z = 0 boundary of radius R centered at ⃗x0 on
the spatial slice at time t0 . B̃ is the (d − 1)-dimensional hemispherical surface in AdS ending on
∂B, and Σ is the enclosed d-dimensional spatial region.

## PDF page 17

To derive local equations from the gravitational first law, we will show that there exists
a form χ which satisfies the relations (4.14) off shell, and whose derivative is
g b
a
dχ = −2ξB
δEab
ε

(4.15)

where the d-form εb is the natural volume form on co-dimension one surfaces in the bulk
g
(defined in eq. (5.3)), ξB is the Killing vector (3.1) that vanishes on B̃(R, x0 ), and δEab
are the linearized gravitational equations of motion. In addition, we will require that
dχ|∂M = 0

(4.16)

B̃

Σ

∂Σ

B

Σ

Multiplying this result by R and then taking the derivative with respect to R, we obtain
∫
∫
g t
g
t
t
(RξB ) δEtt r̂ · ε + 2πR
δEtt
ε =0.
(4.18)
Σ

B̃

The first term vanishes because ξB = 0 on B̃, so we find that
∫
g t
δEtt
ε =0

(4.19)

Σ

for any Σ(R, ⃗x0 ). As we show in appendix A, this implies that the integrand vanishes
g
everywhere, i.e. δEtt
= 0, as we wished to show.
So far we have used the first law for every ball B(R, ⃗x0 ) in a spatial slice at fixed t.
grav
grav
More generally, demanding δSB
= δEB
in a frame of reference defined by a d-velocity
g
µ
µ
ν
vector u implies u u δEµν = 0, where the index µ = 0, . . . , d − 1 runs over the boundary
coordinates. Since this holds for any uµ , we have
g
δEµν
=0.

(4.20)

These are all the components of the gravitational equations of motion along the boundary directions.
g
g
= 0 and δEzz
= 0, we appeal to the initial
To obtain the remaining equations δEzµ
value formulation of gravity, in a radial slicing where these are the constraint equations.
11

This in turn follows from the conservation and tracelessness of the CFT stress tensor.

– 16 –

JHEP03(2014)051

where ∂M is the AdS boundary, assuming the tracelessness and conservation of the holograv
does not depend on the surface
graphic stress tensor.11 This ensures that the energy EB
S on the boundary that we use to evaluate it, as long as ∂S = ∂B. Note that on Σ,
a and εb are non-vanishing, so only the tt component of the
only the time components of ξB
gravitational equations appears on the right-hand side of eq. (4.15).
The derivation of these statements in a general theory of gravity relies on the Iyer-Wald
formalism [46] and is deferred to section 5. Now we will show that the existence of the form
grav
grav
= δEB
gives
χ with these properties implies the equations of motion. The relation δSB
∫
∫
∫
∫
∫
g t
grav
grav
t
dχ = −2 ξB
δEtt
ε .
(4.17)
χ=
0 = δSB
− δEB
=
χ−
χ=

## PDF page 18

This formulation guarantees that if these constraints are satisfied at z = 0, and the other
equations (4.20) hold everywhere, then the constraints hold for all z.12 The vanishing of
the constraints at z = 0 follows from eq. (4.16) combined with eq. (4.15), or ultimately
from the conservation and tracelessness of the holographic stress tensor.
In detail, we have using the Noether identity (discussed in appendix B) linearized
about the AdS background,
∇a (δE g )ab = 0 .
(4.21)
g
Using the vanishing of Eµν
, the general solution to (4.21) can be written as:

1
g
δEzz
= z d−2 Cz − z d ∂µ C µ ,
2

(4.22)

for unfixed Cµ , Cz which are functions of the boundary coordinates. We simply need to
show that Cµ , Cz must vanish. This is achieved by the requirement (4.16) which (using
eq. (4.15) and (4.22)) gives:
(
)
µ
z
0 = dχ|∂M = − ζB
Cµ + ζ̃B
Cz dt ∧ dx1 . . . ∧ dxd−1 .
(4.23)

z ≡ lim
−1 z
−1
Here, we have defined ζ̃B
z→0 (z ξB ) = −2πR (t − t0 ) which is related to the
z . Since it is possible
boundary conformal Killing vector via: ∂µ (ζB )ν + ∂ν (ζB )µ = 2ηµν ζ̃B
to construct χ for all possible boundary regions B and in all Lorentz frames, it follows
that Cµ = Cz = 0.
In summary, we can obtain the full set of linearized gravitational equations, if we can
show that a form χ exists, which satisfies eqs. (4.14), (4.15) and (4.16). We do this in
section 5.

Example: linearized Einstein equations from S = A/4GN
In section 5, we will prove that χ exists in a general theory, but we first give the explicit
formula for Einstein gravity without introducing any additional formalism. Consider the
case of a holographic CFT for which the field theory entanglement entropy of a region A
is equal to one quarter the area of the bulk extremal-area surface with boundary ∂A. In
this case, writing the metric perturbation as hµν = z d−2 Hµν , we are looking for a form
χ whose exterior derivative, restricted to Σ, is proportional to the tt component of the
Einstein equation, and which satisfies
∫
∫
d
grav
χ = δEB =
dd−1 x (R2 − |⃗x − ⃗x0 |2 ) H i i
(4.24)
16G
R
N
B
B
and

∫

B̃

grav
χ = δSB
=

ℓd−3
8GN R

∫

B̃

dd−1 x(R2 H i i − (x − x0 )i (x − x0 )j Hij ) .

(4.25)

grav
Here, we have used eqs. (2.10) and (4.13) to write an explicit expression for δEB
, making
grav
i
ij
use of (4.12) to replace Htt with H i = δ Hij . The expression for δSB was taken
from [16, 17].
12

In Einstein gravity, this follows from the Bianchi identity by a standard argument [47].

– 17 –

JHEP03(2014)051

g
δEzµ
= z d−1 Cµ ,

## PDF page 19

A form χ that satisfies the above requirements is
χ=−

]
1 [
b
b
δ(∇a ξB
εab ) + ξB
εab (∇c hac − ∇a hc c )
16πGN

(4.26)

where εab is defined in eq. (5.3). The restriction of χ to Σ is

π
where ξ t = R
(R2 − z 2 − |⃗x − ⃗x0 |2 ). Using this expression, it is straightforward to verify
eqs. (4.24) and (4.25), and also check that
g t
dχ|Σ = −2ξ t δEtt
ε

(4.28)

where
z d ℓ2−d
g
δEtt
=−

)
(
d+1
i
j i
i j
2 i
∂z H i + ∂j ∂ H i − ∂ ∂ Hij
∂z H i +
32πGN
z

(4.29)

is the (tt)-component of the linearized Einstein equations.13 Conservation dχ|∂M = 0 follows from the conservation and tracelessness of the CFT stress tensor, so the other compog
nents of the Einstein equations δEab
= 0 are also satisfied by the argument above.14 Thus,
for theories where the Ryu-Takayanagi area formula computes entanglement entropies, the
grav
grav
= δEB
are equivalent to the linearized Einstein equations.
non-local equations δSB

5

Linearized equations in general theories of gravity

In this section, we review the formalism used by Iyer and Wald to prove a version of the
first law of black hole thermodynamics in general theories of gravity (section 5.1), and
apply it in section 5.2 to construct a form χ with the properties outlined in section 4.3.
We also argue in section 5.3 that the energy for a perturbed AdS-Rindler spacetime as
defined by Iyer and Wald is equivalent to the energy defined using the holographic stress
tensor in eq. (2.10).
5.1

The covariant formalism for entropy and conserved charges

We begin by introducing notation and setting up the Iyer-Wald formalism [26, 28]. A
helpful general discussion motivating this formalism can be found in [48].
√
g
Here, Eab
is defined by varying the action with respect to g ab and dividing by −g, as usual.
g
14
For the case of Einstein gravity, we have δEzz ∝ H µ µ and δEzµ
∝ ∂µ H µ ν − ∂ν H µ µ = 0 so the vanishing
of these expressions at z = 0 follows immediately from the tracelessness and conservation of the holographic
stress tensor, using (4.13).
13

– 18 –

JHEP03(2014)051

{ [(
)
]
2πz d t
zd
t
t
i
εz
+ ξ + ξ ∂z H i +
χ|Σ =
(4.27)
16πGN
R
z
)
]}
[(
(
)
2π(xi − xi0 )
2π(xj − xj0 )
i
t i
j
t j
t
+ξ ∂ H j −
+ξ ∂ H j
+ε i
R
R

## PDF page 20

Basic definitions
Let L be any gravitational Lagrangian, viewed as a d + 1-form
L = Lε ,

(5.1)

where L is constructed from the metric, curvature tensors, and their covariant derivatives.
Here, ε is the volume form15
ε=

1
εa ···a dxa1 ∧ · · · ∧ dxad+1 .
(d + 1)! 1 d+1

(5.2)

εa =

1
εab ···b dxb2 ∧ · · · ∧ dxbd+1 ,
d! 2 d+1

εab =

1
εabc3 ···cd+1 dxc3 ∧ · · · ∧ dxcd+1 . (5.3)
(d − 1)!

Denoting the dynamical fields collectively by φ = {gµν , . . . }, the variation of L under a
general variation of the fields takes the form
δL = Eφ δφ + dΘ(δφ)

(5.4)

where Eφ = 0 are the equations of motion for the theory, and Θ is called the symplectic potential current.16 In the first term, a sum over fields φ with indices contracted appropriately
is implied.
Definition of Wald entropy from the Noether current
For a spacetime with a bifurcate Killing horizon associated to a Killing vector ξ, the Wald
entropy can be defined in terms of the Noether current associated with ξ, as we now review.
Starting with an arbitrary vector field ξ, the variation of the Lagrangian under a
diffeomorphism generated by ξ µ is
δξ L = d(ξ · L)

(5.5)

where the dot denotes the usual inner product of ξ µ with the form L.17 Since this represents
a local symmetry of a Lagrangian field theory, Noether’s theorem guarantees that we can
associate to it a current J µ [ξ] that is conserved when the equations of motion are satisfied.
This Noether current (expressed as a d-form) is given by
J[ξ] = Θ(δξ φ) − ξ · L .

(5.6)

Using eqs. (5.5) and (5.4), we can check that
dJ[ξ] = −Eφ δξ φ ,

(5.7)

so J is conserved on shell as promised.
√
Note that εa1 ···ad+1 is an antisymmetric tensor, and our sign convention is εzti1 ···id−1 = + −g .
16
This potential Θ, and similarly the Noether charge form Q below, have ambiguities related to boundary
terms in the Lagrangian and shifting by an exact form. Implicitly, these ambiguities, discussed in [27, 28],
have been fixed to simplify our formulae here but would not affect our arguments.
17
1
1
Na1 a2 ···an dxa1 ∧dxa2 ∧· · ·∧dxan , ξ·N = (n−1)!
ξ b Nba2 ···an dxa2 ∧· · ·∧dxan .
That is, given an n-form N = n!
15

– 19 –

JHEP03(2014)051

For later convenience, we also define:

## PDF page 21

Because eq. ( 5.7) holds for all vector fields ξ, it follows [49] that we can find a (d − 1)form Q such that
J[ξ] = dQ[ξ]

(on shell) .

(5.8)

Recalling that the Noether charge associated with the diffeomorphism ξ is the integral of J
over a spacelike hypersurface Σ, we see that the existence of Q (called the Noether charge
form) allows us to express this charge as an integral over the boundary of Σ.
As shown in [28], Q can be written as
abcd
Xcd = −ER
εab ,

(5.9)

abcd is the ‘equation of motion’ for the Riemann tensor, derived as if it were an
where ER
independent field in the Lagrangian:
abcd
ER
=

∂L
∂L
δL
≡
− ∇a 1
+ ··· .
δRabcd
∂Rabcd
∂∇a1Rabcd

(5.10)

eq. (5.8) only defines Q on shell. It is always possible to define Q off shell so that
J[ξ] = dQ[ξ] + ξ a Ca ,

(5.11)

where Ca are the constraint equations on a fixed-time slice. That is,
Ca =

∑
φ

[

r
∑
i=1

s
∑

c1 ···ci ···cr
s
(E φ )cb11 ···b
ε ci −
···a···cr φb1 ···bs

i ···bs c1 ···cr
(E φ )cb11 ···b
φb1 ···a···bs εbi
···cr

i=1

]

,

(5.12)

where φ is a type (r, s) tensor, and the dots indicate that the indices appear in the ith
position. This is shown in [46] and reviewed in appendix B. Note that only the equations
of motion of non-scalar fields appear in Ca .
In a spacetime with a bifurcate Killing horizon, the Wald entropy (1.5) is now defined as
SWald = 2π

∫

Xcd ncd ,

(5.13)

H

where H is the bifurcation surface and ncd is the binormal to H. This definition also applies
to linearized excitations of a stationary background. It is related to the Noether charge
as follows. Let ξ be the Killing vector that generates the horizon and vanishes on H. In
general, ∇[c ξd] = κ ncd on the horizon, where κ is the surface gravity. If we normalize ξ so
that κ = 2π, then the Wald entropy equals the Noether charge
SWald =

∫

Q[ξ] .

(5.14)

H

On the stationary background, this agrees with (5.13) because ξ = 0 on the bifurcation surface. It was argued in [26, 28] that eqs. (5.14) and (5.13) also agree for linearized excitations.

– 20 –

JHEP03(2014)051

Q[ξ] = Wc ξ c + Xcd ∇[c ξd] ,

## PDF page 22

Definition of energy
For perturbations of the background spacetime, we can define an energy canonically associated to a Killing vector ξ. Defining the symplectic current
ω (δ1 φ, δ2 φ) = δ2 Θ(δ1 φ) − δ1 Θ(δ2 φ) ,

(5.15)

ω (δφ, δξ φ) .

(5.16)

δJ[ξ] = δΘ(δξ φ) − ξ · dΘ(δφ)

(5.17)

δHW [ξ] =

C

This can be rewritten using

= ω (δξ φ, δφ) + d(ξ · Θ(δφ))

(5.18)

where we used the background equations of motion E φ = 0 and the formula for the Lie
derivative of a form,
δξ u ≡ Lξ u = ξ · du + d(ξ · u).
(5.19)
Therefore using eqs. (5.11) and (5.18), we have
∫
∫
a
δHW [ξ] = δ ξ Ca +
(δQ[ξ] − ξ · Θ(δφ)) .
C

(5.20)

∂C

Thus, H reduces to a boundary term when the equations of motion are satisfied. We
define the energy δE[ξ] for an arbitrary (i.e. not necessarily on-shell) perturbation of the
background spacetime as this contribution at the asymptotic boundary,18
∫
δE[ξ] =
(δQ[ξ] − ξ · Θ(δφ)) .
(5.21)
∂C

5.2

Definition of χ

Using the notation above, we can now define the form χ described in section 2.3 as
χ = δQ[ξB ] − ξB · Θ(δφ) .

(5.22)

As an example, the covariant formalism is applied to Einstein gravity plus a scalar field
in appendix C, leading to (4.26). In the rest of this section, we will demonstrate that χ
obeys the equations (4.14) and (4.15) that were needed to derive the equations of motion
grav
grav
. That χ also obeys eq. (4.16) will be shown in the next section. We
from δSB
= δEB
emphasize that it is the existence of a form χ with these properties that guarantees that
grav
grav
= δEB
. Thus, starting from
the linearized equations of motion are equivalent to δSB
only the entropy functional SWald , it should be possible to recover the linearized equations
even if we do not know χ, L, Θ, or Q.
18

As discussed in [28], this definition can be extended to general spacetimes with the same asymptotic
∫
∫
behavior provided that there exists a form B such that δ ∂C ξ · B = ∂C ξ · Θ. In this case, we can define
∫
E[ξ] = ∂C (Q[ξ] − ξ · B) .

– 21 –

JHEP03(2014)051

the Hamiltonian that generates translations along ξ µ is obtained by integrating ω over a
Cauchy surface C,
∫

## PDF page 23

The first property in eq. (4.14) follows directly from our definition (5.21) and the
equivalence of δE[ξB ] and δE grav , to be shown in the next section. The second property
follows from
∫
∫
grav
δSB
= δSWald =
δQ[ξB ] =
χ.
(5.23)
B̃

B̃

g b
a
a
dχ = δ(dQ[ξB ] − J[ξB ]) = −ξB
δCa = −2ξB
δEab
ε

(5.24)

g
where Eab
is the equation of motion derived by varying the action with respect to g ab .
Note that fields vanishing on the background do not contribute to the first variation of Ca ,
which is why our derivation always gives the gravitational equations rather than the some
combination of gravitational and matter equations.

5.3

Equivalence of the holographic and the canonical modular energy

For arbitrary perturbations to AdS, we now have two definitions of modular energy associated to a given boundary region B: the “canonical” energy (5.21)
∫
grav
(δQ[ξB ] − ξB · Θ(δφ))
(5.25)
δE(1) ≡ δE[ξB ] ≡
B

associated with the bulk Killing vector ξB that asymptotes to ζB , and the “holographic”
energy (2.10)
∫
grav
δE(2)
=

B

grav ν
dΣµ δTµν
ζB

(5.26)

defined in terms of the holographic stress tensor (4.13).
In order to complete our story, we must show that these two definitions of energy agree,
without assuming the equations of motion. This is not to say that the formulae agree for
arbitrary hµν — they do not. However, equivalence follows from the restrictions on the
grav
grav
asymptotic metric implied by δSB
= δE(2)
. Note that the purely gravitational result of
grav
grav
this paper — that the linearized equations of motion are equivalent to δSB
= δE(1)
—
does not require the results of this subsection; it is needed only to map the CFT problem
to the gravity problem.
Consistency of the AdS/CFT dictionary requires the two definitions to agree, since
both should equal the CFT energy. This is confirmed for Einstein gravity in [50, 51], and
rather generally in [52], but these discussions rely on the equations of motion. Here we will
demonstrate the equivalence explicitly, at the linearized level, in a way that makes clear
that we do not need to start from the equations of motion. For simplicity, we assume in
this calculation that matter fields are not coupled to curvature, so only the metric appears
in the linearized energy.

– 22 –

JHEP03(2014)051

The first equality was discussed in section 2.3, the third equality follows from the definition
of χ since ξB vanishes on B̃, and the second equality was proved in [46], as discussed in
the previous section. The proof in [46] does not use the equations of motion, so it holds
off shell if we define the entropy as in eq. (5.13).
To show eq. (4.15) note that for ξ a Killing vector of the background, eq. (5.18) implies
δJ[ξ] = d(ξ · Θ). Therefore

## PDF page 24

As we discussed in section 4.1 and will show in more detail in section 6, metric perturbations for which the first law is satisfied at leading order in the R expansion behave near
the boundary as
hµν = z d−2 h(d)
(5.27)
µν + . . .
grav
where the dots indicate terms at higher order in z. Other fall-offs, with δSB
= 0, are
also allowed; these are addressed below. The holographic stress tensor is proportional to
(d)
hµν , so
∫
grav
δE(2)
= C2

B

ν
dd−1 x uµ h(d)
µν ζB .

(5.28)

B

for some coefficient C1 , as shown in appendix D. One should in principle be able to verify
that C1 = C2 by an explicit computation. However, since this can be a bit tedious in an
arbitrary higher derivative gravity theory, we present below a slightly indirect but simpler
argument that the two constants must be the same.
To show that the coefficients C1 and C2 are equal, we use the fact that, according to
our definition, the entanglement first law is
grav
grav
δSB
= δE(2)
.

(5.30)

What we have shown in the previous section is that
∫
g b
grav
grav
a
δE(1)
− δSB
= 2 ξB
δEab
ε .

(5.31)

Σ

Plugging eq. (5.30) into eq. (5.31), we find
∫
∫
(d) t
g t
grav
grav
d−1
d−1
d x htt ζB = 2ℓ
dz dd−1 x z 1−d δEtt
ξB
δE(1) − δE(2) = (C1 − C2 )

(5.32)

Σ

B

As R → 0, the middle term in this equation is proportional to (C1 − C2 )Rd . On the
(d)
other hand, the term on the right-hand side starts at O(Rd+2 ), because hµν satisfies the
linearized equations of motion at leading order, as can be explicitly checked. Thus
grav
grav
δE(1)
= δE(2)

(5.33)

for these modes.
As we discuss in section 6.3, the other fall-offs allowed by first law are those for which
grav
δSB = 0 as R → 0. These behave near the boundary as
hµν = z ∆−2 h∆
µν + · · ·

(5.34)

for particular values of ∆ > d − 2, given in eq. (6.37). These modes do not appear in
grav
grav
the holographic stress tensor, so do not contribute to δE(2)
. Their contribution to δE(1)

– 23 –

JHEP03(2014)051

On the other hand, if we plug in the asymptotic expansion (5.27) into eq. (5.25), we find
∫
grav
ν
δE(1) = C1
dd−1 x uµ h(d)
(5.29)
µν ζB

## PDF page 25

is proportional to z ∆−d as z → 0, and thus vanishes if ∆ > d. This means that our
entire analysis applies to modes with ∆ > d, so the linearized equations of motion hold
everywhere. Furthermore, since ∆ depends on the parameters in the Lagrangian, and
grav
δE(1)
must also depend smoothly on these parameters, this conclusion also applies to
modes with ∆ < d. Alternatively, it can be checked explicitly that such modes obey the
leading equations of motion near the boundary (there is a single term to check because
grav
grav
∆ > d − 2) so eq. (5.32) implies δE(1)
= δE(2)
.
Applying this discussion in an arbitrary frame, we have now established that, at the
boundary, χ is equal to the conserved current that appears in the modular energy:
(5.35)

Conservation and traceless of the CFT stress tensor therefore imply dχ|∂M = 0, completing
the derivation in section 4.

6

Application: the holographic dictionary in higher curvature gravity

In section 4.1, we have argued that in the limit R → 0, the entanglement first law, together
with the holographic entanglement functional, yields the holographic dictionary for the
stress tensor. As a concrete and non-trivial application of this observation, in this section
we derive the holographic dictionary for the case when the entanglement entropy is given
by a Wald functional that is polynomial in the Riemann tensor — in other words, for
a higher derivative gravity theory whose action is constructed from arbitrary powers of
the Riemann tensor, but no derivatives thereof. The analysis including derivatives of the
Riemann tensor is similar — and straightforward in any particular example — but we leave
it to future work. As we will show, in this case the entanglement first law allows one to
derive holographic dictionary not only for the stress tensor, but also for the other operators
that couple to the metric in the context of higher derivative gravity.
The usual procedure for finding the holographic dictionary for an arbitrary gravitational theory in AdS is holographic renormalization [40–45]. This technique provides full
information about the holographic dictionary, allowing both arbitrary sources and expectation values. One can thus compute, in principle at least, any desired correlator of the
stress tensor and the other operators that couple to classical fields in the bulk. Nevertheless, computations that use this method can become extremely tedious in the context of
higher derivative gravity. The reason is that a necessary first step in holographic renormalization is to render the variational principle at the spacetime boundary well-defined, and
this can be rather difficult in a general higher derivative gravity theory (e.g. [52, 53]).
However, if one is only interested in computing the expectation value of the stress tensor
in higher derivative gravity rather than its general correlation functions, the “entanglement
first law” method for deriving the holographic dictionary can provide an easy alternative.
The reason for this simplification — besides not having to deal with the variational principle
— is that one can perform all calculations at linearized level, where all higher derivative
gravity theories effectively reduce to R2 theories. A scaling argument can then be used to
argue that the linearized answer holds quite generally.

– 24 –

JHEP03(2014)051

grav ν
χ|∂M = dΣµ Tµν
ζ .

## PDF page 26

6.1

General results

We begin with the general result derived in section 4.1
(
)
d2 − 1
1
grav
δTttgrav (x0 ) =
lim
δS
.
2πΩd−2 R→0 Rd B(R,x0 )

(6.2)

B̃

The binormal ncd is defined as
ncd = n1a n2b − n2a n1b

(6.3)

where n1 and n2 are unit vectors normal to each other and to the bifurcation surface B̃.
To linearized order in the perturbation, they are given by
)
(
)
(
z2
xA ℓ
z2
ℓ
i j
2
a
1
a
(6.4)
1 − 2 htt dt ,
na dx =
1 + 2 2 hij x x dxA
na dx = −
z
2ℓ
Rz
2ℓ R
where xA = xA = {xi , z}.
Next, from the definition of εab in eq. (5.3), we have
δεab =

1
h εab ,
2

h ≡ g cd hcd .

(6.5)

Substituting all these expressions into eq. (6.2), we find
(
)]
[
dd−1 x
xi xj
2ℓ2 tAtB
tAtB
ij
xA xB − 2 δER
+ ER
2htt − hij δ − hij 2
d+2
R
z
R
B z
(6.6)
For a general Lagrangian built from curvatures but no covariant derivatives of curvatures,
abcd is a function of g ab and Rabcd . Evaluated on an AdS background, which is maximally
ER
symmetric and thus satisfies
4πℓ
Wald
δSB
=

d+1 ∫

1
Rabcd = − 2 (gac gbd − gad gbc ) ,
ℓ

(6.7)

the Wald functional takes the following simple form
abcd
ER
= c1 g ⟨ab g cd⟩

(6.8)

for some constant c1 . The indices inside the ⟨ , ⟩ brackets are (anti)symmetrized so that
the resulting object has the same symmetries as the Riemann tensor, as in [53].
abcd , we use the chain rule
To compute δER
abcd
δER
=

abcd
abcd
∂ER
∂ER
ef
δg
+
δRef gh .
∂g ef
∂Ref gh

– 25 –

(6.9)

JHEP03(2014)051

For a general theory of gravity, we have
)
(
∫
grav
Wald
abcd
δSB = δSB
= δ −2π
ER εab ncd
∫ (B̃
)
abcd
abcd
abcd
= −2π
δER
εab ncd + ER
δεab ncd + ER
εab δncd

(6.1)

## PDF page 27

The partial derivatives above are to be evaluated on the background AdS, so using eq. (6.7),
they can be expressed entirely in terms of products of the unperturbed AdS metric, with
various contractions and symmetrizations. Letting
δg ab = −hab ,

δRabcd = Rabcd

(6.10)

abcd is then
the general form of the linearized δER
abcd
δER
= −c2 g ⟨ab g cd⟩ h − c3 h⟨ab g cd⟩ + ℓ2 c4 g ⟨ab g cd⟩ R + ℓ2 c5 R⟨ab g cd⟩ + ℓ2 c6 Rabcd (6.11)

c2 = −2d c4 − c5 ,

c3 = 2 c1 − (d − 1) c5 − 4 c6 .

(6.12)

These constraints follow from the fact that the most general Wald functional that is linear in
the Riemann tensor takes the form (6.27) — see below — which is parametrized by just four
constants. Eq. (6.28) then shows that the six coefficients ci satisfy two additional relations.
To finalize our computation of the linearized Wald functional, we only need to evaluate
the linearized Riemann tensor, given by
1
1
Rabcd = (∇c ∇b had − ∇d ∇b hac + ∇d ∇a hbc − ∇c ∇a hbd ) + (Raecd he b + Re bcd hae ) . (6.13)
2
2
For the computation of the holographic stress tensor (6.1), we only need the leading behaviour of the Riemann tensor as R → 0. This can be easily evaluated by noting that
z ∝ R and z-derivatives of the metric perturbation dominate over xµ -derivatives as z → 0.
More explicitly, near the boundary we can write
λ
hµν (z, xλ ) = z ∆−2 h(∆)
µν (x ) + · · ·

(6.14)

for some ∆ to be determined, where the dots indicate terms at higher order in z. Then, we
can replace ∂z hµν = (∆ − 2)z −1 hµν and ignore all xµ -derivatives, because ∂µ ∼ O(1) will
always be subleading in the R expansion, as compared to ∂z ∼ O(R−1 ). Consequently, in
taking R → 0, we can approximate19
Rµνρσ |R→0 =

∆−2
(hµρ gνσ + hνσ gµρ − hµσ gνρ − hνρ gµσ )
2ℓ2

(6.15)

1
[2(∆ − 1) − ∆2 ] hµν .
2z 2

(6.16)

and
Rµzνz |R→0 =
19

It is not hard to see that if we had also allowed derivatives of the Riemann tensor into the Wald
functional, their linearized leading contribution to the entropy as R → 0 would also be linear in hµν with
no derivatives, due to the above scaling argument. Their contribution would typically be of the same order
as the polynomial one, and straightforward if a bit tedious to compute.

– 26 –

JHEP03(2014)051

abcd with respect to g ef , and
where the first two terms come from the partial derivative of ER
the last three from the partial derivative with respect to the Riemann tensor, evaluated on
AdS. All indices are raised and contracted with the background metric g ab . Note that not
all coefficients ci introduced above are independent, but rather they satisfy

## PDF page 28

We can then substitute this simplified expression into20 eq. (6.11) and further into eq. (6.6).
Upon contracting with xA xB , the integrand will contain terms proportional to htt , δ ij hij
and hij xi xj ; using spherical symmetry, the latter can be replaced by ⃗x2 δ ij hij /(d − 1).
Furthermore, we can write hij δ ij = hµν η µν + htt . The final answer takes the form
Wald
δSB
=

4πℓd−3
R

∫

dd−1 x
(A htt + B η µν hµν )
d−2
z
B

(6.17)

where the coefficients A and B are given by
|⃗x|2
− R2
d−1

)[

c1 c3 c5
−
+ (2 − 2d + ∆d − ∆2 ) + (∆2 − d∆2 + d∆ − 2)c6
2
2
4

]

−R2 ∆(∆ − 1)(d − 2)c6
[
]
|⃗x|2 c1 c3 c5
2
2
B =
−
+ (2 − 2d + ∆ − 2∆ + d∆ ) + c6 (∆ − 2)
d−1 2
2
4
]
[
c5
2
2
2 c1
− c2 + c4 (∆ + d∆ − 2d − ∆ ) + (3∆ − 4 − ∆ ) .
+R
2
4

(6.18)

Using eq. (6.14), it is not hard to verify that the leading contribution in eq. (6.17) scales
as R∆ , so we must choose ∆ = d to obtain a finite result in eq. (6.1). Thus, we find again,
as in Einstein gravity, that in order for the first law of entanglement to be satisfied, the
asymptotic expansion of the metric should start at order z d−2 . Performing the integral in
eq. (6.17) with ∆ = d, we find that
(d)

µ
δTttgrav = α htt + β ηtt h(d)
µ

(6.19)

where the indices on h(d) are now raised with η µν , and the two coeffcients are given by
α = d(−c1 + c3 + (d − 1)c5 + 2dc6 ) ℓd−3

β = [−(d + 2)c1 + 2(d + 1)c2 + c3 + 2d(d + 1)c4 + (d + 1)c5 − 2(d − 2)c6 ] ℓ

(6.20)
d−3

(6.21)

Generalizing the calculation to an arbitrary Lorentz frame as in section (4.1), we conclude that
grav
(d) α
δTµν
= αh(d)
µν + β ηµν hα
20

The explicit expression for eq. (6.11) is
]
[
c5
µνρσ
δER
= (∆d − 2d − ∆2 + ∆) c4 + (∆ − 2) − c2 h g ⟨µν g ρσ⟩
2
]
[
c5
+ 2(∆ − 2)c6 − c3 + (∆d − 2d + 2 − ∆2 ) h⟨µν g ρσ⟩
2
[c
c5
c3 ] µν zz
6
µzρz
δER
=
(2∆ − 2 − ∆2 ) + (∆d − 2d + 2 − ∆2 ) −
h g
2
8
4
[c
c5
c2 ]
4
(∆d − 2d − ∆2 + ∆) + (3∆ − 4 − ∆2 ) −
h g µν g zz
+
2
8
2

– 27 –

(6.22)

JHEP03(2014)051

A=

(

## PDF page 29

As in Einstein gravity, tracelessness and conservation of Tµν imply that21
h(d)µ µ = 0 ,

∂ µ h(d)
µν = 0

(6.23)

so we have
grav
δTµν
= d ℓd−3 [−c1 + c3 + (d − 1) c5 + 2d c6 ] h(d)
µν

= dℓd−3 [c1 + 2(d − 2)c6 ] h(d)
µν .

(6.24)

6.2

Examples

We now give some explicit examples employing the general formula (6.24) and compare
with known results in the literature.
6.2.1

The holographic stress tensor in R2 gravity

To begin, consider the case of an arbitrary R2 gravity theory in d + 1 dimensions, which
contains all possible contractions of the Riemann tensor but no derivatives thereof. It is
21

When α + β d = 0, the vanishing of the trace of the stress tensor no longer implies h(d)µ µ = 0. Using
our results from section 6.3, it is easy to check that precisely at this value of the ci , the additional scalar
operator present in higher curvature gravity — which couples to the trace of the metric — has dimension
∆ = d, and thus appears at the same order in the asymptotic z expansion as the traceless mode that couples
to the CFT stress tensor.
22
There are a few exceptions to this, such as a gauge field in three space-time dimensions, which can
contribute to the stress tensor at quadratic order, or when fields have finely-tuned dimensions that can add
up to d.

– 28 –

JHEP03(2014)051

This gives the holographic stress for a theory in which the Wald entropy is an arbitrary
function of the Riemann tensor, but not its covariant derivatives. The coefficients ci are
defined in eqs. (6.8) and (6.11).
Note that to this point, we have only been considering the leading contribution to the
expectation value of the stress tensor. That is, as noted in footnote 4, we are considering
a one-parameter family of states |Ψ(λ)⟩ with |Ψ(0)⟩ = |0⟩ and within this family, δ⟨Tµν ⟩ ≡
∂λ ⟨Tµν ⟩|λ=0 . However, we will now argue that our result extends beyond this leading
(d)
order to give a general prescription for ⟨Tµν ⟩. In particular, the fact that ⟨Tµν ⟩ ∝ hµν
simply follows from conformal invariance: there is no other field in spacetime that has
the correct tensor structure and transformation properties under rescalings.22 Thus, the
(d)
above expression for the stress tensor holds even when hµν is finite. Another way to see
this fact is to note that since the theory is conformal, the only dimensionless number that
(d) d
d
characterizes the perturbation is ε = c−1
T ⟨Tµν ⟩R in the CFT, or hµν R in spacetime.
Applicability of the first law only requires that ε ≪ 1, see also the appendix of [17]. Thus,
we can either have ⟨Ttt ⟩ small and R finite, or ⟨Ttt ⟩ finite and R → 0. In the first case, we
can derive the linearized gravitational equations in the entire bulk, by taking the amplitude
of the perturbation to be small and using the Wald functional method. In the second case,
we can derive the leading asymptotic expansion of the metric (as z → 0) for a general
non-linear solution.

## PDF page 30

convenient to write the most general Lagrangian of such a theory as
]
[
1
d(d − 1)
2
abcd
2
ab
2 2
+ R + a1 ℓ̃ Rabcd R
+ a2 ℓ̃ Rab R + a3 ℓ̃ R ,
L=
16πGN
ℓ̃2

(6.25)

ℓ4 ℓ2 d − 3
−
+
(2 a1 + d a2 + d(d + 1) a3 ) = 0 .
ℓ̃4 ℓ̃2 d − 1

(6.26)

Of course, ℓ = ℓ̃ when the ai are set to zero. To construct the Wald entropy (1.5), we
consider the variation of the Lagrangian with respect to the curvature, as in eq. (5.10)
[(
)
1
1
2
abcd
+ a3 ℓ̃ R (g ac g bd − g ad g bc )+
(6.27)
ER =
16πGN
2
)]
1 2 ( ac bd
2 abcd
bc ad
ad bc
bd ac
+2a1 ℓ̃ R
+ a2 ℓ̃ R g − R g − R g + R g
2
The coefficients ci defined in eq. (6.11) are given by
[
]
ℓ̃2
1
1 − 2 (2a1 + da2 + d(d + 1)a3 ) 2 ,
c1 =
16πGN
ℓ
[
]
1
ℓ̃2
c3 =
1 − (8a1 + (3d − 1)a2 + 2d(d + 1)a3 ) 2
8πGN
ℓ
c4 =

a3 ℓ̃2
,
8πGN ℓ2

c5 =

a2 ℓ̃2
,
8πGN ℓ2

c2 = −

c6 =

2(a2 + 2d a3 ) ℓ̃2
,
16πGN
ℓ2

a1 ℓ̃2
8πGN ℓ2

(6.28)

which one can verify satisfy the constraints in eq. (6.12). Hence our general expression (6.24) gives
[
]
d ℓd−3
ℓ̃2 (d)
⟨Tµν ⟩ =
1 + (4(d − 3)a1 − 2d a2 − 2d(d + 1)a3 ) 2 hµν
(6.29)
16πGN
ℓ
We have checked that eq. (6.29) agrees perfectly with previous results in the literature that
used more standard holographic techniques: see, for example, equation (51) of [54] for the
case d = 3. We have also checked that in general d our answer agrees with the holographic
stress tensor of [53], when the results of that paper are applied to a flat boundary metric
and the volume divergences are subtracted. Note that the covariant expression of [53] for
the holographic stress tensor in terms of induced fields at the boundary obscures somewhat
the simplicity of the final answer (6.29) for ⟨Tµν ⟩, which is dictated by scaling.23
23

This scaling property might be more obvious if one used instead the Hamiltonian method for holographic
renormalization [45]. Nevertheless, one would still need to deal with the variational principle with that
approach.

– 29 –

JHEP03(2014)051

where ℓ̃ is the scale parametrizing the (negative) cosmological constant. We also use ℓ̃ to
set the scale in the curvature-squared terms, which leaves ai as dimensionless couplings
controlling the strength of these interactions. We assume that the parameters are chosen
such that the theory admits an AdSd+1 vacuum solution of radius ℓ. In fact, it is straightforward to show the AdS radius is determined by the parameters in the Lagrangian (6.25)
by the following quadratic equation

## PDF page 31

6.2.2

An R4 example

As an example where higher powers of curvature appear, consider the theory
[
]
∫
d(d − 1)
1
6
µνρσ 2
d+1 √
+ R + αℓ̃ (Rµνρσ R
) .
I=
d x −g
16πGN
ℓ̃2

(6.30)

The four independent coefficients ci are given by
(
)
1
ℓ̃6
2α ℓ̃6
c1 =
1 − 16d(d + 1)α 6 ,
c4 =
,
16πGN
ℓ
πGN ℓ6

c5 = 0 ,

so our general expression (6.24) gives
(
)
ℓ̃6
dℓd−3
1 + 16d(d + 1)(d − 3)α 6 h(d)
⟨Tµν ⟩ =
µν
16πGN
ℓ

c6 =

d(d + 1)α ℓ̃6
2πGN ℓ6
(6.32)

(6.33)

(3)

Thus, precisely in d = 3 we have ⟨Ttt ⟩ = 3htt /(16πGN ). The explicit solution (142)-(143)
in [54] for the metric of the black hole in presence of the R4 term shows that h00 = m is
uncorrected by the higher derivative term. Hence we also conclude that the mass of the
black hole is uncorrected, in agreement with the expectation of [54].
6.3

Other terms in the FG expansion

A feature of higher derivative gravity is the existence of additional degrees of freedom
contained in the metric. This occurs because the equations of motion are no longer second
order. These new degrees of freedom will appear as new terms in the asymptotic FG
expansion, which according to the usual AdS/CFT lore will represent new operators in the
dual CFT. Here we show how the entanglement first law can be used to derive the FG
expansion for these new modes, including a derivation of the conformal dimensions of the
CFT operators to which they couple.
Of course, the physical interpretation of these modes is unclear. First, they typically
have negative norm indicating that the boundary theory is no longer unitary [55], and
second, their masses are typically at the string scale where the low energy effective field
theory is unreliable. Nonetheless, they do satisfy the equations of motion, so we can ask
how they fit mathematically into our discussion of the first law.

– 30 –

JHEP03(2014)051

This particular example has been studied previously in section 3.4 of [54], for the case
d = 3. The authors of that paper were investigating black hole thermodynamics in the
above theory, and found that in order for the first law to hold, the mass of the black hole
had to be independent of the coefficient of the R4 term. In this subsection, we will use
the holographic entanglement method for computing the stress tensor expectation value to
confirm their result.
The Wald functional for this theory reads
]
[
1 ac bd
1
ad bc
6 abcd
αβγδ
abcd
(g g − g g ) + 4αℓ̃ R
(Rαβγδ R
)
(6.31)
ER =
16πGN 2

## PDF page 32

where we have defined

(∆)

h(∆) ≡ h(∆)i i − h00

and

(∆)
ĥ(∆)
µν ≡ hµν −

1 (∆)
h
.
d

(6.35)

Further the constant factors are given by
[
]
(
) ℓ2
ℓ̃2 ∆
2
aT = 2
2d(a2 + a3 + d a3 ) + a2 (d − ∆)∆ + 4a1 3 − d + d∆ − ∆ −
4ℓ (1 + ∆)
ℓ̃2
[
2
ℓ̃ ∆
2(d − 3)d(a2 + a3 + d a3 ) − (a2 + d a2 + 4d a3 )(d − ∆)∆+
aS =
2
4dℓ (1 + ∆)
]
(
)
ℓ2
2
.
(6.36)
−4a1 3 − d + d∆ − ∆ − (d − 1)
ℓ̃2

grav
We can then satisfy the equation δSB
= 0 at leading order in R, the radius of the
ball, by demanding that the constants aT , aS vanish. This is the case for ∆ = 0 and
∆ = ∆T,S , where24
√
d2 2a3 d(d + 1) + 2da2 − 4a1 (d − 3) − ℓ2 /ℓ̃2
d
±
+
∆±
T =
2
4
4a1 + a2
√
d
d2 (d − 1)ℓ2 /ℓ̃2 − 2(d − 3)[2a1 + a2 d + d(d + 1)a3 ]
∆±
=
±
+
(6.37)
S
2
4
4a1 + a2 (d + 1) + 4a3 d

We have checked that these expressions agree with the coefficients of the asymptotic falloffs
of solutions to the equations of motion in R2 gravity.25 Also, for d = 3, ∆+
S agrees with the
operator dimension that was obtained in [54], also by solving the asymptotic equations of
grav
motion. Therefore, imposing δSB
= 0 as R → 0 ensures that the asymptotic equations
of motion are satisfied, a claim which we use in section 5.3.
Of course, only the ∆+
S,T solutions are physical, since only for them does the x integral converge. It is
grav
interesting though that the δSB
= 0 constraint also knows about the non-normalizable modes in gravity,
including the perturbation of the boundary metric, with ∆ = 0.
25
For completeness, we reproduce the equations of motion that follow from the Lagrangian (6.25):
24

]
d(d − 1)
σ
1[
Gµν −
a1 Rµνρσ Rµνρσ + a2 Rµν Rµν + a3 R2 − (a2 + 4a3 ) □R gµν − 2a1 Rµαβγ Rν αβγ
gµν =
2
ℓ̃2
2ℓ̃4
−(2a2 + 4a1 )Rµανβ Rαβ − 2a3 RRµν + 4a1 Rµα Rν α + (2a3 + a2 + 2a1 )∇µ ∇ν R − (a2 + 4a1 )□Rµν
On the AdS solution of radius ℓ, the relationship between ℓ and ℓ̃ is given in eq. (6.26).

– 31 –

JHEP03(2014)051

grav
These new modes appear as additional solutions to the first law constraint δSB
=
grav
δEB . Previously, we argued that a metric perturbation of the form (6.14) that satisfies
the first law relation must have ∆ = d and be related to the stress tensor expectation value
as we described in the preceding section. Nevertheless, perturbations with ∆ ̸= d, with ∆
grav
an arbitrary real number, are also allowed, as long as they satisfy δSB
= 0.
To show how this works explicitly, we consider the example of general R2 gravity, with
Lagrangian given by eq. (6.25). We consider a metric perturbation of the form (6.14). The
x integral in eq. (6.6) is convergent as long as ∆ > d − 2. Performing this integral, we find
( d−1 ) ( 1
)(
)
d−3 R∆ Ω
Γ
(∆
−
d)
+
1
Γ
ℓ
(∆)
d−2
2
(2 ∆+1 )
δS grav =
ĥ00 aT + h(∆) aS
(6.34)
2GN
2Γ 2

## PDF page 33

7

Discussion

Relation to the work of Jacobson
The results in this paper are reminiscent of (and partly motivated by) the work of Jacobson [29] (see also [56–58]). There, it was shown that if the first law of thermodynamics —
governing the local change in entropy (defined to be horizon area) as a certain bulk energy
flows through the horizon — is assumed to hold for an arbitrary Rindler horizon, then
the full nonlinear Einstein equations must be satisfied. In Jacobson’s case, there was no
microscopic understanding of the meaning of the entropy, and thus no fundamental understanding of why the thermodynamic relation should hold. By contrast, in our case there is
a precise microscopic understanding of both the energy and the entropy appearing in our
relation δSB = δEB , and a proof of the first law at the microscopic level. Also, our gravity
analysis applies to an arbitrary higher curvature theory, a scenario that is problematic
with Jacobson’s approach [57]. On the other hand, because our proof is based on global
rather than local Rindler horizons, we were only able to obtain the gravitational equations
of motion at the linearized level.
Deriving the nonlinear equations?
It is obviously interesting to ask whether we can extend our results to the nonlinear level.
On the CFT side, the entanglement entropies for finite perturbations to the vacuum state
are still constrained by the modular energies, but the constraint is the inequality ∆SA ≤
∆⟨HA ⟩ following from the positivity of relative entropy. For any ball-shaped region, we

– 32 –

JHEP03(2014)051

In this paper, we have seen that a universal relation between entanglement entropy and
‘modular’ energy for small perturbations to the vacuum state of a CFT leads, in the
holographic context, to a nonlocal constraint on the dual spacetimes, which is exactly
equivalent to the linearized gravitational equations. Thus, given any holographic CFT,
we can derive the linearized bulk equations knowing only the entanglement functional.
Moreover, as we showed in sections 4.1 and 6, we can also derive the asymptotic boundary
conditions for the metric perturbation, as well as an expression for the holographic stress
tensor. When matter couplings to curvature vanish, these results taken together imply that
from the entanglement functional, we can derive the complete map from states to metrics
at the linearized level about the vacuum.
We have also shown that this non-local gravitational constraint is precisely the first
law of black hole thermodynamics (in the form proved by Iyer and Wald) applied to certain
Rindler patches of pure AdS that can be also interpreted as zero-mass hyperbolic black
holes. Thus, we have a result that holds purely in classical gravity: in any classical gravitational theory for which anti-de Sitter space is a solution and for which the first law of black
hole thermodynamics holds for some Wald functional SWald , small perturbations about the
AdS vacuum solution are governed by the linearized gravitational equations obtained from
varying the Lagrangian associated to SWald . This provides a converse to the theorem of
Iyer and Wald, but also a microscopic understanding of the origin of the Iyer-Wald first
law for AdS-Rindler horizons.

## PDF page 34

Quantum first law in the bulk.
Finally, it would be interesting to understand the implications of the entanglement first
law (in its infinitesimal form) beyond the classical level on the gravity side. Since the
entanglement first law is an exact relation, it can also be used to study subleading quantum
gravitational corrections to the classical results that we have derived, or CFT states that
do not have a classical bulk interpretation. These quantum states/corrections can be easily
identified by the scaling of their energy and entropy with the central charge in the CFT:
while the classical contributions are proportional to the central charge, the quantum ones
scale with a lower power of it. Thus, the first law should place constraints on the quantum
behaviour of the bulk gravitational theory and will likely also involve an understanding of
the quantum corrections to the Ryu-Takayanagi formula as discussed recently in [59–61].

Acknowledgments
We thank Horacio Casini, Nima Lashkari, Aitor Lewkowycz, Juan Maldacena, Don Marolf,
and Sasha Zhiboedov, for useful conversations. TH, RCM, and MVR also acknowledge the
support of the KITP during the program “Black Holes: Complementarity, Fuzz, or Fire?”
where some of this work was done. The research of TH is supported in part by the National
Science Foundation under Grant No. NSF PHY11-25915. Research at Perimeter Institute
is supported by the Government of Canada through Industry Canada and by the Province
of Ontario through the Ministry of Research & Innovation. The research of MVR and RCM
is supported in part by the Natural Sciences and Engineering Research Council of Canada.
RCM also acknowledges support from the Canadian Institute for Advanced Research. The

– 33 –

JHEP03(2014)051

can still translate this inequality to a constraint on the bulk metric. The set of all such
constraints should significantly restrict the allowed bulk spacetimes, but it seems unlikely
that these restrictions will fully determine the bulk equations at the nonlinear level. In
particular, the nonlinear gravitational equations are sensitive to all the other fields present
in the classical bulk theory, including the components of the metric along any extra compact
directions. These additional degrees of freedom depend significantly on which holographic
CFT we are considering. Thus, starting from the universal relation ∆SA ≤ ∆⟨HA ⟩ (or any
other universal relation for holographic CFTs) one might realistically expect to recover
only a part of the constraints implied by the full non-linear equations; for example, one
might obtain Einstein’s equations with the additional assumption that no other matter
fields are turned on in the bulk.
Another interesting possibility is that one might be able to obtain some constraints
at the nonlinear level in the bulk even from the linearized entanglement first law, by
considering bulk perturbations which are kept finite but taken to be localized closer and
closer to the AdS-Rindler horizon. In such a limit, the energy perturbation in the CFT
vanishes due to gravitational redshift effects. By considering infinitesimal perturbations
away from this limit, the linearized CFT first law should apply, but on the gravity side,
it would appear that we will obtain constraints on a finite perturbation localized near the
horizon. This may be closely related to the approach of Jacobson.

## PDF page 35

research of MG is supported by the DOE grant DE-SC0007901. TF is supported by NSF
Grant No. PHY-1314311.

A

Vanishing of the integrand

Suppose
∫

dd−1 x dz f (⃗x, z) = 0

∀R, ⃗x0

Σ

(A.1)

0

Σ

Σ

These are the average and the first moment of f on the hemisphere B̃(R, x0 ),
∫
∫
IR = dA f = 0 ,
Ii = dA xi f = 0
B̃

(A.3)

B̃

where dA represents the area element on B̃. Now we can repeat the argument replacing
f → xi f in (A.1), and deduce that all moments of f vanish on every hemisphere B̃. We
conclude that f = 0, as we needed to show.
An alternative argument for the vanishing of f is to note that the integral in (A.3),
viewed as a map from B̃ to R, defines the “hyperbolic Radon transform” of the function f ,
whose vanishing implies the vanishing of the function, assuming that f is continuous [62].

B

Noether identities and the off-shell Hamiltonian

In this section, we derive the Noether identities for diffeomorphism invariance, and show
that J[ξ] = dQ[ξ] + ξ a Ca as claimed in (5.11).
Under a diffeomorphism, the variation of the action I is
∫
δξ I = ε(E φ δξ φ)
(B.1)
with the sum over fields φ implicit. The integrand for a field of rank r is
a1 ···ar
s
ε (E φ )ab11···b
···ar δξ φb1 ···bs
(
s
= ε (E φ )ab11···b
···ar

···ar
ξ ∇b φba11···b
−
s
b

r
∑

a1 ···ar
b
s
= εξ b (E φ )ab11···b
···ar ∇b φb1 ···bs + εξ

−εξ b

s
∑
i=1

···λ···ar
+
∇λ ξ ai φba11···b
s

i=1
r
∑
i=1

[

s
∑
i=1

···ar
∇bi ξ λ φba11···λ···b
s

a1 ···λ···ar
s
∇λ (E φ )ab11···b
···b···ar φb1 ···bs

[

]
a1 ···ar
a
s
∇bi (E φ )ab11···b
···ar φb1 ···b···bs − d(ξ Ca )

– 34 –

)

]
(B.2)

JHEP03(2014)051

where Σ(R, ⃗x0 ) is the region z ≥ 0, |⃗x − ⃗x0 |2 + z 2 ≤ R2 . We would like to show that (A.1)
implies that f = 0. To prove this, differentiate the integral, and define
∫
∫
d−1
(A.2)
IR = ∂R d x dz f = 0 ,
Ii = ∂xi dd−1 x dz f = 0 .

## PDF page 36

where the dots indicate that indices appear in the ith position, and the constraints Ca
are defined in eq. (5.12). If ξ has compact support, then the total derivative does not
contribute and since δξ I = 0 for any ξ, we have the following identity for the integrand,
(
r
[
]
∑
∑
a1 ···ar
a1 ···λ···ar
φ b1 ···bs
s
+
∇
(E φ )ab11···b
∇
φ
(E
)
φ
λ
···ar b b1 ···bs
a1 ···b···ar b1 ···bs
i=1

φ

−

s
∑
i=1

[
]
a1 ···ar
s
∇bi (E φ )ab11···b
φ
···ar b1 ···b···bs

)

= 0 . (B.3)

dJ[ξ] = d(ξ a Ca )

(B.4)

for all diffeomorphisms ξ. It follows that [49]
J[ξ] = dQ[ξ] + ξ a Ca ,

(B.5)

for some Q, which we take to be the off-shell definition of the Noether charge Q.

C

Example: Einstein gravity coupled to a scalar

In this appendix we review the covariant formalism applied to Einstein gravity coupled to
a scalar field. The Lagrangian is
]
[
1
1
2
R − (∂ψ) − V (ψ) .
(C.1)
L=ε
16πGN
2
The cosmological constant is included in the scalar potential V (ψ). The definitions (5.4)
and (5.6) give
[
]
)
1 (
ab
a
b
α
Θ=
∇b δg − ∇ δgb − δψ∇ ψ εa
(C.2)
16πGN

and

]
(
)
1
[e d]
g d e
∇e ∇ ξ
+ 2(E ) e ξ εd
J=
8πGN
[

where E g is the gravitational equation of motion,
)
]
[
(
1
1
1
1
1
g
2
Eab =
Rab − gab R − ∂a ψ∂b ψ + gab (∂ψ) − V (ψ) .
16πGN
2
2
2
2

(C.3)

(C.4)

The Noether current can be written
g b
J = dQ + 2ξ a Eab
ε

(C.5)

1 a b
∇ ξ εab .
16π

(C.6)

where
Q=−

– 35 –

JHEP03(2014)051

This is the Noether identity.
Next, remember that the Noether current (5.6) satisfies dJ[ξ] = −εE φ δξ φ. Using (B.2)
and the Noether identity, this becomes

## PDF page 37

D

Form of the bulk charge

In this appendix, we show that the linearized modular energy defined by the bulk WaldNoether procedure always take the simple form noted in eq. (5.29). We start with eq. (5.25),
reproduced here for convenience:
∫
grav
(δQ[ξB ] − ξB · Θ(δφ))
(D.1)
δE(1) =
B

Q[ξ] = Xcd ∇[c ξd] + Wc ξ c + Y(φ, Lξ φ) + dZ(ξ, φ)

(D.2)

where Y is linear in Lξ φ, Z is linear in ξ, and all forms are covariant expressions constructed
from the fields. We assume there is no matter with linear couplings to curvature. The
general covariant form of Xcd is
Xcd = X abcd εab
(D.3)
where X abcd is antisymmetric in both is first two and last two indices. Using symmetry
and arguments similar to those in section 6, at zeroth and first order around AdS and to
leading in the z expansion, we must have (ignoring coefficients)
∣
abcd ∣
X
∝ g ⟨ab g cd⟩ ,
δX abcd ∝ g ⟨ab g cd⟩ h + h⟨ab g cd⟩ .
(D.4)
∣
AdS

grav
The contribution of the first term in eq. (D.2) to δE(1)
is then
)
∫ (
) ∫ (
1
abcd
abcd
abcd
abcd
∇c ξd + X
δ(∇c ξd ) εab
δX
∇c ξd + h X
δ X
εab ∇c ξd =
IX =
2
B
B
(D.5)
where the quantities without δ’s are evaluated on the background AdS solution. The
non-zero background components are

εab → εtz ∝

dd−1 x
,
z d+1

∇[i ξt] =

xi
,
Rz 2

∇[z ξt] =

R2 − |⃗x|2
,
2Rz 3

[c

X tzcd ∝ z 4 δt δzd] . (D.6)

Using eq. (D.4), the leading behaviour of the linearized quantities reads
δX tztz ∝ z 6 (htt + hµν η µν ) ,

δX tzti ∝ z 7 (∂i htt + . . .) ,

δ(∇[z ξt] ) ∝ ζ t ∂z htt

(D.7)

It is clear from the above expressions that only the leading terms in X tztz and δX tztz
will contribute as z → 0. Plugging in the z-dependence of hµν , one finds that all the
(d)
(d)
non-vanishing contributions are proportional to htt or hi i . Requiring moreover that
(d)
(d)
(d)
hµ µ = hi i − htt = 0, which follows from tracelessness of the CFT stress tensor, we
find that
∫
(d)
IX ∝ dd−1 x htt ζ t
(D.8)

where we used the fact that limz→0 ξ t = ζ t .

– 36 –

JHEP03(2014)051

where the Killing vector ξB is given in eq. (3.1). Into this equation we would like to
substitute the asymptotic form of the metric perturbation (5.27), representing the stress
tensor perturbation. As we argued in the main text, modes with different falloffs will not
contribute, since they have the wrong scaling dimension.
As shown in [28], the most general form of Q[ξ] is

## PDF page 38

The contribution of the Wc ξ c = Wt ζ t term is easy to evaluate, taking into account
the fact that the d − 1 form Wc is a covariant expression constructed from hab , gab and
their background covariant derivatives. The most general form of Wc , linearized around
AdS, is thus
Wc = εab F ab c ,

F ab c = f1 (□)(∇a hb c − ∇b ha c ) + f2 (□)(δ a c ∇b h − δ b c ∇a h) .

(D.9)

B

B

The ξ · Θ term in eq. (D.2) has the same form as Wc ξ c so can be treated similarly.
The term Y in eq. (D.2) comes from the ambiguity Θ → Θ + dY(δφ). Together, these
terms contribute to χ in the combination
δY(δξ φ) − δξ Y(δφ) .

(D.11)

This vanishes for a background Killing vector.
Finally, the dZ term is an ambiguity that comes from the fact that Q is only defined
by its derivative. We fix this ambiguity to zero by requiring that there are no boundary
terms in the horizon entropy.
The overall conclusion is
∫
(d)
grav
dd−1 x htt ζ t ,
(D.12)
δE(1)
= C1
B

for some constant C1 .
Open Access. This article is distributed under the terms of the Creative Commons
Attribution License (CC-BY 4.0), which permits any use, distribution and reproduction in
any medium, provided the original author(s) and source are credited.

References
[1] S. Ryu and T. Takayanagi, Holographic derivation of entanglement entropy from AdS/CFT,
Phys. Rev. Lett. 96 (2006) 181602 [hep-th/0603001] [INSPIRE].
[2] S. Ryu and T. Takayanagi, Aspects of holographic entanglement entropy,
JHEP 08 (2006) 045 [hep-th/0605073] [INSPIRE].
[3] T. Nishioka, S. Ryu and T. Takayanagi, Holographic entanglement entropy: an overview,
J. Phys. A 42 (2009) 504008 [arXiv:0905.0932] [INSPIRE].
[4] T. Takayanagi, Entanglement entropy from a holographic viewpoint,
Class. Quant. Grav. 29 (2012) 153001 [arXiv:1204.2450] [INSPIRE].
[5] M. Van Raamsdonk, Comments on quantum gravity and entanglement, arXiv:0907.2939
[INSPIRE].

– 37 –

JHEP03(2014)051

The only non-zero contribution on B will be from F [tz] t , and using tracelessness of the
leading term in h one can easily show that
∫
∫
(d)
c
dd−1 x htt ζ t .
(D.10)
Wc ξ ∝

## PDF page 39

[6] M. Van Raamsdonk, Building up spacetime with quantum entanglement,
Gen. Rel. Grav. 42 (2010) 2323 [arXiv:1005.3035] [INSPIRE].
[7] B. Swingle, Entanglement renormalization and holography, Phys. Rev. D 86 (2012) 065007
[arXiv:0905.1317] [INSPIRE].
[8] B. Swingle, Constructing holographic spacetimes using entanglement renormalization,
arXiv:1209.3304 [INSPIRE].
[9] E. Bianchi and R.C. Myers, On the architecture of spacetime geometry, arXiv:1212.5183
[INSPIRE].

[11] V. Balasubramanian, B.D. Chowdhury, B. Czech, J. de Boer and M.P. Heller, A
hole-ographic spacetime, arXiv:1310.4204 [INSPIRE].
[12] M. Levin and X.-G. Wen, Detecting topological order in a ground state wave function,
Phys. Rev. Lett. 96 (2006) 110405 [cond-mat/0510613] [INSPIRE].
[13] A. Kitaev and J. Preskill, Topological entanglement entropy,
Phys. Rev. Lett. 96 (2006) 110404 [hep-th/0510092] [INSPIRE].
[14] H. Li and F.D.M. Haldane, Entanglement spectrum as a generalization of entanglement
entropy: identification of topological order in non-abelian fractional quantum Hall effect
states, Phys. Rev. Lett. 101 (2008) 010504 [arXiv:0805.0332].
[15] A.M. Turner, F. Pollmann and E. Berg, Topological phases of one-dimensional fermions: An
entanglement point of view, Phys. Rev. B 83 (2011) 075102 [arXiv:1008.4346].
[16] N. Lashkari, M.B. McDermott and M. Van Raamsdonk, Gravitational dynamics from
entanglement “thermodynamics”, arXiv:1308.3716 [INSPIRE].
[17] D.D. Blanco, H. Casini, L.-Y. Hung and R.C. Myers, Relative entropy and holography,
JHEP 08 (2013) 060 [arXiv:1305.3182] [INSPIRE].
[18] J. Bhattacharya, M. Nozaki, T. Takayanagi and T. Ugajin, Thermodynamical property of
entanglement entropy for excited states, Phys. Rev. Lett. 110 (2013) 091602
[arXiv:1212.1164] [INSPIRE].
[19] M. Nozaki, T. Numasawa and T. Takayanagi, Holographic local quenches and entanglement
density, JHEP 05 (2013) 080 [arXiv:1302.5703] [INSPIRE].
[20] D. Allahbakhshi, M. Alishahiha and A. Naseh, Entanglement thermodynamics,
JHEP 08 (2013) 102 [arXiv:1305.2728] [INSPIRE].
[21] G. Wong, I. Klich, L.A. Pando Zayas and D. Vaman, Entanglement temperature and
entanglement entropy of excited states, JHEP 12 (2013) 020 [arXiv:1305.3291] [INSPIRE].
[22] A. Wehrl, General properties of entropy, Rev. Mod. Phys. 50 (1978) 221 [INSPIRE].
[23] V. Vedral, The role of relative entropy in quantum information theory,
Rev. Mod. Phys. 74 (2002) 197 [INSPIRE].
[24] H. Casini, M. Huerta and R.C. Myers, Towards a derivation of holographic entanglement
entropy, JHEP 05 (2011) 036 [arXiv:1102.0440] [INSPIRE].
[25] A. Lewkowycz and J. Maldacena, Generalized gravitational entropy, JHEP 08 (2013) 090
[arXiv:1304.4926] [INSPIRE].

– 38 –

JHEP03(2014)051

[10] R.C. Myers, R. Pourhasan and M. Smolkin, On spacetime entanglement,
JHEP 06 (2013) 013 [arXiv:1304.2030] [INSPIRE].

## PDF page 40

[26] R.M. Wald, Black hole entropy is the Noether charge, Phys. Rev. D 48 (1993) 3427
[gr-qc/9307038] [INSPIRE].
[27] T. Jacobson, G. Kang and R.C. Myers, On black hole entropy, Phys. Rev. D 49 (1994) 6587
[gr-qc/9312023] [INSPIRE].
[28] V. Iyer and R.M. Wald, Some properties of Noether charge and a proposal for dynamical
black hole entropy, Phys. Rev. D 50 (1994) 846 [gr-qc/9403028] [INSPIRE].
[29] T. Jacobson, Thermodynamics of space-time: the Einstein equation of state,
Phys. Rev. Lett. 75 (1995) 1260 [gr-qc/9504004] [INSPIRE].

[31] A. Buchel et al., Holographic GB gravity in arbitrary dimensions, JHEP 03 (2010) 111
[arXiv:0911.4257] [INSPIRE].
[32] V.E. Hubeny, M. Rangamani and T. Takayanagi, A covariant holographic entanglement
entropy proposal, JHEP 07 (2007) 062 [arXiv:0705.0016] [INSPIRE].
[33] A.C. Wall, Maximin surfaces and the strong subadditivity of the covariant holographic
entanglement entropy, arXiv:1211.3494 [INSPIRE].
[34] X. Dong, Holographic entanglement entropy for general higher derivative gravity,
JHEP 01 (2014) 044 [arXiv:1310.5713] [INSPIRE].
[35] J. Camps, Generalized entropy and higher derivative Gravity, arXiv:1310.6659 [INSPIRE].
[36] A. Bhattacharyya, M. Sharma and A. Sinha, On generalized gravitational entropy, squashed
cones and holography, JHEP 01 (2014) 021 [arXiv:1308.5748] [INSPIRE].
[37] A. Bhattacharyya, A. Kaviraj and A. Sinha, Entanglement entropy in higher derivative
holography, JHEP 08 (2013) 012 [arXiv:1305.6694] [INSPIRE].
[38] D.V. Fursaev, A. Patrushev and S.N. Solodukhin, Distributional geometry of squashed cones,
arXiv:1306.4000 [INSPIRE].
[39] L.-Y. Hung, R.C. Myers and M. Smolkin, On holographic entanglement entropy and higher
curvature gravity, JHEP 04 (2011) 025 [arXiv:1101.5813] [INSPIRE].
[40] S. de Haro, S.N. Solodukhin and K. Skenderis, Holographic reconstruction of space-time and
renormalization in the AdS/CFT correspondence, Commun. Math. Phys. 217 (2001) 595
[hep-th/0002230] [INSPIRE].
[41] K. Skenderis, Asymptotically Anti-de Sitter space-times and their stress energy tensor,
Int. J. Mod. Phys. A 16 (2001) 740 [hep-th/0010138] [INSPIRE].
[42] M. Bianchi, D.Z. Freedman and K. Skenderis, Holographic renormalization,
Nucl. Phys. B 631 (2002) 159 [hep-th/0112119] [INSPIRE].
[43] K. Skenderis, Lecture notes on holographic renormalization,
Class. Quant. Grav. 19 (2002) 5849 [hep-th/0209067] [INSPIRE].
[44] V. Balasubramanian and P. Kraus, A stress tensor for Anti-de Sitter gravity,
Commun. Math. Phys. 208 (1999) 413 [hep-th/9902121] [INSPIRE].
[45] I. Papadimitriou and K. Skenderis, AdS/CFT correspondence and geometry,
hep-th/0404176 [INSPIRE].

– 39 –

JHEP03(2014)051

[30] P.D. Hislop and R. Longo, Modular structure of the local algebras associated with the free
massless scalar field theory, Commun. Math. Phys. 84 (1982) 71 [INSPIRE].

## PDF page 41

[46] V. Iyer and R.M. Wald, A comparison of Noether charge and Euclidean methods for
computing the entropy of stationary black holes, Phys. Rev. D 52 (1995) 4430
[gr-qc/9503052] [INSPIRE].
[47] R.M. Wald, General relativity, Chicago University Press, Chicago U.S.A. (1984).
[48] J. Lee and R.M. Wald, Local symmetries and constraints, J. Math. Phys. 31 (1990) 725
[INSPIRE].
[49] R.M. Wald, On identically closed forms locally constructed from a field, J. Math. Phys. 31
(1990) 2378.

[51] S. Hollands, A. Ishibashi and D. Marolf, Comparison between various notions of conserved
charges in asymptotically AdS-spacetimes, Class. Quant. Grav. 22 (2005) 2881
[hep-th/0503045] [INSPIRE].
[52] S. Hollands, A. Ishibashi and D. Marolf, Counter-term charges generate bulk symmetries,
Phys. Rev. D 72 (2005) 104025 [hep-th/0503105] [INSPIRE].
[53] O. Hohm and E. Tonni, A boundary stress tensor for higher-derivative gravity in AdS and
Lifshitz backgrounds, JHEP 04 (2010) 093 [arXiv:1001.3598] [INSPIRE].
[54] J. Smolic and M. Taylor, Higher derivative effects for 4D AdS gravity, JHEP 06 (2013) 096
[arXiv:1301.5205] [INSPIRE].
[55] R.C. Myers and A. Sinha, Holographic c-theorems in arbitrary dimensions,
JHEP 01 (2011) 125 [arXiv:1011.5819] [INSPIRE].
[56] T. Jacobson, Gravitation and vacuum entanglement entropy,
Int. J. Mod. Phys. D 21 (2012) 1242006 [arXiv:1204.6349] [INSPIRE].
[57] R. Guedens, T. Jacobson and S. Sarkar, Horizon entropy and higher curvature equations of
state, Phys. Rev. D 85 (2012) 064017 [arXiv:1112.6215] [INSPIRE].
[58] E. Bianchi, Horizon entanglement entropy and universality of the graviton coupling,
arXiv:1211.0522 [INSPIRE].
[59] T. Barrella, X. Dong, S.A. Hartnoll and V.L. Martin, Holographic entanglement beyond
classical gravity, JHEP 09 (2013) 109 [arXiv:1306.4682] [INSPIRE].
[60] T. Faulkner, A. Lewkowycz and J. Maldacena, Quantum corrections to holographic
entanglement entropy, JHEP 11 (2013) 074 [arXiv:1307.2892] [INSPIRE].
[61] D.A. Galante and R.C. Myers, Holographic Renyi entropies at finite coupling,
JHEP 08 (2013) 063 [arXiv:1305.7191] [INSPIRE].
[62] A. Kurusa, The Radon transform on hyperbolic space, Geometriae Dedicata 40 (1991) 325.

– 40 –

JHEP03(2014)051

[50] I. Papadimitriou and K. Skenderis, Thermodynamics of asymptotically locally AdS
spacetimes, JHEP 08 (2005) 004 [hep-th/0505190] [INSPIRE].
