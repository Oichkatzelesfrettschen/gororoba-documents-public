Source: https://arxiv.org/abs/2408.00873v2
PDF sha256: 3eb55e4fd14067a510d6c5053ea318bd299eabd0e39045cdbff88d2765373268
License: http://creativecommons.org/licenses/by/4.0/

# Transcription of arxiv_2408.00873_baco2_honeycomb_thermal_scaling.pdf

Transcription of `arxiv_2408.00873_baco2_honeycomb_thermal_scaling.pdf` in this directory, 8 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 3, 5 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories; pages 1-2, 4, 6-8 from the PDF's own text layer (pdftotext version 26.10.0, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Scaling behavior and giant field-enhancement of the thermal conductivity in the
honeycomb antiferromagnet BaCo2 (AsO4 )2
Jiayi Hu1 , Ruidan Zhong2,* , Peter Czajka1 , Tong Gao1,** , R. J Cava2 , and N. P. Ong1
1

Department of Physics, Princeton University,
Princeton, NJ, 08544, USA
2
Department of Chemistry, Princeton University,
Princeton, NJ, 08544, USA

arXiv:2408.00873v2 [cond-mat.str-el] 24 Oct 2024

(Dated: October 28, 2024)
The layered honeycomb material BaCo2 (AsO4 )2 (BCAO) is of topical interest because its magnetic
state is related to that of the Kitaev magnet α-RuCl3 . Using thermal transport to probe how
magnetic excitations interact with phonons in the magnetically disordered regime, we have uncovered
an unusually large enhancement of the thermal conductivity κxx in an in-plane magnetic field H.
Just above the Néel temperature TN , a field of 13 T increases κxx by a factor ∼ 211, much larger than
reported previously in any magnetic insulator. Interestingly, κxx (H, T ) exhibits a scaling behavior
in the entire magnetically disordered region that surrounds the ordered zigzag state. The ratio
∆κxx (H, T )/κxx (13, T ), measured throughout the disordered region, collapses to a one-parameter
scaling function exp(−1/gx) (where x = µB B/kB T and g is a constant).

I.

INTRODUCTION

The family of layered honeycomb spin- 21 magnetic materials has attracted considerable interest. In particular,
the ruthenate α-RuCl3 with local moments derived from
4d orbitals in Ru has been identified [1, 2] as the closest
proximate to the Kitaev Hamiltonian HK [3]. The lowtemperature thermal transport properties have played a
central role in illuminating the extent to which predictions based on HK agree with experiment [4–8]. Interest
has extended to related layered, honeycomb spin- 12 materials. In the cobaltate BaCo2 (AsO4 )2 (BCAO), the local
moments based on Co-3d orbitals undergo a sharp transition to a zig-zag state at the Néel temperature TN = 5.4
K [9–11]. In its magnetic, thermal and crystallographic
properties, BCAO shares many features with α-RuCl3 . A
number of recent reports have compared their magnetic
and transport properties [8, 12–20].
In the case of BCAO, the theoretical and experimental
investigations appear to favor a J1 -J3 , XXZ Hamiltonian instead of the Kitaev Hamiltonian [13–18]. Below
TN , the spins in BCAO exhibit a helical magnetic texture
in the ab-plane. The spins, nominally aligned along the
b-axis, exhibit a spiral structure with axis parallel to a∗ .
In an in-plane magnetic field H, the spins are polarized in
a ferrimagnetic, colinear pattern above a field Hc1 ∼ 0.2
T. Long-range magnetic order is suppressed at the critical field Hc2 = 0.5 T [9][11][13]. The transition at the
lower field Hc1 has been investigated by magnetization
and terahertz spectroscopy experiments [12, 13, 19]. A
recent study combining angular dependence of magnetization and dilatometry suggests an intermediate phase
appears before the spins are fully polarized [18]. Another thermal transport experiment measured down to
subKelvin temperatures supports the KQSL picture, yet
other theoretical proposal attribute it to a Dirac spin
liquid phase [19, 21].
Our work here focusses on the magnetically disordered

regime which covers a large fraction of the H-T plane.
We report an unusual scaling behavior of the thermal
conductivity κxx (H, T ) in BCAO observed throughout
the magnetically disordered region below 10 K. In zero
H, strong inelastic scattering of phonons from spin excitations severely suppresses phonon conduction. In an
in-plane magnetic field H, κxx (H, T ) increases dramatically following a one-parameter scaling function. Just
above TN , the field-induced enhancement factor (> 200)
exceeds that previously reported in all magnetic insulators to our knowledge.
Underlying the giant field-enhancement of κxx is the
intense scattering of phonons by the spins which leads
to “localization” of the phonons in zero H. Our results
suggest that the non-analytic behavior of κxx (H, T ) in
the limit H → 0, as well as the scaling behavior over
a large fraction of the magnetically disordered region,
may well be signature hallmarks of strong spin-phonon
coupling.
In several topical areas, e.g. spin qubits based on NV
centers in diamond [22], spin-phonon coupling is a key
topic of interest. The scaling behavior uncovered here
suggests an incisive way to probe these couplings in magnetic materials.

