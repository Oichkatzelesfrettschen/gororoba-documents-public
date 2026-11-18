Source: https://doi.org/10.1140/epjc/s10052-019-7583-9
PDF sha256: e0173da29e19eb87e4876adbd71d8addcd9676d7fee83ec4a824725bf520f524
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of herdeiro_2020_solitons_in_maxwell_scalar_and_einstein_maxwell_scalar_models.pdf

Transcription of `herdeiro_2020_solitons_in_maxwell_scalar_and_einstein_maxwell_scalar_models.pdf` in this directory, 9 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-9 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Eur. Phys. J. C (2020) 80:23
https://doi.org/10.1140/epjc/s10052-019-7583-9

Regular Article - Theoretical Physics

A class of solitons in Maxwell-scalar and Einstein–Maxwell-scalar
models
Carlos A. R. Herdeiro1,a , João M. S. Oliveira1,2,b , Eugen Radu1,c
1 Departamento de Matemática da Universidade de Aveiro, CIDMA, Campus de Santiago, 3810-183 Aveiro, Portugal
2 Centro de Matemática, Universidade do Minho, 4710-057 Braga, Portugal

Received: 29 October 2019 / Accepted: 21 December 2019 / Published online: 11 January 2020
© The Author(s) 2020

Abstract Recently, no-go theorems for the existence of
solitonic solutions in Einstein–Maxwell-scalar (EMS) models have been established (Herdeiro and Oliveira in Class
Quantum Gravity 36(10):105015, 2019). Here we discuss
how these theorems can be circumvented by a specific class
of non-minimal coupling functions between a real, canonical scalar field and the electromagnetic field. When the nonminimal coupling function diverges in a specific way near the
location of a point charge, it regularises all physical quantities yielding an everywhere regular, localised lump of energy.
Such solutions are possible even in flat spacetime Maxwellscalar models, wherein the model is fully integrable in the
spherical sector, and exact solutions can be obtained, yielding
an explicit mechanism to de-singularise the Coulomb field.
Considering their gravitational backreaction, the corresponding (numerical) EMS solitons provide a simple example of
self-gravitating, localised energy lumps.

1 Introduction
Einstein-Maxwell-scalar (EMS) models, described by the
action
∫
√
1
d 4 x −g
S=
4π
(
)
f (φ)
R
1
−
Fμν F μν − ∂μ φ∂ μ φ ,
(1)
4
4
2
wherein the real scalar field φ has a canonical kinetic term and
it is non-minimally coupled to the Maxwell field strength F,
via some function f (φ), emerge naturally in physics (R is the
Ricci scalar). Well known contexts are Kaluza–Klein models
[2–6] and supergravity/string theory [7]. In these cases the
a e-mail: herdeiro@ua.pt
b e-mail: jmiguel.oliveira@ua.pt
c e-mail: eugen.radu@ua.pt

non-minimal coupling is provided by an exponential function
of the sort f (φ) ∼ e−αφ , where α is a constant. But more
general classes of coupling functions have been considered,
for instance, in the context of cosmology [8,9].
Another interesting class of coupling functions emerged
recently in the quest for models that deviate from general
relativity only in the strong gravity regime. If f (φ) obeys
some simple properties, the EMS model accommodates the
phenomenon of spontaneous scalarisation of asymptotically
flat charged black holes [10]. This means that even though
the electrovacuum Reissner–Nordström (RN) black hole is
a solution of the EMS model, for sufficiently high charge
to mass ratio this black hole becomes unstable: it becomes
energetically favourable for the RN black hole to scalarise.
A new family of scalarised black holes bifurcates from the
RN family, which contains the end states of this dynamical
scalarisation mechanism – see also [11–21].
The existence of such a class of EMS models, that allow
spontaneous scalarisation of charged black holes, and accommodates two distinct families of black holes, the bald RN and
the “hairy” scalarised BHs, raised the question if solitons can
also be found in EMS models, as this is often the case in theories that accommodate both bald and hairy BHs. Building
on this question, in [1] a set of theorems were established
showing that, under various assumptions, no such solitonic
solutions exist, similarly to the case of vacuum and electrovacuum. The purpose of this paper is to show that dropping one of the assumptions considered in [1], namely that
the coupling function is everywhere finite, it becomes possible to circumvent the aforementioned theorems and obtain
solitonic solutions, including in the flat spacetime (Maxwellscalar theory) limit. In the latter case, moreover, the solitons
can be, in some examples, obtained in closed form. They
yield pedagogical illustrations of how new physics could desingularise the Coulomb solution at the level of an effective
field theory. In the self-gravitating case, the solutions are
obtained numerically, although we cannot exclude that some

123

## PDF page 2

23 Page 2 of 9

