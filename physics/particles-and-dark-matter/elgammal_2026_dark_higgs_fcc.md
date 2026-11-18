Source: https://arxiv.org/abs/2602.03235v2
PDF sha256: dd84eb0acb80737acee360e63b9b3dc17ae4283a4fe8693c815a7727ebc8ca16
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of elgammal_2026_dark_higgs_fcc.pdf

Transcription of `elgammal_2026_dark_higgs_fcc.pdf` in this directory, 18 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-18 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Search for the production of dark Higgs in the
framework of Mono-Z′ portal at the FCC-ee simulated
√
electron-positron collisions at s = 240 GeV

arXiv:2602.03235v2 [hep-ph] 4 Feb 2026

S. Elgammal,1a N. De Filippisb,c
a

Centre for Theoretical Physics, The British University in Egypt, P.O. Box 43, El Sherouk City,
Cairo 11837, Egypt.
b
Istituto Nazionale di Fisica Nucleare, Sezione di Bari: Bari, Apulia, IT.
c
Politecnico di Bari: Bari, Apulia, IT.

Abstract: In the present work, we study the possible production of the dark Higgs
boson (hD ) candidates, which originated from a simplified-model scenario based on the
Mono-Z′ model, in association with a neutral gauge boson (Z′ ). This study has been
performed by studying events with dimuon plus missing transverse energy produced in
the simulated electron-positron collisions at the foreseen Future Circular Collider in the
Electron-Positron collision mode (FCC-ee), operating at 240 GeV center of mass energy
and integrated luminosity of 10.8 ab−1 . In case no new physics has been discovered, we set
upper limits at a 95% confidence level on the mass of the dark Higgs.
ArXiv ePrint: arXiv:7228004 [hep-ph]

1

sherif.elgammal@bue.edu.eg

## PDF page 2

Contents
1 Introduction

1

2 The simplified Dark Higgs model

3

3 Simulation of SM backgrounds and signal samples

4

4 Event selection and backgrounds reduction
4.1 Event pre-selection
4.2 Event final selection and efficiencies

5
5
7

5 Results

10

6 Summary

12

1

Introduction

The discovery of the Higgs boson at CERN’s Large Hadron Collider (LHC) in 2012 filled
a crucial gap in the Standard Model of particle physics [1, 2]. Its properties continue to be
analyzed, but achieving ultimate precision requires a future collider designed to produce
high quantities of Higgs bosons in a clean environment. Precise measurements could reveal
insights into physics beyond the Standard Model (BSM). Many theories suggest the Higgs
boson could act as a gateway to new physics, particularly through exotic decays into new
light particles [3–7]. Thus, searching for these exotic decays is vital alongside precision
studies at future Higgs factories [8]. While such decays into promptly decaying particles
have been investigated at the LHC and proposed future facilities, new physics might also
appear in other decay modes [9, 10].
Direct searches for the process H → invisible particles have been conducted by the
ATLAS [11–16] and CMS [17–21, 23, 24] collaborations. These searches utilized data
collected during Run 1 (2011–2012) and Run 2 (2015–2018). The analyses targeted channels
in which the Higgs boson is produced via vector boson fusion (VBF), gluon-gluon fusion
(ggH), and in association with either a vector boson (VH, where V represents either a W
or Z boson) or with a top quark pair (ttH). The most stringent constraint on the branching
ratio B(H → inv) has been set by the CMS experiment through the VBF channel, using
data from both Run 1 and Run 2. This analysis reports a 95% confidence level (CL) upper
limit of 0.18 on the branching fraction to invisible particles, with an expected value of 0.10
[24]. In all these analyses, it was assumed that the mass of the Higgs boson decaying into
invisible particles is 125 GeV.
The LEP working group for Higgs boson searches has updated its previous combined
limit for the mass of a Higgs boson that decays invisibly. This study includes the data

–1–

## PDF page 3

collected in a total integrated luminosity of approximately 189-209 pb−1 . No evidence was
found indicating the production of invisibly decaying Higgs bosons in conjunction with a
Z boson decaying into hadrons, electrons, or muons. This conclusion applies to both the
overall event counts and the distributions of the discriminant variables and recoil masses.
Limits on the Higgs boson mass, mh , at the 95% confidence level are established based on
analyses of hadronic and leptonic Z boson decays. Consequently, the mass ranges of 60 112.1 GeV from the hadronic analysis and 60 - 91.3 GeV from the leptonic analysis are
excluded [22].
A promising approach for detecting physics beyond the Standard Model (SM) at future
electron-positron colliders involves analyzing changes in the dilepton mass spectrum. These
changes might appear as a new peak, which is predicted by models that incorporate neutral
gauge bosons, such as Z′ [25] or Randall-Sundrum particles [26]. Alternatively, one could
observe a broad distortion in the spectrum. Such distortions could indicate the presence
of Contact Interactions [27, 28] or frameworks like the ADD model [29]. To support these
theories, the mass spectrum needs to show an excess or deficit of events compared to
the background prediction, a result primarily driven by the production of dilepton via a
Drell-Yan process.
The CMS collaboration has conducted a detailed study of signatures related to Z′ and
Contact Interaction models [30]. Both the ATLAS and CMS collaborations have previously
searched for the massive extra neutral gauge boson Z′ , which is predicted by Grand Unified
Theory (GUT) and Supersymmetry [31–34]. However, there is currently no evidence for
its existence after analyzing the full RUN II period of LHC data [30, 35]. The results from
the CMS experiment have excluded the existence of Z′ , at a 95% Confidence Level (CL),
for mass values ranging from 0.6 to 5.15 TeV, while the ATLAS experiment has ruled out
mass values between 0.6 and 5.1 TeV. Additionally, both ATLAS and CMS have established
stringent limits on the coupling of the Z′ particle to Standard Model (SM) leptons, denoted
as gl . Based on observations of four-muon final states, the coupling constant gl is ruled
out in the range of 0.004 to 0.3, depending on the mass of the Z′ boson [36, 37].
Previous collider experiments, like the LEP-2 [38], have shed light on important in√
sights. For Z′ masses exceeding the center-of-mass energy of s = 209 GeV, the LEP
collaboration set a limit of gl ≤ 0.044 × MZ ′ /(200 GeV). Conversely, for MZ ′ < 209 GeV,
the limit on gl remains at gl ≤ 0.044 [39].
If the Z′ does not interact with quarks, the HL-LHC and future hadron colliders will
be unable to confirm its existence. In such a scenario, electron-positron colliders, like the
proposed Future Circular Collider in its Electron-Positron collision mode (FCC-ee), will
play a vital role. The FCC-ee is expected to begin operations at a center of mass energy
√
of 240 GeV ( s), with plans for a future upgrade to 365 GeV [40–42].
The initial phase of the FCC-ee is designed to be a high-luminosity and high-precision
electron-positron collider, functioning as a factory for electroweak processes, top quarks,
and particularly, the Higgs boson [43]. It provides controllable energy levels and minimizes
QCD background noise, making it a crucial tool in this research area.
This analysis explores a light dark Higgs (hD ) which is produced at FCC-ee in addition
to a light neutral gauge bosons (Z′ ) with a mass MZ ′ ≤ 90 GeV, based on the dark Higgs

