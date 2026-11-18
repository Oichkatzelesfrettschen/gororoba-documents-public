Source: https://arxiv.org/abs/2601.23279v1
PDF sha256: c647509b343b7348f8eff8b31a1a311f67e1e2bb442b53167ac89f902b8e0b90
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of ahmadiniaz_2026_photon_graviton_mixing.pdf

Transcription of `ahmadiniaz_2026_photon_graviton_mixing.pdf` in this directory, 29 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-29 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Prepared for submission to JHEP

arXiv:2601.23279v1 [hep-th] 30 Jan 2026

One loop photon-graviton mixing in an
electromagnetic field: Part 3

N. Ahmadiniaz,a F. Bastianelli,b F. Karbsteinc and C. Schubert d,1
a

Helmholtz-Zentrum Dresden-Rossendorf, Bautzner Landstraße 400, 01328 Dresden, Germany
Dipartimento di Fisica ed Astronomia, Università di Bologna, Via Irnerio 46, I-40126 Bologna,
Italy and INFN, Sezione di Bologna, Via Irnerio 46, I-40126 Bologna, Italy
c
Helmholtz-Institut Jena, Fröbelstieg 3, 07743 Jena, Germany and Theoretisch-Physikalisches Institut, Friedrich-Schiller-Universität Jena, Max-Wien-Platz 1, 07743 Jena, Germany
d
Facultad de Ciencias Físico-Matemáticas, Universidad Michoacana de San Nicolás de Hidalgo,
Avenida Francisco J. Mújica, 58060 Morelia, Michoacán, Mexico
b

E-mail: n.ahmadiniaz@hzdr.de, bastianelli@bo.infn.it,
felix.karbstein@uni-jena.de, christianschubert137@gmail.com
Abstract: Photon-graviton conversion in an electromagnetic field is a well-known prediction of Einstein-Maxwell theory. First discussed at tree-level by Gertsenshtein in 1962, more
recently it has been shown to lead to magnetic dichroism starting from one-loop. While
previously only two diagrams were assumed to contribute to this one-loop photon-graviton
amplitude in a constant electromagnetic field, here we point out the existence of a third
one involving a tadpole subdiagram. As shown by H. Gies and one of the authors in 2016
for the pure QED case, such diagrams cannot be omitted in general even though the tadpole formally vanishes. After a short review of the calculation of one-loop photon-graviton
amplitudes in the worldline formalism, we use this formalism for a unified calculation of all
three diagrams. Although phenomenologically this amplitude is mainly of interest for the
case of the spinor loop in a magnetic field, here we will also include the scalar loop and the
electric field component, since the computational effort is essentially the same. We show
that the tadpole diagram, although contributing to the amplitude, does not contribute to
the magnetic dichroism. The gravitational Ward identity provides a useful check.

1

Corresponding author

## PDF page 2

Contents
1 Introduction

1

2 One-loop amplitudes with one graviton and N photons
2.1 Irreducible contribution
2.2 Reducible contribution

5
5
6

3 Inclusion of a constant electromagnetic field
3.1 General procedure
3.2 The photon tadpole
3.3 The vacuum-polarization tensor in a constant field

7
7
8
9

4 Irreducible contribution to electromagnetic photon-graviton conversion

11

5 Tadpole contribution to electromagnetic photon-graviton conversion

13

6 Third contribution to electromagnetic photon-graviton conversion

15

7 Weak-field expansion of the tadpole contribution

16

8 Ward identities for the photon-graviton amplitude in a constant field

17

9 Conclusions

18

A Einstein-Maxwell theory

19

B Worldline Green’s functions and determinants in a constant field
B.1 Periodic case
B.2 Anti-periodic case

21
21
24

1

Introduction

Although processes in Einstein-Maxwell theory are presently not of direct experimental
relevance, they are of great theoretical interest, and much effort has gone into their study
both at the tree-level [1–6] and the one-loop level [7–11].
A particularly well-studied process is photon-graviton conversion in a magnetic field.
Einstein-Maxwell theory contains a tree-level vertex involving two photons and one graviton,
Fig. 1.

–1–

## PDF page 3

1)

4)

k

2)

k0

k0

0

k = k + k0
k0
k

p

p

=========

0

3) vertex photon-photon-graviton vertex.
Figure 1. Tree-level
k0

k

k0

k

k

+

k0

+

p
p
Replacing one of the photons by an
electromagnetic p0field Fpµν , one p0
can convert
this p0
vertex into the following amplitude for photon-graviton conversion in the field (or the inverse
30 )
process),

k
(tree)

Γ

k

k0

(k0 , ϵ0 ; k, ε; F ) = ϵ0µν εα Πµν,α
(tree) (k; F ),
p

k0

k0

k0

k

iκ µν,α
Πµν,α
,+
(tree) (k; F+) = − 2 C
p

0

p

p

0

k

k0

(1.1)
p

p0

where k0 , ϵ0 (k, ε) are the graviton (photon) momentum and polarisation, and the tensor
300 )
C µν,α is given by
p

(
)µ
(
)ν
(
)α
p0
C µν,α = F µα k ν + F να k µ − Fk · k δ να −k0 F · k δ µαk+
F · k δk µν .
0

(1.2)
k

k0

=========

This is well-known, but we give a derivation in appendix A for completeness.
+
+
amplitude is thep0conversion
of electromagnetic
waves
p
p
p0
6) An important application of this p
into gravitational waves (and vice-versa) in an external magnetic field, as pointed out by
Gertsenshtein as early as 1962 [12]. At the tree level, these processes and the associated
photon-graviton conversion have since been studied by many authors [13–20]. However, it
is only in 2005 that two of the present authors [21] calculated the one-loop correction to
k
the amplitude
(1.1) kdue to the diagram shown in Fig. 2 on the left, with either a scalar or
1
spinor loop.
7)

+
k

Γ(irr)

k

+
k

k

Γ(tadpole)

k

k

Γ(ext)

2

Figure 2. The three one-loop contributions to electromagnetic photon–graviton conversion. Here
“irr” and “ext” denote the irreducible and “extra” contributions, respectively.

Here we employ the usual double-line notation for the full propagator in the constant
external field (Fig. 3).
Using the then novel worldline representation of photon-graviton amplitudes [22–31]
they obtained compact parameter integral representations for this amplitude and for both

–2–

p0

## PDF page 4

1-loop

ΓHE [Ā] =

,

=

where

+

+

+

···

FIG. 1: Diagrammatic representation of the one-loop Heisenberg-Euler effective action. The
Figure 3. Full scalar or spinor propagator in a constant field.
ble line denotes the dressed
fermion propagator accounting for arbitrarily many couplings t
external field Ā, represented by the wiggly lines ending at crosses.

the scalar and spinor loop cases. Those representations are of the same type as the ones
that one finds for the better-known one-loop photon vacuum polarisation in a constant field,
2
l-loop
eformalism
1 [32, 33] or the Feynman diagram approach (see
either
in the worldline
with ΓHE computed
∼ ( απ )l−1
, where
α = 4π
≃ 137
is the fine-structure constant; we use the Heavi
[34–36] and refs. therein).
∫ l-loop
l-loop
Lorentz System
with
c
=
ℏ
=
1.
At
each
loop
order
l,
Γ
=
Lsmall accounts fo
Although numerically these one-loop corrections for realistic field
strengths are
HE
x HE
(suppressed by a factor of α) compared to the tree-level ones, in the subsequent study [37]
infinite number
of couplings to the external field, and thus is fully nonperturbative in
an important qualitative difference emerged: while the tree-level photon-graviton converparametersioneĀ.
For in the
completeness,
sketch
expansion
two-loop
order in the follow
amplitude
field gives we
(contrary
to thethe
superficially
similartocase of
photon-axion
conversion [14, 38–43]) equal conversion rates for both photon polarisations, at the one-loop
We beginlevel
bythis
noting
that the fermionic integral in Eq. (7) can be written as a funct
rate starts becoming polarisation-dependent. This leads to dichroism, and further
analysis by Ahlers et al. [44], who undertook an exhaustive search for other sources of
determinant,
(
)
magnetic dichroism showed that, although magnetic photon-graviton conversion is a very
/
iSψconditions,
[Ā + q] remarkably
= ln det it−i
D[Āthe+leading
q] + m
small effect under realistic
is still
such. effect in the
whole Standard Model. Their analysis of magnetic dichroism was also more complete in
taking
right-hand
of Fig.
2 into account,
contributes
to it at the same
If evaluated
atthe
q=
0, this diagram
quantity
amounts
to thewhich
one-loop
Heisenberg-Euler
effective ac
order in α.
in the external
field Ā, i.e., Γ1-loop
= Sψ [Ā];
for a graphical representation, cf. Fi
HE it[Ā]
Even so, from their numbers
is clear that
this effect will hardly be accessible to
experiment
in the near future,
a conclusion
is consistent
recent detailed
feasibility
Since Sψ is a
one-loop
expression,
the that
two-loop
orderwith
of the
Schwinger
functional is alr
and sensitivity studies of light-induced gravitational effects using interferometric techniques
obtained [45,
by 46].
performing
fluctuation
∼ involving
Dq to Gaußian
Nevertheless,the
this photonic
is of course presently
the case integral
for all process
gravitons, order. For
andSin the
long run we would still consider magnetic dichroism due to photon-graviton
we expand
ψ about the external field Ā,
conversion as a leading contender in the quest for an eventual experimental demonstration
of the existence of the graviton. ∫This is because (i) it involves
∫ ∫only a single gravitational
(
)
( and
1
µ of the graviton itself
(2) (iii))µν
coupling (ii) it does not require a direct (1)
Sψ [Ā + q] = Sψ [Ā] +
Smeasurement
[
Ā]
q
+
q
S
[Ā] dichroism
qν + O(q 3 ),
µ
µ
ψ
ψ
can be measured with high precision using optical cavities2[47–53].
The main purpose of the present paper is to point out the existence of yet another diacontributing to electromagnetic photon-graviton conversion at the same order, shown
where wegram
employed
the shorthand notation
in the middle of Fig. 2, or more precisely its non-vanishing. This requires some explanation.
Prior to 2017 it had generally been assumed, and even stated in QED∣ textbooks (see, e.g.,
∣
( (n)tadpole
)σ1 ...σn
δ n Sψ [A]
[34, 54]) that the one-photon
diagram in a constant
electromagnetic
field Fig. 4
∣
S
[
Ā]
:=
.
ψ
∣
vanishes, and therefore also any diagram containing
it. . . . δA
δA
σ1
σn A=Ā
The argument goes as follows:

