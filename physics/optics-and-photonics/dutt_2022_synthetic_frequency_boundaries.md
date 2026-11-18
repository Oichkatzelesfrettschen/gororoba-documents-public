Source: https://doi.org/10.1038/s41467-022-31140-7
PDF sha256: fc7d9c1ebf588e5a9b00e003af4d73836f86d18f1da918710f0acd80018b1fc8
License: https://creativecommons.org/licenses/by/4.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of dutt_2022_synthetic_frequency_boundaries.pdf

Transcription of `dutt_2022_synthetic_frequency_boundaries.pdf` in this directory, 8 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-8 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

ARTICLE
https://doi.org/10.1038/s41467-022-31140-7

OPEN

Creating boundaries along a synthetic frequency
dimension

1234567890():,;

Avik Dutt 1,2, Luqi Yuan
Shanhui Fan 1 ✉

3, Ki Youl Yang

1, Kai Wang

1, Siddharth Buddhiraju

1, Jelena Vučković

1 &

Synthetic dimensions have garnered widespread interest for implementing high dimensional
classical and quantum dynamics on low-dimensional geometries. Synthetic frequency
dimensions, in particular, have been used to experimentally realize a plethora of bulk physics
effects. However, in synthetic frequency dimension there has not been a demonstration of a
boundary which is of paramount importance in topological physics due to the bulk-edge
correspondence. Here we construct boundaries in the frequency dimension of dynamically
modulated ring resonators by strongly coupling an auxiliary ring. We explore various
effects associated with such boundaries, including conﬁnement of the spectrum of light,
discretization of the band structure, and the interaction of boundaries with one-way chiral
modes in a quantum Hall ladder, which exhibits topologically robust spectral transport.
Our demonstration of sharp boundaries fundamentally expands the capability of exploring
topological physics, and has applications in classical and quantum information processing in
synthetic frequency dimensions.

1 Ginzton Laboratory and Department of Electrical Engineering, Stanford University, Stanford, CA 94305, USA. 2 Department of Mechanical Engineering, Institute
for Physical Science and Technology, University of Maryland, College Park, MD 20742, USA. 3 State Key Laboratory of Advanced Optical Communication
Systems and Networks, School of Physics and Astronomy, Shanghai Jiao Tong University, Shanghai 200240, China. ✉email: shanhui@stanford.edu

NATURE COMMUNICATIONS | (2022)13:3377 | https://doi.org/10.1038/s41467-022-31140-7 | www.nature.com/naturecommunications

1

## PDF page 2

ARTICLE

T

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-022-31140-7

he concept of synthetic dimensions1–3, whereby various
degrees of freedom of atoms or photons are used to mimic
spatial dimensions, is of signiﬁcant recent interest for
simulating high-dimensional phenomena on systems with fewer
geometric dimensions. Synthetic dimensions have been formed
by coupling states labeled by degrees of freedom such as spin1,4,
frequency5,6, orbital angular momentum (OAM)7, time bins8–10
or transverse spatial supermodes11. Many interesting physical
effects, including nontrivial topological phenomena and effective
gauge ﬁelds for neutral ultracold atoms or photons, have been
realized in synthetic dimensions.
Speciﬁcally for topological phenomena, constructing a sharp
boundary in the synthetic dimension is of central importance. An
essential concept in topological physics is the bulk-edge correspondence, which relates the existence and properties of edge
modes in a ﬁnite lattice to the quantized topological invariant of
the corresponding bulk (inﬁnite) lattice. For Hermitian systems,
examples of bulk-edge correspondence include the one-way chiral
edge states at the boundary of a Chern insulator12, the zeroenergy edge modes of a Su-Schrieffer-Heeger model13, and the
recently discovered corner modes of a higher-order topological
insulator14–16. Moreover, the bulk-edge correspondence has also
been generalized to non-Hermitian systems, leading to intriguing
phenomena such as the non-Hermitian skin effect17–20. Creating
a boundary in the synthetic dimension is essential for further
exploration of such phenomena in synthetic space. In addition,
the creation of boundaries in synthetic dimensions is important
for applications such as implementing arbitrary linear transformations for frequency conversion, quantum circuits, and photonic neural networks21.
A prominent approach to create synthetic dimensions is to use
the frequency modes of a ring resonator. Synthetic frequency
dimensions have enabled experimental demonstrations of a plethora of bulk physical effects. For Hermitian systems, examples of
these effects include Bloch oscillations22–25, effective electric and
magnetic gauge ﬁelds26–30, spin-orbit coupling and consequent
spin-momentum locking27, complex long-range coupling31,32, and
chiral currents originating from the nontrivial topology of the
quantum Hall effect27. For non-Hermitian systems, nontrivial
eigenvalue topology such as topological winding or braiding of the
energy bands have also been recently observed in frequency
dimensions33,34. However, experimentally probing the edge implications of these bulk topological phenomena has remained an open
challenge in synthetic frequency dimensions. Unlike systems in real
space, synthetic lattices created using frequency modes typically do
not have a well-deﬁned boundary. In the absence of boundaries or
defects, the robustness of light transport35, which is one of the
hallmarks of topological phenomena, has not been observed along
the frequency axis.
In this paper, we provide an experimental demonstration for
constructing boundaries in synthetic frequency dimensions. Previous theoretical works have investigated synthetic-space boundary
effects by assuming sharp5 or gradual36 changes in the groupvelocity dispersion of the waveguide forming the ring resonator, by
strongly coupling an auxiliary ring21, or by including memory
elements37. Here we experimentally realize the approach of coupling to auxiliary ring resonators. We observe that an excitation
within the ﬁnite lattice stays conﬁned between the boundaries in
synthetic space, resulting in the discretization of the band structure
in reciprocal space. We also implement boundaries in a synthetic
quantum Hall ladder geometry and demonstrate one-way propagation of topological chiral edge states that are immune to back
reﬂection despite the presence of a boundary, thus constituting an
observation of topologically robust transport of light along
the frequency axis. With the added functionality of creating
sharp edges, we anticipate the observation of higher-dimensional
2

