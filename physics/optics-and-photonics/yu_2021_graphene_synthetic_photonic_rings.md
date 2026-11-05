Source: https://doi.org/10.1038/s42005-021-00719-9
PDF sha256: 4594a252613b9e9a879c1568459fb8d850c2df798c8cf7bf3274de9109c6d4ec
License: https://creativecommons.org/licenses/by/4.0

# Transcription of yu_2021_graphene_synthetic_photonic_rings.pdf

Transcription of `yu_2021_graphene_synthetic_photonic_rings.pdf` in this directory, 9 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 5 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories; pages 1-4, 6-9 from the PDF's own text layer (pdftotext version 26.10.0, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

ARTICLE
https://doi.org/10.1038/s42005-021-00719-9

OPEN

Simulating graphene dynamics in synthetic space
with photonic rings

1234567890():,;

Danying Yu1,8, Guangzhen Li
Xianfeng Chen1,5,6,7

1,8, Meng Xiao

2, Da-Wei Wang

3, Yong Wan4, Luqi Yuan

1✉ &

Photonic honeycomb lattices have attracted broad interests for their fruitful ways in
manipulating light, which yet hold difﬁculties in achieving arbitrary reconﬁgurability and
hence ﬂexible functionality due to ﬁxed geometry conﬁgurations. Here we theoretically
propose to construct the honeycomb lattice in a one-dimensional ring array under dynamic
modulations, with an additional synthetic dimension created by connecting the frequency
degree of freedom of light. Such a system is highly re-conﬁgurable with parameters ﬂexibly
controlled by external modulations. Therefore, various physical phenomena associated with
graphene including Klein tunneling, valley-dependent edge states, effective magnetic ﬁeld, as
well as valley-dependent Lorentz force can be simulated in this lattice, which exhibits
important potentials for manipulating photons in different ways. Our work unveils an alternative platform for constructing the honeycomb lattice in a synthetic space, which holds
complex functionalities and could be important for optical signal processing as well as
quantum simulation.

1 State Key Laboratory of Advanced Optical Communication Systems and Networks, School of Physics and Astronomy, Shanghai Jiao Tong University,

200240 Shanghai, China. 2 Key Laboratory of Artiﬁcial Micro- and Nano-Structures of Ministry of Education and School of Physics and Technology, Wuhan
University, 430072 Wuhan, China. 3 Interdisciplinary Center for Quantum Information and Zhejiang Province Key Laboratory of Quantum Technology and
Device, Department of Physics, Zhejiang University, 310027 Hangzhou, China. 4 National Institute of Metrology, 102200 Beijing, China. 5 Shanghai Research
Center for Quantum Sciences, 201315 Shanghai, China. 6 Jinan Institute of Quantum Technology, 250101 Jinan, China. 7 Collaborative Innovation Center of
Light Manipulations and Applications, Shandong Normal University, 250358 Jinan, China. 8These authors contributed equally: Danying Yu, Guangzhen Li.
✉email: yuanluqi@sjtu.edu.cn
COMMUNICATIONS PHYSICS | (2021)4:219 | https://doi.org/10.1038/s42005-021-00719-9 | www.nature.com/commsphys

1

## PDF page 2

ARTICLE

COMMUNICATIONS PHYSICS | https://doi.org/10.1038/s42005-021-00719-9

H

resonant modes near the zero GVD point and is conﬁrmed by
previous experiments41–44. We place electro-optic modulators
(EOM) inside two rings, with modulation frequency Ω/2 and
modulation phase ϕ. A synthetic frequency dimension with the
effective hopping amplitude g can be constructed with spaced
frequency Ω/2 in the frequency axis of light, where modes supported by rings A and B are labeled by a and b, respectively. With
the building block for constructing the one-dimensional synthetic
frequency dimension in a pair of rings, we can then use it to
construct a synthetic honeycomb lattice in a one-dimensional
array of pairs of rings shown in Fig. 1b [see “Methods” section].
The ring array consists groups of rings (n = 1, 2, . . . , N), each of
which contains two pairs of rings with different combinations,
i.e., AB (labeled as α = 1) and BA (labeled as α = 2), respectively.
We write the Hamiltonian of the system under the ﬁrst-order
approximation:
h
H r ¼ ∑ κðayn;m;1 an1;m;2 þ byn;m;2 bn;m;1 Þ

oneycomb lattices, possessing the same geometry as
graphene1,2, have attracted great interest in condensed
matter physics3,4 and photonics5,6. Rich physical phenomena have been reported in photonic honeycomb lattices,
taking advantage of properties of Dirac points and the valley
degree of freedom6–15 and showing an excellent platform for
studying topological photonics16, which also have potential
applications in the interface of nonlinear optics17 and quantum
optics18, pointing towards topological ﬁber19, topological laser20,
as well as edge and gap solitons21. Different platforms have been
achieved to construct photonic honeycomb lattices, such as
waveguide arrays22, on-chip silicon photonics23, semi-conductor
microcavities24, and metamaterials25. However, one notes that the
reconﬁgurability and ﬂexible experimental feasibility of a system
are attractive for satisfying various experimental requirements
and different applications, as well as relaxing the fabrication
constrains, which are naturally limited in the current honeycomb
systems due to their ﬁxed conﬁgurations or structures after
fabrication22–25. Therefore, it is of signiﬁcant importance to ﬁnd
an alternative platform, which is experimentally feasible and
holds reconﬁgurability.
Recently, synthetic dimensions have experienced extensive
explorations in many areas of photonics, for providing exotic
connectivities and exploring physics beyond real dimensions, in
which a photonic synthetic dimension can be formed by coupling
suitable degrees of freedom of light, such as frequency modes,
orbital angular momenta, modal dimensions, and others26–28.
Among the various platforms to construct synthetic dimensions,
a ring resonator under dynamic modulation has been found to be
capable of creating a synthetic dimension along the frequency
axis of light29, which together with spatial dimensions, a variety
of physical implementations have been suggested with two or
more dimensions30–39.
Here, we theoretically propose the construction of a highly reconﬁgurable honeycomb lattice in a synthetic space in a modulated ring resonator system. We show that a one-dimensional ring
resonator array composed by two types of resonators under
appropriate dynamic modulation supports a two-dimensional
honeycomb lattice in a synthetic space including both spatial and
frequency dimensions. Different physics associated with the
photonic graphene can be simulated in this unique platform, such
as Klein tunneling14, valley-dependent edge states13, topological
edge states with the effective magnetic ﬁeld40, and valleydependent Lorentz force8. The modulated ring systems can be
realized in either ﬁber-based system41–44 or on-chip lithium
niobate resonator45, which brings our proposal to a ﬂexible
experimental setup with state-of-art technologies in bulk optics or
integrated photonics. Our work not only broadens the current
research on synthetic dimensions in photonics26,27, but also
enriches quantum simulations with topological photonics46,47,
which shows potential applications in optical signal
processing48,49 and quantum computations50,51.

