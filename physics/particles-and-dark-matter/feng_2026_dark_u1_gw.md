Source: https://arxiv.org/abs/2602.14866v1
PDF sha256: dc0b0b34608846cb8f11b120dc9a23aa6431727ab2dcb907523ef21d2c7bdb27
License: http://creativecommons.org/publicdomain/zero/1.0/
Language: eng
Fidelity: machine-gated

# Transcription of feng_2026_dark_u1_gw.pdf

Transcription of `feng_2026_dark_u1_gw.pdf` in this directory, 55 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-55 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Gauge-independent gravitational waves from a minimal
dark U (1) sector with viable dark matter candidates
Wan-Zhe Feng∗ and Zi-Hui Zhang†

arXiv:2602.14866v1 [hep-ph] 16 Feb 2026

Center for Joint Quantum Studies and Department of Physics,
School of Science, Tianjin University, Tianjin 300350, PR. China

Happy Year of the Horse!

Abstract
Searches for stochastic gravitational wave backgrounds from first-order phase transitions offer a powerful probe of hidden sectors, but quantitative predictions in gauge
theories are obstructed by the gauge dependence of the finite-temperature effective potential and the associated tunneling action. We study a minimal gauged U (1) dark
sector containing a dark Higgs and a dark photon, optionally supplemented by a vectorlike dark fermion, coupled to the Standard Model through Higgs portal or kinetic
mixing. Using the Nielsen identity together with a controlled derivative expansion and
power counting, we construct a gauge-independent effective action in the high- and
low-temperature limits, enabling model-intrinsic nucleation dynamics and robust gravitational wave predictions. We perform dedicated Monte Carlo scans in both limits and
map viable microscopic parameters to detector-facing peak frequencies and amplitudes,
spanning bands relevant to pulsar timing arrays and planned space-based interferometers. In our scans, supercooled transitions typically produce the strongest signals,
whereas parametrically high-temperature transitions are comparatively rare and tend
to be weak. We further connect the phase transition phenomenology to viable dark
matter candidates within the same minimal field content, providing benchmark targets
for dark photon dark matter and dark fermion dark matter, and highlighting their
complementarity with gravitational wave observables. Overall, our results provide an
end-to-end, gauge-independent pipeline from a minimal hidden sector Lagrangian to
gravitational wave spectra and cosmologically viable dark matter benchmarks, yielding
the most reliable and concrete predictions to date for a minimal gauged U (1) dark
sector.

∗
†

Email: vicf@tju.edu.cn
Email: zhangzh_@tju.edu.cn

1

## PDF page 2

Contents
1 Introduction

3

2 The U (1)x extension and portals to the SM
2.1 The U (1)x extension of the SM . . . . . . . . . . . . . . . . . . . . . . . . .
2.2 Higgs portal through scalar mixing . . . . . . . . . . . . . . . . . . . . . . .
2.3 U (1) portal through kinetic mixing . . . . . . . . . . . . . . . . . . . . . . .

4
5
6
8

3 Gauge dependence of the scalar effective action
3.1 The gauge-dependent scalar effective potential . . . . . . . . . . . . . . . . .
3.2 Gauge-independent effective action . . . . . . . . . . . . . . . . . . . . . . .
3.2.1 The field-dependent effective action . . . . . . . . . . . . . . . . . . .
3.2.2 Phase transition at zero temperature . . . . . . . . . . . . . . . . . .
3.2.3 Phase transition at high temperatures (T ≫ mA′ ) . . . . . . . . . . .
3.2.4 Phase transition at low temperatures (T ≪ mA′ ) . . . . . . . . . . . .
3.2.5 Comments and discussions . . . . . . . . . . . . . . . . . . . . . . . .

9
9
12
12
13
17
21
24

4 Gravitational waves from first-order phase transition
4.1 The tunneling action and transition rate . . . . . . . . . . . . . . . . . . . .
4.2 Characteristic temperatures . . . . . . . . . . . . . . . . . . . . . . . . . . .
4.3 Hydrodynamic parameters . . . . . . . . . . . . . . . . . . . . . . . . . . . .
4.4 Gravitational wave power spectrum . . . . . . . . . . . . . . . . . . . . . . .
4.5 Gauge-dependent versus gauge-independent results . . . . . . . . . . . . . .
4.5.1 Gauge-dependent gravitational wave results . . . . . . . . . . . . . .
4.5.2 Gauge-independent gravitational wave predictions . . . . . . . . . . .

26
26
27
30
31
34
34
37

5 Evolution of dark sector particles
5.1 Boltzmann equations for dark particles . . . . . . . . . . . . . . . . . . . . .
5.1.1 Dark photon dark matter from the Higgs portal . . . . . . . . . . . .
5.1.2 Dark fermion dark matter from the U (1) portal . . . . . . . . . . . .
5.2 Benchmark models . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
5.3 Phenomenological implications . . . . . . . . . . . . . . . . . . . . . . . . . .

39
41
41
41
42
43

6 Conclusion and outlook

46

2

## PDF page 3

1

Introduction

The discovery of gravitational waves provides a novel probe of hidden sectors in which
dark matter may reside. Searches for stochastic gravitational wave backgrounds produced
by first-order phase transitions, either from the Standard Model (SM) augmented by new
physics [1–7], or in a dark sector [8–36], offer a powerful and complementary pathway to
uncovering new physics, especially in light of the continuing non-detection of dark matter in
conventional experiments. Gravitational wave observations thus constitute a key component
of a multi-messenger program to test particle physics in the early Universe. Accordingly, the
interplay between gravitational wave phenomenology and physics beyond the SM, particularly in scenarios aimed at explaining the nature of dark matter, has become one of the most
active frontiers of current research.
In well-motivated dark sector models, gravitational wave from a first-order phase transition is particularly compelling: New gauge symmetries and scalar fields are ubiquitous in
beyond the SM frameworks, and their symmetry breaking can naturally occur at scales both
below and above the electroweak scale, leading to gravitational wave signals that span a wide
range of frequencies. Consequently, it is essential to establish robust and concrete predictions
for gravitational wave signals from dark sectors that can be confronted with data across multiple frequency bands. If detected, such a signal can reveal information about the underlying
dark sector parameters including the gauge coupling, the scalar quartic coupling, and the
scalar vacuum expectation value (vev), that may be difficult or impossible to access directly
through collider probes or conventional dark matter searches.
However, a central obstacle to making reliable gravitational wave predictions in gauge
theories is the well-known gauge dependence of the finite-temperature effective potential and
the associated tunneling action. The Higgs effective potential as a function of an arbitrary
background field is not a physical observable. In Rξ gauges, the result depends explicitly
on the gauge-fixing parameter ξ, and thus a conventional computation based directly on
the gauge-dependent effective potential leads to gauge-dependent gravitational wave spectra that can hardly be regarded as genuine “predictions”. This gauge ambiguity obscures
the interpretation of parameter scans and hampers the extraction of robust, model-intrinsic
conclusions.
To address this issue, we adopt a gauge-independent formulation of the effective action based on the Nielsen identity [37–47], with particular emphasis on the low-temperature
treatment developed in [34]. The key payoff is a well-defined, gauge-independent tunneling
action and thus gauge-independent predictions for the phase transition and the resulting
gravitational wave signal within a controlled power counting scheme. We provide a detailed
discussion of the validity of the derivative expansion of the effective action, along with the
associated gauge coupling power counting rules, and the scaling relations between the gauge
coupling and the quartic coupling at zero, high, and low temperatures, thereby clarifying
several common sources of confusion in the literature. Building on the gauge-independent
effective action in the relevant high- and low-temperature limits, we perform dedicated Monte
Carlo scans in both regimes. This yields concrete, detector-facing predictions: each viable
parameter point maps to a peak frequency and amplitude of the stochastic background, enabling a direct comparison with the sensitivity targets of current and planned experiments
across various frequency bands.
3

## PDF page 4

We focus in particular on supercooled first-order phase transitions, which are among the
strongest and most distinctive sources of a stochastic gravitational wave background [19–21,
33–35,48–64]. In such transitions, the nucleation and percolation temperatures satisfy Tn,p ≪
Tc , which typically enhances the gravitational wave amplitude and shifts the peak frequency
to lower values, often bringing the signal into the nanohertz band and thereby attracting
substantial recent attention. Moreover, models that undergo strong supercooling often arise
in nearly flat potentials, for which the tunneling action remains large and nucleation is
delayed. In many such scenarios, the portal couplings to the SM are also small, making these
models challenging to probe with collider searches or conventional dark matter experiments.
Gravitational wave observations therefore become a leading discovery channel and can provide
compelling evidence for this region of parameter space.
In this work we focus on the simplest representative setup: a minimal U (1)x dark sector
featuring a dark Higgs field and a dark photon, and optionally a dark fermion, together with
portal interactions connecting the hidden sector to the SM. This minimality is not merely aesthetic. It makes the parameter dependence transparent, allows for a systematic exploration
of distinct thermal regimes, and admits dark matter candidates whose cosmological evolution can be computed consistently alongside the phase transition dynamics. In particular,
we highlight two viable dark matter candidates already present in the minimal field content:
(1) dark photon dark matter, which requires vanishing or negligibly small kinetic mixing;
and (2) dark fermion dark matter, which relies on a non-negligible dark photon portal.
This paper therefore provides robust and predictive results for gravitational waves generated by the symmetry breaking of a minimal gauged U (1) dark sector with a viable single
dark matter candidate. Such results are significant in the current high energy physics research, where no compelling hints of new physics have emerged from any experiments, and
precision tests as well as multi-messenger searches are becoming increasingly essential for
new physics discovery.
The remainder of this paper is organized as follows. In Section 2 we introduce the minimal dark U (1)x sector and portal interactions that connect it to SM states. In Section 3
we review the gauge dependence of the finite-temperature effective potential and the construction of gauge-independent effective actions based on the Nielsen identity, with particular
emphasis on the low-temperature regime relevant for supercooled phase transitions. In Section 4 we present the computation of gravitational wave signatures from first-order phase
transitions, including the tunneling action and transition rate, characteristic temperatures,
hydrodynamic parameters, and the resulting gravitational wave power spectra, and we compare gauge-dependent result and gauge-independent predictions. In Section 5 we analyze the
cosmological evolution of dark sector particles, derive the coupled Boltzmann equations for
the dark matter scenarios of interest, and present benchmark models and phenomenological
implications. Finally, we summarize our conclusions and present an outlook in Section 6.

2

The U (1)x extension and portals to the SM

In this section, we review the minimal U (1)x extension of the SM, featuring a dark Higgs, a
dark photon, and optionally dark fermions, with their portal interactions to SM particles.

4

## PDF page 5

2.1

The U (1)x extension of the SM

We consider a U (1)x gauge extension of the SM. The full Lagrangian can be written as
L = LSM + Lhid + Lmix ,

(2.1)

where LSM and Lhid is given by
1
LSM ⊃ − Fµν F µν − µ2SM H † H + λSM (H † H)2 ,
4
∣2
∣
1
∣
∣
Lhid = − Fx µν Fxµν + ∣(∂µ − igx A′µ )Φ∣ + µ2x Φ∗ Φ − λx (Φ∗ Φ)2
4
+ gx χγ µ χA′µ + χ(iγ µ ∂µ − mχ )χ ,

(2.2)

(2.3)

where Fµν , Fx µν are the field strengths of the hypercharge and U (1)x gauge fields respectively,
H is the SM Higgs doublet and Φ is the U (1)x Higgs field with U (1)x charge +1. A′µ is the
U (1)x gauge field, and χ is a dark fermion with vector mass mχ and U (1)x charge Qx = +1.
The most important parameters relevant for the study of both U (1)x gravitational wave
physics and dark matter physics are: the U (1)x gauge coupling gx , the U (1)x Higgs vev vx
and its quartic coupling λx .
The mixing terms contain kinetic mixing and Higgs mixing contributions, written as
δ
Lmix = − Fµν Fxµν − λmix (H † H)(Φ∗ Φ)2 ,
2

(2.4)

where δ and λmix are mixing parameters, both receiving stringent constraints from experiments. The experimental constraint of λmix will be discussed in Section 5.2. The kinetic
mixing can result in from either integrating out bifundamental fields charged under both the
U (1)Y and U (1)x , which can be absent; or from graviton loop effects, which are in general
suppressed. We focus on two classes of dark matter candidates in this paper:
• Dark photon dark matter, which requires vanishing or extremely small kinetic mixing, δ ≲ 10−16 .
• Dark fermion dark matter, which requires a non-negligible kinetic mixing.
Expanding Φ around the background field ϕc as
)
1 (
Φ = √ ϕc + hx + iG ,
2

(2.5)

where hx and G are the dark Higgs and Goldstone boson respectively, we obtain
∣
∣2
]2
1
1[
∣
∣
∣(∂µ − igx A′µ )Φ∣ = (∂µ hx + gx A′µ G)2 +
∂µ G − gx A′µ (ϕx + hx )

2
2
1
1
2
2
= (∂µ hx ) + (∂µ G) − gx ϕc (∂µ G)A′µ + · · · .
2
2

(2.6)

Together with the gauge fixing term and the ghost terms,
Lgf = −

)2
1(
∂µ A′µ + ξgx ϕc G ,
2ξ

5

(2.7)

## PDF page 6

[

]

Lghost = c −∂ 2 − ξgx2 ϕc (ϕc + hx ) c ,

(2.8)

where ξ is the gauge parameter, c(c) is the ghost (anti-ghost) field, the mixing between A′
and G in Eq. (2.6) is canceled by the cross term in Lgf . The field-dependent masses in the
Rξ gauge are given by
m2A′ = gx2 ϕ2c ,

m2A′0 = ξm2A′ = ξgx2 ϕ2c ,

(2.9)

m2hx = −µ2x + 3λx ϕ2c ,
m2c = ξm2A′ = ξgx2 ϕ2c ,
m2G = −µ2x + λx ϕ2c + ξm2A′ ,

(2.10)
(2.11)
(2.12)

where the masses of the longitudinal (time-like) gauge component A′0 , the ghost and the
Goldstone boson depend on the gauge parameter ξ.

2.2

Higgs portal through scalar mixing

We now discuss the Higgs portal interactions from H, Φ quartic mixing term. The full scalar
potential reads
(

V (H, ϕx ) = −µ2SM H † H − µ2x Φ∗ Φ + λSM H † H

)2

)2