II.

EXPERIMENT

To measure the thermal conductivity tensor κij of
the BCAO crystal, we heat sunk 3 RuO2 thermometers
(matched and calibrated) to its edges using stycast and
gold wires (Fig. 1a). One short edge of the crystal is heat
sunk to the bath (brass substrate) while the opposite edge
is attached to a heater via gold wires. The sample space
is kept at a pressure less than 5 × 10−5 mbar. We label
as x̂ the common axis of the heat current density J and
field H.
Typically, we measure the field profile of κxx (H, T )

## PDF page 2

2

FIG. 1: Panel (a): Schematic of the crystal attached to the heater, 3 thermometers and the bath by gold wires. The applied
H direction is indicated. Panel (b): The two-up, two-down zigzag phase inferred from neutron scattering [11]. Panel (c):
Comparison of the zero-H κ(T ) (square blue symbols, multiplied by a factor of 30) with κxx vs. T measured in an in-plane
13-T magnetic field (red symbols). The faint blue curve passing through the blue symbols is an interpolation supplemented
by measurements in zero H in which T is continuously varied. The red curve is a fit to the 13-T data using the standard
Callaway expression. More details can be found in the Supplement [23]. Panel (d): The inferred phase diagram of BCAO in
the H-T plane. The magnetically ordered zigzag state is shaded red and coral. Throughout the disordered region (shaded
green), κxx (H, T ) obeys a one-parameter scaling behavior. Deviation from this scaling occurs in the blue region. The fields
Hc1 and Hc2 are obtained from data presented in Figure 2a.

keeping the bath temperature Tbath regulated at a set
point as H is swept from 0 to 13 T and back. At low
T , the applied heat current invariably leads to a finite
shift δT = T − Tbath between the sample’s temperature
T and Tbath (the shift is usually nearly H independent).
Here, however, the anomalously large (211-fold) increase
in κxx (H, T ) causes δT (H, T ) to be strongly field dependent. In all field profiles reported here, we have recorded
δT (H, T ) to correct for these shifts. We also adopted
steps to avoid errors arising from large magnetocaloric
effects which lead to long relaxation times for both the
sample and bath to reach equilibrium whenever H undergoes a step-change (Secs. 1, 3 and 4 of Supplement [23]).
Finally, the tendency of the crystal to fracture under
strain exerted by magnetic torque restricts measurements
so far to in-plane H.
Motivated by the observation of an unusual planar
thermal Hall conductivity κxy in the Kitaev magnet αRuCl3 [6, 7], we have searched for a planar thermal Hall
signal in BCAO focusing on the disordered region close
to the ordered phase. Despite a careful search we did not
detect a finite κxy signal in BCAO within our resolution
(See Sec. 7 of Supplement [23]).

III.

FIELD AND TEMPERATURE PROFILES
OF THERMAL CONDUCTIVITY

The thermal conductivity κxx (H, T ) of BCAO displays
a rich set of features as a function of temperature T and
an in-plane magnetic field H. In the absence of H, κ(T )

(≡ κxx (0, T ), plotted as blue symbols in Fig 1c) slowly
decreases to an anomalously low value (∼ 0.6 W/mK) as
T is lowered to 5.4 K. At the Néel temperature TN (5.4
K), the spins undergo a phase transition to an antiferromagnetic state with zig-zag order. In the ordered state,
κ rises to a broad peak that reflects contributions from
phonons and magnons in the ordered state.
In our experiment, we observe that long-range order
is abruptly suppressed by an in-plane field H ∼ 0.5 T,
consistent with previous studies [12, 13, 15, 20]. As described below, phonons remain strongly coupled to spin
excitations throughout the disordered region surrounding
the ordered state (green region in Fig. 1d). The strong
coupling is steadily weakened as H increases. Eventually,
at large H (13 T), scattering of phonons by the spins becomes negligible, and κxx attains large values (red symbols in Panel c). The field enhancement, expressed by
the ratio κxx (H, T )/κ(T ) (∼ 211 just above TN ) exceeds
that in all other magnetic insulator reported to date. Our
key result is that, over the entire magnetically disordered
region (green region in Panel d), κxx (H, T ) obeys a oneparameter scaling function.
Figure 2a displays field profiles of κxx within the ordered state with T fixed at the values indicated. At the
lowest T (0.49 K), the profile of κxx is virtually flat.
When T is raised (1.64 to 2.75 K) the field profiles feature a dome that is abruptly truncated on the large-H
side by a vertical cliff as H approaches Hc2 (0.5 T), and
long-range order is suppressed. On the low H side, the
dome displays a notch that corresponds to the lower critical field Hc1 (∼ 0.12 T). In previous reports, Hc1 was in-

## PDF page 3

