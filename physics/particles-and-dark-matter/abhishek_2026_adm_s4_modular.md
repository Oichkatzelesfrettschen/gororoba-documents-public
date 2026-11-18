Source: https://arxiv.org/abs/2602.03384v1
PDF sha256: 66eebef97173da8179e7389c35bee2d894a28b61afa9e6f2ed659cecff852509
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of abhishek_2026_adm_s4_modular.pdf

Transcription of `abhishek_2026_adm_s4_modular.pdf` in this directory, 28 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-28 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Prepared for submission to JHEP

arXiv:2602.03384v1 [hep-ph] 3 Feb 2026

Asymmetric dark matter from leptogenesis in type-III
seesaw framework with modular S4 symmetry

Abhishek1,* , V. Suryanarayana Mummidi1,†
1

Department of Physics, National Institute of Technology,
Tiruchirappalli-620015, India

E-mail: 413120051@nitt.edu,venkata@nitt.edu
Abstract: We present a unified framework for neutrino masses, baryogenesis, and dark
matter based on a modular S4 symmetry combined with a type-III seesaw mechanism.
All Yukawa couplings, CP phases, and flavor textures originate from a single complex
modulus τ , whose vacuum expectation value controls both visible and dark sector dynamics. The same modular parameter fixes the neutrino mass matrix, determines the
CP asymmetries driving resonant leptogenesis, and correlates the resulting baryon and
dark matter abundances. A detailed numerical analysis shows that the model reproduces
all neutrino oscillation data within the 3σ NuFIT 5.2 (2024) ranges for normal ordering,
∑
predicting δCP ≃ ±(150◦ − 180◦ ),
mν ≃ (0.06 − 0.08) eV, and an effective Majorana
mass mββ ≃ (8 − 18) × 10−3 eV, testable in next-generation neutrinoless double-beta
decay experiments. The same modular Yukawas yield resonantly enhanced CP asymmetries |ϵL,χ | ∼ 10−9 − 10−6 at MΣ ∼ 107 GeV, successfully generating the observed
baryon asymmetry ηB ≃ 6 × 10−10 and dark relic density Ωχ h2 ≃ 0.12 without additional
free parameters. The predicted correlation Ωχ /ΩB ≃ 5.4 fixes the dark matter mass to
mχ ≃ 0.1 − 2 GeV, consistent with all current constraints. This framework therefore realizes a fully predictive baryon−dark matter co-genesis, where the geometry of the modular
symmetry links the origin of flavor, CP violation, and the cosmic matter asymmetry.

## PDF page 2

Contents
1 Introduction

2

2 Model

4

3 Leptogenesis and Asymmetric Dark Matter
3.1 Co-genesis framework
3.2 Resonant CP asymmetries
3.3 Decay widths and branching ratios
3.4 Boltzmann evolution
3.5 Relic asymmetries and dark matter abundance

7
7
7
8
9
9

4 Numerical Analysis
4.1 Neutrino Sector
4.2 Baryon–Dark Matter Co-genesis
4.3 Correlation between CP Asymmetries and Relic Densities
4.4 Dependence on Dark Matter Mass and Benchmark Predictions

10
10
14
17
18

5 Conclusion

20

Appendix A: Essentials of Modular Symmetry and S4 Yukawa Multiplets

21

Appendix B: Standard Parameterization of Neutrino Observables

23

Appendix C: Boltzmann Framework and Scattering Integrals

23

Appendix D: Dependence on the Dark Yukawa Coupling yDM

24

–1–

## PDF page 3

1

Introduction

Neutrino physics continues to challenge the completeness of the Standard Model (SM) by
revealing phenomena that cannot be accommodated within its original structure. The
discovery of neutrino oscillations by Super–Kamiokande [1], SNO [2], and KamLAND [3]
firmly established that neutrinos possess tiny but nonzero masses, requiring new degrees of
freedom beyond the SM. At the same time, cosmological observations from Planck 2018 [4]
and DESI 2024 [5] determine the baryon and dark matter relic densities with high precision,
ΩB h2 = 0.0224 ± 0.0001,

Ωχ h2 = 0.120 ± 0.001,

(1.1)

yielding the striking ratio Ωχ /ΩB ≃ 5.4. The similarity of these two quantities, despite
their different microphysical origins, strongly hints at a common underlying mechanism
linking baryogenesis and dark matter genesis. Within the SM, however, CP violation from
the quark sector is insufficient by many orders of magnitude to account for the observed
baryon asymmetry ηB = 6.1 × 10−10 [4], and no viable dark matter candidate exists. These
facts motivate extensions of the SM that can simultaneously explain neutrino masses, CP
violation, the baryon asymmetry of the Universe (BAU), and the relic abundance of dark
matter—ideally from a single origin.
A particularly compelling approach to this problem is the asymmetric dark matter
(ADM) hypothesis [7, 40], in which the relic density of dark matter arises from a particle–
antiparticle asymmetry analogous to the baryon asymmetry in the visible sector. If both
asymmetries originate from a common process that violates lepton or baryon number in
the early Universe, their comparable abundances can be naturally explained. This idea
is realized in baryon–dark matter co–genesis models [8, 10, 11], where visible and hidden
asymmetries are generated simultaneously. Among the possible mechanisms, leptogenesis
remains one of the most attractive, as it connects the cosmic matter asymmetry with the
origin of neutrino masses [12, 13].
In standard thermal leptogenesis [13, 14], the CP–violating, out–of–equilibrium decays
of heavy Majorana neutrinos create a lepton asymmetry that is partially converted to a
baryon asymmetry through electroweak sphalerons. While this framework is elegant, it
typically requires very heavy right–handed neutrinos (MN ≳ 1010 GeV) [12]. By contrast,
in the resonant leptogenesis scenario [15, 16], a small mass splitting between nearly degenerate states can resonantly enhance the CP asymmetry, allowing successful baryogenesis
even for masses in the range MN ∼ 107 –109 GeV. In such cases, both the magnitude of the
asymmetry and its flavor dependence are determined by the underlying Yukawa structure
and CP phases.
The connection between leptogenesis and dark matter has been explored through several mechanisms in which the same heavy neutrino decays produce asymmetries in both
the visible and hidden sectors [8, 10, 11]. Depending on the structure of the portal interactions, the resulting dark matter typically lies in the GeV range, yielding the correct ratio
Ωχ /ΩB ∼ 5. Nevertheless, most existing constructions invoke multiple arbitrary couplings,
additional mediator fields, or fine-tuned parameters. A symmetry–based explanation in

–2–

## PDF page 4

which the flavor structure, CP phases, and portal couplings all emerge from a common
theoretical origin is still missing.
A natural step toward such a unified description arises from modular flavor symmetries [17, 18], a new paradigm that replaces the traditional flavon mechanism with modular
forms. In this approach, Yukawa couplings are modular functions of a single complex modulus τ , which transforms under finite modular groups such as A4 , S4 , or A5 . The vacuum
expectation value (vev) of τ determines the entire flavor structure, while its complex phase
provides an intrinsic source of CP violation. Modular invariant models have been shown
to reproduce realistic neutrino mixing patterns consistent with NuFIT global data [19–21].
However, their implications for leptogenesis and asymmetric dark matter have remained
largely unexplored.
In this work, we develop a modular S4 –invariant framework that realizes resonant co–
genesis of baryons and dark matter through a common source of CP violation determined
by the modulus τ . The modular symmetry fixes all Yukawa couplings, linking the flavor
structure of leptons directly to the parameters relevant for early–Universe asymmetry generation. The two quasi–degenerate fermionic triplets Σ1,2 responsible for neutrino mass
generation also drive the co–genesis process, establishing a direct connection between the
neutrino and dark sectors.
Our construction employs the Type–III seesaw mechanism [22, 23], in which the heavy
states are fermionic SU (2)L triplets with zero hypercharge. Unlike the singlet neutrinos of
the Type–I seesaw, the triplet fields couple directly to the electroweak gauge bosons, providing richer phenomenology and potentially testable signatures at colliders. The effective
light–neutrino mass matrix is generated through the relation
T
Mν ≃ −MD
MΣ−1 MD ,

(1.2)

where MD denotes the Dirac mass matrix and MΣ the mass of the heavy triplets. The
presence of SU (2)L interactions allows the triplet states to remain in equilibrium until
temperatures close to their mass scale, ensuring the correct washout dynamics for resonant
leptogenesis while naturally realizing a low seesaw scale (MΣ ∼ 107 GeV). Moreover, the
same modular structure that fixes MD also determines the couplings of Σi to the dark
sector, thereby linking neutrino masses, leptonic CP violation, and dark matter co–genesis.
We solve the coupled Boltzmann equations describing the simultaneous evolution of lepton
and dark asymmetries generated by Σ1 decays [15, 16],
• Σ1 → LH (lepton asymmetry Y∆L ) and Σ1 → χϕ (dark asymmetry Y∆χ ),
• including resonant CP violation, washout, and Σ–mediated transfer effects,
• with sphaleron conversion YB = (28/79)Y∆L ,
• yielding the DM relic ratio Ωχ /ΩB = (mχ /mp )|Y∆χ /Y∆L | [6].

–3–

## PDF page 5

All asymmetries are controlled by Re(τ ), Im(τ ) from the single modular parameter.
The remainder of this paper is organized as follows. Section 2 introduces the modular
S4 structure and the construction of the Yukawa couplings and the derivation of the neutrino mass matrices. Section 3 presents the Boltzmann framework describing co–genesis,
while Section 4 contains the numerical analysis and benchmark predictions. Finally, Section 5 summarizes our conclusions and outlines possible phenomenological implications,
including collider and gravitational–wave signatures.

