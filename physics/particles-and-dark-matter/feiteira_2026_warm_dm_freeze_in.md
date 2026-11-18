Source: https://arxiv.org/abs/2602.20242v1
PDF sha256: cba3d3fdff17f790733711b56868f1fb57aa3df0bf53a3c4d9f27ea6eb49cdc0
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of feiteira_2026_warm_dm_freeze_in.pdf

Transcription of `feiteira_2026_warm_dm_freeze_in.pdf` in this directory, 19 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-19 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Warm dark matter from freeze-in at stronger coupling

Duarte Feiteira 1 , Oleg Lebedev 1 , Vinı́cius Oliveira 2 ,3 ,4
1 Department of Physics and Helsinki Institute of Physics,

Gustaf Hällströmin katu 2a, FI-00014 Helsinki, Finland

arXiv:2602.20242v1 [hep-ph] 23 Feb 2026

2 Departamento de Fı́sica da Universidade de Aveiro and

Center for Research and Development in Mathematics and Applications (CIDMA),
Campus de Santiago, 3810-183 Aveiro, Portugal
3 Department of Physics, Lund University, SE-223 62 Lund, Sweden
4 Laboratório de Instrumentação e Fı́sica Experimental de Partı́culas (LIP),

Universidade do Minho, 4710-057 Braga, Portugal

Abstract
We study warm Higgs portal dark matter (DM) in the framework of freeze-in at stronger coupling.
This scenario assumes that the Standard Model thermal bath temperature has always been
relatively low, which suppresses dark matter production. As a result, a significant DM-Higgs
coupling is allowed, enabling warm dark matter detection via Higgs decay at colliders. We find
that the Lyman-α bound on the DM mass is particularly strong, excluding masses below 50100 keV, depending on further details. The shape of the DM momentum distribution is highly
non-thermal, with low momenta being effectively cut off, and not captured by the common
αβγ-parametrization.

1

## PDF page 2

Contents
1 Introduction
1.1 Higgs portal dark matter . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

2
3

2 Temperature evolution in the Early Universe

4

3 Freeze-in at very low temperatures
3.1 Production kinematics . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
3.2 Boltzmann equation and the collision integral . . . . . . . . . . . . . . . . . . . .
3.3 Models with a temperature peak at TR . . . . . . . . . . . . . . . . . . . . . . . .
3.3.1 On the αβγ parametrization . . . . . . . . . . . . . . . . . . . . . . . . . .
3.3.2 Dark matter abundance . . . . . . . . . . . . . . . . . . . . . . . . . . . .
3.4 Models with a flat temperature profile before reheating . . . . . . . . . . . . . . .

6
7
8
9
11
11
14

4 Conclusion

15

A Implementation of constraints in CLASS

16

1

Introduction

The dark matter (DM) puzzle is one of the outstanding problems of modern physics. The
traditional weakly-interacting-massive-particle (WIMP) paradigm finds itself under pressure from
the direct DM detection experiments. Thus, one is motivated to explore alternative scenarios
involving non-thermal dark matter. A prime example of the latter is the freeze-in mechanism
based on gradual accumulation of dark matter particles without thermalization [1, 2]. This can
be achieved either via small couplings [2] or via low temperatures [3], which suppress the reaction
rate.
The traditional high temperature freeze-in framework suffers from the background of gravitationally produced particles. Once produced, feebly interacting stable particles remain and
accumulate. Both classical and quantum gravitational effects during and immediately after inflation provide an efficient particle production mechanism, which often results in dark matter
over-abundance [4]. To give an example, gravity induces Planck-suppressed couplings between
the inflaton field ϕ and dark matter, e.g. [5, 6]
1
1
ϕ4 S 2 ,
ϕ2 χ̄χ , ...
2
MPl
MPl

(1)

Here S and χ are a scalar and a fermion, respectively. During the inflaton oscillation epoch, such
couplings lead to efficient production of these particles that generally overtakes the traditional
freeze-in mechanism. A similar effect is created by the inflationary de Sitter fluctuations [7, 8],
which eventually turn into particles, although this production channel is much weaker for fermions
[9].
The problem can be solved in scenarios with a low reheating temperature TR [4]. The
energy density of the produced particles gets diluted by the Universe expansion driven by a
non-relativistic inflaton. If the latter decays at late times, the dark relic abundance gets suppressed. The corresponding reheating temperature can even be below the dark matter mass
[3]. This possibility has recently attracted considerable attention [10]-[22] due to its interesting
2

## PDF page 3

observational prospects in collider or direct detection experiments. The DM production rate is
Boltzmann–suppressed allowing for a significant coupling to the SM fields and, thus, possible
detection of freeze-in dark matter [3].
In our current work, we focus on another regime of the low temperature freeze-in. Dark
matter itself can be very light, but the SM particles responsible for its production could have
masses above the bath temperature. We find that this possibility is viable and can account for
warm dark matter in the 100 keV mass range. Its coupling to the Higgs field can be significant
and lead to invisible Higgs decay at the LHC and future colliders.

1.1

Higgs portal dark matter

In what follows, we study light dark matter in the Higgs portal framework [23, 24] with a low
reheating temperature. Let us define the model.
The simplest dark matter model is a real scalar extension of the SM, where the DM stability
is enforced by a Z2 symmetry [25]. The interaction between the SM sector and dark matter S is
given by
Lhs =

λhs †
H HSS .
2

(2)

√
In the unitary gauge, the Higgs doublet is replaced by (h + v)/ 2, where v is the Higgs VEV
and h is the physical Higgs boson. Its interactions relevant for our purposes are
λhs v
hSS ,
2
mf ¯
LSM =
hf f .
v
Lhss =

(3)
(4)

