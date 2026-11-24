Source: https://arxiv.org/abs/2601.22802
PDF sha256: ca3a2efd1fcec98f174b42972b0cbcd03d140e8d34db61be89ee440775307761
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of chen_2026_long_distance_spin_transport_frustrated_hyperkagome_gd3ga5o12.pdf

Transcription of `chen_2026_long_distance_spin_transport_frustrated_hyperkagome_gd3ga5o12.pdf` in this directory, 24 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-24 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Long-distance spin transport in frustrated hyperkagome magnet Gd3Ga5O12
Di Chen1, Bingcheng Luo2, Lei Xu3, Zian Xia4, Linhao Jia2,1, Shaomian Qi2, Congkuan Tian2,1,
Kangyao Chen2, Hang Cui2, Guangyi Chen2, Shili Yan1, Miaoling Huang1, Jian Cui1, Ya Feng1,
Zhentao Wang3,5*, Jiang Xiao4,6*, Jianhua Zhang7,8, Ryuichi Shindou2, X.C. Xie2,6,9, Jian-Hao
Chen2,1,9,10*
1

Beijing Academy of Quantum Information Sciences; Beijing, 100193, China.

2

International Center of Quantum Materials, School of Physics, Peking University; Beijing, 100871,
China.
3

School of Physics, Zhejiang University; Hangzhou, 310058, China.

4

Department of Physics and State Key Laboratory of Surface Physics, Fudan University; Shanghai,
200433, China.
5

Center for Correlated Matter, Zhejiang University; Hangzhou, 310058, China.

6

Institute for Nanoelectronic Devices and Quantum Computing, Fudan University; Shanghai, 200433,
China.
7

N.O.D topia Biotechnology Co., Ltd.; Guangzhou, 510000, China

8

Simpcare Biotechnology Co., Ltd.; Guangzhou, 510000, China

9

Hefei National Laboratory; Hefei, 230088, China.

10

Key Laboratory for the Physics and Chemistry of Nanodevices, Peking University; Beijing, 100871,
China.
*Corresponding authors: Zhentao Wang (ztwang@zju.edu.cn); Jiang Xiao (xiaojiang@fudan.edu.cn);
Jian-Hao Chen (chenjianhao@pku.edu.cn)

Abstract
Transport of spin angular momentum over large distance has been a long sought-after goal in
the field of spintronics. While the majority of the research effort has been devoted to the spin
transport properties of magnetically ordered materials, spin transport in magnetically frustrated
materials has received little attention. Here, we report an anomalous state in frustrated
hyperkagome magnetic insulator Gd3Ga5O12, where spin angular momenta can be transported over
a long distance of 480μm, far exceeding the transport distance of any diffusive spin current in
magnetically ordered materials, to the best of our knowledge. Monte Carlo simulations reveal
significant spin fluctuations, spin-spin correlations and an absence of conventional magnons in
such anomalous state; while the response of the anomalous state to perturbation is found to be akin
to an overdamped forced oscillator. We find close relation of such state to the correlated “director”
state in the material. Our result provides an effective electrical technique to characterize spin-spin
correlations and frustrations; it also unveils the potential of frustrated magnets as powerful channel
materials for spin transport.
1

## PDF page 2

Introduction
The transport of spin angular momenta in solids constitutes the heart of spintronics technology,
a branch of electronics that utilizes the spin degree of freedom for information processing 1, 2, 3. In
particular, magnons in insulating ferromagnets and antiferromagnets have been identified as an
efficient carrier for spin current 4, 5, 6, 7, 8, opening a new field of magnon-based spintronics. More
recently, spin transport was observed in paramagnetic insulators 9, 10, 11 and antiferromagnets above
the Néel temperature 12, 13, 14, suggesting that long-range magnetic order may not be a prerequisite
for spin transport. Unlike ordinary magnetically ordered materials, frustrated magnets, an
important class of magnetic materials where long-range magnetic orders could be prevented due
to geometric 15 or exchange 16 frustrations, are largely unexplored in the thriving field of
spintronics 17, 18.
Frustrated systems without magnetic order do not have well-defined magnons, but instead
have intrinsic spin fluctuations that support novel magnetic states, such as spin ice, spin liquid,
and other exotic quantum states (as schematically illustrated in Fig. 1a) 19. Gd3Ga5O12 (GGG) is a
typical example of frustrated magnetic insulators. High quality single crystal GGG is widely
available since it is a common substrate material 20 for growing epitaxial garnet thin films like
yttrium iron garnet (YIG). At room temperature, GGG behaves as an ordinary paramagnetic
insulator and does not affect either the charge or spin transport in any magnetically ordered
materials that are grown on it. At low temperatures, GGG exhibits characteristics of a
geometrically frustrated antiferromagnetic insulator, which presents strong spin fluctuations
without static order down to 25mK [21]. It exhibits complex magnetic phases at low temperatures,
where different candidates including spin glass 22, spin liquid 23 and a “hidden order” of ten-spinloop director state 24, 25 are proposed. As shown in Fig. 1b, this “hidden order” state is composed
of loops of ten individually fluctuating magnetic Gd3+ ions, where a long-range “director state”
with no overall magnetic moment can be defined by the remanent anti-ferromagnetic coupling
among the disordered spins 24. Such state does not break any crystal structural symmetry or time
reversal symmetry, yet its correlations could exist to moderate magnetic fields 26, 27.
In this study, we experimentally investigate the phase diagrams of the nonlocal second
harmonic spin transport (SHST) signal in GGG as a function of injection current, magnetic field
and temperature. In addition to a normal SHST signal similar to the magnon transport signal in
magnetically ordered systems, an anomalous spin signal is detected below 5K and for magnetic
2

## PDF page 3

field ≲ 9T, where the spin fluctuation and spin-spin correlation are strong 24, 28. This anomalous
spin transport state is characterized by a frustration induced correlation process and exhibits a long
spin transport distance of up to 480μm, far exceeding the transport distance of any diffusive spin
current in magnetically ordered materials 5, 6. Monte Carlo simulations reveal significant spin
fluctuation and spin-spin correlation under conditions when long-distance spin transport emerges
experimentally, and the low energy spin excitations response to electrical perturbation in a way
that is akin to an overdamped forced oscillator. Our experimental result unveils the potential of
frustrated magnets as promising candidates for spin transport.

Results
Fig. 1c displays a simplified atomic schematic of the hyperkagome structure of GGG, where
only the magnetic Gd3+ ions are shown for clarity. These Gd3+ ions form two interpenetrating
lattices of corner-sharing triangles 29, providing the basic ingredient of geometric frustration. The
absence of long-range magnetic order down to a temperature of 2K [21], and a Curie-Weiss
temperature of -2.05K [10, 30] of the GGG <111> sample is experimentally verified by magnetic
moment versus temperature measurement (Supplementary Information Fig. S1a). The fielddependent in-plane magnetization gives a low-temperature saturation magnetization of ~7μB per
Gd3+ (Supplementary Information Fig. S1b), in agreement with previous studies 11. A comparison
of the magnetization data at T ≤ 2K to the Brillouin function for non-interacting and isotropic
S=7/2 spins reveals a deviation (Supplementary Information Fig. S1c). This deviation from pure
paramagnetic behavior becomes more pronounced at lower temperatures, suggesting the
dominance of spin-spin frustration and correlations in GGG [31].
Nonlocal spin transport phase diagrams
Fig. 1d presents a schematic diagram of the experimental setup used in this study. The spin
transport device comprises of two platinum (Pt) wires, an injector, and a detector, which are
fabricated on a GGG <111> channel. An AC current 𝐼𝑖𝑛 = 𝐼𝑖𝑛,0 𝑠𝑖𝑛𝜔𝑡 with frequency ω is applied
through the injector, creating thermal spin excitations in the channel. Here 𝐼𝑖𝑛,0 is the magnitude
of the AC injection current. The nonlocal second harmonic inverse spin Hall voltage 𝑉2𝜔 is
measured by lock-in amplifiers from the detector 5, 32. To comply with the orthogonal rule of the
inverse spin Hall effect 32, an in-plane magnetic field with varying angle θ is applied to produce
an in-plane M component, and a 𝑐𝑜𝑠𝜃 dependence of 𝑉2𝜔 can be detected as shown in the inset of
3