Eur. Phys. J. C (2020) 80:23

carefully designed coupling functions exist where they will
have a closed analytic form.
This paper is organised as follows. In Sect. 2 we discuss
the flat spacetime analysis, i.e. the Maxwell-scalar model in
Minkowski spacetime. We show that the model is integrable
and how the Coulomb singularity can be regularised by a
divergent coupling in a class of explicit examples. In Sect. 3
we consider the self-gravitating solitons, corresponding to
the solutions discussed in flat spacetime in Sect. 2. Conclusions are presented in Sect. 4.

∫

An awkward feature of classical electromagnetism is that
the energy E of the Coulomb field of a point charge Q is
divergent:
∫ +∞ 2
Q
dr = ∞.
(2)
E∼
r2
0
Quantum considerations naturally introduce an ultraviolet
cut-off to the validity of the classical Coulomb solution,
regularising this integral. Quantum Electrodynamics (QED),
however, is itself incomplete as a quantum field theory, due to
the Landau pole [22]. But it yields the important lesson that
the coupling constant g, which determines the strength of the
electromagnetic interaction in the Maxwell Lagrangian
(3)

runs with the energy scale.
Whatever fundamental theory turns out to complete QED,
it may admit a covariant effective field theory description
that captures the dynamics of the coupling. Then, g would
emerge as a spacetime function with some dynamics. In a
simple model, g would be a real scalar field with a standard
kinetic term. Allowing a more general dynamics, one takes g
as being an arbitrary function of the scalar field, keeping the
latter with a standard kinetic term. This suggests considering
the naive covariant effective field theory
∫
√
1
d 4 x −g
S=
4π
(
)
f (φ)
1
−
Fμν F μν − ∂μ φ∂ μ φ ,
(4)
4
2
where φ is a real scalar field, F = d A is the covariant description of the electromagnetic dynamics and the background
is Minkowski spacetime. The function f (φ) specifies the
dynamics of the gauge coupling. This model ignores higher
order corrections in F, so it is certainly incomplete. Nonetheless one may take the aforementioned reasoning as a motiva-

123

The naive model (4), which is the decoupling limit of the
EMS model (1) wherein back reaction is neglected, is integrable in the spherical sector. Taking the following ansatz for
the fields in spherical coordinates in Minkowski spacetime
(t, r, θ, ϕ):
A = V (r )dt,

(5)

the Maxwell equations yield a first integral:

2.1 A physical motivation

1
Fμν F μν ,
4g 2

2.2 An integrable model

φ = φ(r ),

2 Flat spacetime Maxwell-scalar models

L=−

tion to consider this class of simple models. Can the Coulomb
field of a point charge be de-singularised in this context?

V (r ) =

Q
r 2 f (φ)

dr,

(6)

where Q is interpreted as the electric charge. Using this first
integral, the Klein-Gordon equation reads
(
)
(
)
Q2 d
1
2 dφ
r
−
= 0,
r
dr
dr
2 dφ f (φ)
2 d

(7)

which, introducing the coordinate x ≡ 1/r , yields another
first integral
(

dφ
dx

)2
−

Q2
= E.
f (φ)

(8)

It is a simple application of the virial theorem, or a Derricktype scaling theorem [23], to show that solutions must have
E = 0. For instance, this can be seen from the condition [24]
∫
d 3 x Ti j = 0,

(9)

that holds for time-independent, finite energy field configuration in Minkowski spacetime, where i, j are spatial indices in
Cartesian coordinates. Relation (9) is a simple consequence
of energy–momentum conservation and can be interpreted as
the balancing of the total stresses in an extended object. There
are regions where matter is in tension and regions where it
is in compression, for any static balanced soliton. Thus, the
problem of finding solutions is reduced to solving, from (8),
x(φ) =

1
Q

∫ √

f (φ)dφ,

(10)

and then inverting x(φ) → φ(x) → φ(r ). Fixing the coupling function f (φ) one can obtain φ(r ) and, from (6), the
electrostatic potential, both as line integrals. Due to the two
first integrals the system is fully integrable.

## PDF page 3

Eur. Phys. J. C (2020) 80:23

Page 3 of 9 23

2.3 Everywhere regular solutions

2.4.1 A simple coupling yielding regular solutions

