Source: https://arxiv.org/abs/2505.22710v2
PDF sha256: eb7573ba9dfcbd1e4b636ea3abf6430ef9666b33e47c4f41de0847ec60f23ae3
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of asadi_2025_uv_freeze_in_cogenesis.pdf

Transcription of `asadi_2025_uv_freeze_in_cogenesis.pdf` in this directory, 62 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-62 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

MIT-CTP/5873

Genesis of Baryon and Dark Matter Asymmetries
through Ultraviolet Scattering Freeze-in

arXiv:2505.22710v2 [hep-ph] 3 Mar 2026

Pouya Asadi1 , Marianne Moore2,3 , David E. Morrissey4 , Michael Shamma4,5
pasadi@uoregon.edu, mamoore@mit.edu, dmorri@triumf.ca, mshamma@triumf.ca,
1 Institute for Fundamental Science and Department of Physics,

University of Oregon, Eugene, OR 97403, USA
2 Center for Theoretical Physics – a Leinweber Institute,

Massachusetts Institute of Technology, Cambridge, Massachusetts 02139, USA
3 Department of Physics, Harvard University, Cambridge, Massachusetts 02138, USA
4 TRIUMF, 4004 Wesbrook Mall, Vancouver, BC V6T 2A3, Canada
5 Department of Physics and Astronomy, University of California, Riverside, CA 92521, USA

March 5, 2026
Abstract
We introduce a new mechanism for the simultaneous generation of baryon and dark
matter asymmetries through ultraviolet-dominated freeze-in scatterings. The mechanism relies on heavy Majorana neutrinos that connect the visible Standard Model sector
to a dark sector through the neutrino portal. Following reheating of the visible sector
to a temperature well below the heavy neutrino masses, we show that 2-to-2 scattering
processes can populate the dark sector and generate both baryon and dark matter
asymmetries. In some parameter regions, the dominant source of baryon asymmetry
can be charge transfer from the dark sector, a process we call dark wash-in. We also
demonstrate that annihilation of the dark matter to massless states within the dark
sector can deplete the symmetric population without destroying the net baryon charge
to leave only an asymmetric dark matter abundance today. Depending on the specific
model parameters, the observed baryon and dark matter abundances can be attained
with heavy neutrino masses MN ≳ 1010 GeV, and dark matter masses in the range
0.1 GeV ≲ mχ ≲ 103 GeV if the dark matter relic abundance is mainly asymmetric
and even lower masses if it is symmetric.

1

## PDF page 2

Contents
1 Introduction

3

2 Particles, Interactions, and Processes
2.1 Overview of the Model . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
2.2 Cosmological Evolution and Roles . . . . . . . . . . . . . . . . . . . . . . . .
2.3 Overview of Transfer Reactions . . . . . . . . . . . . . . . . . . . . . . . . .
2.4 Overview of Asymmetry Generation . . . . . . . . . . . . . . . . . . . . . . .
2.5 Overview of Dark Sector Processes . . . . . . . . . . . . . . . . . . . . . . .

5
5
8
10
13
16

3 Reheating and Transfer to the Dark Sector
3.1 Populating the Dark Sector by Transfer . . . . . . . . . . . . . . . . . . . . .
3.2 Production of Heavy Neutrinos . . . . . . . . . . . . . . . . . . . . . . . . .
3.3 Comments on Uneven and Instantaneous Reheating . . . . . . . . . . . . . .

17
18
19
20

4 Asymmetry Creation in the Early Universe
4.1 Relations Between Particle and Charge Densities . . . . . . . . . . . . . . .
4.2 Boltzmann Equations for Asymmetries . . . . . . . . . . . . . . . . . . . . .
4.3 Charge Creation and Dark Wash-In . . . . . . . . . . . . . . . . . . . . . . .
4.4 Asymmetry Yields . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

22
22
24
27
32

5 Dark Sector Phenomenology
5.1 Light Degrees of Freedom . . . . . . . . . . . . . . . . . . . . . . . . . . . .
5.2 Dark Matter in a Dark Sink . . . . . . . . . . . . . . . . . . . . . . . . . . .
5.3 Other Potential Observables . . . . . . . . . . . . . . . . . . . . . . . . . . .

35
36
38
42

6 Conclusions

43

A Collision Term Calculations
A.1 Number Density . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
A.2 Energy Density . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

44
45
46

B Asymmetry Matrix Element Calculations

46

C Source and Wash-out Collision Term Calculations

48

D Transfer with Non-Instantaneous Reheating

50

2

## PDF page 3

1

Introduction

The origin of dark matter (DM) and the baryon asymmetry are two unresolved puzzles
in particle physics and cosmology that point towards new physics beyond the Standard
Model (SM). Each of these open problems has motivated numerous theoretical and experimental studies, see Refs. [1–6] and Refs. [7–13], respectively, for recent reviews on DM and
baryogenesis.
Intriguingly, the cosmological energy densities of dark matter and baryons are very similar, ρDM ≃ 5ρB [14, 15]. This similarity is highly surprising if the cosmic origins of the two
are unrelated, and is suggestive of a common source for both. Crucially, such a cogenesis
requires non-gravitational interactions between the SM and dark matter. As this is the only
hint of such interactions, theories that dynamically explain both the SM baryon asymmetry
and DM abundance are important targets for future experimental searches.
Numerous pathways exist for producing the DM abundance. Here, we study freezein [16–18], whereby the DM abundance is initially negligible following reheating and is produced through portal interactions with the SM bath that are too feeble to bring DM into
full equilibrium. While many freeze-in models focus on renormalizable portal interactions,
known as infrared (IR) freeze-in [18], in this work we focus on a non-renormalizable portal,
i.e. ultraviolet (UV) freeze-in [19–21]. In this type of model, the dark sector is primarily
populated near the reheat temperature TRH .
A more limited number of mechanisms have been found to explain the observed baryon
asymmetry, which is only possible if they break lepton or baryon number, violate C and CP,
and involve out-of-equilibrium processes [22]. For example, in leptogenesis heavy neutrinos
generate a lepton asymmetry, which is then converted to a baryon asymmetry by sphaleron
transitions [23–28]. Generically, leptogenesis models rely primarily on the decay of long-lived
heavy neutrinos to furnish the departure from equilibrium [29, 30], although see Ref. [31, 32]
for approaches based on scattering.
Connecting the DM abundance to the baryon asymmetry typically requires further structure. A promising framework to do so is asymmetric dark matter (ADM) [33–37]. In the
ADM paradigm, the DM abundance is set by an asymmetry between the DM particle and
its antiparticle. This allows a connection between the DM and baryon densities when the
asymmetry in one sector is related to that in the other, either from the cogenesis of both
asymmetries in a single step [38–45] or through the creation of an asymmetry in one sector
that is then shared with the other [46–53]. Asymmetric dark matter scenarios can be contrasted with models of baryogenesis via weakly interacting massive particles (WIMPs) [54–61]
where the baryon or lepton asymmetry is generated during symmetric WIMP freeze-out.1
1

There have been some attempts to relate the WIMPy baryogenesis paradigm to ADM. For example, in
Ref. [62] the DM abundance is set ultimately by a combination of freeze-out and an asymmetry.

3

## PDF page 4

In this work, we present a new mechanism for the creation of baryon and dark matter
asymmetries through freeze-in scattering processes. The model includes a neutrino portal [63] that connects the visible SM sector to a dark sector containing SM-singlet fermions
and a scalar. The heavy neutrinos in our model are assumed to be heavier than the SM
bath reheating temperature TRH . Transfer reactions between the two sectors mediated by
the heavy neutrinos populate the dark sector through UV freeze-in and generate charge
asymmetries in both sectors through 2 → 2 scatterings. The asymmetry in the visible sector
is partially reprocessed into the observed baryon asymmetry. The related asymmetry in the
dark sector impacts the final dark matter relic density.
Freeze-in is an essential component of scattering cogenesis, as it gives rise to the required
out-of-equilibrium Sakharov condition [64–68]. However, asymmetry creation by freeze-in is
strongly constrained by CPT and unitarity [69]. In particular, in scenarios with an exactly
conserved global charge, the leading charge asymmetry transfer between sectors vanishes [69,
70]. As a result, the parameter space that generates sufficient SM baryon asymmetry (at
next-to-leading order in the feeble portal coupling) also generates a high DM symmetric
number density (at leading-order), which is typically ruled out by a combination of the
overclosure constraint [14] and other astrophysical observations [71, 72].
Two main aspects of our model allow us to overcome the challenges outlined in Ref. [69].
First, our model includes a natural explicit breaking of the extended lepton number between
the two sectors. This allows for an enhanced charge creation relative to the class of scenarios
treated in Ref. [69]. Second, we postulate that our dark matter candidate is in contact
with a bath of light secluded dark particles that acts as a dark sink [73–75]; eventually
the symmetric abundance of DM freezes out into this dark sink, reducing its population
enormously and leaving only an asymmetric DM abundance today. The dark sink redshifts
like radiation and is not currently constrained by cosmological tests of new relativistic degrees
of freedom. Thanks to these two features ((i) the breaking of the extended lepton number
and (ii) the dark sink), our viable dark matter mass range extends beyond the standard
ADM models to DM masses 1 keV ≲ mχ ≲ 103 GeV, while its abundance can be dominated
by the asymmetry for mχ ≳ 0.1 GeV.2
The higher end of this mass range is achieved in the strong dark wash-out limit. Wash-out
terms play a key role in our setup. Existing constraints on the active neutrino masses push
us to a parameter region where the dark lepton number source terms are more efficient than
those in the visible sector. Some of the dark asymmetry from these sources is transferred
to the visible sector through wash-out processes. In leptogenesis, the concept of wash-out
terms reprocessing a “primordial charge asymmetry” into a SM B − L asymmetry is known
as wash-in [76–78]. In our case, the primordial asymmetry lies in the dark sector charge
2

See Refs. [40, 51] for other ADM models viable over a wide range of DM masses.

4

## PDF page 5

density, so we refer to this mechanism as dark wash-in.
Our model is a complete UV freeze-in cogenesis setup to produce asymmetric dark matter.
The underlying asymmetry creation mechanism is closely related to that of Ref. [31], while
other more recent studies have followed somewhat different approaches [79–85], many using
new elements such as the ARS mechanism [86] or resonant leptogenesis [30]. In Ref. [79] the
DM abundance can be asymmetric, while in Refs. [80–85] it is dominantly symmetric. Our
setup also shares different moving pieces with existing models of baryogenesis that do not
attempt to explain the DM abundance [32, 87, 88].
The rest of the paper is organized as follows. In Sec. 2 we introduce our model and give an
overview of its different moving pieces, including its cosmological evolution and the relevant
processes for generating an asymmetry. In Sec. 3 we provide more details on the cosmic
evolution of our setup and populating the dark sector. Details of the asymmetry generation
are provided in Sec. 4, where we include the final form of the Boltzmann equations and discuss
the significance of the wash-out terms. Finally, in Sec. 5 we discuss further dynamics in the
dark sector and calculate the viable DM mass range. We conclude in Sec. 6. In App. A we
provide further details on the collision terms appearing in the Boltzmann equations. Further
details on the calculation of asymmetric matrix elements can be found in App. B. In App. C
we review the steps taken to simplify the Boltzmann equations. In App. D we compute
energy transfer from the visible sector to the dark sector during non-instantaneous reheating
after inflation.

2

Particles, Interactions, and Processes

In this section we introduce a simple model that can realize asymmetric DM and leptogenesis
through scattering processes during UV freeze-in. It consists of the SM together with heavy
Majorana neutrinos that connect to a dark sector containing a Dirac fermion, a complex
scalar, and a massless Weyl fermion. We also give an overview of the roles of these states
in the cosmological production of the baryon asymmetry and dark matter density, and we
calculate the relevant interaction cross sections for the corresponding processes. These results
will be applied in the following sections to compute the detailed cosmological evolution of
this theory.

2.1

Overview of the Model

In addition to the SM, we consider new Majorana neutrinos Na together with a dark sector
consisting of a Dirac fermion with chiral components χ and χc , a complex scalar ϕ, and a
chiral fermion η. The interaction Lagrangian for these new fields (in 2-component notation)

5

## PDF page 6

•

U(1)Y

U(1)D

U(1)L

U(1)Lx

H
ℓ
ϕ
χ
χc
N
η

+1/2
−1/2
0
0
0
0
0

0
0
−1/2
+1/2
−1/2
0
−1

0
+1
0
0
0
−1
0

0
0
+1/2
+1/2
−1/2
0
0

Table 1: The field content and (approximate) symmetries of the Lagrangian from Eq. (2) in our
UV freeze-in DM setup. We define the symmetry U(1)D , similar to SM hypercharge, in the dark
sector. The extended lepton number, U(1)L+Lx , is explicitly broken by the Majorana mass of N
particles. These particles act as a (neutrino) portal between SM and the dark sector. The χ field
is the lightest particle with fractional U(1)D charge; hence it is stable and acts as the DM in this
scenario.

is
L = LSM + Lasym + Lsink ,

(1)

1
−Lasym ⊃ yia H ·ℓi Na + λa ϕ χ Na + mχ χχc + m2ϕ ϕ† ϕ + Ma Na Na + h.c. ,
2

(2)

−Lsink = yχ ϕ∗ χ η + h.c. .

(3)

with

and

Here, ℓi denotes the lepton doublets of the SM in the standard lepton flavor-diagonal basis,
H is the SM Higgs field with its SU(2)L indices contracted asymmetrically with ℓ, and i and
a refer to flavors of leptons and heavy neutrinos, respectively. The Yukawa couplings yia
and λa are generic complex matrices. For simplicity, we make the non-essential assumption
that the Na couple equally to all SM leptons, yia = ya , i = 1, 2, 3. We also consider two
generations of Na in the spectrum (a = 1, 2) with M1 < M2 .
In the limit of vanishing Majorana masses Ma → 0, the Lagrangian has three independent
Abelian symmetries. They can be chosen to be: (i) the usual SM hypercharge Y , (ii) a dark
hypercharge D, and (iii) an extended lepton number L + Lx , where Lx is an effective lepton
number in the dark sector. The charges of the various fields under these symmetries are
given in Tab. 1. Adding Majorana masses for Na breaks L + Lx explicitly and softly. Taking
the opposite limit of Ma → ∞, L and Lx become approximate independent symmetries
6

## PDF page 7

in the low-energy effective theory up to explicit breaking by operators suppressed by Ma .
We note further that the interactions of Eq. (2) are the most general ones possible at the
renormalizable level up to a |ϕ|4 quartic self-coupling and a |ϕ|2 |H|2 Higgs portal coupling.
A quartic self-coupling for ϕ would not significantly affect the dynamics of the mechanism.
However, a Higgs portal coupling connecting the dark and visible sectors could lead to the
thermalization of the sectors with each other at late times. We assume this interaction to
be negligibly small for our analysis, but we comment on the impact of larger values later on.
Creation of baryon or lepton asymmetries requires new sources of CP violation. Here,
this can arise if some of the couplings in Eq. (2) are complex. Without loss of generality,
we take the Ma to be real, positive, and diagonal. After field redefinitions that preserve this
convention, there remain (nN − 1) physical phases in each of y and λ, and thus our choice of
nN = 2 is the minimal possibility consistent with new CP violation. This remaining freedom
can be used to make y2 and λ2 real and positive, such that the two new physical phases come
solely from y1 and λ1 .
In the dark sector, the lighter of χ and ϕ is stable on account of its smallest fractional
U(1)D charge. To be concrete, we take mχ < mϕ , meaning that χ (combined with its
vector-like partner χc ) is a stable Dirac fermion dark matter candidate. The massless Weyl
fermion η acts as a dark sink [74, 75], providing an annihilation channel for χ as well as a
decay channel for ϕ through ϕ → χη. This interaction also enables rapid self-thermalization
within the dark sector.3
This scenario is an example of a neutrino portal dark sector. Such portals offer the
possibility of explaining (at least part of) the SM neutrino masses through the first term of
Eq. (2). For the universal flavor structure yia = ya , the neutrino mass matrix has two heavy
mostly-singlet states with masses near M1 and M2 , two massless active neutrinos, and one
massive active neutrino with Majorana mass in the seesaw limit of Ma ≫ mZ , where mZ
represents the weak scale, equal to
∣
∣
3 ∣∣ y12 v 2 y22 v 2 ∣∣
+
,
(4)
∆mν = ∣
2 M1
M2 ∣
where v ≃ 246 GeV is the Higgs vacuum expectation value. This massive active neutrino is
an equal linear combination of all three flavor eigenstates. In this work we do not attempt
to explain the full pattern of observed neutrino masses and mixings. However, we do check
that the contribution above to the sum of the active neutrino masses is not too large by
3

If the U(1)D dark hypercharge were a global symmetry, we would expect quantum gravity effects to
break it [89], which could destabilize χ. This could be avoided by weakly gauging the U(1)D , which would
also require introducing a vector-like partner η c for anomaly cancellation. Including such a state would not
significantly alter our conclusions provided the η-η c Dirac mass is very small.

7

## PDF page 8

tot ̸= 0
YSM

YB−L = YLx = YΣχ = 0
MN

T

T = TRH

Y∆χ = YLx

YB−L ̸= 0 YLx ̸= 0
YLx ≪ YΣχ

YB = (28/79)YB−L

T ≲ TRH

mφ
χ

χ

ℓ

χ

TEW
η
ℓ

φ

MN
H

mχ/10

Sphl.

B̄

φ
η

φ

χ̄

η̄

Figure 1: Schematic of the cosmological history and the evolution of different abundances YQ in
our setup. Temperature increases from right to left and time runs from left to right. The universe
reheats to temperature TRH below the heavy neutrino masses and only populates the SM. The dark
sector is immediately populated through UV freeze-in. The asymmetries in the two sectors are
dominantly generated at this stage as well. At lower temperatures, the ϕ field decays to the DM
χ, which subsequently freezes-out into the dark bath η. If the frozen-out symmetric abundance of
χ (denoted by YΣχ ) is not too far from the asymmetric yield Y∆χ , the freeze-out process produces
mostly asymmetric dark matter (Y∆χ ∼ YΣχ ). The generated SM lepton asymmetry is partially
converted into a baryon asymmetry by SM sphalerons throughout this timeline; the conversion
stops after the electroweak symmetry breaking.

imposing the constraint
∆mν < 0.07 eV ,
which is motivated by the cosmological bound

2.2

∑

(5)

mν < 0.072 eV [90].

Cosmological Evolution and Roles

Having introduced the fields and interactions above, our next step is to give an overview of
the cosmological timeline over which these fields can generate the baryon asymmetry and
dark matter density. In the visible sector, some of the lepton asymmetry is converted to
a baryon asymmetry by electroweak sphaleron transitions. In the dark sector, the heavy ϕ
scalars decay to the lighter χ fermions, which subsequently annihilate efficiently to massless
η fermions. This leaves a relic density of χ as dark matter that may be dominated by the
dark sector asymmetry. Detailed calculations of the cosmological evolution of all the relevant
species densities will be given in upcoming sections.
The cosmological history in our scenario is illustrated in Fig. 1. Here YQ denotes the yield
of a quantum charge Q and Y∆χ,Σχ = Yχ ∓ Yχ̄ are the asymmetric and symmetric yields. Key
stages of this evolution are:
1. Primordial inflation reheats the visible sector to a temperature T = TRH ≪ Ma as well
as TRH ≫ mϕ , mχ , mZ . We assume further that this reheating populates exclusively
8

## PDF page 9

