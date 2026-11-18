Source: https://arxiv.org/abs/2110.01865v1
PDF sha256: 316e317c0b2a3cd5ebc09bb930b8b4b61689dde0a7550164b0fb3a4b99960820
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine (failed: characters)

# Transcription of arxiv_2110.01865_linarite_frustrated_spin_chain_transport.pdf

Transcription of `arxiv_2110.01865_linarite_frustrated_spin_chain_transport.pdf` in this directory, 11 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-11 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Thermal transport of the frustrated spin-chain mineral linarite:
Magnetic heat transport and strong spin-phonon scattering
Matthias Gillig,1, 2, ∗ Xiaochen Hong,1, 3 Piyush Sakrikar,4 Gaël Bastien,1 A.U.B. Wolter,1
Leonie Heinze,5 Satoshi Nishimoto,1, 6 Bernd Büchner,1, 2, 7 and Christian Hess1, 3, 7

arXiv:2110.01865v1 [cond-mat.str-el] 5 Oct 2021

1

Leibniz Institute for Solid State and Materials Research, 01069 Dresden, Germany
2
Institute for Solid State Physics, TU Dresden, 01062 Dresden, Germany
3
Fakultät für Mathematik und Naturwissenschaften,
Bergische Universität Wuppertal, 42097 Wupptertal, Germany
4
Indian Institute of Science Education and Research (IISER) Mohali,
Knowledge City, Sector 81, Mohali 140306, India
5
Institut für Physik der Kondensierten Materie, TU Braunschweig, 38106 Braunschweig, Germany
6
Department of Physics, Technical University Dresden, 01069 Dresden, Germany
7
Center for Transport and Devices, TU Dresden, 01062 Dresden, Germany
(Dated: October 6, 2021)
The mineral linarite (PbCuSO4 (OH)2 ) forms a monoclinic structure where a sequence of Cu(OH)2
units forms a spin- 21 chain. Competing ferromagnetic nearest-neighbor (J1 ) and antiferromagnetic
next-nearest-neighbor interactions (J2 ) in this quasi-one-dimensional spin structure imply magnetic
frustration and lead to magnetic ordering below TN = 2.8 K in a mutliferroic elliptical spin-spiral
ground state. Upon the application of a magnetic field along the spin-chain direction, distinct
magnetically ordered phases can be induced. We studied the thermal conductivity κ in this material
across the magnetic phase diagram as well as in the paramagnetic regime in the temperature ranges
0.07–1 K and 9–300 K. We found that in linarite the heat is carried mainly by phonons but shows a
peculiar non-monotonic behavior in field. In particular, κ is highly suppressed at the magnetic phase
boundaries, indicative of strong scattering of the phonons off critical magnetic fluctuations. Even
at temperatures far above the magnetically ordered phases, the phononic thermal conductivity
is reduced due to scattering off magnetic fluctuations. The mean free path due to spin-phonon
scattering (lspin-phonon ) was determined as function of temperature. A power law behavior was
observed mainly above 500 mK indicating the thermal activation of spin fluctuations. In the critical
regime close to the saturation field, lspin-phonon shows a 1/T dependence. Furthermore, a magnon
thermal transport channel was verified in the helical magnetic phase. We estimate a magnon mean
free path which corresponds to about 1000 lattice spacings.
I.

INTRODUCTION

Low-dimensional spin systems are of interest because
of the expected occurrence of strong quantum effects.
Particularly, spin chains attract attention due to the
possibility to host novel ground states, e.g., TomonagaLuttinger liquids. Heat transport experiments in such
systems can elucidate the characteristics by probing the
emerging spin excitations. For isotropic spin- 21 Heisenberg chains a finite thermal Drude weight has been predicted due to the conservation of the heat current [1–
3] which renders the magnetic heat transport ballistic.
Indeed, in material realizations of the isotropic spin1
2 Heisenberg chain, such as the cuprate compounds
SrCuO2 and Sr2 CuO3 , experimental evidence for ballistic spinon heat transport has been inferred from highly
anisotropic heat conductivity tensors [4–7]. Recently,
a non-zero Drude weight was predicted also in a frustrated spin chain, where the interaction among nearest
and next-nearest neighbors are competing [8]. Experimentally, except a pioneering study in LiCu2 O2 , where
a magnon heat channel below the ordering temperature

∗ m.gillig@ifw-dresden.de

was observed [9], heat transport data of frustrated spin- 12
Heisenberg chains is scarce.
In this paper we present heat transport experiments on the frustrated spin-chain material linarite
(PbCuSO4 (OH)2 ). It is a well studied natural mineral
which crystallizes in a monoclinic lattice (space group:
P 21 /m) [10, 11] where a sequence of Cu(OH)2 units
forms a quasi-one-dimensional structure of Cu2+ ions
along the b-direction. Due to the spacial separation of
these strips along a and c it can be described as a quasi1D spin chain with S = 12 . The magnetic interaction
between the spins has been modeled based on different
experimental results (neutron scattering [12], magnetic
susceptibility [13, 14]) which render competing exchange
interactions between nearest neighbors (J1 ≈ −78 K) and
next-nearest neighbors (J2 ≈ 28 K) [12]. Additional finite interchain couplings lead to long range magnetic order below TN = 2.8 K where the spins are arranged in
an helical incommensurate state with the propagation
vector q⃗ = (0; 0.186; 0.5) [15]. This magnetic ordering
implies spin-driven ferroelectricity unveiling strong magnetoelastic coupling in linarite [16]. Given the estimated
Curie-Weiss temperature ΘCW = 27 K [13], the frustration ratio f = ΘTCW
≈ 10 points out the high degree of
N
frustration in the system. The magnetic phase diagram
strongly depends on the direction of the magnetic field

## PDF page 2

2

H b
||

µ0H

10

sat