## PDF page 4

Fig. 1d. GGG has an energy bandgap of approximately 5.66 eV [33], which excludes any
contribution of conduction electrons in the spin signal. We also exclude the current leakage effect
by measuring the resistance between two Pt electrodes in the GGG devices in Supplementary
𝑋
Information Fig. S2. When measuring the AC 𝑉2𝜔 signal, the in-phase component 𝑉2𝜔
=
𝑌
|𝑉2𝜔 |cos𝜙 and the out-of-phase component 𝑉2𝜔
= |𝑉2𝜔 |sin𝜙 are obtained from the lock-in

amplifier, where 𝜙 is the relative phase angle of this AC signal to the injection AC current. The
sign of the SHST signal 𝑉2𝜔 is defined by the sign of sin𝜙, i.e., 𝑉2𝜔 = 𝑠𝑖𝑔𝑛(𝑠𝑖𝑛𝜙)|𝑉2𝜔 |.
𝑋
𝑌
Figs. 2a and 2b show the mapping of 𝑉2𝜔
and 𝑉2𝜔
measured at T = 2K as a function of

magnetic field B and injection current 𝐼𝑖𝑛 , respectively. The magnetic field ranges from 0T to 14T,
and the injection current ranges from 0μA to 132μA. Here, the detector is positioned 2μm away
from the injector and the in-plane magnetic field B is directed at an angle of θ = 0, where θ
represents the angle between B and the perpendicular direction of the detector Pt electrode (as
𝑋
𝑌
depicted in Fig. 1d). For SHST signals in conventional magnetic systems, 𝑉2𝜔
= 0 and 𝑉2𝜔
> 0,
𝜋

corresponding to 𝑉2𝜔 > 0 and 𝜙 = 2 . This value of 𝜙 is due to the second harmonic nature of the
𝐼

2

𝜋

signal, i.e. 𝑉2𝜔 ∝ −(𝐼𝑖𝑛,0 𝑠𝑖𝑛𝜔𝑡)2 ∝ 𝑖𝑛,0
sin⁡(2𝜔𝑡 + 𝜙), where 𝜙 = 2 . The negative sign in the
2
above formula comes from the convention in the field to present thermal magnon signals as
positive signals at θ = 0 [5].
𝑋
𝑌
Thus, the region in Figs. 2a and 2b where 𝑉2𝜔
= 0 and 𝑉2𝜔
> 0 represents the normal state of

GGG, of which the SHST response is similar to conventional magnetic systems; while the region
𝑋
𝑌
with 𝑉2𝜔
≠ 0 or 𝑉2𝜔
< 0 marked the emergence of an anomalous state in the spin transport of the
𝑌
material. Since the normal and anomalous 𝑉2𝜔
are of opposite signs and could compete with each
𝑋
other while they coexist, the anomalous state of GGG is best characterized by a non-zero 𝑉2𝜔
.

Control experiments with Cu electrodes are shown in Supplementary Information Fig. S3, which
𝑋
exclude any possible reactive components contributed to 𝑉2𝜔
. We define the anomalous phase as

the region in Fig. 2a below the gray dashed line. This line marks a cut-off value of 10% of the
𝑋
𝑋
maximum 𝑉2𝜔
signal. Note that other definitions of cut-off value of non-zero 𝑉2𝜔
yield similar

results.
𝑌
Fig. 2b shows 𝑉2𝜔
versus B and Iin with the same gray dashed line as in Fig. 2a. Above the
𝑋
𝑌
gray line, 𝑉2𝜔
= 0 and 𝑉2𝜔
> 0, representing the normal state of GGG. Below the gray line, there
𝑋
𝑌
𝑋
𝑌
are two areas: one with 𝑉2𝜔
≠ 0 and 𝑉2𝜔
> 0 at smaller Iin; the other with 𝑉2𝜔
≠ 0 and 𝑉2𝜔
<0

4

## PDF page 5

at larger Iin. These two areas belong to the same region where the anomalous state coexists with
the normal state with different relative strengths. Equivalently, one can also plot 𝑉2𝜔 versus B and
Iin which can be found in Supplementary Information Fig. S4a. The magnetic field angle 𝜃
dependent 𝑉2𝜔 and 𝜙 of the typical normal and anomalous states can be found in Supplementary
Information Fig. S4b-e, highlighting the stark differences between the two states. Data from
another GGG crystal can be found in Supplementary Information Fig. S5, further verifying the
existence of the anomalous state. Note the signal 𝑉2𝜔 vanishes at 𝜃 = 90° and 270° in all the range
of magnetic field we studied (Supplemental Figure S5-1), which is consistent with the inverse spin
Hall effect rather than spurious reactive components of the circuit.
𝑋
𝑌
In Figs. 2c and 2d, 𝑉2𝜔
and 𝑉2𝜔
versus B with the magnetic field angle 𝜃 = 0 and T = 2K are

plotted for GGG and MnPS3, respectively. MnPS3 is a conventional magnetic insulator with
antiferromagnetic order and it has a normal SHST signal resembling that of YIG [34]. As shown
𝑋
in Fig. 2c, 𝑉2𝜔
> 0 in GGG as soon as B > 0; it increases with increasing B, reaching a maximum,
𝑋
then decreases and finally diminishes above ~9T. In contrast, 𝑉2𝜔
in MnPS3 remains zero from 0T
𝑌
𝑌
to up to 14T, as expected for conventional magnets 34. For the 𝑉2𝜔
component, 𝑉2𝜔
< 0 in GGG

as soon as B > 0; it decreases with increasing B, reaching a minimum, then increases and reverses
𝑌
sign to become positive above ~9T. In comparison, 𝑉2𝜔
in MnPS3 is positive, increases with

increasing magnetic field, then decreases slightly, but remains positive up to 14T as expected. One
𝑋,𝑌
can find that the 𝑉2𝜔
vs. B of GGG from 9T to 14T is similar to that of MnPS3 from 0T to 14T
𝑋,𝑌
(normal state), while the 𝑉2𝜔
vs. B curves of GGG below 9T are completely different from the
𝑌
normal behavior, indicating an anomalous state in the material. Note that a negative 𝑉2𝜔
in GGG

means that the spin transport direction is opposite to those in conventional magnetic materials
when other excitation conditions are the same, highlighting the prominent feature of the anomalous
state.
𝑋
𝑌
Figs. 2e-2f exhibit 𝑉2𝜔
and 𝑉2𝜔
versus 𝐼𝑖𝑛 with 𝜃 = 0 and T = 2K, for GGG and MnPS3,
𝑋
respectively. For GGG, finite 𝑉2𝜔
emerges with minimal 𝐼𝑖𝑛 and monotonically increases with

increasing 𝐼𝑖𝑛 , indicating that the anomalous state is present irrespective of the injection current;
𝑌
𝑉2𝜔
is positive only in the low current range, then quickly decreases to zero and changes sign,

finally saturating at large 𝐼𝑖𝑛 , exemplifying the competition of the normal and anomalous states in
𝑌
𝑋
𝑌
the 𝑉2𝜔
component. In contrast, for MnPS3, 𝑉2𝜔
is always zero, and 𝑉2𝜔
> 0 up to a large

5

## PDF page 6