where ayn;m;α (an,m,α) and byn;m;α (bn,m,α) are corresponding creation
(annihilation) operators, and κ is the evanescent-wave coupling
strength between two rings at the same type. The Hamiltonian in
Eq. (1) therefore supports a two-dimensional synthetic honeycomb lattice [Fig. 1c].
The honeycomb lattice is constructed in a synthetic space
including the spatial (x) and frequency (f) dimensions. Different
from conventional photonic honeycomb lattice in real space13,14
that depends greatly on apparent geometry, the synthetic
honeycomb lattice in Eq. (1) is dependent on both couplings
between rings (κ) and modulations (gi). Therefore, without loss of
generality, we label the horizontal distance in the synthetic lattice
between two sites with the same types as d and the horizontal
distance between two sites with different types as d/2 along the x
axis in the later plots of ﬁeld patterns. The ﬂexible choice of
hopping amplitude gi and phase ϕi provides powerful reconﬁgurability toward different physical phenomena in simulating
graphene dynamics. We ﬁrst consider κ = gi = g and ϕi = 0, and
the synthetic lattice holds the unit cell with the translation
symmetry including two frequency modes a and b in two rings.
The band structure of this honeycomb lattice in the ﬁrst Brillouin
zone can be plotted in the kx–kf space, where kx and kf are wave
vectors reciprocal to the spatial (x) and frequency (f) axes,
respectively. Dirac point K and K 0 at (kx, kf) = (0, ±4π/3Ω) can be
seen in the band structure in Fig. 1d, where the zoomed-in Dirac
cone shows linear dispersion near K 0 point [Fig. 1e]. In the
following, we will show the capability for achieving different
phenomena associated with the honeycomb lattice with the
current platform.

Results
Model. We begin with considering a pair of ring resonators
(labeled as A and B) with the same circumference L undergoing
dynamic modulation [Fig. 1a]. The central resonant frequencies
of ring A and ring B are set at ω0 and ω0 − Ω/2, respectively. In
the absence of group velocity dispersion (GVD) in waveguides
that compose rings, the frequency of the mth resonant mode in
ring A (ring B) is ωm,A = ω0 + mΩ (ωm,B = ω0 − Ω/2 + mΩ),
where Ω = 2πvg/L is the free spectral ranges (FSR) with vg being
the group velocity inside both rings. The approximation that
GVD of waveguides is zero makes the synthetic frequency
dimension being uniform, which is valid for considering ﬁnite

Klein tunneling. Klein tunneling, as an intriguing phenomenon in
physics exploring a particle passing through a barrier higher than its
energy, has experienced great interest in different platforms
including graphene and photonic/phononic crystals7,14,52,53. To
demonstrate such physics in the synthetic honeycomb lattice in
Fig. 1c, we couple the ﬁrst (A1) and the last (A2N) rings with an
external waveguide such that a periodic condition along the x axis
can be naturally created. Such a design forms a carbon-nanotubelike shape [Fig. 2a]. In simulation, we consider N = 12, which
corresponds to 48 rings ranging inside x ∈ [0, 35d], and modes in
the region f ∈ [− 8Ω, 47.5Ω]. Here we refer f = 0 to ω0,B and denote
the ﬁrst (A1) ring as x = 0 for the simplicity. We ﬁrst excite the
honeycomb lattice by injecting an input plane wave with

2

m;n

ð1Þ
þ g 2n1 ðayn;m;1 bn;m;1 eiϕ2n1 þ ayn;m;1 bn;mþ1;1 eiϕ2n1 Þ
i
þ g 2n ðbyn;m;2 an;m1;2 eiϕ2n þ byn;m;2 an;m;2 eiϕ2n Þ þ h:c:;

COMMUNICATIONS PHYSICS | (2021)4:219 | https://doi.org/10.1038/s42005-021-00719-9 | www.nature.com/commsphys

## PDF page 3

COMMUNICATIONS PHYSICS | https://doi.org/10.1038/s42005-021-00719-9

ARTICLE

Fig. 1 Construction of synthetic honeycomb lattice. a Rings A and B support a set of resonant modes a (blue circle) and b (cyan circle) separated by the
free spectral range Ω in the frequency dimension (f). Both rings are modulated by electro-optic modulator (EOM) with modulation phase ϕ, modulation
frequency Ω/2, and effective hopping amplitude g. ω0 and ω0 − Ω/2 are central resonant frequencies of ring A and ring B. m denotes the index of the mth
resonant mode. b A one-dimensional array of ring resonators is composed of groups of pairs of rings in a along the spatial dimension x. Ai (Bi) represents
the ith ring A (ring B), where i is a positive integer. c The system in b can be mapped into a honeycomb lattice in a synthetic space including one spatial
dimension (x) and one frequency dimension (f). an,m,α and bn,m,α represent the operator for the ﬁeld at the mth mode in ring A and ring B, which are labeled
by integers n and α as indicated in the ﬁgure. gi and ϕi are the corresponding effective hopping amplitude and modulation phase, while κ is the coupling
strength. d The band structure of the honeycomb lattice in the reciprocal space (kx, kf), where kx and kf are wave vectors reciprocal to spatial and frequency
axes, ε is the eigenvalue (frequency shift of the ﬁeld), and d denotes the horizontal distance between two sites with same types in the synthetic lattice.
e The zoomed-in Dirac cone at K 0 point in d.

distribution of s1 ¼ eðf f 0 Þ =Δ eikx ðxx0 Þþikf ðf f 0 Þ to excite the initial
wave packet of the ﬁeld shown in Fig. 2b, where f0 = 39Ω,
x0 = 17.5d, and Δ = 8.95Ω, and collect signals through external
waveguides to readout the evolution of the ﬁeld in the synthetic
honeycomb lattice [see “Methods” section]. We set the k-vector in
s1 in the vicinity of the Dirac point K by using (kx, kf) = (0, 4.04π/
3Ω). The corresponding frequency detuning of the source is
ε = 0.036g, which falls in the linear dispersion region in the Dirac
cone as indicated in Fig. 1d and gives the initial velocity of the wave
packet along the negative kf direction. The simulation veriﬁes this
feature, that the ﬁeld propagates to the bottom of the synthetic
honeycomb lattice at t = 42g−1 as shown in Fig. 2c without distortion in shape, since there is no barrier in this case.
Based on the calculation in Fig. 2c, we set an artiﬁcial squareshape barrier in the middle range of the frequency dimension in
the synthetic honeycomb lattice as shown in Fig. 2d, which in
principle can be achieved by adding on-site potential terms
Vayn;m;α an;m;α and Vbyn;m;α bn;m;α in the range f ∈ [12, 35.5]Ω. We
ﬁrst consider the case with V = 0.05g which gives ε < V. The ﬁeld
experiences an effective lift in its energy in the barrier region, but
still sticks to the linear region of the Dirac cone, so the initial
negative group velocity does not change during this process
[Fig. 2d]. This is indeed veriﬁed in the simulation in Fig. 2e,
which shows that the ﬁeld propagates to the bottom of the
synthetic honeycomb at t = 42g−1 without signiﬁcant change in
the ﬁeld distribution. As a comparison, we take a larger potential
V = 1.5g, outside of the linear region of the Dirac cone, where the
ﬁeld propagation is distorted as shown in Fig. 2f.
The artiﬁcial square-shape barrier along the frequency axis of
light is not easy to be constructed in the frequency dimension. In
the waveguide that composes the ring, there exists the group
velocity dispersion that can introduce on-site potentials at modes
with different resonant frequencies34,54. We now take the
dispersion back into the consideration only in this part, with
the zero dispersion point at f1 = 23.75Ω. The modulation
2