3
b
a
...7.5 K
2.75
10
2.68
7
150
8
4.39 K
K<sub>xx</sub> (Wm<sup>-1</sup>K<sup>-1</sup>)
<math>K_{xx} (Wm^{-1}K^{-1})</math>
100
6
1.75<br>1.64
1.03
50
0.49
2
6.09 6.26
0
0.5
1.0
0.0
10
11
2
3
9
0
8
5
<math>\mu_0 H</math> (T)
<math>\mu_0H</math> (T)
d
C
<math>10^{2}</math>
150 -
6<br>4<br>2<br>4<br>2
10<sup>1</sup>
<math>\Delta K_{xx} (Wm^{-1}K^{-1})</math>
<math>K_{xx} (Wm^{-1}K^{-1})</math>
0
2 3<br>μ<sub>0</sub>H (T)
4
100
10<sup>0</sup>
1.5<sub>T</sub>
10<sup>-1</sup>
50
T (K)
0.6
10<sup>-2</sup>
6.4
5.4
7.4
8.4
9.4
0
0
2
3
4
5
6
7
8
0.1
<math>x = \mu_B B / k_B T</math>
T (K)
<b>FIG. 2:</b> Profiles of <math>\kappa_{xx}</math> vs. field and temperature. Panel (a): Field profiles of <math>\kappa_{xx}(H,T)</math> at low <math>H</math> (<math>\mu_0 H < 1.2</math> T). In each
curve, T is fixed at the values indicated. Curves in the temperature interval <math>1.6 < T < 2.8</math> K display a vertical cliff that
signals the abrupt collapse of long-range magnetic order as H approaches <math>H_{c2} = 0.5</math> T. At low H, a second sharp feature <math>H_{c1}</math>
(<math>\sim 0.1 \text{ T}</math>) is observed. Panel (b): Field profiles of <math>\kappa_{xx}</math> extended to 11 T, with T fixed at the values indicated. At each T, <math>\kappa_{xx}</math>
initially increases exponentially with <math>H</math>. At large <math>H</math>, it gradually saturates to its high-field limit. Profiles shown in Panel (a)
are visible as the small mesa below 0.5 T. Panel (c): Curves of <math>\kappa_{xx}(H,T)</math> plotted versus T with H fixed at the values
indicated. The curve <math>\kappa_{xx}(13,T)</math> at the maximum applied <math>H</math> (13 T) serves as an envelope that caps the maximum value
attained at each temperature T. Each curve (e.g. the one at <math>H=4</math> T) initially tracks closely <math>\kappa_{xx}(13,T)</math> as T is raised above
1 K, but deviates away from <math>\kappa_{xx}(13,T)</math> as T is raised (at <math>\sim 2.5</math> K). Curves taken at larger H (e.g. 10 T) deviate from
<math>\kappa_{xx}(13,T)</math> at a higher temperature (4 K). This pattern reflects the one-parameter scaling behavior discussed below. Note the
anomalously low values of <math>\kappa_{xx}</math> in the curve at 0.6 T. Panel (d): First hints of scaling behavior above <math>T_N</math>. When we plot the
field-induced change <math>\Delta \kappa_{xx}(H,T)</math> vs. the scaling variable <math>\mu_0 H/T</math>, we find that all data points above <math>T_N</math> converge to the same
curve when the scaling variable <math>\mu_0 H/T</math> falls below <math>\sim 0.4</math> T/K. The temperature of each data point is given by the color scale.
axis extended to 11 T (the profiles in the ordered phase
terpreted as a transition between either an incommensu-
rate spiral state or a double zigzag pattern to the cAFM
are now reduced to small mesas visible below 0.5 T). At
state 11, 20. Unlike in Refs. 12, 19, we observe only a
each T (e.g. 3 K), <math>\kappa_{xx}</math> increases from a small value (<math>\sim</math>
single sharp transition within the field interval 0.1–0.2 T.
1 W/mK) before slowly saturating to a maximum value
<math>(\sim 42 \text{ W/mK})</math> as H increases to 13 T. All the profiles
In the disordered phase above <math>H_{c2}</math>, <math>\kappa_{xx}</math> increases steeply
with <math>H</math>. This is a small fraction of the scaling pattern
appear to follow the same functional form, with a pattern
uncovered below.
amenable to simple analysis.
Figure 2b shows the field profiles of <math>\kappa_{xx}</math> with the H
To this end, we turn to the orthogonal cuts in which

## PDF page 4

4
κxx (H, T ) is plotted vs. T with H fixed (Fig. 2c). At
each fixed value of H, the curve of κxx vs. T is now
non-monotonic, exhibiting a broad maximum at the temperature Tp (H). As shown in the inset, Tp (H) increases
roughly linearly with H. This suggests that, in the disordered region, κxx depends on H solely through the scaling variable
x = µB B/kB T,

(1)