injection current. The deviation from the quadratic relationship at larger 𝐼𝑖𝑛 could be attributed to
non-linear spin Seebeck effect 34.
The next intriguing question is how this anomalous state behaves at different temperature. Fig.
𝑋
𝑌
3a and Fig. 3b show the 2D plots of 𝑉2𝜔
and 𝑉2𝜔
vs. T and B with 𝜃 = 0, 𝐼𝑖𝑛 = 100⁡𝜇𝐴 and a

channel length of 1𝜇𝑚 (see Supplementary Information Fig. S7 for data with different channel
lengths). While the normal SHST signal (red part in Fig. 3b) persists up to 14K, the anomalous
SHST signal (blue parts in Figs. 3a-b) vanishes above ~5 K and above ~9 T. Note that the nonzero
𝑋
𝑌
𝑉2𝜔
region in Fig. 3a does not exactly coincide with the negative 𝑉2𝜔
region in Fig. 3b, because of
𝑌
competition between the negative (anomalous) signal and the positive (normal) signal in the 𝑉2𝜔
𝑋
𝑌
channel, similar to the situation in Fig. 2b. To demonstrate the anomaly, 𝑉2𝜔
and 𝑉2𝜔
versus T for

GGG at B = 3T are shown in Fig. 3c; similar data taken from MnPS3 are shown in Fig. 3d. For
𝑋
𝑌
MnPS3, 𝑉2𝜔
is strictly zero in the whole temperature range; positive 𝑉2𝜔
emerges with decreasing

temperature below 20K and continue to increase 34, which is expected for conventional SHST
𝑋
signal. For GGG, however, finite 𝑉2𝜔
emerges at about 7K and continue to increase with
𝑌
decreasing temperature; positive 𝑉2𝜔
emerges at about 12K and initially increases with decreasing
𝑌
temperature (similar to MnPS3); a strong down turn in 𝑉2𝜔
appears at low temperature, creating a

maximum in the signal and causing the signal to reverse sign at 3K. The above data clearly
indicates that anomalous spin transport state dominates at lower magnetic fields and at lower
temperatures.
Correlated spin dynamics in the anomalous state
From the previous section, two distinct spin transport states were found in GGG, i.e., one
𝑌
𝑋
normal state and one anomalous state. The normal state is characterized by: 1) 𝑉2𝜔
> 0 and 𝑉2𝜔
=

0; 2) signals persist up to over 10K and up to 14T. The GGG channel right below the injector is
𝜋

lightly perturbed thermally, the temperature oscillation 𝑇(𝑡) = 𝑇0 + ∆𝑇𝑠𝑖𝑛(2𝜔𝑡 + 2 ) changes the
chemical potential of the magnons below the injector. A chemical potential difference ∆𝜇 is
established in the spin transport channel, and a spin current 𝑗𝑠 = 𝐺∆𝜇(𝑇) is generated, where 𝐺 is
the magnon conductance. For the normal paramagnetic phase above 5K, the magnetic moments
are not entangled with each other and are free to relax, so that the system responds effectively
𝑋
instantaneously, producing no measurable 𝑉2𝜔
signal. In this regime, since the nearest-neighbor

exchange interaction in GGG is small with J ~ 0.1 K [35], dipolar interactions become significant
6

## PDF page 7

and could support spin-wave-like excitations under magnetic field, attributing to the normal signal
in GGG [11].
𝑌
In contrast, the anomalous state manifests itself with distinctive SHST signals: 1) 𝑉2𝜔
<0
𝑋
and 𝑉2𝜔
≠ 0; 2) signals emerge below 5K and below a magnetic field of ~9T. The emergence of

this anomalous state at low temperature points its origin to the geometric frustrations in GGG, and
exclude the possibility of phonon-carried spin current which should sustain to high temperatures
36, 37

. Similarly, the suppression of the anomalous state at and above saturating magnetic fields is

natural as geometric frustrations become irrelevant in the presence of strong Zeeman energy 11, 38.
What’s more, in conventional magnets, thermal injection weakens the magnetization near the
injector, resulting in the transport of spin angular momenta in opposite direction than the
expectation for an electrically injected spin current. Since so far thermal magnon induced spin
transport is studied almost solely in conventional magnets, a convention has been established that
𝑌
such opposite direction of spin transport would provide 𝑉2𝜔
> 0 [5]. Note that careful

consideration has to be given for the thin film systems considering the accumulation of spin
excitations at the boundaries 39, but for the bulk system studied here the presented sign convention
is applicable. For the anomalous state in our work, a moderate magnetic field could not align the
frustrated magnetic moments and still results complicated spin configurations with strong spinspin correlations. Thermal perturbation in frustrated magnets will weaken the intrinsic frustration
and spin-spin correlation effects, resulting in more magnetization along the magnetic field
direction. Thus, the anomalous state may transport angular momenta in the same direction as the
𝑌
applied field, resulting in 𝑉2𝜔
< 0 according to the above-mentioned convention, suggesting a

crucial role of spin fluctuations. Indeed, the only work in the literature that is related to correlated
𝑌
spin transport (one-dimensional spinon local spin Seebeck effect), also shows 𝑉2𝜔
< 0 [40].
𝑋
The finite 𝑉2𝜔
in the anomalous state indicates an additional phase delay ∆𝜙 in 𝑉2𝜔 ∝ 𝑗𝑠 ∝
𝜋

sin⁡(2𝜔𝑡 + 2 + ∆𝜙), which is related to a retardation in magnetic relaxation induced by spin-spin
correlations. In a correlated spin system, flipping one spin requires flipping many other spins in
order for the system to go from one ground state to another, resulting in the phase delay analogous
to the imaginary part of AC susceptibility 41. As shown in Fig. 4c, Monte Carlo simulation of
magnetic susceptibility also indicates strong spin fluctuations as well as spin-spin correlations
𝑋
below 5K and near the saturation field, which corresponds well to the 𝑉2𝜔
distribution shown in
𝑋
𝑌
Fig. 3a. Fig. 4a shows 𝑉2𝜔
and 𝑉2𝜔
versus injection current frequency 𝜔 with in-plane magnetic

7

## PDF page 8

field at angle 𝜃 = 0 and magnitude B = 3T at temperatures in the range of 1.8 K - 4 K. A maximum
𝑋
𝑋
in 𝑉2𝜔
appears in the 𝑉2𝜔
vs. 𝜔 curve at low temperatures, representing a quasi-resonance

condition of the frustrated and correlated spin system under external excitation. Moreover, such
𝑋
maximum in 𝑉2𝜔
moves from 37Hz to 60Hz and declines in magnitude with increasing

temperature and eventually disappears at 4K, which is in line with the fact that increasing
temperature weakens the effects of spin correlations, resulting in an increasing quasi-resonance
frequency and an overall decreasing signal from spin-spin correlations. Indeed, geometric
frustrations in GGG lead to macroscopically multi-degenerate spin configurations with mixed total
magnetization 27. One effect of the thermal injection is changing the spin configurations; with spinspin correlations, the spin configurations (thus magnon chemical potential) could not always keep
up with the change of the temperature and is delayed by ∆𝜙, where the phase delay is relevant to
𝜔. Such a response of the chemical potential to the temperature modulation is mathematically
equivalent to an overdamped forced oscillator:
𝑥̈ (𝑡) + 𝛽𝜔0 𝑥̇ (𝑡) + 𝜔0 2 𝑥(𝑡) = 𝛿𝑇 0 𝑒 −𝑖𝜔𝑡 ,
where the chemical potential difference ∆𝜇 is related to the speed of response 𝑥̇ as ∆𝜇 ∝ 𝑥̇ /𝜔0 ,
and the eigen frequency 𝜔0 (𝑇, 𝐵) is related to the evolution of spin configuration depending on
both temperature and the external magnetic field. Then the response function in the frequency
domain can be written as:
𝑖𝜔/𝜔

0
𝜒(𝜔) = 𝜔 2 −𝜔2+𝑖𝛽𝜔
.
𝜔
0

