Source: https://arxiv.org/abs/2602.11405v1
PDF sha256: 54910ddf17efdd419622fffa8c4aae7131833ed441297bac518b952166740129
License: http://creativecommons.org/publicdomain/zero/1.0/
Language: eng
Fidelity: machine-gated

# Transcription of gninenko_2026_dark_axion_portal.pdf

Transcription of `gninenko_2026_dark_axion_portal.pdf` in this directory, 13 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-13 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Constraints on dark axion portal: missing energy and fermion EDMs
Sergei N. Gninenko ,1, 2, 3 N. V. Krasnikov ,1, 2 Valery E. Lyubovitskij ,4, 3 Sergey Kuleshov
Alexey S. Zhevlakov ,2, 6 I. V. Voronchikhin ,1, 7 and D. V. Kirpichnikov 1, ∗

,3, 5

1
Institute for Nuclear Research, 117312 Moscow, Russia
Bogoliubov Laboratory of Theoretical Physics, JINR, 141980 Dubna, Russia
3
Millennium Institute for Subatomic Physics at the High-Energy Frontier (SAPHIR) of ANID,
Fernández Concha 700, Santiago, Chile
4
Institut für Theoretische Physik, Universität Tübingen,
Kepler Center for Astro and Particle Physics,
Auf der Morgenstelle 14, D-72076 Tübingen, Germany
5
Center for Theoretical and Experimental Particle Physics, Facultad de Ciencias Exactas,
Universidad Andres Bello, Fernandez Concha 700, Santiago, Chile
6
Matrosov Institute for System Dynamics and Control Theory SB RAS,
Lermontov str., 134, 664033, Irkutsk, Russia
7
Tomsk Polytechnic University, 634050 Tomsk, Russia

arXiv:2602.11405v1 [hep-ph] 11 Feb 2026

2

We study a model in which a new interactions between the Standard Model (SM) photon and
both the dark photon (γD ) and an ALP (a) are described by the dark axion portal operator. The
implications of this dark axion portal scenario for electron fixed-target experiments are presented. In
particular, we investigate the missing energy signatures associated with production of dark photons
and their subsequent invisible decays into stable dark sector fermions, γD → χχ̄. We discuss the discovery potential for such a scenario and derive projected sensitivity curves for the NA64e and LDMX
experiments. Furthermore, novel constraints of the NA64e for 9.37 × 1011 electrons on target are
derived by considering two production mechanisms for invisible states: (i) the bremsstrahlung-like
emission of an aγD pair, eN → eN γ ∗ (→ aγD ), and (ii) the exclusive vector meson photoproduction,
γ ∗ N → N V , followed by the invisible decays of vector mesons, V → aγD . Additionally, the constraints on the parameter space of CP -violating, fermion-specific ALP and dark photon couplings
are established. These constraints are derived from current experimental bounds on the electric
dipole moments (EDMs) of SM fermions, incorporating loop-induced contributions to the EDMs of
the electron, muon, and neutron.

I.

INTRODUCTION

Axion-like particles (ALP or a) represent a wellmotivated class of pseudo-scalar bosons that emerge naturally in numerous extensions of the Standard Model
(SM). Originally posited as a dynamical solution to the
strong CP problem, their theoretical foundation has been
expanded significantly, as reviewed in [1, 2]. Beyond this
primary role, ALPs provide a viable framework for addressing phenomenological puzzle, serving as viable candidates for the cosmological dark matter (DM) relic density [3–5].
The phenomenological landscape of ALPs extends to
more exotic scenarios, such as those featuring lepton flavor violation. Such models, where ALPs mediate transitions between different lepton generations, have been the
subject of detailed theoretical and experimental investigation [6–9]. Recent reviews and a multitude of studies,
spanning beam-dump experiments, fixed-target facilities,
colliders, RF cavities, and astrophysical probes, explore
various signatures and constraints on these particles [10–
36].
Recent work has introduced a novel interaction framework known as the dark axion portal [37, 38]. This effec-

∗ e-mail: dmbrick@gmail.com

tive operator facilitates the production of dark photons
in the early Universe and, for sufficiently low-mass dark
photon states, provides a viable mechanism for generating the observed cosmological dark matter relic density.
The portal is characterized by vertices coupling the axion
(or a generic ALP) simultaneously to the SM photon and
the dark photon, a-γ-γD .
Building upon the theoretical framework proposed in
Refs. [39–41], this work investigates the phenomenology
of the dark axion portal in a scenario where the associated dark photon decays predominantly into dark sector
(DS) states. In this model, the dark photon is identified
as the gauge boson of a hidden UD (1) symmetry, thereby
acting as the primary mediator between the Standard
Model and DS particles through the portal interaction.
We demonstrate that this scenario yields a rich phenomenology accessible through missing energy signatures
at electron beam fixed-target experiments. Specifically,
we conduct an analysis of the discovery potential for such
signals at the current experiment NA64e [28–32, 42, 43]
and the proposed LDMX facility [44–50].
We also develop the ideas presented in Refs. [51, 52]
where the implication of light sub–GeV bosons for electric dipole moments (EDM) of fermions and CP –odd
dark axion portal coupling was discussed in detail. In
particular, we argue that the EDM of fermions can be
induced by: (i) CP –odd Yukawa–like couplings of ALP,
(ii) CP –even interaction of SM fermions and dark pho-

## PDF page 2

2
ton and (iii) CP –even dark axion portal coupling. As a
result, one can obtain bounds on the corresponding couplings.
This work is structured as follows. Sec. II details the
theoretical framework and benchmark scenarios for the
dark axion portal. Sec. III outlines the missing energy
signatures relevant for dark matter production in fixedtarget experiments. In Sec. IV we outline benchmark experiments. In Sec. V, we derive constraints on the portal’s effective couplings using data from electron-beam
fixed-target facilities. Sec. VI explores the generation
of electric dipole moments for Standard Model fermions
within dark axion portal framework incorporating additional CP -violating couplings. Finally, Section VII provides a summary and conclusions.
II.

THE DESCRIPTION OF THE BENCHMARK
SCENARIOS

The coupling between dark and electromagnetic photons can be associated with ALPs through specific interaction [37, 38]. The effective Lagrangian for such nonrenormalizable dark axion portal takes the form
gaγγD
aFµν F̃ ′µν ,
(1)
Ldark axion portal ⊃
2
that is the interaction between ALP and both SM and
dark photon, where F µν and F̃ ′µν are the stress tensors
of the visible and dark photons, respectively, gaγγD is the
coupling constant.
This work explores a benchmark extension of the dark
axion portal framework by incorporating a minimal dark
sector candidate. Within this model, the dark photon,
emerging from a hidden UD (1) gauge symmetry, acts as
the mediator between the Standard Model sector and a
dark fermionic sector. The relevant Lagrangian is given
by:
LDS ⊃ χ̄ (iγ µ Dµ − mχ ) χ,

(2)

where the DS field χ is a Dirac fermion representing a
dark sector particle with mass mχ . Its covariant derivative is Dµ = ∂µ + igD A′µ , introducing the gauge coupling
gD associated with the hidden UD (1) charge. A key phenomenological assumption of this setup is that the dark
photon decays predominantly into a pair of these dark
fermions, A′ → χχ̄, resulting in an invisible final state
thus making it interesting for searching, in particular,
in fixed target experiments, such as NA64e and LDMX.
The phenomenological consequences of these signatures
are analyzed in Sec. II, III, IV, and V.
One can assume the existence of the the Yukawa–like
couplings of the ALP with SM fermions [41, 52–55],
∑
L̸C P ⊃
gfa af¯f
(3)
f =e,µ,n

violating the CP symmetry, thus they can induce the
electric dipole moment (EDM) of SM fermions. It is

worth to estimate the bounds on the combination of couplings from the EDM of fermions in the framework of
their additional model independent benchmark interactions with dark photon
∑
L⊃
eϵf A′µ f¯γ µ f,
(4)
f =e,µ,n

where protophobic coouplings eϵf of massive hidden vector can be relevant to the exotic fifth force scenarios addressing in Ref. [56].
The study of EDM fermion bounds, incorporating the
Lagrangians in Eqs. (1), (3), and (4), is of particular
interest in the present paper. In Sec. VI, we discuss their
phenomenological implications.

III.

THE MISSING ENERGY SIGNAL

This section outlines the missing energy/momentum
signatures in the 2 → 4 reactions which can be searched
for with the electron fixed-target experiments NA64e [28–
32] and LDMX [44–49]. Specifically, the signature of interest arises from a reaction of a high-energy electron
scattering on a heavy target nucleus N :
eN → eN aγD ,