–2–

## PDF page 4

(DH) simplified model within the mono-Z′ framework [6]. We examine simulated electronpositron collisions at the FCC-ee with 240 GeV center of mass energy, focusing on dimuon
events from Z′ decay and large missing energy linked to dark Higgs decaying to invisible
particles.
This paper is organized as follows: In Section 2, we present the theoretical framework
for the mono-Z′ portal model. Section 3 delves into the simulation techniques employed
to generate both signal and standard model background samples. Moving to Section 4,
we outline the selection criteria and analysis strategy. Finally, Sections 5 and 6 provide a
comprehensive overview of our results and a summary of the analysis.

2

The simplified Dark Higgs model

The mono-Z′ model, as discussed in [6], is one of the top recommendations from the CMS
collaboration for searching for dark Higgs at the LHC [44]. This model encompasses the
production of dark Higgs or dark matter at the LHC, as well as at future electron-positron
colliders, in conjunction with a new neutral gauge boson, Z′ .
The mediator vector boson, Z′ , interacts with the Standard Model particles and dark
Higgs particles in the simplified Dark Higgs (DH) scenario. The Z′ boson generates a light
dark Higgs (hD ), which then disintegrates into a pair of DM particles (χχ̄), assuming the
masses of the dark Higgs and Z′ are equal. The mass choice is given in table 1 and the
Feynman diagram is shown in figure 1. The interaction term, in the Lagrangian, between
Z′

e−
Z′

hD

e+

X
X

Figure 1: Feynman diagram of the DH model, adapted from Ref. [6]
the dark Higgs and Z′ is given by [6]
gD MZ ′ hD Z ′µ Zµ′ ,
where gD denotes the coupling of Z′ to dark Higgs, and MZ ′ is the Z ′ mass.
The interaction term, in the Lagrangian, between the SM particles and Z′ is given by
[6]
∑
gl ψ̄l γµ ψl Z ′µ ,
l

where the coupling of Z′ to visible leptons is represented by gl .
In the DH scenario, the only permitted decay processes are as follows: Z ′ → hD Z ′ ,
hD → χχ, and Z ′ → µ+ µ− . The total decay widths of both the Z ′ and hD can be calculated
using the masses of Z ′ and the dark Higgs, along with the relevant coupling constants. The
free parameters in this scenario include the lightest dark Higgs mass MhD , the mass of the

–3–

## PDF page 5

Table 1: The assumptions of the masses of the particles produced following the DH
scenario, the light dark Higgs introduced in [6].
Scenario

Masses assumptions

Light dark Higgs

MhD =

