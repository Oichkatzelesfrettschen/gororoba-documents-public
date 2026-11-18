Source: https://arxiv.org/abs/2602.21774v1
PDF sha256: 00af215402ece60a6228fdfcc5b20f9bb64946230f5ad3f798fb279b569ed3b4
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of yildiz_2026_dark_sector_fr_gravity.pdf

Transcription of `yildiz_2026_dark_sector_fr_gravity.pdf` in this directory, 31 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-31 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

arXiv:2602.21774v1 [astro-ph.CO] 25 Feb 2026

Linear Perturbations and Multi-Probe
Diagnostics in Dark-Sector Selective f (R, Tχ)
Gravity
L. Yıldız∗1 , D. Kaykı†2 , and E. Güdekli‡3
1,2,3

Department of Physics, Faculty of Science, Istanbul University,
Istanbul 34134, Turkey

Abstract
We develop a dark-sector selective trace-coupled extension of gravity in which the matter–curvature coupling depends exclusively on the
trace of the dark-matter energy–momentum tensor, Tχ , defined from a
canonical dark-matter field χ. This construction provides a microphysically specified trace sector, removes the usual matter-Lagrangian ambiguity of f (R, T )-type models, and preserves minimal coupling of visible
matter by design. We derive the full field equations, the exact darksector exchange structure, and the linear scalar-perturbation system in
gauge-ready form. In the sub-horizon regime, we derive effective modifiedgravity functions governing structure growth and light deflection, and
show that the model generically produces correlated, scale- and timedependent departures from General Relativity in growth and lensing observables. Building on this structure, we formulate a perturbation-focused
multi-probe framework based on redshift-space distortions, weak lensing, and CMB lensing, explicitly targeting degeneracy breaking beyond
background-expansion tests. The analysis establishes the action-level and
perturbation-level foundations of the model and provides a conservative,
reproducible framework for translated linear-regime constraints within a
dark-sector selective modified-gravity setting.

Keywords: dark sector, f (R, T ) gravity, trace coupling, cosmological perturbations, structure growth, gravitational lensing
Highlights
• Dark-sector-only Tχ coupling removes direct visible-matter trace coupling
at the action level
∗ li.yildiz.na@gmail.com

† deha.kayki@ogr.iu.edu.tr
‡ gudekli@istanbul.edu.tr

1

## PDF page 2

• Microphysical canonical-χ construction removes the Lm ambiguity of f (R, T )type models
• Linear scalar perturbations yield scale- and time-dependent growth and
lensing signatures
• Perturbation-level multi-probe diagnostics target background-only degeneracies in modified gravity

1

Introduction

The physical nature of the dark sector remains one of the most persistent
open problems in fundamental physics and cosmology [2, 5]. The concordance
ΛCDM framework provides an excellent effective description of a broad range
of observations[1], yet it leaves the microphysics of dark matter and dark energy unspecified [2, 5]. This motivates theoretically controlled extensions that
are both internally consistent and empirically testable [4, 5]. In particular,
many beyond-ΛCDM scenarios are nearly degenerate at the level of background
expansion, so their viability must be assessed primarily through perturbationsensitive signatures such as the growth of cosmic structure and the deflection of
light [3, 4, 29]. A modified-gravity framework aimed at the dark sector should
therefore deliver predictive, falsifiable correlations between growth and lensing
observables rather than relying on background fits alone [4, 5].
Trace-coupled modifications of gravity provide a phenomenologically rich
arena to explore such signatures [6, 8]. In the standard f (R, T ) class, the gravitational Lagrangian depends on the Ricci scalar R and the trace of the matter
stress-energy tensor T , enabling an effective interaction between matter and geometry [6]. However, two recurrent issues arise in generic f (R, T ) constructions
[6, 7]. First, the theory can inherit an ambiguity associated with the choice of
the matter Lagrangian density Lm and the related tensor Θµν , which affects the
precise form of the field equations and the exchange terms. Second, if visible
matter couples directly to the modified sector, baryonic fifth-force constraints
and local tests of gravity can severely restrict the parameter space [9, 8]. These
issues become particularly acute when one attempts to build a predictive perturbation theory suitable for confrontation with large-scale-structure and lensing
measurements [4, 8].
In this work we address both problems by introducing a dark-sector selective
trace coupling in which the modified-gravity dependence on the matter trace is
restricted to the dark-matter sector only, T → Tχ . Visible matter components
(baryons and radiation) remain minimally coupled by construction, suppressing
direct baryonic fifth-force effects at the level of the fundamental action. In
addition, we define the dark matter microphysically by a canonical field χ, so
(χ)
that Tχ and Θµν are uniquely determined. This choice removes the standard
Lm ambiguity and yields an unambiguous exchange structure between the dark
sector and the modified gravitational dynamics.

2

## PDF page 3

The construction is intended as a minimal, physically interpretable, and
observationally testable effective framework, rather than a unique UV-complete
theory. Its purpose is to isolate curvature–dark-sector coupling effects in the sector where late-time cosmological degeneracies are most likely to appear, while
preserving a clean separation from visible-sector dynamics at the level of the
fundamental action. This separation does not imply that visible-sector observables are unaffected; rather, their response is mediated indirectly through the
modified gravitational dynamics, not through a direct trace coupling in the matter action. In this sense, the model provides a controlled setting in which the
impact of selective trace coupling can be tracked consistently from background
evolution to linear perturbations and, ultimately, to multi-probe observables.
Our primary goal is to develop a perturbation-complete and observationally
relevant framework for this class of models. We derive the full field equations and
the exact dark-sector exchange relations implied by the selective coupling, and
we obtain the linear scalar perturbation system in a gauge-ready form suitable
for direct implementation in numerical pipelines. In the sub-horizon regime, we
show how the theory can be mapped to effective modified-gravity functions that
control the clustering of matter and the deflection of light, enabling predictions
for redshift-space distortions (via f σ8 ) and for weak and CMB lensing [16, 4, 8].
This multi-probe focus is essential to break background-level degeneracies and
to isolate signatures that distinguish the model from General Relativity and
ΛCDM [3, 4, 5].
Positioning relative to other modified-gravity frameworks. The construction is intended to occupy an intermediate position between fully generic
trace-coupled models and purely phenomenological late-time parameterizations.
Compared with generic f (R, T ) theories, the restriction T → Tχ and the microphysical canonical-scalar realization of the dark sector remove the usual matterLagrangian ambiguity and prevent direct trace coupling to visible matter at the
level of the fundamental action, while retaining a non-trivial matter–curvature
exchange structure in the dark sector [6]. Compared with pure f (R) models, the
selective R Tχ and Tχ2 channels enlarge the perturbation-level phenomenology
by introducing an explicit dark-sector trace response in addition to the standard
curvature (scalaron) sector [10]. Finally, unlike model-independent effective descriptions that parameterize modified growth and lensing directly at the level of
linear perturbations (e.g. EFT/Horndeski-inspired or (µ, Σ)-type approaches),
the framework retains an explicit action-level parametrization with a transparent map from Lagrangian coefficients (α, ξ, β) to background and perturbation
quantities, which is useful for implementation-ready and falsifiable multi-probe
inference analyses [11, 12, 13].
From the viewpoint of local-gravity phenomenology, the selective restriction T → Tχ is also advantageous: because visible matter remains minimally
coupled in the matter action, the model avoids direct baryonic trace-coupling
effects at the fundamental level. This does not eliminate the need for screening
or local-gravity consistency tests, since visible-sector observables can still be af-

3

## PDF page 4

fected indirectly through the modified gravitational dynamics, but it provides a
cleaner starting point than generic trace-coupled constructions for incorporating
environment-dependent screening mechanisms.
The paper is organized as follows. In Sec. 2 we introduce the dark-sector selective f (R, Tχ ) action, define the microphysical dark-matter sector, and derive
the field equations together with their conservation and exchange structure. In
Sec. 3 we specialize the theory to an FLRW background and obtain the modified
cosmological evolution equations. In Sec. 4 we derive the linear perturbation
equations and identify the effective functions governing growth and lensing. In
Sec. 5 we connect the theoretical predictions to perturbation-sensitive observables and outline a multi-probe inference strategy. We conclude in Sec. 8 with
a summary and outlook.

2

Dark-sector selective f (R, Tχ ) framework

2.1

Conventions and definitions