(5)

where the scattered electron in the final state is accompanied by a significant missing energy which is carried away
by the ALP, a, and dark photon, γD escaping detection.
Within the minimal dark axion portal scenario (1),
one of the source of the missing energy (Emiss ) is the
bremsstrahlung-like production of an aγD pair via an
off-shell photon. The complete process, eN → eN γ ∗ →
eN aγD , is followed by the prompt invisible decay of the
dark photon, γD → χ̄χ, into stable dark sector fermions.
A representative Feynman diagram for this mechanism is
shown in Fig. 1.
While electron bremsstrahlung remains a primary
mechanism for producing hidden sector particles,
Ref. [48] proposes a complementary source of missingenergy signatures (see e. g. Refs. [57–60] for recent study
of meson decays to DM particles at fixed-target experiments). This alternative channel implies the exclusive
photoproduction of a high-energy vector meson V (such
as ρ, ω, ϕ, or J/ψ) on a target nucleus N , via the reaction
γ ∗ N → N V . The initial off-shell photon γ ∗ originates
from standard bremsstrahlung, eN → eN γ ∗ .
In this analysis, we focus on a specific invisible decay
mode of these vector mesons. We consider the process,
see Fig. 2, where a meson decays into an off-shell photon, which then converts into an ALP and a dark photon:
V → γ ∗ → aγD . This channel provides a distinct signature of the dark axion portal, contributing to the total
missing energy in the final state.
In the dark axion portal scenario, the dark photon can
decay via several channels. For masses satisfying mγD ≳
ma , a visible two-body decay into ALP and SM photon

## PDF page 3

3

FIG. 1. Feynman diagrams illustrating the bremsstrahlung-like production of an ALP and a dark photon in electron-nucleus
scattering, eN → eN aγD . These diagrams correspond to the missing-energy signature within the minimal dark axion portal
scenario, governed by the effective Lagrangian L ⊃ 12 gaγγD aFµν F̃ ′µν . In this analysis, the produced dark photon decays
predominantly into invisible dark sector fermions, γD → χχ̄. Diagrams involving photon emission from the nucleus line are
omitted, as their contribution is suppressed by a factor of order (Zme /MN )2 for electron-nucleus scattering and is therefore
negligible.

becomes kinematically allowed. Its partial decay width
is given by [40]:
2
gaγγ
D
m3
ΓγD →aγ =
96π γD

(
)3
m2a
1− 2
.
mγD

(6)

Simultaneously, the Lagrangian of Eq. (2) permits an
invisible decay into a pair of dark sector fermions, γD →
χ̄χ, provided mγD ≳ 2mχ . The corresponding partial
width is [61]:
g2
ΓγD →χ̄χ = D mγD
12π

(

2m2χ
1+ 2
mγD

)(

4m2χ
1− 2
mγD

)1/2
. (7)

This work focuses on the scenario where the dark photon decays invisibly into a dark fermion pair, γD → χ̄χ.
We assume a branching fraction BrγD →χ̄χ ≃ 1, which
is naturally satisfied for mχ ≪ mγD . This condition requires the invisible decay width to dominate over the visible channel, ΓγD →χ̄χ ≫ ΓγD →aγ . Consequently, a hierarchy between the couplings is implied, gD ≫ gaγγD mγD .
Under this hierarchy, any produced dark photon decays
predominantly into the dark sector.
Furthermore, to ensure the invisibility of the final state
within the fixed-target detector, we require the ALP mass
to be significantly smaller than the dark photon mass,
ma ≪ mγD . This kinematically suppresses the potentially visible decay a → γγD , guaranteeing that both the
ALP and the dark sector fermions escape the experiment
undetected, resulting in a clean missing-energy signature.

A.

Bremstrahlung-like production: γ ∗ → aγD

The expected number of missing-energy events from
the process eN → eN γ ∗ → eN (aγD ), where the electron
scatters off a target nucleus N , can be estimated as:
ρNA
LT
Nγ ∗ →aγD ≃ EOT ·
A

E
∫max

dEmiss
Emin

dσ2→4 (Ee )
. (8)
dEmiss

In this expression, Ee is the initial electron beam energy, EOT is the total number of electrons on target,
and ρ, A, and LT denote the density, atomic mass, and
effective length of the target, respectively. The symbol NA represents Avogadro’s number. The differential cross section dσ2→4 (Ee )/dEmiss describes the 2 → 4
bremsstrahlung-like process eN → eN γ ∗ → eN aγD , and
Emiss = Ea + EγD is the total energy carried away by the
invisible ALP and dark photon system. The integration
limits Emin and Emax are set by the specific energy acceptance and selection criteria of the experimental setup.
We compute the relevant 2 → 4 cross sections using
the CalcHEP software package [62]. To this end, we
have extended the SM implementation in CalcHEP by
introducing two new massive particles: the ALP a and
the dark photon γD . Their interaction with the SM photon is incorporated via the effective Lagrangian term (1).
The target nucleus is modeled as a spin-1/2 particle with
mass MN , atomic mass A, and charge Z. Its coupling
to the photon is implemented through the vertex factor
ieZF (t)γµ , where t = −q 2 > 0 is the squared momentum transfer to the nucleus and F (t) denotes the nuclear
elastic form factor. Following [63, 64], we employ the
parameterization
F (t) =

a2 t
1
,
2
1 + a t 1 + t/d

(9)

with screening and finite-size parameters given by a =
111Z −1/3 /me and d = 0.164A−2/3 GeV2 . This form
factor is incorporated into the analytic expression for
the squared matrix element |MeN →eN aγD |2 generated by
CalcHEP, and the corresponding C++ source files have
been modified accordingly.
Using the experimental parameters detailed in Sec. IV,
we numerically integrate the exact tree-level amplitude
squared for the process eN → eN γ ∗ (→ aγD ) over the full
final-state phase space. This computation is performed
within the CalcHEP framework. For a given target material and a fixed electron beam energy Ee , we evaluate the
total cross section σtot as a function of the dark photon
mass mγD , scanning the range 1 MeV ≲ mγD ≲ 1 GeV
while fixing the ALP mass at ma ≃ 10 keV.

## PDF page 4

4
The multidimensional phase-space integration is carried out using the VEGAS adaptive Monte Carlo algorithm. We configure the integration with Nsession = 10
independent runs, each employing Ncalls = 106 sampling
points. The adaptive grid optimization within VEGAS
achieves a numerical precision of approximately O(0.1)%
to O(0.01)% in the final cross-section results.

B.

Production via vector meson decays: V → aγD

The expected number of missing-energy events from
the process eN → eN γ ∗ → eN (aγD ), where the electron
scatters off a target nucleus N , can be estimated as:

where NV is the total number of the specific vector meson, BrV →aγD is the invisible branching fraction of vector
meson associated with dark ALP portal scenario. Specifically, it is given by
BrV →aγD = ΓV →aγD /ΓVtot

where ΓVtot and ΓV →aγD are the total and invisible decay
width of the vector meson, respectively. In order to calculate ΓV →aγD , we employ the vector meson dominance
(VMD) framework [65]. The relevant mixing between
ordinary SM photon, Aµ , and vector meson, Vµ , reads
LVMD ⊃ −

∑ e m2

V

V

NV = EOT × fbrem × PV ,
where EOT is the total number of electrons on target,
fbrem denotes the fraction of incident electrons that emit
a hard bremsstrahlung photon capable of producing the
meson, and PV represents the probability for such a photon to undergo an exclusive photoproduction interaction
on the target. Following the treatment in Ref. [48], the
photoproduction probability can be approximated as
PV ≃

with X0 the radiation length of the target material, σ0V
the exclusive photoproduction cross section on a single
V
nucleon, and fnuc
an O(1) nuclear correction factor.
For the LDMX Phase-II design, Ref. [48] estimates
LDMX
fbrem
≃ 0.03. Assuming the ultimate planned integrated luminosity of EOT ≃ 1016 , the resulting yields for
light vector mesons are
Nρ ≃ 3 × 1010 ,

Nω ≃ 3 × 109 ,

Nϕ ≃ 5 × 108 . (10)

These yields correspond to a total meson production
ranging from O(108 ) to O(1010 ) events.
For the NA64e planned statistics of EOT ≃ 5 × 1012
the typical numbers of vector mesons are estimated to
be [48]
Nρ ≃ 1.2 × 108 , Nω ≃ 9 × 106 ,

(11)

