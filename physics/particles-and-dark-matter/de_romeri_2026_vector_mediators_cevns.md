Source: https://arxiv.org/abs/2603.00554v1
PDF sha256: a7ea2e567860e9d2bff527e03d44aef365e1ffee8cdc7215655658a82cc8e8a3
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of de_romeri_2026_vector_mediators_cevns.pdf

Transcription of `de_romeri_2026_vector_mediators_cevns.pdf` in this directory, 24 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-24 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Testing light and heavy vector mediators
with solar CEνNS measurements
Valentina De Romeri ,1, a Dimitrios K. Papoulias ,2, b Federica
Pompa ,3, c Gonzalo Sanchez Garcia ,4, d and Christoph A. Ternes 5, 3, e

arXiv:2603.00554v1 [hep-ph] 28 Feb 2026

1

Instituto de Fı́sica Corpuscular (IFIC), CSIC-Universitat de Valéncia, E-46980 Valencia, Spain
2
Institute of Experimental Physics, University of Hamburg, 22761, Hamburg, Germany
3
Istituto Nazionale di Fisica Nucleare (INFN),
Laboratori Nazionali del Gran Sasso, 67100 Assergi, L’Aquila (AQ), Italy
4
Departamento de Fı́sica, Facultad de Ciencias,
Universidad Nacional Autónoma de México,
Apartado Postal 70-542, Ciudad de México 04510, México
5
Gran Sasso Science Institute, Viale F. Crispi 7, L’Aquila, 67100, Italy
The recent observation of coherent elastic neutrino-nucleus scattering from solar 8 B neutrinos in dark matter direct detection experiments has inaugurated the neutrino fog era,
highlighting the extended potential of these experiments as precision neutrino observatories. Recent measurements by the XENONnT, PandaX-4T, and LUX-ZEPLIN experiments
provide new opportunities to test Standard Model predictions and to probe physics beyond
it, in complementarity with dedicated neutrino facilities. We perform a combined analysis of nuclear recoil data from these three facilities to extract information on the solar 8 B
neutrino flux normalization and on the weak mixing angle at low-momentum transfer. We
further investigate the impact of new vector interactions on the solar neutrino event rate,
deriving constraints on nonstandard neutrino interactions and on scenarios with light vector
mediators. Our results demonstrate that dark matter detectors are rapidly becoming complementary to terrestrial neutrino experiments in probing neutrino interactions, and already
set competitive bounds on both light and heavy vector mediators.
Keywords: new vector interactions, dark matter detectors, solar neutrinos, CEνNS

I. INTRODUCTION

Coherent elastic neutrino–nucleus scattering (CEνNS) has recently emerged as a powerful tool
for precision tests of the Standard Model (SM) and for searches of physics beyond it. In this neutralcurrent process, a low-energy neutrino transfers momentum coherently to an entire nucleus [1].
Although theoretically predicted several decades ago [2], its observation remained experimentally
challenging for a long time. The same coherence effect that enhances the SM cross section, scaling
approximately with the square of the number of neutrons in the nuclear target, implies nuclear
recoils at the sub-keV level [3], requiring detectors with extremely low energy thresholds and
ultra-low backgrounds. The first measurement of this process was achieved by the COHERENT
collaboration [4] using pion-decay-at-rest neutrinos at a spallation source. Subsequent observations
with different targets [5–7] and reactor neutrinos [8, 9] have firmly established the process and
confirmed its coherence properties.
Remarkably, the experimental conditions required to observe CEνNS closely match those of
modern dark matter (DM) direct detection experiments [10–12]. Large target masses, low recoil
thresholds, and strong background suppression define both research programs. Ton-scale dualphase liquid xenon detectors such as XENONnT [13], LUX-ZEPLIN (LZ) [14], and PandaX-4T [15]
a

deromeri@ific.uv.es
dimitrios.papoulias@uni-hamburg.de
c
federica.pompa@lngs.infn.it
d
g.sanchez@ciencias.unam.mx
e
christoph.ternes@lngs.infn.it
b

## PDF page 2

2
have reached unprecedented sensitivities in their primary search for weakly interacting massive
particles. Although no conclusive DM signal has been observed, the continuous reduction of energy
thresholds has opened sensitivity to astrophysical neutrinos. In particular, high-energy solar 8 B
neutrinos can now induce detectable CEνNS events in these detectors. This development marks
the practical onset of the so-called neutrino fog [16–21], in which neutrino-induced nuclear recoils
constitute an irreducible background for DM searches. At the same time, it transforms DM facilities
into precision neutrino observatories, probing neutrino properties in a regime complementary to
dedicated neutrino experiments (see, e.g., [21–47]).
This transition has now materialized experimentally. With their latest exposures, the XENONnT
[48], PandaX-4T [49], and LZ [50] collaborations have reported the first indications of nuclear recoils consistent with CEνNS from solar 8 B neutrinos. In the case of XENONnT and PandaX-4T,
the background-only hypothesis is disfavored at nearly three standard deviations, while LZ reports
a 4.5σ significance. These measurements represent the first evidence of CEνNS on a xenon target
and the first observation of solar neutrino–induced nuclear recoils in DM experiments. Interpreted
within the SM, the extracted 8 B flux is consistent with solar model predictions [51] and with results from dedicated neutrino observatories [52]. Beyond confirming SM expectations, these results
establish DM direct detection experiments as a new precision frontier for neutrino physics. They
have already motivated phenomenological studies addressing nonstandard neutrino interactions
(NSI) [43, 53–55], new light mediators [44, 45, 56, 57], electromagnetic properties [42], and the
determination of electroweak parameters at low-momentum transfer [45, 50, 57, 58]. As exposures
continue to increase, solar CEνNS measurements at DM facilities are expected to play a central
role in testing neutrino interactions and physics beyond the SM, as anticipated in earlier studies
(see, e.g., Refs. [26, 27, 40, 59–64]).
In this work, we investigate the implications of the recent observation of 8 B solar CEνNS events
in DM direct detection experiments through a combined spectral analysis of the nuclear-recoil data
reported by XENONnT [48], PandaX-4T [49], and LZ [50]. We first extract determinations of the
8 B solar neutrino flux normalization and of the weak mixing angle at low-momentum transfer, exploiting the complementarity of the three experiments. We then explore the impact of new neutrino
interactions, considering both neutrino NSI described by effective point-like vector operators and
scenarios with a light vector mediator. While these possibilities have previously been studied in the
context of DM detectors (see, e.g., [27, 40, 59, 61, 65]), here we update and extend those analyses
by confronting them with the latest solar CEνNS data. For NSI, we allow for both flavor-conserving
and flavor-violating couplings and consistently include matter effects in the Sun, accounting for
their impact on neutrino propagation and flavor conversion. For light mediators, instead, we focus on flavor-diagonal scenarios, namely a universal coupling framework and an extension of the
SM with a gauged B − L symmetry, so that solar neutrino oscillations remain unaltered and new
physics effects arise solely at detection. We compare the resulting bounds with those obtained
from terrestrial CEνNS experiments [66–72] and neutrino oscillation experiments [70], demonstrating the complementarity and competitive sensitivity of our present 8 B solar-neutrino CEνNS–based
constraints.
The paper is organized as follows. In Sec. II we review neutrino propagation in the Sun and the
CEνNS cross section in the SM as well as how it is modified in the presence of new interactions with
heavy or light vector mediators. The statistical treatment of the LZ data is described in Sec. III;
for the analysis of XENONnT and PandaX-4T data we rely on our previous work [57]. Results are
presented in Sec. IV, and conclusions are finally given in Sec. V.

## PDF page 3

3
II. THEORETICAL FRAMEWORK AND CROSS SECTIONS

The presence of new vector interactions can modify the detection rate of solar neutrinos in two
distinct ways. First, the presence of NSI introduces additional contributions to the matter potential,
thus altering neutrino flavor evolution inside the Sun. This modifies the flavor composition of the
solar neutrino flux (νe , νµ , and ντ ) that reaches the detector. Second, the new interactions directly
effect detection by contributing to the CEνNS cross section. Second, the new, possibly flavordependent, interactions directly affect detection by contributing to the CEνNS cross section.
In this section, we first discuss how heavy, purely vector mediators modify neutrino oscillation
probabilities through their impact on the solar matter potential. We then examine their effect
on the weak nuclear charge entering the CEνNS cross section, considering both heavy and light
mediators. We emphasize that the light mediator scenarios considered in this work are flavor
diagonal and therefore do not alter neutrino flavor conversion in the Sun.
A.

Neutrino nonstandard interactions and light vector mediators

Neutrino NSI provide a convenient and model-independent framework to parametrize the effects
of heavy new physics in neutrino processes at low energies. In particular, heavy vector mediators
appearing in many extensions of the SM, such as extra neutral gauge bosons, induce effective
dimension-six four-fermion operators that modify neutrino neutral-current (NC) interactions. In
this work we focus on operators leading to purely vector interactions.
In the presence of NSI, the NC Lagrangian is modified as [73–75]
∑ qX
√
LNSI
εℓℓ′ (ν̄ℓ γ µ PL νℓ′ ) (q̄γµ PX q) ,
(1)
NC = −2 2 GF
q,ℓ,ℓ′ ,X

where q = {u, d} denotes first-generation quarks, ℓ, ℓ′ label neutrino flavors, and PX with X = L, R
are the chirality projectors. The dimensionless parameters εqX
ℓℓ′ quantify the strength of NSI relative
to the Fermi constant, GF , and they can be either flavor conserving (ℓ = ℓ′ , possibly non-universal)
or flavor changing (ℓ ̸= ℓ′ ). In this work, we focus on the vector part of the interaction given by
qL
qR
εqV
ℓℓ′ = εℓℓ′ + εℓℓ′ . Note that, in principle, axial-vector combinations can also be formed, according
qA
qL
to εℓℓ′ = εℓℓ′ − εqR
ℓℓ′ . However, since axial-vector interactions do not modify the matter potential in
the Sun, and since the axial contribution to the CEνNS cross section is small, we do not consider
them in this work. The propagation of neutrinos in a medium is actually only sensitive to the
combinations
εℓℓ′ = εeV
ℓℓ′ +

Nu uV
Nd dV
εℓℓ′ +
ε ′ ,
Ne
Ne ℓℓ

(2)

where εeV
ℓℓ′ indicates a nonstandard interaction with electrons while Ne , Nu and Nd are the number
densities of electrons, u-quarks and d-quarks, respectively. Note also that in this work we do not
address NSI with electrons, which have been recently studied in [70, 76]. Since in this work we
study, in addition to neutrino propagation, effects of NSI on the CEνNS cross section, we focus
only on NSI with u- or d-quarks.
Note that the parametrization in Eq. (1) is not gauge-invariant1 . In general, gauge invariance
would imply that NC NSI are accompanied by analogous operators in the charged lepton sector, which are tightly constrained by experimental data [79, 80]. However, these bounds can be
1

One possibility, not explored here, is to expand this formalism to all gauge invariant dimension-six operators using
an effective field theory approach (see, for instance, [55, 77, 78]).

## PDF page 4

4
significantly relaxed in new physics scenarios where NSI arise from the exchange of light neutral
mediators with masses well below the electroweak scale (see, e.g., [81–84] and the review [85]). In
such cases, large NSI strengths leading to observable effects in current experiments become viable.
Motivated by this model realizations of such new interactions, it seems convenient to extend our
analysis to scenarios in which the new vector interaction is mediated by a light particle (with a
mass mV comparable to the typical momentum transfer in this process, O ∼ 10 MeV). In this case,
the Lagrangian is given by
1
1
L ⊃ − Vµν V µν + m2V Vµ V µ + Vµ (gνV ν̄α γ µ PL να + gqV q̄γ µ q) ,
4
2