0

𝑌
𝑋
Here 𝜒(𝜔) ∝ ∆𝜇 , and the real and imaginary parts of 𝜒(𝜔) are related to 𝑉2𝜔
and 𝑉2𝜔
,
𝛽𝜔 𝜔

0
respectively, with a corresponding phase delay 𝜙 = 𝑎𝑟𝑐𝑐𝑜𝑡 𝜔 2 −𝜔
2 . The lower the temperature
0

and the stronger the correlation would result in lower magnetic relaxation eigen frequency 𝜔0 , as
the magnetic moments are increasingly affected by the frustrations and behave cooperatively in
𝑌
𝑋
clusters 25. Fig. 4b displays the simulated 𝑉2𝜔
and 𝑉2𝜔
with different 𝜔0 , which agrees well with

the experimental results shown in Fig. 4a. This indicates that the overdamped forced oscillator
model captures the main physics of the correlated spin response in GGG under excitation.
Long-distance spin transport in GGG
One particularly intriguing question is how spin-spin fluctuation and correlation in frustrated
magnetic insulators affect the spin transport properties of such materials, which has never been
8

## PDF page 9

probed experimentally before. Fig. 5a plots the distance d dependent |𝑉2𝜔 | in GGG at one
representative point in the anomalous state (𝑇 = 2K, 𝐵 = 3T, 𝐼𝑖𝑛 = 200𝜇𝐴) and two representative
points in the normal state (strong magnetic field: 𝑇 = 2K, 𝐵 = 14T, 𝐼𝑖𝑛 = 100𝜇𝐴 and high
temperature: 𝑇 = 5K, 𝐵 = 3T, 𝐼𝑖𝑛 = 100𝜇𝐴). Fig. 5a also plots a typical distance dependent |𝑉2𝜔 |
in MnPS3, which is a conventional magnetically ordered insulator. The inset in Fig. 5a is a zoomin plot of all the data except for the anomalous state. It can be seen that the normal state GGG has
a spin diffusion length of several micrometers. For example, at 𝑇 = 5K, 𝐵 = 3T, 𝐼𝑖𝑛 = 100𝜇𝐴, we
extract a spin diffusion length 𝜆 = 1.7087 ± 0.235⁡𝜇𝑚 via a 2D diffusion model (details in
Methods and Supplementary Information Fig. S9), which is comparable to the previous study 11 in
GGG at 𝑇 = 5K, 𝐵 = 3.5T with 𝜆 = 1.8 ± 0.2𝜇𝑚 obtained via the same model. However, the
anomalous SHST signal in GGG decays considerably slower and remains finite up to a distance
of 480𝜇𝑚, two orders of magnitude larger than that of the normal state GGG and MnPS3. An
exceptionally long spin diffusion length 𝜆 = 209.19 ± 22.6𝜇𝑚 is extracted from the 2D diffusion
model (see Supplementary Information Fig. S10).
With the analysis in the previous section, frustration induced novel spin states could be the
cause of the anomalous signal in GGG. Since our experimental temperature is well above the
temperatures for spin glass 22 and spin liquid 23 transitions in GGG, the most likely origin of the
anomalous state should be rooted in the hidden-order state reported in GGG and its isostructural
crystal GAG (Gd3Al5O12) 24, 28. This hidden-order composed of ten Gd3+ ions arranged in a ring
shape, which forms a nematic director state under the antiferromagnetic interactions and local x-y
anisotropic interactions 24, 25. Neutron scattering revealed the onset of director correlations in
GGG/GAG below 5K [28, 42], which agrees with the onset of the anomalous spin transport in our
experiment. More importantly, the ten-spin directors state could give rise to long-range
correlations as shown in Fig. 1b, i.e., the multipoles (indicated by orange double-headed arrows)
located at the center of the ten Gd3+ ions rings are highly correlated, which could mediate longdistance spin transport. It has been theoretically and experimentally shown that the ten-spin
directors state correlations still play a role in the material under a moderate magnetic field 26, 43.
Fig. 4d shows the magnon life time of the highest band at Γ point as a function of magnetic field
obtained from our Monte Carlo simulation. The magnon life time decreases with decreasing field
and a crossover happened from the paramagnetic state to the frustrated state with spin-spin
correlations (details in Methods and Supplementary Information Fig. S13-14). Note that non-spin
9

## PDF page 10

wave excitations with lower excitation energy could exist at lower field, since multi-degenerate
local minima are found in the classical spin configurations 27. Such low energy excitations with
correlations might be the cause of the long-distance spin transport in GGG. Interestingly, AC
susceptibility measurements on GGG have shown two distinct thermally activated processes, one
related to single spin reversal and the other to the fluctuations of ten-ion loops 28, which may
correspond to the normal and anomalous spin transport states we observed.

Discussion
Lastly, we emphasize in Fig. 5b the exceptional spin transport capability in the anomalous
state in GGG, as compared to thermally injected spin current in other magnetic materials 5, 6, 44, 45
with similar injection power (see Supplementary Information Fig. S16). These materials include
antiferromagnets and ferrimagnets such as 𝛼-Fe2O3 [6] as well as YIG [5]. It is interesting to see
that frustrated magnet GGG without magnetic order can transport spin angular momenta to much
greater distance than any magnetically ordered materials. Actually, long-range spin transport in
disordered magnetic systems has been theoretically studied 46, 47, 48, and the ingredient of
antiferromagnetic interactions and local x-y anisotropic interactions has led to the prediction of
superfluid transport in frustrated magnets 49. Experimentally, we found the signal decaying at a
slower rate than the fitting curves as shown in Fig. 5a and in Supplementary Information Fig. S10,
pointing to a different dissipation mechanism from conventional spin diffusion in anomalous state
GGG, and revealing the great potential for the innovative mechanism of spin transport through
spin fluctuations and correlations.
In conclusion, we experimentally studied the nonlocal spin transport in frustrated
hyperkagome magnetic insulator GGG where magnetic order is prevented by geometric
frustrations. We report an anomalous spin transport state in GGG at low temperature, with ultralong-distance spin transport of over 480μm. Such low-dissipation transport distance is
significantly longer than that in the normal state GGG and those achieved in any known
magnetically ordered materials. Theoretical simulations indicate close connections between the
anomalous spin transport state with the spin fluctuation and spin-spin correlation in GGG. Our
result provides a valuable tool for studying spin fluctuations in frustrated magnets, elucidates the
immense potential of frustrated magnets as promising materials for spin transport channels, and
potentially enables novel spintronics devices.

10

## PDF page 11