The resulting DM production mechanism is of the freeze-in type as long as the SM bath temperature is sufficiently low, which can be probed via invisible Higgs decay [26, 27].
In this work, we are interested in very light dark matter with mass below 1 MeV. It can
efficiently be produced via the freeze-in mechanism even at low temperatures, T ≲ 100 MeV.
Annihilation of light SM particles mediated by the Higgs boson leads to the observed DM relic
abundance as long as the coupling λhs is not too small. The production rate is suppressed by
the light fermion Yukawa couplings as well as by the Higgs mass such that DM never thermalizes
and the model belongs to the freeze-in category.
The leading DM production channels are shown in Fig. 1, which dominate for T ≲ 100 MeV.
This upper limit is dictated by the proximity of the QCD phase transition, close to which
the perturbative approach breaks down. At lower temperatures, one may treat the hadrons
in the dilute gas approximation [28], with the pions and muons playing the main role. As
their abundance gets further Boltzmann-suppressed, the electron annihilation channel starts to
dominate at T ∼ 10 MeV.
The framework of freeze-in at stronger coupling assumes that the SM thermal bath temperature has never been high. This is consistent with the observational bounds which only require
the reheating temperature to be above 4 MeV [29]. In the next section, we discuss classes of
postinflationary scenarios, in which the maximal temperature of the SM sector does not significantly exceed the reheating temperature. Such models do not require non-standard cosmological
evolution and only relax the traditional assumption of how the SM sector is produced after
inflation.
3

## PDF page 4

πa

µ+

S
h

πa

S
h

µ−

S

S

Figure 1: Dark matter production via pion and muon annihilation.

2

Temperature evolution in the Early Universe

The exact mechanism of the Standard Model field production in the Early Universe remains
unknown. A simple possibility is that the observable sector was produced via decay of some
primordial field, for example, an inflaton [30] or a generic scalar [31]. The resulting SM energy
density and temperature depend on properties of this field. It is thus reasonable to parametrize
the uncertainty in terms of a few scaling parameters, which vary from model to model.
Consider a general case of the SM sector production from decay of a field χ, which does
not necessarily dominate the energy density of the Universe [31]. The SM quanta are normally
produced in the relativistic regime, so we can assume that the SM energy density ρ scales as
radiation. The energy density of the χ field is denoted by ρχ , whose scaling with the scale factor
is a−n , for some positive n. The Hubble rate H scales as a−m , with m > 0. The values of n and
m are, in general, unrelated and depend on further details.
Denoting the decay width of χ by Γχ , we arrive at the following system of equations:
ρ̇ + 4Hρ = Γχ ρχ ,
H = H0 /am ,
(5)

ρχ = ρ0χ /an .

The label 0 refers to the initial moment a0 = 1 which marks the end of inflation and ρ(1) = 0.
Here we assume that the SM sector does not contribute significantly to the energy balance of
the Universe bef ore reheating and that n, m are constant in the regime of interest.
d
The solution for ρ(a) is easily found using ρ̇ + 4Hρ = a14 dt
(a4 ρ) and dt = da/(aH). Then,
∫
da 4−n
4
0
a
,
(6)
a ρ = Γχ ρχ
aH
and the boundary condition ρ(1) = 0 requires [31]
[
]
Γχ ρ0χ
1
1
ρ(a) =
−
→
(4 − n + m)H0 an−m a4

Γχ ρ0χ
1
n−m
(4 − n + m)H0 a

(7)

at a ≫ 1, given that n − m < 4 for all cases of interest. The approximation becomes reasonable
already at a ∼ O(1). The scaling parameter n − m can have either sign or be zero, depending
on properties of χ. In particular, the SM energy density would increase over time if n − m < 0.
In the simplest case, the inflaton ϕ can directly decay into the SM states and the role of the
mother particle χ is played by the inflaton itself [30]. Since it dominates the energy balance,
m = n/2 and the SM energy density scales as a−m , with m being 3/2 or 2 for the non-relativistic
and relativistic inflaton, respectively. This scaling is maintained until reheating, after which the
usual result ρ ∝ a−4 applies.
4

## PDF page 5