Nϕ ≃ 8 × 106 , NJ/ψ ≃ 1.1 × 105 ,
these values imply the typical fraction of hard
NA64e
bremsstrahlung electrons at the level of fbrem
≃ 0.5.
Remarkably, at LDMX energies, J/ψ production is kinematically forbidden. However, its coherent γ ∗ N →
N J/ψ production is kinematically allowed at the NA64e
facility.
As a result, the typical signal yield associated with vector meson invisible decay into pair of ALP-dark photon
particles reads
NV →aγD ≃ NV × BrV →aγD ,

(12)

gV

Aµ V µ ,

(14)

where mV is a vector meson mass, e is the elementary
electric charge, and gV is a dimensionless coupling constant that can be extracted from the data on strong decays [66]. In Tab. I we collect all vector meson terms
relevant for our analysis.
The amplitude for an on-shell vector meson V to decay
to aγD via virtual photon γ ∗ reads
MV →aγD = ϵµ (q)

V
9 σ0V X0 fnuc
,
7
mp

(13)

em2V gµν
gaγγD ϵνλρσ kλ qρ ϵ∗σ (k), (15)
gV q 2

where q ρ and k λ are the momenta of the vector meson
and dark photon, respectively. Squaring and summing
over final dark photon polarizations ϵ∗σ (k) and averaging
over initial meson polarizations ϵµ (q) yields the decay
rate in the rest frame of the meson:
(
)3
2
e2 gaγγ
m2γD
m3V
D
ΓV →aγD =
1− 2
.
(16)
96π gV2
mV
To evaluate the decay width (16), we employ the FeynCalc package [67] within the Wolfram Mathematica environment [68]. This calculation assumes the mass hierarchy mγD ≫ ma , allowing us to safely neglect the ALP
mass, consistent with the assumptions outlined earlier.
The resulted number of missing energy events reads
∑
Nsign. ≃ Nγ ∗ →aγD +
NV →aγD .
(17)
V

In Fig. 3 we show the total number of aγD pairs produced at the NA64e and LDMX experiments as a function of mγD .
For the LDMX, the dominant production mechanism
of relatively light dark photons, mγD ≲ 30 MeV, is associated with off shell photon emission, γ ∗ → aγD , while
for the heavier dark photons, mγD ≳ 100 MeV, the relevant rate is comparable with vector meson one V → aγD ,
i. e. the vector mesons provide a sizable contribution to
the missing energy signal. Accounting for the V meson
contribution, would result in sensitivity enchantment of
the LDMX to the dark ALP portal coupling, gaγγD , in
the sub-GeV mass range, mγD ≲ 1 GeV.

## PDF page 5

5

FIG. 2. Feynman diagrams for the radiative invisible vector meson decay. A hard photon γ ∗ is produced in the target,
eN → eN γ ∗ , and converts to a vector meson V in the exclusive photoproduction process γ ∗ N → N V in the calorimeter. Then
vector meson decays invisibly to the aγD pair via mixing with the ordinary of-shell photon, γ ∗ . The produced dark photon
dominantly decays into invisible DS particles, γD → χχ̄.

TABLE I. Parameteres of vector mesons (mass mV , coupling
constant gV , total decay width ΓVtot ) relevant for our analysis.
V

mV (MeV)

gV

ΓVtot (MeV)

ρ

775

4.96

147

ω

782

17.3

8.6

ϕ

1019

13.4

4.2

J/ψ

3097

11.8

0.093

Υ

9460

40.3

0.054

The NA64e signal associated with coherent photoproduction of the J/ψ meson yields a rate comparable to
that of γ ∗ → aγD for sufficiently light hidden vectors,
i. e. , for masses mγD ≲ 10 MeV. The total number of
missing energy signatures depends weakly on dark photon mass mγD , This implies a sufficiently mild slope of
the graph for the sub-GeV dark photons. The production
of ρ, ω and ϕ vector mesons at NA64e is subdominant for
the entire mass range of interest 1 MeV ≲ mγD ≲ 1 GeV.
For both experiments, the yields of ϕ mesons are lower
than the yields of ω mesons. Nevertheless, as shown in
Fig. 3, the invisible decays of ϕ mesons can provide better
sensitivity due to the larger branching ratio compared to
that of the ω meson.

IV.

BENCHMARK EXPERIMENTS

The missing energy analysis for the process eN →
eN aγD applied to both NA64e and LDMX builds upon
the established frameworks developed for the related dark
photon search eN → eN γD , as detailed in Refs. [43]
and [50], respectively. The experimental signatures for
these two channels are nearly identical: both experiments
search for events with a single scattered electron in the
final state and a large missing energy, typically exceeding ≳ 50% of the initial beam energy. This stringent
requirement on the missing energy fraction, enabled by a
fully hermetic detector design, provides a powerful tool

for suppressing standard model backgrounds.
We now outline the benchmark input parameters used
for each experimental setup.

A.

The NA64e experiment

The NA64e employs the optimized electron beam from
the H4 beam line at the SPS at CERN. The maximum
intensity of the beam is ≃ 107 electrons per spill of 4.8 s,
the number of good spills is estimated to be 4000 per day.
The reaction for dark photons and ALPs production,
eN → eN aγD , involves the scattering of a high-energy
electron beam (Ee = 100 GeV) off heavy nuclei of a leadscintillator electromagnetic calorimeter (ECAL) surving
as an active target, followed by the prompt invisible decay γD → χ̄χ. A significant fraction of the primary beam
energy, Emiss , is carried away by the aγD system (and
subsequently by the dark sector fermions), leaving no
detectable signal in the hermetic NA64e detector. The
remaining energy, Eerec ≡ Ee − Emiss , is deposited in
the ECAL by the scattered electron. Consequently, the
production of hidden particles manifests as an excess of
events containing a single electromagnetic shower with
energy Eerec above the expected background (see, e.g.,
Ref. [27]). The ECAL target of NA64e is a matrix of
6 × 6 Shashlyk-type modules assembled from lead (Pb)
(ρ = 11.34 g cm−3 , A = 207 g mole−1 , Z = 82) and scintillator (Sc) plates. Note that production of hidden particles in the scintillator is subleading due to its larger
radiation length, X0 (Sc) ≫ X0 (P b), thus we ignore it in
the calculation.
Additionally, we assume that the electromagnetic
shower in the ECAL is initiated within its typical radiation length of 0.56 cm. This defines the effective interaction length in Eq. (8) as LT ≃ X0 , implying that the
dominant production of hidden particles occurs within
the initial radiation length of the active ECAL [69]. Candidate events are required to satisfy Eerec ≲ 0.5Ee , corresponding to a lower integration limit of Emin = 50 GeV
in Eq. (8).
The dominant background sources for the NA64e
missing-energy search are identified as [43]: (i) muon pair

## PDF page 6

6

FIG. 3. The plot shows the number of aγD pairs produced versus γD mass for both LDMX (1016 EOT) and NA64e (5 ×
1012 EOT), with the coupling constant chosen to be gaγγD = 1 GeV−1 . The hidden particles are produced in bremsstrahlunglike reactions and various meson decays. Left panel: the resulted number of invisible signal events for the LDMX experiment, the
aγD pairs are produced through the bremsstrahlung-like channel γ ∗ → aγD (red line), rho meson ρ → aγD (brown line), omega
meson ω → aγD (orange line), and phi meson decay ϕ → aγD (green line). The resulted number of aγD pairs produced at the
LDMX is shown (blue line). Right panel: the same as in the left panel, but for the NA64e electron missing momentum facility,
implying that the dominant signal mechanisms are due to the virtual photon emission γ ∗ → aγD (red line) and J/ψ → aγD
decays (black line).

losses or decays in the target; (ii) in-flight decays along
the beamline; (iii) insufficient calorimeter hermeticity;
and (iv) particles passing through the calorimeter without interaction.
We adopt the background study presented in Ref. [43],
which reports an estimated background of b ≪ 1 events
for the currently accumulated exposure of EOT ≃ 9.37 ×
1011 . For the projected future exposure of EOT ≲ 1013 ,
we anticipate that upgraded detector electronics and refined veto systems will improve background rejection by
an O(1) factor. This improvement is expected to maintain the total background at a level b ≲ 1 event, ensuring
a statistically negligible background for the planned sensitivity studies with ≃ 1013 EOT.

B.

The LDMX experiment

The LDMX is a proposed electron fixed-target experiment at Fermilab, sharing a similar beam-based approach with NA64e. LDMX is specifically designed to
reconstruct the missing momentum of the scattered electron, providing a complementary probe of the process in
Eq. (5). The stringent missing-momentum requirements
and extensive active veto systems employed by both experiments render them virtually background-free for the