2

frequency is chosen to be resonant with the frequency spacing
between modes near f = 8.5Ω (and 39Ω), which results in an
effective parabola-shape potential barrier Vðf Þ ¼ 0:05g þ
2Dðf =Ω  f 1 =ΩÞ2 with D = −1.075 × 10−4g [Fig. 2g]. Such the
group velocity dispersion can be designed by the waveguidestructure engineering55. Note here the maximum value of the
barrier (V max ) is 0.05g > ε. Different from the previous case in
Fig. 2d that the ﬁeld experiences a sudden change in the synthetic
k-space, when the wave packet of the ﬁeld propagates toward the
bottom of the synthetic lattice, it experiences a gradual change
inside the Dirac cone. Yet, the distribution of the wave packet still
remains largely unchanged at t = 42g−1, as one sees in Fig. 2h.
The propagation of the ﬁeld is distorted if one uses a larger
barrier, i.e., beyond the limit of the Dirac cone as shown in Fig. 2i,
where the simulation is performed with V max ¼ 1:5g. Therefore,
as long as the potential change is limited inside the linear region
near the Dirac point, the constructed synthetic honeycomb lattice
supports the Klein tunneling along the frequency axis of light.
Valley-dependent edge state. Valley-dependent photonic phenomena recently attract a broad interest in photonics for providing valley degree of freedom, which offers a new possibility to
manipulate light and ﬁnds important applications in optical
encoding and enlarging the optical information capacity13. Here
we show the existence of valley-dependent edge states in the
synthetic space. Lengths of rings are carefully adjusted to introduce the required effective on-site potential in each ring, which
breaks the inversion symmetry of the synthetic lattice and lifts the
degeneracy at Dirac points K and K 0 .
We consider 12 pairs of rings (24 rings), each of which has a
different circumference L0 close to the reference length L. The
offset in length leads to slightly shifted resonant frequencies in
each ring, which leads to the effective on-site potential on each
column site in the synthetic lattice as shown in Fig. 3a [see
“Methods” section]. As one can see, we consider that there are

COMMUNICATIONS PHYSICS | (2021)4:219 | https://doi.org/10.1038/s42005-021-00719-9 | www.nature.com/commsphys

3

## PDF page 4

ARTICLE

COMMUNICATIONS PHYSICS | https://doi.org/10.1038/s42005-021-00719-9

Fig. 2 Klein tunneling. a An external waveguide connects the ﬁrst (A1) and last (A2N) ring resonator together, which forms an effective carbon-nanotubelike honeycomb lattice in the synthetic space with spatial direction (x) being periodic and frequency dimension (f) being ﬁnite. N is the number of groups
of rings. b The intensity distribution in the synthetic lattice of the initial plane-wave excitation at propagation time t = 0. Ω is the free spectral range, and
d denotes the horizontal distance between two sites with the same types in the synthetic lattice. c The intensity distribution in the synthetic lattice at
t = 42g−1 with no barrier, with g being the effective hopping amplitude. d The cartoon of the excited wave packet in the Dirac cone moving towards the
negative direction along square-shape potential barrier (green line) with the frequency detuning ε (dashed gray line). The corresponding intensity
distribution in the synthetic lattice with the square-shape potential barrier in d at t = 42g−1 with maximum potential value e V = 0.05g and f V = 1.5g.
g The cartoon of the excited wave packet in the Dirac cone moving towards the negative direction along parabola-shape potential barrier (green line) with
the frequency detuning ε (dashed gray line). The corresponding intensity distribution in the synthetic lattice with the parabola-shape potential barrier in
g at t = 42g−1 with maximum potential value h V max ¼ 0:05g and i V max ¼ 1:5g. The red arrows in d and g present the direction of velocity.

on-site potentials ± U0 alternatively in each ring except for the
middle two rings having −U0 forming the artiﬁcial domain wall.
The band structures with an inﬁnite frequency dimension and
ﬁnite rings can be calculated. Figure 3b, c plots the projected band
structures with potentials U0 = 0 and U0 = 0.5g, respectively. One
sees that the Dirac point at K (K 0 ) with kf = 4π/3Ω (kf = 2π/3Ω) is
open and valley-dependent edge states are shown when effective
on-site potentials are added.
To verify edge states in two valleys in the synthetic honeycomb
lattice, we further assume that there are boundaries at the
frequency dimension, which can be achieved either by adding
auxiliary rings to knock out certain modes at particular
frequency56 or by designing a sharp change in the group velocity
dispersion of the waveguide that composes the ring30. Therefore,
a lattice with the range of x ∈ [0, 17d] and f ∈ [0, 23.5Ω] is
considered in simulations. We excite the 12th ring on the artiﬁcial
domain wall by a source ﬁeld which has the Gaussian spectrum:
2
2
s2 ¼ eikf ðf f 2 Þ  eðf f 2 Þ =Δ , with f2 = 11.5Ω and Δ = 8.49Ω. kf
here indicates the relative phase information for different
frequency components in the source. We ﬁrst choose kf = 4π/
3Ω, which excites states near K point, and the simulation results
at t = 10g−1 with U0 = 0 and U0 = 0.5g are plotted in Fig. 3d, e,
respectively. One can see that when effective potentials are zero
and the K point is degenerate, the ﬁeld leaves the domain wall and
spreads into the left and right sides of the synthetic lattice. On the
other hand, when there are non-zero potentials shown in Fig. 3a,
the one-way edge state at the K valley is excited and propagates
towards lower frequency components with most of the energy
4