= 9.64 T

9

V

8

µ0H (T)

7
6

IV

5
4

III

II

3
2

I

1
0
0.0

0.5

1.0

1.5

2.0

2.5

3.0

3.5

T (K)
FIG. 1. Magnetic phase diagram of PbCuSO4 (OH)2 for H||b
adapted from [21]. The Roman numerals label the magnetic
phases: helical incommensurate phase (I), hysteretic commensurate region (II), coexistence phase (III), collinear Néel antiferromagnetic order (IV), and spin-density wave phase (V).

µ0H = 14 T

20

sample 1

j bH b
||

||

-1

-1

15

0 T
10

5

0
0

50

100

150

200

250

300

T (K)
FIG. 2. Thermal conductivity for T > 9 K with magnetic field
applied along the spin-chain direction (H||b)

sured with in-situ calibrated RuO2 sensors using a dilution refrigerator. Magnetic fields of up to 16 T were
applied along the b-direction in all measurements. The
thermal conductivity measurements as a function of temperature with fixed magnetic field were performed in a
steady-state mode, where the given temperature is defined as the average of the temperature at the hot and
cold thermometer. For field-dependent thermal conductivity measurements the temperature of the heat bath
and the heating power were fixed and the magnetic field
was ramped slowly with a maximum rate of 0.06 T min−1
to avoid heating effects. One should note that in this
measurement mode, due to strong changes in κ, the temperature of the sample slightly varies while sweeping the
field, while for our representation of the results, the average temperature of each field ramp is given. We report
experimental results from measurements on two different specimens of naturally grown crystals (both from the
Grand Reef Mine, Graham County, Arizona, USA). Sample 1 was used to investigate the heat transport along
b. The shape of sample 2 allowed to inject a heat current perpendicular to b. The heat current direction is
−20◦ ± 5◦ off the a-axis and was chosen to maximize the
length of the crystal along the heat current.

III.
II.

,

10 T

k (W K m )

[17, 18] which underlines the anisotropic character of the
magnetic system. Here, we focus on the particular case
H||b, which is the best studied case up to date.
Upon the application of a magnetic field along b, several transitions into distinct magnetic phases are induced
[14, 15, 19, 20]. They are depicted in the magnetic phase
diagram in figure 1. The helical magnetic phase, which
at µ0 H = 0 T sets in at TN ≈ 2.8 K, is suppressed by
a magnetic field and below 2 K and above 2.5 T it gives
way to a collinear Néel antiferromagnetic order (IV) with
a commensurate propagation vector q⃗ = (0; 0; 0.5). At
very low temperature (T < 700 mK), a hysteretic region
II separates phase I from IV with a commensurate vector
q⃗ = (0; 0; 0.5) whereas above 1 K the phases I and IV are
connected via a coexistence phase III where the commensurate and an incommensurate, circular spin arrangement coexist [20]. The mentioned phases are enclosed by
a phase which was refined as an incommensurate longitudinal spin-density-wave state [20] with q⃗ = (0; ky ; 0.5)
which depends on the magnetic field and also on temperature [21]. Beyond the saturation field of 9.64 T, determined by a nuclear magnetic resonance (NMR) study
[21], the system is field polarized.

RESULTS

EXPERIMENTAL APPROACH
A.

The thermal conductivity κ has been measured between 9 K and 300 K in a home-built setup with a standard steady-state method where heat was applied on one
side of the sample using a chip resistor whereas the other
side of the crystal was mounted on a cold bath. The applied thermal gradient along the sample was measured
with a Au-Chromel thermocouple. For measurements
between 0.07 K and 1 K the thermal gradient was mea-

Thermal conductivity T ≥ 9 K (paramagnetic
state)

The results for the thermal conductivity measurements
in the temperature range from 9–300 K are shown in figure 2. The zero-field curve resembles that of a phonon
heat conductor with a maximum of 18.7 W K−1 m−1 at
18 K and a decrease towards higher temperatures. Upon
applying a magnetic field parallel to the spin-chain direc-

## PDF page 3

3
tion (H||b), the peak in κ is enhanced below 50 K. At
18 K the increase in field is about 3.4 % for 10 T and 6.8 %
for 14 T. Field-enhanced thermal conductivity is not expected for a pure phonon system and in a paramagnetic
state it can only be explained within a scenario of magnetic scattering of the phonons at 0 T which is gradually
reduced in magnetic field, thus leading to the increase
in κ. Electron spin resonance experiments [13] show a
broadening of resonance lines around 50 K which signals
the occurrence of magnetic fluctuations far above the ordering temperature. Since the onset of the fluctuations
occurs at the same temperature as the field-enhancement
of κ, they can be hold responsible for the phonon scattering. In this scenario, the decline of magnetic scattering
in the κ-data is consistent with a field-induced reduction
of the spin fluctuations.

B.

Thermal conductivity T ≤ 1 K