where µB and kB are, respectively, the Bohr magneton
and the Boltzmann constant, and B = µ0 H is the magentic flux density with µ0 the vacuum permeability.
To test this preliminary hint of scaling behavior, we
plot in Fig. 2d the field-induced change ∆κxx (H, T ) =
κxx (H, T ) − κxx (0, T ) versus x in log-log scale for T between 5.4 and 9.5 K. We find that the data merge to
define a scaling curve that extends over nearly 3 decades
in ∆κxx (H, T ).
Another important feature in Fig. 2c is the role of
κxx (13, T ) (black squares) relative to κxx measured at
lower fields throughout the disordered region. Combining
the perspectives afforded by the fixed-T and fixed-H cuts,
we infer that when T is fixed (e.g. at 4 K), κxx increases
towards κxx (13, T ) but does not exceed it.
Physically, this implies that, in the high-field limit,
phonon conduction asymptotes to the regime in which
ℓ, restricted by scattering from crystalline disorder only,
becomes independent of T . In this limit, the T dependence observed in κxx (H, T ) = 31 cgs (T )vs ℓ arises from
the heat capacity cgs (T ) of the spin-phonon system (vs
is the group velocity of the acoustic branch). As inferred
from the field profiles in Fig. 2b, κxx (13, T ) is a good approximation to this high-field limit below T = 6 K. The
approximation is less satisfactory above 6 K as saturation is approached at increasingly large H. The dashed
curve in Fig. 2c is a fit to κxx (13, T ) using the Callaway
model in this limit (see Sec. 2 of Supplement [23]).
IV.

SCALING BEHAVIOR

The functional form of the scaling curve in Fig. 2d
becomes evident when we plot ∆κxx vs. 1/x in semilog
plot. As shown in Fig. 3a, all the data above 5.4 K collapse onto the straight line corresponding to the function
∆κxx ∼ e−1/gx with g a constant.
The simple scaling based on x accounts only for the
H dependence of ∆κxx (T, H). The further dependence
on T requires more care. This becomes apparent if we
attempt to apply the same analysis to the data below 5.4
K in the disordered region (H > Hc2 ).
The semilog plot of κxx vs. 1/x shown in Fig. 3b reveals that the data segregate into two distinct groups.
Data in the ordered phase (not relevant to scaling) follow flat trajectories that are nearly independent of x. By
contrast, the data in the disordered region fall along diagonal curves that mimic the scaling function except that
they are now displaced vertically by a factor of the form

T β with exponent 2 < β < 3, which we infer arises from
the heat capacity cgs (T ). From the discussion on Fig.
2c, we anticipate that the offsets can be cancelled if we
divide κxx (H, T ) by κxx (13, T ).
This inference is confirmed when we replot
κxx (H, T )/κxx (13, T ) vs.
1/x in Fig.
3c (upper
panel). Now all data throughout the disordered region
below 5.4 K collapse onto one scaling curve. A similar
plot shows that data above 5.4 K also collapse onto the
same curve (lower panel). As noted above, deviation
from scaling appears when x exceeds ∼ 0.3.
Hence, throughout the disordered region below and
above 5.4 K, the ratio ∆κxx (H, T )/κxx (13, T ) is described by the one-parameter scaling form
∆κxx (H, T )
1
= A exp[− ]
κxx (13, T )
gx

(2)

where x is given by Eq. 1 and A and g are constants.
The function e−1/gx implies that ∆κxx initially increases from zero at a very slow rate (the non-analytic
limit H → 0 requires all derivatives to vanish). As discussed, the ultra-slow initial growth may be seen in Fig.
2a. However, once B rises above 1 Tesla, ∆κxx undergoes an exponential increase before ultimately saturating
to a very large value consistent with phonons in a crystal
with a low density of lattice and spin disorder.
We sketch the physical picture suggested by our results. The single-parameter scaling form constrains the
candidate scenarios for describing the field-enhanced κxx .
First, the anomalously low value of κ(T ) in the fluctuating interval 5.4 < T < 10 K at H = 0 implies strong
spin-phonon coupling which leads to repeated absorption
or emission of phonons accompanied by spin flips. Secondly, the non-analytic nature in Eq. 2 in the limit x → 0
implies that, in weak H, deviation of ∆κxx (H, T ) from
zero is initially nearly unresolvable until H exceeds a field
scale of ∼ 1 T. Then κxx increases exponentially. This
strongly non-linear increase is not amenable to a perturbative treatment. (We also point out that Eq. 2 is very
different from the familiar expression e−∆b /kB T describing thermal activation of charge carriers across a band
gap ∆b .)
Throughout the disordered region, we infer that the
phonons and spin excitations constitute a tightly coupled system in which ℓ0 (the phonon mean-free path at
H = 0) is limited to less than 30 nm by intense scattering. Although the scattering may be elastic or inelastic, the scaling form implies that inelastic processes are
dominant in the disordered region. By analogy with experiments on the honeycomb system α-RuCl3 [24–27] we
may expect that spin excitations in the disordered state
exhibit a broad, featureless spectrum that is gapless in
zero H. The low-lying spin excitations interact strongly
with phonons at a select population of sites, which absorb and emit phonons. At temperature T , the phonon
energy distribution peaks sharply at ℏω ≃ kB T .
An applied Zeeman field opens a gap ∆ = gµB H in
the spin spectrum where g is the effective gyromagnetic