Methods
Device fabrication and magnetization characterization
Gd3Ga5O12 <111> single crystals slabs with thickness of 500μm were commercially
purchased from Hefei Kejing Materials Technology Co., Ltd. and CRYSTAL GmbH. The injector
and detector electrodes in the nonlocal spin transport devices are fabricated with standard electronbeam lithography, platinum deposition and lift-off processes. Platinum is deposited in a magnetron
sputtering system, and the length of the electrodes is 100μm, the width of the wires is ~200nm
with a thickness of 10nm. Afterwards, 5nm of titanium and 50nm of gold are patterned to contact
the platinum wires. Distances between the platinum wires range from 1μm to 480μm center-tocenter. Data from nonlocal spin transport GGG devices fabricated on five GGG slabs (device#1 –
device#5) were presented. Data shown in Fig. 2a-b, Fig. 3a-b were obtained from device#1; data
shown in Fig. 2c, 2d, 3e and the normal signal taken at 2K shown in Fig. 5a were obtained from
device#2; the normal signal taken at 5K shown in Fig. 5a were obtained from device#3; data shown
in Fig. 4a were obtained from device #4; the anomalous signal shown in Fig. 5a were obtained
from device#5. Others are stated in the Supplementary Information. For magnetization
measurements, the GGG slab cut into 2.5mm long and 2mm wide was measured using SQUID
magnetometry in a temperature range from 0.4 K to 300 K under external magnetic fields up to
7T.
Nonlocal spin transport measurement
The spin transport measurement of GGG is done in PPMS and Oxford TeslatronPT with lowfrequency lock-in amplifier technique. The injection AC current in the range from 0𝜇𝐴 to 500𝜇𝐴
is provided by lock-in amplifier (Stanford Research SR830). Except for frequency dependent
measurements (0.77-200.77Hz), the injection current frequency is 17.77Hz for all the experiments.
Also, lock-in amplifiers (NF LI5650 and Stanford Research SR830) are used to probe the nonlocal
voltages amplified by low noise voltage preamplifiers (NF LI75A). In lock-in AC measurements,
𝑅
four components of the 𝑉2𝜔 can be obtained, including the amplitude R component 𝑉2𝜔
= |𝑉2𝜔 |,
𝑋
𝑅
𝑌
the relative phase angle 𝜙 , the X component 𝑉2𝜔
= 𝑉2𝜔
cos𝜙 and the Y component 𝑉2𝜔
=
𝑅
𝑉2𝜔
sin𝜙. Here R and 𝜙 provide a complete description of 𝑉2𝜔 ; similarly, X and Y components
𝑅
provide a complete description of 𝑉2𝜔 . Since the amplitude 𝑉2𝜔
is always positive, we combine
𝑅
𝑅
the sign of sin𝜙 and 𝑉2𝜔
, and define the 𝑉2𝜔 = 𝑠𝑖𝑔𝑛(𝑠𝑖𝑛𝜙) · 𝑉2𝜔
= 𝑠𝑖𝑔𝑛(𝑠𝑖𝑛𝜙)|𝑉2𝜔 | to showcase

the 𝑐𝑜𝑠𝜃 dependence of the SHST signal. All 𝜃 dependent 𝑉2𝜔 data shown in the paper are
11

## PDF page 12

original data without subtracting any offset signal. The temperature of the measurement ranges
from 2K to 300K. The applied magnetic field is parallel to our sample plane and the maximum
field is 14T.
Nonlocal SHST signal 𝑽𝟐𝝎 vs. B and Iin
Supplementary Information Fig. S4a displays the corresponding SHST signal 𝑉2𝜔 =
𝑠𝑖𝑔𝑛(𝑠𝑖𝑛𝜙)|𝑉2𝜔 | of which shown in Figs. 2a-b in the main text. Two regions can be observed in
Supplementary Information Fig. S4a, one with positive 𝑉2𝜔 signal and the other with negative 𝑉2𝜔
signal. These two types of signals are further illustrated in Supplementary Information Figs. S4bc and Supplementary Information Figs. S4d-e, respectively. Supplementary Information Figs. S4b
and S4c plot 𝑉2𝜔 and the corresponding phase 𝜙 as a function of magnetic field angle 𝜃, for which
the data was collected with an AC injection current with root mean square value of 𝐼𝑖𝑛 = 100μA
and at B = 14T. Due to the orthogonal rule of ISHE at the detector, 𝑉2𝜔 has a 𝑐𝑜𝑠𝜃 dependence
with a positive value at 𝜃 = 0. The corresponding phases 𝜙 are ±90°. The features shown in
Supplementary Information Figs. S4b-c are consistent with thermally generated magnons in
magnetically order materials 5. Whereas for B = 3T with the same injection current, 𝑉2𝜔 has a 𝑐𝑜𝑠𝜃
dependence with an opposite sign, and the corresponding phases 𝜙 are around -50°and 130°,
deviating from ±90°, as shown in Supplementary Information Figs. S4d-e. Such deviation of 𝜙
𝑋
from ±90°indicates a nonzero 𝑉2𝜔
, which is one major characteristics of the anomalous spin

transport in GGG.
𝑽𝑿𝟐𝝎 and 𝑽𝒀𝟐𝝎 vs. T and B at different channel lengths
In order to understand how spin angular momenta are transported in GGG, we studied the
𝑋
𝑌
temperature and magnetic field dependence of the nonlocal SHST signal 𝑉2𝜔
and 𝑉2𝜔
at different
𝑋
𝑌
injector-detector distances. Supplementary Information Figs. S7a-b replot the 𝑉2𝜔
and 𝑉2𝜔
for

𝑑 = 1⁡𝜇𝑚 in Figs. 3a-b in the main text, and the inset shows the temperature dependent evolution
𝑋
𝑌
of 𝑉2𝜔
and 𝑉2𝜔
under magnetic field of 2.1 T. Similar to Supplementary Information Figs. S7a-b,

Supplementary Information Figs. S7c-d and Supplementary Information Figs. 7e-f are showing
𝑋
𝑌
the phase diagrams of 𝑉2𝜔
and 𝑉2𝜔
vs. T and B for channel length 𝑑 = 2⁡𝜇𝑚 and 𝑑 = 4⁡𝜇𝑚,

respectively. Comparing these phase diagrams of different distances, we find that the normal SHST
signal (red parts in Supplementary Information Figs. S7b, d, e) disappears quickly when the
12

## PDF page 13

channel length becomes longer than 2μm. On the contrary, the anomalous SHST signal (blue parts
in Supplementary Information Figs. S7a-f) decreases much slower, which means that spin angular
momentum can transport to far greater distance in GGG in the anomalous state.
Monte Carlo simulations
We consider the following Hamiltonian:
𝑺 ∙𝑺

3(𝑺𝑖 ∙𝒓𝑖𝑗 )(𝑺𝑗 ∙𝒓𝑖𝑗 )

|𝑟𝑖𝑗 |

|𝒓𝑖𝑗 |

𝑖 𝑗
3 ∑
ℋ = 𝐽1 ∑〈𝑖𝑗〉 𝑺𝑖 ∙ 𝑺𝑗 + 𝐷𝑟𝑛𝑛
3 −
𝑗>𝑖 [

5

] − 𝑔𝜇𝐵 ∑𝑖 𝑩 ∙ 𝑺𝑖 ,

(1)

where 𝐽1 is the super-exchange for nearest-neighbor bonds, and 𝐷 is the strength of the dipoledipole interaction. It is worth noting that the Hamiltonian, even in absence of dipole-dipole
interaction, contains exotic “octupolar order” instead of conventional “dipolar order” at the lowest
available temperature50. The magnitude of the classical spins 𝑺𝑖 is fixed as |𝑺𝑖 | = 7/2⁡ in the
simulation. We fix the 𝑔-factor 𝑔 = 2 for Gd3+. The value of the dipole-dipole interaction is
estimated as 𝐷 ≈ 0.0458𝐾 for a lattice constant of 1.2376nm. In the simulations, the dipole-dipole
interaction was treated using the standard Ewald summation technique. The optimal value of 𝐽1 ≈
0.138𝐾 was extracted by fitting the specific heat data of GGG in Ref. [35] while fixing 𝐷 =
0.0458𝐾. Since we restrict to 𝑇 ≥ 1 K in the simulation, the relatively small further-neighbor
super-exchanges can be safely neglected 51.
We employed the classical Monte Carlo (MC) simulations for the model on a 4 × 4 × 4
lattice (each unit cell contains 24 sublattices) with periodic boundary conditions. Specifically, a
total of 105 MC sweeps with Metropolis update were used for each parameter set. During the first
2.5 × 104 sweeps the system was annealed from 𝑇 = 15 K to the target temperature, and the
thermodynamic properties were measured using the 5 × 104 sweeps at the end of the calculation.
For each parameter set a total of 8 independent MC runs (with different random seeds) were
performed to calculate the statistical averages and error bars. We have verified that the Metropolis
update scheme is sufficient for 𝑇 ≥ 1 K and there is no obvious system size dependence
comparing the results on 4 × 4 × 4 and 8 × 8 × 8 lattices (see datails in Supplementary
Information Fig. S15).
The simulated B-T phase diagrams of magnetic specific heat C, magnetization 𝑀 are shown
in Supplementary Information Fig. S8 and the magnetic susceptibility 𝜒 is shown in Fig. 4c in the
main text. From the susceptibility data, it’s obvious that spin fluctuations become stronger below
5 K and below the saturation field, suggesting the experimentally observed anomalous spin
13

## PDF page 14

transport is rooted in the spin fluctuations and spin-spin correlations. Moreover, the relevant
𝑋
experimental parameter regime in the finite 𝑉2𝜔
distribution shown in Fig. 3a overlaps with the

critical fan of the quantum critical point at saturation.
The spin waves in the paramagnetic phase were computed by the equation-of-motion (EOM)
method using spin configurations sampled from Monte Carlo simulations on 4 × 4 × 4 systems.
Specifically, we integrated the Landau-Lifshitz equation in the 4th-order Adams predictorcorrector scheme, with a total duration of 20000 K-1 and step size ∆𝑡 = 0.002 K. Supplementary
Information Fig. S13 shows the dynamic spin structure factor 𝑆(𝑘, 𝑤) at 2K and under different
magnetic fields. At lower magnetic field, while there is no long-range magnetic order, we can still
observe diffusive spin-spin correlation; with increasing magnetic field, the magnon bands are
1

increasingly well-defined. In Supplementary Information Fig. S14, the magnon life time 𝜏 = 𝜎 can
be obtained by a Gaussian fit 𝐴 ∙ 𝑒

−

(𝜔−𝜇)2
2𝜎2

to the energy dispersion, where 𝜇 is the band center and

𝜎 is the standard deviation representing linewidth. We plot the magnon life time of the highest
band at Γ point as a function of magnetic field as shown in Fig. 4d in the main text. Note that for
B = 0 and 0.71T, it is difficult to get a reliable fitting curve, meaning there is no well-defined
magnon, so that they are not included. For B = 1.41T to 5.66T, reliable and rapidly increasing
magnon life time can be obtained, which is shown in Fig. 4d. Importantly, the experimentally
observed dominance of normal spin transport with drastic decrease in spin transport length is
connected to the formation of conventional gapped magnon bands under strong external magnetic
field in the Monte Carlo simulations.
Distance dependence of normal spin transport in GGG and MnPS3
We investigate two points in the “normal” area of the B-T phase diagram, one is at the low
temperature and high magnetic field regime (𝑇 = 2K, 𝐵 = 14T, 𝐼𝑖𝑛 = 100𝜇𝐴), and the other one
is at the high temperature and low magnetic field regime (𝑇 = 5K, 𝐵 = 3T, 𝐼𝑖𝑛 = 100𝜇𝐴). The
experimental data were fitted to the following equation derived from a two-dimensional diffusion
model 11:
𝑉2𝜔 (𝑑) = 𝐶𝐾0 (𝑑/𝜆)

(2)

where 𝐾0 (𝑑/𝜆) is the modified Bessel function of the second kind, 𝜆 is the spin diffusion length,
and 𝐶 is a numerical coefficient that does not depend on distance d. Here the two-dimensional
diffusion model 11 is used because the thickness of GGG is 500⁡𝜇𝑚 > 𝑑. A typical distance
14

## PDF page 15

dependent 𝑉2𝜔 in MnPS3 is also plotted in Supplementary Information Fig. S9. For MnPS3, the
one-dimensional magnon diffusion model 5 is used since its thickness is around 30nm << d. These
normal SHST signals almost fade away within a distance of 5⁡𝜇𝑚.
Finite element analysis of temperature gradience vs. distance
The signal decay curve for spin transport distance from 4𝜇𝑚 to 100𝜇𝑚 is compared with the
temperature gradient distribution obtained from a finite element thermal analysis in Supplementary
Information Fig. S11. The anomalous |𝑉2𝜔 | decays much slower than the temperature gradient,
indicating that the signal cannot be resulted from a local spin Seebeck effect driven by local
temperature gradience beneath the detecting electrode.
In the finite element simulation, tGGG = 500μm is the GGG thickness, and both the width and
length of the GGG slab are 5mm. The injector has a thickness of tPt = 10nm, a length of lPt = 100μm
and a width of wPt = 200nm. The resistance of the Pt injector is measured to be 7000Ω with an
injection current of 𝐼𝑖𝑛 = 100𝜇𝐴. The heat current normal to the GGG|vacuum and Pt|vacuum
vanish. At the bottom of the GGG slab, the boundary condition T = 2K is used. Other parameters
used in the finite element analysis are listed in Supplementary Information Table 1.
Separation of normal and anomalous spin transport signals
𝑋
𝑌
It is experimentally observed that 1) normal 𝑉2𝜔
= 0 and 2) normal 𝑉2𝜔
decays quickly.