signal topology under consideration [27, 45].
The conceptual design of LDMX comprises a thin target, a precision silicon tracker, and downstream electromagnetic and hadronic calorimeters. For detailed descriptions of the detector layout and subsystems, see
Refs. [45, 49].
A significant fraction of the primary electron beam
energy is lost via the emission of dark-sector particles
within a thin upstream target. The resulting missing
momentum of the scattered electron is reconstructed using a downstream silicon tracker system complemented
by electromagnetic and hadronic calorimeters.
For the numerical analysis presented here, we consider
an aluminum target with the following properties: radiation length X0 = 8.9 cm, density ρ = 2.7 g cm−3 , atomic
mass A = 27 g mol−1 , and atomic number Z = 13. The
effective target thickness is taken as LT ≃ 0.4X0 . According to its design parameters, LDMX plans to accumulate an integrated luminosity of EOT ≃ 1016 electrons
on target, with a beam energy of up to Ee = 8 GeV during its second operational phase [48].
For the LDMX analysis, we adopt selection criteria
based on prior studies searching for invisibly decaying
dark photons in the sub-GeV mass range [45, 48, 49].
This approach is well justified, as the experimental signatures for the processes eN → eN aγD and eN → eN γD

## PDF page 7

7
are nearly identical. The similarity arises because the
differential energy spectra of the aγD system and a single dark photon share a common kinematic shape, with
production dominated by the forward scattering region.
Consequently, we apply the same missing-energy cut used
in those references, requiring the reconstructed electron
energy to satisfy Eerec ≲ 0.3Ee . This corresponds to
a lower integration limit of Emin = 0.7Ee ≃ 5.6 GeV
in Eq. (8) for an Ee ≃ 8 GeV beam.
Based on current simulation studies, the residual backgrounds for LDMX originate primarily from four categories [50]: (i) unbiased electron interactions, (ii) photonuclear reactions, (iii) electro-nuclear interactions, and
(iv) muon conversion events. To maintain sensitivity at
the planned exposure of EOT ≃ 1016 , a targeted upgrade
of the front-end electronics and trigger systems is underway [50]. The objective of these detector improvements
is to achieve an effectively background-free experiment,
ensuring that the projected background remains below a
single event across the light dark state parameter space
targeted by the benchmark search [45, 49].

V.

EXISTED AND EXPECTED SENSITIVITIES

Recent theoretical and phenomenological developments in the dark axion portal framework are summarized as follows. The regarding portal itself was formalized in Ref. [74], which proposed that the coupled system of axions and dark photons could provide a viable
mechanism to account for the observed dark matter relic
density [75].
Subsequently, detailed phenomenological studies have
explored its experimental signatures. Ref. [39] provided a
comprehensive analysis of potential signals at B-factories,
fixed-target neutrino experiments, and beam-dump facilities. Further investigations have focused on specific
channels: the monophoton signature arising from the decay γD → aγ was examined for the experiments such as
LUXE–NPOD [76], SHIP [77], FASER [78], and LHC [79]
in Refs. [40, 80–82]. While a complementary analysis for
reactor neutrino experiments was presented in Ref. [83].
In addition, authors of Ref. [84] proposed a scenario that
connects the dark axion portal phenomenology to a potential solution for the electroweak hierarchy problem.
As emphasized previously, our analysis focuses on the
scenario where the dark photon decays invisibly into dark
sector fermions, γD → χχ̄ and mγD > ma . Consequently,
the exclusion limits derived from searches for visible dark
photon signatures are not directly applicable to the parameter space considered in the following subsections.

A.

Collider based constraints

An authors of Ref. [71] proposed to utilize the ATLAS
as a muon fixed-target experiment. To be more specific,

FIG. 4. The limits at 90 % CL on gaγγD coupling from ATLAS, BaBar, and the fixed-target experiments for the minimal dark ALP portal setup as a function of the dark photon
mass mγD . For the accelerator based sensitivity curves we
imply that Br(γD → χχ̄) ≃ 1 and ma = 10 keV. Green
dashed line is the projected sensitivity for NA64e experiment
for EOT ≃ 5 × 1012 , and blue dashed line corresponds to
the projected sensitivity of LDMX facility for EOT ≃ 1016 .
The shaded green region shows the parameter space excluded
by the NA64e experiment for EOT ≃ 9.37 × 1011 . For completeness, by dashed dotted green lines we show the expected
reaches of NA64e for EOT ≃ 1013 with a finite background,
b ≃ 1, and background free, b ≃ 0, case. We also show the
BaBar [41] excluded bounds for the data on monophoton missing energy signature, e+ e− → γaγD . The BaBar limits [70]
from invisible decays Υ(1S) → aγD are shown by brown solid
line. The projected bounds of ATLAS (L ≃ 3 ab−1 ) associated with muon missing momentum process, µN → µN aγD
are shown by black dashed line [71, 72]. The region of parameter space excluded by supernova (SN) is shown by shaded
red area [73].

authors considered a novel analysis for the ATLAS detector, which takes advantage of the two independent muon
momentum measurements by the inner detector and the
muon system. They also provide the expected reach for
the muon-philic sub-GeV hidden vector, L ⊃ gγD A′ν µ̄γν µ
(see e. g. left panel of Fig. 4 from Ref. [71]) in (mγD , gγD )
plane from ATLAS experiment for projected luminosoty
of L ≃ 3 ab−1 , implying muon missing momentum signature, µN → µN γD . These limits can be relevant for
our benchmark scenario, if one recasts the expected reach
(mγD , gγD ) → (mγD , gaγγD ). Specifically, one can obtain
ATLAS
the relevant for our analysis conservative limit on gaγγ
D
from the plot shown in Fig. 4 of Ref. [71]. For the mass
range of interest 1 MeV ≲ mγD ≲ 1 GeV the rough esti-

## PDF page 8

8
mate yields the following relation between couplings:
NA64µ
ATLAS
,
/gγNA64µ
× gaγγ
≃ gγATLAS
gaγγ
D
D
D
D

(18)

NA64µ
are the experimental reaches
and gγNA64µ
where gaγγ
D
D
of the muon missing momentum facility NA64µ adapted
from Ref. [71] and Ref. [41], respectively for the equivalent anticipated statistics of muons accumulated on target. The conservative estimate (18) is justified by the
the similar missing energy cuts and typical muon beam
energies at ATLAS and NA64µ.
In Fig. 4 we also show The BaBar excluded bounds
for the data on monophoton missing energy signature,
e+ e− → γaγD , adapted from [41]. These BaBar bounds
at the level of gaγγD ≲ 1.5×10−2 GeV−1 rule out the projected limits of ATLAS, gaγγD ≲ 3 × 10−2 GeV−1 , which
can operate as muon missing momentum facility [71].
For the sub-GeV dark photon masses, a sufficiently
strong bound,

gaγγD ≲ 2.0 × 10−2 GeV−1 ,

(19)

can be set from BaBar data [70] on invisible Υ meson
decay. Namely, the regarding branching fraction is constrained to be
BrΥ→inv. ≲ 3 × 10−4

(20)

at 90% CL. That limit can be associate with a relevant
for our analysis bound on the invisible branching fraction of Υ(1S) → aγD vector meson. In order to extract
the coupling constant bound from this limit, we employ
again VMD model for Υ(1S) meson, implying that typical mixing with photons is estimated to be, gΥ ≃ 40.3
from its radiative decay into e+ e− pair. Specifically, the
VMD constant can be linked with leptonic decay width,
ΓΥ→e+ e− ≃ 1.3 keV as follows,
(
gΥ ≃

4πα2 mΥ
3ΓΥ→e+ e−

)1/2
≃ 40.3,

(21)

where α ≃ 1/137 is a fine structure coupling constant,
mΥ ≃ 9460 MeV is a mass of Υ(1S) meson. The resulted
bound (19) is obtained by incorporating data in Tab. I,
Eqs. (20) and (16). The Υ invisible decay bounds (5) rule
out both BaBar monophoton, e+ e− → γaγD , limits and
ATLAS muon missing energy, µN → µN aγD , projected
sensitivities.

B.

Astrophysical constraints

In this subsection we follow Ref. [73] to overview briefly
other constrains on dark axion portal coupling (1) coming
from the supernova bounds.
The supernova SN1987A has served as an important
astrophysical laboratory for probing physics beyond the
SM. The impact of novel particle emission on supernova cooling is characterized by two distinct transport