## PDF page 5

5
a
C
10
12
2
8
14
6
0.0
5.4
10<sup>0</sup>
T > 5.4 K
<math>10^{2}</math>
T < 5.4 K
10<sup>1</sup>
<math>\Delta K_{xx} (Wm^{-1}K^{-1})</math>
10<sup>-1</sup>
10<sup>-2</sup>
<math>10^{-2}</math>
T<sub>avg</sub> (K)
<math>\kappa_{xx}(H,T)</math> / <math>\kappa_{xx}(13T,T)</math>
10<sup>-3</sup> 5.4
.5 K
10
15
5
20
0
<math>x^{-1} = k_B T / \mu_B B</math>
00
5.4
10.0
b
0.5
10<sup>2</sup>
T > 5.4 K
T < 5.4 K
disordered
<math>10^{-1}</math>
ordered
<math>\kappa_{xx}</math> (Wm<sup>-1</sup>K<sup>-1</sup>)
10<sup>1</sup>
10<sup>-2</sup> ·
<math>10^{0}</math>
5.0 K •
2.2 2.8<br>2.0
0.5
4.7
3.3
10<sup>-3</sup>
10<sup>-1</sup>
12
10
12
16 18 20
2
10
0
8
2
14
14
0
8
6
6
4
<math>x^{-1} = k_B T / \mu_B B</math>
<math>x^{-1} = k_B T / \mu_B B</math>
FIG. 3: Uncovering the scaling behavior. (Panel a) The analytical form of the scaling behavior implied in Fig. 2 becomes
apparent in a semilog plot of <math>\Delta \kappa_{xx}</math> vs. <math>1/x</math> with x defined in Eq. [1] All data points taken above <math>T_N</math> fall on the dashed line
given by Eqs. 2 and 1. The equation of the fit (dashed line) is <math>\ln \Delta \kappa_{xx} = -0.628 \, x^{-1} + 5.476</math>, which gives <math>g = 1.6</math>. The scatter
as <math>x \to 0</math> reflects uncertainties in <math>\Delta \kappa_{xx}</math>. (Panel b) Finding the missing pre-factor in the scaling form. At temperatures below
5.4 K, the data points <math>\kappa_{xx}(H,T)</math> segregate into two distinct groups when plotted vs. <math>1/x</math>. In the ordered phase <math>(H < H_{c2})</math>,
the data follow nearly flat trajectories. By contrast, data in the disordered region <math>(H > H_{c2})</math> fall on diagonal curves that
match the dashed line in Panel (a), except that they are systematically displaced downwards as <math>T \to 0</math>. This suggests that <math>\kappa_{xx}</math>
should be divided by a T-dependent factor <math>T^{\beta}</math>, which we approximate by the measured curve <math>\kappa_{xx}(13,T)</math>. (Panel c): Semilog
plots of <math>\kappa_{xx}/\kappa_{xx}(13,T)</math> vs. <math>1/x</math> for <math>T < 5.4</math> K (upper panel) and <math>T > 5.4</math> K (lower). Once <math>\kappa_{xx}</math> is divided by <math>\kappa_{xx}(13,T)</math>, the
diagonal curves in Panel (b) collapse to a single curve, which represents the universal curve given in Eq. [2]. The data above
5.4 K also collapse onto the same curve (lower panel). Hence, over the disordered region (green region in Fig. 11), scaling
behavior prevails. Departure from scaling becomes observable when <math>1/x</math> decreases below <math>\sim 3</math> (dark blue region in Fig. 11).
parameter for the low-lying spin excitations. Phonon an-
hatches far exceeds <math>\ell_0</math>. Each liberated phonon does not
nihilation is blocked when the gap exceeds <math>k_{\rm B}T</math>, i.e.
travel far before becoming retrapped. Hence the initial
increase in <math>\kappa_{xx}</math> is nearly unresolvable, as shown in Figures
<math>g\mu_{\rm B}B > k_{\rm B}T</math>.
(3)
2a and 2b, and implied by the non-analyticity of <math>e^{-T/B}</math>
in the limit <math>B \to 0</math>. Crucially, by Eq. 3 the field at which
In effect, the identified absorption sites act as escape
phonons escape at the identified sites is proportional to
hatches that are propped open by <math>H</math>. Rendering these
T. Hence, the field-induced increase in <math>\ell</math> automatically
sites transparent to phonons allows them to escape the
satisfies the scaling in Eq. 2
trapping well. Despite their small population, these sites
play an outsize role in determining the initial growth of
Increasing <math>H</math> weakens the amplitude of the fluctuating
magnetic order by increasing the polarization of spins,
<math>\kappa_{xx}(H,T)</math>.
which causes the population of escape hatches to pro-
When <math>H</math> is weak, the average spacing between escape