concentrated in the middle two rings on the artiﬁcial domain
wall. Moreover, if we choose kf = 2π/3Ω in the source to excite
the edge state near the K 0 point, the ﬁeld experience
unidirectionally up-conversion in the middle two columns of
the synthetic lattice [Fig. 3f], which shows the possibility of
achieving valley-dependent edge states in the synthetic lattice.
Effective magnetic ﬁeld. Photons are neutral particles, but it has
been shown that, by introducing the proper distribution of
hopping phases in a photonic lattice, one can create an effective
magnetic ﬁeld for photons42. In the synthetic honeycomb lattice
in Fig. 1c, we consider the modulation phase as ϕ2n−1 = (2n − 1)
ϕ and ϕ2n = (2n)ϕ. In each unit cell, the clockwise accumulation
of the hopping phase is −2ϕ, which naturally brings an effective
magnetic ﬁeld. In Fig. 4a, we consider an inﬁnite synthetic lattice
and plot the projected band structure along ϕ, which gives the
butterﬂy-like spectrum. The choice of phase can be tuned in each
modulator arbitrarily. If we set ϕ = π/4, a projected band structure along the kf axis can be plotted by considering ﬁnite number
of rings (with n ∈ [1, 40]). As shown in Fig. 4b, one can see that
there are 8 bulk bands, which is consistent with the fact that there
are 8 sites in each unit cell once phases with ϕ = π/4 are considered. The middle two bulk bands have degenerate points.
Meanwhile, there are 6 gaps between bulk bands, where it supports 8 pairs of topologically protected edge states. By analyzing
the distribution of the eigenstate for each edge state, we can ﬁnd
whether the edge state is located on the left or right edge, as
shown in Fig. 4b. Moreover, the Chern number for each bulk

COMMUNICATIONS PHYSICS | (2021)4:219 | https://doi.org/10.1038/s42005-021-00719-9 | www.nature.com/commsphys

## PDF page 5

ARTICLE
COMMUNICATIONS PHYSICS | https://doi.org/10.1038/s42005-021-00719-9
(a)
<math>U_0 - U_0 \ U_0 - U_0 \cdots U_0 - U_0 \ U_0 - U_0 - U_0 \ U_0 - U_0 \ U_0 \cdots - U_0 \ U_0 - U_0 \ U_0</math>
(b) <math>_3</math>
(c) <math>_{3}</math>
<math>\varepsilon/g</math>
<math>\varepsilon/g</math>
0
0
<math>-3</math>
<math>-3</math>
<math>2\pi/3</math>
<math>4\pi/3</math>
<math>2\pi/3</math>
<math>4\pi/3</math>
<math>2\pi</math>
0
<math>2\pi</math>
0
<math>k_f\Omega</math>
<math>k_f\Omega</math>
(d) 24 K
(f) <b>K</b>'
(e) K
1
18
<math>\sum_{j=12}^{n}</math>
6
0
8
16
0
8
16
0
0
8
16
x/d
x/d
x/d
Fig. 3 Valley-dependent edge state. a Effective on-site potentials (<math>U_0</math> and <math>-U_0</math>) are alternatively applied in the synthetic lattice [formed by spatial
dimension (x) and frequency dimension (f)], with an artificial domain wall in the middle two columns of synthetic lattices (labeled in red dashed line). The
projected band structure in finite rings with <math>\mathbf{b}</math> <math>U_0 = 0</math>, and <math>\mathbf{c}</math> <math>U_0 = 0.5g</math>. <math>k_f</math> is the wave vector reciprocal to frequency axis, <math>\varepsilon</math> is the frequency shift of the field,
<math>\Omega</math> is the free spectral range, and g is the effective hopping amplitude. K and K' are two Dirac points. The simulated intensity distributions at propagation
time <math>t=10g^{-1}</math> under conditions: <b>d</b> <math>U_0=0</math>, and <math>k_f=4\pi/3\Omega</math>; <b>e</b> <math>U_0=0.5g</math>, and <math>k_f=4\pi/3\Omega</math>; <b>f</b> <math>U_0=0.5g</math>, and <math>k_f=2\pi/3\Omega</math>. d labels the horizontal distance
between two sites with same types in the synthetic lattice. Red arrows indicate the excitation at the 12th ring with the central frequency mode at <math>f_2 = 11.5\Omega</math>.
White arrows denote the unidirectional propagation.
band counting from the highest band can be calculated as 1, 1,
the effective magnetic field. In this case, we again consider the
<math>-3</math>, 2, <math>-3</math>, 1, 1, respectively.
excitation <math>\omega_s = \varepsilon_1</math>, and plot the result in Fig. 4d. Different from
We then perform simulations in a synthetic honeycomb lattice
Fig. 4c, here one can see the topologically protected one-way edge
in 12 pairs of rings with <math>f \in [0, 11.5\Omega]</math>. To excite a specific edge
state propagating towards lower frequency components at the
right boundary, which is consistent with the negative slope of the
state in Fig. 4b, we choose a single-frequency source field at the
frequency <math>\omega_{m=5,A} + \omega_s</math> near the 5th mode with a small detuning
edge state at <math>\varepsilon_1</math> in Fig. 4b. We further use <math>\omega_s = \varepsilon_2 = 1.7g</math> and
<math>\omega_{\rm s}</math>, i.e., <math>s_{\rm s}=e^{-i\omega_{\rm s}t}</math> and excite the rightmost ring. The simulations
<math>\omega_{\rm s} = \varepsilon_3 = 2.2g</math> to perform simulations and plot results in Fig. 4e, f,
respectively. In both cases, the excited edge states propagate
are performed with different parameters and results are plotted in
Fig. 4c-f at <math>t = 20g^{-1}</math>. We first set <math>\phi = 0</math>, so there is no effective
towards higher frequency components unidirectionally, corre-
sponding to different edge states with the positive slope. Although
magnetic field, and choose <math>\omega_s = \varepsilon_1 = 0.9g</math>. One can see in Fig. 4c
we study phenomena only associated to the effective magnetic
that the intensity distribution of the field undergoes a random-
field with <math>\phi = \pi/4</math>, the gauge field can be easily tuned in this
walk-like propagation in the synthetic honeycomb lattice, and
synthetic honeycomb lattice.
bulk of the lattice is excited. Next, we set <math>\phi = \pi/4</math> and introduce
5
COMMUNICATIONS PHYSICS | (2021)4:219 | https://doi.org/10.1038/s42005-021-00719-9 | www.nature.com/commsphys

## PDF page 6

ARTICLE

COMMUNICATIONS PHYSICS | https://doi.org/10.1038/s42005-021-00719-9

Fig. 4 Topological edge states with an effective magnetic ﬁeld. a The projected band structure of the honeycomb lattice in Fig. 1c along modulation phase
ϕ. The red dashed line refers to ϕ = π/4. ε is the frequency shift of the ﬁeld, and g is the effective hopping amplitude. b The projected band structure in
ﬁnite rings with ϕ = π/4, where kf is the wave vector reciprocal to the frequency axis, and Ω is the free spectral range. Bands labeled in red (green)
represents edge states on the right (left) boundary of the synthetic lattice. ε1, ε2, and ε3 label three different frequencies in the band structure. c The
simulated intensity distribution as a function of spatial dimension (x) and frequency dimension (f) at propagation time t = 20g−1 with the input ﬁeld having
frequency shift ωs = ε1 for the case ϕ = 0. Simulated intensity distributions at t = 20g−1 for the case ϕ = π/4 with the input ﬁeld having frequency shift ωs
being d ε1, e ε2, and f ε3, respectively. d is the horizontal distance between two sites with the same types in the synthetic lattice. The red arrow indicates the
m = 5th resonant frequency mode in the rightmost ring is excited. White arrows denote the unidirectional propagation.