(3)

where the coupling between neutrinos (quarks) and the new mediator V is given by gνV (gνV ), and
Vµν = ∂µ Vν − ∂ν Vµ .
B. Neutrino propagation in the Sun

In the presence of NSI, neutrino flavor evolution in matter is governed by the effective Hamiltonian
HNSI = H0 +

√









qV
qV
εqV
1 0 0
ee εeµ εeτ
∑
 √

 qV qV qV 
2GF Ne 0 0 0 + 2GF
Nq εeµ εµµ εµτ  ,
qV
qV
q
0 0 0
εqV
eτ εµτ ετ τ

(4)

where H0 = 2E1 ν U diag(0, ∆m221 , ∆m231 )U † is the vacuum Hamiltonian, with U the PMNS mixing
matrix, and Eν the neutrino energy. The second term corresponds to the standard matter potential,
while the third term encodes NC NSI with first-generation quarks (q = u, d), weighted by their
number densities Nq . In our analysis, the solar oscillation parameters are fixed to the values
recently reported by JUNO [86]. The remaining oscillation parameters are taken from Ref. [87],
except for the atmospheric mixing angle, for which we adopt sin2 θ23 = 0.5, consistent with current
global fits [87–89]. This choice implies equal muon and tau flavor components in the solar neutrino
flux at Earth. Note that, in principle, the non-diagonal parameters in the matrix in the last term
can be complex. Here, however, we consider only real NSI. We have numerically verified that,
including CP-phases or simply allowing for the non-diagonal parameters to take negative values
produces the same bounds on the NSI parameters.
For solar neutrinos, adiabatic
√ flavor conversion probabilities can be computed in the mass2
dominance limit, ∆m31 ≫ 2 2GF Ne Eν , where the matter potential is small compared to the
atmospheric mass-squared splitting. In this regime, the three-flavor evolution effectively reduces
to a two-flavor problem (see, e.g., [59, 70]). The electron-neutrino survival probability can then be
written as [90]
Pee (Eν , r) = cos4 θ13 Peff (Eν , r) + sin4 θ13 ,

(5)

where r = R/R⊙ is the production point inside the Sun in units of the solar radius, R⊙ . The
effective two-flavor probability is given by the Parke formula [91]
Peff (Eν , r) =

1
[1 + cos(2θM ) cos(2θ12 )] ,
2

(6)

where θM is the effective mixing angle in matter,
cos(2θM ) = √

∆m221 cos(2θ12 ) − A
(∆m221 cos(2θ12 ) − A)2 + (∆m221 cos(2θ12 ) + B)2

.

(7)

## PDF page 5

5
The NSI effects on the matter potential are present through the parameters A and B, defined as
(
)
√
cos2 θ13 ∑ Nq (r) q
−
εD ,
(8)
A = 4 2Eν GF Ne (r)
2
q Ne (r)
∑
√
B = 4 2Eν GF
Nq (r)εqN .
(9)
q

The effective NSI combinations entering solar neutrino propagation are given by (with cij ≡ cos θij
and sij ≡ sin θij ) [70, 92]
c2
s223 − s213 c223 qV
qV
εqD = − 13 (εqV
−
ε
)
+
(ετ τ − εqV
µµ
µµ )
2 ee
2
qV
2
qV
+ s13 c13 (s23 εqV
eµ + c23 εeτ ) − (1 + s13 )c23 s23 εµτ ,

(10)

qV
qV
qV
2
2
qV
εqN = s13 c23 s23 (εqV
τ τ − εµµ ) + c13 (c23 εeµ − s23 εeτ ) + s13 (s23 − c23 )εµτ .

(11)

Finally, the survival probability must be averaged over the spatial distribution of 8 B production
region inside the Sun2 . The oscillation probabilities at Earth are therefore given by
∫ 1

ρB (r) Peff (Eν , r) dr ,

(12)

Peµ (Eν ) = (1 − Pee (Eν )) cos2 θ23 ,

(13)

Pee (Eν ) =

0

2

Peτ (Eν ) = (1 − Pee (Eν )) sin θ23

(14)

where
ρB (r) denotes the normalized radial distribution of 8 B neutrino production, satisfying
∫1
0 ρB (r) dr = 1, and is taken from Ref. [93]. The differential flux of neutrinos of flavor νℓ at
the detector is then
dϕℓ
dϕ0
=
Peℓ (Eν ) ,
(15)
dEν
dEν
where dϕ0 /dEν is the unoscillated 8 B solar neutrino flux, taken from Refs. [94, 95], with total
normalization fixed to 5.46 × 106 cm−2 s−1 as given in [51, 96] for the high-metallicity B16-GS98
model.
The approach outlined above is valid only under the assumption of adiabatic neutrino evolution
in the interior of the Sun. This condition is always satisfied within the standard three-neutrino
oscillation paradigm, but it may be violated in the presence of large NSI. In our analysis, we follow
the procedure suggested in Ref. [70]: we determine the regions in the (εqD , εqN ) parameter space
for NSI with u- and d-quarks where adiabaticity may fail, and verify whether any combinations of
εqV
ℓℓ′ considered in our study lie within those regions. We find that, in our combined analysis, no
parameter points lead to non-adiabatic evolution3 . Therefore, the use of the adiabatic approach is
fully justified in our analysis.
C. CEνNS cross sections
1.

CEνNS cross section in the Standard Model

Within the SM, the differential cross section for CEνNS with respect to the nuclear recoil energy,
TN , can be written as [2, 97]
dσνℓ N ∣∣
G2 mN ( SM )2 2
mN TN
= F
QV,ℓ FW (|q|2 ) 1 −
∣
dTN SM
π
2Eν2
∣

2

(

)

,

(16)

We have verified that the contribution from hep neutrinos is negligible, while all other solar neutrino components
do not yield nuclear recoils within our region of interest.
3
For the analysis of PandaX-4T data alone, some parameter points may lie in non-adiabatic regions. However, since
the combined results are dominated by LZ data, we consistently adopt the adiabatic approximation throughout.

## PDF page 6

6
where mN is the nuclear mass. In the previous expression, we neglected terms that are suppressed
by TN /mN and higher-order contributions of O(TN2 ). The quantity QSM
V,ℓ represents the SM weak
vector charge of the nucleus, defined as
p
n
QSM
V,ℓ = gV,ℓ Z + gV,ℓ N,

(17)

with Z and N being the proton and neutron number, respectively. At tree level, the corresponding
p
n = −1/2 for neutrons,
vector couplings are given by gV,ℓ
= (1/2 − 2 sin2 θW )/2 for protons and gV,ℓ
while in the SM the flavor dependence becomes only relevant beyond tree level, see e.g. Ref. [98].
Through the proton term, the weak charge depends explicitly on the weak mixing angle, whose
value at low energies is obtained by renormalization group evolution from the Z-pole value and
corresponds to sin2 θW = 0.23857(5) [99].
The effects of the nuclear target structure are encoded in the weak nuclear form factor FW (|q|2 ),
which accounts for the finite spatial extent of the nucleus. For CEνNS induced by 8 B solar neutrinos,
the typical momentum transfer is sufficiently small that the form-factor suppression is modest. In
our numerical analysis, we adopt the Klein-Nystrand parametrization [100]
j1 (|q| RA )
FW (|q| ) = 3
|q| RA
2

(

1
1 + |q|2 a2k

)

,

(18)

where j1 (x) = sin x/x2 −cos x/x is the spherical Bessel function of first order, ak = 0.7 fm, and RA =
1.23 A1/3 (in fm) denotes the nuclear root-mean-square radius, with A the
√ atomic mass number.
The momentum transfer relevant for CEνNS can be estimated as |q| = 2mN TN /197.327 fm−1 ,
corresponding to a characteristic scale of O(10) MeV.
2.

CEνNS cross section with NSI

NSI lead to a flavor-dependent modification of the SM weak charge defined in Eq. (17), such
2
NSI 2
that (QSM
V,ℓ ) → (QV,ℓ ) with [97]
(

QNSI
V,ℓ

)2

=
+