(

+ λx Φ∗ Φ

(

+ λmix H † H

)(

)

Φ∗ Φ . (2.13)

Working in the unitary gauge, H and Φ can be expanded around their minima as
1
H=√
2

(

0
vSM + h0

)

,

)
1 (
Φ = √ vx + h0x ,
2

(2.14)

where h0 , h0x are real scalars in the flavor eigenbasis. The vacuum expectation values vSM , vx
are given by
4µ2SM λx − 2µ2x λmix
,
4λx λSM − λ2mix
4µ2 λSM − 2µ2SM λmix
.
vx2 = x
4λx λSM − λ2mix

2
vSM
=

(2.15)
(2.16)

The kinetic and mass terms are then
[
]
∣
∣2
)
1(
1 2 ′2 ( 0 )2
∣
∣
′
0 2
′2 0
2 ′2
∣(∂µ − igx Aµ )Φ∣ =
∂µ hx + gx A hx + 2vx A hx + vx A ,
2
2(
)(
)
)
1(
2λ v 2
λ v v
h0

−Lmass =

SM SM

h0 h0x

2

λmix vSM vx

mix SM x
2λx vx2

h0x

(2.17)
.

(2.18)

An orthogonal transformation is performed to diagonalize the mass matrix, which transformed the original eigenbasis (h0 h0x )T into mass eigenbasis (h hx )T as
(

h
hx

)

(

=

cos θ − sin θ
sin θ cos θ
6

)(

h0
h0x

)

,

(2.19)

## PDF page 7

where the mixing angle θ is calculated to be
θ=

1
λmix vSM vx
.
arctan
2
2
λx vx2 − λSM vSM

(2.20)

The mass eigenvalues are
√

2
2
m2h = λSM vSM
+ λx vx2 + (λSM vSM
− λx vx2 )

1 + tan2 2θ ,

(2.21)

√

2
2
− λx vx2 ) 1 + tan2 2θ .
m2hx = λSM vSM
+ λx vx2 − (λSM vSM

(2.22)

Define ∆m2 = m2hx − m2h and we obtain
∆m2 sin 2θ
,
2vSM λmix
m2
∆m2 sin2 θ
,
λSM = 2h +
2
2vSM
2vSM
)
( 2
2
mhx
2vSM
λ2mix
2
− sin θ ,
λx =
sin2 2θ ∆m2 ∆m2
vx =

(2.23)
(2.24)
(2.25)

where the quartic coupling λmix must satisfy all current experimental constraints. In the
mass eigenbasis, the scalar potential is now written as
V (h, hx ) = Ch3 h3 + Ch2 hx h2 hx + Chh2x hh2x + Ch3x h3x
+ Ch4 h4 + Ch3 hx h3 hx + Ch2 h2x h2 h2x + Chh3x hh3x + Ch4x h4x
)
1(
h hx
+
2

(

m2h 0
0 m2hx

)(

h
hx

)

(2.26)

,

where the trilinear couplings are given by
2
2
2m2h + m2hx
λmix vSM
m2h
λmix vSM
2
2
2h =
Ch3 =
s
s
c
+
,
c4θ −
,
C
θ
h
θ
x
2vSM cθ
∆m2 θ
2vSM
∆m2
(
)
(
2
2 )
m2hx
m2h + 2m2hx
λmix vSM
λmix vSM
4
2
2
Ch3x =
s +
c , Chh2x =
cθ s θ −
,
2vSM sθ θ
∆m2 θ
2vSM
∆m2

(

(

)

)

(2.27)
(2.28)

and the quartic couplings are
)
1 s22θ
1 (
C =
λmix + c4θ λSM + s4θ λx , Ch3 hx = s2θ −c2θ λmix + 2c2θ λSM − 2s2θ λx ,
4 4
4
)
(
)
1 s22θ
1 (
Ch4x =
λmix + s4θ λSM + c4θ λx , Chh3x = s2θ c2θ λmix + 2s2θ λSM − 2c2θ λx ,
4 4
4
[
)
(
)]
1 ( 2
3
Ch2 h2x =
c2θ + s22θ λmix + s22θ −λmix + λSM + λx ,
4
2
(

)

h4

(2.29)
(2.30)
(2.31)

with cθ ≡ cos θ and sθ ≡ sin θ. The U (1)x gauge boson A′ acquires a mass MA′ = gx vx ,
referred to as a dark photon γ ′ . The couplings of γ ′ to two Higgs fields can be obtained from
the kinetic term
[
∣
∣2
)2
(
)2
(
)(
)]
1 2(
∣
∣
′
2
µ
∣(∂µ − igx Aµ )Φ∣ =
s ∂µ h + cθ ∂µ hx − 2sθ cθ ∂µ h ∂ hx
2 θ
7

## PDF page 8

1
+ gx2 A′2 s2θ h2 + c2θ h2x − 2sθ cθ h hx + 2vx (sθ h + cθ hx ) + vx2 .
2
[

]

(2.32)

The interactions of h, hx to SM particles are calculated to be
L=

1
2
W µ+ Wµ− + MZ2 Z µ Zµ
MW

(

)(

h0
1+
vSM

)2

−

∑

mi fi fi

2
i
)
)(
2
cθ 2 2cθ
1
2
µ+
−
2 µ
h
+
h
M
W
W
+
M
Z
Z
→
µ
W
µ
2
vSM
vSM
2 Z
( 2
)(
)
sθ 2 2sθ
1 2 µ
2
µ+
−
+ 2 hx +
hx MW W Wµ + MZ Z Zµ
vSM
vSM
2

h0
vSM

(

1
cθ h + sθ hx ∑
2cθ sθ
2
W µ+ Wµ− + MZ2 Z µ Zµ −
+ 2 hhx MW
mi fi fi .
vSM
2
vSM
i
(

2.3

)

(2.33)

U (1) portal through kinetic mixing

We now discuss U (1)x portal interactions from the kinetic mixing. In the gauge eigenbasis
V T = (C, B, A3 ) where C, B and A3 denote the dark U (1)x gauge field, SM hypercharge field,
and the neutral SU (2)L gauge field respectively, the mixing matrices take the form [65, 66]
1 δ 0

K= δ 1 0 
,
0 0 1


gx2 vx2
0
0


2
1
1 2 2
2
g v
− 4 g2 gY vSM
M0 =  0
,
4 Y SM
1 2 2
2
0 − 41 g2 gY vSM
g
v
4 2 SM







(2.34)

where g2 and gY denote the SM couplings. To diagonalize these two matrices simultaneously, we first perform a non-unitary transformation K that diagonalizes the kinetic terms
with K T KK = 1. Under the transformation V ′ = K −1 V , the mass matrix becomes
M0′2 = K T M02 K. We then apply an orthogonal transformation O such that OT K T M02 KO is
diagonal. The transformation matrices K and O are found to be
cδ 0 0

K=
 −sδ 1 0  ,
0 0 1




1
0
0
cos ψ 0 sin ψ

0
1
0 
O=
 0 cos θW − sin θW  
,
0 sin θW cos θW
− sin ψ 0 cos ψ






(2.35)

√
√
√
√
where cδ = 1/ 1 − δ 2 , sδ = δ/ 1 − δ 2 , cos θW = g2 / g22 + gY2 , sin θW = gY / g22 + gY2 . The
angle ψ is
√
1
2δ 1 − δ 2 sin θW
ψ = arctan
,
(2.36)
2
1 − ε2 − δ 2 (1 + sin2 θW )
√

where we define ε2 ≡ M12 /MZ2 with M1 = gx vx and MZ = 12 vSM g22 + gY2 .
The full rotation matrix is thus
cδ cos ψ
0
cδ sin ψ
−s
cos
ψ
+
sin
ψ
sin
θ
cos
θ
−s
sin
ψ
− cos ψ sin θW 
R ≡ KO = 

,
δ
W
W
δ
− sin ψ cos θW
sin θW
cos ψ cos θW




8

(2.37)

## PDF page 9

which diagonalizes the kinetic and mass matrices simultaneously and transform the original
eigenbasis V T = (C, B, A3 ) to the mass eigenbasis E T = (A′ , Aγ , Z) with E = RT V . The
resulting mass matrix is
MA2 ′ 0 0


2
T
2
M = R M0 R =  0 0 0  ,
0 0 MZ′2




(2.38)

and the interactions of gauge bosons with fermions can be obtained from
Lint = (gx Jx , gY JY , g2 J3 ) V = (gx Jx , gY JY , g2 J3 ) RE .

(2.39)

The neutral current couplings are summarized as follows
Lχ = gx Qx (R11 A′µ + R13 Zµ )χγ µ χ ,
]
[
1
LA′ ,Z,Aγ = fi γ µ (vi′ − a′i γ 5 )fi A′µ + (vi − ai γ 5 )fi Zµ + eQi fi γ µ fi Aγ µ ,
2
where eQi is the electric charges of the SM fermions, and
vi = (g2 R33 − gY R23 ) Ti3 + 2gY R23 Qi ,
ai = (g2 R33 − gY R23 ) Ti3 ,
vi′ = (g2 R31 − gY R21 ) Ti3 + 2gY R21 Qi ,
a′i = (g2 R31 − gY R21 ) Ti3 .

3

(2.40)
(2.41)

(2.42)
(2.43)
(2.44)
(2.45)

Gauge dependence of the scalar effective action

In gauge theories, the Higgs effective potential as a function of arbitrary background field
is not a physical observable and is in general gauge-dependent. Consequently, the effective
potential depends not only on the U (1)x parameters gx , λx , and vx , but also on the background field value ϕc and on the gauge-fixing parameter ξ. In the conventional approach, one
evaluates the gauge-dependent effective potential and the resulting effective action, which
leads to gauge-dependent gravitational wave results.
In this section, we review the gauge-independent formulation of the effective action based
on the Nielsen identity. This framework is essential for obtaining well-defined gravitational
wave predictions from cosmological phase transitions.

3.1

The gauge-dependent scalar effective potential

The full (gauge-dependent) effective potential is given by
Veff (ϕc , T, ξ) = V0 (ϕc ) + V01-loop (ϕc , ξ) + VT1-loop (ϕc , T, ξ) + Vdaisy (ϕc , T, ξ) ,

(3.1)

where V0 is the tree-level potential, V01-loop and VT1-loop represent the one-loop corrections at
zero and finite temperatures respectively, and Vdaisy corresponds to the daisy contribution
arising from higher-loop resummation. The tree-level potential V0 is written as
λx
µ2
V0 (ϕc ) = − x ϕ2c + ϕ4c .
2
4
9

(3.2)

## PDF page 10

At zero temperature, the one-loop effective potential after dimensional regularization is expressed as
]
[
( 2
)
∑
m4i (ϕc )
mi (ϕc )
1-loop
(ϕc ) =
(3.3)
V0
±gi
log
− Ci − CUV ,
64π 2
Λ2
i
where the prefactor ±1 corresponds to bosons and fermions respectively, gi denotes the degree
of freedom of particle i, and Λ is the renormalization scale. In this work, we set the scale Λ
to be of order the U (1)x gauge boson mass, Λ = gx vx .
The renormalization constants are Ci = 5/6 for gauge bosons and Ci = 3/2 for scalars
and fermions, while CUV = 2ϵ − γ + log 4π with ϵ = 4 − D. It is convenient to adopt the
MS renormalization scheme1 to remove the ultraviolet divergence, under which the one-loop
correction at zero temperature reduces to the Coleman-Weinberg potential, written as
m2i (ϕc )
m4 (ϕc )
VCW (ϕc ) =
− Ci
±gi i 2 log
64π
Λ2
i
[

∑

(

)

]

m2hx
1
3
m2G 3
4
4
=
m
log
−
−
+
m
log
G
64π 2 hx
Λ2
2
Λ2
2
(
)
(
)]
2
2
m ′
5
m
3
+ 3m4A′ log A2 −
− m4c log 2c −
.
Λ
6
Λ
2
[

(

)

(

)

(3.6)

In the last line of the above equation, the coefficient −1 from the m4c term arises from the +1
contribution of the longitudinal (time-like) gauge scalar mode, c.f., Eq. (2.9), together with
the −2 contribution from the ghost.
The thermal contribution to the one-loop effective potential is given by
m2i (ϕc )
T4
,
± gi 2 JB/F
2π
T2
i
(

VT1−loop (ϕc , T ) =

)

∑

where the thermal function J is defined as
ˆ ∞
[
( √
)]
2
2
2
2
JB/F (x ) ≡
dy y log 1 ∓ exp − y + x
.

(3.7)

(3.8)

0
1

Alternatively, one may adopt an on-shell renormalization scheme, which is commonly used in supercooled
phase transition analyses, by introducing an additional counterterm potential Vct , written as
Vct (ϕc ) = −

δµ2x 2 δλx 4
ϕ +
ϕ ,
2 c
4 c

(3.4)

which cancels the ultraviolet divergence of the one-loop correction at zero temperature. Vct is determined by
imposing the tadpole and on-shell mass conditions at zero temperature
∣
∣
∂ 2 (VCW + Vct ) ∣∣
∂(VCW + Vct ) ∣∣
=
0
,
= 0,
(3.5)
∣
∣
∂ϕc
∂ϕ2c
ϕc =vx
ϕc =vx
ensuring that the potential minimum and the field mass coincide with their tree-level values.
However, in this scheme some of the counterterms are ξ-dependent and may spoil the power-counting
procedure required for the gauge-independent analysis presented in the next subsection. We therefore adopt
the MS scheme throughout this paper.

10

## PDF page 11

In the high-temperature limit (x = m/T ≪ 1), the thermal function can be expanded as [67]
π4 π2 2 π 3
1
+ x − x − x4 log x2 + · · · ,
45 12
6
32
4
2
7π
π
1
JF (x2 ) ≈
− x2 − x4 log x2 + · · · .
360 24
32

JB (x2 ) ≈ −

(3.9)
(3.10)

In the low-temperature regime (x ≫ 1), the expansion takes the form [68, 69]
JB/F (x2 ) ≈ ∓

k
∑
(±1)l
l=1

l2

x2 K2 (xl) ,

(3.11)

where K2 is the modified Bessel function of the second kind, and k denotes the order at
which the series is truncated. It has been shown that truncating at k = 2, 3 provides a good
approximation [68].
Daisy (or ring) resummation [2], which sums the leading infrared-divergent bosonic zeromode contributions to all orders2 and thereby renders the finite-temperature effective potential infrared finite in regimes where naive perturbation theory would otherwise break down,
must be included in the full thermal Higgs effective potential. Two approaches are commonly
used for daisy resummation: the Parwani method [76] and the Arnold-Espinosa method [3].
In the Parwani method, the daisy correction is implemented by replacing the tree-level masses
in JB functions with thermal masses,
m2i (ϕc ) → m2i (ϕc ) + Πi (T ) .

(3.12)

In the Arnold-Espinosa method that we follow in this work, an additional term is added to
the effective potential,
[
]3/2
[
]3/2
T ∑
− m2i (ϕc )
,
gi m2i (ϕc ) + Πi (T )
Vdaisy (ϕc , T ) = −
12π i
}

{

(3.13)

where the sum runs over the longitudinal gauge boson and scalar modes. The one-loop
thermal masses for the U (1)x dark sector particles are given by [30]
n
1 2 2 ∑
1 2 2 2
ΠA′ = gx T +
gx Qi T ,
3
i=1 6

1
1
Πhx = λx T 2 + gx2 T 2 ,
3
4

1
ΠG = λx T 2 ,
4

(3.14)

where the second term in ΠA′ arises from chiral fermion loops. For a Dirac fermion χ with
U (1)x charge Qx , it can be treated as two chiral fermions with the same charge, one obtains
1
ΠA′ = gx2 (1 + Q2x )T 2 .
3

(3.15)

The two prescriptions agree at leading infrared order but can differ by higher-order terms.
Although the Parwani approach is often numerically smoother, the Arnold–Espinosa prescription is generally preferred for a controlled perturbative expansion and is therefore more
suitable for the gauge-independent analysis.
2

Another approach is to integrate out the temperature dependence by matching to a three-dimensional
EFT [70–75].

11

## PDF page 12

3.2

Gauge-independent effective action

As discussed above, the effective potential evaluated at a fixed background field value is
in general gauge-dependent, and therefore cannot by itself be used to define an unambiguous gravitational wave signal. A gauge-independent treatment can be formulated using the
Nielsen identity, which states that an infinitesimal change in the gauge parameter ξ can be
compensated by a corresponding field redefinition of the background configuration. In this
sense, the ξ dependence of Veff at fixed ϕ is a coordinate effect in field space. The induced
shift of the background field from the field redefinition, is of higher order in the ℏ expansion
and therefore does not appear at the leading order.
Gauge independence of physical quantities, such as the bounce action, the nucleation rate,
and related observables, follows when they are evaluated on-shell, i.e., on configurations satisfying δS/δϕ = 0, within a consistent loop (ℏ) expansion. Under this procedure, the relevant
effective action is gauge-independent, leading to well-defined gravitational wave predictions
for a given model.
In a weakly coupled U (1)x theory, the ℏ order tracks powers of gx2 and λx . Every gauge
interaction brings at least two powers of gx per closed loop in the Abelian U (1)x theory, and
scalar self-interactions bring one power of λx at one loop. Hence, each extra loop corresponds
to one extra factor of gx2 or λx . With an appropriate choice of power counting, λx ∼ gxn , which
depends on the temperature regime and will be specified in this subsection, one can organize
the effective potential as an expansion in powers of the U (1)x gauge coupling gx . This ordering
separates leading and subleading contributions in a controlled manner and ensures that the
resulting effective action is gauge-independent at the order considered, guaranteed by the
Nielsen identity.
In this subsection, we review the gauge-independent analysis of the scalar effective action
for phase transitions at zero temperature, in the high-temperature regime, and in the lowtemperature (supercooled) regime.
3.2.1

The field-dependent effective action

In quantum field theory, the tree-level potential is modified by higher-order radiative corrections, which can be calculated using the functional method. Consider a scalar field ϕ coupled
to a classical source J, the partition function is given by
ˆ
ˆ
{[
]}
iW [J]
4
Z[J] = e
= Dϕ exp i S[ϕ] + d x Jϕ ,
(3.16)
´
where S[ϕ] = d4 x L[ϕ] denotes the action. The functional derivative of W [J] with respect
to J(x) is computed as
´
´
δ log Z[J]
Dϕ ei (L+Jϕ) ϕ(x)
δW [J]
´
= −i
= ´
,
(3.17)
δJ(x)
δJ(x)
Dϕ ei (L+Jϕ)
corresponding to the vacuum expectation value of ϕ(x) in the presence of a non-zero external
source J(x). This quantity defines the classical field (mean field) ϕc (x) as
∣ ⟩
δW [J] ⟨ ∣∣
∣
= Ω∣ϕ(x)∣Ω ≡ ϕc (x) .
J
δJ(x)

12

(3.18)

## PDF page 13

The effective action Γ[ϕ] is then defined through the Legendre transformation of W [J] as
ˆ
Γ[ϕc ] ≡ W [J] − d4 x J(x)ϕc (x) ,
(3.19)
satisfying

δ
Γ[ϕc ] = −J(x) .
δϕc (x)

(3.20)

When the external source J(x) is set to zero, one obtains
∣
δ
= 0.
Γ[ϕc ]∣∣
δϕc (x)
J=0
∣

(3.21)

For a translation-invariant vacuum state, one may obtain an x-independent solution ϕc
and express the effective action in form of
ˆ
Γ[ϕc ] = − d4 x Veff (ϕc ) ,
(3.22)
where Veff denotes the effective
´ potential. Applying a Fourier transformation from position
to momentum space, ϕ̃(p) = d4 x e−ipx ϕ(x), the effective potential can be recast as
Veff (ϕc ) = −

∞
∑
ϕnc
n=0

n!

Γ(n) (p = 0) ,

(3.23)

where Γ(n) represents the n-point effective vertex in momentum space with all external momenta set to zero.
In what follows, we use ϕc to denote the background (mean) field. For a homogeneous
configuration, the true vacuum at temperature T is given by the constant field value ϕc that
minimizes the finite-temperature effective potential Veff (ϕc , T ) globally.
3.2.2

Phase transition at zero temperature

The gauge-independent bubble nucleation rate at zero temperature is derived in [37] by employing the power counting of the gauge coupling and a derivative expansion of the Nielsen
identity [77]. In this subsection, we review the computation in [37] demonstrating the gauge
independence of the effective action at zero temperature, and the extension to finite temperature will be discussed in Section 3.2.3 and 3.2.4.
The gauge dependence of the effective action in Rξ gauges governed by the Nielsen identity
is expressed as
ˆ
δSeff
∂Seff
= − d4 x
C(x) ,
(3.24)
ξ
∂ξ
δϕc (x)
where ϕc denotes the background field, C(x) is the Nielsen function, given by
ˆ
⟨
(
)⟩
√
igx
C(x) =
d4 y c̄(x)G(x)c(y) × ∂µ A′µ (y) + 2ξgx ϕc G(y) ,
2
13

(3.25)

## PDF page 14

where gx is a gauge coupling, c, c̄ and G represent the ghost, anti-ghost and Goldstone boson,
respectively. A derivative expansion of Seff , C(x) and δSeff /δϕc can then be performed in
powers of the derivatives of ϕc , yielding
ˆ
[
]
Seff = d4 x Veff (ϕc ) + 12 Z(ϕc )(∂µ ϕc )2 + O(∂ 4 ) ,
(3.26)
[

]

C(x) = C0 (ϕc ) + D(ϕ)(∂µ ϕc )2 − ∂ µ D̃(ϕc )∂µ ϕc + O(∂ 4 ) ,

(3.27)

[
]
δSeff
∂Veff (ϕc ) 1 ∂Z
=
+
(∂µ ϕc )2 − ∂ µ Z(ϕc )∂µ ϕc + O(∂ 4 ) ,
δϕc
∂ϕc
2 ∂ϕc

(3.28)

where Z(ϕc ) denotes the field renormalization factor and C0 , D, D̃ are Nielsen coefficients;
the total derivative term containing D̃ are discussed in [39]. Substituting the derivative
expansions given in Eqs. (3.26)–(3.28) into Eq. (3.24), the Nielsen identity at order ∂ 0 and
∂ 2 is derived as
ξ

∂Veff
∂Veff
= −C0
,
∂ξ
∂ϕc
∂ 2 Veff
∂Z
∂Z
∂C0
∂Veff
= −C0
,
ξ
− 2Z
+ 2D
+ 2D̃
∂ξ
∂ϕc
∂ϕc
∂ϕc
∂ϕ2c

(3.29)
(3.30)

where integration by parts is applied and the surface term vanishes as follows:
ˆ
ˆ
{ [
}
[
]
] [
]
4
d x C0 (ϕc )∂µ Z(ϕc )∂µ ϕc = d4 x ∂µ C0 (ϕc )Z(ϕc )∂µ ϕc − ∂µ C0 (ϕc ) Z(ϕc )∂µ ϕc
ˆ
[
]
= d4 x ∂µ C0 (ϕc ) Z(ϕc )∂µ ϕc
ˆ
∂C0
= d4 x Z(ϕc )
(∂µ ϕc )2 .
(3.31)
∂ϕc
Now take the loop (ℏ) expansion to the potential and the field strength renormalization as
V = V0 + ℏV1 + ℏ2 V2 + · · · ,

Z = 1 + ℏZ1 + ℏ2 Z2 + · · · .

(3.32)

In a weakly coupled U (1)x theory, the order in ℏ tracks powers of gx2 and λx . The analysis
below will proceed by expanding V and Z, as well as the Nielsen coefficients, in powers of
the U (1)x gauge coupling gx .
For the zero-temperature analysis, a Higgs-like scalar potential without thermal effects
does not generically produce a phase transition. A first-order transition requires two minima
separated by a barrier, with the true vacuum lying below the false vacuum initially located
at ϕ = 0. One simple way to realize this in a toy setup is to choose a positive mass term for
the scalar,
1
(3.33)
V (ϕ) ⊃ µ2x ϕ2 ,
µ2x > 0
2
in contrast to the usual Higgs potential with a negative mass-squared term. Additionally,
since the barrier is generated by the Coleman-Weinberg contribution, the positive mass term
∼ µ2 cannot be parametrically large, otherwise the potential will not develop. This setup can
14

## PDF page 15

thus support a zero-temperature phase transition and is often adopted for pioneering studies
[37].
For a gauge theory in which the gauge symmetry is broken by a Higgs field, a crucial
prerequisite for a controlled expansion is to choose an appropriate power counting for the
Higgs quartic coupling λx in terms of the gauge coupling gx . In the zero-temperature regime,
one commonly adopts the scaling
λx ∼ gx4 .
(3.34)
This scaling has two key insights:
• The generation of the barrier at zero temperature: In a gauged U (1)x theory,
the dominant Coleman-Weinberg contribution scales as
VCW (ϕ) ∼

gx2 ϕ2
gx4 4
gx4 4
ϕ
log
∼
ϕ .
16π 2
Λ2
16π 2

(3.35)

The extremum condition V ′ (vx ) = 0 implies
(

µ2x ∼ vx2

g4
λx + x 2
16π

)

.

(3.36)

For the Coleman-Weinberg contribution to compete with the tree-level quartic term
and thereby generate a barrier, one requires λx ∼ gx4 . It then follows that µ2x ∼ gx4 ϕ2c .
• The validity of the derivative expansion: The derivative expansion is a lowmomentum expansion obtained after integrating out the heavy modes of the theory,
and it is expanded in powers of the ratio of the characteristic momentum scale associated
with spatial variations of the background field, kfield , to the mass scale of heavy modes
that have been integrated out, Λ(ϕwall ). Here ϕwall denotes the typical field value within
the bubble wall. The derivative expansion is thus valid when kfield /Λ(ϕwall ) ≪ 1, i.e.,
kfield ≪ Λ(ϕwall ).
The characteristic momentum is estimated as
kfield ∼

1
Lwall

∼

√

V ′′ (ϕwall ) ,

(3.37)

where Lwall is the characteristic thickness of the bubble wall. For the zero-temperature
phase transition,
g2
kfield ∼ x ϕwall ,
(3.38)
4π
which is parametrically much smaller than the scale at which the dark photon has
been integrated out, Λ = gx ϕwall , and thus the derivative expansion is valid at zero
temperature.
At zero temperature, the effective potential Veff is given by
0T
0T
8
Veff
= Vg0T
4 + Vg 6 + O(gx ) ,
x
x

15

(3.39)

## PDF page 16

with the leading and subleading effective potentials written as
µ2x 2 λx 4
m4 ′
m2 ′
5
ϕc + ϕc + 3 A2 log A2 −
,
2
4
64π
Λ
6
(
)
(
)
m4G
m2G 3
m4c
m2c
3
0T
Vgx6 =
log 2 −
−
log 2 −
,
64π 2
Λ
2
64π 2
Λ
2
(

Vg0T
4 =
x

)

(3.40)
(3.41)

The field strength renormalization Z is expanded in powers of the gauge coupling gx as
Z = 1 + Zgx2 + O(gx4 ) .
(
)
g2
m2
m2 ′
= x 2 ξ log 2c + 3 log A2 + ξ ,
16π
Λ
Λ

(3.42)

and perturbation analysis shows that the Nielson coefficient C0 (ϕc ) starts at order gx2 and
D, D̃ starts at unity, expressed as
C0 = Cgx2 + O(gx4 )
m2
ξg 2 ϕc
= − x 2 log 2c + O(gx4 ) ,
32π
Λ
2
D, D̃ = 1 + O(gx ) .

(3.43)
(3.44)

The leading and subleading contributions to the Nielsen identity are thus obtained as follows
ξ
ξ

∂Vg0T
4
x
∂ξ
∂Vg0T
6
x

= 0,

(3.45)

= −Cgx2

∂Vg0T
4
x

∂ξ
∂ϕc
∂Zgx2
∂Cgx2
ξ
= −2
,
∂ξ
∂ϕc

,

(3.46)
(3.47)

which hold analytically.
The standard procedure for calculating the bubble nucleation rate at zero temperature is
finding a bounce solution ϕb [78, 79] from the leading-order equation of motion
∣
∂Vg0T
4
x ∣
∣

.

(3.48)

Γ = A e−(S0 +S1 ) ,

(3.49)

□ϕb =

∣

∂ϕc ∣ϕc =ϕb

The nucleation rate is then obtained as
0T

0T

where the coefficient A is expressed in terms of functional determinants associated with the
characteristic mass scales of the theory, S00T and S10T denote the Euclidean action of the
bounce solution, given by
ˆ
]
[
1
0T
4
0T
2
S0 = d x Vgx4 (ϕb ) + (∂µ ϕb ) ,
(3.50)
2
16

## PDF page 17

ˆ
S10T =

1
Zg2 (ϕb , ξ) (∂µ ϕb )2 .
d4 x Vg0T
6 (ϕb , ξ) +
x
2 x
]

[

(3.51)

is ξ-independent. Using Eqs. (3.41) and (3.42), one finds
S0 is gauge-independent since Vg0T
4
x
ˆ

[ ∂V 0T

1 ∂Zgx2
dx ξ
+ ξ
(∂µ ϕb )2
∂ξ
2 ∂ξ
ˆ
[
]∣∣
∂Vg0T
4
∂Cgx2
4
2 ∣
x
= − d x Cgx2
+
(∂µ ϕb ) ∣∣
∂ϕc
∂ϕc
ϕc =ϕb
∣
ˆ
[
]
0T
∣
∂Vgx4
∣
= − d4 x Cgx2
+ (∂µ Cgx2 )(∂µ ϕb ) ∣∣
∂ϕc
ϕc =ϕb
ˆ
[ ∂V 0T
]∣∣
gx4
∣
= − d4 x Cgx2
− □ϕb ∣
∣
∂ϕc
ϕc =ϕb

∂S 0T
ξ 1 =
∂ξ

4

]

gx6

= 0,

(3.52)

the bounce solution ϕb ensures the gauge independence of the subleading effective action S10T .
3.2.3

Phase transition at high temperatures (T ≫ mA′ )

High-temperature phase transitions typically occur at temperatures only slightly below the
critical temperature Tc , which is generally much larger than the U (1)x gauge boson mass. In
this situation, the percolation temperature that characterizes the onset of the phase transition
is usually close to the nucleation temperature, Tp ≈ Tn , as will be discussed in Section 4.2. At
Tn , the background field value satisfies ϕc ≳ vx , and the transition temperature is much larger
than the particle masses in the U (1)x sector, i.e. Tn ≫ mA′ . In this regime, the calculation
can be simplified by expanding in m/T and neglecting higher-order terms.
The bubble nucleation rate at finite temperature is given by
Γ(T ) = A(T ) e−S3 (T )/T ,
ˆ
[
]
S3 (T ) = d3 x Veff (ϕc , T ) + 21 Z(ϕc , T )(∂i ϕc )2 + O(∂ 4 ) ,

(3.53)
(3.54)

where ϕc denotes the background field, Z(ϕc , T ) is the field renormalization factor, and the
prefactor A(T ) will be given in Eq. (4.4).
We now implement the power counting procedure for the high-temperature phase transition, following [39, 43, 44]. The nucleation temperature Tn marks the onset of the phase
transition and lies slightly below the critical temperature Tc , at which the two minima of
the effective potential become degenerate. Therefore Tc can be taken as a representative
characteristic temperature of the transition. Including the one-loop thermal corrections to
Veff and employing the high-temperature expansion in Eq. (3.9), the leading contribution to
the effective potential becomes
VLO = −

µ2x 2 λx 4 T 2 2
ϕc + ϕc +
(mhx + 3m2A′ + m2G − m2c ) + · · ·
2
4
24
17

## PDF page 18

1
λx
= − µ2eff ϕ2c + ϕ4c · · · ,
2
4

(3.55)

where particle masses are given in Eqs. (2.9)–(2.12), and
−µ2eff = −µ2x +

(

1
λ + 14 gx2
3 x

)

(3.56)

T2 .

The negative mass term −µ2x competes with the positive T 2 corrections, leading to a critical
crossover temperature To where the Higgs effective mass is zero, i.e., µ2eff = 0. This temperatures is just slightly below Tc and a little bit above Tn , i.e., Tc ≳ To ≳ Tn . Near the
high-temperature phase transition, all terms in the potential are expected to be of the same
order of magnitude [3, 42],3 yielding the following power counting relation:
λx ∼ gx3 ,

µ2eff ∼ gx3 T 2 ,

T ∼ ϕc .

(3.61)

For the scaling adopted above, the derivative expansion expanded in powers of √
kfield /Λ, where
the characteristic momentum scale associated with field variations is kfield ∼ V ′′ ∼ g 3/2 ϕc ,
and the cutoff scale Λ is set by the non-zero Matsubara modes, Λ ∼ 2πT . Hence,
g 3/2
kfield
∼ x ≪ 1,
Λ
2π

(3.62)

ensuring that the derivative expansion is well controlled in the high-temperature regime.
In practice, our parameter scan shows that a high-temperature phase transition can also
occur for λx ≪ gx3 . In this case, the nucleation temperature Tn can lie well below Tc , while
the high-temperature expansion with mA′ /Tn ≪ 1 remains reasonably applicable.
With the thermal corrections, the corrected field-dependent masses become
m2A′ = gx2 ϕ2c ,

m2A′0 = ξgx2 ϕ2c ,

m2c = ξgx2 ϕ2c ,

m2hx = −µ2eff + 3λx ϕ2c ,
m2G = −µ2eff + λx ϕ2c + ξgx2 ϕ2c .
3

(3.63)
(3.64)
(3.65)

The full thermal potential can be effectively written as
V (ϕ, T ) = D(T 2 − T02 )ϕ2 − ET ϕ3 +

λx 4
ϕ ,
4

(3.57)

where T0 is the temperature at which ϕ = 0 is no longer a local minimum. At the critical temperature Tc ,
V ′ (ϕ, Tc ) = 0 ,

V (ϕ, Tc ) = V (0, Tc ) ,

(3.58)

E2 2
T ,
λx c

(3.59)

which solve to
ϕc =

2E
Tc ,
λx

D(T 2 − T02 ) =

at Tc .

Plugging in back to the potential Eq. (3.57) we find all three terms are the same parametric size ∼ E 4 Tc4 /λ3x .
At Tn which lies just slightly below Tc , relation Eq. (3.59) approximately holds and thus
ϕc
2E
≈
∼ O(1) .
Tn
λx
In gauge theory, E ∼ gx3 and thus λx ∼ gx3 .

18

(3.60)

## PDF page 19

Using the power counting introduced in Eq. (3.61), the leading-order effective potential
is obtained as
µ2x 2 λx 4 T 2 2
ϕ + ϕc +
(m + 3m2A′ + m2G − m2c )
2 c
4
24 hx
]
T[ 3
−
2mA′ + (m2A′ + ΠA′ )3/2
12
(
)3/2 ]
1
λx
g3 T [
= − µ2eff ϕ2c + ϕ4c − x 2ϕ3c + 31 T 2 + ϕ2c
.
2
4
12π

VgHT
=−
3
x

(3.66)

To evaluate the next-to-leading order contribution, we first examine the Coleman-Weinberg
potential, c.f., Eq. (3.6),
VCW = F (m2hx ) + 3F (m2A′ ) + F (m2G ) − F (m2c ) ,
where

(3.67)

m2i
m4i
log 2 − Ci .
(3.68)
64π 2
Λ
Among these terms, the gauge-independent contributions are F (m2hx ) ∼ O(gx6 ) and F (m2A′ ) ∼
O(gx4 ). We then perform a Taylor expansion f (x) = f (a) + f ′ (a) (x − a) + · · · around m2c ,
and we obtain
F (m2G ) − F (m2c ) ≃ F ′ (m2c ) (m2G − m2c ) ∼ ξ O(gx5 ) ,
(3.69)
(

F (m2i ) ≡

)

where F ′ (m2c ) ∼ O(m2c ). The remaining terms of the effective potential are
−

]
T [ 2
(mhx + Πhx )3/2 + (m2G + ΠG )3/2 − m3G + m3G − m3c ,
12π

(3.70)

where the first two 3/2-power terms arise from daisy resummation, while the two underlined
terms originate from the high-temperature expansion of the bosonic thermal function JB ,
c.f., Eq. (3.9). The term (m2hx + Πhx )3/2 ∼ O(gx9/2 ) is of higher order in the power counting
than O(gx4 ) and is therefore neglected. The gauge-dependent part is evaluated as
(m2G + ΠG )3/2 − m3c =

1
−µ2eff + λx ϕ2c + ξgx2 ϕ2c + λx T 2

(

)3/2

4

(

≈ −µ2eff + λx ϕ2c + ξgx2 ϕ2c

)3/2

(

− ξgx2 ϕ2c

(

− ξgx2 ϕ2c

)3/2

∼

√

)3/2

ξ O(gx4 ) ,

(3.71)

where m2c = ξgx2 ϕ2c is much larger than −µ2eff +λx ϕ2c + 14 λx T 2 , for ξ ≳ gx . For the limit ξ ≪ gx ,
the gauge-dependent contribution becomes negligible. In either case, this contribution is
counted as a second-order effect and is therefore included in the O(gx4 ) potential, Vgx4 .
Therefore, the next-to-leading order potential is written as
(
)
m4A′
m2A′
5
0
Vgx4 = 3
log 2 −
−
2

64π

Λ

6

)
T ( 3
mG − m3c .
12π

(3.72)

It was pointed out in [37] that, under a specific choice of power counting, certain higherloop diagrams can yield sizable contributions. In particular, diagrams containing transverse
photon loops along a scalar propagator do not increase the overall parametric order of the
19

## PDF page 20

amplitude, and therefore may contribute as the same order as lower-loop terms. These
contributions can be summed by replacing the tree-level Goldstone mass with a dressed
mass [37],
HT
1 ∂Vgx3
(3.73)
m2G → m̃2G ≡
+ ξgx2 ϕ2c .
ϕc ∂ϕc
After the substitution, the subleading potential is written as
(
)
m4A′
m2A′
5
0
Ṽgx4 = 3
log 2 −
−
2

)
T ( 3
m̃G − m3c
64π
Λ
6
12π √
)
[
(
)]
√
4 (
2
mA′
mA′
T gx ϕc ξ
gx3 T
5
2
2
1 2
2
≃3
log 2 −
−
−µeff + λx ϕc −
2ϕc + 3 T + ϕc . (3.74)
64π 2
Λ
6
8π
4π

For nucleation-related observables, one typically requires higher accuracy than that provided by the leading-order barrier alone. The next-to-leading order (NLO) effective potential
is derived within a three-dimensional finite-temperature effective field theory (EFT) framework. The three-dimensional effective potential is computed in a constant background field
ϕ3 using three-dimensional perturbation theory: the leading-order piece is the tree-level potential plus the leading three-dimensional one-loop contributions, while the NLO piece consists of the relevant two-loop vacuum diagrams in the three-dimensional EFT together with
the corrections induced by NLO-matched parameters. After renormalization and consistent
power counting, one arrives at [43, 44]
√ [
(
)]
√
ξ
gx3 T
T
g
ϕ
x
c
2
2
HT
1 2
2
−µeff + λx ϕc −
2ϕc + 3 T + ϕc
Vgx4 = −
8π
4π
( 2 2)
( 2 1 2
)]
[
4gx ( 3 T + ϕ2c )
1 4 2 2 3
1
4gx ϕc
+
g T ϕc − + ln
+ ln
,
(3.75)
(4π)2 x
2
Λ2
2
Λ2
which will be used for the high-temperature phase transition analysis in the following sections.
With the above discussion, the gauge-independent effective action can be thus constructed. The effective potential and the field renormalization factor are expanded in powers
of the coupling gx as
HT
Veff
= VgHT
+ VgHT
+ O(gx9/2 T 4 ) ,
3
4
x
x

Z = 1 + Zgx + O(gx3/2 ) ,

(3.76)
(3.77)

where Zgx is given in [39] as
22
ϕ2c
gx T
− +(
Zgx =
)3/2 .
48π
ϕc
1 2
2
T +ϕ
[

]

3

(3.78)

c

The leading-order potential Vgx3 , c.f., Eq. (3.66), is manifestly gauge-independent, and the
corresponding bounce solution ϕb satisfies
∣

∂Vgx3 ∣∣
∇ ϕb =
∣
,
∂ϕc ∣ϕc =ϕb
2

ϕb (∞) = 0 ,
20

ϕ′b (0) = 0 .

(3.79)

## PDF page 21

The nucleation rate then takes the form
HT

HT

Γ = A e−(S0 +S1 )/T ,
ˆ
[
]
1
HT
3
HT
2
S0 = d x Vgx3 (ϕb ) + (∂i ϕb ) ,
2
ˆ
[
]
1
2
S1HT = d3 x VgHT
Z
(∂
ϕ
)
.
4 (ϕb ) +
g
i b
x
2 x

(3.80)
(3.81)
(3.82)

The leading order effective action is gauge-independent, since the leading order effective
potential Vgx3 is constructed to be ξ-independent.
To analyze the gauge dependence of Vgx4 and S1 , we employ the finite-temperature Nielsen
identity and expand its coefficients
C = Cgx + O(gx3/2 ) ,

D, D̃ = O(gx−1 ) ,

(3.83)

which yields
∂VgHT
3
x

∂VgHT
4
x

= −Cgx
,
(3.84)
∂ξ
∂ϕc
∂Zgx
∂Cgx
ξ
= −2
,
(3.85)
∂ξ
∂ϕc
√
where the leading coefficient Cgx = ξgx T /(16π) [39] is independent of the background field
ϕc , i.e., ∂Cgx /∂ϕc = 0. Together with the gauge-independent renormalization factor Zgx
in Eq. (3.78), such that ∂Zgx /∂ξ = 0, they ensure consistency with the Nielsen relation in
Eq. (3.85). Finally, applying Gauss’s theorem and the asymptotic behavior of ϕb , one arrives
ξ

ˆ

[ ∂V HT

1 ∂Zgx
dx ξ
+ ξ
(∂i ϕb )2
∂ξ
2 ∂ξ
ˆ
[
]∣∣
∂VgHT
3
∣
3
x
= d x −Cgx
+ 0 ∣∣
∂ϕc
ϕc =ϕb
ˆ
= −Cgx d3 x ∇2 ϕb
ˆ
= −Cgx d2 S ∂ϕb

∂S HT
ξ 1 =
∂ξ

3

gx4

= 0.

]

(3.86)

In the high-temperature regime, Eqs. (3.84) and (3.85) are satisfied explicitly by the analytic
expressions given above, demonstrating that the resulting high-temperature effective action
is analytically gauge-independent.
3.2.4

Phase transition at low temperatures (T ≪ mA′ )

The supercooled phase transition typically takes place at Tp ≪ mA′ . In this regime, the
nontrivial temperature-dependent contributions relevant to the transition are generally subdominant to the pure field-dependent terms, since Tp ≪ ϕc (Tp ) ∼ vx . In this case, however,
21

## PDF page 22

unlike in the high-temperature regime, the low-temperature thermal contribution does not
admit a well-defined analytic expansion in the small parameter T /m. Moreover, the thermal
effects are significant only when the field value approaches zero. The basic strategy is therefore to treat the thermal corrections as small perturbations added to the zero-temperature
effective potential, as was done in [34].
Unlike the zero-temperature toy setup with a positive Higgs mass term, a minimal gauged
U (1) Higgs sector contains the standard tachyonic mass-squared term. In the supercooled
regime, thermal effects, although being small since Tp ≪ vx , can lift the effective mass term
positive and thereby create and maintain a false vacuum at ϕ = 0, as long as the tachyonic
mass-squared parameter µ2x is parametrically small.
In addition to turning the effective mass term positive, a successful supercooled phase
transition requires thermal effects to generate a local barrier near ϕ = 0. This barrier
arises from the one-loop thermal contribution together with daisy resummation, through the
thermal cubic term ∼ T ϕ3 . Although this term is parametrically suppressed in the lowtemperature regime since Tp ≪ vx , it can still induce a barrier in the vicinity of ϕ = 0,
where Tp ∼ gx ϕ. Consequently, the thermally generated barrier peaks at field values of order
ϕbarrier ∼ Tp /gx in the supercooled phase transition.
The thermal cubic term ∼ T ϕ3 responsible for generating the barrier is loop induced
and is parametrically suppressed, especially in the low-temperature regime. For this term to
compete with the quartic contribution, the quartic coupling λx must itself be loop sized. In
particular, λx should not exceed the size implied by the Coleman-Weinberg contribution:

which implies

m4 ′
m2 ′
λx 4
ϕ ≲ A2 log A2 ,
4
64π
Λ
(

(3.87)

)

gx4
λx ≲ O
.
(3.88)
16π 2
For this scaling, the characteristic momentum scale associated with spatial variations of
the background field can be estimated as

gx2
ϕwall ,
(3.89)
4π
whereas the heavy scale that has been integrated out is set by the mass of the U (1)x gauge
boson, Λ ∼ gx ϕwall . This implies
kfield
gx
∼
≪ 1,
(3.90)
Λ
4π
and thus the derivative expansion remains parametrically controlled in the low-temperature
regime, even in the ϕ → 0 region.
Thus for the supercooled phase transition, we use the scaling [34] to organize the fielddependent terms in the effective potential
kfield ∼

√

λx ϕwall ∼

µ2x ∼ gx4 ϕ2c ,

λx ∼ gx4 ,

(3.91)

For the thermal contributions, as T → 0, the daisy contribution scales as Vdaisy ∼ T ϕ3c ,
while the one-loop thermal contribution is further suppressed exponentially,
(

T4
m2
J
B
2π 2
T2

)

∼ T 4 e−m/T .
22

(3.92)

## PDF page 23

Therefore, away from the barrier region, thermal effects are generally negligible because
T ≪ ϕc (T ), and all thermal contributions can be safely neglected relative to the purely
field-dependent terms.
Nevertheless, thermal effects are essential for generating the barrier around ϕ ∼ Tp /gx ,
enabling the supercooled phase transition. In the vicinity of ϕ ∼ Tp /gx , the temperaturedependent contributions can be comparable to the field-dependent terms. We therefore retain
all thermal contributions in both the leading and subleading orders of effective potentials.
Consequently, the leading and subleading order effective potentials are thus written as
(
)
m4A′
m2A′
5
µ2x 2 λx 4
LT
log 2 −
Vgx4 = − ϕc + ϕc + 3
2

2

4

64π

Λ[
6
( 2 )
( 2 )]
4
mhx
T
mA′
hx
3
3
+ Vdaisy (T ) + Vdaisy (T ) + 2 JB
,
+3J
B
2π
T2
T2
)
)
(
(
m4c
m4G
m2G 3
m2c
3
LT
Vgx6 =
−
log 2 −
log 2 −
64π 2
Λ
2 [ 64π 2
Λ
2
( 2 )
( 2 )]
4
T
m
m
G
c
G
+ Vdaisy
(T 3 ) + 2 JB
− JB
,
2
2
2π
T
T
Z (ϕc ) = 1 + Zgx2 (ϕc , T = 0) + δZgx2 (ϕc , T ) + O(gx4 ) ,
A′

(3.93)

(3.94)
(3.95)

where we incorporate the gauge-independent thermal contributions into the leading order effective potential, while the ξ-dependent thermal terms are assigned to the subleading effective
potential.
The bounce solution is obtained by solving
∣
∂VgLT
4
x ∣
∣

∇ ϕb =
2

∣

∂ϕc ∣ϕc =ϕb

,

ϕb (∞) = 0 ,

ϕ′b (0) = 0 ,

(3.96)

and the nucleation rate is
LT

LT

Γ = A e−(S0 +S1 )/T ,
ˆ
]
[
1
2
LT
3
LT
S0 = d x Vgx4 (ϕb ) + (∂i ϕb ) ,
2
ˆ
[
]
1
2
2
(ϕ
)
+
(∂
ϕ
)
,
S1LT = d3 x VgLT
Z
6
b
i b
g
x
2 x

(3.97)
(3.98)
(3.99)

where all terms in S0 are ξ-independent. The Nielsen identities are analogous to the zerotemperature case as
ξ
ξ

∂VgLT
4
x
∂ξ
∂VgLT
6
x

= 0,
= −Cgx2

(3.100)
∂VgLT
4
x

∂ξ
∂ϕc
∂Zgx2
∂Cgx2
ξ
= −2
.
∂ξ
∂ϕc
23

,

(3.101)
(3.102)

## PDF page 24

where Zgx2 and Cgx2 are given in Eqs. (3.42)–(3.43), as in the zero-temperature analysis. Using
the identities above, we obtain
ˆ
]
[ ∂V LT
∂S1LT
1 ∂Zgx2
gx6
3
2
ξ
= dx ξ
+ ξ
(∂i ϕb )
∂ξ
∂ξ
2 ∂ξ
ˆ
]∣∣
[
∂VgLT
2
4
∂C
g
2
3
x
x
+
(∂i ϕb ) ∣∣
= − d x Cgx2
∣
∂ϕc
∂ϕc
ϕc =ϕb
∣
ˆ
[
]
LT
∣
∂Vgx4
3
= − d x Cgx2
+ (∂i Cgx2 ) (∂i ϕb ) ∣∣
∣
∂ϕc
ϕc =ϕb
∣
ˆ
[ ∂V LT
]∣
gx4
∣
= − d3 x Cgx2
− ∇2 ϕb ∣∣
∂ϕc
ϕc =ϕb
= 0,

(3.103)

demonstrating that the subleading effective action S1 is gauge invariant.
In practice, once the thermal contributions are included, Eq. (3.101) is still satisfied
to a good approximation. The subleading effective action S1LT is shown numerically to be
approximately gauge-independent.
3.2.5

Comments and discussions

Regarding gauge-independent treatments of the finite-temperature effective potential and
their use in gravitational wave calculations, a few practical points are worth recording:
• The power counting rule: For the high-temperature phase transition analysis in [39,
43, 44], the Higgs quartic coupling is taken to scale as λx ∼ gx3 . More precisely, it is
assumed to lie in the region gx4 ≪ λx ≪ gx3 [3].4 In our parameter scan, we find that all
viable high-temperature phase transitions satisfy λx ≲ gx3 , while in many cases λx ≪ gx4 .
This typically occurs for benchmark points in which Tn lies somewhat below Tc , while
the high-temperature approximation mA′ /Tn ≪ 1 remains reasonably valid.
Nevertheless, adopting the scaling λx ∼ gx3 to organize the leading and subleading
terms in the potential does yield a gauge-independent effective action, as can be verified
4

For high-temperature phase transitions, one expects
gx ϕc
gx ϕc
∼
≪ 1.
Tn
Tc

(3.104)

Using the thermal effective potential in Eq. (3.57), one finds at Tc ,
ϕc
2E
g3
∼
∼ x.
Tc
λx
λx

(3.105)

Substituting this into the previous condition gives
gx

ϕc
g4
∼ x ≪ 1.
Tc
λx

(3.106)

Hence, a consistent high-temperature phase transition typically requires λx ≫ gx4 , implying that, for fixed
λx , moving deeper into the high-temperature regime favors smaller values of gx .

24

## PDF page 25

analytically using the Nielsen identity. However, alternative scalings, e.g., λx ∼ gx4 , do
not yield a consistent result, as the Nielsen identity is not satisfied at the corresponding
order, and thus the resulting subleading effective action is not gauge-independent.
What, then, is the role of the power counting? In our view, it provides a systematic
organization of the calculation: it singles out the leading contributions that determine
the bounce solution, treats subleading terms as controlled corrections, and consistently
discards higher-order terms in the gauge coupling gx .
• Gauge-parameter dependence: In the gauge-independent treatment, one must ensure that the terms neglected from the full effective potential are indeed parametrically
small. Since some of the omitted contributions scale as ∼ ξ n g higher powers , the gauge
parameter ξ cannot be taken arbitrarily large. Otherwise the power counting scheme
ceases to be reliable and the expansion breaks down, even if the Nielsen identity is
satisfied up to subleading order in the effective potential. In practice, we find that
the gauge-independent treatment remains valid for moderately small values of ξ, e.g.,
ξ ≲ O(1 − 10).
• Solving for the bounce: A central step in our gravitational wave analysis is to
determine the bounce solution associated with the finite-temperature effective potential.
In the usual (gauge-dependent) approach, one typically works in the Landau gauge and
solves for the bounce using the full effective potential evaluated at ξ = 0. By contrast,
in the gauge-independent treatment one computes the bounce using the leading-order
potential V0 , which is explicitly ξ-independent. For this procedure to be self-consistent,
the theory must remain in the weak-coupling regime, αx ≪ 1, such that the subleading
contribution V1 does not significantly distort the bounce solution determined from V0 .
In practice, we enforce this by restricting the Monte Carlo scan to gx < 0.7. A more
accurate treatment would therefore require solving for the bounce using the full thermal
effective potential, which we leave for future work.
• Comments on the low-temperature analysis: Our scan indicates that a supercooled phase transition typically favors a moderately large gauge coupling,5 e.g.,
gx ≳ 0.5, in sharp contrast to the high-temperature case, where smaller gx is generally
preferred, c.f, Eq. (3.106). This trend can be understood from two main considerations.
First, as discussed in the previous section, the low-temperature barrier is generated by
the thermal cubic term ∼ T ϕ3 near ϕ = 0, whose coefficient scales as E ∝ gx3 . A larger
gx therefore enhances the cubic term and makes it easier to develop a sufficiently strong
5

A conformal U (1) Higgs sector typically contains no tree-level ϕ2 term. The local minimum at the origin
is instead stabilized by the finite-temperature thermal mass. In this setup, a potential barrier can arise
even without relying on the thermal cubic contribution ∼ T ϕ3 , and may be generated predominantly by the
Coleman-Weinberg potential. As a result, the allowed range of the gauge coupling gx can be more flexible
than in the conventional Higgsed U (1) case with a tachyonic mass term. Moreover, conformal U (1) models
naturally admit shallow potentials, and it is therefore common to find Tn,p ≪ v and α ≳ 1, corresponding
to strong supercooled phase transitions that yield enhanced gravitational wave signals with peak frequencies
shifted to lower bands [10,21,31,52,54,63,80]. Hence conformal hidden sectors are often discussed as natural
pathways to nanohertz band signals.

25

## PDF page 26

barrier for the supercooled phase transition.6
Second, the tree-level tachyonic mass term must be lifted to an effective positive value
by thermal mass corrections proportional to gx2 in order to create and stabilize a local
minimum at ϕ = 0. A larger gx thus keeps the symmetric point ϕ = 0 metastable down
to lower temperatures, delaying the loss of metastability, which is essential for realizing
a supercooled transition.

4

Gravitational waves from first-order phase transition

In a U (1) gauge theory, the finite-temperature effective potential can induce a first-order
phase transition and consequently generate a stochastic gravitational wave background. In
this section, we review the standard computation of the gravitational wave signal, starting
from the nucleation rate inferred from the bounce solution for a given set of model parameters.

4.1

The tunneling action and transition rate

As the temperature falls below the critical temperature Tc , the effective potential may develop two local minima separated by a barrier, rendering the minimum in the symmetric
phase metastable. The transition from the false vacuum to the true vacuum then proceeds
via bubble nucleation. The resulting bubbles expand and collide, sourcing a stochastic gravitational wave background. At finite temperature, the bubble nucleation rate, also referred
to as the transition rate or the false vacuum decay rate, is given by [78, 79]
Γ(T ) = A(T ) e−S3 (T )/T ,

(4.1)

where S3 (T ) ≡ S3 (ϕb , T ) is the three-dimensional Euclidean action evaluated on the O(3)
symmetric bounce configuration. The action is defined as
ˆ ∞
[
]
(4.2)
S3 (ϕ, T ) =
d3 x 12 (∇ϕ)2 + Ṽeff (ϕ, T ) ,
0

with Ṽeff (ϕ, T ) ≡ Veff (ϕ, T ) − Veff (ϕFV , T ) the free energy density shifted relative to the false
vacuum. The bounce ϕb satisfies the equation of motion
d2 ϕ 2 dϕ
∂
+
=
Ṽeff (ϕ, T ) ,
dr2
r dr
∂ϕ

(4.3)
∣

and subjects to the boundary conditions ϕ(r → ∞) = 0 and dϕ/dr∣∣ = 0, with r2 = x2 . In
r=0
this work the solution is obtained using CosmoTransitions [81].
6

The effective thermal potential in Eq. (3.57) is derived in the high-temperature limit, where the JB
functions admit a high-temperature expansion. In the low-temperature regime, Eq. (3.57) remains applicable
in the field range ϕ ≲ Tp /gx . In particular, as ϕ → 0 the field value is again much smaller than the
temperature, and thus the high-temperature expansion remains valid in this small-field region, which is the
most relevant for generating a thermal barrier. Nevertheless, Eq. (3.57) should not be used indiscriminately
across the full temperature range in analyses of supercooled phase transitions.

26

## PDF page 27

The prefactor A(T ) is given by [82]
S3 (ϕb , T )
A(T ) = T
2πT
[

[
] −1/2
]3/2 
 det′ −∇2 + V ′′ (ϕb , T ) 
[
]
,
 det −∇2 + V ′′ (ϕ , T ) 

(4.4)

FV

where det′ denotes the functional determinant with zero eigenvalues omitted. For dimensional
consistency, A(T ) is commonly approximated as [82]
[

A(T ) ≃ T

4

S3 (ϕb , T )
2πT

]3/2

(4.5)

.

The false vacuum fraction Pf is introduced to track the progress of the phase transition,
written as [83, 84]
]
[
(4.6)
Pf (t) = exp −Vtext (t) ,
where Vtext (T ) denotes the fractional extended volume occupied by true vacuum bubbles at
time t, given by
ˆ
4π t ′
a3 (t′ )
ext
Vt (t) =
dt Γ(t′ ) 3 R3 (t′ , t) ,
(4.7)
3 tc
a (t)
with

ˆ t
R(t , t) =
′

t′

dt′′ vw

a(t)
,
a(t′′ )

(4.8)

in which an initial bubble radius is often neglected and the bubble wall velocity vw is assumed
to remain constant throughout the expansion. Thus Eq. (4.7) becomes
4π 3
Vtext (t) =
v
3 w

4.2

ˆ t

a(t′ )
dt′ Γ(t′ )
a(t)
tc
[

]3 [ˆ t

a(t)
dt′′ ′′
a(t )
t′

]3

.

(4.9)

Characteristic temperatures

To analyze the transition dynamics and predict the resulting gravitational waves, we introduce several benchmark temperatures that characterize key stages of the phase transition.
Critical temperature Tc The critical temperature Tc is defined as the temperature at
which the effective potential of the true and false vacua become degenerate, Veff (ϕTV , Tc ) =
Veff (ϕFV , Tc ), with a potential barrier separating the two minima.
Nucleation temperature Tn The nucleation temperature Tn is the temperature at which
bubbles of the broken phase begin to form in the false vacuum at an appreciable rate, signaling
the onset of efficient nucleation. It is defined when one bubble is nucleated within one Hubble
volume per Hubble time
ˆ tn
Γ
dt ≃ 1 ,
(4.10)
3
tc H

27

## PDF page 28

where Γ is the bubble nucleation rate and H is the Hubble parameter including the vacuum
energy contribution, given by
1 π2
ρrad + ρvac
=
g∗ T 4 + ∆Veff (T ) ,
H =
2
2
3MPl
3MPl
30
[

2

]

(4.11)

where ∆Veff = Veff (ϕFV , T ) − Veff (ϕTV , T ), g∗ is the effective number of relativistic degrees of
freedom including both the SM and hidden sectors, and MPl = 2.4 × 1018 GeV denotes the
reduced Planck mass.
Given the temperature dependence of both Γ(T ) and H(T ), it is convenient to express the
nucleation condition as a function of temperature [85]. Assuming an adiabatically expanding
Universe, the conservation of entropy per comoving volume implies
]
ds
d[
s(t)a3 (t) = 0 ⇒
= −3H(t)s(t) ,
dt
dt

(4.12)

where s is the entropy density of the plasma and a is the scale factor. The entropy density
is written as
∂p
∂V
s(T ) =
=−
,
(4.13)
∂T
∂T
which can be combined with Eq. (4.12) and obtain

yielding

dT ∂ 2 V
∂V
dT ds
=−
= 3H(T )
,
2
dt dT
dt ∂T
∂T

(4.14)

dT
∂T V
= −3H(T )
,
dt
∂T T V

(4.15)

2

where the derivatives ∂T V = ∂V
and ∂T T V = ∂∂TV2 are evaluated at the false vacuum. In the
∂T
literature, the MIT bag equation of state [86] is often employed, in which the false vacuum
potential is parameterized as
V (ϕFV , T ) = aT 4 + b ,
(4.16)
with a, b being temperature-independent coefficients. This bag model simplifies Eq. (4.15) to
the familiar form
dT bag
= −H(T )T ,
(4.17)
dt
and the nucleation condition defined by Eq. (4.10) can then be rewritten as
ˆ Tc

Γ(T ) 1
dT ≃ 1 .
4
Tn H(T ) T

(4.18)

When the phase transition occurs near the electroweak scale, the nucleation condition in
Eq. (4.18) can be well approximated by S3 (Tn )/Tn ≃ 140.
For a high-temperature phase transition, the nucleation temperature Tn typically lies only
slightly below Tc and marks the onset of the transition. This is not the case for a supercooled
phase transition, where the onset is instead characterized by the percolation temperature Tp .
28

## PDF page 29

Percolation temperature Tp The percolation temperature Tp is the temperature at which
bubbles have nucleated and grown enough that they percolate through space.
For a fast phase transition, the nucleation temperature Tn is sufficient to characterize
both the onset and completion of the transition. However, a slow or supercooled transition
is long lasting, during which the Universe can remain trapped in the false vacuum for an
extended period after it becomes metastable, delaying bubble collision to the temperature
much lower than Tn . In such case, Tp provides a more accurate description of the transition
dynamics and is supposed as the reference temperature for gravitational wave calculations,
particularly for the strong supercooling in which Tp ≪ Tn [50].
The percolation temperature Tp is defined by roughly 70% of the Universe remains in the
false vacuum, Pf (Tp ) ≈ 0.7 [48, 87]. In Eq. (4.9), the ratio of scale factors at different times
is given by
[ˆ t1
]
a(t1 )
= exp
dt′ H(t′ ) .
(4.19)
a(t2 )
t2
Assuming an adiabatic expansion and adopting the MIT bag equation of state, this ratio can
be recast as a function of temperature
(ˆ T2
)
a(T1 )
1
T2
= exp
,
(4.20)
dT ′ ′ =
a(T2 )
T
T1
T1
leading to

4π
Pf (T ) = exp − vw3
3
{

ˆ Tc

Γ(T ′ )
dT ′4
T H(T ′ )
′

T

[ˆ T ′
T

dT ′′ 3
.
H(T ′′ )
] }

(4.21)

To ensure the phase transition completes successfully, two conditions must be checked [60,
85]: (1) the transition has an end temperature Te , defined by Pf (Te ) = ε ≲ 0.01; (2) the
physical volume of the false vacuum Vphys (t) = a3 (t)Pf (t) decreases with time,
dVphys
d
= Vphys
ln Pf (t) + 3H(t) ≤ 0 ,
dt
dt
[

]

(4.22)

giving rise to

dVtext
+ 3 ≤ 0,
dT
and this condition should be verified at both Tp and Te .
T

(4.23)

Reheating temperature Treh A first-order phase transition releases latent heat and can
reheat the plasma from the percolation temperature Tp to a reheating temperature Treh .
Assuming instantaneous reheating, Treh is estimated by
]1/4

[

Treh ≃ 1 + α(Tp )

Tp ,

(4.24)

where α(T ) is the transition strength at temperature T . For moderate supercooling (α ≲ 1),
one has Treh ≈ Tp ; whereas for strong supercooling (α ≫ 1), the reheating temperature can
be significantly higher than Tp , or even higher than Tc [60]. The present gravitational wave

29

## PDF page 30

amplitude and frequency are obtained by redshifting their values from the reheating temperature Treh rather than from Tp down to today.
To summarize this subsection, as the Universe cools, the dark U (1)x sector undergoing a
supercooled phase transition may pass through the following characteristic temperatures,
Tc > Tn ≫ Tp ≳ Te ≳ T0 ≳ 0 .

(4.25)

Recall that T0 is defined as the temperature at which ϕ = 0 ceases to be a local minimum.
In a typical supercooled phase transition, Tp , Te , and T0 are close to one another.

4.3

Hydrodynamic parameters

The gravitational wave signal originating from a first-order phase transition depends sensitively on the characteristic length scale L∗ , which represents the typical scale carrying most
of the released energy. A common estimate identifies L∗ with the mean bubble separation
R∗ , which is
(8π)1/3
R∗ =
vw ,
(4.26)
β
where vw is the bubble wall velocity and β is the inverse time scale, defined as
d S3
β=−
dt T
(

)∣∣
∣
∣
∣

d S3
= H(T )T
dT T
t=tp
(

)∣∣
∣
∣
∣

,

(4.27)

T =Tp

which corresponds to an exponential nucleation rate and is usually expressed in the following
form
( )∣
β
d S3 ∣∣
.
(4.28)
=T
∣
Hp
dT T ∣T =Tp
For strong supercooled phase transitions, β may become tiny or even negative, indicating the
commonly exponential approximation breaks down. In this case, the mean bubble separation
R∗ should instead be directly determined from the bubble number density
[

]−1/3

R∗ (T ) ≡ n(T )

[

= T

ˆ Tc
T

]−1/3
′
′
′ Γ(T )Pf (T )
dT
.
T ′4 H(T ′ )

(4.29)

The strength of the phase transition is parameterized by α, defined as [88, 89]
α≡

θ̄f (Tp ) − θ̄t (Tp )
,
3wf (Tp )

θ̄ ≡ e −

p
,
c2s,t

(4.30)

where wf denotes the enthalpy density in the false vacuum, θ̄ represents the pseudotrace
that is a generalization of the vacuum energy, and c2s is the speed of sound in the plasma.
Subscripts f and t refer to quantities in the false and true vacua respectively. The hydrodynamics of the plasma is described by the energy density e, pressure p, and enthalpy density
w. The plasma is usually modeled as a perfect relativistic fluid, for which the pressure is
30

## PDF page 31

related to the free energy density F by p = −F. Since F equals to the effective potential,
one has p = −Veff . The relevant thermodynamic quantities are given by
p ≡ −Veff (ϕc , T ) +
∂p
− p,
∂T
∂p
w≡T
= p + e,
∂T
δp
∂p/∂T
≃
,
c2s ≡
δe
∂e/∂T

π2
geff (T )T 4 ,
90

e≡T

(4.31)
(4.32)
(4.33)
(4.34)

where the second term in p accounts for the field-independent contribution from all relativistic
particle species in thermal equilibrium with the dark Higgs hx at temperature T [89].
During the phase transition, the released energy accelerates bubbles, while the interaction
between bubble walls and the surrounding plasma impedes the acceleration. When the
released energy is sufficiently large to overcome this friction, the wall continues to accelerate
without reaching a terminal velocity, entering a runaway regime. The corresponding criterion
parameter is defined as [90]
∑
1 i gi ci ∆m2i Tp2
α∞ ≡
,
(4.35)
18
wf (Tp )
where ci = 1 (1/2) for bosons (fermions), gi denotes the internal degrees of freedom of particle
i and ∆m2i = m2i,t − m2i,f with the sum running over all species that gain a mass during the
transition. If α > α∞ , the bubble wall runs away, yielding vw ≃ 1. In the non-runaway regime
(α < α∞ ), the wall eventually reaches a model-dependent terminal velocity. We compute the
wall velocity vw (α, c2s,f , c2s,t , Ψ), where Ψ ≡ wt /wf denotes the ratio of the enthalpy densities
in the true and false phases, following [91, 92].
Kinetic energy fraction is defined as K ≡ ρfl /ep which quantifies the fraction of available
vacuum energy converted into bulk motion of the plasma, where ep is the total energy density
at the percolation temperature Tp , and ρfl is the plasma kinetic energy density, obtained by
integrating over the fluid profile. The kinetic energy fraction can be further parameterized
as
α
(4.36)
κ(α, c2s,f , c2s,t , vw ) ,
K≃
1+α
where κ represents the efficiency factor, determined by the transition strength, sound speeds
in two phases and wall velocity, with detailed calculations provided in [88, 89].

4.4

Gravitational wave power spectrum

The gravitational wave power spectrum is defined as
ΩGW (f ) ≡

1 dρGW
,
ρc d log f

(4.37)

where f denotes the frequency and ρc is the critical density. The total gravitational wave
signal typically receives three primary contributions: (1) bubble collisions of the scalar field;
31

## PDF page 32

(2) sound waves in the bulk plasma; (3) magneto-hydrodynamic turbulence in the plasma [93–
95]. Accordingly,
h2 ΩGW (f ) = h2 Ωϕ (f ) + h2 Ωsw (f ) + h2 Ωtb (f ) ,
(4.38)
with each component parametrized as
h2 Ω(f ) = h2 Ωpeak S(f ) ,

(4.39)

where Ωpeak is the peak amplitude and S the spectral-shape function.
Phase transitions in a dark sector can be characterized by two strength parameters, αtot
and αh , defined as [17, 22, 25, 33],
∆θ̄(Th,p )
],
αtot = [
v
3 wf (Tv,p ) + wfh (Th,p )

αh =

∆θ̄(Th,p )
,
3wfh (Th,p )

(4.40)

where ∆θ̄ = θ̄f − θ̄t , c.f., Eq. (4.30). Here, wfv and wfh denote the false vacuum enthalpy densities of the visible and hidden sector, respectively, and Tv,p and Th,p are their corresponding
percolation temperatures. In this work, we assume that the dark sector shares the same temperature as the visible sector, Th = Tv , due to efficient interactions between the two sectors.
The total parameter αtot determines the amplitude of gravitational waves, and αh controls
the efficiency factor κ which describes the fraction of vacuum energy transformed into the
bulk kinetic energy of the plasma.
Under this framework, the runaway condition introduced in Eq. (4.35) generalizes to the
hidden sector as
∑
2
1 i gi ci ∆m2i Th,p
,
(4.41)
αh,∞ ≡
18
wfh (Th,p )
where ci = 1 (1/2) for bosons (fermions), gi is the internal degrees of freedom of particle i,
and ∆m2i = m2i,t − m2i,f . In the runaway regime (αh,∞ < αh ), efficiency factors are given by
κcol = 1 −

αh,∞
,
αh

κsw =

αh,∞
κ(αh,∞ , c2s,f , c2s,t , vw ) ,
αh

κtb = ϵκsw ,

(4.42)

where ϵ denotes the fraction of bulk motion that is turbulent. In the non-runaway regime
(αh,∞ > αh ), the factors are
κcol = 0 ,

κsw = κ(αh , c2s,f , c2s,t , vw ) ,

κtb = ϵκsw ,

(4.43)

In this work we adopt ϵ = 0.1 according to numerical simulations [96].
The present gravitational wave amplitude and frequency are obtained by redshifting their
values at production evaluated at the temperature T∗ , given by
a∗
h Ω0 (f0 ) =
a0
2

and

(

)4 (

H∗
H0

)2

(

Ω1 (f∗ ) = 1.67 × 10

−5

a∗
geff (T∗ )
f0 = f∗ = 1.65 × 10−5 Hz
a0
100
(

32

100
geff (T∗ )

)1/6 (

)1/3

Ω∗ (f∗ ) ,

(4.44)

)

T∗
,
100 GeV

(4.45)

## PDF page 33

where the subscript 0 denotes present quantities and ∗ denotes those evaluated at the time
of the gravitational wave production.
As noted in the previous section, a supercooled phase transition releases latent heat and
can reheat the plasma from the percolation temperature Tp to a reheating temperature Treh .
The present gravitational wave amplitude and frequency are therefore obtained by evaluating
the redshift factor at T∗ = Treh rather than at Tp .
The gravitational wave power spectra observed today for the three contributions are thus
given by
1. bubble collision
h2 Ωϕ (f ) = 1.67 × 10−5

0.11vw3
100
2
0.42 + vw geff (Treh )
(

)1/3 (

κcol αtot
1 + αtot

)2 (

β
H∗

)−2

Sϕ (f ) ,

3.8(f /fϕ )2.8
,
1 + 2.8(f /fϕ )3.8
)
)1/6 (
)(
)(
(
Treh
β
0.62
−7 geff (Treh )
Hz .
fϕ = 1.6 × 10
100
1 GeV H∗ 1.8 − 0.1vw + vw2

Sϕ (f ) =

(4.46)
(4.47)
(4.48)

2. sound wave
h Ωsw (f ) = 2.65 × 10 vw
−6

2

f
Ssw (f ) =
fsw
(

(

100
geff (Treh )

(

4 + 3 f /fsw

fsw = 1.9 × 10

−7

κsw αtot
1 + αtot

)2 (

β
H∗

)−1

Ssw (f ) ,

(4.49)

]7/2

7

)3 [

)1/3 (

1 geff (Treh )
vw
100
(

(4.50)

,

)2

)1/6 (

Treh
1 GeV

)(

β
Hz .
H∗
)

(4.51)

3. turbulence
h Ωtb (f ) = 3.35 × 10 vw
−4

2

(

Stb (f ) =
ftb =

f
ftb

)3 [

(

100
geff (Treh )

]11/3 (

1
(

)1/3 (

1 + f /ftb

)

κtb αtot
1 + αtot

1 + 8π

f
H∗′

)3/2

Stb (f ) ,

)−1

(4.52)
(4.53)

,

2.7
fsw ,
1.9

(4.54)

where fϕ , fsw , ftb are peak frequencies, H∗ denotes the Hubble rate at gravitational wave
production, where we take T∗ = Treh , and H∗′ is the redshifted Hubble rate, given by
H∗′ =

(

a
geff (Treh )
H∗ ≃ 1.6 × 10−5 Hz
a0
100
)

(

33

)1/6 (

Treh
.
100 GeV
)

(4.55)

## PDF page 34

Strong signals from supercooling Using the hydrodynamic parameters defined in Section 4.3 together with the gravitational wave power spectrum formulas, we summarize the
main factors by which supercooled phase transitions can generically produce stronger signals:
• From Eq. (4.30), the transition strength parameter α scales inversely with the radiation
energy density, ρrad (Tp ) ∝ Tp4 . Supercooled transitions typically have a much lower
percolation temperature Tp , and thus lead to a large α. In this regime the fraction of
energy available to source gravitational waves, κα/(1 + α), is enhanced and approaches
κ. As a result, the released vacuum energy can constitute a sizable fraction of the total
energy density, leading to substantially stronger gravitational wave signals.
• The parameter β characterizes the inverse time scale over which the nucleation rate
grows, and hence β/H controls the typical duration of the transition. In supercooled
scenarios, nucleation is delayed and then turns on rapidly, thus the transition proceeds
with larger characteristic bubble sizes; c.f., Eq. (4.26). Since gravitational waves are
sourced by anisotropic stresses on length scales of order R∗ ∼ vw /β, a smaller β/H
typically enhances the signal amplitude.
• In the strong supercooling limit, the driving pressure can be large while plasma friction
becomes relatively less important. Bubble walls may therefore become highly relativistic and can more readily approach runaway behavior. This increases the fraction
of the released energy stored in the bubble walls or in the scalar field kinetic energy,
thereby enhancing the collision- and field-sourced contributions to the gravitational
wave spectrum.
Finally, noted from gravitational wave power spectrum formulas, the peak frequency
parametrically scales as
fpeak ∝ T∗ ×

(
)
β
× redshift factors .
H∗

(4.56)

Supercooling typically implies a smaller characteristic temperature T∗ and often a smaller
β/H∗ , both of which push fpeak to lower values. Consequently, supercooled transitions are
a well-motivated and frequently studied mechanism for generating signals in the nanohertz
band.

4.5

Gauge-dependent versus gauge-independent results

In this subsection, we perform a Monte Carlo scan of the parameter space for gravitational
waves sourced by the first-order phase transition, using both a gauge-dependent treatment
in Landau gauge (ξ = 0) and the gauge-independent framework discussed in Section 3.
4.5.1

Gauge-dependent gravitational wave results

To begin, we perform a scan using the gauge-dependent finite-temperature effective potential
in Landau gauge (ξ = 0), as presented in Section 3.1. We sample 3 × 104 parameter points
in the ranges
gx ∈ [10−2 , 1], λx ∈ [10−6 , 10−1 ], vx ∈ [10−3 , 103 ] GeV .
(4.57)
34

## PDF page 35

103

10−9

LISA
TianQin ET
CE

h2 ΩGW

10−12

BBO

−15

10

1.5

LISA
TianQin ET

102

CE

10−15

BBO

10−18

U DECIGO

101
100

10−21

10−1

1.0

10−24

10−30
10−10

Taiji

10−12

10−21

10−27

µAres

10−9

2.5
2.0

U DECIGO

10−18

10−6

3.0

v x [GeV]

Taiji

h2 ΩGW

µAres

T p /mA′

10−6

10−24
NANOGrav
PPTA DR3
EPTA DR2

10−8

0.5

10−6

10−4

f [Hz]

10−2

100

10−27
10−30
10−10

102

(a)

10−2

NANOGrav
PPTA DR3
EPTA DR2

10−3
10−8

10−6

10−4

f [Hz]

10−2

100

102

(b)

Figure 1: Gauge-dependent gravitational wave signals from a Monte Carlo scan over the
parameter ranges in Eq. (4.57) using the finite-temperature effective potential in Landau
gauge (ξ = 0). Scatter points show the peak frequency and peak amplitude of the predicted
stochastic background from the first-order phase transition. Panel (a) is color-coded by the
ratio Tp /mA′ , and panel (b) by the U (1)x symmetry breaking scale vx ∈ [10−3 , 103 ] GeV. The
colored regions denote the power-law integrated sensitivities of current and future detectors,
including Taiji [97], TianQin [98], LISA [99], µAres [100], BBO [101], U_DECIGO [102],
ET [103], and CE [104]. Box plots show the PTA signals from NANOGrav [105], PPTA [106],
and EPTA [107], with dataset and plotting style following [108].
and find 6962 points for which the phase transition completes successfully. The corresponding
peak signals are shown in Fig. 1. The scatter points are color-coded by Tp /mA′ and by vx .
Although results obtained from a gauge-dependent potential do not constitute definitive
gravitational wave predictions for the U (1) dark sector, the two panels nevertheless reveal
clear trends that are instructive for understanding the underlying physics: larger symmetry
breaking scales vx shift the gravitational wave signal toward higher frequencies, while smaller
vx shift it toward lower frequencies. In our scan, the lowest peak frequencies approach the
nanohertz band with vx ≲ 100 MeV.
The temperature at which the transition occurs is also closely correlated with the signal
strength: low-temperature transitions typically yield larger amplitudes, whereas transitions
occurring at higher temperatures tend to produce much weaker signals.
To quantify the range of thermal regimes encountered in the gauge-dependent scan, we
classify the successful transition points into four categories according to the ratio Tp /mA′ ,
with the supercooled and (approximately) high-temperature regimes being the ones that can
be treated within the gauge-independent framework:
1. Supercooled phase transition: Tp /mA′ ≲ 0.2;
2. (Moderately) low-temperature phase transition: 0.2 < Tp /mA′ < 0.5;
3. Intermediate regime: 0.5 < Tp /mA′ < 2;
4. (Approximately) high-temperature phase transition: Tp /mA′ ≳ 2.
35

## PDF page 36

The number of points and the corresponding fractions in each category are summarized in
Table 1, and the overall composition is illustrated by the pie chart in Fig. 2.
Case
Supercooled: Tp /mA′ ≲ 0.2
(Approx) low-T : 0.2 < Tp /mA′ < 0.5
Intermediate: 0.5 < Tp /mA′ < 2
(Approx) high-T : Tp /mA′ ≳ 2
Total

number
2156
2083
2377
346
6962

fraction
30.97 %
29.92 %
34.14 %
4.97 %
100 %

Table 1: Statistics of successful first-order phase transition points obtained in the gaugedependent calculation (Landau gauge, ξ = 0). We sample 3 × 104 parameter points in the
ranges of Eq. (4.57) and find 6962 points for which the transition percolates successfully. The
successful points are classified by the ratio Tp /mA′ . For each category we report the number
of points and the corresponding fraction of the total sample.

High-T
4.97%
Low-T

34.14%

29.92%

Intermediate

30.97%
Supercooled

Figure 2: Pie chart showing the composition of phase transition regimes in the gaugedependent scan (Landau gauge, ξ = 0) over the parameter ranges in Eq. (4.57). The
classification is based on the ratio Tp /mA′ as defined in Table 1, which also lists the corresponding event counts and fractions.
From the statistics, we find that supercooled transitions account for roughly 30% of all
successful phase transition points. They typically yield the strongest gravitational wave
signals among the regimes considered, as shown in Fig. 1, and many lie within the projected sensitivity of near-future experiments. Moderately low-temperature transitions with
0.2 < Tp /mA′ < 0.5 constitute another ∼ 30% of the successful points. Taken together,
the supercooled and moderately low-temperature regimes are naturally and approximately,
respectively, suited to the low-temperature gauge-independent framework.
We identify an approximately high-temperature regime using the criterion Tp /mA′ ≳ 2,
which already constitutes a small subset of the successful points (below 5%). Truly hightemperature transitions for which the high-temperature expansion is parametrically justified,
Tp /mA′ ≫ 10, are rare in our scan. These points generally produce very weak signals and
are therefore difficult to detect, making them phenomenologically less compelling.
36

## PDF page 37

The remaining points lie in an intermediate regime, 0.5 < Tp /mA′ < 2, and make up about
35% of the successful sample. Their predicted signals are intermediate between the supercooled and high-temperature cases. This regime is not applicable to the gauge-independent
treatments: the high-temperature expansion is not valid, while the low-temperature thermal
contributions cannot be regarded as small corrections. Moreover, the associated gravitational
wave signals are typically below the reach of near-future detectors, rendering this region also
less phenomenologically relevant at present.
It should be noted that part of the literature adopts Eq. (3.57) as the starting point for
gravitational wave analyses and reports many viable points in the intermediate- and lowtemperature regimes. Such treatments are not appropriate. Eq. (3.57) is obtained by employing the high-temperature expansion of the JB functions, which ceases to be valid once the
high-temperature condition is no longer satisfied. Consequently, the resulting gravitational
wave spectra in regimes where the high-temperature expansion is not valid are unreliable,
regardless of gauge-dependent issues.
4.5.2

Gauge-independent gravitational wave predictions

The gauge-independent effective action in the high- and low-temperature limits is discussed in
detail in Section 3, and we scan these two regimes separately. The ranges of input parameters
are chosen as follows:
high-T : gx ∈ [10−3 , 0.7], λx ∈ [10−9 , 10−2 ], vx ∈ [10−3 , 102 ] GeV ,
low-T : gx ∈ [10−2 , 0.7], λx ∈ [10−6 , 10−2 ], vx ∈ [10−3 , 102 ] GeV .

(4.58)
(4.59)

For each regime, we sample 3 × 104 points and compute the resulting stochastic gravitational wave background. The results are displayed in the {f, ΩGW h2 } plane, where each
scatter point corresponds to the peak frequency and peak amplitude for a given parameter
set. The high-temperature scan is shown in Fig. 3, and the low-temperature scan in Fig. 4.
To illustrate the dependence on key parameters, we color-code the points by the ratio Tp /mA′
in the left panels and by vx in the right panels of Figs. 3 and 4. We recover the same qualitative trend observed in the gauge-dependent scan: larger vx typically shifts the signal toward
higher peak frequencies.
It is important to note, however, that the raw outputs of these scans include parameter points that lie outside the temperature-limit assumptions underlying the corresponding
gauge-independent treatments. In particular, the high-temperature scan contains points with
Tp /mA′ < 2, which do not satisfy the (approximately) high-temperature criterion and must
be discarded. Likewise, the low-temperature scan contains points with Tp /mA′ > 0.5, which
fall outside the (approximately) low-temperature domain and must be discarded.
To ensure consistency with the assumptions adopted in the preceding analysis, we retain
only points with Tp /mA′ ≳ 2 as belonging to the (approximately) high-temperature regime,
and points with Tp /mA′ ≲ 0.5 as belonging to the (approximately) low-temperature regime.
Within the latter, points with Tp /mA′ ≲ 0.2 correspond to genuinely supercooled transitions.
The surviving points from the two scans are combined in Fig. 5, which provides concrete,
gauge-independent predictions for the minimal gauged U (1)x dark sector.
The empty gap in Fig. 5 corresponds to the intermediate regime 0.5 < Tp /mA′ < 2, where
the high-temperature expansion is not valid and the low-temperature thermal contributions
37

## PDF page 38

10

−14

10

CE

2.5

U DECIGO

10−23
10−26
10−10

10−8

10−4

f [Hz]

10−2

100

CE
BBO

10−17

U DECIGO

100

10−1

10−20
10−23

1.0
10−6

101

ET

10−14

1.5

NANOGrav
PPTA DR3
EPTA DR2

LISA

TianQin

10

2.0

10−20

Taiji

−11

3.5
3.0

BBO

10−17

µAres
10−8

4.0

ET

TianQin

−11

h2 ΩGW

LISA

h2 ΩGW

Taiji

T p /mA′

µAres
10−8

102

10−5

4.5

v x [GeV]

10−5

10−26
10−10

102

10−2

NANOGrav
PPTA DR3
EPTA DR2

10−3
10−8

10−6

(a)

10−4

f [Hz]

10−2

100

102

(b)

Figure 3: Gauge-independent gravitational wave signals in the high-temperature regime.
Each scatter point shows the peak frequency and peak amplitude of the stochastic background
sourced by a first-order phase transition. In panel (a), points are color-coded by Tp /mA′ . In
panel (b), points are color-coded by the U (1)x symmetry breaking scale vx , scanned over
vx ∈ [10−3 , 102 ] GeV. All points with Tp /mA′ < 2 violate the high-temperature assumption
and should be discarded.

h2 ΩGW

10−14

ET
CE

0.8

U DECIGO

0.6

10−26
10−10

10−8

f [Hz]

10−2

100

101

ET
CE

100

BBO
10−1

U DECIGO

10−20

0.2
10−4

TianQin

10−17

10−23

10−6

LISA

10−14

0.4

NANOGrav
PPTA DR3
EPTA DR2

Taiji

10−11

1.2
1.0

10−20
10−23

10−8

1.4

BBO

10−17

µAres

1.6

LISA
TianQin

10−11

102

10−5

h2 ΩGW

10−8

Taiji

T p /mA′

µAres

v x [GeV]

1.8

10−5

10−26
10−10

102

(a)

10−2

NANOGrav
PPTA DR3
EPTA DR2

10−3
10−8

10−6

10−4

f [Hz]

10−2

100

102

(b)

Figure 4: Gauge-independent gravitational wave signals in the low-temperature regime.
Each scatter point shows the peak frequency and peak amplitude of the stochastic background
sourced by a first-order phase transition. In panel (a), points are color-coded by Tp /mA′ . In
panel (b), points are color-coded by the U (1)x symmetry breaking scale vx , scanned over
vx ∈ [10−3 , 102 ] GeV. All points with Tp /mA′ > 0.5 violate the low-temperature assumption
and should be discarded.
cannot be treated as small corrections. Consequently, neither the high- nor low-temperature
gauge-independent framework applies, and concrete predictions in this intermediate regime
are not currently under theoretical control. Moreover, the corresponding gravitational wave
signals are typically weaker than those from supercooled transitions and are generally below
the projected reach of near-future experiments, rendering this regime less phenomenologically
relevant at present.
To illustrate the impact of gauge dependence on the predicted gravitational wave signals,
38

## PDF page 39

0.5

µAres

Taiji

10

(f)
TianQin

−12

10

h2 ΩGW

LISA

(e)

−9

ET

0.3

CE

BBO

10−15

0.01

U DECIGO

−18

10

8

(d)

10−21

4

10−24
10−27
10−30
10−10

T p /mA′

10−6

NANOGrav
PPTA DR3
EPTA DR2

2
10−8

10−6

10−4

f [Hz]

10−2

100

102

Figure 5: Concrete gauge-independent gravitational wave predictions for the minimal gauged U (1)x dark sector, obtained by combining the physically consistent points
selected from Fig. 3 (Tp /mA′ ≳ 2) and Fig. 4 (Tp /mA′ ≲ 0.5). The gap corresponds to
the intermediate regime 0.5 < Tp /mA′ < 2, where neither the high- nor low-temperature
gauge-independent treatment is applicable. Low-temperature points are shown in blue, with
darker shades corresponding to smaller Tp /mA′ (stronger supercooling). High-temperature
points are shown in red, with darker shades corresponding to larger Tp /mA′ . Black crosses
mark three benchmark models for Case 2, for which the dark matter evolution is computed
explicitly (see Table 3), providing benchmark targets for multi-messenger searches of the corresponding U (1) model. In particular, benchmark models (e) and (f) lie within the projected
sensitivity of Taiji, TianQin, and LISA.
we explicitly compare our gauge-independent treatment with the gauge-dependent calculation
in Fig. 6. As representative examples, we consider benchmark models (e) and (f), which
undergo supercooled phase transitions, and present the resulting gravitational wave spectra
ΩGW h2 as functions of frequency. The gauge-independent predictions are shown as solid
curves. The gauge-dependent results are obtained by varying the gauge parameter over
ξ ∈ [0, 5] and are displayed as shaded bands; the dashed curves indicate the Landau gauge case
with ξ = 0. One observes substantial deviations between the gauge-independent predictions
and the gauge-dependent results.

5

Evolution of dark sector particles

A successful dark sector model should also furnish viable dark matter candidates. With the
steadily improving sensitivity of dark matter detection experiments and collider searches,
many conventional freeze-out scenarios, especially in the traditional WIMP mass range
O(10 − 100 GeV), are increasingly constrained. In large regions of parameter space, the

39

## PDF page 40

10−6

Taiji

µAres

LISA

10−9
10

h2 ΩGW

ET

TianQin

−12

BBO

10−15

CE

U DECIGO

10−18
10−21

NANOGrav
PPTA DR3
EPTA DR2
model (e)
model ( f )

10−24
10−27
10−30
10−10

10−8

10−6

10−4

f [Hz]

10−2

100

102

Figure 6: Comparison of the gauge-independent treatment with the gauge-dependent computation. Shown are the gravitational wave spectra ΩGW h2 as functions of frequency for
benchmark models (e) and (f) in the low-temperature regime. The shaded bands indicate the
gauge-dependent results obtained by varying the gauge parameter over ξ ∈ [0, 5]. Solid curves
denote the gauge-independent predictions, while dashed curves show the gauge-dependent results in Landau gauge (ξ = 0).
annihilation of dark matter into SM states,
annihilation

XX (or XX) −−−−−−−−→ SM particles ,

(5.1)

is no longer efficient enough to yield the observed relic abundance without conflicting with
existing bounds [109, 110].
Within the minimal U (1)x setup, two well-motivated possibilities arise, as discussed in
Section 2. First, the dark photon can serve as dark matter provided it is stable, which
typically requires vanishing or negligibly small kinetic mixing with the hypercharge gauge
field. In this limit its relic abundance is set by Higgs portal interactions. Second, a vectorlike
dark fermion can be the dark matter candidate, communicating with the SM predominantly
through the dark photon portal, since it does not couple directly to the dark Higgs in the
minimal field content, a non-negligible kinetic mixing is then required to maintain efficient
interactions. Alternatively, one may introduce two vectorlike fermions χ1 and χ2 with an
allowed Yukawa interaction ∼ Hx χ1 χ2 for an appropriate assignment of U (1)x charges.
In this paper, we consider both classes of dark matter candidates in the secluded regime,
where they annihilate into light dark sector mediators that subsequently decay into SM states.

40

## PDF page 41

5.1

Boltzmann equations for dark particles

5.1.1

Dark photon dark matter from the Higgs portal

The dominant annihilation channel for dark photon dark matter proceeds via
decay

annihilation

A′ A′ −−−−−−−−→ hx hx −−−−−−→ SM particles .

(5.2)

The coupled Boltzmann equations governing Yhx and YA′ are given by
]
dYhx
s ∑ [ eq 2
= −
2 (Yhx ) − Yh2x ⟨σv⟩hx hx →{ii,hh,ZZ,W ± W ∓ }
dT
T H i∈SM
{

+ (Yh Yheqx − Yh Yhx ) ⟨σv⟩hhx →{ii,hh,ZZ,W ± W ∓ }
+ 2YA2′ ⟨σv⟩A′ A′ →hx hx − 2Yh2x ⟨σv⟩hx hx →A′ A′
+ YA2′ ⟨σv⟩A′ A′ →hhx − Yh Yhx ⟨σv⟩hhx →A′ A′
(

+ 2 θ(mh − 2mhx ) −Yh2x ⟨σv⟩hx hx →h + 1s Yh ⟨Γ⟩h→hx hx

)

+ θ(mhx − 2mi ) 1s (Yheqx − Yhx )⟨Γ⟩hx →ii
(

+ θ(mhx − 2m )
A′

dYA′
s
= −2×
dT
T H i∈SM

YA2′ ⟨σv⟩A′ A′ →hx − 1s Yhx ⟨Γ⟩hx →A′ A′

∑ {[

)}

(5.3)

,

]

(YAeq′ )2 − YA2′ ⟨σv⟩A′ A′ →{ii,hh,ZZ,W ± W ∓ }

− YA2′ ⟨σv⟩A′ A′ →hx hx + Yh2x ⟨σv⟩hx hx →A′ A′
− YA2′ ⟨σv⟩A′ A′ →hhx + Yh Yhx ⟨σv⟩hhx →A′ A′
(

+ θ(mh − 2mA′ ) −YA2′ ⟨σv⟩A′ A′ →h + 1s Yh ⟨Γ⟩h→A′ A′
(

+ θ(mhx − 2mA′ )

−YA2′ ⟨σv⟩A′ A′ →hx + 1s Yhx ⟨Γ⟩hx →A′ A′

where
H=
5.1.2

)

√

H

=
1 T dheff

1 + 3 heff dT

π 2 geff T 2 /MPl
.
90 1 + 13 hT dhdTeff

)}

,

(5.4)

(5.5)

eff

Dark fermion dark matter from the U (1) portal

The benchmark models we consider are chosen such that the dark Higgs hx remains in thermal
equilibrium and decays into SM fermions before BBN, and thus without affecting the number
density evolution of the dark matter or the dark photon. We therefore focus on the coupled
evolution of χ and A′ . The dominant annihilation channel for dark fermion dark matter is
Z, A′

χχ̄ −−−−−−→ SM particles .
The coupled Boltzmann equations for Yχ and YA′ are given by
]
dYχ
s ∑ [ eq 2
= −
(Yχ ) − Yχ2 ⟨σv⟩χχ→{ii,ZZ}
dT
T H i∈SM
{

41

(5.6)

## PDF page 42

− Yχ2 ⟨σv⟩χχ→A′ Z + YA′ YZ ⟨σv⟩A′ Z→χχ
− Yχ2 ⟨σv⟩χχ→A′ A′ + YA2′ ⟨σv⟩A′ A′ →χχ
(

+ θ(mA′ − 2mχ )

−Yχ2 ⟨σv⟩χχ→A′ + 1s YA′ ⟨Γ⟩A′ →χχ

)}

,

(5.7)

[
dYA′
s
= −
(YAeq′ − YA′ ) YZ ⟨σv⟩A′ Z→ii + Yγ ⟨σv⟩A′ γ→ii
dT
T H i∈SM
∑{

(

+2Yi ⟨σv⟩iA′ →iZ + ⟨σv⟩iA′ →iγ

)]

+ Yχ2 ⟨σv⟩χχ→A′ A′ − YA2′ ⟨σv⟩A′ A′ →χχ
(

)

(

)}

+ θ(mA′ − 2mχ ) Yχ2 ⟨σv⟩χχ→A′ − 1s YA′ ⟨Γ⟩A′ →χχ
+ θ(mA′ − 2mi )

5.2

Yi2 ⟨σv⟩ii→A′ − 1s YA′ ⟨Γ⟩A′ →ii

.

(5.8)

Benchmark models

Case-1: dark photon dark matter Current bounds on the mixing parameter | sin θ |,
c.f., Eq. (2.20) arise from rare meson decays, beam-dump experiments, collider searches,
and astrophysical observations, see [111–113] for recent summaries. Colliders also constrain
invisible Higgs decays. The ATLAS Collaboration reports Br(h → inv) < 0.107 at 95%
CL [114], while CMS finds Br(h → inv) < 0.15 at 95% CL [115]. The invisible branching
fraction is
Γh→inv
,
Γh→inv = Γh→hx hx + Γh→A′ A′ ,
(5.9)
Br(h → inv) =
Γh→SM + Γh→inv
where for mh ≃ 125 GeV the SM Higgs width is Γh→SM = 4.1 MeV [116]. Since the dark
Higgs hx ultimately decays into SM fermions, its lifetime must be shorter than O(1 s) to
avoid spoiling big-bang nucleosynthesis.
For this scenario we present three benchmark models in Table 2, with vx = 100, 200,
450 GeV and a mass hierarchy mA′ > mhx . This hierarchy is required to realize a first-order
phase transition and hence to generate a stochastic gravitational wave signal. All benchmarks
are consistent with current experimental bounds.
For each benchmark we compute both the number density evolution of the relevant dark
sector species and the gravitational wave signal from the phase transition. The Boltzmann
equations governing Yhx and YA′ are given in Eqs. (5.3)–(5.4). As the Universe cools, the dark
sector undergoes a first-order phase transition during which U (1)x is spontaneously broken
and the dark photon A′ acquires a mass. After the transition, A′ annihilates into lighter
states, including the dark Higgs hx and SM particles, and subsequently freezes out, yielding
the observed dark matter relic abundance. The dark Higgs hx is unstable and decays into
SM fermions before big bang nucleosynthesis (BBN).
Although these benchmarks satisfy the dark matter relic density constraint, they typically require a tiny dark gauge coupling gx to avoid excessive secluded depletion of the the
dark photon. As a result, the phase transition is relatively weak and the corresponding gravitational wave signal is suppressed. Moreover, for these benchmarks we find that Tp /mA′
lies outside the validity ranges of our gauge-independent treatments in both the high- and
low-temperature limits.
42

## PDF page 43

Model
(a)
(b)
(c)

vx
100
200
450

gx
0.0221
0.0372
0.0525

λx
1.84 × 10−7
1.00 × 10−6
2.95 × 10−6

λmix
1 × 10−5
1 × 10−5
1 × 10−6

mhx
0.061
0.28
1.09

mA′
2.21
7.44
23.63

ΩA′ h2
0.12
0.12
0.12

τhx
2.61 × 10−3
5.19 × 10−7
9.64 × 10−7

Tp
3.90
10.85
29.69

Tp /mA′
1.77
1.46
1.26

Table 2: Benchmark models for Case 1, in which the dark photon is the dark matter candidate
and the dark sector communicates with the SM through the Higgs portal. All masses are in
GeV. For each benchmark we compute both the dark sector number density evolution and
the first-order phase transition dynamics. The Higgs mixing parameter λmix satisfies current
experimental bounds, and the hx lifetimes (in seconds) are ensured to be shorter than 1 s.
We also list the percolation temperature Tp and the ratio Tp /mA′ for each benchmark.
Case-2: dark fermion dark matter In Case 2, the dark matter candidate is a vectorlike
dark fermion χ with no direct Yukawa coupling to the dark Higgs hx . As a result, χ affects
the finite-temperature effective potential Veff (ϕc , T ) only indirectly through its contribution
to the longitudinal dark photon thermal mass ΠA′ , c.f., Eq. (3.15). Consequently, in the
gauge-independent calculation the coefficient appearing in ΠA′ is modified to 2/3.
The kinetic-mixing parameter δ in this work denotes the mixing between U (1)x and the
hypercharge gauge field U (1)Y , c.f., Eq. (2.4). Experimental searches constrain the kinetic
mixing between the dark photon and the electromagnetic photon, parameterized by δ. The
two parameters are related by [66, 117]
√

δ≈

g22 + gY2
g2

δ.

(5.10)

For Case 2, we choose three benchmark models, listed in Table 3, with vx = 1, 10,
100 GeV. For each benchmark we compute both the dark sector number density evolution
and the associated gravitational wave signal. All benchmarks satisfy current experimental
constraints on the kinetic mixing parameter δ and are shown in Fig. 7. The Boltzmann
equations governing the evolution of Yχ and YA′ are given in Eqs. (5.7)–(5.8).
In model (d), the dark fermion is heavier than the dark photon, mχ > mA′ . As the
Universe cools, χχ̄ annihilates efficiently into dark photons and yields the observed relic
abundance. The dark photons subsequently decay into e+ e− pairs before BBN. For models (e)
and (f), we instead choose mχ to lie slightly below mA′ . This near-degeneracy allows for a
larger gx while still reproducing the correct Ωχ h2 via the process A′ A′ → χχ. We indicate
these three Case 2 benchmarks in Figs. 5 and 7. Benchmark models (e) and (f) lie within
the projected sensitivity of Taiji, TianQin, and LISA, and thus provide promising multimessenger targets for a genuinely minimal U (1) dark sector.

5.3

Phenomenological implications

The continuing non-observation of weakly interacting massive particles (WIMP), especially
in the O(10 − 100 GeV) region, has substantially challenged a large class of traditional dark
matter scenarios. Current limits from direct and indirect detection, together with collider
searches, have significantly narrowed the viable parameter space for many WIMP candidates.
As a result, the measured relic abundance has increasingly become a stringent constraint on
43

## PDF page 44

Model vx
gx
λx
(d)
1 0.0208 1.93 × 10−7
(e)
10 0.505 1.17 × 10−4
(f)
100 0.391 3.13 × 10−5

mχ
mA′
Ωχ h2
0.35 0.0208 0.12
4.50
5.05
0.12
38.50 39.10 0.12

δ
1.3 × 10−10
1 × 10−8
1 × 10−8

τ A′
0.35
1.05 × 10−7
1.14 × 10−8

Tp
Tp /mA′
0.0423
2.03
0.54
0.107
3.34
0.085

Table 3: Benchmark models for Case 2, in which the dark matter candidate is a vectorlike
fermion χ that communicates with the SM through U (1) portal via kinetic mixing. All
masses are in GeV and lifetimes in seconds. For each benchmark we compute both the
dark sector number density evolution and the first-order phase transition dynamics. All
benchmarks satisfy the relevant constraints on the kinetic mixing parameter δ (see Fig. 7).
The corresponding peak gravitational wave signals are shown in Fig. 5. We also list the
percolation temperature Tp and the ratio Tp /mA′ for each benchmark.
10−2

(g − 2)e

10−4

Others

E141
nu-Cal

−6

10

δ

E137
(e)

10−8

(f)

SN1987A
(d)

10−10

10−12
10−3

10−2

10−1

m [GeV]

100

101

102

A′

Figure 7: Experimental constraints on the kinetic mixing parameter δ, defined in Eqs. (2.4)
and (5.10), for dark photon masses mA′ ∈ [1MeV, 100GeV]. The three Case 2 benchmark
models (Table 3) are shown as black crosses and are consistent with all current experimental bounds. Constraints on the kinetic mixing for dark photons with mA′ ≳ 1 MeV arise
from supernova (SN1987A) [118], (g − 2)e [119] and from various beam dump experiments:
E141 [120], E137 [121–123], ν-Cal [124, 125]. The pink region in the upper portion of the
plot, labeled as “Others”, collects constraints from collider and fixed-target experiments, including: CMS [126], BaBar [127], LHCb [128], KLOE [129–132] and A1 [133].
model building rather than an automatic target that can be achieved across broad regions of
parameter space.
At the level of thermal freeze-out, the tension is particularly transparent: with present
experimental sensitivities, many WIMP-like candidates that remain compatible with direct
detection bounds cannot maintain sufficient annihilation into SM final states, which leads to
an overproduction of dark matter. In hidden sector constructions, this difficulty can be even
more pronounced, since the interactions connecting the dark sector to the SM are typically
mediated by portal couplings that must be small. Consequently, annihilation directly into
44

## PDF page 45

SM particles can be inefficient. An common alternative is secluded annihilation, in which
dark matter annihilates dominantly into lighter dark mediators that subsequently decay into
SM states, thereby achieving an efficient depletion of the relic abundance while alleviating
dark matter experimental constraints.
In the minimal U (1)x framework considered here, these general considerations manifest
themselves clearly in the benchmark models. As illustrated in Fig. 5, parameter points with
dark fermion dark matter can simultaneously achieve sufficient annihilation to match the observed relic density and produce a potentially detectable stochastic gravitational wave signal
from the first-order phase transition. By contrast, dark photon dark matter realized through
secluded freeze-out cannot accommodate both requirements: regions of parameter space that
yield an observable gravitational wave signal often require a sizable gauge coupling, while
such a coupling tends to deplete the dark photon relic abundance too efficiently, making
it difficult to retain the correct relic density. This complementarity is not surprising. Detectable gravitational wave signals from a first-order phase transition generally favor a sizable
gauge coupling, which strengthens the dynamics of the transition and enhances the signal.
However, the same sizable coupling often increases the efficiency of dark photon annihilation,
reducing the relic density below the observed value via freeze-out.
Dark fermion dark matter can annihilate into dark photons, which then decay into SM
particles via portal interactions. The presence of an additional mass parameter mχ offers additional flexibility. In particular, choosing mχ close to the dark photon mass can suppress the
annihilation efficiency and prevent excessive depletion, enabling simultaneous compatibility
with the relic abundance and gravitational wave detectability.
It should be noted that in the √
minimal U (1)x setup, the dark photon and dark Higgs
masses are mA′ = gx vx and mhx = 2λ vx , respectively. Given the scaling relation between
the Higgs quartic coupling and the gauge coupling discussed in detail in Section 3 in both
high- and low-temperature regimes, the dark photon is generically heavier than the dark
Higgs. Accordingly, in all benchmark models considered here we impose mA′ > mhx , a
hierarchy that is required for a dark sector phase transition in this minimal setup.
Finally, we emphasize that production via freeze-in can remain viable for both classes of
dark matter candidates even when the gauge coupling is sizable. For dark fermion dark matter, previous studies, see, e.g., [66, 134],7 demonstrate that large regions of parameter space
can satisfy existing experimental constraints while reproducing the observed relic abundance.
For dark photon dark matter, even if the hidden sector possesses a sizable gauge coupling, the
Higgs portal mixing can be adjusted to generate an appropriate abundance. More broadly,
freeze-in production can offer greater freedom to maintain a sizable gauge coupling, and hence
potentially large gravitational wave signals, while still achieving the correct relic density. A
systematic exploration of this possibility, in particular for dark photon dark matter in the
minimal gauged U (1)x setup, is left open for future work.
7

Although these references consider a simplified U (1)x setup consisting only of a vectorlike fermion and a
dark photon whose mass arises from the Stückelberg mechanism, they already illustrate the broad viability
and flexibility of freeze-in production in U (1) portal scenarios.

45

## PDF page 46

6

Conclusion and outlook

In this work, we investigated gauge-independent predictions for stochastic gravitational waves
sourced by first-order phase transitions in a minimal gauged U (1)x dark sector. This addresses
a central obstacle to making reliable predictions in gauge theories: the gauge dependence of
the finite-temperature effective potential and the associated tunneling action. To obtain
model-intrinsic and reproducible results, we adopted a gauge-independent formulation of the
effective action based on the Nielsen identity, combined with a controlled derivative expansion
and power counting. This framework yields a gauge-independent tunneling action, enabling
a well-defined treatment of nucleation dynamics and, consequently, robust gravitational wave
predictions. The resulting signals span a wide range of peak frequencies relevant to pulsar
timing arrays and planned space-based interferometers, and they exhibit systematic trends
across parameter space.
We performed Monte Carlo explorations of the parameter space using both the conventional gauge-dependent approach and, separately, the gauge-independent framework in the
high- and low-temperature limits. The gauge-dependent scan is useful for building intuition
and reveals clear qualitative trends: the U (1)x symmetry breaking scale vx largely controls the
characteristic frequency, while the phase transition temperature regime correlates strongly
with the signal strength, with supercooled transitions typically producing larger amplitudes.
At the same time, an explicit comparison shows that gauge-dependent spectra can depart significantly from the gauge-independent predictions when the gauge-fixing parameter is varied,
underscoring that the gauge choice can materially impact phenomenological interpretations.
Using the gauge-independent effective action, we scanned the high- and low-temperature
limits separately and then retained only those points consistent with the corresponding
temperature-limit assumptions. The surviving points shown in Fig. 5 provide concrete, gaugeindependent predictions for the minimal U (1)x setup, mapping viable microscopic parameters
to detector-facing peak frequencies and amplitudes. A notable outcome is that supercooled
transitions constitute a substantial fraction of successful transitions in broad scans and, when
realized, often populate the most promising regions of experimental sensitivity, reinforcing
the view that supercooled first-order phase transitions are among the most compelling targets
in current gravitational wave searches.
By contrast, parametrically high-temperature transitions are comparatively rare and typically yield weak signals. Between these limits lies an intermediate regime in which neither
the high- nor the low-temperature gauge-independent treatment is applicable. Bridging this
gap with a fully gauge-independent framework remains an important open direction.
Finally, we connected the phase transition phenomenology to viable dark matter candidates within the same minimal field content. We considered both dark photon dark matter
via the Higgs portal, and dark fermion dark matter via the dark photon portal, in secluded
settings, and provided benchmark targets that enable genuine multi-messenger tests. The
benchmarks illustrate a clear complementarity: parameter regions capable of producing potentially detectable gravitational waves typically favor sizable gauge dynamics, which can be
in tension with reproducing the observed relic abundance for dark photon dark matter via
secluded freeze-out. By contrast, dark fermion dark matter retains greater flexibility and can
more readily accommodate both relic density consistency and gravitational wave visibility.
More broadly, freeze-in production channels may further expand the viable parameter space
46

## PDF page 47

while maintaining sizable gauge couplings, and merit systematic exploration in future work.
Across all temperature regimes, we find a robust feature of the parameter region that
supports a first-order phase transition: the dark photon must be heavier than the dark
Higgs. If nature were to realize the opposite hierarchy, a U (1)x breaking phase transition in
the minimal dark sector and thus the associated gravitational wave signal, will not occur.
Taken together, this work delivers a gauge-independent, end-to-end pipeline that connects a minimal hidden sector Lagrangian to nucleation dynamics, stochastic gravitational
wave spectra, and cosmologically viable dark matter benchmarks. Our results make clear
that gauge independence is not merely a technical refinement, but a necessary condition for
obtaining physically meaningful gravitational wave predictions in gauge theories. Within this
framework, even the minimal gauged U (1)x dark sector yields predictive, detector-relevant
targets, most notably in the supercooled regime, that are complementary to collider probes
and conventional dark matter searches.
Looking ahead, the setup studied here admits several natural extensions, including additional hidden states, gauge-independent conformal U (1) realizations, and explorations of
phase transitions at larger symmetry breaking scales. More broadly, the lesson is general:
whenever gauge fields and spontaneous symmetry breaking play a dynamical role, gravitational wave predictions should be formulated in gauge-independent terms to enable reliable
comparisons with experimental data and across different theoretical studies.
Acknowledgments:
This work is supported in part by the National Natural Science Foundation of China under
Grant No. 11935009, and Tianjin University Self-Innovation Fund Extreme Basic Research
Project Grant No. 2025XJ21-0007.

47

## PDF page 48

References
[1] G. W. Anderson and L. J. Hall,
doi:10.1103/PhysRevD.45.2685

Phys. Rev. D 45,

2685-2698 (1992)

[2] M. E. Carrington, Phys. Rev. D 45, 2933-2944 (1992) doi:10.1103/PhysRevD.45.2933
[3] P. B. Arnold and O. Espinosa, Phys. Rev. D 47, 3546 (1993) [erratum: Phys. Rev. D
50, 6662 (1994)] doi:10.1103/PhysRevD.47.3546 [arXiv:hep-ph/9212235 [hep-ph]].
[4] K. Kajantie, M. Laine, K. Rummukainen and M. E. Shaposhnikov, Phys. Rev. Lett. 77,
2887-2890 (1996) doi:10.1103/PhysRevLett.77.2887 [arXiv:hep-ph/9605288 [hep-ph]].
[5] C. Grojean, G. Servant and J. D. Wells, Phys. Rev. D 71, 036001 (2005)
doi:10.1103/PhysRevD.71.036001 [arXiv:hep-ph/0407019 [hep-ph]].
[6] D. E. Morrissey and M. J. Ramsey-Musolf, New J. Phys. 14, 125003 (2012)
doi:10.1088/1367-2630/14/12/125003 [arXiv:1206.2942 [hep-ph]].
[7] P. Athron, C. Balázs, A. Fowlie, L. Morris and L. Wu, Prog. Part. Nucl. Phys. 135,
104094 (2024) doi:10.1016/j.ppnp.2023.104094 [arXiv:2305.02357 [hep-ph]].
[8] P.
Schwaller,
Phys.
Rev.
Lett.
115,
no.18,
doi:10.1103/PhysRevLett.115.181101 [arXiv:1504.07263 [hep-ph]].

181101

(2015)

[9] J. Jaeckel, V. V. Khoze and M. Spannowsky, Phys. Rev. D 94, no.10, 103519 (2016)
doi:10.1103/PhysRevD.94.103519 [arXiv:1602.03901 [hep-ph]].
[10] R. Jinno and M. Takimoto, Phys. Rev. D 95, no.1,
doi:10.1103/PhysRevD.95.015020 [arXiv:1604.05035 [hep-ph]].
[11] A.
Addazi,
Mod.
Phys.
Lett.
A
32,
no.08,
doi:10.1142/S0217732317500493 [arXiv:1607.08057 [hep-ph]].

015020

(2017)

1750049

(2017)

[12] W. Chao, H. K. Guo and J. Shu, JCAP 09, 009 (2017) doi:10.1088/14757516/2017/09/009 [arXiv:1702.02698 [hep-ph]].
[13] A. Addazi and A. Marciano, Chin. Phys. C 42, no.2, 023107 (2018) doi:10.1088/16741137/42/2/023107 [arXiv:1703.03248 [hep-ph]].
[14] L. Marzola, A. Racioppi and V. Vaskonen, Eur. Phys. J. C 77, no.7, 484 (2017)
doi:10.1140/epjc/s10052-017-4996-1 [arXiv:1704.01034 [hep-ph]].
[15] I. Baldes and C. Garcia-Cely, JHEP 05, 190 (2019) doi:10.1007/JHEP05(2019)190
[arXiv:1809.01198 [hep-ph]].
[16] C. Marzo, L. Marzola and V. Vaskonen, Eur. Phys. J. C 79, no.7, 601 (2019)
doi:10.1140/epjc/s10052-019-7076-x [arXiv:1811.11169 [hep-ph]].
[17] M. Breitbach, J. Kopp, E. Madge, T. Opferkuch and P. Schwaller, JCAP 07, 007 (2019)
doi:10.1088/1475-7516/2019/07/007 [arXiv:1811.11175 [hep-ph]].
48

## PDF page 49

[18] M. Fairbairn,
E. Hardy and A. Wickens,
JHEP
doi:10.1007/JHEP07(2019)044 [arXiv:1901.11038 [hep-ph]].

07,

044

(2019)

[19] Y. Nakai, M. Suzuki, F. Takahashi and M. Yamada, Phys. Lett. B 816, 136238 (2021)
doi:10.1016/j.physletb.2021.136238 [arXiv:2009.09754 [astro-ph.CO]].
[20] A. Addazi, Y. F. Cai, Q. Gan, A. Marciano and K. Zeng, Sci. China Phys. Mech. Astron.
64, no.9, 290411 (2021) doi:10.1007/s11433-021-1724-6 [arXiv:2009.10327 [hep-ph]].
[21] K. Fujikura, S. Girmohanta, Y. Nakai and M. Suzuki, Phys. Lett. B 846, 138203 (2023)
doi:10.1016/j.physletb.2023.138203 [arXiv:2306.17086 [hep-ph]].
[22] F. Ertas, F. Kahlhoefer and C. Tasillo, JCAP 02, no.02, 014 (2022) doi:10.1088/14757516/2022/02/014 [arXiv:2109.06208 [astro-ph.CO]].
[23] W. Wang, W. L. Xu and J. M. Yang, Eur. Phys. J. Plus 138, no.9, 781 (2023)
doi:10.1140/epjp/s13360-023-04412-4 [arXiv:2209.11408 [hep-ph]].
[24] Z. Chen, K. Ye and M. Zhang, Phys. Rev. D 107, no.9, 095027 (2023)
doi:10.1103/PhysRevD.107.095027 [arXiv:2303.11820 [hep-ph]].
[25] T. Bringmann, P. F. Depta, T. Konstandin, K. Schmidt-Hoberg and C. Tasillo, JCAP
11, 053 (2023) doi:10.1088/1475-7516/2023/11/053 [arXiv:2306.09411 [astro-ph.CO]].
[26] S. P. Li and K. P. Xie, Phys. Rev. D 108, no.5,
doi:10.1103/PhysRevD.108.055018 [arXiv:2307.01086 [hep-ph]].

055018

(2023)

[27] S. Kanemura and S. P. Li, JCAP 03, 005 (2024) doi:10.1088/1475-7516/2024/03/005
[arXiv:2308.16390 [hep-ph]].
[28] T. Bringmann, T. E. Gonzalo, F. Kahlhoefer, J. Matuszak and C. Tasillo, JCAP 05,
065 (2024) doi:10.1088/1475-7516/2024/05/065 [arXiv:2311.06346 [astro-ph.CO]].
[29] A. Banik, Y. Cui, Y. D. Tsai and Y. Tsai, [arXiv:2412.16282 [hep-ph]].
[30] W. Z. Feng, J. Li and P. Nath, Phys. Rev. D 110, no.1, 015020 (2024)
doi:10.1103/PhysRevD.110.015020 [arXiv:2403.09558 [hep-ph]].
[31] S. Balan, T. Bringmann, F. Kahlhoefer, J. Matuszak and C. Tasillo, JCAP 08, 062
(2025) doi:10.1088/1475-7516/2025/08/062 [arXiv:2502.19478 [hep-ph]].
[32] V. Baules and N. Okada, [arXiv:2508.13527 [hep-ph]].
[33] J. Li and P. Nath, Phys. Rev. D 111, no.12, 123007 (2025) doi:10.1103/79cb-rssl
[arXiv:2501.14986 [hep-ph]].
[34] W. Z. Feng, J. Li, P. Nath and Z. H. Ye, [arXiv:2510.13770 [hep-ph]].
[35] Z. Wang, [arXiv:2601.04340 [astro-ph.CO]].
[36] R. Houtz, M. Ulloa and M. West, [arXiv:2511.23467 [hep-ph]].
49

## PDF page 50

[37] D. Metaxas and E. J. Weinberg, Phys. Rev. D 53,
doi:10.1103/PhysRevD.53.836 [arXiv:hep-ph/9507381 [hep-ph]].
[38] H. H. Patel and M. J. Ramsey-Musolf,
JHEP
doi:10.1007/JHEP07(2011)029 [arXiv:1101.4665 [hep-ph]].

07,

836-843

(1996)

029

(2011)

[39] M. Garny and T. Konstandin, JHEP 07, 189 (2012) doi:10.1007/JHEP07(2012)189
[arXiv:1205.3392 [hep-ph]].
[40] A. Andreassen, W. Frost and M. D. Schwartz, Phys. Rev. D 91, no.1, 016009 (2015)
doi:10.1103/PhysRevD.91.016009 [arXiv:1408.0287 [hep-ph]].
[41] A. Andreassen, W. Frost and M. D. Schwartz, Phys. Rev. Lett. 113, no.24, 241801
(2014) doi:10.1103/PhysRevLett.113.241801 [arXiv:1408.0292 [hep-ph]].
[42] S. Arunasalam and M. J. Ramsey-Musolf,
JHEP
doi:10.1007/JHEP08(2022)138 [arXiv:2105.07588 [hep-ph]].

08,

138

(2022)

[43] J. Löfgren, M. J. Ramsey-Musolf, P. Schicho and T. V. I. Tenkanen, Phys. Rev. Lett.
130, no.25, 251801 (2023) doi:10.1103/PhysRevLett.130.251801 [arXiv:2112.05472 [hepph]].
[44] J. Hirvonen, J. Löfgren, M. J. Ramsey-Musolf, P. Schicho and T. V. I. Tenkanen, JHEP
07, 135 (2022) doi:10.1007/JHEP07(2022)135 [arXiv:2112.08912 [hep-ph]].
[45] Y. Zhu, J. Liu, R. Qin and L. Bian, Phys. Rev. D 112, no.1, 015018 (2025)
doi:10.1103/f4gr-hycg [arXiv:2503.19566 [hep-ph]].
[46] J. Liu, R. Qin and L. Bian, [arXiv:2512.05565 [hep-ph]].
[47] J. Liu, R. Qin and L. Bian, [arXiv:2601.05793 [hep-ph]].
[48] L. Leitao and A. Megevand, JCAP 05, 037 (2016) doi:10.1088/1475-7516/2016/05/037
[arXiv:1512.08962 [astro-ph.CO]].
[49] A. Megevand and S. Ramirez, Nucl. Phys. B 919, 74-109
doi:10.1016/j.nuclphysb.2017.03.009 [arXiv:1611.05853 [astro-ph.CO]].

(2017)

[50] A. Kobakhidze, C. Lagger, A. Manning and J. Yue, Eur. Phys. J. C 77, no.8, 570 (2017)
doi:10.1140/epjc/s10052-017-5132-y [arXiv:1703.06552 [hep-ph]].
[51] S. Iso, P. D. Serpico and K. Shimada, Phys. Rev. Lett. 119, no.14, 141301 (2017)
doi:10.1103/PhysRevLett.119.141301 [arXiv:1704.04955 [hep-ph]].
[52] J. Ellis, M. Lewicki, J. M. No and V. Vaskonen, JCAP 06, 024 (2019) doi:10.1088/14757516/2019/06/024 [arXiv:1903.09642 [hep-ph]].
[53] X. Wang, F. P. Huang and X. Zhang, JCAP 05, 045 (2020) doi:10.1088/14757516/2020/05/045 [arXiv:2003.08892 [hep-ph]].

50

## PDF page 51

[54] J. Ellis, M. Lewicki and V. Vaskonen, JCAP 11, 020 (2020) doi:10.1088/14757516/2020/11/020 [arXiv:2007.15586 [astro-ph.CO]].
[55] K. Kawana, Phys. Rev. D 105, no.10, 103515 (2022) doi:10.1103/PhysRevD.105.103515
[arXiv:2201.00560 [hep-ph]].
[56] K. Freese and M. W. Winkler, Phys. Rev. D 106, no.10, 103523 (2022)
doi:10.1103/PhysRevD.106.103523 [arXiv:2208.03330 [astro-ph.CO]].
[57] M. Lewicki and V. Vaskonen, Eur. Phys. J. C 83, no.2,
doi:10.1140/epjc/s10052-023-11241-3 [arXiv:2208.11697 [astro-ph.CO]].

109

(2023)

[58] L. Sagunski, P. Schicho and D. Schmitt, Phys. Rev. D 107, no.12, 123512 (2023)
doi:10.1103/PhysRevD.107.123512 [arXiv:2303.02450 [hep-ph]].
[59] E. Madge, E. Morgante, C. Puchades-Ibáñez, N. Ramberg, W. Ratzinger, S. Schenk and
P. Schwaller, JHEP 10, 171 (2023) doi:10.1007/JHEP10(2023)171 [arXiv:2306.14856
[hep-ph]].
[60] P. Athron, A. Fowlie, C. T. Lu, L. Morris, L. Wu, Y. Wu and Z. Xu, Phys. Rev. Lett.
132, no.22, 221001 (2024) doi:10.1103/PhysRevLett.132.221001 [arXiv:2306.17239 [hepph]].
[61] T. Ghosh, A. Ghoshal, H. K. Guo, F. Hajkarim, S. F. King, K. Sinha, X. Wang and
G. White, JCAP 05, 100 (2024) doi:10.1088/1475-7516/2024/05/100 [arXiv:2307.02259
[astro-ph.HE]].
[62] P. Athron, L. Morris and Z. Xu, JCAP 05, 075 (2024) doi:10.1088/14757516/2024/05/075 [arXiv:2309.05474 [hep-ph]].
[63] P. Athron, S. Datta and Z. Y. Zhang, [arXiv:2511.10288 [hep-ph]].
[64] S. Pascoli, S. Rosauro-Alcaraz and M. Zandi, [arXiv:2602.02829 [hep-ph]].
[65] D. Feldman, Z. Liu and P. Nath, Phys. Rev. D 75,
doi:10.1103/PhysRevD.75.115001 [arXiv:hep-ph/0702123 [hep-ph]].

115001

(2007)

[66] W. Z. Feng, Z. H. Zhang and K. Y. Zhang, JCAP 05, 112 (2024) doi:10.1088/14757516/2024/05/112 [arXiv:2312.03837 [hep-ph]].
[67] L. Dolan and R. Jackiw, Phys. Rev. D 9, 3320-3341 (1974) doi:10.1103/PhysRevD.9.3320
[68] D. Curtin, P. Meade and H. Ramani, Eur. Phys. J. C 78, no.9, 787 (2018)
doi:10.1140/epjc/s10052-018-6268-0 [arXiv:1612.00466 [hep-ph]].
[69] M. Laine and A. Vuorinen, Lect. Notes Phys. 925, pp.1-281 (2016) Springer, 2016,
doi:10.1007/978-3-319-31933-9 [arXiv:1701.01554 [hep-ph]].
[70] P. H. Ginsparg, Nucl. Phys. B 170, 388-408 (1980) doi:10.1016/0550-3213(80)90418-6

51

## PDF page 52

[71] T. Appelquist and R. D.
doi:10.1103/PhysRevD.23.2305

Pisarski,

Phys.

Rev.

D

23,

2305

(1981)

[72] S. Nadkarni, Phys. Rev. D 27, 917 (1983) doi:10.1103/PhysRevD.27.917
[73] K. Farakos, K. Kajantie, K. Rummukainen and M. E. Shaposhnikov, Nucl. Phys. B 425,
67-109 (1994) doi:10.1016/0550-3213(94)90173-2 [arXiv:hep-ph/9404201 [hep-ph]].
[74] K. Kajantie, M. Laine, K. Rummukainen and M. E. Shaposhnikov, Nucl. Phys. B 458,
90-136 (1996) doi:10.1016/0550-3213(95)00549-8 [arXiv:hep-ph/9508379 [hep-ph]].
[75] E. Braaten and A. Nieto,
Phys. Rev. D 51,
doi:10.1103/PhysRevD.51.6990 [arXiv:hep-ph/9501375 [hep-ph]].

6990-7006

(1995)

[76] R. R. Parwani, Phys. Rev. D 45, 4695 (1992) [erratum: Phys. Rev. D 48, 5965 (1993)]
doi:10.1103/PhysRevD.45.4695 [arXiv:hep-ph/9204216 [hep-ph]].
[77] N. K. Nielsen, Nucl. Phys. B 101, 173-188 (1975) doi:10.1016/0550-3213(75)90301-6
[78] S. R. Coleman, Phys. Rev. D 15, 2929-2936 (1977) [erratum: Phys. Rev. D 16, 1248
(1977)] doi:10.1103/PhysRevD.16.1248
[79] C. G. Callan, Jr. and S. R. Coleman, Phys. Rev. D 16, 1762-1768 (1977)
doi:10.1103/PhysRevD.16.1762
[80] M. Kierkla, A. Karam and B. Swiezewska, JHEP
doi:10.1007/JHEP03(2023)007 [arXiv:2210.07075 [astro-ph.CO]].

03,

007

(2023)

[81] C. L. Wainwright,
Comput. Phys. Commun.
doi:10.1016/j.cpc.2012.04.004 [arXiv:1109.4189 [hep-ph]].

2006-2013

(2012)

183,

[82] A. D. Linde, Nucl. Phys. B 216, 421 (1983) [erratum: Nucl. Phys. B 223, 544 (1983)]
doi:10.1016/0550-3213(83)90072-X
[83] A. H. Guth and S. H. H. Tye, Phys. Rev. Lett. 44, 631 (1980) [erratum: Phys. Rev.
Lett. 44, 963 (1980)] doi:10.1103/PhysRevLett.44.631
[84] A. H. Guth and E. J.
doi:10.1103/PhysRevD.23.876

Weinberg,

Phys.

Rev.

D

23,

876

(1981)

[85] P. Athron, C. Balázs and L. Morris, JCAP 03, 006 (2023) doi:10.1088/14757516/2023/03/006 [arXiv:2212.07559 [hep-ph]].
[86] A. Chodos, R. L. Jaffe, K. Johnson, C. B. Thorn and V. F. Weisskopf, Phys. Rev. D 9,
3471-3495 (1974) doi:10.1103/PhysRevD.9.3471
[87] L. Leitao, A. Megevand and A. D. Sanchez, JCAP 10, 024 (2012) doi:10.1088/14757516/2012/10/024 [arXiv:1205.3070 [astro-ph.CO]].
[88] F. Giese, T. Konstandin and J. van de Vis, JCAP 07, no.07, 057 (2020)
doi:10.1088/1475-7516/2020/07/057 [arXiv:2004.06995 [astro-ph.CO]].
52

## PDF page 53

[89] F. Giese, T. Konstandin, K. Schmitz and J. van de Vis, JCAP 01, 072 (2021)
doi:10.1088/1475-7516/2021/01/072 [arXiv:2010.09744 [astro-ph.CO]].
[90] J. R. Espinosa, T. Konstandin, J. M. No and G. Servant, JCAP 06, 028 (2010)
doi:10.1088/1475-7516/2010/06/028 [arXiv:1004.4187 [hep-ph]].
[91] W. Y. Ai, B. Laurent and J. van de Vis, JCAP 07, 002 (2023) doi:10.1088/14757516/2023/07/002 [arXiv:2303.10171 [astro-ph.CO]].
[92] W. Y. Ai, B. Laurent and J. van de Vis, JHEP
doi:10.1007/JHEP02(2025)119 [arXiv:2411.13641 [hep-ph]].

02,

119

(2025)

[93] A. Kosowsky, M. S. Turner and R. Watkins, Phys. Rev. D 45, 4514-4535 (1992)
doi:10.1103/PhysRevD.45.4514
[94] M. Hindmarsh, S. J. Huber, K. Rummukainen and D. J. Weir, Phys. Rev. Lett. 112,
041301 (2014) doi:10.1103/PhysRevLett.112.041301 [arXiv:1304.2433 [hep-ph]].
[95] C. Caprini and R. Durrer,
Phys. Rev. D 74,
063521
doi:10.1103/PhysRevD.74.063521 [arXiv:astro-ph/0603476 [astro-ph]].

(2006)

[96] M. Hindmarsh, S. J. Huber, K. Rummukainen and D. J. Weir, Phys. Rev. D 92, no.12,
123009 (2015) doi:10.1103/PhysRevD.92.123009 [arXiv:1504.03291 [astro-ph.CO]].
[97] W. H. Ruan, Z. K. Guo, R. G. Cai and Y. Z. Zhang, Int. J. Mod. Phys. A 35, no.17,
2050075 (2020) doi:10.1142/S0217751X2050075X [arXiv:1807.09495 [gr-qc]].
[98] J. Luo et al. [TianQin], Class. Quant. Grav. 33, no.3, 035010 (2016) doi:10.1088/02649381/33/3/035010 [arXiv:1512.02076 [astro-ph.IM]].
[99] P. Amaro-Seoane et al. [LISA], [arXiv:1702.00786 [astro-ph.IM]].
[100] A. Sesana, N. Korsakova, M. A. Sedda, V. Baibhav, E. Barausse, S. Barke, E. Berti,
M. Bonetti, P. R. Capelo and C. Caprini, et al. Exper. Astron. 51, no.3, 1333-1383
(2021) doi:10.1007/s10686-021-09709-9 [arXiv:1908.11391 [astro-ph.IM]].
[101] C. Grojean and G. Servant,
Phys. Rev. D 75,
doi:10.1103/PhysRevD.75.043507 [arXiv:hep-ph/0607107 [hep-ph]].

043507

(2007)

[102] S. Kuroyanagi, S. Tsujikawa, T. Chiba and N. Sugiyama, Phys. Rev. D 90, no.6, 063513
(2014) doi:10.1103/PhysRevD.90.063513 [arXiv:1406.1369 [astro-ph.CO]].
[103] M. Punturo, M. Abernathy, F. Acernese, B. Allen, N. Andersson, K. Arun, F. Barone,
B. Barr, M. Barsuglia and M. Beker, et al. Class. Quant. Grav. 27, 194002 (2010)
doi:10.1088/0264-9381/27/19/194002
[104] B. P. Abbott et al. [LIGO Scientific], Class. Quant. Grav. 34, no.4, 044001 (2017)
doi:10.1088/1361-6382/aa51f4 [arXiv:1607.08697 [astro-ph.IM]].

53

## PDF page 54

[105] G. Agazie et al. [NANOGrav], Astrophys. J. Lett. 951,
doi:10.3847/2041-8213/acdac6 [arXiv:2306.16213 [astro-ph.HE]].

no.1, L8 (2023)

[106] D. J. Reardon, A. Zic, R. M. Shannon, G. B. Hobbs, M. Bailes, V. Di Marco, A. Kapur,
A. F. Rogers, E. Thrane and J. Askew, et al. Astrophys. J. Lett. 951, no.1, L6 (2023)
doi:10.3847/2041-8213/acdd02 [arXiv:2306.16215 [astro-ph.HE]].
[107] J. Antoniadis et al. [EPTA and InPTA:], Astron. Astrophys. 678, A50 (2023)
doi:10.1051/0004-6361/202346844 [arXiv:2306.16214 [astro-ph.HE]].
[108] P. Athron, C. Balázs, A. Fowlie and Y. Zhang, Eur. Phys. J. C 80, no.6, 567 (2020)
doi:10.1140/epjc/s10052-020-8035-2 [arXiv:2003.02859 [hep-ph]].
[109] G. Arcadi, D. Cabo-Almeida, M. Dutra, P. Ghosh, M. Lindner, Y. Mambrini, J. P. Neto,
M. Pierre, S. Profumo and F. S. Queiroz, Eur. Phys. J. C 85, no.2, 152 (2025)
doi:10.1140/epjc/s10052-024-13672-y [arXiv:2403.15860 [hep-ph]].
[110] W. Z. Feng and Z. H. Zhang, [arXiv:2409.17217 [hep-ph]].
[111] J. Beacham, C. Burrage, D. Curtin, A. De Roeck, J. Evans, J. L. Feng, C. Gatto,
S. Gninenko, A. Hartin and I. Irastorza, et al. J. Phys. G 47, no.1, 010501 (2020)
doi:10.1088/1361-6471/ab4cd2 [arXiv:1901.09966 [hep-ex]].
[112] G. Arcadi, A. Djouadi and M. Kado, Eur. Phys. J. C 81, no.7, 653 (2021)
doi:10.1140/epjc/s10052-021-09411-2 [arXiv:2101.02507 [hep-ph]].
[113] E. Cortina Gil et al. [NA62], JHEP 11, 143 (2025) doi:10.1007/JHEP11(2025)143
[arXiv:2507.17286 [hep-ex]].
[114] G.
Aad
et al.
[ATLAS],
Phys.
Lett.
B
842,
doi:10.1016/j.physletb.2023.137963 [arXiv:2301.10731 [hep-ex]].

137963

[115] A. Tumasyan et al. [CMS], Eur. Phys. J. C 83, no.10,
doi:10.1140/epjc/s10052-023-11952-7 [arXiv:2303.01214 [hep-ex]].

933

(2023)
(2023)

[116] D. de Florian et al. [LHC Higgs Cross Section Working Group], CERN Yellow Rep.
Monogr. 2, 1-869 (2017) doi:10.23731/CYRM-2017-002 [arXiv:1610.07922 [hep-ph]].
[117] W. Z. Feng and Z. H. Zhang, Phys. Rev. D 112, no.3, 035004 (2025) doi:10.1103/vshngbdp [arXiv:2405.19431 [hep-ph]].
[118] J. H. Chang, R. Essig and S. D. McDermott, JHEP 01,
doi:10.1007/JHEP01(2017)107 [arXiv:1611.03864 [hep-ph]].

107 (2017)

[119] M. Pospelov, Phys. Rev. D 80, 095002 (2009) doi:10.1103/PhysRevD.80.095002
[arXiv:0811.1030 [hep-ph]].
[120] E. M. Riordan, M. W. Krasny, K. Lang, P. De Barbaro, A. Bodek, S. Dasu, N. Varelas, X. Wang, R. G. Arnold and D. Benton, et al. Phys. Rev. Lett. 59, 755 (1987)
doi:10.1103/PhysRevLett.59.755
54

## PDF page 55

[121] J. D. Bjorken, S. Ecklund, W. R. Nelson, A. Abashian, C. Church, B. Lu,
L. W. Mo, T. A. Nunamaker and P. Rassmann, Phys. Rev. D 38, 3375 (1988)
doi:10.1103/PhysRevD.38.3375
[122] B. Batell, R. Essig and Z. Surujon, Phys. Rev. Lett. 113, no.17, 171802 (2014)
doi:10.1103/PhysRevLett.113.171802 [arXiv:1406.2698 [hep-ph]].
[123] L. Marsicano, M. Battaglieri, M. Bondi’, C. D. R. Carvajal, A. Celentano, M. De
Napoli, R. De Vita, E. Nardi, M. Raggi and P. Valente, Phys. Rev. D 98, no.1, 015031
(2018) doi:10.1103/PhysRevD.98.015031 [arXiv:1802.03794 [hep-ex]].
[124] J. Blumlein and J. Brunner, Phys. Lett. B 701,
doi:10.1016/j.physletb.2011.05.046 [arXiv:1104.2747 [hep-ex]].

155-159

(2011)

[125] J. Blümlein and J. Brunner, Phys. Lett. B 731,
doi:10.1016/j.physletb.2014.02.029 [arXiv:1311.3870 [hep-ph]].

320-326

(2014)

[126] [CMS], CMS-PAS-EXO-19-018.
[127] J. P. Lees et al. [BaBar], Phys. Rev. Lett. 113, no.20,
doi:10.1103/PhysRevLett.113.201801 [arXiv:1406.2980 [hep-ex]].

201801 (2014)

[128] R. Aaij et al. [LHCb], Phys. Rev. Lett. 124, no.4,
doi:10.1103/PhysRevLett.124.041801 [arXiv:1910.06926 [hep-ex]].

041801

(2020)

[129] F. Archilli et al. [KLOE-2],
Phys. Lett. B 706,
doi:10.1016/j.physletb.2011.11.033 [arXiv:1110.0411 [hep-ex]].

251-255

(2012)

[130] D. Babusci et al. [KLOE-2],
Phys. Lett. B 720,
doi:10.1016/j.physletb.2013.01.067 [arXiv:1210.3927 [hep-ex]].

111-115

(2013)

[131] D. Babusci et al. [KLOE-2],
Phys. Lett. B 736,
doi:10.1016/j.physletb.2014.08.005 [arXiv:1404.7772 [hep-ex]].

459-464

(2014)

[132] A. Anastasi et al. [KLOE-2], Phys. Lett. B 757,
doi:10.1016/j.physletb.2016.04.019 [arXiv:1603.06086 [hep-ex]].

356-361

(2016)

[133] H. Merkel, P. Achenbach, C. Ayerbe Gayoso, T. Beranek, J. Bericic, J. C. Bernauer,
R. Böhm, D. Bosnar, L. Correa and L. Debenjak, et al. Phys. Rev. Lett. 112, no.22,
221802 (2014) doi:10.1103/PhysRevLett.112.221802 [arXiv:1404.5502 [hep-ex]].
[134] A. Aboubrahim, W. Z. Feng, P. Nath and Z. Y. Wang, Phys. Rev. D 103, no.7, 075014
(2021) doi:10.1103/PhysRevD.103.075014 [arXiv:2008.00529 [hep-ph]].

55