We adopt metric signature (−, +, +, +) and units c = ℏ = 1. The covariant
derivative is ∇µ and □ ≡ g µν ∇µ ∇ν . We define the partial derivatives of the
gravitational function as
fR ≡

2.2

∂f
,
∂R

fT ≡

∂f
.
∂Tχ

(1)

Action and matter content

We consider a trace-coupled extension in which the gravitational trace dependence is restricted to the dark-matter trace Tχ , while visible components remain
minimally coupled. The action is
[
]
∫
1
4 √
S = d x −g
f (R, Tχ ) + Lb + Lrad + Lχ ,
(2)
2κ2
where κ2 ≡ 8πG and Lb and Lrad denote baryons and radiation.
This construction is adopted as a dark-sector selective extension of the
f (R, T ) framework [6], in which the trace dependence of the gravitational sector
is restricted to Tχ rather than the total matter trace. The motivation is twofold:
it preserves a clean phenomenological separation between visible-sector dynamics and dark-sector backreaction channels, and it isolates the modified coupling
to the sector where late-time cosmological degeneracies and beyond-ΛCDM signatures are most naturally probed in a controlled way. In this sense, the model
is treated throughout as a minimal, physically interpretable, and observationally
testable effective framework, rather than a unique UV-complete theory.
To remove the usual matter-Lagrangian ambiguity present in generic f (R, T )
scenarios, we define dark matter microphysically as a canonical scalar field χ,
1
Lχ = − g µν ∂µ χ ∂ν χ − V (χ).
2
4

(3)

## PDF page 5

(χ)