the visible sector with no significant densities of Na or dark states χ, ϕ, or η created
at this point.
2. Immediately after reheating, scattering processes initiated by ℓ and H within the visible
sector begin to populate the dark sector. Since these processes are all mediated by the
heavy Na with masses Ma ≫ TRH , the direct production of Na is negligible and transfer
to the dark sector is dominated by 2 → 2 reactions at temperatures close to reheating,
corresponding to UV freeze-in production [21]. As this occurs, scattering within the
dark sector through η quickly equilibrates this sector to a dark temperature Tx < T .
3. With C and CP violation together with L number violation from the massive Majorana
neutrino masses Ma , 2 → 2 scattering processes between and within the visible and
dark sectors generate B − L and Lx charge asymmetries in each sector. Wash-out
processes also deplete the asymmetries and transfer them from one sector to the other.
Just like the reactions populating the dark sector, these asymmetry transfer processes
are dominated by temperatures near reheating and tend to freeze out soon after. Once
the transfer reactions freeze out, the two sectors dilute and cool independently with
their respective asymmetries remaining fixed.
4. As the dark temperature falls below Tx ∼ mϕ , the asymmetry in ϕ is transferred to
the one in χ by decays ϕ → χη. When Tx falls below mχ , the massive dark fermions
undergo freeze-out through χχ̄ → η η̄, depleting their symmetric density but leaving
the asymmetry unchanged. The massless η fermion thus serves both to self-thermalize
the dark sector and to absorb its symmetric abundance, i.e. acting as a dark sink in
the sense of Refs. [74, 75].
5. In the visible sector, a fraction of the visible B − L asymmetry is converted into a
baryon asymmetry by electroweak sphaleron transitions throughout this timeline [91].
This conversion stops shortly after electroweak symmetry breaking [92].
Our scenario has all the ingredients required to generate the DM abundance and the SM
baryon asymmetry. Specifically, the scenario realizes the well-known Sakharov conditions
for creating the matter asymmetry [8, 22]. Violation of lepton number L is provided by the
Majorana masses Ma of the heavy neutrinos, while electroweak sphaleron transitions affect
the combination B + L. Breaking of C and CP are provided by the new chiral interactions
together with the weak phases introduced by the new couplings of Eq. (2). And finally,
a departure from equilibrium arises if the visible and dark sectors do not fully equilibrate
with each other. In the sections to come, we will show explicitly how these ingredients can
combine to produce asymmetries in visible baryon charge and dark matter number.

9

## PDF page 10

2.3

Overview of Transfer Reactions

The first stage of cosmological evolution in our scenario after primordial reheating to a
visible temperature TRH is dictated by transfer reactions. We define these to be the reactions
mediated by the heavy Majorana neutrinos Na . At leading order in the relevant couplings,
transfer reactions share particle number and energy between the visible and dark sectors.
Going beyond leading order, a subset of these reactions can also generate asymmetries within
and between the two sectors. We outline our calculation of transfer reaction rates in this
subsection.
It is useful to define some quantities of interest and introduce a simplified notation. We
write the matrix element for a process going from the initial state α to the final state β as
M(α → β) ≡ Mαβ .

(6)

The matrix elements for a process and its charge conjugate can be merged to define symmetric
and asymmetric squared matrix elements:
†

|ΣMαβ |2 ≡ |Mαβ |2 + |Mαβ † |2 ,

†
|∆Mαβ |2 ≡ |Mαβ |2 − |Mαβ † |2 .

(7)
(8)

In these and other squared matrix elements, we implicitly sum over all initial and final
internal degrees of freedom. We also write
nΣX ≡ nX + nX † ,

n∆X ≡ nX − nX † ,

(9)
(10)

where X denotes any particle in the spectrum and X † its antiparticle. The evolution of these
symmetric and asymmetric abundances depends on the symmetric and asymmetric matrix
elements.
The transfer reactions relevant to our scenario are all 2 → 2 processes and listed in Tab. 2.
We divide these processes into two broad categories. Those in the upper section of the table
contribute to generating particle asymmetries. In contrast, reactions in the lower section
of the table do not create asymmetries at leading non-trivial order, but they can have an
important impact on particle asymmetries by washing out asymmetries that have already
been created. Further details on asymmetry creation and wash-out will be discussed below.
Since transfer reactions are mediated by the exchange of heavy Majorana neutrinos and
we focus on temperatures well below their masses, T ≪ Ma , it is a good approximation to
expand their corresponding matrix elements in powers of 1/Ma . The expansion begins at the

10

## PDF page 11

Reaction

∆L

∆Lx

∆(L + Lx )

Asymmetry?

ℓi H
ℓi H
ℓi H
χϕ

→
→
→
→

ℓ†j H †
χ† ϕ†
χϕ
χ† ϕ†

−2
−1
−1
0

0
−1
+1
−2

−2
−2
0
−2

Y
Y
Y
Y

ℓi ℓj
ℓi χ
ℓi χ†
ℓi ϕ
ℓi ϕ†
χχ

→
→
→
→
→
→

H †H †
H † ϕ†
H †ϕ
H † χ†
H †χ
ϕ† ϕ†

−2
−1
−1
−1
−1
0

0
−1
+1
−1
+1
−2

−2
−2
0
−2
0
−2

N
N
N
N
N
N

Table 2: List of all relevant 2 → 2 transfer reactions in our scenario, up to time reversal and
charge conjugation, as well as the changes in charges they induce. They are separated according to
whether (Y) or not (N) they give rise to non-zero asymmetric matrix elements at leading non-trivial
order.

linear order, and each term is accompanied by one or more positive powers of energy E. To
compute collision terms for the evolution of number or energy densities, these matrix elements
are then integrated over the final and initial state phase spaces weighted by the appropriate
quantum distribution functions and statistics factors. The appearance of positive powers of
energies implies that the support for these integrals is pushed to regions with E/T ≳ O(few)
where the quantum distributions are numerically close to Maxwell-Boltzmann (MB) [93].
Motivated by this, we make the simplifying approximation of evaluating all transfer reaction
collision terms using the MB approximation in this work.
Within the MB approximation, it is convenient to define for each process of the form
1 + 2 → 3 + 4 a Lorentz invariant scattering kernel :
∫
∫
12
2
W34 (s) ≡ S dΠ3 dΠ4 (2π)4 δ (4) (p1 + p2 − p3 − p4 )| M12
(11)
34 | ,
where s = (p1 + p2 )2 is the Mandelstam variable, dΠi = d3 pi /[(2π)3 2Ei ] are phase space
measures, S is the usual symmetry factor for identical initial or final states, and the squared
matrix element is implicitly summed over all initial and final internal degrees of freedom.
A scattering kernel is related to the scattering cross section of the corresponding process
according to W = 4 E1 E2 g1 g2 σv, where gi is the number of internal degrees of freedom of
particle i and v is the relative (Møller) velocity of the incoming particles [94, 95].
Given a scattering kernel for a reaction, its contribution to the collision term for the

11

## PDF page 12

evolution of an observable O that is independent of the final-state phase space in the MB
approximation is
∫
∫
12
12
[CO ]34 = dΠ1 dΠ2 W34
(s) f1 f2 δO ,
(12)
where fi are the MB distribution functions for the initial states and δO is the change in
the observable in the reaction. In particular, for number density of a species, δO is the net
change in the species particle number per reaction. The full collision term is the sum of
contributions from all relevant reactions. Further details on evaluating collision terms are
collected in App. A.
The expansion of matrix elements in powers of 1/Ma discussed above carries through to
the scattering kernels for symmetric and asymmetric squared matrix elements. By Lorentz
invariance, the positive powers of energy appearing in matrix elements must end up as
positive powers of the Mandelstam variable s. This allows us to write
†

ΣWβα (s) ≡ Wβα (s) + Wβα† (s) ≡ [S1 ]αβ × s + [S2 ]αβ × s2 + O(s3 ) ,
†

∆Wβα (s) ≡ Wβα (s) − Wβα† (s) ≡ [D1 ]αβ × s + [D2 ]αβ × s2 + O(s3 ) .

(13)
(14)

The coefficients [Si ]αβ and [Di ]αβ are independent of s. As demonstrated in Ref. [21] and
generalized in App. A, expanding this way allows for a simple connection between these
coefficients and the collision terms that control the cosmological evolution of number and
energy densities.
Turning now to explicit calculations in our theory, we collect in Tab. 3 the tree-level
symmetric coefficients [S1 ] and [S2 ] for all relevant transfer reactions.4 This is a complete set
of symmetric coefficients since by definition the symmetric matrix element for the process
α → β is equal to that for α† → β † , while CPT implies equality between those for α → β and
β † → α† . Some of the [S1 ] coefficients in Tab. 3 vanish, which can be understood in terms of
the charge L + Lx . This charge is only broken by the Majorana masses Ma , which act as a
spurion. Complexifying this mass and counting its insertions show that [S1 ] = 0 for reactions
that preserve L + Lx . In contrast to the symmetric matrix elements, all asymmetric matrix
elements vanish at tree-level and only emerge at loop order. These will be investigated in
detail below.
The expression for ℓi ℓj → H † H † includes a symmetry factor for the initial state appropriate for i = j.
Later on we will sum these terms freely over all lepton flavors i and j. This sum double counts when i ̸= j
but is compensated for by the extra factor of 1/2 included in the table.
4

12

## PDF page 13

Process
ℓ†j H †

ℓi H

→

ℓi H

→

χ† ϕ†

ℓi H

→

χϕ

χϕ →

χ† ϕ†

ℓi χ →

H † ϕ†

ℓi ℓj

ℓi χ†

→
→

ℓi ϕ →

ℓi ϕ†

→

χχ

→

H †H †
H †ϕ
H † χ†
H †χ
ϕ† ϕ†

4π[S1 ]
∑
2
6| a yia Ma−1 yja |
∑
2
| a λa Ma−1 yia |