The Standard Model fields start being produced immediately after inflation. Due to the large
couplings, they thermalize rather quickly and, soon after their production, the SM sector can be
assigned the temperature
)
(
n−m
30 1/4 1/4
TSM ≃
ρ
∝ a− 4 ,
(8)
2
g∗ π
where g∗ is the number of the SM degrees of freedom. In the simplest case, this temperature
decreases as a−n/8 until reheating, when the observable sector takes over the energy balance.
Therefore, if the SM fields are produced via ϕ → SM, the maximal temperature is far above the
reheating temperature.

T
1

TR

2
3

aR

a

Figure 2: Temperature of the Standard Model sector in the postinflationary epoch (on a logarithmic scale), with reheating at a ∼ aR . The different scenarios represent: (1) direct SM particle
production through inflaton decay, n − m > 0, (2) SM sector production via a cascade decay,
n − m = 0, (3) SM sector production via a longer cascade decay, n − m < 0.
In a more general situation, n − m differs from n/2 and can take on negative or zero values.
For example, the inflaton decay into the SM sector can be blocked by symmetry requirements,
while ϕ → χχ would be allowed. The observable sector is then produced via decay of the dark
state χ,
ϕ → χχ → SM ,
(9)
or a more complicated decay chain. This happens, for example, when the inflaton is charged under
an (approximate) lepton number symmetry such that it decays primarily into the right-handed
neutrinos via the coupling ϕ νR νR . If these are very weakly coupled and do not thermalize, they
can play the role of χ and produce the SM states through νR → ℓH. According to the argument
above, the energy density of νR scales exactly as the Hubble rate does, a−m , which implies
n−m=0,

(10)

and the SM temperature remains constant until reheating. As a result, the maximal temperature
is close to the reheating temperature, Tmax ≃ TR .
The value of n decreases as the decay chain gets longer, ϕ → χ1 χ1 → χ2 χ2 χ2 χ2 → ...,
while m is constant as long as the energy density is dominated by the mother particle. Thus,
n − m < 0 if the decay chain contains more than one intermediate particle. In this case, the
5

## PDF page 6

SM temperature increases until reheating, after which it decreases as a−1 . In the transition
region, the energy balance changes and the approximation of the inflaton domination becomes
inadequate. However, the transition to reheating can happen quite fast, depending on the decay
rates of χi , such that Tmax would remain close to TR .
The different possibilities for the SM temperature evolution are illustrated in Fig. 2. Option
(1) corresponds to the traditional inflaton decay into the SM states, while options (2) and (3)
reflect more general production mechanisms involving decay of intermediate particles. The blob
at a ∼ aR reflects the uncertainty in the transition region. Here, “reheating” is defined as the
period after which the energy density gets dominated by the SM thermal bath.
In cases (2) and (3), the temperature of the SM bath may have never exceeded the MeV scale.
Indeed, the lower bound on the reheating temperature is about 4 MeV. Such a low temperature
does not require non-standard cosmology, it only necessitates small couplings of the primordial
fields to the SM particles. This class of models is the focus of our present work.
We conclude that, since the SM particle production mechanism remains unknown, one ought
to account for distinct possibilities for the temperature evolution in the Early Universe. In
the context of freeze-in production of dark matter, they lead to vastly different scenarios. For
example, when Tmax ≃ TR , production of dark matter with mass above TR is dominated by
the temperature range T ≃ TR . This distinguishes the low TR freeze-in models from their more
traditional counterparts, leading to distinct phenomenology.

3

Freeze-in at very low temperatures

Since the observational bound on the reheating temperature is about 4 MeV [29], it is possible
that the temperature of the Standard Model thermal bath has never been high. In fact, it could
be lower than the dark matter mass or the mass of the SM mother particle responsible for DM
production. In these cases, the production rates are Boltzmann-suppressed. As a result, low-T
freeze-in is compatible with significant DM-SM couplings, without dark matter thermalization
[3].
In this work, we are interested in warm dark matter, which is intrinsically very light. Thus,
Boltzmann suppression appears due to the bath temperature being lower than the SM particle
masses responsible for DM production. In the Higgs portal models, such mother particles are
pions and muons in much of the parameter space of interest [26].
We focus on temperatures below 100 MeV such that the pion approximation of the SM hadron
gas becomes adequate. This is due to the pions being relatively dilute and the momentum
transfer in the collisions being small, enabling the EFT approach. At higher temperatures, close
to the QCD phase transition scale, the SM bath cannot be treated in the weakly coupled gas
approximation [28]. However, at yet higher temperatures, the heavy quark and lepton production
channels dominate, making the perturbative calculation reliable again [26].
In the above temperature range, the particles with the largest couplings to the Higgs are
pions and muons. They give comparable contributions to the DM production. At very low temperatures, T ∼ 10 MeV, both of them become irrelevant due to the strong Boltzmann suppression
and the production is dominated by the electron channel.
In the next subsection, we consider the kinematics of light dark matter production in a low
temperature thermal bath. This analysis is instructive for understanding main features of the
momentum distribution function.

6

## PDF page 7

3.1

Production kinematics

Consider the light dark matter production via pion annihilation in the regime ms ≪ T ≪ mπ .
The pions are mostly non-relativistic, so the DM energy is naturally close to mπ . Hence, the
bulk of the produced DM particles would have a momentum distribution centered around mπ .
On the other hand, the pions at the Boltzmann tail produce highly energetic as well as low
energy particles. At first glance, it appears that the DM momenta should be cutoff at |p| = mπ
from below, yet certain kinematic configurations lead to production of DM particles with energy
below the pion mass.
Let us neglect the DM mass (ms → 0) for now and consider the reaction
k1 + k2 → p̃ + p ,
where ki are the pion 4-momenta, while p, p̃ are the DM 4-momenta in the thermal bath rest
(“lab”) frame. Suppose we are interested in large |p| ≫ mπ . The initial state pion(s) must then
be highly relativistic. The reaction rate contains the usual Boltzmann factors for the initial state,
e−E1 /T e−E2 /T ,

(11)

where Ei are the temporal components of ki . For the reaction to be most efficient, the Boltzmann
suppression must be minimized,
E1 + E2 → min ,
subject to the constraint that E1 + E2 ≥ p0 . This requires minimizing p̃0 , while in the center-ofmass (CM) frame, the DM particle energy is bounded by mπ from below. Clearly, the necessary
particle energy reduction can only be achieved via a strong boost in the direction of motion of
the tilded particle.
Let us formalize this argument. The minimal energy DM configuration in the CM frame is
( )
(
)
mπ
mπ
′
′
p =
, p̃ =
,
(12)
mπ
−mπ
where the spacial component of the 4-momentum refers to the z-direction. The boost to the lab
frame is accomplished by
( ) ( )
(
)
( )
p0
cosh η sinh η
mπ
mπ
η
=e
=
,
(13)
, p=Λ
Λ=
sinh η cosh η
mπ
mπ
p0
where η is the rapidity. This fixes
(

η

e = p0 /mπ , p̃ = mπ /p0

mπ
−mπ

)
→0

(14)

at large p0 . Thus, we get E1 + E2 = p0 + m2π /p0 , which tends to p0 at large energies.1 This
configuration minimizes the Boltzmann suppression for a given p0 ≫ mπ ,
(
)
p0
m2π
−E1 /T −E2 /T
e
e
= exp − −
.
(15)
T
p0 T
It is this combination of the momenta that appears in the asymptotic limits of the Boltzmann
collision term. The corresponding kinematic configuration is shown in Fig. 3. The pion momenta
7

## PDF page 8

π
π

p0 /2
m2π /p0

p0

p0 /2

Figure 3: Production of one hard and one soft DM particle via a relativistic pion collision.
Corrections of order m2π /p0 to the pion momenta are neglected.
are found by boosting their CM values by Λ, which yields approximately 12 (p0 , p0 )T , up to m2π /p0
corrections.
This exercise also shows that DM with arbitrarily small momenta can be produced, although
the production rate is strongly Bolztmann-suppressed. By relabelling p0 ↔ m2π /p0 , one finds
that the corresponding Boltzmann factor is again given by (15) with p0 ≪ mπ .

3.2

Boltzmann equation and the collision integral

The critical quantity for our analysis is the dark matter momentum distribution function f (|p|, t).
It satisfies the Boltzmann equation [30]
∂f
∂f
1
− H|p|
=
C(p, t) ,
∂t
∂|p|
p0

(16)

where H is the Hubble rate and C(p, t) is the collision
particle production. The
)
( term describing
a0
d
left hand side of this equation is equivalent to dt f |p(0)| a(t) , t , so introducing the physical
a0
momentum p(t) ≡ a(t)
p(0) , one can integrate the equation with the result
∫
f (|p(t)|, t) =

dt′

C(p′ , t′ )
a(t)
with p′ = p(t)
.
′
p0
a(t′ )

Particle production is controlled by the collision integral,
∫ 3
d k1 d3 k2 d3 p̃
1
C(p) =
(2π)4 δ (4) (k1 + k2 − p̃ − p) |M|2 f (k1 )f (k2 ) ,
(2π)9
2E1 2E2 2Ep̃

(17)

(18)

with the Maxwell-Boltzmann statistics f (k1 )f (k2 ) = e−(E1 +E2 )/T . Here we follow the definition
of C(p) from [32]. For the leading Higgs portal reactions, the scattering matrix element is a
function of the CM energy, |M|2 = |M(s)|2 , s ≡ (k1 + k2 )2 . The integral above is Lorentzinvariant apart from the thermal distribution factor f (k1 )f (k2 ).
The collision term has been computed, for example, in [32]. To understand the shape of the
DM momentum distribution, let us consider the asymptotic regimes of large and small momenta.
Focussing on the pion contribution at T ≪ mπ , we can set |M(s)|2 ≃ |M(4m2π )|2 , since the
1
If the CM energy is not minimized by the DM configuration, the correction behaves as E 2 /p0 instead of
m2π /p0 , with E > mπ .

8

## PDF page 9

annihilation proceeds primarily via the s-wave.2 This applies also to the asymptotic regimes
considered in Sec. 3.1: even though p0 ≫ mπ or p0 ≪ mπ , the CM energy is still close to 2mπ .
Denoting p ≡ |p| and setting ms ≃ 0, we have
C(p) ≃ c

T e−p/T
p

∫ ∞
ds
4m2π

√
− s
1 − 4m2π /s e 4pT ,

(19)

where c is a constant proportional to |M(4m2π )|2 . The integral is easily evaluated using the
integration variable x = (s − 4m2π )/4pT and one finds the following asymptotic limits:
(
)
p
m2π
p1/2 T 5/2
exp − −
,
C(p) ∝
mπ
T
pT
(
)
p
m2π
2
2
p ≫ mπ /T : C(p) ∝ T exp − −
.
T
pT
p ≪ m2π /T :

(20)

These results are consistent with the considerations of Sec. 3.1. In particular, the form of the
exponential is dictated by the collision kinematics. Similar considerations apply to the muon
annihilation channel, up to inconsequential modifications.
The consequent momentum distribution function depends on the temperature evolution in
the Early Universe. In what follows, we consider two possibilities which motivate the concept
of freeze-in at stronger coupling: one, in which the temperature peaks at T ≃ TR , and another
with a flat temperature profile before reheating.

3.3

Models with a temperature peak at TR

Consider a class of models with n − m < 0 in Eq. 5, i.e. curve (3) in Fig. 2. In many aspects,
the physics of dark matter production in such scenarios is captured by the instant reheating
approximation. Indeed, the DM production before reheating is suppressed by both the Boltzmann
and dilution factors. Hence, one may neglect it and simply approximate the system by the
effective temperature T = 0 before reheating and T ∝ TR /a after reheating. The quality of this
approximation depends on the value of n − m as well as further details. Nevertheless, we will
adopt it in what follows, keeping in mind the associated uncertainty.
We note that our results can readily be extended to a more general situation with Tmax > TR
as long as Tmax is low enough to ensure the Boltzmann suppression of DM production [31].
The main features of the distribution function can be understood analytically. Introducing
the comoving momentum
p
q≡ ,
(21)
T
we have
∫ TR
1
dT C(q, T )
f (q) =
,
(22)
q T T2
H
taking the number of the SM degrees of freedom approximately constant. The main difference
from the standard freeze-in calculations, which assume a very high reheating temperature, is that
the upper limit of integration is rather low instead of ∞. This affects the functional dependence
2
Relaxing this assumption does not affect the collision integral in any significant way since its behavior is
controlled primarily by the exponential factor. The s-dependence of the amplitude is given in [33], although it
cannot be extrapolated to energies far above the pion mass.

9

## PDF page 10

√
of f (q). Typically it takes the form e−q / q in high T models, whereas in our case it becomes
quite different.
Focussing again on the pion contribution, the integral can easily be computed in the asymptotic regions:
(
)
m2π
√
2
2
q ≪ mπ /TR : f (q) ∝ q exp − 2 ,
qTR
1
(23)
q ≫ m2π /TR2 : f (q) ∝ √ exp (−q) .
q
The large momentum behavior remains the same as in the high T models, wheres at low momenta,
it changes completely. The IR modes get effectively cut-off. The reason is clear: at the time
of production, the physical momenta are close to mπ , while at later times they red-shift by the
factor T /TR . The particles simply do not have enough time to red-shift to lower values, resulting
in strong suppression of the IR modes. The typical comoving momentum is q ∼ mπ /TR and the
lower values like q ∼ 1 would be exponentially suppressed.3 In high-T models, the red-shifting
is effective over a much longer period and the above feature is thus absent.
Our numerical integration result is presented in Fig. 4. It is clearly seen that the low momenta are exponentially suppressed, while the typical value is q ∼ mπ /TR . These features make
the distribution highly non-thermal and shock-wave-like, distinguishing it from f (q) the high-T
freeze-in models [34]-[37].
1.

f(q)

0.8
0.6
0.4
0.2
0

2

mπ
TR

4

6

8

q

Figure 4: Comoving momentum distribution function of DM produced via pion annihilation,
with TR = 50 MeV and assuming instant-like reheating. For convenience, f (q) is normalized to
1 at the maximum.
In the muon annihilation channel, we find a similar distribution function due to the proximity
of the pion and muon masses. The electron counterpart is quite different, yet the electron
contribution is suppressed and does not play any significant role.
3
The modes with q ∼ mπ /TR ≪ (mπ /TR )2 appear to be suppressed according to the asymptotic expression,
however, the value of f (q) depends on the overall normalization, e.g. the Higgs portal coupling, and thus can be
adjusted at will.

10

## PDF page 11

3.3.1

On the αβγ parametrization

It is common to parametrize the momentum distribution function as [38]
∣
∣
f (q)∣
∝ q α exp(β q γ ) ,
high TR

(24)

with constant α, β, γ. Although the high TR freeze-in models are accommodated by this Ansatz
very well, low TR scenarios do not follow the same pattern. Indeed, the asymptotic form (23)
shows that the coefficients α, β, γ become momentum-dependent,
α, β, γ → α(q), β(q), γ(q) .
For example, γ flips from 1 at large momenta to -1 at low momenta. Hence, the functional form
of f (q) is quite different and the α, β, γ parametrization is not particularly useful. Nor does the
above distribution fit the quasi-thermal form [37].
We find that this feature is generic in the low TR framework and not restricted to the Higgs
portal models. For example, DM can be produced via decay of a mother particle at low T .
In this case, the kinematic considerations of Sec. 3.1 apply with some modifications, while the
main features remain. In particular, the low momentum states are produced by a highly boosted
mother particle, which leads to strong Boltzmann-suppression. As a result, f (q) at small q
exhibits a similar behavior to that observed in our case. Furthermore, in reality, dark matter can
be produced by multiple mother particles, which can lead to an even more complicated non-αβγ
shape of f (q), depending on their relative contributions.
We emphasize that these conclusions are reached in the framework of Standard Cosmology
after reheating. In particular, the expansion history has not been modified. We only assume
that the reheating temperature is low due to small couplings and that the SM states have been
produced via decay of a spectator field.
Strong suppression of the low-momentum modes leads to strict bounds on warm dark matter
from structure formation [39], which we quantify in the next subsection.
3.3.2

Dark matter abundance

The dark matter abundance is computed via the Boltzmann equation for the number density n,
ṅ + 3Hn = 2 Γ(SM → DM) − 2 Γ(DM → SM) ,

(25)

where Γ denotes the reaction rate per unit volume and the factor of 2 appears due to 2 DM quanta
being involved in each reaction. In the freeze-in framework, the produced DM density is far below
its thermal equilibrium value such that DM annihilation can be neglected, Γ(DM → SM) ≃ 0.
For the Maxwell-Boltzmann distribution function, the production reaction rate takes the form
2
Γ(f¯f → SS) = ⟨σ(f¯f → SS)vr ⟩ (neq
f ) ,

(26)

where ⟨...⟩ stands for the thermal average, σ is the reaction cross section which includes the
symmetry factors for the initial and final states, vr is the relative velocity of the initial state
particles and neq
f is the thermal equilibrium density of f .
At low temperatures, light dark matter can be produced via annihilation of
• muons
11

## PDF page 12

• pions
• electrons
• photons
Numerically, the dominant contributions are provided by the muons and the pions. Although
the muon annihilation amplitude suffers from mild velocity suppression, the muon density is
higher, which makes the reaction rate comparable to or higher than that for the pions. The
electron contribution is strongly suppressed by the electron mass and even though the electron
density is high, the corresponding reaction rate is small. It starts to dominate only at very low
temperatures, T ∼ 10 MeV, when the heavier particles become very dilute. On the other hand,
we find that the photon channel is always negligible [26].
The production cross section calculation is based on the following scattering amplitudes.
The pion annihilation occurs primarily at low momentum transfer, i.e. s ≃ 4m2π . This regime
is captured by the chiral perturbation theory and the low energy theorems [40, 41, 42], and the
amplitude is extracted from |Mh→πi πi | = |Mπi πi →h | at s ≃ 4m2π , using the results of [33]. For
a single pion type, this yields
4 λ2hs m4π
|Mπi πi →SS |2 ≃
,
(27)
m4h
in the standard QFT convention, for ms ∼ 0. When this matrix element enters the thermal rate
calculation, it is to be multiplied by the phase space symmetry and multiplicity factors. Due to
the identical pions in the initial state and identical scalars in the final state, the symmetry factor
is 1/2 × 1/2, while the pion multiplicity factor is 3.
The standard QFT muon annihilation amplitude squared, averaged over the initial state
spins, is given by
∣
∣
λ2 m2 (s − 4m2µ )
∣Mµ+ µ− →SS ∣2 = hs µ
,
(28)
2m4h
for ms ∼ 0. In the thermal reaction rate, this matrix element gets multiplied by the spin
multiplicity factor 22 as well as the phase space symmetry factor 1/2 due to identical scalars in
the final state.
The Boltzmann equation is solved numerically and the DM abundance Y is computed via
n
Y =
,
(29)
sSM
where sSM is the SM entropy density,
2π 2
sSM =
gs T 3 , H =
45

√

g∗ π 2 T 2
.
90 MPl

(30)

Here gs is the SM d.o.f. number contributing to the entropy and g∗ is that contributing to the
energy density. Due to entropy conservation, Y remains constant after DM production completes,
which in practice means shortly after T ∼ TR . The observed value is
Y∞ = 4.4 × 10−10

GeV
.
ms

(31)

In the regime ms ≪ mπ,µ , the reaction rates and the resulting n are independent of the DM
mass. Since Γ, n ∝ λ2hs , we therefore find the scaling
1
λhs ∝ √
.
ms
12

(32)

## PDF page 13

10 2

20

LHC
HL-LHC

hs

24
Lyman-

10 3

0.03

30
60
80

FCC

40
0.1

0.3

ms [MeV]

1

Figure 5: Parameter space of the Higgs portal DM model at low masses. Along the colored
lines, the observed DM abundance is reproduced, for a given TR (in MeV). The shaded areas
are excluded by the LHC and Lyman-α constraints, while the dashed lines show the prospects
of DM detection via invisible Higgs decay.
Fig. 5 shows the result of our parameter space analysis. We are focussing the low dark
matter masses below 1 MeV since for larger masses our scalar DM is cold [26]. We also take
the maximal reheating temperature to be 80 MeV in order to stay safely below the QCD phase
transition temperature, close to which our perturbative dilute gas analysis becomes inadequate.
The observed DM abundance is reproduced along the lines marked by TR (in MeV).4
The pink shaded area is excluded by the Lyman-α constraints on warm DM, which we have
analyzed using the CLASS tool [43, 44] as described in Appendix A. These become stronger for
smaller TR . Indeed, the DM momentum at the production point is given by the pion and muon
masses, and a lower TR implies less time for “red-shifting” the momentum to small values at the
structure formation epoch. This makes dark matter “warmer”. We observe that values of ms
below 70 - 100 keV are excluded. Such a constraint is stronger than that in high-T models due
to the larger DM comoving momentum, q ∼ mπ,µ /TR , and the IR suppression of the momentum
distribution.
The grey area is excluded by the LHC search for invisible Higgs decay, h → SS. The
corresponding decay width is given by
√
λ2hs v 2
4m2
Γ(h → SS) =
1 − 2s .
(33)
32πmh
mh
We use the bound on the invisible decay branching ratio BRinv ≲ 10% [45], which excludes the
Higgs portal couplings above 10−2 . The dashed lines show the prospects for observing this mode
4

These agree within a factor of 1.4 to 1.9 with our previous results [26]. The discrepancy is due to the different
treatment of the hadronic states: numerical integration over various hadronic states based on a plot in [33] is now
replaced with the chiral perturbation limit which only involves the pions at low T . We note that our treatment of
the SM plasma as an ideal gas also entails some uncertainty, especially at temperatures close to the QCD phase
transition [28].

13

## PDF page 14

at the HL-LHC and FCC. We take the HL-LHC benchmark goal to be BRinv = 3% [46], while
that of the FCC to be BRinv = 0.3% [47].
We thus conclude that warm dark matter in the Higgs portal framework can be probed via
invisible Higgs decay at current and future colliders.

3.4

Models with a flat temperature profile before reheating

Consider now a class of models exhibiting a flat temperature profile before reheating. This
corresponds to n − m = 0 in Eq. 5 and curve (2) in Fig. 2. Such a possibility is realized,
for example, when the inflaton decays into the right-handed neutrinos νR , which subsequently
produce the SM fields: ϕ → νR νR → SM.
1.

f(q)

0.8
0.6
0.4
0.2
0

mπ
TR

2

4

6

8

q

Figure 6: Comoving momentum distribution function of DM produced via pion annihilation,
with TR = 50 MeV and assuming a constant T profile before reheating. For convenience, f (q) is
normalized to 1 at the maximum.
Compared to the previous case, the momentum distribution function receives an extra piece
∆f which is due to the particles produced before the reheating point at a = aR . The full
distribution function is given by
∣
∣
f (q) = f (q)∣
+ ∆f (q) ,
(34)
T <TR

∣
∣
where f (q)∣

T <TR

has been computed in the previous subsection and ∆f is
1
∆f (p, aR ) =
p aR

∫ aR
0

da′
aR
C(p′ , a′ ) with p′ = p ′ .
′
H(a )
a

(35)

In this integral, the temperature is taken to be constant, T = TR and the comoving momentum
is given by q = p/TR at a = aR . After that, the comoving momentum q = p(T )/T remains
constant. Before reheating, we may take H ∝ a−2 assuming radiation-like scaling of the energy
density of the Universe, although this is not a critical assumption and analogous results can
readily be obtained for different scaling laws.
The asymptotic behavior of f (q) can be understood analytically. Consider the low momentum
regime p ≪ TR . The collision term can be approximated by C(p′ ) ∝ p′α exp(−p′ /TR −m2π /(p′ TR ))
14

## PDF page 15

with some positive α. The integral is dominated by the vicinity of the point a′∗ = aR p/mπ which
maximizes the exponential. Around this point, the exponential has a Gaussian form with a small
width ∝ p such that the integrand can be approximated by a “box” function. This yields ∆f ∝ p2 ,
which also gives the asymptotic behavior
∣ of the full function f . In the large p limit, the above
∣
integral is suppressed compared to f (q)∣
and the asymptotic behavior of f (q) remains the
T <TR

same as in the previous section.
These results are dictated by simple physical considerations. The DM quanta with arbitrarily
small momenta p are generated via “red-shifting” the initially energetic particles (E ≃ mπ ). For
a given p, this fixes the production scale factor a′∗ = aR p/mπ ≪ aR . On the other hand,
production of highly energetic particles is dominated by late times. Indeed, the temperature
remains constant between a ∼ 0 and a = aR , while particles produced at earlier times are
subject to the “red-shifting”. Hence, the constant T period does not affect the large momentum
behavior of the distribution function.
We thus find the following asymptotic scaling of f (q):
f (q) ∝ q 2 ,
1
q ≫ m2π /TR2 : f (q) ∝ √ exp (−q) .
q
q≪1 :

(36)

Our numerical result is presented in Fig. 6. Compared to our previous findings, we observe that
the peak of the distribution moves to a lower momentum and that the IR modes do not get
cut off. Nevertheless, the above asymptotic form shows that the αβγ-parametrization is still
not applicable, strictly speaking.5 This is natural since the low and high momentum behavior
is determined by the pre-reheating and post-reheating epochs, respectively. We also find that
the peak of the distribution is correlated with mπ /TR and, in practice, located not far from
q ∼ mπ /TR . An analogous statement applies to f (q) generated in the muon annihilation channel.
The DM relic abundance now contains two contributions: one from the SM radiation domination epoch (a > aR ), as before, and the other from the pre-reheating era (a < aR ). The new
contribution is
∣
2 Γ(SM → SS) ∣∣
∆Y =
,
(37)
∣
5 H sSM
T =TR
2
where Γ = ⟨σvr ⟩ neq
SM is the DM production rate per unit volume. This results in a smaller
coupling being sufficient for producing the right relic density.
Our parameter space analysis is presented in Fig. 7. The relic abundance lines move somewhat
to the lower couplings, with the shift getting smaller at higher temperatures due to ∆Y /Y0 ∝
1/TR . The Lyman-α constraints relax compared to the previous case, with the lower bound on
the DM mass being in the range 50 − 100 keV. Although the DM momentum distribution shifts
to the lower values, most DM particles are still energetic, with typical comoving momenta not
far from mπ /TR .6 As a result, the structure formation bound remains strong.

4

Conclusion

We have studied light Higgs portal dark matter in the context of freeze-in at stronger coupling.
In particular, we have focused on the warm dark matter window and the reheating temperature
5
We find that the αβγ-parametrization can reproduce well the overall shape of f (q), while failing in the
asymptotic regions. This difference may be insignificant for applications.
6
The electron annihilation channel becomes important only at TR ≲ 15 MeV.

15

## PDF page 16

LHC

10 2

20

hs

Lyman-

HL-LHC

24
10 3

FCC

30
60
80

0.03

40
0.1

0.3

ms [MeV]

1

Figure 7: Parameter space of the Higgs portal DM model at low masses, assuming a constant
temperature profile before reheating. Along the colored lines, the observed DM abundance is
reproduced, for a given TR (in MeV). The shaded areas are excluded by the LHC and Lyman-α
constraints, while the dashed lines show the prospects of DM detection via invisible Higgs decay.
below 100 MeV. The main production channel is the muon and pion annihilation mediated by
the Higgs. The reaction rate is suppressed by the Boltzmann factor at T < mµ,π , the small
Yukawa couplings as well as by the Higgs propagator. This makes the production mechanism to
be of the freeze-in type, even though the Higgs-DM coupling can be significant.
We find that the observed relic density can be produced in the warm dark matter regime for
the Higgs portal coupling λhs in the range 10−4 − 10−2 , which leads to the invisible Higgs decay
within the reach of the LHC and FCC. The Lyman-α bound sets a strong lower bound on the
warm DM mass, not far from 100 keV. This is due to the fact that the DM momentum distribution
function has a highly non-thermal shape, with most particles having momenta substantially above
the SM temperature. Generally, we find that the momentum distribution in the low T freeze-in
framework is not captured by the usual αβγ parametrization.
The model is best probed by the invisible Higgs decay into dark matter, with the decay
branching ratio at the percent level. This mode can be observed at the LHC and future colliders
such as the FCC.
Acknowledgements. We are grateful to Deanna Hooper for help with the CLASS package.

A

Implementation of constraints in CLASS

To obtain the Lyman-α constraints using CLASS [43], two main inputs are needed: the distribution function f (p̄) in terms of a dimensionless momentum p̄ and a dimensionless normalization
p
scale Tncdm . The momentum p̄ is defined by p̄ = Tncdm
T0 , where p is the physical momentum
today and T0 is the average CMB temperature today. The most convenient normalization scale
π
for freeze-in at stronger coupling is Tncdm = m
TR . The distribution function can be computed by
solving numerically the Boltzmann equation or by using more sophisticated tools like DRAKE
16

## PDF page 17

[48].
With the above input, CLASS computes the power spectrum corresponding to a given dark
matter model. Then, the Lyman-α constraints can be imposed using the area criterion, detailed
in [35] and [34]. To apply this criterion, one first needs to obtain the one-dimensional power
spectrum by integrating the three-dimensional one over the momentum, from k to klim → ∞.
Then, one quantifies the difference between our non-thermal DM model and
cold DM case
∫ kthe
max
through the ratio r(k) of the two spectra. The area is then defined as AX = kmin dk r(k), where
kmin = 0.5 h/Mpc and kmax = 20 h/Mpc [35]. In the CDM case, ACDM = kmax − kmin . At
−AX
the next step, one obtains the area estimator δAX = ACDM
ACDM . This estimator must be first
computed for a benchmark WDM model with the Fermi-Dirac distribution function and a DM
mass of 5.3 keV. Then, the same estimator is computed for our DM model. In order for our
model to be consistent with the Lyman-α observations, the area estimator must be below that
of the benchmark model. The choice of klim can have an impact on the area estimator as shown
in [32]. However, the dependence on klim is the same for any relevant model. Thus, as long as
we choose the same value of klim for all the calculations, we obtain consistent results.
Following this procedure, we find the benchmark model value
δAlim
X = 0.205,

mWDM = 5.3 keV,

klim = 100 h/Mpc .

(38)

To identify the region allowed by the Lyman-α observations, we apply the following procedure.
1. Choose TR and compute f (p̄). Tncdm and f (p̄) are input in CLASS.
2. Choose mDM and input it in CLASS.
3. Compute the area estimator and check if it is bellow the bound in Eq. (38).
4. Vary mDM until the area estimator bound is saturated. Lower values of mDM are excluded.
5. Repeat for a different TR . A pair (mDM , TR ) corresponds to a point in the parameter
space (mDM , λhs ) through the relic density condition. It lies on the boundary of the
allowed region.

References
[1] S. Dodelson and L. M. Widrow, Phys. Rev. Lett. 72, 17-20 (1994).
[2] L. J. Hall, K. Jedamzik, J. March-Russell and S. M. West, JHEP 03, 080 (2010).
[3] C. Cosme, F. Costa and O. Lebedev, Phys. Rev. D 109, no.7, 075038 (2024).
[4] O. Lebedev, JCAP 02, 032 (2023).
[5] O. Lebedev and J. H. Yoon, JCAP 07, no.07, 001 (2022).
[6] F. Koutroulis, O. Lebedev and S. Pokorski, JHEP 04, 027 (2024).
[7] D. Feiteira and O. Lebedev, JCAP 07, 003 (2025).
[8] F. Costa and J. Kim, [arXiv:2602.10215 [hep-ph]].
17

## PDF page 18

[9] D. Feiteira, F. Koutroulis, O. Lebedev and S. Pokorski, [arXiv:2509.01673 [hep-ph]], to
appear in JCAP.
[10] N. Bernal, S. Mukherjee and J. Unwin, [arXiv:2602.10112 [hep-ph]].
[11] N. Bernal, S. Mukherjee and J. Unwin, JCAP 02, 010 (2026).
[12] N. Bernal, G. Cottin, B. Dı́az Sáez and M. López, JHEP 01, 081 (2026).
[13] N. Bernal, E. Cervantes, K. Deka and A. Hryczuk, JHEP 09, 083 (2025).
[14] N. Koivunen, O. Lebedev and M. Raidal, Eur. Phys. J. C 84, no.11, 1234 (2024).
[15] G. Arcadi, D. Cabo-Almeida and O. Lebedev, Phys. Lett. B 861, 139268 (2025).
[16] S. Khan, J. Kim and H. M. Lee, JCAP 06, 040 (2025).
[17] S. Khan, J. Kim and H. M. Lee, [arXiv:2509.17129 [hep-ph]].
[18] H. M. Lee, M. Park and V. Sanz, JHEP 05, 126 (2025).
[19] A. Roy and R. Sahu, [arXiv:2508.14726 [hep-ph]].
[20] K. K. Boddy, K. Freese, G. Montefalcone and B. Shams Es Haghi, Phys. Rev. D 111, no.6,
6 (2025).
[21] P. Arias, B. Dı́az Sáez, L. Duarte, J. Jones-Pérez, W. Rodriguez and D. Z. Herrera, JHEP
01, 135 (2026).
[22] S. E. Henrich, Y. Mambrini and K. A. Olive, Phys. Rev. D 111, no.8, 083501 (2025).
[23] B. Patt and F. Wilczek, [arXiv:hep-ph/0605188 [hep-ph]].
[24] O. Lebedev, Prog. Part. Nucl. Phys. 120, 103881 (2021).
[25] V. Silveira and A. Zee, Phys. Lett. B 161, 136-140 (1985).
[26] O. Lebedev, A. P. Morais, V. Oliveira and R. Pasechnik, JHEP 04, 136 (2025).
[27] G. Arcadi, F. Costa, A. Goudelis and O. Lebedev, JHEP 07, 044 (2024).
[28] A. Bazavov et al. [HotQCD], Phys. Rev. D 86, 034509 (2012).
[29] S. Hannestad, Phys. Rev. D 70, 043506 (2004).
[30] E. W. Kolb and M. S. Turner, Front. Phys. 69, 1-547 (1990).
[31] C. Cosme, F. Costa and O. Lebedev, JCAP 06, 031 (2024).
[32] F. D’Eramo and A. Lenoci, JCAP 10, 045 (2021).
[33] M. W. Winkler, Phys. Rev. D 99, no.1, 015018 (2019).
[34] G. Ballesteros, M. A. G. Garcia and M. Pierre, JCAP 03, 101 (2021).
[35] Q. Decant, J. Heisig, D. C. Hooper and L. Lopez-Honorez, JCAP 03, 041 (2022).
18

## PDF page 19

[36] F. D’Eramo, A. Lenoci and T. Sassi, [arXiv:2511.07511 [hep-ph]].
[37] F. D’Eramo, A. Lenoci and A. Dekker, Phys. Rev. D 112, no.11, 11 (2025).
[38] K. J. Bae, A. Kamada, S. P. Liew and K. Yanagi, JCAP 01, 054 (2018).
[39] M. Viel, J. Lesgourgues, M. G. Haehnelt, S. Matarrese and A. Riotto, Phys. Rev. D 71,
063534 (2005).
[40] A. I. Vainshtein, V. I. Zakharov and M. A. Shifman, Sov. Phys. Usp. 23, 429-449 (1980).
[41] M. B. Voloshin, Sov. J. Nucl. Phys. 45, 122 (1987).
[42] S. Dawson and H. E. Haber, Int. J. Mod. Phys. A 7, 107-120 (1992).
[43] D. Blas, J. Lesgourgues and T. Tram, JCAP 07, 034 (2011).
[44] J. Lesgourgues and T. Tram, JCAP 09, 032 (2011).
[45] G. Aad et al. [ATLAS], Phys. Lett. B 842, 137963 (2023).
[46] P. A. Rivadeneira Bracho, “Search for invisible decays of the Higgs boson produced via
vector boson fusion at the ATLAS detector with 139 fb−1 of integrated luminosity,” PhD
thesis, University of Hamburg, 2022.
[47] P. Giacomelli, talk at ICHEP 2018, https://indico.cern.ch/event/686555/contributions/2971566/
attachments/1682031/2703684/Higgs-measurements-FCC-ICHEP-2018_169.pdf
[48] T. Binder, T. Bringmann, M. Gustafsson and A. Hryczuk, Eur. Phys. J. C 81, 577 (2021).

19