The corresponding stress-energy tensor follows from Tµν ≡ − √2−g
giving
]
[
1
2
(χ)
(∂χ) + V (χ) ,
Tµν = ∂µ χ ∂ν χ − gµν
2

√
δ( −gLχ )
,
δg µν

(4)

with (∂χ)2 ≡ g ρσ ∂ρ χ ∂σ χ. Its trace is
(χ)
Tχ ≡ g µν Tµν
= −(∂χ)2 − 4V (χ).

(5)

With the canonical choice (3), both Tχ and the metric variation entering
(χ)
Θµν are fixed uniquely, so the fT -induced exchange terms are defined without
the matter-Lagrangian ambiguity that affects generic phenomenological f (R, T )
implementations [6, 7].
The restriction T → Tχ in Eq. (2) defines a dark-sector selective matter–
curvature coupling. Visible matter is assumed to be minimally coupled through
Lb and Lrad , so that standard local constraints associated with direct baryonic
couplings are avoided at the level of the fundamental action [9, 8]. This does
not imply that visible-sector observables are unaffected; rather, their response is
mediated indirectly through the modified gravitational dynamics, not through a
direct trace coupling in the matter action. In the next subsection we derive the
modified field equations and the exact exchange structure induced by fT ̸= 0,
which will be the basis for the background and linear perturbation analysis.

2.3

Field equations and dark-sector exchange structure

Varying the action (2) with respect to the metric yields the modified field equations. Writing fR ≡ ∂f /∂R and fT ≡ ∂f /∂Tχ , one obtains
(
)
(
)
1
(b)
(rad)
(χ)
(χ)
+ Tµν
+ Tµν
fR Rµν − f gµν + (gµν □ − ∇µ ∇ν ) fR = κ2 Tµν
− fT Tµν
+ Θ(χ)
,
µν
2
(6)
(χ)

where the tensor Θµν is defined by
(χ)

αβ
Θ(χ)
µν ≡ g

δTαβ

δg µν

.

(7)

Because the trace coupling is restricted to Tχ , only the dark-matter sector enters
the fT term; visible matter remains minimally coupled.
(χ)

Closed form of Θµν for canonical χ
(χ)

For the canonical scalar field defined in Eq. (3), Θµν is uniquely determined.
Using the standard identity for minimally coupled matter, one finds the closed
form [6, 7]
[
]
1
2
(χ)
(χ)
Θµν = −2 Tµν + gµν Lχ = gµν
(∂χ) + V (χ) − 2 ∂µ χ ∂ν χ.
(8)
2
5

## PDF page 6

A particularly useful simplification is
(χ)
Tµν
+ Θ(χ)
µν = − ∂µ χ ∂ν χ,

(9)

which makes the structure of the trace coupling especially transparent.
The canonical scalar-field description (3) is adopted as a minimal microphysical realisation of the dark sector that fixes Tχ and the metric variation
(χ)
entering Θµν unambiguously, thereby enabling a perturbation-complete and
implementation-ready formulation of the theory. We do not interpret χ as a
unique fundamental particle-physics model of dark matter; rather, it serves as a
representative low-energy effective degree of freedom capturing a broad class of
scalar dark-matter scenarios (e.g. ultralight/axion-like fields or moduli in cosmology) at the level relevant for background and linear-perturbation dynamics
[17, 18, 19]. The framework can be straightforwardly generalised to other darkmatter Lagrangians if desired, with the present choice providing the minimal
benchmark required for transparent multi-probe predictions. Extensions to noncanonical scalar sectors or fluid/field effective descriptions can be treated within
the same selective-coupling strategy, but are beyond the scope of the present
perturbation-benchmark study.
Conservation laws and dark-sector exchange
Since baryons and radiation appear only through minimal couplings in Lb and
Lrad , they satisfy the standard conservation laws,
(b)
∇µ Tµν
= 0,

(rad)
∇µ Tµν
= 0.

(10)

In contrast, the dark sector generally exchanges energy-momentum with the
modified gravity sector when fT ̸= 0. The non-conservation equation implied
by the Bianchi identity and Eq. (6) can be written as [6]
[(
]
) ∇µ f
1
fT
T
(χ)
µ (χ)
(χ)
Tµν
+ Θ(χ)
+
∇
Θ
−
∇
T
(11)
∇µ Tµν
= 2
ν χ .
µν
µν
κ − fT
fT
2
Using Eq. (9), the first term becomes explicitly proportional to ∂µ χ ∂ν χ, making
the dark-sector selective nature of the exchange manifest.

3

Background cosmology

3.1

FLRW setup

We consider a spatially flat FLRW background with cosmic time t,
ds2 = −dt2 + a2 (t) δij dxi dxj ,

(12)

where a(t) is the scale factor and H ≡ ȧ/a is the Hubble rate. For this background,
(
)
R = 6 2H 2 + Ḣ ,
(13)
6

## PDF page 7

and we assume a homogeneous dark-matter field χ = χ(t).
The standard background densities of baryons and radiation are denoted by
ρb and ρrad , with pressures pb ≃ 0 and prad = ρrad /3. For the canonical field χ,
the background energy density and pressure are
ρχ =

1 2
χ̇ + V (χ),
2

pχ =

1 2
χ̇ − V (χ),
2

(14)

so that ρχ + pχ = χ̇2 . The trace defined in Eq. (5) becomes
Tχ = χ̇2 − 4V (χ),

(15)

and hence fR (t) and fT (t) are time dependent through R(t) and Tχ (t).

3.2

Modified Friedmann equations
(χ)

(χ)

Using Eq. (6) and the identity Tµν + Θµν = −∂µ χ ∂ν χ from Eq. (9), the 00
component yields
3H 2 fR = κ2 (ρb + ρrad + ρχ ) + fT χ̇2 +

1
(fR R − f ) − 3H f˙R .
2

The spatial components give
(
)
1
− 2Ḣ + 3H 2 fR = κ2 (prad + pχ ) − (fR R − f ) + f¨R + 2H f˙R .
2

(16)

(17)

Combining Eqs. (16) and (17) produces the useful form
−2Ḣ fR = κ2 [(ρb + pb ) + (ρrad + prad ) + (ρχ + pχ )] + fT χ̇2 + f¨R − H f˙R , (18)
where pb ≃ 0.
Figure 1 makes explicit that the late-time bound on fR0 constrains primarily
the combination 2αR0 + ξTχ0 , leading to a degeneracy direction in the (α̂, ˜
ξ)
plane. In the remainder of the paper we therefore treat the model parameters
in a genuinely multi-probe way (and, in practice, through normalized parameter
combinations): background information alone constrains only limited combinations, whereas growth and lensing respond differently to the scalaron-mediated
(curvature) sector and to the selective trace source [3, 4, 8, 16]. Combining
f σ8 with weak/CMB lensing therefore provides the main route to break this
degeneracy at the level of linear perturbations [4, 5, 16]..

3.3

Visible-sector conservation and dark-sector evolution

Because baryons and radiation are minimally coupled, Eq. (10) implies the
standard continuity equations,
ρ̇b + 3Hρb = 0,

ρ̇rad + 4Hρrad = 0.

(19)

The dark sector generally exchanges energy with the modified gravity sector
when fT ̸= 0 [6]. A convenient way to encode the background dynamics is
7

## PDF page 8

˜ plane for the polynomial
Figure 1: Translated late-time constraint in the (α̂, ξ)
2
2
model f (R, Tχ ) = R+αR +ξRTχ +βTχ , using the benchmark cap log10 |fR0 | <
−4.18 and the dust-level approximation Tχ0 ≃ −ρχ0 . Here α̂ ≡ αH02 and
ξ˜ ≡ ξρc0 . The shaded strip shows the allowed region satisfying |fR0 | = |2αR0 +
ξTχ0 | < 10−4.18 , illustrating the parameter-combination degeneracy beyond the
pure-α and pure-ξ˜ limits (dashed/dotted lines).

8

## PDF page 9

through the modified equation of motion obtained by varying the action with
respect to χ. Denoting V,χ ≡ dV /dχ, the homogeneous field satisfies
(

fT
1+ 2
κ

)

(
)
f˙T
2fT
(χ̈ + 3H χ̇) + 2 χ̇ + 1 + 2 V,χ = 0.
κ
κ

(20)

Equivalently, the dark-matter energy density obeys a modified continuity equation,
ρ̇χ + 3H (ρχ + pχ ) = Qχ ,
(21)
where, using Eq. (20),
f˙T
fT
Qχ = χ̇ (χ̈ + 3H χ̇ + V,χ ) = − 2
χ̇2 − 2
V,χ χ̇.
κ + fT
κ + fT

(22)

This term quantifies the background-level energy exchange induced by the selective trace coupling.

3.4

Consistency conditions and GR limit

The General Relativity limit is recovered when f (R, Tχ ) → R so that fR → 1
and fT → 0, in which case Eqs. (16)–(22) reduce to the standard Friedmann
system with a canonical scalar field. For a well-defined background evolution,
the theory must also avoid singular denominators, in particular κ2 ± fT ̸= 0
wherever Eqs. (11) and (22) are used, and it must satisfy the usual positivity
requirement fR > 0 to prevent an effective sign flip of the gravitational coupling
[10, 20].
Viability and stability cuts. In addition to the GR limit and the absence
of singular denominators, we impose linear-viability conditions for a predictive
late-time cosmology:
fR > 0,

fRR > 0,

K ≡1+

fT
> 0,
κ2

(23)

where fRR > 0 ensures Dolgov–Kawasaki stability in the curvature sector [21,
10, 20] and K > 0 guarantees that the coefficient of δ χ̈ in the perturbed Klein–
Gordon equation (Eq. 46) remains positive, avoiding ghost-like kinetic behavior
of χ fluctuations.
Effective dust regime of χ. Although the selective trace source is defined
using a canonical scalar field χ, the late-time large-scale observables considered
here are most directly interpreted when the dark sector clusters effectively as
pressureless matter. This is consistently realized, for instance, by an oscillating
scalar in an approximately quadratic potential in the regime mχ ≫ H, for which
time-averaging yields ⟨wχ ⟩ ≃ 0 and hence ⟨Tχ ⟩ ≃ −⟨ρχ ⟩ (up to corrections
suppressed by H/mχ ) [22, 17, 18]. In this limit, the standard growth equation

9

## PDF page 10

Figure 2: Redshift evolution of the quasi-static transition scale ktrans (z) ≃
a Meff (z) for viable benchmark points in the (α̂, ˜
ξ) plane, using the polynomial
model f (R, Tχ ) = R + αR2 + ξRTχ + βTχ2 and the effective mass expression in
Eq. (68). The plotted curves use the dust-regime benchmark closure ⟨V ⟩ ≃ ρχ /2
2
(oscillating quadratic scalar), yielding Meff
/H02 = [1−2 ˜
ξΩχ0 (1+z)3 ]/(6α̂). This
figure identifies the scale at which scalaron-mediated modifications are expected
to transition in the quasi-static regime [10, 22].

10

## PDF page 11

used in Sec. 5 applies, while the selective coupling effects enter through (fT , δfT )
and the additional source terms derived in Sec. 4.
More precisely, the dust-like closure adopted here assumes that the background field oscillates around a locally quadratic minimum, V (χ) ≃ 12 m2χ χ2 ,
with oscillation frequency mχ much larger than the Hubble rate over the latetime redshift range relevant to the linear observables considered. In this adiabatic/averaged regime, residual pressure and gradient contributions are suppressed on sufficiently large scales [22, 18]. Correspondingly, the perturbationlevel mapping developed here is formulated for the late-time large-scale linear
regime in which the oscillation-averaged effective dust approximation is valid.
Within this regime, the standard dust-based variable f σ8 can be used consistently in the linear observational mapping employed in Sec. 5. The present
construction therefore targets the perturbation-level, late-time large-scale sector, while preserving the selective-coupling modifications through (fT , δfT ) and
the extra source terms derived in Sec. 4.

4

Linear cosmological perturbations

4.1

Newtonian gauge and perturbation variables

We work with scalar perturbations around the flat FLRW background in Newtonian gauge [23],
ds2 = −(1 + 2Ψ) dt2 + a2 (t)(1 − 2Φ) δij dxi dxj ,

(24)

where Ψ(t, x) and Φ(t, x) are the Bardeen potentials. The dark-matter field is
decomposed as
χ(t, x) = χ̄(t) + δχ(t, x),
(25)
and similarly for all background quantities. We denote Fourier modes by δX(t, x) =
∫ d3 k
ik·x
.
(2π)3 δX(t, k) e
For later use, we define the total (visible + dark) matter density perturbation
by δρ ≡ δρb + δρrad + δρχ , and introduce the velocity potentials vI (for each
(I)
species I) through δui = ∂i vI at linear order.

4.2

Perturbations of Tχ and of the coupling functions

The trace Tχ defined in Eq. (5) perturbs as Tχ = T̄χ + δTχ . For the canonical
scalar field in Newtonian gauge, keeping only linear terms, one finds
δTχ = 2χ̄˙ δ χ̇ − 2Ψ χ̄˙ 2 − 4V,χ δχ,

(26)

where V,χ ≡ dV /dχ is evaluated on the background.
Since fR and fT depend on (R, Tχ ), their perturbations are
δfR = fRR δR + fRT δTχ ,

(27)

δfT = fT R δR + fT T δTχ ,

(28)

11

## PDF page 12

where fRR ≡ ∂ 2 f /∂R2 , fRT ≡ ∂ 2 f /(∂R ∂Tχ ), and fT T ≡ ∂ 2 f /∂Tχ2 are evaluated on the background. The Ricci-scalar perturbation δR is obtained from
Eq. (24) and will enter the linearized field equations through Eqs. (27)–(28).
For concreteness and parameter-level interpretability, we adopt the minimal
polynomial realization
f (R, Tχ ) = R + αR2 + ξRTχ + βTχ2 ,

(29)

as an effective expansion around the GR limit. These relations also clarify
the parameter roles at linear order in this parametrization: α enters primarily
through the curvature-response sector (via fRR and the effective scalaron scale),
ξ mixes curvature and dark-sector trace perturbations through fRT = fT R , and
β controls the leading trace-sector response through fT T . As a result, different
observables probe different combinations of (α, ξ, β): background information
alone is generally insufficient to separate them, whereas growth and lensing
respond differently to the curvature and trace-coupling channels [8, 4, 16].

4.3

Effective functions for growth and lensing

A key objective is to connect the linearized system to perturbation-sensitive
observables. In Fourier space, and in the sub-horizon regime, the scalar sector
can be parameterized by effective modified-gravity functions µ(k, a) and η(k, a)
defined via [16, 4]
k 2 Ψ ≡ −4πG a2 µ(k, a) ρm ∆m ,

η(k, a) ≡

Φ
,
Ψ

(30)

where ρm is the background total matter density (typically baryons plus the
clustering dark component), and ∆m is the gauge-invariant comoving matter
density contrast [23].
No double counting between ρm ∆m and ΠDS . In our notation, ρm ∆m
denotes the standard comoving clustering source entering the phenomenological
definitions of µ and Σ, including the clustering dark component in the effective
dust regime. The additional term ΠDS introduced in the QS Poisson constraint
(Eq. 60) collects only the selective trace-coupling contributions proportional
to (fT , δfT ) and vanishes in the GR limit fT → 0; therefore ΠDS should be
interpreted as an extra modified-gravity source, not as a second counting of the
matter density perturbation.
The Weyl (lensing) potential is controlled by Φ + Ψ, and it is convenient to
define [16, 4]
k 2 (Φ + Ψ) ≡ −8πG a2 Σ(k, a) ρm ∆m ,

Σ(k, a) ≡

µ(k, a)
[1 + η(k, a)] . (31)
2

In the following subsections we derive the full linearized equations from Eq. (6)
and identify µ(k, a) and η(k, a) explicitly in terms of the model functions and
background evolution, enabling direct confrontation with redshift-space distortions (via f σ8 ) and lensing data.
12

## PDF page 13

4.4

Perturbed dark-matter stress–energy

For the canonical field χ defined in Eq. (3), the linear perturbations of energy
density, pressure, and momentum density in Newtonian gauge are [23, 24]
δρχ = χ̄˙ δ χ̇ − χ̄˙ 2 Ψ + V,χ δχ,
δpχ = χ̄˙ δ χ̇ − χ̄˙ 2 Ψ − V,χ δχ,
(χ)
δT0i = − χ̄˙ ∂i δχ

(32)
(33)

(ρ̄χ + p̄χ ) vχ = − χ̄˙ δχ,

⇒

(34)

where V,χ ≡ dV /dχ is evaluated on the background.

4.5

Linearized field equations and robust slip relation

Define the geometric operator
1
Eµν ≡ fR Rµν − f gµν + (gµν □ − ∇µ ∇ν ) fR .
2
The field equations (6) can be written compactly as
(
)
(b)
(rad)
(χ)
(χ)
Eµν = κ2 Tµν
+ Tµν
+ Tµν
− fT Sµν ,
Sµν ≡ Tµν
+ Θ(χ)
µν .

(35)

(36)

For canonical χ, Eq. (9) implies the exact identity
Sµν = −∂µ χ ∂ν χ.

(37)

At the background level one has S̄00 = −χ̄˙ 2 and S̄0i = S̄ij = 0. At linear order
this gives the particularly simple perturbations
δS00 = −2χ̄˙ δ χ̇,

δS0i = −χ̄˙ ∂i δχ,

δSij = 0 (to first order).

(38)

Therefore, the linearized field equations take the schematic but exact form
(tot)
δEµν = κ2 δTµν
− f¯T δSµν − δfT S̄µν ,

(39)

(tot)

where δTµν includes baryons, radiation, and χ.
A key robust consequence follows from the traceless spatial (ij) sector. Since
δSij = 0 at linear order and the canonical scalar has no anisotropic stress, the
traceless ij equation yields the gravitational slip sourced purely by δfR [10, 20],
δfR
Φ−Ψ= ¯ .
fR

(40)

In the next subsection we will compute the explicit 00 and 0i components of
Eq. (39) in Fourier space and then extract µ(k, a) and η(k, a) consistently with
Eqs. (30)–(31).

13

## PDF page 14

Figure 3: Diagnostic quasi-static scalaron response kernel, Rs (k, z) = k 2 /[k 2 +
2
(z)], for viable benchmark points of the selective dark-sector f (R, Tχ )
ktrans
model, where ktrans (z) ≃ a Meff (z) is determined by the effective mass derived
in Sec. 4.11. Solid (dashed) curves denote z = 0 (z = 2). This plot isolates
the scale at which scalaron-mediated modifications become active and provides
a theory-level bridge between the effective-mass sector and the scale-dependent
growth/lensing observables reconstructed in the quasi-static regime.

4.6

Linearized modified Klein–Gordon equation

The dark-matter field equation follows from varying the action with respect to
χ. It is convenient to introduce the dimensionless coupling
fT
,
K ≡ 1 + B,
C ≡ 1 + 2B,
κ2
so that the exact covariant equation of motion can be written as
B≡

K □χ + ∇µ B ∇µ χ − C V,χ = 0.

(41)

(42)

On the FLRW background this reproduces Eq. (20).
Linearizing Eq. (42) around χ = χ̄ + δχ and B = B̄ + δB yields, to first
order,
K̄ δ(□χ)+δK □χ+∇µ δB ∇µ χ̄+∇µ B̄ ∇µ δχ+δg µν (∂µ B̄)(∂ν χ̄)−C¯ V,χχ δχ−δC V,χ = 0,
(43)
where δK = δB and δC = 2 δB.
The coupling perturbation δB is determined by the gravitational function
through
1
1
(44)
δB = 2 δfT = 2 (fT R δR + fT T δTχ ) ,
κ
κ
with δTχ given in Eq. (26). On the FLRW background, δg 00 = 2Ψ and
˙
δg µν (∂µ B̄)(∂ν χ̄) = 2Ψ B̄˙ χ̄.
14

(45)

## PDF page 15

Finally, the perturbed d’Alembertian acting on χ is defined geometrically by
¯ µ∇
¯ ν χ̄ + ḡ µν δΓρ µν ∂ρ χ̄,
¯ δχ + δg µν ∇
δ(□χ) ≡ δ(g µν ∇µ ∇ν χ) = □

(46)

which can be evaluated explicitly in Newtonian gauge using Eq. (24). In the next
subsection we provide the explicit Fourier-space form and then close the system
for (Φ, Ψ, δχ) to extract µ(k, a) and η(k, a) consistently with Eqs. (30)–(31).

4.7

Explicit Newtonian-gauge form and Fourier-space equation for δχ

Explicit form of δ(□χ)
Evaluating Eq. (46) for the Newtonian-gauge metric (24) and a homogeneous
background χ̄(t) gives
δ(□χ) = −δ χ̈ − 3H δ χ̇ −

(
)
k2
˙ Ψ̇ + 3Φ̇ + 2Ψ (χ̄
¨ + 3H ˙
δχ
+
χ̄
χ̄) ,
a2

(47)

where k is the comoving wavenumber in Fourier space.
Fourier-space linearized modified Klein–Gordon equation
Using Eq. (47) in the compact linear equation (43), and keeping the definitions
K = 1 + B, C = 1 + 2B from Eq. (41), one obtains
( 2
)
(
)
(
)
k
K̄ δ χ̈ + 3H K̄ + B̄˙ δ χ̇ + K̄ 2 + C¯ V,χχ δχ = K̄ χ̄˙ Ψ̇ + 3Φ̇ − 2C¯ V,χ Ψ − χ̄˙ δ Ḃ + δB □χ − 2V,χ δB,
a
(48)
where
¨ + 3H ˙
□χ = −(χ̄
χ̄),

(49)

and the coupling perturbation δB is
δB =

1
(fT R δR + fT T δTχ ) ,
κ2

δTχ = 2χ̄˙ δ χ̇ − 2Ψ χ̄˙ 2 − 4V,χ δχ,

(50)

with all background-dependent coefficients evaluated on (R̄, T̄χ ). Equation (48)
closes the δχ dynamics once δR is specified from the metric perturbations.

4.8

Eliminating δR and closing the system

A practical advantage of the (R, Tχ ) dependence is that δR never needs to
be written explicitly in terms of (Φ, Ψ) in order to close the system. From
Eqs. (27)–(28) we have, at linear order,
δfR = fRR δR + fRT δTχ ,

δfT = fT R δR + fT T δTχ ,

15

(51)

## PDF page 16

with fRT = fT R . We assume fRR ̸= 0 so that δR can be eliminated in favor
of δfR ; the special case fRR = 0 can be treated separately. Solving the first
relation for δR gives
1
(δfR − fRT δTχ ) .
(52)
δR =
fRR
Substituting Eq. (52) into δfT yields an expression that depends only on δfR
and δTχ ,
(
)
2
fRT
fRT
δfT =
δfR + fT T −
δTχ .
(53)
fRR
fRR
Therefore the coupling perturbation δB = δfT /κ2 becomes
(
)
2
1 fRT
1
fRT
δB = 2
δfR + 2 fT T −
δTχ .
κ fRR
κ
fRR

(54)

Using the robust slip relation (40),
δfR = f¯R (Φ − Ψ),

(55)

Eq. (54) can be expressed entirely in terms of (Φ, Ψ) and δTχ . For reference,
the canonical-field trace perturbation is
δTχ = 2χ̄˙ δ χ̇ − 2Ψ χ̄˙ 2 − 4V,χ δχ.

4.9

(56)

Trace equation for the scalaron perturbation δfR

Taking the trace of the field equations (6) gives the exact scalar equation
3□fR + fR R − 2f = κ2 T (tot) − fT S,

(χ)
2
S ≡ g µν (Tµν
+ Θ(χ)
µν ) = −(∂χ) , (57)

where T (tot) is the trace of the total stress-energy tensor (baryons + radiation
+ χ). Linearizing Eq. (57) yields
3 δ(□fR ) + R̄ δfR − f¯R δR − 2f¯T δTχ = κ2 δT (tot) − f¯T δS − δfT S̄,

(58)

with δR eliminated by Eq. (52) and δfT given by Eq. (53). For the canonical
field,
S̄ = χ̄˙ 2 ,
δS = 2χ̄˙ δ χ̇ − 2Ψ χ̄˙ 2 .
(59)
Finally, the perturbed d’Alembertian acting on fR is defined analogously to
Eq. (46) as
¯ µ∇
¯ ν f¯R + ḡ µν δΓρ µν ∂ρ f¯R ,
¯ δfR + δg µν ∇
δ(□fR ) = □

(60)

where f¯R = f¯R (t) in the background.
Equations (48), (58), and (40), together with Eq. (54), provide a gaugeconsistent closure once supplemented by the 00 and 0i constraint equations for
the metric potentials.

16

## PDF page 17

4.10

Quasi-static sub-horizon limit and observable reconstruction

We now specialize to the quasi-static (QS) sub-horizon regime [10, 8],
k2
≫ H 2,
a2

∣ ∣ ∣ ∣
k
k
∣ ∣ ∣ ∣
∣Φ̇∣ , ∣Ψ̇∣ ≪ |Φ| , |Ψ| ,
a
a

∣
∣
k
∣ ˙ ∣
∣δ fR ∣ ≪ |δfR | ,
a

(61)

retaining the leading spatial-gradient terms that control growth and lensing.
QS constraints for the metric potentials
In the QS limit, the linearized field equations (39) reduce to a Poisson-type
constraint for Φ with two distinct sources: (i) the standard clustering source
ρm ∆m and (ii) a dark-sector selective contribution induced by (fT , δfT ) and
δS00 . We write the leading-gradient constraint in the compact form
κ2
1
k 2 δfR
k2
Φ ≃ − ¯ ρm ∆m − ¯ ΠDS (k, a) −
,
2
a
2a2 f¯R
2fR
2fR

(62)

where ΠDS collects the dark-sector selective terms that vanish in the GR limit
and is given by
ΠDS (k, a) ≡ χ̄˙ 2 δfT − f¯T δS00 ,

δS00 = −2χ̄˙ δ χ̇.

(63)

The coupling perturbation δfT is eliminated by Eq. (53), so that ΠDS is expressed entirely in terms of δfR and (δχ, δ χ̇).
The gravitational slip remains exact at linear order,
δfR
Φ−Ψ= ¯ ,
fR

(64)

so that Ψ is obtained from Φ once δfR is known.
QS trace equation for δfR
In the same QS limit, the trace equation (58) becomes an algebraic relation that
determines δfR up to the source terms. Keeping the dominant gradient term
δ(□fR ) ≃ −(k 2 /a2 )δfR and eliminating δR and δfT using Eqs. (52) and (53),
we obtain the schematic QS form
( 2
)
k
2
+
m
(a)
δfR ≃ Stot (k, a) + SDS (k, a),
(65)
f
a2
where m2f (a) is the effective mass term for the scalaron perturbation δfR and
Stot and SDS denote, respectively, the standard trace source (from δT (tot) ) and
the additional dark-sector selective sources involving δTχ and δS. Their explicit
expressions follow uniquely once a concrete model f (R, Tχ ) is specified, because
they depend only on the background derivatives (f¯R , f¯RR , f¯RT , f¯T , f¯T T ) and on
the perturbations (δχ, δ χ̇, Φ, Ψ).
17

## PDF page 18

Reconstruction of µ(k, a), η(k, a) and Σ(k, a)
Given δfR from Eq. (65), the potentials are obtained from Eqs. (62) and (64),
and the observable functions are then read off from their defining relations (30)–
(31):
k 2 (Φ + Ψ)
.
8πGa2 ρm ∆m
(66)
In the GR limit f¯R → 1 and ΠDS → 0 and δfR → 0, one recovers µ = η = Σ = 1.
µ(k, a) = −

4.11

k2 Ψ
,
4πGa2 ρm ∆m

η(k, a) =

Φ
,
Ψ

Σ(k, a) = −

QS scalaron equation and effective mass

In the QS sub-horizon regime, the trace equation provides an algebraic relation
for the scalaron perturbation δfR . Keeping the dominant gradient contribution
δ(□fR ) ≃ −(k 2 /a2 )δfR and eliminating δR and δfT using Eqs. (52) and (53),
one may cast the result in the compact form
( 2
)
]
k
1 [ 2 (tot) ¯
2
+
M
κ
δT
−
f
δS
−
B(a)
δT
(a)
δf
≃
−
,
(67)
T
χ
R
eff
a2
3
where the effective mass and the explicit δTχ -source coefficient are determined
only by background derivatives of f (R, Tχ ):
]
(
[
)
2
1 f¯R − S̄ f¯RT
f¯RT
f¯RT
f¯R − R̄ f¯RR − S̄ f¯RT
2
¯
¯
¯
=
− R̄ ,
B(a) ≡ fR ¯ −2fT +S̄ fT T − ¯
.
Meff (a) ≡
3
3f¯RR
f¯RR
fRR
fRR
(68)
For the canonical field, S̄ = χ̄˙ 2 and T̄χ = S̄ − 4V (χ̄), hence the coefficient
B(a) and the explicit δTχ -source contribution in Eq. (67) are fully determined
by background derivatives of f (R, Tχ ) together with the canonical scalar-sector
perturbations under the QS sub-horizon approximation.

18

## PDF page 19

Figure 4: Diagnostic QS growth-modification map and transition scale.
Two-dimensional map of the diagnostic growth modification µproxy (k, z) − 1 in
the quasi-static sub-horizon regime, displayed over mode scale k/H0 and redshift z. The proxy µproxy (k, z) is constructed from the QS algebraic closure for
the scalaron perturbation in Eq. (67) with the background-defined coefficients
Meff (a) and B(a) given in Eq. (68). The solid curve shows the evolving transition
locus ktrans (z)/H0 , illustrating that the onset of scale-dependent growth departures tracks the effective-mass scale ktrans (z) ≃ aMeff (z). This figure therefore
provides a compact pre-closure diagnostic of where, in the (k, z) plane, the
model predicts the strongest QS growth response.

δS = 2χ̄˙ δ χ̇ − 2Ψ χ̄˙ 2 ,

δTχ = δS − 4V,χ δχ = 2χ̄˙ δ χ̇ − 2Ψ χ̄˙ 2 − 4V,χ δχ. (69)

For the specific polynomial choice in Eq. (29), using f¯RR = 2α, f¯RT = ξ,
f¯T T = 2β and f¯R = 1+2αR̄+ξ T̄χ , one obtains the explicit background functions
[
]
[
]
1 1 + 2αR̄ + ξ T̄χ − ξ S̄
1 1 + ξ(T̄χ − S̄)
1 − 4ξV (χ̄)
2
Meff
(a) =
− R̄ =
=
,
3
2α
3
2α
6α
(70)
and
)
(
(
) ξ
(
)
ξ2
2
˙
B(a) = 1 + 2αR̄ + ξ T̄χ
− 2 ξ R̄ + 2β T̄χ + χ̄ 2β −
.
(71)
2α
2α
19

## PDF page 20

Equation (67), together with the QS constraints (62) and the slip relation (64),
enables a fully explicit reconstruction of µ(k, a), η(k, a), and Σ(k, a) once the
perturbations (δχ, δ χ̇) are related to ρm ∆m via the QS limit of Eq. (48) with
δB from Eq. (44).

5

Observational signatures and inference strategy

5.1

Background expansion observables

Although we work in natural units (c = ℏ = 1) in the theoretical sections, in
this section we restore c when expressing observational distances in conventional
units. Assuming spatial flatness, we compute
∫ z
dz ′
c
,
DM (z) = c
,
DL (z) = (1 + z) DM (z), (72)
DH (z) =
′
H(z)
0 H(z )
and the corresponding distance modulus for Type Ia supernovae [25],
]
[
DL (z)
+ 25.
µSN (z) = 5 log10
Mpc
For BAO analyses we adopt the standard volume-averaged distance
[
]1/3
2
DV (z) = z DM
(z) DH (z)
,

(73)

(74)

and/or the anisotropic pair (DM (z)/rd , DH (z)/rd ), where rd is the sound horizon at the drag epoch computed consistently within the same background cosmology [26, 27].

5.2

Linear growth and lensing in the QS regime

On sub-horizon scales where the QS approximation holds, clustering and lensing
are controlled by the effective functions µ(k, a) and Σ(k, a) defined in Eqs. (30)
and (31) [10, 8, 4]. For each Fourier mode k, the growth of the comoving density
contrast ∆m (k, a) can be written as
(
)
H′
3
∆′′m + 2 +
∆′m − Ωm (a) µ(k, a) ∆m = 0,
(75)
H
2
where primes denote derivatives with respect to ln a and Ωm (a) ≡ κ2 ρm /(3H 2 ).
Redshift-space distortions constrain f σ8 (z) with
f (z) ≡

d ln ∆m
,
d ln a

f σ8 (z) = f (z) σ8 (z),

(76)

while weak lensing and CMB lensing constrain the Weyl potential through
Σ(k, a),
k 2 (Φ + Ψ) = −8πGa2 Σ(k, a) ρm ∆m .
(77)
20

## PDF page 21

In our framework, µ, η and Σ are reconstructed from Eqs. (62), (64), and (66),
using δfR obtained from the QS trace equation (67) and the model derivatives
in Sec. 2.

Figure 5: Transition-sensitivity ridge of the quasi-static (QS) growth
diagnostic. Heat map of the logarithmic response measure Tµ (k, z) ≡
∂µproxy (k, z)/∂ ln k across the (k, z) plane (horizontal axis: log10 (k/H0 ); vertical axis: redshift z), for the same Benchmark C setup adopted in the preceding
analysis. The bright ridge delineates the scale band where the reconstructed
QS growth response becomes maximally sensitive to mode scale, marking the
effective transition between GR-like behavior and the modified-gravity scalar
sector in the QS limit. The solid curve overlays the predicted transition locus
k = ktrans (z), highlighting that the strongest scale sensitivity tracks the evolving QS transition scale inferred from the effective-mass sector. The color bar
reports the computed range of Tµ for this benchmark.
Figure 5 visualizes where the QS reconstruction becomes most scale-sensitive
in the (k, z) plane, and shows that the resulting sensitivity ridge follows the
transition locus ktrans (z) identified from the effective-mass sector.

5.3

Data vector design for multi-probe inference

We define an implementation-ready multi-probe data-vector structure designed
to separately test (i) the background expansion and (ii) the growth and lensing
21

## PDF page 22

sector:
D = {BAO, SN, f σ8 , WL, CMB lensing} .

(78)

Geometric probes (BAO+SN) mainly constrain H(z) and distances, while latetime clustering and lensing probe the scale and time dependence of µ(k, a) and
Σ(k, a) in the linear regime. As representative contemporary choices (included
here only as concrete examples of the probe classes entering the inference design), one may consider DESI DR2 BAO measurements, the Pantheon+ SN
compilation, DES Y6 weak-lensing and clustering products, and ACT DR6 CMB
lensing products.

5.4

Effective-likelihood construction and sampling blueprint

Assuming independent Gaussian likelihoods (or using published covariances
when available), the total log-likelihood can be written in the standard form
∑
T
−2 ln Ltot =
(dX − tX (θ)) C−1
(79)
X (dX − tX (θ)) ,
X

where dX and CX denote the data vector and covariance for probe X, and
tX (θ) are the corresponding theory predictions. This expression defines the
effective-likelihood layer used to map the present perturbation-level formulation
to an implementation-ready inference pipeline. Within the scope of this work,
it is used as a sampling blueprint and parameter-structure map for translated
linear-regime consistency diagnostics, rather than as a completed Boltzmannlevel survey fit.

5.5

Stability cuts and theory priors

To ensure viability throughout the late-time redshift range targeted by the observational mapping considered here, we impose hard stability cuts:
f¯R (a) > 0,

(80)

α > 0,
|f¯T (a)| ≪ κ2 at late times,

(81)
(82)

2
Meff
(a) > 0,

(83)

together with the non-singularity conditions summarized in Sec. 3.4. The priors
Π(θ) are taken broad and minimally informative on cosmological parameters,
while (α, ξ, β) are sampled in log-space over ranges that keep the QS reconstruction valid and avoid strong-coupling regimes.
Scope of the present stability analysis. The stability conditions imposed
above are intended as linear-viability requirements for the late-time regime considered in this work, i.e. for background evolution, quasi-static perturbations,
and the effective-likelihood mapping to growth/lensing observables. They do

22

## PDF page 23

not constitute a full non-linear stability proof of the theory. A dedicated nonlinear treatment (including mode coupling and small-scale structure formation
effects) is beyond the scope of the present analysis.

6

Observational inputs and likelihood

In the absence of a dedicated Boltzmann-code implementation for the present
f (R, Tχ ) realization (including the selective dark-sector coupling), we adopt a
conservative constraint-translation strategy: we anchor the late-time, linearscale departures from GR to current bounds on phenomenological modifiedgravity functions and on the present-day scalar response in viable f (R)-like
scenarios.
By construction, the present inference layer is restricted to late-time linear
(or quasi-static linear) observables. We do not model non-linear structure formation, halo-scale clustering, or screening/environmental effects in this work,
since these require a dedicated Boltzmann implementation coupled to a calibrated non-linear pipeline. Accordingly, all translated constraints reported below should be interpreted as conservative linear-regime benchmarks rather than
full non-linear parameter bounds. Theoretical viability is enforced separately
through the stability cuts and theory priors introduced in Sec. 5.5.
This choice should be viewed as a conservative intermediate step between a
formal theoretical formulation and a full Boltzmann-level data analysis: while
it does not provide direct spectrum-level constraints, it yields a non-trivial and
falsifiable late-time benchmark through translated bounds on (fR0 , µ0 , Σ0 ) combined with theory-viability cuts [28].

6.1

Phenomenological bounds on µ and Σ

We use updated constraints on the (µ, Σ) parameterization inferred from joint
CMB and late-time probes. In particular, Andrade et al. report (for a combined
analysis including ACT, WMAP and late-time datasets)
µ0 − 1 = 0.02 ± 0.19,

Σ0 − 1 = 0.021 ± 0.068,

(84)

at 68% confidence level [14]. These constraints are consistent with GR and provide a robust benchmark for allowing (or excluding) percent-level modifications
to clustering and lensing at z ≃ 0.

6.2

Benchmark bound on the present-day scalar response

For viable f (R)-type theories, an informative late-time handle is the present-day
quantity fR0 ≡ fR (R0 ) − 1, which controls the effective gravitational strength
on linear scales (in the quasi-static regime, µ ≃ 1/fR up to scale-dependent corrections; see, e.g., [10]). As a representative benchmark from galaxy clustering
× CMB lensing cross-correlations, Kou et al. report 95% limits on |fR0 | at the

23

## PDF page 24

level
log10 |fR0 | < −4.18

(95% CL),

(85)

with the precise number depending mildly on analysis choices [15]. We adopt
Eq. (85) as a conservative cap on the present-day scalar response for any model
whose late-time linear phenomenology reduces to an fR -controlled effective Newton constant.

6.3

Effective likelihood layer

Parameter response map and degeneracy considerations. At the level
of linear perturbations, the three coefficients play qualitatively different roles.
The curvature coefficient α controls the scalaron response scale (through the
effective curvature sector), the mixing coefficient ξ controls the strength of
the selective curvature–dark-sector trace coupling, and β governs the leading
trace-sector self-interaction. Consequently, late-time constraints often act primarily on parameter combinations rather than on each coefficient separately
(e.g. through the present-day scalar response). In particular, the translated fR0
bound constrains a combination of (α, ξ) at z = 0, while the (µ0 , Σ0 ) consistency
layer provides an additional phenomenological handle on the relative impact
of curvature and lensing-sector modifications. A full multi-probe degeneracybreaking analysis using growth and lensing observables across redshift is deferred to future work with a dedicated Boltzmann-code implementation; here
we retain a conservative effective-likelihood layer designed to preserve parameter
interpretability while avoiding over-claiming.
We implement Eq. (85) as a Gaussian pseudo-likelihood for fR0 centered on
GR,
]
[
10−4.18
(fR0 − 0)2
,
σfR0 ≡
≃ 3.37 × 10−5 ,
(86)
LfR0 ∝ exp −
2
2σfR0
1.96
together with the consistency check that the predicted (µ0 , Σ0 ) remain within
the broad 68% ranges in Eq. (84). This yields a fully specified, non-empty
inference layer that can be upgraded to a full MCMC over LSS/CMB spectra
once a dedicated solver is in place.
Status of the inference layer. The effective likelihood introduced here is
intended as a conservative phenomenological layer, not as a replacement for a full
Boltzmann-level inference from CMB/LSS power spectra and cross-correlations.
Accordingly, the results in this section should be interpreted as translated latetime consistency constraints and parameter-structure diagnostics at the linearresponse level.

24

## PDF page 25

7

Results and discussion

7.1

Translated bounds on the model parameters

For our action f (R, Tχ ) = R + αR2 + ξRTχ + βTχ2 , the background derivative
with respect to R reads
fR = 1 + 2αR + ξTχ .
(87)
Therefore the present-day deviation parameter is
fR0 ≡ fR (R0 , Tχ0 ) − 1 = 2αR0 + ξTχ0 .

(88)

Adopting a flat ΛCDM reference background with Planck-2018 parameters
[1], the present-day Ricci scalar may be written as
)
(
(
)
3
(89)
R0 = 6 2H02 + Ḣ0 = 6 2 − Ωm0 H02 ≃ 9.17 H02 ,
2
where we used Ḣ0 = −(3/2)Ωm0 H02 for matter+Λ.
Using the benchmark constraint (85), Eq. (88) implies a stringent cap on
the parameter combination 2αR0 + ξTχ0 . Two informative limiting cases are:
(i) Pure curvature correction at late times (ξ = 0). Then |fR0 | = |2αR0 |
and
10−4.18
10−4.18
|α|H02 <
≃ 3.60 × 10−6 .
(90)
=
2(R0 /H02 )
2 × 9.17
(ii) Pure selective coupling contribution at late times (α = 0). For a
pressureless dark sector at z ≃ 0, Tχ0 ≃ −ρχ0 , with ρχ0 = Ωc0 ρc0 and ρc0 =
3H02 /κ2 . Defining the dimensionless coupling ξ˜ ≡ ξρc0 , Eq. (88) yields |fR0 | ≃
|˜
ξ|Ωc0 , so that
−4.18
˜ < 10
|ξ|
≃ 2.5 × 10−4 ,
(91)
Ωc0
where we used Ωc0 ≃ 0.264 for the Planck-2018 baseline [1].
To assess how much observational leverage remains within the viable region
implied by Eq. (91), we map the inter-benchmark spread of the reconstructed
QS growth proxy across the (k, z) plane. This highlights the scale–redshift
domain where growth measurements can most efficiently discriminate among
viable selective-coupling benchmarks.

25

## PDF page 26

Figure 6: Inter-benchmark discriminating-power map in the QS growth
sector. Two-dimensional map of the inter-benchmark spread of the recon(b)
(b)
structed QS growth proxy, ∆µspread
proxy (k, z) ≡ maxb µproxy (k, z)−minb µproxy (k, z),
evaluated over the viable selective-coupling benchmark set b (four representative
points, as in Fig. 2). The color scale shows where the QS growth response differs
most strongly across viable benchmarks, providing a direct measure of discriminating power in the (k, z) plane. The thick curve marks the peak-discrimination
ridge, i.e. the locus where ∆µspread
proxy attains its maximum at fixed redshift. Overall, the figure isolates the mode-scale band and redshift range in which growth
data are expected to be most sensitive to selective-coupling realizations while
remaining consistent with the late-time bound in Eq. (91).
Figure 6 therefore identifies the (k, z) domain where viable selective-coupling
benchmarks are maximally separable through QS growth information.

7.2

Consistency with µ0 –Σ0 bounds

Within the quasi-static linear regime, small |fR0 | ≪ 1 implies that departures
in the effective clustering and lensing strengths scale as O(fR0 ) (up to the
usual scale-dependent scalaron corrections) [10]. Given |fR0 | ≲ 10−4.18 , the
predicted late-time (µ0 , Σ0 ) remain automatically compatible with the broader
phenomenological constraints in Eq. (84) [14].

26

## PDF page 27

7.3

Interpretation for the dark sector

The translated bounds (90)–(91) show that any viable late-time realization of
the present f (R, Tχ ) model must be close to GR in terms of the scalar response
fR today. This does not eliminate the model’s novelty: the selective coupling
terms (ξRTχ , βTχ2 ) can still leave distinctive fingerprints in (i) transition dynamics if the dark-sector equation of state departs from dust, (ii) scale-dependent
growth around k/a ∼ Meff (a)the framework implies, and (iii) cross-correlations
where lensing and clustering respond differently to dark-sector stress. A dedicated numerical implementation will enable testing these signatures beyond the
present translated-linear bounds.

8

Conclusions

We developed a dark-sector selective extension of modified gravity in which
the gravitational action depends on the Ricci scalar R and exclusively on the
dark trace Tχ , f (R, Tχ ), thereby avoiding direct visible-sector trace coupling
in the fundamental action and reducing the associated ambiguities and phenomenological tensions that arise in generic trace-coupled constructions. We
derived the background equations and linear perturbation relations in Newtonian gauge, including a closed elimination of δR in favor of δfR and an explicit
expression for δfT that controls the dark-sector selective source entering the
metric constraint. A key outcome is a gauge-consistent perturbation system for
(Φ, Ψ, δχ, δfR ), from which the effective growth and lensing responses µ(k, a)
and Σ(k, a) can be reconstructed in the quasi-static sub-horizon regime.
To obtain explicit late-time implications without requiring a dedicated Boltzmannlevel likelihood pipeline, we adopted a conservative constraint-translation strategy. Using current phenomenological bounds on (µ0 , Σ0 ) together with a representative 95% limit on the present-day scalar response |fR0 | from galaxyclustering × CMB-lensing cross-correlations, we translated these limits into constraints on our minimal polynomial realization f (R, Tχ ) = R + αR2 + ξRTχ +
βTχ2 . This yields translated upper bounds on the late-time parameter combination 2αR0 + ξTχ0 and, in informative limits, on |α|H02 and the dimensionless
selective coupling ξ˜ ≡ ξρc0 under the dust-level approximation Tχ0 ≃ −ρχ0 .
These translated bounds indicate that viable late-time realizations must remain
close to GR in terms of the present-day scalar response fR , while still allowing
qualitatively distinctive signatures through the selective trace channel.
The principal physical novelty of the framework is that it separates the
origin of deviations from GR into two structurally distinct contributions in the
quasi-static metric constraint: scalaron-mediated effects (curvature sector) and
dark-sector selective sourcing. This implies that combined growth and lensing
datasets can, in principle, discriminate a purely f (R)-like modification from
an intrinsically dark-sector-driven departure. In particular, once a full linear
solver is implemented, the model predicts correlated but non-identical scaledependent responses in clustering and lensing, controlled by the transition scale

27

## PDF page 28

k/a ∼ Meff (a) and by the selective source induced by (ξ, β) through δfT and
ΠDS .
A full-likelihood confrontation with CMB/LSS power spectra and crosscorrelations requires a dedicated Boltzmann implementation and is beyond the
scope of the present work. The results reported here are therefore restricted
to translated late-time constraints in the linear/QS regime. Within this scope,
the action-level formulation, exact exchange structure, and perturbation-level
closure derived in this work provide a consistent basis for direct observational
testing of dark-sector selective trace coupling.

A

Technical details and complementary derivations

This Appendix collects technical steps that are useful for reproducibility and
for cross-checking the perturbation algebra, and can be expanded if required by
referees.

A.1

Variation identities and conventions

We summarize the sign conventions, metric signature, and variation identities
used throughout. We work with signature (−, +, +, +) and define
□ ≡ g µν ∇µ ∇ν ,

Rµν = ∂λ Γλ µν − ∂ν Γλ µλ + Γλ λρ Γρ µν − Γλ νρ Γρ µλ .

(92)

The variation of the Ricci scalar is written in the standard form
δR = Rµν δg µν + g µν δRµν ,

A.2

δRµν = ∇λ δΓλ µν − ∇ν δΓλ µλ .

(93)

Derivation of the anisotropic stress relation

We provide the intermediate steps leading to the slip relation Φ−Ψ = δfR /f¯R in
Newtonian gauge by extracting the traceless spatial part of the linearized field
equations and using the absence of intrinsic anisotropic stress for the canonical
dark scalar.

A.3

Elimination of δR in favor of δfR

Starting from δfR = fRR δR + fRT δTχ and assuming fRR ̸= 0, we derive δR =
(δfR − fRT δTχ )/fRR and insert it into δfT to obtain Eq. (53). We also discuss
the special case fRR = 0, in which δRis not eliminated in the same way and
the system must be reformulated.

A.4

Quasi-static reduction and reconstruction formulae

We detail the steps used to obtain the QS relations for the potentials and for δfR ,
including the dominant-gradient approximation δ(□fR ) ≃ −(k 2 /a2 )δfR , and we
28

## PDF page 29

provide a checklist of conditions under which the QS reduction is quantitatively
reliable for a given dataset.

A.5

Translated-constraint mapping details

We give the explicit mapping between the observational benchmark bound on
fR0 and the parameter combination 2αR0 + ξTχ0 in Eq. (88), including the
ΛCDM estimate for R0 in Eq. (89) and the dust approximation Tχ0 ≃ −ρχ0 .
We also discuss how the mapping changes if the dark sector departs from dust
or if Tχ includes additional dark species.

References
[1] N. Aghanim et al. [Planck Collaboration], “Planck 2018 results. VI. Cosmological parameters,” Astron. Astrophys. 641, A6 (2020). doi:10.1051/00046361/201833910
[2] D. Huterer and D. L. Shafer, “Dark energy two decades after: Observables, probes, consistency tests,” Rep. Prog. Phys. 81, no.1, 016901 (2018),
doi:10.1088/1361-6633/aa997e.
[3] E. V. Linder, “Cosmic growth history and expansion history,” Phys. Rev.
D 72, 043529 (2005), doi:10.1103/PhysRevD.72.043529.
[4] M. Ishak, “Testing General Relativity in Cosmology,” Living Rev. Relativ.
22, no.1, 1 (2019), doi:10.1007/s41114-018-0017-4.
[5] L. Amendola et al., “Cosmology and fundamental physics with the Euclid
satellite,” Living Rev. Relativ. 21, no.1, 2 (2018), doi:10.1007/s41114-0170010-3.
[6] T. Harko, F. S. N. Lobo, S. Nojiri and S. D. Odintsov, “f (R, T ) gravity,”
Phys. Rev. D 84, 024020 (2011). doi:10.1103/PhysRevD.84.024020
[7] G. A. Carvalho, F. Rocha, H. O. Oliveira and R. V. Lobato, “General
approach to the Lagrangian ambiguity in f (R, T ) gravity,” Eur. Phys. J.
C 81, 134 (2021), doi:10.1140/epjc/s10052-021-08920-4.
[8] K. Koyama, “Cosmological tests of modified gravity,” Rep. Prog. Phys. 79,
046902 (2016), doi:10.1088/0034-4885/79/4/046902.
[9] A. Joyce, B. Jain, J. Khoury and M. Trodden,
Cosmological Standard Model,” Phys. Rept. 568,
doi:10.1016/j.physrep.2014.12.002.

“Beyond the
1–98 (2015),

[10] A. De Felice and S. Tsujikawa, “f (R) theories,” Living Rev. Relativ. 13, 3
(2010). doi:10.12942/lrr-2010-3

29

## PDF page 30

[11] G. Gubitosi, F. Piazza and F. Vernizzi, “The Effective Field Theory of
Dark Energy,” JCAP 02, 032 (2013). doi:10.1088/1475-7516/2013/02/032
[12] E. Bellini and I. Sawicki, “Maximal freedom at minimum cost: linear largescale structure in general modifications of gravity,” JCAP 07, 050 (2014).
doi:10.1088/1475-7516/2014/07/050
[13] M. Ishak, “Testing General Relativity in Cosmology,” Living Rev. Relativ.
22, 1 (2019). doi:10.1007/s41114-018-0017-4
[14] U. Andrade, A. J. S. Capistrano, E. Di Valentino and R. C. Nunes, “Exploring modified gravity: constraints on the µ and Σ parametrization with
WMAP, ACT, and SPT,” Mon. Not. R. Astron. Soc. 529, 831–838 (2024).
doi:10.1093/mnras/stae402
[15] R. Kou, B. A. Benson, J. R. Bond, M. S. Madhavacheril, Y. Omori,
N. Raghunathan, C. S. Reichardt and M. White, “Constraining f (R)
gravity with cross-correlation of galaxies and cosmic microwave background lensing,” Astron. Astrophys. 686, A190 (2024). doi:10.1051/00046361/202348639
[16] L. Pogosian and A. Silvestri, “What can cosmology tell us about gravity?
Constraining Horndeski gravity with Σ and µ,” Phys. Rev. D 94, 104014
(2016), doi:10.1103/PhysRevD.94.104014.
[17] D. J. E. Marsh, “Axion cosmology,” Phys. Rept. 643, 1–79 (2016),
doi:10.1016/j.physrep.2016.06.005.
[18] L. Hui, J. P. Ostriker, S. Tremaine and E. Witten, “Ultralight scalars
as cosmological dark matter,” Phys. Rev. D 95, no.4, 043541 (2017),
doi:10.1103/PhysRevD.95.043541.
[19] G. Kane, K. Sinha and S. Watson, “Cosmological Moduli and the PostInflationary Universe: A Critical Review,” Int. J. Mod. Phys. D 24, no.08,
1530022 (2015), doi:10.1142/S0218271815300220.
[20] T. P. Sotiriou and V. Faraoni, “f (R) theories of gravity,” Rev. Mod. Phys.
82, 451–497 (2010), doi:10.1103/RevModPhys.82.451.
[21] A. D. Dolgov and M. Kawasaki, “Can modified gravity explain
accelerated cosmic expansion?,” Phys. Lett. B 573, 1–4 (2003),
doi:10.1016/j.physletb.2003.08.039.
[22] M. S. Turner, “Coherent scalar-field oscillations in an expanding universe,”
Phys. Rev. D 28, 1243 (1983), doi:10.1103/PhysRevD.28.1243.
[23] C.-P. Ma and E. Bertschinger, “Cosmological Perturbation Theory in the
Synchronous and Conformal Newtonian Gauges,” Astrophys. J. 455, 7–25
(1995), doi:10.1086/176550.

30

## PDF page 31

[24] V. Mukhanov, Physical Foundations of Cosmology, Cambridge University
Press, Cambridge (2005), doi:10.1017/CBO9780511790553.
[25] D. W. Hogg, “Distance measures in cosmology,” arXiv:astro-ph/9905116
(1999).
[26] D. J. Eisenstein et al., “Detection of the Baryon Acoustic Peak in the LargeScale Correlation Function of SDSS Luminous Red Galaxies,” Astrophys.
J. 633, 560–574 (2005). doi:10.1086/466512 [arXiv:astro-ph/0501171].
[27] W. J. Percival et al., “Measuring the Baryon Acoustic Oscillation scale
using the Sloan Digital Sky Survey and 2dF Galaxy Redshift Survey,”
Mon. Not. Roy. Astron. Soc. 381, 1053–1066 (2007). doi:10.1111/j.13652966.2007.12268.x [arXiv:0705.3323 [astro-ph]].
[28] L. Yıldız, D. Kaykı, and E. Güdekli, “Causal Israel–Stewart viscosity
and background scaling with a geometric dark-sector proxy in a modelindependent effective-fluid framework,” Int. J. Geom. Methods Mod. Phys.
(2026), doi:10.1142/S0219887826501409.
[29] L. Boubekeur, E. Giusarma, O. Mena and H. Ramı́rez, “Current status of modified gravity,” Phys. Rev. D 90, 103512 (2014),
doi:10.1103/PhysRevD.90.103512 [arXiv:1407.6837 [astro-ph.CO]].

31