These two points can be exploited to separate the normal contribution and the anomalous
𝑋
𝑌
contribution of the spin transport signal to 𝑉2𝜔
and 𝑉2𝜔
when they are mixed at lower temperature
𝑋
𝑌
and lower magnetic field. Supplementary Information Fig. S12a plots 𝑉2𝜔
and 𝑉2𝜔
separately of
𝑋
the |𝑉2𝜔 | data shown in Supplementary Information Fig. S11. One can see that 𝑉2𝜔
follows one
𝑌
𝑋
monotonic curve while 𝑉2𝜔
is non-monotonic, highlighting the fact that 𝑉2𝜔
only has anomalous
𝑌
𝑋
contribution while 𝑉2𝜔
has both anomalous and normal contributions. A fitting of 𝑉2𝜔
with the

two-dimensional diffusion model gives 𝜆 = 55.276 ± 6.53𝜇𝑚, which is one order of magnitude
bigger than the normal case. The isolation of the normal spin signal can be based on the observation
𝑋
𝑌
that the normal spin transport length is relatively short and the trends of 𝑉2𝜔
vs. d and 𝑉2𝜔
vs. d

are similar for distance over 20𝜇𝑚. With the above information, we raise the ansatz that the
𝑌
𝑋
anomalous SHST signal 𝐴𝑉2𝜔
is proportional to 𝑉2𝜔
. Thus, the normal SHST signal 𝑁𝑉2𝜔 can be
𝑌
𝑌
𝑌
𝑋
extracted from 𝑉2𝜔
by subtracting 𝑉2𝜔
with the anomalous SHST signal 𝐴𝑉2𝜔
= −2.58 × 𝑉2𝜔

15

## PDF page 16

(Supplementary Information Fig. S12b). Here the ratio -2.58 is obtained by setting 𝑁𝑉2𝜔 = 0 at
𝑑 = 60⁡𝜇𝑚. A fitting of the extracted 𝑁𝑉2𝜔 data (blue points in Supplementary Information Fig.
12b) to equation (2) gives 𝜆 = 7.3999 ± 1.79𝜇𝑚 , which is consistent with the normal spin
transport behaviors shown in Supplementary Information Fig. S9.

Data Availability
The experimental data generated in this study (Fig. 1-5 in the main text and Fig. S1-7, Fig. S9-12,
Fig. S16-17 in the Supplementary Information) have been deposited in the Harvard Dataverse
under accession code CL317 [52]. All other data that support the findings of this study are available
from the corresponding authors upon request.

Code Availability
The code supporting the analysis reported in this paper is available from the corresponding authors
upon request.

References
1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.