Valley-dependent Lorentz force. Different from the effective
magnetic ﬁeld for photons introduced by modulation phases, a
pseudo magnetic ﬁeld can also be alternatively generated by
applying non-uniform strain in the honeycomb lattice57. In our
proposed synthetic honeycomb lattice, we can also easily simulate
the effective valley-dependent Lorentz force by varying modulation strength in each ring.
We consider a relatively large synthetic lattice composed of 56
pairs of rings with a range of x ∈ [0, 83d] and f ∈ [0, 59.5Ω]. We
emphasize that, although there are 112 rings considered in
simulations for better illustration, one does not require such a
large number of rings to realize the effective valley-dependent
Lorentz force in physics. For each modulator, we consider effective
modulation strengths having g2n−1 = [1 + η(3n − 42.75)]g and
g2n = [1 + η(3n − 41.25)]g, where η is a constant. Following the
relation between coupling strengths in a honeycomb lattice and
the effective gauge potential58–60, we obtain an effective gauge
potential Af(x) ∝ g(x) − κ and Ax = 0 in the vicinity of the Dirac
point, where the relation between n and x is used and κ is assumed
to be a constant. This effective gauge potential leads to a pseudo
magnetic ﬁeld B ∝ η and along the z direction. Therefore, one can
tune η by changing modulations strengths in rings to vary B in the
synthetic honeycomb lattice.
In simulations, we inject ﬁelds into multiple rings with different
frequency components to excite a Gaussian-shape wave packet
6

s4 ¼ e½ðxx0 Þ =ð15:5dÞ þðf f 3 Þ =Δ   ei½kx ðxx0 Þþkf ðf f 3 Þ in the synthetic
lattice, where Δ = 8.95Ω, x0 = 40d and f3 = 29.5Ω are the center
position of the Gaussian-shape wave packet. The phase information (kx, kf) is chosen to excite different states in the vicinity of the
Dirac point K or K 0 in the ﬁrst Brillouin zone. The simulated
motion of the center of the wave packet (xc, fc) is then plotted to
show the trajectory of the ﬁeld in the synthetic lattice, with the
deﬁnition of (xc, fc) can be found in Methods.
We ﬁrst excite the vicinity of Dirac point by a wave packet s4 with
(kx, kf) = (0, 4.4π/3Ω) which gives an initial group velocity pointing
toward the negative frequency axis. Without the pseudo magnetic
ﬁeld (η = 0), the wave packet of the ﬁeld propagates without
changing the direction and its trajectory is straight, as shown in
Fig. 5a. Instead, if η = 0.004, the motion of the wave packet is bent to
the clockwise side due to the pseudo magnetic ﬁeld. On the other
hand, if we excite the K 0 point with (kx, kf) = (0, − 4.4π/3Ω), the
motion of the wave packet is bent to the counter clockwise side under
pseudo magnetic ﬁeld in the synthetic lattice [Fig. 5b]. In Fig. 5c, d,
0
we also excite
pﬃﬃ the vicinity of Dirac points pKﬃﬃ and K with
(kx, kf) = (2.2 3π/3Ω, −2.2π/3Ω)
and
(2.2 3π/3Ω, 2.2π/3Ω),
respectively. One see that, with a non-zero η, trajectories of the ﬁeld
are bent towards different directions. The direction of the pseudo
magnetic ﬁeld is dependent on the valley in the synthetic honeycomb
lattice, which therefore results in the ﬁeld bending effect by the
effective valley-dependent Lorentz force.
2

2

2

2

COMMUNICATIONS PHYSICS | (2021)4:219 | https://doi.org/10.1038/s42005-021-00719-9 | www.nature.com/commsphys

## PDF page 7

COMMUNICATIONS PHYSICS | https://doi.org/10.1038/s42005-021-00719-9

ARTICLE

Fig. 5 Valley-dependent Lorentz force. The simulated trajectories of the center of the Gaussian-shape wave packet (xc, fc) at discrete times with time
0
interval δt = 0.5g−1, where g is the effective hopping amplitude. p
The
ﬃﬃﬃ lattice is excited by initial source in the
pﬃﬃﬃ vicinity of the Dirac point K or K with a
(kx, kf) = (0, 4.4π/3Ω), b (kx, kf) = (0, −4.4π/3Ω), c (kx, kf) = (2.2 3π/3Ω, −2.2π/3Ω), and d (kx, kf) = (2.2 3π/3Ω, 2.2π/3Ω). kx and kf are wave vectors
reciprocal to spatial and frequency axes, Ω is the free spectral range, d denotes the horizontal distance between two sites with the same types in the
synthetic lattice, and t is propagation time. The trajectory with a black solid (hollow) circle represents the motion of the wave packet in the case with
(without) the valley-dependent Lorentz force, which is projected into the spatial-frequency (x, f) plane with the varying color of circles representing the
center position in the synthetic lattice at different simulation times.

Discussion
The highly tunable parameters of modulated ring resonators are
of apparent signiﬁcance in our theoretical design for achieving the
synthetic honeycomb lattice, which can be realized in potential
experiments based on established platforms with ﬁber loops41–44,
and lithium niobate technologies45,61. For the ﬁber-based ring
resonator, the modulation frequency is ~10 MHz for a ﬁber
length of ~10 m. 2 × 2 ﬁber couplers with a high-contract splitting
ratio can be used to couple two rings. As for the on-chip lithium
niobate device, ﬁelds in nearby resonators are coupled through
the evanescent wave, where the modulation frequency can reach
~10 GHz when the ring radius is ~2–3 mm45. In our theoretical
proposal, the hopping amplitude gi as well as modulation phase ϕi
along the frequency dimension [Fig. 1c] can be individually tuned
by changing the external applied voltage on the electro-optic
modulator inside each ring. Moreover, lengths of rings can be
slightly altered by additional delay lines or thermal effects added
into ﬁber or on-chip rings if needed, which provides a way to
modify the effective on-site potential in each ring. Therefore, after
the one-dimensional coupled rings are fabricated, this design can
support simulating various graphene dynamics in two dimensions
by setting proper parameters in modulators, including phenomena we have shown previously in this paper. Our proposed synthetic honeycomb lattice hence potentially provides high
reconﬁgurability.