4π[S2 ]
∑ ∗ −1 ∗ ]
−3
4 Re
a yia Ma yja
b yib Mb yjb
[∑
]
∑
−1 ∗
−3
∗
2 Re
λ
M
y
λ
M
y
a
ia
a
ib
b
a
b b
∑ ∗ −2 2
| a λa Ma yia |
[∑ 2 −3 ∑ ∗2 −1 ]
(4/3) Re
a λa Ma
b λb Mb
[∑
]
∑
−1 ∗
−3
∗
3 Re
y
M
y
y
M
y
ia
ja
a
ib
jb
b
a
b
[∑
∑ ∗ −1 ∗ ]
−3
−2 Re
b λb Mb yib
a λa Ma yia
∑ ∗ −2 2
(1/3)| a λa Ma yia |
[∑
∑ ∗ −1 ∗ ]
−3
(−2/3) Re
λ
M
y
a
ia
a
a
b λb Mb yib
∑ ∗ −2 2
| a λa Ma yia |
[∑ 2 −3 ∑ ∗2 −1 ]
− Re
b λb Mb
a λa Ma
[∑

0
∑ 2 −1 2
2| a λa Ma |
∑
3| a yia Ma−1 yja |2
∑
2
2| a λa Ma−1 yia |
0
∑
2
| a λa Ma−1 yia |
0
∑ 2 −1 2
| a λa Ma |

Table 3: Coefficients [S1 ] and [S2 ] for symmetric scattering kernels defined in Eq. (13) for all
relevant transfer reactions in our scenario. They are the first two terms in an expansion in powers
of the Mandelstam variable s.

2.4

Overview of Asymmetry Generation

A subset of the transfer reactions listed in Tab. 2 have a non-zero asymmetric squared matrix
element |∆Mαβ |2 , a necessary ingredient for sourcing net charges in the early universe. In this
section we identify the dominant sources of such asymmetries and compute their asymmetric
matrix elements at leading non-trivial order.
Physical CP violation requires interference involving two types of phases:
• Weak phase: a phase that changes sign between a process and its conjugate. These
phases are provided by the couplings in the Lagrangian [65, 67].
• Strong phase: a phase that does not change sign between a process and its conjugate.
These arise in the present context from intermediate virtual particles going on shell in
loops [96].
To demonstrate this explicitly, let us decompose the matrix element for a process α → β in
terms of independent Feynman diagrams as
Mαβ =

∑∑
n

†

Mαβ † ≡

ci n Pi n ,

in

∑∑
n

c∗in Pin ,

(15)

in

where n ≥ 0 counts the loop order, in runs over all contributions at loop order n, cin contains
all the couplings appearing in the corresponding diagram and is conjugated in the conjugate
13

## PDF page 14

process, and Pin denotes the rest of the amplitude and is identical for a process and its
conjugate. It follows that the asymmetric squared matrix element of Eq. (8) is given by
|∆Mαβ |2 = −4

∑

Im(Pi∗0 Pi1 ) Im(c∗i0 ci1 ) + . . . ,

(16)

i0 ,i1

where the omitted terms are of higher order in the loop expansion. This expression shows
why a non-zero asymmetric squared matrix element is contingent on having both weak
phases (from ci ) as well as strong phases (from Pj ). In our scenario, weak phases come
from the non-trivial phases in the Yukawa couplings yia and λa . Strong phases arise from
the imaginary parts of loop amplitudes generated by intermediate particles going on shell.
Among the four processes listed in Tab. 2, the asymmetries in ℓi H → ℓ†j H † and χϕ → χ† ϕ†
are nearly identical in terms of the amplitude topologies by which they are generated. Asymmetries in both processes arise from the interference between tree-level contributions from
s- and u-channel amplitudes with one-loop diagrams with s-channel massive neutrinos Na
receiving propagator corrections from loops of χϕ (for ℓi H → ℓ†j H † ) or ℓk H (for χϕ → χ† ϕ† )
and Majorana mass insertions on one or the other side of the loop. These topologies are
illustrated in Fig. 2. In contrast, for ℓi H → χ† ϕ† and ℓi H → χϕ, there is only an s-channel
diagram at tree level, with the leading asymmetry arising from the interference between this
diagram and loop diagrams with an s-channel Majorana neutrino and propagator or vertex
loops. These are also shown in Fig. 2. We note that one-loop diagrams with a Majorana
neutrino in the t-channel do not generate a strong phase and therefore do not contribute
to asymmetries at leading order. More details about calculating the corresponding matrix
elements are provided in App. B.
The final results of our calculations can be expressed in terms of the expansion coefficients
for asymmetric scattering kernels defined in Eq. (14). We find [D1 ] = 0 for all processes,
while for [D2 ] specializing to identical couplings yia = ya for all ng = 3 SM lepton generations
we obtain
(
)
∑ y ∗ 2 Ma yb λb Mb yc λ∗
3
a
c
[D2 ]ℓℓi†H
=
Im
,
(17)
†
2
2
2
32π 2
M
M
M
jH
a
c
b
a,b,c
(
)
∑ y ∗ λ∗ Mb y ∗ λc λ2 Md 3ng ∑ y 2 Ma y ∗ λ∗ Mb y ∗ λc
1
c
a
c
b b
d
b b
[D2 ]ℓχi†Hϕ† =
Im
+
, (18)
2
2
2 M2
2
2
32π 2
M
M
2
M
M
M
c
a
c
b
d
b
b,c,d
a,b,c
(
)
2
∑ yb λb Mb yc λ∗ λ∗ Md 3ng ∑ y 2 Ma y ∗ λ∗ Mb y ∗ λc
1
ℓi H
c d
a
c
b b
[D2 ]χϕ =
Im
+
, (19)
2
2
2
2
32π 2
M
M
M
2
M
Mb2 Mc2
c
a
b
d
a,b,c
b,c,d
(
)
∗
∗2
∑
n
λ
λ
M
y
λ
M
y
g
b b b c c d
d
[D2 ]χϕ
=
Im
.
(20)
2
2
χ † ϕ†
2
16π 2
M
M
M
c
b
d
b,c,d
14

## PDF page 15

Nc

Nc

Na

Nc

Nb

Na

Nb

Nb

Na

Na

Nb

Figure 2: Diagrams contributing to asymmetric squared matrix elements at leading non-trivial
order. The tree diagrams in the top left (middle and right) apply to reactions that conserve (violate)
L+Lx such as ℓi H → χϕ (ℓi H → χ† ϕ† ) and have an even (odd) number of Majorana neutrino mass
insertions. The u-channel tree-level diagram only arises for ℓi H → ℓ†j H † , χϕ → χ† ϕ† , and their
conjugates. The loop diagrams in the left (right) column apply to processes that conserve (violate)
L + Lx and involve two (one) Majorana mass insertion(s).

These relations satisfy a number of consistency conditions. From Sec. 2.1 we know that
to obtain physical weak phases we need at least two flavors of Majorana neutrinos with
different masses. Here, we see that each term within the parentheses in the expressions
above is manifestly real when there is only a single heavy neutrino flavor. A second check
is that these relations are symmetric under the interchange of λa ↔ ya and swapping visible
and hidden sector particles once lepton flavors and SU(2)L factors are taken into account.
A more complicated condition on the asymmetric coefficients is implied by CPT and
unitarity. Together, these require that for any initial state α [64–69],
∑

∆Wβα (s) = 0 ,

(21)

β

where the sum runs over all possible final states.5 This condition is fulfilled by the asymmetry
5

This relation holds at finite temperature in the MB approximation. There is a related generalization
when full quantum statistics is included [64, 65, 69].

15

## PDF page 16

coefficients collected in Eqs. (17)–(20). Specifically, it is straightforward to check that
0 =

∑
iH
[D2 ]ℓℓi†H
+ [D2 ]ℓχi†Hϕ† + [D2 ]ℓχϕ
,
H†

(22)

j

j

0 = [D2 ]χϕ
+
χ † ϕ†

∑

+
[D2 ]χϕ
ℓ† H †

∑

j

j

[D2 ]χϕ
ℓj H ,

(23)

j
ℓ H

ℓ H

j
where in the second relation we have used [D2 ]χϕ
= [D2 ]χj† ϕ† and [D2 ]χϕ
ℓj H = −[D2 ]χϕ .
ℓ† H †
j

2.5

Overview of Dark Sector Processes

The second class of new processes in our scenario are reactions entirely within the dark sector
through the interactions of Eq. (3). In contrast to transfer reactions, these are mediated
primarily by the light η fermion and thus remain active down to low temperatures. Dark
sector processes play an important role in determining the ultimate contribution of the dark
sector to the cosmological abundance of dark matter.
At high dark temperatures, Tx ≫ mϕ , mχ , the main role of dark sector reactions is to
maintain equilibrium among the χ, ϕ, and η states. Indeed, as long as the dimensionless
coupling yχ of Eq. (3) is not much smaller than unity, energy transferred from the visible
sector to the dark sector will quickly be thermalized within the dark sector to a temperature Tx < T . We consider yχ ∼ 1 to assume effectively instantaneous dark thermalization
throughout our analysis, but will comment further on the size of yχ in Sec. 5.
When Tx falls to near or below mϕ,χ , it is convenient to change from the 2-component
fermion formulation we have been using to a 4-component one. We define (in an abuse of
notation)
(
χ=

χ
χc †

)

(
,

η=

η
0

)
.

(24)

In this notation, the coupling of Eq. (3) translates into
−Lsink = yχ ϕ∗ χc PL η + h.c. .

(25)

The physical dark states consist of a massive complex scalar ϕ, a lighter Dirac fermion χ,
and a massless Weyl fermion η. In our study we assume mϕ > mχ , although the opposite
mass ordering would yield a similar phenomenology.
As the dark temperature falls below Tx ∼ mϕ , the decay ϕ → χη dominates over the
inverse decay and the density of ϕ is depopulated. Crucially to our scenario, these decays
preserve dark sector lepton number Lx (as well as L + Lx ); they only transfer any net charge
16

## PDF page 17

from the ϕ population to one in χ. The decay rate is
[
(
)2 ]2
yχ2
mχ
mϕ 1 −
.
Γ(ϕ → χη) =
16π
mϕ

(26)

This is much larger than Hubble when Tx ∼ mϕ for all the parameter values considered in
this work.
Evolving further to Tx ∼ mχ , the interactions of Eq. (3) also provide an annihilation
channel χχ̄ → η η̄. This reaction depletes the symmetric density of χ, transferring it to the
massless η fermions which act as a dark sink in the sense of Refs. [74, 75]. However, since
this reaction preserves the charge Lx it does not alter the asymmetry in χ. The scattering
kernel for the reaction is


)2
(
) (
2
2
2
2
4
2(m − mχ )
mϕ − mχ
yχ
1+A
1 
1 − √ ϕ
+
,
(27)
Wηχη̄χ̄ (s) =
ln
2
2
8π
1−A
mϕ − mχ + s/2 1 − A2
s(s − 4m2 )
χ

/
√
2
where 2A = s(s − 4mχ ) (m2ϕ −m2χ +s/2). The corresponding cross section at low velocities
v in the center-of-mass frame is
[
]
yχ4
m2χ
2
σv =
1
+
O(v
)
32π (m2ϕ + m2χ )2
)
(
(
) ( yχ )4 GeV 2
1
−21
3
.
≃ 7.2 × 10 cm /s ×
0.5
mχ
[(mϕ /mχ )2 + 1]2

(28)

This leading term corresponds to the s-wave in a multipole expansion and is unsuppressed
at the low velocities relevant for χ freeze-out. If this cross section is large enough, the relic
density of χ can be dominated by the asymmetry [97,98], corresponding to asymmetric dark
matter [33, 35–37].

3

Reheating and Transfer to the Dark Sector

Having presented an overview of our scenario, we turn next to investigating its cosmological
evolution. As described in Sec. 2, our starting point is reheating after primordial inflation.
We assume that this reheating populates the visible sector nearly exclusively, and produces
only negligible abundances of the dark sector and heavy Majorana states. In this section
we compute the rate of energy transfer to the dark sector following reheating of the visible
sector. This lays the foundation for our upcoming asymmetry calculations, which we defer
to the next section. A necessary condition for asymmetry generation in the scenario is
17

## PDF page 18

Tx < T ; this imposes constraints on the relative size of TRH and Ma . We also show that for
TRH ≪ Ma the direct production of heavy Majorana neutrinos after inflation is small enough
to be neglected. Finally, we comment on the plausibility of the assumptions we make about
primordial reheating.

3.1

Populating the Dark Sector by Transfer

Starting from a visible sector at TRH and an empty dark sector, transfer reactions initiated
by visible states will quickly populate the dark sector. These reactions are mediated by
heavy neutrinos. If they are fast enough, transfer reactions can even fully equilibrate the
two sectors. We compute here the amount of energy transferred to the dark sector and the
conditions under which full equilibration is avoided.
For TRH ≫ mϕ , mχ , mZ , the evolution of the energy densities of the dark and visible
sectors can be approximated by
dρ
= −4Hρ − CE ,
(29)
dt
dρx
= −4Hρx + CE ,
dt
√
2
where ρ (ρx ) is the visible (dark) energy density, H = (ρ + ρx )/3MPl
is the Hubble param18
eter with the reduced Planck mass MPl ≃ 2.435 × 10 GeV, and CE is the energy transfer
collision term. Assuming self-thermalization within both sectors, which is expected given
the particle content of each sector, we can relate the energy densities to temperatures by
ρ=

π2
g∗ T 4 ,
30

ρx =

π2
g∗x Tx4 ,
30

(30)

where g∗ ≃ 106.75 and g∗x ≃ 7.25 are the effective numbers of relativistic energy degrees of
freedom in the visible and dark sectors.
For Tx ≪ T and T ≪ Ma , the energy transfer collision term CE is dominated by the 2 → 2
reactions ℓH → χϕ, ℓH → χ† ϕ† and their conjugates. Energy transfer from other reactions
is suppressed by powers of Tx /T < 1. The leading contributions from each of these channels
can be obtained from Tab. 3 together with the results collected in App. A. Neglecting also
asymmetries between these processes and their conjugates, which are expected to be small,
we find
† †

χ ϕ
χϕ
ℓH
CE ≃ 2[CE ]ℓH
χ† ϕ† + 2[CE ]χϕ − 2[CE ]ℓH − 2[CE ]ℓH
{
}
) 9
3
192 (
7
ℓH
ℓH
ℓH
=
[S1 ]χ† ϕ† T + 4 [S2 ]χ† ϕ† + [S2 ]χϕ T − T → Tx ,
π4
π

18

(31)

## PDF page 19

where the definition for [CE ] is given in App. A. This expression, together with the relations
of Eq. (30), provides everything needed to evaluate Eq. (29).
While our final results are based on a full numerical evaluation of Eq. (29), it is instructive
to obtain an approximate solution valid for Tx ≪ T . In this limit, the visible sector dominates
the total energy density and therefore the Hubble rate. Moreover, energy transfer does not
significantly impact the time evolution of T , which scales approximately as T ∝ 1/a. The
energy density of the dark sector is then
ρx
≃
ρ

[

(
1−

T
TRH

) ](

(1)

CE
ρH

)
TRH

[
(
)3 ]( (2) )
T
CE
1
1−
+
3
TRH
ρH

,

(32)

TRH

(n)

where CE is portion of the full collision term obtained from terms [Sn ] in Eq. (31). From
this expression we see that energy transfer in this scenario is UV dominated, with the change
in ρx relative to ρ occurring at temperatures T near reheating. The asymptotic dark sector
temperature resulting from this transfer is
Tx
≡ ξ ≃
T

[

g∗
g∗,x

(

(1)
(2)
CE + CE /3

ρH

)]1/4
.

(33)

TRH

The self-consistency of this approximate result requires ξ < 1. We will see later that ξ < 1
is also needed for the generation of asymmetries and to avoid cosmological constraints. In
practice, we will encounter values ξ ∼ 0.1–0.5 over the parameter ranges that can produce
interesting charge asymmetries, which is consistent with this approximation.

3.2

Production of Heavy Neutrinos

Similar methods can be used to compute the density of heavy neutrinos created after reheating. The number density of heavy neutrino species a evolves after reheating as
dna
= −3Hna + Cna ,
dt

(34)

with the number collision term Cna given to a very good approximation by [67]
Cna

⟨ ⟩
(
)
1
eq
≃
ΓN →ℓH na (T ) − na
γ T a
⟨ ⟩
(
)
1
eq
+
ΓN →χϕ na (Tx ) − na ,
γ Tx a

19

(35)

## PDF page 20

where
ΓNa →ℓH =

∑ |yia |2
i

8π

Ma ,

ΓNa →χϕ =

|λa |2
Ma ,
16π

(36)

with ⟨1/γ⟩Ti = ⟨ma /Ea ⟩Ti is the thermally averaged time dilation factor, neq
a (Ti ) is the
equilibrium number density of Na at temperature Ti , and the decay widths implicitly include
both the listed decay and its C-conjugate (e.g. ΓNa →ℓH has both Na → ℓH and Na → ℓ† H † ).
For the initial conditions na → 0, Tx → 0, and T → TRH ≪ Ma at reheating, the yield
Ya = na /s of Na , with s = 2π 2 g∗s T 3 /45 being the visible entropy density, is always less than
or equal to the equilibrium value at temperature Ma ≫ T > Tx ,
Ya ≤

45
neq
a (T )
≃ 2
x3/2 e−xa ,
s
π (2π)3/2 g∗s a

(37)

where xa = Ma /T . For xa ≳ 25, we find that this density of Na is too small to produce
a significant asymmetry of baryons or dark matter. Since we wish to focus on asymmetry
creation through scattering, we therefore restrict ourselves to M1 /TRH ≥ 25. Moreover, for
such large values of M1 /TRH we also find that the population of dark sector states from
thermal 2 → 1 production of Na followed by Na → χ† ϕ† is negligible compared to the direct
2 → 2 transfer production discussed above.6
While we restrict ourselves to M1 /TRH ≥ 25, it should be noted that this model could
have a viable parameter space for smaller values of M1 /TRH . In such a regime, the primordial
abundance of Na particles is no longer negligible and our scattering calculations would have
to be augmented with the decay of the heavy Majorana neutrinos as well as significant population of the dark sector through decays. As M1 /TRH decreases to near unity, conventional
(asymmetric dark) leptogenesis dominated by decays takes over, as studied in Ref. [40], and
the scattering contributions become negligible.

3.3

Comments on Uneven and Instantaneous Reheating

In this work we assume that inflationary reheating is uneven in that it populates the visible
sector to a much higher degree than the dark sector or the heavy neutrinos. This serves
two key purposes for the asymmetry creation mechanism we study. First, a small initial
dark sector density enables this sector to achieve a different (smaller) temperature than the
visible providing a departure from equilibrium. Second, a tiny initial population of heavy
neutrinos ensures that the dominant source of asymmetries is scattering rather than the outof-equilibrium decays of these massive states. Here we argue that our assumptions about
6

This is also needed to justify our truncated expansion of the scattering kernel in powers of s/Ma2 .

20

## PDF page 21

reheating can be realized in plausible inflationary scenarios for the ranges M1 /TRH ≳ 25 and
ξ = Tx /T ∼ 0.1–0.5 that we consider in our asymmetry calculations.
For inflationary reheating to populate the visible sector over the dark sector, the inflaton
must decay much more readily to the visible sector. This can be achieved with sufficiently
uneven couplings of the inflaton to the two sectors [99–101].7 If the reheating process is
nearly instantaneous, this condition is sufficient to ensure a small dark sector density at the
reheating temperature TRH . We note that nearly instantaneous reheating can be consistent
with current data [105].
Even if reheating is not instantaneous, our assumptions about the state of the universe
after reheating can still be realized to a good approximation. In the standard picture of perturbative reheating, the universe undergoes a phase of domination by inflaton oscillations
between the end of inflation and reheating at visible temperature TRH [106–108]. During
this oscillation phase, the visible temperature can be much larger than TRH which can enhance thermal reactions through higher-dimensional operators [109–112], or facilitate the
production of states heavier than TRH [19, 20]. In our scenario, temperatures greater than
TRH can enhance the rates of transfer reactions or facilitate direct Na production before full
reheating, and may even lead to a full thermalization of the visible and dark sectors before
reheating. However, these effects are countered by the continuous injection of entropy into
the visible sector by inflaton decays, which strongly dilutes the reaction products created
before the end of reheating. In the end, we find that as long as the two sectors are thermally
decoupled at TRH and that xRH = M1 /TRH is large enough, the final population of the dark
sector well after reheating is expected to be nearly identical to what would be obtained from
instantaneous reheating with dark sector population only after TRH .
Calculations supporting the claims above are collected in App. D, and we summarize the
key results here. We model the reheating process with a scalar field oscillating in a quadratic
potential and gradually populating the visible SM sector by decays. Energy transfer to the
dark sector during and after reheating can proceed through 2 → 2 reactions such as ℓH → χϕ
as well as 2 → 1 production ℓH → Na followed by Na → χϕ. For 2 → 2 reactions through
higher-dimensional operators, generalizing the results of Refs. [110, 111] for particle number
transfer to energy transfer, we find that the transfer is dominated by T ∼ TRH for operator
dimensions less than d < 53/6. The contributions from just before the end of reheating are of
the same size or less than those from after reheating. In our scenario, the dominant transfer
comes from d = 5 operators and thus non-instantaneous reheating gives similar results to
instantaneous in this channel. For energy transfer through 2 → 1 production of on-shell Na ,
there is an enhancement from reactions at temperatures M1 ≳ T ≳ TRH relative to after
7

Analogously, in preheating scenarios [102–104] the visible sector can be populated preferentially if the
modes that are excited connect mainly to the SM [100].

21

## PDF page 22

reheating. However, the total contribution from such 2 → 1 processes falls off more quickly
with the ratio xRH = M1 /TRH than for 2 → 2 processes with d = 5 operators. Therefore the
2 → 2 contribution dominates for sufficiently large xRH , and for the parameters considered
in our analysis we find xRH ≳ 25 is typically enough for this. Nearly identical arguments can
be applied to asymmetry generation.
In addition to thermal reactions during and after reheating, energy could also be transferred to the dark sector or the massive neutrinos by gravitational production [113–116]. This
source depends on the Hubble rate during inflation, but is subleading relative to the thermal
channels considered above for the lighter dark sector states. For the massive neutrinos Na ,
their gravitational production is suppressed with our working assumption of M1 /TRH ≫ 1.
Moreover, in contrast to gravitational DM candidates they decay promptly at reheating over
the parameter ranges we study and therefore do not accumulate a large density over time.

4

Asymmetry Creation in the Early Universe

We now turn to study the creation of charge asymmetries in our scenario. The specific charges
we track are B − L and Lx since they are broken individually by transfer reactions but are
conserved by all other reactions in the theory. These charges are generated predominantly at
temperatures near TRH , characteristic of UV freeze-in. In this section, we study in detail the
creation of B − L and Lx charges through scattering. First, we connect these charges with
individual particle densities by imposing constraints implied by the conservation of other
charges as well as equilibrium relations enforced by fast reactions within the visible and
dark sectors. Next, we derive the full set of Boltzmann equations for charge creation. After
that, we investigate specific solutions to these equations. Finally, we study more broadly the
parameter regions over which our scenario can account for the observed baryon abundance,
while relating it to the asymmetry generated in the dark sector.

4.1

Relations Between Particle and Charge Densities

Once created, charge asymmetries are quickly redistributed by much faster reactions within
each of the visible and dark sectors. We can account for the effect of these fast intra-sector
reactions through relations between different chemical potentials.
Recall that a relativistic particle species X with chemical potential µX has an asymmetric
number density of [117, 118]
1
n∆X ≃ gX kX µX TX2 ,
6

(38)

where gX is the number of internal degrees of freedom, kX = 1 (2) for a fermion (boson),
22

## PDF page 23

and TX is its temperature. Moreover, if a reaction α → β is much faster than Hubble, the
chemical potentials of the species involved equilibrate according to [119, 120]
∑

µα =

α

∑

Γα→β ≫ H .

µβ ,

β

(39)

Finally, given an approximately conserved charge Q, the net charge density is related to
species number densities by
nQ ≡

∑

Qi ni ,

(40)

i

where the sum runs over all particle species with charges Qi .
Starting in the visible sector at the high temperatures T ∼ TRH where the asymmetries
are predominantly created, we expect unbroken electroweak symmetry and the equilibration
of all SM gauge interactions [121]. In this temperature range we also expect the equilibration
of both strong and weak sphaleron transitions, as well as most of the Yukawa interactions.
In our analysis we assume that all the Yukawa interactions are equilibrated for simplicity.8
Imposing the equilibration relations from these reactions on the chemical potentials and
demanding zero net hypercharge, we find that all SM chemical potentials can be related to
the net B − L charge. Most importantly for us, we obtain
µℓi = −

7
µB−L ,
79

µH = −

4
µB−L ,
79

(41)

where we have defined µB−L ≡ 6nB−L /T 2 . Note that our assumption of equilibrated lepton
Yukawa interactions together with equal lepton couplings to the Na imply that all the lepton
asymmetries are equal.
Below the electroweak symmetry breaking temperature the electroweak sphalerons turn
off [91,92] and the relations of Eq. (41) are modified. For these lower temperatures, the final
baryon density is [121]
µB =

28
µB−L ,
79

(42)

where µB ≡ 6nB /T 2 .
Turning next to the dark sector, at the high temperatures relevant for asymmetry creation, T ∼ TRH , all dark sector states are effectively massless by assumption. We expect
that the interaction of Eq. (3) will be equilibrated as well as (in most cases) the Dirac mass
of χ. Demanding zero net U(1)D charge as well, all number densities can be related to the
8

This is true for most of the parameter space we study and the error introduced otherwise is small [26–28].

23

## PDF page 24

dark sector lepton charge Lx defined in Tab. 1. For Tx ≫ mϕ , mχ we find
µχ =

1
µL = −µχc ,
2 x

µϕ =

1
µL ,
2 x

µη = µϕ − µχ = 0 ,

(43)

where µLx ≡ 6nLx /Tx2 . As Tx falls below mϕ , the asymmetry in ϕ is transferred to χ and η
such that
µχ = µη = −µχc = µLx .

(44)

This relation remains fixed at Tx < mχ by U(1)D conservation.
The chemical potential relations above allow us to account for the effect of fast intrasector interactions in our model and relate all final asymmetric number densities to the net
Lx and B − L charges produced at high temperatures.

4.2

Boltzmann Equations for Asymmetries

Let us now turn to study the generation and time evolution of the charge asymmetries in
B − L and Lx . These charges are only broken in the theory by transfer reactions. In this
section we obtain the Boltzmann equations that govern the creation and redistribution of
B − L and Lx asymmetries. Some related technical details are collected in App. C.
The general form of the Boltzmann equations for charges Q = B − L, Lx is
dnQ
+ 3HnQ = CQ ,
dt

(45)

where CQ is the collision term describing reactions that change the charge. This term
follows from the general form of Eq. (12), and involves a sum of contributions from all
relevant reactions α → β weighted by the corresponding charge change ∆Qαβ . Here, these
reactions correspond to the transfer reactions in Tab. 2, together with their charge and time
conjugates. In general, CQ depends on the visible and dark temperatures T and Tx as well
as the charges nQ .
Since we expect charge densities to be small relative to total particle number densities
during creation, we expand the charge collision terms to linear order in the asymmetries (or
equivalently the chemical potentials). Upon summing over all reactions, the charge collision
terms can be put in the form
CQ = S Q − W Q ,

(46)

where SQ is a source term that depends on asymmetric matrix elements but is independent of
the charge asymmetries themselves, and WQ is a wash-out term that depends on symmetric
24

## PDF page 25

matrix elements but is also linear in charge asymmetries.
Using CPT and unitarity in the form of Eqs. (22,23), the source terms for B − L and Lx
can be written exclusively in terms of the asymmetries in the reaction rates for ℓi H → ℓ†j H †
and χϕ → χ† ϕ† , respectively. For B − L, we find
12n2g [ ]ℓi H
T8
8
8
SB−L =
D2 ℓ† H † (1 − ξ ) T ≡ σB−L 4 ,
j
π4
M1

(47)

where ng = 3 is the number of lepton generations, ξ = Tx /T ≤ 1, and σB−L is dimensionless.
For Lx , we get
T8
12 [ ]χϕ
8
8
SLx = 4 D2 χ† ϕ† (1 − ξ ) T ≡ σLx 4 .
π
M1

(48)

In the latter forms of these expressions, the coefficients σQ are nearly temperature independent for ξ ≪ 1. They are also both proportional to asymmetric matrix elements that violate
the charges within each sector and require C and CP violation.
A note is in order about these sources in view of the strong constraints on charge creation
through scattering derived in Refs. [64–68], and Ref. [69] in particular, based on equilibration, CPT, and unitarity. Both sources are seen to vanish when ξ = 1, corresponding to
equilibration between the visible and dark sectors. This addresses the primary obstacles in
Refs. [64–68]. The more recent study of Ref. [69] expands these arguments to the case of
freeze-in between two sectors at different temperatures to show that CPT and unitarity imply
that the transfer of a conserved charge between two sectors is proportional to at least the third
power of the portal interaction, i.e. the next-to-leading order, and therefore very suppressed.
Our scenario evades this suppression by explicitly breaking the overall L + Lx symmetry.
After integrating out the massive Na neutrinos, the combination ya λa can be thought of
as the effective freeze-in portal between the two sectors. Taken together, Eqs. (17,20) and
Eqs. (47,48) demonstrate that our source terms are proportional to the portal coupling to
the second power, i.e. the leading order. The key difference relative to Ref. [69] comes from
insertions of the Majorana masses Ma that break the L + Lx symmetry explicitly. Indeed,
by applying CPT and unitarity we have written the sources of Eqs. (47,48) such that they
are proportional to the contributions from reactions that break L + Lx explicitly within each
sector.
The wash-out terms receive contributions from all reactions listed in Tab. 2, including
from processes that do not generate asymmetries. We find
(

WB−L
WLx

)

[

(
)
(
)](
)
(1)
(1)
(2)
(2)
nB−L
T 3 ωB−L,B−L ωB−L,Lx
T 5 ωB−L,B−L ωB−L,Lx
+ 4
,
=
(1)
(2)
M12 ωL(1)x ,B−L
M1 ωL(2)x ,B−L
ωLx ,Lx
ωLx ,Lx
nLx
25

(49)

## PDF page 26

where
(1)
ωB−L,B−L

)
33M12 [ (
ℓi ℓj
ℓi H
ℓi H
ℓi H
=
ng 2ng [S1 ]ℓ† H † + 2ng [S1 ]H † H † + [S1 ]χ† ϕ† + [S1 ]χϕ
79π 4 (
j
)]
†

†

+ [S1 ]ℓχ
+ [S1 ]ℓϕ
+ [S1 ]ℓϕ
+ ξ 3 [S1 ]ℓχ
H † ϕ†
H†ϕ
H † χ†
H†χ

(1)

ωB−L,Lx = −

(1)

ωLx ,B−L = −

(1)

ωLx ,Lx =

(50)

,

)
3M12 [ (
ℓχ
ℓχ†
ℓϕ
ℓϕ†
n
[S
]
−
[S
]
+
[S
]
−
[S
]
g
1
1
1
1
H † ϕ†
H†ϕ
H † χ†
H†χ
π4 (
)]
ℓH
,
+ ξ 3 [S1 ]ℓH
χ† ϕ† − [S1 ]χϕ
)
33M12 [ (
ℓi H
ℓi H
n
[S
]
−
[S
]
g
1
1
†
†
χϕ
χ ϕ
79π 4(
)]
†
ℓχ
ℓϕ
ℓϕ†
+ξ 3 [S1 ]ℓχ
−
[S
]
+
[S
]
−
[S
]
,
1 H†ϕ
1 H † χ†
1 H†χ
H † ϕ†

)
3M12 [ (
ℓχ†
ℓϕ†
ℓχ
ℓϕ
+
[S
]
+
[S
]
n
[S
]
+
[S
]
1
1
g
1
1
†
†
†
†
†
†
H ϕ
H ϕ
H χ
H χ
π4 (
)]
χχ
ℓi H
ℓi H
,
+
n
[S
]
+
n
[S
]
+
2[S
]
+ξ 3 2[S1 ]χϕ
g 1 χϕ
g 1 χ † ϕ†
1 ϕ† ϕ†
χ † ϕ†

(51)

(52)

(53)

where [S1 ] coefficients can be found in Tab. 3. Factors of M1 have been added to make the
(1)
(2)
ωQR terms dimensionless. The expressions for ωQR are identical but with the replacements
{1, ξ 3 }[S1 ] → 24M12 {1, ξ 5 }[S2 ] for reactions with intra-sector initial states (e.g. ℓi H or χϕ)
or {1, ξ 3 }[S1 ] → 24M12 {ξ, ξ 4 }[S2 ] for inter-sector (e.g. ℓχ) initial states.
A key aspect of these expressions is the overall signs of the various terms. Specifically,
they imply that when nQ is non-zero, the wash-out term for the charge Q tends to relax it
to zero. However, we also see that a non-zero charge nQ′ ̸=Q can act as a source for charge Q.
(1,2)
Global stability is guaranteed by the feature that wash-out matrices ωQR have non-negative
traces and determinants.
The Boltzmann equations for Q = B − L, Lx of Eq. (45) together with the expressions
for the source terms of Eqs. (47,48), the wash-out terms of Eq. (49), and the temperature
evolution of Eqs. (29,30) provide a closed system of equations that we solve numerically. To
interpret our numerical results, it is instructive to write these equations in the simplifying
case when Tx /T = ξ ≪ 1, where energy transfer from the visible to the dark sector does not
√
2
. This
significantly alter the time evolution of the visible temperature T and H ≃ ρ/3MPl
implies approximate conservation of entropy in the visible sector. In turn, we have that
u ≡

TRH
T

(54)

is proportional to the scale factor, u ∝ a(t), provided g∗s is constant as we expect for
26

## PDF page 27

T ≫ 100 GeV. Adopting u as the evolution variable and normalizing the charge densities by
the visible entropy density YQ = nQ /s with s = 2π 2 g∗s T 3 /45, we obtain
d
du

(

YB−L
YLx

)

(
)
SB−L − WB−L
1
≃
usH
SLx − WLx
(
)
1
M14
1 σB−L
≃ 4
u s(M1 )H(M1 ) x3RH σLx
)(
)
(
(1)
(1)
YB−L
1 ωB−L,B−L ωB−L,Lx
1 M1
− 2
(1)
u H(M1 ) xRH ωL(1)x ,B−L
ωLx ,Lx
YLx
)(
)
(
(2)
(2)
YB−L
1 M1
1 ωB−L,B−L ωB−L,Lx
− 4
.
(2)
u H(M1 ) x3RH ωL(2)x ,B−L
ωLx ,Lx
YLx

(55)

Here xRH ≡ M1 /TRH , and s(M1 ) and H(M1 ) refer to the visible entropy density and Hubble
rate in the radiation phase formally evaluated at T = M1 with ξ = 0.

4.3

Charge Creation and Dark Wash-In

To study the evolution of charges in our scenario we fix a set of benchmark parameters. It
is convenient to do so in terms of ratios relative to M1 , |λ1 |, and |y1 | and a pair of phases.
For our primary set of benchmarks, we take
M2 = 3M1 ,

y1 = |y1 |eiα ,

y2 = 2|y1 | ,

λ1 = |λ1 | eiβ ,

λ2 = |λ1 | .

(56)

The phase conventions here are completely general and can be obtained by field redefinitions. We also set the magnitude of the lepton Yukawa coupling |y1 | to be the maximum
value allowed by the neutrino mass constraint of Eq. (5) derived from Eq. (4). With the
benchmarks above, this implies the numerical value
(
)(
)
2.32 × 10−3
M1
∆mν
|y1 | =
,
|1 + 3eiα | 1012 GeV
0.07 eV
2

(57)

√
evaluated with ∆mν → 0.07 eV. Note as well that we have |y1 | ∝ M1 . Larger values
of the couplings tend to produce greater asymmetries, whereas in the limit M2 ≫ M1 the
heavier neutrino decouples and the CP violation needed for the source terms is suppressed.
These benchmark values are therefore optimistic in terms of asymmetry generation, but they
are not tuned or reliant on any symmetry. To fully specify the model, the only remaining
quantities to fix are M1 , |λ1 |, and the two phases.

27

## PDF page 28

Using the benchmark coupling ratios, we obtain source terms in Eqs. (47,48)
σB−L
σLx

[
]
12n2g 4 2 2
10
32
sin(α − β) −
sin(α + β) +
sin(2α) (1 − ξ 8 ) ,
=
|y1 λ1 |
4
π
3
27
27
]
[
5
12 2 4
16
sin(α + β) +
sin(2β) (1 − ξ 8 ) .
=
|y λ | 0 sin(α − β) −
π4 1 1
27
27

(58)
(59)

A crucial point here is that both phases appear in both source terms. This implies that
σB−L /|y14 λ21 | and σLx /|y12 λ41 | are expected to be of similar magnitudes in the absence of
(n)
tuning. The wash-out coefficients ωQR can be evaluated in the same way. They have nearly
the same form but with cosines of the phases rather than sines, and typically do not vanish
as the phases go to zero.
The dependence of the source and wash-out coefficients on the two phases has a useful
implication. When these phases are smaller than unity, rescaling them according to α → ζα,
(n)
(n)
β → ζβ with ζ < 1 induces CE → CE , ωQ,Q′ → ωQ,Q′ , and σQ → ζσQ to a very good
approximation. Now, the evolution equations of Eqs. (29,45,46) are invariant under these
transformations if we also shift ρ → ρ, ρx → ρx , and YQ → ζYQ . It follows that a solution for
the densities and asymmetry yields for one set of phases also implies a solution for smaller
phases rescaled by ζ < 1 in which the energy densities ρ and ρx are unchanged but both
charge yields are reduced by a factor of ζ. We will make use of this feature below when
we investigate the conditions under which our scenario can generate the observed baryon
abundance.
To illustrate the specific impact of the phases on asymmetry generation, we consider four
phase benchmark values of (α, β):
B1
B2
B3
B4

=
=
=
=

(−2π/3, π/4)
(−π/3, π/4)
(0.5215π, π/4)
(−2π/3, 0.6052π)

{
}
→ 1.21, 0.76 ,
{
}
→
− 1.57, 0.39 ,
{
}
→ 0.00, 0.63 ,
{
}
→ 1.60, 0.00 .

(60)

The quantities in braces on the right are the values of the sums of sines in square parentheses
appearing in Eqs. (58,59) for σB−L and σLx , respectively. Benchmark B1 has equal signs for
the source term coefficients while benchmark B2 has opposite signs. Benchmark B3 is chosen
such that the B − L source coefficient σB−L vanishes while benchmark B4 has σLx = 0. The
first two benchmarks are reasonably generic for phases on the order of unity, while the second
two benchmarks require specific tuning. We solve our system of equations with a range of
values of model parameters for these benchmark scenarios.
In the left panel of Fig. 3 we show the evolution of the dark temperature ratio ξ = Tx /T as
a function of the visible temperature parameter TRH /T − 1 for the phase benchmark B1 with
28

## PDF page 29

10−8

0.5
|λ1 | = 1.00

10−10

|λ1 | = 0.10

10−11

Tx /T

|λ1 | = 0.03

10−12

0.3

10−13
10−14

0.2
|λ1 | = 1.00
|λ1 | = 0.30

0.1
0.0 −6
10

|YQ |

0.4

10−9

|λ1 | = 0.30

|λ1 | = 0.10
|λ1 | = 0.03

10−3
100
(TRH /T ) − 1

103

10−6

10−3
100
(TRH /T ) − 1

10−15
10−16
10−17
10−18
103

Figure 3: Evolution of the dark temperature ratio ξ = Tx /T (left), and charge densities (right)
of |YB−L | (solid) and |YLx | (dashed) as functions of the inverse temperature relative to reheating
for several values of |λ1 |. Other parameters are specified in the text, with M1 = 1010 GeV, phase
benchmark B1, and |y1 | as large as possible subject to the upper bound on neutrino masses. The
dotted black line corresponds to the |YB−L | value required for the observed baryon asymmetry
today. The evolution in the left plot is generic to UV freeze-in models and shows that for the
chosen parameters the two sectors do not thermalize (ξ < 1). The right plot highlights the
possibility of dark wash-in at larger λ1 values, whereby some of the asymmetry in the dark sector
is transferred to the visible sector via wash-out reactions.

M1 = 1010 GeV (giving |y1 | ≃ 2 × 10−3 ) and several values of |λ1 |. We also fix the reheating
temperature to xRH = M1 /TRH = 30. As expected from our estimates of Eqs. (32,33), we find
that the temperature ratio ξ grows from zero to a nearly constant value once TRH /T − 1 ≳ 1,
with the asymptotic value scaling as
(
ξ∼

|y1 λ1 |2 MPl
xRH M1

)1/4
.

(61)

We find as well that when xRH is held fixed and |y1 | is chosen to saturate the neutrino mass
constraint of Eq. (5), the asymptotic temperature ratio is nearly independent of M1 . For
all cases considered in Fig. 3, ξ remains well below unity and therefore the dark and visible
sectors do not fully equilibrate.
In the right panel of Fig. 3 we show the evolution of the magnitudes of the B − L (solid)
and Lx (dashed) charge yields as a function of TRH /T for the same benchmark parameters.
The shapes of different curves can be understood from the charge evolution equations in the
approximate form of Eq. (55). Immediately after reheating, the source terms dominate and
both charges begin to grow. If the charges become large enough, wash-out reactions can

29

## PDF page 30

slow or even reverse their growth. The wash-out of one charge can also act as a source for
(1,2)
the other through the off-diagonal wash-out coefficients ωQ,Q′ ̸=Q , a process termed wash-in
in Refs. [76–78]. Most of this evolution occurs within a few Hubble times after reheating due
to the overall 1/u4 factors in the source terms and the 1/u2 factors in the leading wash-out
coefficients, which imply that these driving terms eventually decouple. Correspondingly, the
charge yields in Fig. 3 are seen to approach constant values for u = TRH /T − 1 ≫ 1.
For the parameter ranges considered, we typically have |λ1 | > |y1 |. This leads to the
dark Lx source term, which scales as σLx ∝ |y12 λ41 |, being larger than the visible B − L source
that scales as σB−L ∝ |y14 λ21 |. Thus, the dark charge Lx grows more quickly than B − L
at early times. However, these larger couplings also enable greater wash-out. Most of the
dark wash-out is controlled by the coefficient ωLx ,Lx ∼ |y12 λ21 | + ξ 3 |λ1 |4 . We find that dark
wash-out is strong, corresponding to a significant decrease in the final charge relative to the
source alone, when the following condition holds:
∣
(1)
M1 ωLx ,Lx ∣∣
∣
H(M1 ) xRH ∣

(u−1)=1

≫1.

(62)

This condition is met in our scenario for larger |λ1 | and smaller M1 . The impact of strong
wash-out can be seen in the right panel of Fig. 3, specifically in the |YLx | curves for |λ1 | = 1
and |λ1 | = 0.3 where at later times we see a distinctive fall off in |YLx |. Correspondingly,
there is an increase in slope for the |YB−L | curves from wash-in contributions to the charge
B − L from the dark sector, in addition to the direct B − L source. We call this effect dark
wash-in to highlight the role of the dark sector asymmetry as the primary source of the SM
asymmetry in certain parameter regions. In contrast, we do not find a strong wash-out of
B − L charge due to the constraint on |y1 | from neutrino masses.
In the left panel of Fig. 4 we show the effect of varying M1 on charge generation with
fixed |λ1 | = 1 for phase benchmark B1 with xRH = 30 and maximal |y1 |. If |y1 | and xRH
are held fixed, the source and wash-out terms can be shown to both scale as MPl /M1 at
leading order. However, here we adjust |y1 | to be as large as allowed by the neutrino mass
√
constraint of Eq. (5) which fixes |y1 | ∝ M1 (with values ranging between |y1 | ≃ 2 × 10−4
and 0.2). The net effect is that lowering M1 (with fixed xRH and maximal |y1 |) leaves the Lx
source unchanged, enhances Lx wash-out, and weakens the B − L source. These effects are
evident in the left panel of Fig. 4. All the |YLx | curves in the plot follow the same trajectory
until significant wash-out begins, with the onset of wash-out starting earlier for smaller M1 .
For |YB−L |, the decrease in the source for lower M1 is also manifest. Another feature of the
|YB−L | curves is that the contribution from dark wash-in becomes increasingly important for
smaller direct B − L sources.
The right panel of Fig. 4 shows the evolution of the charge yields for the four phase
30

## PDF page 31

M1 = 108 GeV
M1 = 1010 GeV
M1 = 1012 GeV
M1 = 1014 GeV

10−3
100
(TRH /T ) − 1

103

10−6

10−3
100
(TRH /T ) − 1

10

10−6
10−7
10−8
10−9
10−10
10−11
10−12
10−13
10−14
10−15
10−16
10−17
10−18
3

|YQ |

B1
B2
B3
B4

|YQ |

10−6
10−7
10−8
10−9
10−10
10−11
10−12
10−13
10−14
10−15
10−16
10−17
10−18 −6
10

Figure 4: Evolution of the charge densities |YB−L | (solid) and |YLx | (dashed) as a function of the
inverse temperature relative to reheating. In the left panel we show curves for M1 = 108,10,12,14 GeV
and phases as in benchmark B1, see Eq. (60). In the right panel we show curves for phase
benchmarks B1, B2, B3, B4 with M1 = 1010 GeV. For both panels, we also set xRH = 30, |λ1 | = 1,
and |y1 | as large as possible subject to the neutrino mass bound. The horizontal dotted black line
corresponds to the |YB−L | value required for the observed baryon asymmetry today. The left panel
shows that increasing M1 reduces wash-out in the dark sector and increases the asymmetries in
both sectors. The right panel shows that generic benchmarks B1 and B2, as well as benchmark
B3 with zero visible sector source terms, give rise to comparable asymmetries via the dark wash-in
mechanism. In benchmark B4 with no dark source term, there is no dark wash-in, but instead a
transfer of asymmetry from the visible to the dark sector.

benchmarks B1–B4. For B1, the contributions to YB−L from the source and dark wash-in
add constructively. In contrast, for B2 the source and dark wash-in interfere destructively,
and produce a dip in |YB−L | when the contributions from the direct source are overtaken by
those from wash-in. In benchmark B3, the B − L source is tuned to zero (see Eq. (60)), and
the entire B − L charge yield comes from dark wash-in.9 In benchmark B4, the phases are
tuned to produce a vanishing source for Lx , and thus the flow of wash-in is in the opposite
direction of the other benchmark scenarios. The entire B − L charge now comes from the
source alone, while a much smaller Lx charge is produced by wash-in from the visible sector.
While we have focused on specific ratios of M2 /M1 , |y2 /y1 |, and |λ2 /λ1 | (as specified in
Eq. (56)) in the discussion above, we have checked that moderate variations in these values
do not change our qualitative results and primary conclusions. In contrast, the more extreme
limits of M2 /M1 → ∞ or λ2 → 0 lead to very different behavior. The former corresponds
to decoupling the N2 neutrino, in which case we are left with effectively only one heavy
9
The final value of |YB−L | for B3 is higher than for B1 and B2 since the specific phases of B3 lead to a
moderate cancellation in the neutrino mass contribution of Eq. (4), allowing a larger value of |y1 |.

31

## PDF page 32

neutrino that is not able to sustain the CP violation needed for generating asymmetries. In
the latter limit, the dark sector states couple exclusively to N1 so that no physical phase
remains in the dark sector and the dark source term vanishes (while the SM source term is
still non-zero and can generate a B − L asymmetry). As a result, this limit is similar to
phase benchmark B4 from Eq. (60).

4.4

Asymmetry Yields

Having gained an understanding of how the visible and dark charges are created, we now
compute the values of the visible and dark charges today that can be obtained in our scenario
and investigate whether it can explain the observed baryon abundance. Similar to the
previous section, we focus on representative benchmark scenarios that capture the generic
behavior of relevant quantities across our parameter space. Even though we compute the
yields of B − L and Lx charges at temperatures well above the electroweak scale and the
masses of the χ and ϕ dark states, their values do not change once the transfer reactions
discussed above decouple. Moreover, it is straightforward to relate these charge yields to
the final baryon and dark matter (χ) asymmetries using the relations obtained in Sec. 4.1:
YB = (28/79)YB−L and Y∆χ = YLx .
In Fig. 5 we show the late time yields of baryon number YB and Y∆χ in the M1 –|λ1 |
plane for maximal |y1 |, phase benchmark B1, and xRH = 30. The shaded regions in the
lower left of both plots fail to produce the observed baryon asymmetry, YB ≃ 8.7 × 10−11 ,
and are excluded [14, 15]. In the upper right unshaded region, the baryon yield for phase
benchmark B1 is greater than the observed value. However, the correct baryon abundance
can be obtained at any point in this region with smaller values of the phases α and β relative
to the benchmark, as discussed in Sec. 4.3 above.
The dynamics of charge creation studied in the previous subsection can be seen in Fig. 5.
For YB , production comes primarily from the direct source term in the region at larger
M1 and smaller |λ1 |. Moving to smaller M1 and larger |λ1 |, additional B − L is generated
by wash-in from the dark sector, corresponding to the contour feature seen in this region.
Similarly, for Y∆χ = YLx the Lx source term dominates dark charge production for larger M1
and smaller |λ1 |. As noted in the previous subsection, the source is nearly independent of
M1 for maximal |y1 | in this regime. In contrast, in the upper left region of the plot the final
dark charge density falls off rapidly with smaller M1 and larger |λ1 |, and coincides with the
onset of strong wash-out of Lx . To demonstrate this point, the dashed white line in the plots
denotes the boundary above which the strong wash-out condition of Eq. (62) is satisfied.
Comparing the two panels in Fig. 5, we also see that the baryon and dark matter asymmetries can be similar when wash-out is weak. On the other hand, in the strong wash-out
regime, the dark asymmetry is severely depleted and some of it is transferred to the visible
32

## PDF page 33

−10

−10

1011 1012
M1 (GeV)

1013

1014

|λ1 |

−8

−12

1010

−6

−8
log10 (YB )

|λ1 |

10−1

10−2 9
10

100

−6

10−1

−12

−14

−14

−16

−16
10−2 9
10

−18

1010

1011 1012
M1 (GeV)

1013

1014

log10 (Y∆χ )

100

−18

Figure 5: Late time charge densities YB (left) and Y∆χ (right) as functions of M1 and |λ1 |
obtained in the scenario with maximal lepton coupling |y1 |, phase benchmark B1, and xRH = 30.
The shaded regions in the lower left of both plots fail to produce the observed baryon density and
are excluded. The dashed white line marks the boundary above which the strong dark wash-out
condition of Eq. (62) is met. The left panel shows that in our setup we can produce the full baryon
asymmetry for a wide range of parameters. The right panel demonstrates that both asymmetries
tend to be similar in magnitude except in the strong dark wash-out regime where the dark charge
can be orders of magnitude lower.

sector. It was shown previously [40] that similarly large hierarchies are possible in dark leptogenesis models that rely on heavy neutrino decays where the two sectors are in equilibrium.
Our results extend this conclusion to models where the main source of asymmetry-generation
is scattering processes and the visible and the dark sectors never reach an equilibrium. In
the next section, we argue that this large hierarchy translates into a wide range of viable
DM masses that can explain the observed DM abundance today.
In Fig. 6 we show contours of the late time charge densities YB and Y∆χ for a range
of values of M1 and reheating ratio xRH = M1 /TRH . In both plots we fix maximal |y1 |,
|λ1 | = 1, and again use phase benchmark B1. The shaded regions in both panels show where
the predicted baryon density is too low and are excluded. To the lower right of the shaded
region the baryon asymmetry is too large, but as discussed above the observed asymmetry
can be obtained here with smaller phase values. To the left of the dotted white line in both
panels, the strong dark wash-out condition of Eq. (62) is satisfied and correspondingly we
see a reduced dark matter asymmetry.
From the left panel of Fig. 6 we see that YB decreases for larger xRH when other quantities
are held fixed. This is consistent with our expressions for charge evolution in Eq. (55), where
we find that the source terms fall off as 1/x3RH and the leading wash-out terms decrease as
1/xRH . Indeed, at larger M1 , where the direct B − L source dominates, we see a faster
decrease relative to regions at lower M1 , in which the dominant source of baryons is wash-in
33

## PDF page 34

−6

200

−6

175

−8

175

−8

125
100

−12

75
50
25 9
10

1010

1011 1012
M1 (GeV)

1013

1014

150
xRH

−10

log10 (YB )

xRH

150

−10

125
100

−12

−14

75

−14

−16

50

−16

−18

25 9
10

1010

1011 1012
M1 (GeV)

1013

1014

log10 (Y∆χ )

200

−18

Figure 6: Late time charge densities YB (left) and Y∆χ (right) as functions of M1 and
xRH = M1 /TRH obtained in the scenario with maximal lepton coupling |y1 |, |λ1 | = 1, and phase
benchmark B1. The shaded regions in the upper left of both plots fail to produce the observed
baryon density and are excluded. The strong dark wash-out condition of Eq. (62) is met to the
left of the dashed white line in both panels. The left panel shows that by going to smaller xRH
values the observed asymmetry can be attained for lower reheating temperatures. The right panel
re-emphasizes the fact that when the wash-out terms are very strong (to the left of the dashed
white line) they efficiently transfer the asymmetry generated in the dark sector to the visible sector
and give rise to a large hierarchy between the two asymmetries.

from the dark sector. Related features appear in the right panel for Y∆χ . Here, a rapid fall
with xRH is seen at larger M1 , where wash-out is weak and the dark source dominates. In
contrast, at smaller M1 , where the strong dark wash-out regime is realized, the reduction
in wash-out for large xRH counteracts the decrease in the source leading to dark charge
densities that are nearly independent of xRH . Note that similar to Fig. 3, we find that the
DM asymmetry can be orders of magnitude below the SM asymmetry in the strong wash-out
regime.
Our results in Figs. 5-6 also indicate a lower bound on the reheating temperature TRH ≳
4 × 108 GeV if our scenario is to explain the full baryon asymmetry with the benchmark
parameters considered. It is interesting to compare this requirement to the Davidson-Ibarra
bound derived in Ref. [122], where the authors showed that thermal leptogenesis models with
a type-I seesaw mechanism can only generate the observed baryon asymmetry for reheating
temperatures TRH ≳ 109 GeV. Both bounds have the same underlying origin. Smaller TRH
require lower values of M1 to activate the asymmetry generation dynamics. In turn, this
implies that smaller lepton Yukawa couplings are needed for consistency with neutrino mass
requirements. Since the B − L sources in both scenarios scale as |y|4 , the net result is that
sufficient asymmetry generation requires a reasonably large reheating temperature. Despite
these similarities, we also note that the dark wash-in effect allows us to reach slightly lower
34

## PDF page 35

reheating temperatures.10
While the benchmark parameters fixed in Eqs. (56,60) and studied above are fairly representative of the model parameter space, it is interesting to consider whether deviating from
these values could allow us to generate the observed SM asymmetry with lower reheat temperatures. To answer this question, we have performed a broader scan over model parameters
to search for the lowest possible reheating temperature TRH that still generates the observed
baryon asymmetry, while remaining consistent with constraints such as the neutrino mass
bound of Eq. (5) and xRH > 25. With one significant exception, we find that the lowest
possible reheating temperatures for a given M1 value lie within an order-one factor of the
values shown in Fig. 5 for benchmark B1. The specific exception to this conclusion occurs
when the couplings and phases are tuned to minimize the contribution to the active neutrino
masses via Eq. (4). With such a tuning, much larger values of |y1 | are allowed leading to
greatly increased B − L sources, and reheating temperatures as low as TRH ∼ 106 − 107 GeV
are possible. However, given the tuning required to achieve these lower reheat temperatures,
we do not study this possibility any further.

5

Dark Sector Phenomenology

After freeze-in and asymmetry creation shortly after reheating, the visible and dark sectors
evolve independently. As the universe cools to dark temperatures Tx ≲ mϕ , the decay
ϕ → χη transfers the entire Lx asymmetry to χ. Cooling further to Tx ≲ mχ , the annihilation
χχ̄ → η η̄ depletes the symmetric abundance of χ but does not alter the asymmetry. At very
late times, the dark sector consists of a relic density of dark matter consisting of χ (and χ̄)
together with a dark radiation component from the massless η fermions.
In this section we study the cosmological implications of the dark sector and its asymmetry. We investigate the contribution of η to the total radiation density as characterized by
its contribution to the effective number of neutrinos, ∆Neff . We also compute the depletion
of χ through annihilation and determine the range of masses and couplings that allow it to
make up the entire dark matter abundance given the asymmetries computed in the previous
section. This is found to occur with primarily asymmetric χ dark matter for masses between
0.1 GeV ≲ mχ ≲ 103 GeV, while an even greater range of masses is possible for mainly
symmetric dark matter.
10

Previous wash-in models have found even lower reheating temperatures [76, 78], but they do not rely on
heavy neutrinos for B − L or CP violation.

35

## PDF page 36

5.1

Light Degrees of Freedom

To ensure consistency with cosmological observations, particularly the Cosmic Microwave
Background (CMB), the contribution of the η fermion to the radiation density near recombination must not be too large. The key parameter here is the change in the effective number
of neutrinos, ∆Neff , which quantifies the total contribution of new relativistic degrees of
freedom to the energy density in units of a single neutrino species in the instantaneous deSM
≃ 3.046, accounting
coupling limit. Within the standard neutrino decoupling scenario, Neff
for non-instantaneous neutrino decoupling [123, 124]. The latest Planck measurement finds
Neff = 2.99 ± 0.17, leading to a 2σ upper limit of ∆Neff ≲ 0.3 [14]. Upcoming cosmological
surveys such as CMB-S4 aim to further tighten this constraint to ∆Neff ≲ 0.06 [125].
The contribution of the Weyl fermion η to ∆Neff at recombination is
4
∆Neff = ξCMB

(

11
4

)4/3
,

(63)

where ξCMB is the ratio of the dark temperature to the visible photon temperature at the
epoch of CMB formation. For the current (future) constraint ∆Neff ≲ 0.3 (∆Neff ≲ 0.06),
this implies ξCMB ≲ 0.53 (ξCMB ≲ 0.35).
We can relate ξCMB to the previously-computed temperature ratio ξ generated by freezein at high temperatures (T, Tx ≫ mϕ , mχ , mZ ) using the separate conservation of entropy
in both sectors once transfer reactions have decoupled. This gives
[

g∗s,x (TFI ) g∗s (T )
ξ(T ) = ξ(TFI )
g∗s (TFI ) g∗s,x (T )

]1/3
,

(64)

where TFI is the visible temperature after freeze-in has completed and Tx (T ) ≡ ξ(T ) T is
treated as a function of T . Since we consider freeze-in occurring at very high temperatures,
we have the boundary values g∗s (TFI ) ≃ 106.75 and g∗s,x (TFI ) ≃ 7.25. Specializing to the
temperature of recombination, where we expect the only relativistic degrees of freedom in
the dark sector to be the η Weyl fermion, we also have g∗s,x (TCMB ) ≃ 1.75. This translates
into a constraint on the freeze-in temperature ratio ξ = ξ(TFI ) of

0.99 ; ∆N < 0.3
eff
ξ≲
.
0.66 ; ∆Neff < 0.06

(65)

This upper bound on ξ can be compared to the temperature ratios we obtain in our asymmetry calculations. In Fig. 7 we show ξ as a function of |λ1 | and xRH = M1 /TRH for
benchmark B1 with M1 = 1010 GeV (but the result is independent of M1 ). We find that over

36

## PDF page 37

200

0.5

175

0.4

125

0.3

100

0.2

ξ

xRH

150

75
0.1

50
25 −2
10

10−1
|λ1 |

100

0.0

Figure 7: Ratio of the temperatures in the two sectors ξ = Tx /T immediately after the dark sector
is populated near reheating for benchmark B1 in terms of the coupling |λ1 | and xRH = M1 /TRH . We
set M1 = 1010 GeV in this figure. Since ξ < 1 throughout the figure, the dark and visible sectors
do not equilibrate with each other anywhere in the parameter regions we study. We find that
everywhere in this parameter space ξ is small enough to evade the bounds from the contribution
of η to ∆Neff , see the text for details.

the entire parameter space, the dark sector temperature is low enough to evade current and
anticipated future limits on ∆Neff .
Before moving on, let us comment on the interactions of our theory given in Eq. (2),
and specifically the Higgs portal operator κ|ϕ|2 |H|2 that we did not include among them.
Adding this coupling can have an important effect on the effective number of light degrees of
freedom in the scenario since it connects the dark and visible sectors without a suppression
by the heavy neutrino masses and can lead to their thermalization. Being renormalizable,
the thermalization reactions mediated by this operator grow increasingly important relative
to the Hubble rate at lower temperatures until the onset of electroweak symmetry breaking,
at which point they become highly suppressed. Depending on the size of the Higgs portal
coupling κ, there are three regimes: i) κ is very small and the operator does not lead to
any significant thermalization of the two sectors, ii) κ is moderately small such that the
Higgs portal is inactive during asymmetry generation near T ∼ TRH but thermalizes the two
sectors with each other at a later time, iii) κ is large enough to keep the dark and visible
sectors in thermal contact all the way up to reheating. Only regimes i) and ii) are consistent
with our asymmetry generation mechanism, and so far we have assumed to be in regime i).
Now, in our full theory with heavy neutrinos, the Higgs portal coupling is generated
by log-divergent loops involving the other couplings.11 Below the heavy neutrino scale,
11