The first-order
term corresponds to a one-loop photon current induced by the field Ā,
1. A constant field emits only photons with zero energy-momentum, thus there is a factor
( (2) )µ
of δ(k).
the Hessian is
related to the one-loop photon polarization tensor Πµν [Ā] := Sψ

evaluated in the external field Ā; for completeness note that this definition of the ph

polarization tensor differs from that of [57] by an overall minus sign. To Gaußian order
–3–

ignore the terms of O(q 3 ) in the exponent, resulting in
iW [Ā]

e

iSψ [Ā]

≃e

∫

i

Dq e

∫(

(1)

Sψ [Ā]

)µ

qµ − 2i

∫∫

(

qµ D −1 −Π[Ā]

)µν

qν

.

## PDF page 5

kµ

Figure 4. One-photon amplitude in a constant electromagnetic field.

2. Because of gauge invariance, this diagram in a momentum expansion starts with the
term linear in momentum.

+

+ ...

+

3. δ(k)k µ = 0.

Since the tadpole thus formally vanishes, it has been assumed for decades that also any
3: One-particle reducible
diagrams constituting the last term in Eq. (26). For the definition
diagram containing it can be discarded, for example, the “handcuff” contribution Fig. 5 to
e double line, cf. Fig. 1.
the two-loop Euler-Heisenberg Lagrangian [34, 35].
2-loop

ΓHE [Ā] =

+

Figure
5. “Handcuff” diagram
in aaction.
constantObviously,
field.
4: Diagrams
constituting
the two-loop
Heisenberg-Euler
effective
we have
2-loop ∣∣
2-loop ∣∣
= ΓHE 1PI +ΓHE 1PR . Note that the first diagram amounts to the leftmost one in Fig. 2,
However, in 2016 H. Gies and one of the authors [55] noted that such diagrams can
e it is drawn in a slightly different way; for the definition of the double line, cf. Fig. 1.

p

give finite values because of the infrared divergence of the connecting photon propagator.
In dimensional regularization, the key integral is
∫
µ kν
µν
Eq.
(2)
follows
Eq. one-loop
(4).
sponding to the straightforwardly
Dyson series of from
the full
resummed
propagator. In the
k
ηphoton
dD k δ D (k) 2 =
.
(1.3)
the recent
analysis performed
in Ref.
[1], this k
contribution
was believed
to vanish
term ofPrior
Eq.to(26),
this resummed
propagator
interconnects
twoDone-loop
photon
currents
)
d (d) one αfinds a non-vanishing result, which
Applying
integral
handcuff
diagram
(1) in constant
fields
[7, 9], this
based on
theto the
argument
that (2π)
δ (k) k = 0 in Eq. (5), thereby
[
Ā]
.
All
the
diagrams
arising
when
adopting
the
expansion
(29) in the last term in
ψ
can be that,
expressed
the following
way in divergent
terms of the
one-loop
Euler-Heisenberg
missing the subtlety
upon in
convolution
withsimple
the infrared
photon
propagator,
26) are one-particle
reducible;
Lagrangian
[56, 57]see
(seeFig.
also3.
[58])
the current (5) might induce finite 1PR tadpole contributions in Feynman diagrams. Finally,
(EH)
(EH) of a 1PI and a 1PR
turn,
the two-loop
Heisenberg-Euler effective
action
∂Lspinconsists
∂L
1
note that L2-loop
may alternatively be viewed as
one-loop
calculation
performed with the
spin
1PRa
HE
Lspin =
,
µν
ramcharged
and is particle
given by
2 ∂F
∂Fµνfor quantum corrections
propagator in the constant field already
accounting
(the The
superscript
stands
for
reducible”).
∫ “one-particle
at one-loop level.
latter is‘1PR’
depicted
in ∫
Fig.
2. Identifying
the in- and outgoing charged

1
1
Γ2-loop
HE [Ā] = Tr(DΠ[Ā]) +
⏞⏞ ∣ ⏟ ⏟2
⏟2
∣
=:Γ2-loop
HE
1PI

( (1) ) µν ( (1) )
Sψ [Ā] µ D Sψ [Ā] ν .
⏞⏞ ∣
⏟
2-loop ∣
=:ΓHE

(30)

1PR

+

he FIG.
existence
as
a matter
of to
principle
of the
1PR term
in Eq.
(30)
has been
known for a
2:
One-loop
corrections
the charged
particle
propagator
in an
external
electromagnetic
Figure 6. Full scalar or spinor propagator in a constant field.

field.It has, however, been argued that this term vanishes for constant external fields
time.

Similarly, [59, 60] found that the one-loop tadpole contribution to the scalar or spinor
4]. Let
us reproduce
this
argument
for reasons
ofshown
completeness:
a crucial building block
particle lines (in
Fig.
2 )to in
form
loops, the
diagrams
in Fig. 1 are recovered.
propagator
a constant
field
(Fig.6) is
also non-vanishing,
and given by
(1)
e 1PR term is Sψ [Ā] ν , which corresponds to the one-loop(EH)
photon current which will
1PR

∂S(p) ∂L

µ
S
(p)
= jµ
, not depend on any
alled jB.
[Ā] below.
For a constant external
field,
[∂F
Ā]µνdoes
∂F
1-loopCharged
1-loop
µν
particle propagators in constant
electromagnetic
fields

µ
etime point x either. On the other hand, j1-loop
[Ā] is a Lorentz 4-vector. The vector

Meanwhile,
Refs.only
[5, 6]behave
explicitlyfrom
determined
the one-loop
corrections
for
x of the
current can
generated
the building
blockstadpole
F̄ , ∂ and
x. However,

the propagators
of =
both
charged
scalar
and spinor particles
in constant fields within the
onstant
fields ∂ µ F νκ
0 and
for an
x independent
current,
– 4 – all conceivable combinations
worldline formalism. The respective Feynman diagram is depicted in Fig. 2 (right). Their

one vector index vanish and so does the current (an explicit verification of this fact in
finding is that in momentum space this 1PR contribution to the charged particle propagator

entum space is given below).

can be expressed similarly to Eq. (2) as

While this part of the argument holds true in the full analysis, it does not necessarily

## PDF page 6

where S(p) denotes the tree-level propagator in the field, see also [61].
Below we perform the similar, albeit more complicated, calculation of the middle diagram of Fig. 2. Moreover, we provide a unified calculation of all three diagrams using the
worldline formalism, and show that, although the tadpole diagram contributes to the amplitude, it leaves the magnetic dichroism unchanged. Although our main interest is in the
magnetic field and spinor loop case, we will perform all calculations in a general constant
field and for both the scalar and spinor loop, since in the worldline formalism this essentially does not imply any extra computational effort. All formulas required to specialize the
field to a purely magnetic one (as well as a purely electric or crossed-field one) are given in
appendix B.
The organization of the paper is as follows. In section 2 we review the worldline
representation of the one-loop photon-graviton amplitudes with a scalar or spinor loop in
vacuum, including a short discussion of the gauge and gravitational Ward identities. In
section 3 we show how to incorporate an external constant electromagnetic field. Section 4
summarizes the worldline calculation of [21, 37] of the “main” or “irreducible” contributions
Γ(irr) to these amplitudes, while section 6 analyzes the contribution Γ(ext) . The central
section is 5 where we derive the new “tadpole” contributions Γ(tadpole) . In section 7 we
study the weak-field expansion of the tadpole contribution in a magnetic field. In section
8 we verify the gravitational Ward identities for these amplitudes, which also provides a
non-trivial check. Section 9 offers our conclusions. Appendix A establishes our conventions
for Einstein-Maxwell theory, while in appendix B we collect some useful formulas involving
the worldline Green’s functions and determinants in a constant field.
Partial results of this work were presented in [62].

2

One-loop amplitudes with one graviton and N photons

We shortly summarize the worldline approach to the calculation of the one-loop amplitudes
involving a scalar or spinor in the loop and one graviton and N photons, first in vacuum
[28–31, 63, 64]. These amplitudes have an irreducible contribution, where all the external
legs are directly attached to the loop, and a reducible one, where the graviton is attached
to one of the photons.
2.1

Irreducible contribution

The irreducible spinor/scalar loop contribution to the one-graviton N -photon amplitude is
given by [65]
(

)
( κ )∫ ∞ dT
D
−2
2
N
Γ( spin ) (k0 , ϵ0 ; . . . ; kN , εN ) =
(−ie) −
e−m T (4πT )− 2
N,1
1
4 0 T
scal
⟨
⟩
× V(Gspin ) [k0 , ϵ0 ] V(γspin ) [k1 , ε1 ] · · · V(γspin ) [kN , εN ] .
(irr)

scal

scal

(2.1)

scal

Here e and κ are the electromagnetic and gravitational couplings, m the mass and T the
proper-time of the loop scalar or spinor. k0 and ϵ0 denote the graviton momentum and

–5–

## PDF page 7

polarization tensor, the remaining ki ’s and εi ’s the photon ones. V G and V γ denote the
graviton and photon vertex operators,
γ
Vscal
[k, ε] =
γ
Vspin
[k, ε] =

∫ T
0

∫ T
0

dτ ε · ẋ(τ ) eik·x(τ ) ,

(2.2)

[
]
dτ ε · ẋ(τ ) − iψ(τ ) · f · ψ(τ ) eik·x(τ ) ,

(2.3)

∫ T [
]
dτ ẋµ (τ )ẋν (τ ) + aµ (τ )aν (τ ) + bµ (τ )cν (τ ) eik0 ·x(τ ) ,
0
∫ T [
G
dτ ẋµ (τ )ẋν (τ ) + aµ (τ )aν (τ ) + bµ (τ )cν (τ )
Vspin
[k0 , ϵ0 ] = ϵ0µν
0
]
+ψ µ (τ )ψ̇ ν (τ ) + αµ (τ )αν (τ ) + iẋµ (τ )ψ ν (τ )ψ(τ ) · k eik0 ·x(τ ) ,
G
Vscal
[k0 , ϵ0 ] = ϵ0µν