Here we study the proposal for constructing the honeycomb
lattice in the synthetic space. In spatial dimensions, there naturally exist various lattice structures with different symmetries,
which are possible to be simulated in the synthetic space. For
example, different lattice-geometry opportunities have been theoretically discussed in the cold-atom platform where Ramanassisted tunnelings have been used to construct the synthetic
dimension62. In photonics, however, most researches on synthetic
dimensions focus on lattices with the C4 symmetry33,47,63, while
constructing more complicated lattice structures is still lacking.
The proposed method that we use to build the synthetic honeycomb lattice through staggered resonances, therefore, offers a
different perspective for considering to create lattices with C3
symmetry64–67, such as triangular lattice and kagome lattice,
where valley degree of freedom naturally emerges, and hence
shows a way for further constructing other complicated lattice
structures with richer physics in photonics68,69.
In summary, we use an array of ring resonators composed by
two types of rings undergoing dynamic modulations to form a
two-dimensional honeycomb lattice in a synthetic space including
one spatial dimension and one frequency dimension. We theoretically demonstrate a highly re-conﬁgurable synthetic honeycomb lattice, which is ﬂexibly adjusted for achieving various
parameters by changing the external modulation details. It has
been used to simulate various phenomena including Klein

COMMUNICATIONS PHYSICS | (2021)4:219 | https://doi.org/10.1038/s42005-021-00719-9 | www.nature.com/commsphys

7

## PDF page 8

ARTICLE

COMMUNICATIONS PHYSICS | https://doi.org/10.1038/s42005-021-00719-9

tunneling, valley-dependent edge states, topological edge states
with an effective magnetic ﬁeld, and ﬁeld bending with the valleydependent Lorentz force. Follow our theoretical proposal, future
works can land on extending the honeycomb lattice to a threedimensional structure with synthetic dimensions and/or adding
optical nonlinearity to explore further light-manipulating
opportunities. Our work shows not only the capability for
simulating quantum phenomena, valley-dependent physics, and
topological states in a modulated ring system, but also points out
an alternative way to control the frequency information of light
with synthetic dimensions, which potentially enriches quantum
simulations of graphene physics with photonic technologies.

where In,m,α = ∣Cn,m,α∣2 or ∣Dn,m,α∣2, xn,m,α, and fn,m,α are the corresponding position
along the x axis and frequency dimension in the synthetic lattice, respectively.

Data availability
The data that support the ﬁndings of this study are available from the corresponding
author upon reasonable request.

Code availability
All codes used to produce the ﬁndings of this study are available from the corresponding
author upon request.

Received: 19 July 2021; Accepted: 7 September 2021;

Methods
The construction of the synthetic honeycomb lattice. In Fig. 1a, ring A (B)
supports a set of resonant modes with frequency ωm,A = ω0 + mΩ (ωm,B = ω0 − Ω/
2 + mΩ), which is plotted in blue (cyan) color. The effective hopping amplitude
between the nearby resonant modes a and b in two rings is formed through a twostep process: the resonant mode a in ring A couples to a corresponding nonresonant mode in ring B via evanescent-wave coupling, and then couples to the
resonant mode b in ring B via the dynamic modulation, vice versa. Hence the
effective coupling strength g is composed of both the evanescent-wave coupling
strength and the modulation strength in EOM70, and hence such connections
construct a synthetic frequency dimension in a pairs of modulated rings. The
construction of effective couplings between resonant modes in a pair of rings with
the AB type can also be generalized to the pair of rings with the BA type by mirror
symmetry [see the pair of rings labeled by n = 1 and α = 2 as an example in
Fig. 1c]. Therefore, in an array of pairs of rings arranged with alternate combinations AB and BA as shown in Fig. 1b, the spatially nearby resonant modes at the
same frequency can be coupled through the evanescent wave at the coupling
strength κ. Following this procedure, a synthetic honeycomb lattice can be constructed in a space shown in Fig. 1c with the longitudinal frequency dimension and
the horizontal spatial dimension.
Simulation method. We expand the ﬁeld inside each ring as




y
y
ψðtÞ ¼ ∑ C
n;m;α an;m;α þ Dn;m;α bn;m;α j0i;
n;m

An effective on-site potential induced by frequency shift. For a ring, the
resonant frequency for the mth resonant mode is ωm = ω0 + mΩ = ω0 + m ⋅ 2πvg/
L, where ω0 is a reference optical frequency and is much larger than Ω (which is
usually in the regime of GHz to THz). Without loss of generality, we can rewrite
the equation of resonant frequency as ωm = (M + m) ⋅ 2πvg/L, where M ≫ m is a
number orders of magnitudes larger than m. If we consider the length of the ring
changes to L0 ¼ L  δL (δL ≪ L), the new resonant frequency becomes ω0m ¼
ðM þ M  δL=L þ mÞ  2πvg =L ¼ ðM 0 þ m0 Þ  2πvg =L ¼ ω00 þ m0 Ω under the ﬁrstorder approximation, where m0 ¼ m þ roundðM  δL=LÞ and then M 0 is shifted by
a number smaller than 1. Hence, by changing the length of rings slightly, one is
possible to shift the reference frequency ω0 with a small amount, which results in
an effective on-site potential U  ω00  ω0 in each ring.
Deﬁnitions of xc and fc. We deﬁne central positions of the Gaussian-shape wave
packet in the synthetic lattice as

∑n;m;α f n;m;α I m;n;α
;
fc ¼
∑n;m;α I n;m;α

8

2.
3.
4.
5.

6.
7.
8.
9.

where γ is the coupling strength between the external waveguide and the ring
through evanescent wave. EC(D),m,α(t−) (EC(D),m,α(t+)) is the corresponding ﬁeld
component injected (collected) through the external waveguide, and t± = t + 0±.

∑n;m;α xn;m;α I m;n;α
;
∑n;m;α I n;m;α

1.

ð2Þ

at the mth mode in the correwhere Cn,m,α and Dn,m,α are the ﬁeld amplitude


sponding ring. Schrödinger equation i _ψðtÞ ¼ H ψðtÞ is then used in
simulations30. For different simulations, we take different source s to excite particular rings at speciﬁc modes, which we show details in the main text. The excitation process is done by coupling each ring with external waveguides where the
light can be injected. The ﬁeld amplitudes in rings can then also be read out
through waveguides. The coupling equation between the external waveguide and
the ring is
!
!
!
pﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ
Cn;m;α ðDn;m;α Þðt  Þ
Cn;m;α ðDn;m;α Þðt þ Þ
1  γ2
iγ
¼
; ð3Þ
pﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ

þ
ECðDÞ;m;α ðt Þ
ECðDÞ;m;α ðt Þ
iγ
1  γ2

xc ¼

References

10.
11.
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

ð4Þ

26.
27.