Note that no such contribution is generated if the theory is embedded into supersymmetry.

37

## PDF page 38

the Higgs portal operator is only renormalized proportionally to itself. This implies that the
Higgs portal coupling κ can in principle be tuned to near zero at the heavy scale and will stay
that way at lower scales, realizing regime i). However, without tuning the natural magnitude
of the coupling is |κ| ≳ |yλ|2 /(4π)2 . For the parameter values considered in our analysis,
we find that this loop-generated natural value of κ is typically too small to thermalize the
two sectors at reheating but large enough to equilibrate them at lower temperatures and
continuing down to the weak scale. This corresponds to regime ii) described above, and is
consistent with the generation of asymmetries but modifies our estimates above for ∆Neff .
To compute the effect, we note that thermalization down to electroweak symmetry breaking
in the early universe corresponds to effectively replacing the high-scale freeze-in value of ξ
with unity. Using Eq. (64), this leads to a prediction of ∆Neff ≃ 0.3, right on the boundary
of what is allowed by current data. Therefore extending our theory to include a natural value
of κ leads to a prediction for ∆Neff that is expected to be tested by future surveys [125].

5.2

Dark Matter in a Dark Sink

After freeze-in of the dark sector and decay of the ϕ state, the DM candidate χ has an
asymmetric yield Y∆χ as well as a much larger symmetric yield YΣχ . If the symmetric yield
is not depleted, it is nearly always too large to allow χ to be the dark matter. However,
our scenario contains the massless η fermion into which the χ state can annihilate. These
particles form a relativistic thermal bath that absorbs the energy density of the symmetric
χ population, acting as a dark sink for this energy [74, 75]. The dark bath is analogous to
the SM photon bath, and does not contribute to the DM density due to the masslessness of
its η constituents.
The relic abundance of χ is determined by the symmetric yield YΣχ following the freezeout of the annihilation reaction χχ̄ → η η̄. Computing this relic yield proceeds much like
standard dark matter freeze-out [94,95] but with two twists: the dark temperature Tx differs
from the visible one [126, 127], and the χ population has an asymmetry [97, 98].12 The
evolution equations for the χ and χ̄ densities are
(
)
dnχ̄
dnχ
eq
+ 3Hnχ =
+ 3Hnχ̄ = −⟨σv⟩ nχ nχ̄ − neq
n
,
χ̄
χ
dt
dt