2

Model

We consider a framework governed by the SM gauge symmetry SU (2)L × U (1)Y , extended
by a modular flavor symmetry S4 of level 3 [17] and a discrete stabilizing symmetry Z2DM [6].
The modular symmetry governs the flavor structure of leptons, while Z2DM ensures the
absolute stability of the dark matter candidate. In this construction, neutrino masses
arise via a type-III seesaw mechanism [22, 23], and the baryon asymmetry is generated
through leptogenesis [14]. A common fermion triplet mediator connects the visible and
dark sectors, providing a unified origin for both the lepton asymmetry and the dark matter
relic abundance [8].
The choice of the modular group S4 is motivated by its ability to reproduce realistic
lepton-mixing patterns through modular forms of low weight, avoiding the need for additional flavon fields [18]. Its vev ⟨τ ⟩ spontaneously breaks the modular invariance, fixing the
modular forms Yi (τ ) that determine the Yukawa structures of both visible and dark sectors.
For concreteness, τ is stabilized near the self-dual point τ = ω = e2πi/3 [41], where the
modular forms take fixed numerical values. The modular breaking scale Λmod ∼ 1010 GeV
lies above the seesaw mass scale MΣ ∼ 107 GeV, thereby establishing a clear hierarchy
between flavor generation and neutrino mass formation.
The field content and their transformation properties under SU (2)L ×U (1)Y ×S4 ×Z2DM
are summarized in Table 1. The model introduces a fermionic SU (2)L triplet Σ, which
plays a central role in neutrino mass generation and in mediating the visible–dark sector
connection. The scalar doublets Hu and Hd are the Higgs fields responsible for electroweak
symmetry breaking, while an additional scalar ϕ and a fermion χ constitute the dark sector.
The fields ϕ and χ are odd under Z2DM , while all other fields remain even, preventing dark
matter decay and ensuring the stability of χ [6].
The discrete parity Z2DM is assumed to be exact and unbroken by higher-dimensional
or gravitational operators. Operators such as (LHu )χ/Λ are forbidden since χ and ϕ are
odd under Z2DM whereas all other fields are even. Loop-induced corrections respect this
discrete symmetry, guaranteeing the stability of the dark fermion χ even in the presence
of Planck-suppressed effects.
The modular forms appearing in the Yukawa interactions transform as multiplets of S4
and are listed in Table 2. They carry modular weights corresponding to the order of
the modular function, which determines the allowed couplings in the Lagrangian. The

–4–

## PDF page 6

Table 1. Transformation properties of matter and Higgs fields under SU (2)L × U (1)Y × S4 × Z2DM .
The modular weights kI are indicated in the last row.

Field

L

lR 1

lR2

lR3

Σ

Hu

Hd

ϕ

χ

SU (2)L

2

1

1

1

3

2

2

3

2

U (1)Y

−1/2

−1

−1

−1

0

+1/2

−1/2

+1/2

−1/2

S4

3

1′

1

1′

2

1

1

1

2

Z2DM

+

+

+

+

+

+

+

−

−

kI

−2

0

−2

−2

−2

0

0

0

−2

Table 2. Transformation properties of modular Yukawa couplings under SU (2)L × U (1)Y × S4 ×
Z2DM . The modular weight kI corresponds to the form weight.

Y3

(2)

Y3′

(2)

Y1

(4)

Y3

(4)

Y3′

(4)

Y2

(4)

S4

3

3′

1

3

3′

2

kI

2

2

4

4

4

4

symmetry-breaking chain of the framework is expressed as
spontaneous modular breaking

EWSB

⟨τ ⟩

⟨Hu,d ⟩=v

S4modular × SU (2)L × U (1)Y ===================⇒ SU (2)L × U (1)Y ======⇒ U (1)em ,
(2.1)
where ⟨τ ⟩ generates the modular forms that fix the Yukawa structures, while the Higgs vev
v ≃ 246 GeV triggers electroweak symmetry breaking.
Each operator in the Lagrangian satisfies the modular weight conservation condition
∑
i ki + kY = 0, ensuring modular invariance [17]. Explicitly,
(2)

(LlR1 )3′ Hd Y3′ :

(−2) + (0) + (0) + (2) = 0,

(4)
(LΣ)3 Hu Y3 :
(4)
(Σχϕ)Y1 :

(−2) + (−2) + (0) + (4) = 0,
(−2) + (−2) + (0) + (4) = 0.

The complete Lagrangian of the model is written as
L = Lℓ + LD + LΣ + LDM ,

(2.2)

where the terms correspond to the charged-lepton, Dirac-neutrino, Majorana, and darkmatter portal sectors, respectively.
The charged-lepton Yukawa couplings consistent with the modular S4 symmetry take
the form
(2)

(4)

Lℓ = α(LlR1 )3′ Hd Y3′ + β(LlR2 )3 Hd Y3

–5–

(4)

+ γ(LlR3 )3′ Hd Y3′ + h.c.,

(2.3)

## PDF page 7

which, after electroweak symmetry breaking, leads to the charged-lepton mass matrix


α Y3
−2β Y2 Y3
2γ Y1 Y3

(√
) (√
)

(2.4)
Mℓ = vd 
α Y5 β 3 Y1 Y4 + Y2 Y5 γ 3 Y2 Y4 − Y1 Y5  .
(√
) (√
)
α Y4 β 3 Y1 Y5 + Y2 Y4 γ 3 Y2 Y5 − Y1 Y4
The Dirac neutrino mass term arises from
(4)

LD = αD (LΣ)3 Hu Y3

(4)

+ βD (LΣ)3′ Hu Y3′ + h.c.,

(2.5)

leading to the Dirac mass matrix MD :



−2αD Y2 Y3
−2βD Y1 Y3

(√
)
(
)
(
)
(
)
√
√
√


3
3
3
3
1
3
3
3
.
−α
Y
Y
+
Y
Y
+
β
Y
Y
−
Y
Y
α
Y
Y
+
Y
Y
+
β
−
Y
Y
+
Y
Y
MD = vu 
1
4
2
5
2
5
1
4
1
5
2
4
1
5
2
4
D
D
D
D
2
2
2
2
2
2
2
2




(√
)
(
)
(
)
(
)
√
√
√
3
3
3
3
1
3
3
3
−αD 2 Y1 Y5 + 2 Y2 Y4 + βD 2 Y2 Y4 − 2 Y1 Y5 αD 2 Y1 Y4 + 2 Y2 Y5 + βD − 2 Y1 Y4 + 2 Y2 Y5