The thermal conductivity of sample 1 as function of
temperature for T < 1 K is shown in figure 3 with
the heat current and the magnetic field applied along
the spin-chain axis. The zero-field thermal conductivity increases monotonically from 75 mK to 1 K. κ exhibits a temperature dependence that scales with ∝ T 2.50
(T < 0.4 K) and ∝ T 2.04 (0.4 K < T < 1 K) (see fig.
10) which deviates from the standard phonon expression
κ ∝ cV ∝ T 3 . In this temperature and field regime
the spin system orders in an elliptical spiral, so it is expectable that both phonons and magnons contribute to
the thermal conductivity directly and at the same time
act as a potential scatterer of the respective other quasiparticle. Since neither the temperature dependence nor
the absolute value of either contribution is known, it is
not straight forward to disentangle the two contributions.
To this end the application of a magnetic field can help
to resolve this since it should not affect a purely phononic
heat conduction channel. Figures 3 (a)-(c) depict how
the temperature dependence of the thermal conductivity
evolves under magnetic field in the regimes of 0–4 T, 4–
9 T and 9–16 T, respectively. In the lowest range (fig. 3
(a)) and below 0.6 K, κ is only weakly altered by a magnetic field. However, with increasing temperature the
field effect intensifies. Between 0.6–1 K it is clearly noticeable that H suppresses κ with the strongest impact
at 2.5 T where it is diminished by 29 % at 1 K. With
further increase of H, κ recovers about 50 % of the suppressed fraction at 4 T. Above 6 T (fig. 3 (b)) another
decrease sets in, diminishing κ first at higher temperature, and for µ0 H > 7.5 T the region of suppressed κ
is subsequently shifted towards lower temperature with
increasing magnetic field. The transition between these
two regions is clearly visible and traces the phase boundary in the H-T phase diagram between phase IV and V.
Below 200 mK the field induced effects are reduced. The
graph in panel 3 (c) shows the results for µ0 H > 9 T
where the trend in the field dependence is inverted and

κ recovers quickly until it becomes field independent at
12 T and higher. Over the whole field range, a strong
change in the temperature dependence of κ is observed,
the most pronounced changes occur when the κ(T ) curve
crosses a phase boundary, e.g., at 8.1 T exhibiting a steep
slope below 0.5 K whereas for T > 0.7 K the increase with
temperature is smaller.
At 16 T, far above the saturation field, it is expected
that all magnetic excitations are gapped out and the
low-temperature thermal conductivity in this regime is
independent of the magnetic system and thus purely
phononic. Comparing this to the smaller κ in field below
16 T, it is obvious that the thermal transport is dominated by phonons and the respective reduction must
be assigned to spin-phonon scattering. Measurements of
the thermal expansion have also shown previously that
a strong coupling of the lattice to the magnetic system
is present in linarite [14]. Magnetic heat transport can,
however, not be ruled out, but it would require a detailed knowledge of the magnetic excitations to disentangle their intricate interplay with the phonon system.
However, at 0 T, the thermal conductivity is enhanced
compared to the phononic background. This can only be
attributed to an additional magnetic contribution κmag
to the thermal conductivity.

Anisotropy of κ - evidence for magnon heat transport in the
helical phase

In order to estimate κmag , in figure 3 (d) the difference between the zero-field and 16 T curve is plotted as
function of temperature (κmag = κ(0 T) − κ(16 T)). κmag
adds 10 % of the phononic background to the total thermal conductivity and it follows a quadratic temperature
dependence up to 0.8 K where a downturn sets in. Due to
the strong magneto-elastic coupling across the differently
ordered phases, the intense phonon scattering off magnetic excitations must also be considered at 0 T, diminishing κph (0 T) compared to the phononic background in
the polarized state. Therefore, at this stage of the analysis the calculated κmag should be considered a lower
bound for the magnetic contribution.
In order to clarify to what extent magnetic phonon
scattering must be considered to extract the correct value
of κmag , κ has been measured on an additional sample 2
(see fig. 4) along a direction perpendicular to the spinchain axis. Due to the anisotropy of the magnetic lattice, no significant magnetic heat transport is expected,
whereas the phonon contribution and its scattering behavior is assumed to be isotropic. Figure 4 (a) shows the
results for µ0 H ≤ 9 T. κ/T differs from sample 1 by a
fixed factor of about two, while the temperature dependence and the systematic change in magnetic field are the
same. The different absolute value can be explained by
differences in the geometric factor of the two samples that
were not perfectly defined due to the natural grown shape
of the crystals. On the other hand, the apparent identi-

## PDF page 4

4
(b)

(a)
sample 1

0.5 T

sample 1

j || b, H || b

3 T

j || b, H || b

1 T4 T

£µH£4T
0

4 T

1.5 T

m

-1

0 T

6 T
4 T

£µH£9T
0

7 T

2 T

7.5 T

k / T (W K

-2

2.5 T

7.7 T

8 T

7.9 T

8.1 T

8.5 T

8.2 T

9 T

8.3 T

T (K)

sample 1

-2

k

µ0H=0T

mag

10 T
9.5 T
9 T

T (K)

2

)

12 T
10.5 T

k / T (W K

~ T

-1

0

j || b, H || b

14 T

m

)
-1

£ µ H £ 16 T

m

9 T

16 T
15 T

j || b, H || b

-1

0 T

sample 1

T (K)

(d)

k

(c)

(W K

)

0 T

T (K)

FIG. 3. Temperature dependence of the low-temperature thermal conductivity of sample 1 with the heat current and magnetic
field oriented along the b-direction for the magnetic field ranges (a) 0-4 T, (b) 4-9 T and (c) 9-16 T. In (d) the open circles
depict the magnetic contribution to the thermal conductivity at zero field obtained from subtracting the phononic background
in the polarized phase at 16 T from the zero-field curve κ0T
mag = κ(0T) − κ(16T), the solid line is a guide to the eye.

cal field dependence confirms the validity of the assumption of isotropic phonon scattering. In this configuration
the thermal conductivity traces the features of the phase
diagram by exhibiting significant changes close to a magnetic phase transition. In panel (b), the thermal conductivity for µ0 H ≥ 9 T is depicted. At 9 T it is suppressed
most prominently before it recovers at a larger field and
becomes field independent at 13 T and above. Most importantly, the zero-field curve matches vastly with the
phononic background at 16 T which means that there is
no detectable additional contribution at zero field compared to the phononic background. Furthermore there
is also not a significant reduction of κ/T (0 T) due to
magnetic scattering, merely above 0.7 K a slight deviation sets in. Consequently, κmag determined in sample 1
indeed is the actual magnetic contribution of the spiral
spin system to heat transport up to 0.7 K. Above 0.7 K,