regimes, defined by the interaction strength of the new
particle species. In the weak-coupling limit, particles produced in the stellar core undergo negligible re-scattering,
freely escaping the proto-neutron star volume. This defines the transparent or free-streaming regime, where energy loss is proportional to the production rate. Constraints derived in this regime establish a lower bound on
the particle coupling, as any stronger interaction would
only enhance the emission and violate observational limits.
Conversely, if the coupling is sufficiently strong, the
novel particles achieve local thermal equilibrium and become trapped within the dense medium. In this trapping regime, energy is transported diffusively and radiated from a neutrinosphere- like last scattering surface.
As the coupling strength increases, this effective emission surface recedes to larger radii and lower temperatures within the stellar gradient, thereby reducing the
spectral luminosity. This behavior generates an upper
bound on allowable couplings, as excessively strong interactions suppress the emergent flux below levels detectable from SN1987A. The full exclusion contour, spanning from the free-streaming lower bound to the trapping
upper bound, is plotted within the framework of the Raffelt criterion [85]. In Fig. 4 we show the relevant bounds
by shaded red region, adapted from [73].

C.

The reach of the missing energy experiments

By using Eq. (17) to calculate the expected number
of aγD production events, we derive projected exclusion
limits on the portal coupling gaγγD within the minimal
dark ALP portal framework. Assuming a backgroundfree search (b ≃ 0) and a null observation, nobs. ≃ 0,
we set a 90% confidence level (CL) exclusion criterion
corresponding to a signal yield of Nsign. ≳ 2.3 events.
This criterion is used to determine the upper bounds on
gaγγD presented in the following analysis.
In Fig. 4 we show the expected reach of NA64e and
LDMX by green and blue solid lines, respectively. Note
that projected limits on gaγγD from LDMX are fairly
strong, i. e. for small masses of dark photon, mγD ≃
O(1) MeV the expected reach is estimated to be at the
level of g ≲ O(10−4 ) GeV−1 . The regarding LDMX sensitivity enchantment can be explained by the large number of the projected accumulated statistics, EOT ≃ 1016 ,
by the final phase of experimental running.
In addition, we note that the projected limits of NA64e
for EOT ≃ 5 × 1012 can rule the typical couplings at the
level of gaγγD ≲ (3.5−5)×10−3 GeV−1 for sub-GeV dark
photons. In Fig. 4 we show by the shaded green region
the excluded limits of NA64e for the current accumulated
statistics [31] of EOT ≃ 9.37 × 1011 . To be more specific,
the current bounds of NA64e rules out the couplings in
the range 8 × 10−3 GeV−1 ≲ gaγγD ≲ 1.5 × 10−2 GeV−1
for the dark photon masses of interest, mγD ≲ 1 GeV.
To perform additional conservative projection, in

## PDF page 9

9
TABLE II. Upper limits on couplings of new particles from data on EDMs of electron, muon, and neutron.
Coupling combination
[ (
)
]
mγD = ma ≫ mf , |gfa gaγγD eϵf | × log Λ2 /m2γD + 1/2 :

Electron (90 % CL)

Muon (95 % CL)

Neutron (90 % CL)

≲ 5.0 × 10−15 GeV−1 , ≲ 2.3 × 10−4 GeV−1 , ≲ 2.2 × 10−11 GeV−1 ,
[ (
)
]
mγD ≫ mf ≫ ma , |gfa gaγγD eϵf | × log Λ2 /m2γD + 5/2 :

FIG. 5. Feynman diagrams which generate EDM terms due
to axion coupling with both dark and SM photons (see, e. g.,
Eq. (22) for detail).

Fig. 4 we also show the expected reaches of NA64e implying the anticipated statistics of EOT ≃ 1013 for both
background free, b = 0, and non-negligible number of regarding events, b ≃ 1 (see, e. g., Ref. [86] and references
therein for detail). To summarize principal findings of
this section, we note that accounting for vector mesons
would result in a sensitivity enhancement by a factor of
O(1) for the LDMX facility in the large mass region,
mγD ≲ 1 GeV. In contrast, for the NA64e experiment,
vector meson decays enhance its sensitivity to dark ALP
portal by several orders of magnitude for the sub-GeV
mass range. However, a sufficiently large portion of the
parameter space within, 500 MeV ≲ mγD ≲ 1 GeV is
constrained from the SN1987A.
VI.

BOUNDS FROM FERMION EDMS

In this section, we derive the constraints on the combinations of P -even and P -odd couplings of new particles
using data on electric dipole moments (EDMs) of leptons and neutron. The contributions of new particles to
EDMs are described by the Bar-Zee diagrams in Fig. 5.
This contribution is generated by an additional interaction Lagrangian containing three terms: (i) P -parity violating coupling of ALP with SM fermions, gfa , (ii) P parity conserving coupling of ALP with SM photon and
dark photon, gaγγD , and (iii) P -parity conserving coupling of dark photon with SM fermions, eϵf ,
gaγγD
L ⊃ gfa af¯f +
aFµν F̃ ′µν + eϵf f¯γ µ A′µ f .
2

(22)

To be more specific, the EDM of spin- 12 fermion f
(neutron or leptons) is defined as df = DE (0, Λ), where

FIG. 6. Boundaries for the product of CP-odd and CP-even
couplings from EDM neutron and electron/muon as the function of the dark photon mass.

DE (q 2 , Λ) is the relativistic electric dipole form factor extracted from full electromagnetic vertex function of corresponding fermion [87–91]:
Minv = ūf (p2 ) Γµ (p1 , p2 ) uf (p1 ) ,
Γµ = −σ µν qν γ 5 DE (q 2 , Λ) + . . . ,

(23)

where q = p1 − p2 is a momentum of photon. The contribution of dark axion portal depicted in Fig. 5 is divergent. With the cut-off regularization, the result in (23)
is expressed in terms of the ultra-violet (UV) scale, Λ.
In particular, the relevant contributions of the specific
diagrams in Fig. 5 read [41]
df = −

[
]
G
1 I(m2γD , m2f ) − I(m2a , m2f )
−
+
, (24)
4π 2
2
m2γD − m2a

where G = gfa gaγγD eϵf is a product of the coupling constants, and auxiliary loop function I(m2 , m2f ) is defined

## PDF page 10

10
such as LDMX and NA64e. In particular, we calculated
the rate of aγD pair production processes eN → eN aγD
followed by the invisible dark photon decay into DS particles γD → χχ̄ for the specific fixed target facility.

as
2

I(m , m2f )