(66)

3/2
where neq
exp[−(mχ ∓ µχ )/Tx ] and ⟨σv⟩ are evaluated at the dark temχ,χ̄ = gχ (mχ Tx /2π)
perature Tx . It is convenient to change variables to

xx =
12

mχ
,
Tx

Zχ,χ̄ =

x3x
nχ,χ̄ ,
m3χ

We assume here without loss of generality that χ has a positive asymmetry, Y∆χ ≥ 0.

38

(67)

## PDF page 39

and define Z∆ = Zχ − Zχ̄ . For xx ≳ 3 the only remaining relativistic dark species is η so that
g∗s,x ≃ 1.75 is effectively constant. Together with Eq. (66), this implies that Z∆ is constant.
The evolution of Zχ̄ in terms of these variables is
)
m3χ ⟨σv⟩ ( 2
dZχ̄
2
=− 4
Zχ̄ + Zχ̄ Z∆ − Zeq
dxx
xx H

(68)

3/2

with Zeq = gχ xx e−xx /(2π)3/2 .
To evaluate this equation, we also need the visible temperature T in terms of xx to
determine the Hubble rate, and a relation between Zχ,χ̄ and Yχ,χ̄ to set the initial condition.
The first follows from Eq. (64), but now with T to be taken as a function of Tx . For the
second, we have
Zχ,χ̄ (xx ) =

2π 2
g∗s (xx ) ξ −3 (xx ) Yχ,χ̄ (xx ) .
45

(69)

Note that both of these relations are implicit and can be solved iteratively.
We solve Eq. (68) using standard techniques [97, 98] with the freeze-in values of ξ and
Y∆χ computed previously as inputs. The dark sector parameters yχ , mχ , and mϕ do not
impact freeze-in provided the coupling yχ is large enough to self-thermalize the dark sector
and the masses mϕ , mχ are much smaller than Tx during freeze-in. For our calculations, we
set yχ = 1 to ensure dark thermalization while remaining in the perturbative regime, and
mϕ ≥ 1.5 mχ to avoid coannihilation effects. Together with the masses, these parameters
fix the annihilation cross section given in Eq. (28), which has a leading s-wave term at low
collision velocities.
Given an asymmetry Y∆χ , the total yield of χ and χ̄ is bounded below by the asymmetry.
In turn, this implies an upper bound on the χ mass of mχ ≤ mn (ΩDM /ΩB )(YB /Y∆χ ), where
mn is the effective nucleon mass. The upper bound is approached when dark matter is
almost completely asymmetric, corresponding to strong χχ̄ → η η̄ annihilation. When the
annihilation is less efficient, such as for smaller values of yχ or larger ratios mϕ /mχ , the
relic abundance is less asymmetric and the dark matter mass must be smaller to achieve the
observed relic density.
In Fig. 8 we show the maximum allowed χ dark matter mass to obtain the correct relic
density in the M1 –|λ1 | plane with asymmetries computed using the benchmark B1 (shown
in Fig. 5) up to phase rescalings and yχ = 1, mϕ = 1.5 mχ . In the shaded region, the baryon
asymmetry YB is smaller than the observed value YBobs and the dark matter asymmetry we
use to compute relic densities is precisely that displayed in the right panel of Fig. 5. In
the unshaded region, the baryon asymmetry for phase benchmark B1 is larger than the
measured value. Here, we apply the weak phase rescaling procedure discussed in Sec. 4.3
39

## PDF page 40

100

4

|λ1 |

2
10

−1

1

log10 (mmax
χ /GeV)

3

0
10−2 9
10

1010

1011
1012
M1 (GeV)

1013

1014

−1

Figure 8: Maximum allowed dark matter mass to obtain the observed dark matter relic density
subject to the constraint of generating the full baryon abundance in the M1 –|λ1 | plane for (rescaled)
phase benchmark B1 with dark matter annihilation to the dark sink with yχ = 1 and mϕ = 1.5 mχ .
In the shaded region the baryon abundance is smaller than the observed value. In the unshaded
region the baryon asymmetry with benchmark B1 is too large; here we implicitly reduce the weak
phases to get the correct baryon abundance while maintaining the ratio YB /Y∆χ . Between the cyan
dashed lines, the dark matter relic population is mainly asymmetric with Y∆χ ≥ 0.8YΣχ . We find
that our scenario can account for the observed dark matter abundance with dark matter masses
spanning a wide range.

in which we implicitly reduce the phases α and β relative to the benchmark to obtain
YB = YBobs . This procedure also reduces the dark matter asymmetry Y∆χ compared to what
is shown in Fig. 5, but maintains the ratio YB /Y∆χ . The dashed cyan lines in the figure
indicate the boundary of the region where the relic abundance can be mostly asymmetric
with Yχ̄ /Yχ < 0.1 (corresponding to Y∆χ ≃ 0.8YΣχ ).
Dark matter in this scenario can be mainly asymmetric throughout most of the region
where the observed baryon density is obtained. Depending on the relative sizes of the
baryon and dark matter asymmetries, maximum (asymmetric) dark matter masses in the
range 0.1 GeV ≲ mmax
≲ 103 GeV can be achieved. The exception to this occurs in the
χ
upper left unshaded region. Referring to Fig. 5, this region coincides with strong wash-out
of the dark charge asymmetry. On account of the wash-out, the dark matter asymmetry
Y∆χ is very small here, and larger χ masses mχ ≳ 103 GeV would be needed to obtain the
full dark matter abundance. However, for such large masses the annihilation cross section
of Eq. (28), which scales as 1/m2χ , becomes too small to reduce the symmetric component of
40

## PDF page 41

the χ density down to the level of the asymmetry. In this region the dark matter abundance
must be primarily symmetric and the maximum dark matter mass plateaus to symmetric
freeze-out values for our choice of parameters yχ = 1 and mϕ = 1.5 mχ .
By going to larger mϕ /mχ values, the annihilation cross section can be significantly
reduced allowing for a larger symmetric dark matter component.13 This allows us to explain
the dark matter abundance today with even lower χ masses. We verify that by varying these
parameters we can explain the observed dark matter abundance today down to mχ ∼ keV at
which point various astrophysical constraints become relevant [71, 72]. Let us also mention
that if late-time thermalization between the dark and visible sectors occurs due to the Higgs
portal operator κ|H|2 |ϕ|2 as discussed in Sec. 5.1, we would have a larger value of ξ during
the freezeout process compared to the analysis above. This would tend to increase the final
dark matter abundance, and therefore lead to somewhat smaller maximal dark matter masses
than shown in Fig. 8.
Unfortunately, the prospects for testing the dark matter in the model experimentally look
bleak. Our dark matter particle χ is stable and only connects to visible matter through very
massive singlet neutrinos with M1 ≳ 1010 GeV, naively evading direct detection or collider
probes. And since the χ dark matter annihilates to the invisible η particles, no useful indirect
detection signal is expected either. One might also expect dark matter self-interactions or
dissipation involving the massless η particles. However, the possible low-energy operators are
constrained by the symmetries of the theory. The leading χ–η and χ–χ scattering interactions
emerge from four-fermion operators suppressed by 1/m2ϕ , and are point-like and too feeble
to have an observable impact [128].
As a final remark, let us connect our dark sink freeze-out calculations to the stringent
unitarity constraints on freeze-in cogenesis models [64–66, 68, 69], and comment on how our
scenario evades them. CPT and unitarity imply cancellations in generating a baryon asymmetry from equilibrium scattering when summed over all production channels [66]. These
arguments were further extended to the case of two sectors that are out of equilibrium with
each other (while maintaining intra-sector equilibrium) [69]. Specifically, Ref. [69] showed
that the transfer of any conserved charge shared between the two sectors is vanishing at leading order in the portal coupling and can only occur at the third power of this coupling. For
freeze-in mechanisms, which require a feeble portal coupling, this implies a grossly suppressed
asymmetric abundance compared to the symmetric number density. In dark matter-baryon
cogenesis models, if the dark matter asymmetry is within a few orders of magnitude of the
baryon asymmetry, this implies the symmetric dark matter abundance will be much too
large unless it is significantly depleted.
13

Reduced annihilation cross sections can also be done with smaller yχ , but when this coupling becomes
too small our assumption of rapid dark sector self-thermalization at freeze-in may break down.

41

## PDF page 42

Our scenario avoids these pitfalls in two ways. First, the cancellation proven in Ref. [69]
is avoided in our setup because the shared conserved charge L + Lx is explicitly broken by
the heavy neutrino masses Ma , and we are able to obtain comparatively larger asymmetries. Indeed, after applying CPT and unitarity we find that our leading source terms are
proportional to asymmetries in reactions that explicitly break the shared L + Lx charge,
see Eqs. (47,48). Second, the dark sink in our model enables an efficient depletion of the
symmetric abundance of DM into η fermions, which in turn allows us to explain the observed
DM abundance with primarily asymmetric dark matter.

5.3

Other Potential Observables

The primary asymmetry creation dynamics in our scenario must occur at a very high energy
scale relative to laboratory experiments, in analogy to minimal leptogenesis, and this makes
the scenario difficult to test experimentally. Even so, theoretical considerations such as
neutrino mass generation and quantum naturalness motivate potential additional signatures
in our mechanism. We comment here on two classes of possibilities.
Just like standard leptogenesis, the interactions in our scenario can be extended to a
theory of neutrino masses and mixings [26–28]. While the mapping from the CP violating phases in the full theory responsible for asymmetry generation to observable phases
at low energies is not unique, there is a general expectation for CP violation to arise in
the Pontecorvo-Maki-Nakagawa-Sakata (PMNS) matrix [129, 130] that could potentially be
observed at Hyper-Kamiokande [131] and DUNE [132]. Furthermore, our asymmetry generation mechanism favors larger absolute neutrino masses [133], which can be probed in
cosmology [90, 134] and searches for neutrinoless double beta decay [135–137].
Our baryogenesis mechanism also relies on a new scalar field ϕ that connects with the
massive neutrinos. These neutrinos must be very heavy and the scalar-neutrino coupling
needs to be large for asymmetry generation, while the scalar must be considerably lighter to
enable the efficient depletion of the symmetric dark matter component through annihilation,
Eq. (28). Together, these requirements imply large quantum corrections to the dark scalar
mass that must be tuned away to keep it relatively light, analogous to corrections to the
Higgs mass from heavy seesaw neutrinos [138, 139]. This conclusion can be avoided if our
scenario is part of a supersymmetric theory with a scale of soft supersymmetry breaking in
the dark sector not too far above the weak scale. Interestingly, such an embedding would
also suppress a Higgs portal coupling between the dark scalar and the SM Higgs that could
lead to the thermalization of the two sectors, as discussed in Sec. 5.1. On the one hand, this
would eliminate the ∆Neff observable discussed above. On the other, a supersymmetrization
of the theory would also lead to potentially observable superpartners in the visible sector.

42

## PDF page 43

6

Conclusions

In this work, we have developed a simple model for the creation of baryon and dark matter
asymmetries through UV freeze-in scattering. Given the remarkable similarity between the
DM and SM matter abundances, theories that can explain this concordance dynamically
are more natural candidates for the particle nature of DM and well-motivated targets for
various experimental programs. Thus, as one of the first viable models of UV freeze-in DM,
our results provide more credence for this DM mechanism.
Our setup is an asymmetric DM model through a neutrino portal, with an additional new
ultra-light fermion in the dark sector. Unlike most models of heavy neutrino leptogenesis,
in our UV freeze-in model the universe is assumed to reheat to a temperature well below
the masses of the heavy neutrinos with no significant heavy neutrino population, and thus
the asymmetry can not be generated through the portal neutrino decays. Nonetheless, we
show that the 2-to-2 scattering processes mediated by the heavy neutrinos are sufficient for
generating enough asymmetry. The large Majorana mass of the neutrino portal particles
breaks an extended lepton number. This enables different net lepton numbers between the
two sectors, as a result of which DM mass can span a wide range.
Only a small subset of transfer processes between the two sectors contribute to populating
the dark sector as source terms, see Tab. 2. While the remaining processes do not directly
source an asymmetry in dark matter abundance, they have an indispensable role as wash-out
terms that can produce qualitatively new effects. After populating the dark sector through
the source terms, the wash-out terms can redistribute the generated dark asymmetry to a
lepton asymmetry in the visible sector. This is a manifestation of the general idea of wash-in,
in which wash-out terms reprocess a primordial asymmetry in some conserved charge into a
B − L asymmetry. In our model this primordial asymmetry is in the form of a dark matter
asymmetry, so we dub our mechanism dark wash-in.
Although this redistribution allows us to circumvent the Davidson-Ibarra bound on thermal leptogenesis models [122], other cosmological considerations prevent the reheat temperature to be substantially below the original Davidson-Ibarra bound. Depending on model
parameters (couplings and heavy neutrino masses), we can explain the observed SM and
DM abundances today for TRH ≳ 108 GeV and 0.1 GeV ≲ mχ ≲ 103 GeV with an asymmetric dark matter abundance, while even lower masses are viable for symmetric dark matter
abundance.
In conjunction with the asymmetric DM abundance, we also produce a symmetric DM
abundance that is orders of magnitude higher and has to be depleted to evade stringent
astrophysical bounds on the DM density. To that end, we introduced new ultra-light dark
fermions that act as a dark thermal bath into which the DM’s symmetric abundance can
annihilate. This is a manifestation of the dark sink idea and can be used to avoid overclosing
43

## PDF page 44

the universe and other astrophysical bounds. It also allows us to explain the visible and dark
abundances today with dark matter masses as low as O(1) keV for symmetric dark matter
abundance.
Our model is a stepping stone towards a complete solution of the coincidence problem
that relies on the UV freeze-in mechanism. However, to fully solve the coincidence problem,
our generation of asymmetric number densities should be infused with a dynamical selection
of the DM mass such that the total energy densities of the two sectors are naturally within
O(1) factors of each other. Our setup can nevertheless serve as an extreme case, delineating
the space of models that could explain the coincidence problem through freeze-in scattering.
While detecting direct signals of our model appears to be challenging, it would be interesting
to explore potential impacts on neutrino properties [137] or inflationary observables [140].

Acknowledgments
We thank Joe Bramante, Hooman Davoudiasl, Keisuke Harigaya, Graham Kribs, David
McKeen, Alex Millar, Keith Olive, Brian Shuve, Tracy Slatyer, Flip Tanedo, and James
Unwin for illuminating discussions. The work of P.A. is supported by the U.S. Department
of Energy under grant number DE-SC0011640. M.M. is supported by subMIT at MIT
Physics, the Fonds de Recherche du Québec – Nature et Technologies (FRQNT) doctoral
research scholarship (Grant No. 305494), and the Natural Sciences and Engineering Research
Council (NSERC) Canada Postgraduate Scholarship - Doctoral (Grant No. 577851), the U.S.
Department of Energy, Office of Science, Office of High Energy Physics of U.S. Department of
Energy under grant Contract Number DE-SC0012567. This work is supported by Discovery
Grants from NSERC. TRIUMF receives federal funding via a contribution agreement with
the National Research Council (NRC) of Canada. M.S. is supported by the US Department
of Energy under award number DE-SC0008541. This research was supported in part by
grant NSF PHY-2309135 to the Kavli Institute for Theoretical Physics (KITP).

A

Collision Term Calculations

In this appendix we collect some technical details on calculating the contributions to collision
terms appearing in the Boltzmann equations for number and energy densities from 2 → 2
transfer processes. We follow in the footsteps of Refs. [94, 95], but generalize their results
to reactions involving particles belonging to separate thermal baths with different temperatures. We also follow the calculation of Ref. [21] to show that in our setup, and given the
functional form of our matrix elements, the collision terms have simple specific scalings with
temperature. In these calculations, we will also work within the Maxwell-Boltzmann (MB)
44

## PDF page 45

approximation and focus on the specific case of effectively massless particles.

A.1

Number Density

Consider a general 2 → 2 reaction with labels 1 + 2 → 3 + 4. In the MB approximation, from
Eq. (12), the contribution of this reaction to the collision terms for the evolution of number
densities is
∫
∫
12
12
[Cn ]34 ≡ ∆N dΠ1 dΠ2 W34
(s) f1 (T1 )f2 (T2 ) ,
(70)
where fi (Ti ) = (ni /neq
i ) exp(−Ei /Ti ) and ∆N is the change in the relevant species number
per reaction. This expression can be simplified by generalizing the approach of Refs. [94, 95]
to allow for each species to have an independent temperature Ti and assuming massless
particles. To do so, define new variables as
e± =

E1 E2
±
,
T1
T2

1
ŝ = s/ (T1 T2 ) = (e2+ − e2− )(1 − cos θ) ,
2

(71)

where θ is the angle between p⃗1 and p⃗2 . These vary over the ranges
ŝ ≥ 0 ,

e+ ≥

√

√
|e− | ≤ e2+ − ŝ .

ŝ ,

(72)

Changing variables in Eq. (70) yields
[Cn ]12
34

)
∫ ∫
∫
n1 n2 (T1 T2 )2
12
dŝ de+ de− W34
= ∆N
(T1 T2 ŝ) e−e+
eq eq
4
n n
8(2π)
( 1 2 )
∫
∫
√
n1 n2 (T1 T2 )2
12
dŝ W34 (T1 T2 ŝ) de+ 2 e2+ − ŝ e−e+
= ∆N
eq
4
neq
n
8(2π)
( 1 2 )√
∫
√
√
n1 n2
T1 T2
12
ds W34
(s) s K1 ( s/T1 T2 ) ,
= ∆N
eq eq
4
n1 n2 4(2π)
(

(73)

where K1 (z) is a modified Bessel function and in the last line we have used [141]
n

(−∂z ) [z

−ν

Γ(1/2)
Kν (z)] = ν
2 Γ(ν + 1/2)

∫ ∞
1

dt tn (t2 − 1)ν−1/2 e−zt .

(74)

Note that the full collision term for the evolution of a given number density will receive
contributions of this form from all reactions that change the number of the species, including
the reverse reaction 3 + 4 → 1 + 2.
The expression of Eq. (73) can be evaluated analytically when the scattering kernel W(s)

45

## PDF page 46

is a polynomial in s using the identity [141]
∫ ∞
0

dt tµ−1 Kν (t) = 2µ−2 Γ(µ/2 − ν/2) Γ(µ/2 + ν/2) ,

|Re(ν)| < Re(µ) .

(75)

12
As an example, applying this relation to the monomial form W34
(s) → Ak sk , we obtain

[Cn ]12
34

(
→

n1 n2
eq
neq
1 n2

)

k! (k + 1)! 22k
Ak (T1 T2 )k+2
(2π)4

(76)

This result coincides with the calculation of Ref. [70]. Let us also point out that the larger
the power of k, the better the MB approximation used here is expected to be.

A.2

Energy Density

For energy transfer between sectors, we are primarily interested in reactions of the form
1 + 2 → 3 + 4 where both initial states are in the visible sector at temperature T and both
final states are in a dark sector with an independent temperature Tx . This reaction transfers
energy from the visible sector to the dark sector with rate
∫
∫
12
12
[CE ]34 ≡
dΠ1 dΠ2 W34
(s) (E1 + E2 ) f1 (T )f2 (T )
(77)
(
)
∫ ∞
√
n1 n2
T
12
ds
W
(s)
s
K
(
s/T ) .
=
2
eq eq
34
n1 n2 4(2π)4 0
As before, we have generalized the analysis of Refs. [94, 95] to obtain the second line. The
corresponding expression for the reverse reaction would involve Tx rather than T .
12
For the specific case of a monomial scattering kernel, W34
→ Ak sk , evaluating Eq. (77)
using the relation of Eq. (75) yields
[CE ]12
34

B

(
→

n1 n2
eq
neq
1 n2

)

k! (k + 2)! 22k+1
Ak T 2k+5 .
(2π)4

(78)

Asymmetry Matrix Element Calculations

In this appendix we elaborate on the calculation of asymmetric matrix elements and scattering kernels. As discussed in Sec. 2.4, these require both real and imaginary phases and
arise at leading non-trivial order through the interference between tree-level and one-loop
diagrams. In our scenario, the weak phases come from the couplings yia and λa while the
strong phases arise from intermediate particles going on shell in loops.
The diagrammatic topologies contributing to asymmetric matrix elements at leading
46

## PDF page 47

order are shown in Fig. 2. Strong phases arising from loop diagrams can be obtained with
unitarity cuts [96]. After cutting, each one-loop diagram can be associated with a pair of
tree-level diagrams and their related weak phases. With this in mind, it is convenient to
define the following products of couplings:
As,ij = Au,ij =

∑ yia Ma yja
a

Bs = Bu =

∑ λa Ma λa
a

Ci =
Di =

Ma2
Ma2

∑ yia Ma λa
Ma2
a
∑ yia λ∗
a
∼
2
M
a
a

∼ (ℓi H → ℓ†j H † )s,u ,

(79)

∼ (χϕ → χ† ϕ† )s,u ,
∼ (ℓi H → χ† ϕ† )s ,
(ℓi H → χϕ)s ,

where, on the right-hand side in each line, we indicate in which matrix element calculation
the product appears. The coefficients corresponding to the CP conjugates of each tree-level
diagram is the same. For CP- or T- conjugate diagrams, the related coefficient should be
complex conjugated.
For any given process, only a subset of one-loop diagrams contribute to asymmetries.
Depending on which particles run in the loop and where mass insertions occur, the product
of complex couplings Im(c∗0 c1 ) vanishes for many combinations. In terms of how asymmetries
arise through loop topologies, there are three main classes: i) ℓi H → ℓ†j H † and χϕ → χ† ϕ† ;
ii) ℓi H → χ† ϕ† ; iii) ℓi H → χϕ. We treat each of these in turn.
For ℓi H → ℓ†j H † and χϕ → χ† ϕ† there are s- and u-channel diagrams at tree-level.
One-loop asymmetries are generated by propagator loops on s-channel Na containing χϕ for
ℓH → ℓ† H † and ℓH for χϕ → χ† ϕ† . There are contributions from Majorana mass insertions
on either side of the loop. At leading order in an expansion in powers of Mandelstam
variables, we find
)
]
[(
st
Im 2A∗s,ij + A∗u,ij (Ci Dj + Di Cj )
4π

(80)

]
[
∑
st
|∆Mχϕ
| = − Im (Bs∗ + Bu∗ )
(Ck Dk∗ + Dk∗ Ck ) .
χ † ϕ†
4π
k

(81)

2

|∆Mℓℓi†H
| =−
H†
j

and
2

The relative factors of two in some of terms correspond to differences in SU(2)L contractions.
The second class of asymmetries corresponds to the reaction ℓi H → χ† ϕ† and its conjugates. There is now only a single s-channel contribution at tree-level. The loops relevant
47

## PDF page 48

to asymmetries are vertex loops on either side of the diagram, and propagator loops on an
s-channel Na leg containing ℓk H and a Majorana mass insertion on the ℓi H side or with χϕ
and a mass insertion on the χϕ side. We find the asymmetric matrix element
st
2
|∆Mℓχi†Hϕ† | = −
4π

[
Im Ci∗

(

)]
∑

Au,ik Dk∗ + Di Bu + 2

k

∑

As,ik Dk∗ + Di Bs

.

(82)

k

In the last bracket above, the first two terms correspond to the vertex loops and the second
two to the propagator loops.
The last class of processes supporting an asymmetry is ℓi H → χϕ. This reaction preserves the combined charge L + Lx and requires an even number of Majorana neutrino mass
insertions. To generate asymmetries, the single s-channel contribution at tree level interferes
with vertex loops at both sides of the diagram as well as propagator loops containing χϕ
and ℓk H on an s-channel Majorana neutrino line. The asymmetry is
[

su
2
iH
|∆Mℓχϕ
| =−
Im
4π

)]

(
Di∗

∑

Au,ik Ck∗ + Ci Bu∗ + 2

∑

As,ik Ck∗ + Ci Bs∗

.

(83)

k

k

As above, in the last bracket the first two terms correspond to vertex loops and the last two
terms are propagator loops.
Integrating these expressions over the final state phase spaces yields the related asymmetric scattering kernels. This produces −st → s2 /16π and −su → s2 /16π, and thus the
leading terms in all the scattering kernels are proportional to s2 . These can be shown to
satisfy the CPT/unitarity constraint of Eq. (21). Specializing to ng = 3 lepton generations
with yia = ya , we obtain the asymmetry coefficients [D2 ] of Eqs. (17)–(20).

C

Source and Wash-out Collision Term Calculations

We turn now to elaborating on the calculation of the collision terms CQ for the charges
Q = B − L, Lx defined in Eq. (45). In our scenario, these are dominated by 2 → 2 reactions
of the form 1 + 2 → 3 + 4. For the discussion here, it is convenient to classify such reactions
as self-conjugate, satisfying (34) = (12)† , and non-self-conjugate otherwise. The total contribution to CQ from a self-conjugate reaction involves only 1 + 2 → 1† + 2† and 1† + 2† → 1 + 2.
For a non-self-conjugate reaction, there are also independent reverse reactions giving four
contributions: 1 + 2 → 3 + 4, 1† + 2† → 3† + 4† , 3 + 4 → 1 + 2, and 3† + 4† → 1† + 2† .
Consider first a self-conjugate reaction 1 + 2 → 3 + 4, with 3 = 1† and 4 = 2† , that

48

## PDF page 49

changes the charge Q by the amount ∆Q. The total contribution to CQ from Eqs. (12,70) is
∫

/
∆CQ ∆Q =

∫
dΠ1

)
(
† †
12
dΠ2 W34
f1 f2 − W31† 42† f1† f2† ,

(84)

where
fi,i† = e±µi /Ti e−Ei /Ti ≡ e±µi /Ti fi0 ,

(85)

with Ti being the relevant temperature of the i-th species and µi its chemical potential. Since
we expect small asymmetries, it is a good approximation to expand to linear order in the
chemical potentials. We find
∫

/

∆CQ ∆Q =

[

∫
dΠ1

dΠ2

12
12
∆W34
+ ΣW34

(

µ1 µ2
+
T1 T2

)]

f10 f20 .

(86)

Referring back to Eq. (46), we identify the first term above with part of the source term SQ
and the second term with a portion of the wash-out term WQ .
The contribution to the charge collision term CQ from a non-self-conjugate reaction
1 + 2 → 3 + 4 follows similarly, but now with additional pieces coming from the independent reverse reactions. These can be simplified using the effective masslessness of all
initial and final states, CPT, and our definitions of symmetric and asymmetric matrix ele34
12
34
12
ments. Together, these imply ΣW12
(s) = ΣW34
(s) and ∆W12
(s) = −∆W34
(s). Assembling
all the terms gives the final result
/

∆CQ ∆Q =

∫

∫
dΠ1

(
( 0 0
)
12
dΠ2 ∆W34
f1 f2 + f30 f40

12
+ ΣW34

[(

µ1 µ2
+
T1 T2

)

f10 f20 −

(87)
(

µ3 µ4
+
T3 T4

)

f30 f40

])
,

where here f30 = exp(−E1 /T3 ) and f40 = exp(−E2 /T4 ) are functions of the momenta being
integrated over and the scattering kernels are functions of s = (p1 + p2 )2 . As for the self12
conjugate case, the first term depending on ∆W34
contributes to the source term for Q while
12
the second that depends on ΣW34
contributes to the wash-out term.
The full charge collision term CQ is the sum of contributions from all relevant reactions
that change charge Q. For our scenario, these are collected in Tab. 2. Collecting them all and
relating the species chemical potentials to the charge chemical potentials using Eqs. (41,43),
we obtain the source and wash-out terms collected in Sec. 4.2.
To give more insight into how the general results here translate into the specific expressions in Sec. 4.2, let us now present two examples. First, we derive the source term for B −L.
49

## PDF page 50

This example also demonstrates how CPT and unitarity resolve the seemingly curious feature
of Eqs. (86,87) that the source contributions from the individual contributions do not vanish
in equilibrium, corresponding to T1 = T2 = T3 = T4 . The reactions contributing to the
B − L source are ℓi H → ℓ† H † (∆Q = 2), ℓi H → χϕ (∆Q = 1), and ℓi H → χ† ϕ† (∆Q = 1).
Summing over them, we obtain
∫
SQ =

∫
dΠ1

dΠ2

[
∑ ∑
i

=

∑∫

∫
dΠ1

i,j

(

ℓi H
H
∆Wℓℓ†iH
+ ∆Wχℓi†Hϕ†
2 fℓ0 fH0 + ∆Wχϕ
†
j

j

H
dΠ2 ∆Wℓℓ†iH
†
j

(

fℓ0 fH0 − fχ0 fϕ0

)(

fℓ0 fH0 + fχ0 fϕ0

)

]
(88)

)

In going from the first to the second line, we have applied the CPT and unitarity relation of
Eq. (21) (as realized explicitly in Eqs. (22,23)). Upon integrating over the initial state phase
space, we reproduce Eq. (47). We also see that, in contrast to the individual contributions
to the source, the full source term vanishes in equilibrium when Tx = T .
As a second example, let us compute the contributions to the B − L and Lx wash-out
terms from the reaction ℓi H → χ† ϕ† , which has ∆(B − L) = +1 and ∆Lx = −1. Applying
our general result, we get
∫
∆WQ /∆Q =

∫
dΠ1

dΠ2 ΣWχℓi†Hϕ†

[(

)
)
(
]
µℓ + µH
−µχ − µϕ 0 0
0 0
fℓ fH −
fχ fϕ
T
Tx

(89)

∫
∫
66 nB−L
dΠ1 dΠ2 ΣWχℓi†Hϕ† fℓ0 fH0
= −
79 T 3
∫
∫
nLx
dΠ1 dΠ2 ΣWχℓi†Hϕ† fχ0 fϕ0
+6 3
Tx
Here, we have used the relations between chemical potentials and charge densities obtained
in Sec. 4.1. Integrating over these expressions over phase space reproduces the corresponding
parts of Eq. (49).

D

Transfer with Non-Instantaneous Reheating

In our primary analysis above we assumed instantaneous reheating after inflation to a temperature TRH < M1 . Here we consider the impact of non-instantaneous reheating on our
scenario. Based on our estimates, we argue that most of the results obtained with instantaneous reheating also apply to motivated non-instantaneous cases as long as the ratio M1 /TRH
is large enough.
As a simple model for the reheating process, we consider a reheating period between the
inflation and radiation eras during which the total energy density of the universe is domi50

## PDF page 51

nated by a scalar field (such as the inflaton) oscillating in a quadratic potential as it decays
exclusively to light SM particles. The averaged energy density of these oscillations redshifts
like matter, ρo ∝ a−3 . After a brief initial transient, the subdominant visible radiation component reaches a maximum and then redshifts as ρr ∝ T 4 ∝ a−3/2 . Reheating is completed
when the radiation density becomes dominant at temperature TRH . For the purposes of our
estimates, a sufficient parametrization of this behavior is
{
H≃

HRH a−3/2 ; T > TRH
HRH a−2
; T < TRH

{
,

T ≃

TRH a−3/8 ; T > TRH
TRH a−1
; T < TRH

,

(90)

2
where we have normalized a = 1 at reheating and HRH ∼ TRH
/MPl . We also define
xRH = M1 /TRH and assume that it is larger than unity.
Consider now the transfer of energy density from the visible sector to the dark sector
during and after reheating. The dominant reactions contributing to the transfer are 2 → 2
processes such as ℓH → χ† ϕ† mediated by an off-shell Na , together with 2 → 1 production
ℓH → Na followed by the 1 → 2 decay Na → χϕ. To compute the total amount of energy
transferred, it is helpful to consider the contributions from three disjoint regions in the
evolution: i) a ∈ [ai , aM ], ii) a ∈ [aM , 1], iii) a ∈ [1, af ], where ai is some initial scale factor
after inflation, aM is the scale factor at which T = M1 , and af is some final scale factor after
the end of reheating. Regions i) and ii) occur during the reheating process, while region iii)
is the evolution after reheating has completed. Note that we implicitly allow the maximum
temperature achieved during reheating to exceed M1 . For simplicity, we also consider only
a single flavor of massive neutrino N1 .
Let us estimate first the transfer of energy to the dark sector energy from 2 → 2 reactions.
The contribution from region i) with a < aM can be shown to be subleading, so we discuss
only the portions from regions ii) and iii) here. When a > aM , the leading part of the energy
transfer collision term is