To assess if the solutions have finite energy one must consider
the energy–momentum of the model,
)
(
1
4π Tμν = f (φ) Fμα Fν α − gμν Fαβ F αβ
4
1
(11)
+∂μ φ∂ν φ − gμν ∂α φ∂ α φ.
2

As an explicit example, consider

This yields the energy density ρ, after using (8):
ρ = T00 =

Q2
4πr 4 f (φ)

.

(12)

E=

ρd x =
3

∫ +∞
0

Q2
dr.
r 2 f (φ)

(13)

In order to obtain regular solutions at the origin we assume
the scalar field admits a power series expansion near the origin:
∑
φ pr p ,
(14)
φ = φ0 +

(−Nr N +1 φ N + . . . )2 =

Q2
f (φ)

.

(15)

Thus, as r → 0,
f (φ) ∼

Q
.
Qα + r

(16)

Regularity of the scalar field at the origin then requires the
coupling to diverge as ∼ 1/r 2N +2 . From (12) this implies
that the energy density is finite therein and from (6),

(19)

The coupling diverges as 1/r 4 at the origin, as anticipated.
This divergence precisely cancels the divergence of the
Maxwell field at the origin, c f. (12), making it finite and
non-zero. In fact, the energy density, from (12), is
ρ=

Q2
.
4π(Qα + r )4

(21)

It follows that the total energy (13) is
E=

Q
.
3α

(22)

Now, using (6) we obtain for the electrostatic potential:
V (r ) = −

1
Q2
.
N 2 φ 2N r 2N +2

(18)

One observes that φ(r ) is regular and smooth as r → 0,
φ(r ) ≃ 1/α − r/(Qα 2 ); thus we expect, from (16), that the
coupling to diverge as 1/r 4 . Asymptotically, on the other
hand, φ(r ) ≃ Q/r . Thus the scalar “charge” coincides with
the electric charge. Plugging (19) into (18) yields:
)
(
αQ 4
.
(20)
f (r ) = 1 +
r

p=N

We do not constrain the constant coefficient φ0 , which may
or may not vanish. Apart from φ0 , let φ N , where N ∈ N ⩾ 1
be the first non-vanishing coefficient in this expansion. Then,
from (8),

1
,
(1 − αφ)4

where α is a non-zero constant. Then (10) immediately
yields, taking the integration constant such that φ → 0 as
r → ∞:
φ(r ) =

and the total energy, E, obtained by integrating the energy
density on a spacelike slice
∫

f (φ) =

rQ
α2 Q 3
−
.
(Qα + r )2
3(Qα + r )3

(23)

All the quantities (21), (22), (23) manifestly reduce to the
usual Coulombic ones upon taking α → 0. In such case (19)
reduces to the profile of a scalar charge Q at the origin. The
expressions make manifest how α regularises the solution.
2.4.2 A family of couplings yielding regular solutions

V (r ) = V (0) +

N 2 φ 2N
(2N + 1)Q

r 2N +1 + . . . ,

(17)

close to the origin. Thus, all physical quantities are finite close
to the origin, for this class of behaviours of the coupling.
2.4 A class of examples
There is still, of course, some freedom in choosing the coupling function, within the class with the correct divergent
behaviour at the origin. Let us consider examples.

As further examples, with slightly different features, we generalise the coupling (18) as
f (φ) =

1
,
(1 − αφ)n

(24)

where n is an integer. Using this coupling, Eq. (10) gives
∫
1
1
(25)
=
(1 − αφ)−n/2 dφ,
r
Q
which has a different indefinite integral for n ̸= 2 and n = 2.

123

## PDF page 4

23 Page 4 of 9

Eur. Phys. J. C (2020) 80:23

For n ̸= 2, imposing φ(r → ∞) = 0 to fix the integration
constant, one obtains
[
] 2
1
α Q(n − 2) 2−n
1
1+
,
(26)
φ(r ) = −
α
α
2r
which reduces to (18) for n = 4. For regular solutions at the
origin we require limr →0 φ to be finite. This implies n > 2,
in which case
(
) 2
n−2
2r
1
1
,
(27)
lim φ(r ) = −
r →0
α
α α Q(n − 2)
which is finite, as required. For n = 3 we see that the second
term goes as r 2 ; but for n > 4, the second term has a noninteger power. In the former case we anticipate, from (16),
that the coupling diverges as 1/r 6 . In the latter case, φ is
not analytic at the origin. It will, nonetheless yield a regular
solution, when analysing the usual physical quantities.
The coupling f (φ) as a function of r then reads:
] 2n
[
n−2
αQ
(n − 2)
,
(28)
f (r ) = 1 +
2r
2n

which diverges as ∼ 1/r n−2 at the origin, for n > 2, but
respects the condition limr →∞ f (r ) = 1. We confirm, in
particular, the 1/r 6 divergence, for n = 3 and a divergence
with (generically) a non-integer inverse power for n ⩾ 5.
The electric field E μ = −∂μ V (r ) has only one non-zero
component which reads, from (6)
[
]− 2n
n−2
Q
αQ
Q
,
(29)
Er (r ) = − 2 = − 2 1 +
(n − 2)
r f
r
2r
4

which behaves as r n−2 near the origin, and it is thus regular
for n > 2.
The total energy now reads

This is because, again, φ in this case does not admit a power
series expansion near the origin. This illustrates yet a different example of divergent coupling that yields regular solutions.
The electric field is now
Q
Q
Er (r ) = − 2 = − 2 e−2α Q/r ,
r f
r
and the total energy is
E=

Q
.
2α

2.5 Dilatonic coupling: a spherically symmetric solution
As mentioned in the Introduction, a dilatonic coupling
f (φ) = e−αφ ,

)
1(
1 − e−α Q/r ,
α

where α is a constant, emerges in relevant scenarios. Let us
thus briefly mention the existence of a spherically symmetric,
exact solution for this coupling.
Considering (35) in (10), and taking the integration constant so that the scalar field vanishes asymptotically we
immediately get

f (r ) = e

,

(31)

(36)

]
[
αQ 2
f (φ) = e−αφ = 1 +
.
2r

(37)

Thus, the coupling diverges at the origin and, if α Q > 0 it is
regular elsewhere. Moreover, using now (6) we get
V (r ) = −

2Q
.
α Q + 2r

(38)

One finds the following small-r expansion of the solution

(32)

which, as before, also diverges at r = 0 but respects
limr →∞ f (r ) = 1. Observe, however, it does not diverge as
an inverse power of r , which was the conclusion in Sect. 2.3.

123

[
]
αQ
2
log 1 +
.
α
2r

Thus, the coupling, as a function of r is

which is a regular solution at r = 0 with limr →0 φ(r ) = 1/α.
The coupling function f (φ) becomes
2α Q/r

(35)

(30)

Thus, the family of cases with n > 2 illustrate how regular
solutions can be obtained, with a different analytic behaviour
of the scalar field near the origin (the cases n = 3 and n = 4)
and non-analytic behaviour (n > 4).
With n = 2, following a similar reasoning one obtains
φ(r ) =

(34)

In these considerations α Q was assumed to be positive.
Otherwise the total energy (30)–(34) would be negative,
which would violate the weak energy condition. Interestingly
enough, despite the seemingly different solution for n = 2,
the total energy E is a smooth function of the power n, as
(34) coincides with setting n = 2 in (30).

φ=−
2Q
.
E=
(n + 2)α

(33)

φ(r ) =

2
α

V (r ) = −

(
log r − log

αQ
2

)
+ O(r ),

2
4r
+ 2 + O(r 2 ) ;
α
α Q

(39)

## PDF page 5

Eur. Phys. J. C (2020) 80:23

Page 5 of 9 23

thus, the scalar field diverges at the origin. Asymptotically,
on the other hand, both fields are well behaved
( )
α Q2
1
Q
,
+
O
φ(r ) = − +
2
r
4 r
r3
( )
Q
α Q2
1
V (r ) = − +
.
(40)
+
O
r
2 r2
r3
The energy density of this solution diverges at the origin:
ρ = −Ttt =

Q2
πr 2 (α Q + 2r )2

;

the total mass, however, is finite
∫ ∞
2Q
.
drr 2 ρ =
M = 4π
α
0

(41)

(42)

3 The gravitating solitons
The above flat spacetime solutions can be made to selfgravitate by coupling (4) to Einstein’s general relativity. For
the case of the regular solutions described in the previous
section, this yields, perhaps, the simplest models of charged
soliton.
One now considers the EMS model (1), where c = G = 1.
In addition to the ansatz (5) we consider the metric form
dr 2
+ r 2 (dθ 2 + sin2 θ dϕ 2 ) ,
N (r )
2m(r )
,
(43)
where N (r ) ≡ 1 −
r

ds 2 = −e−2δ(r ) N (r )dt 2 +

and m(r ) is the Misner–Sharp mass; r is thus the areal radius,
a geometrically meaningful coordinate.
The ansatz (5) and (43) yield the following effective
Lagrangian:
r 2 −δ
r2
e N φ ′2 +
f (φ)eδ V ′2 .
2
2

(44)

As in the flat spacetime case, the equation of the electric
potential possesses a first integral, which generalises (6), and
reads
Q
,
V ′ = e−δ 2
r f (φ)

r2
Q2
N φ ′2 + 2 S(φ),
2
2r
δ ′ + r φ ′2 = 0,
e−δ d S(φ) 2
(e−δ r 2 N φ ′ )′ − 2
Q =0,
2r dφ
m′ =

(46)
(47)
(48)

where we have defined
S(φ) ≡

1
.
f (φ)

(49)

The smooth of a spacetime configurations can be assessed
by analysing the Ricci scalar

This solution is interesting in that it shows a divergent coupling can source a finite mass configuration which, nonetheless, is not fully regular, as the scalar field and the energy
density diverge at the origin.

Leff = e−δ m ′ −

of generality. Using this integral, the remaining equations of
motion become1

(45)

where again the integration constant Q is the electric charge,
which we shall assume to be strictly positive, without any loss

R=

N
(3r δ ′ − 4)
r
]
2 [
+ 2 1 + N (r 2 δ ′′ − (1 − r δ ′ )2 ) − N ′′ ,
r

and the Kretschmann scalar
]
2 [
4
K = 4 (1 − N )2 + 2 N ′2 + (N ′ − 2N δ ′ )2
r
r
]2
[
′′
′ ′
+ N − 3δ N + 2N (δ ′2 − δ ′′ ) .

(50)

(51)

3.1 Asymptotic expansions
3.1.1 Near the origin
A small r analysis of the field equations confirms the conclusion observed in the flat space analysis: for a scalar
field admitting a power series expansion near the origin
φ = φ0 + φ1r + . . . and φ1 ̸= 0, if the coupling diverges as
1/r 4 , finite energy, everywhere regular solutions are possible. To see this, we again start by assuming the existence of
a power series expansion of solutions, with the scalar field
approaching a finite nonzero value
φ(r ) → φ0 as r → 0,

(52)

where φ0 is arbitrary. Then, the equations of motion, together
with the assumption of regularity, impose, for the n th derivative of S(φ) computed at the origin, denoted S (n) (φ0 ),
S(φ0 ) = S (1) (φ0 ) = S (2) (φ0 ) = S (3) (φ0 ) = 0,
whereas S (4) (φ0 ) > 0.

(53)

This implies the advertised behaviour: the coupling function
f (φ) diverges as 1/r 4 as r → 0. This behaviour cancels the
divergence associated with the presence of an electric charge,
providing a smooth configuration as r → 0.
1 There is an extra equation, which is a constraint and can be derived

from (46)–(48).

123

## PDF page 6

23 Page 6 of 9

Eur. Phys. J. C (2020) 80:23

The small r expansion of the matter functions reads
√
2 6r
φ(r ) = φ0 − √
+ φ2 r 2 + . . . ,
Q S (4) (φ0 )
V (r ) = −

8e−δ0
r3 + . . . ,
Q 3 S (4) (φ0 )

yields the following approximate solutions:
m(r ) = M −
(54)

while for the metric functions we find
√
1
8
2 6φ2
3
r4 + . . . ,
m(r ) = 2 (4)
r − √
Q S (φ0 )
Q S (4) (φ0 )
δ(r ) = δ0 −

12r 2
Q 2 S (4) (φ0 )

+ ...,

(55)

where φ2 and δ0 are constants that are fixed by the numerics
when integrating the field equations from the origin to infinity
and requiring the correct asymptotic behaviour. With this
expansion, both the Kretschmann curvature scalar and Ricci
scalar are finite as r → 0, taking the form
K ≡ Rμναβ R μναβ

√
3840
2560 6φ2
= 4 (4)
− 3 (4)
r + ...,
Q [S (φ0 )]2
Q [S (φ0 )]3/2

(56)

√
48
16 6φ2
R = 2 (4)
r + ...
−
Q S (φ0 )
Q(S (4) (φ0 ))1/2

The small r expansion of S(φ) reads
√
24
8 6φ2
√
S(φ) = 4 (4)
r5 + . . . ,
r4 −
3
(4)
Q S (φ0 )
Q S (φ0 )

(57)

(58)

1
∼ (φ − φ0 )4 as r → 0 .
f (φ)

(59)

Of course, we could have assumed that in the scalar field
expansion φ1 = 0 and the power series starts at a higher order
term. This would impact in the way the coupling diverges at
the origin, similarly to the flat spacetime analysis of Sect. 2.3.
For concreteness, here we focus on the case with φ1 ̸= 0. This
case corresponds, in the non-back-reacting case, to having
N = 1 in Eq. (14). Choosing φ1 = 0 in the latter would imply
a different behaviour for the divergence of f (φ), implied
by the Eq. (16). In the back-reacting case this would correspond to having S (4) (φ0 ) = 0. Non-trivial solutions with
such behaviour should exist, as well.
3.1.2 Near infinity
A large r analysis of the field equations, on the other hand,
imposing
f (φ) → 1 as r → ∞,

123

(60)

(61)
δ(r ) =

Q 2s
+ ...
2r 2

(62)

Here M is the ADM mass and Q is the electric charge; is the
electrostatic potential at infinity and Q s is the scalar ’charge’
which in general needs not equal the electric charge (it did in
the flat spacetime illustration above). In fact, the equations
of motion possess again two first integrals implying that the
gravitating solutions satisfy the following relation
M 2 + Q 2s = Q 2 .

(63)

This last equation, in particular, shows manifestly the curved
background breaks the equality between Q and Q s .
Interestingly, one can show that there is a Smarr relation
in terms of these asymptotic quantities, which is not affected
by the scalar field,
Q.

(64)

Moreover, a first law of thermodynamics can be obtained in
the form
dM =

which implies the following generic approximate form of
the coupling function
S(φ) =

Qs
+ ...,
r
Q
V (r ) = −
+ ... ,
r
φ(r ) =

M=

and

Q 2 + Q 2s
+ ...,
2r

dQ .

(65)

We emphasise the absence of a scalar field contribution in
these relations.
3.2 The full solutions
The gravitating version of the exact solution in Minkowski
spacetime described in Sect. 2.4.1, with coupling (18), and
whose asymptotic limits have been described in Sect. 3.1,
can be constructed numerically. The set of four ordinary differential equations obtained from the above setup was solved
numerically by using a standard Runge–Kutta ordinary differential equation solver and appropriate boundary conditions. Fixing α, gravitating solitons exist for arbitrary large
values of Q. The profile of a typical solution is shown in
Fig. 1. As one can see, the profiles of the various functions, and in particular that of the Kretschmann scalar K ,
are smooth as r → 0. In Fig. 2 we show the ADM mass vs.
electric charge diagram for families of solutions with different values of α. One can see that for all families, the solutions
trivialise as α → 0. Moreover, a smaller α implies that the
same value of the electric charge can support a more massive
soliton. Obviously, the solutions also trivialise as Q → 0.
The electric charge supports the soliton. This is also manifest from the following virial identity that can be derived for
these solutions:

## PDF page 7

Eur. Phys. J. C (2020) 80:23

Page 7 of 9 23

2

α=0.7143 Qe=2

K(r)/3
1.5

φ(r)
e-2δ(r)

1

m(r)
V(r)

0.5

0

-2

0

2

log10r

4

The perturbative solutions are obtained by performing a
power series expansion for all relevant functions
∑ ( 1 )k
m k (r ) ,
m(r ) =
α
k⩾1
∑ ( 1 )k
δ(r ) =
δk (r ),
(67)
α
k⩾1
∑ ( 1 )k
φ(r ) =
φk (r ),
α
k⩾1
∑ ( 1 )k
V (r ) =
Vk (r ) .
(68)
α
k⩾1

Fig. 1 Profiles of an illustrative gravitating soliton with the coupling
(18)
5

α=0.2
4

As for the numerical solutions of the previous subsection,
we focus on the quartic coupling function (18). Solving iteratively the field equations order by order in 1/α, we arrive at
the following expressions2
qr 3
,
3(q + r )3
qr 4 (10q 2 + qr + r 2 )
,
m 4 (r ) = −
90(q + r )6
q 2 (q + 3r )
,
δ1 (r ) = 0 = δ3 (r ), δ2 (r ) =
6(q + r )3
q 2 (q 4 + 6q 3 r + 15q 2 r 2 + 100qr 3 − 30r 4 )
,
δ4 (r ) =
540(q + r )6
q
q(2q − r )r 2
,
φ1 (r ) =
, φ2 = 0, φ3 (r ) =
q +r
18(q + r )4
r3
, V2 (r ) = 0,
V1 (r ) =
3(q + r )3
r 3 (5q 3 + 25q 2 r + 6qr 2 + r 3 )
,
(69)
V3 (r ) = −
90(q + r )6

m 1 (r ) = 0 = m 3 (r ), m 2 (r ) =
3

α=1.25

M

α=0.66
2

α=2

1

α=10
0

0

2

4

6

8

10

Q

Fig. 2 ADM vs. electric charge for families of gravitating solitons
with different values of α. The straight lines are obtained from the perturbative solutions, whereas the dots represent the numerical solutions

∫ ∞
0

dr e−δ φ ′2 =

∫ ∞
dr
0

e−δ Q 2
.
r 2 f (φ)

(66)

For Q = 0 the right hand side vanishes, and so must the left
hand side, which implies φ ′ = 0 and hence no non-trivial
scalar profile exists.
Self-gravitating solitons with the coupling (24) and n = 3
where also obtained. They follow the same pattern as the
n = 3 case, which is therefore illustrative.
3.3 Perturbative solutions
The existence of a flat spacetime solution, whose total
mass-energy is proportional to 1/α, suggests that the selfgravitating solitons may be expressed as a perturbative series
in 1/α. Let us indeed show that the numerical solutions of
the previous subsection can be approximated by such perturbative solutions. This approximation, as we will show and as
one may anticipate, is accurate for sufficiently large α.

where q is a free parameter, whose physical significance
becomes transparent by computing the far field asymptotics
of the electric potential. One finds it is related to the electric
charge measured at infinity Q, as
Q=

q
.
α

(70)

The perturbative solution yields the following ADM mass
and scalar charge, valid to fourth order in perturbation theory:
)
(
1
1
Q
,
1−
+
M=
3α
30α 2
1080α 4
)
(
1
7
Q.
(71)
Qs = 1 −
+
18α 2
3240α 4
2 We have computed the solution up to eighth order and no obvious

pattern could be found. Here we display only the first few terms for
each function.

123

## PDF page 8

23 Page 8 of 9

Observe that the first terms in (71) reproduce the flat spacetime limit, Eq. (22) and the fact that the electric and scalar
charge coincide in that limit.
In Fig. 2 the perturbative solutions (71) are compared with
the numerical solutions. One can observe that the former provide a good approximation for large values of α; for instance,
for α = 10 the relative difference between the numerical
result for M(Q) and the theory one is around 10−4 . However, the differences start to increase for smaller α. This is
illustrated by the results for α = 0.2 in Fig. 2.
Finally let us mention that a similar solution has been
derived for the self-gravitating solitons with the coupling
(24) and n = 3. In this case one finds, e.g.
)
(
2
22
2Q
+ ...
(72)
1−
+
M=
5α
45α 2
14625α 4

4 Discussion
Recently, a set of theorems were shown [1] establishing that
the model (1) does not allow self-gravitating solitons. One of
the observations therein is that if the coupling would diverge
the theorems could, potentially, be circumvented. The purpose of this paper was to provide the mechanism how this
can happen providing a simple construction of flat spacetime
and gravitating solitons.
Preliminary analysis shows the solitons we have described
herein are stable against spherical perturbations. If this is the
case for generic perturbations, these solitons can be used for
dynamical studies in many setups, as, for instance, boson
stars [25,26]. Moreover, this construction reveals how to desingularise the Coulomb field in a classical field theory, without resorting to non-linear electrodynamics, as in the BornInfeld model [27], or invoking a manifestly extended object,
such as in the Dirac model of the electron as a spherical
membrane [28].
Finally, let us remark that there is a well known similarity between the EMS model and the extended scalar–
tensor-Gauss–Bonnet model, where black hole scalarisation
was first pointed out in [29–31]. Very recently, a family of
particle-like solutions in the latter model were discussed [32].
These particle like solutions are also supported by a divergent coupling making them the counterparts of the solutions
described herein. But in the cases reported in [32] the scalar
field also diverges at the origin, in contrast with our fully
regular solutions.
Acknowledgements J.O. is supported by the FCT Grant PD/BD/1281
84/2016. This work is supported by The Center for Research and
Development in Mathematics and Applications (CIDMA) and by
the Centre of Mathematics (CMAT) through the Portuguese Foundation for Science and Technology (FCT - Fundação para a Ciência e a Tecnologia), references UIDB/04106/2020, UIDP/04106/2020,
UIDB/00013/2020 and UIDP/00013/2020 and by national funds (OE),

123

Eur. Phys. J. C (2020) 80:23
through FCT, I.P., in the scope of the framework contract foreseen in
the numbers 4, 5 and 6 of the article 23, of the Decree-Law 57/2016,
of August 29, changed by Law 57/2017, of July 19. We acknowledge support from the project PTDC/FIS-OUT/28407/2017. This work
has further been supported by the European Union’s Horizon 2020
research and innovation (RISE) programmes H2020-MSCA-RISE2015 Grant no. StronGrHEP-690904 and H2020-MSCA-RISE-2017
Grant no. FunFiCO-777740. The authors would like to acknowledge
networking support by the COST Action CA16104.
Data Availability Statement This manuscript has no associated data
or the data will not be deposited. [Authors’ comment: There is no data
to be uploaded since this is a theoretical study.]
Open Access This article is licensed under a Creative Commons Attribution 4.0 International License, which permits use, sharing, adaptation,
distribution and reproduction in any medium or format, as long as you
give appropriate credit to the original author(s) and the source, provide a link to the Creative Commons licence, and indicate if changes
were made. The images or other third party material in this article
are included in the article’s Creative Commons licence, unless indicated otherwise in a credit line to the material. If material is not
included in the article’s Creative Commons licence and your intended
use is not permitted by statutory regulation or exceeds the permitted use, you will need to obtain permission directly from the copyright holder. To view a copy of this licence, visit http://creativecomm
ons.org/licenses/by/4.0/.
Funded by SCOAP3 .

References
1. C.A.R. Herdeiro, J.M.S. Oliveira, Class. Quantum Gravity 36(10),
105015 (2019). arXiv:1902.07721 [gr-qc]
2. T. Kaluza, Sitzungsber. Preuss. Akad. Wiss. Berlin (Math. Phys. )
1921, 966 (1921)
3. T. Kaluza, Int. J. Mod. Phys. D 27(14), 1870001 (2018).
arXiv:1803.08616 [physics.hist-ph]
4. O. Klein, Z. Phys. 37, 895 (1926)
5. O. Klein, Surv. High Energy Phys. 5, 241 (1986)
6. T. Appelquist, A. Chodos, P.G.O. Freund, Reading, USA: AddisonWesley (1987) 619 (Frontiers in physics, 65)
7. P. Van Nieuwenhuizen, Phys. Rep. 68, 189 (1981)
8. J. Martin, J. Yokoyama, JCAP 0801, 025 (2008). arXiv:0711.4307
[astro-ph]
9. A. Maleknejad, M.M. Sheikh-Jabbari, J. Soda, Phys. Rep. 528, 161
(2013). arXiv:1212.2921 [hep-th]
10. C.A.R. Herdeiro, E. Radu, N. Sanchis-Gual, J.A. Font, Phys. Rev.
Lett. 121(10), 101102 (2018). arXiv:1806.05190 [gr-qc]
11. P.G.S. Fernandes, C.A.R. Herdeiro, A.M. Pombo, E. Radu, N.
Sanchis-Gual, Class. Quantum Gravity 36(13), 134002 (2019).
arXiv:1902.05079 [gr-qc]
12. D. Astefanesei, C. Herdeiro, A. Pombo, E. Radu, JHEP 10, 78
(2019). arXiv:1905.08304 [hep-th]
13. Y.S. Myung, D.C. Zou, Eur. Phys. J. C 79(3), 273 (2019).
arXiv:1808.02609 [gr-qc]
14. Y.S. Myung, D.C. Zou, Phys. Lett. B 790, 400 (2019).
arXiv:1812.03604 [gr-qc]
15. Y.S. Myung, D.C. Zou, Eur. Phys. J. C 79(8), 641 (2019).
arXiv:1904.09864 [gr-qc]
16. R.A. Konoplya, A. Zhidenko, Phys. Rev. D 100(4), 044015 (2019).
arXiv:1907.05551 [gr-qc]
17. P.G.S. Fernandes, C.A.R. Herdeiro, A.M. Pombo, E. Radu, N.
Sanchis-Gual, Phys. Rev. D 100, 084045 (2019). arXiv:1908.00037
[gr-qc]

## PDF page 9

Eur. Phys. J. C (2020) 80:23
18. M. Boskovic, R. Brito, V. Cardoso, T. Ikeda, H. Witek, Phys. Rev.
D 99, 035006 (2019). arXiv:1811.04945 [gr-qc]
19. M. Minamitsuji, T. Ikeda, Phys. Rev. D 99, 04401 (2019).
arXiv:1812.03551 [gr-qc]
20. H.O. Silva, C.F.B. Macedo, T.P. Sotiriou, L. Gualtieri, J. Sakstein,
E. Berti, Phys. Rev. D 99, 064011 (2019). arXiv:1812.05590 [grqc]
21. C.A.R. Herdeiro, E. Radu, Phys. Rev. D 99(8), 084039 (2019).
arXiv:1901.02953 [gr-qc]
22. M.E. Peskin, D.V. Schroeder, An Introduction to Quantum Field
Theory (Taylor & Francis Inc., New York, 1995)
23. G.H. Derrick, J. Math. Phys. 5, 1252 (1964)
24. G.W. Gibbons, Lect. Notes Phys. 383, 110 (1991).
arXiv:1109.3538 [gr-qc]
25. S.L. Liebling, C. Palenzuela, Living Rev. Relativ. 15, 6 (2012)
26. S.L. Liebling, C. Palenzuela, Living Rev. Relativ. 20(1), 5 (2017).
arXiv:1202.5809 [gr-qc]

Page 9 of 9 23
27. M. Born, L. Infeld, Proc. R. Soc. Lond. A 144(852), 425 (1934)
28. P.A.M. Dirac, Proc. R. Soc. Lond. A 268, 57 (1962)
29. D.D. Doneva, S.S. Yazadjiev, Phys. Rev. Lett. 120(13), 131103
(2018). arXiv:1711.01187 [gr-qc]
30. H.O. Silva, J. Sakstein, L. Gualtieri, T.P. Sotiriou, E. Berti, Phys.
Rev. Lett. 120(13), 131104 (2018). arXiv:1711.02080 [gr-qc]
31. G. Antoniou, A. Bakopoulos, P. Kanti, Phys. Rev. Lett. 120(13),
131102 (2018). arXiv:1711.03390 [hep-th]
32. B. Kleihaus, J. Kunz, P. Kanti, arXiv:1910.02121 [gr-qc]

123