## PDF page 6

6
liferate. In analogy with percolation conductance, the
largest enhancement of ℓ occurs when connected paths
form skeletal spines that span the crystal. When H exceeds ∼ 1 T, rapid proliferation of the hatches enables
the connectivity of phonon propagation paths to exceed
the percolation limit, and κxx undergoes the exponential
growth observed.

V.

COMPARISON WITH OTHER MAGNETIC
INSULATORS

Experiments showing large field-induced enhancement
of κxx have been reported in several layered magnetic
insulators. We briefly survey the results beginning with
the largest previously reported (Fig. 4 and Table S1 in
Supplement [23]). Zhao et al. found that, in Co3 V2 O8 ,
κxx increases 100 fold in a field of 14 T [28] at 7.5K.
They interpret the increase as caused by a series of magnetic phase transitions occuring in a narrow window (5
transitions between 6 and 12 K). While there are fewer
known phase transitions in the case of BCAO, recent
dilatometry experiment indeed suggests more intermediate phases [18]. One difference we want to point out
though is that BCAO has only one critical temperature,
and it has been relatively robust even when applied pressure [15]. More importantly, the field-induced enhancement persists up to as high as 13T well beyond the critical
field Hc2 = 0.5T , and the scaling behavior also covers a
wide regime in the phase diagram surrounding the ordering states. As a result, a succession of phase transitions
doesn’t seem to be the whole story, though intense spin
fluctuations do seem to be one of the key components.
A recent experiment on another honeycomb Kitaev
magnet candidate Na2 Co2 TeO6 found that κxx increases
by a factor of 70 in a field of 16 T [29]. The authors attribute this intense scattering to the abundance of magnetic excitations above a triple-Q ground state. The authors do not report any scaling behavior in the observed
κxx vs. H.
In the Kitaev magnet α-RuCl3 , κxx has been reported
to increase 13-fold compared to the value at 7T , the critical field of its zig-zag state [30]. The ratio is smaller if
compared to its zero field value (See Table 1 in the Supplement [23]). The authors are able to fit κab with a modified Callaway model, adding a relaxation term that takes
into account the resonance between phonon and magnetic
gap, whose size is linear to the applied field. Motivated
by this study, We also tried fitting our data at finite field
with the modified Callaway model, with spin-phonon resonance terms. However, we have not succeeded in fitting
our data with physically meaningful parameters (the exception is the curve at 13 T where ℓ is limited by disorder
scattering). In fact, the non-analyticity inherent in the
H → 0 limit in Eq.3 rules out a Callaway-type description in the scaling regime in BCAO. Because it is not
possible to reproduce the non-analyticity in a Callowaytype formulation, our conclusion is that the empirical fits

FIG. 4: Comparison of the field enhancement of κxx
(expressed as a ratio) with the ratio reported for other
magnetic insulators[28–34]. BCAO is marked with a red
star. In the ratio for HoMnO∗3 the denominator is κxx (2.2T).
For RuCl∗∗
3 , the denominator is κxx (7.5T). See Sec. 6 in
Supplement [23] for detailed information.

used in α-RuCl3 cannot be applied to BCAO.

***************

## PDF page 7

7
*Present address of R.Z.: Tsung-Dao Lee Institute and
School of Physics and Astronomy, Shanghai Jiao Tong
University, Shanghai 201210, China
**Present address of T.G.: Building 3, West Area,
Xibeiwang East Street, Haidian District, Beijing 100193,
China

J.H. and N.P.O. The crystals were grown and characterized by R.Z. and R.J.C. The manuscript was written by
J.H. and N.P.O. with input from all authors.

Acknowledgement The thermal transport experiments
were supported by the US Department of Energy (Basic Energy Sciences) under contract DE-SC0017863
to N.P.O. An award from the U.S. National Science
Foundation (DMR 2011750) supported the materials
growth (R.J.C.) and acquisition of cryogenic equipment
(N.P.O.). N.P.O. acknowledges support from the Gordon and Betty Moore Foundation EPiQS initiative (grant
GBMF9466).

Additional Information
Supplementary Materials is available in the online version
of the paper.

Competing financial interests
The authors declare no competing financial interests.

Correspondence and requests for materials should
be addressed to J.H. (jiayih@princeton.edu) or N.P.O.
(npo@princeton.edu).

Author contributions
J.H., P.C. and N.P.O. conceptualized the experiment.
J.H. performed all measurements with initial guidance
from P.C. Data in an earlier experiment by T.G. provided
substantial insights. The present data were analyzed by