CE ≃

)
A ( 2k+5
T
− Tx2k+5 ,
2k
M1

(91)

/ 4
with k = 1 and A ≃ 3M12 [S1 ]ℓH
π . Applying the form to region ii), neglecting reverse
χ † ϕ†
reactions we find the upper bound
∫ 1

a4
T 2k+5
∆(a ρx ) ≲
da
A
aH
M 2k
aM
(
) 1
(
) 1
AM1
−(2k+1)
(29−6k)/8
4
xRH
1 − aM
.
≃ TRH
HRH
29 − 6k
4

(92)

This contribution is dominated by T ∼ TRH for k < 29/6, as we have here. Similarly, energy
51

## PDF page 52

transfer from the visible sector to the dark sector in region iii) after reheating is
∫ af

a4
T 2k+5
da
∆(a ρx ) ≲
A
aH
M12k
1
(
)
(
) 1
AM1
−(2k+1)
−(2k−1)
4
≃ TRH
xRH
1 − af
.
HRH
2k − 1
4

(93)

This result matches our previous calculation in Sec 3.1, and is dominated by reactions near
T ∼ TRH . Comparing the contributions from regions ii) and iii), we see that they are of
the same order. A similar conclusion holds for asymmetry generation and washout, which
is dominated in our scenario by operators with k = 1 (washout) and k = 2 (asymmetry
sources).
We turn next to the transfer of energy to the dark sector from the direct production and
decay of the massive neutrinos. The relevant energy transfer collision term for total decay
width Γ ≫ H of the massive neutrino N1 is
CE ≃ M1

]
ΓN1 →ℓH ΓN1 →χϕ [
n̄1 (T ) − n̄1 (Tx ) ,
Γ

(94)

where the partial widths are listed in Eq. (36). Starting with region i), we have
∫
a4 2(3/4)ζ(3) 3
ΓN1 →ℓH ΓN1 →χϕ aM
da
T
∆(a ρx ) ≲ M1
Γ
aH
π2
ai
4 12ζ(3) ΓN1 →ℓH ΓN1 →χϕ −32/3
≃ TRH
xRH .
35π 2
Γ HRH
4