Castro Neto, A. H., Guinea, F., Peres, N. M. R., Novoselov, K. S. & Geim, A. K.
The electronic properties of graphene. Rev. Mod. Phys. 81, 109–162 (2009).
Das Sarma, S., Adam, S., Hwang, E. H. & Rossi, E. Electronic transport in twodimensional graphene. Rev. Mod. Phys. 83, 407–470 (2011).
Zhang, H. J. et al. Topological insulators in ternary compounds with a
honeycomb lattice. Phys. Rev. Lett. 106, 156402 (2011).
Kitagawa, K. et al. A spin–orbital-entangled quantum liquid on a honeycomb
lattice. Nature 554, 341–345 (2018).
Tarruell, L., Greif, D., Uehlinger, T., Jotzu, G. & Esslinger, T. Creating, moving
and merging Dirac points with a Fermi gas in a tunable honeycomb lattice.
Nature 483, 302–305 (2012).
Milićević, M. et al. Edge states in polariton honeycomb lattices. 2D Mater. 2,
034012 (2015).
Bahat-Treidel, O. et al. Klein tunneling in deformed honeycomb lattices. Phys.
Rev. Lett. 104, 063901 (2010).
Rechtsman, M. C. et al. Strain-induced pseudomagnetic ﬁeld and photonic
Landau levels in dielectric structures. Nat. Photonics 7, 153–158 (2013).
Ezawa, M. Spin valleytronics in silicene: quantum spin Hall-quantum
anomalous Hall insulators and single-valley semimetals. Phys. Rev. B 87,
155415 (2013).
Ozawa, T. & Carusotto, I. Anomalous and quantum Hall effects in lossy
photonic lattices. Phys. Rev. Lett. 112, 133902 (2014).
Jacqmin, T. et al. Direct observation of Dirac cones and a Flatband in a
honeycomb lattice for polaritons. Phys. Rev. Lett. 112, 116402 (2014).
Deng, F. et al. Valley-dependent beams controlled by pseudomagnetic ﬁeld in
distorted photonic graphene. Opt. Lett. 40, 3380–3383 (2015).
Dong, J. W., Chen, X. D., Zhu, H., Wang, Y. & Zhang, X. Valley photonic
crystals for control of spin and topology. Nat. Mater. 16, 298–302 (2017).
Jiang, X. et al. Direct observation of Klein tunneling in phononic crystals.
Science 370, 1447–1450 (2020).
Jamadi, O. et al. Direct observation of photonic Landau levels and helical edge
states in strained honeycomb lattices. Light Sci. Appl. 9, 144 (2020).
Noh, J., Huang, S., Chen, K. P. & Rechtsman, M. C. Observation of photonic
topological valley hall edge states. Phys. Rev. Lett. 120, 063902 (2018).
Guan, C. et al. Pseudospin-mediated optical spin–spin interaction in
nonlinear photonic graphene. Laser Photonics Rev. 13, 1800242 (2019).
Barik, S. et al. A topological quantum optics interface. Science 359, 666–668
(2018).
Lin, H. & Lu, L. Dirac-vortex topological photonic crystal ﬁber. Light Sci. Appl.
9, 202 (2020).
Yang, Z. Q., Shao, Z. K., Chen, H., Mao, X. R. & Ma, R. M. Spin-momentumlocked edge mode for topological vortex lasing. Phys. Rev. Lett. 125, 013903
(2020).
Zhang, Z. et al. Observation of edge solitons in photonic graphene. Nat.
Commun. 11, 1902 (2020).
Rechtsman, M. C. et al. Photonic Floquet topological insulators. Nature 496,
196–200 (2013).
Parappurath, N., Alpeggiani, F., Kuipers, L. & Verhagen, E. Direct observation
of topological edge states in silicon photonic crystals: Spin, dispersion, and
chiral routing. Sci. Adv. 6, eaaw4137 (2020).
Klembt, S. et al. Exciton-polariton topological insulator. Nature 562, 552–556
(2018).
Smirnova, D. et al. Third-Harmonic generation in photonic topological
metasurfaces. Phys. Rev. Lett. 123, 103901 (2019).
Yuan, L., Lin, Q., Xiao, M. & Fan, S. Synthetic dimension in photonics. Optica
5, 1396–1405 (2018).
Ozawa, T. & Price, H. M. Topological quantum matter in synthetic
dimensions. Nat. Rev. Phys. 1, 349–357 (2019).

COMMUNICATIONS PHYSICS | (2021)4:219 | https://doi.org/10.1038/s42005-021-00719-9 | www.nature.com/commsphys

## PDF page 9

COMMUNICATIONS PHYSICS | https://doi.org/10.1038/s42005-021-00719-9

28. Lustig, E. & Segev, M. Topological photonics in synthetic dimensions. Adv.
Opt. Photon. 13, 426–461 (2021).
29. Yuan, L., Dutt, A. & Fan, S. Tutorial: synthetic frequency dimensions in
dynamically modulated ring resonators. APL Photonics 6, 071102 (2021).
30. Yuan, L., Shi, Y. & Fan, S. Photonic gauge potential in a system with a
synthetic frequency dimension. Opt. Lett. 41, 741–744 (2016).
31. Ozawa, T., Price, H. M., Goldman, N., Zilberberg, O. & Carusotto, I. Synthetic
dimensions in integrated photonics: from optical isolation to fourdimensional quantum Hall physics. Phys. Rev. A 93, 043827 (2016).
32. Lin, Q., Sun, X. Q., Xiao, M., Zhang, S. C. & Fan, S. A three-dimensional
photonic topological insulator using a two-dimensional ring resonator lattice
with a synthetic frequency dimension. Sci. Adv. 4, eaat2774 (2018).
33. Lustig, E. et al. Photonic topological insulator in synthetic dimensions. Nature
567, 365–360 (2019).
34. Yu, D., Yuan, L. & Chen, X. Isolated photonic ﬂatband with the effective
magnetic ﬂux in a synthetic space including the frequency dimension. Laser
Photonics Rev. 14, 2000041 (2020).
35. Yang, Z. et al. Mode-locked topological insulator laser utilizing synthetic
dimensions. Phys. Rev. X 10, 011059 (2020).
36. Song, Y. et al. Two-dimensional non-Hermitian skin effect in a synthetic
photonic lattice. Phys. Rev. Appl. 14, 064076 (2020).
37. Dutt, A., Minkov, M., Williamson, I. A. D. & Fan, S. Higher-order topological
insulators in synthetic dimensions. Light Sci. Appl. 9, 131 (2020).
38. Zhang, W. & Zhang, X. Quadrupole topological phases in the zerodimensional optical cavity. EPL 131, 24004 (2020).
39. Nemirovsky, L., Cohen, M., Lumer, Y., Lustig, E. & Segev, M. Synthetic-space
photonic topological insulators utilizing dynamically invariant structure. Phys.
Rev. Lett. 127, 093901 (2021).
40. Poo, Y., Wu, R. X., Lin, Z., Yang, Y. & Chan, C. T. Experimental realization of
self-guiding unidirectional electromagnetic edge states. Phys. Rev. Lett. 106,
093903 (2011).
41. Dutt, A. et al. Experimental band structure spectroscopy along a synthetic
dimension. Nat. Commun. 10, 3122 (2019).
42. Dutt, A. et al. A single photonic cavity with two independent physical
synthetic dimensions. Science 367, 59–64 (2020).
43. Li, G. et al. Dynamic band structure measurement in the synthetic space. Sci.
Adv. 7, eabe4335 (2021).
44. Wang, K. et al. Generating arbitrary topological windings of a non-Hermitian
band. Science 371, 1240–1245 (2021).
45. Hu, Y., Reimer, C., Shams-Ansari, A., Zhang, M. & Loncar, M. Realization of
high-dimensional frequency crystals in electro-optic microcombs. Optica 7,
1189 (2020).
46. Ozawa, T. et al. Topological photonics. Rev. Mod. Phys. 91, 015006 (2019).
47. Segev, M. & Bandres, M. A. Topological photonics: where do we go from here?
Nanophotonics 10, 425–434 (2021).
48. Pérez, D. et al. Multipurpose silicon photonics signal processor core. Nat.
Commun. 8, 636 (2017).
49. Nakajima, M., Tanaka, K. & Hashimoto, T. Scalable reservoir computing on
coherent linear photonic processor. Commun. Phys. 4, 20 (2021).
50. Feng, L. T. et al. On-chip coherent conversion of photonic quantum entanglement
between different degrees of freedom. Nat. Commun. 7, 11985 (2016).
51. Liu, C. et al. Two-dimensional materials for next-generation computing
technologies. Nat. Nanotechnol. 15, 545–557 (2020).
52. Dreisow, F. et al. Klein tunneling of light in waveguide superlattices. EPL 91,
10008 (2012).
53. Ni, X. et al. Spin-and valley-polarized one-way Klein tunneling in photonic
topological insulators. Sci. Adv. 4, eaap8802 (2018).
54. Shan, Q., Yu, D., Li, G., Yuan, L. & Chen, X. One-way topological states along
vague boundaries in synthetic frequency dimensions including group velocity
dispersion. PIER 169, 33–43 (2020).
55. Turner, A. C. et al. Tailored anomalous group-velocity dispersion in silicon
channel waveguides. Opt. Express 14, 4357–4365 (2006).
56. Yuan, L. et al. Photonic gauge potential in one cavity with synthetic frequency and
orbital angular momentum dimensions. Phys. Rev. Lett. 122, 083903 (2019).
57. Low, T. & Guinea, F. Strain-induced pseudomagnetic ﬁeld for novel graphene
electronics. Nano Lett. 10, 3551–3554 (2010).
58. Vozmediano, M. A. H., Katsnelson, M. I. & Guinea, F. Gauge ﬁelds in
graphene. Phys. Rep. 496, 109–148 (2010).
59. de Juan, F., Cortijo, A., Vozmediano, M. A. H. & Cano, A. Aharonov-Bohm
interferences from local deformations in graphene. Nat. Phys. 7, 810–815 (2011).
60. Prabhakar, S., Nepal, R., Melnik, R. & Kovalev, A. A. Valley-dependent
Lorentz force and Aharonov-Bohm phase in strained graphene p-n junction.
Phys. Rev. B 99, 094111 (2019).