[(

)

(

)

p
dV
n
dV
gV,ℓ
+ 2εuV
Z + gV,ℓ
+ εuV
N
ℓℓ + εℓℓ
ℓℓ + 2εℓℓ

]2

)
(
) ∣2
∑ ∣∣(
∣
dV
uV
dV
∣ 2εuV
ℓℓ′ + εℓℓ′ Z + εℓℓ′ + 2εℓℓ′ N ∣ .

(19)

ℓ′ ̸=ℓ

For an incoming νℓ , the CEνNS cross section must be appropriately weighted by the relevant
neutrino energy flux following Eq. (15).
3.

CEνNS cross section in presence of new light vector mediators

In the presence of a light vector mediator of mass mV , the CEνNS cross section is modified
to [101]
∣

[

dσνℓ N ∣∣
CV
(Eν , TN ) = 1 + κ √
( 2
)
∣
SM
dTN V
2GF QV,ℓ mV + 2mN TN

]2

∣

dσνℓ N ∣∣
,
dTN ∣SM

(20)

where the squared bracket explicitly accounts for the interference between the SM amplitude and
the contribution induced by the new interaction.
Assuming universal quark couplings, the effective coupling to the nucleus is encoded in the
coefficient CV ≡ 3AgV2 = 3AgνV gqV , with gνV and gqV denoting the fundamental couplings of

## PDF page 7

7
the vector mediator to neutrinos and quarks, respectively. The factor κ accounts for the specific
U (1)′ charge assignments of the model under consideration. We restrict ourselves to flavor-diagonal
interactions and consider two benchmark scenarios: (i) a phenomenological model with universal
couplings, for which κ = 1, and (ii) a B − L extension of the SM [102, 103], characterized by
κ = −1/3. While the universal-coupling scenario is not anomaly-free and is introduced here purely
as an effective description, it allows for destructive interference with the SM contribution. In
contrast, in the B − L model only constructive interference is possible.
III.

DATA ANALYSIS

The analyses of XENONnT and PandaX-4T data follow what was described in Refs. [42, 57].
The analysis of the paired prompt scintillation (S1) and delayed electroluminescence (S2) signals
in LZ data [50] follows a similar approach. The differential event rate is defined as
max

Eν
∑ dϕℓ dσν N
dR
ℓ
dEν
= E (TN )
,
min
dTN
dE
dT
Eν
ν
N
ℓ=e,µ,τ

∫

(21)

dσ

dϕℓ
ℓN
where dE
is the (oscillated) νℓ flux at the detector, dTνN
the CEνNS cross section, and E (TN ) the
ν
detector efficiency provided by the LZ Collaboration
[50].
The lower integration limit depends on
√
the nuclear recoil energy and reads as Eνmin = mN TN /2, while Eνmax is defined by the endpoint of
the neutrino energy distribution, Eνmax ≈ 16 MeV in the case of 8 B neutrinos. As for XENONnT,
the LZ data are presented in bins of S2 [50]. Then, the number of events per bin i is given by

Ri = E

dR
dn ,
i dn

∫

(22)

where E = 5.7 t×yr is the exposure achieved so far by the LZ experiment. Within the experimental
region of interest (ROI) and following [50], we consider 5 bins between [155, 645] photons detected
(phd), which correspond to nuclear recoil energies of [1, 6] keV. The differential event rate in
Eq. (22) is then expressed via a change of variables
dR dTN
dR
=
,
dn
dTN dn

(23)

where the translation between the nuclear recoil energy and the S2 signal is given by
n ≡ S2 = g2 TN Qy (TN ) ,

(24)

with g2 = 34.0 phd/electron, and the charge yield Qy (TN ) taken from [50].
The total number of predicted events for LZ in each bin i is given by
Ni = Ri (1 + α) + BiAC (1 + β) ,

(25)

where the spectrum of the dominant accidental coincidence (AC) background, BiAC , is provided by
the Collaboration [50]. Through a combined analysis of both ionization and scintillation signals,
LZ has observed 19 events in the ROI. We compare our predictions with the measured data Di
using
{ [
2

χ = min 2
α,β

(

Di
Ni − Di + Di ln
Ni
i

∑

)]

(

+

α
σα

)2

(

+

β
σβ

)2 }

.

(26)

Here, α (β) is a nuisance parameter with σα = 12% (σβ = 30%) accounting for the 8 B flux
prediction (the normalization of the AC background component).

## PDF page 8

8
10
XENONnT
PandaX-4T
LZ
combined

∆χ2

8

B16-AGSS09met (Low Metallicity)
B16-GS98 (High Metallicity)
SNO (2013)

6

PandaX-4T (JCAP 05 (2025) 012)

4

XENONnT (JCAP 05 (2025) 012)
LZ (this result)

2

Xe combined (this result)

0
0.0 2.5 5.0 7.5 10.0 12.5 15.0 17.5 20.0
8

B neutrino flux [106 cm−2 s−1]

1

2

3

4
8

5

6

7

8

9

10

11

12

13

14

15

B neutrino flux [106 cm−2 s−1]

FIG. 1: Left panel: The ∆χ2 profiles for the determination of the 8 B solar neutrino flux for
PandaX-4T (dotted green), XENONnT (dashed blue), LZ (dot-dashed orange), and the combined
analysis (solid magenta). Right panel: 8 B solar neutrino flux determination from our individual
and combined analyses of solar CEνNS data, in comparison with other experimental
measurements from neutral-current reactions [48–50, 52, 96], as well as predictions from low- and
high-metallicity solar models [51]. The superimposed dotted bars represent the official flux
determinations as reported by each Collaboration.
IV. RESULTS

In the following we discuss the results of our analyses of SM physics in Sec. IV A, neutrino NSI
in Sec. IV B, and new light vector mediators in Sec. IV C.
A.

SM physics: 8 B flux and weak mixing angle

The recent CEνNS measurements from DM direct detection experiments provide a simultaneous
test of the prediction for the 8 B neutrino flux from Standard Solar Models (SSMs) and of the SM
prediction for the weak mixing angle, sin2 θW .
Regarding the determination of the 8 B flux, the three Collaborations report results consistent
with the predictions from SSMs and with previous dedicated solar neutrino experiments. At 68%
8
+3.1
+2.1
6
−2 s−1 from XENONnT,
confidence level (CL), they obtain ΦνB = (4.7+3.6
−2.3 , 8.4−3.1 , 3.1−1.3 )×10 cm
PandaX-4T and LZ data, respectively. In deriving our results, we assume the SM prediction for the
CEνNS cross section, fixing sin2 θW = 0.23857 [99]. The corresponding ∆χ2 profiles are displayed
in the left panel of Fig. 1. The green dotted and blue dashed curves represent the PandaX-4T
and XENONnT results, previously presented in [57] (see also the complementary analysis in [45]),
while the orange dot-dashed curve shows the new LZ analysis. The solid magenta line determines
their combined result. At 1σ, our individual and combined analyses give
8

6
−2 −1
ΦνB = (7.7+7.0
−5.9 ) × 10 cm s
8B

6
−2 −1
Φν = (5.7+3.2
−2.8 ) × 10 cm s
8B

6
−2 −1
Φν = (3.5+2.2
−2.2 ) × 10 cm s
8
6
−2 −1
ΦνB = (4.3+1.3
−1.3 ) × 10 cm s

(PandaX-4T) ,

(27)

(XENONnT) ,

(28)

(LZ) ,

(29)

(combined) .

(30)

We report these determinations in the right panel of Fig. 1 as green, blue, orange, and magenta
error bars, respectively. For completeness and ease of comparison, we also display as dotted error

## PDF page 9

9

APV

EW
(PDG2024) combined

0.20

2

Dresden-II

SM

4

0.25

(reactor CEνNS)

6

CONUS+
(reactor CEνNS)

0.30

sin2θW

∆χ2

8

Xe Combined

XENONnT
PandaX-4T
LZ
combined

(solar CEνNS)

10

SLAC E158
(ee)

LEP I
Qweak

eDIS

(ep)

Tevatron SLC

LHC

COHERENT CsI+LAr
(π-DAR CEνNS)

0.15

0
0.0

0.1

0.2

0.3

0.4

0.5

10−3

10−2

10−1

2

100

101

102

103

µ [GeV]

sin θW

FIG. 2: Left panel: The ∆χ2 profiles for the determination of the weak mixing angle for
PandaX-4T (dotted green), XENONnT (dashed blue), LZ (dot-dashed orange), and the combined
analysis (solid magenta). The dashed vertical line corresponds to the expected value of sin2 θW
within the SM. Right panel: Our 1σ combined CEνNS measurement, together with the ones from
other experiments at different energy scales [69, 99, 106–114]. The running of the weak mixing
angle as defined in the MS renormalization scheme [104, 105] is also shown (gray dashed line).

bars the official results quoted by each of the Collaborations. Our extracted flux normalizations
are consistent with the measurement from SNO [52], also shown in the same panel, as well as with
the predictions of both low- and high-metallicity solar models [51].
The observation of CEνNS in DM direct detection experiments also enables a determination
of the weak mixing angle, sin2 θW , at low-momentum transfer. In this case, we fix the neutrino
8
flux normalization to ΦνB = 5.46 × 106 cm−2 s−1 [51, 96] with a corresponding 12% uncertainty to
account for the residual flux normalization error. In addition to the PandaX-4T and XENONnT
results already presented in [57] (see also [45, 58]), we extract the 1σ best-fit value for LZ and
compute the combined determination from the three experiments. The corresponding ∆χ2 profiles
are shown in the left panel of Fig. 2, with the same color code applied before. Our 1σ results give
sin2 θW = 0.30+0.16
−0.21

(PandaX-4T) ,

(31)

sin θW = 0.25+0.09
−0.10
2
sin θW = 0.17+0.06
−0.06
2
sin θW = 0.20+0.05
−0.06

(XENONnT) ,

(32)

(LZ) ,

(33)

(combined) .

(34)

2

The right panel of Fig. 2 shows the combined best-fit value together with its associated 1σ uncertainty band. The gray dashed curve represents the renormalization group evolution of sin2 θW in
the MS scheme [104, 105], while other experimental constraints at different energy scales are also
indicated [69, 99, 106–114]. As can be seen, the determination from DM direct detection experiments is becoming competitive with those obtained from reactor experiments such as CONUS+ [72]
and Dresden-II [106] (see also Ref. [115]). A more precise constraint is achieved by the combined
analysis of COHERENT CsI and LAr data [69], although at a somewhat higher energy scale due
to the different neutrino source. Overall, the observation of neutrinos via the CEνNS channel in
DM direct detection experiments provides, as a by-product, a valuable test of a fundamental SM
parameter.

## PDF page 10

1.0

1.0

0.5

0.5
ϵdV
αα

ϵdV
ee

10

0.0

0.0

90% CL

−0.5
−1.0
−1.0

90% CL

XENONnT
PandaX-4T
LZ
combined

−0.5

−0.5

0.0
ϵuV
ee

0.5

1.0

−1.0
−1.0

α=e
α=µ
α=τ

−0.5

0.0
ϵuV
αα

0.5

1.0

dV
FIG. 3: Left panel: 90% CL contours in the (ϵuV
ee , ϵee ) plane. All the other NSI parameters are
fixed to zero. Green, blue and orange lines refer to PandaX-4T, XENONnT and LZ, respectively,
while the pink region corresponds to their combined result. Right panel: 90% CL contours from
dV
the combined analysis in the diagonal (ϵuV
αα , ϵαα ) plane, with α = e, µ, τ in shaded pink, green and
blue color, respectively, and all the other NSI parameters fixed to zero.

B. Neutrino NSI

We present in this section the constraints on neutrino NSI obtained from the individual and
combined analyses of XENONnT, PandaX-4T and LZ. For simplicity, we first consider two nonzero
dV
NSI parameters at a time. We show in the left panel of Fig. 3 the 90% CL contours in the (ϵuV
ee , ϵee )
parameter space. The results are illustrated for the individual and combined analyses, which turns
out to be dominated by the LZ data. The constraints obtained from the combined XENONnT
+ PandaX-4T + LZ analysis are competitive with existing ones from COHERENT CsI+LAr [69]
and CONUS+ [72]. The right panel of Fig. 3 shows a comparison of the three NSI planes involving
uV dV
uV dV
dV
diagonal NSI couplings, (ϵuV
ee , ϵee ), (ϵµµ , ϵµµ ) and (ϵτ τ , ϵτ τ ). In this case, only the combined
constraints are shown. The solar 8 B neutrino-induced CEνNS data provide sensitivity to the ϵqV
ττ
NSI parameters, which are not accessible in measurements at spallation-source or reactor facilities.
The access to the ϵqV
τ τ channel makes DM direct detection facilities a great addition to dedicated
CEνNS experiments.
From here on, we will consider NSI with either u- or d-quarks. In Fig. 4 we show the 90%
uV
dV
dV
CL bounds on the (εuV
ee , εµµ ) (left panel) and the (εee , εµµ ) (right panel) parameter space, while
fixing all the other NSI parameters to zero. Again, the combined analysis is driven by LZ. In
both panels, we also indicate the regions compatible with the so-called LMA-dark solution [116],
characterized by sin2 θ12 > 0.5 and sizeable NSI contributions. In the presence of sufficiently large
NSI, the symmetry of the effective Hamiltonian under a simultaneous flip of the mass ordering
and the θ12 octant can be restored through an appropriate sign change in the matter potential.
Assuming NSI with either u- or d-quarks only, our combined analysis excludes the parameter space
required to realize the LMA-dark solution at more than 3σ. This result is consistent with previous
studies [43, 117, 118], which have highlighted the increasing tension of the LMA-dark scenario in
light of recent CEνNS data. We stress, however, that this conclusion does not necessarily extend
to scenarios with light mediators, where the phenomenology can differ significantly [119].
Finally, we consider all the NSI as free parameters in the analysis and present marginalized
constraints. Figure 5 shows the result of our combined analysis of XENONnT, PandaX-4T and LZ
data, assuming NSI with u-quarks only. Each panel displays a two-dimensional projection onto a

## PDF page 11

11
1.0

1.0
0.5

ϵdV
µµ

ϵuV
µµ

LM

0.0

−1.0
−1.0

A-

90% CL

XENONnT
PandaX-4T
LZ
combined

−0.5

LM

0.0

90% CL

−0.5

rk

da

0.5

k
ar

d
A-

−0.5

0.0
ϵuV
ee

0.5

1.0

−1.0
−1.0

XENONnT
PandaX-4T
LZ
combined

−0.5

0.0
ϵdV
ee

0.5

1.0

qV
FIG. 4: 90% CL contours in the (ϵqV
ee , ϵµµ ) plane, with q = u (d) in the left panel (right panel).
Green, blue and orange lines refer to PandaX-4T, XENONnT and LZ, respectively, while the
pink region corresponds to their combined result. We report here in gray also the parameter
space region compatible with the LMA-dark solution.

pair of NSI parameters, with the allowed regions shown at 1σ, 2σ, and 3σ (from darker to lighter
blue). All remaining NSI parameters are profiled over in each projection. The corresponding onedimensional reduced χ2 profiles are shown in Fig. 6 for each of the εuV
αβ . We present both the
individual constraints from XENONnT, PandaX-4T, and LZ as well as the combined one. The
corresponding allowed 1σ intervals are summarized in the upper half of Table I. Note that we do
not observe the double-minimum structure frequently reported in other similar works. This feature
typically arises in analyses where only one NSI parameter is varied at a time. In contrast, when
all NSI parameters and their correlations are consistently included, degeneracies arise, resulting
in the relatively flat profiles displayed in the figure. We have verified that, when allowing for
only one NSI parameter at the time, the sensitivity improves and two minima become apparent,
although their significance remain low. This behavior is also reflected in Fig. 3, where a single
allowed band is obtained instead of two separate bands. We understand this is a consequence
of the low statistical significance of current solar CEνNS data and it can be improved with the
accumulation of more statistics. The combined bounds derived here are mostly driven by the
LZ result, and they are comparable in strength to those obtained from analyses of COHERENT
data [66, 69, 120, 121], although they remain weaker than the constraints achieved in global fits
combining multiple dedicated neutrino experiments, in particular from oscillations [70].
The results of the analogous analysis assuming NSI with d-quarks are presented in Figs. 7
and 8, with the corresponding 1σ intervals summarized in the lower half of Table I. The qualitative
conclusions closely mirror those obtained in the u-quark case: the allowed regions exhibit similar
structures, and a flat profile appears once all parameter correlations are taken into account. Since
for xenon the number of neutrons exceeds the number of protons in the targets, the bounds on
NSI with d-quarks are in general slightly more stringent than those with u-quarks. This is also
manifested in less pronounced contour shapes, as visible in Fig. 7. Moreover, while our results
confirm and complement previous analyses of solar CEνNS data [43, 45, 53, 54], a direct comparison
(even focusing on the XENONnT and PandaX-4T datasets only) is not straightforward. The main
differences stem from our use of a full spectral analysis and from the fact that we simultaneously
vary and profile over all relevant NSI parameters, consistently accounting for their correlations. In
addition, a key novelty of our work is the inclusion of the recent LZ data, which strengthens and
updates the overall constraints.

## PDF page 12

12

Combined analysis
XENONnT + PandaX-4T + LZ

ϵuV
µµ

0.5

1σ
2σ
3σ

0.0
−0.5

ϵuV
ττ

0.5
0.0

−0.5

ϵuV
eµ

0.5
0.0
−0.5

ϵuV
eτ

0.5
0.0

−0.5

ϵuV
µτ

0.5
0.0
−0.5
−0.5 0.0 0.5 −0.5 0.0 0.5 −0.5 0.0 0.5 −0.5 0.0 0.5 −0.5 0.0 0.5

ϵuV
ee

ϵuV
µµ

ϵuV
ττ

ϵuV
eµ

ϵuV
eτ

FIG. 5: The allowed regions at 1σ, 2σ and 3σ for 2 degrees of freedom for all pairs of NSI
parameters with u-quarks from the combined XENONnT + PandaX-4T + LZ analysis. In each
panel, we minimize with respect to all other NSI parameters that are not shown.

C. Light vector mediators

We finally discuss the constraints obtained from our combined analysis in the presence of light
vector mediators. We show our results in Fig. 9, comparing them with other existing constraints.
We report in magenta our 90% CL constraints of the combined XENONnT + PandaX-4T + LZ
CEνNS analysis for the vector universal (left panel) and B − L (right panel) mediators. We also
show existing constraints from other CEνNS data from COHERENT [69, 122], CONNIE [123, 124],
CONUS [125, 126], and CONUS+ [9, 72, 127]. Furthermore, we include limits from elastic neutrinoelectron scattering data at BOREXINO [71], CHARM-II [128], and TEXONO [128, 129], and
from a combined analysis of PandaX-4T, XENONnT, and LZ electron recoil data [37, 130]. We

## PDF page 13

13
10

10

3σ

XENONnT
PandaX-4T
LZ
Combined

∆χ2

8
6
4
2

2σ

0
−1.0

∆χ2

10

8

8

6

6

4
2

1σ

−0.5

0.0

0.5

ϵuV
ee

2σ

4
2

1σ

0
1.0 −1.0
10

3σ

10

3σ

−0.5

0.0

0.5

ϵuV
µµ

8

8

8

6

6

6

4
2

2σ

4
2

1σ

0
−1.0

−0.5

0.0

ϵuV
eµ

0.5

2σ

4
2

1σ

0
1.0 −1.0

−0.5

0.0

ϵuV
eτ

0.5

2σ

1σ

0
1.0 −1.0
10

3σ

3σ

−0.5

0.0

0.5

1.0

0.5

1.0

ϵuV
ττ

3σ

2σ

1σ

0
1.0 −1.0

−0.5

0.0

ϵuV
µτ

FIG. 6: ∆χ2 profiles of all NSI parameters with u-quarks from the combined XENONnT +
PandaX-4T + LZ analysis. The results for the individual analysis of each experiment are also
depicted. In each panel, we minimize with respect to all other NSI parameters that are not shown.
Parameter
LZ
XENONnT PandaX-4T
Combined
ϵuV
[-0.126,
0.558]
[-0.211,
0.646]
[-0.302,
0.809]
[-0.136,
0.557]
ee
uV
[-0.126, 0.605] [-0.218, 0.779] [-0.342, 0.944] [-0.125, 0.622]
ϵµµ
[-0.143, 0.573] [-0.243, 0.759] [-0.381, 0.942] [-0.143, 0.572]
ϵuV
ττ
uV
[-0.241, 0.234] [-0.311, 0.304] [-0.403, 0.391] [-0.241, 0.234]
ϵeµ
[-0.243, 0.247] [-0.315, 0.319] [-0.405, 0.411] [-0.243, 0.247]
ϵuV
eτ
ϵuV
[-0.299, 0.237] [-0.418, 0.304] [-0.545, 0.399] [-0.305, 0.237]
µτ
dV
ϵee
[-0.116, 0.496] [-0.205, 0.590] [-0.276, 0.715] [-0.119, 0.496]
ϵdV
[-0.111, 0.473] [-0.199, 0.564] [-0.315, 0.758] [-0.111, 0.473]
µµ
dV
ϵτ τ
[-0.128, 0.496] [-0.220, 0.596] [-0.341, 0.756] [-0.127, 0.495]
ϵdV
[-0.214, 0.209] [-0.279, 0.272] [-0.362, 0.349] [-0.214, 0.209]
eµ
dV
ϵeτ
[-0.217, 0.222] [-0.282, 0.287] [-0.362, 0.372] [-0.217, 0.222]
ϵdV
[-0.219, 0.210] [-0.293, 0.274] [-0.431, 0.356] [-0.219, 0.210]
µτ

TABLE I: The 1σ limits for NSI with u-quarks and d-quarks obtained in this analysis.
further show exclusions from NA64 [131–133] and other fixed-target and beam-dump experiments,
which include E137 [134], E141 [135], KEK [136], E774 [137], Orsay [138–140], and ν-CAL I [141–
144], CHARM [145, 146], NOMAD [147], PS191 [148, 149], A1 [150], and APEX [151], and from
colliders BaBar [152, 153] and LHCb [154]. Astrophysical and cosmological probes place important
constraints on light mediators. While these limits depend strongly on the underlying model and
would require a dedicated study for precise determination, we highlight with Neff the parameter

## PDF page 14

14

Combined analysis
XENONnT + PandaX-4T + LZ

ϵdV
µµ

0.5

1σ
2σ
3σ

0.0
−0.5

ϵdV
ττ

0.5
0.0

−0.5

ϵdV
eµ

0.5
0.0
−0.5

ϵdV
eτ

0.5
0.0

−0.5

ϵdV
µτ

0.5
0.0
−0.5
−0.5 0.0 0.5 −0.5 0.0 0.5 −0.5 0.0 0.5 −0.5 0.0 0.5 −0.5 0.0 0.5

ϵdV
ee

ϵdV
µµ

ϵdV
ττ

ϵdV
eµ

ϵdV
eτ

FIG. 7: Same as Fig. 5, but for NSI with d-quarks.
regions that could be incompatible with BBN [155–157] and CMB [158] observations. Regions
disfavored by supernova measurements are instead indicated by SN1987A [159–163].
We find that, in the universal vector scenario, the constraint is largely driven by XENONnT and
therefore closely resembles the bound previously reported in Ref. [57]. In contrast, in the gauged
B − L framework, the sensitivity is dominated by the recent LZ data. This behaviour can be traced
back to the fact that the LZ CEνNS measurement lies slightly below the SM expectation. As a
result, scenarios such as B − L, where the new contribution interferes constructively with the SM
amplitude and enhances the event rate, are stronger constrained by LZ; See Appendix A for more
details. In both models, the resulting bounds are comparable in strength to those obtained from
other neutrino scattering experiments for mediator masses mV >
∼ 10 MeV. For lighter mediators,
however, constraints from elastic neutrino–electron scattering become significantly more stringent.
Our findings are consistent with previous studies, most notably Refs. [43–45], which also explored
new light mediators in light of the XENONnT and PandaX-4T CEνNS data. In this respect, our

## PDF page 15

15
10

10

3σ

XENONnT
PandaX-4T
LZ
Combined

∆χ2

8
6
4
2

2σ

0
−1.0

∆χ2

10

8

8

6

6

4
2

1σ

−0.5

0.0

0.5

ϵdV
ee

2σ

4
2

1σ

0
1.0 −1.0
10

3σ

10

3σ

−0.5

0.0

0.5

ϵdV
µµ

8

8

8

6

6

6

4
2

2σ

4
2

1σ

0
−1.0

−0.5

0.0

ϵdV
eµ

0.5

2σ

4
2

1σ

0
1.0 −1.0

−0.5

0.0

0.5

ϵdV
eτ

2σ

1σ

0
1.0 −1.0
10

3σ

3σ

−0.5

0.0

0.5

1.0

0.5

1.0

ϵdV
ττ

3σ

2σ

1σ

0
1.0 −1.0

−0.5

0.0

ϵdV
µτ

FIG. 8: Same as Fig. 6, but for NSI with d-quarks.

analysis again extends the existing literature by incorporating the recent LZ nuclear-recoil results,
thereby providing a comprehensive and up-to-date picture.
Within the universal vector scenario, it is also important to stress that an analysis based on a
single dataset (XENONnT, LZ, or PandaX-4T alone) is not sufficient to lift the intrinsic parameter
degeneracy. Individually, each experiment allows for a narrow, unconstrained strip in the whole
parameter space (with the exception of PandaX-4T which is presently not sensitive enough to
resolve this strip, see, e.g., Ref. [57] and Appendix A) corresponding to an exact degeneracy in the
total cross section, which cannot be excluded by that dataset alone. As detailed in Appendix A,
only the combined analysis of all three experiments is able to resolve this degeneracy and reduce the
allowed region; eventually, only combining datasets with different target materials or improving
recoil energy sensitivity in a single experiment would allow to fully probe it. Remarkably, the
resulting limits are already competitive with those obtained from dedicated CEνNS experiments
such as COHERENT and CONUS+. The results shown here assume universal couplings of the
light mediator to quarks and electrons, a well-motivated benchmark scenario. If this universality
assumption is relaxed, the present bounds, together with other CEνNS-based constraints, can
become the dominant limits in the mediator mass range mV ≃ 20–200 MeV.

V.

CONCLUSIONS

The recent detection of 8 B solar neutrinos via the CEνNS channel at DM direct detection
facilities marks the entry of these experiments into the so-called neutrino fog. On one hand, such
solar neutrino signals slow down progress through the DM parameter space, the primary goal of
these experiments. On the other hand, their detection via neutral-current nuclear scattering opens

## PDF page 16

16

universal vector

10−2
10−3

10−3

10

Babar

CO
CHARM
CONUS

R
HE
CO

4

6
NA

TEXONO
+
US
Borexino

90% CL

N
CO

−7

LHCb

10−4

CHARM

LZ
T+
)
Xn
X+ Eν ES
Pn
(

LHCb

PnX + XnT + LZ (CEνNS)

10−5

N
ERE

+

S
NU
CO

64

NA

TEXONO

Borexino
Z

10

90% CL

T

COH

10−6

beam dump

Babar

−7

L
T+
Xn )
X + Eν ES
Pn
(

Neff

PnX + XnT + LZ
(CEνNS)

T
EN

Neff

gV

10−6

E

gB−L

I
NN

10−4
10−5

vector B − L

10−2

beam dump

SN1987A

10−8 −5
10

10−4

10−3

10−2

10−1

100

101

10−8 −5
10

mV [GeV]

10−4

10−3

10−2

10−1

100

101

mV [GeV]

FIG. 9: 90% CL excluded regions (magenta shaded areas) from combined CEνNS solar data
(XENONnT + PandaX-4T + LZ) for universal vector (left panel) and vector B − L (right panel)
interactions. Existing bounds from other searches are shown for comparison.

up new phenomenological research directions and enables the opportunity to employ current and
future DM facilities as neutrino observatories.
Motivated by these recent experimental results, we build upon previous analyses to investigate
their impact on both SM parameters and potential new physics. We perform a combined spectral
analysis of CEνNS data collected by the XENONnT, PandaX-4T, and LZ experiments and extract
a determination of the solar 8 B neutrino flux normalization. Our results, both for individual
datasets and the combined analysis, are in good agreement with the official values reported by the
Collaborations, demonstrating the robustness of our statistical approach.
We further determine the weak mixing angle, a key SM parameter, at low energies, illustrating
the power of DM facilities to perform precision SM tests and thereby significantly expanding their
physics reach beyond their primary goal. Additionally, we explore the potential of these measurements to probe new neutrino interactions mediated by both heavy and light vector mediators. Our
results show that DM direct detection experiments provide complementary constraints to dedicated
neutrino facilities, yielding competitive bounds on nonstandard effective vector interactions as well
as on the mass and coupling of light vector mediators, including universal and B − L scenarios.
In conclusion, our work demonstrates that solar neutrino signals in DM detectors transform
these experiments into competitive probes of both the SM and new physics, highlighting their
evolving role as versatile observatories in astroparticle physics.

ACKNOWLEDGMENTS

We thank Mariam Tórtola for helpful discussions. V.D.R. acknowledges financial support by the
grant CIDEXG/2022/20 (from Generalitat Valenciana) and by the Spanish grants CNS2023-144124
(MCIN/AEI/10.13039/501100011033 and “Next Generation EU”/PRTR), PID2023-147306NBI00, and CEX2023-001292-S (MCIU/AEI/10.13039/501100011033). D.K.P. acknowledges funding
from the European Union’s Horizon Europe research and innovation programme under the Marie
Sklodowska-Curie Actions grant agreement No. 101198541 (neutrinoSPHERE). G.S.G. has been
supported by Sistema Nacional de Investigadoras e Investigadores (SNII, México) and by SECIHTI
Project No. CBF-2025-I-1589.

## PDF page 17

17

universal vector

10−2

gB−L

10−3

gV

10−3
90% CL

10

vector B − L

10−2

−4

10

XENONnT
PandaX-4T
LZ
combined

10−5 −3
10

10−2

10−1

mV [GeV]

100

90% CL

101

−4

10−5 −3
10

XENONnT
PandaX-4T
LZ
combined

10−2

10−1

100

101

mV [GeV]

FIG. 10: 90% CL exclusion limits for universal (left panel) and B − L vector (right panel)
interactions. Blue, green and orange lines correspond to XENONnT, PandaX-4T and LZ bounds,
respectively, while the magenta refers to the combined exclusion region.
Appendix A: Individual bounds on light vector mediators

The individual 90% CL bounds in the mediator mass-coupling plane, obtained from each experiment are displayed in Fig. 10 for the universal (left panel) and B − L (right panel) vector
interactions. The improvement resulting from the new LZ data is particularly notable in the case
of the B − L model. The shapes of the constraints can be understood as follows:
√ for light media2 2GF mN QSM TN

V,ℓ
tors (mV ≪ |q|), a saturation of the depicted constrains happens for gV2 = −
, i.e.
3Aκ
the constraint depends only on the coupling. On the other hand, in the heavy mediator regime
(mV ≫ |q|),
the constraints appear as straight lines with positive slope and depend on the ratio
√
2
gV
m2V

2GF QSM

= − 3Aκ V,ℓ . Moreover, in the case of the universal vector model, a full degeneracy of the
cross section occurs for
CV
√
(A1)
( 2
) = −2 .
SM
2GF QV,ℓ mV + 2mN TN
It is interesting to notice that an individual analysis of LZ, PandaX-4T or XENONnT data is not
sufficient to break the degeneracy. However, this becomes possible via a combined analysis of all
the available data performed in the present work, see e.g. the magenta exclusion regions, without
necessarily the need of recurring to different target materials. The parameter space region where
the destructive interference occurs is indeed dependent on the N/Z ratio typical of the target
material [122, 164].

[1] M. Abdullah et al., “Coherent elastic neutrino-nucleus scattering: Terrestrial and astrophysical
applications,” arXiv:2203.07361 [hep-ph].
[2] D. Z. Freedman, “Coherent Neutrino Nucleus Scattering as a Probe of the Weak Neutral Current,”
Phys. Rev. D 9 (1974) 1389–1392.
[3] A. Drukier and L. Stodolsky, “Principles and Applications of a Neutral Current Detector for
Neutrino Physics and Astronomy,” Phys. Rev. D 30 (1984) 2295.
[4] COHERENT Collaboration, D. Akimov et al., “Observation of Coherent Elastic Neutrino-Nucleus
Scattering,” Science 357 (2017) 1123–1126, arXiv:1708.01294 [nucl-ex].

## PDF page 18

18
[5] COHERENT Collaboration, D. Akimov et al., “First Measurement of Coherent Elastic
Neutrino-Nucleus Scattering on Argon,” Phys. Rev. Lett. 126 no. 1, (2021) 012002,
arXiv:2003.10630 [nucl-ex].
[6] COHERENT Collaboration, D. Akimov et al., “Measurement of the Coherent Elastic
Neutrino-Nucleus Scattering Cross Section on CsI by COHERENT,” Phys. Rev. Lett. 129 (2022)
081801, arXiv:2110.07730 [hep-ex].
[7] S. Adamski et al., “First detection of coherent elastic neutrino-nucleus scattering on germanium,”
arXiv:2406.13806 [hep-ex].
[8] J. Colaresi, J. I. Collar, T. W. Hossbach, C. M. Lewis, and K. M. Yocum, “Measurement of Coherent
Elastic Neutrino-Nucleus Scattering from Reactor Antineutrinos,” Phys. Rev. Lett. 129 no. 21, (2022)
211802, arXiv:2202.09672 [hep-ex].
[9] N. Ackermann et al., “Direct observation of coherent elastic antineutrino–nucleus scattering,” Nature
643 no. 8074, (2025) 1229–1233, arXiv:2501.05206 [hep-ex].
[10] M. W. Goodman and E. Witten, “Detectability of Certain Dark Matter Candidates,” Phys. Rev. D
31 (1985) 3059.
[11] M. Schumann, “Direct Detection of WIMP Dark Matter: Concepts and Status,” J. Phys. G 46
no. 10, (2019) 103003, arXiv:1903.03026 [astro-ph.CO].
[12] J. Billard et al., “Direct detection of dark matter—APPEC committee report*,” Rept. Prog. Phys. 85
no. 5, (2022) 056201, arXiv:2104.07634 [hep-ex].
[13] XENON Collaboration, E. Aprile et al., “First Dark Matter Search with Nuclear Recoils from the
XENONnT Experiment,” Phys. Rev. Lett. 131 no. 4, (2023) 041003, arXiv:2303.14729 [hep-ex].
[14] LZ Collaboration, J. Aalbers et al., “First Dark Matter Search Results from the LUX-ZEPLIN (LZ)
Experiment,” Phys. Rev. Lett. 131 no. 4, (2023) 041002, arXiv:2207.03764 [hep-ex].
[15] PandaX Collaboration, Z. Bo et al., “Dark Matter Search Results from 1.54 Tonne·Year Exposure of
PandaX-4T,” Phys. Rev. Lett. 134 no. 1, (2025) 011805, arXiv:2408.00664 [hep-ex].
[16] C. A. J. O’Hare, “New Definition of the Neutrino Floor for Direct Dark Matter Searches,” Phys. Rev.
Lett. 127 no. 25, (2021) 251802, arXiv:2109.03116 [hep-ph].
[17] J. Monroe and P. Fisher, “Neutrino Backgrounds to Dark Matter Searches,” Phys. Rev. D 76 (2007)
033007, arXiv:0706.3019 [astro-ph].
[18] J. D. Vergados and H. Ejiri, “Can Solar Neutrinos be a Serious Background in Direct Dark Matter
Searches?,” Nucl. Phys. B 804 (2008) 144–159, arXiv:0805.2583 [hep-ph].
[19] L. E. Strigari, “Neutrino Coherent Scattering Rates at Direct Dark Matter Detectors,” New J. Phys.
11 (2009) 105011, arXiv:0903.3630 [astro-ph.CO].
[20] J. Billard, L. Strigari, and E. Figueroa-Feliciano, “Implication of neutrino backgrounds on the reach
of next generation dark matter direct detection experiments,” Phys. Rev. D 89 no. 2, (2014) 023524,
arXiv:1307.5458 [hep-ph].
[21] V. De Romeri, A. Majumdar, D. K. Papoulias, and R. Srivastava, “New light mediators and the
neutrino fog: Implications from XENONnT nuclear recoil data,” arXiv:2512.08853 [hep-ph].
[22] R. Harnik, J. Kopp, and P. A. N. Machado, “Exploring nu Signals in Dark Matter Detectors,” JCAP
07 (2012) 026, arXiv:1202.6073 [hep-ph].
[23] M. Atzori Corona, W. M. Bonivento, M. Cadeddu, N. Cargioli, and F. Dordei, “New constraint on
neutrino magnetic moment and neutrino millicharge from LUX-ZEPLIN dark matter search results,”
Phys. Rev. D 107 no. 5, (2023) 053001, arXiv:2207.05036 [hep-ph].
[24] A. de Gouvêa, E. McGinness, I. Martinez-Soler, and Y. F. Perez-Gonzalez, “pp solar neutrinos at
DARWIN,” Phys. Rev. D 106 no. 9, (2022) 096017, arXiv:2111.02421 [hep-ph].
[25] C. Giunti and C. A. Ternes, “Testing neutrino electromagnetic properties at current and future dark
matter experiments,” Phys. Rev. D 108 no. 9, (2023) 095044, arXiv:2309.17380 [hep-ph].
[26] D. G. Cerdeño, M. Fairbairn, T. Jubb, P. A. N. Machado, A. C. Vincent, and C. Bœhm, “Physics
from solar neutrinos in dark matter direct detection experiments,” JHEP 05 (2016) 118,
arXiv:1604.01025 [hep-ph]. [Erratum: JHEP 09, 048 (2016)].
[27] B. Dutta, S. Liao, L. E. Strigari, and J. W. Walker, “Non-standard interactions of solar neutrinos in
dark matter experiments,” Phys. Lett. B 773 (2017) 242–246, arXiv:1705.00661 [hep-ph].
[28] G. B. Gelmini, V. Takhistov, and S. J. Witte, “Geoneutrinos in Large Direct Detection
Experiments,” Phys. Rev. D 99 no. 9, (2019) 093009, arXiv:1812.05550 [hep-ph].

## PDF page 19

19
[29] R. Essig, M. Sholapurkar, and T.-T. Yu, “Solar Neutrinos as a Signal and Background in
Direct-Detection Experiments Searching for Sub-GeV Dark Matter With Electron Recoils,” Phys.
Rev. D 97 no. 9, (2018) 095029, arXiv:1801.10159 [hep-ph].
[30] C. Boehm, D. G. Cerdeno, M. Fairbairn, P. A. N. Machado, and A. C. Vincent, “Light new physics
in XENON1T,” Phys. Rev. D 102 (2020) 115013, arXiv:2006.11250 [hep-ph].
[31] D. Aristizabal Sierra, V. De Romeri, L. J. Flores, and D. K. Papoulias, “Light vector mediators
facing XENON1T data,” Phys. Lett. B 809 (2020) 135681, arXiv:2006.12457 [hep-ph].
[32] D. Aristizabal Sierra, R. Branada, O. G. Miranda, and G. Sanchez Garcia, “Sensitivity of direct
detection experiments to neutrino magnetic dipole moments,” JHEP 12 (2020) 178,
arXiv:2008.05080 [hep-ph].
[33] D. W. P. d. Amaral, D. G. Cerdeno, P. Foldenauer, and E. Reid, “Solar neutrino probes of the muon
anomalous magnetic moment in the gauged U(1)Lµ −Lτ ,” JHEP 12 (2020) 155, arXiv:2006.11225
[hep-ph].
[34] B. Dutta, R. F. Lang, S. Liao, S. Sinha, L. Strigari, and A. Thompson, “A global analysis strategy to
resolve neutrino NSI degeneracies with scattering and oscillation data,” JHEP 09 (2020) 106,
arXiv:2002.03066 [hep-ph].
[35] A. M. Suliga and I. Tamborra, “Astrophysical constraints on nonstandard coherent neutrino-nucleus
scattering,” Phys. Rev. D 103 no. 8, (2021) 083002, arXiv:2010.14545 [hep-ph].
[36] D. W. P. Amaral, D. G. Cerdeno, A. Cheek, and P. Foldenauer, “Confirming U (1)Lµ −Lτ as a solution
for (g − 2)µ with neutrinos,” Eur. Phys. J. C 81 no. 10, (2021) 861, arXiv:2104.03297 [hep-ph].
[37] V. De Romeri, D. K. Papoulias, and C. A. Ternes, “Light vector mediators at direct detection
experiments,” JHEP 05 (2024) 165, arXiv:2402.05506 [hep-ph].
[38] J. Aalbers et al., “A next-generation liquid xenon observatory for dark matter and neutrino physics,”
J. Phys. G 50 no. 1, (2023) 013001, arXiv:2203.02309 [physics.ins-det].
[39] D. Alonso-González, D. W. P. Amaral, A. Bariego-Quintana, D. Cerdeño, and M. de los Rios,
“Measuring the sterile neutrino mass in spallation source and direct detection experiments,” JHEP
12 (2023) 096, arXiv:2307.05176 [hep-ph].
[40] D. W. P. Amaral, D. Cerdeno, A. Cheek, and P. Foldenauer, “A direct detection view of the neutrino
NSI landscape,” JHEP 07 (2023) 071, arXiv:2302.12846 [hep-ph].
[41] A. Majumdar, D. K. Papoulias, H. Prajapati, and R. Srivastava, “Constraining low scale Dark
Hypercharge symmetry at spallation, reactor and Dark Matter direct detection experiments,”
arXiv:2411.04197 [hep-ph].
[42] V. De Romeri, D. K. Papoulias, G. Sanchez Garcia, C. A. Ternes, and M. Tórtola, “Neutrino
electromagnetic properties and sterile dipole portal in light of the first solar CEνNS data,” JCAP 05
(2025) 080, arXiv:2412.14991 [hep-ph].
[43] J. Gehrlein and T. Kushwaha, “Testing the dark side of neutrino oscillations with the solar neutrino
fog at dark matter experiments,” Phys. Rev. D 112 no. 9, (2025) 095032, arXiv:2508.14166
[hep-ph].
[44] P. Blanco-Mas, P. Coloma, G. Herrera, P. Huber, J. Kopp, I. M. Shoemaker, and Z. Tabrizi, “Clarity
through the neutrino fog: constraining new forces in dark matter detectors,” JHEP 08 (2025) 043,
arXiv:2411.14206 [hep-ph].
[45] M. Atzori Corona, M. Cadeddu, N. Cargioli, F. Dordei, and M. Sestu, “When backgrounds become
signals: neutrino interactions in xenon-based dark matter detectors,” arXiv:2509.22178 [hep-ph].
[46] M. Demirci and M. F. Mustamin, “Solar neutrino constraints on light mediators through coherent
elastic neutrino-nucleus scattering,” Phys. Rev. D 109 no. 1, (2024) 015021, arXiv:2312.17502
[hep-ph].
[47] M. Atzori Corona, M. Cadeddu, N. Cargioli, F. Dordei, C. Giunti, and C. A. Ternes, “Standard
Model Tested with Neutrinos,” Phys. Rev. Lett. 135 no. 23, (2025) 231803, arXiv:2504.05272
[hep-ph].
[48] XENON Collaboration, E. Aprile et al., “First Indication of Solar 8 B Neutrinos via Coherent Elastic
Neutrino-Nucleus Scattering with XENONnT,” Phys. Rev. Lett. 133 (2024) 191002,
arXiv:2408.02877 [nucl-ex].
[49] PandaX Collaboration, Z. Bo et al., “First Indication of Solar B8 Neutrinos through Coherent
Elastic Neutrino-Nucleus Scattering in PandaX-4T,” Phys. Rev. Lett. 133 no. 19, (2024) 191001,
arXiv:2407.10892 [hep-ex].

## PDF page 20

20
[50] LZ Collaboration, D. S. Akerib et al., “Searches for Light Dark Matter and Evidence of Coherent
Elastic Neutrino-Nucleus Scattering of Solar Neutrinos with the LUX-ZEPLIN (LZ) Experiment,”
arXiv:2512.08065 [hep-ex].
[51] N. Vinyoles, A. M. Serenelli, F. L. Villante, S. Basu, J. Bergström, M. C. Gonzalez-Garcia,
M. Maltoni, C. Peña Garay, and N. Song, “A new Generation of Standard Solar Models,” Astrophys.
J. 835 no. 2, (2017) 202, arXiv:1611.09867 [astro-ph.SR].
[52] SNO Collaboration, B. Aharmim et al., “Combined Analysis of all Three Phases of Solar Neutrino
Data from the Sudbury Neutrino Observatory,” Phys. Rev. C 88 (2013) 025501, arXiv:1109.0763
[nucl-ex].
[53] D. Aristizabal Sierra, N. Mishra, and L. Strigari, “Implications of first neutrino-induced nuclear
recoil measurements in direct detection experiments: Probing nonstandard interaction via CEνNS,”
Phys. Rev. D 111 no. 5, (2025) 055007, arXiv:2409.02003 [hep-ph].
[54] G. Li, C.-Q. Song, F.-J. Tang, and J.-H. Yu, “Constraints on neutrino nonstandard interactions from
COHERENT, PandaX-4T and XENONnT,” Phys. Rev. D 111 no. 3, (2025) 035002,
arXiv:2409.04703 [hep-ph].
[55] G. Li, C.-Q. Song, F.-J. Tang, and J.-H. Yu, “A Comprehensive Effective Field Theory Framework
for Coherent Elastic Neutrino-Nucleus Scattering,” arXiv:2601.19883 [hep-ph].
[56] S.-y. Xia, “Measuring Solar neutrino Fluxes in Direct Detection Experiments in the Presence of Light
Mediators,” arXiv:2410.01167 [hep-ph].
[57] V. De Romeri, D. K. Papoulias, and C. A. Ternes, “Bounds on new neutrino interactions from the
first CEνNS data at direct detection experiments,” JCAP 05 (2025) 012, arXiv:2411.11749
[hep-ph].
[58] T. N. Maity and C. Boehm, “First constraint on the weak mixing angle using direct detection
experiments,” Phys. Rev. D 112 no. 5, (2025) 053001, arXiv:2409.04385 [hep-ph].
[59] D. Aristizabal Sierra, N. Rojas, and M. H. G. Tytgat, “Neutrino non-standard interactions and dark
matter searches with multi-ton scale detectors,” JHEP 03 (2018) 197, arXiv:1712.09667 [hep-ph].
[60] M. C. Gonzalez-Garcia, M. Maltoni, Y. F. Perez-Gonzalez, and R. Zukanovich Funchal, “Neutrino
Discovery Limit of Dark Matter Direct Detection Experiments in the Presence of Non-Standard
Interactions,” JHEP 07 (2018) 019, arXiv:1803.03650 [hep-ph].
[61] D. Aristizabal Sierra, B. Dutta, S. Liao, and L. E. Strigari, “Coherent elastic neutrino-nucleus
scattering in multi-ton scale dark matter experiments: Classification of vector and scalar interactions
new physics signals,” JHEP 12 (2019) 124, arXiv:1910.12437 [hep-ph].
[62] A. Majumdar, D. K. Papoulias, and R. Srivastava, “Dark matter detectors as a novel probe for light
new physics,” Phys. Rev. D 106 no. 1, (2022) 013001, arXiv:2112.03309 [hep-ph].
[63] T. Schwemberger and T.-T. Yu, “Detecting beyond the standard model interactions of solar
neutrinos in low-threshold dark matter detectors,” Phys. Rev. D 106 no. 1, (2022) 015002,
arXiv:2202.01254 [hep-ph].
[64] E. Bertuzzo, F. F. Deppisch, S. Kulkarni, Y. F. Perez Gonzalez, and R. Zukanovich Funchal, “Dark
Matter and Exotic Neutrino Interactions in Direct Detection Searches,” JHEP 04 (2017) 073,
arXiv:1701.07443 [hep-ph].
[65] B. Dutta and L. E. Strigari, “Neutrino physics with dark matter detectors,” Ann. Rev. Nucl. Part.
Sci. 69 (2019) 137–161, arXiv:1901.08876 [hep-ph].
[66] C. Giunti, “General COHERENT constraints on neutrino nonstandard interactions,” Phys. Rev. D
101 no. 3, (2020) 035039, arXiv:1909.00466 [hep-ph].
[67] D. K. Papoulias, T. S. Kosmas, and Y. Kuno, “Recent probes of standard and non-standard neutrino
physics with nuclei,” Front. in Phys. 7 (2019) 191, arXiv:1911.00916 [hep-ph].
[68] O. G. Miranda, D. K. Papoulias, G. Sanchez Garcia, O. Sanders, M. Tórtola, and J. W. F. Valle,
“Implications of the first detection of coherent elastic neutrino-nucleus scattering (CEvNS) with
Liquid Argon,” JHEP 05 (2020) 130, arXiv:2003.12050 [hep-ph]. [Erratum: JHEP 01, 067 (2021)].
[69] V. De Romeri, O. G. Miranda, D. K. Papoulias, G. Sanchez Garcia, M. Tórtola, and J. W. F. Valle,
“Physics implications of a combined analysis of COHERENT CsI and LAr data,” JHEP 04 (2023)
035, arXiv:2211.11905 [hep-ph].
[70] P. Coloma, M. C. Gonzalez-Garcia, M. Maltoni, J. P. Pinheiro, and S. Urrea, “Global constraints on
non-standard neutrino interactions with quarks and electrons,” JHEP 08 (2023) 032,
arXiv:2305.07698 [hep-ph].

## PDF page 21

21
[71] P. Coloma, I. Esteban, M. C. Gonzalez-Garcia, L. Larizgoitia, F. Monrabal, and S. Palomares-Ruiz,
“Bounds on new physics with data of the Dresden-II reactor experiment and COHERENT,” JHEP
05 (2022) 037, arXiv:2202.10829 [hep-ph].
[72] V. De Romeri, D. K. Papoulias, and G. Sanchez Garcia, “Implications of the first CONUS+
measurement of coherent elastic neutrino-nucleus scattering,” Phys. Rev. D 111 no. 7, (2025) 075025,
arXiv:2501.17843 [hep-ph].
[73] T. Ohlsson, “Status of non-standard neutrino interactions,” Rept. Prog. Phys. 76 (2013) 044201,
arXiv:1209.2710 [hep-ph].
[74] O. G. Miranda and H. Nunokawa, “Non standard neutrino interactions: current status and future
prospects,” New J. Phys. 17 no. 9, (2015) 095002, arXiv:1505.06254 [hep-ph].
[75] Y. Farzan and M. Tortola, “Neutrino oscillations and Non-Standard Interactions,” Front. in Phys. 6
(2018) 10, arXiv:1710.09360 [hep-ph].
[76] BOREXINO Collaboration, V. Antonelli et al., “Constraints on non-standard neutrino interactions
from Borexino extended data-set,” arXiv:2602.08685 [hep-ex].
[77] V. Bresó-Pla, A. Falkowski, M. González-Alonso, and K. Monsálvez-Pozo, “EFT analysis of New
Physics at COHERENT,” JHEP 05 (2023) 074, arXiv:2301.07036 [hep-ph].
[78] P. Coloma, E. Fernández-Martı́nez, J. López-Pavón, X. Marcano, D. Naredo-Tuero, and S. Urrea,
“Improving the global SMEFT picture with bounds on neutrino NSI,” JHEP 02 (2025) 137,
arXiv:2411.00090 [hep-ph].
[79] M. B. Gavela, D. Hernandez, T. Ota, and W. Winter, “Large gauge invariant non-standard neutrino
interactions,” Phys. Rev. D 79 (2009) 013007, arXiv:0809.3451 [hep-ph].
[80] S. Antusch, J. P. Baumann, and E. Fernandez-Martinez, “Non-Standard Neutrino Interactions with
Matter from Physics Beyond the Standard Model,” Nucl. Phys. B 810 (2009) 369–388,
arXiv:0807.1003 [hep-ph].
[81] Y. Farzan and I. M. Shoemaker, “Lepton Flavor Violating Non-Standard Interactions via Light
Mediators,” JHEP 07 (2016) 033, arXiv:1512.09147 [hep-ph].
[82] Y. Farzan, “A model for large non-standard interactions of neutrinos leading to the LMA-Dark
solution,” Phys. Lett. B 748 (2015) 311–315, arXiv:1505.06906 [hep-ph].
[83] J. Heeck, M. Lindner, W. Rodejohann, and S. Vogl, “Non-Standard Neutrino Interactions and
Neutral Gauge Bosons,” SciPost Phys. 6 no. 3, (2019) 038, arXiv:1812.04067 [hep-ph].
[84] K. S. Babu, A. Friedland, P. A. N. Machado, and I. Mocioiu, “Flavor Gauge Models Below the Fermi
Scale,” JHEP 12 (2017) 096, arXiv:1705.01822 [hep-ph].
[85] Neutrino Non-Standard Interactions: A Status Report, vol. 2. 2019. arXiv:1907.00991 [hep-ph].
[86] JUNO Collaboration, A. Abusleme et al., “First measurement of reactor neutrino oscillations at
JUNO,” arXiv:2511.14593 [hep-ex].
[87] P. F. de Salas, D. V. Forero, S. Gariazzo, P. Martı́nez-Miravé, O. Mena, C. A. Ternes, M. Tórtola,
and J. W. F. Valle, “2020 global reassessment of the neutrino oscillation picture,” JHEP 02 (2021)
071, arXiv:2006.11237 [hep-ph].
[88] F. Capozzi, W. Giarè, E. Lisi, A. Marrone, A. Melchiorri, and A. Palazzo, “Neutrino masses and
mixing: Entering the era of subpercent precision,” Phys. Rev. D 111 no. 9, (2025) 093006,
arXiv:2503.07752 [hep-ph].
[89] I. Esteban, M. C. Gonzalez-Garcia, M. Maltoni, I. Martinez-Soler, J. P. Pinheiro, and T. Schwetz,
“NuFit-6.0: updated global analysis of three-flavor neutrino oscillations,” JHEP 12 (2024) 216,
arXiv:2410.05380 [hep-ph].
[90] T.-K. Kuo and J. T. Pantaleone, “The Solar Neutrino Problem and Three Neutrino Oscillations,”
Phys. Rev. Lett. 57 (1986) 1805–1808.
[91] S. J. Parke, “Nonadiabatic Level Crossing in Resonant Neutrino Oscillations,” Phys. Rev. Lett. 57
(1986) 1275–1278, arXiv:2212.06978 [hep-ph].
[92] M. C. Gonzalez-Garcia and M. Maltoni, “Determination of matter potential from global analysis of
neutrino oscillation data,” JHEP 09 (2013) 152, arXiv:1307.3092 [hep-ph].
[93] J. N. Bahcall, A. M. Serenelli, and S. Basu, “10,000 standard solar models: a Monte Carlo
simulation,” Astrophys. J. Suppl. 165 (2006) 400–431, arXiv:astro-ph/0511337.
[94] J. Bahcall. http://www.sns.ias.edu/~jnb/SNdata/sndata.html.
[95] J. N. Bahcall, E. Lisi, D. E. Alburger, L. De Braeckeleer, S. J. Freedman, and J. Napolitano,
“Standard neutrino spectrum from B-8 decay,” Phys. Rev. C 54 (1996) 411–422,

## PDF page 22

22
arXiv:nucl-th/9601044.
[96] D. Baxter et al., “Recommended conventions for reporting results from direct dark matter searches,”
Eur. Phys. J. C 81 no. 10, (2021) 907, arXiv:2105.00599 [hep-ex].
[97] J. Barranco, O. G. Miranda, and T. I. Rashba, “Probing new physics with coherent neutrino
scattering off nuclei,” JHEP 12 (2005) 021, arXiv:hep-ph/0508299.
[98] M. Cadeddu, F. Dordei, C. Giunti, Y. F. Li, E. Picciau, and Y. Y. Zhang, “Physics results from the
first COHERENT observation of coherent elastic neutrino-nucleus scattering in argon and their
combination with cesium-iodide data,” Phys. Rev. D 102 no. 1, (2020) 015030, arXiv:2005.01645
[hep-ph].
[99] Particle Data Group Collaboration, S. Navas et al., “Review of particle physics,” Phys. Rev. D 110
no. 3, (2024) 030001.
[100] S. Klein and J. Nystrand, “Exclusive vector meson production in relativistic heavy ion collisions,”
Phys. Rev. C 60 (1999) 014903, arXiv:hep-ph/9902259.
[101] P. M. Candela, V. De Romeri, P. Melas, D. K. Papoulias, and N. Saoulidou, “Up-scattering
production of a sterile fermion at DUNE: complementarity with spallation source and direct
detection experiments,” JHEP 10 (2024) 032, arXiv:2404.12476 [hep-ph].
[102] P. Langacker, “The Physics of Heavy Z ′ Gauge Bosons,” Rev. Mod. Phys. 81 (2009) 1199–1228,
arXiv:0801.1345 [hep-ph].
[103] S. Okada, “Z ′ Portal Dark Matter in the Minimal B − L Model,” Adv. High Energy Phys. 2018
(2018) 5340935, arXiv:1803.06793 [hep-ph].
[104] J. Erler and R. Ferro-Hernández, “Weak Mixing Angle in the Thomson Limit,” JHEP 03 (2018) 196,
arXiv:1712.09146 [hep-ph].
[105] J. Erler and M. J. Ramsey-Musolf, “The Weak mixing angle at low energies,” Phys. Rev. D 72 (2005)
073003, arXiv:hep-ph/0409169.
[106] A. Majumdar, D. K. Papoulias, R. Srivastava, and J. W. F. Valle, “Physics implications of recent
Dresden-II reactor data,” Phys. Rev. D 106 no. 9, (2022) 093010, arXiv:2208.13262 [hep-ph].
[107] NuTeV Collaboration, G. P. Zeller et al., “A Precise Determination of Electroweak Parameters in
Neutrino Nucleon Scattering,” Phys. Rev. Lett. 88 (2002) 091802, arXiv:hep-ex/0110059. [Erratum:
Phys.Rev.Lett. 90, 239902 (2003)].
[108] PVDIS Collaboration, D. Wang et al., “Measurement of parity violation in electron–quark
scattering,” Nature 506 no. 7486, (2014) 67–70.
[109] SLAC E158 Collaboration, P. L. Anthony et al., “Precision measurement of the weak mixing angle in
Moller scattering,” Phys. Rev. Lett. 95 (2005) 081601, arXiv:hep-ex/0504049.
[110] Qweak Collaboration, D. Androić et al., “Precision measurement of the weak charge of the proton,”
Nature 557 no. 7704, (2018) 207–211, arXiv:1905.08283 [nucl-ex].
[111] ALEPH, DELPHI, L3, OPAL, SLD, LEP Electroweak Working Group, SLD Electroweak Group,
SLD Heavy Flavour Group Collaboration, S. Schael et al., “Precision electroweak measurements on
the Z resonance,” Phys. Rept. 427 (2006) 257–454, arXiv:hep-ex/0509008.
[112] CDF, D0 Collaboration, T. A. Aaltonen et al., “Tevatron Run II combination of the effective leptonic
electroweak mixing angle,” Phys. Rev. D 97 no. 11, (2018) 112007, arXiv:1801.06283 [hep-ex].
[113] ATLAS Collaboration, G. Aad et al., “Measurement
of the forward-backward asymmetry of electron
√
and muon pair-production in pp collisions at s = 7 TeV with the ATLAS detector,” JHEP 09
(2015) 049, arXiv:1503.03709 [hep-ex].
[114] ATLAS Collaboration, “Measurement of the effective leptonic weak
mixing angle using electron and
√
muon pairs from Z-boson decay in the ATLAS experiment at s = 8 TeV,”.
[115] M. Atzori Corona, M. Cadeddu, N. Cargioli, F. Dordei, C. Giunti, Y. F. Li, C. A. Ternes, and Y. Y.
Zhang, “Impact of the Dresden-II and COHERENT neutrino scattering data on neutrino
electromagnetic properties and electroweak physics,” JHEP 09 (2022) 164, arXiv:2205.09484
[hep-ph].
[116] O. G. Miranda, M. A. Tortola, and J. W. F. Valle, “Are solar neutrino oscillations robust?,” JHEP
10 (2006) 008, arXiv:hep-ph/0406280.
[117] P. Coloma, M. C. Gonzalez-Garcia, M. Maltoni, and T. Schwetz, “COHERENT Enlightenment of
the Neutrino Dark Side,” Phys. Rev. D 96 no. 11, (2017) 115007, arXiv:1708.02899 [hep-ph].
[118] M. Chaves and T. Schwetz, “Resolving the LMA-dark NSI degeneracy with coherent
neutrino-nucleus scattering,” JHEP 05 (2021) 042, arXiv:2102.11981 [hep-ph].

## PDF page 23

23
[119] P. B. Denton, Y. Farzan, and I. M. Shoemaker, “Testing large non-standard neutrino interactions
with arbitrary mediator mass after COHERENT data,” JHEP 07 (2018) 037, arXiv:1804.03660
[hep-ph].
[120] P. Coloma, I. Esteban, M. C. Gonzalez-Garcia, and M. Maltoni, “Improved global fit to
Non-Standard neutrino Interactions using COHERENT energy and timing data,” JHEP 02 (2020)
023, arXiv:1911.09109 [hep-ph]. [Addendum: JHEP 12, 071 (2020)].
[121] V. M. Lozano, G. Sanchez Garcia, and A. Terrones, “Neutrino nonstandard interactions: Confronting
COHERENT and LHC data,” Phys. Rev. D 112 no. 5, (2025) 055017, arXiv:2503.11766 [hep-ph].
[122] M. Atzori Corona, M. Cadeddu, N. Cargioli, F. Dordei, C. Giunti, Y. F. Li, E. Picciau, C. A. Ternes,
and Y. Y. Zhang, “Probing light mediators and (g − 2)ţ through detection of coherent elastic
neutrino nucleus scattering at COHERENT,” JHEP 05 (2022) 109, arXiv:2202.11002 [hep-ph].
[123] CONNIE Collaboration, A. Aguilar-Arevalo et al., “Search for light mediators in the low-energy data
of the CONNIE reactor neutrino experiment,” JHEP 04 (2020) 054, arXiv:1910.04951 [hep-ex].
[124] CONNIE Collaboration, A. A. Aguilar-Arevalo et al., “Searches for CEνNS and Physics beyond the
Standard Model using Skipper-CCDs at CONNIE,” arXiv:2403.15976 [hep-ex].
[125] CONUS Collaboration, H. Bonet et al., “Novel constraints on neutrino physics beyond the standard
model from the CONUS experiment,” JHEP 05 (2022) 085, arXiv:2110.02174 [hep-ph].
[126] M. Lindner, T. Rink, and M. Sen, “Light vector bosons and the weak mixing angle in the light of
future germanium-based reactor CEνNS experiments,” JHEP 08 (2024) 171, arXiv:2401.13025
[hep-ph].
[127] A. Chattaraj, A. Majumdar, and R. Srivastava, “Probing standard model and beyond with reactor
CEνNS data of CONUS+ experiment,” Phys. Lett. B 864 (2025) 139438, arXiv:2501.12441
[hep-ph].
[128] M. Bauer, P. Foldenauer, and J. Jaeckel, “Hunting All the Hidden Photons,” JHEP 07 (2018) 094,
arXiv:1803.05466 [hep-ph].
[129] TEXONO Collaboration, M. Deniz et al., “Measurement of Nu(e)-bar -Electron Scattering
Cross-Section with a CsI(Tl) Scintillating Crystal Array at the Kuo-Sheng Nuclear Power Reactor,”
Phys. Rev. D 81 (2010) 072001, arXiv:0911.1597 [hep-ex].
[130] S. K. A., A. Majumdar, D. K. Papoulias, H. Prajapati, and R. Srivastava, “Implications of first LZ
and XENONnT results: A comparative study of neutrino properties and light mediators,” Phys.
Lett. B 839 (2023) 137742, arXiv:2208.06415 [hep-ph].
[131] NA64 Collaboration, Y. M. Andreev et al., “Constraints on New Physics in Electron g − 2 from a
Search for Invisible Decays of a Scalar, Pseudoscalar, Vector, and Axial Vector,” Phys. Rev. Lett. 126
no. 21, (2021) 211802, arXiv:2102.01885 [hep-ex].
[132] NA64 Collaboration, Y. M. Andreev et al., “Search for a New B-L Z’ Gauge Boson with the NA64
Experiment at CERN,” Phys. Rev. Lett. 129 no. 16, (2022) 161801, arXiv:2207.09979 [hep-ex].
[133] NA64 Collaboration, Y. M. Andreev et al., “Search for Light Dark Matter with NA64 at CERN,”
Phys. Rev. Lett. 131 no. 16, (2023) 161801, arXiv:2307.02404 [hep-ex].
[134] J. D. Bjorken, S. Ecklund, W. R. Nelson, A. Abashian, C. Church, B. Lu, L. W. Mo, T. A.
Nunamaker, and P. Rassmann, “Search for Neutral Metastable Penetrating Particles Produced in the
SLAC Beam Dump,” Phys. Rev. D 38 (1988) 3375.
[135] E. M. Riordan et al., “A Search for Short Lived Axions in an Electron Beam Dump Experiment,”
Phys. Rev. Lett. 59 (1987) 755.
[136] A. Konaka et al., “Search for Neutral Particles in Electron Beam Dump Experiment,” Phys. Rev.
Lett. 57 (1986) 659.
[137] A. Bross, M. Crisler, S. H. Pordes, J. Volk, S. Errede, and J. Wrbanek, “A Search for Shortlived
Particles Produced in an Electron Beam Dump,” Phys. Rev. Lett. 67 (1991) 2942–2945.
[138] M. Davier and H. Nguyen Ngoc, “An Unambiguous Search for a Light Higgs Boson,” Phys. Lett. B
229 (1989) 150–155.
[139] J. D. Bjorken, R. Essig, P. Schuster, and N. Toro, “New Fixed-Target Experiments to Search for
Dark Gauge Forces,” Phys. Rev. D 80 (2009) 075018, arXiv:0906.0580 [hep-ph].
[140] S. Andreas, C. Niebuhr, and A. Ringwald, “New Limits on Hidden Photons from Past Electron
Beam Dumps,” Phys. Rev. D 86 (2012) 095019, arXiv:1209.6083 [hep-ph].
[141] J. Blumlein et al., “Limits on neutral light scalar and pseudoscalar particles in a proton beam dump
experiment,” Z. Phys. C 51 (1991) 341–350.

## PDF page 24

24
[142] J. Blumlein et al., “Limits on the mass of light (pseudo)scalar particles from Bethe-Heitler e+ e- and
mu+ mu- pair production in a proton - iron beam dump experiment,” Int. J. Mod. Phys. A 7 (1992)
3835–3850.
[143] J. Blumlein and J. Brunner, “New Exclusion Limits for Dark Gauge Forces from Beam-Dump Data,”
Phys. Lett. B 701 (2011) 155–159, arXiv:1104.2747 [hep-ex].
[144] J. Blümlein and J. Brunner, “New Exclusion Limits on Dark Gauge Forces from Proton
Bremsstrahlung in Beam-Dump Data,” Phys. Lett. B 731 (2014) 320–326, arXiv:1311.3870
[hep-ph].
[145] CHARM Collaboration, F. Bergsma et al., “Search for Axion Like Particle Production in 400-GeV
Proton - Copper Interactions,” Phys. Lett. B 157 (1985) 458–462.
[146] S. N. Gninenko, “Constraints on sub-GeV hidden sector gauge bosons from a search for heavy
neutrino decays,” Phys. Lett. B 713 (2012) 244–248, arXiv:1204.3583 [hep-ph].
[147] NOMAD Collaboration, P. Astier et al., “Search for heavy neutrinos mixing with tau neutrinos,”
Phys. Lett. B 506 (2001) 27–38, arXiv:hep-ex/0101041.
[148] G. Bernardi et al., “Search for Neutrino Decay,” Phys. Lett. B 166 (1986) 479–483.
[149] S. N. Gninenko, “Stringent limits on the π 0 → γX, X → e + e− decay from neutrino experiments
and constraints on new light gauge bosons,” Phys. Rev. D 85 (2012) 055027, arXiv:1112.5438
[hep-ph].
[150] H. Merkel et al., “Search at the Mainz Microtron for Light Massive Gauge Bosons Relevant for the
Muon g-2 Anomaly,” Phys. Rev. Lett. 112 no. 22, (2014) 221802, arXiv:1404.5502 [hep-ex].
[151] APEX Collaboration, S. Abrahamyan et al., “Search for a New Gauge Boson in Electron-Nucleus
Fixed-Target Scattering by the APEX Experiment,” Phys. Rev. Lett. 107 (2011) 191804,
arXiv:1108.2750 [hep-ex].
[152] BaBar Collaboration, J. P. Lees et al., “Search for a Dark Photon in e+ e− Collisions at BaBar,”
Phys. Rev. Lett. 113 no. 20, (2014) 201801, arXiv:1406.2980 [hep-ex].
[153] BaBar Collaboration, J. P. Lees et al., “Search for Invisible Decays of a Dark Photon Produced in
e+ e− Collisions at BaBar,” Phys. Rev. Lett. 119 no. 13, (2017) 131804, arXiv:1702.03327
[hep-ex].
[154] LHCb Collaboration, R. Aaij et al., “Search for Dark Photons Produced in 13 TeV pp Collisions,”
Phys. Rev. Lett. 120 no. 6, (2018) 061801, arXiv:1710.02867 [hep-ex].
[155] H. Esseili and G. D. Kribs, “Cosmological implications of gauged U(1)B−L on ∆N ef f in the CMB
and BBN,” JCAP 05 (2024) 110, arXiv:2308.07955 [hep-ph].
[156] S.-P. Li and X.-J. Xu, “Nef f constraints on light mediators coupled to neutrinos: the
dilution-resistant effect,” JHEP 10 (2023) 012, arXiv:2307.13967 [hep-ph].
[157] D. K. Ghosh, P. Ghosh, S. Jeesun, and R. Srivastava, “Neff at CMB challenges U(1)X light gauge
boson scenarios,” Phys. Rev. D 110 no. 7, (2024) 075032, arXiv:2404.10077 [hep-ph].
[158] D. K. Ghosh, P. Ghosh, S. Jeesun, and R. Srivastava, “Neff at cmb challenges u(1)X light gauge
boson scenarios,” Phys. Rev. D 110 (Oct, 2024) 075032.
https://link.aps.org/doi/10.1103/PhysRevD.110.075032.
[159] L. Heurtier and Y. Zhang, “Supernova Constraints on Massive (Pseudo)Scalar Coupling to
Neutrinos,” JCAP 02 (2017) 042, arXiv:1609.05882 [hep-ph].
[160] J. H. Chang, R. Essig, and S. D. McDermott, “Revisiting Supernova 1987A Constraints on Dark
Photons,” JHEP 01 (2017) 107, arXiv:1611.03864 [hep-ph].
[161] D. Croon, G. Elor, R. K. Leane, and S. D. McDermott, “Supernova Muons: New Constraints on Z’
Bosons, Axions and ALPs,” JHEP 01 (2021) 107, arXiv:2006.13942 [hep-ph].
[162] A. Caputo, G. Raffelt, and E. Vitagliano, “Muonic boson limits: Supernova redux,” Phys. Rev. D 105
no. 3, (2022) 035022, arXiv:2109.03244 [hep-ph].
[163] A. Caputo, G. Raffelt, and E. Vitagliano, “Radiative transfer in stars by feebly interacting bosons,”
JCAP 08 no. 08, (2022) 045, arXiv:2204.11862 [astro-ph.SR].
[164] J. Liao and D. Marfatia, “COHERENT constraints on nonstandard neutrino interactions,” Phys.
Lett. B 775 (2017) 54–57, arXiv:1708.04255 [hep-ph].