[1] Banerjee, A., Bridges, C.A., Yan, J.Q., Aczel, A.A., Li,
L., Stone, M.B., Granroth, G.E., Lumsden, M.D., Yiu,
Y., Knolle, J. and Bhattacharjee, S., Proximate Kitaev
quantum spin liquid behaviour in a honeycomb magnet.
Nature Materials. 15, 733-740 (2016).
[2] Jackeli, G. and Khaliullin, G. Mott Insulators in the
Strong Spin-Orbit Coupling Limit: From Heisenberg to a
Quantum Compass and Kitaev Models. Phys. Rev. Lett..
102, 017205 (2009,1).
[3] Kitaev, A. Anyons in an exactly solved model and beyond. Annals Of Physics. 321, 2-111 (2006), January
Special Issue.
[4] Leahy, I., Pocs, C., Siegfried, P., Graf, D., Do, S., Choi,
K., Normand, B. and Lee, M. Anomalous thermal conductivity and magnetic torque response in the honeycomb magnet α-RuCl3 . Physical Review Letters. 118,
187203 (2017).
[5] Czajka, P., Gao, T., Hirschberger, M., Lampen-Kelley,
P., Banerjee, A., Yan, J., Mandrus, D., Nagler, S. and
Ong, N. Oscillations of the thermal conductivity in the
spin-liquid state of α-RuCl3 . Nature Physics. 17, 915-919
(2021).
[6] Kasahara, Y., Ohnishi, T., Mizukami, Y., Tanaka, O.,
Ma, S., Sugii, K., Kurita, N., Tanaka, H., Nasu, J., Motome, Y. and Others, Majorana quantization and halfinteger thermal quantum Hall effect in a Kitaev spin liquid. Nature. 559, 227-231 (2018).
[7] Czajka, P., Gao, T., Hirschberger, M., Lampen-Kelley,
P., Banerjee, A., Quirk, N., Mandrus, D., Nagler, S. and
Ong, N. Planar thermal Hall effect of topological bosons
in the Kitaev magnet α-RuCl3 . Nature Materials. 22, 3641 (2023).
[8] Liu, H. and Khaliullin, G. Pseudospin exchange interactions in d7 cobalt compounds: Possible realization of the
Kitaev model. Phys. Rev. B. 97, 014407 (2018,1).

[9] Regnault, L., Burlet, P. and Rossat-Mignod, J. Magnetic
ordering in a planar X - Y model: BaCo2 (AsO4 )2 . Physica B+C. 86-88 pp. 660-662 (1977).
[10] Regnault, L., Rossat-Mignod, J., Villain, J. and Combarieu, A. Specific heat of the quasi 2D-XY helimagnets
BaCo2 (AsO4 )2 and BaCo2 (PO4 )2 . Journal De Physique
Colloques. 39, C6-759-C6-761 (1978)
[11] Regnault, L., Boullier, C. and Lorenzo, J. Polarizedneutron investigation of magnetic ordering and spin dynamics in BaCo2 (AsO4 )2 frustrated honeycomb-lattice
magnet. Heliyon. 4, e00507 (2018).
[12] Zhong, R., Gao, T., Ong, N. and Robert J. Cava Weakfield induced nonmagnetic state in a Co-based honeycomb. Science Advances. 6, eaay6953 (2020).
[13] Halloran, T., Desrochers, F., Zhang, E., Chen, T., Chern,
L., Xu, Z., Winn, B., Graves-Brook, M., Stone, M.,
Kolesnikov, A. and Others, Geometrical frustration versus Kitaev interactions in BaCo2 (AsO4 )2 . Proceedings Of
The National Academy Of Sciences. 120, e2215509119
(2023).
[14] Maksimov, P., Ushakov, A., Pchelkina, Z., Li, Y., Winter, S. and Streltsov, S. Ab initio guided minimal model
for the “Kitaev” material BaCo2 (AsO4 )2 : Importance of
direct hopping, third-neighbor exchange, and quantum
fluctuations. Physical Review B. 106, 165131 (2022)
[15] Huyan, S., Schmidt, J., Gati, E., Zhong, R., Cava, R.,
Canfield, P. and Bud’Ko, S. Hydrostatic pressure effect on the Co-based honeycomb magnet BaCo2 (AsO4 )2 .
Physical Review B. 105, 184431 (2022)
[16] Das, S., Voleti, S., Saha-Dasgupta, T. and Paramekanti,
A. XY magnetism, Kitaev exchange, and long-range frustration in the Jef f = 1/2 honeycomb cobaltates. Physical
Review B. 104, 134425 (2021)
[17] Winter, S. Magnetic couplings in edge-sharing high-spin
d 7 compounds. Journal Of Physics: Materials. 5, 045003

## PDF page 8