(2.4)

(2.5)

and fµν = kµ εν − kν εµ the linearized photon field-strength tensor. The Wick contractions
⟨· · · ⟩ are to be performed using the set of worldline correlators
⟨xµ (τ )xν (τ ′ )⟩ = −GB (τ, τ ′ ) ,
1
⟨ψ µ (τ )ψ ν (τ ′ )⟩ = GF (τ, τ ′ ) ,
2
⟨aµ (τ )aν (τ ′ )⟩ = 2δ(τ − τ ′ )δ µν ,
µ

ν

′

µ

ν

′

′

⟨b (τ )c (τ )⟩ = −4δ(τ − τ )δ
′

⟨α (τ )α (τ )⟩ = 2δ(τ − τ )δ

µν

µν

(2.6)
(2.7)
(2.8)
,

,

(2.9)
(2.10)

with the worldline Green’s functions
(τ − τ ′ )2
,
T
GF (τ, τ ′ ) = sgn(τ − τ ′ ) .

GB (τ, τ ′ ) = | τ − τ ′ | −

2.2

(2.11)
(2.12)

Reducible contribution

The reducible contribution to the N -photon/one graviton amplitude, where the graviton is
attached to one of the photons, usually would be constructed by sewing together the N photon amplitude and the photon-photon-graviton vertex of Fig. 1. For the analogous case
(red)pp′
of the scalar tree-level propagator dressed with N photons and one graviton, DN,1
, it was
shown in [64] that the effect of this sewing can be expressed by the following replacement
rule
(red)pp′
DN,1
(k0 , ϵ0 ; . . . ; kN , εN ) =

N
∑

′

pp
DN,0
(k1 , ε1 ; . . . ; ki + k0 , υi ; . . . ; kN , εN ) ,

i=1

with an effective photon polarization vector
υi ≡ −κ

{ϵ0 , fi } · (ki + k0 )
ϵ0 · fi · k0 + fi · ϵ0 · ki
= −κ
.
(ki + k0 )2
2k0 · ki

–6–

(2.13)

## PDF page 8

Here we observe that the same replacement rule applies as well for the one-loop N -photon/one
graviton amplitudes with either a scalar or a spinor loop. For the scalar loop this is obvious
from the fact that our derivation of that rule in [64] did not make use at all of the boundary
conditions imposed on the scalar path integral. But neither did we use the specific form
of the scalar vertex operator, and the reader can easily convince herself that changing the
scalar vertex operator into a spinor one will not make a difference here. Thus, without
further ado, we can write down the reducible part of the spinor/scalar loop contribution to
the one-graviton N -photon amplitude as
(red)

Γ( spin )
scal

N,1

(k0 , ϵ0 ; . . . ; kN , εN ) =

i=1

where υiµ is the same as in (2.13).

3
3.1

N
∑

Γ( spin )
scal

N,0

(k1 , ε1 ; . . . ; ki + k0 , υi ; . . . ; kN , εN ) , (2.14)

Inclusion of a constant electromagnetic field
General procedure

The generalisation of the formalism to the case of the photon-graviton amplitudes in a
constant electromagnetic field is straightforward and proceeds essentially as in the purely
electromagnetic case [24, 26, 27, 33, 68–70]: the master formulas (2.1) acquire an additional
determinant factor
]
[
1
Z
(Spinor loop) ,
(3.1)
det 2
tanZ
[
]
1
Z
det 2
(Scalar loop) ,
(3.2)
sinZ

(Zµν ≡ eFµν T ), and the worldline Green’s functions GB , GF have to be replaced by their
constant-field versions GB , GF ,
( −iĠB (τ,τ ′ )Z
)
T
e
− cos Z
′
′
GB (τ, τ ) =
+ iĠB (τ, τ ) ,
2Z
sin Z
′

e−iZ ĠB (τ,τ )
.
(3.3)
cosZ
Since these Green’s functions have a non-trivial Lorentz structure, the Wick-contraction
rules (2.6), (2.7) generalise in the form
GF (τ, τ ′ ) = GF (τ, τ ′ )

µν
⟨xµ (τ )xν (τ ′ )⟩F = −GB
(τ, τ ′ ) ,
(3.4)
1
⟨ψ µ (τ )ψ ν (τ ′ )⟩F = GFµν (τ, τ ′ ) ,
(3.5)
2
with the Wick-contraction rules for the ghosts unchanged.
Thus the vacuum master formula (2.1) directly generalises to the constant-field background as
( )
[(
)]
( κ )∫ ∞ dT
D
1
−2
Z/tanZ
2
(irr)
Γ( spin ) (k0 , ϵ0 ; . . . ; kN , εN ; F ) =
(−ie)N −
e−m T (4πT )− 2 det 2
N,1
1
4 0 T
Z/sinZ
scal
⟨
⟩
× V(Gspin ) [k0 , ϵ0 ] V(γspin ) [k1 , ε1 ] · · · V(γspin ) [kN , εN ]
.
(3.6)
scal

scal

scal

–7–

F

## PDF page 9

The rule (2.14) for the construction of the reducible contributions, where the graviton
gets attached to one of the photons, is also not affected by the presence of the external
field.
At the one-graviton level, the only really new aspect arising from the presence of the
external field is that there is now a second type of reducible contributions, since the graviton
can now be attached also to one of the photons emitted by the external field, see Fig. 7.

Figure 7. Field-induced type of reducible contributions.

(ext)

It is easy to see that the contribution of this diagram, to be called ΓN,1 , can be
obtained from the purely photonic amplitude with N +1 photons in the field by the following
modification of (2.14),
(ext)
Γ( spin )
scal

N,1

where now

(k0 , ϵ0 ; . . . ; kN , εN ; F ) = Γ( spin )
scal

υF ≡ iκ
3.2

N +1,0

(k0 , υF ; k1 , ε1 ; . . . ; . . . ; kN , εN ; F ) ,

{ϵ0 , F } · k0
.
k02

(3.7)

(3.8)

The photon tadpole

For starters, let us work out (3.6) for the pure QED case with one and two photons. For
the tadpole (Fig. 4) with a scalar loop, this yields
]
[
1
dT
Z
−D
−m2 T
2
2
(4πT ) e
Γscal (k, ε; F ) = −e(2π) δ (k)
det
T
sin Z
0
∫ T
[1
]
×
dτ ε · ĠB (τ, τ ) · k exp k · GB (τ, τ ) · k .
2
0
D D

∫ ∞

(3.9)

Using the coincidence limits (B.6), (B.7) this can be written more explicitly as
]
Z
Γscal (k, ε; F ) = −ie(2π) δ (k)
dT (4πT ) e
det
sin Z
0
[
]
(
( cotZ
1)
T
1 )
×ε · cotZ −
· k exp k ·
− 2 ·k .
Z
4
Z
Z
D D

∫ ∞

2
−D
2 −m T

1
2