∫1
=

]
[
dx m2 (1 − x) + m2f x2

0

m2 (1 − x) + m2f x2
.
× log
Λ2

(25)

Since the interaction in (1) is non-renormalizable, we
treat Λ as scale up to which our consideration is valid.
Using the upper limits/results for the electron, muon,
and neutron EDMs:
|de | < 4.1 × 10−30 e cm,
|dµ | < 1.9 × 10−19 e cm,

at 90 % CL, Ref. [92] ,
at 95 % CL, Ref. [93] ,

|dn | < 1.8 × 10−26 e cm,

at

90 % CL, Ref. [94] ,

we get the upper limits for combinations of couplings of
new particles, which are displayed in Tab. II. We set for
concreteness two benchmark cut-off scales Λ ≃ 100 GeV
and Λ ≃ 200 GeV and plot relevant limits in Fig. 6 for the
following approaches: (i) heavy dark photon with mass
hierarchy, mγD ≫ ma ≫ mf , (ii) equivalent mass of dark
photon and ALP, mγD = ma ≫ mf .
It turns out that the electron EDM, which is currently constrained by the JILA collaboration [92] is
very sensitive to probe non-minimal CP-odd dark ALP
portal scenario (22) at the level of |gea gaγγD eϵe | ≲
O(10−15 ) GeV−1 . The upper bounds on the coupling
combination for the muon - and neutron- specific scenarios are estimated to be at the level of |gµa gaγγD eϵµ | ≲
O(10−5 ) GeV−1 and |gna gaγγD eϵn | ≲ O(10−12 ) GeV−1 ,
respectively. The bounds on the combinations of couplings depend logarithmically on dark photom mass

We derive new exclusion limits based on the NA64e
data set with 9.37×1011 EOT by considering two distinct
production mechanisms leading to invisible final states:
(i) the bremsstrahlung-like emission of an ALP-dark photon pair, eN → eN γ ∗ (→ aγD ), and (ii) exclusive vector
meson photoproduction, γ ∗ N → N V , followed by the
invisible decay V → aγD .
We find that vector mesons enhance sensitivity differently across experiments. For LDMX in the mγD ≲
1 GeV region, the enhancement factor is O(1). For NA64,
vector meson decays boost sensitivity to the dark ALP
portal by several orders of magnitude.
In a separate analysis, we establish constraints on the
parameter space of CP -violating, fermion-specific ALP
couplings. These bounds are obtained by correlating the
contributions of such couplings to the electric dipole moments of the SM fermions. Specifically, we utilize current
experimental limits on the EDM of SM fermions and include the associated, loop-induced contributions to the
EDMs of the electron, muon, and neutron.

ACKNOWLEDGMENTS

We have studied the missing energy signatures for the
projected and existed electron fixed target experiments,

We would like to thank I. Galon, S. Demidov,
R. Dusaev, A. Pukhov, and Y. Soreq, for very helpful
discussions and correspondences. The work of V. E. L.
and S. K. on deriving EDM bounds was funded by
FONDECYT (Chile) under Grant No. 1240066 and by
ANID−Millennium Program−ICN2019 044 (Chile). The
work of D. V. K on deriving sensitivities for both NA64e
and ATLAS experiments was supported by the the Russian Science Foundation grant No. 25-12-00309.

[1] R. D. Peccei and Helen R. Quinn, “Constraints Imposed
by CP Conservation in the Presence of Instantons,” Phys.
Rev. D 16, 1791–1797 (1977).
[2] Luca Di Luzio, Maurizio Giannotti, Enrico Nardi, and
Luca Visinelli, “The landscape of QCD axion models,”
Phys. Rept. 870, 1–117 (2020), arXiv:2003.01100 [hepph].
[3] C. Boehm and Pierre Fayet, “Scalar dark matter candidates,” Nucl. Phys. B 683, 219–263 (2004), arXiv:hepph/0305261.
[4] Matthew J. Dolan, Felix Kahlhoefer, Christopher McCabe, and Kai Schmidt-Hoberg, “A taste of dark matter: Flavour constraints on pseudoscalar mediators,”
JHEP 03, 171 (2015), [Erratum: JHEP 07, 103 (2015)],
arXiv:1412.5174 [hep-ph].

[5] Yonit Hochberg, Eric Kuflik, Robert Mcgehee, Hitoshi
Murayama, and Katelin Schutz, “Strongly interacting
massive particles through the axion portal,” Phys. Rev.
D 98, 115031 (2018), arXiv:1806.10139 [hep-ph].
[6] C. Han, M. L. López-Ibáñez, A. Melis, O. Vives, and
J. M. Yang, “Anomaly-free leptophilic axionlike particle
and its flavor violating tests,” Phys. Rev. D 103, 035028
(2021), arXiv:2007.08834 [hep-ph].
[7] Hooman Davoudiasl, Roman Marcarelli, and Ethan T.
Neil, “Lepton-Flavor-Violating ALPs at the ElectronIon Collider:
A Golden Opportunity,”
(2021),
arXiv:2112.04513 [hep-ph].
[8] S. N. Gninenko and N. V. Krasnikov, “Leptonic scalar
portal: the origin of muon g − 2 anomaly and dark matter?” (2022), arXiv:2202.04410 [hep-ph].

VII.

CONCLUSION

## PDF page 11

11
[9] Martin Bauer, Matthias Neubert, Sophie Renner, Marvin Schnubel, and Andrea Thamm, “The Low-Energy
Effective Theory of Axions and ALPs,” JHEP 04, 063
(2021), arXiv:2012.12272 [hep-ph].
[10] Kiwoon Choi, Sang Hui Im, and Chang Sub Shin, “Recent Progress in the Physics of Axions and Axion-Like
Particles,” Ann. Rev. Nucl. Part. Sci. 71, 225–252 (2021),
arXiv:2012.05029 [hep-ph].
[11] R. R. Dusaev, D. V. Kirpichnikov, and M. M. Kirsanov, “Photoproduction of axionlike particles in the
NA64 experiment,” Phys. Rev. D 102, 055018 (2020),
arXiv:2004.04469 [hep-ph].
[12] D. Banerjee et al. (NA64), “Search for Axionlike and
Scalar Particles with the NA64 Experiment,” Phys. Rev.
Lett. 125, 081801 (2020), arXiv:2005.02710 [hep-ex].
[13] Hiroyuki Ishida, Shinya Matsuzaki,
and Yoshihiro
Shigekami, “New perspective in searching for axionlike
particles from flavor physics,” Phys. Rev. D 103, 095022
(2021), arXiv:2006.02725 [hep-ph].
[14] Yasuhito Sakaki and Daiki Ueda, “Searching for new
light particles at the international linear collider main
beam dump,” Phys. Rev. D 103, 035024 (2021),
arXiv:2009.13790 [hep-ph].
[15] Vedran Brdar, Bhaskar Dutta, Wooyoung Jang, Doojin Kim, Ian M. Shoemaker, Zahra Tabrizi, Adrian
Thompson, and Jaehoon Yu, “Axionlike Particles at
Future Neutrino Experiments: Closing the Cosmological Triangle,” Phys. Rev. Lett. 126, 201801 (2021),
arXiv:2011.07054 [hep-ph].
[16] Dmitry Salnikov, Petr Satunin, D. V. Kirpichnikov, and
Maxim Fitkevich, “Examining axion-like particles with
superconducting radio-frequency cavity,” JHEP 03, 143
(2021), arXiv:2011.12871 [hep-ph].
[17] Dmitry Salnikov, Petr Satunin, and D. V. Kirpichnikov,
“Probing axion-like particles with RF cavities separated
by a thin barrier,” Phys. Lett. B 873, 140142 (2026),
arXiv:2405.04983 [hep-ph].
[18] Yonatan Kahn, Bianca Giaccone, Andrei Lunin,
Alexandr Netepenko, Roman Pilipenko, and Michael
Wentzel, “Searching for axions and light-by-light scattering with superconducting RF cavities,” Proc. SPIE Int.
Soc. Opt. Eng. 12016, 29 (2022).
[19] Luc Darmé, Federica Giacchino, Enrico Nardi, and
Mauro Raggi, “Invisible decays of axion-like particles: constraints and prospects,” JHEP 06, 009 (2021),
arXiv:2012.07894 [hep-ph].
[20] P. S. Bhupal Dev, Doojin Kim, Kuver Sinha, and
Yongchao Zhang, “PASSAT at future neutrino experiments: Hybrid beam-dump-helioscope facilities to probe
light axionlike particles,” Phys. Rev. D 104, 035037
(2021), arXiv:2101.08781 [hep-ph].
[21] H. Abramowicz et al., “Conceptual design report for the
LUXE experiment,” Eur. Phys. J. ST 230, 2445–2560
(2021), arXiv:2102.02032 [hep-ex].
[22] Jean-François Fortin, Huai-Ke Guo, Steven P. Harris,
Doojin Kim, Kuver Sinha, and Chen Sun, “Axions:
From magnetars and neutron star mergers to beam
dumps and BECs,” Int. J. Mod. Phys. D 30, 2130002
(2021), arXiv:2102.12503 [hep-ph].
[23] Kento Asai, Sho Iwamoto, Yasuhito Sakaki,
and
Daiki Ueda, “New physics searches at the ILC positron
and electron beam dumps,” JHEP 09, 183 (2021),
arXiv:2105.13768 [hep-ph].
[24] Nikita Blinov, Elizabeth Kowalczyk, and Margaret

Wynne, “Axion-like particle searches at DarkQuest,”
JHEP 02, 036 (2022), arXiv:2112.09814 [hep-ph].
[25] I. Larin et al. (PrimEx), “A New Measurement of the π 0
Radiative Decay Width,” Phys. Rev. Lett. 106, 162303
(2011), arXiv:1009.1681 [nucl-ex].
[26] S. N. Gninenko, N. V. Krasnikov, M. M. Kirsanov, and
D. V. Kirpichnikov, “Missing energy signature from invisible decays of dark photons at the CERN SPS,” Phys.
Rev. D 94, 095025 (2016), arXiv:1604.08432 [hep-ph].
[27] D. Banerjee et al. (NA64), “Search for invisible decays
of sub-GeV dark photons in missing-energy events at
the CERN SPS,” Phys. Rev. Lett. 118, 011802 (2017),
arXiv:1610.02988 [hep-ex].
[28] S. N. Gninenko, D. V. Kirpichnikov, M. M. Kirsanov,
and N. V. Krasnikov, “The exact tree-level calculation
of the dark photon production in high-energy electron
scattering at the CERN SPS,” Phys. Lett. B 782, 406–
411 (2018), arXiv:1712.05706 [hep-ph].
[29] S. N. Gninenko, D. V. Kirpichnikov, M. M. Kirsanov,
and N. V. Krasnikov, “Combined search for light dark
matter with electron and muon beams at NA64,” Phys.
Lett. B 796, 117–122 (2019), arXiv:1903.07899 [hep-ph].
[30] D. Banerjee et al., “Dark matter search in missing energy
events with NA64,” Phys. Rev. Lett. 123, 121801 (2019),
arXiv:1906.00176 [hep-ex].
[31] Yu. M. Andreev et al., “Improved exclusion limit for light
dark matter from e+e- annihilation in NA64,” Phys. Rev.
D 104, L091701 (2021), arXiv:2108.04195 [hep-ex].
[32] Yu. M. Andreev et al. (NA64), “Constraints on New
Physics in Electron g − 2 from a Search for Invisible Decays of a Scalar, Pseudoscalar, Vector, and Axial Vector,”
Phys. Rev. Lett. 126, 211802 (2021), arXiv:2102.01885
[hep-ex].
[33] Nikita Blinov, Gordan Krnjaic, and Douglas Tuckler, “Characterizing Dark Matter Signals with Missing
Momentum Experiments,” Phys. Rev. D 103, 035030
(2021), arXiv:2010.03577 [hep-ph].
[34] Tegan D. Beattie et al., “Construction and Performance
of the Barrel Electromagnetic Calorimeter for the GlueX
Experiment,” Nucl. Instrum. Meth. A 896, 24–42 (2018),
arXiv:1801.03088 [physics.ins-det].
[35] Andrey L. Pankratov et al., “Search for dark-matter axions beyond the quantum limit: The cosmological axion
Sarov haloscope proposal,” Phys. Rev. D 112, 035003
(2025), arXiv:2506.18595 [hep-ph].
[36] Krzysztof Jodlowski, “Dark axion portal at Z boson factories,” JHEP 08, 022 (2025), arXiv:2411.19196 [hep-ph].
[37] Kunio Kaneta, Hye-Sung Lee, and Seokhoon Yun, “Portal Connecting Dark Photons and Axions,” Phys. Rev.
Lett. 118, 101802 (2017), arXiv:1611.01466 [hep-ph].
[38] Kunio Kaneta, Hye-Sung Lee, and Seokhoon Yun,
“Dark photon relic dark matter production through the
dark axion portal,” Phys. Rev. D 95, 115032 (2017),
arXiv:1704.07542 [hep-ph].
[39] Patrick deNiverville, Hye-Sung Lee, and Min-Seok Seo,
“Implications of the dark axion portal for the muon
g−2 , B factories, fixed target neutrino experiments,
and beam dumps,” Phys. Rev. D 98, 115011 (2018),
arXiv:1806.00757 [hep-ph].
[40] Patrick deNiverville and Hye-Sung Lee, “Implications of
the dark axion portal for SHiP and FASER and the advantages of monophoton signals,” Phys. Rev. D 100,
055017 (2019), arXiv:1904.13061 [hep-ph].
[41] Alexey S. Zhevlakov, Dmitry V. Kirpichnikov, and

## PDF page 12

12
Valery E. Lyubovitskij, “Implication of the dark axion
portal for the EDM of fermions and dark matter probing with NA64e, NA64µ, LDMX, M3, and BaBar,” Phys.
Rev. D 106, 035018 (2022), arXiv:2204.09978 [hep-ph].
[42] Yu. M. Andreev et al. (NA64), “Searching for Light Dark
Matter and Dark Sectors with the NA64 experiment at
the CERN SPS,” (2025), arXiv:2505.14291 [hep-ex].
[43] Yu. M. Andreev et al. (NA64), “Search for Light Dark
Matter with NA64 at CERN,” Phys. Rev. Lett. 131,
161801 (2023), arXiv:2307.02404 [hep-ex].
[44] Jeremiah Mans (LDMX), “The LDMX Experiment,”
EPJ Web Conf. 142, 01020 (2017).
[45] Asher Berlin, Nikita Blinov, Gordan Krnjaic, Philip
Schuster, and Natalia Toro, “Dark Matter, Millicharges,
Axion and Scalar Particles, Gauge Bosons, and Other
New Physics with LDMX,” Phys. Rev. D 99, 075001
(2019), arXiv:1807.01730 [hep-ph].
[46] Torsten Åkesson et al. (LDMX), “Light Dark Matter eXperiment (LDMX),” (2018), arXiv:1808.05219 [hep-ex].
[47] Artur M. Ankowski, Alexander Friedland, Shirley Weishi
Li, Omar Moreno, Philip Schuster, Natalia Toro, and
Nhan Tran, “Lepton-Nucleus Cross Section Measurements for DUNE with the LDMX Detector,” Phys. Rev.
D 101, 053004 (2020), arXiv:1912.06140 [hep-ph].
[48] Philip Schuster, Natalia Toro, and Kevin Zhou, “Probing invisible vector meson decays with the NA64 and
LDMX experiments,” Phys. Rev. D 105, 035036 (2022),
arXiv:2112.02104 [hep-ph].
[49] Torsten Åkesson et al., “Current Status and Future
Prospects for the Light Dark Matter eXperiment,” in
2022 Snowmass Summer Study (2022) arXiv:2203.08192
[hep-ex].
[50] Torsten Akesson et al. (LDMX), “LDMX - The Light
Dark Matter eXperiment,” (2025), arXiv:2508.11833
[hep-ex].
[51] D. V. Kirpichnikov, Valery E. Lyubovitskij,
and
Alexey S. Zhevlakov, “Implication of hidden sub-GeV
bosons for the (g − 2)µ , 8 Be-4 He anomaly, proton charge
radius, EDM of fermions, and dark axion portal,” Phys.
Rev. D 102, 095024 (2020), arXiv:2002.07496 [hep-ph].
[52] D. V. Kirpichnikov, Valery E. Lyubovitskij,
and
Alexey S. Zhevlakov, “Constraints on CP-odd ALP couplings from EDM limits of fermions,” Particles 3, 719–728
(2020), arXiv:2004.13656 [hep-ph].
[53] Y. V. Stadnik, V. A. Dzuba, and V. V. Flambaum,
“Improved Limits on Axionlike-Particle-Mediated P , T
-Violating Interactions between Electrons and Nucleons
from Electric Dipole Moments of Atoms and Molecules,”
Phys. Rev. Lett. 120, 013202 (2018), arXiv:1708.00486
[physics.atom-ph].
[54] V. A. Dzuba, V. V. Flambaum, I. B. Samsonov, and
Y. V. Stadnik, “New constraints on axion-mediated P,Tviolating interaction from electric dipole moments of
diamagnetic atoms,” Phys. Rev. D 98, 035048 (2018),
arXiv:1805.01234 [physics.atom-ph].
[55] Victor Flambaum, Simon Lambert,
and Maxim
Pospelov, “Scalar-tensor theories with pseudoscalar couplings,” Phys. Rev. D 80, 105021 (2009), arXiv:0902.3217
[hep-ph].
[56] Jonathan L. Feng, Bartosz Fornal, Iftah Galon, Susan
Gardner, Jordan Smolinsky, Tim M. P. Tait, and Philip
Tanedo, “Protophobic Fifth-Force Interpretation of the
Observed Anomaly in 8 Be Nuclear Transitions,” Phys.
Rev. Lett. 117, 071803 (2016), arXiv:1604.07411 [hep-

ph].
[57] Avik Banerjee, Riccardo Catena, and Taylor R. Gray,
“Magnetic Dipole Portal Vector Dark Matter at FixedTargets,” (2025), arXiv:2511.23259 [hep-ph].
[58] Sergei N. Gninenko, Dmitry V. Kirpichnikov, Sergey
Kuleshov, Valery E. Lyubovitskij,
and Alexey S.
Zhevlakov, “Test of the vector portal with dark fermions
in the charge-exchange reactions in the NA64 experiment at CERN SPS,” Phys. Rev. D 109, 075021 (2024),
arXiv:2312.01703 [hep-ph].
[59] Alexey S. Zhevlakov, Dmitry V. Kirpichnikov, Sergei N.
Gninenko, Sergey Kuleshov, and Valery E. Lyubovitskij,
“Probing invisible vector meson decay mode with the
hadronic beam in the NA64 experiment at SPS CERN,”
Phys. Rev. D 108, 115005 (2023), arXiv:2309.09347 [hepph].
[60] A. S. Zhevlakov, V. E. Lyubovitskij, D. V. Kirpichnikov,
S. Kuleshov, and S. N. Gninenko, “Studying Dark Photon Models in Decays of Neutral Mesons,” Phys. Part.
Nucl. 56, 500–505 (2025).
[61] M. Bondi, A. Celentano, R. R. Dusaev, D. V. Kirpichnikov, M. M. Kirsanov, N. V. Krasnikov, L. Marsicano,
and D. Shchukin, “Fully Geant4 compatible package for
the simulation of Dark Matter in fixed target experiments,” Comput. Phys. Commun. 269, 108129 (2021),
arXiv:2101.12192 [hep-ph].
[62] Alexander Belyaev, Neil D. Christensen, and Alexander
Pukhov, “CalcHEP 3.4 for collider physics within and
beyond the Standard Model,” Comput. Phys. Commun.
184, 1729–1769 (2013), arXiv:1207.6082 [hep-ph].
[63] James D. Bjorken, Rouven Essig, Philip Schuster, and
Natalia Toro, “New Fixed-Target Experiments to Search
for Dark Gauge Forces,” Phys. Rev. D 80, 075018 (2009),
arXiv:0906.0580 [hep-ph].
[64] Yung-Su Tsai, “AXION BREMSSTRAHLUNG BY AN
ELECTRON BEAM,” Phys. Rev. D 34, 1326 (1986).
[65] Heath Bland O’Connell, B. C. Pearce, Anthony William
Thomas, and Anthony Gordon Williams, “ρ − ω mixing, vector meson dominance and the pion form-factor,”
Prog. Part. Nucl. Phys. 39, 201–252 (1997), arXiv:hepph/9501251.
[66] S. Navas et al. (Particle Data Group), “Review of particle
physics,” Phys. Rev. D 110, 030001 (2024).
[67] Vladyslav Shtabovenko, Rolf Mertig, and Frederik Orellana, “New Developments in FeynCalc 9.0,” Comput.
Phys. Commun. 207, 432–444 (2016), arXiv:1601.01167
[hep-ph].
[68] Wolfram Research, Inc., “Mathematica, Version 13.0.0,”
Champaign, IL, 2021.
[69] Xiaoyong Chu, Josef Pradler, and Lukas Semmelrock,
“Light dark states with electromagnetic form factors,”
Phys. Rev. D 99, 015040 (2019), arXiv:1811.04095 [hepph].
[70] Bernard Aubert et al. (BaBar), “A Search for Invisible
Decays of the Upsilon(1S),” Phys. Rev. Lett. 103, 251801
(2009), arXiv:0908.2840 [hep-ex].
[71] Iftah Galon, Enrique Kajamovitz, David Shih, Yotam
Soreq, and Shlomit Tarem, “Searching for muonic forces
with the ATLAS detector,” Phys. Rev. D 101, 011701
(2020), arXiv:1906.09272 [hep-ph].
[72] Georges Aad et al. (ATLAS), “Muon reconstruction performance of the
√ ATLAS detector in proton–proton collision data at s =13 TeV,” Eur. Phys. J. C 76, 292
(2016), arXiv:1603.05598 [hep-ex].

## PDF page 13

13
[73] Anson Hook, Gustavo Marques-Tavares, and Clayton Ristow, “Supernova constraints on an axionphoton-dark photon interaction,” JHEP 06, 167 (2021),
arXiv:2105.06476 [hep-ph].
[74] Juan Cortabitarte Gutiérrez, Bradley J. Kavanagh,
Núria Castelló-Mor, Francisco J. Casas, Jose M.
Diego, Enrique Martı́nez-González, and Rocı́o Vilar
Cortabitarte, “Cosmology and direct detection of the
Dark Axion Portal,” (2021), arXiv:2112.11387 [hep-ph].
[75] Paola Arias, Bastian Diaz Saez, and Joerg Jaeckel,
“Freezing-in the pure dark axion portal,” JCAP 06, 060
(2025), arXiv:2501.17234 [hep-ph].
[76] Zhaoyu Bai et al., “New physics searches with an optical dump at LUXE,” Phys. Rev. D 106, 115034 (2022),
arXiv:2107.13554 [hep-ph].
[77] Sergey Alekhin et al., “A facility to Search for Hidden
Particles at the CERN SPS: the SHiP physics case,”
Rept. Prog. Phys. 79, 124201 (2016), arXiv:1504.04855
[hep-ph].
[78] Jonathan L. Feng et al., “The Forward Physics Facility
at the High-Luminosity LHC,” (2022), arXiv:2203.05090
[hep-ex].
[79] Georges Aad et al. (ATLAS), “Search for displaced photons produced in exotic decays of the Higgs boson using
13 TeV pp collisions with the ATLAS detector,” Phys.
Rev. D 108, 032016 (2023), arXiv:2209.01029 [hep-ex].
[80] Noam Ness and Barry Cimring, “Exploring the Dark Axion Portal in the LUXE-NPOD Experiment,” (2025),
arXiv:2512.11975 [hep-ph].
[81] Krzysztof Jodlowski, “Probing some photon portals to
new physics at intensity frontier experiments,” Phys.
Rev. D 108, 115017 (2023), arXiv:2305.05710 [hep-ph].
[82] Paola Arias, Bastián Dı́az Sáez, Lucı́a Duarte, Joel
Jones-Pérez, Walter Rodriguez, and Danilo Zegarra
Herrera, “Probing displaced (dark)photons from low reheating freeze-in at the LHC,” JHEP 01, 135 (2026),
arXiv:2507.15930 [hep-ph].
[83] Patrick Deniverville, Hye-Sung Lee, and Young-Min
Lee, “New searches at reactor experiments based on the
dark axion portal,” Phys. Rev. D 103, 075006 (2021),
arXiv:2011.03276 [hep-ph].
[84] Valerie Domcke, Kai Schmitz, and Tevong You, “Cosmological Relaxation through the Dark Axion Portal,”
(2021), arXiv:2108.11295 [hep-ph].

[85] G. G. Raffelt, Stars as laboratories for fundamental
physics: The astrophysics of neutrinos, axions, and other
weakly interacting particles (1996).
[86] Sergei N. Gninenko, N. V. Krasnikov, Sergey Kuleshov,
Valery E. Lyubovitskij, P. Crivelli, D. V. Kirpichnikov,
L. Molina Bueno, Alexey S. Zhevlakov, H. Sieber, and
I. V. Voronchikhin, “Probing millicharged particles with
NA64µ and LDMX,” (2025), arXiv:2505.04295 [hep-ph].
[87] Thomas Gutsche, Astrid N. Hiller Blin, Sergey Kovalenko, Serguei Kuleshov, Valery E. Lyubovitskij,
Manuel J. Vicente Vacas, and Alexey Zhevlakov, “CPviolating decays of the pseudoscalars eta and eta’ and
their connection to the electric dipole moment of the neutron,” Phys. Rev. D 95, 036022 (2017), arXiv:1612.02276
[hep-ph].
[88] Alexey S. Zhevlakov, Thomas Gutsche, and Valery E.
Lyubovitskij, “Updated limits on the CP violating ηππ
and η ′ ππ couplings derived from the neutron EDM,”
Phys. Rev. D 99, 115004 (2019), arXiv:1904.08154 [hepph].
[89] Alexey S. Zhevlakov, Mikhail Gorchtein, Astrid N.
Hiller Blin, Thomas Gutsche, and Valery E. Lyubovitskij, “Bounds on rare decays of η and η ′ mesons from
the neutron EDM,” Phys. Rev. D 99, 031703 (2019),
arXiv:1812.00171 [hep-ph].
[90] Claudio Dib, Amand Faessler, Thomas Gutsche, Sergey
Kovalenko, Jan Kuckei, Valery E. Lyubovitskij, and
Kem Pumsa-ard, “The Neutron electric dipole formfactor in the perturbative chiral quark model,” J. Phys.
G 32, 547–564 (2006), arXiv:hep-ph/0601144.
[91] Amand Faessler, Thomas Gutsche, Sergey Kovalenko,
and Valery E. Lyubovitskij, “Hadronic electric dipole moments in R-parity violating supersymmetry,” Phys. Rev.
D 73, 114023 (2006), arXiv:hep-ph/0604026.
[92] Tanya S. Roussy et al., “An improved bound on the
electron’s electric dipole moment,” Science 381, adg4084
(2023), arXiv:2212.11841 [physics.atom-ph].
[93] G. W. Bennett et al. (Muon (g-2)), “An Improved Limit
on the Muon Electric Dipole Moment,” Phys. Rev. D 80,
052008 (2009), arXiv:0811.1207 [hep-ex].
[94] C. Abel et al., “Measurement of the Permanent Electric
Dipole Moment of the Neutron,” Phys. Rev. Lett. 124,
081803 (2020), arXiv:2001.11966 [hep-ex].
