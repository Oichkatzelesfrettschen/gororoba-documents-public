Source: https://arxiv.org/abs/2401.08346v2
PDF sha256: 2b81fcfabc5fea202d9f5e5680f4f58433fadbe75e2d6af0df418411168ee61c
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine (failed: characters)

# Transcription of anninos_2024_graviton_photon_expanding.pdf

Transcription of `anninos_2024_graviton_photon_expanding.pdf` in this directory, 27 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 25 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories; pages 1-24, 26-27 from the PDF's own text layer (pdftotext version 26.10.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Graviton-Photon Oscillations in an Expanding Universe
Peter Anninos∗1 , Tony Rothman †2 , and Andrea Palessandro‡3
1

Lawrence Livermore National Laboratory

arXiv:2401.08346v2 [gr-qc] 1 Apr 2024

2 New York University, Department of Applied Physics (retired)
3 Deloitte Consulting, Artificial Intelligence and Data

Abstract
Through the Gertsenshtein effect, the presence of a large external B-field may allow
photons and gravitons to mix in a way that resembles neutrino oscillations and is even
more similar to axion-photon mixing. Assuming a background B-field (or any field that
behaves like one), we examine the Gertsenshtein mechanism in the context of FLRW expanding universe models, as well as de Sitter space. The conformal invariance of Maxwell’s
equations and the conformal noninvariance of the Einstein equations preclude the operation of the Gertsenshtein effect at all scales. In general we find for the matter- and
radiation-dominated cases, graviton-oscillations are possible only at late conformal times
or when the wavelengths are much shorter than the horizon (kη ≫ 1), but that the timedependent oscillations eventually damp out in any case. The presence of charged particles
additionally damps out the oscillations. For the de Sitter universe, we find that oscillations are possible only at early conformal times (η ≪ H −1 ) and for wavelengths short
compared to the Hubble radius, but eventually freeze in when wavelengths become longer
than the Hubble radius. In principle a Gertsenshtein-like mechanism might influence the
balance of particle species in an inflationary phase before freezing in; however, we find
that in all our models the mixing length is larger than the Hubble radius. We discuss
several possible remedies to this situation.

1

Introduction

Sixty years ago Mikhail Gertsenshtein [1] demonstrated that the presence of a large external
magnetic field can cause gravitational and electromagnetic waves to mix, producing oscillations
that in certain respects resemble neutrino-flavor oscillations. In a recent paper [2] Palessandro
∗

anninos1@llnl.gov
tonyrothman@gmail.com
‡
apalessandro@deloitte.dk
†

1

## PDF page 2

and Rothman gave a straightforward derivation of the Gertsenshtein mechanism, also pointing
out that the axion-photon oscillations of current research interest are described by an essentially
identical process. In a companion paper [3] they showed that the self-interaction terms of the
Yang-Mills SU(2) field can take the place of Gertsenshtein’s external magnetic field to produce
oscillations between gravitational waves and Yang-Mills “bosonic waves.” Both processes are
classical, but in quantum language one can say that the external Maxwell or the Yang-Mills
magnetic field catalyzes the mixing of gravitons with photons or Yang-Mills bosons. Such a
description of course assumes that gravitons exist, a fact that has not, and perhaps never will
be experimentally established [4–7]. Yang-Mills SU(2) bosons are also entirely hypothetical.
The purpose of the present article is to investigate the behavior of the Gertsenshtein effect
in expanding FLRW universes. Several complications, however, make a consistent treatment
of both gravitational waves and electromagnetic waves on an expanding background nontrivial. First, the usual d’Alembertian form of the gravitational wave equation found in textbooks
gives incorrect results for nonstatic and curved spacetimes; one must therefore solve the full Einstein equations directly. Second, the introduction of an electromagnetic field with a preferred
spatial direction breaks the symmetries of the isotropic and homogeneous FLRW universe;
one must therefore either treat the waves as perturbations on an FLRW background or go to
an anisotropic or inhomogeneous model. Furthermore, Maxwell’s equations are known to be
conformally invariant (see Wald [9]). Numerous authors [11–15] have recently treated the consequences of this property in the context of cosmological electromagnetic fields. Its importance
for our investigation is that, while Maxwell’s equations are conformally invariant, Einstein’s
equations are not. Consequently, the symmetry between the gravitational wave equation and
the electromagnetic wave equation is destroyed, making their solution more difficult, as well as
immediately suggesting that the Gertsenshtein mechanism cannot operate at all scales.
In the following section we review the derivation of the Gertsenshtein effect given in [2].
As just implied, however, the comparatively simple formalism employed there cannot be consistently applied to an expanding cosmological model. We must therefore adopt a more so-

2

## PDF page 3

phisticated covariant description for both the underlying cosmology and the electromagnetic
field. After introducing the new formalism in §2 and deriving the relevant wave equations, we
then proceed to find solutions for the de Sitter universe (§3), radiation- and matter-dominated
universe (§4) and curvature-dominated universes (§5). For the latter cases, we find damped
mixing solutions at late times when particle wavelengths are much less than the Hubble radius1 , but that the solutions are frozen in at greater that Hubble-length scales, meaning that the
Gertsenshtein effect does not function in that regime. Surprisingly, for the de Sitter universe,
the opposite occurs. We find mixing solutions at early times, but not at late times. Thus, it
is possible that in an inflationary universe the Gertsenshtein mechanism might operate for a
time, until particle species are frozen out. Because the mixing length scale in today’s universe
is greater than the Hubble radius, the question arises as to whether it makes physical sense
to study the Gertsenshtein mechanism in expanding models. We discuss such issues in the
conclusion and propose several reasons why such a study might be reasonable.

2

Electrodynamics in an expanding universe

As discussed above, oscillations between electromagnetic and gravitational plane waves can be
made to take place when a large background magnetic field B0 couples the internal magnetic
field of an electromagnetic wave to the spacetime curvature produced by a gravitational wave
traveling in the same direction. The result is coherent oscillations between the electromagnetic
and gravitational wave; in particle language, the external magnetic field has catalyzed a resonant mixing between photon and graviton states. The derivation in [2] of this Gertsenshtein
mechanism basically amounts to simultaneously solving the Maxwell-Einstein vacuum equations along with the gravitational wave equation, assuming that the source consists entirely of
the system’s electromagnetic energy.
To summarize the procedure and introduce notation, for a flat, static spacetime we assume
1

usually, but incorrectly, referred to as the“horizon.”

3

## PDF page 4