boundary phenomena that have been beyond the purview of realspace or synthetic-space topological photonics.
Results
Creation of boundaries in one dimension. Consider a single
ring resonator of length L0 made of a waveguide with group
velocity vg (Fig. 1a). In the absence of group velocity dispersion,
the ring supports cavity modes equispaced in frequency by the
free-spectral range (FSR) ΩR = 2πvg/L0. To excite these modes we
couple the ring with an external waveguide at an amplitude
coupling ratio γ0. The resulting transmission spectrum, assuming
that all the ring modes are critically coupled with an internal loss
rate equal to the external coupling loss rate, is shown in Fig. 1c.
The spectrum features a periodic array of resonant dips equally
spaced by the FSR. These modes can be coupled to form a onedimensional (1D) synthetic frequency lattice by electro-optically
modulating the refractive index of a small portion of the ring at a
modulation frequency ΩM = ΩR5,6,32. The Hamiltonian for such a
system is32,38,
M

H ¼ J ∑ bym bmþ1 þ H:c:
m¼M

ð1Þ

where bm ðbym Þ is the annihilation (creation) operator for a mode
at frequency ωm = ω0 + mΩR. For a single ring with ω0 ≫ ΩR, a
very large number of modes (M > 100) can be coupled along the
synthetic frequency dimension, as demonstrated experimentally
in refs. 25,32. Thus a single modulated ring closely approximates
the bulk behavior (M → ∞) of a lattice.
To truncate such a lattice and create boundaries, we couple an
auxiliary ring resonator of a smaller length La < L0, corresponding
to a larger FSR ΩR,a = 2πvg/La (Fig. 1b). Here we have assumed
that the auxiliary ring is made of a waveguide with the same
group velocity as the main ring, and is coupled to the main ring
via a directional coupler with an amplitude coupling coefﬁcient
γa. Note that similar geometries have previously been used
for optical communications, ﬂat-band lattices, reconﬁgurable
frequency conversion, and demonstrating coupled-resonator
induced transparency39–45.
As an illustration, Fig. 1d shows the spectral positions of the
main cavity and auxiliary ring modes for N = L0/La = 6 in the
absence of modulation. The corresponding transmission
spectrum is plotted in Fig. 1e. Near the frequencies where the
resonances from the two rings align, if γa > γ20 =2, a splitting is
induced (Fig. 1f). Here γ20 is the power splitting ratio of the
directional coupler between the input-output waveguide and
the main ring. Unlike the spectrum in Fig. 1c, the spectrum here
in Fig. 1e is no longer periodic with respect to translation by ΩR
along the frequency axis.
When the modulation is again introduced in the main ring
with a modulation frequency ΩM = ΩR, the modulation can
induce the transition between some of the modes. Speciﬁcally in
Fig. 1e, the green arrows represent the allowed modulationinduced couplings along the frequency dimension, whereas the
red crosses represent inhibition of the coupling to modes that are
perturbed by the auxiliary ring. A series of several ﬁnite lattices
are formed, which are separated by the split resonances induced
by the auxiliary ring. The presence of the auxiliary ring thus can
introduce a sharp boundary in the synthetic dimension.
Characterization of the unmodulated resonators. To experimentally characterize the resonator in the absence of modulation,
we measure the transmission spectra (Fig. 2) in an experimental
realization of the setup shown in Fig. 1a. The details of the
experiments, which are implemented using ﬁber rings, are provided in Supplementary Information Section I. Without the

NATURE COMMUNICATIONS | (2022)13:3377 | https://doi.org/10.1038/s41467-022-31140-7 | www.nature.com/naturecommunications

## PDF page 3

ARTICLE

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-022-31140-7

a

b

a

b

c

c

d

e

f

Fig. 1 Ring resonator and its transmission spectrum with and without an
auxiliary ring. Schematic of a static ring resonator (a) and its simulated
transmission T (c). The frequencies of the ring's modes are indicated in (d)
with blue lines. b Ring with a coupled auxiliary resonator (red), and its
corresponding transmission spectrum in the absence of modulation (e).
The frequencies of the auxiliary ring's modes are indicated in (d) with red
lines. f Shows a zoom-in around the mode of the auxiliary resonator that is
aligned to a mode of the main ring. c, e, f are calculated numerically using a
scattering matrix method with a power splitting ratio of γ20 ¼ 0:01. For
illustrative purposes, a propagation loss rate α0 in the main ring is chosen
to critically couple it to the waveguide, expðα0 L0 Þ ¼ 1  γ20 ¼ 0:99. The
auxiliary ring is assumed to be lossless. The red crosses in (e) indicate that
the modulation at the FSR cannot couple the split modes to the rest of the
lattice as they are not aligned to the frequency grid of the main ring. EOM
electro-optic modulator.

auxiliary ring, the transmission features a set of resonant dips,
with minimum transmission T min  0:7 that are similar for all
the dips. These dips correspond to the resonances of the main
ring. The frequency spacing of the nearest resonances as a

