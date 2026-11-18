Source: see manifest row of the PDF
PDF sha256: 69b81d42f641bad3cfd274cdd465df8041b6f88303ffcc11cd57b28973ccde43
License: CC-BY-4.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of buchel_2018_ringing_in_de_sitter_spacetime.pdf

Transcription of `buchel_2018_ringing_in_de_sitter_spacetime.pdf` in this directory, 14 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-14 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Available online at www.sciencedirect.com

ScienceDirect
Nuclear Physics B 928 (2018) 307–320
www.elsevier.com/locate/nuclphysb

Ringing in de Sitter spacetime
Alex Buchel a,b,∗
a Department of Applied Mathematics, Department of Physics and Astronomy, University of Western Ontario, London,

Ontario N6A 5B7, Canada
b Perimeter Institute for Theoretical Physics, Waterloo, Ontario N2J 2W9, Canada

Received 8 July 2017; accepted 20 January 2018
Editor: Leonardo Rastelli

Abstract
Hydrodynamics is a universal effective theory describing relaxation of quantum field theories towards
equilibrium. Massive QFTs in de Sitter spacetime are never at equilibrium. We use holographic gauge
theory/gravity correspondence to describe relaxation of a QFT to its Bunch–Davies vacuum — an attractor
of its late-time dynamics. Specifically, we compute the analogue of the quasinormal modes describing the
relaxation of a holographic toy model QFT in de Sitter.
© 2018 The Author(s). Published by Elsevier B.V. This is an open access article under the CC BY license
(http://creativecommons.org/licenses/by/4.0/). Funded by SCOAP3 .

1. Introduction
Isolated strongly interacting systems typically1 reach a thermal equilibrium state at late times
of its dynamical evolution. An approach towards equilibrium is governed by hydrodynamics —
a universal effective theory organized as derivative expansion of the local velocity gradients to
the temperature of the final equilibrium state. One example is the relativistic hydrodynamics
of conformal gauge theories developed in [3,4]. As an effective description, gradient expansion
of the gauge theory hydrodynamics has zero radius of convergence due to the existence of the
* Correspondence to: Department of Applied Mathematics, Department of Physics and Astronomy, University of
Western Ontario, London, Ontario N6A 5B7, Canada.
E-mail address: abuchel@uwo.ca.
1 There are some exceptions to this lore: condensed matter systems with many-body localization [1]; holographic
models with phase-space restricted dynamics [2].

https://doi.org/10.1016/j.nuclphysb.2018.01.021
0550-3213/© 2018 The Author(s). Published by Elsevier B.V. This is an open access article under the CC BY license
(http://creativecommons.org/licenses/by/4.0/). Funded by SCOAP3 .

## PDF page 2

308

A. Buchel / Nuclear Physics B 928 (2018) 307–320

non-hydrodynamic modes in equilibrium plasma [5,6]. Whenever gauge theory allows for a dual
holographic description [7,8] in terms of classical supergravity, its thermal equilibrium state is
represented by a black hole/black brane in the gravitational dual [9]. Furthermore, linearized
hydrodynamic and non-hydrodynamic excitations about the equilibrium state are mapped to the
quasinormal modes (QNMs) of the corresponding dual black hole [10]. QNMs encode the information about the relaxation of the near-equilibrium state of a gauge theory plasma [11–14].
Implicit in the above overview was an assumption that QFT dynamics occurs in Minkowski
spacetime. Using holographic correspondence,2 it was argued in [21,22] that massive gauge theories in de Sitter spacetime are not in equilibrium at late times: while Bunch–Davies (BD) vacuum
is the late-time attractor of a dynamical evolution of a QFT state, the co-moving entropy production rate is nonzero. In this paper we make the first step addressing the question:
What is the effective theory of the relaxation towards Bunch–Davies vacuum of a massive
QFT?
We restrict our attention to a simple holographic toy model of a 2 + 1-dimensional massive
QF T3 with the effective dual gravitational action3 :
[
]
∫
√
1
1
S4 = 2
dx 4 −γ R + 6 − (∇φ)2 + φ 2 .
(1.1)
2
2κ
M4

The four dimensional gravitational constant κ is related to the ultraviolet (UV) conformal fixed
point CF T3 central charge c as
192
.
κ2
φ is a gravitational bulk scalar with
c=

(1.2)

L2 m2φ = −2 ,

(1.3)

which is dual to a dimension φ = 2 operator Oφ of the boundary theory. QF T3 is a relevant
deformation of the UV CF T3 with
HCF T → HQF T = HCF T +  Oφ ,

(1.4)

with  being the deformation mass scale. We study QF T3 dynamics in de Sitter spacetime with
a Hubble constant H ; thus the metric on M4 boundary, ds∂2M4 , is taken as
(
)
ds∂2M4 = −dt 2 + e2H t dx12 + dx22 .
(1.5)
Following [21], in the next section we describe gravitational dynamical setup encoding de Sitter
evolution of spatially homogeneous and isotropic states of the boundary field theory. We study
the late-time attractor of the evolution in section 2.1. In section 2.2 we compute the spectrum
of linearized fluctuations of the boundary theory around its BD vacuum. In section 2.3 we use
fully nonlinear characteristic formulation of asymptotically AdS dynamics [23] and establish
that generic homogeneous and isotropic states of the boundary theory indeed “ring-down” to BD
vacuum with frequencies computed in section 2.2. We conclude in section 3.
2 For early work on gauge theories in de Sitter within holographic framework see [15–20].
3 We set the radius L of an asymptotic AdS geometry to unity.
4

## PDF page 3

A. Buchel / Nuclear Physics B 928 (2018) 307–320

309

2. Holographic gravitational dynamics
A generic state of the boundary field theory with a gravitational dual (1.1), homogeneous and
isotropic in the spatial boundary coordinates x = {x1 , x2 }, leads to a bulk gravitational metric
ansatz
ds42 = 2dt (dr − Adt) + 2 dx 2 ,

(2.1)

with the warp factors A,  as well as the bulk scalar φ depending only on {t, r}. From the
effective action (1.1) we obtain the following equations of motion:
3
1
′
0 = d+
 + d+  (ln )′ −  − φ 2 ,
2
4
d+  ′
′
′
φ +φ ,
0 = d+ φ + d+ φ (ln ) +

d+ 
1
0 = A′′ − 2 2 ′ + d+ φ φ ′ ,
2

as well as the Hamiltonian constraint equation:

(2.2)

1
0 = ′′ + (φ ′ )2 ,
4
and the momentum constraint equation:
(
)′ 1 (
))
d+  (
2
′
0 = d+
 − 2Ad+
 − 2 A2 +  (d+ φ)2 + 2A 6 + φ 2 .
4


(2.3)

(2.4)

∂
∂
In (2.2)–(2.4) we denoted ′ = ∂r
, ˙ = ∂t∂ , and d+ = ∂t∂ + A ∂r
. The near-boundary r → ∞
asymptotic behavior of the metric functions and the scalar encode the mass parameter  and
the boundary metric scale factor a(t) ≡ eH t :

(
)
 = a r + λ + O(r −1 ) ,

A=

(
)
r2
ȧ
+ λ−
r + O(r 0 ) ,
2
a

φ=


+ O(r −2 ) .
r
(2.5)

λ = λ(t) in (2.5) is the residual radial coordinate diffeomorphism parameter [23]. An initial
state of the boundary field theory is specified providing the scalar profile φ(0, r) and solving the
constraint (2.3), subject to the boundary conditions (2.5). Equations (2.2) can then be used to
evolve the state.
The subleading terms in the boundary expansion of the metric functions and the scalar encode
the evolution of the energy density E(t), the pressure P (t) and the expectation values of the operator Oφ (t) of the prescribed boundary QFT initial state. Specifically, extending the asymptotic
expansion (2.5) for {φ, A},
( )
 f2 (t)
1
φ = + 2 +O 3 ,
r
r
r
(
)
(
)
( )
2
r2
ȧ
λ2 2 ȧ
1

1
A=
+ λ−
r+
−
− λ − λ̇ +
μ(t) − f2 (t) −
λ +O 2 ,
2
a
2
8
a
r
4
4
r
(2.6)

## PDF page 4

310

A. Buchel / Nuclear Physics B 928 (2018) 307–320

the observables of interest can be computed following the holographic renormalization of the
model:
(
)
ȧ
(ȧ)2
2κ 2 E(t) = −4μ + 2 + δ1 3 + 2δ2  2 ,
(2.7)
a
a
(
)
1
ä
,
(2.8)
2κ 2 P (t) = −2μ + (f2 + λ) + −δ1 3 − 2δ2 
2
a
(
(
))
ȧ
(ȧ)2
ä
2
2
,
(2.9)
2κ Oφ (t) = −f2 − λ +  + 3δ1  + δ2 4 + 2 2
a
a
a
where the terms in brackets, depending on arbitrary constants {δ1 , δ2 }, encode the renormalization scheme ambiguities. Independent of the renormalization scheme, these expectation values
satisfy the expected conformal Ward identity
−E + 2P = −Oφ .

(2.10)

Furthermore, the conservation of the stress-energy tensor
dE
ȧ
+ 2 (E + P ) = 0 ,
dt
a
is a consequence of the momentum constraint (2.4):
(
( (
)
)
)
ȧ
1
ȧ
ä
2 ȧ
0 = μ̇ +
3μ − f2 −
λ+
+
.
a
4
4 a
a
a

(2.11)

(2.12)

From now on we choose a scheme with δi = 0.
One of the advantages of the holographic formulation of a QFT dynamics is the natural definition of its far-from-equilibrium entropy density. A gravitational geometry (2.1) has an apparent
horizon located at r = rAH , where [23]
∣
∣
d+ ∣∣
= 0.
(2.13)
r=rAH

Following [24,25] we associate the non-equilibrium entropy density s of the boundary QFT with
the Bekenstein–Hawking entropy density of the apparent horizon
∣
∣
2π
a 2 s = 2 2 ∣∣
.
(2.14)
κ
r=rAH
Using the holographic background equations of motion (2.2)–(2.4) we find
∣
2∣
d(a 2 s) 2π
2 ′ (d+ φ) ∣
.
= 2 ( ) 2
dt
κ
φ + 6 ∣r=rAH

(2.15)

Following [21] it is easy to prove that the entropy production rate as defined by (2.15) is nonnegative, i.e.,
d(a 2 s)
≥ 0,
(2.16)
dt
in holographic dynamics governed by (2.2)–(2.4).
The holographic evolution as explained above is implemented in section 2.3, adopting numerical codes developed in [26,27].

## PDF page 5

A. Buchel / Nuclear Physics B 928 (2018) 307–320

311

2.1. Bunch–Davies vacua of holographic toy QF T3
Following [21], the equations for the late-time attractor of the evolution (a Bunch–Davies
vacuum [21]) can be obtained from (2.2)–(2.4) taking t → ∞ limit with identification
lim {φ, A}(t, r) = {φ, A}v ,

t→∞

lim

t→∞

(t, r)
= σv (r) .
a(t)

(2.17)

Introducing a new radial coordinate
H
,
r
and denoting
x≡

φv = p(x) ,

(2.18)

Av =

H2
g(x) ,
2x 2

σv =

H
f (x) ,
x

(2.19)

we find
1
0 = f ′′ + (p ′ )2 f ,
4
(
)−1 (
′′
2
′ 2
2
2f 2 x 4 (p ′ )3 − f 2 p(p ′ )2 x 2
0 = p + (fp + 12f x − 12xf + 6f )f x

(2.20)

+ (24x 4 (f ′ )2 + 4f x 2 (p 2 − 6x + 6)f ′ − 2f 2 x(p 2 + 6))p ′
)
+ 12p((f ′ )2 x 2 − 2f xf ′ + f 2 ) ,
along with an algebraic expression for g:
g=−

2f (fp 2 + 12f ′ x 2 − 12xf + 6f )
.
f 2 (p ′ )2 x 2 − 12(f ′ )2 x 2 + 24xff ′ − 12f 2

(2.21)

Vacuum solution has to satisfy the boundary conditions (2.5), and remain nonsingular for x ∈
(0, xAH ], where the location of the apparent horizon xAH is determined from [21]
(
)∣
′
d+ (t, xAH ) = 0
⇐⇒
f (x) (2x + g(x)) − g(x)f (x) ∣∣
= 0.
(2.22)
x=xAH

Without loss of generality we fix the diffeomorphism parameter λ so that
∣
∣
Av (x)∣∣
= 0.

(2.23)

x= 13

We will always have xAH > 13 .
It is straightforward to construct an analytic solution to (2.20) as a series expansion in conformal symmetry breaking parameter
p1 ≡


,
H

p = p1

( )
x
x 2 (2x − 1) 3 x 2 (875x 3 − 647x 2 + 9x + 51) 5
p1 −
p1 + O p17 ,
−
3
5
1−x
9(x − 1)
12960(x − 1)

(2.24)
(2.25)

## PDF page 6

312

A. Buchel / Nuclear Physics B 928 (2018) 307–320

Fig. 1. Vacuum energy density Ev of the holographic toy model as a function of the conformal symmetry breaking
 (solid black line). Dashed red line indicates perturbative prediction, see (2.29). c is the UV central
deformation p1 = H
charge of the model (see (1.2)).

x(4x − 1) 2 x(4x − 1)(23x 2 − 5x − 5) 4
p1
p +
24(x − 1) 1
3456(x − 1)3
( )
x(49618x 5 − 46133x 4 + 9055x 3 − 2745x 2 + 3225x − 645) 6
+
p
+
O
p18 ,
1
6220800(x − 1)5

f =1−x +

which determines following (2.21)
(
x(3x − 1) 2 (3x − 1)(19x 2 − 2x − 5)x 4
g = (1 − 3x) 1 − x +
p1
p +
12(x − 1) 1
1728(x − 1)3
( ))
x(3x − 1)(1937x 4 − 1196x 3 + 54x 2 − 204x + 129) 6
+
p1 + O p18 .
622080(x − 1)5

(2.26)

(2.27)

From (2.22), the apparent horizon is located at
1
1
1
20401 2/3 8/3
2/3
4/3
xAH =1 − 62/3 p1 + 61/3 p1 + p12 −
6 p1
6
12
9
622080
(2.28)
(
)
685273 1/3 10/3 40841057 4
14/3
−
6 p1 +
p + O p1
.
12441600
99532800 1
For generic p1 we have to resort numerics. Details of the numerical implementation are explained in [21]. Fig. 1 presents the vacuum energy Ev as a function of p1 in renormalization
scheme δi = 0. Using perturbative solution (2.25), (2.26) we find
( )
Ev
1
5
43
2κ 2 3 = p12 +
p14 −
p16 + O p18 .
(2.29)
H
3
216
51840
Note that in vacuum Pv = −Ev , thus following (2.10),
Ev
.
(2.30)

In [22] it was argued that the vacuum of a massive QFT in de Sitter has a constant “entanglement” entropy density sent , related to the comoving entropy production rate R at late times.
Specifically, parameterizing the comoving entropy production from (2.15) as
Oφ,v = 3

## PDF page 7

A. Buchel / Nuclear Physics B 928 (2018) 307–320

313

Fig. 2. Vacuum entropy density sent of the holographic toy model (see (2.32)) as a function of the conformal symmetry
 . Dashed red line indicates perturbative prediction, see (2.33). c is the UV central charge
breaking deformation p1 = H
of the model (see (1.2)).

1 d ( 2 )
a s ≡ 2H × R ,
t→∞ H 2 a 2 dt
the vacuum entropy density sent is
lim

sent ≡ lim s = H 2 R .
t→∞

(2.31)

(2.32)

Fig. 2 presents the vacuum entropy density as a function of p1 — this result is renormalization
scheme independent. Perturbatively,
( )
κ 2 sent
1
1 2
5 2/3 8/3
3359 1/3 10/3
4/3
= 61/3 p1 −
p1 −
6 p1 −
6 p1 + O p14 . (2.33)
2
2π H
6
12
216
311040
Following [22], the surface gravity of the apparent horizon equals (−H ).
2.2. Spectrum of vacuum linearized fluctuations
For static horizons in holography, quasinormal modes of black holes/black branes represent
the physical linearized fluctuations in the dual boundary field theory plasma at equilibrium. In
Fefferman–Graham coordinate of the asymptotically AdS bulk geometry the spectrum of QNMs
is determined solving Sturm–Liouville problem for the linearized fluctuations with Dirichlet conditions at the asymptotic boundary for the non-normalizable modes of the fluctuating fields, and
incoming boundary condition at the horizon [28]. In case of infalling Eddington–Finkelstein
coordinates (as in (2.1)), the horizon boundary condition is replaced with the regularity at the
trapped surface (the apparent horizon). We stress again that it is the boundary conditions at the
horizon and the asymptotic boundary that determine the spectrum of fluctuations.
In analogy to QNMs, we consider linearized fluctuations of the system (2.2)–(2.4) about the
late-time attractor solution (2.17). To this end, we define the fluctuations with the harmonic time
dependence of frequency ω as follows:
)
(t, x) H (
φ(t, x) = p(x) + δ H1 (x) e−iωt ,
=
f (x) + δ H2 (x) e−iωt ,
a(t)
x
(2.34)
(
)
2
H
−iωt
A(t, x) = 2 g(x) + δ H3 (x) e
,
2x

## PDF page 8

314

A. Buchel / Nuclear Physics B 928 (2018) 307–320

where δ is the amplitude of the fluctuations. Substituting (2.34) into (2.2)–(2.4) and collecting
O(δ) terms we obtain4 a consistent set of coupled radial equations of motion for Hi :
0 = H1′′ + C1,1 H1′ + C1,2 H1 + C1,3 H2 + C1,4 H3 ,
0 = H2′ + C2,1 H1′ + C2,2 H1 + C2,3 H2 + C2,4 H3 ,

(2.35)

0 = H3′ + C3,1 H1′ + C3,2 H1 + C3,3 H2 + C3,4 H3 ,
where the connection coefficients
]
[
′
′
Ci,j = Ci,j f (x), p (x); f (x), p(x); x; ω̂

(2.36)

are functionals of vacuum functions {f, p} (see (2.20)) and the reduced frequency
ω̂ ≡

ω
.
H

(2.37)

As in case of the QNMs, we insist that the linearized fluctuations Hi do not change boundary
QFT data, i.e., we require
H1 = x 2 + O(x 3 ) ,

H2 = O(x) ,

H3 = O(x) ,

(2.38)

as x → 0 (the asymptotic AdS boundary). The O(x 2 ) term in the H1 asymptotic is simply the definition of the amplitude of the linearized fluctuations. Recall [21] that the vacuum
equations of motion have a coordinate singularity5 when Av (x = xsingularity ) = 0. In our
case xsingularity = 13 , see (2.23). This coordinate singularity occurs always before the apparent horizon: xAH > xsingularity . Turns out that the connection coefficients Ci,j are singular at
xsingualarity , and requiring that this is just a coordinate singularity and the fluctuating fields Hi
are smooth across this point and extend all the way to the apparent horizon xAH , provides the
second boundary condition on the spectrum of fluctuations.
To recap: the spectrum of linearized fluctuations about Bunch–Davies vacuum is determined
from:
• Dirichlet conditions at the AdS boundary on the non-normalizable modes of the dual gravitational bulk fluctuating fields;
• regularity condition for bulk fluctuating fields at the location Av = 0.
It is instructive to solve (2.36) perturbatively in the conformal deformation parameter p1 ,
using perturbative expansion for the BD vacuum (2.25)–(2.26). Introducing
Hi (x) =

∞
∑

p1k Hi,k (x) ,

k=0

ω̂ =

∞
∑

p1k ω̂k ,

(2.39)

k=0

to leading order k = 0 we find:
4 Explicit form of (2.36) is provided as a separate file with the arXiv.org submission of this paper.
5 There is no coordinate singularity in the radial coordinate in the characteristic formulation of the dynamical evolution
implemented in section 2.3.

## PDF page 9

A. Buchel / Nuclear Physics B 928 (2018) 307–320

2i(3ix 2 − ω̂0 x − i) ′
2i(ix − ω̂0 x − i)
H1,0 ,
H −
x(x − 1)(3x − 1) 1,0 (3x − 1)(x − 1)2 x 2
i(2ix − i + ω̂0 )
1
′
0 = H2,0
+
H2,0 −
H3,0 ,
(x − 1)(2x − 1)
2x(x − 1)(2x − 1)
2ω̂0 x(ω̂0 + i)
i(4ix 2 − 5ix − ω̂0 x + i)
′
0 = H3,0
−
H2,0 +
H3,0 .
(x − 1)(2x − 1)
x(x − 1)(2x − 1)

315

′′
0 = H1,0
−

(2.40)

Note that to leading order in p1 equations for H1 and {H2 , H3 } decouple. The general solution
of the first equation in (2.41), subject to (2.38), is
(
⎧
)−1+i ω̂0 )
(
x
1−3x
⎨ −
1
−
,
ω̂0 ̸= −i
1−x
2(1−x)(1−i ω̂0 )
H1,0 =
(2.41)
⎩
x
− 2(1−x)
ln 1−3x
,
ω̂
=
−i
.
0
1−x
Requiring that H1,0 is analytic at x = xsingularity = 13 produces the spectrum of fluctuations to
leading order in p1 :
ω̂ ≡ ω̂(n) = −in + O(p1 ) ,

n = 2, 3, · · ·

(2.42)

Note that in a conformal limit p1 → 0 the mode (2.41) disappears from the spectrum — all
2/3
(n)-modes are singular at x = xAH = 1 + O(p1 ). We interpreted this fact as a statement that the
Bunch–Davies vacuum of a CFT does not ring. It is straightforward to check that the remaining
two equations in (2.41) do not lead to new spectral branches.6
The leading order solution (2.42) can be extended to higher orders in O(p1 ). For example, for
n = 2 mode we find:
(
( ))
1 2
1 4
1591
(2)
6
ω̂ = −i 2 +
p −
p +
p + O p18
,
12 1 54 1 622080 1
x2
x 3 (19x − 6) 2 x 3 (6768x 3 − 3125x 2 − 950x + 535) 4
(2)
+
p +
p1
H1 =
2
(1 − x)
36(x − 1)4 1
25920(x − 1)6
x 3 (17864583x 5 − 14152740x 4 + 1089102x 3 − 157220x 2 + 1292795x − 409080) 6
+
p1
130636800(x − 1)8
( )
+ O p18 ,
(2)

H2 = −
−

x(13x 2 − 2x + 1)
x(2867x 4 − 1644x 3 + 646x 2 − 444x + 111) 3
p
−
p1
1
72(x − 1)2
34560(x − 1)4

x(17822851x 6 − 8946582x 5 − 7415409x 4 + 8763460x 3 − 5161395x 2 + 2036586x − 339431) 5
p1
522547200(x − 1)6
( )

+ O p17 ,

(

(2)
H3 = (3x − 1)

+

(4x 2 + x + 1)x
(1036x 4 + 95x 3 − 447x 2 − 51x + 111)x 3
p
+
p1
1
36(x − 1)2
17280(x − 1)4

(8634226x 6 − 6320265x 5 + 1435341x 4 − 731078x 3 − 568056x 2 + 1083183x − 339431)x 5
p1
261273600(x − 1)6
)

( )
+ O p17 ,

(2.43)
6 This is also confirmed comparing with the relaxation to BD vacuum in the full nonlinear dynamics as explained in
section 2.3.

## PDF page 10

316

A. Buchel / Nuclear Physics B 928 (2018) 307–320

Fig. 3. Spectra of BD vacuum fluctuations for several low-lying modes n = 2, 3, 4, 5. Red dashed lines indicate pertur.
bative predictions perturbative in conformal symmetry breaking parameter p1 = H

where we fixed the diffeomorphism parameter λ(t) to all orders in p1 requiring that A(t, x =
1
3 ) = 0. Note that n = 2 mode is purely dissipative. In fact, we find that all modes except for
n = 3 are purely dissipative. For example,
(
( ))
1
337
ω̂(4) = −i 4 −
p14 +
p16 + O p18
,
216
777600
(
( ))
5
589
p14 −
p16 + O p18
,
ω̂(5) = −i 5 −
4096
15925248

(2.44)

while
1√
11i 2
37 √ 3
1855i 4
2076503 √ 5
2 p1 −
2 p1 −
2 p1
p1 +
p1 −
4
192
12288
221184
1132462080
( )
1240993i
+
p16 + O p17 .
1061683200
(2.45)

ω̂(3) = −3i +

What makes the mode n = 3 special is the fact that the connection coefficients Ci,j in (2.36) have
a simple pole at ω̂ = −3i. Unfortunately, we do not understand the physical reason for this.
For general p1 the spectrum of fluctuations can be computed numerically. These results are
presented in Fig. 3 for n = {2, 3, 4, 5} modes. The dashed red lines indicate perturbative approximation (2.43), (2.44) and (2.45). In what follows to refer to the fluctuations in BD vacuum as
QNMs.
Although the spectrum is determined solving (2.36) on the radial interval x ∈ (0, xsingularity ),
we verified that the solution can indeed be smoothly extended to the full interval x ∈ (0, xAH ).
(2)
For example, the radial profile H1 (x) at p1 = 1 is presented in Fig. 4.
2.3. Fully nonlinear dynamics and relaxation to BD vacuum
In this section we report results of the fully nonlinear evolution of the toy holographic QFT
defined by a dual gravitational action (1.1). Numerical implementation parallel the codes developed in [26,27], and will not be discussed here.

## PDF page 11

A. Buchel / Nuclear Physics B 928 (2018) 307–320

317

(2)

Fig. 4. Fluctuation profile H1 at p1 = 1 as a function of x > xsingularity . The vertical green line indicates the location
of the apparent horizon, see (2.22). The dashed red line is the perturbative prediction (2.43).

In what follows we focus on the model7 with p1 = 1. We use the radial coordinate as in (2.18)
and evolve in dimensionless time τ ≡ H t . As in [23] we adjust the diffeomorphism parameter λ(t) so that the apparent horizon is always at xAH = 1. We set the initial condition for the
evolution as
φ(0, x) = φinitial (x) = p1 x + A x 2 e−x ,

(2.46)

where A is the amplitude. We also need to supply the initial energy density (see (2.12))
μ(0) ≡ μinitial .

(2.47)

We verified that BD vacuum is indeed the attractor of long-time dynamics by choosing different
initial states for the evolution, i.e., different profiles φinitial and/or μinitial .
Fig. 5 represent a typical dynamical evolution of the boundary QFT state from the initial
condition (2.46). As times τ = H t ≳ 2 the state relaxes to BD vacuum. The relaxation process is
studied in further details as follows.
■ We use the last 1000 data points, corresponding to time interval τ ∈ [5.6, 6] and fit the observed
Oφ (τ ) with a single QNM ansatz:
Oφ = α1 + α2 e−iα3 τ ,
f it

(2.48)

where αi are constant free parameters. α1 is expected to agree with the BD expectation value and
α3 should approximate the frequency of the lowest BD QNM mode, i.e., n = 2. We find that the
BD vacuum expectation value is correct with a relative error of ∼ 3 × 10−6 and the relative error
in the frequency,
∣
∣
∣
∣
∣1 − α3 ∣ = 2.7 × 10−3 ,
(2.49)
∣
(2)
ω̂ ∣
is in excellent agreement with the result in section 2.2.
■ To check on the spectrum of higher QNMs computed in section 2.2 we restrict to 1000 data
points in the intermediate time-range, τ ∈ [4, 4.4]. We compute residual δ defined as
∣
∣
QNM
(τ ) ∣
Oφ
∣
∣
∣,
δ(τ ) ≡ ∣1 −
(2.50)
Oφ (τ ) ∣
7 The discussion is generic for the parameter set with stable and convergent evolution of the code.

## PDF page 12

318

A. Buchel / Nuclear Physics B 928 (2018) 307–320

Fig. 5. Fully nonlinear dynamical evolution of the initial boundary QFT state (2.46) (the solid black curve) as a function
of τ = H t . The red line represents the late-time asymptotic value of the operator Oφ computed in BD vacuum in
section 2.1. (For interpretation of the references to color in this figure legend, the reader is referred to the web version of
this article.)

Fig. 6. Relaxation to BD vacuum via the QNMs computed in section 2.2. The residuals δ are computed with the best fit
QN M
Oφ
to the evolution data using a constant and: a single n = 2 mode (blue curve); two modes n = 2, 3 (red curve); 3
modes n = 2, 3, 4 (green curve). (For interpretation of the references to color in this figure legend, the reader is referred
to the web version of this article.)

QNM

where Oφ
(τ ) is the best QNM approximation to the data in the time subinterval with constant
free fit parameters αi and frequencies ω̂(n) computed in section 2.2:
n=2:
n = 2, 3 :
n = 2, 3, 4 :

QNM

Oφ

= α1 + α2 e−i ω̂

(2) τ

,

(2)
(3)
QNM
= α1 + α2 e−i ω̂ τ + α3 eIm[ω̂ ]τ cos[Re[ω̂(3) ]τ + α4 ] ,
Oφ

QNM

Oφ

= α1 + α2 e−i ω̂

(2) τ

+ α5 e−i ω̂

.

(4) τ

+ α3 eIm[ω̂

(3) ]τ

cos[Re[ω̂(3) ]τ + α4 ]

(2.51)

The residual δ is presented in Fig. 6. The quality of approximation suggests that the QNMs
computed in section 2.2 are all the modes defining the relaxation of the theory to its BD vacuum.

## PDF page 13

A. Buchel / Nuclear Physics B 928 (2018) 307–320

319

3. Conclusion
A surprising fact discovered in [21,22] is that a vacuum of a massive QFT in de Sitter space–
time has a constant entropy density sent . We stress that it is important that both the Hubble
constant is nonzero, and that the theory is non-conformal. For example, in a simple 2 + 1 dimensional holographic toy model discussed here

≪ 1,
(3.1)
H
where c is a UV central charge of the model and  is a mass scale of the theory.
Thermal equilibrium states have entropy. (Non)-hydrodynamic modes in equilibrium plasma
owe their existence to this entropy — no entropy, nothing to excite. By analogy, the nonvanishing
vacuum entropy of a massive QFT in de Sitter suggests that there should be analogous QNM-like
excitations about its Bunch–Davies vacuum. In this paper we showed that this is indeed the case.
sent ∼ c 4/3 H 2/3 ,

Acknowledgements
Research at Perimeter Institute is supported by the Government of Canada through Industry
Canada and by the Province of Ontario through the Ministry of Research & Innovation. This
work was further supported by NSERC through the Discovery Grants program.
References
[1] R. Nandkishore, D.A. Huse, Many-body localization and thermalization in quantum statistical mechanics, Annu.
Rev. Condens. Matter Phys. 6 (1) (2015) 15.
[2] V. Balasubramanian, A. Buchel, S.R. Green, L. Lehner, S.L. Liebling, Holographic thermalization, stability of antide Sitter space, and the Fermi–Pasta–Ulam paradox, Phys. Rev. Lett. 113 (7) (2014) 071601, https://doi.org/10.1103/
PhysRevLett.113.071601, arXiv:1403.6471 [hep-th].
[3] R. Baier, P. Romatschke, D.T. Son, A.O. Starinets, M.A. Stephanov, Relativistic viscous hydrodynamics, conformal
invariance, and holography, J. High Energy Phys. 0804 (2008) 100, https://doi.org/10.1088/1126-6708/2008/04/100,
arXiv:0712.2451 [hep-th].
[4] S. Bhattacharyya, V.E. Hubeny, S. Minwalla, M. Rangamani, Nonlinear fluid dynamics from gravity, J. High Energy
Phys. 0802 (2008) 045, https://doi.org/10.1088/1126-6708/2008/02/045, arXiv:0712.2456 [hep-th].
[5] M.P. Heller, R.A. Janik, P. Witaszczyk, Hydrodynamic gradient expansion in Gauge theory plasmas, Phys. Rev.
Lett. 110 (21) (2013) 211602, https://doi.org/10.1103/PhysRevLett.110.211602, arXiv:1302.0697 [hep-th].
[6] A. Buchel, M.P. Heller, J. Noronha, Entropy production, hydrodynamics, and resurgence in the primordial quark–
gluon plasma from holography, Phys. Rev. D 94 (10) (2016) 106011, https://doi.org/10.1103/PhysRevD.94.106011,
arXiv:1603.05344 [hep-th].
[7] J.M. Maldacena, The large N limit of superconformal field theories and supergravity, Adv. Theor. Math. Phys. 2
(1998) 231;
J.M. Maldacena, Int. J. Theor. Phys. 38 (1999) 1113, arXiv:hep-th/9711200.
[8] O. Aharony, S.S. Gubser, J.M. Maldacena, H. Ooguri, Y. Oz, Large N field theories, string theory and gravity, Phys.
Rep. 323 (2000) 183, arXiv:hep-th/9905111.
[9] E. Witten, Anti-de Sitter space, thermal phase transition, and confinement in gauge theories, Adv. Theor. Math.
Phys. 2 (1998) 505, arXiv:hep-th/9803131.
[10] E. Berti, V. Cardoso, A.O. Starinets, Quasinormal modes of black holes and black branes, Class. Quantum Gravity
26 (2009) 163001, https://doi.org/10.1088/0264-9381/26/16/163001, arXiv:0905.2975 [gr-qc].
[11] A. Buchel, M.P. Heller, R.C. Myers, Equilibration rates in a strongly coupled nonconformal quark–gluon plasma,
Phys. Rev. Lett. 114 (25) (2015) 251601, https://doi.org/10.1103/PhysRevLett.114.251601, arXiv:1503.07114 [hepth].
[12] J.F. Fuini, L.G. Yaffe, Far-from-equilibrium dynamics of a strongly coupled non-Abelian plasma with nonzero charge density or external magnetic field, J. High Energy Phys. 1507 (2015) 116, https://doi.org/10.1007/
JHEP07(2015)116, arXiv:1503.07148 [hep-th].

## PDF page 14

320

A. Buchel / Nuclear Physics B 928 (2018) 307–320

[13] R.A. Janik, G. Plewa, H. Soltanpanahi, M. Spalinski, Linearized nonequilibrium dynamics in nonconformal plasma,
Phys. Rev. D 91 (12) (2015) 126013, https://doi.org/10.1103/PhysRevD.91.126013, arXiv:1503.07149 [hep-th].
[14] A. Buchel, A. Day, Universal relaxation in quark–gluon plasma at strong coupling, Phys. Rev. D 92 (2) (2015)
026009, https://doi.org/10.1103/PhysRevD.92.026009, arXiv:1505.05012 [hep-th].
[15] A. Buchel, Gauge/gravity correspondence in accelerating universe, Phys. Rev. D 65 (2002) 125015, https://doi.org/
10.1103/PhysRevD.65.125015, arXiv:hep-th/0203041.
[16] A. Buchel, P. Langfelder, J. Walcher, On time dependent backgrounds in supergravity and string theory, Phys. Rev.
D 67 (2003) 024011, https://doi.org/10.1103/PhysRevD.67.024011, arXiv:hep-th/0207214.
[17] A. Buchel, Compactifications of the N = 2* flow, Phys. Lett. B 570 (2003) 89, https://doi.org/10.1016/j.physletb.
2003.07.030, arXiv:hep-th/0302107.
[18] A. Buchel, A. Ghodsi, Braneworld inflation, Phys. Rev. D 70 (2004) 126008, https://doi.org/10.1103/PhysRevD.
70.126008, arXiv:hep-th/0404151.
[19] A. Buchel, Inflation on the resolved warped deformed conifold, Phys. Rev. D 74 (2006) 046009, https://doi.org/
10.1103/PhysRevD.74.046009, arXiv:hep-th/0601013.
[20] A. Buchel, D.A. Galante, Cascading gauge theory on dS4 and string theory landscape, Nucl. Phys. B 883 (2014)
107, https://doi.org/10.1016/j.nuclphysb.2014.03.022, arXiv:1310.1372 [hep-th].
[21] A. Buchel, A. Karapetyan, De Sitter vacua of strongly interacting QFT, J. High Energy Phys. 1703 (2017) 114,
https://doi.org/10.1007/JHEP03(2017)114, arXiv:1702.01320 [hep-th].
[22] A. Buchel, Verlinde gravity and AdS/CFT, arXiv:1702.08590 [hep-th].
[23] P.M. Chesler, L.G. Yaffe, Numerical solution of gravitational dynamics in asymptotically anti-de Sitter spacetimes,
J. High Energy Phys. 1407 (2014) 086, https://doi.org/10.1007/JHEP07(2014)086, arXiv:1309.1439 [hep-th].
[24] I. Booth, Black hole boundaries, Can. J. Phys. 83 (2005) 1073, https://doi.org/10.1139/p05-063, arXiv:gr-qc/
0508107.
[25] P. Figueras, V.E. Hubeny, M. Rangamani, S.F. Ross, Dynamical black holes and expanding plasmas, J. High Energy
Phys. 0904 (2009) 137, https://doi.org/10.1088/1126-6708/2009/04/137, arXiv:0902.4696 [hep-th].
[26] P. Bosch, A. Buchel, L. Lehner, Unstable horizons and singularity development in holography, arXiv:1704.05454
[hep-th].
[27] A. Buchel, Singularity development and supersymmetry in holography, arXiv:1705.08560 [hep-th].
[28] P.K. Kovtun, A.O. Starinets, Quasinormal modes and holography, Phys. Rev. D 72 (2005) 086009, https://doi.org/
10.1103/PhysRevD.72.086009, arXiv:hep-th/0506184.