(95)

From region ii) we find
(
)3/2
∫
ΓN1 →ℓH ΓN1 →χϕ a1
a4
M1 T
∆(a ρx ) ≲ M1
da
2
e−M1 /T
Γ
aH
2π
aM
16
ΓN1 →ℓH ΓN1 →χϕ −32/3
4
≃ TRH
xRH Γ(73/6 + 1) .
3/2
3(2π)
Γ HRH
4

Note that in the second line above we have used
∫ xRH
du u73/6 e−u ≲ Γ(73/6 + 1) ,

(96)

(97)

1

where Γ(z) is the gamma function and this expression is an approximate equality for xRH ≫
73/6. Finally, in region iii) we obtain
ΓN →ℓH ΓN1 →χϕ
∆(a ρx ) ≲ M1 1
Γ
4

52

∫ af
1

(
)3/2
a4
M1 T
2
e−M1 /T
da
aH
2π

(98)

## PDF page 53

4
≃ TRH

2
ΓN1 →ℓH ΓN1 →χϕ 3/2 −xRH
xRH e
.
3/2
(2π)
Γ HRH

Examining the contributions from the three regions, we find that region ii) is dominant.
We are now equipped to compare the relative contributions from 2 → 2 and 2 → 1
processes to the dark sector energy density. Examining the scalings of the various contributions with xRH , the dominant source of dark sector energy will come from 2 → 2
reactions near reheating if xRH is big enough. Evaluating numerically, and noting that
AM1 ∼ |λ1 |2 ΓN1 →ℓH ΓN1 →χϕ /Γ for |λ|2 ≫ |y|2 , we find that 2 → 2 reactions near TRH dominate the energy transfer to the dark sector when xRH ≳ 20 for |λ1 | = 1.0 and when xRH ≳ 35
for |λ1 | = 0.1. Also, fixing xRH = 30 we find that 2 → 2 reactions near TRH are the leading source of energy transfer to the dark sector throughout the parameter region where the
mechanism can generate the observed baryon abundance. Based on these calculations, we
conclude that replacing our previous assumption of instantaneous reheating with a more
gradual reheating process as modeled above our results for energy transfer to the dark sector
would not change in a significantly qualitative way for most of the parameter ranges we
consider. Nearly identical arguments can be applied to asymmetry generation through the
decays of massive neutrinos created prior to reheating; their contribution is subleading to
that from 2 → 2 processes after reheating provided xRH is large enough.

53

## PDF page 54

References
[1] G. Jungman, M. Kamionkowski, and K. Griest, “Supersymmetric dark matter,”
Phys. Rept. 267 (1996) 195–373, arXiv:hep-ph/9506380.
[2] G. Bertone, D. Hooper, and J. Silk, “Particle dark matter: Evidence, candidates and
constraints,” Phys. Rept. 405 (2005) 279–390, arXiv:hep-ph/0404175.
[3] L. Roszkowski, E. M. Sessolo, and S. Trojanowski, “WIMP dark matter candidates
and searches—current status and future prospects,” Rept. Prog. Phys. 81 no. 6,
(2018) 066201, arXiv:1707.06277 [hep-ph].
[4] A. Arbey and F. Mahmoudi, “Dark matter and the early Universe: a review,” Prog.
Part. Nucl. Phys. 119 (2021) 103865, arXiv:2104.11488 [hep-ph].
[5] M. Cirelli, A. Strumia, and J. Zupan, “Dark Matter,” arXiv e-prints (6, 2024) ,
arXiv:2406.01705 [hep-ph].
[6] N. Bozorgnia, J. Bramante, J. M. Cline, D. Curtin, D. McKeen, D. E. Morrissey,
A. Ritz, S. Viel, A. C. Vincent, and Y. Zhang, “Dark Matter Candidates and
Searches,” arXiv:2410.23454 [hep-ph].
[7] A. Riotto, “Theories of baryogenesis,” in Proceedings, Summer School in High-energy
physics and cosmology: Trieste, Italy, June 29-July 17, 1998, pp. 326–436. 1998.
arXiv:hep-ph/9807454 [hep-ph].
[8] J. M. Cline, “Baryogenesis,” in Les Houches Summer School - Session 86: Particle
Physics and Cosmology: The Fabric of Spacetime. 9, 2006. arXiv:hep-ph/0609145.
[9] S. Davidson, E. Nardi, and Y. Nir, “Leptogenesis,” Phys. Rept. 466 (2008) 105–177,
arXiv:0802.2962 [hep-ph].
[10] L. Canetti, M. Drewes, and M. Shaposhnikov, “Matter and Antimatter in the
Universe,” New J. Phys. 14 (2012) 095012, arXiv:1204.4186 [hep-ph].
[11] D. E. Morrissey and M. J. Ramsey-Musolf, “Electroweak baryogenesis,” New J. Phys.
14 (2012) 125003, arXiv:1206.2942 [hep-ph].
[12] G. Elor et al., “New Ideas in Baryogenesis: A Snowmass White Paper,” in Snowmass
2021. 3, 2022. arXiv:2203.05010 [hep-ph].
[13] J. L. Barrow et al., “Theories and Experiments for Testable Baryogenesis
Mechanisms: A Snowmass White Paper,” arXiv e-prints (3, 2022) ,
arXiv:2203.07059 [hep-ph].
[14] Planck Collaboration, N. Aghanim et al., “Planck 2018 results. VI. Cosmological
parameters,” Astron. Astrophys. 641 (2020) A6, arXiv:1807.06209
[astro-ph.CO]. [Erratum: Astron.Astrophys. 652, C4 (2021)].
[15] ACT Collaboration, T. Louis et al., “The Atacama Cosmology Telescope: DR6
Power Spectra, Likelihoods and ΛCDM Parameters,” arXiv e-prints (3, 2025) ,
arXiv:2503.14452 [astro-ph.CO].

54

## PDF page 55

[16] S. Dodelson and L. M. Widrow, “Sterile-neutrinos as dark matter,” Phys. Rev. Lett.
72 (1994) 17–20, arXiv:hep-ph/9303287.
[17] J. McDonald, “Gauge singlet scalars as cold dark matter,” Phys. Rev. D 50 (1994)
3637–3649, arXiv:hep-ph/0702143.
[18] L. J. Hall, K. Jedamzik, J. March-Russell, and S. M. West, “Freeze-In Production of
FIMP Dark Matter,” JHEP 03 (2010) 080, arXiv:0911.1120 [hep-ph].
[19] D. J. H. Chung, E. W. Kolb, and A. Riotto, “Production of massive particles during
reheating,” Phys. Rev. D 60 (1999) 063504, arXiv:hep-ph/9809453.
[20] G. F. Giudice, E. W. Kolb, and A. Riotto, “Largest temperature of the radiation era
and its cosmological implications,” Phys. Rev. D 64 (2001) 023508,
arXiv:hep-ph/0005123.
[21] F. Elahi, C. Kolda, and J. Unwin, “UltraViolet Freeze-in,” JHEP 03 (2015) 048,
arXiv:1410.6157 [hep-ph].
[22] A. D. Sakharov, “Violation of CP Invariance, C asymmetry, and baryon asymmetry
of the universe,” Pisma Zh. Eksp. Teor. Fiz. 5 (1967) 32–35.
[23] M. Fukugita and T. Yanagida, “Baryogenesis Without Grand Unification,” Phys.
Lett. B 174 (1986) 45–47.
[24] M. A. Luty, “Baryogenesis via leptogenesis,” Phys. Rev. D 45 (1992) 455–465.
[25] G. F. Giudice, A. Notari, M. Raidal, A. Riotto, and A. Strumia, “Towards a
complete theory of thermal leptogenesis in the SM and MSSM,” Nucl. Phys. B 685
(2004) 89–149, arXiv:hep-ph/0310123.
[26] W. Buchmuller, R. D. Peccei, and T. Yanagida, “Leptogenesis as the origin of
matter,” Ann. Rev. Nucl. Part. Sci. 55 (2005) 311–355, arXiv:hep-ph/0502169
[hep-ph].
[27] M.-C. Chen, “TASI 2006 Lectures on Leptogenesis,” in Theoretical Advanced Study
Institute in Elementary Particle Physics: Exploring New Frontiers Using Colliders
and Neutrinos, pp. 123–176. 3, 2007. arXiv:hep-ph/0703087.
[28] C. S. Fong, E. Nardi, and A. Riotto, “Leptogenesis in the Universe,” Adv. High
Energy Phys. 2012 (2012) 158303, arXiv:1301.3062 [hep-ph].
[29] A. Pilaftsis, “CP violation and baryogenesis due to heavy Majorana neutrinos,”
Phys. Rev. D 56 (1997) 5431–5451, arXiv:hep-ph/9707235.
[30] A. Pilaftsis and T. E. J. Underwood, “Resonant leptogenesis,” Nucl. Phys. B 692
(2004) 303–345, arXiv:hep-ph/0309342.
[31] L. Bento and Z. Berezhiani, “Leptogenesis via collisions: The Lepton number leaking
to the hidden sector,” Phys. Rev. Lett. 87 (2001) 231304, arXiv:hep-ph/0107281.
[32] T. Blažek, J. Heeck, J. Heisig, P. Maták, and V. Zaujec, “Dirac leptogenesis from
asymmetry wash-in via scatterings,” Phys. Rev. D 110 no. 5, (2024) 055042,
arXiv:2404.16934 [hep-ph].
55

## PDF page 56

[33] S. Nussinov, “Technocosmology: Could a technibaryon excess provide a ’natural’
missing mass candidate?” Phys. Lett. 165B (1985) 55–58.
[34] D. B. Kaplan, “A Single explanation for both the baryon and dark matter densities,”
Phys. Rev. Lett. 68 (1992) 741–743.
[35] D. E. Kaplan, M. A. Luty, and K. M. Zurek, “Asymmetric Dark Matter,” Phys. Rev.
D79 (2009) 115016, arXiv:0901.4117 [hep-ph].
[36] K. Petraki and R. R. Volkas, “Review of asymmetric dark matter,” Int. J. Mod.
Phys. A 28 (2013) 1330028, arXiv:1305.4939 [hep-ph].
[37] K. M. Zurek, “Asymmetric Dark Matter: Theories, Signatures, and Constraints,”
Phys. Rept. 537 (2014) 91–121, arXiv:1308.0338 [hep-ph].
[38] H. Davoudiasl, D. E. Morrissey, K. Sigurdson, and S. Tulin, “Hylogenesis: A Unified
Origin for Baryonic Visible Matter and Antibaryonic Dark Matter,” Phys. Rev. Lett.
105 (2010) 211304, arXiv:1008.2399 [hep-ph].
[39] H. Davoudiasl and R. N. Mohapatra, “On Relating the Genesis of Cosmic Baryons
and Dark Matter,” New J. Phys. 14 (2012) 095011, arXiv:1203.1247 [hep-ph].
[40] A. Falkowski, J. T. Ruderman, and T. Volansky, “Asymmetric Dark Matter from
Leptogenesis,” JHEP 05 (2011) 106, arXiv:1101.4936 [hep-ph].
[41] N. F. Bell, K. Petraki, I. M. Shoemaker, and R. R. Volkas, “Pangenesis in a
Baryon-Symmetric Universe: Dark and Visible Matter via the Affleck-Dine
Mechanism,” Phys. Rev. D 84 (2011) 123505, arXiv:1105.3730 [hep-ph].
[42] C. Cheung and K. M. Zurek, “Affleck-Dine Cogenesis,” Phys. Rev. D 84 (2011)
035007, arXiv:1105.4612 [hep-ph].
[43] J. March-Russell and M. McCullough, “Asymmetric Dark Matter via Spontaneous
Co-Genesis,” JCAP 03 (2012) 019, arXiv:1106.4319 [hep-ph].
[44] B. Barman, D. Borah, and R. Roshan, “Nonthermal leptogenesis and UV freeze-in of
dark matter: Impact of inflationary reheating,” Phys. Rev. D 104 no. 3, (2021)
035022, arXiv:2103.01675 [hep-ph].
[45] D. Bose, R. Pramanick, and T. S. Ray, “Cogenesis of visible and dark matter in a
scotogenic model,” arXiv:2409.06541 [hep-ph].
[46] J. Shelton and K. M. Zurek, “Darkogenesis: A baryon asymmetry from the dark
matter sector,” Phys. Rev. D 82 (2010) 123512, arXiv:1008.1997 [hep-ph].
[47] N. Haba and S. Matsumoto, “Baryogenesis from Dark Sector,” Prog. Theor. Phys.
125 (2011) 1311–1316, arXiv:1008.2487 [hep-ph].
[48] M. R. Buckley and L. Randall, “Xogenesis,” JHEP 09 (2011) 009, arXiv:1009.0270
[hep-ph].
[49] M. Blennow, B. Dasgupta, E. Fernandez-Martinez, and N. Rius, “Aidnogenesis via
Leptogenesis and Dark Sphalerons,” JHEP 03 (2011) 014, arXiv:1009.3159
[hep-ph].
56