Fig. 2 Measurement of transmission through a static ring resonator and
frequency separation of modes. Transmission spectrum without (a) and
with (b) an auxiliary ring resonator coupled. ΩR = 5.35 MHz in (a), (c),
ΩR = 5.25 MHz in (b). L0 = 38.6 m, L0/La ≈ 12, γ0 = 0.1, γa/γ0 = 5. Inset in
(b) shows a numerical calculation of the transmission spectrum based on a
scattering matrix model, similar to Fig. 1d, but with ﬁnite roundtrip losses in
both the main ring and the auxiliary ring of 5%. c Frequency difference
between adjacent resonances of the main ring without an auxiliary ring
from (a) (blue), and with an auxiliary ring from (b) (orange), as a function
of the order of the resonances.

function of the order of resonances is plotted as the blue line in
Fig. 2c. We see that the frequency spacing is nearly a constant.
In the presence of coupling to the auxiliary ring, there is a
marked increase in T min near the main cavity modes that are
aligned to the auxiliary ring modes (Fig. 2b). The increase in
T min is in accordance with scattering matrix simulations
including a loss in the auxiliary ring (inset of Fig. 2b), and this
loss was ignored in Fig. 1d, e for simplicity. Around the resonant frequencies of the auxiliary ring, we see that the resonances of the coupled system are no longer equally spaced
(orange line in Fig. 2c). In addition, for the coupled system, the
frequency spacings between modes far away from the resonances of the auxiliary ring, which we deﬁne as the FSR of our
coupled ring system, is smaller as compared to the FSR of the
main ring by itself (Fig. 2c, see Supplementary Section II for an
analytical derivation of this effect).
Measurement of boundary effects in 1D lattice space. For the
remainder of the paper, we will consider a modulated resonator.
We ﬁrst demonstrate the effect of a boundary created by the
auxiliary ring by measuring the steady-state intensity distribution
in the synthetic frequency dimension (Fig. 3) in the presence of
modulation. We excite the system at a frequency ωin near one of
the resonances of the main ring, the order of which is denoted by
m0. ωin is gradually swept, and the detuning Δω ¼ ωin  ωm0
forms the vertical axis in Fig. 3a, b, d–f. At each input frequency,
the frequency-lattice distribution of the steady-state cavity ﬁeld

NATURE COMMUNICATIONS | (2022)13:3377 | https://doi.org/10.1038/s41467-022-31140-7 | www.nature.com/naturecommunications

3

## PDF page 4

ARTICLE

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-022-31140-7

b

d

e

c
(Arb. Units)

a

f

Fig. 3 Amplitude distribution in frequency lattice space. a, b Without and (d–f) with an auxiliary ring, corresponding to inﬁnite and ﬁnite lattices
respectively. a, d, f are experimentally measured heterodyne spectra. b, e are obtained from simulations based on a Floquet scattering matrix analysis.
c Blue (inﬁnite) and green (ﬁnite) curves represent line cuts through the raw heterodyne data at Δω ≈ 0. Dots represent line cuts through respective
simulated spectra in panels (b, e) respectively. The inﬁnite lattice data without an auxiliary ring is vertically offset by 4 units. f The heterodyne spectra
similar to (d) but over a much larger range of input laser detuning Δω > ΩR, thus exciting various lattice sites between the two boundaries. The breakdown
of discrete modal translational symmetry is evident, as the response changes depending on which frequency site is excited. Due to reﬂection from the
boundaries, fringes are visible in (d–f). Here the frequency mode axis (m − m0) is measured with respect to the input laser frequency. Arb. Units
arbitrary units.

is obtained from a heterodyne measurement of the transmitted
ﬁeld46. This frequency sideband number is denoted by m − m0
along the horizontal axis in Fig. 3.
In the absence of the auxiliary ring, the transmitted ﬁeld
contains a large number of sidebands (Fig. 3a). This experimental
data matches well with the simulated spectrum in Fig. 3b which
was calculated using a Floquet scattering matrix analysis. The
steady-state ﬁeld intensity of the m-th sideband away from the
input falls off exponentially as expðjm  m0 j=τ p JÞ (see Fig. 3c
bottom), for large m − m025, where τp and J are the ring photon
lifetime and the modulation strength respectively.
On the other hand, when the auxiliary ring is coupled to the
main ring, the output ﬁeld contains a far smaller number of
sidebands. This indicates that within the ring, the only modes
excited are those that lie between the two boundaries along the
frequency axis (experiment: Fig. 3d, simulations: Fig. 3e). We also
observe interference fringes created by reﬂections from the
boundaries. Note that the strengths of the fringes increase with an
increase in the modulation-induced coupling strength, since light
is able to traverse along the frequency axis for longer distances
before getting dissipated. However, the strong conﬁnement of
light to within the boundaries is preserved as long as the splitting
induced by the auxiliary ring resonator is larger than 2J. Figure 3f
illustrates the spectra upon exciting various lattice sites within the
two boundaries. This result was obtained by sweeping the input
laser detuning over a large range Δω ≫ ΩR. Since the measured
heterodyne spectrum is always referenced to the input laser
frequency mode m0, we observe a shift of the output spectrum
towards lower frequency sidebands as m0 increases.
Measurement of 1D boundary effects in reciprocal space. An
inﬁnite lattice that obeys discrete translational symmetry can be
characterized by a conserved continuous quantum number, the
Bloch quasimomentum k ∈ [0, 2π), which labels the bulk properties in reciprocal space. For each k, one or more continuous
bands are formed which correspond to the eigenenergy spectrum
of the inﬁnite lattice. In the frequency synthetic dimension, the
wavevector along the frequency axis corresponds to a time variable. We have previously demonstrated a synthetic-space band
4