8
(2022)
[18] Mukharjee, P., Shen, B., Erdmann, S., Jesche, A., Kaiser,
J., Baral, P., Zaharko, O., Gegenwart, P. and Tsirlin, A.
Intermediate field-induced phase of the honeycomb magnet BaCo2 (AsO4 )2 . ArXiv Preprint arXiv:2403.04466.
(2024)
[19] Tu, C., Dai, D., Zhang, X., Zhao, C., Jin, X., Gao,
B., Dai, P. and Li, S. Evidence for gapless quantum spin liquid in a honeycomb lattice. ArXiv Preprint
arXiv:2212.07322. (2022).
[20] Zhang, X., Xu, Y., Halloran, T., Zhong, R., Broholm,
C., Cava, R., Drichko, N. and Armitage, N. A magnetic continuum in the cobalt-based honeycomb magnet
BaCo2 (AsO4 )2 . Nature Materials. 22, 58-63 (2023).
[21] Bose, A., Routh, M., Voleti, S., Saha, S., Kumar, M.,
Saha-Dasgupta, T. and Paramekanti, A. Proximate Dirac
spin liquid in the honeycomb lattice J1 -J3 XXZ model:
Numerical study and application to cobaltates. Physical
Review B. 108, 174422 (2023)
[22] Wolfowicz, G., Heremans, F., Anderson, C., Kanai, S.,
Seo, H., Gali, A., Galli, G. and Awschalom, D. Quantum guidelines for solid-state spin defects. Nature Reviews Materials. 6, 906-925 (2021).
[23] See Supplemental Information.
[24] Ponomaryov, A., Schulze, E., Wosnitza, J., LampenKelley, P., Banerjee, A., Yan, J., Bridges, C., Mandrus,
D., Nagler, S., Kolezhuk, A. and Zvyagin, S. Unconventional spin dynamics in the honeycomb-lattice material α-RuCl3 : High-field electron spin resonance studies.
Physical Review B. 96, 241107 (2017).
[25] Ponomaryov, A., Zviagina, L., Wosnitza, J., LampenKelley, P., Banerjee, A., Yan, J., Bridges, C., Mandrus,
D., Nagler, S. and Zvyagin, S. Nature of magnetic excitations in the high-field phase of α-RuCl3 . Physical Review
Letters. 125, 037202 (2020).
[26] Wellm, C., Zeisner, J., Alfonsov, A., Wolter, A., Roslova,
M., Isaeva, A., Doert, T., Vojta, M., Büchner, B. and
Kataev, V. Signatures of low-energy fractionalized excitations in α-RuCl3 from field-dependent microwave absorption. Physical Review B. 98, 184408 (2018).
[27] Balz, C., Lampen-Kelley, P., Banerjee, A., Yan, J., Lu,

Z., Hu, X., Yadav, S., Takano, Y., Liu, Y., Tennant, D.,
Lumsden, M., Mandrus, D. and Nagler, S. Finite field
regime for a quantum spin liquid in α-RuCl3 . Physical
Review B. 100, 060405 (2019).
[28] Zhao, X., Wu, J., Zhao, Z., He, Z., Song, J., Zhao, J., Liu,
X., Sun, X. and Li, X. Heat switch effect in an antiferromagnetic insulator Co3 V2 O8 . Applied Physics Letters.
108, 242405 (2016).
[29] Hong, X., Gillig, M., Yao, W., Janssen, L., Kocsis, V.,
Gass, S., Li, Y., Wolter, A., Büchner, B. and Hess, C.
Phonon thermal transport shaped by strong spin-phonon
scattering in a Kitaev material Na2 Co2 TeO6 . Npj Quantum Materials. 9, 18 (2024).
[30] Hentrich, R., Wolter, A., Zotos, X., Brenig, W., Nowak,
D., Isaeva, A., Doert, T., Banerjee, A., LampenKelley, P., Mandrus, D., Nagler, S., Sears, J., Kim, Y.,
Büchner, B. and Hess, C. Unusual Phonon Heat Transport in α-RuCl3 : Strong Spin-Phonon Scattering and
Field-Induced Spin Gap. Phys. Rev. Lett.. 120, 117204
(2018,3).
[31] Li, Q., Zhao, Z., Fan, C., Zhang, F., Zhou, H., Zhao, X.
and Sun, X. Phonon-glass-like behavior of magnetic origin in single-crystal Tb2 Ti2 O7 . Phys. Rev. B. 87, 214408
(2013,6).
[32] Wang, X., Fan, C., Zhao, Z., Tao, W., Liu, X., Ke, W.,
Zhao, X. and Sun, X. Large magnetothermal conductivity of HoMnO3 single crystals and its relation to the
magnetic-field-induced transitions of magnetic structure.
Phys. Rev. B. 82, 094405 (2010,9).
[33] Berggold, K., Baier, J., Meier, D., Mydosh, J., Lorenz,
T., Hemberger, J., Balbashov, A., Aliouane, N. and
Argyriou, D. Anomalous thermal expansion and strong
damping of the thermal conductivity of NdMnO3 and
TbMnO3 due to 4f crystal-field excitations. Physical Review B—Condensed Matter And Materials Physics. 76,
094418 (2007).
[34] Pocs, C., Leahy, I., Zheng, H., Cao, G., Choi, E., Do, S.,
Choi, K., Normand, B. and Lee, M. Giant thermal magnetoconductivity in CrCl3 and a general model for spinphonon scattering. Phys. Rev. Res.. 2, 013059 (2020,1).