Murakami, S., Nagaosa, N., Zhang, S.-C. Dissipationless Quantum Spin Current at Room
Temperature. Science 301, 1348-1351 (2003).
Kim, S. K. et al. Ferrimagnetic spintronics. Nat. Mater. 21, 24-34 (2021).
Barman, A. et al. The 2021 Magnonics Roadmap. J. Phys.: Condens. Matter 33, 413001
(2021).
Kajiwara, Y. et al. Transmission of electrical signals by spin-wave interconversion in a
magnetic insulator. Nature 464, 262-266 (2010).
Cornelissen, L. J., Liu, J., Duine, R. A., Youssef, J. B., van Wees, B. J. Long-distance
transport of magnon spin information in a magnetic insulator at room temperature. Nat.
Phys. 11, 1022-1026 (2015).
Lebrun, R. et al. Tunable long-distance spin transport in a crystalline antiferromagnetic
iron oxide. Nature 561, 222-225 (2018).
Wei, X. Y. et al. Giant magnon spin conductivity in ultrathin yttrium iron garnet films. Nat.
Mater. 21, 1352-1356 (2022).
Lee, K. et al. Superluminal-like magnon propagation in antiferromagnetic NiO at nanoscale
distances. Nat. Nanotechnol. 16, 1337-1341 (2021).
Shiomi, Y., Saitoh, E. Paramagnetic Spin Pumping. Phys. Rev. Lett. 113, 266602 (2014).
Wu, S. M., Pearson, J. E., Bhattacharya, A. Paramagnetic spin seebeck effect. Phys. Rev.
Lett. 114, 186602 (2015).
Oyanagi, K. et al. Spin transport in insulators without exchange stiffness. Nat. Commun.
10, 4740 (2019).
16

## PDF page 17

12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.
30.
31.
32.
33.
34.

Lin, W., Chen, K., Zhang, S., Chien, C. L. Enhancement of Thermally Injected Spin Current
through an Antiferromagnetic Insulator. Phys. Rev. Lett. 116, 186601 (2016).
Qiu, Z. et al. Spin-current probe for phase transition in an insulator. Nat. Commun. 7, 12670
(2016).
Qiu, Z. et al. Spin colossal magnetoresistance in an antiferromagnetic insulator. Nat. Mater.
17, 577-580 (2018).
Wannier, G. H. Antiferromagnetism. The Triangular Ising Net. Phys. Rev. 79, 357-364
(1950).
Kitaev, A. Anyons in an exactly solved model and beyond. Ann. Phys. 321, 2-111 (2006).
Hoang, D.-T., Diep, H. Spin Transport in Magnetically Ordered Systems: Ferromagnets,
Antiferromagnets and Frustrated Systems. Condens. Matter 8, 3 (2022).
Zarzuela, R., Hill, D., Sinova, J., Tserkovnyak, Y. Dynamically stabilized spin superfluidity
in frustrated magnets. Phys. Rev. B 103, 174424 (2021).
Balents, L. Spin liquids in frustrated magnets. Nature 464, 199-208 (2010).
Sasvári, J., Werner, P.-E. Structural studies of gadolinium gallium garnet. Acta Chem.
Scand. 37, 203-206 (1983).
Dunsiger, S. R. et al. Low Temperature Spin Dynamics of the Geometrically Frustrated
Antiferromagnetic Garnet Gd3Ga5O12. Phys. Rev. Lett. 85, 3504-3507 (2000).
Schiffer, P. et al. Frustration Induced Spin Freezing in a Site-Ordered Magnet: Gadolinium
Gallium Garnet. Phys. Rev. Lett. 74, 2379-2382 (1995).
Tsui, Y. K., Burns, C. A., Snyder, J., Schiffer, P. Magnetic Field Induced Transitions from
Spin Glass to Liquid to Long Range Order in a 3D Geometrically Frustrated Magnet. Phys.
Rev. Lett. 82, 3532-3535 (1999).
Paddison Joseph, A. M. et al. Hidden order in spin-liquid Gd3Ga5O12. Science 350, 179181 (2015).
Deen, P. P. An Overview of the Director State in Gadolinium Gallate Garnet. Front. Phys.
10, 868339 (2022).
d’Ambrumenil, N., Petrenko, O. A., Mutka, H., Deen, P. P. Dispersionless Spin Waves and
Underlying Field-Induced Magnetic Order in Gadolinium Gallium Garnet. Phys. Rev. Lett.
114, 227203 (2015).
Ancliff, M., Sachnev, V., d’Ambrumenil, N. Model of the low temperature magnetic phases
of gadolinium gallium garnet. J. Phys.: Condens. Matter 33, 475801 (2021).
Jacobsen, H. et al. Spin dynamics of the director state in frustrated hyperkagome systems.
Phys. Rev. B 104, 054440 (2021).
Deen, P. P. et al. Spin dynamics in the hyperkagome compound Gd3Ga5O12. Phys. Rev. B
82, 174408 (2010).
Oyanagi, K. et al. Paramagnetic spin Hall magnetoresistance. Phys. Rev. B 104, 134428
(2021).
Stefanita, C.-G. Magnetism: Basics and Applications, 1 edn. Springer Berlin, Heidelberg:
Boston, MA., 2012.
Saitoh, E., Ueda, M., Miyajima, H., Tatara, G. Conversion of spin current into charge
current at room temperature: Inverse spin-Hall effect. Appl. Phys. Lett. 88, 182509 (2006).
Ghimire, K., Haneef, H. F., Collins, R. W., Podraza, N. J. Optical properties of singlecrystal Gd3Ga5O12 from the infrared to ultraviolet. Phys. Status Solidi B 252, 2191-2198
(2015).
Chen, G. et al. Electrically switchable van der Waals magnon valves. Nat. Commun. 12,
6279 (2021).
17

## PDF page 18

35.
36.
37.
38.
39.
40.
41.
42.
43.
44.
45.
46.
47.
48.
49.
50.
51.
52.

Kinney, W. I., Wolf, W. P. Magnetic interactions and short range order in gadolinium
gallium garnet. J. Appl. Phys. 50, 2115-2117 (1979).
An, K. et al. Coherent long-range transfer of angular momentum between magnon Kittel
modes by phonons. Phys. Rev. B 101, 060407(R) (2020).
Rückriegel, A., Duine, R. A. Long-Range Phonon Spin Transport in Ferromagnet–
Nonmagnetic Insulator Heterostructures. Phys. Rev. Lett. 124, 117201 (2020).
Liu, C. et al. Probing short-range magnetic order in a geometrically frustrated magnet by
means of the spin Seebeck effect. Phys. Rev. B 98, 060415(R) (2018).
Shan, J. et al. Influence of yttrium iron garnet thickness and heater opacity on the nonlocal
transport of electrically and thermally excited magnons. Phys. Rev. B 94, 174437 (2016).
Hirobe, D. et al. One-dimensional spinon spin currents. Nat. Phys. 13, 30-34 (2016).
Topping, C. V., Blundell, S. J. A.C. susceptibility as a probe of low-frequency magnetic
dynamics. J. Phys.: Condens. Matter 31, 013001 (2019).
Petrenko, O. A., Ritter, C., Yethiraj, M., McK Paul, D. Investigation of the LowTemperature Spin-Liquid Behavior of the Frustrated Magnet Gadolinium Gallium Garnet.
Phys. Rev. Lett. 80, 4570-4573 (1998).
Ancliff, M., Sachnev, V. Numerical estimation of the ground states of frustrated
antiferromagnet gadolinium gallium garnet. J. Korean Phys. Soc. 82, 699-706 (2023).
Xing, W. et al. Magnon Transport in Quasi-Two-Dimensional van der Waals
Antiferromagnets. Phys. Rev. X 9, 011026 (2019).
Yuan, W. et al. Experimental signatures of spin superfluid ground state in canted
antiferromagnet Cr2O3 via nonlocal spin transport. Sci. Adv. 4, eaat1098 (2018).
Tserkovnyak, Y., Ochoa, H. Generalized boundary conditions for spin transfer. Phys. Rev.
B 96, 100402(R) (2017).
Ochoa, H., Zarzuela, R., Tserkovnyak, Y. Spin hydrodynamics in amorphous magnets.
Phys. Rev. B 98, 054424 (2018).
Iacocca, E., Hoefer, M. A. Hydrodynamic description of long-distance spin transport
through noncollinear magnetization states: Role of dispersion, nonlinearity, and damping.
Phys. Rev. B 99, 184402 (2019).
Goli, V. M. L. D. P., Manchon, A. Crossover from diffusive to superfluid transport in
frustrated magnets. Phys. Rev. B 103, 104425 (2021).
Zhitomirsky, M. E. Octupolar ordering of classical kagome antiferromagnets in two and
three dimensions. Phys. Rev. B 78, 094423 (2008).
Yavors'kii, T., Enjalran, M., Gingras, M. J. Spin Hamiltonian, competing small energy
scales, and incommensurate long-range order in the highly frustrated Gd3Ga5O12 garnet
antiferromagnet. Phys. Rev. Lett. 97, 267203 (2006).
Chen, D. Long-distance spin transport in frustrated hyperkagome magnet Gd3Ga5O12.
https://doi.org/10.7910/DVN/MOC96L Harvard Dataverse (2025).