a

b

c

d

Fig. 4 Band structure of bulk and ﬁnite lattices in one dimension.
a Measured band structure for a bulk lattice without any boundary, that
is, without coupling to an auxiliary ring. A continuous band is observed.
b Experimentally measured band structure from the time-resolved
transmission of the main ring, when an auxiliary ring is coupled.
A discrete band structure is seen, due to the effect of a boundary
creating a ﬁnite lattice. c Floquet simulations using a full scattering
matrix analysis of the structure in Fig. 1a, showing agreement with the
experimental measurements in (b). d Result of a tight-binding Floquet
analysis of Eq. (1), for a ﬁnite lattice with M = 4 (9 sites). The agreement
of (d), which is not based on a modulated ring system but a general
tight-binding lattice, establishes that a boundary can be realized along
the synthetic frequency dimension using an auxiliary ring. J/ΩR = 0.12.

structure spectroscopy technique32. In this technique, we scan the
input frequency of a continuous-wave laser. For each frequency,
after the transient dissipates, we measure the transmission
intensity as a function of time. Since the time corresponds to the
wavevector k along the synthetic frequency dimension, the
resulting two-dimensional plot of transmission as a function of
frequency and wavevector then provides a measure of the
bandstructure. An example of such a measurement, for our system in the absence of the auxiliary ring, is shown in Fig. 4a. The
locations of the peaks in the frequency-wavevector space closely
match the band structure of a one-dimensional tight-binding
model with nearest-neighbor coupling.

NATURE COMMUNICATIONS | (2022)13:3377 | https://doi.org/10.1038/s41467-022-31140-7 | www.nature.com/naturecommunications

## PDF page 5

ARTICLE

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-022-31140-7

b

…
,

a

…

,

EOM

0
d

c

f

e
0.75

(Arb. Units)

0.25

-4 -3 -2 -1 0

h

g
-2 -1 0

0.25

< 0.1

i

1

1

0.75

j

0

X

1

0 1 2

2

X

3