phonon scattering sets in also at 0 T. Since κ(0 T) is
reduced below the phononic background, the simple subtraction does not yield a meaningful κmag in this temperature range. This gives an explanation for the kinklike feature that appears in κmag at 0.9 K in figure 3 (d)
where an overestimation of the phonon contribution produces such an artifact. Also for the κ(T ) curves for fields
µ0 H > 0 T, where κ is below the phononic background,
it is not straightforward to disentangle possible magnon
contributions from phonons since both quasiparticles are
expected to scatter off each other which suppresses the
respective fraction of κ.

## PDF page 5

5
(a)

(b)

0.5
sample 2

k / T (W K

-2

m)

0.4

0 T

j

b, H || b

0 T

£µH£9T

sample 2

2.7 T
7 T

2 T

0

0.5

4 T

13 T

j

b, H || b

9 T

£ µ H £ 16 T

0.4

16 T
0 T

0

7.5 T
0.3

0.3

10 T

9 T
7.7 T
8 T

0.2

0.2

9 T

7.9 T

0.1

0.1

0.0
0.0

0.0
0.2

0.4

0.6

0.8

1.0

T (K)

0.0

0.2

0.4

0.6

0.8

1.0

T (K)

FIG. 4. Temperature dependence of the low-temperature thermal conductivity of sample 2 with the heat current perpendicular
and the magnetic field parallel to the b-direction for the magnetic field ranges (a) 0-9 T and (b) 9-16 T.

Field dependence of κ - evidence for strong spin-phonon
scattering

Figure 5 shows the thermal conductivity κ/T as function of magnetic field at various temperatures for sample
1 (j||b) in panel (a) and sample 2 (j ⊥ b) in panel (b).
It provides additional information about abrupt changes
in κ under magnetic field. As mentioned in section II,
κ’s field dependence leads to a relative variation of the
sample temperature which is however smaller than the
relative changes in κ itself. This effect is most significant
in phase V where the mean temperature of the sample
as compared to phase I is raised by 10 %. Despite this
variation of the sample temperature, the data for κ(H)
are well consistent with those for κ(T ) where the temperature variation is absent. This can be verified in fig. 5
(a), e.g., for the data at T ≈ 170 mK where the triangles
represent data from constant field measurements.
For the heat transport along the spin chain direction
(j||b) (fig. 5 (a)), the field dependence is similar for all
temperatures. Compared to the high-field limit, which
defines the maximum phononic background, κ is mostly
reduced at lower fields. Only in phase I, κ exceeds the
high-field limit due to the additional magnetic contribution. At lowest temperature, κ seems largely field independent. However at the phase transitions sharp features occur. From phase I to phase II there is a step-like
change which corresponds to switching off the magnetic
transport channel. At higher temperatures, this step is
accompanied by a dip implying enhanced phonon scattering at the critical field value. The proximity to ferroelectric order in phase I [16] might also affect the phonon
transport there. The phase line between II and IV is
not represented by a sharp feature in the thermal conductivity data. At 8.3 T another step down indicates the

onset of the spin density wave phase (V) at which the
315 mK curve is reduced by about 20 %. With increasing
temperature this abrupt change intensifies in the relative
height. Also at higher T , a slow decrease of κ sets already in at lower fields within phase IV. Beyond the step,
the strong dip becomes even deeper until a minimum is
reached which coincides with the upper phase boundary
of region V. For higher fields, the thermal conductivity recovers steadily to the high-field limit over a range of 0.5 T
at 170 mK to up to 3 T at 870 mK. The 500 mK curve was
measured for ramping the magnetic field up and down
without signatures for hysteretic behavior in any of the
features within experimental resolution. All the distinct
features and the explicit field dependence underline the
impact of the magnetic excitations on the phonon system.
Especially at the phase boundaries where an intensification of magnetic fluctuations is expected the phonons are
scattered most strongly. Compared to previous experimental findings [14, 15, 18, 19, 21], the features in κ(H)
identified as phase boundaries are slightly higher on the
axis of magnetic field (< 5 %), which might be due to
sample dependency or marginal misalignment of the baxis with magnetic field.
The graph in panel 5 (b) depicts the field dependence
of κ/T perpendicular to the spin-chain direction, measured on sample 2. The overall behavior agrees with the
result of sample 1. κ(H) being largely isotropic validates
the phononic predominance of the thermal conductivity.
The clear difference between the two orientations is the
absence of the contribution in phase I which exceeds the
phononic background and is attributed to magnetic heat
transport in the spin chain. Also the effect of a magnetic
field on this magnetic channel can be determined qualitatively from figure 5 (a). Above 500 mK, κmag decreases
approximately linearly with increasing field, whereas for
the two curves below 500 mK κmag seems to form a field-

## PDF page 6

6

j

(a)

I

II

|| b,

IV

H

|| b (sample 1)

V

PM

T ~ 870 mK

0.8

k / T (W K

-2

m

-1

)

1.0

T ~ 700 mK

0.6

T ~ 500 mK

0.4

T ~ 315 mK
0.2

T ~ 170 mK

0.0

j^

(b)

0.5

I

II

b,

H

|| b (sample 2)

V

IV

PM

0.4

T ~ 820 mK

m

-1

)

independent plateau across phase I.
Figure 6 depicts the relative field dependence in sample 1 where κ is normalized to the value at 15 T. This
highlights the temperature dependence of the features in
κ that occur while sweeping the field. The most pronounced changes occur in phase I and V. Below 3 T, the
field independence softens with increasing temperature,
leading to a decline of κ towards the phase boundary. An
also peculiar behavior occurs in phase V and in the vicinity of its phase boundaries. The sharp step that marks
the phase transition at 7.9 T and 870 mK becomes weaker
with lowering the temperature until there is only a small
dip left at 170 mK. The minimum that coincides with
the upper phase boundary also becomes less intense upon
cooling. However there is still a deep trench remaining at
lowest temperature. Across the whole temperature range
a substantial field dependence of κ is present between the
two phase boundaries.