[

(3.10)

To get the corresponding quantity for spinor QED, we have to include the spin part of
the photon vertex operator, change the determinant factor, and to supply the usual global

–8–

## PDF page 10

factor of −2. This yields

∫ ∞

[

Z
dT (4πT ) e
Γspin (k, ε; F ) = 2ie(2π) δ (k)
det
tan Z
0
[
]
(
)
(
)
1
T
cotZ
1
×ε · cotZ + tanZ −
· k exp k ·
− 2 ·k .
Z
4
Z
Z
D D

−D
−m2 T
2

1
2

]
(3.11)

Note that, as mentioned in the introduction, the expressions (3.10), (3.11) formally vanish
on account of the factor δ D (k) k µ .
3.3

The vacuum-polarization tensor in a constant field

For N = 2 in the scalar case we find the integrand
[
] 1
⟨
⟩
γ
γ
= ε1 · G̈B12 · ε2 − ε1 · ĠB1i · ki ε2 · ĠB2j · kj e 2 ki ·GBij ·kj ,
Vscal
[k1 , ε1 ]Vscal
[k2 , ε2 ]
F

(3.12)

where summation over i, j = 1, 2 is understood. We use momentum conservation to write
k = k1 = −k2 . Removing the second derivative in the first term by an IBP in τ1 , the
integrand becomes
) ]
)
(
[
(
ε1 · ĠB12 · ε2 k · ĠB12 · k + ε1 · ĠB12 − ĠB · k ε2 · ĠB21 − ĠB · k e−k·(GB12 −GB )·k , (3.13)

where we have introduced the further notation of indicating the constant coincidence limit
of a Green’s function by the omission of its argument, ĠB ≡ ĠBii etc. The content of the
µν
ε2ν ,
brackets then turns into ε1µ Iscal
)νκ
)µλ (
(
µν
µν
ĠB21 − ĠB
kκ kλ .
Iscal
= ĠB12
k · ĠB12 · k + ĠB12 − ĠB

(3.14)

GB12 = SB12 + AB12 ,

(3.15)

Next we would like to use the fact that the integrand contains terms which integrate to zero
due to antisymmetry under the exchange τ1 ↔ τ2 . Thus we decompose the constant-field
worldline Green’s function as

where SBij denotes the even (SBii ≡ SB ) and ABij the odd part (ABii ≡ AB ) as a power
series in F . Only the Lorentz even part of GBij contributes in the exponent,
(
)
k · (GB12 − GB ) · k = k · SB12 − SB · k ≡ T k · Φ12 · k .

(3.16)

µν
Iscal
turns, after decomposing all factors of ĠBij as above, and deleting all τ - odd terms,
into
{
(
)µλ (
)νκ }
µν
µν
µλ
κλ
νκ
˜
Iscal ≡ ṠB12 ṠB12 − ṠB12 ṠB12 + ȦB12 − ȦB
ȦB12 − ȦB
kκ kλ .

(3.17)

–9–

## PDF page 11

In this way we obtain the following integral representations for the dimensionally regularized
constant-field vacuum polarization tensor in scalar QED:
[
]∫ 1
∫ ∞
1
Z
e2
dT 2− D −m2 T
µν
2 e
2
e−T k·Φ12 ·k .
(k;
F
)
=
−
det
du1 I˜scal
Πµν
T
D
scal
T
sin
Z
0
(4π) 2 0
(3.18)
As usual we have rescaled to the unit circle and set u2 = 0.
For spinor QED, the formula corresponding to (3.14) is [33]
µν
µν
Ispin
= ĠB12
k · ĠB12 · k − GFµν12 k · GF 12 · k
[(
]
)µλ (
)νκ
µλ
νκ
− ĠB − GF − ĠB12
ĠB21 − ĠB + GF
+ GF 12 GF 21 k κ k λ

(3.19)

and (3.17) generalizes to
{(
) (
)
µν
µν
µλ
µν
µλ
κλ
νκ
κλ
νκ
˜
Ispin ≡
ṠB12 ṠB12 − ṠB12 ṠB12 − SF 12 SF 12 − SF 12 SF 12
(
)µλ (
)νκ
+ ȦB12 − ȦB + AF
ȦB12 − ȦB + AF
}
µλ
νκ
−AF 12 AF 12 k κ k λ .

(3.20)

Taking the global factor of −2 and the change of the field-dependent determinant factor
(3.2) into account, (3.18) generalizes to
[
]∫ 1
∫ ∞
1
dT 2− D −m2 T
e2
Z
µν
µν
Πspin (k; F ) = 2
T 2e
det 2
du1 I˜spin
e−T k·Φ12 ·k .
D
T
tan
Z
2
0
0
(4π)
(3.21)
As is well-known, the constant field vacuum polarization tensors contain the UV divergences of the ordinary vacuum polarization tensors, but no further ones, so that on-shell
renormalization can be performed by subtraction of the integrand at zero field strength
and momentum. In this way we find for the renormalized vacuum polarization tensors
(indicating the renormalisation by a ‘bar’) [33]
{
[
]
∫ ∞
∫
1
dT −m2 T 1
Z
e2
µν
Π̄scal (k; F ) = −
e
du1 det 2
I˜µν e−T k·Φ12 ·k
16π 2 0 T
sin Z scal
0
}
(
)
− δ µν k 2 − k µ k ν (1 − 2u1 )2 ,
(3.22)
{
[
]
∫
∫
1
Z
e2 ∞ dT −m2 T 1
µν
µν
e
I˜spin
e−T k·Φ12 ·k
Π̄spin (k; F ) =
du1 det 2
8π 2 0 T
tan
Z
0
}
( µν 2
)
µ ν
+4 δ k − k k u1 (1 − u1 ) .
(3.23)

The remaining u1 - integral can be brought into a more standard form by a transformation
of variables v = ĠB12 = 1 − 2u1 .
The matrix decomposition formulas of appendix B can be used to write these integral
representations more explicitly (for the generic case of parallel electric and magnetic fields
this has been done in [33]).

– 10 –

## PDF page 12

4

Irreducible contribution to electromagnetic photon-graviton conversion

We now turn to applying this formalism to the electromagnetic photon-graviton conversion
(irr)
amplitude, starting with the irreducible contribution Γspin . Using the machinery developed
above, its worldline representation can be written as
[
]
∫
1 tan(Z)
κ ∞ dT −m2 T
(irr)
−D
−
Γspin (k0 , ϵ0 ; k, ε; F ) = −2(−ie)(− )
e
(4πT ) 2 det 2
4 0 T
Z
⟨
⟩
γ
G
(4.1)
× Vspin
[k0 , ϵ0 ]Vspin [k, ε] .
F

Performing the Wick contractions according to the rules for the constant-field case, eqs.
(3.4) and (3.5), stripping off ϵ0 , ε as in (1.1), and eliminating k0 through k0 = −k, the
result can be written as
∫ ∞
[
]
eκ
dT −m2 T − D
− 1 tanZ
2 det 2
Πµν,α
(k;
F
)
=
−
e
T
D
spin
Z
2(4π) 2 0 T
∫ T
∫ T
( µν,α
(µν),α )
×
dτ1
dτ2 e−k·ḠB12 ·k Jscal
+ Jψ
,
(4.2)
0

0

µν,α
we have collected all terms that come from the purely orbital part of the
where in Jscal
( (µν),α
(µν),α
(νµ),α )
vertex operators, and Jψ
≡ 12 Jψ
+ Jψ
contains all the terms involving the
spin of the loop fermion. Here ḠB12 ≡ GB12 − GB is the modified Green’s function obtained
by subtracting its coincidence limit. Using the symmetry properties (B.5) and (B.37), the
result can be written as
)(
)α [
(
)ν (
)]
(
µν,α
µν
µα
Jscal
= G̈B11
− 2δ11 δ µν k · Ġ B12 + G̈B12
Ġ B12 · k + µ ↔ ν
(
)µ (
)ν (
)α
− Ġ B12 · k
Ġ B12 · k
k · Ġ B12 ,
(4.3)

(
)ν (
)µ ](
)α
[
Ġ B12 · k
GF 22 · k
Jψµν,α = ĠFµν11 − 2δ11 δ µν + GF 11 · k
(
)ν
(
)µ
− GF 12 · k ĠFνα12 + GFµα12 ĠF 12 · k
[
(
) (
)ν (
)α ](
)µ
+ −GFνα12 k · G F 12 · k + GF 12 · k
k · G F 12
Ġ B12 · k
(
)(
)α
− ĠFµν11 − 2δ11 δ µν k · Ġ B12
[
(
)µ (
)ν ](
)α
µν
− G̈B11
− 2δ11 δ µν − Ġ B12 · k
Ġ B12 · k
GF 22 · k
[
(
)ν
)µ (
)α ](
µα
+ G̈B12
− Ġ B12 · k
k · Ġ B12
GF 11 · k .

(4.4)

µν,α −k·G B12 ·k
It will be useful to add to Jscal
e
the total derivative term

−

)ν
(
)]
1 ∂ [ µα (
Ġ B12 Ġ B12 · k e−k·G B12 ·k + µ ↔ ν .
2 ∂τ1

– 11 –

(4.5)

## PDF page 13

(µν),α

µν,α
We can then replace Jscal
+ Jψ

by
(µν),α

(µν),α

µν,α
µν,α
Jspin
= Jspin,1
+ Jspin,2 + Jspin,3

(4.6)

where
(
)[(
) ]α
µν,α
µν
Jspin,1
= − G̈B11
− ĠFµν11
Ġ B21 + GF 22 · k ,
[(
(
)ν
)ν
µα (
) ]µ
µν,α
να
Jspin,2
= −Ġ B12 G̈B12 · k + GFµα12 ĠF 12 · k + G̈B12
Ġ B12 + GF 11 · k
(
)µ
−ĠFνα12 GF 12 · k ,
(
)µ {[(
) ]ν [(
) ]α
µν,α
Jspin,3
= Ġ B12 · k
Ġ B12 + GF 11 · k
Ġ B21 + GF 22 · k
(
)ν (
)α
}
να
− GF 12 k
GF 21 k + Ġ B12 k · ĠB12 · k − GFνα12 k · GF 12 · k .

(4.7)

Before proceeding further, let us use this integral representation to analyse the general
structure of this amplitude. Although our calculation is nonperturbative in the external
field, we can use the series expansions of GB , ĠB , G̈B and GF , ĠF in the field, whose first few
terms are given in (B.9) - (B.11) and (B.40), (B.41), to compute the amplitude involving a
given number of interactions with the field. It is then immediately seen that this amplitude
is nonzero only if this number of interactions is odd, since otherwise the τ1,2 integrations
vanish by antisymmetry.
The leading term in this expansion in the background field is UV divergent. In dimensional regularisation, this divergence is [21]
Πµν,α
spin,div (k; F ) = −

4 ie2 κ
1
C µν,α (k) ,
3 (4π)2 D − 4

(4.8)

where C µν,α is the same tensor that appeared in the tree-level amplitude, eq. (1.2). This
was to be expected since the amplitude must be multiplicatively renormalizable (although
quantum gravity is not a renormalizable theory, amplitudes in Einstein-Maxwell theory
involving gravitational fields and gravitons only externally are still renormalizable by power
counting). Renormalization is performed by subtracting the amplitude at zero field strength
and zero momentum, leading to the following form of the renormalized amplitude Π̄:
∫ ∞
eκ
dT −m2 T
e
2
32π 0 T 3
{
}
]∫ T ∫ T
[
4 2 µν,α
−k·G B12 ·k µν,α
− 12 tan(Z)
dτ1 dτ2 e
× det
Jspin + iT eC
.
Z
3
0
0

Π̄µν,α
spin (k; F ) = −

(4.9)

Once more this can still be simplified using the decompositions GB,F = SB,F + AB,F where
µν
µν
SB,F
contains the even powers of F µν in the power series representation of GB,F
, and Aµν
B,F
the odd ones. After this replacement all terms in the integrand are either symmetric or
antisymmetric under the exchange τ1 ↔ τ2 , and the antisymmetric ones can be deleted
since their τ1,2 - integrals vanish. Further, as usual, we rescale τi = T ui , i = 1, 2, and set

– 12 –

## PDF page 14

u2 = 0. This leads to
Π̄µν,α
spin (k; F ) = −

eκ
32π 2

{
[
]∫ 1
1 tan(Z)
dT −m2 T
du1
e
det− 2
T
Z
0
0
}
3
∑
4
(µν),α
× e−k·S B12 ·k
J˜spin,m + ieC µν,α ,
3

∫ ∞

(4.10)

m=1

where
( (
(
) )α
µν
µν,α
− ṠFµν11 ) k · ȦB12 + AF 22
J˜spin,1
= S̈B11
,
(
)µ
(
)µ
(
)ν
(
)ν
µα
µν,α
µα
να
να
˜
Jspin,2 = −ṠB12 ÄB12 · k + SF 12 ȦF 12 · k + ÄB12 ṠB12 · k − ȦF 12 SF 12 · k
(
)ν
)ν
µα (
− ȦB12 S̈B12 · k + Aµα
Ṡ
·
k
F 12
F 12
((
)µ
(
)µ
)
να
+S̈B12
ȦB12 + AF 11 · k − ṠFνα12 AF 12 · k ,
(
)µ [(
)ν ( (
)ν (
)α
)) α (
µν,α
J˜spin,3
= − ṠB12 · k
ṠB12 · k
k · ȦB12 + AF 11
− SF 12 · k
k · AF 12
((
)α (
)ν (
)α
) )ν (
+ ȦB12 + AF 11 · k
k · ṠB12 − AF 12 · k
k · SF 12
]
να
k
·
S
·
k
− ȦB12 k · ṠB12 · k + Aνα
F 12
F 12
(
)µ [(
)ν (
)α (
)ν (
)α
− ȦB12 · k
ṠB12 · k
k · ṠB12 − SF 12 · k
k · SF 12
)ν (
)α
((
) )ν ( (
) )α (
− AF 12 · k
k · AF 12
+ ȦB12 + AF 11 · k
k · ȦB12 + AF 11
]
να
− ṠB12
k · ṠB12 · k + SFνα12 k · SF 12 · k .
(4.11)

It is then straightforward to write the integrands more explicitly using the decomposition
formulas of appendix B.
The corresponding result for the scalar loop is obtained[by omitting
all terms
]
[ involving
]
− 21 tan(Z)
− 12 sin(Z)
the fermionic worldline Green’s function, changing det
to
det
, and
Z
Z
multiplying by a global factor of − 12 .

5

Tadpole contribution to electromagnetic photon-graviton conversion

The tadpole contribution (middle diagram in Fig. 2) can be constructed using our result
(3.11) for the one-photon amplitude in the field, replacing k by k ′ , ε by the υ of (2.13), and
integrating over k ′ . This gives
[
]∫
∫ ∞
1
Z
δ D (k ′ )
(tadpole)
−m2 T
−D
2
2
det
dD k ′ ′2
Γspin
(k0 , ϵ0 ; k, ε; F ) = 2ieκ
dT (4πT ) e
tan Z
k
0
[
]
(
(
)
)
1
T
cotZ
1
×k ′ · cotZ + tanZ −
· {ϵ0 , f } · k ′ exp k ′ ·
− 2 · k′
(5.1)
Z
4
Z
Z
(we have also used the antisymmetry of the Lorentz matrix cotZ + tanZ − Z1 ). In the
presence of the delta function, the factor exp[k ′ · · · k ′ ] can be replaced by unity since the

– 13 –

## PDF page 15

prefactor already contains two powers of k ′ . Applying the integral formula (1.3) leads to
∫ ∞
D
4
2
(tadpole)
dT (4πT )− 2 e−m T
Γspin
(k0 = −k, ϵ0 ; k, ε; F ) = ieκ
D
0
[
] [(
]
1
Z
1)
tr cotZ + tanZ −
×det 2
· ϵ0 · f .
(5.2)
tan Z
Z

This contribution, too, for D = 4, contains a UV divergence, stemming from the terms
linear in the field. Thus to calculate it we can replace the determinant factor with unity,
and under the trace make the replacement
cotZ + tanZ −

1
2
≈ Z.
Z
3

(5.3)

Extracting the pole in dimensional regularization we get
(tadpole)

Γspin,div (k0 = −k, ϵ0 ; k, ε; F ) = −

1
4 ie2 κ
tr (F ϵ0 f ) .
2
3 (4π) D − 4

(5.4)

As usual, we remove it by a subtraction at the integrand level, and the renormalized tadpole
contribution becomes
∫ ∞
dT −m2 T
ieκ
(tadpole)
Γ̄spin
(k0 = −k, ϵ0 ; k, ε; F ) =
e
2
16π 0 T 2
{
[
] [(
]
}
1
Z
1)
2
× det 2
tr cotZ + tanZ −
· ϵ0 · f − tr (Zϵ0 f ) .
(5.5)
tan Z
Z
3

Specializing to a constant magnetic background pointing along the z-axis (see Appendix B),
we rewrite the renormalized expression in D dimensions in order to perform the proper-time
integral within dimensional regularization. Now the renormalized tadpole contribution is
given by
D
ieκ
(tadpole)
Γ̄spin
(k0 = −k, ϵ0 ; k, ε; B) = −
(2π)− 2 tr(r+ ϵ0 f )

∫ ∞

D
0
{
}
z
2
×
+ coth z − z coth z
3

D

2

dT T − 2 e−m T

(5.6)

with z = eBT and Z = zr+ . The z-integral can be carried out in closed form, leading to an
expression of the renormalized tadpole contribution in terms of the Hurwitz zeta function
ζ(s, a),
D)
ieκ ( π )− D2 (
tr(r+ ϵ0 f )
Γ 1−
DeB eB
2
[
( m2 ) D −1 D (
D
D
m2 )
2
× − 2− 2
− ζ 1 − ,1 +
eB
2
2
2eB

(tadpole)
Γ̄spin
(k0 = −k, ϵ0 ; k, ε; B) =

]
D
(D
) m2 (
D
m2 ) 21− 2 (
D )( m2 ) D2 −2
+
−1
ζ 2 − ,1 +
+
1−
.
2
2eB
2
2eB
3
2
eB

(5.7)

– 14 –

## PDF page 16

However, note that, unlike the renormalization which we performed on the irreducible
(irr)
contribution Γspin , this one is nothing new; the contribution of the tadpole linear in the field
corresponds to the diagram shown in Fig. 8, which makes it clear that this subtraction is just
TADPOLEN
a special case (the zero-momentum limit) of the QED photon wave function renormalization,

k

k

Figure 8. Tadpole diagram expanded to linear order in the field.

Note that, differently from the irreducible contribution, for the tadpole contribution
the renormalization completely removes the part linear in the field, leaving only terms of
cubic or higher order in the field.
Let us also give the corresponding result for the scalar loop:
ieκ
(tadpole)
Γ̄scal
(k0 = −k, ϵ0 ; k, ε; F ) = −
32π 2

∫ ∞

dT −m2 T
e
T2
0
{
[
] [(
]
}
1
Z
1)
1
× det 2
tr cotZ −
· ϵ0 · f + tr (Zϵ0 f ) .
sin Z
Z
3

(5.8)

Analogously to the spinor loop, one obtains the following representation for the scalar case:
(tadpole)

Γ̄scal

6

2ieκ ( 2π )− D2 (
D)
Γ 1−
tr(r+ ϵ0 f )
(k0 = −k, ϵ0 ; k, ε; F ) = −
DeB eB
2
[
D (
D 1
m2 ) (
D ) m2 (
D 1
m2 )
ζ 1− , +
+ 1−
ζ 2− , +
×
2
2 2 2eB
2 2eB
2 2 2eB
]
D
2− 2 (
D )( m2 ) D2 −2
+
1−
.
(5.9)
3
2
eB

Third contribution to electromagnetic photon-graviton conversion

For the other reducible contribution, corresponding to the third diagram in Fig. 2, we
can use eqs. (3.7), (3.8), with k ′ = k0 = −k, and our results for the vacuum polarization
tensor in a constant field from subsection 3.3. Like the tadpole contribution, it has a UV
divergence from the field-independent part of the vacuum polarization tensor. This part
corresponds to the right-hand diagram of Fig. 2, but with the loop fermion taken in vacuum,
and according to the LSZ formalism is not to be taken into account in the calculation of the

– 15 –

## PDF page 17

on-shell amplitude. Using our result (3.23) for the on-shell renormalized one-loop vacuum
polarization tensor in the constant field, and putting things together, we have
(
)
(ext)
βα
βα
Γ̄spin (k0 = −k, ϵ0 ; k, ε; F ) = vF β Π̄spin (k; F ) − Π̄spin (k; 0) εα ,
(6.1)
with

υF = iκ

Π̄βα
spin (k; F ) =

e2
8π 2

∫ ∞
0

{ϵ0 , F } · k
{ϵ0 , F } · k0
,
= −iκ
2
k2
k0

dT −m2 T
e
T

{

]
Z
βα
du1 det
I˜spin
e−T k·Φ12 ·k
tan Z
0
}
)
2 ( βα 2
β α
+ δ k −k k
,
3

∫ 1

1
2

(6.2)

[

(6.3)

βα
and I˜spin
as given in (3.20). Note that this contribution, too, after renormalization starts
with terms cubic in F , and that on-shell it has an IR divergence through the pole in (6.2).
A proper treatment of the on-shell limit requires a somewhat different interpretation of
the third diagram, namely as a correction to the tree-level amplitude due to the modified
dispersion relation of the photon in the field [44]. In the presence of an external field, the
physical photon eigenmodes no longer satisfy the vacuum on-shell condition k 2 = 0; instead,
their propagation is governed by the dispersion relation k 2 + Π(k) = 0, where Π denotes
the photon polarization tensor, leading in general to a field induced deviation from k 2 = 0.
The corresponding amplitude for a scalar loop is simply obtained by replacing Π̄βα
spin (k; F )

with Π̄βα
scal (k; F ) in (6.1).

7

Weak-field expansion of the tadpole contribution

Since phenomenological applications are primarily concerned with the regime of weak external fields, we briefly discuss the tadpole contribution in the limit of a weak magnetic
background,
eB ≪ m2 .
(6.1)
In this regime, the proper-time integrals admit a systematic asymptotic expansion in powers
of the dimensionless ratio eB/m2 .
For definiteness, we present the weak-field expansion only for the spinor loop, since the
scalar case follows by an entirely analogous procedure. To derive this expansion, it is convenient to return to the proper-time representation of the spinor tadpole contribution given
in Eq. (5.6), prior to performing the z-integration. Specializing to D = 4, the hyperbolic
functions appearing in the integrand can be expanded for small
z = eBT ,

(6.2)

which is justified since the proper-time integral is exponentially dominated by values T ∼
1/m2 in the weak-field regime.

– 16 –

## PDF page 18

A compact representation of the weak-field expansion follows from the series representation of the integrand in Eq. (5.6),
∞

∑ 22n B2n
z
+ coth z − z coth2 z =
z 2n−1 ,
3
(2n − 1)!

(6.3)

n=2

where Bn denotes the Bernoulli numbers. Substituting this expansion into the proper-time
integral and carrying out the integration term by term yields the following closed-form
weak-field expansion for the renormalized spinor tadpole contribution:
(tadpole)

Γ̄spin

ieκ
(2π)−2 (eB)2 tr(r+ ϵ0 f )
4eB
∞
∑
22n B2n ( eB )2n−2
×
Γ(2n − 2) .
(2n − 1)! m2

(k0 = −k, ϵ0 ; k, ε; B) = −

(6.4)

n=2

The corresponding weak-field expansion for the scalar loop can be obtained by the same
method and will not be displayed here.

8

Ward identities for the photon-graviton amplitude in a constant field

Finally, let us discuss how the Ward identities work for the photon-graviton amplitude in
a constant field, returning to the off-shell unrenormalized amplitudes. Here there is no
difference between the scalar and spinor-loop cases. It is easy to see that the gauge Ward
identity holds for each of the three contributions separately, i.e.
Γ(irr),(tadpole),(ext) (−k, ϵ0 ; k, δε; F ) = 0 ,

(7.1)

where δεµi = k µ .
For the gravitational Ward identity, defined by the transformation
µ ν
µ ν
δϵµν
0 = k0 ζ0 + ζ0 k0 ,

(7.2)

a slight extension of the manipulations of the appendix of [21] shows that the inclusion of
the one-photon amplitude leads to
Γ(irr) (k0 , δϵ0 ; k, ε; F ) = Γ(k0 + k, ε̃; F ) + Γ(k0 , ε̃F ; k, ε; F ) ,

(7.3)

where on the right-hand side we have now the one- and two-photon amplitudes, and
ε̃µi ≡ κ(kiµ ενi − εµi kiν )ζ0ν = κ(fi · ζ0 )µ ,

ϵ̃µF ≡ −iκ(F · ζ0 )µ .

(7.4)

However, the first term on the right-hand side of (7.3) vanishes when setting k0 = −k.
Using
k0 · F · ζ0 µ
k0 ,
δυFµ = −ε̃µF − iκ
(7.5)
k02

– 17 –

## PDF page 19

(irr)

(ext)

we can get from (7.3) the following on-shell Ward identity connecting Γspin and Γspin ,
Γ(irr) (−k, δϵ0 ; k, ε; F ) + Γ(ext) (−k, δϵ0 ; k, ε; F ) = 0 ,

(7.6)

while the tadpole contribution on-shell becomes invariant by itself,
Γ(tadpole) (−k, δϵ0 ; k, ε; F ) = 0 ,

(7.7)

as can be easily seen from (5.2) using the on-shell relations k 2 = ε · k = ζ0 · k0 = 0.

9

Conclusions

In this work we have re-examined electromagnetic photon–graviton conversion in a constant external field within Einstein–Maxwell theory at the one-loop level. Although photon–graviton conversion in an electromagnetic field might eventually find applications in a
broader range of physical contexts, here we have focused on its dichroism aspect, motivated
by the analysis of Ref. [44], which demonstrated that this process provides the leading
Standard Model contribution to magnetic dichroism, despite its small absolute magnitude
under realistic conditions.
Our main result is the identification and explicit evaluation of a non-vanishing tadpole
contribution to the one-loop photon–graviton conversion amplitude, corresponding to the
middle diagram in Fig. 2. Contrary to long-standing assumptions, this diagram does not
vanish once the infrared behavior of the connecting photon propagator is treated correctly
in dimensional regularization. Using the worldline formalism, we have provided a unified
calculation of all one-loop contributions — irreducible, tadpole, and other reducible — for
scalar and spinor loops in a general constant electromagnetic background.
Although the tadpole diagram contributes to the full one-loop amplitude, it is irrelevant
for magnetic dichroism already at a structural level. From (5.6) we see that the magnetic
tadpole contribution depends on the photon and graviton polarizations through a global
factor tr(F ϵ0 f ), which (for on-shell gravitons) is proportional to the tree-level amplitude
Γ(tree) (k0 , ϵ0 ; k, ε; F ) of eq. (1.1), implying identical photon–graviton conversion rates for
the two photon polarizations. Consequently, the magnetic dichroism remains unchanged,
and the analysis of Ahlers et al. [44] is not affected by the presence of the tadpole diagram.
In the weak-field regime eB/m2 ≪ 1, relevant for phenomenological applications, the
tadpole contribution is moreover parametrically suppressed compared to the irreducible
one-loop contribution. In the strong-field limit eB/m2 ≫ 1, the relative importance of different one-loop contributions can change qualitatively, as has been demonstrated in related
contexts [71]. In such regimes, tadpole-type contributions may play a more prominent role
in the overall amplitude, which could be relevant not only from a theoretical standpoint but
also in extensions of the Standard Model involving light or weakly charged particles, such
as mini-charged particles [72], for which strong-field effects can become physically relevant.
Independently of these phenomenological considerations, the inclusion of the tadpole diagram is conceptually important. It completes the one-loop description of photon–graviton
conversion in external fields and clarifies its close connection to other one-particle reducible

– 18 –

## PDF page 20

effects in background-field QED. Our results thus provide a consistent and complete framework for future studies, including strong-field backgrounds, non-standard charged sectors,
and higher-loop corrections.

A

Einstein-Maxwell theory

In our euclidean conventions, the action for a scalar field coupled to electromagnetism and
gravity is
∫
]
√ [
S[ϕ, ϕ∗ ; g, A] = dD x g g µν (∂µ − ieAµ )ϕ∗ (∂ν + ieAν )ϕ + (m2 + ξR)ϕ∗ ϕ . (A.1)

In the spin 1/2 case, the euclidean action for a Dirac field Ψ coupled to electromagnetism
and gravity is given by
∫
√
S[Ψ, Ψ̄; e, A] = dD x g Ψ̄( /
∇ + m)Ψ
(A.2)
where the vielbein eaµ and the spin connection ωµab appear inside the Dirac operator
∇ = γ a eµa ∇µ ,
/

1
∇µ = ∂µ + ieAµ + ωµab γ a γ b .
4

(A.3)

Moreover, we will need also the interaction between photons and gravitons, which is described by the action of Einstein-Maxwell theory (in euclidean conventions)
)
(
∫
1
1
D √
µν
S[g, A] = d x g − 2 R + Fµν F
(A.4)
2κ
4
where κ2 = 8πGN . Let us expand this action to quadratic order in the fields. Expanding
gµν = δµν + κhµν and Aµ = Āµ + aµ , so that Fµν = F̄µν + fµν , and using the short-hand
notation h ≡ δ µν hµν , one obtains the following quadratic approximation in the fluctuations
(hµν , aµ ) around the background (δµν , Āµ ):
(
)2
1
1 α
1
1
1
1
2
2
S(2) = d x
(∂α hµν ) − (∂α h) −
∂ hαµ − ∂µ h + (∂µ aν )2 − (∂ µ aµ )2
4
8
2
2
2
2
)
(
κ
1
− hµν F̄ µα F̄ ν α − δ µν F̄ 2
2
4
(
)
1 µν αβ
µα ν
− κhµν F̄ f α − δ F̄ fαβ
4
]}
κ2 [( 1 2 1 2 ) 2
µν αβ
µα ν
µν
β
h − hµν F̄ + h h F̄µα F̄νβ + (2h h α − hh )F̄µβ F̄ν
+
.
4
8
4
(A.5)
∫

D

{

In the second line of this expression, we recognize the linear coupling − κ2 hµν T̄ µν of the
graviton hµν to the stress tensor of the background electromagnetic field
1
T̄ µν = F̄ µα F̄ ν α − δ µν F̄ 2 .
4

– 19 –

(A.6)

## PDF page 21

The existence of this tadpole vertex indicates that the nontrivial background stress tensor
tends to curve space. The third line in (A.5) gives instead the tree-level graviton-photon
conversion in the electromagnetic background. Using plane waves
hµν (x) = ϵ0µν eik0 x ,

aα (x) = εα eikx

(A.7)

we get for this conversion term the vertex (deleting now the ‘bar’ on F )
[
]
1
∆S(2) = (2π)D δ D (k0 + k) ϵ0µν εα (−iκ) F µα k ν − (F · k)µ δ να + δ µν (F · k)α .
2

The two-point functions (which we denote by Π), in either coordinate or momentum
space, are contained in S(2) (or in the quadratic part of the full effective action Γ(2) =
(1−loop)

−S(2) + Γ(2)

+ · · · ) as follows 1
∫

{

1
1
hµν (x)Πµν,λρ (−i∂)hλρ (x) + aα (x)Παβ (−i∂)aβ (x)
2
2
}
κ
µν,α
µν
+hµν (x)Π
(−i∂)aα (x) − hµν (x)T̄ (x)
2
{
∫
D
1
1
d k
hµν (−k)Πµν,λρ (k)hλρ (k) + aα (−k)Παβ (k)aβ (k)
=
D
(2π)
2
2
}
κ
µν,α
µν
+hµν (−k)Π
(k)aα (k) − hµν (−k)T̄ (k) .
2

S(2) =

D

d x

(A.8)

The equations of motion in terms of these two-point functions then read
δaα (−k) :
δhµν (−k) :

Παβ (k)aβ (k) + Πµν,α (−k)hµν (k) = 0
κ
Πµν,λρ (k)hλρ (k) + Πµν,α (k)aα (k) = T̄ µν (k)
2

(A.9)
(A.10)

and, in particular, one obtains from (A.5)
2 αβ
Παβ
− kα kβ ,
tree (k) = k δ
iκ µν,α
Πµν,α
C
tree (k) = −
2

(A.11)
(A.12)

with
(
)µ
(
)ν
(
)α
C µν,α = F µα k ν + F να k µ − F · k δ να − F · k δ µα + F · k δ µν

(A.13)

depicted in Fig. 1.
From the cubic fluctuations, we will still need the term coupling the graviton to two
photons:
∫
(
)
1
κ
Gγγ
S(3) = −
dD x hµν f µα f ν α − δ µν f 2 .
(A.14)
2
4
1

We Fourier transform fields as hµν (k) =
∫ dD k
ikx
hµν (x) = (2π)
.
D hµν (k) e

∫

dD x e−ikx hµν (x), with inverse Fourier transform given by

– 20 –

## PDF page 22

B

Worldline Green’s functions and determinants in a constant field

Define Zµν ≡ eFµν T .
B.1

Periodic case

Determinant factor:
det

1
2

[

]
Z
.
sin Z

(B.1)

Worldline Green’s function and its derivatives:
(
)
T
Z −iZ ĠB12
GB12 =
e
+ iZ ĠB12 − 1 ,
2Z 2 sinZ
(
)
i
Z −iZ ĠB12
ĠB12 =
e
−1 ,
Z sinZ
2 Z −iZ ĠB12
G̈B12 = 2δ12 −
e
T sinZ

(B.2)
(B.3)
(B.4)

Symmetry properties:
T
GB12 = GB21
,

T
ĠB12 = −ĠB21
,

T
G̈B12 = G̈B21
.

(B.5)

Coincidence limits:
T ( cot Z
1 )
− 2 ,
2
Z
Z
i
ĠB (τ, τ ) = icotZ − ,
Z
2
G̈B (τ, τ ) = 2δ(0) − Z cot Z .
T
GB (τ, τ ) =

(B.6)
(B.7)
(B.8)

Weak-field expansion:
( 1
1
i
T) 2
− ĠB12 GB12 Z +
G2B12 −
Z + O(Z 3 ) ,
6 3
3T
90
(G
1)
2
B12
ĠB12 = ĠB12 + 2i
−
Z+
ĠB12 GB12 Z 2 + O(Z 3 ) ,
T
6
3T
(G
2
2
1) 2
B12
−
Z + O(Z 3 ) .
G̈B12 = 2δ12 − + iĠB12 Z − 4
T
T
T
6
GB12 = GB12 −

(B.9)
(B.10)
(B.11)

Even-odd decomposition:
For the purpose of simplifying integrals, it will often be convenient to decompose the
constant-field worldline Green’s functions as
GB12 = SB12 + AB12

(B.12)

where SB denotes the even and AB the odd part as a power series in F . Note that SB is
symmetric as a Lorentz matrix and AB antisymmetric, which motivates our notation.
Special constant fields:

– 21 –

## PDF page 23

• Parallel electric and magnetic fields:
in the generic case, it is possible to find a Lorentz system where E and B both point
along the z - axis. If we further assume, for definiteness, that E · B > 0, then we can
take them both to point along the positive z-axis, E = (0, 0, E), B = (0, 0, B). The
euclidean field strength tensor then takes the form


0 B 0 0
 −B 0 0 0 


F =
(B.13)
 .
 0 0 0 iE 
0 0 −iE 0
Defining z+ ≡ eBT and z− ≡ ieET , the determinant factor (B.1) can then be written
as
[
]
z+ z−
eBT
eET
− 21 sin Z
=
=
det
.
(B.14)
Z
sinh z+ sinh z−
sinh eBT sin eET
We further define Lorentz matrices g+ , g− , and r+ , r− by




1000
0000
0 1 0 0
0 0 0 0




g+ ≡ 
,
g
≡


,
−
0 0 0 0
0 0 1 0
0000
0001




0 100
00 0 0
 −1 0 0 0 
0 0 0 0




r+ ≡ 
r− ≡ 
,
.
 0 0 0 0
0 0 0 1
0 000
0 0 −1 0

(B.15)

Then one can show the following matrix decompositions of the worldline Green’s
functions
µν
SB12
=−

T ∑ AB12 (zα ) µν
gα ,
2 α=±
zα

iT ∑ SB12 (zα ) − ĠB12 µν
rα ,
2 α=±
zα
∑
µν
ṠB12
=
SB12 (zα ) gαµν ,

Aµν
B12 =

(B.16)
(B.17)
(B.18)

α=±

Ȧµν
B12 = −i

∑

AB12 (zα ) rαµν ,

α=±

µν
S̈B12
= G̈B12 δ µν −

Äµν
B12 =

2 ∑
zα AB12 (zα ) gαµν ,
T α=±

2i ∑
zα SB12 (zα ) rαµν .
T α=±

– 22 –

(B.19)
(B.20)
(B.21)

## PDF page 24

These decompositions involve essentially only the two scalar, dimensionless functions
SB12 and AB12 ,
sinh(z ĠB12 )
,
sinh z
cosh(z ĠB12 ) 1
AB12 (z) =
− .
sinh z
z
SB12 (z) =

(B.22)
(B.23)

Of those only AB12 has a non-vanishing coincidence limit,
ABii = coth z −

1
.
z

(B.24)

Let us also write down the first few terms of the weak field expansions of these
functions,
[
]
2 GB12 2 ( 2 GB12
2 G2B12 ) 4
6
SB12 (z) = ĠB12 1 −
z +
+
z + O(z ) , (B.25)
3 T
45 T
15 T 2
(1
( 1
GB12 )
2 G2B12 ) 3
−2
z + O(z 5 ) .
(B.26)
AB12 (z) =
z+ − +
3
T
45 3 T 2

• The purely magnetic field case:

We let the magnetic field point along the positive z-axis and denote z = eBT . Then
the determinant factor (B.1) becomes
[
]
z
− 12 sin Z
det
=
.
(B.27)
Z
sinh z

The decompositions (B.16) - (B.21) now involve only the three matrices g+ , g− and
r+ :
)
T
T(
SB12 (z) − ĠB12 ir+ ,
(B.28)
GB (τ1 , τ2 ) = GB12 g− − AB12 (z)g+ +
2z
2z
ĠB (τ1 , τ2 ) = ĠB12 g− + SB12 (z)g+ − AB12 (z)ir+ ,
(B.29)
2z
2z
G̈B (τ1 , τ2 ) = G̈B12 1l − AB12 (z)g+ + SB12 (z)ir+ .
(B.30)
T
T
The coincidence limits (B.6) - (B.8) turn into
(
)
(
)
T
T
1
T
T
1 z
GB (τ, τ ) = − g− −
coth z −
g+ = − 1l −
coth z − −
g+ ,
6
2z
z
6
2z
z 3
(B.31)
)
(
1
ĠB (τ, τ ) = − coth z −
ir+ ,
(B.32)
z
(
)
(
1)
2z
1
G̈B (τ, τ ) = 2 δ(0) −
1l −
coth z −
g+ .
(B.33)
T
T
z
• The purely electric field case:
To obtain the analogue of the magnetic formulas (B.27) - (B.33) for a purely electric
field pointing into the z-direction, just replace z = eBT by z = ieET and interchange
+ ↔ − everywhere.

– 23 –

## PDF page 25

• The crossed-field case:
In a “crossed field”, defined by E ⊥ B, E = B, both invariants B 2 − E 2 and E · B
vanish. For such a field F 3 = 0, so that the power series (B.9)-(B.11) break off after
their quadratic terms. The worldline correlators thus can be represented by the terms
given there.
The determinant factor becomes unity.
B.2

Anti-periodic case

Determinant factor:
]
1[
det 2 cos Z .

(B.34)

Worldline Green’s function and its derivative:

e−iZ ĠB12
,
cosZ
2i
Z −iZ ĠB12
ĠF (τ1 , τ2 ) = 2δ12 + GF 12
e
.
T
cos Z

GF (τ1 , τ2 ) = GF 12

(B.35)
(B.36)

Symmetry properties:
GF 12 = −GFT 21 ,

ĠF 12 = ĠFT 21 .

(B.37)

GF (τ, τ ) = −i tanZ ,
2
ĠF (τ, τ ) = 2δ(0) + Z tan Z .
T

(B.38)

Coincidence limits:

(B.39)

Weak-field expansion:
GF 12 = GF 12 − iGF 12 ĠB12 Z + 2GF 12
ĠF 12 = 2δ12 +

GB12 2
Z + O(Z 3 ) ,
T

2
2
iZGF 12 + GF 12 ĠB12 Z 2 + O(Z 3 ) .
T
T

(B.40)
(B.41)

Even-odd decomposition:
GF = SF + AF .

(B.42)

Special constant fields:
• Parallel electric and magnetic fields:
With the same notation as in the periodic case above,
]
1[
det 2 cos Z = cosh z+ cosh z− = cosh(eBT ) cos(eET ) ,
– 24 –

(B.43)

## PDF page 26

SFµν12 =

∑

SF 12 (zα ) gαµν ,

α=±

Aµν
F 12 = −

∑

AF 12 (zα ) irαµν ,

α=±

ṠFµν12 = ĠF 12 1l −
Ȧµν
F 12 =

(B.44)

2 ∑
AF 12 (zα ) gαµν ,
T α=±

2 ∑
zα SF 12 (zα ) irαµν .
T α=±

(B.45)
(B.46)
(B.47)

The scalar, dimensionless coefficient functions appearing in these formulas are
SF 12 (z) = GF 12

cosh(z ĠB12 )
,
cosh(z)

(B.48)

AF 12 (z) = GF 12

sinh(z ĠB12 )
.
cosh(z)

(B.49)

Of those, it is AF 12 that has a non-vanishing coincidence limit
AF ii = tanh z .

(B.50)

As for the periodic case above, let us also write down the first few terms of the weak
field expansions of these functions:
]
[
GB12 2 2 ( GB12 G2B12 ) 4
6
z +
+
z + O(z ) ,
(B.51)
SF 12 (z) = GF 12 1 − 2
T
3
T
T2
[
]
(1 2 G
)
B12
AF 12 (z) = GF 12 ĠB12 z −
+
z 3 + O(z 5 ) .
(B.52)
3 3 T
• The purely magnetic field case:
With the same notations as for the periodic case above, the determinant factor becomes
]
1[
det 2 cosZ = cosh z .
(B.53)
The worldline correlators (B.35), (B.36) specialize to

GF (τ1 , τ2 ) = GF 12 g− + SF 12 (z)g+ − AF 12 (z) ir+ ,
2z
2z
ĠF (τ1 , τ2 ) = ĠF 12 1l − AF 12 (z)g+ + SF 12 (z) ir+
T
T

(B.54)
(B.55)

with coincidence limits
GF (τ, τ ) = −tanh z ir+ ,
2z
ĠF (τ, τ ) = 2δ(0)1l − tanh z g+ .
T

(B.56)
(B.57)

• The purely electric field case:
The rules for the transition from the magnetic to the electric field are the same as for
the periodic case above.

– 25 –

## PDF page 27

• The crossed-field case:
As in the periodic case, for a crossed field the determinant factor becomes unity,
and the worldline correlators are given exactly by their weak-field expansion to order
O(F 2 ), (B.40) and (B.41).

Acknowledgments
We would like to thank F. Fillion-Gourdeau and A. Ilderton for helpful discussions and
correspondence.

References
[1] W. K. De Logi and A. R. Mickelson, Phys. Rev. D 16, 2915 (1977).
[2] M. Atsumi, Progress of Theoretical Physics 63, 312 (1980).
[3] S.Y. Choi, J.S. Shim, and H.S. Song, Phys. Rev. D 48, 2953 (1993), arXiv:hep-th/9306250,
Phys. Rev. D 51, 2751 (1995), arXiv:hep-th/9411092.
[4] N. E. J. Bjerrum-Bohr, J. F. Donoghue and B. R. Holstein, Phys. Rev. D 67, 084033 (2003),
arXiv:hep-th/0211071.
[5] S. Hu and F. Zhou, Progress of Theoretical and Experimental Physics 7, 073B10 (2020).
[6] B.R. Holstein, Phys. Rev. D 74, 085002 (2006), arXiv:gr-qc/0607054
Am. J. Phys. 74, 1002 (2006), arXiv:hep-ph/0607187.
[7] F.A. Berends and R. Gastmans, Ann. Phys. 98 (1976) 225.
[8] P. Bittar, S. Fichet and L. de Souza, Phys. Rev. D 112, 045009 (2025),
arXiv:hep-th/2404.07254.
[9] V. P. Frolov, W. Israel, and S. N. Solodukhin, Phys. Rev. D 54, 2732 (1996),
arXiv:hep-th/9602105.
[10] N. K. Nielsen, Annals Phys. 327, 861 (2012), arXiv:hep-th/1109.2699.
[11] I. Y. Park, Progress of Theoretical and Experimental Physics 2021, 013B03 (2021),
arXiv:gr-qc/1807.11595.
[12] M.E. Gertsenshtein, Sov. Phys. JETP 14 (1962) 84.
[13] Ya. B. Zel’dovich and I.D. Novikov, The structure and evolution of the universe, Rel.
Astrophys. Vol. 2 (1983), Chicago University Press.
[14] G. Raffelt and L. Stodolsky, Phys. Rev. D37, 1237 (1988).
[15] H. N. Long, D.V. Soa, and T. A. Tran, Mod. Phys. Lett. A9 (1994) 3619,
arXiv:astro-ph/9410003.
[16] J. C. R. Magueijo, Phys. Rev. D49 (1994) 671.
[17] P. Chen, Phys. Rev. Lett. 74 (1995) 634; erratum-ibid. 74 (1995) 3091.
[18] A.N. Cillis and D. Harari, Phys. Rev. D54 (1996) 4757, arXiv:astro-ph/9609200.
[19] C. Deffayet and J.-P. Uzan, Phys. Rev. D62 (2000) 063507, arXiv:hep-ph/0002129.

– 26 –

## PDF page 28

[20] A. Ejlli, D. Ejlli, A.M. Cruise, G. Pisano and H. Grote, Eur. Phys. J. C 79 (2019) 1032,
arXiv:gr-qc/1908.00232.
[21] F. Bastianelli and C. Schubert, JHEP 0502, 069 (2005), arXiv:gr-qc/0412095.
[22] M.J. Strassler, Nucl. Phys. B 385 (1992) 145, arXiv:hep-ph/9205205.
[23] M.G. Schmidt and C. Schubert, Phys. Lett. B 318, 438 (1993), arXiv:hep-th/9309055.
[24] R. Zh. Shaisultanov, Phys. Lett. B 378 (1996) 354, arXiv:hep-th/9512142.
[25] S.L. Adler and C. Schubert, Phys. Rev. Lett. 77 (1996) 1695, arXiv:hep-th/9605035.
[26] M. Reuter, M. G. Schmidt and C. Schubert, Ann. Phys. (N.Y.) 259 (1997) 313,
arXiv:hep-th/9610191.
[27] C. Schubert, Phys. Rept. 355, 73 (2001), arXiv:hep-th/0101036.
[28] F. Bastianelli and A. Zirotti, Nucl. Phys. B 642, 372 (2002), arXiv:hep-th/0205182.
[29] F. Bastianelli, O. Corradini and A. Zirotti, JHEP 0401 023 (2004), arXiv:hep-th/0312064.
[30] F. Bastianelli, O. Corradini and A. Zirotti, Phys. Rev. D 67, 104009 (2003),
arXiv:hep-th/0211134.
[31] F. Bastianelli and P. van Nieuwenhuizen, Path integrals and anomalies in curved space,
Cambridge University press, 2006.
[32] W. Dittrich, R. Shaisultanov, Phys. Rev. D 62 (2000) 045024, arXiv:hep-th/0001171.
[33] C. Schubert, Nucl. Phys. B 585, 407 (2000), arXiv:hep-ph/0001288.
[34] W. Dittrich and M. Reuter, Effective Lagrangians in Quantum Electrodynamics, Springer
1985.
[35] V. I. Ritus, Sov. Phys. JETP 42, 774 (1975).
[36] W. Dittrich and H. Gies, Probing the Quantum Vacuum, Springer 2000.
[37] F. Bastianelli, U. Nucamendi, C. Schubert, and V. M. Villanueva, JHEP 0711 (2007) 099,
arXiv:gr-qc/0710.5572.
[38] L. Maiani, R. Petronzio, E. Zavattini, Phys. Lett. B 175, 359 (1986).
[39] P. Sikivie, Phys. Rev. Lett. 51, 1415 (1983); Erratum: Phys. Rev. Lett. 52, 695 (1984).
[40] A. Mirizzi, G. G. Raffelt, P. D. Serpico, Lect. Notes Phys. 741, 115 (2006),
arXiv:astro-ph/0607415.
[41] E. Masaki, A. Aoki, J. Soda, Phys. Rev. D 96, 043519 (2017), arXiv:astro-ph/1702.08843.
[42] S. Villalba-Chávez, Nucl. Phys. B 881, 391 (2014), arXiv:hep-ph/1308.4033.
[43] H. Tam and Q. Tang, Nucl. Phys. B 716, 435 (2012), arXiv:hep-ph/1107.1712.
[44] M. Ahlers, J. Jaeckel and A. Ringwald, Phys. Rev. D 79 075017 (2009),
arXiv:hep-ph/0812.3150.
[45] R. Schützhold, Phys. Rev. Lett. 135, 171501 (2025), arXiv:gr-qc/2502.10221.
[46] F. Fillion-Gourdeau and S. MacLean, Phys. Rev. D 111, 122004 (2025),
arXiv:gr-qc/2506.05534.
[47] A. T. Schmitt, Y. Joly et al, Optica 8, 56 (2021), arXiv:physics.ins-det/2003.00849.
[48] B. Marx, K. S. Schulze et al, Phys. Rev. Lett. 110, 254801 (2013).

– 27 –

## PDF page 29

[49] H. Bernhardt, A. T. Schmitt et al, Phys. Rev. Res. 2, 023365 (2020).
[50] S-J. Chen, H-H. Mei and W-T Ni, Mod. Phys. Lett. A 22, 2815 (2007),
arXiv:hep-ex/0611050.
[51] F. Della Valle, A. Ejlli et al, Eur. Phys. J. C. 76, 1 (2016), arXiv:physics.optics /1510.08052.
[52] A. Ejlli, F. Della Valle et al, Phys. Rept. 871, 1 (2020), arXiv:physics.optics /2005.12913.
[53] G. Zavattini, F. Della Valle et al, Eur. Phys. J. C. 82, 1 (2022),
arXiv:physics.optics/2110.03943.
[54] E.S. Fradkin, D.M. Gitman, S.M. Shvartsman, Quantum Electrodynamics with Unstable
Vacuum, Springer 1991.
[55] H. Gies and F. Karbstein, JHEP 1703 (2017) 108, arXiv:hep-th/1612.07251.
[56] F. Karbstein, JHEP 10, 075 (2017), arXiv:hep-th/1709.03819.
[57] F. Karbstein, JHEP 01, 057 (2022), arXiv:hep-th/2109.04823.
[58] M. Bordag and I. G. Pirozhenko, MDPI Physics 6, 237 (2024).
[59] J. P. Edwards and C. Schubert, Nucl. Phys. B 923 (2017) 339, arXiv:hep-th/1704.00482.
[60] N. Ahmadiniaz, F. Bastianelli, O. Corradini, J. P. Edwards and C. Schubert, Nucl. Phys. B
924 (2017) 377, arXiv:hep-th/1704.05040.
[61] N. Ahmadiniaz, J. P. Edwards and A. Ilderton, JHEP 05 (2019) 038,
arXiv:hep-th/1901.09416.
[62] N. Ahmadiniaz, F. Bastianelli, F. Karbstein and C. Schubert, Proceedings of Sixteenth
Marcel Grossmann Meeting on General Relativity, July 5-10, 2021, Eds. R. Ruffini and
Gregory V. Vereshchagin, World Scientific, February 2023, 4393-4400,
arXiv:hep-ph/2111.01980.
[63] F. Bastianelli, O. Corradini, J. M. Dávila and C. Schubert, Phys. Lett. B 716, 345 (2012),
arXiv:hep-th/1202.4502.
[64] N. Ahmadiniaz, F.M. Balli, O. Corradini, J.M. Dávila and C. Schubert, Nucl. Phys. B 950
(2020) 114877, arXiv:hep-th/1908.03425.
[65] F. Bastianelli and C. Schubert, Worldline Path Integrals and Quantum Field Theory,
Cambridge University Press (To appear).
[66] E. Leader and E. Predazzi, J. Phys. G 40 (2013) 075001, arXiv:hep-ph/1101.3425.
[67] N. Ahmadiniaz and C. Schubert, Eur. Phys. Lett. 130 (2020) 41001,
arXiv:hep-th/2001.00885.
[68] N. Ahmadiniaz, M. A. Lopez-Lopez and C. Schubert, Phys. Lett. B 852 (2024) 138610,
arXiv:hep-th/2312.07047.
[69] M.A. Lopez Lopez, Phys. Lett. B 860 (2025) 139157, arXiv:hep-th/2408.16474.
[70] I. Ahumada, P. Copinger and J.P. Edwards, Phys. Rev. D 112 (2025) 096024,
arXiv:hep-th/2507.22308.
[71] F. Karbstein, Phys. Rev. Lett. 122 (2019) 211602, arXiv:hep-th/1903.06998.
[72] B. Döbrich, H. Gies, N. Neitz, F. Karbstein, Phys. Rev. Lett. 109 (2012) 131802,
arXiv:hep-ph/1203.2533.

– 28 –