(2.6)
The heavy Majorana mass term for Σ is given by
(
)
1
1
(4)
(4)
LΣ = M Y1 Tr(Σc Σ) + Mϵ Σc · Y2 ⊗ Σ + h.c.,
2
2
1
yielding
)
(
)
( ( 2
)
M Y1 + Y22 − Mϵ Y22 − Y12
Mϵ Y1 Y2
MΣ =
(
)
(
) .
Mϵ Y1 Y2
M Y12 + Y22 + Mϵ Y22 − Y12

(2.7)

(2.8)

The eigenvalues of MΣ correspond to two quasi-degenerate heavy Majorana mass eigenstates Σ1,2 with masses M1,2 , whose small modular-induced splitting enables resonant enhancement.
The light neutrino mass matrix is then obtained through the type-III seesaw relation,
T
,
Mν = −MD MΣ−1 MD

(2.9)

linking low-energy neutrino parameters directly to the modular structure.
Finally, the dark sector interacts through the portal coupling
(4)

LDM = yDM Tr[ Σ(χϕ) ] Y2

+ h.c.,

(2.10)

where χ is stabilized by the discrete symmetry ZDM
2 , and yDM denotes the dark-sector
Yukawa coupling that controls the strength of the portal interaction between the heavy
triplet Σ and the dark fields (χ, ϕ). After the breaking of the modular S4 symmetry, the
(4)
modular form Y2 (τ ) induces a specific flavor structure for the dark Yukawa coupling,
which can be written as
)
(
Y12 − Y22 2Y1 Y2
Yχ = yDM
.
(2.11)
2Y1 Y2 −Y12 + Y22
This interaction transfers the generated lepton asymmetry to the dark sector through Σ
exchange [8], resulting in correlated baryon and dark matter abundances. All coefficients
α, β, γ, αD , βD , M, Mϵ ∼ O(1) are real free parameters that can be traded for rescaled
modular forms Yi → αi Yi (τ = ω), whose values are fixed by requiring realistic mass
hierarchies consistent with oscillation data.

–6–

## PDF page 8

3

Leptogenesis and Asymmetric Dark Matter

In this section we describe a co-genesis scenario in which the BAU and the DM relic
abundance originate simultaneously from the CP-violating decays of nearly degenerate
heavy Majorana fermions [8, 9]. The framework relies on resonant leptogenesis [15] and
incorporates a modular S4 flavor structure, which ties the CP phases of the visible and
dark sectors to a common complex modulus τ [17].
3.1

Co-genesis framework

The two heavy triplet states Σ1,2 originate from the S4 doublet Σ introduced in Sec. 2.
A small mass splitting ∆MΣ = |M2 − M1 | is induced by the modular-symmetry–breaking
parameter Mϵ in Eq. (2.8), naturally realizing the quasi-degenerate spectrum required for
resonant enhancement [15].
The relevant interactions governing leptogenesis and dark-matter asymmetry generation are
1
L ⊃ −(Yν )αi Lα H̃u Σi − (Yχ )i χ ϕ Σi − Σci (MΣ )ij Σj + h.c.,
(3.1)
2
where H̃u = iσ2 Hu∗ .
The modular forms determining these couplings follow from the assignments in Sec. 2:
(4)

Yν ∝ αD Y3

(4)

(4)

Yχ ∝ yDM Y2 ,

+ βD Y3′ ,

(4)

MΣ = M Y1

(4)

+ Mϵ Y2 .

Hence the CP phases in both Yν and Yχ originate from the same complex modulus τ .
The heavy fermions Σi decay through two competing channels,
Σi → LHu ,

Σi → χϕ,

(3.2)

producing CP asymmetries in both the visible and dark sectors. Since the dark scalar ϕ
does not acquire a vev, it acts purely as a final-state field, ensuring the stability of the dark
sector.
For the lighter state Σ1 , the CP asymmetries are defined as
Γ(Σ1 → LHu ) − Γ(Σ1 → L̄Hu† )
ϵL =
,
ΓΣ1

ϵχ =

Γ(Σ1 → χϕ) − Γ(Σ1 → χ̄ϕ† )
,
ΓΣ1

(3.3)

where ΓΣ1 denotes the total decay width of Σ1 .
3.2

Resonant CP asymmetries

In the resonant regime, the CP asymmetry is dominated by self-energy diagrams involving
the nearly degenerate states Σi and Σj (i ̸= j) see in Fig. 1 [15, 16, 24]. Neglecting vertex
corrections and keeping only the resonantly enhanced self-energy piece, the CP asymmetries
are
[
(
)]
(0)
Im (Yν† Yν )ij (Yν† Yν + 2Yχ† Yχ )ij
(Mi2 − Mj2 ) Mi Γj
i
,
(3.4)
ϵL =
(0)2
8π (Yν† Yν + Yχ† Yχ )ii
(Mi2 − Mj2 )2 + Mi2 Γj
[
(
)]
(0)
Im (Yχ† Yχ )ij (2Yν† Yν + Yχ† Yχ )ij
(Mi2 − Mj2 ) Mi Γj
i
,
(3.5)
ϵχ =
(0)2
8π (Yν† Yν + Yχ† Yχ )ii
(Mi2 − Mj2 )2 + Mi2 Γj

–7–

## PDF page 9

(a)

(d)

(b)

(c)

(e)

(f)

Figure 1. One–loop self–energy diagrams contributing to the CP asymmetries in the visible and
dark sectors. The interference between tree–level and loop processes with intermediate triplet
exchange induces unequal decay rates into ℓα H and χϕ versus their CP–conjugate channels.

where the tree-level width is
(0)

Γj

≃

]
Mj [ †
(Yν Yν )jj + (Yχ† Yχ )jj ,
8π

including both CP-conjugate decay channels in the standard total-width normalization.
3.3

Decay widths and branching ratios

The total decay width of Σ1 is
ΓΣ1 = Γ(Σ1 → LHu ) + Γ(Σ1 → χϕ),

(3.6)

with partial widths
Γ(Σ1 → LHu ) =

M12
m̃1 ,
8πvu2

Γ(Σ1 → χϕ) =

M12
m̃dm ,
8πvu2

(3.7)

which can be expressed in terms of the effective mass parameters
m̃1 =

|Yν |2 vu2
,
M1

m̃dm =

|yχ |2 vu2
.
4M1

(3.8)

The factor 1/4 in m̃dm arises from the SU(2)L normalization of the triplet coupling. This
normalization is consistently included in the total width appearing in the CP-asymmetry
denominators.
The branching ratios into visible and dark sectors are therefore
BrL =

Γ(Σ1 → LHu )
,
ΓΣ1

Brχ =

Γ(Σ1 → χϕ)
,
ΓΣ1

(3.9)

where the dark Yukawa coupling contributes with an effective weight of 1/4 in the total
width, as reflected in Brχ through m̃dm .

–8–

## PDF page 10

Figure 2. Feynman diagrams contributing to the 2 → 2 scattering processes entering the Boltzmann
equations (3.11) and (3.12). The top row shows the ∆L = 2 processes responsible for lepton-numberviolating washout, while the bottom row displays the ∆L = 0 transfer processes that mediate the
exchange of the asymmetry between the visible and dark sectors.

3.4

Boltzmann evolution

Defining the washout parameter K1 ≡ ΓΣ1 /H(z = 1), the coupled Boltzmann equations [8]
for the comoving abundances YΣ1 = nΣ1 /s, Y∆L = YL − YL̄ , and Y∆χ = Yχ − Yχ̄ are
)
Γ1
K1 (z) (
dYΣ1
=−
z
YΣ1 − YΣeq1 ,
dz
H(z = 1) K2 (z)
[
)
Γ1
K1 (z) ( eq
dY∆L
=−
ϵL z
YΣ1 − YΣ1 + 2Br2L IW (z) Y∆L
dz
H(z = 1)
K2 (z)
)]
(
+ BrL Brχ IT+ (z) (Y∆L + Y∆χ ) + IT− (z) (Y∆L − Y∆χ ) ,

(3.11)

[
)
dY∆χ
Γ1
K1 (z) ( eq
=−
ϵχ z
YΣ1 − YΣ1 + 2Br2χ IW (z) Y∆χ
dz
H(z = 1)
K2 (z)
)]
(
+ BrL Brχ IT+ (z) (Y∆L + Y∆χ ) − IT− (z) (Y∆L − Y∆χ ) ,

(3.12)

(3.10)

where H(z) is the Hubble rate in the radiation-dominated era and K1,2 (z) are modified
Bessel functions. The functions IW (z) and IT± (z) encode thermally averaged washout and
transfer contributions from inverse decays and off-shell Σ1 -mediated scatterings [8, 42], as
detailed in Appendix C. These equations capture the interplay among decay, washout, and
transfer processes that shape both asymmetries, as illustrated in Fig. 2.
3.5

Relic asymmetries and dark matter abundance

After Σ1 decays freeze out, Y∆L and Y∆χ become conserved. The lepton asymmetry is
partially converted into a baryon asymmetry by electroweak sphalerons,
YB = csph Y∆L ,

–9–

csph =

8
,
23

(3.13)

## PDF page 11

which assumes Standard Model field content and efficient sphaleron conversion above the
electroweak scale [13]. The symmetric component of χ annihilates efficiently through tchannel ϕ exchange since mχ ≃ 0.1−2 GeV ≪ mϕ ≃ 100 GeV, rendering χχ̄ → ϕϕ kinematically forbidden, leaving only the asymmetric relic contribution relevant at late times.
The present-day energy-density ratio of dark matter to baryons is
mχ |Y∆χ |
Ωχ
=
,
ΩB
mp |Y∆L |

(3.14)

where mp is the proton mass. The observed ratio Ωχ /ΩB ≃ 5.4 [4] implies that comparable
visible and dark asymmetries naturally correspond to mχ ≃ 0.1−2 GeV.
∞ and
Once Σ1 has decayed completely, the asymmetries saturate to constant values Y∆L
∞
Y∆χ , leading to [40]
2

Ωχ h =
and therefore

∞|
mχ s0 |Y∆χ

ρc /h2

,

ρc /h2 = 1.05 × 10−5 GeV cm−3 ,

∣
∣
∣
∣
∣Y ∞ ∣
∞ ∣
Ωχ ∣∣ Y∆L
∣
∣
∣
mχ ≃ mp
∣ ∞ ∣ ≃ 5.4 mp ∣ ∆L
∞ ∣∣ .
∣
∣ Y∆χ
ΩB ∣ Y∆χ

(3.15)

(3.16)

If Brχ > BrL , the dark asymmetry is larger and Eq. (3.16) predicts a correspondingly heavier ADM candidate, linking the DM and neutrino mass scales through the same modular
origin of CP violation.
Overall, this framework quantitatively connects neutrino masses, baryon asymmetry, and
dark matter abundance, all governed by the common modular parameter τ that controls
both flavor and CP violation.

4

Numerical Analysis

4.1

Neutrino Sector
Table 3. NuFIT 5.2 (2024) best-fit values and 3σ ranges for normal hierarchy.

Parameter

Best-fit ± 1σ

3σ range

sin2 θ12

0.307+0.012
−0.011
0.561+0.012
−0.015
0.02195+0.00054
−0.00058
+0.19
7.49−0.19
2.534+0.025
−0.023

0.275 − 0.345

2

sin θ23
sin2 θ13
∆m221 [10−5 eV2 ]
∆m231 [10−3 eV2 ]

0.430 − 0.596
0.02023 − 0.02376
6.92 − 8.05
2.463 − 2.606

The numerical analysis has been performed for the normal hierarchy of neutrino masses
within the modular S4 framework. The light-neutrino mass matrix is obtained from the
T [22, 23], where all entries of M
type-III seesaw relation Mν = −MD MΣ−1 MD
D and MΣ
are determined by the modular forms Yi (τ ) defined in Appendix A. The physical lepton

– 10 –

## PDF page 12

101

100

100

10 1

10 1

10 2

10 2

|Yi |

|Yi |

101

10 3

|Y1 |
|Y2 |
|Y3 |
|Y4 |
|Y5 |

10 4
10 5
10 6
1.35

1.40

1.45

1.50

Re( )

10 3
10 4
10 5

1.55

1.60

1.65

10 6

2.5

2.6

2.7

Im( )

2.8

|Y1 |
|Y2 |
|Y3 |
|Y4 |
|Y5 |

2.9

3.0
0.7
0.6

2.8

0.5

2.7

0.4

2.6

0.3

χ2

Im τ

2.9

0.2

2.5

0.1

2.4
1.35 1.40 1.45 1.50 1.55 1.60 1.65

Re τ

Figure 3. Allowed region of the complex modulus τ in the modular S4 framework. Upper: absolute
values of modular Yukawa forms |Yi | versus Re τ (left) and Im τ (right). Lower: χ2 distribution in
the (Re τ, Im τ ) plane. All displayed points lie within the NuFIT 5.2 3σ ranges.

mixing matrix is constructed as UPMNS = Uℓ† Uν [26], with Uℓ and Uν diagonalizing Mℓ Mℓ†
and Mν , respectively. All oscillation observables are computed in the standard PMNS
parametrization,1 and the resulting predictions are compared with the NuFIT 5.2 (2024)
global analysis for normal ordering [27]. The corresponding 3σ ranges are summarized in
Table 3.
The input parameters are varied within the domains
1.0 < Re τ < 2.0,

0.5 < Im τ < 3.0,

0.5 < α < 1.6,

0.3 < β < 1.1,

1.0 < γ < 1.6,

10−5 < βD < 10−3 ,

5 × 102 GeV < M < 5 × 103 GeV,

10−3 < αD < 10−2 ,
105 GeV < Mϵ < 5 × 107 GeV.

For each parameter set, the modular Yukawa couplings are determined by the chosen
τ , thereby fixing the flavor structure entirely through the S4 modular forms [17]. The
resulting parameter space is constrained by the NuFIT 5.2 3σ limits on mixing angles and
∑
mass-squared differences [27], as well as the Planck bound
mν < 0.12 eV [4].
1

Explicit definitions of sin2 θij , δCP , and mββ are given in Appendix B.

– 11 –

## PDF page 13

0.5
0.4

0.1
0.06

0.08

0.10

Σmν [eV]

0.12

0.0240

χ2

sin 2 θ23

0.50

0.2

0.45

0.1
0.06

0.08

0.10

Σmν [eV]

Excluded region

0.0235

0.14

0.5

0.0230

0.4

0.0225

0.3

0.0220

0.12

χ2

sin 2 θ13

0.3

0.40

0.14

0.5
0.4

0.55

0.3
0.2

Excluded region

0.60

χ2

sin 2 θ12

Excluded region

0.34
0.33
0.32
0.31
0.30
0.29
0.28
0.27

0.0215

0.2

0.0210

0.1

0.0205
0.06

0.08

0.10

Σmν [eV]

0.12

0.14

∑
Figure 4. Correlations between the total neutrino mass
mν and the mixing angles sin2 θ12
(upper left), sin2 θ23 (upper right), and sin2 θ13 (lower panel). Dashed lines denote the 3σ ranges
∑
from NuFIT 5.2, and the shaded band shows the cosmological bound
mν < 0.12 eV.

The region of the complex modulus τ consistent with neutrino oscillation data is displayed in Fig. 3, showing that acceptable solutions cluster around two narrow bands near
Re τ ≃ 1.35 and Re τ ≃ 1.63 with Im τ ≃ 2.6–2.8. These regions correspond to points where
the modular Yukawa structures reproduce all neutrino mixing angles and mass-squared differences within the 3σ NuFIT 5.2 ranges, thereby phenomenologically fixing the modulus.
In this framework, τ is not stabilized by an explicit potential but is effectively determined
by requiring simultaneous agreement with low-energy neutrino observables, a standard approach in modular-flavor analyses [32, 43]. The localization of τ close to the self-dual point
ω = e2πi/3 reflects the geometric properties of modular forms, which naturally yield hierarchical and stable Yukawa textures in this region. The magnitudes of the modular couplings
exhibit the ordering |Y1 | ≫ |Y3 | > |Y2 | > |Y4 | > |Y5 | as shown in upper panel of Fig. 3,
consistent with realistic lepton mass hierarchies. The apparent flatness of the modular
Yukawas arises from the exponential suppression of higher-order q-terms (q = e2πiτ ) for
large Im τ , leading to quasi-degenerate modular textures in a phenomenologically preferred
τ region that simultaneously accounts for flavor and CP observables.
∑
The correlations between
mν and the mixing angles are shown in Fig. 4. All viable
∑
points lie below the cosmological limit
mν < 0.12 eV and fall within the 3σ regions of
∑
the global fit. The results indicate
mν ≃ (0.06–0.08) eV, sin2 θ12 ≃ 0.30, sin2 θ23 ≃ 0.57,

– 12 –

## PDF page 14

0.7

100

0.6

100

0.6

50

0.5

50

0.5

0

0.4

0

0.4

50

0.3

50

0.3

100

0.2

100

0.2

150

0.1

150

0.1

0.525 0.550 0.575 0.600 0.625

100

sin 2 θ23

0

α21 [°]

χ2

150

α31 [°]

0.7

χ2

δCP [°]

150

100

Figure 5. Left: correlation between δCP and sin2 θ23 , showing near-maximal CP violation. Right:
predicted Majorana phase structure (α21 , α31 ) exhibiting discrete clustering near (0, π) and (±π/2),
a distinctive imprint of the modular symmetry.

and sin2 θ13 ≃ 0.022, providing an excellent match to data and confirming that the model
favors the normal ordering.
The atmospheric mixing angle and CP phase satisfy sin2 θ23 ≃ 0.56–0.59 and δCP ∈
[±150◦ , ±180◦ ], as displayed in Fig. 5, implying nearly maximal CP violation. The predicted Majorana phases cluster around (0, π) and (±π/2), reflecting the discrete modular
structure of the Yukawa sector.
100

KamLAND-Zen

10 2

LEGEND-1000
nEXO

0.8
0.6

χ2

mββ [eV]

Disfavored by KamLAND-Zen
10 1

Disfavored by Cosmology

1.0

0.4

10 3

4
10 10
4

0.2

10 3

10 2

m1 [eV]

10 1

100

0.0

Figure 6. Effective Majorana mass mββ versus the lightest neutrino mass m1 . Colored bands
denote the current and projected sensitivities of KamLAND-Zen, LEGEND-1000, and nEXO.

The effective Majorana mass relevant for neutrinoless double beta decay, mββ =
2 + m U 2 + m U 2 | [28], is found to be in the range m
−3 eV,
|m1 Ue1
2 e2
3 e3
ββ ≃ (8–18) × 10
as shown in Fig. 6. This lies below the current KamLAND-Zen bound [29] but within the

– 13 –

## PDF page 15

future reach of nEXO [31] and LEGEND-1000 [30].
The modular S4 framework with type-III seesaw successfully reproduces all neutrino oscillation observables within 3σ without fine-tuning, with the entire flavor structure governed
by a single modulus τ . Since the same Yukawa couplings (Yν ) and triplet masses (M1 , M2 )
also control the decay asymmetries of the heavy fermions, these neutrino-determined parameters directly constrain the CP-violating sources for leptogenesis. The next section
explores how this common structure naturally links baryon asymmetry and dark matter
relic abundance through resonant co-genesis.
4.2

Baryon–Dark Matter Co-genesis

Having established the theoretical setup in Section 3, we now present a detailed numerical
study of the correlated generation of the baryon asymmetry and ADM within the neutrinoviable modular S4 framework. All Yukawa couplings, CP phases, and decay parameters
entering leptogenesis are derived from the modular forms Yi (τ ) fixed by the same complex
modulus τ that governs the neutrino sector. Hence, no additional free phases are introduced
for baryogenesis or ADM production [32].
The CP asymmetries ϵL and ϵχ are evaluated using the modular Yukawa structures
defined in Eqs. (3.4)–(3.5), within the neutrino-consistent parameter space obtained in
Section 4. The phenomenologically relevant region of the complex modulus τ is restricted
to two narrow bands centered at Re τ ≃ 1.37 and 1.64 with Im τ ≃ 2.6–2.8, where the
modular forms develop sizable imaginary components. For each allowed τ , the corresponding Yukawa matrices (Yν , Yχ ) are constructed and inserted into the loop-induced decay
asymmetry expressions, yielding the visible and dark sector CP parameters ϵL and ϵχ .
The relative magnitudes of ϵL and ϵχ are further controlled by the portal coupling yDM
appearing in Eqs. (2.10). Although the modular structure fixes the relative phases of the
two sectors, the value of yDM determines their relative decay branching fractions and hence
the dominant source of CP violation. For yDM ≲ 10−3 , the dark decay Σ1 → χϕ dominates,
yielding a larger dark asymmetry. At yDM ∼ 10−2 , the visible and dark CP asymmetries
become nearly identical, |ϵL | ≃ |ϵχ |, reflecting their common modular origin. This regime
corresponds to balanced co-genesis, where both sectors freeze out with comparable asymmetries. A representative illustration of the yDM dependence of the CP asymmetry ratio
is provided in Appendix D, confirming the robustness of our numerical results.
The resulting distributions of |ϵL | and |ϵχ | as functions of the heavy-triplet mass M1
are shown in Fig. 7, while the variation of |ϵL | in the complex τ plane is displayed in Fig. 8.
Both quantities lie in the range 10−9 –10−6 throughout the neutrino-viable parameter space,
sufficient to account for the observed baryon asymmetry after including washout effects.
The mild spread visible in Fig. 7 thus reflects not only the small modular-phase differences
but also the variation in yDM that controls the visible–dark balance.
The resonant enhancement characteristic of this regime amplifies the CP violation by
a factor of O(102–3 ), compensating for the relatively small Yukawa couplings |Yν,χ | ∼ 10−3
without the need for any fine-tuning. Although both ϵL and ϵχ are governed by the same
complex modulus τ , they are not exactly proportional. The visible-sector Yukawa matrix
(4)
(4)
(4)
Yν ∼ (Y3 , Y3′ ) and the dark-sector coupling Yχ ∼ Y2 transform under different S4

– 14 –

## PDF page 16

10 6

10 6

10 7

10 7

| |

| L|

multiplets and carry distinct modular weights. As a result, their complex phases are
correlated but not identical, leading to comparable—though not perfectly matched—CP
asymmetries in the two sectors. This feature is evident in Figs. 7(a,b), where both |ϵL | and
|ϵχ | cluster around the same order of magnitude but exhibit visible scatter. The heatmap
in Fig. 8 further highlights that the maximal CP violation occurs precisely within the
neutrino-viable τ bands, confirming that, in this framework, the imaginary part of τ acts
as the sole physical source of CP violation.

10 8

10 8

2 × 107

3 × 107

M1 [GeV]

4 × 107

6 × 107

2 × 107

3 × 107

4 × 107

6 × 107

3 × 107

4 × 107

6 × 107

M1 [GeV]

10 6

10 6
10 7

| |

| L|

10 7
10 8

10 8

10 9

2 × 107

3 × 107

4 × 107

M1 [GeV]

6 × 107

2 × 107

M1 [GeV]

Figure 7. CP asymmetries as functions of the lightest heavy-triplet mass M1 for two representative
values of the dark-sector Yukawa coupling yDM . Upper panels: yDM = 10−2 (balanced co-genesis
regime with |ϵL | ≃ |ϵχ |); lower panels: yDM = 10−3 (dark-dominated regime with |ϵχ | > |ϵL |). Left:
visible-sector asymmetry |ϵL |; right: dark-sector asymmetry |ϵχ |.

To illustrate the quantitative realization of perfect co-genesis, we select benchmark
points (BP1–BP4) from the neutrino-oscillation consistent τ region, each reproducing the
observed baryon asymmetry and dark matter relic density within the 3σ NuFIT 5.2 limits.
The corresponding parameters and cosmological observables are summarized in Table 4.
These benchmarks serve as representative examples for the subsequent Boltzmann evolution.
The left panel presents the thermally averaged decay, washout, and transfer rates
normalized to the Hubble expansion. At early times (z = M1 /T < 1) the total decay rate
ΓD /H is several orders of magnitude above unity, keeping Σ1 in thermal equilibrium. As
the Universe cools and z approaches unity, the decay rate falls below the Hubble expansion,

– 15 –

## PDF page 17

2.9
10 7

2.7

10 8

| L|

Im( )

2.8

2.6

10 9

2.5
1.35

1.40

1.45

1.50

Re( )

1.55

1.60

1.65

10 10

108
106
104
102
100
10 2
10 4
10 6
10 8 2
10

102

102
100
10 2
10 4
10 6
10 8
10 10
10 12
10 14 2
10

102

102
100
10 2
10 4
10 6
10 8
10 10
10 12
10 14 2
10

D/H

W/H
T/H

Y

108
106
104
102
100
10 2
10 4
10 6
10 8 2
10

10 1

100

z = M1/T

101

D/H
W/H
T/H

Y

/H

/H

Figure 8. Magnitude of the CP asymmetry |ϵL | in the complex τ plane. The two allowed τ
bands around Re τ ≃ 1.37 and 1.64 with Im τ ≃ 2.6–2.8 coincide with the neutrino-viable region,
confirming that the imaginary part of τ acts as the sole physical source of CP violation.

10 1

100

z = M1/T

101

YN
|Y L|
|Y |
YNeq

10 1

100

z = M1/T

101

102

YN
|Y L|
|Y |
YNeq

10 1

100

z = M1/T

101

Figure 9. Boltzmann evolution for benchmark points BP4 (upper row, yDM = 10−2 , balanced
cogenesis) and BP1 (lower row, yDM = 10−3 , dark-dominated). Left: thermally averaged decay,
washout, and transfer rates as functions of z = M1 /T . Right: comoving yields of the heavy triplet
and the lepton and dark asymmetries. Both asymmetries freeze out around z ≳ 6, with co-genesis
realized near intermediate yDM values.

– 16 –

102

## PDF page 18

Table 4. Benchmark points illustrating the transition between dark- and balanced co-genesis
regimes. All benchmarks reproduce the observed baryon asymmetry and dark relic density within
uncertainties.
Point

τ

M1 [107 GeV]

|ϵL |

|ϵχ |

yDM = 10
BP1
BP2

1.37 + i2.63
1.64 + i2.57

−3

ηB

Ω χ h2

Ωχ /ΩB

mχ [GeV]

(dark-dominated)

1.9

2.3×10−8

4.3×10−7

4.6×10−10

0.10

4.03

0.97

2.1

−8

−8

−10

0.116

5.19

0.70

3.05×10

7.72×10

5.9×10

yDM = 10−2 (balanced cogenesis)
BP3
BP4

1.64 + i2.52
1.37 + i2.69

1.96

3.17×10−8

3.19×10−8

6.15×10−10

0.121

5.4

1.78

4.16

−8

−8

6.5×10−10

0.12

5.7

1.76

3.37×10

3.39×10

marking the onset of the out-of-equilibrium regime required by the Sakharov conditions.
The washout (W/H) and transfer (T /H) processes remain much smaller than unity during
this epoch, ensuring that the generated asymmetries are only mildly erased.
The Boltzmann evolution of the heavy triplet and the resulting asymmetries is shown
in Fig. 9 (right panel) for representative portal couplings yDM = 10−3 and 10−2 , corresponding respectively to benchmark points BP1 (dark-dominated) and BP3 (balanced
co-genesis) listed in Table 4. In both cases, the triplet remains in thermal equilibrium
for z < 1 and departs near z ≃ 1, satisfying the out-of-equilibrium condition required
for leptogenesis. Once the decays of Σ1 become inefficient (z ≳ 1), CP-violating decays
generate simultaneous lepton and dark asymmetries. The comoving yields YN , |Y∆L |, and
|Y∆χ | evolve as shown in the right panels of Fig. 9: both asymmetries grow and freeze out
around z ≳ 6, when ΓD /H ≪ 1. For small yDM , the dark yield |Y∆χ | dominates, while
at larger yDM the visible and dark yields become comparable, reflecting their nearly equal
CP asymmetries. The balanced co-genesis regime is therefore realized around yDM ∼ 10−2 ,
∞ | ≃ |Y ∞ |. Other benchmark points exhibit qualitatively similar evolution with
where |Y∆L
∆χ
only mild variations in the final asymmetry ratios, so BP1 and BP3 sufficiently illustrate
the generic behavior of the co-genesis dynamics in this framework.
4.3

Correlation between CP Asymmetries and Relic Densities

The solutions of the coupled Boltzmann equations (3.10)–(3.12) for the benchmark points in
∞ and Y ∞ , which are subsequently converted into the
Table 4 yield the final asymmetries Y∆L
∆χ
baryon and dark matter relic abundances through Eqs. (3.13)–(3.15) [33]. Fig. 10 illustrates
the numerical correlation between microscopic CP asymmetries (ϵL , ϵχ ) and macroscopic
observables ηB and Ωχ h2 . Both balanced cogenesis and dark-sector dominated regimes
are included in this combined τ -scan. Their contributions appear as a mild spread in the
correlation plots, reflecting the small variations of the branching ratios and CP phases
across the parameter space.
At fixed heavy-triplet mass M1 , both ηB and Ωχ h2 scale linearly with the corresponding
CP asymmetries for small |ϵL,χ |, as expected when washout is not yet saturated. Beyond
this range, partial washout effects flatten the growth of the generated asymmetries, reflecting the onset of asymmetry damping. Across the neutrino-viable τ region, the baryon
obs = (6.12 ± 0.03) × 10−10 [4], while
asymmetry consistently falls near the observed value ηB

– 17 –

## PDF page 19

100
10 2

B

h2

100

10 4

h2

Asymmetries / Relic Density

the dark relic density matches the Planck constraint Ωχ h2 = 0.12 ± 0.001, demonstrating
that both sectors reach the correct magnitudes without additional parameter tuning. Because ϵχ tracks ϵL up to O(1) factors, the linear trend with |ϵL | in Fig. 10(a) effectively
captures the behavior of both CP sources.
Numerically, the ratio Ωχ /ΩB stabilizes in a narrow band Ωχ /ΩB ≃ 5–7, fully consistent with the cosmological value Ωχ /ΩB ≃ 5.4. The mild spread arises from small O(1)
differences between the modular phases of Yν and Yχ , confirming that the co-genesis correlation originates directly from the modular flavor geometry rather than from any ad-hoc
phase tuning.

10 6
10 8

All points
Viable points
Observed B
Observed h 2

10 1
10 2

10 10
10 9

10 8

| L|

10 7

10 6

10 3
10 11

10 10

B

10 9

10 8

Figure 10. Correlation between microscopic CP asymmetries and macroscopic relic observables.
(a) Baryon asymmetry ηB (blue) and dark matter relic density Ωχ h2 (red) as functions of the CP
asymmetry |ϵL |, showing linear scaling in the regime of unsaturated washout and mild saturation
at larger values. (b) Direct correlation between Ωχ h2 and ηB for all τ points (blue) and neutrinoobs
viable points (red stars), demonstrating co-genesis near the observed values ηB
= 6.12 × 10−10
and Ωχ h2 = 0.12.

Overall, the modular S4 structure enforces a robust correlation at the order-of-magnitude
level between ϵL , ϵχ , and the final relic abundances. Since the same modulus τ governs
both visible and dark CP violation, the observed Ωχ /ΩB ratio emerges naturally from the
modular geometry, providing a unified and predictive framework for baryon–dark matter
co-genesis. Because ϵχ tracks ϵL up to O(1) factors, the linear trend with |ϵL | in Fig. 10
effectively captures the behavior of both CP sources. For clarity, we present the correlation
using the dark-sector asymmetry |ϵχ | follows the same trend due to their common modular
origin and comparable magnitudes across the viable parameter space.
4.4

Dependence on Dark Matter Mass and Benchmark Predictions

To further quantify the co-genesis mechanism, we analyze the dependence of the dark
matter relic density Ωχ h2 and the ratio Ωχ /ΩB on the dark fermion mass mχ . The results
are obtained by solving the Boltzmann equations for the benchmark points in Table 4,
keeping all other parameters fixed to their neutrino-viable modular values.
Figure 11 shows that both quantities scale approximately linearly with mχ once the
∞ and Y ∞ have frozen out. In this regime, the relic
dark and visible asymmetries Y∆χ
∆L
2
∞ |, and the ratio Ω /Ω increases proportionally with
abundance follows Ωχ h ∝ mχ |Y∆χ
χ
B

– 18 –

## PDF page 20

mχ . All benchmark trajectories nearly coincide, indicating that the freeze-out asymmetries
are very similar throughout the neutrino-consistent τ region. The intersection with the
observed Planck values, Ωχ h2 = 0.120 ± 0.001 and Ωχ /ΩB ≃ 5.4 [4], occurs for
mχ ≃ (0.1–2) GeV,

(4.1)

in excellent agreement with the numerical benchmarks in Table 4.
105

=(1.37+2.69i)
=(1.63+2.63i)
=(1.37+2.65i)
=(1.37+2.54i)
=(1.37+2.63i)
=(1.64+2.57i)
=(1.37+2.59i)
=(1.37+2.70i)
=(1.64+2.47i)
Observed ~5.4

/ B

103
102
101

= (1.37 + 2.69i)
= (1.63 + 2.63i)
= (1.37 + 2.65i)
= (1.37 + 2.54i)
= (1.37 + 2.63i)
= (1.64 + 2.57i)
= (1.37 + 2.59i)
= (1.37 + 2.70i)
= (1.64 + 2.47i)
Observed h 2 = 0.12

103
102

h2

104

101
100
10 1

100

10 2

10 1

10 3
10 2

10 1

100

101

102

m [GeV]

103

104

10 2

10 1

100

101

102

m [GeV]

103

104

Figure 11. Dependence of the relic abundances on the dark matter mass mχ for the benchmark
points in Table 4. Left: ratio Ωχ /ΩB as a function of mχ . Right: dark matter relic density
Ωχ h2 versus mχ . Both show an approximately linear trend once the asymmetry is frozen, and all
benchmark trajectories nearly coincide, reflecting the small spread of freeze-out asymmetries across
the viable τ region.
∞ and Y ∞ , the
Because the same τ -controlled CP asymmetries determine both Y∆L
∆χ
preferred value mχ ≃ 0.5–2 GeV effectively encodes neutrino-sector information in the dark
matter mass prediction. The resulting mχ is therefore not imposed by hand, but emerges
naturally from the modular S4 dynamics that govern both visible and dark asymmetry
generation.

Remarks on theoretical assumptions. The present analysis is based on the supersymmetric modular S4 framework, so it is worth clarifying how the different energy scales
remain consistent within the framework. The model is analyzed in the effective nonsupersymmetric limit, yet it can naturally arise from a supersymmetric or supergravity
completion in which the modulus τ and its associated modular functions Yi (τ ) originate
from a chiral modulus field. Supersymmetry breaking may be represented by a spurion
field X = θ2 F , which transmits soft terms of typical size mSUSY ≃ F/Mmess , where Mmess
is the mediation scale[17].
In the parameter range explored here, the heavy fermionic triplets have characteristic
masses
MΣ ∼ 107 GeV,
while the dark matter mass remains in the few–GeV regime. A plausible and phenomenologically stable hierarchy of
mSUSY ∼ 106–8 GeV,

Mmess ∼ 1014–16 GeV,

– 19 –

## PDF page 21

leads to a ratio mSUSY /Mmess ≲ 10−8 , which keeps any supersymmetric threshold effects
on the modular Yukawa structure extremely small.
Because of this suppression, the modular flavor relations remain radiatively stable,
and the predictions derived from them are not distorted by higher-scale corrections. Furthermore, all possible superpartners are expected to decouple well before the leptogenesis
epoch, leaving a consistent low-energy theory that contains only the Standard Model fields,
the fermionic triplets Σi , and the dark-sector fields (χ, ϕ). This ensures that the effective
description used in our analysis remains valid throughout the relevant cosmological evolution.
Time dependence of the CP asymmetry. In resonant leptogenesis, a full quantum
treatment reveals that the CP asymmetry ϵ(t) can exhibit oscillatory time dependence
when the mass splitting ∆M becomes comparable to the decay width Γ [34]. In the
present analysis, we employ the standard momentum-averaged Boltzmann formalism [35],
using time-independent asymmetries ϵL,χ derived from the one-loop decay amplitudes. For
the benchmark parameters ∆M/M1 = 10−3 –10−5 and Γ/M1 ∼ 10−6 , the coherence time
of the quasi-degenerate states is much shorter than the timescale of asymmetry generation,
so any oscillations in ϵ(t) are effectively averaged out. Consequently, the time-averaged
asymmetry provides an accurate estimate of the integrated baryon yield [36]. Comparisons
with quantum-kinetic treatments indicate that deviations from the time-independent approximation remain at the level of at most O(10%) in this regime, validating the use of the
static approximation for the parameter space considered here.
Flavour effects. Flavour-dependent washout effects can in principle become relevant
for M1,2 ≲ 1012 GeV [37, 38]. However, in the present modular framework, the Yukawa
structures yield nearly aligned flavour projectors [39], so the heavy-triplet decays effectively produce a single coherent lepton state. In this case, the total lepton asymmetry is
well described by the single-flavour Boltzmann equations employed here. A fully flavourresolved treatment would primarily redistribute the asymmetry among e, µ, τ flavours and
is expected to alter the final baryon asymmetry only at the O(1) level, without affecting
our qualitative co-genesis conclusions.

5

Conclusion

In this work we have presented a unified framework for neutrino masses, baryogenesis, and
dark matter based on a modular S4 symmetry with a type-III seesaw mechanism. The
model simultaneously explains the observed neutrino oscillation data and the cosmological baryon and dark matter relic abundances through a common origin in the complex
modulus τ , which determines all Yukawa couplings and CP phases.
A detailed numerical analysis was performed for the normal hierarchy of neutrino
masses. The modular structure naturally restricts τ to narrow viable bands around Re τ ≃
1.35 and 1.64 with Im τ ≃ 2.6–2.8, where the modular forms reproduce the observed mixing
angles and mass-squared differences within the 3σ ranges of the NuFIT 5.2 (2024) global
fit. The framework predicts a nearly maximal leptonic CP phase δCP ≃ ±(150◦ − 180◦ )

– 20 –

## PDF page 22

and an effective Majorana mass mββ ≃ (8–18) × 10−3 eV, which lies below the present
KamLAND-Zen bound but within the projected sensitivity of nEXO and LEGEND-1000.
The same modular parameter τ that controls the neutrino sector also fixes the Yukawa
couplings governing the CP-violating decays of the heavy triplet fermions, thereby linking
the visible and dark sectors. The resulting CP asymmetries |ϵL,χ | ∼ 10−9 –10−6 generate comparable lepton and dark asymmetries through resonant decays of Σ1,2 at M1,2 ∼
107 GeV. Solutions of the coupled Boltzmann equations show that both asymmetries freeze
out with similar magnitudes, yielding the observed baryon asymmetry ηB ≃ 6 × 10−10 and
the correct dark relic density Ωχ h2 ≃ 0.12 without any parameter tuning.
The co-genesis mechanism exhibits a strong numerical correlation between ηB and
2
Ωχ h , reflecting the common modular origin of the CP asymmetries. The ratio Ωχ /ΩB
stabilizes near the cosmological value 3 ≲ Ωχ /ΩB ≲ 7, corresponding to a dark-matter
mass prediction mχ ≃ 0.1–2 GeV. The predicted GeV-scale dark-matter mass and its
extremely suppressed interactions with the visible sector ensure full consistency with existing laboratory, astrophysical, and cosmological constraints on asymmetric fermionic dark
matter.
The predictive power of the modular S4 symmetry lies in its ability to relate flavor,
CP violation, and cosmology through the single modulus τ . Once τ is fixed by low-energy
neutrino data, all other observables—baryon asymmetry, dark matter abundance, and 0νββ
predictions—follow without additional parameters. This work therefore demonstrates a
fully predictive realization of baryon–dark matter co-genesis embedded in a modular flavor
theory, linking the origin of flavor and matter–antimatter asymmetry through a common
geometric parameter. Future measurements of the leptonic CP phase, neutrinoless double
beta decay, and searches for light asymmetric dark matter will provide decisive tests of this
unified modular framework.

Appendix A: Essentials of Modular Symmetry and S4 Yukawa Multiplets
Modular symmetry provides a geometric approach to flavor symmetries in which Yukawa
couplings are expressed as modular forms—holomorphic functions of a single complex parameter τ in the upper half-plane (Im τ > 0). The modulus transforms under the modular
group SL(2, Z) as
aτ + b
τ −→
,
a, b, c, d ∈ Z, ad − bc = 1.
(A.1)
cτ + d
The two generators,
1
S : τ ↦→ − ,
T : τ ↦→ τ + 1,
(A.2)
τ
satisfy S 2 = (ST )3 = I and define the modular group relations. Finite subgroups ΓN =
Γ(1)/Γ(N ) correspond to well-known discrete flavor symmetries:
Γ2 ≃ S3 ,

Γ3 ≃ A4 ,

Γ4 ≃ S4 ,

Γ5 ≃ A5 .

In this work we employ Γ4 ≃ S4 , the smallest modular group that yields realistic lepton
mixing while retaining a nontrivial structure of modular forms.

– 21 –

## PDF page 23

A modular form of weight k and level N transforms as
k

Yi (τ ) −→ (cτ + d) ρij (γ) Yj (τ ),

( )
a b
γ=
∈ ΓN ,
c d

(A.3)

where ρ(γ) is a unitary representation of the finite modular group. The number of independent modular forms of weight 2k increases with N , as summarized in Table 5.
Table 5. Number of linearly independent modular forms of weight 2k for low modular levels N .

Level N
2
3
4
5

Associated group
S3
A4
S4
A5

# of forms (weight 2k)
k+1
2k + 1
4k + 1
10k + 1

—
A.1 Structure of the S4 Group
The finite group S4 contains five irreducible representations: 1, 1′ , 2, 3, and 3′ . Its
generators satisfy
S 2 = T 4 = (ST )3 = I.
(A.4)
The relevant Clebsch–Gordan (CG) products are
1′ ⊗1′ = 1,

2⊗2 = 1 ⊕ 1′ ⊕ 2,

2⊗3 = 3 ⊕ 3′ ,

3⊗3′ = 1′ ⊕ 2 ⊕ 3 ⊕ 3′ .

3⊗3 = 1 ⊕ 2 ⊕ 3 ⊕ 3′ ,
(A.5)

Explicit CG coefficients and representation matrices are listed in Refs. [21, 32] and are used
to build modular-invariant Yukawa interactions.
A.2 Modular Forms under S4
(2)

At level N = 4, the lowest-weight modular forms furnish a doublet Y2 = (Y1 , Y2 )T and a
(2)
triplet-prime Y3′ = (Y3 , Y4 , Y5 )T . With q ≡ e2πiτ , their schematic q-expansions are
√
Y1 ≃ 1 + 3q + 3q 2 + O(q 3 ),
Y2 ≃ 3 q 1/2 (1 + 4q + 6q 2 + · · · ),
√
Y3 ≃ 1 − 2q + 6q 2 + · · · ,
Y4 ≃ 2 q 1/4 (1 + 6q + 13q 2 + · · · ),
√
Y5 ≃ 4 2 q 3/4 (1 + 2q + 3q 2 + · · · ).
(A.6)
Higher-weight modular multiplets are constructed by modular-covariant products of these
basic forms. The independent weight-four combinations used in our model are
(4)

Y1

(4)

= Y12 + Y22 ,

√
√
= (−2Y2 Y3 , 3Y1 Y5 + Y2 Y4 , 3Y1 Y4 + Y2 Y5 )T ,
√
√
(4)
Y3′ = (2Y1 Y3 , 3Y2 Y5 − Y1 Y4 , 3Y2 Y4 − Y1 Y5 )T .

Y2

= (Y22 − Y12 , 2Y1 Y2 )T ,

(4)

Y3

– 22 –

(A.7)

## PDF page 24

The superscript “(4)” denotes the total modular weight. These multiplets generate all
Yukawa couplings appearing in the charged-lepton, neutrino, and dark sectors, ensuring
modular-invariant interactions consistent with S4 representation theory. In practice, only
the relative magnitudes and phases of the modular forms—fixed by the chosen value of
τ —enter physical observables. The group-theoretical structures, generator matrices, and
modular-form expansions presented here follow the conventions established in [44].

Appendix B: Standard Parameterization of Neutrino Observables
The lepton mixing matrix UPMNS is obtained via
UPMNS = Uℓ† Uν ,

(B.8)

where Uℓ and Uν diagonalize the charged-lepton and neutrino mass matrices:
Uℓ† Mℓ Mℓ† Uℓ = diag(m2e , m2µ , m2τ ),

Uν† Mν Uν∗ = diag(m1 , m2 , m3 ).

In the PDG convention,




1 0
0
c13 0 s13 e−iδ
c12 s12 0




UPMNS = 0 c23 s23  0
1
0 −s12 c12 0 Pν ,
0 −s23 c23
−s13 eiδ 0 c13
0
0 1

(B.9)

(B.10)

where cij ≡ cos θij , sij ≡ sin θij , and Pν = diag(1, eiα21 /2 , eiα31 /2 ).
Mixing observables follow as
sin2 θ13 = |Ue3 |2 ,

sin2 θ12 =

|Ue2 |2
,
1 − |Ue3 |2

and the CP-violating quantities are
[
]
∗
∗
δCP = − arg Ue1 Ue3
Uµ3 Uµ1
,

sin2 θ23 =

|Uµ3 |2
,
1 − |Ue3 |2

[
]
∗ ∗
JCP = Im Ue1 Uµ2 Ue2
Uµ1 .

The Majorana phases can be expressed as
(
)
Ue2
α21 = 2 arg
,
Ue1

(

Ue3
α31 = 2 arg
Ue1

(B.11)

(B.12)

)
+ 2δCP .

(B.13)

The mass-squared splittings and total neutrino mass are
∆m221 = m22 − m21 ,

∆m231 = m23 − m21 ,

Σmν = m1 + m2 + m3 .

(B.14)

Appendix C: Boltzmann Framework and Scattering Integrals
For completeness, we summarize the Boltzmann equation used in the two–sector analysis.
The comoving asymmetries Y∆a = Ya − Yā for a = L, χ evolve according to [8]
)
ΓΣ1 zK1 (z) (
dY∆a
eq
=−
YΣ1 − YΣ1 ϵa − 2 Br2a IW (z) Y∆a
dz
H1 K2 (z)
[
]
− Bra Brb IT+ (z) (Y∆a + Y∆b ) + IT− (z) (Y∆a − Y∆b ) ,
(C.15)

– 23 –

## PDF page 25

where b ̸= a, z = M1 /T , and H1 = H(T = M1 ). The first term describes the CP–violating
source from Σ1 decays, while the remaining terms account for washout and inter–sector
transfer effects.
The thermal integrals entering Eq. (C.15) are defined as
Γ̂
Ii (z) =
π

∫ ∞

dt t2 K1 (t) fi (t2 /z 2 ),

(C.16)

0

where Γ̂ = ΓN1 /MN1 , and
fW (s) =

fT+ (s) =
fT− (s) =

s/2

+

s − log(s + 1)
2(s − 1) (s + 1) log(s + 1) − s
−
s
s
(s − 1)2 + Γ̂2

(s − 1)2 + Γ̂2
s/2
log(s + 1)
+
+
,
s+1
s+2
s/2
(s − 1)2 + Γ̂2
s2 /2
(s − 1)2 + Γ̂2

(C.17)

+

s
s − log(s + 1)
+
,
s+1
s

(C.18)

+

(s + 1) log(s + 1) − s (s + 2) log(s + 1) − 2s
+
.
s+1
s

(C.19)

Here IW corresponds to 2 ↔ 2 washout within a sector, and IT± encode transfer scatterings between sectors.
As z = M1 /T increases, the pole (on-shell) contributions to the integrals are exponentially suppressed, and inverse decays become subdominant. In this regime, the Boltzmann
evolution is controlled by off-shell 2 ↔ 2 scattering processes, which admit simple analytic
approximations. For z ≫ 1, the integrals reduce to the asymptotic forms
ID (z) ≃

3W H1
,
z 2 ΓN1

IT + (z) ≃

W H1
,
z 2 ΓN1

IT − (z) ≃

14W H1
,
z 4 ΓN1

(C.20)

where W denotes the reduced scattering rate.

Appendix D: Behavior of the CP Asymmetry Ratio as a Function of yDM
In order to clarify the origin of the dark-sector dominance observed at small values of yDM ,
we present in Fig. 12 the ratio |ϵχ /ϵL | as a function of yDM for a representative benchmark
point in the modulus,
τ = 1.64 + i 2.57.
For yDM ≲ 10−3 , the ratio exhibits a mild enhancement, arising from the different
interference structures entering the visible and dark CP asymmetries. As yDM increases,
the ratio smoothly approaches unity, indicating comparable visible and dark contributions.
This behavior confirms that the enhancement at small yDM is a controlled quantitative
effect rather than a breakdown of the perturbative expansion.

– 24 –

## PDF page 26

102

| / L|

101
100
10 1
10 2

10 4

10 3

yDM

10 2

10 1

Figure 12. Ratio of CP asymmetries |ϵχ /ϵL | as a function of the dark Yukawa coupling yDM for
a fixed representative value of the modulus τ = 1.64 + i 2.57. The horizontal dashed line indicates
equal visible and dark CP asymmetries.

References
[1] Y. Fukuda et al. [Super-Kamiokande Collaboration], “Evidence for Oscillation of
Atmospheric Neutrinos,” Phys. Rev. Lett. 81 (1998), 1562–1567,
doi:10.1103/PhysRevLett.81.1562, arXiv:hep-ex/9807003.
[2] Q. R. Ahmad et al. (SNO Collaboration), “Measurement of the rate of νe + d → p + p + e−
and the total active solar neutrino flux,” Phys. Rev. Lett. 87 (2001) 071301,
10.1103/PhysRevLett.87.071301, arXiv:nucl-ex/0106015.
[3] S. Abe et al. [KamLAND Collaboration], “Precision Measurement of Neutrino Oscillation
Parameters with KamLAND,” Phys. Rev. Lett. 100 (2008), 221803,
doi:10.1103/PhysRevLett.100.221803, arXiv:0801.4589 [hep-ex]
[4] N. Aghanim et al. (Planck Collaboration), “Planck 2018 results. VI. Cosmological
parameters,” Astron. Astrophys. 641 (2020) A6, 10.1051/0004-6361/201833910,
arXiv:1807.06209.
[5] V. Abdurashitov et al. (DESI Collaboration), “DESI 2024 VI: Cosmological Constraints
from the Measurements of Baryon Acoustic Oscillations,” arXiv:2404.03002.
[6] D. E. Kaplan, M. A. Luty and K. M. Zurek, Asymmetric dark matter, Phys. Rev. D 79
(2009) 115016, doi:10.1103/PhysRevD.79.115016, arXiv:0901.4117 [hep-ph].
[7] K. Petraki and R. R. Volkas, Review of asymmetric dark matter, Int. J. Mod. Phys. A 28
(2013) 1330028, doi:10.1142/S0217751X13300286, arXiv:1305.4939 [hep-ph].
[8] A. Falkowski, J. T. Ruderman and T. Volansky, Asymmetric Dark Matter from Leptogenesis,
JHEP 05 (2011) 106, doi:10.1007/JHEP05(2011)106, arXiv:1101.4936 [hep-ph].
[9] B. Dutta and J. Kumar, Asymmetric dark matter from hidden sector baryogenesis, Phys.
Lett. B 699 (2011) 364–367, doi:10.1016/j.physletb.2011.04.036, arXiv:1102.4895 [hep-ph].
[10] U. Patel, L. Malhotra, S. Patra and U. A. Yajnik, Cogenesis of visible and dark sector
asymmetry in a minimal seesaw framework, (2022), arXiv:2211.04722 [hep-ph].
[11] A. Biswas, S. Choubey, L. Covi and S. Khan, Common origin of baryon asymmetry, dark

– 25 –

## PDF page 27

matter and neutrino mass, JHEP 05 (2019) 193, doi:10.1007/JHEP05(2019)193,
arXiv:1812.06122 [hep-ph].
[12] S. Davidson, E. Nardi and Y. Nir, “Leptogenesis,” Phys. Rept. 466 (2008) 1–81,
10.1016/j.physrep.2008.06.002, arXiv:0802.2962.
[13] W. Buchmüller, P. Di Bari and M. Plümacher, Leptogenesis for pedestrians, Annals Phys.
315 (2005) 305–351, doi:10.1016/j.aop.2004.02.003, arXiv:hep-ph/0401240.
[14] M. Fukugita and T. Yanagida, Baryogenesis Without Grand Unification, Phys. Lett. B 174
(1986) 45–47, doi:10.1016/0370-2693(86)91126-3.
[15] A. Pilaftsis and T. E. J. Underwood, “Resonant leptogenesis,” Nucl. Phys. B 692 (2004)
303–348, 10.1016/j.nuclphysb.2004.05.021, arXiv:hep-ph/0309342.
[16] P. S. B. Dev, P. Millington, A. Pilaftsis and D. Teresi, Resonant Enhancement in
Leptogenesis, Int. J. Mod. Phys. A 33 (2018) 1842003, doi:10.1142/S0217751X18420034.
[17] J. C. Criado and F. Feruglio, Modular invariance faces precision neutrino data, SciPost
Phys. 5 (2018) 042, doi:10.21468/SciPostPhys.5.5.042, arXiv:1807.01125 [hep-ph].
[18] T. Kobayashi and M. Tanimoto, Modular flavor symmetric models, (2023), arXiv:2307.03384
[hep-ph].
[19] T. Kobayashi et al., A4 lepton flavor model and modulus stabilization from S4 modular
symmetry, Phys. Rev. D, vol. 100, no. 11, p. 115045, 2019, arXiv:1909.05139. Erratum:
Phys. Rev. D, vol. 101, p. 039904, 2020.
[20] J. T. Penedo and S. T. Petcov, Lepton Masses and Mixing from Modular S4 Symmetry,
Nucl. Phys. B, vol. 939, pp. 292–307, 2019, arXiv:1806.11040.
[21] X. Wang and S. Zhou, The minimal seesaw model with a modular S4 symmetry, JHEP,
vol. 05, p. 017, 2020, arXiv:1910.09473.
[22] R. Foot, H. Lew, X. He and G. C. Joshi, Seesaw neutrino masses induced by a triplet of
leptons, Z. Phys. C 44 (1989) 441, doi:10.1007/BF01548594.
[23] E. Ma, Pathways to naturally small neutrino masses, Phys. Rev. Lett. 81 (1998) 1171–1174,
doi:10.1103/PhysRevLett.81.1171, arXiv:hep-ph/9805219.
[24] L. Covi, E. Roulet and F. Vissani, “CP violating decays in leptogenesis: The dominant
contribution from self-energy diagrams,” Phys. Lett. B 384 (1996) 169–174,
10.1016/0370-2693(96)00814-2, arXiv:hep-ph/9605319.
[25] A. Falkowski, D. M. Pierce and J. Thaler, “Asymmetric Dark Matter from Hidden Sector
Baryogenesis,” JHEP 1110 (2011) 028, 10.1007/JHEP10(2011)028, arXiv:1106.3057.
[26] R. L. Workman et al. (Particle Data Group), “Review of Particle Physics,” PTEP 2024
(2024) 083C01, 10.1093/ptep/ptad095.
[27] I. Esteban, M. C. Gonzalez-Garcia, M. Maltoni, I. Martinez-Soler, J. P. Pinheiro and
T. Schwetz, NuFit-6.0: updated global analysis of three-flavor neutrino oscillations, JHEP 12
(2024) 216, doi:10.1007/JHEP12(2024)216
[28] Abhishek and V. Suryanarayana Mummidi, Low scale leptogenesis and TM1 mixing in
neutrinophilic two Higgs doublet model (ν2HDM) with S4 flavor symmetry, Phys. Lett. B
870 (2025) 139919, doi:10.1016/j.physletb.2025.139919, arXiv:2504.04413 [hep-ph].
[29] S. Abe et al. [KamLAND-Zen], Search for Majorana Neutrinos with the Complete
KamLAND-Zen Dataset, (2024), arXiv:2406.11438 [hep-ex].

– 26 –

## PDF page 28

[30] LEGEND Collaboration, N. Abgrall, I. Abt, et al. LEGEND-1000 Preconceptual Design
Report. 2021. arXiv:2107.11462 [physics.ins-det].
[31] G. Adhikari, S. Al Kharusi, E. Angelico, et al. nEXO: neutrinoless double beta decay search
beyond 1028 year half-life sensitivity. Journal of Physics G: Nuclear and Particle Physics,
49(1):015104, 2021. ISSN 1361-6471. DOI: 10.1088/1361-6471/ac3631
[32] P. P. Novichkov, J. T. Penedo, S. T. Petcov and A. V. Titov, Modular S 4 models of lepton
masses and mixing, JHEP 04 (2019) 005, doi:10.1007/JHEP04(2019)005, arXiv:1811.04933
[hep-ph].
[33] C. S. Fong, M. C. Gonzalez-Garcia, E. Nardi and J. Racker, Supersymmetric leptogenesis,
JCAP 12 (2010) 013, doi:10.1088/1475-7516/2010/12/013, arXiv:1009.0003 [hep-ph].
[34] M. Flanz, E. A. Paschos and U. Sarkar, “Baryogenesis from a lepton asymmetric decay,”
Phys. Lett. B 382 (1996) 447–452, 10.1016/0370-2693(96)00698-1, arXiv:hep-ph/9607310.
[35] W. Buchmuller and M. Plumacher, “Status of thermal leptogenesis,” Phys. Lett. B 530
(2002) 15–26, 10.1016/S0370-2693(02)01329-5, arXiv:hep-ph/0207189.
[36] T. Garbrecht, “Leptogenesis from first principles in the resonant regime,” Phys. Rev. D 90
(2014) 025033, 10.1103/PhysRevD.90.025033, arXiv:1404.3358 [hep-ph].
[37] A. Abada, S. Davidson, A. Ibarra, F.-X. Josse-Michaux, M. Losada and A. Riotto, “Flavour
matters in leptogenesis,” JHEP 09 (2006) 010, 10.1088/1126-6708/2006/09/010,
arXiv:hep-ph/0605281.
[38] E. Nardi, Y. Nir, E. Roulet and J. Racker, “The importance of flavor in leptogenesis,” JHEP
01 (2006) 164, 10.1088/1126-6708/2006/01/164, arXiv:hep-ph/0601084.
[39] M. Endo and T. Orikasa, “Leptogenesis in modular symmetry,” JHEP 05 (2019) 115,
10.1007/JHEP05(2019)115, arXiv:1812.10709 [hep-ph].
[40] K. M. Zurek, Asymmetric Dark Matter: Theories, Signatures, and Constraints, Phys. Rept.
537 (2014) 91–121, doi:10.1016/j.physrep.2013.12.001, arXiv:1308.0338.
[41] F. Feruglio, Fermion masses, critical behavior and universality, JHEP 03 (2023) 236,
doi:10.1007/JHEP03(2023)236, arXiv:2212.09762 [hep-ph].
[42] S. Mahapatra, P. K. Paul, N. Sahu and P. Shukla, Asymmetric long-lived dark matter and
leptogenesis from the type-III seesaw framework, Phys. Rev. D 111 (2025) 015043,
doi:10.1103/PhysRevD.111.015043, arXiv:2405.00939 [hep-ph].
[43] G. J. Ding, S. F. King, X. G. Liu, and J. N. Lu. Modular S4 and A4 symmetries and their
fixed points: new predictive examples of lepton mixing. J. High Energ. Phys., 2019(12):030,
2019.
[44] X. Zhang and S. Zhou, Inverse seesaw model with a modular S4 symmetry: lepton flavor
mixing and warm dark matter, arXiv:2106.03433, 2021.

– 27 –