A.

-2

DISCUSSION

k / T (W K

IV.

Phonon transport

The findings of the above presented experiments show
deviations of a simple Debye-like thermal conductor in
several aspects which are discussed in the following.
Across the magnetically ordered phases, κ exhibits a
strong magnetic field dependence where it is largely reduced below the undisturbed phonon contribution at the
high-field limit. Therefore, significant magneto-elastic
coupling between phonons and magnetic degrees of freedom must be present which constrains the phonon mean
free path. The effect is strongest between 7 and 10.5 T
which corresponds to phase V and its vicinity. For the
phases at lower field, magnetic scattering only becomes
relevant above 500 mK (see fig. 4 (a)).
We begin our discussion with the purely phononic part
of the thermal conductivity (e.g. at 16 T). It shows a deviation from the standard T 3 behavior given by the specific heat of the phonon system (see fig. 11). In the low
temperature limit of pure phonon systems, the phonon
wavelength becomes so large that boundary scattering is
the only relevant process to limit the mean free path.
It has been shown before that a smooth crystal surface
causes phonons to specularly reflect at the boundaries
leading to a behavior of κph ∝ T α where α = 2 − 3 (e.g.
in Al2 O3 [22] and in LiF [23]), as is also observed in our
data, implying a temperature dependent phonon mean
free path. In the following we will estimate the phonon
mean free path lph using the formula
κph =

1
⟨v⟩ cV l,
3

(1)

with ⟨v⟩ the mean phonon velocity averaged over all
branches, cV the specific heat of the phonon system normalized to the volume, and l the phonon mean free path.

0.3

T ~ 610 mK
0.2

T ~ 300 mK
T ~ 220 mK

0.1

T ~ 160 mK

0.0
0

2

4

6

8

10

12

14

16

µ0H (T)
FIG. 5. Thermal conductivity as function of magnetic field
where in (a) both the heat current and the magnetic field are
applied along b in sample 1. (b) shows the thermal conductivity κ/T of sample 2 as a function of magnetic field where the
heat current j is applied perpendicular to b and the magnetic
field parallel to b. The dashed lines correspond to the phase
boundaries at T ≈ 250 mK as referred to in [14]. The dotted
lines refer to the phononic background which is defined in the
fully polarized phase.

At low temperature, one can assume that only acoustic phonons contribute with a k-independent vs . In this
ΘD kB
approximation the velocity is given as vs = h̄(6π
2 N )1/3
where ΘD is the Debye temperature and N the number
of elementary cells per unit volume. The volumetric specific heat is given as the product of the density of the material ρ and the specific heat of the phonon system. The
phononic contribution to the specific heat and the Debye
temperature were determined from a fit of the measured
specific heat by a harmonic model in a previous publication [14]. The Debye temperature is estimated at 133 K.
At low temperature the volumetric specific heat is thus
ρ
ρ
Cph = M
βT 3 where M stands
estimated with cV = M
for the material’s molar mass and β = 1.508 mJ/molK4 .
Using the mentioned parameters the phonon mean free

## PDF page 7

7
1.2

I

II

1.1

IV

V

T ~ 315 mK

PM

T ~ 170 mK T ~ 500 mK

1.0

T ~ 700 mK

k(H) / k(15T)

0.9

T ~ 870 mK

0.8

0.7

0.6

0.5

0.4

0.3
0

2

4

6

8

10

12

14

µ0H (T)
FIG. 6. Relative field dependence of thermal conductivity in
sample 1 (j, H||b) where κ is normalized to the value at 15 T
in the polarized phase. The dashed lines refer to the phase
boundaries at 250 mK as referred to in [14].

path is given as
ltotal =

3κ
.
cV vs

(2)

The temperature dependence of ltotal was determined for
the data measured on sample 1 and is plotted in figure
7 (a) for different magnetic field values. ltotal at 16 T
represents the magnetically undisturbed phonon scattering behavior. At 1 K ltotal = 53 µm, upon cooling it increases to 246 µm at 75 mK which corresponds to 53 %
of the sample width. This renders the phonon system
close to the ballistic regime where the mean free path
is only limited by the sample’s edges. The double logarithmic representation shows that it does not follow a
clear power law over the entire temperature range. Such
a behavior has been reported previously like in the insulating YBa2 Cu4 O6 where the curvature of κ/T changes
as function of temperature [24].
In order to describe the magnetic scattering separately,
we consider an additional magnetic scattering mechanism
−1
−1
−1
in the total mean free path ltotal
= lphonon
+ lspin-phonon
,
according to Matthiessen’s rule. This spin-phonon mean
free path can be separated from ltotal considering that
the mean free path of the magnetically undisturbed
phonons lphonon is field independent and is equal to the
phonon mean free path in the polarized phase (lphonon =
ltotal (16 T)). The spin-phonon mean free path is then
given as
lspin-phonon = cV vs
3κ

1

.
−1
− lphonon
(16 T)

(3)

lspin-phonon as function of temperature is depicted in
figure 7 (b). It can be determined for the fields where
ltotal differs clearly from lphonon. The plot ranges up to

3000 µm, beyond this value the data scatters strongly due
to small differences between lphonon and ltotal of the respective field and therefore does not allow a reasonable
interpretation. Spin-phonon scattering becomes mostly
relevant in phase V and its vicinity. For 7 T and lower,
lspin-phonon is much larger than lphonon , thus the trivial
phonon scattering predominates with respect to the magnetic scattering. On the other hand, above 500 mK and
for all fields, spin-phonon scattering is present and increasing, indicating that the magnetic scattering is thermally activated. In certain regions of the temperature
range, all the curves obey a power law behavior which is
indicated by the solid and dashed black lines in figure 7
(b). The respective exponents of the power law are listed
in table I in the Appendix. Interestingly, at 10 T, close
to the critical point where the magnetic field begins to
polarize the spins, lspin-phonon follows a T −1 dependence
over a wide temperature range. It is tempting to interpret this as a fingerprint of the critical scattering close to
saturation. However, at present, there is no meaningful
interpretation of the power law coefficient. However, we
believe that the temperature dependence can be useful
to determine the spin-phonon scattering matrix element
in future works.
The importance of magnetic scattering in phase V with
respect to all the other phases is remarkable. Electron
spin resonance measurements show a continuous decrease
of the resonance frequency with field within phase V and
its collapse at the saturation field [25]. Such observations
hint at a fan state in phase V. In former NMR experiments on this phase, a broad spectrum was observed superimposed with an additional broad peak which follows
the NMR signal of the paramagnetic field and temperature range [20]. This implies that two different local environments are present in phase V, either in a microscopic
coexistence or in a phase separation. Previous neutron
diffraction measurements reported a reduction of the integrated intensity upon entering phase V [20, 21] which
agrees with both afore mentioned scenarios. Furthermore in inelastic neutron scattering (INS) experiments,
the spin wave dispersion in phase V appears to be less
intense [26] which can be ascribed to either strong spin
fluctuations resulting in a lower ordered magnetic moment or to only a partial detection of the magnetic state
due to phase separation. The scenario of phase separation would imply that in phase V there are domain walls
present in the crystal. The appearance of domain walls
causes additional scattering of the phonons and provides
an explanation for the strong suppression of the phononic
thermal conductivity compared to the other phases. The
temperature evolution of the suppression, as shown in
figure 6, follows a trend where the scattering becomes
less intense towards lowest temperatures. Considering
that the phonon wavelength increases with lowering the
temperature, one can expect that at lowest temperature
it becomes significantly larger than the magnetic domain
size reducing the efficiency of phonons being scattered
by domain walls. Thereby the thermal conductivity data

## PDF page 8

8
agrees with the scenario of magnetic phase separation.
Yet the observed transport properties in phase V do
not rule out strongly fluctuating spins and in this scope
the heavily reduced κ can be explained by intense phonon
scattering. We point out that magnetic fluctuations obviously remain important also at higher temperatures,
since they affect κ at least up to 50 K.
(a)
8.5 T
10.5 T
16 T

10 T

6 T
4 T

/ w

(µm)

100

total

l

total

3 T

l

0.1
7 T

9.5 T

9 T
8.1 T

(b)

6 T
3 T

1000

1

7 T
8.1 T

10 T

4 T

/ w

-1

100

l

10.5 T
0.1

9.5 T

9 T
10
0.1

1

T (K)
FIG. 7. (a) The phonon mean free path ltotal as function
of temperature in sample 1, (b) spin-phonon mean free path
lspin-phonon which describes the limit of phonon propagation
due to spin-phonon scattering. Dashed and solid black lines
are guides to the eye and illustrate the power law behavior.
The respective exponents are shown in table I. The left scales
are normalized to the width of the sample.

B.

with x = εk /kB T , the excitation’s dispersion function
εk , a k-independent magnon mean free path lmag and
the number of chains per unit area ns . For kB T ≪ |J| =
78 K · kB the integral does not depend on temperature
and converges to π 2 /3. With this the magnon mean free
path is given as

spin-phonon

T

l

spin-phonon

(µm)

~

8.5 T

linear fit of the low-energy dispersion yields a magnon veb
locity of vmag
= 872.5 m s−1 averaged over both branches
for positive and negative momenta. The obtained value
agrees well with the theoretical modeling of the INS reb
sults, yielding a value of vtheo
= 883.1 m s−1 . The measurement along c reveals an energy scale by a factor of
20 smaller with maxima at 1 meV, where the linear fit
c
= 435 m s−1 . Experimenyields a lower velocity of vmag
tal data for dispersions along the a-axis have not been
reported in the literature so far. However, interactions
can safely be assumed negligible given the large interchain distance along the a-axis of 9.682 
A. Due to these
anisotropic energy scales the assumption may be valid
that a quasi-one-dimensional spin wave excitation carries the heat along the chain whose thermal conductivity
is given in the kinetic model by
∫
2
ns lmag kB
T Jπ/2kB T x2 exp(x)
κmag =
dx (4)
πh̄
(exp(x) − 1)2
0

Magnon transport

A second aspect that distinguishes linarite from a trivial phonon conductor is the magnetic heat transport
channel that is present in phase I given by the anisotropic
enhancement of κ compared to the polarized phase. INS
measurements have shown that the dispersion at 0 T differs for the two axes b and c [12]. Along the chain direction, two minima at ±0.2π/a and a crossing of the
branches at 0π/a were observed. Linear spin wave theory
calculations yield a dispersion with maxima of 19 meV. A

lmag =

3h̄ κmag
.
2
2πns kB
T

(5)

The result is presented in figure 8 showing a linear
temperature dependence up to 0.7 K where it reaches
0.011 µm which corresponds to about 40 chain units. A
mean free path that vanishes for T → 0 K appears unphysical and challenges the assumptions made.
An alternative method to estimate the magnon mean
free path is to use the plain three-dimensional kinetic
model with
κ=

1
ρ
1
cV,mag vmag lmag = Cmag vmag lmag
3
3
M

(6)

b
which requires the afore mentioned magnon velocity vmag
and the magnon contribution to the volumetric specific
ρ
Cmag . Cmag has been reported by
heat cV,mag = M
Schäpers et al. [14] down to 0.5 K. Below 2 K, it can be
described with Cmag = γT 3 where γ = 151 mJ/molK4 .
The hereby calculated mean free path is shown in figure 9. It increases towards cooling with a mostly linear
slope and reaches 0.5 µm below 0.3 K which corresponds
to about 2000 chain units. This second method yields a
more plausible temperature dependence of the mean free
path and gives a more realistic description of the spin system’s heat transport. However, the estimation contains
uncertainties which are mainly the dimensionality of the
spin system contained in the prefactor of 31 in equation
6 and the approximation of the magnon velocity. These
factors may alter the absolute value of lmag but do not
affect the temperature dependence. Compared to the
spin-chain compound SrCuO2 (lmag ≈ 1.5 µm) [5], the

## PDF page 9

9

12

800

40
2500

600

l

l

1000

4
10

200
500

2

0
0.0

/ b/2
mag

mag

1500

400

l

/ b/2

20

mag

6

2000

(nm)

30

8

l

mag

(nm)

10

0.2

0.4

0.6

0.8

0
1.0

T (K)

FIG. 8. The magnon mean free path of the magnon excitations at µ0 H = 0 T estimated for a one dimensional system.
The right scale is normalized to the distance of magnetic ions.

mean free path is of the same order of magnitude. On
the other hand it is considerably larger than in CaCu2 O3
[27] (lmag = 22 
A). In both materials it has been shown
that the mean free path scales with the density of defects within the chains. Transferring these findings to our
measurements we can determine that in the here studied
crystals the average length of chain segments is about
1000 unit cells.
For the regions beyond phase I, magnetic contributions
to the thermal conductivity are either absent or too small
to significantly exceed the phonon background. According to expression 6, each magnon conductivity depends
on three parameters. It has been reported that Cmag
varies with the magnetic field but is not heavily suppressed [14]. This implies that in these phases either
the magnon velocity is diminished due to flattened dispersions or the mean free path is limited due to more
intense magnon scattering compared to the helical phase
or both simultaneously.
Finally, in contrast to the nonfrustrated spin chains
(SrCuO2 , Sr2 CuO3 ), there is no indication of ballistic
heat transport of spinons in the frustrated spin-chain material linarite. The frustration ratio α = J2 /J1 in linarite is negative, whereas the occurrence of a finite Drude
weight has been predicted for α > 0 [8]. This raises the
question if the nature of the next-nearest neighbor interaction can influence the thermal transport behavior and
we hope that the present experimental study can motivate further theoretical investigations on thermal transport in a frustrated ferromagnetic J1 -J2 chain.

V.

CONCLUSION

We measured the thermal conductivity of linarite
across the magnetic phase diagram below 1 K as well
as far above TN in the paramagnetic regime. The heat
transport is dominated by phonons. However strong
magneto-elastic coupling limits the phonon mean free

0
0.0

0.2

0.4

0.6

0.8

0
1.0

T (K)

FIG. 9. The magnon mean free path of the magnon excitations at µ0 H = 0 T estimated using the kinetic model with
the experimental magnetic specific heat of linarite. The right
scale is normalized to the distance of magnetic ions.

path and leads to a drastic field dependence which is even
observable far above the ordering temperature. Due to
the significant magnetic scattering of the phonons relevant features of the magnetic phase diagram are indirectly detectable by the heat transport of the lattice. An
estimation of the phonon mean free path in the low temperature limit renders the phonon heat transport close
to the ballistic regime where phonon propagation is only
limited by the sample boundaries. The phonon mean free
path due to spin-phonon scattering has been determined
as function of temperature and shows different power law
behaviors depending on the magnetic field. Furthermore
we have found that in the helical magnetic phase there
is a direct contribution of magnetic excitations to the
thermal conductivity parallel to the spin-chain direction.
The mean free path of these excitations gives a measure
for the length of the materials spin-chain segments.
ACKNOWLEDGEMENTS

We thank Stefan Süllow and Kirrily Rule for fruitful discussions. This work has been supported by
the Deutsche Forschungsgemeinschaft under Contracts
No. WO 1532/3-2 and No. SU 229/9-2, through SFB
1143 (project-id 247310070), as well as the WürzburgDresden Cluster of Excellence on Complexity and Topology in Quantum Matter ct.qmat (EXC 2147, project-id
390858490). This work has been further supported by the
European Research Council (ERC) under the European
Union’s Horizon 2020 research and innovation program
(Grant Agreement No. 647276-MARS-ERC-2014-CoG)
and under the Marie Sklodowska-Curie actions (Grant
Agreement No 796048).

## PDF page 10

10
SUPPLEMENTAL MATERIAL
1.0

sample #1

~ T

Appendix A: Temperature dependence of κ

k / T (W K

-1

m

-1

)

µ0H = 16 T
0.8
1.10

0.6

0.4

0.2

~ T

1.42

0.0
0.0

0.2

0.4

0.6

0.8

1.0

T (K)

1.0

sample #1

~ T

FIG. 11. Thermal conductivity at 16 T of sample 1 fitted with
a power law (κ = C0 · T α ) where α = 2.42 for T < 0.4 K (solid
blue line) and α = 2.10 for 0.4 K < T < 1 K (dotted black
line)

1.50

Appendix B: Exponents of the power law behavior
of lspin-phonon

0.8

k / T (W K

-1

m

-1

)

µ0H = 0 T

0.6

0.4

~ T

1.04

0.2

0.0
0.0

0.2

0.4

0.6

0.8

1.0

µ0 H (T) p µ0 H (T) p
3
-3.8
8.5
-2.5
4
-4
9
-3.2
6
-1.5
9.5
0.1
7
-4
10
-1
8.1
-2.5
10.5
-2.5

T (K)

FIG. 10. Zero-field thermal conductivity of sample 1 fitted
with a power law (κ = C0 · T α ) where α = 2.50 for T < 0.4 K
(solid blue line) and α = 2.04 for 0.4 K < T < 1 K (dotted
black line)

TABLE I. Exponents of the power law behavior of
lspin-phonon = a0 T p as indicated by the dashed and solid black
lines in figure 7 (b).

[11] P. F. Schofield, C. C. Wilson, K. S. Knight, and C. A.
[1] X.
Zotos,
F.
Naef,
and
P.
Prelovsek,
Kirk, Can. Mineral. 47, 649 (2009).
Phys. Rev. B 55, 11029 (1997).
[12] K. C. Rule, B. Willenberg, M. Schäpers, A. U. B. Wolter,
[2] X. Zotos, Phys. Rev. Lett. 82, 1764 (1999).
B. Büchner, S.-L. Drechsler, G. Ehlers, D. A. Tennant,
[3] A.
Klümper
and
K.
Sakai,
Journal of Physics A: Mathematical and General 35, 2173 (2002).R. A. Mole, J. S. Gardner, S. Süllow, and S. Nishimoto,
Phys. Rev. B 95, 024430 (2017).
[4] T.
Kawamata,
N.
Takahashi,
T.
Adachi,
[13] A. U. B. Wolter, F. Lipps, M. Schäpers, S.T. Noji, K. Kudo, N. Kobayashi, and Y. Koike,
L. Drechsler, S. Nishimoto, R. Vogel, V. Kataev,
J. Phys. Soc. Jpn. 77, 034607 (2008).
B. Büchner, H. Rosner, M. Schmitt, M. Uhlarz, Y. Sk[5] N. Hlubek, P. Ribeiro, R. Saint-Martin, A. Revcolevschi,
G. Roth, G. Behr, B. Büchner, and C. Hess,
ourski, J. Wosnitza, S. Süllow, and K. C. Rule,
Phys. Rev. B 81, 020405 (2010).
Phys. Rev. B 85, 014407 (2012).
[6] N. Hlubek, X. Zotos, S. Singh, R. Saint-Martin,
[14] M. Schäpers, A. U. B. Wolter, S. L. Drechsler, S. NishiA. Revcolevschi,
B. Büchner, and C. Hess,
moto, K. H. Müller, M. Abdel-Hafiez, W. SchottenJournal of Statistical Mechanics: Theory and Experiment 2012, hamel,
P03006 B.
(2012).
Büchner, J. Richter, B. Ouladdiaf, M. Uhlarz,
[7] C. Hess, Physics Reports 811, 1 (2019).
R. Beyer, Y. Skourski, J. Wosnitza, K. C. Rule, H. Ryll,
B. Klemke, K. Kiefer, M. Reehuis, B. Willenberg, and
[8] J. Stolpp, S.-S. Zhang, F. Heidrich-Meisner, and C. D.
S. Süllow, Physical Review B 88, 184410 (2013).
Batista, Phys. Rev. B 99, 134413 (2019).
[15] B. Willenberg, M. Schäpers, K. C. Rule, S. Süllow,
[9] X. G. Liu, X. M. Wang, W. P. Ke, W. Tao, X. Zhao, and
M. Reehuis, H. Ryll, B. Klemke, K. Kiefer, W. SchotX. F. Sun, Phys. Rev. B 83, 144408 (2011).
tenhamel, B. Büchner, B. Ouladdiaf, M. Uhlarz,
[10] H. Effenberger, Mineralogy and Petrology 36, 3 (1987).

## PDF page 11

11
R. Beyer, J. Wosnitza, and A. U. B. Wolter,
Phys Rev Lett 108, 117202 (2012).
[16] T. Mack, A. Ruff, H.-A. Krug von Nidda, A. Loidl, and
S. Krohns, Sci. Rep. 7, 1 (2017).
[17] E.
Cemal,
M.
Enderle,
R.
K.
Kremer,
B. Fak, E. Ressouche, J. P. Goff, M. V.
Gvozdikova, M. E. Zhitomirsky, and T. Ziman,
Phys Rev Lett 120, 067203 (2018).
[18] Y. Feng, K. Yu. Povarov, and A. Zheludev,
Phys. Rev. B 98, 054419 (2018).
[19] K. Yu. Povarov, Y. Feng, and A. Zheludev,
Phys. Rev. B 94, 214409 (2016).
[20] B. Willenberg, M. Schäpers, A. U. B. Wolter, S.-L.
Drechsler, M. Reehuis, J.-U. Hoffmann, B. Büchner, A. J.
Studer, K. C. Rule, B. Ouladdiaf, S. Süllow, and S. Nishimoto, Phys. Rev. Lett. 116, 047202 (2016).

[21] L. Heinze, G. Bastien, B. Ryll, J.-U. Hoffmann,
M. Reehuis, B. Ouladdiaf, F. Bert, E. Kermarrec,
P. Mendels, S. Nishimoto, S.-L. Drechsler, U. K.
Rößler, H. Rosner, B. Büchner, A. J. Studer,
K. C. Rule, S. Süllow, and A. U. B. Wolter,
Phys. Rev. B 99, 094436 (2019).
[22] R.
O.
Pohl
and
B.
Stritzker,
Phys. Rev. B 25, 3608 (1982).
[23] P. D. Thacher, Phys. Rev. 156, 975 (1967).
[24] L. Taillefer, B. Lussier, R. Gagnon, K. Behnia, and
H. Aubin, Phys. Rev. Lett. 79, 483 (1997).
[25] S. K. Gotovko, L. E. Svistov, A. M. Kuzmenko, A. Pimenov, and M. E. Zhitomirsky,
Physical Review B 100, 174412 (2019), pRB.
[26] L. Heinze, K. C. Rule, and S. Süllow, unpublished.
[27] C. Hess, H. ElHaes, A. Waske, B. Büchner, C. Sekar,
G. Krabbes, F. Heidrich-Meisner, and W. Brenig,
Physical Review Letters 98, 027201 (2007).