Fig. 5 Interaction of quantum Hall ladder with boundaries. a Two-leg quantum Hall ladder was constructed using two coupled rings, both of which are
modulated with a phase difference ϕ between the two modulations. The auxiliary ring (red) introduces a boundary in the synthetic frequency dimension of
the left ring, corresponding to a ﬁnite lower leg of the ladder in (b). b Shows a lattice model for (a). Coupling constants J and K are determined by the
modulation amplitude in (a) and the evanescent coupling rate between the rings. c Schematic of the lattice excitation and its dynamics along the frequency
dimension for the trivial case ϕ = 0. The wave propagates along the frequency axis, reaches the boundary, and gets reﬂected, forming fringes in the steadystate intensity distribution. d Bulk band structure of the ladder for ϕ = 0, showing symmetric bands with no chirality. e Measured lattice space occupation,
showing fringes due to reﬂection from the boundary and bidirectional propagation. The fringes are clearly visible in the blue line cut in (f) taken at Δω/
ΩR = 0.11. Purple dots in (f) represent Floquet scattering matrix simulation results. g–i Same as (c–e) but for the nontrivial topology case ϕ = π/2. Chiral
one-way modes are visible in (h) [colorbar represents the strength of localization on the ladder's lower leg, nL(k) = ∣bL(k)∣2]. Pink shaded regions depict
energies with one-way modes, as veriﬁed experimentally in (i). Back-reﬂection is inhibited (schematics in (g)), leading to unidirectional propagation and no
fringes despite the presence of a boundary, as visible in the orange line cut in (f). Red dots are simulation results. j Same as i but over a larger range of input
laser detuning, showing the steady state for exciting various frequency sites. The boxed region corresponds to (i), near Δω = 0. For Δω/ΩR near {−3, −2,
−1, 1}, the input mode m0 is also shifted by the same amount. y-axis labels in (e) and (i) represent Δω/ΩR and are shared with (d) and (h).

We repeat the same measurement in the presence of the
auxiliary ring (Fig. 4b). We see strong excitation of the system
only at a discrete set of frequencies, as expected since the presence
of the two boundaries results in a discrete set of eigenstates. For
each of these eigenstates, the wavevector components spread over
a range, centered at approximately where the wavevector would
be at the same frequency for the inﬁnite system. The experimental
results in Fig. 4b agree excellently with numerical simulation
results shown in Fig. 4c based on a Floquet scattering matrix
analysis of the coupled ring system. Moreover, the numerical
results indicate that the discrete eigenfrequencies that we observe
in Fig. 4b agree with tight-binding simulations (Fig. 4d) where
open boundaries are imposed on the two ends of a ﬁnite lattice,
providing further evidence of a sharp boundary that we create.
Demonstration of boundary effects in a quantum Hall ladder.
We now demonstrate the effect of boundary on a topologically
nontrivial system, the two-leg quantum Hall ladder47, and show
how it enables us to observe topologically robust transport of light
along the frequency axis. To construct a two-leg quantum Hall
ladder, we use a setup schematically shown in Fig. 5a, where we
couple a pair of main ring resonators. The main ring on the left is

in addition coupled to an auxiliary ring. We ensure that the FSR
of the main ring on the right matches the FSR of the coupled
system consisting of the main ring on the left together with the
auxiliary ring. We modulate both of the main rings at a frequency
ΩM = 2π ⋅ 5.28 MHz, which matches the FSR, with a relative
phase difference ϕ in the modulations on the two rings5. The
resulting Hamiltonian then describes a two-leg quantum Hall
ladder4,27,47 (Fig. 5b):
H2 ¼ J

NL

∑

m¼N L

þK

bym;L bmþ1;L þ J

NL

∑

m¼N L

NR

∑

m¼N R

bym;R bmþ1;R eiϕ
ð2Þ

bym;L bm;R þ H:c:

where NL and NR represent the number of frequency modes in the
left and right legs of the ladder respectively, and NL < NR due to
the presence of the auxiliary ring that couples to the main ring on
the left. J is the modulation-induced hopping along the synthetic
frequency dimension. K represents the coupling between the two
legs of the ladder, determined by the splitting ratio of the directional coupler that couples the two main rings together. The
model in Eq. (2) exhibits a uniform effective magnetic ﬂux ϕ

NATURE COMMUNICATIONS | (2022)13:3377 | https://doi.org/10.1038/s41467-022-31140-7 | www.nature.com/naturecommunications

5

## PDF page 6

ARTICLE

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-022-31140-7

permeating each square plaquette of the lattice. For ϕ ≠ 0, π, timereversal symmetry is broken; such a model then supports oneway chiral states on each leg which are immune to back reﬂections from the boundary or corner (Fig. 5g, h). This one-way
nature derives from a parent 2D quantum Hall insulator
which manifests strong topological protection47,48. Thus, the
setup allows us to study the interaction of boundaries with
the topologically protected one-way chiral modes in a quantum
Hall ladder.
To demonstrate the effect of the boundary as induced by the
auxiliary ring, we excite the left main ring in the setup as shown
in Fig. 5a. We choose the excitation frequency to match one of the
lattice sites away from the boundary (Fig. 5c and g). In the case of
ϕ = 0, the band structure for an inﬁnite two-leg system is shown
in Fig. 5d. Since the system has time-reversal symmetry, the
eigenstates equally occupy the left and the right legs and the
system does not exhibit any chiral behavior. Consequently, with
the excitation as shown in Fig. 5c, we expect that the generated
ﬁeld will propagate to both sides of the excitation site. Also, we
expect to see interference fringes between the site of excitation
and the boundaries. In Fig. 5e, we show the experimental results
for this case where we measure the spectrum of the transmitted
light via heterodyne detection (see Methods). We indeed observe
that the output ﬁeld contains strong components on both sides of
the excitation site m = m0. In Fig. 5f, we plot the amplitude at
various lattice sites for Δω/ΩR = 0.11. We observe interference
fringes due to the presence of the boundaries (indicated by green
vertical lines), as exempliﬁed by the dips at m − m0 = ±2.
In the case of ϕ = π/2, the band structure for the inﬁnite
system is shown in Fig. 5h. Since the system breaks time-reversal
symmetry, the eigenstates show asymmetry in occupation
between the left leg and the right leg, as illustrated in Fig. 5h
where the color gradient shows the projection of the eigenstate
on the left leg. Hence, with the excitation shown in Fig. 5g where
the left leg is excited, we expect that the generated ﬁeld will
propagate to higher frequencies for the lower band, and to lower
frequencies for the upper band, as determined by the sign of the
group velocities of the chiral modes in Fig. 5h. Also, we do not
expect to see interference fringes between the site of excitation
and the boundaries, since the one-way nature of the chiral modes
should suppress back reﬂection from the boundaries (schematics
in Fig. 5g). In Fig. 5i, we show the experimental results for this
case where we measure the spectrum of the transmitted light via
heterodyne detection. Strikingly different from Fig. 5e, we indeed
observe that the output ﬁeld contains frequency components
almost exclusively for modes to the left of the excitation
(m − m0 ≤ 0) for the upper band, in the one-way detuning range
shaded in pink in Fig. 5h. The direction of frequency conversion
switches for the lower band. In Fig. 5f, we plot the experimentally
measured amplitude at various lattice sites as the orange curve,
which agrees well with Floquet scattering matrix simulations
(red dots). The one-way nature, as well as the absence of
interference fringes, are borne out in this amplitude distribution
in frequency lattice space. Fig. 5j plots the amplitude distribution
for a wide range of detuning Δω, corresponding to the excitation
of different lattice sites m0 along the frequency dimension.
We observe that the topological robustness of light transport, as
evidenced by the one-way nature and the lack of fringes, persists
as we excite modes with different distances from the boundary.
Note that the persistence of one-way propagation in the two-leg
ladder limit attests to the topological robustness of the full 2D
quantum Hall lattice independent of the boundary along the
frequency axis. This is because the ladder preserves the modal
structure of the edge states of the full 2D lattice in spite of the
removal of all the bulk sites from the full 2D lattice, as predicted
theoretically in ref. 47.
6

Discussion
We have demonstrated the construction of sharp boundaries in
synthetic dimensions by coupling an auxiliary ring resonator
to a dynamically modulated ring, using a platform based on
optical ﬁbers. Recent progress in nanophotonic electro-optic
modulators49,50 incorporated into low-loss microring resonators provide opportunities for scalable on-chip integration of
such concepts. This approach can be generalized to higher
dimensions for exploring nontrivial topological boundary
phenomena25,51,52, both in conventional topological insulators
as well as in higher-order topological insulators. While our
demonstrations were limited to the simplest case of nearestneighbor coupling, there are several ways to create boundaries
in the presence of long-range coupling28,32, a feature that is
readily accessible in synthetic frequency dimensions. Examples
include: (i) using multiple incommensurate rings, (ii) using
perturbations to the cross section of the ring (as recently
demonstrated in ref. 53,54), and (iii) using dispersion engineering of the waveguide that comprises the ring. Our results
also show that the energy of a synthetic lattice can be conﬁned
to a ﬁnite number of sites by coupling to additional auxiliary
resonators, which is critical in efﬁcient implementations of
linear transformations or matrix-vector multiplications21. Our
work should signiﬁcantly advance the capabilities of synthetic
dimensions in both topological photonics and for quantum55
and classical signal processing.
Methods
Experimental details. In this section, we provide a detailed description of the
experimental setup corresponding to Fig. 5 of the main text. The setups for Figs.
2–4 can be obtained by disconnecting the second main ring on the right in Fig. 5a.
We use a ﬁber ring resonator32,46, with a lithium niobate phase modulator in each
ring as the electro-optic modulator (EOM). The rings are excited by a low-noise
continuous-wave laser (RIO Orion)56, with a narrow linewidth <3 kHz. The main
rings have a length of L0 ≈ 38.6 m, corresponding to a free-spectral range (FSR) of
5.35 MHz. Both the main ﬁber rings are coupled to through and drop ports to
enable an independent calibration of the FSR of each ring when the coupling
between the two rings is absent. The FSRs of the two rings are passively equalized
by measuring the FSR of each ring and adding extra lengths of ﬁber or free-space
sections in the second ring to compensate for the difference. The auxiliary ring
consists of a loop of ﬁber containing a ﬁber polarization controller. The electrical
signals used to drive the two modulators are derived from the same ﬁeldprogrammable gate array (FPGA), to ensure phase synchronization over long
timescales. The phase difference between them was precisely controlled in software,
and could be varied across the entire range [0, 2π). By contrast, when independent
function generators were used to drive the two modulators, we observed a continuous drift in the phase offset. Hence it was important to use two modulation
signals derived from the same FPGA clock. The modulation signals were ampliﬁed
by RF ampliﬁers before driving the EOMs. Each of the main rings also had an
erbium-doped ﬁber ampliﬁer (EDFA) to compensate for the losses from the EOM
and other components. The auxiliary ring resonator had no EDFA. The ampliﬁed
spontaneous emission noise from the EDFA was ﬁltered using a dense-wavelength
division multiplexing (DWDM) ﬁlter with a passband of 26.5 GHz centered at
1542.12 nm.
To enable strong coupling between the two rings (Kτp > 1), where τp is the
photon lifetime in the main ring resonators and K is the coupling rate between the
main rings, we use polarization-maintaining (PM) ﬁber components at the
junction between them. This is because the polarization axes of the two rings set by
the EOMs are otherwise independent. The PM sections are illustrated by the blue
ﬁbers in Supplementary Fig. S1. The splitting ratio of the inter-cavity coupler is
75:25, that of the input coupler is 95:5, and that of the auxiliary ring coupler is
60:40. The through port signal was monitored on a slow photodiode (e.g., Fig. 2),
whereas the drop port signal was sent to a fast photodiode with a bandwidth of
5 GHz after optical ampliﬁcation with a semiconductor optical ampliﬁer (not
shown). For band structure measurement (Fig. 4), the drop port signal was directly
sent to the photodiode in this manner. For frequency lattice-space measurements
(Figs. 3 and 5), the drop port output was ﬁrst mixed with the output of an acoustooptic modulator (AOM) before sending it to the fast photodiode. The AOM shifted
a part of the input laser by the RF drive frequency of 500 MHz to enable
heterodyne detection of the cavity output.
Comparison with active mode-locking: In our setup, the presence of both an
EDFA and a modulator is similar to that of an actively mode-locked laser.
However, a few important differences exist: (i) The setup is operated completely
below the lasing threshold; (ii) The input is around the same wavelength as the

NATURE COMMUNICATIONS | (2022)13:3377 | https://doi.org/10.1038/s41467-022-31140-7 | www.nature.com/naturecommunications

## PDF page 7

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-022-31140-7

output in the 1550-nm band, as opposed to lasers where the pump is at a
signiﬁcantly shorter wavelength than the lasing output. In our experiments, the
EDFA only plays the role of mitigating roundtrip losses to achieve a high effective
ﬁnesse for the cavity. If one operates the EDFA at gain higher than the roundtrip
loss, especially with an amplitude modulator, actively mode-locked pulses can be
produced57,58.

Data availability
The data generated in this study have been deposited in the Zenodo database under
accession code 10.5281/zenodo.6516650 (https://doi.org/10.5281/zenodo.6516650).

Code availability
The codes used to process the data generated in this study have been deposited in the
Zenodo database under accession code 10.5281/zenodo.6516650 (https://doi.org/10.5281/
zenodo.6516650).

Received: 4 November 2021; Accepted: 6 June 2022;

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

Boada, O., Celi, A., Latorre, J. I. & Lewenstein, M. Quantum simulation of an
extra dimension. Phys. Rev. Lett. 108, 133001 (2012).
Yuan, L., Lin, Q., Xiao, M. & Fan, S. Synthetic dimension in photonics. Optica
5, 1396–1405 (2018).
Price, H. et al. Roadmap on topological photonics. J. Phys. Photonics https://
doi.org/10.1088/2515-7647/ac4ee4 (2022).
Mancini, M. et al. Observation of chiral edge states with neutral fermions in
synthetic Hall ribbons. Science 349, 1510–1513 (2015).
Yuan, L., Shi, Y. & Fan, S. Photonic gauge potential in a system with a
synthetic frequency dimension. Opt. Lett. 41, 741–744 (2016).
Ozawa, T., Price, H. M., Goldman, N., Zilberberg, O. & Carusotto, I. Synthetic
dimensions in integrated photonics: from optical isolation to four-dimensional
quantum Hall physics. Phys. Rev. A 93, 043827 (2016).
Luo, X.-W. et al. Quantum simulation of 2D topological physics in a 1D array
of optical cavities. Nat. Commun. 6, 7704 (2015).
Regensburger, A. et al. Parity-time synthetic photonic lattices. Nature 488,
167–171 (2012).
Chalabi, H. et al. Synthetic gauge ﬁeld for two-dimensional time-multiplexed
quantum random walks. Phys. Rev. Lett. 123, 150503 (2019).
Leefmans, C. et al. Topological dissipation in a time-multiplexed photonic
resonator network. Nat. Phys. 18, 442–449 (2022).
Lustig, E. et al. Photonic topological insulator in synthetic dimensions. Nature
567, 356–360 (2019).
Thouless, D. J., Kohmoto, M., Nightingale, M. P. & den Nijs, M. Quantized
Hall conductance in a two-dimensional periodic potential. Phys. Rev. Lett. 49,
405–408 (1982).
Su, W. P., Schrieffer, J. R. & Heeger, A. J. Solitons in polyacetylene. Phys. Rev.
Lett. 42, 1698–1701 (1979).
Benalcazar, W. A., Bernevig, B. A. & Hughes, T. L. Quantized electric
multipole insulators. Science 357, 61–66 (2017).
Dutt, A., Minkov, M., Williamson, I. A. D. & Fan, S. Higher-order topological
insulators in synthetic dimensions. Light.: Sci. Appl. 9, 131 (2020).
Mittal, S. et al. Photonic quadrupole topological phases. Nat. Photonics 13,
692–696 (2019).
Okuma, N., Kawabata, K., Shiozaki, K. & Sato, M. Topological origin of nonHermitian skin effects. Phys. Rev. Lett. 124, 086801 (2020).
Weidemann, S. et al. Topological funneling of light. Science 368, 311–314
(2020).
Bergholtz, E. J., Budich, J. C. & Kunst, F. K. Exceptional topology of nonHermitian systems. Rev. Mod. Phys. 93, 015005 (2021).
Ghatak, A., Brandenbourger, M., van Wezel, J. & Coulais, C. Observation of
non-Hermitian topology and its bulk-edge correspondence in an active
mechanical metamaterial. Proc. Natl Acad. Sci. USA 117, 29561–29568
(2020).
Buddhiraju, S., Dutt, A., Minkov, M., Williamson, I. A. D. & Fan, S. Arbitrary
linear transformations for photons in the frequency synthetic dimension. Nat.
Commun. 12, 2401 (2021).
Chen, H. et al. Real-time observation of frequency Bloch oscillations with ﬁbre
loop modulation. Light.: Sci. Appl. 10, 48 (2021).
Lee, N. R. A. et al. Propagation of microwave photons along a synthetic
dimension. Phys. Rev. A 101, 053807 (2020).

ARTICLE

24. Bersch, C., Onishchukov, G. & Peschel, U. Experimental observation of
spectral Bloch oscillations. Opt. Lett. 34, 2372–2374 (2009).
25. Hu, Y., Reimer, C., Shams-Ansari, A., Zhang, M. & Loncar, M. Realization of
high-dimensional frequency crystals in electro-optic microcombs. Optica 7,
1189–1194 (2020).
26. Li, G. et al. Dynamic band structure measurement in the synthetic space. Sci.
Adv. 7, eabe4335 (2021).
27. Dutt, A. et al. A single photonic cavity with two independent physical
synthetic dimensions. Science 367, 59–64 (2020).
28. Wang, K. et al. Multidimensional synthetic chiral-tube lattices via nonlinear
frequency conversion. Light.: Sci. Appl. 9, 132 (2020).
29. Balčytis, A. et al. Synthetic dimension band structures on a Si CMOS photonic
platform. Sci. Adv. 8, eabk0468 (2022).
30. Qin, C. et al. Spectrum control through discrete frequency diffraction
in the presence of photonic Gauge potentials. Phys. Rev. Lett. 120, 133901
(2018).
31. Bell, B. A. et al. Spectral photonic lattices with complex long-range coupling.
Optica 4, 1433–1436 (2017).
32. Dutt, A. et al. Experimental band structure spectroscopy along a synthetic
dimension. Nat. Commun. 10, 3122 (2019).
33. Wang, K. et al. Generating arbitrary topological windings of a non-Hermitian
band. Science 371, 1240–1245 (2021).
34. Wang, K., Dutt, A., Wojcik, C. C. & Fan, S. Topological complex-energy
braiding of non-Hermitian bands. Nature 598, 59–64 (2021).
35. Schwennicke, K. & Yuen-Zhou, J. Enantioselective topological frequency
conversion. J. Phys. Chem. Lett. 13, 2434–2441 (2022).
36. Shan, Q., Yu, D., Li, G., Yuan, L. & Chen, aX. One-way topological states along
vague boundaries in synthetic frequency dimensions including group velocity
dispersion (invited). Prog. Electromagn. Res. 169, 33–43 (2020).
37. Baum, Y. & Refael, G. Setting boundaries with memory: generation of
topological boundary states in ﬂoquet-induced synthetic crystals. Phys. Rev.
Lett. 120, 106402 (2018).
38. Yuan, L., Dutt, A. & Fan, S. Synthetic frequency dimensions in dynamically
modulated ring resonators. APL Photonics 6, 071102 (2021).
39. Haldar, R., Das, S. & Varshney, S. K. Theory and design of off-axis microring
resonators for high-density on-chip photonic applications. J. Lightwave
Technol. 31, 3976–3986 (2013).
40. Souza, M. C. M. M. et al. Embedded coupled microrings with high-ﬁnesse and
close-spaced resonances for optical signal processing. Opt. Express 22, 10430
(2014).
41. Li, G. et al. Observation of ﬂat-band and band transition in the synthetic
space. arXiv:2108.11581 (2021).
42. Wang, J. et al. Simultaneous observation of superluminal and slow light
propagation in a nested ﬁber ring resonator. Opt. Express 18, 13180–13186
(2010).
43. Haldar, R., Banik, A. D. & Varshney, S. K. Design of CMOS compatible and
compact, thermally-compensated electro-optic modulator based on off-axis
microring resonator for dense wavelength division multiplexing applications.
Opt. Express 22, 22411 (2014).
44. Hu, Y. et al. On-chip electro-optic frequency shifters and beam splitters.
Nature 599, 587–593 (2021).
45. Smith, D. D., Chang, H., Fuller, K. A., Rosenberger, A. T. & Boyd, R. W.
Coupled-resonator-induced transparency. Phys. Rev. A 69, 063804 (2004).
46. Dutt, A. et al. Experimental demonstration of dynamical input isolation in
nonadiabatically modulated photonic cavities. ACS Photonics 6, 162–169
(2019).
47. Hügel, D. & Paredes, B. Chiral ladders and the edges of quantum Hall
insulators. Phys. Rev. A 89, 023619 (2014).
48. Wang, Z., Chong, Y. D., Joannopoulos, J. D. & Soljačić, M. Reﬂection-free
one-way edge modes in a gyromagnetic photonic crystal. Phys. Rev. Lett. 100,
013905 (2008).
49. Zhang, M. et al. Broadband electro-optic frequency comb generation in a
lithium niobate microring resonator. Nature 568, 373–377 (2019).
50. Tzuang, L. D., Soltani, M., Lee, Y. H. D. & Lipson, M. High RF carrier
frequency modulation in silicon resonators by coupling adjacent free-spectralrange modes. Opt. Lett. 39, 1799–1802 (2014).
51. Yuan, L. et al. Photonic gauge potential in one cavity with synthetic frequency
and orbital angular momentum dimensions. Phys. Rev. Lett. 122, 083903
(2019).
52. Yuan, L., Xiao, M., Lin, Q. & Fan, S. Synthetic-space with arbitrary dimensions
in a few rings undergoing dynamic modulation. Phys. Rev. B 97, 104105
(2018).
53. Lu, X., Rao, A., Moille, G., Westly, D. A. & Srinivasan, K. Universal
frequency engineering tool for microcavity nonlinear optics: multiple
selective mode splitting of whispering-gallery resonances. Photon. Res. 8,
1676–1686 (2020).
54. Lu, X., McClung, A. & Srinivasan, K. High-Q slow light and its localization in
a photonic crystal microring. Nat. Photon. 16, 66–71 (2022).

NATURE COMMUNICATIONS | (2022)13:3377 | https://doi.org/10.1038/s41467-022-31140-7 | www.nature.com/naturecommunications

7

## PDF page 8

ARTICLE

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-022-31140-7

55. Zhu, X. et al. Hypercubic cluster states in the phase-modulated quantum
optical frequency comb. Optica 8, 281–290 (2021).
56. Numata, K., Camp, J., Krainak, M. A. & Stolpner, L. Performance of planarwaveguide external cavity laser for precision measurements. Opt. Express 18,
22781–22788 (2010).
57. Martin, I. Floquet dynamics of classical and quantum cavity ﬁelds. Ann. Phys.
405, 101–129 (2019).
58. Yuan, L., Lin, Q., Xiao, M., Dutt, A. & Fan, S. Pulse shortening in an actively
mode-locked laser with parity-time symmetry. APL Photonics 3, 086103 (2018).

Additional information
Supplementary information The online version contains supplementary material
available at https://doi.org/10.1038/s41467-022-31140-7.
Correspondence and requests for materials should be addressed to Shanhui Fan.
Peer review information Nature Communications thanks Michael Steel and the other
anonymous reviewer(s) for their contribution to the peer review of this work. Peer review
reports are available.
Reprints and permission information is available at http://www.nature.com/reprints

Acknowledgements
We acknowledge David A. B. Miller for providing lab space and equipment, and Meir
Orenstein and Momchil Minkov for useful discussions. This work is supported by a
Vannevar Bush Faculty Fellowship from the U.S. Department of Defense (Grant No.
N00014-17-1-3030) and a MURI project from the U.S. Air Force Ofﬁce of Scientiﬁc
Research (Grant No. FA9550-18-1-0379). L.Y. also acknowledges the support of the
National Natural Science Foundation of China (11974245, 12122407).

Author contributions
A.D., L.Y., and S.F. conceived the project. A.D. carried out the experiments with assistance from K.Y.Y. and K.W. S.B. and A.D. developed the Floquet simulations. A.D., L.Y.,
K.Y.Y., K.W., J.V., and S.F. discussed the results and contributed to writing the manuscript. S.F. supervised the project.

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

Competing interests
The authors declare no competing interests.

8

© The Author(s) 2022

NATURE COMMUNICATIONS | (2022)13:3377 | https://doi.org/10.1038/s41467-022-31140-7 | www.nature.com/naturecommunications