{
MZ ′ ,
125 GeV,

MZ ′ < 125 GeV
MZ ′ > 125 GeV.

Z′ boson (MZ ′ ), and the couplings of Z′ to both leptons and dark Higgs particles, gl and
gD , respectively.
The CMS and ATLAS detectors have extensively searched for Z′ bosons over the years,
confirming that heavy neutral gauge bosons do not exist in the mass range of 0.2 to 5.15
TeV. Therefore, we focus on the production of light neutral gauge bosons (Z′ ) below 90
GeV at the FCC-ee.
Due to previous restrictions from experiments like CMS, ATLAS, and LEP-2, the value
of gl is approximately 0.003 for MZ ′ between 10 and 90 GeV [39]. In contrast, gD is set
to 1.0 as suggested by the LHC Dark Matter Working Group [45], while the masses (MZ ′ ,
MhD ) are varied.

3

Simulation of SM backgrounds and signal samples

The SM background processes yielding muon pairs in the signal region are Z/γ → µ+ µ− ,
and → τ + τ − production, the production of top quark pairs (tt̄ → µ+ µ− + 2b + 2ν), and
production of diboson (W + W − → µ+ µ− + 2ν, ZZ → µ+ µ− + 2ν and ZZ → 4µ).
Table 2: The simulated SM backgrounds generated from electron-positron collisions at
√
the FCC-ee at s = 240 GeV. Their corresponding cross-section times branching ratios
for each process, and the generation order are presented. Names of these MC samples and
the used generators are stated as well.
Process

Deacy channel

Generator

σ × BR (fb)

Order

Z/γ
Z/γ
WW
ZZ
ZZ
tt̄

µ+ µ−
τ +τ −
µ+ µ− + 2ν
µ+ µ− + 2ν
4µ
µ+ µ− + 2ν + 2b

Whizard
Whizard
Whizard
Whizard
Whizard
Whizard

4776.0
4826.0
200.6
5.0
0.6
1.7×10−6

LO
LO
LO
LO
LO
LO

The DH scenario signal samples and the corresponding SM background samples are
privately produced. They have been generated using the WHIZARD event generator 3.1.1
[46]. The ISR effect was included and interfaced with Pythia 6.24 for the parton shower

–4–

## PDF page 6

model and hadronization [48]. For a fast detector simulation of the IDEA detector model
[47], the DELPHES package [49] was used. These were generated from electron-positron
collisions at the FCC-ee with a 240 GeV center of mass energy, which corresponds to the
circumstances of RUN I.
For the scenario where dark Higgs is produced along with Z′ , we have considered the
mass assumptions as summarized in table 1. Assuming gl = 0.003 and gD = 1.0, table
3 shows the production cross section times branching ratios at Leading Order (LO) for
various mass points of Z′ .
Table 3: Cross-sections times branching ratios BR(Z ′ → µ+ µ− ) for the DH scenario,
calculated for different values of MZ ′ in (GeV), assuming the coupling constant gD = 1.0,
√
and gl = 0.003, at s = 240 GeV.
M Z ′ = M hD
σ × BR (fb)

20

30
−01

7.4 × 10

40
−01

7.1 × 10

6.7 × 10

50
−01

60
−01

6.3 × 10

6.0 × 10

70
−01

80
−01

5.8 × 10

5.7 × 10−01

The Monte Carlo simulations were used to generate the SM background samples and
calculate their corresponding cross-sections for this analysis. The calculations were done
in leading order and can be found in table 2. Due to the tiny value of the cross section of
the leptonic decay of tt̄, it has been excluded from the analysis.
The signal samples and SM background processes were estimated from these simulations and were normalized to their respective cross sections and an integrated luminosity
of 10.8 ab−1 .
An ad-hoc flat 10% uncertainty is applied to cover all possible systematic effects.

4
4.1

Event selection and backgrounds reduction
Event pre-selection

The event selection process has been designed to reconstruct a final state consisting of two
muons with low transverse momentum (pT ) and missing energy accounting for the invisible
particles. The selection is made by applying cuts on various kinematic parameters.
Both muons must pass a preliminary selection that includes the following criteria:
- pµT (GeV) > 5,
- |η µ | (rad) < 2.5,
- Σi piT /pµT < 0.1.
Here, Σi piT /pµT < 0.1, represents the isolation cut in DELPHES software to reject
muons produced inside jets. This cut requires that the scalar pT sum of all muon tracks
within a cone of ∆R = 0.5 around the muon candidate, excluding the muon candidate
itself, should not exceed 10% of the pT of the muon. These pre-selection cuts are listed in
Table 4. Each event is selected based on two opposite-charge muons.
Figure 2 illustrates the distribution of the dimuon invariant mass for events that passed
the pre-selection criteria outlined in table 4, with Mµ+ µ− < 120 GeV. In this visualization,
the red histogram represents the Z/γ background, while the cyan histogram indicates the

–5–

## PDF page 7

Table 4: Summary of cut-based event selections used in the analysis.
Pre-selection

Final selection

pµT > 5 GeV
|η µ | < 2.5 rad
Σi piT /pµT < 0.1

pµT > 5 GeV
|η µ | < 2.5 rad
Σi piT /pµT < 0.1
+ −
+ −
|E miss − E µ µ |/E µ µ < 0.4
∆ϕµ+ µ− ,E⃗ miss > 3 rad
cos(Angle3D ) < −0.8
∆R(µ+ µ− ) < 1.7

Events / 1 GeV

vector boson pair background (W W ). The green histogram corresponds to the process
ZZ → 2µ2ν, and the yellow histogram depicts the ZZ → 4µ events. These histograms
are presented in a stacked format. While the signals of the DH scenario, which have
been generated with different masses (from 30 to 80 GeV) of the Z′ boson and fixing the
coupling constants gl = 0.003 and gD = 1.0, are represented by different colored lines, and
are overlaid.
10.8 ab-1 (240 GeV)
1012

Z/ γ → µ +µ −, τ+τ−
WW→ 2l2ν
ZZ→ 2l2ν
ZZ→ 4l
MZ' = 30 GeV
MZ' = 40 GeV
MZ' = 50 GeV
MZ' = 60 GeV
MZ' = 70 GeV
MZ' = 80 GeV

Delphes simulation(FCC-ee)

1011

e + e - → Z' → Z' hD

1010

Dark Higgs: Z'→µ +µ −

9

10

g = 0.003, g = 1.0

108

l

D

107
106
105
104
103
102
10
1
10−1
10

20

30

40

50

60

70

80

90

100

110

120

Mµ+µ- [GeV]

Figure 2: The measured dimuon invariant mass spectrum, after applying pre-selection
summarized in table 4, for the estimated SM backgrounds and different choices of neutral
gauge boson (Z′ ) masses generated based on the DH scenario, with gl = 0.003 and
gD = 1.0.
In e+ e− collisions, the total energy and momentum of the final states are well understood, with only minor distortions from factors like initial state radiation (ISR) and
beam-energy spread (BES) resulting from synchrotron radiation and beamstrahlung effects. When the decay products of the Z ′ boson can be clearly identified, it is possible to
precisely determine the energy and momentum of the dark Higgs particle, which in turn
allows us to calculate its mass. This calculation, known as the recoil mass (Mrec ), is based
on energy-momentum conservation and can be achieved with excellent accuracy, regardless

–6–

## PDF page 8

of how the dark Higgs boson decays [52]. Then, the recoil mass is calculated from the
following equation,
√
√
Mrec = s + Mµ+ µ− − 2 sE µ+ µ− ,

Events / 2 GeV

√
+ −
where s represents the center-of-mass energy, E µ µ denotes the energy of the dimuon
pair, and Mµ+ µ− refers to the invariant mass of the dimuon pair. To avoid the influence of
the Z and SM Higgs boson (ZH) events, we conducted our analysis with a recoil mass set
below 90 GeV (i.e. Mrec < 90 GeV).
10.8 ab-1 (240 GeV)
1010

Z/ γ → µ +µ −
Z/ γ → τ+τ−
WW→ 2µ 2ν
ZZ→ 2µ 2ν
ZZ→ 4µ
Mh = 30 GeV
MhD = 40 GeV
MhD = 50 GeV
MhD = 60 GeV
MhD = 70 GeV
MhD = 80 GeV

Delphes simulation(FCC-ee)

109

e + e - → Z' → Z' hD

108

Dark Higgs: Z'→µ +µ −

107

g = 0.003, g = 1.0
l

D

106

D

105
104
103
102
10
1
10−1
0

10

20

30

40

50

60

70

80

90

Mrec [GeV]

Figure 3: The recoil mass spectrum, for events passing the pre-selection summarized in
table 4, for the estimated SM backgrounds and different choices of the dark Higss masses
generated based on the DH simplified model, with the coupling constants gl = 0.003 and
gD = 1.0.
In Figure 3, we present the recoil mass spectrum for events that satisfy the pre-selection
criteria outlined in Table 4. The histograms illustrate the estimated Standard Model backgrounds alongside various dark Higgs masses (MhD = 30, 40, ..., 80 GeV) that were generated based on the dark Higgs simplified model. This analysis utilizes coupling constants of
gl = 0.003 and gD = 1.0.
Figures 2 and 3 demonstrate that the signal samples are heavily mixed with background
events across the entire dimuon invariant mass and recoil mass ranges. Hence, as outlined
in the following paragraph, we need to implement stricter criteria to effectively separate
the signals from Standard Model backgrounds.
4.2

Event final selection and efficiencies

In addition to the pre-selection criteria, we have applied tighter cuts based on four variables:
+ −
1. We assess the relative difference between the energy of the dimuon (E µ µ ) and
the missing energy (E miss ). This difference is selected to be less than 0.4, defined by the
+ −
+ −
condition |E miss − E µ µ |/E µ µ < 0.4.

–7–

## PDF page 9

Z → τ+τ−
WW
ZZ(2µ 2ν )
ZZ(4µ )
MZ' = 30 GeV
MZ' = 70 GeV

0.8

1

1.2
miss

|E
+

−

+

Events

(a) |E miss − E µ µ |/E µ µ

Events

Z/ γ → µ +µ −

1.4

µ+µ-

-E

Z/ γ → µ +µ −
Z → τ+τ−
WW
ZZ(2µ 2ν )
ZZ(4µ )
MZ' = 30 GeV
MZ' = 70 GeV

2

2.5

µ+µ-

−

1012
Delphes simulation(FCC-ee)
1011
e + e - → Z' → Z' hD
1010
Dark Higgs: Z'→µ +µ −
109
g = 0.003, g = 1.0
l
D
108
107
6
10
105
104
103
102
10
1
10−1
−2
10
10−3−1 −0.8 −0.6 −0.4 −0.2

10.8 ab-1 (240 GeV)

1012
Delphes simulation(FCC-ee)
1011
e + e - → Z' → Z' hD
1010
Dark Higgs: Z'→µ +µ −
9
10
g = 0.003, g = 1.0
l
D
108
107
6
10
105
104
103
102
10
1
10−1
−2
10
10−3 0
0.5
1
1.5

3
-

µ+µ

|φ

|/E

− φmiss| [rad]

(b) ∆ϕµ+ µ− ,E⃗ miss
10.8 ab-1 (240 GeV)
Events

Events

10.8 ab-1 (240 GeV)

1012
Delphes simulation(FCC-ee)
1011
e + e - → Z' → Z' hD
1010
Dark Higgs: Z'→µ +µ −
9
10
g = 0.003, g = 1.0
l
D
108
107
6
10
105
104
103
102
10
1
10−1
−2
10
10−3 0
0.2
0.4
0.6

Z/ γ → µ +µ −

Z → τ+τ−
WW
ZZ(2µ 2ν )
ZZ(4µ )
MZ' = 30 GeV
MZ' = 70 GeV

0

0.2

0.4

0.6 0.8
1
cos(Angle3D)

1012
Delphes simulation(FCC-ee)
1011
e + e - → Z' → Z' hD
1010
Dark Higgs: Z'→µ +µ −
109
g = 0.003, g = 1.0
l
D
108
107
6
10
105
104
103
102
10
1
10−1
−2
10
10−3 0
1
2
3

10.8 ab-1 (240 GeV)
Z/ γ → µ +µ −
Z → τ+τ−
WW
ZZ(2µ 2ν )
ZZ(4µ )
MZ' = 30 GeV
MZ' = 70 GeV

4

5

6

+

Figure 4: The distributions of three variables for dimuon events, where each muon
passes the low pT muon ID discussed in the pre-selection in table 4. The four variables
+ −
+ −
are |E miss − E µ µ |/E µ µ 4a, ∆ϕµ+ µ− ,E⃗ miss 4b, cos(Angle3D ) 4c, and ∆R(µ+ µ− ) 4d.
The model corresponds to the DH scenario with two different values of Z ′ (MZ ′ = 30 and
70 GeV) and SM backgrounds. The vertical dashed lines correspond to the chosen cut
value for each variable.
2. We calculate the azimuthal angle difference ∆ϕµ+ µ− ,E⃗ miss , which is the difference
+ −

between the azimuthal angles of the dimuon and the missing energy (|ϕµ µ − ϕmiss |). This
value is required to be greater than 3.0 radians.
3. We apply a criterion on the cosine of the 3D angle between the missing energy
vector and the dimuon system vector to ensure they are back-to-back, requiring that
cos(Angle3D ) < −0.8.
Finally, we impose a cut on the angular separation ∆R(µ+ µ− ) between the two
opposite-sign muons, which must be less than 1.7.
The graphs in Figure 4 display the distributions of specific variables for two signal
presentations of the simplified model associated with the dark Higgs scenario, corresponding

–8–

8

∆R(µ µ-)

(d) ∆R(µ+ µ− )

(c) cos(Angle3D )

7

## PDF page 10

Z/ γ → µ +µ −
Z/ γ → τ+τ−
WW
ZZ(2µ 2ν )
ZZ(4µ )
MZ' = 30 GeV

Delphes simulation(FCC-ee)
e + e - → Z' → Z' hD

Dark Higgs: Z'→µ +µ −
g = 0.003, g = 1.0
l

N-1 Eff. / 10 GeV

N-1 Eff. / 10 GeV

10

D

1

10

10

−1

10
e + e - → Z' → Z' hD

Dark Higgs: Z'→µ +µ −
g = 0.003, g = 1.0
l

20

40

60

80

100

10

120

D

1

10

−2

Z/ γ → µ +µ −
Z/ γ → τ+τ−
WW
ZZ(2µ 2ν )
ZZ(4µ )
MZ' = 30 GeV

Delphes simulation(FCC-ee)

−1

−2

20

40

60

80

100

µ

p [GeV]

p [GeV]

T

T

(b)
10

Z/ γ → µ +µ −
Z/ γ → τ+τ−
WW
ZZ(2µ 2ν )
ZZ(4µ )
MZ' = 30 GeV

Delphes simulation(FCC-ee)
e + e - → Z' → Z' hD

Dark Higgs: Z'→µ +µ −
g = 0.003, g = 1.0
l

N-1 Eff. / 10 GeV

N-1 Eff. / 10 GeV

(a)

120
µ

D

1

10

−1

10−2

10
e + e - → Z' → Z' hD

Dark Higgs: Z'→µ +µ −
g = 0.003, g = 1.0
l

40

60

80

100

−1

10−2

120

D

1

10

20

Z/ γ → µ +µ −
Z/ γ → τ+τ−
WW
ZZ(2µ 2ν )
ZZ(4µ )
MZ' = 30 GeV

Delphes simulation(FCC-ee)

20

40

60

80

100

µ

p [GeV]

p [GeV]

T

(c)

T

(d)

Figure 5: Distributions of the N-1 efficiencies plotted against the transverse momentum
of the leading reconstructed muon (pµT ) for the following cuts;
+ −
+ −
|E miss − E µ µ |/E µ µ < 0.4 5a, ∆ϕµ+ µ− ,E⃗ miss > 3.0 5b, ∆R(µ+ µ− ) < 1.7 5c, and
cos(Angle3D ) < −0.8 5d for the signal in the DH scenario with MZ ′ = 30 GeV and for the
SM backgrounds.

to MZ ′ values of 30 GeV and 70 GeV. Additionally, the figure includes the Standard
Model (SM) backgrounds. These variables are presented for HD signal samples and SM
backgrounds concerning dimuon events that satisfy the pre-selection criteria specified in
Table 4, with Mµ+ µ− < 120 GeV.
+ −

+ −

The first variable is represented as |E miss − E µ µ |/E µ µ , with its graph displayed
in Plot 4a. The second variable is denoted as ∆ϕµ+ µ− ,E⃗ miss , and its corresponding graph
is shown in Plot 4b. The third variable measures the variable, cos(Angle3D ), is illustrated
in Plot 4c. Lastly, the angular distance between the two muons, referred to as ∆R(µ+ µ− ),
is presented in Plot 4d. The vertical dashed lines in these figures indicate the selected cut
value for each variable.
The performance metrics for fine-tuning these rigorous cuts are illustrated by plotting

–9–

120
µ

## PDF page 11

the N-1 efficiency for each of the four criteria detailed in Table 4. To calculate the N-1
efficiency, we take the number of events that successfully pass the final selection and divide
it by the number of events that would have cleared the final selection in the absence of the
specific cut under consideration.
In figure 5, we present the distributions of the N-1 efficiencies plotted against the
transverse momentum of the leading reconstructed muon (pµT ) for the following conditions:
+ −
+ −
|E miss − E µ µ |/E µ µ < 0.4 5a, ∆ϕµ+ µ− ,E⃗ miss > 3.0 5b, ∆R(µ+ µ− ) < 1.7 5c, and
cos(Angle3D ) < −0.8 5d. These plots focus on the signal in the DH scenario (indicated by
black closed circles), with MZ ′ = 30 GeV, gDM = 1.0 and gl = 0.003, alongside standard
model (SM) backgrounds marked with open colored markers.
The efficiency plots demonstrate that the application of these four stringent selection
criteria effectively suppresses the background from the process Z/γ → µ+ µ− , τ τ . This
approach also minimizes contamination from events such as W W , ZZ(4µ), and ZZ(2µ2ν).
Additionally, it ensures that the signal maintains a consistently flat efficiency across high
transverse muon momentum (pµT > 40 GeV).

Results
Events / 2 GeV

5

10.8 ab-1 (240 GeV)
107

Z/ γ → µ +µ −
Z/ γ → τ+τ−
WW→ 2µ 2ν
ZZ→ 2µ 2ν
ZZ→ 4µ
Mh = 30 GeV
MhD = 40 GeV
MhD = 50 GeV
MhD = 60 GeV
MhD = 70 GeV
MhD = 80 GeV

Delphes simulation(FCC-ee)
6

10

e + e - → Z' → Z' hD
Dark Higgs: Z'→µ +µ −

105

g = 0.003, g = 1.0
l

104

D

D

103
102
10
1
10−1
10−2
10−3

0

10

20

30

40

50

60

70

80

90

Mrec [GeV]

Figure 6: The recoil mass spectrum, for events passing the final selection listed in table
4, for the estimated SM backgrounds and different choices of the dark Higss masses
generated based on the DH simplified model, with the coupling constants gl = 0.003 and
gD = 1.0.
Figure 6 shows the recoil mass spectrum for events that meet the final selection criteria
listed in Table 4. The histograms represent the estimated SM backgrounds and various
dark Higgs masses (MhD = 30, 40, ..., 80 GeV) generated based on the DH simplified
model, with the coupling constants gl = 0.003 and gD = 1.0.
The shape-based analysis utilizes the distributions of the recoil mass (Mrec ), in different
bins around the dark Higgs mass (MhD − 5 < Mrec < MhD + 5), for events passing the final
event selection listed in table 4 as effective discriminators.

– 10 –

## PDF page 12

Table 5 presents the number of events that satisfy the final event selection criteria,
calculated across different bins of the recoil mass (MhD − 5 < Mrec < MhD + 5) in line with
the DH scenario. The assumed coupling constants are gD = 1.0 and gl = 0.003. The yields
shown in the table encompass all anticipated relevant Standard Model backgrounds, based
√
on an integrated luminosity of 10.8 ab−1 and a center-of-mass energy of s = 240 GeV.
Furthermore, the table takes into account the total uncertainties, including both statistical
and systematic components.
When analyzing an enriched sample of events for a specific signal process, it is essential
to assess the entire distribution of a variable across all events rather than just counting the
number of events within a specified signal region. In this framework, the profile likelihood
can be employed for hypothesis testing by utilizing the asymptotic properties of the proL(b)
filed likelihood ratio, defined as: λ = L(s+b)
. From this ratio, the p-value and statistical
significance, denoted as SL , can be derived using the following formula, [53, 54],
SL =

√

−2lnλ,

SL

where L(s + b) is the maximum likelihood value obtained in the full signal-plusbackground unbinned maximum likelihood fit, and L(b) is the maximum likelihood from
the unbinned background-only fit.
The outcomes of this definition are presented in the last row of table 5, which quantifies
the significance of the excess signal events in comparison to the standard model (SM)
background events.
102

Delphes simulation(FCC-ee)

Mh = 30 GeV

e + e - → Z' → Z' hD

D

Dark Higgs: Z'→µ +µ −

Mh = 60 GeV
D

g = 0.003, g = 1.0
l

D

10

5σ

1

−1

10

1

10

lumi [ab-1]

Figure 7: The statistical significance (SL ) versus integrated luminosity for MhD = 30
(closed circles) and 60 (opened circles) GeV for events passing the final selection. The
model signal represents the DH scenario with coupling constants gl = 0.003, and gD = 1.0
√
at s = 240 GeV. The dashed red line indicates SL = 5 .
Figures 7 illustrates the statistical significance (SL ) as a function of the FCC-ee integrated luminosity for two values of dark Higgs mass (MhD = 30 and 60 GeV), for events
that meet final criteria outlined in Table 4. These figures reflect the model associated with

– 11 –

## PDF page 13

√
the DH scenario, using coupling constants of gl = 0.003 and gD = 1.0 at s = 240 GeV.
The dashed red line in the plots represents a significance value of S = 5. For MhD of 30
GeV, one can achieve a 5σ discovery at an integrated luminosity of 1.21 ab−1 . While for
MhD = 60 GeV requires an integrated luminosity of 3.5 ab−1 .
Table 5: The number of events satisfying the criteria of the final event selection are
illustrated for several recoil mass bins (MhD − 5 < Mrec < MhD + 5), for each SM
background, and the DH model signals for 10.8 ab−1 integrated luminosity and the
coupling constants gD = 1.0, gl = 0.003. The total Uncertainty, including the statistical
and systematic components, is indicated.
Mrec (GeV)

[15,25]

[25,35]

[35,45]

[45,55]

[55,65]

[65,75]

[75,85]

WW

179.1 ± 22.4

410.3 ± 45.8

648.6 ± 69.7

876.9 ± 92.6

1151.4 ± 120.0

1563.1 ± 161.2

1990.7 ± 204.0

ZZ → 2µ2ν

0.04 ± 0.2

0.32 ± 0.57

0.47 ± 0.69

1.51 ± 1.24

2.81 ± 1.70

5.18 ± 2.33

11.05 ± 3.50

ZZ → 4µ

0.04 ± 0.2

0.014 ± 0.12

0.041 ± 0.20

0.027 ± 0.17

0.041 ± 0.20

0.055 ± 0.23

0.041 ± 0.20

Sum Bkgs

179.2 ± 22.4

410.6 ± 45.8

649.1 ± 69.7

878.4 ± 92.7

1154.2 ± 120.3

1568.3 ± 161.8

2001.8 ± 205.1

DH signal

128.4 ± 17.1

2077.0 ± 212.6

2119.1 ± 216.9

2039.2 ± 208.9

1854.8 ± 190.4

1561.4 ± 161.1

832.4 ± 88.1

3.4σ

13.8σ

12.3σ

9.6σ

7.5σ

4.9σ

4.2σ

SL

We used the profile likelihood method to analyze our results statistically and performed a statistical test based on the Mrec distributions. We used the modified frequentist
construction CLs [55, 56], which is based on the asymptotic approximation [54], to derive
exclusion limits on the product of signal cross sections and the branching fraction Br(Z ′
→ µµ) at a 95% confidence level. In the likelihood, the systematic uncertainties are treated
as nuisance parameters.
In the mono-Z′ model, the 95% upper limit on the cross-section times the branching
ratio for the DH simplified scenario is shown in figure 8. The result is presented for the
muonic decay of the Z′ and with coupling constant values of gl = 0.003 and gD = 1.0, for
an integrated luminosity of 10.8 ab−1 . This limit shows that the dark Higgs mass range
from 20 to 80 GeV can be excluded for the coupling constant values of gl = 0.003 and
gD = 1.0.

6

Summary

The Future Circular Collider operating in Electron-Positron collision mode (FCC-ee) is
an outstanding facility for uncovering particles that extend beyond the Standard Model
(BSM). It offers a distinct signature for pinpointing unknown particles, such as dark matter,
extra neutral gauge bosons, and Kaluza-Klein excitations.
Our research investigated the recoil mass distributions with low-mass dimuon pairs
within the mono-Z′ model framework (Mrec < 90 GeV), using simulated Monte Carlo
(MC) data samples from the FCC-ee. These MC samples were generated from electron√
positron collisions with s = 240 GeV, including signal and Standard Model background
events. This setup corresponds to what is anticipated for FCC-ee Run 1, which is expected
to have an integrated luminosity of 10.8 ab−1 .

– 12 –

## PDF page 14

Delphes simulation(FCC-ee)

95% CL upper limit

e + e - → Z' → Z' hD

Median expected

Dark Higgs: Z' → µ +µ −

−2

10

expected ± 1σ

g = 0.003, g = 1.0
l

expected ± 2σ

D

Theory
−3

10

10−4

+

95% CL σ (e e− → Z'+ hD) × Br (Z' → µµ) [pb]

10.8 ab-1 (240 GeV)

10−1

−5

10

−6

10

20

25

30

35

40

45

50

55

60

65

70

75

80

Mh [GeV]
D

Figure 8: 95% CL upper limits on the cross-section times the branching ratio
(expected), as a function of the dark Higgs mass (MhD ) based on the mono-Z′ model,
with the muonic decay of the Z′ . The black line represents the DH scenario with coupling
constant values of gl = 0.003 and gD = 1.0.
In this study, we investigated the effects of a simplified model scenario known as the
dark Higgs (DH), focusing on dark Higgs production associated with a Z ′ boson at the
FCC-ee. We analyzed the results from the muonic decay mode of the Z ′ boson, with
coupling constants fixed at gl = 0.003 and gD = 1.0.
We implemented effective discrimination cuts that entirely suppressed the Z/γ background and significantly reduced the diboson W W and ZZ contaminations. This approach
enabled us to differentiate more effectively between signal events and the SM backgrounds.
Consequently, we achieved a noteworthy decrease in the SM backgrounds while maintaining the signal strength by applying the appropriate cuts, which are outlined in Table 4 for
the DH scenario.
Dark Higgs signals with a mass MhD > 20 GeV can exceed a 5σ discovery threshold
with an integrated luminosity of 10.8 ab−1 when the coupling constants are set at gD = 1.0
and gl = 0.003. However, for lighter dark Higgs states with MhD < 30 GeV, reaching a 5σ
discovery becomes unattainable.
Finally, if the dark Higgs signal is not observed at the FCC-ee, we set upper limits on
the mass of dark Higgs (MhD ) at the 95% confidence level for the charged muonic decay
channel of Z ′ . Limits have been established for the dark Higgs scenario with gl = 0.003
and gD = 1.0, which excludes the dark Higgs mass range from 20 to 80 GeV.
This study highlights the promising opportunities to directly investigate the existence
of a dark Higgs particle within the framework of physics that extends beyond the Standard
Model at the FCC-ee. This is especially pertinent for the mono-Z ′ model, which features
coupling parameters of gl = 0.003 and gD = 1.0, along with dark Higgs masses below 90
GeV. Notably, this domain has remained unexplored by the LHC.
Previous e+ e− colliders, including the LEP working group, updated the limits for
the mass of a Higgs boson that decays invisibly using data from approximately 189-209

– 13 –

## PDF page 15

pb−1 . No evidence was found for invisibly decaying Higgs bosons produced with a Z boson
decaying into hadrons, electrons, or muons. The 95% confidence level limits exclude Higgs
boson masses of 60 - 112.1 GeV from hadronic analysis and 60 - 91.3 GeV from leptonic
analysis. Our analysis lowers the limit to 20 GeV.
The findings related to the electron-philic decay scenario of Z ′ would closely align
with the results presented in this study, provided that the reconstruction efficiencies and
resolutions for both electrons and muons are similar.

Acknowledgments
The author of this paper would like to thank Tongyan Lin, co-author of [6], for providing us
with the UFO model files, helping us to generate the signal events, and cross-checking the
results. In addition, this paper is based on works supported by the Science, Technology,
and Innovation Funding Authority (STDF) under grant number 48289.

References
[1] ATLAS Collaboration, Observation of a new particle in the search for the Standard Model
Higgs boson with the ATLAS detector at the LHC. Physics Letters B (2012). DOI:
10.1016/j.physletb.2012.08.020.
[2] CMS Collaboration, Observation of a new boson at a mass of 125 GeV with the CMS
experiment at the LHC. Physics Letters B (2012). DOI: 10.1016/j.physletb.2012.08.021.
[3] D. Curtin et al., Exotic decays of the 125 GeV Higgs boson, Phys. Rev. D 90 (2014) 075004
[1312.4992].
[4] LHC Higgs Cross Section Working Group collaboration, Handbook of LHC Higgs Cross
Sections: 4. Deciphering the Nature of the Higgs Sector, 1610.07922.
[5] D. Curtin and C.B. Verhaaren, Discovering Uncolored Naturalness in Exotic Higgs Decays,
JHEP 12 (2015) 072 [1506.06141].
[6] Marcelo Autran, Kevin Bauer, Tongyan Lin, and Daniel Whiteson, Searches for dark matter
in events with a resonance and missing transverse energy. Physical Review D 92 (2015) 035007
[arXiv:1504.01386] [hep-ph].
[7] ATLAS Collaboration, Search for a new leptonically decaying neutral vector boson in
√
association with missing transverse energy in proton-proton collisions at s = 13 TeV with
the ATLAS detector, ATLAS-CONF-2023-045, 18 August 2023.
[8] Z. Liu, L.-T. Wang and H. Zhang, Exotic decays of the 125 GeV Higgs boson at future e+ e−
lepton colliders, Chin. Phys. C 41 (2017) 063102 [1612.09284].
[9] ATLAS Collaboration, Search for dark matter produced in association with a Standard Model
Higgs boson decaying into b-quarks using the full Run 2 dataset from the ATLAS detector,
JHEP 11 (2021) 209, [arXiv:2108.13391v2] [hep-ex].
[10] ATLAS Collaboration, Search for dark matter in events with missing transverse momentum
√
and a Higgs boson decaying into two photons in pp collisions at s = 13 TeV with the
ATLAS detector, JHEP 10 (2021) 13, [arXiv:2104.13240v2] [hep-ex].

– 14 –

## PDF page 16

[11] ATLAS Collaboration, Search for an invisibly decaying Higgs boson or dark matter
√
candidates produced in association with a Z boson in pp collisions at s = 13 TeV with the
ATLAS detector. Phys. Lett. B 776, 318 (2018). https://doi.org/10.1016/j.physletb.
2017.11.049. arXiv:1708.09624
[12] ATLAS Collaboration, Combination of searches for invisible Higgs boson decays with the
ATLAS experiment. Phys. Rev. Lett. 122, 231801 (2019).
https://doi.org/10.1103/PhysRevLett. 122.231801. arXiv:1904.05105.
[13] ATLAS Collaboration, Search for new phenomena in events with an energetic jet and missing
√
transverse momentum in pp collisions at s = 13 TeV with the ATLAS detector. Phys. Rev.
D 103, 112006 (2021). https://doi.org/10.1103/PhysRevD.103.112006. arXiv:2102.10874.
[14] ATLAS Collaboration, Search for associated production of a Z boson with an invisibly
√
decaying Higgs boson or dark matter candidates at s = 13 TeV with the ATLAS detector.
Phys. Lett. B 829, 137066 (2022). https://doi.org/10.1016/j.physletb.2022. 137066.
arXiv:2111.08372.
[15] ATLAS Collaboration, Search for invisible Higgs-boson decays in events with vector-boson
fusion signatures using 139 fb−1 of proton-proton data recorded by the ATLAS experiment.
JHEP 08, 104 (2022). https://doi.org/10.1007/JHEP08(2022)104. arXiv:2202.07953.
[16] ATLAS Collaboration, Constraints on spin-0 dark matter mediators and invisible Higgs
decays using ATLAS 13 TeV pp collision data with two top quarks and missing transverse
momentum in the final state. Eur. Phys. J. C 83 (2023) 503.
https://doi.org/10.1140/epjc/s10052-023-11477-z. arXiv:2211.05426.
√
[17] CMS Collaboration, Searches for invisible decays of the Higgs boson in pp collisions at s =
7, 8, and 13 TeV. JHEP 02, 135 (2017). https://doi.org/10.1007/JHEP02(2017)135.
arXiv:1610.09218.
[18] CMS Collaboration, Search for direct top squark pair production in events with one lepton,
jets, and missing transverse momentum at 13 TeV with the CMS experiment. JHEP 05, 032
(2020). https://doi.org/10.1007/JHEP05(2020)032. arXiv:1912.08887.
[19] CMS Collaboration, Search for top squark pair production using dilepton final states in pp
√
collision data collected at s = 13 TeV. Eur. Phys. J. C 81, 3 (2021).
https://doi.org/10.1140/epjc/s10052-020-08701-5. arXiv:2008.05936.
[20] CMS Collaboration, Combined searches for the production of supersymmetric top quark
√
partners in proton-proton collisions at s = 13 TeV. Eur. Phys. J. C 81, 970 (2021).
https://doi.org/10.1140/epjc/s10052-021-09721-5. arXiv:2107.10892.
[21] CMS Collaboration, Search for dark matter produced in association with a leptonically
√
decaying Z boson in proton-proton collisions at s = 13 TeV. Eur. Phys. J. C 81, 13 (2021).
https://doi.org/10.1140/epjc/s10052-020-08739-5. arXiv:2008.04735. [Erratum:
https://doi.org/10.1140/epjc/s10052-021-08959-3].
[22] L3 Collaboration, Search for an invisibly-decaying Higgs boson at LEP. Phys. Lett. B 609
(2005) 35-48. hep-ex/0501033 [hep-ex].
[23] CMS Collaboration, Search for new particles in events with energetic jets and large missing
√
transverse momentum in proton-proton collisions at s = 13 TeV. JHEP 11, 153 (2021).
https://doi.org/10.1007/JHEP11(2021)153. arXiv:2107.13021.
[24] CMS Collaboration, Search for invisible decays of the Higgs boson produced via vector boson

– 15 –

## PDF page 17

√
fusion in proton-proton collisions at s = 13 TeV. Phys. Rev. D 105, 092007 (2022).
https://doi.org/10.1103/PhysRevD.105.092007. arXiv:2201.11585.
[25] P. Langacker, The Physics of Heavy Z’ Gauge Bosons. Rev. Mod. Phys, 81:1199–1228, 2008.
[26] L. Randall and R. Sundrum, A large mass hierarchy from a small extra dimension. Phys.
Rev. Lett., 83:3370–3373, 1999.
[27] Lane K. Eichten, E. and M. Peskin, New Tests for Quark and Lepton Substructure. Phys.
Rev. Lett., 50(11):811814, 1983.
[28] E. Eichten et al., Supercollider physics. Rev. Mod. Phys., 56(4):579707, 1984.
[29] Dimopoulos S. Arkani Hamed, N. and G. Dvali, Phenomenology, Astrophysics and
Cosmology of Theories with Sub-Millimeter Dimensions and TeV Scale Quantum Gravity.
Phys. Rev. D., 59(8), 1999.
[30] The CMS Collaboration, Search for resonant and nonresonant new phenomena in high mass
√
dilepton final states at s = 13 TeV. JHEP 07 (2021) 208.
[31] M. Cvetic and S. Godfrey, “Discovery and identification of extra gauge bosons”,
arXiv:hep-ph/9504216.
[32] A. Leike, “The Phenomenology of extra neutral gauge bosons”, Phy. Rep. 317, 143 (1999)
[arXiv:hepph/9805494].
[33] M. Cvetic, P. Langacker, and B. Kayser, “Determination of g-R / g-L in left-right symmetric
models at hadron colliders”, Phys. Rev. Lett. 68 (1992) 2871.
[34] S. Dimopoulos and H. Georgi, “Softly Broken Supersymmetry And SU(5)”, Nucl. Phys. B
193 (1981) 150.
[35] ATLAS Collaboration, Search for high-mass dilepton resonances using 139 fb−1 of pp collision
√
data collected at s = 13 TeV with the ATLAS detector, Phys. Lett. B 796 (2019) 68.
[36] ATLAS collaboration, Search for a new Z′ gauge boson in 4µ events with the ATLAS
experiment, JHEP 07 (2023) 90.
[37] CMS collaboration, Search for an Lµ − Lτ gauge boson using Z → 4µ events in
√
proton-proton collisions at s = 13 TeV, Phys. Lett. B 792 (2019) 345.
[38] LEP et al. collaborations, A combination of preliminary electroweak measurements and
constraints on the Standard Model, hep-ex/0312023 [INSPIRE].
[39] Arnab Dasgupta, P. S. Bhupal Dev, Tao Han, Rojalin Padhan, Si Wang, Keping Xie,
Searching for heavy leptophilic Z ′ : from lepton colliders to gravitational waves, JHEP 12
(2023) 011.
[40] 2020 Update of the European Strategy for Particle Physics (Brochure), Tech. Rep.
CERN-ESU-015, Geneva (2020), DOI.
[41] A. Abada et al., FCC-ee: The Lepton Collider: Future Circular Collider Conceptual Design
Report Volume 2, Eur. Phys. J. ST 228 (2019) 261.
[42] M. Benedikt, et al., FCC-ee: The Lepton Collider : Future Circular Collider Conceptual
Design Report Volume 2. Eur. Phys. J. Spec. Top. 228(261), 400 (2019).
https://doi.org/10.1140/epjst/e2019-900045-4.
[43] S. Alipour-Fard, N. Craig, M. Jiang and S. Koren, Long Live the Higgs Factory: Higgs

– 16 –

## PDF page 18

Decays to Long-Lived Particles at Future Lepton Colliders, Chin. Phys. C 43 (2019) 053101
[1812.05588].
[44] CMS Collaboration, Dark sector searches with the CMS experiment. Phys. Rept. 1115 (2025)
448. https://doi.org/10.1016/j.physrep.2024.09.013. arXiv:2405.13778 [hep-ex].
[45] A. Boveia et al., Recommendations on presenting LHC searches for missing transverse energy
signals using simplified s-channel models of dark matter, Phys. Dark Univ. 27 (2020) 100365
[arXiv:1603.04156] [INSPIRE].
[46] Wolfgang Kilian, Thorsten Ohl, and Jurgen Reuter. WHIZARD—simulating multi-particle
processes at LHC and FCC-ee. The European Physical Journal C, 71(9), Sep 2011.
[47] The IDEA detector concept for FCC-ee (2025). arXiv:2502.21223 [physics.ins-det].
[48] T. Sjostrand, S. Mrenna and P. Skands, PYTHIA 6.4 Physics and Manual
[arXiv:hep-ph/0603175].
[49] J. de Favereau, C. Delaere, P. Demin, A. Giammanco, V. Lemaı̂tre, A. Mertens, M. Selvaggi,
DELPHES 3, A modular framework for fast simulation of a generic collider experiment, JHEP
1402 (2014).
[50] J Collins and D. Soper, Angular distribution of dileptons in high-energy hadron collisions.
Phys. Rev. D., 16(7):2219–2225, 1977.
[51] CMS Collaboration, Forward-backward asymmetry of Drell-Yan lepton pairs in pp collisions
√
at s = 8 TeV. Eur. Phys. J. C 76 (2016) 325.
[52] J. Eysermans, A. Li, G. Bernardi, Higgs boson mass and model-independent ZH cross-section
at FCC-ee in the di-electron and di-muon final states (2023).
https://doi.org/10.17181/jfb44-s0d81.
[53] Yong-Sheng Zhu, On Statistical Significance of Signal, High Energy Phys. Nucl. Phys. 30:
331-334, 2006, arXiv:0812.2708v1 [physics.data-an].
[54] G. Cowan et al., Asymptotic formulae for likelihood-based tests of new physics, Eur. Phys. J.
C 71 (2011), p. 1554, doi: 10.1140/epjc/s10052-011-1554-0, arXiv: 1007.1727
[physics.data-an], Erratum: Eur. Phys. J. C 73 (2013) 2501.
[55] A. L. Read, Presentation of search results: the CLs technique, J. Phys. G: Nucl. Part.Phys.
28 (2002) 2693, doi:10.1088/0954-3899/28/10/313.
[56] T. Junk, Confidence level computation for combining searches with small statistics, Nuclear
Instruments and Methods in Physics Research Section A: Accelerators, Spectrometers,
Detectors and Associated Equipment, Volume 434, Issues 2–3, 1999, Pages 435-443, ISSN
0168-9002, https://doi.org/10.1016/S0168-9002(99)00498-2.

– 17 –