## PDF page 57

[50] E. Hall, T. Konstandin, R. McGehee, H. Murayama, and G. Servant, “Baryogenesis
From a Dark First-Order Phase Transition,” JHEP 04 (2020) 042,
arXiv:1910.08068 [hep-ph].
[51] E. Hall, R. McGehee, H. Murayama, and B. Suter, “Asymmetric dark matter may
not be light,” Phys. Rev. D 106 no. 7, (2022) 075008, arXiv:2107.03398 [hep-ph].
[52] A. Datta, R. Roshan, and A. Sil, “Imprint of the Seesaw Mechanism on Feebly
Interacting Dark Matter and the Baryon Asymmetry,” Phys. Rev. Lett. 127 no. 23,
(2021) 231801, arXiv:2104.02030 [hep-ph].
[53] S. Bhattacharya, R. Roshan, A. Sil, and D. Vatsyayan, “Symmetry origin of baryon
asymmetry, dark matter, and neutrino mass,” Phys. Rev. D 106 no. 7, (2022)
075005, arXiv:2105.06189 [hep-ph].
[54] Y. Cui, L. Randall, and B. Shuve, “A WIMPy Baryogenesis Miracle,” JHEP 04
(2012) 075, arXiv:1112.2704 [hep-ph].
[55] Y. Cui and R. Sundrum, “Baryogenesis for weakly interacting massive particles,”
Phys. Rev. D 87 no. 11, (2013) 116013, arXiv:1212.2973 [hep-ph].
[56] J. McDonald, “Baryomorphosis: Relating the Baryon Asymmetry to the ’WIMP
Miracle’,” Phys. Rev. D83 (2011) 083509, arXiv:1009.3227 [hep-ph].
[57] S. Davidson and M. Elmer, “Similar Dark Matter and Baryon abundances with
TeV-scale Leptogenesis,” JHEP 10 (2012) 148, arXiv:1208.0551 [hep-ph].
[58] Y. Cui, “A Review of WIMP Baryogenesis Mechanisms,” Mod. Phys. Lett. A30
no. 37, (2015) 1530028, arXiv:1510.04298 [hep-ph].
[59] X. Chu, Y. Cui, J. Pradler, and M. Shamma, “Dark freeze-out cogenesis,” JHEP 03
(2022) 031, arXiv:2112.10784 [hep-ph].
[60] D. Mahanta and D. Borah, “WIMPy leptogenesis in non-standard cosmologies,”
JCAP 03 (2023) 049, arXiv:2208.11295 [hep-ph].
[61] J. Heisig, “Conversion-Driven Leptogenesis: A Testable Theory of Dark Matter and
Baryogenesis at the Electroweak Scale,” Phys. Rev. Lett. 133 no. 19, (2024) 191803,
arXiv:2404.12428 [hep-ph].
[62] Y. Cui and M. Shamma, “WIMP Cogenesis for Asymmetric Dark Matter and the
Baryon Asymmetry,” JHEP 12 (2020) 046, arXiv:2002.05170 [hep-ph].
[63] M. Pospelov, A. Ritz, and M. B. Voloshin, “Secluded WIMP Dark Matter,” Phys.
Lett. B 662 (2008) 53–61, arXiv:0711.4866 [hep-ph].
[64] D. Toussaint, S. B. Treiman, F. Wilczek, and A. Zee, “Matter - Antimatter
Accounting, Thermodynamics, and Black Hole Radiation,” Phys. Rev. D 19 (1979)
1036–1045.
[65] S. Weinberg, “Cosmological Production of Baryons,” Phys. Rev. Lett. 42 (1979)
850–853.
[66] D. V. Nanopoulos and S. Weinberg, “Mechanisms for Cosmological Baryon
Production,” Phys. Rev. D 20 (1979) 2484.
57

## PDF page 58

[67] E. W. Kolb and S. Wolfram, “Baryon Number Generation in the Early Universe,”
Nucl. Phys. B 172 (1980) 224. [Erratum: Nucl.Phys.B 195, 542 (1982)].
[68] S. M. Barr, “Comments on Unitarity and the Possible Origins of the Baryon
Asymmetry of the Universe,” Phys. Rev. D 19 (1979) 3803.
[69] A. Hook, “Unitarity constraints on asymmetric freeze-in,” Phys. Rev. D 84 (2011)
055003, arXiv:1105.3728 [hep-ph].
[70] J. Unwin, “Towards cogenesis via Asymmetric Freeze-In: The χ who came-in from
the cold,” JHEP 10 (2014) 190, arXiv:1406.3027 [hep-ph].
[71] K. Sigurdson, “Hidden Hot Dark Matter as Cold Dark Matter,” arXiv:0912.2346
[astro-ph.CO].
[72] S. Das and K. Sigurdson, “Cosmological Limits on Hidden Sector Dark Matter,”
Phys. Rev. D 85 (2012) 063510, arXiv:1012.4458 [astro-ph.CO].
[73] M. Blennow, E. Fernandez-Martinez, O. Mena, J. Redondo, and P. Serra,
“Asymmetric Dark Matter and Dark Radiation,” JCAP 07 (2012) 022,
arXiv:1203.5803 [hep-ph].
[74] P. N. Bhattiprolu, R. McGehee, and A. Pierce, “Dark sink enhances the direct
detection of freeze-in dark matter,” Phys. Rev. D 110 no. 3, (2024) L031702,
arXiv:2312.14152 [hep-ph].
[75] P. N. Bhattiprolu, R. McGehee, E. Petrosky, and A. Pierce, “Sub-MeV dark sink
dark matter,” Phys. Rev. D 111 no. 3, (2025) 035027, arXiv:2408.07744 [hep-ph].
[76] V. Domcke, K. Kamada, K. Mukaida, K. Schmitz, and M. Yamada, “Wash-In
Leptogenesis,” Phys. Rev. Lett. 126 no. 20, (2021) 201802, arXiv:2011.09347
[hep-ph].
[77] V. Domcke, K. Kamada, K. Mukaida, K. Schmitz, and M. Yamada, “Wash-in
leptogenesis after axion inflation,” JHEP 01 (2023) 053, arXiv:2210.06412
[hep-ph].
[78] M. A. Mojahed, K. Schmitz, and D. Wilken, “A lower bound on the right-handed
neutrino mass from wash-in leptogenesis,” arXiv:2501.07634 [hep-ph].
[79] I. Baldes, N. F. Bell, A. J. Millar, and R. R. Volkas, “Asymmetric Dark Matter and
CP Violating Scatterings in a UV Complete Model,” JCAP 1510 (2015) 048,
arXiv:1506.07521 [hep-ph].
[80] A. Goudelis, P. Papachristou, and V. C. Spanos, “Mechanism for baryogenesis via
feebly interacting massive particles,” Phys. Rev. D 105 no. 4, (2022) 043521,
arXiv:2111.05740 [hep-ph].
[81] A. Goudelis, D. Karamitros, P. Papachristou, and V. C. Spanos, “Ultraviolet freeze-in
baryogenesis,” Phys. Rev. D 106 no. 2, (2022) 023515, arXiv:2204.13554 [hep-ph].
[82] T. Blazek, P. Matak, J. Ramaj, and M. Sabova, “Minimal effective theory for
leptogenesis, dark matter, and neutrino masses,” arXiv:2504.15164 [hep-ph].
58

## PDF page 59

[83] B. Shuve and D. Tucker-Smith, “Baryogenesis and Dark Matter from Freeze-In,”
Phys. Rev. D 101 no. 11, (2020) 115023, arXiv:2004.00636 [hep-ph].
[84] I. Flood, R. Porto, J. Schlesinger, B. Shuve, and M. Thum, “Hidden-sector neutrinos
and freeze-in leptogenesis,” Phys. Rev. D 105 no. 9, (2022) 095025,
arXiv:2109.10908 [hep-ph].
[85] J. Berman, B. Shuve, and D. Tucker-Smith, “Freeze-in leptogenesis via dark-matter
oscillations,” Phys. Rev. D 105 no. 9, (2022) 095027, arXiv:2201.11502 [hep-ph].
[86] E. K. Akhmedov, V. A. Rubakov, and A. Y. Smirnov, “Baryogenesis via neutrino
oscillations,” Phys. Rev. Lett. 81 (1998) 1359–1362, arXiv:hep-ph/9803255.
[87] I. Baldes, N. F. Bell, K. Petraki, and R. R. Volkas, “Particle-antiparticle asymmetries
from annihilations,” Phys. Rev. Lett. 113 no. 18, (2014) 181601, arXiv:1407.4566
[hep-ph].
[88] I. Baldes, N. F. Bell, A. Millar, K. Petraki, and R. R. Volkas, “The role of CP
violating scatterings in baryogenesis - case study of the neutron portal,” JCAP 11
(2014) 041, arXiv:1410.0108 [hep-ph].
[89] T. Banks and N. Seiberg, “Symmetries and Strings in Field Theory and Gravity,”
Phys. Rev. D 83 (2011) 084019, arXiv:1011.5120 [hep-th].
[90] DESI Collaboration, A. G. Adame et al., “DESI 2024 VI: cosmological constraints
from the measurements of baryon acoustic oscillations,” JCAP 02 (2025) 021,
arXiv:2404.03002 [astro-ph.CO].
[91] S. Y. Khlebnikov and M. E. Shaposhnikov, “The Statistical Theory of Anomalous
Fermion Number Nonconservation,” Nucl. Phys. B 308 (1988) 885–912.
[92] M. D’Onofrio, K. Rummukainen, and A. Tranberg, “Sphaleron Rate in the Minimal
Standard Model,” Phys. Rev. Lett. 113 no. 14, (2014) 141602, arXiv:1404.3565
[hep-ph].
[93] T. Bringmann, S. Heeba, F. Kahlhoefer, and K. Vangsnes, “Freezing-in a hot bath:
resonances, medium effects and phase transitions,” JHEP 02 (2022) 110,
arXiv:2111.14871 [hep-ph].
[94] P. Gondolo and G. Gelmini, “Cosmic abundances of stable particles: Improved
analysis,” Nucl. Phys. B 360 (1991) 145–179.
[95] J. Edsjo and P. Gondolo, “Neutralino relic density including coannihilations,” Phys.
Rev. D 56 (1997) 1879–1894, arXiv:hep-ph/9704361.
[96] R. E. Cutkosky, “Singularities and discontinuities of Feynman amplitudes,” J. Math.
Phys. 1 (1960) 429–433.
[97] M. L. Graesser, I. M. Shoemaker, and L. Vecchi, “Asymmetric WIMP dark matter,”
JHEP 10 (2011) 110, arXiv:1103.2771 [hep-ph].
[98] H. Iminniyaz, M. Drees, and X. Chen, “Relic Abundance of Asymmetric Dark
Matter,” JCAP 07 (2011) 003, arXiv:1104.5548 [hep-ph].
59

## PDF page 60

[99] P. Adshead, Y. Cui, and J. Shelton, “Chilly Dark Sectors and Asymmetric
Reheating,” JHEP 06 (2016) 016, arXiv:1604.02458 [hep-ph].
[100] E. Hardy and J. Unwin, “Symmetric and Asymmetric Reheating,” JHEP 09 (2017)
113, arXiv:1703.07642 [hep-ph].
[101] P. Adshead, P. Ralegankar, and J. Shelton, “Reheating in two-sector cosmology,”
JHEP 08 (2019) 151, arXiv:1906.02755 [hep-ph].
[102] L. Kofman, A. D. Linde, and A. A. Starobinsky, “Reheating after inflation,” Phys.
Rev. Lett. 73 (1994) 3195–3198, arXiv:hep-th/9405187.
[103] L. Kofman, A. D. Linde, and A. A. Starobinsky, “Towards the theory of reheating
after inflation,” Phys. Rev. D 56 (1997) 3258–3295, arXiv:hep-ph/9704452.
[104] G. N. Felder, L. Kofman, and A. D. Linde, “Instant preheating,” Phys. Rev. D 59
(1999) 123523, arXiv:hep-ph/9812289.
[105] J. Martin, C. Ringeval, and V. Vennin, “Cosmic Inflation at the crossroads,” JCAP
07 (2024) 087, arXiv:2404.10647 [astro-ph.CO].
[106] A. Albrecht, P. J. Steinhardt, M. S. Turner, and F. Wilczek, “Reheating an
Inflationary Universe,” Phys. Rev. Lett. 48 (1982) 1437.
[107] A. D. Dolgov and A. D. Linde, “Baryon Asymmetry in Inflationary Universe,” Phys.
Lett. B 116 (1982) 329.
[108] L. F. Abbott, E. Farhi, and M. B. Wise, “Particle Production in the New
Inflationary Cosmology,” Phys. Lett. B 117 (1982) 29.
[109] J. McDonald, “Warm Dark Matter via Ultra-Violet Freeze-In: Reheating
Temperature and Non-Thermal Distribution for Fermionic Higgs Portal Dark
Matter,” JCAP 08 (2016) 035, arXiv:1512.06422 [hep-ph].
[110] S.-L. Chen and Z. Kang, “On UltraViolet Freeze-in Dark Matter during Reheating,”
JCAP 05 (2018) 036, arXiv:1711.02556 [hep-ph].
[111] K. Kaneta, Y. Mambrini, and K. A. Olive, “Radiative production of nonthermal dark
matter,” Phys. Rev. D 99 no. 6, (2019) 063508, arXiv:1901.04449 [hep-ph].
[112] M. A. G. Garcia, K. Kaneta, Y. Mambrini, and K. A. Olive, “Reheating and
Post-inflationary Production of Dark Matter,” Phys. Rev. D 101 no. 12, (2020)
123507, arXiv:2004.08404 [hep-ph].
[113] J. Ren and H.-J. He, “Probing Gravitational Dark Matter,” JCAP 03 (2015) 052,
arXiv:1410.6436 [hep-ph].
[114] M. Garny, M. Sandora, and M. S. Sloth, “Planckian Interacting Massive Particles as
Dark Matter,” Phys. Rev. Lett. 116 no. 10, (2016) 101302, arXiv:1511.03278
[hep-ph].
[115] Y. Ema, K. Nakayama, and Y. Tang, “Production of Purely Gravitational Dark
Matter,” JHEP 09 (2018) 135, arXiv:1804.07471 [hep-ph].

60

## PDF page 61

[116] Y. Mambrini and K. A. Olive, “Gravitational Production of Dark Matter during
Reheating,” Phys. Rev. D 103 no. 11, (2021) 115009, arXiv:2102.06214 [hep-ph].
[117] H. E. Haber and H. A. Weldon, “Thermodynamics of an Ultrarelativistic Bose Gas,”
Phys. Rev. Lett. 46 (1981) 1497.
[118] H. E. Haber and H. A. Weldon, “Finite Temperature Symmetry Breaking as
Bose-Einstein Condensation,” Phys. Rev. D 25 (1982) 502.
[119] E. W. Kolb and M. S. Turner, The Early Universe, vol. 69. Addison-Wesley, 1990.
[120] V. A. Rubakov and D. S. Gorbunov, Introduction to the Theory of the Early
Universe: Hot big bang theory. World Scientific, Singapore, 2017.
[121] J. A. Harvey and M. S. Turner, “Cosmological baryon and lepton number in the
presence of electroweak fermion number violation,” Phys. Rev. D 42 (1990)
3344–3349.
[122] S. Davidson and A. Ibarra, “A Lower bound on the right-handed neutrino mass from
leptogenesis,” Phys. Lett. B 535 (2002) 25–32, arXiv:hep-ph/0202239.
[123] G. Mangano, G. Miele, S. Pastor, T. Pinto, O. Pisanti, and P. D. Serpico, “Relic
neutrino decoupling including flavor oscillations,” Nucl. Phys. B 729 (2005) 221–234,
arXiv:hep-ph/0506164.
[124] M. Cielo, M. Escudero, G. Mangano, and O. Pisanti, “Neff in the Standard Model at
NLO is 3.043,” Phys. Rev. D 108 no. 12, (2023) L121301, arXiv:2306.05460
[hep-ph].
[125] CMB-S4 Collaboration, K. N. Abazajian et al., “CMB-S4 Science Book, First
Edition,” arXiv e-prints (10, 2016) , arXiv:1610.02743 [astro-ph.CO].
[126] J. L. Feng, H. Tu, and H.-B. Yu, “Thermal Relics in Hidden Sectors,” JCAP 10
(2008) 043, arXiv:0808.2318 [hep-ph].
[127] X. Chu, T. Hambye, and M. H. Tytgat, “The Four Basic Ways of Creating Dark
Matter Through a Portal,” JCAP 05 (2012) 034, arXiv:1112.0493 [hep-ph].
[128] S. Tulin and H.-B. Yu, “Dark Matter Self-interactions and Small Scale Structure,”
Phys. Rept. 730 (2018) 1–57, arXiv:1705.02358 [hep-ph].
[129] Z. Maki, M. Nakagawa, and S. Sakata, “Remarks on the unified model of elementary
particles,” Prog. Theor. Phys. 28 (1962) 870–880.
[130] B. Pontecorvo, “Neutrino Experiments and the Problem of Conservation of Leptonic
Charge,” Sov. Phys. JETP 26 (1968) 984–988.
[131] Hyper-Kamiokande Collaboration, K. Abe et al., “Hyper-Kamiokande Design
Report,” arXiv:1805.04163 [physics.ins-det].
[132] DUNE Collaboration, B. Abi et al., “Deep Underground Neutrino Experiment
(DUNE), Far Detector Technical Design Report, Volume II: DUNE Physics,”
arXiv:2002.03005 [hep-ex].

61

## PDF page 62

[133] T. Hambye, Y. Lin, A. Notari, M. Papucci, and A. Strumia, “Constraints on neutrino
masses from leptogenesis models,” Nucl. Phys. B 695 (2004) 169–191,
arXiv:hep-ph/0312203.
[134] J. Lesgourgues and S. Pastor, “Massive neutrinos and cosmology,” Phys. Rept. 429
(2006) 307–379, arXiv:astro-ph/0603494.
[135] J. Schechter and J. W. F. Valle, “Neutrinoless Double beta Decay in SU(2) x U(1)
Theories,” Phys. Rev. D 25 (1982) 2951.
[136] M. J. Dolinski, A. W. P. Poon, and W. Rodejohann, “Neutrinoless Double-Beta
Decay: Status and Prospects,” Ann. Rev. Nucl. Part. Sci. 69 (2019) 219–251,
arXiv:1902.04097 [nucl-ex].
[137] M. Agostini, G. Benato, J. A. Detwiler, J. Menéndez, and F. Vissani, “Toward the
discovery of matter creation with neutrinoless ββ decay,” Rev. Mod. Phys. 95 no. 2,
(2023) 025002, arXiv:2202.01787 [hep-ex].
[138] F. Vissani, “Do experiments suggest a hierarchy problem?,” Phys. Rev. D 57 (1998)
7027–7030, arXiv:hep-ph/9709409.
[139] A. de Gouvea, D. Hernandez, and T. M. P. Tait, “Criteria for Natural Hierarchies,”
Phys. Rev. D 89 no. 11, (2014) 115005, arXiv:1402.2658 [hep-ph].
[140] Y. Cui and Z.-Z. Xianyu, “Probing Leptogenesis with the Cosmological Collider,”
Phys. Rev. Lett. 129 no. 11, (2022) 111301, arXiv:2112.10793 [hep-ph].
[141] “NIST Digital Library of Mathematical Functions,” https://dlmf.nist.gov/,
Release 1.2.2 of 2024-09-15. https://dlmf.nist.gov/. F. W. J. Olver, A. B. Olde
Daalhuis, D. W. Lozier, B. I. Schneider, R. F. Boisvert, C. W. Clark, B. R. Miller,
B. V. Saunders, H. S. Cohl, and M. A. McClain, eds.

62