ARTICLE

61. Zhang, M., Wang, C., Cheng, R., Shams-Ansari, A. & Lončar, M. Monolithic
ultra-high-Q lithium niobate microring resonator. Optica 4, 1536–1537 (2017).
62. Suszalski, D. & Zakrzewski, J. Different lattice geometries with a synthetic
dimension. Phys. Rev. A 94, 033602 (2016).
63. Ozawa, T. & Price, H. M. Topological quantum matter in synthetic
dimensions. Nat. Rev. Phys. 1, 349–357 (2019).
64. Zandbergen, S. R. & de Dood, M. J. A. Experimental observation of strong
edge effects on the pseudodiffusive transport of light in photonic graphene.
Phy. Rev. Lett. 104, 043903 (2010).
65. Struck, J. et al. Quantum simulation of frustrated classical magnetism in
triangular optical lattices. Science 333, 996–999 (2011).
66. Schulz, S. A., Upham, J., O’Faolain, L. & Boyd, R. W. Photonic crystal slow
light waveguides in a kagome lattice. Opt. Lett. 42, 3243–3246 (2017).
67. Li, M. et al. Higher-order topological states in photonic kagome crystals with
long-range interactions. Nat. Photonics 14, 89–94 (2019).
68. Chern, G. & Saxena, A. PT-symmetric phase in kagome-based photonic
lattices. Opt. Lett. 40, 5806–5809 (2015).
69. Maimaiti, W., Dietz, B. & Andreanov, A. Microwave photonic crystals as an
experimental realization of a combined honeycomb-kagome lattice. Phys. Rev.
B 102, 214301 (2020).
70. Yuan, L., Xiao, M., Lin, Q. & Fan, S. Synthetic space with arbitrary dimensions
in a few rings undergoing dynamic modulation. Phys. Rev. B 97, 104105
(2018).

Acknowledgements
We greatly thank Prof. Shanhui Fan for fruitful discussions. The research is supported by
the National Natural Science Foundation of China (11974245), National Key R&D
Program of China (2017YFA0303701), Shanghai Municipal Science and Technology
Major Project (2019SHZDZX01), Natural Science Foundation of Shanghai
(19ZR1475700), and China Postdoctoral Science Foundation (2020M671090). This work
is also partially supported by the Fundamental Research Funds for the Central Universities. L.Y. acknowledges support from the Program for Professor of Special
Appointment (Eastern Scholar) at Shanghai Institutions of Higher Learning. X.C. also
acknowledges the support from Shandong Quancheng Scholarship (00242019024).

Author contributions
L.Y. initiated the idea. D.Y. and L.Y. performed simulations. D.Y., G.L., M.X., and L.Y.
discussed the results. D.Y., G.L., and L.Y. wrote the draft. D.Y., G.L., M.X., D.-W.W.,
Y.W., L.Y., and X.C. revised the manuscript and contributed to scientiﬁc discussions of
the manuscript. L.Y. and X.C. supervised the project.

Competing interests
The authors declare no competing interests.

Additional information
Correspondence and requests for materials should be addressed to Luqi Yuan.
Peer review information Communications Physics thanks the anonymous reviewers for
their contribution to the peer review of this work.
Reprints and permission information is available at http://www.nature.com/reprints
Publisher’s note Springer Nature remains neutral with regard to jurisdictional claims in
published maps and institutional afﬁliations.

Open Access This article is licensed under a Creative Commons
Attribution 4.0 International License, which permits use, sharing,
adaptation, distribution and reproduction in any medium or format, as long as you give
appropriate credit to the original author(s) and the source, provide a link to the Creative
Commons license, and indicate if changes were made. The images or other third party
material in this article are included in the article’s Creative Commons license, unless
indicated otherwise in a credit line to the material. If material is not included in the
article’s Creative Commons license and your intended use is not permitted by statutory
regulation or exceeds the permitted use, you will need to obtain permission directly from
the copyright holder. To view a copy of this license, visit http://creativecommons.org/
licenses/by/4.0/.
© The Author(s) 2021

COMMUNICATIONS PHYSICS | (2021)4:219 | https://doi.org/10.1038/s42005-021-00719-9 | www.nature.com/commsphys

9