as usual that the gravitational wave (GW) is represented by a weak perturbation hµν (x, t) ≪ 1
traveling on a Minkowski background such that the full metric is
gµν = ηµν + hµν ; g µν = η µν − hµν ; hµν ≡ η αµ η βµ hαβ ,

(2.1)

where the flat-space metric is given by ηµν = (−1, 1, 1, 1). In the standard transverse-traceless
(TT), or Lorenz, gauge, if the wave is assumed to be propagating in the z-direction, then
hµν = hµν (z, t) and the two independent polarizations of the GW are h11 = −h22 and h12 = h21 .2
In this situation the linearized gravitational wave equation is
□hµν = −16πGTµν .

(2.2)

and the stress-energy tensor is taken to be
1
4πTij = −(Ei Ej + Bi Bj ) + δij (E · E + B · B)
2

(2.3)

for total electric and magnetic fields of the system E and B. We assume that E is the electric
field of the photon alone (small), while B = B0 + b for external field B0 and photon magnetic
field b.
The vacuum Einstein-Maxwell equations, which describe the propagation of the electromagnetic wave (EMW) on a curved background, can be written as
1 √
√ ( −gg αµ g βν Fµν ),β = 0,
−g

(2.4)

where Fµν is the usual flat-space electromagnetic field tensor.
The trick in deriving the Gertsenshtein effect is to choose the external field B0 = constant
such that B0 ⊥ b and B0 ≫ b. This linearizes the equations; for b = by and B0 = B0x (2.2)
and (2.4) give to first order in hµν and b the coupled system
b̈y − b′′y = h′′12 B0 ,

(2.5)

ḧ12 − h′′12 = −4B0 by .

(2.6)

2

We use units in which G = c = 1 and follow MTW [8] conventions throughout. In particular, Greek indices
= 0...3 are spacetime indices, while Latin indices are spatial indices = 1...3. Repeated indices in any position
are summed.

4

## PDF page 5

(Here and below a dot (·) represents the time derivative and a prime (′ ) indicates differentiation
with respect to z.)
To establish graviton-photon mixing we search for “wavepacket” solutions to these equations, i.e., we assume that both b and h (dropping subscripts) are product functions of a rapidly
oscillating component and a slowly oscillating component:
h = hr (z − t)hs (z + t) ;

b = br (z − t)bs (z + t),

(2.7)

where “r” stands for “rapid” and “s” stands for slow. In the cases of interest, these expressions
can be also written as
h(z, t) = Aeiωr (z−η) e−iωs (z+η)

;

b(z, t) = Beiωr (z−η) e−iωs (z+η) ,

(2.8)