Acknowledgments
This project has been supported by the National Key R&D Program of China (Grant Nos.
2024YFA1409001 (J.-H.C), 2024YFA1408303 (Z.W.)), the Innovation Program for Quantum
Science and Technology (2021ZD0302403 (J.-H.C)), the National Natural Science Foundation of
18

## PDF page 19

China (NSFC Grant Nos. 12304537 (D.C.), 92265106 (J.-H.C), 11774010 (J.-H.C), 11921005 (J.H.C), 12374124 (Z.W.)). J.-H.C acknowledges technical support form Peking Nanofab.

Author Contributions Statement
J.-H.C conceived the idea and directed the experiment; D.C. fabricated most of the devices and
performed the transport measurements; B.L. & L.J. aided in device fabrication; C.T. did the
SQUID measurement; S.Q., G.C., S.Y., M.H., J.C. & Y.F. aided in transport measurement; D.C.,
B.L. & K.C. collected and did data analysis; J.Z. provided computational facilities; L.X., J.Z., Z.X.,
X.C.X., R.S., Z.W. & J.X. provided theoretical and numerical analysis; H.C. performed the finite
element analysis of heat distribution; D.C. & J.-H.C wrote the manuscript; all authors commented
and modified the manuscript.

Competing interests statement
The authors declare no competing interests.

19

## PDF page 20

Fig. 1 | Spin transport in frustrated hyperkagome magnet GGG. (a) Sketches of spin wave in
ordered magnet and fluctuating spins in frustrated magnet. The opaque arrows represent the
localized magnetic moments, while the transparent arrows represent the fluctuations of the
moments. (b) Schematic of the long-range multipole order formed from ten-spin loops of Gd3+ in
GGG. Orange double-headed arrows indicate the ten-spin director that are ordered normal to the
loop plane. Smaller gray arrows represent the localized magnetic moments. (c) Crystal structure
of hyperkagome magnet GGG with only Gd atoms shown. The two inter-penetrating cornersharing Gd3+ triangular sublattices are colored in gray and pink, respectively. (d) Schematics of
the nonlocal spin transport measurement setup with electrical connections. Two Pt wires are
patterned on a GGG slab, one to inject spin current by thermal excitation and the other to detect
the spin current through inverse spin Hall effect. Specifically, 𝐼𝑖𝑛 : AC injection current; 𝑉2𝜔 : the
second harmonic thermal magnon inverse spin Hall signal; θ: the angle of the in-plane magnetic
field B with respect to the direction perpendicular to the Pt electrodes. The inset shows angle
dependent 𝑉2𝜔 of GGG with 𝐵 = 3T and 𝐼𝑖𝑛 = 80𝜇𝐴 and T= 2K, in which the black solid line is
a cosine function fit.

20

## PDF page 21

Fig. 2 | Magnetic field and injection current dependent nonlocal signal 𝑽𝑿,𝒀
𝟐𝝎 . (a) (b) 2D color
𝑋
𝑌
plot of 𝑉2𝜔
(a) and 𝑉2𝜔
(b) versus B and 𝐼𝑖𝑛 in GGG, respectively. All data are taken from a GGG
device with a 2𝜇𝑚 channel length at T = 2K. The dashed gray lines are guides for the boundary of
𝑋
𝑌
the anomalous signal. (c) (d) 𝑉2𝜔
and 𝑉2𝜔
versus B in a typical GGG (c) and MnPS3 (d) device
𝑋
𝑌
with 𝐼𝑖𝑛 = 100𝜇𝐴, respectively. (e) (f) 𝑉2𝜔 and 𝑉2𝜔
versus 𝐼𝑖𝑛 in a typical GGG device at T = 2K
and B = 3T (e) and a typical MnPS3 device at T = 2K and B = 4T (f), respectively. The injection
current frequency is 17.77Hz.

21

## PDF page 22

Fig. 3 | Temperature and magnetic field dependence of the nonlocal signal 𝑽𝑿,𝒀
𝟐𝝎 . (a) (b) 2D
𝑋
𝑌
color plots of 𝑉2𝜔
and 𝑉2𝜔
vs. T and B, respectively, with 𝐼𝑖𝑛 = 100𝜇𝐴 and channel length of 1𝜇𝑚.
𝑋
𝑌
(c) (d) T dependence of 𝑉2𝜔
and 𝑉2𝜔
in a typical GGG device (c) and MnPS3 device (d),
respectively. Here B = 3T for GGG and 4T for MnPS3, and the injection current frequency is
17.77Hz.

22

## PDF page 23

Fig. 4 | Magnetic excitation related to spin-spin correlations. (a) Injection frequency-dependent
𝑋
𝑌
𝑉2𝜔
and 𝑉2𝜔
at 1.8K to 4K with 𝐼𝑖𝑛 = 200𝜇𝐴, B = 3T and channel length of 10𝜇𝑚. (b) Simulation
of the real and imaginary part of the response 𝜒(𝜔) for an overdamped forced oscillator. Here
𝜔0 = 2, 2.4, 2.8, 3.2, 3.6, 4⁡𝑘𝐻𝑧⁡and 𝛽 = 60. (c) Monte Carlo simulated magnetic susceptibility vs.
T and B applied along the [-1,1,0] direction. (d) Magnetic field dependent magnon life time 𝜏 of
the highest band at Γ point obtained from Monte Carlo simulations at 2K. The error bars of 𝜏 are
calculated from the standard error of the linewidth 𝜎.

23

## PDF page 24

Fig. 5 | Anomalous long-distance spin transport in GGG. (a) |𝑉2𝜔 | versus channel length d for
normal and anomalous spin transport states. Anomalous GGG (marked as an-GGG): blue circles,
𝐵 = 3T, 𝐼𝑖𝑛 = 200𝜇𝐴, T = 2K; normal GGG (marked as n-GGG): purple triangles, 𝐵 = 3T, 𝐼𝑖𝑛 =
100𝜇𝐴, T = 5K; red squares, 𝐵 = 14T, 𝐼𝑖𝑛 = 100𝜇𝐴, T = 2K; MnPS3: yellow triangles, 𝐵 = 4T,
𝐼𝑖𝑛 = 100𝜇𝐴, T = 2K. Every data point is extracted by a cosine fit from a magnetic field angledependent measurement, with error bar represented the standard error of fit. The yellow solid line
is a fit to the 1D magnon diffusion model 5 while other solid lines are fits to the 2D diffusion model
due to larger sample thickness 11. (b) Comparison of our work and the reported maximum transport
distances of thermal excited magnons in the literature 5, 6, 44, 45, grouped in magnetically ordered
region (blue part), and magnetically frustrated region (red part).

24