with ωr ≫ ωs . The product decomposition allows us to find the beat frequency between the
GW and the EMW, which is represented by the frequency of the slow component, ωs . One
finds for the system (2.5)-(2.6)
)
)
(
(
√
z+t+φ
z+t+φ
; bs = A B0 cos
,
hs = A sin
L
L

(2.9)

provided that L ≡ 2/B0 . Notice that

h2s +

b2s
= A2 = constant,
B0

(2.10)

which is a statement that energy is conserved under graviton-photon oscillations.
The quantity
L=

2
1
=
B0
ωs

is the mixing length of the Gertsenshtein mechanism. In cgs units
(
)
1 Gauss
2c2
≈ 2Mpc
L= √
.
B0
GB0

(2.11)

(2.12)

The strength of the intergalactic magnetic field is not known with any certainty, but
B0 ≈ 10−9 G appears to represent something like an upper limit (cf. [16]). For this value
of B0 today’s mixing length, L0 is far greater than the Hubble radius of the universe, although
5

## PDF page 6

around magnetars, where B0 ∼ 1014 G, the mixing length can be only ∼ 106 km, making
neutron stars plausible graviton factories.

As already mentioned in the Introduction, given that L0 is much greater than the Hubble radius, one can legitimately ask whether it makes physical sense to consider cosmological
photon-graviton mixing. We delay discussion of this question until §6, after presentation of
our results. The immediate technical difficulty confronting us is that due to the other issues
discussed in the Introduction, the above formalism, in particular the underlying equations (2.1)
- (2.4), cannot be consistently applied to the expanding universe scenario. We therefore adopt
an approach similar to the one employed by Anninos [10] for representing conformally decomposed matter-filled spacetimes and by Tsagas [11] for the elecromagnetic field description, both
of which use a covariant 3 + 1 splitting of spacetime.
We write the general plane-symmetric, conformally decomposed metric in the form gµν =
−dt2 + γij dxi dxj for both flat and non-flat topologies, with


a1 (t)(1 − f (t, z))
h(t, z)
0
2
2
a(t) 
a(t)
γ̂ij =
h(t, z)
a2 (t)(1 + f (t, z))
0  ,
γij =
2
R(r)
R(r)2
0
0
a3 (t)

(2.13)

where R(r) = 1 + κr2 /4, κ = −1, 0, + 1 for open, flat, and closed spacetimes respectively,
r is related to the usual radius via r = r/(1 + κr 2 /4), and h(t, z) and f (t, z) are first order
(gravitational wave) perturbations. The ai (t) are constrained such that the determinant of the
conformal metric γ̂ij is unity (|γ̂| = 1), while a(t) is the conformal factor which, for the case of
matter dominated isotropic cosmologies takes the familiar form a(t) ∝ t2/3 .
In order to simplify our analysis, however, we consider only cross-polarized gravity waves
and set f = 0 throughout. Further simplifications are made by adopting a geodesic slicing
condition (unit lapse α = 1, zero shift β i in the 3+1 convention), isotropic background (constant
∫
and equal ai ), and (later) a conformal time coordinate η = dt/a(t).
The total stress energy tensor is a linear combination of matter (perfect fluid plus cosmo-

6

## PDF page 7

µν
µν
logical constant) and electromagnetic fields T µν = Tm
+ Tem
, with

Λ µν
µν
g ,
Tm
= ρh uµ uν + PT g µν → ρE uµ uν + P hµν −
8π

(2.14)

and
1
µν
= Fλµ F νλ − g µν F λκ Fλκ
4πTem
4
1 α
= (E Eα + B α Bα ) (hµν + uµ uν ) − (E µ E ν + B µ B ν ) + 2u(µ ǫν)αβ Eα Bβ ,
2

(2.15)
(2.16)

where F µν is the Faraday tensor, Λ is the cosmological constant, ρh = ρ + e + P is the proper
relativistic enthalpy, uµ is the covariant 4-velocity, and hµν = gµν + uµ uν is the projection
operator orthogonal to the fluid frame. For simplicity we assume a barotropic equation of
state P = wρE while absorbing the internal energy into a total energy density ρE = ρ + e.
The barotropic coefficient w relates to the usual adiabatic index via w = γ − 1. This form
conveniently accommodates dust w = 0 (γ = 1), non-relativistic matter w = 2/3 (γ = 5/3),
and relativistic matter or radiation w = 1/3 (γ = 4/3).
For the electromagnetic field we follow the convention in [2, 3] and define weak (relative to
the background energy density) electromagnetic field vectors of the form
E i = a(t)−3 [e(t, z), 0, 0] ,

(2.17)

B i = a(t)−3 [B0 , b(t, z), 0]

(2.18)

where B0 is the constant value of the external magnetic field, and the factor a(t)−3 is introduced to scale away the metric determinant and simplify the resulting differential equations.
Perturbation equations for the metric and fields are derived assuming B02 ≪ ρE a4 to preserve
isotropy at zero order. Formally we have introduced two smallness parameters defining the
field strength relative to the dominant cosmological energy density ǫ ≡ B µ Bµ /ρE ≪ 1, and the
gravitational wave amplitude. We point out the electromagnetic energy density B µ Bµ scales to
lowest order as ∝ B02 a−4 , similar to ρE as expected for radiation-like behavior consistent with
magnetic flux conservation.3
Note for B0 = 0 in 2.18, B 2 = Bi B i ≡ a2 B i B i = a−4 b2 , implying that adiabatic decay of B 2 ∝ a−4 is
satisfied by b = constant, and therefore b is interpreted as the magnetic flux.
3

7

## PDF page 8

It is not possible to derive plane wave equations in non-flat spacetimes except in the limit of
small (localized) spatial volumes such that r ≪ 1. Moreover, in order to pick up all contributions
to the field equations from curvature it is important to keep spatial derivatives throughout the
complete derivation of the second order PDEs due to the 3D nature of the metric and use
of Cartesian coordinates. For this purpose we evaluate the following second order differential
representation of Maxwell’s equations
□F ab + g be ∇d ∇e F da + g ae ∇d ∇e F bd = 0 ,

(2.19)

before taking the limit (x, y, z) → 0.
In the r ≪ 1 limit we derive general differential equations applicable to all the spacetimes
considered in this paper. For the GW:
h′′
κ
ȧ
4
+ 3 ḣ − 2 h + 4 B0 b = 0.
2
a
a
a
a

(2.20)

B0 ′′
κ
b′′ ȧ
+
ḃ
−
h
+
(2b + B0 h) = 0.
a2 a
a2
a2

(2.21)

ḧ −
For the EMW:
b̈ −

For the background (isotropic) expansion:
ȧ2 Λ
8πρ0
κ
− − 3(1+w) + 2 = 0 ,
2
a
3
3a
a

(2.22)

where ρ0 is a constant defining the total energy density of matter or radiation. Notice we
have neglected electromagnetic field energy from the background expansion as a higher order
contribution, which would otherwise have appeared as ∝ B02 /a4 . Also, (2.21) reduces to that
in [11] when B0 = 0.
The above equations simplify considerably when rewritten in conformal time η ≡
giving

∫

dt/a(t),

4
ȧ
ḧ − h′′ + 2 ḣ − κh + 2 B0 b = 0 ,
a
a

(2.23)

b̈ − b′′ − B0 h′′ + κ (2b + B0 h) = 0 ,

(2.24)

8πρ0
B02
ȧ2 Λa2
−
−
−
+κ=0 ,
a2
3
3a1+3w 3a2
8

(2.25)

## PDF page 9

where for future reference (§6) we have now included the (assumed small) magnetic field energy
density in the Friedmann equation.
The most obvious feature of the above is that the GW equation contains a damping term,
while the B-field equation does not. This is a reflection of the conformal invariance of Maxwell’s
equations and will be responsible for much of the behavior of the solutions.
We also point out that to close equations (2.23) - (2.25) we need an explicit expression
for the scale factor as a function of (conformal) time, essentially a solution to the Friedmann
equation (2.25). In general this is not trivial, and so in order to retain these equations in
manageable form, we consider only solutions in regimes where the scale factor is approximated
by a simple power law or exponential. In the following sections, we discuss each of these
standard cases, finding analytic solutions at both early and late cosmological times.

3

de Sitter space

Here we examine the flat (κ = 0), exponentially expanding case a = eHt , which written in
conformal time is
a(η) = (1 − Hη)−1.

(3.26)

Note that H 2 = Λ/3 for cosmological constant Λ and that from (2.25) with ρB ∼ B 2 ∝ a−4 , we
are tacitly assuming the constraint B02 /a4 ≪ Λ. In the de Sitter model, equations (2.23) and
(2.24) become
H
ḣ + 4 (1 − Hη)2 B0 b = 0,
(1 − Hη)
′′
b̈ − b − B0 h′′ = 0.
ḧ − h′′ + 2

(3.27)

This system evidently has analytic solutions for both early and late times. For early times
Hη ≪ 1, and so we have simply
ḧ − h′′ + 2(aH)ḣ + 4B0 a−2 b = 0,
b̈ − b′′ − B0 h′′ = 0.

(3.28)

(Although a ≈ 1 at early times we have explicitly included it here in order that the
mixing length L be expressed as a function of the scale factor; see e.g. 3.35.) Now following
9

## PDF page 10

the procedure of [2] and [3] we assume a wave packet solution of the form (2.7)-(2.8), where
the rapidly varying components br and hr describe the propagation of electromagnetic and
gravitational wave packets of energy ωr , while the slowly varying components bs and hs describe
the coherent oscillations between them with frequency ωs ≪ ωr . However, since (3.28) for h
includes a damping term, we anticipate that its solution should contain a factor e−γη with
damping constant γ and modify the ansatz slightly to read
h(z, η) = Aeiωr (z−η) e−iωs (z+η) e−γη ,
b(z, η) = Beiωr (z−η) e−iωs (z+η) .

(3.29)

Substituting the expression for h into the first of (3.28) gives
[
]
A −4ωr ωs + 2iγ(ωr + ωs ) − 2iaH(ωr + ωs ) + γ 2 − 2aHγ e−γη = −4BB0 a−2 .

(3.30)

The imaginary part must vanish, implying that γ = aH. Also, Hη ≪ 1, so we can assume
eHη ≈ 1. Thus

4B0 a−2
A
=
.
B
4ωr ωs + (aH)2

(3.31)

4Bωr ωs = AB0 (ωr − ωs )2 ≈ AB0 ωr2,

(3.32)

A
4ωs
.
=
B
B0 ωr

(3.33)

Substituting the anzatz for b into the second of (3.28) gives

or

Eliminating A/B from the above two equations yields a quadratic equation with solutions
√
[
]
(aH)2
B02 ωr2a−2
ωs = −
1 ± 1 + 16
.
(3.34)
8ωr
(aH)4
Thus, contrary to the static case, in de Sitter the mixing frequency depends on ωr , as well as
on H. The overall sign in (3.34) is not important and can be changed by choosing ωs positive
in (3.29), which does not alter the underlying interpretation that ωs is the beat frequency
produced by the superposition of two waves traveling in the same direction. The choice of sign
for the radical reflects two different solutions for the decoupled GW and EMW equations in the
10

## PDF page 11

limit B0 = 0. When B0 = 0, equation (3.30) is satisfied for (non-zero) GWs h by choosing the
positive radical, which results in ωs = −(aH)2 /4ωr ; the negative radical gives ωs = 0, which is
appropriate for linearized plane wave solutions of equation (3.32) for b.
Despite that for B0 = 0 the GW solution is ωs = (aH)2 /4ωr , from (2.23) and 2.24 it is
evident that in this limit for FLRW models the coupling between b and h vanishes. Thus no
graviton-photon mixing can be taking place. The GW and EMW oscillate independently; the
beat frequency ωs in the metric perturbations evidently arises through a natural “resonance”
with the background expansion that dampens gravitational waves at the Hubble rate, and
which vanishes as H → 0.
Note that in the limit B0 ωr ≫ (aH)2 , (3.34) gives for either sign option
L≡

2a
1
=
,
ωs
B0

(3.35)

which reduces to the static result (2.11) for a → 1, as expected.
Although we have thus far made only an early time approximation, the damping of h
strongly suggests that the Gertsenshtein mechanism cannot function forever in the de Sitter
universe; either the gravitational waves effectively disappear or, as is known [17], they freezeout when their wavelengths reach superhorizon scales, causing mixing to cease. This suspicion
is confirmed by examining the late-time behavior of Eqs. (3.27).
To find a late-time solution, let ε ≡ (1 − Hη). Then
h′′
4B0 b
2
ḧ − ḣ − 2 = − 2 ε2 ,
ε
H
H
2
′′
′′
H b̈ − b = B0 h ,

(3.36)

where (·) now indicates d/dε. We assume a separable solution h = h(ε)h(z). The equation for
h(z) is simply
h′′ (z) = −k̂ 2 H 2 h(z),

(3.37)

where k̂ 2 is the (dimensionless) separation constant. The above of course implies oscillatory
behavior h(z) ∼ e−ik̂Hz . For the homogeneous (B0 = 0) case, the equation for h(ε) becomes
2
ḧ(ε) − ḣ(ε) + k̂ 2 h(ε) = 0,
ε
11

(3.38)

## PDF page 12

which is Bessel’s equation with solutions
h(ε) = ε+3/2 J(k̂ε)±3/2 .

(3.39)

Since the late-time behavior of the system corresponds to ε → 0, we can expand the Bessel
functions in powers of ε and retain the first few terms. To order ε2
h(ε) = h0 +

k̂ 2
h0 ε2
2

(3.40)

satisfies the homogeneous equation (B0 = 0) to lowest order. If for the inhomogeneous case we
keep the same form for h(ε) and additionally expand b as
b(ε) = b0 + b1 ε2 ,

(3.41)

with the same spatial dependence as h(z), we find upon substituting into (3.36) that the
solutions
k̂ 4 H 2 h0
,
8B0
B0 k̂ 2 h0
,
b1 = −
2

b0 = −

(3.42)
(3.43)

satisfy both the GW and EMW equations to order H 2 k̂ 4 /B02 ≪ 1 in the long wavelength limit
√
k ≡ k̂H ≪ aH; here we have had to additionally impose the condition that B0 ≪ Λa2 = Ha2
for de Sitter (see (2.25)).
For a less restrictive condition on the wavelength, the ansatz
)
(
k̂h0 B0 c2
ε2 ,
+
h = h0 + B0 c1 +
2
2

(3.44)

which reduces to the previous when B0 = 0, leads to h = b = 0 to order ε2 , which of course
precludes any oscillations, including waves of the type (3.29).4
We therefore conclude that the Gertsenshtein effect is inoperable in de Sitter space at late
times Hη ⪅ 1.
4

Note that solutions (3.29) are separable; we merely wrote them in a way to emphasize their wavelike
character.

12

## PDF page 13

4

Radiation- and matter-dominated universes

For the RD and MD universes, equations (2.23) and (2.24) become
p
4B0 b
ḧ − h′′ + 2 ḣ − κh = −
,
η
(η/η0 )2p
b̈ − b′′ + 2κb = B0 (h′′ − κh),

(4.45)

where (η/η0 )p = a and p = 1, 2 for the RD and MD cases, respectively. Here, we must assume
that |B|2 ≪ ρE , or equivalently B02 ≪ ρE a4 . Additionally, since we retain curvature in these
equations we must also have κ ≪ ρE a2 , but leave open for the moment the relative scaling
between magnetic field strength and curvature.
As in the late time de Sitter case, we first solve these equations by separation of variables.
For h = h(η)h(z) with separation constant k, we have for the flat-space decoupled situation
p
ḧ(η) + 2 ḣ + k 2 h(η) = 0 ;
η

h′′ (z) = −k 2 h(z).

(4.46)

The former is again a Bessel equation, and so the full (decoupled) inhomogeneous solutions are
RD : ho (z, η) ∝ η −1/2 J±1/2 (kη)e−ikz

MD : ho (z, η) ∝ η −3/2 J±3/2 (kη)e−ikz

;

(4.47)

Guided by these solutions, we now attempt to solve the inhomogeneous equations for the
RD and MD cases in the limits kη ≪ 1 and kη ≫ 1.

4.1

Radiation-dominated, kη ≪ 1

This represents solutions for which λ ≫ η ∼ H −1 , in other words “superhorizon” (super–
Hubble-radius) evolution. Since we are also restricted to r ≪ 1, it also represents very early
times. The asymptotic form of the J1/2 Bessel function for small argument suggests we try
solutions of the form
h = [h0 + h1 (kη)2 + h2 (kη)4 ]e−ikz ,
b = [b1 (kη)2 + b2 (kη)4 ]e−ikz .

13

(4.48)

## PDF page 14

Inserting these expressions into (4.45) and equating powers of η leads to four equations for the
five constants. After some algebra we find
B0 h0
(1 + κ) ,
2(
)
1−κ
b1
2 2
− 2B0 η0 ,
=
3B0 1 + κ
(
)
b1
5
2 2
=
B0 η0 (1 + κ) − κ − 2 ,
18
2
(
)
2
(1 − κ)
1 2 2
b1
2 4 4
+ B0 η0 (κ − 10) + B0 η0 (1 + κ) ,
= −
60B0
1+κ
3
3

b1 = −
h1
b2
h2

(4.49)

where κ = κ/k 2 , and h0 is a freely specifiable parameter. These solutions satisfy both field
and gravity wave equations to order (kη)4 , and have the identical power-law behavior as in the
decoupled (B0 = 0) case.
We note that these solutions are compatible with those of Tsagas [11] and Grishchuk [18]
for the “superadiabatic” amplification of EMWs and GWs, meaning that the magnetic flux b
increases over time5 and h falls off more slowly than a−1 at “superhorizon” scales.6 The exact
time dependence of b for the growing modes considered here differs from Tsagas’s, given that
he assumed an exponential solution a ∼ eη and we have assumed a power law a ∼ η p . Our time
dependence for h is exactly that of Grishchuk for both the RD and MD cases (cf. §4.3, below).
For us the important point is that, because these solutions are not oscillatory, they once
again preclude the Gertsenshtein effect from operating in this regime.

4.2

Radiation-dominated, kη ≫ 1

This represents “subhorizon” (sub–Hubble-radius) late-time behavior.
We directly attempt to find a mixing solution. Analogously to de Sitter we assume
b(z, η) = Beiωr (z−η) e−iωs (z+η) (kη)n ,
h(z, η) = Aeiωr (z−η) e−iωs (z+η) (kη)m .
5
6

See footnote 3
ρh ∝ ḣ2 ∝ ω 2 h2 . Both ω and h decrease as a−1 , so ρh ∝ a−4 .

14

(4.50)

## PDF page 15

Equation (4.45) for h then gives
−4ωr ωs −

m(m + 1)
B
2i(m + 1)
(ωr + ωs ) +
−
κ
=
−
4B0 k 2 η02 (kη)n−m−2 .
2
η
η
A

(4.51)

Note that choosing m = −1 causes the imaginary part and higher-order terms on the left to
vanish, resulting in the correct asymptotic form for the decoupled solution (4.47). Similarly,
(4.45) for b gives
−4ωr ωs − i

n(n − 1)
A
2n
(ωr + ωs ) +
+ 2κ = −B0 ((ωr − ωs )2 + κ) (kη)m−n .
2
η
η
B

(4.52)

Here, choosing n = 0 causes the imaginary part to vanish, meaning that b is undamped. Now,
with (ωr − ωs )2 ≈ ωr2 , (4.52) becomes
−4ωr ωs − i

n(n − 1)
2n
A
(ωr + ωs ) +
+ 2κ = −B0 (ωr2 + κ) (kη)m−n ,
2
η
η
B

(4.53)

or
B
(kη)m−n B0 (ωr2 + κ)
.
=−
A
−4ωr ωs − 2in(ωr +ωs ) + n(n−1)
+
2κ
2
η

(4.54)

η

Inserting this into (4.51) yields, for any n, m,
(
)
2i(m + 1)
m(m + 1)
−4ωr ωs −
(ωr + ωs ) +
−κ
η
η2
)
(
4B02 η02 k 2 (ωr2 + κ)
2in(ωr + ωs ) n(n − 1)
+
+
2κ
=
.
× −4ωr ωs −
η
η2
(kη)2

(4.55)

Notice that the RHS is independent of n, m. Thus, since kη ≫ 1, if we neglect all terms with
powers of kη in the denominators for a lowest-order approximation, we can equate either factor
in parentheses to zero, which is the same as setting the LHS of (4.51) or (4.52) to zero with the
higher-order terms neglected. The result is:
ωs =

κ
−κ
,
.
2ωr 4ωr

(4.56)

Since the coupling with B0 has been neglected, this evidently represents a “curvature-induced”
resonance similar to the effect discussed in §3, but it does not represent graviton-photon mixing.

15

## PDF page 16

If we now restrict ourselves to the physically motivated solution m = −1, then in (4.55)
we must have n = 0 to kill the imaginary part and retain a non-negligible coupling term. This
results in the quadratic
2B0 η02 (ωr2 + κ)
= 0,
η2

(4.57)

√
[
]]
[
2B02 η02 (ωr2 + κ)
κ
1± 1+8 1+
.
ωs =
8ωr
κ2 η 2

(4.58)

8ωr2 ωs2 − 2ωr ωs κ − κ2 −
with solution

Notice that if the last term is neglected then the roots are the same as the frequencies (4.56).
On the other hand, in the high frequency limit (ωr2 ≫ κ) the result simplifies to
B0
,
2a

(4.59)

2a
1
=
,
ωs
B0

(4.60)

ωs =
or equivalently
L=

which again recovers the static solution for the mixing length.
Since n = 0 in this case, the amplitude of b remains constant. We interpret this to be a
result of the conformal invariance of the electromagnetic field discussed earlier. Regardless of
the choice of m and n, however, the result suggests that in flat space (with zero or negligible
curvature) the mixing frequency decreases as the universe expands until there is no mixing
whatsoever and the Gertsenshtein effect ceases to operate.
We make a final point regarding the curvature terms in the above equations. In deriving these solutions we have implicitly assumed that radiation (not curvature) determines the
background cosmology. The Friedmann equation
ȧ2 =

8πρ0 η02
8πρ0
−
κ
=
−κ
3a1+3w
3η 2

(4.61)

puts a relative scale on the curvature terms, which is valid for both RD (w = 1/3) and
MD (w = 0) models. To satisfy radiation-dominance (or dust-dominance, next section) with
κ = ±1, we require 8πρ0 η02 /3η 2 ≫ 1. Together with the subhorizon condition (kη) ≫ 1, the
16

## PDF page 17

solutions in this section are therefore valid only for 1 ≪ (kη)2 ≪ 8πρ0 k 2 /3, effectively putting
a time limit on their validity. Beyond this limit we must consider solutions in a curvaturedominated regime, which we do in §5.

4.3

Matter-dominated, kη ≪ 1

This represents early-time, “superhorizon” (super–Hubble-radius) solutions.
The asymptotic form of J3/2 in (4.47) for small argument suggests that for the coupled case
we attempt a solution of the form
h(η) = h0 + h1 (kη)2 + h2 (kη)4 ,
b(η) = b0 + b1 (kη)4 + b2 (kη)6 .

(4.62)

Inserting this ansatz into (4.45) and defining κ = κ/k 2 as we did earlier, gives h0 = b0 = 0
along with
12b1
,
B0 (1 + κ)
b1 4 − κ
,
=
6B0 1 + κ
b1
= −
(10 + 11κ) ,
180

h1 = −
h2
b2

(4.63)

where b1 is arbitrary, but because h0 = 0 one finds two conditions relating h1 and b1 , which
result in the constraint
B02 k 2 η04 (1 + κ) = 30 .

(4.64)

Again, since these solutions are frozen-in, rather than oscillatory, the Gertsenshtein effect is
evidently inoperable in this regime.

4.4

Matter-dominated, kη ≫ 1

This represents late-time, “subhorizon” (sub–Hubble-radius) solutions.

17

## PDF page 18

We follow the identical procedure as for the RD κη ≫ 1 case. The only difference is that
in (4.45) p = 2. Assuming ansatz (4.50) for b and h, the GW equation becomes
−4ωr ωs −

m(m + 3)
B
2i(m + 2)
(ωr + ωs ) +
− κ = − 4B0 k 4 η04 (kη)n−m−4 .
2
η
η
A

(4.65)

Note that in this case m = −2 causes the imaginary part to vanish and gives the correct asymptotic behavior for the decoupled solution. Eq. (4.52) for b is unchanged, and so eliminating
B/A as before gives for m = −2
)(
)
(
2n(ωr + ωs ) n(n − 1)
4B02 k 4 η04 (ωr2 + κ)
2
−4ωr ωs − i
+
+
2κ
=
,
−4ωr ωs − 2 − κ
η
η
η2
(kη)4
(4.66)
where we have also set (ωr − ωs )2 ≈ ωr2 . The lowest-order constant solutions found by ignoring
all higher-order terms (kη)−1 and smaller (including the coupling term), are the same as in the
RD case:
ωs =

−κ
κ
,
.
2ωr 4ωr

(4.67)

If we additionally set n = 0, the remaining imaginary term vanishes, as well as the n(n − 1)
term, and the coupling term can be retained to derive a time-dependent mixing frequency. In
this case the resulting quadratic becomes
)
(
2κ 2B02 η04 (ωr2 + κ)
4ωr
2
2 2
−
2ω
κ
−
κ
−
−
= 0,
8ωr ωs + ωs
r
η2
η2
η4

(4.68)

with solutions
1
ωs =
8ωr

[(

2
κ− 2
η

)

2
± 2
η

√

]
9
1 + 4B02 η04 (ωr2 + κ) + 3κη 2 + κ2 η 4 .
4

(4.69)

We point out three particularly interesting limits in this expression. In the limit of zero
curvature κ → 0:

[
]
√
1
2 4 2
1 ± 1 + 4B0 η0 ωr ;
ωs = −
4ωr η 2

(4.70)

1
B0
≡ ωs =
;
L
2a

(4.71)

in the high-frequency ωr2 ≫ 1 where we once again recover the static solution:

18

## PDF page 19

and at extremely short wavelengths (kη) ≫ 1:
ωs =

κ
−κ
,
,
2ωr 4ωr

(4.72)

where we recover both earlier solutions (4.67) obtained by dropping all high order terms.
We thus see that the Gertsenshtein effect is operable in this regime, but that the timedependent solution damps out at an even faster rate than in radiation-dominated models.

We should also make a note concerning the presence of charged particles in RD and MD
models. In the real universe, recombination occurs at z ∼ 103 , when the universe is already
matter dominated. Above recombination temperatures, one would not expect the Gertsenshtein
mechanism to operate in the standard RD model due to Thomson scattering of photons off free
electrons, which makes the universe opaque to electromagnetic radiation. Below recombination
temperatures and above reionization (the ”dark ages”) one can model the presence of charged
particles in a somewhat ad hoc fashion similarly to the procedure in Domcke and Garcia2
Cely [19] by adding a term (ωp0
/a)b (in conformal time) to the LHS of the second of the wave
√
eqs. (4.45). Here, ωp0 ≡ e2 ne0 /me is today’s value of the plasma frequency. For the current

value of B0 ≲ 10−9 G, our requirement that B02 ≪ ρ0 for a RD or MD universe is easily met,

as is the constraint that kη ≫ 1 for EMWs. Then, repeating the above derivation for the MD
case, the solution becomes


√
4 4
ω
η
1 
2
3
2
9
p
.
ωs =
κ − 2 + ω 2p ± 2 1 + 4B02 η04 (ωr2 + κ) + 3κη 2 + κ2 η 4 + ω 2p κη 4 + ω 2p η 2 +
8ωr
η
η
4
2
4
(4.73)

2
2 2
/a = ωp0
η0 /η 2 .
where ω 2p ≡ ωp0

In the case that spatial curvature is negligible, and ignoring all but the frequency-dependent
terms appropriate for the high frequency limit, (4.73 reduces to
√
[
]
2 2
ω 2p
16B ω
ωs =
1 ± 1 + 2 04 r .
8ωr
a ωp

(4.74)

When the second term under the radical dominates, this expression becomes our previous result
ωs = B0 /2a. For ωp0 ∼ 1 Hz, as in [19], that takes place when ωr ≳ 10 MeV. Below these
19

## PDF page 20

4
energies effects of the plasma need to be taken into account. We see that when ωp0
≫ 16B02 ωr2

with the (+) root, the above reduces to
L−1 = ωs =

2
2
ωp0
ωp0
=
,
4aωr
4ωr0

(4.75)

independent of redshift, since ωr = ωr0 /a. When evaluated in terms of coordinate time, this
2
expression agrees with the one given in [19], ωs ∼ (1 + z)2 ωp0
/4ωr0.

However, this result should not be interpreted as the mixing length associated with the
Gertsenshtein effect: Since B0 no longer appears in (4.75), graviton-photon oscillations cannot
take place. Instead, it gives a “coherence length” or “skin depth” above which the EMW does
not propagate. On the other hand, after expanding the radical in (4.74) when the plasma
frequency dominates, the negative root provides a rough scaling of the Gertsenshtein effect
ωs ∝ B02 ωr /(aωp )2 , which has the anticipated behavior that ωs → 0 when B0 → 0, ωp → ∞,
and a → ∞. We note that the inclusion of electric charges produces results similar to those
pointed out by Zel’dovich in his original objections to the Gertsenshtein effect [20].

5

Curvature-dominated universe

As discussed in §4.2, the RD and MD cases have a limited domain of validity, after which the
model becomes curvature dominated. For the CD regime, the Friedmann equation in conformal
time (2.25) becomes simply

( )2
ȧ
= −κ,
a

(5.76)

for κ = ±1. Here we must assume the constraint B02 ≪ |κ|a2 . Curvature-dominance simplifies the GW equation (2.23 considerably by replacing a time-dependent expansion rate in the
damping term by the constant H ≡ ȧ/a. Perhaps not surprisingly, equations (2.23) and (2.24)
can then be satisfied by the same ansatz (3.29) we employed in the de Sitter case, which is
applicable to both positive and negative curvature.
Substituting the expressions (3.29) into (2.23) and (2.24), we find from the GW equation
)
[
]
(
A −4ωr ωs + 2i(ωr + ωs )(γ − H) − 2Hγ + γ 2 − κ = −B 4B0 a−2 eγη ,
20

(5.77)

## PDF page 21

and from the EMW equation
[
]
AB0 (ωr − ωs )2 + κ = −B (2κ − 4ωr ωs ) eγη .

(5.78)

Again, these expressions are valid for both positive and negative curvature spacetimes, which
in the regime considered here differ only by the value of H.
At this point the positive and negative curvature solutions take different forms, depending
on whether H is real or imaginary (the latter will be true in the closed κ = +1 topology with
its oscillatory behavior.) For κ = −1, requiring that the imaginary parts of equation (5.77)
vanish gives γ = H = 1. Then solving (5.77) and (5.78) together to eliminate A/B gives
B02
(1 + 2ωr ωs )
.
=
(ωr − ωs )2 − 1
2a2 ωr ωs
This is a quadratic equation for ωs and with (ωr + ωs )2 ≈ ωr2 , yields
[
]
√
4B02 (ωr2 − 1)
1
ωs =
−1 + 1 +
.
4ωr
a2

(5.79)

(5.80)

We have chosen the (+) root in (5.80) because B0 = 0 in (5.77) implies ωs = 0. When the
second term in the discriminant dominates and ωr ≫ 1 and a = 1, this result reduces to the
static case (2.11). The condition ωr ≫ 1 is, inserting dimensions, really ωr ≫ H; thus ωr ≫ 1
is satisfied for any wave whose period is much shorter than H −1 . Moreover, the utility of the
plane-wave ansatz evidently assumes that a ∼ constant, in which case the GW equation becomes essentially that of a damped harmonic oscillator. Consequently, ωr ≫ 1 should hold in
any remotely plausible scenario. We also see, however, that a = 1 gives the maximum value of
ωs and as the universe expands, ωs decreases monotonically to zero, quenching photon-graviton
oscillations.

For the κ = +1 case, H = ±i. In order for the imaginary part of (5.77) to vanish, one
must take γ = 0, leaving
(
)
A [−4ωr ωs − 1 ± 2(ωr + ωs )] = −B 4B0 a−2 eγη .
21

(5.81)

## PDF page 22

Similarly to above, with (5.78) this gives for H = +i
4B02
(4ωr ωs − 2)
=
.
(ωr − ωs )2 + 1
a2 [4ωr ωs − 2(ωr + ωs ) + 1]

(5.82)

Assuming again that ωr ≫ ωs , we get the quadratic dispersion relationship
16ωr2ωs2 − 4ωr (2ωr + 1)ωs + 2(2ωr − 1) −

4B02 (ωr2 + 1)
= 0,
a2

which can be solved for ωs to get
[
]
√
2
2
16B
(ω
+
1)
1
0
r
1 + 2ωr ± 4ωr2 − 12ωr + 9 +
ωs =
.
2
8ωr
a

(5.83)

(5.84)

For B0 = 0, (5.81) requires ωs = 1/2. This is obtained with the positive root in (5.84) and
the previous assumption that ωr ≫ 1. The static limit is recovered when the last term in the
discriminant dominates and a ∼ 1, but more generally we have for the mixing length
L=

2a
1
=
.
ωs
B0

(5.85)

Note that despite the presence of a in all our expressions for L, they represent comoving lengths,
since ωs = ks comes from e−iks (z+η) , where z is a comoving coordinate.

6

Discussion

We have shown that in radiation- and matter-dominated models, the Gertsenshtein mechanism
can operate in the limit kη ≫ 1, that is at times and spatial scales when the graviton or
photon wavelength is much shorter than the Hubble radius. For curvature-dominated models,
we found mixing solutions for both positive and negative curvature, assuming only that the
expansion rate is slow compared to the particle frequency. Nevertheless, in all these cases it
appears that oscillations damp out as the universe expands. For the de Sitter universe we found
similar behavior: the Gertsenshtein effect can take place only at early times (η ≪ H −1 ) and for
perturbation wavelengths much smaller than the Hubble radius. In all cases, for superhorizon
wavelengths, the perturbations freeze in and oscillations cease.
22

## PDF page 23

When the effect of charged particles are included (during the “dark ages”) we find that
charge density oscillations at the plasma frequency impose a strong constraint on photongraviton mixing, essentially suppressing mixing at EMW frequencies below ∼ 10 MeV, and,
as discussed earlier, causes the mixing frequency to decrease with the square of the plasma
frequency (within the coherence length of Gertsenshtein mixing). Such effects are not important for a curvature-dominated universe or a cosmological-constant–dominated universe, where
coupling to GWs occur through the spacetime geometry, not its matter content. For radiationdominated models we do not expect the Gerstenshtein effect to operate at all, due to Thomson
scattering of EMWs off electrons.
Turning to regimes where the GE operates without plasma dissipation, and given that
today’s intergalactic magnetic field ≲ 10−9 G implies that the mixing length for gravitonphoton conversion is ≳ 105 Hubble radii, we should confront the question raised at the start of
this paper: Does a “cosmological” Gertsenshtein effect have any observable consequences?
Initially, one might hope that it does. Presumably, the cosmological magnetic field was
much larger in the early universe than it is today, and the Gertsenshtein effect (or similar mixing
process, such as axion-photon mixing or graviton-Yang-Mills-boson mixing) could conceivably
provide a mechanism for altering the balance of particle species during an inflationary phase.
Our current assessment is, however, that the outlook appears not to be bright. In conformal
time the Hubble radius is H −1 = a2 /ȧ. The proper mixing length, for all models and regimes
where the GE operates unhindered, is Lp = aL = 2a2 /B0 for constant B0 . Notice, however,
that this can be written as Lp = 2/|B|, where |B| = B0 /a2 is the magnitude of the background
field when B is defined covariantly as in (2.18). Thus Lp evidently gives an “invariant” measure
of the mixing length, which can be applied to both the static or expanding cases. Hence in
general
2ȧ
Lp
=
.
−1
H
B0

(6.86)

For the RD and MD cases respectively, the Friedmann equation (2.25) then shows
√
ρ0
Lp
≫1 ;
≈
−1
H
B0
23

√
aρ0
Lp
≫ 1.
≈
−1
H
B0

(6.87)

## PDF page 24

For de Sitter, the horizon is not the Hubble radius, but the parameter in our results is H and
one easily finds that Lp /H −1 ≫ 1 as well.
Consequently, photon-graviton oscillations always lie outside the Hubble radius and are in
principle unobservable. The same would be the case for the SU(2) boson-graviton oscillations
investigated in [3]. There, the mixing length was found to be essentially the same, with B0
replaced by qA2 , for coupling constant q and potential A, such that q 2 A4 ≪ 1. We do point
out that the lack of observability also holds for superadiabatic amplification of gravitational
and electromagnetic waves [11, 18], which also takes place at superhorizon scales.
One might suspect a possible “out” is to consider a scalar field φ instead of a magnetic
field b in a potential-dominated inflationary phase. In that case our isotropy constraint might
be evaded because the (isotropic) scalar potential V would replace B02 /a2 and also drive the
expansion such that H ∼ V 1/2 a (see 2.25). Then Lp could become as short as ∼ H −1 , which is
in fact what one expects for quantum mechanically excited modes in de Sitter [21]. In such a
scenario, the Gertsenshtein mechanism could have an observable effect on the particle make-up
of the universe.
Unfortunately, coupling gravitons to scalar modes in this scenario is nontrivial.

Re-

EM
placing Tµν
in the Einstein equations with the standard scalar-field stress-energy tensor

Tµν = φ,µ φ,ν −[V (φ) + 12 φ,α φ,α ]gµν and assuming potential dominance, yields for both the
h11 and h12 modes exactly (2.23) with a zero RHS. In other words, at first order there is no
coupling between h and φ.
In short, although a Gertsenshtein-like mechanism could in principle affect the particle balance in an inflationary period by catalyzing inter-species conversion, in practice it is ineffective
unless a stronger coupling among fields can be engineered. Whether that is best carried out
in an f (R) or other higher-order theory of gravity, or in an anisotropic cosmology, remains the
subject for future investigation.

Acknowledgements
The work by P.A. was performed under the auspices of the U.S. Department of Energy by
24

## PDF page 25

<math display="block">{\bf Lawrence\ Livermore\ National\ Laboratory\ under\ contract\ DE-AC52-07NA27344}.</math>
25

## PDF page 26

References
[1] Gertsenshtein, M. E.“Wave resonance of light and gravitational waves” Sov. Phys. JETP
14, 84-85 (1962).
[2] A. Palessandro and T. Rothman, “A simple derivation of the Gertsenshtein effect,” Phys.
Dark Univ. 40, 101187 (2023). doi:10.1016/j.dark.2023.101187 [arXiv:2301.02072 [gr-qc]].
[3] A. Palessandro and T. Rothman, “Autocatalysis of Graviton Production via the
Gertsenstein Effect in the Yang-Mills Field” Phys. Dark Univ. 42, 101341 (2023).
[arXiv:2301.12801 [gr-qc]].
[4] T. Rothman and S. Boughn, “Can gravitons be detected?” Foundations of Physics 36,
1801-1825 (2006).
[5] A. Palessandro and M. S. Sloth, “Gravitational Absorption Lines” Phys. Rev. D 101,
043504 (2020).
[6] F. J. Dyson, “Do gravitons exist?” Talk given at Boston University, November 8, 2005.
[7] F. J. Dyson, “Photon-Graviton Oscillations” (unpublished).
[8] C. W. Misner, K. S. Thorne and J. A. Wheeler, Gravitation (W. H. Freeman, New York,
1973).
[9] R. Wald, General Relativity (U. Chicago Press, 1984), Appendix D.
[10] P. Anninos, “Plane symmetric cosmology with relativistic hydrodynamics,” Phys. Rev. D
58, 064010 (1998).
[11] C. G. Tsagas, “Electromagnetic fields in curved spacetimes,” Class. Quant. Grav. 22,
393-408 (2005). doi:10.1088/0264-9381/22/2/011 [arXiv:gr-qc/0407080 [gr-qc]].
[12] B. Jancewicz, “Plane electromagnetic wave in spatially flat Friedman universe,” J. Math.
Phys. 60, 052505 (2019). doi:10.1063/1.5058731 [arXiv:1809.03346 [gr-qc]].
26

## PDF page 27

[13] L. Combi and G. Romero, “Electromagnetic fields and charges in expanding universes,”
Phys. Rev. D 99, 064017 (2019).
[14] J. Cote, V. Faraoni, A. Giusti, “Revisiting the conformal invariance of Maxwell’s equations
in curved spacetime,” Gen. Rel. and Gravitation 51, 117 (2019).
[15] I. Cotalescu, “Maxwell field in spatially flat FLRW space-times,” Eur. Phys. J. C 81, 908
(2021).
[16] D. Garrison, “Using Gravitational Waves to put limits on Primordial Magnetic Fields,”
arXiv:1608.01005v2.
[17] T. Rothman and P. Anninos, “A Phase Space Approach to the Gravitational Arrow of
Time,” Phys. Rev. D55, 1948-1963 (1997).
[18] L. Grishchuk, “Amplification of gravitational waves in an isotropic universe,” Zh. Eksp.
Teor. Fiz. 67, 825-838 (1974).
[19] V. Domcke and C. Garcy-Cely, “Potential of radio telescopes as high-frequency gravitational wave detectors,” Phys. Rev. Lett. 126, 021104 (2021).
[20] Ya. B. Zel’dovich,“Electromagnetic and gravitational waves in a stationary magnetic field,”
Zh. Eksp. Theor. Fiz. 68, 1311-1315 (1973).
[21] M. Turner and L. Windrow,“Inflation-produced, large-scale magnetic fields,” Phys. Rev.
D 37, 2743-2754 (1988).

27
